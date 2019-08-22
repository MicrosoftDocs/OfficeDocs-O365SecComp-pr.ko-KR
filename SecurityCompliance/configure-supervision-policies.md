---
title: 조직의 감독 정책 구성
ms.author: robmazz
author: robmazz
manager: laurawi
audience: Admin
ms.topic: article
f1_keywords:
- ms.o365.cc.SupervisoryReview
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- Strat_O365_IP
- M365-security-compliance
search.appverid:
- MET150
- MOE150
description: 관리 검토 정책을 설정 하 여 검토를 위한 직원 정보를 수집 합니다.
ms.openlocfilehash: c4735226235d557dc138d6eebaf9c7a84c39020c
ms.sourcegitcommit: 3f3f3ecb28ef65d023f3573f9a4e09a0586d8f53
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/21/2019
ms.locfileid: "36490785"
---
# <a name="configure-supervision-policies-for-your-organization"></a><span data-ttu-id="a8eb8-103">조직의 감독 정책 구성</span><span class="sxs-lookup"><span data-stu-id="a8eb8-103">Configure supervision policies for your organization</span></span>

<span data-ttu-id="a8eb8-104">감독 정책을 사용 하 여 내부 또는 외부 검토자가 검사할 직원 통신을 캡처할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a8eb8-104">Use supervision policies to capture employee communications for examination by internal or external reviewers.</span></span> <span data-ttu-id="a8eb8-105">감독 정책을 통해 조직의 통신을 모니터링 하는 방법에 대 한 자세한 내용은 [Office 365의 감독 정책을](supervision-policies.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="a8eb8-105">For more information about how supervision policies can help you monitor communications in your organization, see [Supervision policies in Office 365](supervision-policies.md).</span></span>

> [!NOTE]
> <span data-ttu-id="a8eb8-106">감독 정책에 따라 모니터링 되는 사용자에 게는 Microsoft 365 E5 규정 준수 라이선스, 고급 준수 추가 기능이 포함 된 Office 365 Enterprise E3 라이선스 또는 Office 365 Enterprise E5 구독에 포함 되어 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8eb8-106">Users monitored by supervision policies must have either a Microsoft 365 E5 Compliance license, an Office 365 Enterprise E3 license with the Advanced Compliance add-on, or be included in an Office 365 Enterprise E5 subscription.</span></span>
> <span data-ttu-id="a8eb8-107">기존 Enterprise E5 요금제가 없고, 감독을 려 고 하는 경우 [Office 365 Enterprise e 5의 평가판에 등록할](https://go.microsoft.com/fwlink/p/?LinkID=698279)수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a8eb8-107">If you don't have an existing Enterprise E5 plan and want to try supervision, you can [sign up for a trial of Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span></span>
  
<span data-ttu-id="a8eb8-108">Office 365 조직에서 감독을 설정 및 사용 하려면 다음 단계를 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8eb8-108">Follow these steps to set up and use supervision in your Office 365 organization:</span></span>
  
- <span data-ttu-id="a8eb8-109">**1 단계 (옵션)**: [감독을 위한 그룹 설정](#step-1-set-up-groups-for-supervision-optional)</span><span class="sxs-lookup"><span data-stu-id="a8eb8-109">**Step 1 (optional)**: [Set up groups for Supervision](#step-1-set-up-groups-for-supervision-optional)</span></span> 

    <span data-ttu-id="a8eb8-110">감독 사용을 시작 하기 전에 의사 소통을 검토 하 고 검토를 수행 해야 하는 사람을 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8eb8-110">Before you start using supervision, determine who needs communications reviewed and who performs reviews.</span></span> <span data-ttu-id="a8eb8-111">소수의 사용자만을 시작 하 여 감독의 작동 방식을 확인 하려는 경우 지금 그룹 설정 건너뛰기를 건너뛸 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a8eb8-111">If you want to get started with just a few users to see how supervision works, you can skip setting up groups for now.</span></span>

- <span data-ttu-id="a8eb8-112">**2 단계 (필수 사항)**: [조직에서 감독을 사용할 수 있도록 설정](#step-2-make-supervision-available-in-your-organization-required)</span><span class="sxs-lookup"><span data-stu-id="a8eb8-112">**Step 2 (required)**: [Make supervision available in your organization](#step-2-make-supervision-available-in-your-organization-required)</span></span>

    <span data-ttu-id="a8eb8-113">정책을 설정할 수 있도록 자신을 관리 검토 역할 그룹에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8eb8-113">Add yourself to the Supervisory Review role group so you can set up policies.</span></span> <span data-ttu-id="a8eb8-114">이 역할이 할당 된 모든 사용자는 준수 센터의 **감독** 페이지에 액세스할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a8eb8-114">Anyone who has this role assigned can access the **Supervision** page in the Compliance Center.</span></span> <span data-ttu-id="a8eb8-115">다시 볼 수 있는 전자 메일이 Exchange Online에서 호스팅되는 경우 각 검토자 [에 게 Exchange online에 대 한 원격 PowerShell 액세스](https://docs.microsoft.com/powershell/exchange/exchange-online/disable-access-to-exchange-online-powershell)권한이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8eb8-115">If reviewable email is hosted on Exchange Online, each reviewer must have [remote PowerShell access to Exchange Online](https://docs.microsoft.com/powershell/exchange/exchange-online/disable-access-to-exchange-online-powershell).</span></span>

- <span data-ttu-id="a8eb8-116">**3 단계 (선택 사항)**: [사용자 지정 중요 한 정보 유형 및 사용자 지정 키워드 사전 만들기](#step-3-create-custom-sensitive-information-types-and-custom-keyword-dictionaries-optional)</span><span class="sxs-lookup"><span data-stu-id="a8eb8-116">**Step 3 (optional)**: [Create custom sensitive information types and custom keyword dictionaries](#step-3-create-custom-sensitive-information-types-and-custom-keyword-dictionaries-optional)</span></span>

    <span data-ttu-id="a8eb8-117">감독 정책에 대 한 사용자 지정 중요 한 정보 유형 또는 사용자 지정 키워드 사전이 필요한 경우에는 감독 마법사를 시작 하기 전에 만들어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8eb8-117">If you need a custom sensitive info type or a custom keyword dictionary for your supervision policy, you need to create it before starting the supervision wizard.</span></span>

- <span data-ttu-id="a8eb8-118">**4 단계 (필수 사항)**: [감독 정책 설정](#step-4-set-up-a-supervision-policy-required)</span><span class="sxs-lookup"><span data-stu-id="a8eb8-118">**Step 4 (required)**: [Set up a supervision policy](#step-4-set-up-a-supervision-policy-required)</span></span>

    <span data-ttu-id="a8eb8-119">준수 센터에서 감독 정책을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a8eb8-119">You create supervision policies in the Compliance Center.</span></span> <span data-ttu-id="a8eb8-120">이러한 정책은 조직에서 검토할 대상이 되는 통신을 정의 하 고 검토를 수행 하는 사람을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8eb8-120">These policies define which communications are subject to review in your organization and specifies who performs reviews.</span></span> <span data-ttu-id="a8eb8-121">통신에는 전자 메일 및 Microsoft 팀 통신과 타사 플랫폼 통신 (예: Facebook, Twitter 등)이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a8eb8-121">Communications include email and Microsoft Teams communications, and 3rd-party platform communications (such as Facebook, Twitter, etc.)</span></span>

- <span data-ttu-id="a8eb8-122">**5 단계 (선택 사항)**: [감독 정책 테스트](#step-5-test-your-supervision-policy-optional)</span><span class="sxs-lookup"><span data-stu-id="a8eb8-122">**Step 5 (optional)**: [Test your supervision policy](#step-5-test-your-supervision-policy-optional)</span></span>

    <span data-ttu-id="a8eb8-123">감독 정책을 테스트 하 여 원하는 대로 작동 하는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8eb8-123">Test your supervision policy to make sure it functions as desired.</span></span> <span data-ttu-id="a8eb8-124">규정 준수 전략이 표준을 충족 하는지 확인 하는 것이 중요 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8eb8-124">It is important to ensure that your compliance strategy is meeting your standards.</span></span>

- <span data-ttu-id="a8eb8-125">**6 단계 (선택 사항)**: [Office 365 감독 대시보드를 사용 하지 않고 감독 되는 통신을 검토 하는 검토자를 위해 Outlook을 구성](#step-6-configure-outlook-for-reviewers-optional) 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8eb8-125">**Step 6 (optional)**: [Configure Outlook for reviewers who do not want to use Office 365 supervision dashboard to review supervised communications](#step-6-configure-outlook-for-reviewers-optional)</span></span>

    <span data-ttu-id="a8eb8-126">사용자가 각 항목을 평가 하 고 분류할 수 있도록 Outlook 클라이언트 내의 감독 기능에 대 한 액세스 권한을 검토자에 게 보내도록 Outlook을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8eb8-126">Configure Outlook to give reviewers access to the supervision functionality within the Outlook client so they can assess and categorize each item.</span></span>

## <a name="step-1-set-up-groups-for-supervision-optional"></a><span data-ttu-id="a8eb8-127">1 단계: 감독에 대 한 그룹 설정 (선택 사항)</span><span class="sxs-lookup"><span data-stu-id="a8eb8-127">Step 1: Set up groups for Supervision (optional)</span></span>

 <span data-ttu-id="a8eb8-128">감독 정책을 만들 때, 의사 소통을 검토 한 사람과 검토를 수행 하는 사람을 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8eb8-128">When you create a supervision policy, you define who has their communications reviewed and who performs reviews.</span></span> <span data-ttu-id="a8eb8-129">정책에서는 전자 메일 주소를 사용 하 여 개인 이나 사용자 그룹을 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8eb8-129">In the policy, you'll use email addresses to identify individuals or groups of people.</span></span> <span data-ttu-id="a8eb8-130">설정을 단순화 하기 위해 통신을 검토 한 사용자에 대 한 그룹을 만들고 해당 통신을 검토할 사용자에 대 한 그룹을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a8eb8-130">To simplify your setup, you can create groups for people who have their communication reviewed and groups for people who review those communications.</span></span> <span data-ttu-id="a8eb8-131">그룹을 사용 하는 경우 몇 가지 필요할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a8eb8-131">If you're using groups, you may need several.</span></span> <span data-ttu-id="a8eb8-132">예를 들어 서로 다른 두 사용자 그룹 간의 통신을 모니터링 하거나 감독 하지 않을 그룹을 지정 하려는 경우</span><span class="sxs-lookup"><span data-stu-id="a8eb8-132">For example, you want to monitor communications between two distinct groups of people or if you want to specify a group that isn't going to be supervised.</span></span>

<span data-ttu-id="a8eb8-133">다음 차트를 사용 하 여 조직에서 감독 정책을 위해 그룹을 구성 하는 데 도움이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a8eb8-133">Use the following chart to help you configure groups in your organization for supervision policies:</span></span>

| <span data-ttu-id="a8eb8-134">**정책 구성원**</span><span class="sxs-lookup"><span data-stu-id="a8eb8-134">**Policy Member**</span></span> | <span data-ttu-id="a8eb8-135">**지원 되는 그룹**</span><span class="sxs-lookup"><span data-stu-id="a8eb8-135">**Supported Groups**</span></span> | <span data-ttu-id="a8eb8-136">**지원 되지 않는 그룹**</span><span class="sxs-lookup"><span data-stu-id="a8eb8-136">**Unsupported Groups**</span></span> |
|:-----|:-----|:-----|
|<span data-ttu-id="a8eb8-137">감독 사용자</span><span class="sxs-lookup"><span data-stu-id="a8eb8-137">Supervised users</span></span> <br> <span data-ttu-id="a8eb8-138">감독 되지 않은 사용자</span><span class="sxs-lookup"><span data-stu-id="a8eb8-138">Non-supervised users</span></span> | <span data-ttu-id="a8eb8-139">메일 그룹</span><span class="sxs-lookup"><span data-stu-id="a8eb8-139">Distribution groups</span></span> <br> <span data-ttu-id="a8eb8-140">Office 365 그룹</span><span class="sxs-lookup"><span data-stu-id="a8eb8-140">Office 365 groups</span></span> | <span data-ttu-id="a8eb8-141">동적 메일 그룹</span><span class="sxs-lookup"><span data-stu-id="a8eb8-141">Dynamic distribution groups</span></span> |
| <span data-ttu-id="a8eb8-142">가</span><span class="sxs-lookup"><span data-stu-id="a8eb8-142">Reviewers</span></span> | <span data-ttu-id="a8eb8-143">메일 사용 가능 보안 그룹</span><span class="sxs-lookup"><span data-stu-id="a8eb8-143">Mail-enabled security groups</span></span>  | <span data-ttu-id="a8eb8-144">메일 그룹</span><span class="sxs-lookup"><span data-stu-id="a8eb8-144">Distribution groups</span></span> <br> <span data-ttu-id="a8eb8-145">동적 메일 그룹</span><span class="sxs-lookup"><span data-stu-id="a8eb8-145">Dynamic distribution groups</span></span> |
  
<span data-ttu-id="a8eb8-146">감독 되는 사용자에 대 한 Office 365 그룹을 선택 하면 정책이 공유 Office 365 사서함의 콘텐츠 및 해당 그룹과 연결 된 Microsoft 팀 채널을 모니터링 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8eb8-146">When you select an Office 365 group for supervised users, the policy monitors the content of the shared Office 365 mailbox and the Microsoft Teams channels associated with the group.</span></span> <span data-ttu-id="a8eb8-147">메일 그룹을 선택 하는 경우 정책은 개별 사용자 사서함을 모니터링 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8eb8-147">When you select a distribution list, the policy monitors individual user mailboxes.</span></span>

<span data-ttu-id="a8eb8-148">대규모 엔터프라이즈 조직에서 감독 사용자를 관리 하려면 대규모 그룹의 모든 사용자를 모니터링 해야 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a8eb8-148">To manage supervised users in large enterprise organizations, you may need to monitor all users across large groups.</span></span> <span data-ttu-id="a8eb8-149">PowerShell을 사용 하 여 할당 된 그룹에 대 한 전역 감독 정책에 대 한 메일 그룹을 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a8eb8-149">You can use PowerShell to configure a distribution group for a global supervision policy for the assigned group.</span></span> <span data-ttu-id="a8eb8-150">이를 통해 단일 정책을 사용 하는 수천 명의 사용자를 모니터링 하 고 조직에 새 직원이 참가할 때 감독 정책을 업데이트할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a8eb8-150">This enables you to monitor thousands of users with a single policy and keep the supervision policy updated as new employees join your organization.</span></span>

1. <span data-ttu-id="a8eb8-151">다음 속성을 사용 하 여 전역 감독 정책에 대 한 전용 [메일 그룹](https://docs.microsoft.com/powershell/module/exchange/users-and-groups/new-distributiongroup?view=exchange-ps) 을 만듭니다 .이 메일 그룹이 다른 목적이 나 기타 Office 365 서비스에 사용 되지 않는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8eb8-151">Create a dedicated [distribution group](https://docs.microsoft.com/powershell/module/exchange/users-and-groups/new-distributiongroup?view=exchange-ps) for your global supervision policy with the following properties: Make sure that this distribution group isn't used for other purposes or other Office 365 services.</span></span>

    - <span data-ttu-id="a8eb8-152">**MemberDepartRestriction = 닫힘**</span><span class="sxs-lookup"><span data-stu-id="a8eb8-152">**MemberDepartRestriction = Closed**.</span></span> <span data-ttu-id="a8eb8-153">사용자가 메일 그룹에서 자신을 제거할 수 없도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8eb8-153">Ensures that users cannot remove themselves from the distribution group.</span></span>
    - <span data-ttu-id="a8eb8-154">**Memberjoinrestriction = 닫힘**</span><span class="sxs-lookup"><span data-stu-id="a8eb8-154">**MemberJoinRestriction = Closed**.</span></span> <span data-ttu-id="a8eb8-155">사용자가 메일 그룹에 자신을 추가할 수 없도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8eb8-155">Ensures that users cannot add themselves to the distribution group.</span></span>
    - <span data-ttu-id="a8eb8-156">**ModerationEnabled = True**</span><span class="sxs-lookup"><span data-stu-id="a8eb8-156">**ModerationEnabled = True**.</span></span> <span data-ttu-id="a8eb8-157">이 그룹으로 전송 되는 모든 메시지에 대 한 승인이 가능 하며, 해당 그룹이 감독 정책 구성 외부에서 통신 하는 데 사용 되 고 있지는 않은지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8eb8-157">Ensures that all messages sent to this group are subject to approval and that the group is not being used to communicate outside of the supervision policy configuration.</span></span>

    ```
    New-DistributionGroup -Name <your group name> -Alias <your group alias> -MemberDepartRestriction 'Closed' -MemberJoinRestriction 'Closed' -ModerationEnabled $true
    ```
2. <span data-ttu-id="a8eb8-158">조직의 감독 정책에 추가한 사용자를 추적 하려면 사용 되지 않는 [Exchange 사용자 지정 특성](https://docs.microsoft.com/Exchange/recipients/mailbox-custom-attributes?view=exchserver-2019&viewFallbackFrom=exchonline-ww) 을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8eb8-158">Select an unused [Exchange custom attribute](https://docs.microsoft.com/Exchange/recipients/mailbox-custom-attributes?view=exchserver-2019&viewFallbackFrom=exchonline-ww) to track users added to the supervision policy in your organization.</span></span>

3. <span data-ttu-id="a8eb8-159">다음 PowerShell 스크립트를 반복 된 일정에 따라 실행 하 여 감독 정책에 사용자를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8eb8-159">Run the following PowerShell script on a recurring schedule to add users to the supervision policy:</span></span>

    ```
    $Mbx = (Get-Mailbox -RecipientTypeDetails UserMailbox -ResultSize Unlimited -Filter {CustomAttribute9 -eq $Null})
    $i = 0
    ForEach ($M in $Mbx) 
    {
      Write-Host "Adding" $M.DisplayName
      Add-DistributionGroupMember -Identity <your group name> -Member $M.DistinguishedName -ErrorAction SilentlyContinue
      Set-Mailbox -Identity $M.Alias -<your custom attribute name> SRAdded 
      $i++
    }
    Write-Host $i "Mailboxes added to supervisory review distribution group."
    ```

<span data-ttu-id="a8eb8-160">그룹을 설정 하는 방법에 대 한 자세한 내용은 다음을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="a8eb8-160">For more information about setting up groups, see:</span></span>

- [<span data-ttu-id="a8eb8-161">메일 그룹 만들기 및 관리</span><span class="sxs-lookup"><span data-stu-id="a8eb8-161">Create and manage distribution groups</span></span>](https://docs.microsoft.com/Exchange/recipients-in-exchange-online/manage-distribution-groups/manage-distribution-groups)
- [<span data-ttu-id="a8eb8-162">메일 사용 가능 보안 그룹 관리</span><span class="sxs-lookup"><span data-stu-id="a8eb8-162">Manage mail-enabled security groups</span></span>](https://docs.microsoft.com/Exchange/recipients-in-exchange-online/manage-mail-enabled-security-groups)
- [<span data-ttu-id="a8eb8-163">Office 365 그룹 개요</span><span class="sxs-lookup"><span data-stu-id="a8eb8-163">Overview of Office 365 Groups</span></span>](https://docs.microsoft.com/office365/admin/create-groups/office-365-groups?view=o365-worldwide)

## <a name="step-2-make-supervision-available-in-your-organization-required"></a><span data-ttu-id="a8eb8-164">2 단계: 조직에서 감독을 사용할 수 있도록 설정 (필수)</span><span class="sxs-lookup"><span data-stu-id="a8eb8-164">Step 2: Make supervision available in your organization (required)</span></span>

<span data-ttu-id="a8eb8-165">**감독** 을 준수 센터에서 메뉴 옵션으로 사용할 수 있도록 하려면 관리 검토 관리자 역할을 할당 받아야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8eb8-165">To make **Supervision** available as a menu option in the Compliance Center, you must be assigned the Supervisory Review Administrator role.</span></span>
  
<span data-ttu-id="a8eb8-166">이렇게 하려면 자신을 관리 검토 역할 그룹의 구성원으로 추가 하거나 역할 그룹을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a8eb8-166">To do this, you can either add yourself as a member of the Supervisory Review role group, or you can create a role group.</span></span>
  
### <a name="add-members-to-the-supervisory-review-role-group"></a><span data-ttu-id="a8eb8-167">관리 검토 역할 그룹에 구성원 추가</span><span class="sxs-lookup"><span data-stu-id="a8eb8-167">Add members to the Supervisory Review role group</span></span>

1. <span data-ttu-id="a8eb8-168">Office 365 [https://protection.office.com](https://protection.office.com) 조직의 관리자 계정에 대 한 자격 증명을 사용 하 여 로그인 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8eb8-168">Sign into [https://protection.office.com](https://protection.office.com) using credentials for an admin account in your Office 365 organization.</span></span>

2. <span data-ttu-id="a8eb8-169">준수 센터에서 **사용 권한**으로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8eb8-169">In the Compliance Center, go to **Permissions**.</span></span>

3. <span data-ttu-id="a8eb8-170">**관리 검토** 역할 그룹을 선택한 다음 편집 아이콘을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8eb8-170">Select the **Supervisory Review** role group and then click the Edit icon.</span></span>

4. <span data-ttu-id="a8eb8-171">**구성원** 섹션에서 조직에 대 한 감독을 관리 하려는 사용자를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8eb8-171">In the **Members** section, add the people who you want to manage supervision for your organization.</span></span>

### <a name="create-a-new-role-group"></a><span data-ttu-id="a8eb8-172">새 역할 그룹 만들기</span><span class="sxs-lookup"><span data-stu-id="a8eb8-172">Create a new role group</span></span>

1. <span data-ttu-id="a8eb8-173">Office 365 [https://protection.office.com](https://protection.office.com) 조직의 관리자 계정에 대 한 자격 증명을 사용 하 여 로그인 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8eb8-173">Sign into [https://protection.office.com](https://protection.office.com) using credentials for an admin account in your Office 365 organization.</span></span>

2. <span data-ttu-id="a8eb8-174">준수 센터에서 **사용 권한** 으로 이동한 다음 추가 (**+**)를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8eb8-174">In the Compliance Center, go to **Permissions** and then click Add (**+**).</span></span>

3. <span data-ttu-id="a8eb8-175">**역할** 섹션에서 추가 (**+**)를 클릭 하 고 아래로 스크롤하여 **관리 검토 관리자**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8eb8-175">In the **Roles** section, click Add (**+**) and scroll down to **Supervisory Review Administrator**.</span></span> <span data-ttu-id="a8eb8-176">이 역할을 역할 그룹에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8eb8-176">Add this role to the role group.</span></span>

4. <span data-ttu-id="a8eb8-177">**구성원** 섹션에서 조직에 대 한 감독을 관리 하려는 사용자를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8eb8-177">In the **Members** section, add the people who you want to manage supervision for your organization.</span></span>

<span data-ttu-id="a8eb8-178">역할 그룹 및 사용 권한에 대 한 자세한 내용은 [준수 센터의 사용 권한을](permissions-in-the-security-and-compliance-center.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="a8eb8-178">For more information about role groups and permissions, see [Permissions in the Compliance Center](permissions-in-the-security-and-compliance-center.md).</span></span>

### <a name="enable-remote-powershell-access-for-reviewers-if-email-is-hosted-on-exchange-online"></a><span data-ttu-id="a8eb8-179">검토자에 대해 원격 PowerShell 액세스 사용 (전자 메일이 Exchange Online에서 호스트 되는 경우)</span><span class="sxs-lookup"><span data-stu-id="a8eb8-179">Enable remote PowerShell access for reviewers (if email is hosted on Exchange Online)</span></span>

1. <span data-ttu-id="a8eb8-180">[사용 또는 사용 안 함 Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/disable-access-to-exchange-online-powershell)에 대 한 지침을 따릅니다.</span><span class="sxs-lookup"><span data-stu-id="a8eb8-180">Follow the guidance in [Enable or disable access to Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/disable-access-to-exchange-online-powershell).</span></span>

## <a name="step-3-create-custom-sensitive-information-types-and-custom-keyword-dictionaries-optional"></a><span data-ttu-id="a8eb8-181">3 단계: 사용자 지정 중요 한 정보 유형 및 사용자 지정 키워드 사전 만들기 (선택 사항)</span><span class="sxs-lookup"><span data-stu-id="a8eb8-181">Step 3: Create custom sensitive information types and custom keyword dictionaries (optional)</span></span>

<span data-ttu-id="a8eb8-182">감독 정책 마법사에서 기존 사용자 지정 중요 한 정보 유형 또는 사용자 지정 키워드 사전을 선택 하려면 먼저 필요한 경우 이러한 항목을 만들어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8eb8-182">In order to pick from existing custom sensitive information types or custom keyword dictionaries in the supervision policy wizard, you first need to create these items if needed.</span></span>

### <a name="create-custom-keyword-dictionarylexicon-optional"></a><span data-ttu-id="a8eb8-183">사용자 지정 키워드 사전/어휘 만들기 (선택 사항)</span><span class="sxs-lookup"><span data-stu-id="a8eb8-183">Create custom keyword dictionary/lexicon (optional)</span></span>

<span data-ttu-id="a8eb8-184">메모장과 같은 텍스트 편집기를 사용 하 여 감독 정책에서 모니터링할 키워드 용어를 포함 하는 파일을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a8eb8-184">Use a text editor (like Notepad), to create a file that includes the keyword terms you'd like to monitor in a supervision policy.</span></span> <span data-ttu-id="a8eb8-185">각 용어가 별도의 줄에 있는지 확인 하 고 파일을 **유니코드/u t f-16 (꼬마)** 형식으로 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8eb8-185">Make sure that each term is on a separate line and save the file in the **Unicode/UTF-16 (Little Endian)** format.</span></span>

### <a name="create-custom-sensitive-information-types"></a><span data-ttu-id="a8eb8-186">사용자 지정 중요 한 정보 유형 만들기</span><span class="sxs-lookup"><span data-stu-id="a8eb8-186">Create custom sensitive information types</span></span>

1. <span data-ttu-id="a8eb8-187">새로운 중요 한 정보 유형을 만들고 Office 365 보안 & 준수 센터에 사용자 지정 사전을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8eb8-187">Create a new sensitive information type and add your custom dictionary in the Office 365 Security & Compliance Center.</span></span> <span data-ttu-id="a8eb8-188">**중요 한 정보** 유형 **분류** \> 로 이동 하 여 **새 중요 한 정보 유형 마법사**의 단계를 따릅니다.</span><span class="sxs-lookup"><span data-stu-id="a8eb8-188">Navigate to **Classifications** \> **Sensitive info types** and follow the steps in the **New sensitive info type wizard**.</span></span> <span data-ttu-id="a8eb8-189">여기에서 다음을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8eb8-189">Here you will:</span></span>

    - <span data-ttu-id="a8eb8-190">중요 한 정보 유형에 대 한 이름 및 설명 정의</span><span class="sxs-lookup"><span data-stu-id="a8eb8-190">Define a name and description for the sensitive info type</span></span>
    - <span data-ttu-id="a8eb8-191">근접성, 신뢰 수준 및 주 패턴 요소 정의</span><span class="sxs-lookup"><span data-stu-id="a8eb8-191">Define the proximity, confidence level, and primary pattern elements</span></span>
    - <span data-ttu-id="a8eb8-192">일치 요소에 대 한 요구 사항으로 사용자 지정 사전 가져오기</span><span class="sxs-lookup"><span data-stu-id="a8eb8-192">Import your custom dictionary as a requirement for the matching element</span></span>
    - <span data-ttu-id="a8eb8-193">선택 항목 검토 및 중요 한 정보 유형 만들기</span><span class="sxs-lookup"><span data-stu-id="a8eb8-193">Review your selections and create the sensitive info type</span></span>

    <span data-ttu-id="a8eb8-194">자세한 내용은 [사용자 지정 중요 한 정보 유형 만들기](create-a-custom-sensitive-information-type.md) 및 [키워드 사전 만들기](create-a-keyword-dictionary.md) 를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="a8eb8-194">For more detailed information, see [Create a custom sensitive information type](create-a-custom-sensitive-information-type.md) and [Create a keyword dictionary](create-a-keyword-dictionary.md)</span></span>

    <span data-ttu-id="a8eb8-195">사용자 지정 사전/어휘를 만든 후에는 [DlpKeywordDictionary](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-dlp/get-dlpkeyworddictionary) cmdlet을 사용 하 여 구성 된 키워드를 보거나 [DlpKeywordDictionary](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-dlp/set-dlpkeyworddictionary) cmdlet에서 용어를 추가 및 제거할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a8eb8-195">After the custom dictionary/lexicon is created, you can view the configured keywords with the [Get-DlpKeywordDictionary](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-dlp/get-dlpkeyworddictionary) cmdlet or add and remove terms using the [Set-DlpKeywordDictionary](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-dlp/set-dlpkeyworddictionary) cmdlet.</span></span>

## <a name="step-4-set-up-a-supervision-policy-required"></a><span data-ttu-id="a8eb8-196">4 단계: 감독 정책 설정 (필수)</span><span class="sxs-lookup"><span data-stu-id="a8eb8-196">Step 4: Set up a supervision policy (required)</span></span>
  
1. <span data-ttu-id="a8eb8-197">Office 365 [https://protection.office.com](https://protection.office.com) 조직의 관리자 계정에 대 한 자격 증명을 사용 하 여 로그인 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8eb8-197">Sign into [https://protection.office.com](https://protection.office.com) using credentials for an admin account in your Office 365 organization.</span></span>

2. <span data-ttu-id="a8eb8-198">준수 센터에서 **감독**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8eb8-198">In the Compliance Center, select **Supervision**.</span></span>
  
3. <span data-ttu-id="a8eb8-199">**만들기** 를 선택 하 고 마법사의 지시에 따라 정책 구성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8eb8-199">Select **Create** and follow the wizard to set up the policy configuration.</span></span> <span data-ttu-id="a8eb8-200">마법사를 사용 하 여 다음을 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a8eb8-200">Using the wizard, you will:</span></span>

    - <span data-ttu-id="a8eb8-201">정책에 이름과 설명을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8eb8-201">Give the policy a name and description.</span></span>
    - <span data-ttu-id="a8eb8-202">제외할 사용자 또는 그룹 선택을 비롯 하 여 감독할 사용자 또는 그룹을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8eb8-202">Choose the users or groups to supervise, including choosing users or groups you'd like to exclude.</span></span>
    - <span data-ttu-id="a8eb8-203">감독 정책 [조건을](supervision-policies.md#ConditionalSettings)정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8eb8-203">Define the supervision policy [conditions](supervision-policies.md#ConditionalSettings).</span></span> <span data-ttu-id="a8eb8-204">메시지 주소, 키워드, 파일 형식 및 크기 일치 조건에서 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a8eb8-204">You can choose from message address, keyword, file types, and size match conditions.</span></span>
    - <span data-ttu-id="a8eb8-205">중요 한 정보 유형을 포함 하 고 싶은 경우 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8eb8-205">Choose if you'd like to include sensitive information types.</span></span> <span data-ttu-id="a8eb8-206">여기에서 기본 및 사용자 지정 중요 한 정보 유형을 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a8eb8-206">This is where you can select default and custom sensitive info types.</span></span>
    - <span data-ttu-id="a8eb8-207">공격적인 언어 모델을 사용 하도록 설정 하려면 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8eb8-207">Choose if you'd like to enable the offensive language model.</span></span> <span data-ttu-id="a8eb8-208">이는 전자 메일 메시지 본문에서 보내거나 받은 부적절 한 언어를 감지 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8eb8-208">This detects inappropriate language sent or received in the body of email messages.</span></span>
    - <span data-ttu-id="a8eb8-209">검토할 통신의 비율을 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8eb8-209">Define the percentage of communications to review.</span></span>
    - <span data-ttu-id="a8eb8-210">정책에 대 한 검토자를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8eb8-210">Choose the reviewers for the policy.</span></span> <span data-ttu-id="a8eb8-211">검토자는 개별 사용자 또는 [메일 사용이 가능한 보안 그룹이](https://docs.microsoft.com/Exchange/recipients-in-exchange-online/manage-mail-enabled-security-groups#create-a-mail-enabled-security-group)될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a8eb8-211">Reviewers can be individual users or [mail-enabled security groups](https://docs.microsoft.com/Exchange/recipients-in-exchange-online/manage-mail-enabled-security-groups#create-a-mail-enabled-security-group).</span></span> <span data-ttu-id="a8eb8-212">모든 검토자에 게 Exchange Online에서 호스트 되는 사서함이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8eb8-212">All reviewers must have mailboxes hosted on Exchange Online.</span></span>
    - <span data-ttu-id="a8eb8-213">정책 선택을 검토 하 고 정책을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a8eb8-213">Review your policy selections and create the policy.</span></span>

## <a name="step-5-test-your-supervision-policy-optional"></a><span data-ttu-id="a8eb8-214">5 단계: 감독 정책 테스트 (선택 사항)</span><span class="sxs-lookup"><span data-stu-id="a8eb8-214">Step 5: Test your supervision policy (optional)</span></span>

<span data-ttu-id="a8eb8-215">감독 정책을 만든 후에는 테스트를 통해 정의한 조건이 정책에 의해 적절 하 게 적용 되는지 확인 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="a8eb8-215">After you create a supervision policy, it's a good idea to test to make sure that the conditions you defined are being properly enforced by the policy.</span></span> <span data-ttu-id="a8eb8-216">또한 감독 정책에 중요 한 정보 유형이 포함 되어 있는 경우 [DLP (데이터 손실 방지) 정책을 테스트할](create-test-tune-dlp-policy.md) 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a8eb8-216">You may also want to [test your data loss prevention (DLP) policies](create-test-tune-dlp-policy.md) if your supervision policies include sensitive information types.</span></span> <span data-ttu-id="a8eb8-217">다음 단계에 따라 감독 정책을 테스트 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8eb8-217">Follow these steps to test your supervision policy:</span></span>

1. <span data-ttu-id="a8eb8-218">테스트할 정책에 정의 된 감독 된 사용자로 로그인 한 전자 메일 클라이언트 또는 Microsoft 팀을 엽니다.</span><span class="sxs-lookup"><span data-stu-id="a8eb8-218">Open an email client or Microsoft Teams logged in as a supervised user defined in the policy you want to test.</span></span>
2. <span data-ttu-id="a8eb8-219">감독 정책에 정의한 기준을 충족 하는 전자 메일 또는 Microsoft 팀 채팅을 보냅니다.</span><span class="sxs-lookup"><span data-stu-id="a8eb8-219">Send an email or Microsoft Teams chat that meets the criteria you've defined in the supervision policy.</span></span> <span data-ttu-id="a8eb8-220">키워드, 첨부 파일 크기, 도메인 등이 될 수 있습니다. 정책에서 구성 된 조건부 설정이 너무 제한적일 또는 너무 lenient 인지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8eb8-220">This can be a keyword, attachment size, domain, etc. Make sure that you determine if your configured conditional settings in the policy are too restrictive or too lenient.</span></span>

    > [!Note]
    > <span data-ttu-id="a8eb8-221">정의 된 정책이 적용 되는 전자 메일은 거의 실시간으로 처리 되며 정책이 구성 된 직후에 테스트할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a8eb8-221">Emails subject to defined policies are processed in near real-time and can be tested immediately after the policy is configured.</span></span> <span data-ttu-id="a8eb8-222">Microsoft 팀의 채팅에는 정책에서 전체 프로세스를 수행 하는 데 최대 24 시간이 걸릴 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a8eb8-222">Chats in Microsoft Teams can take up to 24 hours to fully process in a policy.</span></span> 

3. <span data-ttu-id="a8eb8-223">감독 정책에 지정 된 검토자로 Office 365 테 넌 트에 로그인 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8eb8-223">Log into your Office 365 tenant as a reviewer designated in the supervision policy.</span></span> <span data-ttu-id="a8eb8-224">*사용자 지정 정책이* > **열려** 있는 **감독** > 을 탐색 하 여 정책에 대 한 보고서를 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8eb8-224">Navigate to **Supervision** > *Your Custom Policy* > **Open** to view the report for the policy.</span></span>

## <a name="step-6-configure-outlook-for-reviewers-optional"></a><span data-ttu-id="a8eb8-225">6 단계: Outlook for 검토자별로 구성 (선택 사항)</span><span class="sxs-lookup"><span data-stu-id="a8eb8-225">Step 6: Configure Outlook for reviewers (optional)</span></span>

<span data-ttu-id="a8eb8-226">통신을 검토 하기 위해 Office 365의 감독 대시보드 대신 Outlook을 사용 하려는 검토자는 Outlook 클라이언트를 구성 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8eb8-226">Reviewers that want to use Outlook instead of the Supervision dashboard in Office 365 to review communications must configure their Outlook client.</span></span>

### <a name="step-1-copy-the-address-for-the-supervision-mailbox"></a><span data-ttu-id="a8eb8-227">1 단계: 감독 사서함의 주소 복사</span><span class="sxs-lookup"><span data-stu-id="a8eb8-227">Step 1: Copy the address for the supervision mailbox</span></span>

<span data-ttu-id="a8eb8-228">Outlook 데스크톱에 대해 검토를 구성 하려면 감독 정책 설정의 일부로 만들어진 감독 사서함의 주소가 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8eb8-228">To configure review for Outlook desktop, you need the address for the supervision mailbox created as part of the supervision policy setup.</span></span>
  
> [!NOTE]
> <span data-ttu-id="a8eb8-229">다른 사용자가 정책을 만든 경우이 주소에서 추가 기능을 설치 하도록 요청 받아야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8eb8-229">If someone else created the policy, you need to get this address from them to install the add-in.</span></span>

<span data-ttu-id="a8eb8-230">**감독 사서함 주소를 찾으려면**</span><span class="sxs-lookup"><span data-stu-id="a8eb8-230">**To find the supervision mailbox address**</span></span>
  
1. <span data-ttu-id="a8eb8-231">조직의 관리자 계정에 대 한 자격 증명을 사용 하 여 [준수 센터](https://compliance.microsoft.com) 에 로그인 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8eb8-231">Sign into the [Compliance Center](https://compliance.microsoft.com) using credentials for an admin account in your organization.</span></span>

2. <span data-ttu-id="a8eb8-232">**감독**으로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8eb8-232">Go to **Supervision**.</span></span>

3. <span data-ttu-id="a8eb8-233">검토 하려는 통신에 대 한 감독 정책을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8eb8-233">Select a supervision policy for the communications you want to review.</span></span>

4. <span data-ttu-id="a8eb8-234">정책 세부 정보 플라이 아웃의 **감독 사서함**에서 주소를 복사 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8eb8-234">In the policy details flyout, under **Supervision mailbox**, copy the address.</span></span><br/><span data-ttu-id="a8eb8-235">![감독 사서함 주소가 강조 표시 된 감독 정책의 세부 정보 플라이 아웃의 ' 감독 사서함 ' 섹션](media/71779d0e-4f01-4dd3-8234-5f9c30eeb067.jpg)</span><span class="sxs-lookup"><span data-stu-id="a8eb8-235">![The 'Supervision Mailbox' section of a supervision policy's details flyout showing the supervision mailbox address highlighted](media/71779d0e-4f01-4dd3-8234-5f9c30eeb067.jpg)</span></span>
  
### <a name="step-2-configure-the-supervision-mailbox-for-outlook-access"></a><span data-ttu-id="a8eb8-236">2 단계: Outlook 액세스를 위한 감독 사서함 구성</span><span class="sxs-lookup"><span data-stu-id="a8eb8-236">Step 2: Configure the supervision mailbox for Outlook access</span></span>

<span data-ttu-id="a8eb8-237">다음으로, Outlook을 감독 사서함에 연결할 수 있도록 검토자가 몇 개의 Exchange Online PowerShell 명령을 실행 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8eb8-237">Next, reviewers need to run a couple Exchange Online PowerShell commands so they can connect Outlook to the supervision mailbox.</span></span>
  
1. <span data-ttu-id="a8eb8-238">Exchange Online PowerShell에 연결합니다.</span><span class="sxs-lookup"><span data-stu-id="a8eb8-238">Connect to Exchange Online PowerShell.</span></span> [<span data-ttu-id="a8eb8-239">어떻게 해야 합니까?</span><span class="sxs-lookup"><span data-stu-id="a8eb8-239">How do I do this?</span></span>](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell)

2. <span data-ttu-id="a8eb8-240">다음 명령을 실행 하면 *SupervisoryReview {GUID} @domain onmicrosoft.com* 는 위의 1 단계에서 복사한 주소이 고 *사용자* 는 3 단계에서 감독 사서함에 연결할 검토자의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a8eb8-240">Run the following commands, where  *SupervisoryReview{GUID}@domain.onmicrosoft.com*  is the address you copied in Step 1 above, and  *User*  is the name of the reviewer who will connect to the supervision mailbox in Step 3.</span></span>

    ```Add-MailboxPermission "SupervisoryReview{GUID}@domain.onmicrosoft.com" -User <alias or email address of the account that has reviewer permissions to the supervision mailbox> -AccessRights FullAccess```

    ```Set-Mailbox "<SupervisoryReview{GUID}@domain.onmicrosoft.com>" -HiddenFromAddressListsEnabled: $false```

3. <span data-ttu-id="a8eb8-241">3 단계로 넘어가기 전까지 1 시간 이상 기다립니다.</span><span class="sxs-lookup"><span data-stu-id="a8eb8-241">Wait at least an hour before moving on to Step 3.</span></span>

### <a name="step-3-create-an-outlook-profile-to-connect-to-the-supervision-mailbox"></a><span data-ttu-id="a8eb8-242">3 단계: Outlook 프로필을 만들어 감독 사서함에 연결</span><span class="sxs-lookup"><span data-stu-id="a8eb8-242">Step 3: Create an Outlook profile to connect to the supervision mailbox</span></span>

<span data-ttu-id="a8eb8-243">마지막 단계에서 검토자는 Outlook 프로필을 만들어 감독 사서함에 연결 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8eb8-243">For the final step, reviewers need to create an Outlook profile to connect to the supervision mailbox.</span></span>

> [!NOTE]
> <span data-ttu-id="a8eb8-244">새 Outlook 프로필을 만들려면 Windows 제어판의 메일 설정을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8eb8-244">To create a new Outlook profile, you'll use the Mail settings in the Windows Control Panel.</span></span> <span data-ttu-id="a8eb8-245">이러한 설정에 액세스 하기 위해 수행 하는 경로는 사용 중인 Windows 운영 체제 (Windows 7, Windows 8 또는 Windows 10)와 설치 된 Outlook 버전에 따라 달라질 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a8eb8-245">The path you take to get to these settings might depend on which Windows operating system (Windows 7, Windows 8, or Windows 10) you're using, and which version of Outlook is installed.</span></span>
  
1. <span data-ttu-id="a8eb8-246">제어판을 엽니다.</span><span class="sxs-lookup"><span data-stu-id="a8eb8-246">Open the Control Panel.</span></span> <span data-ttu-id="a8eb8-247">창 위쪽의 **검색** 상자에 **Mail**을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8eb8-247">In the **Search** box at the top of the window, type **Mail**.</span></span><br/><span data-ttu-id="a8eb8-248">(제어판을 표시 하는 방법에 대 한 자세한 내용을 확인 하세요.</span><span class="sxs-lookup"><span data-stu-id="a8eb8-248">(Not sure how to get to the Control Panel?</span></span> <span data-ttu-id="a8eb8-249">[제어판은 무엇 인가요?](https://support.microsoft.com/help/13764/windows-where-is-control-panel)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="a8eb8-249">See [Where is Control Panel?](https://support.microsoft.com/help/13764/windows-where-is-control-panel))</span></span>
  
2. <span data-ttu-id="a8eb8-250">**메일** 앱을 엽니다.</span><span class="sxs-lookup"><span data-stu-id="a8eb8-250">Open the **Mail** app.</span></span>

3. <span data-ttu-id="a8eb8-251">**메일 설정-Outlook**에서 **프로필 보기**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8eb8-251">In **Mail Setup - Outlook**, click **Show Profiles**.</span></span><br/><span data-ttu-id="a8eb8-252">![' 프로필 표시 ' 단추가 강조 표시 된 상태로 ' 메일 설정-Outlook ' 대화 상자](media/28b5dae9-d10c-4f2b-926a-294c857d555c.jpg)</span><span class="sxs-lookup"><span data-stu-id="a8eb8-252">![The 'Mail Setup - Outlook' dialog box with the 'Show Profiles' button highlighted](media/28b5dae9-d10c-4f2b-926a-294c857d555c.jpg)</span></span>
  
4. <span data-ttu-id="a8eb8-253">**메일**에서 **추가**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8eb8-253">In **Mail**, click **Add**.</span></span> <span data-ttu-id="a8eb8-254">그런 다음 **새 프로필**에 감독 사서함의 이름을 입력 합니다 (예: **감독**).</span><span class="sxs-lookup"><span data-stu-id="a8eb8-254">Then, in **New Profile**, enter a name for the supervision mailbox (such as **Supervision**).</span></span><br/><span data-ttu-id="a8eb8-255">![' 프로필 이름 ' 상자에 ' 감독 ' 이름을 표시 하는 ' 새 프로필 ' 대화 상자가 있습니다.](media/d02ae181-b541-4ec6-8f51-698f30033204.jpg)</span><span class="sxs-lookup"><span data-stu-id="a8eb8-255">![The 'New Profile' dialog showing the name 'Supervision' in the 'Profile Name' box](media/d02ae181-b541-4ec6-8f51-698f30033204.jpg)</span></span>
  
5. <span data-ttu-id="a8eb8-256">**Outlook을 Office 365에 연결**에서 **다른 계정에 연결**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8eb8-256">In **Connect Outlook to Office 365**, click **Connect to a different account**.</span></span><br/><span data-ttu-id="a8eb8-257">![' 다른 계정에 연결 ' 링크가 강조 표시 된 ' Outlook과 Office 365 연결 ' 메시지](media/fac49ff8-a7f0-4e82-a271-9ec045a95de1.jpg)</span><span class="sxs-lookup"><span data-stu-id="a8eb8-257">![The 'Connect Outlook to Office 365' message with the 'Connect to a different account' link highlighted](media/fac49ff8-a7f0-4e82-a271-9ec045a95de1.jpg)</span></span>
  
6. <span data-ttu-id="a8eb8-258">**자동 계정 설정**에서 **수동 설치 또는 추가 서버 유형을**선택 하 고 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8eb8-258">In **Auto Account Setup**, choose **Manual setup or additional server types**, and then click **Next**.</span></span>

7. <span data-ttu-id="a8eb8-259">**계정 유형 선택**에서 **Office 365**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8eb8-259">In **Choose Your Account Type**, choose **Office 365**.</span></span> <span data-ttu-id="a8eb8-260">그런 다음 **전자 메일 주소** 상자에 이전에 복사한 감독 사서함의 주소를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8eb8-260">Then, in the **Email Address** box, enter the address of the supervision mailbox you copied previously.</span></span><br/><span data-ttu-id="a8eb8-261">![' 전자 메일 주소 ' 확인란이 강조 표시 된 Outlook의 ' 계정 추가 ' 대화 상자에서 ' 계정 유형 선택 ' 페이지입니다.](media/4f601236-9f69-4cf6-a58c-0b91204aa8cb.jpg)</span><span class="sxs-lookup"><span data-stu-id="a8eb8-261">![The 'Choose Your Account Type' page of the 'Add Account' dialog in Outlook showing the 'Email Address' box highlighted.](media/4f601236-9f69-4cf6-a58c-0b91204aa8cb.jpg)</span></span>
  
8. <span data-ttu-id="a8eb8-262">메시지가 나타나면 Office 365 자격 증명을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8eb8-262">When prompted, enter your Office 365 credentials.</span></span>

9. <span data-ttu-id="a8eb8-263">성공 하면 \*\*감독 — \<정책 이름\> \*\* 폴더가 Outlook의 폴더 목록 보기에 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a8eb8-263">If successful, the **Supervision — \<policy name\>** folder is listed in the Folder List view in Outlook.</span></span>

## <a name="powershell-reference"></a><span data-ttu-id="a8eb8-264">PowerShell 참조</span><span class="sxs-lookup"><span data-stu-id="a8eb8-264">PowerShell reference</span></span>

<span data-ttu-id="a8eb8-265">필요한 경우 다음 PowerShell cmdlet을 사용 하 여 감독 정책을 만들고 관리할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a8eb8-265">If needed, you can create and manage supervision policies with the following PowerShell cmdlets:</span></span>

- [<span data-ttu-id="a8eb8-266">Remove-supervisoryreviewpolicyv2</span><span class="sxs-lookup"><span data-stu-id="a8eb8-266">New-SupervisoryReviewPolicyV2</span></span>](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance/new-supervisoryreviewpolicyv2?view=exchange-ps)
- [<span data-ttu-id="a8eb8-267">Remove-supervisoryreviewpolicyv2</span><span class="sxs-lookup"><span data-stu-id="a8eb8-267">Get-SupervisoryReviewPolicyV2</span></span>](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance/get-supervisoryreviewpolicyv2?view=exchange-ps)
- [<span data-ttu-id="a8eb8-268">Remove-supervisoryreviewpolicyv2</span><span class="sxs-lookup"><span data-stu-id="a8eb8-268">Set-SupervisoryReviewPolicyV2</span></span>](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance/set-supervisoryreviewpolicyv2?view=exchange-ps)
- [<span data-ttu-id="a8eb8-269">Remove-supervisoryreviewpolicyv2을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8eb8-269">Remove-SupervisoryReviewPolicyV2</span></span>](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance/remove-supervisoryreviewpolicyv2?view=exchange-ps)
- [<span data-ttu-id="a8eb8-270">Set-supervisoryreviewrule</span><span class="sxs-lookup"><span data-stu-id="a8eb8-270">New-SupervisoryReviewRule</span></span>](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance/new-supervisoryreviewrule?view=exchange-ps)
- [<span data-ttu-id="a8eb8-271">Set-supervisoryreviewrule</span><span class="sxs-lookup"><span data-stu-id="a8eb8-271">Set-SupervisoryReviewRule</span></span>](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance/set-supervisoryreviewrule?view=exchange-ps)
- [<span data-ttu-id="a8eb8-272">SupervisoryReviewActivity</span><span class="sxs-lookup"><span data-stu-id="a8eb8-272">Get-SupervisoryReviewActivity</span></span>](https://docs.microsoft.com/powershell/module/exchange/reporting/get-supervisoryreviewactivity)
- [<span data-ttu-id="a8eb8-273">SupervisoryReviewOverallProgressReport</span><span class="sxs-lookup"><span data-stu-id="a8eb8-273">Get-SupervisoryReviewOverallProgressReport</span></span>](https://docs.microsoft.com/powershell/module/exchange/reporting/get-supervisoryreviewoverallprogressreport)
- [<span data-ttu-id="a8eb8-274">SupervisoryReviewTopCasesReport</span><span class="sxs-lookup"><span data-stu-id="a8eb8-274">Get-SupervisoryReviewTopCasesReport</span></span>](https://docs.microsoft.com/powershell/module/exchange/reporting/get-supervisoryreviewtopcasesreport)
