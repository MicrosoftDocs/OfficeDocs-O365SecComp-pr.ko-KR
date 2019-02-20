---
title: Office 365 Cloud App Security의 액세스 정책
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.reviewer: alesibov
ms.audience: Admin
ms.topic: reference
ms.date: 02/14/2019
ms.service: o365-administration
localization_priority: Normal
description: Office 365 cloud App Security access 정책을 사용 하면 사용자, 위치, 장치 및 앱을 기반으로 클라우드 앱 액세스를 실시간으로 모니터링 하 고 제어할 수 있습니다. 관리 되는 장치에 클라이언트 인증서를 배포 하거나 타사 MDM 인증서와 같은 기존 인증서를 사용 하 여 도메인에 가입 되지 않은 장치를 포함 하 여 Windows Intune에서 관리 되지 않는 장치에 대 한 액세스 정책을 만들 수 있습니다. 예를 들어 관리 되는 장치에 클라이언트 인증서를 배포한 다음 인증서 없이 장치에서 액세스 하는 것을 차단할 수 있습니다.
ms.openlocfilehash: bb4404793647c65ab8addc148e6efe24242f3079
ms.sourcegitcommit: 8679937354c1d8870ecd41519a59d2d7468c23c4
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/19/2019
ms.locfileid: "30103313"
---
# <a name="access-policies-in-office-365-cloud-app-security"></a><span data-ttu-id="e19a3-105">Office 365 Cloud App Security의 액세스 정책</span><span class="sxs-lookup"><span data-stu-id="e19a3-105">Access policies in Office 365 Cloud App Security</span></span>

|<span data-ttu-id="e19a3-106">계산 \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="e19a3-106">\*\*\*\*Evaluation\*\* \>\*\*</span></span>|<span data-ttu-id="e19a3-107">계획 \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="e19a3-107">\*\*\*\*Planning\*\* \>\*\*</span></span>|<span data-ttu-id="e19a3-108">배포 \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="e19a3-108">\*\*\*\*Deployment\*\* \>\*\*</span></span>|<span data-ttu-id="e19a3-109">사용률 \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="e19a3-109">\*\*\*\*Utilization\*\*\*\*</span></span>|
|:-----|:-----|:-----|:-----|
|[<span data-ttu-id="e19a3-110">평가 시작</span><span class="sxs-lookup"><span data-stu-id="e19a3-110">Start evaluating</span></span>](office-365-cas-overview.md) <br/> |[<span data-ttu-id="e19a3-111">계획 시작</span><span class="sxs-lookup"><span data-stu-id="e19a3-111">Start planning</span></span>](get-ready-for-office-365-cas.md) <br/> |<span data-ttu-id="e19a3-112">사용자가 여기 있어!</span><span class="sxs-lookup"><span data-stu-id="e19a3-112">You are here!</span></span>  <br/> [<span data-ttu-id="e19a3-113">다음 단계</span><span class="sxs-lookup"><span data-stu-id="e19a3-113">Next step</span></span>](group-your-ip-addresses-in-ocas.md) <br/> |[<span data-ttu-id="e19a3-114">활용 시작</span><span class="sxs-lookup"><span data-stu-id="e19a3-114">Start utilizing</span></span>](utilization-activities-for-ocas.md) <br/> |

<span data-ttu-id="e19a3-p102">Office 365 cloud App Security access 정책을 사용 하면 사용자, 위치, 장치 및 앱을 기반으로 클라우드 앱 액세스를 실시간으로 모니터링 하 고 제어할 수 있습니다. 관리 되는 장치에 클라이언트 인증서를 배포 하거나 타사 MDM 인증서와 같은 기존 인증서를 사용 하 여 도메인에 가입 되지 않은 장치를 포함 하 여 Windows Intune에서 관리 되지 않는 장치에 대 한 액세스 정책을 만들 수 있습니다. 예를 들어 관리 되는 장치에 클라이언트 인증서를 배포한 다음 인증서 없이 장치에서 액세스 하는 것을 차단할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e19a3-p102">Office 365 Cloud App Security access policies enable real-time monitoring and control over access to cloud apps based on user, location, device, and app. You can create access policies for any device, including devices that aren't domain joined, and not managed by Windows Intune by rolling out client certificates to managed devices or by using existing certificates, such as third-party MDM certificates. For example, you can deploy client certificates to managed devices, and then block access from devices without a certificate.</span></span>

<span data-ttu-id="e19a3-118"> [세션 정책을](ocas-session-policies.md) 사용 하 여 액세스를 완전히 허용 하거나 차단 하지 않고 세션을 모니터링 하 고 특정 세션 작업을 제한 하는 동안 액세스를 허용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e19a3-118">Instead of allowing or blocking access completely, with [session policies](ocas-session-policies.md) you can allow access while monitoring the session and/or limit specific session activities.</span></span>

## <a name="prerequisites-to-using-access-policies"></a><span data-ttu-id="e19a3-119">액세스 정책 사용을 위한 필수 구성 요소</span><span class="sxs-lookup"><span data-stu-id="e19a3-119">Prerequisites to using access policies</span></span>

- <span data-ttu-id="e19a3-120">Azure AD Premium P1 라이선스</span><span class="sxs-lookup"><span data-stu-id="e19a3-120">Azure AD Premium P1 license</span></span>

- <span data-ttu-id="e19a3-121">관련 앱을 [조건부 액세스 앱 컨트롤을 사용 하 여 배포](https://docs.microsoft.com/en-us/cloud-app-security/proxy-deployment-aad) 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e19a3-121">The relevant apps should be [deployed with Conditional Access App Control](https://docs.microsoft.com/en-us/cloud-app-security/proxy-deployment-aad)</span></span>

- <span data-ttu-id="e19a3-122">아래에 설명 된 대로 사용자를 Office 365 Cloud App Security로 리디렉션하는 [Azure AD 조건부 액세스 정책이](https://docs.microsoft.com/azure/active-directory/active-directory-conditional-access-azure-portal) 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e19a3-122">An [Azure AD conditional access policy](https://docs.microsoft.com/azure/active-directory/active-directory-conditional-access-azure-portal) should be in place that redirects users to Office 365 Cloud App Security, as described below.</span></span>

## <a name="create-an-azure-ad-conditional-access-policy"></a><span data-ttu-id="e19a3-123">Azure AD 조건부 액세스 정책 만들기</span><span class="sxs-lookup"><span data-stu-id="e19a3-123">Create an Azure AD conditional access policy</span></span>

<span data-ttu-id="e19a3-p103">Azure Active Directory 조건부 액세스 정책 및 클라우드 응용 프로그램 보안 세션 정책은 각 사용자 세션을 검사 하 고 각 앱에 대 한 정책 결정을 내리는 동시에 작동 합니다. Azure AD에서 조건부 액세스 정책을 설정 하려면 다음 절차를 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="e19a3-p103">Azure Active Directory conditional access policies and Cloud App Security session policies work in tandem to examine each user session and make policy decisions for each app. To set up a conditional access policy in Azure AD, follow this procedure:</span></span>

1. <span data-ttu-id="e19a3-126">사용자 또는 사용자 그룹에 대 한 할당과 조건부 액세스 앱 컨트롤을 사용 하 여 제어할 앱에 대 한 할당을 사용 하 여 [Azure AD 조건부 액세스 정책을](https://docs.microsoft.com/azure/active-directory/active-directory-conditional-access-azure-portal) 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="e19a3-126">Configure an [Azure AD conditional access policy](https://docs.microsoft.com/azure/active-directory/active-directory-conditional-access-azure-portal) with assignments for user or group of users and the app you want to control with Conditional Access App Control.</span></span><br><span data-ttu-id="e19a3-127">참고:  [조건부 Access 앱 컨트롤을 사용 하 여 배포한](https://docs.microsoft.com/cloud-app-security/proxy-deployment-aad)앱만이 정책의 영향을 받습니다.</span><span class="sxs-lookup"><span data-stu-id="e19a3-127">NOTE: Only apps that were [deployed with Conditional Access App Control](https://docs.microsoft.com/cloud-app-security/proxy-deployment-aad) will be affected by this policy.</span></span>

2. <span data-ttu-id="e19a3-128"> *\*Session*\*에서 *\*조건부 액세스 앱 제어 적용 제한** 사용을 선택 하 여 Office 365 Cloud App Security로 사용자를 라우팅합니다.</span><span class="sxs-lookup"><span data-stu-id="e19a3-128">Route users to Office 365 Cloud App Security by selecting the **Use Conditional Access App Control enforced restrictions** under **Session**.</span></span>

## <a name="create-a-cloud-app-security-access-policy"></a><span data-ttu-id="e19a3-129">Cloud App Security access 정책 만들기</span><span class="sxs-lookup"><span data-stu-id="e19a3-129">Create a Cloud App Security access policy</span></span>

<span data-ttu-id="e19a3-130">새 액세스 정책을 만들려면 다음 절차를 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="e19a3-130">To create a new access policy, follow this procedure:</span></span>

1. <span data-ttu-id="e19a3-131">포털에서 **제어** 다음에 **정책을**선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="e19a3-131">In the portal, select **Control** followed by **Policies**.</span></span>

2. <span data-ttu-id="e19a3-132"> *\*정책** 페이지에서 *\*정책** 만들기를 클릭 하 고 *\*액세스 정책을*\*선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="e19a3-132">In the **Policies** page, click **Create policy** and select **Access policy**.</span></span>

3. <span data-ttu-id="e19a3-133"> *\*액세스 정책** 창에서 \*관리 되지 않는 장치 로부터의 액세스 차단\*같은 정책의 이름을 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="e19a3-133">In the **Access policy** window, assign a name for your policy, such as *Block access from unmanaged devices*.</span></span>

4. <span data-ttu-id="e19a3-p104">  \*\*다음의 모든\*\*항목에 해당 하는 활동의 \*\*활동 원본\*\*에서 정책에 적용할 추가 활동 필터를 선택 합니다. 필터에는 다음 옵션이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e19a3-p104">In the **Activities matching all of the following** section, Under **Activity source**, select additional activity filters to apply to the policy. Filters include the following options:</span></span>
    
    - <span data-ttu-id="e19a3-136">**장치 태그**:이 필터를 사용 하 여 관리 되지 않는 장치를 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="e19a3-136">**Device tags**: Use this filter to identify unmanaged devices.</span></span>
    
    - <span data-ttu-id="e19a3-137">**위치**:이 필터를 사용 하 여 알 수 없는 (또는 위험한) 위치를 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="e19a3-137">**Location**: Use this filter to identify unknown (and therefore risky) locations.</span></span>
    
    - <span data-ttu-id="e19a3-138">**ip 주소**:이 필터를 사용 하 여 ip 주소당 필터링 하거나 이전에 할당 된 ip 주소 태그를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="e19a3-138">**IP address**: Use this filter to filter per IP addresses or use previously assigned IP address tags.</span></span>
    
    - <span data-ttu-id="e19a3-p105">**사용자 에이전트 태그**:이 필터를 사용 하 여 추론에서 모바일 및 데스크톱 앱을 식별 하도록 설정 합니다. 이 필터는 같음 또는 같지 않음으로 설정할 수 있습니다. 각 클라우드 앱에 대해 모바일 및 데스크톱 앱에 대해 값을 테스트 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e19a3-p105">**User agent tag**: Use this filter to enable the heuristic to identify mobile and desktop apps. This filter can be set to equals or does not equal. The values should be tested against your mobile and desktop apps for each cloud app.</span></span>

5. <span data-ttu-id="e19a3-142"> *\*작업*\*에서 다음 옵션 중 하나를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="e19a3-142">Under **Actions**, select one of the following options:</span></span>
    
    - <span data-ttu-id="e19a3-143">**Allow**: 설정한 정책 필터에 따라 명시적으로 액세스를 허용 하도록이 작업을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e19a3-143">**Allow**: Set this action to explicitly allow access according to the policy filters you set.</span></span>
    
    - <span data-ttu-id="e19a3-144">**차단**: 설정한 정책 필터에 따라 액세스를 명시적으로 차단 하려면이 작업을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e19a3-144">**Block**: Set this action to explicitly block access according to the policy filters you set.</span></span>

6. <span data-ttu-id="e19a3-145"> *\*정책의 심각도로 각 일치 이벤트에 대 한 알림을 만들고** 경고 제한을 설정 하 고 알림을 전자 메일, 문자 메시지 또는 둘 다 중에서 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e19a3-145">You can **Create an alert for each matching event with the policy's severity** and set an alert limit and select whether you want the alert as an email, a text message or both.</span></span>

## <a name="next-steps"></a><span data-ttu-id="e19a3-146">다음 단계</span><span class="sxs-lookup"><span data-stu-id="e19a3-146">Next steps</span></span>

- [<span data-ttu-id="e19a3-147">IP를 그룹화하여 Office 365 Cloud App Security 관리를 단순화</span><span class="sxs-lookup"><span data-stu-id="e19a3-147">Group your IP addresses to simplify management in Office 365 Cloud App Security</span></span>](group-your-ip-addresses-in-ocas.md)