---
title: SharePoint, OneDrive 및 Microsoft Teams에 대한 Office 365 ATP
ms.author: deniseb
author: denisebmsft
manager: dansimp
audience: Admin
ms.date: 03/19/2019
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 26261670-db33-4c53-b125-af0662c34607
ms.collection:
- M365-security-compliance
description: Office 365 Advanced Threat Protection을 SharePoint Online, 비즈니스용 OneDrive 그리고 Microsoft Teams의 파일에까지 확장하여 조직의 더욱 안전한 협업을 가능하게 하십시오.
ms.openlocfilehash: 1a9fbf54b1393f250bc259ecb2e8bb9fd36f2ae0
ms.sourcegitcommit: 32ecff689ae32c59a39b7633ca0f36a304e7516e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/09/2019
ms.locfileid: "35598644"
---
# <a name="office-365-atp-for-sharepoint-onedrive-and-microsoft-teams"></a><span data-ttu-id="b097d-103">SharePoint, OneDrive 및 Microsoft Teams에 대한 Office 365 ATP</span><span class="sxs-lookup"><span data-stu-id="b097d-103">Office 365 ATP for SharePoint, OneDrive, and Microsoft Teams</span></span>

## <a name="overview-of-office-365-atp-for-sharepoint-onedrive-and-microsoft-teams"></a><span data-ttu-id="b097d-104">SharePoint, OneDrive 및 Microsoft Teams에 대한 Office 365 ATP의 개요</span><span class="sxs-lookup"><span data-stu-id="b097d-104">Overview of Office 365 ATP for SharePoint, OneDrive, and Microsoft Teams</span></span>

<span data-ttu-id="b097d-p101">사용자들은 SharePoint, OneDrive 및 Microsoft teams를 활용하여 정기적으로 파일을 공유하고 협업을 합니다. [Office 365 Advanced Threat Protection](office-365-atp.md) (ATP)를 통해 조직은 보다 안전한 방식으로 협업을 할 수 있습니다. ATP는 팀 사이트 및 문서 라이브러리에서 악성으로 식별되는 파일을 탐지하고 차단합니다.</span><span class="sxs-lookup"><span data-stu-id="b097d-p101">People regularly share files and collaborate using SharePoint, OneDrive, and Microsoft Teams. With [Office 365 Advanced Threat Protection](office-365-atp.md) (ATP), your organization can collaborate in a safer manner. ATP helps detect and block files that are identified as malicious in team sites and document libraries.</span></span>  
  
## <a name="how-it-works"></a><span data-ttu-id="b097d-108">작동 방법</span><span class="sxs-lookup"><span data-stu-id="b097d-108">How it works</span></span>

<span data-ttu-id="b097d-p102">SharePoint 온라인, 비즈니스용 OneDrive, Microsoft teams에서의 파일이 악성으로 확인되었을 시 ATP는 해당 파일을 잠그기 위해 파일의 저장소와 직접 통합합니다. 다음의 그림은 라이브러리에서 탐지된 악성 파일의 예를 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="b097d-p102">When a file in SharePoint Online, OneDrive for Business, and Microsoft Teams has been identified as malicious, ATP directly integrates with the file stores to lock that file. The following image shows an example of a malicious file detected in a library.</span></span>
  
<span data-ttu-id="b097d-111">[![악성 파일로 탐지된 한 개의 파일을 포함한 비즈니스용 OneDrive에 있는 파일](media/2bba71cc-7ad1-4799-8b9d-d56f923db3a7.png)](https://support.office.com/article/01e902ad-a903-4e0f-b093-1e1ac0c37ad2)</span><span class="sxs-lookup"><span data-stu-id="b097d-111">[![Files in OneDrive for Business with one detected as malicious](media/2bba71cc-7ad1-4799-8b9d-d56f923db3a7.png)](https://support.office.com/article/01e902ad-a903-4e0f-b093-1e1ac0c37ad2)</span></span>
  
<span data-ttu-id="b097d-p103">차단된 파일이 여전히 문서 라이브러리와 웹, 모바일 또는 데스크톱 응용 프로그램에 있을지라도 차단된 파일은 열기, 복사, 이동 혹은 공유할 수 없습니다. 하지만 사용자는 차단된 파일을 삭제할 수 있습니다. 사용자의 모바일 장치에서 보이는 예시는 다음과 같습니다:</span><span class="sxs-lookup"><span data-stu-id="b097d-p103">Although the blocked file is still listed in the document library and web, mobile, or desktop applications, the blocked file cannot be opened, copied, moved, or shared. People can, however, delete a blocked file. Here's an example of what that looks like on a user's mobile device:</span></span>
  
<span data-ttu-id="b097d-115">[![OneDrive 모바일 앱의 비즈니스용 OneDrive에서 차단된 파일 삭제](media/cb1c1705-fd0a-45b8-9a26-c22503011d54.png)](https://support.office.com/article/01e902ad-a903-4e0f-b093-1e1ac0c37ad2)</span><span class="sxs-lookup"><span data-stu-id="b097d-115">[![Deleting a blocked file from OneDrive for Business from the OneDrive mobile app](media/cb1c1705-fd0a-45b8-9a26-c22503011d54.png)](https://support.office.com/article/01e902ad-a903-4e0f-b093-1e1ac0c37ad2)</span></span>
  
<span data-ttu-id="b097d-p104">Office 365의 구성 방식에 따라 사용자는 차단된 파일을 다운로드하거나 하지 못할 수 있습니다. 사용자의 모바일 장치에서 차단된 파일을 다운로드하는 스크린샷은 다음과 같습니다:</span><span class="sxs-lookup"><span data-stu-id="b097d-p104">Depending on how Office 365 is configured, people might or might not have the ability to download a blocked file. Here's what downloading a blocked file looks like on a user's mobile device:</span></span>
  
<span data-ttu-id="b097d-118">[![비즈니스용 OneDrive에서 차단된 파일 다운로드](media/be288a82-bdd8-4371-93d8-1783db3b61bc.png)](https://support.office.com/article/01e902ad-a903-4e0f-b093-1e1ac0c37ad2)</span><span class="sxs-lookup"><span data-stu-id="b097d-118">[![Downloading a blocked file in OneDrive for Business](media/be288a82-bdd8-4371-93d8-1783db3b61bc.png)](https://support.office.com/article/01e902ad-a903-4e0f-b093-1e1ac0c37ad2)</span></span>
  
<span data-ttu-id="b097d-119">자세한 내용은 [SharePoint, OneDrive 및 Microsoft Teams에 대한 Office 365 ATP 실행](turn-on-atp-for-spo-odb-and-teams.md)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="b097d-119">To learn more, see [Turn on Office 365 ATP for SharePoint, OneDrive, and Microsoft Teams](turn-on-atp-for-spo-odb-and-teams.md).</span></span>
  
## <a name="keep-these-points-in-mind"></a><span data-ttu-id="b097d-120">다음의 사항을 염두에 둡니다.</span><span class="sxs-lookup"><span data-stu-id="b097d-120">Keep these points in mind</span></span>

- <span data-ttu-id="b097d-p105">ATP는 그 설계 상 SharePoint 온라인, 비즈니스용 OneDrive 혹은 Microsoft Teams의 모든 파일을 스캔하지 않습니다. 악성 파일을 식별하기 위해 파일들은 스마트 휴리스틱과 위협 신호와 함께 공유 및 게스트 활동 이벤트를 사용하는 프로세스를 통해 비동기적으로 스캔됩니다.</span><span class="sxs-lookup"><span data-stu-id="b097d-p105">ATP will not scan every single file in SharePoint Online, OneDrive for Business, or Microsoft Teams. This is by design. Files are scanned asynchronously, through a process that uses sharing and guest activity events along with smart heuristics and threat signals to identify malicious files.</span></span>

- <span data-ttu-id="b097d-p106">SharePoint 사이트가 [모던 경험](https://docs.microsoft.com/sharepoint/guide-to-sharepoint-modern-experience)을 사용하도록 구성되었는지 확인합니다. 파일이 악성으로 확인되고 차단되었을 때 사용자는 이러한 발생을 모던 경험을 통해 확인할 수 있지만 클래식 보기에서는 확인할 수 없습니다. ATP 보호 기능은 모던 환경 또는 클래식 보기의 사용 여부에관계없이 적용됩니다; 그러나 파일이 차단되었다는 시각적 표시는 모던 경험을 통해서만 제공됩니다.</span><span class="sxs-lookup"><span data-stu-id="b097d-p106">Make sure your SharePoint sites are configured to use the [Modern experience](https://docs.microsoft.com/sharepoint/guide-to-sharepoint-modern-experience). When a file is identified as malicious and blocked, people can see that this has occurred in the Modern experience, but not the Classic view. ATP protection applies whether the Modern experience or the Classic view is used; however, visual indicators that a file is blocked are present only in the Modern experience.</span></span>
    
- <span data-ttu-id="b097d-127">SharePoint Online, 비즈니스용 OneDrive 또는 Microsoft 팀에서 악성으로 식별 되는 파일은 [Office 365 Advanced Threat Protection](view-reports-for-atp.md) 및 [Explorer (및 실시간 검색)](threat-explorer.md)에 대 한 보고서에 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b097d-127">Files that are identified as malicious in SharePoint Online, OneDrive for Business, or Microsoft Teams will show up in [reports for Office 365 Advanced Threat Protection](view-reports-for-atp.md) and in [Explorer (and real-time detections)](threat-explorer.md).</span></span>
    
- <span data-ttu-id="b097d-p107">ATP는 조직의 전반적인 위협 보호 전략의 일부로서 스팸 방지 및 악성코드 방지 보호 수단 외에 안전한 링크 및 안전한 첨부 파일 기능을 포함합니다. 자세한 내용은 [Office 365의 위협으로부터 보호](protect-against-threats.md)를 참조합니다.</span><span class="sxs-lookup"><span data-stu-id="b097d-p107">ATP is part of your organization's overall threat protection strategy, which includes anti-spam and anti-malware protection, as well as Safe Links and Safe Attachments. To learn more, see [Protect against threats in Office 365](protect-against-threats.md).</span></span>
    
- <span data-ttu-id="b097d-p108">SharePoint 온라인 관리자는 악성으로 탐지된 파일을 사용자들이 다운로드할 수 있도록 할지 여부를 결정할 수 있습니다. 이는  DisallowInfectedFileDownload 매개 변수를 사용하여 Set-SPOTenant PowerShell cmdlet을 실행하여 결정합니다 ([SharePoint, OneDrive 및 Microsoft Teams에 대한 Office 365 ATP 실행](turn-on-atp-for-spo-odb-and-teams.md)참조).</span><span class="sxs-lookup"><span data-stu-id="b097d-p108">A SharePoint Online administrator can determine whether to enable people to download files that are detected as malicious. This is done by running the Set-SPOTenant PowerShell cmdlet using a DisallowInfectedFileDownload parameter (see [Turn on Office 365 ATP for SharePoint, OneDrive, and Microsoft Teams](turn-on-atp-for-spo-odb-and-teams.md)).</span></span>
    
## <a name="quarantine-in-atp-for-sharepoint-online-onedrive-for-business-and-microsoft-teams"></a><span data-ttu-id="b097d-132">SharePoint 온라인, 비즈니스용 OneDrive 및 Microsoft Teams를 위한 ATP를 통한 검역</span><span class="sxs-lookup"><span data-stu-id="b097d-132">Quarantine in ATP for SharePoint Online, OneDrive for Business, and Microsoft Teams</span></span>

 <span data-ttu-id="b097d-133">2018년 5월 말부터 보안&amp; 준수 센터의 [검역](quarantine-email-messages.md) 기능이 SharePoint Online, 비즈니스용 OneDrive 및 Microsoft Teams를 위해 ATP로 확장됩니다.</span><span class="sxs-lookup"><span data-stu-id="b097d-133">Beginning in late May 2018, [quarantine](quarantine-email-messages.md) capabilities in the Security &amp; Compliance Center are being extended to ATP for SharePoint Online, OneDrive for Business, and Microsoft Teams.</span></span>
  
<span data-ttu-id="b097d-p109">SharePoint Online, 비즈니스용 OneDrive 및 Microsoft Teams의 파일이 악성으로 확인될 시 ATP가 파일을 열거나 공유하지 못하도록 차단하는 조치 외에도 해당 파일은 검역 항목 목록에 포함이 됩니다. (보안&amp; 준수 센터에서 **위협 관리** \> **검토** \> **검역** 및 **콘텐츠** 필터링을 선택합니다.)</span><span class="sxs-lookup"><span data-stu-id="b097d-p109">When a file in SharePoint Online, OneDrive for Business, or Microsoft Teams is identified as malicious, in addition to ATP blocking the file from being opened or shared, that file is included in a list of quarantined items. (In the Security &amp; Compliance Center, go to **Threat management** \> **Review** \> **Quarantine** and filter for **Content**.)</span></span> 
  
<span data-ttu-id="b097d-136">귀하가 조직의 Office 365 보안팀의 구성원이고 필요한 [Office 365 보안 &amp;준수 센터](permissions-in-the-security-and-compliance-center.md)에 할당되는 사용 권한을 보유하고 있는 경우, 검역소에서 ATP를 통해 악성으로 확인된 파일을 다운로드, 공개, 보고 및  삭제할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b097d-136">If you're part of your organization's Office 365 security team and have the necessary [permissions assigned in the Office 365 Security &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md), you can download, release, report, and delete files that are detected as malicious by ATP from quarantine.</span></span>
  
- <span data-ttu-id="b097d-p110">파일을 **출시 및 보고** 시 해당 팀 사이트 또는 SharePoint, OneDrive의 문서 라이브러리 또는 Microsoft Teams의 파일에 있는 ATP 블록이 제거됩니다. 이후 사용자는 해당 파일의 열기, 공유 및 다운로드를 할 수 있게 됩니다. **Microsoft에 보고서 보내기** 옵션을 선택 시 해당 파일은 Microsoft에 가양성으로 보고됩니다.</span><span class="sxs-lookup"><span data-stu-id="b097d-p110">**Releasing and reporting** a file removes the ATP block on the file in the respective team site or document library for SharePoint, OneDrive, or Microsoft Teams. Users are then able to open, share, and download the file. And, when the **Send report to Microsoft** option is selected, the file is reported as a false positive to Microsoft.</span></span> 
    
- <span data-ttu-id="b097d-p111">**파일을 삭제** 시 파일을 검역소에서 제거하지만 파일은 여전히 열거나 공유할 수 없도록 차단됩니다. 파일은 또한 해당 문서 라이브러리 또는 팀 사이트 (SharePoint 온라인, 비즈니스용 OneDrive 또는 Microsoft Teams)에서 삭제되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b097d-p111">**Deleting a file** removes the file from quarantine; however, the file is still blocked from being opened or shared. The file must also be deleted in its respective document library or team site (SharePoint Online, OneDrive for Business, or Microsoft Teams).</span></span> 
    
- <span data-ttu-id="b097d-142">**파일을 다운로드** 시 파일을 다운로드하고 모든 가양성에 대해 분석할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b097d-142">**Downloading a file** enables you to download and analyze the file for any false positives.</span></span> 
    
## <a name="next-steps"></a><span data-ttu-id="b097d-143">다음 단계</span><span class="sxs-lookup"><span data-stu-id="b097d-143">Next steps</span></span>

1. [<span data-ttu-id="b097d-144">SharePoint, OneDrive 및 Microsoft Teams에 대한 Office 365 ATP 실행</span><span class="sxs-lookup"><span data-stu-id="b097d-144">Turn on Office 365 ATP for SharePoint, OneDrive, and Microsoft Teams</span></span>](turn-on-atp-for-spo-odb-and-teams.md)
    
2. [<span data-ttu-id="b097d-145">SharePoint, OneDrive 또는 Microsoft Teams에서 감지한 악성 파일에 대한 정보 보기</span><span class="sxs-lookup"><span data-stu-id="b097d-145">View information about malicious files detected in SharePoint, OneDrive, or Microsoft Teams</span></span>](malicious-files-detected-in-spo-odb-or-teams.md)
    
