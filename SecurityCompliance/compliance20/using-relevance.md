---
title: 관련성 모듈을 사용 하 여 Advanced eDiscovery에서 데이터 분석
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: ''
ms.openlocfilehash: ae0546edbc9cb95808ba1843f835eab7dc460f0b
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/17/2019
ms.locfileid: "34151500"
---
# <a name="use-the-relevance-module-to-analyze-data-in-advanced-ediscovery"></a><span data-ttu-id="31b06-102">관련성 모듈을 사용 하 여 Advanced eDiscovery에서 데이터 분석</span><span class="sxs-lookup"><span data-stu-id="31b06-102">Use the Relevance module to analyze data in Advanced eDiscovery</span></span>

<span data-ttu-id="31b06-103">고급 eDiscovery에서 관련성 모듈에는 사례와 관련 된 파일의 관련성 교육과 검토가 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="31b06-103">In Advanced eDiscovery, the Relevance module includes the Relevance training and review of files related to a case.</span></span> <span data-ttu-id="31b06-104">관련성 워크플로를 사용 하려면 검토 집합 내에서 검토 설정 관리로 이동 하 여 관련성 표시를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="31b06-104">In order to use the Relevance workflow, go to Manage review set within a review set and click on Show Relevance.</span></span> <span data-ttu-id="31b06-105">워크플로를 시작 하려면 몇 가지 단계를 완료 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="31b06-105">There are a couple of steps you need to complete before you can start the workflow:</span></span>

- <span data-ttu-id="31b06-106">프로세스: 검토 집합에 추가 된 각 부하 집합은 여기에 "컨테이너"로 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="31b06-106">Process: each load set added to the review set will show up as a "container" here.</span></span> <span data-ttu-id="31b06-107">이러한 문서를 관련성이 있는 모듈에 추가 하려면 먼저 처리 해야 합니다. 또한 특정 문제에 대해 미리 태그가 지정 되거나 시드로 표시할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="31b06-107">You need to process these documents before you can add them to Relevance module; this is also where you can mark them as seed or pre-tagged for a specific issue.</span></span>

- <span data-ttu-id="31b06-108">관련성에 추가: 관련성 \> 부하에서 처리 된 문서를 교육에 사용할 수 있도록 해당 항목을 추가할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="31b06-108">Add to Relevance: Under Relevance \> Loads, you can add documents that have been processed to Relevance to make them available for training.</span></span>

<span data-ttu-id="31b06-109">관련성 워크플로는 다음과 같이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="31b06-109">The Relevance workflow is shown and described as follows:</span></span>
  
![관련성 워크플로](../media/44c67dd2-7a20-40a9-b0ed-784364845c77.gif)
  
- <span data-ttu-id="31b06-111">**평가 및 추적 주기**:</span><span class="sxs-lookup"><span data-stu-id="31b06-111">**Cycles of assessment and tracking**:</span></span>
    
  - <span data-ttu-id="31b06-112">**평가**: 무작위 파일 샘플을 기반으로 초기 평가를 사용 하도록 설정 하 고이 평가를 통해 예측 코딩 프로세스의 성능을 결정 하는 결정을 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="31b06-112">**Assessment**: Enables early assessment based on a random sample of files and uses this assessment to apply decisions to determine the performance of the predictive coding process.</span></span> 
    
  - <span data-ttu-id="31b06-113">**트랙**: 프로세스의 통계 유효성을 모니터링 하는 동안 평가의 중간 결과를 계산 하 고 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="31b06-113">**Track**: Calculate and display interim results of the assessment while monitoring statistical validity of the process.</span></span> 
    
- <span data-ttu-id="31b06-114">**교육 주기 및 추적**</span><span class="sxs-lookup"><span data-stu-id="31b06-114">**Cycles of training and tracking**</span></span>
    
  - <span data-ttu-id="31b06-115">**태그**: 고급 eDiscovery는 전문가의 반복적인 검토 및 개별 파일에 대 한 태그 지정에 따라 각 문제와 관련 된 관련성 기준을 학습 합니다.</span><span class="sxs-lookup"><span data-stu-id="31b06-115">**Tag**: Advanced eDiscovery learns Relevance criteria specific to each issue based on the expert's iterative review and tagging of individual files.</span></span>
    
  - <span data-ttu-id="31b06-116">**트랙**: 프로세스의 통계 유효성을 모니터링 하는 동안 관련성 교육의 중간 결과를 계산 하 고 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="31b06-116">**Track**: Calculate and display interim results of the Relevance training while monitoring statistical validity of the process.</span></span> 
    
- <span data-ttu-id="31b06-117">**일괄 처리 계산**: 축적 되 고 배운 관련성 기준은 전체 파일 컬렉션에 적용 되며 각 파일에 대 한 관련성 점수가 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="31b06-117">**Batch calculation**: The accumulated and learned Relevance criteria is applied to the entire file collection, and a Relevance score is generated for each file.</span></span>
    
- <span data-ttu-id="31b06-118">**결정**: 전체 사례에 적용 된 분석 결과가 일괄 처리 후에 표시 되 고, 문서 검토 결정을 내리는 데 사용 되는 데이터가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="31b06-118">**Decide**: The results of the analysis applied to the entire case is displayed after Batch calculation, and data used to make document review decisions is displayed.</span></span>
    
- <span data-ttu-id="31b06-119">**테스트**: 결과를 테스트 하 여 고급 eDiscovery 처리의 유효성 및 효율성을 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="31b06-119">**Test**: Results can be tested to verify the validity and effectiveness of the Advanced eDiscovery processing.</span></span>

- <span data-ttu-id="31b06-120">**검색**: 관련성 워크플로가 완료 되 면 검토 집합 내에서 쿼리를 실행할 때 문서와 같은 출력을 사용 하 여 문제를 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="31b06-120">**Search**: Once the Relevance workflow is complete, you can use the output such as read percentile of a document for your issue when you run a query within your review set.</span></span>
    
## <a name="guidelines-for-relevance-training-and-review"></a><span data-ttu-id="31b06-121">관련성 교육 및 검토 지침</span><span class="sxs-lookup"><span data-stu-id="31b06-121">Guidelines for Relevance training and review</span></span>

<span data-ttu-id="31b06-122">다음은 관련성 교육과 검토 지침에 대 한 개요입니다.</span><span class="sxs-lookup"><span data-stu-id="31b06-122">Following is an overview of guidelines for Relevance training and review:</span></span>
  
- <span data-ttu-id="31b06-123">**오류 및 불일치**: 교육 중에 태그 오류가 발생 한 경우 문제를 해결 하기 위해 이전 파일 샘플로 돌아갑니다.</span><span class="sxs-lookup"><span data-stu-id="31b06-123">**Errors and inconsistencies**: If tagging errors are made during training, return to previous file samples to correct them.</span></span> <span data-ttu-id="31b06-124">오류가 너무 많이 발생 하거나 사례 또는 문제에 대 한 새로운 측면이 발생 하는 경우에는 관련성 기준을 관리자가 다시 정의 하 고 관련성 학습을 재시작 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="31b06-124">If there are too many errors to correct or there is a new perspective of the case or issue, the Relevance criteria should be redefined by the Administrator, and the Relevance training restarted.</span></span>
    
- <span data-ttu-id="31b06-125">**태그 지정 및 교육**:</span><span class="sxs-lookup"><span data-stu-id="31b06-125">**Tagging and training**:</span></span> 
    
  - <span data-ttu-id="31b06-126">파일은 콘텐츠만 사용 하 여 태그를 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="31b06-126">Files should be tagged based on content only.</span></span> <span data-ttu-id="31b06-127">Custodian, date 또는 file 경로와 같은 메타 데이터를 고려 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="31b06-127">Do not consider metadata, such as custodian, date, or file path.</span></span> 
    
  - <span data-ttu-id="31b06-128">파일에 태그를 지정할 때 텍스트에 날짜 범위 표시를 고려 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="31b06-128">Do not consider date range indications in the text when tagging files.</span></span>
    
  - <span data-ttu-id="31b06-129">파일에 태그를 지정할 때 포함 된 그래픽 이미지를 고려 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="31b06-129">Do not consider embedded graphical images when tagging files.</span></span>
     
  - <span data-ttu-id="31b06-130">무시 텍스트 보기의 표시 된 파일 내용에서 관련성이 높은 관련성에 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="31b06-130">Ignore text applied to Relevance will be removed in the displayed file content in the text view in Relevance.</span></span> <span data-ttu-id="31b06-131">"무시" 텍스트에 대 한 값이 관련성 학습을 이미 시작한 후에 정의 된 경우에는 무시 된 텍스트가 정의 된 지점에서 만든 샘플 파일에 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="31b06-131">If the values for Ignore text were defined after Relevance training already started, the new ignored text will be applied to sample files created from the point in which it was defined.</span></span> <span data-ttu-id="31b06-132">무시 텍스트 기능은 파일 분석의 성능을 저하 시킬 수 있으므로 주의 해 서 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="31b06-132">The Ignore Text feature should be used cautiously, as its use may reduce the performance of file analysis</span></span>
    
  - <span data-ttu-id="31b06-133">필요한 경우에만 **태그 지정 건너뛰기** 옵션을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="31b06-133">Use the **Skip tagging** option only when necessary.</span></span> <span data-ttu-id="31b06-134">고급 eDiscovery는 건너뛴 파일을 기반으로 교육을 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="31b06-134">Advanced eDiscovery does not train based on skipped files.</span></span> <span data-ttu-id="31b06-135">평가에서는 파일에 대 한 관련성을 알기 어려운 경우에는 **건너뛰기를**선택 하는 것이 아니라 가능한 경우에도 적절 한 (R) 또는 적절 하지 않은 (veiligheid) 태그를 지정 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="31b06-135">In assessment, if it's hard to tell whether a file is relevant, it is better to tag as Relevant (R) or Not relevant (NR) whenever possible rather than selecting **Skip**.</span></span> <span data-ttu-id="31b06-136">Advanced eDiscovery에서 교육을 평가할 때는 이러한 유형의 파일을 처리 하는 방법을 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="31b06-136">When Advanced eDiscovery evaluates training, it can then be seen how well these types of files were processed.</span></span>
    
  - <span data-ttu-id="31b06-137">압축을 푼 텍스트가 매우 적은 파일에도 가능 하면 교육에서 "건너뛰기"가 아닌 R/VEILIGHEID로 태그를 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="31b06-137">Even files with a very small amount of extracted text should be tagged in training as R/NR, rather than as "Skip", when possible.</span></span> 
    
  - <span data-ttu-id="31b06-138">태그를 지정 하면 파일을 읽을 수 있고 R/VEILIGHEID 태그로 태그를 지정할 수 있는 한 분류자에 게 영향을 줍니다.</span><span class="sxs-lookup"><span data-stu-id="31b06-138">Tagging can impact the classifier as long as the file is readable and can be tagged as R/NR.</span></span>
    
  - <span data-ttu-id="31b06-139">**태그** 탭에 표시 된 샘플 파일 목록의 파일 시퀀스 번호를 사용 하 여 사용자는 표시 된 파일의 원래 순서 대로 돌아갈 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="31b06-139">The file sequence number on the displayed Sample files list on the **Tag** tab allows the user to return to the original displayed order of the files.</span></span> 
    
  - <span data-ttu-id="31b06-140">모든 샘플로 돌아가서 평가 및 학습 집합 파일의 태그를 변경할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="31b06-140">You can go back to any sample and change the tagging of the assessment and training set files.</span></span> <span data-ttu-id="31b06-141">변경 내용은 다음 샘플을 만들 때 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="31b06-141">The changes will be applied when creating the next sample.</span></span>
    
  - <span data-ttu-id="31b06-142">스캔 한 Excel 파일을 PDF 형식으로 지정 하는 경우 파일 태그를 지정할 때 기본 Excel 파일과 동일 하 게 취급 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="31b06-142">Scanned Excel files in PDF format should be treated the same as native Excel files when tagging files.</span></span>
    
  - <span data-ttu-id="31b06-143">파일의 관련성 태그 지정과 관련 하 여 확실 하지 않은 경우 전문가에 게 문의 하십시오.</span><span class="sxs-lookup"><span data-stu-id="31b06-143">When in doubt regarding the Relevance tagging of a file, consult an expert.</span></span> <span data-ttu-id="31b06-144">관련성을 교육 하는 동안 잘못 된 태그를 지정 하면 프로세스의 후반부에서 시간이 더 오래 걸릴 수 있으며 전체 결과의 품질에 부정적인 영향을 줄 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="31b06-144">Incorrect tagging during the Relevance training can lead to lost time later in the process and may also have a negative impact on the quality of the overall results.</span></span>
    
  - <span data-ttu-id="31b06-145">키워드 목록에서 정의 된 키워드는 사용자가 태그를 지정 하는 동안 관련 파일을 식별 하는 데 도움이 되는 색으로 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="31b06-145">Keywords that were defined in Keyword lists will be displayed in colors to help the user identify relevant files while tagging.</span></span>
    
- <span data-ttu-id="31b06-146">**일괄 처리**: 전문가가 R/veiligheid로 태그가 지정 된 파일에는 점수가 0 또는 100로 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="31b06-146">**Batch calculation**: Files that were tagged as R/NR by the expert will receive a score of either 0 or 100.</span></span> <span data-ttu-id="31b06-147">이는 일괄 계산 전의 태그 작성에 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="31b06-147">This applies to tagging made before Batch calculation.</span></span> <span data-ttu-id="31b06-148">전문가가 일괄 계산을 수행한 후에 유휴 상태로 전환 하 여이 문제에 계속 태그를 지정 하면, 새로 태그 된 점수가 100/0이 아니라 원래 점수가 됩니다.</span><span class="sxs-lookup"><span data-stu-id="31b06-148">If the expert switched the issue to Idle after Batch Calculation and continued tagging this issue, the newly tagged scores will not be 100/0 but rather the original score.</span></span>
    
- <span data-ttu-id="31b06-149">**문제 및 샘플링 모드**: 해당 작업에 대 한 작업이 완료 되 면 (관련성 교육이 안정화 되 고 일괄 처리를 수행한 경우) 문제가 취소 되거나 다른 사용자가 문제를 해결 하는 경우에는 일반적으로 문제가 꺼집니다.</span><span class="sxs-lookup"><span data-stu-id="31b06-149">**Issues and sampling mode**: Issues are usually turned Off when work on them is completed (Relevance training is stabilized and Batch calculation was performed), when the issues are canceled, or when another user is working on the issues.</span></span>
    
## <a name="steps-in-relevance-training"></a><span data-ttu-id="31b06-150">관련성 교육의 단계</span><span class="sxs-lookup"><span data-stu-id="31b06-150">Steps in Relevance training</span></span>

<span data-ttu-id="31b06-151">**관련성 \> 추적** 탭에서 Advanced eDiscovery는 다음 단계에 따라 처리에서 진행 하는 방법에 대 한 권장 사항을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="31b06-151">In the **Relevance \> Track** tab, Advanced eDiscovery provides recommendations on how to proceed in the processing, with the following next steps.</span></span> <span data-ttu-id="31b06-152">관련성 교육 프로세스에서 다음 각 단계를 권장 하는 것은 아래에 설명 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="31b06-152">The implications are described below when each of the following steps is recommended in the Relevance training process.</span></span> 
  
- <span data-ttu-id="31b06-153">태그 지정/계속 태그 지정: 각 파일에 대해 전문가가 수행 하는 파일 검토 및 관련성 태그 지정 및 샘플 내에서 문제를 해결 합니다.</span><span class="sxs-lookup"><span data-stu-id="31b06-153">Tagging / Continue tagging: File review and Relevance tagging performed by an expert for each file and issue within a sample.</span></span>
    
  - <span data-ttu-id="31b06-154">함축: 기존 샘플에 태그를 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="31b06-154">Implication: An existing sample needs to be tagged.</span></span>
    
- <span data-ttu-id="31b06-155">평가/계속 평가: 대/소문자 문제 관련성을 조기에 확인 하 고 현재 사례에 대해 가져온 파일 모집단의 관련성을 미리 볼 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="31b06-155">Assessment / Continue assessment: Enables early validation of case issue relevance and a preliminary view of the relevance of the file population imported for the current case.</span></span>
    
  - <span data-ttu-id="31b06-156">함축: 추가 평가가 필요 하거나 권장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="31b06-156">Implication: More assessment is required or recommended.</span></span>
    
- <span data-ttu-id="31b06-157">교육/계속 교육: 고급 eDiscovery에서 파일 샘플 태그를 지정 하는 전문가 로부터 학습 하 고 각 사례 컨텍스트 내의 각 문제와 관련 된 관련성 기준을 식별 하는 기능을 제공 하는 프로세스입니다.</span><span class="sxs-lookup"><span data-stu-id="31b06-157">Training / Continue training: Process during which Advanced eDiscovery learns from the expert who is tagging the file samples and acquires the ability to identify Relevance criteria pertinent to each issue within the context of each case.</span></span>
    
  - <span data-ttu-id="31b06-158">함축: 문제에 대 한 교육은 더 많이 필요 합니다. 다음 예제를 만들고 태그를 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="31b06-158">Implication: The issue needs more training; the next sample should be created and tagged.</span></span> 
    
- <span data-ttu-id="31b06-159">일괄 계산: 고급 eDiscovery에서 학습 단계 중에 얻은 지식을 사용 하 여 전체 파일 채우기에 적용 하는 관련성 프로세스입니다.</span><span class="sxs-lookup"><span data-stu-id="31b06-159">Batch calculation: Relevance process in which Advanced eDiscovery takes the knowledge acquired during the training stage and applies it to the entire file population.</span></span> <span data-ttu-id="31b06-160">관련 파일 그룹의 모든 파일은 관련성을 평가 하 고 관련성 점수를 할당 받습니다.</span><span class="sxs-lookup"><span data-stu-id="31b06-160">All files in the pertinent file group are assessed for relevance and assigned a Relevance score.</span></span>
    
  - <span data-ttu-id="31b06-161">함축: 문제가 안정화 되 고 일괄 처리를 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="31b06-161">Implication: The issue has stabilized, and Batch calculation can be performed.</span></span>
    
- <span data-ttu-id="31b06-162">보완: 관련성이 있는 경우 전문가가 롤링 로드 시나리오에서 추가 파일 로드 로부터 선택한 파일의 샘플을 검토 하 고 태그를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="31b06-162">Catch-up: Relevance indicates when an expert reviews and tags a sample of files selected from an additional file load during a Rolling Loads scenario.</span></span>
    
  - <span data-ttu-id="31b06-163">함축: 작업을 계속 하려면 새 부하가 추가 되 고 보완 작업이 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="31b06-163">Implication: A new load has been added, and Catch-up is required to continue working.</span></span>
    
- <span data-ttu-id="31b06-164">태그 불일치: 프로세스가 고급 eDiscovery 알고리즘을 통해 분석에 부정적인 영향을 줄 수 있는 파일 태그 지정 프로세스의 불일치를 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="31b06-164">Tag inconsistencies: Process identifies, via an Advanced eDiscovery algorithm, inconsistencies in the file tagging process that may negatively impact the analysis.</span></span>
    
  - <span data-ttu-id="31b06-165">함축: 다음 샘플에는 이전 예제에서 태그를 지정 하 고 태그를 다시 실행 해야 하는 파일이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="31b06-165">Implication: The next sample will include files that have been tagged in previous samples, and their tagging must be redone.</span></span>
    
- <span data-ttu-id="31b06-166">업데이트 분류자: 사용자가 태그 지정 또는 시드 변경 내용을 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="31b06-166">Update classifier: Allows the user to apply tagging or seeding changes.</span></span>
    
  - <span data-ttu-id="31b06-167">함축: 태그 지정 및 시드 변경 내용은 다른 관련성 샘플을 수동으로 실행 하지 않고도 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="31b06-167">Implication: Tagging and seeding changes can be applied without needing to manually run another Relevance sample.</span></span>
    
- <span data-ttu-id="31b06-168">보류: 관련성 교육 프로세스가 완료 됩니다.</span><span class="sxs-lookup"><span data-stu-id="31b06-168">On hold: The Relevance training process is completed.</span></span>
    
  - <span data-ttu-id="31b06-169">함축:이 시점에서는 관련성 교육이 필요 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="31b06-169">Implication: No Relevance training is required at this point.</span></span>
    
<span data-ttu-id="31b06-170">고급 eDiscovery에서는 프로세스를 안내 하지만 다른 단계에서 권장 되는 다음 단계를 통해 탭과 페이지를 탐색할 수 있을 뿐만 아니라 개별 사례, 문제 또는 사용자에 게 적합 한 상황을 해결 하기 위한 선택도 가능 합니다. 문서 검토 프로세스</span><span class="sxs-lookup"><span data-stu-id="31b06-170">Although Advanced eDiscovery guides you through the process, with recommended Next steps at different stages, it also allows you to navigate between tabs and pages, and to make choices to address situations that may be pertinent to your individual case, issue, or document review process.</span></span> 
  
<span data-ttu-id="31b06-171">고급 eDiscovery 다음 단계 처리 옵션을 수락 하거나 무시할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="31b06-171">It is possible to accept or override Advanced eDiscovery Next step processing choices.</span></span> <span data-ttu-id="31b06-172">권장 되는 다음 단계를 제외한 나머지 단계를 수행 하려면 대화에 확장 된 문제 표시에 나열 된 **다음 단계** 를 클릭 하 고 다음 단계 옆에 있는 **Modify (수정** ) 단추를 클릭 한 다음 다른 다음 단계 옵션을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="31b06-172">If you want to perform a step other than the recommended Next step, click the **Next step** listed in the expanded issue display in the dialog, click the **Modify** button next to the Next step, and select another Next step option.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="31b06-173">일부 옵션은 프로세스의 해당 시점에는 사용할 수 없으므로 잠금 해제 후에도 사용 하지 않도록 설정 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="31b06-173">Some options may remain disabled after unlocking as they are not supported for use at that point in the process.</span></span> 
  
## <a name="more-information"></a><span data-ttu-id="31b06-174">추가 정보</span><span class="sxs-lookup"><span data-stu-id="31b06-174">More information</span></span>

[<span data-ttu-id="31b06-175">관련성 평가 이해</span><span class="sxs-lookup"><span data-stu-id="31b06-175">Understanding Assessment in Relevance</span></span>](../assessment-in-relevance-in-advanced-ediscovery.md)
  
[<span data-ttu-id="31b06-176">태그 지정 및 평가</span><span class="sxs-lookup"><span data-stu-id="31b06-176">Tagging and Assessment</span></span>](../tagging-and-assessment-in-advanced-ediscovery.md)
  
[<span data-ttu-id="31b06-177">태그 지정 및 관련성 교육</span><span class="sxs-lookup"><span data-stu-id="31b06-177">Tagging and Relevance training</span></span>](../tagging-and-relevance-training-in-advanced-ediscovery.md)
  
[<span data-ttu-id="31b06-178">관련성 분석 추적</span><span class="sxs-lookup"><span data-stu-id="31b06-178">Tracking Relevance analysis</span></span>](../track-relevance-analysis-in-advanced-ediscovery.md)
  
[<span data-ttu-id="31b06-179">결과를 기준으로 결정</span><span class="sxs-lookup"><span data-stu-id="31b06-179">Deciding based on the results</span></span>](../decision-based-on-the-results-in-advanced-ediscovery.md)
  
[<span data-ttu-id="31b06-180">관련성 분석 테스트</span><span class="sxs-lookup"><span data-stu-id="31b06-180">Testing Relevance analysis</span></span>](../test-relevance-analysis-in-advanced-ediscovery.md)

[<span data-ttu-id="31b06-181">검토 집합에서 데이터 쿼리</span><span class="sxs-lookup"><span data-stu-id="31b06-181">Query the data in a review set</span></span>](review-set-search.md)
