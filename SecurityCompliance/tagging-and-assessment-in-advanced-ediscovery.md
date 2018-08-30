---
title: Office 365 Advanced eDiscovery에서 태그 지정 및 평가
ms.author: chrfox
author: chrfox
manager: laurawi
ms.date: 9/14/2017
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: b5c82de7-ed2f-4cc6-becd-db403faf4d18
description: '평가 교육, 파일, 태그 지정 하 고 Office 365 고급 eDiscovery의 평가 결과 검토할 때를 포함 하 여 수행 하는 단계를 검토 합니다. '
ms.openlocfilehash: 0f67dd4780a29536888231f556c18fe887f230ba
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22533367"
---
# <a name="tagging-and-assessment-in-office-365-advanced-ediscovery"></a><span data-ttu-id="71c0c-103">Office 365 Advanced eDiscovery에서 태그 지정 및 평가</span><span class="sxs-lookup"><span data-stu-id="71c0c-103">Tagging and Assessment in Office 365 Advanced eDiscovery</span></span>

> [!NOTE]
> <span data-ttu-id="71c0c-p101">고급 eDiscovery 조직에 대 한 고급 준수 추가 기능 또는 e 5 구독은 Office 365 E3 필요합니다. 해당 요금제에 가입한 상태 고급 eDiscovery 시도 하려는 하지 경우에 [Office 365 Enterprise e 5의 평가판 등록](https://go.microsoft.com/fwlink/p/?LinkID=698279)할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="71c0c-p101">Advanced eDiscovery requires an Office 365 E3 with the Advanced Compliance add-on or an E5 subscription for your organization. If you don't have that plan and want to try Advanced eDiscovery, you can [sign up for a trial of Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span></span> 
  
<span data-ttu-id="71c0c-106">이 섹션에서는 고급 eDiscovery 관련성 평가 모듈에 대 한 절차에 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="71c0c-106">This section describes the procedure for the Advanced eDiscovery Relevance Assessment module.</span></span> 
  
## <a name="performing-assessment-training-and-analysis"></a><span data-ttu-id="71c0c-107">평가 교육 및 분석을 수행합니다.</span><span class="sxs-lookup"><span data-stu-id="71c0c-107">Performing Assessment training and analysis</span></span>

1. <span data-ttu-id="71c0c-108">**관련성 \> 추적** 탭에서 사례 평가 시작 하려면 **평가** 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="71c0c-108">In the **Relevance \> Track** tab, click **Assessment** to start case assessment.</span></span> 
    
    <span data-ttu-id="71c0c-109">예이 절차의 목적으로 샘플 평가 500 파일 집합이 만들어지고 태그 패널, 표시 된 파일 내용 및 기타 태그 지정 옵션을 포함 하는 **태그** 탭이 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="71c0c-109">For example purposes in this procedure, a sample assessment set of 500 files is created and the **Tag** tab is displayed, which contains the Tagging panel, displayed file content and other tagging options.</span></span> 
    
    ![평가 대 한 관련 태그 탭](media/c8acf891-b1cd-4344-816c-eabb8cbbe742.png)
  
2. <span data-ttu-id="71c0c-111">이 예제에서 각 파일을 검토 하 고 각 사례 문제에 대 한 파일의 관련성을 결정 하지는 Relevance (R)를 사용 하 여 파일에 태그 지정 **태그 지정 패널** 창의 관련 (NR) 및 건너뛰기 단추를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="71c0c-111">Review each file in the sample, determine the file's relevance for each case issue, and tag the file using the Relevance (R), Not relevant (NR) and Skip buttons in the **Tagging panel** pane.</span></span> 
    
    > [!NOTE]
    >  <span data-ttu-id="71c0c-p102">평가 500 태그가 지정 된 파일이 필요합니다. 파일 "을 건너뛰지", 태그에 더 많은 파일 받게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="71c0c-p102">Assessment requires 500 tagged files. If files are "skipped", you will receive more files to tag.</span></span> 
  
3. <span data-ttu-id="71c0c-114">이 예제에서 모든 파일에 태그 지정을 한 후 **계산**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="71c0c-114">After tagging all files in the sample, click **Calculate**.</span></span> 
    
    <span data-ttu-id="71c0c-p103">평가 현재 오류 여백 및 다양성은 계산 아래와 같이 당 미화, 확장 된 세부 정보가 들어 있는 **관련성 추적** 탭에 표시 됩니다. 이 대화 상자에 대 한 자세한 내용은 뒷부분의 "결과 검토 평가" 섹션에 설명 되어있습니다.</span><span class="sxs-lookup"><span data-stu-id="71c0c-p103">The Assessment current error margin and richness are calculated and displayed in the **Relevance Track** tab, with expanded details per issue, as shown below. More details about this dialog are described in the later section "Reviewing Assessments results".</span></span> 
    
    ![관련 트랙-평가](media/da911ba5-8678-40d6-9ad5-fd0b058355c1.png)
  
    > [!TIP]
    > <span data-ttu-id="71c0c-p104">기본적으로 진행 하는 기본 다음 단계에는 문제에 대 한 평가 진행률 표시기가 완료 되 면 평가 예제를 검토 하 고 충분 한 관련 파일 태그가 지정 된 나타내는 하는 것이 좋습니다. > 그렇지 않은 경우, **추적** 탭 결과 및 컨트롤의 여백 오류 및 다음 단계를 확인 하려는 경우 **수정** 옆에 있는 **다음 단계**를 클릭, **계속 평가**선택한 다음 **확인**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="71c0c-p104">By default, we recommend that you proceed to the default Next step when the Assessment progress indicator for the issue has completed, indicating that the assessment sample was reviewed and sufficient relevant files were tagged. > Otherwise, if you want to view the **Track** tab results and control the margin of error and the next step, click **Modify** adjacent to **Next Step**, select **Continue assessment**, and then click **OK**.</span></span> 
  
1. <span data-ttu-id="71c0c-p105">보고 하 여 문제 당 평가 매개 변수를 지정 **평가** 확인란의 오른쪽에 **수정** 을 클릭 합니다. 다음 예제와 같이 각 문제에 대 한는 **평가 수준** 대화 상자가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="71c0c-p105">Click **Modify** to the right of the **Assessment** check box to view and specify assessment parameters per issue. An **Assessment level** dialog for each issue is displayed, as shown in the following example:</span></span> 
    
    ![평가 수준 사례 문제](media/b7113fef-d125-4617-ae1b-c9eb0bf79aec.png)
  
    <span data-ttu-id="71c0c-123">이 문제에 대 한 다음 매개 변수는 계산 하 고 **평가 수준** 대화 상자에 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="71c0c-123">The following parameters for the issue are calculated and displayed in the **Assessment level** dialog:</span></span> 
    
    <span data-ttu-id="71c0c-p106">**회수에 대 한 대상 오류 여백 추정**:이 값에 따라을 검토 하는 데 필요한 추가 파일의 예상된 수 계산 됩니다. 회수에 사용 되는 여백 95% 신뢰 수준 및 75% 보다 큽니다.</span><span class="sxs-lookup"><span data-stu-id="71c0c-p106">**Target error margin for recall estimates**: Based on this value, the estimated number of additional files necessary to review is calculated. The margin used for recall is greater than 75% and with a 95% confidence level.</span></span> 
    
    <span data-ttu-id="71c0c-126">**추가 평가 파일 필요한**: 현재 오류 여백 요구 사항을 충족 되지 않은 경우에 필요한 얼마나 많은 더 많은 파일을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="71c0c-126">**Additional assessment files required**: Indicates how many more files are necessary if the current error margin's requirements have not been met.</span></span> 
    
2. <span data-ttu-id="71c0c-127">현재 오류 여백을 조정 하 고 각각 다른 오류 여백 (당 문제)의 효과 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="71c0c-127">To adjust the current error margin and see the effect of different error margins (per issue):</span></span>
    
1. <span data-ttu-id="71c0c-128">**문제를 선택** 목록에서 문제점을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="71c0c-128">In the **Select issue** list, select an issue.</span></span> 
    
2. <span data-ttu-id="71c0c-129">**회수에 대 한 대상 오류 여백 예상치**를에서 새 값을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="71c0c-129">In **Target error margin for recall estimates**, enter a new value.</span></span>
    
3. <span data-ttu-id="71c0c-130">에 따라 조정의 영향을 보려면 **값을 업데이트** 를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="71c0c-130">Click **Update values** to see the impact of the adjustments.</span></span> 
    
3. <span data-ttu-id="71c0c-131">다음과 같은 추가 매개 변수 및 세부 정보를 확인 하려면 **평가 수준** 대화 상자에서 **고급** 을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="71c0c-131">Click **Advanced** in the **Assessment level** dialog to see the following additional parameters and details:</span></span> 
    
    ![평가 수준 사례 문제를 상세하게 보기](media/577d7e0e-95df-48c2-9dec-bdeab5e801d8.png)
  
    <span data-ttu-id="71c0c-133">**기간 미정 다양성**: 현재 평가 결과 따라 다양성 예상</span><span class="sxs-lookup"><span data-stu-id="71c0c-133">**Estimated richness**: Estimated richness according to the current assessment results</span></span>
    
    <span data-ttu-id="71c0c-p107">**가정된 회수에**: 기본적으로 대상 오류 여백 75% 이상이 회수에 적용 합니다. 이 매개 변수를 변경 하 고 다른 회수 값 범위에는 오차를 제어 하려는 경우에 **편집** 을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="71c0c-p107">**For assumed recall**: By default, the target error margin applies to recall above 75%. Click **Edit** if you want to change this parameter and control the margin of error on a different range of recall values.</span></span> 
    
    <span data-ttu-id="71c0c-p108">**신뢰 수준**: 기본적으로 신뢰에 대 한 권장된 오류 여백은 95%입니다. 이 매개 변수를 변경 하려는 경우에 **편집** 을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="71c0c-p108">**Confidence level**: By default, the recommended error margin for confidence is 95%. Click **Edit** if you want to change this parameter.</span></span> 
    
    <span data-ttu-id="71c0c-138">**예상 다양성 오류 여백**: 업데이트 된 값이 제공,이 풍부한 기능의 예상 되는 오차 모든 추가 평가 파일을 검토 한 후 합니다.</span><span class="sxs-lookup"><span data-stu-id="71c0c-138">**Expected richness error margin**: Given the updated values, this is the expected margin of error of the richness, after all additional assessment files are reviewed.</span></span>
    
    <span data-ttu-id="71c0c-139">**추가 평가 파일 필요한**: 업데이트 된 값이 지정, 추가 평가 수가 파일의 목표에 도달를 검토 해야 할 합니다.</span><span class="sxs-lookup"><span data-stu-id="71c0c-139">**Additional assessment files required**: Given the updated values, the number of additional assessment files that need to be reviewed to reach the target.</span></span>
    
    <span data-ttu-id="71c0c-140">**총 평가 파일 필요한**: 검토를 위해 필요한 평가 파일의 총 업데이트 된 값을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="71c0c-140">**Total assessment files required**: Given the updated values, total assessment files required for review.</span></span>
    
    <span data-ttu-id="71c0c-141">**평가에서 관련 파일의 예상 번호**: 업데이트 된 값을 예상 되는 모든 추가 평가 파일을 검토 한 후 전체 평가에 관련 된 파일 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="71c0c-141">**Expected number of relevant files in assessment**: Given the updated values, the expected number of relevant files in the entire assessment after all additional assessment files are reviewed.</span></span>
    
4. <span data-ttu-id="71c0c-p109">매개 변수를 변경 하는 경우 **값이 다시 계산**을 클릭 합니다. 마쳤으면, 하나의 문제가 있는 경우는 변경 내용 (또는 **다음** 여러 문제를 검토 하거나 수정 하려면 했으면 및 다음 **마침**)를 저장 하려면 **확인** 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="71c0c-p109">Click **Recalculate values**, if parameters are changed. When you are done, if there is one issue, click **OK** to save the changes (or **Next** when there are multiple issues to review or modify and then **Finish**).</span></span> 
    
    <span data-ttu-id="71c0c-144">모든 문제 검토 되거나 조정 된 후 여러 문제가 있는 경우는 **평가 수준: 요약** 다음 예제와 같이 대화 상자가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="71c0c-144">When there are multiple issues, after all issues have been reviewed or adjusted, an **Assessment level: summary** dialog is displayed, as shown in the following example.</span></span> 
    
    ![평가 수준 요약](media/4997b46d-10a5-4abc-b3b2-7b75a370eb9e.png)
  
    <span data-ttu-id="71c0c-146">평가 성공적으로 완료 관련성 교육의 다음 단계로 진행 합니다.</span><span class="sxs-lookup"><span data-stu-id="71c0c-146">Upon successful completion of assessment, proceed to the next stage in Relevance training.</span></span>
    
## <a name="reviewing-assessment-results"></a><span data-ttu-id="71c0c-147">평가 결과 검토</span><span class="sxs-lookup"><span data-stu-id="71c0c-147">Reviewing assessment results</span></span>

<span data-ttu-id="71c0c-148">평가 샘플 태그가 지정 된 후 평가 결과 계산 하 고 관련성 추적 탭에 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="71c0c-148">After an Assessment sample is tagged, the assessment results are calculated and displayed in the Relevance Track tab.</span></span>
  
<span data-ttu-id="71c0c-149">다음과 같은 결과가 표시 되는 확장 된 추적 표시에서:</span><span class="sxs-lookup"><span data-stu-id="71c0c-149">The following results are displayed in the expanded Track display:</span></span> 
  
- <span data-ttu-id="71c0c-150">회수 예측에 대 한 현재 오류 여백 평가</span><span class="sxs-lookup"><span data-stu-id="71c0c-150">Assessment current error margin for recall estimates</span></span>
    
- <span data-ttu-id="71c0c-151">예상된 풍부한 기능</span><span class="sxs-lookup"><span data-stu-id="71c0c-151">Estimated richness</span></span>
    
- <span data-ttu-id="71c0c-152">검토용 필요한 추가 평가 파일</span><span class="sxs-lookup"><span data-stu-id="71c0c-152">Additional assessment files required (for review)</span></span>
    
<span data-ttu-id="71c0c-p110">평가 현재 오류 여백은 고급 eDiscovery가 권장 오류 여백입니다. "추가 평가 필요한 파일"에 대 한 표시 되는 번호는 권장 사항에 해당 합니다.</span><span class="sxs-lookup"><span data-stu-id="71c0c-p110">The Assessment current error margin is the error margin recommended by Advanced eDiscovery. The number displayed for the "Additional assessment files required" corresponds to that recommendation.</span></span>
  
<span data-ttu-id="71c0c-p111">평가 진행률 표시기 완료 되 면 현재 오류 오차는 평가의 수준을 표시 합니다. 평가 진행 하는 경우 사용자가 다른 평가 샘플을 태그를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="71c0c-p111">The Assessment progress indicator shows the level of completion of the assessment, given the current error margin. When assessment is underway, the user will tag another assessment sample.</span></span>
  
<span data-ttu-id="71c0c-157">완료 된 것으로 평가 표시 하는 평가 진행률 표시기를 평가 샘플 검토를 완료 하 고 충분 한 관련 파일 태그가 지정 된 의미 합니다.</span><span class="sxs-lookup"><span data-stu-id="71c0c-157">When the assessment progress indicator shows assessment as complete, that means the assessment sample review was completed and sufficient relevant files were tagged.</span></span> 
  
<span data-ttu-id="71c0c-158">확장 된 추적 표시 권장된 다음 단계에서는, 평가 통계 및 자세한 결과에 대 한 액세스를 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="71c0c-158">The expanded Track display shows the recommended next step, the assessment statistics, and access to detailed results.</span></span>
  
<span data-ttu-id="71c0c-p112">다양성 매우 낮을 때 유용한 통계를 생성 하려면 관련 파일의 최소한의 수에 도달 하는 데 필요한 추가 평가 파일 수가 매우 높습니다. 고급 eDiscovery 교육 이동 하는 것을 권장 다음 합니다. 평가 진행률 표시기 회색으로 표시 됩니다. 하 고 통계를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="71c0c-p112">When richness is very low, the number of additional assessment files needed to reach a minimal number of relevant files to produce useful statistics is very high. Advanced eDiscovery will then recommend moving on to training. The assessment progress indicator will be shaded, and no statistics will be available.</span></span> 
  
<span data-ttu-id="71c0c-p113">통계적 기반된 안정화 없는 경우에는 더 낮은 수준의 정확성 및 신뢰 수준을 사용 하 여 결과 없을 것입니다. 그러나 파일을 찾는데 관련 관련 파일을 찾을 수의 비율을 알고 있는 해야하는 경우 이러한 결과 사용할 수 있습니다. 마찬가지로,이 상태 하는데 사용할 수 낮은 다양성와 문제를 교육 관련성 점수가 포함 된 특정 문제에 관련 파일에 대 한 액세스를 가속화할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="71c0c-p113">In the absence of statistically based stabilization, there will be results with a lower level of accuracy and confidence level. However, these results can be used to find relevant files when you do not need to know the percentage of relevant files found. Similarly, this status can be used to train issues with low richness, where Relevance scores can accelerate access to files relevant to a specific issue.</span></span>
  
> [!TIP]
> <span data-ttu-id="71c0c-p114">**관련성 \> 추적** 탭을 표시 하는 확장 된 문제, 다음 보기 옵션을 사용할 수: > 다음과 같이 권장 되는 다음 단계 **다음 단계: 태그 지정** **수정** 단추를 클릭 하 여 문제) (당 바이패스 될 해당 오른쪽, 선택한 다음 **다음 단계**에 서로 다른 단계를 선택 합니다. 평가 진행률 표시기 완료 되지 않으면 더 많은 평가 파일 태그를 지정 하 고 통계 정확 하 게 되도록 하려면 다음 권장된 옵션을 평가 됩니다. > 오류 여백을 변경 하 고 **평가 수준 대화**를 **회수에 대 한 대상 오류 여백 추정**, 변경 및 **업데이트 값**을 클릭 하 고 **수정**클릭 하 여 그 영향을 평가 수 있습니다. 또한이 대화 상자에서 **고급**을 클릭 하 여 고급 옵션을 볼 수 있습니다. > **보기**를 클릭 하 여 추가 평가 수준 통계 및 해당 영향을 볼 수 있습니다. 표시 된 세부 결과 대화 상자에서 사용할 수 있는 통계가 문제, 당 최소한 500 태그가 지정 된 평가 파일 및 문제에 대 한 최소 18 파일 다음과 관련 됨으로 태그가 지정 된 경우.</span><span class="sxs-lookup"><span data-stu-id="71c0c-p114">In the **Relevance \> Track** tab, expanded issue display, the following viewing options are available: > The recommended next step, such as **Next step: Tagging** can be bypassed (per issue) by clicking the **Modify** button to its right, and then selecting an different step in the **Next step**. When the assessment progress indicator has not completed, assessment will be the next recommended option, to tag more assessment files and increase statistics accuracy. > You can change the error margin and assess its impact, by clicking **Modify**, and in the **Assessment level dialog**, changing the **Target error margin for recall estimates**, and clicking **Update values**. Also, in this dialog, you can view advanced options, by clicking **Advanced**. > You can view additional assessment level statistics and their impact by clicking **View**. In the displayed Detail results dialog, statistics are available per issue, when there are at least 500 tagged assessment files and at least 18 files are tagged as Relevant for the issue.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="71c0c-171">참고 항목</span><span class="sxs-lookup"><span data-stu-id="71c0c-171">See also</span></span>

[<span data-ttu-id="71c0c-172">Office 365 Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="71c0c-172">Office 365 Advanced eDiscovery</span></span>](office-365-advanced-ediscovery.md)
  
[<span data-ttu-id="71c0c-173">관련성에 이해 평가</span><span class="sxs-lookup"><span data-stu-id="71c0c-173">Understanding Assessment in Relevance</span></span>](assessment-in-relevance-in-advanced-ediscovery.md)
  
[<span data-ttu-id="71c0c-174">태그 지정 및 관련성 교육</span><span class="sxs-lookup"><span data-stu-id="71c0c-174">Tagging and Relevance training</span></span>](tagging-and-relevance-training-in-advanced-ediscovery.md)
  
[<span data-ttu-id="71c0c-175">관련성 분석 추적</span><span class="sxs-lookup"><span data-stu-id="71c0c-175">Tracking Relevance analysis</span></span>](track-relevance-analysis-in-advanced-ediscovery.md)
  
[<span data-ttu-id="71c0c-176">결과에 따라 결정</span><span class="sxs-lookup"><span data-stu-id="71c0c-176">Deciding based on the results</span></span>](decision-based-on-the-results-in-advanced-ediscovery.md)
  
[<span data-ttu-id="71c0c-177">관련성 분석 테스트</span><span class="sxs-lookup"><span data-stu-id="71c0c-177">Testing Relevance analysis</span></span>](test-relevance-analysis-in-advanced-ediscovery.md)

