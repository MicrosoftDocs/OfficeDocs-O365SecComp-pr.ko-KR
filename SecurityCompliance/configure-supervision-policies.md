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
ms.openlocfilehash: 76a5e7152b609944eeb2fe1390e204e1463a673b
ms.sourcegitcommit: 9a69ea604b415af4fef4964a19a09f3cead5a2ce
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/20/2019
ms.locfileid: "30701293"
---
# <a name="configure-supervision-policies-for-your-organization"></a><span data-ttu-id="53650-103">조직의 감독 정책 구성</span><span class="sxs-lookup"><span data-stu-id="53650-103">Configure supervision policies for your organization</span></span>

<span data-ttu-id="53650-104">감독 정책을 사용 하 여 내부 또는 외부 검토자가 검사할 직원 통신을 캡처할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="53650-104">Use supervision policies to capture employee communications for examination by internal or external reviewers.</span></span> <span data-ttu-id="53650-105">감독 정책을 통해 조직의 통신을 모니터링 하는 방법에 대 한 자세한 내용은 [Office 365의 감독 정책을](supervision-policies.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="53650-105">For more information about how supervision policies can help you monitor communications in your organization, see [Supervision policies in Office 365](supervision-policies.md).</span></span>

> [!NOTE]
> <span data-ttu-id="53650-106">감독 정책에 따라 모니터링 되는 사용자에 게는 Microsoft 365 E5 규정 준수 라이선스, 고급 준수 추가 기능이 포함 된 office 365 enterprise E3 라이선스 또는 office 365 Enterprise E5 구독에 포함 되어 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="53650-106">Users monitored by supervision policies must have either a Microsoft 365 E5 Compliance license, an Office 365 Enterprise E3 license with the Advanced Compliance add-on, or be included in an Office 365 Enterprise E5 subscription.</span></span>
<span data-ttu-id="53650-107">기존 Enterprise e5 요금제가 없고, 감독을 려 고 하는 경우 [Office 365 Enterprise e 5의 평가판에 등록할](https://go.microsoft.com/fwlink/p/?LinkID=698279)수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="53650-107">If you don't have an existing Enterprise E5 plan and want to try supervision, you can [sign up for a trial of Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span></span>
  
<span data-ttu-id="53650-108">Office 365 조직에서 감독을 설정 및 사용 하려면 다음 단계를 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="53650-108">Follow these steps to set up and use supervision in your Office 365 organization:</span></span>
  
- <span data-ttu-id="53650-109">**1 단계 (선택 사항)** - [감독을 위한 그룹 설정](configure-supervision-policies.md#exampledist)</span><span class="sxs-lookup"><span data-stu-id="53650-109">**Step 1 (optional)** - [Set up groups for Supervision](configure-supervision-policies.md#exampledist)</span></span>

    <span data-ttu-id="53650-110">감독 사용을 시작 하기 전에 의사 소통을 검토 하 고 이러한 검토를 수행할 사용자를 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="53650-110">Before you start using supervision, determine who will have their communications reviewed and who will perform those reviews.</span></span> <span data-ttu-id="53650-111">소수의 사용자만을 시작 하 여 감독의 작동 방식을 확인 하려는 경우 지금 그룹 설정 건너뛰기를 건너뛸 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="53650-111">If you want to get started with just a few users to see how supervision works, you can skip setting up groups for now.</span></span>

- <span data-ttu-id="53650-112">**2 단계 (필수)** - [조직에서 감독을 사용할 수 있도록 설정](configure-supervision-policies.md#MakeAvailable)</span><span class="sxs-lookup"><span data-stu-id="53650-112">**Step 2 (required)** - [Make supervision available in your organization](configure-supervision-policies.md#MakeAvailable)</span></span>

    <span data-ttu-id="53650-113">정책을 설정할 수 있도록 자신을 관리 검토 역할 그룹에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="53650-113">Add yourself to the Supervisory Review role group so you can set up policies.</span></span> <span data-ttu-id="53650-114">이 역할이 할당 된 모든 사용자는 보안 & 준수 센터의 **데이터 거 버 넌 스** 에 있는 **감독** 페이지에 액세스할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="53650-114">Anyone who has this role assigned can access the **Supervision** page under **Data Governance** in the Security & Compliance Center.</span></span> <span data-ttu-id="53650-115">검토할 전자 메일이 exchange online에서 호스트 되는 경우 각 검토자에 [게 exchange online에 대 한 원격 PowerShell 액세스](https://docs.microsoft.com/powershell/exchange/exchange-online/disable-access-to-exchange-online-powershell)권한도 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="53650-115">If email to be reviewed is hosted on Exchange Online, each reviewer must also have [remote PowerShell access to Exchange Online](https://docs.microsoft.com/powershell/exchange/exchange-online/disable-access-to-exchange-online-powershell).</span></span>

- <span data-ttu-id="53650-116">**3 단계 (선택 사항)** - [사용자 지정 중요 한 정보 유형 또는 사용자 지정 키워드 사전/lexicons 구성](configure-supervision-policies.md#sensitiveinfo)</span><span class="sxs-lookup"><span data-stu-id="53650-116">**Step 3 (optional)** - [Configure custom sensitive information types or custom keyword dictionaries/lexicons](configure-supervision-policies.md#sensitiveinfo)</span></span>

    <span data-ttu-id="53650-117">감독 정책에 대 한 사용자 지정 중요 한 정보 유형 또는 사용자 지정 키워드 사전을 사용 해야 하는 경우에는 감독 마법사를 시작 하기 전에 만들어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="53650-117">If you need to use a custom sensitive info type or a custom keyword dictionary for your supervision policy, you'll need to create it before starting the supervision wizard.</span></span>

- <span data-ttu-id="53650-118">**4 단계 (필수)** - [감독 정책 설정](configure-supervision-policies.md#setupsuper)</span><span class="sxs-lookup"><span data-stu-id="53650-118">**Step 4 (required)** - [Set up a supervision policy](configure-supervision-policies.md#setupsuper)</span></span>

    <span data-ttu-id="53650-119">보안 & 준수 센터에서 감독 정책을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="53650-119">You'll create supervision policies in the Security & Compliance Center.</span></span> <span data-ttu-id="53650-120">이러한 정책은 조직에서 검토할 대상이 되는 통신을 정의 하 고 검토를 수행할 사용자를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="53650-120">These policies define which communications are subject to review in your organization and specifies who should perform reviews.</span></span> <span data-ttu-id="53650-121">통신에는 전자 메일 및 Microsoft 팀 통신과 타사 플랫폼 통신 (예: Facebook, Twitter 등)이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="53650-121">Communications include email and Microsoft Teams communications, as well as 3rd-party platform communications (such as Facebook, Twitter, etc.)</span></span>

- <span data-ttu-id="53650-122">**5 단계-(선택 사항)** [새 감독 정책 테스트](configure-supervision-policies.md#TestPolicy)</span><span class="sxs-lookup"><span data-stu-id="53650-122">**Step 5 - (optional)** [Test your new supervision policy](configure-supervision-policies.md#TestPolicy)</span></span>

    <span data-ttu-id="53650-123">규정 준수 전략이 표준을 충족 하는지 확인 하는 것이 중요 한 역할을 하는 경우에는 감독 정책이 필요에 따라 작동 하도록 테스트 합니다.</span><span class="sxs-lookup"><span data-stu-id="53650-123">Testing your supervision policy to make sure it is functioning as desired is an important part of ensuring that your compliance strategy is meeting your standards.</span></span>

- <span data-ttu-id="53650-124">**6 단계-(선택 사항)** [outlook for Office 365 감독 대시보드 또는 웹용 outlook (이전의 outlook web App)을 사용 하지 않고 감독 된 통신을 검토 합니다](configure-supervision-policies.md#UseOutlook) .</span><span class="sxs-lookup"><span data-stu-id="53650-124">**Step 6 - (optional)** [Configure Outlook for reviewers who do not want to use Office 365 supervision dashboard or Outlook on the web (formerly known as Outlook Web App) to review supervised communications](configure-supervision-policies.md#UseOutlook)</span></span>

    <span data-ttu-id="53650-125">검토자가 outlook 클라이언트 내의 감독 기능에 액세스 하 여 각 항목을 평가 하 고 분류할 수 있도록 outlook을 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="53650-125">Outlook can be configured to give reviewers access to the supervision functionality within the Outlook client so they can assess and categorize each item.</span></span>

<span data-ttu-id="53650-126"><a name="exampledist"> </a></span><span class="sxs-lookup"><span data-stu-id="53650-126"></span></span>

## <a name="step-1---set-up-groups-for-supervision-optional"></a><span data-ttu-id="53650-127">1 단계-감독에 대 한 그룹 설정 (선택 사항)</span><span class="sxs-lookup"><span data-stu-id="53650-127">Step 1 - Set up groups for Supervision (optional)</span></span>

 <span data-ttu-id="53650-128">감독 정책을 만들 때 의사 소통을 검토 하 고 이러한 검토를 수행할 사용자를 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="53650-128">When you create a supervision policy, you'll determine who will have their communications reviewed and who will perform those reviews.</span></span> <span data-ttu-id="53650-129">정책에서는 전자 메일 주소를 사용 하 여 개인 이나 사용자 그룹을 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="53650-129">In the policy, you'll use email addresses to identify individuals or groups of people.</span></span> <span data-ttu-id="53650-130">설정을 간소화 하기 위해 통신을 검토 하 고 이러한 통신을 검토할 사용자에 대 한 그룹을 담당 하는 사용자에 대 한 그룹을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="53650-130">To simplify your setup, you can create groups for people who will have their communication reviewed and groups for people who will review those communications.</span></span> <span data-ttu-id="53650-131">그룹을 사용 하는 경우에는 서로 다른 두 사용자 그룹 간의 통신을 모니터링 하려는 경우 또는 감독 하지 않을 그룹을 지정 하려는 경우에는 여러 가지 사항이 필요할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="53650-131">If you're using groups, you might need several—for example, if you want to monitor communications between two distinct groups of people or if you want to specify a group that isn't going to be supervised.</span></span>

<span data-ttu-id="53650-132">다음 차트를 사용 하 여 조직에서 감독 정책을 위해 그룹을 구성 하는 데 도움이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="53650-132">Use the following chart to help you configure groups in your organization for supervision policies:</span></span>

| <span data-ttu-id="53650-133">**정책 구성원**</span><span class="sxs-lookup"><span data-stu-id="53650-133">**Policy Member**</span></span> | <span data-ttu-id="53650-134">**지원 되는 그룹**</span><span class="sxs-lookup"><span data-stu-id="53650-134">**Supported Groups**</span></span> | <span data-ttu-id="53650-135">**지원 되지 않는 그룹**</span><span class="sxs-lookup"><span data-stu-id="53650-135">**Unsupported Groups**</span></span> |
|:-----|:-----|:-----|
|<span data-ttu-id="53650-136">감독 사용자</span><span class="sxs-lookup"><span data-stu-id="53650-136">Supervised users</span></span> | <span data-ttu-id="53650-137">메일 그룹</span><span class="sxs-lookup"><span data-stu-id="53650-137">Distribution groups</span></span> <br> <span data-ttu-id="53650-138">Office 365 그룹</span><span class="sxs-lookup"><span data-stu-id="53650-138">Office 365 groups</span></span> | <span data-ttu-id="53650-139">동적 메일 그룹</span><span class="sxs-lookup"><span data-stu-id="53650-139">Dynamic distribution groups</span></span> |
| <span data-ttu-id="53650-140">가</span><span class="sxs-lookup"><span data-stu-id="53650-140">Reviewers</span></span> | <span data-ttu-id="53650-141">메일 사용 가능 보안 그룹</span><span class="sxs-lookup"><span data-stu-id="53650-141">Mail-enabled security groups</span></span>  | <span data-ttu-id="53650-142">메일 그룹</span><span class="sxs-lookup"><span data-stu-id="53650-142">Distribution groups</span></span> <br> <span data-ttu-id="53650-143">동적 메일 그룹</span><span class="sxs-lookup"><span data-stu-id="53650-143">Dynamic distribution groups</span></span> |
  
<span data-ttu-id="53650-144">그룹을 설정 하는 방법에 대 한 자세한 내용은 다음을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="53650-144">For more information about setting up groups, see:</span></span>
- [<span data-ttu-id="53650-145">메일 그룹 만들기 및 관리</span><span class="sxs-lookup"><span data-stu-id="53650-145">Create and manage distribution groups</span></span>](https://docs.microsoft.com/Exchange/recipients-in-exchange-online/manage-distribution-groups/manage-distribution-groups)
- [<span data-ttu-id="53650-146">메일 사용 가능 보안 그룹 관리</span><span class="sxs-lookup"><span data-stu-id="53650-146">Manage mail-enabled security groups</span></span>](https://docs.microsoft.com/Exchange/recipients-in-exchange-online/manage-mail-enabled-security-groups)
- [<span data-ttu-id="53650-147">Office 365 그룹 개요</span><span class="sxs-lookup"><span data-stu-id="53650-147">Overview of Office 365 Groups</span></span>](https://docs.microsoft.com/office365/admin/create-groups/office-365-groups?view=o365-worldwide)

<span data-ttu-id="53650-148"><a name="MakeAvailable"> </a></span><span class="sxs-lookup"><span data-stu-id="53650-148"></span></span>

## <a name="step-2---make-supervision-available-in-your-organization-required"></a><span data-ttu-id="53650-149">2 단계-조직에서 감독을 사용할 수 있도록 설정 (필수)</span><span class="sxs-lookup"><span data-stu-id="53650-149">Step 2 - Make supervision available in your organization (required)</span></span>

<span data-ttu-id="53650-150">보안 & 준수 센터에서 **감독** 을 메뉴 옵션으로 사용 하도록 설정 하려면 관리 검토 관리자 역할이 할당 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="53650-150">To make **Supervision** available as a menu option in the Security & Compliance Center, you must be assigned the Supervisory Review Administrator role.</span></span>
  
<span data-ttu-id="53650-151">이렇게 하려면 자신을 관리 검토 역할 그룹의 구성원으로 추가 하거나 새 역할 그룹을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="53650-151">To do this, you can either add yourself as a member of the Supervisory Review role group, or you can create a new role group.</span></span>
  
### <a name="add-members-to-the-supervisory-review-role-group"></a><span data-ttu-id="53650-152">관리 검토 역할 그룹에 구성원 추가</span><span class="sxs-lookup"><span data-stu-id="53650-152">Add members to the Supervisory Review role group</span></span>

1. <span data-ttu-id="53650-153">Office 365 [https://protection.office.com](https://protection.office.com) 조직의 관리자 계정에 대 한 자격 증명을 사용 하 여 로그인 합니다.</span><span class="sxs-lookup"><span data-stu-id="53650-153">Sign into [https://protection.office.com](https://protection.office.com) using credentials for an admin account in your Office 365 organization.</span></span>

2. <span data-ttu-id="53650-154">보안 & 준수 센터에서 **사용 권한**으로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="53650-154">In the Security & Compliance Center, go to **Permissions**.</span></span>

3. <span data-ttu-id="53650-155">**관리 검토** 역할 그룹을 선택한 다음 편집 아이콘을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="53650-155">Select the **Supervisory Review** role group and then click the Edit icon.</span></span>

4. <span data-ttu-id="53650-156">**구성원** 섹션에서 조직에 대 한 감독을 관리 하려는 사용자를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="53650-156">In the **Members** section, add the people who you want to manage supervision for your organization.</span></span>

### <a name="create-a-new-role-group"></a><span data-ttu-id="53650-157">새 역할 그룹 만들기</span><span class="sxs-lookup"><span data-stu-id="53650-157">Create a new role group</span></span>

1. <span data-ttu-id="53650-158">Office 365 [https://protection.office.com](https://protection.office.com) 조직의 관리자 계정에 대 한 자격 증명을 사용 하 여 로그인 합니다.</span><span class="sxs-lookup"><span data-stu-id="53650-158">Sign into [https://protection.office.com](https://protection.office.com) using credentials for an admin account in your Office 365 organization.</span></span>

2. <span data-ttu-id="53650-159">보안 & 준수 센터에서 **사용 권한** 으로 이동한 다음 추가 (**+**)를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="53650-159">In the Security & Compliance Center, go to **Permissions** and then click Add (**+**).</span></span>

3. <span data-ttu-id="53650-160">**역할** 섹션에서 추가 (**+**)를 클릭 하 고 아래로 스크롤하여 **관리 검토 관리자**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="53650-160">In the **Roles** section, click Add (**+**) and scroll down to **Supervisory Review Administrator**.</span></span> <span data-ttu-id="53650-161">이 역할을 역할 그룹에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="53650-161">Add this role to the role group.</span></span>

4. <span data-ttu-id="53650-162">**구성원** 섹션에서 조직에 대 한 감독을 관리 하려는 사용자를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="53650-162">In the **Members** section, add the people who you want to manage supervision for your organization.</span></span>

<span data-ttu-id="53650-163">역할 그룹 및 사용 권한에 대 한 자세한 내용은 [Office 365 보안 &amp; 및 준수 센터의 사용 권한을](permissions-in-the-security-and-compliance-center.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="53650-163">For more information about role groups and permissions, see [Permissions in the Office 365 Security &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md).</span></span>

### <a name="enable-remote-powershell-access-for-reviewers-if-email-is-hosted-on-exchange-online"></a><span data-ttu-id="53650-164">검토자에 대해 원격 PowerShell 액세스 사용 (전자 메일이 Exchange Online에서 호스트 되는 경우)</span><span class="sxs-lookup"><span data-stu-id="53650-164">Enable remote PowerShell access for reviewers (if email is hosted on Exchange Online)</span></span>

1. <span data-ttu-id="53650-165">[사용 또는 사용 안 함 Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/disable-access-to-exchange-online-powershell)에 대 한 지침을 따릅니다.</span><span class="sxs-lookup"><span data-stu-id="53650-165">Follow the guidance in [Enable or disable access to Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/disable-access-to-exchange-online-powershell).</span></span>

<span data-ttu-id="53650-166"><a name="sensitiveinfo"> </a></span><span class="sxs-lookup"><span data-stu-id="53650-166"></span></span>
  
## <a name="step-3---create-custom-sensitive-information-types-and-custom-keyword-dictionaries-optional"></a><span data-ttu-id="53650-167">3 단계-사용자 지정 중요 한 정보 유형 및 사용자 지정 키워드 사전 만들기 (선택 사항)</span><span class="sxs-lookup"><span data-stu-id="53650-167">Step 3 - Create custom sensitive information types and custom keyword dictionaries (optional)</span></span>

<span data-ttu-id="53650-168">감독 정책 마법사에서 기존 사용자 지정 중요 한 정보 유형 또는 사용자 지정 키워드 사전을 선택 하려면 먼저 필요한 경우 이러한 항목을 만들어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="53650-168">In order to pick from existing custom sensitive information types or custom keyword dictionaries in the supervision policy wizard, you first need to create these items if needed.</span></span>

### <a name="create-custom-keyword-dictionarylexicon-optional"></a><span data-ttu-id="53650-169">사용자 지정 키워드 사전/어휘 만들기 (선택 사항)</span><span class="sxs-lookup"><span data-stu-id="53650-169">Create custom keyword dictionary/lexicon (optional)</span></span>

<span data-ttu-id="53650-170">메모장과 같은 텍스트 편집기를 사용 하 여 감독 정책에서 모니터링할 키워드 용어를 포함 하는 새 파일을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="53650-170">Using a text editor (like Notepad), create a new file that includes the keyword terms you'd like to monitor in a supervision policy.</span></span> <span data-ttu-id="53650-171">각 용어가 별도의 줄에 있는지 확인 하 고 파일을 **유니코드/u t f-16 (꼬마)** 형식으로 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="53650-171">Make sure each term is on a separate line and save the file in the **Unicode/UTF-16 (Little Endian)** format.</span></span>

### <a name="create-custom-sensitive-information-types"></a><span data-ttu-id="53650-172">사용자 지정 중요 한 정보 유형 만들기</span><span class="sxs-lookup"><span data-stu-id="53650-172">Create custom sensitive information types</span></span>

1. <span data-ttu-id="53650-173">새 중요 한 정보 유형을 만들고 Office 365 Security & 준수 센터에서 사용자 지정 사전을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="53650-173">Create a new sensitive information type and add your custom dictionary in the Office 365 Security & Compliance Center.</span></span> <span data-ttu-id="53650-174">**중요 한 정보** 유형 **분류** \> 로 이동 하 여 **새 중요 한 정보 유형 마법사**의 단계를 따릅니다.</span><span class="sxs-lookup"><span data-stu-id="53650-174">Navigate to **Classifications** \> **Sensitive info types** and follow the steps in the **New sensitive info type wizard**.</span></span> <span data-ttu-id="53650-175">여기에서 다음을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="53650-175">Here you will:</span></span>

    - <span data-ttu-id="53650-176">중요 한 정보 유형에 대 한 이름 및 설명 정의</span><span class="sxs-lookup"><span data-stu-id="53650-176">Define a name and description for the sensitive info type</span></span>
    - <span data-ttu-id="53650-177">근접성, 신뢰 수준 및 주 패턴 요소 정의</span><span class="sxs-lookup"><span data-stu-id="53650-177">Define the proximity, confidence level, and primary pattern elements</span></span>
    - <span data-ttu-id="53650-178">일치 요소에 대 한 요구 사항으로 사용자 지정 사전 가져오기</span><span class="sxs-lookup"><span data-stu-id="53650-178">Import your custom dictionary as a requirement for the matching element</span></span>
    - <span data-ttu-id="53650-179">선택 항목 검토 및 중요 한 정보 유형 만들기</span><span class="sxs-lookup"><span data-stu-id="53650-179">Review your selections and create the sensitive info type</span></span>

    <span data-ttu-id="53650-180">자세한 내용은 [사용자 지정 중요 한 정보 유형 만들기](create-a-custom-sensitive-information-type.md) 및 [키워드 사전 만들기](create-a-keyword-dictionary.md) 를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="53650-180">For more detailed information, see [Create a custom sensitive information type](create-a-custom-sensitive-information-type.md) and [Create a keyword dictionary](create-a-keyword-dictionary.md)</span></span>

    <span data-ttu-id="53650-181">사용자 지정 사전/어휘를 만든 후에는 [DlpKeywordDictionary](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-dlp/get-dlpkeyworddictionary) cmdlet을 사용 하 여 구성 된 키워드를 보거나 [DlpKeywordDictionary](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-dlp/set-dlpkeyworddictionary) cmdlet을 사용 하 여 용어를 추가 및 제거할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="53650-181">After the custom dictionary/lexicon is created, you can view the configured keywords using the [Get-DlpKeywordDictionary](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-dlp/get-dlpkeyworddictionary) cmdlet or add and remove terms using the [Set-DlpKeywordDictionary](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-dlp/set-dlpkeyworddictionary) cmdlet.</span></span>

<span data-ttu-id="53650-182"><a name="setupsuper"> </a></span><span class="sxs-lookup"><span data-stu-id="53650-182"></span></span>

## <a name="step-4---set-up-a-supervision-policy-required"></a><span data-ttu-id="53650-183">4 단계-감독 정책 설정 (필수)</span><span class="sxs-lookup"><span data-stu-id="53650-183">Step 4 - Set up a supervision policy (required)</span></span>
  
1. <span data-ttu-id="53650-184">Office 365 [https://protection.office.com](https://protection.office.com) 조직의 관리자 계정에 대 한 자격 증명을 사용 하 여 로그인 합니다.</span><span class="sxs-lookup"><span data-stu-id="53650-184">Sign into [https://protection.office.com](https://protection.office.com) using credentials for an admin account in your Office 365 organization.</span></span>

2. <span data-ttu-id="53650-185">보안 & 준수 센터에서 **감독**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="53650-185">In the Security & Compliance Center, select **Supervision**.</span></span>
  
3. <span data-ttu-id="53650-186">**만들기** 를 선택 하 고 마법사의 지시에 따라 다음과 같은 정책 페이지를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="53650-186">Select **Create** and then follow the wizard to set up the following pages of the policy.</span></span> <span data-ttu-id="53650-187">마법사를 사용 하 여 다음을 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="53650-187">Using the wizard, you will:</span></span>

    - <span data-ttu-id="53650-188">정책에 이름과 설명을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="53650-188">Give the policy a name and description.</span></span>
    - <span data-ttu-id="53650-189">제외할 사용자 또는 그룹 선택을 비롯 하 여 감독할 사용자 또는 그룹을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="53650-189">Choose the users or groups to supervise, including choosing users or groups you'd like to exclude.</span></span>
    - <span data-ttu-id="53650-190">감독 정책 조건을 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="53650-190">Define the supervision policy conditions.</span></span>
    - <span data-ttu-id="53650-191">중요 한 정보 유형을 포함 하 고 싶은 경우 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="53650-191">Choose if you'd like to include sensitive information types.</span></span> <span data-ttu-id="53650-192">여기에서 기본 및 사용자 지정 중요 한 정보 유형을 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="53650-192">This is where you can select default and custom sensitive info types.</span></span>
    - <span data-ttu-id="53650-193">검토할 통신의 비율을 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="53650-193">Define the percentage of communications to review.</span></span>
    - <span data-ttu-id="53650-194">정책에 대 한 검토자를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="53650-194">Choose the reviewers for the policy.</span></span> <span data-ttu-id="53650-195">검토자는 개별 사용자 또는 [메일 사용이 가능한 보안 그룹이](https://docs.microsoft.com/Exchange/recipients-in-exchange-online/manage-mail-enabled-security-groups#create-a-mail-enabled-security-group)될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="53650-195">Reviewers can be individual users or [mail-enabled security groups](https://docs.microsoft.com/Exchange/recipients-in-exchange-online/manage-mail-enabled-security-groups#create-a-mail-enabled-security-group).</span></span>
    - <span data-ttu-id="53650-196">정책 선택을 검토 하 고 정책을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="53650-196">Review your policy selections and create the policy.</span></span>

<span data-ttu-id="53650-197"><a name="TestPolicy"> </a></span><span class="sxs-lookup"><span data-stu-id="53650-197"></span></span>

## <a name="step-5---test-your-supervision-policy-optional"></a><span data-ttu-id="53650-198">5 단계-감독 정책 테스트 (선택 사항)</span><span class="sxs-lookup"><span data-stu-id="53650-198">Step 5 - Test your supervision policy (optional)</span></span>

<span data-ttu-id="53650-199">감독 정책을 만든 후에는 테스트를 통해 정의한 조건이 정책에 의해 적절 하 게 적용 되는지 확인 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="53650-199">After you create a supervision policy, it's a good idea to test to make sure that the conditions you defined are being properly enforced by the policy.</span></span> <span data-ttu-id="53650-200">또한 감독 정책에 중요 한 정보 유형이 포함 되어 있는 경우 [DLP (데이터 손실 방지) 정책을 테스트할](create-test-tune-dlp-policy.md) 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="53650-200">You may also want to [test your data loss prevention (DLP) policies](create-test-tune-dlp-policy.md) if your supervision policies include sensitive information types.</span></span> <span data-ttu-id="53650-201">다음 단계에 따라 감독 정책을 테스트 합니다.</span><span class="sxs-lookup"><span data-stu-id="53650-201">Follow the steps below to test your supervision policy:</span></span>

1. <span data-ttu-id="53650-202">테스트할 정책에 정의 된 감독 된 사용자로 로그인 한 전자 메일 클라이언트 또는 Microsoft 팀을 엽니다.</span><span class="sxs-lookup"><span data-stu-id="53650-202">Open an email client or Microsoft Teams logged in as a supervised user defined in the policy you want to test.</span></span>
2. <span data-ttu-id="53650-203">감독 정책에 정의한 기준을 충족 하는 전자 메일 또는 Microsoft 팀 채팅을 보냅니다.</span><span class="sxs-lookup"><span data-stu-id="53650-203">Send an email or Microsoft Teams chat that meets the criteria you've defined in the supervision policy.</span></span> <span data-ttu-id="53650-204">키워드, 첨부 파일 크기, 도메인 등이 될 수 있습니다. 정책에서 구성 된 조건부 설정이 너무 제한적 이거나 너무 lenient 인지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="53650-204">This can be a keyword, attachment size, domain, etc. Make sure you determine if your configured conditional settings in the policy is too restrictive or too lenient.</span></span>

    > [!Note]
    > <span data-ttu-id="53650-205">정의 된 정책이 적용 되는 전자 메일은 거의 실시간으로 처리 되며 정책이 구성 된 직후에 테스트할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="53650-205">Emails subject to defined policies are processed in near real-time and can be tested immediately after the policy is configured.</span></span> <span data-ttu-id="53650-206">Microsoft 팀의 채팅에는 정책에서 전체 프로세스를 수행 하는 데 최대 24 시간이 걸릴 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="53650-206">Chats in Microsoft Teams can take up to 24 hours to fully process in a policy.</span></span> 

3. <span data-ttu-id="53650-207">감독 정책에 지정 된 검토자로 Office 365 테 넌 트에 로그인 합니다.</span><span class="sxs-lookup"><span data-stu-id="53650-207">Log into your Office 365 tenant as a reviewer designated in the supervision policy.</span></span> <span data-ttu-id="53650-208">*사용자 지정 정책이* > **열려** 있는 **감독** > 을 탐색 하 여 정책에 대 한 보고서를 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="53650-208">Navigate to **Supervision** > *Your Custom Policy* > **Open** to view the report for the policy.</span></span>

<span data-ttu-id="53650-209"><a name="UseOutlook"> </a></span><span class="sxs-lookup"><span data-stu-id="53650-209"></span></span>

## <a name="step-6---configure-outlook-for-reviewers-optional"></a><span data-ttu-id="53650-210">6 단계-Outlook for 검토자별로 구성 (선택 사항)</span><span class="sxs-lookup"><span data-stu-id="53650-210">Step 6 - Configure Outlook for reviewers (optional)</span></span>

<span data-ttu-id="53650-211">Office 365에서 감독 대시보드를 사용 하 여 통신을 검토 하는 대신 outlook을 사용 하려는 검토자는 자신의 outlook 클라이언트를 구성 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="53650-211">Reviewers that want to use Outlook instead of using the Supervision dashboard in Office 365 to review communications must configure their Outlook client.</span></span>

### <a name="step-1-copy-the-address-for-the-supervision-mailbox"></a><span data-ttu-id="53650-212">1 단계: 감독 사서함의 주소 복사</span><span class="sxs-lookup"><span data-stu-id="53650-212">Step 1: Copy the address for the supervision mailbox</span></span>

<span data-ttu-id="53650-213">웹용 outlook 데스크톱 또는 outlook에 대 한 검토를 구성 하려면 감독 정책 설정의 일부로 만들어진 감독 사서함의 주소가 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="53650-213">To configure review for Outlook desktop or Outlook for the web, you'll need the address for the supervision mailbox that was created as part of the supervision policy setup.</span></span>
  
> [!NOTE]
> <span data-ttu-id="53650-214">다른 사용자가 정책을 만든 경우이 주소에서 추가 기능을 설치 하도록 요청 받아야 합니다.</span><span class="sxs-lookup"><span data-stu-id="53650-214">If someone else created the policy, you'll need to get this address from them to install the add-in.</span></span>

 <span data-ttu-id="53650-215">**감독 사서함 주소를 찾으려면**</span><span class="sxs-lookup"><span data-stu-id="53650-215">**To find the supervision mailbox address**</span></span>
  
1. <span data-ttu-id="53650-216">Office 365 조직의 관리자 계정에 대 한 자격 증명을 사용 하 여 [ &amp; 보안 및 준수 센터](https://protection.office.com) 에 로그인 합니다.</span><span class="sxs-lookup"><span data-stu-id="53650-216">Sign into the [Security &amp; Compliance Center](https://protection.office.com) using credentials for an admin account in your Office 365 organization.</span></span>

2. <span data-ttu-id="53650-217">**감독**으로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="53650-217">Go to **Supervision**.</span></span>

3. <span data-ttu-id="53650-218">검토할 통신을 모으는 감독 정책을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="53650-218">Click the supervision policy that's gathering the communications you want to review.</span></span>

4. <span data-ttu-id="53650-219">정책 세부 정보 플라이 아웃의 **감독 사서함**에서 주소를 복사 합니다.</span><span class="sxs-lookup"><span data-stu-id="53650-219">In the policy details flyout, under **Supervision mailbox**, copy the address.</span></span><br/><span data-ttu-id="53650-220">![감독 사서함 주소가 강조 표시 된 감독 정책의 세부 정보 플라이 아웃의 ' 감독 사서함 ' 섹션](media/71779d0e-4f01-4dd3-8234-5f9c30eeb067.jpg)</span><span class="sxs-lookup"><span data-stu-id="53650-220">![The 'Supervision Mailbox' section of a supervision policy's details flyout showing the supervision mailbox address highlighted](media/71779d0e-4f01-4dd3-8234-5f9c30eeb067.jpg)</span></span>
  
### <a name="step-2-configure-the-supervision-mailbox-for-outlook-access"></a><span data-ttu-id="53650-221">2 단계: Outlook 액세스를 위한 감독 사서함 구성</span><span class="sxs-lookup"><span data-stu-id="53650-221">Step 2: Configure the supervision mailbox for Outlook access</span></span>

<span data-ttu-id="53650-222">다음으로, Outlook을 메일 감독 사서함에 연결할 수 있도록 검토자가 몇 개의 Exchange Online PowerShell 명령을 실행 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="53650-222">Next, reviewers will need to run a couple Exchange Online PowerShell commands so they can connect Outlook to the supervision mailbox.</span></span>
  
1. <span data-ttu-id="53650-223">Exchange Online PowerShell에 연결합니다.</span><span class="sxs-lookup"><span data-stu-id="53650-223">Connect to Exchange Online PowerShell.</span></span> [<span data-ttu-id="53650-224">어떻게 해야 합니까?</span><span class="sxs-lookup"><span data-stu-id="53650-224">How do I do this?</span></span>](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell)

2. <span data-ttu-id="53650-225">다음 명령을 실행 하면 *SupervisoryReview {GUID} @domain onmicrosoft.com* 는 위의 1 단계에서 복사한 주소이 고 *사용자* 는 3 단계에서 감독 사서함에 연결할 검토자의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="53650-225">Run the following commands, where  *SupervisoryReview{GUID}@domain.onmicrosoft.com*  is the address you copied in Step 1 above, and  *User*  is the name of the reviewer who will be connecting to the supervision mailbox in Step 3.</span></span>

    ```Add-MailboxPermission "SupervisoryReview{GUID}@domain.onmicrosoft.com" -User <alias or email address of the account that has reviewer permissions to the supervision mailbox> -AccessRights FullAccess```

    ```Set-Mailbox "<SupervisoryReview{GUID}@domain.onmicrosoft.com>" -HiddenFromAddressListsEnabled: $false```

3. <span data-ttu-id="53650-226">아래 3 단계로 넘어가기 전까지 적어도 1 시간 이상 기다립니다.</span><span class="sxs-lookup"><span data-stu-id="53650-226">Wait at least an hour before moving on to Step 3 below.</span></span>

### <a name="step-3-create-an-outlook-profile-to-connect-to-the-supervision-mailbox"></a><span data-ttu-id="53650-227">3 단계: Outlook 프로필을 만들어 감독 사서함에 연결</span><span class="sxs-lookup"><span data-stu-id="53650-227">Step 3: Create an Outlook profile to connect to the supervision mailbox</span></span>

<span data-ttu-id="53650-228">마지막 단계에서 검토자는 Outlook 프로필을 만들어 감독 사서함에 연결 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="53650-228">For the final step, reviewers will need to create an Outlook profile to connect to the supervision mailbox.</span></span>

> [!NOTE]
> <span data-ttu-id="53650-229">새 Outlook 프로필을 만들려면 Windows 제어판의 메일 설정을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="53650-229">To create a new Outlook profile, you'll use the Mail settings in the Windows Control Panel.</span></span> <span data-ttu-id="53650-230">이러한 설정에 액세스 하기 위해 수행 하는 경로는 사용 중인 windows 운영 체제 (windows 7, windows 8 또는 windows 10)와 설치 된 Outlook 버전에 따라 달라질 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="53650-230">The path you take to get to these settings might depend on which Windows operating system (Windows 7, Windows 8, or Windows 10) you're using, and which version of Outlook is installed.</span></span>
  
1. <span data-ttu-id="53650-231">제어판을 열고 창 위쪽의 **검색** 상자에 **Mail**을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="53650-231">Open the Control Panel, and in the **Search** box at the top of the window, type **Mail**.</span></span><br/><span data-ttu-id="53650-232">(제어판을 표시 하는 방법에 대 한 자세한 내용을 확인 하세요.</span><span class="sxs-lookup"><span data-stu-id="53650-232">(Not sure how to get to the Control Panel?</span></span> <span data-ttu-id="53650-233">[제어판은 무엇 인가요?](https://support.microsoft.com/help/13764/windows-where-is-control-panel)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="53650-233">See [Where is Control Panel?](https://support.microsoft.com/help/13764/windows-where-is-control-panel))</span></span>
  
2. <span data-ttu-id="53650-234">**메일** 앱을 엽니다.</span><span class="sxs-lookup"><span data-stu-id="53650-234">Open the **Mail** app.</span></span>

3. <span data-ttu-id="53650-235">**메일 설정-Outlook**에서 **프로필 보기**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="53650-235">In **Mail Setup - Outlook**, click **Show Profiles**.</span></span><br/><span data-ttu-id="53650-236">![' 프로필 표시 ' 단추가 강조 표시 된 상태로 ' 메일 설정-Outlook ' 대화 상자](media/28b5dae9-d10c-4f2b-926a-294c857d555c.jpg)</span><span class="sxs-lookup"><span data-stu-id="53650-236">![The 'Mail Setup - Outlook' dialog box with the 'Show Profiles' button highlighted](media/28b5dae9-d10c-4f2b-926a-294c857d555c.jpg)</span></span>
  
4. <span data-ttu-id="53650-237">**메일**에서 **추가**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="53650-237">In **Mail**, click **Add**.</span></span> <span data-ttu-id="53650-238">그런 다음 **새 프로필**에 감독 사서함의 이름을 입력 합니다 (예: **감독**).</span><span class="sxs-lookup"><span data-stu-id="53650-238">Then, in **New Profile**, enter a name for the supervision mailbox (such as **Supervision**).</span></span><br/><span data-ttu-id="53650-239">![' 프로필 이름 ' 상자에 ' 감독 ' 이름을 표시 하는 ' 새 프로필 ' 대화 상자가 있습니다.](media/d02ae181-b541-4ec6-8f51-698f30033204.jpg)</span><span class="sxs-lookup"><span data-stu-id="53650-239">![The 'New Profile' dialog showing the name 'Supervision' in the 'Profile Name' box](media/d02ae181-b541-4ec6-8f51-698f30033204.jpg)</span></span>
  
5. <span data-ttu-id="53650-240">**Outlook을 Office 365에 연결**에서 **다른 계정에 연결**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="53650-240">In **Connect Outlook to Office 365**, click **Connect to a different account**.</span></span><br/><span data-ttu-id="53650-241">![' 다른 계정에 연결 ' 링크가 강조 표시 된 ' Outlook과 Office 365 연결 ' 메시지](media/fac49ff8-a7f0-4e82-a271-9ec045a95de1.jpg)</span><span class="sxs-lookup"><span data-stu-id="53650-241">![The 'Connect Outlook to Office 365' message with the 'Connect to a different account' link highlighted](media/fac49ff8-a7f0-4e82-a271-9ec045a95de1.jpg)</span></span>
  
6. <span data-ttu-id="53650-242">**자동 계정 설정**에서 **수동 설치 또는 추가 서버 유형을**선택 하 고 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="53650-242">In **Auto Account Setup**, choose **Manual setup or additional server types**, and then click **Next**.</span></span>

7. <span data-ttu-id="53650-243">**계정 유형 선택**에서 **Office 365**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="53650-243">In **Choose Your Account Type**, choose **Office 365**.</span></span> <span data-ttu-id="53650-244">그런 다음 **전자 메일 주소** 상자에 이전에 복사한 감독 사서함의 주소를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="53650-244">Then, in the **Email Address** box, enter the address of the supervision mailbox you copied previously.</span></span><br/><span data-ttu-id="53650-245">![' 전자 메일 주소 ' 확인란이 강조 표시 된 Outlook의 ' 계정 추가 ' 대화 상자에서 ' 계정 유형 선택 ' 페이지입니다.](media/4f601236-9f69-4cf6-a58c-0b91204aa8cb.jpg)</span><span class="sxs-lookup"><span data-stu-id="53650-245">![The 'Choose Your Account Type' page of the 'Add Account' dialog in Outlook showing the 'Email Address' box highlighted.](media/4f601236-9f69-4cf6-a58c-0b91204aa8cb.jpg)</span></span>
  
8. <span data-ttu-id="53650-246">메시지가 나타나면 Office 365 자격 증명을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="53650-246">When prompted, enter your Office 365 credentials.</span></span>

9. <span data-ttu-id="53650-247">성공 하면 Outlook의 폴더 목록 보기에 \*\*감독 \<정책 이름\> \*\* 폴더가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="53650-247">If successful, you'll see the **Supervision - \<policy name\>** folder listed in the Folder List view in Outlook.</span></span>

## <a name="powershell-reference"></a><span data-ttu-id="53650-248">PowerShell 참조</span><span class="sxs-lookup"><span data-stu-id="53650-248">PowerShell reference</span></span>

<span data-ttu-id="53650-249">필요한 경우 다음 PowerShell cmdlet을 사용 하 여 감독 정책을 만들고 관리할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="53650-249">If needed, you can create and manage supervision policies using the following PowerShell cmdlets:</span></span>

- [<span data-ttu-id="53650-250">remove-supervisoryreviewpolicyv2</span><span class="sxs-lookup"><span data-stu-id="53650-250">New-SupervisoryReviewPolicyV2</span></span>](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance/new-supervisoryreviewpolicyv2?view=exchange-ps)
- [<span data-ttu-id="53650-251">remove-supervisoryreviewpolicyv2</span><span class="sxs-lookup"><span data-stu-id="53650-251">Get-SupervisoryReviewPolicyV2</span></span>](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance/get-supervisoryreviewpolicyv2?view=exchange-ps)
- [<span data-ttu-id="53650-252">remove-supervisoryreviewpolicyv2</span><span class="sxs-lookup"><span data-stu-id="53650-252">Set-SupervisoryReviewPolicyV2</span></span>](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance/set-supervisoryreviewpolicyv2?view=exchange-ps)
- [<span data-ttu-id="53650-253">remove-supervisoryreviewpolicyv2을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="53650-253">Remove-SupervisoryReviewPolicyV2</span></span>](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance/remove-supervisoryreviewpolicyv2?view=exchange-ps)
- [<span data-ttu-id="53650-254">set-supervisoryreviewrule</span><span class="sxs-lookup"><span data-stu-id="53650-254">New-SupervisoryReviewRule</span></span>](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance/new-supervisoryreviewrule?view=exchange-ps)
- [<span data-ttu-id="53650-255">set-supervisoryreviewrule</span><span class="sxs-lookup"><span data-stu-id="53650-255">Set-SupervisoryReviewRule</span></span>](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance/set-supervisoryreviewrule?view=exchange-ps)
- [<span data-ttu-id="53650-256">SupervisoryReviewActivity</span><span class="sxs-lookup"><span data-stu-id="53650-256">Get-SupervisoryReviewActivity</span></span>](https://docs.microsoft.com/powershell/module/exchange/reporting/get-supervisoryreviewactivity)
- [<span data-ttu-id="53650-257">SupervisoryReviewOverallProgressReport</span><span class="sxs-lookup"><span data-stu-id="53650-257">Get-SupervisoryReviewOverallProgressReport</span></span>](https://docs.microsoft.com/powershell/module/exchange/reporting/get-supervisoryreviewoverallprogressreport)
- [<span data-ttu-id="53650-258">SupervisoryReviewTopCasesReport</span><span class="sxs-lookup"><span data-stu-id="53650-258">Get-SupervisoryReviewTopCasesReport</span></span>](https://docs.microsoft.com/powershell/module/exchange/reporting/get-supervisoryreviewtopcasesreport)