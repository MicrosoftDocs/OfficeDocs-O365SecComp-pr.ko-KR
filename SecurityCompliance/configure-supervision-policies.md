---
title: 조직의 감독 정책 구성
ms.author: robmazz
author: robmazz
manager: laurawi
ms.audience: Admin
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
ms.assetid: d14ae7c3-fcb0-4a03-967b-cbed861bb086
description: 검토할 직원 정보를 캡처하기 위해 관리 검토 정책을 설정 합니다.
ms.openlocfilehash: af317194fcf551acde8c53cdf6aa38bfb040dc84
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30216738"
---
# <a name="configure-supervision-policies-for-your-organization"></a><span data-ttu-id="28ff3-103">조직의 감독 정책 구성</span><span class="sxs-lookup"><span data-stu-id="28ff3-103">Configure supervision policies for your organization</span></span>

<span data-ttu-id="28ff3-p101">감독 정책을 사용 하 여 내부 또는 외부 검토자가 검사할 직원 통신을 캡처할 수 있습니다. 감독 정책을 통해 조직의 통신을 모니터링 하는 방법에 대 한 자세한 내용은 [Office 365의 감독 정책을](supervision-policies.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="28ff3-p101">Use supervision policies to capture employee communications for examination by internal or external reviewers. For more information about how supervision policies can help you monitor communications in your organization, see [Supervision policies in Office 365](supervision-policies.md).</span></span>

> [!NOTE]
> <span data-ttu-id="28ff3-p102">감독 정책에 따라 모니터링 되는 사용자에 게는 고급 준수 추가 기능이 포함 된 office 365 Enterprise E3 라이선스가 있거나 office 365 enterprise E5 구독에 포함 되어 있어야 합니다. 기존 Enterprise e5 요금제가 없고, 감독을 려 고 하는 경우 [Office 365 Enterprise e 5의 평가판에 등록할](https://go.microsoft.com/fwlink/p/?LinkID=698279)수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="28ff3-p102">Users monitored by supervision policies must have either an Office 365 Enterprise E3 license with the Advanced Compliance add-on or be included in an Office 365 Enterprise E5 subscription. If you don't have an existing Enterprise E5 plan and want to try supervision, you can [sign up for a trial of Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span></span>
  
<span data-ttu-id="28ff3-108">Office 365 조직에서 감독을 설정 및 사용 하려면 다음 단계를 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="28ff3-108">Follow these steps to set up and use supervision in your Office 365 organization:</span></span>
  
- <span data-ttu-id="28ff3-109">**1 단계 (선택 사항)** - [감독을 위한 그룹 설정](configure-supervision-policies.md#exampledist)</span><span class="sxs-lookup"><span data-stu-id="28ff3-109">**Step 1 (optional)** - [Set up groups for Supervision](configure-supervision-policies.md#exampledist)</span></span>

    <span data-ttu-id="28ff3-p103">감독 사용을 시작 하기 전에 의사 소통을 검토 하 고 이러한 검토를 수행할 사용자를 결정 합니다. 소수의 사용자만을 시작 하 여 감독의 작동 방식을 확인 하려는 경우 지금 그룹 설정 건너뛰기를 건너뛸 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="28ff3-p103">Before you start using supervision, determine who will have their communications reviewed and who will perform those reviews. If you want to get started with just a few users to see how supervision works, you can skip setting up groups for now.</span></span>

- <span data-ttu-id="28ff3-112">**2 단계 (필수)** - [조직에서 감독을 사용할 수 있도록 설정](configure-supervision-policies.md#MakeAvailable)</span><span class="sxs-lookup"><span data-stu-id="28ff3-112">**Step 2 (required)** - [Make supervision available in your organization](configure-supervision-policies.md#MakeAvailable)</span></span>

    <span data-ttu-id="28ff3-p104">정책을 설정할 수 있도록 자신을 관리 검토 역할 그룹에 추가 합니다. 이 역할이 할당 된 모든 사용자는 보안 & 준수 센터의 **데이터 거 버 넌 스** 에 있는 **감독** 페이지에 액세스할 수 있습니다. 검토할 전자 메일이 exchange online에서 호스트 되는 경우 각 검토자에 [게 exchange online에 대 한 원격 PowerShell 액세스](https://docs.microsoft.com/powershell/exchange/exchange-online/disable-access-to-exchange-online-powershell)권한도 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="28ff3-p104">Add yourself to the Supervisory Review role group so you can set up policies. Anyone who has this role assigned can access the **Supervision** page under **Data Governance** in the Security & Compliance Center. If email to be reviewed is hosted on Exchange Online, each reviewer must also have [remote PowerShell access to Exchange Online](https://docs.microsoft.com/powershell/exchange/exchange-online/disable-access-to-exchange-online-powershell).</span></span>

- <span data-ttu-id="28ff3-116">**3 단계 (선택 사항)** - [사용자 지정 중요 한 정보 유형 또는 사용자 지정 키워드 사전/lexicons 구성](configure-supervision-policies.md#sensitiveinfo)</span><span class="sxs-lookup"><span data-stu-id="28ff3-116">**Step 3 (optional)** - [Configure custom sensitive information types or custom keyword dictionaries/lexicons](configure-supervision-policies.md#sensitiveinfo)</span></span>

    <span data-ttu-id="28ff3-117">감독 정책에 대 한 사용자 지정 중요 한 정보 유형 또는 사용자 지정 키워드 사전을 사용 해야 하는 경우에는 감독 마법사를 시작 하기 전에 만들어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="28ff3-117">If you need to use a custom sensitive info type or a custom keyword dictionary for your supervision policy, you'll need to create it before starting the supervision wizard.</span></span>

- <span data-ttu-id="28ff3-118">**4 단계 (필수)** - [감독 정책 설정](configure-supervision-policies.md#setupsuper)</span><span class="sxs-lookup"><span data-stu-id="28ff3-118">**Step 4 (required)** - [Set up a supervision policy](configure-supervision-policies.md#setupsuper)</span></span>

    <span data-ttu-id="28ff3-p105">보안 & 준수 센터에서 감독 정책을 만듭니다. 이러한 정책은 조직에서 검토할 대상이 되는 통신을 정의 하 고 검토를 수행할 사용자를 지정 합니다. 통신에는 전자 메일 및 Microsoft 팀 통신과 타사 플랫폼 통신 (예: Facebook, Twitter 등)이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="28ff3-p105">You'll create supervision policies in the Security & Compliance Center. These policies define which communications are subject to review in your organization and specifies who should perform reviews. Communications include email and Microsoft Teams communications, as well as 3rd-party platform communications (such as Facebook, Twitter, etc.)</span></span>

- <span data-ttu-id="28ff3-122">**5 단계-(선택 사항)** [새 감독 정책 테스트](configure-supervision-policies.md#TestPolicy)</span><span class="sxs-lookup"><span data-stu-id="28ff3-122">**Step 5 - (optional)** [Test your new supervision policy](configure-supervision-policies.md#TestPolicy)</span></span>

    <span data-ttu-id="28ff3-123">규정 준수 전략이 표준을 충족 하는지 확인 하는 것이 중요 한 역할을 하는 경우에는 감독 정책이 필요에 따라 작동 하도록 테스트 합니다.</span><span class="sxs-lookup"><span data-stu-id="28ff3-123">Testing your supervision policy to make sure it is functioning as desired is an important part of ensuring that your compliance strategy is meeting your standards.</span></span>

- <span data-ttu-id="28ff3-124">**6 단계-(선택 사항)** [outlook 추가 기능을 설정 하 여 Office 365 감독 대시보드 또는 웹용 outlook (이전의 outlook web App)을 사용 하지 않으려는 경우 감독 된 통신을 검토 합니다](configure-supervision-policies.md#UseOutlook) .</span><span class="sxs-lookup"><span data-stu-id="28ff3-124">**Step 6 - (optional)** [Set up Outlook add-in for reviewers who do not want to use Office 365 supervision dashboard or Outlook on the web (formerly known as Outlook Web App) to review supervised communications](configure-supervision-policies.md#UseOutlook)</span></span>

    <span data-ttu-id="28ff3-125">outlook의 감독 추가 기능은 검토자가 outlook 클라이언트 내에서 감독 기능에 액세스 하 여 각 항목을 평가 하 고 분류할 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="28ff3-125">The Supervision add-in for Outlook gives reviewers access to the supervision functionality right within the Outlook client so they can assess and categorize each item.</span></span>

<span data-ttu-id="28ff3-126"><a name="exampledist"> </a></span><span class="sxs-lookup"><span data-stu-id="28ff3-126"></span></span>

## <a name="step-1---set-up-groups-for-supervision-optional"></a><span data-ttu-id="28ff3-127">1 단계-감독에 대 한 그룹 설정 (선택 사항)</span><span class="sxs-lookup"><span data-stu-id="28ff3-127">Step 1 - Set up groups for Supervision (optional)</span></span>

 <span data-ttu-id="28ff3-p106">감독 정책을 만들 때 의사 소통을 검토 하 고 이러한 검토를 수행할 사용자를 결정 합니다. 정책에서는 전자 메일 주소를 사용 하 여 개인 이나 사용자 그룹을 식별 합니다. 설정을 단순화 하기 위해 통신을 검토 하 고 해당 통신을 검토할 사용자에 대 한 그룹을 확인할 사용자에 대 한 그룹을 만듭니다. 그룹을 사용 하는 경우에는 서로 다른 두 그룹 간의 통신을 모니터링 하려는 경우 또는 감독 하지 않을 그룹을 지정 하려는 경우에는 여러 가지 사항이 필요할 수도 있습니다. 이 작업 방법에 대 한 자세한 내용은 [예제 메일 그룹](configure-supervision-policies.md#GroupExample) 을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="28ff3-p106">When you create a supervision policy, you'll determine who will have their communications reviewed and who will perform those reviews. In the policy, you'll use email addresses to identify individuals or groups of people. To simplify your setup, create groups for people who will have their communication reviewed and groups for people who will review those communications. If you're using groups, you might need several—for example, if you want to monitor communications between two distinct groups of people, or if you want to specify a group that isn't going to be supervised. See [Example distribution groups](configure-supervision-policies.md#GroupExample) for details about how this works.</span></span>
  
<span data-ttu-id="28ff3-p107">조직의 그룹 간 또는 사이에서 통신을 감독할 Exchange 관리 센터에서 메일 그룹을 설정 합니다 ( **받는 사람** \> **그룹**으로 이동). 메일 그룹을 설정 하는 방법에 대 한 자세한 내용은 [메일 그룹 관리](http://go.microsoft.com/fwlink/?LinkId=613635) 를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="28ff3-p107">To supervise communications between or within groups in your organization, set up distribution groups in the Exchange admin center (go to **recipients** \> **groups**). For more information about setting up distribution groups, see [Manage distribution groups](http://go.microsoft.com/fwlink/?LinkId=613635)</span></span>
  
> [!NOTE]
> <span data-ttu-id="28ff3-p108">원하는 경우 동적 메일 그룹 또는 보안 그룹을 감독에 사용할 수도 있습니다. 조직의 요구 사항에 적합 한지 여부를 결정 하는 데 도움이 되도록 [메일 사용이 가능한 보안 그룹 관리](http://go.microsoft.com/fwlink/?LinkId=627033)및 [동적 메일 그룹 관리](http://go.microsoft.com/fwlink/?LinkId=627058)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="28ff3-p108">You can also use dynamic distribution groups or security groups for supervision if you prefer. To help you decide if these better fit your organization needs, see [Manage mail-enabled security groups](http://go.microsoft.com/fwlink/?LinkId=627033), and [Manage dynamic distribution groups](http://go.microsoft.com/fwlink/?LinkId=627058).</span></span>
  
<span data-ttu-id="28ff3-137"><a name="GroupExample"> </a></span><span class="sxs-lookup"><span data-stu-id="28ff3-137"></span></span>

### <a name="example-distribution-groups"></a><span data-ttu-id="28ff3-138">예시 메일 그룹</span><span class="sxs-lookup"><span data-stu-id="28ff3-138">Example distribution groups</span></span>

<span data-ttu-id="28ff3-139">이 예에는 Contoso 재무 국제 지역 이라는 금융 조직에 대해 설정 된 메일 그룹이 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="28ff3-139">This example includes a distribution group that has been set up for a financial organization called Contoso Financial International.</span></span>
  
<span data-ttu-id="28ff3-p109">Contoso Financial International에서 미국에 있는 중개인 간 통신 샘플링을 감독해야 합니다. 하지만 해당 그룹 내에 있는 준수 관리자는 감독이 필요하지 않습니다. 이 예에서는 다음 그룹을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="28ff3-p109">In Contoso Financial International, a sampling of communications between brokers in the United States must be supervised. However, compliance officers within that group do not require supervision. For this example, we can create the following groups:</span></span>
  
|<span data-ttu-id="28ff3-143">**이 메일 그룹 설정**</span><span class="sxs-lookup"><span data-stu-id="28ff3-143">**Set up this distribution group**</span></span>|<span data-ttu-id="28ff3-144">**그룹 주소(별칭)**</span><span class="sxs-lookup"><span data-stu-id="28ff3-144">**Group address (alias)**</span></span>|<span data-ttu-id="28ff3-145">**설명**</span><span class="sxs-lookup"><span data-stu-id="28ff3-145">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="28ff3-146">모든 미국 중개인</span><span class="sxs-lookup"><span data-stu-id="28ff3-146">All US brokers</span></span> | <span data-ttu-id="28ff3-147">US_Brokers@Contoso.com</span><span class="sxs-lookup"><span data-stu-id="28ff3-147">US_Brokers@Contoso.com</span></span> | <span data-ttu-id="28ff3-148">이 그룹에는 Contoso에서 근무하는 모든 미국 중개인에 대한 전자 메일 주소가 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="28ff3-148">This group includes email addresses for all US-based brokers who work for Contoso.</span></span> |
| <span data-ttu-id="28ff3-149">모든 미국 준수 관리자</span><span class="sxs-lookup"><span data-stu-id="28ff3-149">All US compliance officers</span></span> | <span data-ttu-id="28ff3-150">US_Compliance@Contoso.com</span><span class="sxs-lookup"><span data-stu-id="28ff3-150">US_Compliance@Contoso.com</span></span>  | <span data-ttu-id="28ff3-p110">이 그룹에는 Contoso에서 근무 하는 모든 미국 기반 규정 준수 관리자의 전자 메일 주소가 포함 됩니다. 이 그룹은 모든 미국 기반 브로커의 하위 집합 이므로이 별칭을 사용 하 여 감독 정책에서 규정 준수 관리자를 제외할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="28ff3-p110">This group includes email addresses for all US-based compliance officers who work for Contoso. Because this group is a subset of all US-based brokers, you can use this alias to exempt compliance officers from a supervision policy.</span></span> |
  
<span data-ttu-id="28ff3-153"><a name="MakeAvailable"> </a></span><span class="sxs-lookup"><span data-stu-id="28ff3-153"></span></span>

## <a name="step-2---make-supervision-available-in-your-organization-required"></a><span data-ttu-id="28ff3-154">2 단계-조직에서 감독을 사용할 수 있도록 설정 (필수)</span><span class="sxs-lookup"><span data-stu-id="28ff3-154">Step 2 - Make supervision available in your organization (required)</span></span>

<span data-ttu-id="28ff3-155">보안 & 준수 센터에서 **감독** 을 메뉴 옵션으로 사용 하도록 설정 하려면 관리 검토 관리자 역할이 할당 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="28ff3-155">To make **Supervision** available as a menu option in the Security & Compliance Center, you must be assigned the Supervisory Review Administrator role.</span></span>
  
<span data-ttu-id="28ff3-156">이렇게 하려면 자신을 관리 검토 역할 그룹의 구성원으로 추가 하거나 새 역할 그룹을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="28ff3-156">To do this, you can either add yourself as a member of the Supervisory Review role group, or you can create a new role group.</span></span>
  
### <a name="add-members-to-the-supervisory-review-role-group"></a><span data-ttu-id="28ff3-157">관리 검토 역할 그룹에 구성원 추가</span><span class="sxs-lookup"><span data-stu-id="28ff3-157">Add members to the Supervisory Review role group</span></span>

1. <span data-ttu-id="28ff3-158">Office 365 [https://protection.office.com](https://protection.office.com) 조직의 관리자 계정에 대 한 자격 증명을 사용 하 여 로그인 합니다.</span><span class="sxs-lookup"><span data-stu-id="28ff3-158">Sign into [https://protection.office.com](https://protection.office.com) using credentials for an admin account in your Office 365 organization.</span></span>

2. <span data-ttu-id="28ff3-159">보안 & 준수 센터에서 **사용 권한**으로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="28ff3-159">In the Security & Compliance Center, go to **Permissions**.</span></span>

3. <span data-ttu-id="28ff3-160">**관리 검토** 역할 그룹을 선택한 다음 편집 아이콘을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="28ff3-160">Select the **Supervisory Review** role group and then click the Edit icon.</span></span>

4. <span data-ttu-id="28ff3-161">**구성원** 섹션에서 조직에 대 한 감독을 관리 하려는 사용자를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="28ff3-161">In the **Members** section, add the people who you want to manage supervision for your organization.</span></span>

### <a name="create-a-new-role-group"></a><span data-ttu-id="28ff3-162">새 역할 그룹 만들기</span><span class="sxs-lookup"><span data-stu-id="28ff3-162">Create a new role group</span></span>

1. <span data-ttu-id="28ff3-163">Office 365 [https://protection.office.com](https://protection.office.com) 조직의 관리자 계정에 대 한 자격 증명을 사용 하 여 로그인 합니다.</span><span class="sxs-lookup"><span data-stu-id="28ff3-163">Sign into [https://protection.office.com](https://protection.office.com) using credentials for an admin account in your Office 365 organization.</span></span>

2. <span data-ttu-id="28ff3-164">보안 & 준수 센터에서 **사용 권한** 으로 이동한 다음 추가 (**+**)를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="28ff3-164">In the Security & Compliance Center, go to **Permissions** and then click Add (**+**).</span></span>

3. <span data-ttu-id="28ff3-p111">**역할** 섹션에서 추가 (**+**)를 클릭 하 고 아래로 스크롤하여 **관리 검토 관리자**를 선택 합니다. 이 역할을 역할 그룹에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="28ff3-p111">In the **Roles** section, click Add (**+**) and scroll down to **Supervisory Review Administrator**. Add this role to the role group.</span></span>

4. <span data-ttu-id="28ff3-167">**구성원** 섹션에서 조직에 대 한 감독을 관리 하려는 사용자를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="28ff3-167">In the **Members** section, add the people who you want to manage supervision for your organization.</span></span>

<span data-ttu-id="28ff3-168">역할 그룹 및 사용 권한에 대 한 자세한 내용은 [Office 365 보안 &amp; 및 준수 센터의 사용 권한을](permissions-in-the-security-and-compliance-center.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="28ff3-168">For more information about role groups and permissions, see [Permissions in the Office 365 Security &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md).</span></span>

### <a name="enable-remote-powershell-access-for-reviewers-if-email-is-hosted-on-exchange-online"></a><span data-ttu-id="28ff3-169">검토자에 대해 원격 PowerShell 액세스 사용 (전자 메일이 Exchange Online에서 호스트 되는 경우)</span><span class="sxs-lookup"><span data-stu-id="28ff3-169">Enable remote PowerShell access for reviewers (if email is hosted on Exchange Online)</span></span>

1. <span data-ttu-id="28ff3-170">[사용 또는 사용 안 함 Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/disable-access-to-exchange-online-powershell)에 대 한 지침을 따릅니다.</span><span class="sxs-lookup"><span data-stu-id="28ff3-170">Follow the guidance in [Enable or disable access to Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/disable-access-to-exchange-online-powershell).</span></span>

<span data-ttu-id="28ff3-171"><a name="sensitiveinfo"> </a></span><span class="sxs-lookup"><span data-stu-id="28ff3-171"></span></span>
  
## <a name="step-3---create-custom-sensitive-information-types-or-custom-keyword-dictionaries-optional"></a><span data-ttu-id="28ff3-172">3 단계-사용자 지정 중요 한 정보 유형 또는 사용자 지정 키워드 사전 만들기 (선택 사항)</span><span class="sxs-lookup"><span data-stu-id="28ff3-172">Step 3 - Create custom sensitive information types or custom keyword dictionaries (optional)</span></span>

<span data-ttu-id="28ff3-173">감독 정책 마법사에서 기존 사용자 지정 중요 한 정보 유형 또는 사용자 지정 키워드 사전을 선택 하려면 먼저 필요한 경우 이러한 항목을 만들어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="28ff3-173">In order to pick from existing custom sensitive information types or custom keyword dictionaries in the supervision policy wizard, you first need to create these items if needed.</span></span>

### <a name="create-custom-sensitive-information-types"></a><span data-ttu-id="28ff3-174">사용자 지정 중요 한 정보 유형 만들기</span><span class="sxs-lookup"><span data-stu-id="28ff3-174">Create custom sensitive information types</span></span>

1. <span data-ttu-id="28ff3-p112">Office 365 Security & 준수 센터에서 새 중요 한 정보 유형을 만듭니다. **중요 한 정보** 유형 **분류** \> 로 이동 하 여 **새 중요 한 정보 유형 마법사**의 단계를 따릅니다. 여기에서 다음을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="28ff3-p112">Create a new sensitive information type in the Office 365 Security & Compliance Center. Navigate to **Classifications** \> **Sensitive info types** and follow the steps in the **New sensitive info type wizard**. Here you will:</span></span>

    - <span data-ttu-id="28ff3-178">중요 한 정보 유형에 대 한 이름 및 설명 정의</span><span class="sxs-lookup"><span data-stu-id="28ff3-178">Define a name and description for the sensitive info type</span></span>
    - <span data-ttu-id="28ff3-179">근접성, 신뢰 수준 및 주 패턴 요소 정의</span><span class="sxs-lookup"><span data-stu-id="28ff3-179">Define the proximity, confidence level, and primary pattern elements</span></span>
    - <span data-ttu-id="28ff3-180">선택 항목 검토 및 중요 한 정보 유형 만들기</span><span class="sxs-lookup"><span data-stu-id="28ff3-180">Review your selections and create the sensitive info type</span></span>

    <span data-ttu-id="28ff3-181">자세한 내용은 [사용자 지정 중요 한 정보 유형 만들기](create-a-custom-sensitive-information-type.md)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="28ff3-181">For more detailed information, see [Create a custom sensitive information type](create-a-custom-sensitive-information-type.md).</span></span>

### <a name="create-custom-keyword-dictionarylexicon"></a><span data-ttu-id="28ff3-182">사용자 지정 키워드 사전/어휘 만들기</span><span class="sxs-lookup"><span data-stu-id="28ff3-182">Create custom keyword dictionary/lexicon</span></span>

1. <span data-ttu-id="28ff3-p113">메모장과 같은 텍스트 편집기를 사용 하 여 감독 정책에서 모니터링할 키워드 용어를 포함 하는 새 파일을 만듭니다. 각 용어가 별도의 줄에 있는지 확인 하 고 파일을 **유니코드/u t f-16 (꼬마)** 형식으로 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="28ff3-p113">Using a text editor (like Notepad), create a new file that includes the keyword terms you'd like to monitor in a supervision policy. Make sure each term is on a separate line and save the file in the **Unicode/UTF-16 (Little Endian)** format.</span></span>
2. <span data-ttu-id="28ff3-p114">PowerShell을 사용 하 여 Office 365 테 넌 트에 키워드 파일을 가져옵니다. PowerShell을 사용 하 여 office 365에 연결 하려면 [connect to office 365 Security & 준수 센터 PowerShell](https://docs.microsoft.com/powershell/exchange/office-365-scc/connect-to-scc-powershell/connect-to-scc-powershell)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="28ff3-p114">Import the keyword file into your Office 365 tenant using PowerShell. To connect to Office 365 with PowerShell, see [Connect to Office 365 Security & Compliance Center PowerShell](https://docs.microsoft.com/powershell/exchange/office-365-scc/connect-to-scc-powershell/connect-to-scc-powershell).</span></span>

    <span data-ttu-id="28ff3-187">PowerShell을 사용 하 여 Office 365에 연결한 후에 키워드 사전을 가져오려면 다음 명령을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="28ff3-187">After you've connected to Office 365 with PowerShell, run the following commands to import your keyword dictionary:</span></span>

    ```
    $fileData = Get-Content "your keyword path and file name" -Encoding Byte -ReadCount 0

    New-DlpKeywordDictionary -Name "Name for your keyword dictionary" -Description "optional description for your keyword dictionary" -FileData $fileData
    ```
    <span data-ttu-id="28ff3-188">자세한 내용은 [Create a keyword dictionary](create-a-keyword-dictionary.md)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="28ff3-188">For more detailed information, see [Create a keyword dictionary](create-a-keyword-dictionary.md).</span></span>

3. <span data-ttu-id="28ff3-p115">Office 365 Security & 준수 센터에서 새 중요 한 정보 유형을 만듭니다. **중요 한 정보** 유형 **분류** \> 로 이동 하 여 **새 중요 한 정보 유형 마법사**의 단계를 따릅니다. 여기에서 다음을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="28ff3-p115">Create a new sensitive information type in the Office 365 Security & Compliance Center. Navigate to **Classifications** \> **Sensitive info types** and follow the steps in the **New sensitive info type wizard**. Here you will:</span></span>

    - <span data-ttu-id="28ff3-192">중요 한 정보 유형에 대 한 이름 및 설명 정의</span><span class="sxs-lookup"><span data-stu-id="28ff3-192">Define a name and description for the sensitive info type</span></span>
    - <span data-ttu-id="28ff3-193">일치 요소에 대 한 요구 사항으로 사용자 지정 사전 추가</span><span class="sxs-lookup"><span data-stu-id="28ff3-193">Add your custom dictionary as a requirement for the matching element</span></span>
    - <span data-ttu-id="28ff3-194">선택 항목 검토 및 중요 한 정보 유형 만들기</span><span class="sxs-lookup"><span data-stu-id="28ff3-194">Review your selections and create the sensitive info type</span></span>

    <span data-ttu-id="28ff3-195">사용자 지정 사전/어휘를 만든 후에는 [DlpKeywordDictionary](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-dlp/get-dlpkeyworddictionary) cmdlet을 사용 하 여 구성 된 키워드를 보거나 [DlpKeywordDictionary](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-dlp/set-dlpkeyworddictionary) cmdlet을 사용 하 여 용어를 추가 및 제거할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="28ff3-195">After the custom dictionary/lexicon is created, you can view the configured keywords using the [Get-DlpKeywordDictionary](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-dlp/get-dlpkeyworddictionary) cmdlet or add and remove terms using the [Set-DlpKeywordDictionary](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-dlp/set-dlpkeyworddictionary) cmdlet.</span></span>

    <span data-ttu-id="28ff3-196">자세한 내용은 [사용자 지정 중요 한 정보 유형 만들기](create-a-custom-sensitive-information-type.md)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="28ff3-196">For more detailed information, see [Create a custom sensitive information type](create-a-custom-sensitive-information-type.md).</span></span>

<span data-ttu-id="28ff3-197"><a name="setupsuper"> </a></span><span class="sxs-lookup"><span data-stu-id="28ff3-197"></span></span>

## <a name="step-4---set-up-a-supervision-policy-required"></a><span data-ttu-id="28ff3-198">4 단계-감독 정책 설정 (필수)</span><span class="sxs-lookup"><span data-stu-id="28ff3-198">Step 4 - Set up a supervision policy (required)</span></span>
  
1. <span data-ttu-id="28ff3-199">Office 365 [https://protection.office.com](https://protection.office.com) 조직의 관리자 계정에 대 한 자격 증명을 사용 하 여 로그인 합니다.</span><span class="sxs-lookup"><span data-stu-id="28ff3-199">Sign into [https://protection.office.com](https://protection.office.com) using credentials for an admin account in your Office 365 organization.</span></span>

2. <span data-ttu-id="28ff3-200">보안 & 준수 센터에서 **감독**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="28ff3-200">In the Security & Compliance Center, select **Supervision**.</span></span>
  
3. <span data-ttu-id="28ff3-p116">**만들기** 를 선택 하 고 마법사의 지시에 따라 다음과 같은 정책 페이지를 설정 합니다. 마법사를 사용 하 여 다음을 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="28ff3-p116">Select **Create** and then follow the wizard to set up the following pages of the policy. Using the wizard, you will:</span></span>

    - <span data-ttu-id="28ff3-203">정책에 이름과 설명을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="28ff3-203">Give the policy a name and description.</span></span>
    - <span data-ttu-id="28ff3-204">제외할 사용자 또는 그룹 선택을 비롯 하 여 감독할 사용자 또는 그룹을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="28ff3-204">Choose the users or groups to supervise, including choosing users or groups you'd like to exclude.</span></span>
    - <span data-ttu-id="28ff3-205">감독 정책 조건을 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="28ff3-205">Define the supervision policy conditions.</span></span>
    - <span data-ttu-id="28ff3-p117">중요 한 정보 유형을 포함 하 고 싶은 경우 선택 합니다. 여기에서 기본 및 사용자 지정 중요 한 정보 유형을 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="28ff3-p117">Choose if you'd like to include sensitive information types. This is where you can select default and custom sensitive info types.</span></span>
    - <span data-ttu-id="28ff3-208">검토할 통신의 비율을 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="28ff3-208">Define the percentage of communications to review.</span></span>
    - <span data-ttu-id="28ff3-p118">정책에 대 한 검토자를 선택 합니다. 검토자는 개별 사용자 또는 [메일 사용이 가능한 보안 그룹이](https://docs.microsoft.com/Exchange/recipients-in-exchange-online/manage-mail-enabled-security-groups#create-a-mail-enabled-security-group)될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="28ff3-p118">Choose the reviewers for the policy. Reviewers can be individual users or [mail-enabled security groups](https://docs.microsoft.com/Exchange/recipients-in-exchange-online/manage-mail-enabled-security-groups#create-a-mail-enabled-security-group).</span></span>
    - <span data-ttu-id="28ff3-211">정책 선택을 검토 하 고 정책을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="28ff3-211">Review your policy selections and create the policy.</span></span>

<span data-ttu-id="28ff3-212"><a name="TestPolicy"> </a></span><span class="sxs-lookup"><span data-stu-id="28ff3-212"></span></span>

## <a name="step-5---test-your-supervision-policy-optional"></a><span data-ttu-id="28ff3-213">5 단계-감독 정책 테스트 (선택 사항)</span><span class="sxs-lookup"><span data-stu-id="28ff3-213">Step 5 - Test your supervision policy (optional)</span></span>

<span data-ttu-id="28ff3-p119">감독 정책을 만든 후에는 테스트를 통해 정의한 조건이 정책에 의해 적절 하 게 적용 되는지 확인 하는 것이 좋습니다. 또한 감독 정책에 중요 한 정보 유형이 포함 되어 있는 경우 [DLP (데이터 손실 방지) 정책을 테스트할](create-test-tune-dlp-policy.md) 수도 있습니다. 다음 단계에 따라 감독 정책을 테스트 합니다.</span><span class="sxs-lookup"><span data-stu-id="28ff3-p119">After you create a supervision policy, it's a good idea to test to make sure that the conditions you defined are being properly enforced by the policy. You may also want to [test your data loss prevention (DLP) policies](create-test-tune-dlp-policy.md) if your supervision policies include sensitive information types. Follow the steps below to test your supervision policy:</span></span>

1. <span data-ttu-id="28ff3-217">테스트할 정책에 정의 된 감독 된 사용자로 로그인 한 전자 메일 클라이언트 또는 Microsoft 팀을 엽니다.</span><span class="sxs-lookup"><span data-stu-id="28ff3-217">Open an email client or Microsoft Teams logged in as a supervised user defined in the policy you want to test.</span></span>
2. <span data-ttu-id="28ff3-p120">감독 정책에 정의한 기준을 충족 하는 전자 메일 또는 Microsoft 팀 채팅을 보냅니다. 키워드, 첨부 파일 크기, 도메인 등이 될 수 있습니다. 정책에서 구성 된 조건부 설정이 너무 제한적 이거나 너무 lenient 인지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="28ff3-p120">Send an email or Microsoft Teams chat that meets the criteria you've defined in the supervision policy. This can be a keyword, attachment size, domain, etc. Make sure you determine if your configured conditional settings in the policy is too restrictive or too lenient.</span></span>

    > [!Note]
    > <span data-ttu-id="28ff3-p121">정의 된 정책이 적용 되는 전자 메일은 거의 실시간으로 처리 되며 정책이 구성 된 직후에 테스트할 수 있습니다. Microsoft 팀의 채팅에는 정책에서 전체 프로세스를 수행 하는 데 최대 24 시간이 걸릴 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="28ff3-p121">Emails subject to defined policies are processed in near real-time and can be tested immediately after the policy is configured. Chats in Microsoft Teams can take up to 24 hours to fully process in a policy.</span></span> 

3. <span data-ttu-id="28ff3-p122">감독 정책에 지정 된 검토자로 Office 365 테 넌 트에 로그인 합니다. *사용자 지정 정책이* > **열려** 있는 **감독** > 을 탐색 하 여 정책에 대 한 보고서를 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="28ff3-p122">Log into your Office 365 tenant as a reviewer designated in the supervision policy. Navigate to **Supervision** > *Your Custom Policy* > **Open** to view the report for the policy.</span></span>

<span data-ttu-id="28ff3-224"><a name="UseOutlook"> </a></span><span class="sxs-lookup"><span data-stu-id="28ff3-224"></span></span>

## <a name="step-6---set-up-outlook-add-in-for-reviewers-optional"></a><span data-ttu-id="28ff3-225">6 단계-검토자 용 Outlook 추가 기능 설정 (선택 사항)</span><span class="sxs-lookup"><span data-stu-id="28ff3-225">Step 6 - Set up Outlook add-in for reviewers (optional)</span></span>

<span data-ttu-id="28ff3-226">통신을 검토 하기 위해 Office 365 또는 웹용 outlook에서 감독 대시보드를 사용 하는 대신 outlook을 사용 하려는 검토자는 outlook 클라이언트에 대 한 감독 추가 기능을 설치 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="28ff3-226">Reviewers that want to use Outlook instead of using the Supervision dashboard in Office 365 or Outlook on the web to review communications must install the Supervision add-in for their Outlook client.</span></span>

### <a name="step-1-copy-the-address-for-the-supervision-mailbox"></a><span data-ttu-id="28ff3-227">1 단계: 감독 사서함의 주소 복사</span><span class="sxs-lookup"><span data-stu-id="28ff3-227">Step 1: Copy the address for the supervision mailbox</span></span>

<span data-ttu-id="28ff3-228">Outlook 데스크톱에 대 한 추가 기능을 설치 하려면 감독 정책 설정의 일부로 만들어진 감독 사서함의 주소가 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="28ff3-228">To install the add-in for Outlook desktop, you'll need the address for the supervision mailbox that was created as part of the supervision policy setup.</span></span>
  
> [!NOTE]
> <span data-ttu-id="28ff3-229">다른 사용자가 정책을 만든 경우이 주소에서 추가 기능을 설치 하도록 요청 받아야 합니다.</span><span class="sxs-lookup"><span data-stu-id="28ff3-229">If someone else created the policy, you'll need to get this address from them to install the add-in.</span></span>

 <span data-ttu-id="28ff3-230">**감독 사서함 주소를 찾으려면**</span><span class="sxs-lookup"><span data-stu-id="28ff3-230">**To find the supervision mailbox address**</span></span>
  
1. <span data-ttu-id="28ff3-231">Office 365 조직의 관리자 계정에 대 한 자격 증명을 사용 하 여 [ &amp; 보안 및 준수 센터](https://protection.office.com) 에 로그인 합니다.</span><span class="sxs-lookup"><span data-stu-id="28ff3-231">Sign into the [Security &amp; Compliance Center](https://protection.office.com) using credentials for an admin account in your Office 365 organization.</span></span>

2. <span data-ttu-id="28ff3-232">**감독**으로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="28ff3-232">Go to **Supervision**.</span></span>

3. <span data-ttu-id="28ff3-233">검토할 통신을 모으는 감독 정책을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="28ff3-233">Click the supervision policy that's gathering the communications you want to review.</span></span>

4. <span data-ttu-id="28ff3-234">정책 세부 정보 플라이 아웃의 **감독 사서함**에서 주소를 복사 합니다.</span><span class="sxs-lookup"><span data-stu-id="28ff3-234">In the policy details flyout, under **Supervision mailbox**, copy the address.</span></span><br/><span data-ttu-id="28ff3-235">![감독 사서함 주소가 강조 표시 된 감독 정책의 세부 정보 플라이 아웃의 ' 감독 사서함 ' 섹션](media/71779d0e-4f01-4dd3-8234-5f9c30eeb067.jpg)</span><span class="sxs-lookup"><span data-stu-id="28ff3-235">![The 'Supervision Mailbox' section of a supervision policy's details flyout showing the supervision mailbox address highlighted](media/71779d0e-4f01-4dd3-8234-5f9c30eeb067.jpg)</span></span>
  
### <a name="step-2-configure-the-supervision-mailbox-for-outlook-desktop-access"></a><span data-ttu-id="28ff3-236">2 단계: Outlook 데스크톱 액세스에 대 한 감독 사서함 구성</span><span class="sxs-lookup"><span data-stu-id="28ff3-236">Step 2: Configure the supervision mailbox for Outlook desktop access</span></span>

<span data-ttu-id="28ff3-237">다음으로, Outlook을 메일 감독 사서함에 연결할 수 있도록 검토자가 몇 개의 Exchange Online PowerShell 명령을 실행 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="28ff3-237">Next, reviewers will need to run a couple Exchange Online PowerShell commands so they can connect Outlook to the supervision mailbox.</span></span>
  
1. <span data-ttu-id="28ff3-p123">Exchange Online PowerShell에 연결 합니다. [어떻게](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell) 해야 합니까?</span><span class="sxs-lookup"><span data-stu-id="28ff3-p123">Connect to Exchange Online PowerShell. [How do I do this?](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell)</span></span>

2. <span data-ttu-id="28ff3-240">다음 명령을 실행 하면 *SupervisoryReview {GUID} @domain onmicrosoft.com* 는 위의 1 단계에서 복사한 주소이 고 *사용자* 는 3 단계에서 감독 사서함에 연결할 검토자의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="28ff3-240">Run the following commands, where  *SupervisoryReview{GUID}@domain.onmicrosoft.com*  is the address you copied in Step 1 above, and  *User*  is the name of the reviewer who will be connecting to the supervision mailbox in Step 3.</span></span>

    ```Add-MailboxPermission "SupervisoryReview{GUID}@domain.onmicrosoft.com" -User <alias or email address of the account that has reviewer permissions to the supervision mailbox> -AccessRights FullAccess```

    ```Set-Mailbox "<SupervisoryReview{GUID}@domain.onmicrosoft.com>" -HiddenFromAddressListsEnabled: $false```

3. <span data-ttu-id="28ff3-241">아래 3 단계로 넘어가기 전까지 적어도 1 시간 이상 기다립니다.</span><span class="sxs-lookup"><span data-stu-id="28ff3-241">Wait at least an hour before moving on to Step 3 below.</span></span>

### <a name="step-3-create-an-outlook-profile-to-connect-to-the-supervision-mailbox"></a><span data-ttu-id="28ff3-242">3 단계: Outlook 프로필을 만들어 감독 사서함에 연결</span><span class="sxs-lookup"><span data-stu-id="28ff3-242">Step 3: Create an Outlook profile to connect to the supervision mailbox</span></span>

<span data-ttu-id="28ff3-243">마지막 단계에서 검토자는 Outlook 프로필을 만들어 감독 사서함에 연결 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="28ff3-243">For the final step, reviewers will need to create an Outlook profile to connect to the supervision mailbox.</span></span>

> [!NOTE]
> <span data-ttu-id="28ff3-p124">새 Outlook 프로필을 만들려면 Windows 제어판의 메일 설정을 사용 합니다. 이러한 설정에 액세스 하기 위해 수행 하는 경로는 사용 중인 windows 운영 체제 (windows 7, windows 8 또는 windows 10)와 설치 된 Outlook 버전에 따라 달라질 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="28ff3-p124">To create a new Outlook profile, you'll use the Mail settings in the Windows Control Panel. The path you take to get to these settings might depend on which Windows operating system (Windows 7, Windows 8, or Windows 10) you're using, and which version of Outlook is installed.</span></span>
  
1. <span data-ttu-id="28ff3-246">제어판을 열고 창 위쪽의 **검색** 상자에 **Mail**을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="28ff3-246">Open the Control Panel, and in the **Search** box at the top of the window, type **Mail**.</span></span><br/><span data-ttu-id="28ff3-p125">(제어판을 표시 하는 방법에 대 한 자세한 내용을 확인 하세요. [제어판은 무엇 인가요?](https://support.microsoft.com/help/13764/windows-where-is-control-panel)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="28ff3-p125">(Not sure how to get to the Control Panel? See [Where is Control Panel?](https://support.microsoft.com/help/13764/windows-where-is-control-panel))</span></span>
  
2. <span data-ttu-id="28ff3-249">**메일** 앱을 엽니다.</span><span class="sxs-lookup"><span data-stu-id="28ff3-249">Open the **Mail** app.</span></span>

3. <span data-ttu-id="28ff3-250">**메일 설정-Outlook**에서 **프로필 보기**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="28ff3-250">In **Mail Setup - Outlook**, click **Show Profiles**.</span></span><br/><span data-ttu-id="28ff3-251">![' 프로필 표시 ' 단추가 강조 표시 된 상태로 ' 메일 설정-Outlook ' 대화 상자](media/28b5dae9-d10c-4f2b-926a-294c857d555c.jpg)</span><span class="sxs-lookup"><span data-stu-id="28ff3-251">![The 'Mail Setup - Outlook' dialog box with the 'Show Profiles' button highlighted](media/28b5dae9-d10c-4f2b-926a-294c857d555c.jpg)</span></span>
  
4. <span data-ttu-id="28ff3-p126">**메일**에서 **추가**를 클릭 합니다. 그런 다음 **새 프로필**에 감독 사서함의 이름을 입력 합니다 (예: **감독**).</span><span class="sxs-lookup"><span data-stu-id="28ff3-p126">In **Mail**, click **Add**. Then, in **New Profile**, enter a name for the supervision mailbox (such as **Supervision**).</span></span><br/><span data-ttu-id="28ff3-254">![' 프로필 이름 ' 상자에 ' 감독 ' 이름을 표시 하는 ' 새 프로필 ' 대화 상자가 있습니다.](media/d02ae181-b541-4ec6-8f51-698f30033204.jpg)</span><span class="sxs-lookup"><span data-stu-id="28ff3-254">![The 'New Profile' dialog showing the name 'Supervision' in the 'Profile Name' box](media/d02ae181-b541-4ec6-8f51-698f30033204.jpg)</span></span>
  
5. <span data-ttu-id="28ff3-255">**Outlook을 Office 365에 연결**에서 **다른 계정에 연결**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="28ff3-255">In **Connect Outlook to Office 365**, click **Connect to a different account**.</span></span><br/><span data-ttu-id="28ff3-256">![' 다른 계정에 연결 ' 링크가 강조 표시 된 ' Outlook과 Office 365 연결 ' 메시지](media/fac49ff8-a7f0-4e82-a271-9ec045a95de1.jpg)</span><span class="sxs-lookup"><span data-stu-id="28ff3-256">![The 'Connect Outlook to Office 365' message with the 'Connect to a different account' link highlighted](media/fac49ff8-a7f0-4e82-a271-9ec045a95de1.jpg)</span></span>
  
6. <span data-ttu-id="28ff3-257">**자동 계정 설정**에서 **수동 설치 또는 추가 서버 유형을**선택 하 고 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="28ff3-257">In **Auto Account Setup**, choose **Manual setup or additional server types**, and then click **Next**.</span></span>

7. <span data-ttu-id="28ff3-p127">**계정 유형 선택**에서 **Office 365**을 선택 합니다. 그런 다음 **전자 메일 주소** 상자에 이전에 복사한 감독 사서함의 주소를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="28ff3-p127">In **Choose Your Account Type**, choose **Office 365**. Then, in the **Email Address** box, enter the address of the supervision mailbox you copied previously.</span></span><br/><span data-ttu-id="28ff3-260">![' 전자 메일 주소 ' 확인란이 강조 표시 된 Outlook의 ' 계정 추가 ' 대화 상자에서 ' 계정 유형 선택 ' 페이지입니다.](media/4f601236-9f69-4cf6-a58c-0b91204aa8cb.jpg)</span><span class="sxs-lookup"><span data-stu-id="28ff3-260">![The 'Choose Your Account Type' page of the 'Add Account' dialog in Outlook showing the 'Email Address' box highlighted.](media/4f601236-9f69-4cf6-a58c-0b91204aa8cb.jpg)</span></span>
  
8. <span data-ttu-id="28ff3-261">메시지가 나타나면 Office 365 자격 증명을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="28ff3-261">When prompted, enter your Office 365 credentials.</span></span>

9. <span data-ttu-id="28ff3-262">성공 하면 Outlook의 폴더 목록 보기에 \*\*감독 \<정책 이름\> \*\* 폴더가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="28ff3-262">If successful, you'll see the **Supervision - \<policy name\>** folder listed in the Folder List view in Outlook.</span></span>

## <a name="powershell-reference"></a><span data-ttu-id="28ff3-263">PowerShell 참조</span><span class="sxs-lookup"><span data-stu-id="28ff3-263">PowerShell reference</span></span>

<span data-ttu-id="28ff3-264">필요한 경우 다음 PowerShell cmdlet을 사용 하 여 감독 정책을 만들고 관리할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="28ff3-264">If needed, you can create and manage supervision policies using the following PowerShell cmdlets:</span></span>

- [<span data-ttu-id="28ff3-265">remove-supervisoryreviewpolicyv2</span><span class="sxs-lookup"><span data-stu-id="28ff3-265">New-SupervisoryReviewPolicyV2</span></span>](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance/new-supervisoryreviewpolicyv2?view=exchange-ps)
- [<span data-ttu-id="28ff3-266">remove-supervisoryreviewpolicyv2</span><span class="sxs-lookup"><span data-stu-id="28ff3-266">Get-SupervisoryReviewPolicyV2</span></span>](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance/get-supervisoryreviewpolicyv2?view=exchange-ps)
- [<span data-ttu-id="28ff3-267">remove-supervisoryreviewpolicyv2</span><span class="sxs-lookup"><span data-stu-id="28ff3-267">Set-SupervisoryReviewPolicyV2</span></span>](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance/set-supervisoryreviewpolicyv2?view=exchange-ps)
- [<span data-ttu-id="28ff3-268">remove-supervisoryreviewpolicyv2을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="28ff3-268">Remove-SupervisoryReviewPolicyV2</span></span>](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance/remove-supervisoryreviewpolicyv2?view=exchange-ps)
- [<span data-ttu-id="28ff3-269">set-supervisoryreviewrule</span><span class="sxs-lookup"><span data-stu-id="28ff3-269">New-SupervisoryReviewRule</span></span>](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance/new-supervisoryreviewrule?view=exchange-ps)
- [<span data-ttu-id="28ff3-270">set-supervisoryreviewrule</span><span class="sxs-lookup"><span data-stu-id="28ff3-270">Set-SupervisoryReviewRule</span></span>](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance/set-supervisoryreviewrule?view=exchange-ps)
- [<span data-ttu-id="28ff3-271">SupervisoryReviewActivity</span><span class="sxs-lookup"><span data-stu-id="28ff3-271">Get-SupervisoryReviewActivity</span></span>](https://docs.microsoft.com/powershell/module/exchange/reporting/get-supervisoryreviewactivity)
- [<span data-ttu-id="28ff3-272">SupervisoryReviewOverallProgressReport</span><span class="sxs-lookup"><span data-stu-id="28ff3-272">Get-SupervisoryReviewOverallProgressReport</span></span>](https://docs.microsoft.com/powershell/module/exchange/reporting/get-supervisoryreviewoverallprogressreport)
- [<span data-ttu-id="28ff3-273">SupervisoryReviewTopCasesReport</span><span class="sxs-lookup"><span data-stu-id="28ff3-273">Get-SupervisoryReviewTopCasesReport</span></span>](https://docs.microsoft.com/powershell/module/exchange/reporting/get-supervisoryreviewtopcasesreport)