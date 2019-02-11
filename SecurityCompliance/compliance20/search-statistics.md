---
title: 검색 통계
ms.author: markjjo
author: esclee
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
ms.openlocfilehash: 0cfc1e5f04887cbdbcc0be8854fc50d6f9b5f1f2
ms.sourcegitcommit: 7e2a0185cadea7f3a6afc5ddc445eac2e1ce22eb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/11/2019
ms.locfileid: "29706009"
---
# <a name="search-statistics"></a><span data-ttu-id="04358-102">검색 통계</span><span class="sxs-lookup"><span data-stu-id="04358-102">Search statistics</span></span>

<span data-ttu-id="04358-p101">검색 결과 유효성을 검사 하는 한 가지 방법은 한 기대 눈금에 맞춰집니다 있는지 확인 하도록 결과 주위 통계를 확인 하는 것입니다. 검색 완료 되 면 높은 수준의 통계 검색 세부 정보 플라이 아웃에 나와 있습니다.</span><span class="sxs-lookup"><span data-stu-id="04358-p101">One way you can validate your search results is to look at the statistics around your results to make sure they align with your expectations. When a search completes, high-level statistics are shown on the search details flyout:</span></span>
- <span data-ttu-id="04358-105">번호 및 검색에서 검색 되는 항목의 볼륨</span><span class="sxs-lookup"><span data-stu-id="04358-105">Number and volume of items retrieved by the search</span></span>
- <span data-ttu-id="04358-106">번호와 볼륨의 부분적으로 인덱싱된/인덱싱되지 않은 검색 위치에서 발견 된 항목</span><span class="sxs-lookup"><span data-stu-id="04358-106">Number and volume of partially indexed/unindexed items that were found in the search locations</span></span>
- <span data-ttu-id="04358-p102">수의 사서함과 위치를 검색 합니다. 자세한 통계를 보려면 검색 세부 정보 플라이 아웃에서 "통계"에서 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="04358-p102">Number of mailboxes and locations searched. In order to view more detailed statistics, click on "Statistics" from the search details flyout.</span></span>

## <a name="summary"></a><span data-ttu-id="04358-109">요약</span><span class="sxs-lookup"><span data-stu-id="04358-109">Summary</span></span>

<span data-ttu-id="04358-p103">요약 보기의 위치 (예: Exchange) 형식으로 분류 된 검색 결과 볼 수 있습니다. 각 위치 유형에 대 한 다음을 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="04358-p103">In Summary view, you can see the search results broken down by location type (e.g. Exchange). For each location type, you can see:</span></span>
- <span data-ttu-id="04358-112">검색 조건에 일치 하는 항목을 했던 위치 개수</span><span class="sxs-lookup"><span data-stu-id="04358-112">Number of locations that had items that matched the search conditions</span></span>
- <span data-ttu-id="04358-113">검색 조건에 일치 하는 이러한 위치에서 항목 수</span><span class="sxs-lookup"><span data-stu-id="04358-113">Number of items from these locations that matched the search conditions</span></span>
- <span data-ttu-id="04358-114">검색 조건과 일치 하는 항목의 총 볼륨입니다.</span><span class="sxs-lookup"><span data-stu-id="04358-114">Total volume of items that matched the search conditions.</span></span>

## <a name="top-locations"></a><span data-ttu-id="04358-115">위쪽 위치</span><span class="sxs-lookup"><span data-stu-id="04358-115">Top locations</span></span>

<span data-ttu-id="04358-p104">위쪽 위치 보기의 개별 위치에서 가장 일치 하는 결과를 볼 수 있습니다. 각 위치에 대해 다음을 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="04358-p104">In Top locations view, you see the individual locations with the most matches. For each location, you will see:</span></span>
- <span data-ttu-id="04358-118">위치 이름 (예: SharePoint URL)</span><span class="sxs-lookup"><span data-stu-id="04358-118">Location name (e.g. SharePoint URL)</span></span>
- <span data-ttu-id="04358-119">위치 종류</span><span class="sxs-lookup"><span data-stu-id="04358-119">Location type</span></span>
- <span data-ttu-id="04358-120">검색 조건에 일치 하는 항목 수</span><span class="sxs-lookup"><span data-stu-id="04358-120">Number of items that matched the search conditions</span></span>
- <span data-ttu-id="04358-121">검색 조건과 일치 하는 항목의 총 볼륨입니다.</span><span class="sxs-lookup"><span data-stu-id="04358-121">Total volume of items that matched the search conditions.</span></span>

## <a name="queries"></a><span data-ttu-id="04358-122">쿼리</span><span class="sxs-lookup"><span data-stu-id="04358-122">Queries</span></span>

<span data-ttu-id="04358-p105">쿼리에서 (c:s) 키워드 또는 키워드 행을 사용 하는 경우 위치 유형 마다 쿼리 보기에서 쿼리를 분석을 볼 수 있습니다. 각 위치 유형에 대 한 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="04358-p105">If you have used (c:s) keyword or keyword rows in your query, then you can see the breakdown of your query in Queries view per location type. For each location type, you will see:</span></span>

- <span data-ttu-id="04358-p106">부: 단어 "기본" 또는 "키워드"이이 열에 지정할 하거나 됩니다. "기본"을 의미 하는 행 전체 쿼리 통계를 제공 "키워드" 쿼리 구성 요소 중 하나를 의미 하는 반면 합니다.</span><span class="sxs-lookup"><span data-stu-id="04358-p106">Part: this column will either have the word "Primary" or "Keyword". "Primary" means that the row presents statistics on the entire query, whereas "Keyword" means one of the query components.</span></span>

- <span data-ttu-id="04358-p107">쿼리:는 실제 쿼리 구성 요소는 행을 참조 합니다. "기본" 부분을 사용 하는 경우이 속성은 전체 쿼리에 존재 합니다. 파트 "키워드" 했으므로, 다음 쿼리 구성 요소 중 하나 나타납니다.</span><span class="sxs-lookup"><span data-stu-id="04358-p107">Query: the actual query component the row refers to. If Part is "Primary", this will be the entire query; if Part was "Keyword", you will see one of the query components here.</span></span>
  
  - <span data-ttu-id="04358-129">실제 쿼리는 (모든 키워드를 지정 하지 않으면) 하 여 모든 contentin 사서함을 검색 하는 경우 (크기 gt_ = 0) 항목을 모두 반환 되도록</span><span class="sxs-lookup"><span data-stu-id="04358-129">When you search all contentin mailboxes (by not specifying any keywords), the actual query is (size >= 0) so that all items are returned</span></span>
  
  - <span data-ttu-id="04358-130">비즈니스 사이트에 대 한 SharePoint Online 및 OneDrive를 검색 하는 경우에 다음 구성 요소 2가 추가 됩니다.</span><span class="sxs-lookup"><span data-stu-id="04358-130">When you search SharePoint Online and OneDrive for Business sites, the two following components are added:</span></span>
    
    - <span data-ttu-id="04358-131">하지 IsExternalContent:1-온-프레미스 SharePoint 조직에서 모든 콘텐츠를 제외 합니다.</span><span class="sxs-lookup"><span data-stu-id="04358-131">NOT IsExternalContent:1 - excludes any content from an on-premises SharePoint organization</span></span>
    
    - <span data-ttu-id="04358-132">하지 isOneNotePage: 1-있기 때문에 이러한 중복 항목을 검색 쿼리와 일치 하는 모든 문서의 모든 OneNote 파일을 제외 합니다.</span><span class="sxs-lookup"><span data-stu-id="04358-132">NOT isOneNotePage: 1 - excludes all OneNote files because these would be duplicates of any document that matches the search query.</span></span>

- <span data-ttu-id="04358-133">검색 조건과 일치 하는 항목을 했던 위치 개수입니다.</span><span class="sxs-lookup"><span data-stu-id="04358-133">Number of locations that had items that matched the search conditions.</span></span>

- <span data-ttu-id="04358-134">검색 조건과 일치 하는 이러한 위치에서 항목의 수입니다.</span><span class="sxs-lookup"><span data-stu-id="04358-134">Number of items from these locations that matched the search conditions.</span></span>

- <span data-ttu-id="04358-135">검색 조건과 일치 하는 항목의 총 볼륨입니다.</span><span class="sxs-lookup"><span data-stu-id="04358-135">Total volume of items that matched the search conditions.</span></span>

## <a name="refiners"></a><span data-ttu-id="04358-136">구체화</span><span class="sxs-lookup"><span data-stu-id="04358-136">Refiners</span></span>

<span data-ttu-id="04358-p108">Exchange 사서함에 대 한 구체화 보기에서는 ItemClass, 보낸사람 및 받는 사람으로 추가 붕괴로. 각 위치 및 구체화 값에 대 한 검색에서 반환 된 문서 수를 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="04358-p108">For Exchange mailboxes, refiners view gives you additional breakdowns by ItemClass, Sender, and Recipient. For each location and refiner value, you can see how many documents were returned in the search.</span></span>