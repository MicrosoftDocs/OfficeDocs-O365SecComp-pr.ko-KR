---
title: Office 365 Cloud App Security 적용한 후 사용률 활동
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 2/26/2018
ms.audience: ITPro
ms.topic: conceptual
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 86f414ad-81de-4703-b40a-c6615bbe9108
description: 설정 하면 Office 365 클라우드 응용 프로그램 보안 롤아웃 후 구성은 올바른 하의 정기적 검토 준비 하는 특정 작업을 수행 합니다.
ms.openlocfilehash: bc8cfad8eb9d9444066c3193ec2978e9ffd9f56a
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22533267"
---
# <a name="utilization-activities-after-rolling-out-office-365-cloud-app-security"></a><span data-ttu-id="32846-103">Office 365 Cloud App Security 적용한 후 사용률 활동</span><span class="sxs-lookup"><span data-stu-id="32846-103">Utilization activities after rolling out Office 365 Cloud App Security</span></span>
  
|<span data-ttu-id="32846-104">평가 * *\>**</span><span class="sxs-lookup"><span data-stu-id="32846-104">****Evaluation** \>**</span></span>|<span data-ttu-id="32846-105">계획 * *\>**</span><span class="sxs-lookup"><span data-stu-id="32846-105">****Planning** \>**</span></span>|<span data-ttu-id="32846-106">배포 * *\>**</span><span class="sxs-lookup"><span data-stu-id="32846-106">****Deployment** \>**</span></span>|<span data-ttu-id="32846-107">사용률 \* \* \*</span><span class="sxs-lookup"><span data-stu-id="32846-107">****Utilization****</span></span>|
|:-----|:-----|:-----|:-----|
|[<span data-ttu-id="32846-108">평가 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="32846-108">Start evaluating</span></span>](office-365-cas-overview.md) <br/> |[<span data-ttu-id="32846-109">계획을 시작합니다</span><span class="sxs-lookup"><span data-stu-id="32846-109">Start planning</span></span>](get-ready-for-office-365-cas.md) <br/> |[<span data-ttu-id="32846-110">배포를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="32846-110">Start deploying</span></span>](turn-on-office-365-cas.md) <br/> |<span data-ttu-id="32846-111">여기는!</span><span class="sxs-lookup"><span data-stu-id="32846-111">You are here!</span></span>  <br/> [<span data-ttu-id="32846-112">다음 단계</span><span class="sxs-lookup"><span data-stu-id="32846-112">Next step</span></span>](review-office-365-cas-alerts.md) <br/> |
   
> [!NOTE]
> <span data-ttu-id="32846-p101">Office 365 클라우드 App 보안은 Office 365 Enterprise e 5에 사용할 수 있습니다. 조직의 다른 Office 365 Enterprise 등록을 사용 하는 경우 Office 365 클라우드 앱 보안 추가 기능으로 구입할 수 있습니다. (전역 관리자는 Office 365 관리 센터에서 선택 **대금 청구** \> **추가 구독**.) 자세한 내용은 참조 [Office 365 플랫폼 서비스 설명: Office 365 보안 &amp; 준수 센터](https://technet.microsoft.com/en-us/library/dn933793.aspx) [구입 또는 비즈니스를 위한 Office 365에 대 한 추가 기능을 편집](https://support.office.com/article/4e7b57d6-b93b-457d-aecd-0ea58bff07a6)하 고 있습니다.</span><span class="sxs-lookup"><span data-stu-id="32846-p101">Office 365 Cloud App Security is available in Office 365 Enterprise E5. If your organization is using another Office 365 Enterprise subscription, Office 365 Cloud App Security can be purchased as an add-on. (As a global administrator, in the Office 365 admin center, choose **Billing** \> **Add subscriptions**.) For more information, see [Office 365 Platform Service Description: Office 365 Security &amp; Compliance Center](https://technet.microsoft.com/en-us/library/dn933793.aspx) and [Buy or edit an add-on for Office 365 for business](https://support.office.com/article/4e7b57d6-b93b-457d-aecd-0ea58bff07a6).</span></span> 
  
<span data-ttu-id="32846-116">설정 및 Office 365 클라우드 응용 프로그램 보안 구성 되어 있다고을 한 후 Office 365 전역 관리자 또는 조직에 대 한 보안 관리자 권한으로 특정 사용률 작업을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="32846-116">After you have set up and configured Office 365 Cloud App Security, you'll want to perform certain utilization tasks as an Office 365 global administrator or security administrator for your organization.</span></span> 

<span data-ttu-id="32846-p102">이러한 작업을 수행 하 여는 Office 365 클라우드 App 보안은 올바르게 구성, 정책에는 최신 상태로 및 조직의 Office 365에서 값을 실현를 보장할 수 수 있습니다. 지침으로이 문서를 사용 하 여 이러한 작업에 대 한 계획을 세우는 데 도움이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="32846-p102">By performing these tasks, you'll help ensure that Office 365 Cloud App Security is configured correctly, your policies are up to date, and your organization realizes value from Office 365. Use this article as a guide to help you plan for these tasks.</span></span>
  
> [!NOTE]
> <span data-ttu-id="32846-p103">이 문서에서 설명 하는 작업을 수행 하려면 전역 관리자 또는 보안 관리자 여야 합니다. 자세한 내용은 참조 [Office 365 보안에 대 한 사용 권한을 &amp; 준수 센터](permissions-in-the-security-and-compliance-center.md)합니다.</span><span class="sxs-lookup"><span data-stu-id="32846-p103">You must be a global administrator or security administrator to perform the tasks described in this article. To learn more, see [Permissions in the Office 365 Security &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md).</span></span> 
    
## <a name="activities-after-the-initial-configuration-and-rollout-of-office-365-cloud-app-security"></a><span data-ttu-id="32846-121">초기 구성 데이터베이스 및 Office 365 클라우드 응용 프로그램 보안을 배포 후 작업</span><span class="sxs-lookup"><span data-stu-id="32846-121">Activities after the initial configuration and rollout of Office 365 Cloud App Security</span></span>

<span data-ttu-id="32846-122">Office 365 클라우드 응용 프로그램 보안을 구성 하 고 전역 관리자 또는 보안 관리자, 롤아웃 후 해야 몇가지 사항을 고려해 야 합니다.</span><span class="sxs-lookup"><span data-stu-id="32846-122">After Office 365 Cloud App Security is configured and rolled out, as a global administrator or security administrators, you have several things to consider:</span></span>
  
- <span data-ttu-id="32846-123">작업 해야하는 IT 부서 일정에 추가할 수 있습니까?</span><span class="sxs-lookup"><span data-stu-id="32846-123">What tasks need to be added to the IT department calendar?</span></span>
    
- <span data-ttu-id="32846-124">Office 365 클라우드 앱 보안 시간에 따른 정책의 오른쪽 집합을 사용 하도록 구성 된 하려면 어떻게 해야 합니까?</span><span class="sxs-lookup"><span data-stu-id="32846-124">How can you make sure Office 365 Cloud App Security is configured to use the right set of policies over time?</span></span>
    
- <span data-ttu-id="32846-125">IT 관리 체인을 어떤 종류의 요약 정보를 보낼 해야 합니까?</span><span class="sxs-lookup"><span data-stu-id="32846-125">What kinds of summary information should you send up the IT management chain?</span></span>
    
<span data-ttu-id="32846-126">다음 표에서 진행 중인 작업을 수행 하려는 및 IT 부서의 일정에 추가 하는 것이 좋습니다 정기적으로 작업을 간략하게 요약 한 합니다.</span><span class="sxs-lookup"><span data-stu-id="32846-126">The following table briefly summarizes the ongoing tasks you'll want to perform and periodic tasks you should consider adding to your IT department's calendar.</span></span>
  
|<span data-ttu-id="32846-127">**진행 중인 작업**</span><span class="sxs-lookup"><span data-stu-id="32846-127">**Ongoing tasks**</span></span>|<span data-ttu-id="32846-128">**정기적으로 작업**</span><span class="sxs-lookup"><span data-stu-id="32846-128">**Periodic tasks**</span></span>|
|:-----|:-----|
| <span data-ttu-id="32846-129">경고 메시지를 보내는 전자 메일 계정을 모니터링합니다</span><span class="sxs-lookup"><span data-stu-id="32846-129">Monitor the email accounts to which you are sending alert messages</span></span>  <br/>  <span data-ttu-id="32846-130">새로운 인터넷 공격에 대 한 최신 정보에 대 한 업계 cybersecurity 뉴스 피드를 모니터링 합니다.</span><span class="sxs-lookup"><span data-stu-id="32846-130">Monitor industry cybersecurity news feeds for the latest information about new cyber attacks</span></span>  <br/>  <span data-ttu-id="32846-131">보안 경고를 식별 하 고 보안 문제 및 위험을 해결 작업을 수행합니다</span><span class="sxs-lookup"><span data-stu-id="32846-131">Act on security alerts to identify and address security incidents and risks</span></span>  <br/>  <span data-ttu-id="32846-132">각 보안 문제 및 해결 방법 중앙 로그에 요약</span><span class="sxs-lookup"><span data-stu-id="32846-132">Summarize each security incident and resolution in a central log</span></span>  <br/> | <span data-ttu-id="32846-133">Office 365 클라우드 응용 프로그램 보안 알림 별색 비정상 상태를 월별 또는 분기별로 검토를 수행 하 고 추세 분석</span><span class="sxs-lookup"><span data-stu-id="32846-133">Perform monthly or quarterly reviews of Office 365 Cloud App Security alerts to spot anomalies and analyze trends</span></span>  <br/>  <span data-ttu-id="32846-134">Office 365 클라우드 응용 프로그램 보안 및 주소 새 cyberattacks 및 cybersecurity의 흐름에서 향상 된 기능을 포함 하 여 기존 Office 365 클라우드 응용 프로그램 보안 정책의 월별 또는 분기별로 검토를 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="32846-134">Perform monthly or quarterly reviews of your existing Office 365 Cloud App Security policies to include enhancements in Office 365 Cloud App Security and address new cyberattacks and trends in cybersecurity</span></span>  <br/> |
   
<span data-ttu-id="32846-135">조직의 크기와 모니터링 및 유지 관리 하는 보안 스 태 쳐에 관심을 따라를 포함 하 여 IT 관리 체인에 대 한 월별 요약을 컴파일할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="32846-135">Depending on your organization's size and interest in monitoring and maintaining a security stature, you can compile a monthly summary for your IT management chain that includes:</span></span>
  
- <span data-ttu-id="32846-136">다양 한 유형의 Office 365 클라우드 앱 보안 있는 것으로 식별 하는 보안 문제</span><span class="sxs-lookup"><span data-stu-id="32846-136">The different types of security incidents identified with Office 365 Cloud App Security</span></span>
    
- <span data-ttu-id="32846-137">보안 문제를 발견 하는 문제 발생 횟수 등의 로그를 중앙에서 요약 정보</span><span class="sxs-lookup"><span data-stu-id="32846-137">Summary information from your central log of the security incidents, such as number of incidents detected</span></span>
    
- <span data-ttu-id="32846-138">경고 추세 및 주소가 지정 방법</span><span class="sxs-lookup"><span data-stu-id="32846-138">Alert trends and how they were addressed</span></span>
    
- <span data-ttu-id="32846-139">최신 cybersecurity 추세</span><span class="sxs-lookup"><span data-stu-id="32846-139">The latest cybersecurity trends</span></span>
    
- <span data-ttu-id="32846-140">Office 365 클라우드 응용 프로그램 보안 정책 변경 사항 및 최종 사용자에 대 한 영향에 대 한 권장 사항</span><span class="sxs-lookup"><span data-stu-id="32846-140">Recommendations for Office 365 Cloud App Security policy changes and their impact on end users</span></span>
    
## <a name="activities-after-time-has-passed-since-rolling-out-office-365-cloud-app-security"></a><span data-ttu-id="32846-141">Office 365 클라우드 앱 보안 롤아웃 이후 시간이 경과한 후 활동</span><span class="sxs-lookup"><span data-stu-id="32846-141">Activities after time has passed since rolling out Office 365 Cloud App Security</span></span>

<span data-ttu-id="32846-142">조직의 보안 목표와 현재 기능을 반영 하는 구성으로 다시 이동 하려면 다음 단계를 수행와 시간의 처음 구성 또는 Office 365 클라우드 응용 프로그램 보안 정책을 유지 관리 이후을 통과 하는 경우 Office 365 클라우드 응용 프로그램 보안:</span><span class="sxs-lookup"><span data-stu-id="32846-142">If a protracted amount of time has passed since you initially configured or maintained your Office 365 Cloud App Security policies, take the following steps to get back to a configuration that reflects your organization's security goals and the current capabilities of Office 365 Cloud App Security:</span></span>
  
1. <span data-ttu-id="32846-143">Office 365 클라우드 응용 프로그램 보안에 대 한 마지막 구성 변경의 날짜를 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="32846-143">Determine the date of the last configuration change for Office 365 Cloud App Security.</span></span>
    
2. <span data-ttu-id="32846-p104">현재 Office 365 클라우드 응용 프로그램 보안 구성을 이해 하 고 필요에 따라 해당 정책이 조정 합니다. 예, 알림 전자 메일을 통해 전송 되 고 위치를 알고 있는 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="32846-p104">Understand your current Office 365 Cloud App Security configuration and adjust those policies as needed. For example, make sure you know where alerts are being sent via email.</span></span>
    
3. <span data-ttu-id="32846-146">Office 365 클라우드 응용 프로그램 보안을 마지막으로 구성한 이후 제품 변경 사항에 대 한 [Office 365 클라우드 응용 프로그램 보안의 새로운 기능](new-in-office-365-cas.md) 을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="32846-146">See [what's new in Office 365 Cloud App Security](new-in-office-365-cas.md) for product changes since you last configured Office 365 Cloud App Security.</span></span> 
    
4. <span data-ttu-id="32846-147">Office 365 클라우드 응용 프로그램 보안 경고 및 로그 별색 비정상 상태에 대 한 분석을 수행 하 고 추세를 분석 합니다.</span><span class="sxs-lookup"><span data-stu-id="32846-147">Perform an analysis of Office 365 Cloud App Security alerts and logs to spot anomalies and analyze trends.</span></span>
    
5. <span data-ttu-id="32846-148">최신 보안 위협 요소를 인식 되도록 업계 cybersecurity 추세를 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="32846-148">Check industry cybersecurity trends to become aware of the latest security threats.</span></span>
    
6. <span data-ttu-id="32846-p105">Office 365 클라우드 응용 프로그램 보안 정책의 현재 집합을 수 있도록 하는 변경 내용에 대 한 분석을 수행 합니다. Office 365 클라우드 응용 프로그램 보안 기능 변경 사항, 현재 비정상 상태 및 cybersecurity 추세를 통합 합니다. 새 정책 만들기 또는 기존 정책 변경 내용을 권장 합니다.</span><span class="sxs-lookup"><span data-stu-id="32846-p105">Perform an analysis of the changes that need to be made to the current set of Office 365 Cloud App Security policies. Incorporate Office 365 Cloud App Security feature changes, current anomalies, and cybersecurity trends. Recommend changes to existing policies or the creation of new policies.</span></span>
    
7. <span data-ttu-id="32846-p106">정책 변경 내용을 구현에 대 한 계획을 확인 합니다. 통신 (인사 및 대화)가 필요에 따라 최종 사용자와 제안 된 변경 내용 같은 결과가 발생 합니다.</span><span class="sxs-lookup"><span data-stu-id="32846-p106">Make a plan for implementing the policy changes. Communicate (socialize) the consequences of the proposed changes with your end users as needed.</span></span>
    
8. <span data-ttu-id="32846-154">Office 365 클라우드 응용 프로그램 보안 정책 변경 내용을 구현 합니다.</span><span class="sxs-lookup"><span data-stu-id="32846-154">Implement the Office 365 Cloud App Security policy changes.</span></span>
    
9. <span data-ttu-id="32846-155">최종 사용자에 게 피드백 및 Office 365 클라우드 응용 프로그램 보안 경고를 모니터링 하 고 시간에 따른 정책을 조정 합니다.</span><span class="sxs-lookup"><span data-stu-id="32846-155">Monitor end user feedback and Office 365 Cloud App Security alerts and adjust policies over time.</span></span>
    
## <a name="next-steps"></a><span data-ttu-id="32846-156">다음 단계</span><span class="sxs-lookup"><span data-stu-id="32846-156">Next steps</span></span>

- [<span data-ttu-id="32846-157">활동 조사</span><span class="sxs-lookup"><span data-stu-id="32846-157">Investigate an activity</span></span>](investigate-an-activity-in-office-365-cas.md)
    
- [<span data-ttu-id="32846-158">일시 중단 또는 사용자 계정 복원</span><span class="sxs-lookup"><span data-stu-id="32846-158">Suspend or restore a user account</span></span>](suspend-or-restore-an-account-in-ocas.md)
    
- [<span data-ttu-id="32846-159">앱 사용 권한 관리</span><span class="sxs-lookup"><span data-stu-id="32846-159">Manage app permissions</span></span>](manage-app-permissions-in-ocas.md)
    
- [<span data-ttu-id="32846-160">Office 365 Cloud App Security을 사용하여 앱 검색 결과 검토</span><span class="sxs-lookup"><span data-stu-id="32846-160">Review app discovery findings in Office 365 Cloud App Security</span></span>](review-app-discovery-findings-in-ocas.md)
    
- <span data-ttu-id="32846-161">지원 되는 [웹 트래픽 로그 및 데이터 원본](web-traffic-logs-and-data-sources-for-ocas.md) 목록 보기</span><span class="sxs-lookup"><span data-stu-id="32846-161">View a list of supported [Web traffic logs and data sources](web-traffic-logs-and-data-sources-for-ocas.md)</span></span>
    

