---
title: 관련성 모듈을 사용 하 여 고급 eDiscovery (미리 보기)에서 데이터 분석
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection: ''
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: ''
ms.openlocfilehash: 5e30a7f6919f50d2d73606fae3b53f21ef33e223
ms.sourcegitcommit: ee28ee2b2bdfd049333c2f495d7f7780d13af4a6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2019
ms.locfileid: "29608113"
---
# <a name="using-the-relevance-module-to-analyze-data-in-advanced-ediscovery-preview"></a><span data-ttu-id="3e095-102">관련성 모듈을 사용 하 여 고급 eDiscovery (미리 보기)에서 데이터 분석</span><span class="sxs-lookup"><span data-stu-id="3e095-102">Using the Relevance module to analyze data in Advanced eDiscovery (Preview)</span></span>

<span data-ttu-id="3e095-p101">고급 eDiscovery (미리 보기), 관련성 모듈 관련성 교육 및 사례와 관련 된 파일의 검토를 포함 합니다. 관련성 워크플로 표시 된 이며 설명은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="3e095-p101">In Advanced eDiscovery (Preview), the Relevance module includes the Relevance training and review of files related to a case. The Relevance workflow is shown and described as follows:</span></span>
  
![관련성 워크플로](../media/44c67dd2-7a20-40a9-b0ed-784364845c77.gif)
  
- <span data-ttu-id="3e095-106">**주기 평가 및 추적**합니다.</span><span class="sxs-lookup"><span data-stu-id="3e095-106">**Cycles of assessment and tracking**:</span></span>
    
  - <span data-ttu-id="3e095-107">**평가**: 파일의 임의 표본을 기반으로 초기 평가 사용 하도록 설정 하 고이 평가 사용 하 여 예측 코딩 프로세스의 성능을 확인 하는 결정을 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="3e095-107">**Assessment**: Enables early assessment based on a random sample of files and uses this assessment to apply decisions to determine the performance of the predictive coding process.</span></span> 
    
  - <span data-ttu-id="3e095-108">**추적**:를 계산 하 고 평가 하는 프로세스의 통계 유효성을 모니터링 하는 동안 중간 결과 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="3e095-108">**Track**: Calculate and display interim results of the assessment while monitoring statistical validity of the process.</span></span> 
    
- <span data-ttu-id="3e095-109">**교육 및 추적 주기**</span><span class="sxs-lookup"><span data-stu-id="3e095-109">**Cycles of training and tracking**</span></span>
    
  - <span data-ttu-id="3e095-110">**태그**: 고급 eDiscovery (미리 보기)가 관련성 기준 전문가 반복 검토에 따라 각 문제에 특정 및 개별 파일의 태그 지정이 습득 합니다.</span><span class="sxs-lookup"><span data-stu-id="3e095-110">**Tag**: Advanced eDiscovery (Preview) learns Relevance criteria specific to each issue based on the expert's iterative review and tagging of individual files.</span></span>
    
  - <span data-ttu-id="3e095-111">**추적**:를 계산 하 고 모니터링 하는 프로세스의 통계 유효성을 검사 하는 동안 관련성 교육의 중간 결과 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="3e095-111">**Track**: Calculate and display interim results of the Relevance training while monitoring statistical validity of the process.</span></span> 
    
- <span data-ttu-id="3e095-112">**일괄 처리 계산**: 누적 및 습득 관련성 조건을 전체 파일 컬렉션에 적용 되 고 각 파일에 대 한 관련성 점수 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="3e095-112">**Batch calculation**: The accumulated and learned Relevance criteria is applied to the entire file collection, and a Relevance score is generated for each file.</span></span>
    
- <span data-ttu-id="3e095-113">**판단**: 전체 대/소문자에 적용 된 분석의 결과 일괄 처리 계산 후 표시 되 고 문서 검토 사항을 결정 하는 데 사용 되는 데이터가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="3e095-113">**Decide**: The results of the analysis applied to the entire case is displayed after Batch calculation, and data used to make document review decisions is displayed.</span></span>
    
- <span data-ttu-id="3e095-114">**테스트**: 유효성 및 고급 eDiscovery (미리 보기) 처리의 효과 확인 하는 결과 테스트할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3e095-114">**Test**: Results can be tested to verify the validity and effectiveness of the Advanced eDiscovery (Preview) processing.</span></span>

- <span data-ttu-id="3e095-115">**검색**: 작업 집합 내에서 쿼리를 실행 하는 경우 문제에 대 한 읽기 백분위 수의 문서와 같은 출력을 사용할 수 관련성 워크플로 완료 되 면 합니다.</span><span class="sxs-lookup"><span data-stu-id="3e095-115">**Search**: Once the Relevance workflow is complete, you can use the output such as read percentile of a document for your issue when you run a query within your working set.</span></span>
    
## <a name="guidelines-for-relevance-training-and-review"></a><span data-ttu-id="3e095-116">관련성 교육 및 검토에 대 한 지침</span><span class="sxs-lookup"><span data-stu-id="3e095-116">Guidelines for Relevance training and review</span></span>

<span data-ttu-id="3e095-117">다음은 관련성 교육 및 검토에 대 한 지침에 대 한 개요입니다.</span><span class="sxs-lookup"><span data-stu-id="3e095-117">Following is an overview of guidelines for Relevance training and review:</span></span>
  
- <span data-ttu-id="3e095-p102">**오류 및 불일치 항목**: 교육 하는 동안 태그 지정 오류가 있으면 오류를 수정 하려면 이전 파일 예제를 반환 합니다. 너무 많은 오류를 수정 중이거나 문제 확인 하는 경우의 새로운 측면이, 하는 경우 관련성 조건, 관리자가 다시 정의할 수 있어야 하 고 관련성 교육 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="3e095-p102">**Errors and inconsistencies**: If tagging errors are made during training, return to previous file samples to correct them. If there are too many errors to correct or there is a new perspective of the case or issue, the Relevance criteria should be redefined by the Administrator, and the Relevance training restarted.</span></span>
    
- <span data-ttu-id="3e095-120">**태그 지정 및 교육**:</span><span class="sxs-lookup"><span data-stu-id="3e095-120">**Tagging and training**:</span></span> 
    
  - <span data-ttu-id="3e095-p103">파일만 내용에 따라 태그가 지정 수 있어야 합니다. 더불어, 날짜 또는 파일 경로 등의 메타 데이터를 고려 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3e095-p103">Files should be tagged based on content only. Do not consider metadata, such as custodian, date, or file path.</span></span> 
    
  - <span data-ttu-id="3e095-123">파일에 태그를 지정 하는 경우 범위 오류 표시 텍스트의 날짜에 고려 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3e095-123">Do not consider date range indications in the text when tagging files.</span></span>
    
  - <span data-ttu-id="3e095-124">파일에 태그를 지정 하는 경우 포함 된 그래픽 이미지를 고려 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3e095-124">Do not consider embedded graphical images when tagging files.</span></span>
     
  - <span data-ttu-id="3e095-p104">무시 관련성에 관련성에 적용 되는 텍스트를 텍스트 보기에 표시 된 파일 내용을에서 제거 됩니다. 무시 텍스트에 대 한 값 시작 이미 교육 관련성 후 정의 된 경우 새 무시 텍스트는 이전에 정의 된 지점에서 작성 한 샘플 파일에 적용 됩니다. 텍스트를 무시 기능 사용 해야 신중 하 게, 해당 사용에는 파일 분석의 성능을 저하 시킬 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3e095-p104">Ignore text applied to Relevance will be removed in the displayed file content in the text view in Relevance. If the values for Ignore text were defined after Relevance training already started, the new ignored text will be applied to sample files created from the point in which it was defined. The Ignore Text feature should be used cautiously, as its use may reduce the performance of file analysis</span></span>
    
  - <span data-ttu-id="3e095-p105">필요한 경우에 **태그 지정을 건너뜁니다** 옵션을 사용 합니다. 에 건너뛴된 파일을 고급 eDiscovery (미리 보기)를 기반으로 교육지 않습니다. 평가에서 파일을 관련이 있는지 여부를 확인 하기 어려운 경우 하는 것이 태그 Relevant (R)로 여부 관련 (NR) **건너뛰기**를 선택 하는 대신 가능 합니다. 고급 eDiscovery (미리 보기) 교육 계산을 하는 경우 다음 볼 수 있습니다 이러한 종류의 파일 처리 된 얼마나 잘 합니다.</span><span class="sxs-lookup"><span data-stu-id="3e095-p105">Use the **Skip tagging** option only when necessary. Advanced eDiscovery (Preview) does not train based on skipped files. In assessment, if it's hard to tell whether a file is relevant, it is better to tag as Relevant (R) or Not relevant (NR) whenever possible rather than selecting **Skip**. When Advanced eDiscovery (Preview) evaluates training, it can then be seen how well these types of files were processed.</span></span>
    
  - <span data-ttu-id="3e095-132">매우 작은 양의 추출 된 텍스트에도 파일 "건너뛰기", 가능 하면가 아니라 R/NR 교육에 태그를 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="3e095-132">Even files with a very small amount of extracted text should be tagged in training as R/NR, rather than as "Skip", when possible.</span></span> 
    
  - <span data-ttu-id="3e095-133">태그 지정 영향을 줄 수 분류자도 파일을 읽을 수 및 R/NR으로 태그가 지정 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3e095-133">Tagging can impact the classifier as long as the file is readable and can be tagged as R/NR.</span></span>
    
  - <span data-ttu-id="3e095-134">**태그** 탭에 표시 된 예제 파일 목록에서 파일 시퀀스 번호는 파일의 원래 표시 된 순서를 반환할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3e095-134">The file sequence number on the displayed Sample files list on the **Tag** tab allows the user to return to the original displayed order of the files.</span></span> 
    
  - <span data-ttu-id="3e095-p106">모든 샘플으로 이동 하 고 평가 태그 지정을 변경 하 고 교육 파일을 설정 합니다. 다음 샘플을 만들 때 변경 내용이 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="3e095-p106">You can go back to any sample and change the tagging of the assessment and training set files. The changes will be applied when creating the next sample.</span></span>
    
  - <span data-ttu-id="3e095-137">PDF 형식으로 파일 해야 스캔 한 Excel 동일 하 게 취급 네이티브 Excel 파일 파일에 태그를 지정 하는 경우.</span><span class="sxs-lookup"><span data-stu-id="3e095-137">Scanned Excel files in PDF format should be treated the same as native Excel files when tagging files.</span></span>
    
  - <span data-ttu-id="3e095-p107">파일의 관련성 태그에 대 한 의심을 전문가 게 문의 합니다. 관련성 교육 하는 동안 잘못 된 태그 지정 하는 프로세스 뒷부분에 나오는 손실된 시간 종료 될 수 있습니다 하 고 전체 결과의 품질에 부정적인 영향을 설치 되어있을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3e095-p107">When in doubt regarding the Relevance tagging of a file, consult an expert. Incorrect tagging during the Relevance training can lead to lost time later in the process and may also have a negative impact on the quality of the overall results.</span></span>
    
  - <span data-ttu-id="3e095-140">키워드 정의 된 키워드의 목록에 태그를 지정 하는 동안 관련 파일을 식별 하는 사용자를 위해 색에 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="3e095-140">Keywords that were defined in Keyword lists will be displayed in colors to help the user identify relevant files while tagging.</span></span>
    
- <span data-ttu-id="3e095-p108">**일괄 처리 계산**: R/NR 전문가가 0 또는 100의 점수를 받게 됩니다으로 태그가 지정 된 파일입니다. 이 일괄 처리 계산 하기 전에 만든 태그 지정에 적용 됩니다. 전문가 일괄 처리 계산 후 문제를 유휴 상태로 전환 하이 문제에 태그 지정을 계속 하는 경우 0이 100/않으며 원래 점수 아니라 새로 태그가 지정 된 점수가 포함 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3e095-p108">**Batch calculation**: Files that were tagged as R/NR by the expert will receive a score of either 0 or 100. This applies to tagging made before Batch calculation. If the expert switched the issue to Idle after Batch Calculation and continued tagging this issue, the newly tagged scores will not be 100/0 but rather the original score.</span></span>
    
- <span data-ttu-id="3e095-144">**문제 및 샘플링 모드**: 문제는 일반적으로 해제 시간에 완료 되 면 (관련성 교육 안정은 및 일괄 처리 계산 수행 된) 문제는 취소 될 때 또는 문제에 다른 사용자가 작동 하는 경우.</span><span class="sxs-lookup"><span data-stu-id="3e095-144">**Issues and sampling mode**: Issues are usually turned Off when work on them is completed (Relevance training is stabilized and Batch calculation was performed), when the issues are canceled, or when another user is working on the issues.</span></span>
    
## <a name="steps-in-relevance-training"></a><span data-ttu-id="3e095-145">관련성 교육의 단계</span><span class="sxs-lookup"><span data-stu-id="3e095-145">Steps in Relevance training</span></span>

<span data-ttu-id="3e095-p109">**관련성 \> 추적** 탭, 고급 eDiscovery 권장 사항에는 다음 단계에 따라 다음 처리를 계속 하는 방법에 제공 합니다. 관련성 교육 프로세스에서 것이 좋습니다 각 다음 단계를 수행 하는 경우에 영향 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="3e095-p109">In the **Relevance \> Track** tab, Advanced eDiscovery provides recommendations on how to proceed in the processing, with the following next steps. The implications are described below when each of the following steps is recommended in the Relevance training process.</span></span> 
  
- <span data-ttu-id="3e095-148">태그 / 태그 지정을 계속: 파일 및 샘플 내에서 발급할 파일 검토 및 관련성 태그 각각에 대 한 전문가가 의해 수행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="3e095-148">Tagging / Continue tagging: File review and Relevance tagging performed by an expert for each file and issue within a sample.</span></span>
    
  - <span data-ttu-id="3e095-149">의미:는 기존 샘플 태그를 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="3e095-149">Implication: An existing sample needs to be tagged.</span></span>
    
- <span data-ttu-id="3e095-150">평가 평가 계속 /: 사례 문제 관련성의 초기 유효성을 검사 하 고 현재 사례에 대해 가져온 파일 모집단의 관련성의 예비 보기를 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3e095-150">Assessment / Continue assessment: Enables early validation of case issue relevance and a preliminary view of the relevance of the file population imported for the current case.</span></span>
    
  - <span data-ttu-id="3e095-151">의미: 더 많은 평가 필요 하거나 권장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="3e095-151">Implication: More assessment is required or recommended.</span></span>
    
- <span data-ttu-id="3e095-152">교육 / 교육 계속: 프로세스는 고급 하는 동안 파일에 태그 지정은 전문가가에서 eDiscovery 알아냅니다 샘플링 하 고 각각의 경우 컨텍스트 내에서 각 문제에 관련 된 관련성 조건을 식별 하는 능력을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="3e095-152">Training / Continue training: Process during which Advanced eDiscovery learns from the expert who is tagging the file samples and acquires the ability to identify Relevance criteria pertinent to each issue within the context of each case.</span></span>
    
  - <span data-ttu-id="3e095-153">의미: 문제 필요한 기타 교육; 다음 예제를 작성 하 고 태그를 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="3e095-153">Implication: The issue needs more training; the next sample should be created and tagged.</span></span> 
    
- <span data-ttu-id="3e095-p110">계산을 일괄 처리: 관련성 프로세스는 고급 설정의 eDiscovery 교육 단계 중에 얻은 정보를 가져와 파일 전체 모집단을 적용 합니다. 관련 파일 그룹의 모든 파일은 관련성에 대 한 평가 하 고 관련성 점수를 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="3e095-p110">Batch calculation: Relevance process in which Advanced eDiscovery takes the knowledge acquired during the training stage and applies it to the entire file population. All files in the pertinent file group are assessed for relevance and assigned a Relevance score.</span></span>
    
  - <span data-ttu-id="3e095-156">의미:이 문제를 될때까지, 및 일괄 처리 계산을 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3e095-156">Implication: The issue has stabilized, and Batch calculation can be performed.</span></span>
    
- <span data-ttu-id="3e095-157">후속 작업: 관련성 전문가가 검토 하 고 롤링 로드 하는 시나리오를 하는 동안 추가 파일 부하에서 선택한 파일의 샘플 태그를 지정 하는 경우를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="3e095-157">Catch-up: Relevance indicates when an expert reviews and tags a sample of files selected from an additional file load during a Rolling Loads scenario.</span></span>
    
  - <span data-ttu-id="3e095-158">의미: 새 부하에 추가한 후 및 후속 작업을 계속 하려면 반드시 입력 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="3e095-158">Implication: A new load has been added, and Catch-up is required to continue working.</span></span>
    
- <span data-ttu-id="3e095-159">불일치 항목에 태그 지정: 프로세스를 식별 하는 고급 eDiscovery 알고리즘을 통해 분석에 부정적인 영향을 줄 수 있는 프로세스에 태그를 지정 하는 파일의 일관성 오류입니다.</span><span class="sxs-lookup"><span data-stu-id="3e095-159">Tag inconsistencies: Process identifies, via an Advanced eDiscovery algorithm, inconsistencies in the file tagging process that may negatively impact the analysis.</span></span>
    
  - <span data-ttu-id="3e095-160">의미: 다음 예제는 이전 예제에서 태그가 지정 된 파일을 포함 됩니다 및 해당 태그 지정 다시 실행 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="3e095-160">Implication: The next sample will include files that have been tagged in previous samples, and their tagging must be redone.</span></span>
    
- <span data-ttu-id="3e095-161">분류자 업데이트: 태그 지정 또는 시드 변경 내용을 적용할 수 있도록 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="3e095-161">Update classifier: Allows the user to apply tagging or seeding changes.</span></span>
    
  - <span data-ttu-id="3e095-162">의미: 태그를 지정 하 고 변경 내용을 시드 적용할 수 수동으로 예제를 실행 하려면 다른 관련성을 작성할 필요 없이 합니다.</span><span class="sxs-lookup"><span data-stu-id="3e095-162">Implication: Tagging and seeding changes can be applied without needing to manually run another Relevance sample.</span></span>
    
- <span data-ttu-id="3e095-163">대기: The 관련성 교육 프로세스를 완료 합니다.</span><span class="sxs-lookup"><span data-stu-id="3e095-163">On hold: The Relevance training process is completed.</span></span>
    
  - <span data-ttu-id="3e095-164">의미: 없음 관련성 교육은 필요한이 시점입니다.</span><span class="sxs-lookup"><span data-stu-id="3e095-164">Implication: No Relevance training is required at this point.</span></span>
    
<span data-ttu-id="3e095-165">고급 eDiscovery 과정을 안내해를 사용 하는 프로세스와 각 단계에서 권장 되는 다음 단계를 있지만 수도 있습니다 탭 및 페이지 사이 탐색 하 고 문제, 개별 경우 관련 될 수 있는 주소 상황을 선택할 수 또는 문서 검토 프로세스입니다.</span><span class="sxs-lookup"><span data-stu-id="3e095-165">Although Advanced eDiscovery guides you through the process, with recommended Next steps at different stages, it also allows you to navigate between tabs and pages, and to make choices to address situations that may be pertinent to your individual case, issue, or document review process.</span></span> 
  
<span data-ttu-id="3e095-p111">그대로 사용 하거나 선택 항목을 처리 하는 고급 eDiscovery 다음 단계를 재정의 하는 것이 불가능 합니다. 권장된 다음 단계에서는 아닌 단계를 수행 합니다를 클릭 하는 경우 대화 상자에 표시 되는 확장 된 문제에에서 나열 된 **다음 단계** , 다음 단계 옆에 있는 **수정** 단추를 클릭 하 고 다른 다음 단계 옵션을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="3e095-p111">It is possible to accept or override Advanced eDiscovery Next step processing choices. If you want to perform a step other than the recommended Next step, click the **Next step** listed in the expanded issue display in the dialog, click the **Modify** button next to the Next step, and select another Next step option.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="3e095-168">일부 옵션으로 사용 하는 프로세스에서 해당 시점에 대 한 지원 되지 않습니다의 잠금을 해제 한 후 기능을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3e095-168">Some options may remain disabled after unlocking as they are not supported for use at that point in the process.</span></span> 
  
## <a name="more-information"></a><span data-ttu-id="3e095-169">추가 정보</span><span class="sxs-lookup"><span data-stu-id="3e095-169">More information</span></span>

[<span data-ttu-id="3e095-170">관련성에 이해 평가</span><span class="sxs-lookup"><span data-stu-id="3e095-170">Understanding Assessment in Relevance</span></span>](../assessment-in-relevance-in-advanced-ediscovery.md)
  
[<span data-ttu-id="3e095-171">태그 지정 및 평가</span><span class="sxs-lookup"><span data-stu-id="3e095-171">Tagging and Assessment</span></span>](../tagging-and-assessment-in-advanced-ediscovery.md)
  
[<span data-ttu-id="3e095-172">태그 지정 및 관련성 교육</span><span class="sxs-lookup"><span data-stu-id="3e095-172">Tagging and Relevance training</span></span>](../tagging-and-relevance-training-in-advanced-ediscovery.md)
  
[<span data-ttu-id="3e095-173">관련성 분석 추적</span><span class="sxs-lookup"><span data-stu-id="3e095-173">Tracking Relevance analysis</span></span>](../track-relevance-analysis-in-advanced-ediscovery.md)
  
[<span data-ttu-id="3e095-174">결과에 따라 결정</span><span class="sxs-lookup"><span data-stu-id="3e095-174">Deciding based on the results</span></span>](../decision-based-on-the-results-in-advanced-ediscovery.md)
  
[<span data-ttu-id="3e095-175">관련성 분석 테스트</span><span class="sxs-lookup"><span data-stu-id="3e095-175">Testing Relevance analysis</span></span>](../test-relevance-analysis-in-advanced-ediscovery.md)

[<span data-ttu-id="3e095-176">작업 집합 내에서 쿼리</span><span class="sxs-lookup"><span data-stu-id="3e095-176">Query within working set</span></span>](working-set-search.md)
