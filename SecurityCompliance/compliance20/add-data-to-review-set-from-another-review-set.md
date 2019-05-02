---
title: 한 검토 집합의 데이터를 다른 검토 집합에 추가
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
ms.openlocfilehash: 025fd90373313f762ce1d1dab8d48286e32e3cbb
ms.sourcegitcommit: 4ce350f8f3eb597587945a8ac9b33e9793440c64
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/01/2019
ms.locfileid: "33527246"
---
# <a name="add-data-to-a-review-set-from-another-review-set"></a><span data-ttu-id="5308d-102">다른 검토 집합의 검토 집합에 데이터 추가</span><span class="sxs-lookup"><span data-stu-id="5308d-102">Add data to a review set from another review set</span></span>

<span data-ttu-id="5308d-103">어떤 경우에는 한 검토 집합에서 문서 일부를 carve 다른 검토 집합에서 개별적으로 사용 해야 할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5308d-103">In some cases, it may be necessary to carve out a portion of documents from one review set and work with them individually in another review set.</span></span>  <span data-ttu-id="5308d-104">이 기능은 검토 집합에 콘텐츠를 culled 데이터 하위 집합에 대 한 분석을 실행 하려는 경우 특히 유용 합니다.</span><span class="sxs-lookup"><span data-stu-id="5308d-104">This is especially useful if you've culled content in a review set and want to run analytics on the subset of data.</span></span>

<span data-ttu-id="5308d-105">다음 워크플로를 사용 하 여 검토 집합 간에 콘텐츠를 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5308d-105">Use the following workflow to add content from one review set to another.</span></span>

## <a name="before-you-begin"></a><span data-ttu-id="5308d-106">시작하기 전에</span><span class="sxs-lookup"><span data-stu-id="5308d-106">Before you begin</span></span>

<span data-ttu-id="5308d-107">시작 하기 전에 데이터를 추가할 새 검토 집합을 만들어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="5308d-107">Before you start, you'll need to create a new review set to add the data to.</span></span>  <span data-ttu-id="5308d-108">사례에 대 한 **검토 집합** 탭에 새 검토 집합을 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5308d-108">A new review set can be added on the **Review sets** tab of the case.</span></span> <span data-ttu-id="5308d-109">자세한 내용은 [검토 집합 관리](managing-review-sets.md)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="5308d-109">For more information, see [Manage review sets](managing-review-sets.md).</span></span>

## <a name="step-1-identify-content-to-add-to-another-review-set"></a><span data-ttu-id="5308d-110">1 단계: 다른 검토 집합에 추가할 콘텐츠 식별</span><span class="sxs-lookup"><span data-stu-id="5308d-110">Step 1: Identify content to add to another review set</span></span>

<span data-ttu-id="5308d-111">문서 눈금이 나 검색 결과의 모든 항목을 선택 하 여 검토 집합에 콘텐츠를 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5308d-111">You can add content to a review set by selecting emails and documents in the document grid or all items in a search result.</span></span>  <span data-ttu-id="5308d-112">선택한 항목을 추가 하려면 항목을 선택 하 고 **동작**을 클릭 한 다음 **다른 검토 집합에 추가**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="5308d-112">If choosing to add selected items, select the items, click **Action**, and then click **Add to another review set**.</span></span>

![다른 검토 집합에 추가](../media/64f2a4d4-eba3-4ab3-a3ba-d519feea3142.png)

## <a name="step-2-specify-options-for-adding-to-another-review-set"></a><span data-ttu-id="5308d-114">2 단계: 다른 검토 집합에 추가 하기 위한 옵션 지정</span><span class="sxs-lookup"><span data-stu-id="5308d-114">Step 2: Specify options for adding to another review set</span></span>

<span data-ttu-id="5308d-115">**다른 검토 집합** 플라이 아웃 페이지에서 항목을 추가 하려는 검토 집합을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="5308d-115">In the **Add to another review set** flyout page, choose the review set you want to add the items to.</span></span> <span data-ttu-id="5308d-116">**모든 검색 결과** 또는 **선택한 항목**을 추가할지 여부를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="5308d-116">Choose whether to add **All search results** or **Selected items**.</span></span>  <span data-ttu-id="5308d-117">추가 정보는 항목의 모든 메타 데이터를 포함 하 고 마지막으로 문서 태그를 새 검토 집합에 포함시킬지 여부를 지정 하는 옵션을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="5308d-117">Additional information provides options to include all metadata from the items and finally whether or not the document tags should be included in the new review set.</span></span>  <span data-ttu-id="5308d-118">**확인** 을 클릭 하면 새 작업이 만들어져서 검토 집합에 콘텐츠가 추가 됩니다. **작업** 탭에서 해당 작업의 진행 상태를 모니터링할 수 있습니다. 자세한 내용은 [작업 관리](managing-jobs-ediscovery20.md)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="5308d-118">After clicking **Ok** a new job will be created to add the content to a review set; you can monitor the progress of that job on the **Job** tab. For more information, see [Manage jobs](managing-jobs-ediscovery20.md).</span></span>

![다른 검토 집합에 추가](../media/6440ee44-68fd-44d7-b43a-3a477345525c.png)
