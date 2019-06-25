---
title: 정보 장벽 문제 해결
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
description: 이 문서를 정보 장벽 문제 해결을 위한 지침으로 사용 하십시오.
ms.openlocfilehash: e8750358aaa7788c85f0ab656b30f5b5149d898c
ms.sourcegitcommit: 044003455eb36071806c9f008ac631d54c64dde6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/24/2019
ms.locfileid: "35199516"
---
# <a name="troubleshooting-information-barriers-preview"></a><span data-ttu-id="dd7c7-103">정보 장벽 문제 해결 (미리 보기)</span><span class="sxs-lookup"><span data-stu-id="dd7c7-103">Troubleshooting information barriers (Preview)</span></span>

<span data-ttu-id="dd7c7-104">[정보 장벽 (미리 보기)](information-barriers.md) 을 사용 하면 조직이 법적 요구 사항 및 업계 규정을 준수 하는 데 도움이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="dd7c7-104">[Information barriers (Preview)](information-barriers.md) can help your organization remain compliant with legal requirements and industry regulations.</span></span> <span data-ttu-id="dd7c7-105">예를 들어 정보 장벽에서는 특정 사용자 그룹 간의 통신을 제한 하 여 관심 있는 문제나 다른 문제가 발생 하지 않도록 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dd7c7-105">For example, with information barriers, you can restrict communication between specific groups of users to avoid a conflict of interest or other issues.</span></span> <span data-ttu-id="dd7c7-106">정보 장애물을 설정 하는 방법에 대 한 자세한 내용은 [Define information for about about (Preview)](information-barriers-policies.md)을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="dd7c7-106">(To learn more about how to set up information barriers, see [Define policies for information barriers (Preview)](information-barriers-policies.md).)</span></span>

<span data-ttu-id="dd7c7-107">정보 장벽에 따라 예기치 않은 문제가 발생 하는 경우 이러한 문제를 해결 하기 위해 몇 가지 단계를 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dd7c7-107">In the event that people run into unexpected issues after information barriers are in place, there are some steps you can take to resolve those issues.</span></span> <span data-ttu-id="dd7c7-108">이 문서를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="dd7c7-108">Use this article as a guide.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="dd7c7-109">이 문서에서 설명 하는 작업을 수행 하려면 다음 중 하 나와 같은 적절 한 역할을 할당 받아야 합니다.</span><span class="sxs-lookup"><span data-stu-id="dd7c7-109">To perform the tasks described in this article, you must be assigned an appropriate role, such as one of the following:</span></span><br/><span data-ttu-id="dd7c7-110">-Microsoft 365 Enterprise 전역 관리자</span><span class="sxs-lookup"><span data-stu-id="dd7c7-110">- Microsoft 365 Enterprise Global Administrator</span></span><br/><span data-ttu-id="dd7c7-111">-Office 365 전역 관리자</span><span class="sxs-lookup"><span data-stu-id="dd7c7-111">- Office 365 Global Administrator</span></span><br/><span data-ttu-id="dd7c7-112">-준수 관리자</span><span class="sxs-lookup"><span data-stu-id="dd7c7-112">- Compliance Administrator</span></span><br/><span data-ttu-id="dd7c7-113">-IB 준수 관리 (새 역할입니다.)</span><span class="sxs-lookup"><span data-stu-id="dd7c7-113">- IB Compliance Management (this is a new role!)</span></span><p><span data-ttu-id="dd7c7-114">정보 장벽에 대 한 필수 구성 요소에 대 한 자세한 내용은 [필수 구성 요소 (정보 장벽 정책)](information-barriers-policies.md#prerequisites)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="dd7c7-114">To learn more about prerequisites for information barriers, see [Prerequisites (for information barrier policies)](information-barriers-policies.md#prerequisites).</span></span><p><span data-ttu-id="dd7c7-115">[Office 365 Security & 준수 센터 PowerShell에 연결](https://docs.microsoft.com/powershell/exchange/office-365-scc/connect-to-scc-powershell/connect-to-scc-powershell?view=exchange-ps)되어 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="dd7c7-115">Make sure to [connect to Office 365 Security & Compliance Center PowerShell](https://docs.microsoft.com/powershell/exchange/office-365-scc/connect-to-scc-powershell/connect-to-scc-powershell?view=exchange-ps).</span></span>

## <a name="issue-communications-are-allowed-between-users-who-should-be-blocked-in-microsoft-teams"></a><span data-ttu-id="dd7c7-116">문제: Microsoft 팀에서 차단 해야 하는 사용자 간에 통신이 허용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="dd7c7-116">Issue: Communications are allowed between users who should be blocked in Microsoft Teams</span></span>

<span data-ttu-id="dd7c7-117">이 경우 정보 장애물을 정의, 활성 및 적용 하더라도 서로 통신을 차단 해야 하는 사용자는 Microsoft 팀에서 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dd7c7-117">In this case, although information barriers are defined, active, and applied, people who should be prevented from communicating with each other are somehow able to in Microsoft Teams.</span></span>

### <a name="what-to-do"></a><span data-ttu-id="dd7c7-118">수행할 작업</span><span class="sxs-lookup"><span data-stu-id="dd7c7-118">What to do</span></span>

<span data-ttu-id="dd7c7-119">해당 사용자가 정보 장벽 정책에 포함 되어 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="dd7c7-119">Verify that the users in question are included in an information barrier policy.</span></span> 

1. <span data-ttu-id="dd7c7-120">Identity 매개 변수와 함께 **InformationBarrierRecipientStatus** cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="dd7c7-120">Use the **Get-InformationBarrierRecipientStatus** cmdlet with Identity parameters.</span></span>

    <span data-ttu-id="dd7c7-121">구문과`Get-InformationBarrierRecipientStatus -Identity <value> -Identity2 <value>`</span><span class="sxs-lookup"><span data-stu-id="dd7c7-121">Syntax: `Get-InformationBarrierRecipientStatus -Identity <value> -Identity2 <value>`</span></span> 

    <span data-ttu-id="dd7c7-122">이름, 별칭, 고유 이름, 정식 도메인 이름, 전자 메일 주소 또는 GUID와 같은 각 사용자를 고유 하 게 식별 하는 모든 값을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dd7c7-122">You can use any value that uniquely identifies each user, such as name, alias, distinguished name, canonical domain name, email address, or GUID.</span></span> 

    <span data-ttu-id="dd7c7-123">예제: `Get-InformationBarrierRecipientStatus -Identity meganb -Identity2 alexw`</span><span class="sxs-lookup"><span data-stu-id="dd7c7-123">Example: `Get-InformationBarrierRecipientStatus -Identity meganb -Identity2 alexw`</span></span> 

    <span data-ttu-id="dd7c7-124">이 예에서는 Office 365의 두 사용자 계정 ( *Megan*용 *meganb* 및 *Alex*용 *alexw* )을 참조 합니다.</span><span class="sxs-lookup"><span data-stu-id="dd7c7-124">In this example, we refer to two user accounts in Office 365: *meganb* for *Megan*, and *alexw* for *Alex*.</span></span> 
    
    > [!TIP]
    > <span data-ttu-id="dd7c7-125">단일 사용자에 대해이 cmdlet을 사용할 수도 있습니다.`Get-InformationBarrierRecipientStatus -Identity <value>`</span><span class="sxs-lookup"><span data-stu-id="dd7c7-125">You can also use this cmdlet for a single user: `Get-InformationBarrierRecipientStatus -Identity <value>`</span></span>
    
2. <span data-ttu-id="dd7c7-126">발견 된 내용을 검토 합니다.</span><span class="sxs-lookup"><span data-stu-id="dd7c7-126">Review the findings.</span></span> <span data-ttu-id="dd7c7-127">**InformationBarrierRecipientStatus** cmdlet은 특성 값 및 적용 되는 정보 장벽 정책과 같은 사용자에 대 한 정보를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="dd7c7-127">The **Get-InformationBarrierRecipientStatus** cmdlet returns information about users, such as attribute values and any information barrier policies that are applied.</span></span> 

    <span data-ttu-id="dd7c7-128">결과를 검토 하 고 다음 표에 설명 된 대로 다음 단계를 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="dd7c7-128">Review the results, and then take your next steps, as described in the following table:</span></span>
    
    |<span data-ttu-id="dd7c7-129">결과</span><span class="sxs-lookup"><span data-stu-id="dd7c7-129">Results</span></span>  |<span data-ttu-id="dd7c7-130">다음 단계</span><span class="sxs-lookup"><span data-stu-id="dd7c7-130">Next steps</span></span>  |
    |---------|---------|
    |<span data-ttu-id="dd7c7-131">선택한 사용자에 대 한 세그먼트가 나열 되지 않음</span><span class="sxs-lookup"><span data-stu-id="dd7c7-131">No segments are listed for the selected user(s)</span></span>     |<span data-ttu-id="dd7c7-132">다음 중 하나를 수행합니다.</span><span class="sxs-lookup"><span data-stu-id="dd7c7-132">Do one of the following:</span></span><br/><span data-ttu-id="dd7c7-133">-Azure Active Directory에서 사용자 프로필을 편집 하 여 기존 세그먼트에 사용자를 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="dd7c7-133">- Assign users to an existing segment by editing their user profiles in Azure Active Directory.</span></span> <span data-ttu-id="dd7c7-134">( [Office 365 PowerShell을 사용 하 여 사용자 계정 속성 구성](https://docs.microsoft.com/office365/enterprise/powershell/configure-user-account-properties-with-office-365-powershell)참조)</span><span class="sxs-lookup"><span data-stu-id="dd7c7-134">(See [Configure user account properties with Office 365 PowerShell](https://docs.microsoft.com/office365/enterprise/powershell/configure-user-account-properties-with-office-365-powershell).)</span></span><br/><span data-ttu-id="dd7c7-135">- [정보 장벽에 대해 지원 되는 특성](information-barriers-attributes.md)을 사용 하 여 세그먼트를 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="dd7c7-135">- Define a segment using a [supported attribute for information barriers](information-barriers-attributes.md).</span></span> <span data-ttu-id="dd7c7-136">그런 다음 [새 정책을 정의](information-barriers-policies.md#part-2-define-information-barrier-policies) 하거나 [기존 정책을 편집](information-barriers-edit-segments-policies.md.md#edit-a-policy) 하 여 해당 세그먼트를 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="dd7c7-136">Then, either [define a new policy](information-barriers-policies.md#part-2-define-information-barrier-policies) or [edit an existing policy](information-barriers-edit-segments-policies.md.md#edit-a-policy) to include that segment.</span></span>  |
    |<span data-ttu-id="dd7c7-137">세그먼트는 나열 되지만 해당 세그먼트에 정보 장벽 정책이 할당 되지 않음</span><span class="sxs-lookup"><span data-stu-id="dd7c7-137">Segments are listed but no information barrier policies are assigned to those segments</span></span>     |<span data-ttu-id="dd7c7-138">다음 중 하나를 수행합니다.</span><span class="sxs-lookup"><span data-stu-id="dd7c7-138">Do one of the following:</span></span><br/><span data-ttu-id="dd7c7-139">- 문제의 각 세그먼트에 대 한 [새 정보 장벽 정책 정의](information-barriers-policies.md#part-2-define-information-barrier-policies)</span><span class="sxs-lookup"><span data-stu-id="dd7c7-139">- [Define a new information barrier policy](information-barriers-policies.md#part-2-define-information-barrier-policies) for each segment in question</span></span><br/><span data-ttu-id="dd7c7-140">- [기존 정보 장벽 정책을 편집](information-barriers-edit-segments-policies.md.md#edit-a-policy) 하 여 올바른 세그먼트에 할당</span><span class="sxs-lookup"><span data-stu-id="dd7c7-140">- [Edit an existing information barrier policy](information-barriers-edit-segments-policies.md.md#edit-a-policy) to assign it to the correct segment</span></span>         |
    |<span data-ttu-id="dd7c7-141">나열 된 세그먼트는 정보 장벽 정책에 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dd7c7-141">Segments are listed and each is included in an information barrier policy</span></span>     |<span data-ttu-id="dd7c7-142">- `Get-InformationBarrierPolicy` Cmdlet을 실행 하 여 정보 장벽 정책이 활성 상태 인지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="dd7c7-142">- Run the `Get-InformationBarrierPolicy` cmdlet to verify that information barrier policies are active</span></span><br/><span data-ttu-id="dd7c7-143">-정책이 적용 `Get-InformationBarrierPoliciesApplicationStatus` 되었는지 확인 하는 cmdlet을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="dd7c7-143">- Run the `Get-InformationBarrierPoliciesApplicationStatus` cmdlet to confirm the policies are applied</span></span><br/><span data-ttu-id="dd7c7-144">- `Start-InformationBarrierPoliciesApplication` Cmdlet을 실행 하 여 모든 활성 정보 장벽 정책 적용</span><span class="sxs-lookup"><span data-stu-id="dd7c7-144">- Run the `Start-InformationBarrierPoliciesApplication` cmdlet to apply all active information barrier policies</span></span>          |
    

## <a name="issue-people-are-unexpectedly-blocked-from-communicating-in-microsoft-teams"></a><span data-ttu-id="dd7c7-145">문제: 사용자가 Microsoft 팀에서 의견을 교환할 수 없도록 예기치 않게 차단 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="dd7c7-145">Issue: People are unexpectedly blocked from communicating in Microsoft Teams</span></span> 

<span data-ttu-id="dd7c7-146">이 경우 사용자는 Microsoft 팀에서 다른 사용자와 통신 하는 동안 예기치 않은 문제를 보고 하 게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="dd7c7-146">In this case, people are reporting unexpected issues communicating with others in Microsoft Teams.</span></span> <span data-ttu-id="dd7c7-147">예제:</span><span class="sxs-lookup"><span data-stu-id="dd7c7-147">Examples:</span></span>
- <span data-ttu-id="dd7c7-148">사용자가 Microsoft 팀에서 다른 사용자를 찾을 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="dd7c7-148">A user is unable to find another user in Microsoft Teams.</span></span>
- <span data-ttu-id="dd7c7-149">사용자가 Microsoft 팀에서 다른 사용자를 선택할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="dd7c7-149">A user cannot select another user in Microsoft Teams.</span></span>
- <span data-ttu-id="dd7c7-150">사용자가 다른 사용자를 볼 수 있지만 Microsoft 팀에서 다른 사용자에 게 메시지를 보내거나이를 보낼 수는 없습니다.</span><span class="sxs-lookup"><span data-stu-id="dd7c7-150">A user can see another user, but cannot select or send messages to that other user in Microsoft Teams.</span></span>
- <span data-ttu-id="dd7c7-151">사용자는 다른 사용자를 보고 선택할 수 있지만 Microsoft 팀에서 해당 사용자와 통신할 수는 없습니다.</span><span class="sxs-lookup"><span data-stu-id="dd7c7-151">A user can see and select another user, but cannot communicate with that user in Microsoft Teams.</span></span>

### <a name="what-to-do"></a><span data-ttu-id="dd7c7-152">수행할 작업</span><span class="sxs-lookup"><span data-stu-id="dd7c7-152">What to do</span></span>

<span data-ttu-id="dd7c7-153">사용자가 정보 장벽 정책의 영향을 받는지 여부를 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="dd7c7-153">Determine whether the users are affected by an information barrier policy.</span></span>

1. <span data-ttu-id="dd7c7-154">**InformationBarrierRecipientStatus** Cmdlet을 Identity 매개 변수와 함께 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="dd7c7-154">Use the **Get-InformationBarrierRecipientStatus** cmdlet with the Identity parameter.</span></span> 

    <span data-ttu-id="dd7c7-155">구문은`Get-InformationBarrierRecipientStatus -Identity`</span><span class="sxs-lookup"><span data-stu-id="dd7c7-155">The syntax is `Get-InformationBarrierRecipientStatus -Identity`</span></span>

    <span data-ttu-id="dd7c7-156">각 받는 사람을 고유 하 게 식별 하는 모든 id 값 (예: 이름, 별칭, DN (고유 이름), 정식 DN, 전자 메일 주소 또는 GUID)을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dd7c7-156">You can use any identity value that uniquely identifies each recipient, such as Name, Alias, Distinguished name (DN), Canonical DN, Email address, or GUID.</span></span>

    <span data-ttu-id="dd7c7-157">예제: `Get-InformationBarrierRecipientStatus -Identity meganb`</span><span class="sxs-lookup"><span data-stu-id="dd7c7-157">Example: `Get-InformationBarrierRecipientStatus -Identity meganb`</span></span>

    <span data-ttu-id="dd7c7-158">이 예제에서는 Identity 매개 변수에 별칭 (*meganb*)을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="dd7c7-158">In this example, we are using an alias (*meganb*) for the Identity parameter.</span></span> <span data-ttu-id="dd7c7-159">이 cmdlet은 사용자가 정보 장벽 정책의 영향을 받는지 여부를 나타내는 정보를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="dd7c7-159">This cmdlet will return information that indicates whether the user is affected by an information barrier policy.</span></span> <span data-ttu-id="dd7c7-160">(\* ExoPolicyId: \<GUID>를 찾아보십시오.)</span><span class="sxs-lookup"><span data-stu-id="dd7c7-160">(Look for \*ExoPolicyId: \<GUID>.)</span></span>

    <span data-ttu-id="dd7c7-161">사용자가 정보 장벽 정책에 포함 되어 있지 않은 경우 지원 서비스에 문의 하세요.</span><span class="sxs-lookup"><span data-stu-id="dd7c7-161">If the users are not included in information barrier policies, contact support.</span></span> <span data-ttu-id="dd7c7-162">그렇지 않으면 다음 단계를 진행 합니다.</span><span class="sxs-lookup"><span data-stu-id="dd7c7-162">Otherwise, proceed to the next step.</span></span>

2. <span data-ttu-id="dd7c7-163">정보 장벽 정책에 포함 된 세그먼트를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="dd7c7-163">Find out which segments are included in an information barrier policy.</span></span> <span data-ttu-id="dd7c7-164">이 작업을 수행 하려면 Identity `Get-InformationBarrierPolicy` 매개 변수와 함께 cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="dd7c7-164">To do this, use the `Get-InformationBarrierPolicy` cmdlet with the Identity parameter.</span></span> <span data-ttu-id="dd7c7-165">이전 단계에서 받은 정책 GUID (ExoPolicyId)와 같은 세부 정보를 id 값으로 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="dd7c7-165">Use details, such as the policy GUID (ExoPolicyId) you received during the previous step, as an identity value.</span></span>

    <span data-ttu-id="dd7c7-166">예제: `Get-InformationBarrierPolicy -Identity b42c3d0f-49e9-4506-a0a5-bf2853b5df6f`</span><span class="sxs-lookup"><span data-stu-id="dd7c7-166">Example: `Get-InformationBarrierPolicy -Identity b42c3d0f-49e9-4506-a0a5-bf2853b5df6f`</span></span>

    <span data-ttu-id="dd7c7-167">이 예에서는 ExoPolicyId *b42c3d0f-49e9-4506-a0a5-bf2853b5df6f*가 있는 정보 장벽 정책에 대 한 자세한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="dd7c7-167">In this example, we are getting detailed information about the information barrier policy that has ExoPolicyId *b42c3d0f-49e9-4506-a0a5-bf2853b5df6f*.</span></span>
    
    <span data-ttu-id="dd7c7-168">Cmdlet을 실행 한 후 결과에서 **AssignedSegment**, **SegmentsAllowed**및 **SegmentsBlocked** 값을 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="dd7c7-168">After you run the cmdlet, in the results, look for **AssignedSegment**, **SegmentsAllowed**, and **SegmentsBlocked** values.</span></span>

    <span data-ttu-id="dd7c7-169">예: `Get-InformationBarrierPolicy` cmdlet을 실행 한 후 결과 목록에서 다음을 살펴보았습니다.</span><span class="sxs-lookup"><span data-stu-id="dd7c7-169">Example: After running the `Get-InformationBarrierPolicy` cmdlet, we saw the following in our list of results:</span></span>

    ```powershell
        AssignedSegment      : Sales
        SegmentsAllowed      : {}
        SegmentsBlocked      : {Research}
    ```
    <span data-ttu-id="dd7c7-170">이 경우 정보 장벽 정책이 Sales 및 Research 세그먼트에 있는 사용자에 게 영향을 줄 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dd7c7-170">In this case, we can see that an information barrier policy affects people who are in the Sales and Research segments.</span></span> <span data-ttu-id="dd7c7-171">이 경우에는 영업 직원이 조사 담당자와 의견을 교환할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="dd7c7-171">In this case, people in Sales are prevented from communicating with people in Research.</span></span> <span data-ttu-id="dd7c7-172">이 문제가 올바른 것 같으면 정보 장애가 예상 대로 작동 하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="dd7c7-172">If this seems correct, then information barriers are working as expected.</span></span> <span data-ttu-id="dd7c7-173">그렇지 않으면 다음 단계를 진행 합니다.</span><span class="sxs-lookup"><span data-stu-id="dd7c7-173">If not, proceed to the next step.</span></span>

4. <span data-ttu-id="dd7c7-174">세그먼트가 올바르게 정의 되었는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="dd7c7-174">Make sure your segments are defined correctly.</span></span> <span data-ttu-id="dd7c7-175">이 작업을 수행 하려면 `Get-OrganizationSegment` cmdlet을 사용 하 여 결과 목록을 검토 합니다.</span><span class="sxs-lookup"><span data-stu-id="dd7c7-175">To do this, use the `Get-OrganizationSegment` cmdlet, and review the list of results.</span></span> 

    <span data-ttu-id="dd7c7-176">특정 세그먼트에 대 한 세부 정보를 보려면 Identity `Get-OrganizationSegment` 매개 변수와 함께 cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="dd7c7-176">To view details for a specific segment, use the `Get-OrganizationSegment` cmdlet with an Identity parameter.</span></span> 

    <span data-ttu-id="dd7c7-177">예제: `Get-OrganizationSegment -Identity c96e0837-c232-4a8a-841e-ef45787d8fcd`</span><span class="sxs-lookup"><span data-stu-id="dd7c7-177">Example: `Get-OrganizationSegment -Identity c96e0837-c232-4a8a-841e-ef45787d8fcd`</span></span>

    <span data-ttu-id="dd7c7-178">이 예에서는 GUID *c96e0837-c232-4a8a-841e-ef45787d8fcd*가 있는 세그먼트에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="dd7c7-178">In this example, we are getting information about the segment that has GUID *c96e0837-c232-4a8a-841e-ef45787d8fcd*.</span></span>

    <span data-ttu-id="dd7c7-179">해당 세그먼트에 대 한 세부 정보를 검토 합니다.</span><span class="sxs-lookup"><span data-stu-id="dd7c7-179">Review the details for the segment.</span></span> <span data-ttu-id="dd7c7-180">필요한 경우 [세그먼트를 편집](information-barriers-edit-segments-policies.md.md#edit-a-segment)하 고 `Start-InformationBarrierPoliciesApplication` cmdlet을 다시 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="dd7c7-180">If necessary, [edit a segment](information-barriers-edit-segments-policies.md.md#edit-a-segment), and then re-use the `Start-InformationBarrierPoliciesApplication` cmdlet.</span></span>

    <span data-ttu-id="dd7c7-181">정보 장벽 정책에 여전히 문제가 있는 경우 고객 지원에 문의 하세요.</span><span class="sxs-lookup"><span data-stu-id="dd7c7-181">If you are still having issues with your information barrier policy, contact support.</span></span>
    
## <a name="issue-the-information-barrier-application-process-is-taking-too-long"></a><span data-ttu-id="dd7c7-182">문제: 정보 장벽 응용 프로그램 프로세스가 너무 오래 걸립니다.</span><span class="sxs-lookup"><span data-stu-id="dd7c7-182">Issue: The information barrier application process is taking too long</span></span>

<span data-ttu-id="dd7c7-183">**InformationBarrierPoliciesApplication** cmdlet을 실행 한 후 프로세스를 완료 하는 데 시간이 너무 오래 걸립니다.</span><span class="sxs-lookup"><span data-stu-id="dd7c7-183">After running the **Start-InformationBarrierPoliciesApplication** cmdlet, the process is taking a really long time to finish.</span></span>

### <a name="what-to-do"></a><span data-ttu-id="dd7c7-184">수행할 작업</span><span class="sxs-lookup"><span data-stu-id="dd7c7-184">What to do</span></span>

<span data-ttu-id="dd7c7-185">정책 응용 프로그램 cmdlet을 실행 하는 경우 조직의 모든 계정에 대 한 정보 장벽 정책이 사용자에 의해 적용 되거나 제거 됩니다.</span><span class="sxs-lookup"><span data-stu-id="dd7c7-185">Keep in mind that when you run the policy application cmdlet, information barrier policies are being applied (or removed), user by user, for all accounts in your organization.</span></span> <span data-ttu-id="dd7c7-186">사용자 수가 많은 경우 처리 하는 데 시간이 오래 걸릴 것입니다.</span><span class="sxs-lookup"><span data-stu-id="dd7c7-186">If you have a lot of users, it will take a while to process.</span></span> <span data-ttu-id="dd7c7-187">일반적으로 5000 사용자 계정을 처리 하는 데 한 시간 정도 소요 됩니다.</span><span class="sxs-lookup"><span data-stu-id="dd7c7-187">(As a general guideline, it takes about an hour to process 5,000 user accounts.)</span></span>

1. <span data-ttu-id="dd7c7-188">**InformationBarrierPoliciesApplicationStatus** cmdlet을 사용 하 여 가장 최근 정책 응용 프로그램의 상태를 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dd7c7-188">Use the **Get-InformationBarrierPoliciesApplicationStatus** cmdlet to verify status of the most recent policy application.</span></span>

    <span data-ttu-id="dd7c7-189">구문과`Get-InformationBarrierPoliciesApplicationStatus`</span><span class="sxs-lookup"><span data-stu-id="dd7c7-189">Syntax: `Get-InformationBarrierPoliciesApplicationStatus`</span></span>

    <span data-ttu-id="dd7c7-190">( *모든* 정보 장벽 정책 응용 프로그램에 대 한 상태를 표시 하려면 다음 cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="dd7c7-190">(To display status for *all* information barrier policy applications, use this cmdlet:</span></span><br/>
    <span data-ttu-id="dd7c7-191">`Get-InformationBarrierPoliciesApplicationStatus -All $true`)</span><span class="sxs-lookup"><span data-stu-id="dd7c7-191"></span></span>

    <span data-ttu-id="dd7c7-192">이렇게 하면 정책 응용 프로그램을 완료, 실패 또는 진행 중인지 여부에 대 한 정보가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="dd7c7-192">This will display information about whether policy application completed, failed, or is in progress..</span></span>

2. <span data-ttu-id="dd7c7-193">이전 단계의 결과에 따라 다음 단계 중 하나를 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="dd7c7-193">Depending on the results of the previous step, take one of the following steps:</span></span>
  
    |<span data-ttu-id="dd7c7-194">상태</span><span class="sxs-lookup"><span data-stu-id="dd7c7-194">Status</span></span>  |<span data-ttu-id="dd7c7-195">다음 단계</span><span class="sxs-lookup"><span data-stu-id="dd7c7-195">Next step</span></span>  |
    |---------|---------|
    |<span data-ttu-id="dd7c7-196">**시작 되지 않음**</span><span class="sxs-lookup"><span data-stu-id="dd7c7-196">**Not started**</span></span>     |<span data-ttu-id="dd7c7-197">**InformationBarrierPoliciesApplication** cmdlet을 실행 한 후 45 분이 경과 하면 감사 로그를 검토 하 여 정책 정의에 오류가 있는지 또는 응용 프로그램이 시작 되지 않은 다른 이유가 있는지를 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="dd7c7-197">If it has been more than 45 minutes since the **Start-InformationBarrierPoliciesApplication** cmdlet has been run, review your audit log to see if there are any errors in policy definitions, or some other reason why the application has not started.</span></span> |
    |<span data-ttu-id="dd7c7-198">**실패**</span><span class="sxs-lookup"><span data-stu-id="dd7c7-198">**Failed**</span></span>     |<span data-ttu-id="dd7c7-199">응용 프로그램이 실패 한 경우 감사 로그를 검토 합니다.</span><span class="sxs-lookup"><span data-stu-id="dd7c7-199">If the application has failed, review your audit log.</span></span> <span data-ttu-id="dd7c7-200">또한 세그먼트 및 정책도 검토 합니다.</span><span class="sxs-lookup"><span data-stu-id="dd7c7-200">Also review your segments and policies.</span></span> <span data-ttu-id="dd7c7-201">두 개 이상의 세그먼트에 할당 된 사용자가 있나요?</span><span class="sxs-lookup"><span data-stu-id="dd7c7-201">Are any users assigned to more than one segment?</span></span> <span data-ttu-id="dd7c7-202">모든 세그먼트에 두 개 이상의 poliicy이 할당 됩니까?</span><span class="sxs-lookup"><span data-stu-id="dd7c7-202">Are any segments assigned more than one poliicy?</span></span> <span data-ttu-id="dd7c7-203">필요한 경우 세그먼트 및/또는 [편집 정책을](information-barriers-edit-segments-policies.md.md#edit-a-policy) [편집](information-barriers-edit-segments-policies.md.md#edit-a-segment) 하 고 **InformationBarrierPoliciesApplication** cmdlet을 다시 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="dd7c7-203">If necessary, [edit segments](information-barriers-edit-segments-policies.md.md#edit-a-segment) and/or [edit policies](information-barriers-edit-segments-policies.md.md#edit-a-policy), and then run the **Start-InformationBarrierPoliciesApplication** cmdlet again.</span></span>  |
    |<span data-ttu-id="dd7c7-204">**진행 중**</span><span class="sxs-lookup"><span data-stu-id="dd7c7-204">**In progress**</span></span>     |<span data-ttu-id="dd7c7-205">응용 프로그램이 계속 진행 되 고 있는 경우 완료 하는 데 더 많은 시간이 걸릴 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dd7c7-205">If the application is still in progress, allow more time for it to complete.</span></span> <span data-ttu-id="dd7c7-206">기간이 며칠 이면 감사 로그를 수집한 다음 고객 지원에 문의 하세요.</span><span class="sxs-lookup"><span data-stu-id="dd7c7-206">If it has been several days, gather your audit logs, and then contact support.</span></span> |

## <a name="related-topics"></a><span data-ttu-id="dd7c7-207">관련 항목</span><span class="sxs-lookup"><span data-stu-id="dd7c7-207">Related topics</span></span>

[<span data-ttu-id="dd7c7-208">Microsoft 팀의 정보 장벽에 대 한 정책 정의 (미리 보기)</span><span class="sxs-lookup"><span data-stu-id="dd7c7-208">Define policies for information barriers in Microsoft Teams (Preview)</span></span>](information-barriers-policies.md)

[<span data-ttu-id="dd7c7-209">정보 장벽 (미리 보기)</span><span class="sxs-lookup"><span data-stu-id="dd7c7-209">Information barriers (Preview)</span></span>](information-barriers.md)



