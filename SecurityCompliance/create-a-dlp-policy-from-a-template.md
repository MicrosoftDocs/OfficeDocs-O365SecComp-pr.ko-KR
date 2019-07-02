---
title: 템플릿에서 DLP 정책 만들기
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 6/29/2018
audience: Admin
ms.topic: article
f1_keywords:
- ms.o365.cc.NewPolicyFromTemplate
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- M365-security-compliance
search.appverid:
- MET150
description: 'DLP 정책을 사용하여 가장 쉽고 가장 일반적인 방법은 Office 365에 포함된 템플릿 중 하나를 사용하는 것입니다. '
ms.openlocfilehash: 0f1cd4fdf08edcd747dc3d1bc92625dda49e50de
ms.sourcegitcommit: 0d5a863f48914eeaaf29f7d2a2022618de186247
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/15/2019
ms.locfileid: "34077714"
---
# <a name="create-a-dlp-policy-from-a-template"></a><span data-ttu-id="dcb99-103">템플릿에서 DLP 정책 만들기</span><span class="sxs-lookup"><span data-stu-id="dcb99-103">Create a DLP policy from a template</span></span>

<span data-ttu-id="dcb99-104">DLP 정책을 사용하여 가장 쉽고 가장 일반적인 방법은 Office 365에 포함된 템플릿 중 하나를 사용하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="dcb99-104">The easiest, most common way to get started with DLP policies is to use one of the templates included in Office 365.</span></span> <span data-ttu-id="dcb99-105">이러한 서식 파일 중 하나를 그대로 사용 하거나 조직의 특정 규정 준수 요구 사항을 충족 하도록 규칙을 사용자 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dcb99-105">You can use one of these templates as is, or customize the rules to meet your organization's specific compliance requirements.</span></span>
  
<span data-ttu-id="dcb99-p102">Office 365에는 광범위한 일반적인 규정 및 비즈니스 정책 요구를 충족하기 위해 바로 사용할 수 있는 40가지 이상의 템플릿이 포함되어 있습니다. 예를 들어 다음에 대한 DLP 정책 템플릿이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dcb99-p102">Office 365 includes over 40 ready-to-use templates that can help you meet a wide range of common regulatory and business policy needs. For example, there are DLP policy templates for:</span></span>
  
- <span data-ttu-id="dcb99-108">GLBA(Gramm-Leach-Bliley Act)</span><span class="sxs-lookup"><span data-stu-id="dcb99-108">Gramm-Leach-Bliley Act (GLBA)</span></span>
    
- <span data-ttu-id="dcb99-109">PCI-DSS(Payment Card Industry Data Security Standard)</span><span class="sxs-lookup"><span data-stu-id="dcb99-109">Payment Card Industry Data Security Standard (PCI-DSS)</span></span>
    
- <span data-ttu-id="dcb99-110">U.S. PII(United States Personally Identifiable Information)</span><span class="sxs-lookup"><span data-stu-id="dcb99-110">United States Personally Identifiable Information (U.S. PII)</span></span>
    
- <span data-ttu-id="dcb99-111">미국 HIPAA(Health Insurance Act)</span><span class="sxs-lookup"><span data-stu-id="dcb99-111">United States Health Insurance Act (HIPAA)</span></span>
    
<span data-ttu-id="dcb99-p103">기존 규칙을 수정하거나 새로 추가하여 템플릿을 미세 조정할 수 있습니다. 예를 들어 새로운 유형의 중요한 정보를 규칙에 추가하거나, 한 규칙의 템플릿 수를 수정하여 트리거하기 더 어렵게 또는 더 쉽게 만들거나, 업무 정당성을 제공하여 규칙의 작업을 재정의할 수 있도록 하거나, 알림 및 사고 보고서를 받을 수 있는 사람을 변경할 수 있습니다. DLP 정책 템플릿은 여러 일반적인 규정 준수 시나리오에 대한 유연한 시작점입니다.</span><span class="sxs-lookup"><span data-stu-id="dcb99-p103">You can fine tune a template by modifying any of the existing rules or adding new ones. For example, you can add new types of sensitive information to a rule, modify the counts in a rule to make it harder or easier to trigger, allow people to override the actions in a rule by providing a business justification, or change who notifications and incident reports are sent to. A DLP policy template is a flexible starting point for many common compliance scenarios.</span></span>
  
<span data-ttu-id="dcb99-115">기본 규칙이 없는 사용자 지정 템플릿을 선택하고, 조직의 특정 규정 준수 요구에 맞게 DLP 정책을 처음부터 새로 구성할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dcb99-115">You can also choose the Custom template, which has no default rules, and configure your DLP policy from scratch, to meet the specific compliance requirements for your organization.</span></span>
  
## <a name="example-identify-sensitive-information-across-all-onedrive-for-business-sites-and-restrict-access-for-people-outside-your-organization"></a><span data-ttu-id="dcb99-116">예: 모든 비즈니스용 OneDrive 사이트에서 중요 한 정보를 식별 하 고 조직 외부의 사용자에 대 한 액세스 제한</span><span class="sxs-lookup"><span data-stu-id="dcb99-116">Example: Identify sensitive information across all OneDrive for Business sites and restrict access for people outside your organization</span></span>

<span data-ttu-id="dcb99-117">비즈니스용 OneDrive 계정을 통해 조직의 사용자가 쉽게 문서를 공동 작업 하 고 공유할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dcb99-117">OneDrive for Business accounts make it easy for people across your organization to collaborate and share documents.</span></span> <span data-ttu-id="dcb99-118">그러나 규정 준수 관리자는 비즈니스용 OneDrive 계정에 저장 된 중요 한 정보가 실수로 조직 외부의 사용자와 공유 될 수 있다는 것을 고려해 야 합니다.</span><span class="sxs-lookup"><span data-stu-id="dcb99-118">But a common concern for compliance officers is that sensitive information stored in OneDrive for Business accounts may be inadvertently shared with people outside your organization.</span></span> <span data-ttu-id="dcb99-119">DLP 정책은 이러한 위험을 줄이는 데 도움이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dcb99-119">A DLP policy can help mitigate this risk.</span></span>
  
<span data-ttu-id="dcb99-120">이 예에서는 개별 Taxpayer 식별 번호 (ITIN), 주민 등록 번호 및 미국 여권 번호를 포함 하는 미국 PII 데이터를 식별 하는 DLP 정책을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="dcb99-120">In this example, you'll create a DLP policy that identifies U.S. PII data, which includes Individual Taxpayer Identification Numbers (ITIN), Social Security Numbers, and U.S. passport numbers.</span></span> <span data-ttu-id="dcb99-121">서식 파일을 사용 하 여 시작 하 고 조직의 규정 준수 요구 사항에 맞게 서식 파일을 수정 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="dcb99-121">You'll get started by using a template, and then you'll modify the template to meet your organization's compliance requirements—specifically, you'll:</span></span>
  
- <span data-ttu-id="dcb99-122">DLP 정책이 중요 한 데이터를 더 많이 보호 하도록 중요 한 정보 유형 (예를 들어, 은행 계좌 번호 및 미국 운전 면허 번호)을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="dcb99-122">Add a couple of types of sensitive information—U.S. bank account numbers and U.S. driver's license numbers—so that the DLP policy protects even more of your sensitive data.</span></span>
    
- <span data-ttu-id="dcb99-123">중요 한 정보가 한 번만 발생 하 여 외부 사용자에 대 한 액세스를 제한할 수 있도록 정책을 보다 중요 하 게 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="dcb99-123">Make the policy more sensitive, so that a single occurrence of sensitive information is enough to restrict access for external users.</span></span>
    
- <span data-ttu-id="dcb99-124">업무 정당성을 제공하거나 가양성을 보고하여 작업을 재정의할 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="dcb99-124">Allow users to override the actions by providing a business justification or reporting a false positive.</span></span> <span data-ttu-id="dcb99-125">이러한 방식으로 중요 한 정보를 공유 하는 유효한 비즈니스 이유가 있는 경우 DLP 정책은 조직의 사용자가 작업을 수행 하는 것을 막지 못합니다.</span><span class="sxs-lookup"><span data-stu-id="dcb99-125">This way, your DLP policy won't prevent people in your organization from getting their work done, provided they have a valid business reason for sharing the sensitive information.</span></span>
    
### <a name="create-a-dlp-policy-from-a-template"></a><span data-ttu-id="dcb99-126">템플릿에서 DLP 정책 만들기</span><span class="sxs-lookup"><span data-stu-id="dcb99-126">Create a DLP policy from a template</span></span>

1. <span data-ttu-id="dcb99-127">[https://protection.office.com](https://protection.office.com)으로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="dcb99-127">Go to [https://protection.office.com](https://protection.office.com).</span></span>
    
2. <span data-ttu-id="dcb99-128">회사 또는 학교 계정을 사용하여 Office 365에 로그인합니다.</span><span class="sxs-lookup"><span data-stu-id="dcb99-128">Sign in to Office 365 using your work or school account.</span></span> <span data-ttu-id="dcb99-129">현재는 Office 365 보안 &amp; 및 준수 센터에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dcb99-129">You're now in the Office 365 Security &amp; Compliance Center.</span></span>
    
3. <span data-ttu-id="dcb99-130">보안 &amp; 준수 센터 \> 왼쪽 탐색 \> **데이터 손실 방지** \> **정책** \> **+ 정책 만들기**</span><span class="sxs-lookup"><span data-stu-id="dcb99-130">In the Security &amp; Compliance Center \> left navigation \> **Data loss prevention** \> **Policy** \> **+ Create a policy**.</span></span>
    
    ![정책 만들기 단추](media/b1e48a08-92e2-47ca-abdc-4341694ddc7c.png)
  
4. <span data-ttu-id="dcb99-132">\> **다음**에 필요한 중요 한 정보 유형을 보호 하는 DLP 정책 템플릿을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="dcb99-132">Choose the DLP policy template that protects the types of sensitive information that you need \> **Next**.</span></span>
    
    <span data-ttu-id="dcb99-133">이 예에서는 보호 하려는 중요 한 정보의 유형이 대부분 포함 되어 있기 때문에 **개인 정보** \> 보호 및 **PII (개인 식별 정보) 데이터** 를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="dcb99-133">In this example, you'll select **Privacy** \> **U.S. Personally Identifiable Information ‎(PII)‎ Data** because it already includes most of the types of sensitive information that you want to protect—you'll add a couple later.</span></span> 
    
    <span data-ttu-id="dcb99-134">서식 파일을 선택 하는 경우 오른쪽에 설명 된 설명을 읽고 서식 파일에서 보호 하는 중요 한 정보 유형을 알 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dcb99-134">When you select a template, you can read the description on the right to learn what types of sensitive information the template protects.</span></span>
    
    ![DLP 정책 템플릿 선택을 위한 페이지](media/775266f6-ad87-4080-8d7c-97f2e7403b30.png)
  
5. <span data-ttu-id="dcb99-136">정책 \> 이름을 **다음**으로 합니다.</span><span class="sxs-lookup"><span data-stu-id="dcb99-136">Name the policy \> **Next**.</span></span>
    
6. <span data-ttu-id="dcb99-137">DLP 정책으로 보호 하려는 위치를 선택 하려면 다음 중 하나를 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="dcb99-137">To choose the locations that you want the DLP policy to protect, do one of the following:</span></span>
    
  - <span data-ttu-id="dcb99-138">\> \*\*\*\* **Office 365의 모든 위치를** 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="dcb99-138">Choose **All locations in Office 365** \> **Next**.</span></span>
    
  - <span data-ttu-id="dcb99-139">\> **다음**에 **특정 위치 선택을** 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="dcb99-139">Choose **Let me choose specific locations** \> **Next**.</span></span> <span data-ttu-id="dcb99-140">이 예에서는이를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="dcb99-140">For this example, choose this.</span></span>
    
    <span data-ttu-id="dcb99-141">모든 Exchange 전자 메일 또는 모든 OneDrive 계정 등의 전체 위치를 포함 하거나 제외 하려면 해당 위치의 **상태** 를 전환 하거나 설정/해제 합니다.</span><span class="sxs-lookup"><span data-stu-id="dcb99-141">To include or exclude an entire location such as all Exchange email or all OneDrive accounts, switch the **Status** of that location on or off.</span></span> 
    
    <span data-ttu-id="dcb99-142">특정 SharePoint 사이트 또는 비즈니스용 OneDrive 계정만 포함 하려면 **상태** 를 설정으로 전환한 다음 **포함** 아래의 링크를 클릭 하 여 특정 사이트 또는 계정을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="dcb99-142">To include only specific SharePoint sites or OneDrive for Business accounts, switch the **Status** to on, and then click the links under **Include** to choose specific sites or accounts.</span></span> <span data-ttu-id="dcb99-143">사이트에 정책을 적용하면 해당 정책에 구성된 규칙이 해당 사이트의 모든 하위 사이트에 자동으로 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="dcb99-143">When you apply a policy to a site, the rules configured in that policy are automatically applied to all subsites of that site.</span></span> 
    
    ![DLP 정책을 적용할 수 있는 위치에 대 한 옵션](media/ee50a61a-e867-4571-a150-3eec8d83650f.png)
  
    <span data-ttu-id="dcb99-145">이 예에서는 모든 비즈니스용 OneDrive 계정에 저장 된 중요 한 정보를 보호 하려면 **Exchange 전자 메일** 및 **SharePoint 사이트**에 대 한 **상태** 를 모두 해제 하 고 **OneDrive 계정**에 대 한 **상태** 를 유지 합니다.</span><span class="sxs-lookup"><span data-stu-id="dcb99-145">In this example, to protect sensitive information stored in all OneDrive for Business accounts, turn off the **Status** for both **Exchange email** and **SharePoint sites**, and leave the **Status** on for **OneDrive accounts**.</span></span>
    
7. <span data-ttu-id="dcb99-146">**고급 설정** \> 사용 **다음**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="dcb99-146">Choose **Use advanced settings** \> **Next**.</span></span>
    
8. <span data-ttu-id="dcb99-147">DLP 정책 템플릿에는 특정 유형의 중요한 정보를 검색하는 조건과 그에 따른 작업이 미리 정의된 규칙이 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dcb99-147">A DLP policy template contains predefined rules with conditions and actions that detect and act upon specific types of sensitive information.</span></span> <span data-ttu-id="dcb99-148">기존 규칙을 편집, 삭제 또는 해제 하거나 새로 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dcb99-148">You can edit, delete, or turn off any of the existing rules, or add new ones.</span></span> <span data-ttu-id="dcb99-149">완료 되 면 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="dcb99-149">When done, click **Next**.</span></span>
    
    ![미국 PII 정책 서식 파일에 확장 된 규칙](media/3bc9f1b6-f8ad-4334-863a-24448bb87687.png)
  
    <span data-ttu-id="dcb99-151">이 예에서 미국 PII 데이터 서식 파일에는 다음과 같은 두 가지 미리 정의 된 규칙이 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dcb99-151">In this example, the U.S. PII Data template includes two predefined rules:</span></span>
    
  - <span data-ttu-id="dcb99-152">**낮은 콘텐츠의 양이 검색 됨 미국 PII** 이 규칙은 조직 외부의 사용자와 파일을 공유 하는 세 가지 유형의 중요 한 정보 (ITIN, SSN, 미국 여권 번호)가 각각 1 ~ 10 개까지 포함 된 파일을 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="dcb99-152">**Low volume of content detected U.S. PII** This rule looks for files containing between 1 and 10 occurrences of each of three types of sensitive information (ITIN, SSN, and U.S. passport numbers), where the files are shared with people outside the organization.</span></span> <span data-ttu-id="dcb99-153">발견 된 경우 규칙은 기본 사이트 모음 관리자, 문서 소유자 및 문서를 마지막으로 수정한 사람에 게 전자 메일 알림을 보냅니다.</span><span class="sxs-lookup"><span data-stu-id="dcb99-153">If found, the rule sends an email notification to the primary site collection administrator, document owner, and person who last modified the document.</span></span> 
    
  - <span data-ttu-id="dcb99-154">**높은 양의 콘텐츠가 검색 됨 미국 PII** 이 규칙은 조직 외부의 사용자와 파일을 공유 하는 동일한 세 가지 중요 한 정보 유형이 각각 한 번 이상 발생 하는 파일을 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="dcb99-154">**High volume of content detected U.S. PII** This rule looks for files containing 10 or more occurrences of each of the same three sensitive information types, where the files are shared with people outside the organization.</span></span> <span data-ttu-id="dcb99-155">이 작업을 수행 하면 전자 메일 알림도 함께 전송 되 고 파일에 대 한 액세스가 제한 됩니다.</span><span class="sxs-lookup"><span data-stu-id="dcb99-155">If found, this action also sends an email notification, plus it restricts access to the file.</span></span> <span data-ttu-id="dcb99-156">비즈니스용 OneDrive 계정의 콘텐츠에 대 한 기본 사이트 모음 관리자, 문서 소유자 및 문서를 마지막으로 수정한 사람을 제외한 모든 사용자에 대해 문서에 대 한 사용 권한이 제한 됩니다.</span><span class="sxs-lookup"><span data-stu-id="dcb99-156">For content in a OneDrive for Business account, this means that permissions for the document are restricted for everyone except the primary site collection administrator, document owner, and person who last modified the document.</span></span> 
    
    <span data-ttu-id="dcb99-157">조직의 특정 요구 사항을 충족 하기 위해 중요 한 정보가 한 번 발생 하는 경우 외부 사용자에 대 한 액세스를 차단할 수 있도록 규칙을 보다 쉽게 트리거할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dcb99-157">To meet your organization's specific requirements, you may want to make the rules easier to trigger, so that a single occurrence of sensitive information is enough to block access for external users.</span></span> <span data-ttu-id="dcb99-158">이러한 규칙을 확인 한 후에는 낮은 및 높은 수 규칙이 필요 하지 않음을 이해 하 고 중요 한 정보가 발견 되 면 액세스를 차단 하는 규칙을 하나만 사용 하면 됩니다.</span><span class="sxs-lookup"><span data-stu-id="dcb99-158">After looking at these rules, you understand that you don't need low and high count rules—you need only a single rule that blocks access if any occurrence of sensitive information is found.</span></span>
    
    <span data-ttu-id="dcb99-159">따라서 **낮은 양의 콘텐츠에서 검색 된 규칙 (미국 PII** \> **삭제 규칙**)을 확장 합니다.</span><span class="sxs-lookup"><span data-stu-id="dcb99-159">So you expand the rule named **Low volume of content detected U.S. PII** \> **Delete rule**.</span></span>
    
    ![삭제 규칙 단추](media/bc36f7d2-0fae-4af1-92e8-95ba51077b12.png)
  
9. <span data-ttu-id="dcb99-161">이제이 예에서는 두 가지 중요 한 정보 유형 (미국 은행 계좌 번호 및 미국 운전 면허 번호)을 추가 하 고, 사용자가 규칙을 재정의 하 고, 수를 발생으로 변경 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="dcb99-161">Now, in this example, you need to add two sensitive information types (U.S. bank account numbers and U.S. driver's license numbers), allow people to override a rule, and change the count to any occurrence.</span></span> <span data-ttu-id="dcb99-162">이 모든 작업을 하나의 규칙을 편집 하 여 수행할 수 있으므로 **높은 양의 콘텐츠가 검색 된 미국 PII** \> **편집 규칙**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="dcb99-162">You can do all of this by editing one rule, so select **High volume of content detected U.S. PII** \> **Edit rule**.</span></span>
    
    ![규칙 편집 단추](media/eaf54067-4945-4c98-8dd6-fb2c5d6de075.png)
  
10. <span data-ttu-id="dcb99-164">중요 한 정보 유형을 추가 하려면 **조건** 섹션 \> 에서 **유형 추가 또는 변경을 변경**합니다.</span><span class="sxs-lookup"><span data-stu-id="dcb99-164">To add a sensitive information type, in the **Conditions** section \> **Add or change types**.</span></span> <span data-ttu-id="dcb99-165">그런 다음 **추가 또는 변경 유형** \> 에서 **추가** \> 를 선택 하 고 **미국 은행 계좌 번호** 및 **미국 운전 면허 번호** \> **추가** \> \*\*\*\* 를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="dcb99-165">Then, under **Add or change types** \> choose **Add** \> select **U.S. Bank Account Number** and **U.S. Driver's License Number** \> **Add** \> **Done**.</span></span>
    
    ![형식 추가 또는 변경 옵션](media/c6c3ae86-f7db-40a8-a6e4-db11692024be.png)
  
    ![형식 추가 또는 변경 창](media/fdbb96af-b914-4a6c-a97b-bbd014689965.png)
  
11. <span data-ttu-id="dcb99-168">개수 (규칙을 트리거하는 데 필요한 중요 한 정보의 인스턴스 수)를 변경 하려면 **인스턴스 개수** \> 에서 각 유형에 \> 대해 **최소값** 을 선택 하 고 1을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="dcb99-168">To change the count (the number of instances of sensitive information required to trigger the rule), under **Instance count** \> choose the **min** value for each type \> enter 1.</span></span> <span data-ttu-id="dcb99-169">최소 개수는 비워 둘 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="dcb99-169">The minimum count cannot be empty.</span></span> <span data-ttu-id="dcb99-170">최대 개수는 비어 있을 수 있습니다. 빈 **max** 값을 **any**로 변환 합니다.</span><span class="sxs-lookup"><span data-stu-id="dcb99-170">The maximum count can be empty; an empty **max** value convert to **any**.</span></span>
    
    <span data-ttu-id="dcb99-171">완료 되 면 모든 중요 한 정보 유형의 최소 개수가 **1** 이어야 하 고 최대 개수는 **any**여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="dcb99-171">When finished, the min count for all of the sensitive information types should be **1** and the max count should be **any**.</span></span> <span data-ttu-id="dcb99-172">즉, 이러한 유형의 중요 한 정보가 발생 하는 경우에는이 조건이 충족 됩니다.</span><span class="sxs-lookup"><span data-stu-id="dcb99-172">In other words, any occurrence of this type of sensitive information will satisfy this condition.</span></span>
    
    ![중요 한 정보 유형에 대 한 인스턴스 개수](media/5c6e08cb-59a9-4558-b54b-d899836d4737.png)
  
12. <span data-ttu-id="dcb99-174">최종 사용자 지정 기능을 사용 하는 경우에는 DLP 정책이 유효한 비즈니스 정당성을 갖고 있거나 가양성이 발생 하는 경우 해당 사용자에 게 작업을 차단 하 여 차단 작업을 무시 하는 옵션을 포함 하도록 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dcb99-174">For the final customization, you don't want your DLP policies to block people from doing their work when they have a valid business justification or encounter a false positive, so you want the user notification to include options to override the blocking action.</span></span>
    
    <span data-ttu-id="dcb99-175">**사용자 알림** 섹션에서이 규칙에 대 한 전자 메일 알림 및 정책 팁이 서식 파일에 기본적으로 설정 되어 있음을 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dcb99-175">In the **User notifications** section, you can see that email notifications and policy tips are turned on by default for this rule in the template.</span></span> 
    
    <span data-ttu-id="dcb99-176">**사용자 재정의** 섹션에서는 비즈니스 근거에 대 한 재정의가 설정 되어 있음을 확인할 수 있지만 가양성 보고서에 대 한 재정의는 사용 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="dcb99-176">In the **User overrides** section, you can see that overrides for a business justification are turned on, but overrides to report false positives are not.</span></span> <span data-ttu-id="dcb99-177">**규칙이 가양성으로 보고 되 면 자동으로 규칙 재정의를**선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="dcb99-177">Choose **Override the rule automatically if they report it as a false positive**.</span></span>
    
    ![사용자 알림 섹션 및 사용자 재정의 섹션](media/62720e7a-a939-4c03-b414-67748f3d64a0.png)
  
13. <span data-ttu-id="dcb99-179">규칙 편집기의 위쪽에서이 규칙의 이름을 미국 pii가 검색 된 기본 **높은 볼륨** 에서 해당 중요 한 정보 유형에 서 발생 하는 모든 **콘텐츠로** 변경 했습니다.</span><span class="sxs-lookup"><span data-stu-id="dcb99-179">At the top of the rule editor, change the name of this rule from the default **High volume of content detected U.S. PII** to **Any content detected with U.S. PII** because it's now triggered by any occurrence of its sensitive information types.</span></span> 
    
14. <span data-ttu-id="dcb99-180">규칙 편집기 \> 의 맨 아래에 **저장**합니다.</span><span class="sxs-lookup"><span data-stu-id="dcb99-180">At the bottom of the rule editor \> **Save**.</span></span>
    
15. <span data-ttu-id="dcb99-181">\> **다음**규칙에 대 한 조건 및 작업을 검토 하십시오.</span><span class="sxs-lookup"><span data-stu-id="dcb99-181">Review the conditions and actions for this rule \> **Next**.</span></span>
    
    <span data-ttu-id="dcb99-182">오른쪽에서 규칙에 대 한 **Status** 스위치를 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="dcb99-182">On the right, notice the **Status** switch for the rule.</span></span> <span data-ttu-id="dcb99-183">전체 정책을 해제 하면 해당 정책에 포함 된 모든 규칙도 꺼집니다.</span><span class="sxs-lookup"><span data-stu-id="dcb99-183">If you turn off an entire policy, all rules contained in the policy are also turned off.</span></span> <span data-ttu-id="dcb99-184">그러나 전체 정책을 해제 하지 않고 특정 규칙을 해제할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dcb99-184">However, here you can turn off a specific rule without turning off the entire policy.</span></span> <span data-ttu-id="dcb99-185">이 기능은 많은 수의 가양성을 생성하는 규칙을 조사해야 할 경우에 유용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dcb99-185">This can be useful when you need to investigate a rule that is generating a large number of false positives.</span></span> 
    
16. <span data-ttu-id="dcb99-186">다음 페이지에서 다음 사항을 읽고 이해 한 다음 규칙을 켤 지, 아니면 먼저 \> \*\*\*\* 테스트를 수행할지를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="dcb99-186">On the next page, read and understand the following, and then choose whether to turn on the rule or test it out first \> **Next**.</span></span>
    
     <span data-ttu-id="dcb99-187">DLP 정책을 만들기 전에, 완전히 적용하지 않은 상태에서 서서히 롤아웃하면서 영향을 평가하고 효율성을 테스트하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="dcb99-187">Before you create your DLP policies, you should consider rolling them out gradually to assess their impact and test their effectiveness before you fully enforce them.</span></span> <span data-ttu-id="dcb99-188">예를 들어 새 DLP 정책이 사용자가 작업을 완료 하는 데 필요한 수천 개의 문서에 대 한 액세스를 차단 하는 것을 원하지 않을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dcb99-188">For example, you don't want a new DLP policy to unintentionally block access to thousands of documents that people require to get their work done.</span></span> 
    
    <span data-ttu-id="dcb99-189">잠재적으로 큰 영향을 주는 DLP 정책을 만드는 경우에는 다음 순서를 따르는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="dcb99-189">If you're creating DLP policies with a large potential impact, we recommend following this sequence:</span></span>
    
17. <span data-ttu-id="dcb99-p121">정책 설명이 없는 테스트 모드에서 시작하고 DLP 보고서를 사용하여 영향을 평가합니다. DLP 보고서를 사용하여 정책 일치의 횟수, 위치, 유형 및 심각도를 확인할 수 있습니다. 결과에 따라 필요에 맞게 규칙을 미세 조정할 수 있습니다. 테스트 모드에서 DLP 정책은 조직에서 작업하는 사용자의 생산성에 영향을 주지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="dcb99-p121">Start in test mode without Policy Tips and then use the DLP reports to assess the impact. You can use DLP reports to view the number, location, type, and severity of policy matches. Based on the results, you can fine tune the rules as needed. In test mode, DLP policies will not impact the productivity of people working in your organization.</span></span> 
    
18. <span data-ttu-id="dcb99-p122">알림 및 정책 팁을 사용하여 테스트 모드로 전환하여 사용자에게 규정 준수 정책을 교육하고 적용될 규칙을 준비하도록 할 수 있습니다. 이 단계에서 규칙을 미세 조정할 수 있도록 사용자에게 가양성을 보고하도록 요청할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dcb99-p122">Move to Test mode with notifications and Policy Tips so that you can begin to teach users about your compliance policies and prepare them for the rules that are going to be applied. At this stage, you can also ask users to report false positives so that you can further refine the rules.</span></span>
    
19. <span data-ttu-id="dcb99-196">규칙이 적용 되 고 콘텐츠가 보호 되도록 정책을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dcb99-196">Turn on the policies so that the rules are enforced and the content's protected.</span></span> <span data-ttu-id="dcb99-197">DLP 보고서 및 문제 보고서나 알림을 계속 모니터링하여 결과가 의도한 대로 나타나는지 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="dcb99-197">Continue to monitor the DLP reports and any incident reports or notifications to make sure that the results are what you intend.</span></span> 
    
    ![테스트 모드를 사용 하 여 정책 설정에 대 한 옵션](media/49fafaac-c6cb-41de-99c4-c43c3e380c3a.png)
  
20. <span data-ttu-id="dcb99-199">이 정책 \> 에 대 한 설정을 검토 하 여 **만들기**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="dcb99-199">Review your settings for this policy \> choose **Create**.</span></span>
    
<span data-ttu-id="dcb99-200">DLP 정책을 만들고 켠 후에는 정책이 포함 된 모든 콘텐츠 원본 (예: SharePoint Online 사이트 또는 비즈니스용 OneDrive 계정)에 배포 되며 정책에서 해당 콘텐츠에 대 한 규칙을 자동으로 적용 하기 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="dcb99-200">After you create and turn on a DLP policy, it's deployed to any content sources that it includes, such as SharePoint Online sites or OneDrive for Business accounts, where the policy begins automatically enforcing its rules on that content.</span></span>
  
## <a name="view-the-status-of-a-dlp-policy"></a><span data-ttu-id="dcb99-201">DLP 정책의 상태 보기</span><span class="sxs-lookup"><span data-stu-id="dcb99-201">View the status of a DLP policy</span></span>

<span data-ttu-id="dcb99-202">언제 든 지 보안 &amp; 및 준수 센터의 **데이터 손실 방지** 섹션에 있는 **정책** 페이지에서 DLP 정책의 상태를 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dcb99-202">At any time, you can view the status of your DLP policies on the **Policy** page in the **Data loss prevention** section of the Security &amp; Compliance Center.</span></span> <span data-ttu-id="dcb99-203">여기에서 정책이 제대로 사용 또는 사용되지 않도록 설정되었는지 여부, 정책이 테스트 모드인지 여부 등의 중요 정보를 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dcb99-203">Here you can find important information, such as whether a policy was successfully enabled or disabled, or whether the policy is in test mode.</span></span> 
  
<span data-ttu-id="dcb99-204">아래에는 기타 상태와 해당 의미가 나와 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dcb99-204">Here are the different statuses and what they mean.</span></span>
  
|<span data-ttu-id="dcb99-205">**상태**</span><span class="sxs-lookup"><span data-stu-id="dcb99-205">**Status**</span></span>|<span data-ttu-id="dcb99-206">**설명**</span><span class="sxs-lookup"><span data-stu-id="dcb99-206">**Explanation**</span></span>|
|:-----|:-----|
|<span data-ttu-id="dcb99-207">**켜는 중…**</span><span class="sxs-lookup"><span data-stu-id="dcb99-207">**Turning on…**</span></span> <br/> |<span data-ttu-id="dcb99-p125">정책이 포함하는 콘텐츠 원본으로 배포 중입니다. 정책이 아직 모든 원본에 적용되지는 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="dcb99-p125">The policy is being deployed to the content sources that it includes. The policy is not yet enforced on all sources.</span></span>  <br/> |
|<span data-ttu-id="dcb99-210">**테스트 중(알림 사용)**</span><span class="sxs-lookup"><span data-stu-id="dcb99-210">**Testing, with notifications**</span></span> <br/> |<span data-ttu-id="dcb99-p126">정책이 테스트 모드입니다. 규칙의 작업이 적용되지 않지만 정책 일치 항목은 수집되고 DLP 보고서를 사용하여 볼 수 있습니다. 정책 일치 항목에 대한 알림이 지정된 받는 사람에게 전송됩니다.</span><span class="sxs-lookup"><span data-stu-id="dcb99-p126">The policy is in test mode. The actions in a rule are not applied, but policy matches are collected and can be viewed by using the DLP reports. Notifications about policy matches are sent to the specified recipients.</span></span>  <br/> |
|<span data-ttu-id="dcb99-214">**테스트 중(알림 사용 안 함)**</span><span class="sxs-lookup"><span data-stu-id="dcb99-214">**Testing, without notifications**</span></span> <br/> |<span data-ttu-id="dcb99-p127">정책이 테스트 모드입니다. 규칙의 작업이 적용되지 않지만 정책 일치 항목은 수집되고 DLP 보고서를 사용하여 볼 수 있습니다. 정책 일치 항목에 대한 알림이 지정된 받는 사람에게 전송되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="dcb99-p127">The policy is in test mode. The actions in a rule are not applied, but policy matches are collected and can be viewed by using the DLP reports. Notifications about policy matches are not sent to the specified recipients.</span></span>  <br/> |
|<span data-ttu-id="dcb99-218">**켜짐**</span><span class="sxs-lookup"><span data-stu-id="dcb99-218">**On**</span></span> <br/> |<span data-ttu-id="dcb99-p128">정책이 활성 상태이며 적용됩니다. 정책이 모든 콘텐츠 원본으로 배포되었습니다.</span><span class="sxs-lookup"><span data-stu-id="dcb99-p128">The policy is active and enforced. The policy was successfully deployed to all its content sources.</span></span>  <br/> |
|<span data-ttu-id="dcb99-221">**끄는 중...**</span><span class="sxs-lookup"><span data-stu-id="dcb99-221">**Turning off…**</span></span> <br/> |<span data-ttu-id="dcb99-p129">정책이 포함하는 콘텐츠 원본에서 제거 중입니다. 정책이 여전히 활성 상태이며 일부 원본에 적용될 수 있습니다. 정책을 끄는 데 45시간까지 소요될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dcb99-p129">The policy is being removed from the content sources that it includes. The policy may still be active and enforced on some sources. Turning off a policy may take up to 45 minutes.</span></span>  <br/> |
|<span data-ttu-id="dcb99-225">**해제**</span><span class="sxs-lookup"><span data-stu-id="dcb99-225">**Off**</span></span> <br/> |<span data-ttu-id="dcb99-p130">정책이 활성 상태가 아니며 적용되지 않습니다. 정책에 대한 설정(원본, 키워드, 기간 등)은 저장됩니다.</span><span class="sxs-lookup"><span data-stu-id="dcb99-p130">The policy is not active and not enforced. The settings for the policy (sources, keywords, duration, etc) are saved.</span></span>  <br/> |
|<span data-ttu-id="dcb99-228">**삭제 중 ...**</span><span class="sxs-lookup"><span data-stu-id="dcb99-228">**Deleting…**</span></span> <br/> |<span data-ttu-id="dcb99-p131">정책이 삭제되는 중입니다. 정책이 활성 상태가 아니며 적용되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="dcb99-p131">The policy is in the process of being deleted. The policy is not active and not enforced.</span></span>  <br/> |
   
## <a name="turn-off-a-dlp-policy"></a><span data-ttu-id="dcb99-231">DLP 정책 끄기</span><span class="sxs-lookup"><span data-stu-id="dcb99-231">Turn off a DLP policy</span></span>

<span data-ttu-id="dcb99-232">언제 든 지 DLP 정책을 편집 하거나 해제할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dcb99-232">You can edit or turn off a DLP policy at any time.</span></span> <span data-ttu-id="dcb99-233">정책을 해제 하면 정책의 모든 규칙이 사용 하지 않도록 설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="dcb99-233">Turning off a policy disables all of the rules in the policy.</span></span>
  
<span data-ttu-id="dcb99-234">DLP 정책을 편집 하거나 해제 하려면 **정책** 페이지 \> 에서 정책 \> **편집 정책을**선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="dcb99-234">To edit or turn off a DLP policy, on the **Policy** page \> select the policy \> **Edit policy**.</span></span>
  
![정책 편집 단추](media/ce319e92-0519-44fe-9507-45a409eaefe4.png)
  
<span data-ttu-id="dcb99-236">또한 정책을 편집한 다음 위에 설명 된 대로 해당 규칙의 **상태** 를 전환 하 여 각 규칙을 개별적으로 해제할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dcb99-236">In addition, you can turn off each rule individually by editing the policy and then toggling off the **Status** of that rule, as described above.</span></span> 
  
## <a name="more-information"></a><span data-ttu-id="dcb99-237">추가 정보</span><span class="sxs-lookup"><span data-stu-id="dcb99-237">More information</span></span>

- [<span data-ttu-id="dcb99-238">데이터 손실 방지 정책 개요</span><span class="sxs-lookup"><span data-stu-id="dcb99-238">Overview of data loss prevention policies</span></span>](data-loss-prevention-policies.md)
    
- [<span data-ttu-id="dcb99-239">DLP 정책에 대한 알림 보내기 및 정책 팁 표시</span><span class="sxs-lookup"><span data-stu-id="dcb99-239">Send notifications and show policy tips for DLP policies</span></span>](use-notifications-and-policy-tips.md)
    
- [<span data-ttu-id="dcb99-240">FCI 또는 기타 속성을 갖는 문서를 보호하는 DLP 정책 만들기</span><span class="sxs-lookup"><span data-stu-id="dcb99-240">Create a DLP policy to protect documents with FCI or other properties</span></span>](protect-documents-that-have-fci-or-other-properties.md)
    
- [<span data-ttu-id="dcb99-241">DLP 정책 템플릿에 포함되는 내용</span><span class="sxs-lookup"><span data-stu-id="dcb99-241">What the DLP policy templates include</span></span>](what-the-dlp-policy-templates-include.md)
    
- [<span data-ttu-id="dcb99-242">중요 한 정보 유형 목록</span><span class="sxs-lookup"><span data-stu-id="dcb99-242">Sensitive information types inventory</span></span>](what-the-sensitive-information-types-look-for.md)
    

