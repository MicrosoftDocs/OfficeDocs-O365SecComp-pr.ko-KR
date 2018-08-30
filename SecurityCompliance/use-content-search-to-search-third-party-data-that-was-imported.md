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
# <a name="use-content-search-to-search-third-party-data-that-was-imported-to-office-365"></a>콘텐츠 검색을 사용 하 여 Office 365로 가져온 제 3 자 데이터를 검색 하려면

[콘텐츠 검색 eDiscovery 도구](content-search.md) 를 사용 하 여 Office 365 보안에서 수 &amp; 준수 센터 타사 데이터 원본에서 Office 365에서 사서함에 가져온 항목을 찾으려고 합니다. 가져온된 모든 타사 데이터 항목을 검색 하는 쿼리를 만들 수 나 특정 타사 데이터 항목에만 검색 쿼리를 만들 수 있습니다. 또한, 쿼리 기반 보존 정책을 만들 수도 있습니다 또는 Office 365의 제 3 자 데이터를 유지 하기 위해 쿼리 기반 eDiscovery 유지 합니다. 
  
타사 데이터 및 Office 365로 가져올 수 있는 타사 데이터 형식의 목록을 가져오는 방법에 대 한 자세한 내용은 [Office 365의 보관 제 3 자 데이터](archiving-third-party-data.md)를 참조 하십시오. 
  
## <a name="creating-a-query-to-search-all-third-party-data"></a>모든 타사 데이터를 검색 하는 쿼리 만들기 (영문)

검색 (또는 대기 장소)를 Office 365로 가져온 했을 때 제 3 자 데이터 형식일 수 사용할 수는 `kind:externaldata` 메시지 속성-값 쌍 키워드 상자에 콘텐츠 검색을 위한 또는 쿼리 기반 보존을 만들 때 합니다. 등 모든 타사 데이터 원본에서 가져온 항목을 검색 하 고 가져온된 항목의 Subject 속성에 "contoso" 라는 단어를 포함 하려면 다음 쿼리를 사용 합니다. 
  
```
kind:externaldata AND subject:contoso
```

이전 키워드 쿼리 예제는 subject 속성을 포함 합니다. 제 3 자 데이터에 대 한 다른 속성의 목록에 대 한 항목 수에 키워드 쿼리에 포함 [Office 365의 보관 제 3 자 데이터](archiving-third-party-data.md#more-information)의 "자세한 정보" 섹션을 참조 하십시오.
  
검색 및 제 3 자 데이터 보존에 대 한 쿼리를 만들 때 검색 결과 범위를 좁힐 조건을 사용할 수도 있습니다. 콘텐츠 검색 쿼리 만들기 (영문) 하는 방법에 대 한 자세한 내용은 [키워드 쿼리 및 콘텐츠 검색에 대 한 검색 조건을](keyword-queries-and-search-conditions.md)참조 하십시오.
  
## <a name="creating-a-query-to-search-specific-types-of-third-party-data"></a>특정 유형의 제 3 자 데이터를 검색 하는 쿼리 만들기 (영문)

모든 유형의 제 3 자 데이터를 검색 하는 대신 콘텐츠 검색에 대 한 키워드 상자에 다음과 같은 메시지 속성-값 쌍을 사용 하 여 쿼리에는 지정 유형의 제 3 자 데이터를 검색 하는 유일한 만들 수 있습니다.
  
```
itemclass:ipm.externaldata.<third-party data type>* 
```

예,만 Subject 속성에 사용 되는 "contoso" 라는 단어를 포함 하는 Facebook 데이터를 검색 하려면 다음 쿼리를 사용 합니다.
  
```
itemclass:ipm.externaldata.Facebook* AND subject:contoso
```

다음 표에 검색할 수 있는 타사 데이터 형식 및 값에 사용 하는 `itemclass:` message 해당 유형의 제 3 자 데이터에 대 한 구체적으로 검색 하는 속성입니다. 참고 해당 쿼리 구문 대/소문자 구분 되지 않습니다. 
  
|**타사 데이터 형식**|**값에 대 한 `itemclass:` 속성**|
|:-----|:-----|
|AIM  <br/> | `ipm.externaldata.AIM*` <br/> |
|American Idol  <br/> | `ipm.externaldata.AmericanIdol*` <br/> |
|AOL with Pivot Client   <br/> | `ipm.externaldata.Pivot.IM` <br/> |
|Apple Juice  <br/> | `ipm.externaldata.AppleJuice*` <br/> |
|Ares  <br/> | `ipm.externaldata.Ares*` <br/> |
|Axs Encrypted  <br/> | `ipm.externaldata.AxsEncrypted*` <br/> |
|Axs Exchange  <br/> | `ipm.externaldata.AxsExchange*` <br/> |
|Axs Local Archive  <br/> | `ipm.externaldata.AxsLocalArchive*` <br/> |
|Axs 개체 틀  <br/> | `ipm.externaldata.AxsPlaceHolder*` <br/> |
|Axs Signed  <br/> | `ipm.externaldata.AxsSigned*` <br/> |
|Bazaarvoice  <br/> | `ipm.externaldata.Bazaarvoice*` <br/> |
|Bearshare  <br/> | `ipm.externaldata.Bearshare*` <br/> |
|들어오는 BitTorrent  <br/> | `ipm.externaldata.BitTorrent*` <br/> |
|Blackberry  <br/> | `ipm.externaldata.Blackberry*` <br/> |
|BlackBerry 통화 기록  <br/> | `ipm.externaldata.BlackBerryCall*` <br/> |
|BlackBerry 메신저  <br/> | `ipm.externaldata.BlackBerryMessenger*` <br/> |
|BlackBerry 핀  <br/> | `ipm.externaldata.BlackBerryPIN*` <br/> |
|BlackBerry SMS  <br/> | `ipm.externaldata.BlackBerrySMS*` <br/> |
|Bloomberg  <br/> | `ipm.externaldata.Bloomberg*` <br/> |
|Bloomberg Mail
  <br/> | `ipm.externaldata.BloombergMail*` <br/> |
|Bloomberg 메시징  <br/> | `ipm.externaldata.BloombergMessaging*` <br/> |
|Box
  <br/> | `ipm.externaldata.Box*` <br/> |
|IM cisco &amp; 현재 상태 서버  <br/> | `ipm.externaldata.Jabber.IM` <br/> |
|Cisco Jabber  <br/> | `ipm.externaldata.Jabber*` <br/> |
|CipherCloud for Salesforce Chatter  <br/> | `ipm.externaldata.Chatter.Post` <br/>  `ipm.externaldata.Chatter.Comment` <br/> |
|Direct Connect  <br/> | `ipm.externaldata.DirectConnect*` <br/> |
|Facebook  <br/> | `ipm.externaldata.Facebook*` <br/> |
|FastTrack  <br/> | `ipm.externaldata.FastTrack*` <br/> |
|FXConnect  <br/> | `ipm.externaldata.FXConnect.chat` <br/> |
|Flickr
  <br/> | `ipm.externaldata.Flickr*` <br/> |
|Gnutella  <br/> | `ipm.externaldata.Gnutella*` <br/> |
|Google+
  <br/> | `ipm.externaldata.GooglePlus*` <br/> |
|Google Talk  <br/> | `ipm.externaldata.GoogleTalk*` <br/> |
|GoToMyPC  <br/> | `ipm.externaldata.GoToMyPC*` <br/> |
|HipChat  <br/> | `ipm.externaldata.HipChat*` <br/> |
|Hopster  <br/> | `ipm.externaldata.Hopster*` <br/> |
|HubConnex  <br/> | `ipm.externaldata.HubConnex*` <br/> |
|IBM 연결  <br/> | `ipm.externaldata.Connections*` <br/> |
|IBM SameTime  <br/> | `ipm.externaldata.Sametime*` <br/> |
|ICE 채팅  <br/> | `ipm.externaldata.ICEChat.Chat` <br/> |
|Indii Messenger
  <br/> | `ipm.externaldata.Indii*` <br/> |
|Instagram
  <br/> | `ipm.externaldata.Instagram*` <br/> |
|Instant Bloomberg
  <br/> | `ipm.externaldata.InstantBloomberg*` <br/> |
|InvestEdge  <br/> | `ipm.externaldata.InvestEdge*` <br/> |
|IRC  <br/> | `ipm.externaldata.IRC*` <br/> |
|Jive
  <br/> | `ipm.externaldata.Jive*` <br/> |
|JiveApiRetention  <br/> | `ipm.externaldata.JiveApiRetention*` <br/> |
|JXTA  <br/> | `ipm.externaldata.JXTA*` <br/> |
|LinkedIn  <br/> | `ipm.externaldata.LinkedIn*` <br/> |
|MFTP  <br/> | `ipm.externaldata.MFTP*` <br/> |
|Microsoft UC  <br/> | `ipm.externaldata.MicrosoftUC*` <br/> |
|주의 맞춤  <br/> | `ipm.externaldata.MindAlign*` <br/> |
|Mobile Guard  <br/> | `ipm.externaldata.MobileGuard*` <br/> |
|MSN  <br/> | `ipm.externaldata.MSN*` <br/> |
|MySpace  <br/> | `ipm.externaldata.MySpace*` <br/> |
|NEONetwork  <br/> | `ipm.externaldata.NEONetwork*` <br/> |
|OpenNap  <br/> | `ipm.externaldata.OpenNap*` <br/> |
|Pinterest  <br/> | `ipm.externaldata.Pinterest*` <br/> |
|Pivot  <br/> | `ipm.externaldata.Pivot*` <br/> |
|QQ  <br/> | `ipm.externaldata.QQ*` <br/> |
|Microsoft SharePoint  <br/> | `ipm.externaldata.SharePoint*` <br/> |
|Salesforce Chatter  <br/> | `ipm.externaldata.Chatter*` <br/> |
|비즈니스용 Skype  <br/> | `ipm.externaldata.Skype*` <br/> |
|Slack Enterprise Grid  <br/> | `ipm.externaldata.Slack.IM` <br/> |
|SoftEther  <br/> | `ipm.externaldata.SoftEther*` <br/> |
|
Squawker
  <br/> | `ipm.externaldata.Squawker*` <br/> |
|Symphony
  <br/> | `ipm.externaldata.Symphony*` <br/> |
|Thomson Reuters  <br/> | `ipm.externaldata.Reuters*` <br/> |
| Thomson Reuters Eikon Messenger
  <br/> | `ipm.externaldata.ReutersEikon*` <br/> |
|Tor  <br/> | `ipm.externaldata.Tor*` <br/> |
|TTT  <br/> | `ipm.externaldata.TTT*` <br/> |
|Twitter  <br/> | `ipm.externaldata.Twitter*` <br/> |
|UBS Chat
  <br/> | `ipm.externaldata.UBS*` <br/> |
|Vimeo  <br/> | `ipm.externaldata.Vimeo*` <br/> |
|WinMX  <br/> | `ipm.externaldata.WinMX*` <br/> |
|Winny  <br/> | `ipm.externaldata.Winny*` <br/> |
|Yahoo!  <br/> | `ipm.externaldata.Yahoo!*` <br/> |
|Yammer  <br/> | `ipm.externaldata.Yammer*` <br/> |
|YellowJacket  <br/> | `ipm.externaldata.YellowJacket*` <br/> |
|YouTube  <br/> | `ipm.externaldata.YouTube*` <br/> |
