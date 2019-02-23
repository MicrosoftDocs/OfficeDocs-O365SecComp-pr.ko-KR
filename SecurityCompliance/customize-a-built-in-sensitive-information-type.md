---
title: 기본 제공 중요한 정보 유형 사용자 지정
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 6/25/2018
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Priority
ms.collection: Strat_O365_IP
search.appverid:
- MOE150
- MET150
ms.assetid: 2164ce3d-4d64-4283-b6b1-b81fbe835e8e
description: 콘텐츠에서 중요한 정보를 찾을 때는 소유 말하는 규칙에서 해당 정보를 설명해야 합니다. DLP(데이터 손실 방지)에는 바로 사용할 수 있는 가장 일반적인 중요한 정보 유형에 대한 규칙이 포함되어 있습니다. 이러한 규칙을 사용하려면 정책에 포함해야 합니다. 조직의 특정 요구 사항에 맞게 이러한 기본 제공 규칙을 조정하려고 할 경우 사용자 지정 중요한 정보 유형을 만들면 됩니다. 이 항목에서는 광범위한 잠재적 신용 카드 정보를 검색하도록 기존 규칙 컬렉션을 포함하는 XML 파일을 사용자 지정하는 방법을 보여 줍니다.
ms.openlocfilehash: 9014a2270947fb97edc1ce834985fbd084bc19e6
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30215448"
---
# <a name="customize-a-built-in-sensitive-information-type"></a><span data-ttu-id="6425d-107">기본 제공 중요한 정보 유형 사용자 지정</span><span class="sxs-lookup"><span data-stu-id="6425d-107">Customize a built-in sensitive information type</span></span>

<span data-ttu-id="6425d-p102">콘텐츠에서 중요한 정보를 찾을 때는 소유 말하는 *규칙*에서 해당 정보를 설명해야 합니다. DLP(데이터 손실 방지)에는 바로 사용할 수 있는 가장 일반적인 중요한 정보 유형에 대한 규칙이 포함되어 있습니다. 이러한 규칙을 사용하려면 정책에 포함해야 합니다. 조직의 특정 요구 사항에 맞게 이러한 기본 제공 규칙을 조정하려고 할 경우 사용자 지정 중요한 정보 유형을 만들면 됩니다. 이 항목에서는 광범위한 잠재적 신용 카드 정보를 검색하도록 기존 규칙 컬렉션을 포함하는 XML 파일을 사용자 지정하는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="6425d-p102">When looking for sensitive information in content, you need to describe that information in what's called a  *rule*  . Data loss prevention (DLP) includes rules for the most-common sensitive information types that you can use right away. To use these rules, you have to include them in a policy. You might find that you want to adjust these built-in rules to meet your organization's specific needs, and you can do that by creating a custom sensitive information type. This topic shows you how to customize the XML file that contains the existing rule collection to detect a wider range of potential credit-card information.</span></span> 
  
<span data-ttu-id="6425d-p103">이 예제를 다른 기본 제공 중요한 정보 유형에 적용할 수 있습니다. 기본 중요한 정보 유형과 XML 정의 목록을 보려면 [중요한 정보 유형이 찾는 항목](what-the-sensitive-information-types-look-for.md)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="6425d-p103">You can take this example and apply it to other built-in sensitive information types. For a list of default sensitive information types and XML definitions, see [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span> 
  
## <a name="export-the-xml-file-of-the-current-rules"></a><span data-ttu-id="6425d-115">현재 규칙의 XML 파일 내보내기</span><span class="sxs-lookup"><span data-stu-id="6425d-115">Export the XML file of the current rules</span></span>

<span data-ttu-id="6425d-116">XML을 내보내려면 [원격 PowerShell을 통해 보안 및 준수 센터에 연결](https://go.microsoft.com/fwlink/?linkid=799771)해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="6425d-116">To export the XML, you need to [connect to the Security and Compliance Center via Remote PowerShell.](https://go.microsoft.com/fwlink/?linkid=799771).</span></span>
  
1. <span data-ttu-id="6425d-p104">PowerShell에서 다음을 입력하여 화면에 조직의 규칙을 표시합니다. 고유한 규칙을 아직 만들지 않은 경우 “Microsoft 규칙 패키지”라는 기본 제공 규칙만 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="6425d-p104">In the PowerShell, type the following to display your organization's rules on screen. If you haven't created your own, you'll only see the default, built-in rules, labeled "Microsoft Rule Package."</span></span>
    
     `Get-DlpSensitiveInformationTypeRulePackage`
    
2. <span data-ttu-id="6425d-p105">다음을 입력하여 조직의 규칙을 변수에 저장합니다. 변수에 저장하면 나중에 원격 PowerShell 명령에 적합한 형식으로 쉽게 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6425d-p105">Store your organization's rules in a in a variable by typing the following. Storing something in a variable makes it easily available later in a format that works for remote PowerShell commands.</span></span>
    
     `$ruleCollections = Get-DlpSensitiveInformationTypeRulePackage`
    
3. <span data-ttu-id="6425d-p106">다음을 입력하여 해당 데이터로 형식이 지정된 XML 파일을 만듭니다. (`Set-content`는 XML 파일에 쓰는 cmdlet의 부분입니다.)</span><span class="sxs-lookup"><span data-stu-id="6425d-p106">Make a formatted XML file with all that data by typing the following. ( `Set-content` is the part of the cmdlet that writes the XML to the file.)</span></span> 
    
     `Set-Content -path "C:\custompath\exportedRules.xml" -Encoding Byte -Value $ruleCollections.SerializedClassificationRuleCollection`
    
    > [!IMPORTANT]
    > <span data-ttu-id="6425d-p107">규칙 팩이 실제로 저장된 파일 위치를 사용해야 합니다. `C:\custompath\`는 자리 표시자입니다.</span><span class="sxs-lookup"><span data-stu-id="6425d-p107">Make sure that you use the file location where your rule pack is actually stored.  `C:\custompath\` is a placeholder.</span></span> 
  
## <a name="find-the-rule-that-you-want-to-modify-in-the-xml"></a><span data-ttu-id="6425d-125">XML에서 수정하려는 규칙 찾기</span><span class="sxs-lookup"><span data-stu-id="6425d-125">Find the rule that you want to modify in the XML</span></span>

<span data-ttu-id="6425d-p108">위의 cmdlet은 사용자가 제공한 기본 규칙을 포함하는 전체 *규칙 컬렉션*을 내보냈습니다. 다음으로, 수정하려는 신용 카드 번호 규칙을 검색해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="6425d-p108">The cmdlets above exported the entire  *rule collection*  , which includes the default rules we provide. Next you'll need to look specifically for the Credit Card Number rule that you want to modify.</span></span> 
  
1. <span data-ttu-id="6425d-128">텍스트 편집기를 사용하여 이전 섹션에서 내보낸 XML 파일을 엽니다.</span><span class="sxs-lookup"><span data-stu-id="6425d-128">Use a text editor to open the XML file that you exported in the previous section.</span></span>
    
2. <span data-ttu-id="6425d-p109">아래로 스크롤하여 `<Rules>` 태그로 이동합니다. 이 태그는 DLP 규칙을 포함하는 섹션의 시작을 나타냅니다. (이 XML 파일에는 전체 규칙 컬렉션에 대한 정보가 포함되어 있으므로 해당 규칙으로 이동하기 위해 다시 위로 스크롤해야 합니다.)</span><span class="sxs-lookup"><span data-stu-id="6425d-p109">Scroll down to the  `<Rules>` tag, which is the start of the section that contains the DLP rules. (Because this XML file contains the information for the entire rule collection, it contains other information at the top that you need to scroll past to get to the rules.)</span></span> 
    
3. <span data-ttu-id="6425d-p110">*Func_credit_card*를 찾아 신용 카드 번호 규칙 정의를 확인합니다. XML에서 규칙 이름에는 공백이 있으면 안 되므로 일반적으로 공백이 밑줄로 바뀌고, 규칙 이름은 때때로 축약형으로 표시됩니다. “SSN”으로 축약되는 미국 사회 보장 번호 규칙을 예로 들 수 있습니다. 신용 카드 번호 규칙 XML은 다음 코드 예제와 같아야 합니다.</span><span class="sxs-lookup"><span data-stu-id="6425d-p110">Look for  *Func_credit_card*  to find the Credit Card Number rule definition. (In the XML, rule names can't contain spaces, so the spaces are usually replaced with underscores, and rule names are sometimes abbreviated. An example of this is the U.S. Social Security number rule, which is abbreviated "SSN." The Credit Card Number rule XML should look like the following code sample.</span></span> 
    
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

<span data-ttu-id="6425d-p111">XML에서 신용 카드 번호 규칙 정의를 찾았으므로 요구에 맞게 규칙의 XML을 사용자 지정할 수 있습니다. (XML 정의를 다시 확인하려면 이 항목 끝에 나오는 [용어 설명](#term-glossary)을 참조하세요.)</span><span class="sxs-lookup"><span data-stu-id="6425d-p111">Now that you have located the Credit Card Number rule definition in the XML, you can customize the rule's XML to meet your needs. (For a refresher on the XML definitions, see the [Term glossary](#term-glossary) at the end of this topic.)</span></span> 
  
## <a name="modify-the-xml-and-create-a-new-sensitive-information-type"></a><span data-ttu-id="6425d-137">XML 수정 및 중요한 정보 유형 새로 만들기</span><span class="sxs-lookup"><span data-stu-id="6425d-137">Modify the XML and create a new sensitive information type</span></span>

<span data-ttu-id="6425d-p112">먼저, 기본 규칙을 직접 수정할 수 없으므로 중요한 정보 유형을 새로 만들어야 합니다. [Office 365 보안 및 준수 센터 PowerShell에서 사용자 지정 중요한 정보 유형 만들기](create-a-custom-sensitive-information-type-in-scc-powershell.md)에 요약된 사용자 지정 중요한 정보 유형으로 다양한 작업을 수행할 수 있습니다. 이 예제에서는 신용 카드 번호 규칙에서 증빙을 제거하고 키워드를 추가하는 등, 간단한 작업만 수행합니다.</span><span class="sxs-lookup"><span data-stu-id="6425d-p112">First, you need to create a new sensitive information type because you can't directly modify the default rules. You can do a wide variety of things with custom sensitive information types, which are outlined in [Create a custom sensitive information type in Office 365 Security & Compliance Center PowerShell](create-a-custom-sensitive-information-type-in-scc-powershell.md). For this example, we'll keep it simple and only remove corroborative evidence and add keywords to the Credit Card Number rule.</span></span>
  
<span data-ttu-id="6425d-p113">모든 XML 규칙 정의는 다음과 같은 일반 템플릿을 토대로 작성됩니다. 신용 카드 번호 정의 XML을 복사한 후 템플릿에 붙여넣고, 일부 값을 수정한 후(다음 예제의 ". . ." 자리 표시자 확인) 수정한 XML을 정책에서 사용할 수 있는 새 규칙으로 업로드해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="6425d-p113">All XML rule definitions are built on the following general template. You need to copy and paste the Credit Card Number definition XML in the template, modify some values (notice the ". . ." placeholders in the following example), and then upload the modified XML as a new rule that can be used in policies.</span></span>
  
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

<span data-ttu-id="6425d-p114">이제, 다음 XML과 비슷한 결과를 얻게 됩니다. 규칙 패키지 및 규칙은 고유한 GUID로 식별되므로 2개의 GUID, 즉 규칙 패키지용 GUID와 신용 카드 번호 규칙용 GUID를 생성해야 합니다(다음 코드 예제의 엔터티 ID용 GUID는 기본 제공 규칙 정의에 대한 것이므로 새 GUID로 바꾸어야 함). GUID를 생성하는 몇 가지 방법이 있지만 PowerShell에서 **[guid]::NewGuid()** 를 입력하여 쉽게 생성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6425d-p114">Now, you have something that looks similar to the following XML. Because rule packages and rules are identified by their unique GUIDs, you need to generate two GUIDs: one for the rule package and one to replace the GUID for the Credit Card Number rule. (The GUID for the entity ID in the following code sample is the one for our built-in rule definition, which you need to replace with a new one.) There are several ways to generate GUIDs, but you can do it easily in PowerShell by typing **[guid]::NewGuid()**.</span></span> 
  
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

## <a name="remove-the-corroborative-evidence-requirement-from-a-sensitive-information-type"></a><span data-ttu-id="6425d-149">중요한 정보 유형에서 증빙 요구 사항 제거</span><span class="sxs-lookup"><span data-stu-id="6425d-149">Remove the corroborative evidence requirement from a sensitive information type</span></span>

<span data-ttu-id="6425d-p115">사용자가 보안 및 준수 센터에 업로드할 수 있는 새 중요한 정보 유형을 만들었으므로, 이제 다음 단계는 규칙을 좀 더 구체적으로 지정하는 것입니다. 체크섬을 통과하는 16자리 숫자만 찾고 추가(증빙) 증거(예: 키워드)를 요구하지 않도록 규칙을 수정합니다. 이렇게 하려면 증빙을 찾는 XML의 부분을 제거해야 합니다. 일반적으로 신용 카드 번호와 비슷한 특정 키워드 또는 만료 날짜가 있으므로 증빙은 가양성을 줄이는 데 매우 유용합니다. 해당 증거를 제거하는 경우 이 예제에서 값이 85인 `confidenceLevel`을 줄여 찾은 항목이 신용 카드 번호가 맞는지를 나타내는 신뢰도도 조정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="6425d-p115">Now that you have a new sensitive information type that you're able to upload to the Security &amp; Compliance Center, the next step is to make the rule more specific. Modify the rule so that it only looks for a 16-digit number that passes the checksum but doesn't require additional (corroborative) evidence (for example keywords). To do this, you need to remove the part of the XML that looks for corroborative evidence. Corroborative evidence is very helpful in reducing false positives because usually there are certain keywords or an expiration date near the credit card number. If you remove that evidence, you should also adjust how confident you are that you found a credit card number by lowering the  `confidenceLevel`, which is 85 in the example.</span></span>
  
```
<Entity id="db80b3da-0056-436e-b0ca-1f4cf7080d1f" patternsProximity="300"
      <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_credit_card" />
      </Pattern>
    </Entity>
```

## <a name="look-for-keywords-that-are-specific-to-your-organization"></a><span data-ttu-id="6425d-155">조직에 관련된 키워드 찾기</span><span class="sxs-lookup"><span data-stu-id="6425d-155">Look for keywords that are specific to your organization</span></span>

<span data-ttu-id="6425d-p116">증빙을 요구하면서 다른 또는 추가 키워드를 원할 수 있고, 해당 증거를 찾을 위치를 변경할 수도 있습니다. `patternsProximity`를 조정하여 증빙 범위를 16자리 숫자 정도로 확장하거나 축소할 수 있습니다. 고유의 키워드를 추가하려면 키워드 목록을 정의하고 규칙 내에서 참조해야 합니다. 다음 XML은 키워드 "회사 카드" 및 "Contoso 카드"를 추가하여 해당 구를 신용 카드 번호의 150자 내에 포함하는 모든 메시지가 신용 카드 번호로 식별되도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="6425d-p116">You might want to require corroborative evidence but want different or additional keywords, and perhaps you want to change where to look for that evidence. You can adjust the  `patternsProximity` to expand or shrink the window for corroborative evidence around the 16-digit number. To add your own keywords, you need to define a keyword list and reference it within your rule. The following XML adds the keywords "company card" and "Contoso card" so that any message that contains those phrases within 150 characters of a credit card number will be identified as a credit card number.</span></span> 
  
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

## <a name="upload-your-rule"></a><span data-ttu-id="6425d-160">규칙 업로드</span><span class="sxs-lookup"><span data-stu-id="6425d-160">Upload your rule</span></span>

<span data-ttu-id="6425d-161">규칙을 업로드하려면 다음을 수행해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="6425d-161">To upload your rule, you need to do the following.</span></span>
  
1. <span data-ttu-id="6425d-p117">유니코드 인코딩을 사용하여 .xml 파일로 저장합니다. 이 작업은 파일을 다른 인코딩으로 저장하면 규칙이 작동하지 않으므로 중요합니다.</span><span class="sxs-lookup"><span data-stu-id="6425d-p117">Save it as an .xml file with Unicode encoding. This is important because the rule won't work if the file is saved with a different encoding.</span></span>
    
2. [<span data-ttu-id="6425d-164">원격 PowerShell을 통해 보안 및 준수 센터에 연결합니다.</span><span class="sxs-lookup"><span data-stu-id="6425d-164">Connect to the Security and Compliance Center via Remote PowerShell.</span></span>](https://go.microsoft.com/fwlink/?linkid=799771)
    
3. <span data-ttu-id="6425d-165">PowerShell에서 다음을 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="6425d-165">In the PowerShell, type the following.</span></span>
    
     <span data-ttu-id="6425d-166">`New-DlpSensitiveInformationTypeRulePackage -FileData (Get-Content -Path "C:\custompath\MyNewRulePack.xml" -Encoding Byte)`.</span><span class="sxs-lookup"><span data-stu-id="6425d-166">`New-DlpSensitiveInformationTypeRulePackage -FileData (Get-Content -Path "C:\custompath\MyNewRulePack.xml" -Encoding Byte)`.</span></span>
    
    > [!IMPORTANT]
    > <span data-ttu-id="6425d-p118">규칙 팩이 실제로 저장된 파일 위치를 사용해야 합니다. `C:\custompath\`는 자리 표시자입니다.</span><span class="sxs-lookup"><span data-stu-id="6425d-p118">Make sure that you use the file location where your rule pack is actually stored.  `C:\custompath\` is a placeholder.</span></span> 
  
4. <span data-ttu-id="6425d-169">확인하려면 Y를 입력하고 **Enter** 키를 누릅니다.</span><span class="sxs-lookup"><span data-stu-id="6425d-169">To confirm, type Y, and then press **Enter**.</span></span>
    
5. <span data-ttu-id="6425d-170">`Get-DlpSensitiveInformationType`을 입력하여 새 규칙이 업로드되었는지 확인합니다. 새 규칙이 업로드되었으면 규칙 이름이 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="6425d-170">Verify that your new rule was uploaded by typing  `Get-DlpSensitiveInformationType`, which now displays the name of your rule.</span></span>
    
<span data-ttu-id="6425d-p119">새 규칙을 사용하여 중요한 정보를 검색하려면 해당 규칙을 DLP 정책에 추가해야 합니다. 정책에 규칙을 추가하는 방법을 알아보려면 [템플릿에서 DLP 정책 만들기](create-a-dlp-policy-from-a-template.md)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="6425d-p119">To start using the new rule to detect sensitive information, you need to add the rule to a DLP policy. To learn how to add the rule to a policy, see [Create a DLP policy from a template](create-a-dlp-policy-from-a-template.md).</span></span>
  
## <a name="term-glossary"></a><span data-ttu-id="6425d-173">용어 설명</span><span class="sxs-lookup"><span data-stu-id="6425d-173">Term glossary</span></span>

<span data-ttu-id="6425d-174">다음은 이 절차 동안 표시되는 용어에 대한 정의입니다.</span><span class="sxs-lookup"><span data-stu-id="6425d-174">These are the definitions for the terms you encountered during this procedure.</span></span>
  
|<span data-ttu-id="6425d-175">**용어**</span><span class="sxs-lookup"><span data-stu-id="6425d-175">**Term**</span></span>|<span data-ttu-id="6425d-176">**정의**</span><span class="sxs-lookup"><span data-stu-id="6425d-176">**Definition**</span></span>|
|:-----|:-----|
|<span data-ttu-id="6425d-177">엔터티</span><span class="sxs-lookup"><span data-stu-id="6425d-177">Entity</span></span>  <br/> |<span data-ttu-id="6425d-p120">엔터티는 소유 말해서 신용 카드 번호와 같은 중요한 정보 유형입니다. 각 엔터티는 고유한 GUID를 ID로 갖습니다. GUID를 복사한 후 XML에서 검색하면 XML 규칙 정의와 해당 XML 규칙의 모든 지역화된 번역을 찾을 수 있습니다. 또한 번역에 대한 GUID를 찾은 후 해당 GUID를 검색하여 이 정의를 찾을 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6425d-p120">Entities are what we call sensitive information types, such as credit card numbers. Each entity has a unique GUID as its ID. If you copy a GUID and search for it in the XML, you'll find the XML rule definition and all the localized translations of that XML rule. You can also find this definition by locating the GUID for the translation and then searching for that GUID.</span></span>  <br/> |
|<span data-ttu-id="6425d-182">함수</span><span class="sxs-lookup"><span data-stu-id="6425d-182">Functions</span></span>  <br/> |<span data-ttu-id="6425d-p121">XML 파일은 컴파일된 코드의 함수에 해당하는 `Func_credit_card`를 참조합니다. 함수는 복잡한 regex를 실행하는 데 사용되며 체크섬이 기본 제공 규칙과 일치하는지 확인합니다. 이러한 작업이 코드에서 진행되므로 일부 변수는 XML 파일에 나타나지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6425d-p121">The XML file references  `Func_credit_card`, which is a function in compiled code. Functions are used to run complex regexes and verify that checksums match for our built-in rules.) Because this happens in the code, some of the variables don't appear in the XML file.  </span></span><br/> |
|<span data-ttu-id="6425d-185">IdMatch</span><span class="sxs-lookup"><span data-stu-id="6425d-185">IdMatch</span></span>  <br/> |<span data-ttu-id="6425d-p122">패턴이 일치하려고 시도하는 식별자입니다(예: 신용 카드 번호). [엔터티 규칙](https://support.office.com/article/c4ab8707-0839-4855-9390-3dbcb43475a7.aspx#dlp-entity)에서 이 내용 및 `Match` 태그에 대해 자세히 알아볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6425d-p122">This is the identifier that the pattern is to trying to match—for example, a credit card number. You can read more about this and about the  `Match` tags in [Entity rules](https://support.office.com/article/c4ab8707-0839-4855-9390-3dbcb43475a7.aspx#dlp-entity).  </span></span><br/> |
|<span data-ttu-id="6425d-188">키워드 목록</span><span class="sxs-lookup"><span data-stu-id="6425d-188">Keyword lists</span></span>  <br/> |<span data-ttu-id="6425d-p123">XML 파일은 엔터티에 대한 `patternsProximity` 내에서 일치하는지 확인하는 키워드 목록에 해당하는 `keyword_cc_verification` 및 `keyword_cc_name`도 참조합니다.</span><span class="sxs-lookup"><span data-stu-id="6425d-p123">The XML file also references  `keyword_cc_verification` and  `keyword_cc_name`, which are lists of keywords from which we are looking for matches within the  `patternsProximity` for the entity. These aren't currently displayed in the XML.  </span></span><br/> |
|<span data-ttu-id="6425d-191">패턴</span><span class="sxs-lookup"><span data-stu-id="6425d-191">Pattern</span></span>  <br/> |<span data-ttu-id="6425d-p124">패턴은 중요한 유형이 검색할 항목 목록을 포함합니다. 여기에는 키워드, regex 및 내부 함수(체크섬 확인 등의 작업 수행)가 포함됩니다. 중요한 정보 유형에는 고유한 신뢰도를 갖는 여러 패턴이 있을 수 있습니다. 증빙이 발견되면 높은 신뢰도를 반환하고, 증빙이 거의 없거나 전혀 없으면 낮은 신뢰도를 반환하는 중요한 정보 유형을 만들면 유용합니다.</span><span class="sxs-lookup"><span data-stu-id="6425d-p124">The pattern contains the list of what the sensitive type is looking for. This includes keywords, regexes, and internal functions (that perform tasks like verifying checksums). Sensitive information types can have multiple patterns with unique confidences. This is useful when creating a sensitive information type that returns a high confidence if corroborative evidence is found and a lower confidence if little or no corroborative evidence is found.</span></span>  <br/> |
|<span data-ttu-id="6425d-196">패턴 confidenceLevel</span><span class="sxs-lookup"><span data-stu-id="6425d-196">Pattern confidenceLevel</span></span>  <br/> |<span data-ttu-id="6425d-p125">DLP 엔진이 일치 항목을 발견한 신뢰도입니다. 이 수준의 신뢰도는 패턴 요구 사항이 충족될 경우 패턴의 일치와 연관됩니다. ETR(Exchange 전송 규칙)을 사용할 때 고려해야 하는 신뢰도 측정값입니다.</span><span class="sxs-lookup"><span data-stu-id="6425d-p125">This is the level of confidence that the DLP engine found a match. This level of confidence is associated with a match for the pattern if the pattern's requirements are met. This is the confidence measure you should consider when using Exchange transport rules (ETRs).</span></span>  <br/> |
|<span data-ttu-id="6425d-200">patternsProximity</span><span class="sxs-lookup"><span data-stu-id="6425d-200">patternsProximity</span></span>  <br/> |<span data-ttu-id="6425d-201">신용 카드 번호 패턴처럼 보이는 항목이 있는 경우 `patternsProximity`는 증빙을 찾게 되는 해당 번호 주변의 근접 범위를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="6425d-201">When we find what looks like a credit card number pattern,  `patternsProximity` is the proximity around that number where we'll look for corroborative evidence.</span></span>  <br/> |
|<span data-ttu-id="6425d-202">recommendedConfidence</span><span class="sxs-lookup"><span data-stu-id="6425d-202">recommendedConfidence</span></span>  <br/> |<span data-ttu-id="6425d-p126">이 규칙에 대해 권장되는 신뢰도입니다. 권장 신뢰도는 엔터티 및 선호도에 적용됩니다. 엔터티의 경우 이 값은 패턴의 `confidenceLevel`에 대해 평가되지 않으며, 적용하려는 신뢰도를 선택하는 데 도움이 되는 권장 사항일 뿐입니다. 선호도의 경우 ETR 작업이 호출되려면 패턴의 `confidenceLevel`이 `recommendedConfidence` 값보다 커야 합니다. `recommendedConfidence`는 작업을 호출하는 ETR에서 사용되는 기본 신뢰도입니다. 원할 경우 대신 패턴의 신뢰도를 기준으로 호출할 ETR을 수동으로 변경할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6425d-p126">This is the confidence level we recommend for this rule. The recommended confidence applies to entities and affinities. For entities, this number is never evaluated against the  `confidenceLevel` for the pattern. It's merely a suggestion to help you choose a confidence level if you want to apply one. For affinities, the  `confidenceLevel` of the pattern must be higher than the  `recommendedConfidence` number for an ETR action to be invoked. The  `recommendedConfidence` is the default confidence level used in ETRs that invokes an action. If you want, you can manually change the ETR to be invoked based off the pattern's confidence level, instead.  </span></span><br/> |
   
## <a name="for-more-information"></a><span data-ttu-id="6425d-210">자세한 내용</span><span class="sxs-lookup"><span data-stu-id="6425d-210">For more information</span></span>

- [<span data-ttu-id="6425d-211">중요한 정보 유형이 찾는 항목</span><span class="sxs-lookup"><span data-stu-id="6425d-211">What the sensitive information types look for</span></span>](what-the-sensitive-information-types-look-for.md)
    
- [<span data-ttu-id="6425d-212">사용자 지정 중요한 정보 유형 만들기</span><span class="sxs-lookup"><span data-stu-id="6425d-212">Create a custom sensitive information type</span></span>](create-a-custom-sensitive-information-type.md)
    
- [<span data-ttu-id="6425d-213">데이터 손실 방지 정책 개요</span><span class="sxs-lookup"><span data-stu-id="6425d-213">Overview of data loss prevention policies</span></span>](data-loss-prevention-policies.md)
    

