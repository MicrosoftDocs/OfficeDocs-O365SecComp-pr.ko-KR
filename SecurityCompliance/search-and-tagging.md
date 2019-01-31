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
# <a name="search-and-tagging"></a>검색 및 태그 지정

고급 ediscovery에서 검색 및 태그 지정 모듈을 사용 하면 검색, 미리 보기, 및 사례에 문서를 구성 하 고 수 있습니다. 현재이 모듈 베타 버전에서입니다. 검색 및 태그의 간단한 데모, [고급 eDiscovery 사용 하 여 데이터 관리](https://www.youtube.com/watch?v=VaPYL3DHP6I) 비디오를 참조 하십시오.

> [!NOTE]
> Advanced eDiscovery를 사용하려면 Office 365 E3의 고급 준수 추가 기능이나 조직을 위한 E5 구독이 필요합니다. 이 요금제가 없는 상태에서 Advanced eDiscovery를 사용하려는 경우에는 [Office 365 Enterprise E5 평가판을 등록](https://go.microsoft.com/fwlink/p/?LinkID=698279)할 수 있습니다. 
  
## <a name="search-the-documents-in-your-case"></a>사례에는 문서를 검색 합니다.

후 고급 eDiscovery 사례에서 문서를 처리 (분석 또는 관련성 모듈을 실행 하는 필요한 경우), 문서를 검색 하 고 다음 (레이블 라고도 함)는 대/소문자 관련 태그를 적용 하 여 구성 하는 검색 및 태그를 사용할 수 있습니다. 제공 된 조건 카드를 사용 하 여 검색 쿼리를 정의 하거나 키워드의 KQL와 같은 쿼리 언어를 사용 하 여 카드 조건문 수 있습니다. AND, OR, NOT, 예: 일반적인 KQL 구문을 NEAR(n)는 지원 되는,으로 후행 다중 문자 와일드 카드 (*) 하 고 있습니다. 

다음 표에서 KQL 키워드 쿼리를 사용 하 여 검색할 수 있는 속성을 보여줍니다. 또는 (선택한 속성)에 대 한 조건 검색 쿼리를 추가 하려면 고급 ediscovery 검색 도구에 대 한 조건 카드를 사용할 수 있습니다.

|**속성**|**설명**|
|:-----|:-----|
|**caselabel** <br/> | 만든/때 적용 되는 문서 태그가 지정 된 태그의 이름입니다. <br/> |
|**더불어** <br/> | 더불어 연관 된 문서입니다. 있으며 제한 사항이 있습니다. <br/> |
|**날짜** <br/> | 보낸 전자 메일;에 대 한 날짜 사이트 문서에 대 한 수정 된 날짜입니다. <br/> |
|**fileid** <br/> | 대/소문자 내에서 파일 ID입니다. <br/> |
|**파일 형식** <br/> | 기본 파일 확장명입니다. <br/> |
|**fileclass** <br/> | 전자 메일, 문서 또는 첨부 파일입니다. <br/> |
|**senderauthor** <br/> | 전자 메일;에 대 한 보낸사람 사이트 문서에 대 한 만든이입니다. <br/> |
|**크기** <br/> | KB에 있는 파일의 크기입니다. <br/> |
|**게시가** <br/> | 전자 메일;에 대 한 제목 사이트 문서에 대 한 제목입니다. <br/> |
|**숨은 참조** <br/> | 전자 메일의 숨은 참조 필드입니다. <br/> |
|**참조** <br/> | 전자 메일의 참조 필드입니다. <br/> |
|**참가자** <br/> | 누락 된 링크를 포함 하 여 전자 메일 스레드의 모든 참가자의 전자 메일 주소입니다. <br/> |
|**수신** <br/> | 전자 메일을 받은 날짜입니다. <br/> |
|**받는 사람** <br/> | 전자 메일의 받는 사람에 포함 된 받는 사람, 사람, 참조 또는 숨은 참조 필드입니다. <br/> |
|**보낸 사람** <br/> | 전자 메일의 보낸사람입니다. <br/> |
|**lastmodifieddate** <br/> | 마지막 수정 날짜의 사이트 문서입니다. <br/> |
|**전송** <br/> | 전자 메일의 보낸된 날짜입니다. <br/> |
|**받는 사람** <br/> | 전자 메일의 받는 사람 필드에 나열 된 받는 사람입니다. <br/> |
|**작성자** <br/> | 사이트 문서 작성자입니다. <br/> |
|**제목** <br/> | 사이트 문서의 제목입니다. <br/> |
|**dominanttheme**\* <br/> | 항목의 기준 테마입니다. <br/> |
|**themeslist**\* <br/> | 항목에 연관 된 테마입니다. <br/> |
|**readpercentile_ [issuenum]**\*\* <br/> | [Issuenum]에 정의 된 문제에 대 한 항목의 읽기 백분위 수 있습니다. <br/> |
|**relevancescore_ [issuenum]**\*\* <br/> | [Issuenum]에 정의 된 문제에 대 한 항목의 관련성 점수입니다. <br/> |
|**relevancetag_ [tagname]**\*\* <br/> | 항목이 있으면 된 수동으로 관련성, [tagname]으로 정의 하는 태그에 대 한 태그가 지정 된 됩니다. <br/> |
|||

\*테마 모듈이 실행 된 경우에 사용할 수 있습니다.

\*\*관련성 모듈이 실행 된 경우에 사용할 수 있습니다.

또는 고급 eDiscovery 검색 도구 (선택한 속성)에 대 한 조건 검색 쿼리를 추가 하려면 조건 카드를 사용할 수 있습니다. 다음 스크린샷에서 쿼리를 추가할 수 있는 조건입니다. **그룹** 열 속성은 전자 메일, 사이트 문서 또는 ( *공통*값으로 표시) 모두에 적용 되는지 여부를 나타냅니다. 또한이 열 관련성 모듈을 실행 하 고 나면 사용할 수 있는 검색 가능한 속성을 식별 합니다.

![고급 eDiscovery 검색 도구에서 검색 조건](media/AeDSearchConditions.png)

검색 가능한 속성에 대 한 자세한 내용은 [쿼리 키워드 및 검색 조건을](keyword-queries-and-search-conditions.md)참조 하십시오.
  
## <a name="see-also"></a>참고 항목

[Office 365 Advanced eDiscovery](office-365-advanced-ediscovery.md)
  
[관련성에 이해 평가](assessment-in-relevance-in-advanced-ediscovery.md)
  
[태그 지정 및 평가](tagging-and-assessment-in-advanced-ediscovery.md)
  
[태그 지정 및 관련성 교육](tagging-and-relevance-training-in-advanced-ediscovery.md)
  
[관련성 분석 추적](track-relevance-analysis-in-advanced-ediscovery.md)
  
[결과에 따라 결정](decision-based-on-the-results-in-advanced-ediscovery.md)
  
[관련성 분석 테스트](test-relevance-analysis-in-advanced-ediscovery.md)

