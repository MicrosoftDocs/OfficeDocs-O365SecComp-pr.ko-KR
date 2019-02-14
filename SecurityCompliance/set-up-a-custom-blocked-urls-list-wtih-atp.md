---
title: Office 365 ATP 안전 링크를 사용 하 여 차단 된 Url 목록 사용자 지정 설정
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.audience: Admin
ms.topic: article
ms.date: 02/06/2019
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 896a7efb-1683-465e-a394-261349e5d866
ms.collection: M365-security-compliance
description: Office 365 고급 위협 보호를 사용 하 여 조직에 대 한 차단 된 Url의 목록을 설정 하는 방법에 알아봅니다. 차단 된 Url ATP 안전한 링크 정책에 따라 Office 문서 및 전자 메일 메시지에 적용 됩니다.
ms.openlocfilehash: 261d85ce72de3a19ed4c2327d56fe1f32107781b
ms.sourcegitcommit: efccf5b4f22d34a9674bc55ebf3d88bc8bda2972
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/14/2019
ms.locfileid: "29995319"
---
# <a name="set-up-a-custom-blocked-urls-list-using-office-365-atp-safe-links"></a><span data-ttu-id="2e19d-104">Office 365 ATP 안전 링크를 사용 하 여 차단 된 Url 목록 사용자 지정 설정</span><span class="sxs-lookup"><span data-stu-id="2e19d-104">Set up a custom blocked URLs list using Office 365 ATP Safe Links</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2e19d-p102">이 문서는 기업 고객을 위한 것입니다. Outlook에서 안전한 링크에 대 한 정보에 대 한 자세한 내용은 홈 사용자 인 경우 [Outlook.com 고급 보안](https://support.office.com/article/advanced-outlook-com-security-for-office-365-subscribers-882d2243-eab9-4545-a58a-b36fee4a46e2)을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="2e19d-p102">This article is intended for business customers. If you are a home user looking for information about Safe Links in Outlook, see [Advanced Outlook.com security](https://support.office.com/article/advanced-outlook-com-security-for-office-365-subscribers-882d2243-eab9-4545-a58a-b36fee4a46e2).</span></span>

<span data-ttu-id="2e19d-p103">[Office 365 고급 위협 보호](office-365-atp.md) ATP (), 조직 웹사이트 주소 (Url) 차단 되는 사용자 지정 목록을 할 수 있습니다. URL을 차단 되 면 차단 된 URL에 대 한 링크를 클릭 하는 사람 된 다음 이미지 유사한 [경고 페이지](atp-safe-links-warning-pages.md) 로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="2e19d-p103">With [Office 365 Advanced Threat Protection](office-365-atp.md) (ATP), your organization can have a custom list of website addresses (URLs) that are blocked. When a URL is blocked, people who click on links to the blocked URL are taken to a [warning page](atp-safe-links-warning-pages.md) that resembles the following image:</span></span> 
  
![이 사이트는 차단](media/6b4bda2d-a1e6-419e-8b10-588e83c3af3f.png)
  
<span data-ttu-id="2e19d-110">차단 된 Url 목록 조직의 Office 365 보안 팀에 의해 정의 된 하 고 해당 목록은 Office 365 ATP 안전한 링크 정책에 포함 되는 사용자 조직에서 모든 사용자에 게 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="2e19d-110">The blocked URLs list is defined by your organization's Office 365 security team, and that list applies to everyone in the organization who is covered by Office 365 ATP Safe Links policies.</span></span> 
  
<span data-ttu-id="2e19d-111">[Office 365의 ATP 안전 링크](atp-safe-links.md)에 대 한 조직의 사용자 지정 차단된 Url 목록을 설정 하는 방법은이 문서를 읽어보십시오.</span><span class="sxs-lookup"><span data-stu-id="2e19d-111">Read this article to learn how to set up your organization's custom blocked URLs list for [ATP Safe Links in Office 365](atp-safe-links.md).</span></span>
  
## <a name="view-or-edit-a-custom-list-of-blocked-urls"></a><span data-ttu-id="2e19d-112">차단 된 Url의 사용자 지정 목록을 편집 또는 보기</span><span class="sxs-lookup"><span data-stu-id="2e19d-112">View or edit a custom list of blocked URLs</span></span>

<span data-ttu-id="2e19d-p104">[Office 365의 ATP 안전한 링크](atp-safe-links.md) 여러 목록, 조직의 사용자 지정 차단된 Url 목록 포함을 사용 합니다. 필요한 사용 권한이 하는 경우에 조직의 사용자 지정 목록을 설정할 수 있습니다. 조직의 기본 안전한 링크 정책을 편집 하 여이 작업을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="2e19d-p104">[ATP Safe Links in Office 365](atp-safe-links.md) uses several lists, including your organization's custom blocked URLs list. If you have the necessary permissions, you can set up your organization's custom list. You do this by editing your organization's default Safe Links policy.</span></span>

<span data-ttu-id="2e19d-116">ATP 정책, 편집 (또는 정의)에 할당 되어 있어야 다음 표에 설명 된 역할 중 하나:</span><span class="sxs-lookup"><span data-stu-id="2e19d-116">To edit (or define) ATP policies, you must be assigned one of the roles described in the following table:</span></span> 

|<span data-ttu-id="2e19d-117">역할</span><span class="sxs-lookup"><span data-stu-id="2e19d-117">Role</span></span>  |<span data-ttu-id="2e19d-118">Where/방법 할당</span><span class="sxs-lookup"><span data-stu-id="2e19d-118">Where/how assigned</span></span>  |
|---------|---------|
|<span data-ttu-id="2e19d-119">Office 365 전역 관리자</span><span class="sxs-lookup"><span data-stu-id="2e19d-119">Office 365 Global Administrator</span></span> |<span data-ttu-id="2e19d-p105">Office 365를 구매 하 여를 로그인 하는 사람 이름은 기본적으로 전역 admin입니다. (자세한 내용은 [Office 365에 대 한 관리자 역할](https://docs.microsoft.com/office365/admin/add-users/about-admin-roles) 참조 하십시오.)</span><span class="sxs-lookup"><span data-stu-id="2e19d-p105">The person who signs up to buy Office 365 is a global admin by default. (See [About Office 365 admin roles](https://docs.microsoft.com/office365/admin/add-users/about-admin-roles) to learn more.)</span></span>         |
|<span data-ttu-id="2e19d-122">보안 관리자</span><span class="sxs-lookup"><span data-stu-id="2e19d-122">Security Administrator</span></span> |<span data-ttu-id="2e19d-123">Azure Active Directory 관리 센터 ([https://aad.portal.azure.com](https://aad.portal.azure.com))</span><span class="sxs-lookup"><span data-stu-id="2e19d-123">Azure Active Directory admin center ([https://aad.portal.azure.com](https://aad.portal.azure.com))</span></span>|
|<span data-ttu-id="2e19d-124">Exchange Online 조직 관리</span><span class="sxs-lookup"><span data-stu-id="2e19d-124">Exchange Online Organization Management</span></span> |<span data-ttu-id="2e19d-125">Exchange 관리 센터 ([https://outlook.office365.com/ecp](https://outlook.office365.com/ecp))</span><span class="sxs-lookup"><span data-stu-id="2e19d-125">Exchange admin center ([https://outlook.office365.com/ecp](https://outlook.office365.com/ecp))</span></span> <br><span data-ttu-id="2e19d-126">또는</span><span class="sxs-lookup"><span data-stu-id="2e19d-126">or</span></span> <br>  <span data-ttu-id="2e19d-127">PowerShell cmdlet (참조 [Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/exchange-online-powershell?view=exchange-ps))</span><span class="sxs-lookup"><span data-stu-id="2e19d-127">PowerShell cmdlets (See [Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/exchange-online-powershell?view=exchange-ps))</span></span> |

> [!TIP]
> <span data-ttu-id="2e19d-128">역할 및 사용 권한 하는 방법에 대 한 자세한 내용은 참조 [Office 365 보안에 대 한 사용 권한을 &amp; 준수 센터](permissions-in-the-security-and-compliance-center.md)합니다.</span><span class="sxs-lookup"><span data-stu-id="2e19d-128">To learn more about roles and permissions, see [Permissions in the Office 365 Security &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md).</span></span>

### <a name="to-view-or-edit-a-custom-blocked-urls-list"></a><span data-ttu-id="2e19d-129">차단 된 Url 목록 보기 또는 사용자 지정을 편집 하려면</span><span class="sxs-lookup"><span data-stu-id="2e19d-129">To view or edit a custom blocked URLs list</span></span>
  
1. <span data-ttu-id="2e19d-130">이동 [https://protection.office.com](https://protection.office.com) 와 작업이 나 교육용 계정 사용 하 여 로그인 합니다.</span><span class="sxs-lookup"><span data-stu-id="2e19d-130">Go to [https://protection.office.com](https://protection.office.com) and sign in with your work or school account.</span></span> 
    
2. <span data-ttu-id="2e19d-131">왼쪽 탐색 영역 **위협 관리**, **정책** 선택 \> **안전 링크**입니다.</span><span class="sxs-lookup"><span data-stu-id="2e19d-131">In the left navigation, under **Threat management**, choose **Policy** \> **Safe Links**.</span></span>
    
3. <span data-ttu-id="2e19d-132">**조직 전체에 적용 되는 정책** 섹션에서 **기본**을 선택 하 고 **편집** (편집 단추는 연필 유사)를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="2e19d-132">In the **Policies that apply to the entire organization** section, select **Default**, and then choose **Edit** (the Edit button resembles a pencil).</span></span><br/><span data-ttu-id="2e19d-133">![안전한 링크 보호에 대 한 기본 정책을 편집 하려면 편집을 클릭 합니다.](media/d08f9615-d947-4033-813a-d310ec2c8cca.png)</span><span class="sxs-lookup"><span data-stu-id="2e19d-133">![Click Edit to edit your default policy for Safe Links protection](media/d08f9615-d947-4033-813a-d310ec2c8cca.png)</span></span><br/><span data-ttu-id="2e19d-p106">이 옵션을 사용 하면 차단 된 Url의 목록을 볼 수 있습니다. 처음에 어떤 Url도 여기에 나열 된 없을 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2e19d-p106">This enables you to view your list of blocked URLs. At first, you might not have any URLs listed here.</span></span><br/><span data-ttu-id="2e19d-136">![차단 되는 기본 안전한 링크 정책에서 Url 목록](media/575e1449-6191-40ac-b626-030a2fd3fb11.png)</span><span class="sxs-lookup"><span data-stu-id="2e19d-136">![Blocked URLs list in the default Safe Links policy](media/575e1449-6191-40ac-b626-030a2fd3fb11.png)</span></span>
  
4. <span data-ttu-id="2e19d-137">선택 **유효한 URL 입력** 상자에 URL을 입력 하 고 더하기 기호를 선택 합니다 (**+**).</span><span class="sxs-lookup"><span data-stu-id="2e19d-137">Select the **Enter a valid URL** box, type a URL, and then choose the plus sign (**+**).</span></span> 

5. <span data-ttu-id="2e19d-138">화면 오른쪽 아래 모서리에서 Url을 추가 (영문)이 끝나면 **저장**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="2e19d-138">When you are finished adding URLs, in the lower right corner of the screen, choose **Save**.</span></span>
    
## <a name="a-few-things-to-keep-in-mind"></a><span data-ttu-id="2e19d-139">주의 해야할 사항</span><span class="sxs-lookup"><span data-stu-id="2e19d-139">A few things to keep in mind</span></span>

<span data-ttu-id="2e19d-140">대화 목록에 Url을 추가 하는 동안 다음과 같은 사항을 사항에 유의 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="2e19d-140">While you add URLs to your list, keep the following points in mind:</span></span> 

- <span data-ttu-id="2e19d-p107">슬래시를 포함 하지 마십시오 ( **/**) URL의 끝에 있습니다. 입력 하는 대신 등 `http://www.contoso.com/`, 입력 `http://www.contoso.com`합니다.</span><span class="sxs-lookup"><span data-stu-id="2e19d-p107">Do not include a forward slash ( **/**) at the end of the URL. For example, instead of entering `http://www.contoso.com/`, enter `http://www.contoso.com`.</span></span>
    
- <span data-ttu-id="2e19d-p108">한 도메인에만 나타나는 URL을 지정할 수 있습니다 (같은 `contoso.com` 또는 `tailspintoys.com`). 이것은 클릭 차단 도메인을 포함 하는 모든 URL에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2e19d-p108">You can specify a domain-only URL (like `contoso.com` or `tailspintoys.com`). This will block clicks on any URL that contains the domain.</span></span>

- <span data-ttu-id="2e19d-p109">하위 도메인을 지정할 수 있습니다 (같은 `toys.contoso.com*`) 전체 도메인을 차단 하지 않고 (같은 `contoso.com`). 이는 블록의 하위 도메인이 포함 하는 모든 URL 하지만 클릭을 차단 되지 않습니다 전체 도메인을 포함 하는 url입니다.</span><span class="sxs-lookup"><span data-stu-id="2e19d-p109">You can specify a subdomain (like `toys.contoso.com*`) without blocking a full domain (like `contoso.com`). This will block clicks any URL that contains the subdomain, but it won't block clicks to a URL that contains the full domain.</span></span>  
    
- <span data-ttu-id="2e19d-p110">세 개까지 와일드 카드 별표를 포함할 수 있습니다 (\*) URL 당 합니다. 입력할 수 및 이러한 항목이 어떤 영향에 대 한 예가 다음 표에 나와 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2e19d-p110">You can include up to three wildcard asterisks (\*) per URL. The following table lists some examples of what you can enter and what effect those entries have.</span></span>
    
|<span data-ttu-id="2e19d-149">**예제 항목**</span><span class="sxs-lookup"><span data-stu-id="2e19d-149">**Example Entry**</span></span>|<span data-ttu-id="2e19d-150">**기능**</span><span class="sxs-lookup"><span data-stu-id="2e19d-150">**What It Does**</span></span>|
|:-----|:-----|
|<span data-ttu-id="2e19d-151">`contoso.com`또는`*contoso.com*`</span><span class="sxs-lookup"><span data-stu-id="2e19d-151">`contoso.com` or `*contoso.com*`</span></span>  <br/> |<span data-ttu-id="2e19d-152">도메인, 하위 도메인, 및 경로 같은 차단 `https://www.contoso.com`, `http://sub.contoso.com`, 및`http://contoso.com/abc`</span><span class="sxs-lookup"><span data-stu-id="2e19d-152">Blocks the domain, subdomains, and paths, such as `https://www.contoso.com`, `http://sub.contoso.com`, and `http://contoso.com/abc`</span></span>  <br/> |
|`http://contoso.com/a`  <br/> |<span data-ttu-id="2e19d-153">사이트를 차단 `http://contoso.com/a` 이지만 하지 추가 하위 경로`http://contoso.com/a/b`</span><span class="sxs-lookup"><span data-stu-id="2e19d-153">Blocks a site `http://contoso.com/a` but not additional subpaths like `http://contoso.com/a/b`</span></span>  <br/> |
|`http://contoso.com/a*`  <br/> |<span data-ttu-id="2e19d-154">사이트를 차단 `http://contoso.com/a` 추가 하위 경로 같은 및`http://contoso.com/a/b`</span><span class="sxs-lookup"><span data-stu-id="2e19d-154">Blocks a site `http://contoso.com/a` and additional subpaths like `http://contoso.com/a/b`</span></span>  <br/> |
|`http://toys.contoso.com*`  <br/> |<span data-ttu-id="2e19d-155">하위 도메인 (이 경우 "상사")를 차단 하지만 다른 도메인 Url 클릭을 허용 (같은 `http://contoso.com` 또는 `http://home.contoso.com`).</span><span class="sxs-lookup"><span data-stu-id="2e19d-155">Blocks a subdomain ("toys" in this case) but allow clicks to other domain URLs (like `http://contoso.com` or `http://home.contoso.com`).</span></span>  <br/> |
   

## <a name="how-to-define-exceptions-for-certain-users-in-an-organization"></a><span data-ttu-id="2e19d-156">조직에서 특정 사용자에 대 한 예외를 정의 하는 방법</span><span class="sxs-lookup"><span data-stu-id="2e19d-156">How to define exceptions for certain users in an organization</span></span>

<span data-ttu-id="2e19d-p111">다른 사용자에 대 한 차단 되었을 수 있는 Url을 볼 수 있도록 특정 그룹을 하려는 경우에 특정 받는 사람에 게 적용 되는 ATP 안전한 링크 정책을 지정할 수 있습니다. [ATP 안전 링크를 사용 하는 사용자 지정 "rewrite 수행" Url 목록 설정](set-up-a-custom-do-not-rewrite-urls-list-with-atp.md)을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="2e19d-p111">If you want certain groups to be able to view URLs that might be blocked for others, you can specify an ATP Safe Links policy that applies to specific recipients. See [Set up a custom "do not rewrite" URLs list using ATP Safe Links](set-up-a-custom-do-not-rewrite-urls-list-with-atp.md).</span></span>
  

