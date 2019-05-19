---
title: Office 365 Advanced eDiscovery에서 분석에 대 한 텍스트 무시 옵션 설정
ms.author: chrfox
author: chrfox
manager: laurawi
ms.date: 9/14/2017
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: 44055727-56e8-42d7-9dc3-fb942f3901cc
description: 'Office 365 Advanced eDiscovery에서 Analyze 및 Process 모듈을 사용할 때 특정 텍스트를 무시 하는 규칙을 정의 하는 방법을 알아봅니다.  '
ms.openlocfilehash: 70d9879f1cb6b3def06ff978fc2f7fa8f20a92f0
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/17/2019
ms.locfileid: "34156680"
---
# <a name="set-ignore-text-option-for-analyze-in-office-365-advanced-ediscovery"></a><span data-ttu-id="63140-103">Office 365 Advanced eDiscovery에서 분석에 대 한 텍스트 무시 옵션 설정</span><span class="sxs-lookup"><span data-stu-id="63140-103">Set Ignore Text option for Analyze in Office 365 Advanced eDiscovery</span></span>

> [!NOTE]
> <span data-ttu-id="63140-p101">Advanced eDiscovery를 사용하려면 Office 365 E3의 고급 준수 추가 기능이나 조직을 위한 E5 구독이 필요합니다. 이 요금제가 없는 상태에서 Advanced eDiscovery를 사용하려는 경우에는 [Office 365 Enterprise E5 평가판을 등록](https://go.microsoft.com/fwlink/p/?LinkID=698279)할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="63140-p101">Advanced eDiscovery requires an Office 365 E3 with the Advanced Compliance add-on or an E5 subscription for your organization. If you don't have that plan and want to try Advanced eDiscovery, you can [sign up for a trial of Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span></span> 
  
<span data-ttu-id="63140-106">텍스트 무시 기능은 분석 (거의 중복, 전자 메일 스레드, 테마) 및 관련성에 따라 다음과 같은 고급 eDiscovery 모듈 전체 또는 일부에 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="63140-106">The Ignore Text feature can be applied to all or any of the following Advanced eDiscovery modules: Analyze (Near-duplicates, Email Threads, Themes) and Relevance.</span></span> <span data-ttu-id="63140-107">무시 된 텍스트는 관련성이 있는 파일에 표시 되지 않으며, 분석/계산은 무시 되는 텍스트를 무시 합니다.</span><span class="sxs-lookup"><span data-stu-id="63140-107">Ignored text will not appear in files displayed in Relevance, and the analysis/calculations will discard the ignored text.</span></span>
  
<span data-ttu-id="63140-108">이미 실행 했던 모듈에 대해 무시 텍스트 기능이 이전에 정의 된 경우에는 텍스트 무시 설정이 이제 수정 되지 않도록 보호 됩니다.</span><span class="sxs-lookup"><span data-stu-id="63140-108">If the Ignore Text feature was previously defined for modules that have already run, the Ignore Text setting will now be protected from being modified.</span></span> <span data-ttu-id="63140-109">그러나 관련성 모듈에 대 한 텍스트 무시 기능은 언제 든 지 변경 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="63140-109">However, the Ignore Text feature for the Relevance module can still be changed at any time.</span></span>
  
## <a name="how-ignore-text-filters-are-applied"></a><span data-ttu-id="63140-110">무시 텍스트 필터를 적용 하는 방법</span><span class="sxs-lookup"><span data-stu-id="63140-110">How Ignore Text filters are applied</span></span>

<span data-ttu-id="63140-111">여러 Ignore 텍스트 필터는 입력 한 순서 대로 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="63140-111">Multiple Ignore Text filters are applied in the order that they were entered.</span></span> <span data-ttu-id="63140-112">적용 되는 순서를 변경 하려면 삭제 하 고 원하는 순서 대로 다시 입력 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="63140-112">To change the order in which they are applied, they must be deleted and re-entered in the desired order.</span></span>
  
<span data-ttu-id="63140-113">예를 들어 텍스트 콘텐츠가 "DAVE BOB ALICE 고 전날" 인 경우 다음은 무시 텍스트 항목과 결과의 예입니다.</span><span class="sxs-lookup"><span data-stu-id="63140-113">For example, if the text content is: "DAVE BOB ALICE CAROL EVE", the following are samples of Ignore Text entries and the results:</span></span>
  
||||
|:-----|:-----|:-----|
|<span data-ttu-id="63140-114">**텍스트 항목 무시**</span><span class="sxs-lookup"><span data-stu-id="63140-114">**Ignore Text entries**</span></span> <br/> |**==\>** <br/> |<span data-ttu-id="63140-115">**결과**</span><span class="sxs-lookup"><span data-stu-id="63140-115">**Results**</span></span> <br/> |
|<span data-ttu-id="63140-116">"ALICE", "BOB의가을"</span><span class="sxs-lookup"><span data-stu-id="63140-116">"ALICE", "BOB CAROL"</span></span>  <br/> |==\>  <br/> |<span data-ttu-id="63140-117">"DAVE 전날"</span><span class="sxs-lookup"><span data-stu-id="63140-117">"DAVE EVE"</span></span>  <br/> |
|<span data-ttu-id="63140-118">"ALICE", "BOB ALICE 고 대"</span><span class="sxs-lookup"><span data-stu-id="63140-118">"ALICE", "BOB ALICE CAROL"</span></span>  <br/> |==\>  <br/> |<span data-ttu-id="63140-119">"DAVE BOB 고 전날"</span><span class="sxs-lookup"><span data-stu-id="63140-119">"DAVE BOB CAROL EVE"</span></span>  <br/> |
   
<span data-ttu-id="63140-120">첫 번째 무시 텍스트가 적용 된 후에 문자열이 검색 되지 않으므로 두 번째 Ignore 텍스트 항목은 구현 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="63140-120">The second Ignore Text entry is not implemented because the string is not found as such AFTER the first Ignore Text has been applied.</span></span>
  
## <a name="use-regular-expressions-when-defining-ignore-text"></a><span data-ttu-id="63140-121">텍스트 무시를 정의할 때 정규식 사용</span><span class="sxs-lookup"><span data-stu-id="63140-121">Use regular expressions when defining Ignore Text</span></span>

<span data-ttu-id="63140-122">정규식은 무시 텍스트를 정의할 때 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="63140-122">Regular expressions are supported for use when defining Ignore Text.</span></span> <span data-ttu-id="63140-123">다음은 정규식 구문과 사용 방법의 예입니다.</span><span class="sxs-lookup"><span data-stu-id="63140-123">The following are examples of regular expression syntax and usage:</span></span>
  
- <span data-ttu-id="63140-124">시작 부분에서 줄 끝까지 텍스트를 제거 하려면 다음을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="63140-124">To remove (ignore) text from Begin until the end of a line:</span></span>
    
     `Begin(.*)$`
    
    <span data-ttu-id="63140-125">여기에서 "Begin"은 줄에서이 문자열의 초기 항목입니다.</span><span class="sxs-lookup"><span data-stu-id="63140-125">where "Begin" is the initial occurrence of this string in the line.</span></span>
    
    <span data-ttu-id="63140-126">예를 들어 다음과 같은 텍스트를 예로 들 있습니다.</span><span class="sxs-lookup"><span data-stu-id="63140-126">For example, for the following text:</span></span>
    
    <span data-ttu-id="63140-127">**"이 문장이 나 첫 번째 줄입니다.**</span><span class="sxs-lookup"><span data-stu-id="63140-127">**"This is first sentence and first line**</span></span>
    
    <span data-ttu-id="63140-128">**두 번째 문장이 며 두 번째 줄이 됩니다. "**</span><span class="sxs-lookup"><span data-stu-id="63140-128">**This is second sentence and second line"**</span></span>
    
    <span data-ttu-id="63140-129">정규식 first (.\*) $의 결과는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="63140-129">the Regular Expression first(.\*)$ will result in:</span></span>
    
    <span data-ttu-id="63140-130">**"이는**</span><span class="sxs-lookup"><span data-stu-id="63140-130">**"This is**</span></span>
    
    <span data-ttu-id="63140-131">**두 번째 문장이 며 두 번째 줄이 됩니다. "**</span><span class="sxs-lookup"><span data-stu-id="63140-131">**This is second sentence and second line"**</span></span>
    
- <span data-ttu-id="63140-132">전자 메일 스레드 끝에 자동으로 삽입 되는 고 지 사항 및 법률 문서를 제거 하려면:</span><span class="sxs-lookup"><span data-stu-id="63140-132">To remove disclaimers and legal statements automatically inserted at the end of email threads:</span></span>
    
     `Begin(.|\s)*End`
    
    <span data-ttu-id="63140-133">여기서 "Begin" 및 "End"는 줄 바꿈된 텍스트 단락의 시작과 끝에 있는 고유한 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="63140-133">where "Begin" and "End" are unique strings at the beginning and end of a wrapped text paragraph.</span></span> 
    
    <span data-ttu-id="63140-134">예를 들어 다음 정규식은 Begin 및 End 문자열 사이에 있는 전자 메일 스레드에 있는 고 지 사항 및 법률 자문을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="63140-134">For example, the following regular expression will remove disclaimers and legal statements that were in the email thread between the Begin and End strings:</span></span>
    
    <span data-ttu-id="63140-135">**이 메시지에는 기밀 정보 (. | \s)\*확인이 필요한 경우 하드 카피 버전을 요청 하세요.**</span><span class="sxs-lookup"><span data-stu-id="63140-135">**This message contains confidential information (.|\s)\*If verification is required please request a hard-copy version**</span></span>
    
- <span data-ttu-id="63140-136">고 지 사항 (특수 문자 포함)을 제거 하려면</span><span class="sxs-lookup"><span data-stu-id="63140-136">To remove a disclaimer (including special characters):</span></span> 
    
    <span data-ttu-id="63140-137">예를 들어 다음 텍스트 (고 지 사항이 x로 표시 됨)에 대해 다음을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="63140-137">For example, for the following text (with the disclaimer represented here by x's):</span></span> 
    
    <span data-ttu-id="63140-138">**/\*\이 메시지에는 기밀 정보가 포함 되어 있습니다. xxxx xxxx**</span><span class="sxs-lookup"><span data-stu-id="63140-138">**/\*\ This message contains confidential information. xxxx xxxx**</span></span>
    
    <span data-ttu-id="63140-139">**xxxx xxxx xxxx xxxx xxxx xxxx xxxx**</span><span class="sxs-lookup"><span data-stu-id="63140-139">**xxxx xxxx xxxx xxxx xxxx xxxx xxxx**</span></span>
    
    <span data-ttu-id="63140-140">\**xxxx xxxx 확인이 필요한 경우에는 하드 카피 버전을 요청 하세요. /\*\**</span><span class="sxs-lookup"><span data-stu-id="63140-140">\**xxxx xxxx If verification is required, please request a hard-copy version. /\*\**</span></span>
    
    <span data-ttu-id="63140-141">위의 부인 내용을 제거 하는 정규식은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="63140-141">the regular expression to remove the above disclaimer should be:</span></span> 
    
    <span data-ttu-id="63140-142">**\/\\*\\이 메시지에는 기밀\.정보 (. | \s)\* 확인이 필요한 경우 하드 카피 버전\. 을 요청 하세요.\/\\*\\**</span><span class="sxs-lookup"><span data-stu-id="63140-142">**\/\\*\\ This message contains confidential information\.(.|\s)\* If verification is required please request a hard-copy version\. \/\\*\\**</span></span>
    
- <span data-ttu-id="63140-143">정규식 규칙:</span><span class="sxs-lookup"><span data-stu-id="63140-143">Regular expression rules:</span></span>
    
  - <span data-ttu-id="63140-144">공백을 제외 하 고 알파벳의 일부가 아닌 모든 문자, "_" 및 "-"은 앞에 "가와 야 합니다\".</span><span class="sxs-lookup"><span data-stu-id="63140-144">Any characters that are not part of the alphabet except for space(s), "_" and "-" must be preceded by "\".</span></span>
    
  - <span data-ttu-id="63140-145">일반 eExpression 필드의 길이에는 제한이 없습니다.</span><span class="sxs-lookup"><span data-stu-id="63140-145">The regular eExpression field can be unlimited length.</span></span>
    
> [!TIP]
> <span data-ttu-id="63140-146">정규식의 자세한 설명과 자세한 내용은 [정규식 언어-빠른 참조](https://msdn.microsoft.com/en-us/library/az24scfc%28v=vs.110%29.aspx)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="63140-146">For an explanation and detailed syntax of regular expressions, see: [Regular Expression Language - Quick Reference](https://msdn.microsoft.com/en-us/library/az24scfc%28v=vs.110%29.aspx).</span></span> 
  
## <a name="define-ignore-text-rule"></a><span data-ttu-id="63140-147">무시 텍스트 규칙 정의</span><span class="sxs-lookup"><span data-stu-id="63140-147">Define Ignore Text rule</span></span>

1. <span data-ttu-id="63140-148">분석 \*\* \> 분석 옵션 \> 관리\*\* 탭의 **텍스트 무시** 섹션에서 **+** 아이콘을 클릭 하 여 규칙을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="63140-148">In the **Manage \> Analyze \> Analyze options** tab, in the **Ignore Text** section, click the **+** icon to add a rule.</span></span> 
    
2. <span data-ttu-id="63140-149">**Ignore 텍스트 추가** 대화 상자의 **이름** 필드에 무시 텍스트 규칙의 이름을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="63140-149">In the **Add Ignore Text** dialog, in the **Name** field, type a name for the Ignore Text rule.</span></span> 
    
    ![무시 하는 텍스트 추가](media/98e5129b-2667-4692-86fa-2d0117187a7f.png)
  
3. <span data-ttu-id="63140-151">**텍스트** 상자에 무시할 텍스트를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="63140-151">In the **Text** box, type the text to be ignored.</span></span> <span data-ttu-id="63140-152">텍스트 필드에 무제한의 문자를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="63140-152">The text field allows an unlimited number of characters.</span></span> 
    
    > [!TIP]
    > <span data-ttu-id="63140-153">위의 창에 표시 된 것 처럼 전구 \*\*\*\* 를 클릭 하 여 Ignore 텍스트 규칙에 대 한 일반적인 구문 지침을 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="63140-153">As shown in the window above, click **light bulb** to see common syntax guidelines for the Ignore Text rule.</span></span> 
  
4. <span data-ttu-id="63140-154">필요한 경우 **대/소문자 구분** 확인란을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="63140-154">Select the **Case sensitive** check box, if desired.</span></span> 
    
5. <span data-ttu-id="63140-155">**적용 대상** 목록에서 정의를 적용할 고급 eDiscovery 모듈을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="63140-155">In the **Apply to** list, select the Advanced eDiscovery modules in which to apply the definition.</span></span> 
    
6. <span data-ttu-id="63140-156">예제 텍스트에 대 한 테스트를 실행 하려면 **입력** 텍스트 상자에 예제 텍스트를 입력 하 고 **테스트**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="63140-156">If you want a test run on sample text, type sample text in the **Input** text box and click **Test**.</span></span> <span data-ttu-id="63140-157">결과가 **출력** 텍스트 상자에 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="63140-157">The results are displayed in the **Output** text box.</span></span> 
    
7. <span data-ttu-id="63140-158">**확인** 을 클릭 하 여 무시 텍스트 규칙을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="63140-158">Click **OK** to save the Ignore Text rule.</span></span> <span data-ttu-id="63140-159">정의 된 Ignore 텍스트 규칙이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="63140-159">The defined Ignore Text rule is displayed.</span></span> 
    
    ![무시 설정 텍스트 이름](media/3a788ac3-4a1c-46c9-89bd-7ff32d68ce23.png)
  
## <a name="see-also"></a><span data-ttu-id="63140-161">참고 항목</span><span class="sxs-lookup"><span data-stu-id="63140-161">See also</span></span>

[<span data-ttu-id="63140-162">Office 365 Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="63140-162">Office 365 Advanced eDiscovery</span></span>](office-365-advanced-ediscovery.md)
  
[<span data-ttu-id="63140-163">문서 유사성 이해</span><span class="sxs-lookup"><span data-stu-id="63140-163">Understanding document similarity</span></span>](understand-document-similarity-in-advanced-ediscovery.md)
  
[<span data-ttu-id="63140-164">분석 옵션 설정</span><span class="sxs-lookup"><span data-stu-id="63140-164">Setting Analyze options</span></span>](set-analyze-options-in-advanced-ediscovery.md)
  
[<span data-ttu-id="63140-165">고급 설정 분석 설정</span><span class="sxs-lookup"><span data-stu-id="63140-165">Setting Analyze advanced settings</span></span>](set-analyze-advanced-settings-in-advanced-ediscovery.md)
  
[<span data-ttu-id="63140-166">분석 결과 보기</span><span class="sxs-lookup"><span data-stu-id="63140-166">Viewing Analyze results</span></span>](view-analyze-results-in-advanced-ediscovery.md)

