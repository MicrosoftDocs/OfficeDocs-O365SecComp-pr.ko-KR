---
title: Office 365 앱용 조건부 액세스 앱 컨트롤 배포
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.reviewer: alesibov
ms.audience: Admin
ms.topic: reference
ms.date: 02/27/2019
ms.service: O365-seccomp
localization_priority: Normal
description: Office 365 Cloud app Security 조건부 Access 앱 컨트롤에서 제어할 Azure AD Office 365 앱을 구성 하려면 다음 단계를 수행 합니다.
ms.openlocfilehash: 74cc415220282491694bf417a6761fd43a6d3521
ms.sourcegitcommit: e23b84ef4eee9cccec7205826b71ddfe9aaac2f8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33402946"
---
# <a name="deploy-conditional-access-app-control-for-office-365-apps"></a><span data-ttu-id="b423d-103">Office 365 앱용 조건부 액세스 앱 컨트롤 배포</span><span class="sxs-lookup"><span data-stu-id="b423d-103">Deploy Conditional Access App Control for Office 365 apps</span></span>

|<span data-ttu-id="b423d-104">계산 \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="b423d-104">\*\*\*\*Evaluation\*\* \>\*\*</span></span>|<span data-ttu-id="b423d-105">계획 \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="b423d-105">\*\*\*\*Planning\*\* \>\*\*</span></span>|<span data-ttu-id="b423d-106">배포 \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="b423d-106">\*\*\*\*Deployment\*\* \>\*\*</span></span>|<span data-ttu-id="b423d-107">사용률 \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="b423d-107">\*\*\*\*Utilization\*\*\*\*</span></span>|
|:-----|:-----|:-----|:-----|
|[<span data-ttu-id="b423d-108">평가 시작</span><span class="sxs-lookup"><span data-stu-id="b423d-108">Start evaluating</span></span>](office-365-cas-overview.md) <br/> |[<span data-ttu-id="b423d-109">계획 시작</span><span class="sxs-lookup"><span data-stu-id="b423d-109">Start planning</span></span>](get-ready-for-office-365-cas.md) <br/> |<span data-ttu-id="b423d-110">사용자가 여기 있어!</span><span class="sxs-lookup"><span data-stu-id="b423d-110">You are here!</span></span>  <br/> [<span data-ttu-id="b423d-111">다음 단계</span><span class="sxs-lookup"><span data-stu-id="b423d-111">Next step</span></span>](ocas-session-policies.md) <br/> |[<span data-ttu-id="b423d-112">활용 시작</span><span class="sxs-lookup"><span data-stu-id="b423d-112">Start utilizing</span></span>](utilization-activities-for-ocas.md) <br/> |

<span data-ttu-id="b423d-113">Office 365 Cloud app Security 조건부 Access 앱 컨트롤에서 제어할 Azure AD Office 365 앱을 구성 하려면 다음 단계를 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="b423d-113">Follow these steps to configure Azure AD Office 365 apps to be controlled by Office 365 Cloud App Security Conditional Access App Control.</span></span>

<span data-ttu-id="b423d-114">**1 단계: [Azure AD 조건부 액세스 테스트 정책 만들기](#step-1-create-an-azure-ad-conditional-access-test-policy)**</span><span class="sxs-lookup"><span data-stu-id="b423d-114">**Step 1: [Create an Azure AD conditional access test policy](#step-1-create-an-azure-ad-conditional-access-test-policy)**</span></span>

<span data-ttu-id="b423d-115">**2 단계: [범위가 지정 된 사용자를 앱에서 정책으로 로그인](#step-2-sign-in-with-a-user-scoped-to-the-policy-in-the-apps)**</span><span class="sxs-lookup"><span data-stu-id="b423d-115">**Step 2: [Sign in with a user scoped to the policy in the apps](#step-2-sign-in-with-a-user-scoped-to-the-policy-in-the-apps)**</span></span>

<span data-ttu-id="b423d-116">**3 단계: Azure AD에서 기본 제공 클라우드 앱 보안 정책을 선택 하지 않았거나 추천 되지 않은 앱에 정책을 적용 하려면 [Cloud App Security 포털에서 고급 컨트롤을 구성 합니다](#step-3-configure-advanced-controls-in-the-cloud-app-security-portal) .**</span><span class="sxs-lookup"><span data-stu-id="b423d-116">**Step 3: If you did not select a built-in Cloud App Security policy in Azure AD or if you want to apply the policy to a non-featured app, [Configure advanced controls in the Cloud App Security portal](#step-3-configure-advanced-controls-in-the-cloud-app-security-portal)**</span></span>

<span data-ttu-id="b423d-117">**4 단계: [배포 테스트](#step-4-test-the-deployment)**</span><span class="sxs-lookup"><span data-stu-id="b423d-117">**Step 4: [Test the deployment](#step-4-test-the-deployment)**</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b423d-118">office 365 앱에 대해 조건부 Access 앱 컨트롤을 배포 하려면 office 365 Cloud App Security license 뿐만 아니라  [Azure AD Premium P1에 대 한 유효한 라이선스가](https://docs.microsoft.com/azure/active-directory/license-users-groups)필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="b423d-118">To deploy Conditional Access App Control for Office 365 apps, you need a valid [license for Azure AD Premium P1](https://docs.microsoft.com/azure/active-directory/license-users-groups) as well as a Office 365 Cloud App Security license.</span></span>

## <a name="step-1-create-an-azure-ad-conditional-access-test-policy"></a><span data-ttu-id="b423d-119">1 단계: Azure AD 조건부 액세스 테스트 정책 만들기</span><span class="sxs-lookup"><span data-stu-id="b423d-119">Step 1: Create an Azure AD conditional access test policy</span></span> 

1. <span data-ttu-id="b423d-120">Azure Active Directory의 **보안**에서 **조건부 액세스**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="b423d-120">In Azure Active Directory, under **Security**, click on **Conditional access**.</span></span>

2. <span data-ttu-id="b423d-121"> *\*새 정책을** 클릭 하 고 새 정책을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b423d-121">Click **New policy** and create a new policy.</span></span>

3. <span data-ttu-id="b423d-122">테스트 정책의 **사용자**에서 초기 로그온 및 확인에 사용할 수 있는 테스트 사용자 또는 사용자를 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="b423d-122">In the TEST policy, under **Users**, assign a test user or user that can be used for an initial sign-on and verification.</span></span>

4. <span data-ttu-id="b423d-123">테스트 정책의 **클라우드 앱**에서 제어할 앱을 조건부 액세스 앱 컨트롤로 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="b423d-123">In the TEST policy, under **Cloud app**, assign the apps you want to control with Conditional Access App Control.</span></span>

5. <span data-ttu-id="b423d-124"> *\*세션*\*에서 기본 제공 정책 중 하나를 사용 하도록 정책을 설정 하 고, *\*모니터 전용** 또는 *\*다운로드를 차단*\*합니다.</span><span class="sxs-lookup"><span data-stu-id="b423d-124">Under **Session**, set the policy to use either of the built-in policies, **Monitor only** or **Block downloads**.</span></span> <span data-ttu-id="b423d-125">또는 Cloud App Security portal에서 고급 정책을 설정 하려면 **사용자 지정 정책을** 사용 합니다 .를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="b423d-125">Or select **Use custom policy** to set an advanced policy in the Cloud App Security portal.</span></span>

6. <span data-ttu-id="b423d-126">해당 하는 **조건 할당** 을 추가 하거나 **컨트롤** 을 부여 합니다 (선택 사항).</span><span class="sxs-lookup"><span data-stu-id="b423d-126">Add any applicable **Condition assignments** or **Grant controls** (optional).</span></span>

> ![Azure AD 조건부 액세스](media/OCASimage1.png)

## <a name="step-2-sign-in-with-a-user-scoped-to-the-policy-in-the-apps"></a><span data-ttu-id="b423d-128">2 단계: 범위가 지정 된 사용자를 앱에서 정책으로 로그인</span><span class="sxs-lookup"><span data-stu-id="b423d-128">Step 2: Sign in with a user scoped to the policy in the apps</span></span> 

<span data-ttu-id="b423d-129">정책을 만든 후에는 해당 정책에 구성 된 각 앱에 로그인 합니다.</span><span class="sxs-lookup"><span data-stu-id="b423d-129">After you've created the policy, sign in to each app configured in that policy.</span></span> <span data-ttu-id="b423d-130">정책에 구성 된 사용자를 사용 하 여 로그인 했는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="b423d-130">Make sure you sign in using a user configured in the policy.</span></span> <span data-ttu-id="b423d-131">먼저 기존 세션에서 로그 아웃 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b423d-131">Make sure to first sign out of existing sessions.</span></span>

<span data-ttu-id="b423d-132">Cloud App Security에서는 로그인 하는 각각의 새 앱에 대해 정책 세부 정보를 서버와 동기화 합니다.</span><span class="sxs-lookup"><span data-stu-id="b423d-132">Cloud App Security will sync your policy details to its servers for each new app you log in to.</span></span> <span data-ttu-id="b423d-133">최대 1 분까지 걸릴 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b423d-133">This may take up to one minute.</span></span>

## <a name="step-3-configure-advanced-controls-in-the-cloud-app-security-portal"></a><span data-ttu-id="b423d-134">3 단계: Cloud App Security 포털에서 고급 컨트롤 구성</span><span class="sxs-lookup"><span data-stu-id="b423d-134">Step 3: Configure advanced controls in the Cloud App Security portal</span></span> 

<span data-ttu-id="b423d-135">위 지침에서는 주요 앱에 대 한 기본 제공 Cloud App 보안 정책을 Azure AD에 직접 만드는 데 도움이 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="b423d-135">The instructions above helped you create a built-in Cloud App Security policy for featured apps directly in Azure AD.</span></span>

<span data-ttu-id="b423d-136">고급 정책을 구성 하려면 Office 365 Cloud App Security 포털에서 [액세스 정책](ocas-access-policies.md) 또는 [세션 정책을](ocas-session-policies.md) 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b423d-136">To configure an advanced policy, create an [access policy](ocas-access-policies.md) or a [session policy](ocas-session-policies.md) in the Office 365 Cloud App Security portal.</span></span>

### <a name="to-identify-devices-using-client-certificates-this-is-optional"></a><span data-ttu-id="b423d-137">클라이언트 인증서를 사용 하 여 장치를 확인 하려면 (선택 사항):</span><span class="sxs-lookup"><span data-stu-id="b423d-137">To identify devices using client certificates (this is optional):</span></span>

1. <span data-ttu-id="b423d-138">cog 설정으로 이동 하 여 **장치 id**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="b423d-138">Go to the settings cog and choose **Device identification**.</span></span>

2. <span data-ttu-id="b423d-139">하나 이상의 루트 또는 중간 인증서를 업로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="b423d-139">Upload one or more root or intermediate certificates.</span></span>

3. <span data-ttu-id="b423d-140">인증서를 업로드 한 후에는 **장치 태그** 및 **유효한 클라이언트 인증서**를 기반으로 액세스 정책 및 세션 정책을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b423d-140">After the certificate is uploaded, you can create access policies and session policies based on **Device tag** and **Valid client certificate**.</span></span>

![조건부 액세스 앱 제어 장치 ID](media/OCASimage2.png)

> [!NOTE]
> <span data-ttu-id="b423d-142">인증서는 세션이 유효한 클라이언트 인증서 필터를 사용 하는 정책과 일치 하는 경우에만 사용자에 게 요청 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b423d-142">A certificate is only requested from a user if the session matches a policy that uses the valid client certificate filter.</span></span>
> 
## <a name="step-4-test-the-deployment"></a><span data-ttu-id="b423d-143">4 단계: 배포 테스트</span><span class="sxs-lookup"><span data-stu-id="b423d-143">Step 4: Test the deployment</span></span> 

1. <span data-ttu-id="b423d-144">먼저 기존 세션에서 로그 아웃 합니다.</span><span class="sxs-lookup"><span data-stu-id="b423d-144">First sign out of any existing sessions.</span></span> <span data-ttu-id="b423d-145">그런 다음 성공적으로 배포 된 각 앱에 로그인 해 봅니다.</span><span class="sxs-lookup"><span data-stu-id="b423d-145">Then, try to sign in to each app that was successfully deployed.</span></span> <span data-ttu-id="b423d-146">Azure AD에 구성 된 정책과 일치 하는 사용자를 사용 하 여 로그인 합니다.</span><span class="sxs-lookup"><span data-stu-id="b423d-146">Sign in using a user that matches the policy configured in Azure AD.</span></span>

2. <span data-ttu-id="b423d-147">Cloud App Security 포털의 **조사**에서 **작업 로그**를 선택 하 고 각 앱에 대해 로그인 작업이 캡처 되었는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="b423d-147">In the Cloud App Security portal, under **Investigate**, select **Activity log**, and make sure the login activities are captured for each app.</span></span>

3. <span data-ttu-id="b423d-148"> *\*고급*\*을 클릭 한 다음 원본을 사용 하 여 필터링을 *\*액세스 제어*\*하 여 필터링 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b423d-148">You can filter by clicking on **Advanced**, and then filtering using **Source equals Access control**.</span></span>

4. <span data-ttu-id="b423d-149">관리 되는 장치와 관리 되지 않는 장치에서 모바일 및 데스크톱 앱에 로그인 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="b423d-149">It's recommended that you sign into mobile and desktop apps from managed and unmanaged devices.</span></span> <span data-ttu-id="b423d-150">이는 활동을 활동 로그에 올바르게 캡처 했는지 확인 하기 위한 것입니다.</span><span class="sxs-lookup"><span data-stu-id="b423d-150">This is to make sure that the activities are properly captured in the activity log.</span></span> <span data-ttu-id="b423d-151">작업이 제대로 캡처되고 있는지 확인 하려면 single sign-on 로그온을 클릭 하 여 작업 서랍을 엽니다.</span><span class="sxs-lookup"><span data-stu-id="b423d-151">To verify that the activity is properly captured, click on a single sign-on log on activity so that it opens the activity drawer.</span></span> <span data-ttu-id="b423d-152">장치가 네이티브 클라이언트 (즉, 모바일 또는 데스크톱 응용 프로그램) 인지 또는 장치가 관리 되는 장치 (호환, 도메인에 가입 된 클라이언트 인증서) 중 어떤 것인지에 관계 없이 **사용자 에이전트 태그** 에 적절 한 반영이 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="b423d-152">Make sure the **User agent tag** properly reflects whether the device is a native client (meaning either a mobile or desktop app) or the device is a managed device (compliant, domain joined, or valid client certificate).</span></span>

> [!NOTE]
> <span data-ttu-id="b423d-153">배포 된 후에는 조건부 Access 앱 제어 페이지에서 앱을 제거할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="b423d-153">After it is deployed, you can't remove an app from the Conditional Access App Control page.</span></span> <span data-ttu-id="b423d-154">앱에 대 한 세션 또는 액세스 정책을 설정 하지 않으면 조건부 access 앱 컨트롤에서 앱에 대 한 동작을 변경 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b423d-154">As long as you don't set a session or access policy on the app, the Conditional Access App Control won't change any behavior for the app.</span></span>

## <a name="next-steps"></a><span data-ttu-id="b423d-155">다음 단계</span><span class="sxs-lookup"><span data-stu-id="b423d-155">Next steps</span></span>

- [<span data-ttu-id="b423d-156">Office 365 Cloud App Security의 세션 정책에 대해 자세히 알아보기</span><span class="sxs-lookup"><span data-stu-id="b423d-156">Learn about session policies in Office 365 Cloud App Security</span></span>](ocas-session-policies.md)

- [<span data-ttu-id="b423d-157">Office 365 Cloud App Security의 액세스 정책에 대해 자세히 알아보기</span><span class="sxs-lookup"><span data-stu-id="b423d-157">Learn about access policies in Office 365 Cloud App Security</span></span>](ocas-access-policies.md) 

- [<span data-ttu-id="b423d-158">IP를 그룹화하여 Office 365 Cloud App Security 관리를 단순화</span><span class="sxs-lookup"><span data-stu-id="b423d-158">Group your IP addresses to simplify management in Office 365 Cloud App Security</span></span>](group-your-ip-addresses-in-ocas.md)