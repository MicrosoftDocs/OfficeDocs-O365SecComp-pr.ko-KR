---
title: 민감도 레이블에서 암호화를 사용하여 콘텐츠 액세스 제한
ms.author: stephow
author: stephow-MSFT
manager: laurawi
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Priority
ms.collection:
- M365-security-compliance
search.appverid:
- MOE150
- MET150
description: 민감한 레이블을 만들면 레이블이 적용되는 콘텐츠에 대한 액세스를 제한할 수 있습니다. 민감도 레이블에서 암호화를 사용하여 내용을 보호할 수 있습니다.
ms.openlocfilehash: a30f5d6168ea8118ef6b30ff26a429857affaa4a
ms.sourcegitcommit: fd3db13cd4fc71cd2cb164fd702007acba3e7399
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/04/2019
ms.locfileid: "36717683"
---
# <a name="restrict-access-to-content-by-using-encryption-in-sensitivity-labels"></a><span data-ttu-id="35700-104">민감도 레이블에서 암호화를 사용하여 콘텐츠 액세스 제한</span><span class="sxs-lookup"><span data-stu-id="35700-104">Restrict access to content by using encryption in sensitivity labels</span></span>

<span data-ttu-id="35700-p102">민감한 레이블을 만들면 레이블이 적용되는 콘텐츠에 대한 액세스를 제한할 수 있습니다. 예를 들어 민감도 레이블의 암호화 설정으로 다음과 같이 콘텐츠를 보호할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="35700-p102">When you create a sensitivity label, you can restrict access to content that the label will be applied to. For example, with the encryption settings for a sensitivity label, you can protect content so that:</span></span>

- <span data-ttu-id="35700-107">조직 내의 사용자만 기밀 문서나 전자 메일을 열 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="35700-107">Only users within your organization can open a confidential document or email.</span></span>
- <span data-ttu-id="35700-108">마케팅 부서의 사용자만 프로모션 공지 사항 문서 또는 전자 메일을 편집하고 인쇄할 수 있으며 조직의 다른 모든 사용자는 이를 읽는 것만 가능합니다.</span><span class="sxs-lookup"><span data-stu-id="35700-108">Only users in the marketing department can edit and print the promotion announcement document or email, while all other users in your organization can only read it.</span></span>
- <span data-ttu-id="35700-109">사용자는 내부 재구성에 대한 소식이 포함된 전자 메일을 전달하거나 정보를 복사할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="35700-109">Users cannot forward an email or copy information from it that contains news about an internal reorganization.</span></span>
- <span data-ttu-id="35700-110">비즈니스 파트너에게 전송되는 현재 가격 목록은 특정 날짜 이후에 열 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="35700-110">The current price list that is sent to business partners cannot be opened after a specified date.</span></span>

<span data-ttu-id="35700-111">문서 또는 전자 메일이 암호화되면 콘텐츠에 대한 액세스가 다음과 같이 제한됩니다.</span><span class="sxs-lookup"><span data-stu-id="35700-111">When a document or email is encrypted, access to the content is restricted, so that it:</span></span>

- <span data-ttu-id="35700-112">레이블의 암호화 설정에 따라 권한이 있는 사용자만 암호를 해독할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="35700-112">Can be decrypted only by users authorized by the label’s encryption settings.</span></span>
- <span data-ttu-id="35700-113">파일의 이름이 바뀌더라도 조직의 내부 또는 외부에 관계 없이 암호화된 상태로 유지됩니다.</span><span class="sxs-lookup"><span data-stu-id="35700-113">Remains encrypted no matter where it resides, inside or outside your organization, even if the file’s renamed.</span></span>
- <span data-ttu-id="35700-114">작동 중단 시(예: OneDrive 계정에서) 및 전송 중(예: 보낸 전자 메일)에 모두 암호화됩니다.</span><span class="sxs-lookup"><span data-stu-id="35700-114">Is encrypted both at rest (for example, in a OneDrive account) and in transit (for example, a sent email).</span></span>

<span data-ttu-id="35700-115">마지막으로, 관리자가 민감도 레이블을 만들 때 다음 중 하나를 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="35700-115">Finally, as an admin, when you create a sensitivity label, you can choose either to:</span></span>

- <span data-ttu-id="35700-116">어떤 사용자에게 해당 레이블이 있는 콘텐츠에 어떤 권한을 부여할 것인지 정확하게 결정하도록 **지금 권한을 할당**합니다.</span><span class="sxs-lookup"><span data-stu-id="35700-116">**Assign permissions now**, so that you determine exactly which users get which permissions to content with that label.</span></span>
- <span data-ttu-id="35700-117">사용자가 콘텐츠에 레이블을 적용하는 경우 **사용자가 권한을 할당하도록** 허용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="35700-117">**Let users assign permissions** when they apply the label to content.</span></span> <span data-ttu-id="35700-118">이렇게 하면 조직의 사용자가 공동 작업과 작업 수행을 유연하게 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="35700-118">This way, you can allow people in your organization some flexibility that they might need to collaborate and get their work done.</span></span>

<span data-ttu-id="35700-119">암호화 설정은 Microsoft 365 규정 준수 센터, Microsoft 365 보안 센터 또는 Office 365 보안 및 규정 준수 센터에서 민감도 레이블을 만들 때 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="35700-119">The encryption settings are available when you create a sensitivity label in the Microsoft 365 compliance center, Microsoft 365 security center, or Office 365 Security & Compliance Center.</span></span> <span data-ttu-id="35700-120">왼쪽 탐색 창에서 **분류** > **민감도 레이블** > **레이블 만들기**를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="35700-120">In the left nav, choose **Classification** > **Sensitivity label** > **Create a label**.</span></span>

## <a name="how-encryption-works"></a><span data-ttu-id="35700-121">암호화가 작동하는 방식</span><span class="sxs-lookup"><span data-stu-id="35700-121">How encryption works</span></span>

<span data-ttu-id="35700-p105">암호화는 Microsoft Azure AD Rights Management(Azure RMS)를 사용합니다. Azure RMS는 암호화, ID 및 권한 부여 정책을 사용합니다. 자세한 내용은 [Azure 권한 관리 정의](https://docs.microsoft.com/ko-KR/azure/information-protection/what-is-azure-rms)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="35700-p105">Encryption uses Azure Rights Management (Azure RMS). Azure RMS uses encryption, identity, and authorization policies. To learn more, see [What is Azure Rights Management?](https://docs.microsoft.com/ko-KR/azure/information-protection/what-is-azure-rms)</span></span>

## <a name="how-to-turn-on-encryption-for-a-sensitivity-label"></a><span data-ttu-id="35700-125">민감도 레이블의 암호화를 설정하는 방법</span><span class="sxs-lookup"><span data-stu-id="35700-125">How to turn on encryption for a sensitivity label</span></span>

<span data-ttu-id="35700-126">시작하려면 먼저 **암호화**를 **설정**으로 전환하고 아래의 작업 여부를 선택합니다. </span><span class="sxs-lookup"><span data-stu-id="35700-126">To begin, simply toggle **Encryption** to **On**, and then choose whether to:</span></span>

- <span data-ttu-id="35700-127">어떤 사용자에게 해당 레이블이 있는 콘텐츠에 어떤 권한을 부여할 것인지 정확하게 결정할 수 있도록 **지금 권한을 할당**합니다.</span><span class="sxs-lookup"><span data-stu-id="35700-127">**Assign permissions now**, so that you can determine exactly which users get which permissions to content with that label.</span></span> <span data-ttu-id="35700-128">자세한 내용은 다음 섹션 [지금 권한 할당](#assign-permissions-now) 을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="35700-128">For more information, see the next section [Assign permissions now](#assign-permissions-now).</span></span>
- <span data-ttu-id="35700-129">사용자가 콘텐츠에 레이블을 적용하는 경우 **사용자가 권한을 할당하도록** 허용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="35700-129">**Let users assign permissions** when they apply the label to content.</span></span> <span data-ttu-id="35700-130">이렇게 하면 조직의 사용자가 공동 작업과 작업 수행을 유연하게 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="35700-130">This way, you can allow people in your organization some flexibility that they might need to collaborate and get their work done.</span></span> <span data-ttu-id="35700-131">자세한 내용은 아래 섹션 [사용자가 권한을 할당할 수 있도록 허용](#let-users-assign-permissions)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="35700-131">For more information, see the below section [Let users assign permissions](#let-users-assign-permissions).</span></span>

<span data-ttu-id="35700-132">예를 들어, 가장 중요한 콘텐츠에 적용되는 **극비**라는 민감도 레이블을 사용하는 경우 해당 콘텐츠의 사용 권한 유형을 받을 사용자를 결정하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="35700-132">For example, if you have a sensitivity label named **Highly Confidential** that will be applied to your most sensitive content, you may want to decide now who gets what type of permissions to that content.</span></span>

<span data-ttu-id="35700-133">또는 **비즈니스 계약서**라는 민감도 레이블을 사용하고, 사용자 조직의 워크플로에 따라 사용자가 임시로 다른 사용자와 이 콘텐츠에 대해 공동 작업해야 하는 경우, 사용자가 레이블을 지정할 때 권한을 받을 사용자를 결정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="35700-133">Alternatively, if you have a sensitivity label named **Business Contracts**, and your organization's workflow requires that your people collaborate on this content with different people on an ad hoc basis, you may want to allow your users to decide who gets permissions when they assign the label.</span></span> <span data-ttu-id="35700-134">이와 같은 유연성을 갖추어 사용자의 생산성은 향상되고 관리자가 특정 시나리오를 해결하기 위해 새 민감도 레이블을 업데이트하거나 만들어야 하는 요청은 줄일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="35700-134">This flexibility both helps your users' productivity and reduces the requests for your admins to update or create new sensitivity labels to address specific scenarios.</span></span>

![사용자 또는 관리자가 정의한 권한 추가 옵션](media/sensitivity-label-user-or-admin-defined-permissions.png)

## <a name="assign-permissions-now"></a><span data-ttu-id="35700-136">지금 권한 할당</span><span class="sxs-lookup"><span data-stu-id="35700-136">Assign permissions now</span></span>

<span data-ttu-id="35700-137">아래 옵션을 사용하여 이 레이블이 적용되는 전자 메일 또는 문서에 액세스할 수 있는 사용자를 제어합니다.</span><span class="sxs-lookup"><span data-stu-id="35700-137">To begin, simply toggle Encryption to On, and then use the options below to control who can access email or documents to which this label is applied. You can:</span></span> <span data-ttu-id="35700-138">다음을 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="35700-138">You can:</span></span>

1. <span data-ttu-id="35700-p110">**전자 메일과 문서 둘 다에 암호화를 적용하거나 전자 메일에만 적용합니다.** 전자 메일만 선택하면 이 레이블이 있는 메시지가 Outlook에서 암호화되지만 이 레이블이 있는 문서는 Word 또는 PowerPoint와 같은 다른 응용 프로그램에서 암호화되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="35700-p110">**Apply encryption to both email and documents, or just email.** If you choose just email, messages with this label will be encrypted in Outlook, but documents with this label won't be encrypted in other apps, such as Word or PowerPoint.</span></span> 
2. <span data-ttu-id="35700-p111">특정 날짜 또는 레이블을 지정한 후 특정 일수가 지나면 **레이블을 지정한 콘텐츠에 대한 액세스가 만료**되도록 합니다. 이 기간 이후 사용자는 레이블을 지정한 항목을 열 수 없습니다. 날짜를 지정하는 경우 표준 시간대의 해당 날짜 자정에 적용됩니다. 일부 전자 메일 클라이언트의 경우 캐싱 메커니즘으로 인해 만료 기능이 적용되지 않을 수 있으며 만료 날짜가 지난 전자 메일이 표시될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="35700-p111">**Allow access to labeled content to expire**, either on a specific date or after a specific number of days after the label is applied. After this time, users won’t be able to open the labeled item. If you specify a date, it is effective midnight on that date in your current time zone. (Note that some email clients may not enforce expiration and show emails past their expiration date, due to their caching mechanisms.)</span></span>
3. <span data-ttu-id="35700-p112">**오프라인 액세스 허용**을 허용 안 함, 항상 허용 또는 레이블을 적용한 후 특정 일수 동안 허용합니다. 오프라인 액세스를 허용 안 함 또는 며칠로 제한하는 경우 임계값에 도달하면 사용자를 다시 인증해야 하고 액세스 권한이 기록됩니다. 자세한 내용은 권한 관리 사용 라이선스에 대한 다음 섹션을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="35700-p112">**Allow offline access** never, always, or for a specific number of days after the label is applied. If you restrict offline access to never or a number of days, when that threshold is reached, users must be reauthenticated and their access is logged. For more information, see the next section on the Rights Management use license.</span></span>

![관리자가 정의한 권한에 대한 설정](media/sensitivity-encryption-settings-for-admin-defined-permissions.png)

### <a name="rights-management-use-license-for-offline-access"></a><span data-ttu-id="35700-149">오프라인 액세스에 대한 권한 관리 사용 라이선스</span><span class="sxs-lookup"><span data-stu-id="35700-149">Rights Management use license for offline access</span></span>

<span data-ttu-id="35700-p113">사용자가 민감도 레이블로 보호되는 문서 또는 전자 메일을 오프라인으로 열면 사용자에게 해당 콘텐츠에 대한 Microsoft Azure AD Rights Management 사용 라이선스가 부여됩니다. 이 사용 라이선스는 문서 또는 전자 메일에 대한 사용자의 사용 권한 및 콘텐츠를 암호화하는 데 사용된 암호화 키가 포함된 인증서입니다. 사용 라이선스에는 만료 날짜가 설정된 경우 만료 날짜와 사용 라이선스가 유효한 기간이 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="35700-p113">When a user opens a document or email offline that’s been protected by a sensitivity label, an Azure Rights Management use license for that content is granted to the user. This use license is a certificate that contains the user's usage rights for the document or email, and the encryption key that was used to encrypt the content. The use license also contains an expiration date if this has been set, and how long the use license is valid.</span></span>

<span data-ttu-id="35700-p114">만료 날짜가 설정된 경우 테넌트에 대한 기본 사용 라이선스의 유효 기간은 30일입니다. 사용 라이센스 동안 콘텐츠에 대해 다시 인증받지 않습니다. 이를 통해 인터넷에 연결하지 않고도 보호된 문서 또는 전자 메일을 계속 열 수 있습니다. 사용 라이선스 유효 기간이 만료되면 다음에 사용자가 보호된 문서 또는 전자 메일에 액세스할 때 다시 인증받아야 합니다.</span><span class="sxs-lookup"><span data-stu-id="35700-p114">If no expiration date has been set, the default use license validity period for a tenant is 30 days. For the duration of the use license, the user is not reauthenticated or reauthorized for the content. This lets the user continue to open the protected document or email without an Internet connection. When the use license validity period expires, the next time the user accesses the protected document or email, the user must be reauthenticated and reauthorized.</span></span>

<span data-ttu-id="35700-p115">재인증 외에도 정책 및 사용자 그룹 구성원 자격이 다시 평가됩니다. 즉, 사용자가 마지막으로 콘텐츠에 액세스한 시점에서 정책이나 그룹 구성원에 변경된 사항이 있는 경우 사용자에게 동일한 문서 또는 전자 메일에 대해 다른 액세스 결과를 제공할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="35700-p115">In addition to reauthentication, the policy and user group membership is reevaluated. This means that users could experience different access results for the same document or email if there are changes in the policy or group membership from when they last accessed the content.</span></span>

<span data-ttu-id="35700-159">기본값 30일 설정을 변경하는 방법을 알아보려면 [권한 관리 사용 라이선스](https://docs.microsoft.com/ko-KR/azure/information-protection/configure-usage-rights#rights-management-use-license)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="35700-159">To learn how to change the default 30-day setting, see [Rights Management use license](https://docs.microsoft.com/ko-KR/azure/information-protection/configure-usage-rights#rights-management-use-license).</span></span>

### <a name="assign-permissions-to-specific-users-or-groups"></a><span data-ttu-id="35700-160">특정 사용자 또는 그룹에 사용 권한 할당</span><span class="sxs-lookup"><span data-stu-id="35700-160">Assign permissions to specific users or groups</span></span>

<span data-ttu-id="35700-161">특정 사용자만 레이블이 지정된 콘텐츠와 상호 작용할 수 있도록 사용 권한을 부여할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="35700-161">You can grant permissions to specific people so that only they can interact with the labeled content.</span></span>

<span data-ttu-id="35700-162">다음의 2단계로 간단하게 진행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="35700-162">Doing so is a straightforward two-step process:</span></span>

1. <span data-ttu-id="35700-163">먼저 사용 권한을 할당할 사용자 또는 그룹을 레이블이 지정된 콘텐츠에 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="35700-163">First you add users or groups that will be assigned permissions to the labeled content.</span></span>
2. <span data-ttu-id="35700-164">그런 다음 해당 사용자가 레이블이 지정된 콘텐츠에 대한 사용 권한을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="35700-164">Then you choose which permissions those users have for the labeled content.</span></span>

![사용자에게 사용 권한을 할당하는 옵션](media/Sensitivity-Assign-permissions-settings.png)

#### <a name="add-users-or-groups"></a><span data-ttu-id="35700-166">사용자 또는 그룹 추가</span><span class="sxs-lookup"><span data-stu-id="35700-166">Add users or groups</span></span>

<span data-ttu-id="35700-167">권한을 할당할 때 다음을 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="35700-167">When you assign permissions, you can choose:</span></span>

- <span data-ttu-id="35700-p116">조직의 모든 사용자(모든 테넌트 구성원). 이 설정에서는 게스트 계정이 제외됩니다.</span><span class="sxs-lookup"><span data-stu-id="35700-p116">Everyone in your organization (all tenant members). This setting excludes guest accounts.</span></span>
- <span data-ttu-id="35700-170">모든 특정 사용자 또는 전자 메일 사용이 가능한 보안 그룹, 메일 그룹, Office 365 그룹 또는 동적 메일 그룹.</span><span class="sxs-lookup"><span data-stu-id="35700-170">Any specific user or email-enabled security group, distribution group, Office 365 group, or dynamic distribution group.</span></span> 
- <span data-ttu-id="35700-171">조직 외부의 모든 이메일 주소 또는 도메인(예: gmail.com, hotmail.com 또는 outlook.com).</span><span class="sxs-lookup"><span data-stu-id="35700-171">Any email address or domain outside your organization, such as gmail.com, hotmail.com, or outlook.com.</span></span>

<span data-ttu-id="35700-172">모든 테넌트 구성원을 선택하거나 디렉토리를 탐색할 때 사용자 또는 그룹에 전자 메일 주소가 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="35700-172">When you choose all tenant members or browse the directory, the users or groups must have an email address.</span></span>

<span data-ttu-id="35700-p117">모범 사례로 사용자 대신 그룹을 사용할 수 있습니다. 이 전략으로 더 간단하게 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="35700-p117">As a best practice, use groups rather than users. This strategy keeps your configuration simpler.</span></span>

#### <a name="choose-permissions"></a><span data-ttu-id="35700-175">사용 권한 선택</span><span class="sxs-lookup"><span data-stu-id="35700-175">Choose permissions</span></span>

<span data-ttu-id="35700-176">해당 사용자 또는 그룹에 허용할 사용 권한을 선택하면 다음 중 하나를 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="35700-176">When you choose which permissions to allow for those users or groups, you can select either:</span></span>

- <span data-ttu-id="35700-177">미리 설정된 권한 그룹(예: 공동 작성 또는 검토자)이 있는 [미리 정의된 권한 수준](https://docs.microsoft.com/ko-KR/azure/information-protection/configure-usage-rights#rights-included-in-permissions-levels).</span><span class="sxs-lookup"><span data-stu-id="35700-177">A [predefined permissions level](https://docs.microsoft.com/ko-KR/azure/information-protection/configure-usage-rights#rights-included-in-permissions-levels) with a preset group of rights, such as Co-Author or Reviewer.</span></span>
- <span data-ttu-id="35700-178">원하는 사용 권한을 선택해 허용할 수 있는 사용자 지정 권한 그룹.</span><span class="sxs-lookup"><span data-stu-id="35700-178">A Custom group of rights, where you choose whichever permissions you want.</span></span>

<span data-ttu-id="35700-179">각 특정 사용 권한에 대한 자세한 내용은 [사용 권한 및 설명](https://docs.microsoft.com/ko-KR/azure/information-protection/configure-usage-rights#usage-rights-and-descriptions)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="35700-179">For more information on each specific permission, see [Usage rights and descriptions](https://docs.microsoft.com/ko-KR/azure/information-protection/configure-usage-rights#usage-rights-and-descriptions).</span></span>  

![미리 설정된 옵션 또는 사용자 지정 사용 권한](media/Sensitivity-Choose-permissions-settings.png)

<span data-ttu-id="35700-p118">동일한 레이블로 다른 사용자에게 다른 권한을 부여할 수 있습니다. 예를 들어 아래 그림과 같이 단일 레이블로 일부 사용자를 검토자로 다른 사용자를 공동 작성자로 할당할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="35700-p118">Note that the same label can grant different permissions to different users. For example, a single label can assign some users as Reviewer and a different user as Co-author, as shown below.</span></span>

<span data-ttu-id="35700-p119">이를 위해서는 사용자 또는 그룹을 추가하고 사용 권한을 할당하고 해당 설정을 저장합니다. 그런 다음 매번 이 단계를 반복하여 사용자를 추가하고 권한을 할당하고 설정을 저장합니다. 이 작업을 필요한 만큼 수행하여 여러 사용자에게 서로 다른 권한을 정의할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="35700-p119">To do this, add users or groups, assign them permissions, and save those settings. Then repeat these steps, adding users and assigning them permissions, saving the settings each time. You can do this as often as necessary, to define different permissions for different users.</span></span>

![다른 사용 권한을 가진 다른 사용자](media/Sensitivity-Multiple-users-permissions.png)

#### <a name="rights-management-issuer-user-applying-the-sensitivity-label-always-has-full-control"></a><span data-ttu-id="35700-187">권한 관리 발급자(민감도 레이블을 적용한 사용자)는 항상 모든 권한을 갖습니다</span><span class="sxs-lookup"><span data-stu-id="35700-187">Rights Management issuer (user applying the sensitivity label) always has Full Control</span></span>

<span data-ttu-id="35700-p120">민감도 레이블의 암호화는 Azure RMS를 사용합니다. 사용자가 Azure RMS를 사용하여 문서 또는 전자 메일을 보호하기 위해 중요도 레이블을 적용하면 해당 사용자는 해당 내용에 대한 권한 관리 발급자가 됩니다.</span><span class="sxs-lookup"><span data-stu-id="35700-p120">Encryption for a sensitivity label uses Azure RMS. When a user applies a sensitivity label to protect a document or email by using Azure RMS, that user becomes the Rights Management issuers for that content.</span></span>

<span data-ttu-id="35700-190">권한 관리 발급자는 문서 또는 전자 메일에 대한 모든 권한을 항상 부여받으며, 또한 다음과 같은 권한을 갖습니다.</span><span class="sxs-lookup"><span data-stu-id="35700-190">The Rights Management issuer is always granted Full Control permissions for the document or email, and in addition:</span></span>

- <span data-ttu-id="35700-191">보호 설정에 만료 날짜가 포함된 경우 권한 관리 발급자는 해당 날짜 이후에도 여전히 문서 또는 전자 메일을 열고 편집할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="35700-191">If the protection settings include an expiration date, the Rights Management issuer can still open and edit the document or email after that date.</span></span>
- <span data-ttu-id="35700-192">권한 관리 발급자는 문서 또는 전자 메일을 언제든지 오프라인으로 액세스할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="35700-192">The Rights Management issuer can always access the document or email offline.</span></span>
- <span data-ttu-id="35700-193">권한 관리 발급자는 권한이 해지된 후에도 문서를 열 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="35700-193">The Rights Management issuer can still open a document after it is revoked.</span></span>

<span data-ttu-id="35700-194">자세한 내용은 [권한 관리 발급자 및 권한 관리 소유자](https://docs.microsoft.com/ko-KR/azure/information-protection/configure-usage-rights#rights-management-issuer-and-rights-management-owner)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="35700-194">For more information, see [Rights Management issuer and Rights Management owner](https://docs.microsoft.com/ko-KR/azure/information-protection/configure-usage-rights#rights-management-issuer-and-rights-management-owner).</span></span>

## <a name="let-users-assign-permissions"></a><span data-ttu-id="35700-195">사용자가 권한을 할당하도록 허용</span><span class="sxs-lookup"><span data-stu-id="35700-195">Let users assign permissions</span></span>

<span data-ttu-id="35700-196">다음 옵션을 사용하여 사용자가 민감도 레이블을 콘텐츠에 수동으로 추가할 때 사용자가 권한을 할당하도록 허용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="35700-196">You can use these options to let users assign permissions when they manually apply a sensitivity label to content:</span></span>

- <span data-ttu-id="35700-197">Outlook에서, **전달 금지** 옵션과 동등한 제한 사항을 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="35700-197">In Outlook, a user can enforce restrictions equivalent to the **Do Not Forward** option.</span></span> <span data-ttu-id="35700-198">이 옵션은 Windows용 Outlook에서 기본적으로 지원되며 Azure Information Protection 통합 레이블 지정 클라이언트를 설치할 필요가 없습니다.</span><span class="sxs-lookup"><span data-stu-id="35700-198">This option is supported natively in Outlook on Windows, and does not require you to install the Azure Information Protection unified labeling client.</span></span>
- <span data-ttu-id="35700-199">Word, PowerPoint 및 Excel의 경우, 특정 사용자, 그룹 또는 조직에 대한 권한 수준을 선택하라는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="35700-199">In Word, PowerPoint, and Excel, a user is prompted to select a permission level for specific users, groups, or organizations.</span></span> <span data-ttu-id="35700-200">이 옵션은 이 Office 앱에서 기본적으로 지원되지 않으므로 Azure Information Protection 통합 레이블 지정 클라이언트를 설치해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="35700-200">This option is not supported natively in these Office apps, so your users must install the Azure Information Protection unified labeling client.</span></span>

<span data-ttu-id="35700-201">다음 옵션에서는 민감도 레이블이 표시될 앱을 결정합니다.</span><span class="sxs-lookup"><span data-stu-id="35700-201">These options determine in which apps the sensitivity label will appear:</span></span>

- <span data-ttu-id="35700-202">민감도 레이블에 Outlook 옵션만 활성화된 경우, 레이블이 Outlook에서만 사용자에게만 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="35700-202">If the sensitivity label has only the Outlook option enabled, the label will appear to users only in Outlook.</span></span>
- <span data-ttu-id="35700-203">민감도 레이블에 Word, PowerPoint 및 Excel 옵션만 활성화된 경우, 레이블이 해당 앱에서만 사용자에게 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="35700-203">If the sensitivity label has only the Word, PowerPoint, and Excel option enabled, the label will appear to users only in those apps.</span></span>
- <span data-ttu-id="35700-204">민감도 레이블에 두 옵션이 모두 활성화된 경우, 사용 가능한 모든 앱(Outlook, Word, PowerPoint 및 Excel)에서 레이블이 사용자에게 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="35700-204">If the sensitivity label has both options enabled, the label will appear to users in all of the available apps: Outlook, Word, PowerPoint, and Excel.</span></span>

<span data-ttu-id="35700-205">사용자가 권한을 할당할 수 있도록 허용하는 민감도 레이블은 사용자가 수동으로만 콘텐츠에 적용할 수 있으므로, 이를 추천 레이블로 자동 적용 또는 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="35700-205">A sensitivity label that lets users assign permissions can be applied to content only manually by users; it can't be auto-applied or used as a recommended label.</span></span>

> [!NOTE]
> <span data-ttu-id="35700-206">사용자가 권한을 할당하도록 허용하려면 Azure Information Protection 구독이 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="35700-206">Letting users assign permissions requires an Azure Information Protection subscription.</span></span> <span data-ttu-id="35700-207">Word, PowerPoint 및 Excel에서 이 기능을 사용하려면 [Azure Information Protection 통합 레이블 지정 클라이언트](https://docs.microsoft.com/azure/information-protection/rms-client/install-unifiedlabelingclient-app)를 다운로드하여 설치해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="35700-207">To use this feature in Word, PowerPoint, and Excel, you must download and install the [Azure Information Protection unified labeling client](https://docs.microsoft.com/azure/information-protection/rms-client/install-unifiedlabelingclient-app).</span></span> <span data-ttu-id="35700-208">Office 앱에서 이 기능에 대한 기본 지원에 대해 작업하고 있으므로 Azure Information Protection 클라이언트를 사용하지 않아도 됩니다.</span><span class="sxs-lookup"><span data-stu-id="35700-208">We're working on native support for this feature in these Office apps, so that they won't require the Azure Information Protection client.</span></span> <span data-ttu-id="35700-209">또한, 클라이언트는 Windows에서만 실행되므로 Mac, iOS, Android 또는 웹용 Office에서는 이 기능이 아직 지원되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="35700-209">Also, the client runs only on Windows, so this feature is not yet supported on Mac, iOS, Android, or Office for the web.</span></span>

![사용자 정의 권한에 대한 암호화 설정](media/sensitivity-encryption-settings-for-user-defined-permissions.png)

### <a name="outlook-restrictions"></a><span data-ttu-id="35700-211">Outlook 제한 사항</span><span class="sxs-lookup"><span data-stu-id="35700-211">Outlook restrictions</span></span>

<span data-ttu-id="35700-212">Outlook에서, 사용자가 메시지에 권한을 할당하도록 허용하는 민감도 레이블을 적용하는 경우 이 제한 사항은 전달 금지 옵션과 동일합니다.</span><span class="sxs-lookup"><span data-stu-id="35700-212">In Outlook, when a user applies a sensitivity label that lets them assign permissions to a message, the restrictions are the same as the Do Not Forward option.</span></span> <span data-ttu-id="35700-213">사용자에게 메시지 맨 위에 레이블 이름과 설명이 표시됩니다. 이는 콘텐츠가 보호되고 있음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="35700-213">The user will see the label name and description at the top of the message, which indicates the content's being protected.</span></span> <span data-ttu-id="35700-214">Word, PowerPoint 및 Excel([다음 섹션](#word-powerpoint-and-excel-permissions) 참조)과 달리, 사용자에게 특정 권한을 선택 하라는 메시지가 표시되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="35700-214">Unlike Word, PowerPoint, and Excel (see the [next section](#word-powerpoint-and-excel-permissions)), users aren't prompted to select specific permissions.</span></span>

![Outlook의 메시지에 적용된 민감도 레이블](media/sensitivity-label-outlook-protection-applied.png)

<span data-ttu-id="35700-216">전달 금지 옵션이 전자 메일에 적용되는 경우, 전자 메일이 암호화되므로 받는 사람을 인증해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="35700-216">When the Do Not Forward option is applied to an email, the email is encrypted and recipients must be authenticated.</span></span> <span data-ttu-id="35700-217">그런 다음, 받는 사람이 이를 전달하거나, 인쇄하거나, 복사할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="35700-217">Then, the recipients cannot forward it, print it, or copy from it.</span></span> <span data-ttu-id="35700-218">예를 들어, Outlook 클라이언트에서 전달 단추를 사용할 수 없고, 다른 이름으로 저장 및 인쇄 메뉴 옵션도 사용할 수 없으며, 받는 사람, 참조 또는 숨은 참조 상자에서 받는 사람을 추가하거나 변경할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="35700-218">For example, in the Outlook client, the Forward button is not available, the Save As and Print menu options are not available, and you cannot add or change recipients in the To, Cc, or Bcc boxes.</span></span>

<span data-ttu-id="35700-219">전자 메일에 첨부된 보호되지 않는 Office 문서는 자동으로 동일한 제한 사항을 상속합니다.</span><span class="sxs-lookup"><span data-stu-id="35700-219">Unprotected Office documents that are attached to the email automatically inherit the same restrictions.</span></span> <span data-ttu-id="35700-220">이 문서에 적용되는 사용 권한은 콘텐츠 편집, 편집, 저장, 보기, 열기, 읽기, 모든 매크로입니다.</span><span class="sxs-lookup"><span data-stu-id="35700-220">The usage rights applied to these documents are Edit Content, Edit; Save; View, Open, Read; and Allow Macros.</span></span> <span data-ttu-id="35700-221">사용자가 첨부 파일에 대해 다른 권한을 요구하는 경우 또는 첨부 파일이 상속된 보호를 지원하는 Office 문서가 아닌 경우, 사용자가 파일을 전자 메일에 첨부하기 전에 파일을 보호해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="35700-221">If the user wants different usage rights for an attachment, or the attachment is not an Office document that supports this inherited protection, the user needs to protect the file before attaching it to the email.</span></span>

### <a name="word-powerpoint-and-excel-permissions"></a><span data-ttu-id="35700-222">Word, PowerPoint 및 Excel 권한</span><span class="sxs-lookup"><span data-stu-id="35700-222">Word, PowerPoint, and Excel permissions</span></span>

<span data-ttu-id="35700-223">Word, PowerPoint 및 Excel에서, 사용자가 문서에 권한을 할당하도록 허용하는 민감도 레이블을 적용하는 경우, 아래에 표시된 대로 콘텐츠를 보호하라는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="35700-223">In Word, PowerPoint, and Excel, when a user applies a sensitivity label that lets them assign permissions to a document, they are prompted to protect the content as shown below.</span></span>

<span data-ttu-id="35700-224">사용자는 다음을 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="35700-224">The user can modify records.</span></span>

- <span data-ttu-id="35700-225">뷰어(보기 전용 권한 할당) 또는 공동 작성자(보기, 편집, 복사 및 인쇄 권한 할당)와 같은 권한 수준을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="35700-225">Select a permission level, such as Viewer (which assigns View Only permission) or Co-Author (which assigns View, Edit, Copy, and Print permissions).</span></span>
- <span data-ttu-id="35700-226">사용자, 그룹 또는 조직을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="35700-226">Select users, groups, or organizations.</span></span> <span data-ttu-id="35700-227">여기에는 조직의 내부 또는 외부 사용자가 모두 포함될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="35700-227">This can include people both inside or outside your organizations.</span></span>
- <span data-ttu-id="35700-228">선택한 사용자가 콘텐츠에 액세스할 수 없는 만료 날짜를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="35700-228">Set an expiration date, after which the selected users cannot access the content.</span></span> <span data-ttu-id="35700-229">자세한 내용은 위에 있는 섹션 [오프라인 액세스용 권한 관리 사용자 라이선스](#rights-management-use-license-for-offline-access)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="35700-229">For more information, see the above section [Rights Management use license for offline access](#rights-management-use-license-for-offline-access).</span></span>

![사용자 지정 권한을 사용하여 보호하기 위한 옵션](media/sensitivity-aip-custom-permissions-dialog.png)

## <a name="what-happens-to-existing-encryption-when-a-labels-applied"></a><span data-ttu-id="35700-231">레이블이 적용되면 기존 암호화는 어떻게 되나요?</span><span class="sxs-lookup"><span data-stu-id="35700-231">What happens to existing encryption when a label's applied</span></span>

<span data-ttu-id="35700-232">민감도 레이블이 콘텐츠에 적용되기 전에, 일부 다른 보호 설정을 적용하여 콘텐츠를 암호화하는 것이 가능합니다.</span><span class="sxs-lookup"><span data-stu-id="35700-232">Before a sensitivity label is applied to content, it's possible that a user already encrypted the content by applying some other protection setting.</span></span> <span data-ttu-id="35700-233">예를 들어 다음 기능을 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="35700-233">For example, a user might have applied:</span></span>

- <span data-ttu-id="35700-234">**전달 금지** 옵션.</span><span class="sxs-lookup"><span data-stu-id="35700-234">The **Do Not Forward** option.</span></span>
- <span data-ttu-id="35700-235">Azure Information Protection 통합된 레이블 지정 클라이언트를 사용하여 사용자 지정 보호합니다.</span><span class="sxs-lookup"><span data-stu-id="35700-235">Custom protection by using the Azure Information Protection unified labeling client.</span></span>
- <span data-ttu-id="35700-236">콘텐츠를 암호화하지만 레이블과 관련이 없는 Azure RMS(Rights Management Service) 서식 파일입니다.</span><span class="sxs-lookup"><span data-stu-id="35700-236">An Azure Rights Management Service (RMS) template that encrypts the content but is not associated with a label.</span></span>

<span data-ttu-id="35700-237">이 테이블에서는 민감도 레이블이 해당 콘텐츠에 적용되는 경우 기존 암호화가 어떻게 되는지에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="35700-237">This table describe what happens to existing encyption when a sensitivity label is applied to that content.</span></span>
<br/>
<br/>

| |<span data-ttu-id="35700-238">**암호화가 해제된 민감도 레이블을 적용**</span><span class="sxs-lookup"><span data-stu-id="35700-238">**User applies a sensitivity label with encryption turned off**</span></span>|<span data-ttu-id="35700-239">**사용자 설정 되어 암호화로 민감도 레이블을 적용**</span><span class="sxs-lookup"><span data-stu-id="35700-239">**User applies a sensitivity label with encryption turned on**</span></span>|<span data-ttu-id="35700-240">**보호 제거를 사용하여 레이블을 적용**<sup>1</sup></span><span class="sxs-lookup"><span data-stu-id="35700-240">**User applies a label with Remove Protection**<sup>1</sup></span></span>|
|:-----|:-----|:-----|:-----|
|<span data-ttu-id="35700-241">**전달 금지**</span><span class="sxs-lookup"><span data-stu-id="35700-241">**Do Not Forward**</span></span>|<span data-ttu-id="35700-242">전자 메일 - 보호가 제거됨</span><span class="sxs-lookup"><span data-stu-id="35700-242">Email - Protection is removed</span></span><br/><span data-ttu-id="35700-243">문서 - 보호가 유지됨</span><span class="sxs-lookup"><span data-stu-id="35700-243">Document - Protection is preserved</span></span>|<span data-ttu-id="35700-244">레이블 보호가 적용됨</span><span class="sxs-lookup"><span data-stu-id="35700-244">Label protection is applied</span></span>|<span data-ttu-id="35700-245">**전달 금지**가 제거됨</span><span class="sxs-lookup"><span data-stu-id="35700-245">**Do Not Forward** is removed</span></span>|
|<span data-ttu-id="35700-246">**사용자 지정 보호**<sup>1</sup></span><span class="sxs-lookup"><span data-stu-id="35700-246">**Custom protection**<sup>1</sup></span></span>|<span data-ttu-id="35700-247">보호가 유지됨</span><span class="sxs-lookup"><span data-stu-id="35700-247">Protection is preserved</span></span>|<span data-ttu-id="35700-248">레이블 보호가 적용됨</span><span class="sxs-lookup"><span data-stu-id="35700-248">Label protection is applied</span></span>|<span data-ttu-id="35700-249">사용자 지정 보호가 제거됨</span><span class="sxs-lookup"><span data-stu-id="35700-249">Custom protection is removed</span></span>|
|<span data-ttu-id="35700-250">**Azure RMS 서식 파일**</span><span class="sxs-lookup"><span data-stu-id="35700-250">**Azure RMS template**</span></span>|<span data-ttu-id="35700-251">보호가 유지됨</span><span class="sxs-lookup"><span data-stu-id="35700-251">Protection is preserved</span></span>|<span data-ttu-id="35700-252">레이블 보호가 적용됨</span><span class="sxs-lookup"><span data-stu-id="35700-252">Label protection is applied</span></span>|<span data-ttu-id="35700-253">사용자 지정 보호가 제거됨</span><span class="sxs-lookup"><span data-stu-id="35700-253">Custom protection is removed</span></span>|

<span data-ttu-id="35700-254"><sup>1</sup>이 기능은 Azure Information Protection 레이블 지정 클라이언트에서만 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="35700-254"><sup>1</sup>This is supported only in the Azure Information Protection labeling client.</span></span>

## <a name="storing-encrypted-content-in-onedrive-and-sharepoint"></a><span data-ttu-id="35700-255">OneDrive 및 SharePoint에 암호화된 콘텐츠 저장</span><span class="sxs-lookup"><span data-stu-id="35700-255">Storing encrypted content in OneDrive and SharePoint</span></span>

<span data-ttu-id="35700-p130">OneDrive 및 SharePoint에 저장된 파일에 암호화가 적용되어 있으면 이 파일의 내용을 처리할 수 없습니다. 즉 공동 작성, eDiscovery, 검색, Delve 및 기타 공동 작업 기능이 작동하지 않습니다. 또한 DLP(데이터 손실 방지) 정책은 메타데이터(Office 365 레이블 포함)에만 작동할 수 있지만 암호화된 파일의 내용(예: 파일 내의 신용 카드 번호)에는 작동할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="35700-p130">Be aware that when encryption is applied to files stored in OneDrive and SharePoint, the service cannot process the contents of these files. This means that features such as co-authoring, eDiscovery, search, Delve, and other collaborative features do not work. Also, data loss prevention (DLP) policies can work only with the metadata (including Office 365 labels) but not the contents of encrypted files (such as credit card numbers within files).</span></span>

<span data-ttu-id="35700-p131">이는 OneDrive 및 SharePoint에 저장된 콘텐츠에만 적용됩니다. Exchange Online에서 메일 흐름 규칙(전송 규칙이라고도 함)은 [수퍼 사용자 계정](https://docs.microsoft.com/ko-KR/azure/information-protection/configure-super-users)을 사용하여 암호화된 콘텐츠를 검사하고 DLP 정책을 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="35700-p131">This applies only to content stored in OneDrive and SharePoint. In Exchange Online, mail flow rules (also known as transport rules) use the [super user account](https://docs.microsoft.com/ko-KR/azure/information-protection/configure-super-users) so that they can scan encrypted content and enforce DLP policies.</span></span>

## <a name="important-prerequisites"></a><span data-ttu-id="35700-261">중요한 필수 구성 요소</span><span class="sxs-lookup"><span data-stu-id="35700-261">Important prerequisites</span></span>

<span data-ttu-id="35700-262">암호화를 사용하려면 먼저 이러한 작업을 수행해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="35700-262">Before you can use encryption, you might need to perform these tasks.</span></span>

### <a name="activating-azure-rights-management"></a><span data-ttu-id="35700-263">Microsoft Azure AD Rights Management 활성화</span><span class="sxs-lookup"><span data-stu-id="35700-263">Activating Azure Rights Management</span></span>

<span data-ttu-id="35700-p132">민감도 레이블에 암호화를 사용하려면 테넌트에서 Azure 권한 관리 서비스를 활성화해야 합니다. 최신 테넌트의 경우 기본적으로 서비스가 활성화되어 있지만 수동으로 서비스를 활성화해야 할 수 있습니다. 자세한 내용은 [Microsoft Azure AD Rights Management 활성화](https://docs.microsoft.com/ko-KR/azure/information-protection/activate-service)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="35700-p132">To use encryption in sensitivity labels, the Azure Rights Management service needs to be activated in your tenant. In newer tenants, the service is on by default, but you might need to manually activate the service. For more information, see [Activating Azure Rights Management](https://docs.microsoft.com/ko-KR/azure/information-protection/activate-service).</span></span>

### <a name="configure-exchange-for-azure-information-protection"></a><span data-ttu-id="35700-267">Azure Information Protection에 대한 Exchange 구성</span><span class="sxs-lookup"><span data-stu-id="35700-267">Configure Exchange for Azure Information Protection</span></span>

<span data-ttu-id="35700-p133">사용자가 전자 메일을 보호하기 위해 Outlook에서 레이블을 적용하기 전에 Exchange에서 Azure 정보 보호를 구성할 필요가 없습니다. 그러나 Exchange에서 Microsoft Azure Information Protection을 구성하기 전까지 Exchange에서 Microsoft Azure AD Rights Management을 사용하는 모든 기능을 온전히 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="35700-p133">Exchange does not have to be configured for Azure Information Protection before users can apply labels in Outlook to protect their emails. However, until Exchange is configured for Azure Information Protection, you do not get the full functionality of using Azure Rights Management protection with Exchange.</span></span>
 
<span data-ttu-id="35700-270">예를 들어 사용자는 휴대폰 또는 웹용 Outlook에서 보호된 전자 메일을 볼 수 없으며 검색 시 보호된 전자 메일이 인덱싱되지 않으며 권한 관리 보호를 위한 Exchange Online DLP를 구성할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="35700-270">For example, users cannot view protected emails on mobile phones or with Outlook on the web, protected emails cannot be indexed for search, and you cannot configure Exchange Online DLP for Rights Management protection.</span></span> 

<span data-ttu-id="35700-271">Exchange에서 이러한 추가 시나리오를 지원할 수 있는지 확인하려면 다음을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="35700-271">To ensure that Exchange can support these additional scenarios, see the following:</span></span>

- <span data-ttu-id="35700-272">Exchange Online의 경우 [Exchange Online: IRM 구성](https://docs.microsoft.com/ko-KR/azure/information-protection/configure-office365#exchange-online-irm-configuration)에 대한 설명서를 참고하세요.</span><span class="sxs-lookup"><span data-stu-id="35700-272">For Exchange Online, see the instructions for [Exchange Online: IRM Configuration](https://docs.microsoft.com/ko-KR/azure/information-protection/configure-office365#exchange-online-irm-configuration).</span></span>
- <span data-ttu-id="35700-273">Exchange 온-프레미스의 경우 [RMS 커넥터를 배포하고 Exchange 서버를 구성](https://docs.microsoft.com/ko-KR/azure/information-protection/deploy-rms-connector)해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="35700-273">For Exchange on-premises, you must deploy the [RMS connector and configure your Exchange servers](https://docs.microsoft.com/ko-KR/azure/information-protection/deploy-rms-connector).</span></span> 
