---
title: 정보 장벽 정책의 특성
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 05/31/2019
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.collection:
- M365-security-compliance
localization_priority: None
description: 이 문서를 정보 장벽 정책에서 사용할 수 있는 다양 한 특성에 대 한 참조로 사용 합니다.
ms.openlocfilehash: e72e37950442974897de479c7c11f0053a578d1c
ms.sourcegitcommit: 4fedeb06a6e7796096fc6279cfb091c7b89d484d
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/31/2019
ms.locfileid: "34668328"
---
# <a name="attributes-for-information-barrier-policies-preview"></a><span data-ttu-id="d85fd-103">정보 장벽 정책의 특성 (미리 보기)</span><span class="sxs-lookup"><span data-stu-id="d85fd-103">Attributes for information barrier policies (Preview)</span></span>

<span data-ttu-id="d85fd-104">Azure Active Directory의 특정 특성을 사용 하 여 사용자를 분할할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d85fd-104">Certain attributes in Azure Active Directory can be used to segment users.</span></span> <span data-ttu-id="d85fd-105">세그먼트는 정보 장벽 정책에 대 한 필터로 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d85fd-105">Segments are then used as filters for information barrier policies.</span></span> <span data-ttu-id="d85fd-106">예를 들어 **부서** 를 사용 하 여 조직 내 부서별로 사용자 세그먼트를 정의할 수 있습니다 (두 부서가 동시에 단일 직원이 작동 하지 않는다고 가정).</span><span class="sxs-lookup"><span data-stu-id="d85fd-106">For example, you might use **Department** to define segments of users by department within your organization (assuming no single employee works for two departments at the same time).</span></span> 

<span data-ttu-id="d85fd-107">이 문서에서는 사용할 수 있는 특성 목록을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="d85fd-107">This article provides a list of attributes that can be used.</span></span> <span data-ttu-id="d85fd-108">정보 장벽에 대 한 자세한 내용은 다음 리소스를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="d85fd-108">To learn more about information barriers, see the following resources:</span></span>
- [<span data-ttu-id="d85fd-109">정보 장벽 (미리 보기)</span><span class="sxs-lookup"><span data-stu-id="d85fd-109">Information barriers (Preview)</span></span>](information-barriers.md)
- [<span data-ttu-id="d85fd-110">Microsoft 팀의 정보 장벽에 대 한 정책 정의 (미리 보기)</span><span class="sxs-lookup"><span data-stu-id="d85fd-110">Define policies for information barriers in Microsoft Teams (Preview)</span></span>](information-barriers-policies.md)

## <a name="how-to-use-attributes-in-information-barrier-policies"></a><span data-ttu-id="d85fd-111">정보 장벽 정책에서 특성을 사용 하는 방법</span><span class="sxs-lookup"><span data-stu-id="d85fd-111">How to use attributes in information barrier policies</span></span>

<span data-ttu-id="d85fd-112">이 문서에 나와 있는 특성을 사용 하 여 사용자의 세그먼트를 정의 하거나 편집할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d85fd-112">The attributes listed in this article can be used to define (or edit) segments of users.</span></span> <span data-ttu-id="d85fd-113">세그먼트는 다음 예제와 같이 정보 장벽 정책에서 매개 변수 (UserGroupFilter)로 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d85fd-113">Segments are used as parameters (UserGroupFilter) in information barrier policies, as shown in the following examples:</span></span>

|<span data-ttu-id="d85fd-114">예제</span><span class="sxs-lookup"><span data-stu-id="d85fd-114">Example</span></span>  |<span data-ttu-id="d85fd-115">#A0</span><span class="sxs-lookup"><span data-stu-id="d85fd-115">Cmdlet</span></span>  |
|---------|---------|
|<span data-ttu-id="d85fd-116">부서 특성을 사용 하 여 Segment1 라는 세그먼트를 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="d85fd-116">Define a segment called Segment1 using the Department attribute</span></span>     | `New-OrganizationSegment -Name "Segment1" -UserGroupFilter "Department -eq 'Department1'"`        |
|<span data-ttu-id="d85fd-117">MemberOf 특성을 사용 하 여 SegmentA 이라는 세그먼트를 정의 합니다 (이 특성에 그룹 이름 (예: "BlueGroup")이 포함 되어 있다고 가정).</span><span class="sxs-lookup"><span data-stu-id="d85fd-117">Define a segment called SegmentA using the MemberOf attribute (suppose this attribute contains group names, such as "BlueGroup")</span></span>     | `New-OrganizationSegment -Name "SegmentA" -UserGroupFilter "MemberOf -eq 'BlueGroup'"`        |
|<span data-ttu-id="d85fd-118">ExtensionAttribute1을 사용 하 여 DayTraders 라는 세그먼트를 정의 합니다 (이 특성에 직함 (예: "Daytraders")이 포함 되어 있다고 가정 합니다.)</span><span class="sxs-lookup"><span data-stu-id="d85fd-118">Define a segment called DayTraders using ExtensionAttribute1 (suppose this attribute contains job titles, such as "DayTrader")</span></span>|`New-OrganizationSegment -Name "DayTraders" -UserGroupFilter "ExtensionAttribute1 -eq 'DayTrader'"` |

<span data-ttu-id="d85fd-119">세그먼트를 정의할 때 모든 세그먼트에 같은 특성을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="d85fd-119">When you define segments, use the same attribute for all your segments.</span></span> <span data-ttu-id="d85fd-120">예를 들어 *부서*를 사용 하 여 일부 세그먼트를 정의 하는 경우에는 *부서*를 사용 하 여 모든 세그먼트를 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="d85fd-120">For example, if you define some segments using *Department*, define all of the segments using *Department*.</span></span> <span data-ttu-id="d85fd-121">*부서* 및 다른 사용자는 *MemberOf*를 사용 하 여 일부 세그먼트를 정의 하지 마세요.</span><span class="sxs-lookup"><span data-stu-id="d85fd-121">Don't define some segments using *Department* and others using *MemberOf*.</span></span> <span data-ttu-id="d85fd-122">세그먼트가 겹치지 않는지 확인 합니다. 각 사용자는 정확히 하나의 세그먼트에 할당 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d85fd-122">Make sure your segments do not overlap; each user should be assigned to exactly one segment.</span></span> 

<span data-ttu-id="d85fd-123">자세한 내용은 [PowerShell을 사용 하 여 세그먼트 정의](information-barriers-policies.md#define-segments-using-powershell)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="d85fd-123">To learn more, see [Define segments using PowerShell](information-barriers-policies.md#define-segments-using-powershell).</span></span>

## <a name="reference"></a><span data-ttu-id="d85fd-124">참조</span><span class="sxs-lookup"><span data-stu-id="d85fd-124">Reference</span></span>

<span data-ttu-id="d85fd-125">다음 표에는 정보 장벽에 사용할 수 있는 특성이 나와 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d85fd-125">The following table lists the attributes that you can use with information barriers.</span></span>

|<span data-ttu-id="d85fd-126">Azure Active Directory 속성 이름 (LDAP 표시 이름)</span><span class="sxs-lookup"><span data-stu-id="d85fd-126">Azure Active Directory property name (LDAP display name)</span></span>  |<span data-ttu-id="d85fd-127">Exchange 속성 이름</span><span class="sxs-lookup"><span data-stu-id="d85fd-127">Exchange property name</span></span>  |
|---------|---------|
|<span data-ttu-id="d85fd-128">Co</span><span class="sxs-lookup"><span data-stu-id="d85fd-128">Co</span></span>       | <span data-ttu-id="d85fd-129">Co</span><span class="sxs-lookup"><span data-stu-id="d85fd-129">Co</span></span>        |
|<span data-ttu-id="d85fd-130">Company</span><span class="sxs-lookup"><span data-stu-id="d85fd-130">Company</span></span>     |<span data-ttu-id="d85fd-131">Company</span><span class="sxs-lookup"><span data-stu-id="d85fd-131">Company</span></span>         |
|<span data-ttu-id="d85fd-132">부서</span><span class="sxs-lookup"><span data-stu-id="d85fd-132">Department</span></span>     |<span data-ttu-id="d85fd-133">부서</span><span class="sxs-lookup"><span data-stu-id="d85fd-133">Department</span></span>         |
|<span data-ttu-id="d85fd-134">ExtensionAttribute1</span><span class="sxs-lookup"><span data-stu-id="d85fd-134">ExtensionAttribute1</span></span> |<span data-ttu-id="d85fd-135">CustomAttribute1</span><span class="sxs-lookup"><span data-stu-id="d85fd-135">CustomAttribute1</span></span>  |
|<span data-ttu-id="d85fd-136">ExtensionAttribute2</span><span class="sxs-lookup"><span data-stu-id="d85fd-136">ExtensionAttribute2</span></span> |<span data-ttu-id="d85fd-137">CustomAttribute2</span><span class="sxs-lookup"><span data-stu-id="d85fd-137">CustomAttribute2</span></span>  |
|<span data-ttu-id="d85fd-138">ExtensionAttribute3</span><span class="sxs-lookup"><span data-stu-id="d85fd-138">ExtensionAttribute3</span></span> |<span data-ttu-id="d85fd-139">CustomAttribute3</span><span class="sxs-lookup"><span data-stu-id="d85fd-139">CustomAttribute3</span></span>  |
|<span data-ttu-id="d85fd-140">ExtensionAttribute4</span><span class="sxs-lookup"><span data-stu-id="d85fd-140">ExtensionAttribute4</span></span> |<span data-ttu-id="d85fd-141">CustomAttribute4</span><span class="sxs-lookup"><span data-stu-id="d85fd-141">CustomAttribute4</span></span>  |
|<span data-ttu-id="d85fd-142">ExtensionAttribute5</span><span class="sxs-lookup"><span data-stu-id="d85fd-142">ExtensionAttribute5</span></span> |<span data-ttu-id="d85fd-143">CustomAttribute5</span><span class="sxs-lookup"><span data-stu-id="d85fd-143">CustomAttribute5</span></span>  |
|<span data-ttu-id="d85fd-144">ExtensionAttribute6</span><span class="sxs-lookup"><span data-stu-id="d85fd-144">ExtensionAttribute6</span></span> |<span data-ttu-id="d85fd-145">CustomAttribute6</span><span class="sxs-lookup"><span data-stu-id="d85fd-145">CustomAttribute6</span></span>  |
|<span data-ttu-id="d85fd-146">ExtensionAttribute7</span><span class="sxs-lookup"><span data-stu-id="d85fd-146">ExtensionAttribute7</span></span> |<span data-ttu-id="d85fd-147">CustomAttribute7</span><span class="sxs-lookup"><span data-stu-id="d85fd-147">CustomAttribute7</span></span>  |
|<span data-ttu-id="d85fd-148">ExtensionAttribute8</span><span class="sxs-lookup"><span data-stu-id="d85fd-148">ExtensionAttribute8</span></span> |<span data-ttu-id="d85fd-149">CustomAttribute8</span><span class="sxs-lookup"><span data-stu-id="d85fd-149">CustomAttribute8</span></span>  |
|<span data-ttu-id="d85fd-150">ExtensionAttribute9</span><span class="sxs-lookup"><span data-stu-id="d85fd-150">ExtensionAttribute9</span></span> |<span data-ttu-id="d85fd-151">CustomAttribute9</span><span class="sxs-lookup"><span data-stu-id="d85fd-151">CustomAttribute9</span></span>  |
|<span data-ttu-id="d85fd-152">ExtensionAttribute10</span><span class="sxs-lookup"><span data-stu-id="d85fd-152">ExtensionAttribute10</span></span> |<span data-ttu-id="d85fd-153">CustomAttribute10</span><span class="sxs-lookup"><span data-stu-id="d85fd-153">CustomAttribute10</span></span>  |
|<span data-ttu-id="d85fd-154">ExtensionAttribute11</span><span class="sxs-lookup"><span data-stu-id="d85fd-154">ExtensionAttribute11</span></span> |<span data-ttu-id="d85fd-155">CustomAttribute11</span><span class="sxs-lookup"><span data-stu-id="d85fd-155">CustomAttribute11</span></span>  |
|<span data-ttu-id="d85fd-156">ExtensionAttribute12</span><span class="sxs-lookup"><span data-stu-id="d85fd-156">ExtensionAttribute12</span></span> |<span data-ttu-id="d85fd-157">CustomAttribute12</span><span class="sxs-lookup"><span data-stu-id="d85fd-157">CustomAttribute12</span></span>  |
|<span data-ttu-id="d85fd-158">ExtensionAttribute13</span><span class="sxs-lookup"><span data-stu-id="d85fd-158">ExtensionAttribute13</span></span> |<span data-ttu-id="d85fd-159">CustomAttribute13</span><span class="sxs-lookup"><span data-stu-id="d85fd-159">CustomAttribute13</span></span>  |
|<span data-ttu-id="d85fd-160">ExtensionAttribute14</span><span class="sxs-lookup"><span data-stu-id="d85fd-160">ExtensionAttribute14</span></span> |<span data-ttu-id="d85fd-161">CustomAttribute14</span><span class="sxs-lookup"><span data-stu-id="d85fd-161">CustomAttribute14</span></span>  |
|<span data-ttu-id="d85fd-162">ExtensionAttribute15</span><span class="sxs-lookup"><span data-stu-id="d85fd-162">ExtensionAttribute15</span></span> |<span data-ttu-id="d85fd-163">CustomAttribute15</span><span class="sxs-lookup"><span data-stu-id="d85fd-163">CustomAttribute15</span></span>  |
|<span data-ttu-id="d85fd-164">MSExchExtensionCustomAttribute1</span><span class="sxs-lookup"><span data-stu-id="d85fd-164">MSExchExtensionCustomAttribute1</span></span> |<span data-ttu-id="d85fd-165">ExtensionCustomAttribute1</span><span class="sxs-lookup"><span data-stu-id="d85fd-165">ExtensionCustomAttribute1</span></span> |
|<span data-ttu-id="d85fd-166">MSExchExtensionCustomAttribute2</span><span class="sxs-lookup"><span data-stu-id="d85fd-166">MSExchExtensionCustomAttribute2</span></span> |<span data-ttu-id="d85fd-167">ExtensionCustomAttribute2</span><span class="sxs-lookup"><span data-stu-id="d85fd-167">ExtensionCustomAttribute2</span></span> |
|<span data-ttu-id="d85fd-168">MSExchExtensionCustomAttribute3</span><span class="sxs-lookup"><span data-stu-id="d85fd-168">MSExchExtensionCustomAttribute3</span></span> |<span data-ttu-id="d85fd-169">ExtensionCustomAttribute3</span><span class="sxs-lookup"><span data-stu-id="d85fd-169">ExtensionCustomAttribute3</span></span> |
|<span data-ttu-id="d85fd-170">MSExchExtensionCustomAttribute4</span><span class="sxs-lookup"><span data-stu-id="d85fd-170">MSExchExtensionCustomAttribute4</span></span> |<span data-ttu-id="d85fd-171">ExtensionCustomAttribute4</span><span class="sxs-lookup"><span data-stu-id="d85fd-171">ExtensionCustomAttribute4</span></span> |
|<span data-ttu-id="d85fd-172">MSExchExtensionCustomAttribute5</span><span class="sxs-lookup"><span data-stu-id="d85fd-172">MSExchExtensionCustomAttribute5</span></span> |<span data-ttu-id="d85fd-173">ExtensionCustomAttribute5</span><span class="sxs-lookup"><span data-stu-id="d85fd-173">ExtensionCustomAttribute5</span></span> |
|<span data-ttu-id="d85fd-174">MailNickname</span><span class="sxs-lookup"><span data-stu-id="d85fd-174">MailNickname</span></span> |<span data-ttu-id="d85fd-175">별칭</span><span class="sxs-lookup"><span data-stu-id="d85fd-175">Alias</span></span> |
|<span data-ttu-id="d85fd-176">PhysicalDeliveryOfficeName</span><span class="sxs-lookup"><span data-stu-id="d85fd-176">PhysicalDeliveryOfficeName</span></span> |<span data-ttu-id="d85fd-177">Office</span><span class="sxs-lookup"><span data-stu-id="d85fd-177">Office</span></span> |
|<span data-ttu-id="d85fd-178">PostalCode</span><span class="sxs-lookup"><span data-stu-id="d85fd-178">PostalCode</span></span> |<span data-ttu-id="d85fd-179">PostalCode</span><span class="sxs-lookup"><span data-stu-id="d85fd-179">PostalCode</span></span> |
|<span data-ttu-id="d85fd-180">ProxyAddresses</span><span class="sxs-lookup"><span data-stu-id="d85fd-180">ProxyAddresses</span></span> |<span data-ttu-id="d85fd-181">EmailAddresses</span><span class="sxs-lookup"><span data-stu-id="d85fd-181">EmailAddresses</span></span> |
|<span data-ttu-id="d85fd-182">StreetAddress</span><span class="sxs-lookup"><span data-stu-id="d85fd-182">StreetAddress</span></span> |<span data-ttu-id="d85fd-183">StreetAddress</span><span class="sxs-lookup"><span data-stu-id="d85fd-183">StreetAddress</span></span> |
|<span data-ttu-id="d85fd-184">TargetAddress</span><span class="sxs-lookup"><span data-stu-id="d85fd-184">TargetAddress</span></span> |<span data-ttu-id="d85fd-185">ExternalEmailAddress</span><span class="sxs-lookup"><span data-stu-id="d85fd-185">ExternalEmailAddress</span></span> |
|<span data-ttu-id="d85fd-186">UsageLocation</span><span class="sxs-lookup"><span data-stu-id="d85fd-186">UsageLocation</span></span> |<span data-ttu-id="d85fd-187">UsageLocation</span><span class="sxs-lookup"><span data-stu-id="d85fd-187">UsageLocation</span></span> |
|<span data-ttu-id="d85fd-188">UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="d85fd-188">UserPrincipalName</span></span>  |<span data-ttu-id="d85fd-189">UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="d85fd-189">UserPrincipalName</span></span>  |
|<span data-ttu-id="d85fd-190">메일로</span><span class="sxs-lookup"><span data-stu-id="d85fd-190">Mail</span></span>   |<span data-ttu-id="d85fd-191">WindowsEmailAddress</span><span class="sxs-lookup"><span data-stu-id="d85fd-191">WindowsEmailAddress</span></span>    |
|<span data-ttu-id="d85fd-192">설명</span><span class="sxs-lookup"><span data-stu-id="d85fd-192">Description</span></span>    |<span data-ttu-id="d85fd-193">설명</span><span class="sxs-lookup"><span data-stu-id="d85fd-193">Description</span></span>    |
|<span data-ttu-id="d85fd-194">소속</span><span class="sxs-lookup"><span data-stu-id="d85fd-194">MemberOf</span></span>   |<span data-ttu-id="d85fd-195">MemberOfGroup</span><span class="sxs-lookup"><span data-stu-id="d85fd-195">MemberOfGroup</span></span>  |

## <a name="related-topics"></a><span data-ttu-id="d85fd-196">관련 항목</span><span class="sxs-lookup"><span data-stu-id="d85fd-196">Related topics</span></span>

[<span data-ttu-id="d85fd-197">Microsoft 팀의 정보 장벽에 대 한 정책 정의 (미리 보기)</span><span class="sxs-lookup"><span data-stu-id="d85fd-197">Define policies for information barriers in Microsoft Teams (Preview)</span></span>](information-barriers-policies.md)

[<span data-ttu-id="d85fd-198">정보 장벽 문제 해결 (미리 보기)</span><span class="sxs-lookup"><span data-stu-id="d85fd-198">Troubleshooting information barriers (Preview)</span></span>](information-barriers-troubleshooting.md)

[<span data-ttu-id="d85fd-199">정보 장벽 (미리 보기)</span><span class="sxs-lookup"><span data-stu-id="d85fd-199">Information barriers (Preview)</span></span>](information-barriers.md)



