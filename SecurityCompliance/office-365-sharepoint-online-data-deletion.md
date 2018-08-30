---
title: Office 365 SharePoint 온라인 데이터 삭제
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
description: SharePoint Online에서 데이터 삭제에 대 한 설명을 합니다.
ms.openlocfilehash: c281f6de9cd9e4978ac4a6997333d71d8835420f
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22533095"
---
# <a name="sharepoint-online-data-deletion-in-office-365"></a><span data-ttu-id="dc599-103">Office 365의에서 SharePoint Online 데이터 삭제</span><span class="sxs-lookup"><span data-stu-id="dc599-103">SharePoint Online Data Deletion in Office 365</span></span>

<span data-ttu-id="dc599-p101">SharePoint Online 응용 프로그램 데이터베이스 내에서 추상화 된 코드로 개체를 저장합니다. SharePoint Online에 파일을 업로드 하는 사용자 때 해당 파일은 분해 하 고 응용 프로그램 코드로 변환 하 고 여러 데이터베이스에 걸쳐 여러 테이블에 저장 합니다. SharePoint Online에서 고객을 업로드 하는 모든 콘텐츠 (잠재적으로 사용 하 여 암호화 여러 AES 256 비트 키), 청크를 나누어 이며 데이터 센터에 걸쳐 분산 합니다. 청크와 암호화 프로세스에 대 한 구체적인 정보에 대 한 [Microsoft 클라우드에서 암호화](office-365-encryption-in-the-microsoft-cloud-overview.md)를 참조 하십시오. SharePoint Online 데이터 손실을 방지 하려면 데이터 보호 서비스 제공 됩니다. 특히, 백업은 12 시간 마다 수행 되며 14 일 동안 보존 됩니다.</span><span class="sxs-lookup"><span data-stu-id="dc599-p101">SharePoint Online stores objects as abstracted code within application databases. When a user uploads a file to SharePoint Online, that file is disassembled and translated into application code and stored in multiple tables across multiple databases. In SharePoint Online, all content that a customer uploads is broken into chunks, encrypted (potentially with multiple AES 256-bit keys), and distributed across the datacenter. For specific details about the chunking and encryption process, see [Encryption in the Microsoft Cloud](office-365-encryption-in-the-microsoft-cloud-overview.md). Data protection services are provided to prevent the loss of SharePoint Online data. Specifically, backups are performed every 12 hours and retained for 14 days.</span></span>

<span data-ttu-id="dc599-p102">SharePoint Online 사이트에서 콘텐츠를 삭제 하면 즉시 삭제 되지 않습니다. 필요한 경우을 사이트 휴지통으로, 여기서 복원할 수, 보내집니다. (참조 [삭제 된 사이트 모음 휴지통에서 항목 복원](https://support.office.com/article/Restore-deleted-items-from-the-site-collection-recycle-bin-5fa924ee-16d7-487b-9a0a-021b9062d14b) 복원 단계에 대 한). 기본 사이트 휴지통 보존 시간은 약 90 일입니다. 사이트 휴지통에서 콘텐츠를 삭제 하는 경우 사이트 모음 휴지통으로, 30 일의 보존 시간을 가진 하는 전송 됩니다. 관리자가 휴지통에서 항목을 유지 하는 시간을 구성할 수 있습니다 하지만 기본 보존 기간은 약 90 일이 없는 경우에는, 합니다. 사이트 모음 저장 용량 할당량 및 [목록 보기 임계값](https://support.office.com/article/List-View-Threshold-b8588dae-9387-48c2-9248-c24122f07c59)에 대해 사이트 recycle bin 저장소를 계산합니다.</span><span class="sxs-lookup"><span data-stu-id="dc599-p102">When you delete content from a SharePoint Online site, it's not deleted immediately. It's sent to a Site Recycle Bin, where it can be restored, if needed. (See [Restore deleted items from the site collection recycle bin](https://support.office.com/article/Restore-deleted-items-from-the-site-collection-recycle-bin-5fa924ee-16d7-487b-9a0a-021b9062d14b) for restore steps.) The default Site Recycle Bin retention time is about 90 days. If you delete content from a Site Recycle Bin, it's sent to the Site Collection Recycle Bin, which has a retention time of 30 days. The length of time to keep things in the recycle bin can be configured by an administrator, but in the absence of that, the default retention period is about 90 days. The site recycle bin storage counts against site collection storage quota and the [List View Threshold](https://support.office.com/article/List-View-Threshold-b8588dae-9387-48c2-9248-c24122f07c59).</span></span>

<span data-ttu-id="dc599-116">사이트 모음을 삭제 하는 경우에 컬렉션에 있는 모든 콘텐츠 및 사용자 정보를 포함 하는 사이트의 계층 구조를 삭제 하려는 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dc599-116">When you delete a site collection, you're also deleting the hierarchy of sites in the collection, including all content and user information:</span></span>
- <span data-ttu-id="dc599-117">문서 및 문서 라이브러리</span><span class="sxs-lookup"><span data-stu-id="dc599-117">Documents and document libraries</span></span>
- <span data-ttu-id="dc599-118">목록 및 목록 데이터</span><span class="sxs-lookup"><span data-stu-id="dc599-118">Lists and list data</span></span>
- <span data-ttu-id="dc599-119">사이트 구성 설정</span><span class="sxs-lookup"><span data-stu-id="dc599-119">Site configuration settings</span></span>
- <span data-ttu-id="dc599-120">사이트 또는 사이트의 하위 사이트와 관련 된 역할 및 보안 정보</span><span class="sxs-lookup"><span data-stu-id="dc599-120">Role and security information that is related to the site or its subsites</span></span>
- <span data-ttu-id="dc599-121">하위 사이트의 최상위 웹사이트, 콘텐츠 및 사용자 정보</span><span class="sxs-lookup"><span data-stu-id="dc599-121">Subsites of the top-level website, their contents, and user information</span></span>

<span data-ttu-id="dc599-p103">사이트 모음을 삭제 하기 전에에서는 SharePoint Online 사이트에 대 한 Microsoft에 의해 유지 관리 하는 데이터 백업 일정에 설명 하는 계획을 위한 SharePoint Online 서비스 설명을 검토 하는 것이 좋습니다. 또한 백업에서 복원을 수 있는 메모는 사이트 모음 또는 하위 사이트, 파일, 목록 또는 라이브러리에 대해서만 있습니다. 이러한 복구 해야하는 경우 휴지통을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="dc599-p103">Before you delete a site collection, we recommend you review the SharePoint Online Service Description for your plan, which outlines the data backup schedule maintained by Microsoft for SharePoint Online sites. Also note that restorations from backups can are only for site collections or sub-sites, not for files, lists, or libraries. If you need to recover those, use the Recycle Bin.</span></span>

<span data-ttu-id="dc599-p104">사이트 모음을 실수로 삭제 한 경우 복원할 수는 사이트 모음 휴지통에서 사이트 모음 관리자가 30 일 내에 있습니다. 30 일 후에 복원 하는 사이트 모음, 필요한 경우 복원할 수 Microsoft가 30 일 만료에서 14 일 내에서 서비스 요청을 통해 Microsoft에 문의 하 여 합니다.</span><span class="sxs-lookup"><span data-stu-id="dc599-p104">If you accidentally delete a site collection, it can be restored from the Site Collection Recycle Bin by a Site Collection Administrator within 30 days. If you need a site collection restored after 30 days, it can be restored by Microsoft within 14 days from the 30-day expiration by contacting Microsoft via a Service Request.</span></span>

<span data-ttu-id="dc599-p105">하드 삭제 하거나 [Remove-spodeletedsite cmdlet](https://docs.microsoft.com/powershell/module/sharepoint-online/Remove-SPODeletedSite?view=sharepoint-ps)을 사용 하 여 사이트 모음을 영구적으로 삭제 하는 관리자는 사용자가 사이트 휴지통에서 삭제 된 항목을 제거 하 고 보존 및 백업 기간 만료 될 때 발생 합니다. 사용자 하드 삭제 하는 경우 (영구적으로 삭제 또는 제거) SharePoint Online에서 콘텐츠를 삭제 된 청크에 대 한 모든 암호화 키도 삭제 됩니다. 이전에 삭제 된 청크를 저장 하는 디스크에 대 한 차단은 사용 하지 않는 되어 사용할 수는 다시 사용으로 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="dc599-p105">Hard deletion occurs when a user purges deleted items from the Site Recycle Bin, and the retention and backup periods expire, or when an administrator permanently deletes a site collection using the [Remove-SPODeletedSite cmdlet](https://docs.microsoft.com/powershell/module/sharepoint-online/Remove-SPODeletedSite?view=sharepoint-ps). When a user hard deletes (permanently deletes, or purges) content from SharePoint Online, all encryption keys for the deleted chunks are also deleted. The blocks on the disks that previously stored the deleted chunks are marked as unused and available for re-use.</span></span>
