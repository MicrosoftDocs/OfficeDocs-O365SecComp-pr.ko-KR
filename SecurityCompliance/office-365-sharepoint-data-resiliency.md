---
title: Office 365 SharePoint 데이터 복구
ms.author: robmazz
author: robmazz
manager: laurawi
ms.date: 8/21/2018
audience: ITPro
ms.topic: article
ms.service: Office 365 Administration
localization_priority: None
search.appverid:
- MET150
ms.collection:
- Strat_O365_IP
- M365-security-compliance
description: Office 365에서 SharePoint Online의 데이터 복구에 대 한 개요를 설명 합니다.
ms.openlocfilehash: c550cb6572cb71b53cd544af64339129f72b888f
ms.sourcegitcommit: c94cb88a9ce5bcc2d3c558f0fcc648519cc264a2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/20/2019
ms.locfileid: "30090890"
---
# <a name="sharepoint-online-data-resiliency"></a><span data-ttu-id="4273b-103">SharePoint Online 데이터 복구</span><span class="sxs-lookup"><span data-stu-id="4273b-103">SharePoint Online Data Resiliency</span></span>
<span data-ttu-id="4273b-p101">SharePoint Online의 주요 원칙은 데이터의 단일 복사본을 사용 하지 않는 것입니다. SharePoint Online은 SQL Server 복제를 사용 하 여 데이터베이스 간에 데이터 및 데이터베이스 개체를 복사 하 고 분산 한 다음 일관성을 유지 하기 위해 데이터베이스를 동기화 하는 데 사용할 수 있는 기술 집합입니다.</span><span class="sxs-lookup"><span data-stu-id="4273b-p101">A key principle for SharePoint Online is to never have a single copy of any piece of data. SharePoint Online uses SQL Server replication, which is a set of technologies for copying and distributing data and database objects from one database to another, and then synchronizing between databases to maintain consistency.</span></span> 

<span data-ttu-id="4273b-p102">예를 들어 사용자가 SharePoint Online에서 파일을 저장 하면 파일이 파일을 청크 분할, 암호화 및 Azure Blob storage 내에 저장 됩니다. Azure Blob service는 응용 프로그램 및 전송 계층에서 데이터 무결성을 보장 하는 메커니즘을 제공 합니다. 이 게시물은 서비스 및 클라이언트 측면에서 이러한 메커니즘을 자세히 설명 합니다. MD5 확인은 PUT 및 GET 작업에서 모두 선택 사항입니다. 그러나 HTTP를 사용 하는 경우 네트워크를 통한 데이터 무결성을 보장 하기 위한 편리한 기능을 제공 합니다. 또한 https는 전송 계층 보안을 제공 하기 때문에 https를 통해 연결 하는 동안에는 중복을 위해 MD5 확인을 추가로 수행 하지 않아도 됩니다. Azure Blob service는 영속적 저장소 미디어를 제공 하며 저장 된 데이터에 대 한 자체 무결성 확인을 사용 합니다. 응용 프로그램과 상호 작용 하는 데 사용 되는 MD5's는 응용 프로그램 및 서비스 간에 HTTP를 통해 데이터를 전송할 때 데이터의 무결성을 확인 하기 위해 제공 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4273b-p102">For example, when a user saves a file in SharePoint Online, the file is chunked, encrypted, and stored within Azure Blob storage. Azure Blob service provides mechanisms to ensure data integrity both at the application and transport layers. This post will detail these mechanisms from the service and client perspective. MD5 checking is optional on both PUT and GET operations; however, it does provide a convenience facility to ensure data integrity across the network when using HTTP. Additionally, since HTTPS provides transport layer security additional MD5 checking is not needed while connecting over HTTPS as it would be redundant. Azure Blob service provides a durable storage medium, and uses its own integrity checking for stored data. The MD5's that are used when interacting with an application are provided for checking the integrity of the data when transferring that data between the application and service via HTTP.</span></span> 

<span data-ttu-id="4273b-p103">데이터 무결성을 보장 하기 위해 Azure Blob service에서는 두 가지 다른 manners에서 데이터에 대 한 MD5 해시를 사용 합니다. 이러한 값은 데이터 무결성을 제공 하기 위해 응용 프로그램을 적절히 디자인 하기 위해 계산, 전송 및 저장 된 방식을 이해 하는 것이 중요 합니다. 자세한 내용은 [Windows Azure Blob MD5 개요](http://blogs.msdn.com/b/windowsazurestorage/archive/2011/02/18/windows-azure-blob-md5-overview.aspx)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="4273b-p103">To ensure data integrity the Azure Blob service uses MD5 hashes of the data in a couple different manners. It is important to understand how these values are calculated, transmitted, stored, and eventually enforced to appropriately design your application to utilize them to provide data integrity. For more information, see [Windows Azure Blob MD5 Overview](http://blogs.msdn.com/b/windowsazurestorage/archive/2011/02/18/windows-azure-blob-md5-overview.aspx).</span></span> 

<span data-ttu-id="4273b-p104">메타 데이터 및 파일에 대 한 포인터는 SQL Server 데이터베이스 (콘텐츠 데이터베이스)에 저장 됩니다. 모든 청크 파일, 파일 조각 및 업데이트 델타는 여러 azure 저장소 계정에 무작위로 분산 되는 azure 저장소의 blob로 저장 됩니다. SQL 데이터베이스는 동일한 데이터 센터 내에서 별도의 랙에 다른 raid 10 저장소 배열에 동기식으로 미러링 되는 raid 10 저장소 배열에 호스트 됩니다. 그런 다음 두 번째 데이터 센터의 다른 RAID 10 저장소 배열에 데이터를 복제 하기 위해 비동기 로그 전달을 사용 합니다. RAID 10, 동기 및 비동기 복제를 사용 하 여 데이터를 보호 하는 것 외에도, 예정 된 데이터 백업이 두 번째 데이터 센터에 비동기식으로 복제 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4273b-p104">Metadata and pointers to the file are stored in a SQL Server database (the content database). All the chunks – files, pieces of files, and update deltas – are stored as blobs in Azure storage that are randomly distributed across multiple Azure storage accounts. The SQL database is hosted on a RAID 10 storage array which is synchronously mirrored to another RAID 10 storage array in a separate rack within the same datacenter. Asynchronous log shipping is then used to replicate the data to another RAID 10 storage array in a second datacenter. In addition to protecting data with RAID 10 and synchronous and asynchronous replication, scheduled data backups are taken which are also asynchronously replicated to the second datacenter.</span></span> 

<span data-ttu-id="4273b-p105">SharePoint Online에서 데이터 백업은 12 시간 마다 수행 되며 14 일 동안 보존 됩니다. 또한 SharePoint Online에서는 미국에서 테 넌 트를 프로 비전 한 고객을 위한 시카고 및 San Antonio 같은 고객 데이터 위치 영역 내에 지리적으로 구분 된 여러 데이터 센터가 있는 활성 대기 시스템을 사용 합니다. 활성/활성으로 구성 됩니다. 예를 들어 시카고가 기본 데이터 센터이 고 san Antonio가 장애 조치 데이터 센터로 인 한 live 사용자와 san Antonio가 장애 조치 (failover) 데이터 센터 인 실제 사용자가 기본 데이터 센터 및 시카고로 유지 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4273b-p105">In SharePoint Online, data backups are performed every 12 hours and retained for 14 days. SharePoint Online also uses a hot standby system that includes paired geographically-separate datacenters within the same customer data location region (for example, Chicago and San Antonio for customers who have provisioned their tenant in the United States) configured as active/active. For example, there are live users that have Chicago as their primary datacenter and San Antonio as a failover datacenter, and live users that have San Antonio as their primary datacenter and Chicago as their failover datacenter.</span></span> 