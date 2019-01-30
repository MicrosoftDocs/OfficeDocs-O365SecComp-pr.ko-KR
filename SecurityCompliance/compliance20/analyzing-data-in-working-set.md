---
title: 고급 eDiscovery (미리 보기)에서 작업 집합에서 데이터 분석
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
ms.openlocfilehash: a6284204fd709bcf936688f36f38f6b3283b1f98
ms.sourcegitcommit: ee28ee2b2bdfd049333c2f495d7f7780d13af4a6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2019
ms.locfileid: "29608107"
---
# <a name="analyzing-data-in-a-working-set-in-advanced-ediscovery-preview"></a><span data-ttu-id="af57f-102">고급 eDiscovery (미리 보기)에서 작업 집합에서 데이터 분석</span><span class="sxs-lookup"><span data-stu-id="af57f-102">Analyzing data in a working set in Advanced eDiscovery (Preview)</span></span>

<span data-ttu-id="af57f-p101">수집 된 문서 수 클 경우 모두 검토 하는 것이 어려울 수 있습니다. 고급 eDiscovery (미리 보기)는 다양 한 문서 정보를 손실 없이 검토 하 고 일관 된 방식으로 문서를 구성 하는데 도움이 되는 문서의 양을 줄일를 분석 하는 도구를 제공 합니다. 이러한 기능에 대 한 자세한 내용은 참조 합니다.</span><span class="sxs-lookup"><span data-stu-id="af57f-p101">When the number of collected documents is large, it can be quite difficult to review them all. Advanced eDiscovery (Preview) provides a number of tools to analyze the documents to reduce the volume of documents to be reviewed without any loss in information, and to help you organize the documents in a coherent manner. To learn more about these capabilities, see:</span></span>

- [<span data-ttu-id="af57f-106">중복 검색 근처</span><span class="sxs-lookup"><span data-stu-id="af57f-106">Near duplicate detection</span></span>](near-duplicates.md)
- [<span data-ttu-id="af57f-107">전자 메일 스레딩</span><span class="sxs-lookup"><span data-stu-id="af57f-107">Email threading</span></span>](email-threading.md)
- [<span data-ttu-id="af57f-108">테마</span><span class="sxs-lookup"><span data-stu-id="af57f-108">Themes</span></span>](themes.md)

<span data-ttu-id="af57f-109">작업 집합의 데이터를 분석 합니다.</span><span class="sxs-lookup"><span data-stu-id="af57f-109">To analyze data in a working set:</span></span>

1. <span data-ttu-id="af57f-p102">사례 분석 설정을 구성 합니다. 자세한 내용은 [검색 및 분석 설정 구성을](configure-search-analytics-settings.md)참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="af57f-p102">Configure analytics settings for your case. For more information, see [Configure search and analytics settings](configure-search-analytics-settings.md).</span></span>
2. <span data-ttu-id="af57f-112">분석 하려는 작업 집합을 엽니다.</span><span class="sxs-lookup"><span data-stu-id="af57f-112">Open the working set you wish to analyze.</span></span>
3. <span data-ttu-id="af57f-113">"관리 작업 집합"로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="af57f-113">Go to "Manage working set".</span></span>
4. <span data-ttu-id="af57f-114">"분석"을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="af57f-114">Click "Analyze".</span></span>

<span data-ttu-id="af57f-115">사용자의 경우에서 작업 탭에는 분석의 진행률을 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="af57f-115">You can check the progress of analysis in the Jobs tab in your case.</span></span>

 <span data-ttu-id="af57f-116">분석 완료 되 면 분석 보고서를 볼 수 있습니다, 사용자 작업 내에서 실행된 된 쿼리 (대 한 자세한 내용은 참조 하십시오 [설정 하면 작업 내에서 쿼리](working-set-search.md)) 분석의 출력에 설정 하 고 (자세한 내용은 참조 [에 대 한 특정 문서의 관련된 문서를 참조 하십시오. 작업 집합의 데이터를 검토](reviewing-data-in-working-set.md)).</span><span class="sxs-lookup"><span data-stu-id="af57f-116">Once analysis is completed, you can view analytics report, run queries within your working set on outputs of the analysis (for more information see [Query within your working set](working-set-search.md)), and see related documents of a given document (for more information see [Reviewing data in working set](reviewing-data-in-working-set.md)).</span></span>

## <a name="analytics-report"></a><span data-ttu-id="af57f-117">분석 보고서</span><span class="sxs-lookup"><span data-stu-id="af57f-117">Analytics report</span></span>

<span data-ttu-id="af57f-118">작업 집합에 대 한 분석 보고서를 보려면</span><span class="sxs-lookup"><span data-stu-id="af57f-118">To view a analytics report for your working set:</span></span>

1. <span data-ttu-id="af57f-119">작업 집합을 엽니다.</span><span class="sxs-lookup"><span data-stu-id="af57f-119">Open your working set.</span></span>
2. <span data-ttu-id="af57f-120">"관리 작업 집합"로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="af57f-120">Go to "Manage working set".</span></span>
3. <span data-ttu-id="af57f-121">"보고서"를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="af57f-121">Click "Report".</span></span>

<span data-ttu-id="af57f-122">보고서에는 4 개의 구성 요소가 분석에서:</span><span class="sxs-lookup"><span data-stu-id="af57f-122">The report has four components from analysis:</span></span>

- <span data-ttu-id="af57f-123">**분석 하 여** -얼마나 많은 전자 메일, 첨부 파일 및 문서를 느슨한 작업 집합에서 발견 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="af57f-123">**Breakdown** - How many emails, attachments, and loose documents were found in the working set.</span></span>

- <span data-ttu-id="af57f-124">**문서 (첨부 파일은 제외)** -얼마나 많은 느슨한 문서 위치별, 피벗의 중복 되는 값 이나 다른 문서를 정확 하 게 복제 근처에 고유한 했습니다.</span><span class="sxs-lookup"><span data-stu-id="af57f-124">**Documents (excluding attachments)** - How many loose documents were pivots, unique near duplicates of a pivot, or an exact duplicate of another document.</span></span>

- <span data-ttu-id="af57f-125">**전자 메일** -inclusives, 복사본 (포함), (포함) minuses 또는 위의 사항 얼마나 많은 전자 메일이 했습니다.</span><span class="sxs-lookup"><span data-stu-id="af57f-125">**Emails** - How many emails were inclusives, inclusive copies, inclusive minuses, or none of the above.</span></span>

- <span data-ttu-id="af57f-126">**첨부 파일** -얼마나 많은 전자 메일 첨부 된 고유 또는 작업 집합 내에서 서로 다른 전자 메일 첨부 파일의 복제 합니다.</span><span class="sxs-lookup"><span data-stu-id="af57f-126">**Attachments** - How many email attachments were unique or duplicates of a different email attachment within the working set.</span></span>