---
title: SharePoint, OneDrive 및 Microsoft Teams에 대한 Office 365 ATP
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 26261670-db33-4c53-b125-af0662c34607
description: SharePoint Online, 조직에 대 한 안전 하 게 공동 작업을 통해 비즈니스 및 Microsoft 팀의 비즈니스용 OneDrive의 파일을 Office 365 고급 위협 보호를 확장 합니다.
ms.openlocfilehash: ff07d88a150d3f059681556feec9a5e89b5875a8
ms.sourcegitcommit: 099bbfb1d16b251fd5cf18ec6515faaf9a989176
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25454325"
---
# <a name="office-365-atp-for-sharepoint-onedrive-and-microsoft-teams"></a><span data-ttu-id="199d0-103">SharePoint, OneDrive 및 Microsoft Teams에 대한 Office 365 ATP</span><span class="sxs-lookup"><span data-stu-id="199d0-103">Office 365 ATP for SharePoint, OneDrive, and Microsoft Teams</span></span>

## <a name="overview-of-office-365-atp-for-sharepoint-onedrive-and-microsoft-teams"></a><span data-ttu-id="199d0-104">SharePoint, OneDrive 및 팀이 Microsoft Office 365 ATP의 개요 (영문)</span><span class="sxs-lookup"><span data-stu-id="199d0-104">Overview of Office 365 ATP for SharePoint, OneDrive, and Microsoft Teams</span></span>

<span data-ttu-id="199d0-p101">파일 공유를 정기적으로 사용자 및 SharePoint, OneDrive 및 Microsoft 팀을 사용 하 여 공동 작업을 수행 합니다. [Office 365 고급 위협 보호](office-365-atp.md) ATP ()와 함께 조직 보다 안전한 방식으로 공동 작업할 수 있습니다. ATP를 검색 하 고 팀 사이트 및 문서 라이브러리에서 악성으로 식별 되는 파일을 차단 합니다.</span><span class="sxs-lookup"><span data-stu-id="199d0-p101">People regularly share files and collaborate using SharePoint, OneDrive, and Microsoft Teams. With [Office 365 Advanced Threat Protection](office-365-atp.md) (ATP), your organization can collaborate in a safer manner. ATP helps detect and block files that are identified as malicious in team sites and document libraries.</span></span>  
  
### <a name="how-it-works"></a><span data-ttu-id="199d0-108">작업 방법</span><span class="sxs-lookup"><span data-stu-id="199d0-108">How it works</span></span>

<span data-ttu-id="199d0-p102">SharePoint Online에서 파일, 비즈니스 및 Microsoft 팀의 비즈니스용 OneDrive 악성으로 확인 되었습니다, 그리고 ATP 직접 해당 파일을 잠그는 파일 저장소와 통합 됩니다. 다음 그림 라이브러리에서 감지 된 악의적인 파일의 예를 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="199d0-p102">When a file in SharePoint Online, OneDrive for Business, and Microsoft Teams has been identified as malicious, ATP directly integrates with the file stores to lock that file. The following image shows an example of a malicious file detected in a library.</span></span>
  
<span data-ttu-id="199d0-111">[![악의적인 것으로 감지 하 나와 함께 비즈니스용 OneDrive에 파일의 스크린샷](media/2bba71cc-7ad1-4799-8b9d-d56f923db3a7.png)](https://support.office.com/article/01e902ad-a903-4e0f-b093-1e1ac0c37ad2)</span><span class="sxs-lookup"><span data-stu-id="199d0-111">[![Screenshot of files in OneDrive for Business with one detected as malicious](media/2bba71cc-7ad1-4799-8b9d-d56f923db3a7.png)](https://support.office.com/article/01e902ad-a903-4e0f-b093-1e1ac0c37ad2)</span></span>
  
<span data-ttu-id="199d0-p103">차단 된 파일은 문서 라이브러리 및 웹, 모바일, 또는 데스크톱 응용 프로그램에 계속 표시 되지만 차단 된 파일 열기, 복사, 이동 하거나 수 없습니다, 공유 합니다. 사용자 수, 차단 된 파일을 삭제 되지만 합니다. 다음 사용자의 모바일 장치에서 다음과 같은 어떤 하는 예제:</span><span class="sxs-lookup"><span data-stu-id="199d0-p103">Although the blocked file is still listed in the document library and web, mobile, or desktop applications, the blocked file cannot be opened, copied, moved, or shared. People can, however, delete a blocked file. Here's an example of what that looks like on a user's mobile device:</span></span>
  
<span data-ttu-id="199d0-115">[![비즈니스용 OneDrive의 OneDrive 모바일 응용 프로그램에서 차단 된 파일을 삭제 하는 스크린샷](media/cb1c1705-fd0a-45b8-9a26-c22503011d54.png)](https://support.office.com/article/01e902ad-a903-4e0f-b093-1e1ac0c37ad2)</span><span class="sxs-lookup"><span data-stu-id="199d0-115">[![Screenshot of deleting a blocked file from OneDrive for Business from the OneDrive mobile app](media/cb1c1705-fd0a-45b8-9a26-c22503011d54.png)](https://support.office.com/article/01e902ad-a903-4e0f-b093-1e1ac0c37ad2)</span></span>
  
<span data-ttu-id="199d0-p104">Office 365를 구성 하는 방법에 따라 사용자 수도 있고 차단 된 파일을 다운로드 하는 기능을 없을 수도 있습니다. 차단 된 파일을 다운로드 하의 모습 사용자의 모바일 장치에서 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="199d0-p104">Depending on how Office 365 is configured, people might or might not have the ability to download a blocked file. Here's what downloading a blocked file looks like on a user's mobile device:</span></span>
  
<span data-ttu-id="199d0-118">[![비즈니스용 OneDrive에 차단 된 파일을 다운로드 하는 스크린샷](media/be288a82-bdd8-4371-93d8-1783db3b61bc.png)](https://support.office.com/article/01e902ad-a903-4e0f-b093-1e1ac0c37ad2)</span><span class="sxs-lookup"><span data-stu-id="199d0-118">[![Screenshot of downloading a blocked file in OneDrive for Business](media/be288a82-bdd8-4371-93d8-1783db3b61bc.png)](https://support.office.com/article/01e902ad-a903-4e0f-b093-1e1ac0c37ad2)</span></span>
  
<span data-ttu-id="199d0-119">자세한 내용은, [SharePoint, OneDrive 및 팀이 Microsoft Office 365 ATP 설정](turn-on-atp-for-spo-odb-and-teams.md)을 참조 합니다.</span><span class="sxs-lookup"><span data-stu-id="199d0-119">To learn more, see [Turn on Office 365 ATP for SharePoint, OneDrive, and Microsoft Teams](turn-on-atp-for-spo-odb-and-teams.md).</span></span>
  
### <a name="keep-the-following-points-in-mind"></a><span data-ttu-id="199d0-120">다음 사항을 염두합니다</span><span class="sxs-lookup"><span data-stu-id="199d0-120">Keep the following points in mind</span></span>

- <span data-ttu-id="199d0-p105">ATP는 회사 또는 팀이 Microsoft에 대 한 SharePoint Online, OneDrive에서 모든 단일 파일을 검색 하지 않습니다. 의도적인 것입니다. 파일에서 스마트 한 추론 방식 및 위협 신호 함께 공유 및 관람객 활동 이벤트를 사용 하 여 악의적인 파일을 식별 하는 프로세스를 통해 비동기적으로 검색 됩니다.</span><span class="sxs-lookup"><span data-stu-id="199d0-p105">ATP will not scan every single file in SharePoint Online, OneDrive for Business, or Microsoft Teams. This is by design. Files are scanned asynchronously, through a process that uses sharing and guest activity events along with smart heuristics and threat signals to identify malicious files.</span></span>

- <span data-ttu-id="199d0-p106">SharePoint 사이트에 [현대 경험](https://docs.microsoft.com/sharepoint/guide-to-sharepoint-modern-experience)을 사용 하도록 구성 되었는지 확인 합니다. 악의적인 및 차단 된 파일을 식별 되는 사용자 되었다는 현대 경험 하지만 하지 클래식 보기에서 볼 수 있습니다. ATP 보호 적용 현대 경험 나 기본 보기, 사용 여부 그러나 파일이 차단 되는 시각적 표시기는 현대 환경에만 존재 합니다.</span><span class="sxs-lookup"><span data-stu-id="199d0-p106">Make sure your SharePoint sites are configured to use the [Modern experience](https://docs.microsoft.com/sharepoint/guide-to-sharepoint-modern-experience). When a file is identified as malicious and blocked, people can see that this has occurred in the Modern experience, but not the Classic view. ATP protection applies whether the Modern experience or the Classic view is used; however, visual indicators that a file is blocked are present only in the Modern experience.</span></span>
    
- <span data-ttu-id="199d0-127">SharePoint Online에서 악의적으로 식별 되는 파일, 회사 또는 Microsoft 팀의 비즈니스용 OneDrive 위협 탐색기 ( [Office 365 위협 인텔리전스](office-365-ti.md)의 일부) 및 [Office 365 고급 위협 보호에 대 한 보고서](view-reports-for-atp.md) 에서 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="199d0-127">Files that are identified as malicious in SharePoint Online, OneDrive for Business, or Microsoft Teams will show up in [reports for Office 365 Advanced Threat Protection](view-reports-for-atp.md) and in Threat Explorer (part of [Office 365 Threat Intelligence](office-365-ti.md)).</span></span>
    
- <span data-ttu-id="199d0-p107">ATP는 조직의 전체 위협 보호 전략의 스팸 방지 및 맬웨어 방지 보호 기능으로 안전 링크와 안전한 첨부 파일을 포함 하는 일부입니다. 자세한 내용은 [Office 365의 위협 으로부터 보호](protect-against-threats.md)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="199d0-p107">ATP is part of your organization's overall threat protection strategy, which includes anti-spam and anti-malware protection, as well as Safe Links and Safe Attachments. To learn more, see [Protect against threats in Office 365](protect-against-threats.md).</span></span>
    
- <span data-ttu-id="199d0-p108">SharePoint Online 관리자가 악성으로 검색 되는 파일을 다운로드 하는 사용자의 사용 여부를 확인할 수 있습니다. 이 DisallowInfectedFileDownload 매개 변수를 사용 하 여 Set-spotenant PowerShell cmdlet을 실행 하 여 작업은 수행 ( [SharePoint, OneDrive 및 팀이 Microsoft Office 365 ATP 설정](turn-on-atp-for-spo-odb-and-teams.md)참조).</span><span class="sxs-lookup"><span data-stu-id="199d0-p108">A SharePoint Online administrator can determine whether to enable people to download files that are detected as malicious. This is done by running the Set-SPOTenant PowerShell cmdlet using a DisallowInfectedFileDownload parameter (see [Turn on Office 365 ATP for SharePoint, OneDrive, and Microsoft Teams](turn-on-atp-for-spo-odb-and-teams.md)).</span></span>
    
## <a name="quarantine-in-atp-for-sharepoint-online-onedrive-for-business-and-microsoft-teams"></a><span data-ttu-id="199d0-132">온라인 격리 SharePoint에 대 한 ATP에, 비즈니스 및 Microsoft 팀의 비즈니스용 OneDrive</span><span class="sxs-lookup"><span data-stu-id="199d0-132">Quarantine in ATP for SharePoint Online, OneDrive for Business, and Microsoft Teams</span></span>

 <span data-ttu-id="199d0-133">가능한 가장 늦은 년 5 월 2018, 보안에서 [격리](quarantine-email-messages.md) 기능에에서 시작 &amp; 준수 센터는 하기 위해 확장 된 ATP SharePoint에 대 한 온라인으로 비즈니스 및 Microsoft 팀의 비즈니스용 OneDrive 합니다.</span><span class="sxs-lookup"><span data-stu-id="199d0-133">Beginning in late May 2018, [quarantine](quarantine-email-messages.md) capabilities in the Security &amp; Compliance Center are being extended to ATP for SharePoint Online, OneDrive for Business, and Microsoft Teams.</span></span>
  
<span data-ttu-id="199d0-p109">때 SharePoint Online에서 파일, 회사 또는 Microsoft 팀의 비즈니스용 OneDrive 열거나 공유에서 파일을 차단 하는 ATP 외에도 악의적인으로 식별 된, 격리 된 항목 목록에 해당 파일이 포함 됩니다. (보안에서 &amp; 준수 센터, **위협 관리로** 이동 \> **검토** \> **격리** 하 고 **콘텐츠**에 대 한 필터입니다.)</span><span class="sxs-lookup"><span data-stu-id="199d0-p109">When a file in SharePoint Online, OneDrive for Business, or Microsoft Teams is identified as malicious, in addition to ATP blocking the file from being opened or shared, that file is included in a list of quarantined items. (In the Security &amp; Compliance Center, go to **Threat management** \> **Review** \> **Quarantine** and filter for **Content**.)</span></span> 
  
<span data-ttu-id="199d0-136">조직의 Office 365 보안 팀의 일부 이며는 데 필요한 경우 [Office 365 보안에 할당 된 사용 권한을 &amp; 준수 센터](permissions-in-the-security-and-compliance-center.md), 다운로드, 릴리스, 보고 및 ATP 하 여 악성으로 검색 되는 파일을 삭제할 수 있습니다 격리 됩니다.</span><span class="sxs-lookup"><span data-stu-id="199d0-136">If you're part of your organization's Office 365 security team and have the necessary [permissions assigned in the Office 365 Security &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md), you can download, release, report, and delete files that are detected as malicious by ATP from quarantine.</span></span>
  
- <span data-ttu-id="199d0-p110">**릴리스 및 보고** 파일을 SharePoint, OneDrive, 또는 Microsoft 팀의 ATP 블록 파일에 해당 하는 팀 사이트 또는 문서 라이브러리에서 제거합니다. 그러면 사용자가 열기, 공유 및 파일을 다운로드 하려면 수입니다. 및 파일을 **Microsoft에 보고서 보내기** 옵션을 선택 하는 경우 Microsoft에 가양성으로 보고 됩니다.</span><span class="sxs-lookup"><span data-stu-id="199d0-p110">**Releasing and reporting** a file removes the ATP block on the file in the respective team site or document library for SharePoint, OneDrive, or Microsoft Teams. Users are then able to open, share, and download the file. And, when the **Send report to Microsoft** option is selected, the file is reported as a false positive to Microsoft.</span></span> 
    
- <span data-ttu-id="199d0-p111">격리;에서 파일을 제거 하 **는 파일을 삭제** 그러나 열거나 공유 파일은 여전히 못 차단 됩니다. 파일 (SharePoint Online, 회사 또는 Microsoft 팀의 비즈니스용 OneDrive) 해당 문서 라이브러리 또는 팀 사이트에도 삭제 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="199d0-p111">**Deleting a file** removes the file from quarantine; however, the file is still blocked from being opened or shared. The file must also be deleted in its respective document library or team site (SharePoint Online, OneDrive for Business, or Microsoft Teams).</span></span> 
    
- <span data-ttu-id="199d0-142">**파일을 다운로드 하** 는 다운로드 하 고 모든 가양성에 대 한 파일을 분석할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="199d0-142">**Downloading a file** enables you to download and analyze the file for any false positives.</span></span> 
    
## <a name="next-steps"></a><span data-ttu-id="199d0-143">다음 단계</span><span class="sxs-lookup"><span data-stu-id="199d0-143">Next steps</span></span>

- [<span data-ttu-id="199d0-144">SharePoint, OneDrive 및 팀이 Microsoft Office 365 ATP 설정</span><span class="sxs-lookup"><span data-stu-id="199d0-144">Turn on Office 365 ATP for SharePoint, OneDrive, and Microsoft Teams</span></span>](turn-on-atp-for-spo-odb-and-teams.md)
    
- [<span data-ttu-id="199d0-145">SharePoint, OneDrive, 또는 팀이 Microsoft에서 감지 된 악의적인 파일에 대 한 정보 보기</span><span class="sxs-lookup"><span data-stu-id="199d0-145">View information about malicious files detected in SharePoint, OneDrive, or Microsoft Teams</span></span>](malicious-files-detected-in-spo-odb-or-teams.md)
    
## <a name="related-topics"></a><span data-ttu-id="199d0-146">관련 항목</span><span class="sxs-lookup"><span data-stu-id="199d0-146">Related topics</span></span>

[<span data-ttu-id="199d0-147">Office 365 Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="199d0-147">Office 365 Advanced Threat Protection</span></span>](office-365-atp.md)
  
[<span data-ttu-id="199d0-148">Office 365 고급 위협 보호에 대 한 보고서 보기</span><span class="sxs-lookup"><span data-stu-id="199d0-148">View the reports for Office 365 Advanced Threat Protection</span></span>](view-reports-for-atp.md)
  
[<span data-ttu-id="199d0-149">Office 365 보안에 대 한 사용 권한을 &amp; 준수 센터</span><span class="sxs-lookup"><span data-stu-id="199d0-149">Permissions in the Office 365 Security &amp; Compliance Center</span></span>](permissions-in-the-security-and-compliance-center.md)
  

