---
title: EU 운전 면허 번호
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 8/17/2018
ms.audience: Admin
ms.topic: reference
ms.service: O365-seccomp
ms.collection: M365-security-compliance
localization_priority: Normal
description: 이 항목에서는 DLP (데이터 손실 방지) 정책이 EU 드라이버의 라이선스 번호 중요 정보 유형을 검색할 때 찾는 항목을 보여 줍니다. 이 중요 한 정보 유형은 각 국가에 대 한 다양 한 패턴, 키워드 및 기타 증거를 정의 합니다.
ms.openlocfilehash: be9497c325866a670dff8d82b5170f4ca947c4ad
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32255776"
---
# <a name="eu-drivers-license-number"></a>EU 운전 면허 번호

이 항목에서는 DLP (데이터 손실 방지) 정책이 EU 드라이버의 라이선스 번호 중요 정보 유형을 검색할 때 찾는 항목을 보여 줍니다. 이 중요 한 정보 유형은 각 국가에 대 한 다양 한 패턴, 키워드 및 기타 증거를 정의 합니다.
  
## <a name="austria"></a>오스트리아

### <a name="format"></a>형식일

공백과 구분 기호가 없는 8 자리 숫자
  
### <a name="pattern"></a>패턴

8자리 숫자
  
### <a name="checksum"></a>제외

아니요
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 정규식이 해당 `Regex_austria_eu_driver's_license_number` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- from `Keywords_austria_eu_driver's_license_number` 키워드를 찾았습니다. 
    
```
<!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_austria_eu_driver's_license_number" />
          <Match idRef="Keywords_austria_eu_driver's_license_number" />
        </Pattern>
    </Entity>

```

### <a name="keywords"></a>키워드

| |
|**Keywords_austria_eu_driver's_license_number**|
|:-----|
|dl  <br/> driver license  <br/> 드라이버 라이선스 번호  <br/> 드라이버 라이선스  <br/> drivers lic  <br/> drivers license  <br/> driver's licence  <br/> driver's license  <br/> 운전 면허 번호  <br/> 운전 라이선스 번호  <br/>  운전 면허 번호  <br/> dlno #  <br/> fuhrerschein  <br/> fuhrerschein republik osterreich  <br/> |
   
## <a name="belgium"></a>벨기에

### <a name="format"></a>형식일

공백과 구분 기호가 없는 10 자리 숫자
  
### <a name="pattern"></a>패턴

10자리 숫자
  
### <a name="checksum"></a>제외

아니요
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 정규식이 해당 `Regex_belgium_eu_driver's_license_number` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- from `Keywords_belgium_eu_driver's_license_number` 키워드를 찾았습니다. 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_belgium_eu_driver's_license_number" />
          <Match idRef="Keywords_belgium_eu_driver's_license_number" />
        </Pattern>
</Entity>

```

### <a name="keywords"></a>키워드

| |
|**Keywords__belgium_eu_driver's_license_number**|
|:-----|
|dl  <br/> driver license  <br/> 드라이버 라이선스 번호  <br/> 드라이버 라이선스  <br/> drivers lic  <br/> drivers license  <br/> drivers licence  <br/> driver's license  <br/> 운전 면허 번호  <br/> 운전 라이선스 번호  <br/> dlno #  <br/> rijbewijs  <br/> rijbewijsnummer  <br/> führerscheinnummer  <br/> fuhrerscheinnummer  <br/> fuehrerscheinnummer  <br/> führerschein-veiligheid  <br/> fuehrerschein-veiligheid  <br/> fuehrerschein-veiligheid  <br/> |
   
## <a name="bulgaria"></a>불가리아

### <a name="format"></a>형식일

공백과 구분 기호를 사용 하지 않고 9 자리 숫자
  
### <a name="pattern"></a>패턴

9자리 숫자
  
### <a name="checksum"></a>제외

아니요
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 정규식이 해당 `Regex_bulgaria_eu_driver's_license_number` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- from `Keywords_bulgaria_eu_driver's_license_number` 키워드를 찾았습니다. 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
             <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_bulgaria_eu_driver's_license_number" />
          <Match idRef="Keywords_bulgaria_eu_driver's_license_number" />
        </Pattern> 
</Entity>    

```

### <a name="keywords"></a>키워드

| |
|**Keywords_bulgaria_eu_driver's_license_number**|
|:-----|
|dl  <br/> driver license  <br/> 드라이버 라이선스 번호  <br/> 드라이버 라이선스  <br/> drivers lic  <br/> drivers license  <br/> drivers licence  <br/> driver's license  <br/> 운전 면허 번호  <br/> 운전 라이선스 번호  <br/> 운전 면허 번호  <br/> dlno #  <br/> свидетелство за управление на мпс  <br/> свидетелство за управление на моторно превозно средство  <br/> сумпс  <br/> шофьорска книжка  <br/> |
   
## <a name="croatia"></a>크로아티아

### <a name="format"></a>형식일

공백과 구분 기호가 없는 8 자리 숫자
  
### <a name="pattern"></a>패턴

8자리 숫자
  
### <a name="checksum"></a>제외

아니요
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 정규식이 해당 `Regex_croatia_eu_driver's_license_number` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- from `Keywords_croatia_eu_driver's_license_number` 키워드를 찾았습니다. 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_croatia_eu_driver's_license_number" />
          <Match idRef="Keywords_croatia_eu_driver's_license_number" />
        </Pattern>
</Entity>

```

### <a name="keywords"></a>키워드

| |
|**Keywords_croatia_eu_driver's_license_number**|
|:-----|
|dl  <br/> driver license  <br/> 드라이버 라이선스 번호  <br/> 드라이버 라이선스  <br/> drivers lic  <br/> drivers license  <br/> drivers licence  <br/> driver's license  <br/> 운전 면허 번호  <br/> 운전 라이선스 번호  <br/> 운전 면허 번호  <br/> dlno #  <br/> vozačka dozvola  <br/> |
   
## <a name="cyprus"></a>키프로스

### <a name="format"></a>형식일

공백과 구분 기호를 사용 하지 않고 12 자리 숫자
  
### <a name="pattern"></a>패턴

12자리 숫자
  
### <a name="checksum"></a>제외

아니요
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 정규식이 해당 `Regex_cyprus_eu_driver's_license_number` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- from `Keywords_cyprus_eu_driver's_license_number` 키워드를 찾았습니다. 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_cyprus_eu_driver's_license_number" />
          <Match idRef="Keywords_cyprus_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>키워드

| |
|**Keywords_cyprus_eu_driver's_license_number**|
|:-----|
|dl  <br/> driver license  <br/> 드라이버 라이선스 번호  <br/> 드라이버 라이선스  <br/> drivers lic  <br/> drivers license  <br/> drivers licence  <br/> 운전 면허 번호  <br/> 운전 라이선스 번호  <br/> 운전 면허 번호  <br/> dlno #  <br/> άδεια οδήγησης  <br/> |
   
## <a name="czech-republic"></a>체코 공화국

### <a name="format"></a>형식일

2 개의 문자 다음에 6 자리 숫자
  
### <a name="pattern"></a>패턴

8 개의 문자 및 숫자:
  
- 2 개 문자 (대/소문자 구분 안 함)
    
- 공백 1개(선택 사항)
    
- 6자리 숫자
    
### <a name="checksum"></a>제외

아니요
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 정규식이 해당 `Regex_czech_republic_eu_driver's_license_number` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- from `Keywords_czech_republic_eu_driver's_license_number` 키워드를 찾았습니다. 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_czech_republic_eu_driver's_license_number" />
          <Match idRef="Keywords_czech_republic_eu_driver's_license_number" />
        </Pattern>
</Entity>

```

### <a name="keywords"></a>키워드

| |
|**Keywords_czech_republic_eu_driver's_license_number**|
|:-----|
|dl  <br/> driver license  <br/> 드라이버 라이선스 번호  <br/> 드라이버 라이선스  <br/> drivers lic  <br/> drivers license  <br/> drivers licence  <br/> driver's license  <br/> 운전 면허 번호  <br/> 운전 면허 번호  <br/> 운전 라이선스 번호  <br/> 운전 면허 번호  <br/> dlno #  <br/> řidičský prúkaz  <br/> |
   
## <a name="denmark"></a>덴마크

### <a name="format"></a>형식일

공백과 구분 기호가 없는 8 자리 숫자
  
### <a name="pattern"></a>패턴

8자리 숫자
  
### <a name="checksum"></a>제외

예
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 정규식이 해당 `Regex_denmark_eu_driver's_license_number` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- from `Keywords_denmark_eu_driver's_license_number` 키워드를 찾았습니다. 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_denmark_eu_driver's_license_number" />
          <Match idRef="Keywords_denmark_eu_driver's_license_number" />
        </Pattern>
</Entity>

```

### <a name="keywords"></a>키워드

| |
|**Keywords_denmark_eu_driver's_license_number**|
|:-----|
|dl  <br/> driver license  <br/> 드라이버 라이선스 번호  <br/> 드라이버 라이선스  <br/> drivers lic  <br/> drivers license  <br/> drivers licence  <br/> driver's license  <br/> 운전 면허 번호  <br/> 운전 라이선스 번호  <br/> 운전 면허 번호  <br/> dlno #  <br/> kørekort  <br/> kørekortnummer  <br/> |
   
## <a name="estonia"></a>에스토니아

### <a name="format"></a>형식일

2 개의 문자 다음에 6 자리 숫자
  
### <a name="pattern"></a>패턴

2 개의 문자와 6 자리 숫자:
  
-  문자 "ET" (대/소문자 구분 안 함) 
    
- 6자리 숫자
    
### <a name="checksum"></a>제외

아니요
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 정규식이 해당 `Regex_estonia_eu_driver's_license_number` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- from `Keywords_estonia_eu_driver's_license_number` 키워드를 찾았습니다. 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_estonia_eu_driver's_license_number" />
          <Match idRef="Keywords_estonia_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>키워드

| |
|**Keywords_estonia_eu_driver's_license_number**|
|:-----|
|dl  <br/> driver license  <br/> 드라이버 라이선스 번호  <br/> 드라이버 라이선스 번호  <br/> 드라이버 라이선스  <br/> drivers lic  <br/> drivers license  <br/> drivers licence  <br/> driver's license  <br/> 운전 면허 번호  <br/> 운전 면허 번호  <br/> dlno #  <br/> permis de conduire  <br/> |
   
## <a name="finland"></a>핀란드

### <a name="format"></a>형식일

하이픈을 포함하는 10자리 숫자
  
### <a name="pattern"></a>패턴

하이픈을 포함 하는 10 자리 숫자:
  
-  6자리 숫자 
    
- 하이픈
    
-  4자리 숫자 
    
### <a name="checksum"></a>제외

아니요
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 정규식이 해당 `Regex_finland_eu_driver's_license_number` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- from `Keywords_finland_eu_driver's_license_number` 키워드를 찾았습니다. 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_finland_eu_driver's_license_number" />
          <Match idRef="Keywords_finland_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>키워드

| |
|**Keywords_finland_eu_driver's_license_number**|
|:-----|
|dl  <br/> driver license  <br/> 드라이버 라이선스 번호  <br/> 드라이버 라이선스  <br/> drivers lic  <br/> drivers license  <br/> drivers licence  <br/> driver's license  <br/> 운전 면허 번호  <br/> 운전 라이선스 번호  <br/> 운전 면허 번호  <br/> dlno #  <br/> ajokortti  <br/> |
   
## <a name="france"></a>프랑스

자세한 내용은 [중요 한 정보 유형이 찾는](what-the-sensitive-information-types-look-for.md)"경기도 운전 면허 번호" 섹션을 참조 하십시오.
  
## <a name="germany"></a>독일

자세한 내용은 [중요 한 정보 유형이 찾는](what-the-sensitive-information-types-look-for.md)"독일어 운전 면허 번호" 섹션을 참조 하십시오.
  
## <a name="greece"></a>그리스

### <a name="format"></a>형식일

공백과 구분 기호를 사용 하지 않고 9 자리 숫자
  
### <a name="pattern"></a>패턴

 9자리 숫자 
  
### <a name="checksum"></a>제외

아니요
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 정규식이 해당 `Regex_greece_eu_driver's_license_number` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- from `Keywords_greece_eu_driver's_license_number` 키워드를 찾았습니다. 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_greece_eu_driver's_license_number" />
          <Match idRef="Keywords_greece_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>키워드

| |
|**Keywords_greece_eu_driver's_license_number**|
|:-----|
|dlL  <br/> driver license  <br/> 드라이버 라이선스 번호  <br/> 드라이버 라이선스  <br/> drivers lic  <br/> drivers license  <br/> drivers licence  <br/> driver's license  <br/> 운전 면허 번호  <br/> 운전 라이선스 번호  <br/> 운전 면허 번호  <br/> dlno #  <br/> δεια οδήγησης  <br/> Adeia odigisis  <br/> |
   
## <a name="hungary"></a>헝가리

### <a name="format"></a>형식일

2 개의 문자 다음에 6 자리 숫자
  
### <a name="pattern"></a>패턴

2 개의 문자와 6 자리 숫자:
  
-  2 개 문자 (대/소문자 구분 안 함) 
    
- 6자리 숫자
    
### <a name="checksum"></a>제외

아니요
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 정규식이 해당 `Regex_hungary_eu_driver's_license_number` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- from `Keywords_hungary_eu_driver's_license_number` 키워드를 찾았습니다. 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_hungary_eu_driver's_license_number" />
          <Match idRef="Keywords_hungary_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>키워드

| |
|**Keywords_hungary_eu_driver's_license_number**|
|:-----|
|dl  <br/> driver license  <br/> 드라이버 라이선스 번호  <br/> 드라이버 라이선스  <br/> drivers lic  <br/> drivers license  <br/> drivers licence  <br/> driver's license  <br/> 운전 면허 번호  <br/> 운전 라이선스 번호  <br/> 운전 면허 번호  <br/> dlno #  <br/> vezetoi  <br/> |
   
## <a name="ireland"></a>Ireland

### <a name="format"></a>형식일

6 자리 숫자와 4 개 문자
  
### <a name="pattern"></a>패턴

6 자리 숫자와 4 개 문자:
  
- 6자리 숫자
    
- 4 개 문자 (대/소문자 구분 안 함)
    
### <a name="checksum"></a>제외

아니요
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 정규식이 해당 `Regex_ireland_eu_driver's_license_number` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- from `Keywords_ireland_eu_driver's_license_number` 키워드를 찾았습니다. 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_ireland_eu_driver's_license_number" />
          <Match idRef="Keywords_ireland_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>키워드

| |
|**Keywords_ireland_eu_driver's_license_number**|
|:-----|
|dl  <br/> driver license  <br/> 드라이버 라이선스 번호  <br/> 드라이버 라이선스  <br/> drivers lic  <br/> drivers license  <br/> drivers licence  <br/> driver's license  <br/> 운전 면허 번호  <br/> 운전 라이선스 번호  <br/> 운전 면허 번호  <br/> dlno #  <br/> ceadúnas tiomána  <br/> |
   
## <a name="italy"></a>이탈리아

자세한 내용은 [중요 한 정보 유형이 찾는](what-the-sensitive-information-types-look-for.md)"이탈리아 운전 면허 번호" 섹션을 참조 하십시오.
  
## <a name="latvia"></a>라트비아

### <a name="format"></a>형식일

3 개의 문자 및 6 자리 숫자
  
### <a name="pattern"></a>패턴

3 개의 문자 및 6 자리 숫자:
  
-  3 개 문자 (대/소문자 구분 안 함) 
    
- 6자리 숫자
    
### <a name="checksum"></a>제외

아니요
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 정규식이 해당 `Regex_latvia_eu_driver's_license_number` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- from `Keywords_latvia_eu_driver's_license_number` 키워드를 찾았습니다. 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_latvia_eu_driver's_license_number" />
          <Match idRef="Keywords_latvia_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>키워드

| |
|**Keywords_latvia_eu_driver's_license_number**|
|:-----|
|dl  <br/> driver license  <br/> 드라이버 라이선스 번호  <br/> 드라이버 라이선스  <br/> drivers lic  <br/> drivers license  <br/> drivers licence  <br/> driver's license  <br/> 운전 면허 번호  <br/> 운전 라이선스 번호  <br/> 운전 면허 번호  <br/> dlno #  <br/> autovadītāja apliecība  <br/> |
   
## <a name="lithuania"></a>리투아니아

### <a name="format"></a>형식일

공백과 구분 기호가 없는 8 자리 숫자
  
### <a name="pattern"></a>패턴

 8자리 숫자 
  
### <a name="checksum"></a>제외

아니요
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 정규식이 해당 `Regex_lithuania_eu_driver's_license_number` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- from `Keywords_lithuania_eu_driver's_license_number` 키워드를 찾았습니다. 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_lithuania_eu_driver's_license_number" />
          <Match idRef="Keywords_lithuania_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>키워드

| |
|**Keywords_lithuania_eu_driver's_license_number**|
|:-----|
|dl  <br/> driver license  <br/> 드라이버 라이선스 번호  <br/> 드라이버 라이선스  <br/> drivers lic  <br/> drivers license  <br/> drivers licence  <br/> driver's license  <br/> 운전 면허 번호  <br/> 운전 라이선스 번호  <br/> 운전 면허 번호  <br/> dlno #  <br/> vairuotojo pažymėjimas  <br/> |
   
## <a name="luxemburg"></a>셈

### <a name="format"></a>형식일

공백과 구분 기호가 없는 6 자리 숫자
  
### <a name="pattern"></a>패턴

 6자리 숫자 
  
### <a name="checksum"></a>제외

아니요
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 정규식이 해당 `Regex_luxemburg_eu_driver's_license_number` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- from `Keywords_luxemburg_eu_driver's_license_number` 키워드를 찾았습니다. 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_luxemburg_eu_driver's_license_number" />
          <Match idRef="Keywords_luxemburg_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>키워드

| |
|**Keywords_luxemburg_eu_driver's_license_number**|
|:-----|
|dl  <br/> driver license  <br/> 드라이버 라이선스 번호  <br/> 드라이버 라이선스  <br/> drivers lic  <br/> drivers license  <br/> drivers licence  <br/> driver's license  <br/> 운전 면허 번호  <br/> 운전 라이선스 번호  <br/> 운전 면허 번호  <br/> dlno #  <br/> fahrerlaubnis  <br/> |
   
## <a name="malta"></a>몰타

### <a name="format"></a>형식일

지정 된 패턴에서 두 개의 문자와 6 자리 숫자 조합
  
### <a name="pattern"></a>패턴

두 문자와 6 자리 숫자의 조합:
  
- 2 개 문자 (대/소문자 구분 안 함)
    
- 공백 1개(선택 사항)
    
- 3자리 숫자
    
- 공백 1개(선택 사항)
    
- 3자리 숫자
    
### <a name="checksum"></a>제외

아니요
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 정규식이 해당 `Regex_malta_eu_driver's_license_number` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- from `Keywords_malta_eu_driver's_license_number` 키워드를 찾았습니다. 
    
```
<!-- EU Driver's License Number -->
 <Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_malta_eu_driver's_license_number" />
          <Match idRef="Keywords_malta_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>키워드

| |
|**Keywords_malta_eu_driver's_license_number**|
|:-----|
|dl  <br/> driver license  <br/> 드라이버 라이선스 번호  <br/> 드라이버 라이선스  <br/> drivers lic  <br/> drivers license  <br/> drivers licence  <br/> driver's license  <br/> 운전 면허 번호  <br/> 운전 라이선스 번호  <br/> 운전 면허 번호  <br/> dlno #  <br/> liċenzja tas-sewqan  <br/> |
   
## <a name="netherlands"></a>네덜란드

### <a name="format"></a>형식일

공백과 구분 기호가 없는 10 자리 숫자
  
### <a name="pattern"></a>패턴

10자리 숫자
  
### <a name="checksum"></a>제외

아니요
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 정규식이 해당 `Regex_netherlands_eu_driver's_license_number` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- from `Keywords_netherlands_eu_driver's_license_number` 키워드를 찾았습니다. 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_netherlands_eu_driver's_license_number" />
          <Match idRef="Keywords_netherlands_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>키워드

| |
|**Keywords_netherlands_eu_driver's_license_number**|
|:-----|
|dl  <br/> driver license  <br/> 드라이버 라이선스 번호  <br/> 드라이버 라이선스  <br/> drivers lic  <br/> drivers license  <br/> drivers licence  <br/> driver's license  <br/> 운전 면허 번호  <br/> 운전 라이선스 번호  <br/> 운전 면허 번호  <br/> dlno #  <br/> permis de conduire  <br/> rijbewijs  <br/> rijbewijsnummer  <br/> |
   
## <a name="poland"></a>폴란드

### <a name="format"></a>형식일

두 개의 슬래시를 포함 하는 14 자리 숫자
  
### <a name="pattern"></a>패턴

14 자리 숫자와 2 개의 슬래시:
  
-  5자리 숫자 
    
- 정방향 슬래시
    
- 2자리 숫자
    
- 정방향 슬래시
    
- 7자리 숫자
    
### <a name="checksum"></a>제외

아니요
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 정규식이 해당 `Regex_poland_eu_driver's_license_number` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- from `Keywords_poland_eu_driver's_license_number` 키워드를 찾았습니다. 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_poland_eu_driver's_license_number" />
          <Match idRef="Keywords_poland_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>키워드

| |
|**Keywords_poland_eu_driver's_license_number**|
|:-----|
|dl  <br/> driver license  <br/> 드라이버 라이선스 번호  <br/> 드라이버 라이선스  <br/> drivers lic  <br/> drivers license  <br/> drivers licence  <br/> driver's license  <br/> 운전 면허 번호  <br/> 운전 라이선스 번호  <br/> 운전 면허 번호  <br/> dlno #  <br/> prawo jazdy  <br/> |
   
## <a name="portugal"></a>포르투갈

### <a name="format"></a>형식일

두 개의 문자와 지정 된 패턴에 있는 일곱 개의 숫자
  
### <a name="pattern"></a>패턴

두 문자 다음에 특수 문자를 사용한 7 개의 숫자를 입력 합니다.
  
-  2 개 문자 (대/소문자 구분 안 함) 
    
- 하이픈
    
- 6자리 숫자
    
- 공백
    
- 1자리 숫자
    
### <a name="checksum"></a>제외

아니요
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 정규식이 해당 `Regex_portugal_eu_driver's_license_number` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- from `Keywords_portugal_eu_driver's_license_number` 키워드를 찾았습니다. 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_portugal_eu_driver's_license_number" />
          <Match idRef="Keywords_portugal_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>키워드

| |
|**Keywords_portugal_eu_driver's_license_number**|
|:-----|
|dl  <br/> driver license  <br/> 드라이버 라이선스 번호  <br/> 드라이버 라이선스  <br/> drivers lic  <br/> drivers license  <br/> drivers licence  <br/> driver's license  <br/> 운전 면허 번호  <br/> 운전 라이선스 번호  <br/> 운전 면허 번호  <br/> dlno #  <br/> carteira de motorista  <br/> |
   
## <a name="romania"></a>루마니아

### <a name="format"></a>형식일

한 문자 다음에 8 자리 숫자
  
### <a name="pattern"></a>패턴

1 개의 문자 다음에 8 자리 숫자:
  
-  1 개 문자 (대/소문자 구분 안 함) 또는 숫자 
    
- 8자리 숫자
    
### <a name="checksum"></a>제외

아니요
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 정규식이 해당 `Regex_romania_eu_driver's_license_number` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- from `Keywords_romania_eu_driver's_license_number` 키워드를 찾았습니다. 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_romania_eu_driver's_license_number" />
          <Match idRef="Keywords_romania_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>키워드

| |
|**Keywords_romania_eu_driver's_license_number**|
|:-----|
|dl  <br/> driver license  <br/> 드라이버 라이선스 번호  <br/> 드라이버 라이선스  <br/> drivers lic  <br/> drivers license  <br/> drivers licence  <br/> driver's license  <br/> 운전 면허 번호  <br/> 운전 라이선스 번호  <br/> 운전 면허 번호  <br/> dlno #  <br/> permis de conducere  <br/> |
   
## <a name="slovakia"></a>슬로바키아

### <a name="format"></a>형식일

한 문자 다음에 7 자리 숫자
  
### <a name="pattern"></a>패턴

한 문자 다음에 7 자리 숫자
  
- 1 개 문자 (대/소문자 구분 안 함) 또는 숫자
    
-  7자리 숫자 
    
### <a name="checksum"></a>제외

아니요
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 정규식이 해당 `Regex_slovakia_eu_driver's_license_number` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- from `Keywords_slovakia_eu_driver's_license_number` 키워드를 찾았습니다. 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_slovaknia_eu_driver's_license_number" />
          <Match idRef="Keywords_slovakia_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>키워드

| |
|**Keywords_slovakia_eu_driver's_license_number**|
|:-----|
|dl  <br/> driver license  <br/> 드라이버 라이선스 번호  <br/> 드라이버 라이선스  <br/> drivers lic  <br/> drivers license  <br/> drivers licence  <br/> driver's license  <br/> 운전 면허 번호  <br/> 운전 라이선스 번호  <br/> 운전 면허 번호  <br/> dlno #  <br/> vodičský preukaz  <br/> |
   
## <a name="slovenia"></a>슬로베니아

### <a name="format"></a>형식일

공백과 구분 기호를 사용 하지 않고 9 자리 숫자
  
### <a name="pattern"></a>패턴

9자리 숫자
  
### <a name="checksum"></a>제외

아니요
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 정규식이 해당 `Regex_slovenia_eu_driver's_license_number` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- from `Keywords_slovenia_eu_driver's_license_number` 키워드를 찾았습니다. 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_slovenia_eu_driver's_license_number" />
          <Match idRef="Keywords_slovenia_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>키워드

| |
|**Keywords_slovenia_eu_driver's_license_number**|
|:-----|
|dl  <br/> driver license  <br/> 드라이버 라이선스 번호  <br/> 드라이버 라이선스  <br/> drivers lic  <br/> drivers license  <br/> drivers licence  <br/> driver's license  <br/> 운전 면허 번호  <br/> 운전 라이선스 번호  <br/> 운전 면허 번호  <br/> dlno #  <br/> vozniško dovoljenje  <br/> |
   
## <a name="spain"></a>스페인

### <a name="format"></a>형식일

8 자리 숫자와 문자 1 개
  
### <a name="pattern"></a>패턴

8 자리 숫자와 문자 1 개:
  
-  8자리 숫자 
    
- 1 자리 숫자 또는 문자 (대/소문자 구분 안 함)
    
### <a name="checksum"></a>제외

예
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 이 함수 `Func_spain_eu_driver's_license_number` 는 해당 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- from `Keywords_spain_eu_driver's_license_number` 키워드를 찾았습니다. 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Func_spain_eu_driver's_license_number" />
          <Match idRef="Keywords_spain_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>키워드

| |
|**Keywords_spain_eu_driver's_license_number**|
|:-----|
|dlno #  <br/> dl  <br/> drivers lic  <br/> 드라이버 라이선스  <br/> driver license  <br/> drivers licence  <br/> drivers license  <br/> driver's licence  <br/> driver's license  <br/> driving licence  <br/> driving license  <br/> 드라이버 라이선스 번호  <br/> 드라이버 라이선스 번호  <br/> 영향 요소 라이선스 번호  <br/> 운전 면허 번호  <br/> 운전 라이선스 번호  <br/> 운전 면허 번호  <br/> 운전 라이선스 번호  <br/> 운전 면허 번호  <br/> 추진 허용  <br/> 제어 허용 번호  <br/> permiso de conducción  <br/> permiso conducción  <br/> número licencia conducir  <br/> número de 네트워크 de conducir  <br/> número carnet conducir  <br/> licencia conducir  <br/> número de permiso de conducir  <br/> número de permiso conducir  <br/> número permiso conducir  <br/> permiso conducir  <br/> licencia de manejo  <br/> el carnet de conducir  <br/> carnet conducir  <br/> |
   
## <a name="sweden"></a>스웨덴

### <a name="format"></a>형식일

하이픈을 포함 하는 10 자리 숫자
  
### <a name="pattern"></a>패턴

하이픈을 포함 하는 10 자리 숫자:
  
-  6자리 숫자 
    
- 하이픈
    
- 4자리 숫자
    
### <a name="checksum"></a>제외

아니요
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 정규식이 해당 `Regex_sweden_eu_driver's_license_number` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- from `Keywords_sweden_eu_driver's_license_number` 키워드를 찾았습니다. 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_sweden_eu_driver's_license_number" />
          <Match idRef="Keywords_sweden_eu_driver's_license_number" />
        </Pattern>
</Entity> 
```

### <a name="keywords"></a>키워드

| |
|**Keywords_sweden_eu_driver's_license_number**|
|:-----|
|dl  <br/> driver license  <br/> 드라이버 라이선스 번호  <br/> 드라이버 라이선스  <br/> drivers lic  <br/> drivers license  <br/> drivers licence  <br/> driver's license  <br/> 운전 면허 번호  <br/> 운전 라이선스 번호  <br/> 운전 면허 번호  <br/> dlno #  <br/> körkort  <br/> |
   
## <a name="uk"></a>영국의

자세한 내용은 영국 섹션을 참조 하십시오. [중요 한 정보 유형에 서 확인 되는](what-the-sensitive-information-types-look-for.md)운전 면허 번호입니다.
  
## <a name="see-also"></a>참고 항목

[중요한 정보 형식이 찾는 항목](what-the-sensitive-information-types-look-for.md)

