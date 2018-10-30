---
title: 사이트에 저장된 중요한 데이터를 찾기 위한 쿼리 작성
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 6/29/2018
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: 3019fbc5-7f15-4972-8d0e-dc182dc7f836
description: SharePoint Online에서 데이터 손실 방지 (DLP), 테 넌 트 전체에서 중요 한 데이터를 포함 하는 문서를 검색할 수 있습니다. 문서를 검색 한 후 데이터를 보호 하기 위해 문서 소유자와 함께 작업할 수 있습니다. 이 항목 중요 한 데이터를 검색 하는 쿼리를 형성 하는 데 도움이 됩니다.
ms.openlocfilehash: c30cb2e4b93e1a7db90f3e3f922f406285c6f692
ms.sourcegitcommit: 81e06e09bf5ca8e3f51b164d6251b1c35b3285cf
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2018
ms.locfileid: "25829189"
---
# <a name="form-a-query-to-find-sensitive-data-stored-on-sites"></a>사이트에 저장된 중요한 데이터를 찾기 위한 쿼리 작성

개인, 자신의 사이트에 그리고 시간이 지남에 따라이 노출할 수 데이터 손실의 중요 한 위험을 조직 또는 사용자가 자주 신용 카드 번호, 주민등록 번호, 등의 중요 한 데이터를 저장 합니다. 사이트에 저장 된 문서-OneDrive를 포함 하 여 비즈니스 사이트에 대 한-안 되는 정보에 대 한 액세스를 가진 조직 외부의 사용자와 공유할 수 없습니다. SharePoint Online에서 데이터 손실 방지 (DLP), 테 넌 트 전체에서 중요 한 데이터를 포함 하는 문서를 검색할 수 있습니다. 문서를 검색 한 후 데이터를 보호 하기 위해 문서 소유자와 함께 작업할 수 있습니다. 이 항목 중요 한 데이터를 검색 하는 쿼리를 형성 하는 데 도움이 됩니다.
  
> [!NOTE]
> 전자 검색 또는 eDiscovery 및 DLP는 [SharePoint Online 계획 2](https://go.microsoft.com/fwlink/?LinkId=510080)필요로 하는 프리미엄 기능입니다. 
  
## <a name="forming-a-basic-dlp-query"></a>기본 DLP 쿼리 작성

기본 DLP 쿼리를 구성 하는 세 부분으로 이루어져 있습니다: SensitiveType, 범위 및 신뢰 범위를 계산 합니다. 다음 그림에 나와있는 것 처럼 **SensitiveType: "\<유형\>"** 이 필요 하 고 모두**|\<범위를 계산\> ** 및**|\<신뢰 범위\> ** 는 선택 사항입니다. 
  
![필수 및 옵션으로 구분되는 예제 쿼리](media/DLP-query-example-text.png)
  
### <a name="sensitive-type---required"></a>중요한 정보 유형 - 필수

따라서 각 부분 이란? SharePoint DLP 쿼리 속성은 일반적으로 시작 `SensitiveType:"` 및 [중요 한 정보 유형 인벤토리](https://go.microsoft.com/fwlink/?LinkID=509999)에서 이름을 지정 하 고 끝나는 정보 유형을 `"`합니다. 또한 조직에 대해 만든 [사용자 지정 중요 한 정보 유형](create-a-custom-sensitive-information-type.md) 이름을 사용할 수 있습니다. 예, 신용 카드 번호를 포함 하는 문서에 대 한 보고 있을 수 있습니다. 이러한 인스턴스에 다음 형식 사용: `SensitiveType:"Credit Card Number"`합니다. Count 범위나 신뢰 범위를 포함 하지 않았으므로, 때문에 쿼리 신용 카드 번호를 검색 하는 모든 문서를 반환 합니다. 실행할 수 있는 가장 간단한 쿼리 이며 대부분의 결과 반환 합니다. 맞춤법 검사 및 중요 한 종류의 간격을 되어있으면 점을 염두에 두십시오. 
  
### <a name="ranges---optional"></a>범위 - 옵션

다음 두 부분에 모두 범위, 보겠습니다 신속 하 게 범위의 모습을 검사 합니다. SharePoint DLP 쿼리 기본 범위로 표현 됩니다 2 개의 마침표로 구분 된 두 숫자는 다음과 같은: `[number]..[number]`합니다. 예를 하는 경우 `10..20` 를 사용 하 고, 해당 범위는 캡처 10 20% ~ 번호입니다. 여러 다른 범위 조합 및이 항목에서 설명 하는 몇가지 있습니다. 
  
쿼리를 count 범위를 추가 해 보겠습니다. 문서 쿼리 결과에 포함 된 전에 반드시 포함 해야하는 중요 한 정보의 발생 횟수를 정의 하려면 count 범위를 사용할 수 있습니다. 예 5 정확 하 게 신용 카드 번호를 포함 하는 문서에만 반환 하 여 쿼리를 사용할 경우이 사용: `SensitiveType:"Credit Card Number|5"`합니다. Count 범위 높은 수준의 위험이 발생할 수 있는 문서를 식별 하면을 수 있습니다. 등 조직 5 개 이상의 신용 카드 번호를 사용 하 여 문서 높은 위험 수준 고려 될 수 있습니다. 이 조건은 맞춤 하는 문서를 찾으려면이 쿼리를 사용 하면: `SensitiveType:"Credit Card Number|5.."`합니다. 또는 5 개를 사용 하 여 문서를 찾을 수 또는이 쿼리를 사용 하 여 적은 수의 신용 카드 번호: `SensitiveType:"Credit Card Number|..5"`합니다. 
  
#### <a name="confidence-range"></a>신뢰도 범위

마지막으로, 신뢰 범위는 검색 된 중요 한 형식이 일치 하는 실제로 임을 신뢰의 수준입니다. 신뢰 범위에 대 한 값 범위를 계산 하려면 비슷하게 작동 합니다. Count 범위를 포함 하지 않고 쿼리를 만들 수 있습니다. 예: 신용 카드 번호의 숫자를 사용 하 여 문서를 검색 하려면-이상 만큼 반복할 신뢰 범위는 85%-이 쿼리를 사용 하면: `SensitiveType:"Credit Card Number|*|85.."`합니다. 
  
> [!IMPORTANT]
> 별표 ( `*`) 모든 값의 작동을 의미 하는 와일드 카드 문자입니다. 와일드 카드 문자를 사용할 수 있습니다 ( `*`) 중 하나에서 count 범위 또는 신뢰 범위에 있지만 중요 한 형식에 없는 합니다. 
  
### <a name="additional-query-properties-and-search-operators-available-in-the-ediscovery-center"></a>eDiscovery 센터에서 사용할 수 있는 추가 쿼리 속성 및 검색 연산자

또한 DLP SharePoint에 대 한 특정 시간 범위 내에서 검색 되는 파일에 대 한 검색 하는데 도움이 되는 속성 LastSensitiveContentScan를 소개 합니다. 에 대 한와 쿼리 예는 `LastSensitiveContentScan` 속성을 다음 섹션의 [복잡 한 쿼리의 예제](form-a-query-to-find-sensitive-data-stored-on-sites.md#BKMK_ExamplesOfComplexQueries) 를 참조 합니다. 
  
쿼리를 만들려면 DLP 관련 속성은 물론 표준 SharePoint eDiscovery 검색 속성을 다음과 같이 사용할 수 `Author` 또는 `FileExtension`합니다. 복잡 한 쿼리를 작성할 연산자를 사용할 수 있습니다. 사용 가능한 속성 및 연산자 목록 [검색 속성을 사용 하 고 eDiscovery 사용 하 여 연산을](https://go.microsoft.com/fwlink/?LinkId=510093) 블로그 게시물을 참조 하십시오. 
  
## <a name="examples-of-complex-queries"></a>예제

다음 예제에서는 쿼리를 정확 하 게 원하는 항목 찾으려고 구체화할 수는 방법을 설명 하기 위해 다른 중요 한 형식, 속성 및 연산자를 사용 합니다.
  
|**쿼리**|**설명**|
|:-----|:-----|
| `SensitiveType:"International Banking Account Number (IBAN)"` <br/> |너무 오래, 있지만 것이 중요 한 해당 형식에 대 한 올바른 이름 때문에 이름 이상한 것 처럼 보일 수 있습니다. [중요 한 정보 유형 목록](https://go.microsoft.com/fwlink/?LinkID=509999)에서 정확 하 게 이름을 사용할 수 있는지 확인 합니다. 또한 조직에 대해 만든 [사용자 지정 중요 한 정보 유형](create-a-custom-sensitive-information-type.md) 이름을 사용할 수 있습니다.<br/> |
| ' SensitiveType: "신용 카드 번호|1..4294967295|1..100"' <br/> |하나 이상의 일치를 사용 하 여 문서 "신용 카드 번호입니다." 중요 한 형식으로 반환 각 범위에 대 한 값은 해당 최소 및 최대 값입니다. 이 쿼리를 작성 하는 간단한 방법은 `SensitiveType:"Credit Card Number"`, 하지만 재미 있는?<br/> |
| ' SensitiveType: "신용 카드 번호| LastSensitiveContentScan:"8/11/2018..8/13/2018 및 5..25" "' <br/> |이 2018 년 8 월 13를 통해 2018 년 8 월 11에서 검색 된 5-25 신용 카드 번호를 사용 하 여 문서를 반환 합니다.  <br/> |
| ' SensitiveType: "신용 카드 번호| LastSensitiveContentScan:"8/11/2018..8/13/2018 및 5..25" "하지 FileExtension:XLSX' <br/> |이 2018 년 8 월 13를 통해 2018 년 8 월 11에서 검색 된 5-25 신용 카드 번호를 사용 하 여 문서를 반환 합니다. XLSX 확장명을 가진 파일 쿼리 결과에 포함 되지 않습니다.  `FileExtension` 쿼리를 포함할 수 있는 많은 속성 중 하나입니다. 자세한 내용은 [검색 속성을 사용 하 고 eDiscovery 사용 하 여 연산을](https://go.microsoft.com/fwlink/?LinkId=510093)참조 하십시오.<br/> |
| `SensitiveType:"Credit Card Number" OR SensitiveType:"U.S. Social Security Number (SSN)"` <br/> |이 쿼리는 신용 카드 번호 또는 사회 보장 번호가 포함된 문서를 반환합니다.  <br/> |
   
## <a name="examples-of-queries-to-avoid"></a>예제

모든 쿼리에 같은 만들어집니다. 다음 표에서 DLP SharePoint에 대 한 작동 하지 않는 쿼리의 예제를 제공 하 고 이유를 설명 합니다.
  
|**지원되지 않는 쿼리**|**이유**|
|:-----|:-----|
| ' SensitiveType: "신용 카드 번호|.." ` <br/> |하나 이상의 숫자를 추가해야 합니다.  <br/> |
| `SensitiveType:"NotARule"` <br/> |"NotARule" 형식의 유효한 중요 한 유형 이름 없습니다. [중요 한 정보 유형 목록](https://go.microsoft.com/fwlink/?LinkID=509999) 에서 이름만 DLP 쿼리에서 작동 합니다.<br/> |
| ' SensitiveType: "신용 카드 번호|0"' <br/> |0으로 최소값 또는 최대값 범위 내에서 유효 하지 않습니다.  <br/> |
| `SensitiveType:"Credit Card Number"` <br/> |것을 확인 하는 것이 어려울 수 이지만 "신용" 및 "카드" 잘못 된 쿼리 하는 사이의 공백을 합니다. [중요 한 정보 유형 목록](https://go.microsoft.com/fwlink/?LinkID=509999)에서 정확 하 게 중요 한 형식 이름을 사용 합니다.<br/> |
| ' SensitiveType: "신용 카드 번호|1.. 3"' <br/> |2 구간 부분을 구분 하 여 공백으로 하면 안됩니다.  <br/> |
| ' SensitiveType: "신용 카드 번호| |1.|80.."' <br/> |너무 많은 파이프 구분 기호 (가지|). 대신 다음과 같은이 형식: ' SensitiveType: "신용 카드 번호|1.|80.."' <br/> |
| ' SensitiveType: "신용 카드 번호|1.|80..101"' <br/> |Confidence 값을 백분율로 나타내므로 100을 초과할 수 없습니다. 대신 1에서 100 사이의 숫자를 선택 합니다.  <br/> |
   
## <a name="for-more-information"></a>자세한 내용

[중요한 정보 유형이 찾는 항목](what-the-sensitive-information-types-look-for.md)
  
[콘텐츠 검색을 실행 하는 Office 365 보안에서 &amp; 준수 센터](run-a-content-search-in-the-security-and-compliance-center.md)
  
[콘텐츠 검색에 대한 키워드 쿼리 및 검색 조건](keyword-queries-and-search-conditions.md)
  

