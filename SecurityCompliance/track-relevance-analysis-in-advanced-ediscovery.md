---
title: Office 365 Advanced eDiscovery에서 관련성 분석 추적
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
ms.assetid: 3ab1e2c3-28cf-4bf5-b0a8-c0222f32bdf5
description: '보기 및 관련성 교육 상태 및 Office 365 고급 ediscovery에서 사례 문제에 대 한 결과 해석 하는 방법에 알아봅니다.  '
ms.openlocfilehash: a19f7eaabf5dc15eefaa7209ded8261020d0d557
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22534153"
---
# <a name="track-relevance-analysis-in-office-365-advanced-ediscovery"></a><span data-ttu-id="4f951-103">Office 365 Advanced eDiscovery에서 관련성 분석 추적</span><span class="sxs-lookup"><span data-stu-id="4f951-103">Track Relevance analysis in Office 365 Advanced eDiscovery</span></span>

> [!NOTE]
> <span data-ttu-id="4f951-p101">고급 eDiscovery 조직에 대 한 고급 준수 추가 기능 또는 e 5 구독은 Office 365 E3 필요합니다. 해당 요금제에 가입한 상태 고급 eDiscovery 시도 하려는 하지 경우에 [Office 365 Enterprise e 5의 평가판 등록](https://go.microsoft.com/fwlink/p/?LinkID=698279)할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4f951-p101">Advanced eDiscovery requires an Office 365 E3 with the Advanced Compliance add-on or an E5 subscription for your organization. If you don't have that plan and want to try Advanced eDiscovery, you can [sign up for a trial of Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span></span> 
  
<span data-ttu-id="4f951-106">고급 eDiscovery 관련성 추적 탭의 표시 하는 태그 탭에서 수행 하 고 관련성 교육의 계산 된 유효성을 검사 하 고 관련성에 반복적인 교육 프로세스를 수행 하려면 다음 단계를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="4f951-106">In Advanced eDiscovery, the Relevance Track tab displays the calculated validity of the Relevance training performed in the Tag tab and indicates the next step to take in the iterative training process in Relevance.</span></span> 
  
## <a name="tracking-relevance-training-status"></a><span data-ttu-id="4f951-107">관련성 교육 상태를 추적합니다.</span><span class="sxs-lookup"><span data-stu-id="4f951-107">Tracking Relevance training status</span></span>

1. <span data-ttu-id="4f951-108">아래 **문제 이름** 대화 상자의 다음 예에서 같이 사례 문제에 대 한 관련성 추적에 다음 정보를 봅니다.</span><span class="sxs-lookup"><span data-stu-id="4f951-108">View the following details in Relevance Track for the case issues, as shown in the following example of an **Issue name** dialog below.</span></span> 
    
  - <span data-ttu-id="4f951-p102">**평가**:이 진행률 표시기가이 이때 하기 위해 수행 교육 관련성 오차는 측면에서 평가 대상이 달성 정도를 표시 합니다. 다양 한 관련성 교육 결과 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4f951-p102">**Assessment**: This progress indicator shows to what degree the Relevance training performed to this point has achieved the assessment target in terms of margin of error. The richness of the Relevance training results is also displayed.</span></span> 
    
  - <span data-ttu-id="4f951-p103">**교육**: 관련성 교육 결과 안정성 및 각 문제에 대 한 관련성 교육 샘플 수를 표시 하는 숫자 배율과 태그가 지정 된이 색으로 구분 된 진행률 표시기 및 도구 설명 표시를 나타냅니다. 전문가 반복적인 관련성 교육 프로세스의 진행 상황을 모니터링합니다.</span><span class="sxs-lookup"><span data-stu-id="4f951-p103">**Training**: This color-coded progress indicator and tool-tip display indicates the Relevance training results stability and a numeric scale showing the number of Relevance training samples tagged for each issue. The expert monitors the progress of the iterative Relevance training process.</span></span> 
    
  - <span data-ttu-id="4f951-113">**일괄 처리 계산**:이 진행률 표시기 계산 일괄 처리를 완료 하는 방법에 대 한 정보를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="4f951-113">**Batch calculation**: This progress indicator provides information about the completion of Batch calculation.</span></span>
    
  - <span data-ttu-id="4f951-114">**다음 단계**: 수행 하려면 다음 단계에 대 한 권장을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="4f951-114">**Next step**: Displays the recommendation for the next step to be performed.</span></span> 
    
    <span data-ttu-id="4f951-p104">이 예제에서는 완료 된 색 진행률 표시기와는 확인 표시가 표시에 지정 된 문제에 대 한 성공적으로 완료 된 평가 표시 됩니다. 태그 지정 진행 되 고, 이지만 대/소문자 여전히 불안정 한 것으로 간주 됩니다 (안정성 상태 도구 설명에도 표시). 다음 단계 권장은 "교육을 진행" 합니다.</span><span class="sxs-lookup"><span data-stu-id="4f951-p104">In the example, a successfully completed Assessment for an issue is shown, indicated by the completed color progress indicator and the checkmark. Tagging is underway, but the case is still considered unstable (stability status also shown in a tool-tip). The next step recommendation is "Training".</span></span> 
    
    ![관련 트랙 훈련 1 단계](media/a00fe607-680a-48eb-9d61-4565319f7ab6.png)
  
    <span data-ttu-id="4f951-p105">확장 된 보기 옵션 및 추가 정보를 표시합니다. 현재 표시 된 오류 여백을 기존 (이미 태그가 지정 된) 평가 파일을 지정 된 평가의 현재 상태에서 회수의 오류 여백입니다.</span><span class="sxs-lookup"><span data-stu-id="4f951-p105">The expanded view displays additional information and options. The displayed current error margin is the error margin of the recall in the current state of assessment, given the existing (already tagged) assessment files.</span></span>
    
    > [!NOTE]
    >  <span data-ttu-id="4f951-p106">문제 및 다음 "모든 문제"에 대 한 **평가** 확인란 선택을 취소 하 여 평가 단계를 무시할 수 있습니다. 그러나 결과적으로, 됩니다이 문제에 대 한 통계 없습니다. > **평가** 확인란의 선택을 취소만 가능 평가 수행 하기 전에 합니다. 각 문제에 대 한 확인란의 선택을 취소 하는 경우에 평가 사용 하지 않을 경우에 여러 문제가 존재 하는 경우</span><span class="sxs-lookup"><span data-stu-id="4f951-p106">The Assessment stage can be bypassed by clearing the **Assessment** check box per issue and then for "all issues". However, as a result, there will be no statistics for this issue. > Clearing the **Assessment** check box can only be done before assessment is performed. Where multiple issues exist in a case, assessment is bypassed only if the check box is cleared for each issue</span></span> 
  
    <span data-ttu-id="4f951-125">평가와 완료 되지 않으면 첫번째 예제 파일의 설정, 평가 더 많은 파일 태그 지정을 위한 다음 단계를 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4f951-125">When assessment is not completed with the first sample set of files, assessment might be the next step for tagging more files.</span></span> 
    
    <span data-ttu-id="4f951-p107">**관련성** 에 \> **추적**, 교육 진행률 표시기 및 도구 설명의 안정성과 도달 하기 위해 필요한 추가 샘플 예상된 번호를 표시 합니다. 이 예상 필요한 추가 교육에 대 한 지침을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="4f951-p107">In **Relevance** \> **Track**, the training progress indicator and tool-tip indicate the estimated number of additional samples needed to reach stability. This estimate provides a guideline for the additional training needed.</span></span>
    
    ![관련 트랙 훈련](media/98dbc3f5-5238-4d73-9f88-1aa4d77ea729.png)
  
2. <span data-ttu-id="4f951-p108">완료 태그 지정 및 교육을 계속 해야하는 경우 **교육**을 클릭 합니다. 추가 교육에 대 한 설정 로드 된 파일에서 다른 샘플 파일 집합이 생성 됩니다. 다음 태그를 지정 하 고 더 많은 파일 교육을 태그 탭으로 돌아갑니다.</span><span class="sxs-lookup"><span data-stu-id="4f951-p108">When you're done tagging and if you need to continue training, click **Training**. Another sample set of files is generated from the loaded file set for additional training. You are then returned to the Tag tab to tag and train more files.</span></span>
    
### <a name="reaching-stable-training-levels"></a><span data-ttu-id="4f951-132">안정적인 교육 수준에 도달할 때</span><span class="sxs-lookup"><span data-stu-id="4f951-132">Reaching stable training levels</span></span>

<span data-ttu-id="4f951-133">평가 파일 교육 안정적인 수준 권한을 획득 한가, 고급 eDiscovery 일괄 처리 계산 준비가 된 것입니다.</span><span class="sxs-lookup"><span data-stu-id="4f951-133">After the assessment files have attained a stable level of training, Advanced eDiscovery is ready for Batch calculation.</span></span>
  
> [!NOTE]
> <span data-ttu-id="4f951-p109">일반적으로 교육 예제 (영문), 안정적인 3 후 다음 단계는 "일괄 처리 계산" 합니다. 있을 수 있습니다 예외 등 이전 샘플 또는 시드 파일 작업을 추가한에서 파일을 태그 지정을 변경 하는 경우에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4f951-p109">Usually, after three stable training samples, the next step is "Batch calculation". There may be exceptions, for example, when there were changes to the tagging of files from earlier samples or when seed files were added.</span></span> 
  
### <a name="performing-batch-calculation"></a><span data-ttu-id="4f951-136">일괄 처리 계산을 수행합니다.</span><span class="sxs-lookup"><span data-stu-id="4f951-136">Performing Batch calculation</span></span>

<span data-ttu-id="4f951-137">(경우 안정적인 교육 상태 확인 표시가 표시 및 도구 설명에 안정 상태 진행률 표시줄에 표시 됩니다.) 교육 성공적으로 완료 한 후 다음 단계에서는으로 실행 되는 일괄 처리 계산 파일의 관련성을 평가 하 고 관련성 점수를 할당 하려면 파일 전체 모집단을 관련성 교육 과정에서 얻은 정보를 적용 하는 일괄 처리 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="4f951-137">Batch calculation is executed as the next step after training is successfully completed (when a stable training status is shown by the progress bar, a checkmark and stable status in the tool-tip.) Batch calculation applies the knowledge acquired during the Relevance training to the entire file population, to assess the files' relevance and to assign Relevance scores.</span></span>
  
<span data-ttu-id="4f951-p110">둘 이상의 문제가 있을 때 일괄 처리 계산 문제 당 수행 됩니다. 일괄 처리 계산 하는 동안 모든 파일을 처리 하는 동안 진행 상황 모니터링 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4f951-p110">When there is more than one issue, Batch calculation is done per issue. During Batch calculation, progress is monitored while processing all of the files.</span></span> 
  
<span data-ttu-id="4f951-p111">여기에 권장 되는 다음 단계는 "None"으로,이 시점 없는 추가 반복적인 관련성 교육 있으면 필요한 것입니다. 다음 단계는는 **관련성 \> 판단** 탭 합니다.</span><span class="sxs-lookup"><span data-stu-id="4f951-p111">Here, the recommended next step is "None", which indicates that no additional iterative Relevance training is required at this point. The next phase is the **Relevance \> Decide** tab.</span></span> 
  
<span data-ttu-id="4f951-142">일괄 처리 계산 후 새 파일을 가져오려는 경우 관리자가 새 부하를 가져온된 파일을 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4f951-142">If you want to import new files after Batch calculation, the administrator can add the imported files to a new load.</span></span>
  
> [!NOTE]
> <span data-ttu-id="4f951-p112">일괄 처리 계산 하는 동안 **취소** 를 클릭 하는 프로세스 저장 하는 이미 실행 되었습니다. 일괄 처리 계산 다시를 실행 하는 경우 마지막 실행 된 지점에서 프로세스가 계속 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4f951-p112">If you click **Cancel** during Batch calculation, the process saves what was already executed. If you run Batch calculation again, the process will continue from the last executed point.</span></span> 
  
### <a name="assessing-tagging-consistency"></a><span data-ttu-id="4f951-145">태그 지정 일관성 평가</span><span class="sxs-lookup"><span data-stu-id="4f951-145">Assessing tagging consistency</span></span>

<span data-ttu-id="4f951-p113">파일에 태그 지정에 불일치가 있으면 분석에 영향을 줄 수 있습니다. 일관성 프로세스에 태그를 지정 하는 고급 eDiscovery 결과 최적의 중이거나 의심 스러운에서 일관성은 때 사용할 수 있습니다. 가능한 일관성 없이 태그가 지정 된 파일의 목록이 반환 되 면 하 고를 검토 하 고 다시 태그가 지정 된, 필요에 따라 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4f951-p113">If there are inconsistencies in file tagging, it can affect the analysis. The Advanced eDiscovery tagging consistency process can be used when results are not optimal or consistency is in doubt. A list of possible inconsistently tagged files is returned, and they can be reviewed and re-tagged, as necessary.</span></span>
  
> [!NOTE]
> <span data-ttu-id="4f951-p114">**관련성** 에서 일관성에 태그를 지정 하는 다음과 같은 평가 볼 수 있습니다는 7 개 이상의 교육 라운드 후 \> **추적** \> **문제** \> **자세한 결과** \> **교육 진행**합니다. 이 검토는 한번에 하나의 문제에 대 한 수행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4f951-p114">After seven or more training rounds following assessment, tagging consistency can be viewed in **Relevance** \> **Track** \> **Issue** \> **Detailed results** \> **Training progress**. This review is done for one issue at a time.</span></span> 
  
1. <span data-ttu-id="4f951-151">**관련성 \> 추적**, 문제의 행을 확장 합니다.</span><span class="sxs-lookup"><span data-stu-id="4f951-151">In **Relevance \> Track**, expand an issue's row.</span></span>
    
2. <span data-ttu-id="4f951-152">**다음 단계**오른쪽에 **수정**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="4f951-152">To the right of **Next step**, click **Modify**.</span></span>
    
3. <span data-ttu-id="4f951-153">7 교육 예제 (영문) 한 후 **다음 단계** 옵션으로 **태그 불일치 항목** 을 선택 하 고 **확인**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="4f951-153">Select **Tag inconsistencies** as the **Next step** option, after seven training samples and click **OK**.</span></span>
    
4. <span data-ttu-id="4f951-p115">**태그 불일치 항목**을 선택 합니다. **태그** 탭 다시 필요에 따라 태그 지정 불일치 항목의 목록을 표시 (영문)이 열립니다.</span><span class="sxs-lookup"><span data-stu-id="4f951-p115">Select **Tag inconsistencies**. The **Tag** tab opens displaying a list of the inconsistencies to re-tag as necessary.</span></span> 
    
5. <span data-ttu-id="4f951-p116">**계산** 변경 내용을 전송 하기를 클릭 합니다. 불일치 항목에 태그 지정 후 다음 단계는 "교육을 진행" 합니다.</span><span class="sxs-lookup"><span data-stu-id="4f951-p116">Click **Calculate** to submit the changes. The next step after tagging inconsistencies is "Training".</span></span> 
    
## <a name="viewing-and-using-relevance-results"></a><span data-ttu-id="4f951-158">보기 및 관련성 결과 사용 하 여</span><span class="sxs-lookup"><span data-stu-id="4f951-158">Viewing and using Relevance results</span></span>

<span data-ttu-id="4f951-p117">**관련성 \> 추적** 탭 문제가 행을 확장 하 고 **자세한 결과**얻으려면 옆에 있는 **보기**를 클릭 합니다. 자세한 결과 창 되어 표시,으로 표시 된 아래에서 설명한 것입니다.</span><span class="sxs-lookup"><span data-stu-id="4f951-p117">In the **Relevance \> Track** tab, expand an issue's row, and next to **Detailed results**, click **View**. The Detailed results panes are displayed, as shown and described below.</span></span>
  
![자세한 결과 교육 하는 관련성](media/495c04a9-ed1e-4355-8cab-c14270ca2bbb.png)
  
### <a name="tagging-summary"></a><span data-ttu-id="4f951-162">요약에 태그 지정</span><span class="sxs-lookup"><span data-stu-id="4f951-162">Tagging summary</span></span>

 <span data-ttu-id="4f951-163">아래에 표시 된 예제에서는 **태그 요약** 각 평가, 교육 및 프로세스에 태그를 지정 하는 따라잡기 파일에 대 한 합계를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="4f951-163">In the example shown below, the **Tagging summary** displays totals for each of Assessment, Training, and Catch-up file tagging processes.</span></span> 
  
![관련성 추적 태그 요약](media/0ec906fc-bc84-4245-a964-fb3ca37891db.png)
  
### <a name="keywords"></a><span data-ttu-id="4f951-165">키워드</span><span class="sxs-lookup"><span data-stu-id="4f951-165">Keywords</span></span>

<span data-ttu-id="4f951-p118">키워드 고유 문자열, 단어, 구문 또는 고급 eDiscovery 하 여 파일을 관련이 있는지 여부에 대 한 중요 한 표시기로 식별 되는 파일에 있는 단어의 순서입니다. "포함" 열 키워드와 관련 됨,으로 태그가 지정 된 파일에는 가중치를 나열 하 고 키워드 및 Not으로 태그가 지정 된 파일에는 가중치를 나열 하는 "제외" 열 관련 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4f951-p118">A keyword is a unique string, word, phrase, or sequence of words in a file identified by Advanced eDiscovery as a significant indicator of whether a file is relevant. The "Include" columns list keyword and weights in files tagged as Relevant, and the "Exclude" columns lists keywords and weights in files tagged as Not relevant.</span></span>
  
<span data-ttu-id="4f951-p119">고급 eDiscovery 양수 또는 음수 키워드 가중치 값을 할당합니다. 클수록 가중치, 키워드 표시 되는 파일 일괄 처리 계산 하는 동안 관련성 점수가 높은 할당 되어있는지 많을 수록 가능성 합니다.</span><span class="sxs-lookup"><span data-stu-id="4f951-p119">Advanced eDiscovery assigns negative or positive keyword weight values. The higher the weight, the higher the likelihood that a file in which the keyword appears is assigned a higher Relevance score during Batch calculation.</span></span> 
  
<span data-ttu-id="4f951-170">키워드의 고급 eDiscovery 목록 전문가가 또는 간접 온전성 검사도 작성 되는 목록을 보완 하기 위해 사용할 수는 파일의 모든 위치에서 프로세스를 검토 합니다.</span><span class="sxs-lookup"><span data-stu-id="4f951-170">The Advanced eDiscovery list of keywords can be used to supplement a list built by an expert or as an indirect sanity check at any point in the file review process.</span></span>
  
### <a name="training-progress"></a><span data-ttu-id="4f951-171">교육 진행</span><span class="sxs-lookup"><span data-stu-id="4f951-171">Training progress</span></span>

<span data-ttu-id="4f951-172">**교육 진행** 창 아래 예제와 같이 교육 진행 그래프 및 품질 표시기 표시 되는 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="4f951-172">The **Training Progress** pane includes a training progress graph and quality indicator display, as shown in the example below.</span></span> 
  
![관련 교육 진행 상황 관리](media/8a5089f5-a162-4246-ae09-bc1921859860.png)
  
 <span data-ttu-id="4f951-174">**품질 표시기 교육**: 태그 지정 일관성의 등급을 다음과 같이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4f951-174">**Training quality indicator**: Displays the rating of the tagging consistency as follows:</span></span>
  
- <span data-ttu-id="4f951-p120">**좋은**: 파일 일관 되 게 태그가 지정 됩니다. (녹색 밝게 표시)</span><span class="sxs-lookup"><span data-stu-id="4f951-p120">**Good**: Files are tagged consistently. (Green light displayed)</span></span>
    
- <span data-ttu-id="4f951-p121">**중간**: 일부 파일을 일관성 없이 태그가 지정 될 수 있습니다. (노란색 밝게 표시 됨)</span><span class="sxs-lookup"><span data-stu-id="4f951-p121">**Medium**: Some files may be tagged inconsistently. (Yellow light displayed)</span></span>
    
- <span data-ttu-id="4f951-p122">**경고**: 많은 파일은 일관성 없이 태그 처리 될 수 있습니다. (빨간색 표시등이 표시)</span><span class="sxs-lookup"><span data-stu-id="4f951-p122">**Warning**: Many files may be tagged inconsistently. (Red light displayed)</span></span>
    
 <span data-ttu-id="4f951-p123">**진행률 그래프 교육**: F 측정 값에 비해 관련성 교육 주기 횟수 후 관련성 교육 안정성의 정도 표시 합니다. 전체 신뢰 구간 좁힐 그래프에서 왼쪽에서 오른쪽으로 이동 하 고 함께 사용 하는 F-조치 고급 eDiscovery 관련성 안정성 확인 하 여 관련성 교육 결과 때 최적화 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4f951-p123">**Training progress graph**: Shows the degree of Relevance training stability after a number of Relevance training cycles in comparison to the F-measure value. As we move from the left to the right across the graph, the confidence interval narrows and is used, along with the F-measure, by Advanced eDiscovery Relevance to determine stability when the Relevance training results are optimized.</span></span>
  
> [!NOTE]
> <span data-ttu-id="4f951-p124">관련성 f2 키를 회수 정밀도로 배의 가중치를 수신 하는 위치는 F 측정 메트릭을 사용 합니다. 사례에 대 한 높은 다양성 (넘는: 25%), 관련성 사용 하 여 F1 함께 (1:1 비율로). **관련성 설치 프로그램** 에서 F 측정 비율을 구성할 수 있습니다 \> **고급 설정**합니다.</span><span class="sxs-lookup"><span data-stu-id="4f951-p124">Relevance uses F2, an F-measure metric where Recall receives twice as much weight as Precision. For cases with high richness (over 25%), Relevance uses F1 (1:1 ratio). The F-measure ratio can be configured in **Relevance setup** \> **Advanced settings**.</span></span> 
  
### <a name="batch-calculation-results"></a><span data-ttu-id="4f951-186">일괄 처리 계산 결과</span><span class="sxs-lookup"><span data-stu-id="4f951-186">Batch calculation results</span></span>

<span data-ttu-id="4f951-187">**일괄 처리 계산 결과** 창에 다음과 같은 관련성을 획득 하는 파일의 수에 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4f951-187">The **Batch calculation results** pane includes the number of files that were scored for Relevance, as follows:</span></span> 
  
- <span data-ttu-id="4f951-188">**Success**</span><span class="sxs-lookup"><span data-stu-id="4f951-188">**Success**</span></span>
    
- <span data-ttu-id="4f951-189">**빈**: 텍스트가 없는, 등 유일한 공백을/탭</span><span class="sxs-lookup"><span data-stu-id="4f951-189">**Empty**: Contains no text, for example, only spaces/tabs</span></span>
    
- <span data-ttu-id="4f951-190">**실패**: 과도 한 크기 때문에 읽을 수 없는 또는</span><span class="sxs-lookup"><span data-stu-id="4f951-190">**Failed**: Due to excessive size or could not be read</span></span>
    
- <span data-ttu-id="4f951-191">**Ignored**: 과도 한 크기 때문에</span><span class="sxs-lookup"><span data-stu-id="4f951-191">**Ignored**: Due to excessive size</span></span>
    
- <span data-ttu-id="4f951-192">**Nebulous**: 의미 없는 텍스트일 또는 사용 가능한 기능 문제와 관련 된 포함</span><span class="sxs-lookup"><span data-stu-id="4f951-192">**Nebulous**: Contains meaningless text or no features relevant to the issue</span></span>
    
> [!NOTE]
> <span data-ttu-id="4f951-193">비어 있는 경우 실패, Ignored, 또는 Nebulous 받습니다 관련성 점수는-1입니다.</span><span class="sxs-lookup"><span data-stu-id="4f951-193">Empty, Failed, Ignored, or Nebulous will receive a Relevance score of -1.</span></span> 
  
### <a name="training-statistics"></a><span data-ttu-id="4f951-194">교육 통계</span><span class="sxs-lookup"><span data-stu-id="4f951-194">Training statistics</span></span>

<span data-ttu-id="4f951-195">통계 및 고급 eDiscovery 관련성 교육에서 결과에 따라 그래프를 표시 하는 **교육 통계** 창입니다.</span><span class="sxs-lookup"><span data-stu-id="4f951-195">The **Training statistics** pane displays statistics and graphs based on results from Advanced eDiscovery Relevance training.</span></span> 
  
![관련 트랙 교육 통계](media/9a07740e-20d3-49fb-b9b9-84265e0a1836.png)
  
<span data-ttu-id="4f951-197">이 보기에 표시</span><span class="sxs-lookup"><span data-stu-id="4f951-197">This view shows the following:</span></span>
  
- <span data-ttu-id="4f951-p125">**검토 회수 비율**: 관련성에 따라 결과의 비교에 구성원이 선형 검토를 얻었습니다. 회수 검토 집합 크기 집합 주어진 예상 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4f951-p125">**Review-recall ratio**: Comparison of results according to Relevance scores in a hypothetically linear review. Recall is estimated given the review set size set.</span></span>
    
- <span data-ttu-id="4f951-200">**매개 변수**: 누적 전체 대/소문자에 대 한 파일 모집단 관계에서 설정 검토와 관련 된 통계를 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="4f951-200">**Parameters**: Cumulative calculated statistics pertaining to the review set in relation to the file population for the entire case.</span></span>
    
- <span data-ttu-id="4f951-201">**검토**:이 실시간 구분에 검토 하려면 파일의 백분율을 기준으로 합니다.</span><span class="sxs-lookup"><span data-stu-id="4f951-201">**Review**: Percentage of files to review based on this cutoff.</span></span>
    
- <span data-ttu-id="4f951-202">**회수**: 검토 집합에서 파일을 다음과 관련 됨의 비율입니다.</span><span class="sxs-lookup"><span data-stu-id="4f951-202">**Recall**: Percentage of Relevant files in the review set.</span></span> 
    
- <span data-ttu-id="4f951-p126">**관련성 점수 하 여 배포**: 마감 점수 미만 왼쪽에 진한 회색 디스플레이 있는 파일입니다. 총 파일 관계에서 설정 검토 파일 관련성 점수 및 파일의 관련된 백분율을 표시 하는 도구 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="4f951-p126">**Distribution by relevance score**: Files in the dark gray display to the left are below the cutoff score. A tool-tip displays the Relevance score and the related percentage of files in the review file set in relation to the total files.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4f951-205">참고 항목</span><span class="sxs-lookup"><span data-stu-id="4f951-205">See also</span></span>

[<span data-ttu-id="4f951-206">Office 365 Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="4f951-206">Office 365 Advanced eDiscovery</span></span>](office-365-advanced-ediscovery.md)
  
[<span data-ttu-id="4f951-207">관련성에 이해 평가</span><span class="sxs-lookup"><span data-stu-id="4f951-207">Understanding Assessment in Relevance</span></span>](assessment-in-relevance-in-advanced-ediscovery.md)
  
[<span data-ttu-id="4f951-208">수행 하 고 평가 검토 합니다.</span><span class="sxs-lookup"><span data-stu-id="4f951-208">Performing and reviewing Assessment</span></span>](tagging-and-assessment-in-advanced-ediscovery.md)
  
[<span data-ttu-id="4f951-209">관련성 교육을 수행합니다.</span><span class="sxs-lookup"><span data-stu-id="4f951-209">Performing Relevance training</span></span>](tagging-and-relevance-training-in-advanced-ediscovery.md)
  
[<span data-ttu-id="4f951-210">결과에 따라 결정</span><span class="sxs-lookup"><span data-stu-id="4f951-210">Making decisions based on the results</span></span>](decision-based-on-the-results-in-advanced-ediscovery.md)
  
[<span data-ttu-id="4f951-211">관련성 분석 테스트</span><span class="sxs-lookup"><span data-stu-id="4f951-211">Testing Relevance analysis</span></span>](test-relevance-analysis-in-advanced-ediscovery.md)

