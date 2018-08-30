---
title: EU 사회보장 번호 또는에 상응 하는 ID
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 8/17/2018
ms.audience: Admin
ms.topic: reference
ms.service: o365-administration
localization_priority: Normal
ms.assetid: 1fabd341-e594-4bfe-961c-62aa82893f60
description: 이 항목에서는 EU 사회보장 번호 또는 해당 하는 ID 중요 한 정보 유형을 감지 하는 경우의 데이터 손실 방지 (DLP) 정책을 찾아에 대해 보여줍니다. 이 중요 한 정보 유형 다양 한 패턴, 키워드 및 각 국가 대 한 기타 증거를 정의합니다.
ms.openlocfilehash: 6f1027dcfb648ed937b8180d74d4bc6348dab650
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22533379"
---
# <a name="eu-social-security-number-or-equivalent-id"></a>EU 사회보장 번호 또는에 상응 하는 ID

이 항목에서는 EU 사회보장 번호 (SSN) 또는 해당 하는 ID 중요 한 정보 유형을 감지 하는 경우의 데이터 손실 방지 (DLP) 정책을 찾아에 대해 보여줍니다. 이 중요 한 정보 유형 다양 한 패턴, 키워드 및 각 국가 대 한 기타 증거를 정의합니다.
  
## <a name="austria"></a>오스트리아

### <a name="format"></a>형식

지정 된 형식에서 10 자 사이일
  
### <a name="pattern"></a>패턴

10자리 숫자:
  
-  일련 번호에 해당 하는 세 자리 숫자 
    
- 하나 이상의 검사 숫자
    
- 생일 (DDMMYY)에 해당 하는 6 자리 숫자
    
### <a name="checksum"></a>체크섬

예
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.
  
- 다음은 함수 `Func_austria_eu_ssn_or_equivalent` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- 키워드에서 `Keywords_austria_eu_ssn_or_equivalent` 를 찾을 수 있습니다. 
    
DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 다음은 함수 `Func_austria_eu_ssn_or_equivalent` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
```
 <!-- EU SSN or Equivalent Number -->
<Entity id="d24e32a4-c0bb-4ba8-899d-6303b95742d9" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_austria_eu_ssn_or_equivalent" />
          <Match idRef="Keywords_austria_eu_ssn_or_equivalent" />
        </Pattern>
<Pattern confidenceLevel="75">
            <IdMatch idRef="Func_austria_eu_ssn_or_equivalent" />
          </Pattern>
</Entity>
```

### <a name="keywords"></a>키워드

#### <a name="keywordsaustriaeussnorequivalent"></a>Keywords_austria_eu_ssn_or_equivalent

주민등록 없음
  
social security number

  

social security code
  
보험 번호
  
오스트리아 ssn
  
ssn #
  
ssn
  
보험 코드
  
보험 코드 #
  
socialsecurityno #
  
sozialversicherungsnummer
  
soziale 독일어 kein
  
versicherungsnummer
  
## <a name="belgium"></a>벨기에

### <a name="format"></a>형식

공백이 나 구분 기호 없이 11 자리 숫자
  
### <a name="pattern"></a>패턴

11자리 숫자
  
### <a name="checksum"></a>체크섬

예
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.
  
- 다음은 함수 `Func_belgium_eu_ssn_or_equivalent` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- 키워드에서 `Keywords_belgium_eu_ssn_or_equivalent` 를 찾을 수 있습니다. 
    
DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 다음은 함수 `Func_belgium_eu_ssn_or_equivalent` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
```
 <!-- EU SSN or Equivalent Number -->
<Entity id="d24e32a4-c0bb-4ba8-899d-6303b95742d9" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_belgium_eu_ssn_or_equivalent" />
          <Match idRef="Keywords_belgium_eu_ssn_or_equivalent" />
        </Pattern> 
       <Pattern confidenceLevel="75">
          <IdMatch idRef="Func_belgium_eu_ssn_or_equivalent" />
        </Pattern>      
</Entity>
```

### <a name="keywords"></a>키워드

#### <a name="keywordsbelgiumeussnorequivalent"></a>Keywords_belgium_eu_ssn_or_equivalent

국가 번호 (벨기에)
  
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
  
numéro 국가
  
numéro de sécurité

  
numéro d'assuré
  
identifiant 국가
  
identifiantnational #
  
numéronational #
  
## <a name="croatia"></a>크로아티아

### <a name="format"></a>형식

공백 및 구분 기호 없이 11 자리 숫자
  
### <a name="pattern"></a>패턴

 11자리 숫자: 
  
-  10 자리 숫자 
    
- 하나 이상의 검사 숫자
    
### <a name="checksum"></a>체크섬

예
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.
  
- 다음은 함수 `Func_croatia_eu_ssn_or_equivalent` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- 키워드에서 `Keywords_croatia_eu_ssn_or_equivalent` 를 찾을 수 있습니다. 
    
DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 다음은 함수 `Func_croatia_eu_ssn_or_equivalent` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
```
 <!-- EU SSN or Equivalent Number -->
<Entity id="d24e32a4-c0bb-4ba8-899d-6303b95742d9" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_croatia_eu_ssn_or_equivalent" />
          <Match idRef="Keywords_croatia_eu_ssn_or_equivalent" />
        </Pattern> 
       <Pattern confidenceLevel="75">
          <IdMatch idRef="Func_croatia_eu_ssn_or_equivalent" />
        </Pattern>      
</Entity>
```

### <a name="keywords"></a>키워드

#### <a name="keywordscroatiaeussnorequivalent"></a>Keywords_croatia_eu_ssn_or_equivalent

개인 식별 번호
  
마스터 시민 번호
  
국가 id 번호
  
social security number

  
nationalnumber #
  
ssn #
  
ssn
  
nationalnumber
  
bnn #
  
bnn
  
개인 id 번호
  
personalidnumber #
  
oib
  
osobni identifikacijski broj
  
## <a name="czech-republic"></a>체코 공화국

### <a name="format"></a>형식

10 자리 숫자와 지정한 패턴에 백슬래시
  
### <a name="pattern"></a>패턴

10 자리 숫자와 백슬래시:
  
- 생일 (YYMMDD)에 해당 하는 6 자리 숫자: 
    
- 백슬래시
    
- 같은 날짜 탄생 하 게 하는 사용자를 구분 하는 일련 번호에 해당 하는 세 자리 숫자
    
- 하나 이상의 검사 숫자
    
### <a name="checksum"></a>체크섬

예
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.
  
- 다음은 함수 `Func_czech_republic_eu_ssn_or_equivalent` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- 키워드에서 `Keywords_czech_republic_eu_ssn_or_equivalent` 를 찾을 수 있습니다. 
    
DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 다음은 함수 `Func_czech_republic_eu_ssn_or_equivalent` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
```
 <!-- EU SSN or Equivalent Number -->
<Entity id="d24e32a4-c0bb-4ba8-899d-6303b95742d9" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_czech_republic_eu_ssn_or_equivalent" />
          <Match idRef="Keywords_czech_republic_eu_ssn_or_equivalent" />
        </Pattern> 
       <Pattern confidenceLevel="75">
          <IdMatch idRef="Func_czech_republic_eu_ssn_or_equivalent" />
        </Pattern>      
</Entity>
```

### <a name="keywords"></a>키워드

#### <a name="keywordsczechrepubliceussnorequivalent"></a>Keywords_czech_republic_eu_ssn_or_equivalent

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
  
## <a name="denmark"></a>덴마크

### <a name="format"></a>형식

10 자리 숫자 및 지정된 된 패턴에 하이픈
  
### <a name="pattern"></a>패턴

10 자리 숫자 및 하이픈:
  
- 생일 (DDMMYY)에 해당 하는 6 자리 숫자 
    
- 하이픈
    
- 시퀀스 번호에 해당 하는 4 자리 숫자
    
### <a name="checksum"></a>체크섬

예
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.
  
- 다음은 함수 `Func_denmark_eu_ssn_or_equivalent` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- 키워드에서 `Keywords_denmark_eu_ssn_or_equivalent` 를 찾을 수 있습니다. 
    
DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 다음은 함수 `Func_denmark_eu_ssn_or_equivalent` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
```
 <!-- EU SSN or Equivalent Number -->
<Entity id="d24e32a4-c0bb-4ba8-899d-6303b95742d9" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_denmark_eu_ssn_or_equivalent" />
          <Match idRef="Keywords_denmark_eu_ssn_or_equivalent" />
        </Pattern> 
       <Pattern confidenceLevel="75">
          <IdMatch idRef="Func_denmark_eu_ssn_or_equivalent" />
        </Pattern>      
</Entity>
```

### <a name="keywords"></a>키워드

#### <a name="keywordsdenmarkeussnorequivalent"></a>Keywords_denmark_eu_ssn_or_equivalent

개인 식별 번호
  
국가 id 번호
  
social security number

  
nationalnumber #
  
ssn #
  
ssn
  
국가 번호
  
개인 id 번호
  
personalidnumber #
  
cpr nummer
  
personnummer
  
## <a name="finland"></a>핀란드

### <a name="format"></a>형식

지정 된 형식에는 11 자리의 조합
  
### <a name="pattern"></a>패턴

지정 된 형식에는 11 자리의 조합 합니다.
  
-  6자리 숫자 
    
- 하나의 인스턴스는 다음 중 하나:
    
  - 더하기 기호
    
  - 빼기 기호
    
  - "A" 문자 (대 소문자 구분 안함)
    
- 3자리 숫자
    
- 하나의 문자 또는 한 자리 숫자
    
### <a name="checksum"></a>체크섬

예
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.
  
- 다음은 함수 `Func_finland_eu_ssn_or_equivalent` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- 키워드에서 `Keywords_finland_eu_ssn_or_equivalent` 를 찾을 수 있습니다. 
    
DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 다음은 함수 `Func_finland_eu_ssn_or_equivalent` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
```
 <!-- EU SSN or Equivalent Number -->
<Entity id="d24e32a4-c0bb-4ba8-899d-6303b95742d9" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_finland_eu_ssn_or_equivalent" />
          <Match idRef="Keywords_finland_eu_ssn_or_equivalent" />
        </Pattern> 
       <Pattern confidenceLevel="75">
          <IdMatch idRef="Func_finland_eu_ssn_or_equivalent" />
        </Pattern>      
</Entity>
```

### <a name="keywords"></a>키워드

#### <a name="keywordsfinlandeussnorequivalent"></a>Keywords_finland_eu_ssn_or_equivalent

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
  
hetu
  
## <a name="france"></a>프랑스

자세한 내용은의 섹션을 참조 "프랑스 사회보장 번호 (INSEE)" [에 대 한 중요 한 정보 유형을 확인](what-the-sensitive-information-types-look-for.md)합니다.
  
## <a name="germany"></a>독일

자세한 내용은의 섹션을 참조 "독일 Id 카드 번호" [에 대 한 중요 한 정보 유형을 확인](what-the-sensitive-information-types-look-for.md)합니다.
  
## <a name="greece"></a>그리스

자세한 내용은의 섹션을 참조 "그리스 국가 ID 카드" [에 대 한 중요 한 정보 유형을 확인](what-the-sensitive-information-types-look-for.md)합니다.
  
## <a name="hungary"></a>헝가리

### <a name="format"></a>형식

공백 및 구분 기호 없이 숫자 9 개
  
### <a name="pattern"></a>패턴

9자리 숫자
  
### <a name="checksum"></a>체크섬

예
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.
  
- 다음은 함수 `Func_hungary_eu_ssn_or_equivalent` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- 키워드에서 `Keywords_hungary_eu_ssn_or_equivalent` 를 찾을 수 있습니다. 
    
DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 다음은 함수 `Func_hungary_eu_ssn_or_equivalent` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
```
 <!-- EU SSN or Equivalent Number -->
<Entity id="d24e32a4-c0bb-4ba8-899d-6303b95742d9" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_hungary_eu_ssn_or_equivalent" />
          <Match idRef="Keywords_hungary_eu_ssn_or_equivalent" />
        </Pattern> 
       <Pattern confidenceLevel="75">
          <IdMatch idRef="Func_hungary_eu_ssn_or_equivalent" />
        </Pattern>      
</Entity>
```

### <a name="keywords"></a>키워드

#### <a name="keywordshungaryeussnorequivalent"></a>Keywords_hungary_eu_ssn_or_equivalent

헝가리어 사회보장 번호
  
social security number

  
socialsecuritynumber #
  
hssn #
  
socialsecuritynno
  
hssn
  
taj
  
taj #
  
ssn
  
ssn #
  
주민등록 없음
  
áfa
  
közösségi adószám
  
általános forgalmi adó szám
  
hozzáadottérték adó
  
áfa szám
  
magyar áfa szám
  
## <a name="portugal"></a>포르투갈

자세한 내용은의 섹션을 참조 "포르투갈 시민 카드 번호" [에 대 한 중요 한 정보 유형을 확인](what-the-sensitive-information-types-look-for.md)합니다.
  
## <a name="spain"></a>스페인

자세한 내용은의 섹션을 참조 "스페인 사회보장 번호 (SSN)" [에 대 한 중요 한 정보 유형을 확인](what-the-sensitive-information-types-look-for.md)합니다.
  
## <a name="sweden"></a>스웨덴

### <a name="format"></a>형식

공백 및 구분 기호 없이 12 자리
  
### <a name="pattern"></a>패턴

12자리 숫자:
  
-  생일 (YYYYMMDD)에 해당 하는 8 개의 자릿수 
    
- 일련 번호에 해당 하는 세 자리 숫자입니다. 
    
  - 일련번호에서 마지막 숫자 1 여자 2 남자 하는 것이 홀수와 짝수 탑재에 대 한 할당 하 여 성별을 나타냅니다.
    
  - 1990, 최대 일련번호의 배정에 상응는 국가 번호의 bearer 출생 하거나 (1947 하기 전에 태어난) 하는 경우 여기에서 자신이 명의 된 살고 있는, 세금 레코드에 따라 1947, 1 월 1에서 특수 코드 (일반적으로 7 자리 수로 9)에 대 한 immigrants 
    
- 하나 이상의 검사 숫자
    
### <a name="checksum"></a>체크섬

예
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.
  
- 다음은 함수 `Func_sweden_eu_ssn_or_equivalent` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- 키워드에서 `Keywords_sweden_eu_ssn_or_equivalent` 를 찾을 수 있습니다. 
    
DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 다음은 함수 `Func_sweden_eu_ssn_or_equivalent` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
```
 <!-- EU SSN or Equivalent Number -->
<Entity id="d24e32a4-c0bb-4ba8-899d-6303b95742d9" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_sweden_eu_ssn_or_equivalent" />
          <Match idRef="Keywords_sweden_eu_ssn_or_equivalent" />
        </Pattern> 
       <Pattern confidenceLevel="75">
          <IdMatch idRef="Func_sweden_eu_ssn_or_equivalent" />
        </Pattern>      
</Entity>
```

### <a name="keywords"></a>키워드

#### <a name="keywordsswedeneussnorequivalent"></a>Keywords_sweden_eu_ssn_or_equivalent

개인 id 번호
  
identification number

  
개인 id 없음
  
identity 없음
  
식별 없음
  
개인 식별 없음
  
personnummer id
  
personligt id nummer
  
unikt id nummer
  
personnummer
  
identifikationsnumret
  
personnummer #
  
identifikationsnumret #
  
## <a name="see-also"></a>참고 항목

[중요한 정보 형식이 찾는 항목](what-the-sensitive-information-types-look-for.md)

