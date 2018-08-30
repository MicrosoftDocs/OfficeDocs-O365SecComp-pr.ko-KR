---
title: 검토 하 고 필요한 작업을 Office 365 Cloud App Security 검토 및 알림 작업 수행
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
ms.assetid: 97e9c3d9-df89-458e-924b-369becee5532
description: Office 365 클라우드 응용 프로그램 보안에서 경고 페이지를 사용 하 여를 잠재적 문제를 보고 하 여 작업도 하지 않습니다. 해제 하 고 또는 경고를 확인 하 고, 필요한 경우에 사용자 계정이 일시 중단 수 있습니다.
ms.openlocfilehash: 62431adc73354e573978781f120a11746aef08d9
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22532886"
---
# <a name="review-and-take-action-on-alerts-in-office-365-cloud-app-security"></a><span data-ttu-id="251b9-104">검토 하 고 필요한 작업을 Office 365 Cloud App Security 검토 및 알림 작업 수행</span><span class="sxs-lookup"><span data-stu-id="251b9-104">Review and take action on alerts in Office 365 Cloud App Security</span></span>
  
|<span data-ttu-id="251b9-105">평가 * *\>**</span><span class="sxs-lookup"><span data-stu-id="251b9-105">****Evaluation** \>**</span></span>|<span data-ttu-id="251b9-106">계획 * *\>**</span><span class="sxs-lookup"><span data-stu-id="251b9-106">****Planning** \>**</span></span>|<span data-ttu-id="251b9-107">배포 * *\>**</span><span class="sxs-lookup"><span data-stu-id="251b9-107">****Deployment** \>**</span></span>|<span data-ttu-id="251b9-108">사용률 \* \* \*</span><span class="sxs-lookup"><span data-stu-id="251b9-108">****Utilization****</span></span>|
|:-----|:-----|:-----|:-----|
|[<span data-ttu-id="251b9-109">평가 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="251b9-109">Start evaluating</span></span>](office-365-cas-overview.md) <br/> |[<span data-ttu-id="251b9-110">계획을 시작합니다</span><span class="sxs-lookup"><span data-stu-id="251b9-110">Start planning</span></span>](get-ready-for-office-365-cas.md) <br/> |[<span data-ttu-id="251b9-111">배포를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="251b9-111">Start deploying</span></span>](turn-on-office-365-cas.md) <br/> |<span data-ttu-id="251b9-112">여기는!</span><span class="sxs-lookup"><span data-stu-id="251b9-112">You are here!</span></span>  <br/> [<span data-ttu-id="251b9-113">다음 단계</span><span class="sxs-lookup"><span data-stu-id="251b9-113">Next steps</span></span>](#next-steps) <br/> |
   
<span data-ttu-id="251b9-114">잠재적인 문제를 확인 하 고 필요한 경우 작업을 수행 하려면 Office 365 클라우드 앱 보안에서 경고 페이지를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="251b9-114">You can use the Alerts page in Office 365 Cloud App Security to view potential issues and, if needed, take action.</span></span>
  
> [!NOTE]
> <span data-ttu-id="251b9-p102">이 문서에서 작업을 수행 하는 전역 관리자 또는 보안 관리자 여야 합니다. 참조 [Office 365 보안에 대 한 사용 권한을 &amp; 준수 센터](permissions-in-the-security-and-compliance-center.md)합니다.</span><span class="sxs-lookup"><span data-stu-id="251b9-p102">You must be a global administrator or security administrator to perform the tasks in this article. See [Permissions in the Office 365 Security &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md).</span></span> 
  
## <a name="how-to-get-to-the-alerts-page"></a><span data-ttu-id="251b9-117">알림 페이지로 이동 하는 방법</span><span class="sxs-lookup"><span data-stu-id="251b9-117">How to get to the Alerts page</span></span>

1. <span data-ttu-id="251b9-118">전역 관리자 또는 보안 관리자로 이동 [https://protection.office.com](https://protection.office.com) 작업이 나 교육용 계정을 사용 하 여 로그인 하 고 있습니다.</span><span class="sxs-lookup"><span data-stu-id="251b9-118">As a global administrator or security administrator, go to [https://protection.office.com](https://protection.office.com) and sign in using your work or school account.</span></span> 
    
2. <span data-ttu-id="251b9-119">보안에서 &amp; 준수 센터 **알림** 선택 \> **관리 고급 알림**입니다.</span><span class="sxs-lookup"><span data-stu-id="251b9-119">In the Security &amp; Compliance Center, choose **Alerts** \> **Manage advanced alerts**.</span></span>
    
3. <span data-ttu-id="251b9-120">**Office 365 클라우드 응용 프로그램 보안으로 이동**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="251b9-120">Choose **Go to Office 365 Cloud App Security**.</span></span>
    
    ![보안에서 &amp; 준수 센터 Office 365 클라우드 앱 보안으로 이동 하려면 고급 알림 관리를 선택 합니다.](media/958632d4-03e3-4ade-8e22-d5509db6fca7.png)
  
4. <span data-ttu-id="251b9-122">화면 위쪽 탐색 모음에서 **경고**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="251b9-122">In the navigation bar across the top of the screen, choose **Alerts**.</span></span>
    
    ![경고 페이지에서 경고를 트리거한 된 및 수행 하는 모든 작업을 볼 수 있습니다.](media/3b53d4c9-4b13-435d-8547-8c0f9ae6b914.png)
  
## <a name="review-and-handle-alerts"></a><span data-ttu-id="251b9-124">검토 및 핸들 알림</span><span class="sxs-lookup"><span data-stu-id="251b9-124">Review and handle alerts</span></span>

<span data-ttu-id="251b9-p103">알림 추가로 조사를 수행 해야할 수 있는 Office 365 클라우드 환경에서 작업을 파악 하는데 도움이 됩니다. 새 정책 만들기 또는 표시 경고에 따라 기존 정책을 편집 하려면 결정할 수 있습니다. 예, 이상한 위치에서 로그온 하는 관리자의 이름을 표시 하는 경우에 관리자가 특정 위치에서 Office 365에 로그인 하지 못하게 하는 정책을 설정 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="251b9-p103">Alerts help you identify activities in your Office 365 cloud environment that you might want to investigate further. You might also decide to create new policies or edit existing policies based on the alerts you see. For example, if you see an administrator logging on from a strange location, you may decide to set up a policy that prevents administrators from signing in to Office 365 from certain locations.</span></span>
  
> [!TIP]
> <span data-ttu-id="251b9-128">먼저 가장 중요 한 항목을 관리할 수 있도록 **범주별** 로 또는 **심각도** 경고를 필터링 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="251b9-128">You can filter the alerts by **Category** or by **Severity** so you can manage the most important ones first.</span></span> 
  
<span data-ttu-id="251b9-p104">각 경고에 대해 수행할 동작을 결정할 수 있도록 어떤 인해으로 찾습니다. 경고에 대 한 자세한 내용을 보려면 및 경고를 해결 하거나 일시 중단 하는 사용자 계정 등의 작업을 수행할 세부 정보 페이지를 열려면 경고를 선택 합니다. 세부 정보 페이지에서 활동 로그, 계정 및 경고와 관련 된 사용자를 검토 하 고 다음과 같은 작업을 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="251b9-p104">For each alert, look into what caused it so you can decide what action to take. To see more details about an alert and to take action, such as resolving the alert or suspending a users account, choose the alert to open a details page. On the details page, you can review the activity log, accounts, and users that are related to the alert, and take actions such as the following:</span></span>
  
- <span data-ttu-id="251b9-p105">**해제** 경고 가양성 했으므로,이 해제 합니다. 필요에 따라 해제할 이유를 설명 하는 메모를 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="251b9-p105">**Dismiss** If the alert was a false positive, dismiss it. You can optionally add a comment explaining why you dismissed it.</span></span> 
    
- <span data-ttu-id="251b9-p106">**경고를 해결 합니다.** 알고 있는 활동에 대 한 위협 요소 되지 않습니다 하 여 경고가 발생 하는 경우,이 해결 합니다. 필요에 따라 해결 한 이유를 설명 하는 메모를 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="251b9-p106">**Resolve alert** If the alert was triggered by an activity that you know isn't a threat, resolve it. You can optionally add a comment explaining why you resolved it.</span></span> 
    
- <span data-ttu-id="251b9-136">**일시 중단** 허가 되지 않은 기호 기능 등 해당 사용자를 알고 있는 경우 다른 국가에서 로그인 사용자 계정에는 로컬 사무실에서 물리적으로, 의심 되 [는 계정을 일시 중단](suspend-or-restore-an-account-in-ocas.md) 상황을 조사 하는 동안 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="251b9-136">**Suspend** If you suspect unauthorized sign ins on an account, for example, someone signing in from another country when you know that person is physically at a local office, you can [suspend the account](suspend-or-restore-an-account-in-ocas.md) while you investigate what's going on.</span></span> 
    
## <a name="next-steps"></a><span data-ttu-id="251b9-137">다음 단계</span><span class="sxs-lookup"><span data-stu-id="251b9-137">Next steps</span></span>

- [<span data-ttu-id="251b9-138">활동 조사</span><span class="sxs-lookup"><span data-stu-id="251b9-138">Investigate an activity</span></span>](investigate-an-activity-in-office-365-cas.md)
    
- [<span data-ttu-id="251b9-139">일시 중단 또는 사용자 계정 복원</span><span class="sxs-lookup"><span data-stu-id="251b9-139">Suspend or restore a user account</span></span>](suspend-or-restore-an-account-in-ocas.md)
    
- <span data-ttu-id="251b9-140">지원 되는 [웹 트래픽 로그 및 데이터 원본](web-traffic-logs-and-data-sources-for-ocas.md) 목록 보기</span><span class="sxs-lookup"><span data-stu-id="251b9-140">View a list of supported [Web traffic logs and data sources](web-traffic-logs-and-data-sources-for-ocas.md)</span></span>
    
- <span data-ttu-id="251b9-141">[Office 365 클라우드 응용 프로그램 보안에 대 한 사용률 활동](utilization-activities-for-ocas.md) 을 검토 합니다.</span><span class="sxs-lookup"><span data-stu-id="251b9-141">Review your [utilization activities for Office 365 Cloud App Security](utilization-activities-for-ocas.md)</span></span>
    

