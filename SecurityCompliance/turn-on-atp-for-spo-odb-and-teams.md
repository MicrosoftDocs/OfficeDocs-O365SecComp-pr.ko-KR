---
title: SharePoint, OneDrive 및 Microsoft Teams에 대한 Office 365 ATP 실행
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.audience: ITPro
ms.topic: article
ms.date: 02/06/2019
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 07e76024-0c80-40dc-8c48-1dd0d0f863cb
description: SharePoint, OneDrive 및 검색 된 파일에 대 한 알림을 설정 하는 방법을 포함 하 여 팀에 대 한 ATP를 설정 하는 방법에 알아봅니다.
ms.openlocfilehash: 9745d45428035cc52346d19aa42e5e134123d016
ms.sourcegitcommit: d6a28c4f6db6a676ca960173e8ff8f17d4aa1c4b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/06/2019
ms.locfileid: "29755299"
---
# <a name="turn-on-office-365-atp-for-sharepoint-onedrive-and-microsoft-teams"></a><span data-ttu-id="d8b3e-103">SharePoint, OneDrive 및 Microsoft Teams에 대한 Office 365 ATP 실행</span><span class="sxs-lookup"><span data-stu-id="d8b3e-103">Turn on Office 365 ATP for SharePoint, OneDrive, and Microsoft Teams</span></span>

<span data-ttu-id="d8b3e-p101">[SharePoint, OneDrive 및 팀이 Microsoft office 365 ATP](atp-for-spo-odb-and-teams.md) 실수로 악의적인 파일 공유에서 조직을 보호 합니다. 악의적인 파일 감지 되 면 해당 파일 열기, 복사, 이동 또는 조직의 보안 팀에 의해 추가 조치가 때까지 공유할 수 있는 아무도 있도록 차단 됩니다. SharePoint에 대 한 ATP를 설정 하는이 문서를 읽기, OneDrive 및 팀 검색 된 파일에 대 한 알림을 받으려면 경고를 설정 하 고에서는 다음 단계를 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="d8b3e-p101">[Office 365 ATP for SharePoint, OneDrive, and Microsoft Teams](atp-for-spo-odb-and-teams.md) protects your organization from inadvertently sharing malicious files. When a malicious file is detected, that file is blocked so that no one can open, copy, move, or share it until further actions are taken by the organization's security team. Read this article to turn on ATP for SharePoint, OneDrive, and Teams, set up alerts to be notified about detected files, and take your next steps.</span></span> 
  
<span data-ttu-id="d8b3e-107">ATP 정책, 정의 (또는 편집)를 할당 되어 있어야 다음 표에 설명 된 역할 중 하나:</span><span class="sxs-lookup"><span data-stu-id="d8b3e-107">To define (or edit) ATP policies, you must be assigned one of the roles described in the following table:</span></span>

|<span data-ttu-id="d8b3e-108">역할</span><span class="sxs-lookup"><span data-stu-id="d8b3e-108">Role</span></span>  |<span data-ttu-id="d8b3e-109">Where/방법 할당</span><span class="sxs-lookup"><span data-stu-id="d8b3e-109">Where/how assigned</span></span>  |
|---------|---------|
|<span data-ttu-id="d8b3e-110">Office 365 전역 관리자</span><span class="sxs-lookup"><span data-stu-id="d8b3e-110">Office 365 Global Administrator</span></span> |<span data-ttu-id="d8b3e-p102">Office 365를 구매 하 여를 로그인 하는 사람 이름은 기본적으로 전역 admin입니다. (자세한 내용은 [Office 365에 대 한 관리자 역할](https://docs.microsoft.com/office365/admin/add-users/about-admin-roles) 참조 하십시오.)</span><span class="sxs-lookup"><span data-stu-id="d8b3e-p102">The person who signs up to buy Office 365 is a global admin by default. (See [About Office 365 admin roles](https://docs.microsoft.com/office365/admin/add-users/about-admin-roles) to learn more.)</span></span>         |
|<span data-ttu-id="d8b3e-113">보안 관리자</span><span class="sxs-lookup"><span data-stu-id="d8b3e-113">Security Administrator</span></span> |<span data-ttu-id="d8b3e-114">Azure Active Directory 관리 센터 ([https://aad.portal.azure.com](https://aad.portal.azure.com))</span><span class="sxs-lookup"><span data-stu-id="d8b3e-114">Azure Active Directory admin center ([https://aad.portal.azure.com](https://aad.portal.azure.com))</span></span>|
|<span data-ttu-id="d8b3e-115">Exchange Online 조직 관리</span><span class="sxs-lookup"><span data-stu-id="d8b3e-115">Exchange Online Organization Management</span></span> |<span data-ttu-id="d8b3e-116">Exchange 관리 센터 ([https://outlook.office365.com/ecp](https://outlook.office365.com/ecp))</span><span class="sxs-lookup"><span data-stu-id="d8b3e-116">Exchange admin center ([https://outlook.office365.com/ecp](https://outlook.office365.com/ecp))</span></span> <br><span data-ttu-id="d8b3e-117">또는</span><span class="sxs-lookup"><span data-stu-id="d8b3e-117">or</span></span> <br>  <span data-ttu-id="d8b3e-118">PowerShell cmdlet (참조 [Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/exchange-online-powershell?view=exchange-ps))</span><span class="sxs-lookup"><span data-stu-id="d8b3e-118">PowerShell cmdlets (See [Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/exchange-online-powershell?view=exchange-ps))</span></span> |
  
## <a name="turn-on-atp-for-sharepoint-onedrive-and-microsoft-teams"></a><span data-ttu-id="d8b3e-119">SharePoint, OneDrive 및 Microsoft Teams에 대한 ATP 켜기</span><span class="sxs-lookup"><span data-stu-id="d8b3e-119">Turn on ATP for SharePoint, OneDrive, and Microsoft Teams</span></span>

<span data-ttu-id="d8b3e-p103">**이 절차를 시작 하기 전에 Office 365 환경에 대 한 감사 로깅이 이미 설정 되어있는지 확인**하십시오. 이 Exchange Online 할당 된 감사 로그 역할을 가진 사용자가 일반적으로 수행 됩니다. 자세한 내용은 [Office 365 설정 또는 해제 로그 검색 감사](turn-audit-log-search-on-or-off.md)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="d8b3e-p103">**Before you begin this procedure, make sure that audit logging is already turned on for your Office 365 environment**. This is typically done by someone who has the Audit Logs role assigned in Exchange Online. For more information, see [Turn Office 365 audit log search on or off](turn-audit-log-search-on-or-off.md).</span></span>
  
1. <span data-ttu-id="d8b3e-123">이동 [https://protection.office.com](https://protection.office.com)와 작업이 나 교육용 계정 사용 하 여 로그인 합니다.</span><span class="sxs-lookup"><span data-stu-id="d8b3e-123">Go to [https://protection.office.com](https://protection.office.com), and sign in with your work or school account.</span></span>
    
2. <span data-ttu-id="d8b3e-124">Office 365 보안에서 &amp; 준수 센터 왼쪽된 탐색 창의 **위협 관리** **정책** 을 선택 \> **안전한 첨부 파일**입니다.</span><span class="sxs-lookup"><span data-stu-id="d8b3e-124">In the Office 365 Security &amp; Compliance Center, in the left navigation pane, under **Threat management**, choose **Policy** \> **Safe Attachments**.</span></span> <br/><span data-ttu-id="d8b3e-125">![보안에서 &amp; 준수 센터 위협 관리를 선택 \> 정책](media/08849c91-f043-4cd1-a55e-d440c86442f2.png)</span><span class="sxs-lookup"><span data-stu-id="d8b3e-125">![In the Security &amp; Compliance Center, choose Threat management \> Policy](media/08849c91-f043-4cd1-a55e-d440c86442f2.png)</span></span>
  
3. <span data-ttu-id="d8b3e-126">**SharePoint, OneDrive 및 Microsoft 팀의 ATP 설정**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="d8b3e-126">Select **Turn on ATP for SharePoint, OneDrive, and Microsoft Teams**.</span></span><br/><span data-ttu-id="d8b3e-127">![온라인으로 비즈니스용 OneDrive, Microsoft 팀의 SharePoint에 대 한 고급 위협 보호 설정](media/48cfaace-59cc-4e60-bf86-05ff6b99bdbf.png)</span><span class="sxs-lookup"><span data-stu-id="d8b3e-127">![Turn on Advanced Threat Protection for SharePoint Online, OneDrive for Business, and Microsoft Teams](media/48cfaace-59cc-4e60-bf86-05ff6b99bdbf.png)</span></span>
  
4. <span data-ttu-id="d8b3e-128">**저장**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="d8b3e-128">Click **Save**.</span></span>
    
5. <span data-ttu-id="d8b3e-129">검토 (하 고 적절 하 게 편집) 조직의 [안전한 첨부 파일 정책](set-up-atp-safe-attachments-policies.md) 및 [안전 링크 정책](set-up-atp-safe-links-policies.md).</span><span class="sxs-lookup"><span data-stu-id="d8b3e-129">Review (and, as appropriate, edit) your organization's [Safe Attachments policies](set-up-atp-safe-attachments-policies.md) and [Safe Links policies](set-up-atp-safe-links-policies.md).</span></span>
    
6. <span data-ttu-id="d8b3e-130">(권장) 전역 관리자 또는 SharePoint Online 관리자가 *true*로 설정 하는 **DisallowInfectedFileDownload** 매개 변수와 함께 **[Set-spotenant](https://docs.microsoft.com/powershell/module/sharepoint-online/Set-SPOTenant?view=sharepoint-ps)** cmdlet을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="d8b3e-130">(Recommended) As a global administrator or a SharePoint Online administrator, run the **[Set-SPOTenant](https://docs.microsoft.com/powershell/module/sharepoint-online/Set-SPOTenant?view=sharepoint-ps)** cmdlet with the **DisallowInfectedFileDownload** parameter set to  *true*.</span></span> <br/>
      - <span data-ttu-id="d8b3e-p104">파일을 검색 매개 변수를 *true로* 블록 (삭제)을 제외한 모든 작업에 대 한 설정 합니다. 사용자 수는 없습니다 열, 이동, 복사 또는 검색 된 파일을 공유 합니다.</span><span class="sxs-lookup"><span data-stu-id="d8b3e-p104">Setting the parameter to *true* blocks all actions (except Delete) for detected files. People cannot open, move, copy, or share detected files.</span></span>
      - <span data-ttu-id="d8b3e-p105">삭제 및 다운로드를 제외 하 고 모든 작업을 차단 매개 변수를 *false로* 설정 합니다. 사용자는 위험을 수용 하 고 발견 된 파일을 다운로드 하도록 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d8b3e-p105">Setting the parameter to *false* blocks all actions except Delete and Download. People can choose to accept the risk and download a detected file.</span></span>  
   
7. <span data-ttu-id="d8b3e-135">모든 Office 365 데이터 센터에 분산 하 여 변경 내용 최대 30 분까지를 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="d8b3e-135">Allow up to 30 minutes for your changes to spread to all Office 365 datacenters.</span></span>
    
8. <span data-ttu-id="d8b3e-136">(권장) 검색 된 파일에 대 한 알림을 설정으로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="d8b3e-136">(Recommended) Proceed to set up alerts for detected files.</span></span>
    
<span data-ttu-id="d8b3e-137">PowerShell을 사용 하 여 Office 365를 사용 하는 방법에 대 한 자세한 내용은, [PowerShell 사용 하 여 Office 365 관리](https://docs.microsoft.com/office365/enterprise/powershell/manage-office-365-with-office-365-powershell)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="d8b3e-137">To learn more about using PowerShell with Office 365, see [Manage Office 365 with PowerShell](https://docs.microsoft.com/office365/enterprise/powershell/manage-office-365-with-office-365-powershell).</span></span> 

<span data-ttu-id="d8b3e-138">자세한 사용자 환경에 대 한 악의적인으로 파일에서 발견 하는 경우, [악의적인 파일을 SharePoint Online, OneDrive, 또는 팀이 Microsoft에서 발견 되 면 수행할 작업을](https://support.office.com/article/01e902ad-a903-4e0f-b093-1e1ac0c37ad2)참조 합니다.</span><span class="sxs-lookup"><span data-stu-id="d8b3e-138">To learn more about the user experience when a file has been detected as malicious, see [What to do when a malicious file is found in SharePoint Online, OneDrive, or Microsoft Teams](https://support.office.com/article/01e902ad-a903-4e0f-b093-1e1ac0c37ad2).</span></span> 
  
## <a name="set-up-alerts-for-detected-files"></a><span data-ttu-id="d8b3e-139">검색 된 파일에 대 한 알림 설정</span><span class="sxs-lookup"><span data-stu-id="d8b3e-139">Set up alerts for detected files</span></span>

<span data-ttu-id="d8b3e-140">회사 또는 팀이 Microsoft에 대 한 SharePoint Online, OneDrive에서 파일을 악의적으로 식별 된 때 알림을 받으려면, 알림을 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d8b3e-140">To receive notification when a file in SharePoint Online, OneDrive for Business, or Microsoft Teams has been identified as malicious, you can set up an alert.</span></span>
  
1. <span data-ttu-id="d8b3e-141">[Office 365 보안 &amp; 준수 센터](https://protection.office.com), **알림** 을 선택 \> **관리 경고**합니다.</span><span class="sxs-lookup"><span data-stu-id="d8b3e-141">In the [Office 365 Security &amp; Compliance Center](https://protection.office.com), choose **Alerts** \> **Manage alerts**.</span></span>
    
2. <span data-ttu-id="d8b3e-142">**새 경고 정책**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="d8b3e-142">Choose **New alert policy**.</span></span>
    
3. <span data-ttu-id="d8b3e-p106">경고에 대 한 이름을 지정 합니다. 예, 라이브러리의 악의적인 파일을 입력할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d8b3e-p106">Specify a name for the alert. For example, you could type Malicious Files in Libraries.</span></span>
    
4. <span data-ttu-id="d8b3e-p107">경고에 대 한 설명을 입력 합니다. 예, SharePoint Online, OneDrive, 또는 Microsoft 팀의 악의적인 파일을 감지 되 면 관리자에 게 알리는 입력할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d8b3e-p107">Type a description for the alert. For example, you could type Notifies admins when malicious files are detected in SharePoint Online, OneDrive, or Microsoft Teams.</span></span>
    
5. <span data-ttu-id="d8b3e-147">**... 때이 경고 보내기** 섹션에서 다음을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="d8b3e-147">In the **Send this alert when...** section, do the following:</span></span> 
    
    <span data-ttu-id="d8b3e-p108">a. **작업** 목록에서 **파일에 감지 맬웨어**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="d8b3e-p108">a. In the **Activities** list, choose **Detected malware in file**.</span></span>
    
    <span data-ttu-id="d8b3e-p109">b. **사용자** 필드를 비워 둡니다.</span><span class="sxs-lookup"><span data-stu-id="d8b3e-p109">b. Leave the **Users** field empty.</span></span> 
    
6. <span data-ttu-id="d8b3e-152">**이 경고를 보내기...** 섹션에서 하나 이상의 전역 관리자, 보안 관리자 또는 악의적인 파일을 감지 하는 경우 알림을 받을 보안 독자를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="d8b3e-152">In the **Send this alert to...** section, select one or more global administrators, security administrators, or security readers who should receive notification when a malicious file is detected.</span></span> 
    
7. <span data-ttu-id="d8b3e-153">**저장**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="d8b3e-153">Click **Save**.</span></span>
    
<span data-ttu-id="d8b3e-154">경고에 대 한 자세한 내용은 참조 하십시오. [Office 365 보안에서 활동 알림을 만들 &amp; 준수 센터](create-activity-alerts.md)합니다.</span><span class="sxs-lookup"><span data-stu-id="d8b3e-154">To learn more about alerts, see [Create activity alerts in the Office 365 Security &amp; Compliance Center](create-activity-alerts.md).</span></span> 
  
## <a name="next-steps"></a><span data-ttu-id="d8b3e-155">다음 단계</span><span class="sxs-lookup"><span data-stu-id="d8b3e-155">Next steps</span></span>

1. [<span data-ttu-id="d8b3e-156">SharePoint, OneDrive 또는 Microsoft Teams에서 감지한 악성 파일에 대한 정보 보기</span><span class="sxs-lookup"><span data-stu-id="d8b3e-156">View information about malicious files detected in SharePoint, OneDrive, or Microsoft Teams</span></span>](malicious-files-detected-in-spo-odb-or-teams.md)
    
2. [<span data-ttu-id="d8b3e-157">Office 365에서 관리자 권한으로 격리 된 메시지와 파일을 관리 합니다.</span><span class="sxs-lookup"><span data-stu-id="d8b3e-157">Manage quarantined messages and files as an administrator in Office 365</span></span>](manage-quarantined-messages-and-files.md)
    

  

