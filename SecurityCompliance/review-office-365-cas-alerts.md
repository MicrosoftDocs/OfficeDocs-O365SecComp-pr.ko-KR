---
title: 검토 하 고 필요한 작업을 Office 365 Cloud App Security 검토 및 알림 작업 수행
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 97e9c3d9-df89-458e-924b-369becee5532
description: Office 365 Cloud App Security의 알림 페이지를 사용 하 여 잠재적인 문제를 확인 하 고 조치를 취할 수 있습니다. 알림을 해제 하거나 확인 하 고 필요한 경우 사용자 계정을 일시 중단할 수 있습니다.
ms.openlocfilehash: ddef10293fca7b722a13babdca5c05bbe2398cb3
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32261484"
---
# <a name="review-and-take-action-on-alerts-in-office-365-cloud-app-security"></a><span data-ttu-id="be231-104">검토 하 고 필요한 작업을 Office 365 Cloud App Security 검토 및 알림 작업 수행</span><span class="sxs-lookup"><span data-stu-id="be231-104">Review and take action on alerts in Office 365 Cloud App Security</span></span>
  
|<span data-ttu-id="be231-105">계산 \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="be231-105">\*\*\*\*Evaluation\*\* \>\*\*</span></span>|<span data-ttu-id="be231-106">계획 \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="be231-106">\*\*\*\*Planning\*\* \>\*\*</span></span>|<span data-ttu-id="be231-107">배포 \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="be231-107">\*\*\*\*Deployment\*\* \>\*\*</span></span>|<span data-ttu-id="be231-108">사용률 \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="be231-108">\*\*\*\*Utilization\*\*\*\*</span></span>|
|:-----|:-----|:-----|:-----|
|[<span data-ttu-id="be231-109">평가 시작</span><span class="sxs-lookup"><span data-stu-id="be231-109">Start evaluating</span></span>](office-365-cas-overview.md) <br/> |[<span data-ttu-id="be231-110">계획 시작</span><span class="sxs-lookup"><span data-stu-id="be231-110">Start planning</span></span>](get-ready-for-office-365-cas.md) <br/> |[<span data-ttu-id="be231-111">배포 시작</span><span class="sxs-lookup"><span data-stu-id="be231-111">Start deploying</span></span>](turn-on-office-365-cas.md) <br/> |<span data-ttu-id="be231-112">사용자가 여기 있어!</span><span class="sxs-lookup"><span data-stu-id="be231-112">You are here!</span></span>  <br/> [<span data-ttu-id="be231-113">다음 단계</span><span class="sxs-lookup"><span data-stu-id="be231-113">Next steps</span></span>](#next-steps) <br/> |
   
<span data-ttu-id="be231-114">Office 365 Cloud App Security의 알림 페이지를 사용 하 여 잠재적인 문제를 확인 하 고 필요한 경우 조치를 취할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="be231-114">You can use the Alerts page in Office 365 Cloud App Security to view potential issues and, if needed, take action.</span></span>
  
> [!NOTE]
> <span data-ttu-id="be231-115">이 문서의 작업을 수행 하려면 전역 관리자 또는 보안 관리자 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="be231-115">You must be a global administrator or security administrator to perform the tasks in this article.</span></span> <span data-ttu-id="be231-116">[Office 365 보안 &amp; 및 준수 센터의 사용 권한을](permissions-in-the-security-and-compliance-center.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="be231-116">See [Permissions in the Office 365 Security &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md).</span></span> 
  
## <a name="how-to-get-to-the-alerts-page"></a><span data-ttu-id="be231-117">알림 페이지에 액세스 하는 방법</span><span class="sxs-lookup"><span data-stu-id="be231-117">How to get to the Alerts page</span></span>

1. <span data-ttu-id="be231-118">Cloud App Security portal ([https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com))로 이동 하 여 로그인 합니다.</span><span class="sxs-lookup"><span data-stu-id="be231-118">Go to the Cloud App Security portal ([https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com)) and sign in.</span></span>
  
2. <span data-ttu-id="be231-119">화면 위쪽의 탐색 모음에서 **경고**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="be231-119">In the navigation bar across the top of the screen, choose **Alerts**.</span></span><br/><span data-ttu-id="be231-120">![알림 페이지에서 트리거된 알림과 수행한 모든 작업을 확인할 수 있습니다.](media/3b53d4c9-4b13-435d-8547-8c0f9ae6b914.png)</span><span class="sxs-lookup"><span data-stu-id="be231-120">![On the Alerts page, you can see alerts that were triggered and any actions taken.](media/3b53d4c9-4b13-435d-8547-8c0f9ae6b914.png)</span></span>
 
> [!NOTE]
> <span data-ttu-id="be231-121">Cloud App security alerts는 보안 & 준수 센터 ( **알림** > **보기 경고**로 이동)에도 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="be231-121">Cloud App Security alerts are also visible in the Security & Compliance Center (go to **Alerts** > **View alerts**.</span></span> <span data-ttu-id="be231-122">그러나 현재 클라우드 응용 프로그램 보안 포털 및 security & 준수 센터에서 이러한 경고를 해결 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="be231-122">Currently, however, you must resolve these alerts in both the Cloud App Security portal and the Security & Compliance Center.</span></span> <span data-ttu-id="be231-123">자세한 내용은 [Cloud App Security alerts 보기](alert-policies.md#viewing-cloud-app-security-alerts)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="be231-123">To learn more, see [Viewing Cloud App Security alerts](alert-policies.md#viewing-cloud-app-security-alerts).)</span></span> 
 
## <a name="review-and-handle-alerts"></a><span data-ttu-id="be231-124">알림 검토 및 처리</span><span class="sxs-lookup"><span data-stu-id="be231-124">Review and handle alerts</span></span>

<span data-ttu-id="be231-125">알림은 Office 365 클라우드 환경에서 더 자세히 조사 하려는 활동을 식별 하는 데 도움이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="be231-125">Alerts help you identify activities in your Office 365 cloud environment that you might want to investigate further.</span></span> <span data-ttu-id="be231-126">표시 되는 경고에 따라 새 정책 만들기 또는 기존 정책 편집을 결정할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="be231-126">You might also decide to create new policies or edit existing policies based on the alerts you see.</span></span> <span data-ttu-id="be231-127">예를 들어, 관리자가 이상한 위치에서 로그온을 보게 되는 경우 관리자가 특정 위치에서 Office 365에 로그인 하지 못하도록 하는 정책을 설정 하는 것을 결정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="be231-127">For example, if you see an administrator logging on from a strange location, you may decide to set up a policy that prevents administrators from signing in to Office 365 from certain locations.</span></span>
  
> [!TIP]
> <span data-ttu-id="be231-128">가장 중요 한 항목을 먼저 관리할 수 있도록 **범주** 또는 **심각도** 별로 알림을 필터링 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="be231-128">You can filter the alerts by **Category** or by **Severity** so you can manage the most important ones first.</span></span> 
  
<span data-ttu-id="be231-129">각 경고에 대해 발생 한 결과를 확인 하 여 수행할 작업을 결정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="be231-129">For each alert, look into what caused it so you can decide what action to take.</span></span> <span data-ttu-id="be231-130">경고에 대 한 세부 정보를 확인 하 고 경고를 해결 하거나 사용자 계정을 일시 중단 하는 등의 조치를 취해야 하는 경우에는 경고를 선택 하 여 세부 정보 페이지를 엽니다.</span><span class="sxs-lookup"><span data-stu-id="be231-130">To see more details about an alert and to take action, such as resolving the alert or suspending a users account, choose the alert to open a details page.</span></span> <span data-ttu-id="be231-131">세부 정보 페이지에서 경고와 관련 된 활동 로그, 계정 및 사용자를 검토 하 고 다음과 같은 작업을 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="be231-131">On the details page, you can review the activity log, accounts, and users that are related to the alert, and take actions such as the following:</span></span>
  
- <span data-ttu-id="be231-132">**해제** 경고가 가양성 이면 해제 합니다.</span><span class="sxs-lookup"><span data-stu-id="be231-132">**Dismiss** If the alert was a false positive, dismiss it.</span></span> <span data-ttu-id="be231-133">필요한 경우이를 해제 한 이유를 설명 하는 주석을 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="be231-133">You can optionally add a comment explaining why you dismissed it.</span></span> 
    
- <span data-ttu-id="be231-134">**경고 해결** 위협이 아닌 것으로 확인 된 활동에 의해 경고가 트리거된 경우 문제를 해결 합니다.</span><span class="sxs-lookup"><span data-stu-id="be231-134">**Resolve alert** If the alert was triggered by an activity that you know isn't a threat, resolve it.</span></span> <span data-ttu-id="be231-135">원하는 경우 해결 된 이유를 설명 하는 설명을 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="be231-135">You can optionally add a comment explaining why you resolved it.</span></span> 
    
- <span data-ttu-id="be231-136">**일시 중단** 예를 들어 사용자가 실제로 로컬 사무실에 있음을 알게 될 때 다른 국가에서 로그인 하는 사용자와 같은 계정에 대 한 권한 없는 로그인으로 의심 되는 경우에는 어떤 일이 진행 되는지 조사 하는 동안 [계정을 일시 중단할](suspend-or-restore-an-account-in-ocas.md) 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="be231-136">**Suspend** If you suspect unauthorized sign ins on an account, for example, someone signing in from another country when you know that person is physically at a local office, you can [suspend the account](suspend-or-restore-an-account-in-ocas.md) while you investigate what's going on.</span></span> 
    
## <a name="next-steps"></a><span data-ttu-id="be231-137">다음 단계</span><span class="sxs-lookup"><span data-stu-id="be231-137">Next steps</span></span>

- [<span data-ttu-id="be231-138">활동 조사</span><span class="sxs-lookup"><span data-stu-id="be231-138">Investigate an activity</span></span>](investigate-an-activity-in-office-365-cas.md)
    
- [<span data-ttu-id="be231-139">사용자 계정 일시 중단 또는 복원</span><span class="sxs-lookup"><span data-stu-id="be231-139">Suspend or restore a user account</span></span>](suspend-or-restore-an-account-in-ocas.md)
    
- <span data-ttu-id="be231-140">지원 되는 [웹 트래픽 로그 및 데이터 원본](web-traffic-logs-and-data-sources-for-ocas.md) 목록 보기</span><span class="sxs-lookup"><span data-stu-id="be231-140">View a list of supported [Web traffic logs and data sources](web-traffic-logs-and-data-sources-for-ocas.md)</span></span>
    
- <span data-ttu-id="be231-141">[Office 365 Cloud App Security에 대 한 사용률 작업](utilization-activities-for-ocas.md) 검토</span><span class="sxs-lookup"><span data-stu-id="be231-141">Review your [utilization activities for Office 365 Cloud App Security](utilization-activities-for-ocas.md)</span></span>
    

