---
title: 정보 장벽 정책 편집
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 06/28/2019
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.collection:
- M365-security-compliance
localization_priority: None
description: 정보 장벽에 대 한 정책을 편집 하거나 제거 하는 방법을 알아봅니다.
ms.openlocfilehash: c3dca18ad217b89d9f9ae78b590cfb07f4631f37
ms.sourcegitcommit: 011bfa60cafdf47900aadf96a17eb275efa877c4
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/29/2019
ms.locfileid: "35394333"
---
# <a name="edit-or-remove-information-barrier-policies-preview"></a><span data-ttu-id="07a78-103">정보 장벽 정책 편집 (또는 제거) (미리 보기)</span><span class="sxs-lookup"><span data-stu-id="07a78-103">Edit (or remove) information barrier policies (Preview)</span></span>

<span data-ttu-id="07a78-104">[정보 장벽 정책을 정의한](information-barriers-policies.md)후에는 [문제 해결](information-barriers-troubleshooting.md) 또는 일반 유지 관리의 일환으로 이러한 정책 또는 사용자 세그먼트를 변경 해야 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="07a78-104">After you have [defined information barrier policies](information-barriers-policies.md), you might need to make changes to those policies or to your user segments, as part of [troubleshooting](information-barriers-troubleshooting.md) or as regular maintenance.</span></span> <span data-ttu-id="07a78-105">이 문서를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="07a78-105">Use this article as a guide.</span></span>

## <a name="what-do-you-want-to-do"></a><span data-ttu-id="07a78-106">무슨 작업을 하고 싶으십니까?</span><span class="sxs-lookup"><span data-stu-id="07a78-106">What do you want to do?</span></span>

|<span data-ttu-id="07a78-107">동작은</span><span class="sxs-lookup"><span data-stu-id="07a78-107">Action</span></span>  |<span data-ttu-id="07a78-108">설명</span><span class="sxs-lookup"><span data-stu-id="07a78-108">Description</span></span> |
|---------|---------|
|[<span data-ttu-id="07a78-109">사용자 계정 특성 편집</span><span class="sxs-lookup"><span data-stu-id="07a78-109">Edit user account attributes</span></span>](#edit-user-account-attributes)     |<span data-ttu-id="07a78-110">세그먼트를 정의 하는 데 사용할 수 있는 특성을 Azure Active Directory에 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="07a78-110">Fill in attributes in Azure Active Directory that can be used to define segments.</span></span><br/><span data-ttu-id="07a78-111">사용자 계정 특성을 편집 해야 하는 세그먼트에 사용자가 포함 되어 있지 않거나, 사용자가 속한 세그먼트를 변경 하거나, 다른 특성을 사용 하 여 세그먼트를 정의할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="07a78-111">Edit user account attributes when users are not included in segments they should be, to change which segments users are in, or to define segments using different attributes.</span></span>         |
|[<span data-ttu-id="07a78-112">세그먼트 편집</span><span class="sxs-lookup"><span data-stu-id="07a78-112">Edit a segment</span></span>](#edit-a-segment)     |<span data-ttu-id="07a78-113">세그먼트 정의 방법을 변경 하려면 세그먼트를 편집 합니다.</span><span class="sxs-lookup"><span data-stu-id="07a78-113">Edit segments when you want to change how a segment is defined.</span></span> <br/><span data-ttu-id="07a78-114">예를 들어 처음에 *부서* 를 사용 하 여 세그먼트를 정의 했을 때, 이제 *MemberOf*와 같은 다른 특성을 사용 하려고 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="07a78-114">For example, you might have originally defined segments using *Department* and now want to use another attribute, such as *MemberOf*.</span></span>         |
|[<span data-ttu-id="07a78-115">정책 편집</span><span class="sxs-lookup"><span data-stu-id="07a78-115">Edit a policy</span></span>](#edit-a-policy)     |<span data-ttu-id="07a78-116">정책 작동 방식을 변경 하려면 정보 장벽 정책 편집을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="07a78-116">Edit an information barrier policy when you want to change how a policy works.</span></span><br/><span data-ttu-id="07a78-117">예를 들어 두 세그먼트 간의 통신을 차단 하는 대신 특정 세그먼트 간에만 통신을 수행 하도록 할지 결정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="07a78-117">For example, instead of blocking communications between two segments, you might decide you want to allow communications to occur only between certain segments.</span></span>         |
|[<span data-ttu-id="07a78-118">정책을 비활성 상태로 설정</span><span class="sxs-lookup"><span data-stu-id="07a78-118">Set a policy to inactive status</span></span>](#set-a-policy-to-inactive-status)     |<span data-ttu-id="07a78-119">정책을 변경 하려는 경우 또는 정책을 적용 하지 않으려는 경우에는 정책을 비활성 상태로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="07a78-119">Set a policy to inactive status when you want to make changes to a policy, or when you don't want a policy to be in effect.</span></span>         |
|[<span data-ttu-id="07a78-120">정책 제거</span><span class="sxs-lookup"><span data-stu-id="07a78-120">Remove a policy</span></span>](#remove-a-policy)     |<span data-ttu-id="07a78-121">특정 정책이 더 이상 필요 하지 않은 경우 정보 장벽 정책을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="07a78-121">Remove an information barrier policy when you no longer need a particular policy in place.</span></span>         |
|[<span data-ttu-id="07a78-122">정책 응용 프로그램 중지</span><span class="sxs-lookup"><span data-stu-id="07a78-122">Stop a policy application</span></span>](#stop-a-policy-application)     |<span data-ttu-id="07a78-123">정보 장벽 정책을 적용 하는 프로세스를 중지 하려면이 작업을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="07a78-123">Do this when you want to stop the process of applying information barrier policies.</span></span><br/><span data-ttu-id="07a78-124">정책 응용 프로그램을 중지 하는 것은 즉각적이 아니며 사용자에 게 이미 적용 된 정책을 실행 취소 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="07a78-124">Note that stopping a policy application is not instant, and it does not undo policies that are already applied to users.</span></span>         |
|[<span data-ttu-id="07a78-125">정보 장벽에 대 한 정책 정의 (미리 보기)</span><span class="sxs-lookup"><span data-stu-id="07a78-125">Define policies for information barriers (Preview)</span></span>](information-barriers-policies.md)     |<span data-ttu-id="07a78-126">해당 정책이 아직 위치에 없는 경우 정보 장벽 정책을 정의 하 고, 특정 사용자 그룹 간의 통신을 제한 하거나 제한 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="07a78-126">Define an information barrier policy when you do not already have such policies in place, and you must restrict or limit communications between specific groups of users.</span></span>         |
|[<span data-ttu-id="07a78-127">정보 장벽 문제 해결 (미리 보기)</span><span class="sxs-lookup"><span data-stu-id="07a78-127">Troubleshooting information barriers (Preview)</span></span>](information-barriers-troubleshooting.md)     |<span data-ttu-id="07a78-128">정보 장벽에서 예기치 않은 문제가 발생 하는 경우이 문서를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="07a78-128">Refer to this article when you run into unexpected issues with information barriers.</span></span>         |

> [!IMPORTANT]
> <span data-ttu-id="07a78-129">이 문서에서 설명 하는 작업을 수행 하려면 다음 중 하 나와 같은 적절 한 역할을 할당 받아야 합니다.</span><span class="sxs-lookup"><span data-stu-id="07a78-129">To perform the tasks described in this article, you must be assigned an appropriate role, such as one of the following:</span></span><br/><span data-ttu-id="07a78-130">-Microsoft 365 Enterprise 전역 관리자</span><span class="sxs-lookup"><span data-stu-id="07a78-130">- Microsoft 365 Enterprise Global Administrator</span></span><br/><span data-ttu-id="07a78-131">-Office 365 전역 관리자</span><span class="sxs-lookup"><span data-stu-id="07a78-131">- Office 365 Global Administrator</span></span><br/><span data-ttu-id="07a78-132">-준수 관리자</span><span class="sxs-lookup"><span data-stu-id="07a78-132">- Compliance Administrator</span></span><br/><span data-ttu-id="07a78-133">-IB 준수 관리 (새 역할입니다.)</span><span class="sxs-lookup"><span data-stu-id="07a78-133">- IB Compliance Management (this is a new role!)</span></span><p><span data-ttu-id="07a78-134">정보 장벽에 대 한 필수 구성 요소에 대 한 자세한 내용은 [필수 구성 요소 (정보 장벽 정책)](information-barriers-policies.md#prerequisites)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="07a78-134">To learn more about prerequisites for information barriers, see [Prerequisites (for information barrier policies)](information-barriers-policies.md#prerequisites).</span></span><p><span data-ttu-id="07a78-135">[Office 365 Security & 준수 센터 PowerShell에 연결](https://docs.microsoft.com/powershell/exchange/office-365-scc/connect-to-scc-powershell/connect-to-scc-powershell?view=exchange-ps)되어 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="07a78-135">Make sure to [connect to Office 365 Security & Compliance Center PowerShell](https://docs.microsoft.com/powershell/exchange/office-365-scc/connect-to-scc-powershell/connect-to-scc-powershell?view=exchange-ps).</span></span>

## <a name="edit-user-account-attributes"></a><span data-ttu-id="07a78-136">사용자 계정 특성 편집</span><span class="sxs-lookup"><span data-stu-id="07a78-136">Edit user account attributes</span></span>

<span data-ttu-id="07a78-137">다음 절차에 사용 하 여 사용자 조각화에 사용 되는 특성을 편집 합니다.</span><span class="sxs-lookup"><span data-stu-id="07a78-137">Use this procedure to edit attributes that are used for segmenting users.</span></span> 

<span data-ttu-id="07a78-138">예를 들어 부서 특성을 사용 하는 경우 현재 하나 이상의 사용자 계정에 부서에 대해 나열 된 값이 없는 경우 부서 정보를 포함 하도록 해당 사용자 계정을 편집 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="07a78-138">For example, if you are using a Department attribute, and one or more user accounts do not currently have any values listed for Department, you must edit those user accounts to include Department information.</span></span> 

<span data-ttu-id="07a78-139">사용자 계정 특성은 정보 장벽 정책을 할당할 수 있도록 세그먼트를 정의 하는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="07a78-139">User account attributes are used for defining segments so that information barrier policies can be assigned.</span></span>

1. <span data-ttu-id="07a78-140">특성 값 및 할당 된 세그먼트와 같은 특정 사용자 계정에 대 한 세부 정보를 보려면 **InformationBarrierRecipientStatus** Cmdlet을 Identity 매개 변수와 함께 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="07a78-140">To view details for a specific user account, such as attribute values and assigned segment(s), use the **Get-InformationBarrierRecipientStatus** cmdlet with Identity parameters.</span></span> 

    |<span data-ttu-id="07a78-141">구문과</span><span class="sxs-lookup"><span data-stu-id="07a78-141">Syntax</span></span>  |<span data-ttu-id="07a78-142">예제</span><span class="sxs-lookup"><span data-stu-id="07a78-142">Example</span></span>  |
    |---------|---------|
    |`Get-InformationBarrierRecipientStatus -Identity <value> -Identity2 <value>` <p>   <span data-ttu-id="07a78-143">이름, 별칭, 고유 이름, 정식 도메인 이름, 전자 메일 주소 또는 GUID와 같은 각 사용자를 고유 하 게 식별 하는 모든 값을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="07a78-143">You can use any value that uniquely identifies each user, such as name, alias, distinguished name, canonical domain name, email address, or GUID.</span></span> <p>   <span data-ttu-id="07a78-144">(단일 사용자에 대해이 cmdlet을 사용할 수도 있습니다. `Get-InformationBarrierRecipientStatus -Identity <value>`)</span><span class="sxs-lookup"><span data-stu-id="07a78-144">(You can also use this cmdlet for a single user: `Get-InformationBarrierRecipientStatus -Identity <value>`)</span></span>      |`Get-InformationBarrierRecipientStatus -Identity meganb -Identity2 alexw`  <p>   <span data-ttu-id="07a78-145">이 예에서는 Office 365의 두 사용자 계정 ( *Megan*용 *meganb* 및 *Alex*용 *alexw* )을 참조 합니다.</span><span class="sxs-lookup"><span data-stu-id="07a78-145">In this example, we refer to two user accounts in Office 365: *meganb* for *Megan*, and *alexw* for *Alex*.</span></span>         |

2. <span data-ttu-id="07a78-146">사용자 계정 프로필에 대해 편집 하려는 특성을 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="07a78-146">Determine which attribute you want to edit for your user account profile(s).</span></span> <span data-ttu-id="07a78-147">자세한 [내용은 정보 장벽 정책 (미리 보기)에 대 한 특성](information-barriers-attributes.md) 을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="07a78-147">Refer to [Attributes for information barrier policies (Preview)](information-barriers-attributes.md) for more details.</span></span> 

3. <span data-ttu-id="07a78-148">이전 단계에서 선택한 특성에 대 한 값을 포함 하도록 하나 이상의 사용자 계정을 편집 합니다.</span><span class="sxs-lookup"><span data-stu-id="07a78-148">Edit one or more user accounts to include values for the attribute you selected in the previous step.</span></span> <span data-ttu-id="07a78-149">이렇게 하려면 다음 절차 중 하나를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="07a78-149">To do this, use one of the following procedures:</span></span>

    - <span data-ttu-id="07a78-150">단일 계정을 편집 하려면 [Azure Active Directory를 사용 하 여 사용자 프로필 정보 추가 또는 업데이트](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-users-profile-azure-portal)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="07a78-150">To edit a single account, see [Add or update a user's profile information using Azure Active Directory](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-users-profile-azure-portal).</span></span>

    - <span data-ttu-id="07a78-151">여러 계정을 편집 하거나 PowerShell을 사용 하 여 단일 계정을 편집 하려면 [Office 365 PowerShell을 사용 하 여 사용자 계정 속성 구성을](https://docs.microsoft.com/office365/enterprise/powershell/configure-user-account-properties-with-office-365-powershell)참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="07a78-151">To edit multiple accounts (or use PowerShell to edit a single account), see [Configure user account properties with Office 365 PowerShell](https://docs.microsoft.com/office365/enterprise/powershell/configure-user-account-properties-with-office-365-powershell).</span></span>

## <a name="edit-a-segment"></a><span data-ttu-id="07a78-152">세그먼트 편집</span><span class="sxs-lookup"><span data-stu-id="07a78-152">Edit a segment</span></span>

<span data-ttu-id="07a78-153">이 절차를 사용 하 여 사용자 세그먼트의 정의를 편집 합니다.</span><span class="sxs-lookup"><span data-stu-id="07a78-153">Use this procedure edit the definition of a user segment.</span></span> <span data-ttu-id="07a78-154">예를 들어 세그먼트 이름을 변경 하거나 세그먼트에 포함 된 사용자를 확인 하는 데 사용 되는 필터를 변경할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="07a78-154">For example, you might change the name of a segment, or the filter that is used to determine who's included in the segment.</span></span>

1. <span data-ttu-id="07a78-155">모든 기존 세그먼트를 보려면 **OrganizationSegment** cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="07a78-155">To view all existing segments, use the **Get-OrganizationSegment** cmdlet.</span></span>
    
    <span data-ttu-id="07a78-156">구문과`Get-OrganizationSegment`</span><span class="sxs-lookup"><span data-stu-id="07a78-156">Syntax: `Get-OrganizationSegment`</span></span>

    <span data-ttu-id="07a78-157">세그먼트 유형, UserGroupFilter 값, 해당 개체를 만들거나 마지막으로 수정한 사람, GUID 등의 각 세그먼트와 세부 정보에 대 한 목록이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="07a78-157">You will see a list of segments and details for each, such as segment type, its UserGroupFilter value, who created or last modified it, GUID, and so on.</span></span>

    > [!TIP]
    > <span data-ttu-id="07a78-158">나중에 참조 하기 위해 세그먼트 목록을 인쇄 하거나 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="07a78-158">Print or save your list of segments for reference later.</span></span> <span data-ttu-id="07a78-159">예를 들어 세그먼트를 편집 하려면 해당 이름을 확인 하거나 값을 식별 해야 합니다 (이는 Identity 매개 변수와 함께 사용 됨).</span><span class="sxs-lookup"><span data-stu-id="07a78-159">For example, if you want to edit a segment, you will need to know its name or identify value (this is used with the Identity parameter).</span></span>

2. <span data-ttu-id="07a78-160">세그먼트를 편집 하려면 **Identity** 매개 변수와 관련 세부 정보와 함께 **OrganizationSegment** cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="07a78-160">To edit a segment, use the **Set-OrganizationSegment** cmdlet with the **Identity** parameter and relevant details.</span></span> 

    |<span data-ttu-id="07a78-161">구문과</span><span class="sxs-lookup"><span data-stu-id="07a78-161">Syntax</span></span>  |<span data-ttu-id="07a78-162">예제</span><span class="sxs-lookup"><span data-stu-id="07a78-162">Example</span></span>  |
    |---------|---------|
    |`Set-OrganizationSegment -Identity GUID -UserGroupFilter "attribute -eq 'attributevalue'"`     |`Set-OrganizationSegment -Identity c96e0837-c232-4a8a-841e-ef45787d8fcd -UserGroupFilter "Department -eq 'HRDept'"` <p><span data-ttu-id="07a78-163">이 예에서는 GUID가 *c96e0837-c232-4a8a-841e-ef45787d8fcd*인 세그먼트에 대해 부서 이름을 "hrdept"로 업데이트 했습니다.</span><span class="sxs-lookup"><span data-stu-id="07a78-163">In this example, for the segment that has the GUID *c96e0837-c232-4a8a-841e-ef45787d8fcd*, we updated the department name to "HRDept".</span></span>         |

<span data-ttu-id="07a78-164">조직의 세그먼트 편집을 마친 후에는 정보 장벽 정책을 [정의](information-barriers-policies.md#part-2-define-information-barrier-policies) 하거나 [편집할](#edit-a-policy) 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="07a78-164">When you have finished editing segments for your organization, you can either [define](information-barriers-policies.md#part-2-define-information-barrier-policies) or [edit](#edit-a-policy) information barrier policies.</span></span>

## <a name="edit-a-policy"></a><span data-ttu-id="07a78-165">정책 편집</span><span class="sxs-lookup"><span data-stu-id="07a78-165">Edit a policy</span></span>

1. <span data-ttu-id="07a78-166">현재 정보 장벽 정책 목록을 보려면 **InformationBarrierPolicy** cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="07a78-166">To view a list of current information barrier policies, use the **Get-InformationBarrierPolicy** cmdlet.</span></span>

    <span data-ttu-id="07a78-167">구문과`Get-InformationBarrierPolicy`</span><span class="sxs-lookup"><span data-stu-id="07a78-167">Syntax: `Get-InformationBarrierPolicy`</span></span>

    <span data-ttu-id="07a78-168">결과 목록에서 변경 하려는 정책을 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="07a78-168">In the list of results, identify the policy that you want to change.</span></span> <span data-ttu-id="07a78-169">정책의 GUID 및 이름을 적어둡니다.</span><span class="sxs-lookup"><span data-stu-id="07a78-169">Note the policy's GUID and name.</span></span>

2. <span data-ttu-id="07a78-170">**InformationBarrierPolicy** Cmdlet에서 **Identity** 매개 변수를 사용 하 여 변경할 내용을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="07a78-170">Use the **Set-InformationBarrierPolicy** cmdlet with an **Identity** parameter, and specify the changes you want to make.</span></span>

    <span data-ttu-id="07a78-171">예: *연구* 세그먼트가 *영업* 및 *마케팅* 세그먼트와 통신 하지 못하도록 차단 하도록 정책이 정의 되어 있다고 가정 합니다.</span><span class="sxs-lookup"><span data-stu-id="07a78-171">Example: Suppose a policy was defined to block the *Research* segment from communicating with the *Sales* and *Marketing* segments.</span></span> <span data-ttu-id="07a78-172">이 cmdlet을 사용 하 여 정책이 정의 되었습니다.`New-InformationBarrierPolicy -Name "Research-SalesMarketing" -AssignedSegment "Research" -SegmentsBlocked "Sales","Marketing"`</span><span class="sxs-lookup"><span data-stu-id="07a78-172">The policy was defined by using this cmdlet: `New-InformationBarrierPolicy -Name "Research-SalesMarketing" -AssignedSegment "Research" -SegmentsBlocked "Sales","Marketing"`</span></span>
    
    <span data-ttu-id="07a78-173">*리서치* 세그먼트의 사람들이 *HR* 세그먼트의 사용자와만 통신할 수 있도록이를 변경 하려는 경우를 가정해 보겠습니다.</span><span class="sxs-lookup"><span data-stu-id="07a78-173">Suppose we want to change it so that people in the *Research* segment can only communicate with people in the *HR* segment.</span></span> <span data-ttu-id="07a78-174">이 변경 작업을 수행 하려면 다음 cmdlet을 사용 합니다.`Set-InformationBarrierPolicy -Identity 43c37853-ea10-4b90-a23d-ab8c93772471 -SegmentsAllowed "HR"`</span><span class="sxs-lookup"><span data-stu-id="07a78-174">To make this change, we use this cmdlet: `Set-InformationBarrierPolicy -Identity 43c37853-ea10-4b90-a23d-ab8c93772471 -SegmentsAllowed "HR"`</span></span>

    <span data-ttu-id="07a78-175">이 예에서는 "SegmentsBlocked"를 "SegmentsAllowed"로 변경 하 고 *HR* 세그먼트를 지정 했습니다.</span><span class="sxs-lookup"><span data-stu-id="07a78-175">In this example, we changed "SegmentsBlocked" to "SegmentsAllowed" and specified the *HR* segment.</span></span>

3. <span data-ttu-id="07a78-176">정책 편집을 마친 후에는 변경 내용을 적용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="07a78-176">When you are finished editing a policy, make sure to apply your changes.</span></span> <span data-ttu-id="07a78-177">( [정보 장벽 정책 적용](information-barriers-policies.md#part-3-apply-information-barrier-policies)참조)</span><span class="sxs-lookup"><span data-stu-id="07a78-177">(See [Apply information barrier policies](information-barriers-policies.md#part-3-apply-information-barrier-policies).)</span></span>

## <a name="set-a-policy-to-inactive-status"></a><span data-ttu-id="07a78-178">정책을 비활성 상태로 설정</span><span class="sxs-lookup"><span data-stu-id="07a78-178">Set a policy to inactive status</span></span>

1. <span data-ttu-id="07a78-179">현재 정보 장벽 정책 목록을 보려면 **InformationBarrierPolicy** cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="07a78-179">To view a list of current information barrier policies, use the **Get-InformationBarrierPolicy** cmdlet.</span></span>

    <span data-ttu-id="07a78-180">구문과`Get-InformationBarrierPolicy`</span><span class="sxs-lookup"><span data-stu-id="07a78-180">Syntax: `Get-InformationBarrierPolicy`</span></span>

    <span data-ttu-id="07a78-181">결과 목록에서 변경 하거나 제거할 정책을 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="07a78-181">In the list of results, identify the policy that you want to change (or remove).</span></span> <span data-ttu-id="07a78-182">정책의 GUID 및 이름을 적어둡니다.</span><span class="sxs-lookup"><span data-stu-id="07a78-182">Note the policy's GUID and name.</span></span>

2. <span data-ttu-id="07a78-183">정책의 상태를 비활성으로 설정 하려면 Identity 매개 변수와 함께 **InformationBarrierPolicy** cmdlet을 사용 하 고 State 매개 변수는 비활성으로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="07a78-183">To set the policy's status to inactive, use the **Set-InformationBarrierPolicy** cmdlet with an Identity parameter and the State parameter set to Inactive.</span></span>

    |<span data-ttu-id="07a78-184">구문과</span><span class="sxs-lookup"><span data-stu-id="07a78-184">Syntax</span></span>  |<span data-ttu-id="07a78-185">예제</span><span class="sxs-lookup"><span data-stu-id="07a78-185">Example</span></span>  |
    |---------|---------|
    |`Set-InformationBarrierPolicy -Identity GUID -State Inactive`     |`Set-InformationBarrierPolicy -Identity 43c37853-ea10-4b90-a23d-ab8c9377247 -State Inactive` <p><span data-ttu-id="07a78-186">이 예에서는 GUID *43c37853-ea10-4b90-a23d-ab8c9377247을 사용* 하는 정보 장벽 정책을 비활성 상태로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="07a78-186">In this example, we set an information barrier policy that has GUID *43c37853-ea10-4b90-a23d-ab8c9377247* to an inactive status.</span></span>         |

3. <span data-ttu-id="07a78-187">변경 내용을 적용 하려면 **InformationBarrierPoliciesApplication** cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="07a78-187">To apply your changes, use the **Start-InformationBarrierPoliciesApplication** cmdlet.</span></span>

    <span data-ttu-id="07a78-188">구문과`Start-InformationBarrierPoliciesApplication`</span><span class="sxs-lookup"><span data-stu-id="07a78-188">Syntax: `Start-InformationBarrierPoliciesApplication`</span></span>

    <span data-ttu-id="07a78-189">사용자가 조직에 대해 변경 내용을 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="07a78-189">Changes are applied, user by user, for your organization.</span></span> <span data-ttu-id="07a78-190">대규모 조직에서는이 프로세스를 완료 하는 데 24 시간 이상 소요 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="07a78-190">If your organization is large, it can take 24 hours (or more) for this process to complete.</span></span> <span data-ttu-id="07a78-191">일반적으로 5000 사용자 계정을 처리 하는 데 한 시간 정도 소요 됩니다.</span><span class="sxs-lookup"><span data-stu-id="07a78-191">(As a general guideline, it takes about an hour to process 5,000 user accounts.)</span></span>

<span data-ttu-id="07a78-192">이때 하나 이상의 정보 장벽 정책이 비활성 상태로 설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="07a78-192">At this point, one or more information barrier policies are set to inactive status.</span></span> <span data-ttu-id="07a78-193">여기서는 다음 작업을 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="07a78-193">From here, you can do any of the following:</span></span>
- <span data-ttu-id="07a78-194">그대로 유지 (비활성 상태로 설정 된 정책이 사용자에 게 영향을 주지 않음)</span><span class="sxs-lookup"><span data-stu-id="07a78-194">Keep it as is (a policy set to inactive status has no effect on users)</span></span>
- [<span data-ttu-id="07a78-195">정책 편집</span><span class="sxs-lookup"><span data-stu-id="07a78-195">Edit a policy</span></span>](#edit-a-policy) 
- [<span data-ttu-id="07a78-196">정책 제거</span><span class="sxs-lookup"><span data-stu-id="07a78-196">Remove a policy</span></span>](#remove-a-policy)

## <a name="remove-a-policy"></a><span data-ttu-id="07a78-197">정책 제거</span><span class="sxs-lookup"><span data-stu-id="07a78-197">Remove a policy</span></span>

1. <span data-ttu-id="07a78-198">현재 정보 장벽 정책 목록을 보려면 **InformationBarrierPolicy** cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="07a78-198">To view a list of current information barrier policies, use the **Get-InformationBarrierPolicy** cmdlet.</span></span>

    <span data-ttu-id="07a78-199">구문과`Get-InformationBarrierPolicy`</span><span class="sxs-lookup"><span data-stu-id="07a78-199">Syntax: `Get-InformationBarrierPolicy`</span></span>

    <span data-ttu-id="07a78-200">결과 목록에서 제거할 정책을 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="07a78-200">In the list of results, identify the policy that you want to remove.</span></span> <span data-ttu-id="07a78-201">정책의 GUID 및 이름을 적어둡니다.</span><span class="sxs-lookup"><span data-stu-id="07a78-201">Note the policy's GUID and name.</span></span> <span data-ttu-id="07a78-202">정책이 비활성 상태로 설정 되어 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="07a78-202">Make sure the policy is set to inactive status.</span></span>

2. <span data-ttu-id="07a78-203">**InformationBarrierPolicy** Cmdlet을 Identity 매개 변수와 함께 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="07a78-203">Use the **Remove-InformationBarrierPolicy** cmdlet with an Identity parameter.</span></span>

    |<span data-ttu-id="07a78-204">구문과</span><span class="sxs-lookup"><span data-stu-id="07a78-204">Syntax</span></span>  |<span data-ttu-id="07a78-205">예제</span><span class="sxs-lookup"><span data-stu-id="07a78-205">Example</span></span>  |
    |---------|---------|
    |`Remove-InformationBarrierPolicy -Identity GUID`     |`Remove-InformationBarrierPolicy -Identity 43c37853-ea10-4b90-a23d-ab8c93772471` <p><span data-ttu-id="07a78-206">이 예에서는 GUID가 *43c37853-ea10-4b90-a23d-ab8c93772471*인 정책을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="07a78-206">In this example, we are removing the policy that has GUID *43c37853-ea10-4b90-a23d-ab8c93772471*.</span></span>          |

    <span data-ttu-id="07a78-207">메시지가 표시 되 면 변경 내용을 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="07a78-207">When prompted, confirm the change.</span></span>

3. <span data-ttu-id="07a78-208">제거할 각 정책에 대해 1-2 단계를 반복 합니다.</span><span class="sxs-lookup"><span data-stu-id="07a78-208">Repeat steps 1-2 for each policy you want to remove.</span></span>

4. <span data-ttu-id="07a78-209">정책을 제거한 후에는 변경 내용을 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="07a78-209">When you are finished removing policies, apply your changes.</span></span> <span data-ttu-id="07a78-210">이 작업을 수행 하려면 **InformationBarrierPoliciesApplication** cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="07a78-210">To do this, use the **Start-InformationBarrierPoliciesApplication** cmdlet.</span></span>

    <span data-ttu-id="07a78-211">구문과`Start-InformationBarrierPoliciesApplication`</span><span class="sxs-lookup"><span data-stu-id="07a78-211">Syntax: `Start-InformationBarrierPoliciesApplication`</span></span>

    <span data-ttu-id="07a78-212">사용자가 조직에 대해 변경 내용을 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="07a78-212">Changes are applied, user by user, for your organization.</span></span> <span data-ttu-id="07a78-213">대규모 조직에서는이 프로세스를 완료 하는 데 24 시간 이상 소요 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="07a78-213">If your organization is large, it can take 24 hours (or more) for this process to complete.</span></span>

## <a name="stop-a-policy-application"></a><span data-ttu-id="07a78-214">정책 응용 프로그램 중지</span><span class="sxs-lookup"><span data-stu-id="07a78-214">Stop a policy application</span></span>

<span data-ttu-id="07a78-215">정보 장벽 정책 적용을 시작 하 고 나면 해당 정책을 적용 하지 않으려면 다음 절차를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="07a78-215">If, after you have started applying information barrier policies, you want to stop those policies from being applied, use the following procedure.</span></span> <span data-ttu-id="07a78-216">프로세스를 시작 하는 데 약 30-35 분이 소요 됨을 염두에 두어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="07a78-216">Keep in mind that it will take approximately 30-35 minutes for the process to begin.</span></span>

1. <span data-ttu-id="07a78-217">가장 최근 정보 장벽 정책 응용 프로그램의 상태를 확인 하려면 **InformationBarrierPoliciesApplicationStatus** cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="07a78-217">To view the status of the most recent information barrier policy application, use the **Get-InformationBarrierPoliciesApplicationStatus** cmdlet.</span></span>

    <span data-ttu-id="07a78-218">구문과`Get-InformationBarrierPoliciesApplicationStatus`</span><span class="sxs-lookup"><span data-stu-id="07a78-218">Syntax: `Get-InformationBarrierPoliciesApplicationStatus`</span></span>

    <span data-ttu-id="07a78-219">응용 프로그램의 GUID를 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="07a78-219">Note the application's GUID.</span></span>

2. <span data-ttu-id="07a78-220">**InformationBarrierPoliciesApplication** Cmdlet을 Identity 매개 변수와 함께 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="07a78-220">Use the **Stop-InformationBarrierPoliciesApplication** cmdlet with an Identity parameter.</span></span>

    |<span data-ttu-id="07a78-221">구문과</span><span class="sxs-lookup"><span data-stu-id="07a78-221">Syntax</span></span>  |<span data-ttu-id="07a78-222">예제</span><span class="sxs-lookup"><span data-stu-id="07a78-222">Example</span></span>  |
    |---------|---------|
    |`Stop-InformationBarrierPoliciesApplication -Identity GUID`     |`Stop-InformationBarrierPoliciesApplication -Identity 46237888-12ca-42e3-a541-3fcb7b5231d1` <p><span data-ttu-id="07a78-223">이 예에서는 정보 장벽 정책이 적용 되지 않도록 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="07a78-223">In this example, we are stopping information barrier policies from being applied.</span></span>         |

## <a name="related-articles"></a><span data-ttu-id="07a78-224">관련 문서</span><span class="sxs-lookup"><span data-stu-id="07a78-224">Related articles</span></span>

[<span data-ttu-id="07a78-225">정보 장벽에 대 한 개요 보기</span><span class="sxs-lookup"><span data-stu-id="07a78-225">Get an overview of information barriers</span></span>](information-barriers.md)

[<span data-ttu-id="07a78-226">정보 장벽에 대 한 정책 정의 (미리 보기)</span><span class="sxs-lookup"><span data-stu-id="07a78-226">Define policies for information barriers (Preview)</span></span>](information-barriers-policies.md)

[<span data-ttu-id="07a78-227">Microsoft 팀의 정보 장벽에 대해 자세히 알아보기</span><span class="sxs-lookup"><span data-stu-id="07a78-227">Learn more about information barriers in Microsoft Teams</span></span>](https://docs.microsoft.com/MicrosoftTeams/information-barriers-in-teams)

[<span data-ttu-id="07a78-228">정보 장벽 정책의 특성 (미리 보기)</span><span class="sxs-lookup"><span data-stu-id="07a78-228">Attributes for information barrier policies (Preview)</span></span>](information-barriers-attributes.md)

[<span data-ttu-id="07a78-229">정보 장벽 문제 해결 (미리 보기)</span><span class="sxs-lookup"><span data-stu-id="07a78-229">Troubleshooting information barriers (Preview)</span></span>](information-barriers-troubleshooting.md)
