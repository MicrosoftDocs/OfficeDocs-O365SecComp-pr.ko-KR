---
title: Office 365 Cloud App Security 시작
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.audience: ITPro
ms.topic: overview
ms.date: 02/15/2019
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: d9ee4d67-f2b3-42b4-9c9e-c4529904990a
description: Office 365 Cloud App Security를 사용 하 여 시작 하기
ms.openlocfilehash: d6049bb1a36a078c6e5e33c60928bd3ae872c33f
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30219898"
---
# <a name="get-ready-for-office-365-cloud-app-security"></a><span data-ttu-id="610a5-103">Office 365 Cloud App Security 시작</span><span class="sxs-lookup"><span data-stu-id="610a5-103">Get ready for Office 365 Cloud App Security</span></span>
  
|<span data-ttu-id="610a5-104">계산 \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="610a5-104">\*\*\*\*Evaluation\*\* \>\*\*</span></span>|<span data-ttu-id="610a5-105">계획 \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="610a5-105">\*\*\*\*Planning\*\* \>\*\*</span></span>|<span data-ttu-id="610a5-106">배포 \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="610a5-106">\*\*\*\*Deployment\*\* \>\*\*</span></span>|<span data-ttu-id="610a5-107">사용률 \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="610a5-107">\*\*\*\*Utilization\*\*\*\*</span></span>|
|:-----|:-----|:-----|:-----|
|[<span data-ttu-id="610a5-108">평가 시작</span><span class="sxs-lookup"><span data-stu-id="610a5-108">Start evaluating</span></span>](office-365-cas-overview.md) <br/> |<span data-ttu-id="610a5-109">사용자가 여기 있어!</span><span class="sxs-lookup"><span data-stu-id="610a5-109">You are here!</span></span>  <br/> [<span data-ttu-id="610a5-110">다음 단계</span><span class="sxs-lookup"><span data-stu-id="610a5-110">Next step</span></span>](turn-on-office-365-cas.md) <br/> |[<span data-ttu-id="610a5-111">배포 시작</span><span class="sxs-lookup"><span data-stu-id="610a5-111">Start deploying</span></span>](turn-on-office-365-cas.md) <br/> |[<span data-ttu-id="610a5-112">활용 시작</span><span class="sxs-lookup"><span data-stu-id="610a5-112">Start utilizing</span></span>](utilization-activities-for-ocas.md) <br/> |
   
<span data-ttu-id="610a5-p101">조직에 대 한 Office 365 Cloud App Security를 설정 하 고 구현할 때 몇 가지 사항을 고려해 야 합니다. 이 문서를 Office 365 Cloud App Security 계획에 대 한 지침으로 사용 하세요.</span><span class="sxs-lookup"><span data-stu-id="610a5-p101">As you prepare to turn on and implement Office 365 Cloud App Security for your organization, there are a few things to take into account. Use this article as a guide to plan for Office 365 Cloud App Security.</span></span>
    
## <a name="step-1-identify-and-protect-your-global-and-security-administrator-accounts"></a><span data-ttu-id="610a5-115">1 단계: 전역 및 보안 관리자 계정 식별 및 보호</span><span class="sxs-lookup"><span data-stu-id="610a5-115">Step 1: Identify and protect your global and security administrator accounts</span></span>

<span data-ttu-id="610a5-p102">전역 관리자, 보안 관리자 및 보안 독자는 Office 365 Cloud App security 포털에 액세스 하 여 정책을 보고, 경고를 검토 하 고, 보고서를 사용할 수 있습니다. 전역 관리자 및 보안 관리자는 정책을 정의 하 고 다른 작업을 수행 하 여 조직을 보호할 수 있습니다. 자세한 내용은 [Office 365 보안 &amp; 및 준수 센터의 사용 권한을](permissions-in-the-security-and-compliance-center.md)참조 하세요. 예방 조치로 향상 된 사용 권한을 가진 조직의 사용자 계정을 검토 합니다.</span><span class="sxs-lookup"><span data-stu-id="610a5-p102">Global administrators, security administrators, and security readers can access the Office 365 Cloud App Security portal to view policies, review alerts, and use reports. Global administrators and security administrators can define policies and take other actions to protect your organization. (For more information, see [Permissions in the Office 365 Security &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md).) Review your organization's user accounts that have elevated permissions as a precaution.</span></span> 
  
 <span data-ttu-id="610a5-119">**[Office 365 전역 관리자 계정을 보호](https://docs.microsoft.com/office365/enterprise/protect-your-global-administrator-accounts)** 합니다.</span><span class="sxs-lookup"><span data-stu-id="610a5-119">**[Protect your Office 365 global administrator accounts](https://docs.microsoft.com/office365/enterprise/protect-your-global-administrator-accounts)**.</span></span> 
  
## <a name="step-2-turn-on-audit-logging-for-your-organization"></a><span data-ttu-id="610a5-120">2 단계: 조직에 대 한 감사 로깅 설정</span><span class="sxs-lookup"><span data-stu-id="610a5-120">Step 2: Turn on audit logging for your organization</span></span>

<span data-ttu-id="610a5-p103">Office 365 Cloud App Security가 올바르게 작동 하려면 감사 로깅을 켜야 합니다. 이 작업은 일반적으로 Exchange Online 관리자 또는 전역 관리자가 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="610a5-p103">In order for Office 365 Cloud App Security to work correct, audit logging must be turned on. This is typically done by an Exchange Online administrator or a global administrator.</span></span>
  
 <span data-ttu-id="610a5-123">**[Office 365 감사 로그 검색을 설정 하거나 해제](turn-audit-log-search-on-or-off.md)** 합니다.</span><span class="sxs-lookup"><span data-stu-id="610a5-123">**[Turn Office 365 audit log search on or off](turn-audit-log-search-on-or-off.md)**.</span></span> 
  
## <a name="step-3-go-to-the-office-365-cloud-app-security-portal"></a><span data-ttu-id="610a5-124">3 단계: Office 365 Cloud App Security 포털로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="610a5-124">Step 3: Go to the Office 365 Cloud App Security portal</span></span>

<span data-ttu-id="610a5-125">Office 365 Cloud App Security portal로 이동 [https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com) 하 여 로그인 해 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="610a5-125">You can get to the Office 365 Cloud App Security portal by going to [https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com) and signing in.</span></span> 

<span data-ttu-id="610a5-p104">Office 365 보안 &amp; 및 준수 센터에서 찾을 수도 있습니다. 이 작업을 수행 하는 좋은 방법은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="610a5-p104">You can also get there from the Office 365 Security &amp; Compliance Center. Here's one good way to do it:</span></span>

1. <span data-ttu-id="610a5-p105">[https://protection.office.com](https://protection.office.com) 으로 이동 하 여 로그인 합니다. (보안 &amp; 및 준수 센터로 이동 합니다.)</span><span class="sxs-lookup"><span data-stu-id="610a5-p105">Go to [https://protection.office.com](https://protection.office.com) and sign in. (This takes you to the Security &amp; Compliance Center.)</span></span>
    
2. <span data-ttu-id="610a5-130">**경고** \> 로 이동 하 여 **고급 알림을 관리**합니다.</span><span class="sxs-lookup"><span data-stu-id="610a5-130">Go to **Alerts** \> **Manage advanced alerts**.</span></span>
    
3. <span data-ttu-id="610a5-131">office **365 cloud app security로 이동을** 선택 하 여 office 365 cloud app security 포털로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="610a5-131">Choose **Go to Office 365 Cloud App Security** to go to the Office 365 Cloud App Security portal.</span></span><br> <span data-ttu-id="610a5-132">![Office 365 Cloud App Security로 이동 하려면 고급 알림 관리를 선택 합니다.](media/958632d4-03e3-4ade-8e22-d5509db6fca7.png)</span><span class="sxs-lookup"><span data-stu-id="610a5-132">![Choose Manage Advanced Alerts to go to Office 365 Cloud App Security](media/958632d4-03e3-4ade-8e22-d5509db6fca7.png)</span></span><br><span data-ttu-id="610a5-133">Office 365 Cloud App Security 포털로 이동 하면 첫 번째로 표시 되는 페이지는 다음과 같은 이미지의 정책 페이지입니다.</span><span class="sxs-lookup"><span data-stu-id="610a5-133">When you go to the Office 365 Cloud App Security portal, the first page you see is the Policies page, which resembles the following image:</span></span><br><span data-ttu-id="610a5-134">![Office 365 Cloud App Security 포털로 이동 하면 정책 페이지부터 시작 합니다.](media/5cb8833c-4e08-438c-bab3-91b5106f6f3f.png)</span><span class="sxs-lookup"><span data-stu-id="610a5-134">![When you go to the Office 365 Cloud App Security portal, you start with the Policies page](media/5cb8833c-4e08-438c-bab3-91b5106f6f3f.png)</span></span><br>
  
## <a name="step-4-define-policies-and-set-up-alerts-amp-actions"></a><span data-ttu-id="610a5-135">4 단계: 정책 정의 및 알림 &amp; 작업 설정</span><span class="sxs-lookup"><span data-stu-id="610a5-135">Step 4: Define policies and set up alerts &amp; actions</span></span>

<span data-ttu-id="610a5-p106">전역 관리자 및 보안 관리자는 Office 365 Cloud App security에서 정책을 정의 합니다. 정책 정의 프로세스 중에는 알림 및 작업도 설정 됩니다. 알림은 보기에 표시 되거나 전자 메일을 통해 전송 되는 기준 기반 알림입니다.</span><span class="sxs-lookup"><span data-stu-id="610a5-p106">Global administrators and security administrators define policies in Office 365 Cloud App Security. During the process of defining policies, alerts and actions are also set. An alert is a criteria-based notification that appears in a view or is sent via email.</span></span> 
  
<span data-ttu-id="610a5-p107">Office 365 Cloud App Security에는 두 가지 유형의 경고가 있으며, 의심 스러운 활동을 검색 하는 변칙 검색 알림과 조직의 이례적인 일이 될 수 있는 활동에 대해 정의 된 활동 경고가 있습니다. 경고는 조직에 익숙하지 않은 Office 365 환경에서 활동이 발생 하는 경우 전역 관리자 및 보안 관리자에 게 알립니다.</span><span class="sxs-lookup"><span data-stu-id="610a5-p107">There are two types of alerts in Office 365 Cloud App Security: anomaly detection alerts that detect suspicious activity, and activity alerts, which are defined for activities that might be atypical for your organization. Alerts notify global administrators and security administrators when there's an activity in your Office 365 environment that's unusual for your organization.</span></span>
  
<span data-ttu-id="610a5-141">자세히 알아보려면 다음 리소스를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="610a5-141">See the following resources to learn more:</span></span>
  
- [<span data-ttu-id="610a5-142">Office 365 Cloud App Security 활동 정책 및 알림</span><span class="sxs-lookup"><span data-stu-id="610a5-142">Activity policies and alerts in Office 365 Cloud App Security</span></span>](activity-policies-and-alerts.md)
    
- [<span data-ttu-id="610a5-143">Office 365 Cloud App Security 변칙 검색 정책</span><span class="sxs-lookup"><span data-stu-id="610a5-143">Anomaly detection policies in Office 365 Cloud App Security</span></span>](anomaly-detection-policies-in-ocas.md)
    
- [<span data-ttu-id="610a5-144">Office 365 Cloud App Security alerts에 대 한 검토 및 조치 수행</span><span class="sxs-lookup"><span data-stu-id="610a5-144">Review and take action on Office 365 Cloud App Security alerts</span></span>](review-office-365-cas-alerts.md)
    

## <a name="step-5-set-up-conditional-access-app-control"></a><span data-ttu-id="610a5-145">5 단계: 조건부 액세스 앱 컨트롤 설정</span><span class="sxs-lookup"><span data-stu-id="610a5-145">Step 5: Set up Conditional Access App Control</span></span>

<span data-ttu-id="610a5-p108">사용자가 어떤 앱을 사용할 수 있는지와 같은 특정 조건에 따라 조직의 앱에 컨트롤을 설정 하 고 적용 합니다. 사용자 앱 액세스 및 세션 정책을 정의 하 여 중요 한 문서를 다운로드 및 암호화할 수 있는지 여부를 결정 하 고, 특정 앱에 대 한 액세스를 차단 하 고, 특정 앱에 대 한 읽기 전용 모드를 설정 하 고, 회사 이외의 네트워크에서 사용자 세션을 제한 합니다.</span><span class="sxs-lookup"><span data-stu-id="610a5-p108">Set up and enforce controls on your organization's apps, based on certain conditions, such as which users can use what apps, and where. Define user app access and session policies to determine whether sensitive documents can be downloaded and encrypted, block access to certain apps, set up read-only mode for certain apps, and restrict user sessions from non-corporate networks.</span></span>

<span data-ttu-id="610a5-148">자세히 알아보려면 다음 리소스를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="610a5-148">See the following resources to learn more:</span></span>

- [<span data-ttu-id="610a5-149">Office 365 Cloud App Security 조건부 액세스 앱 컨트롤을 사용하여 앱 보호</span><span class="sxs-lookup"><span data-stu-id="610a5-149">Protect apps with Office 365 Cloud App Security Conditional Access App Control</span></span>](ocas-conditional-access-app-control.md)

- [<span data-ttu-id="610a5-150">Office 365 앱용 조건부 액세스 앱 컨트롤 배포</span><span class="sxs-lookup"><span data-stu-id="610a5-150">Deploy Conditional Access App Control for Office 365 apps</span></span>](ocas-deploy-conditional-access-app-control.md)

## <a name="step-6-learn-about-your-organizations-cloud-usage"></a><span data-ttu-id="610a5-151">6 단계: 조직의 클라우드 사용에 대 한 자세한 정보</span><span class="sxs-lookup"><span data-stu-id="610a5-151">Step 6: Learn about your organization's cloud usage</span></span>

<span data-ttu-id="610a5-p109">전역 관리자, 보안 관리자 또는 보안 독자는 보고서 및 클라우드 검색 대시보드 (생산성 앱 검색이 라고도 함)를 통해 조직의 클라우드 사용에 대 한 정보를 확인할 수 있습니다. 이 대시보드는 사용자, 앱, 웹 트래픽 및 위험 수준에 대 한 정보를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="610a5-p109">As a global administrator, security administrator, or security reader, you can learn about your organization's cloud usage through reports and a Cloud Discovery dashboard (also called Productivity App Discovery). This dashboard shows information about users, apps, web traffic, and risk levels.</span></span>
  
![Office 365 CAS 포털에서 클라우드 검색 대시보드 검색 \> 을 선택 합니다.](media/61269290-fd82-4d4b-8045-aea1ebc82287.png)
  
<span data-ttu-id="610a5-155">생산성 앱 검색 대시보드로 이동 하려면 Office 365 cloud App Security 포털에서 **클라우드 검색 대시보드** **검색** \> 을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="610a5-155">To go to the Productivity App Discovery dashboard, in the Office 365 Cloud App Security portal, choose **Discover** \> **Cloud Discovery dashboard**.</span></span>
  
![Office 365 CAS 포털에서 검색을 선택 합니다.](media/73b5299f-94b5-49dd-a00f-154d188eb2c5.png)
  
<span data-ttu-id="610a5-p110">보고서를 필요한 정보로 채우려면 조직의 방화벽 및 프록시에서 로그 파일을 업로드 합니다. 자세한 내용은 다음 리소스를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="610a5-p110">To populate reports with the information you need, upload your log files from your organization's firewalls and proxies. To learn more, see the following resources:</span></span>
  
- [<span data-ttu-id="610a5-159">Office 365 Cloud app Security에서 앱 검색 보고서 만들기</span><span class="sxs-lookup"><span data-stu-id="610a5-159">Create app discovery reports in Office 365 Cloud App Security</span></span>](create-app-discovery-reports-in-ocas.md)
    
- [<span data-ttu-id="610a5-160">Office 365 Cloud App Security을 사용하여 앱 검색 결과 검토</span><span class="sxs-lookup"><span data-stu-id="610a5-160">Review app discovery findings in Office 365 Cloud App Security</span></span>](review-app-discovery-findings-in-ocas.md)
    
## <a name="step-7-manage-apps-that-your-organization-is-using-to-access-office-365"></a><span data-ttu-id="610a5-161">7 단계: 조직에서 Office 365에 액세스 하는 데 사용 하는 앱 관리</span><span class="sxs-lookup"><span data-stu-id="610a5-161">Step 7: Manage apps that your organization is using to access Office 365</span></span>

<span data-ttu-id="610a5-p111">전역 관리자 또는 보안 관리자로 서 조직의 사용자가 Office 365을 통해 장치에서 사용 하는 응용 프로그램, 타사 앱 등의 앱을 관리할 수 있습니다. 예를 들어 사용자가 Office 365에서 사용 하려는 사용자 지정 앱을 다운로드 했다고 가정 합니다. 사용자가 사용 중인 앱을 검토 하거나, 신뢰할 수 없는 앱을 차단 하거나, 추적 목적으로 앱을 승인 된 것으로 표시할 수 있습니다. [Office 365 Cloud App Security를 사용 하 여 OAuth 앱을 관리](manage-app-permissions-in-ocas.md)합니다.</span><span class="sxs-lookup"><span data-stu-id="610a5-p111">As a global administrator or security administrator, you can manage apps, such as custom apps or third-party apps, that people in your organization are using on their devices with Office 365. For example, suppose that someone has downloaded a custom app they want to use with Office 365. You can review the apps people are using, ban untrusted apps, or mark apps as approved for your tracking purposes. [Manage OAuth apps using Office 365 Cloud App Security](manage-app-permissions-in-ocas.md).</span></span>
  
## <a name="step-8-create-a-maintenance-plan"></a><span data-ttu-id="610a5-166">8 단계: 유지 관리 계획 만들기</span><span class="sxs-lookup"><span data-stu-id="610a5-166">Step 8: Create a maintenance plan</span></span>

<span data-ttu-id="610a5-p112">office 365 Cloud App Security를 설정 하 고 구성한 후에는 특정 사용률 작업을 조직의 Office 365 전역 관리자 또는 보안 관리자로 수행 하는 것이 좋습니다. 이러한 작업을 수행 하 여 office 365 Cloud App Security가 올바르게 구성 되어 있고, 정책이 최신 상태 이며, 조직에서 office 365의 가치를 인식 하도록 하는 데 도움이 됩니다. 이 문서를 참조 하 여 이러한 작업을 계획 하는 데 도움을 받을 수 있습니다. [Office 365 Cloud App Security를 시작한 후 사용률 작업](utilization-activities-for-ocas.md)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="610a5-p112">After you have set up and configured Office 365 Cloud App Security, you'll want to perform certain utilization tasks as an Office 365 global administrator or security administrator for your organization. By performing these tasks, you'll help ensure that Office 365 Cloud App Security is configured correctly, your policies are up to date, and your organization realizes value from Office 365. Use this article as a guide to help you plan for these tasks. See [Utilization activities after rolling out Office 365 Cloud App Security](utilization-activities-for-ocas.md).</span></span>

## <a name="optional-step-9-use-your-siem-server-with-office-365-cloud-app-security"></a><span data-ttu-id="610a5-171">반드시 9 단계: Office 365 Cloud App Security에서 siem 서버 사용</span><span class="sxs-lookup"><span data-stu-id="610a5-171">(Optional) Step 9: Use your SIEM server with Office 365 Cloud App Security</span></span>

<span data-ttu-id="610a5-p113">조직에서 siem (보안 정보 및 이벤트 관리) 서버를 사용 하 고 있나요? Office 365 Cloud App Security는 이제 siem server와 통합 하 여 경고에 대 한 중앙 집중식 모니터링을 사용할 수 있습니다. siem 서비스와 통합 하면 일반적인 보안 워크플로를 유지 관리 하면서 클라우드 응용 프로그램을 보다 효율적으로 보호 하 고, 클라우드 기반 및 온-프레미스 이벤트 간의 보안 절차를 자동화 하 고 상관 관계를 유지할 수 있습니다. siem 에이전트는 서버에서 실행 되며, Office 365 Cloud App Security의 알림을 가져오고, 해당 알림을 siem 서버로 스트리밍합니다. [siem integration과 Office 365 Cloud App Security를](integrate-your-siem-server-with-office-365-cas.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="610a5-p113">Is your organization using a security information and event management (SIEM) server? Office 365 Cloud App Security can now integrate with your SIEM server to enable centralized monitoring of alerts. Integrating with a SIEM service allows you to better protect your cloud applications while maintaining your usual security workflow, automating security procedures and correlating between cloud-based and on-premises events. The SIEM agent runs on your server, pulls alerts from Office 365 Cloud App Security, and streams those alerts into your SIEM server. See [SIEM integration with Office 365 Cloud App Security](integrate-your-siem-server-with-office-365-cas.md).</span></span>
  
## <a name="next-steps"></a><span data-ttu-id="610a5-177">다음 단계</span><span class="sxs-lookup"><span data-stu-id="610a5-177">Next steps</span></span>

- [<span data-ttu-id="610a5-178">Office 365 Cloud App Security 켜기</span><span class="sxs-lookup"><span data-stu-id="610a5-178">Turn on Office 365 Cloud App Security</span></span>](turn-on-office-365-cas.md)
    
- <span data-ttu-id="610a5-179">Office 365 Cloud App Security의 강력한 기능을 시연 하 고 개념 증명을 만들 수 있는 실무 환경에 대 한 [테스트 랩 가이드](https://docs.microsoft.com/office365/enterprise/cloud-app-security-for-your-office-365-dev-test-environment) 를 사용해 보십시오.</span><span class="sxs-lookup"><span data-stu-id="610a5-179">Try our [Test Lab Guide](https://docs.microsoft.com/office365/enterprise/cloud-app-security-for-your-office-365-dev-test-environment) for a hands-on experience where you can demonstrate the powerful features of Office 365 Cloud App Security and create a proof of concept.</span></span> 
    

