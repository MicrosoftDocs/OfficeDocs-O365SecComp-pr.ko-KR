---
title: 검색 쿼리 작성
ms.author: markjjo
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
description: Microsoft 365에서 데이터 조사를 사용할 때 데이터를 검색할 때 키워드와 조건을 사용 하 여 검색 범위를 좁힐 수 있습니다.
ms.openlocfilehash: 6d6c7e99257d071595365ec9a9557892fe3fe8db
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/17/2019
ms.locfileid: "34151060"
---
# <a name="build-search-queries"></a><span data-ttu-id="95a2e-103">검색 쿼리 작성</span><span class="sxs-lookup"><span data-stu-id="95a2e-103">Build search queries</span></span>

<span data-ttu-id="95a2e-104">검색 쿼리를 작성 하는 경우 키워드를 사용 하 여 검색 범위를 좁혀 조사에 가장 적합 한 항목을 반환할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="95a2e-104">When building search queries, you can use keywords to find specific content and conditions to narrow the scope of the search to return items that are most relevant to your investigation.</span></span>

![키워드 및 조건을 사용 하 여 검색 결과 범위 좁히기](../media/SearchQueryBox.png)

## <a name="keyword-searches"></a><span data-ttu-id="95a2e-106">키워드 검색</span><span class="sxs-lookup"><span data-stu-id="95a2e-106">Keyword searches</span></span>

<span data-ttu-id="95a2e-107">검색 쿼리의 **키워드** 상자에 키워드 쿼리를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="95a2e-107">Type a keyword query in the **Keywords** box in the search query.</span></span> <span data-ttu-id="95a2e-108">키워드, 전자 메일 메시지 속성 (예: 보낸 날짜 및 받은 날짜가 동일) 또는 문서 속성 (예: 파일 이름 또는 문서를 마지막으로 변경한 날짜)을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="95a2e-108">You can specify keywords, email message properties, (such as sent and received dates), or document properties (such as file names or the date that a document was last changed).</span></span> <span data-ttu-id="95a2e-109">**And**, **OR**, **NOT**및 **NEAR**과 같은 부울 연산자를 사용 하는 보다 복잡 한 쿼리를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="95a2e-109">You can use a more complex queries that use a Boolean operator, such as **AND**, **OR**, **NOT**, and **NEAR**.</span></span> <span data-ttu-id="95a2e-110">전자 메일 메시지에 포함 되지 않은 SharePoint 및 OneDrive의 문서에서 중요 한 정보 (예: 사회 보장 번호)를 검색 하거나 외부에서 공유한 문서를 검색할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="95a2e-110">You can also search for sensitive information (such as social security numbers) in documents in SharePoint and OneDrive (not in email messages), or search for documents that have been shared externally.</span></span> <span data-ttu-id="95a2e-111">**키워드** 상자를 비워 두면 지정 된 콘텐츠 위치에 있는 모든 콘텐츠가 검색 결과에 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="95a2e-111">If you leave the **Keywords** box empty, all content located in the specified content locations will be included in the search results.</span></span>
    
<span data-ttu-id="95a2e-112">또는 **키워드 목록 표시** 확인란을 클릭 하 고 각 행에 키워드나 키워드 구를 입력할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="95a2e-112">Alternatively, you can click the **Show keyword list** checkbox and the type a keyword or keyword phrase in each row.</span></span> <span data-ttu-id="95a2e-113">이 작업을 수행 하는 경우 각 행의 키워드는 생성 되는 검색 쿼리의 **OR** 연산자와 유사한 기능을 하는 논리 연산자 ( *c:s*로 표시 됨)에 의해 연결 됩니다.</span><span class="sxs-lookup"><span data-stu-id="95a2e-113">If you do this, the keywords in each row are connected by a logical operator (which is represented as *c:s*) that is similar in functionality to the **OR** operator in the search query that's created.</span></span> <span data-ttu-id="95a2e-114">즉, 모든 행에 키워드가 포함 된 항목이 검색 결과에 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="95a2e-114">This means that items that contain any keyword in any row will be included in the search results.</span></span>

![키워드 목록을 사용 하 여 쿼리의 각 키워드에 대 한 통계 가져오기](../media/KeywordListSearch.png)

<span data-ttu-id="95a2e-116">키워드 목록을 사용 하는 이유</span><span class="sxs-lookup"><span data-stu-id="95a2e-116">Why use the keyword list?</span></span> <span data-ttu-id="95a2e-117">키워드 목록에서 각 키워드와 일치 하는 항목 수를 보여 주는 통계를 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="95a2e-117">You can get statistics that show how many items match each keyword in the keyword list.</span></span> <span data-ttu-id="95a2e-118">이를 통해 가장 (및 최소) 효율적인 키워드를 빠르게 식별할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="95a2e-118">This can help you quickly identify the keywords that are the most (and least) effective.</span></span> <span data-ttu-id="95a2e-119">키워드 목록에 있는 행에 괄호로 묶은 키워드 구를 사용할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="95a2e-119">You can also use a keyword phrase (surrounded by parentheses) in a row in the keywords list.</span></span> <span data-ttu-id="95a2e-120">검색 통계에 대 한 자세한 내용은 [검색 통계](search-statistics.md)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="95a2e-120">For more information about search statistics, see [Search statistics](search-statistics.md).</span></span>

> [!NOTE]
> <span data-ttu-id="95a2e-121">큰 키워드 목록으로 인해 발생 하는 문제를 줄이기 위해 키워드 목록에는 최대 20 개의 행만 있을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="95a2e-121">To help reduce issues caused by large keyword lists, you're limited to a maximum of 20 rows in the keyword list.</span></span>

## <a name="conditions"></a><span data-ttu-id="95a2e-122">조건</span><span class="sxs-lookup"><span data-stu-id="95a2e-122">Conditions</span></span>
    
<span data-ttu-id="95a2e-123">검색 조건을 추가 하 여 검색 범위를 좁히고 보다 구체화 된 결과 집합을 반환할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="95a2e-123">You can add search conditions to narrow the scope of a search and return a more refined set of results.</span></span> <span data-ttu-id="95a2e-124">각 조건은 검색 쿼리에 검색을 시작할 때 만들어지고 실행 되는 절을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="95a2e-124">Each condition adds a clause to the search query that is created and run when you start the search.</span></span> <span data-ttu-id="95a2e-125">조건은 **AND** 연산자의 기능과 비슷한 논리 연산자 ( *c:c*로 표시 됨)에 의해 키워드 상자에 지정 된 키워드 쿼리에 논리적으로 연결 됩니다.</span><span class="sxs-lookup"><span data-stu-id="95a2e-125">A condition is logically connected to the keyword query (specified in the keyword box) by a logical operator (which is represented as *c:c*) that is similar in functionality to the **AND** operator.</span></span> <span data-ttu-id="95a2e-126">즉, 항목은 검색 결과에 포함할 키워드 쿼리와 하나 이상의 조건을 만족 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="95a2e-126">That means that items have to satisfy both the keyword query and one or more conditions to be included in the search results.</span></span> <span data-ttu-id="95a2e-127">조건은 이런 방식으로 결과 범위를 좁히는 데 도움이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="95a2e-127">This is how conditions help to narrow your results.</span></span> <span data-ttu-id="95a2e-128">검색 쿼리에 사용할 수 있는 조건에 대 한 목록 및 설명은 [키워드 쿼리 및 검색 조건의](../keyword-queries-and-search-conditions.md#search-conditions)"검색 조건" 섹션을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="95a2e-128">For a list and description of conditions that you can use in a search query, see the "Search conditions" section in [Keyword queries and search conditions](../keyword-queries-and-search-conditions.md#search-conditions).</span></span>
