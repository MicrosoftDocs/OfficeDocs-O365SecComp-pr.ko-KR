---
title: 사이트에 저장된 중요한 데이터를 찾기 위한 쿼리 작성
ms.author: chrfox
author: chrfox
manager: laurawi
ms.date: 6/29/2018
audience: Admin
ms.topic: article
ms.service: O365-seccomp
ms.collection:
- M365-security-compliance
localization_priority: Normal
search.appverid:
- MOE150
- MET150
description: SharePoint Online의 DLP (데이터 손실 방지)를 사용 하 여 테 넌 트 전체에서 중요 한 데이터가 포함 된 문서를 검색할 수 있습니다. 문서를 검색한 후 문서 소유자와 함께 작업하여 데이터를 보호할 수 있습니다. 이 항목은 중요한 데이터를 검색하는 쿼리를 작성하는 데 도움이 될 수 있습니다.
ms.openlocfilehash: c9013e8334a4ef891885c7bc53b746b2db42b156
ms.sourcegitcommit: 7a0cb7e1da39fc485fc29e7325b843d16b9808af
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/07/2019
ms.locfileid: "36230552"
---
# <a name="form-a-query-to-find-sensitive-data-stored-on-sites"></a>사이트에 저장된 중요한 데이터를 찾기 위한 쿼리 작성

사용자들은 종종 신용 카드 번호, 사회 보장 번호 또는 개인 정보와 같은 중요한 데이터를 사이트에 저장하며, 시간에 지나면서 이로 인해 조직은 심각한 데이터 손실 위험에 처할 수 있습니다. 비즈니스용 OneDrive 사이트를 포함 하 여 사이트에 저장 된 문서는 해당 정보에 대 한 액세스 권한이 없는 조직 외부의 사용자와 공유할 수 있습니다. SharePoint Online의 DLP (데이터 손실 방지)를 사용 하 여 테 넌 트 전체에서 중요 한 데이터가 포함 된 문서를 검색할 수 있습니다. 문서를 검색한 후 문서 소유자와 함께 작업하여 데이터를 보호할 수 있습니다. 이 항목은 중요한 데이터를 검색하는 쿼리를 작성하는 데 도움이 될 수 있습니다.
  
> [!NOTE]
> 전자 검색, eDiscovery 및 DLP는 [SharePoint Online 계획 2](https://go.microsoft.com/fwlink/?LinkId=510080)가 필요한 프리미엄 기능입니다. 
  
## <a name="forming-a-basic-dlp-query"></a>기본 DLP 쿼리 작성

기본 DLP 쿼리는 중요한 정보 유형, 개수 범위 및 신뢰도 범위의 세 부분으로 구성됩니다. 다음 그림과 같이 **SensitiveType: "\<\>type"** 이 필요 하며**|\<\> count 범위** 와**|\<신뢰 범위\> ** 모두 선택 사항입니다. 
  
![필수 및 옵션으로 구분되는 예제 쿼리](media/DLP-query-example-text.png)
  
### <a name="sensitive-type---required"></a>중요한 정보 유형 - 필수

그렇다면 각 부분에는 어떤 것이 있나요? SharePoint DLP 쿼리는 일반적으로 중요 한 `SensitiveType:"` [정보 유형 인벤토리에서](https://go.microsoft.com/fwlink/?LinkID=509999)속성 및 정보 형식 이름으로 시작 되며로 끝납니다 `"`. 조직에 대해 만든 [사용자 지정 중요 한 정보 유형의](create-a-custom-sensitive-information-type.md) 이름을 사용할 수도 있습니다. 예를 들어 신용 카드 번호가 포함 된 문서를 찾고 있을 수 있습니다. 이러한 인스턴스에서는 다음 형식을 사용 해야 `SensitiveType:"Credit Card Number"`합니다. 개수 범위 또는 신뢰 범위를 포함 하지 않았으므로이 쿼리는 신용 카드 번호가 검색 되는 모든 문서를 반환 합니다. 이 쿼리는 가장 간단한 쿼리로, 가장 많은 결과를 반환 합니다. 중요 한 유형의 철자와 간격이 중요 하다는 것을 염두에 두어야 합니다. 
  
### <a name="ranges---optional"></a>범위 - 옵션

그 다음 두 개의 요소는 모두 범위 이므로 범위를 빠르게 확인할 수 있습니다. SharePoint DLP 쿼리에서 기본 범위는 두 개의 마침표로 구분 되는 두 개의 숫자로 표현 되며 다음과 `[number]..[number]`같습니다. 예를 들어이 `10..20` 값이 사용 되는 경우 해당 범위는 10에서 20 사이의 숫자를 캡처합니다. 다양 한 범위 조합이 있으며이 항목에서는 여러 가지 내용에 대해 설명 합니다. 
  
쿼리에 개수 범위를 추가 해 보겠습니다. 개수 범위를 사용 하 여 문서를 쿼리 결과에 포함 하기 전에 포함 해야 하는 중요 한 정보의 발생 수를 정의할 수 있습니다. 예를 들어 쿼리가 정확히 5 개의 신용 카드 번호를 포함 하는 문서만 반환 하 게 하려면 다음 `SensitiveType:"Credit Card Number|5"`을 사용 합니다. 또한 개수 범위는 높은 수준의 위험을 야기 하는 문서를 식별 하는 데 도움이 됩니다. 예를 들어 조직에서 5 명 이상의 신용 카드 번호가 포함 된 문서를 높은 위험 수준으로 고려할 수 있습니다. 이 조건에 해당 하는 문서를 찾으려면 다음 `SensitiveType:"Credit Card Number|5.."`쿼리를 사용 합니다. 또는 다음 `SensitiveType:"Credit Card Number|..5"`쿼리를 사용 하 여 5 개 이하의 신용 카드 번호가 포함 된 문서를 찾을 수 있습니다. 
  
#### <a name="confidence-range"></a>신뢰도 범위

마지막으로 신뢰 범위는 검색 된 중요 형식이 실제로 일치 하는 신뢰도 수준입니다. 신뢰도 범위에 대 한 값이 count 범위와 유사 하 게 작동 합니다. 개수 범위를 포함 하지 않고 쿼리를 만들 수 있습니다. 예를 들어 신뢰 범위가 85% 이상인 경우 신용 카드 번호를 사용 하 여 문서를 검색 하는 경우이 쿼리 `SensitiveType:"Credit Card Number|*|85.."`를 사용할 수 있습니다. 
  
> [!IMPORTANT]
> 별표 ( `*`)는 와일드 카드 문자로, 모든 값이 작동 함을 의미 합니다. 개수 범위 또는 신뢰도 범위에서 와일드 `*`카드 문자 ()를 사용할 수 있지만이 경우에는 중요 한 형식이 아닙니다. 
  
### <a name="additional-query-properties-and-search-operators-available-in-the-ediscovery-center"></a>eDiscovery 센터에서 사용할 수 있는 추가 쿼리 속성 및 검색 연산자

또한 SharePoint의 DLP에는 특정 시간대 내에서 검색 되는 파일을 검색 하는 데 도움이 되는 LastSensitiveContentScan 속성을 소개 합니다. 이 속성을 사용 하 `LastSensitiveContentScan` 는 쿼리 예제는 다음 섹션의 [복잡 한 쿼리 예](#examples-of-complex-queries) 를 참조 하십시오. 
  
DLP 관련 속성만 사용 하 여 쿼리를 만들 수 있을 뿐 아니라 또는 `Author` `FileExtension`와 같은 표준 SharePoint eDiscovery 검색 속성을 사용할 수도 있습니다. 연산자를 사용하여 복잡한 쿼리를 작성할 수 있습니다. 사용 가능한 속성 및 연산자 목록에 대해서는 eDiscovery 블로그 게시물에서 [검색 속성 및 연산자 사용](https://go.microsoft.com/fwlink/?LinkId=510093) 을 참조 하십시오. 
  
## <a name="examples-of-complex-queries"></a>예제

다음 예제에서는 서로 다른 중요 한 형식, 속성 및 연산자를 사용 하 여 쿼리를 구체화 하 여 원하는 결과를 정확히 찾는 방법을 보여 줍니다.
  
|**Query**|**설명**|
|:-----|:-----|
| `SensitiveType:"International Banking Account Number (IBAN)"` <br/> |이는 길이가 긴 하지만 해당 중요 형식에 대 한 올바른 이름이 며 이름이 이상 하 게 보일 수 있습니다. [중요 한 정보 유형 인벤토리에서](https://go.microsoft.com/fwlink/?LinkID=509999)정확한 이름을 사용 해야 합니다. 조직에 대해 만든 [사용자 지정 중요 한 정보 유형의](create-a-custom-sensitive-information-type.md) 이름을 사용할 수도 있습니다.  <br/> |
| `SensitiveType:"Credit Card Number|1..4294967295|1..100"` <br/> |중요 한 유형 "신용 카드 번호"에 대 한 일치 하는 항목이 하나 이상 포함 된 문서를 반환 합니다. 각 범위의 값은 해당 최소값 및 최대값입니다. 이 쿼리를 좀 더 간단 하 게 `SensitiveType:"Credit Card Number"`작성할 수는 있지만,이를 위한 흥미로운 방법은 무엇 인가요?  <br/> |
| `SensitiveType:"Credit Card Number| 5..25" AND LastSensitiveContentScan:"8/11/2018..8/13/2018"` <br/> |이 값은 5-25 년 8 월 11 일에서 검색 된 2018 2018 신용 카드 번호를 포함 하는 문서를 반환 합니다.  <br/> |
| `SensitiveType:"Credit Card Number| 5..25" AND LastSensitiveContentScan:"8/11/2018..8/13/2018" NOT FileExtension:XLSX` <br/> |이 값은 5-25 년 8 월 11 일에서 검색 된 2018 2018 신용 카드 번호를 포함 하는 문서를 반환 합니다. .XLSX 확장명을 가진 파일은 쿼리 결과에 포함 되지 않습니다.  `FileExtension`는 쿼리에 포함할 수 있는 여러 속성 중 하나입니다. 자세한 내용은 [eDiscovery에 검색 속성 및 연산자 사용](https://go.microsoft.com/fwlink/?LinkId=510093)을 참조 하십시오.  <br/> |
| `SensitiveType:"Credit Card Number" OR SensitiveType:"U.S. Social Security Number (SSN)"` <br/> |이 쿼리는 신용 카드 번호 또는 사회 보장 번호가 포함된 문서를 반환합니다.  <br/> |
   
## <a name="examples-of-queries-to-avoid"></a>예제

모든 쿼리가 동일하게 만들어지는 것은 아닙니다. 다음 표에서는 SharePoint에서 DLP에 대해 작동 하지 않는 쿼리의 예와 해당 이유에 대해 설명 합니다.
  
|**지원되지 않는 쿼리**|**이유**|
|:-----|:-----|
| `SensitiveType:"Credit Card Number|.."` <br/> |하나 이상의 숫자를 추가해야 합니다.  <br/> |
| `SensitiveType:"NotARule"` <br/> |"NotARule"은 유효한 중요 형식 이름이 아닙니다. [중요 한 정보 유형 목록](https://go.microsoft.com/fwlink/?LinkID=509999) 에 있는 이름만 DLP 쿼리에서 작동 합니다.  <br/> |
| `SensitiveType:"Credit Card Number|0"` <br/> |0은 범위의 최소값 또는 최대값으로 올바르지 않습니다.  <br/> |
| `SensitiveType:"Credit Card Number"` <br/> |보기는 어려울 수 있지만 "신용"와 "카드" 사이에는 쿼리가 잘못 된 것을 나타내는 추가 공백이 있습니다. [중요 한 정보 유형 인벤토리에서](https://go.microsoft.com/fwlink/?LinkID=509999)정확히 중요 한 형식 이름을 사용 합니다.  <br/> |
| `SensitiveType:"Credit Card Number|1. .3"` <br/> |두 기간 부분은 공백으로 구분 하지 않아야 합니다.  <br/> |
| `SensitiveType:"Credit Card Number| |1..|80.."` <br/> |파이프 구분 기호가 너무 많습니다 (|). 대신 다음 형식을 따르세요.`SensitiveType: "Credit Card Number|1..|80.."` <br/> |
| `SensitiveType:"Credit Card Number|1..|80..101"` <br/> |신뢰도 값은 백분율을 나타내므로 100을 초과할 수 없습니다. 따라서 1에서 100 사이의 숫자를 선택하세요.  <br/> |
   
## <a name="for-more-information"></a>자세한 내용

[중요한 정보 유형이 찾는 항목](what-the-sensitive-information-types-look-for.md)
  
[Office 365 보안 &amp; 및 준수 센터에서 콘텐츠 검색 실행](run-a-content-search-in-the-security-and-compliance-center.md)
  
[콘텐츠 검색에 대한 키워드 쿼리 및 검색 조건](keyword-queries-and-search-conditions.md)
  

