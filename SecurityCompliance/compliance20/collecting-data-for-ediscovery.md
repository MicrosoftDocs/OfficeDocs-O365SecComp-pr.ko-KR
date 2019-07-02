---
title: Advanced eDiscovery에서 사례에 대 한 데이터 수집
ms.author: esclee
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
ms.openlocfilehash: 091d6f8835ae1aae2f075f0b510954255c3a6a5c
ms.sourcegitcommit: e323610df2df71c84f536e8a38650d33d8069e41
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/04/2019
ms.locfileid: "34703841"
---
# <a name="collect-data-for-a-case-in-advanced-ediscovery"></a><span data-ttu-id="d3c6b-102">Advanced eDiscovery에서 사례에 대 한 데이터 수집</span><span class="sxs-lookup"><span data-stu-id="d3c6b-102">Collect data for a case in Advanced eDiscovery</span></span>

<span data-ttu-id="d3c6b-103">해당 사례에 관심이 있는 custodians 및 데이터 원본을 파악 한 후에는 delve에 사용할 문서 집합을 식별 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3c6b-103">Once you have identified custodians and data sources that are of interest for your case, it's time to identify the set of documents to delve into.</span></span> <span data-ttu-id="d3c6b-104">고급 eDiscovery의 검색 도구를 사용 하 여 Office 365에서 custodial 및 비 custodial 위치를 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d3c6b-104">You can use the Search tool in Advanced eDiscovery to identify these from custodial and non-custodial locations in Office 365.</span></span>

<span data-ttu-id="d3c6b-105">검색을 실행 한 후 검색 쿼리와 일치 하는 항목이 가장 많은 위치와 같은 검색 된 항목에 대 한 통계를 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d3c6b-105">After you run a search, you will be able to view statistics on the retrieved items such as the locations that had the most items that matched the search query.</span></span> <span data-ttu-id="d3c6b-106">또한 결과의 하위 집합을 미리 볼 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d3c6b-106">You can also preview a subset of the results.</span></span> <span data-ttu-id="d3c6b-107">추가로 확인할 문서 집합을 식별 한 경우 수집 및 처리할 검토 집합에 검색 결과를 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d3c6b-107">When you've identified the set of documents that want to further examine, you can add the search results to a review set to collect and process.</span></span>

## <a name="create-a-search"></a><span data-ttu-id="d3c6b-108">Create a search</span><span class="sxs-lookup"><span data-stu-id="d3c6b-108">Create a search</span></span>

<span data-ttu-id="d3c6b-109">검색 탭에서 **새 검색** 을 클릭 하면 검색을 만드는 과정을 안내 하는 마법사가 시작 됩니다. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="d3c6b-109">Clicking **New search** on the **Searches** tab will start a wizard that guides you through creating a search.</span></span> <span data-ttu-id="d3c6b-110">검색을 만드는 방법에 대 한 자세한 내용은 [create a search를 검색 하 여 데이터 수집](create-search-to-collect-data.md)을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="d3c6b-110">For detailed information on how to create a search, see [Create a search to collect data](create-search-to-collect-data.md).</span></span>

<span data-ttu-id="d3c6b-111">검색을 만든 후에는 세부 정보가 포함 된 플라이 아웃 페이지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d3c6b-111">After a search is created, a flyout page with details is displayed.</span></span> <span data-ttu-id="d3c6b-112">검색이 아직 완료 되지 않았으므로 **통계** 및 **미리 보기** 단추가 초기에 회색으로 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d3c6b-112">Note that the **Statistics** and **Preview** buttons are initially grayed out because the search has not completed yet.</span></span> <span data-ttu-id="d3c6b-113">검색의 진행 상태를 추적할 수 있습니다 (검색 탭) \*\*\*\* .</span><span class="sxs-lookup"><span data-stu-id="d3c6b-113">You can keep track of the progress of the search on the **Searches** tab.</span></span>

## <a name="view-search-results-and-statistics"></a><span data-ttu-id="d3c6b-114">검색 결과 및 통계 보기</span><span class="sxs-lookup"><span data-stu-id="d3c6b-114">View search results and statistics</span></span>

<span data-ttu-id="d3c6b-115">콘텐츠 검색에는 통계 (예측) 및 미리 보기의 두 가지 구성 요소가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d3c6b-115">There are two components of a content search: Statistics (Estimates) and Preview.</span></span> <span data-ttu-id="d3c6b-116">이러한 각 구성 요소가 완료 되 면 **검색** 탭의 해당 열에 **제출** 됨에서 **진행 중** 에서 **완료**됨으로 변경 된 상태가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d3c6b-116">As each of these components complete, you will see the status displayed in the corresponding columns on the **Searches** tab change from from **Submitted** to **In progress** to **Completed**.</span></span>

<span data-ttu-id="d3c6b-117">검색 예측이 완료 되 면 검색을 클릭 하 여 플라이 아웃 페이지를 표시 하 고 검색 결과에 대 한 일부 높은 수준의 통계를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3c6b-117">Once the search estimate is completed, click the search to display the flyout page, which will display some high-level statistics about the results of the search.</span></span> <span data-ttu-id="d3c6b-118">이 시점에서 **통계** 단추가 활성화 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d3c6b-118">At this point, the **Statistics** button will be active.</span></span> <span data-ttu-id="d3c6b-119">이 도구를 클릭 하 여 다음과 같은 검색 통계를 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d3c6b-119">You can click it to see search statistics, such as:</span></span>

- <span data-ttu-id="d3c6b-120">요약</span><span class="sxs-lookup"><span data-stu-id="d3c6b-120">Summary</span></span>
- <span data-ttu-id="d3c6b-121">상위 위치</span><span class="sxs-lookup"><span data-stu-id="d3c6b-121">Top locations</span></span>
- <span data-ttu-id="d3c6b-122">쿼리하도록</span><span class="sxs-lookup"><span data-stu-id="d3c6b-122">Queries</span></span>

<span data-ttu-id="d3c6b-123">검색 통계에 대 한 자세한 내용은 [검색 통계](search-statistics.md)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="d3c6b-123">For more information about search statistics, see [Search statistics](search-statistics.md).</span></span>

<span data-ttu-id="d3c6b-124">미리 보기가 완료 되 면 **미리 보기** 단추가 활성화 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d3c6b-124">Once preview is completed, the **Preview** button will be active.</span></span> <span data-ttu-id="d3c6b-125">이 도구를 클릭 하 여 결과의 샘플링할 하위 집합을 미리 봅니다.</span><span class="sxs-lookup"><span data-stu-id="d3c6b-125">Click it to preview a sampled subset of the results.</span></span>

## <a name="adding-search-results-to-a-review-set"></a><span data-ttu-id="d3c6b-126">검토 집합에 검색 결과 추가</span><span class="sxs-lookup"><span data-stu-id="d3c6b-126">Adding search results to a review set</span></span>

<span data-ttu-id="d3c6b-127">검색의 전체 결과를 수집 하 고 처리할 준비가 되 면 검토 집합에 추가 하 여 검색할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d3c6b-127">When you are ready to collect and process the entire results of a search, you can do so by adding it to a review set.</span></span> <span data-ttu-id="d3c6b-128">자세한 내용은 [검토 집합에 데이터 추가](add-data-to-review-set.md)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="d3c6b-128">For details, see [Add data to a review set](add-data-to-review-set.md).</span></span> 