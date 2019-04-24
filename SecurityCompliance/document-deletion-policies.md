---
title: 문서 삭제 정책 개요
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: overview
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- SPO160
ms.assetid: 55e8d858-f278-482b-a198-2e62d6a2e6e5
description: 조직은 규정 준수, 법률 또는 기타 비즈니스 요구 사항으로 인해 일정 기간 동안 문서를 보존 해야 할 수 있습니다. 그러나 조직에서 필요한 것 보다 긴 문서를 보관 하는 경우에는 불필요 한 법적 위험을 생성 합니다. 문서 삭제 정책을 사용 하면 특정 기간이 지난 후에 사이트에서 문서를 삭제 하 여 위험을 줄일 수 있으며, 문서를 만든 후 5 년 동안 사용자의 비즈니스용 OneDrive 사이트에서 문서를 삭제할 수 있습니다.
ms.openlocfilehash: 2a6b1c29986020ebd63f6ddb960f0d28ba348b3e
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32257596"
---
# <a name="overview-of-document-deletion-policies"></a><span data-ttu-id="d9432-105">문서 삭제 정책 개요</span><span class="sxs-lookup"><span data-stu-id="d9432-105">Overview of document deletion policies</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d9432-106">앞으로는 문서 삭제 정책 대신 microsoft 365 준수 센터, microsoft 365 보안 센터 또는 Office 365 보안 &amp; 준수 센터에서 만든 보존 정책을 사용 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="d9432-106">Moving forward, we recommend that you use a retention policy or labels created in the Microsoft 365 compliance center, Microsoft 365 security center, or Office 365 Security &amp; Compliance Center instead of a document deletion policy.</span></span> <span data-ttu-id="d9432-107">문서 삭제 정책은 계속 해 서 보존 정책과 함께 작동 하지만 Office 365의 모든 위치에서 콘텐츠를 보존 하거나 삭제 해야 하는 경우에는 보존 정책을 사용 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="d9432-107">Document deletion policies will continue to work side by side with retention policies, but if you need to retain or delete content anywhere in Office 365, we recommend that you use a retention policy.</span></span> <span data-ttu-id="d9432-108">자세한 내용은 [이러한 기능 대신 보존 정책 사용](retention-policies.md#use-a-retention-policy-instead-of-these-features)을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="d9432-108">For more information, see [Use a retention policy instead of these features](retention-policies.md#use-a-retention-policy-instead-of-these-features).</span></span>
  
<span data-ttu-id="d9432-109">조직은 규정 준수, 법률 또는 기타 비즈니스 요구 사항으로 인해 일정 기간 동안 문서를 보존 해야 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d9432-109">Your organization may be required to retain documents for a period of time because of compliance, legal, or other business requirements.</span></span> <span data-ttu-id="d9432-110">그러나 조직에서 필요한 것 보다 긴 문서를 보관 하는 경우에는 불필요 한 법적 위험을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="d9432-110">However, if your organization keeps documents longer than required, you create unnecessary legal risk.</span></span> <span data-ttu-id="d9432-111">문서 삭제 정책을 사용 하면 특정 기간이 지난 후에 사이트에서 문서를 삭제 하 여 위험을 줄일 수 있으며, 문서를 만든 후 5 년 동안 사용자의 비즈니스용 OneDrive 사이트에서 문서를 삭제할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d9432-111">With a document deletion policy, you can proactively reduce risk by deleting documents in a site after a specific period of time—for example, you can delete documents in users' OneDrive for Business sites five years after the documents were created.</span></span>
  
<span data-ttu-id="d9432-112">문서 삭제 정책은 다음과 같은 강력 하 고 유연성이 뛰어납니다.</span><span class="sxs-lookup"><span data-stu-id="d9432-112">Document deletion policies are powerful yet flexible—for example, you can:</span></span>
  
- <span data-ttu-id="d9432-113">사이트 소유자가 중앙에서 만들고 관리 하는 정책에서 선택할 수 있도록 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="d9432-113">Allow site owners to choose from policies that you centrally create and manage.</span></span> <span data-ttu-id="d9432-114">또한 사이트 소유자가 콘텐츠에 정책이 적용 되지 않는 경우이를 모두 옵트아웃 하도록 허용할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d9432-114">You can also allow site owners to opt out altogether if they decide a policy does not apply to their content.</span></span>
    
- <span data-ttu-id="d9432-115">모든 비즈니스용 OneDrive 사이트와 같은 사이트 모음의 모든 사이트에 단일 필수 정책을 적용 하거나, 팀 사이트 서식 파일과 같은 특정 사이트 모음 서식 파일에서 만든 모든 사이트 모음에 정책을 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="d9432-115">Enforce a single mandatory policy on all sites in a site collection, such as all OneDrive for Business sites, or even enforce a policy on all site collections created from a specific site collection template, such as the Team Site template.</span></span>
    
- <span data-ttu-id="d9432-116">사이트 소유자에 게 필요한 작업 없이 자동으로 적용 되는 기본 규칙을 사용 하 여 기본 정책을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="d9432-116">Provide a default policy with a default rule that will be automatically applied without any action required by site owners.</span></span>
    
- <span data-ttu-id="d9432-117">사이트 소유자가 선택할 수 있는 여러 삭제 규칙을 포함 하는 정책을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d9432-117">Create a policy that includes several deletion rules that a site owner can choose from.</span></span>
    
<span data-ttu-id="d9432-118">문서 삭제 정책 센터를 사용 하 여 문서 삭제 정책을 만들고 관리 합니다.</span><span class="sxs-lookup"><span data-stu-id="d9432-118">You create and manage document deletion policies by using the Document Deletion Policy Center.</span></span> <span data-ttu-id="d9432-119">또는 **엔터프라이즈** 탭에서 [사이트 모음을 만들고](https://go.microsoft.com/fwlink/p/?LinkID=404342) **준수 정책 센터** 를 선택 하 여 수동으로 정책 센터를 만들 수 있습니다. 각 테 넌 트에는 문서 삭제 정책 센터가 하나만 있을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d9432-119">Alternatively, you can create the policy center manually by [creating the site collection](https://go.microsoft.com/fwlink/p/?LinkID=404342) and choosing **Compliance Policy Center** on the **Enterprise** tab. Each tenant can have only one Document Deletion Policy Center.</span></span> 
  
![문서 삭제 정책 센터의 홈 페이지](media/IP-Document-Deletion-Policy-Center-home-page.png)
  
## <a name="when-to-use-document-deletion-policies"></a><span data-ttu-id="d9432-121">문서 삭제 정책을 사용 해야 하는 경우</span><span class="sxs-lookup"><span data-stu-id="d9432-121">When to use document deletion policies</span></span>

<span data-ttu-id="d9432-122">문서 삭제 정책 외에도, Office 365에서는 사이트 콘텐츠에 대 한 다음과 같은 보존 정책을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="d9432-122">In addition to document deletion policies, Office 365 provides these retention policies for site content:</span></span>
  
- [<span data-ttu-id="d9432-123">레코드 관리</span><span class="sxs-lookup"><span data-stu-id="d9432-123">Records management</span></span>](https://go.microsoft.com/fwlink/p/?LinkID=404250)
    
- [<span data-ttu-id="d9432-124">콘텐츠 형식, 목록 및 라이브러리에 대 한 정보 관리 정책</span><span class="sxs-lookup"><span data-stu-id="d9432-124">Information management policies for content types, lists, and libraries</span></span>](https://go.microsoft.com/fwlink/p/?LinkID=404239)
    
- [<span data-ttu-id="d9432-125">사이트 정책</span><span class="sxs-lookup"><span data-stu-id="d9432-125">Site policies</span></span>](https://go.microsoft.com/fwlink/p/?LinkID=404242)
    
<span data-ttu-id="d9432-126">각 정책 유형은 특정 유형의 사이트 또는 데이터에 가장 잘 작동 합니다.</span><span class="sxs-lookup"><span data-stu-id="d9432-126">Each type of policy works best for a specific type of site or data.</span></span> <span data-ttu-id="d9432-127">예를 들어 조직에는 계약에 대 한 금융 사이트 또는 문서 관련 기술 자료와 같은 콘텐츠 형식을 사용 하는 고도로 구조화 된 사이트가 있을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d9432-127">For example, your organization may have a highly structured site that uses content types, such as a financial site for contracts or a knowledge base for articles.</span></span> <span data-ttu-id="d9432-128">이 경우 콘텐츠 형식 정책을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d9432-128">In this case, you can use content type policies.</span></span> <span data-ttu-id="d9432-129">또는 조직에서 법적 문서를 보존 해야 할 수 있으며,이 경우 콘텐츠 형식 및 레코드 센터를 사용 하 여 파일 계획을 구현할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d9432-129">Or your organization may need to retain legal documents, in which case you might use content types and a Records Center to implement a file plan.</span></span>
  
<span data-ttu-id="d9432-130">문서 삭제 정책은 구조화 된 데이터와 콘텐츠 형식에 가장 적합 한 레코드 관리 또는 정보 관리 정책을 대체 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d9432-130">Document deletion policies don't replace records management or information management policies, which work best with structured data and content types.</span></span> <span data-ttu-id="d9432-131">대신, 비즈니스용 OneDrive 사이트 및 팀 사이트와 같은 구조화 되지 않은 데이터의 자동 삭제를 광범위 하 게 관리 해야 하는 경우에는 문서 삭제 정책을 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d9432-131">Instead, you should use document deletion policies when you need to broadly manage the automatic deletion of unstructured data such as OneDrive for Business sites and team sites.</span></span>
  
![사이트 콘텐츠에 대한 보존 옵션을 보여 주는 다이어그램](media/IP-Retention-policies-for-site-content.png)
  
<span data-ttu-id="d9432-133">콘텐츠 형식 정책 또는 목록이나 라이브러리에 대한 정보 관리 정책을 이미 사용하는 사이트에 문서 삭제 정책을 적용하는 경우 문서 삭제 정책이 유효한 동안 해당 정책은 무시됩니다.</span><span class="sxs-lookup"><span data-stu-id="d9432-133">If you apply a document deletion policy to a site that already uses content type policies or information management policies for a list or library, those policies are ignored while the document deletion policy is in effect.</span></span> <span data-ttu-id="d9432-134">즉, 사이트에서 구조화 된 콘텐츠 또는 구조화 되지 않은 콘텐츠에 대 한 정책만 사용 하도록 계획 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d9432-134">This means you should plan for a site to use only policies meant for structured or unstructured content, not both.</span></span> <span data-ttu-id="d9432-135">문서 삭제 정책이 다른 정책을 재정의 하는 방법에 대 한 자세한 내용은 [사이트에 대 한 문서 삭제 정책 적용 또는 제거](apply-or-remove-a-document-deletion-policy-for-a-site.md)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="d9432-135">For more information on how document deletion policies override other policies, see [Apply or remove a document deletion policy for a site](apply-or-remove-a-document-deletion-policy-for-a-site.md).</span></span>
  
<span data-ttu-id="d9432-136">다른 정책과 달리, 문서 삭제 정책은 목록이 아닌 문서 라이브러리에 대해서만 작동 합니다.</span><span class="sxs-lookup"><span data-stu-id="d9432-136">Unlike other policies, document deletion policies work only on document libraries, not lists.</span></span>
  
## <a name="deletion-policies-and-rules"></a><span data-ttu-id="d9432-137">삭제 정책 및 규칙</span><span class="sxs-lookup"><span data-stu-id="d9432-137">Deletion policies and rules</span></span>

<span data-ttu-id="d9432-138">문서 삭제 정책에는 다음을 지정 하는 하나 이상의 삭제 규칙이 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d9432-138">A document deletion policy contains one or more delete rules that specify:</span></span>
  
- <span data-ttu-id="d9432-139">삭제할 시간 간격입니다.</span><span class="sxs-lookup"><span data-stu-id="d9432-139">The time period until deletion.</span></span>
    
- <span data-ttu-id="d9432-140">문서를 만들거나 마지막으로 수정한 시점에서 삭제 날짜를 계산할지 여부</span><span class="sxs-lookup"><span data-stu-id="d9432-140">Whether to calculate the deletion date from the when the document was created or last modified.</span></span>
    
- <span data-ttu-id="d9432-141">문서를 영구적으로 삭제할지 휴지통에 적용할지를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d9432-141">Whether to delete the document permanently or to the Recycle Bin.</span></span>
    
<span data-ttu-id="d9432-142">정책에 규칙이 둘 이상 포함 되어 있는 경우 사이트 소유자는 콘텐츠에 가장 적합 한 규칙을 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d9432-142">If a policy contains more than one rule, site owners can select the rule that best applies to their content.</span></span>
  
![새 삭제 규칙 페이지](media/IP-New-deletion-rule.png)
  
## <a name="policies-and-assignments"></a><span data-ttu-id="d9432-144">정책 및 할당</span><span class="sxs-lookup"><span data-stu-id="d9432-144">Policies and assignments</span></span>

<span data-ttu-id="d9432-145">문서 삭제 정책을 만든 후에는이를 사이트 모음 서식 파일에 할당할 수 있습니다 (예를 들어, 모든 사용자의 onedrive 사이트가 포함 되도록 비즈니스용 onedrive 서식 파일에 정책을 할당할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d9432-145">After you create a document deletion policy, you can assign it to a site collection template — for example, you can assign a policy to the OneDrive for Business template so that it includes every user's OneDrive site.</span></span> <span data-ttu-id="d9432-146">사이트 모음 서식 파일에 정책을 할당 하면 나중에 해당 서식 파일에서 만든 사이트 모음 외에도 해당 서식 파일에서 이미 만든 모든 사이트 모음에 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d9432-146">When you assign a policy to a site collection template, this applies to all site collections already created from that template, in addition to any site collections created from that template in the future.</span></span>
  
![OneDrive 옵션을 표시하는 서식 파일 페이지 선택](media/IP-Choose-a-template.png)
  
<span data-ttu-id="d9432-148">또한 특정 사이트 모음에 정책을 할당할 수 있으며, 이렇게 하면 해당 사이트 모음 서식 파일에 할당 된 모든 정책이 재정의 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d9432-148">You can also assign a policy to a specific site collection— doing so overrides any policies that have been assigned to that site collection template.</span></span> <span data-ttu-id="d9432-149">예를 들어 팀 사이트 서식 파일에 정책을 할당 한 후 해당 서식 파일에서 만든 특정 사이트 모음에 대해 다른 정책 집합을 적용 하 여 다시 정의할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d9432-149">For example, you may assign policies to the Team Site template, but then override them by applying a different set of policies to a specific site collection created from that template.</span></span>
  
### <a name="one-mandatory-policy-or-several-policies-to-choose-from"></a><span data-ttu-id="d9432-150">선택할 수 있는 한 가지 필수 정책 또는 여러 정책</span><span class="sxs-lookup"><span data-stu-id="d9432-150">One mandatory policy or several policies to choose from</span></span>

<span data-ttu-id="d9432-151">정책을 할당할 때는이 정책만 할당할 수 있도록 설정 하 고 사이트 모음의 모든 사이트에 적용 되도록 하도록 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d9432-151">When you assign a policy, you can choose to make it mandatory, so that only this policy can be assigned and that it will be applied to all sites in the site collection.</span></span> <span data-ttu-id="d9432-152">사이트 소유자는 필수 정책을 거부할 수 없으며,이는 사이트의 문서에 관계 없이 삭제 정책이 적용 됨을 의미 합니다.</span><span class="sxs-lookup"><span data-stu-id="d9432-152">Site owners cannot opt out of a mandatory policy, which means documents in the site will be subject to the delete policy no matter what.</span></span>
  
<span data-ttu-id="d9432-153">단일 정책을 필수 항목으로 설정 하는 대신 사이트 모음에 여러 정책을 할당 하 여 각 사이트 소유자가 사이트에 적용할 정책을 선택할 수 있도록 하거나, 전혀 사용 하지 않도록 설정할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d9432-153">Instead of making a single policy mandatory, you can also assign several policies to a site collection, which allows each site owner to choose which policy to apply to their site, or even to opt out altogether.</span></span> <span data-ttu-id="d9432-154">예를 들어 일반 비즈니스 문서에 대 한 하나의 정책 및 다른 보존 일정이 있는 재무 문서에 대 한 다른 정책을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d9432-154">For example, you can create one policy for general business documents and another policy for financial documents that have a different retention schedule.</span></span> <span data-ttu-id="d9432-155">사이트 소유자는 사이트에 포함 된 콘텐츠를 가장 잘 알고 있으며 적용할 문서 삭제 정책을 파악 하기도 합니다.</span><span class="sxs-lookup"><span data-stu-id="d9432-155">A site owner often knows best what content their site contains and therefore which document deletion policy to apply.</span></span> <span data-ttu-id="d9432-156">각 사이트에는 정책을 하나만 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d9432-156">Each site can have only one policy applied to it.</span></span>
  
### <a name="one-rule-or-several-rules-to-choose-from"></a><span data-ttu-id="d9432-157">선택할 수 있는 한 가지 규칙 또는 여러 규칙</span><span class="sxs-lookup"><span data-stu-id="d9432-157">One rule or several rules to choose from</span></span>

<span data-ttu-id="d9432-158">또한 일반적인 비즈니스 문서에 대 한 삭제 정책에는 다음과 같은 두 가지 규칙이 포함 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d9432-158">In turn, each policy can contain many rules—for example, a deletion policy for general business documents may have two rules:</span></span>
  
- <span data-ttu-id="d9432-159">법적 의무 또는 지속적인 비즈니스 필요성에 따라 보존이 필요 하지 않은 문서는 작성에서 1 년 이상 보존 되지 않아야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d9432-159">Documents that don't need retention based on legal obligations or ongoing business need should not be retained for more than one year from creation.</span></span>
    
- <span data-ttu-id="d9432-160">1 년 이상 지속 되는 활성 비즈니스 사용에 필요한 문서는 생성 시 3 년 이상 보존 하지 않아야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d9432-160">Documents necessary for active, ongoing business use that are needed for more than one year, should not be retained for more than three years from creation.</span></span>
    
<span data-ttu-id="d9432-161">사이트 소유자는 사이트에 일반 비즈니스 문서가 포함 되어 있는지 확인 하 고,이 삭제 정책을 선택 하 고, 정책에서 적절 한 규칙을 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d9432-161">A site owner can determine that their site contains general business documents, select this deletion policy, and then select the appropriate rule from the policy.</span></span> <span data-ttu-id="d9432-162">사이트에 현재 적용 된 정책 (정책이 아님)의 규칙만 선택할 수 있으며이 규칙은 사이트의 모든 문서 라이브러리에 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d9432-162">You can only select a rule from the policy that's currently applied to the site (not from any policy), and the rule applies to all document libraries in the site.</span></span>
  
## <a name="the-relationship-of-site-collections-policies-and-rules"></a><span data-ttu-id="d9432-163">사이트 모음, 정책 및 규칙의 관계</span><span class="sxs-lookup"><span data-stu-id="d9432-163">The relationship of site collections, policies, and rules</span></span>

<span data-ttu-id="d9432-164">기본 관계는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="d9432-164">The basic relationship is this:</span></span>
  
<span data-ttu-id="d9432-165">사이트 모음 또는 사이트 모음 서식 파일에는 하나 이상의 정책이 할당 될 수 있으며 각 정책에는 하나 이상의 규칙이 있을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d9432-165">A site collection or a site collection template can have one or more policies assigned to it, and each of those policies can have one or more rules.</span></span> <span data-ttu-id="d9432-166">그러나 사이트 마다 활성화 되는 정책은 하나만 있을 수 있으며, 사이트 내의 라이브러리에 대해 언제 든 지 하나의 삭제 규칙만 활성화할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d9432-166">However, there can be only one policy that's active per site, and there can be only one deletion rule that's active at any time for the libraries within the site.</span></span>
  
![정책 간 관계를 보여 주는 다이어그램](media/IP-Two-policies-four-rules.png)
  
## <a name="document-deletion-policies-are-inherited"></a><span data-ttu-id="d9432-168">문서 삭제 정책이 상속 됨</span><span class="sxs-lookup"><span data-stu-id="d9432-168">Document deletion policies are inherited</span></span>

<span data-ttu-id="d9432-169">사용 권한, 탐색 및 기타 다양 한 사이트 기능과 마찬가지로 문서 삭제 정책이 상속 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d9432-169">Like permissions, navigation, and many other site features, document deletion policies are inherited.</span></span> <span data-ttu-id="d9432-170">사이트 소유자는 자신의 사이트에 대 한 문서 삭제 정책을 선택할 수 있으며, 모든 하위 사이트는 부모에서 정책을 상속 받습니다.</span><span class="sxs-lookup"><span data-stu-id="d9432-170">A site owner can select a document deletion policy for their site, and all subsites inherit the policy from the parent.</span></span> <span data-ttu-id="d9432-171">하위 사이트의 소유자는 다른 정책 및 규칙 조합을 선택 하 여 상속을 중단 하 고, 해당 정책을 모든 하위 사이트에 적용 하 여 상속이 다시 무효화 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d9432-171">An owner of a subsite can break inheritance by selecting a different policy and rule combination, and that policy applies to all subsites until inheritance is broken again.</span></span>
  
## <a name="assigning-document-deletion-policies-for-the-first-time"></a><span data-ttu-id="d9432-172">문서 삭제 정책을 처음 할당</span><span class="sxs-lookup"><span data-stu-id="d9432-172">Assigning document deletion policies for the first time</span></span>

<span data-ttu-id="d9432-173">문서 삭제 정책에 지정 된 기간 이란 정책이 할당 된 이후의 시간이 아니라 문서를 만들거나 수정한 이후의 시간을 의미 한다는 것을 이해 하는 것이 중요 합니다.</span><span class="sxs-lookup"><span data-stu-id="d9432-173">It's important to understand that the time period specified for a document deletion policy means the time since the document was created or modified, not the time since the policy was assigned.</span></span> <span data-ttu-id="d9432-174">예를 들어 문서 삭제 정책을 만든 후 2 년 후에 영구적으로 삭제 하 고, 여러 사이트 모음을 4 ~ 5 년 전에 만든 사이트 모음 서식 파일에 해당 정책을 할당 하는 경우를 예로 들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d9432-174">For example, you might create a document deletion policy that permanently deletes documents two years after they were created, and then assign that policy to a site collection template from which several site collections were created four or five years ago.</span></span> <span data-ttu-id="d9432-175">이 경우 기존 사이트 모음에 삭제 정책으로 지정 된 2 년 보다 오래 된 문서가 많이 포함 되어 있을 수 있으며,이는 첫 번째 항목에 대해 문서 삭제 정책을 할당 한 후에 많은 콘텐츠가 즉시 삭제 됨을 의미 합니다. 표준.</span><span class="sxs-lookup"><span data-stu-id="d9432-175">In this case, it's likely that the existing site collections contain many documents that are already older than the two years specified by the deletion policy—this means a lot of content will be deleted soon after assigning the document deletion policy for the first time.</span></span>
  
<span data-ttu-id="d9432-176">정책을 처음 할당할 때는 사이트의 모든 문서가 평가되며 조건을 충족하는 문서는 삭제됩니다.</span><span class="sxs-lookup"><span data-stu-id="d9432-176">When you assign the policy for the first time, all documents in the site are evaluated and, if they meet the criteria, they will be deleted.</span></span> <span data-ttu-id="d9432-177">이러한 방식은 정책이 할당된 이후에 만들어진 새 문서 뿐만 아니라 기존의 모든 문서에 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="d9432-177">This applies to all existing documents, not just new documents created since the policy was assigned.</span></span> <span data-ttu-id="d9432-178">그리고 해당 기간은 정책이 처음 할당 된 시간을 나타내는 것이 아니라 각 문서의 보존 기간을 염두에 두어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d9432-178">And remember that the time period is for the age of each document, not the time from when the policy was first assigned.</span></span>
  
<span data-ttu-id="d9432-179">따라서 사이트에 정책을 처음으로 할당 하기 전에 먼저 기존 콘텐츠의 보존 기간을 고려 하 고 정책이 기존 콘텐츠에 어떻게 영향을 주는 지를 고려해 야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d9432-179">Therefore, before you assign a policy to a site for the first time, you should first consider the age of the existing content and how the policy may impact that existing content.</span></span> <span data-ttu-id="d9432-180">사이트 소유자에 게 새 정책을 할당 하기 전에이를 전달 하 여 이러한 영향을 평가할 수 있는 시간을 제공할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d9432-180">You may also want to communicate the new policy to site owners before assigning it, to give them time to assess the possible impact.</span></span>
  
## <a name="time-lag-for-propagating-policies"></a><span data-ttu-id="d9432-181">정책 전파 시간 지연</span><span class="sxs-lookup"><span data-stu-id="d9432-181">Time lag for propagating policies</span></span>

<span data-ttu-id="d9432-182">사이트 모음에 정책을 할당 하면 사이트 소유자가 사이트 **설정** 페이지의 **문서 삭제 정책** 링크를 사용 하 여 사이트에 대해 사용 가능한 정책을 보고 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="d9432-182">After you assign policies to a site collection, site owners use the **Document Deletion Policies** link on the **Site Settings** page to view and apply policies available for the site.</span></span> 
  
<span data-ttu-id="d9432-183">사이트 모음에 정책이 할당 되지 않은 경우 **문서 삭제 정책** 링크가 표시 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d9432-183">The **Document Deletion Policies** link won't appear unless policies have been assigned to the site collection.</span></span> <span data-ttu-id="d9432-184">또한 사이트에 정책이 할당 된 직후에 링크가 표시 되지 않으며, **문서 삭제 정책** 링크가 나타나면 정책이 할당 될 때까지 최대 24 시간이 걸릴 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d9432-184">Also, the link doesn't appear immediately after policies have been assigned to the site—it can take up to 24 hours from when the policies are assigned to when the **Document Deletion Policies** link appears.</span></span> 
  
## <a name="permissions"></a><span data-ttu-id="d9432-185">사용 권한</span><span class="sxs-lookup"><span data-stu-id="d9432-185">Permissions</span></span>

<span data-ttu-id="d9432-186">문서 삭제 정책 센터를 사용할 규정 준수 팀의 구성원은 정책이 적용 될 정책 센터 및 사이트 모음에 대 한 사용 권한이 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="d9432-186">Members of your compliance team who will use the Document Deletion Policy Center need permissions to both the policy center and site collections to which policies will be applied.</span></span> <span data-ttu-id="d9432-187">따라서 다음 작업이 권장됩니다.</span><span class="sxs-lookup"><span data-stu-id="d9432-187">We recommend that you:</span></span>
  
1. <span data-ttu-id="d9432-188">문서 삭제 정책 센터의 모든 사용자를 포함 하는 보안 그룹 (준수 정책 관리 팀)을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d9432-188">Create a security group that contains all users of the Document Deletion Policy Center—most likely your compliance policy-management team.</span></span> <span data-ttu-id="d9432-189">자세한 내용은 [메일 사용이 가능한 보안 그룹 관리](https://go.microsoft.com/fwlink/p/?LinkID=404345) 를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="d9432-189">See [Manage Mail-Enabled Security Groups](https://go.microsoft.com/fwlink/p/?LinkID=404345) for more information.</span></span> 
    
2. <span data-ttu-id="d9432-190">문서 삭제 정책 센터에서 보안 그룹에 사이트 모음 소유자 권한을 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="d9432-190">In the Document Deletion Policy Center, assign site collection owner permissions to the security group.</span></span> <span data-ttu-id="d9432-191">자세한 내용은 [사이트 모음 관리자의 사용 권한을](https://go.microsoft.com/fwlink/p/?LinkID=404346) 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="d9432-191">See [Permissions for site collection administrators](https://go.microsoft.com/fwlink/p/?LinkID=404346) for more information.</span></span> 
    
3. <span data-ttu-id="d9432-192">문서 삭제 정책을 할당 해야 하는 각 사이트 모음에서 보안 그룹에 사이트 모음 소유자 권한을 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="d9432-192">In each site collection to which you need to assign document deletion policies, assign site collection owner permissions to the security group.</span></span>
    
## <a name="how-document-deletion-policies-work-with-hold-policies"></a><span data-ttu-id="d9432-193">문서 삭제 정책이 보류 정책에 작동 하는 방식</span><span class="sxs-lookup"><span data-stu-id="d9432-193">How document deletion policies work with hold policies</span></span>

<span data-ttu-id="d9432-194">보류 정책은 모든 콘텐츠가 특정 기간 동안 보존 되도록 하며 문서 삭제 정책은 모든 콘텐츠가 특정 기간 후에 삭제 되도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="d9432-194">A hold policy ensures that all content is preserved for a specific period of time, while a document deletion policy ensures that all content is deleted after a specific period of time.</span></span>
  
<span data-ttu-id="d9432-195">고정 된 기간 동안 문서를 보존 해야 하는 경우에는 보류 정책을 삭제 정책과 함께 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d9432-195">If you need to retain documents for a fixed period of time, you can use a hold policy in conjunction with a deletion policy.</span></span> <span data-ttu-id="d9432-196">예를 들어 문서가 수정 된 후 3 년 동안 문서를 보관 한 다음 삭제 정책을 설정 하 여 해당 문서를 마지막으로 수정한 후 3 년 후에 삭제할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d9432-196">For example, you could hold documents for three years after they are modified, and then set up a deletion policy to delete those documents three years after they were last modified.</span></span>
  
<span data-ttu-id="d9432-197">삭제 정책은 보류를 재정의할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="d9432-197">Note that a deletion policy cannot override a hold.</span></span> <span data-ttu-id="d9432-198">사이트가 보류 중이 고 문서 삭제 정책이 문서를 삭제 하는 경우 문서를 수동으로 삭제 한 것과 동일한 방식으로 문서가 보존 보류 라이브러리에 보존 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d9432-198">If a site is on hold and a document deletion policy deletes a document, then the document will be preserved in the Preservation Hold library in the same way as if the document had been deleted manually.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="d9432-199">참고 항목</span><span class="sxs-lookup"><span data-stu-id="d9432-199">See also</span></span>

[<span data-ttu-id="d9432-200">사이트에 문서 삭제 정책 적용 또는 제거</span><span class="sxs-lookup"><span data-stu-id="d9432-200">Apply or remove a document deletion policy for a site</span></span>](apply-or-remove-a-document-deletion-policy-for-a-site.md)

[<span data-ttu-id="d9432-201">문서 삭제 정책 만들기</span><span class="sxs-lookup"><span data-stu-id="d9432-201">Create a document deletion policy</span></span>](create-a-document-deletion-policy.md)


