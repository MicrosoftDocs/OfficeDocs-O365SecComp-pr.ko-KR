---
title: 신속한 조사를 위한 분석 실행
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
ms.openlocfilehash: 7462b415c2e5b0a66c08bb9b5abb647f366e9785
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/17/2019
ms.locfileid: "34153660"
---
# <a name="run-analytics-to-investigate-faster"></a><span data-ttu-id="433ae-102">신속한 조사를 위한 분석 실행</span><span class="sxs-lookup"><span data-stu-id="433ae-102">Run analytics to investigate faster</span></span>

<span data-ttu-id="433ae-103">증거 수집이 크면 검토 하기가 어려울 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="433ae-103">When an evidence collection is large, it can be difficult to review them all.</span></span> <span data-ttu-id="433ae-104">증명 정보 집합에 동일 하거나 유사한 전자 메일 메시지 또는 문서의 복사본이 여러 개 포함 되는 경우가 많습니다.</span><span class="sxs-lookup"><span data-stu-id="433ae-104">A set of evidence often includes multiple copies of the same or similar email messages or documents.</span></span> <span data-ttu-id="433ae-105">데이터 조사 (미리 보기)는 정보 손실 없이 검토 해야 하는 문서 크기를 줄이는 데 도움이 되는 다양 한 분석 도구를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="433ae-105">Data Investigations (Preview) provides a number of analytics tools that can help you reduce the volume of documents that need to be reviewed without any loss in information.</span></span> <span data-ttu-id="433ae-106">이러한 기능에 대 한 자세한 내용은 다음 항목을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="433ae-106">To learn more about these capabilities, see:</span></span>

- [<span data-ttu-id="433ae-107">중복에 가까운 검색</span><span class="sxs-lookup"><span data-stu-id="433ae-107">Near duplicate detection</span></span>](near-duplicates.md)

- [<span data-ttu-id="433ae-108">전자 메일 스레드</span><span class="sxs-lookup"><span data-stu-id="433ae-108">Email threading</span></span>](email-threading.md)

- [<span data-ttu-id="433ae-109">테마</span><span class="sxs-lookup"><span data-stu-id="433ae-109">Themes</span></span>](themes.md)

<span data-ttu-id="433ae-110">증거 집합에서 데이터를 분석 하려면 다음을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="433ae-110">To analyze data in an evidence set:</span></span>

1. <span data-ttu-id="433ae-111">조사에 대 한 분석 설정을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="433ae-111">Configure the analytics settings for your investigation.</span></span> <span data-ttu-id="433ae-112">자세한 내용은 [Configure search and analytics settings](configure-search-analytics-settings.md)을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="433ae-112">For more information, see [Configure search and analytics settings](configure-search-analytics-settings.md).</span></span>

2. <span data-ttu-id="433ae-113">증거 집합을 엽니다.</span><span class="sxs-lookup"><span data-stu-id="433ae-113">Open the evidence set.</span></span>

3. <span data-ttu-id="433ae-114">**증거 관리**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="433ae-114">Click **Manage evidence**.</span></span>

4. <span data-ttu-id="433ae-115">**분석**에서 **분석**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="433ae-115">Under **Analytics**, click **Analyze**.</span></span>

<span data-ttu-id="433ae-116">조사에서 **작업** 탭의 분석 진행률을 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="433ae-116">You can check the progress of analysis on the **Jobs** tab in your investigation.</span></span> <span data-ttu-id="433ae-117">트리거된 작업 유형은 **analytics를 실행**하는 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="433ae-117">The job type that's triggered is named **Running analytics**.</span></span>

 <span data-ttu-id="433ae-118">분석이 완료 되 면 오른쪽 패널에 있는 검토 중인 문서와 정확히 일치 하는 중복 항목 또는 거의 중복 항목 목록을 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="433ae-118">After analysis is completed, you can see a list of exact duplicates or near-duplicates of the document that you're reviewing located in the panel on the right.</span></span> <span data-ttu-id="433ae-119">보고 있는 문서의 모든 중복 항목을 선택 하려면이 패널을 사용 하 여 작업을 쉽게 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="433ae-119">To select all duplicates of the document you're viewing, you can easily do so using this panel.</span></span> <span data-ttu-id="433ae-120">이 패널의 다른 기능에 대 한 자세한 내용은 [Review data in 증거](review-data-in-evidence.md)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="433ae-120">To learn more about other features on this panel, see [Review data in evidence](review-data-in-evidence.md).</span></span> 

<span data-ttu-id="433ae-121">테마와 같은 분석 출력을 사용 하 여 증명 정보 내에서 추가 쿼리를 실행할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="433ae-121">You can also run additional queries within your evidence using the outputs of the analysis such as themes.</span></span> <span data-ttu-id="433ae-122">자세한 내용은 [데이터를 증거에 쿼리](evidence-query.md)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="433ae-122">For more information, see [Query the data in evidence](evidence-query.md).</span></span>

## <a name="analytics-report"></a><span data-ttu-id="433ae-123">분석 보고서</span><span class="sxs-lookup"><span data-stu-id="433ae-123">Analytics report</span></span>

<span data-ttu-id="433ae-124">증명 정보에 대 한 분석 보고서를 보려면:</span><span class="sxs-lookup"><span data-stu-id="433ae-124">To view an analytics report for your evidence:</span></span>

1. <span data-ttu-id="433ae-125">증거 집합을 엽니다.</span><span class="sxs-lookup"><span data-stu-id="433ae-125">Open the evidence set.</span></span>

2. <span data-ttu-id="433ae-126">**증거 관리**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="433ae-126">Click **Manage evidence**.</span></span>

3. <span data-ttu-id="433ae-127">**분석**에서 **보고서 보기**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="433ae-127">Under **Analytics**, click **View report**.</span></span>

<span data-ttu-id="433ae-128">보고서에는 분석을 통해 다음과 같은 4 가지 구성 요소가 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="433ae-128">The report has four components from analysis:</span></span>

- <span data-ttu-id="433ae-129">**분석 결과** -증명 정보 집합에 있는 원시 전자 메일, 첨부 파일 및 문서 수입니다.</span><span class="sxs-lookup"><span data-stu-id="433ae-129">**Breakdown** - The number of raw emails, attachments, and documents found in the evidence set.</span></span>

- <span data-ttu-id="433ae-130">**전자 메일** -inclusives, 포괄 minuses, 포괄 복사본 또는 위의 값이 없는 eamil 메시지의 수입니다.</span><span class="sxs-lookup"><span data-stu-id="433ae-130">**Emails** - The number of eamil messages that are inclusives, inclusive minuses, inclusive copies, or none of the above.</span></span>
   - <span data-ttu-id="433ae-131">Inclusives: 이전 기록을 모두 포함 하며 검토가 필요한 전자 메일 스레드의 마지막 메시지입니다.</span><span class="sxs-lookup"><span data-stu-id="433ae-131">Inclusives: The last message in the email thread that contains all previous history and requires review.</span></span>
   - <span data-ttu-id="433ae-132">포함 minuses: 스레드가 검토 해야 하는 다른 첨부 파일이 하나 이상 포함 된 메시지입니다.</span><span class="sxs-lookup"><span data-stu-id="433ae-132">Inclusive minuses: The message in the thread that contains one or more different attachments that requires review.</span></span>
   - <span data-ttu-id="433ae-133">포함 복사본: 다른 포함 또는 포함 마이너스 메시지 (제목 및 본문)의 복사본 인 메시지입니다.</span><span class="sxs-lookup"><span data-stu-id="433ae-133">Inclusive copies: The message that is a copy of another inclusive or inclusive minus message (subject and body).</span></span>

- <span data-ttu-id="433ae-134">**첨부 파일** -동일한 증거 내에 있는 다른 전자 메일 첨부 파일의 고유 또는 중복 되는 전자 메일 첨부 파일의 수입니다.</span><span class="sxs-lookup"><span data-stu-id="433ae-134">**Attachments** - The number of email attachments that are unique or duplicates of a different email attachment within the same evidence same.</span></span>

- <span data-ttu-id="433ae-135">**문서 (전자 메일 첨부 파일 제외)** -검토 해야 하는 고유 문서 수 (예: 거의 중복 된 집합의 가장 대표적인 문서 또는 다른 문서의 정확한 중복)입니다.</span><span class="sxs-lookup"><span data-stu-id="433ae-135">**Documents (excluding email attachments)** - The number of unique documents that require review, for example, the most representative document of the near-duplicate set or an exact duplicate of another document).</span></span>