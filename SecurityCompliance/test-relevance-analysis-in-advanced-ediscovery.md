---
title: Office 365 Advanced eDiscovery에서 관련성 분석 테스트
ms.author: chrfox
author: chrfox
manager: laurawi
ms.date: 9/14/2017
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: 1b092f7c-ea55-44f5-b419-63f3458fd7e0
description: 'Office 365 Advanced eDiscovery의 일괄 계산 후 테스트 탭을 사용 하 여 전체 처리 품질을 테스트 및 비교 하 고 유효성 검사를 수행 하는 방법에 대해 알아봅니다.  '
ms.openlocfilehash: 984a7b3f8088604aca235a1caf60bb67b5471499
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/17/2019
ms.locfileid: "34158310"
---
# <a name="test-relevance-analysis-in-office-365-advanced-ediscovery"></a><span data-ttu-id="c17bb-103">Office 365 Advanced eDiscovery에서 관련성 분석 테스트</span><span class="sxs-lookup"><span data-stu-id="c17bb-103">Test Relevance analysis in Office 365 Advanced eDiscovery</span></span>

> [!NOTE]
> <span data-ttu-id="c17bb-p101">Advanced eDiscovery를 사용하려면 Office 365 E3의 고급 준수 추가 기능이나 조직을 위한 E5 구독이 필요합니다. 이 요금제가 없는 상태에서 Advanced eDiscovery를 사용하려는 경우에는 [Office 365 Enterprise E5 평가판을 등록](https://go.microsoft.com/fwlink/p/?LinkID=698279)할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c17bb-p101">Advanced eDiscovery requires an Office 365 E3 with the Advanced Compliance add-on or an E5 subscription for your organization. If you don't have that plan and want to try Advanced eDiscovery, you can [sign up for a trial of Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span></span> 
  
<span data-ttu-id="c17bb-106">고급 eDiscovery의 테스트 탭에서는 전체 처리 품질을 테스트 및 비교 하 고 유효성을 검사할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c17bb-106">The Test tab in Advanced eDiscovery enables you to test, compare, and validate the overall quality of processing.</span></span> <span data-ttu-id="c17bb-107">이러한 테스트는 일괄 계산 후에 수행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c17bb-107">These tests are performed after Batch calculation.</span></span> <span data-ttu-id="c17bb-108">전문가는 컬렉션의 파일에 태그를 지정 하 여 태그 있는 각 파일이 실제로 대/소문자와 관련성이 있는지 여부를 최종 판단 합니다.</span><span class="sxs-lookup"><span data-stu-id="c17bb-108">By tagging the files in the collection, an expert makes the final judgment about whether each tagged file is actually relevant to the case.</span></span> 
  
<span data-ttu-id="c17bb-109">단일 및 다중 문제 시나리오에서는 일반적으로 각 문제와 관련 된 테스트를 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="c17bb-109">In single and multiple-issue scenarios, tests are typically performed per issue.</span></span> <span data-ttu-id="c17bb-110">각 테스트 후에 결과를 볼 수 있으며, 지정 된 샘플 테스트 파일을 사용 하 여 테스트 결과를 다시 수정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c17bb-110">Results can be viewed after each test, and test results can be reworked with specified sample test files.</span></span>
  
## <a name="testing-the-rest"></a><span data-ttu-id="c17bb-111">나머지 테스트</span><span class="sxs-lookup"><span data-stu-id="c17bb-111">Testing the rest</span></span>

<span data-ttu-id="c17bb-112">"Rest 테스트" 테스트를 통해 최종 고급 eDiscovery 결과를 기준으로 특정 관련성 구분 점수 위에 있는 파일만 검토 하는 등의 culling 의사 결정을 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c17bb-112">The "Test the Rest" test is used to validate culling decisions, for example, to review only files above a specific Relevance cutoff score based on the final Advanced eDiscovery results.</span></span> <span data-ttu-id="c17bb-113">전문가는 선택한 구분 점수 아래의 파일 샘플을 검토 하 여 해당 집합 내의 관련 파일 수를 평가 합니다.</span><span class="sxs-lookup"><span data-stu-id="c17bb-113">The expert reviews a sample of files under a selected cutoff score to evaluate the number of relevant files within that set.</span></span>
  
<span data-ttu-id="c17bb-114">이 테스트에서는 검토 집합 간 통계 및 비교를 제공 하 고 나머지 채우기를 테스트 합니다.</span><span class="sxs-lookup"><span data-stu-id="c17bb-114">This test provides statistics and a comparison between the Review set and the Test the Rest population.</span></span> <span data-ttu-id="c17bb-115">검토 집합의 결과는 교육 중에 관련성에 따라 계산 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c17bb-115">The results of the review set are those calculated by Relevance during Training.</span></span> <span data-ttu-id="c17bb-116">결과에는 다음과 같은 설정 및 입력 매개 변수에 따른 계산이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c17bb-116">The results include calculations , based on settings and input parameters, such as:</span></span>
  
- <span data-ttu-id="c17bb-117">샘플 및 식별 된 관련 파일의 파일 수에 대 한 샘플 통계를 테스트 합니다.</span><span class="sxs-lookup"><span data-stu-id="c17bb-117">Test sample statistics of the number of files in a sample and identified relevant files.</span></span> 
    
- <span data-ttu-id="c17bb-118">테이블 형식 및 검토 집합의 인구 매개 변수와 나머지 부분 (예: 파일 수, 예상 되는 관련 파일의 수, 예상 되는 다양성, 추가 관련 파일을 찾는 데 걸리는 평균 비용)을 비교 합니다.</span><span class="sxs-lookup"><span data-stu-id="c17bb-118">Tabular comparison of the Population parameters of the Review set and the Rest, for example, the number of files, estimated number of relevant files, estimated richness, and the average cost of finding an additional relevant file.</span></span> <span data-ttu-id="c17bb-119">Cost 매개 변수 설정은 관리자가 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c17bb-119">Cost parameter settings can be set by the administrator.</span></span>
    
1. <span data-ttu-id="c17bb-120">**관련성 \> 테스트** 탭을 엽니다.</span><span class="sxs-lookup"><span data-stu-id="c17bb-120">Open the **Relevance \> Test** tab.</span></span> 
    
2. <span data-ttu-id="c17bb-121">**테스트** 탭에서 **새 테스트**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="c17bb-121">In the **Test** tab, click **New test**.</span></span> <span data-ttu-id="c17bb-122">다음 예와 같이 **테스트 만들기** 대화 상자가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c17bb-122">The **Create test** dialog is displayed, as shown in the following example.</span></span> 
    
    ![나머지 결과 테스트 하는 관련성](media/46e6898a-f929-4fd0-88d9-6f91d04b6ce2.png)
  
3. <span data-ttu-id="c17bb-124">**테스트 이름**및 **설명**에 이름과 설명을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="c17bb-124">In **Test name**, and **Description**, type the name and description.</span></span>
    
4. <span data-ttu-id="c17bb-125">**테스트 유형** 목록에서 **나머지 테스트를 선택 합니다** .</span><span class="sxs-lookup"><span data-stu-id="c17bb-125">In the **Test type** list, select **Test the Rest**</span></span>
    
5. <span data-ttu-id="c17bb-126">**문제/범주** 목록에서 문제점 이름을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="c17bb-126">In the **Issue / Category** list, select the issue name.</span></span> 
    
6. <span data-ttu-id="c17bb-127">**로드** 목록에서 부하를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="c17bb-127">In the **Load** list, select the load.</span></span> 
    
7. <span data-ttu-id="c17bb-128">**읽기%** 에서 기본값을 수락 하거나 구분 기준 점수 매기기 값을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="c17bb-128">In **Read %**, accept the default value or select a value for the cutoff Relevance score.</span></span> 
    
8. <span data-ttu-id="c17bb-129">**설정**하거나 기본값을 그대로 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="c17bb-129">In **Set size**, or accept the default value.</span></span> <span data-ttu-id="c17bb-130">복원 아이콘은 기본값을 복원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c17bb-130">Note that the restore icons will restore the default values.</span></span>
    
9. <span data-ttu-id="c17bb-131">**태그 지정 시작**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="c17bb-131">Click **Start tagging**.</span></span> <span data-ttu-id="c17bb-132">테스트 샘플이 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c17bb-132">A test sample is generated.</span></span>
    
10. <span data-ttu-id="c17bb-133">\*\* \> 관련성 태그\*\* 탭에서 각 파일을 검토 하 고 태그를 만들었으면 완료 되 면 **계산**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="c17bb-133">Review and tag each of the files in the **Relevance \> Tag** tab and when done, click **Calculate**.</span></span>
    
11. <span data-ttu-id="c17bb-134">테스트 탭에서 **결과 보기** 를 클릭 하 여 테스트 결과를 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c17bb-134">In the Test tab, you can click **View results** to see the test results.</span></span> <span data-ttu-id="c17bb-135">다음 그림에 예가 나와 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c17bb-135">An example is shown in the following figure.</span></span> 
    
    ![나머지 결과 테스트 합니다.](media/b95744a9-047d-4c29-992d-04fa7e58e58a.png)
  
<span data-ttu-id="c17bb-137">위 그림에서 표의 **샘플 매개 변수** 섹션에는 전문가가 태그를 지정 하는 샘플의 파일 수와 해당 예제에 나와 있는 관련 파일의 수에 대 한 자세한 정보가 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c17bb-137">In the figure above, the **Sample parameters** section of the table contains details about the number of files in the sample tagged by the expert, and the number of relevant files found in that sample.</span></span> 
  
<span data-ttu-id="c17bb-138">테이블의 **인구 매개 변수** 섹션에는 선택한 구분 아래에 점수가 있는 파일의 검토 집합 및 선택한 구분 위에 점수가 있는 파일의 "나머지"를 포함 하는 테스트 결과가 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c17bb-138">The **Population parameters** section of the table contains the test results, including the Review set population of files with a score below the selected cutoff and "The Rest" population of files with a score above the selected cutoff.</span></span> <span data-ttu-id="c17bb-139">각 모집단에 대해 다음 결과가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c17bb-139">For each population, the following results are displayed:</span></span> 
  
- <span data-ttu-id="c17bb-140">% 규정 된 읽기 전용 구분이 있는 파일 포함</span><span class="sxs-lookup"><span data-stu-id="c17bb-140">Includes files with read % - Stated cutoff</span></span>
    
- <span data-ttu-id="c17bb-141">총 파일 수</span><span class="sxs-lookup"><span data-stu-id="c17bb-141">The total number of files</span></span> 
    
- <span data-ttu-id="c17bb-142">예상 되는 관련 파일의 수</span><span class="sxs-lookup"><span data-stu-id="c17bb-142">The estimated number of relevant files</span></span> 
    
- <span data-ttu-id="c17bb-143">예측 된 다양성</span><span class="sxs-lookup"><span data-stu-id="c17bb-143">The estimated richness</span></span> 
    
- <span data-ttu-id="c17bb-144">다른 관련 파일을 찾기 위한 평균 검토 비용</span><span class="sxs-lookup"><span data-stu-id="c17bb-144">The average review cost of finding another relevant file</span></span>
    
## <a name="testing-the-slice"></a><span data-ttu-id="c17bb-145">조각 테스트</span><span class="sxs-lookup"><span data-stu-id="c17bb-145">Testing the slice</span></span>

<span data-ttu-id="c17bb-146">"조각 테스트" 테스트는 "Rest 테스트" 테스트와 비슷한 테스트를 수행 하지만 관련성 읽기%로 지정 된 파일 집합의 세그먼트에 해당 합니다.</span><span class="sxs-lookup"><span data-stu-id="c17bb-146">The "Test the Slice" test performs testing similar to the "Test the Rest" test, but to a segment of the file set as specified by Relevance Read %.</span></span>
  
1. <span data-ttu-id="c17bb-147">**관련성 \> 테스트** 탭을 엽니다.</span><span class="sxs-lookup"><span data-stu-id="c17bb-147">Open the **Relevance \> Test** tab.</span></span> 
    
2. <span data-ttu-id="c17bb-148">**테스트** 탭에서 **새 테스트**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="c17bb-148">In the **Test** tab, click **New test**.</span></span> <span data-ttu-id="c17bb-149">**테스트 만들기** 대화 상자가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c17bb-149">The **Create test** dialog is displayed.</span></span> 
    
3. <span data-ttu-id="c17bb-150">**테스트 이름** 및 **설명**에 정보를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="c17bb-150">In **Test name** and **Description**, type the information.</span></span>
    
4. <span data-ttu-id="c17bb-151">**테스트 유형** 목록에서 **조각 테스트**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="c17bb-151">In the **Test type** list, select **Test the Slice**.</span></span>
    
5. <span data-ttu-id="c17bb-152">**문제점** 목록에서 문제점 이름을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="c17bb-152">In the **Issue** list, select the issue name.</span></span> 
    
6. <span data-ttu-id="c17bb-153">**로드** 목록에서 부하를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="c17bb-153">In the **Load** list, select the load.</span></span> 
    
7. <span data-ttu-id="c17bb-154">다음 **사이에 읽기%** 에서 기본 하한값 및 high 범위 값을 적용 하거나 값 구분 점수를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="c17bb-154">In **Read % between**, accept the default low and high range values or select values for the cutoff Relevance scores.</span></span> 
    
8. <span data-ttu-id="c17bb-155">**크기 설정**에서 값을 선택 하거나 기본값을 그대로 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="c17bb-155">In **Set size**, select a value or accept the default value.</span></span>
    
    <span data-ttu-id="c17bb-156">복원 아이콘은 기본값을 복원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c17bb-156">The restore icons will restore the default value.</span></span>
    
9. <span data-ttu-id="c17bb-157">**태그 지정 시작**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="c17bb-157">Click **Start tagging**.</span></span> <span data-ttu-id="c17bb-158">테스트 샘플이 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c17bb-158">A test sample is generated.</span></span>
    
10. <span data-ttu-id="c17bb-159">\*\* \> 관련성 태그\*\* 탭에서 각 파일을 검토 하 고 태그를 만들었으면 완료 되 면 **계산**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="c17bb-159">Review and tag each of the files in the **Relevance \> Tag** tab and when done, click **Calculate**.</span></span> 
    
11. <span data-ttu-id="c17bb-160">테스트 탭에서 **결과 보기** 를 클릭 하 여 테스트 결과를 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c17bb-160">In the Test tab, you can click **View results** to see the test results.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="c17bb-161">참고 항목</span><span class="sxs-lookup"><span data-stu-id="c17bb-161">See also</span></span>

[<span data-ttu-id="c17bb-162">Office 365 Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="c17bb-162">Office 365 Advanced eDiscovery</span></span>](office-365-advanced-ediscovery.md)
  
[<span data-ttu-id="c17bb-163">관련성 평가 이해</span><span class="sxs-lookup"><span data-stu-id="c17bb-163">Understanding Assessment in Relevance</span></span>](assessment-in-relevance-in-advanced-ediscovery.md)
  
[<span data-ttu-id="c17bb-164">태그 지정 및 평가</span><span class="sxs-lookup"><span data-stu-id="c17bb-164">Tagging and Assessment</span></span>](tagging-and-assessment-in-advanced-ediscovery.md)
  
[<span data-ttu-id="c17bb-165">태그 지정 및 관련성 교육</span><span class="sxs-lookup"><span data-stu-id="c17bb-165">Tagging and Relevance training</span></span>](tagging-and-relevance-training-in-advanced-ediscovery.md)
  
[<span data-ttu-id="c17bb-166">관련성 분석 추적</span><span class="sxs-lookup"><span data-stu-id="c17bb-166">Tracking Relevance analysis</span></span>](track-relevance-analysis-in-advanced-ediscovery.md)
  
[<span data-ttu-id="c17bb-167">결과를 기준으로 결정</span><span class="sxs-lookup"><span data-stu-id="c17bb-167">Deciding based on the results</span></span>](decision-based-on-the-results-in-advanced-ediscovery.md)

