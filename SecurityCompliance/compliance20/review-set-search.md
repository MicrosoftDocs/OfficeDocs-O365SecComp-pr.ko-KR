---
title: 검토 집합의 데이터 쿼리
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
ms.openlocfilehash: 395cc01238f4dbc91de5dd652e10121f5e0cc926
ms.sourcegitcommit: 4ce350f8f3eb597587945a8ac9b33e9793440c64
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/01/2019
ms.locfileid: "33527237"
---
# <a name="query-the-data-in-a-review-set"></a><span data-ttu-id="7db92-102">검토 집합의 데이터 쿼리</span><span class="sxs-lookup"><span data-stu-id="7db92-102">Query the data in a review set</span></span>

<span data-ttu-id="7db92-103">대부분의 경우 검토 집합에 있는 항목을 보다 자세히 살펴보고 보다 효율적으로 검토 하도록 구성 하는 것이 도움이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7db92-103">In most cases, it will be useful to be able to dig deeper into what is there in a review set and organize them to review more efficiently.</span></span> <span data-ttu-id="7db92-104">검토 집합 내의 쿼리를 사용 하면 사용자가 한 번에 정의한 기준을 충족 하는 문서 하위 집합에 집중할 수 있으므로 작업을 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7db92-104">Queries within a review set enables you to do so by letting you focus on a subset of documents that meet the criteria defined by you at once.</span></span>

## <a name="creating-and-running-a-query-within-a-review-set"></a><span data-ttu-id="7db92-105">검토 집합 내에서 쿼리 만들기 및 실행</span><span class="sxs-lookup"><span data-stu-id="7db92-105">Creating and running a query within a review set</span></span>

<span data-ttu-id="7db92-106">검토 집합 내에서 쿼리를 만들고 실행 하려면 검토 집합에서 "새 쿼리"를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="7db92-106">In order to create and run a query within your review set, click on "New Query" in your review set.</span></span> <span data-ttu-id="7db92-107">쿼리 이름을 지정 하 고 조건을 정의한 후에는 "저장"을 클릭 하 여 쿼리를 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="7db92-107">After you name your query and define the conditions, click "Save" to run the query.</span></span> <span data-ttu-id="7db92-108">이전에 저장 한 쿼리를 실행 하려면 저장 된 쿼리를 클릭 하면 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7db92-108">To run a query that has been previously saved, simply click on the saved query.</span></span> <span data-ttu-id="7db92-109">검색할 수 있는 메타 데이터 목록은 [문서 메타 데이터 필드](document-metadata-fields.md) 를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="7db92-109">Refer to [Document metadata fields](document-metadata-fields.md) for a list of metadata you can search by.</span></span>

## <a name="building-your-query"></a><span data-ttu-id="7db92-110">쿼리 작성</span><span class="sxs-lookup"><span data-stu-id="7db92-110">Building your query</span></span>

<span data-ttu-id="7db92-111">키워드 조건 카드에 조건 카드와 쿼리 언어를 함께 사용 하 여 쿼리를 작성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7db92-111">You can build your query using a combination of condition cards and query language in the Keywords condition card.</span></span> <span data-ttu-id="7db92-112">조건 카드를 블록으로 그룹화 하 여 보다 복잡 한 쿼리를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7db92-112">You can group condition cards together as a block to craft a more complex query.</span></span>

### <a name="condition-card"></a><span data-ttu-id="7db92-113">조건 카드</span><span class="sxs-lookup"><span data-stu-id="7db92-113">Condition card</span></span>

<span data-ttu-id="7db92-114">검토 집합의 모든 검색 가능 필드에는 쿼리를 작성 하는 데 사용할 수 있는 해당 하는 조건 카드가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7db92-114">Every searchable field in a review set has a corresponding condition card that you can use to build your query.</span></span>

<span data-ttu-id="7db92-115">여러 유형의 조건 카드를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7db92-115">There are multiple types of condition cards:</span></span>
- <span data-ttu-id="7db92-116">Freetext: freetext 조건 카드는 subject와 같은 텍스트 필드에 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7db92-116">Freetext: freetext condition card is used for text fields such as subject.</span></span> <span data-ttu-id="7db92-117">여러 검색 용어를 쉼표로 구분 하 여 나열할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7db92-117">You can list multiple search terms by separating them out with a comma.</span></span>
- <span data-ttu-id="7db92-118">날짜: 날짜 조건 카드는 마지막으로 수정한 날짜와 같은 날짜 필드에 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7db92-118">Date: date condition card is used for date fields such as last modified date.</span></span>
- <span data-ttu-id="7db92-119">검색 옵션: 검색 옵션 조건 카드에는 검토 집합의 특정 필드에 사용할 수 있는 값 목록이 제공 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7db92-119">Search options: search options condition card will provide a list of possible values for the particular field in your review set.</span></span> <span data-ttu-id="7db92-120">이 속성은 검토 집합에서 가능한 값의 수가 제한 되는 필드 (예: 보낸 사람)에 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7db92-120">This is used for fields, such as sender, where there is a finite number of possible values in your review set.</span></span>
- <span data-ttu-id="7db92-121">키워드: 키워드 조건 카드는 용어를 검색 하거나에서 KQL와 같은 쿼리 언어를 사용 하는 데 사용할 수 있는 freetext 조건 카드의 특정 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="7db92-121">Keyword: keyword condition card is a specific instance of freetext condition card that you can use to search for terms, or use KQL-like query language in.</span></span> <span data-ttu-id="7db92-122">자세한 내용은 아래를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="7db92-122">See below for more detail.</span></span>

### <a name="query-language"></a><span data-ttu-id="7db92-123">쿼리 언어</span><span class="sxs-lookup"><span data-stu-id="7db92-123">Query language</span></span>

<span data-ttu-id="7db92-124">조건 카드 외에도 키워드 카드에서 KQL 같은 쿼리 언어를 사용 하 여 쿼리를 작성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7db92-124">In addition to condition cards, you can use a KQL-like query language in the Keywords card to craft your query.</span></span> <span data-ttu-id="7db92-125">쿼리 언어는 AND, OR, NOT 및 NEAR (n)과 같은 표준 KQL 구문을 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7db92-125">The query language supports standard KQL syntax like AND, OR, NOT, and NEAR(n).</span></span> <span data-ttu-id="7db92-126">또한 단일 문자 와일드 카드 (?) 및 여러 문자 와일드 카드 (\*)를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7db92-126">It also supports single-character wildcard (?) and multi-character wildcard (\*).</span></span>

## <a name="filter"></a><span data-ttu-id="7db92-127">필터</span><span class="sxs-lookup"><span data-stu-id="7db92-127">Filter</span></span>

<span data-ttu-id="7db92-128">저장할 수 있는 쿼리 외에도 필터를 사용 하 여 쿼리 결과에 추가 조건을 신속 하 게 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7db92-128">In addition to queries that you can save, you can overlay additional conditions on the fly to your query results using filters.</span></span> <span data-ttu-id="7db92-129">필터는 다음과 같은 몇 가지 중요 한 점에서 쿼리와 다릅니다.</span><span class="sxs-lookup"><span data-stu-id="7db92-129">Filters differ from queries in a few significant ways:</span></span>
- <span data-ttu-id="7db92-130">필터는 임시 (즉, 서로 다른 세션에 유지 되지 않음) 이며, 쿼리가 검토 집합에 저장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7db92-130">Filters are transient (i.e. they do not persist over different sessions), whereas queries are saved to the review set.</span></span>
- <span data-ttu-id="7db92-131">필터는 항상 자동으로 추가 됩니다. 필터는 현재 적용 된 쿼리 위에 적용 되며, 쿼리를 적용 하면 해당 쿼리가 대체 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7db92-131">Filters are always additive; filters will apply on top of the query you have in effect at the moment, whereas applying a query will replace the query in effect.</span></span>