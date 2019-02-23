---
title: SharePoint Online의 바이러스 검색
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 01/14/2019
ms.audience: Admin
ms.topic: reference
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- SPO160
- MOE150
- MET150
ms.assetid: e3c6df61-8513-499d-ad8e-8a91770bff63
description: Office 365은 사용자가 SharePoint Online에 업로드 하는 파일에서 바이러스를 검색 하 여 맬웨어 로부터 환경을 보호 하는 데 도움이 됩니다. 업로드 후 파일에서 바이러스를 검사 합니다. 파일이 감염 된 것으로 확인 되 면 사용자가 파일을 다운로드 하거나 동기화 할 수 없도록 속성이 설정 됩니다.
ms.openlocfilehash: d39a5be525e25de8206e8d4219d9c83bfa6eaae0
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30212968"
---
# <a name="virus-detection-in-sharepoint-online"></a><span data-ttu-id="a8c4e-105">SharePoint Online의 바이러스 검색</span><span class="sxs-lookup"><span data-stu-id="a8c4e-105">Virus detection in SharePoint Online</span></span>

<span data-ttu-id="a8c4e-p102">Office 365은 사용자가 SharePoint Online에 업로드 하는 파일에서 바이러스를 검색 하 여 맬웨어 로부터 환경을 보호 하는 데 도움이 됩니다. 업로드 후 파일에서 바이러스를 검사 합니다. 파일이 감염 된 것으로 확인 되 면 사용자가 파일을 다운로드 하거나 동기화 할 수 없도록 속성이 설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a8c4e-p102">Office 365 can help protect your environment from malware by detecting viruses in files that users upload to SharePoint Online. Files are scanned for viruses after they are uploaded. If a file is found to be infected, a property is set so that users can't download or sync the file.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="a8c4e-p103">SharePoint Online의 이러한 바이러스 백신 기능은 바이러스를 포함 하는 방법입니다. 사용자 환경에 대 한 맬웨어를 방어 하기 위한 단일 방어선이 아닙니다. 모든 고객은 다양 한 계층에서 맬웨어 방지 보호 기능을 평가 및 구현 하 고 엔터프라이즈 인프라를 보호 하기 위한 모범 사례를 적용할 것을 권장 합니다. 전략 및 모범 사례에 대 한 자세한 내용은 [Office 365에 대 한 보안 모범 사례](security-best-practices.md)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="a8c4e-p103">These antivirus capabilities in SharePoint Online are a way to contain viruses. They aren't intended as a single point of defense against malware for your environment. We encourage all customers to assess and implement antimalware protection at various layers and apply best practices for securing your enterprise infrastructure. For more information about strategies and best practices, see [Security best practices for Office 365](security-best-practices.md).</span></span> 
  
## <a name="what-happens-when-an-infected-file-is-uploaded-to-sharepoint-online"></a><span data-ttu-id="a8c4e-113">감염 된 파일을 SharePoint Online에 업로드 한 경우 어떻게 되나요?</span><span class="sxs-lookup"><span data-stu-id="a8c4e-113">What happens when an infected file is uploaded to SharePoint Online?</span></span>

<span data-ttu-id="a8c4e-p104">Office 365에서는 일반적인 바이러스 검색 엔진을 사용 합니다. 엔진이 SharePoint Online 내에서 비동기적으로 실행 되며 업로드 된 후 파일을 검사 합니다. 바이러스를 포함 하는 파일을 찾으면 다시 다운로드할 수 없도록 플래그가 지정 됩니다. 2018 년 4 월에는 검색 된 파일에 대 한 250mb 제한이 제거 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="a8c4e-p104">Office 365 uses a common virus detection engine. The engine runs asynchronously within SharePoint Online, and scans files after they're uploaded. When a file is found to contain a virus, it's flagged so that it can't be downloaded again. In April 2018, we removed the 25 MB limit for scanned files.</span></span>
  
<span data-ttu-id="a8c4e-118">수행 되는 작업은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="a8c4e-118">Here's what happens:</span></span>
  
1. <span data-ttu-id="a8c4e-119">사용자가 파일을 SharePoint Online에 업로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8c4e-119">A user uploads a file to SharePoint Online.</span></span>
    
2. <span data-ttu-id="a8c4e-120">바이러스 검색 엔진이 파일을 검사 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8c4e-120">The virus detection engine scans the file.</span></span>
    
3. <span data-ttu-id="a8c4e-121">바이러스가 발견 되 면 바이러스 엔진은 파일에서 감염 되었음을 나타내는 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8c4e-121">If a virus is found, the virus engine sets a property on the file indicating that it is infected.</span></span>
    
## <a name="what-happens-when-a-user-tries-to-download-an-infected-file-by-using-the-browser"></a><span data-ttu-id="a8c4e-122">사용자가 브라우저를 사용 하 여 감염 된 파일을 다운로드 하려고 하면 어떻게 되나요?</span><span class="sxs-lookup"><span data-stu-id="a8c4e-122">What happens when a user tries to download an infected file by using the browser?</span></span>

<span data-ttu-id="a8c4e-123">파일이 바이러스에 감염 된 경우 사용자는 브라우저를 사용 하 여 SharePoint Online에서 파일을 다운로드할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="a8c4e-123">If a file is infected with a virus, users can't download the file from SharePoint Online by using the browser.</span></span>
  
<span data-ttu-id="a8c4e-124">수행 되는 작업은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="a8c4e-124">Here's what happens:</span></span>
  
1. <span data-ttu-id="a8c4e-125">사용자가 웹 브라우저를 열고 SharePoint Online에서 감염 된 파일을 다운로드 하려고 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8c4e-125">A user opens a web browser and tries to download an infected file from SharePoint Online.</span></span>
    
2. <span data-ttu-id="a8c4e-p105">사용자에 게 바이러스가 감지 되었음을 알리는 경고가 표시 됩니다. 사용자에 게 파일을 다운로드 하 고 자체 바이러스 백신 소프트웨어를 사용 하 여 복구를 시도할 수 있는 옵션이 제공 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a8c4e-p105">The user is given a warning that a virus has been detected. The user is given the option to download the file and attempt to clean it using their own virus software.</span></span>

> [!NOTE]
> <span data-ttu-id="a8c4e-p106">**DisallowInfectedFileDownload** 매개 변수와 함께 set-spotenant cmdlet을 사용 하 여 바이러스 백신 경고 창 에서도 검색 된 파일을 다운로드할 수 없습니다. [DisallowInfectedFileDownload] (https://docs.microsoft.com/powershell/module/sharepoint-online/Set-SPOTenant)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="a8c4e-p106">You can use the Set-SPOTenant cmdlet with the **DisallowInfectedFileDownload** parameter to not allow users to download a detected file, even in the anti-virus warning window. See [DisallowInfectedFileDownload] (https://docs.microsoft.com/powershell/module/sharepoint-online/Set-SPOTenant).</span></span>
    
## <a name="what-happens-when-the-onedrive-sync-client-tries-to-sync-an-infected-file"></a><span data-ttu-id="a8c4e-130">OneDrive 동기화 클라이언트가 감염 된 파일을 동기화 하려고 할 때 수행 되는 작업</span><span class="sxs-lookup"><span data-stu-id="a8c4e-130">What happens when the OneDrive sync client tries to sync an infected file?</span></span>

<span data-ttu-id="a8c4e-p107">사용자가 새 onedrive 동기화 클라이언트 (excel.exe) 또는 이전 비즈니스용 onedrive 동기화 클라이언트 (Groove)를 사용 하 여 파일을 동기화 하는지 여부에 관계 없이 파일에 바이러스가 포함 되어 있으면 동기화 클라이언트에서 다운로드 하지 않습니다. 동기화 클라이언트에서는 파일을 동기화 할 수 없다는 알림을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8c4e-p107">Whether users sync files with the new OneDrive sync client (OneDrive.exe) or the previous OneDrive for Business sync client (Groove.exe), if a file contains a virus, the sync client won't download it. The sync client will display a notification that the file can't be synced.</span></span>
  

