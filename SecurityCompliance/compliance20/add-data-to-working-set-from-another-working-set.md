---
title: 한 작업 집합의 데이터를 다른 작업 집합에 추가
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
ms.openlocfilehash: e9e34d112cb84c27fec35e752eb2bfcbfe3136a3
ms.sourcegitcommit: f0e3c9de0b545081a4d264f74559b941f6c71410
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/22/2019
ms.locfileid: "31958239"
---
# <a name="add-data-to-a-working-set-from-another-working-set"></a><span data-ttu-id="248e0-102">다른 작업 집합의 작업 집합에 데이터 추가</span><span class="sxs-lookup"><span data-stu-id="248e0-102">Add data to a working set from another working set</span></span>
<span data-ttu-id="248e0-103">일부 경우에는 한 작업 집합에서 문서 일부를 carve 다른 작업 집합에서 개별적으로 사용 해야 할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="248e0-103">In some cases, it may be necessary to carve out a portion of documents from one working set and work with them individually in another working set.</span></span>  <span data-ttu-id="248e0-104">이 기능은 작업 집합에 콘텐츠를 culled 데이터 하위 집합에 대 한 분석을 실행 하려는 경우 특히 유용 합니다.</span><span class="sxs-lookup"><span data-stu-id="248e0-104">This is especially useful if you've culled content in a working set and want to run analytics on the subset of data.</span></span>

<span data-ttu-id="248e0-105">다음 워크플로를 사용 하 여 작업 집합 간에 콘텐츠를 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="248e0-105">Use the following workflow to add content from one working set to another.</span></span>

## <a name="before-you-start"></a><span data-ttu-id="248e0-106">시작하기 전에</span><span class="sxs-lookup"><span data-stu-id="248e0-106">Before you start</span></span>
<span data-ttu-id="248e0-107">시작 하기 전에 새 작업 집합을 만들어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="248e0-107">Before you start, you'll need to create a new working set.</span></span>  <span data-ttu-id="248e0-108">*작업 집합* 탭에서 [더 자세히 알아보려면](https://docs.microsoft.com/en-us/office365/securitycompliance/compliance20/managing-working-sets)새 작업 집합을 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="248e0-108">A new working set can be added through the *Working sets* tab [Learn more](https://docs.microsoft.com/en-us/office365/securitycompliance/compliance20/managing-working-sets).</span></span>

## <a name="step-1-identify-content-to-add-to-another-working-set"></a><span data-ttu-id="248e0-109">1 단계: 다른 작업 집합에 추가할 콘텐츠 식별</span><span class="sxs-lookup"><span data-stu-id="248e0-109">Step 1: Identify content to add to another working set</span></span>
<span data-ttu-id="248e0-110">문서 눈금이 나 검색 결과의 모든 항목을 선택 하 여 작업 집합에 콘텐츠를 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="248e0-110">You can add content to a working set by selecting emails and documents in the document grid or all items in a search result.</span></span>  <span data-ttu-id="248e0-111">선택한 항목을 추가 하려면 항목을 선택 하 고 *작업* 드롭다운을 클릭 한 다음 *다른 작업 집합에 추가*합니다.</span><span class="sxs-lookup"><span data-stu-id="248e0-111">If choosing to add selected items, select the items and click the *Action* drop down then *Add to another working set*.</span></span>

![다른 작업 집합에 추가](../media/64f2a4d4-eba3-4ab3-a3ba-d519feea3142.png)

## <a name="step-2-specify-options-for-adding-to-another-workings-set"></a><span data-ttu-id="248e0-113">2 단계: 다른 작업 집합에 추가 하기 위한 옵션 지정</span><span class="sxs-lookup"><span data-stu-id="248e0-113">Step 2: Specify options for adding to another workings set</span></span>
<span data-ttu-id="248e0-114">*다른 작업 집합에 추가 옵션* 플라이 아웃에서 먼저 항목을 추가할 작업 집합을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="248e0-114">In the *Add to another working set options* flyout, first choose the working set you want to add the items to.</span></span>  <span data-ttu-id="248e0-115">모든 검색 결과 또는 선택한 항목을 추가할지 여부를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="248e0-115">Choose whether to add All search results or Selected items.</span></span>  <span data-ttu-id="248e0-116">추가 정보는 항목의 모든 메타 데이터를 포함 하 고 마지막으로 문서 태그를 새 작업 집합에 포함시킬지 여부를 지정 하는 옵션을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="248e0-116">Additional information provides options to include all metadata from the items and finally whether or not the document tags should be included in the new working set.</span></span>  <span data-ttu-id="248e0-117">*확인* 을 클릭 하 여 작업 집합에 콘텐츠를 추가 하는 새 작업을 만들고 작업 탭에서 해당 작업의 진행 상태를 모니터링할 수 [](https://docs.microsoft.com/en-us/office365/securitycompliance/compliance20/managing-jobs-ediscovery20) 있습니다. ![다른 작업 집합에 추가](../media/6440ee44-68fd-44d7-b43a-3a477345525c.png)</span><span class="sxs-lookup"><span data-stu-id="248e0-117">After clicking *OK* a new job will be created to add the content to a working set, you can monitor the progress of that job in the [Jobs](https://docs.microsoft.com/en-us/office365/securitycompliance/compliance20/managing-jobs-ediscovery20) tab. ![Add to another working set](../media/6440ee44-68fd-44d7-b43a-3a477345525c.png)</span></span>
