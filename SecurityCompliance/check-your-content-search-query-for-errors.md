---
title: 오류에 대한 콘텐츠 검색 쿼리 확인
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 11/30/2016
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid: MOE150
ms.assetid: 88898874-e262-4c5c-b6d2-4e697497fc74
description: 검색을 실행 하기 전에 키워드 쿼리를 검사 하 여 지원 되지 않는 문자나 소문자 부울 연산자와 같은 오류 및 오타에 대 한 콘텐츠 검색을 확인 합니다. 오류가 발견 되 면 수정 된 쿼리를 제안 합니다.
ms.openlocfilehash: 9f9f59c4466102d678bc3a599aa208869bbd9d64
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/17/2019
ms.locfileid: "34155580"
---
# <a name="check-your-content-search-query-for-errors"></a><span data-ttu-id="791b7-104">오류에 대한 콘텐츠 검색 쿼리 확인</span><span class="sxs-lookup"><span data-stu-id="791b7-104">Check your Content Search query for errors</span></span>

<span data-ttu-id="791b7-105">콘텐츠 검색을 만들거나 편집할 때 Office 365에서 쿼리를 검사 하 여 지원 되지 않는 문자와 대문자로 표시할 수 없는 부울 연산자를 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="791b7-105">When you create or edit a Content Search, you can have Office 365 check your query for unsupported characters and Boolean operators that might not be capitalized.</span></span> <span data-ttu-id="791b7-106">미치는?</span><span class="sxs-lookup"><span data-stu-id="791b7-106">How?</span></span> <span data-ttu-id="791b7-107">콘텐츠 검색의 쿼리 페이지에서 **오타가 있는지 확인을** 클릭 하기만 하면 됩니다.</span><span class="sxs-lookup"><span data-stu-id="791b7-107">Just click **Check query for typos** on the query page of a Content Search.</span></span> 
  
!["오타에 대 한 쿼리 확인"을 클릭 하 여 검색 쿼리를 검사 하 여 지원 되지 않는 문자](media/e5314306-cfb2-481d-9b5c-13ce658156e7.png)
  
<span data-ttu-id="791b7-109">여기에는 검사 하는 지원 되지 않는 문자 목록이 나와 있습니다.</span><span class="sxs-lookup"><span data-stu-id="791b7-109">Here's a list of the unsupported characters that we check for.</span></span> <span data-ttu-id="791b7-110">지원 되지 않는 문자는 대개 숨겨지고 대개 검색 오류가 발생 하거나 의도 하지 않은 결과가 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="791b7-110">Unsupported characters are often hidden, and they typically cause a search error or return unintended results.</span></span>
  
- <span data-ttu-id="791b7-111">**스마트 따옴표** -둥근 작은따옴표나 큰따옴표 (굽은 따옴표 라고도 함)는 지원 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="791b7-111">**Smart quotation marks** - Smart single and double quotation marks (also called curly quotes) aren't supported.</span></span> <span data-ttu-id="791b7-112">검색 쿼리에는 곧은 따옴표만 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="791b7-112">Only straight quotation marks can be used in a search query.</span></span> 
    
- <span data-ttu-id="791b7-113">인쇄할 수 없는 문자와 **제어 되지 않는 문자** -인쇄할 수 없는 문자 및 제어 되는 문자는 부호 있는 기호를 나타내지 않습니다 (예: 영문자).</span><span class="sxs-lookup"><span data-stu-id="791b7-113">**Non-printable and control characters** - Non-printable and control characters don't represent a written symbol, such as a alpha-numeric character.</span></span> <span data-ttu-id="791b7-114">인쇄할 수 없는 문자 및 제어 문자의 예로는 텍스트 또는 별도의 텍스트 줄을 지정 하는 문자를 들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="791b7-114">Examples of non-printable and control characters include characters that format text or separate lines of text.</span></span> 
    
- <span data-ttu-id="791b7-115">**왼쪽에서 오른쪽 및 오른쪽에서 왼쪽 표시** -왼쪽에서 오른쪽으로 쓰기 언어의 텍스트 방향 (예: 영어 및 스페인어) 및 오른쪽에서 왼쪽으로 쓰기 언어 (아랍어, 히브리어)를 나타내는 데 사용 되는 제어 문자입니다.</span><span class="sxs-lookup"><span data-stu-id="791b7-115">**Left-to-right and right-to-left marks** - These are control characters used to indicate text direction for left-to-right languages (such as English and Spanish) and right-to-left languages (such as Arabic and Hebrew).</span></span>
    
- <span data-ttu-id="791b7-116">**소문자 부울 연산자** -검색 쿼리에 **NOT** **And**, **OR**등의 부울 연산자를 사용 하는 경우에는 대문자 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="791b7-116">**Lowercase Boolean operators** - If you use a Boolean operator, such as **AND**, **OR**, and **NOT** in a search query, it must be uppercase.</span></span> <span data-ttu-id="791b7-117">쿼리에 오타가 있는지 여부를 확인 하는 경우 쿼리 구문에는 소문자 연산자를 사용할 수 있지만 부울 연산자가 사용 되는 것으로 표시 되는 경우가 많습니다. 예를 `(WordA or WordB) and (WordC or WordD)`들면입니다.</span><span class="sxs-lookup"><span data-stu-id="791b7-117">When we check a query for typos, the query syntax will often indicate that a Boolean operator is being used even though lowercase operators might be used; for example,  `(WordA or WordB) and (WordC or WordD)`.</span></span>
    
## <a name="what-happens-if-a-query-has-an-unsupported-character"></a><span data-ttu-id="791b7-118">쿼리에 지원 되지 않는 문자가 있으면 어떻게 되나요?</span><span class="sxs-lookup"><span data-stu-id="791b7-118">What happens if a query has an unsupported character?</span></span>

<span data-ttu-id="791b7-119">쿼리에서 지원 되지 않는 문자가 발견 되 면 발견 된 지원 되지 않는 문자와 대안을 제안 하는 경고 메시지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="791b7-119">If unsupported characters are found in your query, a warning message is displayed that says unsupported characters that were found and a suggests an alternative.</span></span> <span data-ttu-id="791b7-120">그런 다음 원래 쿼리를 유지 하거나 제안 된 수정 쿼리로 바꿀 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="791b7-120">Then you then have the option keep the original query or replace it with the suggested revised query.</span></span> <span data-ttu-id="791b7-121">다음은 이전 스크린샷에 검색 쿼리에 대 한 **오타가 있는지 확인** 을 클릭 하면 표시 되는 경고 메시지의 예입니다.</span><span class="sxs-lookup"><span data-stu-id="791b7-121">Here's an example of the warning message that's displayed after you click **Check query for typos** for the search query in the previous screenshot.</span></span> <span data-ttu-id="791b7-122">원래 쿼리에는 스마트 시황 및 소문자 부울 연산자가 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="791b7-122">Notice that the original query contains smart quotes and lowercase Boolean operators.</span></span> 
  
![쿼리에 대 한 제안 된 수정 내용으로 경고 메시지가 표시 됨](media/23214b30-8e52-412c-bd80-63fb1b3ed52d.png)
  
## <a name="how-to-prevent-unsupported-characters-in-your-search-queries"></a><span data-ttu-id="791b7-124">검색 쿼리에서 지원 되지 않는 문자를 차단 하는 방법</span><span class="sxs-lookup"><span data-stu-id="791b7-124">How to prevent unsupported characters in your search queries</span></span>

<span data-ttu-id="791b7-125">지원 되지 않는 문자는 대개 쿼리 또는 쿼리 일부를 Microsoft Word 또는 Microsoft Excel 등의 다른 응용 프로그램에서 복사 하 고 콘텐츠 검색의 쿼리 페이지에 있는 키워드 상자에 복사할 때 쿼리에 추가 됩니다.</span><span class="sxs-lookup"><span data-stu-id="791b7-125">Unsupported characters are typically added to a query when you copy the query or parts of the query from other applications (such as Microsoft Word or Microsoft Excel) and copy them to the keyword box on the query page of a Content Search.</span></span> <span data-ttu-id="791b7-126">지원 되지 않는 문자를 차단 하는 가장 좋은 방법은 키워드 상자에 쿼리를 입력 하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="791b7-126">The best way to prevent unsupported characters is to just type the query in the keyword box.</span></span> <span data-ttu-id="791b7-127">또는 Word 또는 Excel에서 쿼리를 복사한 다음이를 Microsoft 메모장과 같은 일반 텍스트 편집기의 파일에 붙여 넣을 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="791b7-127">Alternatively, you can copy a query from Word or Excel and then paste it to file in a plain text editor, such as Microsoft Notepad.</span></span> <span data-ttu-id="791b7-128">그런 다음 텍스트 파일을 저장 하 고 **인코딩** 드롭다운 목록에서 **ANSI** 를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="791b7-128">Then save the text file and select **ANSI** in the **Encoding** drop-down list.</span></span> <span data-ttu-id="791b7-129">이렇게 하면 지원 되지 않는 문자나 서식이 모두 제거 됩니다.</span><span class="sxs-lookup"><span data-stu-id="791b7-129">This will remove any formatting and unsupported characters.</span></span> <span data-ttu-id="791b7-130">그런 다음 텍스트 파일의 쿼리를 키워드 쿼리 상자에 복사 하 여 붙여 넣을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="791b7-130">Then you can copy and paste the query from the text file to the keyword query box.</span></span> 
