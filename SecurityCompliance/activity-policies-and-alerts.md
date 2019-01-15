---
title: Office 365 Cloud App Security 활동 정책 및 알림
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 2/26/2018
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 367f25d3-10a0-4a91-bdae-70ebb7a79c98
description: Office 365 클라우드 응용 프로그램을 설정 하려면 보안 경고를 특정 활동을 발생 하거나 너무 자주 발생 하는 경우를 트리거할 수를 사용 하 여 작업 정책을 정의 합니다. 경고를 트리거하도록 정책을 설정 하 여에 대 한 알림을 받을 수 및 특정 활동을 모니터링 합니다.
ms.openlocfilehash: 6f5039d09dea98de970ab4bd28e95a6cfad73db4
ms.sourcegitcommit: 9034809b6f308bedc3b8ddcca8242586b5c30f94
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/15/2019
ms.locfileid: "28015010"
---
# <a name="activity-policies-and-alerts-in-office-365-cloud-app-security"></a><span data-ttu-id="6504e-104">Office 365 Cloud App Security 활동 정책 및 알림</span><span class="sxs-lookup"><span data-stu-id="6504e-104">Activity policies and alerts in Office 365 Cloud App Security</span></span>

<span data-ttu-id="6504e-105">Office 365 고급 보안 관리 Office 365 클라우드 응용 프로그램 보안 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6504e-105">Office 365 Advanced Security Management is now Office 365 Cloud App Security.</span></span>
  
|<span data-ttu-id="6504e-106">평가 \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="6504e-106">\*\*\*\*Evaluation\*\* \>\*\*</span></span>|<span data-ttu-id="6504e-107">계획 \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="6504e-107">\*\*\*\*Planning\*\* \>\*\*</span></span>|<span data-ttu-id="6504e-108">배포 \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="6504e-108">\*\*\*\*Deployment\*\* \>\*\*</span></span>|<span data-ttu-id="6504e-109">사용률 \* \* \*</span><span class="sxs-lookup"><span data-stu-id="6504e-109">\*\*\*\*Utilization\*\*\*\*</span></span>|
|:-----|:-----|:-----|:-----|
|[<span data-ttu-id="6504e-110">평가 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="6504e-110">Start evaluating</span></span>](office-365-cas-overview.md) <br/> |[<span data-ttu-id="6504e-111">계획을 시작합니다</span><span class="sxs-lookup"><span data-stu-id="6504e-111">Start planning</span></span>](get-ready-for-office-365-cas.md) <br/> |<span data-ttu-id="6504e-112">여기는!</span><span class="sxs-lookup"><span data-stu-id="6504e-112">You are here!</span></span>  <br/> [<span data-ttu-id="6504e-113">다음 단계</span><span class="sxs-lookup"><span data-stu-id="6504e-113">Next step</span></span>](anomaly-detection-policies-in-ocas.md) <br/> |[<span data-ttu-id="6504e-114">활용 하 여 시작</span><span class="sxs-lookup"><span data-stu-id="6504e-114">Start utilizing</span></span>](utilization-activities-for-ocas.md) <br/> |
   
<span data-ttu-id="6504e-p102">Office 365 클라우드 응용 프로그램 보안 고급 클라우드 관리 정책 발생 하거나 너무 자주 발생 하는 특정 작업에 대 한 경고를 트리거합니다. 등 사용자 Office 365에 로그인 하 려 하 고 1 분에 70 번 실패 경우를 가정해 보겠습니다. 다른 사용자 7, 000iops 파일을 다운로드 또는 로그인, 캐나다에서 해당 사용자가 다른 위치에 있어야 할 때 나타나는 경우를 가정해 보겠습니다. 또는 심각한 문제 다른 사용자의 계정 암호가 손상 된 하 고 공격자는 해당 계정을 사용 하 여 조직의 클라우드 앱 및 중요 한 데이터에 액세스 하는 경우를 가정해 보겠습니다.</span><span class="sxs-lookup"><span data-stu-id="6504e-p102">With Office 365 Cloud App Security, advanced cloud management policies trigger alerts for specific activities that happen or happen too frequently. For example, suppose a user tries to sign in to Office 365 and fails 70 times in one minute. Suppose that another user downloads 7,000 files, or appears to be signed in from Canada, when that user is supposed to be in another location. Or worse, suppose that someone's account has been compromised, and an attacker is using that account to access your organization's cloud apps and sensitive data.</span></span>
  
<span data-ttu-id="6504e-p103">[전역 관리자 또는 보안 관리자](permissions-in-the-security-and-compliance-center.md)인 경우 활동 알림을 이러한와 같은 이벤트 될 때 발생 합니다. 셰이프시트에서 변경 된 조사할 수 있을 때까지 사용자 계정을 일시 중단 하는 등의 특정 작업을 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6504e-p103">If you are a [global administrator or security administrator](permissions-in-the-security-and-compliance-center.md), activity alerts notify you when events like these occur. You can then take specific actions, such as suspending a user account until you can investigate what happened.</span></span>
  
> [!NOTE]
> <span data-ttu-id="6504e-p104">Office 365 클라우드 응용 프로그램 보안 정책에서 서로 다릅니다 [Office 365 보안에서 정책 경고 &amp; 준수 센터](alert-policies.md)합니다. 이 문서에서 설명 하는 정책 Office 365 클라우드 응용 프로그램 보안 포털에 정의 되어 있고 수 높이 데 도움이 활동 조직의 클라우드 환경을 관리 합니다.</span><span class="sxs-lookup"><span data-stu-id="6504e-p104">Office 365 Cloud App Security policies are different from [alert policies in the Office 365 Security &amp; Compliance Center](alert-policies.md). The activity policies described in this article are defined in the Office 365 Cloud App Security portal, and can help you better manage your organization's cloud environment.</span></span> 
  
## <a name="before-you-begin"></a><span data-ttu-id="6504e-123">시작하기 전에</span><span class="sxs-lookup"><span data-stu-id="6504e-123">Before you begin</span></span>

<span data-ttu-id="6504e-124">다음 사항을 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="6504e-124">Make sure that:</span></span>
  
- <span data-ttu-id="6504e-125">조직에 [Office 365 클라우드 응용 프로그램 보안](office-365-cas-overview.md)및 서비스를 [설정](turn-on-office-365-cas.md)합니다.</span><span class="sxs-lookup"><span data-stu-id="6504e-125">Your organization has [Office 365 Cloud App Security](office-365-cas-overview.md), and the service is [turned on](turn-on-office-365-cas.md).</span></span>
    
- <span data-ttu-id="6504e-126">Office 365 환경에 대 한 [감사 로깅](turn-audit-log-search-on-or-off.md) 기능이 켜 집니다.</span><span class="sxs-lookup"><span data-stu-id="6504e-126">[Audit logging](turn-audit-log-search-on-or-off.md) is turned on for your Office 365 environment.</span></span> 
    
- <span data-ttu-id="6504e-127">전역 관리자 또는 Office 365에 대 한 보안 관리자는 합니다.</span><span class="sxs-lookup"><span data-stu-id="6504e-127">You are a global administrator or security administrator for Office 365.</span></span>
    
## <a name="create-a-new-activity-policy"></a><span data-ttu-id="6504e-128">새 작업 정책 만들기</span><span class="sxs-lookup"><span data-stu-id="6504e-128">Create a new activity policy</span></span>

1. <span data-ttu-id="6504e-129">전역 관리자 또는 보안 관리자로 이동 [https://protection.office.com](https://protection.office.com) 작업이 나 교육용 계정을 사용 하 여 로그인 하 고 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6504e-129">As a global administrator or security administrator, go to [https://protection.office.com](https://protection.office.com) and sign in using your work or school account.</span></span> 
    
2. <span data-ttu-id="6504e-130">보안에서 &amp; 준수 센터 **알림** 선택 \> **관리 고급 알림**입니다.</span><span class="sxs-lookup"><span data-stu-id="6504e-130">In the Security &amp; Compliance Center, choose **Alerts** \> **Manage advanced alerts**.</span></span>
    
3. <span data-ttu-id="6504e-131">**Office 365 클라우드 응용 프로그램 보안으로 이동**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="6504e-131">Choose **Go to Office 365 Cloud App Security**.</span></span>
    
    <span data-ttu-id="6504e-132">이 Office 365 클라우드 앱 보안 정책 페이지로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="6504e-132">This takes you to the Office 365 Cloud App Security Policies page.</span></span>
    
    ![정책 페이지로 시작 하 여 Office 365 클라우드 응용 프로그램 보안 포털에 이동할 때](media/5cb8833c-4e08-438c-bab3-91b5106f6f3f.png)
  
4. <span data-ttu-id="6504e-134">**정책 만들기**클릭 하 고 **작업 정책**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="6504e-134">Click **Create policy**, and then select **Activity policy**.</span></span>
    
    ![O365 CA에서 정책을 만들면 활동 정책과 이상 탐지 정책을 선택할 수 있습니다.](media/79f34535-ddf9-4a5b-a0a3-8766bf9c174c.png)
  
5. <span data-ttu-id="6504e-p105">**활동 정책 만들기** 페이지에서 **정책 이름** 및 **설명**을 지정 합니다. 정책에 따라 기본 서식 파일의 기반을 **정책 서식 파일** 목록에서 하나를 선택 하거나 서식 파일을 사용 하지 않고 직접 정책을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6504e-p105">On the **Create activity policy** page, specify the **Policy name** and **Description**. To base your policy on a default template, choose one in the **Policy template** list, or create your own policy without using a template.</span></span> 
    
    ![Office 365 클라우드 앱 보안이 포함 된 활동 정책을 만들 수 있습니다.](media/4083a76f-7074-4d6a-8200-6d76d49259d7.png)
  
6. <span data-ttu-id="6504e-p106">**정책 심각도** (낮음, 보통, 또는 높음) 얼마나 심각 하는 것이 경우이 정책에는 경고를 표시할 경우을 측정 하는 선택 합니다. 이렇게 하면 나중에 검토 하는 경우 경고를 필터링 합니다.</span><span class="sxs-lookup"><span data-stu-id="6504e-p106">Choose a **Policy severity** (Low, Medium, or High) that measures how serious it is to you if this policy triggers an alert. This will help you filter alerts when you're reviewing them later.</span></span> 
    
7. <span data-ttu-id="6504e-p107">이 정책에 대 한 **범주** 를 선택 합니다. 이렇게 하면 필터 및 정렬, 트리거된 알림 또는 변경 하 게 검토 하는 경우 그룹 정책의 합니다.</span><span class="sxs-lookup"><span data-stu-id="6504e-p107">Choose a **Category** for this policy. This will help you filter and sort alerts that have been triggered, or to group policies when you're reviewing them to make changes.</span></span> 
    
8. <span data-ttu-id="6504e-143">다른 작업 또는이 정책에 따라 경고를 발생 시키는 메트릭을 설정 하려면 **활동 필터** 를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="6504e-143">Choose **Activity filters** to set up other actions or metrics that will trigger an alert based on this policy.</span></span> 
    
9. <span data-ttu-id="6504e-144">**활동 매개 변수와 일치**에서 지정한 수의 반복 해 서 활동 경고 트리거 하기 전에 필요한 경우 또는 단일 활동을 필터에 일치 하는 경우 정책 위반 트리거되는지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6504e-144">Under **Activity match parameters**, specify whether a policy violation will be triggered when a single activity matches the filters, or if a specified number of repeated activities is required before the alert triggers.</span></span>
    
    <span data-ttu-id="6504e-145">**반복 작업**을 선택 하는 경우 활동을 시간 프레임 수를 지정 및 모든 app와 같은 사용자 또는 특정 응용 프로그램 내에서 사용자에 대 한 위반 count가 있는지 여부.</span><span class="sxs-lookup"><span data-stu-id="6504e-145">If you select **Repeated activity**, specify the number of activities, the time frame, and whether a violation will count for a user within a specific app or for the same user with any app.</span></span>
    
10. <span data-ttu-id="6504e-146">필요에 따라 **만들기 경고** 전자 메일, 텍스트 메시지 또는 둘 모두) (통해이 정책에서 알림을 받도록 추가 알림을 만들 수를 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6504e-146">Optionally, you can select **Create alert** to create additional alerts to receive notifications from this policy (via email, text message, or both).</span></span> 
    
    > [!IMPORTANT]
    > <span data-ttu-id="6504e-147">전자 메일 공급자 no-reply@cloudappsecurity.com에서 보낸 전자 메일을 차단 하지 있는지 확인 하십시오.</span><span class="sxs-lookup"><span data-stu-id="6504e-147">Make sure that your email provider doesn't block emails sent from no-reply@cloudappsecurity.com.</span></span> 
  
11. <span data-ttu-id="6504e-148">사용자를 일시 중단 하거나 사용자가 Office 365 응용 프로그램을 다시 로그인 해야 경고가 표시 될 때 취해야 하는 **작업** 을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="6504e-148">Choose the **Actions** that should be taken when an alert is triggered to suspend the user or require the user to sign in again to Office 365 apps.</span></span> 
    
12. <span data-ttu-id="6504e-149">사용자 정책 만들기를 종료 하려면 **만들기** 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="6504e-149">Choose **Create** to finish creating your policy.</span></span> 
    
## <a name="next-steps"></a><span data-ttu-id="6504e-150">다음 단계</span><span class="sxs-lookup"><span data-stu-id="6504e-150">Next steps</span></span>

- [<span data-ttu-id="6504e-151">예외 탐지 정책</span><span class="sxs-lookup"><span data-stu-id="6504e-151">Anomaly detection policies</span></span>](anomaly-detection-policies-in-ocas.md)
    
- [<span data-ttu-id="6504e-152">SIEM 서버 통합</span><span class="sxs-lookup"><span data-stu-id="6504e-152">Integrate your SIEM server</span></span>](integrate-your-siem-server-with-office-365-cas.md)
    
- [<span data-ttu-id="6504e-153">검토 및 알림 작업을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="6504e-153">Review and take action on alerts</span></span>](review-office-365-cas-alerts.md)
    
- [<span data-ttu-id="6504e-154">관리를 단순화 하 여 IP 주소를 그룹화</span><span class="sxs-lookup"><span data-stu-id="6504e-154">Group your IP addresses to simplify management</span></span>](group-your-ip-addresses-in-ocas.md)
    

