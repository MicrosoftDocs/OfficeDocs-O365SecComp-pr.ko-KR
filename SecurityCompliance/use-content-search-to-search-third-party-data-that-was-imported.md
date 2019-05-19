---
title: 콘텐츠 검색을 사용 하 여 Office 365로 가져온 타사 데이터 검색
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 10/27/2017
audience: Admin
ms.topic: conceptual
ms.service: O365-seccomp
ms.collection: M365-security-compliance
localization_priority: Normal
search.appverid: MOE150
ms.assetid: ec2677ff-c4d7-4363-a9e7-22c80e015688
description: 콘텐츠 검색 eDiscovery 도구를 사용 하 여 타사 데이터 원본에서 Office 365의 사서함으로 가져온 항목을 검색 합니다. 가져온 모든 항목을 검색 하는 쿼리를 만들거나 특정 타사 데이터 형식을 검색 하기 위한 쿼리를 만들 수 있습니다. 이 문서에서는 키워드 쿼리에서 Office 365로 가져올 수 있는 타사 데이터 형식을 검색 하는 데 사용할 수 있는 값을 보여 줍니다.
ms.openlocfilehash: 4a611ed04cc102aad4d978a379efbf46a0bd70e2
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/17/2019
ms.locfileid: "34156210"
---
# <a name="use-content-search-to-search-third-party-data-that-was-imported-to-office-365"></a><span data-ttu-id="b1644-105">콘텐츠 검색을 사용 하 여 Office 365로 가져온 타사 데이터 검색</span><span class="sxs-lookup"><span data-stu-id="b1644-105">Use Content Search to search third-party data that was imported to Office 365</span></span>

<span data-ttu-id="b1644-106">보안 & 준수 센터의 [콘텐츠 검색 eDiscovery 도구](content-search.md) 를 사용 하 여 타사 데이터 원본에서 Office 365의 사서함으로 가져온 항목을 검색할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b1644-106">You can use the [Content Search eDiscovery tool](content-search.md) in the Security & Compliance Center to search for items that were imported to mailboxes in Office 365 from a third-party data source.</span></span> <span data-ttu-id="b1644-107">가져온 모든 타사 데이터 항목을 검색 하는 쿼리를 만들 수도 있고 특정 타사 데이터 항목만 검색 하는 쿼리를 만들 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b1644-107">You can create a query to search all imported third-party data items or you can create a query to only search specific third-party data items.</span></span> <span data-ttu-id="b1644-108">또한 Office 365에서 타사 데이터를 보존 하기 위해 쿼리 기반 보존 정책 또는 쿼리 기반 eDiscovery 보존을 만들 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b1644-108">Additionally, you can also create a query-based Preservation Policy or a query-based eDiscovery hold to preserve third-party data in Office 365.</span></span> 
  
<span data-ttu-id="b1644-109">타사 데이터 및 Office 365로 가져올 수 있는 타사 데이터 형식 목록을 가져오는 방법에 대 한 자세한 내용은 [office 365에서 파트너와 협력 하](work-with-partner-to-archive-third-party-data.md)여 타사 데이터 보관을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="b1644-109">For more information about importing third-party data and a list of the third-party data types that can be imported to Office 365, see [Work with a partner to archive third-party data in Office 365](work-with-partner-to-archive-third-party-data.md).</span></span> 
  
## <a name="creating-a-query-to-search-all-third-party-data"></a><span data-ttu-id="b1644-110">모든 타사 데이터를 검색 하기 위한 쿼리 만들기</span><span class="sxs-lookup"><span data-stu-id="b1644-110">Creating a query to search all third-party data</span></span>

<span data-ttu-id="b1644-111">Office 365로 가져온 모든 타사 데이터 형식을 검색 하거나 보류 하려면 콘텐츠 검색의 키워드 상자에 `kind:externaldata` 메시지 속성-값 쌍을 사용 하거나 쿼리 기반 보존을 만들 때 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b1644-111">To search (or place on hold) any type of third-party data that you've imported to Office 365, you can you can use the  `kind:externaldata` message property-value pair in the keyword box for a Content Search or when creating a query-based hold.</span></span> <span data-ttu-id="b1644-112">예를 들어 모든 타사 데이터 원본에서 가져온 항목을 검색 하 고 가져온 항목의 Subject 속성에 "contoso" 라는 단어를 포함 하는 경우에는 다음 쿼리를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1644-112">For example, to search for items that were imported from any third-party data source and contain the word "contoso" in the Subject property of the imported item, you would use the following query:</span></span> 
  
```
kind:externaldata AND subject:contoso
```

<span data-ttu-id="b1644-113">이전 keyword 쿼리 예제에는 subject 속성이 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b1644-113">The previous keyword query example includes the subject property.</span></span> <span data-ttu-id="b1644-114">키워드 쿼리에 포함할 수 있는 타사 데이터 항목의 기타 속성 목록은 [Office 365에서 타사 데이터를 보관 하기 위한 파트너와 작업](work-with-partner-to-archive-third-party-data.md#more-information)의 "추가 정보" 섹션을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="b1644-114">For a list of other properties for third-party data items that can included in a keyword query, see the "More information" section in [Work with a partner to archive third-party data in Office 365](work-with-partner-to-archive-third-party-data.md#more-information).</span></span>
  
<span data-ttu-id="b1644-115">타사 데이터를 검색 하 고 유지 하기 위한 쿼리를 만들 때 조건을 사용 하 여 검색 결과의 범위를 좁힐 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b1644-115">When creating queries to search and hold third-party data, you can also use conditions to narrow the search results.</span></span> <span data-ttu-id="b1644-116">콘텐츠 검색 쿼리를 만드는 방법에 대 한 자세한 내용은 [키워드 쿼리 및 검색 조건을](keyword-queries-and-search-conditions.md)참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="b1644-116">For more information about creating Content Search queries, see [Keyword queries and search conditions for Content Search](keyword-queries-and-search-conditions.md).</span></span>
  
## <a name="creating-a-query-to-search-specific-types-of-third-party-data"></a><span data-ttu-id="b1644-117">특정 유형의 타사 데이터를 검색 하기 위한 쿼리 만들기</span><span class="sxs-lookup"><span data-stu-id="b1644-117">Creating a query to search specific types of third-party data</span></span>

<span data-ttu-id="b1644-118">모든 유형의 타사 데이터를 검색 하는 대신 콘텐츠 검색의 키워드 상자에 다음과 같은 메시지 속성 값 쌍을 사용 하 여 지정 된 타사 데이터를 검색 하는 쿼리를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b1644-118">Instead of searching all types of third-party data, you can create queries that only search for a specify type of third-party data by using the following message property-value pair in the keyword box for a Content Search:</span></span>
  
```
itemclass:ipm.externaldata.<third-party data type>* 
```

<span data-ttu-id="b1644-119">예를 들어 Subject 속성에서 "contoso" 라는 단어가 포함 된 Facebook 데이터만 검색 하려면 다음 쿼리를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1644-119">For example, to only search Facebook data that contains the word "contoso" in the Subject property, you would use the following query:</span></span>
  
```
itemclass:ipm.externaldata.Facebook* AND subject:contoso
```

<span data-ttu-id="b1644-120">다음 표에서는 검색할 수 있는 타사 데이터 형식 및 해당 유형의 타사 데이터를 특별히 검색 하기 위해 `itemclass:` message 속성에 사용할 값을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="b1644-120">The following table lists the third-party data types that you can search, and the value to use for the  `itemclass:` message property to specifically search for that type of third-party data.</span></span> <span data-ttu-id="b1644-121">쿼리 구문은 대/소문자를 구분 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b1644-121">Note that the query syntax isn't case sensitive.</span></span> 
  
|<span data-ttu-id="b1644-122">**타사 데이터 형식**</span><span class="sxs-lookup"><span data-stu-id="b1644-122">**Third-party data type**</span></span>|<span data-ttu-id="b1644-123">**`itemclass:` 속성 값**</span><span class="sxs-lookup"><span data-stu-id="b1644-123">**Value for  `itemclass:` property**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b1644-124">AIM</span><span class="sxs-lookup"><span data-stu-id="b1644-124">AIM</span></span>  <br/> | `ipm.externaldata.AIM*` <br/> |
|<span data-ttu-id="b1644-125">American Idol</span><span class="sxs-lookup"><span data-stu-id="b1644-125">American Idol</span></span>  <br/> | `ipm.externaldata.AmericanIdol*` <br/> |
|<span data-ttu-id="b1644-126">AOL with Pivot Client </span><span class="sxs-lookup"><span data-stu-id="b1644-126">AOL with Pivot Client</span></span>  <br/> | `ipm.externaldata.Pivot.IM` <br/> |
|<span data-ttu-id="b1644-127">Apple Juice</span><span class="sxs-lookup"><span data-stu-id="b1644-127">Apple Juice</span></span>  <br/> | `ipm.externaldata.AppleJuice*` <br/> |
|<span data-ttu-id="b1644-128">Ares</span><span class="sxs-lookup"><span data-stu-id="b1644-128">Ares</span></span>  <br/> | `ipm.externaldata.Ares*` <br/> |
|<span data-ttu-id="b1644-129">Axs Encrypted</span><span class="sxs-lookup"><span data-stu-id="b1644-129">Axs Encrypted</span></span>  <br/> | `ipm.externaldata.AxsEncrypted*` <br/> |
|<span data-ttu-id="b1644-130">Axs Exchange</span><span class="sxs-lookup"><span data-stu-id="b1644-130">Axs Exchange</span></span>  <br/> | `ipm.externaldata.AxsExchange*` <br/> |
|<span data-ttu-id="b1644-131">Axs Local Archive</span><span class="sxs-lookup"><span data-stu-id="b1644-131">Axs Local Archive</span></span>  <br/> | `ipm.externaldata.AxsLocalArchive*` <br/> |
|<span data-ttu-id="b1644-132">Axs 자리 표시자</span><span class="sxs-lookup"><span data-stu-id="b1644-132">Axs Placeholder</span></span>  <br/> | `ipm.externaldata.AxsPlaceHolder*` <br/> |
|<span data-ttu-id="b1644-133">Axs Signed</span><span class="sxs-lookup"><span data-stu-id="b1644-133">Axs Signed</span></span>  <br/> | `ipm.externaldata.AxsSigned*` <br/> |
|<span data-ttu-id="b1644-134">Bazaarvoice</span><span class="sxs-lookup"><span data-stu-id="b1644-134">Bazaarvoice</span></span>  <br/> | `ipm.externaldata.Bazaarvoice*` <br/> |
|<span data-ttu-id="b1644-135">Bearshare</span><span class="sxs-lookup"><span data-stu-id="b1644-135">Bearshare</span></span>  <br/> | `ipm.externaldata.Bearshare*` <br/> |
|<span data-ttu-id="b1644-136">BitTorrent</span><span class="sxs-lookup"><span data-stu-id="b1644-136">BitTorrent</span></span>  <br/> | `ipm.externaldata.BitTorrent*` <br/> |
|<span data-ttu-id="b1644-137">Blackberry</span><span class="sxs-lookup"><span data-stu-id="b1644-137">Blackberry</span></span>  <br/> | `ipm.externaldata.Blackberry*` <br/> |
|<span data-ttu-id="b1644-138">BlackBerry 통화 로그</span><span class="sxs-lookup"><span data-stu-id="b1644-138">BlackBerry Call Logs</span></span>  <br/> | `ipm.externaldata.BlackBerryCall*` <br/> |
|<span data-ttu-id="b1644-139">BlackBerry Messenger</span><span class="sxs-lookup"><span data-stu-id="b1644-139">BlackBerry Messenger</span></span>  <br/> | `ipm.externaldata.BlackBerryMessenger*` <br/> |
|<span data-ttu-id="b1644-140">BlackBerry PIN</span><span class="sxs-lookup"><span data-stu-id="b1644-140">BlackBerry PIN</span></span>  <br/> | `ipm.externaldata.BlackBerryPIN*` <br/> |
|<span data-ttu-id="b1644-141">BlackBerry SMS</span><span class="sxs-lookup"><span data-stu-id="b1644-141">BlackBerry SMS</span></span>  <br/> | `ipm.externaldata.BlackBerrySMS*` <br/> |
|<span data-ttu-id="b1644-142">Bloomberg</span><span class="sxs-lookup"><span data-stu-id="b1644-142">Bloomberg</span></span>  <br/> | `ipm.externaldata.Bloomberg*` <br/> |
|<span data-ttu-id="b1644-143">Bloomberg Mail</span><span class="sxs-lookup"><span data-stu-id="b1644-143">Bloomberg Mail</span></span>  <br/> | `ipm.externaldata.BloombergMail*` <br/> |
|<span data-ttu-id="b1644-144">Bloomberg 메시징</span><span class="sxs-lookup"><span data-stu-id="b1644-144">Bloomberg Messaging</span></span>  <br/> | `ipm.externaldata.BloombergMessaging*` <br/> |
|<span data-ttu-id="b1644-145">Box</span><span class="sxs-lookup"><span data-stu-id="b1644-145">Box</span></span>  <br/> | `ipm.externaldata.Box*` <br/> |
|<span data-ttu-id="b1644-146">Cisco IM &amp; 현재 상태 서버</span><span class="sxs-lookup"><span data-stu-id="b1644-146">Cisco IM &amp; Presence Server</span></span>  <br/> | `ipm.externaldata.Jabber.IM` <br/> |
|<span data-ttu-id="b1644-147">Cisco Jabber</span><span class="sxs-lookup"><span data-stu-id="b1644-147">Cisco Jabber</span></span>  <br/> | `ipm.externaldata.Jabber*` <br/> |
|<span data-ttu-id="b1644-148">CipherCloud for Salesforce Chatter</span><span class="sxs-lookup"><span data-stu-id="b1644-148">CipherCloud for Salesforce Chatter</span></span>  <br/> | `ipm.externaldata.Chatter.Post` <br/>  `ipm.externaldata.Chatter.Comment` <br/> |
|<span data-ttu-id="b1644-149">Direct Connect</span><span class="sxs-lookup"><span data-stu-id="b1644-149">Direct Connect</span></span>  <br/> | `ipm.externaldata.DirectConnect*` <br/> |
|<span data-ttu-id="b1644-150">Facebook</span><span class="sxs-lookup"><span data-stu-id="b1644-150">Facebook</span></span>  <br/> | `ipm.externaldata.Facebook*` <br/> |
|<span data-ttu-id="b1644-151">FastTrack</span><span class="sxs-lookup"><span data-stu-id="b1644-151">FastTrack</span></span>  <br/> | `ipm.externaldata.FastTrack*` <br/> |
|<span data-ttu-id="b1644-152">FXConnect</span><span class="sxs-lookup"><span data-stu-id="b1644-152">FXConnect</span></span>  <br/> | `ipm.externaldata.FXConnect.chat` <br/> |
|<span data-ttu-id="b1644-153">Flickr</span><span class="sxs-lookup"><span data-stu-id="b1644-153">Flickr</span></span>  <br/> | `ipm.externaldata.Flickr*` <br/> |
|<span data-ttu-id="b1644-154">Gnutella</span><span class="sxs-lookup"><span data-stu-id="b1644-154">Gnutella</span></span>  <br/> | `ipm.externaldata.Gnutella*` <br/> |
|<span data-ttu-id="b1644-155">Google +</span><span class="sxs-lookup"><span data-stu-id="b1644-155">Google+</span></span>  <br/> | `ipm.externaldata.GooglePlus*` <br/> |
|<span data-ttu-id="b1644-156">Google 대화</span><span class="sxs-lookup"><span data-stu-id="b1644-156">Google Talk</span></span>  <br/> | `ipm.externaldata.GoogleTalk*` <br/> |
|<span data-ttu-id="b1644-157">GoToMyPC</span><span class="sxs-lookup"><span data-stu-id="b1644-157">GoToMyPC</span></span>  <br/> | `ipm.externaldata.GoToMyPC*` <br/> |
|<span data-ttu-id="b1644-158">HipChat</span><span class="sxs-lookup"><span data-stu-id="b1644-158">HipChat</span></span>  <br/> | `ipm.externaldata.HipChat*` <br/> |
|<span data-ttu-id="b1644-159">Hopster</span><span class="sxs-lookup"><span data-stu-id="b1644-159">Hopster</span></span>  <br/> | `ipm.externaldata.Hopster*` <br/> |
|<span data-ttu-id="b1644-160">HubConnex</span><span class="sxs-lookup"><span data-stu-id="b1644-160">HubConnex</span></span>  <br/> | `ipm.externaldata.HubConnex*` <br/> |
|<span data-ttu-id="b1644-161">IBM 연결</span><span class="sxs-lookup"><span data-stu-id="b1644-161">IBM Connections</span></span>  <br/> | `ipm.externaldata.Connections*` <br/> |
|<span data-ttu-id="b1644-162">IBM SameTime</span><span class="sxs-lookup"><span data-stu-id="b1644-162">IBM SameTime</span></span>  <br/> | `ipm.externaldata.Sametime*` <br/> |
|<span data-ttu-id="b1644-163">얼음 채팅</span><span class="sxs-lookup"><span data-stu-id="b1644-163">ICE Chat</span></span>  <br/> | `ipm.externaldata.ICEChat.Chat` <br/> |
|<span data-ttu-id="b1644-164">Indii Messenger</span><span class="sxs-lookup"><span data-stu-id="b1644-164">Indii Messenger</span></span>  <br/> | `ipm.externaldata.Indii*` <br/> |
|<span data-ttu-id="b1644-165">명령이 있는 agram</span><span class="sxs-lookup"><span data-stu-id="b1644-165">Instagram</span></span>  <br/> | `ipm.externaldata.Instagram*` <br/> |
|<span data-ttu-id="b1644-166">Instant Bloomberg</span><span class="sxs-lookup"><span data-stu-id="b1644-166">Instant Bloomberg</span></span>  <br/> | `ipm.externaldata.InstantBloomberg*` <br/> |
|<span data-ttu-id="b1644-167">InvestEdge</span><span class="sxs-lookup"><span data-stu-id="b1644-167">InvestEdge</span></span>  <br/> | `ipm.externaldata.InvestEdge*` <br/> |
|<span data-ttu-id="b1644-168">IRC</span><span class="sxs-lookup"><span data-stu-id="b1644-168">IRC</span></span>  <br/> | `ipm.externaldata.IRC*` <br/> |
|<span data-ttu-id="b1644-169">Jive</span><span class="sxs-lookup"><span data-stu-id="b1644-169">Jive</span></span>  <br/> | `ipm.externaldata.Jive*` <br/> |
|<span data-ttu-id="b1644-170">JiveApiRetention</span><span class="sxs-lookup"><span data-stu-id="b1644-170">JiveApiRetention</span></span>  <br/> | `ipm.externaldata.JiveApiRetention*` <br/> |
|<span data-ttu-id="b1644-171">JXTA</span><span class="sxs-lookup"><span data-stu-id="b1644-171">JXTA</span></span>  <br/> | `ipm.externaldata.JXTA*` <br/> |
|<span data-ttu-id="b1644-172">LinkedIn</span><span class="sxs-lookup"><span data-stu-id="b1644-172">LinkedIn</span></span>  <br/> | `ipm.externaldata.LinkedIn*` <br/> |
|<span data-ttu-id="b1644-173">MFTP</span><span class="sxs-lookup"><span data-stu-id="b1644-173">MFTP</span></span>  <br/> | `ipm.externaldata.MFTP*` <br/> |
|<span data-ttu-id="b1644-174">Microsoft UC</span><span class="sxs-lookup"><span data-stu-id="b1644-174">Microsoft UC</span></span>  <br/> | `ipm.externaldata.MicrosoftUC*` <br/> |
|<span data-ttu-id="b1644-175">마인드 맞춤</span><span class="sxs-lookup"><span data-stu-id="b1644-175">Mind Align</span></span>  <br/> | `ipm.externaldata.MindAlign*` <br/> |
|<span data-ttu-id="b1644-176">Mobile Guard</span><span class="sxs-lookup"><span data-stu-id="b1644-176">Mobile Guard</span></span>  <br/> | `ipm.externaldata.MobileGuard*` <br/> |
|<span data-ttu-id="b1644-177">수신</span><span class="sxs-lookup"><span data-stu-id="b1644-177">MSN</span></span>  <br/> | `ipm.externaldata.MSN*` <br/> |
|<span data-ttu-id="b1644-178">MySpace</span><span class="sxs-lookup"><span data-stu-id="b1644-178">MySpace</span></span>  <br/> | `ipm.externaldata.MySpace*` <br/> |
|<span data-ttu-id="b1644-179">NEONetwork</span><span class="sxs-lookup"><span data-stu-id="b1644-179">NEONetwork</span></span>  <br/> | `ipm.externaldata.NEONetwork*` <br/> |
|<span data-ttu-id="b1644-180">OpenNap</span><span class="sxs-lookup"><span data-stu-id="b1644-180">OpenNap</span></span>  <br/> | `ipm.externaldata.OpenNap*` <br/> |
|<span data-ttu-id="b1644-181">유 이율</span><span class="sxs-lookup"><span data-stu-id="b1644-181">Pinterest</span></span>  <br/> | `ipm.externaldata.Pinterest*` <br/> |
|<span data-ttu-id="b1644-182">Pivot</span><span class="sxs-lookup"><span data-stu-id="b1644-182">Pivot</span></span>  <br/> | `ipm.externaldata.Pivot*` <br/> |
|<span data-ttu-id="b1644-183">QQ</span><span class="sxs-lookup"><span data-stu-id="b1644-183">QQ</span></span>  <br/> | `ipm.externaldata.QQ*` <br/> |
|<span data-ttu-id="b1644-184">Microsoft SharePoint</span><span class="sxs-lookup"><span data-stu-id="b1644-184">Microsoft SharePoint</span></span>  <br/> | `ipm.externaldata.SharePoint*` <br/> |
|<span data-ttu-id="b1644-185">Salesforce Chatter</span><span class="sxs-lookup"><span data-stu-id="b1644-185">Salesforce Chatter</span></span>  <br/> | `ipm.externaldata.Chatter*` <br/> |
|<span data-ttu-id="b1644-186">비즈니스용 Skype</span><span class="sxs-lookup"><span data-stu-id="b1644-186">Skype for Business</span></span>  <br/> | `ipm.externaldata.Skype*` <br/> |
|<span data-ttu-id="b1644-187">Slack Enterprise Grid</span><span class="sxs-lookup"><span data-stu-id="b1644-187">Slack Enterprise Grid</span></span>  <br/> | `ipm.externaldata.Slack.IM` <br/> |
|<span data-ttu-id="b1644-188">SoftEther</span><span class="sxs-lookup"><span data-stu-id="b1644-188">SoftEther</span></span>  <br/> | `ipm.externaldata.SoftEther*` <br/> |
|<span data-ttu-id="b1644-189">Squawker</span><span class="sxs-lookup"><span data-stu-id="b1644-189">Squawker</span></span>  <br/> | `ipm.externaldata.Squawker*` <br/> |
|<span data-ttu-id="b1644-190">Symphony</span><span class="sxs-lookup"><span data-stu-id="b1644-190">Symphony</span></span>  <br/> | `ipm.externaldata.Symphony*` <br/> |
|<span data-ttu-id="b1644-191">Thomson Reuters</span><span class="sxs-lookup"><span data-stu-id="b1644-191">Thomson Reuters</span></span>  <br/> | `ipm.externaldata.Reuters*` <br/> |
| <span data-ttu-id="b1644-192">Thomson Reuters Eikon Messenger</span><span class="sxs-lookup"><span data-stu-id="b1644-192">Thomson Reuters Eikon Messenger</span></span>  <br/> | `ipm.externaldata.ReutersEikon*` <br/> |
|<span data-ttu-id="b1644-193">한자</span><span class="sxs-lookup"><span data-stu-id="b1644-193">Tor</span></span>  <br/> | `ipm.externaldata.Tor*` <br/> |
|<span data-ttu-id="b1644-194">TTT</span><span class="sxs-lookup"><span data-stu-id="b1644-194">TTT</span></span>  <br/> | `ipm.externaldata.TTT*` <br/> |
|<span data-ttu-id="b1644-195">Twitter</span><span class="sxs-lookup"><span data-stu-id="b1644-195">Twitter</span></span>  <br/> | `ipm.externaldata.Twitter*` <br/> |
|<span data-ttu-id="b1644-196">UBS Chat</span><span class="sxs-lookup"><span data-stu-id="b1644-196">UBS Chat</span></span>  <br/> | `ipm.externaldata.UBS*` <br/> |
|<span data-ttu-id="b1644-197">Vimeo</span><span class="sxs-lookup"><span data-stu-id="b1644-197">Vimeo</span></span>  <br/> | `ipm.externaldata.Vimeo*` <br/> |
|<span data-ttu-id="b1644-198">WinMX</span><span class="sxs-lookup"><span data-stu-id="b1644-198">WinMX</span></span>  <br/> | `ipm.externaldata.WinMX*` <br/> |
|<span data-ttu-id="b1644-199">Winny</span><span class="sxs-lookup"><span data-stu-id="b1644-199">Winny</span></span>  <br/> | `ipm.externaldata.Winny*` <br/> |
|<span data-ttu-id="b1644-200">!</span><span class="sxs-lookup"><span data-stu-id="b1644-200">Yahoo!</span></span>  <br/> | `ipm.externaldata.Yahoo!*` <br/> |
|<span data-ttu-id="b1644-201">Yammer</span><span class="sxs-lookup"><span data-stu-id="b1644-201">Yammer</span></span>  <br/> | `ipm.externaldata.Yammer*` <br/> |
|<span data-ttu-id="b1644-202">YellowJacket</span><span class="sxs-lookup"><span data-stu-id="b1644-202">YellowJacket</span></span>  <br/> | `ipm.externaldata.YellowJacket*` <br/> |
|<span data-ttu-id="b1644-203">YouTube</span><span class="sxs-lookup"><span data-stu-id="b1644-203">YouTube</span></span>  <br/> | `ipm.externaldata.YouTube*` <br/> |
