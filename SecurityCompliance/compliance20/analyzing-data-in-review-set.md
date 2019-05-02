---
title: 고급 eDiscovery에서 검토 집합의 데이터 분석
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
ms.openlocfilehash: c765234e1aa0738415f66f90b66ebce0fcab2505
ms.sourcegitcommit: 4ce350f8f3eb597587945a8ac9b33e9793440c64
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/01/2019
ms.locfileid: "33527234"
---
# <a name="analyze-data-in-a-review-set-in-advanced-ediscovery"></a><span data-ttu-id="300d6-102">고급 eDiscovery에서 검토 집합의 데이터 분석</span><span class="sxs-lookup"><span data-stu-id="300d6-102">Analyze data in a review set in Advanced eDiscovery</span></span>

<span data-ttu-id="300d6-103">수집 된 문서 수가 크면 검토 하는 것이 상당히 어려울 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="300d6-103">When the number of collected documents is large, it can be quite difficult to review them all.</span></span> <span data-ttu-id="300d6-104">고급 eDiscovery에서는 문서를 분석 하 여 정보 손실 없이 검토할 문서 크기를 줄이고 일관 된 방식으로 문서를 구성 하는 데 도움이 되는 다양 한 도구를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="300d6-104">Advanced eDiscovery provides a number of tools to analyze the documents to reduce the volume of documents to be reviewed without any loss in information, and to help you organize the documents in a coherent manner.</span></span> <span data-ttu-id="300d6-105">이러한 기능에 대 한 자세한 내용은 다음 항목을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="300d6-105">To learn more about these capabilities, see:</span></span>

- [<span data-ttu-id="300d6-106">중복에 가까운 검색</span><span class="sxs-lookup"><span data-stu-id="300d6-106">Near duplicate detection</span></span>](near-duplicates.md)

- [<span data-ttu-id="300d6-107">전자 메일 스레드</span><span class="sxs-lookup"><span data-stu-id="300d6-107">Email threading</span></span>](email-threading.md)

- [<span data-ttu-id="300d6-108">테마</span><span class="sxs-lookup"><span data-stu-id="300d6-108">Themes</span></span>](themes.md)

<span data-ttu-id="300d6-109">검토 집합에서 데이터를 분석 하려면 다음을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="300d6-109">To analyze data in a review set:</span></span>

1. <span data-ttu-id="300d6-110">사례에 대 한 분석 설정을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="300d6-110">Configure analytics settings for your case.</span></span> <span data-ttu-id="300d6-111">자세한 내용은 [Configure search and analytics settings](configure-search-analytics-settings.md)을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="300d6-111">For more information, see [Configure search and analytics settings](configure-search-analytics-settings.md).</span></span>

2. <span data-ttu-id="300d6-112">분석 하려는 검토 집합을 엽니다.</span><span class="sxs-lookup"><span data-stu-id="300d6-112">Open the review set you want to analyze.</span></span>

3. <span data-ttu-id="300d6-113">**검토 설정 관리**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="300d6-113">Click **Manage review set**.</span></span>

4. <span data-ttu-id="300d6-114">**분석**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="300d6-114">Click **Analyze**.</span></span>

<span data-ttu-id="300d6-115">사례에 대 한 **작업** 탭에서 분석 진행률을 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="300d6-115">You can check the progress of analysis on the **Jobs** tab of the case.</span></span>

 <span data-ttu-id="300d6-116">분석이 완료 되 면 분석 보고서를 보고, 분석 출력에 대 한 검토 집합 내에서 쿼리를 실행 하 고 ( [검토 집합 내의 쿼리](review-set-search.md)참조), 지정 된 문서의 관련 문서를 볼 수 있습니다 ( [검토 집합의 데이터 검토](reviewing-data-in-review-set.md)참조).</span><span class="sxs-lookup"><span data-stu-id="300d6-116">After analysis is completed, you can view analytics report, run queries within your review set on outputs of the analysis (see [Query within your review set](review-set-search.md)), and see related documents of a given document (see [Reviewing data in review set](reviewing-data-in-review-set.md)).</span></span>

## <a name="analytics-report"></a><span data-ttu-id="300d6-117">분석 보고서</span><span class="sxs-lookup"><span data-stu-id="300d6-117">Analytics report</span></span>

<span data-ttu-id="300d6-118">검토 집합에 대 한 분석 보고서를 보려면:</span><span class="sxs-lookup"><span data-stu-id="300d6-118">To view a analytics report for a review set:</span></span>

1. <span data-ttu-id="300d6-119">검토 집합을 엽니다.</span><span class="sxs-lookup"><span data-stu-id="300d6-119">Open the review set.</span></span>

2. <span data-ttu-id="300d6-120">**검토 설정 관리**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="300d6-120">Click **Manage review set**.</span></span>

3. <span data-ttu-id="300d6-121">**보고서**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="300d6-121">Click **Report**.</span></span>

<span data-ttu-id="300d6-122">보고서에는 분석을 통해 다음과 같은 4 가지 구성 요소가 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="300d6-122">The report has four components from analysis:</span></span>

- <span data-ttu-id="300d6-123">**분석 결과** -검토 집합에서 찾은 전자 메일 메시지, 첨부 파일 및 느슨한 문서 수입니다.</span><span class="sxs-lookup"><span data-stu-id="300d6-123">**Breakdown** - How many email messages, attachments, and loose documents were found in the review set.</span></span>

- <span data-ttu-id="300d6-124">**문서 (첨부 파일 제외)** -피벗, 중복 되는 항목에 대 한 고유 하지 않은 문서 또는 다른 문서와 정확히 일치 하는 복사본의 수입니다.</span><span class="sxs-lookup"><span data-stu-id="300d6-124">**Documents (excluding attachments)** - How many loose documents were pivots, unique near duplicates of a pivot, or an exact duplicate of another document.</span></span>

- <span data-ttu-id="300d6-125">**전자 메일** -inclusives, 포함 복사본, 포함 minuses 또는이 중 어느 것도 사용 되지 않은 전자 메일 메시지의 수입니다.</span><span class="sxs-lookup"><span data-stu-id="300d6-125">**Emails** - How many email messages were inclusives, inclusive copies, inclusive minuses, or none of the above.</span></span>

- <span data-ttu-id="300d6-126">**첨부 파일** -검토 집합에 있는 다른 전자 메일 첨부 파일의 고유 복사본 또는 중복 된 전자 메일 첨부 파일의 수입니다.</span><span class="sxs-lookup"><span data-stu-id="300d6-126">**Attachments** - How many email attachments were unique or duplicates of a another email attachment in the review set.</span></span>