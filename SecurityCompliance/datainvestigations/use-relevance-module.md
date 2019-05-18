---
title: 관련성 모듈을 사용 하 여 증거의 데이터 분석
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
ms.openlocfilehash: 2d7c3ae16b573af7351abda19edebde7ad7491b8
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/17/2019
ms.locfileid: "34150590"
---
# <a name="use-the-relevance-module-to-analyze-data-in-evidence"></a><span data-ttu-id="c348b-102">관련성 모듈을 사용 하 여 증거의 데이터 분석</span><span class="sxs-lookup"><span data-stu-id="c348b-102">Use the Relevance module to analyze data in evidence</span></span>

<span data-ttu-id="c348b-103">데이터 조사 (미리 보기)에서 관련성 모듈에는 조사와 관련 된 파일의 관련성 교육과 검토가 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c348b-103">In Data Investigations (Preview), the Relevance module includes the Relevance training and review of files related to an investigation.</span></span> <span data-ttu-id="c348b-104">관련성 워크플로는 다음과 같이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c348b-104">The Relevance workflow is shown and described as follows:</span></span>
  
![관련성 워크플로](../media/44c67dd2-7a20-40a9-b0ed-784364845c77.gif)
  
- <span data-ttu-id="c348b-106">**평가 및 추적 주기**:</span><span class="sxs-lookup"><span data-stu-id="c348b-106">**Cycles of assessment and tracking**:</span></span>
    
  - <span data-ttu-id="c348b-107">**평가**: 무작위 파일 샘플을 기반으로 초기 평가를 사용 하도록 설정 하 고이 평가를 통해 예측 코딩 프로세스의 성능을 결정 하는 결정을 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="c348b-107">**Assessment**: Enables early assessment based on a random sample of files and uses this assessment to apply decisions to determine the performance of the predictive coding process.</span></span> 
    
  - <span data-ttu-id="c348b-108">**트랙**: 프로세스의 통계 유효성을 모니터링 하는 동안 평가의 중간 결과를 계산 하 고 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="c348b-108">**Track**: Calculate and display interim results of the assessment while monitoring statistical validity of the process.</span></span> 
    
- <span data-ttu-id="c348b-109">**교육 주기 및 추적**</span><span class="sxs-lookup"><span data-stu-id="c348b-109">**Cycles of training and tracking**</span></span>
    
  - <span data-ttu-id="c348b-110">**태그**: 데이터 조사 (미리 보기)에서는 개별 파일의 전문가 반복 검토 및 태그 지정에 따라 각 문제와 관련 된 관련성 기준을 학습 합니다.</span><span class="sxs-lookup"><span data-stu-id="c348b-110">**Tag**: Data Investigations (Preview) learns Relevance criteria specific to each issue based on the expert's iterative review and tagging of individual files.</span></span>
    
  - <span data-ttu-id="c348b-111">**트랙**: 프로세스의 통계 유효성을 모니터링 하는 동안 관련성 교육의 중간 결과를 계산 하 고 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="c348b-111">**Track**: Calculate and display interim results of the Relevance training while monitoring statistical validity of the process.</span></span> 
    
- <span data-ttu-id="c348b-112">**일괄 처리 계산**: 축적 되 고 배운 관련성 기준은 전체 파일 컬렉션에 적용 되며 각 파일에 대 한 관련성 점수가 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c348b-112">**Batch calculation**: The accumulated and learned Relevance criteria is applied to the entire file collection, and a Relevance score is generated for each file.</span></span>
    
- <span data-ttu-id="c348b-113">**결정**: 전체 사례에 적용 된 분석 결과가 일괄 처리 후에 표시 되 고, 문서 검토 결정을 내리는 데 사용 되는 데이터가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c348b-113">**Decide**: The results of the analysis applied to the entire case is displayed after Batch calculation, and data used to make document review decisions is displayed.</span></span>
    
- <span data-ttu-id="c348b-114">**테스트**: 결과를 테스트 하 여 데이터 조사 (미리 보기) 처리의 유효성 및 효율성을 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c348b-114">**Test**: Results can be tested to verify the validity and effectiveness of the Data Investigations (Preview) processing.</span></span>

- <span data-ttu-id="c348b-115">**검색**: 관련성 워크플로가 완료 되 면 작업 집합 내에서 쿼리를 실행할 때 문서와 같은 출력을 사용 하 여 문제를 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c348b-115">**Search**: Once the Relevance workflow is complete, you can use the output such as read percentile of a document for your issue when you run a query within your working set.</span></span>
    
## <a name="guidelines-for-relevance-training-and-review"></a><span data-ttu-id="c348b-116">관련성 교육 및 검토 지침</span><span class="sxs-lookup"><span data-stu-id="c348b-116">Guidelines for Relevance training and review</span></span>

<span data-ttu-id="c348b-117">다음은 관련성 교육과 검토 지침에 대 한 개요입니다.</span><span class="sxs-lookup"><span data-stu-id="c348b-117">Following is an overview of guidelines for Relevance training and review:</span></span>
  
- <span data-ttu-id="c348b-118">**오류 및 불일치**: 교육 중에 태그 오류가 발생 한 경우 문제를 해결 하기 위해 이전 파일 샘플로 돌아갑니다.</span><span class="sxs-lookup"><span data-stu-id="c348b-118">**Errors and inconsistencies**: If tagging errors are made during training, return to previous file samples to correct them.</span></span> <span data-ttu-id="c348b-119">오류가 너무 많이 발생 하거나 사례 또는 문제에 대 한 새로운 측면이 발생 하는 경우에는 관련성 기준을 관리자가 다시 정의 하 고 관련성 학습을 재시작 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c348b-119">If there are too many errors to correct or there is a new perspective of the case or issue, the Relevance criteria should be redefined by the Administrator, and the Relevance training restarted.</span></span>
    
- <span data-ttu-id="c348b-120">**태그 지정 및 교육**:</span><span class="sxs-lookup"><span data-stu-id="c348b-120">**Tagging and training**:</span></span> 
    
  - <span data-ttu-id="c348b-121">파일은 콘텐츠만 사용 하 여 태그를 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c348b-121">Files should be tagged based on content only.</span></span> <span data-ttu-id="c348b-122">Custodian, date 또는 file 경로와 같은 메타 데이터를 고려 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c348b-122">Do not consider metadata, such as custodian, date, or file path.</span></span> 
    
  - <span data-ttu-id="c348b-123">파일에 태그를 지정할 때 텍스트에 날짜 범위 표시를 고려 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c348b-123">Do not consider date range indications in the text when tagging files.</span></span>
    
  - <span data-ttu-id="c348b-124">파일에 태그를 지정할 때 포함 된 그래픽 이미지를 고려 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c348b-124">Do not consider embedded graphical images when tagging files.</span></span>
     
  - <span data-ttu-id="c348b-125">무시 텍스트 보기의 표시 된 파일 내용에서 관련성이 높은 관련성에 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c348b-125">Ignore text applied to Relevance will be removed in the displayed file content in the text view in Relevance.</span></span> <span data-ttu-id="c348b-126">"무시" 텍스트에 대 한 값이 관련성 학습을 이미 시작한 후에 정의 된 경우에는 무시 된 텍스트가 정의 된 지점에서 만든 샘플 파일에 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c348b-126">If the values for Ignore text were defined after Relevance training already started, the new ignored text will be applied to sample files created from the point in which it was defined.</span></span> <span data-ttu-id="c348b-127">무시 텍스트 기능은 파일 분석의 성능을 저하 시킬 수 있으므로 주의 해 서 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c348b-127">The Ignore Text feature should be used cautiously, as its use may reduce the performance of file analysis</span></span>
    
  - <span data-ttu-id="c348b-128">필요한 경우에만 **태그 지정 건너뛰기** 옵션을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="c348b-128">Use the **Skip tagging** option only when necessary.</span></span> <span data-ttu-id="c348b-129">건너뛴 파일에 따라 데이터 조사 (미리 보기)가 성향 습득 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c348b-129">Data Investigations (Preview) does not train based on skipped files.</span></span> <span data-ttu-id="c348b-130">평가에서는 파일에 대 한 관련성을 알기 어려운 경우에는 **건너뛰기를**선택 하는 것이 아니라 가능한 경우에도 적절 한 (R) 또는 적절 하지 않은 (veiligheid) 태그를 지정 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="c348b-130">In assessment, if it's hard to tell whether a file is relevant, it is better to tag as Relevant (R) or Not relevant (NR) whenever possible rather than selecting **Skip**.</span></span> <span data-ttu-id="c348b-131">데이터 조사 (미리 보기)에서 교육을 평가할 때 이러한 유형의 파일을 처리 하는 방법을 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c348b-131">When Data Investigations (Preview) evaluates training, it can then be seen how well these types of files were processed.</span></span>
    
  - <span data-ttu-id="c348b-132">압축을 푼 텍스트가 매우 적은 파일에도 가능 하면 교육에서 "건너뛰기"가 아닌 R/VEILIGHEID로 태그를 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c348b-132">Even files with a very small amount of extracted text should be tagged in training as R/NR, rather than as "Skip", when possible.</span></span> 
    
  - <span data-ttu-id="c348b-133">태그를 지정 하면 파일을 읽을 수 있고 R/VEILIGHEID 태그로 태그를 지정할 수 있는 한 분류자에 게 영향을 줍니다.</span><span class="sxs-lookup"><span data-stu-id="c348b-133">Tagging can impact the classifier as long as the file is readable and can be tagged as R/NR.</span></span>
    
  - <span data-ttu-id="c348b-134">**태그** 탭에 표시 된 샘플 파일 목록의 파일 시퀀스 번호를 사용 하 여 사용자는 표시 된 파일의 원래 순서 대로 돌아갈 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c348b-134">The file sequence number on the displayed Sample files list on the **Tag** tab allows the user to return to the original displayed order of the files.</span></span> 
    
  - <span data-ttu-id="c348b-135">모든 샘플로 돌아가서 평가 및 학습 집합 파일의 태그를 변경할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c348b-135">You can go back to any sample and change the tagging of the assessment and training set files.</span></span> <span data-ttu-id="c348b-136">변경 내용은 다음 샘플을 만들 때 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c348b-136">The changes will be applied when creating the next sample.</span></span>
    
  - <span data-ttu-id="c348b-137">스캔 한 Excel 파일을 PDF 형식으로 지정 하는 경우 파일 태그를 지정할 때 기본 Excel 파일과 동일 하 게 취급 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c348b-137">Scanned Excel files in PDF format should be treated the same as native Excel files when tagging files.</span></span>
    
  - <span data-ttu-id="c348b-138">파일의 관련성 태그 지정과 관련 하 여 확실 하지 않은 경우 전문가에 게 문의 하십시오.</span><span class="sxs-lookup"><span data-stu-id="c348b-138">When in doubt regarding the Relevance tagging of a file, consult an expert.</span></span> <span data-ttu-id="c348b-139">관련성을 교육 하는 동안 잘못 된 태그를 지정 하면 프로세스의 후반부에서 시간이 더 오래 걸릴 수 있으며 전체 결과의 품질에 부정적인 영향을 줄 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c348b-139">Incorrect tagging during the Relevance training can lead to lost time later in the process and may also have a negative impact on the quality of the overall results.</span></span>
    
  - <span data-ttu-id="c348b-140">키워드 목록에서 정의 된 키워드는 사용자가 태그를 지정 하는 동안 관련 파일을 식별 하는 데 도움이 되는 색으로 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c348b-140">Keywords that were defined in Keyword lists will be displayed in colors to help the user identify relevant files while tagging.</span></span>
    
- <span data-ttu-id="c348b-141">**일괄 처리**: 전문가가 R/veiligheid로 태그가 지정 된 파일에는 점수가 0 또는 100로 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c348b-141">**Batch calculation**: Files that were tagged as R/NR by the expert will receive a score of either 0 or 100.</span></span> <span data-ttu-id="c348b-142">이는 일괄 계산 전의 태그 작성에 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c348b-142">This applies to tagging made before Batch calculation.</span></span> <span data-ttu-id="c348b-143">전문가가 일괄 계산을 수행한 후에 유휴 상태로 전환 하 여이 문제에 계속 태그를 지정 하면, 새로 태그 된 점수가 100/0이 아니라 원래 점수가 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c348b-143">If the expert switched the issue to Idle after Batch Calculation and continued tagging this issue, the newly tagged scores will not be 100/0 but rather the original score.</span></span>
    
- <span data-ttu-id="c348b-144">**문제 및 샘플링 모드**: 해당 작업에 대 한 작업이 완료 되 면 (관련성 교육이 안정화 되 고 일괄 처리를 수행한 경우) 문제가 취소 되거나 다른 사용자가 문제를 해결 하는 경우에는 일반적으로 문제가 꺼집니다.</span><span class="sxs-lookup"><span data-stu-id="c348b-144">**Issues and sampling mode**: Issues are usually turned Off when work on them is completed (Relevance training is stabilized and Batch calculation was performed), when the issues are canceled, or when another user is working on the issues.</span></span>
    
## <a name="steps-in-relevance-training"></a><span data-ttu-id="c348b-145">관련성 교육의 단계</span><span class="sxs-lookup"><span data-stu-id="c348b-145">Steps in Relevance training</span></span>

<span data-ttu-id="c348b-146">**관련성 \> 추적** 탭에서 데이터 조사는 다음 단계를 수행 하 여 처리에서 진행 하는 방법에 대 한 권장 사항을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="c348b-146">In the **Relevance \> Track** tab, Data investigations provides recommendations on how to proceed in the processing, with the following next steps.</span></span> <span data-ttu-id="c348b-147">관련성 교육 프로세스에서 다음 각 단계를 권장 하는 것은 아래에 설명 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c348b-147">The implications are described below when each of the following steps is recommended in the Relevance training process.</span></span> 
  
- <span data-ttu-id="c348b-148">태그 지정/계속 태그 지정: 각 파일에 대해 전문가가 수행 하는 파일 검토 및 관련성 태그 지정 및 샘플 내에서 문제를 해결 합니다.</span><span class="sxs-lookup"><span data-stu-id="c348b-148">Tagging / Continue tagging: File review and Relevance tagging performed by an expert for each file and issue within a sample.</span></span>
    
  - <span data-ttu-id="c348b-149">함축: 기존 샘플에 태그를 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c348b-149">Implication: An existing sample needs to be tagged.</span></span>
    
- <span data-ttu-id="c348b-150">평가/계속 평가: 대/소문자 문제 관련성을 조기에 확인 하 고 현재 사례에 대해 가져온 파일 모집단의 관련성을 미리 볼 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="c348b-150">Assessment / Continue assessment: Enables early validation of case issue relevance and a preliminary view of the relevance of the file population imported for the current case.</span></span>
    
  - <span data-ttu-id="c348b-151">함축: 추가 평가가 필요 하거나 권장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c348b-151">Implication: More assessment is required or recommended.</span></span>
    
- <span data-ttu-id="c348b-152">교육/계속 교육: 파일 샘플에 태그를 지정 하는 전문가 로부터 데이터 조사를 학습 하 고 각 사례 컨텍스트 내의 각 문제와 관련 된 관련성 기준을 식별 하는 기능을 제공 하는 프로세스입니다.</span><span class="sxs-lookup"><span data-stu-id="c348b-152">Training / Continue training: Process during which Data investigations learns from the expert who is tagging the file samples and acquires the ability to identify Relevance criteria pertinent to each issue within the context of each case.</span></span>
    
  - <span data-ttu-id="c348b-153">함축: 문제에 대 한 교육은 더 많이 필요 합니다. 다음 예제를 만들고 태그를 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c348b-153">Implication: The issue needs more training; the next sample should be created and tagged.</span></span> 
    
- <span data-ttu-id="c348b-154">일괄 처리: 데이터 조사에서 학습 단계 동안 얻은 정보를 받아 전체 파일 채우기에 적용 하는 관련성 프로세스입니다.</span><span class="sxs-lookup"><span data-stu-id="c348b-154">Batch calculation: Relevance process in which Data investigations takes the knowledge acquired during the training stage and applies it to the entire file population.</span></span> <span data-ttu-id="c348b-155">관련 파일 그룹의 모든 파일은 관련성을 평가 하 고 관련성 점수를 할당 받습니다.</span><span class="sxs-lookup"><span data-stu-id="c348b-155">All files in the pertinent file group are assessed for relevance and assigned a Relevance score.</span></span>
    
  - <span data-ttu-id="c348b-156">함축: 문제가 안정화 되 고 일괄 처리를 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c348b-156">Implication: The issue has stabilized, and Batch calculation can be performed.</span></span>
    
- <span data-ttu-id="c348b-157">보완: 관련성이 있는 경우 전문가가 롤링 로드 시나리오에서 추가 파일 로드 로부터 선택한 파일의 샘플을 검토 하 고 태그를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c348b-157">Catch-up: Relevance indicates when an expert reviews and tags a sample of files selected from an additional file load during a Rolling Loads scenario.</span></span>
    
  - <span data-ttu-id="c348b-158">함축: 작업을 계속 하려면 새 부하가 추가 되 고 보완 작업이 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="c348b-158">Implication: A new load has been added, and Catch-up is required to continue working.</span></span>
    
- <span data-ttu-id="c348b-159">태그 불일치: 프로세스에서 데이터 조사 알고리즘을 통해 분석에 부정적인 영향을 줄 수 있는 파일 태그 지정 프로세스의 불일치를 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="c348b-159">Tag inconsistencies: Process identifies, via an Data investigations algorithm, inconsistencies in the file tagging process that may negatively impact the analysis.</span></span>
    
  - <span data-ttu-id="c348b-160">함축: 다음 샘플에는 이전 예제에서 태그를 지정 하 고 태그를 다시 실행 해야 하는 파일이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c348b-160">Implication: The next sample will include files that have been tagged in previous samples, and their tagging must be redone.</span></span>
    
- <span data-ttu-id="c348b-161">업데이트 분류자: 사용자가 태그 지정 또는 시드 변경 내용을 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c348b-161">Update classifier: Allows the user to apply tagging or seeding changes.</span></span>
    
  - <span data-ttu-id="c348b-162">함축: 태그 지정 및 시드 변경 내용은 다른 관련성 샘플을 수동으로 실행 하지 않고도 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c348b-162">Implication: Tagging and seeding changes can be applied without needing to manually run another Relevance sample.</span></span>
    
- <span data-ttu-id="c348b-163">보류: 관련성 교육 프로세스가 완료 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c348b-163">On hold: The Relevance training process is completed.</span></span>
    
  - <span data-ttu-id="c348b-164">함축:이 시점에서는 관련성 교육이 필요 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c348b-164">Implication: No Relevance training is required at this point.</span></span>
    
<span data-ttu-id="c348b-165">데이터 조사 과정에서 프로세스를 안내 하지만 다른 단계에서 권장 되는 다음 단계를 수행 하는 경우에도 탭과 페이지를 탐색 하 고 개별 사례, 문제 또는 사용자에 게 관련이 있을 수 있는 상황에 대해 선택할 수 있습니다. 문서 검토 프로세스</span><span class="sxs-lookup"><span data-stu-id="c348b-165">Although Data investigations guides you through the process, with recommended Next steps at different stages, it also allows you to navigate between tabs and pages, and to make choices to address situations that may be pertinent to your individual case, issue, or document review process.</span></span> 
  
<span data-ttu-id="c348b-166">데이터 조사를 수락 하거나 재정의 하는 작업은 다음 단계 처리 옵션을 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c348b-166">It is possible to accept or override Data investigations Next step processing choices.</span></span> <span data-ttu-id="c348b-167">권장 되는 다음 단계를 제외한 나머지 단계를 수행 하려면 대화에 확장 된 문제 표시에 나열 된 **다음 단계** 를 클릭 하 고 다음 단계 옆에 있는 **Modify (수정** ) 단추를 클릭 한 다음 다른 다음 단계 옵션을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="c348b-167">If you want to perform a step other than the recommended Next step, click the **Next step** listed in the expanded issue display in the dialog, click the **Modify** button next to the Next step, and select another Next step option.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="c348b-168">일부 옵션은 프로세스의 해당 시점에는 사용할 수 없으므로 잠금 해제 후에도 사용 하지 않도록 설정 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c348b-168">Some options may remain disabled after unlocking as they are not supported for use at that point in the process.</span></span> 
  
## <a name="more-information"></a><span data-ttu-id="c348b-169">추가 정보</span><span class="sxs-lookup"><span data-stu-id="c348b-169">More information</span></span>

[<span data-ttu-id="c348b-170">관련성 평가 이해</span><span class="sxs-lookup"><span data-stu-id="c348b-170">Understanding Assessment in Relevance</span></span>](../assessment-in-relevance-in-advanced-ediscovery.md)
  
[<span data-ttu-id="c348b-171">태그 지정 및 평가</span><span class="sxs-lookup"><span data-stu-id="c348b-171">Tagging and assessment</span></span>](../tagging-and-assessment-in-advanced-ediscovery.md)
  
[<span data-ttu-id="c348b-172">태그 지정 및 관련성 교육</span><span class="sxs-lookup"><span data-stu-id="c348b-172">Tagging and Relevance training</span></span>](../tagging-and-relevance-training-in-advanced-ediscovery.md)
  
[<span data-ttu-id="c348b-173">관련성 분석 추적</span><span class="sxs-lookup"><span data-stu-id="c348b-173">Tracking Relevance analysis</span></span>](../track-relevance-analysis-in-advanced-ediscovery.md)
  
[<span data-ttu-id="c348b-174">결과를 기준으로 결정</span><span class="sxs-lookup"><span data-stu-id="c348b-174">Deciding based on the results</span></span>](../decision-based-on-the-results-in-advanced-ediscovery.md)
  
[<span data-ttu-id="c348b-175">관련성 분석 테스트</span><span class="sxs-lookup"><span data-stu-id="c348b-175">Testing Relevance analysis</span></span>](../test-relevance-analysis-in-advanced-ediscovery.md)

[<span data-ttu-id="c348b-176">증거에서 데이터 쿼리</span><span class="sxs-lookup"><span data-stu-id="c348b-176">Query the data in evidence</span></span>](evidence-query.md)
