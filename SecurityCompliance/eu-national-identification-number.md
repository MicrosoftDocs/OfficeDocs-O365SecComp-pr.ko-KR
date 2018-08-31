---
title: EU 국가 Id 번호
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 8/17/2018
ms.audience: Admin
ms.topic: reference
ms.service: o365-administration
localization_priority: Normal
ms.assetid: 2ea971bf-9434-4b61-b825-2bbd28ae6064
description: 이 항목에서는 EU 국가 Id 번호 중요 한 정보 유형을 감지 하는 경우의 데이터 손실 방지 (DLP) 정책을 찾아에 대해 보여줍니다. 이 중요 한 정보 유형 다양 한 패턴, 키워드 및 각 국가 대 한 기타 증거를 정의합니다.
ms.openlocfilehash: 29d2126b937ff46039284a74eb2a84f2ebbacb41
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22533439"
---
# <a name="eu-national-identification-number"></a>EU 국가 Id 번호

이 항목에서는 EU 국가 Id 번호 중요 한 정보 유형을 감지 하는 경우의 데이터 손실 방지 (DLP) 정책을 찾아에 대해 보여줍니다. 이 중요 한 정보 유형 다양 한 패턴, 키워드 및 각 국가 대 한 기타 증거를 정의합니다.
  
## <a name="austria"></a>오스트리아

### <a name="format"></a>형식

문자, 숫자 및 특수 문자는 24 문자 조합
  
### <a name="pattern"></a>패턴

24 문자 수:
  
-  22 문자 (대 소문자 구분 안함), 숫자, 백슬래시, 슬래시, 또는 더하기 기호 
    
- 두 문자 (대 소문자 구분 안함), 숫자, 백슬래시, 슬래시, 더하기 기호 또는 등호
    
### <a name="checksum"></a>체크섬

해당 없음
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 정규식 `Regex_austria_eu_national_id_card` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- 키워드에서 `Keywords_austria_eu_national_id_card` 를 찾을 수 있습니다. 
    
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

오스트리아 identity 번호
  
identity 국가 번호
  
identity 번호
  

national id
  
personalausweis republik österreich
  
## <a name="belgium"></a>벨기에

자세한 내용은의 섹션을 참조 "벨기에 국가 번호" [에 대 한 중요 한 정보 유형을 확인](what-the-sensitive-information-types-look-for.md)합니다.
  
## <a name="bulgaria"></a>불가리아

### <a name="format"></a>형식

공백 및 구분 기호 없이 10 자리 숫자
  
### <a name="pattern"></a>패턴

공백 및 구분 기호 없이 10 자리 숫자
  
-  생일 (YYMMDD)에 해당 하는 6 자리 숫자 
    
- 생일 축에 해당 하는 두 자리 숫자
    
- 성별에 해당 하는 한 자리 숫자: 1 여자 2 남자 및 탑재에 대 한 홀수 짝수 숫자로
    
- 하나 이상의 검사 숫자
    
### <a name="checksum"></a>체크섬

예
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.
  
- 다음은 함수 `Func_bulgaria_national_number` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- 키워드에서 `Keywords_bulgaria_national_number` 를 찾을 수 있습니다. 
    
DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 다음은 함수 `Func_bulgaria_national_number` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
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
  
ssn #
  
ssn
  
nationalnumber
  
bnn #
  
bnn
  
개인 id 번호
  
personalidnumber #
  
ЕДИНЕН ГРАЖДАНСКИ НОМЕР
  
edinen grazhdanski nomer
  
ЕГН
  
ЕГН #
  
## <a name="croatia"></a>크로아티아

자세한 내용은의 섹션을 참조 "크로아티아 Identity Number" [에 대 한 중요 한 정보 유형을 확인](what-the-sensitive-information-types-look-for.md)합니다.
  
## <a name="cyprus"></a>키프로스

### <a name="format"></a>형식

공백 및 구분 기호 없이 10 자리 숫자
  
### <a name="pattern"></a>패턴

 10 자리 숫자 
  
### <a name="checksum"></a>체크섬

해당 없음
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 정규식 `Regex_cyprus_eu_national_id_card` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- 키워드에서 `Keywords_cyprus_eu_national_id_card` 를 찾을 수 있습니다. 
    
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
  
국가 id 번호
  
개인 id 번호
  
id 카드 번호
  
ΤΑΥΤΟΤΗΤΑΣ
  
## <a name="czech-republic"></a>체코 공화국

자세한 내용은의 섹션을 참조 "체코어 국가 Identity Number" [에 대 한 중요 한 정보 유형을 확인](what-the-sensitive-information-types-look-for.md)합니다.
  
## <a name="denmark"></a>덴마크

자세한 내용은의 섹션을 참조 "덴마크 개인 Id 번호" [에 대 한 중요 한 정보 유형을 확인](what-the-sensitive-information-types-look-for.md)합니다.
  
## <a name="estonia"></a>에스토니아

### <a name="format"></a>형식

공백 및 구분 기호 없이 11 자리 숫자
  
### <a name="pattern"></a>패턴

11자리 숫자:
  
- 성별 및 생일 세기에 해당 하는 한 자리 숫자 (홀수 번호 1 여자 2 남자, 짝수 여성; 1-2: 19 세기; 3-4: 20 세기; 5-6: 21 세기)
    
- 생일 (YYMMDD)에 해당 하는 6 자리 숫자
    
- 같은 날짜 태어난 장애인을 구분 하는 일련 번호에 해당 하는 세 자리 숫자
    
- 하나 이상의 검사 숫자
    
### <a name="checksum"></a>체크섬

예
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.
  
- 다음은 함수 `Func_estonia_eu_national_id_card` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- 키워드에서 `Keywords_estonia_eu_national_id_card` 를 찾을 수 있습니다. 
    
DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 다음은 함수 `Func_estonia_eu_national_id_card` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
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
  
국가 id 번호
  
국가 번호
  
개인 id 번호
  
personalidnumber #
  
ik
  
isikukood
  
id kaart
  
## <a name="finland"></a>핀란드

자세한 내용은의 섹션을 참조 "핀란드 국가 ID" [에 대 한 중요 한 정보 유형을 확인](what-the-sensitive-information-types-look-for.md)합니다.
  
## <a name="france"></a>프랑스

자세한 내용은의 섹션을 참조 "프랑스 국가 ID 카드 (CNI)" [에 대 한 중요 한 정보 유형을 확인](what-the-sensitive-information-types-look-for.md)합니다.
  
## <a name="germany"></a>독일

자세한 내용은의 섹션을 참조 "독일 Id 카드 번호" [에 대 한 중요 한 정보 유형을 확인](what-the-sensitive-information-types-look-for.md)합니다.
  
## <a name="greece"></a>그리스

자세한 내용은의 섹션을 참조 "그리스 국가 ID 카드" [에 대 한 중요 한 정보 유형을 확인](what-the-sensitive-information-types-look-for.md)합니다.
  
## <a name="hungary"></a>헝가리

### <a name="format"></a>형식

11자리 숫자
  
### <a name="pattern"></a>패턴

11자리 숫자:
  
-  성별 (1-2 남자, 2-탑재, 다른 번호는 1900 하기 전에 태어난 시민 또는 이중 참여 의식와 시민에 대 한 가능한도)에 해당 하는 한 자리 숫자 
    
- 생일 (YYMMDD)에 해당 하는 6 자리 숫자
    
- 일련 번호에 해당 하는 세 자리 숫자
    
- 하나 이상의 검사 숫자
    
### <a name="checksum"></a>체크섬

예
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.
  
- 다음은 함수 `Func_hungary_eu_national_id_card` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- 키워드에서 `Keywords_hungary_eu_national_id_card` 를 찾을 수 있습니다. 
    
DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 다음은 함수 `Func_hungary_eu_national_id_card` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
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

### <a name="format"></a>형식

문자, 숫자 및 지정된 된 패턴에 포함 된 공백은 9 개 문자 조합
  
### <a name="pattern"></a>패턴

문자, 숫자 및 지정된 된 패턴에 포함 된 공백은 9 개 문자 조합
  
현재 2013 년 1 월 1 일에서:
  
-  7자리 숫자 
    
- 하나 이상의 검사 숫자
    
- 한 칸 또는 대문자 "W" (대/소문자 구분)
    
2013 년 1 월 1 일 하기 전에:
  
-  7자리 숫자 
    
- 하나 이상의 검사 숫자
    
- 한 칸 또는 대문자 (대/소문자 구분)
    
### <a name="checksum"></a>체크섬

예
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.
  
- 다음은 함수 패턴과 일치 하는 콘텐츠를 찾습니다.
    
- 키워드에서 발견 됩니다.
    
DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 다음은 함수 패턴과 일치 하는 콘텐츠를 찾습니다.
    
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

개인 공공 서비스 번호
  
pps 없음
  
수익 및 사회 보험 번호
  
rsi 없음
  
개인 식별 번호
  
identification number

  
개인 id 번호
  
uimhir phearsanta seirbhíse poiblí
  
uimh 합니다. psp
  
## <a name="italy"></a>이탈리아

### <a name="format"></a>형식

문자와 지정한 패턴의 자릿수의 16 자리의 조합
  
### <a name="pattern"></a>패턴

문자와 숫자의 16 자리의 조합 합니다.
  
- 패밀리 이름에서 처음 세 자음에 해당 하는 세 개 문자
    
- 먼저, 세번째 및 네번째에 해당 하는 세 글자로 자음 첫 사용자 이름
    
- 마지막 생일의 연도의 숫자에 해당 하는 두 자리 숫자
    
- 달의 생일 편지에 해당 하는 하나의 문자-문자 사전순으로 사용 되지만 문자를 E, H, L, M, P, R T로 사용 됩니다 (따라서 1 월 A 이며 년 10 월 R)
    
- 생일의 월의 날짜에 해당 하는 두 자리-성별을 구별 하기 위해 40 여자 생일 요일에 추가 됩니다
    
- 사용자 출생 여기서는 지방 자치 단체에 특정 지역 번호에 해당 하는 4 자리 숫자 (국가 수준의 코드는 외국에 사용 됨)
    
- 하나의 패리티 숫자
    
### <a name="checksum"></a>체크섬

예
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.
  
- 다음은 함수 `Func_italy_eu_national_id_card` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- 키워드에서 `Keywords_italy_eu_national_id_card` 를 찾을 수 있습니다. 
    
DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 다음은 함수 `Func_italy_eu_national_id_card` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
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
  
codice fiscale
  
## <a name="italy"></a>이탈리아

### <a name="format"></a>형식

11 및 지정 된 형식 하이픈
  
### <a name="pattern"></a>패턴

11 자릿수와 하이픈:
  
-  생일 (DDMMYY)에 해당 하는 6 자리 숫자 
    
- 하이픈
    
- (19 세기 "0", 20 세기에 대 한 "1" 및 "2" 21 세기에 대 한) 생일 세기에 해당 하는 한 자리 숫자
    
- 임의로 생성 하는 4 자리 숫자
    
### <a name="checksum"></a>체크섬

예
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.
  
- 다음은 함수 `Func_latvia_eu_national_id_card` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- 키워드에서 `Keywords_latvia_eu_national_id_card` 를 찾을 수 있습니다. 
    
DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 다음은 함수 `Func_latvia_eu_national_id_card` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
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
  
사용자가 나옵니다 kods
  
## <a name="lithuania"></a>리투아니아

### <a name="format"></a>형식

공백 및 구분 기호 없이 11 자리 숫자
  
### <a name="pattern"></a>패턴

공백 및 구분 기호 없이 11 숫자:
  
- 사용자의 성별와 생일 세기에 해당 하는 한 자리 숫자
    
-  생일 (YYMMDD)에 해당 하는 6 자리 숫자 
    
- 생일의 날짜의 일련 번호에 해당 하는 세 자리 숫자
    
- 하나 이상의 검사 숫자
    
### <a name="checksum"></a>체크섬

예
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.
  
- 다음은 함수 `Func_lithuania_eu_national_id_card` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- 키워드에서 `Keywords_lithuania_eu_national_id_card` 를 찾을 수 있습니다. 
    
DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 다음은 함수 `Func_lithuania_eu_national_id_card` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
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
  
개인 코드입니다.
  
asmeninis skaitmeninis kodas
  
unikalus identifikavimo numeris
  
piliečio paslaugos numeris
  
unikalus identifikavimo kodas
  
asmens kodas 합니다.
  
## <a name="luxemburg"></a>룩셈부르크

### <a name="format"></a>형식

공백 및 구분 기호 없이 11 자리 숫자
  
### <a name="pattern"></a>패턴

11자리 숫자
  
- 사용자의 성별와 생일 세기에 해당 하는 한 자리 숫자
    
-  생일 (YYMMDD)에 해당 하는 6 자리 숫자 
    
- 생일의 날짜의 일련 번호에 해당 하는 세 자리 숫자
    
- 하나 이상의 검사 숫자
    
### <a name="checksum"></a>체크섬

해당 없음
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 정규식 `Regex_luxemburg_eu_national_id_card` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- 키워드에서 `Keywords_luxemburg_eu_national_id_card` 를 찾을 수 있습니다. 
    
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
  
eindeutige id nummer
  
eindeutige id
  
id personnelle
  
numéro d'identification 담당자
  
idpersonnelle #
  
persönliche identifikationsnummer
  
eindeutigeid #
  
## <a name="malta"></a>몰타

### <a name="format"></a>형식

한 문자 앞에 오는 7 자리 숫자
  
### <a name="pattern"></a>패턴

7 자리 숫자를 한 문자 앞에 오는:
  
-  7자리 숫자 
    
- 하나의 대문자 (대/소문자 구분)
    
### <a name="checksum"></a>체크섬

해당 없음
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 정규식 `Regex_malta_eu_national_id_card` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- 키워드에서 `Keywords_malta_eu_national_id_card` 를 찾을 수 있습니다. 
    
DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 65% 신뢰합니다.
  
- 정규식 `Regex_malta_eu_national_id_card` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
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
  
numru ta ' identifikazzjoni uniku
  
numru 게 servizz taċ-ċittadin
  
numru ta' identità uniku
  
## <a name="netherlands"></a>네덜란드

### <a name="format"></a>형식

공백이 나 구분 기호 없이 숫자 9 개
  
### <a name="pattern"></a>패턴

9자리 숫자
  
### <a name="checksum"></a>체크섬

예
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.
  
- 다음은 함수 `Func_netherlands_eu_national_id_card` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- 키워드에서 발견 됩니다.
    
DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 다음은 함수 `Func_netherlands_eu_national_id_card` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
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
  
bsn #
  
persoonlijke numerieke 코드
  
uniek identificatienummer
  
burgerservicenummer
  
uniek identiteitsnummer
  
## <a name="poland"></a>폴란드

자세한 내용은의 섹션을 참조 "폴란드 국가 ID (PESEL)" [에 대 한 중요 한 정보 유형을 확인](what-the-sensitive-information-types-look-for.md)합니다.
  
## <a name="portugal"></a>포르투갈

자세한 내용은의 섹션을 참조 "포르투갈 시민 카드 번호" [에 대 한 중요 한 정보 유형을 확인](what-the-sensitive-information-types-look-for.md)합니다.
  
## <a name="romania"></a>루마니아

### <a name="format"></a>형식

공백 및 구분 기호 없이 13 자릿수
  
### <a name="pattern"></a>패턴

13자리 숫자
  
### <a name="checksum"></a>체크섬

예
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.
  
- 다음은 함수 `Func_romania_eu_national_id_card` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- 키워드에서 `Keywords_romania_eu_national_id_card` 를 찾을 수 있습니다. 
    
DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 다음은 함수 `Func_romania_eu_national_id_card` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
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
  
고정
  
핀 번호
  
보험 번호
  
insurancenumber #
  
고유 id 번호
  
uniqueidentityno #
  
코드 숫자 개인
  
개인 identificare 대구
  
코드 unic identificare
  
număr 개인 unic
  
număr identitate
  
개인 număr identificare
  
număridentitate #
  
codnumericpersonal #
  
numărpersonalunic #
  
## <a name="slovakia"></a>슬로바키아

### <a name="format"></a>형식

하나의 백슬래시를 포함 하는 10 자리 숫자
  
### <a name="pattern"></a>패턴

하나의 백슬래시를 포함 하는 10 자리 숫자:
  
### <a name="checksum"></a>체크섬

예
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.
  
- 다음은 함수 `Func_slovakia_eu_national_id_card` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- 키워드에서 `Keywords_slovakia_eu_national_id_card` 를 찾을 수 있습니다. 
    
DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 다음은 함수 `Func_slovakia_eu_national_id_card` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
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

생일 번호
  
국가 id 번호
  
개인 식별 번호
  
social security number

  
nationalnumber #
  
ssn #
  
ssn
  
국가 번호
  
개인 id 번호
  
personalidnumber #
  
rč
  
rodné číslo
  
rodne cislo
  
## <a name="slovenia"></a>슬로베니아

### <a name="format"></a>형식

공백이 나 구분 기호 없이 13 자릿수
  
### <a name="pattern"></a>패턴

지정된 된 패턴의 자릿수 13:
  
-  "LLL" 해당 생일의 연도의 세 자리 마지막 생일 (DDMMLLL)에 해당 하는 7 자리 숫자 
    
- 생일의 영역에 해당 하는 두 자리 숫자
    
- 성별 및 일련 번호의 조합에 해당 하는 (000 499 1 여자 2 남자에 대 한) 및 500-999 탑재에 대 한 동일한 날에 태어난 사용자에 게는 세 자리 숫자
    
- 하나 이상의 검사 숫자
    
### <a name="checksum"></a>체크섬

예
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.
  
- 다음은 함수 `Func_slovenia_eu_national_id_card` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- 키워드에서 `Keywords_slovenia_eu_national_id_card` 를 찾을 수 있습니다. 
    
DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 다음은 함수 `Func_slovenia_eu_national_id_card` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
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
  
등록 하는 고유 번호
  
고유 id 번호
  
uniqueidentityno #
  
고유 마스터 시민 번호
  
edinstvena identifikacijska številka
  
uniqueidentityno #
  
edinstvena številka glavnega državljana
  
emšo
  
## <a name="spain"></a>스페인

### <a name="format"></a>형식

한 문자 앞에 오는 7 자리 숫자
  
### <a name="pattern"></a>패턴

한 문자 앞에 오는 7 자리 숫자
  
- 7자리 숫자
    
- 한 자리 숫자 또는 문자 (대 소문자 구분 안함)
    
### <a name="checksum"></a>체크섬

해당 없음
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 정규식 `Regex_spain_eu_national_id_card` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- 키워드에서 `Keywords_spain_eu_national_id_card"` 를 찾을 수 있습니다. 
    
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
  
국가 id 번호
  
identity 국가 번호
  
보험 번호
  
개인 식별 번호
  
국가 identity
  
개인 id 없음
  
고유 id 번호
  
nationalidno #
  
uniqueid #
  
dni #
  
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

자세한 내용은의 섹션을 참조 "스웨덴 국가 ID" [에 대 한 중요 한 정보 유형을 확인](what-the-sensitive-information-types-look-for.md)합니다.
  
## <a name="see-also"></a>참고 항목

[중요한 정보 형식이 찾는 항목](what-the-sensitive-information-types-look-for.md)

