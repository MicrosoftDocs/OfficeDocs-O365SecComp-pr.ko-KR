---
title: 검색 쿼리 작성
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
ms.openlocfilehash: e62d486b102fa035ae21b379d30bb0657b82acc9
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32242506"
---
# <a name="build-search-queries"></a><span data-ttu-id="778a8-102">검색 쿼리 작성</span><span class="sxs-lookup"><span data-stu-id="778a8-102">Build search queries</span></span>

<span data-ttu-id="778a8-103">쿼리를 작성할 때 다양 한 키워드와 조건을 사용 하 여 찾을 항목을 정의할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="778a8-103">In building your query, you can use various keywords and conditions to define which items to find.</span></span>

## <a name="keyword-searches"></a><span data-ttu-id="778a8-104">키워드 검색</span><span class="sxs-lookup"><span data-stu-id="778a8-104">Keyword searches</span></span>

<span data-ttu-id="778a8-105">**키워드** 에 검색 쿼리를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="778a8-105">Type a search query in **Keywords** box.</span></span> <span data-ttu-id="778a8-106">키워드, 메시지 속성(보낸 날짜 및 받은 날짜) 또는 문서 속성(예: 파일 이름 또는 문서를 마지막으로 변경한 날짜)을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="778a8-106">You can specify keywords, message properties such as sent and received dates, or document properties such as file names or the date that a document was last changed.</span></span> <span data-ttu-id="778a8-107">**and**, **OR**, **NOT**및 **NEAR**과 같은 부울 연산자를 사용 하는 보다 복잡 한 쿼리를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="778a8-107">You can use a more complex queries that use a Boolean operator, such as **AND**, **OR**, **NOT**, and **NEAR**.</span></span> <span data-ttu-id="778a8-108">문서에서 중요 한 정보 (예: 주민 등록 번호)를 검색 하거나 외부에서 공유한 문서를 검색할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="778a8-108">You can also search for sensitive information (such as social security numbers) in documents, or search for documents that have been shared externally.</span></span> <span data-ttu-id="778a8-109">키워드 상자를 비워 두면 지정 된 콘텐츠 위치에 있는 모든 콘텐츠가 검색 결과에 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="778a8-109">If you leave the keyword box empty, all content located in the specified content locations will be included in the search results.</span></span>
    
<span data-ttu-id="778a8-110">또는 **키워드 목록 표시** 확인란을 클릭 하 고 각 행에 키워드를 입력할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="778a8-110">Alternatively, you can click the **Show keyword list** checkbox and the type a keyword in each row.</span></span> <span data-ttu-id="778a8-111">이 작업을 수행 하는 경우 각 행의 키워드는 생성 되는 검색 쿼리의 **OR** 연산자와 유사한 기능을 하는 논리 연산자 ( **c:s**)에 의해 연결 됩니다.</span><span class="sxs-lookup"><span data-stu-id="778a8-111">If you do this, the keywords on each row are connected by a logical operator ( **c:s**) that is similar in functionality to the **OR** operator in the search query that's created.</span></span> 
    
<span data-ttu-id="778a8-112">키워드 목록을 사용 하는 이유</span><span class="sxs-lookup"><span data-stu-id="778a8-112">Why use the keyword list?</span></span> <span data-ttu-id="778a8-113">각 키워드와 일치 하는 항목의 수를 보여 주는 통계를 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="778a8-113">You can get statistics that show how many items match each keyword.</span></span> <span data-ttu-id="778a8-114">이를 통해 가장 효과적이 고 효과적인 키워드를 빠르게 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="778a8-114">This can help you quickly identify which keywords are the most (and least) effective.</span></span> <span data-ttu-id="778a8-115">행에 괄호를 사용 하 여 키워드로 묶은 키워드 구를 사용할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="778a8-115">You can also use a keyword phrase (surrounded by parentheses) in a row.</span></span> <span data-ttu-id="778a8-116">검색 통계에 대 한 자세한 내용은 [검색 통계](search-statistics.md)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="778a8-116">For more information about search statistics, see [Search statistic](search-statistics.md).</span></span>

## <a name="conditions"></a><span data-ttu-id="778a8-117">조건</span><span class="sxs-lookup"><span data-stu-id="778a8-117">Conditions</span></span>
    
<span data-ttu-id="778a8-118">검색 조건을 추가 하 여 검색 범위를 좁히고 보다 구체화 된 결과 집합을 반환할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="778a8-118">You can add search conditions to narrow a search and return a more refined set of results.</span></span> <span data-ttu-id="778a8-119">각 조건은 검색 쿼리에 검색을 시작할 때 만들어지고 실행 되는 절을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="778a8-119">Each condition adds a clause to the search query that is created and run when you start the search.</span></span> <span data-ttu-id="778a8-120">조건은 **AND** 연산자의 기능과 유사한 논리 연산자 (**c:c**)에 의해 키워드 상자에 지정 된 키워드 쿼리에 논리적으로 연결 됩니다.</span><span class="sxs-lookup"><span data-stu-id="778a8-120">A condition is logically connected to the keyword query (specified in the keyword box) by a logical operator (**c:c**) that is similar in functionality to the **AND** operator.</span></span> <span data-ttu-id="778a8-121">즉, 항목은 키워드 쿼리와 결과에 포함할 하나 이상의 조건을 만족 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="778a8-121">That means that items have to satisfy both the keyword query and one or more conditions to be included in the results.</span></span> <span data-ttu-id="778a8-122">조건은 이런 방식으로 결과 범위를 좁히는 데 도움이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="778a8-122">This is how conditions help to narrow your results.</span></span> <span data-ttu-id="778a8-123">검색 쿼리에 사용할 수 있는 조건에 대 한 목록 및 설명은 [키워드 쿼리 및 검색 조건의 콘텐츠 검색](../keyword-queries-and-search-conditions.md#search-conditions)에서 "검색 조건" 섹션을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="778a8-123">For a list and description of conditions that you can use in a search query, see the "Search conditions" section in [Keyword queries and search conditions for Content Search](../keyword-queries-and-search-conditions.md#search-conditions).</span></span>


