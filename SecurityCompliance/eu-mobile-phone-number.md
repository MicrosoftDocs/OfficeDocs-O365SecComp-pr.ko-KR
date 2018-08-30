---
title: EU 휴대폰 번호
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 8/16/2018
ms.audience: Admin
ms.topic: reference
ms.service: o365-administration
localization_priority: Normal
ms.assetid: 555e7675-2ae8-42d1-9b8e-2c8f8cd21337
description: Office 365 보안에서 데이터 손실 방지 (DLP) &amp; 준수 센터 DLP 정책에서 사용 하 여 사용할 수 있는 많은 중요 한 정보 유형을 포함 합니다. 이 항목에서는 EU 휴대폰 번호 중요 한 정보 유형에 설명 합니다.
ms.openlocfilehash: d0818759dae8ed86cc9aef6f7fad48cbd2acf24f
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22533403"
---
# <a name="eu-mobile-phone-number"></a>EU 휴대폰 번호

Office 365 보안에서 데이터 손실 방지 (DLP) &amp; 준수 센터 DLP 정책에서 사용 하 여 사용할 수 있는 많은 중요 한 정보 유형을 포함 합니다. 이 항목에서는 EU 휴대폰 번호 중요 한 정보 유형에 설명 합니다. 
  
## <a name="austria"></a>오스트리아

### <a name="format"></a>형식

표준 길이 없이 자릿수
  
### <a name="pattern"></a>패턴

-  숫자 
    
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 정규식 `Regex_austria_eu_mobile_number` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- 정규식 `Regex_austria_eu_formatted_mobile_number` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- 키워드에서 `Keywords_austria_eu_mobile_number` 를 찾을 수 있습니다. 
    
```
 
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_austria_eu_mobile_number"/>
          <Match idRef="Keywords_austria_eu_mobile_number" />
        </Pattern>
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_austria_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="belgium"></a>벨기에

### <a name="pattern"></a>패턴

-  숫자 
    
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 정규식 `Regex_belgium_eu_mobile_number` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- 정규식 `Regex_belgium_eu_formatted_mobile_number` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- 키워드에서 `Keywords_belgium_eu_mobile_number` 를 찾을 수 있습니다. 
    
```
 
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_belgium_eu_mobile_number"/>
          <Match idRef="Keywords_belgium_eu_mobile_number" />
        </Pattern>
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_belgium_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="bulgaria"></a>불가리아

### <a name="pattern"></a>패턴

-  숫자 
    
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 정규식 `Regex_bulgaria_eu_mobile_number` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- 정규식 `Regex_bulgaria_eu_formatted_mobile_number` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- 키워드에서 `Keywords_bulgaria_eu_mobile_number` 를 찾을 수 있습니다. 
    
```
 
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_bulgaria_eu_mobile_number"/>
          <Match idRef="Keywords_bulgaria_eu_mobile_number" />
        </Pattern>
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_bulgaria_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="croatia"></a>크로아티아

### <a name="pattern"></a>패턴

-  숫자 
    
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 정규식 `Regex_croatia_eu_mobile_number` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- 정규식 `Regex_croatia_eu_formatted_mobile_number` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- 키워드에서 `Keywords_croatia_eu_mobile_number` 를 찾을 수 있습니다. 
    
```
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_croatia_eu_mobile_number"/>
          <Match idRef="Keywords_croatia_eu_mobile_number" />
        </Pattern>
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_croatia_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="cyprus"></a>키프로스

### <a name="pattern"></a>패턴

-  숫자 
    
### <a name="checksum"></a>체크섬

해당 없음
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 정규식 `Regex_cyprus_eu_mobile_number` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- 정규식 `Regex_cyprus_eu_formatted_mobile_number` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- 키워드에서 `Keywords_cyprus_eu_mobile_number` 를 찾을 수 있습니다. 
    
```
 
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_cyprus_eu_mobile_number"/>
          <Match idRef="Keywords_cyprus_eu_mobile_number" />
        </Pattern>
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_cyprus_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="czech-republic"></a>체코 공화국

### <a name="pattern"></a>패턴

-  숫자 
    
### <a name="checksum"></a>체크섬

해당 없음
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 정규식 `Regex_czech_republic_eu_mobile_number` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- 정규식 `Regex_czech_republic_eu_formatted_mobile_number` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- 키워드에서 `Keywords_czech_republic_eu_mobile_number` 를 찾을 수 있습니다. 
    
```
 
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_czech_republic_eu_mobile_number"/>
          <Match idRef="Keywords_czech_republic_eu_mobile_number" />
        </Pattern>
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_czech_republic_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="denmark"></a>덴마크

### <a name="pattern"></a>패턴

-  숫자 
    
### <a name="checksum"></a>체크섬

해당 없음
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 정규식 `Regex_denmark_eu_mobile_number` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- 정규식 `Regex_denmark_eu_formatted_mobile_number` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- 키워드에서 `Keywords_denmark_eu_mobile_number` 를 찾을 수 있습니다. 
    
```
 
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_denmark_eu_mobile_number"/>
          <Match idRef="Keywords_denmark_eu_mobile_number" />
        </Pattern>
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_denmark_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="estonia"></a>에스토니아

### <a name="pattern"></a>패턴

-  숫자 
    
### <a name="checksum"></a>체크섬

해당 없음
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 정규식 `Regex_estonia_eu_mobile_number` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- 정규식 `Regex_estonia_eu_formatted_mobile_number` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- 키워드에서 `Keywords_estonia_eu_mobile_number` 를 찾을 수 있습니다. 
    
```
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_estonia_eu_mobile_number"/>
          <Match idRef="Keywords_estonia_eu_mobile_number" />
        </Pattern>
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_estonia_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="finland"></a>핀란드

### <a name="pattern"></a>패턴

-  숫자 
    
### <a name="checksum"></a>체크섬

해당 없음
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 정규식 `Regex_finland_eu_mobile_number` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- 정규식 `Regex_finland_eu_formatted_mobile_number` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- 키워드에서 `Keywords_finland_eu_mobile_number` 를 찾을 수 있습니다. 
    
```
 
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_finland_eu_mobile_number"/>
          <Match idRef="Keywords_finland_eu_mobile_number" />
        </Pattern>
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_finland_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="france"></a>프랑스

### <a name="pattern"></a>패턴

-  숫자 
    
### <a name="checksum"></a>체크섬

해당 없음
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 정규식 `Regex_france_eu_mobile_number` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- 정규식 `Regex_france_eu_formatted_mobile_number` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- 키워드에서 `Keywords_france_eu_mobile_number` 를 찾을 수 있습니다. 
    
```
 
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_france_eu_mobile_number"/>
          <Match idRef="Keywords_france_eu_mobile_number" />
        </Pattern>
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_france_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="germany"></a>독일

### <a name="pattern"></a>패턴

-  숫자 
    
### <a name="checksum"></a>체크섬

해당 없음
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 정규식 `Regex_germany_eu_mobile_number` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- 정규식 `Regex_germany_eu_formatted_mobile_number` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- 키워드에서 `Keywords_germany_eu_mobile_number` 를 찾을 수 있습니다. 
    
```
 
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_germany_eu_mobile_number"/>
          <Match idRef="Keywords_germany_eu_mobile_number" />
        </Pattern>
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_germany_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="greece"></a>그리스

### <a name="pattern"></a>패턴

-  숫자 
    
### <a name="checksum"></a>체크섬

해당 없음
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 정규식 `Regex_greece_eu_mobile_number` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- 정규식 `Regex_greece_eu_formatted_mobile_number` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- 키워드에서 `Keywords_greece_eu_mobile_number` 를 찾을 수 있습니다. 
    
```
 
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_greece_eu_mobile_number"/>
          <Match idRef="Keywords_greece_eu_mobile_number" />
        </Pattern>
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_greece_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="hungary"></a>헝가리

### <a name="pattern"></a>패턴

-  숫자 
    
### <a name="checksum"></a>체크섬

해당 없음
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 정규식 `Regex_hungary_eu_mobile_number` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- 정규식 `Regex_hungary_eu_formatted_mobile_number` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- 키워드에서 `Keywords_hungary_eu_mobile_number` 를 찾을 수 있습니다. 
    
```
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_hungary_eu_mobile_number"/>
          <Match idRef="Keywords_hungary_eu_mobile_number" />
        </Pattern>
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_hungary_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="ireland"></a>Ireland

### <a name="pattern"></a>패턴

-  숫자 
    
### <a name="checksum"></a>체크섬

해당 없음
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 정규식 `Regex_ireland_eu_mobile_number` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- 정규식 `Regex_ireland_eu_formatted_mobile_number` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- 키워드에서 `Keywords_ireland_eu_mobile_number` 를 찾을 수 있습니다. 
    
```
 
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_ireland_eu_mobile_number"/>
          <Match idRef="Keywords_ireland_eu_mobile_number" />
        </Pattern>
<!-- Strictly formatted patterns without mandatory corroborative evidence -->
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_ireland_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="italy"></a>이탈리아

### <a name="pattern"></a>패턴

-  숫자 
    
### <a name="checksum"></a>체크섬

해당 없음
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 정규식 `Regex_italy_eu_mobile_number` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- 정규식 `Regex_italy_eu_formatted_mobile_number` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- 키워드에서 `Keywords_italy_eu_mobile_number` 를 찾을 수 있습니다. 
    
```
 
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_italy_eu_mobile_number"/>
          <Match idRef="Keywords_italy_eu_mobile_number" />
        </Pattern>
<!-- Strictly formatted patterns without mandatory corroborative evidence -->
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_italy_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="latvia"></a>라트비아

### <a name="pattern"></a>패턴

-  숫자 
    
### <a name="checksum"></a>체크섬

해당 없음
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 정규식 `Regex_latvia_eu_mobile_number` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- 정규식 `Regex_latvia_eu_formatted_mobile_number` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- 키워드에서 `Keywords_latvia_eu_mobile_number` 를 찾을 수 있습니다. 
    
```
 
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_latvia_eu_mobile_number"/>
          <Match idRef="Keywords_latvia_eu_mobile_number" />
        </Pattern>
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_latvia_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="lithuania"></a>리투아니아

### <a name="pattern"></a>패턴

-  숫자 
    
### <a name="checksum"></a>체크섬

해당 없음
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 정규식 `Regex_lithuania_eu_mobile_number` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- 정규식 `Regex_lithuania_eu_formatted_mobile_number` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- 키워드에서 `Keywords_lithuania_eu_mobile_number` 를 찾을 수 있습니다. 
    
```
 
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_lithuania_eu_mobile_number"/>
          <Match idRef="Keywords_lithuania_eu_mobile_number" />
        </Pattern>
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_lithuania_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="luxemburg"></a>룩셈부르크

### <a name="pattern"></a>패턴

-  숫자 
    
### <a name="checksum"></a>체크섬

해당 없음
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 정규식 `Regex_luxumburg_eu_mobile_number` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- 정규식 `Regex_luxumburg_eu_formatted_mobile_number` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- 키워드에서 `Keywords_luxumburg_eu_mobile_number` 를 찾을 수 있습니다. 
    
```
 
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_luxumburg_eu_mobile_number"/>
          <Match idRef="Keywords_luxumburg_eu_mobile_number" />
        </Pattern>
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_luxumburg_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="malta"></a>몰타

### <a name="pattern"></a>패턴

-  숫자 
    
### <a name="checksum"></a>체크섬

해당 없음
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 정규식 `Regex_malta_eu_mobile_number` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- 정규식 `Regex_malta_eu_formatted_mobile_number` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- 키워드에서 `Keywords_malta_eu_mobile_number` 를 찾을 수 있습니다. 
    
```
 
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_malta_eu_mobile_number"/>
          <Match idRef="Keywords_malta_eu_mobile_number" />
        </Pattern>
<!-- Strictly formatted patterns without mandatory corroborative evidence -->
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_malta_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="netherlands"></a>네덜란드

### <a name="pattern"></a>패턴

-  숫자 
    
### <a name="checksum"></a>체크섬

해당 없음
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 정규식 `Regex_netherlands_eu_mobile_number` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- 정규식 `Regex_netherlands_eu_formatted_mobile_number` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- 키워드에서 `Keywords_netherlands_eu_mobile_number` 를 찾을 수 있습니다. 
    
```
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_netherlands_eu_mobile_number"/>
          <Match idRef="Keywords_netherlands_eu_mobile_number" />
        </Pattern>
<!-- Strictly formatted patterns without mandatory corroborative evidence -->
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_netherlands_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="poland"></a>폴란드

### <a name="pattern"></a>패턴

-  숫자 
    
### <a name="checksum"></a>체크섬

해당 없음
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 정규식 `Regex_poland_eu_mobile_number` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- 정규식 `Regex_poland_eu_formatted_mobile_number` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- 키워드에서 `Keywords_poland_eu_mobile_number` 를 찾을 수 있습니다. 
    
```
 
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_poland_eu_mobile_number"/>
          <Match idRef="Keywords_poland_eu_mobile_number" />
        </Pattern>
<!-- Strictly formatted patterns without mandatory corroborative evidence -->
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_poland_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="portugal"></a>포르투갈

### <a name="pattern"></a>패턴

-  숫자 
    
### <a name="checksum"></a>체크섬

해당 없음
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 정규식 `Regex_portugal_eu_mobile_number` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- 정규식 `Regex_portugal_eu_formatted_mobile_number` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- 키워드에서 `Keywords_portugal_eu_mobile_number` 를 찾을 수 있습니다. 
    
```
 
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_portugal_eu_mobile_number"/>
          <Match idRef="Keywords_portugal_eu_mobile_number" />
        </Pattern>
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_portugal_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="romania"></a>루마니아

### <a name="pattern"></a>패턴

-  숫자 
    
### <a name="checksum"></a>체크섬

해당 없음
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 정규식 `Regex_romania_eu_mobile_number` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- 정규식 `Regex_romania_eu_formatted_mobile_number` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- 키워드에서 `Keywords_romania_eu_mobile_number` 를 찾을 수 있습니다. 
    
```
 
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_romania_eu_mobile_number"/>
          <Match idRef="Keywords_romania_eu_mobile_number" />
        </Pattern>
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_romania_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="slovakia"></a>슬로바키아

### <a name="pattern"></a>패턴

-  숫자 
    
### <a name="checksum"></a>체크섬

해당 없음
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 정규식 `Regex_slovakia_eu_mobile_number` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- 정규식 `Regex_slovakia_eu_formatted_mobile_number` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- 키워드에서 `Keywords_slovakia_eu_mobile_number` 를 찾을 수 있습니다. 
    
```
 
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_slovakia_eu_mobile_number"/>
          <Match idRef="Keywords_slovakia_eu_mobile_number" />
        </Pattern>
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_slovakia_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="slovenia"></a>슬로베니아

### <a name="pattern"></a>패턴

-  숫자 
    
### <a name="checksum"></a>체크섬

해당 없음
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 정규식 `Regex_slovenia_eu_mobile_number` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- 정규식 `Regex_slovenia_eu_formatted_mobile_number` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- 키워드에서 `Keywords_slovenia_eu_mobile_number` 를 찾을 수 있습니다. 
    
```
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_slovenia_eu_mobile_number"/>
          <Match idRef="Keywords_slovenia_eu_mobile_number" />
        </Pattern>
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_slovenia_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="spain"></a>스페인

### <a name="pattern"></a>패턴

-  숫자 
    
### <a name="checksum"></a>체크섬

해당 없음
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 정규식 `Regex_spain_eu_mobile_number` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- 정규식 `Regex_spain_eu_formatted_mobile_number` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- 키워드에서 `Keywords_spain_eu_mobile_number` 를 찾을 수 있습니다. 
    
```
 
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_spain_eu_mobile_number"/>
          <Match idRef="Keywords_spain_eu_mobile_number" />
        </Pattern>
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_spain_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="sweden"></a>스웨덴

### <a name="pattern"></a>패턴

-  숫자 
    
### <a name="checksum"></a>체크섬

해당 없음
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 정규식 `Regex_sweden_eu_mobile_number` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- 정규식 `Regex_sweden_eu_formatted_mobile_number` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- 키워드에서 `Keywords_sweden_eu_mobile_number` 를 찾을 수 있습니다. 
    
```
 
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_sweden_eu_mobile_number"/>
          <Match idRef="Keywords_sweden_eu_mobile_number" />
        </Pattern>
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_sweden_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="uk"></a>영국

### <a name="pattern"></a>패턴

-  숫자 
    
### <a name="checksum"></a>체크섬

해당 없음
  
### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
  
- 정규식 `Regex_uk_eu_mobile_number` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- 정규식 `Regex_uk_eu_formatted_mobile_number` 패턴과 일치 하는 콘텐츠를 찾습니다. 
    
- 키워드에서 `Keywords_uk_eu_mobile_number` 를 찾을 수 있습니다. 
    
```
 
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_uk_eu_mobile_number"/>
          <Match idRef="Keywords_uk_eu_mobile_number" />
        </Pattern>
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_uk_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="see-also"></a>참고 항목

[중요한 정보 형식이 찾는 항목](what-the-sensitive-information-types-look-for.md)

