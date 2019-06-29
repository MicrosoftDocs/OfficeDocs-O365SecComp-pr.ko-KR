---
title: 정보 장벽 정책의 특성
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
description: 이 문서를 정보 장벽 정책에서 사용할 수 있는 다양 한 특성에 대 한 참조로 사용 합니다.
ms.openlocfilehash: 896b87a3ccc696d3a8193e37237fe555d326ca52
ms.sourcegitcommit: 011bfa60cafdf47900aadf96a17eb275efa877c4
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/29/2019
ms.locfileid: "35394313"
---
# <a name="attributes-for-information-barrier-policies-preview"></a><span data-ttu-id="cbee5-103">정보 장벽 정책의 특성 (미리 보기)</span><span class="sxs-lookup"><span data-stu-id="cbee5-103">Attributes for information barrier policies (Preview)</span></span>

<span data-ttu-id="cbee5-104">Azure Active Directory의 특정 특성을 사용 하 여 사용자를 분할할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cbee5-104">Certain attributes in Azure Active Directory can be used to segment users.</span></span> <span data-ttu-id="cbee5-105">세그먼트를 정의한 후에는 이러한 세그먼트를 정보 장벽 정책의 필터로 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cbee5-105">Once segments are defined, those segments can be used as filters for information barrier policies.</span></span> <span data-ttu-id="cbee5-106">예를 들어 **부서** 를 사용 하 여 조직 내 부서별로 사용자 세그먼트를 정의할 수 있습니다 (두 부서가 동시에 단일 직원이 작동 하지 않는다고 가정).</span><span class="sxs-lookup"><span data-stu-id="cbee5-106">For example, you might use **Department** to define segments of users by department within your organization (assuming no single employee works for two departments at the same time).</span></span> 

<span data-ttu-id="cbee5-107">이 문서에서는 정보 장벽에서 특성을 사용 하는 방법에 대해 설명 하 고 사용할 수 있는 특성 목록을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="cbee5-107">This article describes how to use attributes with information barriers, and it provides a list of attributes that can be used.</span></span> <span data-ttu-id="cbee5-108">정보 장벽에 대 한 자세한 내용은 다음 리소스를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="cbee5-108">To learn more about information barriers, see the following resources:</span></span>
- [<span data-ttu-id="cbee5-109">정보 장벽 (미리 보기)</span><span class="sxs-lookup"><span data-stu-id="cbee5-109">Information barriers (Preview)</span></span>](information-barriers.md)
- [<span data-ttu-id="cbee5-110">Microsoft 팀의 정보 장벽에 대 한 정책 정의 (미리 보기)</span><span class="sxs-lookup"><span data-stu-id="cbee5-110">Define policies for information barriers in Microsoft Teams (Preview)</span></span>](information-barriers-policies.md)
- [<span data-ttu-id="cbee5-111">정보 장벽 정책 편집 (또는 제거) (미리 보기)</span><span class="sxs-lookup"><span data-stu-id="cbee5-111">Edit (or remove) information barrier policies (Preview)</span></span>](information-barriers-edit-segments-policies.md.md)

## <a name="how-to-use-attributes-in-information-barrier-policies"></a><span data-ttu-id="cbee5-112">정보 장벽 정책에서 특성을 사용 하는 방법</span><span class="sxs-lookup"><span data-stu-id="cbee5-112">How to use attributes in information barrier policies</span></span>

<span data-ttu-id="cbee5-113">이 문서에 나와 있는 특성을 사용 하 여 사용자의 세그먼트를 정의 하거나 편집할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cbee5-113">The attributes listed in this article can be used to define or edit segments of users.</span></span> <span data-ttu-id="cbee5-114">정의 된 세그먼트는 [정보 장벽 정책](information-barriers-policies.md)에서 매개 변수 ( *usergroupfilter* 값 이라고 함)로 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="cbee5-114">Your defined segments serve as parameters (called *UserGroupFilter* values) in [information barrier policies](information-barriers-policies.md).</span></span>

1. <span data-ttu-id="cbee5-115">세그먼트를 정의 하는 데 사용할 특성을 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cbee5-115">Determine which attribute you want to use to define segments.</span></span> <span data-ttu-id="cbee5-116">(이 문서의 [참조](#reference) 섹션 참조)</span><span class="sxs-lookup"><span data-stu-id="cbee5-116">(See the [Reference](#reference) section in this article.)</span></span>

2. <span data-ttu-id="cbee5-117">사용자 계정에 1 단계에서 선택한 특성에 대 한 값이 입력 되어 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="cbee5-117">Make sure the user accounts have values filled in for the attribute(s) you selected in Step 1.</span></span> <span data-ttu-id="cbee5-118">사용자 계정 정보를 확인 하 고 필요한 경우 특성 값을 포함 하도록 사용자 계정을 편집 합니다.</span><span class="sxs-lookup"><span data-stu-id="cbee5-118">View user account details, and if necessary, edit user accounts to include attribute values.</span></span> 

    <span data-ttu-id="cbee5-119">PowerShell을 사용 하 여이 작업을 수행 하려면 [Configure user account properties With Office 365 PowerShell](https://docs.microsoft.com/office365/enterprise/powershell/configure-user-account-properties-with-office-365-powershell)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="cbee5-119">To do this using PowerShell, see [Configure user account properties with Office 365 PowerShell](https://docs.microsoft.com/office365/enterprise/powershell/configure-user-account-properties-with-office-365-powershell).</span></span>

    <span data-ttu-id="cbee5-120">Azure Active Directory에서이 작업을 수행 하려면 [Azure Active directory를 사용 하 여 사용자 프로필 정보 추가 또는 업데이트](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-users-profile-azure-portal)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="cbee5-120">To do this in Azure Active Directory, see [Add or update a user's profile information using Azure Active Directory](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-users-profile-azure-portal).</span></span>

3. <span data-ttu-id="cbee5-121">다음 예와 같이 [PowerShell을 사용 하 여 세그먼트를 정의](information-barriers-policies.md#define-segments-using-powershell)합니다.</span><span class="sxs-lookup"><span data-stu-id="cbee5-121">[Define segments using PowerShell](information-barriers-policies.md#define-segments-using-powershell), similar to the following examples:</span></span>

    |<span data-ttu-id="cbee5-122">예제</span><span class="sxs-lookup"><span data-stu-id="cbee5-122">Example</span></span>  |<span data-ttu-id="cbee5-123">#A0</span><span class="sxs-lookup"><span data-stu-id="cbee5-123">Cmdlet</span></span>  |
    |---------|---------|
    |<span data-ttu-id="cbee5-124">부서 특성을 사용 하 여 Segment1 라는 세그먼트를 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="cbee5-124">Define a segment called Segment1 using the Department attribute</span></span>     | `New-OrganizationSegment -Name "Segment1" -UserGroupFilter "Department -eq 'Department1'"`        |
    |<span data-ttu-id="cbee5-125">MemberOf 특성을 사용 하 여 SegmentA 이라는 세그먼트를 정의 합니다 (이 특성에 그룹 이름 (예: "BlueGroup")이 포함 되어 있다고 가정).</span><span class="sxs-lookup"><span data-stu-id="cbee5-125">Define a segment called SegmentA using the MemberOf attribute (suppose this attribute contains group names, such as "BlueGroup")</span></span>     | `New-OrganizationSegment -Name "SegmentA" -UserGroupFilter "MemberOf -eq 'BlueGroup'"`        |
    |<span data-ttu-id="cbee5-126">ExtensionAttribute1을 사용 하 여 DayTraders 라는 세그먼트를 정의 합니다 (이 특성에 직함 (예: "Daytraders")이 포함 되어 있다고 가정 합니다.)</span><span class="sxs-lookup"><span data-stu-id="cbee5-126">Define a segment called DayTraders using ExtensionAttribute1 (suppose this attribute contains job titles, such as "DayTrader")</span></span>|`New-OrganizationSegment -Name "DayTraders" -UserGroupFilter "ExtensionAttribute1 -eq 'DayTrader'"` |

    > [!TIP]
    > <span data-ttu-id="cbee5-127">세그먼트를 정의할 때 모든 세그먼트에 같은 특성을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="cbee5-127">When you define segments, use the same attribute for all your segments.</span></span> <span data-ttu-id="cbee5-128">예를 들어 *부서*를 사용 하 여 일부 세그먼트를 정의 하는 경우에는 *부서*를 사용 하 여 모든 세그먼트를 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="cbee5-128">For example, if you define some segments using *Department*, define all of the segments using *Department*.</span></span> <span data-ttu-id="cbee5-129">*부서* 및 다른 사용자는 *MemberOf*를 사용 하 여 일부 세그먼트를 정의 하지 마세요.</span><span class="sxs-lookup"><span data-stu-id="cbee5-129">Don't define some segments using *Department* and others using *MemberOf*.</span></span> <span data-ttu-id="cbee5-130">세그먼트가 겹치지 않는지 확인 합니다. 각 사용자는 정확히 하나의 세그먼트에 할당 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="cbee5-130">Make sure your segments do not overlap; each user should be assigned to exactly one segment.</span></span> 

## <a name="reference"></a><span data-ttu-id="cbee5-131">참조</span><span class="sxs-lookup"><span data-stu-id="cbee5-131">Reference</span></span>

<span data-ttu-id="cbee5-132">다음 표에는 정보 장벽에 사용할 수 있는 특성이 나와 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cbee5-132">The following table lists the attributes that you can use with information barriers.</span></span>

|<span data-ttu-id="cbee5-133">Azure Active Directory 속성 이름 (LDAP 표시 이름)</span><span class="sxs-lookup"><span data-stu-id="cbee5-133">Azure Active Directory property name (LDAP display name)</span></span>  |<span data-ttu-id="cbee5-134">Exchange 속성 이름</span><span class="sxs-lookup"><span data-stu-id="cbee5-134">Exchange property name</span></span>  |
|---------|---------|
|<span data-ttu-id="cbee5-135">Co</span><span class="sxs-lookup"><span data-stu-id="cbee5-135">Co</span></span>       | <span data-ttu-id="cbee5-136">Co</span><span class="sxs-lookup"><span data-stu-id="cbee5-136">Co</span></span>        |
|<span data-ttu-id="cbee5-137">Company</span><span class="sxs-lookup"><span data-stu-id="cbee5-137">Company</span></span>     |<span data-ttu-id="cbee5-138">Company</span><span class="sxs-lookup"><span data-stu-id="cbee5-138">Company</span></span>         |
|<span data-ttu-id="cbee5-139">부서</span><span class="sxs-lookup"><span data-stu-id="cbee5-139">Department</span></span>     |<span data-ttu-id="cbee5-140">부서</span><span class="sxs-lookup"><span data-stu-id="cbee5-140">Department</span></span>         |
|<span data-ttu-id="cbee5-141">ExtensionAttribute1</span><span class="sxs-lookup"><span data-stu-id="cbee5-141">ExtensionAttribute1</span></span> |<span data-ttu-id="cbee5-142">CustomAttribute1</span><span class="sxs-lookup"><span data-stu-id="cbee5-142">CustomAttribute1</span></span>  |
|<span data-ttu-id="cbee5-143">ExtensionAttribute2</span><span class="sxs-lookup"><span data-stu-id="cbee5-143">ExtensionAttribute2</span></span> |<span data-ttu-id="cbee5-144">CustomAttribute2</span><span class="sxs-lookup"><span data-stu-id="cbee5-144">CustomAttribute2</span></span>  |
|<span data-ttu-id="cbee5-145">ExtensionAttribute3</span><span class="sxs-lookup"><span data-stu-id="cbee5-145">ExtensionAttribute3</span></span> |<span data-ttu-id="cbee5-146">CustomAttribute3</span><span class="sxs-lookup"><span data-stu-id="cbee5-146">CustomAttribute3</span></span>  |
|<span data-ttu-id="cbee5-147">ExtensionAttribute4</span><span class="sxs-lookup"><span data-stu-id="cbee5-147">ExtensionAttribute4</span></span> |<span data-ttu-id="cbee5-148">CustomAttribute4</span><span class="sxs-lookup"><span data-stu-id="cbee5-148">CustomAttribute4</span></span>  |
|<span data-ttu-id="cbee5-149">ExtensionAttribute5</span><span class="sxs-lookup"><span data-stu-id="cbee5-149">ExtensionAttribute5</span></span> |<span data-ttu-id="cbee5-150">CustomAttribute5</span><span class="sxs-lookup"><span data-stu-id="cbee5-150">CustomAttribute5</span></span>  |
|<span data-ttu-id="cbee5-151">ExtensionAttribute6</span><span class="sxs-lookup"><span data-stu-id="cbee5-151">ExtensionAttribute6</span></span> |<span data-ttu-id="cbee5-152">CustomAttribute6</span><span class="sxs-lookup"><span data-stu-id="cbee5-152">CustomAttribute6</span></span>  |
|<span data-ttu-id="cbee5-153">ExtensionAttribute7</span><span class="sxs-lookup"><span data-stu-id="cbee5-153">ExtensionAttribute7</span></span> |<span data-ttu-id="cbee5-154">CustomAttribute7</span><span class="sxs-lookup"><span data-stu-id="cbee5-154">CustomAttribute7</span></span>  |
|<span data-ttu-id="cbee5-155">ExtensionAttribute8</span><span class="sxs-lookup"><span data-stu-id="cbee5-155">ExtensionAttribute8</span></span> |<span data-ttu-id="cbee5-156">CustomAttribute8</span><span class="sxs-lookup"><span data-stu-id="cbee5-156">CustomAttribute8</span></span>  |
|<span data-ttu-id="cbee5-157">ExtensionAttribute9</span><span class="sxs-lookup"><span data-stu-id="cbee5-157">ExtensionAttribute9</span></span> |<span data-ttu-id="cbee5-158">CustomAttribute9</span><span class="sxs-lookup"><span data-stu-id="cbee5-158">CustomAttribute9</span></span>  |
|<span data-ttu-id="cbee5-159">ExtensionAttribute10</span><span class="sxs-lookup"><span data-stu-id="cbee5-159">ExtensionAttribute10</span></span> |<span data-ttu-id="cbee5-160">CustomAttribute10</span><span class="sxs-lookup"><span data-stu-id="cbee5-160">CustomAttribute10</span></span>  |
|<span data-ttu-id="cbee5-161">ExtensionAttribute11</span><span class="sxs-lookup"><span data-stu-id="cbee5-161">ExtensionAttribute11</span></span> |<span data-ttu-id="cbee5-162">CustomAttribute11</span><span class="sxs-lookup"><span data-stu-id="cbee5-162">CustomAttribute11</span></span>  |
|<span data-ttu-id="cbee5-163">ExtensionAttribute12</span><span class="sxs-lookup"><span data-stu-id="cbee5-163">ExtensionAttribute12</span></span> |<span data-ttu-id="cbee5-164">CustomAttribute12</span><span class="sxs-lookup"><span data-stu-id="cbee5-164">CustomAttribute12</span></span>  |
|<span data-ttu-id="cbee5-165">ExtensionAttribute13</span><span class="sxs-lookup"><span data-stu-id="cbee5-165">ExtensionAttribute13</span></span> |<span data-ttu-id="cbee5-166">CustomAttribute13</span><span class="sxs-lookup"><span data-stu-id="cbee5-166">CustomAttribute13</span></span>  |
|<span data-ttu-id="cbee5-167">ExtensionAttribute14</span><span class="sxs-lookup"><span data-stu-id="cbee5-167">ExtensionAttribute14</span></span> |<span data-ttu-id="cbee5-168">CustomAttribute14</span><span class="sxs-lookup"><span data-stu-id="cbee5-168">CustomAttribute14</span></span>  |
|<span data-ttu-id="cbee5-169">ExtensionAttribute15</span><span class="sxs-lookup"><span data-stu-id="cbee5-169">ExtensionAttribute15</span></span> |<span data-ttu-id="cbee5-170">CustomAttribute15</span><span class="sxs-lookup"><span data-stu-id="cbee5-170">CustomAttribute15</span></span>  |
|<span data-ttu-id="cbee5-171">MSExchExtensionCustomAttribute1</span><span class="sxs-lookup"><span data-stu-id="cbee5-171">MSExchExtensionCustomAttribute1</span></span> |<span data-ttu-id="cbee5-172">ExtensionCustomAttribute1</span><span class="sxs-lookup"><span data-stu-id="cbee5-172">ExtensionCustomAttribute1</span></span> |
|<span data-ttu-id="cbee5-173">MSExchExtensionCustomAttribute2</span><span class="sxs-lookup"><span data-stu-id="cbee5-173">MSExchExtensionCustomAttribute2</span></span> |<span data-ttu-id="cbee5-174">ExtensionCustomAttribute2</span><span class="sxs-lookup"><span data-stu-id="cbee5-174">ExtensionCustomAttribute2</span></span> |
|<span data-ttu-id="cbee5-175">MSExchExtensionCustomAttribute3</span><span class="sxs-lookup"><span data-stu-id="cbee5-175">MSExchExtensionCustomAttribute3</span></span> |<span data-ttu-id="cbee5-176">ExtensionCustomAttribute3</span><span class="sxs-lookup"><span data-stu-id="cbee5-176">ExtensionCustomAttribute3</span></span> |
|<span data-ttu-id="cbee5-177">MSExchExtensionCustomAttribute4</span><span class="sxs-lookup"><span data-stu-id="cbee5-177">MSExchExtensionCustomAttribute4</span></span> |<span data-ttu-id="cbee5-178">ExtensionCustomAttribute4</span><span class="sxs-lookup"><span data-stu-id="cbee5-178">ExtensionCustomAttribute4</span></span> |
|<span data-ttu-id="cbee5-179">MSExchExtensionCustomAttribute5</span><span class="sxs-lookup"><span data-stu-id="cbee5-179">MSExchExtensionCustomAttribute5</span></span> |<span data-ttu-id="cbee5-180">ExtensionCustomAttribute5</span><span class="sxs-lookup"><span data-stu-id="cbee5-180">ExtensionCustomAttribute5</span></span> |
|<span data-ttu-id="cbee5-181">MailNickname</span><span class="sxs-lookup"><span data-stu-id="cbee5-181">MailNickname</span></span> |<span data-ttu-id="cbee5-182">별칭</span><span class="sxs-lookup"><span data-stu-id="cbee5-182">Alias</span></span> |
|<span data-ttu-id="cbee5-183">PhysicalDeliveryOfficeName</span><span class="sxs-lookup"><span data-stu-id="cbee5-183">PhysicalDeliveryOfficeName</span></span> |<span data-ttu-id="cbee5-184">Office</span><span class="sxs-lookup"><span data-stu-id="cbee5-184">Office</span></span> |
|<span data-ttu-id="cbee5-185">PostalCode</span><span class="sxs-lookup"><span data-stu-id="cbee5-185">PostalCode</span></span> |<span data-ttu-id="cbee5-186">PostalCode</span><span class="sxs-lookup"><span data-stu-id="cbee5-186">PostalCode</span></span> |
|<span data-ttu-id="cbee5-187">ProxyAddresses</span><span class="sxs-lookup"><span data-stu-id="cbee5-187">ProxyAddresses</span></span> |<span data-ttu-id="cbee5-188">EmailAddresses</span><span class="sxs-lookup"><span data-stu-id="cbee5-188">EmailAddresses</span></span> |
|<span data-ttu-id="cbee5-189">StreetAddress</span><span class="sxs-lookup"><span data-stu-id="cbee5-189">StreetAddress</span></span> |<span data-ttu-id="cbee5-190">StreetAddress</span><span class="sxs-lookup"><span data-stu-id="cbee5-190">StreetAddress</span></span> |
|<span data-ttu-id="cbee5-191">TargetAddress</span><span class="sxs-lookup"><span data-stu-id="cbee5-191">TargetAddress</span></span> |<span data-ttu-id="cbee5-192">ExternalEmailAddress</span><span class="sxs-lookup"><span data-stu-id="cbee5-192">ExternalEmailAddress</span></span> |
|<span data-ttu-id="cbee5-193">UsageLocation</span><span class="sxs-lookup"><span data-stu-id="cbee5-193">UsageLocation</span></span> |<span data-ttu-id="cbee5-194">UsageLocation</span><span class="sxs-lookup"><span data-stu-id="cbee5-194">UsageLocation</span></span> |
|<span data-ttu-id="cbee5-195">UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="cbee5-195">UserPrincipalName</span></span>  |<span data-ttu-id="cbee5-196">UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="cbee5-196">UserPrincipalName</span></span>  |
|<span data-ttu-id="cbee5-197">메일로</span><span class="sxs-lookup"><span data-stu-id="cbee5-197">Mail</span></span>   |<span data-ttu-id="cbee5-198">WindowsEmailAddress</span><span class="sxs-lookup"><span data-stu-id="cbee5-198">WindowsEmailAddress</span></span>    |
|<span data-ttu-id="cbee5-199">설명</span><span class="sxs-lookup"><span data-stu-id="cbee5-199">Description</span></span>    |<span data-ttu-id="cbee5-200">설명</span><span class="sxs-lookup"><span data-stu-id="cbee5-200">Description</span></span>    |
|<span data-ttu-id="cbee5-201">소속</span><span class="sxs-lookup"><span data-stu-id="cbee5-201">MemberOf</span></span>   |<span data-ttu-id="cbee5-202">MemberOfGroup</span><span class="sxs-lookup"><span data-stu-id="cbee5-202">MemberOfGroup</span></span>  |

## <a name="related-topics"></a><span data-ttu-id="cbee5-203">관련 항목</span><span class="sxs-lookup"><span data-stu-id="cbee5-203">Related topics</span></span>

[<span data-ttu-id="cbee5-204">Microsoft 팀의 정보 장벽에 대 한 정책 정의 (미리 보기)</span><span class="sxs-lookup"><span data-stu-id="cbee5-204">Define policies for information barriers in Microsoft Teams (Preview)</span></span>](information-barriers-policies.md)

[<span data-ttu-id="cbee5-205">정보 장벽 문제 해결 (미리 보기)</span><span class="sxs-lookup"><span data-stu-id="cbee5-205">Troubleshooting information barriers (Preview)</span></span>](information-barriers-troubleshooting.md)

[<span data-ttu-id="cbee5-206">정보 장벽 (미리 보기)</span><span class="sxs-lookup"><span data-stu-id="cbee5-206">Information barriers (Preview)</span></span>](information-barriers.md)



