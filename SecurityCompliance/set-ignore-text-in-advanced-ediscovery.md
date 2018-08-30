---
title: Office 365 Advanced eDiscovery에서 분석에 대한 텍스트 무시 옵션 설정
ms.author: chrfox
author: chrfox
manager: laurawi
ms.date: 9/14/2017
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: 44055727-56e8-42d7-9dc3-fb942f3901cc
description: 'Office 365 고급 eDiscovery의 분석 및 프로세스 모듈을 사용 하는 경우 특정 텍스트를 무시 하도록 규칙을 정의 하는 방법에 알아봅니다.  '
ms.openlocfilehash: eb7e7052979087b7dba98aac3b0c9ab75ec0d02a
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22533541"
---
# <a name="set-ignore-text-option-for-analyze-in-office-365-advanced-ediscovery"></a><span data-ttu-id="a57be-103">Office 365 Advanced eDiscovery에서 분석에 대한 텍스트 무시 옵션 설정</span><span class="sxs-lookup"><span data-stu-id="a57be-103">Set Ignore Text option for Analyze in Office 365 Advanced eDiscovery</span></span>

> [!NOTE]
> <span data-ttu-id="a57be-p101">고급 eDiscovery 조직에 대 한 고급 준수 추가 기능 또는 e 5 구독은 Office 365 E3 필요합니다. 해당 요금제에 가입한 상태 고급 eDiscovery 시도 하려는 하지 경우에 [Office 365 Enterprise e 5의 평가판 등록](https://go.microsoft.com/fwlink/p/?LinkID=698279)할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a57be-p101">Advanced eDiscovery requires an Office 365 E3 with the Advanced Compliance add-on or an E5 subscription for your organization. If you don't have that plan and want to try Advanced eDiscovery, you can [sign up for a trial of Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span></span> 
  
<span data-ttu-id="a57be-p102">다음과 같은 고급 eDiscovery 모듈 중 하나 또는 모두에 텍스트를 무시 기능을 적용할 수 있습니다: (근처-중복 되는 값, 전자 메일 스레드 테마)를 분석 하 고 관련성 합니다. 무시 텍스트 관련성을에 표시 되는 파일에 표시 되지 않으며 분석/계산 무시 텍스트를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="a57be-p102">The Ignore Text feature can be applied to all or any of the following Advanced eDiscovery modules: Analyze (Near-duplicates, Email Threads, Themes) and Relevance. Ignored text will not appear in files displayed in Relevance, and the analysis/calculations will discard the ignored text.</span></span>
  
<span data-ttu-id="a57be-p103">텍스트를 무시 기능이 이미 실행 되는 모듈에 대 한 이전에 정의 된 경우 텍스트를 무시 설정은 수정 되지 이제 보호 됩니다. 그러나 관련성 모듈에 대 한 텍스트를 무시 기능 언제 든 지 여전히 변경할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a57be-p103">If the Ignore Text feature was previously defined for modules that have already run, the Ignore Text setting will now be protected from being modified. However, the Ignore Text feature for the Relevance module can still be changed at any time.</span></span>
  
## <a name="how-ignore-text-filters-are-applied"></a><span data-ttu-id="a57be-110">텍스트를 무시 필터가 적용 되는 방법</span><span class="sxs-lookup"><span data-stu-id="a57be-110">How Ignore Text filters are applied</span></span>

<span data-ttu-id="a57be-p104">여러 무시 텍스트 필터는 입력 된 순서로 적용 됩니다. 적용 되는 순서를 변경 하려면 자신이 해야 삭제 되어 원하는 순서로 다시 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="a57be-p104">Multiple Ignore Text filters are applied in the order that they were entered. To change the order in which they are applied, they must be deleted and re-entered in the desired order.</span></span>
  
<span data-ttu-id="a57be-113">예: 텍스트 콘텐츠가 경우: "DAVE BOB ALICE CAROL EVE"는 다음과 같은 항목 텍스트를 무시 하 고 결과의 샘플:</span><span class="sxs-lookup"><span data-stu-id="a57be-113">For example, if the text content is: "DAVE BOB ALICE CAROL EVE", the following are samples of Ignore Text entries and the results:</span></span>
  
||||
|:-----|:-----|:-----|
|<span data-ttu-id="a57be-114">**텍스트 항목을 무시 합니다.**</span><span class="sxs-lookup"><span data-stu-id="a57be-114">**Ignore Text entries**</span></span> <br/> |**==\>** <br/> |<span data-ttu-id="a57be-115">**결과**</span><span class="sxs-lookup"><span data-stu-id="a57be-115">**Results**</span></span> <br/> |
|<span data-ttu-id="a57be-116">"ALICE", "CAROL BOB"</span><span class="sxs-lookup"><span data-stu-id="a57be-116">"ALICE", "BOB CAROL"</span></span>  <br/> |==\>  <br/> |<span data-ttu-id="a57be-117">"DAVE EVE"</span><span class="sxs-lookup"><span data-stu-id="a57be-117">"DAVE EVE"</span></span>  <br/> |
|<span data-ttu-id="a57be-118">"ALICE", "ALICE BOB CAROL"</span><span class="sxs-lookup"><span data-stu-id="a57be-118">"ALICE", "BOB ALICE CAROL"</span></span>  <br/> |==\>  <br/> |<span data-ttu-id="a57be-119">"DAVE BOB CAROL EVE"</span><span class="sxs-lookup"><span data-stu-id="a57be-119">"DAVE BOB CAROL EVE"</span></span>  <br/> |
   
<span data-ttu-id="a57be-120">두번째 무시 텍스트 항목에는 첫번째 무시 텍스트가 적용 된 후에 문자열이 이와 같이 발견 되지 않으면 때문에 구현 되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="a57be-120">The second Ignore Text entry is not implemented because the string is not found as such AFTER the first Ignore Text has been applied.</span></span>
  
## <a name="use-regular-expressions-when-defining-ignore-text"></a><span data-ttu-id="a57be-121">텍스트를 무시를 정의할 때 정규식을 사용 하 여</span><span class="sxs-lookup"><span data-stu-id="a57be-121">Use regular expressions when defining Ignore Text</span></span>

<span data-ttu-id="a57be-p105">정규식 무시 텍스트를 정의할 때 사용할 수 있도록 지원 합니다. 다음은 정규식 구문 및 사용법의 예입니다.</span><span class="sxs-lookup"><span data-stu-id="a57be-p105">Regular expressions are supported for use when defining Ignore Text. The following are examples of regular expression syntax and usage:</span></span>
  
- <span data-ttu-id="a57be-124">제거 하려면 (무시) 텍스트 줄의 끝까지 시작에서:</span><span class="sxs-lookup"><span data-stu-id="a57be-124">To remove (ignore) text from Begin until the end of a line:</span></span>
    
     `Begin(.*)$`
    
    <span data-ttu-id="a57be-125">여기서 "Begin"는 줄에서이 문자열의 초기 항목입니다.</span><span class="sxs-lookup"><span data-stu-id="a57be-125">where "Begin" is the initial occurrence of this string in the line.</span></span>
    
    <span data-ttu-id="a57be-126">예: 다음 텍스트:</span><span class="sxs-lookup"><span data-stu-id="a57be-126">For example, for the following text:</span></span>
    
    <span data-ttu-id="a57be-127">**"이 고 첫 문장 첫 줄**</span><span class="sxs-lookup"><span data-stu-id="a57be-127">**"This is first sentence and first line**</span></span>
    
    <span data-ttu-id="a57be-128">**이 두번째 문장 및 둘째 줄 "**</span><span class="sxs-lookup"><span data-stu-id="a57be-128">**This is second sentence and second line"**</span></span>
    
    <span data-ttu-id="a57be-129">정규식 first(.\*) $ 발생 합니다.</span><span class="sxs-lookup"><span data-stu-id="a57be-129">the Regular Expression first(.\*)$ will result in:</span></span>
    
    <span data-ttu-id="a57be-130">**"This is**</span><span class="sxs-lookup"><span data-stu-id="a57be-130">**"This is**</span></span>
    
    <span data-ttu-id="a57be-131">**이 두번째 문장 및 둘째 줄 "**</span><span class="sxs-lookup"><span data-stu-id="a57be-131">**This is second sentence and second line"**</span></span>
    
- <span data-ttu-id="a57be-132">법적 고 지 사항 및 전자 메일 스레드의 끝에 자동으로 삽입 된 법률 정보를 제거 하는 방법</span><span class="sxs-lookup"><span data-stu-id="a57be-132">To remove disclaimers and legal statements automatically inserted at the end of email threads:</span></span>
    
     `Begin(.|\s)*End`
    
    <span data-ttu-id="a57be-133">여기서 "시작" 및 "종료"는 겹쳐진된 텍스트 단락의 시작과 끝에 고유한 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="a57be-133">where "Begin" and "End" are unique strings at the beginning and end of a wrapped text paragraph.</span></span> 
    
    <span data-ttu-id="a57be-134">예 다음 정규식 법적 고 지 사항 및 전자 메일 스레드 Begin 및 End 문자열 사이에서 있던 법률 정보 제거 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a57be-134">For example, the following regular expression will remove disclaimers and legal statements that were in the email thread between the Begin and End strings:</span></span>
    
    <span data-ttu-id="a57be-135">**기밀 정보를 포함 하는이 메시지 (. | \s)\*확인이 필요 하면 하드 카피 버전을 요청 하십시오**</span><span class="sxs-lookup"><span data-stu-id="a57be-135">**This message contains confidential information (.|\s)\*If verification is required please request a hard-copy version**</span></span>
    
- <span data-ttu-id="a57be-136">제거 하려면 (특수 문자를 포함 하 여) 하는 고 지 사항:</span><span class="sxs-lookup"><span data-stu-id="a57be-136">To remove a disclaimer (including special characters):</span></span> 
    
    <span data-ttu-id="a57be-137">예 (x 하 여 여기에 표시 되 고 지 사항)와 다음 텍스트:</span><span class="sxs-lookup"><span data-stu-id="a57be-137">For example, for the following text (with the disclaimer represented here by x's):</span></span> 
    
    <span data-ttu-id="a57be-138">**/\*\ \이 메시지는 기밀 정보를 포함합니다. 이며 이며**</span><span class="sxs-lookup"><span data-stu-id="a57be-138">**/\*\ This message contains confidential information. xxxx xxxx**</span></span>
    
    <span data-ttu-id="a57be-139">**이며 이며 이며 이며 이며 이며 이며**</span><span class="sxs-lookup"><span data-stu-id="a57be-139">**xxxx xxxx xxxx xxxx xxxx xxxx xxxx**</span></span>
    
    <span data-ttu-id="a57be-140">\**이며 이며 확인이 필요한 경우에 하드 카피 버전을 요청 하십시오. /\*\**</span><span class="sxs-lookup"><span data-stu-id="a57be-140">\**xxxx xxxx If verification is required, please request a hard-copy version. /\*\**</span></span>
    
    <span data-ttu-id="a57be-141">위의 고 지 사항은 제거 하는 정규식 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a57be-141">the regular expression to remove the above disclaimer should be:</span></span> 
    
    <span data-ttu-id="a57be-142">**\/\\*\\기밀 정보를 포함 하는이 메시지\.(. | \s)\* 확인이 필요 하면 하드 카피 버전을 요청 하십시오\.\/\\*\\**</span><span class="sxs-lookup"><span data-stu-id="a57be-142">**\/\\*\\ This message contains confidential information\.(.|\s)\* If verification is required please request a hard-copy version\. \/\\*\\**</span></span>
    
- <span data-ttu-id="a57be-143">정규식 규칙:</span><span class="sxs-lookup"><span data-stu-id="a57be-143">Regular expression rules:</span></span>
    
  - <span data-ttu-id="a57be-144">공간, "_"를 제외 하 고 알파벳의 일부가 아닌 모든 문자 및 "-" 앞에 나와야 "\"합니다.</span><span class="sxs-lookup"><span data-stu-id="a57be-144">Any characters that are not part of the alphabet except for space(s), "_" and "-" must be preceded by "\".</span></span>
    
  - <span data-ttu-id="a57be-145">일반 eExpression 필드 길이 제한 없음을된 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a57be-145">The regular eExpression field can be unlimited length.</span></span>
    
> [!TIP]
> <span data-ttu-id="a57be-146">설명과 정규식의 자세한 구문에 대 한 참조: [일반 표현 언어-빠른 참조](https://msdn.microsoft.com/en-us/library/az24scfc%28v=vs.110%29.aspx)합니다.</span><span class="sxs-lookup"><span data-stu-id="a57be-146">For an explanation and detailed syntax of regular expressions, see: [Regular Expression Language - Quick Reference](https://msdn.microsoft.com/en-us/library/az24scfc%28v=vs.110%29.aspx).</span></span> 
  
## <a name="define-ignore-text-rule"></a><span data-ttu-id="a57be-147">텍스트를 무시 규칙 정의</span><span class="sxs-lookup"><span data-stu-id="a57be-147">Define Ignore Text rule</span></span>

1. <span data-ttu-id="a57be-148">**관리 \> 분석 \> 옵션 분석** **무시 텍스트** 섹션에서 탭을 클릭 하는 **+** 규칙을 추가 하는 아이콘 합니다.</span><span class="sxs-lookup"><span data-stu-id="a57be-148">In the **Manage \> Analyze \> Analyze options** tab, in the **Ignore Text** section, click the **+** icon to add a rule.</span></span> 
    
2. <span data-ttu-id="a57be-149">**이름** 필드에서 **무시 텍스트 추가** 대화 상자에서 텍스트를 무시 규칙에 대 한 이름을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="a57be-149">In the **Add Ignore Text** dialog, in the **Name** field, type a name for the Ignore Text rule.</span></span> 
    
    ![무시 하는 텍스트 추가](media/98e5129b-2667-4692-86fa-2d0117187a7f.png)
  
3. <span data-ttu-id="a57be-p106">**텍스트** 상자에서 무시 되도록 텍스트를 입력 합니다. 텍스트 필드에는 무제한 개수의 문자 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a57be-p106">In the **Text** box, type the text to be ignored. The text field allows an unlimited number of characters.</span></span> 
    
    > [!TIP]
    > <span data-ttu-id="a57be-153">위쪽 창에 표시 된 것과 같이 무시 텍스트 규칙에 대 한 일반적인 구문을 지침을 보려면 **전구** 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="a57be-153">As shown in the window above, click **light bulb** to see common syntax guidelines for the Ignore Text rule.</span></span> 
  
4. <span data-ttu-id="a57be-154">원하는 경우 **대/소문자 구분** 확인란을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="a57be-154">Select the **Case sensitive** check box, if desired.</span></span> 
    
5. <span data-ttu-id="a57be-155">**적용 대상** 목록에서 프로그램 정의 적용 하는 고급 eDiscovery 모듈을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="a57be-155">In the **Apply to** list, select the Advanced eDiscovery modules in which to apply the definition.</span></span> 
    
6. <span data-ttu-id="a57be-p107">예제 텍스트에서 실행 하는 테스트를 **입력** 텍스트 상자에 예제 텍스트를 입력 하 고 **테스트**를 클릭 합니다. 결과 **출력** 텍스트 상자에 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a57be-p107">If you want a test run on sample text, type sample text in the **Input** text box and click **Test**. The results are displayed in the **Output** text box.</span></span> 
    
7. <span data-ttu-id="a57be-p108">텍스트를 무시 규칙을 저장 하려면 **확인** 클릭 합니다. 정의 된 텍스트를 무시 규칙이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a57be-p108">Click **OK** to save the Ignore Text rule. The defined Ignore Text rule is displayed.</span></span> 
    
    ![무시 설정 텍스트 이름](media/3a788ac3-4a1c-46c9-89bd-7ff32d68ce23.png)
  
## <a name="see-also"></a><span data-ttu-id="a57be-161">참고 항목</span><span class="sxs-lookup"><span data-stu-id="a57be-161">See also</span></span>

[<span data-ttu-id="a57be-162">Office 365 Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="a57be-162">Office 365 Advanced eDiscovery</span></span>](office-365-advanced-ediscovery.md)
  
[<span data-ttu-id="a57be-163">문서 다음과 비슷한 이해 (영문)</span><span class="sxs-lookup"><span data-stu-id="a57be-163">Understanding document similarity</span></span>](understand-document-similarity-in-advanced-ediscovery.md)
  
[<span data-ttu-id="a57be-164">분석 옵션 설정</span><span class="sxs-lookup"><span data-stu-id="a57be-164">Setting Analyze options</span></span>](set-analyze-options-in-advanced-ediscovery.md)
  
[<span data-ttu-id="a57be-165">고급 설정 설정 분석</span><span class="sxs-lookup"><span data-stu-id="a57be-165">Setting Analyze advanced settings</span></span>](set-analyze-advanced-settings-in-advanced-ediscovery.md)
  
[<span data-ttu-id="a57be-166">분석 결과 보기</span><span class="sxs-lookup"><span data-stu-id="a57be-166">Viewing Analyze results</span></span>](view-analyze-results-in-advanced-ediscovery.md)

