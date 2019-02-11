---
title: Office 365 Cloud App Security 시작
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.audience: ITPro
ms.topic: overview
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: d9ee4d67-f2b3-42b4-9c9e-c4529904990a
description: Office 365 클라우드 응용 프로그램 보안을 사용 하 여 시작
ms.openlocfilehash: 1d1ae464278a5d9aafa5a176298f03174b6a37dc
ms.sourcegitcommit: 7e2a0185cadea7f3a6afc5ddc445eac2e1ce22eb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/11/2019
ms.locfileid: "29603699"
---
# <a name="get-ready-for-office-365-cloud-app-security"></a><span data-ttu-id="067e1-103">Office 365 Cloud App Security 시작</span><span class="sxs-lookup"><span data-stu-id="067e1-103">Get ready for Office 365 Cloud App Security</span></span>
  
|<span data-ttu-id="067e1-104">평가 \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="067e1-104">\*\*\*\*Evaluation\*\* \>\*\*</span></span>|<span data-ttu-id="067e1-105">계획 \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="067e1-105">\*\*\*\*Planning\*\* \>\*\*</span></span>|<span data-ttu-id="067e1-106">배포 \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="067e1-106">\*\*\*\*Deployment\*\* \>\*\*</span></span>|<span data-ttu-id="067e1-107">사용률 \* \* \*</span><span class="sxs-lookup"><span data-stu-id="067e1-107">\*\*\*\*Utilization\*\*\*\*</span></span>|
|:-----|:-----|:-----|:-----|
|[<span data-ttu-id="067e1-108">평가 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="067e1-108">Start evaluating</span></span>](office-365-cas-overview.md) <br/> |<span data-ttu-id="067e1-109">여기는!</span><span class="sxs-lookup"><span data-stu-id="067e1-109">You are here!</span></span>  <br/> [<span data-ttu-id="067e1-110">다음 단계</span><span class="sxs-lookup"><span data-stu-id="067e1-110">Next step</span></span>](turn-on-office-365-cas.md) <br/> |[<span data-ttu-id="067e1-111">배포를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="067e1-111">Start deploying</span></span>](turn-on-office-365-cas.md) <br/> |[<span data-ttu-id="067e1-112">활용 하 여 시작</span><span class="sxs-lookup"><span data-stu-id="067e1-112">Start utilizing</span></span>](utilization-activities-for-ocas.md) <br/> |
   
<span data-ttu-id="067e1-p101">설정 하 고 조직에 대 한 Office 365 클라우드 응용 프로그램 보안 (고급 보안 관리 이전의 함)를 구현 하려면 준비할 때는 다음과 같은 사항을 몇가지 사항을 고려 합니다. Office 365 클라우드 응용 프로그램 보안 계획 지침으로이 문서를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="067e1-p101">As you prepare to turn on and implement Office 365 Cloud App Security (formerly known as Advanced Security Management) for your organization, there are a few things to take into account. Use this article as a guide to plan for Office 365 Cloud App Security.</span></span>
    
## <a name="step-1-identify-and-protect-your-global-and-security-administrator-accounts"></a><span data-ttu-id="067e1-115">1 단계:를 식별 하 고 전역 및 보안 관리자 계정 보호</span><span class="sxs-lookup"><span data-stu-id="067e1-115">Step 1: Identify and protect your global and security administrator accounts</span></span>

<span data-ttu-id="067e1-p102">전역 관리자, 보안 관리자 및 보안 독자 정책을 보려면 경고를 검토 하 고 보고서를 사용 하 여를 Office 365 클라우드 응용 프로그램 보안 포털에 액세스할 수 있습니다. 전역 관리자 및 보안 관리자 정책을 정의 하 고 조직을 보호 하기 위한 다른 작업을 수행할 수 있습니다. (자세한 내용은 참조 [Office 365 보안에 대 한 사용 권한을 &amp; 준수 센터](permissions-in-the-security-and-compliance-center.md).) 더 높은 권한이 예방 조치로 조직의 사용자 계정을 검토 합니다.</span><span class="sxs-lookup"><span data-stu-id="067e1-p102">Global administrators, security administrators, and security readers can access the Office 365 Cloud App Security portal to view policies, review alerts, and use reports. Global administrators and security administrators can define policies and take other actions to protect your organization. (For more information, see [Permissions in the Office 365 Security &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md).) Review your organization's user accounts that have elevated permissions as a precaution.</span></span> 
  
 <span data-ttu-id="067e1-119">**[암호로 보호 Office 365 전역 관리자 계정](https://docs.microsoft.com/office365/enterprise/protect-your-global-administrator-accounts)** 입니다.</span><span class="sxs-lookup"><span data-stu-id="067e1-119">**[Protect your Office 365 global administrator accounts](https://docs.microsoft.com/office365/enterprise/protect-your-global-administrator-accounts)**.</span></span> 
  
## <a name="step-2-turn-on-audit-logging-for-your-organization"></a><span data-ttu-id="067e1-120">2 단계: 조직에 대해 감사 로깅을 설정합니다</span><span class="sxs-lookup"><span data-stu-id="067e1-120">Step 2: Turn on audit logging for your organization</span></span>

<span data-ttu-id="067e1-p103">올바른 작동 하도록 Office 365 클라우드 응용 프로그램 보안에 대 한 순서로 감사 로깅을 설정 해야 합니다. 이 Exchange Online 관리자 또는 전역 관리자가 일반적으로 수행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="067e1-p103">In order for Office 365 Cloud App Security to work correct, audit logging must be turned on. This is typically done by an Exchange Online administrator or a global administrator.</span></span>
  
 <span data-ttu-id="067e1-123">**[Office 365 설정 또는 해제 로그 검색 감사](turn-audit-log-search-on-or-off.md)** 합니다.</span><span class="sxs-lookup"><span data-stu-id="067e1-123">**[Turn Office 365 audit log search on or off](turn-audit-log-search-on-or-off.md)**.</span></span> 
  
## <a name="step-3-go-to-the-office-365-cloud-app-security-portal"></a><span data-ttu-id="067e1-124">3 단계: 포털로 이동 하는 Office 365 클라우드 응용 프로그램 보안</span><span class="sxs-lookup"><span data-stu-id="067e1-124">Step 3: Go to the Office 365 Cloud App Security portal</span></span>

<span data-ttu-id="067e1-125">으로 이동 하 여 Office 365 클라우드 응용 프로그램 보안 포털을 얻을 수 [https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com) 로그인 하 고 있습니다.</span><span class="sxs-lookup"><span data-stu-id="067e1-125">You can get to the Office 365 Cloud App Security portal by going to [https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com) and signing in.</span></span> 

<span data-ttu-id="067e1-p104">Office 365 보안에서 다음과 같은 얻을 수도 있습니다 &amp; 준수 센터입니다. 작업을 수행 하는 한 가지 좋은 방법은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="067e1-p104">You can also get there from the Office 365 Security &amp; Compliance Center. Here's one good way to do it:</span></span>

1. <span data-ttu-id="067e1-p105">이동 [https://protection.office.com](https://protection.office.com) 및 sign in. (이렇게 하면 보안 &amp; 준수 센터.)</span><span class="sxs-lookup"><span data-stu-id="067e1-p105">Go to [https://protection.office.com](https://protection.office.com) and sign in. (This takes you to the Security &amp; Compliance Center.)</span></span>
    
2. <span data-ttu-id="067e1-130">**경고** 로 이동 \> **관리 고급 알림**입니다.</span><span class="sxs-lookup"><span data-stu-id="067e1-130">Go to **Alerts** \> **Manage advanced alerts**.</span></span>
    
3. <span data-ttu-id="067e1-131">**Office 365 클라우드 앱 보안으로 이동** 하 여 Office 365 클라우드 응용 프로그램 보안 포털에 이동 하려면 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="067e1-131">Choose **Go to Office 365 Cloud App Security** to go to the Office 365 Cloud App Security portal.</span></span><br> <span data-ttu-id="067e1-132">![Office 365 클라우드 앱 보안으로 이동 하려면 고급 알림 관리를 선택 합니다.](media/958632d4-03e3-4ade-8e22-d5509db6fca7.png)</span><span class="sxs-lookup"><span data-stu-id="067e1-132">![Choose Manage Advanced Alerts to go to Office 365 Cloud App Security](media/958632d4-03e3-4ade-8e22-d5509db6fca7.png)</span></span><br><span data-ttu-id="067e1-133">Office 365 클라우드 응용 프로그램 보안 포털에 이동할 때 표시 첫 페이지는 다음 이미지와 비슷합니다 정책 페이지의:</span><span class="sxs-lookup"><span data-stu-id="067e1-133">When you go to the Office 365 Cloud App Security portal, the first page you see is the Policies page, which resembles the following image:</span></span><br><span data-ttu-id="067e1-134">![정책 페이지로 시작 하 여 Office 365 클라우드 응용 프로그램 보안 포털에 이동할 때](media/5cb8833c-4e08-438c-bab3-91b5106f6f3f.png)</span><span class="sxs-lookup"><span data-stu-id="067e1-134">![When you go to the Office 365 Cloud App Security portal, you start with the Policies page](media/5cb8833c-4e08-438c-bab3-91b5106f6f3f.png)</span></span><br>
  
## <a name="step-4-define-policies-and-set-up-alerts-amp-actions"></a><span data-ttu-id="067e1-135">4 단계: 정책을 정의 하 고 알림을 설정할 &amp; 작업</span><span class="sxs-lookup"><span data-stu-id="067e1-135">Step 4: Define policies and set up alerts &amp; actions</span></span>

<span data-ttu-id="067e1-p106">전역 관리자 및 보안 관리자가 Office 365 클라우드 응용 프로그램 보안에서 정책을 정의 합니다. 정책 정의 하는 과정 알림 및 작업은도 함께 설정 합니다. 알림을 보기에 표시 또는 전자 메일을 통해 전송 되는 조건 기반 알림입니다.</span><span class="sxs-lookup"><span data-stu-id="067e1-p106">Global administrators and security administrators define policies in Office 365 Cloud App Security. During the process of defining policies, alerts and actions are also set. An alert is a criteria-based notification that appears in a view or is sent via email.</span></span> 
  
<span data-ttu-id="067e1-p107">Office 365 클라우드 응용 프로그램 보안에 대 한 알림 메시지에 두가지 유형이: 의심 스러운 활동을 검색 하는 예외 감지 경고 및 조직에 대 한 예외적인 될 수 있는 작업에 대해 정의 되는 활동 경고 합니다. 알림 조직에 대 한 일반적인 하지 않은 Office 365 환경에서 활동 때 전역 관리자 및 보안 관리자를 알립니다.</span><span class="sxs-lookup"><span data-stu-id="067e1-p107">There are two types of alerts in Office 365 Cloud App Security: anomaly detection alerts that detect suspicious activity, and activity alerts, which are defined for activities that might be atypical for your organization. Alerts notify global administrators and security administrators when there's an activity in your Office 365 environment that's unusual for your organization.</span></span>
  
<span data-ttu-id="067e1-141">자세한 내용은 다음 리소스를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="067e1-141">See the following resources to learn more:</span></span>
  
- [<span data-ttu-id="067e1-142">Office 365 Cloud App Security 활동 정책 및 알림</span><span class="sxs-lookup"><span data-stu-id="067e1-142">Activity policies and alerts in Office 365 Cloud App Security</span></span>](activity-policies-and-alerts.md)
    
- [<span data-ttu-id="067e1-143">Office 365 Cloud App Security 변칙 검색 정책</span><span class="sxs-lookup"><span data-stu-id="067e1-143">Anomaly detection policies in Office 365 Cloud App Security</span></span>](anomaly-detection-policies-in-ocas.md)
    
- [<span data-ttu-id="067e1-144">검토 하 고 Office 365 클라우드 응용 프로그램 보안 경고에서 작업 수행</span><span class="sxs-lookup"><span data-stu-id="067e1-144">Review and take action on Office 365 Cloud App Security alerts</span></span>](review-office-365-cas-alerts.md)
    
## <a name="step-5-learn-about-your-organizations-cloud-usage"></a><span data-ttu-id="067e1-145">5 단계: 조직의 클라우드 사용 현황에 대 한 설명</span><span class="sxs-lookup"><span data-stu-id="067e1-145">Step 5: Learn about your organization's cloud usage</span></span>

<span data-ttu-id="067e1-p108">전역 관리자, 보안 관리자 또는 보안 판독기, 보고서 및 (생산성 응용 프로그램 검색 라고도 함) 클라우드 검색 대시보드를 통해 조직의 클라우드 사용 하는 방법을 배울 수 있습니다. 이 대시보드는 사용자, 앱, 웹 트래픽 및 위험 수준에 대 한 정보를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="067e1-p108">As a global administrator, security administrator, or security reader, you can learn about your organization's cloud usage through reports and a Cloud Discovery dashboard (also called Productivity App Discovery). This dashboard shows information about users, apps, web traffic, and risk levels.</span></span>
  
![Office 365 CAS 포털에서 검색을 선택 \> 클라우드 검색 대시보드](media/61269290-fd82-4d4b-8045-aea1ebc82287.png)
  
<span data-ttu-id="067e1-149">Office 365 클라우드 응용 프로그램 보안 포털에서 생산성 응용 프로그램 검색 대시보드를 이동 하려면 **검색** 선택 \> **클라우드 검색 대시보드**합니다.</span><span class="sxs-lookup"><span data-stu-id="067e1-149">To go to the Productivity App Discovery dashboard, in the Office 365 Cloud App Security portal, choose **Discover** \> **Cloud Discovery dashboard**.</span></span>
  
![Office 365 CAS 포털에서 검색을 선택](media/73b5299f-94b5-49dd-a00f-154d188eb2c5.png)
  
<span data-ttu-id="067e1-p109">필요한 정보를 사용 하 여 보고서를 채우려면 조직의 방화벽 및 프록시에서 로그 파일을 업로드 합니다. 자세한 내용은 다음 리소스를 참조 합니다.</span><span class="sxs-lookup"><span data-stu-id="067e1-p109">To populate reports with the information you need, upload your log files from your organization's firewalls and proxies. To learn more, see the following resources:</span></span>
  
- [<span data-ttu-id="067e1-153">Office 365 클라우드 앱 보안에서 app 검색 보고서 만들기</span><span class="sxs-lookup"><span data-stu-id="067e1-153">Create app discovery reports in Office 365 Cloud App Security</span></span>](create-app-discovery-reports-in-ocas.md)
    
- [<span data-ttu-id="067e1-154">Office 365 Cloud App Security을 사용하여 앱 검색 결과 검토</span><span class="sxs-lookup"><span data-stu-id="067e1-154">Review app discovery findings in Office 365 Cloud App Security</span></span>](review-app-discovery-findings-in-ocas.md)
    
## <a name="step-6-manage-apps-that-your-organization-is-using-to-access-office-365"></a><span data-ttu-id="067e1-155">조직에서 Office 365 액세스를 사용 하는 앱을 관리 하는 6 단계:</span><span class="sxs-lookup"><span data-stu-id="067e1-155">Step 6: Manage apps that your organization is using to access Office 365</span></span>

<span data-ttu-id="067e1-p110">전역 관리자 또는 보안 관리자, 예: 사용자 지정 응용 프로그램 또는 Office 365를 통해 장치에 조직에서 사용자를 사용 하는 타사 응용 프로그램, 응용 프로그램을 관리할 수 있습니다. 예, Office 365와 함께 사용 하 여 원하는 사용자 지정 앱을 다운로드 한가 다른 사용자 경우를 가정해 보겠습니다. 사용자를 사용 하는 앱을 검토 하, 신뢰할 수 없는 앱을 금지 하거나을 추적 목적에 대 한 승인 앱을 표시할 수 있습니다. [Office 365 클라우드 응용 프로그램 보안을 사용 하 여 관리 OAuth 앱](manage-app-permissions-in-ocas.md)입니다.</span><span class="sxs-lookup"><span data-stu-id="067e1-p110">As a global administrator or security administrator, you can manage apps, such as custom apps or third-party apps, that people in your organization are using on their devices with Office 365. For example, suppose that someone has downloaded a custom app they want to use with Office 365. You can review the apps people are using, ban untrusted apps, or mark apps as approved for your tracking purposes. [Manage OAuth apps using Office 365 Cloud App Security](manage-app-permissions-in-ocas.md).</span></span>
  
## <a name="step-7-use-your-siem-server-with-office-365-cloud-app-security"></a><span data-ttu-id="067e1-160">7 단계: SIEM 서버를 사용 하 여 Office 365 클라우드 응용 프로그램 보안</span><span class="sxs-lookup"><span data-stu-id="067e1-160">Step 7: Use your SIEM server with Office 365 Cloud App Security</span></span>

<span data-ttu-id="067e1-p111">보안 정보 및 이벤트 관리 (SIEM) 서버를 사용 하 여 조직의? Office 365 클라우드 앱 보안 이제 알림 중앙 집중화 된 모니터링을 활성화 하려면 SIEM 서버와 통합할 수 있습니다. SIEM 서비스와 통합 하면 아주 좋음, 일반적인 보안 워크플로 유지 관리 하 고, 보안 절차를 자동화 하 고, 클라우드 기반 간의 상호 연관 시키는 하면서 클라우드 응용 프로그램을 보호 하기 위해 수 있으며 온-프레미스 이벤트입니다. 메뉴 및 도구 모음을 SIEM 에이전트 서버에서 실행 Office 365 클라우드 응용 프로그램 보안에서 알림을 가져오는 SIEM 서버에 이러한 알림을 스트리밍합니다. [Office 365 클라우드 응용 프로그램 보안 SIEM 통합](integrate-your-siem-server-with-office-365-cas.md)을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="067e1-p111">Is your organization using a security information and event management (SIEM) server? Office 365 Cloud App Security can now integrate with your SIEM server to enable centralized monitoring of alerts. Integrating with a SIEM service allows you to better protect your cloud applications while maintaining your usual security workflow, automating security procedures and correlating between cloud-based and on-premises events. The SIEM agent runs on your server, pulls alerts from Office 365 Cloud App Security, and streams those alerts into your SIEM server. See [SIEM integration with Office 365 Cloud App Security](integrate-your-siem-server-with-office-365-cas.md).</span></span>
  
## <a name="next-steps"></a><span data-ttu-id="067e1-166">다음 단계</span><span class="sxs-lookup"><span data-stu-id="067e1-166">Next steps</span></span>

- [<span data-ttu-id="067e1-167">Office 365 Cloud App Security 켜기</span><span class="sxs-lookup"><span data-stu-id="067e1-167">Turn on Office 365 Cloud App Security</span></span>](turn-on-office-365-cas.md)
    
- <span data-ttu-id="067e1-168">Office 365 클라우드 응용 프로그램 보안의 강력한 기능을 설명 하 고 기술적 개념 증명을 만들 수 있는 실습 환경에 대 한 [테스트 랩 가이드](https://docs.microsoft.com/office365/enterprise/cloud-app-security-for-your-office-365-dev-test-environment) 를 시도 합니다.</span><span class="sxs-lookup"><span data-stu-id="067e1-168">Try our [Test Lab Guide](https://docs.microsoft.com/office365/enterprise/cloud-app-security-for-your-office-365-dev-test-environment) for a hands-on experience where you can demonstrate the powerful features of Office 365 Cloud App Security and create a proof of concept.</span></span> 
    

