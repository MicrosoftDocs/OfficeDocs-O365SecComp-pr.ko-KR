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
ms.collection: Strat_O365_Enterprise
description: Office 365의 SharePoint Online에서 데이터 복구를 간략하게 설명 합니다.
ms.openlocfilehash: ba6259e8e582a4abcf0f184b162177119a57718f
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22533499"
---
# <a name="sharepoint-online-data-resiliency"></a>SharePoint Online 데이터 복구
SharePoint Online에 대 한 주요 원칙은 하지 모든 데이터의 단일 복사본을 포함 하는 것입니다. SharePoint Online 집합인 기술을 복사 하 고 다른 하나 데이터베이스에서 데이터 및 데이터베이스 개체를 배포 하 고, 다음 일관성을 유지 하기 위해 데이터베이스 간의 동기화를 수행 하는 SQL Server 복제를 사용 합니다. 

등 SharePoint Online에서 파일을 저장 하는 사용자, 하는 경우 파일은 청크 분할 된, 암호화 및 Azure Blob 저장소 내에 저장 합니다. Azure Blob 서비스 데이터 무결성을 보장 두 응용 프로그램 및 전송 계층에서 하는 메커니즘을 제공 합니다. 이 게시물 서비스 및 클라이언트 관점에서 볼 때 이러한 메커니즘에 자세히 설명 합니다. MD5 검사 하는 것은 모두 PUT 및 GET 작업;에서 선택 사항 그러나 HTTP를 사용 하는 경우 네트워크를 통해 데이터 무결성을 보장 하는 편리 하 게 기능을 제공 합니다. 또한 HTTPS 추가 전송 계층 보안을 제공 하므로 MD5 검사 필요 하지 않은 중복 된 것 처럼 HTTPS를 통해 연결 하는 동안 합니다. Azure Blob 서비스 지 속성 저장소 중간 규모를 제공 하 고 자체 무결성 저장 된 데이터에 대 한 검사를 사용 합니다. MD5의 응용 프로그램와 상호작용 하는 경우에 사용 되는 데이터의 무결성을 확인 하는 응용 프로그램 및 서비스 간의 HTTP를 통해 해당 데이터를 전송할 때 제공 됩니다. 

Azure Blob 데이터 무결성을 보장 하려면 서비스 데이터의 MD5 해시를 사용 하 여 몇 다른 방법에 있습니다. 것은 어떻게 이러한 값은 계산, 전송, 저장 및 적절 하 게 데이터 무결성을 제공 하 여 활용 하도록 응용 프로그램을 디자인 하는 결국 적용을 이해 하는 것이 중요 합니다. 자세한 내용은 [Windows Azure Blob MD5 개요](http://blogs.msdn.com/b/windowsazurestorage/archive/2011/02/18/windows-azure-blob-md5-overview.aspx)를 참조 하십시오. 

메타 데이터 및 파일에 대 한 포인터는 SQL Server 데이터베이스 (콘텐츠 데이터베이스)에 저장 됩니다. -파일, 파일 및 업데이트 델타의 부분-모든 청크 여러 Azure 저장소 계정에 분산 임의로 Azure 저장소에서 blob로 저장 됩니다. SQL 데이터베이스는 동일한 데이터 센터 내에서 별도 랙에서 다른 RAID 10 저장소 배열에 동기적으로 미러링 되는 RAID 10 저장소 배열에서 호스팅됩니다. 비동기 로그 전달 보조 데이터 센터의 다른 RAID 10 저장소 배열에 데이터를 복제에 사용 됩니다. RAID 10 및 동기 및 비동기 복제를 사용 하 여 데이터를 보호 하는 경우, 외에도 예약 된 데이터를 백업 하는 비동기적으로 보조 데이터 센터에 복제 수행 됩니다. 

SharePoint Online에서 데이터를 백업 12 시간 마다 수행 하 고 14 일 동안 보존 됩니다. SharePoint Online 영역 내에서 동일한 고객 데이터 위치 (예: 시카고 및 프로 비전 자신의 테 넌 트 미국의 경우에는 고객에 대 한 샌안토니오) 쌍으로 지정 된 지리적으로 별도 데이터 센터를 포함 하는 핫 대기 시스템에도 사용 액티브/액티브 구성합니다. 예, 시카고가 기본 데이터 센터 및 장애 조치 데이터 센터도 샌안토니오도 있고 해당 기본 데이터 센터 및 장애 조치 데이터 센터와 시카고도 샌안토니오 수 있는 사용자를 live에 live 사용자가 있습니다. 