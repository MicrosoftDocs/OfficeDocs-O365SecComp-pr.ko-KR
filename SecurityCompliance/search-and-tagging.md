---
title: 검색 및 태그 지정
ms.author: chrfox
author: chrfox
manager: laurawi
ms.date: 6/13/2018
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 22f5adad-1bc0-460d-94a9-8732929f5b99
description: 고급 ediscovery에서 검색 및 태그 지정 모듈을 사용 하면 검색, 미리 보기, 및 사례에 문서를 구성 하 고 수 있습니다. 현재이 모듈 베타 버전에서입니다.
ms.openlocfilehash: fde887e496e9a40aa88d841053a0c66e48f04200
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22533578"
---
# <a name="search-and-tagging"></a><span data-ttu-id="a1a58-104">검색 및 태그 지정</span><span class="sxs-lookup"><span data-stu-id="a1a58-104">Search and Tagging</span></span>

<span data-ttu-id="a1a58-p102">고급 ediscovery에서 검색 및 태그 지정 모듈을 사용 하면 검색, 미리 보기, 및 사례에 문서를 구성 하 고 수 있습니다. 현재이 모듈 베타 버전에서입니다.</span><span class="sxs-lookup"><span data-stu-id="a1a58-p102">In Advanced eDiscovery, the Search and Tagging module enables you to search, preview, and organize the documents in your case. Currently, this module is in beta.</span></span>

> [!NOTE]
> <span data-ttu-id="a1a58-p103">고급 eDiscovery 조직에 대 한 고급 준수 추가 기능 또는 e 5 구독은 Office 365 E3 필요합니다. 해당 요금제에 가입한 상태 고급 eDiscovery 시도 하려는 하지 경우에 [Office 365 Enterprise e 5의 평가판 등록](https://go.microsoft.com/fwlink/p/?LinkID=698279)할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a1a58-p103">Advanced eDiscovery requires an Office 365 E3 with the Advanced Compliance add-on or an E5 subscription for your organization. If you don't have that plan and want to try Advanced eDiscovery, you can [sign up for a trial of Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span></span> 
  
## <a name="search-the-documents-in-your-case"></a><span data-ttu-id="a1a58-109">사례에는 문서를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="a1a58-109">Search the documents in your case</span></span>

<span data-ttu-id="a1a58-p104">고급 eDiscovery의 문서를 처리 한 되 고 분석 모듈 또는 관련성 모듈을 필요에 따라 실행 검색을 사용할 수 있는 태그 지정 하는 경우에는 문서를 통해 검색 하 고 구성 하 고, 대/소문자 관련 태그를 사용 하 고 있습니다. 제공 된 조건 카드를 사용 하 여 쿼리를 정의 하거나 키워드에 KQL와 같은 쿼리 언어를 통해 카드 조건문 수 있습니다. AND, OR, NOT, 예: 일반적인 KQL 구문을 NEAR(n)는 지원 되는,으로 후행 다중 문자 와일드 카드 (\*) 하 고 있습니다. 이러한 속성은 쿼리 언어 속성 이름에 지원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a1a58-p104">Once you have processed documents in Advanced eDiscovery and optionally run the Analyze module or the Relevance module, you can use Search and Tagging to search through the documents in the case and organize them using case-specific tags. You can define your queries using the provided condition cards, or through a KQL-like query language in the Keywords condition card. Common KQL syntax, such as AND, OR, NOT, and NEAR(n) are supported, as well as trailing multi-character wildcard (\*). These properties are supported in the query language property name:</span></span>

- <span data-ttu-id="a1a58-114">caselabel: 만든/적용 된 태그에서 검색 하 고 태그 지정이 있는 경우</span><span class="sxs-lookup"><span data-stu-id="a1a58-114">caselabel: tags created/applied in Search and Tagging for this case</span></span> 
- <span data-ttu-id="a1a58-115">custodians: custodians 제한 사항에 따라 달라 집니다 경우-할당</span><span class="sxs-lookup"><span data-stu-id="a1a58-115">custodians: custodians assigned in the case - subject to limitations</span></span>
- <span data-ttu-id="a1a58-116">날짜: 보낸 전자 메일에 대 한 날짜, 수정한 문서에 대 한 날짜</span><span class="sxs-lookup"><span data-stu-id="a1a58-116">date: sent date for email, modified date for documents</span></span>
- <span data-ttu-id="a1a58-117">fileid: 대/소문자 내에서 파일 ID</span><span class="sxs-lookup"><span data-stu-id="a1a58-117">fileid: file ID within the case</span></span>
- <span data-ttu-id="a1a58-118">파일 형식: 기본 파일 확장명</span><span class="sxs-lookup"><span data-stu-id="a1a58-118">filetype: native file extension</span></span>
- <span data-ttu-id="a1a58-119">fileclass: 전자 메일, 문서 또는 첨부 파일</span><span class="sxs-lookup"><span data-stu-id="a1a58-119">fileclass: email, document, or attachment</span></span>
- <span data-ttu-id="a1a58-120">senderauthor: 만든이 문서에 대 한 전자 메일에 대 한 보낸사람</span><span class="sxs-lookup"><span data-stu-id="a1a58-120">senderauthor: sender for emails, author for documents</span></span>
- <span data-ttu-id="a1a58-121">크기: KB에서 파일의 크기 조정</span><span class="sxs-lookup"><span data-stu-id="a1a58-121">size: size of the file in KB</span></span>
- <span data-ttu-id="a1a58-122">게시가: 전자 메일, 문서에 대 한 제목에 대 한 제목</span><span class="sxs-lookup"><span data-stu-id="a1a58-122">subjecttitle: subject for emails, title for documents</span></span>
- <span data-ttu-id="a1a58-123">숨은 참조</span><span class="sxs-lookup"><span data-stu-id="a1a58-123">bcc</span></span>
- <span data-ttu-id="a1a58-124">참조</span><span class="sxs-lookup"><span data-stu-id="a1a58-124">cc</span></span>
- <span data-ttu-id="a1a58-125">참가자: 누락 된 링크를 포함 하 여 전자 메일 스레드에서 모든 참가자의 주소를 전자 메일로 보내기</span><span class="sxs-lookup"><span data-stu-id="a1a58-125">participants: Email addresses of all participants in an email thread, including for missing links</span></span>
- <span data-ttu-id="a1a58-126">수신: 받은 날짜</span><span class="sxs-lookup"><span data-stu-id="a1a58-126">received: received date</span></span>
- <span data-ttu-id="a1a58-127">받는 사람: 전자 메일을 받는 사람 이름 또는 주소 (, 참조, 숨은 참조)</span><span class="sxs-lookup"><span data-stu-id="a1a58-127">recipients: email recipient names or addresses (to, cc, bcc)</span></span>
- <span data-ttu-id="a1a58-128">보낸 사람</span><span class="sxs-lookup"><span data-stu-id="a1a58-128">sender</span></span>
- <span data-ttu-id="a1a58-129">lastmodifieddate: 마지막으로 수정한 날짜의 문서</span><span class="sxs-lookup"><span data-stu-id="a1a58-129">lastmodifieddate: last modified date of a document</span></span>
- <span data-ttu-id="a1a58-130">전송: 보낸 전자 메일의 날짜</span><span class="sxs-lookup"><span data-stu-id="a1a58-130">sent: sent date of an email</span></span>
- <span data-ttu-id="a1a58-131">작업</span><span class="sxs-lookup"><span data-stu-id="a1a58-131">to</span></span>
- <span data-ttu-id="a1a58-132">만든이: 만든이의 전자 메일</span><span class="sxs-lookup"><span data-stu-id="a1a58-132">author: author of an email</span></span>
- <span data-ttu-id="a1a58-133">제목: 문서 제목</span><span class="sxs-lookup"><span data-stu-id="a1a58-133">title: title of a document</span></span>
- <span data-ttu-id="a1a58-134">dominanttheme: 항목의 기준 테마\*</span><span class="sxs-lookup"><span data-stu-id="a1a58-134">dominanttheme: dominant theme of an item\*</span></span>
- <span data-ttu-id="a1a58-135">themeslist: 항목 연관 된 테마\*</span><span class="sxs-lookup"><span data-stu-id="a1a58-135">themeslist: themes that are associated with an item\*</span></span>
- <span data-ttu-id="a1a58-136">readpercentile_ [issuenum]: [issuenum] 문제에 대 한 항목의 백분위 수 읽기\*\*</span><span class="sxs-lookup"><span data-stu-id="a1a58-136">readpercentile_[issuenum]: read percentile of an item for issue [issuenum]\*\*</span></span>
- <span data-ttu-id="a1a58-137">relevancescore_ [issuenum]: [issuenum] 문제에 대 한 항목의 관련성 점수\*\*</span><span class="sxs-lookup"><span data-stu-id="a1a58-137">relevancescore_[issuenum]: relevance score of an item for issue [issuenum]\*\*</span></span>
- <span data-ttu-id="a1a58-138">relevancetag_ [issuenum]: 관련성, [issuenum]에 대 한 자체의 태그에 대 한 항목 수동으로 표시 된 경우\*\*</span><span class="sxs-lookup"><span data-stu-id="a1a58-138">relevancetag_[issuenum]: if an item has been manually tagged for relevance, its tag for [issuenum]\*\*</span></span>

<span data-ttu-id="a1a58-139">\*테마 모듈이 실행 된 경우에 사용할 수 \* \* 관련성 모듈이 실행 된 경우에 사용할 수</span><span class="sxs-lookup"><span data-stu-id="a1a58-139">\* Only available if the Themes module has been run \*\* Only available if the Relevance module has been run</span></span>
  
## <a name="see-also"></a><span data-ttu-id="a1a58-140">참고 항목</span><span class="sxs-lookup"><span data-stu-id="a1a58-140">See also</span></span>

[<span data-ttu-id="a1a58-141">Office 365 Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="a1a58-141">Office 365 Advanced eDiscovery</span></span>](office-365-advanced-ediscovery.md)
  
[<span data-ttu-id="a1a58-142">관련성에 이해 평가</span><span class="sxs-lookup"><span data-stu-id="a1a58-142">Understanding Assessment in Relevance</span></span>](assessment-in-relevance-in-advanced-ediscovery.md)
  
[<span data-ttu-id="a1a58-143">태그 지정 및 평가</span><span class="sxs-lookup"><span data-stu-id="a1a58-143">Tagging and Assessment</span></span>](tagging-and-assessment-in-advanced-ediscovery.md)
  
[<span data-ttu-id="a1a58-144">태그 지정 및 관련성 교육</span><span class="sxs-lookup"><span data-stu-id="a1a58-144">Tagging and Relevance training</span></span>](tagging-and-relevance-training-in-advanced-ediscovery.md)
  
[<span data-ttu-id="a1a58-145">관련성 분석 추적</span><span class="sxs-lookup"><span data-stu-id="a1a58-145">Tracking Relevance analysis</span></span>](track-relevance-analysis-in-advanced-ediscovery.md)
  
[<span data-ttu-id="a1a58-146">결과에 따라 결정</span><span class="sxs-lookup"><span data-stu-id="a1a58-146">Deciding based on the results</span></span>](decision-based-on-the-results-in-advanced-ediscovery.md)
  
[<span data-ttu-id="a1a58-147">관련성 분석 테스트</span><span class="sxs-lookup"><span data-stu-id="a1a58-147">Testing Relevance analysis</span></span>](test-relevance-analysis-in-advanced-ediscovery.md)

