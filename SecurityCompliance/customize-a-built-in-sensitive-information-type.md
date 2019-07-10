---
title: 기본 제공 중요한 정보 유형 사용자 지정
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 07/08/2019
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Priority
ms.collection:
- M365-security-compliance
search.appverid:
- MOE150
- MET150
description: 콘텐츠에서 중요한 정보를 찾을 때는 소유 말하는 규칙에서 해당 정보를 설명해야 합니다. DLP(데이터 손실 방지)에는 바로 사용할 수 있는 가장 일반적인 중요한 정보 유형에 대한 규칙이 포함되어 있습니다. 이러한 규칙을 사용하려면 정책에 포함해야 합니다. 조직의 특정 요구 사항에 맞게 이러한 기본 제공 규칙을 조정하려고 할 경우 사용자 지정 중요한 정보 유형을 만들면 됩니다. 이 항목에서는 광범위한 잠재적 신용 카드 정보를 검색하도록 기존 규칙 컬렉션을 포함하는 XML 파일을 사용자 지정하는 방법을 보여 줍니다.
ms.openlocfilehash: 8a621e3f1b24a8cea9cd263e44dc2def8a8b95b7
ms.sourcegitcommit: a6f046f1529b0515f4f0e918a19ec83f4138b871
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/08/2019
ms.locfileid: "35587107"
---
# <a name="customize-a-built-in-sensitive-information-type"></a>기본 제공 중요한 정보 유형 사용자 지정

콘텐츠에서 중요한 정보를 찾을 때는 소유 말하는 *규칙*에서 해당 정보를 설명해야 합니다. DLP(데이터 손실 방지)에는 바로 사용할 수 있는 가장 일반적인 중요한 정보 유형에 대한 규칙이 포함되어 있습니다. 이러한 규칙을 사용하려면 정책에 포함해야 합니다. 조직의 특정 요구 사항에 맞게 이러한 기본 제공 규칙을 조정하려고 할 경우 사용자 지정 중요한 정보 유형을 만들면 됩니다. 이 항목에서는 광범위한 잠재적 신용 카드 정보를 검색하도록 기존 규칙 컬렉션을 포함하는 XML 파일을 사용자 지정하는 방법을 보여 줍니다. 
  
이 예제를 다른 기본 제공 중요한 정보 유형에 적용할 수 있습니다. 기본 중요한 정보 유형과 XML 정의 목록을 보려면 [중요한 정보 유형이 찾는 항목](what-the-sensitive-information-types-look-for.md)을 참조하세요. 
  
## <a name="export-the-xml-file-of-the-current-rules"></a>현재 규칙의 XML 파일 내보내기

XML을 내보내려면 [원격 PowerShell을 통해 보안 및 준수 센터에 연결](https://docs.microsoft.com/powershell/exchange/office-365-scc/connect-to-scc-powershell/connect-to-scc-powershell?view=exchange-ps)해야 합니다.
  
1. PowerShell에서 다음을 입력하여 화면에 조직의 규칙을 표시합니다. 고유한 규칙을 아직 만들지 않은 경우 “Microsoft 규칙 패키지”라는 기본 제공 규칙만 표시됩니다.
    
     `Get-DlpSensitiveInformationTypeRulePackage`
    
2. 다음을 입력하여 조직의 규칙을 변수에 저장합니다. 변수에 저장하면 나중에 원격 PowerShell 명령에 적합한 형식으로 쉽게 사용할 수 있습니다.
    
     `$ruleCollections = Get-DlpSensitiveInformationTypeRulePackage`
    
3. 다음을 입력하여 해당 데이터로 형식이 지정된 XML 파일을 만듭니다. (`Set-content`는 XML 파일에 쓰는 cmdlet의 부분입니다.) 
    
     `Set-Content -path "C:\custompath\exportedRules.xml" -Encoding Byte -Value $ruleCollections.SerializedClassificationRuleCollection`
    
    > [!IMPORTANT]
    > 규칙 팩이 실제로 저장된 파일 위치를 사용해야 합니다. `C:\custompath\`는 자리 표시자입니다. 
  
## <a name="find-the-rule-that-you-want-to-modify-in-the-xml"></a>XML에서 수정하려는 규칙 찾기

위의 cmdlet은 사용자가 제공한 기본 규칙을 포함하는 전체 *규칙 컬렉션*을 내보냈습니다. 다음으로, 수정하려는 신용 카드 번호 규칙을 검색해야 합니다. 
  
1. 텍스트 편집기를 사용하여 이전 섹션에서 내보낸 XML 파일을 엽니다.
    
2. 아래로 스크롤하여 `<Rules>` 태그로 이동합니다. 이 태그는 DLP 규칙을 포함하는 섹션의 시작을 나타냅니다. (이 XML 파일에는 전체 규칙 컬렉션에 대한 정보가 포함되어 있으므로 해당 규칙으로 이동하기 위해 다시 위로 스크롤해야 합니다.) 
    
3. *Func_credit_card*를 찾아 신용 카드 번호 규칙 정의를 확인합니다. XML에서 규칙 이름에는 공백이 있으면 안 되므로 일반적으로 공백이 밑줄로 바뀌고, 규칙 이름은 때때로 축약형으로 표시됩니다. “SSN”으로 축약되는 미국 사회 보장 번호 규칙을 예로 들 수 있습니다. 신용 카드 번호 규칙 XML은 다음 코드 예제와 같아야 합니다. 
    
  ```
  <Entity id="50842eb7-edc8-4019-85dd-5a5c1f2bb085"
         patternsProximity="300" recommendedConfidence="85">
        <Pattern confidenceLevel="85">
         <IdMatch idRef="Func_credit_card" />
          <Any minMatches="1">
            <Match idRef="Keyword_cc_verification" />
            <Match idRef="Keyword_cc_name" />
            <Match idRef="Func_expiration_date" />
          </Any>
        </Pattern>
      </Entity>
  ```

XML에서 신용 카드 번호 규칙 정의를 찾았으므로 요구에 맞게 규칙의 XML을 사용자 지정할 수 있습니다. (XML 정의를 다시 확인하려면 이 항목 끝에 나오는 [용어 설명](#term-glossary)을 참조하세요.) 
  
## <a name="modify-the-xml-and-create-a-new-sensitive-information-type"></a>XML 수정 및 중요한 정보 유형 새로 만들기

먼저, 기본 규칙을 직접 수정할 수 없으므로 중요한 정보 유형을 새로 만들어야 합니다. [보안 및 준수 센터 PowerShell에서 사용자 지정 중요한 정보 유형 만들기](create-a-custom-sensitive-information-type-in-scc-powershell.md)에 요약된 사용자 지정 중요한 정보 유형으로 다양한 작업을 수행할 수 있습니다. 이 예제에서는 신용 카드 번호 규칙에서 증빙을 제거하고 키워드를 추가하는 등, 간단한 작업만 수행합니다.
  
모든 XML 규칙 정의는 다음과 같은 일반 템플릿을 토대로 작성됩니다. 신용 카드 번호 정의 XML을 복사한 후 템플릿에 붙여넣고, 일부 값을 수정한 후(다음 예제의 ". . ." 자리 표시자 확인) 수정한 XML을 정책에서 사용할 수 있는 새 규칙으로 업로드해야 합니다.
  
```
<?xml version="1.0" encoding="utf-16"?>
<RulePackage xmlns="http://schemas.microsoft.com/office/2011/mce">
  <RulePack id=". . .">
    <Version major="1" minor="0" build="0" revision="0" />
    <Publisher id=". . ." /> 
    <Details defaultLangCode=". . .">
      <LocalizedDetails langcode=" . . . ">
         <PublisherName>. . .</PublisherName>
         <Name>. . .</Name>
         <Description>. . .</Description>
      </LocalizedDetails>
    </Details>
  </RulePack>
  
 <Rules>
   <!-- Paste the Credit Card Number rule definition here.--> 
      <LocalizedStrings>
         <Resource idRef=". . .">
           <Name default="true" langcode=" . . . ">. . .</Name>
           <Description default="true" langcode=". . ."> . . .</Description>
         </Resource>
      </LocalizedStrings>
   </Rules>
</RulePackage>
```

이제, 다음 XML과 비슷한 결과를 얻게 됩니다. 규칙 패키지 및 규칙은 고유한 GUID로 식별되므로 2개의 GUID, 즉 규칙 패키지용 GUID와 신용 카드 번호 규칙용 GUID를 생성해야 합니다(다음 코드 예제의 엔터티 ID용 GUID는 기본 제공 규칙 정의에 대한 것이므로 새 GUID로 바꾸어야 함). GUID를 생성하는 몇 가지 방법이 있지만 PowerShell에서 **[guid]::NewGuid()** 를 입력하여 쉽게 생성할 수 있습니다. 
  
```
<?xml version="1.0" encoding="utf-16"?>
<RulePackage xmlns="http://schemas.microsoft.com/office/2011/mce">
  <RulePack id="8aac8390-e99f-4487-8d16-7f0cdee8defc">
    <Version major="1" minor="0" build="0" revision="0" />
    <Publisher id="8d34806e-cd65-4178-ba0e-5d7d712e5b66" />
    <Details defaultLangCode="en">
      <LocalizedDetails langcode="en">
        <PublisherName>Contoso Ltd.</PublisherName>
        <Name>Financial Information</Name>
        <Description>Modified versions of the Microsoft rule package</Description>
      </LocalizedDetails>
    </Details>
  </RulePack>
  
 <Rules>
    <Entity id="db80b3da-0056-436e-b0ca-1f4cf7080d1f"
       patternsProximity="300" recommendedConfidence="85">
      <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_credit_card" />
        <Any minMatches="1">
          <Match idRef="Keyword_cc_verification" />
          <Match idRef="Keyword_cc_name" />
          <Match idRef="Func_expiration_date" />
        </Any>
      </Pattern>
    </Entity>
      <LocalizedStrings>
         <Resource idRef="db80b3da-0056-436e-b0ca-1f4cf7080d1f"> 
<!-- This is the GUID for the preceding Credit Card Number entity because the following text is for that Entity. -->
           <Name default="true" langcode="en-us">Modified Credit Card Number</Name>
           <Description default="true" langcode="en-us">Credit Card Number that looks for additional keywords, and another version of Credit Card Number that doesn't require keywords (but has a lower confidence level)</Description>
         </Resource>
      </LocalizedStrings>
   </Rules>
</RulePackage>
```

## <a name="remove-the-corroborative-evidence-requirement-from-a-sensitive-information-type"></a>중요한 정보 유형에서 증빙 요구 사항 제거

사용자가 보안 및 준수 센터에 업로드할 수 있는 새 중요한 정보 유형을 만들었으므로, 이제 다음 단계는 규칙을 좀 더 구체적으로 지정하는 것입니다. 체크섬을 통과하는 16자리 숫자만 찾고 추가(증빙) 증거(예: 키워드)를 요구하지 않도록 규칙을 수정합니다. 이렇게 하려면 증빙을 찾는 XML의 부분을 제거해야 합니다. 일반적으로 신용 카드 번호와 비슷한 특정 키워드 또는 만료 날짜가 있으므로 증빙은 가양성을 줄이는 데 매우 유용합니다. 해당 증거를 제거하는 경우 이 예제에서 값이 85인 `confidenceLevel`을 줄여 찾은 항목이 신용 카드 번호가 맞는지를 나타내는 신뢰도도 조정해야 합니다.
  
```
<Entity id="db80b3da-0056-436e-b0ca-1f4cf7080d1f" patternsProximity="300"
      <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_credit_card" />
      </Pattern>
    </Entity>
```

## <a name="look-for-keywords-that-are-specific-to-your-organization"></a>조직에 관련된 키워드 찾기

증빙을 요구하면서 다른 또는 추가 키워드를 원할 수 있고, 해당 증거를 찾을 위치를 변경할 수도 있습니다. `patternsProximity`를 조정하여 증빙 범위를 16자리 숫자 정도로 확장하거나 축소할 수 있습니다. 고유의 키워드를 추가하려면 키워드 목록을 정의하고 규칙 내에서 참조해야 합니다. 다음 XML은 키워드 "회사 카드" 및 "Contoso 카드"를 추가하여 해당 구를 신용 카드 번호의 150자 내에 포함하는 모든 메시지가 신용 카드 번호로 식별되도록 합니다. 
  
```
<Rules>
<! -- Modify the patternsProximity to be "150" rather than "300." -->
    <Entity id="db80b3da-0056-436e-b0ca-1f4cf7080d1f" patternsProximity="150" recommendedConfidence="85">
      <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_credit_card" />
        <Any minMatches="1">
          <Match idRef="Keyword_cc_verification" />
          <Match idRef="Keyword_cc_name" />
<!-- Add the following XML, which references the keywords at the end of the XML sample. -->
          <Match idRef="My_Additional_Keywords" />
          <Match idRef="Func_expiration_date" />
        </Any>
      </Pattern>
    </Entity>
<!-- Add the following XML, and update the information inside the <Term> tags with the keywords that you want to detect. -->
    <Keyword id="My_Additional_Keywords">
      <Group matchStyle="word">
        <Term caseSensitive="false">company card</Term>
        <Term caseSensitive="false">Contoso card</Term>
      </Group>
    </Keyword>
```

## <a name="upload-your-rule"></a>규칙 업로드

규칙을 업로드하려면 다음을 수행해야 합니다.
  
1. 유니코드 인코딩을 사용하여 .xml 파일로 저장합니다. 이 작업은 파일을 다른 인코딩으로 저장하면 규칙이 작동하지 않으므로 중요합니다.
    
2. [원격 PowerShell을 통해 보안 및 준수 센터에 연결합니다.](https://go.microsoft.com/fwlink/?linkid=799771)
    
3. PowerShell에서 다음을 입력합니다.
    
     `New-DlpSensitiveInformationTypeRulePackage -FileData (Get-Content -Path "C:\custompath\MyNewRulePack.xml" -Encoding Byte)`.
    
    > [!IMPORTANT]
    > 규칙 팩이 실제로 저장된 파일 위치를 사용해야 합니다. `C:\custompath\`는 자리 표시자입니다. 
  
4. 확인하려면 Y를 입력하고 **Enter** 키를 누릅니다.
    
5. `Get-DlpSensitiveInformationType`을 입력하여 새 규칙이 업로드되었는지 확인합니다. 새 규칙이 업로드되었으면 규칙 이름이 표시됩니다.
    
새 규칙을 사용하여 중요한 정보를 검색하려면 해당 규칙을 DLP 정책에 추가해야 합니다. 정책에 규칙을 추가하는 방법을 알아보려면 [템플릿에서 DLP 정책 만들기](create-a-dlp-policy-from-a-template.md)를 참조하세요.
  
## <a name="term-glossary"></a>용어 설명

다음은 이 절차 동안 표시되는 용어에 대한 정의입니다.
  
|**용어**|**정의**|
|:-----|:-----|
|엔터티|엔터티는 소유 말해서 신용 카드 번호와 같은 중요한 정보 유형입니다. 각 엔터티는 고유한 GUID를 ID로 갖습니다. GUID를 복사한 후 XML에서 검색하면 XML 규칙 정의와 해당 XML 규칙의 모든 지역화된 번역을 찾을 수 있습니다. 또한 번역에 대한 GUID를 찾은 후 해당 GUID를 검색하여 이 정의를 찾을 수도 있습니다.|
|함수|XML 파일은 컴파일된 코드의 함수에 해당하는 `Func_credit_card`를 참조합니다. 함수는 복잡한 regex를 실행하는 데 사용되며 체크섬이 기본 제공 규칙과 일치하는지 확인합니다. 이러한 작업이 코드에서 진행되므로 일부 변수는 XML 파일에 나타나지 않습니다.|
|IdMatch|이는 패턴과 일치하는 ID(예: 신용 카드 번호)입니다.|
|키워드 목록|XML 파일은 엔터티에 대한 `patternsProximity` 내에서 일치하는지 확인하는 키워드 목록에 해당하는 `keyword_cc_verification` 및 `keyword_cc_name`도 참조합니다.|
|패턴|패턴은 중요한 유형이 검색할 항목 목록을 포함합니다. 여기에는 키워드, regex 및 내부 함수(체크섬 확인 등의 작업 수행)가 포함됩니다. 중요한 정보 유형에는 고유한 신뢰도를 갖는 여러 패턴이 있을 수 있습니다. 증빙이 발견되면 높은 신뢰도를 반환하고, 증빙이 거의 없거나 전혀 없으면 낮은 신뢰도를 반환하는 중요한 정보 유형을 만들면 유용합니다.|
|패턴 confidenceLevel|DLP 엔진이 일치 항목을 발견한 신뢰도입니다. 이 수준의 신뢰도는 패턴 요구 사항이 충족될 경우 패턴의 일치와 연관됩니다. 이는 Exchange 메일 흐름 규칙(전송 규칙이라고도 함)을 사용할 때 고려해야 할 신뢰도 측정값입니다.|
|patternsProximity|신용 카드 번호 패턴처럼 보이는 항목이 있는 경우 `patternsProximity`는 증빙을 찾게 되는 해당 번호 주변의 근접 범위를 나타냅니다.|
|recommendedConfidence|이 규칙에 대해 권장되는 신뢰도입니다. 권장 신뢰도는 엔터티 및 선호도에 적용됩니다. 엔터티의 경우 이 값은 패턴의 `confidenceLevel`에 대해 평가되지 않으며, 적용하려는 신뢰도를 선택하는 데 도움이 되는 권장 사항일 뿐입니다. 선호도의 경우 메일 흐름 규칙 작업이 호출되려면 패턴의 `confidenceLevel`이 `recommendedConfidence` 값보다 커야 합니다. `recommendedConfidence`는 작업을 호출하는 메일 흐름 규칙에서 사용되는 기본 신뢰도입니다. 원할 경우 대신 패턴의 신뢰도를 기준으로 호출할 메일 흐름 규칙을 수동으로 변경할 수 있습니다.|
   
## <a name="for-more-information"></a>자세한 내용

- [중요한 정보 유형이 찾는 항목](what-the-sensitive-information-types-look-for.md)
    
- [사용자 지정 중요한 정보 유형 만들기](create-a-custom-sensitive-information-type.md)
    
- [데이터 손실 방지 정책 개요](data-loss-prevention-policies.md)
    

