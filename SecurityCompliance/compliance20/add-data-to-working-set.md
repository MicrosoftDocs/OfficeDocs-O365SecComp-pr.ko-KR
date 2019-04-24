---
title: 검색 결과를 작업 집합에 추가
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
ms.openlocfilehash: 7830b483190a69e6055fae369580064c5df42f49
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32243395"
---
# <a name="add-search-results-to-a-working-set"></a><span data-ttu-id="fdc66-102">검색 결과를 작업 집합에 추가</span><span class="sxs-lookup"><span data-stu-id="fdc66-102">Add search results to a working set</span></span>

<span data-ttu-id="fdc66-103">Exchange, SharePoint 및 비즈니스용 OneDrive에 대 한 검색을 식별 하 고 culled 결과를 작업 집합에 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fdc66-103">After you've identified and culled with searches against Exchange, SharePoint and OneDrive for business, you can add the results to a working set.</span></span> <span data-ttu-id="fdc66-104">작업 집합은 라이트닝 fast 검색 결과에 대해 인덱싱할 수 있는 정적 문서 집합을 나타내고, 전자 메일 스레드 식별을 분석 하 고, 중복 검색 및 테마를 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="fdc66-104">Working sets represent a static set of documents that we will index for lightning fast search results, analyze for email thread identification, near duplicate detection and themes.</span></span>  <span data-ttu-id="fdc66-105">office 365에서 수집한 데이터를 사용 하 여 부재 중인 365 데이터 원본의 데이터를 실시간으로 나란히 추가할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fdc66-105">You can also add data from Non-Office 365 data sources to live side by side with the data you collect from Office 365.</span></span>

<span data-ttu-id="fdc66-106">작업 집합에 데이터를 추가 하려면 먼저 검색을 선택 하 여 검색 결과 플라이 아웃에서 *+ 작업 집합에 결과 추가* 단추를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="fdc66-106">To add data to a working set, start by selecting a search, in the search results fly out, click the *+ Add results to working set* button.</span></span>

![작업 집합에 데이터 추가](../media/c1b4fc00-7a15-4587-b9b0-ce594bb02e4d.png)

<span data-ttu-id="fdc66-108">그런 다음 기존 작업 집합이 나 *새 작업 집합*에 추가 하도록 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fdc66-108">You can then choose to add to an existing working set or a *New working set*.</span></span>  <span data-ttu-id="fdc66-109">새 작업 집합에 추가 하는 경우 이름을 지정 하 고 마지막으로 *추가* 단추를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="fdc66-109">If adding to a new working set, specify the name and finally click the *Add* button.</span></span>

![작업 집합 선택](../media/e8c6ab51-da8d-4c39-9b21-26bfdf453fb9.png)

<span data-ttu-id="fdc66-111">작업 집합에 데이터를 추가 하는 것은 장기 실행 프로세스 이므로 작업 탭 또는 *검색* 탭의 *작업 집합 상태* 열에서 진행률을 추적할 수 있습니다.  이 프로세스에는 Office 365에서 항목 수집 및 마지막으로 & 인덱싱이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="fdc66-111">Adding data to a working set is a long running process, you can either track the progress in the Jobs tab or in the *Working set status* column in the *Searches* tab.  The process includes gathering items from Office 365 and finally Ingestion & Indexing.</span></span>  <span data-ttu-id="fdc66-112">작업 집합 처리가 완료 되 면 작업 집합 탭을 클릭 한 다음 작업 집합을 클릭 하 \*\* 여 작업 세트로 이동할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fdc66-112">Once working set processing is completed, you can navigate to the working set by clicking on the *Working Sets* tab and then clicking on the working set.</span></span>  <span data-ttu-id="fdc66-113">그런 다음 이동 하 여 관련 데이터를 검색, 검토, 태그 지정 및 내보낼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fdc66-113">You can then move on to searching, reviewing, tagging and exporting any relevant data.</span></span>

## <a name="adding-a-sample-to-a-working-set"></a><span data-ttu-id="fdc66-114">작업 집합에 예제 추가</span><span class="sxs-lookup"><span data-stu-id="fdc66-114">Adding a sample to a working set</span></span>

<span data-ttu-id="fdc66-115">검색에서 검색 한 모든 문서를 수집 하기 전에 검색 결과의 유효성을 보다 thorougly 하는 경우 모든 항목을 추가 하는 대신 검색 결과의 무작위 샘플을 작업 집합에 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fdc66-115">If you would like to validate your search results more thorougly before collecting all documents that were retrieved by your search, you can add a random sample of the search results to a working set instead of adding everything.</span></span>

<span data-ttu-id="fdc66-116">작업 집합에 샘플을 추가 하려면 먼저 검색을 선택 하 고 검색 결과 플라이 아웃에서 *예제* 단추를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="fdc66-116">To add a sample to a working set, start by selecting a search, in the search results flyout, click *Sample* button.</span></span>

<span data-ttu-id="fdc66-117">그런 다음 표본 추출의 매개 변수를 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fdc66-117">You can then choose the parameter of your sampling.</span></span> <span data-ttu-id="fdc66-118">다음 두 가지 옵션이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fdc66-118">There are two options:</span></span>
- <span data-ttu-id="fdc66-119">신뢰 수준 및 간격: 지정 된 통계 매개 변수를 충족 하기 위해 샘플 크기를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="fdc66-119">Confidence level and interval: sample size will be chosen to satisfy the given statistical parameters.</span></span>
- <span data-ttu-id="fdc66-120">백분율: 검색에 의해 반환 된 항목 수와 선택한 매개 변수를 기준으로 샘플 크기가 결정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="fdc66-120">Percentage: sample size will be determined based on the number of items that was returned by the search, and the chosen parameter.</span></span>

<span data-ttu-id="fdc66-121">마지막으로 예제를 추가할 작업 집합을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="fdc66-121">Finally, choose the working set to add the sample to.</span></span> <span data-ttu-id="fdc66-122">여기에서 작업 집합에 전체 검색을 추가 하는 것과 마찬가지로 프로세스의 상태를 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fdc66-122">From there, you can check the status of the process just as you would for adding a whole search into a working set.</span></span> 