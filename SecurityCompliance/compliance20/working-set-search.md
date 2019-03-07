---
title: 작업 집합에서 데이터 쿼리
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
ms.openlocfilehash: 2523072181307cce510f0f318834329b2c70b376
ms.sourcegitcommit: 6aa82374eef09d2c1921f93bda3eabeeb28aadeb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/06/2019
ms.locfileid: "30454990"
---
# <a name="query-the-data-in-a-working-set"></a><span data-ttu-id="2dfeb-102">작업 집합에서 데이터 쿼리</span><span class="sxs-lookup"><span data-stu-id="2dfeb-102">Query the data in a working set</span></span>

<span data-ttu-id="2dfeb-103">대부분의 경우이 기능은 작업 집합에 있는 항목을 보다 자세히 살펴보고 보다 효율적으로 검토할 수 있도록 구성 하는 데 도움이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="2dfeb-103">In most cases, it will be useful to be able to dig deeper into what is there in a working set and organize them to review more efficiently.</span></span> <span data-ttu-id="2dfeb-104">작업 집합 내의 쿼리를 사용 하면 사용자가 한 번에 정의한 기준을 충족 하는 문서 하위 집합에 집중할 수 있으므로이를 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2dfeb-104">Queries within a working set enables you to do so by letting you focus on a subset of documents that meet the criteria defined by you at once.</span></span>

## <a name="creating-and-running-a-query-within-a-working-set"></a><span data-ttu-id="2dfeb-105">작업 집합 내에서 쿼리 만들기 및 실행</span><span class="sxs-lookup"><span data-stu-id="2dfeb-105">Creating and running a query within a working set</span></span>

<span data-ttu-id="2dfeb-106">작업 집합 내에서 쿼리를 만들고 실행 하려면 작업 집합에서 "새 쿼리"를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="2dfeb-106">In order to create and run a query within your working set, click on "New Query" in your working set.</span></span> <span data-ttu-id="2dfeb-107">쿼리 이름을 지정 하 고 조건을 정의한 후에는 "저장"을 클릭 하 여 쿼리를 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="2dfeb-107">After you name your query and define the conditions, click "Save" to run the query.</span></span> <span data-ttu-id="2dfeb-108">이전에 저장 한 쿼리를 실행 하려면 저장 된 쿼리를 클릭 하면 됩니다.</span><span class="sxs-lookup"><span data-stu-id="2dfeb-108">To run a query that has been previously saved, simply click on the saved query.</span></span> <span data-ttu-id="2dfeb-109">검색할 수 있는 메타 데이터 목록은 [문서 메타 데이터 필드](document-metadata-fields.md) 를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="2dfeb-109">Refer to [Document metadata fields](document-metadata-fields.md) for a list of metadata you can search by.</span></span>

## <a name="building-your-query"></a><span data-ttu-id="2dfeb-110">쿼리 작성</span><span class="sxs-lookup"><span data-stu-id="2dfeb-110">Building your query</span></span>

<span data-ttu-id="2dfeb-111">키워드 조건 카드에 조건 카드와 쿼리 언어를 함께 사용 하 여 쿼리를 작성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2dfeb-111">You can build your query using a combination of condition cards and query language in the Keywords condition card.</span></span>

### <a name="condition-card"></a><span data-ttu-id="2dfeb-112">조건 카드</span><span class="sxs-lookup"><span data-stu-id="2dfeb-112">Condition card</span></span>

<span data-ttu-id="2dfeb-113">작업 집합의 모든 검색 가능 필드에는 쿼리를 작성 하는 데 사용할 수 있는 해당 하는 조건 카드가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2dfeb-113">Every searchable field in a working set has a corresponding condition card that you can use to build your query.</span></span>

<span data-ttu-id="2dfeb-114">여러 유형의 조건 카드를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2dfeb-114">There are multiple types of condition cards:</span></span>
- <span data-ttu-id="2dfeb-115">freetext: freetext 조건 카드는 subject와 같은 텍스트 필드에 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="2dfeb-115">Freetext: freetext condition card is used for text fields such as subject.</span></span> <span data-ttu-id="2dfeb-116">여러 검색 용어를 쉼표로 구분 하 여 나열할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2dfeb-116">You can list multiple search terms by separating them out with a comma.</span></span>
- <span data-ttu-id="2dfeb-117">날짜: 날짜 조건 카드는 마지막으로 수정한 날짜와 같은 날짜 필드에 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="2dfeb-117">Date: date condition card is used for date fields such as last modified date.</span></span>
- <span data-ttu-id="2dfeb-118">검색 옵션: 검색 옵션 조건 카드에는 작업 집합의 특정 필드에 사용할 수 있는 값의 목록이 제공 됩니다.</span><span class="sxs-lookup"><span data-stu-id="2dfeb-118">Search options: search options condition card will provide a list of possible values for the particular field in your working set.</span></span> <span data-ttu-id="2dfeb-119">이 속성은 작업 집합에 가능한 값의 수가 한정 된 보낸 사람 등의 필드에 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="2dfeb-119">This is used for fields such as sender, where there is a finite number of possible values in your working set.</span></span>
- <span data-ttu-id="2dfeb-120">키워드: 키워드 조건 카드는 용어를 검색 하거나에서 KQL와 같은 쿼리 언어를 사용 하는 데 사용할 수 있는 freetext 조건 카드의 특정 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="2dfeb-120">Keyword: keyword condition card is a specific instance of freetext condition card that you can use to search for terms, or use KQL-like query language in.</span></span> <span data-ttu-id="2dfeb-121">자세한 내용은 아래를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="2dfeb-121">See below for more detail.</span></span>

### <a name="query-language"></a><span data-ttu-id="2dfeb-122">쿼리 언어</span><span class="sxs-lookup"><span data-stu-id="2dfeb-122">Query language</span></span>

<span data-ttu-id="2dfeb-123">조건 카드 외에도 키워드 카드에서 KQL 같은 쿼리 언어를 사용 하 여 쿼리를 작성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2dfeb-123">In addition to condition cards, you can use a KQL-like query language in the Keywords card to craft your query.</span></span> <span data-ttu-id="2dfeb-124">쿼리 언어는 and, OR, NOT 및 NEAR (n)과 같은 표준 KQL 구문을 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2dfeb-124">The query language supports standard KQL syntax like AND, OR, NOT, and NEAR(n).</span></span> <span data-ttu-id="2dfeb-125">또한 단일 문자 와일드 카드 (?) 및 여러 문자 와일드 카드 (\*)를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2dfeb-125">It also supports single-character wildcard (?) and multi-character wildcard (\*).</span></span>