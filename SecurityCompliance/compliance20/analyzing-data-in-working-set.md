---
title: Advanced eDiscovery (Preview)의 작업 집합에서 데이터 분석
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
ms.openlocfilehash: e3f3e863423fe4312a944eb6f04a58182e11665c
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32243239"
---
# <a name="analyze-data-in-a-working-set-in-advanced-ediscovery-preview"></a><span data-ttu-id="c9f69-102">Advanced eDiscovery (Preview)의 작업 집합에서 데이터 분석</span><span class="sxs-lookup"><span data-stu-id="c9f69-102">Analyze data in a working set in Advanced eDiscovery (Preview)</span></span>

<span data-ttu-id="c9f69-103">수집 된 문서 수가 크면 검토 하는 것이 상당히 어려울 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c9f69-103">When the number of collected documents is large, it can be quite difficult to review them all.</span></span> <span data-ttu-id="c9f69-104">Advanced eDiscovery (Preview)에서는 문서를 분석 하 여 정보 손실 없이 검토할 문서 크기를 줄이고, 일관 된 방식으로 문서를 구성 하는 데 도움이 되는 다양 한 도구를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="c9f69-104">Advanced eDiscovery (Preview) provides a number of tools to analyze the documents to reduce the volume of documents to be reviewed without any loss in information, and to help you organize the documents in a coherent manner.</span></span> <span data-ttu-id="c9f69-105">이러한 기능에 대 한 자세한 내용은 다음 항목을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="c9f69-105">To learn more about these capabilities, see:</span></span>

- [<span data-ttu-id="c9f69-106">중복에 가까운 검색</span><span class="sxs-lookup"><span data-stu-id="c9f69-106">Near duplicate detection</span></span>](near-duplicates.md)
- [<span data-ttu-id="c9f69-107">전자 메일 스레드</span><span class="sxs-lookup"><span data-stu-id="c9f69-107">Email threading</span></span>](email-threading.md)
- [<span data-ttu-id="c9f69-108">테마</span><span class="sxs-lookup"><span data-stu-id="c9f69-108">Themes</span></span>](themes.md)

<span data-ttu-id="c9f69-109">작업 집합의 데이터를 분석 하려면 다음을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="c9f69-109">To analyze data in a working set:</span></span>

1. <span data-ttu-id="c9f69-110">사례에 대 한 분석 설정을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="c9f69-110">Configure analytics settings for your case.</span></span> <span data-ttu-id="c9f69-111">자세한 내용은 [Configure search and analytics settings](configure-search-analytics-settings.md)을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="c9f69-111">For more information, see [Configure search and analytics settings](configure-search-analytics-settings.md).</span></span>
2. <span data-ttu-id="c9f69-112">분석할 작업 집합을 엽니다.</span><span class="sxs-lookup"><span data-stu-id="c9f69-112">Open the working set you wish to analyze.</span></span>
3. <span data-ttu-id="c9f69-113">"작업 집합 관리"로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="c9f69-113">Go to "Manage working set".</span></span>
4. <span data-ttu-id="c9f69-114">"분석"을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="c9f69-114">Click "Analyze".</span></span>

<span data-ttu-id="c9f69-115">해당 사례의 작업 탭에서 분석 진행률을 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c9f69-115">You can check the progress of analysis in the Jobs tab in your case.</span></span>

 <span data-ttu-id="c9f69-116">분석이 완료 되 면 분석 보고서를 확인 하 여 작업 집합 내에서 쿼리를 실행 하 고 ( [작업 집합 내의 쿼리](working-set-search.md)참조), 지정 된 문서의 관련 문서를 볼 수 있습니다 (자세한 내용은 다음 항목을 참조 하십시오 [. 작업 집합의 데이터 검토](reviewing-data-in-working-set.md)</span><span class="sxs-lookup"><span data-stu-id="c9f69-116">Once analysis is completed, you can view analytics report, run queries within your working set on outputs of the analysis (for more information see [Query within your working set](working-set-search.md)), and see related documents of a given document (for more information see [Reviewing data in working set](reviewing-data-in-working-set.md)).</span></span>

## <a name="analytics-report"></a><span data-ttu-id="c9f69-117">분석 보고서</span><span class="sxs-lookup"><span data-stu-id="c9f69-117">Analytics report</span></span>

<span data-ttu-id="c9f69-118">작업 집합에 대 한 분석 보고서를 보려면:</span><span class="sxs-lookup"><span data-stu-id="c9f69-118">To view a analytics report for your working set:</span></span>

1. <span data-ttu-id="c9f69-119">작업 집합을 엽니다.</span><span class="sxs-lookup"><span data-stu-id="c9f69-119">Open your working set.</span></span>
2. <span data-ttu-id="c9f69-120">"작업 집합 관리"로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="c9f69-120">Go to "Manage working set".</span></span>
3. <span data-ttu-id="c9f69-121">"보고서"를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="c9f69-121">Click "Report".</span></span>

<span data-ttu-id="c9f69-122">보고서에는 분석을 통해 다음과 같은 4 가지 구성 요소가 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c9f69-122">The report has four components from analysis:</span></span>

- <span data-ttu-id="c9f69-123">**분석 결과** -작업 집합에서 찾은 전자 메일, 첨부 파일 및 느슨한 문서 수입니다.</span><span class="sxs-lookup"><span data-stu-id="c9f69-123">**Breakdown** - How many emails, attachments, and loose documents were found in the working set.</span></span>

- <span data-ttu-id="c9f69-124">**문서 (첨부 파일 제외)** -피벗, 중복 되는 항목에 대 한 고유 하지 않은 문서 또는 다른 문서와 정확히 일치 하는 복사본의 수입니다.</span><span class="sxs-lookup"><span data-stu-id="c9f69-124">**Documents (excluding attachments)** - How many loose documents were pivots, unique near duplicates of a pivot, or an exact duplicate of another document.</span></span>

- <span data-ttu-id="c9f69-125">**전자 메일** -inclusives, 포함 복사본, 포함 minuses, 또는 없음 중에서 어떤 전자 메일을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c9f69-125">**Emails** - How many emails were inclusives, inclusive copies, inclusive minuses, or none of the above.</span></span>

- <span data-ttu-id="c9f69-126">**첨부 파일** -작업 집합 내에 있는 다른 전자 메일 첨부 파일의 고유 또는 중복 된 전자 메일 첨부 파일의 수입니다.</span><span class="sxs-lookup"><span data-stu-id="c9f69-126">**Attachments** - How many email attachments were unique or duplicates of a different email attachment within the working set.</span></span>