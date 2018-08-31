---
title: Office 365 ATP 안전 링크를 사용 하 여 차단 된 Url 목록 사용자 지정 설정
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 5/30/2018
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 896a7efb-1683-465e-a394-261349e5d866
description: Office 365 고급 위협 보호를 사용 하 여 조직에 대 한 차단 된 Url의 목록을 설정 하는 방법을 알아보려면이 문서를 읽어보십시오. 차단 된 Url ATP 안전한 링크 정책에 따라 Office 문서 및 전자 메일 메시지에 적용 됩니다.
ms.openlocfilehash: cd1e7858c8929bf468b2a4d5e09ccde9d5adc7b1
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22533542"
---
# <a name="set-up-a-custom-blocked-urls-list-using-office-365-atp-safe-links"></a><span data-ttu-id="f8823-104">Office 365 ATP 안전 링크를 사용 하 여 차단 된 Url 목록 사용자 지정 설정</span><span class="sxs-lookup"><span data-stu-id="f8823-104">Set up a custom blocked URLs list using Office 365 ATP Safe Links</span></span>

<span data-ttu-id="f8823-p102">[Office 365 고급 위협 보호](office-365-atp.md) ATP (), 조직 웹사이트 주소 (Url) 차단 되는 사용자 지정 목록을 할 수 있습니다. URL을 차단 되 면 차단 된 URL에 대 한 링크를 클릭 하는 사람 된 다음 이미지 유사한 [경고 페이지](atp-safe-links-warning-pages.md) 로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="f8823-p102">With [Office 365 Advanced Threat Protection](office-365-atp.md) (ATP), your organization can have a custom list of website addresses (URLs) that are blocked. When a URL is blocked, people who click on links to the blocked URL are taken to a [warning page](atp-safe-links-warning-pages.md) that resembles the following image:</span></span> 
  
![이 사이트는 차단](media/6b4bda2d-a1e6-419e-8b10-588e83c3af3f.png)
  
<span data-ttu-id="f8823-108">차단 된 Url 목록 조직의 Office 365 보안 팀에 의해 정의 된 하 고 해당 목록은 Office 365 ATP 안전한 링크 정책에 포함 되는 사용자 조직에서 모든 사용자에 게 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f8823-108">The blocked URLs list is defined by your organization's Office 365 security team, and that list applies to everyone in the organization who is covered by Office 365 ATP Safe Links policies.</span></span> 
  
<span data-ttu-id="f8823-109">[Office 365의 ATP 안전 링크](atp-safe-links.md)에 대 한 조직의 사용자 지정 차단된 Url 목록을 설정 하는 방법은이 문서를 읽어보십시오.</span><span class="sxs-lookup"><span data-stu-id="f8823-109">Read this article to learn how to set up your organization's custom blocked URLs list for [ATP Safe Links in Office 365](atp-safe-links.md).</span></span>
  
## <a name="view-or-edit-a-custom-list-of-blocked-urls"></a><span data-ttu-id="f8823-110">차단 된 Url의 사용자 지정 목록을 편집 또는 보기</span><span class="sxs-lookup"><span data-stu-id="f8823-110">View or edit a custom list of blocked URLs</span></span>

<span data-ttu-id="f8823-p103">[Office 365의 ATP 안전한 링크](atp-safe-links.md) 여러 목록, 조직의 사용자 지정 차단된 Url 목록 포함을 사용 합니다. 필요한 사용 권한이 하는 경우에 조직의 사용자 지정 목록을 설정할 수 있습니다. 조직의 기본 안전한 링크 정책을 편집 하 여이 작업을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="f8823-p103">[ATP Safe Links in Office 365](atp-safe-links.md) uses several lists, including your organization's custom blocked URLs list. If you have the necessary permissions, you can set up your organization's custom list. You do this by editing your organization's default Safe Links policy.</span></span>
  
1. <span data-ttu-id="f8823-114">이동 [https://protection.office.com](https://protection.office.com) 와 작업이 나 교육용 계정 사용 하 여 로그인 합니다.</span><span class="sxs-lookup"><span data-stu-id="f8823-114">Go to [https://protection.office.com](https://protection.office.com) and sign in with your work or school account.</span></span> 
    
2. <span data-ttu-id="f8823-115">왼쪽 탐색 영역 **위협 관리**, **정책** 선택 \> **안전 링크**입니다.</span><span class="sxs-lookup"><span data-stu-id="f8823-115">In the left navigation, under **Threat management**, choose **Policy** \> **Safe Links**.</span></span>
    
3. <span data-ttu-id="f8823-116">**조직 전체에 적용 되는 정책** 섹션에서 **기본**을 선택 하 고 **편집** (편집 단추는 연필 유사)를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="f8823-116">In the **Policies that apply to the entire organization** section, select **Default**, and then choose **Edit** (the Edit button resembles a pencil).</span></span> 
    
    ![안전한 링크 보호에 대 한 기본 정책을 편집 하려면 편집을 클릭 합니다.](media/d08f9615-d947-4033-813a-d310ec2c8cca.png)
  
    <span data-ttu-id="f8823-p104">차단 된 Url의 목록을 보려면 이동 하는 위치입니다. 참고를 처음에 나열 된 모든 Url이 없습니다.</span><span class="sxs-lookup"><span data-stu-id="f8823-p104">This is where you go to view your list of blocked URLs. Note that at first, you won't have any URLs listed.</span></span>
    
    ![차단 되는 Url 목록 조직 전체에 적용 되는 안전한 링크 정책 기본에서입니다.](media/575e1449-6191-40ac-b626-030a2fd3fb11.png)
  
4. <span data-ttu-id="f8823-p105">**유효한 URL 입력** 상자를 선택 하 고 URL을 입력 하 고 더하기 기호 (+)를 선택 합니다. 다음은 사항에 유의 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="f8823-p105">Select the **Enter a valid URL** box, and then type a URL, and then choose the plus sign (+). Here are a few things to keep in mind:</span></span> 
    
  - <span data-ttu-id="f8823-p106">한 도메인에만 나타나는 URL을 지정할 수 있습니다 (같은 `contoso.com` 또는 `tailspintoys.com`). 이것은 클릭 차단 도메인을 포함 하는 모든 URL에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f8823-p106">You can specify a domain-only URL (like `contoso.com` or `tailspintoys.com`). This will block clicks on any URL that contains the domain.</span></span>
    
  - <span data-ttu-id="f8823-p107">슬래시를 포함 하지 마십시오 ( **/**) URL의 끝에 있습니다. 입력 하는 대신 등 `http://www.contoso.com/`, 입력 `http://www.contoso.com`합니다.</span><span class="sxs-lookup"><span data-stu-id="f8823-p107">Do not include a forward slash ( **/**) at the end of the URL. For example, instead of entering `http://www.contoso.com/`, enter `http://www.contoso.com`.</span></span>
    
  - <span data-ttu-id="f8823-p108">세 개까지 와일드 카드 별표를 포함할 수 있습니다 (\*) URL 당 합니다. 입력할 수 및 이러한 항목이 어떤 영향에 대 한 예가 다음 표에 나와 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f8823-p108">You can include up to three wildcard asterisks (\*) per URL. The following table lists some examples of what you can enter and what effect those entries have.</span></span>
    
|<span data-ttu-id="f8823-129">**예제 항목**</span><span class="sxs-lookup"><span data-stu-id="f8823-129">**Example Entry**</span></span>|<span data-ttu-id="f8823-130">**기능**</span><span class="sxs-lookup"><span data-stu-id="f8823-130">**What It Does**</span></span>|
|:-----|:-----|
|<span data-ttu-id="f8823-131">`contoso.com`또는`\*contoso.com\*`</span><span class="sxs-lookup"><span data-stu-id="f8823-131">`contoso.com` or `\*contoso.com\*`</span></span>  <br/> |<span data-ttu-id="f8823-132">도메인, 하위 도메인, 및 경로 같은 차단 `https://www.contoso.com`, `http://sub.contoso.com`, 및`http://contoso.com/abc`</span><span class="sxs-lookup"><span data-stu-id="f8823-132">Blocks the domain, subdomains, and paths, such as `https://www.contoso.com`, `http://sub.contoso.com`, and `http://contoso.com/abc`</span></span>  <br/> |
|`http://contoso.com/a`  <br/> |<span data-ttu-id="f8823-133">사이트를 차단 `http://contoso.com/a` 이지만 하지 추가 하위 경로`http://contoso.com/a/b`</span><span class="sxs-lookup"><span data-stu-id="f8823-133">Blocks a site `http://contoso.com/a` but not additional subpaths like `http://contoso.com/a/b`</span></span>  <br/> |
|`http://contoso.com/a\*`  <br/> |<span data-ttu-id="f8823-134">사이트를 차단 `http://contoso.com/a` 추가 하위 경로 같은 및`http://contoso.com/a/b`</span><span class="sxs-lookup"><span data-stu-id="f8823-134">Blocks a site `http://contoso.com/a` and additional subpaths like `http://contoso.com/a/b`</span></span>  <br/> |
   
5. <span data-ttu-id="f8823-135">화면 오른쪽 아래 모서리에서 Url을 추가 (영문)이 끝나면 **저장**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="f8823-135">When you are finished adding URLs, in the lower right corner of the screen, choose **Save**.</span></span>
    
## <a name="what-if-i-want-to-define-exceptions-for-certain-users-in-my-organization"></a><span data-ttu-id="f8823-136">조직 내에서 특정 사용자에 대 한 예외를 정의 하려면 어떻게 해야 합니까?</span><span class="sxs-lookup"><span data-stu-id="f8823-136">What if I want to define exceptions for certain users in my organization?</span></span>

<span data-ttu-id="f8823-p109">다른 사용자에 대 한 차단 되었을 수 있는 Url을 볼 수 있도록 특정 그룹을 하려는 경우에 특정 받는 사람에 게 적용 되는 ATP 안전한 링크 정책을 지정할 수 있습니다. [ATP 안전 링크를 사용 하는 사용자 지정 "rewrite 수행" Url 목록 설정](set-up-a-custom-do-not-rewrite-urls-list-with-atp.md)을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="f8823-p109">If you want certain groups to be able to view URLs that might be blocked for others, you can specify an ATP Safe Links policy that applies to specific recipients. See [Set up a custom "do not rewrite" URLs list using ATP Safe Links](set-up-a-custom-do-not-rewrite-urls-list-with-atp.md).</span></span>
  
## <a name="related-topics"></a><span data-ttu-id="f8823-139">관련 항목</span><span class="sxs-lookup"><span data-stu-id="f8823-139">Related topics</span></span>

[<span data-ttu-id="f8823-140">Office 365 Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="f8823-140">Office 365 Advanced Threat Protection</span></span>](office-365-atp.md)
  
[<span data-ttu-id="f8823-141">Office 365의에서 ATP 안전 하 게 보호 링크</span><span class="sxs-lookup"><span data-stu-id="f8823-141">ATP Safe Links in Office 365</span></span>](atp-safe-links.md)
  
[<span data-ttu-id="f8823-142">Office 365의 ATP 안전한 링크 정책 설정</span><span class="sxs-lookup"><span data-stu-id="f8823-142">Set up ATP Safe Links policies in Office 365</span></span>](set-up-atp-safe-links-policies.md)
  
[<span data-ttu-id="f8823-143">Office 365의에서 ATP 안전 하 게 보호 첨부 파일</span><span class="sxs-lookup"><span data-stu-id="f8823-143">ATP Safe Attachments in Office 365</span></span>](atp-safe-attachments.md)

[<span data-ttu-id="f8823-144">Office 365 보안에 대 한 사용 권한을 &amp; 준수 센터</span><span class="sxs-lookup"><span data-stu-id="f8823-144">Permissions in the Office 365 Security &amp; Compliance Center</span></span>](permissions-in-the-security-and-compliance-center.md)
  

