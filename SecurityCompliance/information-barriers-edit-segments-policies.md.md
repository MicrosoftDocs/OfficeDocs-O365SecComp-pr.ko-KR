---
title: 정보 장벽 정책 편집 또는 제거
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 06/24/2019
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.collection:
- M365-security-compliance
localization_priority: None
description: 정보 장벽에 대 한 정책을 편집 하거나 제거 하는 방법을 알아봅니다.
ms.openlocfilehash: e6bed4df2329d426f86bd4cde07bdc7d1a2792cd
ms.sourcegitcommit: 7c48ce016fa9f45a3813467f7c5a2fd72f9b8f49
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/25/2019
ms.locfileid: "35215651"
---
# <a name="edit-or-remove-information-barrier-policies-preview"></a><span data-ttu-id="8bdd5-103">정보 장벽 정책 편집 또는 제거 (미리 보기)</span><span class="sxs-lookup"><span data-stu-id="8bdd5-103">Edit or remove information barrier policies (Preview)</span></span>

## <a name="overview"></a><span data-ttu-id="8bdd5-104">개요</span><span class="sxs-lookup"><span data-stu-id="8bdd5-104">Overview</span></span>

<span data-ttu-id="8bdd5-105">[정보 장벽 정책을 정의한](information-barriers-policies.md)후에는 [문제 해결](information-barriers-troubleshooting.md) 또는 일반 유지 관리의 일환으로 이러한 정책 또는 사용자 세그먼트를 변경 해야 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8bdd5-105">After you have [defined information barrier policies](information-barriers-policies.md), you might need to make changes to those policies or to your user segments, as part of [troubleshooting](information-barriers-troubleshooting.md) or as regular maintenance.</span></span> <span data-ttu-id="8bdd5-106">이 문서를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="8bdd5-106">Use this article as a guide.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8bdd5-107">이 문서에서 설명 하는 작업을 수행 하려면 다음 중 하 나와 같은 적절 한 역할을 할당 받아야 합니다.</span><span class="sxs-lookup"><span data-stu-id="8bdd5-107">To perform the tasks described in this article, you must be assigned an appropriate role, such as one of the following:</span></span><br/><span data-ttu-id="8bdd5-108">-Microsoft 365 Enterprise 전역 관리자</span><span class="sxs-lookup"><span data-stu-id="8bdd5-108">- Microsoft 365 Enterprise Global Administrator</span></span><br/><span data-ttu-id="8bdd5-109">-Office 365 전역 관리자</span><span class="sxs-lookup"><span data-stu-id="8bdd5-109">- Office 365 Global Administrator</span></span><br/><span data-ttu-id="8bdd5-110">-준수 관리자</span><span class="sxs-lookup"><span data-stu-id="8bdd5-110">- Compliance Administrator</span></span><br/><span data-ttu-id="8bdd5-111">-IB 준수 관리 (새 역할입니다.)</span><span class="sxs-lookup"><span data-stu-id="8bdd5-111">- IB Compliance Management (this is a new role!)</span></span><p><span data-ttu-id="8bdd5-112">정보 장벽에 대 한 필수 구성 요소에 대 한 자세한 내용은 [필수 구성 요소 (정보 장벽 정책)](information-barriers-policies.md#prerequisites)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="8bdd5-112">To learn more about prerequisites for information barriers, see [Prerequisites (for information barrier policies)](information-barriers-policies.md#prerequisites).</span></span><p><span data-ttu-id="8bdd5-113">[Office 365 Security & 준수 센터 PowerShell에 연결](https://docs.microsoft.com/powershell/exchange/office-365-scc/connect-to-scc-powershell/connect-to-scc-powershell?view=exchange-ps)되어 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="8bdd5-113">Make sure to [connect to Office 365 Security & Compliance Center PowerShell](https://docs.microsoft.com/powershell/exchange/office-365-scc/connect-to-scc-powershell/connect-to-scc-powershell?view=exchange-ps).</span></span>

## <a name="edit-user-account-attributes"></a><span data-ttu-id="8bdd5-114">사용자 계정 특성 편집</span><span class="sxs-lookup"><span data-stu-id="8bdd5-114">Edit user account attributes</span></span>

<span data-ttu-id="8bdd5-115">다음 절차에 사용 하 여 사용자 조각화에 사용 되는 특성을 편집 합니다.</span><span class="sxs-lookup"><span data-stu-id="8bdd5-115">Use this procedure to edit attributes that are used for segmenting users.</span></span> 

<span data-ttu-id="8bdd5-116">예를 들어 부서 특성을 사용 하는 경우 현재 하나 이상의 사용자 계정에 부서에 대해 나열 된 값이 없는 경우 부서 정보를 포함 하도록 해당 사용자 계정을 편집 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="8bdd5-116">For example, if you are using a Department attribute, and one or more user accounts do not currently have any values listed for Department, you must edit those user accounts to include Department information.</span></span> 

<span data-ttu-id="8bdd5-117">사용자 계정 특성은 정보 장벽 정책을 할당할 수 있도록 세그먼트를 정의 하는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8bdd5-117">User account attributes are used for defining segments so that information barrier policies can be assigned.</span></span>

1. <span data-ttu-id="8bdd5-118">특성 값 및 할당 된 세그먼트와 같은 특정 사용자 계정에 대 한 세부 정보를 보려면 **InformationBarrierRecipientStatus** Cmdlet을 Identity 매개 변수와 함께 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="8bdd5-118">To view details for a specific user account, such as attribute values and assigned segment(s), use the **Get-InformationBarrierRecipientStatus** cmdlet with Identity parameters.</span></span> 

   <span data-ttu-id="8bdd5-119">구문과`Get-InformationBarrierRecipientStatus -Identity <value> -Identity2 <value>`</span><span class="sxs-lookup"><span data-stu-id="8bdd5-119">Syntax: `Get-InformationBarrierRecipientStatus -Identity <value> -Identity2 <value>`</span></span> 
    
   <span data-ttu-id="8bdd5-120">이름, 별칭, 고유 이름, 정식 도메인 이름, 전자 메일 주소 또는 GUID와 같은 각 사용자를 고유 하 게 식별 하는 모든 값을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8bdd5-120">You can use any value that uniquely identifies each user, such as name, alias, distinguished name, canonical domain name, email address, or GUID.</span></span> 
    
   <span data-ttu-id="8bdd5-121">예제: `Get-InformationBarrierRecipientStatus -Identity meganb -Identity2 alexw`</span><span class="sxs-lookup"><span data-stu-id="8bdd5-121">Example: `Get-InformationBarrierRecipientStatus -Identity meganb -Identity2 alexw`</span></span> 
    
   <span data-ttu-id="8bdd5-122">이 예에서는 Office 365의 두 사용자 계정 ( *Megan*용 *meganb* 및 *Alex*용 *alexw* )을 참조 합니다.</span><span class="sxs-lookup"><span data-stu-id="8bdd5-122">In this example, we refer to two user accounts in Office 365: *meganb* for *Megan*, and *alexw* for *Alex*.</span></span> 
    
   <span data-ttu-id="8bdd5-123">(단일 사용자에 대해이 cmdlet을 사용할 수도 있습니다. `Get-InformationBarrierRecipientStatus -Identity <value>`)</span><span class="sxs-lookup"><span data-stu-id="8bdd5-123">(You can also use this cmdlet for a single user: `Get-InformationBarrierRecipientStatus -Identity <value>`)</span></span> 
    
2. <span data-ttu-id="8bdd5-124">사용자 계정 프로필에 대해 편집 하려는 특성을 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8bdd5-124">Determine which attribute you want to edit for your user account profile(s).</span></span> <span data-ttu-id="8bdd5-125">자세한 [내용은 정보 장벽 정책 (미리 보기)에 대 한 특성](information-barriers-attributes.md) 을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="8bdd5-125">Refer to [Attributes for information barrier policies (Preview)](information-barriers-attributes.md) for more details.</span></span> 

3. <span data-ttu-id="8bdd5-126">이전 단계에서 선택한 특성에 대 한 값을 포함 하도록 하나 이상의 사용자 계정을 편집 합니다.</span><span class="sxs-lookup"><span data-stu-id="8bdd5-126">Edit one or more user accounts to include values for the attribute you selected in the previous step.</span></span> <span data-ttu-id="8bdd5-127">이렇게 하려면 다음 절차 중 하나를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="8bdd5-127">To do this, use one of the following procedures:</span></span>

    - <span data-ttu-id="8bdd5-128">단일 계정을 편집 하려면 [Azure Active Directory를 사용 하 여 사용자 프로필 정보 추가 또는 업데이트](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-users-profile-azure-portal)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="8bdd5-128">To edit a single account, see [Add or update a user's profile information using Azure Active Directory](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-users-profile-azure-portal).</span></span>

    - <span data-ttu-id="8bdd5-129">여러 계정을 편집 하거나 PowerShell을 사용 하 여 단일 계정을 편집 하려면 [Office 365 PowerShell을 사용 하 여 사용자 계정 속성 구성을](https://docs.microsoft.com/office365/enterprise/powershell/configure-user-account-properties-with-office-365-powershell)참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="8bdd5-129">To edit multiple accounts (or use PowerShell to edit a single account), see [Configure user account properties with Office 365 PowerShell](https://docs.microsoft.com/office365/enterprise/powershell/configure-user-account-properties-with-office-365-powershell).</span></span>

## <a name="edit-a-segment"></a><span data-ttu-id="8bdd5-130">세그먼트 편집</span><span class="sxs-lookup"><span data-stu-id="8bdd5-130">Edit a segment</span></span>

<span data-ttu-id="8bdd5-131">이 절차를 사용 하 여 사용자 세그먼트의 정의를 편집 합니다.</span><span class="sxs-lookup"><span data-stu-id="8bdd5-131">Use this procedure edit the definition of a user segment.</span></span> <span data-ttu-id="8bdd5-132">예를 들어 세그먼트 이름을 변경 하거나 세그먼트에 포함 된 사용자를 확인 하는 데 사용 되는 필터를 변경할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8bdd5-132">For example, you might change the name of a segment, or the filter that is used to determine who's included in the segment.</span></span>

1. <span data-ttu-id="8bdd5-133">모든 기존 세그먼트를 보려면 **OrganizationSegment** cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="8bdd5-133">To view all existing segments, use the **Get-OrganizationSegment** cmdlet.</span></span>
    
    <span data-ttu-id="8bdd5-134">구문과`Get-OrganizationSegment`</span><span class="sxs-lookup"><span data-stu-id="8bdd5-134">Syntax: `Get-OrganizationSegment`</span></span>

    <span data-ttu-id="8bdd5-135">세그먼트 유형, UserGroupFilter 값, 해당 개체를 만들거나 마지막으로 수정한 사람, GUID 등의 각 세그먼트와 세부 정보에 대 한 목록이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8bdd5-135">You will see a list of segments and details for each, such as segment type, its UserGroupFilter value, who created or last modified it, GUID, and so on.</span></span>

    > [!TIP]
    > <span data-ttu-id="8bdd5-136">나중에 참조 하기 위해 세그먼트 목록을 인쇄 하거나 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="8bdd5-136">Print or save your list of segments for reference later.</span></span> <span data-ttu-id="8bdd5-137">예를 들어 세그먼트를 편집 하려면 해당 이름을 확인 하거나 값을 식별 해야 합니다 (이는 Identity 매개 변수와 함께 사용 됨).</span><span class="sxs-lookup"><span data-stu-id="8bdd5-137">For example, if you want to edit a segment, you will need to know its name or identify value (this is used with the Identity parameter).</span></span>

2. <span data-ttu-id="8bdd5-138">세그먼트를 편집 하려면 **Identity** 매개 변수와 관련 세부 정보와 함께 **OrganizationSegment** cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="8bdd5-138">To edit a segment, use the **Set-OrganizationSegment** cmdlet with the **Identity** parameter and relevant details.</span></span> 

    <span data-ttu-id="8bdd5-139">구문과`Set-OrganizationSegment -Identity GUID -UserGroupFilter "attribute -eq 'attributevalue'"`</span><span class="sxs-lookup"><span data-stu-id="8bdd5-139">Syntax: `Set-OrganizationSegment -Identity GUID -UserGroupFilter "attribute -eq 'attributevalue'"`</span></span>

    <span data-ttu-id="8bdd5-140">예제: `Set-OrganizationSegment -Identity c96e0837-c232-4a8a-841e-ef45787d8fcd -UserGroupFilter "Department -eq 'HRDept'"`</span><span class="sxs-lookup"><span data-stu-id="8bdd5-140">Example: `Set-OrganizationSegment -Identity c96e0837-c232-4a8a-841e-ef45787d8fcd -UserGroupFilter "Department -eq 'HRDept'"`</span></span>

    <span data-ttu-id="8bdd5-141">이 예에서는 GUID가 *c96e0837-c232-4a8a-841e-ef45787d8fcd*인 세그먼트에 대해 부서 이름을 "hrdept"로 업데이트 했습니다.</span><span class="sxs-lookup"><span data-stu-id="8bdd5-141">In this example, for the segment that has the GUID *c96e0837-c232-4a8a-841e-ef45787d8fcd*, we updated the department name to "HRDept".</span></span>

<span data-ttu-id="8bdd5-142">조직의 세그먼트 편집을 마친 후에는 정보 장벽 정책을 [정의](information-barriers-policies.md#part-2-define-information-barrier-policies) 하거나 [편집할](#edit-a-policy) 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8bdd5-142">When you have finished editing segments for your organization, you can either [define](information-barriers-policies.md#part-2-define-information-barrier-policies) or [edit](#edit-a-policy) information barrier policies.</span></span>

## <a name="edit-a-policy"></a><span data-ttu-id="8bdd5-143">정책 편집</span><span class="sxs-lookup"><span data-stu-id="8bdd5-143">Edit a policy</span></span>

1. <span data-ttu-id="8bdd5-144">현재 정보 장벽 정책 목록을 보려면 **InformationBarrierPolicy** cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="8bdd5-144">To view a list of current information barrier policies, use the **Get-InformationBarrierPolicy** cmdlet.</span></span>

    <span data-ttu-id="8bdd5-145">구문과`Get-InformationBarrierPolicy`</span><span class="sxs-lookup"><span data-stu-id="8bdd5-145">Syntax: `Get-InformationBarrierPolicy`</span></span>

    <span data-ttu-id="8bdd5-146">결과 목록에서 변경 하려는 정책을 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="8bdd5-146">In the list of results, identify the policy that you want to change.</span></span> <span data-ttu-id="8bdd5-147">정책의 GUID 및 이름을 적어둡니다.</span><span class="sxs-lookup"><span data-stu-id="8bdd5-147">Note the policy's GUID and name.</span></span>

2. <span data-ttu-id="8bdd5-148">**InformationBarrierPolicy** Cmdlet에서 **Identity** 매개 변수를 사용 하 여 변경할 내용을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8bdd5-148">Use the **Set-InformationBarrierPolicy** cmdlet with an **Identity** parameter, and specify the changes you want to make.</span></span>

    <span data-ttu-id="8bdd5-149">예: *연구* 세그먼트가 *영업* 및 *마케팅* 세그먼트와 통신 하지 못하도록 차단 하도록 정책이 정의 되어 있다고 가정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8bdd5-149">Example: Suppose a policy was defined to block the *Research* segment from communicating with the *Sales* and *Marketing* segments.</span></span> <span data-ttu-id="8bdd5-150">이 cmdlet을 사용 하 여 정책이 정의 되었습니다.`New-InformationBarrierPolicy -Name "Research-SalesMarketing" -AssignedSegment "Research" -SegmentsBlocked "Sales","Marketing"`</span><span class="sxs-lookup"><span data-stu-id="8bdd5-150">The policy was defined by using this cmdlet: `New-InformationBarrierPolicy -Name "Research-SalesMarketing" -AssignedSegment "Research" -SegmentsBlocked "Sales","Marketing"`</span></span>
    
    <span data-ttu-id="8bdd5-151">*리서치* 세그먼트의 사람들이 *HR* 세그먼트의 사용자와만 통신할 수 있도록이를 변경 하려는 경우를 가정해 보겠습니다.</span><span class="sxs-lookup"><span data-stu-id="8bdd5-151">Suppose we want to change it so that people in the *Research* segment can only communicate with people in the *HR* segment.</span></span> <span data-ttu-id="8bdd5-152">이 변경 작업을 수행 하려면 다음 cmdlet을 사용 합니다.`Set-InformationBarrierPolicy -Identity 43c37853-ea10-4b90-a23d-ab8c93772471 -SegmentsAllowed "HR"`</span><span class="sxs-lookup"><span data-stu-id="8bdd5-152">To make this change, we use this cmdlet: `Set-InformationBarrierPolicy -Identity 43c37853-ea10-4b90-a23d-ab8c93772471 -SegmentsAllowed "HR"`</span></span>

    <span data-ttu-id="8bdd5-153">이 예에서는 "SegmentsBlocked"를 "SegmentsAllowed"로 변경 하 고 *HR* 세그먼트를 지정 했습니다.</span><span class="sxs-lookup"><span data-stu-id="8bdd5-153">In this example, we changed "SegmentsBlocked" to "SegmentsAllowed" and specified the *HR* segment.</span></span>

3. <span data-ttu-id="8bdd5-154">정책 편집을 마친 후에는 변경 내용을 적용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="8bdd5-154">When you are finished editing a policy, make sure to apply your changes.</span></span> <span data-ttu-id="8bdd5-155">( [정보 장벽 정책 적용](information-barriers-policies.md#part-3-apply-information-barrier-policies)참조)</span><span class="sxs-lookup"><span data-stu-id="8bdd5-155">(See [Apply information barrier policies](information-barriers-policies.md#part-3-apply-information-barrier-policies).)</span></span>

## <a name="set-a-policy-to-inactive-status"></a><span data-ttu-id="8bdd5-156">정책을 비활성 상태로 설정</span><span class="sxs-lookup"><span data-stu-id="8bdd5-156">Set a policy to inactive status</span></span>

1. <span data-ttu-id="8bdd5-157">현재 정보 장벽 정책 목록을 보려면 **InformationBarrierPolicy** cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="8bdd5-157">To view a list of current information barrier policies, use the **Get-InformationBarrierPolicy** cmdlet.</span></span>

    <span data-ttu-id="8bdd5-158">구문과`Get-InformationBarrierPolicy`</span><span class="sxs-lookup"><span data-stu-id="8bdd5-158">Syntax: `Get-InformationBarrierPolicy`</span></span>

    <span data-ttu-id="8bdd5-159">결과 목록에서 변경 하거나 제거할 정책을 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="8bdd5-159">In the list of results, identify the policy that you want to change (or remove).</span></span> <span data-ttu-id="8bdd5-160">정책의 GUID 및 이름을 적어둡니다.</span><span class="sxs-lookup"><span data-stu-id="8bdd5-160">Note the policy's GUID and name.</span></span>

2. <span data-ttu-id="8bdd5-161">정책의 상태를 비활성으로 설정 하려면 Identity 매개 변수와 함께 **InformationBarrierPolicy** cmdlet을 사용 하 고 State 매개 변수는 비활성으로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8bdd5-161">To set the policy's status to inactive, use the **Set-InformationBarrierPolicy** cmdlet with an Identity parameter and the State parameter set to Inactive.</span></span>

    <span data-ttu-id="8bdd5-162">구문과`Set-InformationBarrierPolicy -Identity GUID -State Inactive`</span><span class="sxs-lookup"><span data-stu-id="8bdd5-162">Syntax: `Set-InformationBarrierPolicy -Identity GUID -State Inactive`</span></span>

    `Set-InformationBarrierPolicy -Identity 43c37853-ea10-4b90-a23d-ab8c9377247 -State Inactive`

    <span data-ttu-id="8bdd5-163">이 예에서는 GUID *43c37853-ea10-4b90-a23d-ab8c9377247을 사용* 하는 정보 장벽 정책을 비활성 상태로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8bdd5-163">In this example, we set an information barrier policy that has GUID *43c37853-ea10-4b90-a23d-ab8c9377247* to an inactive status.</span></span>

3. <span data-ttu-id="8bdd5-164">변경 내용을 적용 하려면 **InformationBarrierPoliciesApplication** cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="8bdd5-164">To apply your changes, use the **Start-InformationBarrierPoliciesApplication** cmdlet.</span></span>

    <span data-ttu-id="8bdd5-165">구문과`Start-InformationBarrierPoliciesApplication`</span><span class="sxs-lookup"><span data-stu-id="8bdd5-165">Syntax: `Start-InformationBarrierPoliciesApplication`</span></span>

    <span data-ttu-id="8bdd5-166">사용자가 조직에 대해 변경 내용을 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="8bdd5-166">Changes are applied, user by user, for your organization.</span></span> <span data-ttu-id="8bdd5-167">대규모 조직에서는이 프로세스를 완료 하는 데 24 시간 이상 소요 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8bdd5-167">If your organization is large, it can take 24 hours (or more) for this process to complete.</span></span> <span data-ttu-id="8bdd5-168">일반적으로 5000 사용자 계정을 처리 하는 데 한 시간 정도 소요 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8bdd5-168">(As a general guideline, it takes about an hour to process 5,000 user accounts.)</span></span>

<span data-ttu-id="8bdd5-169">이때 하나 이상의 정보 장벽 정책이 비활성 상태로 설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8bdd5-169">At this point, one or more information barrier policies are set to inactive status.</span></span> <span data-ttu-id="8bdd5-170">여기서는 다음 작업을 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8bdd5-170">From here, you can do any of the following:</span></span>
- <span data-ttu-id="8bdd5-171">그대로 유지 (비활성 상태로 설정 된 정책이 사용자에 게 영향을 주지 않음)</span><span class="sxs-lookup"><span data-stu-id="8bdd5-171">Keep it as is (a policy set to inactive status has no effect on users)</span></span>
- [<span data-ttu-id="8bdd5-172">정책 편집</span><span class="sxs-lookup"><span data-stu-id="8bdd5-172">Edit a policy</span></span>](#edit-a-policy) 
- [<span data-ttu-id="8bdd5-173">정책 제거</span><span class="sxs-lookup"><span data-stu-id="8bdd5-173">Remove a policy</span></span>](#remove-a-policy)

## <a name="remove-a-policy"></a><span data-ttu-id="8bdd5-174">정책 제거</span><span class="sxs-lookup"><span data-stu-id="8bdd5-174">Remove a policy</span></span>

1. <span data-ttu-id="8bdd5-175">현재 정보 장벽 정책 목록을 보려면 **InformationBarrierPolicy** cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="8bdd5-175">To view a list of current information barrier policies, use the **Get-InformationBarrierPolicy** cmdlet.</span></span>

    <span data-ttu-id="8bdd5-176">구문과`Get-InformationBarrierPolicy`</span><span class="sxs-lookup"><span data-stu-id="8bdd5-176">Syntax: `Get-InformationBarrierPolicy`</span></span>

    <span data-ttu-id="8bdd5-177">결과 목록에서 제거할 정책을 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="8bdd5-177">In the list of results, identify the policy that you want to remove.</span></span> <span data-ttu-id="8bdd5-178">정책의 GUID 및 이름을 적어둡니다.</span><span class="sxs-lookup"><span data-stu-id="8bdd5-178">Note the policy's GUID and name.</span></span> <span data-ttu-id="8bdd5-179">정책이 비활성 상태로 설정 되어 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="8bdd5-179">Make sure the policy is set to inactive status.</span></span>

2. <span data-ttu-id="8bdd5-180">**InformationBarrierPolicy** Cmdlet을 Identity 매개 변수와 함께 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="8bdd5-180">Use the **Remove-InformationBarrierPolicy** cmdlet with an Identity parameter.</span></span>

    <span data-ttu-id="8bdd5-181">구문과`Remove-InformationBarrierPolicy -Identity GUID`</span><span class="sxs-lookup"><span data-stu-id="8bdd5-181">Syntax: `Remove-InformationBarrierPolicy -Identity GUID`</span></span>

    <span data-ttu-id="8bdd5-182">예: GUID *43c37853-ea10-4b90-a23d-ab8c93772471*가 있는 정책을 제거 하려고 한다고 가정 합시다.</span><span class="sxs-lookup"><span data-stu-id="8bdd5-182">Example: Suppose we want to remove a policy that has GUID *43c37853-ea10-4b90-a23d-ab8c93772471*.</span></span> <span data-ttu-id="8bdd5-183">이렇게 하려면 다음과 같은 cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="8bdd5-183">To do this, we use this cmdlet:</span></span>
    
    `Remove-InformationBarrierPolicy -Identity 43c37853-ea10-4b90-a23d-ab8c93772471`

    <span data-ttu-id="8bdd5-184">메시지가 표시 되 면 변경 내용을 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="8bdd5-184">When prompted, confirm the change.</span></span>

3. <span data-ttu-id="8bdd5-185">제거할 각 정책에 대해 1-2 단계를 반복 합니다.</span><span class="sxs-lookup"><span data-stu-id="8bdd5-185">Repeat steps 1-2 for each policy you want to remove.</span></span>

4. <span data-ttu-id="8bdd5-186">정책을 제거한 후에는 변경 내용을 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="8bdd5-186">When you are finished removing policies, apply your changes.</span></span> <span data-ttu-id="8bdd5-187">이 작업을 수행 하려면 **InformationBarrierPoliciesApplication** cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="8bdd5-187">To do this, use the **Start-InformationBarrierPoliciesApplication** cmdlet.</span></span>

    <span data-ttu-id="8bdd5-188">구문과`Start-InformationBarrierPoliciesApplication`</span><span class="sxs-lookup"><span data-stu-id="8bdd5-188">Syntax: `Start-InformationBarrierPoliciesApplication`</span></span>

    <span data-ttu-id="8bdd5-189">사용자가 조직에 대해 변경 내용을 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="8bdd5-189">Changes are applied, user by user, for your organization.</span></span> <span data-ttu-id="8bdd5-190">대규모 조직에서는이 프로세스를 완료 하는 데 24 시간 이상 소요 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8bdd5-190">If your organization is large, it can take 24 hours (or more) for this process to complete.</span></span>

## <a name="stop-a-policy-application"></a><span data-ttu-id="8bdd5-191">정책 응용 프로그램 중지</span><span class="sxs-lookup"><span data-stu-id="8bdd5-191">Stop a policy application</span></span>

<span data-ttu-id="8bdd5-192">정보 장벽 정책 적용을 시작 하 고 나면 해당 정책을 적용 하지 않으려면 다음 절차를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="8bdd5-192">If, after you have started applying information barrier policies, you want to stop those policies from being applied, use the following procedure.</span></span> <span data-ttu-id="8bdd5-193">프로세스를 시작 하는 데 약 30-35 분이 소요 됨을 염두에 두어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="8bdd5-193">Keep in mind that it will take approximately 30-35 minutes for the process to begin.</span></span>

1. <span data-ttu-id="8bdd5-194">가장 최근 정보 장벽 정책 응용 프로그램의 상태를 확인 하려면 **InformationBarrierPoliciesApplicationStatus** cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="8bdd5-194">To view the status of the most recent information barrier policy application, use the **Get-InformationBarrierPoliciesApplicationStatus** cmdlet.</span></span>

    <span data-ttu-id="8bdd5-195">구문과`Get-InformationBarrierPoliciesApplicationStatus`</span><span class="sxs-lookup"><span data-stu-id="8bdd5-195">Syntax: `Get-InformationBarrierPoliciesApplicationStatus`</span></span>

    <span data-ttu-id="8bdd5-196">응용 프로그램의 GUID를 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="8bdd5-196">Note the application's GUID.</span></span>

2. <span data-ttu-id="8bdd5-197">**InformationBarrierPoliciesApplication** Cmdlet을 Identity 매개 변수와 함께 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="8bdd5-197">Use the **Stop-InformationBarrierPoliciesApplication** cmdlet with an Identity parameter.</span></span>

    <span data-ttu-id="8bdd5-198">구문과`Stop-InformationBarrierPoliciesApplication -Identity GUID`</span><span class="sxs-lookup"><span data-stu-id="8bdd5-198">Syntax:  `Stop-InformationBarrierPoliciesApplication -Identity GUID`</span></span>

    <span data-ttu-id="8bdd5-199">예제: `Stop-InformationBarrierPoliciesApplication -Identity 46237888-12ca-42e3-a541-3fcb7b5231d1`</span><span class="sxs-lookup"><span data-stu-id="8bdd5-199">Example: `Stop-InformationBarrierPoliciesApplication -Identity 46237888-12ca-42e3-a541-3fcb7b5231d1`</span></span>

    <span data-ttu-id="8bdd5-200">이 예에서는 정보 장벽 정책이 적용 되지 않도록 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="8bdd5-200">In this example, we are stopping information barrier policies from being applied.</span></span>

## <a name="related-articles"></a><span data-ttu-id="8bdd5-201">관련 문서</span><span class="sxs-lookup"><span data-stu-id="8bdd5-201">Related articles</span></span>

[<span data-ttu-id="8bdd5-202">정보 장벽에 대 한 개요 보기</span><span class="sxs-lookup"><span data-stu-id="8bdd5-202">Get an overview of information barriers</span></span>](information-barriers.md)

[<span data-ttu-id="8bdd5-203">정보 장벽에 대 한 정책 정의 (미리 보기)</span><span class="sxs-lookup"><span data-stu-id="8bdd5-203">Define policies for information barriers (Preview)</span></span>](information-barriers-policies.md)

[<span data-ttu-id="8bdd5-204">Microsoft 팀의 정보 장벽에 대해 자세히 알아보기</span><span class="sxs-lookup"><span data-stu-id="8bdd5-204">Learn more about information barriers in Microsoft Teams</span></span>](https://docs.microsoft.com/MicrosoftTeams/information-barriers-in-teams)

[<span data-ttu-id="8bdd5-205">정보 장벽 정책의 특성 (미리 보기)</span><span class="sxs-lookup"><span data-stu-id="8bdd5-205">Attributes for information barrier policies (Preview)</span></span>](information-barriers-attributes.md)

[<span data-ttu-id="8bdd5-206">정보 장벽 문제 해결 (미리 보기)</span><span class="sxs-lookup"><span data-stu-id="8bdd5-206">Troubleshooting information barriers (Preview)</span></span>](information-barriers-troubleshooting.md)
