---
title: 검색 및 태그 지정
ms.author: chrfox
author: chrfox
manager: laurawi
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 22f5adad-1bc0-460d-94a9-8732929f5b99
description: 고급 eDiscovery에서 검색 및 태그 지정 모듈을 사용 하 여 사용자의 경우 문서를 검색, 미리 보기 및 구성할 수 있습니다. 현재이 모듈은 베타 버전입니다.
ms.openlocfilehash: b3e660e6dca014323cfd06f10c14747751aeb386
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/17/2019
ms.locfileid: "34158540"
---
# <a name="search-and-tagging"></a>검색 및 태그 지정

고급 eDiscovery에서 검색 및 태그 지정 모듈을 사용 하 여 사용자의 경우 문서를 검색, 미리 보기 및 구성할 수 있습니다. 현재이 모듈은 베타 버전입니다. 검색 및 태그 지정에 대 한 간단한 데모를 보려면 [고급 eDiscovery로 데이터 관리](https://www.youtube.com/watch?v=VaPYL3DHP6I) 비디오를 참조 하세요.

> [!NOTE]
> Advanced eDiscovery를 사용하려면 Office 365 E3의 고급 준수 추가 기능이나 조직을 위한 E5 구독이 필요합니다. 이 요금제가 없는 상태에서 Advanced eDiscovery를 사용하려는 경우에는 [Office 365 Enterprise E5 평가판을 등록](https://go.microsoft.com/fwlink/p/?LinkID=698279)할 수 있습니다. 
  
## <a name="search-the-documents-in-your-case"></a>사례에서 문서 검색

고급 eDiscovery 사례에서 문서를 처리 하 고 (필요한 경우 분석 또는 관련성 모듈을 실행) 검색 및 태그 지정 기능을 사용 하 여 문서를 검색 한 다음 대/소문자 별 태그 (레이블 라고도 함)를 적용 하 여이를 구성할 수 있습니다. 제공 된 조건 카드를 사용 하거나 키워드 조건 카드에서 KQL와 같은 형식의 쿼리 언어를 사용 하 여 검색 쿼리를 정의할 수 있습니다. AND, OR, NOT 및 NEAR (n)과 같은 일반 KQL 구문은 지원 되 고 후행 여러 문자 와일드 카드 (*)와 유사 합니다. 

다음 표에는 KQL keyword 쿼리를 사용 하 여 검색할 수 있는 속성이 나와 있습니다. 또는 고급 eDiscovery 검색 도구에서 조건 카드를 사용 하 여 검색 쿼리에 조건 (선택한 속성)을 추가할 수 있습니다.

|**속성**|**설명**|
|:-----|:-----|
|**caselabel** <br/> | 문서에 태그를 지정 하는 경우 생성/적용 되는 태그의 이름입니다. <br/> |
|**custodian** <br/> | 문서와 연결 된 custodian입니다. 제한 사항에 따라 달라 집니다. <br/> |
|**종료일** <br/> | 전자 메일을 보낸 날짜 사이트 문서를 수정한 날짜입니다. <br/> |
|**열려** <br/> | 사례 내의 파일 ID입니다. <br/> |
|**filetype** <br/> | 네이티브 파일 확장명입니다. <br/> |
|**fileclass** <br/> | 전자 메일, 문서 또는 첨부 파일 <br/> |
|**senderauthor** <br/> | 전자 메일 보낸 사람 사이트 문서에 대 한 작성자입니다. <br/> |
|**크기** <br/> | 파일 크기 (MB)입니다. <br/> |
|**호칭 제목** <br/> | 전자 메일의 제목입니다. 사이트 문서의 제목입니다. <br/> |
|**숨은 참조** <br/> | 전자 메일의 숨은 참조 필드입니다. <br/> |
|**참조** <br/> | 전자 메일의 참조 필드입니다. <br/> |
|**할당** <br/> | 누락 된 링크를 포함 하 여 전자 메일 스레드에 있는 모든 참가자의 전자 메일 주소입니다. <br/> |
|**received** <br/> | 전자 메일을 받은 날짜입니다. <br/> |
|**받는 사람** <br/> | 전자 메일의 받는 사람, 참조 또는 숨은 참조 필드에 포함 됩니다. <br/> |
|**보낸 사람** <br/> | 전자 메일을 보낸 사람입니다. <br/> |
|**lastmodifieddate** <br/> | 사이트 문서를 마지막으로 수정한 날짜입니다. <br/> |
|**전송할** <br/> | 전자 메일의 보낸 날짜입니다. <br/> |
|**받는 사람** <br/> | 전자 메일의 받는 사람 필드에 나열 되어 있습니다. <br/> |
|**제작할** <br/> | 사이트 문서의 만든이입니다. <br/> |
|**직책** <br/> | 사이트 문서의 제목입니다. <br/> |
|**dominanttheme**\* <br/> | 항목의 기준 테마입니다. <br/> |
|**기타 eslist**\* <br/> | 항목과 연결 된 테마입니다. <br/> |
|**readpercentile_[issuenum]**\*\* <br/> | [Issuenum]로 정의 된 문제에 대해 항목의 읽기 백분위 수를 지정 합니다. <br/> |
|**relevancescore_[issuenum]**\*\* <br/> | [Issuenum]에 의해 정의 된 문제에 대 한 항목의 관련성 점수입니다. <br/> |
|**relevancetag_ [tagname]**\*\* <br/> | 항목에 관련성을 수동으로 태그가 지정 된 경우 [tagname]에 정의 된 태그입니다. <br/> |
|||

\*Themes 모듈을 실행 한 경우에만 사용할 수 있습니다.

\*\*관련성 모듈이 실행 된 경우에만 사용할 수 있습니다.

또는 고급 eDiscovery 검색 도구에서 조건 카드를 사용 하 여 검색 쿼리에 조건 (선택한 속성)을 추가할 수 있습니다. 다음 스크린샷은 쿼리에 추가할 수 있는 조건을 보여 줍니다. **그룹** 열은 속성을 전자 메일, 사이트 문서 또는 둘 다에 적용할지를 나타냅니다 ( *공통*값으로 표시 됨). 또한이 열은 관련성 모듈을 실행 한 후에 사용할 수 있는 검색 가능한 속성을 식별 합니다.

![Advanced eDiscovery 검색 도구의 검색 조건](media/AeDSearchConditions.png)

검색 가능한 속성에 대 한 자세한 내용은 [키워드 쿼리 및 검색 조건을](keyword-queries-and-search-conditions.md)참조 하세요.
  
## <a name="see-also"></a>참고 항목

[Office 365 Advanced eDiscovery](office-365-advanced-ediscovery.md)
  
[관련성 평가 이해](assessment-in-relevance-in-advanced-ediscovery.md)
  
[태그 지정 및 평가](tagging-and-assessment-in-advanced-ediscovery.md)
  
[태그 지정 및 관련성 교육](tagging-and-relevance-training-in-advanced-ediscovery.md)
  
[관련성 분석 추적](track-relevance-analysis-in-advanced-ediscovery.md)
  
[결과를 기준으로 결정](decision-based-on-the-results-in-advanced-ediscovery.md)
  
[관련성 분석 테스트](test-relevance-analysis-in-advanced-ediscovery.md)

