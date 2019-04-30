---
title: 콘텐츠 검색을 다시 시도 하 여 콘텐츠 위치 오류 해결
ms.author: markjjo
author: markjjo
manager: laurawi
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: ''
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: 다시 시도 단추를 사용 하 여 콘텐츠 위치 오류가 있는 콘텐츠 검색 문제를 해결 합니다.
ms.openlocfilehash: 0963bccfe88a74b82ec3155469ca6d892bf2f7d8
ms.sourcegitcommit: 72e8a74b55fe7f56b50e30ff10a635734b5a3220
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/30/2019
ms.locfileid: "33472383"
---
# <a name="retry-a-content-search-to-resolve-a-content-location-error"></a><span data-ttu-id="f54e4-103">콘텐츠 검색을 다시 시도 하 여 콘텐츠 위치 오류 해결</span><span class="sxs-lookup"><span data-stu-id="f54e4-103">Retry a Content Search to resolve a content location error</span></span>

<span data-ttu-id="f54e4-104">보안 및 준수 센터에서 콘텐츠 검색을 사용 하 여 많은 수의 사서함을 검색 하는 경우 다음과 유사한 검색 오류를 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f54e4-104">When you use Content Search in the security and compliance center to search a large number of mailboxes, you may get search errors that are similar to the following:</span></span>

```
Error

The search on the following locations failed:

User1@contoso.com: Problem in processing the request. Please try again later. If you keep getting this error, contact your admin. (CS008-009)

User2@contoso.com: Application error occurred. Please try again later. (CS012-002)
```

<span data-ttu-id="f54e4-105">이러한 오류 (CS008와 CS012-009의 오류 코드 포함)는 콘텐츠 검색에서 특정 콘텐츠 위치를 검색 하지 못했음을 나타냅니다. 이 예에서는 두 사서함이 검색 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f54e4-105">These errors (with error codes of CS008-009 and CS012-002) indicate that Content Search failed to search specific content locations; in this example, two mailboxes weren't searched.</span></span> <span data-ttu-id="f54e4-106">이러한 오류는 콘텐츠 검색의 상태 세부 정보 플라이 아웃 페이지에 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f54e4-106">These errors are displayed on the status details flyout page of the Content Search.</span></span>

## <a name="cause-of-content-location-errors"></a><span data-ttu-id="f54e4-107">콘텐츠 위치 오류 원인</span><span class="sxs-lookup"><span data-stu-id="f54e4-107">Cause of content location errors</span></span>

<span data-ttu-id="f54e4-108">많은 수의 사서함을 검색할 때 검색은 Microsoft 데이터 센터의 수많은 서버에 분산 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f54e4-108">When searching a large number of mailboxes, the search is distributed across thousands of servers in a Microsoft datacenter.</span></span> <span data-ttu-id="f54e4-109">특정 서버는 언제 든 지 다시 부팅 상태가 되거나 중복 복사본에 장애 조치 (failover) 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f54e4-109">At any one time, specific servers could be in reboot state or in the process of failing over to redundant copies.</span></span> <span data-ttu-id="f54e4-110">이러한 경우에는 콘텐츠 검색 요청이 데이터를 검색 하는 데 시간이 초과 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f54e4-110">In either of these cases, the Content Search's request to retrieve data will timeout.</span></span> <span data-ttu-id="f54e4-111">이전 예제에서 실패 한 사서함에 대 한 오류는 검색 시간 초과로 인해 발생 했습니다.</span><span class="sxs-lookup"><span data-stu-id="f54e4-111">In the previous example, the errors for the mailboxes that failed were the result of the search timing out.</span></span>

## <a name="resolving-content-location-errors"></a><span data-ttu-id="f54e4-112">콘텐츠 위치 오류 해결</span><span class="sxs-lookup"><span data-stu-id="f54e4-112">Resolving content location errors</span></span>

<span data-ttu-id="f54e4-113">검색을 다시 시작 하면 여러 서버에서 유사한 오류가 발생 하는 경우가 많습니다.</span><span class="sxs-lookup"><span data-stu-id="f54e4-113">Restarting the search will often result in similar errors on different servers.</span></span> <span data-ttu-id="f54e4-114">검색을 다시 시작 하는 대신 검색 결과 페이지 위쪽에 표시 되는 **다시 시도** 단추를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="f54e4-114">Instead of restarting the search, click the **Retry** button that is displayed at the top of the search results page.</span></span>

![다시 시도 단추를 클릭 하 여 콘텐츠 위치 오류 해결](media/retrycontentsearch3.png)

<span data-ttu-id="f54e4-116">이렇게 하면 오류가 발생 한 사서함에 대해서만 검색이 다시 시도 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f54e4-116">This will result in the retrying the search only for the mailboxes that failed.</span></span> <span data-ttu-id="f54e4-117">검색을 다시 시도 하면 성공적으로 반환 된 다른 결과가 보존 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f54e4-117">When you retry the search, the other results that were successfully returned are retained.</span></span>

## <a name="tips-to-avoid-content-location-errors"></a><span data-ttu-id="f54e4-118">콘텐츠 위치 오류를 방지 하기 위한 팁</span><span class="sxs-lookup"><span data-stu-id="f54e4-118">Tips to avoid content location errors</span></span>

<span data-ttu-id="f54e4-119">다음은 콘텐츠 위치 오류의 몇 가지 추가 원인과 많은 수의 사서함을 검색할 때 방지 하는 데 도움이 되는 몇 가지 팁입니다.</span><span class="sxs-lookup"><span data-stu-id="f54e4-119">Here are some addition causes of content location errors and some tips to help you avoid them when searching large numbers of mailboxes.</span></span>

- <span data-ttu-id="f54e4-120">사용자 작업으로 인해 검색 중인 사서함이 사용 중일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f54e4-120">The mailbox being searched might be busy due to user activity.</span></span> <span data-ttu-id="f54e4-121">이 경우 검색 서비스는 사서함을 사용할 수 없게 되는 것을 방지할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f54e4-121">In this case, the search service might throttle itself to prevent the mailbox from becoming unavailable.</span></span> <span data-ttu-id="f54e4-122">이를 방지 하려면 업무 외 시간에 검색을 실행 해 봅니다.</span><span class="sxs-lookup"><span data-stu-id="f54e4-122">To avoid this, try running searches during non-business hours.</span></span>

- <span data-ttu-id="f54e4-123">검색 쿼리가 사서함에서 너무 많은 콘텐츠를 검색 하 고 있을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f54e4-123">The search query might be retrieving too much content from the mailbox.</span></span> <span data-ttu-id="f54e4-124">가능한 경우 키워드, 날짜 범위 및 검색 조건을 사용 하 여 검색 범위를 좁힙니다.</span><span class="sxs-lookup"><span data-stu-id="f54e4-124">If possible, try to narrow the scope of the search by using keywords, date ranges, and search conditions.</span></span>

- <span data-ttu-id="f54e4-125">[키워드 목록을](view-keyword-statistics-for-content-search.md#get-keyword-statistics-for-content-searches)사용 하 여 검색 쿼리를 만들 때 키워드나 키워드 구문이 너무 많습니다.</span><span class="sxs-lookup"><span data-stu-id="f54e4-125">Too many keywords or keyword phrases when you create a search query using the [keywords list](view-keyword-statistics-for-content-search.md#get-keyword-statistics-for-content-searches).</span></span> <span data-ttu-id="f54e4-126">키워드 목록을 사용 하는 검색 쿼리를 실행 하면 기본적으로 키워드 목록에 있는 각 행에 대해 별도의 검색을 실행 하 여 통계가 생성 될 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="f54e4-126">When you run a search query that uses the keywords list, the service essentially runs a separate search for each row in the keyword list so that statistics can be generated.</span></span> <span data-ttu-id="f54e4-127">검색 쿼리에서 키워드 목록을 사용 하는 경우에는 키워드 목록에서 행 수를 최소화 하거나, 숫자 키워드를 작은 목록으로 나누고, 각 키워드 목록에 대해 다른 검색을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f54e4-127">If you're using the keywords list in search queries, minimize the number of rows in the keyword list or divide the number keywords into smaller lists and create a different search for each keyword list.</span></span>

  > [!NOTE]
  > <span data-ttu-id="f54e4-128">큰 키워드 목록으로 인해 발생 하는 문제를 줄이기 위해 이제는 검색 쿼리의 키워드 목록에서 최대 20 개의 행으로 제한 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f54e4-128">To help reduce issues caused by large keyword lists, you're now limited to a maximum of 20 rows in the keyword list of a search query.</span></span>

- <span data-ttu-id="f54e4-129">동시에 같은 사서함에서 너무 많은 검색을 수행 하 고 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f54e4-129">Too many searches are being performed on the same mailbox at the same time.</span></span> <span data-ttu-id="f54e4-130">가능한 경우 한 사서함에서 한 번에 하나씩 검색을 실행 해 봅니다.</span><span class="sxs-lookup"><span data-stu-id="f54e4-130">If possible, try to run one search at a time on any one mailbox.</span></span>

- <span data-ttu-id="f54e4-131">단일 검색에서 너무 많은 사서함을 검색 하는 경우</span><span class="sxs-lookup"><span data-stu-id="f54e4-131">Searching too many mailboxes in a single search.</span></span> <span data-ttu-id="f54e4-132">매우 많은 수의 사서함을 검색할 때 콘텐츠 위치 오류의 발생 가능성이 증가 합니다.</span><span class="sxs-lookup"><span data-stu-id="f54e4-132">The probability of content location errors increases when searching a very large number of mailboxes.</span></span> <span data-ttu-id="f54e4-133">가능한 경우 각 검색에 조직에 있는 사서함의 하위 집합이 포함 되도록 여러 검색을 실행 해 봅니다.</span><span class="sxs-lookup"><span data-stu-id="f54e4-133">If possible, try to run multiple searches so that each search includes a subset of  mailboxes in your organization.</span></span>

- <span data-ttu-id="f54e4-134">사서함에서 필요한 유지 관리 작업을 수행 하 고 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f54e4-134">Required maintenance is being performed on the mailbox.</span></span> <span data-ttu-id="f54e4-135">이 문제가 가끔 발생 하는 것은 아니지만 콘텐츠 위치 오류를 받은 후에 잠시 기다린 후에 검색을 다시 시도 하세요.</span><span class="sxs-lookup"><span data-stu-id="f54e4-135">Though this cause probably occurs infrequently, wait a little while after receiving the content location error and then retry the search.</span></span>
