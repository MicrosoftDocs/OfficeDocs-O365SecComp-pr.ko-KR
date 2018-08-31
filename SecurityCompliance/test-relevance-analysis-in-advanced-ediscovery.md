---
title: Office 365 Advanced eDiscovery에서 관련성 분석 테스트
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
ms.assetid: 1b092f7c-ea55-44f5-b419-63f3458fd7e0
description: '탭을 사용 하는 테스트 Office 365 고급 eDiscovery의 일괄 처리 계산 후 테스트를 비교 하 고 처리의 전반적인 품질의 유효성을 검사 하는 방법에 알아봅니다.  '
ms.openlocfilehash: 782859fe3b6bb3d00945c477928131cd1154446d
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22533517"
---
# <a name="test-relevance-analysis-in-office-365-advanced-ediscovery"></a><span data-ttu-id="d0fe6-103">Office 365 Advanced eDiscovery에서 관련성 분석 테스트</span><span class="sxs-lookup"><span data-stu-id="d0fe6-103">Test Relevance analysis in Office 365 Advanced eDiscovery</span></span>

> [!NOTE]
> <span data-ttu-id="d0fe6-p101">고급 eDiscovery 조직에 대 한 고급 준수 추가 기능 또는 e 5 구독은 Office 365 E3 필요합니다. 해당 요금제에 가입한 상태 고급 eDiscovery 시도 하려는 하지 경우에 [Office 365 Enterprise e 5의 평가판 등록](https://go.microsoft.com/fwlink/p/?LinkID=698279)할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d0fe6-p101">Advanced eDiscovery requires an Office 365 E3 with the Advanced Compliance add-on or an E5 subscription for your organization. If you don't have that plan and want to try Advanced eDiscovery, you can [sign up for a trial of Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span></span> 
  
<span data-ttu-id="d0fe6-p102">고급 eDiscovery의 테스트 탭을 사용 하면 테스트, 비교, 및 처리의 전반적인 품질의 유효성을 검사 수 있습니다. 이러한 테스트에서는 일괄 처리 계산 후 수행 됩니다. 컬렉션에 있는 파일에 태그 지정 하면, 전문가가 각 태그가 지정 된 파일은 실제로 대/소문자와 관련이 있는지 여부에 대 한 최종 판단을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d0fe6-p102">The Test tab in Advanced eDiscovery enables you to test, compare, and validate the overall quality of processing. These tests are performed after Batch calculation. By tagging the files in the collection, an expert makes the final judgment about whether each tagged file is actually relevant to the case.</span></span> 
  
<span data-ttu-id="d0fe6-p103">단일 및 다중 문제 시나리오에서 테스트 문제 당 일반적으로 수행 됩니다. 각 테스트 한 후 결과 볼 수 및 테스트 결과 지정 된 샘플 테스트 파일을 다시 작동할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d0fe6-p103">In single and multiple-issue scenarios, tests are typically performed per issue. Results can be viewed after each test, and test results can be reworked with specified sample test files.</span></span>
  
## <a name="testing-the-rest"></a><span data-ttu-id="d0fe6-111">나머지 테스트</span><span class="sxs-lookup"><span data-stu-id="d0fe6-111">Testing the rest</span></span>

<span data-ttu-id="d0fe6-p104">예 선별 결정의 유효성을 검사 하려면, 고급 eDiscovery 최종 결과에 따라 특정 관련성 마감 점수 위에 파일을 검토 하려면 "나머지 테스트" 테스트 사용 됩니다. 해당 집합 내에서 관련 파일의 수를 계산할 선택한 마감 점수 아래에 있는 파일의 예제를 검토 하는 전문가입니다.</span><span class="sxs-lookup"><span data-stu-id="d0fe6-p104">The "Test the Rest" test is used to validate culling decisions, for example, to review only files above a specific Relevance cutoff score based on the final Advanced eDiscovery results. The expert reviews a sample of files under a selected cutoff score to evaluate the number of relevant files within that set.</span></span>
  
<span data-ttu-id="d0fe6-p105">이 테스트 나머지 모집단 통계 및 검토 집합과 테스트 간의 비교를 제공합니다. 검토 집합의 결과 교육 하는 동안 관련성으로 계산 합니다. 과 같은 계산에 따라 설정 및 입력된 매개 변수를 포함 하는 결과:</span><span class="sxs-lookup"><span data-stu-id="d0fe6-p105">This test provides statistics and a comparison between the Review set and the Test the Rest population. The results of the review set are those calculated by Relevance during Training. The results include calculations , based on settings and input parameters, such as:</span></span>
  
- <span data-ttu-id="d0fe6-117">샘플 및 식별 된 관련 파일에 파일의 수에 대 한 샘플 통계를 테스트 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0fe6-117">Test sample statistics of the number of files in a sample and identified relevant files.</span></span> 
    
- <span data-ttu-id="d0fe6-p106">테이블 형식 비교 검토 설정 하 고 나머지 부분에서는 파일, 수 등의 모집단 매개 변수 중 관련 파일, 예상된 풍부한 기능 및 관련 파일을 추가로 찾기 (영문)의 평균 운송 비용의 수를 예상 합니다. 관리자가 비용된 매개 변수 설정은 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d0fe6-p106">Tabular comparison of the Population parameters of the Review set and the Rest, for example, the number of files, estimated number of relevant files, estimated richness, and the average cost of finding an additional relevant file. Cost parameter settings can be set by the administrator.</span></span>
    
1. <span data-ttu-id="d0fe6-120">열기는 **관련성 \> 테스트** 탭 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0fe6-120">Open the **Relevance \> Test** tab.</span></span> 
    
2. <span data-ttu-id="d0fe6-p107">**테스트** 탭에서 **새로 만들기를 테스트**를 클릭 합니다. 다음 예제와 같이 **테스트 만들기** 대화 상자가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d0fe6-p107">In the **Test** tab, click **New test**. The **Create test** dialog is displayed, as shown in the following example.</span></span> 
    
    ![나머지 결과 테스트 하는 관련성](media/46e6898a-f929-4fd0-88d9-6f91d04b6ce2.png)
  
3. <span data-ttu-id="d0fe6-124">**테스트 이름**및 **설명**에 이름과 설명을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0fe6-124">In **Test name**, and **Description**, type the name and description.</span></span>
    
4. <span data-ttu-id="d0fe6-125">**테스트 유형** 목록에서 **나머지 테스트** 를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0fe6-125">In the **Test type** list, select **Test the Rest**</span></span>
    
5. <span data-ttu-id="d0fe6-126">에 **문제 / 범주** 목록에서 문제 이름을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0fe6-126">In the **Issue / Category** list, select the issue name.</span></span> 
    
6. <span data-ttu-id="d0fe6-127">**로드** 목록에서 부하를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0fe6-127">In the **Load** list, select the load.</span></span> 
    
7. <span data-ttu-id="d0fe6-128">**읽기 %** 기본값을 그대로 적용 하거나 마감 관련성 점수에 대 한 값을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0fe6-128">In **Read %**, accept the default value or select a value for the cutoff Relevance score.</span></span> 
    
8. <span data-ttu-id="d0fe6-p108">**크기를 설정**하거나 기본값을 그대로 사용 합니다. 참고 복원 아이콘의 기본값을 복원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0fe6-p108">In **Set size**, or accept the default value. Note that the restore icons will restore the default values.</span></span>
    
9. <span data-ttu-id="d0fe6-p109">**태그 지정을 시작**을 클릭 합니다. 테스트 샘플 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d0fe6-p109">Click **Start tagging**. A test sample is generated.</span></span>
    
10. <span data-ttu-id="d0fe6-133">검토 하 고 태그를 지정 된 각 파일에는 **관련성 \> 태그** 탭 및 작업을 마치면 **계산**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0fe6-133">Review and tag each of the files in the **Relevance \> Tag** tab and when done, click **Calculate**.</span></span>
    
11. <span data-ttu-id="d0fe6-p110">테스트 탭에서 테스트 결과 볼 수 있는 **결과 보기를** 클릭 수 있습니다. 예는 다음 그림에 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d0fe6-p110">In the Test tab, you can click **View results** to see the test results. An example is shown in the following figure.</span></span> 
    
    ![나머지 결과 테스트 합니다.](media/b95744a9-047d-4c29-992d-04fa7e58e58a.png)
  
<span data-ttu-id="d0fe6-137">위의 그림 테이블의 **샘플 매개** 변수 섹션은 전문가 태그가 지정 된 샘플에서 파일의 수 및 해당 샘플에 있는 관련 파일의 수에 대 한 세부 정보를 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0fe6-137">In the figure above, the **Sample parameters** section of the table contains details about the number of files in the sample tagged by the expert, and the number of relevant files found in that sample.</span></span> 
  
<span data-ttu-id="d0fe6-p111">테이블의 **모집단 매개** 변수 섹션에는 선택한 구분 아래 점수가 포함 된 파일의 검토 집합 모집단 및 선택한 구분 위에 점수와 함께 파일, 000 명의 "The 나머지"를 포함 하는 테스트 결과 포함 합니다. 각 모집단에 대 한 다음과 같은 결과가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d0fe6-p111">The **Population parameters** section of the table contains the test results, including the Review set population of files with a score below the selected cutoff and "The Rest" population of files with a score above the selected cutoff. For each population, the following results are displayed:</span></span> 
  
- <span data-ttu-id="d0fe6-140">읽기 %-명시 된 구분을 가진 파일이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d0fe6-140">Includes files with read % - Stated cutoff</span></span>
    
- <span data-ttu-id="d0fe6-141">파일의 총 수</span><span class="sxs-lookup"><span data-stu-id="d0fe6-141">The total number of files</span></span> 
    
- <span data-ttu-id="d0fe6-142">관련 파일의 예상된 수</span><span class="sxs-lookup"><span data-stu-id="d0fe6-142">The estimated number of relevant files</span></span> 
    
- <span data-ttu-id="d0fe6-143">예상된 풍부한 기능</span><span class="sxs-lookup"><span data-stu-id="d0fe6-143">The estimated richness</span></span> 
    
- <span data-ttu-id="d0fe6-144">다른 관련 파일 찾기 (영문)의 평균 검토 비용</span><span class="sxs-lookup"><span data-stu-id="d0fe6-144">The average review cost of finding another relevant file</span></span>
    
## <a name="testing-the-slice"></a><span data-ttu-id="d0fe6-145">해당 조각의 테스트</span><span class="sxs-lookup"><span data-stu-id="d0fe6-145">Testing the slice</span></span>

<span data-ttu-id="d0fe6-146">"테스트는 슬라이스" 테스트 "테스트의 나머지 부분에"와 유사한 테스트를 수행 테스트, 하지만 관련성 읽기 %에 의해 지정 된 파일의 세그먼트를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0fe6-146">The "Test the Slice" test performs testing similar to the "Test the Rest" test, but to a segment of the file set as specified by Relevance Read %.</span></span>
  
1. <span data-ttu-id="d0fe6-147">열기는 **관련성 \> 테스트** 탭 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0fe6-147">Open the **Relevance \> Test** tab.</span></span> 
    
2. <span data-ttu-id="d0fe6-p112">**테스트** 탭에서 **새로 만들기를 테스트**를 클릭 합니다. **테스트 만들기** 대화 상자가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d0fe6-p112">In the **Test** tab, click **New test**. The **Create test** dialog is displayed.</span></span> 
    
3. <span data-ttu-id="d0fe6-150">**테스트 이름** 및 **설명**정보를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0fe6-150">In **Test name** and **Description**, type the information.</span></span>
    
4. <span data-ttu-id="d0fe6-151">**테스트 유형** 목록에서 **해당 조각의 테스트**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0fe6-151">In the **Test type** list, select **Test the Slice**.</span></span>
    
5. <span data-ttu-id="d0fe6-152">**문제** 목록에서 문제 이름을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0fe6-152">In the **Issue** list, select the issue name.</span></span> 
    
6. <span data-ttu-id="d0fe6-153">**로드** 목록에서 부하를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0fe6-153">In the **Load** list, select the load.</span></span> 
    
7. <span data-ttu-id="d0fe6-154">**읽기 % 사이**기본 낮은 및 높은 범위 값 이나 구분 관련성 점수에 대 한 값을 선택할를 그대로 둡니다.</span><span class="sxs-lookup"><span data-stu-id="d0fe6-154">In **Read % between**, accept the default low and high range values or select values for the cutoff Relevance scores.</span></span> 
    
8. <span data-ttu-id="d0fe6-155">**크기를 설정**에서 값을 선택 하거나 기본값을 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0fe6-155">In **Set size**, select a value or accept the default value.</span></span>
    
    <span data-ttu-id="d0fe6-156">복원 아이콘은 기본값을 복원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0fe6-156">The restore icons will restore the default value.</span></span>
    
9. <span data-ttu-id="d0fe6-p113">**태그 지정을 시작**을 클릭 합니다. 테스트 샘플 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d0fe6-p113">Click **Start tagging**. A test sample is generated.</span></span>
    
10. <span data-ttu-id="d0fe6-159">검토 하 고 태그를 지정 된 각 파일에는 **관련성 \> 태그** 탭 및 작업을 마치면 **계산**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0fe6-159">Review and tag each of the files in the **Relevance \> Tag** tab and when done, click **Calculate**.</span></span> 
    
11. <span data-ttu-id="d0fe6-160">테스트 탭에서 테스트 결과 볼 수 있는 **결과 보기를** 클릭 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d0fe6-160">In the Test tab, you can click **View results** to see the test results.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="d0fe6-161">참고 항목</span><span class="sxs-lookup"><span data-stu-id="d0fe6-161">See also</span></span>

[<span data-ttu-id="d0fe6-162">Office 365 Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="d0fe6-162">Office 365 Advanced eDiscovery</span></span>](office-365-advanced-ediscovery.md)
  
[<span data-ttu-id="d0fe6-163">관련성에 이해 평가</span><span class="sxs-lookup"><span data-stu-id="d0fe6-163">Understanding Assessment in Relevance</span></span>](assessment-in-relevance-in-advanced-ediscovery.md)
  
[<span data-ttu-id="d0fe6-164">태그 지정 및 평가</span><span class="sxs-lookup"><span data-stu-id="d0fe6-164">Tagging and Assessment</span></span>](tagging-and-assessment-in-advanced-ediscovery.md)
  
[<span data-ttu-id="d0fe6-165">태그 지정 및 관련성 교육</span><span class="sxs-lookup"><span data-stu-id="d0fe6-165">Tagging and Relevance training</span></span>](tagging-and-relevance-training-in-advanced-ediscovery.md)
  
[<span data-ttu-id="d0fe6-166">관련성 분석 추적</span><span class="sxs-lookup"><span data-stu-id="d0fe6-166">Tracking Relevance analysis</span></span>](track-relevance-analysis-in-advanced-ediscovery.md)
  
[<span data-ttu-id="d0fe6-167">결과에 따라 결정</span><span class="sxs-lookup"><span data-stu-id="d0fe6-167">Deciding based on the results</span></span>](decision-based-on-the-results-in-advanced-ediscovery.md)

