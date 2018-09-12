---
title: 사용자 지정 중요한 정보 유형 만들기
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 10/5/2017
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Priority
ms.collection: Strat_O365_IP
search.appverid:
- MOE150
- MET150
ms.assetid: 82c382a5-b6db-44fd-995d-b333b3c7fc30
description: '다른 유형의 중요한 정보(예: 조직 고유의 형식을 사용하는 직원 ID)를 식별하고 보호해야 할 경우 사용자 지정 중요한 정보 유형을 만들 수 있습니다. 중요한 정보 유형은 규칙 패키지라는 XML 파일에 정의됩니다. 이 항목에서는 고유한 사용자 지정 중요한 정보 유형을 정의하는 XML 파일을 만드는 방법을 보여 줍니다. 사용자는 정규식을 만드는 방법을 알아야 합니다.'
ms.openlocfilehash: 56683dd8ceac286f79084d2c2f19f48f5849a02f
ms.sourcegitcommit: 4be502d1fc6cbaef4c72d599758d51efe3a173c9
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/06/2018
ms.locfileid: "23849431"
---
# <a name="create-a-custom-sensitive-information-type"></a><span data-ttu-id="c05ab-106">사용자 지정 중요한 정보 유형 만들기</span><span class="sxs-lookup"><span data-stu-id="c05ab-106">Create a custom sensitive information type</span></span>

<span data-ttu-id="c05ab-p102">Office 365의 DLP(데이터 손실 방지)에는 DLP 정책에서 바로 사용할 수 있는 많은 [중요한 정보 유형](what-the-sensitive-information-types-look-for.md)이 포함되어 있습니다. 이러한 기본 제공 유형은 신용 카드 번호, 은행 계좌 번호, 여권 번호 등을 식별하고 보호하는 데 도움이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c05ab-p102">Data loss prevention (DLP) in Office 365 includes many [sensitive information types](what-the-sensitive-information-types-look-for.md) that are ready for you to use in your DLP policies. These built-in types can help identify and protect credit card numbers, bank account numbers, passport numbers, and more.</span></span> 
  
<span data-ttu-id="c05ab-p103">그렇지만 다른 유형의 중요한 정보(예: 조직 고유의 형식을 사용하는 직원 ID)를 식별하고 보호해야 할 경우 사용자 지정 중요한 정보 유형을 만들 수 있습니다. 중요한 정보 유형은 규칙 패키지라는 XML 파일에 정의됩니다.</span><span class="sxs-lookup"><span data-stu-id="c05ab-p103">But if you need to identify and protect a different type of sensitive information - for example, an employee ID that uses a format specific to your organization - you can create a custom sensitive information type. A sensitive information type is defined in an XML file called a rule package.</span></span>
  
<span data-ttu-id="c05ab-p104">이 항목에서는 고유한 사용자 지정 중요한 정보 유형을 정의하는 XML 파일을 만드는 방법을 보여 줍니다. 사용자는 정규식을 만드는 방법을 알아야 합니다. 한 가지 예로, 이 항목에서는 직원 ID를 식별하는 사용자 지정 중요한 정보 유형을 만듭니다. 이 예제 XML을 고유한 XML 파일의 시작점으로 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c05ab-p104">This topic shows you how to create an XML file that defines your own custom sensitive information type. You need to know how to create a regular expression. As an example, this topic creates a custom sensitive information type that identifies an employee ID. You can use this example XML as a starting point for your own XML file.</span></span>
  
<span data-ttu-id="c05ab-p105">잘 구성된 XML 파일을 만들었으면 PowerShell을 사용하여 Office 365에 업로드할 수 있습니다. 그러면 DLP 정책에서 해당 사용자 지정 중요한 정보 유형을 사용하고 중요한 정보가 의도대로 감지되는지 테스트할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c05ab-p105">After you've created a well-formed XML file, you can upload it to Office 365 by using PowerShell. Then you're ready to use your custom sensitive information type in your DLP policies and test that it's detecting the sensitive information as you intended.</span></span>

## <a name="important-disclaimer"></a><span data-ttu-id="c05ab-117">중요 고지 사항</span><span class="sxs-lookup"><span data-stu-id="c05ab-117">Important disclaimer</span></span>

<span data-ttu-id="c05ab-p106">고객 환경 및 콘텐츠 일치 요구의 차이 때문에 Microsoft 지원 서비스는고객 콘텐츠 일치 정의(예: 사용자 지정 분류 또는 정규식 패턴(“RegEx”) 정의)를 제공하도록 지원할 수 없습니다. 고객 콘텐츠 일치 개발, 테스트 및 디버그를 위해 Office 365 고객은 내부 IT 리소스에 의존하거나 MCS(Microsoft 컨설팅 서비스)와 같은 외부 컨설팅 리소스에 의존해야 합니다. 지원 엔지니어는 이 기능에 대해 제한된 지원을 제공할 수 있지만 사용자 지정 콘텐츠 일치 개발이 고객의 요구나 의무를 이행할 것이라는 보장을 제공할 수 없습니다. 제공될 수 있는 지원 유형의 예로, 테스트 목적으로 샘플 정규식 패턴이 제공될 수 있습니다. 또는 지원 서비스는 단일 특정 콘텐츠 예제에서 예상대로 트리거되지 않는 기존 RegEx 패턴 문제를 해결하는 데 도움을 줄 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c05ab-p106">Due to the variances in customer environments and content match requirements, Microsoft Support cannot assist in providing custom content-matching definitions – e.g. defining custom classifications or regular expression patterns (“RegEx”). For custom content-matching development, testing, and debugging, Office 365 customers will need to rely upon internal IT resources, or use an external consulting resource such as Microsoft Consulting Services (MCS).  Support engineers can provide limited support for the feature, but cannot provide assurances that any custom content-matching development will fulfill the customer’s requirements or obligations.  As an example of the type of support which can be provided, sample regular expression patterns may be provided for testing purposes. Or support can assist with troubleshooting an existing RegEx pattern which is not triggering as expected with a single specific content example.</span></span>

 <span data-ttu-id="c05ab-123">텍스트를 처리하는 데 사용되는 .NET regex 엔진에 대한 자세한 내용은 [.NET의 정규식](https://docs.microsoft.com/ko-KR/dotnet/standard/base-types/regular-expressions)에 대한 설명서를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="c05ab-123">For additional information on the .NET regex engine that's used for processing the text, see the documentaiton on [Regular Expressions in .NET](https://docs.microsoft.com/ko-KR/dotnet/standard/base-types/regular-expressions).</span></span>
    
## <a name="sample-xml-of-a-rule-package"></a><span data-ttu-id="c05ab-124">규칙 패키지의 샘플 XML</span><span class="sxs-lookup"><span data-stu-id="c05ab-124">Sample XML of a rule package</span></span>

<span data-ttu-id="c05ab-p107">다음은 이 항목에서 만들 규칙 패키지의 샘플 XML입니다. 요소와 특성은 다음 섹션에 설명됩니다.</span><span class="sxs-lookup"><span data-stu-id="c05ab-p107">Here's the sample XML of the rule package that we'll create in this topic. Elements and attributes are explained in the sections below.</span></span>
  
```
<?xml version="1.0" encoding="UTF-16"?>
<RulePackage xmlns="http://schemas.microsoft.com/office/2011/mce">
<RulePack id="DAD86A92-AB18-43BB-AB35-96F7C594ADAA">
    <Version build="0" major="1" minor="0" revision="0"/>
    <Publisher id="619DD8C3-7B80-4998-A312-4DF0402BAC04"/>
    <Details defaultLangCode="en-us">
        <LocalizedDetails langcode="en-us">
            <PublisherName>Contoso</PublisherName>
            <Name>Employee ID Custom Rule Pack</Name>
            <Description>
            This rule package contains the custom Employee ID entity.
            </Description>
        </LocalizedDetails>
    </Details>
</RulePack>
<Rules>
<!-- Employee ID -->
    <Entity id="E1CC861E-3FE9-4A58-82DF-4BD259EAB378" patternsProximity="300" recommendedConfidence="70">
        <Pattern confidenceLevel="60">
            <IdMatch idRef="Regex_employee_id"/>
        </Pattern>
        <Pattern confidenceLevel="70">
            <IdMatch idRef="Regex_employee_id"/>
            <Match idRef="Func_us_date"/>
        </Pattern>
        <Pattern confidenceLevel="80">
            <IdMatch idRef="Regex_employee_id"/>
            <Match idRef="Func_us_date"/>
            <Any minMatches="1">
                <Match idRef="Keyword_badge" minCount="2"/>
                <Match idRef="Keyword_employee"/>
            </Any>
            <Any minMatches="0" maxMatches="0">
                <Match idRef="Keyword_false_positives_local"/>
                <Match idRef="Keyword_false_positives_intl"/>
            </Any>
        </Pattern>
    </Entity>
    <Regex id="Regex_employee_id">(\s)(\d{9})(\s)</Regex>
    <Keyword id="Keyword_employee">
        <Group matchStyle="word">
            <Term>Identification</Term>
            <Term>Contoso Employee</Term>
        </Group>
    </Keyword>
    <Keyword id="Keyword_badge">
        <Group matchStyle="string">
            <Term>card</Term>
            <Term>badge</Term>
            <Term caseSensitive="true">ID</Term>
        </Group>
    </Keyword>
    <Keyword id="Keyword_false_positives_local">
        <Group matchStyle="word">
            <Term>credit card</Term>
            <Term>national ID</Term>
        </Group>
    </Keyword>
    <Keyword id="Keyword_false_positives_intl">
        <Group matchStyle="word">
            <Term>identity card</Term>
            <Term>national ID</Term>
            <Term>EU debit card</Term>
        </Group>
    </Keyword>
    <LocalizedStrings>
        <Resource idRef="E1CC861E-3FE9-4A58-82DF-4BD259EAB378">
            <Name default="true" langcode="en-us">Employee ID</Name>
            <Description default="true" langcode="en-us">
            A custom classification for detecting Employee IDs.
            </Description>
            <Name default="true" langcode="de-de">Name for German locale</Name>
            <Description default="true" langcode="de-de">
            Description for German locale.
            </Description>
        </Resource>
    </LocalizedStrings>
</Rules>
</RulePackage>

```

## <a name="what-are-your-key-requirements-rule-entity-pattern-elements"></a><span data-ttu-id="c05ab-p108">주요 요구 사항은 무엇인가요? [Rule, Entity, Pattern 요소]</span><span class="sxs-lookup"><span data-stu-id="c05ab-p108">What are your key requirements? [Rule, Entity, Pattern elements]</span></span>

<span data-ttu-id="c05ab-129">시작하기 전에 규칙에 대한 XML 스키마의 기본 구조와 이 구조를 사용하여 올바른 콘텐츠를 식별하도록 사용자 지정 중요한 정보 유형을 정의하는 방법을 이해하면 도움이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c05ab-129">Before you get started, it's helpful to understand the basic structure of the XML schema for a rule, and how you can use this structure to define your custom sensitive information type so that it will identify the right content.</span></span>
  
<span data-ttu-id="c05ab-p109">규칙은 하나 이상의 엔터티(중요 한 정보 유형)를 정의하고, 각 엔터티는 하나 이상의 패턴을 정의합니다. 패턴은 전자 메일이나 문서와 같은 콘텐츠를 평가할 때 DLP가 검색하는 항목을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="c05ab-p109">A rule defines one or more entities (sensitive information types), and each entity defines one or more patterns. A pattern is what DLP looks for when it evaluates content such as email and documents.</span></span>
  
<span data-ttu-id="c05ab-p110">(용어에 대한 참고 사항: DLP 정책에 익숙한 경우 정책에 조건 및 작업으로 구성되는 하나 이상의 규칙이 포함되어 있다는 사실을 알고 있을 것입니다. 그렇지만 이 항목에서 XML 태그는 규칙을 사용하여 중요한 정보 유형이라고도 하는 엔터티를 정의하는 패턴을 나타냅니다. 따라서 이 항목에서는 규칙이 나올 경우 조건 및 작업이 아닌 중요한 정보 유형으로 간주합니다.)</span><span class="sxs-lookup"><span data-stu-id="c05ab-p110">(A quick note on terminology - if you're familiar with DLP policies, you know that a policy contains one or more rules comprised of conditions and actions. However, in this topic, the XML markup uses rule to mean the patterns that define an entity, also known as a sensitive information type. So in this topic, when you see rule, think entity or sensitive information type, not conditions and actions.)</span></span>
  
### <a name="simplest-scenario-entity-with-one-pattern"></a><span data-ttu-id="c05ab-135">가장 간단한 시나리오: 하나의 패턴을 갖는 엔터티</span><span class="sxs-lookup"><span data-stu-id="c05ab-135">Simplest scenario: entity with one pattern</span></span>

<span data-ttu-id="c05ab-p111">다음은 가장 간단한 시나리오입니다. DLP 정책이 9자리 숫자로 구성된 조직의 직원 ID를 포함하는 콘텐츠를 식별하게 하려고 합니다. 따라서 패턴은 9자리 숫자를 식별하는 규칙에 포함된 정규식을 나타냅니다. 9자리 숫자를 포함하는 모든 콘텐츠는 해당 패턴을 충족합니다.</span><span class="sxs-lookup"><span data-stu-id="c05ab-p111">Here's the simplest scenario. You want your DLP policy to identify content that contains your organization's employee ID, which is formatted as a nine-digit number. So the pattern refers to a regular expression contained in the rule that identifies nine-digit numbers. Any content containing a nine-digit number satisfies the pattern.</span></span>
  
![하나의 패턴을 갖는 엔터티 다이어그램](media/4cc82dcf-068f-43ff-99b2-bac3892e9819.png)
  
<span data-ttu-id="c05ab-141">이 패턴은 간단하지만 9자리 숫자를 포함하는 콘텐츠를 일치시켜 직원 ID가 아닐 수 있는 많은 가양성을 식별할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c05ab-141">However, while simple, this pattern may identify many false positives by matching content that contains any nine-digit number that is not necessarily an employee ID.</span></span>
  
### <a name="more-common-scenario-entity-with-multiple-patterns"></a><span data-ttu-id="c05ab-142">좀 더 일반적인 시나리오: 여러 패턴을 갖는 엔터티</span><span class="sxs-lookup"><span data-stu-id="c05ab-142">More common scenario: entity with multiple patterns</span></span>

<span data-ttu-id="c05ab-143">이러한 이유로, 해당 엔터티(예: 9자리 숫자) 외에 뒷받침하는 증거(예: 키워드 또는 날짜)를 식별하는 패턴을 추가적으로 사용하여 엔터티를 정의하는 것이 좀 더 일반적입니다.</span><span class="sxs-lookup"><span data-stu-id="c05ab-143">For this reason, it's more common to define an entity by using more than one pattern, where the patterns identify supporting evidence (such as a keyword or date) in addition to the entity (such as a nine-digit number).</span></span>
  
<span data-ttu-id="c05ab-144">예를 들어, 직원 ID를 포함하는 콘텐츠를 식별할 확률을 높이기 위해, 채용 날짜도 식별하는 다른 패턴을 정의하고, 9자리 숫자 외에 채용 날짜와 키워드(예: “직원 ID”)를 둘 다 식별하는 또 다른 패턴을 정의할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c05ab-144">For example, to increase the likelihood of identifying content that contains an employee ID, you can define another pattern that also identifies a hire date, and define yet another pattern that identifies both a hire date and a keyword (such as "employee ID"), in addition to the nine-digit number.</span></span>
  
![여러 패턴을 갖는 엔터티 다이어그램](media/c8dc2c9d-00c6-4ebc-889a-53b41a90024a.png)
  
<span data-ttu-id="c05ab-146">이 구조는 다음과 같은 몇 가지 중요한 측면을 갖습니다.</span><span class="sxs-lookup"><span data-stu-id="c05ab-146">Note a couple of important aspects of this structure:</span></span>
  
- <span data-ttu-id="c05ab-p112">더 많은 증거를 요구하는 패턴일수록 신뢰도가 더 높습니다. 이러한 측면은 나중에 이 중요한 정보 유형을 DLP 정책에서 사용할 경우 신뢰도가 더 높은 좀 더 제한적인 작업(예: 콘텐츠 차단)과 신뢰도가 더 낮은 덜 제한적인 작업(예: 알림 보내기)을 사용할 수 있기 때문에 유용합니다.</span><span class="sxs-lookup"><span data-stu-id="c05ab-p112">Patterns that require more evidence have a higher confidence level. This is useful because when you later use this sensitive information type in a DLP policy, you can use more restrictive actions (such as block content) with only the higher-confidence matches, and you can use less restrictive actions (such as send notification) with the lower-confidence matches.</span></span>
    
- <span data-ttu-id="c05ab-p113">지원 IdMatch 및 Match 요소는 실제로 Pattern이 아닌 Rule 요소의 자식인 regex 및 키워드를 참조합니다. 이러한 지원 요소는 Pattern에서 참조되지만 Rule에 포함됩니다. 즉, 정규식이나 키워드 목록과 같은 지원 요소를 한 번 정의하여 여러 엔터티 및 패턴에서 참조할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c05ab-p113">The supporting IdMatch and Match elements reference regexes and keywords that are actually children of the Rule element, not the Pattern. These supporting elements are referenced by the Pattern but included in the Rule. This means that a single definition of a supporting element, like a regular expression or a keyword list, can be referenced by multiple entities and patterns.</span></span>
    
## <a name="what-entity-do-you-need-to-identify-entity-element-id-attribute"></a><span data-ttu-id="c05ab-p114">어떤 엔터티를 식별해야 하나요? [Entity 요소, ID 특성]</span><span class="sxs-lookup"><span data-stu-id="c05ab-p114">What entity do you need to identify? [Entity element, id attribute]</span></span>

<span data-ttu-id="c05ab-p115">엔터티는 잘 정의된 패턴을 갖는 신용 카드 번호와 같은 중요한 정보 유형입니다. 각 엔터티는 고유한 GUID를 해당 ID로 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="c05ab-p115">An entity is a sensitive information type, such as a credit card number, that has a well-defined pattern. Each entity has a unique GUID as its ID.</span></span>
  
### <a name="name-the-entity-and-generate-its-guid"></a><span data-ttu-id="c05ab-156">엔터티에 이름 지정 및 해당 GUID 생성</span><span class="sxs-lookup"><span data-stu-id="c05ab-156">Name the entity and generate its GUID</span></span>

<span data-ttu-id="c05ab-p116">Rules 및 Entity 요소를 추가합니다. 그런 후 사용자 지정 엔터티의 이름(이 예제에서는 직원 ID)을 포함하는 주석을 추가합니다. 나중에 이 엔터티 이름을 지역화된 문자열 섹션에 추가합니다. 그러면 해당 이름이 DLP 정책을 만들 때 UI에 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="c05ab-p116">Add the Rules and Entity elements. Then add a comment that contains the name of your custom entity - in this example, Employee ID. Later, you'll add the entity name to the localized strings section, and that name is what appears in the UI when you create a DLP policy.</span></span>
  
<span data-ttu-id="c05ab-p117">다음으로, 엔터티의 GUID를 생성합니다. GUID를 생성하는 방법에는 여러 가지가 있지만 PowerShell에서 [guid]::NewGuid()를 입력하여 쉽게 만들 수 있습니다. 나중에 엔터티 GUID 지역화된 문자열 섹션을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="c05ab-p117">Next, generate a GUID for your entity. There are several ways to generate GUIDs, but you can do it easily in PowerShell by typing [guid]::NewGuid(). Later, you'll also add the entity GUID to the localized strings section.</span></span>
  
![Rules 및 Entity 보여 주는 XML 태그 요소](media/c46c0209-0947-44e0-ac3a-8fd5209a81aa.png)
  
## <a name="what-pattern-do-you-want-to-match-pattern-element-idmatch-element-regex-element"></a><span data-ttu-id="c05ab-p118">일치하려는 패턴은 어느 것인가요? [Pattern 요소, IdMatch 요소, Regex 요소]</span><span class="sxs-lookup"><span data-stu-id="c05ab-p118">What pattern do you want to match? [Pattern element, IdMatch element, Regex element]</span></span>

<span data-ttu-id="c05ab-p119">패턴에는 중요한 정보 유형이 검색하는 항목 목록이 포함됩니다. 여기에는 regex, 키워드 및 기본 제공 함수(regex를 실행하여 날짜나 주소를 찾는 것과 같은 작업 수행)가 포함될 수 있습니다. 중요한 정보 유형은 고유한 신뢰도를 갖는 여러 패턴을 포함할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c05ab-p119">The pattern contains the list of what the sensitive information type is looking for. This can include regexes, keywords, and built-in functions (which perform tasks like running regexes to find dates or addresses). Sensitive information types can have multiple patterns with unique confidences.</span></span>
  
<span data-ttu-id="c05ab-p120">아래의 모든 패턴이 갖는 공통점은 모두가 공백 (\s) … (\s)으로 둘러싸인 9자리 숫자(\d{9})를 찾는 동일한 정규식을 참조한다는 것입니다. 이 정규식은 IdMatch 요소에서 참조되고 직원 ID 엔터티를 찾는 모든 패턴의 공통된 요구 사항입니다. IdMatch는 패턴이 직원 ID, 신용 카드 번호, 주민 등록 번호 등을 일치시킬 식별자입니다. Pattern 요소에는 IdMatch 요소가 1개만 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c05ab-p120">What all of the below patterns have in common is that they all reference the same regular expression, which looks for a nine-digit number (\d{9}) surrounded by white space (\s) … (\s). This regular expression is referenced by the IdMatch element and is the common requirement for all patterns that look for the Employee ID entity. IdMatch is the identifier that the pattern is to trying to match, such as Employee ID or credit card number or social security number. A Pattern element must have exactly one IdMatch element.</span></span>
  
![단일 Regex 요소를 참조하는 여러 Pattern 요소를 보여 주는 XML 태그](media/8f3f497b-3b8b-4bad-9c6a-d9abf0520854.png)
  
<span data-ttu-id="c05ab-p121">결과가 충족되면 패턴은 해당 개수 및 신뢰도를 반환합니다. 이 결과를 DLP 정책의 조건에서 사용할 수 있습니다. 중요한 정보 유형을 감지하는 조건을 DLP 정책에 추가하면 여기에 표시된 것처럼 개수 및 신뢰도를 편집할 수 있습니다. 신뢰도(일치 정확도라고도 함)는 이 항목의 뒷부분에서 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="c05ab-p121">When satisfied, a pattern returns a count and confidence level, which you can use in the conditions in your DLP policy. When you add a condition for detecting a sensitive information type to a DLP policy, you can edit the count and confidence level as shown here. Confidence level (also called match accuracy) is explained later in this topic.</span></span>
  
![인스턴스 개수 및 일치 정확도 옵션](media/11d0b51e-7c3f-4cc6-96d8-b29bcdae1aeb.png)
  
<span data-ttu-id="c05ab-p122">정규식을 만들 때 인식해야 하는 잠재적인 문제가 있을 수 있다는 사실을 고려해야 합니다. 예를 들어, 너무 많은 콘텐츠를 식별하는 regex를 작성하여 업로드하는 경우 성능에 영향을 줄 수 있습니다. 이러한 잠재적인 문제에 대한 자세한 내용은 뒷부분에 나오는 [인식해야 하는 잠재적인 유효성 검사 문제](#potential-validation-issues-to-be-aware-of)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="c05ab-p122">When you create your regular expression, keep in mind that there are potential issues to be aware of. For example, if you write and upload a regex that identifies too much content, this can impact performance. To learn more about these potential issues, see the later section [Potential validation issues to be aware of](#potential-validation-issues-to-be-aware-of).</span></span>
  
## <a name="do-you-want-to-require-additional-evidence-match-element-mincount-attribute"></a><span data-ttu-id="c05ab-p123">추가 증거를 요구하려고 하나요? [Match 요소, minCount 특성]</span><span class="sxs-lookup"><span data-stu-id="c05ab-p123">Do you want to require additional evidence? [Match element, minCount attribute]</span></span>

<span data-ttu-id="c05ab-184">패턴은 IdMatch 외에 Match 요소를 사용하여 키워드, regex, 날짜 또는 주소와 같은 추가적인 증거를 요구할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c05ab-184">In addition to the IdMatch, a pattern can use the Match element to require additional supporting evidence, such as a keyword, regex, date, or address.</span></span>
  
<span data-ttu-id="c05ab-p124">하나의 패턴에 여러 Match 요소가 포함될 수 있으며, 이러한 요소는 Pattern 요소에 직접 포함되거나 Any 요소를 사용해서 조합하여 사용할 수 있습니다. Match 요소는 암시적 AND 연산자로 조인됩니다. 패턴이 일치하려면 모든 Match 요소가 충족되어야 합니다. Any 요소를 사용하여 AND 또는 OR 연산자를 도입할 수 있습니다(뒷부분에 나오는 섹션에서 자세한 내용 제공).</span><span class="sxs-lookup"><span data-stu-id="c05ab-p124">A Pattern can include multiple Match elements; they can be included directly in the Pattern element or combined by using the Any element. Match elements are joined by an implicit AND operator; all Match elements must be satisfied for the pattern to be matched. You can use the Any element to introduce AND or OR operators (more on that in a later section).</span></span>
  
<span data-ttu-id="c05ab-p125">선택적인 minCount 특성을 사용하여 각 Match 요소에 대해 검색되어야 하는 일치 인스턴스 수를 지정할 수 있습니다. 예를 들어, 키워드 목록에서 두 개 이상의 키워드가 검색된 경우에만 패턴이 충족되도록 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c05ab-p125">You can use the optional minCount attribute to specify how many instances of a match need to be found for each of the Match elements. For example, you can specify that a pattern is satisfied only when at least two keywords from a keyword list are found.</span></span>
  
![minOccurs 특성을 갖는 Match 요소를 보여 주는 XML 태그](media/607f6b5e-2c7d-43a5-a131-a649f122e15a.png)
  
### <a name="keywords-keyword-group-and-term-elements-matchstyle-and-casesensitive-attributes"></a><span data-ttu-id="c05ab-191">키워드 [Keyword, Group 및 Term 요소, matchStyle 및 caseSensitive 특성]</span><span class="sxs-lookup"><span data-stu-id="c05ab-191">Keywords [Keyword, Group, and Term elements, matchStyle and caseSensitive attributes]</span></span>

<span data-ttu-id="c05ab-p126">직원 ID와 같은 중요한 정보를 식별할 경우 흔히 중요한 증거로 키워드를 사용할 수 있습니다. 예를 들어, 9자리 숫자를 일치시키는 것 외에도, "카드", "배지", "ID"와 같은 단어를 찾을 수 있습니다. 이렇게 하려면 Keyword 요소를 사용합니다. Keyword 요소에는 여러 패턴 또는 엔터티의 여러 Match 요소에서 참조할 수 있는 ID 특성이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c05ab-p126">When you identify sensitive information, like an employee ID, you often want to require keywords as corroborative evidence. For example, in addition to matching a nine-digit number, you may want to look for words like "card", "badge", or "ID". To do this, you use the Keyword element. The Keyword element has an id attribute that can be referenced by multiple Match elements in multiple patterns or entities.</span></span>
  
<span data-ttu-id="c05ab-p127">키워드는 Group 요소에 Term 요소 목록으로 포함됩니다. Group 요소에는 다음과 같은 두 값 중 하나를 갖는 matchStyle 특성이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c05ab-p127">Keywords are included as a list of Term elements in a Group element. The Group element has a matchStyle attribute with two possible values:</span></span>
  
- <span data-ttu-id="c05ab-p128">**matchStyle="word"** word 일치는 공백 또는 다른 구분 기호로 둘러싸인 전체 단어를 식별합니다. 단어의 일부를 일치시키거나 아시아 언어의 단어를 일치시켜야 하는 경우가 아니면 항상 word를 사용하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="c05ab-p128">**matchStyle="word"** Word match identifies whole words surrounded by white space or other delimiters. You should always use word unless you need to match parts of words or match words in Asian languages.</span></span> 
    
- <span data-ttu-id="c05ab-p129">**matchStyle="string"** string 일치는 무엇으로 둘러싸여 있는지에 관계없이 문자열을 식별합니다. 예를 들어, "id"는 "bid" 및 "idea"를 일치시킵니다. 아시아 단어를 일치시키거나 키워드를 다른 문자열의 일부로 포함할 수 있는 경우에만 string을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="c05ab-p129">**matchStyle="string"** String match identifies strings no matter what they're surrounded by. For example, "id" will match "bid" and "idea". Use string only when you need to match Asian words or if your keyword may be included as part of other strings.</span></span> 
    
<span data-ttu-id="c05ab-203">마지막으로, 콘텐츠가 대소문자를 포함하는 키워드와 정확히 일치하도록 지정하려면 하도록 Term 요소의 caseSensitive 특성을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c05ab-203">Finally, you can use the caseSensitive attribute of the Term element to specify that the content must match the keyword exactly, including lower- and upper-case letters.</span></span>
  
![키워드를 참조하는 Match 요소를 보여 주는 XML 태그](media/e729ba27-dec6-46f4-9242-584c6c12fd85.png)
  
### <a name="regular-expressions-regex-element"></a><span data-ttu-id="c05ab-205">정규식 [Regex 요소]</span><span class="sxs-lookup"><span data-stu-id="c05ab-205">Regular expressions [Regex element]</span></span>

<span data-ttu-id="c05ab-p130">이 예제에서 직원 ID 엔터티는 이미 IdMatch 요소를 사용하여 패턴, 즉 공백으로 둘러싸인 9자리 숫자에 대한 정규식을 참조합니다. 또한 패턴은 Match 요소를 사용하여 미국 우편 번호 형식의 5자리 또는 9자리 숫자와 같은 증빙을 식별하기 위해 추가 Regex 요소를 참조할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c05ab-p130">In this example, the employee ID entity already uses the IdMatch element to reference a regex for the pattern - a nine-digit number surrounded by whitespace. In addition, a pattern can use a Match element to reference an additional Regex element to identify corroborative evidence, such as a five- or nine-digit number in the format of a US zip code.</span></span>
  
### <a name="additional-patterns-such-as-dates-or-addresses-built-in-functions"></a><span data-ttu-id="c05ab-208">날짜 또는 주소와 같은 추가 패턴 [기본 제공 함수]</span><span class="sxs-lookup"><span data-stu-id="c05ab-208">Additional patterns such as dates or addresses [built-in functions]</span></span>

<span data-ttu-id="c05ab-p131">기본 제공 중요한 정보 유형에 외에도, DLP에는 미국 날짜, 유럽 날짜, 만료 날짜 또는 미국 주소와 같은 증빙을 식별할 수 있는 기본 제공 함수도 포함되어 있습니다. DLP는 고유의 사용자 지정 함수 업로드를 지원하지 않지만, 사용자 지정 중요한 정보 유형을 만들 때 엔터티가 기본 제공 함수를 참조할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c05ab-p131">In addition to the built-in sensitive information types, DLP also includes built-in functions that can identify corroborative evidence such as a US date, EU date, expiration date, or US address. DLP does not support uploading your own custom functions, but when you create a custom sensitive information type, your entity can reference the built-in functions.</span></span>
  
<span data-ttu-id="c05ab-211">예를 들어, 직원 ID 배지에 채용 날짜가 있는 경우 이 사용자 지정 엔터티는 기본 제공 함수 `Func_us_date`를 날짜가 미국에서 일반적으로 사용되는 형식을 갖는 날짜를 식별할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c05ab-211">For example, an employee ID badge has a hire date on it, so this custom entity can use the built-in function  `Func_us_date` to identify a date in the format commonly used in the US.</span></span> 
  
<span data-ttu-id="c05ab-212">자세한 내용은 [DLP 함수가 찾는 항목](what-the-dlp-functions-look-for.md)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="c05ab-212">For more information, see [What the DLP functions look for](what-the-dlp-functions-look-for.md).</span></span>
  
![기본 제공 함수를 참조하는 Match 요소를 보여 주는 XML 태그](media/dac6eae3-9c52-4537-b984-f9f127cc9c33.png)
  
## <a name="different-combinations-of-evidence-any-element-minmatches-and-maxmatches-attributes"></a><span data-ttu-id="c05ab-214">다양한 증거 조합 [Any 요소, minMatches 및 maxMatches 특성]</span><span class="sxs-lookup"><span data-stu-id="c05ab-214">Different combinations of evidence [Any element, minMatches and maxMatches attributes]</span></span>

<span data-ttu-id="c05ab-p132">Pattern 요소에서 모든 IdMatch 및 Match 요소는 암시적 AND 연산자로 조인됩니다. 즉, 패턴이 충족되기 위해서는 모든 일치 항목이 충족되어야 합니다. 그렇지만 Any 요소를 통해 Match 요소를 그룹화하여 좀 더 유연한 일치 논리를 만들 수 있습니다. 예를 들어, Any 요소를 사용하여 자식 Match 요소를 모두 일치시키거나 모두 일치시키지 않거나 정확한 하위 집합만 일치시킬 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c05ab-p132">In a Pattern element, all IdMatch and Match elements are joined by an implicit AND operator - all of the matches must be satisfied before the pattern can be satisfied. However, you can create more flexible matching logic by using the Any element to group Match elements. For example, you can use the Any element to match all, none, or an exact subset of its children Match elements.</span></span>
  
<span data-ttu-id="c05ab-p133">Any 요소에는 패턴이 일치되기 위해 충족되어야 하는 자식 Match 요소 수를 정의하는 데 사용할 수 있는 선택적 minMatches 및 maxMatches 특성이 있습니다. 이러한 특성은 일치를 위해 확인되는 증거 인스턴스 수가 아니라 충족되어야 하는 Match 요소의 수를 정의합니다. 특정 일치의 최소 인스턴스 수(예: 목록의 2개 키워드)를 정의하려면 Match 요소에 대해 minCount 특성을 사용합니다(위 내용 참조).</span><span class="sxs-lookup"><span data-stu-id="c05ab-p133">The Any element has optional minMatches and maxMatches attributes that you can use to define how many of the children Match elements must be satisfied before the pattern is matched. Note that these attributes define the number of Match elements that must be satisfied, not the number of instances of evidence found for the matches. To define a minimum number of instances for a specific match, such as two keywords from a list, use the minCount attribute for a Match element (see above).</span></span>
  
### <a name="match-at-least-one-child-match-element"></a><span data-ttu-id="c05ab-221">하나 이상의 자식 Match 요소 일치</span><span class="sxs-lookup"><span data-stu-id="c05ab-221">Match at least one child Match element</span></span>

<span data-ttu-id="c05ab-p134">최소 개수의 Match 요소만 충족되도록 요구하려는 경우 minMatches 특성을 사용할 수 있습니다. 실제로 Match 요소는 암시적 OR 연산자로 조인됩니다. 목록에서 미국 형식 날짜 또는 키워드가 발견되면 이 Any 요소가 충족됩니다.</span><span class="sxs-lookup"><span data-stu-id="c05ab-p134">If you want to require that only a minimum number of Match elements must be met, you can use the minMatches attribute. In effect, these Match elements are joined by an implicit OR operator. This Any element is satisfied if a US-formatted date or a keyword from either list is found.</span></span>
  
![minMatches 특성을 갖는 Any 요소를 보여 주는 XML 태그](media/385db1b1-571b-4a05-81b3-db28f5099c17.png)
  
### <a name="match-an-exact-subset-of-any-children-match-elements"></a><span data-ttu-id="c05ab-226">자식 Match 요소의 정확한 하위 집합 일치</span><span class="sxs-lookup"><span data-stu-id="c05ab-226">Match an exact subset of any children Match elements</span></span>

<span data-ttu-id="c05ab-p135">정확한 개수의 Match 요소가 충족되어야 하는 경우 minMatches 및 maxMatches를 같은 값으로 설정할 수 있습니다. 이 Any 요소는 정확히 하나의 날짜 또는 키워드가 검색되어야만 충족되며, 일치 항목 수가 더 있으면 패턴이 일치되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c05ab-p135">If you want to require that an exact number of Match elements must be met, you can set minMatches and maxMatches to the same value. This Any element is satisfied only if exactly one date or keyword is found - any more than that, and the pattern won't be matched.</span></span>
  
![minMatches 및 maxMatches 특성을 갖는 Any 요소를 보여 주는 XML 태그](media/97b10002-7781-42e8-ac5a-20ad8c5a887e.png)
  
### <a name="match-none-of-children-match-elements"></a><span data-ttu-id="c05ab-230">어떤 자식 Match 요소와도 일치하지 않음</span><span class="sxs-lookup"><span data-stu-id="c05ab-230">Match none of children Match elements</span></span>

<span data-ttu-id="c05ab-p136">패턴이 충족되기 위해 특정 증거가 없어야 하는 경우 minMatches와 maxMatches를 0으로 설정할 수 있습니다. 이 방식은 키워드 목록 또는 가양성을 나타낼 수 있는 기타 증거가 있는 경우에 유용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c05ab-p136">If you want to require the absence of specific evidence for a pattern to be satisfied, you can set both minMatches and maxMatches to 0. This can be useful if you have a keyword list or other evidence that are likely to indicate a false positive.</span></span>
  
<span data-ttu-id="c05ab-p137">예를 들어, 직원 ID 엔터티는 키워드 "card"를 찾습니다. 이것인 "ID card"를 나타낼 수 있기 때문입니다. 카드가 "credit card" 구에만 나타나면 해당 콘텐츠의 “card”는 “ID card”를 의미하지 않을 수 있습니다. 따라서 패턴을 충족하기 위해 제외하려는 용어 목록에 "credit card"를 키워드로 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c05ab-p137">For example, the employee ID entity looks for the keyword "card" because it might refer to an "ID card". However, if card appears only in the phrase "credit card", "card" in this content is unlikely to mean "ID card". So you can add "credit card" as a keyword to a list of terms that you want to exclude from satisfying the pattern.</span></span>
  
![maxMatches 특성 값 0을 표시하는 XML 태그](media/f81d44e5-3db8-48a8-8919-f483a386afdf.png)
  
## <a name="how-close-to-the-entity-must-the-other-evidence-be-patternsproximity-attribute"></a><span data-ttu-id="c05ab-p138">엔터티가 다른 증거와 얼마나 가까워야 하나요? [patternsProximity 특성]</span><span class="sxs-lookup"><span data-stu-id="c05ab-p138">How close to the entity must the other evidence be? [patternsProximity attribute]</span></span>

<span data-ttu-id="c05ab-p139">중요한 정보 유형은 직원 ID를 나타나는 패턴을 찾으며, 해당 패턴의 일부로 “ID”와 같은 키워드 등을 중요 증거로 찾습니다. 이 증거에 더 가까울수록 패턴이 실제 직원 ID일 확률이 높습니다. Entity 요소의 필수 patternsProximity 특성을 사용하여 패턴의 다른 증거가 엔터티에 얼마나 가까워야 하는지 결정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c05ab-p139">Your sensitive information type is looking for a pattern that represents an employee ID, and as part of that pattern it's also looking for corroborative evidence like a keyword such as "ID". It makes sense that the closer together this evidence is, the more likely the pattern is to be an actual employee ID. You can determine how close other evidence in the pattern must be to the entity by using the required patternsProximity attribute of the Entity element.</span></span>
  
![patternsProximity 특성을 보여 주는 XML 태그](media/e97eb7dc-b897-4e11-9325-91c742d9839b.png)
  
<span data-ttu-id="c05ab-p140">엔터티의 각 패턴에 대해, patternsProximity 특성 값은 해당 패턴에 대해 지정된 다른 모든 Match의 IdMatch 위치로부터 거리(유니코드 문자)를 정의합니다. 근접 범위는 IdMatch 위치에 의해 고정되며, 범위는 IdMatch의 좌우로 확장됩니다.</span><span class="sxs-lookup"><span data-stu-id="c05ab-p140">For each pattern in the entity, the patternsProximity attribute value defines the distance (in Unicode characters) from the IdMatch location for all other Matches specified for that Pattern. The proximity window is anchored by the IdMatch location, with the window extending to the left and right of the IdMatch.</span></span>
  
![근접 범위 다이어그램](media/b593dfd1-5eef-4d79-8726-a28923f7c31e.png)
  
<span data-ttu-id="c05ab-p141">아래 예제에서는 근접 범위가 사용자 지정 엔터티에 대한 IdMatch 요소가 하나 이상의 키워드 또는 날짜 증빙 일치를 요구하는 패턴 일치에 어떤 영향을 미치는지를 보여 줍니다. ID2 및 ID3의 경우 근접 범위 내에서 증빙을 찾을 수 없거나 부분적인 증빙만 발견되므로 ID1만 일치합니다.</span><span class="sxs-lookup"><span data-stu-id="c05ab-p141">The example below illustrates how the proximity window affects the pattern matching where IdMatch element for the employee ID custom entity requires at least one corroborating match of keyword or date. Only ID1 matches because for ID2 and ID3, either no or only partial corroborating evidence is found within the proximity window.</span></span>
  
![증빙 및 근접 범위 다이어그램](media/dc68e38e-dfa1-45b8-b204-89c8ba121f96.png)
  
<span data-ttu-id="c05ab-p142">전자 메일의 경우 메시지 본문과 각 첨부 파일이 별도 항목으로 취급됩니다. 즉, 근접 범위는 이러한 각 항목이 범위 너머까지 확장되지 않습니다. 각 항목(첨부 파일 또는 본문) 내에 idMatch 및 증빙이 둘 다 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c05ab-p142">Note that for email, the message body and each attachment are treated as separate items. This means that the proximity window does not extend beyond the end of each of these items. For each item (attachment or body), both the idMatch and corroborative evidence needs to reside in that item.</span></span>
  
## <a name="what-are-the-right-confidence-levels-for-different-patterns-confidencelevel-attribute-recommendedconfidence-attribute"></a><span data-ttu-id="c05ab-p143">여러 다른 패턴의 적정 신뢰도는 얼마나 되나요? [confidenceLevel 특성, recommendedConfidence 특성]</span><span class="sxs-lookup"><span data-stu-id="c05ab-p143">What are the right confidence levels for different patterns? [confidenceLevel attribute, recommendedConfidence attribute]</span></span>

<span data-ttu-id="c05ab-p144">패턴이 더 많은 증거를 요구할수록 패턴이 일치될 때 실제 엔터티(예: 직원 ID)가 식별될 신뢰도는 더 높아집니다. 예를 들어, 매우 근접한 9자리 ID 숫자, 채용 날짜, 키워드를 요구하는 패턴의 경우 9자리 ID 숫자만 요구하는 패턴의 경우보다 신뢰도가 더 높습니다.</span><span class="sxs-lookup"><span data-stu-id="c05ab-p144">The more evidence that a pattern requires, the more confidence you have that an actual entity (such as employee ID) has been identified when the pattern is matched. For example, you have more confidence in a pattern that requires a nine-digit ID number, hire date, and keyword in close proximity, than you do in a pattern that requires only a nine-digit ID number.</span></span>
  
<span data-ttu-id="c05ab-p145">Pattern 요소에는 필수 confidencelevel 특성이 있습니다. confidenceLevel 값(1에서 100 사이의 정수)을 엔터티의 각 패턴에 대한 고유 ID로 생각할 수 있습니다. 즉, 엔터티의 패턴에는 다른 신뢰도가 할당되어야 합니다. 정수 정밀도 값은 중요하지 않습니다. 준수 팀에서 허용하는 숫자만 선택하면 됩니다. 사용자 지정 중요한 정보 유형을 업로드한 후 DLP 정책을 만든 후에 생성한 규칙의 조건에서 이러한 신뢰도를 참조할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c05ab-p145">The Pattern element has a required confidenceLevel attribute. You can think of the value of confidenceLevel (an integer between 1 and 100) as a unique ID for each pattern in an entity - the patterns in an entity must have different confidence levels that you assign. The precise value of the integer doesn't matter - simply pick numbers that make sense to your compliance team. After you upload your custom sensitive information type and then create a DLP policy, you can reference these confidence levels in the conditions of the rules that you create.</span></span>
  
![다른 confidenceLevel 특성 값을 갖는 Pattern 요소를 보여 주는 XML 태그](media/301e0ba1-2deb-4add-977b-f6e9e18fba8b.png)
  
<span data-ttu-id="c05ab-p146">각 Pattern의 confidenceLevel 외에도, Entity에는 recommendedConfidence 특성이 있습니다. 권장되는 신뢰도 특성은 규칙의 기본 신뢰도로 생각할 수 있습니다. DLP 정책에서 규칙을 만들 경우 사용할 규칙의 신뢰도를 지정하지 않으면 규칙은 엔터티의 권장 신뢰도에 따라 일치됩니다.</span><span class="sxs-lookup"><span data-stu-id="c05ab-p146">In addition to confidenceLevel for each Pattern, the Entity has a recommendedConfidence attribute. The recommended confidence attribute can be thought of as the default confidence level for the rule. When you create a rule in a DLP policy, if you don't specify a confidence level for the rule to use, that rule will match based on the recommended confidence level for the entity.</span></span>
  
## <a name="do-you-want-to-support-other-languages-in-the-ui-of-the-security-amp-compliance-center-localizedstrings-element"></a><span data-ttu-id="c05ab-p147">보안 및 준수 센터의 UI에서 다른 언어를 지원하려고 하나요? [LocalizedStrings 요소]</span><span class="sxs-lookup"><span data-stu-id="c05ab-p147">Do you want to support other languages in the UI of the Security &amp; Compliance Center? [LocalizedStrings element]</span></span>

<span data-ttu-id="c05ab-p148">준수 팀에서 Office 365 보안 및 준수 센터를 사용하여 다른 로캘 및 다른 언어로 DLP 정책을 만드는 경우 사용자 지정 중요한 정보 유형의 지역화된 이름 및 설명 버전을 제공할 수 있습니다. 준수 팀에서 지원되는 언어로 Office 365를 사용하는 경우 UI에 지역화된 이름이 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="c05ab-p148">If your compliance team uses the Office 365 Security &amp; Compliance Center to create DLP policies in different locales and in different languages, you can provide localized versions of the name and description of your custom sensitive information type. When your compliance team uses Office 365 in a language that you support, they'll see the localized name in the UI.</span></span>
  
![인스턴스 개수 및 일치 정확도 옵션](media/11d0b51e-7c3f-4cc6-96d8-b29bcdae1aeb.png)
  
<span data-ttu-id="c05ab-p149">Rules 요소는 사용자 지정 엔터티의 GUID를 참조하는 Resource 요소가 포함된 LocalizedStrings 요소를 포함해야 합니다. 마찬가지로, 각 Resource 요소는 각각이 langcode 특성을 사용하여 특정 언어에 대해 지역화된 문자열을 제공하는 하나 이상의 Name 및 Description 요소를 포함합니다.</span><span class="sxs-lookup"><span data-stu-id="c05ab-p149">The Rules element must contain a LocalizedStrings element, which contains a Resource element that references the GUID of your custom entity. In turn, each Resource element contains one or more Name and Description elements that each use the langcode attribute to provide a localized string for a specific language.</span></span>
  
![LocalizedStrings 요소의 내용을 보여 주는 XML 태그](media/a96fc34a-b93d-498f-8b92-285b16a7bbe6.png)
  
<span data-ttu-id="c05ab-p150">보안 및 준수 센터의 UI에 사용자 지정 중요한 정보 유형이 표시될 때만 지역화된 문자열을 사용합니다. 키워드 목록 또는 정규식의 다른 지역화된 버전을 제공할 때는 지역화된 문자열을 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="c05ab-p150">Note that you use localized strings only for how your custom sensitive information type appears in the UI of the Security &amp; Compliance Center. You can't use localized strings to provide different localized versions of a keyword list or regular expression.</span></span>
  
## <a name="other-rule-package-markup-rulepack-guid"></a><span data-ttu-id="c05ab-274">다른 규칙 패키지 태그 [RulePack GUID]</span><span class="sxs-lookup"><span data-stu-id="c05ab-274">Other rule package markup [RulePack GUID]</span></span>

<span data-ttu-id="c05ab-p151">마지막으로, 각 RulePackage의 시작 부분에는 채워야 하는 일반적인 정보가 포함되어 있습니다. 다음 태그를 템플릿으로 사용하고 ". . ." 자리 표시자를 사용자 고유의 정보로 바꿀 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c05ab-p151">Finally, the beginning of each RulePackage contains some general information that you need to fill in. You can use the following markup as a template and replace the ". . ." placeholders with your own info.</span></span>
  
<span data-ttu-id="c05ab-p152">가장 중요한 점은 RulePack의 GUID를 생성해야 한다는 것입니다. 그뿐 아니라 엔터티의 GUID를 생성했을 것입니다. 이 GUID는 RulePack의 두 번째 GUID입니다. GUID를 생성하는 방법에는 몇 가지가 있지만 PowerShell에서 [guid]::NewGuid()를 입력하여 쉽게 생성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c05ab-p152">Most importantly, you'll need to generate a GUID for the RulePack. Above, you generated a GUID for the entity; this is a second GUID for the RulePack. There are several ways to generate GUIDs, but you can do it easily in PowerShell by typing [guid]::NewGuid().</span></span>
  
<span data-ttu-id="c05ab-p153">Version 요소도 중요합니다. 처음으로 규칙 패키지를 업로드하면, Office 365에서 버전 번호를 표시합니다. 나중에 규칙 패키지를 업데이트하고 새 버전을 업로드하는 경우 해당 버전 번호를 업데이트해야 합니다. 그렇지 않으면 Office 365에서 규칙 패키지를 배포하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c05ab-p153">The Version element is also important. When you upload your rule package for the first time, Office 365 notes the version number. Later, if you update the rule package and upload a new version, make sure to update the version number or Office 365 won't deploy the rule package.</span></span>
  
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
    . . .
 </Rules>
</RulePackage>

```

<span data-ttu-id="c05ab-286">완료되면 RulePack 요소는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="c05ab-286">When complete, your RulePack element should look like this.</span></span>
  
![RulePack 요소를 보여 주는 XML 태그](media/fd0f31a7-c3ee-43cd-a71b-6a3813b21155.png)
  
## <a name="changes-for-exchange-online"></a><span data-ttu-id="c05ab-288">Exchange Online의 변경</span><span class="sxs-lookup"><span data-stu-id="c05ab-288">Changes for Exchange Online</span></span>

<span data-ttu-id="c05ab-p154">이전에는 Exchange Online PowerShell을 사용하여 DLP에 대한 사용자 지정 중요한 정보 유형을 가져왔습니다. 이제 사용자 지정 중요한 정보 유형은 Exchange 관리 센터와 보안 및 준수 센터 둘 다에서 사용할 수 있습니다. 이러한 기능 개선의 일부로, 보안 및 준수 센터 PowerShell을 사용하여 사용자 지정 중요한 정보 유형을 가져와야 하며, 더 이상 Exchange Powershell에서 가져올 수 없습니다. 사용자 지정 중요한 정보 유형은 이전과 마찬가지로 계속 작동하지만 보안 및 준수 센터의 사용자 지정 중요한 정보 유형에 대한 변경 내용이 Exchange 관리 센터에 반영되는 데 최대 1시간이 소요될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c05ab-p154">Previously, you might have used Exchange Online PowerShell to import your custom sensitive information types for DLP. Now your custom sensitive information types can be used in both the Exchange Admin Center and the Security &amp; Compliance Center. As part of this improvement, you should use Security &amp; Compliance Center PowerShell to import your custom sensitive information types - you can't import them from the Exchange PowerShell anymore. Your custom sensitive information types will continue to work just like before; however, it may take up to one hour for changes made to custom sensitive information types in the Security &amp; Compliance Center to appear in the Exchange Admin Center.</span></span>
  
<span data-ttu-id="c05ab-p155">보안 및 준수 센터에서 `DlpSensitiveInformationTypeRulePackage` cmdlet을 사용하여 규칙 패키지를 업로드합니다. 이전에는 Exchange 관리 센터에서 `ClassificationRuleCollection` cmdlet을 사용했습니다.</span><span class="sxs-lookup"><span data-stu-id="c05ab-p155">Note that in the Security &amp; Compliance Center, you use the  `DlpSensitiveInformationTypeRulePackage` cmdlet to upload a rule package. Previously, in the Exchange Admin Center, you used the  `ClassificationRuleCollection` cmdlet.</span></span> 
  
## <a name="upload-your-rule-package"></a><span data-ttu-id="c05ab-295">규칙 패키지 업로드</span><span class="sxs-lookup"><span data-stu-id="c05ab-295">Upload your rule package</span></span>

<span data-ttu-id="c05ab-296">규칙 패키지를 업로드하려면 다음을 수행합니다.</span><span class="sxs-lookup"><span data-stu-id="c05ab-296">To upload your rule package, do the following.</span></span>
  
1. <span data-ttu-id="c05ab-297">유니코드 인코딩을 사용하여 .xml 파일로 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="c05ab-297">Save it as an .xml file with Unicode encoding.</span></span>
    
2. [<span data-ttu-id="c05ab-298">원격 PowerShell을 사용하여 Office 365 보안 및 준수 센터에 연결</span><span class="sxs-lookup"><span data-stu-id="c05ab-298">Connect to the Office 365 Security &amp; Compliance Center using remote PowerShell</span></span>](http://go.microsoft.com/fwlink/?LinkID=799771&amp;clcid=0x409)
    
3. <span data-ttu-id="c05ab-299">보안 및 준수 센터 PowerShell에서 New-DlpSensitiveInformationTypeRulePackage -FileData (Get-Content -Path "C:\custompath\MyNewRulePack.xml" -Encoding Byte)를 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="c05ab-299">In the Security &amp; Compliance Center PowerShell, type New-DlpSensitiveInformationTypeRulePackage -FileData (Get-Content -Path "C:\custompath\MyNewRulePack.xml" -Encoding Byte).</span></span>
    
    <span data-ttu-id="c05ab-p156">규칙 팩이 실제로 저장된 파일 위치를 사용해야 합니다. C:\custompath\는 자리 표시자입니다.</span><span class="sxs-lookup"><span data-stu-id="c05ab-p156">Make sure that you use the file location where your rule pack is actually stored. C:\custompath\ is a placeholder.</span></span>
    
4. <span data-ttu-id="c05ab-302">확인하려면 Y를 입력하고 Enter 키를 누릅니다.</span><span class="sxs-lookup"><span data-stu-id="c05ab-302">To confirm, type Y, and then press ENTER.</span></span>
    
5. <span data-ttu-id="c05ab-p157">Get-DlpSensitiveInformationType을 입력하고 모든 중요한 정보 유형을 확인하여 새 중요한 정보 유형이 업로드되었는지 검토합니다. 게시자 열을 확인하여 별도의 사용자 지정 중요한 정보 유형을 기본 제공된 정보 유형과 빠르게 구분할 수 있습니다. Get-DlpSensitiveInformationType -Identity "중요한 정보 유형의 이름"을 실행하여 특정 중요한 정보 유형으로 목록을 필터링할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c05ab-p157">Verify that your new sensitive information type was uploaded by typing Get-DlpSensitiveInformationType to see a list of all sensitive types. You can quickly separate custom sensitive information types from those which come built in by looking at the Publisher column. You can filter the list to a specific sensitive information type by running Get-DlpSensitiveInformationType -Identity "name of sensitive information type".</span></span>
    
## <a name="potential-validation-issues-to-be-aware-of"></a><span data-ttu-id="c05ab-306">인식해야 할 잠재적인 유효성 검사 문제</span><span class="sxs-lookup"><span data-stu-id="c05ab-306">Potential validation issues to be aware of</span></span>

<span data-ttu-id="c05ab-p158">규칙 패키지 XML 파일을 업로드할 때 시스템은 XML의 유효성을 검사하고 알려진 잘못된 패턴 및 명확한 성능 문제를 확인합니다. 다음은 유효성 검사가 정규식에서 확인하는 몇 가지 알려진 문제입니다.</span><span class="sxs-lookup"><span data-stu-id="c05ab-p158">When you upload your rule package XML file, the system validates the XML and checks for known bad patterns and obvious performance issues. Here are some known issues that the validation checks for — a regular expression:</span></span>
  
- <span data-ttu-id="c05ab-309">모든 항목을 일치시키는 "|" 표시는 비어 있는 일치로 간주되므로 정규식을 이 표시로 시작하거나 끝낼 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="c05ab-309">Cannot begin or end with alternator "|", which matches everything because it's considered an empty match.</span></span>
    
    <span data-ttu-id="c05ab-310">예를 들어, "|a" 또는 "b|"는 유효성 검사를 통과하지 못합니다.</span><span class="sxs-lookup"><span data-stu-id="c05ab-310">For example, "|a" or "b|" will not pass validation.</span></span>
    
- <span data-ttu-id="c05ab-311">".{0,m}" 패턴은 기능이 없고 성능을 저하시키기만 하므로 정규식을 이 패턴으로 시작하거나 끝낼 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="c05ab-311">Cannot begin or end with a ".{0,m}" pattern, which has no functional purpose and only impairs performance.</span></span>
    
    <span data-ttu-id="c05ab-312">예를 들어, ".{0,50}ASDF" 또는 "ASDF.{0,50}"는 유효성 검사를 통과하지 못합니다.</span><span class="sxs-lookup"><span data-stu-id="c05ab-312">For example, ".{0,50}ASDF" or "ASDF.{0,50}" will not pass validation.</span></span>
    
- <span data-ttu-id="c05ab-313">".{0,m}" 또는 ".{1,m}"을 그룹으로 사용할 수 없고, ".\*" 또는 ".+"를 그룹으로 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="c05ab-313">Cannot have ".{0,m}" or ".{1,m}" in groups, and cannot have ".\*" or ".+" in groups.</span></span>
    
    <span data-ttu-id="c05ab-314">예를 들어, "(.{0,50000})"은 유효성 검사를 통과하지 못합니다.</span><span class="sxs-lookup"><span data-stu-id="c05ab-314">For example, "(.{0,50000})" will not pass validation.</span></span>
    
- <span data-ttu-id="c05ab-315">"{0,m}" 또는 "{1,m}" 리피터가 그룹으로 포함된 문자는 정규식에 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="c05ab-315">Cannot have any character with "{0,m}" or "{1,m}" repeaters in groups.</span></span>
    
    <span data-ttu-id="c05ab-316">예를 들어, "(a\*)"는 유효성 검사를 통과하지 못합니다.</span><span class="sxs-lookup"><span data-stu-id="c05ab-316">For example, "(a\*)" will not pass validation.</span></span>
    
- <span data-ttu-id="c05ab-317">정규식을 ".{1,m}"으로 시작하거나 끝낼 수 없으며 "."만 사용해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c05ab-317">Cannot begin or end with ".{1,m}"; instead, use just "."</span></span>
    
    <span data-ttu-id="c05ab-318">예를 들어, ".{1,m}asdf"는 유효성 검사를 통과하지 못하므로 ".asdf"만 사용해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c05ab-318">For example, ".{1,m}asdf" will not pass validation; instead, use just ".asdf".</span></span>
    
- <span data-ttu-id="c05ab-319">바인딩되지 않은 리피터(예: "\*" 또는 "+")는 그룹으로 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="c05ab-319">Cannot have an unbounded repeater (such as "\*" or "+") on a group.</span></span>
    
    <span data-ttu-id="c05ab-320">예를 들어, "(xx)\*" 및 "(xx)+"는 유효성 검사를 통과하지 못합니다.</span><span class="sxs-lookup"><span data-stu-id="c05ab-320">For example, "(xx)\*" and "(xx)+" will not pass validation.</span></span>
    
<span data-ttu-id="c05ab-321">사용자 지정 중요한 정보 유형에 성능에 영향을 줄 수 있는 문제가 포함된 경우 업로드되지 않으며 다음 오류 메시지 중 하나가 표시될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c05ab-321">If a custom sensitive information type contains an issue that may affect performance, it won't be uploaded and you may see one of these error messages:</span></span>
  
- <span data-ttu-id="c05ab-322">**예상보다 더 많은 콘텐츠와 일치하는 일반 수량자(예: '+', '\*')**</span><span class="sxs-lookup"><span data-stu-id="c05ab-322">**Generic quantifiers which match more content than expected (e.g., '+', '\*')**</span></span>
    
- <span data-ttu-id="c05ab-323">**어설션 둘러보기**</span><span class="sxs-lookup"><span data-stu-id="c05ab-323">**Lookaround assertions**</span></span>
    
- <span data-ttu-id="c05ab-324">**일반 수량자와의 복잡한 그룹화**</span><span class="sxs-lookup"><span data-stu-id="c05ab-324">**Complex grouping in conjunction with general quantifiers**</span></span>
    
## <a name="recrawl-your-content-to-identify-the-sensitive-information"></a><span data-ttu-id="c05ab-325">콘텐츠를 다시 크롤링하여 중요한 정보 식별</span><span class="sxs-lookup"><span data-stu-id="c05ab-325">Recrawl your content to identify the sensitive information</span></span>

<span data-ttu-id="c05ab-p159">DLP는 검색 크롤러를 사용하여 사이트 콘텐츠에서 중요한 정보를 식별하고 분류합니다. SharePoint Online 및 비즈니스용 OneDrive 사이트의 콘텐츠는 업데이트될 때마다 자동으로 다시 크롤링됩니다. 하지만 기존의 모든 콘텐츠에 있는 새로운 사용자 지정 중요한 정보 유형을 식별하려면 해당 콘텐츠를 다시 크롤링해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c05ab-p159">DLP uses the search crawler to identify and classify sensitive information in site content. Content in SharePoint Online and OneDrive for Business sites is recrawled automatically whenever it's updated. But to identify your new custom type of sensitive information in all existing content, that content must be recrawled.</span></span>
  
<span data-ttu-id="c05ab-329">Office 365에서 전체 테넌트의 다시 크롤링을 수동으로 요청할 수 없으나 사이트 모음, 목록 또는 라이브러리에 대해서는 다시 크롤링을 요청할 수 있습니다. [사이트, 라이브러리 또는 목록의 크롤링 및 다시 인덱싱을 수동으로 요청](https://support.office.com/article/9afa977d-39de-4321-b4ca-8c7c7e6d264e)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="c05ab-329">In Office 365, you can't manually request a recrawl of an entire tenant, but you can do this for a site collection, list, or library - see [Manually request crawling and re-indexing of a site, a library or a list](https://support.office.com/article/9afa977d-39de-4321-b4ca-8c7c7e6d264e).</span></span>
  
## <a name="remove-a-custom-sensitive-information-type"></a><span data-ttu-id="c05ab-330">사용자 지정 중요한 정보 유형 제거</span><span class="sxs-lookup"><span data-stu-id="c05ab-330">Remove a custom sensitive information type</span></span>

1. [<span data-ttu-id="c05ab-331">원격 PowerShell을 사용하여 Office 365 보안 및 준수 센터에 연결</span><span class="sxs-lookup"><span data-stu-id="c05ab-331">Connect to the Office 365 Security &amp; Compliance Center using remote PowerShell</span></span>](http://go.microsoft.com/fwlink/?LinkID=799771&amp;clcid=0x409)
    
2. <span data-ttu-id="c05ab-332">보안 및 준수 센터 PowerShell에서 다음 중 하나를 수행합니다.</span><span class="sxs-lookup"><span data-stu-id="c05ab-332">In the Security &amp; Compliance Center PowerShell, do one of the following:</span></span>
    
  - <span data-ttu-id="c05ab-333">전체 규칙 패키지와 패키지에 포함된 모든 엔터티를 제거하려면</span><span class="sxs-lookup"><span data-stu-id="c05ab-333">To remove an entire rule package and all of the entities that it contains</span></span>
    
    <span data-ttu-id="c05ab-334">Remove-DlpSensitiveInformationTypeRulePackage "NameOfYourRulePack"을 입력합니다. 즉, 위의 예제 XML에서는 Remove-DlpSensitiveInformationTypeRulePackage "Employee ID Custom Rule Pack"을 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="c05ab-334">Type Remove-DlpSensitiveInformationTypeRulePackage "NameOfYourRulePack" - for the example XML above, you would type Remove-DlpSensitiveInformationTypeRulePackage "Employee ID Custom Rule Pack".</span></span>
    
    <span data-ttu-id="c05ab-335">규칙 패키지를 식별하려면 \<Rule Pack\> 요소의 \<Name\> 요소(언어 관련) 또는 RulePack 요소에 대한 ID 특성의 GUID를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c05ab-335">Note that to identify your rule package, you can use the \<Name\> element (for any language) in the \<Rule Pack\> element or the GUID of the id attribute of the RulePack element.</span></span>
    
  - <span data-ttu-id="c05ab-336">규칙 패키지에서 단일 엔터티를 제거하려면</span><span class="sxs-lookup"><span data-stu-id="c05ab-336">To remove a single entity from a rule package</span></span>
    
    <span data-ttu-id="c05ab-p160">Set-DlpSensitiveInformationTypeRulePackage를 사용하여 특정 엔터티가 제거된 새 버전의 규칙 팩을 업로드해야 합니다. 제거하기 전에 해당 중요한 정보 유형을 참조하는 DLP 정책이나 Exchange 전송 규칙이 없는지 확인해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c05ab-p160">You must upload a new version of your rulepack with that specific entity removed using Set-DlpSensitiveInformationTypeRulePackage. You'll need to make sure that no DLP policies or Exchange transport rules still reference the sensitive information type before removing it.</span></span>
    
3. <span data-ttu-id="c05ab-339">확인하려면 Y를 입력하고 Enter 키를 누릅니다.</span><span class="sxs-lookup"><span data-stu-id="c05ab-339">To confirm, type Y, and then press ENTER.</span></span>
    
4. <span data-ttu-id="c05ab-340">Get- DlpSensitiveInformationType을 입력할 때 중요한 정보 유형 이름의 더 이상 표시되지 않으면 새 규칙이 제거된 것입니다.</span><span class="sxs-lookup"><span data-stu-id="c05ab-340">Verify that your new rule was removed by typing Get- DlpSensitiveInformationType, which should no longer display the name of your sensitive information type.</span></span>
    
## <a name="reference-rule-package-xml-schema-definition"></a><span data-ttu-id="c05ab-341">참조: 규칙 패키지 XML 스키마 정의</span><span class="sxs-lookup"><span data-stu-id="c05ab-341">Reference: Rule package XML schema definition</span></span>

<span data-ttu-id="c05ab-342">이 태그를 복사하고, XSD 파일로 저장한 후 규칙 패키지 XML 파일의 유효성을 검사하는 데 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c05ab-342">You can copy this markup, save it as an XSD file, and use it to validate your rule package XML file.</span></span>
  
```
<?xml version="1.0" encoding="utf-8"?>
<xs:schema xmlns:mce="http://schemas.microsoft.com/office/2011/mce"
           targetNamespace="http://schemas.microsoft.com/office/2011/mce" 
           xmlns:xs="http://www.w3.org/2001/XMLSchema"
           elementFormDefault="qualified"
           attributeFormDefault="unqualified"
           id="RulePackageSchema">
  <!-- Use include if this schema has the same target namespace as the schema being referenced, otherwise use import -->
  <xs:element name="RulePackage" type="mce:RulePackageType"/>
  <xs:simpleType name="LangType">
    <xs:union memberTypes="xs:language">
      <xs:simpleType>
        <xs:restriction base="xs:string">
          <xs:enumeration value=""/>
        </xs:restriction>
      </xs:simpleType>
    </xs:union>
  </xs:simpleType>
  <xs:simpleType name="GuidType" final="#all">
    <xs:restriction base="xs:token">
      <xs:pattern value="[0-9a-fA-F]{8}\-([0-9a-fA-F]{4}\-){3}[0-9a-fA-F]{12}"/>
    </xs:restriction>
  </xs:simpleType>
  <xs:complexType name="RulePackageType">
    <xs:sequence>
      <xs:element name="RulePack" type="mce:RulePackType"/>
      <xs:element name="Rules" type="mce:RulesType">
        <xs:key name="UniqueRuleId">
          <xs:selector xpath="mce:Entity|mce:Affinity|mce:Version/mce:Entity|mce:Version/mce:Affinity"/>
          <xs:field xpath="@id"/>
        </xs:key>
        <xs:key name="UniqueProcessorId">
          <xs:selector xpath="mce:Regex|mce:Keyword|mce:Fingerprint"></xs:selector>
          <xs:field xpath="@id"/>
        </xs:key>
        <xs:key name="UniqueResourceIdRef">
          <xs:selector xpath="mce:LocalizedStrings/mce:Resource"/>
          <xs:field xpath="@idRef"/>
        </xs:key>        
        <xs:keyref name="ReferencedRuleMustExist" refer="mce:UniqueRuleId">
          <xs:selector xpath="mce:LocalizedStrings/mce:Resource"/>
          <xs:field xpath="@idRef"/>
        </xs:keyref>
        <xs:keyref name="RuleMustHaveResource" refer="mce:UniqueResourceIdRef">
          <xs:selector xpath="mce:Entity|mce:Affinity|mce:Version/mce:Entity|mce:Version/mce:Affinity"/>
          <xs:field xpath="@id"/>
        </xs:keyref>
      </xs:element>
    </xs:sequence>
  </xs:complexType>
  <xs:complexType name="RulePackType">
    <xs:sequence>
      <xs:element name="Version" type="mce:VersionType"/>
      <xs:element name="Publisher" type="mce:PublisherType"/>
      <xs:element name="Details" type="mce:DetailsType">
        <xs:key name="UniqueLangCodeInLocalizedDetails">
          <xs:selector xpath="mce:LocalizedDetails"/>
          <xs:field xpath="@langcode"/>
        </xs:key>
        <xs:keyref name="DefaultLangCodeMustExist" refer="mce:UniqueLangCodeInLocalizedDetails">
          <xs:selector xpath="."/>
          <xs:field xpath="@defaultLangCode"/>
        </xs:keyref>
      </xs:element>
      <xs:element name="Encryption" type="mce:EncryptionType" minOccurs="0" maxOccurs="1"/>
    </xs:sequence>
    <xs:attribute name="id" type="mce:GuidType" use="required"/>
  </xs:complexType>
  <xs:complexType name="VersionType">
    <xs:attribute name="major" type="xs:unsignedShort" use="required"/>
    <xs:attribute name="minor" type="xs:unsignedShort" use="required"/>
    <xs:attribute name="build" type="xs:unsignedShort" use="required"/>
    <xs:attribute name="revision" type="xs:unsignedShort" use="required"/>
  </xs:complexType>
  <xs:complexType name="PublisherType">
    <xs:attribute name="id" type="mce:GuidType" use="required"/>
  </xs:complexType>
  <xs:complexType name="LocalizedDetailsType">
    <xs:sequence>
      <xs:element name="PublisherName" type="mce:NameType"/>
      <xs:element name="Name" type="mce:RulePackNameType"/>
      <xs:element name="Description" type="mce:OptionalNameType"/>
    </xs:sequence>
    <xs:attribute name="langcode" type="mce:LangType" use="required"/>
  </xs:complexType>
  <xs:complexType name="DetailsType">
    <xs:sequence>
      <xs:element name="LocalizedDetails" type="mce:LocalizedDetailsType" maxOccurs="unbounded"/>
    </xs:sequence>
    <xs:attribute name="defaultLangCode" type="mce:LangType" use="required"/>
  </xs:complexType>
  <xs:complexType name="EncryptionType">
    <xs:sequence>
      <xs:element name="Key" type="xs:normalizedString"/>
      <xs:element name="IV" type="xs:normalizedString"/>
    </xs:sequence>
  </xs:complexType>
  <xs:simpleType name="RulePackNameType">
    <xs:restriction base="xs:token">
      <xs:minLength value="1"/>
      <xs:maxLength value="64"/>
    </xs:restriction>
  </xs:simpleType>
  <xs:simpleType name="NameType">
    <xs:restriction base="xs:normalizedString">
      <xs:minLength value="1"/>
      <xs:maxLength value="256"/>
    </xs:restriction>
  </xs:simpleType>
  <xs:simpleType name="OptionalNameType">
    <xs:restriction base="xs:normalizedString">
      <xs:minLength value="0"/>
      <xs:maxLength value="256"/>
    </xs:restriction>
  </xs:simpleType>
  <xs:simpleType name="RestrictedTermType">
    <xs:restriction base="xs:string">
      <xs:minLength value="1"/>
      <xs:maxLength value="100"/>
    </xs:restriction>
  </xs:simpleType>
  <xs:complexType name="RulesType">
    <xs:sequence>
      <xs:choice maxOccurs="unbounded">
        <xs:element name="Entity" type="mce:EntityType"/>
        <xs:element name="Affinity" type="mce:AffinityType"/>
        <xs:element name="Version" type="mce:VersionedRuleType"/>
      </xs:choice>
      <xs:choice minOccurs="0" maxOccurs="unbounded">
        <xs:element name="Regex" type="mce:RegexType"/>
        <xs:element name="Keyword" type="mce:KeywordType"/>
        <xs:element name="Fingerprint" type="mce:FingerprintType"/>
        <xs:element name="ExtendedKeyword" type="mce:ExtendedKeywordType"/>
      </xs:choice>
      <xs:element name="LocalizedStrings" type="mce:LocalizedStringsType"/>
    </xs:sequence>
  </xs:complexType>
  <xs:complexType name="EntityType">
    <xs:sequence>
      <xs:element name="Pattern" type="mce:PatternType" maxOccurs="unbounded"/>
      <xs:element name="Version" type="mce:VersionedPatternType" minOccurs="0" maxOccurs="unbounded" />
    </xs:sequence>
    <xs:attribute name="id" type="mce:GuidType" use="required"/>
    <xs:attribute name="patternsProximity" type="mce:ProximityType" use="required"/>
    <xs:attribute name="recommendedConfidence" type="mce:ProbabilityType"/>
    <xs:attribute name="workload" type="mce:WorkloadType"/>
  </xs:complexType>
  <xs:complexType name="PatternType">
    <xs:sequence>
      <xs:element name="IdMatch" type="mce:IdMatchType"/>
      <xs:choice minOccurs="0" maxOccurs="unbounded">
        <xs:element name="Match" type="mce:MatchType"/>
        <xs:element name="Any" type="mce:AnyType"/>
      </xs:choice>
    </xs:sequence>
    <xs:attribute name="confidenceLevel" type="mce:ProbabilityType" use="required"/>
  </xs:complexType>
  <xs:complexType name="AffinityType">
    <xs:sequence>
      <xs:element name="Evidence" type="mce:EvidenceType" maxOccurs="unbounded"/>
      <xs:element name="Version" type="mce:VersionedEvidenceType" minOccurs="0" maxOccurs="unbounded" />
    </xs:sequence>
    <xs:attribute name="id" type="mce:GuidType" use="required"/>
    <xs:attribute name="evidencesProximity" type="mce:ProximityType" use="required"/>
    <xs:attribute name="thresholdConfidenceLevel" type="mce:ProbabilityType" use="required"/>
    <xs:attribute name="workload" type="mce:WorkloadType"/>
  </xs:complexType>
  <xs:complexType name="EvidenceType">
    <xs:sequence>
      <xs:choice maxOccurs="unbounded">
        <xs:element name="Match" type="mce:MatchType"/>
        <xs:element name="Any" type="mce:AnyType"/>
      </xs:choice>
    </xs:sequence>
    <xs:attribute name="confidenceLevel" type="mce:ProbabilityType" use="required"/>
  </xs:complexType>
  <xs:complexType name="IdMatchType">
    <xs:attribute name="idRef" type="xs:string" use="required"/>
  </xs:complexType>
  <xs:complexType name="MatchType">
    <xs:attribute name="idRef" type="xs:string" use="required"/>
    <xs:attribute name="minCount" type="xs:positiveInteger" use="optional"/>
    <xs:attribute name="uniqueResults" type="xs:boolean" use="optional"/>
  </xs:complexType>
  <xs:complexType name="AnyType">
    <xs:sequence>
      <xs:choice maxOccurs="unbounded">
        <xs:element name="Match" type="mce:MatchType"/>
        <xs:element name="Any" type="mce:AnyType"/>
      </xs:choice>
    </xs:sequence>
    <xs:attribute name="minMatches" type="xs:nonNegativeInteger" default="1"/>
    <xs:attribute name="maxMatches" type="xs:nonNegativeInteger" use="optional"/>
  </xs:complexType>
  <xs:simpleType name="ProximityType">
    <xs:union>
      <xs:simpleType>
        <xs:restriction base='xs:string'>
          <xs:enumeration value="unlimited"/>
        </xs:restriction>
      </xs:simpleType>
      <xs:simpleType>
        <xs:restriction base="xs:positiveInteger">
          <xs:minInclusive value="1"/>
        </xs:restriction>
      </xs:simpleType>
    </xs:union>
  </xs:simpleType>
  <xs:simpleType name="ProbabilityType">
    <xs:restriction base="xs:integer">
      <xs:minInclusive value="1"/>
      <xs:maxInclusive value="100"/>
    </xs:restriction>
  </xs:simpleType>
  <xs:simpleType name="WorkloadType">
    <xs:restriction base="xs:string">
      <xs:enumeration value="Exchange"/>
      <xs:enumeration value="Outlook"/>
    </xs:restriction>
  </xs:simpleType>
  <xs:simpleType name="EngineVersionType">
    <xs:restriction base="xs:token">
      <xs:pattern value="^\d{2}\.01?\.\d{3,4}\.\d{1,3}$"/>
    </xs:restriction>
  </xs:simpleType>
  <xs:complexType name="VersionedRuleType">
    <xs:choice maxOccurs="unbounded">
      <xs:element name="Entity" type="mce:EntityType"/>
      <xs:element name="Affinity" type="mce:AffinityType"/>
    </xs:choice>
    <xs:attribute name="minEngineVersion" type="mce:EngineVersionType" use="required" />
  </xs:complexType>
  <xs:complexType name="VersionedPatternType">
    <xs:sequence>
      <xs:element name="Pattern" type="mce:PatternType" maxOccurs="unbounded"/>
    </xs:sequence>
    <xs:attribute name="minEngineVersion" type="mce:EngineVersionType" use="required" />
  </xs:complexType>
  <xs:complexType name="VersionedEvidenceType">
    <xs:sequence>
      <xs:element name="Evidence" type="mce:EvidenceType" maxOccurs="unbounded"/>
    </xs:sequence>
    <xs:attribute name="minEngineVersion" type="mce:EngineVersionType" use="required" />
  </xs:complexType>
  <xs:simpleType name="FingerprintValueType">
    <xs:restriction base="xs:string">
      <xs:minLength value="2732"/>
      <xs:maxLength value="2732"/>
    </xs:restriction>
  </xs:simpleType>
  <xs:complexType name="FingerprintType">
    <xs:simpleContent>
      <xs:extension base="mce:FingerprintValueType">
        <xs:attribute name="id" type="xs:token" use="required"/>
        <xs:attribute name="threshold" type="mce:ProbabilityType" use="required"/>
        <xs:attribute name="shingleCount" type="xs:positiveInteger" use="required"/>
        <xs:attribute name="description" type="xs:string" use="optional"/>
      </xs:extension>
    </xs:simpleContent>
  </xs:complexType>
  <xs:complexType name="RegexType">
    <xs:simpleContent>
      <xs:extension base="xs:string">
        <xs:attribute name="id" type="xs:token" use="required"/>
      </xs:extension>
    </xs:simpleContent>
  </xs:complexType>
  <xs:complexType name="KeywordType">
    <xs:sequence>
      <xs:element name="Group" type="mce:GroupType" maxOccurs="unbounded"/>
    </xs:sequence>
    <xs:attribute name="id" type="xs:token" use="required"/>
  </xs:complexType>
  <xs:complexType name="GroupType">
    <xs:sequence>
      <xs:choice>
        <xs:element name="Term" type="mce:TermType" maxOccurs="unbounded"/>
      </xs:choice>
    </xs:sequence>
    <xs:attribute name="matchStyle" default="word">
      <xs:simpleType>
        <xs:restriction base="xs:NMTOKEN">
          <xs:enumeration value="word"/>
          <xs:enumeration value="string"/>
        </xs:restriction>
      </xs:simpleType>
    </xs:attribute>
  </xs:complexType>
  <xs:complexType name="TermType">
    <xs:simpleContent>
      <xs:extension base="mce:RestrictedTermType">
        <xs:attribute name="caseSensitive" type="xs:boolean" default="false"/>
      </xs:extension>
    </xs:simpleContent>
  </xs:complexType>
  <xs:complexType name="ExtendedKeywordType">
    <xs:simpleContent>
      <xs:extension base="xs:string">
        <xs:attribute name="id" type="xs:token" use="required"/>
      </xs:extension>
    </xs:simpleContent>
  </xs:complexType>
  <xs:complexType name="LocalizedStringsType">
    <xs:sequence>
      <xs:element name="Resource" type="mce:ResourceType" maxOccurs="unbounded">
      <xs:key name="UniqueLangCodeUsedInNamePerResource">
        <xs:selector xpath="mce:Name"/>
        <xs:field xpath="@langcode"/>
      </xs:key>
      <xs:key name="UniqueLangCodeUsedInDescriptionPerResource">
        <xs:selector xpath="mce:Description"/>
        <xs:field xpath="@langcode"/>
      </xs:key>
    </xs:element>
    </xs:sequence>
  </xs:complexType>
  <xs:complexType name="ResourceType">
    <xs:sequence>
      <xs:element name="Name" type="mce:ResourceNameType" maxOccurs="unbounded"/>
      <xs:element name="Description" type="mce:DescriptionType" minOccurs="0" maxOccurs="unbounded"/>
    </xs:sequence>
    <xs:attribute name="idRef" type="mce:GuidType" use="required"/>
  </xs:complexType>
  <xs:complexType name="ResourceNameType">
    <xs:simpleContent>
      <xs:extension base="xs:string">
        <xs:attribute name="default" type="xs:boolean" default="false"/>
        <xs:attribute name="langcode" type="mce:LangType" use="required"/>
      </xs:extension>
    </xs:simpleContent>
  </xs:complexType>
  <xs:complexType name="DescriptionType">
    <xs:simpleContent>
      <xs:extension base="xs:string">
        <xs:attribute name="default" type="xs:boolean" default="false"/>
        <xs:attribute name="langcode" type="mce:LangType" use="required"/>
      </xs:extension>
    </xs:simpleContent>
  </xs:complexType>
</xs:schema>

```

## <a name="more-information"></a><span data-ttu-id="c05ab-343">추가 정보</span><span class="sxs-lookup"><span data-stu-id="c05ab-343">More information</span></span>

- [<span data-ttu-id="c05ab-344">데이터 손실 방지 정책 개요</span><span class="sxs-lookup"><span data-stu-id="c05ab-344">Overview of data loss prevention policies</span></span>](data-loss-prevention-policies.md)
    
- [<span data-ttu-id="c05ab-345">중요한 정보 유형이 찾는 항목</span><span class="sxs-lookup"><span data-stu-id="c05ab-345">What the sensitive information types look for</span></span>](what-the-sensitive-information-types-look-for.md)
    
- [<span data-ttu-id="c05ab-346">DLP 함수가 찾는 항목</span><span class="sxs-lookup"><span data-stu-id="c05ab-346">What the DLP functions look for</span></span>](what-the-dlp-functions-look-for.md)
    

