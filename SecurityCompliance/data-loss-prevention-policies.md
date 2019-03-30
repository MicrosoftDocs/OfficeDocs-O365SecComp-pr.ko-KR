---
title: 데이터 손실 방지 정책 개요
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 3/29/2019
ms.audience: ITPro
ms.topic: conceptual
f1_keywords:
- ms.o365.cc.DLPLandingPage
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- M365-security-compliance
search.appverid:
- MET150
description: office 365 보안 &amp; 및 준수 센터의 DLP (데이터 손실 방지) 정책을 사용 하 여 office 365에서 중요 한 정보를 식별, 모니터링 및 자동으로 보호할 수 있습니다.
ms.openlocfilehash: 4117a99afc804fd397deb45087c5058077f9ff60
ms.sourcegitcommit: e7a776a04ef6ed5e287a33cfdc36aa2d72862b55
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/29/2019
ms.locfileid: "31000021"
---
# <a name="overview-of-data-loss-prevention-policies"></a><span data-ttu-id="c8a05-103">데이터 손실 방지 정책 개요</span><span class="sxs-lookup"><span data-stu-id="c8a05-103">Overview of data loss prevention policies</span></span>

<span data-ttu-id="c8a05-104">비즈니스 표준 및 산업 규정을 준수하려면 조직에서는 중요한 정보를 보호하고 실수로 공개되지 않도록 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-104">To comply with business standards and industry regulations, organizations need to protect sensitive information and prevent its inadvertent disclosure.</span></span> <span data-ttu-id="c8a05-105">조직 외부에 누출되지 않도록 하려는 중요한 정보의 예로는 금융 데이터나 신용 카드 번호, 주민 등록 번호, 의료 기록과 같은 PII(개인 식별 정보)가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-105">Examples of sensitive information that you might want to prevent from leaking outside your organization include financial data or personally identifiable information (PII) such as credit card numbers, social security numbers, or health records.</span></span> <span data-ttu-id="c8a05-106">office 365 보안 &amp; 및 준수 센터의 DLP (데이터 손실 방지) 정책을 사용 하 여 office 365에서 중요 한 정보를 식별, 모니터링 및 자동으로 보호할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-106">With a data loss prevention (DLP) policy in the Office 365 Security &amp; Compliance Center, you can identify, monitor, and automatically protect sensitive information across Office 365.</span></span>
  
<span data-ttu-id="c8a05-107">DLP 정책을 사용하여 다음 작업을 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-107">With a DLP policy, you can:</span></span>
  
- <span data-ttu-id="c8a05-108">**Exchange online, SharePoint online, 비즈니스용 OneDrive 및 Microsoft 팀과 같은 다양 한 위치에서 중요 한 정보를 식별 합니다.**</span><span class="sxs-lookup"><span data-stu-id="c8a05-108">**Identify sensitive information across many locations, such as Exchange Online, SharePoint Online, OneDrive for Business, and Microsoft Teams.**</span></span>
    
    <span data-ttu-id="c8a05-109">예를 들어 비즈니스용 onedrive 사이트에 저장 된 신용 카드 번호가 포함 된 모든 문서를 식별 하거나 특정 사용자의 onedrive 사이트만 모니터링할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-109">For example, you can identify any document containing a credit card number that's stored in any OneDrive for Business site, or you can monitor just the OneDrive sites of specific people.</span></span>
    
- <span data-ttu-id="c8a05-110">**중요한 정보가 실수로 공유되지 않도록 합니다**.</span><span class="sxs-lookup"><span data-stu-id="c8a05-110">**Prevent the accidental sharing of sensitive information**.</span></span> 
    
    <span data-ttu-id="c8a05-111">예를 들어 조직 외부의 사용자와 공유 하는 상태 레코드가 포함 된 모든 문서 또는 전자 메일을 식별 한 다음 해당 문서에 대 한 액세스를 자동으로 차단 하거나 전자 메일이 전송 되지 않도록 차단할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-111">For example, you can identify any document or email containing a health record that's shared with people outside your organization, and then automatically block access to that document or block the email from being sent.</span></span>
    
- <span data-ttu-id="c8a05-112">**Excel, PowerPoint 및 Word의 데스크톱 버전에서 중요 한 정보를 모니터링 하 고 보호 합니다.**</span><span class="sxs-lookup"><span data-stu-id="c8a05-112">**Monitor and protect sensitive information in the desktop versions of Excel, PowerPoint, and Word.**</span></span>
    
    <span data-ttu-id="c8a05-113">Exchange online, SharePoint online 및 비즈니스용 OneDrive와 마찬가지로 이러한 Office 데스크톱 프로그램은 중요 한 정보를 식별 하 고 DLP 정책을 적용 하는 것과 같은 기능을 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-113">Just like in Exchange Online, SharePoint Online, and OneDrive for Business, these Office desktop programs include the same capabilities to identify sensitive information and apply DLP policies.</span></span> <span data-ttu-id="c8a05-114">DLP는 사용자가 이러한 Office 프로그램에서 콘텐츠를 공유 하는 경우 지속적인 모니터링을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-114">DLP provides continuous monitoring when people share content in these Office programs.</span></span>
    
- <span data-ttu-id="c8a05-115">**사용자가 자신의 워크플로를 중단하지 않고 규정 준수 상태를 유지하도록 하는 방법을 알도록 도와줄 수 있습니다.**</span><span class="sxs-lookup"><span data-stu-id="c8a05-115">**Help users learn how to stay compliant without interrupting their workflow.**</span></span>
    
    <span data-ttu-id="c8a05-116">사용자에게 DLP 정책에 대해 교육하고 자신의 작업을 중단하지 않고 규정 준수 상태를 유지하도록 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-116">You can educate your users about DLP policies and help them remain compliant without blocking their work.</span></span> <span data-ttu-id="c8a05-117">예를 들어 사용자가 중요한 정보를 포함하는 문서를 공유하려고 하면 DLP 정책은 전자 메일 알림을 보내고, 업무 정당성이 있을 경우 이 정책을 재정의할 수 있는 문서 라이브러리의 컨텍스트에서 정책 팁을 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-117">For example, if a user tries to share a document containing sensitive information, a DLP policy can both send them an email notification and show them a policy tip in the context of the document library that allows them to override the policy if they have a business justification.</span></span> <span data-ttu-id="c8a05-118">웹, outlook, Excel, PowerPoint 및 Word의 outlook에도 동일한 정책 팁이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-118">The same policy tips also appear in Outlook on the web, Outlook, Excel, PowerPoint, and Word.</span></span>
    
- <span data-ttu-id="c8a05-119">**조직의 dlp 정책과 일치 하는 콘텐츠를 표시 하는 DLP 보고서를 확인 합니다.**</span><span class="sxs-lookup"><span data-stu-id="c8a05-119">**View DLP reports showing content that matches your organization's DLP policies.**</span></span>
    
    <span data-ttu-id="c8a05-120">조직이 DLP 정책을 어떻게 준수하고 있는지를 평가하기 위해 시간에 따른 각 정책 및 규칙의 일치 횟수를 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-120">To assess how your organization is complying with a DLP policy, you can see how many matches each policy and rule has over time.</span></span> <span data-ttu-id="c8a05-121">DLP 정책을 사용 하 여 사용자가 정책 팁을 무시 하 고 가양성을 보고할 수 있는 경우 사용자가 보고 한 내용도 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-121">If a DLP policy allows users to override a policy tip and report a false positive, you can also view what users have reported.</span></span>
    
<span data-ttu-id="c8a05-122">Office 365 보안 &amp; 및 준수 센터의 데이터 손실 방지 페이지에서 DLP 정책을 만들고 관리 합니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-122">You create and manage DLP policies on the Data loss prevention page in the Office 365 Security &amp; Compliance Center.</span></span>
  
![Office 365 보안 &amp; 및 준수 센터의 데이터 손실 방지 페이지](media/943fd01c-d7aa-43a9-846d-0561321a405e.png)
  
## <a name="what-a-dlp-policy-contains"></a><span data-ttu-id="c8a05-124">DLP 정책에 포함된 내용</span><span class="sxs-lookup"><span data-stu-id="c8a05-124">What a DLP policy contains</span></span>

<span data-ttu-id="c8a05-125">DLP 정책에는 다음과 같은 몇 가지 기본적인 사항이 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-125">A DLP policy contains a few basic things:</span></span>
  
- <span data-ttu-id="c8a05-126">Microsoft 팀 채팅 및 채널과 함께 Exchange Online, SharePoint Online 및 비즈니스용 OneDrive 사이트와 같은 콘텐츠 **위치** 를 보호할 수 있는 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-126">Where to protect the content - **locations** such as Exchange Online, SharePoint Online, and OneDrive for Business sites, as well as Microsoft Teams chats and channels.</span></span> 
    
- <span data-ttu-id="c8a05-127">다음을 비롯하여 **규칙**을 적용하여 콘텐츠를 보호하는 경우 및 방법</span><span class="sxs-lookup"><span data-stu-id="c8a05-127">When and how to protect the content by enforcing **rules** comprised of:</span></span> 
    
  - <span data-ttu-id="c8a05-128">규칙을 적용 하기 전에 콘텐츠가 일치 해야 하는 **조건** (예를 들어 조직 외부의 사용자와 공유 하는 사회 보장 번호가 포함 된 콘텐츠만 찾기)</span><span class="sxs-lookup"><span data-stu-id="c8a05-128">**Conditions** the content must match before the rule is enforced -- for example, look only for content containing Social Security numbers that's been shared with people outside your organization.</span></span> 
    
  - <span data-ttu-id="c8a05-129">조건과 일치하는 콘텐츠를 찾을 때 규칙이 자동으로 수행할 **작업**(예를 들어 문서에 대한 액세스를 차단하고 사용자 및 규정 준수 담당자 둘 다에게 전자 메일 알림 전송)</span><span class="sxs-lookup"><span data-stu-id="c8a05-129">**Actions** that you want the rule to take automatically when content matching the conditions is found -- for example, block access to the document and send both the user and compliance officer an email notification.</span></span> 
    
<span data-ttu-id="c8a05-130">규칙을 사용하여 특정 보호 요구 사항을 충족한 다음, DLP 정책을 사용하여 특정 규정을 준수하는 데 필요한 모든 규칙과 같은 일반적인 보호 요구 사항을 그룹화할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-130">You can use a rule to meet a specific protection requirement, and then use a DLP policy to group together common protection requirements, such as all of the rules needed to comply with a specific regulation.</span></span>
  
<span data-ttu-id="c8a05-131">예를 들어 HIPAA(Health Insurance Portability and Accountability Act)가 적용되는 정보의 현재 상태를 확인하는 데 도움이 되는 DLP 정책이 있을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-131">For example, you might have a DLP policy that helps you detect the presence of information subject to the Health Insurance Portability and Accountability Act (HIPAA).</span></span> <span data-ttu-id="c8a05-132">이 DLP 정책은 모든 SharePoint Online 사이트 및 모든 비즈니스용 OneDrive 사이트 (where)에서 조직 외부의 사용자와 공유 하는 모든 문서를 검색 하 여 해당 정보를 보호 하는 데 도움이 될 수 있습니다 ( 조건)을 선택한 다음 문서에 대 한 액세스를 차단 하 고 알림 (작업)을 보냅니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-132">This DLP policy could help protect HIPAA data (the what) across all SharePoint Online sites and all OneDrive for Business sites (the where) by finding any document containing this sensitive information that's shared with people outside your organization (the conditions) and then blocking access to the document and sending a notification (the actions).</span></span> <span data-ttu-id="c8a05-133">이러한 요구 사항은 개별 규칙으로 저장되고, 관리 및 보고를 단순화하기 위해 DLP 정책으로 함께 그룹화됩니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-133">These requirements are stored as individual rules and grouped together as a DLP policy to simplify management and reporting.</span></span>
  
![DLP 정책에 규칙 및 위치를 보여 주는 다이어그램](media/c006860c-2d00-42cb-aaa4-5b5638d139f7.png)
  
### <a name="locations"></a><span data-ttu-id="c8a05-135">위치</span><span class="sxs-lookup"><span data-stu-id="c8a05-135">Locations</span></span>

<span data-ttu-id="c8a05-136">DLP 정책은 해당 정보가 Exchange Online, SharePoint online, 비즈니스용 OneDrive 또는 Microsoft 팀에 있든 관계 없이 Office 365에서 중요 한 정보를 찾고 보호할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-136">A DLP policy can find and protect sensitive information across Office 365, whether that information is located in Exchange Online, SharePoint Online, OneDrive for Business, or Microsoft Teams.</span></span> <span data-ttu-id="c8a05-137">Exchange 전자 메일, Microsoft 팀 채팅 및 채널, 모든 SharePoint 또는 OneDrive 라이브러리의 콘텐츠를 보호 하거나 정책의 특정 위치를 선택 하도록 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-137">You can choose to protect content in Exchange email, Microsoft Teams chats and channels, and all SharePoint or OneDrive libraries, or select specific locations for a policy.</span></span>
  
![DLP 정책을 적용할 수 있는 위치에 대 한 옵션](media/ee50a61a-e867-4571-a150-3eec8d83650f.png)
  
<span data-ttu-id="c8a05-139">특정 SharePoint 사이트 또는 OneDrive 계정을 포함 하거나 제외 하는 경우 DLP 정책에는 포함 및 제외와 같은 100을 초과 하지 않을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-139">Note that if you choose to include or exclude specific SharePoint sites or OneDrive accounts, a DLP policy can contain no more than 100 such inclusions and exclusions.</span></span> <span data-ttu-id="c8a05-140">이 제한이 있는 경우에도 조직 전체 정책이 나 전체 위치에 적용 되는 정책을 적용 하 여이 제한을 초과할 수 있다는 점을 이해 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-140">Although this limit exists, understand that you can exceed this limit by applying either an org-wide policy or a policy that applies to entire locations.</span></span>
  
### <a name="rules"></a><span data-ttu-id="c8a05-141">규칙</span><span class="sxs-lookup"><span data-stu-id="c8a05-141">Rules</span></span>

<span data-ttu-id="c8a05-142">규칙은 조직의 콘텐츠에 대 한 비즈니스 요구 사항을 적용 하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-142">Rules are what enforce your business requirements on your organization's content.</span></span> <span data-ttu-id="c8a05-143">정책은 하나 이상의 규칙을 포함하고 각 규칙은 조건 및 작업을 구성됩니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-143">A policy contains one or more rules, and each rule consists of conditions and actions.</span></span> <span data-ttu-id="c8a05-144">각 규칙에 대해 조건이 충족되면 작업이 자동으로 수행됩니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-144">For each rule, when the conditions are met, the actions are taken automatically.</span></span> <span data-ttu-id="c8a05-145">규칙은 각 정책에서 우선 순위가 가장 높은 규칙부터 시작 하 여 순차적으로 실행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-145">Rules are executed sequentially, starting with the highest-priority rule in each policy.</span></span>
  
<span data-ttu-id="c8a05-146">또한 규칙은 사용자 (정책 팁 및 전자 메일 알림)와 콘텐츠가 규칙과 일치 하는 관리자 (전자 메일 문제 보고서)에 알리는 옵션도 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-146">A rule also provides options to notify users (with policy tips and email notifications) and admins (with email incident reports) that content has matched the rule.</span></span>
  
<span data-ttu-id="c8a05-147">아래에 설명 된 규칙의 구성 요소는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-147">Here are the components of a rule, each explained below.</span></span>
  
![DLP 규칙 편집기 섹션](media/1859d504-b9c2-45ed-961b-a0092251acc2.png)
  
#### <a name="conditions"></a><span data-ttu-id="c8a05-149">조건</span><span class="sxs-lookup"><span data-stu-id="c8a05-149">Conditions</span></span>

<span data-ttu-id="c8a05-150">조건은 찾으려는 정보의 유형과 작업을 수행 해야 하는 경우를 결정 하는 것 이므로 중요 합니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-150">Conditions are important because they determine what types of information you're looking for, and when to take an action.</span></span> <span data-ttu-id="c8a05-151">예를 들어 콘텐츠에 숫자가 10 개 이상 있고 조직 외부의 사용자와 공유 되는 경우가 아니면 passport 번호가 포함 된 콘텐츠를 무시 하도록 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-151">For example, you might choose to ignore content containing passport numbers unless the content contains more than ten such numbers and is shared with people outside your organization.</span></span>
  
<span data-ttu-id="c8a05-152">사용 중인 중요 한 정보 유형, 문서와 공유 하는 사용자 등의 **상황**에 따라 **콘텐츠에**초점을 맞춥니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-152">Conditions focus on the **content**, such as what types of sensitive information you're looking for, and also on the **context**, such as who the document is shared with.</span></span> <span data-ttu-id="c8a05-153">조건을 사용 하 여 다른 위험 수준에 서로 다른 작업을 할당할 수 있습니다. 예를 들어, 내부적으로 공유 되는 중요 한 콘텐츠는 위험 하 고, 조직 외부의 사용자와 공유 되는 중요 한 콘텐츠 보다 더 적은 작업이 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-153">You can use conditions to assign different actions to different risk levels -- for example, sensitive content shared internally might be lower risk and require fewer actions than sensitive content shared with people outside the organization.</span></span> 
  
![사용 가능한 DLP 조건을 표시 하는 목록](media/0fa43f90-d007-4506-ae93-43e8424fe103.png)
  
<span data-ttu-id="c8a05-155">이제 조건을 사용하여 다음과 같은 경우인지 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-155">The conditions now available can determine if:</span></span>
  
- <span data-ttu-id="c8a05-156">콘텐츠에 중요 한 유형의 정보가 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-156">Content contains a type of sensitive information.</span></span>
    
- <span data-ttu-id="c8a05-157">콘텐츠에 레이블이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-157">Content contains a label.</span></span> <span data-ttu-id="c8a05-158">자세한 내용은 아래 섹션에서 [레이블을 DLP 정책의 조건으로 사용](#using-a-label-as-a-condition-in-a-dlp-policy)하십시오.</span><span class="sxs-lookup"><span data-stu-id="c8a05-158">For more information, see the below section [Using a label as a condition in a DLP policy](#using-a-label-as-a-condition-in-a-dlp-policy).</span></span>
    
- <span data-ttu-id="c8a05-159">콘텐츠가 조직 내부 또는 외부 사용자와 공유됩니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-159">Content is shared with people outside or inside your organization.</span></span>
    
#### <a name="types-of-sensitive-information"></a><span data-ttu-id="c8a05-160">중요한 정보 유형</span><span class="sxs-lookup"><span data-stu-id="c8a05-160">Types of sensitive information</span></span>

<span data-ttu-id="c8a05-161">DLP 정책은 중요 한 정보 **유형**으로 정의 된 중요 한 정보를 보호 하는 데 도움이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-161">A DLP policy can help protect sensitive information, which is defined as a **sensitive information type**.</span></span> <span data-ttu-id="c8a05-162">Office 365에는 신용 카드 번호, 은행 계좌 번호, 국가 ID 번호 및 여권 번호 등 사용할 준비가 된 여러 다른 영역에 대한 일반적인 여러 중요 정보 유형에 대한 정의가 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-162">Office 365 includes definitions for many common sensitive information types across many different regions that are ready for you to use, such as a credit card number, bank account numbers, national ID numbers, and passport numbers.</span></span> 
  
![중요 한 정보를 사용할 수 있는 형식 목록](media/3eaa9911-bc94-44be-902f-363dbf3b07fe.png)
  
<span data-ttu-id="c8a05-164">DLP 정책이 신용 카드 번호와 같은 중요 한 정보 유형을 찾을 때 16 자리 숫자는 찾지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-164">When a DLP policy looks for a sensitive information type such as a credit card number, it doesn't simply look for a 16-digit number.</span></span> <span data-ttu-id="c8a05-165">중요한 각 정보 유형은 다음의 조합을 사용해서 정의되고 검색됩니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-165">Each sensitive information type is defined and detected by using a combination of:</span></span>
  
- <span data-ttu-id="c8a05-166">키워드</span><span class="sxs-lookup"><span data-stu-id="c8a05-166">Keywords</span></span>
    
- <span data-ttu-id="c8a05-167">체크섬 또는 구성의 유효성을 검사하기 위한 내부 함수</span><span class="sxs-lookup"><span data-stu-id="c8a05-167">Internal functions to validate checksums or composition</span></span>
    
- <span data-ttu-id="c8a05-168">패턴 일치를 찾기 위한 정규식의 평가</span><span class="sxs-lookup"><span data-stu-id="c8a05-168">Evaluation of regular expressions to find pattern matches</span></span>
    
- <span data-ttu-id="c8a05-169">기타 콘텐츠 검사</span><span class="sxs-lookup"><span data-stu-id="c8a05-169">Other content examination</span></span>
    
<span data-ttu-id="c8a05-170">이렇게 하면 peoples의 작업을 방해할 수 있는 가양성의 수를 줄이면서 DLP 검색에서 높은 수준의 정확성을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-170">This helps DLP detection achieve a high degree of accuracy while reducing the number of false positives that can interrupt peoples' work.</span></span>
  
#### <a name="actions"></a><span data-ttu-id="c8a05-171">동작</span><span class="sxs-lookup"><span data-stu-id="c8a05-171">Actions</span></span>

<span data-ttu-id="c8a05-172">콘텐츠가 규칙의 조건과 일치 하는 경우 작업을 적용 하 여 콘텐츠를 자동으로 보호할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-172">When content matches a condition in a rule, you can apply actions to automatically protect the content.</span></span>
  
![사용 가능한 동작 목록](media/8aef17fc-1e99-4ac7-adfc-0f2c9c1a0697.png)
  
<span data-ttu-id="c8a05-174">이제 사용 가능한 작업을 통해 다음을 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-174">With the actions now available, you can:</span></span>
  
- <span data-ttu-id="c8a05-175">**콘텐츠에 대 한 액세스 제한** 사이트 콘텐츠의 경우 기본 사이트 모음 관리자, 문서 소유자 및 문서를 마지막으로 수정한 사람을 제외한 모든 사용자에 대해 문서에 대 한 사용 권한이 제한 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-175">**Restrict access to the content** For site content, this means that permissions for the document are restricted for everyone except the primary site collection administrator, document owner, and person who last modified the document.</span></span> <span data-ttu-id="c8a05-176">이러한 사람은 문서에서 중요한 정보를 제거하거나 기타 작업을 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-176">These people can remove the sensitive information from the document or take other remedial action.</span></span> <span data-ttu-id="c8a05-177">문서가 규정을 준수하는 경우 원래 권한은 자동으로 복원됩니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-177">When the document is in compliance, the original permissions will be automatically restored.</span></span> <span data-ttu-id="c8a05-178">문서 액세스가 차단되면 사이트의 라이브러리에서 해당 문서에는 특수한 정책 팁 아이콘이 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-178">When access to a document is blocked, the document appears with a special policy tip icon in the library on the site.</span></span> 
    
    ![정책 설명 표시 문서에 대 한 액세스 차단](media/b6cefed3-d212-43d7-8534-4b92b26ebd50.png)
  
    <span data-ttu-id="c8a05-180">전자 메일 콘텐츠의 경우이 동작은 메시지가 전송 되지 않도록 차단 합니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-180">For email content, this action blocks the message from being sent.</span></span> <span data-ttu-id="c8a05-181">DLP 규칙이 구성 된 방법에 따라 보낸 사람은 NDR을 보거나 규칙에서 알림을 사용 하는 경우 정책 팁 및/또는 전자 메일 알림을 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-181">Depending on how the DLP rule is configured, the sender will see an NDR or (if the rule uses a notification) a policy tip and/or email notification.</span></span>
    
    ![인증 되지 않은 받는 사람을 메시지에서 제거 해야 하는 경고](media/302f9994-912d-41e7-861f-8a4539b3c285.png)
  
#### <a name="user-notifications-and-user-overrides"></a><span data-ttu-id="c8a05-183">사용자 알림 및 사용자 재정의</span><span class="sxs-lookup"><span data-stu-id="c8a05-183">User notifications and user overrides</span></span>

<span data-ttu-id="c8a05-184">알림 및 재정의를 사용 하 여 사용자에 게 DLP 정책을 교육 하 고 작업을 차단 하지 않고 계속 준수 하도록 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-184">You can use notifications and overrides to educate your users about DLP policies and help them remain compliant without blocking their work.</span></span> <span data-ttu-id="c8a05-185">예를 들어 사용자가 중요한 정보를 포함하는 문서를 공유하려고 하면 DLP 정책은 전자 메일 알림을 보내고, 업무 정당성이 있을 경우 이 정책을 재정의할 수 있는 문서 라이브러리의 컨텍스트에서 정책 팁을 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-185">For example, if a user tries to share a document containing sensitive information, a DLP policy can both send them an email notification and show them a policy tip in the context of the document library that allows them to override the policy if they have a business justification.</span></span>
  
![DLP 규칙 편집기의 사용자 알림 및 사용자 재정의 섹션](media/37b560d4-6e4e-489e-9134-d4b9daf60296.png)
  
<span data-ttu-id="c8a05-187">전자 메일은 콘텐츠를 전송, 공유 또는 마지막으로 수정한 사람, 사이트 콘텐츠의 경우 주 사이트 모음 관리자 및 문서 소유자에 게 알릴 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-187">The email can notify the person who sent, shared, or last modified the content and, for site content, the primary site collection administrator and document owner.</span></span> <span data-ttu-id="c8a05-188">또한 전자 메일 알림에서 선택한 사용자를 추가 하거나 제거할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-188">In addition, you can add or remove whomever you choose from the email notification.</span></span>
  
<span data-ttu-id="c8a05-189">전자 메일 알림을 보내는 것 외에도 사용자 알림은 정책 팁을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-189">In addition to sending an email notification, a user notification displays a policy tip:</span></span>
  
- <span data-ttu-id="c8a05-190">outlook 및 웹용 outlook</span><span class="sxs-lookup"><span data-stu-id="c8a05-190">In Outlook and Outlook on the web.</span></span>
    
- <span data-ttu-id="c8a05-191">SharePoint Online 또는 비즈니스용 OneDrive 사이트의 문서</span><span class="sxs-lookup"><span data-stu-id="c8a05-191">For the document on a SharePoint Online or OneDrive for Business site.</span></span>
    
- <span data-ttu-id="c8a05-192">Excel, PowerPoint 및 Word의 경우, 문서가 DLP 정책에 포함 된 사이트에 저장 되어 있는 경우</span><span class="sxs-lookup"><span data-stu-id="c8a05-192">In Excel, PowerPoint, and Word, when the document is stored on a site included in a DLP policy.</span></span>
    
<span data-ttu-id="c8a05-193">전자 메일 알림 및 정책 팁에서는 콘텐츠가 DLP 정책과 충돌 하는 이유를 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-193">The email notification and policy tip explain why content conflicts with a DLP policy.</span></span> <span data-ttu-id="c8a05-194">해당 항목을 선택하면 전자 메일 알림 및 정책 팁은 가양성을 보고하거나 업무 정당성을 제공하여 사용자가 규칙을 재정의할 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-194">If you choose, the email notification and policy tip can allow users to override a rule by reporting a false positive or providing a business justification.</span></span> <span data-ttu-id="c8a05-195">이를 통해 사용자에게 DLP 정책을 교육하고, 사람들이 해당 작업을 수행하지 못하도록 하는 방식으로 정책을 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-195">This can help you educate users about your DLP policies and enforce them without preventing people from doing their work.</span></span> <span data-ttu-id="c8a05-196">재정의 및 가양성에 대한 정보는 보고를 위해 기록되고(DLP 보고서에 대해서는 아래 참조) 사고 보고서(다음 섹션 참조)에 포함되므로 규정 준수 책임자는 정기적으로 이 정보를 검토할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-196">Information about overrides and false positives is also logged for reporting (see below about the DLP reports) and included in the incident reports (next section), so that the compliance officer can regularly review this information.</span></span>
  
<span data-ttu-id="c8a05-197">OneDrive for Business 계정의 정책 팁은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-197">Here's what a policy tip looks like in a OneDrive for Business account.</span></span>
  
![OneDrive 계정의 문서에 대 한 정책 팁](media/f9834d35-94f0-4511-8555-0fe69855ce6d.png)
  
#### <a name="incident-reports"></a><span data-ttu-id="c8a05-199">사고 보고서</span><span class="sxs-lookup"><span data-stu-id="c8a05-199">Incident reports</span></span>

<span data-ttu-id="c8a05-200">규칙이 일치 하는 경우 규정 준수 관리자 또는 선택한 모든 사용자에 게 이벤트 세부 정보와 함께 문제 보고서를 보낼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-200">When a rule is matched, you can send an incident report to your compliance officer (or any people you choose) with details of the event.</span></span> <span data-ttu-id="c8a05-201">이 보고서에는 일치 된 항목에 대 한 정보, 해당 규칙과 일치 하는 실제 콘텐츠 및 콘텐츠를 마지막으로 수정한 사용자의 이름이 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-201">This report includes information about the item that was matched, the actual content that matched the rule, and the name of the person who last modified the content.</span></span> <span data-ttu-id="c8a05-202">전자 메일 메시지의 경우 보고서에는 DLP 정책과 일치 하는 원본 메시지의 첨부 파일로도 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-202">For email messages, the report also includes as an attachment the original message that matches a DLP policy.</span></span>
  
![문제 보고서를 구성 하기 위한 페이지](media/31c6da0e-981c-415e-91bf-d94ca391a893.png)
  
## <a name="grouping-and-logical-operators"></a><span data-ttu-id="c8a05-204">그룹화 및 논리 연산자</span><span class="sxs-lookup"><span data-stu-id="c8a05-204">Grouping and logical operators</span></span>

<span data-ttu-id="c8a05-205">종종 DLP 정책에는 미국 주민 등록 번호를 포함 하는 모든 콘텐츠를 식별 하는 것과 같은 간단한 요구 사항이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-205">Often your DLP policy has a straightforward requirement, such as to identify all content that contains a U.S. Social Security Number.</span></span> <span data-ttu-id="c8a05-206">그러나 다른 시나리오에서는 DLP 정책에서 더 느슨하게 정의 된 데이터를 식별 해야 할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-206">However, in other scenarios, your DLP policy might need to identify more loosely defined data.</span></span>
  
<span data-ttu-id="c8a05-207">예를 들어, HIPAA (미국 의료 보험 Act)가 적용 되는 콘텐츠를 확인 하려면 다음 항목을 확인 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-207">For example, to identify content subject to the U.S. Health Insurance Act (HIPAA), you need to look for:</span></span>
  
- <span data-ttu-id="c8a05-208">미국 사회 보장 번호 또는 마약 적용 에이전시 (DEA) 번호와 같은 특정 유형의 중요 한 정보가 포함 된 콘텐츠입니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-208">Content that contains specific types of sensitive information, such as a U.S. Social Security Number or Drug Enforcement Agency (DEA) Number.</span></span>
    
    <span data-ttu-id="c8a05-209">한</span><span class="sxs-lookup"><span data-stu-id="c8a05-209">AND</span></span>
    
- <span data-ttu-id="c8a05-210">제공 되는 의료 서비스에 대 한 환자 관리 또는 설명에 대 한 통신과 같이 식별 하기 어려운 콘텐츠입니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-210">Content that's more difficult to identify, such as communications about a patient's care or descriptions of medical services provided.</span></span> <span data-ttu-id="c8a05-211">이 콘텐츠를 식별 하려면 Diseases의 국제 분류 (ICD-9cm 또는 ICD-10cm)와 같은 매우 큰 키워드 목록의 일치 키워드를 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-211">Identifying this content requires matching keywords from very large keyword lists, such as the International Classification of Diseases (ICD-9-CM or ICD-10-CM).</span></span>
    
<span data-ttu-id="c8a05-212">그룹화 및 논리 연산자 (and, OR)를 사용 하 여 느슨하게 정의 된 데이터를 쉽게 식별할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-212">You can easily identify such loosely defined data by using grouping and logical operators (AND, OR).</span></span> <span data-ttu-id="c8a05-213">DLP 정책을 만들 때 다음을 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-213">When you create a DLP policy, you can:</span></span>
  
- <span data-ttu-id="c8a05-214">중요 한 정보 유형을 그룹화 합니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-214">Group sensitive information types.</span></span>
    
- <span data-ttu-id="c8a05-215">그룹 내의 중요 한 정보 유형과 그룹 자체 간의 논리 연산자를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-215">Choose the logical operator between the sensitive information types within a group and between the groups themselves.</span></span>
    
### <a name="choosing-the-operator-within-a-group"></a><span data-ttu-id="c8a05-216">그룹 내에서 연산자 선택</span><span class="sxs-lookup"><span data-stu-id="c8a05-216">Choosing the operator within a group</span></span>

<span data-ttu-id="c8a05-217">그룹 내에서 해당 그룹의 조건을 규칙과 일치 시키기 위해 충족 해야 하는지 여부를 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-217">Within a group, you can choose whether any or all of the conditions in that group must be satisfied for the content to match the rule.</span></span>
  
![그룹 내의 운영자를 보여 주는 그룹](media/6a12f1e8-112d-48ee-9a73-82b3dd0542e7.png)
  
### <a name="adding-a-group"></a><span data-ttu-id="c8a05-219">그룹 추가</span><span class="sxs-lookup"><span data-stu-id="c8a05-219">Adding a group</span></span>

<span data-ttu-id="c8a05-220">그룹을 빠르게 추가 하 여 해당 그룹 내에 고유한 조건과 연산자를 포함할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-220">You can quickly add a group, which can have its own conditions and operator within that group.</span></span>
  
![그룹 추가 단추](media/5f72f292-d1f3-4f11-a911-a9f71e10abf6.png)
  
### <a name="choosing-the-operator-between-groups"></a><span data-ttu-id="c8a05-222">그룹 간 연산자 선택</span><span class="sxs-lookup"><span data-stu-id="c8a05-222">Choosing the operator between groups</span></span>

<span data-ttu-id="c8a05-223">그룹 간에 콘텐츠를 규칙과 일치 시키려면 한 그룹 또는 모든 그룹의 조건만 충족 해야 하는지 여부를 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-223">Between groups, you can choose whether the conditions in just one group or all of the groups must be satisfied for the content to match the rule.</span></span>
  
<span data-ttu-id="c8a05-224">예를 들어 기본 제공 **미국 HIPAA** 정책에는 다음을 포함 하는 콘텐츠를 식별 하도록 그룹 간에 **AND** 연산자를 사용 하는 규칙이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-224">For example, the built-in **U.S. HIPAA** policy has a rule that uses an **AND** operator between the groups so that it identifies content that contains:</span></span> 
  
- <span data-ttu-id="c8a05-225">**PII 식별자** 그룹 (하나 이상의 SSN 번호 **또는** DEA 번호)</span><span class="sxs-lookup"><span data-stu-id="c8a05-225">from the group **PII Identifiers** (at least one SSN number **OR** DEA number)</span></span> 
    
    <span data-ttu-id="c8a05-226">**한**</span><span class="sxs-lookup"><span data-stu-id="c8a05-226">**AND**</span></span>
    
- <span data-ttu-id="c8a05-227">그룹 **의료 조항** (하나 이상의 ICD-9-cm 키워드나 ICD 키워드) \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="c8a05-227">from the group **Medical Terms** (at least one ICD-9-CM keyword **OR** ICD-10-CM keyword)</span></span> 
    
![그룹 간 운영자를 보여 주는 그룹](media/354aa77f-569c-4847-9dfe-605ee2bb28d1.png)
  
## <a name="the-priority-by-which-rules-are-processed"></a><span data-ttu-id="c8a05-229">규칙이 처리 되는 우선 순위입니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-229">The priority by which rules are processed</span></span>

<span data-ttu-id="c8a05-230">정책에서 규칙을 만들 때 각 규칙의 우선 순위는 생성 되는 순서 대로 지정 되 고, 처음 만든 규칙은 우선 순위가 가장 높습니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-230">When you create rules in a policy, each rule is assigned a priority in the order in which it's created - meaning, the rule created first has first priority, the rule created second has second priority, and so on.</span></span> <span data-ttu-id="c8a05-231">규칙을 만든 후에는 삭제 하 고 다시 만드는 것을 제외 하 고는 해당 우선 순위를 변경할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-231">After you create a rule, its priority can't be changed, except by deleting and re-creating it.</span></span>
  
![규칙을 우선 순위에 정렬 합니다.](media/f7dc06bf-bc6f-485c-bcdb-606edbcf6565.png)
  
<span data-ttu-id="c8a05-233">규칙을 기준으로 콘텐츠를 평가 하는 경우 규칙은 우선 순위에 따라 처리 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-233">When content is evaluated against rules, the rules are processed in priority order.</span></span> <span data-ttu-id="c8a05-234">콘텐츠가 여러 규칙과 일치 하는 경우 규칙은 우선 순위 순으로 처리 되 고 가장 제한적인 작업이 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-234">If content matches multiple rules, the rules are processed in priority order and the most restrictive action is enforced.</span></span> <span data-ttu-id="c8a05-235">예를 들어 콘텐츠가 다음 규칙과 모두 일치 하는 경우 규칙 3은 우선 순위가 가장 높고 가장 제한적인 규칙입니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-235">For example, if content matches all of the following rules, Rule 3 is enforced because it's the highest priority, most restrictive rule:</span></span>
  
- <span data-ttu-id="c8a05-236">규칙 1: 사용자에 게 알림</span><span class="sxs-lookup"><span data-stu-id="c8a05-236">Rule 1: only notifies users</span></span>
    
- <span data-ttu-id="c8a05-237">규칙 2: 사용자에 게 알리고, 액세스를 제한 하 고, 사용자 재정의를 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-237">Rule 2: notifies users, restricts access, and allows user overrides</span></span>
    
- <span data-ttu-id="c8a05-238">규칙 3: 사용자에 게 알리고, 액세스를 제한 하며, 사용자 재정의를 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-238">Rule 3: notifies users, restricts access, and does not allow user overrides</span></span>
    
- <span data-ttu-id="c8a05-239">규칙 4: 사용자에 게 알림</span><span class="sxs-lookup"><span data-stu-id="c8a05-239">Rule 4: only notifies users</span></span>
    
- <span data-ttu-id="c8a05-240">규칙 5: 액세스 제한</span><span class="sxs-lookup"><span data-stu-id="c8a05-240">Rule 5: restricts access</span></span>
    
- <span data-ttu-id="c8a05-241">규칙 6: 사용자에 게 알리고, 액세스를 제한 하며, 사용자 재정의를 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-241">Rule 6: notifies users, restricts access, and does not allow user overrides</span></span>
    
<span data-ttu-id="c8a05-242">이 예에서는 모든 규칙에 대 한 일치가 감사 로그에 기록 되며 가장 제한적인 규칙만 적용 되더라도 DLP 보고서에 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-242">In this example, note that matches for all of the rules are recorded in the audit logs and shown in the DLP reports, even though only the most restrictive rule is enforced.</span></span>
  
<span data-ttu-id="c8a05-243">정책 팁과 관련 하 여 다음 사항을 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-243">With respect to policy tips, note that:</span></span>
  
- <span data-ttu-id="c8a05-244">가장 높은 우선 순위의 정책 팁만 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-244">Only the policy tip from the highest priority, most restrictive rule will be shown.</span></span> <span data-ttu-id="c8a05-245">예를 들어 알림을 콘텐츠 액세스를 차단하는 규칙의 정책 팁은 단순히 알림을 보내는 규칙의 정책 팁보다 우선적으로 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-245">For example, a policy tip from a rule that blocks access to content will be shown over a policy tip from a rule that simply sends a notification.</span></span> <span data-ttu-id="c8a05-246">따라서 정책 팁이 단계별로 표시되지는 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-246">This prevents people from seeing a cascade of policy tips.</span></span>
    
- <span data-ttu-id="c8a05-247">가장 제한적인 규칙의 정책 팁이 사용자의 규칙 재정의를 허용할 경우 이 규칙을 재정의하면 해당 콘텐츠가 일치하는 다른 모든 규칙이 함께 재정의됩니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-247">If the policy tips in the most restrictive rule allow people to override the rule, then overriding this rule also overrides any other rules that the content matched.</span></span>
    
## <a name="tuning-rules-to-make-them-easier-or-harder-to-match"></a><span data-ttu-id="c8a05-248">보다 쉽고 편리 하 게 사용할 수 있는 조정 규칙</span><span class="sxs-lookup"><span data-stu-id="c8a05-248">Tuning rules to make them easier or harder to match</span></span>

<span data-ttu-id="c8a05-249">사용자가 DLP 정책을 만들고 켠 후에는 다음과 같은 문제가 발생할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-249">After people create and turn on their DLP policies, they sometimes run into these issues:</span></span>
  
- <span data-ttu-id="c8a05-250">중요 한 정보가 **아닌** 콘텐츠가 규칙과 일치 하는 경우 (즉, 가양성이 너무 많음)</span><span class="sxs-lookup"><span data-stu-id="c8a05-250">Too much content that **is not** sensitive information matches the rules - in other words, too many false positives.</span></span> 
    
- <span data-ttu-id="c8a05-251">중요 한 정보가 규칙과 \*\*\*\* 일치 하는 콘텐츠가 너무 적으면 중요 한 정보에는 보호 작업이 적용 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-251">Too little content that **is** sensitive information matches the rules - in other words, the protective actions aren't being enforced on the sensitive information.</span></span> 
    
<span data-ttu-id="c8a05-252">이러한 문제를 해결 하기 위해 인스턴스 수와 일치 정확도를 조정 하 여 규칙을 조정 하면 콘텐츠를 규칙과 일치 시킬 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-252">To address these issues, you can tune your rules by adjusting the instance count and match accuracy to make it harder or easier for content to match the rules.</span></span> <span data-ttu-id="c8a05-253">규칙에 사용 되는 각 중요 한 정보 유형에는 인스턴스 수와 일치 정확도가 모두 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-253">Each sensitive information type used in a rule has both an instance count and match accuracy.</span></span>
  
### <a name="instance-count"></a><span data-ttu-id="c8a05-254">인스턴스 수</span><span class="sxs-lookup"><span data-stu-id="c8a05-254">Instance count</span></span>

<span data-ttu-id="c8a05-255">인스턴스 수는 해당 규칙과 일치 하는 콘텐츠에 대해 제공 해야 하는 특정 유형의 중요 한 정보 발생 수를 의미 합니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-255">Instance count means simply how many occurrences of a specific type of sensitive information must be present for content to match the rule.</span></span> <span data-ttu-id="c8a05-256">예를 들어, 1 ~ 9 고유 미국 또는 영국 사이에 있는 경우 콘텐츠는 아래와 같이 표시 된 규칙과 일치 합니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-256">For example, content will match the rule shown below if between 1 and 9 unique U.S. or U.K.</span></span> <span data-ttu-id="c8a05-257">passport 번호가 식별 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-257">passport numbers are identified.</span></span>
  
<span data-ttu-id="c8a05-258">인스턴스 수에는 중요 한 정보 유형 및 키워드에 대 한 **고유** 일치만 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-258">Note that the instance count includes only **unique** matches for sensitive information types and keywords.</span></span> <span data-ttu-id="c8a05-259">예를 들어 전자 메일에 동일한 신용 카드 번호가 10 번 포함 되어 있는 경우 10 개 항목이 신용 카드 번호의 단일 인스턴스로 계산 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-259">For example, if an email contains 10 occurrences of the same credit card number, those 10 occurrences count as a single instance of a credit card number.</span></span> 
  
<span data-ttu-id="c8a05-260">인스턴스 수를 사용 하 여 규칙을 조정 하려면 다음과 같은 지침이 단순 합니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-260">To use instance count to tune rules, the guidance is straightforward:</span></span>
  
- <span data-ttu-id="c8a05-261">규칙을 보다 쉽게 찾을 수 있도록 **최소** 개수를 줄이거나 **최대** 개수를 늘립니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-261">To make the rule easier to match, decrease the **min** count and/or increase the **max** count.</span></span> <span data-ttu-id="c8a05-262">숫자 값을 삭제 하 여 \*\*\*\* **max** 로 설정할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-262">You can also set **max** to **any** by deleting the numerical value.</span></span> 
    
- <span data-ttu-id="c8a05-263">규칙 일치가 더 어렵게 하려면 **최소** 개수를 늘립니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-263">To make the rule harder to match, increase the **min** count.</span></span> 
    
<span data-ttu-id="c8a05-264">일반적으로 인스턴스 수가 낮은 규칙 (예: 1-9)에는 사용자 알림 보내기와 같은 덜 제한적인 작업을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-264">Typically, you use less restrictive actions, such as sending user notifications, in a rule with a lower instance count (for example, 1-9).</span></span> <span data-ttu-id="c8a05-265">또한 사용자 재정의를 허용 하지 않고 콘텐츠에 대 한 액세스를 제한 하는 것과 같은 더 제한적인 작업을 사용 하는 경우 인스턴스 수가 더 높은 규칙 (예: 10 개)</span><span class="sxs-lookup"><span data-stu-id="c8a05-265">And you use more restrictive actions, such as restricting access to content without allowing user overrides, in a rule with a higher instance count (for example, 10-any).</span></span>
  
![규칙 편집기의 인스턴스 수](media/e7ea3c12-72c5-4bb3-9590-c924c665e84d.png)
  
### <a name="match-accuracy"></a><span data-ttu-id="c8a05-267">정확도 일치</span><span class="sxs-lookup"><span data-stu-id="c8a05-267">Match accuracy</span></span>

<span data-ttu-id="c8a05-268">위에서 설명한 것 처럼 중요 한 정보 유형은 서로 다른 유형의 증명을 조합 하 여 정의 되 고 검색 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-268">As described above, a sensitive information type is defined and detected by using a combination of different types of evidence.</span></span> <span data-ttu-id="c8a05-269">일반적으로 중요 한 정보 유형은 패턴 이라는 여러 조합에 의해 정의 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-269">Commonly, a sensitive information type is defined by multiple such combinations, called patterns.</span></span> <span data-ttu-id="c8a05-270">보다 적은 증거를 필요로 하는 패턴의 경우 일치 하는 정확도 (또는 신뢰 수준)가 더 높고 자세한 증거를 필요로 하는 패턴의 경우 일치 하는 정확도 (또는 신뢰 수준)가 더 높은 것입니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-270">A pattern that requires less evidence has a lower match accuracy (or confidence level), while a pattern that requires more evidence has a higher match accuracy (or confidence level).</span></span> <span data-ttu-id="c8a05-271">모든 중요 한 정보 유형에 서 사용 되는 실제 패턴 및 신뢰 수준에 대 한 자세한 내용은 [중요 한 정보 유형이 찾는 항목](what-the-sensitive-information-types-look-for.md)을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="c8a05-271">To learn more about the actual patterns and confidence levels used by every sensitive information type, see [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
<span data-ttu-id="c8a05-272">예를 들어 신용 카드 번호 라는 중요 한 정보 유형은 다음과 같은 두 가지 패턴으로 정의 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-272">For example, the sensitive information type named Credit Card Number is defined by two patterns:</span></span>
  
- <span data-ttu-id="c8a05-273">다음 요구 사항이 충족 되는 65% 신뢰도가 있는 패턴</span><span class="sxs-lookup"><span data-stu-id="c8a05-273">A pattern with 65% confidence that requires:</span></span>
    
  - <span data-ttu-id="c8a05-274">신용 카드 번호 형식의 숫자입니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-274">A number in the format of a credit card number.</span></span>
    
  - <span data-ttu-id="c8a05-275">체크섬을 통과 하는 숫자입니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-275">A number that passes the checksum.</span></span>
    
- <span data-ttu-id="c8a05-276">다음 요구 사항이 충족 되는 85% 신뢰도가 있는 패턴</span><span class="sxs-lookup"><span data-stu-id="c8a05-276">A pattern with 85% confidence that requires:</span></span>
    
  - <span data-ttu-id="c8a05-277">신용 카드 번호 형식의 숫자입니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-277">A number in the format of a credit card number.</span></span>
    
  - <span data-ttu-id="c8a05-278">체크섬을 통과 하는 숫자입니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-278">A number that passes the checksum.</span></span>
    
  - <span data-ttu-id="c8a05-279">올바른 형식의 키워드나 만료 날짜입니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-279">A keyword or an expiration date in the right format.</span></span>
    
<span data-ttu-id="c8a05-280">규칙에서 이러한 신뢰 수준 (또는 정확성 일치)을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-280">You can use these confidence levels (or match accuracy) in your rules.</span></span> <span data-ttu-id="c8a05-281">일반적으로 일치 정확도가 낮은 규칙에서 사용자 알림 보내기와 같은 덜 제한적인 작업을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-281">Typically, you use less restrictive actions, such as sending user notifications, in a rule with lower match accuracy.</span></span> <span data-ttu-id="c8a05-282">또한 사용자 재정의를 허용 하지 않고 콘텐츠에 대 한 액세스를 제한 하는 것과 같은 더 제한적인 작업을 사용 하는 것은 일치 하는 정확도가 더 높은 규칙입니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-282">And you use more restrictive actions, such as restricting access to content without allowing user overrides, in a rule with higher match accuracy.</span></span>
  
<span data-ttu-id="c8a05-283">신용 카드 번호와 같은 특정 유형의 중요 한 정보가 콘텐츠에서 식별 되 면 단일 신뢰 수준만 반환 되는 것을 이해 하는 것이 중요 합니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-283">It's important to understand that when a specific type of sensitive information, such as a credit card number, is identified in content, only a single confidence level is returned:</span></span>
  
- <span data-ttu-id="c8a05-284">모든 일치 항목이 단일 패턴에 대 한 것 이면 해당 패턴의 신뢰 수준이 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-284">If all of the matches are for a single pattern, the confidence level for that pattern is returned.</span></span>
    
- <span data-ttu-id="c8a05-285">두 개 이상의 패턴에 대해 일치 하는 것이 있는 경우 (즉 서로 다른 신뢰 수준과 일치 하는 일치가 있는 경우) 단일 패턴에 비해 신뢰도 수준이 높은 것이 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-285">If there are matches for more than one pattern (i.e., there are matches with two different confidence levels), a confidence level higher than any of the single patterns alone is returned.</span></span> <span data-ttu-id="c8a05-286">이는 까다로운 부분입니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-286">This is the tricky part.</span></span> <span data-ttu-id="c8a05-287">예를 들어 신용 카드에서 65%와 85% 패턴이 모두 일치 하는 경우, 더 많은 증거가 있다는 것을 의미 하기 때문에 해당 중요 한 정보 유형에 대해 반환 되는 신뢰 수준은 90% 보다 큽니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-287">For example, for a credit card, if both the 65% and 85% patterns are matched, the confidence level returned for that sensitive information type is greater than 90% because more evidence means more confidence.</span></span>
    
<span data-ttu-id="c8a05-288">따라서 신용 카드에 대해 두 개의 상호 배타적인 규칙을 만들고, 65% 일치 정확성을 확인 하 고, 85% 일치 정확성을 사용할 경우 일치 하는 항목의 범위는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-288">So if you want to create two mutually exclusive rules for credit cards, one for the 65% match accuracy and one for the 85% match accuracy, the ranges for match accuracy would look like this.</span></span> <span data-ttu-id="c8a05-289">첫 번째 규칙은 65% 패턴과 일치 하는 항목만 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-289">The first rule picks up only matches of the 65% pattern.</span></span> <span data-ttu-id="c8a05-290">두 번째 규칙은 **하나 이상의** 85% 일치 항목과 일치 하 고 더 낮은 신뢰도 일치를 **가질 수 있습니다** .</span><span class="sxs-lookup"><span data-stu-id="c8a05-290">The second rule picks up matches with **at least one** 85% match and **can potentially have** other lower-confidence matches.</span></span> 
  
![서로 다른 범위가 포함 된 두 규칙 (정확성 일치)](media/21bdfe36-7a91-4347-8098-11809a92f9a4.png)
  
<span data-ttu-id="c8a05-292">이와 같은 이유로, 서로 다른 match accuracies를 사용 하 여 규칙을 만드는 지침은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-292">For these reasons, the guidance for creating rules with different match accuracies is:</span></span>
  
- <span data-ttu-id="c8a05-293">신뢰도가 가장 낮은 수준에는 일반적으로 범위가 아닌 **최소값** 및 **최대값** 에 같은 값이 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-293">The lowest confidence level typically uses the same value for **min** and **max** (not a range).</span></span> 
    
- <span data-ttu-id="c8a05-294">신뢰도가 가장 높은 수준은 일반적으로 낮은 신뢰도 수준에서 100 까지의 범위입니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-294">The highest confidence level is typically a range from just above the lower confidence level to 100.</span></span>
    
- <span data-ttu-id="c8a05-295">신뢰할 수 있는 신뢰 수준 간의 범위는 일반적으로 낮은 신뢰 수준 바로 아래에서 높은 신뢰도 수준 바로 아래 까지입니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-295">Any in-between confidence levels typically range from just above the lower confidence level to just below the higher confidence level.</span></span>
    
## <a name="using-a-label-as-a-condition-in-a-dlp-policy"></a><span data-ttu-id="c8a05-296">레이블을 DLP 정책의 조건으로 사용</span><span class="sxs-lookup"><span data-stu-id="c8a05-296">Using a label as a condition in a DLP policy</span></span>

<span data-ttu-id="c8a05-297">레이블을 만든 후 다음을 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-297">You can create a label and then:</span></span>
  
- <span data-ttu-id="c8a05-298">최종 사용자가 콘텐츠에 레이블을 표시 하 고 콘텐츠를 수동으로 적용할 수 있도록 **게시** 합니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-298">**Publish** it, so that end users can see and manually apply the label to content.</span></span> 
    
- <span data-ttu-id="c8a05-299">선택한 조건과 일치 하는 콘텐츠에 **자동으로 적용** 합니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-299">**Auto-apply** it to content that matches the conditions that you choose.</span></span> 
    
<span data-ttu-id="c8a05-300">레이블에 대 한 자세한 내용은 [보존 레이블 개요](labels.md)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="c8a05-300">For more information about labels, see [Overview of retention labels](labels.md).</span></span>
  
<span data-ttu-id="c8a05-301">레이블을 만든 후에는 해당 레이블을 DLP 정책의 조건으로 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-301">After you create a label, you can then use that label as a condition in your DLP policies.</span></span> <span data-ttu-id="c8a05-302">예를 들어 다음과 같은 이유로이 작업을 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-302">For example, you might want to do this because:</span></span>
  
- <span data-ttu-id="c8a05-303">조직의 사용자가 기밀 전자 메일 및 문서에 레이블을 수동으로 적용할 수 있도록 **기밀**이라는 레이블을 게시 했습니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-303">You published a label named **Confidential**, so that people in your organization can manually apply the label to confidential email and documents.</span></span> <span data-ttu-id="c8a05-304">이 레이블을 DLP 정책의 조건으로 사용 하 여 **기밀** 을 유지 하는 콘텐츠를 조직 외부의 사용자와 공유 하지 못하도록 제한할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-304">By using this label as a condition in your DLP policy, you can restrict content labeled **Confidential** from being shared with people outside your organization.</span></span> 
    
- <span data-ttu-id="c8a05-305">해당 이름의 프로젝트에 대해 **알파인 house** 라는 레이블을 만든 다음 해당 레이블을 "알파인 집" 이라는 키워드가 포함 된 콘텐츠에 자동으로 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-305">You created a label named **Alpine House** for a project of that name, and then applied that label automatically to content containing the keywords "Alpine House".</span></span> <span data-ttu-id="c8a05-306">이 레이블을 DLP 정책의 조건으로 사용 하 여이 콘텐츠를 조직 외부의 사용자와 공유 하려고 할 때 최종 사용자에 게 정책 팁을 표시할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-306">By using this label as a condition in your DLP policy, you can show a policy tip to end users when they're about to share this content with someone outside your organization.</span></span> 
    
- <span data-ttu-id="c8a05-307">레코드 관리자가 레코드를 분류 해야 하는 콘텐츠에 레이블을 수동으로 적용할 수 있도록 **세금 레코드**라는 레이블을 게시 했습니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-307">You published a label named **Tax record**, so that your records manager can manually apply the label to content that needs to be classified as a record.</span></span> <span data-ttu-id="c8a05-308">이 레이블을 DLP 정책의 조건으로 사용 하 여 itins 또는 ssns와 같은 기타 유형의 중요 한 정보와 함께이 레이블로 콘텐츠를 찾을 수 있습니다. **세금 기록**이라는 콘텐츠에 보호 작업을 적용 합니다. 그리고 dlp 보고서 및 감사 로그 데이터에서 dlp 정책에 대 한 자세한 활동 보고서를 확인 하세요.</span><span class="sxs-lookup"><span data-stu-id="c8a05-308">By using this label as a condition in your DLP policy, you can look for content with this label in conjunction with other types of sensitive information such as ITINs or SSNs; apply protection actions to content labeled **Tax record**; and get detailed activity reports about the DLP policy from the DLP reports and audit log data.</span></span> 
    
- <span data-ttu-id="c8a05-309">**Executive 리더십 팀 구분** 이라는 레이블을 Exchange 사서함 및 임원 그룹의 OneDrive 계정에 게시 했습니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-309">You published a label named **Executive Leadership Team - Sensitive** to the Exchange mailboxes and OneDrive accounts of a group of executives.</span></span> <span data-ttu-id="c8a05-310">이 레이블을 DLP 정책의 조건으로 사용 하 여 동일한 콘텐츠 및 사용자 하위 집합에 대해 보존 및 보호 작업을 둘 다 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-310">By using this label as a condition in your DLP policy, you can enforce both retention and protection actions on the same subset of content and users.</span></span> 
    
<span data-ttu-id="c8a05-311">DLP 규칙의 조건으로 레이블을 사용 하 여 특정 콘텐츠, 위치 또는 사용자 집합에 대해 선택적으로 보호 작업을 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-311">By using labels as a condition in your DLP rules, can you selectively enforce protection actions on a specific set of content, locations, or users.</span></span>
  
![조건으로 레이블](media/5b1752b4-a129-4a88-b010-8dcf8a38bb09.png)

### <a name="support-for-sensitivity-labels-is-coming"></a><span data-ttu-id="c8a05-313">민감도 레이블이 지원 됨</span><span class="sxs-lookup"><span data-stu-id="c8a05-313">Support for sensitivity labels is coming</span></span>

<span data-ttu-id="c8a05-314">현재 보존 레이블만 [우편물 종류 레이블이](sensitivity-labels.md)아닌 조건으로 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-314">Note that you can currently use only a retention label as a condition, not a [sensitivity label](sensitivity-labels.md).</span></span> <span data-ttu-id="c8a05-315">현재이 조건에서 민감도 레이블 사용을 지원 하 고 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-315">We're currently working on support for using a sensitivity label in this condition.</span></span>
  
### <a name="how-this-feature-relates-to-other-features"></a><span data-ttu-id="c8a05-316">이 기능이 다른 기능과 어떤 관련이 있는지를 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-316">How this feature relates to other features</span></span>

<span data-ttu-id="c8a05-317">중요 한 정보가 포함 된 콘텐츠에는 다음과 같은 몇 가지 기능이 적용 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-317">Several features can be applied to content containing sensitive information:</span></span>
  
- <span data-ttu-id="c8a05-318">[보존 레이블과](labels.md#applying-a-retention-label-automatically-based-on-conditions) [보존 정책은](retention-policies.md) 모두이 콘텐츠에 대해 **보존** 작업을 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-318">A [retention label](labels.md#applying-a-retention-label-automatically-based-on-conditions) and a [retention policy](retention-policies.md) can both enforce **retention** actions on this content.</span></span> 
    
- <span data-ttu-id="c8a05-319">DLP 정책은이 콘텐츠에 대 한 **보호** 작업을 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-319">A DLP policy can enforce **protection** actions on this content.</span></span> <span data-ttu-id="c8a05-320">이러한 작업을 적용 하기 전에 먼저 DLP 정책을 통해 레이블이 포함 된 콘텐츠 외에 다른 조건이 충족 되도록 해야 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-320">And before enforcing these actions, a DLP policy can require other conditions to be met in addition to the content containing a label.</span></span> 
    
![중요 한 정보에 적용할 수 있는 기능 다이어그램](media/dd410f97-a3a3-455c-a1e9-7ed8ae6893d6.png)
  
<span data-ttu-id="c8a05-322">DLP 정책은 중요 한 정보에 적용 되는 레이블 또는 보존 정책 보다 더 다양 한 검색 기능을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-322">Note that a DLP policy has a richer detection capability than a label or retention policy applied to sensitive information.</span></span> <span data-ttu-id="c8a05-323">DLP 정책은 중요 한 정보가 포함 된 콘텐츠에 대 한 보호 작업을 적용할 수 있으며, 중요 한 정보를 콘텐츠에서 제거 하면 다음에 콘텐츠를 검색할 때 해당 보호 작업이 취소 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-323">A DLP policy can enforce protective actions on content containing sensitive information, and if the sensitive information is removed from the content, those protective actions are undone the next time the content's scanned.</span></span> <span data-ttu-id="c8a05-324">그러나 중요 한 정보가 포함 된 콘텐츠에 보존 정책이 나 레이블을 적용 하는 경우에는 중요 한 정보가 제거 되어도 실행 취소 되지 않는 일회성 동작이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-324">But if a retention policy or label is applied to content containing sensitive information, that's a one-time action that won't be undone even if the sensitive information's removed.</span></span>
  
<span data-ttu-id="c8a05-325">레이블을 DLP 정책의 조건으로 사용 하면 해당 레이블을 사용 하 여 콘텐츠에 대 한 보존 및 보호 작업을 둘 다 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-325">By using a label as a condition in a DLP policy, you can enforce both retention and protection actions on content with that label.</span></span> <span data-ttu-id="c8a05-326">중요 한 정보가 포함 된 콘텐츠 (레이블 및 중요 한 정보 유형 모두)가 콘텐츠를 분류 하는 데 사용 되는 속성 이기 때문에 해당 콘텐츠에 대해 작업을 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-326">You can think of content containing a label exactly like content containing sensitive information - both a label and a sensitive information type are properties used to classify content, so that you can enforce actions on that content.</span></span>
  
![레이블을 조건으로 사용 하는 DLP 정책 다이어그램](media/4538fd8f-fb74-4743-bc22-a5de33adfebb.png)
  
## <a name="simple-settings-vs-advanced-settings"></a><span data-ttu-id="c8a05-328">단순 설정 및 고급 설정 비교</span><span class="sxs-lookup"><span data-stu-id="c8a05-328">Simple settings vs. advanced settings</span></span>

<span data-ttu-id="c8a05-329">DLP 정책을 만들 때 simple 또는 advanced 설정 중에서 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-329">When you create a DLP policy, you'll choose between simple or advanced settings:</span></span>
  
- <span data-ttu-id="c8a05-330">**간단한 설정을** 통해 규칙 편집기를 사용 하지 않고 규칙을 만들거나 수정 하는 방법으로 가장 일반적인 유형의 DLP 정책을 쉽게 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-330">**Simple settings** make it easy to create the most common type of DLP policy without using the rule editor to create or modify rules.</span></span> 
    
- <span data-ttu-id="c8a05-331">**고급 설정** 규칙 편집기를 사용 하 여 DLP 정책의 모든 설정을 완벽 하 게 제어할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-331">**Advanced settings** use the rule editor to give you complete control over every setting for your DLP policy.</span></span> 
    
<span data-ttu-id="c8a05-332">조건 및 작업에 영향을 주는 규칙을 적용 하 여 규칙 편집기를 볼 수는 있지만,이 경우에도 마찬가지로, 단순 설정 및 고급 설정은 정확히 동일 하 게 작동 합니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-332">Don't worry, under the covers, simple settings and advanced settings work exactly the same, by enforcing rules comprised of conditions and actions -- only with simple settings, you don't see the rule editor.</span></span> <span data-ttu-id="c8a05-333">이는 DLP 정책을 만드는 빠른 방법입니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-333">It's a quick way to create a DLP policy.</span></span>
  
### <a name="simple-settings"></a><span data-ttu-id="c8a05-334">단순 설정</span><span class="sxs-lookup"><span data-stu-id="c8a05-334">Simple settings</span></span>

<span data-ttu-id="c8a05-335">지금까지 가장 일반적인 DLP 시나리오는 중요 한 정보가 포함 된 콘텐츠를 조직 외부의 사용자와 공유 하는 것을 방지 하 고 콘텐츠에 액세스할 수 있는 사람을 제한 하는 등의 자동 해결 작업을 수행 하는 정책을 만드는 것입니다. 최종 사용자 또는 관리자 알림을 보내며 나중에 조사를 위해 이벤트를 감사 합니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-335">By far, the most common DLP scenario is creating a policy to help protect content containing sensitive information from being shared with people outside your organization, and taking an automatic remedial action such as restricting who can access the content, sending end-user or admin notifications, and auditing the event for later investigation.</span></span> <span data-ttu-id="c8a05-336">사용자는 DLP를 사용 하 여 중요 한 정보가 실수로 공개 되지 않도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-336">People use DLP to help prevent the inadvertent disclosure of sensitive information.</span></span>
  
<span data-ttu-id="c8a05-337">이러한 목표를 단순화 하기 위해 DLP 정책을 만들 때 **단순 설정 사용**을 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-337">To simplify achieving this goal, when you create a DLP policy, you can choose **Use simple settings**.</span></span> <span data-ttu-id="c8a05-338">이러한 설정은 규칙 편집기로 이동 하지 않고도 가장 일반적인 DLP 정책을 구현 하는 데 필요한 모든 항목을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-338">These settings provide everything you need to implement the most common DLP policy, without having to go into the rule editor.</span></span>
  
![단순 및 고급 설정에 대 한 DLP 옵션](media/33c93824-ead5-43b6-9c3e-fd1630c92a7d.png)
  
### <a name="advanced-settings"></a><span data-ttu-id="c8a05-340">고급 설정</span><span class="sxs-lookup"><span data-stu-id="c8a05-340">Advanced settings</span></span>

<span data-ttu-id="c8a05-341">사용자 지정 된 DLP 정책을 더 만들어야 하는 경우에는 **고급 설정 사용**을 선택 하면 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-341">If you need to create more customized DLP policies, you can choose **Use advanced settings**.</span></span>
  
<span data-ttu-id="c8a05-342">고급 설정에는 각 규칙에 대 한 인스턴스 수 및 일치 정확도 (신뢰 수준)를 비롯 하 여 모든 가능한 옵션에 대 한 모든 권한이 있는 규칙 편집기가 제공 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-342">The advanced settings present you with the rule editor, where you have full control over every possible option, including the instance count and match accuracy (confidence level) for each rule.</span></span>
  
<span data-ttu-id="c8a05-343">섹션으로 빠르게 이동 하려면 위쪽 탐색 모음에서 항목을 클릭 하 여 아래의 해당 섹션으로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-343">To jump to a section quickly, click an item in the top navigation of the rule editor to go to that section below.</span></span>
  
![DLP 규칙 편집기의 위쪽 탐색 메뉴](media/c527b97f-ca53-4c79-ad19-1a63be8a8ecc.png)
  
## <a name="dlp-policy-templates"></a><span data-ttu-id="c8a05-345">DLP 정책 템플릿</span><span class="sxs-lookup"><span data-stu-id="c8a05-345">DLP policy templates</span></span>

<span data-ttu-id="c8a05-346">DLP 정책을 만드는 첫 번째 단계는 보호할 정보를 선택 하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-346">The first step in creating a DLP policy is choosing what information to protect.</span></span> <span data-ttu-id="c8a05-347">DLP 서식 파일로 시작 하 여 새 규칙 집합을 처음부터 새로 작성 하 고, 기본적으로 포함 될 정보 유형을 파악 합니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-347">By starting with a DLP template, you save the work of building a new set of rules from scratch, and figuring out which types of information should be included by default.</span></span> <span data-ttu-id="c8a05-348">그런 다음 이러한 요구 사항을 추가 하거나 수정 하 여 조직의 특정 요구 사항에 맞게 규칙을 미세 조정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-348">You can then add to or modify these requirements to fine tune the rule to meet your organization's specific requirements.</span></span>
  
<span data-ttu-id="c8a05-349">미리 구성 된 DLP 정책 템플릿을 사용 하면 HIPAA 데이터, 금융-gramm-leach-bliley-gramm-leach-bliley Act 데이터, 심지어 로캘별 개인 식별 정보 (P.I.)와 같은 특정 유형의 중요 한 정보를 쉽게 검색할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-349">A preconfigured DLP policy template can help you detect specific types of sensitive information, such as HIPAA data, PCI-DSS data, Gramm-Leach-Bliley Act data, or even locale-specific personally identifiable information (P.I.).</span></span> <span data-ttu-id="c8a05-350">일반적인 유형의 중요한 정보를 쉽게 찾아 보호할 수 있도록 하기 위해 Office 365에 포함된 정책 템플릿에는 이미 시작하는 데 필요한 가장 일반적인 중요한 정보 유형이 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-350">To make it easy for you to find and protect common types of sensitive information, the policy templates included in Office 365 already contain the most common sensitive information types necessary for you to get started.</span></span>
  
![미국용 템플릿이 포커스가 있는 데이터 손실 방지 정책에 대한 템플릿 목록 애국법](media/791b2403-430b-4987-8643-cc20abbd8148.png)
  
<span data-ttu-id="c8a05-352">조직에는 고유한 특정 요구 사항이 있을 수 있으며,이 경우 **사용자 지정 정책** 옵션을 선택 하 여 DLP 정책을 처음부터 새로 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-352">Your organization may also have its own specific requirements, in which case you can create a DLP policy from scratch by choosing the **Custom policy** option.</span></span> <span data-ttu-id="c8a05-353">사용자 지정 정책은 비어 있고 premade 규칙이 포함 되어 있지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-353">A custom policy is empty and contains no premade rules.</span></span> 
  
## <a name="roll-out-dlp-policies-gradually-with-test-mode"></a><span data-ttu-id="c8a05-354">테스트 모드를 사용하여 점차적으로 DLP 정책 롤아웃</span><span class="sxs-lookup"><span data-stu-id="c8a05-354">Roll out DLP policies gradually with test mode</span></span>

<span data-ttu-id="c8a05-355">DLP 정책을 만든 후에는 완전히 적용하기 전에 서서히 롤아웃하면서 영향을 평가하고 효율성을 테스트하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-355">When you create your DLP policies, you should consider rolling them out gradually to assess their impact and test their effectiveness before fully enforcing them.</span></span> <span data-ttu-id="c8a05-356">예를 들어 사용자가 작업을 완료 하기 위해 액세스 해야 하는 수천 개의 문서에 대 한 액세스를 새 DLP 정책에서 실수로 차단 하는 것을 원하지 않을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-356">For example, you don't want a new DLP policy to unintentionally block access to thousands of documents that people require access to in order to get their work done.</span></span>
  
<span data-ttu-id="c8a05-357">잠재적으로 큰 영향을 주는 DLP 정책을 만드는 경우에는 다음 순서를 따르는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-357">If you're creating DLP policies with a large potential impact, we recommend following this sequence:</span></span>
  
1. <span data-ttu-id="c8a05-358">**정책 설명이 없는 테스트 모드로 시작한** 다음 DLP 보고서 및 모든 문제 보고서를 사용 하 여 영향을 평가 합니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-358">**Start in test mode without Policy Tips** and then use the DLP reports and any incident reports to assess the impact.</span></span> <span data-ttu-id="c8a05-359">DLP 보고서를 사용하여 정책 일치의 횟수, 위치, 유형 및 심각도를 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-359">You can use DLP reports to view the number, location, type, and severity of policy matches.</span></span> <span data-ttu-id="c8a05-360">결과에 따라 필요에 맞게 규칙을 미세 조정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-360">Based on the results, you can fine tune the rules as needed.</span></span> <span data-ttu-id="c8a05-361">테스트 모드에서 DLP 정책은 조직에서 작업하는 사용자의 생산성에 영향을 주지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-361">In test mode, DLP policies will not impact the productivity of people working in your organization.</span></span> 
    
2. <span data-ttu-id="c8a05-p152">**알림 및 정책 팁을 사용하여 테스트 모드로 전환**하여 사용자에게 규정 준수 정책을 교육하고 적용될 규칙을 준비하도록 할 수 있습니다. 이 단계에서 규칙을 미세 조정할 수 있도록 사용자에게 가양성을 보고하도록 요청할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-p152">**Move to Test mode with notifications and Policy Tips** so that you can begin to teach users about your compliance policies and prepare them for the rules that are going to be applied. At this stage, you can also ask users to report false positives so that you can further refine the rules.</span></span> 
    
3. <span data-ttu-id="c8a05-364">규칙의 작업이 적용 되 고 콘텐츠가 보호 되도록 **정책에 대 한 전체 적용을 시작** 합니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-364">**Start full enforcement on the policies** so that the actions in the rules are applied and the content's protected.</span></span> <span data-ttu-id="c8a05-365">DLP 보고서 및 문제 보고서나 알림을 계속 모니터링하여 결과가 의도한 대로 나타나는지 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-365">Continue to monitor the DLP reports and any incident reports or notifications to make sure that the results are what you intend.</span></span> 
    
![테스트 모드를 사용 하 여 정책 설정에 대 한 옵션](media/49fafaac-c6cb-41de-99c4-c43c3e380c3a.png)
  
<span data-ttu-id="c8a05-367">언제든지 정책의 모든 규칙에 적용되는 DLP 정책을 끌 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-367">You can turn off a DLP policy at any time, which affects all rules in the policy.</span></span> <span data-ttu-id="c8a05-368">그러나 규칙 편집기에서 상태를 전환 하 여 각 규칙을 개별적으로 끌 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-368">However, each rule can also be turned off individually by toggling its status in the rule editor.</span></span>
  
![정책에서 규칙을 해제 하는 것에 대 한 옵션](media/f7b258ff-1b8b-4127-b580-83c6492f2bef.png)
  
## <a name="dlp-reports"></a><span data-ttu-id="c8a05-370">DLP 보고서</span><span class="sxs-lookup"><span data-stu-id="c8a05-370">DLP reports</span></span>

<span data-ttu-id="c8a05-371">DLP 정책을 만들고 켠 후에는 해당 정책이 의도 한 대로 작동 하 고 준수 상태를 유지 하도록 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-371">After you create and turn on your DLP policies, you'll want to verify that they're working as you intended and helping you stay compliant.</span></span> <span data-ttu-id="c8a05-372">DLP 보고서를 사용하면 시간에 따른 DLP 정책 및 규칙 일치 수와 가양성 및 재정의 수를 빠르게 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-372">With DLP reports, you can quickly view the number of DLP policy and rule matches over time, and the number of false positives and overrides.</span></span> <span data-ttu-id="c8a05-373">각 보고서에 대해 위치, 시간 프레임에 따라 일치하는 항목을 필터링할 수 있으며 특정 정책, 규칙 또는 작업으로 범위를 좁힐 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-373">For each report, you can filter those matches by location, time frame, and even narrow it down to a specific policy, rule, or action.</span></span>
  
<span data-ttu-id="c8a05-374">DLP 보고서를 사용하면 비즈니스 통찰력을 얻고 다음을 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-374">With the DLP reports, you can get business insights and:</span></span>
  
- <span data-ttu-id="c8a05-375">특정 기간에 초점을 맞추고 스파이크 및 추세의 이유를 이해합니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-375">Focus on specific time periods and understand the reasons for spikes and trends.</span></span>
    
- <span data-ttu-id="c8a05-376">조직의 규정 준수 정책을 위반 하는 비즈니스 프로세스를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-376">Discover business processes that violate your organization's compliance policies.</span></span>
    
- <span data-ttu-id="c8a05-377">DLP 정책이 비즈니스에 미치는 영향을 이해합니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-377">Understand any business impact of the DLP policies.</span></span>
    
<span data-ttu-id="c8a05-378">또한 DLP 보고서를 사용하여 실행 중에 DLP 정책을 미세 조정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-378">In addition, you can use the DLP reports to fine tune your DLP policies as you run them.</span></span>
  
![보안 및 준수 센터의 보고서 대시보드](media/6d741252-a0ce-4429-95ba-6c857ecc9a7e.png)
  
## <a name="how-dlp-policies-work"></a><span data-ttu-id="c8a05-380">DLP 정책이 작동하는 방식</span><span class="sxs-lookup"><span data-stu-id="c8a05-380">How DLP policies work</span></span>

<span data-ttu-id="c8a05-p156">DLP는 심도 깊은 콘텐츠 분석(단순 텍스트 검색 아님)을 사용하여 중요한 정보를 검색합니다. 이 심도 깊은 콘텐츠 분석은 키워드 일치, 사전 일치, 정규식 평가, 내부 함수 및 기타 방법을 사용하여 DLP 정책과 일치하는 콘텐츠를 검색합니다. 잠재적으로 데이터의 일부만 중요한 것으로 간주됩니다. DLP 정책은 나머지 콘텐츠로 작업하는 사람들에게 영향을 주거나 작업을 지연시키지 않으면서 해당 데이터를 식별 및 모니터링하고 자동으로 보호할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-p156">DLP detects sensitive information by using deep content analysis (not just a simple text scan). This deep content analysis uses keyword matches, dictionary matches, the evaluation of regular expressions, internal functions, and other methods to detect content that matches your DLP policies. Potentially only a small percentage of your data is considered sensitive. A DLP policy can identify, monitor, and automatically protect just that data, without impeding or affecting people who work with the rest of your content.</span></span>
  
### <a name="policies-are-synced"></a><span data-ttu-id="c8a05-385">정책이 동기화됨</span><span class="sxs-lookup"><span data-stu-id="c8a05-385">Policies are synced</span></span>

<span data-ttu-id="c8a05-386">보안 &amp; 및 준수 센터에서 DLP 정책을 만든 후에는 중앙 정책 저장소에 저장 된 후 다음을 비롯 한 다양 한 콘텐츠 원본과 동기화 합니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-386">After you create a DLP policy in the Security &amp; Compliance Center, it's stored in a central policy store, and then synced to the various content sources, including:</span></span>
  
- <span data-ttu-id="c8a05-387">Exchange Online, 웹에서 outlook 및 outlook으로</span><span class="sxs-lookup"><span data-stu-id="c8a05-387">Exchange Online, and from there to Outlook on the web and Outlook</span></span>
    
- <span data-ttu-id="c8a05-388">비즈니스용 OneDrive 사이트</span><span class="sxs-lookup"><span data-stu-id="c8a05-388">OneDrive for Business sites</span></span>
    
- <span data-ttu-id="c8a05-389">SharePoint Online 사이트</span><span class="sxs-lookup"><span data-stu-id="c8a05-389">SharePoint Online sites</span></span>
    
- <span data-ttu-id="c8a05-390">Office 데스크톱 프로그램 (Excel, PowerPoint 및 Word)</span><span class="sxs-lookup"><span data-stu-id="c8a05-390">Office desktop programs (Excel, PowerPoint, and Word)</span></span>

- <span data-ttu-id="c8a05-391">Microsoft 팀 채널 및 채팅</span><span class="sxs-lookup"><span data-stu-id="c8a05-391">Microsoft Teams channels and chats</span></span>
    
<span data-ttu-id="c8a05-392">정책이 올바른 위치와 동기화 되 면 콘텐츠를 평가 하 고 작업을 적용 하기 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-392">After the policy's synced to the right locations, it starts to evaluate content and enforce actions.</span></span>
  
### <a name="policy-evaluation-in-onedrive-for-business-and-sharepoint-online-sites"></a><span data-ttu-id="c8a05-393">비즈니스용 OneDrive 및 SharePoint Online 사이트에서의 정책 평가</span><span class="sxs-lookup"><span data-stu-id="c8a05-393">Policy evaluation in OneDrive for Business and SharePoint Online sites</span></span>

<span data-ttu-id="c8a05-394">모든 SharePoint Online 사이트 및 비즈니스용 OneDrive 사이트에서 문서는 지속적으로 변경 되며, 계속 해 서 만들어지고 편집 되 고 공유 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-394">Across all of your SharePoint Online sites and OneDrive for Business sites, documents are constantly changing — they're continually being created, edited, shared, and so on.</span></span> <span data-ttu-id="c8a05-395">즉, 문서를 언제 든 지 충돌 하거나 DLP 정책을 준수 하도록 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-395">This means documents can conflict or become compliant with a DLP policy at any time.</span></span> <span data-ttu-id="c8a05-396">예를 들어 사용자가 팀 사이트에 중요 한 정보가 포함 되지 않은 문서를 업로드할 수 있지만 나중에 다른 사람이 같은 문서를 편집 하 고 중요 한 정보를 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-396">For example, a person can upload a document that contains no sensitive information to their team site, but later, a different person can edit the same document and add sensitive information to it.</span></span>
  
<span data-ttu-id="c8a05-397">이러한 이유로 DLP 정책은 백그라운드에서 문서의 정책 일치 여부를 자주 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-397">For this reason, DLP policies check documents for policy matches frequently in the background.</span></span> <span data-ttu-id="c8a05-398">이러한 검사를 비동기 정책 평가로 간주할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-398">You can think of this as asynchronous policy evaluation.</span></span>
  
#### <a name="how-it-works"></a><span data-ttu-id="c8a05-399">작업 방법</span><span class="sxs-lookup"><span data-stu-id="c8a05-399">How it works</span></span>
 
<span data-ttu-id="c8a05-400">누군가가 사이트에서 문서를 추가하거나 변경하면 검색 엔진이 해당 콘텐츠를 검색하므로 사용자가 나중에 검색할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-400">As people add or change documents in their sites, the search engine scans the content, so that you can search for it later.</span></span> <span data-ttu-id="c8a05-401">이 문제가 발생 하는 동안에도 콘텐츠가 중요 한 정보를 검색 하 고 공유 되는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-401">While this is happening, the content's also scanned for sensitive information and to check if it's shared.</span></span> <span data-ttu-id="c8a05-402">발견 되는 중요 한 정보는 검색 인덱스에 안전 하 게 저장 되므로 준수 팀만 액세스할 수 있고 일반적인 사용자에 게는 액세스 하지 않아도 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-402">Any sensitive information that's found is stored securely in the search index, so that only the compliance team can access it, but not typical users.</span></span> <span data-ttu-id="c8a05-403">백그라운드에서 사용 하도록 설정 된 각 DLP 정책 (비동기적으로)이 검색을 자주 실행 하 여 정책과 일치 하는 모든 콘텐츠를 확인 하 고 실수로 인 한 누수 로부터 보호 하기 위해 작업을 적용 하는 경우</span><span class="sxs-lookup"><span data-stu-id="c8a05-403">Each DLP policy that you've turned on runs in the background (asynchronously), checking search frequently for any content that matches a policy, and applying actions to protect it from inadvertent leaks.</span></span>
  
![DLP 정책이 비동기적으로 콘텐츠를 평가 하는 방법을 보여주는 다이어그램](media/bdf73099-039a-4909-ae89-ac12c41992ba.png)
  
<span data-ttu-id="c8a05-p160">마지막으로 문서는 DLP 정책과 충돌할 수 있지만 DLP 정책을 준수할 수도 있습니다. 예를 들어 어떤 사람이 신용 카드 번호를 문서를 추가하는 경우 DLP 정책이 문서에 대한 액세스를 자동으로 차단할 수 있습니다. 하지만 나중에 이 사람이 중요한 정보를 제거하면 다음 번에 정책에 대해 문서가 평가될 때 작업(이 경우 차단)이 자동으로 실행 취소됩니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-p160">Finally, documents can conflict with a DLP policy, but they can also become compliant with a DLP policy. For example, if a person adds credit card numbers to a document, it might cause a DLP policy to block access to the document automatically. But if the person later removes the sensitive information, the action (in this case, blocking) is automatically undone the next time the document is evaluated against the policy.</span></span>
  
<span data-ttu-id="c8a05-408">DLP는 인덱싱할 수 있는 모든 콘텐츠를 평가합니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-408">DLP evaluates any content that can be indexed.</span></span> <span data-ttu-id="c8a05-409">기본적으로 크롤링되는 파일 형식에 대 한 자세한 내용은 [기본 크롤링 파일 이름 확장명 및 구문 분석 된 파일 형식 (SharePoint Server](https://docs.microsoft.com/SharePoint/technical-reference/default-crawled-file-name-extensions-and-parsed-file-types))을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="c8a05-409">For more information on what file types are crawled by default, see [Default crawled file name extensions and parsed file types in SharePoint Server](https://docs.microsoft.com/SharePoint/technical-reference/default-crawled-file-name-extensions-and-parsed-file-types).</span></span>
  
### <a name="policy-evaluation-in-exchange-online-outlook-and-outlook-on-the-web"></a><span data-ttu-id="c8a05-410">Exchange Online, outlook 및 웹용 outlook의 정책 평가</span><span class="sxs-lookup"><span data-stu-id="c8a05-410">Policy evaluation in Exchange Online, Outlook, and Outlook on the web</span></span>

<span data-ttu-id="c8a05-411">exchange online을 위치로 포함 하는 DLP 정책을 만드는 경우에는 해당 정책이 Office 365 보안 &amp; 준수 센터에서 exchange online으로 동기화 된 다음 exchange online에서 웹 및 outlook의 outlook에 제공 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-411">When you create a DLP policy that includes Exchange Online as a location, the policy's synced from the Office 365 Security &amp; Compliance Center to Exchange Online, and then from Exchange Online to Outlook on the web and Outlook.</span></span>
  
<span data-ttu-id="c8a05-412">Outlook에서 메시지를 작성할 때 만들어지는 콘텐츠가 DLP 정책에 대해 평가 되는 동안 사용자는 정책 팁을 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-412">When a message is being composed in Outlook, the user can see policy tips as the content being created is evaluated against DLP policies.</span></span> <span data-ttu-id="c8a05-413">그리고 메시지가 전송 된 후에는 exchange 메일 흐름 규칙 (전송 규칙이 라고도 함)과 exchange 관리 센터에서 만든 dlp 정책을 함께 사용 하 여 dlp 정책에 대 한 메일 흐름의 일반적인 부분으로 평가 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-413">And after a message is sent, it's evaluated against DLP policies as a normal part of mail flow, along with Exchange mail flow rules (also known as transport rules) and DLP policies created in the Exchange admin center.</span></span> <span data-ttu-id="c8a05-414">DLP 정책은 메시지와 첨부 파일을 모두 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-414">DLP policies scan both the message and any attachments.</span></span>
  
### <a name="policy-evaluation-in-the-office-desktop-programs"></a><span data-ttu-id="c8a05-415">Office 데스크톱 프로그램의 정책 평가</span><span class="sxs-lookup"><span data-stu-id="c8a05-415">Policy evaluation in the Office desktop programs</span></span>

<span data-ttu-id="c8a05-416">Excel, PowerPoint 및 Word에는 중요 한 정보를 식별 하 고 DLP 정책을 SharePoint Online 및 비즈니스용 OneDrive로 적용 하는 것과 동일한 기능이 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-416">Excel, PowerPoint, and Word include the same capability to identify sensitive information and apply DLP policies as SharePoint Online and OneDrive for Business.</span></span> <span data-ttu-id="c8a05-417">이러한 Office 프로그램은 중앙 정책 저장소에서 dlp 정책을 직접 동기화 한 다음 사용자가 dlp 정책에 포함 된 사이트에서 연 문서를 사용할 때 dlp 정책에 대해 콘텐츠를 지속적으로 평가 합니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-417">These Office programs sync their DLP policies directly from the central policy store, and then continuously evaluate the content against the DLP policies when people work with documents opened from a site that's included in a DLP policy.</span></span>
  
<span data-ttu-id="c8a05-418">Office의 DLP 정책 계산은 프로그램의 성능 또는 콘텐츠 작업을 수행 하는 사용자의 생산성에 영향을 주지 않도록 설계 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-418">DLP policy evaluation in Office is designed not to affect the performance of the programs or the productivity of people working on content.</span></span> <span data-ttu-id="c8a05-419">대규모 문서에서 작업 중이거나 사용자의 컴퓨터가 사용 중인 경우 정책 팁이 표시 되는 데 몇 초 정도 걸릴 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-419">If they're working on a large document, or the user's computer is busy, it might take a few seconds for a policy tip to appear.</span></span>

### <a name="policy-evaluation-in-microsoft-teams"></a><span data-ttu-id="c8a05-420">Microsoft 팀의 정책 평가</span><span class="sxs-lookup"><span data-stu-id="c8a05-420">Policy evaluation in Microsoft Teams</span></span>
 
<span data-ttu-id="c8a05-421">Microsoft 팀을 위치를 포함 하는 DLP 정책을 만들 때 정책이 Office 365 보안 &amp; 준수 센터에서 사용자 계정 및 Microsoft 팀 채널과 채팅에 동기화 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-421">When you create a DLP policy that includes Microsoft Teams as a location, the policy's synced from the Office 365 Security &amp; Compliance Center to user accounts and Microsoft Teams channels and chats.</span></span> <span data-ttu-id="c8a05-422">DLP 정책이 구성 되는 방식에 따라 누군가 Microsoft 팀 채팅 또는 채널에서 중요 한 정보를 공유 하려고 할 때 메시지가 차단 되거나 해지 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-422">Depending on how DLP policies are configured, when someone attempts to share sensitive information in a Microsoft Teams chat or channel, the message can be blocked or revoked.</span></span> <span data-ttu-id="c8a05-423">또한 중요 한 정보가 들어 있고 게스트 (외부 사용자)와 공유 되는 문서가 해당 사용자에 대해 열리지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-423">And, documents that contain sensitive information and that are shared with guests (external users) won't open for those users.</span></span>

<span data-ttu-id="c8a05-424">예를 들어 사용자가 외부 사용자와 팀 채팅 또는 채널에서 중요 한 정보를 공유 하려고 하는 경우를 가정해 보겠습니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-424">For example, suppose that someone attempts to share sensitive information in a Teams chat or channel with external users.</span></span> <span data-ttu-id="c8a05-425">이를 방지 하기 위해 DLP 정책이 정의 되어 있다고 가정해 보겠습니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-425">Suppose there's a DLP policy defined to prevent this.</span></span> <span data-ttu-id="c8a05-426">보호 기능이 있으면 외부 사용자에 게 전송 되는 중요 한 정보가 포함 된 메시지가 삭제 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-426">With protection in place, messages containing sensitive information sent to external users are deleted.</span></span> <span data-ttu-id="c8a05-427">이 작업은 초 내에 수행 되며 DLP 정책이 구성 되는 방식에 따라 자동으로 수행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-427">This happens within seconds, and it happens automatically, according to how the DLP policy is configured.</span></span>

<span data-ttu-id="c8a05-428">정책 팁 보낸 사람이 메시지를 차단 하거나 해지 한 이유에 대해 알려 줍니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-428">Policy tips notify senders about why their messages were blocked or revoked.</span></span> <span data-ttu-id="c8a05-429">예를 들어 보낸 사람이 메시지에 다른 사람과 공유할 수 없는 pii (개인 식별 정보)가 포함 되어 있거나, pii가 포함 된 문서를 조직 외부의 사용자와 공유할 수 없는 것으로 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-429">For example, a sender might be told that their message contains personally identifiable information (PII) that is not allowed to be shared with anyone, or that a document that contains PII cannot be shared with people outside their organization.</span></span> <span data-ttu-id="c8a05-430">그런 다음 보낸 사람은 메시지를 편집 하 여 DLP 정책을 준수 하도록 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-430">The sender can then edit their message to be compliant with DLP policies.</span></span>
 
## <a name="permissions"></a><span data-ttu-id="c8a05-431">사용 권한</span><span class="sxs-lookup"><span data-stu-id="c8a05-431">Permissions</span></span>

<span data-ttu-id="c8a05-432">준수 팀의 구성원에 게는 DLP 정책을 만들 사용자의 보안 &amp; 및 준수 센터에 대 한 사용 권한이 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-432">Members of your compliance team who will create DLP policies need permissions to the Security &amp; Compliance Center.</span></span> <span data-ttu-id="c8a05-433">기본적으로 테 넌 트 관리자는이 위치에 액세스할 수 있으며, 규정 준수 관리자 및 기타 사용자에 게는 모든 &amp; 테 넌 트 관리 권한을 부여 하지 않고도 보안 준수 센터에 대 한 액세스를 제공 합니다. 이렇게 하려면 다음을 수행 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-433">By default, your tenant admin will have access to this location and can give compliance officers and other people access to the Security &amp; Compliance Center, without giving them all of the permissions of a tenant admin. To do this, we recommend that you:</span></span>
  
1. <span data-ttu-id="c8a05-434">Office 365에서 그룹을 만들고 규정 준수 책임자를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-434">Create a group in Office 365 and add compliance officers to it.</span></span>
    
2. <span data-ttu-id="c8a05-435">보안 &amp; 및 준수 센터의 **사용 권한** 페이지에서 역할 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-435">Create a role group on the **Permissions** page of the Security &amp; Compliance Center.</span></span> 
    
3. <span data-ttu-id="c8a05-436">Office 365 그룹을 역할 그룹에 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-436">Add the Office 365 group to the role group.</span></span>
    
<span data-ttu-id="c8a05-437">자세한 내용은 [Give users access to the Office 365 Compliance Center](grant-access-to-the-security-and-compliance-center.md)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="c8a05-437">For more information, see [Give users access to the Office 365 Compliance Center](grant-access-to-the-security-and-compliance-center.md).</span></span>
  
<span data-ttu-id="c8a05-438">이러한 정책은 DLP 정책을 만들고 적용하는 데만 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-438">These permissions are required only to create and apply a DLP policy.</span></span> <span data-ttu-id="c8a05-439">정책 적용을 위해서는 콘텐츠에 액세스하지 않아도 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-439">Policy enforcement does not require access to the content.</span></span>
  
## <a name="find-the-dlp-cmdlets"></a><span data-ttu-id="c8a05-440">DLP cmdlet 찾기</span><span class="sxs-lookup"><span data-stu-id="c8a05-440">Find the DLP cmdlets</span></span>

<span data-ttu-id="c8a05-441">보안 &amp; 및 준수 센터에 대 한 cmdlet을 대부분 사용 하려면 다음 작업을 수행 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-441">To use most of the cmdlets for the Security &amp; Compliance Center, you need to:</span></span>
  
1. [<span data-ttu-id="c8a05-442">원격 PowerShell을 사용하여 Office 365 보안 및 준수 센터에 연결</span><span class="sxs-lookup"><span data-stu-id="c8a05-442">Connect to the Office 365 Security &amp; Compliance Center using remote PowerShell</span></span>](https://docs.microsoft.com/powershell/exchange/office-365-scc/connect-to-scc-powershell/connect-to-scc-powershell?view=exchange-ps)
    
2. <span data-ttu-id="c8a05-443">이러한 [정책 및 준수-dlp cmdlet](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-dlp/export-dlppolicycollection?view=exchange-ps) 중 하나를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-443">Use any of these [policy-and-compliance-dlp cmdlets](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-dlp/export-dlppolicycollection?view=exchange-ps)</span></span>
    
<span data-ttu-id="c8a05-444">그러나 DLP 보고서는 Exchange Online을 포함 하 여 Office 365 간에 데이터를 가져올 필요가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-444">However, DLP reports need pull data from across Office 365, including Exchange Online.</span></span> <span data-ttu-id="c8a05-445">따라서 **DLP 보고서용 cmdlet은 보안 &amp; 및 준수 센터 powershell이 아닌 Exchange Online Powershell에서 사용할 수 있습니다**.</span><span class="sxs-lookup"><span data-stu-id="c8a05-445">For this reason, **the cmdlets for the DLP reports are available in Exchange Online Powershell -- not in Security &amp; Compliance Center Powershell**.</span></span> <span data-ttu-id="c8a05-446">따라서 DLP 보고서에 대해 cmdlet을 사용 하려면 다음을 수행 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-446">Therefore, to use the cmdlets for the DLP reports, you need to:</span></span>
  
1. <span data-ttu-id="c8a05-447">[Connect to Exchange Online using remote PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell?view=exchange-ps)(원격 PowerShell을 사용하여 Exchange Online에 연결)</span><span class="sxs-lookup"><span data-stu-id="c8a05-447">[Connect to Exchange Online using remote PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell?view=exchange-ps)</span></span>
    
2. <span data-ttu-id="c8a05-448">DLP 보고서에 대해 다음 cmdlet 중 하나를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="c8a05-448">Use any of these cmdlets for the DLP reports:</span></span>
    
  - [<span data-ttu-id="c8a05-449">get-dlpdetectionsreport</span><span class="sxs-lookup"><span data-stu-id="c8a05-449">Get-DlpDetectionsReport</span></span>](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-dlp/Get-DlpDetectionsReport?view=exchange-ps)
    
  - [<span data-ttu-id="c8a05-450">get-dlpdetailreport</span><span class="sxs-lookup"><span data-stu-id="c8a05-450">Get-DlpDetailReport</span></span>](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-dlp/Get-DlpDetailReport?view=exchange-ps)
    
## <a name="more-information"></a><span data-ttu-id="c8a05-451">추가 정보</span><span class="sxs-lookup"><span data-stu-id="c8a05-451">More information</span></span>

- [<span data-ttu-id="c8a05-452">템플릿에서 DLP 정책 만들기</span><span class="sxs-lookup"><span data-stu-id="c8a05-452">Create a DLP policy from a template</span></span>](create-a-dlp-policy-from-a-template.md)
    
- [<span data-ttu-id="c8a05-453">DLP 정책에 대한 알림 보내기 및 정책 팁 표시</span><span class="sxs-lookup"><span data-stu-id="c8a05-453">Send notifications and show policy tips for DLP policies</span></span>](use-notifications-and-policy-tips.md)
    
- [<span data-ttu-id="c8a05-454">FCI 또는 기타 속성을 갖는 문서를 보호하는 DLP 정책 만들기</span><span class="sxs-lookup"><span data-stu-id="c8a05-454">Create a DLP policy to protect documents with FCI or other properties</span></span>](protect-documents-that-have-fci-or-other-properties.md)
    
- [<span data-ttu-id="c8a05-455">DLP 정책 템플릿에 포함되는 내용</span><span class="sxs-lookup"><span data-stu-id="c8a05-455">What the DLP policy templates include</span></span>](what-the-dlp-policy-templates-include.md)
    
- [<span data-ttu-id="c8a05-456">중요한 정보 형식이 찾는 항목</span><span class="sxs-lookup"><span data-stu-id="c8a05-456">What the sensitive information types look for</span></span>](what-the-sensitive-information-types-look-for.md)
    
- [<span data-ttu-id="c8a05-457">DLP 기능이 찾는 항목</span><span class="sxs-lookup"><span data-stu-id="c8a05-457">What the DLP functions look for</span></span>](what-the-dlp-functions-look-for.md)
    
- [<span data-ttu-id="c8a05-458">사용자 지정 중요한 정보 유형 만들기</span><span class="sxs-lookup"><span data-stu-id="c8a05-458">Create a custom sensitive information type</span></span>](create-a-custom-sensitive-information-type.md)
    

