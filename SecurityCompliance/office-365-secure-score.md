---
title: Office 365 보안 점수
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 01/25/2019
ms.audience: Admin
ms.topic: overview
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: c9e7160f-2c34-4bd0-a548-5ddcc862eaef
description: 얼마나 안전 조직 실제로 Office 365에 지 궁금한 적이 있습니까? 보안 점수를 위해 여기 됩니다. 일반 작업 및 Office 365의 보안 설정에 따라 조직의 보안을 분석 하 여 점수를 할당 하는 보안 점수입니다.
ms.openlocfilehash: bc0379e40b09e63e5fded1b1a289d40c306def91
ms.sourcegitcommit: 7e2a0185cadea7f3a6afc5ddc445eac2e1ce22eb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/11/2019
ms.locfileid: "29559091"
---
# <a name="office-365-secure-score"></a><span data-ttu-id="b4f8b-105">Office 365 보안 점수</span><span class="sxs-lookup"><span data-stu-id="b4f8b-105">Office 365 Secure Score</span></span>

<span data-ttu-id="b4f8b-p102">**요약** 얼마나 안전 조직 실제로 Office 365에 지 궁금한 적이 있습니까? 보안 점수를 위해 여기 됩니다. 일반 작업 및 Office 365의 보안 설정에 따라 조직의 보안을 분석 하 여 점수를 할당 하는 보안 점수입니다. 점수 보안 및 사용 방법에 대 한 개요를 얻으려면이 문서를 읽어보십시오.</span><span class="sxs-lookup"><span data-stu-id="b4f8b-p102">**Summary** Ever wonder how secure your organization really is in Office 365? Secure Score is here to help. Secure Score analyzes your organization's security  based on your regular activities and security settings in Office 365, and assigns a score. Read this article to get an overview of Secure Score and how you can use it.</span></span>
  
## <a name="how-to-get-to-secure-score"></a><span data-ttu-id="b4f8b-110">보안 점수를 얻는 방법</span><span class="sxs-lookup"><span data-stu-id="b4f8b-110">How to get to Secure Score</span></span>

<span data-ttu-id="b4f8b-111">조직에 [Office 365 Enterprise](https://docs.microsoft.com/office365/enterprise/), [Microsoft 365 비즈니스](https://docs.microsoft.com/microsoft-365/business/)또는 Office 365 프리미엄을 포함 하는 구독 하는 경우 [필요한 사용 권한](#required-permissions)을 가진 사용자 방문 하 여 조직의 보안 점수를 볼 수 있습니다. [https://securescore.office.com](https://securescore.office.com).</span><span class="sxs-lookup"><span data-stu-id="b4f8b-111">If your organization has a subscription that includes [Office 365 Enterprise](https://docs.microsoft.com/office365/enterprise/), [Microsoft 365 Business](https://docs.microsoft.com/microsoft-365/business/), or Office 365 Business Premium, and you have the [necessary permissions](#required-permissions), you can view your organization's secure score by visiting [https://securescore.office.com](https://securescore.office.com).</span></span> 

<span data-ttu-id="b4f8b-112">보안 & 준수 센터를 방문 하면 또는 ([https://protection.office.com](https://protection.office.com)), 현재 점수가 제공 하는 보안 점수 위젯을 찾아볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b4f8b-112">Alternatively, you can visit the Security & Compliance Center ([https://protection.office.com](https://protection.office.com)), where you'll find a Secure Score widget that provides you with your current score.</span></span>

![보안 점수 위젯](media/SecureScoreWidget-o365.png)

<span data-ttu-id="b4f8b-114">위젯 Secure 점수 대시보드에 대 한 링크를 포함합니다.</span><span class="sxs-lookup"><span data-stu-id="b4f8b-114">The widget includes a link to your Secure Score dashboard.</span></span>

![보안 점수 대시보드](media/SecureScore-WelcomeScreen.png)
  
## <a name="how-it-works"></a><span data-ttu-id="b4f8b-116">작동 방법</span><span class="sxs-lookup"><span data-stu-id="b4f8b-116">How it works</span></span>

<span data-ttu-id="b4f8b-p103">보안 점수 설정 및 작업 Microsoft에 의해 설정 된 초기 계획을 비교 하는 (예: OneDrive, SharePoint 및 Exchange) 한 다음 사용 중인 Office 365 서비스를 결정 합니다. 방법에 따라 점수를 얻을 수 잘 부합 조직 관련 된 보안에 대 한 유용한 정보입니다. 또한 조직의 점수를 개선 하기 위해 수행할 수 있는 단계에서 권장 사항을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b4f8b-p103">Secure Score determines what Office 365 services you're using (such as OneDrive, SharePoint, and Exchange) then compares your settings and activities to a baseline established by Microsoft. You'll get a score based on how well aligned your organization is with security best practices. You'll also get recommendations on steps you can take to improve your organization's score.</span></span> 
  
![Office 365 보안 점수 도구에서 작업 큐](media/SecureScore-ActionsToTake.png)
  
<span data-ttu-id="b4f8b-p104">구입한 서비스에 따라 점수를 계산 하는 보안 점수입니다. 예는 Exchange Online 계획을만 구입한 경우 SharePoint Online 보안 기능에 대 한 획득 수 없습니다. 점수의 분모는 구입 제품에 적용 되는 컨트롤에 대 한 모든 초기 계획의 합입니다. 분자는 합계를 모든 컨트롤의 완료 되 면 하면 또는를 부분적으로 완료 되 면이 행 해야할 임무가 제어 하는 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="b4f8b-p104">Secure Score calculates your score based on the services you purchased. For example, if you only purchased an Exchange Online plan, you won't be scored for SharePoint Online security features. The denominator of the score is the sum of all the baselines for the controls that apply to the products you purchased. The numerator is the sum of all the controls for which you completed, or partially completed, the actions to fulfill that control.</span></span>

<span data-ttu-id="b4f8b-125">에 대해 자세히 알아보려면 어떤 단계를 수행 하 고, 하는 것은 위협에서 사용자를 보호 하는 동작을 확장 하 고 얼마나 많은 포인트 권장 조치를 따라 되 면 귀하의 점수 증가 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4f8b-125">Expand an action to learn about what steps to take, the threats it'll help protect you from, and how many points your score will increase once you follow the recommendation.</span></span>
  
![Office 365 보안 점수 도구에서 확장 된 함수](media/SecureScore-DetailedActionToTake.png)
  
<span data-ttu-id="b4f8b-127">조직의 보안에서 이러한 작업의 영향을 보려면 **점수 분석기** 탭을 선택 하 고 대화 기록을 검토 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4f8b-127">To see the impact of your actions on your organization's security, select the **Score Analyzer** tab and review your history.</span></span> 
  
![Office 365 보안 점수 도구의 점수 분석기 탭](media/SecureScore-ScoreAnalyzer-7days.png)
  
<span data-ttu-id="b4f8b-129">다음은 차트 아래 범주별으로 점수 및 작업의 목록이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b4f8b-129">Below the chart, you'll see a list of scores and actions by category.</span></span> 
  
![탭의 점수 분석기 선택 된 데이터 요소를 보여주는 그래프](media/SecureScore-Analyzer-breakdownbelowchart.png)
 
<span data-ttu-id="b4f8b-131">**[점수가 하지]는** 것 처럼 레이블이 지정 된 작업을 수행할 수 조직에 대 한 있지만 점수가 하지 Secure 점수에 연결 되어 되지 않을 때문에 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4f8b-131">Actions that are labeled as **[Not Scored]** are ones you can perform for your organization, but because they are not connected to Secure Score, they are not scored.</span></span>  

<span data-ttu-id="b4f8b-p105">**점수 분석기** 페이지에서 특정 날짜에 대 한 데이터 요소를 클릭 한 다음 참조는 완성 된 및 불완전 한 작업을 알려면 해당 날짜에 대 한 변경까지 아래로 스크롤하십시오. 하루에 한번 (약 오전 1시 PST)는 점수 계산 됩니다. 측정 된 동작을 변경 하는 경우는 점수 다음날 자동으로 업데이트 됩니다. 점수가에 반영 수에 대 한 변경에 대 한 최대 48 시간까지 걸립니다.</span><span class="sxs-lookup"><span data-stu-id="b4f8b-p105">On the **Score Analyzer** page, click a data point for a specific day, then scroll down to see the completed and incomplete actions for that day to find out what changed. The score is calculated once per day (around 1:00 AM PST). If you make a change to a measured action, the score will automatically update the next day. It takes up to 48 hours for a change to be reflected in your score.</span></span>

<span data-ttu-id="b4f8b-p106">보안 점수 절대 측정 하는 express 하지 않는 도달 하기에 어떻게 가능성이의 합니다. 도달 되 고 위험을 오프셋할 수 있는 기능을 채택한 범위를 나타냅니다. 서비스가 없습니다 있습니다를 위반 하지 않습니다, 하 고 보안 점수 보장 어떤 방식에서으로 해석 하지 않아야 보장할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b4f8b-p106">Secure Score does not express an absolute measure of how likely you are to get breached. It expresses the extent to which you have adopted features that can offset the risk of being breached. No service can guarantee that you will not be breached, and the Secure Score should not be interpreted as a guarantee in any way.</span></span>
 
## <a name="how-secure-score-helps"></a><span data-ttu-id="b4f8b-139">보안 점수를 손쉽게 방법</span><span class="sxs-lookup"><span data-stu-id="b4f8b-139">How Secure Score helps</span></span>

<span data-ttu-id="b4f8b-p107">보안 점수와 Office 365 (대부분의 이미 구입한 있지만 인식 되지 않을 수)의 기본 제공 보안 기능을 사용 하 여 조직의 보안 상황을 향상 시킬 수 있습니다. 이러한 기능에 대해 자세히 안심 조직 위협 으로부터 보호 하기 위해 오른쪽 단계를 수행 하는 기능을 제공 하는 데 도움이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b4f8b-p107">With Secure Score, you can help improve your organization's security posture by using the built-in security features in Office 365 (many of which you already purchased but might not be aware of). Learning more about these features can help give you peace of mind that you're taking the right steps to protect your organization from threats.</span></span>
  
<span data-ttu-id="b4f8b-p108">하지만 word 것에 대 한 소요 방금 하지 않습니다. 고객에 게 보안 점수를 사용 하는 고객에 게 사용 하지 않을 보다 더 많은 시간을 증가 자신의 점수를 살펴보았습니다. (자신의 점수 증가 해당 조직에서 현재 사용 되는 보안 기능.)</span><span class="sxs-lookup"><span data-stu-id="b4f8b-p108">But don't just take our word for it. Customers who are using Secure Score have seen their score increase five times more than customers who aren't using it. (The increase in their score corresponds with the security features being used in their organizations.)</span></span>
  
> [!NOTE]
> <span data-ttu-id="b4f8b-p109">보안 점수 절대 측정 하는 express 하지 않는 도달 하기에 어떻게 가능성이의 합니다. 도달 되 고 위험을 오프셋할 수 있는 제어 채택 범위를 나타냅니다. 서비스가 없습니다 있습니다를 위반 하지 않습니다, 하 고 보안 점수 보장 어떤 방식에서으로 해석 하지 않아야 보장할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b4f8b-p109">Secure Score does not express an absolute measure of how likely you are to get breached. It expresses the extent to which you have adopted controls which can offset the risk of being breached. No service can guarantee that you will not be breached, and Secure Score should not be interpreted as a guarantee in any way.</span></span> 
  
## <a name="required-permissions"></a><span data-ttu-id="b4f8b-148">필요한 사용 권한</span><span class="sxs-lookup"><span data-stu-id="b4f8b-148">Required permissions</span></span>

<span data-ttu-id="b4f8b-149">본 Secure 점수 대시보드를 사용 하기 위해 할당 되어 있어야 Azure Active Directory에서 다음 역할 중 하나:</span><span class="sxs-lookup"><span data-stu-id="b4f8b-149">In order to view and use your Secure Score dashboard, you must be assigned one of the following roles in Azure Active Directory:</span></span>
- <span data-ttu-id="b4f8b-150">전역 관리자</span><span class="sxs-lookup"><span data-stu-id="b4f8b-150">Global Administrator</span></span>
- <span data-ttu-id="b4f8b-151">대금 청구 관리자</span><span class="sxs-lookup"><span data-stu-id="b4f8b-151">Billing Administrator</span></span>
- <span data-ttu-id="b4f8b-152">사용자 관리자</span><span class="sxs-lookup"><span data-stu-id="b4f8b-152">User Administrator</span></span>
- <span data-ttu-id="b4f8b-153">암호 관리자</span><span class="sxs-lookup"><span data-stu-id="b4f8b-153">Password Administrator</span></span>
- <span data-ttu-id="b4f8b-154">보안 관리자</span><span class="sxs-lookup"><span data-stu-id="b4f8b-154">Security Administrator</span></span>
- <span data-ttu-id="b4f8b-155">보안 읽기 권한자</span><span class="sxs-lookup"><span data-stu-id="b4f8b-155">Security Reader</span></span>
- <span data-ttu-id="b4f8b-156">Exchange 관리자</span><span class="sxs-lookup"><span data-stu-id="b4f8b-156">Exchange Administrator</span></span>
- <span data-ttu-id="b4f8b-157">SharePoint 관리자에 게</span><span class="sxs-lookup"><span data-stu-id="b4f8b-157">SharePoint Administrator</span></span>

 <span data-ttu-id="b4f8b-158">관리 역할 할당 되지 않은 사용자에 게 보안 점수에 액세스할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="b4f8b-158">Users who aren't assigned an admin role won't be able to access Secure Score.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b4f8b-159">관련 항목</span><span class="sxs-lookup"><span data-stu-id="b4f8b-159">Related topics</span></span>

[<span data-ttu-id="b4f8b-160">보안 대시보드 개요 (영문)</span><span class="sxs-lookup"><span data-stu-id="b4f8b-160">Security dashboard overview</span></span>](security-dashboard.md)

[<span data-ttu-id="b4f8b-161">내가 구독한 것은 무엇인가요?</span><span class="sxs-lookup"><span data-stu-id="b4f8b-161">What subscription do I have?</span></span>](https://docs.microsoft.com/office365/admin/admin-overview/what-subscription-do-i-have?view=o365-worldwide)