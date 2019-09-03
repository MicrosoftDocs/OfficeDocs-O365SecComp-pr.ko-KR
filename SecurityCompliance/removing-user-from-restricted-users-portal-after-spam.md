---
title: 스팸 메일을 보낸 후 제한된 사용자 포털에서 사용자 제거
ms.author: tracyp
author: MSFTTracyP
manager: dansimp
ms.date: 07/10/2019
audience: ITPro
ms.topic: article
f1_keywords:
- ms.exch.eac.ActionCenter.Restricted.Users.RestrictedUsers
ms.service: O365-seccomp
localization_priority: Priority
search.appverid:
- MET150
ms.assetid: 712cfcc1-31e8-4e51-8561-b64258a8f1e5
ms.collection:
- M365-security-compliance
description: 사용자가 스팸으로 분류되는 Office 365에서 계속해서 전자 메일을 보내는 경우 더 이상 메시지를 보낼 수 없게 됩니다.
ms.openlocfilehash: 56f1a34fe4b47a722ff1dace73dd001f0c4812a2
ms.sourcegitcommit: 33c8e9c16143650ca443d73e91631f9180a9268e
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/25/2019
ms.locfileid: "35854722"
---
# <a name="removing-a-user-from-the-restricted-users-portal-after-sending-spam-email"></a><span data-ttu-id="f9ece-103">스팸 메일을 보낸 후 제한된 사용자 포털에서 사용자 제거</span><span class="sxs-lookup"><span data-stu-id="f9ece-103">Removing a user from the Restricted Users portal after sending spam email</span></span>

<span data-ttu-id="f9ece-104">사용자가 계속해서 Office 365의 스팸으로 분류되는 전자 메일을 보내면 전자 메일을 보낼 수 없게 되지만 받을 수는 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f9ece-104">If a user continuously sends emails that are classified as spam from Office 365, they will be restricted from sending email, but will still be able to receive it.</span></span> <span data-ttu-id="f9ece-105">사용자가 서비스에 잘못된 아웃 바운드 보낸 사람으로 나열되고 다음의 경우 배달 못 함 보고서(NDR)를 받습니다.</span><span class="sxs-lookup"><span data-stu-id="f9ece-105">The user will be listed in the service as a bad outbound sender and will receive a Non-Delivery Report (NDR) that states:</span></span>

> <span data-ttu-id="f9ece-106">"유효한 보낸 사람으로 인식되지 않았기 때문에 메시지를 배달할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="f9ece-106">"Your message couldn't be delivered because you weren't recognized as a valid sender.</span></span> <span data-ttu-id="f9ece-107">가장 일반적인 이유는 전자 메일 주소가 스팸 메일을 보내는 것으로 의심어서 더 이상 전자 메일을 보낼 수 없는 경우입니다.</span><span class="sxs-lookup"><span data-stu-id="f9ece-107">The most common reason for this is that your email address is suspected of sending spam and it's no longer allowed to send email.</span></span>  <span data-ttu-id="f9ece-108">도움이 필요하면 전자 메일 관리자에게 문의하세요.</span><span class="sxs-lookup"><span data-stu-id="f9ece-108">Contact  your email admin for assistance.</span></span> <span data-ttu-id="f9ece-109">원격 서버에서 '550 5.1.8 액세스가 거부되었습니다. 잘못된 아웃 바운드 보낸 사람"이 반환되었습니다.</span><span class="sxs-lookup"><span data-stu-id="f9ece-109">Remote Server returned '550 5.1.8 Access denied, bad outbound sender."</span></span>

## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="f9ece-110">시작하기 전에 알아야 할 사항은 무엇인가요?</span><span class="sxs-lookup"><span data-stu-id="f9ece-110">What do you need to know before you begin?</span></span>
<span data-ttu-id="f9ece-111"><a name="sectionSection0"> </a></span><span class="sxs-lookup"><span data-stu-id="f9ece-111"></span></span>

<span data-ttu-id="f9ece-112">예상 완료 시간: 5분</span><span class="sxs-lookup"><span data-stu-id="f9ece-112">Estimated time to complete: 5 minutes</span></span>
  
<span data-ttu-id="f9ece-113">이러한 절차를 수행하려면 먼저 사용 권한을 할당받아야 합니다.</span><span class="sxs-lookup"><span data-stu-id="f9ece-113">You need to be assigned permissions before you can perform this procedure or procedures.</span></span> <span data-ttu-id="f9ece-114">필요한 권한을 확인하려면 [Exchange Online의 기능 사용 권한](http://technet.microsoft.com/library/15073ce1-0917-403b-8839-02a2ebc96e16.aspx) 항목에서 스팸 방지 항목을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="f9ece-114">You need to be assigned permissions before you can perform this procedure or procedures. To see what permissions you need, see the "Anti-malware" entry in the [Feature permissions in Exchange Online](http://technet.microsoft.com/library/15073ce1-0917-403b-8839-02a2ebc96e16.aspx) topic.</span></span>

<span data-ttu-id="f9ece-115">또한 원격 PowerShell을 통해 다음 절차를 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f9ece-115">The following procedure can also be performed via remote PowerShell.</span></span> <span data-ttu-id="f9ece-116">BlockedSenderAddress cmdlet을 사용하여 제한된 사용자 목록을 가져오고 Remove-BlockedSenderAddress을 사용하여 제한을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="f9ece-116">Use the Get-BlockedSenderAddress cmdlet to get the list of restricted users and Remove-BlockedSenderAddress to remove the restriction.</span></span> <span data-ttu-id="f9ece-117">Windows PowerShell을 사용하여 Exchange Online에 연결하는 방법에 대한 자세한 내용은 [Connect to Exchange Online Using Remote PowerShell](https://go.microsoft.com/fwlink/p/?linkid=396554)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="f9ece-117">To learn how to use Windows PowerShell to connect to Exchange Online, see [Connect to Exchange Online PowerShell](https://go.microsoft.com/fwlink/p/?linkid=396554).</span></span>

## <a name="remove-restrictions-for-a-blocked-office-365-email-account"></a><span data-ttu-id="f9ece-118">차단된 Office 365 전자 메일 계정에 대한 제한 사항 제거</span><span class="sxs-lookup"><span data-stu-id="f9ece-118">Remove restrictions for a blocked Office 365 email account</span></span>

<span data-ttu-id="f9ece-119">SCC(보안 및 준수 센터)에서 이 작업을 완료합니다.</span><span class="sxs-lookup"><span data-stu-id="f9ece-119">You complete this task in the Security & Compliance Center (SCC).</span></span> <span data-ttu-id="f9ece-120">SCC에 대한 자세한 내용은 [보안 및 준수 센터로 이동하세요.](go-to-the-securitycompliance-center.md)</span><span class="sxs-lookup"><span data-stu-id="f9ece-120">[Go to the Security & Compliance Center](go-to-the-securitycompliance-center.md) for more details about SCC.</span></span> <span data-ttu-id="f9ece-121">이러한 기능을 수행하려면 **조직 관리** 또는 **보안 관리자** 역할 그룹에 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="f9ece-121">You need to be in the **Organization Management** or the **Security Administrator** role group in order to perform these functions.</span></span> <span data-ttu-id="f9ece-122">SCC 역학 그룹에 대한 자세한 내용은 [보안 및 준수 센터의 사용 권한으로 이동하세요.](permissions-in-the-security-and-compliance-center.md)</span><span class="sxs-lookup"><span data-stu-id="f9ece-122">[Go to Permissions in the Security & Compliance Center](permissions-in-the-security-and-compliance-center.md) for more details about SCC role groups.</span></span>

1. <span data-ttu-id="f9ece-123">Office 365 전역 관리자 권한이 있는 회사 또는 학교 계정을 사용하여 Office 365 보안 및 규정 준수 센터에 로그인하고 왼쪽에 있는 목록에서 **위협 관리**를 확장하고 **검토**를 선택한 다음 **제한된 사용자**를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="f9ece-123">Using a work or school account that has Office 365 global administrator privileges, sign into the Office 365 Security and Compliance Center and in the list on the left, expand **Threat Management**, choose **Review**, and then choose **Restricted Users**.</span></span>
    
    > [!TIP]
    > <span data-ttu-id="f9ece-124">보안 &amp; 준수 센터에서 **제한된 사용자** 페이지(이전의 관리 센터)로 바로 이동하려면 다음 URL을 사용합니다. > [https://protection.office.com/#/restrictedusers](https://protection.office.com/?hash=/restrictedusers)</span><span class="sxs-lookup"><span data-stu-id="f9ece-124">To go directly to the **Restricted Users** page (formerly known as the Action Center) in the Security &amp; Compliance Center, use this URL: > [https://protection.office.com/#/restrictedusers](https://protection.office.com/?hash=/restrictedusers)</span></span>

2. <span data-ttu-id="f9ece-125">이 페이지에는 전자 메일을 보내지 못하도록 차단된 사용자 목록이 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="f9ece-125">This page will contain the list of users that have been blocked from sending email.</span></span>  <span data-ttu-id="f9ece-126">제한을 제거할 사용자를 찾은 다음 **차단 해제**를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="f9ece-126">Find the user you wish to remove restrictions from, and select **Unblock**.</span></span>

3. <span data-ttu-id="f9ece-127">플라이아웃하면 전송이 제한된 계정에 대한 세부 정보로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="f9ece-127">A fly-out will go into the details about the account whose sending is restricted.</span></span> <span data-ttu-id="f9ece-128">계정이 실제로 손상될 경우에 적절한 조치를 취하는지 확인하기 위해 권장 사항을 검토해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="f9ece-128">You should go through the recommendations to ensure you're taking the proper actions in case the account is actually compromised.</span></span> <span data-ttu-id="f9ece-129">완료되면 **다음**을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="f9ece-129">Click **Next** when it's done.</span></span>

4. <span data-ttu-id="f9ece-130">다음 화면에는 이후 손상을 방지하는 데 도움이 되는 권장 사항이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f9ece-130">The next screen has recommendations to help prevent future compromise.</span></span> <span data-ttu-id="f9ece-131">MFA(다단계 인증)를 사용하도록 설정하고 암호를 변경하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="f9ece-131">Enabling multi-factor authentication (MFA) and changing the passwords are a good defense.</span></span> <span data-ttu-id="f9ece-132">작업이 완료되면 **사용자 차단 해제**를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="f9ece-132">Click **Unblock user** when done.</span></span>

5. <span data-ttu-id="f9ece-133">**예**를 클릭하여 변경 내용을 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="f9ece-133">Click **Yes** to confirm the change.</span></span>

    > [!NOTE]
    > <span data-ttu-id="f9ece-134">제한이 제거되기까지 30분 정도 걸릴 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f9ece-134">It may take 30 minutes or more before restrictions are removed.</span></span> 

## <a name="making-sure-admins-are-alerted-when-this-happens"></a><span data-ttu-id="f9ece-135">이 경우에는 관리자에게 경고를 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="f9ece-135">Making sure admins are alerted when this happens</span></span>

<span data-ttu-id="f9ece-136">"전자 메일 전송 제한 사용자" 경고는 Office 365 보안 및 준수 경고 정책 페이지에서 정책으로 제공됩니다.</span><span class="sxs-lookup"><span data-stu-id="f9ece-136">A "User restricted from sending email" alert is available as a policy under the Office 365 Security & Compliance Alert policies page.</span></span> <span data-ttu-id="f9ece-137">이전에는 아웃 바운드 스팸 정책이었지만 이제는 Office 365 경고 플랫폼의 기본 기능입니다.</span><span class="sxs-lookup"><span data-stu-id="f9ece-137">This was formerly the outbound spam policy but is now native to the Office 365 alerting platform.</span></span> <span data-ttu-id="f9ece-138">경고에 대한 자세한 내용은 [보안 및 준수 센터의 경고 정책](alert-policies.md)으로 이동하세요.</span><span class="sxs-lookup"><span data-stu-id="f9ece-138">Go to [Alert policies in the Security & Compliance Center](alert-policies.md) for more information on alerts.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f9ece-139">경고가 작동하려면 감사 로그 검색이 설정되어 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="f9ece-139">For alerts to work, audit log search must to be turned on.</span></span> <span data-ttu-id="f9ece-140">자세한 내용은 Office [365 감사 로그 검색을 설정하거나 해제](turn-audit-log-search-on-or-off.md)하는 방법을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="f9ece-140">See how to [Turn Office 365 audit log search on or off](turn-audit-log-search-on-or-off.md) for more information.</span></span>

<span data-ttu-id="f9ece-141">이 경고의 정책은 기본값이며 모든 Office 365 테넌트와 함께 제공되며 설정하지 않아도 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f9ece-141">The policy for this alert is a default one and comes with every Office 365 tenant and does not need to be set up.</span></span> <span data-ttu-id="f9ece-142">심각도가 높은 경고로 간주되며 사용자가 메일을 보낼 수 없는 때마다 경고가 발생하면 구성된 TenantAdmins 그룹에 전자 메일을 보냅니다.</span><span class="sxs-lookup"><span data-stu-id="f9ece-142">It is considered a High severity alert and will email the configured TenantAdmins group when the alert is fired whenever a user has been restricted from sending mail.</span></span> <span data-ttu-id="f9ece-143">관리자는 SCC 포털 > 경고 > 경고 정책> 전자 메일 전송 제한 사용자 아래의 경고로 이동하여 이 경고가 발생했을 때 경고를 받는 그룹을 업데이트할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f9ece-143">Admins can update the group notified when this alert happens by going to the alert under the SCC portal > Alerts > Alert policies > Users restricted from sending email.</span></span>

<span data-ttu-id="f9ece-144">다음과 같은 경우 경고를 편집할 수 있게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f9ece-144">You will be able to Edit the alert to:</span></span>
- <span data-ttu-id="f9ece-145">전자 메일 알림 켜기/끄기</span><span class="sxs-lookup"><span data-stu-id="f9ece-145">Turn email notifications On/Off</span></span>
- <span data-ttu-id="f9ece-146">필수 받는 사람에게 전자 메일 보내기</span><span class="sxs-lookup"><span data-stu-id="f9ece-146">Email the required recipients</span></span>
- <span data-ttu-id="f9ece-147">하루당 받는 알림 제한</span><span class="sxs-lookup"><span data-stu-id="f9ece-147">Limit the notifications you get per day</span></span>

## <a name="checking-for-and-removing-restrictions-using-powershell"></a><span data-ttu-id="f9ece-148">PowerShell을 사용하여 제한 확인 및 제거</span><span class="sxs-lookup"><span data-stu-id="f9ece-148">Checking for and removing restrictions using PowerShell</span></span>
<span data-ttu-id="f9ece-149">제한된 사용자에 대한 PowerShell 명령은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="f9ece-149">The PowerShell commands for Restricted Users are:</span></span>
- <span data-ttu-id="f9ece-150">`Get-BlockedSenderAddress`: 실행하여 전자 메일을 보낼 수 없는 사용자 목록 검색</span><span class="sxs-lookup"><span data-stu-id="f9ece-150">`Get-BlockedSenderAddress`: Run to retreive the list of users that are restricted from sending email</span></span>
- <span data-ttu-id="f9ece-151">`Remove-BlockedSenderAddress`: 실행하여 제한된 사용자를 제거</span><span class="sxs-lookup"><span data-stu-id="f9ece-151">`Remove-BlockedSenderAddress`: Run to remove user(s) from being restricted</span></span>

## <a name="for-more-information"></a><span data-ttu-id="f9ece-152">자세한 내용</span><span class="sxs-lookup"><span data-stu-id="f9ece-152">For more information</span></span>

[<span data-ttu-id="f9ece-153">손상된 이메일 계정에 응답</span><span class="sxs-lookup"><span data-stu-id="f9ece-153">Responding to a compromised email account</span></span>](responding-to-a-compromised-email-account.md)

[<span data-ttu-id="f9ece-154">전자 메일 전송 제한 사용자 경고 이해</span><span class="sxs-lookup"><span data-stu-id="f9ece-154">Understanding the User restricted from sending email alert</span></span>](https://docs.microsoft.com/ko-KR/office365/securitycompliance/alert-policies)

[<span data-ttu-id="f9ece-155">아웃바운드 메시지용 높은 위험 배달 풀</span><span class="sxs-lookup"><span data-stu-id="f9ece-155">High-risk delivery pool for outbound messages</span></span>](high-risk-delivery-pool-for-outbound-messages.md)

[<span data-ttu-id="f9ece-156">보안 및 준수 센터의 사용 권한</span><span class="sxs-lookup"><span data-stu-id="f9ece-156">Permissions in the Security & Compliance Center</span></span>](permissions-in-the-security-and-compliance-center.md)

[<span data-ttu-id="f9ece-157">보안 및 준수 센터의 경고 정책</span><span class="sxs-lookup"><span data-stu-id="f9ece-157">Alert policies in the Office 365 Security & Compliance Center</span></span>](https://docs.microsoft.com/ko-KR/office365/securitycompliance/alert-policies)
