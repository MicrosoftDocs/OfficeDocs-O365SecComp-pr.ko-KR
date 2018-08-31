---
title: 문서 삭제 정책 개요
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 6/12/2017
ms.audience: Admin
ms.topic: overview
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- SPO160
ms.assetid: 55e8d858-f278-482b-a198-2e62d6a2e6e5
description: 법적, 규정 준수로 인해 시간 기간에 대 한 문서 또는 기타 비즈니스 요구를 유지 하려면 조직 필요할 수 있습니다. 그러나 필요한 것 보다 긴 문서를 유지 하는 조직, 불필요 한 법적 위험을 만듭니다. 문서 삭제 정책을 사용 하 여 있습니다 사전 위험을 줄일 수 특정 기간 후 사이트의 문서를 삭제 하 여 — 등 비즈니스 5 년이 문서를 만든 후 사이트에 대 한 사용자의 OneDrive에서 문서 삭제할 수 있습니다.
ms.openlocfilehash: 495dd781c56e25e884d47f72a7e48410ea340208
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/27/2018
ms.locfileid: "23013662"
---
# <a name="overview-of-document-deletion-policies"></a><span data-ttu-id="32a70-105">문서 삭제 정책 개요</span><span class="sxs-lookup"><span data-stu-id="32a70-105">Overview of document deletion policies</span></span>

> [!IMPORTANT]
> <span data-ttu-id="32a70-p102">보존 정책 또는 보안에서 만든 레이블을 사용 하는 권장 앞으로 이동, &amp; 문서 삭제 정책 대신 준수 센터입니다. 문서 삭제 정책은 계속 보존 정책 나란히 작동 하지만를 유지 하거나 Office 365의 외부에서 콘텐츠를 삭제 해야 하는 경우 보존 정책을 사용 하는 것이 좋습니다. 자세한 내용은 [이러한 기능 대신 보존 정책 사용](retention-policies.md#use-a-retention-policy-instead-of-these-features)을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="32a70-p102">Moving forward, we recommend that you use a retention policy or labels created in the Security &amp; Compliance Center instead of a document deletion policy. Document deletion policies will continue to work side by side with retention policies, but if you need to retain or delete content anywhere in Office 365, we recommend that you use a retention policy. For more information, see [Use a retention policy instead of these features](retention-policies.md#use-a-retention-policy-instead-of-these-features).</span></span>
  
<span data-ttu-id="32a70-p103">법적, 규정 준수로 인해 시간 기간에 대 한 문서 또는 기타 비즈니스 요구를 유지 하려면 조직 필요할 수 있습니다. 그러나 필요한 것 보다 긴 문서를 유지 하는 조직, 불필요 한 법적 위험을 만듭니다. 문서 삭제 정책을 사용 하 여 있습니다 사전 위험을 줄일 수 특정 기간 후 사이트의 문서를 삭제 하 여 — 등 비즈니스 5 년이 문서를 만든 후 사이트에 대 한 사용자의 OneDrive에서 문서 삭제할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="32a70-p103">Your organization may be required to retain documents for a period of time because of compliance, legal, or other business requirements. However, if your organization keeps documents longer than required, you create unnecessary legal risk. With a document deletion policy, you can proactively reduce risk by deleting documents in a site after a specific period of time—for example, you can delete documents in users' OneDrive for Business sites five years after the documents were created.</span></span>
  
<span data-ttu-id="32a70-112">문서 삭제 정책은 강력한 아직 유연한 — 등을 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="32a70-112">Document deletion policies are powerful yet flexible—for example, you can:</span></span>
  
- <span data-ttu-id="32a70-p104">사이트 소유자가 중앙에서 만들고 관리하는 정책 중에서 선택할 수 있도록 합니다. 또한 사이트 소유자가 콘텐츠에 적용되지 않는 것으로 확인된 정책을 한꺼번에 거부하도록 할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="32a70-p104">Allow site owners to choose from policies that you centrally create and manage. You can also allow site owners to opt out altogether if they decide a policy does not apply to their content.</span></span>
    
- <span data-ttu-id="32a70-115">모든 비즈니스용 OneDrive 사이트와 같은 사이트 모음의 모든 사이트에 단일 필수 정책을 적용하거나, 팀 사이트 서식 파일과 같은 특정 사이트 모음 서식 파일에서 만든 모든 사이트 모음에 정책을 적용합니다.</span><span class="sxs-lookup"><span data-stu-id="32a70-115">Enforce a single mandatory policy on all sites in a site collection, such as all OneDrive for Business sites, or even enforce a policy on all site collections created from a specific site collection template, such as the Team Site template.</span></span>
    
- <span data-ttu-id="32a70-116">사이트 소유자가 다른 작업을 수행하지 않더라도 자동으로 적용되는 기본 규칙을 기본 정책에 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="32a70-116">Provide a default policy with a default rule that will be automatically applied without any action required by site owners.</span></span>
    
- <span data-ttu-id="32a70-117">사이트 소유자가 선택할 수 있는 여러 삭제 규칙이 있는 정책을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="32a70-117">Create a policy that includes several deletion rules that a site owner can choose from.</span></span>
    
<span data-ttu-id="32a70-p105">컨트롤을 만들고 Office 365 보안에서 **보존** 아래에서 찾을 수 있는 문서 삭제 정책 센터를 사용 하 여 문서 삭제 정책 관리 &amp; 준수 센터입니다. 또는 [사이트 모음을](https://go.microsoft.com/fwlink/p/?LinkID=404342) 만들고 **엔터프라이즈** 탭에서 **규정 준수 정책 센터** 를 선택 하 여 수동으로 정책 센터를 만들 수 있습니다. 각 테 넌 트 하나만 문서 삭제 정책 센터 하 고 보안에서 시작 하는 경우 자동으로 만들 수 것 &amp; 준수 센터입니다.</span><span class="sxs-lookup"><span data-stu-id="32a70-p105">You create and manage document deletion policies by using the Document Deletion Policy Center, which you can find under **Retention** in the Office 365 Security &amp; Compliance Center. Alternatively, you can create the policy center manually by [creating the site collection](https://go.microsoft.com/fwlink/p/?LinkID=404342) and choosing **Compliance Policy Center** on the **Enterprise** tab. Each tenant can have only one Document Deletion Policy Center, and it'll be created automatically if you start from the Security &amp; Compliance Center.</span></span> 
  
![문서 삭제 정책 센터의 홈 페이지](media/IP-Document-Deletion-Policy-Center-home-page.png)
  
## <a name="when-to-use-document-deletion-policies"></a><span data-ttu-id="32a70-121">문서 삭제 정책을 사용해야 하는 경우</span><span class="sxs-lookup"><span data-stu-id="32a70-121">When to use document deletion policies</span></span>

<span data-ttu-id="32a70-122">Office 365에서는 문서 삭제 정책 외에 사이트 콘텐츠에 대해 다음과 같은 보존 정책을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="32a70-122">In addition to document deletion policies, Office 365 provides these retention policies for site content:</span></span>
  
- [<span data-ttu-id="32a70-123">레코드 관리</span><span class="sxs-lookup"><span data-stu-id="32a70-123">Records management</span></span>](https://go.microsoft.com/fwlink/p/?LinkID=404250)
    
- [<span data-ttu-id="32a70-124">콘텐츠 형식, 목록 및 라이브러리에 대 한 정보 관리 정책</span><span class="sxs-lookup"><span data-stu-id="32a70-124">Information management policies for content types, lists, and libraries</span></span>](https://go.microsoft.com/fwlink/p/?LinkID=404239)
    
- [<span data-ttu-id="32a70-125">사이트 정책</span><span class="sxs-lookup"><span data-stu-id="32a70-125">Site policies</span></span>](https://go.microsoft.com/fwlink/p/?LinkID=404242)
    
<span data-ttu-id="32a70-p106">각 유형의 정책은 특정 유형의 사이트나 데이터에 가장 적합합니다. 예를 들어 계약서를 위한 재무 사이트나 문서를 위한 기술 자료와 같은 콘텐츠 형식을 사용하는 고도로 구조화된 사이트가 조직에 있을 수 있습니다. 이러한 경우 콘텐츠 형식 정책을 사용할 수 있습니다. 또는 조직이 법률 문서를 보존해야 할 수 있습니다. 이 경우 콘텐츠 형식과 레코드 센터를 사용하여 파일 계획을 구현할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="32a70-p106">Each type of policy works best for a specific type of site or data. For example, your organization may have a highly structured site that uses content types, such as a financial site for contracts or a knowledge base for articles. In this case, you can use content type policies. Or your organization may need to retain legal documents, in which case you might use content types and a Records Center to implement a file plan.</span></span>
  
<span data-ttu-id="32a70-p107">문서 삭제 정책 레코드 관리 또는 정보 관리 정책, 구조화 된 데이터 및 콘텐츠 형식을 사용 하 여 가장 잘 작동 하는 바꾸지 않습니다. 대신, 광범위 하 게 자동으로 삭제 비즈니스 사이트 및 팀 사이트에 대 한 OneDrive와 같은 구조화 되지 않은 데이터를 관리 하는데 필요한 경우 문서 삭제 정책을 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="32a70-p107">Document deletion policies don't replace records management or information management policies, which work best with structured data and content types. Instead, you should use document deletion policies when you need to broadly manage the automatic deletion of unstructured data such as OneDrive for Business sites and team sites.</span></span>
  
![사이트 콘텐츠에 대한 보존 옵션을 보여 주는 다이어그램](media/IP-Retention-policies-for-site-content.png)
  
<span data-ttu-id="32a70-p108">콘텐츠 형식 정책 또는 목록이나 라이브러리에 대한 정보 관리 정책을 이미 사용하는 사이트에 문서 삭제 정책을 적용하는 경우 문서 삭제 정책이 유효한 동안 해당 정책은 무시됩니다. 즉, 사이트에서 구조화된 콘텐츠나 구조화되지 않은 콘텐츠 중 한 가지 용도로만 만들어진 정책을 사용하도록 계획하는 것이 좋습니다. 문서 삭제 정책이 다른 정책을 재정의하는 방식에 대한 자세한 내용은 [Apply or remove a document deletion policy for a site](apply-or-remove-a-document-deletion-policy-for-a-site.md)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="32a70-p108">If you apply a document deletion policy to a site that already uses content type policies or information management policies for a list or library, those policies are ignored while the document deletion policy is in effect. This means you should plan for a site to use only policies meant for structured or unstructured content, not both. For more information on how document deletion policies override other policies, see [Apply or remove a document deletion policy for a site](apply-or-remove-a-document-deletion-policy-for-a-site.md).</span></span>
  
<span data-ttu-id="32a70-136">다른 정책과 달리, 문서 삭제 정책은 목록이 아닌 문서 라이브러리에 대해서만 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="32a70-136">Unlike other policies, document deletion policies work only on document libraries, not lists.</span></span>
  
## <a name="deletion-policies-and-rules"></a><span data-ttu-id="32a70-137">삭제 정책 및 규칙</span><span class="sxs-lookup"><span data-stu-id="32a70-137">Deletion policies and rules</span></span>

<span data-ttu-id="32a70-138">문서 삭제 정책에는 다음을 지정하는 삭제 규칙이 하나 이상 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="32a70-138">A document deletion policy contains one or more delete rules that specify:</span></span>
  
- <span data-ttu-id="32a70-139">삭제할 때까지의 기간</span><span class="sxs-lookup"><span data-stu-id="32a70-139">The time period until deletion.</span></span>
    
- <span data-ttu-id="32a70-140">삭제 날짜를 문서가 만들어진 날부터 계산할지 또는 마지막으로 수정된 날부터 계산할지 여부</span><span class="sxs-lookup"><span data-stu-id="32a70-140">Whether to calculate the deletion date from the when the document was created or last modified.</span></span>
    
- <span data-ttu-id="32a70-141">문서를 영구히 삭제할지 또는 휴지통으로 삭제할지 여부</span><span class="sxs-lookup"><span data-stu-id="32a70-141">Whether to delete the document permanently or to the Recycle Bin.</span></span>
    
<span data-ttu-id="32a70-142">정책에 규칙이 둘 이상 포함되어 있는 경우 사이트 소유자는 콘텐츠에 가장 적합한 규칙을 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="32a70-142">If a policy contains more than one rule, site owners can select the rule that best applies to their content.</span></span>
  
![새 삭제 규칙 페이지](media/IP-New-deletion-rule.png)
  
## <a name="policies-and-assignments"></a><span data-ttu-id="32a70-144">정책 및 할당</span><span class="sxs-lookup"><span data-stu-id="32a70-144">Policies and assignments</span></span>

<span data-ttu-id="32a70-p109">문서 삭제 정책을 만든 후 사이트 모음 서식 파일에 할당할 수 있습니다-예 할당할 수 있습니다는 정책을 OneDrive 비즈니스 서식 파일에 대 한 모든 사용자의 OneDrive 사이트 포함 되도록 합니다. 정책을 사이트 모음 서식 파일에 할당 하는 경우 나중에 해당 서식 파일에서 만든 모든 사이트 모음 외에도 해당 서식 파일에서 이미 만든 모든 사이트 모음에 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="32a70-p109">After you create a document deletion policy, you can assign it to a site collection template — for example, you can assign a policy to the OneDrive for Business template so that it includes every user's OneDrive site. When you assign a policy to a site collection template, this applies to all site collections already created from that template, in addition to any site collections created from that template in the future.</span></span>
  
![OneDrive 옵션을 표시하는 서식 파일 페이지 선택](media/IP-Choose-a-template.png)
  
<span data-ttu-id="32a70-p110">또한 특정 사이트 모음에 정책을 할당하여 해당 사이트 모음 서식 파일에 할당된 정책을 재정의할 수도 있습니다. 예를 들어 팀 사이트 서식 파일에 정책을 할당할 수 있지만 해당 서식 파일에서 만든 특정 사이트 모음에 다른 정책 집합을 적용하여 처음에 할당한 정책을 재정의할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="32a70-p110">You can also assign a policy to a specific site collection— doing so overrides any policies that have been assigned to that site collection template. For example, you may assign policies to the Team Site template, but then override them by applying a different set of policies to a specific site collection created from that template.</span></span>
  
### <a name="one-mandatory-policy-or-several-policies-to-choose-from"></a><span data-ttu-id="32a70-150">선택할 수 있는 한 가지 필수 정책 또는 여러 정책</span><span class="sxs-lookup"><span data-stu-id="32a70-150">One mandatory policy or several policies to choose from</span></span>

<span data-ttu-id="32a70-p111">정책을 할당할 때 필수 정책으로 선택하여 이 정책만 할당할 수 있으며 사이트 모음의 모든 사이트에 적용되도록 할 수 있습니다. 사이트 소유자는 필수 정책을 거부할 수 없습니다. 즉 사이트의 문서는 어떤 경우든 삭제 정책에 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="32a70-p111">When you assign a policy, you can choose to make it mandatory, so that only this policy can be assigned and that it will be applied to all sites in the site collection. Site owners cannot opt out of a mandatory policy, which means documents in the site will be subject to the delete policy no matter what.</span></span>
  
<span data-ttu-id="32a70-p112">단일 정책을 필수로 지정하는 대신, 사이트 모음에 여러 정책을 할당하여 각 사이트 소유자가 해당 사이트에 적용할 정책을 선택하거나 여러 정책을 한꺼번에 거부하도록 할 수도 있습니다. 예를 들어 일반 비즈니스 문서에 대해 하나의 정책을 만들고 다른 보존 일정이 있는 금융 문서에 대해 다른 정책을 만들 수 있습니다. 사이트 소유자가 사이트에 포함된 콘텐츠에 대해 가장 잘 아는 경우가 많으므로 어떤 문서 삭제 정책을 적용하면 좋을지도 가장 잘 알고 있습니다. 각 사이트에는 정책을 하나만 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="32a70-p112">Instead of making a single policy mandatory, you can also assign several policies to a site collection, which allows each site owner to choose which policy to apply to their site, or even to opt out altogether. For example, you can create one policy for general business documents and another policy for financial documents that have a different retention schedule. A site owner often knows best what content their site contains and therefore which document deletion policy to apply. Each site can have only one policy applied to it.</span></span>
  
### <a name="one-rule-or-several-rules-to-choose-from"></a><span data-ttu-id="32a70-157">선택할 수 있는 한 가지 규칙 또는 여러 규칙</span><span class="sxs-lookup"><span data-stu-id="32a70-157">One rule or several rules to choose from</span></span>

<span data-ttu-id="32a70-158">각 정책 많은 규칙 포함 될 수 있습니다를-일반 비즈니스 문서에 대 한 삭제 정책 등 두 규칙을 가질 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="32a70-158">In turn, each policy can contain many rules—for example, a deletion policy for general business documents may have two rules:</span></span>
  
- <span data-ttu-id="32a70-159">법적 의무를 기반으로 보존 하지 않아도 문서 또는 계속 되는 비즈니스 요구 해야하는 만든 날 로부터 1 년 이상 보존할 필요가 없습니다.</span><span class="sxs-lookup"><span data-stu-id="32a70-159">Documents that don't need retention based on legal obligations or ongoing business need should not be retained for more than one year from creation.</span></span>
    
- <span data-ttu-id="32a70-160">1년 이상 지속적으로 업무에 사용해야 하는 문서는 만든 날로부터 3년 이상 보존할 필요가 없습니다.</span><span class="sxs-lookup"><span data-stu-id="32a70-160">Documents necessary for active, ongoing business use that are needed for more than one year, should not be retained for more than three years from creation.</span></span>
    
<span data-ttu-id="32a70-p113">사이트 소유자는 자신의 사이트에는 일반적인 비즈니스를 확인할 수 문서를이 삭제 정책을 선택 하 고 정책에서 적절 한 규칙을 선택 합니다. (하지: 모든 정책)에서 현재 사이트에 적용 되는 정책에서 규칙을 선택할 수 있습니다 및 사이트의 모든 문서 라이브러리에 규칙이 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="32a70-p113">A site owner can determine that their site contains general business documents, select this deletion policy, and then select the appropriate rule from the policy. You can only select a rule from the policy that's currently applied to the site (not from any policy), and the rule applies to all document libraries in the site.</span></span>
  
## <a name="the-relationship-of-site-collections-policies-and-rules"></a><span data-ttu-id="32a70-163">사이트 모음, 정책 및 규칙의 관계</span><span class="sxs-lookup"><span data-stu-id="32a70-163">The relationship of site collections, policies, and rules</span></span>

<span data-ttu-id="32a70-164">기본 관계는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="32a70-164">The basic relationship is this:</span></span>
  
<span data-ttu-id="32a70-p114">사이트 모음 또는 사이트 모음 서식 파일을 계정에 할당 하는 하나 이상의 정책이 하 고 각 이러한 정책을 하나 이상의 규칙을 가질 수 있습니다. 그러나 사이트당를 활성화 하는 정책을 하나만 있을 수 및 언제 든 지 사이트 내에서 라이브러리에 대 한 활성 상태인 삭제 규칙을 하나만 있을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="32a70-p114">A site collection or a site collection template can have one or more policies assigned to it, and each of those policies can have one or more rules. However, there can be only one policy that's active per site, and there can be only one deletion rule that's active at any time for the libraries within the site.</span></span>
  
![정책 간 관계를 보여 주는 다이어그램](media/IP-Two-policies-four-rules.png)
  
## <a name="document-deletion-policies-are-inherited"></a><span data-ttu-id="32a70-168">문서 삭제 정책은 상속됨</span><span class="sxs-lookup"><span data-stu-id="32a70-168">Document deletion policies are inherited</span></span>

<span data-ttu-id="32a70-p115">사용 권한, 탐색 및 기타 여러 사이트 기능처럼 문서 삭제 정책도 상속됩니다. 사이트 소유자는 사이트에 대한 문서 삭제 정책을 선택할 수 있으며 모든 하위 사이트는 상위 사이트에서 정책을 상속합니다. 하위 사이트 소유자는 다른 정책 및 규칙 조합을 선택하여 상속을 끊을 수 있으며 새로운 상속이 다시 끊어질 때까지 모든 하위 사이트에 해당 정책과 규칙이 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="32a70-p115">Like permissions, navigation, and many other site features, document deletion policies are inherited. A site owner can select a document deletion policy for their site, and all subsites inherit the policy from the parent. An owner of a subsite can break inheritance by selecting a different policy and rule combination, and that policy applies to all subsites until inheritance is broken again.</span></span>
  
## <a name="assigning-document-deletion-policies-for-the-first-time"></a><span data-ttu-id="32a70-172">문서 삭제 정책을 처음 할당</span><span class="sxs-lookup"><span data-stu-id="32a70-172">Assigning document deletion policies for the first time</span></span>

<span data-ttu-id="32a70-p116">것 이라는 문서에 대해 지정 된 기간이 삭제 정책 의미 시간 이후에 문서를 만들거나 수정, 정책이 할당 된 이후 시간이 아니라 이해 하는 것이 중요 합니다. 예 2 년 범위가 만들어진 후 문서를 영구적으로 삭제 하는 문서 삭제 정책 만들기 하 고 있는 여러 사이트 모음 4 또는 5 년전 만들어진 사이트 모음 서식 파일에 해당 정책을 할당 수 있습니다. 이 경우에 기존 사이트 모음 삭제 정책에 의해 지정 된 2 년 보다 오래 된 이미 있는 많은 문서를 포함 하는 것은-즉, 많은 양의 콘텐츠를 처음에 대 한 문서 삭제 정책을 할당 한 후 곧 삭제 됩니다 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="32a70-p116">It's important to understand that the time period specified for a document deletion policy means the time since the document was created or modified, not the time since the policy was assigned. For example, you might create a document deletion policy that permanently deletes documents two years after they were created, and then assign that policy to a site collection template from which several site collections were created four or five years ago. In this case, it's likely that the existing site collections contain many documents that are already older than the two years specified by the deletion policy—this means a lot of content will be deleted soon after assigning the document deletion policy for the first time.</span></span>
  
<span data-ttu-id="32a70-p117">정책을 처음 할당할 때는 사이트의 모든 문서가 평가되며 조건을 충족하는 문서는 삭제됩니다. 이러한 방식은 정책이 할당된 이후에 만들어진 새 문서 뿐만 아니라 기존의 모든 문서에 적용됩니다. 또한 해당 기간은 정책이 처음 할당된 이후부터가 아닌 각 문서의 사용 기간에 해당한다는 점에 유의해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="32a70-p117">When you assign the policy for the first time, all documents in the site are evaluated and, if they meet the criteria, they will be deleted. This applies to all existing documents, not just new documents created since the policy was assigned. And remember that the time period is for the age of each document, not the time from when the policy was first assigned.</span></span>
  
<span data-ttu-id="32a70-p118">따라서 처음으로 사이트에 정책을 할당하기 전에 먼저 기존 콘텐츠의 사용 기간과 정책이 기존 콘텐츠에 어떤 영향을 줄 수 있는지 고려해야 합니다. 또한 새 정책을 할당하기 전에 사이트 소유자에게 미리 알려, 가능한 영향을 평가할 시간을 줄 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="32a70-p118">Therefore, before you assign a policy to a site for the first time, you should first consider the age of the existing content and how the policy may impact that existing content. You may also want to communicate the new policy to site owners before assigning it, to give them time to assess the possible impact.</span></span>
  
## <a name="time-lag-for-propagating-policies"></a><span data-ttu-id="32a70-181">정책 전파를 위한 시간 지연</span><span class="sxs-lookup"><span data-stu-id="32a70-181">Time lag for propagating policies</span></span>

<span data-ttu-id="32a70-182">사이트 모음에 정책을 할당한 후에 사이트 소유자는 **사이트 설정** 페이지의 **문서 삭제 정책** 링크를 사용하여 해당 사이트에 대해 사용 가능한 정책을 보고 적용합니다.</span><span class="sxs-lookup"><span data-stu-id="32a70-182">After you assign policies to a site collection, site owners use the **Document Deletion Policies** link on the **Site Settings** page to view and apply policies available for the site.</span></span> 
  
<span data-ttu-id="32a70-p119">**문서 삭제 정책** 링크는 사이트 모음에 정책을 할당 하지 않은 경우에 표시 되지 않습니다. 링크 정책은 사이트에 할당 된 후에 즉시 나타나지 또한- **문서 삭제 정책** 링크를 표시 하는 정책이 할당 되는 경우에서 24 시간까지 걸릴 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="32a70-p119">The **Document Deletion Policies** link won't appear unless policies have been assigned to the site collection. Also, the link doesn't appear immediately after policies have been assigned to the site—it can take up to 24 hours from when the policies are assigned to when the **Document Deletion Policies** link appears.</span></span> 
  
## <a name="permissions"></a><span data-ttu-id="32a70-185">사용 권한</span><span class="sxs-lookup"><span data-stu-id="32a70-185">Permissions</span></span>

<span data-ttu-id="32a70-p120">문서 삭제 정책 센터를 사용하는 규정 준수 팀 구성원은 정책 센터와 정책이 할당될 사이트 모음 둘 다에 대한 권한이 있어야 합니다. 따라서 다음 작업이 권장됩니다.</span><span class="sxs-lookup"><span data-stu-id="32a70-p120">Members of your compliance team who will use the Document Deletion Policy Center need permissions to both the policy center and site collections to which policies will be applied. We recommend that you:</span></span>
  
1. <span data-ttu-id="32a70-p121">문서 삭제 정책 센터의 모든 사용자가 포함 된 보안 그룹 만들기-규정 준수 정책 관리 팀 가능성이 높습니다. 자세한 내용은 [Manage Mail-Enabled 보안 그룹](https://go.microsoft.com/fwlink/p/?LinkID=404345) 을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="32a70-p121">Create a security group that contains all users of the Document Deletion Policy Center—most likely your compliance policy-management team. See [Manage Mail-Enabled Security Groups](https://go.microsoft.com/fwlink/p/?LinkID=404345) for more information.</span></span> 
    
2. <span data-ttu-id="32a70-p122">문서 삭제 정책 센터에서 사이트 모음 소유자 권한을 할당 보안 그룹에 있습니다. 자세한 내용은 [사이트 모음 관리자에 대 한 사용 권한](https://go.microsoft.com/fwlink/p/?LinkID=404346) 을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="32a70-p122">In the Document Deletion Policy Center, assign site collection owner permissions to the security group. See [Permissions for site collection administrators](https://go.microsoft.com/fwlink/p/?LinkID=404346) for more information.</span></span> 
    
3. <span data-ttu-id="32a70-192">문서 삭제 정책을 할당해야 하는 각 사이트 모음에서 보안 그룹에 사이트 모음 소유자 권한을 할당합니다.</span><span class="sxs-lookup"><span data-stu-id="32a70-192">In each site collection to which you need to assign document deletion policies, assign site collection owner permissions to the security group.</span></span>
    
## <a name="how-document-deletion-policies-work-with-hold-policies"></a><span data-ttu-id="32a70-193">문서 삭제 정책이 보류 정책에 작동하는 방식</span><span class="sxs-lookup"><span data-stu-id="32a70-193">How document deletion policies work with hold policies</span></span>

<span data-ttu-id="32a70-194">보류 정책은 모든 콘텐츠가 특정 기간 동안 보존되도록 하지만 문서 삭제 정책은 모든 콘텐츠가 특정 기간 후에 삭제되도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="32a70-194">A hold policy ensures that all content is preserved for a specific period of time, while a document deletion policy ensures that all content is deleted after a specific period of time.</span></span>
  
<span data-ttu-id="32a70-p123">지정된 기간 동안 문서를 보존해야 하는 경우 삭제 정책과 보류 정책을 함께 사용할 수 있습니다. 예를 들어 문서를 수정한 후에 3년 동안 문서를 보존한 다음, 마지막으로 수정하고 3년 후에 해당 문서를 삭제하도록 삭제 정책을 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="32a70-p123">If you need to retain documents for a fixed period of time, you can use a hold policy in conjunction with a deletion policy. For example, you could hold documents for three years after they are modified, and then set up a deletion policy to delete those documents three years after they were last modified.</span></span>
  
<span data-ttu-id="32a70-p124">삭제 정책은 보류 정책을 재정의할 수 없습니다. 사이트가 보류 중이고 문서 삭제 정책에 따라 문서가 삭제되면 문서는 수동으로 삭제한 것처럼 자료 보존 라이브러리에 같은 방식으로 보존됩니다.</span><span class="sxs-lookup"><span data-stu-id="32a70-p124">Note that a deletion policy cannot override a hold. If a site is on hold and a document deletion policy deletes a document, then the document will be preserved in the Preservation Hold library in the same way as if the document had been deleted manually.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="32a70-199">참고 항목</span><span class="sxs-lookup"><span data-stu-id="32a70-199">See also</span></span>

[<span data-ttu-id="32a70-200">사이트에 문서 삭제 정책 적용 또는 제거</span><span class="sxs-lookup"><span data-stu-id="32a70-200">Apply or remove a document deletion policy for a site</span></span>](apply-or-remove-a-document-deletion-policy-for-a-site.md)

[<span data-ttu-id="32a70-201">문서 삭제 정책 만들기</span><span class="sxs-lookup"><span data-stu-id="32a70-201">Create a document deletion policy</span></span>](create-a-document-deletion-policy.md)


