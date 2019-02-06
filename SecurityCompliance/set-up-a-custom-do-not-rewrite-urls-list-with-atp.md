---
title: Office 365 ATP 안전 링크를 사용 하 여 사용자 지정 안함-되지 않음-재작성 Url 목록 설정
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.audience: Admin
ms.topic: article
ms.date: 02/05/2019
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 35dbfd99-da5a-422b-9b0e-c6caf3b645fa
description: ATP 안전한 링크 정책에를 설정 하는 경우에 do not 재작성을 포함할 수 있습니다 ' 목록에 포함 된 사이트를 방문 하 여 조직에서 일부 사용자를 사용 하도록 설정 하는 Url의 목록입니다.
ms.openlocfilehash: f97abdb0f4e20ed968b4f71761a60cda79658d18
ms.sourcegitcommit: a64af0ebd0b03e4a5e60a33e9108c44c7d74f356
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/05/2019
ms.locfileid: "29741071"
---
# <a name="set-up-a-custom-do-not-rewrite-urls-list-using-office-365-atp-safe-links"></a><span data-ttu-id="1536d-103">Office 365 ATP 안전 링크를 사용 하 여 사용자 지정 안함-되지 않음-재작성 Url 목록 설정</span><span class="sxs-lookup"><span data-stu-id="1536d-103">Set up a custom do-not-rewrite URLs list using Office 365 ATP Safe Links</span></span>

<span data-ttu-id="1536d-p101">[Office 365 고급 위협 보호](office-365-atp.md) ATP ()와 함께 조직을 가질 수 [차단 된 사용자 지정 Url](set-up-a-custom-blocked-urls-list-wtih-atp.md)을 웹에 사람들을 클릭 하는 경우 주소 (Url)는 전자 메일 메시지 또는 특정 Office 문서에는 이러한 Url 하려고에서 수 없습니다. 조직에서 특정 그룹에 대 한 사용자 지정 "rewrite 수행" 목록을 역시 조직입니다. "Rewrite 수행" 목록에는 그렇지 않은 경우 [Office 365의 ATP 안전 링크](atp-safe-links.md)에 의해 차단 되는 Url을 방문 하 여 일부 참가자 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1536d-p101">With [Office 365 Advanced Threat Protection](office-365-atp.md) (ATP), your organization can have a [custom blocked URLs](set-up-a-custom-blocked-urls-list-wtih-atp.md), such that when people click on web addresses (URLs) in email messages or certain Office documents, they are prevented from going to those URLs. Your organization can also have custom "do not rewrite" lists for specific groups in your organization. A "do not rewrite" list enables some people to visit URLs that are otherwise blocked by [ATP Safe Links in Office 365](atp-safe-links.md).</span></span> 
  
<span data-ttu-id="1536d-107">이 문서에서는 ATP 안전 링크를 검색 하 고 몇가지 중요 한 사항을 염두에에서 제외 되는 Url의 목록을 지정 하는 방법에 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="1536d-107">This article describes how to specify a list of URLs that are excluded from ATP Safe Links scanning, and a few important points to keep in mind.</span></span>

## <a name="set-up-a-do-not-rewrite-list"></a><span data-ttu-id="1536d-108">"Rewrite 수행" 목록 설정</span><span class="sxs-lookup"><span data-stu-id="1536d-108">Set up a "do not rewrite" list</span></span>

<span data-ttu-id="1536d-p102">ATP 안전한 링크 보호 조직의 차단된 Url 목록 및 예외에 대 한 "rewrite 수행" 목록을 포함 하 여 여러 목록을 사용 합니다. 필요한 사용 권한이 하는 경우에 "rewrite 수행" 사용자 지정 목록을 설정할 수 있습니다. 이렇게 하려면 추가 하거나 조직에서 특정 받는 사람에 게 적용 되는 안전한 링크 정책을 편집 합니다.</span><span class="sxs-lookup"><span data-stu-id="1536d-p102">ATP Safe Links protection uses several lists, including your organization's blocked URLs list and the "do not rewrite" lists for exceptions. If you have the necessary permissions, you can set up your custom "do not rewrite" lists. You do this when you add or edit Safe Links policies that apply to specific recipients in your organization.</span></span> 

<span data-ttu-id="1536d-112">ATP 정책, 편집 (또는 정의)에 할당 되어 있어야 다음 표에 설명 된 역할 중 하나:</span><span class="sxs-lookup"><span data-stu-id="1536d-112">To edit (or define) ATP policies, you must be assigned one of the roles described in the following table:</span></span>

|<span data-ttu-id="1536d-113">역할</span><span class="sxs-lookup"><span data-stu-id="1536d-113">Role</span></span>  |<span data-ttu-id="1536d-114">Where/방법 할당</span><span class="sxs-lookup"><span data-stu-id="1536d-114">Where/how assigned</span></span>  |
|---------|---------|
|<span data-ttu-id="1536d-115">Office 365 전역 관리자</span><span class="sxs-lookup"><span data-stu-id="1536d-115">Office 365 Global Administrator</span></span> |<span data-ttu-id="1536d-p103">Office 365를 구매 하 여를 로그인 하는 사람 이름은 기본적으로 전역 admin입니다. (자세한 내용은 [Office 365에 대 한 관리자 역할](https://docs.microsoft.com/office365/admin/add-users/about-admin-roles) 참조 하십시오.)</span><span class="sxs-lookup"><span data-stu-id="1536d-p103">The person who signs up to buy Office 365 is a global admin by default. (See [About Office 365 admin roles](https://docs.microsoft.com/office365/admin/add-users/about-admin-roles) to learn more.)</span></span>         |
|<span data-ttu-id="1536d-118">Office 365 보안 관리자</span><span class="sxs-lookup"><span data-stu-id="1536d-118">Office 365 Security Administrator</span></span> |<span data-ttu-id="1536d-119">관리 센터 ([https://aka.ms/admincenter](https://aka.ms/admincenter))</span><span class="sxs-lookup"><span data-stu-id="1536d-119">Admin center ([https://aka.ms/admincenter](https://aka.ms/admincenter))</span></span>|
|<span data-ttu-id="1536d-120">Exchange Online 조직 관리</span><span class="sxs-lookup"><span data-stu-id="1536d-120">Exchange Online Organization Management</span></span> |<span data-ttu-id="1536d-121">Exchange 관리 센터 ([https://outlook.office365.com/ecp](https://outlook.office365.com/ecp))</span><span class="sxs-lookup"><span data-stu-id="1536d-121">Exchange admin center ([https://outlook.office365.com/ecp](https://outlook.office365.com/ecp))</span></span> <br><span data-ttu-id="1536d-122">또는</span><span class="sxs-lookup"><span data-stu-id="1536d-122">or</span></span> <br>  <span data-ttu-id="1536d-123">PowerShell cmdlet (참조 [Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/exchange-online-powershell?view=exchange-ps))</span><span class="sxs-lookup"><span data-stu-id="1536d-123">PowerShell cmdlets (See [Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/exchange-online-powershell?view=exchange-ps))</span></span> |
  
1. <span data-ttu-id="1536d-124">이동 [https://protection.office.com](https://protection.office.com) 와 작업이 나 교육용 계정 사용 하 여 로그인 합니다.</span><span class="sxs-lookup"><span data-stu-id="1536d-124">Go to [https://protection.office.com](https://protection.office.com) and sign in with your work or school account.</span></span> 
    
2. <span data-ttu-id="1536d-125">왼쪽 탐색 영역 **위협 관리** \> **정책** \> **안전 링크**입니다.</span><span class="sxs-lookup"><span data-stu-id="1536d-125">In the left navigation, under **Threat management** \> **Policy** \> **Safe Links**.</span></span>
    
3. <span data-ttu-id="1536d-p104">**특정 받는 사람에 게 적용 되는 정책** 섹션에서 **새로 만들기** 를 선택 (새로 만들기 단추 유사한 더하기 기호 ( **+**)) 새 정책을 만들 수 있습니다. (또는 편집할 수 있습니다 기존 정책을.)</span><span class="sxs-lookup"><span data-stu-id="1536d-p104">In the **Policies that apply to specific recipients** section, choose **New** (the New button resembles a plus sign ( **+**)) to create a new policy. (Alternatively, you can edit an existing policy.)</span></span><br/><span data-ttu-id="1536d-128">![특정 전자 메일 받는 사람에 대 한 안전한 링크 정책을 추가 하려면 새로 만들기를 선택 합니다.](media/01073f42-3cec-4ddb-8c10-4d33ec434676.png)</span><span class="sxs-lookup"><span data-stu-id="1536d-128">![Choose New to add a Safe Links policy for specific email recipients](media/01073f42-3cec-4ddb-8c10-4d33ec434676.png)</span></span>
  
4. <span data-ttu-id="1536d-129">이름 및 사용자 정책에 대 한 설명을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1536d-129">Specify a name and description for your policy.</span></span>
    
5. <span data-ttu-id="1536d-130">**다음 Url 다시 작성 하지 않는** 섹션에서 **유효한 URL 입력** 상자를 선택 하 고 URL을 입력 하 고 더하기 기호 (+)를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="1536d-130">In the **Do not rewrite the following URLs** section, select the **Enter a valid URL** box, and then type a URL, and then choose the plus sign (+).</span></span> 
    
6. <span data-ttu-id="1536d-p105">**적용 된** 섹션에서 **받는 사람이의 구성원은**을 선택 하 고 정책에 포함 하려는 그룹을 선택 합니다. **추가**선택 하 고 **확인**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="1536d-p105">In the **Applied To** section, choose **The recipient is a member of**, and then choose the group(s) you want to include in your policy. Choose **Add**, and then choose **OK**.</span></span>
    
7. <span data-ttu-id="1536d-133">화면 오른쪽 아래 모서리에서 Url을 추가 (영문)이 끝나면 **저장**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="1536d-133">When you are finished adding URLs, in the lower right corner of the screen, choose **Save**.</span></span>
    
> [!NOTE]
> <span data-ttu-id="1536d-p106">차단 된 Url의 경우 조직의 사용자 지정 목록을 검토 했는지 확인 합니다. [ATP 안전 링크를 사용 하 여 차단 된 Url 목록 사용자 지정 설정](set-up-a-custom-blocked-urls-list-wtih-atp.md)을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="1536d-p106">Make sure to review your organization's custom list of blocked URLs. See [Set up a custom blocked URLs list using ATP Safe Links](set-up-a-custom-blocked-urls-list-wtih-atp.md).</span></span> 
  
## <a name="important-points-to-keep-in-mind"></a><span data-ttu-id="1536d-136">중요 한 사항을 염두에</span><span class="sxs-lookup"><span data-stu-id="1536d-136">Important points to keep in mind</span></span>

- <span data-ttu-id="1536d-137">"Rewrite 수행" 목록에서 지정 하는 모든 Url ATP 안전 링크를 지정 하는 받는 사람에 대 한 검사에서 제외 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1536d-137">Any URLs that you specify in the "do not rewrite" list are excluded from ATP Safe Links scanning for the recipients that you specify.</span></span>
 
- <span data-ttu-id="1536d-p107">ATP 안전한 링크 정책에 대 한 "rewrite 수행" 목록을 지정 하면 세 개까지 와일드 카드 별표를 포함할 수 있습니다 (\*). 와일드 카드 (\*)와 같은 항목에 대 한 가정 `contoso.com`는 포함 하지 않으면 명시적으로 접두사 또는 하위 도메인과 같은 `http://` 또는 `https://`합니다. 이 항목을는 같은 의미 `contoso.com` 하는 것과 비슷합니다 `*contoso.com*` 대화 "rewrite 수행" 목록에 대 한 합니다.</span><span class="sxs-lookup"><span data-stu-id="1536d-p107">When you specify a "do not rewrite" list for an ATP Safe Links policy, you can include up to three wildcard asterisks (\*). Wildcards (\*) are assumed for entries such as `contoso.com`, which do not explicitly include prefixes or subdomains, like `http://` or `https://`. This means an entry, such as `contoso.com` is similar to `*contoso.com*` for your "do not rewrite" list.</span></span>

- <span data-ttu-id="1536d-p108">"Rewrite 수행" 목록에 이미 Url의 목록을 하는 경우에 해당 그룹을 검토 하 고 적절 하 게 와일드 카드를 추가 하려면 해야 합니다. 예, 기존 목록에 있는 경우 항목 같은 `http://contoso.com/a` 와 같은 하위 경로 포함 하려는 `http://contoso.com/a/b` 정책에 따라 추가 와일드 카드를 입력 한 항목을 같이 되도록 `http://contoso.com/a*`합니다.</span><span class="sxs-lookup"><span data-stu-id="1536d-p108">If you already have a list of URLs in your "do not rewrite" list, make sure to review that list and add wildcards as appropriate. For example, if your existing list has an entry like `http://contoso.com/a` and you want to include subpaths like `http://contoso.com/a/b` in your policy, add a wildcard to your entry so it looks like `http://contoso.com/a*`.</span></span>
    
- <span data-ttu-id="1536d-p109">"Rewrite 수행" 목록에 지정 하는 Url에 슬래시 (/)를 포함 하지 마십시오. 예를 입력 하지 않고 `contoso.com/` 대화 "rewrite 수행" 목록에 입력 `contoso.com`합니다.</span><span class="sxs-lookup"><span data-stu-id="1536d-p109">Do not include a forward slash (/) in the URLs that you specify in your "do not rewrite" list. For example, rather than enter `contoso.com/` in your "do not rewrite" list, enter `contoso.com`.</span></span>
    
<span data-ttu-id="1536d-145">다음 표에서 목록 예제 입력할 수 및 이러한 항목이 어떤 영향 수 있으며</span><span class="sxs-lookup"><span data-stu-id="1536d-145">The following table lists examples of what you can enter and what effect those entries have.</span></span>
    
|<span data-ttu-id="1536d-146">**예제 항목**</span><span class="sxs-lookup"><span data-stu-id="1536d-146">**Example Entry**</span></span>|<span data-ttu-id="1536d-147">**기능**</span><span class="sxs-lookup"><span data-stu-id="1536d-147">**What It Does**</span></span>|
|:-----|:-----|
|`*contoso.com*`  <br/> |<span data-ttu-id="1536d-148">같은 도메인, 하위 도메인, 및 경로 방문 하 여 특정 수신자에 게 허용 `http://www.contoso.com`, `https://www.contoso.com`, `https://maps.contoso.com`, 또는`http://www.contoso.com/a`</span><span class="sxs-lookup"><span data-stu-id="1536d-148">Allows specific recipients to visit a domain, subdomains, and paths, such as `http://www.contoso.com`, `https://www.contoso.com`, `https://maps.contoso.com`, or `http://www.contoso.com/a`</span></span>  <br/> |
|`http://contoso.com/a`  <br/> |<span data-ttu-id="1536d-149">같은 사이트를 방문 하 여 특정 수신자에 게 허용 `http://contoso.com/a`, 하위 경로 하지 않지만`http://contoso.com/a/b`</span><span class="sxs-lookup"><span data-stu-id="1536d-149">Allows specific recipients to visit a site like `http://contoso.com/a`, but not subpaths like `http://contoso.com/a/b`</span></span>  <br/> |
|`http://contoso.com/a*`  <br/> |<span data-ttu-id="1536d-150">같은 사이트를 방문 하 여 특정 수신자에 게 허용 `http://contoso.com/a` 하위 경로 같은 및`http://contoso.com/a/b`</span><span class="sxs-lookup"><span data-stu-id="1536d-150">Allows specific recipients to visit a site like `http://contoso.com/a` and subpaths like `http://contoso.com/a/b`</span></span>  <br/> |
   
 