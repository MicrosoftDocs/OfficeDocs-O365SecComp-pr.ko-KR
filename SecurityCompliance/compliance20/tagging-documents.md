---
title: 작업 집합에서 문서 태그 지정
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
ms.openlocfilehash: 1183264f64a74e50f750ee13618f7532ffe04eb7
ms.sourcegitcommit: 6aa82374eef09d2c1921f93bda3eabeeb28aadeb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/06/2019
ms.locfileid: "30455160"
---
# <a name="tag-documents-in-a-working-set"></a><span data-ttu-id="ec4a1-102">작업 집합에서 문서 태그 지정</span><span class="sxs-lookup"><span data-stu-id="ec4a1-102">Tag documents in a working set</span></span>

<span data-ttu-id="ec4a1-103">작업 집합에 콘텐츠를 구성 하는 것은 eDiscovery 프로세스에서 다양 한 워크플로를 완료 하는 것이 중요 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec4a1-103">Organizing content in a working set is important to complete various workflows in the eDiscovery process.</span></span> <span data-ttu-id="ec4a1-104">성능 저하를 줄여주는 방법에는 다음이 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="ec4a1-104">This includes:</span></span>

-  <span data-ttu-id="ec4a1-105">불필요 한 콘텐츠를 Culling.</span><span class="sxs-lookup"><span data-stu-id="ec4a1-105">Culling unnecessary content.</span></span>

- <span data-ttu-id="ec4a1-106">관련 콘텐츠 식별</span><span class="sxs-lookup"><span data-stu-id="ec4a1-106">Identifying relevant content.</span></span>
 
-  <span data-ttu-id="ec4a1-107">전문가 또는 변호사가 검토 해야 하는 콘텐츠 식별</span><span class="sxs-lookup"><span data-stu-id="ec4a1-107">Identifying content that must be reviewed by an expert or an attorney.</span></span>

<span data-ttu-id="ec4a1-108">전문가, 변호사 또는 다른 사용자가 작업 집합의 콘텐츠를 검토 하는 경우 태그를 사용 하 여 콘텐츠와 관련 된 해당 의견을 캡처할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ec4a1-108">When experts, attorneys, or other users review content in a working set, their opinions related to the content can be captured by using tags.</span></span> <span data-ttu-id="ec4a1-109">예를 들어 불필요 한 콘텐츠를 cull 하는 경우 사용자가 "응답성"과 같은 태그를 사용 하 여 문서에 태그를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ec4a1-109">For example, if the intent is to cull unnecessary content, a user can tag documents with a tag such as “non-responsive”.</span></span> <span data-ttu-id="ec4a1-110">콘텐츠를 검토 하 고 태그를 지정 하 고 나면 "응답성이 아님"으로 태그가 지정 된 모든 콘텐츠를 제외 하는 작업 집합 검색을 만들어 eDiscovery 워크플로의 다음 단계에서 해당 콘텐츠를 제거할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ec4a1-110">After content has been reviewed and tagged, a working set search can be created to exclude any content tagged as “non-responsive”, which eliminates this content from the next steps in the eDiscovery workflow.</span></span> <span data-ttu-id="ec4a1-111">태그를 원하는 검토 워크플로를 지원할 수 있도록 모든 경우에 태그 패널을 사용자 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ec4a1-111">The tag panel can be customized for every case so that the tags can support the intended review workflow.</span></span>

## <a name="tag-types"></a><span data-ttu-id="ec4a1-112">태그 유형</span><span class="sxs-lookup"><span data-stu-id="ec4a1-112">Tag types</span></span>

<span data-ttu-id="ec4a1-113">Advanced eDiscovery (Preview)에서는 두 가지 유형의 태그를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec4a1-113">Advanced eDiscovery (Preview) provides two types of tags:</span></span>

- <span data-ttu-id="ec4a1-114">**단일 choice 태그** -사용자가 그룹 내에서 단일 태그를 선택 하는 것을 제한 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec4a1-114">**Single choice tags** - Restricts users to select a single tag within a group.</span></span> <span data-ttu-id="ec4a1-115">이는 "응답성" 및 "응답 없음"과 같은 충돌 하는 태그를 선택 하지 않도록 하는 데 유용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ec4a1-115">This can be useful to ensure users don’t select conflicting tags such as “responsive” and “non-responsive”.</span></span> 

- <span data-ttu-id="ec4a1-116">**여러 선택 태그** -사용자가 그룹 내에서 여러 태그를 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ec4a1-116">**Multiple choice tags** - Allow users to select multiple tags within a group.</span></span>

## <a name="tag-structure"></a><span data-ttu-id="ec4a1-117">태그 구조</span><span class="sxs-lookup"><span data-stu-id="ec4a1-117">Tag structure</span></span>

<span data-ttu-id="ec4a1-118">태그 형식 외에 태그 패널에서 태그를 구성 하는 방법의 구조를 사용 하 여 문서에 태그를 지정 하는 방법을 보다 직관적으로 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ec4a1-118">In addition to the tag types, the structure of how tags are organization in the tag panel can be used to make tagging documents more intuitive.</span></span> <span data-ttu-id="ec4a1-119">태그는 섹션 별로 그룹화 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ec4a1-119">Tags are grouped by sections.</span></span> <span data-ttu-id="ec4a1-120">작업 집합 검색은 태그별 및 태그별 섹션으로 검색 하는 기능을 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec4a1-120">Working set search supports the ability to search by tag and by tag section.</span></span> <span data-ttu-id="ec4a1-121">즉, 섹션의 태그로 태그가 지정 된 문서를 검색 하기 위해 작업 집합 검색을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ec4a1-121">This means you can create a working set search to retrieve documents tagged with any tag in a section.</span></span>

![태그 패널의 태그 섹션](../media/Tagtypes.png)

<span data-ttu-id="ec4a1-123">태그를 섹션 내에 중첩 시켜 더 체계적으로 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ec4a1-123">Tags can be further organized by nesting them within a section.</span></span> <span data-ttu-id="ec4a1-124">예를 들어 권한 있는 콘텐츠를 식별 하 고 태그를 지정 하는 경우에는 중첩을 사용 하 여 사용자가 문서에 "특권" 태그를 지정 하 고 적절 한 중첩 태그를 확인 하 여 권한 유형을 선택할 수 있음을 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ec4a1-124">For example, if the intent is to identify and tag privileged content, nesting can be used to make it clear that a user can tag a document as “Privileged” and select the type of privilege by checking the appropriate nested tag.</span></span>

![tag 섹션 내의 중첩 태그](../media/Nestingtags.png)

## <a name="applying-tags"></a><span data-ttu-id="ec4a1-126">태그 적용</span><span class="sxs-lookup"><span data-stu-id="ec4a1-126">Applying tags</span></span>

<span data-ttu-id="ec4a1-127">여러 가지 방법으로 콘텐츠에 태그를 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ec4a1-127">There are several ways to apply a tag to content.</span></span>

### <a name="tagging-a-single-document"></a><span data-ttu-id="ec4a1-128">단일 문서 태그 지정</span><span class="sxs-lookup"><span data-stu-id="ec4a1-128">Tagging a single document</span></span>

<span data-ttu-id="ec4a1-129">작업 집합의 문서를 볼 때 **코딩 패널**을 클릭 하 여 검토에 사용할 수 있는 태그를 표시할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ec4a1-129">When viewing a document in a working set, you can display the tags that a review can use by clicking **Coding panel**.</span></span>

![태그 패널을 클릭 하 여 태그 패널 표시](../media/Singledoctag.png)

<span data-ttu-id="ec4a1-131">이렇게 하면 뷰어에 표시 된 문서에 태그를 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ec4a1-131">This will enable you to apply tags to the document displayed in the viewer.</span></span>

### <a name="bulk-tagging"></a><span data-ttu-id="ec4a1-132">대량 태그 지정</span><span class="sxs-lookup"><span data-stu-id="ec4a1-132">Bulk tagging</span></span>

<span data-ttu-id="ec4a1-133">대량 태그 지정은 결과 표에서 여러 파일을 선택한 다음 단일 문서 태그 지정과 유사 하 게 **코딩 패널** 의 태그를 사용 하 여 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ec4a1-133">Bulk tagging can be done by selecting multiple files in the results grid and then using the tags in the **Coding panel** similar to tagging single documents.</span></span> <span data-ttu-id="ec4a1-134">대량 태깅은 태그를 두 번 선택 하 여 수행할 수 있습니다. 첫 번째 클릭은 태그를 적용 하 고 두 번째 선택 옵션을 선택 하면 선택한 모든 파일에 대해 태그의 선택이 취소 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ec4a1-134">Bulk un-tagging can be done by selecting tags twice; the first click will apply the tag, and the second selection will ensure that tag is cleared for all selected files.</span></span>

![자동으로 생성 되는 휴대폰 설명 스크린샷](../media/Bulktag.png)

> [!NOTE]
> <span data-ttu-id="ec4a1-136">대량 태그를 지정 하면 태그 패널에는 패널의 각 태그에 대해 태그 있는 파일 수가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ec4a1-136">When bulk tagging, the tagging panel will display a count of files that are tagged for each tag in the panel.</span></span>

### <a name="tagging-in-other-review-panels"></a><span data-ttu-id="ec4a1-137">다른 검토 패널의 태그 지정</span><span class="sxs-lookup"><span data-stu-id="ec4a1-137">Tagging in other review panels</span></span>

<span data-ttu-id="ec4a1-138">문서를 검토할 때 다른 검토 패널을 사용 하 여 결과 표에서 문서의 기타 특성을 검토할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ec4a1-138">When reviewing documents, you can use the other review panels to review other characteristics of documents in the results grid.</span></span> <span data-ttu-id="ec4a1-139">여기에는 기타 관련 문서, 전자 메일 스레드, 중복 항목 및 해시 중복을 검토 하는 작업이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ec4a1-139">This includes reviewing other related documents, email threads, near duplicates, and hash duplicates.</span></span> <span data-ttu-id="ec4a1-140">예를 들어 **문서 제품군** 검토 패널을 사용 하 여 관련 문서를 검토할 때 관련 문서를 대량으로 태그 지정 하 여 검토 시간을 크게 줄일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ec4a1-140">For example, when your reviewing related documents (by using the **Document family** review panel), you can significantly reduce review time by bulk tagging related documents.</span></span> <span data-ttu-id="ec4a1-141">예를 들어 전자 메일 메시지에 첨부 파일이 여러 개 있고 전체 패밀리가 일관성 있게 태그 처리 되도록 하려는 경우</span><span class="sxs-lookup"><span data-stu-id="ec4a1-141">For example, if an email message has several attachments and you want to ensure that the entire family is tagged consistently.</span></span>

<span data-ttu-id="ec4a1-142">예를 들어 **문서 패밀리** 검토 패널을 사용할 때 **코딩 패널** 을 표시 하는 방법은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="ec4a1-142">For example, here's how to display the **Coding panel** when using the **Document family** review panel:</span></span>

1. <span data-ttu-id="ec4a1-143">선택한 문서에 대해 검토 패널 (예: **문서 패밀리** 검토 패널에 관련 콘텐츠 목록 표시)을 연 상태에서 현재 검토 패널 위쪽에 있는 **코드 문서** 를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec4a1-143">With the review panel open for a selected document (for example, displaying the list of related content in the **Document family** review panel, click **Code documents** at the top of the current review panel.</span></span>

   <span data-ttu-id="ec4a1-144">코딩 패널이 팝업 창으로 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ec4a1-144">The Coding panel is displayed is a pop-up window.</span></span>

2. <span data-ttu-id="ec4a1-145">선택한 문서를 적용할 태그를 하나 이상 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec4a1-145">Choose one or more tags to apply the selected document.</span></span> 

3. <span data-ttu-id="ec4a1-146">모든 문서에 태그를 적용 하려면 **문서 모음** 패널에서 모든 문서를 선택 하 고 **코드 문서**를 클릭 한 다음 전체 문서 패밀리에 적용할 태그를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec4a1-146">To tag all documents, select all documents in the **Document family** panel, click **Code documents**, and then choose the tags to apply to the entire family of documents.</span></span>

![자동으로 생성 되는 소셜 미디어 post 설명 스크린샷](../media/Relatedtag.png)
