---
title: Office 365 Advanced eDiscovery의 결과를 기반으로 결정
ms.author: chrfox
author: chrfox
manager: laurawi
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: aed65bcd-0a4f-43e9-b5e5-b98cc376bdf8
description: 'Office 365 Advanced eDiscovery의 결정 탭에서 사례 파일의 검토 집합에 대 한 올바른 크기를 결정 하는 데 도움이 되는 데이터를 제공 하는 방법에 대해 알아봅니다. '
ms.openlocfilehash: a9250a45129320517f96b9a335db95d164d2dae7
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32257824"
---
# <a name="decision-based-on-the-results-in-office-365-advanced-ediscovery"></a><span data-ttu-id="2f916-103">Office 365 Advanced eDiscovery의 결과를 기반으로 결정</span><span class="sxs-lookup"><span data-stu-id="2f916-103">Decision based on the results in Office 365 Advanced eDiscovery</span></span>

> [!NOTE]
> <span data-ttu-id="2f916-p101">Advanced eDiscovery를 사용하려면 Office 365 E3의 고급 준수 추가 기능이나 조직을 위한 E5 구독이 필요합니다. 이 요금제가 없는 상태에서 Advanced eDiscovery를 사용하려는 경우에는 [Office 365 Enterprise E5 평가판을 등록](https://go.microsoft.com/fwlink/p/?LinkID=698279)할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2f916-p101">Advanced eDiscovery requires an Office 365 E3 with the Advanced Compliance add-on or an E5 subscription for your organization. If you don't have that plan and want to try Advanced eDiscovery, you can [sign up for a trial of Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span></span> 
  
 <span data-ttu-id="2f916-106">고급 eDiscovery에서 결정 탭은 사례 파일의 검토 집합 크기를 결정 하는 데 필요한 의사 결정 통계를 보고 사용 하는 데 필요한 추가 정보를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="2f916-106">In Advanced eDiscovery, the Decide tab provides additional information for viewing and using decision-support statistics for determining the size of the review set of case files.</span></span> 
  
## <a name="using-the-decide-tab"></a><span data-ttu-id="2f916-107">결정 탭 사용</span><span class="sxs-lookup"><span data-stu-id="2f916-107">Using the Decide tab</span></span>

![관련성을 결정](media/f32fed89-f3b5-404a-90c7-ea25d2eb58a9.png)
  
<span data-ttu-id="2f916-109">이 탭에는 다음 항목이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="2f916-109">This tab includes the following:</span></span>
  
- <span data-ttu-id="2f916-110">**문제**: 여기서 필요한 문제를 목록에서 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2f916-110">**Issue**: From here, you can select the issue of interest from the list.</span></span> 
    
- <span data-ttu-id="2f916-111">**검토-회수 비율**: 관련성 성적에 따른 고급 eDiscovery 검토의 비교입니다.</span><span class="sxs-lookup"><span data-stu-id="2f916-111">**Review-recall ratio**: Comparison of Advanced eDiscovery review according to Relevance scores.</span></span> <span data-ttu-id="2f916-112">차트의 구분 지점은 검토 중 이며 관련성 점수에 매핑되는 파일의 비율을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="2f916-112">The Cutoff point in the chart represents the percentage of files to review, mapped to a Relevance score.</span></span> <span data-ttu-id="2f916-113">이는 관련성 테스트 단계 및 culling의 내보내기 임계값으로 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="2f916-113">This is used in the Relevance Test phase and as an Export threshold for culling.</span></span> <span data-ttu-id="2f916-114">검토할 파일 수에 대 한 기본 구분 지점은 재호출 및 정밀도 간의 균형이 가장 적합 한 시점입니다.</span><span class="sxs-lookup"><span data-stu-id="2f916-114">The default cutoff point, for the number of files to review is at the point in which the balance between Recall and Precision is optimal.</span></span> <span data-ttu-id="2f916-115">실제 구분 지점은 목표 및 비용 급여 (% review) 및 위험 (% 회수)에 따라 사용자가 결정 해야 합니다. 슬라이더를 사용 하 여 구분 지점을 조정 하 고 그래프 및 매개 변수에 대 한 영향을 확인 하 고, 검색할 관련 파일의 비율을 조정 하 고, 의사 결정을 확인 하기 전에 결과를 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2f916-115">The actual cutoff point should be determined by the user depending on objectives and the cost tradeoff (%review) and risk (%recall).Using the slider, you can adjust the cutoff point and see the effect on the graph and parameters, when adjusting the percent of relevant files to be retrieved, and before validating a decision.</span></span>
    
- <span data-ttu-id="2f916-116">**매개 변수**: review, 회수, Next 관련성이 있는 and Total cost 매개 변수는 전체 사례에 대 한 컬렉션과 관련 하 여 검토 집합과 관련 된 누적 계산 통계입니다.</span><span class="sxs-lookup"><span data-stu-id="2f916-116">**Parameters**: Review, Recall, Next relevant and Total cost parameters are cumulative calculated statistics pertaining to the review set in relation to the collection for the entire case.</span></span> <span data-ttu-id="2f916-117">이러한 매개 변수에 대 한 정의는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="2f916-117">Definitions for these parameters are as follows:</span></span>
    
    <span data-ttu-id="2f916-118">**검토**:이 구분에 따라 검토할 파일의 비율입니다.</span><span class="sxs-lookup"><span data-stu-id="2f916-118">**Review**: Percentage of files to review based on this cutoff.</span></span> 
    
    <span data-ttu-id="2f916-119">**회수**: 검토 집합에서 관련 파일의 비율입니다.</span><span class="sxs-lookup"><span data-stu-id="2f916-119">**Recall**: Percentage of relevant files in the review set.</span></span> 
    
    <span data-ttu-id="2f916-120">**다음 관련**: 현재 검토 집합에 없는 추가 관련 파일을 검토 하 고 식별 하는 비용입니다.</span><span class="sxs-lookup"><span data-stu-id="2f916-120">**Next relevant**: Cost to review and identify an additional relevant file that is not currently in the review set.</span></span> 
    
    <span data-ttu-id="2f916-121">**총 비용**: 사례 파일의 비율을 검토 하기 위한 비용입니다.</span><span class="sxs-lookup"><span data-stu-id="2f916-121">**Total cost**: Cost for reviewing this percentage of the case files.</span></span> <span data-ttu-id="2f916-122">Cost 매개 변수 설정은 사례 관리자가 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2f916-122">Cost parameter settings can be set by the Case manager.</span></span>
    
- <span data-ttu-id="2f916-123">**관련성 점수를 통한 배포**: 어두운 회색 왼쪽에 표시 되는 파일은 컷오프 점수 아래에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2f916-123">**Distribution by relevance score**: Files in the dark gray display to the left are below the cutoff score.</span></span> <span data-ttu-id="2f916-124">도구-팁에는 총 파일을 기준으로 하 여 검토 파일에 설정 된 파일의 관련성 점수와 관련 백분율이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="2f916-124">A tool-tip displays the Relevance score and the related percentage of files in the review file set in relation to the total files.</span></span>
    
<span data-ttu-id="2f916-125">상세 세부 정보 창에 추가 정보가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="2f916-125">The expanded Details pane displays additional details.</span></span> <span data-ttu-id="2f916-126">컬렉션 그림의 파일에는 빈 파일 또는 ne문서 ou 파일이 포함 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2f916-126">Files in collection figures do not include empty or nebulous files.</span></span> <span data-ttu-id="2f916-127">패밀리 파일 그림은 관련성이 없지만 여전히 패밀리의 일부로 서 계산 되는 파일을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="2f916-127">Family files figures represent files that are not loaded in Relevance, yet still counted as part of the family.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="2f916-128">참고 항목</span><span class="sxs-lookup"><span data-stu-id="2f916-128">See also</span></span>

[<span data-ttu-id="2f916-129">Office 365 Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="2f916-129">Office 365 Advanced eDiscovery</span></span>](office-365-advanced-ediscovery.md)
  
[<span data-ttu-id="2f916-130">관련성 평가 이해</span><span class="sxs-lookup"><span data-stu-id="2f916-130">Understanding Assessment in Relevance</span></span>](assessment-in-relevance-in-advanced-ediscovery.md)
  
[<span data-ttu-id="2f916-131">태그 지정 및 평가</span><span class="sxs-lookup"><span data-stu-id="2f916-131">Tagging and Assessment</span></span>](tagging-and-relevance-training-in-advanced-ediscovery.md)
  
[<span data-ttu-id="2f916-132">관련성 교육 수행</span><span class="sxs-lookup"><span data-stu-id="2f916-132">Performing Relevance training</span></span>](tagging-and-assessment-in-advanced-ediscovery.md)
  
[<span data-ttu-id="2f916-133">관련성 분석 추적</span><span class="sxs-lookup"><span data-stu-id="2f916-133">Tracking Relevance analysis</span></span>](track-relevance-analysis-in-advanced-ediscovery.md)
  
[<span data-ttu-id="2f916-134">관련성 분석 테스트</span><span class="sxs-lookup"><span data-stu-id="2f916-134">Testing Relevance analysis</span></span>](test-relevance-analysis-in-advanced-ediscovery.md)

