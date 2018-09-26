---
title: 오류에 대한 콘텐츠 검색 쿼리 확인
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 11/30/2016
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid: MOE150
ms.assetid: 88898874-e262-4c5c-b6d2-4e697497fc74
description: '오류 및 지원 되지않는 문자 예: 오타에 대 한 콘텐츠 검색에 대 한 키워드 쿼리를 확인 하 고 검색을 실행 하기 전에 부울 연산자를 소문자로 키를 누릅니다. 오류를 발견 되는 경우 수정 된 쿼리를 살펴보시기 표시 됩니다.'
ms.openlocfilehash: 6ae14edc29bb7f8bab5dd2306282a69443872633
ms.sourcegitcommit: 7956955cd919f6e00b64e4506605a743c5872549
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/26/2018
ms.locfileid: "25038291"
---
# <a name="check-your-content-search-query-for-errors"></a><span data-ttu-id="ad341-104">오류에 대한 콘텐츠 검색 쿼리 확인</span><span class="sxs-lookup"><span data-stu-id="ad341-104">Check your Content Search query for errors</span></span>

<span data-ttu-id="ad341-p102">만들거나 콘텐츠 검색을 편집 하는 경우에 지원 되지않는 문자를 대문자로 표시 될 수 있는 부울 연산자 쿼리를 확인 하는 Office 365를 가질 수 있습니다. 어떻게 합니까? 방금 콘텐츠 검색 쿼리 페이지에서 **입력 오류에 대 한 쿼리 확인** 을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad341-p102">When you create or edit a Content Search, you can have Office 365 check your query for unsupported characters and Boolean operators that might not be capitalized. How? Just click **Check query for typos** on the query page of a Content Search.</span></span> 
  
!["오타에 대 한 쿼리 확인" 클릭 지원 되지않는 문자에 대 한 검색 쿼리를 확인 하려면](media/e5314306-cfb2-481d-9b5c-13ce658156e7.png)
  
<span data-ttu-id="ad341-p103">지원 되지않는 문자를 확인 하는데 목록은 다음과 같습니다. 이 속성을 지원 하지 않는 문자는 종종 숨겨지며은 일반적으로 검색 오류가 발생 하거나 원하지 않는 결과 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad341-p103">Here's a list of the unsupported characters that we check for. Unsupported characters are often hidden, and they typically cause a search error or return unintended results.</span></span>
  
- <span data-ttu-id="ad341-p104">**둥근 따옴표로** -스마트 단일와 큰따옴표 (둥근 따옴표 라고도 함)이 지원 되지 않습니다. 검색 쿼리에서 곧은 따옴표를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ad341-p104">**Smart quotation marks** - Smart single and double quotation marks (also called curly quotes) aren't supported. Only straight quotation marks can be used in a search query.</span></span> 
    
- <span data-ttu-id="ad341-p105">**인쇄할 수 없는 및 제어 문자** -인쇄할 수 없 및 제어 문자 영숫자 문자 등의 서 면된 기호를 나타내며 하지 않습니다. 인쇄할 수 없는의 예 및 제어 문자 텍스트 또는 여러 줄 텍스트의 서식을 지정 하는 문자를 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad341-p105">**Non-printable and control characters** - Non-printable and control characters don't represent a written symbol, such as a alpha-numeric character. Examples of non-printable and control characters include characters that format text or separate lines of text.</span></span> 
    
- <span data-ttu-id="ad341-115">**오른쪽으로 왼쪽 및 오른쪽에서 왼쪽으로 표시** -이러한 문자는 제어 문자를 왼쪽에서 오른쪽으로 쓰는 언어 (예: 영어와 스페인어) 및 오른쪽에서 왼쪽으로 쓰는 언어 (예: 아랍어 및 히브리어)에 대 한 텍스트 방향을 나타내는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ad341-115">**Left-to-right and right-to-left marks** - These are control characters used to indicate text direction for left-to-right languages (such as English and Spanish) and right-to-left languages (such as Arabic and Hebrew).</span></span>
    
- <span data-ttu-id="ad341-p106">**소문자 부울 연산자** -부울 연산자, **AND**, **또는**및 **하지** 등의 검색 쿼리를 사용 하는 경우 대문자 여야 합니다. 쿼리 구문 오타에 대 한 쿼리를 확인 하는 경우 부울 연산자가 사용 되 고 있음을 소문자 연산자를 사용할 수 있는 경우에 표시 자주 됩니다. 예, `(WordA or WordB) and (WordC or WordD)`합니다.</span><span class="sxs-lookup"><span data-stu-id="ad341-p106">**Lowercase Boolean operators** - If you use a Boolean operator, such as **AND**, **OR**, and **NOT** in a search query, it must be uppercase. When we check a query for typos, the query syntax will often indicate that a Boolean operator is being used even though lowercase operators might be used; for example,  `(WordA or WordB) and (WordC or WordD)`.</span></span>
    
## <a name="what-happens-if-a-query-has-an-unsupported-character"></a><span data-ttu-id="ad341-118">쿼리를 지원 하지 않는 문자가 포함 하는 경우 어떻게 됩니까?</span><span class="sxs-lookup"><span data-stu-id="ad341-118">What happens if a query has an unsupported character?</span></span>

<span data-ttu-id="ad341-p107">경고 메시지가 발견 된 지원 되지않는 문자를 표시 하는 표시 쿼리에서 지원 하지 않는 문자가 발견 되 면 프로그램 및 대안을 통해 파악할 수 있습니다. 그러면 원래 쿼리를 그대로 사용 하거나 제안된 수정 된 쿼리도 대체 하는 옵션이 다음 제공 합니다. 이전 스크린샷에 검색 쿼리에 대 한 **입력 오류에 대 한 쿼리 확인** 을 클릭 한 후 표시 되는 경고 메시지의 예는 다음과 같습니다. 원래 쿼리 둥근 따옴표 및 소문자 부울 연산자 포함 되어있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad341-p107">If unsupported characters are found in your query, a warning message is displayed that says unsupported characters that were found and a suggests an alternative. Then you then have the option keep the original query or replace it with the suggested revised query. Here's an example of the warning message that's displayed after you click **Check query for typos** for the search query in the previous screenshot. Notice that the original query contains smart quotes and lowercase Boolean operators.</span></span> 
  
![쿼리에 대 한 제안된 수정 함께 경고 메시지가 표시 됩니다.](media/23214b30-8e52-412c-bd80-63fb1b3ed52d.png)
  
## <a name="how-to-prevent-unsupported-characters-in-your-search-queries"></a><span data-ttu-id="ad341-124">검색 쿼리를 지원 하지 않는 문자를 방지 하는 방법</span><span class="sxs-lookup"><span data-stu-id="ad341-124">How to prevent unsupported characters in your search queries</span></span>

<span data-ttu-id="ad341-p108">지원 되지않는 문자 (예: Microsoft Word 또는 Microsoft Excel) 다른 응용 프로그램에서 쿼리 또는 쿼리의 일부를 복사 하 고 콘텐츠 검색 쿼리 페이지에 있는 키워드 상자에 복사 하는 경우에 일반적으로 쿼리에 추가 됩니다. 지원 되지않는 문자를 방지 하기 위해 쿼리 키워드 상자에 입력 하는 가장 좋은 방법은 합니다. 또는 Word 또는 Excel에서 쿼리를 복사할 수 있으며 Microsoft 메모장 등의 일반 텍스트 편집기에서 파일에 붙여넣습니다. 그런 다음 텍스트 파일을 저장 하 고 **ANSI** **인코딩** 드롭다운 목록에서 선택 합니다. 모든 서식 및 지원 되지않는 문자를 사용 하 여 제거 됩니다. 다음 복사 하 고 키워드 쿼리 상자에 텍스트 파일에서 쿼리를 붙여넣을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ad341-p108">Unsupported characters are typically added to a query when you copy the query or parts of the query from other applications (such as Microsoft Word or Microsoft Excel) and copy them to the keyword box on the query page of a Content Search. The best way to prevent unsupported characters is to just type the query in the keyword box. Alternatively, you can copy a query from Word or Excel and then paste it to file in a plain text editor, such as Microsoft Notepad. Then save the text file and select **ANSI** in the **Encoding** drop-down list. This will remove any formatting and unsupported characters. Then you can copy and paste the query from the text file to the keyword query box.</span></span> 
