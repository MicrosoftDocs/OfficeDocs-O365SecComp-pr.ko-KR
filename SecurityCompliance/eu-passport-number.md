---
title: EU 여권 번호
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 8/16/2018
ms.audience: Admin
ms.topic: reference
ms.service: o365-administration
localization_priority: Normal
ms.assetid: 8c00df57-9fb3-459c-ba87-40480c87bd55
description: 이 항목에서는 EU 여권 번호 중요 한 정보 유형을 감지 하는 경우의 데이터 손실 방지 (DLP) 정책을 찾아에 대해 보여줍니다. 이 중요 한 정보 유형 다양 한 패턴, 키워드 및 각 국가 대 한 기타 증거를 정의합니다.
ms.openlocfilehash: 7a7fc1ff826aab4096c46535686eb0fd68173c6f
ms.sourcegitcommit: 7e2a0185cadea7f3a6afc5ddc445eac2e1ce22eb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/11/2019
ms.locfileid: "25840327"
---
# <a name="eu-passport-number"></a>EU 여권 번호

이 항목에서는 EU 여권 번호 중요 한 정보 유형을 감지 하는 경우의 데이터 손실 방지 (DLP) 정책을 찾아에 대해 보여줍니다. 이 중요 한 정보 유형 다양 한 패턴, 키워드 및 각 국가 대 한 기타 증거를 정의합니다.
  
## <a name="austria"></a>오스트리아

### <a name="format"></a>형식

선택 하는 공간 및 7 자리 숫자 앞에 오는 문자 하나
  
### <a name="pattern"></a>패턴

하나의 문자, 7 자리 숫자 및 하나의 공간 조합:
  
- 1개 문자(대/소문자 구분 안 함)
    
- 하나의 공간 (선택 사항)
    
- 7자리 숫자
    
### <a name="checksum"></a>체크섬

해당 없음
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 정규식 `Regex_austria_eu_passport_number` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- 키워드에서 `Keywords_austria_eu_passport_number` 를 찾을 수 있습니다. 
    
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
|여권 번호  <br/> 오스트리아 여권 번호  <br/> passport 없음  <br/> reisepass  <br/> österreichisch reisepass  <br/> |
   
## <a name="belgium"></a>벨기에

### <a name="format"></a>형식

공백이 나 구분 기호 없이 6 자리 숫자 앞에 오는 두 문자
  
### <a name="pattern"></a>패턴

처음 두 6 자리 숫자 앞에 오는 하 고
  
### <a name="checksum"></a>체크섬

해당 없음
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 정규식 `Regex_belgium_eu_passport_number` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- 키워드에서 `Keywords_belgium_eu_passport_number` 를 찾을 수 있습니다. 
    
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
|여권 번호  <br/> 벨기에 여권 번호  <br/> passport 없음  <br/> paspoort  <br/> paspoortnummer  <br/> reisepass kein  <br/> reisepass  <br/> |
   
## <a name="bulgaria"></a>불가리아

### <a name="format"></a>형식

공백 및 구분 기호 없이 숫자 9 개
  
### <a name="pattern"></a>패턴

 9자리 숫자 
  
### <a name="checksum"></a>체크섬

없음
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 정규식 `Regex_bulgaria_eu_passport_number` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- 키워드에서 `Keywords_bulgaria_eu_passport_number` 를 찾을 수 있습니다. 
    
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
|여권 번호  <br/> 불가리아어 여권 번호  <br/> passport 없음  <br/> НОМЕР НА ПАСПОРТА  <br/> |
   
## <a name="croatia"></a>크로아티아

### <a name="format"></a>형식

공백 및 구분 기호 없이 숫자 9 개
  
### <a name="pattern"></a>패턴

 9자리 숫자 
  
### <a name="checksum"></a>체크섬

없음
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 정규식 `Regex_croatia_eu_passport_number` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- 키워드에서 `Keywords_croatia_eu_passport_number` 를 찾을 수 있습니다. 
    
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
|여권 번호  <br/> 크로아티아어 여권 번호  <br/> passport 없음  <br/> broj putovnice  <br/> |
   
## <a name="cyprus"></a>키프로스

### <a name="format"></a>형식

공백이 나 구분 기호 없이 6-8 숫자 앞에 오는 문자 하나
  
### <a name="pattern"></a>패턴

6 ~ 8 개의 숫자 앞에 오는 문자 하나
  
### <a name="checksum"></a>체크섬

없음
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 정규식 `Regex_cyprus_eu_passport_number` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- 키워드에서 `Keywords_cyprus_eu_passport_number` 를 찾을 수 있습니다. 
    
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
|여권 번호  <br/> 키프로스 여권 번호  <br/> passport 없음  <br/> ΑΡΙΘΜΌ ΔΙΑΒΑΤΗΡΊΟΥ  <br/> |
   
## <a name="czech-republic"></a>체코 공화국

### <a name="format"></a>형식

공백이 나 구분 기호 없이 8 개의 숫자
  
### <a name="pattern"></a>패턴

공백이 나 구분 기호 없이 8 개의 숫자
  
### <a name="checksum"></a>체크섬

없음
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 정규식 `Regex_czech_republic_eu_passport_number` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- 키워드에서 `Keywords_czech_republic_eu_passport_number` 를 찾을 수 있습니다. 
    
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
|여권 번호  <br/> 체코어 여권 번호  <br/> passport 없음  <br/> cestovní pas  <br/> pas  <br/> |
   
## <a name="denmark"></a>덴마크

### <a name="format"></a>형식

공백 및 구분 기호 없이 숫자 9 개
  
### <a name="pattern"></a>패턴

 9자리 숫자 
  
### <a name="checksum"></a>체크섬

없음
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 정규식 `Regex_denmark_eu_passport_number` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- 키워드에서 `Keywords_denmark_eu_passport_number` 를 찾을 수 있습니다. 
    
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
|여권 번호  <br/> 덴마크어 여권 번호  <br/> passport 없음  <br/> pas  <br/> pasnummer  <br/> |
   
## <a name="estonia"></a>에스토니아

### <a name="format"></a>형식

공백이 나 구분 기호 없이 7 자리 숫자 앞에 오는 문자 하나
  
### <a name="pattern"></a>패턴

7 자리 숫자 앞에 오는 문자 하나
  
### <a name="checksum"></a>체크섬

없음
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 정규식 `Regex_estonia_eu_passport_number` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- 키워드에서 `Keywords_estonia_eu_passport_number` 를 찾을 수 있습니다. 
    
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
|여권 번호  <br/> 에스토니아어 여권 번호  <br/> passport 없음  <br/> eesti kodaniku 통과  <br/> |
   
## <a name="finland"></a>핀란드

자세한 내용은의 섹션을 참조 "핀란드 여권 번호" [에 대 한 중요 한 정보 유형을 확인](what-the-sensitive-information-types-look-for.md)합니다.
  
## <a name="france"></a>프랑스

자세한 내용은의 섹션을 참조 "프랑스 여권 번호" [에 대 한 중요 한 정보 유형을 확인](what-the-sensitive-information-types-look-for.md)합니다.
  
## <a name="germany"></a>독일

자세한 내용은의 섹션을 참조 "독일 여권 번호" [에 대 한 중요 한 정보 유형을 확인](what-the-sensitive-information-types-look-for.md)합니다.
  
## <a name="greece"></a>그리스

### <a name="format"></a>형식

공백이 나 구분 기호 없이 7 자리 숫자 앞에 오는 두 문자
  
### <a name="pattern"></a>패턴

2개 문자와 7자리 숫자
  
### <a name="checksum"></a>체크섬

없음
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 정규식 `Regex_greece_eu_passport_number` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- 키워드에서 `Keywords_greece_eu_passport_number` 를 찾을 수 있습니다. 
    
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
|여권 번호  <br/> 그리스어 여권 번호  <br/> passport 없음  <br/> ΔΙΑΒΑΤΗΡΙΟ  <br/> |
   
## <a name="hungary"></a>헝가리

### <a name="format"></a>형식

공백이 나 구분 기호 없이 6 또는 7 자리 숫자 앞에 오는 두 문자
  
### <a name="pattern"></a>패턴

6 또는 7 자리 숫자 앞에 오는 두 문자
  
### <a name="checksum"></a>체크섬

없음
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 정규식 `Regex_hungary_eu_passport_number` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- 키워드에서 `Keywords_hungary_eu_passport_number` 를 찾을 수 있습니다. 
    
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
|여권 번호  <br/> 헝가리어 여권 번호  <br/> passport 없음  <br/> útlevél száma  <br/> |
   
## <a name="ireland"></a>Ireland

### <a name="format"></a>형식

두 문자나 공백이 나 구분 기호 없이 7 자리 숫자 앞에 오는 숫자
  
### <a name="pattern"></a>패턴

두 문자 또는 7 자리 숫자 앞에 오는 숫자:
  
- 2자리 숫자 또는 문자(대/소문자 구분 안 함)
    
- 7자리 숫자
    
### <a name="checksum"></a>체크섬

없음
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 정규식 `Regex_ireland_eu_passport_number` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- 키워드에서 `Keywords_ireland_eu_passport_number` 를 찾을 수 있습니다. 
    
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
|여권 번호  <br/> 아일랜드 여권 번호  <br/> passport 없음  <br/> pas  <br/> passport  <br/> passeport  <br/> passeport numero  <br/> |
   
## <a name="italy"></a>이탈리아

### <a name="format"></a>형식

두 문자나 공백이 나 구분 기호 없이 7 자리 숫자 앞에 오는 숫자
  
### <a name="pattern"></a>패턴

두 문자 또는 7 자리 숫자 앞에 오는 숫자:
  
- 2자리 숫자 또는 문자(대/소문자 구분 안 함)
    
- 7자리 숫자
    
### <a name="checksum"></a>체크섬

해당 없음
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 정규식 `Regex_italy_eu_passport_number` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- 키워드에서 `Keywords_italy_eu_passport_number` 를 찾을 수 있습니다. 
    
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
|이탈리아어 여권 번호  <br/> repubblica italiana passaporto  <br/> passaporto  <br/> passaporto italiana  <br/> 여권 번호  <br/> italiana passaporto numero  <br/> passaporto numero  <br/> numéro passeport italien  <br/> numéro passeport  <br/> |
   
## <a name="latvia"></a>라트비아

### <a name="format"></a>형식

두 문자나 공백이 나 구분 기호 없이 7 자리 숫자 앞에 오는 숫자
  
### <a name="pattern"></a>패턴

두 문자 또는 7 자리 숫자 앞에 오는 숫자:
  
- 2자리 숫자 또는 문자(대/소문자 구분 안 함)
    
- 7자리 숫자
    
### <a name="checksum"></a>체크섬

없음
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 정규식 `Regex_latvia_eu_passport_number` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- 키워드에서 `Keywords_latvia_eu_passport_number` 를 찾을 수 있습니다. 
    
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
|여권 번호  <br/> 라트비아어 여권 번호  <br/> passport 없음  <br/> pase numurs  <br/> |
   
## <a name="lithuania"></a>리투아니아

### <a name="format"></a>형식

8 개의 숫자 또는 공백이 나 구분 기호 없이 문자
  
### <a name="pattern"></a>패턴

8 개의 숫자 또는 문자 (하지 대/소문자 구분)
  
### <a name="checksum"></a>체크섬

해당 없음
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 정규식 `Regex_lithuania_eu_passport_number` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- 키워드에서 `Keywords_lithuania_eu_passport_number` 를 찾을 수 있습니다. 
    
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
|여권 번호  <br/> lithunian 여권 번호  <br/> passport 없음  <br/> paso numeris  <br/> |
   
## <a name="luxemburg"></a>룩셈부르크

### <a name="format"></a>형식

8 개의 숫자 또는 공백이 나 구분 기호 없이 문자
  
### <a name="pattern"></a>패턴

8 개의 숫자 또는 문자 (하지 대/소문자 구분)
  
### <a name="checksum"></a>체크섬

없음
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 정규식 `Regex_nation_eu_passport_number` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- 키워드에서 `Keywords_nation_eu_passport_number` 를 찾을 수 있습니다. 
    
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
|여권 번호  <br/> 라트비아어 여권 번호  <br/> passport 없음  <br/> passnummer  <br/> |
   
## <a name="malta"></a>몰타

### <a name="format"></a>형식

공백이 나 구분 하지 않고 7 자리 숫자
  
### <a name="pattern"></a>패턴

 7자리 숫자 
  
### <a name="checksum"></a>체크섬

없음
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 정규식 `Regex_malta_eu_passport_number` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- 키워드에서 `Keywords_malta_eu_passport_number` 를 찾을 수 있습니다. 
    
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
|여권 번호  <br/> 몰타어 여권 번호  <br/> passport 없음  <br/> numru tal passaport  <br/> |
   
## <a name="netherlands"></a>네덜란드

### <a name="format"></a>형식

9 개의 문자나 공백이 나 구분 기호 없이 숫자
  
### <a name="pattern"></a>패턴

9 개의 문자 또는 숫자
  
### <a name="checksum"></a>체크섬

해당 없음
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 정규식 `Regex_netherlands_eu_passport_number` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- 키워드에서 `Keywords_netherlands_eu_passport_number` 를 찾을 수 있습니다. 
    
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
|네덜란드어 여권 번호  <br/> 여권 번호  <br/> 네덜란드 여권 번호  <br/> nederlanden paspoort nummer  <br/> paspoort  <br/> nederlanden paspoortnummer  <br/> paspoortnummer  <br/> |
   
## <a name="poland"></a>폴란드

자세한 내용은의 섹션을 참조 "폴란드 여권 번호" [에 대 한 중요 한 정보 유형을 확인](what-the-sensitive-information-types-look-for.md)합니다.
  
## <a name="portugal"></a>포르투갈

### <a name="format"></a>형식

공백이 나 구분 기호 없이 6 자리 숫자 앞에 오는 문자 하나
  
### <a name="pattern"></a>패턴

6 자리 숫자 앞에 오는 문자 하나:
  
- 1개 문자(대/소문자 구분 안 함)
    
- 6자리 숫자
    
### <a name="checksum"></a>체크섬

없음
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 정규식 `Regex_portugal_eu_passport_number` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- 키워드에서 `Keywords_portugal_eu_passport_number` 를 찾을 수 있습니다. 
    
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
|여권 번호  <br/> 포르투갈어 여권 번호  <br/> passport 없음  <br/> número do passaporte  <br/> |
   
## <a name="romania"></a>루마니아

### <a name="format"></a>형식

공백 및 구분 기호 없이 8 또는 9 자리 숫자
  
### <a name="pattern"></a>패턴

8 또는 9 자리 숫자
  
### <a name="checksum"></a>체크섬

없음
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 정규식 `Regex_romania_eu_passport_number` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- 키워드에서 `Keywords_romania_eu_passport_number` 를 찾을 수 있습니다. 
    
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
|여권 번호  <br/> 루마니아어 여권 번호  <br/> passport 없음  <br/> numărul pașaportului  <br/> |
   
## <a name="slovakia"></a>슬로바키아

### <a name="format"></a>형식

한 자리 숫자 또는 공백이 나 구분 기호 없이 7 자리 숫자 앞에 오는 문자
  
### <a name="pattern"></a>패턴

한 자리 또는 7 자리 숫자 앞에 오는 문자 (하지 대/소문자 구분)
  
### <a name="checksum"></a>체크섬

없음
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 정규식 `Regex_slovakia_eu_passport_number` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- 키워드에서 `Keywords_slovakia_eu_passport_number` 를 찾을 수 있습니다. 
    
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
|여권 번호  <br/> 슬로바키아어 여권 번호  <br/> passport 없음  <br/> Číslo pasu  <br/> |
   
## <a name="slovenia"></a>슬로베니아

### <a name="format"></a>형식

공백이 나 구분 기호 없이 7 자리 숫자 앞에 오는 두 문자
  
### <a name="pattern"></a>패턴

7 자리 숫자 앞에 오는 두 문자 수:
  
- 문자 "P"
    
- 하나의 대문자
    
- 7자리 숫자
    
### <a name="checksum"></a>체크섬

없음
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 정규식 `Regex_slovenia_eu_passport_number` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- 키워드에서 `Keywords_slovenia_eu_passport_number` 를 찾을 수 있습니다. 
    
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
|여권 번호  <br/> 슬로베니아어 여권 번호  <br/> passport 없음  <br/> Številka potnega lista  <br/> |
   
## <a name="spain"></a>스페인

### <a name="format"></a>형식

문자와 공백이 나 구분 기호 없이 숫자는 8 또는 9 개 문자 조합
  
### <a name="pattern"></a>패턴

문자와 숫자는 8 또는 9 개 문자 조합 합니다.
  
-  두 자리 숫자 또는 문자 
    
- 한 자리 숫자 또는 문자 (선택 사항)
    
- 6자리 숫자
    
### <a name="checksum"></a>체크섬

해당 없음
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 정규식 `Regex_spain_eu_passport_number` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- 키워드에서 `Keywords_spain_eu_passport_number` 를 찾을 수 있습니다. 
    
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
|passport  <br/> 스페인 passport  <br/> passport도 서  <br/> 여권 번호  <br/> passport 없음  <br/> libreta pasaporte  <br/> número pasaporte  <br/> españa pasaporte  <br/> pasaporte  <br/> |
   
## <a name="sweden"></a>스웨덴

자세한 내용은의 섹션을 참조 "스웨덴 여권 번호" [에 대 한 중요 한 정보 유형을 확인](what-the-sensitive-information-types-look-for.md)합니다.
  
## <a name="uk"></a>영국

자세한 내용은의 섹션을 참조 "미국/영국 여권 번호" [에 대 한 중요 한 정보 유형을 확인](what-the-sensitive-information-types-look-for.md)합니다.
  
## <a name="see-also"></a>참고 항목

[중요한 정보 형식이 찾는 항목](what-the-sensitive-information-types-look-for.md)

