---
title: 검색 통계
ms.author: markjjo
author: esclee
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: ''
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: ''
ms.openlocfilehash: 98999d3d82efaace7673d70b0334cb0efb80fc08
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30215208"
---
# <a name="search-statistics"></a><span data-ttu-id="29319-102">검색 통계</span><span class="sxs-lookup"><span data-stu-id="29319-102">Search statistics</span></span>

<span data-ttu-id="29319-p101">검색 결과의 유효성을 검사할 수 있는 한 가지 방법은 결과를 기준으로 통계를 확인 하 여 예상과 일치 하는지 확인 하는 것입니다. 검색이 완료 되 면 검색 세부 정보 플라이 아웃에 높은 수준의 통계가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="29319-p101">One way you can validate your search results is to look at the statistics around your results to make sure they align with your expectations. When a search completes, high-level statistics are shown on the search details flyout:</span></span>
- <span data-ttu-id="29319-105">검색을 통해 검색 되는 항목의 수 및 볼륨</span><span class="sxs-lookup"><span data-stu-id="29319-105">Number and volume of items retrieved by the search</span></span>
- <span data-ttu-id="29319-106">검색 위치에서 찾은 부분 인덱싱된/인덱싱되지 않은 항목의 수 및 볼륨</span><span class="sxs-lookup"><span data-stu-id="29319-106">Number and volume of partially indexed/unindexed items that were found in the search locations</span></span>
- <span data-ttu-id="29319-p102">검색 된 사서함 및 위치 수입니다. 자세한 통계를 보려면 검색 세부 정보 플라이 아웃에서 "통계"를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="29319-p102">Number of mailboxes and locations searched. In order to view more detailed statistics, click on "Statistics" from the search details flyout.</span></span>

## <a name="summary"></a><span data-ttu-id="29319-109">요약</span><span class="sxs-lookup"><span data-stu-id="29319-109">Summary</span></span>

<span data-ttu-id="29319-p103">요약 보기에서는 위치 유형 (예: Exchange)으로 분류 된 검색 결과를 볼 수 있습니다. 각 위치 유형에 대해 다음을 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="29319-p103">In Summary view, you can see the search results broken down by location type (e.g. Exchange). For each location type, you can see:</span></span>
- <span data-ttu-id="29319-112">검색 조건과 일치 하는 항목이 있는 위치 수</span><span class="sxs-lookup"><span data-stu-id="29319-112">Number of locations that had items that matched the search conditions</span></span>
- <span data-ttu-id="29319-113">이 위치에서 검색 조건과 일치 하는 항목의 수</span><span class="sxs-lookup"><span data-stu-id="29319-113">Number of items from these locations that matched the search conditions</span></span>
- <span data-ttu-id="29319-114">검색 조건과 일치 하는 항목의 총 크기입니다.</span><span class="sxs-lookup"><span data-stu-id="29319-114">Total volume of items that matched the search conditions.</span></span>

## <a name="top-locations"></a><span data-ttu-id="29319-115">상위 위치</span><span class="sxs-lookup"><span data-stu-id="29319-115">Top locations</span></span>

<span data-ttu-id="29319-p104">상위 위치 보기에는 가장 일치 하는 개별 위치가 표시 됩니다. 각 위치에 대해 다음이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="29319-p104">In Top locations view, you see the individual locations with the most matches. For each location, you will see:</span></span>
- <span data-ttu-id="29319-118">위치 이름 (예: SharePoint URL)</span><span class="sxs-lookup"><span data-stu-id="29319-118">Location name (e.g. SharePoint URL)</span></span>
- <span data-ttu-id="29319-119">위치 종류</span><span class="sxs-lookup"><span data-stu-id="29319-119">Location type</span></span>
- <span data-ttu-id="29319-120">검색 조건과 일치 하는 항목 수</span><span class="sxs-lookup"><span data-stu-id="29319-120">Number of items that matched the search conditions</span></span>
- <span data-ttu-id="29319-121">검색 조건과 일치 하는 항목의 총 크기입니다.</span><span class="sxs-lookup"><span data-stu-id="29319-121">Total volume of items that matched the search conditions.</span></span>

## <a name="queries"></a><span data-ttu-id="29319-122">쿼리하도록</span><span class="sxs-lookup"><span data-stu-id="29319-122">Queries</span></span>

<span data-ttu-id="29319-p105">쿼리에 사용 된 (c:s) 키워드나 키워드 행이 있는 경우 쿼리 결과를 위치 유형별 쿼리 보기로 볼 수 있습니다. 각 위치 유형에 대해 다음이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="29319-p105">If you have used (c:s) keyword or keyword rows in your query, then you can see the breakdown of your query in Queries view per location type. For each location type, you will see:</span></span>

- <span data-ttu-id="29319-p106">파트:이 열에는 "Primary" 또는 "Keyword" 라는 단어가 포함 됩니다. "기본"은 행에 전체 쿼리에 대 한 통계가 표시 되는 반면 "Keyword"는 쿼리 구성 요소 중 하나를 의미 합니다.</span><span class="sxs-lookup"><span data-stu-id="29319-p106">Part: this column will either have the word "Primary" or "Keyword". "Primary" means that the row presents statistics on the entire query, whereas "Keyword" means one of the query components.</span></span>

- <span data-ttu-id="29319-p107">쿼리: 행이 참조 하는 실제 쿼리 구성 요소입니다. Part가 "Primary" 이면 전체 쿼리가 됩니다. Part가 "Keyword" 이면 여기에 쿼리 구성 요소 중 하나가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="29319-p107">Query: the actual query component the row refers to. If Part is "Primary", this will be the entire query; if Part was "Keyword", you will see one of the query components here.</span></span>
  
  - <span data-ttu-id="29319-129">모든 contentin 사서함을 검색 하는 경우 (키워드를 지정 하지 않음) 실제 쿼리는 (size > = 0)로, 모든 항목이 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="29319-129">When you search all contentin mailboxes (by not specifying any keywords), the actual query is (size >= 0) so that all items are returned</span></span>
  
  - <span data-ttu-id="29319-130">SharePoint Online 및 비즈니스용 OneDrive 사이트를 검색 하면 다음과 같은 두 가지 구성 요소가 추가 됩니다.</span><span class="sxs-lookup"><span data-stu-id="29319-130">When you search SharePoint Online and OneDrive for Business sites, the two following components are added:</span></span>
    
    - <span data-ttu-id="29319-131">NOT IsExternalContent: 1-온-프레미스 SharePoint 조직에서 모든 콘텐츠를 제외 합니다.</span><span class="sxs-lookup"><span data-stu-id="29319-131">NOT IsExternalContent:1 - excludes any content from an on-premises SharePoint organization</span></span>
    
    - <span data-ttu-id="29319-132">NOT isOneNotePage: 1-모든 OneNote 파일은 검색 쿼리와 일치 하는 모든 문서와 중복 되므로 제외 합니다.</span><span class="sxs-lookup"><span data-stu-id="29319-132">NOT isOneNotePage: 1 - excludes all OneNote files because these would be duplicates of any document that matches the search query.</span></span>

- <span data-ttu-id="29319-133">검색 조건과 일치 하는 항목이 있는 위치 수입니다.</span><span class="sxs-lookup"><span data-stu-id="29319-133">Number of locations that had items that matched the search conditions.</span></span>

- <span data-ttu-id="29319-134">검색 조건과 일치 하는 이러한 위치에 있는 항목의 수입니다.</span><span class="sxs-lookup"><span data-stu-id="29319-134">Number of items from these locations that matched the search conditions.</span></span>

- <span data-ttu-id="29319-135">검색 조건과 일치 하는 항목의 총 크기입니다.</span><span class="sxs-lookup"><span data-stu-id="29319-135">Total volume of items that matched the search conditions.</span></span>