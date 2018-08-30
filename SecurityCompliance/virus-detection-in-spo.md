---
title: SharePoint Online에서 바이러스 검색
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 4/17/2018
ms.audience: Admin
ms.topic: reference
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- SPO160
- MOE150
- MET150
ms.assetid: e3c6df61-8513-499d-ad8e-8a91770bff63
description: Office 365 SharePoint online 사용자가 업로드 하는 파일에서 바이러스를 검색 하 여 사용자 환경에서 맬웨어 보호 도움이 됩니다. 파일을 업로드할 때문 서 한 후에 대 한 바이러스 검색 됩니다. 감염 된 것 파일을 찾으면 사용자 수 없도록 다운로드 하거나이 파일을 동기화 한 속성이 설정 됩니다.
ms.openlocfilehash: 22e983d35283ff96e1469fdf913e25b8d1d1c485
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22533754"
---
# <a name="virus-detection-in-sharepoint-online"></a><span data-ttu-id="a8090-105">SharePoint Online에서 바이러스 검색</span><span class="sxs-lookup"><span data-stu-id="a8090-105">Virus detection in SharePoint Online</span></span>

<span data-ttu-id="a8090-p102">Office 365 SharePoint online 사용자가 업로드 하는 파일에서 바이러스를 검색 하 여 사용자 환경에서 맬웨어 보호 도움이 됩니다. 파일을 업로드할 때문 서 한 후에 대 한 바이러스 검색 됩니다. 감염 된 것 파일을 찾으면 사용자 수 없도록 다운로드 하거나이 파일을 동기화 한 속성이 설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a8090-p102">Office 365 can help protect your environment from malware by detecting viruses in files that users upload to SharePoint Online. Files are scanned for viruses after they are uploaded. If a file is found to be infected, a property is set so that users can't download or sync the file.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="a8090-p103">SharePoint Online에서 이러한 바이러스 백신 기능은 바이러스를 포함 하는 방법을 사용 하는 것입니다. 이러한 환경에 대 한 맬웨어에 대 한 방어의 단일 지점으로 의도 되지 않습니다. 모든 고객을 평가 하 고 다양 한 계층에서 맬웨어 방지 보호 기능을 구현 하 고 엔터프라이즈 인프라를 보호 하는 것에 대 한 모범 사례를 적용 하는 것이 좋습니다. 전략 및 모범 사례에 대 한 자세한 내용은 [Office 365에 대 한 보안 모범 사례](security-best-practices.md)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="a8090-p103">These antivirus capabilities in SharePoint Online are a way to contain viruses. They aren't intended as a single point of defense against malware for your environment. We encourage all customers to assess and implement antimalware protection at various layers and apply best practices for securing your enterprise infrastructure. For more information about strategies and best practices, see [Security best practices for Office 365](security-best-practices.md).</span></span> 
  
## <a name="what-happens-when-an-infected-file-is-uploaded-to-sharepoint-online"></a><span data-ttu-id="a8090-113">SharePoint Online에 감염된 된 파일은 업로드 되 면 어떻게 됩니까?</span><span class="sxs-lookup"><span data-stu-id="a8090-113">What happens when an infected file is uploaded to SharePoint Online?</span></span>

<span data-ttu-id="a8090-p104">Office 365 일반적인 바이러스 검색 엔진을 사용합니다. 엔진 내 SharePoint Online에서 비동기적으로 실행 하 고 업로드는 하 고 나면 파일을 검사 합니다. 파일에 바이러스가 포함 하도록 발견 되 면 다시 다운로드할 수 있도록 플래그가 지정 됩니다. 4 월 2018에서 스캔 한 파일에 대 한 25MB 제한이 제거 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="a8090-p104">Office 365 uses a common virus detection engine. The engine runs asynchronously within SharePoint Online, and scans files after they're uploaded. When a file is found to contain a virus, it's flagged so that it can't be downloaded again. In April 2018, we removed the 25 MB limit for scanned files.</span></span>
  
<span data-ttu-id="a8090-118">수행 되는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="a8090-118">Here's what happens:</span></span>
  
1. <span data-ttu-id="a8090-119">SharePoint Online에 파일을 업로드 하는 사용자입니다.</span><span class="sxs-lookup"><span data-stu-id="a8090-119">A user uploads a file to SharePoint Online.</span></span>
    
2. <span data-ttu-id="a8090-120">바이러스 검색 엔진에서 파일을 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="a8090-120">The virus detection engine scans the file.</span></span>
    
3. <span data-ttu-id="a8090-121">바이러스가 발견 되는 경우 바이러스 엔진 나타내는 감염 된 파일의 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8090-121">If a virus is found, the virus engine sets a property on the file indicating that it is infected.</span></span>
    
## <a name="what-happens-when-a-user-tries-to-download-an-infected-file-by-using-the-browser"></a><span data-ttu-id="a8090-122">사용자가 브라우저를 사용 하 여 감염된 된 파일을 다운로드 하려고 할 때 수행 하는 작업</span><span class="sxs-lookup"><span data-stu-id="a8090-122">What happens when a user tries to download an infected file by using the browser?</span></span>

<span data-ttu-id="a8090-123">파일은 바이러스에 감염 된, 하는 경우 사용자는 브라우저를 사용 하 여 파일을 SharePoint Online에서 다운로드할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="a8090-123">If a file is infected with a virus, users can't download the file from SharePoint Online by using the browser.</span></span>
  
<span data-ttu-id="a8090-124">수행 되는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="a8090-124">Here's what happens:</span></span>
  
1. <span data-ttu-id="a8090-125">사용자가 웹 브라우저를 열고 및 SharePoint Online에서 감염 된 파일을 다운로드 하려고 시도 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8090-125">A user opens a web browser and tries to download an infected file from SharePoint Online.</span></span>
    
2. <span data-ttu-id="a8090-126">사용자 경고 바이러스에서 발견 된 파일을 다운로드 하려면 옵션이 제공 됩니다 및 자신의 바이러스 소프트웨어를 사용 하 여 치료 시도 되었는지에 제공 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a8090-126">The user is given a warning that a virus has been detected, and is given the option to download the file and attempt to clean it using their own virus software.</span></span>
    
## <a name="what-happens-when-the-onedrive-sync-client-tries-to-sync-an-infected-file"></a><span data-ttu-id="a8090-127">OneDrive 동기화 클라이언트는 감염 된 파일을 동기화 하 려 면 어떻게 됩니까?</span><span class="sxs-lookup"><span data-stu-id="a8090-127">What happens when the OneDrive sync client tries to sync an infected file?</span></span>

<span data-ttu-id="a8090-p105">파일에는 바이러스를 포함 하는 경우 새 OneDrive 동기화 클라이언트 (OneDrive.exe) 또는 비즈니스 동기화 클라이언트 (Groove.exe)에 대 한 이전 OneDrive 파일을 동기화 하는 사용자, 여부 동기화 클라이언트 다운로드 되지 않습니다. 동기화 클라이언트 파일 동기화 할 수 없습니다는 알림이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a8090-p105">Whether users sync files with the new OneDrive sync client (OneDrive.exe) or the previous OneDrive for Business sync client (Groove.exe), if a file contains a virus, the sync client won't download it. The sync client will display a notification that the file can't be synced.</span></span>
  

