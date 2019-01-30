---
title: 검색 쿼리 작성
ms.author: markjjo
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
ms.openlocfilehash: 119cdd9d932b6c1be847c406988efa80b8534795
ms.sourcegitcommit: ee28ee2b2bdfd049333c2f495d7f7780d13af4a6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2019
ms.locfileid: "29608148"
---
# <a name="building-search-queries"></a><span data-ttu-id="09e8e-102">검색 쿼리 작성</span><span class="sxs-lookup"><span data-stu-id="09e8e-102">Building search queries</span></span>
<span data-ttu-id="09e8e-103">쿼리를 작성에서 찾을 수 있는 항목을 정의 하려면 다양 한 키워드 및 조건을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="09e8e-103">In building your query, you can use various keywords and conditions to define which items to find.</span></span>

## <a name="keyword-searches"></a><span data-ttu-id="09e8e-104">키워드 검색</span><span class="sxs-lookup"><span data-stu-id="09e8e-104">Keyword searches</span></span>
<span data-ttu-id="09e8e-p101">**키워드** 상자에 검색 쿼리를 입력 합니다. 키워드, 메시지 전송 및 받은 날짜 또는 파일 이름 등의 문서 속성 또는 문서를 마지막으로 변경한 날짜와 같은 속성을 지정할 수 있습니다. 예: **AND**, **또는**, **하지**및 **NEAR**부울 연산자를 사용 하는 보다 복잡 한 쿼리를 사용할 수 있습니다. 문서 또는 외부에서 공유 된 문서에 대 한 검색에서 중요 한 정보 (예: 주민등록 번호)을 검색할 수도 있습니다. 키워드 상자에 빈을 지정 하지 않으면 검색 결과에 지정 된 콘텐츠 위치에 있는 모든 콘텐츠를 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="09e8e-p101">Type a search query in **Keywords** box. You can specify keywords, message properties such as sent and received dates, or document properties such as file names or the date that a document was last changed. You can use a more complex queries that use a Boolean operator, such as **AND**, **OR**, **NOT**, and **NEAR**. You can also search for sensitive information (such as social security numbers) in documents, or search for documents that have been shared externally. If you leave the keyword box empty, all content located in the specified content locations will be included in the search results.</span></span>
    
<span data-ttu-id="09e8e-p102">또는 수 **키워드 목록을 표시** 확인란을 및 누르면 형식은 각 행에 있는 키워드입니다. 이렇게 하면 각 행에 키워드와 비슷합니다 기능에서 생성 된 검색 쿼리에 **OR** 연산자는 논리 연산자 ( **c:s**)으로 연결 됩니다.</span><span class="sxs-lookup"><span data-stu-id="09e8e-p102">Alternatively, you can click the **Show keyword list** checkbox and the type a keyword in each row. If you do this, the keywords on each row are connected by a logical operator ( **c:s**) that is similar in functionality to the **OR** operator in the search query that's created.</span></span> 
    
<span data-ttu-id="09e8e-p103">키워드 목록을 사용 하는 이유 각 키워드를 일치 하는 얼마나 많은 항목이 표시 하는 통계를 얻을 수 있습니다. 이 키워드는는 가장 (및 최소) 효과적인를 빠르게 식별할 수 있습니다. 행에서 (괄호로 묶입니다) 키워드 구의 사용할 수도 있습니다. 검색 통계에 대 한 자세한 내용은 [검색 통계](search-statistics.md)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="09e8e-p103">Why use the keyword list? You can get statistics that show how many items match each keyword. This can help you quickly identify which keywords are the most (and least) effective. You can also use a keyword phrase (surrounded by parentheses) in a row. For more information about search statistics, see [Search statistic](search-statistics.md).</span></span>

## <a name="conditions"></a><span data-ttu-id="09e8e-117">조건</span><span class="sxs-lookup"><span data-stu-id="09e8e-117">Conditions</span></span>    
<span data-ttu-id="09e8e-p104">검색 범위를 좁힐 하 고 보다 정교한 결과 집합이 반환 하는 검색 조건을 추가할 수 있습니다. 검색 쿼리를 만들고 실행 하 여 검색을 시작 하는 경우에 절을 추가 하는 각 조건입니다. 조건 **및** 연산자 기능와 유사한 논리 연산자 (**c:c**)에 의해 (키워드 상자에 지정 된) 키워드 쿼리를 논리적으로 연결 됩니다. 항목 키워드 쿼리 및 결과에 포함할 하나 이상의 조건을 모두 충족 해야 함을 의미 합니다. 결과 범위를 좁히려면 조건 도움이 되는 방식입니다. 목록 및 설명은 검색 쿼리에서 사용할 수 있는 조건에 대 한 [키워드 쿼리 및 콘텐츠 검색을 위한 검색 조건에서](../keyword-queries-and-search-conditions.md#search-conditions)"검색 조건" 섹션을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="09e8e-p104">You can add search conditions to narrow a search and return a more refined set of results. Each condition adds a clause to the search query that is created and run when you start the search. A condition is logically connected to the keyword query (specified in the keyword box) by a logical operator (**c:c**) that is similar in functionality to the **AND** operator. That means that items have to satisfy both the keyword query and one or more conditions to be included in the results. This is how conditions help to narrow your results. For a list and description of conditions that you can use in a search query, see the "Search conditions" section in [Keyword queries and search conditions for Content Search](../keyword-queries-and-search-conditions.md#search-conditions).</span></span>


