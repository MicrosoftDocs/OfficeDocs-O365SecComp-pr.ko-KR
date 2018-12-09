---
title: 콘텐츠 위치 오류를 해결 하려면 콘텐츠 검색을 다시 시도
ms.author: markjjo
author: markjjo
manager: laurawi
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection: ''
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: 해결 콘텐츠 위치 오류가 있는 콘텐츠 검색에 대 한 다시 시도 단추를 사용 합니다.
ms.openlocfilehash: 0fdc11593fec42e1f9f9b76fbbb408d9c16fd183
ms.sourcegitcommit: d5f841744b716fcf368c670009b61441f5a5eed2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2018
ms.locfileid: "27210195"
---
# <a name="retry-a-content-search-to-resolve-a-content-location-error"></a><span data-ttu-id="57214-103">콘텐츠 위치 오류를 해결 하려면 콘텐츠 검색을 다시 시도</span><span class="sxs-lookup"><span data-stu-id="57214-103">Retry a Content Search to resolve a content location error</span></span>

<span data-ttu-id="57214-104">Office 365 보안 및 규정 준수 센터의 콘텐츠 검색을 사용 하 여 매우 많은 사서함 (예: 100, 000 사서함 또는 단일 콘텐츠 검색의 검색)를 검색 하려면 다음과 비슷한 검색 오류가 발생할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="57214-104">When you use Content Search in the Office 365 Security & Compliance Center to search a very large number of mailboxes (for example, searching 100,000 mailboxes or more in a single Content Search), you may get search errors that are similar to the following:</span></span>

```
Error

The search on the following locations failed:

User1@contoso.com: Problem in processing the request. Please try again later. If you keep getting this error, contact your admin. (CS008-009)

User2@contoso.com: Application error occurred. Please try again later. (CS012-002)
```

<span data-ttu-id="57214-p101">이러한 오류 (오류 코드와 함께 CS008 009 및 CS012-002) 콘텐츠 검색을 특정 콘텐츠 위치; 검색 하지 못했음을 나타냅니다. 이 예제에서는 두 사서함 받지 검색 됩니다. 이러한 오류는 콘텐츠 검색의 상태 정보 플라이 아웃 페이지에 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="57214-p101">These errors (with error codes of CS008-009 and CS012-002) indicate that Content Search failed to search specific content locations; in this example, two mailboxes weren't searched. These errors are displayed on the status details flyout page of the Content Search.</span></span>

## <a name="cause-of-content-location-errors"></a><span data-ttu-id="57214-107">콘텐츠 위치 오류 원인입니다</span><span class="sxs-lookup"><span data-stu-id="57214-107">Cause of content location errors</span></span>

<span data-ttu-id="57214-p102">많은 수의 사서함을 검색할 때 검색은 다양 한 Microsoft 데이터 센터의 서버 전체에 배포 합니다. 언제 든 하나는 특정 서버 다시 부팅 상태에서 또는 중복 복사본에 대 한 장애 조치 프로세스에서 일 수 있습니다. 두이 경우 모두에서 데이터를 검색 하는 콘텐츠 검색 요청 시간 초과 됩니다. 앞의 예제에서는 실패 한 사서함에 대 한 오류 검색 시간 초과 결과 했습니다.</span><span class="sxs-lookup"><span data-stu-id="57214-p102">When searching a large number of mailboxes, the search is distributed across thousands of servers in a Microsoft datacenter. At any one time, specific servers could be in reboot state or in the process of failing over to redundant copies. In either of these cases, the Content Search's request to retrieve data will timeout. In the previous example, the errors for the mailboxes that failed were the result of the search timing out.</span></span>

## <a name="resolving-content-location-errors"></a><span data-ttu-id="57214-112">콘텐츠 위치 오류를 해결 하기</span><span class="sxs-lookup"><span data-stu-id="57214-112">Resolving content location errors</span></span>

<span data-ttu-id="57214-p103">검색을 다시 시작 해도 다른 서버에서 비슷한 오류 종종 발생 합니다. 검색 시스템을 다시 시작 하는 대신 검색 결과 페이지의 위쪽에 표시 되는 **다시 시도** 단추를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="57214-p103">Restarting the search will often result in similar errors on different servers. Instead of restarting the search, click the **Retry** button that is displayed at the top of the search results page.</span></span>

![콘텐츠 위치 오류를 해결 하 고 다시 시도 단추 클릭](media/retrycontentsearch3.png)

<span data-ttu-id="57214-p104">다시 시도 실패 한 사서함에 대해서만 검색 됩니다. 검색을 다시 시도 하는 경우 다른 결과 성공적으로 반환 된 그대로 유지 됩니다.</span><span class="sxs-lookup"><span data-stu-id="57214-p104">This will result in the retrying the search only for the mailboxes that failed. When you retry the search, the other results that were successfully returned are retained.</span></span>

## <a name="tips-to-avoid-content-location-errors"></a><span data-ttu-id="57214-118">콘텐츠 위치 오류를 방지 하기 위한 팁</span><span class="sxs-lookup"><span data-stu-id="57214-118">Tips to avoid content location errors</span></span>

<span data-ttu-id="57214-119">일부 추가 콘텐츠 위치 오류의 원인과 유용한 팁 많은 수의 사서함을 검색 하는 경우이 방지 하기 위해 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="57214-119">Here are some addition causes of content location errors and some tips to help you avoid them when searching large numbers of mailboxes.</span></span>

- <span data-ttu-id="57214-p105">검색이 수행 되는 사서함 사용자 활동으로 인해 과부하 상태일 수 있습니다. 이 경우 검색 서비스에서 사용할 수 없게 되는 사서함을 방지 하기 위해 자체 제한 될 수 있습니다. 이 문제를 방지 하려면 검색을 실행 하는 동안 업무 시간을 봅니다.</span><span class="sxs-lookup"><span data-stu-id="57214-p105">The mailbox being searched might be busy due to user activity. In this case, the search service might throttle itself to prevent the mailbox from becoming unavailable. To avoid this, try running searches during non-business hours.</span></span>

- <span data-ttu-id="57214-p106">사서함에서 검색 쿼리를 너무 많은 콘텐츠를 검색 될 수 있습니다. 가능 하면, 키워드, 날짜 범위 및 검색 조건을 사용 하 여 검색 범위를 좁힐 하려고 합니다.</span><span class="sxs-lookup"><span data-stu-id="57214-p106">The search query might be retrieving too much content from the mailbox. If possible, try to narrow the scope of the search by using keywords, date ranges, and search conditions.</span></span>

- <span data-ttu-id="57214-p107">키워드 또는 키워드 구를 [키워드 목록을](view-keyword-statistics-for-content-search.md#get-keyword-statistics-for-content-searches)사용 하 여 검색 쿼리를 만들 때 너무 많습니다. 키워드 목록을 사용 하는 검색 쿼리를 실행 하면 서비스가 기본적으로 실행 각 행에 대 한 별도 검색 키워드 목록에서 통계를 생성할 수 있도록 합니다. 키워드 목록 검색 쿼리를 사용 하는 경우 키워드 목록에 있는 행의 수를 최소화 또는 더 작은 목록 번호 키워드 나누는 하 고 각 키워드 목록에 대 한 다양 한 검색을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="57214-p107">Too many keywords or keyword phrases when you create a search query using the [keywords list](view-keyword-statistics-for-content-search.md#get-keyword-statistics-for-content-searches). When you run a search query that uses the keywords list, the service essentially runs a separate search for each row in the keyword list so that statistics can be generated. If you're using the keywords list in search queries, minimize the number of rows in the keyword list or divide the number keywords into smaller lists and create a different search for each keyword list.</span></span>

  > [!NOTE]
  > <span data-ttu-id="57214-128">큰 키워드 목록에 의해 발생 하는 문제를 줄일 자신이 지금 검색 쿼리 키워드 목록에서 20 행의 최대 수 있도록 제한 합니다.</span><span class="sxs-lookup"><span data-stu-id="57214-128">To help reduce issues caused by large keyword lists, you're now limited to a maximum of 20 rows in the keyword list of a search query.</span></span>

- <span data-ttu-id="57214-p108">동시에 같은 사서함에서 너무 많은 경우 검색을 수행 중인 됩니다. 가능한 경우 모든 하나 이상의 사서함에 한번에 하나의 검색을 실행 하려고 합니다.</span><span class="sxs-lookup"><span data-stu-id="57214-p108">Too many searches are being performed on the same mailbox at the same time. If possible, try to run one search at a time on any one mailbox.</span></span>

- <span data-ttu-id="57214-p109">단일 검색에서 너무 많은 수의 사서함을 검색 합니다. 콘텐츠 위치 오류의 확률 매우 많은 사서함을 검색할 때 증가 합니다. 가능 하면 조직에서 사서함의 하위 집합을 포함 하는 각 검색 되도록 여러 검색을 실행 하려고 합니다.</span><span class="sxs-lookup"><span data-stu-id="57214-p109">Searching too many mailboxes in a single search. The probability of content location errors increases when searching a very large number of mailboxes. If possible, try to run multiple searches so that each search includes a subset of  mailboxes in your organization.</span></span>

- <span data-ttu-id="57214-p110">사서함에서 수행 되 필요한 유지 관리 합니다. 이러한 원인 자주 발생 했을 경우에 약간 콘텐츠 위치 오류를 받은 후 하는 동안 기다린 다음 검색을 다시 시도 합니다.</span><span class="sxs-lookup"><span data-stu-id="57214-p110">Required maintenance is being performed on the mailbox. Though this cause probably occurs infrequently, wait a little while after receiving the content location error and then retry the search.</span></span>
