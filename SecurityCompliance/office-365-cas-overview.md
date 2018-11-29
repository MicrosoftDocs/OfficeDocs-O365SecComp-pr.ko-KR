---
title: Office 365 Cloud App Security 개요
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.audience: ITPro
ms.topic: overview
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MET150
- MOE150
ms.assetid: 81f0ee9a-9645-45ab-ba56-de9cbccab475
description: 'Office 365 클라우드 응용 프로그램 보안을 사용 하면 의심 스러운 활동 대 한 통찰력의 Office 365는 잠재적인 문제를 가진 하 고 필요한 경우 보안 문제를 해결 하는 작업을 수행 하는 상황을 조사할 수 있도록 합니다. '
ms.openlocfilehash: 722c305288798b38ac125a693d9d150446458324
ms.sourcegitcommit: cd452513d8761b2e50b4f9b6cf29422d146307ec
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/28/2018
ms.locfileid: "26864559"
---
# <a name="overview-of-office-365-cloud-app-security"></a><span data-ttu-id="ab03c-103">Office 365 Cloud App Security 개요</span><span class="sxs-lookup"><span data-stu-id="ab03c-103">Overview of Office 365 Cloud App Security</span></span>
  
|<span data-ttu-id="ab03c-104">평가 \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="ab03c-104">\*\*\*\*Evaluation\*\* \>\*\*</span></span>|<span data-ttu-id="ab03c-105">계획 \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="ab03c-105">\*\*\*\*Planning\*\* \>\*\*</span></span>|<span data-ttu-id="ab03c-106">배포 \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="ab03c-106">\*\*\*\*Deployment\*\* \>\*\*</span></span>|<span data-ttu-id="ab03c-107">사용률 \* \* \*</span><span class="sxs-lookup"><span data-stu-id="ab03c-107">\*\*\*\*Utilization\*\*\*\*</span></span>|
|:-----|:-----|:-----|:-----|
|<span data-ttu-id="ab03c-108">여기는!</span><span class="sxs-lookup"><span data-stu-id="ab03c-108">You are here!</span></span>  <br/> [<span data-ttu-id="ab03c-109">다음 단계</span><span class="sxs-lookup"><span data-stu-id="ab03c-109">Next step</span></span>](get-ready-for-office-365-cas.md) <br/> |[<span data-ttu-id="ab03c-110">계획을 시작합니다</span><span class="sxs-lookup"><span data-stu-id="ab03c-110">Start planning</span></span>](get-ready-for-office-365-cas.md) <br/> |[<span data-ttu-id="ab03c-111">배포를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab03c-111">Start deploying</span></span>](turn-on-office-365-cas.md) <br/> |[<span data-ttu-id="ab03c-112">활용 하 여 시작</span><span class="sxs-lookup"><span data-stu-id="ab03c-112">Start utilizing</span></span>](utilization-activities-for-ocas.md) <br/> |
   
> [!NOTE]
> <span data-ttu-id="ab03c-p101">Office 365 클라우드 App 보안은 Office 365 Enterprise e 5에 사용할 수 있습니다. 조직의 다른 Office 365 Enterprise 등록을 사용 하는 경우 Office 365 클라우드 앱 보안 추가 기능으로 구입할 수 있습니다. (전역 관리자는 Office 365 관리 센터에서 선택 **대금 청구** \> **추가 구독**.) 자세한 내용은 참조 [Office 365 플랫폼 서비스 설명: Office 365 보안 &amp; 준수 센터](https://technet.microsoft.com/en-us/library/dn933793.aspx) [구입 또는 비즈니스를 위한 Office 365에 대 한 추가 기능을 편집](https://support.office.com/article/4e7b57d6-b93b-457d-aecd-0ea58bff07a6)하 고 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ab03c-p101">Office 365 Cloud App Security is available in Office 365 Enterprise E5. If your organization is using another Office 365 Enterprise subscription, Office 365 Cloud App Security can be purchased as an add-on. (As a global administrator, in the Office 365 admin center, choose **Billing** \> **Add subscriptions**.) For more information, see [Office 365 Platform Service Description: Office 365 Security &amp; Compliance Center](https://technet.microsoft.com/en-us/library/dn933793.aspx) and [Buy or edit an add-on for Office 365 for business](https://support.office.com/article/4e7b57d6-b93b-457d-aecd-0ea58bff07a6).</span></span> 
  
<span data-ttu-id="ab03c-p102">Office 365 클라우드 앱 보안 제공 의심 스러운 활동에 대 한 통찰력 Office 365에는 잠재적인 문제를 가진 하 고 필요한 경우 보안 문제를 해결 하는 작업을 수행 하는 상황을 조사할 수 있도록 합니다. Office 365 클라우드 응용 프로그램 보안을 함께 트리거된 알림 예외적인 또는 의심 스러운 활동에 대 한 알림을 받을, 어떻게 Office 365에서 조직의 데이터를 액세스 하 고 사용 하 고, 사용자 계정을 현상이 의심 스러운 작업을 일시 중단 하 고 필요 수 있습니다. 사용자가 로그인 할 알림을 트리거한 된 후에 Office 365 응용 프로그램을 백업 합니다. Office 365 클라우드 응용 프로그램 보안 기능을 대략적를이 문서를 읽어보십시오.</span><span class="sxs-lookup"><span data-stu-id="ab03c-p102">Office 365 Cloud App Security gives you insight into suspicious activity in Office 365 so you can investigate situations that are potentially problematic and, if needed, take action to address security issues. With Office 365 Cloud App Security, you can receive notifications of triggered alerts for atypical or suspicious activities, see how your organization's data in Office 365 is accessed and used, suspend user accounts exhibiting suspicious activity, and require users to log back in to Office 365 apps after an alert has been triggered. Read this article to get an overview of Office 365 Cloud App Security features and capabilities.</span></span>
  
    
## <a name="how-to-find-the-office-365-cloud-app-security-portal"></a><span data-ttu-id="ab03c-119">Office 365 클라우드 응용 프로그램 보안 포털을 찾는 방법</span><span class="sxs-lookup"><span data-stu-id="ab03c-119">How to find the Office 365 Cloud App Security portal</span></span>

> [!NOTE]
> <span data-ttu-id="ab03c-p103">Office 365 클라우드 응용 프로그램 보안 포털에 액세스 하려면 전역 관리자, 보안 관리자 또는 보안 판독기 이어야 합니다. 자세한 내용은 참조 [Office 365 보안에 대 한 사용 권한을 &amp; 준수 센터](permissions-in-the-security-and-compliance-center.md)합니다.</span><span class="sxs-lookup"><span data-stu-id="ab03c-p103">To access the Office 365 Cloud App Security portal, you must be a global administrator, security administrator, or security reader. To learn more, see [Permissions in the Office 365 Security &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md).</span></span> 
  
<span data-ttu-id="ab03c-p104">Office 365 보안을 통해 Office 365 클라우드 응용 프로그램 보안 포털을 얻을 수 &amp; 준수 센터입니다. 작업을 수행 하는 한 가지 좋은 방법은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="ab03c-p104">You can get to the Office 365 Cloud App Security portal through the Office 365 Security &amp; Compliance Center. Here's one good way to do it:</span></span>
  
1. <span data-ttu-id="ab03c-p105">이동 [https://security.microsoft.com](https://security.microsoft.com) 및 Office 365에 대 한 작업이 나 교육용 계정을 사용 하 여 로그인 합니다. (이렇게 하면 보안 &amp; 준수 센터.)</span><span class="sxs-lookup"><span data-stu-id="ab03c-p105">Go to [https://security.microsoft.com](https://security.microsoft.com) and sign in using your work or school account for Office 365. (This takes you to the Security &amp; Compliance Center.)</span></span> 
    
2. <span data-ttu-id="ab03c-126">보안에서 &amp; 준수 센터 **알림** 선택 \> **관리 고급 알림**입니다.</span><span class="sxs-lookup"><span data-stu-id="ab03c-126">In the Security &amp; Compliance Center, choose **Alerts** \> **Manage advanced alerts**.</span></span> <br/><span data-ttu-id="ab03c-127">![보안에서 &amp; 준수 센터 Office 365 클라우드 앱 보안으로 이동 하려면 고급 알림 관리를 선택 합니다.](media/958632d4-03e3-4ade-8e22-d5509db6fca7.png)</span><span class="sxs-lookup"><span data-stu-id="ab03c-127">![In the Security &amp; Compliance Center, choose Manage Advanced Alerts to go to Office 365 Cloud App Security](media/958632d4-03e3-4ade-8e22-d5509db6fca7.png)</span></span><br/><span data-ttu-id="ab03c-128">(하는 경우 Office 365 클라우드 앱 보안 아직 활성화 되지 않으면 및 [Office 365 클라우드 응용 프로그램 보안 설정](turn-on-office-365-cas.md)전역 관리자 여야 합니다.)</span><span class="sxs-lookup"><span data-stu-id="ab03c-128">(If Office 365 Cloud App Security is not yet enabled, and you are a global administrator, [turn on Office 365 Cloud App Security](turn-on-office-365-cas.md).)</span></span>
    
3. <span data-ttu-id="ab03c-129">**Office 365 클라우드 응용 프로그램 보안으로 이동**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab03c-129">Choose **Go to Office 365 Cloud App Security**.</span></span> 
    
## <a name="policies"></a><span data-ttu-id="ab03c-130">Policies(정책)</span><span class="sxs-lookup"><span data-stu-id="ab03c-130">Policies</span></span>

<span data-ttu-id="ab03c-p106">Office 365 조직에 대해 정의 된 정책에 작동 하는 클라우드 응용 프로그램 보안 Office 365 클라우드 앱 보안이 포함 된 조직 많은 미리 정의 된 예외 탐지 정책 및 활동 정책에 대 한 여러 서식 파일을 가져옵니다. 이러한 정책은 일반 예외 사항을 검색, 위험한 IP 주소에서 로그인 하는 사용자를 식별, ransomware 활동 감지 감지 하 고, 회사 비 IP 주소 등에서 관리자 작업 하도록 디자인 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="ab03c-p106">Office 365 Cloud App Security works with the policies that are defined for your organization. With Office 365 Cloud App Security, your organization gets many predefined anomaly detection policies and several templates for activity policies. These policies are designed to detect general anomalies, identify users logging in from a risky IP address, detect ransomware activities, detect administrator activities from non-corporate IP addresses, and more.</span></span>
  
![CAS 포털에서 컨트롤 선택 \> 서식 파일을 보거나 정책 서식 파일을 만들려면](media/88f615b4-aa8a-480c-b239-323dfcd628e1.png)
  
<span data-ttu-id="ab03c-135">Office 365 클라우드 응용 프로그램 보안 포털에서 정책 서식 파일을 보기/사용을 **제어** 이동 \> **서식 파일**입니다.</span><span class="sxs-lookup"><span data-stu-id="ab03c-135">To view/use policy templates, in the Office 365 Cloud App Security portal, go to **Control** \> **Templates**.</span></span> 
  
![O365 CAS 포털에서 컨트롤 선택](media/287c2ea9-5172-4697-8e0e-b9ab654105bc.png)
  
<span data-ttu-id="ab03c-137">정책에 대 한 자세한 내용은 다음 리소스를 참조 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab03c-137">To learn more about policies, see the following resources:</span></span>
  
- [<span data-ttu-id="ab03c-138">Office 365 Cloud App Security 활동 정책 및 알림</span><span class="sxs-lookup"><span data-stu-id="ab03c-138">Activity policies and alerts in Office 365 Cloud App Security</span></span>](activity-policies-and-alerts.md)
    
- [<span data-ttu-id="ab03c-139">Office 365 Cloud App Security 변칙 검색 정책</span><span class="sxs-lookup"><span data-stu-id="ab03c-139">Anomaly detection policies in Office 365 Cloud App Security</span></span>](anomaly-detection-policies-in-ocas.md)
    
## <a name="alerts"></a><span data-ttu-id="ab03c-140">알림</span><span class="sxs-lookup"><span data-stu-id="ab03c-140">Alerts</span></span>

<span data-ttu-id="ab03c-p107">정책 정의 된 경우에 검색 된 의심 스러운 또는 예외적인 활동에 대 한 알려줄 알림 나타납니다. 조직에 대 한 경고를 보려면 화면 위쪽 탐색 모음에서 **알림** 을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab03c-p107">When policies are defined, alerts notify you about suspicious or atypical activities that were detected. To view alerts for your organization, choose **Alerts** in the navigation bar across the top of the screen.</span></span> 
  
![경고 페이지에서 경고를 트리거한 된 및 수행 하는 모든 작업을 볼 수 있습니다.](media/3b53d4c9-4b13-435d-8547-8c0f9ae6b914.png)
  
<span data-ttu-id="ab03c-p108">경고가 트리거되는 대로 들어갈 기능에 대 한 자세한 내용을 보려면 해당를 검토할 수 있습니다. 그런 다음 활동 여전히 의심 스러운 있으면 작업을 회수할 수 있습니다. 예는 문제에 대 한 사용자에 게 알릴 수 있습니다에서 Office 365에 로그인 한 사용자를 일시 중단 또는 사용자가 Office 365 응용 프로그램을 다시 로그인 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab03c-p108">As alerts are triggered you can review them to learn more about what is going on. Then, if the activity is still suspicious, you can take action. For example, you can notify a user about an issue, suspend a user from signing in to Office 365, or require a user to sign back in to Office 365 apps.</span></span>
  
<span data-ttu-id="ab03c-147">경고 하는 방법에 대 한 자세한 내용은 다음 리소스를 참조 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab03c-147">To learn more about alerts, see the following resources:</span></span>
  
- [<span data-ttu-id="ab03c-148">Office 365 Cloud App Security 활동 정책 및 알림</span><span class="sxs-lookup"><span data-stu-id="ab03c-148">Activity policies and alerts in Office 365 Cloud App Security</span></span>](activity-policies-and-alerts.md)
    
- [<span data-ttu-id="ab03c-149">Office 365 Cloud App Security 변칙 검색 정책</span><span class="sxs-lookup"><span data-stu-id="ab03c-149">Anomaly detection policies in Office 365 Cloud App Security</span></span>](anomaly-detection-policies-in-ocas.md)
    
- [<span data-ttu-id="ab03c-150">검토 하 고 Office 365 클라우드 응용 프로그램 보안 경고에서 작업 수행</span><span class="sxs-lookup"><span data-stu-id="ab03c-150">Review and take action on Office 365 Cloud App Security alerts</span></span>](review-office-365-cas-alerts.md)
    
## <a name="activity-logs"></a><span data-ttu-id="ab03c-151">활동 로그</span><span class="sxs-lookup"><span data-stu-id="ab03c-151">Activity logs</span></span>

<span data-ttu-id="ab03c-152">Office 365 클라우드 응용 프로그램 보안의 활동 로그 페이지에서 사용자 작업에 대 한 정보 보기</span><span class="sxs-lookup"><span data-stu-id="ab03c-152">View information about user activities on your Activity log page in Office 365 Cloud App Security.</span></span>
  
![O365 CAS 포털에서 조사 선택 \> 활동 로그](media/ec19e77d-4e11-49fc-ab7c-0e8b0c29c93c.png)
  
<span data-ttu-id="ab03c-154">Office 365 클라우드 응용 프로그램 보안 포털에서이 페이지로 이동 하려면 **조사** 로 이동 \> **활동 로그**합니다.</span><span class="sxs-lookup"><span data-stu-id="ab03c-154">To get to this page, in the Office 365 Cloud App Security portal, go to **Investigate** \> **Activity log**.</span></span> 
  
![O365 CAS 포털에서 조사를 선택 합니다.](media/8c7b87c9-71a6-4952-adb2-185e941ffe9a.png)
  
<span data-ttu-id="ab03c-p109">Office 365 클라우드 응용 프로그램 보안 너무 웹 트래픽 로그를 사용할 수 있습니다. 이러한에 포함 된 자세한 내용은 로그 파일, 사용자 작업을가 더 나은 표시 합니다. Barracuda, 파란색 코트, 검사점, Cisco, Clavister, Dell SonicWALL, Fortinet, Juniper, McAfee, Microsoft, 팔로 알토, Sophos, 들면 Squid, Websence, Zscaler, 등의 로그 파일을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ab03c-p109">You can use your web traffic logs with Office 365 Cloud App Security, too. The more details that are included in those log files, the better visibility you'll have into user activity. You can use log files from Barracuda, Blue Coat, Check Point, Cisco, Clavister, Dell SonicWALL, Fortinet, Juniper, McAfee, Microsoft, Palo Alto, Sophos, Squid, Websence, Zscaler, and more.</span></span>
  
[<span data-ttu-id="ab03c-159">Office 365 클라우드 응용 프로그램 보안에 대 한 웹 트래픽 로그 및 데이터 원본에 대 한 설명</span><span class="sxs-lookup"><span data-stu-id="ab03c-159">Learn about web traffic logs and data sources for Office 365 Cloud App Security</span></span>](web-traffic-logs-and-data-sources-for-ocas.md)
  
## <a name="app-permissions"></a><span data-ttu-id="ab03c-160">응용 프로그램 사용 권한</span><span class="sxs-lookup"><span data-stu-id="ab03c-160">App permissions</span></span>

<span data-ttu-id="ab03c-161">Office 365 클라우드 응용 프로그램 보안을 허용 하거나 Office 365의 데이터에 액세스 하는 타사 응용 프로그램을 사용 하 여 조직에서 사람들이 것을 방지 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ab03c-161">With Office 365 Cloud App Security, you can allow or prevent people in your organization to use third-party apps that access data in Office 365.</span></span>
  
![O365 CAS 조사 메뉴에서 앱 사용 권한 관리 페이지를 액세스할 수 있습니다.](media/78272cda-986f-4b3b-bbbe-8c236c74f5d3.png)
  
<span data-ttu-id="ab03c-163">이 페이지를 보려면, **조사** 로 이동 \> **App 사용 권한**입니다.</span><span class="sxs-lookup"><span data-stu-id="ab03c-163">To get to this page, go to **Investigate** \> **App permissions**.</span></span> 
  
![O365 CAS 포털에서 조사를 선택 합니다.](media/8c7b87c9-71a6-4952-adb2-185e941ffe9a.png)
  
[<span data-ttu-id="ab03c-165">Office 365 Cloud App Security을 사용하여 앱 사용 권한 관리</span><span class="sxs-lookup"><span data-stu-id="ab03c-165">Manage app permissions using Office 365 Cloud App Security</span></span>](manage-app-permissions-in-ocas.md)
  
## <a name="cloud-discovery-dashboard"></a><span data-ttu-id="ab03c-166">클라우드 검색 대시보드</span><span class="sxs-lookup"><span data-stu-id="ab03c-166">Cloud Discovery Dashboard</span></span>

<span data-ttu-id="ab03c-p110">조직 내에서 클라우드 앱 사용 현황에 대 한 정보를 표시 하는 **클라우드 검색 대시보드**를 **생산성 응용 프로그램 검색**라고도 합니다. 앱, 사용자, 트래픽, 거래 등이 대시보드를 사용 하는 방법에 대 한 정보를 볼 수 있습니다. 클라우드 검색 대시보드는 다음 이미지와 유사합니다.</span><span class="sxs-lookup"><span data-stu-id="ab03c-p110">The **Cloud Discovery Dashboard**, also referred to as **Productivity App Discovery**, shows information about cloud app usage within your organization. You can view information about apps, users, traffic, transactions, and more using this dashboard. The Cloud Discovery Dashboard resembles the following image:</span></span> 
  
![Office 365 CAS 포털에서 검색을 선택 \> 클라우드 검색 대시보드](media/61269290-fd82-4d4b-8045-aea1ebc82287.png)
  
<span data-ttu-id="ab03c-171">Office 365 클라우드 응용 프로그램 보안 포털에서이 대시보드를 **검색** 하려면 이동 \> **클라우드 검색 대시보드**합니다.</span><span class="sxs-lookup"><span data-stu-id="ab03c-171">To get to this dashboard, in the Office 365 Cloud App Security portal, go to **Discover** \> **Cloud Discovery dashboard**.</span></span> 
  
![Office 365 CAS 포털에서 검색을 선택](media/73b5299f-94b5-49dd-a00f-154d188eb2c5.png)
  
[<span data-ttu-id="ab03c-173">Office 365 Cloud App Security을 사용하여 앱 검색 결과 검토</span><span class="sxs-lookup"><span data-stu-id="ab03c-173">Review app discovery findings in Office 365 Cloud App Security</span></span>](review-app-discovery-findings-in-ocas.md)
  
## <a name="next-steps"></a><span data-ttu-id="ab03c-174">다음 단계</span><span class="sxs-lookup"><span data-stu-id="ab03c-174">Next steps</span></span>

- <span data-ttu-id="ab03c-175">[Office 365 클라우드 응용 프로그램 보안 사용 사례 및 사용 가이드](https://aka.ms/O365CASGuide)</span><span class="sxs-lookup"><span data-stu-id="ab03c-175">Get the [Office 365 Cloud App Security Use Cases and Usage Guide](https://aka.ms/O365CASGuide)</span></span>
    
- [<span data-ttu-id="ab03c-176">Office 365 Cloud App Security 시작하기</span><span class="sxs-lookup"><span data-stu-id="ab03c-176">Get ready for Office 365 Cloud App Security</span></span>](get-ready-for-office-365-cas.md)
    

