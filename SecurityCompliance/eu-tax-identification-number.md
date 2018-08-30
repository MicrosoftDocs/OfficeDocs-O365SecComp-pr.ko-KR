---
title: EU 세금 Id 번호
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 8/17/2018
ms.audience: Admin
ms.topic: reference
ms.service: o365-administration
localization_priority: Normal
ms.assetid: f04919c8-2356-4de2-bb2a-b9f67f339726
description: 이 항목에서는 EU 세금 Id 번호 중요 한 정보 유형을 감지 하는 경우의 데이터 손실 방지 (DLP) 정책을 찾아에 대해 보여줍니다. 이 중요 한 정보 유형 다양 한 패턴, 키워드 및 각 국가 대 한 기타 증거를 정의합니다.
ms.openlocfilehash: 5192496b393d15fd6d063e09c9bfe1cb3dd7e2dd
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22533472"
---
# <a name="eu-tax-identification-number"></a>EU 세금 Id 번호

이 항목에서는 EU 세금 식별 번호 (주석) 중요 한 정보 유형을 감지 하는 경우의 데이터 손실 방지 (DLP) 정책을 찾아에 대해 보여줍니다. 이 중요 한 정보 유형 다양 한 패턴, 키워드 및 각 국가 대 한 기타 증거를 정의합니다.
  
## <a name="austria"></a>오스트리아

### <a name="format"></a>형식

사용자 지정 하이픈 및 슬래시 숫자 9 개
  
### <a name="pattern"></a>패턴

사용자 지정 하이픈 및 슬래시 9 개의 숫자:
  
-  2자리 숫자 
    
- 하이픈 1개(선택 사항)
    
- 3자리 숫자
    
- 정방향 슬래시 1개(선택 사항)
    
- 4자리 숫자
    
### <a name="checksum"></a>체크섬

예
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.
  
- 다음은 함수 `Func_austria_eu_tax_file_number` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- 키워드에서 `Keywords_austria_eu_tax_file_number` 를 찾을 수 있습니다. 
    
DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 다음은 함수 `Func_austria_eu_tax_file_number` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
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
  
번호
  
사업자 등록 번호
  
tax id

  
st.nr 합니다.
  
steuernummer
  
## <a name="belgium"></a>벨기에

### <a name="format"></a>형식

공백 및 구분 기호 없이 11 자리 숫자
  
### <a name="pattern"></a>패턴

11자리 숫자:
  
- 2자리 숫자
    
- "0" 또는 "1"
    
- 1자리 숫자
    
- "0" 또는 "1" 또는 "2" 또는 "3" 
    
- 6자리 숫자
    
### <a name="checksum"></a>체크섬

해당 없음
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 정규식 `Regex_belgium_eu_tax_file_number` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- 키워드에서 `Keywords_belgium_eu_tax_file_number` 를 찾을 수 있습니다. 
    
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
  
국가 번호
  
사업자 등록 번호
  
tax id

  
nif
  
nif #
  
numéro de registre 국가
  
numéro d'identification fiscale
  
## <a name="bulgaria"></a>불가리아

### <a name="format"></a>형식

공백 및 구분 기호 없이 10 자리 숫자
  
### <a name="pattern"></a>패턴

10자리 숫자
  
### <a name="checksum"></a>체크섬

예
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.
  
- 다음은 함수 `Func_bulgaria_eu_tax_file_number` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- 키워드에서 `Keywords_bulgaria_eu_tax_file_number` 를 찾을 수 있습니다. 
    
DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 다음은 함수 `Func_bulgaria_eu_tax_file_number` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
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

bucn
  
uniform 복제 번호
  
bucn #
  
uniformcivilnumber #
  
uniform 복제 id
  
uniform 복제 없음
  
egn
  
불가리아어 uniform 복제 번호
  
uniformcivilno #
  
egn #
  
УНИФОРМ ГРАЖДАНСКИ НОМЕР
  
Униформ id
  
Униформ граждански id
  
УНИФОРМ ГРАЖДАНСКИ НЕ
  
## <a name="croatia"></a>크로아티아

### <a name="format"></a>형식

공백이 나 구분 기호 없이 11 자리 숫자
  
### <a name="pattern"></a>패턴

11자리 숫자:
  
- 임의로 선택 하는 10 자리 숫자
    
- 하나 이상의 검사 숫자
    
### <a name="checksum"></a>체크섬

예
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.
  
- 다음은 함수 `Func_croatia_eu_tax_file_number` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- 키워드에서 `Keywords_croatia_eu_tax_file_number` 를 찾을 수 있습니다. 
    
DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 다음은 함수 `Func_croatia_eu_tax_file_number` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
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

  
oid
  
oid #
  
porezni broj
  
## <a name="cyprus"></a>키프로스

### <a name="format"></a>형식

8 개의 숫자 및 지정된 된 패턴에 있는 문자 하나
  
### <a name="pattern"></a>패턴

8 개의 숫자와 문자 하나:
  
-  "0" 
    
- 7자리 숫자
    
- 하나의 문자 (대 소문자 구분 안함)
    
### <a name="checksum"></a>체크섬

해당 없음
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.
  
- 다음은 함수 `Func_cyprus_eu_tax_file_number` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- 키워드에서 `Keywords_cyprus_eu_tax_file_number` 를 찾을 수 있습니다. 
    
DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 다음은 함수 `Func_cyprus_eu_tax_file_number` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
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

  
세금 id 코드입니다.
  
눈금
  
눈금 #
  
ΑΡΙΘΜΌΣ ΦΟΡΟΛΟΓΙΚΟΎ ΜΗΤΡΏΟΥ
  
ΦΟΡΟΛΟΓΙΚΉ ΤΑΥΤΌΤΗΤΑ
  
ΚΩΔΙΚΌΣ ΦΟΡΟΛΟΓΙΚΟΎ ΜΗΤΡΏΟΥ
  
## <a name="czech-republic"></a>체코 공화국

### <a name="format"></a>형식

선택적 백슬래시를 9 또는 10 자리 숫자
  
### <a name="pattern"></a>패턴

선택적 backslashl 9 또는 10 자리 숫자:
  
- 6자리 숫자 
    
- 백슬래시 (선택 사항)
    
- 3 개 또는 4 자리 숫자
    
### <a name="checksum"></a>체크섬

해당 없음
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 정규식 `Regex_czech_republic_eu_tax_file_number` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- 키워드에서 `Keywords_czech_republic_eu_tax_file_number` 를 찾을 수 있습니다. 
    
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

### <a name="format"></a>형식

하이픈을 포함 하는 10 자리 숫자
  
### <a name="pattern"></a>패턴

10 자리 숫자를 hyphenl를 포함 합니다.
  
-  생일 (DDMMYY)에 해당 하는 6 자리 숫자 
    
- 하이픈
    
- 개인의 성별 (1 여자 2 남자 및 탑재에 대해서도 홀수)에 해당 하는 첫번째 숫자 생일 세기에 해당 하는 여기서 시퀀스 번호에 해당 하는 4 자리 숫자와 마지막 자릿수
    
### <a name="checksum"></a>체크섬

예
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.
  
- 다음은 함수 `Func_denmark_eu_tax_file_number` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- 키워드에서 `Keywords_denmark_eu_tax_file_number` 를 찾을 수 있습니다. 
    
DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 다음은 함수 `Func_denmark_eu_tax_file_number` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
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
  
cpr #
  
skat nummer
  
skat id
  
## <a name="estonia"></a>에스토니아

### <a name="format"></a>형식

공백이 나 구분 기호 없이 11 자리 숫자
  
### <a name="pattern"></a>패턴

11자리 숫자:
  
-  성별 및 여기서 홀수인 1 여자 2 남자를 나타내고 짝수 나타냅니다 탑재 다음과 같이 생일 세기에 해당 하는 한 자리 숫자: 1, 2 19 세기;에 대 한 3, 4 20 세기;에 대 한 5, 6 21 세기에 대 한 및 
    
- 생일 (YYMMDD)에 해당 하는 6 자리 숫자
    
- 같은 날짜 태어난 장애인을 구분 하는 일련 번호에 해당 하는 세 자리 숫자
    
- 하나 이상의 검사 숫자
    
### <a name="checksum"></a>체크섬

예
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.
  
- 다음은 함수 `Func_estonia_eu_tax_file_number` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- 키워드에서 `Keywords_estonia_eu_tax_file_number` 를 찾을 수 있습니다. 
    
DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 다음은 함수 `Func_estonia_eu_tax_file_number` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
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

### <a name="format"></a>형식

숫자는 11 자리의 조합 문자 및 더하기 및 빼기 기호
  
### <a name="pattern"></a>패턴

숫자는 11 자리의 조합 문자 및 더하기 및 빼기 기호:
  
- 6자리 숫자
    
- 다음 중 하나: 더하기 기호, 빼기 기호 또는 더하기 기호를 의미 있는 문자 "A" (하지 대/소문자 구분) 1800-1899 년 사이 태어난 빼기 서명 간의 태어난 의미 1900-1999 및 "A" 2000 탄생 하 게 하는 방법 및 완료
    
- 3자리 숫자
    
- 하나의 문자 또는 숫자
    
### <a name="checksum"></a>체크섬

예
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.
  
- 다음은 함수 `Func_finland_eu_tax_file_number` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- 키워드에서 `Keywords_finland_eu_tax_file_number` 를 찾을 수 있습니다. 
    
DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 다음은 함수 `Func_finland_eu_tax_file_number` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
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
  
identity 번호
  
핀란드 국가 id 번호
  
personalidnumber #
  
국가 id 번호
  
id 번호
  
국가 id 없습니다.
  
국가 id 번호
  
id 없음
  
tunnistenumero
  
henkilötunnus
  
yksilöllinen henkilökohtainen tunnistenumero
  
ainutlaatuinen henkilökohtainen tunnus
  
identiteetti numero
  
suomen kansallinen henkilötunnus
  
henkilötunnusnumero #
  
kansallisen tunnistenumero
  
tunnusnumero
  
kansallinen tunnus numero
  
## <a name="france"></a>프랑스

### <a name="format"></a>형식

개인 및 엔터티에 대 한 숫자 9 개에 대 한 13 자릿수
  
### <a name="pattern"></a>패턴

개별 사용자에 대 한 자리 숫자 13:
  
- 0, 1, 2 또는 3 이어야 하는 한 자리 숫자
    
- 12자리 숫자
    
엔터티에 대 한 숫자 9 개
  
### <a name="checksum"></a>체크섬

해당 없음
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.
  
- 다음은 함수 `Func_france_eu_tax_file_number` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- 키워드에서 `Keywords_france_eu_tax_file_number` 를 찾을 수 있습니다. 
    
DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 다음은 함수 `Func_france_eu_tax_file_number` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
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

세금 id 번호
  
세금 번호
  
tax id

  
numéro d'identification fiscale
  
## <a name="germany"></a>독일

### <a name="format"></a>형식

공백 및 구분 기호 없이 11 자리 숫자
  
### <a name="pattern"></a>패턴

11 자리 숫자:
  
-  10 자리 숫자 
    
- 하나 이상의 검사 숫자
    
### <a name="checksum"></a>체크섬

예
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.
  
- 다음은 함수 `Func_germany_eu_tax_file_number` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- 키워드에서 `Keywords_germany_eu_tax_file_number` 를 찾을 수 있습니다. 
    
DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 다음은 함수 `Func_germany_eu_tax_file_number` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
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
  
no를 세금 합니다.
  
taxno #
  
taxnumber #
  
taxnumber
  
tax id

  
taxid #
  
세금 id 번호
  
식별을 더 세금 합니다.
  
steuernummer
  
steuer id
  
steueridentifikationsnummer
  
## <a name="greece"></a>그리스

### <a name="format"></a>형식

공백 및 구분 기호 없이 숫자 9 개
  
### <a name="pattern"></a>패턴

9자리 숫자
  
### <a name="checksum"></a>체크섬

해당 없음
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 정규식 `Regex_greece_eu_tax_file_number` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- 키워드에서 `Keywords_greece_eu_tax_file_number` 를 찾을 수 있습니다. 
    
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
  
tin

  
id를 더 세금 합니다.
  
id를 더 세금
  
세금 id 번호
  
세금 레지스트리 번호
  
레지스트리를 더 세금 합니다.
  
afm #
  
주석 #
  
taxidno #
  
taxregistryno #
  
ΑΡΙΘΜΌΣ ΦΟΡΟΛΟΓΙΚΟΎ ΜΗΤΡΏΟΥ
  
aφμ
  
aφμ αριθμός
  
ΦΟΡΟΛΟΓΙΚΟΎ ΜΗΤΡΏΟΥ ΝΟ 합니다.
  
ΤΟΝ ΑΡΙΘΜΌ ΦΟΡΟΛΟΓΙΚΟΎ ΜΗΤΡΏΟΥ
  
## <a name="hungary"></a>헝가리

### <a name="format"></a>형식

공백이 나 구분 기호 없이 10 자리 숫자
  
### <a name="pattern"></a>패턴

10 자리 숫자:
  
-  "8" 되어야 하는 한 자리 숫자 
    
- 날짜 사이의 일 수에 해당 하는 5 자리 01/01/1867 및 개인의 생일의 날짜
    
- 하루에 탄생 하 게 하는 개인을 구분 하기 위해 우연히 생성 번호에 해당 하는 세 자리 숫자
    
- 하나 이상의 검사 숫자
    
### <a name="checksum"></a>체크섬

예
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.
  
- 다음은 함수 `Func_hungary_eu_tax_file_number` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- 키워드에서 `Keywords_hungary_eu_tax_file_number` 를 찾을 수 있습니다. 
    
DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 다음은 함수 `Func_hungary_eu_tax_file_number` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
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

헝가리어 세금 id 번호
  
헝가리어 주석
  
세금 id 번호
  
vat 번호
  
인증 기관을 더 세금
  
세금 id 세금 identity 번호
  
taxidnumber #
  
주석 #
  
hungatiantin #
  
식별을 더 세금
  
taxidno #
  
adóazonosító szám
  
adószám
  
adóhatóság szám
  
## <a name="ireland"></a>Ireland

### <a name="format"></a>형식

공백이 나 구분 기호 없이 문자 앞에 오는 7 자리 숫자
  
### <a name="pattern"></a>패턴

7 자리 숫자 앞에 오는 문자를:
  
-  7자리 숫자 
    
- 하나의 문자 (대 소문자 구분 안함)
    
### <a name="checksum"></a>체크섬

해당 없음
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.
  
- 다음은 함수 `Func_ireland_eu_tax_file_number` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- 키워드에서 `Keywords_ireland_eu_tax_file_number` 를 찾을 수 있습니다. 
    
DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 다음은 함수 `Func_ireland_eu_tax_file_number` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
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

공공 서비스 없음
  
개인 공공 서비스 없음
  
pps 없음
  
개인 no 서비스
  
pps 서비스 없음
  
ppsno #
  
아일랜드 pps 없음
  
publicserviceno #
  
개인 공공 서비스 번호
  
uimhir phearsanta seirbhíse poiblí
  
pps uimh
  
uimhir aitheantais phearsanta
  
## <a name="italy"></a>이탈리아

### <a name="format"></a>형식

16 비트 문자 및 지정 된 패턴의 자릿수
  
### <a name="pattern"></a>패턴

16 대 문자와 숫자:
  
-  패밀리 이름에서 처음 세 자음에 해당 하는 세 개 문자 
    
- 먼저, 세번째 및 네번째에 해당 하는 세 글자로 자음 첫 사용자 이름
    
- 마지막 생일의 연도의 숫자에 해당 하는 두 자리 숫자
    
- 생일의 월에 해당 하는 한 자리 숫자-문자 사전순으로 사용 되지만 문자를 E, H, L, M, P, R T로 사용 됩니다 (따라서 1 월 A 이며 년 10 월 R)
    
- 40 수 컷 구별 하기 위해 산포도 대 한 생일 요일에 추가 되는 여기서 생일의 월의 날짜에 해당 하는 두 자리 숫자
    
- 사용자 출생 여기서는 지방 자치 단체에 특정 지역 번호에 해당 하는 4 자리 숫자-외국에 사용 되는 전체 국가 코드
    
- 하나 이상의 검사 숫자
    
### <a name="checksum"></a>체크섬

예
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.
  
- 다음은 함수 `Func_italy_eu_tax_file_number` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- 키워드에서 `Keywords_italy_eu_tax_file_number` 를 찾을 수 있습니다. 
    
DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 다음은 함수 `Func_italy_eu_tax_file_number` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
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
  
no를 세금 합니다.
  
taxno #
  
taxnumber #
  
taxnumber
  
tax id

  
taxid #
  
회계 코드
  
codice fiscale
  
## <a name="latvia"></a>라트비아

### <a name="format"></a>형식

공백이 나 구분 기호 없이 11 자리 숫자
  
### <a name="pattern"></a>패턴

지정된 된 패턴에 11 자리 숫자
  
-  생일 (DDMMYY)의 날짜에 해당 하는 6 자리 숫자 
    
- 여기서 19 세기에 해당 하는 "0", "1" 해당 20 세기에 "2" 하 고 해당 21 세기 생일 세기에 해당 하는 한 자리 숫자
    
- 4자리 숫자
    
### <a name="checksum"></a>체크섬

예
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.
  
- 다음은 함수 `Func_latvia_eu_tax_file_number` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- 키워드에서 `Keywords_latvia_eu_tax_file_number` 를 찾을 수 있습니다. 
    
DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 다음은 함수 `Func_latvia_eu_tax_file_number` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
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
  
no를 세금 합니다.
  
taxno #
  
taxnumber #
  
taxnumber
  
tax id

  
taxid #
  
세금 id 번호
  
식별을 더 세금 합니다.
  
nodokļa numurs
  
nodokļu identifikācijas numurs
  
nodokļu identifikācija numurs
  
## <a name="lithuania"></a>리투아니아

### <a name="format"></a>형식

공백이 나 구분 기호 없이 11 자리 숫자
  
### <a name="pattern"></a>패턴

11자리 숫자
  
### <a name="checksum"></a>체크섬

해당 없음
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.
  
- 다음은 함수 `Func_lithuania_eu_tax_file_number` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- 키워드에서 `Keywords_lithuania_eu_tax_file_number` 를 찾을 수 있습니다. 
    
DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 다음은 함수 `Func_lithuania_eu_tax_file_number` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
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
  
no를 세금 합니다.
  
세금 no #
  
taxnumber #
  
taxnumber
  
tax id

  
taxid #
  
세금 id 번호
  
식별을 더 세금 합니다.
  
mokesčių id
  
mokesčių numeris
  
mokesčių identifikavimas numeris
  
## <a name="luxemburg"></a>룩셈부르크

### <a name="format"></a>형식

공백이 나 구분 기호 없이 13 자릿수
  
### <a name="pattern"></a>패턴

13자리 숫자:
  
-  11자리 숫자 
    
- 2개의 검사 숫자
    
### <a name="checksum"></a>체크섬

예
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.
  
- 다음은 함수 `Func_luxemburg_eu_tax_file_number` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- 키워드에서 `Keywords_luxemburg_eu_tax_file_number` 를 찾을 수 있습니다. 
    
DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 다음은 함수 `Func_luxemburg_eu_tax_file_number` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
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
  
no를 세금 합니다.
  
taxno #
  
taxnumber #
  
taxnumber
  
tax id

  
taxid #
  
세금 id 번호
  
식별을 더 세금 합니다.
  
steuernummer
  
steuer id
  
steueridentifikationsnummer
  
## <a name="malta"></a>몰타

### <a name="format"></a>형식

몰타어 국민에 대 한: 7 자리 숫자 및 지정된 된 패턴에 있는 문자 하나
  
비 몰타어 국민 및 몰타어 엔터티: 9 자리 숫자
  
### <a name="pattern"></a>패턴

몰타어 국민: 7 자리 숫자와 문자 하나
  
-  7자리 숫자 
    
- 하나의 문자 (대 소문자 구분 안함)
    
비 몰타어 국민 및 몰타어 엔터티: 9 자리 숫자
  
-  9자리 숫자 
    
### <a name="checksum"></a>체크섬

해당 없음
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 다음은 함수 `Func_malta_eu_tax_file_number` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- 키워드에서 `Keywords_malta_eu_tax_file_number` 를 찾을 수 있습니다. 
    
DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 65% 신뢰합니다.
  
- 다음은 함수 `Func_malta_eu_tax_file_number` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
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
  
no를 세금 합니다.
  
taxno #
  
taxnumber #
  
taxnumber
  
tax id

  
taxid #
  
세금 id 번호
  
식별을 더 세금 합니다.
  
numru tat taxxa
  
id tat-taxxa
  
numru ta ' identifikazzjoni tat taxxa
  
## <a name="netherlands"></a>네덜란드

### <a name="format"></a>형식

공백이 나 구분 기호 없이 숫자 9 개
  
### <a name="pattern"></a>패턴

9자리 숫자 
  
### <a name="checksum"></a>체크섬

예
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.
  
- 다음은 함수 `Func_netherlands_eu_tax_file_number` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- 키워드에서 `Keywords_netherlands_eu_tax_file_number` 를 찾을 수 있습니다. 
    
DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 다음은 함수 `Func_netherlands_eu_tax_file_number` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
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

네덜란드 세금 id 번호
  
네덜란드 세금 식별
  
네덜란드령의 세금 id 번호
  
네덜란드령의 세금 식별
  
세금 id 번호
  
네덜란드어 세금 id
  
네덜란드어 세금 id 번호
  
tax id

  
세금 id #
  
세금 번호
  
세금 no #
  
세금 #
  
tin

  
주석 #
  
네덜란드 주석
  
네덜란드령의 주석
  
네덜란드 belasting identificatienummer
  
identificatienummer van belasting
  
identificatienummer belasting
  
네덜란드 belasting identificatie
  
네덜란드 belasting id nummer
  
네덜란드 belastingnummer
  
btw nummer
  
nederlandse belasting identificatie
  
## <a name="poland"></a>폴란드

### <a name="format"></a>형식

공백이 나 구분 기호 없이 11 개의 숫자
  
### <a name="pattern"></a>패턴

11 개의 숫자
  
### <a name="checksum"></a>체크섬

예
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.
  
- 다음은 함수 `Func_poland_eu_tax_file_number` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- 키워드에서 `Keywords_poland_eu_tax_file_number` 를 찾을 수 있습니다. 
    
DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 다음은 함수 `Func_poland_eu_tax_file_number` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
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
  
no를 세금 합니다.
  
taxno #
  
taxnumber #
  
taxnumber
  
닙 (nip)
  
닙 (nip) #
  
tax id

  
세금 id #
  
닙 (nip) id
  
닙 (nip) id #
  
세금 id 번호
  
식별을 더 세금 합니다.
  
vat 번호
  
no를 vat 합니다.
  
vatno #
  
vat id
  
vat id #
  
u r identyfikacji podatkowej
  
polski u r identyfikacji podatkowej
  
numeridentyfikacjipodatkowej #
  
## <a name="portugal"></a>포르투갈

### <a name="format"></a>형식

공백이 나 구분 기호 없이 숫자 9 개
  
### <a name="pattern"></a>패턴

9자리 숫자
  
### <a name="checksum"></a>체크섬

예
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.
  
- 다음은 함수 `Func_portugal_eu_tax_file_number` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- 키워드에서 `Keywords_portugal_eu_tax_file_number` 를 찾을 수 있습니다. 
    
DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 다음은 함수 `Func_portugal_eu_tax_file_number` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
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
  
no를 세금 합니다.
  
taxno #
  
taxnumber #
  
taxnumber
  
nif
  
nif #
  
회계 numero
  
회계 número de identificação
  
## <a name="romania"></a>루마니아

### <a name="format"></a>형식

공백이 나 구분 기호 없이 13 자릿수
  
### <a name="pattern"></a>패턴

13자리 숫자
  
### <a name="checksum"></a>체크섬

해당 없음
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 정규식 `Regex_romania_eu_tax_file_number` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- 키워드에서 `Keywords_romania_eu_tax_file_number` 를 찾을 수 있습니다. 
    
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
  
파일을 더 세금
  


tax file number
  
no 세금
  
세금 번호
  
taxid #
  
taxno #
  
id ul taxei
  
numărul de identificare fiscală
  
## <a name="slovakia"></a>슬로바키아

### <a name="format"></a>형식

공백이 나 구분 기호 없이 10 자리 숫자
  
### <a name="pattern"></a>패턴

10자리 숫자
  
### <a name="checksum"></a>체크섬

해당 없음
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 정규식 `Regex_slovakia_eu_tax_file_number` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- 키워드에서 `Keywords_slovakia_eu_tax_file_number` 를 찾을 수 있습니다. 
    
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
  
주석 id
  
주석 없음
  
슬로바키아어 주석 id
  
tin

  
파일을 더 세금
  


tax file number
  
no 세금
  
세금 번호
  
taxid #
  
taxno #
  
daňové identifikačné číslo
  
daňové číslo
  
daňové číslo súboru
  
## <a name="slovenia"></a>슬로베니아

### <a name="format"></a>형식

공백이 나 구분 기호 없이 8 개의 숫자
  
### <a name="pattern"></a>패턴

8자리 숫자
  
### <a name="checksum"></a>체크섬

예
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.
  
- 다음은 함수 `Func_slovenia_eu_tax_file_number` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- 키워드에서 `Keywords_slovenia_eu_tax_file_number` 를 찾을 수 있습니다. 
    
DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 다음은 함수 `Func_slovenia_eu_tax_file_number` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
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
  
주석 id
  
주석 없음
  
슬로베니아어 주석 id
  
tin

  
파일을 더 세금
  


tax file number
  
no 세금
  
세금 번호
  
taxid #
  
taxno #
  
identifikacijska številka davka
  
davčna številka
  
Številka davčne datoteke
  
## <a name="spain"></a>스페인

### <a name="format"></a>형식

7 또는 8 개의 숫자와 지정한 패턴에 하나 또는 두 문자
  
### <a name="pattern"></a>패턴

스페인 국가 Id 카드와 스페인어 자연 스러운 사용자:
  
-  8자리 숫자 
    
- 하나의 대문자 (대/소문자 구분) 
    
스페인 국가 Id 카드 없이 비 상주 Spaniards
  
- 하나의 대문자 "L" (대/소문자 구분)
    
- 7자리 숫자
    
- 하나의 대문자 (대/소문자 구분) 
    
14 년 없이 스페인 국가 Id 카드의 기간을 아래에서 상주 Spaniards:
  
- 하나의 대문자 "K" (대/소문자 구분)
    
-  7자리 숫자 
    
- 하나의 대문자 (대/소문자 구분)
    
한 말야 Id 번호로 foreigners
  
- "X", "Y" 또는 "Z" (대/소문자 구분) 즉 글자 하나의 대문자 
    
- 7자리 숫자
    
- 하나의 대문자 (대/소문자 구분) 
    
Id 번호 말야의 없이 foreigners
  
- "M" (대/소문자 구분)는 하나의 대문자 
    
- 7자리 숫자
    
- 하나의 대문자 (대/소문자 구분) 
    
### <a name="checksum"></a>체크섬

예
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.
  
- 다음은 함수 `Func_spain_eu_tax_file_number` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- 키워드에서 `Keywords_spain_eu_tax_file_number` 를 찾을 수 있습니다. 
    
DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 다음은 함수 `Func_spain_eu_tax_file_number` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
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
  
cif 없음
  
스페인어 cif id
  
cif
  
파일을 더 세금
  
스페인어 cif 번호
  


tax file number
  
스페인어 cif 없음
  
no 세금
  
세금 번호
  
taxid #
  
taxno #
  
cifid #
  
spanishcifid #
  
spanishcifno #
  
número de contribuyente
  
número de impuesto corporativo
  
회계 número de identificación
  
cif número
  
cifnúmero #
  
## <a name="sweden"></a>스웨덴

### <a name="format"></a>형식

10 자리 숫자 및 지정된 된 패턴의 기호
  
### <a name="pattern"></a>패턴

10 자리 숫자 및 기호:
  
-  생일 (YYMMDD)에 해당 하는 6 자리 숫자 
    
- 더하기 기호, 빼기 기호 또는 백슬래시
    
- Id를 구성 하는 세 자리 번호 매기기 고유 위치: 
    
  - 1990 전에 발급 된 번호에 대 한 7 번째 및 여덟 번째 숫자는 생일 또는 foreign-born 사용자의 국가 식별
    
  - 9 번째 위치에 숫자 1 여자 2 남자 또는 탑재에 대해서도 어느 홀수 하 여 성별을 나타냅니다.
    
- 하나 이상의 검사 숫자
    
### <a name="checksum"></a>체크섬

예
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.
  
- 다음은 함수 `Func_sweden_eu_tax_file_number` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- 키워드에서 `Keywords_sweden_eu_tax_file_number` 를 찾을 수 있습니다. 
    
DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 다음은 함수 `Func_sweden_eu_tax_file_number` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
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

  
id를 더 세금 합니다.
  
세금 id 번호
  
tax identification

  
세금 식별 #
  
no를 세금 합니다.
  
세금 #
  
taxid #
  
세금 파일
  
파일을 더 세금 합니다.
  
개인 id 번호
  
skatt id nummer
  
skatt identifikation
  
personnummer
  
## <a name="uk"></a>영국

### <a name="format"></a>형식

공백 및 구분 기호 없이 10 자리 고유 납세자 참조 (UTR):
  
국가별 보험 번호 (NINO): 자세한 내용은의 섹션을 참조 "영국 National 보험 번호 (NINO)" [에 대 한 중요 한 정보 유형을 확인](what-the-sensitive-information-types-look-for.md)합니다.
  
### <a name="pattern"></a>패턴

고유 납세자 참조 (UTR): 10 자리 숫자
  
국가별 보험 번호 (NINO): 자세한 내용은의 섹션을 참조 "영국 National 보험 번호 (NINO)" [에 대 한 중요 한 정보 유형을 확인](what-the-sensitive-information-types-look-for.md)합니다.
  
### <a name="checksum"></a>체크섬

예
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 다음은 함수 `Func_uk_eu_tax_file_number` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- 키워드에서 `Keywords_uk_eu_tax_file_number` 를 찾을 수 있습니다. 
    
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

  
id를 더 세금 합니다.
  
세금 id 번호
  
tax identification

  
세금 식별 #
  
no를 세금 합니다.
  
세금 #
  
taxid #
  
세금 파일
  
파일을 더 세금 합니다.
  
## <a name="see-also"></a>참고 항목

[중요한 정보 형식이 찾는 항목](what-the-sensitive-information-types-look-for.md)

