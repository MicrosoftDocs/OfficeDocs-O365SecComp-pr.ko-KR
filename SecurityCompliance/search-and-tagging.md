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
# <a name="search-and-tagging"></a>검색 및 태그 지정

고급 ediscovery에서 검색 및 태그 지정 모듈을 사용 하면 검색, 미리 보기, 및 사례에 문서를 구성 하 고 수 있습니다. 현재이 모듈 베타 버전에서입니다.

> [!NOTE]
> 고급 eDiscovery 조직에 대 한 고급 준수 추가 기능 또는 e 5 구독은 Office 365 E3 필요합니다. 해당 요금제에 가입한 상태 고급 eDiscovery 시도 하려는 하지 경우에 [Office 365 Enterprise e 5의 평가판 등록](https://go.microsoft.com/fwlink/p/?LinkID=698279)할 수 있습니다. 
  
## <a name="search-the-documents-in-your-case"></a>사례에는 문서를 검색 합니다.

고급 eDiscovery의 문서를 처리 한 되 고 분석 모듈 또는 관련성 모듈을 필요에 따라 실행 검색을 사용할 수 있는 태그 지정 하는 경우에는 문서를 통해 검색 하 고 구성 하 고, 대/소문자 관련 태그를 사용 하 고 있습니다. 제공 된 조건 카드를 사용 하 여 쿼리를 정의 하거나 키워드에 KQL와 같은 쿼리 언어를 통해 카드 조건문 수 있습니다. AND, OR, NOT, 예: 일반적인 KQL 구문을 NEAR(n)는 지원 되는,으로 후행 다중 문자 와일드 카드 (*) 하 고 있습니다. 이러한 속성은 쿼리 언어 속성 이름에 지원 됩니다.

- caselabel: 만든/적용 된 태그에서 검색 하 고 태그 지정이 있는 경우 
- custodians: custodians 제한 사항에 따라 달라 집니다 경우-할당
- 날짜: 보낸 전자 메일에 대 한 날짜, 수정한 문서에 대 한 날짜
- fileid: 대/소문자 내에서 파일 ID
- 파일 형식: 기본 파일 확장명
- fileclass: 전자 메일, 문서 또는 첨부 파일
- senderauthor: 만든이 문서에 대 한 전자 메일에 대 한 보낸사람
- 크기: KB에서 파일의 크기 조정
- 게시가: 전자 메일, 문서에 대 한 제목에 대 한 제목
- 숨은 참조
- 참조
- 참가자: 누락 된 링크를 포함 하 여 전자 메일 스레드에서 모든 참가자의 주소를 전자 메일로 보내기
- 수신: 받은 날짜
- 받는 사람: 전자 메일을 받는 사람 이름 또는 주소 (, 참조, 숨은 참조)
- 보낸 사람
- lastmodifieddate: 마지막으로 수정한 날짜의 문서
- 전송: 보낸 전자 메일의 날짜
- 작업
- 만든이: 만든이의 전자 메일
- 제목: 문서 제목
- dominanttheme: 항목의 기준 테마\*
- themeslist: 항목 연관 된 테마\*
- readpercentile_ [issuenum]: [issuenum] 문제에 대 한 항목의 백분위 수 읽기\*\*
- relevancescore_ [issuenum]: [issuenum] 문제에 대 한 항목의 관련성 점수\*\*
- relevancetag_ [issuenum]: 관련성, [issuenum]에 대 한 자체의 태그에 대 한 항목 수동으로 표시 된 경우\*\*

\*테마 모듈이 실행 된 경우에 사용할 수 \* \* 관련성 모듈이 실행 된 경우에 사용할 수
  
## <a name="see-also"></a>참고 항목

[Office 365 Advanced eDiscovery](office-365-advanced-ediscovery.md)
  
[관련성에 이해 평가](assessment-in-relevance-in-advanced-ediscovery.md)
  
[태그 지정 및 평가](tagging-and-assessment-in-advanced-ediscovery.md)
  
[태그 지정 및 관련성 교육](tagging-and-relevance-training-in-advanced-ediscovery.md)
  
[관련성 분석 추적](track-relevance-analysis-in-advanced-ediscovery.md)
  
[결과에 따라 결정](decision-based-on-the-results-in-advanced-ediscovery.md)
  
[관련성 분석 테스트](test-relevance-analysis-in-advanced-ediscovery.md)

