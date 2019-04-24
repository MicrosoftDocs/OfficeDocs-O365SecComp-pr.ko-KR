---
title: Office 365 Advanced eDiscovery에서 관련성 모듈 사용
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
ms.assetid: 5d671821-d188-42da-a9ce-9cfe92beedfd
description: '교육 및 파일 검토를 위한 워크플로, 지침 및 단계를 포함 하 여 Office 365 Advanced eDiscovery의 관련성 모듈에 대해 알아봅니다.  '
ms.openlocfilehash: ad44066c8b00bccacf1f4fe2088aa84096c4db84
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32263790"
---
# <a name="use-the-relevance-module-in-office-365-advanced-ediscovery"></a><span data-ttu-id="83c14-103">Office 365 Advanced eDiscovery에서 관련성 모듈 사용</span><span class="sxs-lookup"><span data-stu-id="83c14-103">Use the Relevance module in Office 365 Advanced eDiscovery</span></span>

> [!NOTE]
> <span data-ttu-id="83c14-p101">Advanced eDiscovery를 사용하려면 Office 365 E3의 고급 준수 추가 기능이나 조직을 위한 E5 구독이 필요합니다. 이 요금제가 없는 상태에서 Advanced eDiscovery를 사용하려는 경우에는 [Office 365 Enterprise E5 평가판을 등록](https://go.microsoft.com/fwlink/p/?LinkID=698279)할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="83c14-p101">Advanced eDiscovery requires an Office 365 E3 with the Advanced Compliance add-on or an E5 subscription for your organization. If you don't have that plan and want to try Advanced eDiscovery, you can [sign up for a trial of Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span></span> 
  
<span data-ttu-id="83c14-106">고급 eDiscovery에서 관련성 모듈에는 사례와 관련 된 파일의 관련성 교육과 검토가 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="83c14-106">In Advanced eDiscovery, the Relevance module includes the Relevance training and review of files related to a case.</span></span> <span data-ttu-id="83c14-107">관련성 워크플로는 다음과 같이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="83c14-107">The Relevance workflow is shown and described as follows:</span></span>
  
![관련성 워크플로](media/44c67dd2-7a20-40a9-b0ed-784364845c77.gif)
  
- <span data-ttu-id="83c14-109">**평가 및 추적 주기**:</span><span class="sxs-lookup"><span data-stu-id="83c14-109">**Cycles of assessment and tracking**:</span></span>
    
  - <span data-ttu-id="83c14-110">**평가**: 고급 eDiscovery에서는 파일의 무작위 샘플을 기반으로 초기 평가를 수행 하 고이 평가를 통해 예측 코딩 프로세스의 성능을 결정 하기 위한 결정을 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="83c14-110">**Assessment**: Advanced eDiscovery enables early assessment based on a random sample of files and uses this assessment to apply decisions to determine the performance of the predictive coding process.</span></span> 
    
  - <span data-ttu-id="83c14-111">**트랙**: Advanced eDiscovery는 프로세스의 통계 유효성을 모니터링 하는 동안 평가의 중간 결과를 계산 하 고 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="83c14-111">**Track**: Advanced eDiscovery calculates and displays interim results of the assessment while monitoring statistical validity of the process.</span></span> 
    
- <span data-ttu-id="83c14-112">**교육 주기 및 추적**:</span><span class="sxs-lookup"><span data-stu-id="83c14-112">**Cycles of training and tracking**:</span></span>
    
  - <span data-ttu-id="83c14-113">**태그**: 고급 eDiscovery는 전문가의 반복적인 검토 및 개별 파일에 대 한 태그 지정에 따라 각 문제와 관련 된 관련성 기준을 학습 합니다.</span><span class="sxs-lookup"><span data-stu-id="83c14-113">**Tag**: Advanced eDiscovery learns Relevance criteria specific to each issue based on the expert's iterative review and tagging of individual files.</span></span>
    
  - <span data-ttu-id="83c14-114">**트랙**: Advanced eDiscovery는 프로세스의 통계 유효성을 모니터링 하는 동안 관련성 교육의 중간 결과를 계산 하 고 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="83c14-114">**Track**: Advanced eDiscovery calculates and displays interim results of the Relevance training while monitoring statistical validity of the process.</span></span> 
    
- <span data-ttu-id="83c14-115">**일괄 처리**: 고급 eDiscovery에서는 누적 되 고 배운 관련성 기준을 사용 하 여 전체 파일 컬렉션에 적용 하 고 각 파일에 대 한 관련성 점수를 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="83c14-115">**Batch calculation**: Advanced eDiscovery takes the accumulated and learned Relevance criteria, applies it to the entire file collection, and generates Relevance scores for each file.</span></span>
    
- <span data-ttu-id="83c14-116">의사 **결정**: 고급 eDiscovery는 일괄 계산 후에 전체 사례에 적용 된 분석 결과를 표시 하 고 문서 검토 결정을 위한 데이터를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="83c14-116">**Decide**: Advanced eDiscovery displays the results of the analysis applied to the entire case after Batch calculation and displays data for making document review decisions.</span></span>
    
- <span data-ttu-id="83c14-117">**Test**: advanced ediscovery 결과를 테스트 하 여 advanced ediscovery 처리의 유효성 및 효율성을 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="83c14-117">**Test**: Advanced eDiscovery results can be tested to verify the validity and effectiveness of the Advanced eDiscovery processing.</span></span>
    
## <a name="guidelines-for-relevance-training-and-review"></a><span data-ttu-id="83c14-118">관련성 교육 및 검토 지침</span><span class="sxs-lookup"><span data-stu-id="83c14-118">Guidelines for Relevance training and review</span></span>

<span data-ttu-id="83c14-119">다음은 관련성 교육과 검토 지침에 대 한 개요입니다.</span><span class="sxs-lookup"><span data-stu-id="83c14-119">Following is an overview of guidelines for Relevance training and review:</span></span>
  
- <span data-ttu-id="83c14-120">**오류 및 불일치**: 교육 중에 태그 오류가 발생 한 경우 문제를 해결 하기 위해 이전 파일 샘플로 돌아갑니다.</span><span class="sxs-lookup"><span data-stu-id="83c14-120">**Errors and inconsistencies**: If tagging errors are made during training, return to previous file samples to correct them.</span></span> <span data-ttu-id="83c14-121">오류가 너무 많이 발생 하거나 사례 또는 문제에 대 한 새로운 측면이 발생 하는 경우에는 관련성 기준을 관리자가 다시 정의 하 고 관련성 학습을 재시작 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="83c14-121">If there are too many errors to correct or there is a new perspective of the case or issue, the Relevance criteria should be redefined by the Administrator, and the Relevance training restarted.</span></span>
    
- <span data-ttu-id="83c14-122">**태그 지정 및 교육**:</span><span class="sxs-lookup"><span data-stu-id="83c14-122">**Tagging and training**:</span></span> 
    
  - <span data-ttu-id="83c14-123">파일은 콘텐츠만 사용 하 여 태그를 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="83c14-123">Files should be tagged based on content only.</span></span> <span data-ttu-id="83c14-124">custodian, date 또는 file 경로와 같은 메타 데이터를 고려 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="83c14-124">Do not consider metadata, such as custodian, date, or file path.</span></span> 
    
  - <span data-ttu-id="83c14-125">파일에 태그를 지정할 때 텍스트에 날짜 범위 표시를 고려 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="83c14-125">Do not consider date range indications in the text when tagging files.</span></span>
    
  - <span data-ttu-id="83c14-126">파일에 태그를 지정할 때 포함 된 그래픽 이미지를 고려 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="83c14-126">Do not consider embedded graphical images when tagging files.</span></span>
    
  - <span data-ttu-id="83c14-127">태그를 지정 하는 동안 **서식 있는 텍스트 보기** 아이콘을 사용 하 여 파일을 보는 경우 텍스트 서식을 고려 하지 마십시오.</span><span class="sxs-lookup"><span data-stu-id="83c14-127">If viewing a file using the **formatted text view** icon while tagging, do not consider the formatting of text.</span></span> <span data-ttu-id="83c14-128">예를 들어 문서에 취소선이 표시 되 고, 해당 중심을 기준으로 하는 가로 줄이 분석 된 텍스트의 일부로 서 관련성을 유지 하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="83c14-128">For example, a word displayed with a strikethrough (a horizontal line through its center indicating deletion) is still considered by Relevance as part of the analyzed text.</span></span> 
    
  - <span data-ttu-id="83c14-129">무시 텍스트 보기의 관련 항목 (사례 관리자 또는 관리자가 설정)에는 관련성이 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="83c14-129">Ignore text applied to Relevance (as set by the Case Manager or Administrator) will be removed in the displayed file content in the text view in Relevance.</span></span> <span data-ttu-id="83c14-130">"무시" 텍스트에 대 한 값이 관련성 학습을 이미 시작한 후에 정의 된 경우에는 무시 된 텍스트가 정의 된 지점에서 만든 샘플 파일에 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="83c14-130">If the values for Ignore text were defined after Relevance training already started, the new ignored text will be applied to sample files created from the point in which it was defined.</span></span> <span data-ttu-id="83c14-131">무시 텍스트 기능은 파일 분석의 성능을 저하 시킬 수 있으므로 주의 해 서 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="83c14-131">The Ignore Text feature should be used cautiously, as its use may reduce the performance of file analysis</span></span>
    
  - <span data-ttu-id="83c14-132">필요한 경우에만 **태그 지정 건너뛰기** 옵션을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="83c14-132">Use the **Skip tagging** option only when necessary.</span></span> <span data-ttu-id="83c14-133">고급 eDiscovery는 건너뛴 파일을 기반으로 교육을 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="83c14-133">Advanced eDiscovery does not train based on skipped files.</span></span> <span data-ttu-id="83c14-134">평가에서는 파일에 대 한 관련성을 알기 어려운 경우에는 **건너뛰기를**선택 하는 것이 아니라 가능한 경우에도 적절 한 (R) 또는 적절 하지 않은 (veiligheid) 태그를 지정 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="83c14-134">In assessment, if it's hard to tell whether a file is relevant, it is better to tag as Relevant (R) or Not relevant (NR) whenever possible rather than selecting **Skip**.</span></span> <span data-ttu-id="83c14-135">Advanced eDiscovery에서 교육을 평가할 때는 이러한 유형의 파일을 처리 하는 방법을 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="83c14-135">When Advanced eDiscovery evaluates training, it can then be seen how well these types of files were processed.</span></span>
    
  - <span data-ttu-id="83c14-136">압축을 푼 텍스트가 매우 적은 파일에도 가능 하면 교육에서 "건너뛰기"가 아닌 R/veiligheid로 태그를 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="83c14-136">Even files with a very small amount of extracted text should be tagged in training as R/NR, rather than as "Skip", when possible.</span></span> 
    
  - <span data-ttu-id="83c14-137">태그를 지정 하면 파일을 읽을 수 있고 R/veiligheid 태그로 태그를 지정할 수 있는 한 분류자에 게 영향을 줍니다.</span><span class="sxs-lookup"><span data-stu-id="83c14-137">Tagging can impact the classifier as long as the file is readable and can be tagged as R/NR.</span></span>
    
  - <span data-ttu-id="83c14-138">**태그** 탭에 표시 된 샘플 파일 목록의 파일 시퀀스 번호를 사용 하 여 사용자는 표시 된 파일의 원래 순서 대로 돌아갈 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="83c14-138">The file sequence number on the displayed Sample files list on the **Tag** tab allows the user to return to the original displayed order of the files.</span></span> 
    
  - <span data-ttu-id="83c14-139">모든 샘플로 돌아가서 평가 및 학습 집합 파일의 태그를 변경할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="83c14-139">You can go back to any sample and change the tagging of the assessment and training set files.</span></span> <span data-ttu-id="83c14-140">변경 내용은 다음 샘플을 만들 때 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="83c14-140">The changes will be applied when creating the next sample.</span></span>
    
  - <span data-ttu-id="83c14-141">스캔 한 excel 파일을 PDF 형식으로 지정 하는 경우 파일 태그를 지정할 때 기본 excel 파일과 동일 하 게 취급 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="83c14-141">Scanned Excel files in PDF format should be treated the same as native Excel files when tagging files.</span></span>
    
  - <span data-ttu-id="83c14-142">파일의 관련성 태그 지정과 관련 하 여 확실 하지 않은 경우 전문가에 게 문의 하십시오.</span><span class="sxs-lookup"><span data-stu-id="83c14-142">When in doubt regarding the Relevance tagging of a file, consult an expert.</span></span> <span data-ttu-id="83c14-143">관련성을 교육 하는 동안 잘못 된 태그를 지정 하면 프로세스의 후반부에서 시간이 더 오래 걸릴 수 있으며 전체 결과의 품질에 부정적인 영향을 줄 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="83c14-143">Incorrect tagging during the Relevance training can lead to lost time later in the process and may also have a negative impact on the quality of the overall results.</span></span>
    
  - <span data-ttu-id="83c14-144">키워드 목록에서 정의 된 키워드는 사용자가 태그를 지정 하는 동안 관련 파일을 식별 하는 데 도움이 되는 색으로 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="83c14-144">Keywords that were defined in Keyword lists will be displayed in colors to help the user identify relevant files while tagging.</span></span>
    
- <span data-ttu-id="83c14-145">**일괄 처리**: 전문가가 R/veiligheid로 태그가 지정 된 파일에는 점수가 0 또는 100로 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="83c14-145">**Batch calculation**: Files that were tagged as R/NR by the expert will receive a score of either 0 or 100.</span></span> <span data-ttu-id="83c14-146">이는 일괄 계산 전의 태그 작성에 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="83c14-146">This applies to tagging made before Batch calculation.</span></span> <span data-ttu-id="83c14-147">전문가가 일괄 계산을 수행한 후에 유휴 상태로 전환 하 여이 문제에 계속 태그를 지정 하면, 새로 태그 된 점수가 100/0이 아니라 원래 점수가 됩니다.</span><span class="sxs-lookup"><span data-stu-id="83c14-147">If the expert switched the issue to Idle after Batch Calculation and continued tagging this issue, the newly tagged scores will not be 100/0 but rather the original score.</span></span>
    
- <span data-ttu-id="83c14-148">**문제 및 샘플링 모드**: 해당 작업에 대 한 작업이 완료 되 면 (관련성 교육이 안정화 되 고 일괄 처리를 수행한 경우) 문제가 취소 되거나 다른 사용자가 문제를 해결 하는 경우에는 일반적으로 문제가 꺼집니다.</span><span class="sxs-lookup"><span data-stu-id="83c14-148">**Issues and sampling mode**: Issues are usually turned Off when work on them is completed (Relevance training is stabilized and Batch calculation was performed), when the issues are canceled, or when another user is working on the issues.</span></span>
    
## <a name="steps-in-relevance-training"></a><span data-ttu-id="83c14-149">관련성 교육의 단계</span><span class="sxs-lookup"><span data-stu-id="83c14-149">Steps in Relevance training</span></span>

<span data-ttu-id="83c14-150">**관련성 \> 추적** 탭에서 Advanced eDiscovery는 다음 단계에 따라 처리에서 진행 하는 방법에 대 한 권장 사항을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="83c14-150">In the **Relevance \> Track** tab, Advanced eDiscovery provides recommendations on how to proceed in the processing, with the following next steps.</span></span> <span data-ttu-id="83c14-151">관련성 교육 프로세스에서 다음 각 단계를 권장 하는 것은 아래에 설명 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="83c14-151">The implications are described below when each of the following steps is recommended in the Relevance training process.</span></span> 
  
- <span data-ttu-id="83c14-152">태그 지정/계속 태그 지정: 각 파일에 대해 전문가가 수행 하는 파일 검토 및 관련성 태그 지정 및 샘플 내에서 문제를 해결 합니다.</span><span class="sxs-lookup"><span data-stu-id="83c14-152">Tagging / Continue tagging: File review and Relevance tagging performed by an expert for each file and issue within a sample.</span></span>
    
  - <span data-ttu-id="83c14-153">함축: 기존 샘플에 태그를 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="83c14-153">Implication: An existing sample needs to be tagged.</span></span>
    
- <span data-ttu-id="83c14-154">평가/계속 평가: 대/소문자 문제 관련성을 조기에 확인 하 고 현재 사례에 대해 가져온 파일 모집단의 관련성을 미리 볼 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="83c14-154">Assessment / Continue assessment: Enables early validation of case issue relevance and a preliminary view of the relevance of the file population imported for the current case.</span></span>
    
  - <span data-ttu-id="83c14-155">함축: 추가 평가가 필요 하거나 권장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="83c14-155">Implication: More assessment is required or recommended.</span></span>
    
- <span data-ttu-id="83c14-156">교육/계속 교육: 고급 eDiscovery에서 파일 샘플 태그를 지정 하는 전문가 로부터 학습 하 고 각 사례 컨텍스트 내의 각 문제와 관련 된 관련성 기준을 식별 하는 기능을 제공 하는 프로세스입니다.</span><span class="sxs-lookup"><span data-stu-id="83c14-156">Training / Continue training: Process during which Advanced eDiscovery learns from the expert who is tagging the file samples and acquires the ability to identify Relevance criteria pertinent to each issue within the context of each case.</span></span>
    
  - <span data-ttu-id="83c14-157">함축: 문제에 대 한 교육은 더 많이 필요 합니다. 다음 예제를 만들고 태그를 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="83c14-157">Implication: The issue needs more training; the next sample should be created and tagged.</span></span> 
    
- <span data-ttu-id="83c14-158">일괄 계산: 고급 eDiscovery에서 학습 단계 중에 얻은 지식을 사용 하 여 전체 파일 채우기에 적용 하는 관련성 프로세스입니다.</span><span class="sxs-lookup"><span data-stu-id="83c14-158">Batch calculation: Relevance process in which Advanced eDiscovery takes the knowledge acquired during the training stage and applies it to the entire file population.</span></span> <span data-ttu-id="83c14-159">관련 파일 그룹의 모든 파일은 관련성을 평가 하 고 관련성 점수를 할당 받습니다.</span><span class="sxs-lookup"><span data-stu-id="83c14-159">All files in the pertinent file group are assessed for relevance and assigned a Relevance score.</span></span>
    
  - <span data-ttu-id="83c14-160">함축: 문제가 안정화 되 고 일괄 처리를 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="83c14-160">Implication: The issue has stabilized, and Batch calculation can be performed.</span></span>
    
- <span data-ttu-id="83c14-161">보완: 관련성이 있는 경우 전문가가 롤링 로드 시나리오에서 추가 파일 로드 로부터 선택한 파일의 샘플을 검토 하 고 태그를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="83c14-161">Catch-up: Relevance indicates when an expert reviews and tags a sample of files selected from an additional file load during a Rolling Loads scenario.</span></span>
    
  - <span data-ttu-id="83c14-162">함축: 작업을 계속 하려면 새 부하가 추가 되 고 보완 작업이 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="83c14-162">Implication: A new load has been added, and Catch-up is required to continue working.</span></span>
    
- <span data-ttu-id="83c14-163">태그 불일치: 프로세스가 고급 eDiscovery 알고리즘을 통해 분석에 부정적인 영향을 줄 수 있는 파일 태그 지정 프로세스의 불일치를 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="83c14-163">Tag inconsistencies: Process identifies, via an Advanced eDiscovery algorithm, inconsistencies in the file tagging process that may negatively impact the analysis.</span></span>
    
  - <span data-ttu-id="83c14-164">함축: 다음 샘플에는 이전 예제에서 태그를 지정 하 고 태그를 다시 실행 해야 하는 파일이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="83c14-164">Implication: The next sample will include files that have been tagged in previous samples, and their tagging must be redone.</span></span>
    
- <span data-ttu-id="83c14-165">업데이트 분류자: 사용자가 태그 지정 또는 시드 변경 내용을 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="83c14-165">Update classifier: Allows the user to apply tagging or seeding changes.</span></span>
    
  - <span data-ttu-id="83c14-166">함축: 태그 지정 및 시드 변경 내용은 다른 관련성 샘플을 수동으로 실행 하지 않고도 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="83c14-166">Implication: Tagging and seeding changes can be applied without needing to manually run another Relevance sample.</span></span>
    
- <span data-ttu-id="83c14-167">보류: 관련성 교육 프로세스가 완료 됩니다.</span><span class="sxs-lookup"><span data-stu-id="83c14-167">On hold: The Relevance training process is completed.</span></span>
    
  - <span data-ttu-id="83c14-168">함축:이 시점에서는 관련성 교육이 필요 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="83c14-168">Implication: No Relevance training is required at this point.</span></span>
    
<span data-ttu-id="83c14-169">고급 eDiscovery에서는 프로세스를 안내 하지만 다른 단계에서 권장 되는 다음 단계를 통해 탭과 페이지를 탐색할 수 있을 뿐만 아니라 개별 사례, 문제 또는 사용자에 게 적합 한 상황을 해결 하기 위한 선택도 가능 합니다. 문서 검토 프로세스</span><span class="sxs-lookup"><span data-stu-id="83c14-169">Although Advanced eDiscovery guides you through the process, with recommended Next steps at different stages, it also allows you to navigate between tabs and pages, and to make choices to address situations that may be pertinent to your individual case, issue, or document review process.</span></span> 
  
<span data-ttu-id="83c14-170">고급 eDiscovery 다음 단계 처리 옵션을 수락 하거나 무시할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="83c14-170">It is possible to accept or override Advanced eDiscovery Next step processing choices.</span></span> <span data-ttu-id="83c14-171">권장 되는 다음 단계를 제외한 나머지 단계를 수행 하려면 대화에 확장 된 문제 표시에 나열 된 **다음 단계** 를 클릭 하 고 다음 단계 옆에 있는 **Modify (수정** ) 단추를 클릭 한 다음 다른 다음 단계 옵션을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="83c14-171">If you want to perform a step other than the recommended Next step, click the **Next step** listed in the expanded issue display in the dialog, click the **Modify** button next to the Next step, and select another Next step option.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="83c14-172">일부 옵션은 프로세스의 해당 시점에는 사용할 수 없으므로 잠금 해제 후에도 사용 하지 않도록 설정 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="83c14-172">Some options may remain disabled after unlocking as they are not supported for use at that point in the process.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="83c14-173">참고 항목</span><span class="sxs-lookup"><span data-stu-id="83c14-173">See also</span></span>

[<span data-ttu-id="83c14-174">Office 365 Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="83c14-174">Office 365 Advanced eDiscovery</span></span>](office-365-advanced-ediscovery.md)
  
[<span data-ttu-id="83c14-175">관련성 평가 이해</span><span class="sxs-lookup"><span data-stu-id="83c14-175">Understanding Assessment in Relevance</span></span>](assessment-in-relevance-in-advanced-ediscovery.md)
  
[<span data-ttu-id="83c14-176">태그 지정 및 평가</span><span class="sxs-lookup"><span data-stu-id="83c14-176">Tagging and Assessment</span></span>](tagging-and-assessment-in-advanced-ediscovery.md)
  
[<span data-ttu-id="83c14-177">태그 지정 및 관련성 교육</span><span class="sxs-lookup"><span data-stu-id="83c14-177">Tagging and Relevance training</span></span>](tagging-and-relevance-training-in-advanced-ediscovery.md)
  
[<span data-ttu-id="83c14-178">관련성 분석 추적</span><span class="sxs-lookup"><span data-stu-id="83c14-178">Tracking Relevance analysis</span></span>](track-relevance-analysis-in-advanced-ediscovery.md)
  
[<span data-ttu-id="83c14-179">결과를 기준으로 결정</span><span class="sxs-lookup"><span data-stu-id="83c14-179">Deciding based on the results</span></span>](decision-based-on-the-results-in-advanced-ediscovery.md)
  
[<span data-ttu-id="83c14-180">관련성 분석 테스트</span><span class="sxs-lookup"><span data-stu-id="83c14-180">Testing Relevance analysis</span></span>](test-relevance-analysis-in-advanced-ediscovery.md)

