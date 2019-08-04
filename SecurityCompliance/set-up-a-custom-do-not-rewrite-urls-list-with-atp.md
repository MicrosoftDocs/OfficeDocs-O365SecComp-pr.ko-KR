---
title: Office 365 ATP 안전한 링크를 사용 하 여 사용자 지정 하 여 재작성 되지 않는 Url 목록 설정
ms.author: deniseb
author: denisebmsft
manager: dansimp
audience: Admin
ms.topic: article
ms.date: 02/06/2019
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 35dbfd99-da5a-422b-9b0e-c6caf3b645fa
ms.collection:
- M365-security-compliance
description: ATP 안전한 링크 정책을 설정 하는 경우 조직의 일부 사용자가 목록에 포함 된 사이트를 방문할 수 있도록 하기 위해 다음 Url 목록을 포함 하 여이를 재작성 합니다.
ms.openlocfilehash: 88a3f816c9156abc2d910d8710296e471e2fc540
ms.sourcegitcommit: 32ecff689ae32c59a39b7633ca0f36a304e7516e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/09/2019
ms.locfileid: "35601365"
---
# <a name="set-up-a-custom-do-not-rewrite-urls-list-using-office-365-atp-safe-links"></a><span data-ttu-id="cf01e-103">Office 365 ATP 안전한 링크를 사용 하 여 사용자 지정 하 여 재작성 되지 않는 Url 목록 설정</span><span class="sxs-lookup"><span data-stu-id="cf01e-103">Set up a custom do-not-rewrite URLs list using Office 365 ATP Safe Links</span></span>

> [!IMPORTANT]
> <span data-ttu-id="cf01e-104">이 문서는 [Office 365 Advanced Threat Protection](office-365-atp.md)을 사용 하는 비즈니스 고객을 위한 것입니다.</span><span class="sxs-lookup"><span data-stu-id="cf01e-104">This article is intended for business customers who have [Office 365 Advanced Threat Protection](office-365-atp.md).</span></span> <span data-ttu-id="cf01e-105">Outlook의 안전한 링크에 대 한 정보를 검색 하는 개인 사용자는 [Advanced Outlook.com security](https://support.office.com/article/advanced-outlook-com-security-for-office-365-subscribers-882d2243-eab9-4545-a58a-b36fee4a46e2)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="cf01e-105">If you are a home user looking for information about Safe Links in Outlook, see [Advanced Outlook.com security](https://support.office.com/article/advanced-outlook-com-security-for-office-365-subscribers-882d2243-eab9-4545-a58a-b36fee4a46e2).</span></span>

<span data-ttu-id="cf01e-106">[Office 365 ATP (Advanced Threat Protection](office-365-atp.md) )를 사용 하는 경우 조직에 [사용자 지정 차단 된 url](set-up-a-custom-blocked-urls-list-wtih-atp.md)이 있을 수 있으며, 사용자가 전자 메일 메시지 또는 특정 Office 문서에서 웹 주소 (url)를 클릭할 때 이러한 url로 이동 하는 것이 방지 됩니다.</span><span class="sxs-lookup"><span data-stu-id="cf01e-106">With [Office 365 Advanced Threat Protection](office-365-atp.md) (ATP), your organization can have a [custom blocked URLs](set-up-a-custom-blocked-urls-list-wtih-atp.md), such that when people click on web addresses (URLs) in email messages or certain Office documents, they are prevented from going to those URLs.</span></span> <span data-ttu-id="cf01e-107">조직에서 조직의 특정 그룹에 대해 사용자 지정 "다시 쓰지 않음" 목록을 사용할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cf01e-107">Your organization can also have custom "do not rewrite" lists for specific groups in your organization.</span></span> <span data-ttu-id="cf01e-108">"다시 쓰지 않음" 목록을 사용 하면 일부 사용자가 [Office 365의 ATP 안전한 링크](atp-safe-links.md)에 의해 차단 되는 url을 방문할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cf01e-108">A "do not rewrite" list enables some people to visit URLs that are otherwise blocked by [ATP Safe Links in Office 365](atp-safe-links.md).</span></span> 
  
<span data-ttu-id="cf01e-109">이 문서에서는 ATP 안전한 링크 검색에서 제외 되는 Url 목록과 몇 가지 중요 한 사항을 염두에 두고 있는지를 지정 하는 방법에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf01e-109">This article describes how to specify a list of URLs that are excluded from ATP Safe Links scanning, and a few important points to keep in mind.</span></span>

## <a name="set-up-a-do-not-rewrite-list"></a><span data-ttu-id="cf01e-110">"다시 쓰지 않음" 목록 설정</span><span class="sxs-lookup"><span data-stu-id="cf01e-110">Set up a "do not rewrite" list</span></span>

<span data-ttu-id="cf01e-111">ATP 안전한 링크 보호에서는 조직의 차단 된 Url 목록과 "다시 쓰지 않음" 목록 등 여러 목록을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf01e-111">ATP Safe Links protection uses several lists, including your organization's blocked URLs list and the "do not rewrite" lists for exceptions.</span></span> <span data-ttu-id="cf01e-112">필요한 사용 권한이 있는 경우 사용자 지정 "다시 쓰지 않음" 목록을 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cf01e-112">If you have the necessary permissions, you can set up your custom "do not rewrite" lists.</span></span> <span data-ttu-id="cf01e-113">조직의 특정 받는 사람에 게 적용 되는 안전 링크 정책을 추가 하거나 편집할 때이 작업을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf01e-113">You do this when you add or edit Safe Links policies that apply to specific recipients in your organization.</span></span> 

<span data-ttu-id="cf01e-114">ATP 정책을 편집 하거나 정의 하려면 다음 표에 설명 된 역할 중 하나를 할당 받아야 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf01e-114">To edit (or define) ATP policies, you must be assigned one of the roles described in the following table:</span></span>

|<span data-ttu-id="cf01e-115">역할</span><span class="sxs-lookup"><span data-stu-id="cf01e-115">Role</span></span>  |<span data-ttu-id="cf01e-116">할당 된 위치/방법</span><span class="sxs-lookup"><span data-stu-id="cf01e-116">Where/how assigned</span></span>  |
|---------|---------|
|<span data-ttu-id="cf01e-117">Office 365 전역 관리자</span><span class="sxs-lookup"><span data-stu-id="cf01e-117">Office 365 Global Administrator</span></span> |<span data-ttu-id="cf01e-118">Office 365을 구매 하기 위해 등록 하는 사람은 기본적으로 전역 관리자입니다.</span><span class="sxs-lookup"><span data-stu-id="cf01e-118">The person who signs up to buy Office 365 is a global admin by default.</span></span> <span data-ttu-id="cf01e-119">자세한 내용은 [Office 365 관리자 역할 정보](https://docs.microsoft.com/office365/admin/add-users/about-admin-roles) 를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="cf01e-119">(See [About Office 365 admin roles](https://docs.microsoft.com/office365/admin/add-users/about-admin-roles) to learn more.)</span></span>         |
|<span data-ttu-id="cf01e-120">보안 관리자</span><span class="sxs-lookup"><span data-stu-id="cf01e-120">Security Administrator</span></span> |<span data-ttu-id="cf01e-121">Azure Active Directory 관리 센터 ([https://aad.portal.azure.com](https://aad.portal.azure.com))</span><span class="sxs-lookup"><span data-stu-id="cf01e-121">Azure Active Directory admin center ([https://aad.portal.azure.com](https://aad.portal.azure.com))</span></span>|
|<span data-ttu-id="cf01e-122">Exchange Online 조직 관리</span><span class="sxs-lookup"><span data-stu-id="cf01e-122">Exchange Online Organization Management</span></span> |<span data-ttu-id="cf01e-123">Exchange 관리 센터 ([https://outlook.office365.com/ecp](https://outlook.office365.com/ecp))</span><span class="sxs-lookup"><span data-stu-id="cf01e-123">Exchange admin center ([https://outlook.office365.com/ecp](https://outlook.office365.com/ecp))</span></span> <br><span data-ttu-id="cf01e-124">또는</span><span class="sxs-lookup"><span data-stu-id="cf01e-124">or</span></span> <br>  <span data-ttu-id="cf01e-125">PowerShell cmdlet ( [Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/exchange-online-powershell?view=exchange-ps)참조)</span><span class="sxs-lookup"><span data-stu-id="cf01e-125">PowerShell cmdlets (See [Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/exchange-online-powershell?view=exchange-ps))</span></span> |

> [!TIP]
> <span data-ttu-id="cf01e-126">역할 및 사용 권한에 대 한 자세한 내용은 [Office 365 보안 &amp; 및 준수 센터의 사용 권한을](permissions-in-the-security-and-compliance-center.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="cf01e-126">To learn more about roles and permissions, see [Permissions in the Office 365 Security &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md).</span></span>

### <a name="to-view-or-edit-a-custom-do-not-rewrite-urls-list"></a><span data-ttu-id="cf01e-127">사용자 지정 "다시 쓰지 않음" Url 목록을 보거나 편집 하려면</span><span class="sxs-lookup"><span data-stu-id="cf01e-127">To view or edit a custom "do not rewrite" URLs list</span></span>
  
1. <span data-ttu-id="cf01e-128">[https://protection.office.com](https://protection.office.com) 으로 이동 하 여 회사 또는 학교 계정으로 로그인 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf01e-128">Go to [https://protection.office.com](https://protection.office.com) and sign in with your work or school account.</span></span> 
    
2. <span data-ttu-id="cf01e-129">왼쪽 탐색 창의 **위협 관리** \> **정책** \> **안전한 링크**아래에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cf01e-129">In the left navigation, under **Threat management** \> **Policy** \> **Safe Links**.</span></span>
    
3. <span data-ttu-id="cf01e-130">**특정 받는 사람에 게 적용 되는 정책** 섹션에서 **새로** 만들기 (새로 만들기 단추를 더하기 기호 ( **+**)와 유사)를 선택 하 여 새 정책을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="cf01e-130">In the **Policies that apply to specific recipients** section, choose **New** (the New button resembles a plus sign ( **+**)) to create a new policy.</span></span> <span data-ttu-id="cf01e-131">또는 기존 정책을 편집할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cf01e-131">(Alternatively, you can edit an existing policy.)</span></span><br/><span data-ttu-id="cf01e-132">![특정 전자 메일 받는 사람에 대 한 안전한 링크 정책을 추가 하려면 새로 만들기를 선택 합니다.](media/01073f42-3cec-4ddb-8c10-4d33ec434676.png)</span><span class="sxs-lookup"><span data-stu-id="cf01e-132">![Choose New to add a Safe Links policy for specific email recipients](media/01073f42-3cec-4ddb-8c10-4d33ec434676.png)</span></span>
  
4. <span data-ttu-id="cf01e-133">정책에 대 한 이름 및 설명을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf01e-133">Specify a name and description for your policy.</span></span>
    
5. <span data-ttu-id="cf01e-134">**다음 url을 다시 쓰지** 않음 구역에서 **올바른 url 입력** 상자를 선택 하 고 url을 입력 한 다음 더하기 기호 (+)를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf01e-134">In the **Do not rewrite the following URLs** section, select the **Enter a valid URL** box, and then type a URL, and then choose the plus sign (+).</span></span> 
    
6. <span data-ttu-id="cf01e-135">**적용 대상** 섹션에서 **받는 사람**을 선택 하 고 정책에 포함할 그룹을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf01e-135">In the **Applied To** section, choose **The recipient is a member of**, and then choose the group(s) you want to include in your policy.</span></span> <span data-ttu-id="cf01e-136">**추가**를 선택한 다음 **확인**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf01e-136">Choose **Add**, and then choose **OK**.</span></span>
    
7. <span data-ttu-id="cf01e-137">Url 추가가 완료 되 면 화면의 오른쪽 아래 모서리에서 **저장**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf01e-137">When you are finished adding URLs, in the lower right corner of the screen, choose **Save**.</span></span>
    
> [!NOTE]
> <span data-ttu-id="cf01e-138">조직의 차단 된 Url의 사용자 지정 목록을 검토 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf01e-138">Make sure to review your organization's custom list of blocked URLs.</span></span> <span data-ttu-id="cf01e-139">[ATP 안전한 링크를 사용 하 여 차단 된 사용자 지정 url 목록 설정를](set-up-a-custom-blocked-urls-list-wtih-atp.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="cf01e-139">See [Set up a custom blocked URLs list using ATP Safe Links](set-up-a-custom-blocked-urls-list-wtih-atp.md).</span></span> 
  
## <a name="important-points-to-keep-in-mind"></a><span data-ttu-id="cf01e-140">염두에 두어야 할 중요 사항</span><span class="sxs-lookup"><span data-stu-id="cf01e-140">Important points to keep in mind</span></span>

- <span data-ttu-id="cf01e-141">"다시 쓰지 않음" 목록에서 지정 하는 Url은 지정 된 받는 사람에 대 한 ATP 안전한 링크 검색에서 제외 됩니다.</span><span class="sxs-lookup"><span data-stu-id="cf01e-141">Any URLs that you specify in the "do not rewrite" list are excluded from ATP Safe Links scanning for the recipients that you specify.</span></span>
 
- <span data-ttu-id="cf01e-142">ATP 안전한 링크 정책에 대해 "다시 쓰지 않음" 목록을 지정 하는 경우 최대 3 개의 와일드 카드 별표 (\*)를 포함할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cf01e-142">When you specify a "do not rewrite" list for an ATP Safe Links policy, you can include up to three wildcard asterisks (\*).</span></span> <span data-ttu-id="cf01e-143">와일드 카드\*()는 `http://` or `https://`와 같은 접두사 `contoso.com`또는 하위 도메인을 명시적으로 포함 하지 않는 등의 항목에 대해 가정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="cf01e-143">Wildcards (\*) are assumed for entries such as `contoso.com`, which do not explicitly include prefixes or subdomains, like `http://` or `https://`.</span></span> <span data-ttu-id="cf01e-144">즉, `contoso.com` "다시 쓰지 않음" 목록과 비슷한 `*contoso.com*` 항목을 의미 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf01e-144">This means an entry, such as `contoso.com` is similar to `*contoso.com*` for your "do not rewrite" list.</span></span>

- <span data-ttu-id="cf01e-145">"다시 쓰지 않음" 목록에 이미 Url 목록이 있는 경우 해당 목록을 검토 하 고 와일드 카드를 적절 하 게 추가 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf01e-145">If you already have a list of URLs in your "do not rewrite" list, make sure to review that list and add wildcards as appropriate.</span></span> <span data-ttu-id="cf01e-146">예를 들어 기존 목록에 항목이 `http://contoso.com/a` 있는 경우 정책 `http://contoso.com/a/b` 에 하위 경로를 포함 하려면 항목에 와일드 카드를 추가 하 여 표시 `http://contoso.com/a*`합니다.</span><span class="sxs-lookup"><span data-stu-id="cf01e-146">For example, if your existing list has an entry like `http://contoso.com/a` and you want to include subpaths like `http://contoso.com/a/b` in your policy, add a wildcard to your entry so it looks like `http://contoso.com/a*`.</span></span>
    
- <span data-ttu-id="cf01e-147">"다시 쓰지 않음" 목록에 지정한 Url에 슬래시 (/)를 포함 하지 마십시오.</span><span class="sxs-lookup"><span data-stu-id="cf01e-147">Do not include a forward slash (/) in the URLs that you specify in your "do not rewrite" list.</span></span> <span data-ttu-id="cf01e-148">예를 들어 "다시 쓰지 `contoso.com/` 않음" 목록에 입력 하는 대신 enter 키 `contoso.com`를 누르십시오.</span><span class="sxs-lookup"><span data-stu-id="cf01e-148">For example, rather than enter `contoso.com/` in your "do not rewrite" list, enter `contoso.com`.</span></span>
    
<span data-ttu-id="cf01e-149">다음 표에는 입력 가능한 항목과 해당 항목이 갖는 영향에 대 한 예가 나와 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cf01e-149">The following table lists examples of what you can enter and what effect those entries have.</span></span>
    
|<span data-ttu-id="cf01e-150">**예제 항목**</span><span class="sxs-lookup"><span data-stu-id="cf01e-150">**Example Entry**</span></span>|<span data-ttu-id="cf01e-151">**수행 하는 작업**</span><span class="sxs-lookup"><span data-stu-id="cf01e-151">**What It Does**</span></span>|
|:-----|:-----|
|`*contoso.com*`  <br/> |<span data-ttu-id="cf01e-152">특정 받는 사람이 도메인, 하위 사이트 및 경로 (예: `http://www.contoso.com` `https://www.contoso.com` `https://maps.contoso.com`, 또는)를 사용할 수 있습니다.`http://www.contoso.com/a`</span><span class="sxs-lookup"><span data-stu-id="cf01e-152">Allows specific recipients to visit a domain, subdomains, and paths, such as `http://www.contoso.com`, `https://www.contoso.com`, `https://maps.contoso.com`, or `http://www.contoso.com/a`</span></span>  <br/> |
|`http://contoso.com/a`  <br/> |<span data-ttu-id="cf01e-153">특정 받는 사람이 같은 사이트를 방문 하 `http://contoso.com/a`되 하위 경로는 볼 수 없습니다.`http://contoso.com/a/b`</span><span class="sxs-lookup"><span data-stu-id="cf01e-153">Allows specific recipients to visit a site like `http://contoso.com/a`, but not subpaths like `http://contoso.com/a/b`</span></span>  <br/> |
|`http://contoso.com/a*`  <br/> |<span data-ttu-id="cf01e-154">특정 받는 사람이 같은 사이트 `http://contoso.com/a` 와 같은 하위 경로를 방문할 수 있도록 허용`http://contoso.com/a/b`</span><span class="sxs-lookup"><span data-stu-id="cf01e-154">Allows specific recipients to visit a site like `http://contoso.com/a` and subpaths like `http://contoso.com/a/b`</span></span>  <br/> |
   
 