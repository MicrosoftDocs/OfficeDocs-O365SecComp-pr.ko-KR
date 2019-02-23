---
title: 검색 및 태그 지정
ms.author: chrfox
author: chrfox
manager: laurawi
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 22f5adad-1bc0-460d-94a9-8732929f5b99
description: 고급 eDiscovery에서 검색 및 태그 지정 모듈을 사용 하 여 사용자의 경우 문서를 검색, 미리 보기 및 구성할 수 있습니다. 현재이 모듈은 베타 버전입니다.
ms.openlocfilehash: 58913a01f30b4169470592f5fc271e3ce785ac5d
ms.sourcegitcommit: a80bd8626720fabdf592b84e4424cd3a83d08280
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30222967"
---
# <a name="search-and-tagging"></a><span data-ttu-id="0d0a6-104">검색 및 태그 지정</span><span class="sxs-lookup"><span data-stu-id="0d0a6-104">Search and Tagging</span></span>

<span data-ttu-id="0d0a6-p102">고급 eDiscovery에서 검색 및 태그 지정 모듈을 사용 하 여 사용자의 경우 문서를 검색, 미리 보기 및 구성할 수 있습니다. 현재이 모듈은 베타 버전입니다. 검색 및 태그 지정에 대 한 간단한 데모를 보려면 [고급 eDiscovery로 데이터 관리](https://www.youtube.com/watch?v=VaPYL3DHP6I) 비디오를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="0d0a6-p102">In Advanced eDiscovery, the Search and Tagging module enables you to search, preview, and organize the documents in your case. Currently, this module is in beta. For a brief demonstration of searching and tagging, see the [Manage your data with Advanced eDiscovery](https://www.youtube.com/watch?v=VaPYL3DHP6I) video.</span></span>

> [!NOTE]
> <span data-ttu-id="0d0a6-p103">Advanced eDiscovery를 사용하려면 Office 365 E3의 고급 준수 추가 기능이나 조직을 위한 E5 구독이 필요합니다. 이 요금제가 없는 상태에서 Advanced eDiscovery를 사용하려는 경우에는 [Office 365 Enterprise E5 평가판을 등록](https://go.microsoft.com/fwlink/p/?LinkID=698279)할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0d0a6-p103">Advanced eDiscovery requires an Office 365 E3 with the Advanced Compliance add-on or an E5 subscription for your organization. If you don't have that plan and want to try Advanced eDiscovery, you can [sign up for a trial of Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span></span> 
  
## <a name="search-the-documents-in-your-case"></a><span data-ttu-id="0d0a6-110">사례에서 문서 검색</span><span class="sxs-lookup"><span data-stu-id="0d0a6-110">Search the documents in your case</span></span>

<span data-ttu-id="0d0a6-p104">고급 eDiscovery 사례에서 문서를 처리 하 고 (필요한 경우 분석 또는 관련성 모듈을 실행) 검색 및 태그 지정 기능을 사용 하 여 문서를 검색 한 다음 대/소문자 별 태그 (레이블 라고도 함)를 적용 하 여이를 구성할 수 있습니다. 제공 된 조건 카드를 사용 하거나 키워드 조건 카드에서 KQL와 같은 형식의 쿼리 언어를 사용 하 여 검색 쿼리를 정의할 수 있습니다. and, OR, NOT 및 NEAR (n)과 같은 일반 KQL 구문은 지원 되 고 후행 여러 문자 와일드 카드 (\*)와 유사 합니다.</span><span class="sxs-lookup"><span data-stu-id="0d0a6-p104">After you have processed documents in an Advanced eDiscovery case (and optionally run the Analyze or Relevance module), you can use the Search and Tagging to search documents and then organize them by applying case-specific tags (also called labels). You can define a search query using the provided condition cards or by using a KQL-like query language in the Keywords condition card. Common KQL syntax, such as AND, OR, NOT, and NEAR(n) are supported, as well as trailing multi-character wildcard (\*).</span></span> 

<span data-ttu-id="0d0a6-p105">다음 표에는 KQL keyword 쿼리를 사용 하 여 검색할 수 있는 속성이 나와 있습니다. 또는 고급 eDiscovery 검색 도구에서 조건 카드를 사용 하 여 검색 쿼리에 조건 (선택한 속성)을 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0d0a6-p105">The following table lists the properties that you can search for using a KQL keyword query. Alternatively, you can use a condition card for in the Advanced eDiscovery Search tool to add a condition (for selected properties) to a search query.</span></span>

|<span data-ttu-id="0d0a6-116">**속성**</span><span class="sxs-lookup"><span data-stu-id="0d0a6-116">**Property**</span></span>|<span data-ttu-id="0d0a6-117">**설명**</span><span class="sxs-lookup"><span data-stu-id="0d0a6-117">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="0d0a6-118">**caselabel**</span><span class="sxs-lookup"><span data-stu-id="0d0a6-118">**caselabel**</span></span> <br/> | <span data-ttu-id="0d0a6-119">문서에 태그를 지정 하는 경우 생성/적용 되는 태그의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0d0a6-119">The name of the tag created/applied when a document is tagged.</span></span> <br/> |
|<span data-ttu-id="0d0a6-120">**custodian**</span><span class="sxs-lookup"><span data-stu-id="0d0a6-120">**custodian**</span></span> <br/> | <span data-ttu-id="0d0a6-121">문서와 연결 된 custodian입니다. 제한 사항에 따라 달라 집니다.</span><span class="sxs-lookup"><span data-stu-id="0d0a6-121">The custodian associated with a document; subject to limitations.</span></span> <br/> |
|<span data-ttu-id="0d0a6-122">**종료일**</span><span class="sxs-lookup"><span data-stu-id="0d0a6-122">**date**</span></span> <br/> | <span data-ttu-id="0d0a6-123">전자 메일을 보낸 날짜 사이트 문서를 수정한 날짜입니다.</span><span class="sxs-lookup"><span data-stu-id="0d0a6-123">Sent date for email; the modified date for site documents.</span></span> <br/> |
|<span data-ttu-id="0d0a6-124">**열려**</span><span class="sxs-lookup"><span data-stu-id="0d0a6-124">**fileid**</span></span> <br/> | <span data-ttu-id="0d0a6-125">사례 내의 파일 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="0d0a6-125">The File ID within the case.</span></span> <br/> |
|<span data-ttu-id="0d0a6-126">**filetype**</span><span class="sxs-lookup"><span data-stu-id="0d0a6-126">**filetype**</span></span> <br/> | <span data-ttu-id="0d0a6-127">네이티브 파일 확장명입니다.</span><span class="sxs-lookup"><span data-stu-id="0d0a6-127">The native file extension.</span></span> <br/> |
|<span data-ttu-id="0d0a6-128">**fileclass**</span><span class="sxs-lookup"><span data-stu-id="0d0a6-128">**fileclass**</span></span> <br/> | <span data-ttu-id="0d0a6-129">전자 메일, 문서 또는 첨부 파일</span><span class="sxs-lookup"><span data-stu-id="0d0a6-129">Email, document, or attachment.</span></span> <br/> |
|<span data-ttu-id="0d0a6-130">**senderauthor**</span><span class="sxs-lookup"><span data-stu-id="0d0a6-130">**senderauthor**</span></span> <br/> | <span data-ttu-id="0d0a6-131">전자 메일 보낸 사람 사이트 문서에 대 한 작성자입니다.</span><span class="sxs-lookup"><span data-stu-id="0d0a6-131">The sender for email; the author for site documents.</span></span> <br/> |
|<span data-ttu-id="0d0a6-132">**크기**</span><span class="sxs-lookup"><span data-stu-id="0d0a6-132">**size**</span></span> <br/> | <span data-ttu-id="0d0a6-133">파일 크기 (mb)입니다.</span><span class="sxs-lookup"><span data-stu-id="0d0a6-133">The size of the file in KB.</span></span> <br/> |
|<span data-ttu-id="0d0a6-134">**호칭 제목**</span><span class="sxs-lookup"><span data-stu-id="0d0a6-134">**subjecttitle**</span></span> <br/> | <span data-ttu-id="0d0a6-135">전자 메일의 제목입니다. 사이트 문서의 제목입니다.</span><span class="sxs-lookup"><span data-stu-id="0d0a6-135">The subject for email; the title for site documents.</span></span> <br/> |
|<span data-ttu-id="0d0a6-136">**숨은 참조**</span><span class="sxs-lookup"><span data-stu-id="0d0a6-136">**bcc**</span></span> <br/> | <span data-ttu-id="0d0a6-137">전자 메일의 숨은 참조 필드입니다.</span><span class="sxs-lookup"><span data-stu-id="0d0a6-137">The Bcc field of an email.</span></span> <br/> |
|<span data-ttu-id="0d0a6-138">**참조**</span><span class="sxs-lookup"><span data-stu-id="0d0a6-138">**cc**</span></span> <br/> | <span data-ttu-id="0d0a6-139">전자 메일의 참조 필드입니다.</span><span class="sxs-lookup"><span data-stu-id="0d0a6-139">The Cc field of an email.</span></span> <br/> |
|<span data-ttu-id="0d0a6-140">**할당**</span><span class="sxs-lookup"><span data-stu-id="0d0a6-140">**participants**</span></span> <br/> | <span data-ttu-id="0d0a6-141">누락 된 링크를 포함 하 여 전자 메일 스레드에 있는 모든 참가자의 전자 메일 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="0d0a6-141">The email address of all participants in an email thread, including for missing links.</span></span> <br/> |
|<span data-ttu-id="0d0a6-142">**received**</span><span class="sxs-lookup"><span data-stu-id="0d0a6-142">**received**</span></span> <br/> | <span data-ttu-id="0d0a6-143">전자 메일을 받은 날짜입니다.</span><span class="sxs-lookup"><span data-stu-id="0d0a6-143">The date an email was received.</span></span> <br/> |
|<span data-ttu-id="0d0a6-144">**받는 사람**</span><span class="sxs-lookup"><span data-stu-id="0d0a6-144">**recipients**</span></span> <br/> | <span data-ttu-id="0d0a6-145">전자 메일의 받는 사람, 참조 또는 숨은 참조 필드에 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0d0a6-145">Recipients of an email, included on the To, Cc, or Bcc fields.</span></span> <br/> |
|<span data-ttu-id="0d0a6-146">**보낸 사람**</span><span class="sxs-lookup"><span data-stu-id="0d0a6-146">**sender**</span></span> <br/> | <span data-ttu-id="0d0a6-147">전자 메일을 보낸 사람입니다.</span><span class="sxs-lookup"><span data-stu-id="0d0a6-147">The sender of an email.</span></span> <br/> |
|<span data-ttu-id="0d0a6-148">**lastmodifieddate**</span><span class="sxs-lookup"><span data-stu-id="0d0a6-148">**lastmodifieddate**</span></span> <br/> | <span data-ttu-id="0d0a6-149">사이트 문서를 마지막으로 수정한 날짜입니다.</span><span class="sxs-lookup"><span data-stu-id="0d0a6-149">The last modified date of a site document.</span></span> <br/> |
|<span data-ttu-id="0d0a6-150">**전송할**</span><span class="sxs-lookup"><span data-stu-id="0d0a6-150">**sent**</span></span> <br/> | <span data-ttu-id="0d0a6-151">전자 메일의 보낸 날짜입니다.</span><span class="sxs-lookup"><span data-stu-id="0d0a6-151">The sent date of an email.</span></span> <br/> |
|<span data-ttu-id="0d0a6-152">**받는 사람**</span><span class="sxs-lookup"><span data-stu-id="0d0a6-152">**to**</span></span> <br/> | <span data-ttu-id="0d0a6-153">전자 메일의 받는 사람 필드에 나열 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0d0a6-153">The recipient listed in the To field of an email.</span></span> <br/> |
|<span data-ttu-id="0d0a6-154">**제작할**</span><span class="sxs-lookup"><span data-stu-id="0d0a6-154">**author**</span></span> <br/> | <span data-ttu-id="0d0a6-155">사이트 문서의 만든이입니다.</span><span class="sxs-lookup"><span data-stu-id="0d0a6-155">The author of a site document.</span></span> <br/> |
|<span data-ttu-id="0d0a6-156">**직책**</span><span class="sxs-lookup"><span data-stu-id="0d0a6-156">**title**</span></span> <br/> | <span data-ttu-id="0d0a6-157">사이트 문서의 제목입니다.</span><span class="sxs-lookup"><span data-stu-id="0d0a6-157">The title of a site document.</span></span> <br/> |
|<span data-ttu-id="0d0a6-158">**dominanttheme**\*</span><span class="sxs-lookup"><span data-stu-id="0d0a6-158">**dominanttheme**\*</span></span> <br/> | <span data-ttu-id="0d0a6-159">항목의 기준 테마입니다.</span><span class="sxs-lookup"><span data-stu-id="0d0a6-159">The dominant theme of an item.</span></span> <br/> |
|<span data-ttu-id="0d0a6-160">**기타 eslist**\*</span><span class="sxs-lookup"><span data-stu-id="0d0a6-160">**themeslist**\*</span></span> <br/> | <span data-ttu-id="0d0a6-161">항목과 연결 된 테마입니다.</span><span class="sxs-lookup"><span data-stu-id="0d0a6-161">Themes that are associated with an item.</span></span> <br/> |
|<span data-ttu-id="0d0a6-162">**readpercentile_ [issuenum]**\*\*</span><span class="sxs-lookup"><span data-stu-id="0d0a6-162">**readpercentile_[issuenum]**\*\*</span></span> <br/> | <span data-ttu-id="0d0a6-163">[issuenum]로 정의 된 문제에 대해 항목의 읽기 백분위 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0d0a6-163">The read percentile of an item, for the issue defined by [issuenum].</span></span> <br/> |
|<span data-ttu-id="0d0a6-164">**relevancescore_ [issuenum]**\*\*</span><span class="sxs-lookup"><span data-stu-id="0d0a6-164">**relevancescore_[issuenum]**\*\*</span></span> <br/> | <span data-ttu-id="0d0a6-165">[issuenum]에 의해 정의 된 문제에 대 한 항목의 관련성 점수입니다.</span><span class="sxs-lookup"><span data-stu-id="0d0a6-165">The relevance score of an item, for the issue defined by [issuenum].</span></span> <br/> |
|<span data-ttu-id="0d0a6-166">**relevancetag_ [tagname]**\*\*</span><span class="sxs-lookup"><span data-stu-id="0d0a6-166">**relevancetag_[tagname]**\*\*</span></span> <br/> | <span data-ttu-id="0d0a6-167">항목에 관련성을 수동으로 태그가 지정 된 경우 [tagname]에 정의 된 태그입니다.</span><span class="sxs-lookup"><span data-stu-id="0d0a6-167">If an item has been manually tagged for relevance, the tag defined by  [tagname].</span></span> <br/> |
|||

<span data-ttu-id="0d0a6-168">\*Themes 모듈을 실행 한 경우에만 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0d0a6-168">\* Only available if the Themes module has been run.</span></span>

<span data-ttu-id="0d0a6-169">\*\*관련성 모듈이 실행 된 경우에만 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0d0a6-169">\*\* Only available if the Relevance module has been run.</span></span>

<span data-ttu-id="0d0a6-p106">또는 고급 eDiscovery 검색 도구에서 조건 카드를 사용 하 여 검색 쿼리에 조건 (선택한 속성)을 추가할 수 있습니다. 다음 스크린샷은 쿼리에 추가할 수 있는 조건을 보여 줍니다. **그룹** 열은 속성을 전자 메일, 사이트 문서 또는 둘 다에 적용할지를 나타냅니다 ( *공통*값으로 표시 됨). 또한이 열은 관련성 모듈을 실행 한 후에 사용할 수 있는 검색 가능한 속성을 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="0d0a6-p106">Alternatively, you can use a condition card in the Advanced eDiscovery Search tool to add a condition (for selected properties) to a search query. The following screenshot shows the conditions that can be added to a query. The **Group** column indicates whether the property applies to email, site documents, or both (indicated by the value *Common*). This column also identifies the searchable properties that are available after you run the Relevance module.</span></span>

![Advanced eDiscovery 검색 도구의 검색 조건](media/AeDSearchConditions.png)

<span data-ttu-id="0d0a6-175">검색 가능한 속성에 대 한 자세한 내용은 [키워드 쿼리 및 검색 조건을](keyword-queries-and-search-conditions.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="0d0a6-175">For more information about searchable properties, see [Keyword queries and search conditions](keyword-queries-and-search-conditions.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="0d0a6-176">참고 항목</span><span class="sxs-lookup"><span data-stu-id="0d0a6-176">See also</span></span>

[<span data-ttu-id="0d0a6-177">Office 365 Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="0d0a6-177">Office 365 Advanced eDiscovery</span></span>](office-365-advanced-ediscovery.md)
  
[<span data-ttu-id="0d0a6-178">관련성 평가 이해</span><span class="sxs-lookup"><span data-stu-id="0d0a6-178">Understanding Assessment in Relevance</span></span>](assessment-in-relevance-in-advanced-ediscovery.md)
  
[<span data-ttu-id="0d0a6-179">태그 지정 및 평가</span><span class="sxs-lookup"><span data-stu-id="0d0a6-179">Tagging and Assessment</span></span>](tagging-and-assessment-in-advanced-ediscovery.md)
  
[<span data-ttu-id="0d0a6-180">태그 지정 및 관련성 교육</span><span class="sxs-lookup"><span data-stu-id="0d0a6-180">Tagging and Relevance training</span></span>](tagging-and-relevance-training-in-advanced-ediscovery.md)
  
[<span data-ttu-id="0d0a6-181">관련성 분석 추적</span><span class="sxs-lookup"><span data-stu-id="0d0a6-181">Tracking Relevance analysis</span></span>](track-relevance-analysis-in-advanced-ediscovery.md)
  
[<span data-ttu-id="0d0a6-182">결과를 기준으로 결정</span><span class="sxs-lookup"><span data-stu-id="0d0a6-182">Deciding based on the results</span></span>](decision-based-on-the-results-in-advanced-ediscovery.md)
  
[<span data-ttu-id="0d0a6-183">관련성 분석 테스트</span><span class="sxs-lookup"><span data-stu-id="0d0a6-183">Testing Relevance analysis</span></span>](test-relevance-analysis-in-advanced-ediscovery.md)

