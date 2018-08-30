---
title: EU 운전 면허 번호
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 8/17/2018
ms.audience: Admin
ms.topic: reference
ms.service: o365-administration
localization_priority: Normal
ms.assetid: c3923cd3-ec84-435f-bf41-cadc37996a4b
description: 이 항목에서는 EU 운전 면허 번호 중요 한 정보 유형을 감지 하는 경우의 데이터 손실 방지 (DLP) 정책을 찾아에 대해 보여줍니다. 이 중요 한 정보 유형 다양 한 패턴, 키워드 및 각 국가 대 한 기타 증거를 정의합니다.
ms.openlocfilehash: 065684249f9766d567c63e6b8170d36f56692e45
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22533461"
---
# <a name="eu-drivers-license-number"></a>EU 운전 면허 번호

이 항목에서는 EU 운전 면허 번호 중요 한 정보 유형을 감지 하는 경우의 데이터 손실 방지 (DLP) 정책을 찾아에 대해 보여줍니다. 이 중요 한 정보 유형 다양 한 패턴, 키워드 및 각 국가 대 한 기타 증거를 정의합니다.
  
## <a name="austria"></a>오스트리아

### <a name="format"></a>형식

공백 및 구분 기호 없이 8 개의 숫자
  
### <a name="pattern"></a>패턴

8자리 숫자
  
### <a name="checksum"></a>체크섬

없음
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 정규식 `Regex_austria_eu_driver's_license_number` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- 키워드에서 `Keywords_austria_eu_driver's_license_number` 를 찾을 수 있습니다. 
    
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
|dl #  <br/> 드라이버 라이선스  <br/> 운전 면허 번호  <br/> 드라이버 사용권  <br/> 드라이버 lic 합니다.  <br/> 운전 면허  <br/> 드라이버의 사용권  <br/> 드라이버의 라이선스  <br/> 운전 면허 번호  <br/> 드라이버의 사용권 번호  <br/>  운전 면허 번호  <br/> dlno #  <br/> fuhrerschein  <br/> fuhrerschein republik osterreich  <br/> |
   
## <a name="belgium"></a>벨기에

### <a name="format"></a>형식

공백 및 구분 기호 없이 10 자리 숫자
  
### <a name="pattern"></a>패턴

10자리 숫자
  
### <a name="checksum"></a>체크섬

없음
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 정규식 `Regex_belgium_eu_driver's_license_number` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- 키워드에서 `Keywords_belgium_eu_driver's_license_number` 를 찾을 수 있습니다. 
    
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
|dl #  <br/> 드라이버 라이선스  <br/> 운전 면허 번호  <br/> 드라이버 사용권  <br/> 드라이버 lic 합니다.  <br/> 운전 면허  <br/> drivers licence  <br/> 드라이버의 라이선스  <br/> 운전 면허 번호  <br/> 드라이버의 사용권 번호  <br/> dlno #  <br/> rijbewijs  <br/> rijbewijsnummer  <br/> führerscheinnummer  <br/> fuhrerscheinnummer  <br/> fuehrerscheinnummer  <br/> führerschein nr  <br/> fuehrerschein Nr  <br/> fuehrerschein nr  <br/> |
   
## <a name="bulgaria"></a>불가리아

### <a name="format"></a>형식

공백 및 구분 기호 없이 숫자 9 개
  
### <a name="pattern"></a>패턴

9자리 숫자
  
### <a name="checksum"></a>체크섬

없음
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 정규식 `Regex_bulgaria_eu_driver's_license_number` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- 키워드에서 `Keywords_bulgaria_eu_driver's_license_number` 를 찾을 수 있습니다. 
    
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
|dl #  <br/> 드라이버 라이선스  <br/> 운전 면허 번호  <br/> 드라이버 사용권  <br/> 드라이버 lic 합니다.  <br/> 운전 면허  <br/> drivers licence  <br/> 드라이버의 라이선스  <br/> 운전 면허 번호  <br/> 드라이버의 사용권 번호  <br/> 운전 면허 번호  <br/> dlno #  <br/> СВИДЕТЕЛСТВО ЗА УПРАВЛЕНИЕ НА МПС  <br/> СВИДЕТЕЛСТВО ЗА УПРАВЛЕНИЕ НА МОТОРНО ПРЕВОЗНО СРЕДСТВО  <br/> СУМПС  <br/> ШОФЬОРСКА КНИЖКА  <br/> |
   
## <a name="croatia"></a>크로아티아

### <a name="format"></a>형식

공백 및 구분 기호 없이 8 개의 숫자
  
### <a name="pattern"></a>패턴

8자리 숫자
  
### <a name="checksum"></a>체크섬

없음
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 정규식 `Regex_croatia_eu_driver's_license_number` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- 키워드에서 `Keywords_croatia_eu_driver's_license_number` 를 찾을 수 있습니다. 
    
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
|dl #  <br/> 드라이버 라이선스  <br/> 운전 면허 번호  <br/> 드라이버 사용권  <br/> 드라이버 lic 합니다.  <br/> 운전 면허  <br/> drivers licence  <br/> 드라이버의 라이선스  <br/> 운전 면허 번호  <br/> 드라이버의 사용권 번호  <br/> 운전 면허 번호  <br/> dlno #  <br/> vozačka dozvola  <br/> |
   
## <a name="cyprus"></a>키프로스

### <a name="format"></a>형식

공백 및 구분 기호 없이 12 자리
  
### <a name="pattern"></a>패턴

12자리 숫자
  
### <a name="checksum"></a>체크섬

없음
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 정규식 `Regex_cyprus_eu_driver's_license_number` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- 키워드에서 `Keywords_cyprus_eu_driver's_license_number` 를 찾을 수 있습니다. 
    
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
|dl #  <br/> 드라이버 라이선스  <br/> 운전 면허 번호  <br/> 드라이버 사용권  <br/> 드라이버 lic 합니다.  <br/> 운전 면허  <br/> drivers licence  <br/> 운전 면허 번호  <br/> 드라이버의 사용권 번호  <br/> 운전 면허 번호  <br/> dlno #  <br/> ΆΔΕΙΑ ΟΔΉΓΗΣΗΣ  <br/> |
   
## <a name="czech-republic"></a>체코 공화국

### <a name="format"></a>형식

6 자리 숫자 앞에 오는 두 문자
  
### <a name="pattern"></a>패턴

8 대 문자와 숫자:
  
- 두 문자 (대 소문자 구분 안함)
    
- 공백 1개(선택 사항)
    
- 6자리 숫자
    
### <a name="checksum"></a>체크섬

없음
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 정규식 `Regex_czech_republic_eu_driver's_license_number` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- 키워드에서 `Keywords_czech_republic_eu_driver's_license_number` 를 찾을 수 있습니다. 
    
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
|dl #  <br/> 드라이버 라이선스  <br/> 운전 면허 번호  <br/> 드라이버 사용권  <br/> 드라이버 lic 합니다.  <br/> 운전 면허  <br/> drivers licence  <br/> 드라이버의 라이선스  <br/> 운전 면허 번호  <br/> 운전 면허 번호  <br/> 드라이버의 사용권 번호  <br/> 운전 면허 번호  <br/> dlno #  <br/> Řidičský prúkaz  <br/> |
   
## <a name="denmark"></a>덴마크

### <a name="format"></a>형식

공백 및 구분 기호 없이 8 개의 숫자
  
### <a name="pattern"></a>패턴

8자리 숫자
  
### <a name="checksum"></a>체크섬

예
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 정규식 `Regex_denmark_eu_driver's_license_number` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- 키워드에서 `Keywords_denmark_eu_driver's_license_number` 를 찾을 수 있습니다. 
    
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
|dl #  <br/> 드라이버 라이선스  <br/> 운전 면허 번호  <br/> 드라이버 사용권  <br/> 드라이버 lic 합니다.  <br/> 운전 면허  <br/> drivers licence  <br/> 드라이버의 라이선스  <br/> 운전 면허 번호  <br/> 드라이버의 사용권 번호  <br/> 운전 면허 번호  <br/> dlno #  <br/> kørekort  <br/> kørekortnummer  <br/> |
   
## <a name="estonia"></a>에스토니아

### <a name="format"></a>형식

6 자리 숫자 앞에 오는 두 문자
  
### <a name="pattern"></a>패턴

두 대 문자와 6 자리 숫자:
  
-  문자 "ET" (대 소문자 구분 안함) 
    
- 6자리 숫자
    
### <a name="checksum"></a>체크섬

없음
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 정규식 `Regex_estonia_eu_driver's_license_number` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- 키워드에서 `Keywords_estonia_eu_driver's_license_number` 를 찾을 수 있습니다. 
    
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
|dl #  <br/> 드라이버 라이선스  <br/> 운전 면허 번호  <br/> 운전 면허 번호  <br/> 드라이버 사용권  <br/> 드라이버 lic 합니다.  <br/> 운전 면허  <br/> drivers licence  <br/> 드라이버의 라이선스  <br/> 운전 면허 번호  <br/> 운전 면허 번호  <br/> dlno #  <br/> 
permis de conduire  <br/> |
   
## <a name="finland"></a>핀란드

### <a name="format"></a>형식

하이픈을 포함하는 10자리 숫자
  
### <a name="pattern"></a>패턴

하이픈을 포함 하는 10 자리 숫자:
  
-  6자리 숫자 
    
- 하이픈
    
-  4자리 숫자 
    
### <a name="checksum"></a>체크섬

없음
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 정규식 `Regex_finland_eu_driver's_license_number` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- 키워드에서 `Keywords_finland_eu_driver's_license_number` 를 찾을 수 있습니다. 
    
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
|dl #  <br/> 드라이버 라이선스  <br/> 운전 면허 번호  <br/> 드라이버 사용권  <br/> 드라이버 lic 합니다.  <br/> 운전 면허  <br/> drivers licence  <br/> 드라이버의 라이선스  <br/> 운전 면허 번호  <br/> 드라이버의 사용권 번호  <br/> 운전 면허 번호  <br/> dlno #  <br/> ajokortti  <br/> |
   
## <a name="france"></a>프랑스

자세한 내용은의 섹션을 참조 "프랑스 운전 면허 번호" [에 대 한 중요 한 정보 유형을 확인](what-the-sensitive-information-types-look-for.md)합니다.
  
## <a name="germany"></a>독일

자세한 내용은의 섹션을 참조 "독일 운전 면허 번호" [에 대 한 중요 한 정보 유형을 확인](what-the-sensitive-information-types-look-for.md)합니다.
  
## <a name="greece"></a>그리스

### <a name="format"></a>형식

공백 및 구분 기호 없이 숫자 9 개
  
### <a name="pattern"></a>패턴

 9자리 숫자 
  
### <a name="checksum"></a>체크섬

없음
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 정규식 `Regex_greece_eu_driver's_license_number` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- 키워드에서 `Keywords_greece_eu_driver's_license_number` 를 찾을 수 있습니다. 
    
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
|dlL #  <br/> 드라이버 라이선스  <br/> 운전 면허 번호  <br/> 드라이버 사용권  <br/> 드라이버 lic 합니다.  <br/> 운전 면허  <br/> drivers licence  <br/> 드라이버의 라이선스  <br/> 운전 면허 번호  <br/> 드라이버의 사용권 번호  <br/> 운전 면허 번호  <br/> dlno #  <br/> ΔΕΙΑ ΟΔΉΓΗΣΗΣ  <br/> Adeia odigisis  <br/> |
   
## <a name="hungary"></a>헝가리

### <a name="format"></a>형식

6 자리 숫자 앞에 오는 두 문자
  
### <a name="pattern"></a>패턴

두 대 문자와 6 자리 숫자:
  
-  두 문자 (대 소문자 구분 안함) 
    
- 6자리 숫자
    
### <a name="checksum"></a>체크섬

없음
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 정규식 `Regex_hungary_eu_driver's_license_number` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- 키워드에서 `Keywords_hungary_eu_driver's_license_number` 를 찾을 수 있습니다. 
    
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
|dl #  <br/> 드라이버 라이선스  <br/> 운전 면허 번호  <br/> 드라이버 사용권  <br/> 드라이버 lic 합니다.  <br/> 운전 면허  <br/> drivers licence  <br/> 드라이버의 라이선스  <br/> 운전 면허 번호  <br/> 드라이버의 사용권 번호  <br/> 운전 면허 번호  <br/> dlno #  <br/> vezetoi engedely  <br/> |
   
## <a name="ireland"></a>Ireland

### <a name="format"></a>형식

4 개의 문자 앞에 오는 6 자리 숫자
  
### <a name="pattern"></a>패턴

6 자리 숫자 및 4 개의 문자:
  
- 6자리 숫자
    
- 4 개의 문자 (대 소문자 구분 안함)
    
### <a name="checksum"></a>체크섬

없음
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 정규식 `Regex_ireland_eu_driver's_license_number` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- 키워드에서 `Keywords_ireland_eu_driver's_license_number` 를 찾을 수 있습니다. 
    
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
|dl #  <br/> 드라이버 라이선스  <br/> 운전 면허 번호  <br/> 드라이버 사용권  <br/> 드라이버 lic 합니다.  <br/> 운전 면허  <br/> drivers licence  <br/> 드라이버의 라이선스  <br/> 운전 면허 번호  <br/> 드라이버의 사용권 번호  <br/> 운전 면허 번호  <br/> dlno #  <br/> ceadúnas tiomána  <br/> |
   
## <a name="italy"></a>이탈리아

자세한 내용은의 섹션을 참조 "이탈리아 운전 면허 번호" [에 대 한 중요 한 정보 유형을 확인](what-the-sensitive-information-types-look-for.md)합니다.
  
## <a name="latvia"></a>라트비아

### <a name="format"></a>형식

6 자리 숫자 앞에 오는 세 개 문자
  
### <a name="pattern"></a>패턴

3 대 문자와 6 자리 숫자:
  
-  세 개 문자 (대 소문자 구분 안함) 
    
- 6자리 숫자
    
### <a name="checksum"></a>체크섬

없음
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 정규식 `Regex_latvia_eu_driver's_license_number` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- 키워드에서 `Keywords_latvia_eu_driver's_license_number` 를 찾을 수 있습니다. 
    
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
|dl #  <br/> 드라이버 라이선스  <br/> 운전 면허 번호  <br/> 드라이버 사용권  <br/> 드라이버 lic 합니다.  <br/> 운전 면허  <br/> drivers licence  <br/> 드라이버의 라이선스  <br/> 운전 면허 번호  <br/> 드라이버의 사용권 번호  <br/> 운전 면허 번호  <br/> dlno #  <br/> autovadītāja apliecība  <br/> |
   
## <a name="lithuania"></a>리투아니아

### <a name="format"></a>형식

공백 및 구분 기호 없이 8 개의 숫자
  
### <a name="pattern"></a>패턴

 8자리 숫자 
  
### <a name="checksum"></a>체크섬

없음
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 정규식 `Regex_lithuania_eu_driver's_license_number` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- 키워드에서 `Keywords_lithuania_eu_driver's_license_number` 를 찾을 수 있습니다. 
    
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
|dl #  <br/> 드라이버 라이선스  <br/> 운전 면허 번호  <br/> 드라이버 사용권  <br/> 드라이버 lic 합니다.  <br/> 운전 면허  <br/> drivers licence  <br/> 드라이버의 라이선스  <br/> 운전 면허 번호  <br/> 드라이버의 사용권 번호  <br/> 운전 면허 번호  <br/> dlno #  <br/> vairuotojo pažymėjimas  <br/> |
   
## <a name="luxemburg"></a>룩셈부르크

### <a name="format"></a>형식

공백 및 구분 기호 없이 6 자리 숫자
  
### <a name="pattern"></a>패턴

 6자리 숫자 
  
### <a name="checksum"></a>체크섬

없음
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 정규식 `Regex_luxemburg_eu_driver's_license_number` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- 키워드에서 `Keywords_luxemburg_eu_driver's_license_number` 를 찾을 수 있습니다. 
    
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
|dl #  <br/> 드라이버 라이선스  <br/> 운전 면허 번호  <br/> 드라이버 사용권  <br/> 드라이버 lic 합니다.  <br/> 운전 면허  <br/> drivers licence  <br/> 드라이버의 라이선스  <br/> 운전 면허 번호  <br/> 드라이버의 사용권 번호  <br/> 운전 면허 번호  <br/> dlno #  <br/> fahrerlaubnis  <br/> |
   
## <a name="malta"></a>몰타

### <a name="format"></a>형식

두 문자 및 지정된 된 패턴에 6 자리 숫자의 조합
  
### <a name="pattern"></a>패턴

두 문자와 6 자리 숫자의 조합 합니다.
  
- 두 문자 (숫자 또는 문자, 대 소문자 구분 안함)
    
- 공백 1개(선택 사항)
    
- 3자리 숫자
    
- 공백 1개(선택 사항)
    
- 3자리 숫자
    
### <a name="checksum"></a>체크섬

없음
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 정규식 `Regex_malta_eu_driver's_license_number` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- 키워드에서 `Keywords_malta_eu_driver's_license_number` 를 찾을 수 있습니다. 
    
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
|dl #  <br/> 드라이버 라이선스  <br/> 운전 면허 번호  <br/> 드라이버 사용권  <br/> 드라이버 lic 합니다.  <br/> 운전 면허  <br/> drivers licence  <br/> 드라이버의 라이선스  <br/> 운전 면허 번호  <br/> 드라이버의 사용권 번호  <br/> 운전 면허 번호  <br/> dlno #  <br/> liċenzja 게 sewqan  <br/> |
   
## <a name="netherlands"></a>네덜란드

### <a name="format"></a>형식

공백 및 구분 기호 없이 10 자리 숫자
  
### <a name="pattern"></a>패턴

10자리 숫자
  
### <a name="checksum"></a>체크섬

없음
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 정규식 `Regex_netherlands_eu_driver's_license_number` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- 키워드에서 `Keywords_netherlands_eu_driver's_license_number` 를 찾을 수 있습니다. 
    
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
|dl #  <br/> 드라이버 라이선스  <br/> 운전 면허 번호  <br/> 드라이버 사용권  <br/> 드라이버 lic 합니다.  <br/> 운전 면허  <br/> drivers licence  <br/> 드라이버의 라이선스  <br/> 운전 면허 번호  <br/> 드라이버의 사용권 번호  <br/> 운전 면허 번호  <br/> dlno #  <br/> 
permis de conduire  <br/> rijbewijs  <br/> rijbewijsnummer  <br/> |
   
## <a name="poland"></a>폴란드

### <a name="format"></a>형식

2 슬래시를 포함 하는 14 자리 숫자
  
### <a name="pattern"></a>패턴

14 숫자 및 2 슬래시:
  
-  5자리 숫자 
    
- 정방향 슬래시
    
- 2자리 숫자
    
- 정방향 슬래시
    
- 7자리 숫자
    
### <a name="checksum"></a>체크섬

없음
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 정규식 `Regex_poland_eu_driver's_license_number` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- 키워드에서 `Keywords_poland_eu_driver's_license_number` 를 찾을 수 있습니다. 
    
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
|dl #  <br/> 드라이버 라이선스  <br/> 운전 면허 번호  <br/> 드라이버 사용권  <br/> 드라이버 lic 합니다.  <br/> 운전 면허  <br/> drivers licence  <br/> 드라이버의 라이선스  <br/> 운전 면허 번호  <br/> 드라이버의 사용권 번호  <br/> 운전 면허 번호  <br/> dlno #  <br/> prawo jazdy  <br/> |
   
## <a name="portugal"></a>포르투갈

### <a name="format"></a>형식

지정된 된 패턴에 일곱 개의 숫자 앞에 오는 두 문자
  
### <a name="pattern"></a>패턴

특수 문자가 포함 된 7 번호 앞에 오는 두 문자 수:
  
-  두 문자 (대 소문자 구분 안함) 
    
- 하이픈
    
- 6자리 숫자
    
- 공백
    
- 1자리 숫자
    
### <a name="checksum"></a>체크섬

없음
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 정규식 `Regex_portugal_eu_driver's_license_number` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- 키워드에서 `Keywords_portugal_eu_driver's_license_number` 를 찾을 수 있습니다. 
    
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
|dl #  <br/> 드라이버 라이선스  <br/> 운전 면허 번호  <br/> 드라이버 사용권  <br/> 드라이버 lic 합니다.  <br/> 운전 면허  <br/> drivers licence  <br/> 드라이버의 라이선스  <br/> 운전 면허 번호  <br/> 드라이버의 사용권 번호  <br/> 운전 면허 번호  <br/> dlno #  <br/> carteira de motorista  <br/> |
   
## <a name="romania"></a>루마니아

### <a name="format"></a>형식

8 개의 숫자 앞에 오는 문자 하나
  
### <a name="pattern"></a>패턴

8 개의 숫자 앞에 오는 문자 하나:
  
-  하나의 문자 (대 소문자 구분 안함) 또는 숫자 
    
- 8자리 숫자
    
### <a name="checksum"></a>체크섬

없음
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 정규식 `Regex_romania_eu_driver's_license_number` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- 키워드에서 `Keywords_romania_eu_driver's_license_number` 를 찾을 수 있습니다. 
    
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
|dl #  <br/> 드라이버 라이선스  <br/> 운전 면허 번호  <br/> 드라이버 사용권  <br/> 드라이버 lic 합니다.  <br/> 운전 면허  <br/> drivers licence  <br/> 드라이버의 라이선스  <br/> 운전 면허 번호  <br/> 드라이버의 사용권 번호  <br/> 운전 면허 번호  <br/> dlno #  <br/> permis de conducere  <br/> |
   
## <a name="slovakia"></a>슬로바키아

### <a name="format"></a>형식

7 자리 숫자 앞에 오는 문자 하나
  
### <a name="pattern"></a>패턴

7 자리 숫자 앞에 오는 문자 하나
  
- 하나의 문자 (대 소문자 구분 안함) 또는 숫자
    
-  7자리 숫자 
    
### <a name="checksum"></a>체크섬

없음
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 정규식 `Regex_slovakia_eu_driver's_license_number` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- 키워드에서 `Keywords_slovakia_eu_driver's_license_number` 를 찾을 수 있습니다. 
    
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
|dl #  <br/> 드라이버 라이선스  <br/> 운전 면허 번호  <br/> 드라이버 사용권  <br/> 드라이버 lic 합니다.  <br/> 운전 면허  <br/> drivers licence  <br/> 드라이버의 라이선스  <br/> 운전 면허 번호  <br/> 드라이버의 사용권 번호  <br/> 운전 면허 번호  <br/> dlno #  <br/> vodičský preukaz  <br/> |
   
## <a name="slovenia"></a>슬로베니아

### <a name="format"></a>형식

공백 및 구분 기호 없이 숫자 9 개
  
### <a name="pattern"></a>패턴

9자리 숫자
  
### <a name="checksum"></a>체크섬

없음
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 정규식 `Regex_slovenia_eu_driver's_license_number` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- 키워드에서 `Keywords_slovenia_eu_driver's_license_number` 를 찾을 수 있습니다. 
    
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
|dl #  <br/> 드라이버 라이선스  <br/> 운전 면허 번호  <br/> 드라이버 사용권  <br/> 드라이버 lic 합니다.  <br/> 운전 면허  <br/> drivers licence  <br/> 드라이버의 라이선스  <br/> 운전 면허 번호  <br/> 드라이버의 사용권 번호  <br/> 운전 면허 번호  <br/> dlno #  <br/> vozniško dovoljenje  <br/> |
   
## <a name="spain"></a>스페인

### <a name="format"></a>형식

한 문자 앞에 오는 8 개의 숫자
  
### <a name="pattern"></a>패턴

8 개의 숫자를 한 글자 앞에 오는:
  
-  8자리 숫자 
    
- 한 자리 숫자 또는 문자 (대 소문자 구분 안함)
    
### <a name="checksum"></a>체크섬

예
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 다음은 함수 `Func_spain_eu_driver's_license_number` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- 키워드에서 `Keywords_spain_eu_driver's_license_number` 를 찾을 수 있습니다. 
    
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
|dlno #  <br/> dl #  <br/> 드라이버 lic 합니다.  <br/> 드라이버 사용권  <br/> 드라이버 라이선스  <br/> drivers licence  <br/> 
drivers license  <br/> 드라이버의 사용권  <br/> 드라이버의 라이선스  <br/> driving licence
  <br/> 라이선스를 제어합니다.  <br/> 드라이버 사용권 번호  <br/> 운전 면허 번호  <br/> 드라이버는 사용권 번호  <br/> 운전 면허 번호  <br/> 드라이버의 사용권 번호  <br/> 운전 면허 번호  <br/> driving 사용권 번호  <br/> 운전 면허 번호  <br/> 허용 제어  <br/> 허용 수를 제어합니다.  <br/> permiso de conducción  <br/> permiso conducción  <br/> número licencia conducir  <br/> número de carnet de conducir  <br/> número carnet conducir  <br/> licencia conducir  <br/> número de permiso de conducir  <br/> número de permiso conducir  <br/> número permiso conducir  <br/> permiso conducir  <br/> licencia de manejo  <br/> el carnet de conducir  <br/> carnet conducir  <br/> |
   
## <a name="sweden"></a>스웨덴

### <a name="format"></a>형식

하이픈을 포함 하는 10 자리 숫자
  
### <a name="pattern"></a>패턴

하이픈을 포함 하는 10 자리 숫자:
  
-  6자리 숫자 
    
- 하이픈
    
- 4자리 숫자
    
### <a name="checksum"></a>체크섬

없음
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 정규식 `Regex_sweden_eu_driver's_license_number` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- 키워드에서 `Keywords_sweden_eu_driver's_license_number` 를 찾을 수 있습니다. 
    
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
|dl #  <br/> 드라이버 라이선스  <br/> 운전 면허 번호  <br/> 드라이버 사용권  <br/> 드라이버 lic 합니다.  <br/> 운전 면허  <br/> drivers licence  <br/> 드라이버의 라이선스  <br/> 운전 면허 번호  <br/> 드라이버의 사용권 번호  <br/> 운전 면허 번호  <br/> dlno #  <br/> körkort  <br/> |
   
## <a name="uk"></a>영국

자세한 내용은의 섹션을 참조 "영국 운전 면허 번호" [에 대 한 중요 한 정보 유형을 확인](what-the-sensitive-information-types-look-for.md)합니다.
  
## <a name="see-also"></a>참고 항목

[중요한 정보 형식이 찾는 항목](what-the-sensitive-information-types-look-for.md)

