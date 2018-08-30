---
title: 템플릿에서 DLP 정책 만들기
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 6/29/2018
ms.audience: Admin
ms.topic: article
f1_keywords:
- ms.o365.cc.NewPolicyFromTemplate
ms.service: o365-administration
localization_priority: Normal
ms.collection:
- Strat_O365_IP
search.appverid:
- MET150
ms.assetid: 59414438-99f5-488b-975c-5023f2254369
description: 'DLP 정책을 사용 하 여 시작 하는 것이 가장 편리 하 고 가장 일반적인 방법은 Office 365에 포함 된 서식 파일 중 하나를 사용 하는 것입니다. '
ms.openlocfilehash: 4e3a5d731538e4998858b5f9f7a296c43e6774ac
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22533552"
---
# <a name="create-a-dlp-policy-from-a-template"></a><span data-ttu-id="b47e3-103">템플릿에서 DLP 정책 만들기</span><span class="sxs-lookup"><span data-stu-id="b47e3-103">Create a DLP policy from a template</span></span>

<span data-ttu-id="b47e3-p101">DLP 정책을 사용 하 여 시작 하는 것이 가장 편리 하 고 가장 일반적인 방법은 Office 365에 포함 된 서식 파일 중 하나를 사용 하는 것입니다. 되기 시작 하면 이러한 서식 파일 중 하나를 사용할 수도 있고 조직의 특정 규정 준수 요구 사항을 충족 하기 위해 규칙을 사용자 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b47e3-p101">The easiest, most common way to get started with DLP policies is to use one of the templates included in Office 365. You can use one of these templates as is, or customize the rules to meet your organization's specific compliance requirements.</span></span>
  
<span data-ttu-id="b47e3-p102">Office 365에는 광범위한 일반적인 규정 및 비즈니스 정책 요구를 충족하기 위해 바로 사용할 수 있는 40가지 이상의 템플릿이 포함되어 있습니다. 예를 들어 다음에 대한 DLP 정책 템플릿이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b47e3-p102">Office 365 includes over 40 ready-to-use templates that can help you meet a wide range of common regulatory and business policy needs. For example, there are DLP policy templates for:</span></span>
  
- <span data-ttu-id="b47e3-108">GLBA(Gramm-Leach-Bliley Act)</span><span class="sxs-lookup"><span data-stu-id="b47e3-108">Gramm-Leach-Bliley Act (GLBA)</span></span>
    
- <span data-ttu-id="b47e3-109">PCI-DSS(Payment Card Industry Data Security Standard)</span><span class="sxs-lookup"><span data-stu-id="b47e3-109">Payment Card Industry Data Security Standard (PCI-DSS)</span></span>
    
- <span data-ttu-id="b47e3-110">U.S. PII(United States Personally Identifiable Information)</span><span class="sxs-lookup"><span data-stu-id="b47e3-110">United States Personally Identifiable Information (U.S. PII)</span></span>
    
- <span data-ttu-id="b47e3-111">미국 HIPAA(Health Insurance Act)</span><span class="sxs-lookup"><span data-stu-id="b47e3-111">United States Health Insurance Act (HIPAA)</span></span>
    
<span data-ttu-id="b47e3-p103">기존 규칙을 수정하거나 새로 추가하여 템플릿을 미세 조정할 수 있습니다. 예를 들어 새로운 유형의 중요한 정보를 규칙에 추가하거나, 한 규칙의 템플릿 수를 수정하여 트리거하기 더 어렵게 또는 더 쉽게 만들거나, 업무 정당성을 제공하여 규칙의 작업을 재정의할 수 있도록 하거나, 알림 및 사고 보고서를 받을 수 있는 사람을 변경할 수 있습니다. DLP 정책 템플릿은 여러 일반적인 규정 준수 시나리오에 대한 유연한 시작점입니다.</span><span class="sxs-lookup"><span data-stu-id="b47e3-p103">You can fine tune a template by modifying any of the existing rules or adding new ones. For example, you can add new types of sensitive information to a rule, modify the counts in a rule to make it harder or easier to trigger, allow people to override the actions in a rule by providing a business justification, or change who notifications and incident reports are sent to. A DLP policy template is a flexible starting point for many common compliance scenarios.</span></span>
  
<span data-ttu-id="b47e3-115">기본 규칙이 없는 사용자 지정 템플릿을 선택하고, 조직의 특정 규정 준수 요구에 맞게 DLP 정책을 처음부터 새로 구성할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b47e3-115">You can also choose the Custom template, which has no default rules, and configure your DLP policy from scratch, to meet the specific compliance requirements for your organization.</span></span>
  
## <a name="example-identify-sensitive-information-across-all-onedrive-for-business-sites-and-restrict-access-for-people-outside-your-organization"></a><span data-ttu-id="b47e3-116">예: 비즈니스 사이트에 대 한 모든 OneDrive에서 중요 한 정보를 식별 하 고 조직 외부의 사용자에 대 한 액세스를 제한 합니다.</span><span class="sxs-lookup"><span data-stu-id="b47e3-116">Example: Identify sensitive information across all OneDrive for Business sites and restrict access for people outside your organization</span></span>

<span data-ttu-id="b47e3-p104">비즈니스 계정에 대 한 OneDrive 쉽게 사람들에 대 한 공동 작업을 수행 하 고 문서를 공유 하 여 조직입니다. 하지만 규정 준수 관리자에 대 한 일반적인 문제는 비즈니스 계정에 대 한 OneDrive에 저장 된 중요 한 정보 조직 외부의 사용자와 실수로 공유 수 있습니다. DLP 정책이이 위험을 완화할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b47e3-p104">OneDrive for Business accounts make it easy for people across your organization to collaborate and share documents. But a common concern for compliance officers is that sensitive information stored in OneDrive for Business accounts may be inadvertently shared with people outside your organization. A DLP policy can help mitigate this risk.</span></span>
  
<span data-ttu-id="b47e3-p105">이 예제에서는 개별 납세자 식별 번호 (뿐만), 주민등록 번호, 및 미국 여권 번호를 포함 하는 미국 PII 데이터를 식별 하는 DLP 정책을 만들어야 합니다. 서식 파일을 사용 하 여 시작 하 고 조직의 규정 준수 요구 사항을 충족 서식 파일을 수정 하는 다음-구체적으로 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b47e3-p105">In this example, you'll create a DLP policy that identifies U.S. PII data, which includes Individual Taxpayer Identification Numbers (ITIN), Social Security Numbers, and U.S. passport numbers. You'll get started by using a template, and then you'll modify the template to meet your organization's compliance requirements—specifically, you'll:</span></span>
  
- <span data-ttu-id="b47e3-122">두 종류의 중요 한 information—U.S. 은행 계좌 번호 및 미국 운전 면허 번호 추가-중요 한 데이터의 훨씬 더 많은 보호 하는 DLP 정책 되도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="b47e3-122">Add a couple of types of sensitive information—U.S. bank account numbers and U.S. driver's license numbers—so that the DLP policy protects even more of your sensitive data.</span></span>
    
- <span data-ttu-id="b47e3-123">외부 사용자에 대 한 액세스를 제한 하려면 충분히 중요 한 정보의 단일 발생 될 수 있도록 정책 보다 중요 한 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="b47e3-123">Make the policy more sensitive, so that a single occurrence of sensitive information is enough to restrict access for external users.</span></span>
    
- <span data-ttu-id="b47e3-p106">업무 효율성을 제공 하거나 가양성을 보고 하 여 작업을 재정의할 수 있도록 합니다. 이와 같은 방식이으로 DLP 정책에 따라 중요 한 정보를 공유 하는 유효한 비즈니스 이유를가지고 있습니다. 제공 자신의 작업을 수행 하 고, 시작에서 조직의 사용자를 방해가 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b47e3-p106">Allow users to override the actions by providing a business justification or reporting a false positive. This way, your DLP policy won't prevent people in your organization from getting their work done, provided they have a valid business reason for sharing the sensitive information.</span></span>
    
### <a name="create-a-dlp-policy-from-a-template"></a><span data-ttu-id="b47e3-126">템플릿에서 DLP 정책 만들기</span><span class="sxs-lookup"><span data-stu-id="b47e3-126">Create a DLP policy from a template</span></span>

1. <span data-ttu-id="b47e3-127">이동 [https://protection.office.com](https://protection.office.com)합니다.</span><span class="sxs-lookup"><span data-stu-id="b47e3-127">Go to [https://protection.office.com](https://protection.office.com).</span></span>
    
2. <span data-ttu-id="b47e3-p107">작업이 나 교육용 계정을 사용 하 여 Office 365에 로그인 합니다. Office 365 보안에서 이제는 &amp; 준수 센터입니다.</span><span class="sxs-lookup"><span data-stu-id="b47e3-p107">Sign in to Office 365 using your work or school account. You're now in the Office 365 Security &amp; Compliance Center.</span></span>
    
3. <span data-ttu-id="b47e3-130">보안에서 &amp; 준수 센터 \> 왼쪽 탐색 \> **데이터 손실 방지** \> **정책** \> **+ 정책 만들기**.</span><span class="sxs-lookup"><span data-stu-id="b47e3-130">In the Security &amp; Compliance Center \> left navigation \> **Data loss prevention** \> **Policy** \> **+ Create a policy**.</span></span>
    
    ![정책 단추 만들기](media/b1e48a08-92e2-47ca-abdc-4341694ddc7c.png)
  
4. <span data-ttu-id="b47e3-132">필요한 중요 한 정보의 종류를 보호 하는 DLP 정책 서식 파일을 선택 \> **다음**합니다.</span><span class="sxs-lookup"><span data-stu-id="b47e3-132">Choose the DLP policy template that protects the types of sensitive information that you need \> **Next**.</span></span>
    
    <span data-ttu-id="b47e3-133">이 예제에서는 **개인 정보** 를 선택 합니다 \> **미국 개인 식별 정보 pii (개인) 데이터** 보호 하려는 중요 한 정보의 종류를 대부분 하는 이미 포함 되어 있으므로-몇을 나중에 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b47e3-133">In this example, you'll select **Privacy** \> **U.S. Personally Identifiable Information ‎(PII)‎ Data** because it already includes most of the types of sensitive information that you want to protect—you'll add a couple later.</span></span> 
    
    <span data-ttu-id="b47e3-134">서식 파일을 선택 하면 중요 한 정보는 서식 파일 유형으로 보호 하는 기능에 대해 알아보려면 오른쪽에 있는 설명을 읽을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b47e3-134">When you select a template, you can read the description on the right to learn what types of sensitive information the template protects.</span></span>
    
    ![DLP 정책 서식 파일을 선택 하는 것에 대 한 페이지](media/775266f6-ad87-4080-8d7c-97f2e7403b30.png)
  
5. <span data-ttu-id="b47e3-136">정책 이름을 \> **다음**합니다.</span><span class="sxs-lookup"><span data-stu-id="b47e3-136">Name the policy \> **Next**.</span></span>
    
6. <span data-ttu-id="b47e3-137">DLP 정책을 보호 하려면 다음 중 하나를 수행 하는 위치를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="b47e3-137">To choose the locations that you want the DLP policy to protect, do one of the following:</span></span>
    
  - <span data-ttu-id="b47e3-138">**Office 365의 모든 위치** 를 선택 \> **다음**합니다.</span><span class="sxs-lookup"><span data-stu-id="b47e3-138">Choose **All locations in Office 365** \> **Next**.</span></span>
    
  - <span data-ttu-id="b47e3-p108">**특정 위치를 선택** 선택 \> **다음**합니다. 이 예제에서는이 설정을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="b47e3-p108">Choose **Let me choose specific locations** \> **Next**. For this example, choose this.</span></span>
    
    <span data-ttu-id="b47e3-141">설정 또는 해제를 포함 하거나 모든 Exchange 전자 메일 또는 모든 OneDrive 계정 같은 전체 위치를 제외 하려면 해당 위치의 **상태** 를 전환 합니다.</span><span class="sxs-lookup"><span data-stu-id="b47e3-141">To include or exclude an entire location such as all Exchange email or all OneDrive accounts, switch the **Status** of that location on or off.</span></span> 
    
    <span data-ttu-id="b47e3-p109">비즈니스 계정에 대 한 특정 SharePoint 사이트 또는 OneDrive를 포함 합니다, **상태** 를 전환한 다음 **Include** 특정 사이트 또는 계정을 선택 하려면 아래의 링크를 클릭 합니다. 사이트 정책이 자동으로 해당 사이트의 모든 하위 사이트에 적용 되는 구성 된 규칙에는 정책을 적용 하면.</span><span class="sxs-lookup"><span data-stu-id="b47e3-p109">To include only specific SharePoint sites or OneDrive for Business accounts, switch the **Status** to on, and then click the links under **Include** to choose specific sites or accounts. When you apply a policy to a site, the rules configured in that policy are automatically applied to all subsites of that site.</span></span> 
    
    ![DLP 정책을 적용할 수 있는 위치에 대 한 옵션](media/ee50a61a-e867-4571-a150-3eec8d83650f.png)
  
    <span data-ttu-id="b47e3-145">이 예제에서는 비즈니스 계정에 대 한 모든 OneDrive에 저장 된 중요 한 정보를 보호 하려면 **Exchange 전자 메일** 및 **SharePoint 사이트**를 모두에 대 한 **상태** 를 해제 하 고에 **OneDrive 계정**에 대 한 **상태** 를 유지 합니다.</span><span class="sxs-lookup"><span data-stu-id="b47e3-145">In this example, to protect sensitive information stored in all OneDrive for Business accounts, turn off the **Status** for both **Exchange email** and **SharePoint sites**, and leave the **Status** on for **OneDrive accounts**.</span></span>
    
7. <span data-ttu-id="b47e3-146">**고급 설정 사용을** 선택 \> **다음**합니다.</span><span class="sxs-lookup"><span data-stu-id="b47e3-146">Choose **Use advanced settings** \> **Next**.</span></span>
    
8. <span data-ttu-id="b47e3-p110">DLP 정책 템플릿 조건 및 작업을 검색 하 고 특정 형식의 중요 한 정보에 따라 동작을 사용 하 여 미리 정의 된 규칙을 포함 합니다. 하면 수 편집, 삭제 또는 모든 기존 규칙을 해제 또는 새 값을 추가 합니다. 완료 되 면 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="b47e3-p110">A DLP policy template contains predefined rules with conditions and actions that detect and act upon specific types of sensitive information. You can edit, delete, or turn off any of the existing rules, or add new ones. When done, click **Next**.</span></span>
    
    ![미국 PII 정책 서식 파일에서 규칙 확장](media/3bc9f1b6-f8ad-4334-863a-24448bb87687.png)
  
    <span data-ttu-id="b47e3-151">이 예제에서는 미국 PII 데이터 서식 파일에는 두 미리 정의 된 규칙이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b47e3-151">In this example, the U.S. PII Data template includes two predefined rules:</span></span>
    
  - <span data-ttu-id="b47e3-p111">**콘텐츠의 낮은 볼륨 미국 PII 감지** 이 규칙은 각각 다음과 같은 세가지 유형의 조직 외부의 사용자와는 파일을 공유 하는 중요 한 정보 (뿐만, SSN, 및 미국 여권 번호)의 발생 수를 1에서 10 사이 포함 한 파일을 찾습니다. 발견 규칙 전자 메일 알림을 문서 소유자, 주 사이트 모음 관리자에 게 보내고 경우 마지막으로 수정한 사람 문서입니다.</span><span class="sxs-lookup"><span data-stu-id="b47e3-p111">**Low volume of content detected U.S. PII** This rule looks for files containing between 1 and 10 occurrences of each of three types of sensitive information (ITIN, SSN, and U.S. passport numbers), where the files are shared with people outside the organization. If found, the rule sends an email notification to the primary site collection administrator, document owner, and person who last modified the document.</span></span> 
    
  - <span data-ttu-id="b47e3-p112">**많은 양의 콘텐츠 미국 PII 감지** 이 규칙은 조직 외부의 사용자와는 파일을 공유 하는 각각 동일한 세 중요 한 정보 유형의 10 개 이상의 항목을 포함 하는 파일을 찾습니다. 경우 발견 하 고,이 작업을이 수행 보내, 전자 메일 알림 및 파일에 대 한 액세스를 제한 합니다. 비즈니스 계정에 대 한 OneDrive에서 콘텐츠를 문서에 대 한 사용 권한을 주 사이트 모음 관리자, 문서 소유자 및 문서를 마지막으로 수정한 사람을 제외한 모든 사람에 대 한 제한 되는 의미 합니다.</span><span class="sxs-lookup"><span data-stu-id="b47e3-p112">**High volume of content detected U.S. PII** This rule looks for files containing 10 or more occurrences of each of the same three sensitive information types, where the files are shared with people outside the organization. If found, this action also sends an email notification, plus it restricts access to the file. For content in a OneDrive for Business account, this means that permissions for the document are restricted for everyone except the primary site collection administrator, document owner, and person who last modified the document.</span></span> 
    
    <span data-ttu-id="b47e3-p113">조직의 특정 요구를 충족 하기 위해 외부 사용자에 대 한 액세스를 차단 하도록 충분히 중요 한 정보의 단일 발생 될 수 있도록 하는 규칙 트리거를 쉽게 좋습니다 확인 메시지가 나타납니다. 이러한 규칙을 보고 한 후 낮은 및 높은 count 규칙 않아도 이해-발견 되는 중요 한 정보는 발생 하는 경우에 대 한 액세스를 차단 하는 단일 규칙에만 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="b47e3-p113">To meet your organization's specific requirements, you may want to make the rules easier to trigger, so that a single occurrence of sensitive information is enough to block access for external users. After looking at these rules, you understand that you don't need low and high count rules—you need only a single rule that blocks access if any occurrence of sensitive information is found.</span></span>
    
    <span data-ttu-id="b47e3-159">**낮은 볼륨 콘텐츠의 검색 미국 PII** 라는 규칙을 확장 하므로 \> **규칙을 삭제**합니다.</span><span class="sxs-lookup"><span data-stu-id="b47e3-159">So you expand the rule named **Low volume of content detected U.S. PII** \> **Delete rule**.</span></span>
    
    ![규칙 단추를 삭제 합니다.](media/bc36f7d2-0fae-4af1-92e8-95ba51077b12.png)
  
9. <span data-ttu-id="b47e3-p114">이제이 예제에서는 필요 두 중요 한 정보 유형 (미국 은행 계좌 번호 및 미국 운전 면허 번호)를 추가 하는 규칙을 재정의 하려면 사용자를 허용 하 여 개수를 변경 모든 경우. 하나의 규칙을 편집 하 여이 모든 작업을 수행할 **많은 양의 콘텐츠 미국 PII를 감지** 하므로 선택 수 \> **규칙을 편집**합니다.</span><span class="sxs-lookup"><span data-stu-id="b47e3-p114">Now, in this example, you need to add two sensitive information types (U.S. bank account numbers and U.S. driver's license numbers), allow people to override a rule, and change the count to any occurrence. You can do all of this by editing one rule, so select **High volume of content detected U.S. PII** \> **Edit rule**.</span></span>
    
    ![규칙 단추를 편집 합니다.](media/eaf54067-4945-4c98-8dd6-fb2c5d6de075.png)
  
10. <span data-ttu-id="b47e3-p115">중요 한 정보 유형, **조건** 섹션에서 추가할 \> **추가 또는 변경 유형**입니다. **추가 또는 변경 유형** 아래에서 다음 \> **추가** 선택 \> **미국 은행 계좌 번호** 와 **미국 운전 면허 번호** 를 선택 \> **추가** \> **작업을 수행**합니다.</span><span class="sxs-lookup"><span data-stu-id="b47e3-p115">To add a sensitive information type, in the **Conditions** section \> **Add or change types**. Then, under **Add or change types** \> choose **Add** \> select **U.S. Bank Account Number** and **U.S. Driver's License Number** \> **Add** \> **Done**.</span></span>
    
    ![추가 옵션 또는 형식을 변경 합니다.](media/c6c3ae86-f7db-40a8-a6e4-db11692024be.png)
  
    ![추가 또는 변경 유형 창](media/fdbb96af-b914-4a6c-a97b-bbd014689965.png)
  
11. <span data-ttu-id="b47e3-p116">**인스턴스 수** 아래에서 count (규칙을 트리거하는 데 필요한 중요 한 정보의 인스턴스 수)를 변경 하려면 \> 각 형식에 대 한 **최소** 값 선택 \> 1을 입력 합니다. 최소 count 비워둘 수 없습니다. 최대 개수는 빈; 될 수 있습니다. 빈 **최대** 값을 **모두**로 변환 합니다.</span><span class="sxs-lookup"><span data-stu-id="b47e3-p116">To change the count (the number of instances of sensitive information required to trigger the rule), under **Instance count** \> choose the **min** value for each type \> enter 1. The minimum count cannot be empty. The maximum count can be empty; an empty **max** value convert to **any**.</span></span>
    
    <span data-ttu-id="b47e3-p117">완료 되 면 중요 한 정보 유형의 모든 min count **1** 하며 최대 수 있어야 **모든**. 즉,이 중요 한 정보 유형의 모든 경우는 이러한 조건을 만족 하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="b47e3-p117">When finished, the min count for all of the sensitive information types should be **1** and the max count should be **any**. In other words, any occurrence of this type of sensitive information will satisfy this condition.</span></span>
    
    ![중요 한 정보 형식에 대 한 인스턴스 수](media/5c6e08cb-59a9-4558-b54b-d899836d4737.png)
  
12. <span data-ttu-id="b47e3-174">최종 사용자 지정을 위한에서 유효한 업무상의 이유에 설정 또는 되므로 차단 동작을 재정의 하려면 옵션을 포함 하도록 사용자 알림 원하는 가양성을 발생 하는 경우 해당 작업을 수행 하는 사용자를 차단 하도록 DLP 정책을 하지 않으려고 합니다.</span><span class="sxs-lookup"><span data-stu-id="b47e3-174">For the final customization, you don't want your DLP policies to block people from doing their work when they have a valid business justification or encounter a false positive, so you want the user notification to include options to override the blocking action.</span></span>
    
    <span data-ttu-id="b47e3-175">**사용자 알림** 섹션에 있는 전자 메일 알림 및 정책 팁 켜져 서식 파일에이 규칙에 대 한 기본적으로 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b47e3-175">In the **User notifications** section, you can see that email notifications and policy tips are turned on by default for this rule in the template.</span></span> 
    
    <span data-ttu-id="b47e3-p118">**사용자 재정의** 섹션에는 업무상의 이유에 대 한 재정의으로 설정 되어 있지만 가양성을 보고 하는 재정의 하지는 볼 수 있습니다. **가양성으로 보고 하는 경우에 자동으로 규칙을 무시**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="b47e3-p118">In the **User overrides** section, you can see that overrides for a business justification are turned on, but overrides to report false positives are not. Choose **Override the rule automatically if they report it as a false positive**.</span></span>
    
    ![사용자 알림 섹션 및 사용자 섹션을 재정의 합니다.](media/62720e7a-a939-4c03-b414-67748f3d64a0.png)
  
13. <span data-ttu-id="b47e3-179">규칙 편집기의 위쪽이 규칙의 이름에서에서 변경 **많은 양의 콘텐츠 검색 미국 PII** 기본 **미국 PII와을 감지 하는 모든 콘텐츠** 를 해당 중요 한 정보 유형의 모든 경우에 의해 트리거된 이제 때문에 합니다.</span><span class="sxs-lookup"><span data-stu-id="b47e3-179">At the top of the rule editor, change the name of this rule from the default **High volume of content detected U.S. PII** to **Any content detected with U.S. PII** because it's now triggered by any occurrence of its sensitive information types.</span></span> 
    
14. <span data-ttu-id="b47e3-180">규칙 편집기의 맨 아래에 \> **저장**합니다.</span><span class="sxs-lookup"><span data-stu-id="b47e3-180">At the bottom of the rule editor \> **Save**.</span></span>
    
15. <span data-ttu-id="b47e3-181">조건 및이 규칙에 대 한 동작을 검토 \> **다음**합니다.</span><span class="sxs-lookup"><span data-stu-id="b47e3-181">Review the conditions and actions for this rule \> **Next**.</span></span>
    
    <span data-ttu-id="b47e3-p119">오른쪽으로 전환 규칙에 대 한 **상태** 를 확인 합니다. 전체 정책의 해제 하면 정책에 포함 된 모든 규칙 해제도 됩니다. 그러나 여기 해제할 수 있습니다는 특정 규칙 전체 정책 해제 하지 않고 합니다. 많은 수의 가양성을 생성 하는 규칙을 확인 하려는 경우에 유용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b47e3-p119">On the right, notice the **Status** switch for the rule. If you turn off an entire policy, all rules contained in the policy are also turned off. However, here you can turn off a specific rule without turning off the entire policy. This can be useful when you need to investigate a rule that is generating a large number of false positives.</span></span> 
    
16. <span data-ttu-id="b47e3-186">다음 페이지에서 읽기 및 다음을 이해 하 고 규칙 하거나 먼저 수행 하 여이 테스트 하려면 여부를 선택 \> **다음**합니다.</span><span class="sxs-lookup"><span data-stu-id="b47e3-186">On the next page, read and understand the following, and then choose whether to turn on the rule or test it out first \> **Next**.</span></span>
    
     <span data-ttu-id="b47e3-p120">DLP 정책을 만들기 전에 자신의 영향을 평가 하 고 완벽 하 게 적용 하기 전에 해당 효율성을 테스트 하려면 점진적으로 롤링 하는 것이 좋습니다. 예, 실수로 다양 한 사용자가 작업을 수행 하는 데 필요한 문서에 대 한 액세스를 차단 하는 새 DLP 정책을 원하지 합니다.</span><span class="sxs-lookup"><span data-stu-id="b47e3-p120">Before you create your DLP policies, you should consider rolling them out gradually to assess their impact and test their effectiveness before you fully enforce them. For example, you don't want a new DLP policy to unintentionally block access to thousands of documents that people require to get their work done.</span></span> 
    
    <span data-ttu-id="b47e3-189">이 순서에 따라 권장 하는 경우 큰 잠재적 영향을 주는 DLP 정책을 만들려는, 합니다.</span><span class="sxs-lookup"><span data-stu-id="b47e3-189">If you're creating DLP policies with a large potential impact, we recommend following this sequence:</span></span>
    
17. <span data-ttu-id="b47e3-p121">정책 설명이 없는 테스트 모드에서 시작하고 DLP 보고서를 사용하여 영향을 평가합니다. DLP 보고서를 사용하여 정책 일치의 횟수, 위치, 유형 및 심각도를 확인할 수 있습니다. 결과에 따라 필요에 맞게 규칙을 미세 조정할 수 있습니다. 테스트 모드에서 DLP 정책은 조직에서 작업하는 사용자의 생산성에 영향을 주지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b47e3-p121">Start in test mode without Policy Tips and then use the DLP reports to assess the impact. You can use DLP reports to view the number, location, type, and severity of policy matches. Based on the results, you can fine tune the rules as needed. In test mode, DLP policies will not impact the productivity of people working in your organization.</span></span> 
    
18. <span data-ttu-id="b47e3-p122">알림 및 정책 팁을 사용하여 테스트 모드로 전환하여 사용자에게 규정 준수 정책을 교육하고 적용될 규칙을 준비하도록 할 수 있습니다. 이 단계에서 규칙을 미세 조정할 수 있도록 사용자에게 가양성을 보고하도록 요청할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b47e3-p122">Move to Test mode with notifications and Policy Tips so that you can begin to teach users about your compliance policies and prepare them for the rules that are going to be applied. At this stage, you can also ask users to report false positives so that you can further refine the rules.</span></span>
    
19. <span data-ttu-id="b47e3-p123">규칙이 적용 되는 한 콘텐츠의 보호 되도록 정책을 설정 합니다. DLP 보고서 및 모든 문제 보고서 또는 결과 하 려 한다고 되는지 확인 하 라는 알림이 모니터링을 계속 합니다.</span><span class="sxs-lookup"><span data-stu-id="b47e3-p123">Turn on the policies so that the rules are enforced and the content's protected. Continue to monitor the DLP reports and any incident reports or notifications to make sure that the results are what you intend.</span></span> 
    
    ![테스트 모드를 사용 하 여 정책 설정에 대 한 옵션](media/49fafaac-c6cb-41de-99c4-c43c3e380c3a.png)
  
20. <span data-ttu-id="b47e3-199">이 정책에 대 한 설정을 검토 \> **만들기**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="b47e3-199">Review your settings for this policy \> choose **Create**.</span></span>
    
<span data-ttu-id="b47e3-200">만들어 DLP 정책을 설정 하 고 모든 콘텐츠 원본 SharePoint Online 사이트 이용 하거나 비즈니스 계정에 대 한 OneDrive 등을 포함 하는 정책을 자동으로 해당 콘텐츠에 규칙을 적용 하 고 시작 되는 위치에 배포 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b47e3-200">After you create and turn on a DLP policy, it's deployed to any content sources that it includes, such as SharePoint Online sites or OneDrive for Business accounts, where the policy begins automatically enforcing its rules on that content.</span></span>
  
## <a name="view-the-status-of-a-dlp-policy"></a><span data-ttu-id="b47e3-201">DLP 정책의 상태 보기</span><span class="sxs-lookup"><span data-stu-id="b47e3-201">View the status of a DLP policy</span></span>

<span data-ttu-id="b47e3-p124">언제 든 지 **데이터 손실 방지** 섹션의 보안 **정책** 페이지에서 DLP 정책을 상태를 볼 수 &amp; 준수 센터입니다. 여기서 테스트 모드에서 정책 인지 또는 정책을 성공적으로 사용 하거나 사용 하지 않도록 설정, 여부와 같은 중요 한 정보를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b47e3-p124">At any time, you can view the status of your DLP policies on the **Policy** page in the **Data loss prevention** section of the Security &amp; Compliance Center. Here you can find important information, such as whether a policy was successfully enabled or disabled, or whether the policy is in test mode.</span></span> 
  
<span data-ttu-id="b47e3-204">아래에는 기타 상태와 해당 의미가 나와 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b47e3-204">Here are the different statuses and what they mean.</span></span>
  
|<span data-ttu-id="b47e3-205">**상태**</span><span class="sxs-lookup"><span data-stu-id="b47e3-205">**Status**</span></span>|<span data-ttu-id="b47e3-206">**설명**</span><span class="sxs-lookup"><span data-stu-id="b47e3-206">**Explanation**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b47e3-207">**켜는 중…**</span><span class="sxs-lookup"><span data-stu-id="b47e3-207">**Turning on…**</span></span> <br/> |<span data-ttu-id="b47e3-p125">정책이 포함하는 콘텐츠 원본으로 배포 중입니다. 정책이 아직 모든 원본에 적용되지는 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="b47e3-p125">The policy is being deployed to the content sources that it includes. The policy is not yet enforced on all sources.</span></span>  <br/> |
|<span data-ttu-id="b47e3-210">**테스트 중(알림 사용)**</span><span class="sxs-lookup"><span data-stu-id="b47e3-210">**Testing, with notifications**</span></span> <br/> |<span data-ttu-id="b47e3-p126">정책이 테스트 모드입니다. 규칙의 작업이 적용되지 않지만 정책 일치 항목은 수집되고 DLP 보고서를 사용하여 볼 수 있습니다. 정책 일치 항목에 대한 알림이 지정된 받는 사람에게 전송됩니다.</span><span class="sxs-lookup"><span data-stu-id="b47e3-p126">The policy is in test mode. The actions in a rule are not applied, but policy matches are collected and can be viewed by using the DLP reports. Notifications about policy matches are sent to the specified recipients.</span></span>  <br/> |
|<span data-ttu-id="b47e3-214">**테스트 중(알림 사용 안 함)**</span><span class="sxs-lookup"><span data-stu-id="b47e3-214">**Testing, without notifications**</span></span> <br/> |<span data-ttu-id="b47e3-p127">정책이 테스트 모드입니다. 규칙의 작업이 적용되지 않지만 정책 일치 항목은 수집되고 DLP 보고서를 사용하여 볼 수 있습니다. 정책 일치 항목에 대한 알림이 지정된 받는 사람에게 전송되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b47e3-p127">The policy is in test mode. The actions in a rule are not applied, but policy matches are collected and can be viewed by using the DLP reports. Notifications about policy matches are not sent to the specified recipients.</span></span>  <br/> |
|<span data-ttu-id="b47e3-218">**설정**</span><span class="sxs-lookup"><span data-stu-id="b47e3-218">**On**</span></span> <br/> |<span data-ttu-id="b47e3-p128">정책이 활성 상태이며 적용됩니다. 정책이 모든 콘텐츠 원본으로 배포되었습니다.</span><span class="sxs-lookup"><span data-stu-id="b47e3-p128">The policy is active and enforced. The policy was successfully deployed to all its content sources.</span></span>  <br/> |
|<span data-ttu-id="b47e3-221">**끄는 중...**</span><span class="sxs-lookup"><span data-stu-id="b47e3-221">**Turning off…**</span></span> <br/> |<span data-ttu-id="b47e3-p129">정책이 포함하는 콘텐츠 원본에서 제거 중입니다. 정책이 여전히 활성 상태이며 일부 원본에 적용될 수 있습니다. 정책을 끄는 데 45시간까지 소요될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b47e3-p129">The policy is being removed from the content sources that it includes. The policy may still be active and enforced on some sources. Turning off a policy may take up to 45 minutes.</span></span>  <br/> |
|<span data-ttu-id="b47e3-225">**해제**</span><span class="sxs-lookup"><span data-stu-id="b47e3-225">**Off**</span></span> <br/> |<span data-ttu-id="b47e3-p130">정책이 활성 상태가 아니며 적용되지 않습니다. 정책에 대한 설정(원본, 키워드, 기간 등)은 저장됩니다.</span><span class="sxs-lookup"><span data-stu-id="b47e3-p130">The policy is not active and not enforced. The settings for the policy (sources, keywords, duration, etc) are saved.</span></span>  <br/> |
|<span data-ttu-id="b47e3-228">**삭제 중...**</span><span class="sxs-lookup"><span data-stu-id="b47e3-228">**Deleting…**</span></span> <br/> |<span data-ttu-id="b47e3-p131">정책이 삭제되는 중입니다. 정책이 활성 상태가 아니며 적용되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b47e3-p131">The policy is in the process of being deleted. The policy is not active and not enforced.</span></span>  <br/> |
   
## <a name="turn-off-a-dlp-policy"></a><span data-ttu-id="b47e3-231">DLP 정책 끄기</span><span class="sxs-lookup"><span data-stu-id="b47e3-231">Turn off a DLP policy</span></span>

<span data-ttu-id="b47e3-p132">편집 또는 DLP 정책을 언제 든 지 해제할 수 있습니다. 정책을 해제 정책에서 규칙을 모두 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b47e3-p132">You can edit or turn off a DLP policy at any time. Turning off a policy disables all of the rules in the policy.</span></span>
  
<span data-ttu-id="b47e3-234">편집 하거나 **정책** 페이지에서 DLP 정책을 해제 하려면 \> 정책을 선택 \> **정책을 편집**합니다.</span><span class="sxs-lookup"><span data-stu-id="b47e3-234">To edit or turn off a DLP policy, on the **Policy** page \> select the policy \> **Edit policy**.</span></span>
  
![정책 단추를 편집 합니다.](media/ce319e92-0519-44fe-9507-45a409eaefe4.png)
  
<span data-ttu-id="b47e3-236">또한 해제할 수 있습니다 각 규칙 개별적으로 정책을 편집 하 여 다음 설정/해제 하는 규칙의 **상태** 를 해제 위에서 설명한 대로 합니다.</span><span class="sxs-lookup"><span data-stu-id="b47e3-236">In addition, you can turn off each rule individually by editing the policy and then toggling off the **Status** of that rule, as described above.</span></span> 
  
## <a name="more-information"></a><span data-ttu-id="b47e3-237">추가 정보</span><span class="sxs-lookup"><span data-stu-id="b47e3-237">More information</span></span>

- [<span data-ttu-id="b47e3-238">데이터 손실 방지 정책 개요</span><span class="sxs-lookup"><span data-stu-id="b47e3-238">Overview of data loss prevention policies</span></span>](data-loss-prevention-policies.md)
    
- [<span data-ttu-id="b47e3-239">DLP 정책에 대한 알림 보내기 및 정책 팁 표시</span><span class="sxs-lookup"><span data-stu-id="b47e3-239">Send notifications and show policy tips for DLP policies</span></span>](use-notifications-and-policy-tips.md)
    
- [<span data-ttu-id="b47e3-240">FCI 또는 기타 속성을 갖는 문서를 보호하는 DLP 정책 만들기</span><span class="sxs-lookup"><span data-stu-id="b47e3-240">Create a DLP policy to protect documents with FCI or other properties</span></span>](protect-documents-that-have-fci-or-other-properties.md)
    
- [<span data-ttu-id="b47e3-241">DLP 정책 템플릿에 포함되는 내용</span><span class="sxs-lookup"><span data-stu-id="b47e3-241">What the DLP policy templates include</span></span>](what-the-dlp-policy-templates-include.md)
    
- [<span data-ttu-id="b47e3-242">중요 한 정보 유형 목록</span><span class="sxs-lookup"><span data-stu-id="b47e3-242">Sensitive information types inventory</span></span>](what-the-sensitive-information-types-look-for.md)
    

