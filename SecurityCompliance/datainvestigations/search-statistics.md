---
title: 검색 통계
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: ''
ms.openlocfilehash: 986c3f3cbb19cd0f66b18db274e68a3bf8414952
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32258112"
---
# <a name="search-statistics"></a><span data-ttu-id="9524b-102">검색 통계</span><span class="sxs-lookup"><span data-stu-id="9524b-102">Search statistics</span></span>

<span data-ttu-id="9524b-103">데이터 인시던트를 조사할 때 검색 결과의 유효성을 검사 하는 효과적인 방법은 검색 결과에 대 한 통계를 확인 하 여 예상과 일치 하는지 확인 하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="9524b-103">An effective way to validate your search results when investigation a data incident is to view the statistics about your search results to make sure they align with your expectations.</span></span> <span data-ttu-id="9524b-104">검색이 완료 되 면 검색 세부 정보 플라이 아웃 페이지의 **상태** 아래에 다음과 같은 높은 수준의 통계가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9524b-104">When a search as finished running, the following high-level statistics are displayed under **Status** on the search details flyout page:</span></span>

![검색 세부 정보 플라이 아웃 페이지의 검색 statisics](../media/SearchDetailsFlyout.png)

- <span data-ttu-id="9524b-106">검색 조건과 일치 하는 항목의 예상 수 및 크기</span><span class="sxs-lookup"><span data-stu-id="9524b-106">The estimated number and size of items that matched the search criteria.</span></span>

- <span data-ttu-id="9524b-107">검색할 수 없지만 검색에 포함 된 콘텐츠 위치에서 찾은 부분 인덱싱된 항목의 개수와 크기 ( *인덱싱되지 않은 항목*)</span><span class="sxs-lookup"><span data-stu-id="9524b-107">The number and size of partially indexed items (also called *unindexed items*) that aren't searchable but that were found in the content locations that were included in the search.</span></span>

- <span data-ttu-id="9524b-108">검색 된 사서함 및 사이트의 수입니다.</span><span class="sxs-lookup"><span data-stu-id="9524b-108">The number of mailboxes and sites that were searched.</span></span>

<span data-ttu-id="9524b-109">자세한 통계를 보려면 검색 세부 정보 플라이 아웃 페이지에서 **통계** 를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="9524b-109">To view more detailed statistics, click **Statistics** on the search details flyout page.</span></span> <span data-ttu-id="9524b-110">**검색 통계** 페이지에서 검색 요약, 검색 결과와 일치 하는 항목이 포함 된 위쪽 위치, 검색 쿼리에 대 한 자세한 통계를 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9524b-110">On the **Search statistics** page, you can view the search summary, the top location that contained items that matched the search results, and detailed statistics about the search query.</span></span>

![검색 통계 드롭다운 목록](../media/SearchStatisticsDropDownList.png)

## <a name="summary"></a><span data-ttu-id="9524b-112">요약</span><span class="sxs-lookup"><span data-stu-id="9524b-112">Summary</span></span>

<span data-ttu-id="9524b-113">**요약** 보기에서 위치 유형으로 분류 된 검색 결과를 볼 수 있습니다 (예: 위치에 Exchange 사서함 및 SharePoint 사이트 포함).</span><span class="sxs-lookup"><span data-stu-id="9524b-113">In the **Summary** view, you can see the search results broken down by location type (for example, locations include Exchange mailboxes and SharePoint sites).</span></span> <span data-ttu-id="9524b-114">각 위치 유형에 대해 다음과 같은 정보가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9524b-114">The following information is displayed for each location type:</span></span>

- <span data-ttu-id="9524b-115">검색 조건과 일치 하는 항목이 있는 위치 수입니다.</span><span class="sxs-lookup"><span data-stu-id="9524b-115">The number of locations that had items that matched the search criteria.</span></span>

- <span data-ttu-id="9524b-116">검색 조건과 일치 하는 각 위치 유형의 총 항목 수입니다.</span><span class="sxs-lookup"><span data-stu-id="9524b-116">The total number of items from each location type that matched the search criteria.</span></span>

- <span data-ttu-id="9524b-117">검색 조건과 일치 하는 각 위치 유형의 총 항목 크기입니다.</span><span class="sxs-lookup"><span data-stu-id="9524b-117">The total size of items from each location type that matched the search criteria.</span></span>

## <a name="top-locations"></a><span data-ttu-id="9524b-118">상위 위치</span><span class="sxs-lookup"><span data-stu-id="9524b-118">Top locations</span></span>

<span data-ttu-id="9524b-119">**최상위 위치** 보기에는 검색 조건과 일치 하는 항목을 포함 하는 개별 콘텐츠 위치가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9524b-119">In the **Top locations** view, you see the individual content locations with the most items that matched the search criteria.</span></span> <span data-ttu-id="9524b-120">각 콘텐츠 위치에 대해 다음 정보가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9524b-120">For each content location, the following information is displayed:</span></span>

- <span data-ttu-id="9524b-121">위치 이름입니다. 사서함의 전자 메일 주소 및 SharePoint 사이트의 URL</span><span class="sxs-lookup"><span data-stu-id="9524b-121">The name of the location; the email address for mailboxes and the URL for SharePoint sites</span></span>

- <span data-ttu-id="9524b-122">위치 유형</span><span class="sxs-lookup"><span data-stu-id="9524b-122">The location type</span></span>

- <span data-ttu-id="9524b-123">검색 조건과 일치 하는 항목 수</span><span class="sxs-lookup"><span data-stu-id="9524b-123">Number of items that matched the search criteria</span></span>

- <span data-ttu-id="9524b-124">검색 조건과 일치 하는 모든 항목의 총 크기입니다.</span><span class="sxs-lookup"><span data-stu-id="9524b-124">The total size of all items that matched the search criteria.</span></span>

## <a name="queries"></a><span data-ttu-id="9524b-125">쿼리하도록</span><span class="sxs-lookup"><span data-stu-id="9524b-125">Queries</span></span>

<span data-ttu-id="9524b-126">**쿼리** 보기에서는 검색 쿼리의 각 구성 요소에 대 한 자세한 통계 정보를 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9524b-126">In the **Queries** view, you can see detailed statistics for each component of the search query.</span></span> <span data-ttu-id="9524b-127">검색 쿼리에서 키워드 목록을 사용 하는 경우 **쿼리** 보기에서 각 키워드나 키워드 구와 일치 하는 항목 수를 보여 주는 향상 된 통계를 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9524b-127">If you used the keyword list in the search query, you can view enhanced statistics in the **Queries** view  that show how many items match each keyword or keyword phrase.</span></span> <span data-ttu-id="9524b-128">이를 통해 가장 (및 최소) 쿼리 부분을 빠르게 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9524b-128">This can help you quickly identify which parts of the query are the most (and least) effective.</span></span> 

<span data-ttu-id="9524b-129">**쿼리** 보기에 표시 되는 정보는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="9524b-129">The following information is displayed in the **Queries** view:</span></span>

 - <span data-ttu-id="9524b-130">**위치 유형** -행에 표시 되는 통계의 콘텐츠 위치 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="9524b-130">**Location type** - The type of content location for the statistics displayed in the row.</span></span>

- <span data-ttu-id="9524b-131">**Part** -이 열은 **Primary** or **Keyword**값 중 하나를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="9524b-131">**Part** - This column will display one of the following values: **Primary** or **Keyword**.</span></span> <span data-ttu-id="9524b-132">**Primary** 는 행에 전체 쿼리에 대 한 통계가 표시 됨을 의미 합니다. **키워드** 는 행의 통계가 쿼리 구성 요소 중 하나에 대 한 것을 의미 합니다.</span><span class="sxs-lookup"><span data-stu-id="9524b-132">**Primary** means the row presents statistics on the entire query; **Keyword** means the statistics in the row are for one of the query components.</span></span>

- <span data-ttu-id="9524b-133">**Condition** -행이 참조 하는 검색 쿼리의 실제 쿼리 구성 요소입니다.</span><span class="sxs-lookup"><span data-stu-id="9524b-133">**Condition** - The actual query component of the search query the row refers to.</span></span> <span data-ttu-id="9524b-134">**Part** 열의 값이 **Primary**인 경우 전체 검색 쿼리에 대 한 통계가 표시 됩니다. 값이 **Keyword**이면 **쿼리** 열에 표시 된 쿼리의 구성 요소에 대 한 통계가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9524b-134">If the value in the **Part** column is **Primary**, then the statistics for the entire search query are displayed; if the value is **Keyword**, then the statistics for the component of the query shown in the **Query** column are displayed.</span></span> <span data-ttu-id="9524b-135">예를 들어 키워드 목록이 사용 된 경우 키워드 중 하나의 통계를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="9524b-135">For example, if the keyword list was used, then the statistics one of the keywords are displayed.</span></span>

  <span data-ttu-id="9524b-136">다음은 **쿼리** 열에 표시 되는 통계에 대해 알아야 할 몇 가지 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="9524b-136">Here are some other things to know about the statistics displayed in the **Queries** column:</span></span>
  
  - <span data-ttu-id="9524b-137">모든 키워드를 지정 하지 않고 사서함에서 모든 콘텐츠를 검색 하는 경우 실제 쿼리는 **(size > = 0)** 로, 모든 항목이 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9524b-137">When you search for all content in mailboxes (by not specifying any keywords), the actual query is **(size >= 0)** so that all items are returned</span></span>
  
  - <span data-ttu-id="9524b-138">SharePoint 및 OneDrive 사이트를 검색 하면 다음의 두 구성 요소가 검색 쿼리에 추가 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9524b-138">When you search SharePoint and OneDrive sites, the two following components are added to the search query:</span></span>
    
    <span data-ttu-id="9524b-139">**NOT IsExternalContent: 1** -온-프레미스 SharePoint 조직에서 모든 콘텐츠를 제외 합니다.</span><span class="sxs-lookup"><span data-stu-id="9524b-139">**NOT IsExternalContent:1** - This excludes any content from an on-premises SharePoint organization</span></span>
    
    <span data-ttu-id="9524b-140">**NOT isOneNotePage: 1** -모든 OneNote 파일이 검색 쿼리와 일치 하는 문서와 중복 되므로이를 제외 합니다.</span><span class="sxs-lookup"><span data-stu-id="9524b-140">**NOT isOneNotePage:1** - This excludes all OneNote files because these would be duplicates of any document that matches the search query.</span></span>

- <span data-ttu-id="9524b-141">**검색 위치** 행에 표시 된 파트/조건에 대 한 검색 쿼리와 일치 한 항목이 있는 콘텐츠 위치의 수입니다.</span><span class="sxs-lookup"><span data-stu-id="9524b-141">**Locations in search** The number of content locations that had items that matched the search query for the part/condition displayed in the row.</span></span> <span data-ttu-id="9524b-142">보관 사서함은 검색 조건과 일치 하는 항목을 포함 하는 경우 별도의 위치로 계산 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9524b-142">Note that archive mailboxes are counted as a separate location if they contain items that match the search criteria.</span></span>

- <span data-ttu-id="9524b-143">**항목** -행에 표시 되는 파트/조건에 대해 검색 조건과 일치 하는 항목의 총 수입니다.</span><span class="sxs-lookup"><span data-stu-id="9524b-143">**Items** - The total number of items that matched the search criteria for the part/condition displayed in the row.</span></span>

- <span data-ttu-id="9524b-144">**Size** -행에 표시 된 파트/조건에 대해 검색 조건과 일치 하는 항목의 총 수입니다.</span><span class="sxs-lookup"><span data-stu-id="9524b-144">**Size** - The total number of items that matched the search criteria for the part/condition displayed in the row.</span></span>