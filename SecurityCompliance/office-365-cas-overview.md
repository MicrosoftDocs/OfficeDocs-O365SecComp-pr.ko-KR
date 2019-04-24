---
title: Overview of Office 365 Cloud App Security
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 01/22/2019
ms.audience: ITPro
ms.topic: overview
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MET150
- MOE150
ms.assetid: 81f0ee9a-9645-45ab-ba56-de9cbccab475
description: 'office 365 Cloud App Security에서는 office 365의 의심 스러운 활동에 대 한 정보를 제공 하므로 문제가 발생할 가능성이 있는 상황을 조사 하 고, 필요한 경우 보안 문제 해결에 대 한 조치를 취할 수 있습니다. '
ms.openlocfilehash: 960e4c75a4da13e1a0365f75d290cd18587abd58
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32263082"
---
# <a name="overview-of-office-365-cloud-app-security"></a><span data-ttu-id="78622-103">Overview of Office 365 Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="78622-103">Overview of Office 365 Cloud App Security</span></span>
  
|<span data-ttu-id="78622-104">계산 \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="78622-104">\*\*\*\*Evaluation\*\* \>\*\*</span></span>|<span data-ttu-id="78622-105">계획 \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="78622-105">\*\*\*\*Planning\*\* \>\*\*</span></span>|<span data-ttu-id="78622-106">배포 \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="78622-106">\*\*\*\*Deployment\*\* \>\*\*</span></span>|<span data-ttu-id="78622-107">사용률 \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="78622-107">\*\*\*\*Utilization\*\*\*\*</span></span>|
|:-----|:-----|:-----|:-----|
|<span data-ttu-id="78622-108">사용자가 여기 있어!</span><span class="sxs-lookup"><span data-stu-id="78622-108">You are here!</span></span>  <br/> [<span data-ttu-id="78622-109">다음 단계</span><span class="sxs-lookup"><span data-stu-id="78622-109">Next step</span></span>](get-ready-for-office-365-cas.md) <br/> |[<span data-ttu-id="78622-110">계획 시작</span><span class="sxs-lookup"><span data-stu-id="78622-110">Start planning</span></span>](get-ready-for-office-365-cas.md) <br/> |[<span data-ttu-id="78622-111">배포 시작</span><span class="sxs-lookup"><span data-stu-id="78622-111">Start deploying</span></span>](turn-on-office-365-cas.md) <br/> |[<span data-ttu-id="78622-112">활용 시작</span><span class="sxs-lookup"><span data-stu-id="78622-112">Start utilizing</span></span>](utilization-activities-for-ocas.md) <br/> |
   
> [!NOTE]
> <span data-ttu-id="78622-113">office 365 Cloud App Security는 office 365 Enterprise E5에서 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="78622-113">Office 365 Cloud App Security is available in Office 365 Enterprise E5.</span></span> <span data-ttu-id="78622-114">조직에서 다른 office 365 Enterprise 구독을 사용 하는 경우 office 365 Cloud App Security를 추가 기능으로 구입할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="78622-114">If your organization is using another Office 365 Enterprise subscription, Office 365 Cloud App Security can be purchased as an add-on.</span></span> <span data-ttu-id="78622-115">(전역 관리자 인 경우 Microsoft 365 관리 센터에서 **청구** \> **구독 추가**를 선택 합니다.) 자세한 내용은 [office 365 플랫폼 서비스 설명: office 365 보안 &amp; 및 준수 센터](https://docs.microsoft.com/office365/servicedescriptions/office-365-platform-service-description/office-365-securitycompliance-center) 및 [비즈니스용 office 365 용 추가 기능 구입 또는 편집](https://docs.microsoft.com/office365/admin/subscriptions-and-billing/buy-or-edit-an-add-on)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="78622-115">(As a global administrator, in the Microsoft 365 admin center, choose **Billing** \> **Add subscriptions**.) For more information, see [Office 365 Platform Service Description: Office 365 Security &amp; Compliance Center](https://docs.microsoft.com/office365/servicedescriptions/office-365-platform-service-description/office-365-securitycompliance-center) and [Buy or edit an add-on for Office 365 for business](https://docs.microsoft.com/office365/admin/subscriptions-and-billing/buy-or-edit-an-add-on).</span></span> 
  
<span data-ttu-id="78622-116">office 365 Cloud App Security에서는 문제가 발생할 가능성이 있는 상황을 조사 하 고, 필요한 경우 보안 문제 해결에 대 한 조치를 취할 수 있도록 office 365의 의심 스러운 활동에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="78622-116">Office 365 Cloud App Security gives you insight into suspicious activity in Office 365 so you can investigate situations that are potentially problematic and, if needed, take action to address security issues.</span></span> <span data-ttu-id="78622-117">office 365 Cloud App Security를 사용 하 여 이례적인 또는 의심 스러운 활동에 대 한 트리거된 알림의 알림을 받을 수 있으며, office 365에서 조직의 데이터를 액세스 하 여 사용 하는 방법, 사용자 계정 일시 중단 활동이 발생 하는 방식 및 요구 사항을 참조 하세요. 경고가 트리거된 후 Office 365 앱에 다시 로그인 하는 사용자입니다.</span><span class="sxs-lookup"><span data-stu-id="78622-117">With Office 365 Cloud App Security, you can receive notifications of triggered alerts for atypical or suspicious activities, see how your organization's data in Office 365 is accessed and used, suspend user accounts exhibiting suspicious activity, and require users to log back in to Office 365 apps after an alert has been triggered.</span></span> <span data-ttu-id="78622-118">이 문서를 읽으면 Office 365 Cloud App Security 기능 및 기능에 대 한 개요를 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="78622-118">Read this article to get an overview of Office 365 Cloud App Security features and capabilities.</span></span>
  
    
## <a name="how-to-find-the-office-365-cloud-app-security-portal"></a><span data-ttu-id="78622-119">Office 365 Cloud App Security 포털을 찾는 방법</span><span class="sxs-lookup"><span data-stu-id="78622-119">How to find the Office 365 Cloud App Security portal</span></span>

> [!NOTE]
> <span data-ttu-id="78622-120">office 365 Cloud App Security 포털에 액세스 하려면 office 365 전역 관리자, 보안 관리자 또는 보안 판독기 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="78622-120">To access the Office 365 Cloud App Security portal, you must be an Office 365 global administrator, security administrator, or security reader.</span></span> <span data-ttu-id="78622-121">자세한 내용은 [Office 365 보안 &amp; 및 준수 센터의 사용 권한](permissions-in-the-security-and-compliance-center.md)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="78622-121">To learn more, see [Permissions in the Office 365 Security &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md).</span></span> 
  
<span data-ttu-id="78622-122">Office 365 Cloud App Security portal로 이동 [https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com) 하 여 로그인 해 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="78622-122">You can get to the Office 365 Cloud App Security portal by going to [https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com) and signing in.</span></span> 

<span data-ttu-id="78622-123">Office 365 보안 &amp; 및 준수 센터에서 찾을 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="78622-123">You can also get there from the Office 365 Security &amp; Compliance Center.</span></span> <span data-ttu-id="78622-124">이 작업을 수행 하는 좋은 방법은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="78622-124">Here's one good way to do it:</span></span>
  
1. <span data-ttu-id="78622-125">[https://protection.office.com](https://protection.office.com) 으로 이동 하 여 Office 365에 대 한 회사 또는 학교 계정을 사용 하 여 로그인 합니다.</span><span class="sxs-lookup"><span data-stu-id="78622-125">Go to [https://protection.office.com](https://protection.office.com) and sign in using your work or school account for Office 365.</span></span> <span data-ttu-id="78622-126">(보안 &amp; 및 준수 센터로 이동 합니다.)</span><span class="sxs-lookup"><span data-stu-id="78622-126">(This takes you to the Security &amp; Compliance Center.)</span></span>
    
2. <span data-ttu-id="78622-127">보안 &amp; 및 준수 센터에서 **경고** \> **고급 알림 관리**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="78622-127">In the Security &amp; Compliance Center, choose **Alerts** \> **Manage advanced alerts**.</span></span> <br/><span data-ttu-id="78622-128">![Office 365 Cloud App Security로 이동 하려면 고급 알림 관리를 선택 합니다.](media/958632d4-03e3-4ade-8e22-d5509db6fca7.png)</span><span class="sxs-lookup"><span data-stu-id="78622-128">![Choose Manage Advanced Alerts to go to Office 365 Cloud App Security](media/958632d4-03e3-4ade-8e22-d5509db6fca7.png)</span></span><br/><span data-ttu-id="78622-129">(office 365 cloud app security이 아직 사용 하도록 설정 되어 있지 않고 전역 관리자 인 경우 [office 365 Cloud App Security를 켜십시오](turn-on-office-365-cas.md).)</span><span class="sxs-lookup"><span data-stu-id="78622-129">(If Office 365 Cloud App Security is not yet enabled, and you are a global administrator, [turn on Office 365 Cloud App Security](turn-on-office-365-cas.md).)</span></span>
    
3. <span data-ttu-id="78622-130">**Office 365 Cloud App Security로 이동을**선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="78622-130">Choose **Go to Office 365 Cloud App Security**.</span></span> 
    
## <a name="policies"></a><span data-ttu-id="78622-131">정책도</span><span class="sxs-lookup"><span data-stu-id="78622-131">Policies</span></span>

<span data-ttu-id="78622-132">Office 365 Cloud App Security는 조직에 대해 정의 된 정책에 따라 작동 합니다.</span><span class="sxs-lookup"><span data-stu-id="78622-132">Office 365 Cloud App Security works with the policies that are defined for your organization.</span></span> <span data-ttu-id="78622-133">Office 365 Cloud App Security를 사용 하는 경우 조직에는 몇 가지 미리 정의 된 변칙 검색 정책과 활동 정책에 대 한 여러 서식 파일이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="78622-133">With Office 365 Cloud App Security, your organization gets many predefined anomaly detection policies and several templates for activity policies.</span></span> <span data-ttu-id="78622-134">이러한 정책은 일반적인 예외를 감지 하 고 위험한 ip 주소에서 로그인 하는 사용자를 식별 하며, 랜 섬 웨어 활동을 감지 하 고, 회사 이외의 IP 주소에서 관리자 활동을 검색 하는 등의 작업을 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="78622-134">These policies are designed to detect general anomalies, identify users logging in from a risky IP address, detect ransomware activities, detect administrator activities from non-corporate IP addresses, and more.</span></span>
  
![CAS 포털에서 정책 템플릿을 보거나 만들 \> 컨트롤 템플릿을 선택 합니다.](media/88f615b4-aa8a-480c-b239-323dfcd628e1.png)
  
<span data-ttu-id="78622-136">정책 템플릿을 보거나 사용 하려면 Office 365 Cloud App Security 포털에서 **Control** \> **templates**로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="78622-136">To view/use policy templates, in the Office 365 Cloud App Security portal, go to **Control** \> **Templates**.</span></span> 
  
![O365 CAS 포털에서 Control을 선택 합니다.](media/287c2ea9-5172-4697-8e0e-b9ab654105bc.png)
  
<span data-ttu-id="78622-138">정책에 대 한 자세한 내용은 다음 리소스를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="78622-138">To learn more about policies, see the following resources:</span></span>
  
- [<span data-ttu-id="78622-139">Office 365 Cloud App Security 활동 정책 및 알림</span><span class="sxs-lookup"><span data-stu-id="78622-139">Activity policies and alerts in Office 365 Cloud App Security</span></span>](activity-policies-and-alerts.md)
    
- [<span data-ttu-id="78622-140">Office 365 Cloud App Security 변칙 검색 정책</span><span class="sxs-lookup"><span data-stu-id="78622-140">Anomaly detection policies in Office 365 Cloud App Security</span></span>](anomaly-detection-policies-in-ocas.md)
    
## <a name="alerts"></a><span data-ttu-id="78622-141">경고</span><span class="sxs-lookup"><span data-stu-id="78622-141">Alerts</span></span>

<span data-ttu-id="78622-142">정책이 정의 되 면 감지 된 의심 스러운 활동 또는 이례적인 작업에 대 한 알림을 받습니다.</span><span class="sxs-lookup"><span data-stu-id="78622-142">When policies are defined, alerts notify you about suspicious or atypical activities that were detected.</span></span> <span data-ttu-id="78622-143">조직의 알림을 보려면 화면 맨 위에 있는 탐색 모음에서 **경고** 를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="78622-143">To view alerts for your organization, choose **Alerts** in the navigation bar across the top of the screen.</span></span> 
  
![알림 페이지에서 트리거된 알림과 수행한 모든 작업을 확인할 수 있습니다.](media/3b53d4c9-4b13-435d-8547-8c0f9ae6b914.png)
  
<span data-ttu-id="78622-145">알림이 트리거되면 알림을 검토 하 여 진행 중인 작업에 대해 자세히 알아볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="78622-145">As alerts are triggered you can review them to learn more about what is going on.</span></span> <span data-ttu-id="78622-146">그런 다음 활동이 여전히 의심 스 러 되 면 조치를 취할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="78622-146">Then, if the activity is still suspicious, you can take action.</span></span> <span data-ttu-id="78622-147">예를 들어 사용자에 게 문제를 알리거나, 사용자가 office 365에 로그인 하지 못하도록 일시 중단 하거나, 사용자가 office 365 앱에 다시 로그인 하도록 요구할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="78622-147">For example, you can notify a user about an issue, suspend a user from signing in to Office 365, or require a user to sign back in to Office 365 apps.</span></span>
  
<span data-ttu-id="78622-148">경고에 대 한 자세한 내용은 다음 리소스를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="78622-148">To learn more about alerts, see the following resources:</span></span>
  
- [<span data-ttu-id="78622-149">Office 365 Cloud App Security 활동 정책 및 알림</span><span class="sxs-lookup"><span data-stu-id="78622-149">Activity policies and alerts in Office 365 Cloud App Security</span></span>](activity-policies-and-alerts.md)
    
- [<span data-ttu-id="78622-150">Office 365 Cloud App Security 변칙 검색 정책</span><span class="sxs-lookup"><span data-stu-id="78622-150">Anomaly detection policies in Office 365 Cloud App Security</span></span>](anomaly-detection-policies-in-ocas.md)
    
- [<span data-ttu-id="78622-151">Office 365 Cloud App Security alerts에 대 한 검토 및 조치 수행</span><span class="sxs-lookup"><span data-stu-id="78622-151">Review and take action on Office 365 Cloud App Security alerts</span></span>](review-office-365-cas-alerts.md)
    
## <a name="activity-logs"></a><span data-ttu-id="78622-152">활동 로그</span><span class="sxs-lookup"><span data-stu-id="78622-152">Activity logs</span></span>

<span data-ttu-id="78622-153">Office 365 Cloud App Security의 활동 로그 페이지에 있는 사용자 작업에 대 한 정보를 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="78622-153">View information about user activities on your Activity log page in Office 365 Cloud App Security.</span></span>
  
![O365 CAS 포털에서 작업 로그 조사 \> 를 선택 합니다.](media/ec19e77d-4e11-49fc-ab7c-0e8b0c29c93c.png)
  
<span data-ttu-id="78622-155">이 페이지에 액세스 하려면 Office 365 Cloud App Security 포털에서 **활동 로그** **조사** \> 로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="78622-155">To get to this page, in the Office 365 Cloud App Security portal, go to **Investigate** \> **Activity log**.</span></span> 
  
![O365 CAS 포털에서 조사를 선택 합니다.](media/8c7b87c9-71a6-4952-adb2-185e941ffe9a.png)
  
<span data-ttu-id="78622-157">Office 365 Cloud App Security와 함께 웹 트래픽 로그를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="78622-157">You can use your web traffic logs with Office 365 Cloud App Security, too.</span></span> <span data-ttu-id="78622-158">이러한 로그 파일에 포함 된 자세한 내용은 사용자 작업에 대 한 가시성을 향상 시킵니다.</span><span class="sxs-lookup"><span data-stu-id="78622-158">The more details that are included in those log files, the better visibility you'll have into user activity.</span></span> <span data-ttu-id="78622-159">Barracuda, 파랑 코트, 확인 지점, Cisco, Clavister, Dell SonicWALL, Fortinet, 곱 향나무, McAfee, Microsoft, Palo Alto, Sophos, Squid, websence, Zscaler 등의 로그 파일을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="78622-159">You can use log files from Barracuda, Blue Coat, Check Point, Cisco, Clavister, Dell SonicWALL, Fortinet, Juniper, McAfee, Microsoft, Palo Alto, Sophos, Squid, Websence, Zscaler, and more.</span></span>
  
[<span data-ttu-id="78622-160">Office 365 Cloud App Security에 대 한 웹 트래픽 로그 및 데이터 원본에 대해 자세히 알아보기</span><span class="sxs-lookup"><span data-stu-id="78622-160">Learn about web traffic logs and data sources for Office 365 Cloud App Security</span></span>](web-traffic-logs-and-data-sources-for-ocas.md)
  
## <a name="oauth-apps"></a><span data-ttu-id="78622-161">OAuth 앱</span><span class="sxs-lookup"><span data-stu-id="78622-161">OAuth apps</span></span>

<span data-ttu-id="78622-162">office 365 Cloud App Security를 사용 하 여 조직의 사용자가 office 365의 데이터에 액세스 하는 타사 앱을 사용 하도록 허용 하거나 금지할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="78622-162">With Office 365 Cloud App Security, you can allow or prevent people in your organization to use third-party apps that access data in Office 365.</span></span>
  
![O365 CAS에서는 조사 메뉴에서 OAuth 앱 관리 페이지에 액세스할 수 있습니다.](media/78272cda-986f-4b3b-bbbe-8c236c74f5d3.png)
  
<span data-ttu-id="78622-164">이 페이지에 액세스 하려면 **OAuth 앱** **조사** \> 로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="78622-164">To get to this page, go to **Investigate** \> **OAuth apps**.</span></span> 
  
![O365 CAS 포털에서 조사를 선택 합니다.](media/8c7b87c9-71a6-4952-adb2-185e941ffe9a.png)
  
[<span data-ttu-id="78622-166">Office 365 Cloud App Security를 사용하여 OAuth 앱 관리</span><span class="sxs-lookup"><span data-stu-id="78622-166">Manage OAuth apps using Office 365 Cloud App Security</span></span>](manage-app-permissions-in-ocas.md)
  
## <a name="cloud-discovery-dashboard"></a><span data-ttu-id="78622-167">클라우드 검색 대시보드</span><span class="sxs-lookup"><span data-stu-id="78622-167">Cloud Discovery Dashboard</span></span>

<span data-ttu-id="78622-168">**생산성 앱 검색이**라고도 하는 **클라우드 검색 대시보드**는 조직 내 클라우드 앱 사용에 대 한 정보를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="78622-168">The **Cloud Discovery Dashboard**, also referred to as **Productivity App Discovery**, shows information about cloud app usage within your organization.</span></span> <span data-ttu-id="78622-169">이 대시보드를 사용 하 여 앱, 사용자, 트래픽, 트랜잭션 등에 대 한 정보를 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="78622-169">You can view information about apps, users, traffic, transactions, and more using this dashboard.</span></span> <span data-ttu-id="78622-170">클라우드 검색 대시보드는 다음과 같은 이미지와 비슷합니다.</span><span class="sxs-lookup"><span data-stu-id="78622-170">The Cloud Discovery Dashboard resembles the following image:</span></span> 
  
![Office 365 CAS 포털에서 클라우드 검색 대시보드 검색 \> 을 선택 합니다.](media/61269290-fd82-4d4b-8045-aea1ebc82287.png)
  
<span data-ttu-id="78622-172">이 대시보드에 액세스 하려면 Office 365 cloud App Security 포털에서 \*\*\*\* \> **클라우드 검색 대시보드로**이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="78622-172">To get to this dashboard, in the Office 365 Cloud App Security portal, go to **Discover** \> **Cloud Discovery dashboard**.</span></span> 
  
![Office 365 CAS 포털에서 검색을 선택 합니다.](media/73b5299f-94b5-49dd-a00f-154d188eb2c5.png)
  
[<span data-ttu-id="78622-174">Office 365 Cloud App Security을 사용하여 앱 검색 결과 검토</span><span class="sxs-lookup"><span data-stu-id="78622-174">Review app discovery findings in Office 365 Cloud App Security</span></span>](review-app-discovery-findings-in-ocas.md)
  
## <a name="next-steps"></a><span data-ttu-id="78622-175">다음 단계</span><span class="sxs-lookup"><span data-stu-id="78622-175">Next steps</span></span>

- <span data-ttu-id="78622-176">[Office 365 Cloud App Security 사용 사례 및 사용 가이드](https://aka.ms/O365CASGuide) 받기</span><span class="sxs-lookup"><span data-stu-id="78622-176">Get the [Office 365 Cloud App Security Use Cases and Usage Guide](https://aka.ms/O365CASGuide)</span></span>
    
- [<span data-ttu-id="78622-177">Office 365 Cloud App Security 시작</span><span class="sxs-lookup"><span data-stu-id="78622-177">Get ready for Office 365 Cloud App Security</span></span>](get-ready-for-office-365-cas.md)
    

