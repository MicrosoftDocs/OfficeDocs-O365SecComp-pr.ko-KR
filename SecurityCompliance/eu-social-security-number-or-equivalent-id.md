---
title: EU 주민 등록 번호 또는 동등한 ID
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 8/17/2018
ms.audience: Admin
ms.topic: reference
ms.service: O365-seccomp
localization_priority: Normal
ms.assetid: 1fabd341-e594-4bfe-961c-62aa82893f60
description: 이 항목에서는 DLP (데이터 손실 방지) 정책이 EU 주민 등록 번호 또는 동등한 ID 중요 정보 유형을 검색할 때 찾는 항목을 보여 줍니다. 이 중요 한 정보 유형은 각 국가에 대 한 다양 한 패턴, 키워드 및 기타 증거를 정의 합니다.
ms.openlocfilehash: abcefb6930e9c02d2f32d84b65accfecf1e20d95
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30216528"
---
# <a name="eu-social-security-number-or-equivalent-id"></a>EU 주민 등록 번호 또는 동등한 ID

이 항목에서는 DLP (데이터 손실 방지) 정책이 EU SSN (사회 보장 번호) 또는 동등한 ID 중요 정보 유형을 검색할 때 어떤 사항을 찾을 지를 보여 줍니다. 이 중요 한 정보 유형은 각 국가에 대 한 다양 한 패턴, 키워드 및 기타 증거를 정의 합니다.
  
## <a name="austria"></a>오스트리아

### <a name="format"></a>형식

지정 된 형식의 10 자리 숫자
  
### <a name="pattern"></a>패턴

10자리 숫자:
  
-  일련 번호에 해당 하는 3 자리 숫자 
    
- 검사 숫자 1 개
    
- 생년월일에 해당 하는 6 자리 숫자 (ddmmyy)
    
### <a name="checksum"></a>체크섬

예
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.
  
- 이 함수 `Func_austria_eu_ssn_or_equivalent` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- from `Keywords_austria_eu_ssn_or_equivalent` 키워드를 찾았습니다. 
    
DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 이 함수 `Func_austria_eu_ssn_or_equivalent` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
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

소셜 보안 아니요
  
social security number

  

social security code
  
보험 번호
  
오스트리아
  
ssn
  
ssn
  
보험 코드
  
보험 코드 #
  
사회 alsecurityno #
  
sozialversicherungsnummer
  
soziale sicherheit kein
  
versicherungsnummer
  
## <a name="belgium"></a>벨기에

### <a name="format"></a>형식

공백이 나 구분 기호가 없는 11 자리 숫자
  
### <a name="pattern"></a>패턴

11자리 숫자
  
### <a name="checksum"></a>체크섬

예
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.
  
- 이 함수 `Func_belgium_eu_ssn_or_equivalent` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- from `Keywords_belgium_eu_ssn_or_equivalent` 키워드를 찾았습니다. 
    
DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 이 함수 `Func_belgium_eu_ssn_or_equivalent` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
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

벨기에 국가 번호
  
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
  
numéro 국가
  
numéro de sécurité

  
numéro d'assuré
  
identifiant 국가
  
identifiantnational #
  
numéronational #
  
## <a name="croatia"></a>크로아티아

### <a name="format"></a>형식

공백과 구분 기호를 사용 하지 않고 11 자리 숫자
  
### <a name="pattern"></a>패턴

 11자리 숫자: 
  
-  10 자리 숫자 
    
- 검사 숫자 1 개
    
### <a name="checksum"></a>체크섬

예
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.
  
- 이 함수 `Func_croatia_eu_ssn_or_equivalent` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- from `Keywords_croatia_eu_ssn_or_equivalent` 키워드를 찾았습니다. 
    
DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 이 함수 `Func_croatia_eu_ssn_or_equivalent` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
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
  
국가 식별 번호
  
social security number

  
nationalnumber #
  
ssn
  
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

지정 된 패턴의 10 자리 및 백슬래시
  
### <a name="pattern"></a>패턴

10 자리 숫자와 백슬래시:
  
- 생년월일에 해당 하는 6 자리 숫자 (YYMMDD): 
    
- 백슬래시
    
- 같은 날짜에 태어난 사람을 구분 하는 일련 번호에 해당 하는 3 자리 숫자
    
- 검사 숫자 1 개
    
### <a name="checksum"></a>체크섬

예
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.
  
- 이 함수 `Func_czech_republic_eu_ssn_or_equivalent` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- from `Keywords_czech_republic_eu_ssn_or_equivalent` 키워드를 찾았습니다. 
    
DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 이 함수 `Func_czech_republic_eu_ssn_or_equivalent` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
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

돌 번호
  
국가 식별 번호
  
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
  
## <a name="denmark"></a>덴마크

### <a name="format"></a>형식

지정 된 패턴의 10 자리 및 하이픈
  
### <a name="pattern"></a>패턴

10 자리 숫자와 하이픈:
  
- 생년월일에 해당 하는 6 자리 숫자 (ddmmyy) 
    
- 하이픈
    
- 일련 번호에 해당 하는 4 자리 숫자
    
### <a name="checksum"></a>체크섬

예
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.
  
- 이 함수 `Func_denmark_eu_ssn_or_equivalent` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- from `Keywords_denmark_eu_ssn_or_equivalent` 키워드를 찾았습니다. 
    
DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 이 함수 `Func_denmark_eu_ssn_or_equivalent` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
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
  
국가 식별 번호
  
social security number

  
nationalnumber #
  
ssn
  
ssn
  
국가 번호
  
개인 id 번호
  
personalidnumber #
  
cpr-nummer
  
personnummer
  
## <a name="finland"></a>핀란드

### <a name="format"></a>형식

지정 된 형식의 11 자 조합
  
### <a name="pattern"></a>패턴

다음은 지정 된 형식의 11 자 조합입니다.
  
-  6자리 숫자 
    
- 다음 중 하나의 인스턴스에 대해 다음을 수행 합니다.
    
  - 더하기 기호
    
  - 빼기 기호
    
  - 문자 "A" (대/소문자 구분 안 함)
    
- 3자리 숫자
    
- 1 개의 문자 또는 1 자리 숫자
    
### <a name="checksum"></a>체크섬

예
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.
  
- 이 함수 `Func_finland_eu_ssn_or_equivalent` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- from `Keywords_finland_eu_ssn_or_equivalent` 키워드를 찾았습니다. 
    
DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 이 함수 `Func_finland_eu_ssn_or_equivalent` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
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
  
id 번호
  
핀란드어 국가 id 번호
  
personalidnumber #
  
국가 식별 번호
  
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
  
henkilötunnusnumero #
  
kansallisen tunnistenumero
  
tunnusnumero
  
kansallinen tunnus numero
  
hetu
  
## <a name="france"></a>프랑스

자세한 내용은 [중요 한 정보 유형이 찾는](what-the-sensitive-information-types-look-for.md)"프랑스 사회 보장 번호 (INSEE)" 섹션을 참조 하십시오.
  
## <a name="germany"></a>독일

자세한 내용은 [중요 한 정보 유형이 찾는](what-the-sensitive-information-types-look-for.md)"독일 id 카드 번호" 섹션을 참조 하십시오.
  
## <a name="greece"></a>그리스

자세한 내용은 [중요 한 정보 유형이 찾는](what-the-sensitive-information-types-look-for.md)"그리스 국가 ID 카드" 섹션을 참조 하십시오.
  
## <a name="hungary"></a>헝가리

### <a name="format"></a>형식

공백과 구분 기호를 사용 하지 않고 9 자리 숫자
  
### <a name="pattern"></a>패턴

9자리 숫자
  
### <a name="checksum"></a>체크섬

예
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.
  
- 이 함수 `Func_hungary_eu_ssn_or_equivalent` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- from `Keywords_hungary_eu_ssn_or_equivalent` 키워드를 찾았습니다. 
    
DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 이 함수 `Func_hungary_eu_ssn_or_equivalent` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
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

헝가리어 주민 등록 번호
  
social security number

  
사회 alsecurity번호 #
  
hssn #
  
socialsecuritynno
  
hssn
  
taj
  
taj #
  
ssn
  
ssn
  
소셜 보안 아니요
  
áfa
  
közösségi adószám
  
általános forgalmi adó
  
hozzáadottérték adó
  
áfa szám
  
magyar áfa szám
  
## <a name="portugal"></a>포르투갈

자세한 내용은 [중요 한 정보 유형이 찾는](what-the-sensitive-information-types-look-for.md)"포르투갈 시민이 카드 번호" 섹션을 참조 하십시오.
  
## <a name="spain"></a>스페인

자세한 내용은 [중요 한 정보 유형이 찾는](what-the-sensitive-information-types-look-for.md)"스페인 SSN (사회 보장 번호)" 섹션을 참조 하십시오.
  
## <a name="sweden"></a>스웨덴

### <a name="format"></a>형식

공백과 구분 기호를 사용 하지 않고 12 자리 숫자
  
### <a name="pattern"></a>패턴

12자리 숫자:
  
-  출생 날짜에 해당 하는 8 자리 숫자 (YYYYMMDD) 
    
- 일련 번호에 해당 하는 3 자리 숫자: 
    
  - 일련 번호의 마지막 숫자는 남성에 홀수를 할당 하는 성별과 암의 짝수를 나타냅니다.
    
  - 최대 1990의 일련 번호를 사용 하 여 전화를 corresponded 하는 국가, 즉 세금 레코드에 따라 (1947 이전에 태어난 경우)에는에 대 한 작업을 수행 하는 경우 (예를 들어 세금이 기록 됨) immigrants 
    
- 검사 숫자 1 개
    
### <a name="checksum"></a>체크섬

예
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.
  
- 이 함수 `Func_sweden_eu_ssn_or_equivalent` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- from `Keywords_sweden_eu_ssn_or_equivalent` 키워드를 찾았습니다. 
    
DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 이 함수 `Func_sweden_eu_ssn_or_equivalent` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
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
  
identity no
  
id 아니요
  
개인 식별 아니요
  
personnummer id
  
personligt id-nummer
  
unikt id-nummer
  
personnummer
  
identifikationsnumret
  
personnummer #
  
identifikationsnumret #
  
## <a name="see-also"></a>참고 항목

[중요한 정보 형식이 찾는 항목](what-the-sensitive-information-types-look-for.md)

