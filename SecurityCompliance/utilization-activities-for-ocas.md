---
title: Office 365 Cloud App Security 적용한 후 사용률 활동
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 01/28/2019
ms.audience: ITPro
ms.topic: conceptual
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 86f414ad-81de-4703-b40a-c6615bbe9108
description: Office 365 Cloud App Security을 설정 하 고 롤아웃 한 후에는 특정 작업을 수행 하 여 구성이 올바르고 일반적인 검토를 위해 준비 되었는지 확인 해야 합니다.
ms.openlocfilehash: 232de4df1d1eb4debdddcee2c1d8672d1aeb4b21
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32242546"
---
# <a name="utilization-activities-after-rolling-out-office-365-cloud-app-security"></a><span data-ttu-id="68552-103">Office 365 Cloud App Security 적용한 후 사용률 활동</span><span class="sxs-lookup"><span data-stu-id="68552-103">Utilization activities after rolling out Office 365 Cloud App Security</span></span>
  
|<span data-ttu-id="68552-104">계산 \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="68552-104">\*\*\*\*Evaluation\*\* \>\*\*</span></span>|<span data-ttu-id="68552-105">계획 \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="68552-105">\*\*\*\*Planning\*\* \>\*\*</span></span>|<span data-ttu-id="68552-106">배포 \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="68552-106">\*\*\*\*Deployment\*\* \>\*\*</span></span>|<span data-ttu-id="68552-107">사용률 \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="68552-107">\*\*\*\*Utilization\*\*\*\*</span></span>|
|:-----|:-----|:-----|:-----|
|[<span data-ttu-id="68552-108">평가 시작</span><span class="sxs-lookup"><span data-stu-id="68552-108">Start evaluating</span></span>](office-365-cas-overview.md) <br/> |[<span data-ttu-id="68552-109">계획 시작</span><span class="sxs-lookup"><span data-stu-id="68552-109">Start planning</span></span>](get-ready-for-office-365-cas.md) <br/> |[<span data-ttu-id="68552-110">배포 시작</span><span class="sxs-lookup"><span data-stu-id="68552-110">Start deploying</span></span>](turn-on-office-365-cas.md) <br/> |<span data-ttu-id="68552-111">사용자가 여기 있어!</span><span class="sxs-lookup"><span data-stu-id="68552-111">You are here!</span></span>  <br/> [<span data-ttu-id="68552-112">다음 단계</span><span class="sxs-lookup"><span data-stu-id="68552-112">Next step</span></span>](review-office-365-cas-alerts.md) <br/> |
   
> [!NOTE]
> <span data-ttu-id="68552-113">office 365 Cloud App Security는 office 365 Enterprise E5에서 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="68552-113">Office 365 Cloud App Security is available in Office 365 Enterprise E5.</span></span> <span data-ttu-id="68552-114">조직에서 다른 office 365 Enterprise 구독을 사용 하는 경우 office 365 Cloud App Security를 추가 기능으로 구입할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="68552-114">If your organization is using another Office 365 Enterprise subscription, Office 365 Cloud App Security can be purchased as an add-on.</span></span> <span data-ttu-id="68552-115">(전역 관리자 인 경우 Microsoft 365 관리 센터에서 **청구** \> **구독 추가**를 선택 합니다.) 자세한 내용은 [office 365 플랫폼 서비스 설명: office 365 보안 &amp; 및 준수 센터](https://docs.microsoft.com/office365/servicedescriptions/office-365-platform-service-description/office-365-securitycompliance-center) 및 [비즈니스용 office 365 용 추가 기능 구입 또는 편집](https://support.office.com/article/4e7b57d6-b93b-457d-aecd-0ea58bff07a6)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="68552-115">(As a global administrator, in the Microsoft 365 admin center, choose **Billing** \> **Add subscriptions**.) For more information, see [Office 365 Platform Service Description: Office 365 Security &amp; Compliance Center](https://docs.microsoft.com/office365/servicedescriptions/office-365-platform-service-description/office-365-securitycompliance-center) and [Buy or edit an add-on for Office 365 for business](https://support.office.com/article/4e7b57d6-b93b-457d-aecd-0ea58bff07a6).</span></span> 
  
<span data-ttu-id="68552-116">office 365 Cloud App Security를 설정 하 고 구성한 후에는 특정 사용률 작업을 조직의 Office 365 전역 관리자 또는 보안 관리자로 수행 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="68552-116">After you have set up and configured Office 365 Cloud App Security, you'll want to perform certain utilization tasks as an Office 365 global administrator or security administrator for your organization.</span></span> 

<span data-ttu-id="68552-117">이러한 작업을 수행 하 여 office 365 Cloud App Security가 올바르게 구성 되어 있고, 정책이 최신 상태 이며, 조직에서 office 365의 가치를 인식 하도록 하는 데 도움이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="68552-117">By performing these tasks, you'll help ensure that Office 365 Cloud App Security is configured correctly, your policies are up to date, and your organization realizes value from Office 365.</span></span> <span data-ttu-id="68552-118">이 문서를 참조 하 여 이러한 작업을 계획 하는 데 도움을 받을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="68552-118">Use this article as a guide to help you plan for these tasks.</span></span>
  
> [!NOTE]
> <span data-ttu-id="68552-119">이 문서에서 설명 하는 작업을 수행 하려면 전역 관리자 또는 보안 관리자 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="68552-119">You must be a global administrator or security administrator to perform the tasks described in this article.</span></span> <span data-ttu-id="68552-120">자세한 내용은 [Office 365 보안 &amp; 및 준수 센터의 사용 권한](permissions-in-the-security-and-compliance-center.md)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="68552-120">To learn more, see [Permissions in the Office 365 Security &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md).</span></span> 
    
## <a name="activities-after-the-initial-configuration-and-rollout-of-office-365-cloud-app-security"></a><span data-ttu-id="68552-121">Office 365 Cloud App Security의 초기 구성 및 롤아웃 후의 작업</span><span class="sxs-lookup"><span data-stu-id="68552-121">Activities after the initial configuration and rollout of Office 365 Cloud App Security</span></span>

<span data-ttu-id="68552-122">Office 365 Cloud App security는 전역 관리자 또는 보안 관리자로 구성 및 롤아웃 된 후 다음과 같은 몇 가지 사항을 고려해 야 합니다.</span><span class="sxs-lookup"><span data-stu-id="68552-122">After Office 365 Cloud App Security is configured and rolled out, as a global administrator or security administrators, you have several things to consider:</span></span>
  
- <span data-ttu-id="68552-123">IT 부서 일정에 추가 해야 하는 작업</span><span class="sxs-lookup"><span data-stu-id="68552-123">What tasks need to be added to the IT department calendar?</span></span>
    
- <span data-ttu-id="68552-124">Office 365 Cloud App Security가 시간에 따라 올바른 정책 집합을 사용 하도록 구성 되었는지 확인 하려면 어떻게 해야 하나요?</span><span class="sxs-lookup"><span data-stu-id="68552-124">How can you make sure Office 365 Cloud App Security is configured to use the right set of policies over time?</span></span>
    
- <span data-ttu-id="68552-125">IT 관리 체인을 전송 해야 하는 요약 정보 종류는 무엇입니까?</span><span class="sxs-lookup"><span data-stu-id="68552-125">What kinds of summary information should you send up the IT management chain?</span></span>
    
<span data-ttu-id="68552-126">다음 표에서는 수행 하려는 진행 중인 작업 및 IT 부서의 일정에 추가 하는 데 필요한 정기적인 작업을 간략하게 요약 하 여 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="68552-126">The following table briefly summarizes the ongoing tasks you'll want to perform and periodic tasks you should consider adding to your IT department's calendar.</span></span>
  
|<span data-ttu-id="68552-127">**진행 중인 작업**</span><span class="sxs-lookup"><span data-stu-id="68552-127">**Ongoing tasks**</span></span>|<span data-ttu-id="68552-128">**정기 작업**</span><span class="sxs-lookup"><span data-stu-id="68552-128">**Periodic tasks**</span></span>|
|:-----|:-----|
| <span data-ttu-id="68552-129">알림 메시지를 보낼 전자 메일 계정 모니터링</span><span class="sxs-lookup"><span data-stu-id="68552-129">Monitor the email accounts to which you are sending alert messages</span></span>  <br/>  <span data-ttu-id="68552-130">새 사이버 공격에 대 한 최신 정보에 대 한 업계 cybersecurity 뉴스 피드 모니터링</span><span class="sxs-lookup"><span data-stu-id="68552-130">Monitor industry cybersecurity news feeds for the latest information about new cyber attacks</span></span>  <br/>  <span data-ttu-id="68552-131">보안 사고 및 위험을 식별 하 고 해결 하기 위한 보안 경고 동작</span><span class="sxs-lookup"><span data-stu-id="68552-131">Act on security alerts to identify and address security incidents and risks</span></span>  <br/>  <span data-ttu-id="68552-132">중앙 로그의 각 보안 인시던트 및 해결 방법 요약</span><span class="sxs-lookup"><span data-stu-id="68552-132">Summarize each security incident and resolution in a central log</span></span>  <br/> | <span data-ttu-id="68552-133">Office 365 Cloud App 보안 경고의 월간 또는 분기별 검토를 수행 하 여 예외를 발견 하 고 추세를 분석 합니다.</span><span class="sxs-lookup"><span data-stu-id="68552-133">Perform monthly or quarterly reviews of Office 365 Cloud App Security alerts to spot anomalies and analyze trends</span></span>  <br/>  <span data-ttu-id="68552-134">office 365 cloud app security의 향상 된 기능을 포함 하기 위해 기존 Office 365 cloud app security 정책을 매월 또는 분기별로 검토를 수행 하 고 cybersecurity의 새 고 사이버 공격 및 추세를 해결 합니다.</span><span class="sxs-lookup"><span data-stu-id="68552-134">Perform monthly or quarterly reviews of your existing Office 365 Cloud App Security policies to include enhancements in Office 365 Cloud App Security and address new cyberattacks and trends in cybersecurity</span></span>  <br/> |
   
<span data-ttu-id="68552-135">조직의 규모 및 모니터링 및 유지 관리에 대 한 관심 사항에 따라 다음을 포함 하는 IT 관리 체인에 대 한 월별 요약을 컴파일할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="68552-135">Depending on your organization's size and interest in monitoring and maintaining a security stature, you can compile a monthly summary for your IT management chain that includes:</span></span>
  
- <span data-ttu-id="68552-136">Office 365 Cloud App security로 식별 되는 다양 한 보안 인시던트 유형</span><span class="sxs-lookup"><span data-stu-id="68552-136">The different types of security incidents identified with Office 365 Cloud App Security</span></span>
    
- <span data-ttu-id="68552-137">검색 된 인시던트 수와 같은 보안 사고의 중앙 로그의 요약 정보</span><span class="sxs-lookup"><span data-stu-id="68552-137">Summary information from your central log of the security incidents, such as number of incidents detected</span></span>
    
- <span data-ttu-id="68552-138">알림 경향 및 처리 방법</span><span class="sxs-lookup"><span data-stu-id="68552-138">Alert trends and how they were addressed</span></span>
    
- <span data-ttu-id="68552-139">최신 cybersecurity 추세</span><span class="sxs-lookup"><span data-stu-id="68552-139">The latest cybersecurity trends</span></span>
    
- <span data-ttu-id="68552-140">Office 365 Cloud App Security policy 변경 및 최종 사용자에 게 미치는 영향에 대 한 권장 사항</span><span class="sxs-lookup"><span data-stu-id="68552-140">Recommendations for Office 365 Cloud App Security policy changes and their impact on end users</span></span>
    
## <a name="activities-after-time-has-passed-since-rolling-out-office-365-cloud-app-security"></a><span data-ttu-id="68552-141">Office 365 Cloud App Security 이후 시간이 지난 후 활동</span><span class="sxs-lookup"><span data-stu-id="68552-141">Activities after time has passed since rolling out Office 365 Cloud App Security</span></span>

<span data-ttu-id="68552-142">처음에 Office 365 Cloud App Security 정책을 구성 하거나 유지 관리 한 후에 protracted 시간이 경과 된 경우 다음 단계를 수행 하 여 조직의 보안 목표 및 현재 기능을 반영 하는 구성으로 다시 이동 합니다. Office 365 Cloud App Security의 경우:</span><span class="sxs-lookup"><span data-stu-id="68552-142">If a protracted amount of time has passed since you initially configured or maintained your Office 365 Cloud App Security policies, take the following steps to get back to a configuration that reflects your organization's security goals and the current capabilities of Office 365 Cloud App Security:</span></span>
  
1. <span data-ttu-id="68552-143">Office 365 Cloud App Security에 대 한 마지막 구성 변경 날짜를 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="68552-143">Determine the date of the last configuration change for Office 365 Cloud App Security.</span></span>
    
2. <span data-ttu-id="68552-144">현재 Office 365 Cloud App Security configuration을 이해 하 고 필요에 따라 해당 정책을 조정 합니다.</span><span class="sxs-lookup"><span data-stu-id="68552-144">Understand your current Office 365 Cloud App Security configuration and adjust those policies as needed.</span></span> <span data-ttu-id="68552-145">예를 들어 전자 메일을 통해 알림을 보내는 위치를 알고 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="68552-145">For example, make sure you know where alerts are being sent via email.</span></span>
    
3. <span data-ttu-id="68552-146">office 365 cloud app security를 마지막으로 구성한 이후의 제품 변경 사항에 대해서는 [office 365 cloud app security의 새로운 기능](new-in-office-365-cas.md) 을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="68552-146">See [what's new in Office 365 Cloud App Security](new-in-office-365-cas.md) for product changes since you last configured Office 365 Cloud App Security.</span></span> 
    
4. <span data-ttu-id="68552-147">Office 365 Cloud App 보안 경고 및 로그 분석을 수행 하 여 예외를 강조 하 고 추세를 분석 합니다.</span><span class="sxs-lookup"><span data-stu-id="68552-147">Perform an analysis of Office 365 Cloud App Security alerts and logs to spot anomalies and analyze trends.</span></span>
    
5. <span data-ttu-id="68552-148">업계 cybersecurity 경향을 확인 하 여 최신 보안 위협을 파악 합니다.</span><span class="sxs-lookup"><span data-stu-id="68552-148">Check industry cybersecurity trends to become aware of the latest security threats.</span></span>
    
6. <span data-ttu-id="68552-149">현재 Office 365 Cloud App Security 정책 집합에 적용 해야 하는 변경 사항에 대 한 분석을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="68552-149">Perform an analysis of the changes that need to be made to the current set of Office 365 Cloud App Security policies.</span></span> <span data-ttu-id="68552-150">Office 365 Cloud App Security 기능 변경 사항, 현재 상황 및 cybersecurity 추세를 통합 합니다.</span><span class="sxs-lookup"><span data-stu-id="68552-150">Incorporate Office 365 Cloud App Security feature changes, current anomalies, and cybersecurity trends.</span></span> <span data-ttu-id="68552-151">기존 정책 변경 또는 새 정책 만들기 권장</span><span class="sxs-lookup"><span data-stu-id="68552-151">Recommend changes to existing policies or the creation of new policies.</span></span>
    
7. <span data-ttu-id="68552-152">정책 변경 사항 구현 계획을 수립 합니다.</span><span class="sxs-lookup"><span data-stu-id="68552-152">Make a plan for implementing the policy changes.</span></span> <span data-ttu-id="68552-153">의견 교환 (socialize) 필요에 따라 최종 사용자에 게 제안 된 변경의 결과를 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="68552-153">Communicate (socialize) the consequences of the proposed changes with your end users as needed.</span></span>
    
8. <span data-ttu-id="68552-154">Office 365 Cloud App 보안 정책 변경 사항을 구현 합니다.</span><span class="sxs-lookup"><span data-stu-id="68552-154">Implement the Office 365 Cloud App Security policy changes.</span></span>
    
9. <span data-ttu-id="68552-155">최종 사용자 의견 및 Office 365 Cloud App Security alerts를 모니터링 하 고 시간에 따라 정책을 조정 합니다.</span><span class="sxs-lookup"><span data-stu-id="68552-155">Monitor end user feedback and Office 365 Cloud App Security alerts and adjust policies over time.</span></span>
    
## <a name="next-steps"></a><span data-ttu-id="68552-156">다음 단계</span><span class="sxs-lookup"><span data-stu-id="68552-156">Next steps</span></span>

- [<span data-ttu-id="68552-157">활동 조사</span><span class="sxs-lookup"><span data-stu-id="68552-157">Investigate an activity</span></span>](investigate-an-activity-in-office-365-cas.md)
    
- [<span data-ttu-id="68552-158">사용자 계정 일시 중단 또는 복원</span><span class="sxs-lookup"><span data-stu-id="68552-158">Suspend or restore a user account</span></span>](suspend-or-restore-an-account-in-ocas.md)
    
- [<span data-ttu-id="68552-159">OAuth 앱 관리</span><span class="sxs-lookup"><span data-stu-id="68552-159">Manage OAuth apps</span></span>](manage-app-permissions-in-ocas.md)
    
- [<span data-ttu-id="68552-160">Office 365 Cloud App Security을 사용하여 앱 검색 결과 검토</span><span class="sxs-lookup"><span data-stu-id="68552-160">Review app discovery findings in Office 365 Cloud App Security</span></span>](review-app-discovery-findings-in-ocas.md)
    
- <span data-ttu-id="68552-161">지원 되는 [웹 트래픽 로그 및 데이터 원본](web-traffic-logs-and-data-sources-for-ocas.md) 목록 보기</span><span class="sxs-lookup"><span data-stu-id="68552-161">View a list of supported [Web traffic logs and data sources](web-traffic-logs-and-data-sources-for-ocas.md)</span></span>
    

