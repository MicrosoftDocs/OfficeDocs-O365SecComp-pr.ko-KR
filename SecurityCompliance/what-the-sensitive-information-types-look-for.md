---
title: 중요 한 정보 형식을 찾습니다.
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 6/29/2018
ms.audience: Admin
search.appverid: MET150
ms.topic: reference
f1_keywords:
- ms.o365.cc.UnifiedDLPRuleContainsSensitiveInformation
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- M365-security-compliance
description: Office 365 보안 &amp; 및 준수 센터의 dlp (데이터 손실 방지)에는 dlp 정책에서 사용할 준비가 된 80 중요 한 정보 유형이 포함 되어 있습니다. 이 항목에서는 이러한 모든 중요한 정보 유형의 목록과 DLP 정책이 이러한 각 유형을 검색할 때 찾는 내용을 보여 줍니다.
ms.openlocfilehash: e9811b285e98a791570dc91e275cb5cead4f8bc9
ms.sourcegitcommit: 6e8e2b43a4bea31c1e835c5b050824651c6a0094
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/11/2019
ms.locfileid: "30537645"
---
# <a name="what-the-sensitive-information-types-look-for"></a>중요한 정보 형식이 찾는 항목

Office 365 보안 &amp; 및 준수 센터의 dlp (데이터 손실 방지)에는 dlp 정책에서 사용할 수 있는 중요 한 정보 유형이 많이 포함 되어 있습니다. 이 항목에서는 이러한 모든 중요한 정보 유형의 목록과 DLP 정책이 이러한 각 유형을 검색할 때 찾는 내용을 보여 줍니다. 중요한 정보 유형은 정규식이나 함수로 식별될 수 있는 패턴으로 정의됩니다. 또한 키워드 및 체크섬과 같은 확증적인 증거를 사용하여 중요한 정보 유형을 식별할 수 있습니다. 이러한 평가 프로세스에서 신뢰 수준 및 근접성도 사용됩니다.
  
## <a name="aba-routing-number"></a>ABA 라우팅 번호

### <a name="format"></a>형식일

서식 있는 패턴 또는 서식 없는 패턴으로 표시될 수 있는 9자리 숫자

### <a name="pattern"></a>패턴

서식이
- 0, 1, 2, 3, 6, 7 또는 8로 시작하는 4자리 숫자
- 하이픈
- 4자리 숫자
- 하이픈
- 1자리 숫자

서식 없음: 0, 1, 2, 3, 6, 7 또는 8로 시작 하는 9 개의 연속 숫자 

### <a name="checksum"></a>제외

아니요

### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
- Func_aba_routing 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.
- Keyword_ABA_Routing의 키워드가 발견되었습니다.

```
<!-- ABA Routing Number -->
<Entity id="cb353f78-2b72-4c3c-8827-92ebe4f69fdf" patternsProximity="300" recommendedConfidence="75">
      <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_aba_routing" />
        <Match idRef="Keyword_ABA_Routing" />
      </Pattern>
 </Entity>
```


### <a name="keywords"></a>키워드

#### <a name="keywordabarouting"></a>Keyword_ABA_Routing

- aba
- aba #
- aba routing #
- aba routing number
- aba
- abarouting #
- aba number
- abaroutingnumber
- american bank association routing #
- american bank association routing number
- americanbankassociationrouting #
- americanbankassociationroutingnumber
- bank routing number
- bankrouting #
- bankroutingnumber
- routing transit number
- rtn 
   
## <a name="argentina-national-identity-dni-number"></a>아르헨티나 국가 ID(DNI) 번호

### <a name="format"></a>형식일

마침표로 구분된 8자리 숫자

### <a name="pattern"></a>패턴

8자리 숫자:
- 2자리 숫자
- 마침표 
- 3자리 숫자
- 마침표 
- 3자리 숫자

### <a name="checksum"></a>제외

아니요

### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
- 정규식 Regex_argentina_national_id 해당 패턴과 일치 하는 콘텐츠를 찾습니다.
- Keyword_argentina_national_id에서 키워드가 발견 되었습니다.

```
<!-- Argentina National Identity (DNI) Number -->
<Entity id="eefbb00e-8282-433c-8620-8f1da3bffdb2" recommendedConfidence="75" patternsProximity="300">
   <Pattern confidenceLevel="75">
      <IdMatch idRef="Regex_argentina_national_id"/>
      <Match idRef="Keyword_argentina_national_id"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a>키워드

#### <a name="keywordargentinanationalid"></a>Keyword_argentina_national_id

- Argentina National Identity number 
- ID 
- 식별 국가 id 카드 
- DNI 
- 개인의 NIC 국내 레지스트리 
- Documento Nacional de Identidad 
- Registro Nacional de las Personas 
- Identidad 
- Identificación 
   
## <a name="australia-bank-account-number"></a>호주 은행 계좌 번호

### <a name="format"></a>형식일

6-10자리 숫자(은행 지점 번호 포함 또는 제외)

### <a name="pattern"></a>패턴

계좌 번호는 6-10자리 숫자입니다.
호주 은행 지점 번호:
- 3자리 숫자 
- 하이픈 
- 3자리 숫자

### <a name="checksum"></a>제외

아니요

### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.
- Regex_australia_bank_account_number 정규식이 해당 패턴과 일치하는 콘텐츠를 찾습니다.
- Keyword_australia_bank_account_number의 키워드가 발견되었습니다.
- Regex_australia_bank_account_number_bsb 정규식이 해당 패턴과 일치하는 콘텐츠를 찾습니다.

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
- Regex_australia_bank_account_number 정규식이 해당 패턴과 일치하는 콘텐츠를 찾습니다.
- Keyword_australia_bank_account_number의 키워드가 발견되었습니다.

```
<!-- Australia Bank Account Number -->
<Entity id="74a54de9-2a30-4aa0-a8aa-3d9327fc07c7" patternsProximity="300" recommendedConfidence="75">
  <Pattern confidenceLevel="85">
        <IdMatch idRef="Regex_australia_bank_account_number" />
        <Match idRef="Keyword_australia_bank_account_number" />
        <Match idRef="Regex_australia_bank_account_number_bsb" />
  </Pattern>
  <Pattern confidenceLevel="75">
        <IdMatch idRef="Regex_australia_bank_account_number" />
        <Match idRef="Keyword_australia_bank_account_number" />
  </Pattern>
 </Entity>
```

### <a name="keywords"></a>키워드

#### <a name="keywordaustraliabankaccountnumber"></a>Keyword_australia_bank_account_number

- swift bank code
- correspondent bank
- base currency
- usa account
- holder address
- bank address
- information account
- fund transfers
- bank charges
- bank details
- banking information
- full names
- iaea

   
## <a name="australia-drivers-license-number"></a>호주 운전 면허 번호

### <a name="format"></a>형식일

9개의 문자 및 숫자

### <a name="pattern"></a>패턴

9개의 문자 및 숫자: 

- 2자리 숫자 또는 문자(대/소문자 구분 안 함) 
- 2자리 숫자 
- 5자리 숫자 또는 문자(대/소문자 구분 안 함)

또는

- 1-2개의 선택적 문자(대/소문자 구분 안 함) 
- 4-9자리 숫자

또는

- 9자리 숫자 또는 문자(대/소문자 구분 안 함)

### <a name="checksum"></a>제외

아니요

### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
- Regex_australia_drivers_license_number 정규식이 해당 패턴과 일치하는 콘텐츠를 찾습니다.
- Keyword_australia_drivers_license_number의 키워드가 발견되었습니다.
- Keyword_australia_drivers_license_number_exclusions의 키워드가 발견되지 않았습니다.

```
<!-- Australia Drivers License Number -->
<Entity id="1cbbc8f5-9216-4392-9eb5-5ac2298d1356" patternsProximity="300" recommendedConfidence="75">
   <Pattern confidenceLevel="75">
        <IdMatch idRef="Regex_australia_drivers_license_number" />
        <Match idRef="Keyword_australia_drivers_license_number" />
        <Any minMatches="0" maxMatches="0">
          <Match idRef="Keyword_australia_drivers_license_number_exclusions" />
        </Any>
  </Pattern>
</Entity>
```

### <a name="keywords"></a>키워드

#### <a name="keywordaustraliadriverslicensenumber"></a>Keyword_australia_drivers_license_number

- international driving permits
- australian automobile association
- international driving permit
- driverlicence
- DriverLicences
- Driver Lic
- Driver Licence
- Driver Licences
- DriversLic
- 드라이버 라이선스
- DriversLicences
- Drivers Lic
- Drivers Lics
- Drivers Licence
- Drivers Licences
- driver' Lic
- driver'lics
- driver' 라이선스
- Driver'Licences
- Driver'Lic
- Driver' Lics
- Driver' Licence
- Driver'Licences
- Driver'sLic
- drivers (slics)
- Driver'sLicence
- Driver'sLicences
- Driver's Lic
- Driver's Lics
- Driver's Licence
- Driver's Licences
- driverlic #
- driverlics #
- driverlicence #
- DriverLicences #
- Driver Lic#
- Driver Lics#
- Driver Licence#
- Driver Licences#
- DriversLic #
- driverslics #
- 드라이버 라이선스 #
- DriversLicences #
- Drivers Lic#
- Drivers Lics#
- Drivers Licence#
- Drivers Licences#
- driver' Lic #
- driver'lics #
- driver' 라이선스 #
- Driver'Licences #
- Driver' Lic#
- Driver' Lics#
- Driver' Licence#
- Driver' Licences#
- Driver'sLic #
- drivers (slics #)
- Driver'sLicence #
- Driver'sLicences #
- Driver's Lic#
- Driver's Lics#
- Driver's Licence#
- Driver's Licences# 

#### <a name="keywordaustraliadriverslicensenumberexclusions"></a>Keyword_australia_drivers_license_number_exclusions

- aaa
- driverlicense
- driverlicenses
- Driver License
- Driver Licenses
- 드라이버 라이선스
- 드라이버 라이선스
- Drivers License
- Drivers Licenses
- driver' 라이선스
- driver'licenses
- Driver' License
- Driver' Licenses
- driver'slicense
- driver'slicenses
- Driver's License
- Driver's Licenses
- driverlicense #
- driverlicenses #
- Driver License#
- Driver Licenses#
- 드라이버 라이선스 #
- 드라이버 라이선스 수
- Drivers License#
- Drivers Licenses#
- driver' 라이선스 #
- driver'licenses #
- Driver' License#
- Driver' Licenses#
- driver'slicense #
- driver'slicenses #
- Driver's License#
- Driver's Licenses#
   
## <a name="australia-medical-account-number"></a>호주 의료 계좌 번호

### <a name="format"></a>형식일

10-11자리 숫자

### <a name="pattern"></a>패턴

10-11자리 숫자:
- 첫 번째 숫자는 2-6 범위에 있습니다.
- 9번째 숫자는 검사 숫자입니다.
- 10번째 숫자는 문제 숫자입니다.
- 11번째 숫자(선택 사항)는 개인 번호입니다.

### <a name="checksum"></a>제외

예

### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 95% 신뢰합니다.
- Func_australian_medical_account_number 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.
- Keyword_Australia_Medical_Account_Number의 키워드가 발견되었습니다.
- 체크섬이 통과됩니다.

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.
- Func_australian_medical_account_number 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.
- 체크섬이 통과됩니다.

```
  <!-- Australia Medical Account Number -->
<Entity id="104a99a0-3d3b-4542-a40d-ab0b9e1efe63" recommendedConfidence="85" patternsProximity="300">
    <Pattern confidenceLevel="95">
     <IdMatch idRef="Func_australian_medical_account_number"/>
     <Any minMatches="1">
     <Match idRef="Keyword_Australia_Medical_Account_Number"/>
     </Any>
  </Pattern>
<Pattern confidenceLevel="85">
     <IdMatch idRef="Func_australian_medical_account_number"/>
     <Any minMatches="0" maxMatches="0">
  <Match idRef="Keyword_Australia_Medical_Account_Number"/>
     </Any>
  </Pattern>
</Entity>
```

### <a name="keywords"></a>키워드

#### <a name="keywordaustraliamedicalaccountnumber"></a>Keyword_Australia_Medical_Account_Number

- bank account details
- medicare payments
- mortgage account
- bank payments
- information branch
- credit card loan
- department of human services
- local service
- medicare

   
## <a name="australia-passport-number"></a>호주 여권 번호

### <a name="format"></a>형식일

문자와 7자리 숫자

### <a name="pattern"></a>패턴

1개의 문자(대/소문자 구분 안 함)와 7자리 숫자

### <a name="checksum"></a>제외

아니요

### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
- Regex_australia_passport_number 정규식이 해당 패턴과 일치하는 콘텐츠를 찾습니다.
- Keyword_passport 또는 Keyword_australia_passport_number의 키워드를 찾았습니다.

```
<!-- Australia Passport Number -->
<Entity id="29869db6-602d-4853-ab93-3484f905df50" patternsProximity="300" recommendedConfidence="75">
  <Pattern confidenceLevel="75">
        <IdMatch idRef="Regex_australia_passport_number" />
        <Any minMatches="1">
          <Match idRef="Keyword_passport" />
          <Match idRef="Keyword_australia_passport_number" />
        </Any>
   </Pattern>
</Entity>   
```

### <a name="keywords"></a>키워드

#### <a name="keywordpassport"></a>Keyword_passport

- Passport Number
- Passport No
- Passport #
- 여권
- PassportID
- Passportno
- passportnumber
- パスポート
- パスポート番号
- パスポートのNum
- パスポート ＃ 
- Numéro de passeport
- Passeport n °
- Passeport Non
- Passeport #
- 포트 #
- 지/포트 아님
- Passeportn °

#### <a name="keywordaustraliapassportnumber"></a>Keyword_australia_passport_number

- 여권
- passport details
- immigration and citizenship
- commonwealth of australia
- department of immigration
- residential address
- department of immigration and citizenship
- visa
- national identity card
- passport number
- travel document
- issuing authority
   
## <a name="australia-tax-file-number"></a>호주 세금 파일 번호

### <a name="format"></a>형식일

8-9자리 숫자

### <a name="pattern"></a>패턴

일반적으로 다음과 같이 공백과 함께 표시되는 8-9자리 숫자:
- 3자리 숫자 
- 선택적 공백 1개 
- 3자리 숫자 
- 선택적 공백 1개 
- 마지막 숫자가 검사 숫자인 2-3자리 숫자

### <a name="checksum"></a>제외

예

### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.
- Func_australian_tax_file_number 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.
- Keyword_Australia_Tax_File_Number 또는 Keyword_number_exclusions의 키워드가 발견되지 않았습니다.
- 체크섬이 통과됩니다.

```
    <!-- Australia Tax File Number -->
<Entity id="e29bc95f-ff70-4a37-aa01-04d17360a4c5" patternsProximity="300" recommendedConfidence="85">
    
  <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_australian_tax_file_number" />
        <Any minMatches="0" maxMatches="0">
          <Match idRef="Keyword_Australia_Tax_File_Number" />
          <Match idRef="Keyword_number_exclusions" />
        </Any>
  </Pattern>
</Entity>
```

### <a name="keywords"></a>키워드

#### <a name="keywordaustraliataxfilenumber"></a>Keyword_Australia_Tax_File_Number

- australian business number
- marginal tax rate
- medicare levy
- portfolio number
- service veterans
- withholding tax
- individual tax return
- tax file number

#### <a name="keywordnumberexclusions"></a>Keyword_number_exclusions

- 00000000
- 11111111
- 22222222
- 33333333
- 44444444
- 55555555
- 66666666
- 77777777
- 88888888
- 99999999
- 000000000
- 111111111
- 222222222
- 333333333
- 444444444
- 555555555
- 666666666
- 777777777
- 888888888
- 999999999
- 0000000000
- 1111111111
- 2222222222
- 3333333333
- 4444444444
- 5555555555
- 6666666666
- 7777777777
- 8888888888
- 9999999999

## <a name="azure-documentdb-auth-key"></a>Azure DocumentDB 인증 키

### <a name="format"></a>형식일

아래 패턴에 설명 된 문자 및 문자열이 뒤에 오는 "DocumentDb" 문자열

### <a name="pattern"></a>패턴

- "DocumentDb" 문자열
- 3-200에서 대/소문자, 숫자, 기호, 특수 문자 또는 공백 사이의 조합
- 보다 큼 기호 (>), 등호 (=), 따옴표 (") 또는 아포스트로피 (')
- 86의 대/소문자, 숫자, 슬래시 (/) 또는 더하기 기호 (+)의 조합
- 두 개의 등호 (=)

### <a name="checksum"></a>제외

아니요

### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.
- 정규식 CEP_Regex_AzureDocumentDBAuthKey 해당 패턴과 일치 하는 콘텐츠를 찾습니다.
- CEP_CommonExampleKeywords 정규식이 해당 패턴과 **** 일치 하는 콘텐츠를 찾지 않습니다.

```
<!-- Azure Document DB Auth Key -->
<Entity id="0f587d92-eb28-44a9-bd1c-90f2892b47aa" patternsProximity="300" recommendedConfidence="85">
  <Pattern confidenceLevel="85">
        <IdMatch idRef="CEP_Regex_AzureDocumentDBAuthKey" />
        <Any minMatches="0" maxMatches="0">
            <Match idRef="CEP_CommonExampleKeywords" />
          </Any>
  </Pattern>
</Entity>
```

### <a name="keywords"></a>키워드

#### <a name="cepcommonexamplekeywords"></a>CEP_CommonExampleKeywords

기술적으로이 중요 한 정보 유형은 키워드 목록이 아니라 정규식을 사용 하 여 이러한 키워드를 식별 합니다.

- 극동
- fabrikam
- 대양
- 샌드박스
- 용 onebox
- 로컬
- 127.0.0.1
- testacs입니다. <!--no-hyperlink-->com
- s-int<!--no-hyperlink-->

## <a name="azure-iaas-database-connection-string-and-azure-sql-connection-string"></a>azure IAAS 데이터베이스 연결 문자열 및 azure SQL 연결 문자열

### <a name="format"></a>형식일

"server", "server" 또는 "data source" 라는 문자열은 "cloudapp. azure"를 포함 하 여 아래 패턴에 설명 된 문자 및 문자열을 따릅니다. <!--no-hyperlink-->com "또는" cloudapp. <!--no-hyperlink-->net "또는" 데이터베이스. <!--no-hyperlink-->net "과 문자열" password "또는" password "또는" pwd "가 있습니다.

### <a name="pattern"></a>패턴

- 문자열 "server", "Server" 또는 "data source"
- 0-2 공백 문자
- 등호 (=)
- 0-2 공백 문자
- 1-200에서 대/소문자, 숫자, 기호, 특수 문자 또는 공백 사이의 조합
- 문자열 "cloudapp. <!--no-hyperlink-->com "," cloudapp. <!--no-hyperlink-->net "또는" database. <!--no-hyperlink-->net "
- 1-300에서 대/소문자, 숫자, 기호, 특수 문자 또는 공백 사이의 조합
- 문자열 "password", "password" 또는 "pwd"
- 0-2 공백 문자
- 등호 (=)
- 0-2 공백 문자
- 세미콜론 (;), 따옴표 (") 또는 아포스트로피 (')가 아닌 하나 이상의 문자
- 세미콜론 (;), 따옴표 (") 또는 아포스트로피 (')

### <a name="checksum"></a>제외

아니요

### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.
- 정규식 CEP_Regex_AzureConnectionString 해당 패턴과 일치 하는 콘텐츠를 찾습니다.
- CEP_CommonExampleKeywords 정규식이 해당 패턴과 **** 일치 하는 콘텐츠를 찾지 않습니다.

```
<!--Azure IAAS Database Connection String and Azure SQL Connection String-->
<Entity id="ce1a126d-186f-4700-8c0c-486157b953fd" patternsProximity="300" recommendedConfidence="85">
  <Pattern confidenceLevel="85">
        <IdMatch idRef="CEP_Regex_AzureConnectionString" />
        <Any minMatches="0" maxMatches="0">
            <Match idRef="CEP_CommonExampleKeywords" />
        </Any>
    </Pattern>
</Entity>
```

### <a name="keywords"></a>키워드

#### <a name="cepcommonexamplekeywords"></a>CEP_CommonExampleKeywords

기술적으로이 중요 한 정보 유형은 키워드 목록이 아니라 정규식을 사용 하 여 이러한 키워드를 식별 합니다.

- 극동
- fabrikam
- 대양
- 샌드박스
- 용 onebox
- 로컬
- 127.0.0.1
- testacs입니다. <!--no-hyperlink-->com
- s-int<!--no-hyperlink-->

## <a name="azure-iot-connection-string"></a>Azure IoT Connection 문자열

### <a name="format"></a>형식일

문자열 "HostName" 뒤에 "azure-devices" 라는 문자열을 포함 하 여 아래 패턴에 설명 된 문자 및 문자열이 표시 됩니다. <!--no-hyperlink-->net "및" sharedaccesskey "

### <a name="pattern"></a>패턴

- 문자열 "HostName"
- 0-2 공백 문자
- 등호 (=)
- 0-2 공백 문자
- 1-200에서 대/소문자, 숫자, 기호, 특수 문자 또는 공백 사이의 조합
- 문자열 "azure-장치 <!--no-hyperlink-->net "
- 1-200에서 대/소문자, 숫자, 기호, 특수 문자 또는 공백 사이의 조합
- "sharedaccesskey" 문자열
- 0-2 공백 문자
- 등호 (=)
- 0-2 공백 문자
- 43의 대/소문자, 숫자, 슬래시 (/) 또는 더하기 기호 (+)의 조합
- 등호 (=)

### <a name="checksum"></a>제외

아니요

### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.
- 정규식 CEP_Regex_AzureIoTConnectionString 해당 패턴과 일치 하는 콘텐츠를 찾습니다.
- CEP_CommonExampleKeywords 정규식이 해당 패턴과 **** 일치 하는 콘텐츠를 찾지 않습니다.

```
<!--Azure IoT Connection String-->
<Entity id="0b34bec3-d5d6-4974-b7b0-dcdb5c90c29d" patternsProximity="300" recommendedConfidence="85">
  <Pattern confidenceLevel="85">
        <IdMatch idRef="CEP_Regex_AzureIoTConnectionString" />
        <Any minMatches="0" maxMatches="0">
            <Match idRef="CEP_CommonExampleKeywords" />
        </Any>
  </Pattern>
</Entity>
```

### <a name="keywords"></a>키워드

#### <a name="cepcommonexamplekeywords"></a>CEP_CommonExampleKeywords

기술적으로이 중요 한 정보 유형은 키워드 목록이 아니라 정규식을 사용 하 여 이러한 키워드를 식별 합니다.

- 극동
- fabrikam
- 대양
- 샌드박스
- 용 onebox
- 로컬
- 127.0.0.1
- testacs입니다. <!--no-hyperlink-->com
- s-int<!--no-hyperlink-->

## <a name="azure-publish-setting-password"></a>Azure 게시 설정 암호

### <a name="format"></a>형식일

문자열 "userpwd =" 다음에 영숫자 문자열이 나옵니다.

### <a name="pattern"></a>패턴

- 문자열 "userpwd ="
- 60 대 문자와 숫자의 조합
- 큰따옴표 (")

### <a name="checksum"></a>제외

아니요

### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.
- 정규식 CEP_Regex_AzurePublishSettingPasswords 해당 패턴과 일치 하는 콘텐츠를 찾습니다.
- CEP_CommonExampleKeywords 정규식이 해당 패턴과 **** 일치 하는 콘텐츠를 찾지 않습니다.


```
<!--Azure Publish Setting Password-->
<Entity id="75f4cc8a-a68e-49e5-89ce-fa8f03d286a5" patternsProximity="300" recommendedConfidence="85">
  <Pattern confidenceLevel="85">
       <IdMatch idRef="CEP_Regex_AzurePublishSettingPasswords" />
       <Any minMatches="0" maxMatches="0">
           <Match idRef="CEP_CommonExampleKeywords" />
       </Any>
  </Pattern>
</Entity>
```

### <a name="keywords"></a>키워드

#### <a name="cepcommonexamplekeywords"></a>CEP_CommonExampleKeywords

기술적으로이 중요 한 정보 유형은 키워드 목록이 아니라 정규식을 사용 하 여 이러한 키워드를 식별 합니다.

- 극동
- fabrikam
- 대양
- 샌드박스
- 용 onebox
- 로컬
- 127.0.0.1
- testacs입니다. <!--no-hyperlink-->com
- s-int<!--no-hyperlink-->

## <a name="azure-redis-cache-connection-string"></a>Azure Redis 캐시 연결 문자열

### <a name="format"></a>형식일

문자열 "redis. <!--no-hyperlink-->net "문자열" password "또는" pwd "를 포함 하 여 아래 패턴에 설명 된 문자 및 문자열을 입력 합니다.

### <a name="pattern"></a>패턴

- 문자열 "redis. <!--no-hyperlink-->net "
- 1-200에서 대/소문자, 숫자, 기호, 특수 문자 또는 공백 사이의 조합
- 문자열 "password" 또는 "pwd"
- 0-2 공백 문자
- 등호 (=)
- 0-2 공백 문자
- 대/소문자, 숫자, 슬래시 (/) 또는 더하기 기호 (+)가 있는 43 문자의 조합
- 등호 (=)

### <a name="checksum"></a>제외

아니요

### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.
- 정규식 CEP_Regex_AzureRedisCacheConnectionString가 해당 패턴과 일치 하는 콘텐츠를 찾습니다.
- CEP_CommonExampleKeywords 정규식이 해당 패턴과 **** 일치 하는 콘텐츠를 찾지 않습니다.

```
<!--Azure Redis Cache Connection String-->
<Entity id="095a7e6c-efd8-46d5-af7b-5298d53a49fc" patternsProximity="300" recommendedConfidence="85">
  <Pattern confidenceLevel="85">
        <IdMatch idRef="CEP_Regex_AzureRedisCacheConnectionString" />
        <Any minMatches="0" maxMatches="0">
            <Match idRef="CEP_CommonExampleKeywords" />
        </Any>
  </Pattern>
</Entity>
```

### <a name="keywords"></a>키워드

#### <a name="cepcommonexamplekeywords"></a>CEP_CommonExampleKeywords

기술적으로이 중요 한 정보 유형은 키워드 목록이 아니라 정규식을 사용 하 여 이러한 키워드를 식별 합니다.

- 극동
- fabrikam
- 대양
- 샌드박스
- 용 onebox
- 로컬
- 127.0.0.1
- testacs입니다. <!--no-hyperlink-->com
- s-int<!--no-hyperlink-->

## <a name="azure-sas"></a>Azure SAS

### <a name="format"></a>형식일

아래 패턴에 설명 된 문자 및 문자열이 뒤에 오는 문자열 "sig"

### <a name="pattern"></a>패턴

- 문자열 "sig"
- 0-2 공백 문자
- 등호 (=)
- 0-2 공백 문자
- 대/소문자, 숫자 또는 백분율 기호 (%)가 43-53 자 사이의 조합입니다.
- 문자열 "% 3d"
- 소문자 또는 대문자, 숫자 또는 백분율 기호 (%)가 아닌 모든 문자

### <a name="checksum"></a>제외

아니요

### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.
- 정규식 CEP_Regex_AzureSAS 해당 패턴과 일치 하는 콘텐츠를 찾습니다.

```
<!--Azure SAS-->
<Entity id="4d235014-e564-47f4-a6fb-6ebb4a826834" patternsProximity="300" recommendedConfidence="85">
  <Pattern confidenceLevel="85">
        <IdMatch idRef="CEP_Regex_AzureSAS" />
  </Pattern>
</Entity>
```

## <a name="azure-service-bus-connection-string"></a>Azure Service Bus 연결 문자열

### <a name="format"></a>형식일

문자열 "끝점" 뒤에 "servicebus" 라는 문자열을 포함 하 여 아래 패턴에 나와 있는 문자 및 문자열이 표시 됩니다. <!--no-hyperlink-->net "및" SharedAccesKey "을 차례로 누릅니다.

### <a name="pattern"></a>패턴

- 문자열 "끝점"
- 0-2 공백 문자
- 등호 (=)
- 0-2 공백 문자
- 1-200에서 대/소문자, 숫자, 기호, 특수 문자 또는 공백 사이의 조합
- 문자열 "servicebus. <!--no-hyperlink-->net "
- 1-200에서 대/소문자, 숫자, 기호, 특수 문자 또는 공백 사이의 조합
- "sharedaccesskey" 문자열
- 0-2 공백 문자
- 등호 (=)
- 0-2 공백 문자
- 대/소문자, 숫자, 슬래시 (/) 또는 더하기 기호 (+)가 있는 43 문자의 조합
- 등호 (=)

### <a name="checksum"></a>제외

아니요

### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.
- 정규식 CEP_Regex_AzureServiceBusConnectionString가 해당 패턴과 일치 하는 콘텐츠를 찾습니다.
- CEP_CommonExampleKeywords 정규식이 해당 패턴과 **** 일치 하는 콘텐츠를 찾지 않습니다.

```
<!--Azure Service Bus Connection String-->
<Entity id="b9a6578f-a83f-4fcd-bf44-2130bae49a6f" patternsProximity="300" recommendedConfidence="85">
  <Pattern confidenceLevel="85">
        <IdMatch idRef="CEP_Regex_AzureServiceBusConnectionString" />
        <Any minMatches="0" maxMatches="0">
            <Match idRef="CEP_CommonExampleKeywords" />
        </Any>
  </Pattern>
</Entity>
```

### <a name="keywords"></a>키워드

#### <a name="cepcommonexamplekeywords"></a>CEP_CommonExampleKeywords

기술적으로이 중요 한 정보 유형은 키워드 목록이 아니라 정규식을 사용 하 여 이러한 키워드를 식별 합니다.

- 극동
- fabrikam
- 대양
- 샌드박스
- 용 onebox
- 로컬
- 127.0.0.1
- testacs입니다. <!--no-hyperlink-->com
- s-int<!--no-hyperlink-->

## <a name="azure-storage-account-key"></a>Azure 저장소 계정 키

### <a name="format"></a>형식일

"defaultendpointsprotocol" 문자열은 "AccountKey" 문자열을 포함 하 여 아래 패턴에 설명 된 문자 및 문자열을 따릅니다.

### <a name="pattern"></a>패턴

- 문자열 "defaultendpointsprotocol"
- 0-2 공백 문자
- 등호 (=)
- 0-2 공백 문자
- 1-200에서 대/소문자, 숫자, 기호, 특수 문자 또는 공백 사이의 조합
- 문자열 "AccountKey"
- 0-2 공백 문자
- 등호 (=)
- 0-2 공백 문자
- 대/소문자, 숫자, 슬래시 (/) 또는 더하기 기호 (+)가 있는 86 문자의 조합
- 두 개의 등호 (=)

### <a name="checksum"></a>제외

아니요

### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.
- 정규식 CEP_Regex_AzureStorageAccountKey 해당 패턴과 일치 하는 콘텐츠를 찾습니다.
- CEP_AzureEmulatorStorageAccountFilter 정규식이 해당 패턴과 **** 일치 하는 콘텐츠를 찾지 않습니다.
- CEP_CommonExampleKeywords 정규식이 해당 패턴과 **** 일치 하는 콘텐츠를 찾지 않습니다.

```
<!--Azure Storage Account Key-->
<Entity id="c7bc98e8-551a-4c35-a92d-d2c8cda714a7" patternsProximity="300" recommendedConfidence="85">
  <Pattern confidenceLevel="85">
        <IdMatch idRef="CEP_Regex_AzureStorageAccountKey" />
        <Any minMatches="0" maxMatches="0">
            <Match idRef="CEP_AzureEmulatorStorageAccountFilter" />
            <Match idRef="CEP_CommonExampleKeywords" />
        </Any>
  </Pattern>
</Entity>
```

### <a name="keywords"></a>키워드

#### <a name="cepazureemulatorstorageaccountfilter"></a>CEP_AzureEmulatorStorageAccountFilter

기술적으로이 중요 한 정보 유형은 키워드 목록이 아니라 정규식을 사용 하 여 이러한 키워드를 식별 합니다.

- Eby8vdM02xNOcqFlqUwJPLlmEtlCDXJ1OUzFT50uSRZ6IFsuFq2UVErCz4I6tq/K1SZFPTOtr/KBHBeksoGMGw = =

#### <a name="cepcommonexamplekeywords"></a>CEP_CommonExampleKeywords

기술적으로이 중요 한 정보 유형은 키워드 목록이 아니라 정규식을 사용 하 여 이러한 키워드를 식별 합니다.

- 극동
- fabrikam
- 대양
- 샌드박스
- 용 onebox
- 로컬
- 127.0.0.1
- testacs입니다. <!--no-hyperlink-->com
- s-int<!--no-hyperlink-->

## <a name="azure-storage-account-key-generic"></a>Azure 저장소 계정 키 (일반)

### <a name="format"></a>형식일

아래 패턴에 윤곽선이 있는 문자 앞 이나 뒤에 오는 86 문자의 대/소문자, 숫자, 슬래시 (/) 또는 더하기 기호 (+)의 조합입니다.

### <a name="pattern"></a>패턴

- > (보다 큼 기호), 아포스트로피 ('), 등호 (=), 따옴표 (") 또는 숫자 기호 (#)
- 대/소문자, 숫자, 슬래시 (/) 또는 더하기 기호 (+)가 있는 86 문자의 조합
- 두 개의 등호 (=)


### <a name="checksum"></a>제외

아니요

### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.
- 정규식 CEP_Regex_AzureStorageAccountKeyGeneric 해당 패턴과 일치 하는 콘텐츠를 찾습니다.

```
<!--Azure Storage Account Key (Generic)-->
<Entity id="7ff41bd0-5419-4523-91d6-383b3a37f084" patternsProximity="300" recommendedConfidence="85">
  <Pattern confidenceLevel="85">
        <IdMatch idRef="CEP_Regex_AzureStorageAccountKeyGeneric" />
  </Pattern>
</Entity>
```

## <a name="belgium-national-number"></a>벨기에 국가 번호

### <a name="format"></a>형식일

11자리 숫자와 구분 기호

### <a name="pattern"></a>패턴

11자리 숫자와 구분 기호:
- 생년월일을 나타내는 YY.MM.DD 형식의 6자리 숫자와 마침표 2개  
- 하이픈 
- 세 개의 순차적 숫자(남성의 경우 홀수, 여성의 경우 짝수)  
- 마침표 
- 검사 숫자에 해당하는 두 자리 숫자

### <a name="checksum"></a>제외

예

### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
- Func_belgium_national_number 함수가 해당 패턴과 일치 하는 콘텐츠를 찾습니다.
- Keyword_belgium_national_number에서 키워드가 발견 되었습니다.
- 체크섬이 통과됩니다.

```
<!-- Belgium National Number -->
  <Entity id="fb969c9e-0fd1-4b18-8091-a2123c5e6a54" recommendedConfidence="75" patternsProximity="300">
   <Pattern confidenceLevel="75">
     <IdMatch idRef="Func_belgium_national_number"/>
     <Match idRef="Keyword_belgium_national_number"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a>키워드

#### <a name="keywordbelgiumnationalnumber"></a>Keyword_belgium_national_number

- ID
- 등록
- 확인과 
- ID 
- Identiteitskaart
- Registratie nummer 
- Identificatie nummer 
- Identiteit
- Registratie
- Identificatie 
- Carte d’identité 
- numéro d'immatriculation
- numéro d'identification
- identité 
- inscription 
- Identifikation
- Identifizierung
- Identifikationsnummer
- Personalausweis
- Registrierung
- Registrationsnummer

   
## <a name="brazil-cpf-number"></a>브라질 CPF 번호

### <a name="format"></a>형식일

서식이 있거나 서식이 없을 수 있는 검사 숫자를 포함하는 11자리 숫자

### <a name="pattern"></a>패턴

서식이
- 3자리 숫자 
- 마침표  
- 3자리 숫자 
- 마침표  
- 3자리 숫자 
- 하이픈 
- 검사 숫자에 해당하는 2자리 숫자

서식
- 마지막 2자리 숫자가 검사 숫자인 11자리 숫자

### <a name="checksum"></a>제외

예

### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.
- Func_brazil_cpf 함수가 해당 패턴과 일치 하는 콘텐츠를 찾습니다.
- Keyword_brazil_cpf에서 키워드가 발견 되었습니다.
- 체크섬이 통과됩니다.

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
- Func_brazil_cpf 함수가 해당 패턴과 일치 하는 콘텐츠를 찾습니다.
- 체크섬이 통과됩니다.

```
<!-- Brazil CPF Number -->
<Entity id="78e09124-f2c3-4656-b32a-c1a132cd2711" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Func_brazil_cpf"/>
     <Match idRef="Keyword_brazil_cpf"/>
  </Pattern>
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Func_brazil_cpf"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a>키워드

#### <a name="keywordbrazilcpf"></a>Keyword_brazil_cpf

- CPF
- 확인과
- 등록
- 별
- Cadastro de Pessoas Físicas 
- Imposto 
- Identificação 
- Inscrição 
- 고 eita 
   
## <a name="brazil-legal-entity-number-cnpj"></a>브라질 법인 번호(CNPJ)

### <a name="format"></a>형식일

등록 번호, 지점 번호, 검사 숫자 및 구분 기호를 포함하는 14자리 숫자

### <a name="pattern"></a>패턴
14자리 숫자와 구분 기호:
- 2자리 숫자 
- 마침표  
- 3자리 숫자 
- 마침표  
- 3자리 숫자(처음 8자리 숫자는 등록 번호임)  
- 정방향 슬래시 
- 4자리 지점 번호  
- 하이픈 
- 검사 숫자에 해당하는 2자리 숫자

### <a name="checksum"></a>제외

예

### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.
- Func_brazil_cnpj 함수가 해당 패턴과 일치 하는 콘텐츠를 찾습니다.
- Keyword_brazil_cnpj에서 키워드가 발견 되었습니다.
- 체크섬이 통과됩니다.

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
- Func_brazil_cnpj 함수가 해당 패턴과 일치 하는 콘텐츠를 찾습니다.
- 체크섬이 통과됩니다.

```
<!-- Brazil Legal Entity Number (CNPJ) -->
<Entity id="9b58b5cd-5e90-4df6-b34f-1ebcc88ceae4" recommendedConfidence="85" patternsProximity="300">
   <Pattern confidenceLevel="85">
     <IdMatch idRef="Func_brazil_cnpj"/>
     <Match idRef="Keyword_brazil_cnpj"/>
  </Pattern>
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Func_brazil_cnpj"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a>키워드

#### <a name="keywordbrazilcnpj"></a>Keyword_brazil_cnpj

- CNPJ 
- CNPJ/MF 
- CNPJ-MF 
- National Registry of Legal Entities 
- Taxpayers Registry 
- Legal entity 
- Legal entities 
- Registration Status 
- 비즈니스 
- Company
- CNPJ 
- Cadastro Nacional da Pessoa Jurídica 
- Cadastro Geral de Contribuintes 
- cgc 
- Pessoa jurídica 
- Pessoas jurídicas 
- Situação cadastral 
- Inscrição 
- 포털 
   
## <a name="brazil-national-id-card-rg"></a>	브라질 국가 ID 카드(RG)

### <a name="format"></a>형식일

Registro Geral (이전 형식): 9 자리 숫자

Registro de Identidade (RIC) (새 형식): 11 자리 숫자

### <a name="pattern"></a>패턴

Registro Geral(이전 형식):
- 2자리 숫자 
- 마침표  
- 3자리 숫자 
- 마침표  
- 3자리 숫자 
- 하이픈 
- 검사 숫자에 해당하는 1자리 숫자

Registro de Identidade (RIC) (새 형식):
- 10자리 숫자 
- 하이픈 
- 검사 숫자에 해당하는 1자리 숫자

### <a name="checksum"></a>제외

예

### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.
- Func_brazil_rg 함수가 해당 패턴과 일치 하는 콘텐츠를 찾습니다.
- Keyword_brazil_rg에서 키워드가 발견 되었습니다.
- 체크섬이 통과됩니다.

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
- Func_brazil_rg 함수가 해당 패턴과 일치 하는 콘텐츠를 찾습니다.
- 체크섬이 통과됩니다.

```
<!-- Brazil National ID Card (RG) -->
<Entity id="486de900-db70-41b3-a886-abdf25af119c" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Func_brazil_rg"/>
     <Match idRef="Keyword_brazil_rg"/>
  </Pattern>
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Func_brazil_rg"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a>키워드

#### <a name="keywordbrazilrg"></a>Keyword_brazil_rg

Cédula de identidade identity card 국립 id número de rregistro registro de Iidentidade registro geral RG (이 키워드는 대/소문자를 구분 함) RIC (이 키워드는 대/소문자를 구분 함) 
   
## <a name="canada-bank-account-number"></a>캐나다 은행 계좌 번호

### <a name="format"></a>형식일

7 또는 12자리 숫자

### <a name="pattern"></a>패턴

캐나다 은행 계좌 번호는 7 또는 12자리 숫자입니다.

캐나다 은행 계좌 송금 번호:
- 5자리 숫자 
- 하이픈 
- 3 자리 숫자 또는
- "0" 
- 8자리 숫자

### <a name="checksum"></a>제외

아니요

### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.
- Regex_canada_bank_account_number 정규식이 해당 패턴과 일치하는 콘텐츠를 찾습니다.
- Keyword_canada_bank_account_number의 키워드가 발견되었습니다.
- Regex_canada_bank_account_transit_number 정규식이 해당 패턴과 일치하는 콘텐츠를 찾습니다.

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.
- Regex_canada_bank_account_number 정규식이 해당 패턴과 일치하는 콘텐츠를 찾습니다.
- Keyword_canada_bank_account_number의 키워드가 발견되었습니다.

```
<!-- Canada Bank Account Number -->
<Entity id="552e814c-cb50-4d94-bbaa-bb1d1ffb34de" patternsProximity="300" recommendedConfidence="75">
  <Pattern confidenceLevel="85">
        <IdMatch idRef="Regex_canada_bank_account_number" />
        <Match idRef="Keyword_canada_bank_account_number" />
        <Match idRef="Regex_canada_bank_account_transit_number" />
   </Pattern>
   <Pattern confidenceLevel="75">
        <IdMatch idRef="Regex_canada_bank_account_number" />
        <Match idRef="Keyword_canada_bank_account_number" />
   </Pattern>
</Entity>
```

### <a name="keywords"></a>키워드

#### <a name="keywordcanadabankaccountnumber"></a>Keyword_canada_bank_account_number

- canada savings bonds
- canada revenue agency
- canadian financial institution
- direct deposit form
- canadian citizen
- legal representative
- notary public
- commissioner for oaths
- child care benefit
- universal child care
- canada child tax benefit
- income tax benefit
- harmonized sales tax
- social insurance number
- income tax refund
- child tax benefit
- territorial payments
- institution number
- deposit request
- banking information
- direct deposit
   
## <a name="canada-drivers-license-number"></a>캐나다 운전 면허 번호

### <a name="format"></a>형식일

지역마다 다름

### <a name="pattern"></a>패턴

앨버타, 브리티시 콜롬비아, 매니토바, 뉴브런즈윅, 뉴펀들랜드/래브라도, 노바스코샤, 온타리오, 프린스에드워드아일랜드, 퀘벡 및 서스캐처원을 포함하는 다양한 패턴

### <a name="checksum"></a>제외

아니요

### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
- Func_[province_name]_drivers_license_number 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.
- Keyword_[province_name]_drivers_license_name의 키워드가 발견되었습니다.
- Keyword_canada_drivers_license의 키워드가 발견되었습니다.

```
<!-- Canada Driver's License Number -->
    <Entity id="37186abb-8e48-4800-ad3c-e3d1610b3db0" patternsProximity="300" recommendedConfidence="75">
      <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_alberta_drivers_license_number" />
        <Match idRef="Keyword_alberta_drivers_license_name" />
        <Match idRef="Keyword_canada_drivers_license" />
      </Pattern>
      <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_british_columbia_drivers_license_number" />
        <Match idRef="Keyword_british_columbia_drivers_license_name" />
        <Match idRef="Keyword_canada_drivers_license" />
      </Pattern>
      <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_manitoba_drivers_license_number" />
        <Match idRef="Keyword_manitoba_drivers_license_name" />
        <Match idRef="Keyword_canada_drivers_license" />
      </Pattern>
      <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_new_brunswick_drivers_license_number" />
        <Match idRef="Keyword_new_brunswick_drivers_license_name" />
        <Match idRef="Keyword_canada_drivers_license" />
      </Pattern>
      <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_newfoundland_labrador_drivers_license_number" />
        <Match idRef="Keyword_newfoundland_labrador_drivers_license_name" />
        <Match idRef="Keyword_canada_drivers_license" />
      </Pattern>
      <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_nova_scotia_drivers_license_number" />
        <Match idRef="Keyword_nova_scotia_drivers_license_name" />
        <Match idRef="Keyword_canada_drivers_license" />
      </Pattern>
      <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_ontario_drivers_license_number" />
        <Match idRef="Keyword_ontario_drivers_license_name" />
        <Match idRef="Keyword_canada_drivers_license" />
      </Pattern>
      <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_prince_edward_island_drivers_license_number" />
        <Match idRef="Keyword_prince_edward_island_drivers_license_name" />
        <Match idRef="Keyword_canada_drivers_license" />
      </Pattern>
      <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_quebec_drivers_license_number" />
        <Match idRef="Keyword_quebec_drivers_license_name" />
        <Match idRef="Keyword_canada_drivers_license" />
      </Pattern>
      <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_saskatchewan_drivers_license_number" />
        <Match idRef="Keyword_saskatchewan_drivers_license_name" />
        <Match idRef="Keyword_canada_drivers_license" />
      </Pattern>
    </Entity>
```

### <a name="keywords"></a>키워드

#### <a name="keywordprovincenamedriverslicensename"></a>Keyword_ [province_name] _drivers_license_name

- 시/도 약어(예: AB)
- 시/도 이름(예: 앨버타)

#### <a name="keywordcanadadriverslicense"></a>Keyword_canada_drivers_license

- DL
- 된다
- cdl
- cdls
- driverlic
- driverlics
- driverlicense
- driverlicenses
- driverlicence
- DriverLicences
- Driver Lic
- Driver Lics
- Driver License
- Driver Licenses
- Driver Licence
- Driver Licences
- DriversLic
- driverslics
- 드라이버 라이선스
- DriversLicences
- 드라이버 라이선스
- 드라이버 라이선스
- Drivers Lic
- Drivers Lics
- Drivers License
- Drivers Licenses
- Drivers Licence
- Drivers Licences
- driver' Lic
- driver'lics
- driver' 라이선스
- driver'licenses
- driver' 라이선스
- Driver'Licences
- Driver'Lic
- Driver' Lics
- Driver' License
- Driver'Licenses
- Driver'Licence
- Driver'Licences
- Driver'sLic
- drivers (slics)
- driver'slicense
- driver'slicenses
- Driver'sLicence
- Driver'sLicences
- Driver's Lic
- Driver's Lics
- Driver's License
- Driver's Licenses
- Driver's Licence
- Driver's Licences
- Permis de Conduire
- id
- 번호가
- idcard number
- idcard numbers
- idcard #
- idcard #s
- idcard card
- idcard cards
- idcard
- identification number
- identification numbers
- identification #
- identification #s
- identification card
- identification cards
- 확인과 
- DL
- 된다 
- cdl # 
- cdls # 
- driverlic # 
- driverlics # 
- driverlicense # 
- driverlicenses # 
- driverlicence # 
- DriverLicences # 
- Driver Lic#
- Driver Lics# 
- Driver License# 
- Driver Licenses# 
- Driver License# 
- Driver Licences# 
- DriversLic # 
- driverslics # 
- 드라이버 라이선스 # 
- 드라이버 라이선스 수 
- 드라이버 라이선스 # 
- DriversLicences # 
- Drivers Lic# 
- Drivers Lics# 
- Drivers License# 
- Drivers Licenses# 
- Drivers Licence# 
- Drivers Licences# 
- driver' Lic # 
- driver'lics # 
- driver' 라이선스 # 
- driver'licenses # 
- driver' 라이선스 # 
- Driver'Licences # 
- Driver' Lic# 
- Driver' Lics# 
- Driver' License# 
- Driver' Licenses# 
- Driver' Licence# 
- Driver' Licences# 
- Driver'sLic # 
- drivers (slics #) 
- driver'slicense # 
- driver'slicenses # 
- Driver'sLicence # 
- Driver'sLicences # 
- Driver's Lic# 
- Driver's Lics# 
- Driver's License# 
- Driver's Licenses# 
- Driver's Licence# 
- Driver's Licences# 
- Permis de Conduire# 
- i 
- 번호가 
- idcard card# 
- idcard cards# 
- idcard # 
- identification card# 
- identification cards# 
- 확인과 
   
## <a name="canada-health-service-number"></a>캐나다 건강 서비스 번호

### <a name="format"></a>형식일

10자리 숫자

### <a name="pattern"></a>패턴

10자리 숫자

### <a name="checksum"></a>제외

아니요

### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
- Regex_canada_health_service_number 정규식이 해당 패턴과 일치하는 콘텐츠를 찾습니다.
- Keyword_canada_health_service_number의 키워드가 발견되었습니다.

```
<!-- Canada Health Service Number -->
<Entity id="59c0bf39-7fab-482c-af25-00faa4384c94" patternsProximity="300" recommendedConfidence="75">
  <Pattern confidenceLevel="75">
        <IdMatch idRef="Regex_canada_health_service_number" />
        <Any minMatches="1">
          <Match idRef="Keyword_canada_health_service_number" />
        </Any>
  </Pattern>
</Entity>
```

### <a name="keywords"></a>키워드

#### <a name="keywordcanadahealthservicenumber"></a>Keyword_canada_health_service_number

- personal health number
- patient information
- health services
- speciality services
- automobile accident
- patient hospital
- psychiatrist
- workers compensation
- 종류
      
## <a name="canada-passport-number"></a>캐나다 여권 번호

### <a name="format"></a>형식일

2개의 대문자와 6자리 숫자

### <a name="pattern"></a>패턴

2개의 대문자와 6자리 숫자

### <a name="checksum"></a>제외

아니요

### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
- Regex_canada_passport_number 정규식이 해당 패턴과 일치하는 콘텐츠를 찾습니다.
- Keyword_canada_passport_number 또는 Keyword_passport의 키워드를 찾았습니다.

``` 
<!-- Canada Passport Number -->
<Entity id="14d0db8b-498a-43ed-9fca-f6097ae687eb" patternsProximity="300" recommendedConfidence="75">
  <Pattern confidenceLevel="75">
        <IdMatch idRef="Regex_canada_passport_number" />
        <Any minMatches="1">
          <Match idRef="Keyword_canada_passport_number" />
          <Match idRef="Keyword_passport" />
        </Any>
  </Pattern>
</Entity>
```

### <a name="keywords"></a>키워드

#### <a name="keywordcanadapassportnumber"></a>Keyword_canada_passport_number

- canadian citizenship
- canadian passport
- passport application
- passport photos
- certified translator
- canadian citizens
- processing times
- renewal application

#### <a name="keywordpassport"></a>Keyword_passport

- Passport Number
- Passport No
- Passport #
- 여권
- PassportID
- Passportno
- passportnumber
- パスポート
- パスポート番号
- パスポートのNum
- パスポート #
- Numéro de passeport
- Passeport n °
- Passeport Non
- Passeport #
- 포트 #
- 지/포트 아님
- Passeportn °
   
## <a name="canada-personal-health-identification-number-phin"></a>캐나다 PHIN(개인 건강 식별 번호)

### <a name="format"></a>형식일

9자리 숫자

### <a name="pattern"></a>패턴

9자리 숫자

### <a name="checksum"></a>제외

아니요

### <a name="definition"></a>정의

DLP 정책은 300 문자 (예: Regex_canada_phin)에서 해당 패턴과 일치 하는 콘텐츠를 찾는 경우이 유형의 중요 한 정보를 검색 한다는 것을 75% 확신 합니다.
Keyword_canada_phin 또는 Keyword_canada_provinces의 키워드를 두 개 이상 찾았습니다.

```
<!-- Canada PHIN -->
<Entity id="722e12ac-c89a-4ec8-a1b7-fea3469f89db" patternsProximity="300" recommendedConfidence="75">
  <Pattern confidenceLevel="75">
        <IdMatch idRef="Regex_canada_phin" />
        <Any minMatches="2">
          <Match idRef="Keyword_canada_phin" />
          <Match idRef="Keyword_canada_provinces" />
        </Any>
  </Pattern>
</Entity>
```

### <a name="keywords"></a>키워드

#### <a name="keywordcanadaphin"></a>Keyword_canada_phin

- social insurance number
- health information act
- income tax information
- manitoba health
- health registration
- prescription purchases
- benefit eligibility
- personal health
- power of attorney
- registration number
- personal health number
- practitioner referral
- wellness professional
- patient referral
- health and wellness

#### <a name="keywordcanadaprovinces"></a>Keyword_canada_provinces

- Nunavut
- 퀘벡
- Northwest Territories
- 온타리오
- British Columbia
- 앨버타
- 서스캐처원
- 매니토바
- Yukon
- Newfoundland and Labrador
- New Brunswick
- Nova Scotia
- Prince Edward Island
- 캐나다
   
## <a name="canada-social-insurance-number"></a>캐나다 사회 보험 번호

### <a name="format"></a>형식일

선택적 하이픈 또는 공백을 포함하는 9자리 숫자

### <a name="pattern"></a>패턴

서식이
- 3자리 숫자 
- 하이픈 또는 공백 
- 3자리 숫자 
- 하이픈 또는 공백 
- 3자리 숫자

서식 없음: 9 자리 숫자

### <a name="checksum"></a>제외

예

### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.
- Func_canadian_sin 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.
- 2개 이상의 다음 항목 조합:
    - Keyword_sin의 키워드가 발견되었습니다.
    - Keyword_sin_collaborative의 키워드가 발견되었습니다.
    - Func_eu_date 함수가 올바른 날짜 형식의 날짜를 찾습니다.
- 체크섬이 통과됩니다.

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
- Func_unformatted_canadian_sin 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.
- Keyword_sin의 키워드가 발견되었습니다.
- 체크섬이 통과됩니다.

```
<!-- Canada Social Insurance Number -->
<Entity id="a2f29c85-ecb8-4514-a610-364790c0773e" patternsProximity="300" recommendedConfidence="75">
  <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_canadian_sin" />
        <Any minMatches="2">
          <Match idRef="Keyword_sin" />
          <Match idRef="Keyword_sin_collaborative" />
          <Match idRef="Func_eu_date" />
        </Any>
  </Pattern>
  <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_unformatted_canadian_sin" />
        <Match idRef="Keyword_sin" />
  </Pattern>
</Entity>
```

### <a name="keywords"></a>키워드

#### <a name="keywordsin"></a>Keyword_sin

- sin 
- social insurance 
- numero d'assurance sociale 
- 죄 
- ssn 
- 있는 ssn 
- social security 
- numero d'assurance social 
- national identification number 
- national id 
- sin 
- soc ins 
- social ins 

#### <a name="keywordsincollaborative"></a>Keyword_sin_collaborative

- driver's license 
- drivers license 
- driver's licence 
- drivers licence 
- dob 
- 생년월일 
- 생일 
- Date of Birth 
   
## <a name="chile-identity-card-number"></a>	칠레 ID 카드 번호

### <a name="format"></a>형식일

7-8 자리 숫자와 구분 기호 확인 숫자 또는 문자

### <a name="pattern"></a>패턴

7-8자리 숫자와 구분 기호:
- 1-2자리 숫자 
- 마침표  
- 3자리 숫자 
- 마침표  
- 3자리 숫자 
- 대시 1개 
- 검사 숫자에 해당하는 1자리 숫자 또는 문자(대/소문자 구분 안 함)

### <a name="checksum"></a>제외

예

### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.
- Func_chile_id_card 함수가 해당 패턴과 일치 하는 콘텐츠를 찾습니다.
- Keyword_chile_id_card에서 키워드가 발견 되었습니다.
- 체크섬이 통과됩니다.

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
- Func_chile_id_card 함수가 해당 패턴과 일치 하는 콘텐츠를 찾습니다.
- 체크섬이 통과됩니다.

```
<!-- Chile Identity Card Number -->
<Entity id="4e979794-49a0-407e-a0b9-2c536937b925" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Func_chile_id_card"/>
     <Match idRef="Keyword_chile_id_card"/>
  </Pattern>
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Func_chile_id_card"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a>키워드

#### <a name="keywordchileidcard"></a>Keyword_chile_id_card

- National Identification Number 
- Identity card 
- ID 
- 확인과 
- Rol Único Nacional 
- 실행 
- Rol Único Tributario 
- RUT 
- Cédula de Identidad 
- Número De Identificación Nacional 
- Tarjeta de identificación 
- Identificación 
   
## <a name="china-resident-identity-card-prc-number"></a>	중국 주민 ID 카드(PRC) 번호

### <a name="format"></a>형식일

18자리 숫자

### <a name="pattern"></a>패턴

18자리 숫자:
- 주소 코드에 해당하는 6자리 숫자  
- 생년월일에 해당하는 YYYYMMDD 형식의 8자리 숫자  
- 주문 코드에 해당하는 3자리 숫자  
- 검사 숫자에 해당하는 1자리 숫자

### <a name="checksum"></a>제외

예

### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.
- Func_china_resident_id 함수가 해당 패턴과 일치 하는 콘텐츠를 찾습니다.
- Keyword_china_resident_id에서 키워드가 발견 되었습니다.
- 체크섬이 통과됩니다.

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
- Func_china_resident_id 함수가 해당 패턴과 일치 하는 콘텐츠를 찾습니다.
- 체크섬이 통과됩니다.

```
<!-- China Resident Identity Card (PRC) Number -->
<Entity id="c92daa86-2d16-4871-901f-816b3f554fc1" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Func_china_resident_id"/>
     <Match idRef="Keyword_china_resident_id"/>
  </Pattern>
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Func_china_resident_id"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a>키워드

### <a name="keywordchinaresidentid"></a>Keyword_china_resident_id

- Resident Identity Card 
- 중국 
- National Identification Card 
- 身份证 
- 居民 身份证 
- 居民身份证 
- 鉴定 
- 身分證 
- 居民 身份證
- 鑑定 
   
## <a name="credit-card-number"></a>신용 카드 번호

### <a name="format"></a>형식일

서식이 있거나 서식이 없을 수 있는 16 자리 (dddddddddddddddd), Luhn 테스트를 통과 해야 합니다.

### <a name="pattern"></a>패턴

Visa, MasterCard, Discover Card, JCB, American Express, 상품권 및 식사권을 비롯하여 전 세계 모든 주요 브랜드 카드를 검색하는 매우 복잡하고 강력한 패턴입니다.

### <a name="checksum"></a>제외

있음(Luhn 체크섬)

### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.
- Func_credit_card 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.
- 다음 중 하나가 충족됩니다.
    - Keyword_cc_verification의 키워드가 발견되었습니다.
    - Keyword_cc_name의 키워드가 발견되었습니다.
    - Func_expiration_date 함수가 올바른 날짜 형식의 날짜를 찾습니다.
- 체크섬이 통과됩니다.

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 65% 신뢰합니다.
- Func_credit_card 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.
- 체크섬이 통과됩니다.

```
<!-- Credit Card Number -->
<Entity id="50842eb7-edc8-4019-85dd-5a5c1f2bb085" patternsProximity="300" recommendedConfidence="85">
  <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_credit_card" />
        <Any minMatches="1">
          <Match idRef="Keyword_cc_verification" />
          <Match idRef="Keyword_cc_name" />
          <Match idRef="Func_expiration_date" />
        </Any>
  </Pattern>
  <Pattern confidenceLevel="65">
        <IdMatch idRef="Func_credit_card" />
  </Pattern>
</Entity>
```

### <a name="keywords"></a>키워드

#### <a name="keywordccverification"></a>Keyword_cc_verification

- card verification
- card identification number
- cvn
- cid
- cvc2
- cvv2
- pin block
- security code
- security number
- security no
- issue number
- issue no
- cryptogramme
- numéro de sécurité
- numero de securite
- kreditkartenprüfnummer
- kreditkartenprufnummer
- prüfziffer
- prufziffer
- sicherheits Kode
- sicherheitscode
- sicherheitsnummer
- verfalldatum
- codice di verifica
- cod. sicurezza
- cod sicurezza
- n autorizzazione
- código
- codigo
- cod. seg
- cod seg
- código de segurança
- codigo de seguranca
- codigo de segurança
- código de seguranca
- cód segurança
- cod. seguranca cod segurança
- cód seguranca
- cód segurança
- cod seguranca cod segurança
- cód seguranca
- número de verificação
- numero de verificacao
- ablauf
- gültig bis
- gültigkeitsdatum
- gultig bis
- gultigkeitsdatum
- scadenza
- data scad
- fecha de expiracion
- fecha de venc
- vencimiento
- válido hasta
- valido hasta
- vto
- data de expiração
- data de expiracao
- data em que expira
- 유효한 ade
- valor
- vencimento
- venc 

#### <a name="keywordccname"></a>Keyword_cc_name

- amex
- american express
- americanexpress
- Visa
- mastercard
- master card
- mc 
- mastercards
- master cards
- diner's Club
- diners club
- dinersclub
- discover card
- discovercard
- discover cards
- JCB
- japanese card bureau
- carte blanche
- carteblanche
- credit card
- 참조란
- 참조 #:
- expiration date
- exp date
- expiry date
- date d’expiration
- date d'exp
- date expiration
- bank card
- bankcard
- card number
- card num
- 전화 번호
- 시 번호
- card numbers
- 카드
- credit cards
- creditcards
- ccn
- card holder
- 소유자
- card holders
- 에이 홀더
- check card
- checkcard
- check cards
- checkcards
- debit card
- debitcard
- debit cards
- debitcards
- atm card
- atmcard
- atm cards
- atmcards
- enroute
- en route
- card type
- carte bancaire
- carte de crédit
- carte de credit
- numéro de carte
- numero de carte
- nº de la carte
- nº de carte
- kreditkarte
- karte
- karteninhaber
- karteninhabers
- kreditkarteninhaber
- kreditkarteninstitut
- kreditkartentyp
- eigentümername
- kartennr 
- kartennummer
- kreditkartennummer
- kreditkarten-nummer
- carta di credito
- carta credito
- 카 ta
- n carta
- veiligheid. 카 ta
- nr carta
- numero carta
- numero della carta
- numero di carta
- tarjeta credito
- tarjeta de credito
- tarjeta crédito
- tarjeta de crédito
- tarjeta de atm
- tarjeta atm
- tarjeta debito
- tarjeta de debito
- tarjeta débito
- tarjeta de débito
- nº de tarjeta
- 아니요. de tarjeta
- no de tarjeta
- numero de tarjeta
- número de tarjeta
- tarjeta no
- tarjetahabiente
- cartão de crédito
- cartão de credito
- cartao de crédito
- cartao de credito
- cartão de débito
- cartao de débito
- cartão de debito
- cartao de debito
- débito automático
- debito automatico
- número do cartão
- numero do cartão 
- número do cartao
- numero do cartao
- número de cartão
- numero de cartão
- número de cartao
- numero de cartao
- nº do cartão
- nº do cartao
- n º do cartão
- no do cartão
- no do cartao
- 아니요. do cartão
- 아니요. do cartao 
   
## <a name="croatia-identity-card-number"></a>크로아티아 ID 카드 번호

### <a name="format"></a>형식일

9자리 숫자

### <a name="pattern"></a>패턴

9자리 연속 숫자

### <a name="checksum"></a>제외

아니요

### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
- Func_croatia_id_card 함수가 해당 패턴과 일치 하는 콘텐츠를 찾습니다.
- Keyword_croatia_id_card에서 키워드가 발견 되었습니다.

```
<!--Croatia Identity Card Number-->
<Entity id="ff12f884-c20a-4189-b185-34c8e7258d47" recommendedConfidence="75" patternsProximity="300">
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Func_croatia_id_card"/>
     <Match idRef="Keyword_croatia_id_card"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a>키워드

#### <a name="keywordcroatiaidcard"></a>Keyword_croatia_id_card

- Croatian identity card
- Osobna iskaznica

   
## <a name="croatia-personal-identification-oib-number"></a>크로아티아 개인 식별(OIB) 번호

### <a name="format"></a>형식일

11자리 숫자

### <a name="pattern"></a>패턴

11자리 숫자:
- 10자리 숫자 
- 최종 자릿수는 국제 데이터 교환 목적을 위한 검사 숫자 이며, HR는 11 자리 숫자 앞에 추가 됩니다.

### <a name="checksum"></a>제외

예

### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.
- Func_croatia_oib_number 함수가 해당 패턴과 일치 하는 콘텐츠를 찾습니다.
- Keyword_croatia_oib_number에서 키워드가 발견 되었습니다.
- 체크섬이 통과됩니다.

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
- Func_croatia_oib_number 함수가 해당 패턴과 일치 하는 콘텐츠를 찾습니다.
- 체크섬이 통과됩니다.

```
<!-- Croatia Personal Identification (OIB) Number -->
<Entity id="31983b6d-db95-4eb2-a630-b44bd091968d" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Func_croatia_oib_number"/>
     <Match idRef="Keyword_croatia_oib_number"/>
  </Pattern>
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Func_croatia_oib_number"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a>키워드

#### <a name="keywordcroatiaoibnumber"></a>Keyword_croatia_oib_number

- Personal Identification Number
- Osobni identifikacijski broj 
- OIB 

   
## <a name="czech-personal-identity-number"></a>체코어 개인 id 번호

### <a name="format"></a>형식일

선택적 슬래시 (이전 형식)가 있는 9 자리 숫자와 슬래시 (새 형식)가 있는 10 자리 숫자

### <a name="pattern"></a>패턴

9 자리 숫자 (이전 형식):
- 9자리 숫자

또는

- 출생 날짜를 나타내는 6 자리 숫자
- 정방향 슬래시
- 3자리 숫자

10 자리 숫자 (새 형식):
- 10자리 숫자

또는

- 출생 날짜를 나타내는 6 자리 숫자
- 정방향 슬래시 
- 마지막 숫자가 검사 숫자인 4 자리 숫자

### <a name="checksum"></a>제외

예

### <a name="definition"></a>정의

DLP 정책은 300 문자 근사에서 Func_czech_id_card 함수가 해당 패턴과 일치 하는 콘텐츠를 발견 하는 경우이 유형의 중요 한 정보를 검색 한다는 것을 85% 확신 합니다.
Keyword_czech_id_card에서 키워드가 발견 되었습니다.
체크섬이 통과됩니다.

```
<!-- Czech Personal Identity Number -->
<Entity id="60c0725a-4eb6-455b-9dda-05d8a7396497"      patternsProximity="300" recommendedConfidence="85">
   <Pattern confidenceLevel="85">
      <IdMatch idRef="Func_czech_id_card" />
      <Match idRef="Keyword_czech_id_card" />
   </Pattern>
</Entity>
```
### <a name="keywords"></a>키워드

- 체코어 개인 id 번호
- rodné číslo
   
## <a name="denmark-personal-identification-number"></a>덴마크 개인 식별 번호

### <a name="format"></a>형식일

하이픈을 포함하는 10자리 숫자

### <a name="pattern"></a>패턴

10자리 숫자:
- 생년월일에 해당하는 DDMMYY 형식의 6자리 숫자  
- 하이픈 
- 마지막 숫자가 검사 숫자인 4자리 숫자

### <a name="checksum"></a>제외

예

### <a name="definition"></a>정의

DLP 정책은 300 문자 (예: Regex_denmark_id)에서 해당 패턴과 일치 하는 콘텐츠를 찾는 경우이 유형의 중요 한 정보를 검색 한다는 것을 75% 확신 합니다.
Keyword_denmark_id에서 키워드가 발견 되었습니다.
체크섬이 통과됩니다.

```
<!-- Denmark Personal Identification Number -->
<Entity id="6c4f2fef-56e1-4c00-8093-88d7a01cf460" recommendedConfidence="75" patternsProximity="300">
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Regex_denmark_id"/>
     <Match idRef="Keyword_denmark_id"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a>키워드

#### <a name="keyworddenmarkid"></a>Keyword_denmark_id

- Personal Identification Number
- CPR
- Det Centrale Personregister
- Personnummer
   
## <a name="drug-enforcement-agency-dea-number"></a>DEA(약물 집행 기구) 번호

### <a name="format"></a>형식일

2개 문자와 7자리 숫자

### <a name="pattern"></a>패턴

패턴에는 다음이 모두 포함되어야 합니다.
- 등록 코드에 해당하는 abcdefghjklmnprstux 중 한 문자(대/소문자 구분 안 함) 
- 등록자 성의 첫 문자에 해당하는 한 문자(대/소문자 구분 안 함) 
- 검사 숫자의 마지막 7개 숫자

### <a name="checksum"></a>제외

예

### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.
- Func_dea_number 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.
- 체크섬이 통과됩니다.

```
<!-- DEA Number -->
<Entity id="9a5445ad-406e-43eb-8bd7-cac17ab6d0e4" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Func_dea_number"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a>키워드

없음

   
## <a name="eu-debit-card-number"></a>유럽 직불 카드 번호

### <a name="format"></a>형식일

16자리 숫자

### <a name="pattern"></a>패턴

매우 복잡하고 강력한 패턴

### <a name="checksum"></a>제외

예

### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.
- Func_eu_debit_card 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.
- 다음 중 하나 이상이 충족됩니다.
    - Keyword_eu_debit_card의 키워드가 발견되었습니다.
    - Keyword_card_terms_dict의 키워드가 발견되었습니다.
    - Keyword_card_security_terms_dict의 키워드가 발견되었습니다.
    - Keyword_card_expiration_terms_dict의 키워드가 발견되었습니다.
    - Func_expiration_date 함수가 올바른 날짜 형식의 날짜를 찾습니다.
- 체크섬이 통과됩니다.

```
    <!-- EU Debit Card Number -->
    <Entity id="0e9b3178-9678-47dd-a509-37222ca96b42" patternsProximity="300" recommendedConfidence="85">
      <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_eu_debit_card" />
        <Any minMatches="1">
          <Match idRef="Keyword_eu_debit_card" />
          <Match idRef="Keyword_card_terms_dict" />
          <Match idRef="Keyword_card_security_terms_dict" />
          <Match idRef="Keyword_card_expiration_terms_dict" />
          <Match idRef="Func_expiration_date" />
        </Any>
      </Pattern>
    </Entity>
```

### <a name="keywords"></a>키워드

#### <a name="keywordeudebitcard"></a>Keyword_eu_debit_card

- account number 
- card number 
- card no. 
- security number 
- 참조란 

#### <a name="keywordcardtermsdict"></a>Keyword_card_terms_dict

- acct nbr 
- acct num 
- acct no 
- american express 
- americanexpress 
- americano espresso 
- amex 
- atm card 
- atm cards 
- atm kaart 
- atmcard 
- atmcards 
- atmkaart 
- atmkaarten 
- bancontact 
- bank card 
- bankkaart 
- card holder 
- card holders 
- card num 
- card number 
- card numbers 
- card type 
- cardano numerico 
- 소유자 
- 에이 홀더 
- 전화 번호 
- 시 번호 
- carta bianca 
- carta credito 
- carta di credito 
- cartao de credito 
- cartao de crédito 
- cartao de debito 
- cartao de débito 
- carte bancaire 
- carte blanche 
- carte bleue 
- carte de credit 
- carte de crédit 
- carte di credito 
- carteblanche 
- cartão de credito 
- cartão de crédito 
- cartão de debito 
- cartão de débito 
- cb 
- ccn 
- check card 
- check cards 
- checkcard
- checkcards 
- chequekaart 
- cirrus 
- cirrus-edc-maestro 
- controlekaart 
- controlekaarten 
- credit card 
- credit cards 
- 카드 
- creditcards 
- debetkaart 
- debetkaarten 
- debit card 
- debit cards 
- debitcard 
- debitcards 
- debito automatico 
- diners club 
- dinersclub 
- 찾아보십시오 
- discover card 
- discover cards 
- discovercard 
- discovercards 
- débito automático
- edc 
- eigentümername 
- european debit card 
- hoofdkaart 
- hoofdkaarten 
- in viaggio 
- japanese card bureau 
- japanse kaartdienst 
- jcb 
- kaart 
- kaart num 
- kaartaantal 
- kaartaantallen 
- kaarthouder 
- kaarthouders 
- karte  
- karteninhaber 
- karteninhabers
- kartennr 
- kartennummer 
- kreditkarte 
- kreditkarten-nummer 
- kreditkarteninhaber 
- kreditkarteninstitut 
- kreditkartennummer 
- kreditkartentyp 
- maestro 
- master card 
- master cards 
- mastercard 
- mastercards 
- mc 
- mister cash 
- n carta 
- 카 ta 
- no de tarjeta 
- no do cartao 
- no do cartão 
- 아니요. de tarjeta 
- 아니요. do cartao 
- 아니요. do cartão 
- nr carta 
- veiligheid. 카 ta 
- numeri di scheda 
- numero carta 
- numero de cartao 
- numero de carte 
- numero de cartão 
- numero de tarjeta
- numero della carta 
- numero di carta 
- numero di scheda 
- numero do cartao 
- numero do cartão 
- numéro de carte 
- nº carta 
- nº de carte 
- nº de la carte 
- nº de tarjeta 
- nº do cartao 
- nº do cartão 
- n º do cartão 
- número de cartao 
- número de cartão 
- número de tarjeta 
- número do cartao 
- scheda dell'assegno 
- scheda dell'atmosfera 
- scheda dell'atmosfera 
- scheda della banca 
- scheda di controllo 
- scheda di debito 
- scheda matrice 
- schede dell'atmosfera 
- schede di controllo 
- schede di debito 
- schede matrici 
- scoprono la scheda 
- scoprono le schede 
- 분리 
- supporti di scheda 
- supporto di scheda 
- 스위치 
- tarjeta atm 
- tarjeta credito 
- tarjeta de atm 
- tarjeta de credito 
- tarjeta de debito 
- tarjeta debito 
- tarjeta no
- tarjetahabiente 
- tipo della scheda 
- ufficio giapponese della 
- scheda 
- v pay 
- v-지급 
- visa 
- visa plus 
- visa electron 
- visto 
- visum 
- vpay   

#### <a name="keywordcardsecuritytermsdict"></a>Keyword_card_security_terms_dict

- card identification number
- card verification 
- cardi la verifica 
- cid 
- cod seg 
- cod seguranca 
- cod segurança 
- cod sicurezza 
- cod. seg 
- cod. seguranca 
- cod. segurança 
- cod. sicurezza 
- codice di sicurezza 
- codice di verifica 
- codigo 
- codigo de seguranca 
- codigo de segurança 
- crittogramma 
- cryptogram 
- cryptogramme 
- cv2 
- cvc 
- cvc2 
- cvn 
- cvv 
- cvv2 
- cód seguranca 
- cód segurança 
- cód seguranca 
- cód segurança 
- código 
- código de seguranca 
- código de segurança 
- de kaart controle 
- geeft nr uit 
- issue no 
- issue number 
- kaartidentificatienummer 
- kreditkartenprufnummer 
- kreditkartenprüfnummer 
- kwestieaantal 
- 아니요. dell'edizione 
- 아니요. di sicurezza 
- numero de securite 
- numero de verificacao 
- numero dell'edizione 
- numero di identificazione della 
- scheda 
- numero di sicurezza 
- numero van veiligheid 
- numéro de sécurité 
- nº autorizzazione 
- número de verificação 
- perno il blocco 
- pin block 
- prufziffer 
- prüfziffer 
- security code 
- security no 
- security number 
- sicherheits kode 
- sicherheitscode 
- sicherheitsnummer 
- speldblok 
- veiligheid 번호: 
- veiligheidsaantal 
- veiligheidscode 
- veiligheidsnummer 
- verfalldatum 

#### <a name="keywordcardexpirationtermsdict"></a>Keyword_card_expiration_terms_dict

- ablauf 
- data de expiracao 
- data de expiração 
- data del exp 
- data di exp 
- data di scadenza 
- data em que expira 
- data scad 
- data scadenza 
- date de validité 
- datum afloop 
- datum van exp 
- de afloop 
- espira 
- espira 
- exp date 
- exp datum 
- 행사 
- 예정 
- expires 
- 만료 
- fecha de expiracion 
- fecha de venc 
- gultig bis 
- gultigkeitsdatum 
- gültig bis 
- gültigkeitsdatum 
- la scadenza 
- scadenza 
- valable 
- 유효한 ade 
- valido hasta 
- valor 
- venc 
- vencimento 
- vencimiento 
- verloopt 
- vervaldag 
- vervaldatum 
- vto 
- válido hasta 
   
## <a name="eu-drivers-license-number"></a>EU 운전 면허 번호

자세한 내용은 [EU 운전 면허 번호 중요 정보 유형을](eu-driver-s-license-number.md)참조 하십시오.
  
## <a name="eu-national-identification-number"></a>EU 국가 식별 번호

자세한 내용은 [EU 국가 식별 번호 중요 한 정보 유형을](eu-national-identification-number.md)참조 하세요.
  
## <a name="eu-passport-number"></a>EU 여권 번호

자세한 내용은 [EU Passport 번호 중요 한 정보 유형을](eu-passport-number.md)참조 하십시오.
  
## <a name="eu-social-security-number-or-equivalent-id"></a>EU 주민 등록 번호 또는 동등한 ID

자세한 내용은 [EU 주민 등록 번호 또는 동등한 ID 중요 정보 유형을](eu-social-security-number-or-equivalent-id.md)참조 하십시오.
  
## <a name="eu-tax-identification-number"></a>EU 세금 확인 번호

자세한 내용은 [EU 세금 식별 번호 중요 한 정보 유형을](eu-tax-identification-number.md)참조 하십시오.
  
## <a name="finland-national-id"></a>핀란드 국가 ID

### <a name="format"></a>형식일

세기를 나타내는 6자리 숫자와 문자, 3자리 숫자와 검사 숫자

### <a name="pattern"></a>패턴

패턴에는 다음이 모두 포함되어야 합니다.
- 생년월일에 해당하는 DDMMYY 형식의 6자리 숫자 
- 세기 표시('-', '+' 또는 'a') 
- 3자리 개인 ID 번호 
- 검사 숫자에 해당하는 1자리 숫자 또는 문자(대/소문자 구분 안 함)

### <a name="checksum"></a>제외

예

### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.
- Func_finnish_national_id 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.
- Keyword_finnish_national_id의 키워드가 발견되었습니다.
- 체크섬이 통과됩니다.

```
<!-- Finnish National ID-->
<Entity id="338FD995-4CB5-4F87-AD35-79BD1DD926C1" patternsProximity="300" recommendedConfidence="85">
  <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_finnish_national_id" />
          <Match idRef="Keyword_finnish_national_id" />
  </Pattern>
</Entity>
```

### <a name="keywords"></a>키워드

- Keyword_finnish_national_id
- Sosiaaliturvatunnus
- SOTU Henkilötunnus HETU
- Personbeteckning
- Personnummer
   
## <a name="finland-passport-number"></a>핀란드 여권 번호

9 개의 문자 및 숫자 패턴 조합 형식 조합: 두 문자 (대/소문자 구분 안 함) 7 자리 체크섬 정의 없음 DLP 정책은이 유형의 중요 한 정보를 검색 한 것으로,이에 따라 300 문자의 근사: 정규식 Regex_finland_passport_number 해당 패턴과 일치 하는 콘텐츠를 찾습니다.
Keyword_finland_passport_number에서 키워드가 발견 되었습니다.
<!-- Finland Passport Number -->
<Entity id="d1685ac3-1d3a-40f8-8198-32ef5669c7a5" recommendedConfidence="75" patternsProximity="300"> <Pattern confidenceLevel="75"> <IdMatch idRef="Regex_finland_passport_number"/> <Match idRef="Keyword_finland_passport_number"/> </Pattern>
</Entity>
passport Keyword_finland_passport_number 키워드
   
## <a name="france-drivers-license-number"></a>프랑스 운전 면허 번호

### <a name="format"></a>형식일

12자리 숫자

### <a name="pattern"></a>패턴

비슷한 패턴(예: 프랑스 전화 번호)을 무시하기 위한 유효성 검사 기능을 포함하는 12자리 숫자

### <a name="checksum"></a>제외

아니요

### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
- Func_french_drivers_license 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.
- 다음 중 하나 이상이 충족됩니다.
- Keyword_french_drivers_license의 키워드가 발견되었습니다.
- Func_eu_date 함수가 올바른 날짜 형식의 날짜를 찾습니다.

```
<!-- France Driver's License Number -->
<Entity id="18e55a36-a01b-4b0f-943d-dc10282a1824" patternsProximity="300" recommendedConfidence="75">
  <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_french_drivers_license" />
        <Any minMatches="1">
          <Match idRef="Keyword_french_drivers_license" />
          <Match idRef="Func_eu_date" />
        </Any>
  </Pattern>
</Entity>
```

### <a name="keywords"></a>키워드

#### <a name="keywordfrenchdriverslicense"></a>Keyword_french_drivers_license

- drivers licence
- drivers license
- driving licence
- driving license
- permis de conduire
- licence number
- license number
- licence numbers
- license numbers

## <a name="france-national-id-card-cni"></a>프랑스 국가 ID 카드(CNI)

### <a name="format"></a>형식일

12자리 숫자

### <a name="pattern"></a>패턴

12자리 숫자

### <a name="checksum"></a>제외

아니요

### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 65% 신뢰합니다.
- Regex_france_cni 정규식이 해당 패턴과 일치하는 콘텐츠를 찾습니다.

```
<!-- France CNI -->
<Entity id="f741ac74-1bc0-4665-b69b-f0c7f927c0c4" patternsProximity="300" recommendedConfidence="65">
  <Pattern confidenceLevel="65">
        <IdMatch idRef="Regex_france_cni" />
  </Pattern>
</Entity>
```

### <a name="keywords"></a>키워드

없음
   
## <a name="france-passport-number"></a>프랑스 여권 번호

### <a name="format"></a>형식일

9자리 숫자 및 문자

### <a name="pattern"></a>패턴

9자리 숫자 및 문자:
- 2자리 숫자 
- 2문자(대/소문자 구분 안 함) 
- 5자리 숫자

### <a name="checksum"></a>제외

아니요

### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
- Func_fr_passport 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.
- Keyword_passport의 키워드가 발견되었습니다.

```
<!-- France Passport Number -->
<Entity id="3008b884-8c8c-4cd8-a289-99f34fc7ff5d" patternsProximity="300" recommendedConfidence="75">
  <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_fr_passport" />
        <Match idRef="Keyword_passport" />
  </Pattern>
</Entity>
```

### <a name="keywords"></a>키워드

#### <a name="keywordpassport"></a>Keyword_passport

- Passport Number
- Passport No
- Passport #
- 여권
- PassportID
- Passportno
- passportnumber
- パスポート
- パスポート番号
- パスポートのNum
- パスポート ＃ 
- Numéro de passeport
- Passeport n °
- Passeport Non
- Passeport #
- 포트 #
- 지/포트 아님
- Passeportn °

      
## <a name="france-social-security-number-insee"></a>프랑스 사회 보장 번호(INSEE)

### <a name="format"></a>형식일

15자리 숫자

### <a name="pattern"></a>패턴

다음 두 패턴 중 하나가 일치해야 합니다.
- 13 자리 숫자와 공백 다음 두 자리 숫자<br/>
또는
- 15자리 연속 숫자

### <a name="checksum"></a>제외

예

### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 95% 신뢰합니다.
- Func_french_insee 또는 Func_fr_insee 함수가 해당 패턴과 일치 하는 콘텐츠를 찾습니다.
- Keyword_fr_insee의 키워드가 발견되었습니다.
- 체크섬이 통과됩니다.

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.
- Func_french_insee 또는 Func_fr_insee 함수가 해당 패턴과 일치 하는 콘텐츠를 찾습니다.
- Keyword_fr_insee의 키워드가 발견되지 않았습니다.
- 체크섬이 통과됩니다.

```
<!-- France INSEE -->
<Entity id="71f62b97-efe0-4aa1-aa49-e14de253619d" patternsProximity="300" recommendedConfidence="85">
  <Pattern confidenceLevel="95">
        <IdMatch idRef="Func_french_insee" />
        <Match idRef="Func_fr_insee" />
        <Any minMatches="1">
          <Match idRef="Keyword_fr_insee" />
        </Any>
  </Pattern>
  <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_french_insee" />
        <Match idRef="Func_fr_insee" />
        <Any minMatches="0" maxMatches="0">
          <Match idRef="Keyword_fr_insee" />
        </Any>
  </Pattern>
</Entity>
```

### <a name="keywords"></a>키워드

#### <a name="keywordfrinsee"></a>Keyword_fr_insee

- insee
- securité sociale
- securite sociale
- national id
- national identification
- numéro d'identité
- no d'identité
- 아니요. d'identité
- numero d'identite
- no d'identite
- 아니요. d'identite
- social security number
- social security code
- social insurance number
- le numéro d'identification nationale
- d'identité nationale
- numéro de sécurité sociale
- le code de la sécurité sociale
- numéro d'assurance sociale
- numéro de sécu
- code sécu 
   
## <a name="german-drivers-license-number"></a>독일 운전 면허 번호

### <a name="format"></a>형식일

11자리 숫자와 문자 조합

### <a name="pattern"></a>패턴

11자리 숫자와 문자(대/소문자 구분 안 함):
- 1자리 숫자 또는 문자 
- 2자리 숫자 
- 6자리 숫자 또는 문자 
- 1자리 숫자 
- 1자리 숫자 또는 문자

### <a name="checksum"></a>제외

예

### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
- Func_german_drivers_license 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.
- 다음 중 하나 이상이 충족됩니다.
    - Keyword_german_drivers_license_number의 키워드가 발견되었습니다.
    - Keyword_german_drivers_license_collaborative의 키워드가 발견되었습니다.
    - Keyword_german_drivers_license의 키워드가 발견되었습니다.
- 체크섬이 통과됩니다.

```
<!-- German Driver's License Number -->
<Entity id="91da9335-1edb-45b7-a95f-5fe41a16c63c" patternsProximity="300" recommendedConfidence="75">
  <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_german_drivers_license" />
        <Any minMatches="1">
          <Match idRef="Keyword_german_drivers_license_number" />
          <Match idRef="Keyword_german_drivers_license_collaborative" />
          <Match idRef="Keyword_german_drivers_license" />
        </Any>
  </Pattern>
</Entity>
```

### <a name="keywords"></a>키워드

#### <a name="keywordgermandriverslicensenumber"></a>Keyword_german_drivers_license_number

- Führerschein
- Fuhrerschein
- Fuehrerschein
- Führerscheinnummer
- Fuhrerscheinnummer
- Fuehrerscheinnummer
- Führerschein- 
- Fuhrerschein- 
- Fuehrerschein- 
- FührerscheinnummerNr
- FuhrerscheinnummerNr
- FuehrerscheinnummerNr
- FührerscheinnummerKlasse
- FuhrerscheinnummerKlasse
- FuehrerscheinnummerKlasse
- Führerschein- Nr
- Fuhrerschein- Nr
- Fuehrerschein- Nr 
- Führerschein- Klasse 
- Fuhrerschein- Klasse 
- Fuehrerschein- Klasse
- FührerscheinnummerNr 
- FuhrerscheinnummerNr 
- FuehrerscheinnummerNr 
- FührerscheinnummerKlasse 
- FuhrerscheinnummerKlasse 
- FuehrerscheinnummerKlasse 
- Führerschein- Nr 
- Fuhrerschein- Nr 
- Fuehrerschein- Nr 
- Führerschein- Klasse 
- Fuhrerschein- Klasse 
- Fuehrerschein- Klasse 
- DL 
- 된다
- Driv Lic 
- Driv Licen 
- Driv License
- Driv Licenses 
- Driv Licence 
- Driv Licences 
- Driv Lic 
- Driver Licen 
- Driver License 
- Driver Licenses 
- Driver Licence 
- Driver Licences 
- Drivers Lic 
- Drivers Licen 
- Drivers License 
- Drivers Licenses 
- Drivers Licence 
- Drivers Licences 
- Driver's Lic 
- Driver's Licen 
- Driver's License 
- Driver's Licenses 
- Driver's Licence 
- Driver's Licences 
- Driving Lic 
- Driving Licen 
- Driving License 
- Driving Licenses 
- Driving Licence 
- Driving Licences

#### <a name="keywordgermandriverslicensecollaborative"></a>Keyword_german_drivers_license_collaborative

- veiligheid-Führerschein 
- veiligheid-Fuhrerschein 
- veiligheid-Fuehrerschein 
- Führerschein 
- Fuhrerschein 
- Fuehrerschein 
- N-Führerschein 
- N-Fuhrerschein 
- N-Fuehrerschein
- veiligheid-Führerschein 
- veiligheid-Fuhrerschein 
- veiligheid-Fuehrerschein 
- Führerschein 
- Fuhrerschein 
- Fuehrerschein 
- N-Führerschein 
- N-Fuhrerschein 
- N-Fuehrerschein 

#### <a name="keywordgermandriverslicense"></a>Keyword_german_drivers_license

- ausstellungsdatum
- ausstellungsort
- ausstellende behöde
- ausstellende behorde
- ausstellende behoerde
   
## <a name="german-passport-number"></a>독일 여권 번호

### <a name="format"></a>형식일

10자리 숫자 또는 문자

### <a name="pattern"></a>패턴

패턴에는 다음이 모두 포함되어야 합니다.
- 첫 번째 문자는 숫자 또는 (C, F, G, H, J, K) 집합의 문자임 
- 3자리 숫자 
- 5자리 숫자 또는 (C, -H, J-N, P, R, T, V-Z) 집합의 문자 
- 1자리 숫자

### <a name="checksum"></a>제외

예

### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.
- Func_german_passport 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.
- 5개의 키워드 목록 중에 포함된 키워드가 발견되었습니다.
- 체크섬이 통과됩니다.

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
- Func_german_passport_data 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.
- 5개의 키워드 목록 중에 포함된 키워드가 발견되었습니다.
- 체크섬이 통과됩니다.

```
<!-- German Passport Number -->
<Entity id="2e3da144-d42b-47ed-b123-fbf78604e52c" patternsProximity="300" recommendedConfidence="75">
  <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_german_passport" />
        <Any minMatches="1">
          <Match idRef="Keyword_german_passport" />
          <Match idRef="Keyword_german_passport_collaborative" />
          <Match idRef="Keyword_german_passport_number" />
          <Match idRef="Keyword_german_passport1" />
          <Match idRef="Keyword_german_passport2" />
        </Any>
  </Pattern>
  <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_german_passport_data" />
        <Any minMatches="1">
          <Match idRef="Keyword_german_passport" />
          <Match idRef="Keyword_german_passport_collaborative" />
          <Match idRef="Keyword_german_passport_number" />
          <Match idRef="Keyword_german_passport1" />
          <Match idRef="Keyword_german_passport2" />
        </Any>
  </Pattern>
</Entity>
```

### <a name="keywords"></a>키워드

#### <a name="keywordgermanpassport"></a>Keyword_german_passport

- reisepass
- reisepasse
- reisepassnummer
- 여권
- passports

#### <a name="keywordgermanpassportcollaborative"></a>Keyword_german_passport_collaborative

- ge삼 부, tsdatum
- ausstellungsdatum
- ausstellungsort

#### <a name="keywordgermanpassportnumber"></a>Keyword_german_passport_number

Reisepass veiligheid-Reisepass

#### <a name="keywordgermanpassport1"></a>Keyword_german_passport1

Reisepass-veiligheid

#### <a name="keywordgermanpassport2"></a>Keyword_german_passport2

bnationalit
   
## <a name="germany-identity-card-number"></a>독일 ID 카드 번호

### <a name="format"></a>형식일

2010 년 11 월 1 일 이후: 9 개 문자 및 숫자

1 월 1987 년 10 월 31 일 (2010:10 자리 숫자)

### <a name="pattern"></a>패턴

2010년 11월 1일 이후:
- 1개 문자(대/소문자 구분 안 함) 
- 8자리 숫자

1 년 4 월 1987 일 ~ 10 월 31 일까 지:
- 10자리 숫자

### <a name="checksum"></a>제외

아니요

### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 65% 신뢰합니다.
- 정규식 Regex_germany_id_card 해당 패턴과 일치 하는 콘텐츠를 찾습니다.
- Keyword_germany_id_card에서 키워드가 발견 되었습니다.

```
<!-- Germany Identity Card Number -->
<Entity id="e577372f-c42e-47a0-9d85-bebed1c237d4" recommendedConfidence="65" patternsProximity="300">
  <Pattern confidenceLevel="65">
     <IdMatch idRef="Regex_germany_id_card"/>
     <Match idRef="Keyword_germany_id_card"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a>키워드

#### <a name="keywordgermanyidcard"></a>Keyword_germany_id_card

- Identity Card
- ID
- 확인과
- Personalausweis
- Identifizierungsnummer
- ausweis
- Identifikation
   
## <a name="greece-national-id-card"></a>그리스 국가 ID 카드

### <a name="format"></a>형식일

7-8자리 문자 및 숫자와 대시의 조합

### <a name="pattern"></a>패턴

7자리 문자 및 숫자(이전 형식):
- 1개 문자(그리스어 알파벳의 임의 문자)  
- 대시 1개 
- 6자리 숫자

8자리 문자와 숫자(새로운 형식):
- 그리스어 및 라틴어 알파벳 둘 다에 해당 대문자가 포함된 2개 문자(ABEZHIKMNOPTYX)  
- 대시 1개 
- 6자리 숫자

### <a name="checksum"></a>제외

아니요

### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
- 정규식 Regex_greece_id_card 해당 패턴과 일치 하는 콘텐츠를 찾습니다.
- Keyword_greece_id_card에서 키워드가 발견 되었습니다.

```
<!-- Greece National ID Card -->
<Entity id="82568215-1da1-46d3-874a-d2294d81b5ac" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Regex_greece_id_card"/>
     <Match idRef="Keyword_greece_id_card"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a>키워드

#### <a name="keywordgreeceidcard"></a>Keyword_greece_id_card

- Greek identity Card
- Tautotita
- Δελτίο αστυνομικής ταυτότητας
- Ταυτότητα
   
## <a name="hong-kong-identity-card-hkid-number"></a>HKID(홍콩 ID 카드) 번호

### <a name="format"></a>형식일

8-9자리 문자 및 숫자와 마지막 문자를 선택적 괄호로 묶어서 조합

### <a name="pattern"></a>패턴

8-9자리 문자 조합:
- 1-2개 문자(대/소문자 구분 안 함) 
- 6자리 숫자 
- 검사 숫자에 해당하고 선택적으로 괄호로 묶는 마지막 문자(임의 숫자 또는 문자 A)

### <a name="checksum"></a>제외

예

### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
- Func_hong_kong_id_card 함수가 해당 패턴과 일치 하는 콘텐츠를 찾습니다.
- Keyword_hong_kong_id_card에서 키워드가 발견 되었습니다.
- 체크섬이 통과됩니다.

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 65% 신뢰합니다.
- Func_hong_kong_id_card 함수가 해당 패턴과 일치 하는 콘텐츠를 찾습니다.
- 체크섬이 통과됩니다.

```
<!-- Hong Kong Identity Card (HKID) number -->
<Entity id="e63c28a7-ad29-4c17-a41a-3d2a0b70fd9c" recommendedConfidence="75" patternsProximity="300">
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Func_hong_kong_id_card"/>
     <Match idRef="Keyword_hong_kong_id_card"/>
  </Pattern>
  <Pattern confidenceLevel="65">
     <IdMatch idRef="Func_hong_kong_id_card"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a>키워드

#### <a name="keywordhongkongidcard"></a>Keyword_hong_kong_id_card

- 홍콩 특별 식별자 카드
- HKIDC
- id card
- identity card
- zh-hk id 카드
- 홍콩 id
- 香港身份證
- 香港永久性居民身份證
- 身份證
- 身份証
- 身分證
- 身分証
- 香港身份証
- 香港身分證
- 香港身分証
- 香港身份證
- 香港居民身份證
- 香港居民身份証
- 香港居民身分證
- 香港居民身分証
- 香港永久性居民身份証
- 香港永久性居民身分證
- 香港永久性居民身分証
- 香港永久性居民身份證
- 香港非永久性居民身份證
- 香港非永久性居民身份証
- 香港非永久性居民身分證
- 香港非永久性居民身分証
- 香港特別行政區永久性居民身份證
- 香港特別行政區永久性居民身份証
- 香港特別行政區永久性居民身分證
- 香港特別行政區永久性居民身分証
- 香港特別行政區非永久性居民身份證
- 香港特別行政區非永久性居民身份証
- 香港特別行政區非永久性居民身分證
- 香港特別行政區非永久性居民身分証
   
## <a name="india-permanent-account-number-pan"></a>인도 PAN(영구 계정 번호)

### <a name="format"></a>형식일

10자리 문자 또는 숫자

### <a name="pattern"></a>패턴

10자리 문자 또는 숫자:
- 5개 문자(대/소문자 구분 안 함)  
- 4자리 숫자 
- 알파벳 검사 숫자에 해당하는 문자 1개

### <a name="checksum"></a>제외

예

### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.
- 정규식 Regex_india_permanent_account_number 해당 패턴과 일치 하는 콘텐츠를 찾습니다.
- Keyword_india_permanent_account_number에서 키워드가 발견 되었습니다.
- 체크섬이 통과됩니다.

```
<!-- India Permanent Account Number -->
<Entity id="2602bfee-9bb0-47a5-a7a6-2bf3053e2804" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Regex_india_permanent_account_number"/>
     <Match idRef="Keyword_india_permanent_account_number"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a>키워드

#### <a name="keywordindiapermanentaccountnumber"></a>Keyword_india_permanent_account_number

- Permanent Account Number 
- 확대 
   
## <a name="india-unique-identification-aadhaar-number"></a>인도 고유 ID(Aadhaar) 번호

### <a name="format"></a>형식일

선택적 공백 또는 대시를 포함하는 12자리 숫자

### <a name="pattern"></a>패턴

12자리 숫자:
- 4자리 숫자 
- 선택적 공백 또는 대시  
- 4자리 숫자 
- 선택적 공백 또는 대시  
- 검사 숫자에 해당하는 마지막 숫자

### <a name="checksum"></a>제외

예

### <a name="definition"></a>정의

DLP 정책은 300 문자 근사에서 Func_india_aadhaar 함수가 해당 패턴과 일치 하는 콘텐츠를 발견 하는 경우이 유형의 중요 한 정보를 검색 한다는 것을 85% 확신 합니다.
Keyword_india_aadhar에서 키워드가 발견 되었습니다.
체크섬이 통과됩니다.
DLP 정책은 300 문자 근사에서 Func_india_aadhaar 함수가 해당 패턴과 일치 하는 콘텐츠를 발견 하는 경우이 유형의 중요 한 정보를 검색 한다는 것을 75% 확신 합니다.
체크섬이 통과됩니다.
<!-- India Unique Identification (Aadhaar) number -->
<Entity id="1ca46b29-76f5-4f46-9383-cfa15e91048f" recommendedConfidence="85" patternsProximity="300"> <Pattern confidenceLevel="85"> <IdMatch idRef="Func_india_aadhaar"/> <Match idRef="Keyword_india_aadhar"/> </Pattern> <Pattern confidenceLevel="75"> <IdMatch idRef="Func_india_aadhaar"/> </Pattern>
</Entity>

### <a name="keywords"></a>키워드
   
#### <a name="keywordindiaaadhar"></a>Keyword_india_aadhar
- Aadhar
- Aadhaar
- UID
- आधार
   
## <a name="indonesia-identity-card-ktp-number"></a>인도네시아 ID 카드(KTP) 번호

### <a name="format"></a>형식일

선택적으로 마침표를 포함하는 16자리 숫자

### <a name="pattern"></a>패턴

16자리 숫자:
- 2자리 시/도 코드  
- 마침표(옵션)  
- 2자리 지역 또는 구/군/시 코드  
- 2자리 소구역 코드  
- 마침표(옵션)  
- 생년월일에 해당하는 DDMMYY 형식의 6자리 숫자  
- 마침표(옵션)  
- 4자리 숫자

### <a name="checksum"></a>제외

아니요

### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
- 정규식 Regex_indonesia_id_card 해당 패턴과 일치 하는 콘텐츠를 찾습니다.
- Keyword_indonesia_id_card에서 키워드가 발견 되었습니다.

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
- 정규식 Regex_indonesia_id_card 해당 패턴과 일치 하는 콘텐츠를 찾습니다.

```
<!-- Indonesia Identity Card (KTP) Number -->
<Entity id="da68fdb0-f383-4981-8c86-82689d3b7d55" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Regex_indonesia_id_card"/>
     <Match idRef="Keyword_indonesia_id_card"/>
  </Pattern>
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Regex_indonesia_id_card"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a>키워드
   
#### <a name="keywordindonesiaidcard"></a>Keyword_indonesia_id_card

- KTP
- Kartu Tanda Penduduk 
- Nomor Induk Kependudukan 
   
## <a name="international-banking-account-number-iban"></a>IBAN(국제 은행 계좌 번호)

### <a name="format"></a>형식일

국가 코드 (두 문자) + 검사 숫자 (2 자리 숫자)와 bban 숫자 (최대 30 자)

### <a name="pattern"></a>패턴

패턴에는 다음이 모두 포함되어야 합니다.

- 두 글자로 된 국가 코드
- 두 개의 검사 숫자 (선택적 공백) 
- 1-7 개 문자 또는 숫자의 그룹 (공백으로 구분 가능)
- 1-3 문자 또는 숫자

각 국가의 형식은 약간 다릅니다. iban 중요 한 정보 유형은 다음과 같은 60 국가를 포함 합니다.

ad, ae, al, at, az, ba, be, bg, bh, ch, cr, cy, cz, de, kw, hu,, to,,, fr,,, i,,, ie, il, is,, l,, 5, 60, md, me, mk, e, mt, mu , nl-nl, no, pl, pt, ro, rs, sa, se, si,, sm, tn, tr, vg

### <a name="checksum"></a>제외

예

### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.
- Func_iban 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.
- 체크섬이 통과됩니다.

```
<Entity id="e7dc4711-11b7-4cb0-b88b-2c394a771f0e" patternsProximity="300" recommendedConfidence="85">
  <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_iban" />
  </Pattern>
</Entity>
```

### <a name="keywords"></a>키워드

없음

   
## <a name="ip-address"></a>IP 주소

### <a name="format"></a>형식일

#### <a name="ipv4"></a>IPv4
IPv4 주소의 서식 있는 버전(마침표 있음) 및 서식 없는 버전(마침표 없음)으로 구성된 복잡한 패턴

#### <a name="ipv6"></a>IPv6
서식 있는(콜론 포함) IPv6 번호로 구성된 복잡한 패턴

### <a name="pattern"></a>패턴

### <a name="checksum"></a>제외

아니요

### <a name="definition"></a>정의

IPv6의 경우 DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.
- Regex_ipv6_address 정규식이 해당 패턴과 일치하는 콘텐츠를 찾습니다.
- Keyword_ipaddress의 키워드가 발견되지 않았습니다.

IPv4의 경우 DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 95% 신뢰합니다.
- Regex_ipv4_address 정규식이 해당 패턴과 일치하는 콘텐츠를 찾습니다.
- Keyword_ipaddress의 키워드가 발견되었습니다.

IPv6의 경우 DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 95% 신뢰합니다.
- Regex_ipv6_address 정규식이 해당 패턴과 일치하는 콘텐츠를 찾습니다.
- Keyword_ipaddress의 키워드가 발견되지 않았습니다.

```
    <!-- IP Address -->
    <Entity id="1daa4ad5-e2dd-4ca4-a788-54722c09efb2" patternsProximity="300" recommendedConfidence="85">
      <Pattern confidenceLevel="85">
        <IdMatch idRef="Regex_ipv6_address" />
        <Any minMatches="0" maxMatches="0">
          <Match idRef="Keyword_ipaddress" />
        </Any>
      </Pattern>
      <Pattern confidenceLevel="95">
        <IdMatch idRef="Regex_ipv4_address" />
        <Any minMatches="1">
          <Match idRef="Keyword_ipaddress" />
        </Any>
      </Pattern>
      <Pattern confidenceLevel="95">
        <IdMatch idRef="Regex_ipv6_address" />
        <Any minMatches="1">
          <Match idRef="Keyword_ipaddress" />
        </Any>
      </Pattern>
    </Entity>
```

### <a name="keywords"></a>키워드

#### <a name="keywordipaddress"></a>Keyword_ipaddress

- IP(이 키워드는 대/소문자를 구분함)
- ip address 
- ip addresses
- internet protocol
- IP-כתובת ה 
   
## <a name="international-classification-of-diseases-icd-10-cm"></a>Diseases의 국제 분류 (ICD-10-CM)

### <a name="format"></a>형식일

사전

### <a name="pattern"></a>패턴

Keyword

### <a name="checksum"></a>제외

아니요

### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.
- Dictionary_icd_10_cm에서 키워드가 발견 되었습니다.

```
      <!-- ICD-10 CM -->
      <Entity id="3356946c-6bb7-449b-b253-6ffa419c0ce7" patternsProximity="300" recommendedConfidence="85">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Dictionary_icd_10_cm" />
        </Pattern>
      </Entity>
```

키워드

Dictionary_icd_10_cm 키워드 사전의 모든 용어 이며, [Diseases의 국제 분류, 10 번째 수정, 임상 수정 (icd-10-cm)](https://go.microsoft.com/fwlink/?linkid=852604)을 기반으로 합니다. 이 유형은 보험 코드가 아니라 용어에 대해서만 찾습니다.

   
## <a name="international-classification-of-diseases-icd-9-cm"></a>Diseases의 국제 분류 (ICD-9-CM)

### <a name="format"></a>형식일

사전

### <a name="pattern"></a>패턴

Keyword

### <a name="checksum"></a>제외

아니요

### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.
- Dictionary_icd_9_cm에서 키워드가 발견 되었습니다.

```
      <Entity id="fa3f9c74-ee07-4c52-b5f2-085d6b2c0ec4" patternsProximity="300" recommendedConfidence="85">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Dictionary_icd_9_cm" />
        </Pattern>
      </Entity>
```

### <a name="keywords"></a>키워드

[Diseases의 국가별 분류, 9 번째 버전의 임상 수정 (icd-9cm)](https://go.microsoft.com/fwlink/?linkid=852605)을 기반으로 하는 Dictionary_icd_9_cm 키워드 사전의 모든 용어입니다. 이 유형은 보험 코드가 아니라 용어에 대해서만 찾습니다.
   
## <a name="ireland-personal-public-service-pps-number"></a>아일랜드 PPS(개인 공공 서비스) 번호

### <a name="format"></a>형식일

이전 형식 (31 년 12 월 2012 일까지):
- 7자리 숫자와 1-2개 문자  

새 형식 (1 년 1 월 2013 및 이후):
- 7자리 숫자와 2개 문자

### <a name="pattern"></a>패턴

이전 형식 (31 년 12 월 2012 일까지):
- 7자리 숫자 
- 1-2개 문자(대/소문자 구분 안 함) 

새 형식 (1 년 1 월 2013 및 이후):
- 7자리 숫자 
- 알파벳 검사 숫자에 해당하는 문자 1개(대/소문자 구분 안 함)  
- 문자 "A" 또는 "H"(대/소문자 구분 안 함)

### <a name="checksum"></a>제외

예

### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.
- Func_ireland_pps 함수가 해당 패턴과 일치 하는 콘텐츠를 찾습니다.
- 다음 중 하나가 충족됩니다.
    - Keyword_ireland_pps에서 키워드가 발견 되었습니다.
    - Func_eu_date 함수가 올바른 날짜 형식의 날짜를 찾습니다.
- 체크섬이 통과됩니다.

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 65% 신뢰합니다.
- Func_ireland_pps 함수가 해당 패턴과 일치 하는 콘텐츠를 찾습니다.
- 체크섬이 통과됩니다.

```
<!-- Ireland Personal Public Service (PPS) Number -->
<Entity id="1cdb674d-c19a-4fcf-9f4b-7f56cc87345a" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Func_ireland_pps"/>
     <Any minMatches="1">
  <Match idRef="Keyword_ireland_pps"/>
  <Match idRef="Func_eu_date"/>
     </Any>
  </Pattern>
  <Pattern confidenceLevel="65">
     <IdMatch idRef="Func_ireland_pps"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a>키워드

#### <a name="keywordirelandpps"></a>Keyword_ireland_pps

- Personal Public Service Number 
- PPS Number 
- PPS Num 
- PPS No. 
- PPS # 
- .pps 
- ppsn 
- Public Services Card 
- Uimhir Phearsanta Seirbhíse Poiblí 
- uimh PSP 
- PSP 
   
## <a name="israel-bank-account-number"></a>이스라엘 은행 계좌 번호

### <a name="format"></a>형식일

13자리 숫자

### <a name="pattern"></a>패턴

서식이
- 2자리 숫자 
- 대시 1개 
- 3자리 숫자 
- 대시 1개 
- 8자리 숫자

서식
- 13자리 연속 숫자

### <a name="checksum"></a>제외

아니요

### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
- Regex_israel_bank_account_number 정규식이 해당 패턴과 일치하는 콘텐츠를 찾습니다.
- Keyword_israel_bank_account_number의 키워드가 발견되었습니다.

```
<!-- Israel Bank Account Number -->
<Entity id="7d08b2ff-a0b9-437f-957c-aeddbf9b2b25" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Regex_israel_bank_account_number" />
        <Any minMatches="1">
          <Match idRef="Keyword_israel_bank_account_number" />
        </Any>
    </Pattern>
</Entity>
```

### <a name="keywords"></a>키워드

#### <a name="keywordisraelbankaccountnumber"></a>Keyword_israel_bank_account_number

- Bank Account Number 
- Bank Account 
- Account Number 
- מספר חשבון בנק 
   
## <a name="israel-national-id"></a>이스라엘 국가 ID

### <a name="format"></a>형식일

9자리 숫자

### <a name="pattern"></a>패턴

9자리 연속 숫자

### <a name="checksum"></a>제외

예

### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
- Func_israeli_national_id_number 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.
- Keyword_Israel_National_ID의 키워드가 발견되었습니다.
- 체크섬이 통과됩니다.

```
<!-- Israel National ID Number -->
<Entity id="e05881f5-1db1-418c-89aa-a3ac5c5277ee" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_israeli_national_id_number" />
        <Any minMatches="1">
          <Match idRef="Keyword_Israel_National_ID" />
        </Any>
    </Pattern>
</Entity>
```

### <a name="keywords"></a>키워드

#### <a name="keywordisraelnationalid"></a>Keyword_Israel_National_ID

- מספר זהות 
- National ID Number
   
## <a name="italy-drivers-license-number"></a>이탈리아 운전 면허 번호

### <a name="format"></a>형식일

10개의 문자 및 숫자 조합

### <a name="pattern"></a>패턴

- 10개의 문자 및 숫자 조합:
- 1개 문자(대/소문자 구분 안 함) 
- 문자 "A" 또는 "V"(대/소문자 구분 안 함) 
- 7개 문자(대/소문자 구분 안 함), 숫자 또는 밑줄 문자 
- 1개 문자(대/소문자 구분 안 함)

### <a name="checksum"></a>제외

아니요

### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
- Regex_italy_drivers_license_number 정규식이 해당 패턴과 일치하는 콘텐츠를 찾습니다.
- Keyword_italy_drivers_license_number의 키워드가 발견되었습니다.

```
<!-- Italy Driver's license Number -->
<Entity id="97d6244f-9157-41bd-8e0c-9d669a5c4d71" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Regex_italy_drivers_license_number" />
        <Any minMatches="1">
          <Match idRef="Keyword_italy_drivers_license_number" />
        </Any>
    </Pattern>
</Entity>
```

### <a name="keywords"></a>키워드

#### <a name="keyworditalydriverslicensenumber"></a>Keyword_italy_drivers_license_number

- numero di patente di guida 
- patente di guida 
   
## <a name="japan-bank-account-number"></a>일본 은행 계좌 번호

### <a name="format"></a>형식일

7 또는 8자리 숫자

### <a name="pattern"></a>패턴

은행 계좌 번호:
- 7 또는 8자리 숫자
- 은행 계좌 지점 코드:
- 4자리 숫자 
- 공백 또는 대시(선택 사항) 
- 3자리 숫자

제외

아니요

### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.
- Func_jp_bank_account 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.
- Keyword_jp_bank_account의 키워드가 발견되었습니다.
- 다음 중 하나가 충족됩니다.
- Func_jp_bank_account_branch_code 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.
- Keyword_jp_bank_branch_code의 키워드가 발견되었습니다.

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
- Func_jp_bank_account 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.
- Keyword_jp_bank_account의 키워드가 발견되었습니다.

```
<!-- Japan Bank Account Number -->
<Entity id="d354f95b-96ee-4b80-80bc-4377312b55bc" patternsProximity="300" recommendedConfidence="75">
  <Version minEngineVersion="15.01.0131.000">
    <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_jp_bank_account" />
          <Match idRef="Keyword_jp_bank_account" />
          <Any minMatches="1">
            <Match idRef="Func_jp_bank_account_branch_code" />
            <Match idRef="Keyword_jp_bank_branch_code" />
          </Any>
      </Pattern>
  </Version>    
     <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_jp_bank_account" />
        <Match idRef="Keyword_jp_bank_account" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a>키워드

#### <a name="keywordjpbankaccount"></a>Keyword_jp_bank_account

- Checking Account Number 
- Checking Account 
- Checking Account # 
- Checking Acct Number 
- Checking Acct # 
- Checking Acct No. 
- Checking Account No. 
- Bank Account Number 
- Bank Account 
- Bank Account # 
- Bank Acct Number 
- Bank Acct # 
- Bank Acct No. 
- Bank Account No. 
- Savings Account Number 
- Savings Account 
- Savings Account # 
- Savings Acct Number 
- Savings Acct # 
- Savings Acct No. 
- Savings Account No. 
- Debit Account Number 
- Debit Account 
- Debit Account # 
- Debit Acct Number 
- Debit Acct # 
- Debit Acct No. 
- Debit Account No. 
- 口座番号を当座預金口座の確認 
- #アカウントの確認 、 勘定番号の確認 
- #勘定の確認 
- 勘定番号の確認 
- 口座番号の確認 
- 銀行口座番号 
- 銀行口座 
- 銀行口座 # 
- 銀行の勘定番号 
- 銀行のacct # 
- 銀行の勘定いいえ 
- 銀行口座番号
- 普通預金口座番号 
- 預金口座 
- 貯蓄口座 # 
- 貯蓄勘定の数 
- 貯蓄勘定 # 
- 貯蓄勘定番号 
- 普通預金口座番号 
- 引き落とし口座番号 
- 口座番号 
- 口座番号 # 
- デビットのacct番号 
- デビット勘定 # 
- デビットACCTの番号 
- デビット口座番号 

#### <a name="keywordjpbankbranchcode"></a>Keyword_jp_bank_branch_code

Otemachi

## <a name="japan-drivers-license-number"></a>일본 운전 면허 번호

### <a name="format"></a>형식일

12자리 숫자

### <a name="pattern"></a>패턴

12자리 연속 숫자

### <a name="checksum"></a>제외

아니요

### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
- Func_jp_drivers_license_number 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.
- Keyword_jp_drivers_license_number의 키워드가 발견되었습니다.

```
<!-- Japan Driver's License Number -->
<Entity id="c6011143-d087-451c-8313-7f6d4aed2270" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_jp_drivers_license_number" />
        <Match idRef ="Keyword_jp_drivers_license_number" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a>키워드

#### <a name="keywordjpdriverslicensenumber"></a>Keyword_jp_drivers_license_number

- dl 
- DL 
- 된다 
- 된다 
- driver license 
- driver licenses 
- drivers license 
- driver's license 
- drivers licenses 
- driver's licenses 
- driving licence 
- lic 
- LIC 
- driver'lics 
- state id 
- state identification 
- state identification number 
- 低所得国 # 
- 免許証 
- 状態ID
- 状態の識別 
- 状態の識別番号 
- 運転免許 
- 運転免許証 
- 運転免許証番号 
   
## <a name="japan-passport-number"></a>일본 여권 번호

### <a name="format"></a>형식일

2개 문자와 7자리 숫자

### <a name="pattern"></a>패턴

2개의 문자(대/소문자 구분 안 함)와 7자리 숫자

### <a name="checksum"></a>제외

아니요

### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
- Func_jp_passport 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.
- Keyword_jp_passport의 키워드가 발견되었습니다.

```
<!-- Japan Passport Number -->
<Entity id="75177310-1a09-4613-bf6d-833aae3743f8" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_jp_passport" />
        <Match idRef="Keyword_jp_passport" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a>키워드

#### <a name="keywordjppassport"></a>Keyword_jp_passport

- パスポート 
- パスポート番号 
- パスポートのNum 
- パスポート # 
   
## <a name="japan-resident-registration-number"></a>일본 주민 등록 번호

### <a name="format"></a>형식일

11자리 숫자

### <a name="pattern"></a>패턴

11자리 연속 숫자

### <a name="checksum"></a>제외

아니요

### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
- Func_jp_resident_registration_number 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.
- Keyword_jp_resident_registration_number의 키워드가 발견되었습니다.

```
<!-- Japan Resident Registration Number -->
<Entity id="01c1209b-6389-4faf-a5f8-3f7e13899652" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_jp_resident_registration_number" />
        <Match idRef ="Keyword_jp_resident_registration_number" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a>키워드

#### <a name="keywordjpresidentregistrationnumber"></a>Keyword_jp_resident_registration_number

- Resident Registration Number
- Resident Register Number 
- Residents Basic Registry Number 
- Resident Registration No. 
- Resident Register No. 
- Residents Basic Registry No. 
- Basic Resident Register No. 
- 住民登録番号 、 登録番号をレジデント 
- 住民基本登録番号 、 登録番号 
- 住民基本レジストリ番号を常駐 
- 登録番号を常駐住民基本台帳登録番号 

   
## <a name="japan-social-insurance-number-sin"></a>일본 SIN(사회 보험 번호)

### <a name="format"></a>형식일

7-12자리 숫자

### <a name="pattern"></a>패턴

7-12자리 숫자:
- 4자리 숫자 
- 하이픈 1개(선택 사항) 
- 6 자리 숫자 또는
- 7-12자리 연속 숫자

### <a name="checksum"></a>제외

아니요

### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.
- Func_jp_sin 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.
- Keyword_jp_sin의 키워드가 발견되었습니다.

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
- Func_jp_sin_pre_1997 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.
- Keyword_jp_sin의 키워드가 발견되었습니다.

```
<!-- Japan Social Insurance Number -->
<Entity id="c840e719-0896-45bb-84fd-1ed5c95e45ff" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_jp_sin" />
        <Match idRef="Keyword_jp_sin" />
    </Pattern>
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_jp_sin_pre_1997" />
        <Match idRef="Keyword_jp_sin" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a>키워드

#### <a name="keywordjpsin"></a>Keyword_jp_sin

- Social Insurance No. 
- Social Insurance Num 
- Social Insurance Number 
- 社会保険のテンキー 
- 社会保険番号 

## <a name="japanese-residence-card-number"></a>일본어 거주지 카드 번호

### <a name="format"></a>형식일

12 개의 문자 및 숫자

### <a name="pattern"></a>패턴

12 개의 문자 및 숫자:
- 2문자(대/소문자 구분 안 함)
- 8자리 숫자 
- 2문자(대/소문자 구분 안 함)

### <a name="checksum"></a>제외

아니요

### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
- 정규식 Regex_jp_residence_card_number 해당 패턴과 일치 하는 콘텐츠를 찾습니다.
- Keyword_jp_residence_card_number에서 키워드가 발견 되었습니다.

```
<!--Japan Residence Card Number-->
-<Entity id="ac36fef2-a289-4e2c-bb48-b02366e89fc0" recommendedConfidence="75" patternsProximity="300">
   -<Pattern confidenceLevel="75">
      <IdMatch idRef="Regex_jp_residence_card_number"/>
      <Match idRef="Keyword_jp_residence_card_number"/>
   </Pattern>
</Entity>
```

### <a name="keywords"></a>키워드

#### <a name="keywordjpresidencecardnumber"></a>Keyword_jp_residence_card_number

- 거주지 카드 번호
- 거주지 카드 아니요
- 거주지 카드 #
- 在留カード番号
   
## <a name="malaysia-id-card-number"></a>말레이시아 ID 카드 번호

### <a name="format"></a>형식일

선택적으로 하이픈을 포함하는 12자리 숫자

### <a name="pattern"></a>패턴

12자리 숫자:
- 생년월일에 해당하는 YYMMDD 형식의 6자리 숫자  
- 대시(옵션) 
- 2개 문자로 이루어진 출생지 코드  
- 대시(옵션) 
- 임의의 3자리 숫자  
- 1자리 성별 코드

### <a name="checksum"></a>제외

아니요

### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.
- 정규식 Regex_malaysia_id_card_number 해당 패턴과 일치 하는 콘텐츠를 찾습니다.
- Keyword_malaysia_id_card_number에서 키워드가 발견 되었습니다.

```
<!-- Malaysia ID Card Number -->
</Entity>
      <Entity id="7f0e921c-9677-435b-aba2-bb8f1013c749" patternsProximity="300" recommendedConfidence="85">
        <Pattern confidenceLevel="85">
            <IdMatch idRef="Regex_malaysia_id_card_number" />
            <Match idRef="Keyword_malaysia_id_card_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>키워드
   
#### <a name="keywordmalaysiaidcardnumber"></a>Keyword_malaysia_id_card_number

- 디지털 응용 프로그램 카드
- i/c
- i/c 아니요
- 비용
- ic 아니요
- id card
- 식별 카드
- identity card
- k/p
- k/p 아니요
- kad akuan diri
- kad aplikasi 디지털
- kad pengenalan 말레이시아
- kp
- kp 아니요
- mykad
- mykas
- mykid
- mypr
- myta
- 말레이시아 id 카드
- 말레이지아 id 카드
- nric
- 개인 식별 카드
   
## <a name="netherlands-citizens-service-bsn-number"></a>네덜란드 시민 서비스(BSN) 번호

### <a name="format"></a>형식일

선택적으로 공백을 포함하는 8-9자리 숫자

### <a name="pattern"></a>패턴

8-9자리 숫자:
- 3자리 숫자 
- 공백 1개(선택 사항) 
- 3자리 숫자 
- 공백 1개(선택 사항) 
- 2-3자리 숫자

### <a name="checksum"></a>제외

예

### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.
- Func_netherlands_bsn 함수가 해당 패턴과 일치 하는 콘텐츠를 찾습니다.
- Keyword_netherlands_bsn에서 키워드가 발견 되었습니다.
- Func_eu_date2 함수가 올바른 날짜 형식의 날짜를 찾습니다.
- 체크섬이 통과됩니다.

```
<!-- Netherlands Citizen's Service (BSN) Number -->
<Entity id="c5f54253-ef7e-44f6-a578-440ed67e946d" patternsProximity="300" recommendedConfidence="85">
  <Pattern confidenceLevel="85">
       <IdMatch idRef="Func_netherlands_bsn" /> 
       <Match idRef="Keyword_netherlands_bsn" /> 
       <Match idRef="Func_eu_date2" /> 
  </Pattern>
</Entity>
```

### <a name="keywords"></a>키워드

#### <a name="keywordnetherlandsbsn"></a>Keyword_netherlands_bsn

- Citizen service number 
- BSN 
- Burgerservicenummer 
- Sofinummer 
- Persoonsgebonden nummer 
- Persoonsnummer    

   
## <a name="new-zealand-ministry-of-health-number"></a>뉴질랜드 보건부 번호

### <a name="format"></a>형식일

3개 문자, 공백 1개(선택 사항) 및 4자리 숫자

### <a name="pattern"></a>패턴

3 개의 문자 (대/소문자 구분 안 함) 공백 (선택 사항) 4 자리 숫자

### <a name="checksum"></a>제외

예

### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.
- Func_new_zealand_ministry_of_health_number 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.
- Keyword_nz_terms의 키워드가 발견되었습니다.
- 체크섬이 통과됩니다.

```
<!-- New Zealand Health Number -->
<Entity id="2b71c1c8-d14e-4430-82dc-fd1ed6bf05c7" patternsProximity="300" recommendedConfidence="85">
    <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_new_zealand_ministry_of_health_number" />
        <Any minMatches="1">
          <Match idRef="Keyword_nz_terms" />
        </Any>
    </Pattern>
</Entity>
```

키워드

Keyword_nz_terms

- nhi 
- New Zealand 
- 상태 
- 처리가 
   
## <a name="norway-identification-number"></a>Norway Identification Number

### <a name="format"></a>형식일

11자리 숫자

### <a name="pattern"></a>패턴

11자리 숫자:
- 생년월일에 해당하는 DDMMYY 형식의 6자리 숫자  
- 3자리 개인 번호  
- 2개의 검사 숫자

### <a name="checksum"></a>제외

예

### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.
- Func_norway_id_number 함수가 해당 패턴과 일치 하는 콘텐츠를 찾습니다.
- Keyword_norway_id_number에서 키워드가 발견 되었습니다.
- 체크섬이 통과됩니다.
- DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
- Func_norway_id_numbe 함수가 해당 패턴과 일치 하는 콘텐츠를 찾습니다.
- 체크섬이 통과됩니다.

```
<!-- Norway Identification Number -->
<Entity id="d4c8a798-e9f2-4bd3-9652-500d24080fc3" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Func_norway_id_number"/>
     <Match idRef="Keyword_norway_id_number"/>
  </Pattern>
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Func_norway_id_number"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a>키워드

#### <a name="keywordnorwayidnumber"></a>Keyword_norway_id_number

- Personal identification number
- Norwegian ID Number
- ID Number
- 확인과
- Personnummer
- Fødselsnummer

   
## <a name="philippines-unified-multi-purpose-id-number"></a>필리핀 통합 다목적 ID 번호

### <a name="format"></a>형식일

하이픈으로 구분된 12자리 숫자

### <a name="pattern"></a>패턴

12자리 숫자:
- 4자리 숫자 
- 하이픈 
- 7자리 숫자 
- 하이픈 
- 1자리 숫자

### <a name="checksum"></a>제외

아니요

### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
- 정규식 Regex_philippines_unified_id 해당 패턴과 일치 하는 콘텐츠를 찾습니다.
- Keyword_philippines_id에서 키워드가 발견 되었습니다.

```
<!-- Philippines Unified Multi-Purpose ID number -->
<Entity id="019b39dd-8c25-4765-91a3-d9c6baf3c3b3" recommendedConfidence="75" patternsProximity="300">
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Regex_philippines_unified_id"/>
     <Match idRef="Keyword_philippines_id"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a>키워드
   
#### <a name="keywordphilippinesid"></a>Keyword_philippines_id

- Unified Multi-Purpose ID 
- UMID 
- Identity Card 
- Pinag-isang Multi-Layunin ID
   
## <a name="poland-identity-card"></a>폴란드 ID 카드

### <a name="format"></a>형식일

3개의 문자 및 6자리 숫자

### <a name="pattern"></a>패턴

3개의 문자(대/소문자 구분 안 함)와 6자리 숫자

### <a name="checksum"></a>제외

예

### <a name="definition"></a>정의

DLP 정책은 300 문자 근사에서 Func_polish_national_id 함수가 해당 패턴과 일치 하는 콘텐츠를 발견 하는 경우이 유형의 중요 한 정보를 검색 한다는 것을 75% 확신 합니다.
Keyword_polish_national_id_passport_number의 키워드가 발견되었습니다.
체크섬이 통과됩니다.

```
<!-- Poland Identity Card-->
<Entity id="25E64989-ED5D-40CA-A939-6C14183BB7BF" patternsProximity="300" recommendedConfidence="85">
      <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_polish_national_id" />
          <Match idRef="Keyword_polish_national_id_passport_number" />
      </Pattern>
</Entity>
```

### <a name="keywords"></a>키워드

#### <a name="keywordpolishnationalidpassportnumber"></a>Keyword_polish_national_id_passport_number

- Dowód osobisty
- u r i dowodu osobistego
- Nazwa i u r i dowodu osobistego
- Nazwa i veiligheid dowodu osobistego
- Nazwa i nr dowodu tożsamości
- Dowód Tożsamości
- dow. 르.

   
## <a name="poland-national-id-pesel"></a>폴란드 국가 ID(PESEL)

### <a name="format"></a>형식일

11자리 숫자

### <a name="pattern"></a>패턴

11자리 연속 숫자

### <a name="checksum"></a>제외

예

### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.
- Func_pesel_identification_number 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.
- Keyword_pesel_identification_number의 키워드가 발견되었습니다.
- 체크섬이 통과됩니다.

```
<!-- Poland National ID (PESEL) -->      
<Entity id="E3AAF206-4297-412F-9E06-BA8487E22456" patternsProximity="300" recommendedConfidence="85">
      <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_pesel_identification_number" />
          <Match idRef="Keyword_pesel_identification_number" />
      </Pattern>
</Entity>
```

### <a name="keywords"></a>키워드

#### <a name="keywordpeselidentificationnumber"></a>Keyword_pesel_identification_number

- Nr PESEL
- PESEL   

   
## <a name="poland-passport"></a>폴란드 여권

### <a name="format"></a>형식일

2개 문자와 7자리 숫자

### <a name="pattern"></a>패턴

2개의 문자(대/소문자 구분 안 함)와 7자리 숫자

### <a name="checksum"></a>제외

예

### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.
- Func_polish_passport_number 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.
- Keyword_polish_national_id_passport_number의 키워드가 발견되었습니다.
- 체크섬이 통과됩니다.

```
<!-- Poland Passport Number -->
<Entity id="03937FB5-D2B6-4487-B61F-0F8BFF7C3517" patternsProximity="300" recommendedConfidence="85">
      <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_polish_passport_number" />
          <Match idRef="Keyword_polish_national_id_passport_number" />
      </Pattern>
</Entity>
</Version>
```

### <a name="keywords"></a>키워드

#### <a name="keywordpolishnationalidpassportnumber"></a>Keyword_polish_national_id_passport_number

- u r i (zportu)
- veiligheid. 고 zportu
- 고 zport

   
## <a name="portugal-citizen-card-number"></a>포르투갈 시민 카드 번호

### <a name="format"></a>형식일

8자리 숫자

### <a name="pattern"></a>패턴

8자리 숫자

### <a name="checksum"></a>제외

아니요

### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.
- 정규식 Regex_portugal_citizen_card 해당 패턴과 일치 하는 콘텐츠를 찾습니다.
- Keyword_portugal_citizen_card에서 키워드가 발견 되었습니다.

```
<!-- Portugal Citizen Card Number -->
<Entity id="91a7ece2-add4-4986-9a15-c84544d81ecd" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Regex_portugal_citizen_card"/>
     <Match idRef="Keyword_portugal_citizen_card"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a>키워드

#### <a name="keywordportugalcitizencard"></a>Keyword_portugal_citizen_card

- Citizen Card
- National ID Card
- 참조란
- Cartão de Cidadão
- Bilhete de Identidade
   
## <a name="saudi-arabia-national-id"></a>사우디 아라비아 국가 ID

### <a name="format"></a>형식일

10자리 숫자

### <a name="pattern"></a>패턴

10자리 연속 숫자

### <a name="checksum"></a>제외

아니요

### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
- Regex_saudi_arabia_national_id 정규식이 해당 패턴과 일치하는 콘텐츠를 찾습니다.
- Keyword_saudi_arabia_national_id의 키워드가 발견되었습니다.

```
<!-- Saudi Arabia National ID -->
<Entity id="8c5a0ba8-404a-41a3-8871-746aa21ee6c0" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Regex_saudi_arabia_national_id" />
        <Any minMatches="1">
          <Match idRef="Keyword_saudi_arabia_national_id" />
        </Any>
    </Pattern>
</Entity>
```

### <a name="keywords"></a>키워드

#### <a name="keywordsaudiarabianationalid"></a>Keyword_saudi_arabia_national_id

- Identification Card 
- I card number 
- ID number 
- الوطنية الهوية بطاقة رقم 

   
## <a name="singapore-national-registration-identity-card-nric-number"></a>싱가포르 NRIC(국가 등록 ID 카드) 번호

### <a name="format"></a>형식일

9개의 문자 및 숫자

### <a name="pattern"></a>패턴

- 9개의 문자 및 숫자:
- 문자 "F", "G", "S" 또는 "T"(대/소문자 구분 안 함)  
- 7자리 숫자 
- 알파벳 검사 숫자

### <a name="checksum"></a>제외

예

### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.
- 정규식 Regex_singapore_nric 해당 패턴과 일치 하는 콘텐츠를 찾습니다.
- Keyword_singapore_nric에서 키워드가 발견 되었습니다.
- 체크섬이 통과됩니다.

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
- 정규식 Regex_singapore_nric 해당 패턴과 일치 하는 콘텐츠를 찾습니다.
- 체크섬이 통과됩니다.

```
<!-- Singapore National Registration Identity Card (NRIC) Number -->
<Entity id="cead390a-dd83-4856-9751-fb6dc98c34da" recommendedConfidence="75" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Regex_singapore_nric"/>
     <Match idRef="Keyword_singapore_nric"/>
  </Pattern>
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Regex_singapore_nric"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a>키워드
   
#### <a name="keywordsingaporenric"></a>Keyword_singapore_nric

- National Registration Identity Card 
- Identity Card Number 
- NRIC 
- 비용 
- Foreign Identification Number 
- 삭제할 
- 身份证 
- 身份證 
   
## <a name="south-africa-identification-number"></a>남아프리카 공화국 식별 번호

### <a name="format"></a>형식일

공백을 포함할 수 있는 13자리 숫자

### <a name="pattern"></a>패턴

13자리 숫자:
- 생년월일에 해당하는 YYMMDD 형식의 6자리 숫자  
- 4자리 숫자 
- 1자리 시민권 표시  
- 숫자 "8" 또는 "9"  
- 체크섬 숫자에 해당하는 1자리 숫자

### <a name="checksum"></a>제외

예

### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.
- Func_south_africa_identification_number 함수가 해당 패턴과 일치 하는 콘텐츠를 찾습니다.
- Keyword_south_africa_identification_number에서 키워드가 발견 되었습니다.
- 체크섬이 통과됩니다.

```
<!-- South Africa Identification Number -->
<Entity id="e2adf7cb-8ea6-4048-a2ed-d89eb65f2780" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Func_south_africa_identification_number"/>
     <Match idRef="Keyword_south_africa_identification_number"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a>키워드
   
#### <a name="keywordsouthafricaidentificationnumber"></a>Keyword_south_africa_identification_number

- Identity card
- ID
- 확인과 
   
## <a name="south-korea-resident-registration-number"></a>한국 주민 등록 번호

### <a name="format"></a>형식일

하이픈을 포함하는 13자리 숫자

### <a name="pattern"></a>패턴

13자리 숫자:
- 생년월일에 해당하는 YYMMDD 형식의 6자리 숫자  
- 하이픈 
- 세기 및 성별에 따라 결정되는 1자리 숫자  
- 4자리 출생 지역 코드  
- 앞 번호가 동일한 사람을 구분하기 위해 사용되는 1자리 숫자  
- 검사 숫자

### <a name="checksum"></a>제외

예

### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.
- Func_south_korea_resident_number 함수가 해당 패턴과 일치 하는 콘텐츠를 찾습니다.
- Keyword_south_korea_resident_number에서 키워드가 발견 되었습니다.
- 체크섬이 통과됩니다.

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
- Func_south_korea_resident_number 함수가 해당 패턴과 일치 하는 콘텐츠를 찾습니다.
- 체크섬이 통과됩니다.

```
<!-- South Korea Resident Registration Number -->
<Entity id="5b802e18-ba80-44c4-bc83-bf2ad36ae36a" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Func_south_korea_resident_number"/>
     <Match idRef="Keyword_south_korea_resident_number"/>
  </Pattern>
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Func_south_korea_resident_number"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a>키워드
   
#### <a name="keywordsouthkorearesidentnumber"></a>Keyword_south_korea_resident_number

- National ID card 
- Citizen's Registration Number 
- Jumin deungnok beonho 
- RRN 
- 주민등록번호
   
## <a name="spain-social-security-number-ssn"></a>스페인 SSN(사회 보장 번호)

### <a name="format"></a>형식일

11-12자리 숫자

### <a name="pattern"></a>패턴

11-12 자리 숫자:
- 2자리 숫자 
- 정방향 슬래시 1개(선택 사항) 
- 7-8자리 숫자 
- 정방향 슬래시 1개(선택 사항) 
- 2자리 숫자

### <a name="checksum"></a>제외

예

### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.
- Func_spanish_social_security_number 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.
- 체크섬이 통과됩니다.

```
<!-- Spain SSN -->
<Entity id="5df987c0-8eae-4bce-ace7-b316347f3070" patternsProximity="300" recommendedConfidence="85">
    <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_spanish_social_security_number" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a>키워드

없음

## <a name="sql-server-connection-string"></a>SQL Server 연결 문자열

### <a name="format"></a>형식일

아래 패턴에 설명 된 문자 및 문자열이 뒤에 오는 "user id", "user id", "uid" 또는 "UserId"입니다.

### <a name="pattern"></a>패턴

- 문자열 "user id", "User id", "uid" 또는 "UserId"
- 1-200에서 대/소문자, 숫자, 기호, 특수 문자 또는 공백 사이의 조합
- 문자열 "Password" 또는 "pwd" (여기에서 "pwd" 앞에 소문자 문자가 오지 않음)
- 등호 (=)
- 달러 기호 ($), 백분율 기호 (%, >), 기호 (@), 따옴표 ("), 세미콜론 (;), 왼쪽 중괄호 ([) 또는 왼쪽 대괄호 ({))가 아닌 모든 문자
- 세미콜론 (;), 슬래시 (/) 또는 따옴표 (")가 아닌 7-128 문자의 조합
- 세미콜론 (;) 또는 따옴표 (")

### <a name="checksum"></a>제외

아니요

### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.
- 정규식 CEP_Regex_SQLServerConnectionString 해당 패턴과 일치 하는 콘텐츠를 찾습니다.
- CEP_GlobalFilter의 키워드를 찾을 수 **없습니다** .
- CEP_PasswordPlaceHolder 정규식이 해당 패턴과 **** 일치 하는 콘텐츠를 찾지 않습니다.
- CEP_CommonExampleKeywords 정규식이 해당 패턴과 **** 일치 하는 콘텐츠를 찾지 않습니다.

```
<!---SQL Server Connection String>
<Entity id="e76b6205-d3cb-46f2-bd63-c90153f2f97d" patternsProximity="300" recommendedConfidence="85">
  <Pattern confidenceLevel="85">
        <IdMatch idRef="CEP_Regex_SQLServerConnectionString" />
        <Any minMatches="0" maxMatches="0">
            <Match idRef="CEP_GlobalFilter" />
            <Match idRef="CEP_PasswordPlaceHolder" />
            <Match idRef="CEP_CommonExampleKeywords" />
        </Any>
    </Pattern>
</Entity>
```

### <a name="keywords"></a>키워드

#### <a name="cepglobalfilter"></a>CEP_GlobalFilter

- 일부 암호
- somepassword
- secretPassword
- 예

#### <a name="ceppasswordplaceholder"></a>CEP_PasswordPlaceHolder

기술적으로이 중요 한 정보 유형은 키워드 목록이 아니라 정규식을 사용 하 여 이러한 키워드를 식별 합니다.

- 암호나 pwd에 0-2 공백, 등호 (=), 0-2 공백 및 별표 (*)-----------------------
- 암호나 pwd 뒤에 다음이 있습니다.
    - 등호 (=)
    - 보다 작음 기호 (<)
    - 대문자나 소문자, digits, 별표 (*), 하이픈 (-), 밑줄 (_) 또는 공백 문자인 1-200 문자의 조합
    - 기호 보다 큼 (>)

#### <a name="cepcommonexamplekeywords"></a>CEP_CommonExampleKeywords

기술적으로이 중요 한 정보 유형은 키워드 목록이 아니라 정규식을 사용 하 여 이러한 키워드를 식별 합니다.

- 극동
- fabrikam
- 대양
- 샌드박스
- 용 onebox
- 로컬
- 127.0.0.1
- testacs입니다. <!--no-hyperlink-->com
- s-int<!--no-hyperlink-->

## <a name="sweden-national-id"></a>스웨덴 국가 ID

### <a name="format"></a>형식일

10 또는 12자리 숫자와 선택적 구분 기호

### <a name="pattern"></a>패턴

10 또는 12자리 숫자와 선택적 구분 기호:
- 2-4자리 숫자(선택 사항) 
- YYMMDD 날짜 형식의 6자리 숫자 
- 구분 기호 "-" 또는 "+"(선택 사항) 및
- 4자리 숫자

### <a name="checksum"></a>제외

예

### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.
- Func_swedish_national_identifier 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.
- 체크섬이 통과됩니다.

```
<!-- Sweden National ID -->
<Entity id="f69aaf40-79be-4fac-8f05-fd1910d272c8" patternsProximity="300" recommendedConfidence="85">
    <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_swedish_national_identifier" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a>키워드

아니요
   
## <a name="sweden-passport-number"></a>스웨덴 여권 번호

### <a name="format"></a>형식일

8자리 숫자

### <a name="pattern"></a>패턴

8자리 연속 숫자

### <a name="checksum"></a>제외

아니요

### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
- Regex_sweden_passport_number 정규식이 해당 패턴과 일치하는 콘텐츠를 찾습니다.
- 다음 중 하나가 충족됩니다.
    - Keyword_passport의 키워드가 발견되었습니다.
    - Keyword_sweden_passport의 키워드가 발견되었습니다.

```
<!-- Sweden Passport Number -->
<Entity id="ba4e7456-55a9-4d89-9140-c33673553526" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Regex_sweden_passport_number" />
        <Any minMatches="1">
          <Match idRef="Keyword_passport" />
          <Match idRef="Keyword_sweden_passport" />
        </Any>
    </Pattern>
</Entity>
```

### <a name="keywords"></a>키워드
   
#### <a name="keywordswedenpassport"></a>Keyword_sweden_passport

- visa requirements 
- Alien Registration Card 
- Schengen visas 
- Schengen visa 
- Visa Processing 
- Visa Type 
- Single Entry 
- Multiple Entry 
- G3 Processing Fees 

#### <a name="keywordpassport"></a>Keyword_passport

- Passport Number 
- Passport No 
- Passport # 
- 여권 
- PassportID 
- Passportno 
- passportnumber 
- パスポート 
- パスポート番号 
- パスポートのNum 
- パスポート # 
- Numéro de passeport 
- Passeport n ° 
- Passeport Non 
- Passeport # 
- 포트 # 
- 지/포트 아님 
- Passeportn ° 
   
## <a name="swift-code"></a>SWIFT 코드

### <a name="format"></a>형식일

4개의 문자, 5-31개 문자 또는 숫자

### <a name="pattern"></a>패턴

4개의 문자, 5-31개 문자 또는 숫자:
- 4문자 은행 코드(대/소문자 구분 안 함) 
- 선택적 공백 1개 
- 4-28개 문자 또는 숫자[BBAN(기본 은행 계좌 번호)] 
- 선택적 공백 1개 
- 1-3개 문자 또는 숫자(BBAN의 나머지)

### <a name="checksum"></a>제외

아니요

### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
- Regex_swift 정규식이 해당 패턴과 일치하는 콘텐츠를 찾습니다.
- Keyword_swift의 키워드가 발견되었습니다.

```
<Entity id="cb2ab58c-9cb8-4c81-baf8-a4e106791df4" patternsProximity="300" recommendedConfidence="75">
<Pattern confidenceLevel="75">
        <IdMatch idRef="Regex_swift" />
        <Match idRef="Keyword_swift" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a>키워드
   
#### <a name="keywordswift"></a>Keyword_swift

- international organization for standardization 9362 
- iso 9362 
- iso9362 
- swift\# 
- swiftcode 
- swiftnumber 
- swiftroutingnumber 
- swift code 
- swift number # 
- swift routing number 
- bic number 
- bic code 
- bic\# 
- bic\# 
- bank identifier code 
- 標準化 9362 
- 迅速 # 
- SWIFTコード 
- SWIFT番号 
- 迅速なルーティング番号 
- BIC番号 
- BICコード 
- 銀行識別コードのための国際組織 
- Organisation internationale de normalisation 9362 
- rapide\# 
- code SWIFT 
- le numéro de swift 
- swift numéro d'acheminement 
- le numéro BIC 
- \#bic 
- code identificateur de banque 
   
## <a name="taiwan-national-id"></a>대만 국가 ID

### <a name="format"></a>형식일

1개의 문자, 9자리 숫자

### <a name="pattern"></a>패턴

1개의 문자, 9자리 숫자:
- 1개 문자(영문, 대/소문자 구분 안 함) 
- 숫자 "1" 또는 "2" 
- 8자리 숫자

### <a name="checksum"></a>제외

예

### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.
- Func_taiwanese_national_id 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.
- Keyword_taiwanese_national_id의 키워드가 발견되었습니다.
- 체크섬이 통과됩니다.

```
<!-- Taiwanese National ID -->
<Entity id="4C7BFC34-8DD1-421D-8FB7-6C6182C2AF03" patternsProximity="300" recommendedConfidence="85">
      <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_taiwanese_national_id" />
          <Match idRef="Keyword_taiwanese_national_id" />
      </Pattern>
</Entity>
```

### <a name="keywords"></a>키워드

#### <a name="keywordtaiwanesenationalid"></a>Keyword_taiwanese_national_id

- 身份證字號 
- 身份證 
- 身份證號碼 
- 身份證號 
- 身分證字號 
- 身分證 
- 身分證號碼 
- 身份證號 
- 身分證統一編號 
- 國民身分證統一編號 
- 簽名 
- 蓋章 
- 簽名或蓋章 
- 簽章   
   
## <a name="taiwan-passport-number"></a>	대만 여권 번호

### <a name="format"></a>형식일

- 생체 인식 여권 번호: 9 자리 숫자
- 비-생체 인식 여권 번호: 9 자리 숫자

### <a name="pattern"></a>패턴
생체 인식 여권 번호:
- 숫자 "3"  
- 8자리 숫자

비-생체 인식 여권 번호:
- 9자리 숫자

### <a name="checksum"></a>제외

아니요

### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
- 정규식 Regex_taiwan_passport 해당 패턴과 일치 하는 콘텐츠를 찾습니다.
- Keyword_taiwan_passport에서 키워드가 발견 되었습니다.

```
<!-- Taiwan Passport Number -->
<Entity id="e7251cb4-4c2c-41df-963e-924eb3dae04a" recommendedConfidence="75" patternsProximity="300">
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Regex_taiwan_passport"/>
     <Match idRef="Keyword_taiwan_passport"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a>키워드

#### <a name="keywordtaiwanpassport"></a>Keyword_taiwan_passport

- ROC passport number 
- Passport number 
- Passport no 
- Passport Num 
- Passport # 
- 护照 
- 中華民國護照 
- Zhōnghuá Mínguó hùzhào
   
## <a name="taiwan-resident-certificate-arctarc-number"></a>대만 거주 인증(ARC/TARC) 번호

### <a name="format"></a>형식일

10개의 문자 및 숫자

### <a name="pattern"></a>패턴

10개의 문자 및 숫자:
- 2문자(대/소문자 구분 안 함) 
- 8자리 숫자

### <a name="checksum"></a>제외

아니요

### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
- 정규식 Regex_taiwan_resident_certificate 해당 패턴과 일치 하는 콘텐츠를 찾습니다.
- Keyword_taiwan_resident_certificate에서 키워드가 발견 되었습니다.

```
<!-- Taiwan Resident Certificate (ARC/TARC) -->
<Entity id="48269fec-05ea-46ea-b326-f5623a58c6e9" recommendedConfidence="75" patternsProximity="300">
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Regex_taiwan_resident_certificate"/>
     <Match idRef="Keyword_taiwan_resident_certificate"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a>키워드

#### <a name="keywordtaiwanresidentcertificate"></a>Keyword_taiwan_resident_certificate

- Resident Certificate 
- Resident Cert 
- Resident Cert. 
- Identification card 
- Alien Resident Certificate 
- 화살표 
- Taiwan Area Resident Certificate 
- TARC 
- 居留證 
- 外僑居留證 
- 台灣地區居留證 

## <a name="thai-population-identification-code"></a>태국어 인구 식별 코드

### <a name="format"></a>형식일

13자리 숫자

### <a name="pattern"></a>패턴

13자리 숫자:
- 첫 번째 숫자가 0 또는 9가 아님 
- 12자리 숫자

### <a name="checksum"></a>제외

예

### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.
- Func_Thai_Citizen_Id 함수가 해당 패턴과 일치 하는 콘텐츠를 찾습니다.
- Keyword_Thai_Citizen_Id에서 키워드가 발견 되었습니다.

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
- Func_Thai_Citizen_Id 함수가 해당 패턴과 일치 하는 콘텐츠를 찾습니다.

```
<!-- Thai Citizen ID -->
-<Entity id="44ca9e86-ead7-4c5d-884a-e2eaa401515e" recommendedConfidence="75" patternsProximity="300">
   -<Pattern confidenceLevel="85">
      <IdMatch idRef="Func_Thai_Citizen_Id"/>
      <Match idRef="Keyword_Thai_Citizen_Id"/>
   </Pattern>
   -<Pattern confidenceLevel="75">
      <IdMatch idRef="Func_Thai_Citizen_Id"/>
   </Pattern>
</Entity>
```

### <a name="keywords"></a>키워드

#### <a name="keywordthaicitizenid"></a>Keyword_Thai_Citizen_Id

- ID Number
- id 번호
- บัตรประชาชน
- รหัสบัตรประชาชน
- บัตรประชาชน
- รหัสบัตรประชาชน
  
## <a name="turkish-national-identification-number"></a>터키어 국가 식별 번호

### <a name="format"></a>형식일

11자리 숫자

### <a name="pattern"></a>패턴

11자리 숫자

### <a name="checksum"></a>제외

예

### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.
- Func_Turkish_National_Id 함수가 해당 패턴과 일치 하는 콘텐츠를 찾습니다.
- Keyword_Turkish_National_Id에서 키워드가 발견 되었습니다.

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
- Func_Turkish_National_Id 함수가 해당 패턴과 일치 하는 콘텐츠를 찾습니다.

```
<!-- Turkish National Identity -->
-<Entity id="fb621f20-3876-4cfc-acec-8c8e73ca32c7" recommendedConfidence="75" patternsProximity="300">
   -<Pattern confidenceLevel="85">
      <IdMatch idRef="Func_Turkish_National_Id"/>
      <Match idRef="Keyword_Turkish_National_Id"/>
   </Pattern>
   -<Pattern confidenceLevel="75">
      <IdMatch idRef="Func_Turkish_National_Id"/>
   </Pattern>
</Entity>
```

### <a name="keywords"></a>키워드

#### <a name="keywordturkishnationalid"></a>Keyword_Turkish_National_Id

- TC Kimlik 아니요
- TC Kimlik numarası
- Vatandaşlık numarası
- Vatandaşlık 아니요

## <a name="uk-drivers-license-number"></a>영국 운전 면허 번호

### <a name="format"></a>형식일

지정된 형식의 18개 문자 및 숫자 조합

### <a name="pattern"></a>패턴

18개의 문자 및 숫자:
- 5개 문자(대/소문자 구분 안 함) 또는 문자 대신 숫자 "9" 사용 
- 1자리 숫자 
- 생년월일에 대한 DDMMY 날짜 형식의 5자리 숫자 
- 2개 문자(대/소문자 구분 안 함) 또는 문자 대신 숫자 "9" 사용 
- 5자리 숫자

### <a name="checksum"></a>제외

예

### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
- Func_uk_drivers_license 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.
- Keyword_uk_drivers_license의 키워드가 발견되었습니다.
- 체크섬이 통과됩니다.

```
<!-- U.K. Driver's License Number -->
<Entity id="f93de4be-d94c-40df-a8be-461738047551" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_uk_drivers_license" />
        <Match idRef="Keyword_uk_drivers_license" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a>키워드

#### <a name="keywordukdriverslicense"></a>Keyword_uk_drivers_license

- dvla 
- light vans 
- quadbikes 
- motor cars 
- 125cc 
- sidecar 
- tricycles 
- motorcycles 
- photocard licence 
- learner drivers 
- licence holder 
- licence holders 
- driving licences 
- driving licence 
- dual control car 
   
## <a name="uk-electoral-roll-number"></a>영국 선거 롤 번호

### <a name="format"></a>형식일

2개의 문자, 1-4자리 숫자

### <a name="pattern"></a>패턴

2개의 문자(대/소문자 구분 안 함)와 1-4자리 숫자

### <a name="checksum"></a>제외

아니요

### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
- Regex_uk_electoral 정규식이 해당 패턴과 일치하는 콘텐츠를 찾습니다.
- Keyword_uk_electoral의 키워드가 발견되었습니다.

```
<!-- U.K. Electoral Number -->
<Entity id="a3eea206-dc0c-4f06-9e22-aa1be3059963" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Regex_uk_electoral" />
        <Any minMatches="1">
          <Match idRef="Keyword_uk_electoral" />
        </Any>
    </Pattern>
</Entity>
```

### <a name="keywords"></a>키워드

#### <a name="keywordukelectoral"></a>Keyword_uk_electoral

- council nomination 
- nomination form 
- electoral register 
- electoral roll

   
## <a name="uk-national-health-service-number"></a>영국 국립 보건 서비스 번호

### <a name="format"></a>형식일

공백으로 구분된 10-17자리 숫자

### <a name="pattern"></a>패턴

10-17자리 숫자:
- 3 또는 10자리 숫자 
- 공백 
- 3자리 숫자 
- 공백 
- 4자리 숫자

### <a name="checksum"></a>제외

예

### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.
- Func_uk_nhs_number 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.
- 다음 중 하나가 충족됩니다.
    - Keyword_uk_nhs_number의 키워드가 발견되었습니다.
    - Keyword_uk_nhs_number1의 키워드가 발견되었습니다.
    - Keyword_uk_nhs_number_dob의 키워드가 발견되었습니다.
- 체크섬이 통과됩니다.

```
<!-- U.K. NHS Number -->
<Entity id="3192014e-2a16-44e9-aa69-4b20375c9a78" patternsProximity="300" recommendedConfidence="85">
    <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_uk_nhs_number" />
        <Any minMatches="1">
          <Match idRef="Keyword_uk_nhs_number" />
          <Match idRef="Keyword_uk_nhs_number1" />
          <Match idRef="Keyword_uk_nhs_number_dob" />
        </Any>
    </Pattern>
</Entity>
```

### <a name="keywords"></a>키워드
   
#### <a name="keyworduknhsnumber"></a>Keyword_uk_nhs_number

- 국립 보건 서비스 
- nhs 
- health services authority 
- health authority

#### <a name="keyworduknhsnumber1"></a>Keyword_uk_nhs_number1

- patient id 
- patient identification 
- patient no 
- patient number

#### <a name="keyworduknhsnumberdob"></a>Keyword_uk_nhs_number_dob

- g 
- dob 
- D. O. B 
- Date of Birth 
- Birth Date 
   
## <a name="uk-national-insurance-number-nino"></a>영국 NINO(국민 보험 번호)

### <a name="format"></a>형식일

공백 또는 대시로 구분 된 7 자 또는 9 자

### <a name="pattern"></a>패턴

다음과 같은 두 가지 패턴을 사용할 수 있습니다.

- 두 문자 (유효한 NINOs이 접두사의 특정 문자만 사용 하며이 패턴의 유효성 검사는 대/소문자를 구분 하지 않음)
- 6자리 숫자
- ' A ', ' B ', ' C ' 또는 ' d ' (접두사와 마찬가지로 접미사에서는 특정 문자만 허용 되며 대/소문자 구분 안 함)

또는

- 2 개 문자
- 공백 또는 대시
- 2자리 숫자
- 공백 또는 대시
- 2자리 숫자
- 공백 또는 대시
- 2자리 숫자
- 공백 또는 대시
- ' A ', ' B ', ' C ' 또는 ' d ' 중 하나

### <a name="checksum"></a>제외

아니요

### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.
- Func_uk_nino 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.
- Keyword_uk_nino의 키워드가 발견되었습니다.

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
- Func_uk_nino 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.
- Keyword_uk_nino의 키워드가 발견되지 않았습니다.

```
<!-- U.K. NINO -->
<Entity id="16c07343-c26f-49d2-a987-3daf717e94cc" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_uk_nino" />
        <Any minMatches="1">
          <Match idRef="Keyword_uk_nino" />
        </Any>
    </Pattern>    
     <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_uk_nino" />
        <Any minMatches="0" maxMatches="0">
          <Match idRef="Keyword_uk_nino" />
        </Any>
    </Pattern>
</Entity>
```

### <a name="keywords"></a>키워드

#### <a name="keyworduknino"></a>Keyword_uk_nino

- national insurance number 
- national insurance contributions 
- protection act 
- 소유권 
- social security number 
- insurance application 
- medical application 
- social insurance 
- medical attention 
- social security 
- great britain 
- 소유권    
   
## <a name="us--uk-passport-number"></a>미국/영국 여권 번호

### <a name="format"></a>형식일

9자리 숫자

### <a name="pattern"></a>패턴

9자리 연속 숫자

### <a name="checksum"></a>제외

아니요

### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
- Func_usa_uk_passport 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.
- Keyword_passport의 키워드가 발견되었습니다.

```
<Entity id="178ec42a-18b4-47cc-85c7-d62c92fd67f8" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_usa_uk_passport" />
        <Match idRef="Keyword_passport" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a>키워드

#### <a name="keywordpassport"></a>Keyword_passport

- Passport Number 
- Passport No 
- Passport # 
- 여권 
- PassportID 
- Passportno 
- passportnumber 
- パスポート 
- パスポート番号 
- パスポートのNum 
- パスポート # 
- Numéro de passeport 
- Passeport n ° 
- Passeport Non 
- Passeport # 
- 포트 # 
- 지/포트 아님 
- Passeportn ° 
   
## <a name="us-bank-account-number"></a>미국 은행 계좌 번호

### <a name="format"></a>형식일

8-17자리 숫자

### <a name="pattern"></a>패턴

8-17자리 연속 숫자

### <a name="checksum"></a>제외

아니요

### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
- Regex_usa_bank_account_number 정규식이 해당 패턴과 일치하는 콘텐츠를 찾습니다.
- Keyword_usa_Bank_Account의 키워드가 발견되었습니다.

```
<!-- U.S. Bank Account Number -->
<Entity id="a2ce32a8-f935-4bb6-8e96-2a5157672e2c" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Regex_usa_bank_account_number" />
        <Match idRef="Keyword_usa_Bank_Account" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a>키워드

#### <a name="keywordusabankaccount"></a>Keyword_usa_Bank_Account

- Checking Account Number 
- Checking Account 
- Checking Account # 
- Checking Acct Number 
- Checking Acct # 
- Checking Acct No. 
- Checking Account No. 
- Bank Account Number 
- Bank Account # 
- Bank Acct Number 
- Bank Acct # 
- Bank Acct No. 
- Bank Account No. 
- Savings Account Number 
- Savings Account. 
- Savings Account # 
- Savings Acct Number 
- Savings Acct # 
- Savings Acct No. 
- Savings Account No. 
- Debit Account Number 
- Debit Account 
- Debit Account # 
- Debit Acct Number 
- Debit Acct # 
- Debit Acct No. 
- Debit Account No. 
   
## <a name="us-drivers-license-number"></a>미국 운전 면허 번호

### <a name="format"></a>형식일

주마다 다릅니다.

### <a name="pattern"></a>패턴

주마다 다릅니다(예: 뉴욕).
- ddd ddd ddd와 같이 9 자리 숫자는 일치 합니다.
- ddddddddd와 같은 9 자리 숫자가 일치 하지 않습니다.

### <a name="checksum"></a>제외

아니요

### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
- Func_new_york_drivers_license_number 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.
- Keyword_[state_name]_drivers_license_name의 키워드가 발견되었습니다.
- Keyword_us_drivers_license에서 키워드가 발견 되었습니다.

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 65% 신뢰합니다.
- Func_new_york_drivers_license_number 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.
- Keyword_[state_name]_drivers_license_name의 키워드가 발견되었습니다.
- Keyword_us_drivers_license_abbreviations의 키워드가 발견되었습니다.
- Keyword_us_drivers_license의 키워드가 발견되지 않았습니다.

```
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_new_york_drivers_license_number" />
        <Match idRef="Keyword_new_york_drivers_license_name" />
        <Match idRef="Keyword_us_drivers_license" />
    </Pattern>
    <Pattern confidenceLevel="65">
        <IdMatch idRef="Func_new_york_drivers_license_number" />
        <Match idRef="Keyword_new_york_drivers_license_name" />
        <Match idRef="Keyword_us_drivers_license_abbreviations" />
        <Any minMatches="0" maxMatches="0">
          <Match idRef="Keyword_us_drivers_license" />
        </Any>
    </Pattern>
```

### <a name="keywords"></a>키워드

#### <a name="keywordusdriverslicenseabbreviations"></a>Keyword_us_drivers_license_abbreviations

- DL 
- 된다 
- cdl 
- cdls 
- ID 
- 번호가 
- DL 
- 된다 
- cdl # 
- cdls # 
- i
- 번호가 
- ID number 
- ID numbers 
- LIC 
- LIC 

#### <a name="keywordusdriverslicense"></a>Keyword_us_drivers_license

- driverlic 
- driverlics 
- driverlicense 
- driverlicenses 
- Driver Lic 
- Driver Lics 
- Driver License 
- Driver Licenses 
- DriversLic 
- driverslics 
- 드라이버 라이선스 
- 드라이버 라이선스 
- Drivers Lic 
- Drivers Lics 
- Drivers License 
- Drivers Licenses 
- driver' Lic 
- driver'lics 
- driver' 라이선스 
- driver'licenses 
- Driver' Lic 
- Driver' Lics 
- Driver' License 
- Driver' Licenses
- Driver'sLic 
- drivers (slics) 
- driver'slicense 
- driver'slicenses 
- Driver's Lic 
- Driver's Lics 
- Driver's License 
- Driver's Licenses 
- identification number 
- identification numbers 
- identification # 
- id card 
- id cards 
- identification card 
- identification cards 
- driverlic # 
- driverlics # 
- driverlicense # 
- driverlicenses # 
- Driver Lic# 
- Driver Lics# 
- Driver License# 
- Driver Licenses# 
- DriversLic # 
- driverslics # 
- 드라이버 라이선스 # 
- 드라이버 라이선스 수 
- Drivers Lic# 
- Drivers Lics# 
- Drivers License# 
- Drivers Licenses# 
- driver' Lic # 
- driver'lics # 
- driver' 라이선스 # 
- driver'licenses # 
- Driver' Lic# 
- Driver' Lics# 
- Driver' License# 
- Driver' Licenses# 
- Driver'sLic # 
- drivers (slics #) 
- driver'slicense # 
- driver'slicenses # 
- Driver's Lic# 
- Driver's Lics# 
- Driver's License# 
- Driver's Licenses# 
- id card# 
- id cards# 
- identification card# 
- identification cards# 


#### <a name="keywordstatenamedriverslicensename"></a>Keyword_ [state_name] _drivers_license_name

- 주 약어(예: "NY") 
- 주 이름(예: "New York")    
   
## <a name="us-individual-taxpayer-identification-number-itin"></a>미국 ITIN(개인 납세자 번호)

### <a name="format"></a>형식일

"9"로 시작되고, "7" 또는 "8"을 4번째 숫자로 포함하고, 경우에 따라 공백이나 대시로 서식이 지정된 9자리 숫자

### <a name="pattern"></a>패턴

서식이
- "9"자리 숫자 
- 2자리 숫자 
- 공백 또는 대시 
- "7" 또는 "8" 
- 1자리 숫자 
- 공백 또는 대시 
- 4자리 숫자

서식
- "9"자리 숫자 
- 2자리 숫자 
- "7" 또는 "8" 
- 5자리 숫자

### <a name="checksum"></a>제외

아니요

### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.
- Func_formatted_itin 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.
- 다음 중 하나 이상이 충족됩니다.
    - Keyword_itin의 키워드가 발견되었습니다.
    - Func_us_address 함수가 올바른 날짜 형식의 주소를 찾습니다.
    - Func_us_date 함수가 올바른 날짜 형식의 날짜를 찾습니다.
    - Keyword_itin_collaborative의 키워드가 발견되었습니다.

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
- Func_unformatted_itin 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.
- 다음 중 하나 이상이 충족됩니다.
    - Keyword_itin_collaborative의 키워드가 발견되었습니다.
    - Func_us_address 함수가 올바른 날짜 형식의 주소를 찾습니다.
    - Func_us_date 함수가 올바른 날짜 형식의 날짜를 찾습니다.

```
<!-- U.S. Individual Taxpayer Identification Number (ITIN) -->
<Entity id="e55e2a32-f92d-4985-a35d-a0b269eb687b" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_formatted_itin" />
        <Any minMatches="1">
          <Match idRef="Keyword_itin" />
          <Match idRef="Func_us_address" />
          <Match idRef="Func_us_date" />
          <Match idRef="Keyword_itin_collaborative" />
        </Any>
    </Pattern>
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_unformatted_itin" />
        <Match idRef="Keyword_itin" />
        <Any minMatches="1">
          <Match idRef="Keyword_itin_collaborative" />
          <Match idRef="Func_us_address" />
          <Match idRef="Func_us_date" />
        </Any>
    </Pattern>
</Entity>
```

### <a name="keywords"></a>키워드

#### <a name="keyworditin"></a>Keyword_itin

- taxpayer 
- tax id 
- tax identification 
- itin 
- ssn 
- 언급 
- social security 
- tax payer 
- itins 
- taxid 
- individual taxpayer 

#### <a name="keyworditincollaborative"></a>Keyword_itin_collaborative

- License 
- DL 
- dob 
- 생년월일 
- 생일 
- Date of Birth 
   
## <a name="us-social-security-number-ssn"></a>미국 SSN(사회 보험 번호)

### <a name="format"></a>형식일

서식 있는 패턴 또는 서식 없는 패턴으로 표시될 수 있는 9자리 숫자

> [!NOTE]
> mid가 2011 이전에 실행 된 경우 SSN은 특정 범위 내에서 번호의 특정 부분이 유효한 지 확인 하는 강력한 서식을 사용 해야 하지만 검사 값은 없습니다.

### <a name="pattern"></a>패턴

다음의 네 가지 패턴에서 ssns를 검색 하는 함수는 다음과 같습니다.
- Func_ssn는 대시 또는 공백을 사용 하 여 서식이 지정 된 2011 이전의 고급 서식 (ddd-dd-dddd 또는 ddd dd dd)을 사용 하 여 ssns를 찾습니다.
- Func_unformatted_ssn는 형식이 지정 되지 않은 2011 이전 형식으로 서식이 지정 된 ssns를 찾습니다 (ddddddddd).
- Func_randomized_formatted_ssn는 대시 또는 공백으로 서식이 지정 된 post-2011 ssns를 찾습니다 (ddd-dd-dddd 또는 ddd dd dddd).
- Func_randomized_unformatted_ssn는 형식 없는 2011 ssns를 찾고, 서식이 없는 9 자리 숫자 (ddddddddd)를 찾습니다.

### <a name="checksum"></a>제외

아니요


### <a name="definition"></a>정의

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.
- Func_ssn 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.
- Keyword_ssn의 키워드가 발견되었습니다.

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.
- Func_unformatted_ssn 함수가 해당 패턴과 일치 하는 콘텐츠를 찾습니다.
- Keyword_ssn의 키워드가 발견되었습니다.

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 65% 신뢰합니다.
- Func_randomized_formatted_ssn 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.
- Keyword_ssn의 키워드가 발견되었습니다.
- Func_ssn 함수가 해당 패턴과 일치하는 콘텐츠를 찾지 않습니다.

DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 55% 신뢰합니다.
- Func_randomized_unformatted_ssn 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.
- Keyword_ssn의 키워드가 발견되었습니다.
- Func_unformatted_ssn 함수가 해당 패턴과 일치하는 콘텐츠를 찾지 않습니다.

```
<!-- U.S. Social Security Number (SSN) -->
    <Entity id="a44669fe-0d48-453d-a9b1-2cc83f2cba77" patternsProximity="300" recommendedConfidence="75">
      <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_ssn" />
        <Match idRef="Keyword_ssn" />
      </Pattern>
      <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_unformatted_ssn" />
        <Match idRef="Keyword_ssn" />
      </Pattern>
      <Pattern confidenceLevel="65">
        <IdMatch idRef="Func_randomized_formatted_ssn" />
        <Match idRef="Keyword_ssn" />
        <Any minMatches="0" maxMatches="0">
          <Match idRef="Func_ssn" />
        </Any>
      </Pattern>
      <Pattern confidenceLevel="55">
        <IdMatch idRef="Func_randomized_unformatted_ssn" />
        <Match idRef="Keyword_ssn" />
        <Any minMatches="0" maxMatches="0">
          <Match idRef="Func_unformatted_ssn" />
        </Any>
      </Pattern>
    </Entity>
```

### <a name="keywords"></a>키워드

#### <a name="keywordssn"></a>Keyword_ssn

- Social Security 
- Social Security# 
- Soc Sec 
- SSN 
- 있는 ssn 
- SSN 
- 대비 
- 생길 
   

