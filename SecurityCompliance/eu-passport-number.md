---
title: EU 여권 번호
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 8/16/2018
ms.audience: Admin
ms.topic: reference
ms.service: O365-seccomp
ms.collection: M365-security-compliance
localization_priority: Normal
description: 이 항목에서는 DLP (데이터 손실 방지) 정책이 EU (유럽 여권 번호) 중요 한 정보 유형을 검색할 때 찾는 항목을 보여 줍니다. 이 중요 한 정보 유형은 각 국가에 대 한 다양 한 패턴, 키워드 및 기타 증거를 정의 합니다.
ms.openlocfilehash: 3ab92e87607f41cffa8c15f1179a4eef5369cb29
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32256826"
---
# <a name="eu-passport-number"></a>EU 여권 번호

이 항목에서는 DLP (데이터 손실 방지) 정책이 EU (유럽 여권 번호) 중요 한 정보 유형을 검색할 때 찾는 항목을 보여 줍니다. 이 중요 한 정보 유형은 각 국가에 대 한 다양 한 패턴, 키워드 및 기타 증거를 정의 합니다.
  
## <a name="austria"></a>오스트리아

### <a name="format"></a>형식일

1 개의 문자 다음에 선택적 공백, 일곱 자리 숫자
  
### <a name="pattern"></a>패턴

한 글자, 일곱 자리 및 한 가지 공백 조합입니다.
  
- 1개 문자(대/소문자 구분 안 함)
    
- 1 개의 공백 (선택 사항)
    
- 7자리 숫자
    
### <a name="checksum"></a>제외

해당 없음
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 정규식이 해당 `Regex_austria_eu_passport_number` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- from `Keywords_austria_eu_passport_number` 키워드를 찾았습니다. 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_austria_eu_passport_number" />
          <Match idRef="Keywords_austria_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>키워드

| |
|**Keywords_austria_eu_passport_number**|
|:-----|
|passport number  <br/> 오스트리아 여권 번호  <br/> passport 아니요  <br/> reisepass  <br/> österreichisch reisepass  <br/> |
   
## <a name="belgium"></a>벨기에

### <a name="format"></a>형식일

공백 또는 구분 기호가 없는 2 개 문자 다음에 6 자리 숫자 사용
  
### <a name="pattern"></a>패턴

2 개 문자 및 6 자리 숫자
  
### <a name="checksum"></a>제외

해당 없음
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 정규식이 해당 `Regex_belgium_eu_passport_number` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- from `Keywords_belgium_eu_passport_number` 키워드를 찾았습니다. 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_belgium__eu_passport_number" />
          <Match idRef="Keywords_belgium_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>키워드

| |
|**Keywords_belgium_eu_passport_number**|
|:-----|
|passport number  <br/> 벨기에 여권 번호  <br/> passport 아니요  <br/> 고 대/ort  <br/> paspoortnummer  <br/> reisepass kein  <br/> reisepass  <br/> |
   
## <a name="bulgaria"></a>불가리아

### <a name="format"></a>형식일

공백과 구분 기호를 사용 하지 않고 9 자리 숫자
  
### <a name="pattern"></a>패턴

 9자리 숫자 
  
### <a name="checksum"></a>제외

아니요
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 정규식이 해당 `Regex_bulgaria_eu_passport_number` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- from `Keywords_bulgaria_eu_passport_number` 키워드를 찾았습니다. 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_bulgaria_eu_passport_number" />
          <Match idRef="Keywords_bulgaria_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>키워드

| |
|**Keywords_bulgaria_eu_passport_number**|
|:-----|
|passport number  <br/> 불가리아어 여권 번호  <br/> passport 아니요  <br/> номер на паспорта  <br/> |
   
## <a name="croatia"></a>크로아티아

### <a name="format"></a>형식일

공백과 구분 기호를 사용 하지 않고 9 자리 숫자
  
### <a name="pattern"></a>패턴

 9자리 숫자 
  
### <a name="checksum"></a>제외

아니요
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 정규식이 해당 `Regex_croatia_eu_passport_number` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- from `Keywords_croatia_eu_passport_number` 키워드를 찾았습니다. 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_croatia_eu_passport_number" />
          <Match idRef="Keywords_croatia_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>키워드

| |
|**Keywords_croatia_eu_passport_number**|
|:-----|
|passport number  <br/> 크로아티아어 여권 번호  <br/> passport 아니요  <br/> broj putovnice  <br/> |
   
## <a name="cyprus"></a>키프로스

### <a name="format"></a>형식일

공백 또는 구분 기호가 없는 1 개 문자 다음에 6-8 자리 숫자
  
### <a name="pattern"></a>패턴

한 문자 다음에 6 ~ 8 자리 숫자
  
### <a name="checksum"></a>제외

아니요
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 정규식이 해당 `Regex_cyprus_eu_passport_number` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- from `Keywords_cyprus_eu_passport_number` 키워드를 찾았습니다. 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_cyprus_eu_passport_number" />
          <Match idRef="Keywords_cyprus_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>키워드

| |
|**Keywords_cyprus_eu_passport_number**|
|:-----|
|passport number  <br/> 키프로스 여권 번호  <br/> passport 아니요  <br/> αριθμό διαβατηρίου  <br/> |
   
## <a name="czech-republic"></a>체코 공화국

### <a name="format"></a>형식일

공백이 나 구분 기호가 없는 8 자리 숫자
  
### <a name="pattern"></a>패턴

공백이 나 구분 기호가 없는 8 자리 숫자
  
### <a name="checksum"></a>제외

아니요
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 정규식이 해당 `Regex_czech_republic_eu_passport_number` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- from `Keywords_czech_republic_eu_passport_number` 키워드를 찾았습니다. 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_czech_republic_eu_passport_number" />
          <Match idRef="Keywords_czech_republic_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>키워드

| |
|**Keywords_czech_republic_eu_passport_number**|
|:-----|
|passport number  <br/> 체코어 여권 번호  <br/> passport 아니요  <br/> cestovní pas  <br/> pas  <br/> |
   
## <a name="denmark"></a>덴마크

### <a name="format"></a>형식일

공백과 구분 기호를 사용 하지 않고 9 자리 숫자
  
### <a name="pattern"></a>패턴

 9자리 숫자 
  
### <a name="checksum"></a>제외

아니요
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 정규식이 해당 `Regex_denmark_eu_passport_number` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- from `Keywords_denmark_eu_passport_number` 키워드를 찾았습니다. 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_denmark_eu_passport_number" />
          <Match idRef="Keywords_denmark_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>키워드

| |
|**Keywords_denmark_eu_passport_number**|
|:-----|
|passport number  <br/> 덴마크어 여권 번호  <br/> passport 아니요  <br/> pas  <br/> pasnummer  <br/> |
   
## <a name="estonia"></a>에스토니아

### <a name="format"></a>형식일

공백 또는 구분 기호가 없는 1 개 문자 다음에 7 자리 숫자
  
### <a name="pattern"></a>패턴

1 개의 문자 다음에 7 자리 숫자
  
### <a name="checksum"></a>제외

아니요
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 정규식이 해당 `Regex_estonia_eu_passport_number` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- from `Keywords_estonia_eu_passport_number` 키워드를 찾았습니다. 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_estonia_eu_passport_number" />
          <Match idRef="Keywords_estonia_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>키워드

| |
|**Keywords_estonia_eu_passport_number**|
|:-----|
|passport number  <br/> 에스토니아어 여권 번호  <br/> passport 아니요  <br/> eesti kodaniku pass  <br/> |
   
## <a name="finland"></a>핀란드

자세한 내용은 [중요 한 정보 유형이 찾는](what-the-sensitive-information-types-look-for.md)"핀란드 여권 번호" 섹션을 참조 하십시오.
  
## <a name="france"></a>프랑스

자세한 내용은 [중요 한 정보 유형이 찾는](what-the-sensitive-information-types-look-for.md)"프랑스 여권 번호" 섹션을 참조 하십시오.
  
## <a name="germany"></a>독일

자세한 내용은 [중요 한 정보 유형이 찾는](what-the-sensitive-information-types-look-for.md)"독일 여권 번호" 섹션을 참조 하십시오.
  
## <a name="greece"></a>그리스

### <a name="format"></a>형식일

공백 또는 구분 기호가 없는 7 자리, 두 문자
  
### <a name="pattern"></a>패턴

2개 문자와 7자리 숫자
  
### <a name="checksum"></a>제외

아니요
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 정규식이 해당 `Regex_greece_eu_passport_number` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- from `Keywords_greece_eu_passport_number` 키워드를 찾았습니다. 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_greece_eu_passport_number" />
          <Match idRef="Keywords_greece_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>키워드

| |
|**Keywords_greece_eu_passport_number**|
|:-----|
|passport number  <br/> 그리스 여권 번호  <br/> passport 아니요  <br/> διαβατηριο  <br/> |
   
## <a name="hungary"></a>헝가리

### <a name="format"></a>형식일

공백 또는 구분 기호가 없는 2 개 문자 및 6 자리 숫자
  
### <a name="pattern"></a>패턴

2 개의 문자 다음에 6 개 또는 7 개의 숫자
  
### <a name="checksum"></a>제외

아니요
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 정규식이 해당 `Regex_hungary_eu_passport_number` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- from `Keywords_hungary_eu_passport_number` 키워드를 찾았습니다. 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_hungary_eu_passport_number" />
          <Match idRef="Keywords_hungary_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>키워드

| |
|**Keywords_hungary_eu_passport_number**|
|:-----|
|passport number  <br/> 헝가리어 여권 번호  <br/> passport 아니요  <br/> útlevél száma  <br/> |
   
## <a name="ireland"></a>Ireland

### <a name="format"></a>형식일

공백이 나 구분 기호가 없는 두 개의 문자 또는 숫자와 7 자리 숫자
  
### <a name="pattern"></a>패턴

두 개의 문자 또는 숫자와 7 자리 숫자:
  
- 2자리 숫자 또는 문자(대/소문자 구분 안 함)
    
- 7자리 숫자
    
### <a name="checksum"></a>제외

아니요
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 정규식이 해당 `Regex_ireland_eu_passport_number` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- from `Keywords_ireland_eu_passport_number` 키워드를 찾았습니다. 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_ireland_eu_passport_number" />
          <Match idRef="Keywords_ireland_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>키워드

| |
|**Keywords_ireland_eu_passport_number**|
|:-----|
|passport number  <br/> 아일랜드 여권 번호  <br/> passport 아니요  <br/> pas  <br/> 여권  <br/> 포트  <br/> 포트 numero  <br/> |
   
## <a name="italy"></a>이탈리아

### <a name="format"></a>형식일

공백이 나 구분 기호가 없는 두 개의 문자 또는 숫자와 7 자리 숫자
  
### <a name="pattern"></a>패턴

두 개의 문자 또는 숫자와 7 자리 숫자:
  
- 2자리 숫자 또는 문자(대/소문자 구분 안 함)
    
- 7자리 숫자
    
### <a name="checksum"></a>제외

해당 없음
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 정규식이 해당 `Regex_italy_eu_passport_number` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- from `Keywords_italy_eu_passport_number` 키워드를 찾았습니다. 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_italy_eu_passport_number" />
          <Match idRef="Keywords_italy_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>키워드

| |
|**Keywords_italy_eu_passport_number**|
|:-----|
|이탈리아 여권 번호  <br/> repubblica italiana passaporto  <br/> passaporto  <br/> passaporto italiana  <br/> passport number  <br/> italiana passaporto numero  <br/> passaporto numero  <br/> numéro) 포트 italien  <br/> numéro (고) 포트  <br/> |
   
## <a name="latvia"></a>라트비아

### <a name="format"></a>형식일

공백이 나 구분 기호가 없는 두 개의 문자 또는 숫자와 7 자리 숫자
  
### <a name="pattern"></a>패턴

두 개의 문자 또는 숫자와 7 자리 숫자:
  
- 2자리 숫자 또는 문자(대/소문자 구분 안 함)
    
- 7자리 숫자
    
### <a name="checksum"></a>제외

아니요
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 정규식이 해당 `Regex_latvia_eu_passport_number` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- from `Keywords_latvia_eu_passport_number` 키워드를 찾았습니다. 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_latvia_eu_passport_number" />
          <Match idRef="Keywords_latvia_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>키워드

| |
|**Keywords_latvia_eu_passport_number**|
|:-----|
|passport number  <br/> 라트비아어 여권 번호  <br/> passport 아니요  <br/> pase numurs  <br/> |
   
## <a name="lithuania"></a>리투아니아

### <a name="format"></a>형식일

공백이 나 구분 기호가 없는 8 자리 숫자 또는 문자
  
### <a name="pattern"></a>패턴

8 자리 숫자 또는 문자 (대/소문자 구분 안 함)
  
### <a name="checksum"></a>제외

해당 없음
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 정규식이 해당 `Regex_lithuania_eu_passport_number` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- from `Keywords_lithuania_eu_passport_number` 키워드를 찾았습니다. 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_lithuania_eu_passport_number" />
          <Match idRef="Keywords_lithuania_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>키워드

| |
|**Keywords_lithuania_eu_passport_number**|
|:-----|
|passport number  <br/> lithunian 여권 번호  <br/> passport 아니요  <br/> numeris  <br/> |
   
## <a name="luxemburg"></a>셈

### <a name="format"></a>형식일

공백이 나 구분 기호가 없는 8 자리 숫자 또는 문자
  
### <a name="pattern"></a>패턴

8 자리 숫자 또는 문자 (대/소문자 구분 안 함)
  
### <a name="checksum"></a>제외

아니요
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 정규식이 해당 `Regex_nation_eu_passport_number` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- from `Keywords_nation_eu_passport_number` 키워드를 찾았습니다. 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_nation_eu_passport_number" />
          <Match idRef="Keywords_nation_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>키워드

| |
|**Keywords_nation_eu_passport_number**|
|:-----|
|passport number  <br/> 라트비아어 여권 번호  <br/> passport 아니요  <br/> passnummer  <br/> |
   
## <a name="malta"></a>몰타

### <a name="format"></a>형식일

공백이 나 구분 기호 없이 7 자리 숫자
  
### <a name="pattern"></a>패턴

 7자리 숫자 
  
### <a name="checksum"></a>제외

아니요
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 정규식이 해당 `Regex_malta_eu_passport_number` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- from `Keywords_malta_eu_passport_number` 키워드를 찾았습니다. 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_malta_eu_passport_number" />
          <Match idRef="Keywords_malta_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>키워드

| |
|**Keywords_malta_eu_passport_number**|
|:-----|
|passport number  <br/> 몰타어 여권 번호  <br/> passport 아니요  <br/> numru-passaport  <br/> |
   
## <a name="netherlands"></a>네덜란드

### <a name="format"></a>형식일

공백이 나 구분 기호가 없는 9 개의 문자 또는 숫자
  
### <a name="pattern"></a>패턴

9 개의 문자 또는 숫자
  
### <a name="checksum"></a>제외

해당 없음
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 정규식이 해당 `Regex_netherlands_eu_passport_number` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- from `Keywords_netherlands_eu_passport_number` 키워드를 찾았습니다. 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_netherlands_eu_passport_number" />
          <Match idRef="Keywords_netherlands_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>키워드

| |
|**Keywords_netherlands_eu_passport_number**|
|:-----|
|네덜란드어 여권 번호  <br/> passport number  <br/> 네덜란드 여권 번호  <br/> nederlanden, nummer ort  <br/> 고 대/ort  <br/> nederlanden paspoortnummer  <br/> paspoortnummer  <br/> |
   
## <a name="poland"></a>폴란드

자세한 내용은 [중요 한 정보 유형이 찾는](what-the-sensitive-information-types-look-for.md)"폴란드 여권 번호" 섹션을 참조 하십시오.
  
## <a name="portugal"></a>포르투갈

### <a name="format"></a>형식일

공백 또는 구분 기호가 없는 한 문자 다음에 6 자리 숫자
  
### <a name="pattern"></a>패턴

1 개의 문자 다음에 6 자리 숫자:
  
- 1개 문자(대/소문자 구분 안 함)
    
- 6자리 숫자
    
### <a name="checksum"></a>제외

아니요
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 정규식이 해당 `Regex_portugal_eu_passport_number` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- from `Keywords_portugal_eu_passport_number` 키워드를 찾았습니다. 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_portugal_eu_passport_number" />
          <Match idRef="Keywords_portugal_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>키워드

| |
|**Keywords_portugal_eu_passport_number**|
|:-----|
|passport number  <br/> 포르투갈어 passport 번호  <br/> passport 아니요  <br/> número do passaporte  <br/> |
   
## <a name="romania"></a>루마니아

### <a name="format"></a>형식일

공백과 구분 기호를 사용 하지 않고 8 또는 9 자리 숫자
  
### <a name="pattern"></a>패턴

8 또는 9 자리 숫자
  
### <a name="checksum"></a>제외

아니요
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 정규식이 해당 `Regex_romania_eu_passport_number` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- from `Keywords_romania_eu_passport_number` 키워드를 찾았습니다. 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_romania_eu_passport_number" />
          <Match idRef="Keywords_romania_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>키워드

| |
|**Keywords_romania_eu_passport_number**|
|:-----|
|passport number  <br/> 루마니아어 여권 번호  <br/> passport 아니요  <br/> numărul pașaportului  <br/> |
   
## <a name="slovakia"></a>슬로바키아

### <a name="format"></a>형식일

공백 또는 구분 기호가 없는 한 자리 숫자 또는 문자 다음에 일곱 자리 숫자
  
### <a name="pattern"></a>패턴

1 자리 숫자 또는 문자 (대/소문자 구분 안 함)와 7 자리 숫자
  
### <a name="checksum"></a>제외

아니요
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 정규식이 해당 `Regex_slovakia_eu_passport_number` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- from `Keywords_slovakia_eu_passport_number` 키워드를 찾았습니다. 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_slovakia_eu_passport_number" />
          <Match idRef="Keywords_slovakia_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>키워드

| |
|**Keywords_slovakia_eu_passport_number**|
|:-----|
|passport number  <br/> 슬로바키아어 여권 번호  <br/> passport 아니요  <br/> číslo (u)  <br/> |
   
## <a name="slovenia"></a>슬로베니아

### <a name="format"></a>형식일

공백 또는 구분 기호가 없는 7 자리, 두 문자
  
### <a name="pattern"></a>패턴

2 개 문자와 7 자리 숫자를 입력 합니다.
  
- "P" 문자
    
- 대문자 1 개
    
- 7자리 숫자
    
### <a name="checksum"></a>제외

아니요
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 정규식이 해당 `Regex_slovenia_eu_passport_number` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- from `Keywords_slovenia_eu_passport_number` 키워드를 찾았습니다. 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_slovenia_eu_passport_number" />
          <Match idRef="Keywords_slovenia_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>키워드

| |
|**Keywords_slovenia_eu_passport_number**|
|:-----|
|passport number  <br/> 슬로베니아어 여권 번호  <br/> passport 아니요  <br/> številka potnega lista  <br/> |
   
## <a name="spain"></a>스페인

### <a name="format"></a>형식일

공백이 나 구분 기호가 없는 문자 및 숫자의 8 자리 또는 9 자 조합
  
### <a name="pattern"></a>패턴

문자와 숫자의 8 자리 또는 9 자리 조합:
  
-  두 자리 숫자 또는 문자 
    
- 1 자리 숫자 또는 문자 (선택 사항)
    
- 6자리 숫자
    
### <a name="checksum"></a>제외

해당 없음
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 정규식이 해당 `Regex_spain_eu_passport_number` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- from `Keywords_spain_eu_passport_number` 키워드를 찾았습니다. 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_spain_eu_passport_number" />
          <Match idRef="Keywords_spain_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>키워드

| |
|**Keywords_spain_eu_passport_number**|
|:-----|
|여권  <br/> 스페인 여권  <br/> passport 책  <br/> passport number  <br/> passport 아니요  <br/> pasaporte  <br/> número pasaporte  <br/> españa pasaporte  <br/> pasaporte  <br/> |
   
## <a name="sweden"></a>스웨덴

자세한 내용은 [중요 한 정보 유형이 찾는](what-the-sensitive-information-types-look-for.md)"스웨덴 여권 번호" 섹션을 참조 하십시오.
  
## <a name="uk"></a>영국의

자세한 내용은 "미국/영국" 섹션을 참조 하십시오. [중요 한 정보 유형이 찾는](what-the-sensitive-information-types-look-for.md)Passport 번호입니다.
  
## <a name="see-also"></a>참고 항목

[중요한 정보 형식이 찾는 항목](what-the-sensitive-information-types-look-for.md)

