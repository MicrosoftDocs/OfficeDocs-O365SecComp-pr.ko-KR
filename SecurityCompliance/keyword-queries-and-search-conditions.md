---
title: 콘텐츠 검색에 대한 키워드 쿼리 및 검색 조건
ms.author: markjjo
author: markjjo
manager: laurawi
audience: Admin
ms.topic: reference
f1_keywords:
- ms.o365.cc.SearchQueryLearnMore
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- Strat_O365_IP
- M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: c4639c2e-7223-4302-8e0d-b6e10f1c3be3
description: '보안 & 준수 센터의 콘텐츠 검색 도구를 사용 하 여 Exchange Online 사서함 및 SharePoint 또는 비즈니스용 OneDrive 사이트에서 검색할 수 있는 전자 메일 및 파일 속성에 대해 알아봅니다.  '
ms.openlocfilehash: 01cc40f983ddae6db090f531bc33fc5cc7a638ed
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/17/2019
ms.locfileid: "34152500"
---
# <a name="keyword-queries-and-search-conditions-for-content-search"></a>콘텐츠 검색에 대한 키워드 쿼리 및 검색 조건

이 항목에서는 보안 & 준수 센터의 콘텐츠 검색 기능을 사용 하 여 Exchange Online의 전자 메일 항목 및 SharePoint에 저장 된 문서 및 비즈니스용 OneDrive 사이트에 대해 검색할 수 있는 전자 메일 및 문서 속성에 대해 설명 합니다. 보안 & 준수 센터 PowerShell에서 ** \*-ComplianceSearch** cmdlet을 사용 하 여 이러한 속성을 검색할 수도 있습니다. 또한 다음 항목에 대해 설명 합니다.   
  
- 부울 검색 연산자, 검색 조건 및 기타 검색 쿼리 기법을 사용 하 여 검색 결과를 구체화 합니다.
    
- SharePoint 및 비즈니스용 OneDrive에서 중요 한 데이터 형식 및 사용자 지정 중요 한 데이터 형식 검색
    
- 조직 외부의 사용자와 공유 되는 사이트 콘텐츠 검색
    
콘텐츠 검색을 만드는 방법에 대 한 단계별 지침은 [Office 365의 콘텐츠 검색](content-search.md)을 참조 하세요.

  
> [!NOTE]
> Security & 준수 센터의 콘텐츠 검색 및 security & 준수 센터 PowerShell의 해당 ** \*ComplianceSearch** cmdlet은 KQL (키워드 쿼리 언어)를 사용 합니다. 자세한 내용은 [키워드 쿼리 언어 구문 참조](https://go.microsoft.com/fwlink/?LinkId=269603)를 참조 하십시오. 
  
## <a name="searchable-email-properties"></a>검색 가능한 전자 메일 속성

다음 표에는 보안 & 준수 센터의 콘텐츠 검색 기능을 사용 하거나 **ComplianceSearch** 또는 **ComplianceSearch** cmdlet을 사용 하 여 검색할 수 있는 전자 메일 메시지 속성이 나와 있습니다. 이 표에는 각 속성에 대 한 _속성의 값_ 구문과 예제에서 반환 된 검색 결과에 대 한 설명이 포함 되어 있습니다. 키워드 상자에 콘텐츠 `property:value` 검색에 대 한 이러한 쌍을 입력할 수 있습니다. 
  
|**속성**|**속성 설명**|**예제**|**예제에서 반환된 검색 결과**|
|:-----|:-----|:-----|:-----|
|AttachmentNames|전자 메일 메시지에 첨부되는 파일의 이름입니다.|`attachmentnames:annualreport.ppt`  <br/> `attachmentnames:annual*`|annualreport.ppt라는 파일이 첨부된 메시지입니다. 두 번째 예제에서는 와일드카드를 사용하여 첨부 파일의 파일 이름에 "annual"이라는 단어가 있는 메시지를 반환합니다.|
|대상|전자 메일 메시지의 숨은 참조 필드입니다. <sup>1</sup>|`bcc:pilarp@contoso.com`  <br/> `bcc:pilarp`  <br/> `bcc:"Pilar Pinilla"`|모든 예제는 숨은 참조 필드에 Pilar Pinilla가 포함된 메시지를 반환합니다.|
|범주| 검색할 범주입니다. 범주는 Outlook 또는 웹용 Outlook (이전의 Outlook Web App)을 사용 하 여 사용자가 정의할 수 있습니다. 가능한 값은 다음과 같습니다.  <br/><br/>  색상  <br/>  친환경  <br/>  /  <br/>  자주색  <br/>  빨강  <br/>  노랑|`category:"Red Category"`|원본 사서함에서 red 범주가 지정된 메시지입니다. |
|참조란|전자 메일 메시지의 참조 필드입니다. <sup>1</sup>|`cc:pilarp@contoso.com`  <br/> `cc:"Pilar Pinilla"`|두 예제 모두에서 참조 필드에 Pilar Pinilla가 지정된 메시지입니다.|
|Folderid|특정 사서함 폴더의 폴더 ID (GUID)입니다. 이 속성을 사용 하는 경우에는 지정 된 폴더가 있는 사서함을 검색 해야 합니다. 지정한 폴더만 검색 됩니다. 폴더에 있는 모든 하위 폴더는 검색 되지 않습니다. 하위 폴더를 검색 하려면 검색 하려는 하위 폴더에 대 한 Folderid 속성을 사용 해야 합니다.  <br/> Folderid 속성을 검색 하 고 스크립트를 사용 하 여 특정 사서함의 폴더 Id를 가져오는 방법에 대 한 자세한 내용은 using [Content Search In Office 365 in the 대상 모음](use-content-search-for-targeted-collections.md)을 참조 하십시오.|`folderid:4D6DD7F943C29041A65787E30F02AD1F00000000013A0000`  <br/> `folderid:2370FB455F82FC44BE31397F47B632A70000000001160000 AND participants:garthf@contoso.com`|첫 번째 예에서는 지정 된 사서함 폴더의 모든 항목을 반환 합니다. 두 번째 예에서는 garthf@contoso.com에서 보내거나 받은 지정 된 사서함 폴더의 모든 항목을 반환 합니다.|
|From|전자 메일 메시지의 보낸 사람입니다. <sup>1</sup>|`from:pilarp@contoso.com`  <br/> `from:contoso.com`|지정된 사용자가 보냈거나 지정된 도메인에서 보낸 메시지입니다.|
|HasAttachment|메시지에 첨부 파일이 있는지 여부를 나타냅니다. **True** 또는 **false**값을 사용 합니다.|`from:pilar@contoso.com AND hasattachment:true`|첨부 파일이 있는 지정 된 사용자가 보낸 메시지입니다.|
|얼마나|보낸 사람이 메시지를 보낼 때 지정할 수 있는 전자 메일 메시지의 중요도입니다. 기본적으로 보낸 사람이 중요도를 **높음** 또는 **낮음**으로 설정하지 않았다면 메시지는 보통 중요도로 전송됩니다.|`importance:high`  <br/> `importance:medium`  <br/> `importance:low`|높음 중요도, 보통 중요도 또는 낮은 중요도로 표시된 메시지입니다.|
|IsRead|메시지를 읽었는지 여부를 나타냅니다. **True** 또는 **false**값을 사용 합니다.|`isread:true`  <br/> `isread:false`|첫 번째 예에서는 IsRead 속성이 **True**로 설정 된 메시지를 반환 합니다. 두 번째 예에서는 IsRead 속성이 **False**로 설정 된 메시지를 반환 합니다.|
|ItemClass|이 속성을 사용 하 여 조직에서 Office 365로 가져온 특정 타사 데이터 형식을 검색 합니다. 이 속성에는 다음 구문을 사용 합니다.`itemclass:ipm.externaldata.<third-party data type>*`|`itemclass:ipm.externaldata.Facebook* AND subject:contoso`  <br/> `itemclass:ipm.externaldata.Twitter* AND from:"Ann Beebe" AND "Northwind Traders"`|첫 번째 예에서는 Subject 속성에 "contoso" 라는 단어가 포함 된 Facebook 항목을 반환 합니다. 두 번째 예에서는 Ann Beebe에서 게시 되었으며 키워드 구 "Northwind Traders"를 포함 하는 Twitter 항목을 반환 합니다.  <br/> ItemClass 속성의 타사 데이터 형식에 사용할 값의 전체 목록은 [Office 365로 가져온 타사 데이터를 검색 하려면 사용 콘텐츠 검색](use-content-search-to-search-third-party-data-that-was-imported.md)을 참조 하십시오.|
|정도의| 검색할 전자 메일 메시지의 유형입니다. 사용 가능한 값:  <br/>  연락처만  <br/>  docs  <br/>  메일 주소  <br/>  externaldata  <br/>  못한  <br/>  메시징을  <br/>  저널이  <br/>  모임의  <br/>  microsoftteams (Microsoft 팀의 채팅, 모임 및 통화에서 항목을 반환 합니다.)  <br/>  notes  <br/>  게시물  <br/>  rssfeeds  <br/>  작업과  <br/>  음성 메일|`kind:email`  <br/> `kind:email OR kind:im OR kind:voicemail`  <br/> `kind:externaldata`|첫 번째 예에서는 검색 조건을 충족 하는 전자 메일 메시지를 반환 합니다. 두 번째 예에서는 전자 메일 메시지, 인스턴트 메시징 대화 (Microsoft 팀의 비즈니스용 Skype 대화 및 채팅 포함)를 반환 하 고, 검색 조건을 충족 하는 음성 메시지입니다. 세 번째 예에서는 검색 조건을 충족 하는 Twitter, Facebook 및 Cisco Jabber와 같은 타사 데이터 원본에서 Office 365의 사서함으로 가져온 항목을 반환 합니다. 자세한 내용은 [Office 365에서 타사 데이터 보관](https://go.microsoft.com/fwlink/p/?linkid=716918)을 참조 하세요.|
|할당|전자 메일 메시지의 모든 사용자 필드 이 필드는 From, To, CC 및 BCC입니다. <sup>1</sup>|`participants:garthf@contoso.com`  <br/> `participants:contoso.com`|garthf@contoso.com에서 보냈거나 이 사이트로 보낸 메시지입니다. 두 번째 예제에서는 contoso.com 도메인의 사용자가 보냈거나 이 사용자에게로 보낸 모든 메시지를 반환합니다.|
|Received|받는 사람이 전자 메일 메시지를 받은 날짜입니다.|`received:04/15/2016`  <br/> `received>=01/01/2016 AND received<=03/31/2016`|2016 년 4 월 15 일에 받은 메시지 두 번째 예에서는 2016 년 1 월 2 일과 2016 년 3 월 31 일 사이에 수신 된 모든 메시지를 반환 합니다.|
|받는 사람|전자 메일 메시지의 모든 받는 사람 필드, 이러한 필드는 받는 사람, 참조 및 숨은 참조입니다. <sup>1</sup>|`recipients:garthf@contoso.com`  <br/> `recipients:contoso.com`|garthf@contoso.com으로 보낸 메시지입니다. 두 번째 예제에서는 contoso.com 도메인에 있는 모든 받는 사람에게 전송된 메시지를 반환합니다.|
|전송할|보낸 사람이 전자 메일 메시지를 보낸 날짜입니다.|`sent:07/01/2016`  <br/> `sent>=06/01/2016 AND sent<=07/01/2016`|지정된 날짜 또는 지정된 날짜 범위 내에서 전송된 메시지입니다.|
|크기|항목의 크기(바이트)입니다.|`size>26214400`  <br/> `size:1..1048567`|25 보다 큰 메시지 정도의. 두 번째 예제에서는 1 ~ 1,048,567바이트(1MB) 크기의 메시지를 반환합니다.|
|제목|전자 메일 메시지 제목 줄의 텍스트입니다.  <br/> **참고:** 쿼리에서 Subject 속성을 사용 하면 ???the 검색에서 제목 줄에 검색 중인 텍스트가 포함 된 모든 메시지가 반환 됩니다. 즉, 쿼리는 정확 하 게 일치 하는 메시지만 반환 하지는 않습니다. 예를 들어를 검색 `subject:"Quarterly Financials"`하는 경우 결과에는 제목이 "분기별 Financials 2018" 인 메시지가 포함 됩니다.|`subject:"Quarterly Financials"`  <br/> `subject:northwind`|제목 줄의 텍스트에 "분기별 Financials" 이라는 구가 포함 된 메시지 두 번째 예제에서는 제목 줄에 단어 northwind가 포함된 모든 메시지를 반환합니다.|
|받는 사람|전자 메일 메시지의 대상 필드 <sup>1</sup>|`to:annb@contoso.com`  <br/> `to:annb ` <br/> `to:"Ann Beebe"`|모든 예제에서 받는 사람: 줄에 Ann Beebe가 지정된 메시지를 반환합니다.|
   
> [!NOTE]
> <sup>1</sup> recipient 속성 값의 경우 전자 메일 주소 ( *사용자 계정 이름이* 나 UPN이 라고도 함), 표시 이름 또는 별칭을 사용 하 여 사용자를 지정할 수 있습니다. 예를 들어 annb@contoso.com, annb 또는 "Ann Beebe"를 사용하여 사용자 Ann Beebe를 지정할 수 있습니다.<br/><br/>받는 사람 속성 (From, To, Cc, Bcc, 참가자 및 받는 사람)을 검색할 때 Office 365은 Azure Active Directory에서 각 사용자의 id를 확장 하려고 시도 합니다.  사용자가 Azure Active Directory에 있는 경우에는 쿼리가 사용자의 전자 메일 주소 (UPN), 별칭, 표시 이름 및 LegacyExchangeDN을 포함 하도록 확장 됩니다.<br/><br/>예를 들어를로 `participants:ronnie@contoso.com` 확장 하는 등 `participants:ronnie@contoso.com OR participants:ronnie OR participants:"Ronald Nelson" OR participants:"<LegacyExchangeDN>"`의 쿼리를 예로 들 수 있습니다.

## <a name="searchable-site-properties"></a>검색 가능한 사이트 속성

다음 표에는 보안 & 준수 센터의 콘텐츠 검색 기능을 사용 하거나 **ComplianceSearch** 또는 ComplianceSearch을 사용 하 여 검색할 수 있는 몇 가지 SharePoint 및 비즈니스용 OneDrive 속성이 나와 있습니다. ** **cmdlet 이 표에는 각 속성에 대 한 _속성의 값_ 구문과 예제에서 반환 된 검색 결과에 대 한 설명이 포함 되어 있습니다. 
  
검색할 수 있는 SharePoint 속성의 전체 목록을 보려면 [sharepoint에서 크롤링 및 관리 속성 개요](https://go.microsoft.com/fwlink/p/?LinkId=331599)를 참조 하세요. **쿼리** 가능 열에 **예** 로 표시 된 속성을 검색할 수 있습니다. 
  
|**속성**|**속성 설명**|**예제**|**예제에서 반환된 검색 결과**|
|:-----|:-----|:-----|:-----|
|만든 이|문서를 복사하는 경우 유지되는 Office 문서의 만든 이 필드입니다. 예를 들어 사용자가 문서를 만들고이를 다른 사람에 게 전자 메일로 업로드 한 경우이 문서는 원래 작성자를 계속 유지 합니다. 이 속성에는 사용자의 표시 이름을 사용 해야 합니다.|`author:"Garth Fort"`|Garth Fort가 만든 모든 문서입니다.|
|ContentType|항목, 문서, 비디오 등의 SharePoint 콘텐츠 형식입니다.|`contenttype:document`|모든 문서가 반환됩니다.|
|만든 날짜|항목을 만든 날짜입니다.|`created\>=06/01/2016`|2016 년 6 월 1 일 이후에 만들어진 모든 항목입니다.|
|CreatedBy|항목을 만들었거나 업로드한 사람입니다. 이 속성에는 사용자의 표시 이름을 사용 해야 합니다.|`createdby:"Garth Fort"`|Garth Fort가 만들었거나 업로드한 모든 항목입니다.|
|DetectedLanguage|항목의 언어입니다.|`detectedlanguage:english`|영어로된 모든 항목입니다.|
|DocumentLink|SharePoint 또는 비즈니스용 OneDrive 사이트에 있는 특정 폴더의 경로 (URL)입니다. 이 속성을 사용 하는 경우에는 지정한 폴더가 있는 사이트를 검색 해야 합니다.  <br/> Documentlink 속성에 대해 지정한 폴더의 하위 폴더에 있는 항목을 반환 하려면 지정 된 폴더의 URL을 추가\* /제거 해야 합니다. 예를 들어`documentlink: "https://contoso.sharepoint.com/Shared Documents/*"`  <br/> <br/>Documentlink 속성을 검색 하 고 스크립트를 사용 하 여 특정 사이트의 폴더에 대 한 documentlink Url을 가져오는 방법에 대 한 자세한 내용은 [Office 365의 대상 지정 컬렉션에 콘텐츠 검색 사용](use-content-search-for-targeted-collections.md)을 참조 하세요.|`documentlink:"https://contoso-my.sharepoint.com/personal/garthf_contoso_com/Documents/Private"`  <br/> `documentlink:"https://contoso-my.sharepoint.com/personal/garthf_contoso_com/Documents/Shared with Everyone/*" AND filename:confidential`|첫 번째 예에서는 지정 된 비즈니스용 OneDrive 폴더에 있는 모든 항목을 반환 합니다. 두 번째 예에서는 파일 이름에 "기밀" 이라는 단어가 포함 된 지정 된 사이트 폴더 및 모든 하위 폴더의 문서를 반환 합니다.|
|Fileextension)|파일의 확장명입니다. 예를 들면 .docx, one, .pptx 또는 .xlsx가 있습니다.|`fileextension:xlsx`|모든 Excel 파일 (Excel 2007 이상)|
|이름을|파일의 이름입니다.|`filename:"marketing plan"`  <br/> `filename:estimate`|첫 번째 예제에서는 제목에 "marketing plan"이 정확히 포함된 제목을 반환합니다. 두 번째 예제에서는 파일 이름에 "estimate"라는 단어가 들어 있는 파일을 반환합니다.|
|LastModifiedTime|항목을 마지막으로 변경한 날짜입니다.|`lastmodifiedtime>=05/01/2016`  <br/> `lastmodifiedtime>=05/10/2016 AND lastmodifiedtime<=06/1/2016`|첫 번째 예에서는 5 월 1 일, 2016 이후 변경 된 항목을 반환 합니다. 두 번째 예에서는 5 월 1 일, 2016 년 6 월 1 일 사이에 변경 된 항목 2016을 반환 합니다.|
|ModifiedBy|항목을 마지막으로 변경한 사람입니다. 이 속성에는 사용자의 표시 이름을 사용 해야 합니다.|`modifiedby:"Garth Fort"`|Garth Fort가 마지막으로 변경한 모든 항목입니다.|
|경로|SharePoint 또는 비즈니스용 OneDrive 사이트에 있는 특정 사이트의 경로 (URL)입니다.  <br/> Path 속성에 지정한 사이트의 폴더에 있는 항목을 반환 하려면 지정 된 사이트의 URL을 추가/\* 제거 해야 합니다. 예를 들어`path: "https://contoso.sharepoint.com/Shared Documents/*"`  <br/> <br/> **참고:** 이 `Path` 속성을 사용 하 여 OneDrive 위치를 검색 하면 검색 결과에 .png, tiff 또는 .wav 파일 같은 미디어 파일이 반환 되지 않습니다. 검색 쿼리에서 다른 사이트 속성을 사용 하 여 OneDrive 폴더에서 미디어 파일을 검색 합니다. <br/>|`path:"https://contoso-my.sharepoint.com/personal/garthf_contoso_com/"`  <br/> `path:"https://contoso-my.sharepoint.com/personal/garthf_contoso_com/*" AND filename:confidential`|첫 번째 예에서는 지정 된 비즈니스용 OneDrive 사이트의 모든 항목을 반환 합니다. 두 번째 예에서는 파일 이름에 "기밀" 이라는 단어가 포함 된 지정 된 사이트 (및 사이트의 폴더)의 문서를 반환 합니다.|
|SharedWithUsersOWSUser|지정 된 사용자와 공유 되었으며 사용자의 비즈니스용 OneDrive 사이트에 있는 **공유** 항목 페이지에 표시 되는 문서입니다. 조직의 다른 사용자가 지정 된 사용자와 명시적으로 공유 하는 문서입니다. SharedWithUsersOWSUser 속성을 사용 하는 검색 쿼리와 일치 하는 문서를 내보내면 지정한 사용자에 게 문서를 공유한 사용자의 원래 콘텐츠 위치에서 문서가 내보내집니다. 자세한 내용은 [조직 내에서 공유 되는 사이트 콘텐츠 검색](#searching-for-site-content-shared-within-your-organization)을 참조 하십시오.|`sharedwithusersowsuser:garthf`  <br/> `sharedwithusersowsuser:"garthf@contoso.com"`|두 예 모두 Garth 요새와 명시적으로 공유 된 모든 내부 문서를 반환 하며 Garth 요새의 비즈니스용 OneDrive 계정에 있는 **공유** 에 있는 페이지에 표시 됩니다.|
|사이트|조직의 사이트 또는 사이트 그룹의 URL입니다.|`site:"https://contoso-my.sharepoint.com"`  <br/> `site:"https://contoso.sharepoint.com/sites/teams"`|첫 번째 예에서는 조직 내 모든 사용자의 비즈니스용 OneDrive 사이트에서 항목을 반환 합니다. 두 번째 예제에서는 모든 팀 사이트의 항목을 반환합니다.|
|크기|항목의 크기(바이트)입니다.|`size>=1`  <br/> `size:1..10000`|첫 번째 예제에서는 1바이트 보다 큰 항목을 반환합니다. 두 번째 예제에서는 1부터 10,000바이트 크기의 항목을 반환합니다.|
|제목|문서의 제목입니다. Title 속성은 Microsoft Office 문서에 지정 된 메타 데이터입니다. 문서의 파일 이름과 다릅니다.|`title:"communication plan"`|Office 문서의 Title 메타데이터 속성에 "communication plan"이 포함된 문서입니다.|
   
## <a name="searchable-contact-properties"></a>검색 가능한 연락처 속성

다음 표에는 인덱싱되는 대화 상대 속성과 콘텐츠 검색을 사용 하 여 검색할 수 있는 연락처 속성이 나와 있습니다. 사용자 사서함의 개인 주소록에 있는 연락처 (개인 연락처 라고도 함)에 대해 사용자가 구성 하는 데 사용할 수 있는 속성입니다. 연락처를 검색 하려면 검색할 사서함을 선택한 다음 키워드 쿼리에서 하나 이상의 연락처 속성을 사용 하면 됩니다.
  
> [!TIP]
> 공백이 나 특수 문자를 포함 하는 값을 검색 하려면 큰따옴표 ("")를 사용 하 여 해당 구를 포함 합니다. 예를 `businessaddress:"123 Main Street"`들면입니다. 
  
|**속성**|**속성 설명**|
|:-----|:-----|
|BusinessAddress|**근무처 주소** 속성의 주소입니다. 이 속성은 연락처 속성 페이지의 **작업** 주소 라고도 합니다.|
|BusinessPhone|**회사 전화** 번호 속성의 전화 번호입니다.|
|CompanyName|**Company** 속성의 이름입니다.|
|부서|**부서** 속성의 이름입니다.|
|DisplayName|연락처의 표시 이름입니다. 연락처의 **전체 이름** 속성에 있는 이름입니다.|
|EmailAddress|연락처에 대 한 모든 전자 메일 주소 속성의 주소입니다. 사용자는 연락처에 대해 전자 메일 주소를 여러 개 추가할 수 있습니다. 이 속성을 사용 하면 연락처의 전자 메일 주소 중 하 나와 일치 하는 연락처가 반환 됩니다.|
|FileAs|**파일** 속성 이 속성은 연락처가 사용자의 대화 상대 목록에 나열 되는 방식을 지정 하는 데 사용 됩니다. 예를 들어 연락처를 *firstname, lastname* , *lastname, firstname* 으로 나열할 수 있습니다.|
|GivenName|**Name** 속성의 이름입니다.|
|HomeAddress|**집** 주소 속성의 주소입니다.|
|HomePhone|**집** 전화 번호 속성의 전화 번호입니다.|
|IMAddress|IM 주소 속성 (일반적으로 인스턴트 메시징에 사용 되는 전자 메일 주소)|
|MiddleName|**중간** 이름 속성의 이름입니다.|
|MobilePhone|**휴대폰** 번호 속성의 전화 번호입니다.|
|애칭|**애칭** 속성의 이름입니다.|
|OfficeLocation|**Office** 또는 **office location** 속성의 값입니다.|
|OtherAddress|**기타** address 속성의 값입니다.|
|성|**Last** name 속성의 이름입니다.|
|제목|직위 속성의 제목 **** 입니다.|
   

## <a name="searchable-sensitive-data-types"></a>검색 가능한 중요한 데이터 형식

보안 및 준수 센터의 콘텐츠 검색 기능을 사용 하 여 SharePoint의 문서 및 비즈니스용 OneDrive 사이트에 저장 되어 있는 중요 한 데이터 (예: 신용 카드 번호 또는 사회 보장 번호)를 검색할 수 있습니다. 이 작업은 키워드 쿼리에 중요 한 `SensitiveType` 정보 유형의 속성 및 이름을 사용 하 여 수행할 수 있습니다. 예를 들어 쿼리 `SensitiveType:"Credit Card Number"` 는 신용 카드 번호가 포함 된 문서를 반환 합니다. 이 쿼리 `SensitiveType:"U.S. Social Security Number (SSN)"` 는 미국 사회 보장 번호가 포함 된 문서를 반환 합니다. 검색할 수 있는 중요 한 데이터 형식 목록을 보려면 Security & 준수 센터에서 **중요 한 정보 유형** **분류** \> 로 이동 하십시오. 또는 Security & 준수 센터 PowerShell에서 **DlpSensitiveInformationType** cmdlet을 사용 하 여 중요 한 정보 유형 목록을 표시할 수 있습니다. 
  
또한이 `SensitiveType` 속성을 사용 하 여 조직에 대해 자신이 만들었거나 다른 관리자가 만든 사용자 지정 중요 한 정보 유형의 이름을 검색할 수 있습니다. 기본 제공 및 사용자 지정 중요 한 정보를 구별 하기 위해 Security & 준수 센터의 **중요 한 정보 유형** 페이지 (또는 PowerShell의 **publisher** 속성)에서 **게시자** 열을 사용할 수 있습니다. 유형을. 자세한 내용은 [사용자 지정 중요 한 정보 유형 만들기](create-a-custom-sensitive-information-type.md)를 참조 하십시오.
  
이 `SensitiveType` 속성을 사용 하 여 쿼리를 만드는 방법에 대 한 자세한 내용은 [Form a query to a sites에 저장 된 중요 한 데이터 찾기를](form-a-query-to-find-sensitive-data-stored-on-sites.md)참조 하십시오.

> [!NOTE]
> 중요 한 데이터 형식과 search 속성을 사용 `SensitiveType` 하 여 Exchange Online 사서함에 있는 중요 한 데이터를 검색할 수는 없습니다. 그러나 DLP (데이터 손실 방지) 정책을 사용 하 여 전송 중인 중요 한 emaill 데이터를 보호할 수 있습니다. 자세한 내용은 [데이터 손실 방지 정책 개요](data-loss-prevention-policies.md) 및 [개인 데이터 검색 및 찾기를](search-for-and-find-personal-data.md)참조 하세요.
  
## <a name="search-operators"></a>검색 연산자

**And**, **OR**등의 부울 검색 연산자는 검색 쿼리에 **** 특정 단어를 포함 하거나 제외 하 여 보다 정확한 검색을 정의 하는 데 도움이 됩니다. 다른 기술 (예: \>= 또는 ...), 따옴표, 괄호, 와일드 카드 등의 기타 기법을 사용 하면 검색 쿼리를 보다 구체화할 수 있습니다. 다음 표에서는 검색 결과를 좁히거나 넓히는 데 사용할 수 있는 연산자를 설명합니다. 
  
|**연산자**|**Usage**|**설명**|
|:-----|:-----|:-----|
|한|keyword1 AND keyword2|지정한 키워드나 `property:value` 식이 모두 포함 된 항목을 반환 합니다. 예를 들어 `from:"Ann Beebe" AND subject:northwind` 제목 줄에 northwind 라는 단어를 포함 하는 Ann Beebe에서 보낸 모든 메시지를 반환 합니다. <sup>2</sup>|
|+|keyword1 + keyword2 + keyword3|`keyword3` ** `keyword1` ** 또는가 포함 된 항목을 반환 합니다.`keyword2`   따라서이 예제는 쿼리와 `(keyword2 OR keyword3) AND keyword1`동일 합니다.  <br/> 기호 뒤에 공백이 `keyword1 + keyword2` 있는 쿼리는 * * 및 * * 연산자를 사용 하는 것과는 다릅니다. **+** 이 쿼리는 해당 하는 `"keyword1 + keyword2"` 것과 동일한 작업을 포함 하 `"keyword1 + keyword2"`는 항목을 반환 합니다.|
|또는|keyword1 OR keyword2|지정 된 키워드나 `property:value` 식이 하나 이상 포함 된 항목을 반환 합니다. <sup>2</sup>|
|아닌|keyword1 NOT keyword2  <br/> NOT from:"Ann Beebe"  <br/> 종류 아님: im|키워드나 `property:value` 식으로 지정한 항목을 제외 합니다. 두 번째 예에서는 Ann Beebe에서 보낸 메시지를 제외 합니다. 세 번째 예에서는 대화 내용 사서함 폴더에 저장 된 비즈니스용 Skype 대화와 같은 인스턴트 메시징 대화를 제외 합니다. <sup>2</sup>|
|-|keyword1 -keyword2|**NOT** 연산자와 같습니다. 따라서이 쿼리는를 포함 하 `keyword1` 는 항목을 반환 하며 해당 `keyword2`항목이 포함 된 항목을 제외 합니다.|
|위치|keyword1 NEAR(n) keyword2|서로 인접 한 단어를 포함 하는 항목을 반환 합니다 (여기에서 n은 단어의 개수와 같습니다. 예를 들어 `best NEAR(5) worst` "최악" 라는 단어가 단어 5 개에서 "최상" 사이에 있는 항목을 모두 반환 합니다. 숫자를 지정하지 않으면 기본 거리는 8단어입니다. <sup>2</sup>|
|ONEAR|keyword1 ONEAR(n) keyword2|**Near**과 유사 하지만 지정 된 순서로 서로 근접 한 단어를 포함 하는 항목을 반환 합니다. 예를 들어 `best ONEAR(5) worst` "최상" 이라는 단어가 "최악의" 단어 보다 앞에 있고 두 단어는 서로 다섯 단어 내에 있는 항목을 모두 반환 합니다. 숫자를 지정하지 않으면 기본 거리는 8단어입니다. <sup>2</sup> <br/> > [!NOTE]>에서는 사서함을 검색할 때 **Onear** 연산자를 지원 하지 않습니다. SharePoint 및 비즈니스용 OneDrive 사이트를 검색 하는 경우에만 작동 합니다. 같은 검색에서 사서함 및 사이트를 검색 하는 경우 쿼리에 **Onear** 연산자가 포함 되어 있는 경우에는 **NEAR** 연산자를 사용 하는 것 처럼 검색에서 사서함 항목을 반환 합니다. 즉, 검색 기능은 단어가 나타나는 순서에 관계 없이 지정 된 단어가 서로 가까이 있는 항목을 반환 합니다.|
|:|속성: 값|콜론 (:) `property:value` 구문에서 검색 되는 속성의 값에 지정 된 값이 포함 되도록 지정 합니다. 예를 들어 `recipients:garthf@contoso.com` garthf@contoso.com로 전송 된 모든 메시지를 반환 합니다.|
|=|속성 = 값|**:** 연산자와 같습니다.|
|\<|속성\<값|검색 중인 속성이 지정된 값보다 작음을 나타냅니다.  <sup>개</sup>|
|\>|속성\>값|검색 중인 속성이 지정 된 값 보다 크다는 것을 나타냅니다. <sup>1</sup>|
|\<=|속성\<= 값|검색 중인 속성이 특정 값 보다 작거나 같음을 나타냅니다. <sup>1</sup>|
|\>=|속성\>= 값|검색 중인 속성이 특정 값 보다 크거나 같음을 나타냅니다. <sup>1</sup>|
|..|속성: value1.. value2|검색 중인 속성을 value1 보다 크거나 같고 value2 보다 작거나 같게 나타냅니다. <sup>1</sup>|
|"  "|"fair value"  <br/> subject:"Quarterly Financials"|키워드 및 `property:value` 검색 쿼리에서 정확한 어구 또는 용어를 검색 하려면 큰따옴표 ("")를 사용 합니다.|
|\*|cat\*  <br/> 제목: 설정\*|접두사 와일드 카드 검색 (단어 끝에 별표가 있는 위치)은 키워드나 `property:value` 쿼리에서 0 개 이상의 문자와 일치 합니다. 예를 들어 `title:set*` 문서 제목에는 word 설정, 설정 및 설정 (및 "set"으로 시작 하는 기타 단어)이 포함 된 문서를 반환 합니다.  <br/><br/> **참고:** 접두사 와일드 카드 검색만 사용할 수 있습니다. 예를 들면 **cat\* ** 또는 **set\*** 입니다. ** \*Cat** (접미사 검색), 중 위 검색 **(\*c t** ) 및 ** \*cat\* ** (하위 문자열 검색)은 지원 되지 않습니다.|
|(  )| (fair OR free) AND (from:contoso.com)  <br/>  (IPO OR initial) AND (stock OR shares)  <br/>  (quarterly financials)|괄호는 부울 구, `property:value` 항목 및 키워드를 함께 그룹화 합니다. 예를 들어 `(quarterly financials)` 분기 및 financials 이라는 단어가 포함 된 항목을 반환 합니다.|
   
> [!NOTE]
> <sup>1</sup> 날짜 또는 숫자 값이 있는 속성에는이 연산자를 사용 합니다.<br/> <sup>2</sup> 부울 검색 연산자는 대문자 여야 합니다. 예를 들면 **AND**입니다. **And**와 같은 소문자 연산자를 사용 하는 경우 검색 쿼리에서 키워드로 취급 됩니다. 
  
## <a name="search-conditions"></a>검색 조건

검색 쿼리에 조건을 추가 하 여 검색 범위를 좁히고 보다 구체화 된 결과 집합을 반환할 수 있습니다. 각 조건은 검색을 시작할 때 생성 및 실행되는 KQL 검색 쿼리에 절을 추가합니다.
  
[공용 속성에 대한 조건 ](#conditions-for-common-properties)

[메일 속성에 대한 조건](#conditions-for-mail-properties)

[문서 속성에 대한 조건](#conditions-for-document-properties)

[조건과 함께 사용되는 연산자](#operators-used-with-conditions)

[조건 사용에 대한 지침](#guidelines-for-using-conditions)

[예제](#examples-of-using-conditions-in-search-queries)
  
### <a name="conditions-for-common-properties"></a>공용 속성에 대한 조건

동일한 검색에서 사서함 및 사이트를 검색할 때 공용 속성을 사용하는 조건을 만듭니다. 다음 표에는 조건을 추가할 때 사용할 수 있는 속성이 나와 있습니다.
  
|**조건**|**설명**|
|:-----|:-----|
|날짜|전자 메일 메시지의 경우 받는 사람이 메시지를 받았거나 보낸 사람이 메시지를 보낸 날짜입니다. 문서의 경우 문서를 마지막으로 수정한 날짜입니다.|
|보낸 사람/만든이|전자 메일의 경우 메시지를 보낸 사람입니다. 문서의 경우 Office 문서의 만든 이 필드에 지정된 사람입니다. 여러 개의 이름을 쉼표로 구분하여 입력할 수 있습니다. 두 개 이상의 값은 **OR** 연산자를 사용하여 논리적으로 연결됩니다.|
|크기 (바이트)|전자 메일 및 문서의 경우 항목의 크기(바이트)입니다.|
|제목/제목|전자 메일의 경우 메시지 제목 줄의 텍스트입니다. 문서의 경우 문서 제목입니다. 앞에서 설명한 것 처럼 Title 속성은 Microsoft Office 문서에 지정 된 메타 데이터입니다. 두 개 이상의 제목/제목 이름을 쉼표로 구분 하 여 입력할 수 있습니다. 두 개 이상의 값은 **OR** 연산자를 사용하여 논리적으로 연결됩니다.|
|준수 태그|전자 메일 및 문서에 대해 사용자가 수동으로 할당 한 레이블 정책이 나 레이블에서 자동으로 메시지와 문서에 할당 된 레이블입니다. 레이블은 데이터 거 버 넌 스와 전자 메일 및 문서를 분류 하 고 레이블에 의해 정의 된 분류에 따라 보존 규칙을 적용 하는 데 사용 됩니다. 레이블 이름의 일부를 입력 하 고 와일드 카드를 사용 하거나 전체 레이블 이름을 입력할 수 있습니다. 자세한 내용은 [Office 365의 레이블 개요](labels.md)를 참조 하세요.|
  
### <a name="conditions-for-mail-properties"></a>메일 속성에 대한 조건

사서함 또는 공용 폴더를 검색할 때 메일 속성을 사용하여 조건을 만듭니다. 다음 표에서 조건을 사용할 수 있는 전자 메일 속성을 나열 합니다. 이러한 속성은 이전에 제공한 전자 메일 속성에 대한 설명과 일부 중복되며 편의를 위해 반복해서 제공됩니다.
  
|**조건**|**설명**|
|:-----|:-----|
|메시지 종류| 검색할 메시지의 유형입니다. Kind 전자 메일 속성과 같은 속성입니다. 사용 가능한 값:  <br/><br/>  연락처만  <br/>  docs  <br/>  메일 주소  <br/>  externaldata  <br/>  못한  <br/>  메시징을  <br/>  저널이  <br/>  모임의  <br/>  microsoftteams  <br/>  notes  <br/>  게시물  <br/>  rssfeeds  <br/>  작업과  <br/>  음성 메일|
|할당|전자 메일 메시지의 모든 사용자 필드로, 보낸 사람, 받는 사람, 참조 및 숨은 참조가 여기에 해당됩니다.|
|유형|전자 메일 항목에 대 한 메시지 클래스 속성 이 속성은 ItemClass email 속성과 동일 합니다. 또한 다중 값 조건 이기도 합니다. 따라서 여러 메시지 클래스를 선택 하려면 **CTRL** 키를 누른 상태에서 조건에 추가할 드롭다운 목록에서 메시지 클래스를 두 개 이상 클릭 합니다. 목록에서 선택한 각 메시지 클래스는 해당 검색 쿼리의 **OR** 연산자로 논리적으로 연결 됩니다.  <br/> Exchange에서 사용 되며 **메시지 클래스** 목록에서 선택할 수 있는 메시지 클래스와 해당 메시지 클래스 ID의 목록은 [항목 형식 및 메시지 클래스](https://go.microsoft.com/fwlink/?linkid=848143)를 참조 하십시오.|
|Received|받는 사람이 전자 메일 메시지를 받은 날짜입니다. Received 전자 메일 속성과 같은 속성입니다.|
|받는 사람|전자 메일 메시지를 보낸 사람입니다. To 전자 메일 속성과 같은 속성입니다.|
|보낸 사람|전자 메일 메시지의 보낸 사람입니다.|
|전송할|보낸 사람이 전자 메일 메시지를 보낸 날짜입니다. Sent 전자 메일 속성과 같은 속성입니다.|
|제목|전자 메일 메시지 제목 줄의 텍스트입니다.|
|받는 사람|전자 메일 메시지의 받는 사람입니다.|
  
### <a name="conditions-for-document-properties"></a>문서 속성에 대한 조건

SharePoint 및 비즈니스용 OneDrive 사이트에서 문서를 검색할 때 문서 속성을 사용 하 여 조건을 만듭니다. 다음 표에서는 조건에 사용할 수 있는 문서 속성 목록을 제공합니다. 이러한 속성은 이전에 제공한 사이트 속성에 대한 설명과 일부 중복되며 편의를 위해 반복해서 제공됩니다.
  
|**조건**|**설명**|
|:-----|:-----|
|만든 이|문서를 복사하는 경우 유지되는 Office 문서의 만든 이 필드입니다. 예를 들어 사용자가 문서를 만들고이를 다른 사람에 게 전자 메일로 업로드 한 경우이 문서는 원래 작성자를 계속 유지 합니다.|
|제목|문서의 제목입니다. Title 속성은 Office 문서에 지정된 메타데이터입니다. 문서의 파일 이름과는 다릅니다.|
|만든 날짜|문서를 만든 날짜입니다.|
|마지막으로 수정한 날짜|문서를 마지막으로 변경한 날짜입니다.|
|파일 형식|파일의 확장명입니다. 예를 들면 .docx, one, .pptx 또는 .xlsx가 있습니다. FileExtension 사이트 속성과 같은 속성입니다.|
  
### <a name="operators-used-with-conditions"></a>조건과 함께 사용되는 연산자

조건을 추가할 때 조건에 대한 속성 유형과 관련된 연산자를 선택할 수 있습니다. 다음 표에서는 조건과 함께 사용되는 연산자를 설명하고 검색 쿼리에 사용되는 것과 동일한 연산자를 제공합니다.
  
|**연산자**|**연산자와 동일한 쿼리**|**설명**|
|:-----|:-----|:-----|
|마치면|`property>date`|날짜 조건과 함께 사용됩니다. 지정된 날짜 이후에 전송, 수신 또는 수정된 항목을 반환합니다. |
|Before|`property<date`|날짜 조건과 함께 사용됩니다. 지정된 날짜 이전에 전송, 수신 또는 수정된 항목을 반환합니다.|
|간의|`date..date`|날짜 및 크기 조건과 함께 사용됩니다. 날짜 조건과 함께 사용될 경우 지정된 날짜 범위 내에서 전송, 수신 또는 수정된 항목을 반환합니다. 크기 조건과 함께 사용될 경우 해당 크기가 지정된 범위 내에 속하는 항목을 반환합니다.|
|Contains any of|`(property:value) OR (property:value)`|문자열 값을 지정하는 속성에 대한 조건과 함께 사용됩니다. 하나 이상의 지정된 문자열 값의 일부를 포함하는 항목을 반환합니다.|
|Doesn't contain any of|`-property:value`  <br/> `NOT property:value`|문자열 값을 지정하는 속성에 대한 조건과 함께 사용됩니다. 지정된 문자열 값의 어떤 부분도 포함하지 않는 항목을 반환합니다.|
|Doesn't equal any of|`-property=value`  <br/> `NOT property=value`|문자열 값을 지정하는 속성에 대한 조건과 함께 사용됩니다. 특정 문자열을 포함하지 않는 항목을 반환합니다.|
|내년|`size=value`|지정 된 크기와 같은 항목을 반환 합니다. <sup>1</sup>|
|Equals any of|`(property=value) OR (property=value)`|문자열 값을 지정하는 속성에 대한 조건과 함께 사용됩니다. 하나 이상의 지정된 문자열 값과 정확히 일치하는 항목을 반환합니다.|
|넘을|`size>value`|지정한 속성이 지정한 값 보다 큰 항목을 반환 합니다. <sup>1</sup>|
|Greater or equal|`size>=value`|지정한 속성이 지정한 값 보다 크거나 같은 항목을 반환 합니다. <sup>1</sup>|
|줄일|`size<value`|특정 값 보다 크거나 같은 항목을 반환 합니다. <sup>1</sup>|
|Less or equal|`size<=value`|특정 값 보다 크거나 같은 항목을 반환 합니다. <sup>1</sup>|
|Not equal|`size<>value`|지정 된 크기와 다른 항목을 반환 합니다. <sup>1</sup>|
   
> [!NOTE]
> <sup>1</sup> 이 연산자는 Size 속성을 사용 하는 조건에만 사용할 수 있습니다. 
  
### <a name="guidelines-for-using-conditions"></a>조건 사용에 대한 지침

검색 조건을 사용할 때 다음에 유의하세요.
  
- 조건은 **AND** 연산자를 사용하여 키워드 쿼리(키워드 상자에 지정)에 논리적으로 연결됩니다. 즉, 결과에 포함되려면 항목이 키워드 쿼리와 조건을 모두 만족해야 합니다. 조건은 이런 방식으로 결과 범위를 좁히는 데 도움이 됩니다. 
    
- 검색 쿼리에 두 개 이상의 고유한 조건을 추가 하면 (서로 다른 속성을 지정 하는 조건) 이러한 조건은 **and** 연산자로 논리적으로 연결 됩니다. 즉, 모든 조건(및 키워드 쿼리)을 만족하는 항목만 반환됩니다. 
    
- 동일한 속성에 대해 둘 이상의 조건을 추가하면 해당 조건은 **OR** 연산자에 의해 논리적으로 연결됩니다. 즉, 키워드 쿼리와 조건 중 하나를 만족하는 항목이 반환됩니다. 따라서 동일한 조건 그룹이 **OR** 연산자에 의해 서로 연결된 후 고유한 조건 집합이 **AND** 연산자로 연결됩니다. 
    
- 단일 조건에 쉼표나 세미콜론으로 구분 된 값을 여러 개 추가 하는 경우 이러한 값은 **or** 연산자에 의해 연결 됩니다. 즉, 조건의 속성에 대해 지정된 값을 하나라도 포함하는 항목이 반환됩니다. 
    
- 키워드 상자와 조건을 사용 하 여 만든 검색 쿼리는 **검색** 페이지의 선택한 검색에 대 한 세부 정보 창에 표시 됩니다. 쿼리에서 노테이션 `(c:c)` 오른쪽에 있는 모든 항목은 쿼리에 추가 되는 조건을 나타냅니다. 
    
- 조건은 검색 쿼리에 속성만 추가하고 연산자는 추가하지 않습니다. 이 때문에 세부 정보 창에 표시 되는 쿼리에는 `(c:c)` 노테이션 오른쪽의 연산자가 표시 되지 않습니다. KQL은 쿼리를 실행할 때 논리 연산자를 추가합니다(이전에 설명한 규칙을 따름). 
    
- 끌어서 놓기 컨트롤을 사용하여 조건의 순서를 다시 지정할 수 있습니다. 조건에 대한 컨트롤을 클릭한 후 위 또는 아래로 이동합니다.
    
- 앞에서 설명한 것 처럼 일부 조건 속성을 사용 하 여 여러 값을 입력할 수 있습니다. 각 값은 **OR** 연산자에 의해 논리적으로 연결 됩니다. 이렇게 하면 동일한 조건의 인스턴스가 여러 개 있는 것과 같은 논리가 생성 되며 각 인스턴스에는 단일 값이 있습니다. 다음 그림에서는 값이 여러 개인 단일 조건과 동일한 속성에 대 한 여러 조건의 예가 단일 값을 갖는 예를 보여 줍니다. 두 예 모두 같은 쿼리를 실행 합니다.`(filetype="docx") OR (filetype="pptx") OR (filetype="xlsx")`
    
    ![메시지는 규칙의 모든 조건과 일치해야 합니다. 하나의 조건 또는 다른 조건과 일치해야 하는 경우 각 조건에 대해 별도의 규칙을 사용합니다. 예를 들어 패턴과 일치하는 콘텐츠가 있는 메시지 및 첨부 파일이 있는 메시지에 동일한 고지 사항을 추가하려면 각 조건에 대해 하나의 규칙을 만듭니다. 규칙은 쉽게 복사할 수 있습니다.](media/9880aa29-d117-4531-be20-6d53f1d21341.gif)
  
    ![동일한 속성에 대한 여러 검색 조건](media/1e63d37d-6d8d-4c9b-a509-a7e1c3a05193.gif)
  
> [!TIP]
> 조건이 여러 값을 허용하는 경우 단일 조건을 사용하고 여러 값(쉼표나 세미콜론으로 구분)을 지정하는 것이 좋습니다. 이렇게 하면 적용되는 쿼리 논리가 사용자의 의도와 맞는지 확인하는 데 도움이 됩니다. 
  
### <a name="examples-of-using-conditions-in-search-queries"></a>예제

다음 예제에서는 조건이 포함 된 검색 쿼리의 GUI 기반 버전, 선택한 검색의 세부 정보 창에 표시 되는 검색 쿼리 구문 ( **ComplianceSearch** cmdlet에 의해서도 반환 됨) 및 해당 논리를 보여 줍니다. 해당 KQL 쿼리 
  
#### <a name="example-1"></a>예 1

이 예에서는 신용 카드 번호를 포함 하 고 마지막으로 수정 된 SharePoint 및 비즈니스용 OneDrive 사이트의 문서를 반환 합니다 (2016).
  
 **GUI**
  
![검색 조건 첫 번째 예제](media/099515ba-d4ee-474e-af25-3aa48816b87b.gif)
  
 **검색 쿼리 구문**
  
 `SensitiveType:"Credit Card Number(c:c)(lastmodifiedtime<2016-01-01)`
  
 **검색 쿼리 논리**
  
 `SensitiveType:"Credit Card Number" AND (lastmodifiedtime<2016-01-01)`
  
#### <a name="example-2"></a>예제 2

이 예제에서는 키워드 "report"를 포함하고, 2015년 4월 1일 이전에 전송되었거나 생성되었고, 전자 메일 메시지의 제목 필드나 문서의 제목 속성에 단어 "northwind"가 포함된 전자 메일 항목 또는 문서를 반환합니다. 이 쿼리는 다른 검색 조건에 맞는 웹 페이지를 제외합니다. 
  
 **GUI**
  
![검색 조건 두 번째 예제](media/fe07d495-df81-42da-8106-3cdb409c6e7f.gif)
  
 **검색 쿼리 구문**
  
 `report(c:c)(date<2016-04-01)(subjecttitle:"northwind")(-filetype="aspx")`
  
 **검색 쿼리 논리**
  
 `report AND (date<2016-04-01) AND (subjecttitle:"northwind") NOT (filetype="aspx")`
  
#### <a name="example-3"></a>예 3
<a name="conditionexamples"> </a>

이 예에서는 12/1/2016와 11/30/2016 사이에 전송 되 고 "전화" 또는 "smartphone"으로 시작 하는 단어가 포함 된 전자 메일 메시지 또는 일정 모임이 반환 됩니다.
  
 **GUI**
  
![검색 조건 두 번째 예제](media/973d45fc-0923-43d6-9d0a-25e4a625f057.gif)
  
 **검색 쿼리 구문**
  
 `phone* OR smartphone*(c:c)(sent=2016-12-01..2016-11-30)(kind="email")(kind="meetings")`
  
 **검색 쿼리 논리**
  
 `phone* OR smartphone* AND (sent=2016-12-01..2016-11-30) AND ((kind="email") OR (kind="meetings"))`
  
## <a name="searching-for-site-content-shared-with-external-users"></a>외부 사용자와 공유되는 사이트 콘텐츠 검색

또한 Security & 준수 센터의 콘텐츠 검색 기능을 사용 하 여 SharePoint에 저장 된 문서와 조직 외부의 사용자와 공유 된 비즈니스용 OneDrive 사이트를 검색할 수 있습니다. 이렇게 하면 조직 외부에서 공유되는 중요한 정보나 비공개 정보를 확인할 수 있습니다. 키워드 쿼리에 속성을 `ViewableByExternalUsers` 사용 하 여이 작업을 수행할 수 있습니다. 이 속성은 다음 공유 방법 중 하나를 사용 하 여 외부 사용자와 공유 된 문서 또는 사이트를 반환 합니다. 
  
- 사용자가 인증 된 사용자로 조직에 로그인 하는 데 필요한 공유 초대입니다.
    
- 익명 게스트 링크-이 링크를 가진 누구 든 지 인증 하지 않고도 리소스에 액세스할 수 있습니다.
    
그 예는 다음과 같습니다.
  
- 이 쿼리 `ViewableByExternalUsers:true AND SensitiveType:"Credit Card Number"` 는 조직 외부의 사용자와 공유 되었으며 신용 카드 번호를 포함 하는 모든 항목을 반환 합니다. 
    
- 이 쿼리 `ViewableByExternalUsers:true AND ContentType:document AND site:"https://contoso.sharepoint.com/Sites/Teams"` 는 외부 사용자와 공유 된 조직의 모든 팀 사이트에 있는 문서 목록을 반환 합니다. 
    
> [!TIP]
> 과 `ViewableByExternalUsers:true AND ContentType:document` 같은 검색 쿼리는 검색 결과에 많은 .aspx 파일을 반환할 수 있습니다. 이러한 파일 형식 또는 다른 형식을 제거 하려면이 `FileExtension` 속성을 사용 하 여 특정 파일 형식을 제외할 수 있습니다. 예를 `ViewableByExternalUsers:true AND ContentType:document NOT FileExtension:aspx`들어 
  
조직 외부의 사용자와 공유되는 것으로 간주되는 콘텐츠는 무엇인가요? 공유 초대를 보내거나 공공 장소에서 공유 되는, 조직의 SharePoint 및 비즈니스용 OneDrive 사이트의 문서 예를 들어 다음과 같은 사용자 활동은 외부 사용자가 콘텐츠를 볼 수 있도록 만듭니다.
  
- 사용자가 조직 외부의 사람과 파일 또는 폴더를 공유합니다.
    
- 사용자가 공유 파일을 만든 후 조직 외부의 사람에게 공유 파일에 대한 링크를 보냅니다. 이 링크를 사용하여 외부 사용자를 파일을 보거나 편집할 수 있습니다.
    
- 사용자가 조직 외부의 사람에게 공유 파일을 보거나 편집할 수 있는 공유 초대 메일 또는 게스트 링크를 보냅니다.
    
### <a name="issues-using-the-viewablebyexternalusers-property"></a>ViewableByExternalUsers 속성을 사용 하는 문제

이 속성 `ViewableByExternalUsers` 은 문서 또는 사이트를 외부 사용자와 공유 하는 상태를 나타내는 반면에이 속성이 어떤 작업을 수행 하 고 반영 하지 않을 지를 몇 가지 주의 해야 합니다. 다음 시나리오에서는 `ViewableByExternalUsers` 속성 값이 업데이트 되지 않으며,이 속성을 사용 하는 콘텐츠 검색 쿼리 결과가 정확 하지 않을 수 있습니다. 
  
- 사이트 또는 조직에 대 한 외부 공유 해제와 같은 공유 정책 변경 이 속성은 외부 액세스가 해지 된 경우에도 이전에 액세스할 수 있는 것으로 이전의 공유 문서를 표시 합니다.
    
- 외부 사용자를 Office 365 그룹 또는 Office 365 보안 그룹에 추가 하거나 제거 하는 등 그룹 구성원에 대 한 변경 내용 이 속성은 그룹이 액세스 하는 항목에 대해서는 자동으로 업데이트 되지 않습니다.
    
- 받는 사람이 초대를 수락 하지 않아 해당 콘텐츠에 대 한 액세스 권한이 없는 외부 사용자에 게 공유 초대를 보냅니다.
    
이러한 시나리오에서는 사이트 또는 `ViewableByExternalUsers` 문서 라이브러리를 다시 크롤링 하 고 다시 인덱싱할 때까지 속성에 현재 공유 상태를 반영 하지 않습니다. 

## <a name="searching-for-site-content-shared-within-your-organization"></a>조직 내에서 공유 되는 사이트 콘텐츠 검색

앞에서 설명한 것 처럼,이 `SharedWithUsersOWSUser` 속성을 사용 하 여 조직 내 사용자 간에 공유 된 문서를 검색할 수 있습니다. 사용자가 조직 내부의 다른 사용자와 파일 (또는 폴더)을 공유 하는 경우 공유 파일에 대 한 링크가 파일을 공유 하는 사용자의 비즈니스용 OneDrive 계정에 있는 **내가 공유한** 항목 페이지에 표시 됩니다. 예를 들어 Sara Davis와 공유 된 문서를 검색 하려면 쿼리 `SharedWithUsersOWSUser:"sarad@contoso.com"`를 사용할 수 있습니다. 이 검색의 결과를 내보낼 경우 Sara를 사용 하 여 문서를 공유한 사용자의 콘텐츠 위치에 있는 원본 문서가 다운로드 됩니다.
  
이 `SharedWithUsersOWSUser` 속성을 사용 하는 경우 검색 결과에 반환 되는 특정 사용자와 문서를 명시적으로 공유 해야 합니다. 예를 들어 사용자가 OneDrive 계정에서 문서를 공유 하는 경우에는 다른 사용자 (조직 내부 또는 외부)와 공유 하는 옵션을 사용 하 여 조직 내 사용자와 공유 하거나 특정 사람과 공유할 수 있습니다. 다음은 세 가지 공유 옵션을 보여 주는 OneDrive의 **공유** 창에 대 한 스크린샷입니다. 
  
![특정 사용자와 공유 하는 파일만 SharedWithUsersOWSUser 속성을 사용 하는 검색 쿼리에서 반환 됩니다.](media/469a4b61-68bd-4ab0-b612-ab6302973886.png)
  
세 번째 옵션 ( **특정 사용자**와 공유)을 사용 하 여 공유 하는 문서만 해당 `SharedWithUsersOWSUser` 속성을 사용 하는 검색 쿼리에 의해 반환 됩니다. 

## <a name="searching-for-skype-for-business-conversations"></a>비즈니스용 Skype 대화 검색

다음 키워드 쿼리를 사용 하 여 비즈니스용 Skype 대화에서 콘텐츠를 구체적으로 검색할 수 있습니다.

```
kind:im
```

참고 이전 검색 쿼리는 Microsoft 팀에서 채팅을 반환 하기도 합니다. 이를 방지 하려면 다음 키워드 쿼리를 사용 하 여 비즈니스용 Skype 대화만 포함 되도록 검색 결과 범위를 좁힐 수 있습니다.

```
kind:im AND subject:conversation
```

비즈니스용 Skype 대화가 "대화" 라는 단어로 시작 하는 제목 줄이 있는 전자 메일 메시지로 저장 되므로 이전 키워드 쿼리는 Microsoft 팀의 채팅을 제외 합니다.

특정 날짜 범위 내에서 발생 한 비즈니스용 Skype 대화를 검색 하려면 다음 키워드 쿼리를 사용 합니다.

```
kind:im AND subject:conversation AND (received=startdate..enddate)
```

## <a name="search-tips-and-tricks"></a>검색 팁과 트릭

- 키워드 검색은 대/소문자를 구분하지 않습니다. 예를 들어 **cat** 및 **CAT**은 같은 결과를 반환합니다.  
    
- 부울 연산자 **AND**, **OR**, **NOT**, **NEAR**및 **onear** 는 대문자 여야 합니다. 
    
- 두 개의 키워드나 두 `property:value` 식 사이의 공백은 **AND**를 사용 하는 것과 같습니다. 예를 `from:"Sara Davis" subject:reorganization` 들어 Sara Davis에서 보낸 모든 메시지를 제목 줄에 다시 그룹화 하 여 반환 합니다. 
    
- `property:value` 형식과 일치 하는 구문을 사용 합니다. 값은 대/소문자를 구분 하지 않으며 연산자 뒤에 공백을 사용할 수 없습니다. 공백이 있는 경우 전체 텍스트 검색을 수행해야만 원하는 값이 검색됩니다. 예를 `to: pilarp` 들어 pilarp로 전송 된 메시지 대신 키워드로 "pilarp"을 검색 합니다. 
    
- 받는 사람 속성(예: To, From, Cc 또는 Recipients)을 검색하는 경우 SMTP 주소, 별칭 또는 표시 이름을 사용하여 받는 사람을 나타낼 수 있습니다. 예를 들어, pilarp@contoso.com, pilarp, 또는 "Pilar Pinilla"를 사용할 수 있습니다.
    
- 접두사 와일드 카드 검색만 사용할 수 있습니다. 예를 들면 **cat\* ** 또는 **set\*** 입니다. ** \*Cat** (접미사 검색), 중 위 검색 **(\*c t** ) 및 ** \*cat\* ** (하위 문자열 검색)은 지원 되지 않습니다. 
    
- 속성을 검색할 때 검색 값이 여러 단어로 구성 된 경우 큰따옴표 ("")를 사용 합니다. 예 `subject:budget Q1` 를 들어 제목 줄에 **예산이** 포함 되 고 메시지의 모든 위치나 메시지 속성에 있는 **Q1** 이 포함 된 메시지가 반환 됩니다. 사용 `subject:"budget Q1"` 에서는 제목 줄의 모든 위치에 **예산 Q1** 이 포함 된 모든 메시지를 반환 합니다. 
    
- 검색 결과에서 특정 속성 값으로 표시된 콘텐츠를 제외하려면 속성 이름 앞에 빼기 기호(-)를 추가합니다. 예를 들어 `-from:"Sara Davis"` Sara Davis에서 보낸 모든 메시지를 제외 합니다.

- 일부 특수 문자가 검색 인덱스에 포함 되지 않아 검색할 수 없는 경우에는 검색 연산자 (+-=:))를 포함 합니다. 그리고 $null로 대체 되는 다음 문자를 검색 하면 오류가 발생할 수 있습니다. @ #% ^ &; _ / ?

- 메시지 유형을 기준으로 항목을 내보낼 수 있습니다. 예를 들어 Microsoft 팀에서 Skype 대화 및 채팅을 내보내려면 구문을 `kind:im`사용 합니다. 전자 메일 메시지만 반환 하려면를 사용 `kind:email`합니다. Microsoft 팀에서 채팅, 모임 및 통화를 반환 하려면를 사용 `kind:microsoftteams`합니다.
