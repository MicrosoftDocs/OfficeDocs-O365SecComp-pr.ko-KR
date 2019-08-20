---
title: 보안 및 준수 센터에서 사용자 지정 중요한 정보 유형 만들기
ms.author: chrfox
author: chrfox
manager: laurawi
audience: Admin
ms.topic: article
ms.service: O365-seccomp
ms.date: 04/17/2019
localization_priority: Priority
ms.collection:
- M365-security-compliance
search.appverid:
- MOE150
- MET150
description: 보안 및 준수 센터의 그래픽 사용자 인터페이스에서 DLP에 대한 사용자 지정 중요한 정보 유형을 만들고, 수정, 제거 및 테스트하는 방법을 알아봅니다.
ms.openlocfilehash: e7b2d07c64d97eafee5b269bbc0e395855c2ab44
ms.sourcegitcommit: 0a0d9c1325b4b0581018c31037dcc707d3d679b4
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/09/2019
ms.locfileid: "36279160"
---
# <a name="create-a-custom-sensitive-information-type-in-the-security--compliance-center"></a><span data-ttu-id="c04fa-103">보안 및 준수 센터에서 사용자 지정 중요한 정보 유형 만들기</span><span class="sxs-lookup"><span data-stu-id="c04fa-103">Create a custom sensitive information type in the Security & Compliance Center</span></span>

## <a name="summary"></a><span data-ttu-id="c04fa-104">요약</span><span class="sxs-lookup"><span data-stu-id="c04fa-104">Summary</span></span>

<span data-ttu-id="c04fa-105">이 문서를 읽고 보안 및 준수 센터([https://protection.office.com](https://protection.office.com))에서 [사용자 지정 중요한 정보 유형](custom-sensitive-info-types.md)을 만들어 보세요.</span><span class="sxs-lookup"><span data-stu-id="c04fa-105">Read this article to create a [custom sensitive information type](custom-sensitive-info-types.md) in the Security & Compliance Center ([https://protection.office.com](https://protection.office.com)).</span></span> <span data-ttu-id="c04fa-106">이 방법으로 만드는 사용자 지정 중요한 정보 유형은 이름이 `Microsoft.SCCManaged.CustomRulePack`인 규칙 패키지에 추가됩니다.</span><span class="sxs-lookup"><span data-stu-id="c04fa-106">The custom sensitive information types that you create by using this method are added to the rule package named `Microsoft.SCCManaged.CustomRulePack`.</span></span>

<span data-ttu-id="c04fa-107">PowerShell 및 정확한 데이터 매치 기능을 사용하여 사용자 지정 중요한 정보 유형을 만들 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c04fa-107">You can also create custom sensitive information types by using PowerShell and Exact Data Match capabilities.</span></span> <span data-ttu-id="c04fa-108">해당 방법에 대한 자세한 내용은 다음을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="c04fa-108">To learn more about those methods, see:</span></span>
- <span data-ttu-id="c04fa-109">[보안 및 준수 센터 PowerShell에서 사용자 지정 중요한 정보 유형 만들기](create-a-custom-sensitive-information-type-in-scc-powershell.md)</span><span class="sxs-lookup"><span data-stu-id="c04fa-109">See [Create a custom sensitive information type in Security & Compliance Center PowerShell](create-a-custom-sensitive-information-type-in-scc-powershell.md).</span></span>
- [<span data-ttu-id="c04fa-110">정확한 데이터 매치(EDM)를 사용하여 DLP를 위한 사용자 지정 중요한 정보 유형 만들기</span><span class="sxs-lookup"><span data-stu-id="c04fa-110">Create a custom sensitive information type with Exact Data Match (Preview)</span></span>](create-custom-sensitive-information-types-with-exact-data-match-based-classification.md)

## <a name="before-you-begin"></a><span data-ttu-id="c04fa-111">시작하기 전에...</span><span class="sxs-lookup"><span data-stu-id="c04fa-111">Before you begin</span></span>

- <span data-ttu-id="c04fa-112">조직에 DLP(데이터 손실 방지)를 포함하는 구독(예: Office 365 Enterprise)이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c04fa-112">Your organization must have a subscription, such as Office 365 Enterprise, that includes Data Loss Prevention (DLP).</span></span> <span data-ttu-id="c04fa-113">[메시징 정책 및 규정 준수 서비스 설명](https://docs.microsoft.com/office365/servicedescriptions/exchange-online-protection-service-description/messaging-policy-and-compliance-servicedesc)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="c04fa-113">See [Messaging Policy and Compliance ServiceDescription](https://docs.microsoft.com/office365/servicedescriptions/exchange-online-protection-service-description/messaging-policy-and-compliance-servicedesc).</span></span> 

- <span data-ttu-id="c04fa-p104">사용자 지정 중요한 정보 유형을 위해서는 정규식(RegEx)을 잘 알고 있어야 합니다. 텍스트 처리에 사용되는 Boost.RegEx(이전에는 RegEx++라고 함) 엔진에 대한 자세한 내용은 [Boost.Regex 5.1.3](https://www.boost.org/doc/libs/1_68_0/libs/regex/doc/html/)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="c04fa-p104">Custom sensitive information types require familiarity with regular expressions (RegEx). For more information about the Boost.RegEx (formerly known as RegEx++) engine that's used for processing the text, see [Boost.Regex 5.1.3](https://www.boost.org/doc/libs/1_68_0/libs/regex/doc/html/).</span></span>

  <span data-ttu-id="c04fa-p105">Microsoft 고객 서비스 및 지원에서는 사용자 지정 콘텐츠 일치 정의(사용자 지정 분류 또는 정규식 패턴 만들기)를 제공하는 것을 지원할 수 없습니다. 지원 엔지니어는 기능을 제한적으로 지원할 수 있습니다(예: 테스트 목적으로 샘플 정규식 패턴 제공 또는 예상대로 트리거되지 않는 기존 정규식 패턴 문제 해결 지원). 그러나 사용자 지정 콘텐츠 일치 개발이 귀하의 요구 사항이나 의무를 충족할 것이라고 확신할 수는 없습니다.</span><span class="sxs-lookup"><span data-stu-id="c04fa-p105">Microsoft Customer Service & Support can't assist with providing custom content-matching definitions (creating custom classifications or regular expression patterns). Support engineers can provide limited support for the feature (for example, providing sample regular expression patterns for testing purposes, or assisting with troubleshooting an existing regular expression pattern that's not triggering as expected), but can't provide assurances that any custom content-matching development will fulfill your requirements or obligations.</span></span>

- <span data-ttu-id="c04fa-p106">DLP는 검색 크롤러를 사용하여 SharePoint Online 및 비즈니스용 OneDrive 사이트의 중요한 정보를 식별하고 분류합니다. 기존 콘텐츠에서 새로운 사용자 지정 중요한 정보 유형을 식별하려면 콘텐츠를 다시 크롤링해야 합니다. 일정을 기반으로 콘텐츠가 다시 크롤링되지만 사이트 모음, 목록 또는 라이브러리의 콘텐츠를 수동으로 다시 크롤링할 수 있습니다. 자세한 내용은 [사이트, 라이브러리 또는 목록의 크롤링 및 다시 인덱싱을 수동으로 요청](https://docs.microsoft.com/sharepoint/crawl-site-content)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="c04fa-p106">DLP uses the search crawler to identify and classify sensitive information in SharePoint Online and OneDrive for Business sites. To identify your new custom sensitive information type in existing content, the content must be recrawled. Content is recrawled based on a schedule, but you can manually recrawl content for a site collection, list, or library. For more information, see [Manually request crawling and re-indexing of a site, a library or a list](https://docs.microsoft.com/sharepoint/crawl-site-content).</span></span>

## <a name="create-custom-sensitive-information-types-in-the-security--compliance-center"></a><span data-ttu-id="c04fa-122">보안 및 준수 센터에서 사용자 지정 중요한 정보 유형 만들기</span><span class="sxs-lookup"><span data-stu-id="c04fa-122">Create custom sensitive information types in the Security & Compliance Center</span></span>

<span data-ttu-id="c04fa-123">보안 및 준수 센터에서 **분류** \> **중요한 정보 유형**으로 이동한 후 **만들기**를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="c04fa-123">In the Security & Compliance Center, go to **Classifications** \> **Sensitive info types** and click **Create**.</span></span>

<span data-ttu-id="c04fa-124">설정은 매우 명확하며 마법사의 연결 페이지에서 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="c04fa-124">The settings are fairly self-evident, and are explained on the associate page of the wizard:</span></span>

- <span data-ttu-id="c04fa-125">**이름**</span><span class="sxs-lookup"><span data-stu-id="c04fa-125">**Name**</span></span>

- <span data-ttu-id="c04fa-126">**설명**</span><span class="sxs-lookup"><span data-stu-id="c04fa-126">**Description**</span></span>

- <span data-ttu-id="c04fa-127">**근접**</span><span class="sxs-lookup"><span data-stu-id="c04fa-127">**Proximity**</span></span>

- <span data-ttu-id="c04fa-128">**신뢰 수준**</span><span class="sxs-lookup"><span data-stu-id="c04fa-128">**Confidence level**</span></span>

- <span data-ttu-id="c04fa-129">**기본 패턴 요소**(키워드, 정규식 또는 사전)</span><span class="sxs-lookup"><span data-stu-id="c04fa-129">**Primary pattern element** (keywords, regular expression, or dictionary)</span></span>

- <span data-ttu-id="c04fa-130">선택 사항인 **지원 패턴 요소**(키워드, 정규식 또는 사전) 및 해당하는 **최소 비용** 값</span><span class="sxs-lookup"><span data-stu-id="c04fa-130">Optional **Supporting pattern elements** (keywords, regular expression, or dictionary) and a corresponding **Minimum cost** value.</span></span>

<span data-ttu-id="c04fa-p107">시나리오는 다음과 같습니다. "직원", "ID" 및 "배지"라는 키워드와 함께 콘텐츠의 9자리 직원 번호를 검색하는 사용자 지정 중요한 정보 유형이 필요합니다. 이 사용자 지정 중요한 정보 유형을 만들려면 다음 단계를 수행하세요.</span><span class="sxs-lookup"><span data-stu-id="c04fa-p107">Here's a scenario: You want a custom sensitive information type that detects 9-digit employee numbers in content, along with the keywords "employee" "ID" and "badge". To create this custom sensitive information type, do the following steps:</span></span>

1. <span data-ttu-id="c04fa-133">보안 및 준수 센터에서 **분류** \> **중요한 정보 유형**으로 이동한 후 **만들기**를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="c04fa-133">In the Security & Compliance Center, go to **Classifications** \> **Sensitive info types** and click **Create**.</span></span>

    ![중요한 정보 유형 및 만들기 단추 위치](media/scc-cust-sens-info-type-new.png)

2. <span data-ttu-id="c04fa-135">**이름 및 설명 선택** 페이지가 열리면 다음 값을 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="c04fa-135">In the **Choose a name and description** page that opens, enter the following values:</span></span>

  - <span data-ttu-id="c04fa-136">**이름**: 직원 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="c04fa-136">**Name**: Employee ID.</span></span>

  - <span data-ttu-id="c04fa-137">**설명**: 9자리 Contoso 직원 ID 번호를 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="c04fa-137">**Description**: Detect nine-digit Contoso employee ID numbers.</span></span>

    ![이름 및 설명 페이지](media/scc-cust-sens-info-type-new-name-desc.png)

    <span data-ttu-id="c04fa-139">작업을 마친 후 **다음**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="c04fa-139">When you're finished, click **Next**.</span></span>

3. <span data-ttu-id="c04fa-140">**일치 요구 사항** 페이지가 열리면 **요소 추가**를 클릭하고 다음 설정을 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="c04fa-140">In the **Requirements for matching** page that opens, click **Add an element** configure the following settings:</span></span>

    - <span data-ttu-id="c04fa-141">**다음이 포함된 콘텐츠 검색**:</span><span class="sxs-lookup"><span data-stu-id="c04fa-141">**Detect content containing**:</span></span>
 
      <span data-ttu-id="c04fa-p108">a. **이 중 하나라도 포함**을 클릭하고 **정규식**을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="c04fa-p108">a. Click **Any of these** and select **Regular expression**.</span></span>

      <span data-ttu-id="c04fa-p109">b. 정규식 상자에서 `(\s)(\d{9})(\s)`(앞뒤에 공백이 있는 9자리 숫자) 스트링을 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="c04fa-p109">b. In the regular expression box, enter `(\s)(\d{9})(\s)` (nine-digit numbers surrounded by white space).</span></span>
  
    - <span data-ttu-id="c04fa-146">**지원 요소**: **지원 요소 추가**를 클릭하고 **이 키워드 목록 포함**을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="c04fa-146">**Supporting elements**: Click **Add supporting elements** and select **Contains this keyword list**.</span></span>

    - <span data-ttu-id="c04fa-147">**이 키워드 목록 포함** 영역이 표시되면 다음 설정을 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="c04fa-147">In the **Contains this keyword list** area that appears, configure the following settings:</span></span>

      - <span data-ttu-id="c04fa-148">**키워드 목록**: 직원, ID, 배지 값을 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="c04fa-148">**Keyword list**: Enter the following value: employee,ID,badge.</span></span>

      - <span data-ttu-id="c04fa-149">**최소 개수**: 기본값 1을 그대로 둡니다.</span><span class="sxs-lookup"><span data-stu-id="c04fa-149">**Minimum count**: Leave the default value 1.</span></span>

    - <span data-ttu-id="c04fa-150">기본값인 **신뢰 수준** 값 60을 그대로 둡니다.</span><span class="sxs-lookup"><span data-stu-id="c04fa-150">Leave the default **Confidence level** value 60.</span></span> 

    - <span data-ttu-id="c04fa-151">기본값인 **문자 근접** 값 300을 그대로 둡니다.</span><span class="sxs-lookup"><span data-stu-id="c04fa-151">Leave the default **Character proximity** value 300.</span></span>

    ![페이지 일치에 대한 요구 사항](media/scc-cust-sens-info-type-new-reqs.png)

    <span data-ttu-id="c04fa-153">작업을 마친 후 **다음**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="c04fa-153">When you're finished, click **Next**.</span></span>

4. <span data-ttu-id="c04fa-154">**검토 및 완료** 페이지가 열리면 설정을 검토하고 **마침**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="c04fa-154">On the **Review and finalize** page that opens, review the settings and click **Finish**.</span></span>

    ![검토 및 완료 페이지](media/scc-cust-sens-info-type-new-review.png)

5. <span data-ttu-id="c04fa-p110">다음 페이지에서는 **예**를 클릭하여 새로운 사용자 지정 중요한 정보 유형을 테스트할 것을 권장합니다. 자세한 내용은 [보안 및 준수 센터에서 사용자 지정 중요한 정보 유형 테스트](#test-custom-sensitive-information-types-in-the-security--compliance-center)를 참조하세요. 나중에 규칙을 테스트하려면 **아니요**를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="c04fa-p110">The next page encourages you to test the new custom sensitive information type by clicking **Yes**. For more information, see [Test custom sensitive information types in the Security & Compliance Center](#test-custom-sensitive-information-types-in-the-security--compliance-center). To test the rule later, click **No**.</span></span>

    ![테스트 권장 사항 페이지](media/scc-cust-sens-info-type-new-test.png)

### <a name="how-do-you-know-this-worked"></a><span data-ttu-id="c04fa-160">작동 여부는 어떻게 확인하나요?</span><span class="sxs-lookup"><span data-stu-id="c04fa-160">How do you know this worked?</span></span>

<span data-ttu-id="c04fa-161">새로운 중요한 정보 유형을 성공적으로 만들었는지 확인하려면 다음 단계를 수행합니다.</span><span class="sxs-lookup"><span data-stu-id="c04fa-161">To verify that you've successfully created a new sensitive information type, do any of the following steps:</span></span>

  - <span data-ttu-id="c04fa-162">**분류** \> **중요한 정보 유형**으로 이동하고 새로운 사용자 지정 중요한 정보 유형이 나열되어 있는지 확인하세요.</span><span class="sxs-lookup"><span data-stu-id="c04fa-162">Go to **Classifications** \> **Sensitive info types** and verify the new custom sensitive information type is listed.</span></span>

  - <span data-ttu-id="c04fa-p111">새로운 사용자 지정 중요한 정보 유형을 테스트합니다. 자세한 내용은, [보안 및 준수 센터에서 사용자 지정 중요한 정보 유형 테스트](#test-custom-sensitive-information-types-in-the-security--compliance-center)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="c04fa-p111">Test the new custom sensitive information type. For more information, see [Test custom sensitive information types in the Security & Compliance Center](#test-custom-sensitive-information-types-in-the-security--compliance-center).</span></span>

## <a name="modify-custom-sensitive-information-types-in-the-security--compliance-center"></a><span data-ttu-id="c04fa-165">보안 및 준수 센터에서 사용자 지정 중요한 정보 유형 수정</span><span class="sxs-lookup"><span data-stu-id="c04fa-165">Modify custom sensitive information types in the Security & Compliance Center</span></span>

<span data-ttu-id="c04fa-166">**참고:**</span><span class="sxs-lookup"><span data-stu-id="c04fa-166">**Notes**:</span></span>

- <span data-ttu-id="c04fa-p112">사용자 지정 중요한 정보 유형만 수정할 수 있습니다. 기본 제공 중요한 정보 유형은 수정할 수 없습니다. 그러나 PowerShell을 사용하여 기본 제공 사용자 지정 중요한 정보 유형을 내보낸 후 사용자 지정하고 사용자 지정 중요한 정보 유형으로 가져올 수 있습니다. 자세한 내용은 [기본 중요한 정보 유형 사용자 지정](customize-a-built-in-sensitive-information-type.md)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="c04fa-p112">You can only modify custom sensitive information types; you can't modify built-in sensitive information types. But you can use PowerShell to export built-in custom sensitive information types, customize them, and import them as custom sensitive information types. For more information, see [Customize a built-in sensitive information type](customize-a-built-in-sensitive-information-type.md).</span></span>

- <span data-ttu-id="c04fa-p113">UI에서 만든 사용자 지정 중요한 정보 유형만 수정할 수 있습니다. [PowerShell 프로시저](create-a-custom-sensitive-information-type-in-scc-powershell.md)를 사용하여 사용자 지정 중요한 정보 유형 규칙 패키지를 가져오면 오류가 발생합니다.</span><span class="sxs-lookup"><span data-stu-id="c04fa-p113">You can only modify custom sensitive information types that you created in the UI. If you used the [PowerShell procedure](create-a-custom-sensitive-information-type-in-scc-powershell.md) to import a custom sensitive information type rule package, you'll get an error.</span></span>

<span data-ttu-id="c04fa-172">보안 및 준수 센터에서 **분류** \> **중요한 정보 유형**으로 이동하고, 수정할 사용자 지정 중요한 정보 유형을 선택한 후 **편집**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="c04fa-172">In the Security & Compliance Center, go to **Classifications** \> **Sensitive info types**, select the custom sensitive information type that you want to modify, and then click **Edit**.</span></span>

  ![중요한 정보 유형 및 편집 단추 위치](media/scc-cust-sens-info-type-edit.png)

<span data-ttu-id="c04fa-p114">보안 및 준수 센터에서 사용자 지정 중요한 정보 유형을 만들 때와 동일한 옵션을 사용할 수 있습니다. 자세한 내용은 [보안 및 준수 센터에서 사용자 지정 중요한 정보 유형 만들기](#create-custom-sensitive-information-types-in-the-security--compliance-center)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="c04fa-p114">The same options are available here as when you created the custom sensitive information type in the Security & Compliance Center. For more information, see [Create custom sensitive information types in the Security & Compliance Center](#create-custom-sensitive-information-types-in-the-security--compliance-center).</span></span>

### <a name="how-do-you-know-this-worked"></a><span data-ttu-id="c04fa-176">작동 여부는 어떻게 확인하나요?</span><span class="sxs-lookup"><span data-stu-id="c04fa-176">How do you know this worked?</span></span>

<span data-ttu-id="c04fa-177">수정한 중요한 정보 유형을 성공적으로 만들었는지 확인하려면 다음 단계를 수행합니다.</span><span class="sxs-lookup"><span data-stu-id="c04fa-177">To verify that you've successfully modified a sensitive information type, do any of the following steps:</span></span>

  - <span data-ttu-id="c04fa-178">**분류** \> **중요한 정보 유형**으로 이동하고 수정한 사용자 지정 중요한 정보 유형의 속성을 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="c04fa-178">Go to **Classifications** \> **Sensitive info types** to verify the properties of the modified custom sensitive information type.</span></span> 

  - <span data-ttu-id="c04fa-p115">수정한 사용자 지정 중요한 정보 유형을 테스트합니다. 자세한 내용은, [보안 및 준수 센터에서 사용자 지정 중요한 정보 유형 테스트](#test-custom-sensitive-information-types-in-the-security--compliance-center)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="c04fa-p115">Test the modified custom sensitive information type. For more information, see [Test custom sensitive information types in the Security & Compliance Center](#test-custom-sensitive-information-types-in-the-security--compliance-center).</span></span>

## <a name="remove-custom-sensitive-information-types-in-the-security--compliance-center"></a><span data-ttu-id="c04fa-181">보안 및 준수 센터에서 사용자 지정 중요한 정보 유형 제거</span><span class="sxs-lookup"><span data-stu-id="c04fa-181">Remove custom sensitive information types in the Security & Compliance Center</span></span> 

<span data-ttu-id="c04fa-182">**참고**:</span><span class="sxs-lookup"><span data-stu-id="c04fa-182">**Notes**:</span></span>

- <span data-ttu-id="c04fa-183">사용자 지정 중요한 정보 유형만 제거할 수 있습니다. 기본 제공 중요한 정보 유형은 제거할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="c04fa-183">You can only remove custom sensitive information types; you can't remove built-in sensitive information types.</span></span>

- <span data-ttu-id="c04fa-184">사용자 지정 중요한 정보 유형을 제거하기 전에 DLP 정책이나 Exchange 메일 흐름 규칙(전송 규칙이라고도 함)이 중요한 정보 유형을 계속 참조하지 않는 것을 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="c04fa-184">Before your remove a custom sensitive information type, verify that no DLP policies or Exchange mail flow rules (also known as transport rules) still reference the sensitive information type.</span></span>

1. <span data-ttu-id="c04fa-185">보안 및 준수 센터에서 **분류** \> **중요한 정보 유형**으로 이동하고, 제거할 사용자 지정 중요한 정보 유형을 한 개 이상 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="c04fa-185">In the Security & Compliance Center, go to **Classifications** \> **Sensitive info types** and select one or more custom sensitive information types that you want to remove.</span></span>

2. <span data-ttu-id="c04fa-186">플라이아웃이 열리면 **삭제**(두 개 이상을 선택한 경우 **중요한 정보 유형 삭제**)를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="c04fa-186">In the fly-out that opens, click **Delete** (or **Delete sensitive info types** if you selected more than one).</span></span>

    ![중요한 정보 유형 및 삭제 단추 위치](media/scc-cust-sens-info-type-delete.png)

3. <span data-ttu-id="c04fa-188">나타나는 경고 메시지에서 **예**를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="c04fa-188">In the warning message that appears, click **Yes**.</span></span>

### <a name="how-do-you-know-this-worked"></a><span data-ttu-id="c04fa-189">작동 여부는 어떻게 확인하나요?</span><span class="sxs-lookup"><span data-stu-id="c04fa-189">How do you know this worked?</span></span>

<span data-ttu-id="c04fa-190">사용자 지정 중요한 정보 유형을 성공적으로 삭제했는지 확인하려면 **분류** \> **중요한 정보 유형**으로 이동하여 사용자 지정 중요한 정보 유형이 더 이상 나열되지 않는지 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="c04fa-190">To verify that you've successfully removed a custom sensitive information type, go to **Classifications** \> **Sensitive info types** to verify the custom sensitive information type is no longer listed.</span></span>

## <a name="test-custom-sensitive-information-types-in-the-security--compliance-center"></a><span data-ttu-id="c04fa-191">보안 및 준수 센터에서 사용자 지정 중요한 정보 유형 테스트</span><span class="sxs-lookup"><span data-stu-id="c04fa-191">Test custom sensitive information types in the Security & Compliance Center</span></span>

1. <span data-ttu-id="c04fa-192">보안 및 준수 센터에서 **분류** \> **중요한 정보 유형**으로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="c04fa-192">In the Security & Compliance Center, go to **Classifications** \> **Sensitive info types**.</span></span>

2. <span data-ttu-id="c04fa-p116">테스트할 하나 이상의 사용자 지정 중요한 정보 유형을 선택합니다. 플라이아웃이 열리면 **유형 테스트**(두 개 이상을 선택한 경우 **중요한 정보 유형 테스트**)를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="c04fa-p116">Select one or more custom sensitive information types to test. In the fly-out that opens, click **Test type** (or **Test sensitive info types** if you selected more than one).</span></span>

    ![중요한 정보 유형 및 유형 테스트 단추 위치](media/scc-cust-sens-info-type-test.png)

3. <span data-ttu-id="c04fa-196">**테스트할 파일 업로드** 페이지가 열리면 파일을 끌어서 놓거나 **찾아보기**를 클릭하고 파일을 선택하여 테스트할 문서를 업로드합니다.</span><span class="sxs-lookup"><span data-stu-id="c04fa-196">On the **Upload file to test** page that opens, upload a document to test by dragging and dropping a file or by clicking **Browse** and selecting a file.</span></span>

    ![테스트할 파일 업로드 페이지](media/scc-cust-sens-info-type-test-upload.png)

4. <span data-ttu-id="c04fa-198">**테스트** 단추를 클릭하여 파일에서 패턴 일치에 대해 문서를 테스트합니다.</span><span class="sxs-lookup"><span data-stu-id="c04fa-198">Click the **Test** button to test the document for pattern matches in the file.</span></span>

5. <span data-ttu-id="c04fa-199">**결과 일치** 페이지에서 **마침**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="c04fa-199">On the **Match results** page, click **Finish**.</span></span>

    ![결과 일치](media/scc-cust-sens-info-type-test-results.png)