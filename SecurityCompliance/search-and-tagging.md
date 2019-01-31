---
title: 검색 및 태그 지정
ms.author: chrfox
author: chrfox
manager: laurawi
ms.date: ''
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 22f5adad-1bc0-460d-94a9-8732929f5b99
description: 고급 ediscovery에서 검색 및 태그 지정 모듈을 사용 하면 검색, 미리 보기, 및 사례에 문서를 구성 하 고 수 있습니다. 현재이 모듈 베타 버전에서입니다.
ms.openlocfilehash: 013e559ca55e9a877dfb2f8747c4696f81e1e095
ms.sourcegitcommit: 25f1028643d8a20d17306e8b09cafea46eaf7a58
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/31/2019
ms.locfileid: "29666148"
---
# <a name="search-and-tagging"></a><span data-ttu-id="f3e61-104">검색 및 태그 지정</span><span class="sxs-lookup"><span data-stu-id="f3e61-104">Search and Tagging</span></span>

<span data-ttu-id="f3e61-p102">고급 ediscovery에서 검색 및 태그 지정 모듈을 사용 하면 검색, 미리 보기, 및 사례에 문서를 구성 하 고 수 있습니다. 현재이 모듈 베타 버전에서입니다. 검색 및 태그의 간단한 데모, [고급 eDiscovery 사용 하 여 데이터 관리](https://www.youtube.com/watch?v=VaPYL3DHP6I) 비디오를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="f3e61-p102">In Advanced eDiscovery, the Search and Tagging module enables you to search, preview, and organize the documents in your case. Currently, this module is in beta. For a brief demonstration of searching and tagging, see the [Manage your data with Advanced eDiscovery](https://www.youtube.com/watch?v=VaPYL3DHP6I) video.</span></span>

> [!NOTE]
> <span data-ttu-id="f3e61-p103">Advanced eDiscovery를 사용하려면 Office 365 E3의 고급 준수 추가 기능이나 조직을 위한 E5 구독이 필요합니다. 이 요금제가 없는 상태에서 Advanced eDiscovery를 사용하려는 경우에는 [Office 365 Enterprise E5 평가판을 등록](https://go.microsoft.com/fwlink/p/?LinkID=698279)할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f3e61-p103">Advanced eDiscovery requires an Office 365 E3 with the Advanced Compliance add-on or an E5 subscription for your organization. If you don't have that plan and want to try Advanced eDiscovery, you can [sign up for a trial of Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span></span> 
  
## <a name="search-the-documents-in-your-case"></a><span data-ttu-id="f3e61-110">사례에는 문서를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="f3e61-110">Search the documents in your case</span></span>

<span data-ttu-id="f3e61-p104">후 고급 eDiscovery 사례에서 문서를 처리 (분석 또는 관련성 모듈을 실행 하는 필요한 경우), 문서를 검색 하 고 다음 (레이블 라고도 함)는 대/소문자 관련 태그를 적용 하 여 구성 하는 검색 및 태그를 사용할 수 있습니다. 제공 된 조건 카드를 사용 하 여 검색 쿼리를 정의 하거나 키워드의 KQL와 같은 쿼리 언어를 사용 하 여 카드 조건문 수 있습니다. AND, OR, NOT, 예: 일반적인 KQL 구문을 NEAR(n)는 지원 되는,으로 후행 다중 문자 와일드 카드 (\*) 하 고 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f3e61-p104">After you have processed documents in an Advanced eDiscovery case (and optionally run the Analyze or Relevance module), you can use the Search and Tagging to search documents and then organize them by applying case-specific tags (also called labels). You can define a search query using the provided condition cards or by using a KQL-like query language in the Keywords condition card. Common KQL syntax, such as AND, OR, NOT, and NEAR(n) are supported, as well as trailing multi-character wildcard (\*).</span></span> 

<span data-ttu-id="f3e61-p105">다음 표에서 KQL 키워드 쿼리를 사용 하 여 검색할 수 있는 속성을 보여줍니다. 또는 (선택한 속성)에 대 한 조건 검색 쿼리를 추가 하려면 고급 ediscovery 검색 도구에 대 한 조건 카드를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f3e61-p105">The following table lists the properties that you can search for using a KQL keyword query. Alternatively, you can use a condition card for in the Advanced eDiscovery Search tool to add a condition (for selected properties) to a search query.</span></span>

|<span data-ttu-id="f3e61-116">**속성**</span><span class="sxs-lookup"><span data-stu-id="f3e61-116">**Property**</span></span>|<span data-ttu-id="f3e61-117">**설명**</span><span class="sxs-lookup"><span data-stu-id="f3e61-117">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="f3e61-118">**caselabel**</span><span class="sxs-lookup"><span data-stu-id="f3e61-118">**caselabel**</span></span> <br/> | <span data-ttu-id="f3e61-119">만든/때 적용 되는 문서 태그가 지정 된 태그의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f3e61-119">The name of the tag created/applied when a document is tagged.</span></span> <br/> |
|<span data-ttu-id="f3e61-120">**더불어**</span><span class="sxs-lookup"><span data-stu-id="f3e61-120">**custodian**</span></span> <br/> | <span data-ttu-id="f3e61-121">더불어 연관 된 문서입니다. 있으며 제한 사항이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f3e61-121">The custodian associated with a document; subject to limitations.</span></span> <br/> |
|<span data-ttu-id="f3e61-122">**날짜**</span><span class="sxs-lookup"><span data-stu-id="f3e61-122">**date**</span></span> <br/> | <span data-ttu-id="f3e61-123">보낸 전자 메일;에 대 한 날짜 사이트 문서에 대 한 수정 된 날짜입니다.</span><span class="sxs-lookup"><span data-stu-id="f3e61-123">Sent date for email; the modified date for site documents.</span></span> <br/> |
|<span data-ttu-id="f3e61-124">**fileid**</span><span class="sxs-lookup"><span data-stu-id="f3e61-124">**fileid**</span></span> <br/> | <span data-ttu-id="f3e61-125">대/소문자 내에서 파일 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="f3e61-125">The File ID within the case.</span></span> <br/> |
|<span data-ttu-id="f3e61-126">**파일 형식**</span><span class="sxs-lookup"><span data-stu-id="f3e61-126">**filetype**</span></span> <br/> | <span data-ttu-id="f3e61-127">기본 파일 확장명입니다.</span><span class="sxs-lookup"><span data-stu-id="f3e61-127">The native file extension.</span></span> <br/> |
|<span data-ttu-id="f3e61-128">**fileclass**</span><span class="sxs-lookup"><span data-stu-id="f3e61-128">**fileclass**</span></span> <br/> | <span data-ttu-id="f3e61-129">전자 메일, 문서 또는 첨부 파일입니다.</span><span class="sxs-lookup"><span data-stu-id="f3e61-129">Email, document, or attachment.</span></span> <br/> |
|<span data-ttu-id="f3e61-130">**senderauthor**</span><span class="sxs-lookup"><span data-stu-id="f3e61-130">**senderauthor**</span></span> <br/> | <span data-ttu-id="f3e61-131">전자 메일;에 대 한 보낸사람 사이트 문서에 대 한 만든이입니다.</span><span class="sxs-lookup"><span data-stu-id="f3e61-131">The sender for email; the author for site documents.</span></span> <br/> |
|<span data-ttu-id="f3e61-132">**크기**</span><span class="sxs-lookup"><span data-stu-id="f3e61-132">**size**</span></span> <br/> | <span data-ttu-id="f3e61-133">KB에 있는 파일의 크기입니다.</span><span class="sxs-lookup"><span data-stu-id="f3e61-133">The size of the file in KB.</span></span> <br/> |
|<span data-ttu-id="f3e61-134">**게시가**</span><span class="sxs-lookup"><span data-stu-id="f3e61-134">**subjecttitle**</span></span> <br/> | <span data-ttu-id="f3e61-135">전자 메일;에 대 한 제목 사이트 문서에 대 한 제목입니다.</span><span class="sxs-lookup"><span data-stu-id="f3e61-135">The subject for email; the title for site documents.</span></span> <br/> |
|<span data-ttu-id="f3e61-136">**숨은 참조**</span><span class="sxs-lookup"><span data-stu-id="f3e61-136">**bcc**</span></span> <br/> | <span data-ttu-id="f3e61-137">전자 메일의 숨은 참조 필드입니다.</span><span class="sxs-lookup"><span data-stu-id="f3e61-137">The Bcc field of an email.</span></span> <br/> |
|<span data-ttu-id="f3e61-138">**참조**</span><span class="sxs-lookup"><span data-stu-id="f3e61-138">**cc**</span></span> <br/> | <span data-ttu-id="f3e61-139">전자 메일의 참조 필드입니다.</span><span class="sxs-lookup"><span data-stu-id="f3e61-139">The Cc field of an email.</span></span> <br/> |
|<span data-ttu-id="f3e61-140">**참가자**</span><span class="sxs-lookup"><span data-stu-id="f3e61-140">**participants**</span></span> <br/> | <span data-ttu-id="f3e61-141">누락 된 링크를 포함 하 여 전자 메일 스레드의 모든 참가자의 전자 메일 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="f3e61-141">The email address of all participants in an email thread, including for missing links.</span></span> <br/> |
|<span data-ttu-id="f3e61-142">**수신**</span><span class="sxs-lookup"><span data-stu-id="f3e61-142">**received**</span></span> <br/> | <span data-ttu-id="f3e61-143">전자 메일을 받은 날짜입니다.</span><span class="sxs-lookup"><span data-stu-id="f3e61-143">The date an email was received.</span></span> <br/> |
|<span data-ttu-id="f3e61-144">**받는 사람**</span><span class="sxs-lookup"><span data-stu-id="f3e61-144">**recipients**</span></span> <br/> | <span data-ttu-id="f3e61-145">전자 메일의 받는 사람에 포함 된 받는 사람, 사람, 참조 또는 숨은 참조 필드입니다.</span><span class="sxs-lookup"><span data-stu-id="f3e61-145">Recipients of an email, included on the To, Cc, or Bcc fields.</span></span> <br/> |
|<span data-ttu-id="f3e61-146">**보낸 사람**</span><span class="sxs-lookup"><span data-stu-id="f3e61-146">**sender**</span></span> <br/> | <span data-ttu-id="f3e61-147">전자 메일의 보낸사람입니다.</span><span class="sxs-lookup"><span data-stu-id="f3e61-147">The sender of an email.</span></span> <br/> |
|<span data-ttu-id="f3e61-148">**lastmodifieddate**</span><span class="sxs-lookup"><span data-stu-id="f3e61-148">**lastmodifieddate**</span></span> <br/> | <span data-ttu-id="f3e61-149">마지막 수정 날짜의 사이트 문서입니다.</span><span class="sxs-lookup"><span data-stu-id="f3e61-149">The last modified date of a site document.</span></span> <br/> |
|<span data-ttu-id="f3e61-150">**전송**</span><span class="sxs-lookup"><span data-stu-id="f3e61-150">**sent**</span></span> <br/> | <span data-ttu-id="f3e61-151">전자 메일의 보낸된 날짜입니다.</span><span class="sxs-lookup"><span data-stu-id="f3e61-151">The sent date of an email.</span></span> <br/> |
|<span data-ttu-id="f3e61-152">**받는 사람**</span><span class="sxs-lookup"><span data-stu-id="f3e61-152">**to**</span></span> <br/> | <span data-ttu-id="f3e61-153">전자 메일의 받는 사람 필드에 나열 된 받는 사람입니다.</span><span class="sxs-lookup"><span data-stu-id="f3e61-153">The recipient listed in the To field of an email.</span></span> <br/> |
|<span data-ttu-id="f3e61-154">**작성자**</span><span class="sxs-lookup"><span data-stu-id="f3e61-154">**author**</span></span> <br/> | <span data-ttu-id="f3e61-155">사이트 문서 작성자입니다.</span><span class="sxs-lookup"><span data-stu-id="f3e61-155">The author of a site document.</span></span> <br/> |
|<span data-ttu-id="f3e61-156">**제목**</span><span class="sxs-lookup"><span data-stu-id="f3e61-156">**title**</span></span> <br/> | <span data-ttu-id="f3e61-157">사이트 문서의 제목입니다.</span><span class="sxs-lookup"><span data-stu-id="f3e61-157">The title of a site document.</span></span> <br/> |
|<span data-ttu-id="f3e61-158">**dominanttheme**\*</span><span class="sxs-lookup"><span data-stu-id="f3e61-158">**dominanttheme**\*</span></span> <br/> | <span data-ttu-id="f3e61-159">항목의 기준 테마입니다.</span><span class="sxs-lookup"><span data-stu-id="f3e61-159">The dominant theme of an item.</span></span> <br/> |
|<span data-ttu-id="f3e61-160">**themeslist**\*</span><span class="sxs-lookup"><span data-stu-id="f3e61-160">**themeslist**\*</span></span> <br/> | <span data-ttu-id="f3e61-161">항목에 연관 된 테마입니다.</span><span class="sxs-lookup"><span data-stu-id="f3e61-161">Themes that are associated with an item.</span></span> <br/> |
|<span data-ttu-id="f3e61-162">**readpercentile_ [issuenum]**\*\*</span><span class="sxs-lookup"><span data-stu-id="f3e61-162">**readpercentile_[issuenum]**\*\*</span></span> <br/> | <span data-ttu-id="f3e61-163">[Issuenum]에 정의 된 문제에 대 한 항목의 읽기 백분위 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f3e61-163">The read percentile of an item, for the issue defined by [issuenum].</span></span> <br/> |
|<span data-ttu-id="f3e61-164">**relevancescore_ [issuenum]**\*\*</span><span class="sxs-lookup"><span data-stu-id="f3e61-164">**relevancescore_[issuenum]**\*\*</span></span> <br/> | <span data-ttu-id="f3e61-165">[Issuenum]에 정의 된 문제에 대 한 항목의 관련성 점수입니다.</span><span class="sxs-lookup"><span data-stu-id="f3e61-165">The relevance score of an item, for the issue defined by [issuenum].</span></span> <br/> |
|<span data-ttu-id="f3e61-166">**relevancetag_ [tagname]**\*\*</span><span class="sxs-lookup"><span data-stu-id="f3e61-166">**relevancetag_[tagname]**\*\*</span></span> <br/> | <span data-ttu-id="f3e61-167">항목이 있으면 된 수동으로 관련성, [tagname]으로 정의 하는 태그에 대 한 태그가 지정 된 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f3e61-167">If an item has been manually tagged for relevance, the tag defined by  [tagname].</span></span> <br/> |
|||

<span data-ttu-id="f3e61-168">\*테마 모듈이 실행 된 경우에 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f3e61-168">\* Only available if the Themes module has been run.</span></span>

<span data-ttu-id="f3e61-169">\*\*관련성 모듈이 실행 된 경우에 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f3e61-169">\*\* Only available if the Relevance module has been run.</span></span>

<span data-ttu-id="f3e61-p106">또는 고급 eDiscovery 검색 도구 (선택한 속성)에 대 한 조건 검색 쿼리를 추가 하려면 조건 카드를 사용할 수 있습니다. 다음 스크린샷에서 쿼리를 추가할 수 있는 조건입니다. **그룹** 열 속성은 전자 메일, 사이트 문서 또는 ( *공통*값으로 표시) 모두에 적용 되는지 여부를 나타냅니다. 또한이 열 관련성 모듈을 실행 하 고 나면 사용할 수 있는 검색 가능한 속성을 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="f3e61-p106">Alternatively, you can use a condition card in the Advanced eDiscovery Search tool to add a condition (for selected properties) to a search query. The following screenshot shows the conditions that can be added to a query. The **Group** column indicates whether the property applies to email, site documents, or both (indicated by the value *Common*). This column also identifies the searchable properties that are available after you run the Relevance module.</span></span>

![고급 eDiscovery 검색 도구에서 검색 조건](media/AeDSearchConditions.png)

<span data-ttu-id="f3e61-175">검색 가능한 속성에 대 한 자세한 내용은 [쿼리 키워드 및 검색 조건을](keyword-queries-and-search-conditions.md)참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="f3e61-175">For more information about searchable properties, see [Keyword queries and search conditions](keyword-queries-and-search-conditions.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="f3e61-176">참고 항목</span><span class="sxs-lookup"><span data-stu-id="f3e61-176">See also</span></span>

[<span data-ttu-id="f3e61-177">Office 365 Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="f3e61-177">Office 365 Advanced eDiscovery</span></span>](office-365-advanced-ediscovery.md)
  
[<span data-ttu-id="f3e61-178">관련성에 이해 평가</span><span class="sxs-lookup"><span data-stu-id="f3e61-178">Understanding Assessment in Relevance</span></span>](assessment-in-relevance-in-advanced-ediscovery.md)
  
[<span data-ttu-id="f3e61-179">태그 지정 및 평가</span><span class="sxs-lookup"><span data-stu-id="f3e61-179">Tagging and Assessment</span></span>](tagging-and-assessment-in-advanced-ediscovery.md)
  
[<span data-ttu-id="f3e61-180">태그 지정 및 관련성 교육</span><span class="sxs-lookup"><span data-stu-id="f3e61-180">Tagging and Relevance training</span></span>](tagging-and-relevance-training-in-advanced-ediscovery.md)
  
[<span data-ttu-id="f3e61-181">관련성 분석 추적</span><span class="sxs-lookup"><span data-stu-id="f3e61-181">Tracking Relevance analysis</span></span>](track-relevance-analysis-in-advanced-ediscovery.md)
  
[<span data-ttu-id="f3e61-182">결과에 따라 결정</span><span class="sxs-lookup"><span data-stu-id="f3e61-182">Deciding based on the results</span></span>](decision-based-on-the-results-in-advanced-ediscovery.md)
  
[<span data-ttu-id="f3e61-183">관련성 분석 테스트</span><span class="sxs-lookup"><span data-stu-id="f3e61-183">Testing Relevance analysis</span></span>](test-relevance-analysis-in-advanced-ediscovery.md)

