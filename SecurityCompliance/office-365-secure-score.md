---
title: Office 365 보안 점수
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 02/13/2019
ms.audience: Admin
ms.topic: overview
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: c9e7160f-2c34-4bd0-a548-5ddcc862eaef
description: Office 365에서 조직이 어떻게 보호 되는지 궁금 하십니까? 보안 점수가 여기에 해당 합니다. 보안 점수는 Office 365의 일반 활동 및 보안 설정에 따라 조직의 보안을 분석 하 고 점수를 할당 합니다.
ms.openlocfilehash: dd0dc87910853eba9f2ec3ec6752e857462b46e5
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32262478"
---
# <a name="office-365-secure-score"></a><span data-ttu-id="597cf-105">Office 365 보안 점수</span><span class="sxs-lookup"><span data-stu-id="597cf-105">Office 365 Secure Score</span></span>

<span data-ttu-id="597cf-106">**요약** Office 365에서 조직이 어떻게 보호 되는지 궁금 하십니까?</span><span class="sxs-lookup"><span data-stu-id="597cf-106">**Summary** Ever wonder how secure your organization really is in Office 365?</span></span> <span data-ttu-id="597cf-107">보안 점수가 여기에 해당 합니다.</span><span class="sxs-lookup"><span data-stu-id="597cf-107">Secure Score is here to help.</span></span> <span data-ttu-id="597cf-108">보안 점수는 Office 365의 일반 활동 및 보안 설정에 따라 조직의 보안을 분석 하 고 점수를 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="597cf-108">Secure Score analyzes your organization's security  based on your regular activities and security settings in Office 365, and assigns a score.</span></span> <span data-ttu-id="597cf-109">이 문서를 읽으면 보안 점수에 대 한 개요를 확인 하 고 사용 하는 방법을 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="597cf-109">Read this article to get an overview of Secure Score and how you can use it.</span></span>
  
## <a name="how-to-get-to-secure-score"></a><span data-ttu-id="597cf-110">보안 점수에 액세스 하는 방법</span><span class="sxs-lookup"><span data-stu-id="597cf-110">How to get to Secure Score</span></span>

<span data-ttu-id="597cf-111">조직에 [Office 365 Enterprise](https://docs.microsoft.com/office365/enterprise/), [Microsoft 365 business](https://docs.microsoft.com/microsoft-365/business/)또는 Office 365 business Premium이 포함 된 구독이 있고 [필요한 사용 권한이](#required-permissions)있는 경우에는 방문 하 여 조직의 보안 점수를 볼 수 있습니다. [https://securescore.office.com](https://securescore.office.com).</span><span class="sxs-lookup"><span data-stu-id="597cf-111">If your organization has a subscription that includes [Office 365 Enterprise](https://docs.microsoft.com/office365/enterprise/), [Microsoft 365 Business](https://docs.microsoft.com/microsoft-365/business/), or Office 365 Business Premium, and you have the [necessary permissions](#required-permissions), you can view your organization's secure score by visiting [https://securescore.office.com](https://securescore.office.com).</span></span> 

<span data-ttu-id="597cf-112">또는 보안 & 준수 센터 ([https://protection.office.com](https://protection.office.com))를 방문 하 여 현재 점수를 제공 하는 보안 점수 위젯을 찾을 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="597cf-112">Alternatively, you can visit the Security & Compliance Center ([https://protection.office.com](https://protection.office.com)), where you'll find a Secure Score widget that provides you with your current score.</span></span>

![보안 점수 위젯](media/SecureScoreWidget-o365.png)

<span data-ttu-id="597cf-114">위젯에는 보안 점수 대시보드에 대 한 링크가 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="597cf-114">The widget includes a link to your Secure Score dashboard.</span></span>

![보안 점수 대시보드](media/SecureScore-WelcomeScreen.png)
  
## <a name="how-it-works"></a><span data-ttu-id="597cf-116">작업 방법</span><span class="sxs-lookup"><span data-stu-id="597cf-116">How it works</span></span>

<span data-ttu-id="597cf-117">보안 점수 사용 중인 Office 365 서비스 (예: OneDrive, SharePoint, Exchange)를 결정 하 고 설정 및 작업을 Microsoft에서 설정한 기준에 맞게 비교 합니다.</span><span class="sxs-lookup"><span data-stu-id="597cf-117">Secure Score determines what Office 365 services you're using (such as OneDrive, SharePoint, and Exchange) then compares your settings and activities to a baseline established by Microsoft.</span></span> <span data-ttu-id="597cf-118">조직이 보안 모범 사례와 일치 하는 방식에 따라 점수가 부여 됩니다.</span><span class="sxs-lookup"><span data-stu-id="597cf-118">You'll get a score based on how well aligned your organization is with security best practices.</span></span> <span data-ttu-id="597cf-119">또한 조직의 점수를 높이기 위해 수행할 수 있는 단계에 대 한 권장 사항도 제공 됩니다.</span><span class="sxs-lookup"><span data-stu-id="597cf-119">You'll also get recommendations on steps you can take to improve your organization's score.</span></span> 
  
![Office 365 보안 점수 도구에 있는 작업 큐](media/SecureScore-ActionsToTake.png)
  
<span data-ttu-id="597cf-121">보안 점수는 구매한 서비스에 따라 점수를 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="597cf-121">Secure Score calculates your score based on the services you purchased.</span></span> <span data-ttu-id="597cf-122">예를 들어 Exchange online 요금제만 구매한 경우에는 SharePoint online 보안 기능에 대 한 점수가 매겨지지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="597cf-122">For example, if you only purchased an Exchange Online plan, you won't be scored for SharePoint Online security features.</span></span> <span data-ttu-id="597cf-123">점수의 분모는 구매한 제품에 적용 되는 컨트롤에 대 한 모든 초기 계획의 합계입니다.</span><span class="sxs-lookup"><span data-stu-id="597cf-123">The denominator of the score is the sum of all the baselines for the controls that apply to the products you purchased.</span></span> <span data-ttu-id="597cf-124">분자는 해당 컨트롤을 완료 하거나 부분적으로 완료 한 모든 컨트롤의 합계입니다.</span><span class="sxs-lookup"><span data-stu-id="597cf-124">The numerator is the sum of all the controls for which you completed, or partially completed, the actions to fulfill that control.</span></span>

<span data-ttu-id="597cf-125">작업을 확장 하 여 수행 해야 하는 단계, 사용자 로부터 보호 하는 데 도움이 되는 위협 및 권장 사항에 따라 점수가 증가 하는 점수를 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="597cf-125">Expand an action to learn about what steps to take, the threats it'll help protect you from, and how many points your score will increase once you follow the recommendation.</span></span>
  
![Office 365 보안 점수 도구에 확장 된 작업](media/SecureScore-DetailedActionToTake.png)
  
<span data-ttu-id="597cf-127">조직의 보안에 대 한 작업의 영향을 확인 하려면 **점수 분석기** 탭을 선택 하 고 기록을 검토 합니다.</span><span class="sxs-lookup"><span data-stu-id="597cf-127">To see the impact of your actions on your organization's security, select the **Score Analyzer** tab and review your history.</span></span> 
  
![Office 365 보안 점수 도구의 점수 분석기 탭](media/SecureScore-ScoreAnalyzer-7days.png)
  
<span data-ttu-id="597cf-129">차트 아래에 범주별 점수 및 작업 목록이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="597cf-129">Below the chart, you'll see a list of scores and actions by category.</span></span> 
  
![선택한 데이터 요소를 표시 하는 점수 분석기 탭의 그래프](media/SecureScore-Analyzer-breakdownbelowchart.png)
 
<span data-ttu-id="597cf-131">**[점수가 없음]** 으로 레이블이 지정 된 작업은 조직에 대해 수행할 수 있는 것으로, 보안 점수에 연결 되어 있지 않으므로 점수가 매겨지지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="597cf-131">Actions that are labeled as **[Not Scored]** are ones you can perform for your organization, but because they are not connected to Secure Score, they are not scored.</span></span>  

<span data-ttu-id="597cf-132">**점수 분석기** 페이지에서 특정 날짜에 대 한 데이터 요소를 클릭 한 다음 아래로 스크롤하여 해당 요일의 완료 및 완료 되지 않은 작업을 확인 하 여 변경 된 내용을 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="597cf-132">On the **Score Analyzer** page, click a data point for a specific day, then scroll down to see the completed and incomplete actions for that day to find out what changed.</span></span> <span data-ttu-id="597cf-133">점수는 하루에 한 번 계산 됩니다 (1:00 AM PST 기준).</span><span class="sxs-lookup"><span data-stu-id="597cf-133">The score is calculated once per day (around 1:00 AM PST).</span></span> <span data-ttu-id="597cf-134">측정 된 작업을 변경 하면 점수가 다음 날에 자동으로 업데이트 됩니다.</span><span class="sxs-lookup"><span data-stu-id="597cf-134">If you make a change to a measured action, the score will automatically update the next day.</span></span> <span data-ttu-id="597cf-135">변경 내용이 점수에 반영 되는 데 최대 48 시간이 걸릴 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="597cf-135">It takes up to 48 hours for a change to be reflected in your score.</span></span>

<span data-ttu-id="597cf-136">보안 점수가 위반 되는 정도를 절대적으로 측정 하는 것은 아닙니다.</span><span class="sxs-lookup"><span data-stu-id="597cf-136">Secure Score does not express an absolute measure of how likely you are to get breached.</span></span> <span data-ttu-id="597cf-137">이는 침해 위험을 오프셋할 수 있는 기능을 채택한 범위를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="597cf-137">It expresses the extent to which you have adopted features that can offset the risk of being breached.</span></span> <span data-ttu-id="597cf-138">어떤 서비스도 위반 되지 않도록 보장할 수 있으며 보안 점수는 어떤 식으로든 보증으로 해석 되어서는 안 됩니다.</span><span class="sxs-lookup"><span data-stu-id="597cf-138">No service can guarantee that you will not be breached, and the Secure Score should not be interpreted as a guarantee in any way.</span></span>
 
## <a name="how-secure-score-helps"></a><span data-ttu-id="597cf-139">보안 점수가 어떻게 도움이 되는가</span><span class="sxs-lookup"><span data-stu-id="597cf-139">How Secure Score helps</span></span>

<span data-ttu-id="597cf-140">보안 점수를 사용 하 여 Office 365의 기본 제공 보안 기능을 사용 하 여 조직의 보안을 향상 시킬 수 있습니다 (이미 구매한 반면, 사용자가 알고 있지 않을 수도 있음).</span><span class="sxs-lookup"><span data-stu-id="597cf-140">With Secure Score, you can help improve your organization's security posture by using the built-in security features in Office 365 (many of which you already purchased but might not be aware of).</span></span> <span data-ttu-id="597cf-141">이러한 기능에 대해 자세히 알고 있으면 위협 으로부터 조직을 보호 하기 위해 적절 한 단계를 수행 하는 데 도움이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="597cf-141">Learning more about these features can help give you peace of mind that you're taking the right steps to protect your organization from threats.</span></span>
  
<span data-ttu-id="597cf-142">하지만이 문서에 대 한 단어만 사용 하면 됩니다.</span><span class="sxs-lookup"><span data-stu-id="597cf-142">But don't just take our word for it.</span></span> <span data-ttu-id="597cf-143">보안 점수를 사용 하는 고객은 해당 점수를 사용 하지 않는 고객 보다 5 배의 시간이 더 증가 한 것으로 나타났습니다.</span><span class="sxs-lookup"><span data-stu-id="597cf-143">Customers who are using Secure Score have seen their score increase five times more than customers who aren't using it.</span></span> <span data-ttu-id="597cf-144">(점수가 증가 하는 것은 조직에서 사용 되는 보안 기능에 해당 합니다.)</span><span class="sxs-lookup"><span data-stu-id="597cf-144">(The increase in their score corresponds with the security features being used in their organizations.)</span></span>
  
> [!NOTE]
> <span data-ttu-id="597cf-145">보안 점수가 위반 되는 정도를 절대적으로 측정 하는 것은 아닙니다.</span><span class="sxs-lookup"><span data-stu-id="597cf-145">Secure Score does not express an absolute measure of how likely you are to get breached.</span></span> <span data-ttu-id="597cf-146">이는 위반 위험을 오프셋할 수 있는 컨트롤을 채택한 범위를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="597cf-146">It expresses the extent to which you have adopted controls which can offset the risk of being breached.</span></span> <span data-ttu-id="597cf-147">어떤 서비스도 위반 되지 않도록 보장할 수 있으며 보안 점수는 어떤 식으로든 보증으로 해석 되어서는 안 됩니다.</span><span class="sxs-lookup"><span data-stu-id="597cf-147">No service can guarantee that you will not be breached, and Secure Score should not be interpreted as a guarantee in any way.</span></span> 
  
## <a name="required-permissions"></a><span data-ttu-id="597cf-148">필요한 사용 권한</span><span class="sxs-lookup"><span data-stu-id="597cf-148">Required permissions</span></span>

<span data-ttu-id="597cf-149">보안 점수 대시보드를 보고 사용 하려면 [Azure Active Directory](https://docs.microsoft.com/azure/active-directory/users-groups-roles/directory-assign-admin-roles#available-roles)에서 다음 역할 중 하나를 할당 받아야 합니다.</span><span class="sxs-lookup"><span data-stu-id="597cf-149">In order to view and use your Secure Score dashboard, you must be assigned one of the following roles in [Azure Active Directory](https://docs.microsoft.com/azure/active-directory/users-groups-roles/directory-assign-admin-roles#available-roles):</span></span>
- <span data-ttu-id="597cf-150">전역 관리자</span><span class="sxs-lookup"><span data-stu-id="597cf-150">Global Administrator</span></span>
- <span data-ttu-id="597cf-151">대금 청구 관리자</span><span class="sxs-lookup"><span data-stu-id="597cf-151">Billing Administrator</span></span>
- <span data-ttu-id="597cf-152">사용자 관리자</span><span class="sxs-lookup"><span data-stu-id="597cf-152">User Administrator</span></span>
- <span data-ttu-id="597cf-153">암호 관리자</span><span class="sxs-lookup"><span data-stu-id="597cf-153">Password Administrator</span></span>
- <span data-ttu-id="597cf-154">보안 관리자</span><span class="sxs-lookup"><span data-stu-id="597cf-154">Security Administrator</span></span>
- <span data-ttu-id="597cf-155">보안 독자</span><span class="sxs-lookup"><span data-stu-id="597cf-155">Security Reader</span></span>
- <span data-ttu-id="597cf-156">Exchange 관리자</span><span class="sxs-lookup"><span data-stu-id="597cf-156">Exchange Administrator</span></span>
- <span data-ttu-id="597cf-157">SharePoint 관리자</span><span class="sxs-lookup"><span data-stu-id="597cf-157">SharePoint Administrator</span></span>

 <span data-ttu-id="597cf-158">관리자 역할이 할당 되지 않은 사용자는 보안 점수에 액세스할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="597cf-158">Users who aren't assigned an admin role won't be able to access Secure Score.</span></span>

## <a name="related-topics"></a><span data-ttu-id="597cf-159">관련 항목</span><span class="sxs-lookup"><span data-stu-id="597cf-159">Related topics</span></span>

[<span data-ttu-id="597cf-160">보안 대시보드 개요</span><span class="sxs-lookup"><span data-stu-id="597cf-160">Security dashboard overview</span></span>](security-dashboard.md)

[<span data-ttu-id="597cf-161">내가 구독한 것은 무엇인가요?</span><span class="sxs-lookup"><span data-stu-id="597cf-161">What subscription do I have?</span></span>](https://docs.microsoft.com/office365/admin/admin-overview/what-subscription-do-i-have?view=o365-worldwide)
