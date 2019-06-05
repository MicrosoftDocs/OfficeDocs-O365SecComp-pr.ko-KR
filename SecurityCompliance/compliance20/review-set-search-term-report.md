---
title: 검토 집합에 대 한 검색 용어 보고서 생성
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
ROBOTS: NOINDEX, NOFOLLOW
description: ''
ms.openlocfilehash: 877c0017359ab9193c4cae81cbef4240909053a8
ms.sourcegitcommit: e323610df2df71c84f536e8a38650d33d8069e41
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/04/2019
ms.locfileid: "34714997"
---
# <a name="generate-search-term-report-for-a-review-set"></a><span data-ttu-id="f9819-102">검토 집합에 대 한 검색 용어 보고서 생성</span><span class="sxs-lookup"><span data-stu-id="f9819-102">Generate search term report for a review set</span></span>

<span data-ttu-id="f9819-103">EDiscovery에서는 문서를 쿼리 하는 데 가장 자주 사용 되는 조건 중 하나는 키워드 검색 용어를 사용 하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="f9819-103">In eDiscovery, one of the most frequently used conditions for querying documents is by using keyword search terms.</span></span> <span data-ttu-id="f9819-104">사례에 중요 한 특정 키워드 ( *용어*라고도 함)를 포함 하는 문서를 식별 하 여 검토자가 해당 사용자가 직면 하 고 있는 항목에 대 한 높은 수준의 이해를 시작할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f9819-104">By identifying documents that contain the specific keywords (also referred to as *terms*) that are important to a case, reviewers can begin to get a high-level understanding of what they are facing.</span></span> <span data-ttu-id="f9819-105">Microsoft 365의 고급 eDiscovery에서는 검토 집합 내의 저장 된 쿼리에 검색 용어 보고서를 생성 하 여이 작업을 정확히 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f9819-105">In Advanced eDiscovery in Microsoft 365, you can do precisely this by generating search term reports on saved queries within a review set.</span></span>

## <a name="step-1-create-a-saved-query-in-the-review-set"></a><span data-ttu-id="f9819-106">1 단계: 검토 집합에 저장 된 쿼리 만들기</span><span class="sxs-lookup"><span data-stu-id="f9819-106">Step 1: Create a saved query in the review set</span></span>

<span data-ttu-id="f9819-107">의미 있는 검색 용어 보고서를 생성 하려면 검토 집합에서 검색 용어 보고서를 생성 하려는 문서 집합을 정의 하는 저장 된 쿼리를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f9819-107">To generate a meaningful search term report, create a saved query that defines the set of documents in the review set that you want to generate a search term report for.</span></span> <span data-ttu-id="f9819-108">예를 들어 키워드 조건 카드를 사용 하 여 날짜 범위 또는 실제 검색 용어 집합을 사용 하 여 쿼리를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f9819-108">For example, you can use a date range or the actual set of search terms (by using the Keywords condition card) to create the query.</span></span> <span data-ttu-id="f9819-109">집합 쿼리 검토에 대해 자세히 알아보려면 [검토 집합에서 데이터 쿼리](review-set-search.md)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="f9819-109">To learn more about review set queries, see [Query the data in a review set](review-set-search.md).</span></span>

## <a name="step-2-generate-a-search-term-report"></a><span data-ttu-id="f9819-110">2 단계: 검색 용어 보고서 생성</span><span class="sxs-lookup"><span data-stu-id="f9819-110">Step 2: Generate a search term report</span></span>

<span data-ttu-id="f9819-111">1 단계에서 만든 저장 된 쿼리의 상황에 맞는 메뉴를 통해 또는 검색 용어 보고서 관리 콘솔을 통해 검색 용어 보고서를 생성 하는 두 가지 방법이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f9819-111">There are two different ways to generate a search term report: through the context menu of the saved query you created in Step 1, or through the search term report management console.</span></span>

- <span data-ttu-id="f9819-112">상황에 맞는 메뉴를 사용 하려면 1 단계에서 만든 저장 된 쿼리의 상황에 맞는 메뉴를 열고 **검색 용어 보고서 생성**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="f9819-112">To use the context menu, open the context menu of the saved query you created in Step 1, and click **Generate search term report**.</span></span>

- <span data-ttu-id="f9819-113">관리 콘솔을 사용 하려면 **검토 설정 관리 > 검색 용어 보고서 보기로**이동 하 여 **새로 만들기**를 클릭 한 다음 1 단계에서 만든 저장 된 쿼리를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="f9819-113">To use the management console, go to **Manage review set > View search term reports**, click **New**, and then select the saved query you created in Step 1.</span></span>

<span data-ttu-id="f9819-114">그런 다음 보고할 용어를 각각의 줄 바꿈으로 구분 하 여 입력 합니다. 1 단계에서 만든 저장 된 쿼리가 키워드 조건 카드를 사용 하는 경우, 플라이 아웃 페이지는 저장 된 쿼리에 사용 되는 첫 번째 키워드 조건 카드의 용어로 미리 채워집니다.</span><span class="sxs-lookup"><span data-stu-id="f9819-114">Then, enter the terms you would like to report on, separated by newline; if the saved query that you created in Step 1 used keyword condition card, the flyout page will be pre-populated with the terms from the first keyword condition card used in the saved query.</span></span>

<span data-ttu-id="f9819-115">그런 다음 보고 대상으로 최대 3 개의 피벗을 선택 하 고 **생성**을 클릭 하 여 검색 용어 보고서 생성 작업을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="f9819-115">Then, select up to three pivots to report on, and click on **Generate**, which will start the search term report generation job.</span></span>

### <a name="what-is-a-pivot"></a><span data-ttu-id="f9819-116">피벗 이란?</span><span class="sxs-lookup"><span data-stu-id="f9819-116">What is a pivot?</span></span>

<span data-ttu-id="f9819-117">피벗 보고서가 구성 되는 방식입니다.</span><span class="sxs-lookup"><span data-stu-id="f9819-117">Pivots are how the report will be organized.</span></span> <span data-ttu-id="f9819-118">다음 예를 살펴보겠습니다.</span><span class="sxs-lookup"><span data-stu-id="f9819-118">Consider the following example.</span></span>

- <span data-ttu-id="f9819-119">저장 된 쿼리는 10 개의 문서: 즉, doc1 ~ doc10을 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="f9819-119">The saved query retrieves 10 documents: doc1 thru doc10.</span></span>

- <span data-ttu-id="f9819-120">doc1, doc2, doc3, doc4, doc5, doc6 및 doc7는 "eDiscovery" 라는 용어를 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="f9819-120">doc1, doc2, doc3, doc4, doc5, doc6, and doc7 contain the term "eDiscovery".</span></span>

- <span data-ttu-id="f9819-121">doc6, doc7, doc8, doc9 및 doc10에는 "조사" 라는 용어가 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f9819-121">doc6, doc7, doc8, doc9, and doc10 contain the term "Investigation".</span></span>

- <span data-ttu-id="f9819-122">doc1, doc3, doc5, doc7, doc9은 custodian A에서 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="f9819-122">doc1, doc3, doc5, doc7, doc9 are from custodian A.</span></span>

- <span data-ttu-id="f9819-123">doc2, doc4, doc6, doc8, doc10은 custodian B입니다.</span><span class="sxs-lookup"><span data-stu-id="f9819-123">doc2, doc4, doc6, doc8, doc10 are from custodian B.</span></span>

<span data-ttu-id="f9819-124">이 경우 custodians의 "eDiscovery" 및 "조사" 라는 용어에 대해 검색 용어 보고서를 생성 하 고 검색 용어 보고서는 다음과 같이 구성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f9819-124">In this case, if you were to generate a search term report on the terms "eDiscovery" and "Investigation" and pivot on custodians, the search term report would be organized as follows:</span></span>

- <span data-ttu-id="f9819-125">"eDiscovery"-custodian A: 4 문서</span><span class="sxs-lookup"><span data-stu-id="f9819-125">"eDiscovery" - custodian A: 4 documents</span></span>

- <span data-ttu-id="f9819-126">"eDiscovery"-custodian B: 3 문서</span><span class="sxs-lookup"><span data-stu-id="f9819-126">"eDiscovery" - custodian B: 3 documents</span></span>

- <span data-ttu-id="f9819-127">"조사"-custodian A: 2 개 문서</span><span class="sxs-lookup"><span data-stu-id="f9819-127">"Investigation" - custodian A: 2 documents</span></span>

- <span data-ttu-id="f9819-128">"조사"-custodian B: 3 문서</span><span class="sxs-lookup"><span data-stu-id="f9819-128">"Investigation" - custodian B: 3 documents</span></span>

## <a name="step-3-download-report"></a><span data-ttu-id="f9819-129">3 단계: 보고서 다운로드</span><span class="sxs-lookup"><span data-stu-id="f9819-129">Step 3: Download report</span></span>

<span data-ttu-id="f9819-130">검색 용어 관리 콘솔에서 이전에 만든 검색 용어 보고서 작업의 상태를 추적할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f9819-130">In the search term management console, you can track the status of a previously-created search term report job.</span></span> <span data-ttu-id="f9819-131">작업이 완료 되 면 검색 용어 보고서에 대 한 행을 클릭 하 고 "다운로드"를 클릭 하면 검색 용어 보고서가 CSV 형식으로 다운로드 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f9819-131">Once the job completes, you can click on the row for the search term report and click "Download", which will download the search term report in a CSV format.</span></span> <span data-ttu-id="f9819-132">(검색 용어, 피벗) 튜플에는 하나의 행이 있으며 각 행에는 다음 정보가 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f9819-132">There will be one row per (search term, pivots) tuple, and each row will contain the following information:</span></span>

- <span data-ttu-id="f9819-133">검색 된 문서 수</span><span class="sxs-lookup"><span data-stu-id="f9819-133">How many documents were retrieved?</span></span>

- <span data-ttu-id="f9819-134">문서 전체에서 검색 용어를 찾은 횟수는 몇 회 입니까?</span><span class="sxs-lookup"><span data-stu-id="f9819-134">How many times was the search term found across the documents?</span></span>

- <span data-ttu-id="f9819-135">검색 된 문서의 총 량은 얼마 입니까?</span><span class="sxs-lookup"><span data-stu-id="f9819-135">What is the total volume of retrieved documents?</span></span>

- <span data-ttu-id="f9819-136">검색 된 패밀리가 몇 개입니까?</span><span class="sxs-lookup"><span data-stu-id="f9819-136">How many families were retrieved?</span></span>

- <span data-ttu-id="f9819-137">검색 용어가 없는 문서를 포함 하 여 해당 패밀리의 총 문서 수는 얼마나 됩니까?</span><span class="sxs-lookup"><span data-stu-id="f9819-137">What is the total document count of those families, including the documents that did not have the search term?</span></span>

- <span data-ttu-id="f9819-138">위의 전체 볼륨은 무엇입니까?</span><span class="sxs-lookup"><span data-stu-id="f9819-138">What is the total volume of the above?</span></span>