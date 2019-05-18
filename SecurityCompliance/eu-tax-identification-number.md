---
title: EU 세금 확인 번호
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 8/17/2018
audience: Admin
ms.topic: reference
ms.service: O365-seccomp
ms.collection: M365-security-compliance
localization_priority: Normal
description: 이 항목에서는 EU 세금 식별 번호 중요 정보 유형을 검색할 때 DLP (데이터 손실 방지) 정책이 어떤 역할을 검색 하나요를 보여 줍니다. 이 중요 한 정보 유형은 각 국가에 대 한 다양 한 패턴, 키워드 및 기타 증거를 정의 합니다.
ms.openlocfilehash: adcd9be9b5f8775ad39010d771ff2ac214df1e17
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/17/2019
ms.locfileid: "34152960"
---
# <a name="eu-tax-identification-number"></a>EU 세금 확인 번호

이 항목에서는 언급 (데이터 손실 방지) 정책이 EU (유럽 세금 식별 번호) 중요 한 정보 유형을 검색할 때 찾는 항목을 보여 줍니다. 이 중요 한 정보 유형은 각 국가에 대 한 다양 한 패턴, 키워드 및 기타 증거를 정의 합니다.
  
## <a name="austria"></a>오스트리아

### <a name="format"></a>형식일

하이픈 및 슬래시가 있는 9 자리 숫자
  
### <a name="pattern"></a>패턴

하이픈 및 슬래시가 있는 9 자리 숫자:
  
-  2자리 숫자 
    
- 하이픈 1개(선택 사항)
    
- 3자리 숫자
    
- 정방향 슬래시 1개(선택 사항)
    
- 4자리 숫자
    
### <a name="checksum"></a>제외

예
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.
  
- 이 함수 `Func_austria_eu_tax_file_number` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- From `Keywords_austria_eu_tax_file_number` 키워드를 찾았습니다. 
    
DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 이 함수 `Func_austria_eu_tax_file_number` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_austria_eu_tax_file_number" />
          <Match idRef="Keywords_austria_eu_tax_file_number" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_austria_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>키워드

#### <a name="keywordsaustriaeutaxfilenumber"></a>Keywords_austria_eu_tax_file_number

세금 번호
  
수
  
세금 등록 번호
  
tax id
  
st.nr
  
steuernummer
  
## <a name="belgium"></a>벨기에

### <a name="format"></a>형식일

공백과 구분 기호를 사용 하지 않고 11 자리 숫자
  
### <a name="pattern"></a>패턴

11자리 숫자:
  
- 2자리 숫자
    
- "0" 또는 "1"
    
- 1자리 숫자
    
- "0" 또는 "1" 또는 "2" 또는 "3" 
    
- 6자리 숫자
    
### <a name="checksum"></a>제외

해당 사항 없음
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 정규식이 해당 `Regex_belgium_eu_tax_file_number` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- From `Keywords_belgium_eu_tax_file_number` 키워드를 찾았습니다. 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_belgium_eu_tax_file_number" />
          <Match idRef="Keywords_belgium_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>키워드

#### <a name="keywordsbelgiumeutaxfilenumber"></a>Keywords_belgium_eu_tax_file_number

세금 번호
  
국가 등록 번호
  
세금 등록 번호
  
tax id
  
m
  
m
  
numéro de registre 국립
  
numéro d'identification fiscale
  
## <a name="bulgaria"></a>불가리아

### <a name="format"></a>형식일

공백과 구분 기호가 없는 10 자리 숫자
  
### <a name="pattern"></a>패턴

10자리 숫자
  
### <a name="checksum"></a>제외

예
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.
  
- 이 함수 `Func_bulgaria_eu_tax_file_number` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- From `Keywords_bulgaria_eu_tax_file_number` 키워드를 찾았습니다. 
    
DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 이 함수 `Func_bulgaria_eu_tax_file_number` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_bulgaria_eu_tax_file_number" />
          <Match idRef="Keywords_bulgaria_eu_tax_file_number" />
        </Pattern>
 <Pattern confidenceLevel="75">
          <IdMatch idRef="Func_bulgaria_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>키워드

#### <a name="keywordsbulgariaeutaxfilenumber"></a>Keywords_bulgaria_eu_tax_file_number

고 대 cn
  
일관적인 민사 번호
  
과 (와) cn #
  
uniformcivilnumber#
  
일정 한 민사 일련번호
  
일관적인 민사
  
egn
  
불가리아어 (민사)
  
uniformcivilno#
  
egn#
  
униформ граждански номер
  
униформ id
  
униформ граждански id
  
униформ граждански не
  
## <a name="croatia"></a>크로아티아

### <a name="format"></a>형식일

공백이 나 구분 기호가 없는 11 자리 숫자
  
### <a name="pattern"></a>패턴

11자리 숫자:
  
- 임의로 선택한 10 자리 숫자
    
- 검사 숫자 1 개
    
### <a name="checksum"></a>제외

예
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.
  
- 이 함수 `Func_croatia_eu_tax_file_number` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- From `Keywords_croatia_eu_tax_file_number` 키워드를 찾았습니다. 
    
DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 이 함수 `Func_croatia_eu_tax_file_number` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_croatia_eu_tax_file_number" />
          <Match idRef="Keywords_croatia_eu_tax_file_number" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_croatia_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>키워드

#### <a name="keywordscroatiaeutaxfilenumber"></a>Keywords_croatia_eu_tax_file_number

세금 번호
  
세금
  
tax id
  
원환형
  
원환형
  
porezni broj
  
## <a name="cyprus"></a>키프로스

### <a name="format"></a>형식일

지정 된 패턴에서 8 자리 및 1 개 문자
  
### <a name="pattern"></a>패턴

8 자리 숫자와 1 개 문자:
  
-  "0" 
    
- 7자리 숫자
    
- 1 개 문자 (대/소문자 구분 안 함)
    
### <a name="checksum"></a>제외

해당 사항 없음
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.
  
- 이 함수 `Func_cyprus_eu_tax_file_number` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- From `Keywords_cyprus_eu_tax_file_number` 키워드를 찾았습니다. 
    
DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 이 함수 `Func_cyprus_eu_tax_file_number` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_cyprus_eu_tax_file_number" />
          <Match idRef="Keywords_cyprus_eu_tax_file_number" />
        </Pattern>
Pattern confidenceLevel="75">
          <IdMatch idRef="Func_cyprus_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>키워드

#### <a name="keywordscypruseutaxfilenumber"></a>Keywords_cyprus_eu_tax_file_number

세금 번호
  
세금
  
tax id
  
세금 식별 코드
  
tic
  
tic#
  
αριθμός φορολογικού μητρώου
  
φορολογική ταυτότητα
  
κωδικός φορολογικού μητρώου
  
## <a name="czech-republic"></a>체코 공화국

### <a name="format"></a>형식일

선택적 백슬래시가 있는 9 자리 또는 10 진수
  
### <a name="pattern"></a>패턴

선택적 backslashl이 있는 아홉 자리 숫자
  
- 6자리 숫자 
    
- 백슬래시 (선택 사항)
    
- 3 ~ 4 자리 숫자
    
### <a name="checksum"></a>제외

해당 사항 없음
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 정규식이 해당 `Regex_czech_republic_eu_tax_file_number` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- From `Keywords_czech_republic_eu_tax_file_number` 키워드를 찾았습니다. 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_czech_republic_eu_tax_file_number" />
          <Match idRef="Keywords_czech_republic_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>키워드

#### <a name="keywordsczechrepubliceutaxfilenumber"></a>Keywords_czech_republic_eu_tax_file_number

세금 번호
  
세금
  
tax id
  
개인 번호
  
daňové číslo
  
osobní číslo
  
## <a name="denmark"></a>덴마크

### <a name="format"></a>형식일

하이픈을 포함 하는 10 자리 숫자
  
### <a name="pattern"></a>패턴

Hyphenl를 포함 하는 10 자리 숫자:
  
-  생년월일에 해당 하는 6 자리 숫자 (DDMMYY) 
    
- 하이픈
    
- 첫 번째 숫자가 출생 세기에 해당 하 고 마지막 숫자가 개별 성별에 해당 하는 시퀀스 번호에 해당 하는 4 자리 숫자 (남성의 경우 홀수 및 암에도 해당)
    
### <a name="checksum"></a>제외

예
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.
  
- 이 함수 `Func_denmark_eu_tax_file_number` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- From `Keywords_denmark_eu_tax_file_number` 키워드를 찾았습니다. 
    
DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 이 함수 `Func_denmark_eu_tax_file_number` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_denmark_eu_tax_file_number" />
          <Match idRef="Keywords_denmark_eu_tax_file_number" />
        </Pattern> 
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_denmark_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>키워드

#### <a name="keywordsdenmarkeutaxfilenumber"></a>Keywords_denmark_eu_tax_file_number

세금 번호
  
세금
  
tax id
  
cpr 번호
  
cpr#
  
nummer에서
  
번호 (|)
  
## <a name="estonia"></a>에스토니아

### <a name="format"></a>형식일

공백이 나 구분 기호가 없는 11 자리 숫자
  
### <a name="pattern"></a>패턴

11자리 숫자:
  
-  성별에 해당 하는 숫자와 홀수로 해당 하 고, 홀수를 지정 하 여 19th 세기에 대해 1, 2를 나타내는 숫자입니다. 3, 20th 세기에 대해 4를 적용 합니다. 21 세기에 대해 5, 6 
    
- 생년월일에 해당 하는 6 자리 숫자 (YYMMDD)
    
- 같은 날짜에 태어난 사람을 구분 하는 일련 번호에 해당 하는 3 자리 숫자
    
- 검사 숫자 1 개
    
### <a name="checksum"></a>제외

예
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.
  
- 이 함수 `Func_estonia_eu_tax_file_number` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- From `Keywords_estonia_eu_tax_file_number` 키워드를 찾았습니다. 
    
DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 이 함수 `Func_estonia_eu_tax_file_number` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_estonia_eu_tax_file_number" />
          <Match idRef="Keywords_estonia_eu_tax_file_number" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_estonia_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>키워드

#### <a name="keywordsestoniaeutaxfilenumber"></a>Keywords_estonia_eu_tax_file_number

세금 번호
  
세금
  
tax id
  
개인 코드
  
maksunumber
  
maksu id
  
isikukood
  
## <a name="finland"></a>핀란드

### <a name="format"></a>형식일

숫자, 문자, 더하기 및 빼기 기호를 11 문자로 조합
  
### <a name="pattern"></a>패턴

숫자, 문자, 더하기 및 빼기 기호를 11 문자로 조합한 것입니다.
  
- 6자리 숫자
    
- 더하기 기호, 빼기 기호 또는 + 기호가 1800-1899 사이에 태어난 것을 의미 하는 "A" (대/소문자 구분 안 함), 빼기 기호는 1900-1999 사이에 출생를 의미 하며 "A"는 "A"를 2000 의미 합니다.
    
- 3자리 숫자
    
- 1 개의 문자 또는 한 자리 숫자
    
### <a name="checksum"></a>제외

예
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.
  
- 이 함수 `Func_finland_eu_tax_file_number` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- From `Keywords_finland_eu_tax_file_number` 키워드를 찾았습니다. 
    
DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 이 함수 `Func_finland_eu_tax_file_number` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_finland_eu_tax_file_number" />
          <Match idRef="Keywords_finland_eu_tax_file_number" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_finland_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>키워드

#### <a name="keywordsfinlandeutaxfilenumber"></a>Keywords_finland_eu_tax_file_number

identification number
  
개인 id
  
id 번호
  
핀란드어 국가 id 번호
  
personalidnumber#
  
national identification number
  
id 번호
  
국가 id 번호입니다.
  
국가 id 번호
  
id 없음
  
tunnistenumero
  
henkilötunnus
  
yksilöllinen henkilökohtainen tunnistenumero
  
ainutlaatuinen henkilökohtainen tunnus
  
identiteetti numero
  
suomen kansallinen henkilötunnus
  
henkilötunnusnumero#
  
kansallisen tunnistenumero
  
tunnusnumero
  
kansallinen tunnus numero
  
## <a name="france"></a>프랑스

### <a name="format"></a>형식일

개별 사용자의 경우 13 자리 숫자 및 엔터티의 경우 9 자리 숫자
  
### <a name="pattern"></a>패턴

개별 사용자에 대 한 13 자리 숫자:
  
- 0, 1, 2 또는 3 이어야 하는 1 자리 숫자
    
- 12자리 숫자
    
엔터티의 9 자리 숫자
  
### <a name="checksum"></a>제외

해당 사항 없음
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.
  
- 이 함수 `Func_france_eu_tax_file_number` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- From `Keywords_france_eu_tax_file_number` 키워드를 찾았습니다. 
    
DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 이 함수 `Func_france_eu_tax_file_number` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_france_eu_tax_file_number" />
          <Match idRef="Keywords_france_eu_tax_file_number" />
        </Pattern>
 <Pattern confidenceLevel="75">
          <IdMatch idRef="Func_france_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>키워드

#### <a name="keywordsfranceeutaxfilenumber"></a>Keywords_france_eu_tax_file_number

세금 식별 번호
  
세금 번호
  
tax id
  
numéro d'identification fiscale
  
## <a name="germany"></a>독일

### <a name="format"></a>형식일

공백과 구분 기호를 사용 하지 않고 11 자리 숫자
  
### <a name="pattern"></a>패턴

11 자리 숫자:
  
-  10 자리 숫자 
    
- 검사 숫자 1 개
    
### <a name="checksum"></a>제외

예
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.
  
- 이 함수 `Func_germany_eu_tax_file_number` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- From `Keywords_germany_eu_tax_file_number` 키워드를 찾았습니다. 
    
DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 이 함수 `Func_germany_eu_tax_file_number` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_germany_eu_tax_file_number" />
          <Match idRef="Keywords_germany_eu_tax_file_number" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_germany_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>키워드

#### <a name="keywordsgermanyeutaxfilenumber"></a>Keywords_germany_eu_tax_file_number

세금 번호
  
세금 번호
  
taxno#
  
taxnumber#
  
taxnumber
  
tax id
  
taxid#
  
세금 식별 번호
  
세금 식별 번호
  
steuernummer
  
steuer id
  
steueridentifikationsnummer
  
## <a name="greece"></a>그리스

### <a name="format"></a>형식일

공백과 구분 기호를 사용 하지 않고 9 자리 숫자
  
### <a name="pattern"></a>패턴

9자리 숫자
  
### <a name="checksum"></a>제외

해당 사항 없음
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 정규식이 해당 `Regex_greece_eu_tax_file_number` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- From `Keywords_greece_eu_tax_file_number` 키워드를 찾았습니다. 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_greece_eu_tax_file_number" />
          <Match idRef="Keywords_greece_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>키워드

#### <a name="keywordsgreeceeutaxfilenumber"></a>Keywords_greece_eu_tax_file_number

afm
  
언급
  
세금 번호 번호
  
세금 번호 없음
  
세금 식별 번호
  
세금 레지스트리 번호
  
세금 레지스트리 번호
  
afm #
  
언급
  
taxidno#
  
taxregistryno#
  
αριθμός φορολογικού μητρώου
  
aφμ
  
aφμ αριθμός
  
φορολογικού μητρώου νο.
  
τον αριθμό φορολογικού μητρώου
  
## <a name="hungary"></a>헝가리

### <a name="format"></a>형식일

공백이 나 구분 기호가 없는 10 자리 숫자
  
### <a name="pattern"></a>패턴

10 자리 숫자:
  
-  "8" 이어야 하는 1 자리 숫자 
    
- 날짜 01/01/1867과 개별 생년월일 사이의 일 수에 해당 하는 5 자리 숫자입니다.
    
- 같은 날에 태어난 사람을 구별 하기 위해 기회가 만든 번호에 해당 하는 3 자리 숫자
    
- 검사 숫자 1 개
    
### <a name="checksum"></a>제외

예
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.
  
- 이 함수 `Func_hungary_eu_tax_file_number` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- From `Keywords_hungary_eu_tax_file_number` 키워드를 찾았습니다. 
    
DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 이 함수 `Func_hungary_eu_tax_file_number` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_hungary_eu_tax_file_number" />
          <Match idRef="Keywords_hungary_eu_tax_file_number" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_hungary_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>키워드

#### <a name="keywordshungaryeutaxfilenumber"></a>Keywords_hungary_eu_tax_file_number

헝가리어 세금 식별 번호
  
헝가리어 언급
  
세금 id 번호
  
vat 번호
  
세금 기관 아니요
  
세금 id 세금 id 번호
  
taxidnumber#
  
언급
  
hungatiantin#
  
세금 식별 아니요
  
taxidno#
  
adóazonosító szám
  
adószám
  
adóhatóság szám
  
## <a name="ireland"></a>Ireland

### <a name="format"></a>형식일

공백 또는 구분 기호가 없는 7 자리 숫자와 문자
  
### <a name="pattern"></a>패턴

7 자리 숫자와 문자
  
-  7자리 숫자 
    
- 1 개 문자 (대/소문자 구분 안 함)
    
### <a name="checksum"></a>제외

해당 사항 없음
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.
  
- 이 함수 `Func_ireland_eu_tax_file_number` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- From `Keywords_ireland_eu_tax_file_number` 키워드를 찾았습니다. 
    
DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 이 함수 `Func_ireland_eu_tax_file_number` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_ireland_eu_tax_file_number" />
          <Match idRef="Keywords_ireland_eu_tax_file_number" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_ireland_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>키워드

#### <a name="keywordsirelandeutaxfilenumber"></a>Keywords_ireland_eu_tax_file_number

공용 서비스 없음
  
개인 공용 서비스 없음
  
pps 아니요
  
개인 서비스 없음
  
pps 서비스 없음
  
ppsno#
  
아일랜드 pps 아니요
  
publicserviceno#
  
개인 공용 서비스 번호
  
uimhir phearsanta seirbhíse poiblí
  
pps uimh
  
uimhir aitheantais phearsanta
  
## <a name="italy"></a>이탈리아

### <a name="format"></a>형식일

지정 된 패턴의 문자와 숫자 16 개
  
### <a name="pattern"></a>패턴

16 자의 문자 및 숫자:
  
-  가족 이름에서 처음 세 개의 자음에 해당 하는 3 개의 문자 
    
- 이름의 첫 번째, 세 번째 및 네 번째 자음에 해당 하는 3 개의 문자
    
- 출생 연도의 마지막 자리에 해당 하는 2 자리 숫자
    
- 출생 달에 해당 하는 1 자리 숫자는 알파벳 순으로 사용 되지만 A에서 E, H, L, M, P, R에 해당 하는 문자만 사용 되며, 따라서 1 월은 A와 10 월이 됩니다.
    
- 남성의와 구별 하기 위해 여성의 경우 짝수에서 출생 일에 40이 추가 되는 출생 달의 날짜에 해당 하는 2 자리 숫자
    
- 사용자가 태어난 municipality 관련 지역 번호에 해당 하는 4 자리 숫자-국가 전체 코드를 외국 국가에 사용 합니다.
    
- 검사 숫자 1 개
    
### <a name="checksum"></a>제외

예
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.
  
- 이 함수 `Func_italy_eu_tax_file_number` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- From `Keywords_italy_eu_tax_file_number` 키워드를 찾았습니다. 
    
DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 이 함수 `Func_italy_eu_tax_file_number` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_italy_eu_tax_file_number" />
          <Match idRef="Keywords_italy_eu_tax_file_number" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_italy_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>키워드

#### <a name="keywordsitalyeutaxfilenumber"></a>Keywords_italy_eu_tax_file_number

세금 번호
  
세금 번호
  
taxno#
  
taxnumber#
  
taxnumber
  
tax id
  
taxid#
  
회계 코드
  
codice
  
## <a name="latvia"></a>라트비아

### <a name="format"></a>형식일

공백이 나 구분 기호가 없는 11 자리 숫자
  
### <a name="pattern"></a>패턴

지정 된 패턴에서 11 자리 숫자
  
-  출생 날짜에 해당 하는 6 자리 숫자 (DDMMYY) 
    
- 출생 세기에 해당 하는 1 자리 숫자 이며, "0"은 19th 세기에 해당 하 고 "1"은 20th 세기에 해당 하며 21 세기에 해당 합니다.
    
- 4자리 숫자
    
### <a name="checksum"></a>제외

예
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.
  
- 이 함수 `Func_latvia_eu_tax_file_number` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- From `Keywords_latvia_eu_tax_file_number` 키워드를 찾았습니다. 
    
DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 이 함수 `Func_latvia_eu_tax_file_number` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_latvia_eu_tax_file_number" />
          <Match idRef="Keywords_latvia_eu_tax_file_number" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_latvia_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>키워드

#### <a name="keywordslatviaeutaxfilenumber"></a>Keywords_latvia_eu_tax_file_number

세금 번호
  
세금 번호
  
taxno#
  
taxnumber#
  
taxnumber
  
tax id
  
taxid#
  
세금 식별 번호
  
세금 식별 번호
  
nodokļa numurs
  
nodokļu identifikācijas numurs
  
nodokļu identifikācija numurs
  
## <a name="lithuania"></a>리투아니아

### <a name="format"></a>형식일

공백이 나 구분 기호가 없는 11 자리 숫자
  
### <a name="pattern"></a>패턴

11자리 숫자
  
### <a name="checksum"></a>제외

해당 사항 없음
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.
  
- 이 함수 `Func_lithuania_eu_tax_file_number` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- From `Keywords_lithuania_eu_tax_file_number` 키워드를 찾았습니다. 
    
DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 이 함수 `Func_lithuania_eu_tax_file_number` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_lithuania_eu_tax_file_number" />
          <Match idRef="Keywords_lithuania_eu_tax_file_number" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_lithuania_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>키워드

#### <a name="keywordslithuaniaeutaxfilenumber"></a>Keywords_lithuania_eu_tax_file_number

세금 번호
  
세금 번호
  
세금 없음 #
  
taxnumber#
  
taxnumber
  
tax id
  
taxid#
  
세금 식별 번호
  
세금 식별 번호
  
mokesčių id
  
mokesčių numeris
  
mokesčių identifikavimas numeris
  
## <a name="luxemburg"></a>셈

### <a name="format"></a>형식일

공백이 나 구분 기호가 없는 13 자리 숫자
  
### <a name="pattern"></a>패턴

13자리 숫자:
  
-  11자리 숫자 
    
- 2개의 검사 숫자
    
### <a name="checksum"></a>제외

예
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.
  
- 이 함수 `Func_luxemburg_eu_tax_file_number` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- From `Keywords_luxemburg_eu_tax_file_number` 키워드를 찾았습니다. 
    
DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 이 함수 `Func_luxemburg_eu_tax_file_number` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_luxemburg_eu_tax_file_number" />
          <Match idRef="Keywords_luxemburg_eu_tax_file_number" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_luxemburg_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>키워드

#### <a name="keywordsluxemburgeutaxfilenumber"></a>Keywords_luxemburg_eu_tax_file_number

세금 번호
  
세금 번호
  
taxno#
  
taxnumber#
  
taxnumber
  
tax id
  
taxid#
  
세금 식별 번호
  
세금 식별 번호
  
steuernummer
  
steuer id
  
steueridentifikationsnummer
  
## <a name="malta"></a>몰타

### <a name="format"></a>형식일

몰타어 nationals의 경우 지정 된 패턴의 7 자리 및 한 문자
  
몰타어 이외의 nationals 및 몰타어 엔터티: 9 자리 숫자
  
### <a name="pattern"></a>패턴

몰타어 nationals: 7 자리 숫자 및 1 개 문자
  
-  7자리 숫자 
    
- 1 개 문자 (대/소문자 구분 안 함)
    
몰타어 이외의 nationals 및 몰타어 엔터티: 9 자리 숫자
  
-  9자리 숫자 
    
### <a name="checksum"></a>제외

해당 사항 없음
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 이 함수 `Func_malta_eu_tax_file_number` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- From `Keywords_malta_eu_tax_file_number` 키워드를 찾았습니다. 
    
DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 65% 신뢰합니다.
  
- 이 함수 `Func_malta_eu_tax_file_number` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Func_malta_eu_tax_file_number" />
          <Match idRef="Keywords_malta_eu_tax_file_number" />
        </Pattern>
<Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_malta_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>키워드

#### <a name="keywordsmaltaeutaxfilenumber"></a>Keywords_malta_eu_tax_file_number

세금 번호
  
세금 번호
  
taxno#
  
taxnumber#
  
taxnumber
  
tax id
  
taxid#
  
세금 식별 번호
  
세금 식별 번호
  
numru tat
  
id tat-taxxa
  
numru ta ' taxxa
  
## <a name="netherlands"></a>네덜란드

### <a name="format"></a>형식일

공백이 나 구분 기호가 없는 9 자리 숫자
  
### <a name="pattern"></a>패턴

9자리 숫자 
  
### <a name="checksum"></a>제외

예
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.
  
- 이 함수 `Func_netherlands_eu_tax_file_number` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- From `Keywords_netherlands_eu_tax_file_number` 키워드를 찾았습니다. 
    
DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 이 함수 `Func_netherlands_eu_tax_file_number` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_netherlands_eu_tax_file_number" />
          <Match idRef="Keywords_netherlands_eu_tax_file_number" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_netherlands_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>키워드

#### <a name="keywordsnetherlandseutaxfilenumber"></a>Keywords_netherlands_eu_tax_file_number

네덜란드 세금 식별 번호
  
네덜란드 세금 식별
  
netherland의 세금 식별 번호
  
netherland의 세금 식별
  
세금 식별 번호
  
네덜란드어 세금 번호
  
네덜란드어 세금 식별 번호
  
tax id
  
세금 id #
  
세금 번호
  
세금 없음 #
  
세금
  
언급
  
언급
  
네덜란드 언급
  
netherland의 언급
  
nederlands belasting identificatienummer
  
identificatienummer van belasting
  
identificatienummer belasting
  
nederlands belasting identificatie
  
nederlands belasting id nummer
  
nederlands belastingnummer
  
btw nummer
  
nederlandse belasting identificatie
  
## <a name="poland"></a>폴란드

### <a name="format"></a>형식일

공백이 나 구분 기호가 없는 11 자리 숫자
  
### <a name="pattern"></a>패턴

11 자리 숫자
  
### <a name="checksum"></a>제외

예
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.
  
- 이 함수 `Func_poland_eu_tax_file_number` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- From `Keywords_poland_eu_tax_file_number` 키워드를 찾았습니다. 
    
DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 이 함수 `Func_poland_eu_tax_file_number` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_poland_eu_tax_file_number" />
          <Match idRef="Keywords_poland_eu_tax_file_number" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_poland_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>키워드

#### <a name="keywordspolandeutaxfilenumber"></a>Keywords_poland_eu_tax_file_number

세금 번호
  
세금 번호
  
taxno#
  
taxnumber#
  
taxnumber
  
nip
  
nip#
  
tax id
  
세금 id #
  
nip id
  
nip id #
  
세금 식별 번호
  
세금 식별 번호
  
vat 번호
  
vat 번호
  
vatno#
  
vat id
  
vat id #
  
u r i identyfikacji podatkowej
  
정책 스키 u r i identyfikacji podatkowej
  
numeridentyfikacjipodatkowej#
  
## <a name="portugal"></a>포르투갈

### <a name="format"></a>형식일

공백이 나 구분 기호가 없는 9 자리 숫자
  
### <a name="pattern"></a>패턴

9자리 숫자
  
### <a name="checksum"></a>제외

예
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.
  
- 이 함수 `Func_portugal_eu_tax_file_number` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- From `Keywords_portugal_eu_tax_file_number` 키워드를 찾았습니다. 
    
DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 이 함수 `Func_portugal_eu_tax_file_number` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_portugal_eu_tax_file_number" />
          <Match idRef="Keywords_portugal_eu_tax_file_number" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_portugal_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>키워드

#### <a name="keywordsportugaleutaxfilenumber"></a>Keywords_portugal_eu_tax_file_number

세금 번호
  
세금 번호
  
taxno#
  
taxnumber#
  
taxnumber
  
m
  
m
  
numero 회계
  
número de identificação 회계
  
## <a name="romania"></a>루마니아

### <a name="format"></a>형식일

공백이 나 구분 기호가 없는 13 자리 숫자
  
### <a name="pattern"></a>패턴

13자리 숫자
  
### <a name="checksum"></a>제외

해당 사항 없음
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 정규식이 해당 `Regex_romania_eu_tax_file_number` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- From `Keywords_romania_eu_tax_file_number` 키워드를 찾았습니다. 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_romania_eu_tax_file_number" />
          <Match idRef="Keywords_romania_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>키워드

#### <a name="keywordsromaniaeutaxfilenumber"></a>Keywords_romania_eu_tax_file_number

tax id
  
세금 id 번호
  
세금 파일 번호
  
tax file number
  
세금 없음
  
세금 번호
  
taxid#
  
taxno#
  
id-ul taxei
  
numărul de identificare fiscală
  
## <a name="slovakia"></a>슬로바키아

### <a name="format"></a>형식일

공백이 나 구분 기호가 없는 10 자리 숫자
  
### <a name="pattern"></a>패턴

10자리 숫자
  
### <a name="checksum"></a>제외

해당 사항 없음
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 정규식이 해당 `Regex_slovakia_eu_tax_file_number` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- From `Keywords_slovakia_eu_tax_file_number` 키워드를 찾았습니다. 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_slovakia_eu_tax_file_number" />
          <Match idRef="Keywords_slovakia_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>키워드

#### <a name="keywordsslovakiaeutaxfilenumber"></a>Keywords_slovakia_eu_tax_file_number

tax id
  
세금 id 번호
  
언급 id
  
언급 아니요
  
슬로바키아어 언급 id
  
언급
  
세금 파일 번호
  
tax file number
  
세금 없음
  
세금 번호
  
taxid#
  
taxno#
  
daňové identifikačné číslo
  
daňové číslo
  
daňové číslo súboru
  
## <a name="slovenia"></a>슬로베니아

### <a name="format"></a>형식일

공백이 나 구분 기호가 없는 8 자리 숫자
  
### <a name="pattern"></a>패턴

8자리 숫자
  
### <a name="checksum"></a>제외

예
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.
  
- 이 함수 `Func_slovenia_eu_tax_file_number` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- From `Keywords_slovenia_eu_tax_file_number` 키워드를 찾았습니다. 
    
DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 이 함수 `Func_slovenia_eu_tax_file_number` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_nation_eu_tax_file_number" />
          <Match idRef="Keywords_nation_eu_tax_file_number" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_slovenia_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>키워드

#### <a name="keywordssloveniaeutaxfilenumber"></a>Keywords_slovenia_eu_tax_file_number

tax id
  
세금 id 번호
  
언급 id
  
언급 아니요
  
슬로베니아어 언급 id
  
언급
  
세금 파일 번호
  
tax file number
  
세금 없음
  
세금 번호
  
taxid#
  
taxno#
  
identifikacijska številka davka
  
davčna številka
  
številka davčne datoteke
  
## <a name="spain"></a>스페인

### <a name="format"></a>형식일

지정 된 패턴에 7 ~ 8 자리 숫자와 한 가지 또는 두 개의 문자가 있습니다.
  
### <a name="pattern"></a>패턴

스페인 국내 Id 카드가 있는 스페인어 (자연 사용자):
  
-  8자리 숫자 
    
- 대문자 1 개 (대/소문자 구분) 
    
스페인 국가 Id 카드가 없는 상주 하지 않는 Spaniards
  
- 1 개의 대문자 "L" (대/소문자 구분)
    
- 7자리 숫자
    
- 대문자 1 개 (대/소문자 구분) 
    
스페인 국가 Id 카드를 사용 하지 않고 14 년 동안 상주 하는 Spaniards:
  
- 1 개의 대문자 "K" (대/소문자 구분)
    
-  7자리 숫자 
    
- 대문자 1 개 (대/소문자 구분)
    
Foreigner의 식별 번호를 사용 하는 Foreigners
  
- "X", "Y" 또는 "Z" (대/소문자 구분)의 대문자 1 개 
    
- 7자리 숫자
    
- 대문자 1 개 (대/소문자 구분) 
    
Foreigner의 Id 번호가 없는 Foreigners
  
- "M"을 나타내는 대문자 1 개 (대/소문자 구분) 
    
- 7자리 숫자
    
- 대문자 1 개 (대/소문자 구분) 
    
### <a name="checksum"></a>제외

예
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.
  
- 이 함수 `Func_spain_eu_tax_file_number` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- From `Keywords_spain_eu_tax_file_number` 키워드를 찾았습니다. 
    
DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 이 함수 `Func_spain_eu_tax_file_number` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_spain_eu_tax_file_number" />
          <Match idRef="Keywords_spain_eu_tax_file_number" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_spain_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>키워드

#### <a name="keywordsspaineutaxfilenumber"></a>Keywords_spain_eu_tax_file_number

tax id
  
세금 id 번호
  
cif id
  
cif 아니요
  
스페인어 cif id
  
cif
  
세금 파일 번호
  
스페인어 cif 번호
  
tax file number
  
스페인어 cif 아니요
  
세금 없음
  
세금 번호
  
taxid#
  
taxno#
  
cifid #
  
spanishcifid#
  
spanishcifno#
  
número de contribuyente
  
número de impuesto corporativo
  
número de identificación 회계
  
cif número
  
cifnúmero#
  
## <a name="sweden"></a>스웨덴

### <a name="format"></a>형식일

지정 된 패턴의 10 자리 숫자와 기호
  
### <a name="pattern"></a>패턴

10 자리 숫자와 기호:
  
-  생년월일에 해당 하는 6 자리 숫자 (YYMMDD) 
    
- 더하기 기호, 빼기 기호 또는 백슬래시
    
- 다음은 식별 번호를 고유 하 게 만드는 3 자리 숫자입니다. 
    
  - 1990 이전에 실행 된 번호의 경우 일곱째 및 여덟 번째 숫자는 출생 또는 외부에서 태어난 사람의 국가를 식별 합니다.
    
  - 아홉 번째 위치의 숫자는 성별에 대 한 홀수 또는 암도를 나타냅니다.
    
- 검사 숫자 1 개
    
### <a name="checksum"></a>제외

예
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.
  
- 이 함수 `Func_sweden_eu_tax_file_number` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- From `Keywords_sweden_eu_tax_file_number` 키워드를 찾았습니다. 
    
DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 이 함수 `Func_sweden_eu_tax_file_number` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_sweden_eu_tax_file_number" />
          <Match idRef="Keywords_sweden_eu_tax_file_number" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_sweden_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>키워드

#### <a name="keywordsswedeneutaxfilenumber"></a>Keywords_sweden_eu_tax_file_number

tax id
  
세금 번호 번호
  
세금 id 번호
  
tax identification
  
세금 식별 번호
  
세금 번호
  
세금
  
taxid#
  
세금 파일
  
세금 파일 번호
  
개인 id 번호
  
(nummer at&t id)
  
identifikation at&t
  
personnummer
  
## <a name="uk"></a>영국의

### <a name="format"></a>형식일

UTR (Unique Taxpayer Reference): 공백 및 구분 기호가 없는 10 자리 숫자
  
국가 보험 번호 (NINO): 자세한 내용은 영국 섹션 "을 참조 하세요. [중요 한 정보 유형이 찾는](what-the-sensitive-information-types-look-for.md)국가 보험 번호 (NINO) "입니다.
  
### <a name="pattern"></a>패턴

UTR (Unique Taxpayer Reference): 10 자리 숫자
  
국가 보험 번호 (NINO): 자세한 내용은 영국 섹션 "을 참조 하세요. [중요 한 정보 유형이 찾는](what-the-sensitive-information-types-look-for.md)국가 보험 번호 (NINO) "입니다.
  
### <a name="checksum"></a>제외

예
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 이 함수 `Func_uk_eu_tax_file_number` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- From `Keywords_uk_eu_tax_file_number` 키워드를 찾았습니다. 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Func_uk_eu_tax_file_number" />
          <Match idRef="Keywords_uk_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>키워드

#### <a name="keywordsukeutaxfilenumber"></a>Keywords_uk_eu_tax_file_number

tax id
  
세금 번호 번호
  
세금 id 번호
  
tax identification
  
세금 식별 번호
  
세금 번호
  
세금
  
taxid#
  
세금 파일
  
세금 파일 번호
  
## <a name="see-also"></a>참고 항목

[중요한 정보 형식이 찾는 항목](what-the-sensitive-information-types-look-for.md)

