---
title: Office 365 Advanced eDiscovery에서 태그 지정 및 평가
ms.author: chrfox
author: chrfox
manager: laurawi
ms.date: 9/14/2017
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: b5c82de7-ed2f-4cc6-becd-db403faf4d18
description: '태그 파일을 포함 하 여 평가 교육을 수행 하는 단계를 검토 하 고 Office 365 Advanced eDiscovery에서 평가 결과를 검토 합니다. '
ms.openlocfilehash: 02dae23b6489b40243272beea1d79e871ca6a911
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30217938"
---
# <a name="tagging-and-assessment-in-office-365-advanced-ediscovery"></a><span data-ttu-id="da451-103">Office 365 Advanced eDiscovery에서 태그 지정 및 평가</span><span class="sxs-lookup"><span data-stu-id="da451-103">Tagging and Assessment in Office 365 Advanced eDiscovery</span></span>

> [!NOTE]
> <span data-ttu-id="da451-p101">Advanced eDiscovery를 사용하려면 Office 365 E3의 고급 준수 추가 기능이나 조직을 위한 E5 구독이 필요합니다. 이 요금제가 없는 상태에서 Advanced eDiscovery를 사용하려는 경우에는 [Office 365 Enterprise E5 평가판을 등록](https://go.microsoft.com/fwlink/p/?LinkID=698279)할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="da451-p101">Advanced eDiscovery requires an Office 365 E3 with the Advanced Compliance add-on or an E5 subscription for your organization. If you don't have that plan and want to try Advanced eDiscovery, you can [sign up for a trial of Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span></span> 
  
<span data-ttu-id="da451-106">이 섹션에서는 고급 eDiscovery 관련성 평가 모듈의 절차에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="da451-106">This section describes the procedure for the Advanced eDiscovery Relevance Assessment module.</span></span> 
  
## <a name="performing-assessment-training-and-analysis"></a><span data-ttu-id="da451-107">평가 교육 및 분석 수행</span><span class="sxs-lookup"><span data-stu-id="da451-107">Performing Assessment training and analysis</span></span>

1. <span data-ttu-id="da451-108">\*\* \> 관련성 추적\*\* 탭에서 **평가** 를 클릭 하 여 사례 평가를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="da451-108">In the **Relevance \> Track** tab, click **Assessment** to start case assessment.</span></span> 
    
    <span data-ttu-id="da451-109">이 절차의 목적을 예로 들면, 500 파일의 샘플 평가 집합을 만들고 태그 지정 패널, 표시 된 파일 콘텐츠 및 기타 태그 지정 옵션을 포함 하는 **Tag** 탭이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="da451-109">For example purposes in this procedure, a sample assessment set of 500 files is created and the **Tag** tab is displayed, which contains the Tagging panel, displayed file content and other tagging options.</span></span> 
    
    ![평가 대 한 관련 태그 탭](media/c8acf891-b1cd-4344-816c-eabb8cbbe742.png)
  
2. <span data-ttu-id="da451-111">예제에서 각 파일을 검토 하 고 각 사례 문제에 대 한 파일의 관련성을 확인 하 고 태그 지정 **패널** 창에서 관련성 (R), 관련 없음 (veiligheid) 및 Skip 단추를 사용 하 여 파일에 태그가 지정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="da451-111">Review each file in the sample, determine the file's relevance for each case issue, and tag the file using the Relevance (R), Not relevant (NR) and Skip buttons in the **Tagging panel** pane.</span></span> 
    
    > [!NOTE]
    >  <span data-ttu-id="da451-p102">평가에는 500 태그가 지정 된 파일이 필요 합니다. 파일을 "생략" 하면 더 많은 파일을 태그로 받게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="da451-p102">Assessment requires 500 tagged files. If files are "skipped", you will receive more files to tag.</span></span> 
  
3. <span data-ttu-id="da451-114">샘플의 모든 파일에 태그를 지정 하 고 나면 **계산**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="da451-114">After tagging all files in the sample, click **Calculate**.</span></span> 
    
    <span data-ttu-id="da451-p103">평가 현재 오류 여백 및 다양성은 아래에 표시 된 것 처럼, 문제 당 세부 정보를 포함 하 여 **관련성 트랙** 탭에 계산 되어 표시 됩니다. 이 대화 상자에 대 한 자세한 내용은 뒷부분에 나오는 "평가 결과 검토" 섹션에 설명 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="da451-p103">The Assessment current error margin and richness are calculated and displayed in the **Relevance Track** tab, with expanded details per issue, as shown below. More details about this dialog are described in the later section "Reviewing Assessments results".</span></span> 
    
    ![관련 트랙-평가](media/da911ba5-8678-40d6-9ad5-fd0b058355c1.png)
  
    > [!TIP]
    > <span data-ttu-id="da451-p104">기본적으로 문제에 대 한 평가 진행률 표시기가 완료 되 고 평가 샘플이 검토 되었으며 적절 한 관련 파일에 태그가 지정 되었음을 나타내는 경우에는 기본 다음 단계로 진행 하는 것이 좋습니다. > 그렇지 않고 **추적** 탭 결과를 확인 하 고 오류 여백 및 다음 단계를 제어 하려면 **다음 단계**옆에 있는 **수정을** 클릭 하 고 **평가 계속**을 선택한 다음 **확인**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="da451-p104">By default, we recommend that you proceed to the default Next step when the Assessment progress indicator for the issue has completed, indicating that the assessment sample was reviewed and sufficient relevant files were tagged. > Otherwise, if you want to view the **Track** tab results and control the margin of error and the next step, click **Modify** adjacent to **Next Step**, select **Continue assessment**, and then click **OK**.</span></span> 
  
1. <span data-ttu-id="da451-p105">**평가** 확인란 오른쪽에 있는 **수정을** 클릭 하 여 문제 당 평가 매개 변수를 보고 지정 합니다. 다음 예와 같이 각 문제에 대 한 **평가 수준** 대화 상자가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="da451-p105">Click **Modify** to the right of the **Assessment** check box to view and specify assessment parameters per issue. An **Assessment level** dialog for each issue is displayed, as shown in the following example:</span></span> 
    
    ![평가 수준 사례 문제](media/b7113fef-d125-4617-ae1b-c9eb0bf79aec.png)
  
    <span data-ttu-id="da451-123">문제에 대해 다음 매개 변수가 계산 되어 **평가 수준** 대화 상자에 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="da451-123">The following parameters for the issue are calculated and displayed in the **Assessment level** dialog:</span></span> 
    
    <span data-ttu-id="da451-p106">**회수 예측에 대 한 대상 오류 여백**:이 값에 따라 검토에 필요한 추가 파일의 예상 개수가 계산 됩니다. 리콜에 사용 된 여백은 75%이 고 신뢰 수준이 95% 보다 큽니다.</span><span class="sxs-lookup"><span data-stu-id="da451-p106">**Target error margin for recall estimates**: Based on this value, the estimated number of additional files necessary to review is calculated. The margin used for recall is greater than 75% and with a 95% confidence level.</span></span> 
    
    <span data-ttu-id="da451-126">**추가 평가 파일 필요**: 현재 오류 여백의 요구 사항을 충족 하지 못한 경우 필요한 파일 수를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="da451-126">**Additional assessment files required**: Indicates how many more files are necessary if the current error margin's requirements have not been met.</span></span> 
    
2. <span data-ttu-id="da451-127">현재 오차 여백을 조정 하 고 각 문제에 대 한 다른 오류 여백의 영향을 확인 하려면 다음을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="da451-127">To adjust the current error margin and see the effect of different error margins (per issue):</span></span>
    
1. <span data-ttu-id="da451-128">**문제점 선택** 목록에서 문제를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="da451-128">In the **Select issue** list, select an issue.</span></span> 
    
2. <span data-ttu-id="da451-129">**회수 예측에 대 한 대상 오류 여백**에 새 값을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="da451-129">In **Target error margin for recall estimates**, enter a new value.</span></span>
    
3. <span data-ttu-id="da451-130">**값 업데이트** 를 클릭 하 여 조정에 대 한 영향을 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="da451-130">Click **Update values** to see the impact of the adjustments.</span></span> 
    
3. <span data-ttu-id="da451-131">**평가 수준** 대화 상자에서 **고급** 을 클릭 하 여 다음과 같은 추가 매개 변수 및 세부 정보를 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="da451-131">Click **Advanced** in the **Assessment level** dialog to see the following additional parameters and details:</span></span> 
    
    ![평가 수준 사례 문제를 상세하게 보기](media/577d7e0e-95df-48c2-9dec-bdeab5e801d8.png)
  
    <span data-ttu-id="da451-133">**예측 된 다양성**: 현재 평가 결과에 따라 예측 한 다양성</span><span class="sxs-lookup"><span data-stu-id="da451-133">**Estimated richness**: Estimated richness according to the current assessment results</span></span>
    
    <span data-ttu-id="da451-p107">**가정으로 회수**: 기본적으로 대상 오류 여백은 75% 위의 리콜에 적용 됩니다. 이 매개 변수를 변경 하 고 다른 회수 값 범위에서 오류 여백을 제어 하려면 **편집** 을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="da451-p107">**For assumed recall**: By default, the target error margin applies to recall above 75%. Click **Edit** if you want to change this parameter and control the margin of error on a different range of recall values.</span></span> 
    
    <span data-ttu-id="da451-p108">**신뢰 수준**: 기본적으로 신뢰도에 대 한 권장 오차 여백은 95%입니다. 이 매개 변수를 변경 하려면 **편집** 을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="da451-p108">**Confidence level**: By default, the recommended error margin for confidence is 95%. Click **Edit** if you want to change this parameter.</span></span> 
    
    <span data-ttu-id="da451-138">**예상 되는 오류 여백**: 업데이트 된 값이 제공 되 면, 모든 추가 평가 파일을 검토 한 후에는 풍부한 오류 여백이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="da451-138">**Expected richness error margin**: Given the updated values, this is the expected margin of error of the richness, after all additional assessment files are reviewed.</span></span>
    
    <span data-ttu-id="da451-139">**추가 평가 파일 필요**: 업데이트 된 값이 제공 되 면 대상에 도달 하기 위해 검토 해야 하는 추가 평가 파일의 수입니다.</span><span class="sxs-lookup"><span data-stu-id="da451-139">**Additional assessment files required**: Given the updated values, the number of additional assessment files that need to be reviewed to reach the target.</span></span>
    
    <span data-ttu-id="da451-140">**필요한 평가 파일 개수**: 검토에 필요한 총 평가 파일 및 업데이트 된 값이 제공 됩니다.</span><span class="sxs-lookup"><span data-stu-id="da451-140">**Total assessment files required**: Given the updated values, total assessment files required for review.</span></span>
    
    <span data-ttu-id="da451-141">**평가 중인 관련 파일의 예상 개수**: 업데이트 된 값이 주어 지 며, 모든 추가 평가 파일을 검토 한 후에 전체 평가에서 예상 되는 관련 파일의 수입니다.</span><span class="sxs-lookup"><span data-stu-id="da451-141">**Expected number of relevant files in assessment**: Given the updated values, the expected number of relevant files in the entire assessment after all additional assessment files are reviewed.</span></span>
    
4. <span data-ttu-id="da451-p109">매개 변수가 변경 되 면 **값 다시 계산**을 클릭 합니다. 작업이 완료 되 면 문제가 하나라도 발생 하면 **확인** 을 클릭 하 여 변경 내용을 저장 합니다 (또는 검토 하거나 수정 해야 하는 문제점이 여러 개 있는 경우에는 **다음** 에 **완료**).</span><span class="sxs-lookup"><span data-stu-id="da451-p109">Click **Recalculate values**, if parameters are changed. When you are done, if there is one issue, click **OK** to save the changes (or **Next** when there are multiple issues to review or modify and then **Finish**).</span></span> 
    
    <span data-ttu-id="da451-144">문제가 여러 개 있을 때 모든 문제가 검토 되거나 조정 되 면 다음 예제와 같이 **평가 수준: 요약** 대화 상자가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="da451-144">When there are multiple issues, after all issues have been reviewed or adjusted, an **Assessment level: summary** dialog is displayed, as shown in the following example.</span></span> 
    
    ![평가 수준 요약](media/4997b46d-10a5-4abc-b3b2-7b75a370eb9e.png)
  
    <span data-ttu-id="da451-146">평가가 성공적으로 완료 되 면 관련성 교육의 다음 단계로 진행 합니다.</span><span class="sxs-lookup"><span data-stu-id="da451-146">Upon successful completion of assessment, proceed to the next stage in Relevance training.</span></span>
    
## <a name="reviewing-assessment-results"></a><span data-ttu-id="da451-147">평가 결과 검토</span><span class="sxs-lookup"><span data-stu-id="da451-147">Reviewing assessment results</span></span>

<span data-ttu-id="da451-148">평가 샘플에 태그가 지정 되 면 평가 결과가 계산 되어 관련성 추적 탭에 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="da451-148">After an Assessment sample is tagged, the assessment results are calculated and displayed in the Relevance Track tab.</span></span>
  
<span data-ttu-id="da451-149">확장 된 트랙 표시에는 다음과 같은 결과가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="da451-149">The following results are displayed in the expanded Track display:</span></span> 
  
- <span data-ttu-id="da451-150">재호출 예측에 대 한 현재 오류 여백 평가</span><span class="sxs-lookup"><span data-stu-id="da451-150">Assessment current error margin for recall estimates</span></span>
    
- <span data-ttu-id="da451-151">예측 한 다양성</span><span class="sxs-lookup"><span data-stu-id="da451-151">Estimated richness</span></span>
    
- <span data-ttu-id="da451-152">추가 평가 파일 필요 (검토를 위해)</span><span class="sxs-lookup"><span data-stu-id="da451-152">Additional assessment files required (for review)</span></span>
    
<span data-ttu-id="da451-p110">평가 현재 오류 여백은 고급 eDiscovery에서 권장 하는 오류 여백입니다. "필요한 추가 평가 파일"에 표시 되는 번호는 해당 권장 사항에 해당 합니다.</span><span class="sxs-lookup"><span data-stu-id="da451-p110">The Assessment current error margin is the error margin recommended by Advanced eDiscovery. The number displayed for the "Additional assessment files required" corresponds to that recommendation.</span></span>
  
<span data-ttu-id="da451-p111">평가 진행률 표시기에는 현재 오류 여백이 지정 된 평가 완료 수준이 표시 됩니다. 평가가 진행 되 면 사용자는 다른 평가 샘플에 태그를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="da451-p111">The Assessment progress indicator shows the level of completion of the assessment, given the current error margin. When assessment is underway, the user will tag another assessment sample.</span></span>
  
<span data-ttu-id="da451-157">평가 진행률 표시기에서 평가가 완료 된 것으로 표시 되 면 평가 샘플 검토가 완료 되었으며 관련 파일에 태그가 지정 된 충분 합니다.</span><span class="sxs-lookup"><span data-stu-id="da451-157">When the assessment progress indicator shows assessment as complete, that means the assessment sample review was completed and sufficient relevant files were tagged.</span></span> 
  
<span data-ttu-id="da451-158">확장 된 트랙 표시에는 다음 단계, 평가 통계 및 자세한 결과 액세스에 대 한 권장 정보가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="da451-158">The expanded Track display shows the recommended next step, the assessment statistics, and access to detailed results.</span></span>
  
<span data-ttu-id="da451-p112">다양성을 아주 적게 사용할 경우 유용한 통계를 생성 하기 위해 최소한의 관련 파일에 연결 하는 데 필요한 추가 평가 파일의 수는 매우 높습니다. 고급 eDiscovery는 교육으로 이동 하는 것이 좋습니다. 평가 진행률 표시기는 회색으로 표시 되며 통계를 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="da451-p112">When richness is very low, the number of additional assessment files needed to reach a minimal number of relevant files to produce useful statistics is very high. Advanced eDiscovery will then recommend moving on to training. The assessment progress indicator will be shaded, and no statistics will be available.</span></span> 
  
<span data-ttu-id="da451-p113">통계적으로 기반 하는 안정화가 없으면 더 낮은 수준의 정확성과 신뢰 수준이 적용 됩니다. 그러나 찾은 관련 파일의 비율을 알 필요가 없는 경우 이러한 결과를 사용 하 여 관련 파일을 찾을 수 있습니다. 마찬가지로이 상태를 사용 하 여 특정 문제와 관련 된 파일에 대 한 액세스를 가속화 하는 낮은 다양성의 문제를 교육할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="da451-p113">In the absence of statistically based stabilization, there will be results with a lower level of accuracy and confidence level. However, these results can be used to find relevant files when you do not need to know the percentage of relevant files found. Similarly, this status can be used to train issues with low richness, where Relevance scores can accelerate access to files relevant to a specific issue.</span></span>
  
> [!TIP]
> <span data-ttu-id="da451-p114">\*\* \> 관련성 트랙\*\* 탭에 확장 된 문제가 표시 되 면 다음 보기 옵션을 사용할 수 있습니다. 다음 단계를 > (문제 당) **태그** 를 무시할 수 있습니다. \*\*\*\* 오른쪽으로 이동 하 고 **다음 단계**에서 다른 단계를 선택 합니다. 평가 진행률 표시기가 완료 되지 않은 경우 평가는 다음 옵션을 통해 더 많은 평가 파일에 태그를 추가 하 고 통계 정확성을 높이는 것이 좋습니다. > **수정을**클릭 하 고, **평가 수준 대화 상자**에서 **회수 예측에 대 한 대상 오류 여백을**변경 하 고 **값 업데이트**를 클릭 하 여 오류 여백을 변경 하 고 해당 영향을 평가할 수 있습니다. 또한이 대화 상자에서 고급을 클릭 하 여 고급 옵션을 볼 \*\*\*\* 수 있습니다. > **보기**를 클릭 하 여 추가 평가 수준 통계 및 해당 영향을 볼 수 있습니다. 표시 된 세부 결과 대화 상자에서 최소 500 태그가 지정 된 평가 파일이 있고 최소 18 개 파일에 문제에 대 한 태그가 지정 된 경우 문제 당 통계를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="da451-p114">In the **Relevance \> Track** tab, expanded issue display, the following viewing options are available: > The recommended next step, such as **Next step: Tagging** can be bypassed (per issue) by clicking the **Modify** button to its right, and then selecting an different step in the **Next step**. When the assessment progress indicator has not completed, assessment will be the next recommended option, to tag more assessment files and increase statistics accuracy. > You can change the error margin and assess its impact, by clicking **Modify**, and in the **Assessment level dialog**, changing the **Target error margin for recall estimates**, and clicking **Update values**. Also, in this dialog, you can view advanced options, by clicking **Advanced**. > You can view additional assessment level statistics and their impact by clicking **View**. In the displayed Detail results dialog, statistics are available per issue, when there are at least 500 tagged assessment files and at least 18 files are tagged as Relevant for the issue.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="da451-171">참고 항목</span><span class="sxs-lookup"><span data-stu-id="da451-171">See also</span></span>

[<span data-ttu-id="da451-172">Office 365 Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="da451-172">Office 365 Advanced eDiscovery</span></span>](office-365-advanced-ediscovery.md)
  
[<span data-ttu-id="da451-173">관련성 평가 이해</span><span class="sxs-lookup"><span data-stu-id="da451-173">Understanding Assessment in Relevance</span></span>](assessment-in-relevance-in-advanced-ediscovery.md)
  
[<span data-ttu-id="da451-174">태그 지정 및 관련성 교육</span><span class="sxs-lookup"><span data-stu-id="da451-174">Tagging and Relevance training</span></span>](tagging-and-relevance-training-in-advanced-ediscovery.md)
  
[<span data-ttu-id="da451-175">관련성 분석 추적</span><span class="sxs-lookup"><span data-stu-id="da451-175">Tracking Relevance analysis</span></span>](track-relevance-analysis-in-advanced-ediscovery.md)
  
[<span data-ttu-id="da451-176">결과를 기준으로 결정</span><span class="sxs-lookup"><span data-stu-id="da451-176">Deciding based on the results</span></span>](decision-based-on-the-results-in-advanced-ediscovery.md)
  
[<span data-ttu-id="da451-177">관련성 분석 테스트</span><span class="sxs-lookup"><span data-stu-id="da451-177">Testing Relevance analysis</span></span>](test-relevance-analysis-in-advanced-ediscovery.md)

