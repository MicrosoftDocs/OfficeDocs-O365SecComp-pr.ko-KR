---
title: 문서 삭제 정책 만들기
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 6/29/2018
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- SPO160
ms.assetid: 41b2ed73-eb8d-4429-945e-a8197894585a
description: 조직은 규정 준수, 법률 및 기타 규정 때문에 특정 기간 동안 문서 보존이 필요한 경우가 많습니다. 그렇지만 필요 이상으로 오랫동안 문서를 보존하면 조직은 법적 위험에 노출될 수 있습니다.
ms.openlocfilehash: 6bf4c0604708608ad7af064f4b32b57d33208a39
ms.sourcegitcommit: ede6230c2df398dc0a633e8f32ee0bfede0d5142
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/25/2018
ms.locfileid: "25002661"
---
# <a name="create-a-document-deletion-policy"></a><span data-ttu-id="cbf3f-104">문서 삭제 정책 만들기</span><span class="sxs-lookup"><span data-stu-id="cbf3f-104">Create a document deletion policy</span></span>

> [!IMPORTANT]
> <span data-ttu-id="cbf3f-p102">보존 정책 또는 보안에서 만든 레이블을 사용 하는 권장 앞으로 이동, &amp; 문서 삭제 정책 대신 준수 센터입니다. 문서 삭제 정책은 계속 보존 정책 나란히 작동 하지만를 유지 하거나 Office 365의 외부에서 콘텐츠를 삭제 해야 하는 경우 보존 정책을 사용 하는 것이 좋습니다. 자세한 내용은 [이러한 기능 대신 보존 정책 사용](retention-policies.md#use-a-retention-policy-instead-of-these-features)을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="cbf3f-p102">Moving forward, we recommend that you use a retention policy or labels created in the Security &amp; Compliance Center instead of a document deletion policy. Document deletion policies will continue to work side by side with retention policies, but if you need to retain or delete content anywhere in Office 365, we recommend that you use a retention policy. For more information, see [Use a retention policy instead of these features](retention-policies.md#use-a-retention-policy-instead-of-these-features).</span></span> 
  
<span data-ttu-id="cbf3f-p103">조직은 규정 준수, 법률 및 기타 규정 때문에 특정 기간 동안 문서 보존이 필요한 경우가 많습니다. 그렇지만 필요 이상으로 오랫동안 문서를 보존하면 조직은 법적 위험에 노출될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cbf3f-p103">Organizations are often required to retain documents for a certain period of time due to compliance, legal, or other regulations. However, retaining documents for longer than required can expose the organization to legal risk.</span></span>
  
<span data-ttu-id="cbf3f-110">문서 삭제 정책을 사용 하 여 있습니다 사전 위험을 줄일 수 특정 기간 후 사이트의 문서를 삭제 하 여 — 등 비즈니스 5 년이 문서를 만든 후 사이트에 대 한 사용자의 OneDrive에서 문서 삭제할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cbf3f-110">With a document deletion policy, you can proactively reduce risk by deleting documents in a site after a specific period of time—for example, you can delete documents in users' OneDrive for Business sites five years after the documents were created.</span></span> 
  
<span data-ttu-id="cbf3f-p104">문서 삭제 정책을 만든 후에 사이트 모음 서식 파일에 할당하여 해당 서식 파일에서 만들어진 모든 사이트 모음에서 해당 정책을 사용하도록 할 수 있습니다. 또한 특정 사이트 모음에 정책을 할당하여 해당 사이트 모음에 대한 서식 파일에 할당되었을 수 있는 정책을 재정의할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cbf3f-p104">After you create a document deletion policy, you can assign it to a site collection template, so that the policy is available to all site collections created from that template. You can also assign a policy to a specific a site collection, which overrides any policies that may have been assigned to the template for that site collection.</span></span>
  
![문서 삭제 정책 센터의 홈 페이지](media/IP-Document-Deletion-Policy-Center-home-page.png)
  
## <a name="policy-templates"></a><span data-ttu-id="cbf3f-114">정책 템플릿</span><span class="sxs-lookup"><span data-stu-id="cbf3f-114">Policy templates</span></span>

<span data-ttu-id="cbf3f-p105">문서 삭제 정책을 처음부터 직접 만들거나, 샘플 정책 중 하나를 사용할 수 있습니다. 준수 정책 센터에는 그대로 사용할 수도 있고, 기준 정책으로 사용한 다음 이름을 바꾸거나 수정할 수 있는 샘플 정책이 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cbf3f-p105">You can create a document deletion policy from scratch, or you can use one of the sample policies. The Compliance Policy Center includes sample policies that you can use as is, or you can use them as a starting point and then rename or modify them.</span></span>
  
![샘플 문서 삭제 정책](media/IP-Sample-deletion-policies.png)
  
## <a name="examples-of-how-to-use-document-deletion-policies"></a><span data-ttu-id="cbf3f-118">문서 삭제 정책 사용 방법의 예</span><span class="sxs-lookup"><span data-stu-id="cbf3f-118">Examples of how to use document deletion policies</span></span>

<span data-ttu-id="cbf3f-p106">사이트 모음 또는 사이트 모음 서식 파일 하나 이상의 정책을 할당 하 고 각 이러한 정책을 하나 이상의 규칙을 가질 수 있습니다. 그러나 사이트당를 활성화 하는 정책을 하나만 있을 수 및 언제 든 지 사이트 내에서 라이브러리에 대 한 활성 상태인 삭제 규칙을 하나만 있을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cbf3f-p106">A site collection or a site collection template can have one more policies assigned to it, and each of those policies can have one or more rules. However, there can be only one policy that's active per site, and there can be only one deletion rule that's active at any time for the libraries within the site.</span></span>
  
![정책 간 관계를 보여 주는 다이어그램](media/IP-Two-policies-four-rules.png)
  
<span data-ttu-id="cbf3f-122">또한 정책을 필수 또는 기본으로 선택하고 삭제 규칙을 기본 규칙으로 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cbf3f-122">In addition, you can select a policy as mandatory or default, and you can select a deletion rule as a default rule:</span></span> 
  
- <span data-ttu-id="cbf3f-p107">**필수 정책** 정책을 필수 항목으로 표시 되 면 사이트 모음 또는 서식 파일에 정책은 하나만 할당할 수 있습니다. 정책을 기본으로 표시 되어야 합니다 하 고 모든 사이트에 적용 됩니다. 사이트 소유자는 정책을 거부할 수 없으며 합니다.</span><span class="sxs-lookup"><span data-stu-id="cbf3f-p107">**Mandatory policy**When a policy is marked as mandatory, only one policy can be assigned to the site collection or template. The policy must be marked as default and will be applied to all sites. Site owners cannot opt out of the policy.</span></span>
    
- <span data-ttu-id="cbf3f-126">**기본 정책** 정책을 기본으로 설정 되 면 해당 정책이 사이트 소유자가 필요 없는 작업에 할당 된 모든 사이트에 자동으로 활성 상태가 합니다.</span><span class="sxs-lookup"><span data-stu-id="cbf3f-126">**Default policy**When a policy is set as default, the policy is automatically active in all sites that it's assigned to with no action required by site owner.</span></span>
    
- <span data-ttu-id="cbf3f-127">**기본 규칙** 삭제 규칙이 기본으로 설정 되 면 해당 정책을 사용 하는 사이트의 모든 라이브러리에 자동으로 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="cbf3f-127">**Default rule**When a deletion rule is set as default, it is automatically applied to all libraries in the sites that use the policy.</span></span>
    
<span data-ttu-id="cbf3f-128">다음 예제에서는 필수 정책 또는 기본 정책과 규칙을 사용하게 되는 경우를 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="cbf3f-128">The following examples explain when you might want to use a mandatory policy or default policies and rules.</span></span>
  
### <a name="example-1-apply-a-single-policy-with-a-single-rule-to-a-site-collection-template"></a><span data-ttu-id="cbf3f-129">예 1: 단일 규칙을 갖는 단일 정책을 사이트 모음 서식 파일에 적용</span><span class="sxs-lookup"><span data-stu-id="cbf3f-129">Example 1: Apply a single policy with a single rule to a site collection template</span></span>

<span data-ttu-id="cbf3f-p108">모든 비즈니스용 OneDrive 사이트 또는 모든 팀 사이트와 같이 광범위하고 구조화되지 않은 콘텐츠에 문서 삭제 정책을 적용하려고 할 수 있습니다. 단일 문서 삭제 정책이 사이트 모음 서식 파일에서 만든 모든 사이트에서 활성화되도록 하려면 다음을 수행합니다.</span><span class="sxs-lookup"><span data-stu-id="cbf3f-p108">You may want to enforce a document deletion policy across a broad range of unstructured content, such as all OneDrive for Business sites or all team sites. If you want to ensure that a single document deletion policy is active in all sites created from a site collection template, you can:</span></span>
  
1. <span data-ttu-id="cbf3f-132">단일 기본 삭제 규칙을 갖는 단일 정책을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="cbf3f-132">Create a single policy with a single default deletion rule.</span></span>
    
2. <span data-ttu-id="cbf3f-133">정책을 필수 및 기본 정책으로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="cbf3f-133">Set the policy as mandatory and default.</span></span>
    
3. <span data-ttu-id="cbf3f-134">정책을 사이트 모음 서식 파일에 할당합니다.</span><span class="sxs-lookup"><span data-stu-id="cbf3f-134">Assign the policy to a site collection template.</span></span>
    
<span data-ttu-id="cbf3f-p109">이 예제에서 기본 삭제 규칙은 서식 파일에서 만든 모든 사이트 모음의 모든 라이브러리에 적용되고 사이트 소유자는 정책을 거부할 수 없습니다. 이것이 문서 삭제 정책을 광범위하고 엄격하게 적용하는 가장 간단한 방법입니다.</span><span class="sxs-lookup"><span data-stu-id="cbf3f-p109">In this example, the default deletion rule will be applied to all libraries in all site collections created from the template, and site owners cannot opt out of the policy. This is the simplest way to broadly and rigidly enforce a document deletion policy.</span></span>
  
![단일 필수 정책을 보여 주는 다이어그램](media/IP-Example-1-doc-deletion-policies.png)
  
### <a name="example-2-apply-a-single-policy-with-several-rules-to-a-site-collection-template"></a><span data-ttu-id="cbf3f-138">예 2: 사이트 모음 서식 파일에 여러 규칙을 갖는 단일 정책을 적용합니다</span><span class="sxs-lookup"><span data-stu-id="cbf3f-138">Example 2: Apply a single policy with several rules to a site collection template</span></span>

<span data-ttu-id="cbf3f-p110">사이트 소유자가 사이트에 포함된 콘텐츠 유형을 가장 잘 아는 경우가 많으므로 사이트 소유자가 해당 사이트에 가장 적합한 삭제 규칙을 선택하도록 할 수 있습니다. 또한 사이트 소유자가 정책을 완전히 거부하도록 할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cbf3f-p110">Site owners often know best what type of content their site contains, so you may choose to allow site owners to select the deletion rule that best applies to their site. You may also want to allow site owners to opt out of a policy entirely.</span></span>
  
<span data-ttu-id="cbf3f-p111">정책을 거부하는 동시에 중앙에서는 계속 정책을 만들고 관리할 수 있습니다. 또한 하나의 정책 및 규칙을 기본으로 선택하여 사이트 소유자가 다른 정책을 선택하거나 정책을 거부할 때까지 한 가지 정책이 항상 적용되도록 선택할 수도 있습니다. 사이트 소유자에게 이러한 유연성을 제공하려면 다음을 수행합니다.</span><span class="sxs-lookup"><span data-stu-id="cbf3f-p111">At the same time, you can still centrally create and manage the policies. You can also select one policy and rule as the default, so that a policy is always in effect until the site owner chooses a different one or opts out. If you want to provide such flexibility to site owners, you can:</span></span>
  
1. <span data-ttu-id="cbf3f-143">여러 삭제 규칙이 있는 단일 정책을 만들고 규칙 하나를 기본 규칙으로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="cbf3f-143">Create a single policy with several deletion rules, and set one rule as the default.</span></span>
    
2. <span data-ttu-id="cbf3f-144">정책을 기본 정책으로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="cbf3f-144">Set the policy as the default policy.</span></span>
    
3. <span data-ttu-id="cbf3f-145">정책을 사이트 모음 서식 파일에 할당합니다.</span><span class="sxs-lookup"><span data-stu-id="cbf3f-145">Assign the policy to a site collection template.</span></span>
    
<span data-ttu-id="cbf3f-146">사이트 소유자는 대체 삭제 규칙 중 하나를 선택하거나, 정책을 거부하거나, 아무 작업도 수행하지 않고 기본 정책 및 규칙이 되도록 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cbf3f-146">Site owners can select one of the alternate deletion rules, opt out of the policy, or do nothing and be subject to the default policy and rule.</span></span>
  
![여러 규칙이 있는 정책을 보여 주는 다이어그램](media/IP-Example-2-doc-deletion-policies.png)
  
### <a name="example-3-apply-several-policies-with-one-or-more-rules-to-a-site-collection"></a><span data-ttu-id="cbf3f-148">예 3: 규칙을 하나 이상 갖는 여러 정책을 사이트 모음에 적용</span><span class="sxs-lookup"><span data-stu-id="cbf3f-148">Example 3: Apply several policies with one or more rules to a site collection</span></span>

<span data-ttu-id="cbf3f-p112">이 예제에서는 사이트 소유자가 여러 정책 중에서 정책을 선택할 수 있고, 선택한 후에는 여러 규칙 중에서 선택할 수 있으므로 최대의 유연성이 허용됩니다. 하나의 정책 및 규칙을 기본으로 설정하므로 사이트 소유자가 다른 정책을 선택하거나 정책을 거부할 때까지 한 가지 정책이 항상 적용됩니다. 정책 및 규칙을 기본으로 설정하지 않으면 사이트 소유자가 정책 및 규칙을 선택하여 적용할 때까지 사이트의 문서 라이브러리에 대한 어떤 정책이나 규칙도 활성 상태가 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="cbf3f-p112">This example provides the maximum flexibility to site owners because they can choose from several policies, and after selecting a policy they can often choose from several rules. One policy and rule are set as default, so that a policy is always in effect until the site owner chooses a different one or opts out. Note that if you do not set a policy and rule as the default, then no policies or rules will be active for the document libraries in the site until the site owner takes action to select and apply them.</span></span>
  
<span data-ttu-id="cbf3f-p113">앞의 두 예제와 달리, 이러한 정책은 사이트 모음 서식 파일이 아닌 특정 사이트 모음에 할당됩니다. 즉, 정책을 특정 사이트 모음의 콘텐츠에 대해 좀 더 구체적으로 조정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cbf3f-p113">Unlike the previous two examples, these policies are assigned to a specific site collection — not the site collection template. This means the policies can be more specifically tailored for the content in a specific site collection.</span></span>
  
<span data-ttu-id="cbf3f-p114">정책 및 규칙이 상속됩니다. 사이트 소유자는 사이트에 대한 정책과 규칙을 선택할 수 있으며 모든 하위 사이트는 상위 사이트에서 정책을 상속합니다. 그렇지만 하위 사이트 소유자는 다른 정책 및 규칙을 선택하여 상속을 끊을 수 있으며, 상속이 다시 끊어질 때까지 모든 하위 사이트에 해당 정책과 규칙이 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="cbf3f-p114">Policies and rules are inherited. Site owners can select a policy and rule for their site, and all subsites inherit the policy from the parent. However, an owner of a subsite can break inheritance by selecting a different policy and rule, which in turn applies to all subsites until inheritance is broken again.</span></span>
  
<span data-ttu-id="cbf3f-156">이 시나리오를 설정하려면 다음을 수행합니다.</span><span class="sxs-lookup"><span data-stu-id="cbf3f-156">To set up this scenario, you can:</span></span>
  
1. <span data-ttu-id="cbf3f-157">각각이 규칙을 하나 이상 포함하는 여러 정책을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="cbf3f-157">Create several policies that each contains one or more rules.</span></span>
    
2. <span data-ttu-id="cbf3f-158">정책 및 규칙을 기본으로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="cbf3f-158">Set a policy and rule as the default.</span></span>
    
3. <span data-ttu-id="cbf3f-159">정책을 특정 사이트 모음에 할당합니다.</span><span class="sxs-lookup"><span data-stu-id="cbf3f-159">Assign the policies to a specific site collection.</span></span>
    
<span data-ttu-id="cbf3f-160">또한 정책 및 규칙은 특정 사이트 모음에 맞게 조정되며 사이트 소유자는 자신의 사이트에 가장 적합한 정책 및 규칙을 선택하여 상속을 끊을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cbf3f-160">In addition, the policies and rules are tailored to a specific site collection, where site owners can break inheritance by selecting the policy and rule that best applies to their site.</span></span>
  
![여러 정책 및 규칙을 보여 주는 다이어그램](media/IP-Example-3-doc-deletion-policies.png)
  
## <a name="create-a-document-deletion-policy"></a><span data-ttu-id="cbf3f-162">문서 삭제 정책 만들기</span><span class="sxs-lookup"><span data-stu-id="cbf3f-162">Create a document deletion policy</span></span>

1. <span data-ttu-id="cbf3f-p115">Office 365Security에서 &amp; 준수 센터의 **데이터 관리** 로 이동 \> **보존**합니다. **삭제**에서 **SharePoint Online 및 비즈니스용 OneDrive에 대 한 문서 삭제 정책 관리를**클릭 합니다. 새 브라우저 탭에서 문서 삭제 정책 센터를 엽니다.</span><span class="sxs-lookup"><span data-stu-id="cbf3f-p115">In the Office 365Security &amp; Compliance Center, navigate to **Data management** \> **Retention**. Under **Delete**, click **Manage document deletion policies for SharePoint Online and OneDrive for Business**. The Document Deletion Policy Center opens in a new browser tab.</span></span>
    
    <span data-ttu-id="cbf3f-p116">보안에서 이동 처음으로 &amp; 문서 삭제 정책 센터로 준수 센터, 정책 센터 자동으로 만들어집니다. 또는 [사이트 모음을](http://go.microsoft.com/fwlink/p/?LinkID=404342) 만들고 **엔터프라이즈** 탭에서 **규정 준수 정책 센터** 를 선택 하 여 정책 센터를 수동으로 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cbf3f-p116">The first time you navigate from the Security &amp; Compliance Center to the Document Deletion Policy Center, the policy center is automatically created for you. Alternatively, you can manually create the policy center by [creating the site collection](http://go.microsoft.com/fwlink/p/?LinkID=404342) and choosing **Compliance Policy Center** on the **Enterprise** tab.</span></span> 
    
2. <span data-ttu-id="cbf3f-168">**삭제 정책**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="cbf3f-168">Choose **Deletion Policies**.</span></span>
    
    ![삭제 정책 옵션](media/IP-Deletion-Policies-option.png)
  
3. <span data-ttu-id="cbf3f-170">**새 항목**을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="cbf3f-170">Choose **new item**.</span></span>
    
4. <span data-ttu-id="cbf3f-p117">정책 이름 및 설명을 입력합니다. 사이트 소유자는 이 이름과 설명을 기반으로 사이트의 정책을 선택할 수 있으므로 올바른 정책을 선택하도록 충분한 정보를 포함해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="cbf3f-p117">Enter a policy name and description. Site owners may be selecting a policy for their site based on this name and description, so include enough information for them to choose the correct policy.</span></span>
    
5. <span data-ttu-id="cbf3f-173">규칙을 만들려면 **새로 만들기**를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="cbf3f-173">To create a rule, choose **New**.</span></span>
    
6. <span data-ttu-id="cbf3f-174">이름을 입력하고 다음 옵션을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="cbf3f-174">Enter a name and choose the following options:</span></span>
    
  - <span data-ttu-id="cbf3f-p118">규칙 됩니다 영구적으로 문서를 삭제 또는 휴지통으로 삭제 여부를 선택 합니다. 휴지통 항목을 사이트에서 영구적으로 삭제 되기 전에 2 단계 보안 네트워크를 제공 합니다. 휴지통에 대 한 자세한 내용은 [휴지통을 비우거나 파일을 복원](http://go.microsoft.com/fwlink/p/?LinkID=404348)을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="cbf3f-p118">Choose whether the rule will permanently delete documents or delete them to the Recycle Bin. The Recycle Bin provides a second-stage safety net before an item is permanently deleted from a site. For more information about the Recycle Bin, see [Empty the Recycle Bin or restore your files](http://go.microsoft.com/fwlink/p/?LinkID=404348).</span></span>
    
  - <span data-ttu-id="cbf3f-178">삭제 날짜를 문서가 만들어진 날짜부터 계산할지 또는 마지막으로 수정된 날짜부터 계산할지를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="cbf3f-178">Choose whether the deletion date is calculated from the date when a document was created or last modified.</span></span>
    
  - <span data-ttu-id="cbf3f-179">문서가 삭제될 기간으로 일, 월 또는 년 수를 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="cbf3f-179">Enter a number of days, months, or years as the time period after which a document will be deleted.</span></span>
    
  - <span data-ttu-id="cbf3f-p119">규칙이 기본 규칙인지 여부를 선택합니다. 처음 만든 규칙이 기본 규칙으로 자동 설정됩니다. 기본 규칙은 해당 정책을 사용하는 사이트의 모든 라이브러리에 자동으로 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="cbf3f-p119">Choose whether the rule is a default rule. The first rule that you create is automatically set as the default rule. A default rule is automatically applied to all libraries in the sites that use the policy.</span></span>
    
![새 삭제 규칙 페이지](media/IP-New-deletion-rule.png)
  
7. <span data-ttu-id="cbf3f-184">**저장**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="cbf3f-184">Click **Save**.</span></span>
    
8. <span data-ttu-id="cbf3f-p120">사이트 소유자가 사이트에 적용할 다른 규칙을 선택할 수 있도록 하려면 추가 규칙을 만듭니다. 사이트 소유자가 아무 작업도 수행하지 않을 경우 기본 규칙(있는 경우)이 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="cbf3f-p120">Create additional rules if you want site owners to be able to choose different rules to apply to their site. The default rule, if any, will be applied if the site owner takes no action.</span></span>
    
9. <span data-ttu-id="cbf3f-187">정책에서 규칙을 제거 하려면 규칙을 선택 하 고 **삭제**를 클릭 한 다음 **확인**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="cbf3f-187">To remove a rule from a policy, select the rule, click **Delete**, and then click **OK**.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="cbf3f-188">규칙을 삭제 하 고 정책을 기본 규칙을 포함 하지 않습니다 이면 해당 정책에 대 한 규칙이 적용 될 예정-즉, 문서가 삭제 됩니다.</span><span class="sxs-lookup"><span data-stu-id="cbf3f-188">If you delete a rule, and the policy does not contain a default rule, then no rule will be in effect for that policy—in other words, no documents will be deleted.</span></span> 
  
![정책에서 규칙 제거 확인 메시지](media/IP-Remove-rule-from-policy-message.png)
  
## <a name="assign-the-document-deletion-policy-to-a-site-collection-template"></a><span data-ttu-id="cbf3f-190">문서 삭제 정책을 사이트 모음 서식 파일에 할당</span><span class="sxs-lookup"><span data-stu-id="cbf3f-190">Assign the document deletion policy to a site collection template</span></span>

<span data-ttu-id="cbf3f-191">사이트 모음 서식 파일에 정책을 할당해 기존 사이트 모음과 앞으로 만들어질 사이트 모음을 모두 포함하여, 해당 서식 파일에서 만드는 모든 사이트 모음에서 해당 정책을 사용할 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="cbf3f-191">By assigning a policy to a site collection template, you make the policy available to all site collections created from that template, including both existing site collections and site collections created in the future.</span></span>
  
<span data-ttu-id="cbf3f-p121">것 이라는 문서에 대해 지정 된 기간이 삭제 정책 의미 시간 이후에 문서를 만들거나 수정, 정책이 할당 된 이후 시간이 아니라 이해 하는 것이 중요 합니다. 사이트의 모든 문서 계산 되는 처음에 대 한 정책을 할당 하는 경우 하 고 조건을 만족 하는 경우 삭제 됩니다. 이 모든 기존 문서를 정책이 할당 된 후에 만든 단지 새 문서에 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="cbf3f-p121">It's important to understand that the time period specified for a document deletion policy means the time since the document was created or modified, not the time since the policy was assigned. When you assign the policy for the first time, all documents in the site are evaluated and, if they meet the criteria, they will be deleted. This applies to all existing documents, not just new documents created since the policy was assigned.</span></span>
  
1. <span data-ttu-id="cbf3f-p122">보안에서 &amp; 준수 센터의 **데이터 관리** 로 이동 \> **보존**합니다. **삭제**에서 **SharePoint Online 및 비즈니스용 OneDrive에 대 한 문서 삭제 정책 관리를**클릭 합니다. 새 브라우저 탭에서 문서 삭제 정책 센터를 엽니다.</span><span class="sxs-lookup"><span data-stu-id="cbf3f-p122">In the Security &amp; Compliance Center, navigate to **Data management** \> **Retention**. Under **Delete**, click **Manage document deletion policies for SharePoint Online and OneDrive for Business**. The Document Deletion Policy Center opens in a new browser tab.</span></span>
    
2. <span data-ttu-id="cbf3f-198">**서식 파일에 대한 정책 할당**을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="cbf3f-198">Choose **Policy Assignments for Templates**.</span></span>
    
    ![서식 파일에 대한 정책 할당 옵션](media/IP-Policy-Assignments-for-Templates-option.png)
  
3. <span data-ttu-id="cbf3f-200">**새 항목**을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="cbf3f-200">Choose **new item**.</span></span>
    
4. <span data-ttu-id="cbf3f-201">다음 중 하나를 수행합니다.</span><span class="sxs-lookup"><span data-stu-id="cbf3f-201">Do one of the following:</span></span>
    
  - <span data-ttu-id="cbf3f-202">팀 사이트 서식 파일과 같은 사이트 모음 서식 파일에 정책을 할당하려면 **사이트 모음 서식 파일에 할당**을 선택하고 사이트 모음 서식 파일을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="cbf3f-202">To assign the policy to a site collection template such as the Team Site template, select **Assign to site collection template**, and then select the site collection template.</span></span>
    
  - <span data-ttu-id="cbf3f-203">비즈니스에 대 한 사용자의 One Drive에 정책을 할당 하려면 **비즈니스 서식 파일에 대 한 OneDrive에 할당**을 아래에 강조 표시를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="cbf3f-203">To assign the policy to users' One Drive for Business, choose **Assign to OneDrive for Business Template**, highlighted below.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="cbf3f-204">사이트 모음 서식 파일에 정책을 할당하면 해당 서식 파일에서 만든 기존 사이트 모음과 앞으로 만들어질 사이트 모음 둘 다에서 해당 정책을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cbf3f-204">When you assign a policy to a site collection template, that policy will be available both to existing site collections created from that template and to site collections created in the future.</span></span> 
  
![OneDrive 옵션을 표시하는 서식 파일 페이지 선택](media/IP-Choose-a-template.png)
  
5. <span data-ttu-id="cbf3f-206">**저장**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="cbf3f-206">Click **Save**.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="cbf3f-p123">각 서식 파일에 할당 된 정책 집합이 하나만 가질 수 있습니다. 이 서식 파일에 할당 된 정책에 이미 없다는 오류가 표시 되 면 선택 **취소** \> 왼쪽된 탐색에서 **사이트 모음에 할당** 을 \> 보고 이미 지정 된 정책 집합을 관리 하는 사이트 모음을 선택 합니다. 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="cbf3f-p123">Each template can have only one set of policies assigned to it. If you see an error saying that this template already has policies assigned to it, choose **Cancel** \> **Assign to Site Collection** in the left navigation \> select a site collection to view and manage the set of policies that are already assigned.</span></span> 
  
6. <span data-ttu-id="cbf3f-p124">할당 하 고 하나의 정책이 기본 정책 인지 여부를 선택 하려는 정책을 선택, **할당 된 정책 관리**를 선택 합니다. 기본 정책을 설정할 때 정책에 자동으로 할당 하는 모든 사이트 정책이 현재 작업이 사이트 소유자가 필요 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="cbf3f-p124">Choose **Manage Assigned Policies**, select the policies that you want to assign, and then choose whether one policy is the default policy. When you set a default policy, all sites assigned to the policy automatically have the policy active with no action required by site owner.</span></span>
    
    ![정책 추가 및 관리 페이지](media/IP-Add-and-manage-policies-page.png)
  
7. <span data-ttu-id="cbf3f-212">**저장**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="cbf3f-212">Click **Save**.</span></span>
    
8. <span data-ttu-id="cbf3f-p125">사이트 소유자가 거부하도록 허용하지 않으면서 모든 사이트에 정책을 적용하려면 **필수 정책으로 표시**를 선택합니다. 필수 정책으로 지정하면 해당 정책 하나만 사이트 모음 서식 파일에 할당될 수 있습니다. 또한 해당 정책이 기본 정책으로 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="cbf3f-p125">If you want to enforce the policy on all sites without allowing site owners to opt out, choose **Mark Policy as Mandatory**. When you make a policy mandatory, only that single policy can be assigned to the site collection template. The policy must also be marked as default.</span></span>
    
    <span data-ttu-id="cbf3f-216">이 옵션이 회색으로 표시되면 **할당된 정책 관리**를 선택한 후 정책이 하나 이상 할당되고 기본으로 설정되는지 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="cbf3f-216">If this option is grayed out, choose **Manage Assigned Policies** and make sure that at least one policy is assigned and set as default.</span></span> 
    
9. <span data-ttu-id="cbf3f-217">**저장**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="cbf3f-217">Click **Save**.</span></span>
    
## <a name="assign-the-document-deletion-policy-to-a-site-collection"></a><span data-ttu-id="cbf3f-218">문서 삭제 정책을 사이트 모음에 할당</span><span class="sxs-lookup"><span data-stu-id="cbf3f-218">Assign the document deletion policy to a site collection</span></span>

<span data-ttu-id="cbf3f-p126">특정 사이트 모음에 정책을 할당하여 해당 특정 사이트 모음에서만 정책을 사용하도록 할 수 있습니다. 즉, 사이트 모음의 콘텐츠에 더욱 유사하게 정책을 조정할 수 있습니다. 또한 특정 사이트 모음에 할당된 정책은 해당 사이트 모음에 대한 서식 파일에 할당된 모든 정책을 재정의합니다. 예를 들어 판매 부서 사이트 모음에 할당된 정책(팀 사이트 서식 파일에서 생성)은 팀 사이트 서식 파일에 할당된 모든 정책을 재정의합니다.</span><span class="sxs-lookup"><span data-stu-id="cbf3f-p126">By assigning a policy to a specific site collection, you make the policy available only to that specific site collection. This means you can tailor policies more closely to the content in the site collection. Also, policies assigned to a specific site collection will override any policies that are assigned to the template for that site collection. For example, a policy assigned to the Sales Department site collection (created from the Team Site template) will override any policies assigned to the Team Site template.</span></span>
  
<span data-ttu-id="cbf3f-p127">것 이라는 문서에 대해 지정 된 기간이 삭제 정책 의미 시간 이후에 문서를 만들거나 수정, 정책이 할당 된 이후 시간이 아니라 이해 하는 것이 중요 합니다. 사이트의 모든 문서 계산 되는 처음에 대 한 정책을 할당 하는 경우 하 고 조건을 만족 하는 경우 삭제 됩니다. 이 모든 기존 문서를 정책이 할당 된 후에 만든 단지 새 문서에 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="cbf3f-p127">It's important to understand that the time period specified for a document deletion policy means the time since the document was created or modified, not the time since the policy was assigned. When you assign the policy for the first time, all documents in the site are evaluated and, if they meet the criteria, they will be deleted. This applies to all existing documents, not just new documents created since the policy was assigned.</span></span>
  
1. <span data-ttu-id="cbf3f-p128">보안에서 &amp; 준수 센터의 **데이터 관리** 로 이동 \> **보존**합니다. **삭제**, 아래에서 **SharePoint Online 및 비즈니스용 OneDrive에 대 한 문서 삭제 정책 관리를**선택 합니다. 새 브라우저 탭에서 문서 삭제 정책 센터를 엽니다.</span><span class="sxs-lookup"><span data-stu-id="cbf3f-p128">In the Security &amp; Compliance Center, navigate to **Data management** \> **Retention**. Under **Delete**, choose **Manage document deletion policies for SharePoint Online and OneDrive for Business**. The Document Deletion Policy Center opens in a new browser tab.</span></span>
    
2. <span data-ttu-id="cbf3f-229">**사이트 모음에 대한 정책 할당**을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="cbf3f-229">Choose **Policy Assignments for Site Collections**.</span></span>
    
    ![사이트 모음에 대한 정책 할당 옵션](media/IP-Policy-Assignments-for-Site-Collections-option.png)
  
3. <span data-ttu-id="cbf3f-231">**새 항목**을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="cbf3f-231">Choose **new item**.</span></span>
    
4. <span data-ttu-id="cbf3f-p129">**Choose 사이트 모음을**선택 합니다. 이름 또는 URL로 사이트 모음에 대 한 검색 하 고, 사이트 모음을 선택 하 고 및 **저장**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="cbf3f-p129">Choose **Choose a site collection**. Search for the site collection by name or URL, select the site collection and click **Save**.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="cbf3f-p130">각 사이트 모음에 할당 된 정책 집합이 하나만 가질 수 있습니다. 이미이 사이트 모음에 할당 된 정책이 없다는 오류가 표시 되 면 선택 **취소** \> **사이트 모음에 할당** 하 고 사이트 모음 선택을 보고 하 여 이미 할당 된 정책 집합을 관리 합니다.</span><span class="sxs-lookup"><span data-stu-id="cbf3f-p130">Each site collection can have only one set of policies assigned to it. If you see an error saying that this site collection already has policies assigned to it, choose **Cancel** \> **Assign to Site Collection** and select a site collection to view and manage the set of policies that are already assigned.</span></span> 
  
![사이트 모음 선택 페이지](media/IP-Choose-a-site-collection-page.png)
  
5. <span data-ttu-id="cbf3f-p131">할당 하 고 하나의 정책이 기본 정책 인지 여부를 선택 하려는 정책을 선택, **할당 된 정책 관리**를 선택 합니다. 기본 정책을 설정할 때 정책에 자동으로 할당 하는 모든 사이트 정책이 현재 작업이 사이트 소유자가 필요 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="cbf3f-p131">Choose **Manage Assigned Policies**, select the policies that you want to assign, and then choose whether one policy is the default policy. When you set a default policy, all sites assigned to the policy automatically have the policy active with no action required by site owner.</span></span>
    
    ![정책 추가 및 관리 페이지](media/IP-Add-and-manage-policies-page.png)
  
6. <span data-ttu-id="cbf3f-240">**저장**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="cbf3f-240">Click **Save**.</span></span>
    
7. <span data-ttu-id="cbf3f-p132">사이트 소유자가 거부하도록 허용하지 않으면서 모든 사이트에 정책을 적용하려면 **필수 정책으로 표시**를 선택합니다. 필수 정책으로 지정하면 해당 정책 하나만 사이트 모음에 할당될 수 있습니다. 또한 해당 정책이 기본 정책으로 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="cbf3f-p132">If you want to enforce the policy on all sites without allowing site owners to opt out, choose **Mark Policy as Mandatory**. When you make a policy mandatory, only that single policy can be assigned to the site collection. The policy must also be marked as default.</span></span>
    
    <span data-ttu-id="cbf3f-244">이 옵션이 회색으로 표시되면 **할당된 정책 관리**를 선택한 후 정책이 하나 이상 할당되고 기본으로 설정되는지 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="cbf3f-244">If this option is grayed out, choose **Manage Assigned Policies** and make sure that at least one policy is assigned and set as default.</span></span> 
    
8. <span data-ttu-id="cbf3f-245">**저장**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="cbf3f-245">Click **Save**.</span></span>
    
## <a name="delete-a-policy-assignment"></a><span data-ttu-id="cbf3f-246">정책 할당 삭제</span><span class="sxs-lookup"><span data-stu-id="cbf3f-246">Delete a policy assignment</span></span>

<span data-ttu-id="cbf3f-247">할당을 삭제하면 할당된 정책이 사이트 모음 또는 사이트 모음 서식 파일의 사이트에 더 이상 할당되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="cbf3f-247">When you delete an assignment, the assigned policies will no longer apply to any sites in the site collection or site collection template.</span></span>
  
1. <span data-ttu-id="cbf3f-p133">보안에서 &amp; 준수 센터의 **데이터 관리** 로 이동 \> **보존**합니다. **삭제**, 아래에서 **SharePoint Online 및 비즈니스용 OneDrive에 대 한 문서 삭제 정책 관리를**선택 합니다. 새 브라우저 탭에서 문서 삭제 정책 센터를 엽니다.</span><span class="sxs-lookup"><span data-stu-id="cbf3f-p133">In the Security &amp; Compliance Center, navigate to **Data management** \> **Retention**. Under **Delete**, choose **Manage document deletion policies for SharePoint Online and OneDrive for Business**. The Document Deletion Policy Center opens in a new browser tab.</span></span>
    
2. <span data-ttu-id="cbf3f-251">**서식 파일에 대한 정책 할당** 또는 **사이트 모음에 대한 정책 할당**을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="cbf3f-251">Choose either **Policy Assignments for Templates** or **Policy Assignments for Site Collections**.</span></span>
    
3. <span data-ttu-id="cbf3f-252">배정 항목을 선택 하 고 **항목 삭제**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="cbf3f-252">Select the assignment item and click **Delete Item**.</span></span>
    
    ![정책 할당에 대한 항목 명령 삭제](media/IP-Delete-policy-assignment.png)
  
## <a name="delete-a-policy"></a><span data-ttu-id="cbf3f-254">정책 삭제</span><span class="sxs-lookup"><span data-stu-id="cbf3f-254">Delete a policy</span></span>

<span data-ttu-id="cbf3f-p134">사용 중인 정책을 삭제할 수 없습니다. 사이트 모음 및 해당 정책을 포함 하는 사이트 모음 서식 파일에 할당을 모두 삭제 하려면 먼저 필요한 정책을 삭제할 수 있습니다, 전에-이전 섹션을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="cbf3f-p134">You can't delete a policy that's in use. Before you can delete a policy, you first need to delete all assignments to site collections and site collection templates that include that policy—see the previous section.</span></span>
  
1. <span data-ttu-id="cbf3f-p135">보안에서 &amp; 준수 센터 \> **데이터 관리** 를 선택 \> 의 왼쪽된 탐색 영역에서 **보존** \> **삭제** 에서 \> SharePoint Online 및 OneDrive **관리 문서 삭제 정책 비즈니스를 위한**합니다. 새 브라우저 탭에서 문서 삭제 정책 센터를 엽니다.</span><span class="sxs-lookup"><span data-stu-id="cbf3f-p135">In the Security &amp; Compliance Center \> choose **Data management** \> **Retention** in the left navigation \> under **Delete** \> **Manage document deletion policies for SharePoint Online and OneDrive for Business**. The Document Deletion Policy Center opens in a new browser tab.</span></span>
    
2. <span data-ttu-id="cbf3f-259">선택 \* \* 삭제 정책 \* \*.</span><span class="sxs-lookup"><span data-stu-id="cbf3f-259">Choose \*\* Deletion Policies \*\*.</span></span>
    
    ![삭제 정책 옵션](media/IP-Deletion-Policies-option.png)
  
3. <span data-ttu-id="cbf3f-261">정책을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="cbf3f-261">Select the policy.</span></span>
    
4. <span data-ttu-id="cbf3f-262">리본 메뉴에서 \> **항목** 탭 \> **정책을 제거**합니다.</span><span class="sxs-lookup"><span data-stu-id="cbf3f-262">On the Ribbon \> **Items** tab \> **Remove Policy**.</span></span>
    
    ![리본의 정책 제거 단추](media/IP-Remove-Policy-button-on-Ribbon.png)
  
5. <span data-ttu-id="cbf3f-p136">정책이 사용 되 고 있는 경우 여기에서 사용 하는 사이트 모음의 모든에서 정책을 제거 하려면 라는 수 나타납니다. 확실, **확인**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="cbf3f-p136">If the policy is in use, you'll be asked if you want to remove the policy from all of the site collections where it's being used. If you're sure, choose **OK**.</span></span>
    
    ![정책 확인 메시지 삭제](media/IP-Delete-policy-confirmation.png)
  
## <a name="see-also"></a><span data-ttu-id="cbf3f-267">참고 항목</span><span class="sxs-lookup"><span data-stu-id="cbf3f-267">See also</span></span>

[<span data-ttu-id="cbf3f-268">문서 삭제 정책 개요</span><span class="sxs-lookup"><span data-stu-id="cbf3f-268">Overview of document deletion policies</span></span>](document-deletion-policies.md)

[<span data-ttu-id="cbf3f-269">사이트에 문서 삭제 정책 적용 또는 제거</span><span class="sxs-lookup"><span data-stu-id="cbf3f-269">Apply or remove a document deletion policy for a site</span></span>](apply-or-remove-a-document-deletion-policy-for-a-site.md)
 

