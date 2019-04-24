---
title: EU 국가 식별 번호
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 8/17/2018
ms.audience: Admin
ms.topic: reference
ms.service: O365-seccomp
ms.collection: M365-security-compliance
localization_priority: Normal
description: 이 항목에서는 DLP (데이터 손실 방지) 정책이 EU 국가 식별 번호 중요 정보 유형을 검색할 때 찾는 항목을 보여 줍니다. 이 중요 한 정보 유형은 각 국가에 대 한 다양 한 패턴, 키워드 및 기타 증거를 정의 합니다.
ms.openlocfilehash: afae2c3fa54fe5fcd93990cdf5797f5517c46202
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32255646"
---
# <a name="eu-national-identification-number"></a>EU 국가 식별 번호

이 항목에서는 DLP (데이터 손실 방지) 정책이 EU 국가 식별 번호 중요 정보 유형을 검색할 때 찾는 항목을 보여 줍니다. 이 중요 한 정보 유형은 각 국가에 대 한 다양 한 패턴, 키워드 및 기타 증거를 정의 합니다.
  
## <a name="austria"></a>오스트리아

### <a name="format"></a>형식일

문자, 숫자 및 특수 문자의 24 자 조합
  
### <a name="pattern"></a>패턴

24 문자:
  
-  22 개 문자 (대/소문자 구분 안 함), 숫자, 백슬래시, 슬래시 또는 더하기 기호 
    
- 2 개의 문자 (대/소문자 구분 안 함), 숫자, 백슬래시, 슬래시, 더하기 기호 또는 등호
    
### <a name="checksum"></a>제외

해당 없음
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 정규식이 해당 `Regex_austria_eu_national_id_card` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- from `Keywords_austria_eu_national_id_card` 키워드를 찾았습니다. 
    
```
 
<Entity id="419f449f-6d9d-4be1-a154-b531f7a91b41" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_austria_eu_national_id_card" />
          <Match idRef="Keywords_austria_eu_national_id_card" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>키워드

#### <a name="keywordsaustriaeunationalidcard"></a>Keywords_austria_eu_national_id_card

오스트리아 id 번호
  
국가 id 번호
  
id 번호
  
national id
  
personalausweis republik österreich
  
## <a name="belgium"></a>벨기에

자세한 내용은 [중요 한 정보 유형이 찾는](what-the-sensitive-information-types-look-for.md)"벨기에 국가 번호" 섹션을 참조 하십시오.
  
## <a name="bulgaria"></a>불가리아

### <a name="format"></a>형식일

공백과 구분 기호가 없는 10 자리 숫자
  
### <a name="pattern"></a>패턴

공백과 구분 기호가 없는 10 자리 숫자
  
-  생년월일에 해당 하는 6 자리 숫자 (YYMMDD) 
    
- 출생 순서에 해당 하는 2 자리 숫자
    
- 성별에 해당 하는 1 자리 숫자와이에 해당 하는 짝수 자리 숫자 및 암의 홀수 숫자입니다.
    
- 검사 숫자 1 개
    
### <a name="checksum"></a>제외

예
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.
  
- 이 함수 `Func_bulgaria_national_number` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- from `Keywords_bulgaria_national_number` 키워드를 찾았습니다. 
    
DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 이 함수 `Func_bulgaria_national_number` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
```
<Entity id="419f449f-6d9d-4be1-a154-b531f7a91b41" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_bulgaria_national_number" />
          <Match idRef="Keywords_bulgaria_national_number" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_bulgaria_eu_national_id_card" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>키워드

#### <a name="keywordsbulgarianationalnumber"></a>Keywords_bulgaria_national_number

egn
  
egn #
  
불가리아어 국가 번호
  
국가 번호
  
social security number
  
nationalnumber #
  
ssn
  
ssn
  
nationalnumber
  
bnn #
  
bnn
  
개인 id 번호
  
personalidnumber #
  
единен граждански номер
  
edinen grazhdanski nomer
  
егн
  
егн #
  
## <a name="croatia"></a>크로아티아

자세한 내용은 [중요 한 정보 유형이 찾는](what-the-sensitive-information-types-look-for.md)"크로아티아 id 번호" 섹션을 참조 하십시오.
  
## <a name="cyprus"></a>키프로스

### <a name="format"></a>형식일

공백과 구분 기호가 없는 10 자리 숫자
  
### <a name="pattern"></a>패턴

 10 자리 숫자 
  
### <a name="checksum"></a>제외

해당 없음
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 정규식이 해당 `Regex_cyprus_eu_national_id_card` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- from `Keywords_cyprus_eu_national_id_card` 키워드를 찾았습니다. 
    
```
 
<Entity id="419f449f-6d9d-4be1-a154-b531f7a91b41" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_cyprus_eu_national_id_card" />
          <Match idRef="Keywords_cyprus_eu_national_id_card" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>키워드

#### <a name="keywordscypruseunationalidcard"></a>Keywords_cyprus_eu_national_id_card

id 카드 번호
  
national identification number
  
개인 id 번호
  
id 카드 번호
  
ταυτοτητασ
  
## <a name="czech-republic"></a>체코 공화국

자세한 내용은 [중요 한 정보 유형이 찾는](what-the-sensitive-information-types-look-for.md)"체코어 국내 id 번호" 섹션을 참조 하십시오.
  
## <a name="denmark"></a>덴마크

자세한 내용은 [중요 한 정보 유형이 찾는](what-the-sensitive-information-types-look-for.md)"덴마크 개인 식별 번호" 섹션을 참조 하십시오.
  
## <a name="estonia"></a>에스토니아

### <a name="format"></a>형식일

공백과 구분 기호를 사용 하지 않고 11 자리 숫자
  
### <a name="pattern"></a>패턴

11자리 숫자:
  
- 출생의 성별 및 세기에 해당 하는 1 자리 숫자 (예: 암, 수, 19th 세기, 3-4:20th 세기, 5-6 = 21 세기)
    
- 출생 날짜에 해당 하는 6 자리 숫자 (YYMMDD)
    
- 같은 날짜에 태어난 사람을 구분 하는 일련 번호에 해당 하는 3 자리 숫자
    
- 검사 숫자 1 개
    
### <a name="checksum"></a>제외

예
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.
  
- 이 함수 `Func_estonia_eu_national_id_card` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- from `Keywords_estonia_eu_national_id_card` 키워드를 찾았습니다. 
    
DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 이 함수 `Func_estonia_eu_national_id_card` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
```
 
<Entity id="419f449f-6d9d-4be1-a154-b531f7a91b41" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_estonia_eu_national_id_card" />
          <Match idRef="Keywords_estonia_eu_national_id_card" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_estonia_eu_national_id_card" />
</Pattern>
</Entity>
```

### <a name="keywords"></a>키워드

#### <a name="keywordsestoniaeunationalidcard"></a>Keywords_estonia_eu_national_id_card

개인 식별 코드
  
개인 식별 번호
  
national identification number
  
국가 번호
  
개인 id 번호
  
personalidnumber #
  
ik
  
isikukood
  
id-kaart
  
## <a name="finland"></a>핀란드

자세한 내용은 [중요 한 정보 유형이 찾는](what-the-sensitive-information-types-look-for.md)"핀란드 국가 ID" 섹션을 참조 하십시오.
  
## <a name="france"></a>프랑스

자세한 내용은 [중요 한 정보 유형이 찾는](what-the-sensitive-information-types-look-for.md)"경기도 국가 ID 카드 (cni)" 섹션을 참조 하십시오.
  
## <a name="germany"></a>독일

자세한 내용은 [중요 한 정보 유형이 찾는](what-the-sensitive-information-types-look-for.md)"독일 id 카드 번호" 섹션을 참조 하십시오.
  
## <a name="greece"></a>그리스

자세한 내용은 [중요 한 정보 유형이 찾는](what-the-sensitive-information-types-look-for.md)"그리스 국가 ID 카드" 섹션을 참조 하십시오.
  
## <a name="hungary"></a>헝가리

### <a name="format"></a>형식일

11자리 숫자
  
### <a name="pattern"></a>패턴

11자리 숫자:
  
-  성별에 해당 하는 1 자리 숫자 (1gb, 2 암, 기타 번호는 두 개를 포함 하는 경우에만 발생 합니다. 
    
- 생년월일에 해당 하는 6 자리 숫자 (YYMMDD)
    
- 일련 번호에 해당 하는 3 자리 숫자
    
- 검사 숫자 1 개
    
### <a name="checksum"></a>제외

예
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.
  
- 이 함수 `Func_hungary_eu_national_id_card` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- from `Keywords_hungary_eu_national_id_card` 키워드를 찾았습니다. 
    
DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 이 함수 `Func_hungary_eu_national_id_card` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
```
<Entity id="419f449f-6d9d-4be1-a154-b531f7a91b41" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_hungary_eu_national_id_card" />
          <Match idRef="Keywords_hungary_eu_national_id_card" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_hungary_eu_national_id_card" />
</Pattern>
</Entity>
```

### <a name="keywords"></a>키워드

#### <a name="keywordshungaryeunationalidcard"></a>Keywords_hungary_eu_national_id_card

개인 식별 번호
  
identification number
  
개인 id 번호
  
személyazonosító igazolvány
  
## <a name="ireland"></a>Ireland

### <a name="format"></a>형식일

지정 된 패턴에서 문자, 숫자 및 공백의 9 자 조합
  
### <a name="pattern"></a>패턴

지정 된 패턴에서 문자, 숫자 및 공백의 9 자 조합
  
01 년 1 월 2013 일 현재 위치:
  
-  7자리 숫자 
    
- 검사 숫자 1 개
    
- 1 개의 공백 또는 대문자 "W" (대/소문자 구분)
    
01 년 1 월 2013 일 이전:
  
-  7자리 숫자 
    
- 검사 숫자 1 개
    
- 1 개의 공백 또는 대문자 (대/소문자 구분)
    
### <a name="checksum"></a>제외

예
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.
  
- 이 함수는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.
    
- from 키워드를 찾았습니다.
    
DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 이 함수는 해당 패턴과 일치 하는 콘텐츠를 찾습니다.
    
```
 
<Entity id="419f449f-6d9d-4be1-a154-b531f7a91b41" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_ireland_eu_national_id_card" />
          <Match idRef="Keywords_ireland_eu_national_id_card" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_ireland_eu_national_id_card" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>키워드

#### <a name="keywordsirelandeunationalidcard"></a>Keywords_ireland_eu_national_id_card

개인 공용 서비스 번호
  
pps 아니요
  
수입 및 주민 등록 보험 번호
  
rsi 아니요
  
개인 식별 번호
  
identification number
  
개인 id 번호
  
uimhir phearsanta seirbhíse poiblí
  
uimh psp
  
## <a name="italy"></a>이탈리아

### <a name="format"></a>형식일

지정 된 패턴에 해당 하는 문자 및 숫자의 16 자 조합
  
### <a name="pattern"></a>패턴

문자와 숫자의 16 자 조합:
  
- 가족 이름에서 처음 세 개의 자음에 해당 하는 3 개의 문자
    
- 이름의 첫 번째, 세 번째 및 네 번째 자음에 해당 하는 3 개의 문자
    
- 출생 연도의 마지막 자리에 해당 하는 2 자리 숫자
    
- 출생 월의 문자에 해당 하는 한 문자는 알파벳 순서로 사용 되지만 1 ~ E, H, L, M, P, r에 해당 하는 문자를 사용 하는 경우에만 사용할 수 있습니다.
    
- genders를 구분 하기 위해 출생 달의 날짜에 해당 하는 2 자리 숫자 (40)가 여성 생년월일에 추가 되었습니다.
    
- 사용자가 태어난 municipality 관련 지역 번호에 해당 하는 4 자리 숫자 (국가 전체 코드는 외국 국가에 사용 됨)
    
- 1 개의 패리티 숫자
    
### <a name="checksum"></a>제외

예
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.
  
- 이 함수 `Func_italy_eu_national_id_card` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- from `Keywords_italy_eu_national_id_card` 키워드를 찾았습니다. 
    
DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 이 함수 `Func_italy_eu_national_id_card` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
```
<Entity id="419f449f-6d9d-4be1-a154-b531f7a91b41" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_italy_eu_national_id_card" />
          <Match idRef="Keywords_italy_eu_national_id_card" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_italy_eu_national_id_card" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>키워드

#### <a name="keywordsitalyeunationalidcard"></a>Keywords_italy_eu_national_id_card

개인 코드
  
개인 코드 번호
  
개인 인증서 번호
  
회계 코드
  
personalcodeno #
  
개인 id 번호
  
개인 id 코드
  
codice personale
  
numero certificato personale
  
numero personale
  
numero id personale
  
codice id personale
  
codice
  
## <a name="italy"></a>이탈리아

### <a name="format"></a>형식일

지정 된 형식의 11 자리 숫자 및 하이픈
  
### <a name="pattern"></a>패턴

11 자리 숫자와 하이픈:
  
-  생년월일에 해당 하는 6 자리 숫자 (ddmmyy) 
    
- 하이픈
    
- 출생 세기에 해당 하는 1 자리 숫자 (19th 세기의 경우 "1", 21 세기의 경우 "2")
    
- 임의로 생성 되는 4 자리 숫자
    
### <a name="checksum"></a>제외

예
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.
  
- 이 함수 `Func_latvia_eu_national_id_card` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- from `Keywords_latvia_eu_national_id_card` 키워드를 찾았습니다. 
    
DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 이 함수 `Func_latvia_eu_national_id_card` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
```
<Entity id="419f449f-6d9d-4be1-a154-b531f7a91b41" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_latvia_eu_national_id_card" />
          <Match idRef="Keywords_latvia_eu_national_id_card" />
        </Pattern>
 <Pattern confidenceLevel="75">
          <IdMatch idRef="Func_latvia_eu_national_id_card" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>키워드

#### <a name="keywordslatviaeunationalidcard"></a>Keywords_latvia_eu_national_id_card

개인 코드
  
개인 코드 번호
  
개인 인증서 번호
  
personalcodeno #
  
개인 id 번호
  
개인 id 코드
  
가상 사용자 kods
  
## <a name="lithuania"></a>리투아니아

### <a name="format"></a>형식일

공백과 구분 기호를 사용 하지 않고 11 자리 숫자
  
### <a name="pattern"></a>패턴

공백과 구분 기호를 사용 하지 않고 11 자리 숫자:
  
- 사용자의 성별 및 출생 세기에 해당 하는 1 자리 숫자
    
-  생년월일에 해당 하는 6 자리 숫자 (YYMMDD) 
    
- 출생 날짜의 일련 번호에 해당 하는 3 자리 숫자
    
- 검사 숫자 1 개
    
### <a name="checksum"></a>제외

예
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.
  
- 이 함수 `Func_lithuania_eu_national_id_card` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- from `Keywords_lithuania_eu_national_id_card` 키워드를 찾았습니다. 
    
DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 이 함수 `Func_lithuania_eu_national_id_card` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
```
 
<Entity id="419f449f-6d9d-4be1-a154-b531f7a91b41" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_lithuania_eu_national_id_card" />
          <Match idRef="Keywords_lithuania_eu_national_id_card" />
        </Pattern> 
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_lithuania_eu_national_id_card" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>키워드

#### <a name="keywordslithuaniaeunationalidcard"></a>Keywords_lithuania_eu_national_id_card

개인 숫자 코드
  
고유 id 번호
  
시민 서비스 번호
  
고유 id 번호
  
uniqueidentityno #
  
개인 코드
  
as메이 inis kodas
  
unikalus identifikavimo numeris
  
piliečio paslaugos numeris
  
unikalus identifikavimo kodas
  
asmens kodas
  
## <a name="luxemburg"></a>셈

### <a name="format"></a>형식일

공백과 구분 기호를 사용 하지 않고 11 자리 숫자
  
### <a name="pattern"></a>패턴

11자리 숫자
  
- 사용자의 성별 및 출생 세기에 해당 하는 1 자리 숫자
    
-  생년월일에 해당 하는 6 자리 숫자 (YYMMDD) 
    
- 출생 날짜의 일련 번호에 해당 하는 3 자리 숫자
    
- 검사 숫자 1 개
    
### <a name="checksum"></a>제외

해당 없음
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 정규식이 해당 `Regex_luxemburg_eu_national_id_card` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- from `Keywords_luxemburg_eu_national_id_card` 키워드를 찾았습니다. 
    
```
<Entity id="419f449f-6d9d-4be1-a154-b531f7a91b41" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_luxemburg_eu_national_id_card" />
          <Match idRef="Keywords_luxemburg_eu_national_id_card" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>키워드

#### <a name="keywordsluxemburgeunationalidcard"></a>Keywords_luxemburg_eu_national_id_card

개인 id
  
개인 id 번호
  
personalidno #
  
고유 id 번호
  
personalidnumber #
  
고유 id 키
  
개인 id 코드
  
uniqueidkey #
  
개별 코드
  
개별 id
  
eindeutige id-nummer
  
eindeutige id
  
id personnelle
  
numéro d'identification 담당자
  
idpersonnelle #
  
persönliche identifikationsnummer
  
eindeutigeid #
  
## <a name="malta"></a>몰타

### <a name="format"></a>형식일

7 자리 숫자와 문자 1 개
  
### <a name="pattern"></a>패턴

7 자리 숫자와 문자 1 개:
  
-  7자리 숫자 
    
- 대문자 1 개 (대/소문자 구분)
    
### <a name="checksum"></a>제외

해당 없음
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 정규식이 해당 `Regex_malta_eu_national_id_card` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- from `Keywords_malta_eu_national_id_card` 키워드를 찾았습니다. 
    
DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 65% 신뢰합니다.
  
- 정규식이 해당 `Regex_malta_eu_national_id_card` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
```
 
<Entity id="419f449f-6d9d-4be1-a154-b531f7a91b41" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_malta_eu_national_id_card" />
          <Match idRef="Keywords_malta_eu_national_id_card" />
        </Pattern>
<Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_malta_eu_national_id_card" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>키워드

#### <a name="keywordsmaltaeunationalidcard"></a>Keywords_malta_eu_national_id_card

개인 숫자 코드
  
고유 id 번호
  
시민 서비스 번호
  
고유 id 번호
  
uniqueidentityno #
  
kodiċi numerali personali
  
numru ta ' uniku
  
numru taċ-ċittadin
  
numru ta ' uniku
  
## <a name="netherlands"></a>네덜란드

### <a name="format"></a>형식일

공백이 나 구분 기호가 없는 9 자리 숫자
  
### <a name="pattern"></a>패턴

9자리 숫자
  
### <a name="checksum"></a>제외

예
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.
  
- 이 함수 `Func_netherlands_eu_national_id_card` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- from 키워드를 찾았습니다.
    
DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 이 함수 `Func_netherlands_eu_national_id_card` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
```
 
<Entity id="419f449f-6d9d-4be1-a154-b531f7a91b41" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_netherlands_eu_national_id_card" />
          <Match idRef="Keywords_netherlands_eu_national_id_card" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_netherlands_eu_national_id_card" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>키워드

#### <a name="keywordsnetherlandseunationalidcard"></a>Keywords_netherlands_eu_national_id_card

개인 숫자 코드
  
고유 id 번호
  
시민 서비스 번호
  
고유 id 번호
  
uniqueidentityno #
  
bsn
  
bsn
  
persoonlijke 코드
  
identificatienummer
  
burgerservicenummer
  
identiteitsnummer
  
## <a name="poland"></a>폴란드

자세한 내용은 [중요 한 정보 유형이 찾는](what-the-sensitive-information-types-look-for.md)"폴란드 국가 ID (PESEL)" 섹션을 참조 하십시오.
  
## <a name="portugal"></a>포르투갈

자세한 내용은 [중요 한 정보 유형이 찾는](what-the-sensitive-information-types-look-for.md)"포르투갈 시민이 카드 번호" 섹션을 참조 하십시오.
  
## <a name="romania"></a>루마니아

### <a name="format"></a>형식일

공백과 구분 기호가 없는 13 자리 숫자
  
### <a name="pattern"></a>패턴

13자리 숫자
  
### <a name="checksum"></a>제외

예
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.
  
- 이 함수 `Func_romania_eu_national_id_card` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- from `Keywords_romania_eu_national_id_card` 키워드를 찾았습니다. 
    
DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 이 함수 `Func_romania_eu_national_id_card` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
```
 
<Entity id="419f449f-6d9d-4be1-a154-b531f7a91b41" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_romania_eu_national_id_card" />
          <Match idRef="Keywords_romania_eu_national_id_card" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_romania_eu_national_id_card" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>키워드

#### <a name="keywordsromaniaeunationalidcard"></a>Keywords_romania_eu_national_id_card

개인 숫자 코드
  
고유 id 번호
  
cnp
  
cnp #
  
pin
  
pin
  
보험 번호
  
insurancenumber #
  
고유 id 번호
  
uniqueidentityno #
  
cod 숫자 개인
  
cod identificare personal
  
cod unic identificare
  
număr personal unic
  
număr identitate
  
număr identificare personal
  
număridentitate #
  
codnumericpersonal #
  
numărpersonalunic #
  
## <a name="slovakia"></a>슬로바키아

### <a name="format"></a>형식일

백슬래시 하나를 포함 하는 10 자리 숫자
  
### <a name="pattern"></a>패턴

백슬래시 하나를 포함 하는 10 자리 숫자:
  
### <a name="checksum"></a>제외

예
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.
  
- 이 함수 `Func_slovakia_eu_national_id_card` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- from `Keywords_slovakia_eu_national_id_card` 키워드를 찾았습니다. 
    
DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 이 함수 `Func_slovakia_eu_national_id_card` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
```
 
<Entity id="419f449f-6d9d-4be1-a154-b531f7a91b41" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_slovakia_eu_national_id_card" />
          <Match idRef="Keywords_slovakia_eu_national_id_card" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_slovakia_eu_national_id_card" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>키워드

#### <a name="keywordsslovakiaeunationalidcard"></a>Keywords_slovakia_eu_national_id_card

돌 번호
  
national identification number
  
개인 식별 번호
  
social security number
  
nationalnumber #
  
ssn
  
ssn
  
국가 번호
  
개인 id 번호
  
personalidnumber #
  
rč
  
rodné číslo
  
rodne cislo
  
## <a name="slovenia"></a>슬로베니아

### <a name="format"></a>형식일

공백이 나 구분 기호가 없는 13 자리 숫자
  
### <a name="pattern"></a>패턴

지정 된 패턴의 13 자리 숫자:
  
-  생년월일 (ddmmlll)에 해당 하는 7 자리 숫자 이며 "lll"은 출생 연도의 마지막 세 자리에 해당 합니다. 
    
- 출생 면적에 해당 하는 2 자리 숫자
    
- 같은 날에 태어난 사용자의 성별 및 일련 번호 조합에 해당 하는 3 자리 숫자 (남성는 000-499, 암은 500-999)
    
- 검사 숫자 1 개
    
### <a name="checksum"></a>제외

예
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.
  
- 이 함수 `Func_slovenia_eu_national_id_card` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- from `Keywords_slovenia_eu_national_id_card` 키워드를 찾았습니다. 
    
DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 이 함수 `Func_slovenia_eu_national_id_card` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
```
 
<Entity id="419f449f-6d9d-4be1-a154-b531f7a91b41" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_slovenia_eu_national_id_card" />
          <Match idRef="Keywords_slovenia_eu_national_id_card" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_slovenia_eu_national_id_card" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>키워드

#### <a name="keywordssloveniaeunationalidcard"></a>Keywords_slovenia_eu_national_id_card

개인 숫자 코드
  
고유 id 번호
  
고유 등록 번호
  
고유 id 번호
  
uniqueidentityno #
  
고유 마스터 시민 번호
  
ed명령이 vena identifikacijska številka
  
uniqueidentityno #
  
ed명령이 vena številka glavnega državljana
  
emšo
  
## <a name="spain"></a>스페인

### <a name="format"></a>형식일

7 자리 숫자와 문자 1 개
  
### <a name="pattern"></a>패턴

7 자리 숫자와 문자 1 개
  
- 7자리 숫자
    
- 1 자리 숫자 또는 문자 (대/소문자 구분 안 함)
    
### <a name="checksum"></a>제외

해당 없음
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 정규식이 해당 `Regex_spain_eu_national_id_card` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- from `Keywords_spain_eu_national_id_card"` 키워드를 찾았습니다. 
    
```
 
<Entity id="419f449f-6d9d-4be1-a154-b531f7a91b41" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_spain_eu_national_id_card" />
          <Match idRef="Keywords_spain_eu_national_id_card" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>키워드

#### <a name="keywordsspaineunationalidcard"></a>Keywords_spain_eu_national_id_card

dni
  
national identification number
  
국가 id 번호
  
보험 번호
  
개인 식별 번호
  
국가 id
  
개인 id 없음
  
고유 id 번호
  
nationalidno #
  
uniqueid
  
dni
  
nationalid #
  
nie #
  
nie
  
nienúmero #
  
nie número
  
documento nacional de identidad
  
identidad único
  
número nacional identidad
  
dni número
  
dninúmero #
  
identidadúnico #
  
## <a name="sweden"></a>스웨덴

자세한 내용은 [중요 한 정보 유형이 찾는](what-the-sensitive-information-types-look-for.md)"스웨덴 국가 ID" 섹션을 참조 하십시오.
  
## <a name="see-also"></a>참고 항목

[중요한 정보 형식이 찾는 항목](what-the-sensitive-information-types-look-for.md)

