---
title: Office 365 ATP 안전한 링크
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.audience: Admin
ms.date: 02/11/2019
ms.topic: overview
f1_keywords:
- "197503"
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MET150
- MOE150
- ZVO160
- ZXL160
- ZPP160
- ZWD160
ms.assetid: dd6a1fef-ec4a-4cf4-a25a-bb591c5811e3
description: 안전한 링크 기능은 다음 Office 문서 및 전자 메일 메시지에 하이퍼링크의 클릭 시간 확인 합니다. 피싱 및 기타 공격 으로부터 조직을 보호를 안전한 링크를 사용 합니다.
ms.openlocfilehash: 4d83aa65af47ea6723d6e2042c230fb2b07c174c
ms.sourcegitcommit: 065f5e72676511b5ecf7f10a17685999780e92d8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/11/2019
ms.locfileid: "29888034"
---
# <a name="office-365-atp-safe-links"></a><span data-ttu-id="2aea8-104">Office 365 ATP 안전한 링크</span><span class="sxs-lookup"><span data-stu-id="2aea8-104">Office 365 ATP Safe Links</span></span>

## <a name="overview-of-office-365-atp-safe-links"></a><span data-ttu-id="2aea8-105">Office 365 ATP 안전 하 게 보호 링크의 개요 (영문)</span><span class="sxs-lookup"><span data-stu-id="2aea8-105">Overview of Office 365 ATP Safe Links</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2aea8-p102">이 문서는 기업 고객을 위한 것입니다. Outlook에서 안전한 링크에 대 한 정보에 대 한 자세한 내용은 홈 사용자 인 경우 [Outlook.com 고급 보안](https://support.office.com/article/advanced-outlook-com-security-for-office-365-subscribers-882d2243-eab9-4545-a58a-b36fee4a46e2)을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="2aea8-p102">This article is intended for business customers. If you are a home user looking for information about Safe Links in Outlook, see [Advanced Outlook.com security](https://support.office.com/article/advanced-outlook-com-security-for-office-365-subscribers-882d2243-eab9-4545-a58a-b36fee4a46e2).</span></span>

<span data-ttu-id="2aea8-p103">Office 365 ATP 안전한 링크 ( [고급 위협 보호](office-365-atp.md)의 일부)는 클릭 시간 확인 [전자 메일 메시지](#how-atp-safe-links-works-with-email) 및 [Office 문서](#how-atp-safe-links-works-with-office-documents)에서 웹 주소 (Url)를 제공 하 여 조직을 보호할 수 있습니다. Office 365 보안 팀에 의해 설정 된 [ATP 안전한 링크 정책](set-up-atp-safe-links-policies.md) 을 통해 보호 정의 됩니다.</span><span class="sxs-lookup"><span data-stu-id="2aea8-p103">Office 365 ATP Safe Links (part of [Advanced Threat Protection](office-365-atp.md)) can help protect your organization by providing time-of-click verification of web addresses (URLs) in [email messages](#how-atp-safe-links-works-with-email) and [Office documents](#how-atp-safe-links-works-with-office-documents). Protection is defined through [ATP Safe Links policies](set-up-atp-safe-links-policies.md) that are set by your Office 365 security team.</span></span> 
  
<span data-ttu-id="2aea8-p104">ATP 안전한 링크 정책이 설정 되어, 되 면 Office 365 전역 관리자, 보안 관리자 및 보안 독자 [고급 위협 보호에 대 한 보고서 보기](view-reports-for-atp.md)수 있습니다. 이러한 보고서의 정보에는 조직을 보호 하거나 보안 문제를 조사 하는 추가 단계를 수행 하 여 보안 팀 데 도움이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="2aea8-p104">Once your ATP Safe Links policies are in place, Office 365 global administrators, security administrators, and security readers can [view reports for Advanced Threat Protection](view-reports-for-atp.md). The information in those reports can help your security team take further steps to protect your organization or research security incidents.</span></span>

<span data-ttu-id="2aea8-p105">[ATP에 새로운 기능이 추가 됩니다](office-365-atp.md#new-features-are-continually-being-added-to-atp)Office 365 보안 팀 추가 수 또는 조직의 ATP 안전한 링크 정책을 편집 합니다. 또한 변경 사항 및 향상 된 기능에서는 새로 수정 된 [경고 페이지](atp-safe-links-warning-pages.md) 및 Outlook에서 렌더링 되는 기본 링크와 같은 것을 알 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2aea8-p105">As [new features are added to ATP](office-365-atp.md#new-features-are-continually-being-added-to-atp), your Office 365 security team can add or edit your organization's ATP Safe Links policies. In addition, you might notice changes and improvements, such as our newly revised [warning pages](atp-safe-links-warning-pages.md) and native link rendering in Outlook.</span></span>
         
## <a name="how-atp-safe-links-works-with-urls-in-email"></a><span data-ttu-id="2aea8-114">ATP 안전한 링크 Url이 포함 된 전자 메일에서 작동 하는 방법</span><span class="sxs-lookup"><span data-stu-id="2aea8-114">How ATP Safe Links works with URLs in email</span></span>

<span data-ttu-id="2aea8-115">높은 수준의 같습니다 ATP 안전한 링크 보호 Url에 대 한 전자 메일 (Office 365를 하지 온-프레미스에 호스트)에서 작동 하는 방법.</span><span class="sxs-lookup"><span data-stu-id="2aea8-115">At a high level, here's how ATP Safe Links protection works for URLs in email (hosted in Office 365, not on-premises):</span></span>
  
1. <span data-ttu-id="2aea8-116">사용자는 전자 메일 메시지, Url을 포함 하는 중 일부를 받습니다.</span><span class="sxs-lookup"><span data-stu-id="2aea8-116">People receive email messages, some of which contain URLs.</span></span>
    
2. <span data-ttu-id="2aea8-117">IP (인터넷 프로토콜) 및 봉투를 필터링 하는 Exchange Online Protection을 통해 이동 모든 전자 메일 서명 기반 맬웨어 방지, 스팸 방지 및 맬웨어 방지 필터 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="2aea8-117">All email goes through Exchange Online Protection, where internet protocol (IP) and envelope filters, signature-based malware protection, anti-spam and anti-malware filters are applied.</span></span> 
    
3. <span data-ttu-id="2aea8-118">전자 메일 사용자의 받은 편지함에 도착합니다.</span><span class="sxs-lookup"><span data-stu-id="2aea8-118">Email arrives in people's inboxes.</span></span>
    
4. <span data-ttu-id="2aea8-119">사용자는 Office 365에 로그인 하 고 자신의 전자 메일 받은 편지 함으로 이동 됩니다.</span><span class="sxs-lookup"><span data-stu-id="2aea8-119">A user signs in to Office 365, and goes to their email inbox.</span></span>
    
5. <span data-ttu-id="2aea8-120">사용자 전자 메일 메시지로 열리고 전자 메일 메시지에서 URL에 대해를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="2aea8-120">The user opens an email message, and clicks on a URL in the email message.</span></span>
    
6. <span data-ttu-id="2aea8-p106">ATP 안전한 링크 기능 웹사이트를 열기 전에 URL을 확인 하는 즉시 합니다. 악의적인, 또는 안전 차단 URL은 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="2aea8-p106">The ATP Safe Links feature immediately checks the URL before opening the website. The URL is identified as blocked, malicious, or safe.</span></span>
    
    - <span data-ttu-id="2aea8-123">URL 인 사용자에 게 적용 되는 정책에 대 한 [사용자 지정 "rewrite 수행" Url 목록](set-up-a-custom-do-not-rewrite-urls-list-with-atp.md) 에 포함 된 사이트를 참조 하는 경우 웹사이트를 엽니다.</span><span class="sxs-lookup"><span data-stu-id="2aea8-123">If the URL is to a website that is included in a [custom "Do not rewrite" URLs list](set-up-a-custom-do-not-rewrite-urls-list-with-atp.md) for a policy that applies to the user, the website opens.</span></span> 
    
    - <span data-ttu-id="2aea8-124">조직의 [차단 된 사용자 지정 Url 목록](set-up-a-custom-blocked-urls-list-wtih-atp.md)에 포함 된 웹사이트에 URL이 있는 경우 [경고 페이지가](atp-safe-links-warning-pages.md) 열립니다.</span><span class="sxs-lookup"><span data-stu-id="2aea8-124">If the URL is to a website that is included in the organization's [custom blocked URLs list](set-up-a-custom-blocked-urls-list-wtih-atp.md), a [warning page](atp-safe-links-warning-pages.md) opens.</span></span> 
    
    - <span data-ttu-id="2aea8-125">악성 코드가 포함 될으로 확인 된 사이트로 URL이 있는 경우 [경고 페이지가](atp-safe-links-warning-pages.md) 열립니다.</span><span class="sxs-lookup"><span data-stu-id="2aea8-125">If the URL is to a website that has been determined to be malicious, a [warning page](atp-safe-links-warning-pages.md) opens.</span></span> 
    
    - <span data-ttu-id="2aea8-126">다운로드 가능한 파일에 URL 이동 하는 경우 조직의 [ATP 안전한 링크 정책](set-up-atp-safe-links-policies.md) 은 이러한 콘텐츠를 검사 하도록 구성 된 다운로드 파일을 검사 합니다.</span><span class="sxs-lookup"><span data-stu-id="2aea8-126">If the URL goes to a downloadable file and your organization's [ATP Safe Links policies](set-up-atp-safe-links-policies.md) are configured to scan such content, the downloadable file is checked.</span></span> 
    
    - <span data-ttu-id="2aea8-127">URL을 안전한 것으로 확인 하는 경우 웹사이트를 엽니다.</span><span class="sxs-lookup"><span data-stu-id="2aea8-127">If the URL is determined to be safe, the website opens.</span></span>
    
## <a name="how-atp-safe-links-works-with-urls-in-office-documents"></a><span data-ttu-id="2aea8-128">ATP 안전한 링크 Url이 포함 된 Office 문서에서 작동 하는 방법</span><span class="sxs-lookup"><span data-stu-id="2aea8-128">How ATP Safe Links works with URLs in Office documents</span></span>

<span data-ttu-id="2aea8-129">높은 수준의 같습니다 ATP 안전한 링크 보호 Url에 대 한 Office 365 ProPlus 응용 프로그램 (Word, Excel 및 PowerPoint Windows 또는 Mac, iOS 또는 Android 장치, Windows, OneNote Online 및 Office Online에서 Visio에 Office 응용 프로그램에서의 현재 버전)에서 작동 하는 방법.</span><span class="sxs-lookup"><span data-stu-id="2aea8-129">At a high level, here's how ATP Safe Links protection works for URLs in Office 365 ProPlus applications (current versions of Word, Excel, and PowerPoint on Windows or Mac, Office apps on iOS or Android devices, Visio on Windows, OneNote Online, and Office Online):</span></span>
  
1. <span data-ttu-id="2aea8-p107">사람들이 자신의 컴퓨터, smartphone 또는 태블릿에 Office 365 ProPlus를 설치 했습니다. (또는 자신의 브라우저에서 Office Online 사용 됩니다.)</span><span class="sxs-lookup"><span data-stu-id="2aea8-p107">People have installed Office 365 ProPlus on their computer, smartphone, or tablet. (Or, they are using Office Online in their browser.)</span></span>
    
2. <span data-ttu-id="2aea8-p108">사용자가 Word, Excel, PowerPoint 또는 Visio를 열고 자신의 작업이 나 교육용 계정을 사용 하 여 Office 365 엔터프라이즈에 로그인 합니다. 다음은 문서 Url이 들어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2aea8-p108">A user opens a Word, Excel, PowerPoint, or Visio, and signs in to Office 365 Enterprise using their work or school account. The document contains URLs.</span></span>
    
3. <span data-ttu-id="2aea8-134">사용자가 문서에 URL을 클릭 하면 ATP 안전한 링크 서비스에 대 한 링크를 검사 합니다.</span><span class="sxs-lookup"><span data-stu-id="2aea8-134">When the user clicks on a URL in the document, the link is checked by the ATP Safe Links service.</span></span>
    
  - <span data-ttu-id="2aea8-135">URL 인 사용자에 게 적용 되는 정책에 대 한 [사용자 지정 "rewrite 수행" Url 목록](set-up-a-custom-do-not-rewrite-urls-list-with-atp.md) 에 포함 된 사이트를 참조 하는 경우 해당 사용자는 웹사이트에 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="2aea8-135">If the URL is to a website that is included in a [custom "Do not rewrite" URLs list](set-up-a-custom-do-not-rewrite-urls-list-with-atp.md) for a policy that applies to the user, that user is taken to the website.</span></span> 
    
  - <span data-ttu-id="2aea8-136">조직의 [차단 된 사용자 지정 Url 목록](set-up-a-custom-blocked-urls-list-wtih-atp.md)에 포함 된 웹사이트에 URL이 있는 경우 [경고 페이지](atp-safe-links-warning-pages.md)로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="2aea8-136">If the URL is to a website that is included in the organization's [custom blocked URLs list](set-up-a-custom-blocked-urls-list-wtih-atp.md), the user is taken to a [warning page](atp-safe-links-warning-pages.md).</span></span>
    
  - <span data-ttu-id="2aea8-137">악성 코드가 포함 될으로 확인 된 사이트로 URL이 있는 경우 [경고 페이지](atp-safe-links-warning-pages.md)로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="2aea8-137">If the URL is to a website that has been determined to be malicious, the user is taken to a [warning page](atp-safe-links-warning-pages.md).</span></span>
    
  - <span data-ttu-id="2aea8-138">URL 다운로드 가능한 파일에 들어가고 [ATP 안전한 링크 정책](set-up-atp-safe-links-policies.md) 은 이러한 다운로드를 검색 하도록 구성 된 경우 다운로드 파일을 검사 합니다.</span><span class="sxs-lookup"><span data-stu-id="2aea8-138">If the URL goes to a downloadable file and the [ATP Safe Links policies](set-up-atp-safe-links-policies.md) are configured to scan such downloads, the downloadable file is checked.</span></span> 
    
  - <span data-ttu-id="2aea8-139">URL은 안전한으로 간주 하는 경우 사용자 웹사이트를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="2aea8-139">If the URL is considered safe, the user is taken to the website.</span></span>

## <a name="how-to-get-atp-safe-links-protection"></a><span data-ttu-id="2aea8-140">ATP 안전한 링크 보호 하는 방법</span><span class="sxs-lookup"><span data-stu-id="2aea8-140">How to get ATP Safe Links protection</span></span>

<span data-ttu-id="2aea8-p109">먼저, 구독 [고급 위협 보호](office-365-atp.md)를 포함 해야 합니다. ATP에 [Microsoft 365 Enterprise](https://www.microsoft.com/microsoft-365/enterprise/home)"," [Microsoft 365 비즈니스](https://www.microsoft.com/microsoft-365/business)"," Office 365 엔터프라이즈 e 5 "," Office 365 교육 A5 "," 등의 구독에 포함 됩니다. 조직에 Office 365 ATP를 포함 하지 않는 한 Office 365 구독을 하는 경우에 추가 기능으로 ATP을 잠재적으로 구입할 수 있습니다. 자세한 내용은 [Office 365 고급 위협 보호 계획 및 가격](https://products.office.com/exchange/advance-threat-protection) 및 [Office 365 고급 위협 Protection Service Description](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description)을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="2aea8-p109">First, make sure your subscription includes [Advanced Threat Protection](office-365-atp.md). ATP is included in in subscriptions, such as [Microsoft 365 Enterprise](https://www.microsoft.com/microsoft-365/enterprise/home), [Microsoft 365 Business](https://www.microsoft.com/microsoft-365/business), Office 365 Enterprise E5, Office 365 Education A5, etc. If your organization has an Office 365 subscription that does not include Office 365 ATP, you can potentially purchase ATP as an add-on. For more information, see [Office 365 Advanced Threat Protection plans and pricing](https://products.office.com/exchange/advance-threat-protection) and the [Office 365 Advanced Threat Protection Service Description](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description).</span></span> 
  
<span data-ttu-id="2aea8-p110">다음으로, ATP 안전한 링크 정책에 정의 된 확인 합니다. ( [Office 365 ATP 안전한 링크 정책 설정](set-up-atp-safe-links-policies.md)참조). ATP 안전한 링크 기능은 현재 경우:</span><span class="sxs-lookup"><span data-stu-id="2aea8-p110">Next, make sure your ATP Safe Links policies are defined. (See [Set up Office 365 ATP Safe Links policies](set-up-atp-safe-links-policies.md).) ATP Safe Links features are active when:</span></span>
  
- <span data-ttu-id="2aea8-p111">Word, Excel, PowerPoint 및 Visio 문서 및 전자 메일에 대 한 **ATP 안전한 링크 정책을 설정** 합니다. ( [Office 365의 ATP 안전한 링크 정책 설정](set-up-atp-safe-links-policies.md)참조).</span><span class="sxs-lookup"><span data-stu-id="2aea8-p111">**ATP Safe Links policies are set up** for email and for Word, Excel, PowerPoint, and Visio documents. (See [Set up ATP safe links policies in Office 365](set-up-atp-safe-links-policies.md).)</span></span>

- <span data-ttu-id="2aea8-p112">**Office 365 클라이언트 앱 현대 인증을 사용 하도록 구성 된** (이것은 Office 문서에서 ATP 안전한 링크 보호를 위한)입니다. ( [Office 2016에 대 한 최신 인증](https://docs.microsoft.com/office365/enterprise/modern-auth-for-office-2013-and-2016)참조).</span><span class="sxs-lookup"><span data-stu-id="2aea8-p112">**Office 365 client apps are configured to use Modern Authentication** (this is for ATP Safe Links protection in Office documents). (See [Modern Authentication for Office 2016](https://docs.microsoft.com/office365/enterprise/modern-auth-for-office-2013-and-2016).)</span></span> 
    
- <span data-ttu-id="2aea8-p113">사용자의 작업이 나 교육용 계정을 사용 하 여 **사용자가 Office 365에 로그인 됩니다** . ( [Office 또는 Office 365에 로그인](https://support.office.com/article/b9582171-fd1f-4284-9846-bdd72bb28426)참조).</span><span class="sxs-lookup"><span data-stu-id="2aea8-p113">**Users have signed into Office 365** using their work or school account. (See [Sign in to Office or Office 365](https://support.office.com/article/b9582171-fd1f-4284-9846-bdd72bb28426).)</span></span>
    
- <span data-ttu-id="2aea8-152">**Exchange Online Protection을 통해 조직의 전자 메일을 전달**합니다.</span><span class="sxs-lookup"><span data-stu-id="2aea8-152">**Your organization's email passes through Exchange Online Protection**.</span></span>  

<span data-ttu-id="2aea8-153">ATP 정책, 정의 (또는 편집)를 할당 되어 있어야 다음 표에 설명 된 역할 중 하나:</span><span class="sxs-lookup"><span data-stu-id="2aea8-153">To define (or edit) ATP policies, you must be assigned one of the roles described in the following table:</span></span>

|<span data-ttu-id="2aea8-154">역할</span><span class="sxs-lookup"><span data-stu-id="2aea8-154">Role</span></span>  |<span data-ttu-id="2aea8-155">Where/방법 할당</span><span class="sxs-lookup"><span data-stu-id="2aea8-155">Where/how assigned</span></span>  |
|---------|---------|
|<span data-ttu-id="2aea8-156">Office 365 전역 관리자</span><span class="sxs-lookup"><span data-stu-id="2aea8-156">Office 365 Global Administrator</span></span> |<span data-ttu-id="2aea8-p114">Office 365를 구매 하 여를 로그인 하는 사람 이름은 기본적으로 전역 admin입니다. (자세한 내용은 [Office 365에 대 한 관리자 역할](https://docs.microsoft.com/office365/admin/add-users/about-admin-roles) 참조 하십시오.)</span><span class="sxs-lookup"><span data-stu-id="2aea8-p114">The person who signs up to buy Office 365 is a global admin by default. (See [About Office 365 admin roles](https://docs.microsoft.com/office365/admin/add-users/about-admin-roles) to learn more.)</span></span>         |
|<span data-ttu-id="2aea8-159">보안 관리자</span><span class="sxs-lookup"><span data-stu-id="2aea8-159">Security Administrator</span></span> |<span data-ttu-id="2aea8-160">Azure Active Directory 관리 센터 ([https://aad.portal.azure.com](https://aad.portal.azure.com))</span><span class="sxs-lookup"><span data-stu-id="2aea8-160">Azure Active Directory admin center ([https://aad.portal.azure.com](https://aad.portal.azure.com))</span></span>|
|<span data-ttu-id="2aea8-161">Exchange Online 조직 관리</span><span class="sxs-lookup"><span data-stu-id="2aea8-161">Exchange Online Organization Management</span></span> |<span data-ttu-id="2aea8-162">Exchange 관리 센터 ([https://outlook.office365.com/ecp](https://outlook.office365.com/ecp))</span><span class="sxs-lookup"><span data-stu-id="2aea8-162">Exchange admin center ([https://outlook.office365.com/ecp](https://outlook.office365.com/ecp))</span></span> <br><span data-ttu-id="2aea8-163">또는</span><span class="sxs-lookup"><span data-stu-id="2aea8-163">or</span></span> <br>  <span data-ttu-id="2aea8-164">PowerShell cmdlet (참조 [Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/exchange-online-powershell?view=exchange-ps))</span><span class="sxs-lookup"><span data-stu-id="2aea8-164">PowerShell cmdlets (See [Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/exchange-online-powershell?view=exchange-ps))</span></span> |
    
## <a name="how-to-make-sure-atp-safe-links-protection-is-in-place"></a><span data-ttu-id="2aea8-165">원본 위치에는 있는지 ATP 안전한 링크 보호 하는 방법</span><span class="sxs-lookup"><span data-stu-id="2aea8-165">How to make sure ATP Safe Links protection is in place</span></span>

<span data-ttu-id="2aea8-p115">전역 관리자 또는 보안 관리자, [ATP 안전한 링크 정책](set-up-atp-safe-links-policies.md)을 검토 해야 합니다. ATP 안전한 링크 정책은 여부 보호 적용 하는 전자 메일 메시지에 하이퍼링크에만, 또는 Url에 Office 문서에도에서 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2aea8-p115">As a global administrator or security administrator, be sure to review your [ATP Safe Links policies](set-up-atp-safe-links-policies.md). ATP Safe Links policies determine whether protection applies to hyperlinks in email messages only, or to URLs in Office documents as well.</span></span>

<span data-ttu-id="2aea8-168">ATP 안전한 링크 정책이 설정 되어, 한 후에 조직의 보안 팀 볼 수 [고급 위협 보호에 대 한 보기 보고서](view-reports-for-atp.md)크기는 조직에 대 한 ATP 안전한 링크 보호가 작동 하는 방법을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="2aea8-168">After ATP Safe Links policies are in place, your organization's security team can see see how ATP Safe Links protection is working for your organization is by [viewing reports for Advanced Threat Protection](view-reports-for-atp.md).</span></span> 

## <a name="example-scenarios"></a><span data-ttu-id="2aea8-169">예제 시나리오</span><span class="sxs-lookup"><span data-stu-id="2aea8-169">Example scenarios</span></span>
  
<span data-ttu-id="2aea8-p116">다음 표에서 일부 예제 시나리오를 ATP 안전한 링크 보호 수도 있고 전체에서 되지 않을 수 있습니다. (모든 이러한 경우 가정 조직에 Office 365 Enterprise e 5.)</span><span class="sxs-lookup"><span data-stu-id="2aea8-p116">The following table describes some example scenarios where ATP Safe Links protection might or might not be in place. (In all of these cases, we assume the organization has Office 365 Enterprise E5.)</span></span>
  
|<span data-ttu-id="2aea8-172">**시나리오 예**</span><span class="sxs-lookup"><span data-stu-id="2aea8-172">**Example scenario**</span></span>|<span data-ttu-id="2aea8-173">**ATP 안전한 링크 보호는이 경우에 적용 여부**</span><span class="sxs-lookup"><span data-stu-id="2aea8-173">**Does ATP Safe Links protection apply in this case?**</span></span>|
|:-----|:-----|
|<span data-ttu-id="2aea8-p117">Jean에 Url을 전자 메일 및 Office 문서에서 다루는 ATP 안전한 링크 정책이 있는 그룹의 구성원입니다. Jean은 PowerPoint 프레젠테이션, 보낸 사람이 열리고 프레젠테이션에서 URL을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="2aea8-p117">Jean is a member of a group that has ATP Safe Links policies covering URLs in email and Office documents. Jean opens a PowerPoint presentation that someone sent, and then clicks a URL in the presentation.</span></span>  <br/> |<span data-ttu-id="2aea8-p118">예입니다. 정의 된는 ATP 안전한 링크 정책이 Jean의 그룹, Jean의 전자 메일 및 Jean 열리는 Jean 로그인을 Word, Excel, PowerPoint 또는 Visio 문서 및 Windows, iOS, 또는 Android 장치에서 Office 365 ProPlus를 사용 하 여 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="2aea8-p118">Yes. The ATP Safe Links policies that are defined apply to Jean's group, Jean's email, and Word, Excel, PowerPoint, or Visio documents that Jean opens, so long as Jean is signed in and using Office 365 ProPlus on Windows, iOS, or Android devices.</span></span>  <br/> |
|<span data-ttu-id="2aea8-p119">Chris의 조직, 더 전역 또는 보안 관리자에서 모든 ATP 안전한 링크 정책을 아직 정의 했습니다. Chris 악성 웹사이트에 대 한 URL을 포함 하는 전자 메일을 받습니다. Chris 인식 하지 않으며 URL은 악의적인 및 링크를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="2aea8-p119">In Chris's organization, no global or security administrators have defined any ATP safe links policies yet. Chris receives an email that contains a URL to a malicious website. Chris is unaware the URL is malicious and clicks the link.</span></span>  <br/> |<span data-ttu-id="2aea8-p120">아니요. 원본 위치에 있는 것으로 보호 하기 위해에서 조직의 모든 사용자에 대 한 Url을 적용 하는 기본 정책 정의 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="2aea8-p120">No. The default policy that covers URLs for everyone in the organization must be defined in order for protection to be in place.</span></span>  <br/> |
|<span data-ttu-id="2aea8-p121">Pat의 조직, 더 전역 또는 보안 관리자가 정의 했거나 아직 모든 ATP 안전한 링크 정책을 편집 합니다. Pat은 Word 문서를 열리고 파일의 URL을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="2aea8-p121">In Pat's organization, no global or security administrators have defined or edited any ATP Safe Links policies yet. Pat opens a Word document and clicks a URL in the file.</span></span>  <br/> |<span data-ttu-id="2aea8-p122">원본 위치에 있는 것으로 보호 하기 위해에서 Office 문서를 포함 하는 아니요 A 정책 정의 되어야 합니다. [Office 365의 ATP 안전한 링크 정책 설정](set-up-atp-safe-links-policies.md)참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="2aea8-p122">No. A policy that includes Office documents must be defined in order for protection to be in place. See [Set up ATP Safe Links policies in Office 365](set-up-atp-safe-links-policies.md).  </span></span><br/> |
|<span data-ttu-id="2aea8-p123">백화점 ㈜의 조직에 포함 된 ATP 안전한 링크 정책이 `http://tailspintoys.com` 차단 된 웹사이트도 나열 합니다. Lee에 대 한 URL을 포함 하는 전자 메일 메시지를 수신 `http://tailspintoys.com/aboutus/trythispage`합니다. Lee가 URL을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="2aea8-p123">Lee's organization has a ATP Safe Links policy that has `http://tailspintoys.com` listed as a blocked website. Lee receives an email message that contains a URL to `http://tailspintoys.com/aboutus/trythispage`. Lee clicks the URL.  </span></span><br/> |<span data-ttu-id="2aea8-p124">전체 사이트와 그 하위의 목록에 포함 된 모든 Url을 차단 여부에 따라 다릅니다. [ATP 안전 링크를 사용 하 여 차단 된 Url 목록 사용자 지정 설정](set-up-a-custom-blocked-urls-list-wtih-atp.md)을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="2aea8-p124">It depends on whether the entire site and all its subpages are included in the list of blocked URLs. See [Set up a custom blocked URLs list using ATP Safe Links](set-up-a-custom-blocked-urls-list-wtih-atp.md).  </span></span><br/> |
|<span data-ttu-id="2aea8-193">김 Jean의 동료, 전자 메일을 보내 Jean, 악성 URL이 전자 메일에 포함 된 정확히 모르는 합니다.</span><span class="sxs-lookup"><span data-stu-id="2aea8-193">Jamie, Jean's colleague, sends an email to Jean, not knowing that the email contains a malicious URL.</span></span>  <br/> |<span data-ttu-id="2aea8-p125">ATP 안전한 링크 정책을 조직 내에서 보낸 전자 메일에 대해 정의 되는 여부에 따라 다릅니다. [Office 365의 ATP 안전한 링크 정책 설정](set-up-atp-safe-links-policies.md)참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="2aea8-p125">It depends on whether ATP Safe Links policies are defined for email sent within the organization. See [Set up ATP Safe Links policies in Office 365](set-up-atp-safe-links-policies.md).  </span></span><br/> |


  

