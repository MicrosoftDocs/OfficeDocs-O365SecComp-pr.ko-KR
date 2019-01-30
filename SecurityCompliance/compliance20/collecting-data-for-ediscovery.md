---
title: 고급 eDiscovery (미리 보기)의 경우에 대 한 데이터를 수집합니다.
ms.author: esclee
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
ms.openlocfilehash: 6964cc00d7ae78078aa0729bd5408abd5ed9542a
ms.sourcegitcommit: ee28ee2b2bdfd049333c2f495d7f7780d13af4a6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2019
ms.locfileid: "29608150"
---
# <a name="collecting-data-for-a-case-in-advanced-ediscovery-preview"></a><span data-ttu-id="01784-102">고급 eDiscovery (미리 보기)의 경우에 대 한 데이터를 수집합니다.</span><span class="sxs-lookup"><span data-stu-id="01784-102">Collecting data for a case in Advanced eDiscovery (Preview)</span></span>

<span data-ttu-id="01784-p101">일치 하지 않음 custodians 및 사례 관심 있는 데이터 원본의 식별 한 후에 자세히 살펴볼 문서 집합을 식별 하는 시간입니다. Office 365의 custodial 및 custodial 아닌 위치에서이 식별 하려면 고급 eDiscovery (미리 보기)에서 검색 도구를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="01784-p101">Once you have identified custodians and data sources that are of interest for your case, it's time to identify the set of documents to delve into. You can use the Search tool in Advanced eDiscovery (Preview) to identify these from custodial and non-custodial locations in Office 365.</span></span>

<span data-ttu-id="01784-p102">검색을 실행 한 후 검색 쿼리와 일치 하는 대부분의 항목을 했던 위치와 같은 검색 된 항목에 대 한 통계를 볼 수 있습니다. 결과의 하위 집합을 미리 볼 수 있습니다. 추가 검사 하려면 문서 집합을 결정 했다면 때를 수집 하 고 처리 하는 작업 집합을 검색 결과 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="01784-p102">After you run a search, you will be able to view statistics on the retrieved items such as the locations that had the most items that matched the search query. You can also preview a subset of the results. When you've identified the set of documents that want to further examine, you can add the search results to a working set to collect and process.</span></span>

## <a name="create-a-search"></a><span data-ttu-id="01784-108">검색 만들기</span><span class="sxs-lookup"><span data-stu-id="01784-108">Create a search</span></span>

<span data-ttu-id="01784-p103">**검색** 탭에서 **새 검색** 을 클릭 하는 검색을 만드는 과정을 안내 하는 마법사가 시작 됩니다. 검색을 만드는 방법에 대 한 자세한 내용은 [만들기 데이터 수집에 대 한 검색을](create-search-to-collect-data.md)참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="01784-p103">Clicking **New search** on the **Searches** tab will start a wizard that guides you through creating a search. For detailed information on how to create a search, see [Create a search to collect data](create-search-to-collect-data.md).</span></span>

<span data-ttu-id="01784-p104">검색을 만든 후에 세부 정보를 사용 하 여 플라이 아웃 페이지 표시 됩니다. Note는 **통계** 및 **미리 보기** 단추 처음 회색으로 표시 되므로 검색 아직 완료 되지 않았습니다. 관리할 수 있습니다를 추적 **검색** 탭에서 검색의 진행 합니다.</span><span class="sxs-lookup"><span data-stu-id="01784-p104">After a search is created, a flyout page with details is displayed. Note that the **Statistics** and **Preview** buttons are initially grayed out because the search has not completed yet. You can keep track of the progress of the search on the **Searches** tab.</span></span>

## <a name="view-search-results-and-statistics"></a><span data-ttu-id="01784-114">검색 결과 보기 및 통계</span><span class="sxs-lookup"><span data-stu-id="01784-114">View search results and statistics</span></span>
<span data-ttu-id="01784-p105">콘텐츠 검색의 두 구성 요소는: 통계 (추정치) 및 미리 보기입니다. 이러한 구성 요소는 전체 각각, **검색** 탭에서 해당 열에 표시 하는 상태에서 **진행 중인** 를 **완료**로 **제출 됨** 에서 변경 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="01784-p105">There are two components of a content search: Statistics (Estimates) and Preview. As each of these components complete, you will see the status displayed in the corresponding columns on the **Searches** tab change from from **Submitted** to **In progress** to **Completed**.</span></span>

<span data-ttu-id="01784-p106">검색 estimate 완료 되 면 검색 결과 대 한 높은 수준의 일부 통계 표시는 플라이 아웃 페이지를 표시 하려면 검색을 클릭 합니다. 이 시점 **통계** 단추가 활성화 됩니다. 다음과 같이 검색 통계를 클릭할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="01784-p106">Once the search estimate is completed, click the search to display the flyout page, which will display some high-level statistics about the results of the search. At this point, the **Statistics** button will be active. You can click it to see search statistics, such as:</span></span>

- <span data-ttu-id="01784-120">요약</span><span class="sxs-lookup"><span data-stu-id="01784-120">Summary</span></span>
- <span data-ttu-id="01784-121">위쪽 위치</span><span class="sxs-lookup"><span data-stu-id="01784-121">Top locations</span></span>
- <span data-ttu-id="01784-122">쿼리</span><span class="sxs-lookup"><span data-stu-id="01784-122">Queries</span></span>
- <span data-ttu-id="01784-123">구체화</span><span class="sxs-lookup"><span data-stu-id="01784-123">Refiners</span></span>

<span data-ttu-id="01784-124">검색 통계에 대 한 자세한 내용은 [검색 통계](search-statistics.md)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="01784-124">For more information about search statistics, see [Search statistics](search-statistics.md).</span></span>

<span data-ttu-id="01784-p107">미리 보기를 완료 한 후 **미리 보기** 단추가 활성화 됩니다. 결과의 샘플링 된 하위 집합을 미리 보기를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="01784-p107">Once preview is completed, the **Preview** button will be active. Click it to preview a sampled subset of the results.</span></span>

## <a name="adding-search-results-to-a-working-set"></a><span data-ttu-id="01784-127">작업 집합에 추가 검색 결과</span><span class="sxs-lookup"><span data-stu-id="01784-127">Adding search results to a working set</span></span>

<span data-ttu-id="01784-p108">수집 하 고 전체 검색 결과 처리할 준비가 되 면 작업 집합을 추가 하 여 이렇게 수 있습니다. 자세한 내용은 [작업 집합에 추가 데이터](add-data-to-working-set.md)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="01784-p108">When you are ready to collect and process the entire results of a search, you can do so by adding it to a working set. For details, see [Add data to a working set](add-data-to-working-set.md).</span></span> 