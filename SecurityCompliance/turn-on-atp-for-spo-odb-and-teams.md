---
title: SharePoint, OneDrive 및 Microsoft Teams에 대한 Office 365 ATP 실행
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.audience: ITPro
ms.topic: article
ms.date: 02/06/2019
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 07e76024-0c80-40dc-8c48-1dd0d0f863cb
ms.collection: M365-security-compliance
description: 검색 된 파일에 대 한 알림을 설정 하는 방법을 포함 하 여 SharePoint, OneDrive 및 팀에 대 한 ATP를 설정 하는 방법을 알아봅니다.
ms.openlocfilehash: 88eae37b0da3df75807436d66a5c80e0c40f82d8
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30220398"
---
# <a name="turn-on-office-365-atp-for-sharepoint-onedrive-and-microsoft-teams"></a><span data-ttu-id="33610-103">SharePoint, OneDrive 및 Microsoft Teams에 대한 Office 365 ATP 실행</span><span class="sxs-lookup"><span data-stu-id="33610-103">Turn on Office 365 ATP for SharePoint, OneDrive, and Microsoft Teams</span></span>

<span data-ttu-id="33610-p101">[Office 365 ATP for SharePoint, OneDrive 및 Microsoft 팀은](atp-for-spo-odb-and-teams.md) 악의적인 파일을 실수로 공유 하지 않도록 조직을 보호 합니다. 악성 파일이 검색 되 면 해당 파일이 차단 되므로 조직의 보안 팀이 추가 작업을 수행할 때까지 아무도 해당 파일을 열거나 복사 하거나 이동 하거나 공유할 수 없습니다. 이 문서를 읽으면 SharePoint, OneDrive 및 팀에 대 한 ATP를 켜고, 검색 된 파일에 대 한 알림을 받을 알림을 설정 하 고, 다음 단계를 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="33610-p101">[Office 365 ATP for SharePoint, OneDrive, and Microsoft Teams](atp-for-spo-odb-and-teams.md) protects your organization from inadvertently sharing malicious files. When a malicious file is detected, that file is blocked so that no one can open, copy, move, or share it until further actions are taken by the organization's security team. Read this article to turn on ATP for SharePoint, OneDrive, and Teams, set up alerts to be notified about detected files, and take your next steps.</span></span> 
  
<span data-ttu-id="33610-p102">ATP 정책을 정의 하거나 편집 하려면 적절 한 역할이 할당 되어 있어야 합니다. 다음 표에서는 몇 가지 예를 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="33610-p102">To define (or edit) ATP policies, you must be assigned an appropriate role. Some examples are described in the following table:</span></span>

|<span data-ttu-id="33610-109">역할</span><span class="sxs-lookup"><span data-stu-id="33610-109">Role</span></span>  |<span data-ttu-id="33610-110">할당 된 위치/방법</span><span class="sxs-lookup"><span data-stu-id="33610-110">Where/how assigned</span></span>  |
|---------|---------|
|<span data-ttu-id="33610-111">Office 365 전역 관리자</span><span class="sxs-lookup"><span data-stu-id="33610-111">Office 365 Global Administrator</span></span> |<span data-ttu-id="33610-p103">Office 365을 구매 하기 위해 등록 하는 사람은 기본적으로 전역 관리자입니다. 자세한 내용은 [Office 365 관리자 역할 정보](https://docs.microsoft.com/office365/admin/add-users/about-admin-roles) 를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="33610-p103">The person who signs up to buy Office 365 is a global admin by default. (See [About Office 365 admin roles](https://docs.microsoft.com/office365/admin/add-users/about-admin-roles) to learn more.)</span></span>         |
|<span data-ttu-id="33610-114">보안 관리자</span><span class="sxs-lookup"><span data-stu-id="33610-114">Security Administrator</span></span> |<span data-ttu-id="33610-115">Azure Active Directory 관리 센터 ([https://aad.portal.azure.com](https://aad.portal.azure.com))</span><span class="sxs-lookup"><span data-stu-id="33610-115">Azure Active Directory admin center ([https://aad.portal.azure.com](https://aad.portal.azure.com))</span></span>|
|<span data-ttu-id="33610-116">Exchange Online 조직 관리</span><span class="sxs-lookup"><span data-stu-id="33610-116">Exchange Online Organization Management</span></span> |<span data-ttu-id="33610-117">Exchange 관리 센터 ([https://outlook.office365.com/ecp](https://outlook.office365.com/ecp))</span><span class="sxs-lookup"><span data-stu-id="33610-117">Exchange admin center ([https://outlook.office365.com/ecp](https://outlook.office365.com/ecp))</span></span> <br><span data-ttu-id="33610-118">또는</span><span class="sxs-lookup"><span data-stu-id="33610-118">or</span></span> <br>  <span data-ttu-id="33610-119">PowerShell cmdlet ( [Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/exchange-online-powershell?view=exchange-ps)참조)</span><span class="sxs-lookup"><span data-stu-id="33610-119">PowerShell cmdlets (See [Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/exchange-online-powershell?view=exchange-ps))</span></span> |
  
## <a name="turn-on-atp-for-sharepoint-onedrive-and-microsoft-teams"></a><span data-ttu-id="33610-120">SharePoint, OneDrive 및 Microsoft Teams에 대한 ATP 켜기</span><span class="sxs-lookup"><span data-stu-id="33610-120">Turn on ATP for SharePoint, OneDrive, and Microsoft Teams</span></span>

<span data-ttu-id="33610-p104">**이 절차를 시작 하기 전에 Office 365 환경에 대해 감사 로깅이 이미 설정 되어 있는지 확인**합니다. 이 작업은 일반적으로 Exchange Online에서 감사 로그 역할이 할당 된 사용자가 수행 합니다. 자세한 내용은 [Turn Office 365 감사 로그 검색 켜기 또는 끄기를](turn-audit-log-search-on-or-off.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="33610-p104">**Before you begin this procedure, make sure that audit logging is already turned on for your Office 365 environment**. This is typically done by someone who has the Audit Logs role assigned in Exchange Online. For more information, see [Turn Office 365 audit log search on or off](turn-audit-log-search-on-or-off.md).</span></span>
  
1. <span data-ttu-id="33610-124">[https://protection.office.com](https://protection.office.com)으로 이동 하 여 회사 또는 학교 계정으로 로그인 합니다.</span><span class="sxs-lookup"><span data-stu-id="33610-124">Go to [https://protection.office.com](https://protection.office.com), and sign in with your work or school account.</span></span>
    
2. <span data-ttu-id="33610-125">Office 365 보안 &amp; 및 준수 센터의 왼쪽 탐색 창에 있는 **위협 관리**에서 **정책** \> **안전한 첨부 파일**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="33610-125">In the Office 365 Security &amp; Compliance Center, in the left navigation pane, under **Threat management**, choose **Policy** \> **Safe Attachments**.</span></span> <br/><span data-ttu-id="33610-126">![보안 &amp; 및 준수 센터에서 위협 관리 \> 정책을 선택 합니다.](media/08849c91-f043-4cd1-a55e-d440c86442f2.png)</span><span class="sxs-lookup"><span data-stu-id="33610-126">![In the Security &amp; Compliance Center, choose Threat management \> Policy](media/08849c91-f043-4cd1-a55e-d440c86442f2.png)</span></span>
  
3. <span data-ttu-id="33610-127">**SharePoint, OneDrive 및 Microsoft 팀에 대해 ATP 사용**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="33610-127">Select **Turn on ATP for SharePoint, OneDrive, and Microsoft Teams**.</span></span><br/><span data-ttu-id="33610-128">![SharePoint Online, 비즈니스용 OneDrive 및 Microsoft 팀에 대 한 Advanced Threat Protection 설정](media/48cfaace-59cc-4e60-bf86-05ff6b99bdbf.png)</span><span class="sxs-lookup"><span data-stu-id="33610-128">![Turn on Advanced Threat Protection for SharePoint Online, OneDrive for Business, and Microsoft Teams](media/48cfaace-59cc-4e60-bf86-05ff6b99bdbf.png)</span></span>
  
4. <span data-ttu-id="33610-129">**저장**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="33610-129">Click **Save**.</span></span>
    
5. <span data-ttu-id="33610-130">조직의 [안전한 첨부 파일 정책](set-up-atp-safe-attachments-policies.md) 및 [안전한 링크 정책을](set-up-atp-safe-links-policies.md)검토 하 고 적절 하 게 편집 합니다.</span><span class="sxs-lookup"><span data-stu-id="33610-130">Review (and, as appropriate, edit) your organization's [Safe Attachments policies](set-up-atp-safe-attachments-policies.md) and [Safe Links policies](set-up-atp-safe-links-policies.md).</span></span>
    
6. <span data-ttu-id="33610-131">는 전역 관리자 또는 SharePoint Online 관리자는 **DisallowInfectedFileDownload** 매개 변수를 *true*로 설정 하 여 **[set-spotenant](https://docs.microsoft.com/powershell/module/sharepoint-online/Set-SPOTenant?view=sharepoint-ps)** cmdlet을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="33610-131">(Recommended) As a global administrator or a SharePoint Online administrator, run the **[Set-SPOTenant](https://docs.microsoft.com/powershell/module/sharepoint-online/Set-SPOTenant?view=sharepoint-ps)** cmdlet with the **DisallowInfectedFileDownload** parameter set to  *true*.</span></span> <br/>
      - <span data-ttu-id="33610-p105">이 매개 변수를 *true* 로 설정 하면 검색 된 파일에 대 한 모든 작업 (삭제 제외)이 차단 됩니다. 사용자가 검색 된 파일을 열거나, 이동 하거나, 복사 하거나, 공유할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="33610-p105">Setting the parameter to *true* blocks all actions (except Delete) for detected files. People cannot open, move, copy, or share detected files.</span></span>
      - <span data-ttu-id="33610-p106">이 매개 변수를 *false* 로 설정 하면 삭제 및 다운로드를 제외한 모든 작업이 차단 됩니다. 사용자는 위험을 수락 하 고 검색 된 파일을 다운로드할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="33610-p106">Setting the parameter to *false* blocks all actions except Delete and Download. People can choose to accept the risk and download a detected file.</span></span>  
   
7. <span data-ttu-id="33610-136">변경 내용이 모든 Office 365 데이터 센터에 전파 되는 데 최대 30 분 정도 걸릴 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="33610-136">Allow up to 30 minutes for your changes to spread to all Office 365 datacenters.</span></span>
    
8. <span data-ttu-id="33610-137">는 검색 된 파일에 대 한 알림 설정으로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="33610-137">(Recommended) Proceed to set up alerts for detected files.</span></span>
    
<span data-ttu-id="33610-138">office 365에서 powershell을 사용 하는 방법에 대 한 자세한 내용은 powershell을 사용 하 [여 office 365 관리](https://docs.microsoft.com/office365/enterprise/powershell/manage-office-365-with-office-365-powershell)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="33610-138">To learn more about using PowerShell with Office 365, see [Manage Office 365 with PowerShell](https://docs.microsoft.com/office365/enterprise/powershell/manage-office-365-with-office-365-powershell).</span></span> 

<span data-ttu-id="33610-139">파일이 악성으로 검색 되었을 때의 사용자 환경에 대 한 자세한 내용은 [SharePoint Online, OneDrive 또는 Microsoft 팀에서 악의적인 파일을 찾은 경우 수행할](https://support.office.com/article/01e902ad-a903-4e0f-b093-1e1ac0c37ad2)작업을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="33610-139">To learn more about the user experience when a file has been detected as malicious, see [What to do when a malicious file is found in SharePoint Online, OneDrive, or Microsoft Teams](https://support.office.com/article/01e902ad-a903-4e0f-b093-1e1ac0c37ad2).</span></span> 
  
## <a name="set-up-alerts-for-detected-files"></a><span data-ttu-id="33610-140">검색 된 파일에 대 한 알림 설정</span><span class="sxs-lookup"><span data-stu-id="33610-140">Set up alerts for detected files</span></span>

<span data-ttu-id="33610-141">SharePoint Online의 파일 (비즈니스용 OneDrive 또는 Microsoft 팀)이 악성으로 식별 된 경우 알림을 받으려면 알림을 설정 하면 됩니다.</span><span class="sxs-lookup"><span data-stu-id="33610-141">To receive notification when a file in SharePoint Online, OneDrive for Business, or Microsoft Teams has been identified as malicious, you can set up an alert.</span></span>
  
1. <span data-ttu-id="33610-142">[Office 365 보안 &amp; 및 준수 센터](https://protection.office.com)에서 **경고** \> **관리 알림을**선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="33610-142">In the [Office 365 Security &amp; Compliance Center](https://protection.office.com), choose **Alerts** \> **Manage alerts**.</span></span>
    
2. <span data-ttu-id="33610-143">**새 경고 정책을**선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="33610-143">Choose **New alert policy**.</span></span>
    
3. <span data-ttu-id="33610-p107">알림의 이름을 지정 합니다. 예를 들어 라이브러리에 유해한 파일을 입력할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="33610-p107">Specify a name for the alert. For example, you could type Malicious Files in Libraries.</span></span>
    
4. <span data-ttu-id="33610-p108">경고에 대 한 설명을 입력 합니다. 예를 들어 SharePoint Online, OneDrive 또는 Microsoft 팀에서 악성 파일이 검색 되 면 관리자에 게 알림 메시지를 입력할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="33610-p108">Type a description for the alert. For example, you could type Notifies admins when malicious files are detected in SharePoint Online, OneDrive, or Microsoft Teams.</span></span>
    
5. <span data-ttu-id="33610-148">**알림 보내기** 위치 섹션에서 다음을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="33610-148">In the **Send this alert when...** section, do the following:</span></span> 
    
    <span data-ttu-id="33610-p109">a. **작업** 목록에서 **검색 된 맬웨어를 파일에서**선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="33610-p109">a. In the **Activities** list, choose **Detected malware in file**.</span></span>
    
    <span data-ttu-id="33610-p110">b. **Users** 필드를 비워 둡니다.</span><span class="sxs-lookup"><span data-stu-id="33610-p110">b. Leave the **Users** field empty.</span></span> 
    
6. <span data-ttu-id="33610-153">**이 알림 보내기** ... 섹션에서 악의적인 파일이 검색 되 면 알림을 받을 전역 관리자, 보안 관리자 또는 보안 판독기를 하나 이상 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="33610-153">In the **Send this alert to...** section, select one or more global administrators, security administrators, or security readers who should receive notification when a malicious file is detected.</span></span> 
    
7. <span data-ttu-id="33610-154">**저장**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="33610-154">Click **Save**.</span></span>
    
<span data-ttu-id="33610-155">경고에 대 한 자세한 내용은 [Office 365 보안 &amp; 및 준수 센터에서 활동 경고 만들기](create-activity-alerts.md)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="33610-155">To learn more about alerts, see [Create activity alerts in the Office 365 Security &amp; Compliance Center](create-activity-alerts.md).</span></span> 
  
## <a name="next-steps"></a><span data-ttu-id="33610-156">다음 단계</span><span class="sxs-lookup"><span data-stu-id="33610-156">Next steps</span></span>

1. [<span data-ttu-id="33610-157">SharePoint, OneDrive 또는 Microsoft Teams에서 감지한 악성 파일에 대한 정보 보기</span><span class="sxs-lookup"><span data-stu-id="33610-157">View information about malicious files detected in SharePoint, OneDrive, or Microsoft Teams</span></span>](malicious-files-detected-in-spo-odb-or-teams.md)
    
2. [<span data-ttu-id="33610-158">Office 365에서 격리 된 메시지 및 파일을 관리자 권한으로 관리</span><span class="sxs-lookup"><span data-stu-id="33610-158">Manage quarantined messages and files as an administrator in Office 365</span></span>](manage-quarantined-messages-and-files.md)
    

  

