---
title: 콘텐츠 검색을 사용 하 여 Office 365로 가져온 제 3 자 데이터를 검색 하려면
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 10/27/2017
ms.audience: Admin
ms.topic: reference
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: ec2677ff-c4d7-4363-a9e7-22c80e015688
description: 콘텐츠 검색 eDiscovery 도구를 사용 하 여 Office 365에서 사서함에 제 3 자 데이터 원본에서 가져온 항목을 찾으려고 합니다. 특정 타사 데이터 형식에 대 한 검색 쿼리를 만들거나 가져온된 모든 항목에 대 한 검색 쿼리를 만들 수 있습니다. 이 문서는 Office 365로 가져올 수 있는 타사 데이터 형식을 검색 키워드 쿼리에서 사용할 수 있는 값을 나열 합니다.
ms.openlocfilehash: 90d9dc52dcd9dba9bc273dfcf1c5f22e3913d6ba
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22533746"
---
# <a name="use-content-search-to-search-third-party-data-that-was-imported-to-office-365"></a><span data-ttu-id="7f8a4-105">콘텐츠 검색을 사용 하 여 Office 365로 가져온 제 3 자 데이터를 검색 하려면</span><span class="sxs-lookup"><span data-stu-id="7f8a4-105">Use Content Search to search third-party data that was imported to Office 365</span></span>

<span data-ttu-id="7f8a4-p102">[콘텐츠 검색 eDiscovery 도구](content-search.md) 를 사용 하 여 Office 365 보안에서 수 &amp; 준수 센터 타사 데이터 원본에서 Office 365에서 사서함에 가져온 항목을 찾으려고 합니다. 가져온된 모든 타사 데이터 항목을 검색 하는 쿼리를 만들 수 나 특정 타사 데이터 항목에만 검색 쿼리를 만들 수 있습니다. 또한, 쿼리 기반 보존 정책을 만들 수도 있습니다 또는 Office 365의 제 3 자 데이터를 유지 하기 위해 쿼리 기반 eDiscovery 유지 합니다.</span><span class="sxs-lookup"><span data-stu-id="7f8a4-p102">You can use the [Content Search eDiscovery tool](content-search.md) in the Office 365 Security &amp; Compliance Center to search for items that were imported to mailboxes in Office 365 from a third-party data source. You can create a query to search all imported third-party data items or you can create a query to only search specific third-party data items. Additionally, you can also create a query-based Preservation Policy or a query-based eDiscovery hold to preserve third-party data in Office 365.</span></span> 
  
<span data-ttu-id="7f8a4-109">타사 데이터 및 Office 365로 가져올 수 있는 타사 데이터 형식의 목록을 가져오는 방법에 대 한 자세한 내용은 [Office 365의 보관 제 3 자 데이터](archiving-third-party-data.md)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="7f8a4-109">For more information about importing third-party data and a list of the third-party data types that can be imported to Office 365, see [Archiving third-party data in Office 365](archiving-third-party-data.md).</span></span> 
  
## <a name="creating-a-query-to-search-all-third-party-data"></a><span data-ttu-id="7f8a4-110">모든 타사 데이터를 검색 하는 쿼리 만들기 (영문)</span><span class="sxs-lookup"><span data-stu-id="7f8a4-110">Creating a query to search all third-party data</span></span>

<span data-ttu-id="7f8a4-p103">검색 (또는 대기 장소)를 Office 365로 가져온 했을 때 제 3 자 데이터 형식일 수 사용할 수는 `kind:externaldata` 메시지 속성-값 쌍 키워드 상자에 콘텐츠 검색을 위한 또는 쿼리 기반 보존을 만들 때 합니다. 등 모든 타사 데이터 원본에서 가져온 항목을 검색 하 고 가져온된 항목의 Subject 속성에 "contoso" 라는 단어를 포함 하려면 다음 쿼리를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="7f8a4-p103">To search (or place on hold) any type of third-party data that you've imported to Office 365, you can you can use the  `kind:externaldata` message property-value pair in the keyword box for a Content Search or when creating a query-based hold. For example, to search for items that were imported from any third-party data source and contain the word "contoso" in the Subject property of the imported item, you would use the following query:</span></span> 
  
```
kind:externaldata AND subject:contoso
```

<span data-ttu-id="7f8a4-p104">이전 키워드 쿼리 예제는 subject 속성을 포함 합니다. 제 3 자 데이터에 대 한 다른 속성의 목록에 대 한 항목 수에 키워드 쿼리에 포함 [Office 365의 보관 제 3 자 데이터](archiving-third-party-data.md#more-information)의 "자세한 정보" 섹션을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="7f8a4-p104">The previous keyword query example includes the subject property. For a list of other properties for third-party data items that can included in a keyword query, see the "More information" section in [Archiving third-party data in Office 365](archiving-third-party-data.md#more-information).</span></span>
  
<span data-ttu-id="7f8a4-p105">검색 및 제 3 자 데이터 보존에 대 한 쿼리를 만들 때 검색 결과 범위를 좁힐 조건을 사용할 수도 있습니다. 콘텐츠 검색 쿼리 만들기 (영문) 하는 방법에 대 한 자세한 내용은 [키워드 쿼리 및 콘텐츠 검색에 대 한 검색 조건을](keyword-queries-and-search-conditions.md)참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="7f8a4-p105">When creating queries to search and hold third-party data, you can also use conditions to narrow the search results. For more information about creating Content Search queries, see [Keyword queries and search conditions for Content Search](keyword-queries-and-search-conditions.md).</span></span>
  
## <a name="creating-a-query-to-search-specific-types-of-third-party-data"></a><span data-ttu-id="7f8a4-117">특정 유형의 제 3 자 데이터를 검색 하는 쿼리 만들기 (영문)</span><span class="sxs-lookup"><span data-stu-id="7f8a4-117">Creating a query to search specific types of third-party data</span></span>

<span data-ttu-id="7f8a4-118">모든 유형의 제 3 자 데이터를 검색 하는 대신 콘텐츠 검색에 대 한 키워드 상자에 다음과 같은 메시지 속성-값 쌍을 사용 하 여 쿼리에는 지정 유형의 제 3 자 데이터를 검색 하는 유일한 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7f8a4-118">Instead of searching all types of third-party data, you can create queries that only search for a specify type of third-party data by using the following message property-value pair in the keyword box for a Content Search:</span></span>
  
```
itemclass:ipm.externaldata.<third-party data type>* 
```

<span data-ttu-id="7f8a4-119">예,만 Subject 속성에 사용 되는 "contoso" 라는 단어를 포함 하는 Facebook 데이터를 검색 하려면 다음 쿼리를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="7f8a4-119">For example, to only search Facebook data that contains the word "contoso" in the Subject property, you would use the following query:</span></span>
  
```
itemclass:ipm.externaldata.Facebook* AND subject:contoso
```

<span data-ttu-id="7f8a4-p106">다음 표에 검색할 수 있는 타사 데이터 형식 및 값에 사용 하는 `itemclass:` message 해당 유형의 제 3 자 데이터에 대 한 구체적으로 검색 하는 속성입니다. 참고 해당 쿼리 구문 대/소문자 구분 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7f8a4-p106">The following table lists the third-party data types that you can search, and the value to use for the  `itemclass:` message property to specifically search for that type of third-party data. Note that the query syntax isn't case sensitive.</span></span> 
  
|<span data-ttu-id="7f8a4-122">**타사 데이터 형식**</span><span class="sxs-lookup"><span data-stu-id="7f8a4-122">**Third-party data type**</span></span>|<span data-ttu-id="7f8a4-123">**값에 대 한 `itemclass:` 속성**</span><span class="sxs-lookup"><span data-stu-id="7f8a4-123">**Value for  `itemclass:` property**</span></span>|
|:-----|:-----|
|<span data-ttu-id="7f8a4-124">AIM</span><span class="sxs-lookup"><span data-stu-id="7f8a4-124">AIM</span></span>  <br/> | `ipm.externaldata.AIM*` <br/> |
|<span data-ttu-id="7f8a4-125">American Idol</span><span class="sxs-lookup"><span data-stu-id="7f8a4-125">American Idol</span></span>  <br/> | `ipm.externaldata.AmericanIdol*` <br/> |
|<span data-ttu-id="7f8a4-126">AOL with Pivot Client </span><span class="sxs-lookup"><span data-stu-id="7f8a4-126">AOL with Pivot Client</span></span>  <br/> | `ipm.externaldata.Pivot.IM` <br/> |
|<span data-ttu-id="7f8a4-127">Apple Juice</span><span class="sxs-lookup"><span data-stu-id="7f8a4-127">Apple Juice</span></span>  <br/> | `ipm.externaldata.AppleJuice*` <br/> |
|<span data-ttu-id="7f8a4-128">Ares</span><span class="sxs-lookup"><span data-stu-id="7f8a4-128">Ares</span></span>  <br/> | `ipm.externaldata.Ares*` <br/> |
|<span data-ttu-id="7f8a4-129">Axs Encrypted</span><span class="sxs-lookup"><span data-stu-id="7f8a4-129">Axs Encrypted</span></span>  <br/> | `ipm.externaldata.AxsEncrypted*` <br/> |
|<span data-ttu-id="7f8a4-130">Axs Exchange</span><span class="sxs-lookup"><span data-stu-id="7f8a4-130">Axs Exchange</span></span>  <br/> | `ipm.externaldata.AxsExchange*` <br/> |
|<span data-ttu-id="7f8a4-131">Axs Local Archive</span><span class="sxs-lookup"><span data-stu-id="7f8a4-131">Axs Local Archive</span></span>  <br/> | `ipm.externaldata.AxsLocalArchive*` <br/> |
|<span data-ttu-id="7f8a4-132">Axs 개체 틀</span><span class="sxs-lookup"><span data-stu-id="7f8a4-132">Axs Placeholder</span></span>  <br/> | `ipm.externaldata.AxsPlaceHolder*` <br/> |
|<span data-ttu-id="7f8a4-133">Axs Signed</span><span class="sxs-lookup"><span data-stu-id="7f8a4-133">Axs Signed</span></span>  <br/> | `ipm.externaldata.AxsSigned*` <br/> |
|<span data-ttu-id="7f8a4-134">Bazaarvoice</span><span class="sxs-lookup"><span data-stu-id="7f8a4-134">Bazaarvoice</span></span>  <br/> | `ipm.externaldata.Bazaarvoice*` <br/> |
|<span data-ttu-id="7f8a4-135">Bearshare</span><span class="sxs-lookup"><span data-stu-id="7f8a4-135">Bearshare</span></span>  <br/> | `ipm.externaldata.Bearshare*` <br/> |
|<span data-ttu-id="7f8a4-136">들어오는 BitTorrent</span><span class="sxs-lookup"><span data-stu-id="7f8a4-136">BitTorrent</span></span>  <br/> | `ipm.externaldata.BitTorrent*` <br/> |
|<span data-ttu-id="7f8a4-137">Blackberry</span><span class="sxs-lookup"><span data-stu-id="7f8a4-137">Blackberry</span></span>  <br/> | `ipm.externaldata.Blackberry*` <br/> |
|<span data-ttu-id="7f8a4-138">BlackBerry 통화 기록</span><span class="sxs-lookup"><span data-stu-id="7f8a4-138">BlackBerry Call Logs</span></span>  <br/> | `ipm.externaldata.BlackBerryCall*` <br/> |
|<span data-ttu-id="7f8a4-139">BlackBerry 메신저</span><span class="sxs-lookup"><span data-stu-id="7f8a4-139">BlackBerry Messenger</span></span>  <br/> | `ipm.externaldata.BlackBerryMessenger*` <br/> |
|<span data-ttu-id="7f8a4-140">BlackBerry 핀</span><span class="sxs-lookup"><span data-stu-id="7f8a4-140">BlackBerry PIN</span></span>  <br/> | `ipm.externaldata.BlackBerryPIN*` <br/> |
|<span data-ttu-id="7f8a4-141">BlackBerry SMS</span><span class="sxs-lookup"><span data-stu-id="7f8a4-141">BlackBerry SMS</span></span>  <br/> | `ipm.externaldata.BlackBerrySMS*` <br/> |
|<span data-ttu-id="7f8a4-142">Bloomberg</span><span class="sxs-lookup"><span data-stu-id="7f8a4-142">Bloomberg</span></span>  <br/> | `ipm.externaldata.Bloomberg*` <br/> |
|<span data-ttu-id="7f8a4-143">Bloomberg Mail
</span><span class="sxs-lookup"><span data-stu-id="7f8a4-143">Bloomberg Mail</span></span>  <br/> | `ipm.externaldata.BloombergMail*` <br/> |
|<span data-ttu-id="7f8a4-144">Bloomberg 메시징</span><span class="sxs-lookup"><span data-stu-id="7f8a4-144">Bloomberg Messaging</span></span>  <br/> | `ipm.externaldata.BloombergMessaging*` <br/> |
|<span data-ttu-id="7f8a4-145">Box
</span><span class="sxs-lookup"><span data-stu-id="7f8a4-145">Box</span></span>  <br/> | `ipm.externaldata.Box*` <br/> |
|<span data-ttu-id="7f8a4-146">IM cisco &amp; 현재 상태 서버</span><span class="sxs-lookup"><span data-stu-id="7f8a4-146">Cisco IM &amp; Presence Server</span></span>  <br/> | `ipm.externaldata.Jabber.IM` <br/> |
|<span data-ttu-id="7f8a4-147">Cisco Jabber</span><span class="sxs-lookup"><span data-stu-id="7f8a4-147">Cisco Jabber</span></span>  <br/> | `ipm.externaldata.Jabber*` <br/> |
|<span data-ttu-id="7f8a4-148">CipherCloud for Salesforce Chatter</span><span class="sxs-lookup"><span data-stu-id="7f8a4-148">CipherCloud for Salesforce Chatter</span></span>  <br/> | `ipm.externaldata.Chatter.Post` <br/>  `ipm.externaldata.Chatter.Comment` <br/> |
|<span data-ttu-id="7f8a4-149">Direct Connect</span><span class="sxs-lookup"><span data-stu-id="7f8a4-149">Direct Connect</span></span>  <br/> | `ipm.externaldata.DirectConnect*` <br/> |
|<span data-ttu-id="7f8a4-150">Facebook</span><span class="sxs-lookup"><span data-stu-id="7f8a4-150">Facebook</span></span>  <br/> | `ipm.externaldata.Facebook*` <br/> |
|<span data-ttu-id="7f8a4-151">FastTrack</span><span class="sxs-lookup"><span data-stu-id="7f8a4-151">FastTrack</span></span>  <br/> | `ipm.externaldata.FastTrack*` <br/> |
|<span data-ttu-id="7f8a4-152">FXConnect</span><span class="sxs-lookup"><span data-stu-id="7f8a4-152">FXConnect</span></span>  <br/> | `ipm.externaldata.FXConnect.chat` <br/> |
|<span data-ttu-id="7f8a4-153">Flickr
</span><span class="sxs-lookup"><span data-stu-id="7f8a4-153">Flickr</span></span>  <br/> | `ipm.externaldata.Flickr*` <br/> |
|<span data-ttu-id="7f8a4-154">Gnutella</span><span class="sxs-lookup"><span data-stu-id="7f8a4-154">Gnutella</span></span>  <br/> | `ipm.externaldata.Gnutella*` <br/> |
|<span data-ttu-id="7f8a4-155">Google+
</span><span class="sxs-lookup"><span data-stu-id="7f8a4-155">Google+</span></span>  <br/> | `ipm.externaldata.GooglePlus*` <br/> |
|<span data-ttu-id="7f8a4-156">Google Talk</span><span class="sxs-lookup"><span data-stu-id="7f8a4-156">Google Talk</span></span>  <br/> | `ipm.externaldata.GoogleTalk*` <br/> |
|<span data-ttu-id="7f8a4-157">GoToMyPC</span><span class="sxs-lookup"><span data-stu-id="7f8a4-157">GoToMyPC</span></span>  <br/> | `ipm.externaldata.GoToMyPC*` <br/> |
|<span data-ttu-id="7f8a4-158">HipChat</span><span class="sxs-lookup"><span data-stu-id="7f8a4-158">HipChat</span></span>  <br/> | `ipm.externaldata.HipChat*` <br/> |
|<span data-ttu-id="7f8a4-159">Hopster</span><span class="sxs-lookup"><span data-stu-id="7f8a4-159">Hopster</span></span>  <br/> | `ipm.externaldata.Hopster*` <br/> |
|<span data-ttu-id="7f8a4-160">HubConnex</span><span class="sxs-lookup"><span data-stu-id="7f8a4-160">HubConnex</span></span>  <br/> | `ipm.externaldata.HubConnex*` <br/> |
|<span data-ttu-id="7f8a4-161">IBM 연결</span><span class="sxs-lookup"><span data-stu-id="7f8a4-161">IBM Connections</span></span>  <br/> | `ipm.externaldata.Connections*` <br/> |
|<span data-ttu-id="7f8a4-162">IBM SameTime</span><span class="sxs-lookup"><span data-stu-id="7f8a4-162">IBM SameTime</span></span>  <br/> | `ipm.externaldata.Sametime*` <br/> |
|<span data-ttu-id="7f8a4-163">ICE 채팅</span><span class="sxs-lookup"><span data-stu-id="7f8a4-163">ICE Chat</span></span>  <br/> | `ipm.externaldata.ICEChat.Chat` <br/> |
|<span data-ttu-id="7f8a4-164">Indii Messenger
</span><span class="sxs-lookup"><span data-stu-id="7f8a4-164">Indii Messenger</span></span>  <br/> | `ipm.externaldata.Indii*` <br/> |
|<span data-ttu-id="7f8a4-165">Instagram
</span><span class="sxs-lookup"><span data-stu-id="7f8a4-165">Instagram</span></span>  <br/> | `ipm.externaldata.Instagram*` <br/> |
|<span data-ttu-id="7f8a4-166">Instant Bloomberg
</span><span class="sxs-lookup"><span data-stu-id="7f8a4-166">Instant Bloomberg</span></span>  <br/> | `ipm.externaldata.InstantBloomberg*` <br/> |
|<span data-ttu-id="7f8a4-167">InvestEdge</span><span class="sxs-lookup"><span data-stu-id="7f8a4-167">InvestEdge</span></span>  <br/> | `ipm.externaldata.InvestEdge*` <br/> |
|<span data-ttu-id="7f8a4-168">IRC</span><span class="sxs-lookup"><span data-stu-id="7f8a4-168">IRC</span></span>  <br/> | `ipm.externaldata.IRC*` <br/> |
|<span data-ttu-id="7f8a4-169">Jive
</span><span class="sxs-lookup"><span data-stu-id="7f8a4-169">Jive</span></span>  <br/> | `ipm.externaldata.Jive*` <br/> |
|<span data-ttu-id="7f8a4-170">JiveApiRetention</span><span class="sxs-lookup"><span data-stu-id="7f8a4-170">JiveApiRetention</span></span>  <br/> | `ipm.externaldata.JiveApiRetention*` <br/> |
|<span data-ttu-id="7f8a4-171">JXTA</span><span class="sxs-lookup"><span data-stu-id="7f8a4-171">JXTA</span></span>  <br/> | `ipm.externaldata.JXTA*` <br/> |
|<span data-ttu-id="7f8a4-172">LinkedIn</span><span class="sxs-lookup"><span data-stu-id="7f8a4-172">LinkedIn</span></span>  <br/> | `ipm.externaldata.LinkedIn*` <br/> |
|<span data-ttu-id="7f8a4-173">MFTP</span><span class="sxs-lookup"><span data-stu-id="7f8a4-173">MFTP</span></span>  <br/> | `ipm.externaldata.MFTP*` <br/> |
|<span data-ttu-id="7f8a4-174">Microsoft UC</span><span class="sxs-lookup"><span data-stu-id="7f8a4-174">Microsoft UC</span></span>  <br/> | `ipm.externaldata.MicrosoftUC*` <br/> |
|<span data-ttu-id="7f8a4-175">주의 맞춤</span><span class="sxs-lookup"><span data-stu-id="7f8a4-175">Mind Align</span></span>  <br/> | `ipm.externaldata.MindAlign*` <br/> |
|<span data-ttu-id="7f8a4-176">Mobile Guard</span><span class="sxs-lookup"><span data-stu-id="7f8a4-176">Mobile Guard</span></span>  <br/> | `ipm.externaldata.MobileGuard*` <br/> |
|<span data-ttu-id="7f8a4-177">MSN</span><span class="sxs-lookup"><span data-stu-id="7f8a4-177">MSN</span></span>  <br/> | `ipm.externaldata.MSN*` <br/> |
|<span data-ttu-id="7f8a4-178">MySpace</span><span class="sxs-lookup"><span data-stu-id="7f8a4-178">MySpace</span></span>  <br/> | `ipm.externaldata.MySpace*` <br/> |
|<span data-ttu-id="7f8a4-179">NEONetwork</span><span class="sxs-lookup"><span data-stu-id="7f8a4-179">NEONetwork</span></span>  <br/> | `ipm.externaldata.NEONetwork*` <br/> |
|<span data-ttu-id="7f8a4-180">OpenNap</span><span class="sxs-lookup"><span data-stu-id="7f8a4-180">OpenNap</span></span>  <br/> | `ipm.externaldata.OpenNap*` <br/> |
|<span data-ttu-id="7f8a4-181">Pinterest</span><span class="sxs-lookup"><span data-stu-id="7f8a4-181">Pinterest</span></span>  <br/> | `ipm.externaldata.Pinterest*` <br/> |
|<span data-ttu-id="7f8a4-182">Pivot</span><span class="sxs-lookup"><span data-stu-id="7f8a4-182">Pivot</span></span>  <br/> | `ipm.externaldata.Pivot*` <br/> |
|<span data-ttu-id="7f8a4-183">QQ</span><span class="sxs-lookup"><span data-stu-id="7f8a4-183">QQ</span></span>  <br/> | `ipm.externaldata.QQ*` <br/> |
|<span data-ttu-id="7f8a4-184">Microsoft SharePoint</span><span class="sxs-lookup"><span data-stu-id="7f8a4-184">Microsoft SharePoint</span></span>  <br/> | `ipm.externaldata.SharePoint*` <br/> |
|<span data-ttu-id="7f8a4-185">Salesforce Chatter</span><span class="sxs-lookup"><span data-stu-id="7f8a4-185">Salesforce Chatter</span></span>  <br/> | `ipm.externaldata.Chatter*` <br/> |
|<span data-ttu-id="7f8a4-186">비즈니스용 Skype</span><span class="sxs-lookup"><span data-stu-id="7f8a4-186">Skype for Business</span></span>  <br/> | `ipm.externaldata.Skype*` <br/> |
|<span data-ttu-id="7f8a4-187">Slack Enterprise Grid</span><span class="sxs-lookup"><span data-stu-id="7f8a4-187">Slack Enterprise Grid</span></span>  <br/> | `ipm.externaldata.Slack.IM` <br/> |
|<span data-ttu-id="7f8a4-188">SoftEther</span><span class="sxs-lookup"><span data-stu-id="7f8a4-188">SoftEther</span></span>  <br/> | `ipm.externaldata.SoftEther*` <br/> |
|<span data-ttu-id="7f8a4-189">
Squawker
</span><span class="sxs-lookup"><span data-stu-id="7f8a4-189">Squawker</span></span>  <br/> | `ipm.externaldata.Squawker*` <br/> |
|<span data-ttu-id="7f8a4-190">Symphony
</span><span class="sxs-lookup"><span data-stu-id="7f8a4-190">Symphony</span></span>  <br/> | `ipm.externaldata.Symphony*` <br/> |
|<span data-ttu-id="7f8a4-191">Thomson Reuters</span><span class="sxs-lookup"><span data-stu-id="7f8a4-191">Thomson Reuters</span></span>  <br/> | `ipm.externaldata.Reuters*` <br/> |
| <span data-ttu-id="7f8a4-192">Thomson Reuters Eikon Messenger
</span><span class="sxs-lookup"><span data-stu-id="7f8a4-192">Thomson Reuters Eikon Messenger</span></span>  <br/> | `ipm.externaldata.ReutersEikon*` <br/> |
|<span data-ttu-id="7f8a4-193">Tor</span><span class="sxs-lookup"><span data-stu-id="7f8a4-193">Tor</span></span>  <br/> | `ipm.externaldata.Tor*` <br/> |
|<span data-ttu-id="7f8a4-194">TTT</span><span class="sxs-lookup"><span data-stu-id="7f8a4-194">TTT</span></span>  <br/> | `ipm.externaldata.TTT*` <br/> |
|<span data-ttu-id="7f8a4-195">Twitter</span><span class="sxs-lookup"><span data-stu-id="7f8a4-195">Twitter</span></span>  <br/> | `ipm.externaldata.Twitter*` <br/> |
|<span data-ttu-id="7f8a4-196">UBS Chat
</span><span class="sxs-lookup"><span data-stu-id="7f8a4-196">UBS Chat</span></span>  <br/> | `ipm.externaldata.UBS*` <br/> |
|<span data-ttu-id="7f8a4-197">Vimeo</span><span class="sxs-lookup"><span data-stu-id="7f8a4-197">Vimeo</span></span>  <br/> | `ipm.externaldata.Vimeo*` <br/> |
|<span data-ttu-id="7f8a4-198">WinMX</span><span class="sxs-lookup"><span data-stu-id="7f8a4-198">WinMX</span></span>  <br/> | `ipm.externaldata.WinMX*` <br/> |
|<span data-ttu-id="7f8a4-199">Winny</span><span class="sxs-lookup"><span data-stu-id="7f8a4-199">Winny</span></span>  <br/> | `ipm.externaldata.Winny*` <br/> |
|<span data-ttu-id="7f8a4-200">Yahoo!</span><span class="sxs-lookup"><span data-stu-id="7f8a4-200">Yahoo!</span></span>  <br/> | `ipm.externaldata.Yahoo!*` <br/> |
|<span data-ttu-id="7f8a4-201">Yammer</span><span class="sxs-lookup"><span data-stu-id="7f8a4-201">Yammer</span></span>  <br/> | `ipm.externaldata.Yammer*` <br/> |
|<span data-ttu-id="7f8a4-202">YellowJacket</span><span class="sxs-lookup"><span data-stu-id="7f8a4-202">YellowJacket</span></span>  <br/> | `ipm.externaldata.YellowJacket*` <br/> |
|<span data-ttu-id="7f8a4-203">YouTube</span><span class="sxs-lookup"><span data-stu-id="7f8a4-203">YouTube</span></span>  <br/> | `ipm.externaldata.YouTube*` <br/> |
