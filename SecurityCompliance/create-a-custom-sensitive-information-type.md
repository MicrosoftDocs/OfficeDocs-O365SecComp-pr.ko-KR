---
title: 사용자 지정 중요한 정보 유형 만들기
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Priority
ms.collection:
- M365-security-compliance
search.appverid:
- MOE150
- MET150
description: 보안 및 준수 센터의 그래픽 사용자 인터페이스에서 DLP에 대한 사용자 지정 중요한 정보 유형을 만들고, 수정, 제거 및 테스트하는 방법을 알아봅니다.
ms.openlocfilehash: de7bbc8ee624fe9468dc64a9811db31d529984bf
ms.sourcegitcommit: e7a776a04ef6ed5e287a33cfdc36aa2d72862b55
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/29/2019
ms.locfileid: "30999091"
---
# <a name="create-a-custom-sensitive-information-type"></a><span data-ttu-id="4fee3-103">사용자 지정 중요한 정보 유형 만들기</span><span class="sxs-lookup"><span data-stu-id="4fee3-103">Create a custom sensitive information type</span></span>

<span data-ttu-id="4fee3-p101">Office 365의 DLP(데이터 손실 방지)에는 DLP 정책에서 바로 사용할 수 있는 많은 기본 제공 [중요한 정보 유형](what-the-sensitive-information-types-look-for.md)이 포함되어 있습니다. 이러한 기본 제공 유형은 신용 카드 번호, 은행 계좌 번호, 여권 번호 등을 식별하고 보호하는 데 도움이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4fee3-p101">Data loss prevention (DLP) in Office 365 includes many built-in [sensitive information types](what-the-sensitive-information-types-look-for.md) that are ready for you to use in your DLP policies. These built-in types can help identify and protect credit card numbers, bank account numbers, passport numbers, and more.</span></span> 

<span data-ttu-id="4fee3-106">그렇지만 다른 유형의 중요한 정보(예: 조직 고유의 형식을 사용하는 직원 ID 또는 프로젝트 번호)를 식별하고 보호해야 할 경우 사용자 지정 중요한 정보 유형을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4fee3-106">But if you need to identify and protect a different type of sensitive information (for example, employee IDs or project numbers that uses a format specific to your organization) you can create a custom sensitive information type.</span></span>

<span data-ttu-id="4fee3-107">다음은 사용자 지정 중요한 정보 유형의 기본 구성 요소입니다.</span><span class="sxs-lookup"><span data-stu-id="4fee3-107">The fundamental parts of a custom sensitive information type are:</span></span>

- <span data-ttu-id="4fee3-108">**기본 패턴**: 직원 ID 번호, 프로젝트 번호 등으로, 일반적으로 정규식(RegEx)으로 식별되지만, 해당 패턴이 키워드 목록일 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4fee3-108">**Primary pattern**: employee ID numbers, project numbers, etc. This is typically identified by a regular expression (RegEx), but it can also be a list of keywords.</span></span>

- <span data-ttu-id="4fee3-p102">**추가 증거**: 9자리 직원 ID 번호를 찾고 있다고 가정해 보세요. 모든 9자리 숫자가 직원 ID 번호는 아니므로 "직원", "배지", "ID"또는 추가 정규식을 기반으로 하는 기타 텍스트 패턴과 같은 키워드를 추가로 찾아볼 수 있습니다. 이 뒷받침하는 증거(_뒷받침하는_ 또는 _확증적인_ 증거라고도 함)는 콘텐츠에 있는 9자리 숫자가 실제로 직원 ID 번호일 가능성을 높입니다.</span><span class="sxs-lookup"><span data-stu-id="4fee3-p102">**Additional evidence**: Suppose you're looking for a nine-digit employee ID number. Not all nine-digit numbers are employee ID numbers, so you can look for additional text: keywords like "employee", "badge", "ID", or other text patterns based on additional regular expressions. This supporting evidence (also known as _supporting_ or _corroborative_ evidence) increases the likelihood that nine-digit number found in content is really an employee ID number.</span></span>

- <span data-ttu-id="4fee3-p103">**문자 근접**: 기본 패턴과 뒷받침하는 증거가 서로 가까울수록 검색된 콘텐츠가 원하는 것일 확률이 높습니다. 다음 다이어그램과 같이 기본 패턴과 뒷받침하는 증거(_근접 범위_라고도 함) 사이의 문자 거리를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4fee3-p103">**Character proximity**: It makes sense that the closer the primary pattern and the supporting evidence are to each other, the more likely the detected content is going to be what you're looking for. You can specify the character distance between the primary pattern and the supporting evidence (also known as the _proximity window_) as shown in the following diagram:</span></span>

    ![증거 및 근접 범위 다이어그램](media/dc68e38e-dfa1-45b8-b204-89c8ba121f96.png)

- <span data-ttu-id="4fee3-p104">**신뢰 수준**: 가지고 있는 증거를 뒷받침할수록, 찾고 있는 중요한 정보가 일치하는 확률이 높아집니다. 더 많은 증거를 사용하여 검색된 일치 항목에 대해 높은 수준의 신뢰도를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4fee3-p104">**Confidence level**: The more supporting evidence you have, the higher the likelihood that a match contains the sensitive information you're looking for. You can assign higher levels of confidence for matches that are detected by using more evidence.</span></span>

  <span data-ttu-id="4fee3-p105">결과가 충족되면 패턴은 해당 개수 및 신뢰도를 반환합니다. 이 결과를 DLP 정책의 조건에서 사용할 수 있습니다. 중요한 정보 유형을 검색하는 조건을 DLP 정책에 추가하면 다음 다이어그램에 표시된 것처럼 개수 및 신뢰도를 편집할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4fee3-p105">When satisfied, a pattern returns a count and confidence level, which you can use in the conditions in your DLP policies. When you add a condition for detecting a sensitive information type to a DLP policy, you can edit the count and confidence level as shown in the following diagram:</span></span>

    ![인스턴스 개수 및 일치 정확도 옵션](media/11d0b51e-7c3f-4cc6-96d8-b29bcdae1aeb.png)

<span data-ttu-id="4fee3-120">보안 및 준수 센터에서 사용자 지정 중요한 정보 유형을 만들려면 다음 옵션이 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="4fee3-120">To create custom sensitive information types in the Office 365 Security & Compliance Center, you have the following options:</span></span>

- <span data-ttu-id="4fee3-p106">**UI 사용**: 이 방법은 쉽고 빠르지만 PowerShell보다 구성 옵션이 적습니다. 이 항목의 나머지 부분에서는 이러한 절차에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="4fee3-p106">**Use the UI**: This method is easier and faster, but you have less configuration options than PowerShell. The rest of this topic describes these procedures.</span></span>

- <span data-ttu-id="4fee3-p107">**PowerShell 사용**: 이 방법을 사용하려면 하나 이상의 중요한 정보 유형이 포함된 XML 파일(_규칙 패키지_라고 함)을 만든 다음 PowerShell을 사용하여 규칙 패키지를 가져와야 합니다. 규칙 패키지를 가져오는 것이 규칙 패키지를 만드는 것보다 간단합니다. 이 방법은 UI를 사용하는 것보다 훨씬 복잡하지만 더 많은 구성 옵션이 있습니다. 자세한 지침은 [보안 및 준수 센터 PowerShell에서 사용자 지정 중요한 정보 유형 만들기](create-a-custom-sensitive-information-type-in-scc-powershell.md)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="4fee3-p107">**Use PowerShell**: This method requires that you first create an XML file (called a _rule package_) that contains one or more sensitive information types, and then you use PowerShell to import the rule package (importing the rule package is trivial compared to creating the rule package. This method is much more complex than the UI, but you have more configuration options. For instructions, see [Create a custom sensitive information type in Office 365 Security & Compliance Center PowerShell](create-a-custom-sensitive-information-type-in-scc-powershell.md).</span></span>

<span data-ttu-id="4fee3-126">다음 테이블에 중요한 차이점이 설명되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4fee3-126">The key differences are described in the following table:</span></span>

|<span data-ttu-id="4fee3-127">**UI에서 사용자 지정 중요한 정보 유형**</span><span class="sxs-lookup"><span data-stu-id="4fee3-127">**Custom sensitive information types in the UI**</span></span>|<span data-ttu-id="4fee3-128">**PowerShell에서 사용자 지정 중요한 정보 유형**</span><span class="sxs-lookup"><span data-stu-id="4fee3-128">**Custom sensitive information types in PowerShell**</span></span>|
|:-----|:-----|
|<span data-ttu-id="4fee3-129">이름과 설명이 하나의 언어로 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4fee3-129">Name and Description are in one language.</span></span>|<span data-ttu-id="4fee3-130">이름 및 설명을 위한 여러 언어를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="4fee3-130">Supports multiple languages for Name and Description.</span></span>|
|<span data-ttu-id="4fee3-131">한 개의 패턴을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="4fee3-131">Supports one pattern.</span></span>|<span data-ttu-id="4fee3-132">여러 개의 패턴을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="4fee3-132">Supports multiple patterns.</span></span>|
|<span data-ttu-id="4fee3-133">뒷받침하는 증거는 다음이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4fee3-133">Supporting evidence can be:</span></span> <br/><span data-ttu-id="4fee3-134">• 정규식</span><span class="sxs-lookup"><span data-stu-id="4fee3-134">• Regular expressions</span></span> <br/><span data-ttu-id="4fee3-135">• 키워드</span><span class="sxs-lookup"><span data-stu-id="4fee3-135">• Keywords</span></span> <br/><span data-ttu-id="4fee3-136">• 키워드 사전</span><span class="sxs-lookup"><span data-stu-id="4fee3-136">• Keyword dictionaries</span></span>|<span data-ttu-id="4fee3-137">뒷받침하는 증거는 다음이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4fee3-137">Supporting evidence can be:</span></span> <br/><span data-ttu-id="4fee3-138">• 정규식</span><span class="sxs-lookup"><span data-stu-id="4fee3-138">• Regular expressions</span></span> <br/><span data-ttu-id="4fee3-139">• 키워드</span><span class="sxs-lookup"><span data-stu-id="4fee3-139">• Keywords</span></span> <br/><span data-ttu-id="4fee3-140">• 키워드 사전</span><span class="sxs-lookup"><span data-stu-id="4fee3-140">• Keyword dictionaries</span></span> <br/><span data-ttu-id="4fee3-141">• [기본 제공 DLP 함수](what-the-dlp-functions-look-for.md)</span><span class="sxs-lookup"><span data-stu-id="4fee3-141">• [Built-in DLP functions](what-the-dlp-functions-look-for.md)</span></span>|
|<span data-ttu-id="4fee3-142">사용자 지정 중요한 정보 유형이 이름이 Microsoft.SCCManaged.CustomRulePack인 규칙 패키지에 추가됩니다.</span><span class="sxs-lookup"><span data-stu-id="4fee3-142">Custom sensitive information types are added to the rule package named Microsoft.SCCManaged.CustomRulePack</span></span>|<span data-ttu-id="4fee3-143">사용자 지정 중요한 정보 유형을 포함하는 최대 10개의 규칙 패키지를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4fee3-143">You can create up to 10 rule packages that contain custom sensitive information types.</span></span>|
|<span data-ttu-id="4fee3-144">패턴 일치는 기본 패턴 및 모든 뒷받침하는 증거를 검색해야 합니다(암시적 AND 연산자가 사용됨).</span><span class="sxs-lookup"><span data-stu-id="4fee3-144">Pattern match requires the detection of the primary pattern and all supporting evidence (the implicit AND operator is used).</span></span>|<span data-ttu-id="4fee3-145">패턴 일치는 기본 패턴 및 구성 가능한 뒷받침하는 증거의 양을 검색해야 합니다(암시적 AND 및 OR 연산자를 사용할 수 있음).</span><span class="sxs-lookup"><span data-stu-id="4fee3-145">Pattern match requires the detection of the primary pattern and a configurable amount of supporting evidence (implicit AND and OR operators can be used).</span></span>|

## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="4fee3-146">시작하기 전에 알아야 할 내용</span><span class="sxs-lookup"><span data-stu-id="4fee3-146">What do you need to know before you begin?</span></span>

- <span data-ttu-id="4fee3-147">보안 및 준수 센터를 열려면 [보안 및 준수 센터로 이동](go-to-the-securitycompliance-center.md)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="4fee3-147">To open the Security & Compliance Center, see [Go to the Office 365 Security & Compliance Center](go-to-the-securitycompliance-center.md).</span></span>

- <span data-ttu-id="4fee3-p108">사용자 지정 중요한 정보 유형을 위해서는 정규식(RegEx)을 잘 알고 있어야 합니다. 텍스트 처리에 사용되는 Boost.RegEx(이전에는 RegEx++라고 함) 엔진에 대한 자세한 내용은 [Boost.Regex 5.1.3](https://www.boost.org/doc/libs/1_68_0/libs/regex/doc/html/)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="4fee3-p108">Custom sensitive information types require familiarity with regular expressions (RegEx). For more information about the Boost.RegEx (formerly known as RegEx++) engine that's used for processing the text, see [Boost.Regex 5.1.3](https://www.boost.org/doc/libs/1_68_0/libs/regex/doc/html/).</span></span>

  <span data-ttu-id="4fee3-p109">Microsoft 고객 서비스 및 지원에서는 사용자 지정 콘텐츠 일치 정의(사용자 지정 분류 또는 정규식 패턴 만들기)를 제공하는 것을 지원할 수 없습니다. 지원 엔지니어는 기능을 제한적으로 지원할 수 있습니다(예: 테스트 목적으로 샘플 정규식 패턴 제공 또는 예상대로 트리거되지 않는 기존 정규식 패턴 문제 해결 지원). 그러나 사용자 지정 콘텐츠 일치 개발이 귀하의 요구 사항이나 의무를 충족할 것이라고 확신할 수는 없습니다.</span><span class="sxs-lookup"><span data-stu-id="4fee3-p109">Microsoft Customer Service & Support can't assist with providing custom content-matching definitions (creating custom classifications or regular expression patterns). Support engineers can provide limited support for the feature (for example, providing sample regular expression patterns for testing purposes, or assisting with troubleshooting an existing regular expression pattern that's not triggering as expected), but can't provide assurances that any custom content-matching development will fulfill your requirements or obligations.</span></span>

- <span data-ttu-id="4fee3-p110">DLP는 검색 크롤러를 사용하여 SharePoint Online 및 비즈니스용 OneDrive 사이트의 중요한 정보를 식별하고 분류합니다. 기존 콘텐츠에서 새로운 사용자 지정 중요한 정보 유형을 식별하려면 콘텐츠를 다시 크롤링해야 합니다. 일정을 기반으로 콘텐츠가 다시 크롤링되지만 사이트 모음, 목록 또는 라이브러리의 콘텐츠를 수동으로 다시 크롤링할 수 있습니다. 자세한 내용은 [사이트, 라이브러리 또는 목록의 크롤링 및 다시 인덱싱을 수동으로 요청](https://docs.microsoft.com/sharepoint/crawl-site-content)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="4fee3-p110">DLP uses the search crawler to identify and classify sensitive information in SharePoint Online and OneDrive for Business sites. To identify your new custom sensitive information type in existing content, the content must be recrawled. Content is recrawled based on a schedule, but you can manually recrawl content for a site collection, list, or library. For more information, see [Manually request crawling and re-indexing of a site, a library or a list](https://docs.microsoft.com/sharepoint/crawl-site-content).</span></span>

## <a name="create-custom-sensitive-information-types-in-the-security--compliance-center"></a><span data-ttu-id="4fee3-156">보안 및 준수 센터에서 사용자 지정 중요한 정보 유형 만들기</span><span class="sxs-lookup"><span data-stu-id="4fee3-156">Create custom sensitive information types in the Security & Compliance Center</span></span>

<span data-ttu-id="4fee3-157">보안 및 준수 센터에서 **분류** \> **중요한 정보 유형**으로 이동한 후 **만들기**를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="4fee3-157">In the Security & Compliance Center, go to **Classifications** \> **Sensitive info types** and click **Create**.</span></span>

<span data-ttu-id="4fee3-158">설정은 매우 명확하며 마법사의 연결 페이지에서 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="4fee3-158">The settings are fairly self-evident, and are explained on the associate page of the wizard:</span></span>

- <span data-ttu-id="4fee3-159">**이름**</span><span class="sxs-lookup"><span data-stu-id="4fee3-159">**Name**</span></span>

- <span data-ttu-id="4fee3-160">**설명**</span><span class="sxs-lookup"><span data-stu-id="4fee3-160">**Description**</span></span>

- <span data-ttu-id="4fee3-161">**근접**</span><span class="sxs-lookup"><span data-stu-id="4fee3-161">**Proximity**</span></span>

- <span data-ttu-id="4fee3-162">**신뢰 수준**</span><span class="sxs-lookup"><span data-stu-id="4fee3-162">**Confidence level**</span></span>

- <span data-ttu-id="4fee3-163">**기본 패턴 요소**(키워드, 정규식 또는 사전)</span><span class="sxs-lookup"><span data-stu-id="4fee3-163">**Primary pattern element** (keywords, regular expression, or dictionary)</span></span>

- <span data-ttu-id="4fee3-164">선택 사항인 **지원 패턴 요소**(키워드, 정규식 또는 사전) 및 해당하는 **최소 비용** 값</span><span class="sxs-lookup"><span data-stu-id="4fee3-164">Optional **Supporting pattern elements** (keywords, regular expression, or dictionary) and a corresponding **Minimum cost** value.</span></span>

<span data-ttu-id="4fee3-p111">시나리오는 다음과 같습니다. "직원", "ID" 및 "배지"라는 키워드와 함께 콘텐츠의 9자리 직원 번호를 검색하는 사용자 지정 중요한 정보 유형이 필요합니다. 이 사용자 지정 중요한 정보 유형을 만들려면 다음 단계를 수행하세요.</span><span class="sxs-lookup"><span data-stu-id="4fee3-p111">Here's a scenario: You want a custom sensitive information type that detects 9-digit employee numbers in content, along with the keywords "employee" "ID" and "badge". To create this custom sensitive information type, do the following steps:</span></span>

1. <span data-ttu-id="4fee3-167">보안 및 준수 센터에서 **분류** \> **중요한 정보 유형**으로 이동한 후 **만들기**를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="4fee3-167">In the Security & Compliance Center, go to **Classifications** \> **Sensitive info types** and click **Create**.</span></span>

    ![중요한 정보 유형 및 만들기 단추 위치](media/scc-cust-sens-info-type-new.png)

2. <span data-ttu-id="4fee3-169">**이름 및 설명 선택** 페이지가 열리면 다음 값을 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="4fee3-169">In the **Choose a name and description** page that opens, enter the following values:</span></span>

  - <span data-ttu-id="4fee3-170">**이름**: 직원 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="4fee3-170">**Name**: Employee ID.</span></span>

  - <span data-ttu-id="4fee3-171">**설명**: 9자리 Contoso 직원 ID 번호를 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="4fee3-171">**Description**: Detect nine-digit Contoso employee ID numbers.</span></span>

    ![이름 및 설명 페이지](media/scc-cust-sens-info-type-new-name-desc.png)

    <span data-ttu-id="4fee3-173">작업을 마친 후 **다음**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="4fee3-173">When you're finished, click **Next**.</span></span>

3. <span data-ttu-id="4fee3-174">**일치 요구 사항** 페이지가 열리면 **요소 추가**를 클릭하고 다음 설정을 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="4fee3-174">In the **Requirements for matching** page that opens, click **Add an element** configure the following settings:</span></span>

    - <span data-ttu-id="4fee3-175">**다음이 포함된 콘텐츠 검색**:</span><span class="sxs-lookup"><span data-stu-id="4fee3-175">**Detect content containing**:</span></span>
 
      <span data-ttu-id="4fee3-p112">a. **이 중 하나라도 포함**을 클릭하고 **정규식**을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="4fee3-p112">a. Click **Any of these** and select **Regular expression**.</span></span>

      <span data-ttu-id="4fee3-p113">b. 정규식 상자에서 `(\s)(\d{9})(\s)`(앞뒤에 공백이 있는 9자리 숫자) 스트링을 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="4fee3-p113">b. In the regular expression box, enter `(\s)(\d{9})(\s)` (nine-digit numbers surrounded by white space).</span></span>
  
    - <span data-ttu-id="4fee3-180">**지원 요소**: **지원 요소 추가**를 클릭하고 **이 키워드 목록 포함**을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="4fee3-180">**Supporting elements**: Click **Add supporting elements** and select **Contains this keyword list**.</span></span>

    - <span data-ttu-id="4fee3-181">**이 키워드 목록 포함** 영역이 표시되면 다음 설정을 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="4fee3-181">In the **Contains this keyword list** area that appears, configure the following settings:</span></span>

      - <span data-ttu-id="4fee3-182">**키워드 목록**: 직원, ID, 배지 값을 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="4fee3-182">**Keyword list**: Enter the following value: employee,ID,badge.</span></span>

      - <span data-ttu-id="4fee3-183">**최소 개수**: 기본값 1을 그대로 둡니다.</span><span class="sxs-lookup"><span data-stu-id="4fee3-183">**Minimum count**: Leave the default value 1.</span></span>

    - <span data-ttu-id="4fee3-184">기본값인 **신뢰 수준** 값 60을 그대로 둡니다.</span><span class="sxs-lookup"><span data-stu-id="4fee3-184">Leave the default **Confidence level** value 60.</span></span> 

    - <span data-ttu-id="4fee3-185">기본값인 **문자 근접** 값 300을 그대로 둡니다.</span><span class="sxs-lookup"><span data-stu-id="4fee3-185">Leave the default **Character proximity** value 300.</span></span>

    ![페이지 일치에 대한 요구 사항](media/scc-cust-sens-info-type-new-reqs.png)

    <span data-ttu-id="4fee3-187">작업을 마친 후 **다음**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="4fee3-187">When you're finished, click **Next**.</span></span>

4. <span data-ttu-id="4fee3-188">**검토 및 완료** 페이지가 열리면 설정을 검토하고 **마침**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="4fee3-188">On the **Review and finalize** page that opens, review the settings and click **Finish**.</span></span>

    ![검토 및 완료 페이지](media/scc-cust-sens-info-type-new-review.png)

5. <span data-ttu-id="4fee3-p114">다음 페이지에서는 **예**를 클릭하여 새로운 사용자 지정 중요한 정보 유형을 테스트할 것을 권장합니다. 자세한 내용은 [보안 및 준수 센터에서 사용자 지정 중요한 정보 유형 테스트](#test-custom-sensitive-information-types-in-the-security--compliance-center)를 참조하세요. 나중에 규칙을 테스트하려면 **아니요**를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="4fee3-p114">The next page encourages you to test the new custom sensitive information type by clicking **Yes**. For more information, see [Test custom sensitive information types in the Security & Compliance Center](#test-custom-sensitive-information-types-in-the-security--compliance-center). To test the rule later, click **No**.</span></span>

    ![테스트 권장 사항 페이지](media/scc-cust-sens-info-type-new-test.png)

### <a name="how-do-you-know-this-worked"></a><span data-ttu-id="4fee3-194">작동 여부는 어떻게 확인하나요?</span><span class="sxs-lookup"><span data-stu-id="4fee3-194">How do you know this worked?</span></span>

<span data-ttu-id="4fee3-195">새로운 중요한 정보 유형을 성공적으로 만들었는지 확인하려면 다음 단계를 수행합니다.</span><span class="sxs-lookup"><span data-stu-id="4fee3-195">To verify that you've successfully created a new sensitive information type, do any of the following steps:</span></span>

  - <span data-ttu-id="4fee3-196">**분류** \> **중요한 정보 유형**으로 이동하고 새로운 사용자 지정 중요한 정보 유형이 나열되어 있는지 확인하세요.</span><span class="sxs-lookup"><span data-stu-id="4fee3-196">Go to **Classifications** \> **Sensitive info types** and verify the new custom sensitive information type is listed.</span></span>

  - <span data-ttu-id="4fee3-p115">새로운 사용자 지정 중요한 정보 유형을 테스트합니다. 자세한 내용은, [보안 및 준수 센터에서 사용자 지정 중요한 정보 유형 테스트](#test-custom-sensitive-information-types-in-the-security--compliance-center)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="4fee3-p115">Test the new custom sensitive information type. For more information, see [Test custom sensitive information types in the Security & Compliance Center](#test-custom-sensitive-information-types-in-the-security--compliance-center).</span></span>

## <a name="modify-custom-sensitive-information-types-in-the-security--compliance-center"></a><span data-ttu-id="4fee3-199">보안 및 준수 센터에서 사용자 지정 중요한 정보 유형 수정</span><span class="sxs-lookup"><span data-stu-id="4fee3-199">Modify custom sensitive information types in the Security & Compliance Center</span></span>

<span data-ttu-id="4fee3-200">**참고:**</span><span class="sxs-lookup"><span data-stu-id="4fee3-200">**Notes**:</span></span>

- <span data-ttu-id="4fee3-p116">사용자 지정 중요한 정보 유형만 수정할 수 있습니다. 기본 제공 중요한 정보 유형은 수정할 수 없습니다. 그러나 PowerShell을 사용하여 기본 제공 사용자 지정 중요한 정보 유형을 내보낸 후 사용자 지정하고 사용자 지정 중요한 정보 유형으로 가져올 수 있습니다. 자세한 내용은 [기본 중요한 정보 유형 사용자 지정](customize-a-built-in-sensitive-information-type.md)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="4fee3-p116">You can only modify custom sensitive information types; you can't modify built-in sensitive information types. But you can use PowerShell to export built-in custom sensitive information types, customize them, and import them as custom sensitive information types. For more information, see [Customize a built-in sensitive information type](customize-a-built-in-sensitive-information-type.md).</span></span>

- <span data-ttu-id="4fee3-p117">UI에서 만든 사용자 지정 중요한 정보 유형만 수정할 수 있습니다. [PowerShell 프로시저](create-a-custom-sensitive-information-type-in-scc-powershell.md)를 사용하여 사용자 지정 중요한 정보 유형 규칙 패키지를 가져오면 오류가 발생합니다.</span><span class="sxs-lookup"><span data-stu-id="4fee3-p117">You can only modify custom sensitive information types that you created in the UI. If you used the [PowerShell procedure](create-a-custom-sensitive-information-type-in-scc-powershell.md) to import a custom sensitive information type rule package, you'll get an error.</span></span>

<span data-ttu-id="4fee3-206">보안 및 준수 센터에서 **분류** \> **중요한 정보 유형**으로 이동하고, 수정할 사용자 지정 중요한 정보 유형을 선택한 후 **편집**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="4fee3-206">In the Security & Compliance Center, go to **Classifications** \> **Sensitive info types**, select the custom sensitive information type that you want to modify, and then click **Edit**.</span></span>

  ![중요한 정보 유형 및 편집 단추 위치](media/scc-cust-sens-info-type-edit.png)

<span data-ttu-id="4fee3-p118">보안 및 준수 센터에서 사용자 지정 중요한 정보 유형을 만들 때와 동일한 옵션을 사용할 수 있습니다. 자세한 내용은 [보안 및 준수 센터에서 사용자 지정 중요한 정보 유형 만들기](#create-custom-sensitive-information-types-in-the-security--compliance-center)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="4fee3-p118">The same options are available here as when you created the custom sensitive information type in the Security & Compliance Center. For more information, see [Create custom sensitive information types in the Security & Compliance Center](#create-custom-sensitive-information-types-in-the-security--compliance-center).</span></span>

### <a name="how-do-you-know-this-worked"></a><span data-ttu-id="4fee3-210">작동 여부는 어떻게 확인하나요?</span><span class="sxs-lookup"><span data-stu-id="4fee3-210">How do you know this worked?</span></span>

<span data-ttu-id="4fee3-211">수정한 중요한 정보 유형을 성공적으로 만들었는지 확인하려면 다음 단계를 수행합니다.</span><span class="sxs-lookup"><span data-stu-id="4fee3-211">To verify that you've successfully modified a sensitive information type, do any of the following steps:</span></span>

  - <span data-ttu-id="4fee3-212">**분류** \> **중요한 정보 유형**으로 이동하고 수정한 사용자 지정 중요한 정보 유형의 속성을 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="4fee3-212">Go to **Classifications** \> **Sensitive info types** to verify the properties of the modified custom sensitive information type.</span></span> 

  - <span data-ttu-id="4fee3-p119">수정한 사용자 지정 중요한 정보 유형을 테스트합니다. 자세한 내용은, [보안 및 준수 센터에서 사용자 지정 중요한 정보 유형 테스트](#test-custom-sensitive-information-types-in-the-security--compliance-center)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="4fee3-p119">Test the modified custom sensitive information type. For more information, see [Test custom sensitive information types in the Security & Compliance Center](#test-custom-sensitive-information-types-in-the-security--compliance-center).</span></span>

## <a name="remove-custom-sensitive-information-types-in-the-security--compliance-center"></a><span data-ttu-id="4fee3-215">보안 및 준수 센터에서 사용자 지정 중요한 정보 유형 제거</span><span class="sxs-lookup"><span data-stu-id="4fee3-215">Remove custom sensitive information types in the Security & Compliance Center</span></span> 

<span data-ttu-id="4fee3-216">**참고**:</span><span class="sxs-lookup"><span data-stu-id="4fee3-216">**Notes**:</span></span>

- <span data-ttu-id="4fee3-217">사용자 지정 중요한 정보 유형만 제거할 수 있습니다. 기본 제공 중요한 정보 유형은 제거할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="4fee3-217">You can only remove custom sensitive information types; you can't remove built-in sensitive information types.</span></span>

- <span data-ttu-id="4fee3-218">사용자 지정 중요한 정보 유형을 제거하기 전에 DLP 정책이나 Exchange 메일 흐름 규칙(전송 규칙이라고도 함)이 중요한 정보 유형을 계속 참조하지 않는 것을 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="4fee3-218">Before your remove a custom sensitive information type, verify that no DLP policies or Exchange mail flow rules (also known as transport rules) still reference the sensitive information type.</span></span>

1. <span data-ttu-id="4fee3-219">보안 및 준수 센터에서 **분류** \> **중요한 정보 유형**으로 이동하고, 제거할 사용자 지정 중요한 정보 유형을 한 개 이상 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="4fee3-219">In the Security & Compliance Center, go to **Classifications** \> **Sensitive info types** and select one or more custom sensitive information types that you want to remove.</span></span>

2. <span data-ttu-id="4fee3-220">플라이아웃이 열리면 **삭제**(두 개 이상을 선택한 경우 **중요한 정보 유형 삭제**)를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="4fee3-220">In the fly-out that opens, click **Delete** (or **Delete sensitive info types** if you selected more than one).</span></span>

    ![중요한 정보 유형 및 삭제 단추 위치](media/scc-cust-sens-info-type-delete.png)

3. <span data-ttu-id="4fee3-222">나타나는 경고 메시지에서 **예**를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="4fee3-222">In the warning message that appears, click **Yes**.</span></span>

### <a name="how-do-you-know-this-worked"></a><span data-ttu-id="4fee3-223">작동 여부는 어떻게 확인하나요?</span><span class="sxs-lookup"><span data-stu-id="4fee3-223">How do you know this worked?</span></span>

<span data-ttu-id="4fee3-224">사용자 지정 중요한 정보 유형을 성공적으로 삭제했는지 확인하려면 **분류** \> **중요한 정보 유형**으로 이동하여 사용자 지정 중요한 정보 유형이 더 이상 나열되지 않는지 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="4fee3-224">To verify that you've successfully removed a custom sensitive information type, go to **Classifications** \> **Sensitive info types** to verify the custom sensitive information type is no longer listed.</span></span>

## <a name="test-custom-sensitive-information-types-in-the-security--compliance-center"></a><span data-ttu-id="4fee3-225">보안 및 준수 센터에서 사용자 지정 중요한 정보 유형 테스트</span><span class="sxs-lookup"><span data-stu-id="4fee3-225">Test custom sensitive information types in the Security & Compliance Center</span></span>

1. <span data-ttu-id="4fee3-226">보안 및 준수 센터에서 **분류** \> **중요한 정보 유형**으로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="4fee3-226">In the Security & Compliance Center, go to **Classifications** \> **Sensitive info types**.</span></span>

2. <span data-ttu-id="4fee3-p120">테스트할 하나 이상의 사용자 지정 중요한 정보 유형을 선택합니다. 플라이아웃이 열리면 **유형 테스트**(두 개 이상을 선택한 경우 **중요한 정보 유형 테스트**)를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="4fee3-p120">Select one or more custom sensitive information types to test. In the fly-out that opens, click **Test type** (or **Test sensitive info types** if you selected more than one).</span></span>

    ![중요한 정보 유형 및 유형 테스트 단추 위치](media/scc-cust-sens-info-type-test.png)

3. <span data-ttu-id="4fee3-230">**테스트할 파일 업로드** 페이지가 열리면 파일을 끌어서 놓거나 **찾아보기**를 클릭하고 파일을 선택하여 테스트할 문서를 업로드합니다.</span><span class="sxs-lookup"><span data-stu-id="4fee3-230">On the **Upload file to test** page that opens, upload a document to test by dragging and dropping a file or by clicking **Browse** and selecting a file.</span></span>

    ![테스트할 파일 업로드 페이지](media/scc-cust-sens-info-type-test-upload.png)

4. <span data-ttu-id="4fee3-232">**테스트** 단추를 클릭하여 파일에서 패턴 일치에 대해 문서를 테스트합니다.</span><span class="sxs-lookup"><span data-stu-id="4fee3-232">Click the **Test** button to test the document for pattern matches in the file.</span></span>

5. <span data-ttu-id="4fee3-233">**결과 일치** 페이지에서 **마침**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="4fee3-233">On the **Match results** page, click **Finish**.</span></span>

    ![결과 일치](media/scc-cust-sens-info-type-test-results.png)