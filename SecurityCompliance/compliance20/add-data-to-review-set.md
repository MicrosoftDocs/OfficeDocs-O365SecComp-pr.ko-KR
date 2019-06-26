---
title: 검색 결과를 검토 집합에 추가
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
description: ''
ms.openlocfilehash: fac8ab829107befaa1a3f8b3afe1cec8d3468f1b
ms.sourcegitcommit: bac1b5be5db381e6f8d8f652cff1f8ef4d7f6330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2019
ms.locfileid: "35233325"
---
# <a name="add-search-results-to-a-review-set"></a><span data-ttu-id="5c9ab-102">검색 결과를 검토 집합에 추가</span><span class="sxs-lookup"><span data-stu-id="5c9ab-102">Add search results to a review set</span></span>

<span data-ttu-id="5c9ab-103">검색 결과가 만족 스 러 우면 해당 검색 결과를 검토 하 고 분석할 준비가 되 면 대/소문자에서 검토 집합에 해당 결과를 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5c9ab-103">When you're satisfied with the results of a search and you're ready to review and analyze those search results, you can add them to a review set in the case.</span></span> <span data-ttu-id="5c9ab-104">원본 데이터를 검토 집합에 복사 하면 테마 검색, 거의 중복 검색 및 전자 메일 스레드 식별과 같은 고급 분석 도구를 제공 하 여 검토 및 분석 프로세스를 쉽게 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5c9ab-104">Copying the original data to the review set also facilitates the review and analysis process by providing you with advanced analytics tools such as themes detection, near-duplicate detection, and email thread identification.</span></span> <span data-ttu-id="5c9ab-105">Office 365에서 수집한 데이터 외에도 해당 데이터를 검토할 수 있도록 부재 외 365 데이터 원본의 데이터를 검토 집합에 추가할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5c9ab-105">You can also add data from non-Office 365 data sources to a review set so that you can review that data in addition to the data you collect from Office 365.</span></span>

<span data-ttu-id="5c9ab-106">검토 집합에 검색 결과를 추가할 때 (사례 검토 집합 탭에 있는 검토 집합) \*\*\*\* 다음과 같은 상황이 발생 합니다.</span><span class="sxs-lookup"><span data-stu-id="5c9ab-106">When you add the results of a search to a review set (review sets are on the **Review sets** tab of the case), the following things occur:</span></span>

- <span data-ttu-id="5c9ab-107">검색이 다시 실행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5c9ab-107">The search is run again.</span></span> <span data-ttu-id="5c9ab-108">즉, 검토 집합에 복사 되는 실제 검색 결과는 검색을 마지막으로 실행 했을 때 반환 된 예상 결과와 다를 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5c9ab-108">This means the actual search results copied to the review set may be different than the estimated results that were returned when the search was last run.</span></span>

- <span data-ttu-id="5c9ab-109">검색 결과의 모든 항목은 live Office 365 서비스의 원본 데이터 원본에서 복사 되 고 Microsoft 클라우드의 안전한 Azure 저장소 위치로 복사 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5c9ab-109">All items in the search results are copied from the original data source in the live Office 365 services, and copied to a secure Azure storage location in the Microsoft cloud.</span></span>

- <span data-ttu-id="5c9ab-110">모든 항목 (콘텐츠 및 메타 데이터 포함)은 사례 데이터를 검토 하는 동안 검토 집합의 모든 데이터를 완벽 하 게 검색할 수 있도록 다시 인덱싱됩니다.</span><span class="sxs-lookup"><span data-stu-id="5c9ab-110">All items (including the content and metadata) are re-indexed so that all data in the review set is fully searchable during the review of the case data.</span></span> <span data-ttu-id="5c9ab-111">사례 조사 중에 검토 집합에서 데이터를 검색할 때 데이터를 정밀 하 고 빠르게 검색할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5c9ab-111">Re-indexing the data results in thorough and very fast searches when you search the data in the review set during the case investigation.</span></span>

<span data-ttu-id="5c9ab-112">검토 집합에 데이터를 추가 하려면 검색 탭에서 검색을 클릭 \*\*\*\* 하 고 플라이 아웃 페이지에서 **집합을 검토 하려면 결과 추가를** 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="5c9ab-112">To add data to a review set, click a search on the **Searches** tab, and then click **Add results to review set** on the flyout page.</span></span>

![검토 집합에 데이터 추가](../media/c1b4fc00-7a15-4587-b9b0-ce594bb02e4d.png)

<span data-ttu-id="5c9ab-114">기존 검토 집합에 추가 하거나 새 검토 집합을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5c9ab-114">You can add to an existing review set or create a new review set.</span></span>  <span data-ttu-id="5c9ab-115">새 검토 집합에 추가 하는 경우 이름을 지정 하 고 **추가**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="5c9ab-115">If adding to a new review set, specify the name and then click **Add**.</span></span>

![검토 집합 선택](../media/e8c6ab51-da8d-4c39-9b21-26bfdf453fb9.png)

<span data-ttu-id="5c9ab-117">검토 집합에 데이터를 추가 하는 것은 장시간 실행 되는 프로세스입니다.</span><span class="sxs-lookup"><span data-stu-id="5c9ab-117">Adding data to a review set is a long-running process.</span></span> <span data-ttu-id="5c9ab-118">이 프로세스에는 Office 365 (예: 사서함 및 사이트)의 원본 데이터 원본에서 항목을 수집 하 여 Azure 저장소 위치로 복사한 다음 (이 복사 프로세스는 수집이 라고도 함 \*\*) 항목을 다시 인덱싱하는 작업이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5c9ab-118">This process includes gathering items from the original data sources in Office 365 (for example, from mailboxes and sites), copying them to the Azure storage location (this copying process is also called *ingestion*), and then re-indexing the items.</span></span> <span data-ttu-id="5c9ab-119">**작업** 탭 또는 **검색** 탭의 진행 상태를 추적 하 여 **추가 된 데이터를 검토 집합** 열에서 모니터링할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5c9ab-119">You can track the progress on the **Jobs** tab or on the **Searches** tab by monitoring the status in the **Added data to review set** column.</span></span> <span data-ttu-id="5c9ab-120">검토 집합 처리가 완료 되 면 사례에서 **검토 집합** 탭을 클릭 하 고 검토 집합을 클릭 하 여 검토 집합에서 데이터를 필터링, 검토, 태그 지정 및 내보내는 프로세스를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="5c9ab-120">After the review set processing is completed, click the **Review sets** tab in the case, and click the review set to start the process of filtering, reviewing, tagging, and exporting data in the review set.</span></span>

## <a name="add-a-sample-to-a-review-set"></a><span data-ttu-id="5c9ab-121">검토 집합에 샘플 추가</span><span class="sxs-lookup"><span data-stu-id="5c9ab-121">Add a sample to a review set</span></span>

<span data-ttu-id="5c9ab-122">검색 결과의 유효성을 검토 집합에 추가 하기 전에 보다 철저히 확인 하려는 경우 모든 항목을 추가 하는 대신 검토 집합에 검색 결과의 예제를 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5c9ab-122">If you want to validate the results of a search more thoroughly before adding all of them to a review set, you can add a sample of the search results to a review set instead of adding everything.</span></span>

<span data-ttu-id="5c9ab-123">검토 집합에 샘플을 추가 하려면 검색 탭에서 검색을 클릭 하 \*\*\*\* 고 플라이 아웃 페이지에서 **샘플** 을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="5c9ab-123">To add a sample to a review set, click a search on the **Searches** tab and click **Sample** on the flyout page.</span></span> <span data-ttu-id="5c9ab-124">**매개 변수 샘플링** 페이지에서 다음 옵션 중 하나를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="5c9ab-124">On the **Sampling parameters** page, choose one of the following options:</span></span>

- <span data-ttu-id="5c9ab-125">**신뢰 수준%** 및 **신뢰도 간격%** -검토 집합에 추가 된 항목은 설정한 통계 매개 변수에 따라 결정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5c9ab-125">**Confidence level %** and **Confidence interval %** – The items added to the review set will be determined by the statistical parameters that you set.</span></span> <span data-ttu-id="5c9ab-126">일반적으로 결과를 샘플링할 때 신뢰 수준과 간격을 사용 하는 경우에는 드롭다운 상자에서이를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5c9ab-126">If you typically use a confidence level and interval when sampling results, specify them in the drop-down boxes.</span></span> <span data-ttu-id="5c9ab-127">그렇지 않으면 기본 설정을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="5c9ab-127">Otherwise, use the default settings.</span></span>

- <span data-ttu-id="5c9ab-128">**Random 표본%** – 검토 집합에 추가 되는 항목은 검색에서 반환 되는 총 항목 수에 대 한 지정 된 백분율을 임의로 선택 하 여 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5c9ab-128">**Random sample %** – The items added to the review set is based on a random selection of the specified percentage of the total number of items returned by the search.</span></span>

<span data-ttu-id="5c9ab-129">이전 옵션 중 하나를 선택 하 고 구성한 후에는 예제를 추가할 검토 집합을 선택한 다음 **보내기를**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="5c9ab-129">After selecting and configuring one of the previous options, choose a review set to add the sample to and then click **Send**.</span></span> <span data-ttu-id="5c9ab-130">다시 말하지만 **작업** 탭 이나 **검색** 탭에서 **검토 집합에 추가 된 데이터** 열에서 상태를 모니터링 하 여 진행 상황을 추적할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5c9ab-130">Again, you can track the progress on the **Jobs** tab or on the **Searches** tab by monitoring the status in the **Added data to review set** column.</span></span>