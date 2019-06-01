---
title: 정보 장벽 정책 정의
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
description: Microsoft 팀에서 정보 장벽에 대 한 정책을 정의 하는 방법에 대해 알아봅니다.
ms.openlocfilehash: 3ec9d89f22456f00104135013ee6009e8e4824df
ms.sourcegitcommit: 4fedeb06a6e7796096fc6279cfb091c7b89d484d
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/31/2019
ms.locfileid: "34668326"
---
# <a name="define-policies-for-information-barriers-preview"></a><span data-ttu-id="4bfc1-103">정보 장벽에 대 한 정책 정의 (미리 보기)</span><span class="sxs-lookup"><span data-stu-id="4bfc1-103">Define policies for information barriers (Preview)</span></span>

<span data-ttu-id="4bfc1-104">정보 장애물을 사용 하 여 특정 사용자 세그먼트가 서로 통신 하지 못하도록 설계 된 정책을 정의 하거나 특정 세그먼트가 다른 특정 세그먼트와만 통신할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4bfc1-104">With information barriers, you can define policies that are designed to prevent certain segments of users from communicating with each other, or allow specific segments to communicate only with certain other segments.</span></span> <span data-ttu-id="4bfc1-105">정보 장벽 정책은 조직에서 관련 업계 표준 및 규정 준수를 유지 하 고, 잠재적으로 발생할 수 있는 충돌을 방지 하는 데 도움이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4bfc1-105">Information barrier policies can help your organization maintain compliance with relevant industry standards and regulations, and avoid potential conflicts of interest.</span></span> <span data-ttu-id="4bfc1-106">자세한 내용은 [정보 장벽 (미리 보기)](information-barriers.md)을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="4bfc1-106">To learn more, see [Information barriers (Preview)](information-barriers.md).</span></span> 

> [!IMPORTANT]
> <span data-ttu-id="4bfc1-107">이 문서에서는 정보 장벽 정책을 계획, 정의, 구현 및 관리 하는 방법에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="4bfc1-107">This article describes how to plan, define, implement, and manage information barrier policies.</span></span> <span data-ttu-id="4bfc1-108">여러 단계를 수행 하 고 작업 흐름을 여러 부분으로 분할 합니다.</span><span class="sxs-lookup"><span data-stu-id="4bfc1-108">Several steps are involved, and the work flow is divided into several parts.</span></span> <span data-ttu-id="4bfc1-109">정보 장벽 정책 정의 또는 편집을 시작 하기 전에 [필수 구성 요소](#prerequisites) 및 전체 프로세스를 확인 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="4bfc1-109">Make sure to read through the [prerequisites](#prerequisites) and the entire process before you begin defining (or editing) information barrier policies.</span></span>

## <a name="concepts-of-information-barrier-policies"></a><span data-ttu-id="4bfc1-110">정보 장벽 정책의 개념</span><span class="sxs-lookup"><span data-stu-id="4bfc1-110">Concepts of information barrier policies</span></span>

<span data-ttu-id="4bfc1-111">정보 장벽 정책을 계획, 정의 및 구현 하기 전에 기본 개념에 대해 알아봅니다.</span><span class="sxs-lookup"><span data-stu-id="4bfc1-111">Before you plan, define, and implement information barrier policies, get to know the underlying concepts.</span></span> <span data-ttu-id="4bfc1-112">정보 장벽에서는이 문서에서 설명 하는 사용자 계정 특성, 세그먼트, 정보 장벽 정책 및 정책 응용 프로그램 프로세스를 사용 하 여 작업 합니다.</span><span class="sxs-lookup"><span data-stu-id="4bfc1-112">With information barriers, you'll work with user account attributes, segments, information barrier policies, and a policy application process described in this article.</span></span> 

- <span data-ttu-id="4bfc1-113">**사용자 계정 특성** 은 Azure Active Directory (또는 Exchange Online)에서 정의 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4bfc1-113">**User account attributes** are defined in Azure Active Directory (or Exchange Online).</span></span> <span data-ttu-id="4bfc1-114">이러한 특성에는 부서, 직함, 위치, 팀 이름 등이 포함 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4bfc1-114">These attributes can include department, job title, location, team name, etc.</span></span> 

- <span data-ttu-id="4bfc1-115">**세그먼트** 는 부서, 직책, 위치, 팀 이름 또는 [지원 되는 특성](information-barriers-attributes.md)등 선택한 **사용자 계정 특성**을 사용 하 여 Office 365 보안 & 준수 센터에 정의 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4bfc1-115">**Segments** are defined in the Office 365 Security & Compliance Center using a selected **user account attribute**, such as department, job title, location, team name, or any [supported attribute](information-barriers-attributes.md).</span></span> <span data-ttu-id="4bfc1-116">세그먼트를 정의 해도 사용자에 게 영향을 주지 않습니다. 정보 장벽 정책을 정의 하 고 적용 하기 위한 단계를 설정 하기만 하면 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4bfc1-116">Defining segments does not effect users; it just sets the stage for information barrier policies to be defined and then applied.</span></span>

- <span data-ttu-id="4bfc1-117">**정보 장벽 정책이** 정의 되 고 개별 **세그먼트**에 할당 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4bfc1-117">**Information barrier policies** are defined and assigned to individual **Segments**.</span></span> <span data-ttu-id="4bfc1-118">일부 세그먼트에는 정책이 할당 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4bfc1-118">Not all segments will have a policy assigned.</span></span> <span data-ttu-id="4bfc1-119">또한 하나의 세그먼트에 두 개 이상의 정책이 할당 될 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="4bfc1-119">In addition, no single segment can be assigned more than one policy.</span></span> <span data-ttu-id="4bfc1-120">정책을 정의할 때는 두 가지 종류의 정책 중에서 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="4bfc1-120">When you define policies, you choose from two kinds of policies:</span></span>
    - <span data-ttu-id="4bfc1-121">한 세그먼트가 다른 세그먼트와 통신할 수 없도록 하는 정책</span><span class="sxs-lookup"><span data-stu-id="4bfc1-121">Policies that prevent one segment from communicating with another segment</span></span>
    - <span data-ttu-id="4bfc1-122">하나의 세그먼트가 다른 특정 세그먼트와도 통신할 수 있도록 하는 정책</span><span class="sxs-lookup"><span data-stu-id="4bfc1-122">Policies that allow one segment to communicate with only certain other segments</span></span>

    <span data-ttu-id="4bfc1-123">조직에서 법적 및 업계 요구 사항을 준수 하는 데 필요한 최소 정책 수를 사용 하는 것이 이상적입니다.</span><span class="sxs-lookup"><span data-stu-id="4bfc1-123">Ideally, you'll use the minimum number of policies to ensure your organization is compliant with legal and industry requirements.</span></span>

- <span data-ttu-id="4bfc1-124">**정책 응용 프로그램** 은 모든 정보 장벽 정책이 정의 된 후에 수행 되며, 조직에 적용할 준비가 된 것입니다.</span><span class="sxs-lookup"><span data-stu-id="4bfc1-124">**Policy application** is done after all information barrier policies are defined, and you are ready to apply them in your organization.</span></span>

## <a name="the-work-flow-at-a-glance"></a><span data-ttu-id="4bfc1-125">작업 흐름 살펴보기</span><span class="sxs-lookup"><span data-stu-id="4bfc1-125">The work flow at a glance</span></span>

|<span data-ttu-id="4bfc1-126">단계</span><span class="sxs-lookup"><span data-stu-id="4bfc1-126">Phase</span></span>    |<span data-ttu-id="4bfc1-127">관련 기능</span><span class="sxs-lookup"><span data-stu-id="4bfc1-127">What's involved</span></span>  |
|---------|---------|
|[<span data-ttu-id="4bfc1-128">필수 구성 요소를 충족 하는지 확인</span><span class="sxs-lookup"><span data-stu-id="4bfc1-128">Make sure prerequisites are met</span></span>](#prerequisites)     |<span data-ttu-id="4bfc1-129">-구독에 정보 장벽 포함 여부 확인</span><span class="sxs-lookup"><span data-stu-id="4bfc1-129">- Confirm that your subscription includes information barriers</span></span><br/><span data-ttu-id="4bfc1-130">-세그먼트 및 정책을 정의/편집 하는 데 필요한 권한이 있는지 확인</span><span class="sxs-lookup"><span data-stu-id="4bfc1-130">- Verify that you have the necessary permissions to define/edit segments and policies</span></span><br/><span data-ttu-id="4bfc1-131">-디렉터리 데이터에 조직의 구조가 반영 되는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="4bfc1-131">- Make sure that your directory data reflects your organization's structure</span></span><br/><span data-ttu-id="4bfc1-132">-Microsoft 팀에서 범위 디렉터리 검색이 사용 하도록 설정 되어 있는지 확인</span><span class="sxs-lookup"><span data-stu-id="4bfc1-132">- Make sure that scoped directory search is enabled in Microsoft Teams</span></span><br/><span data-ttu-id="4bfc1-133">-감사 로깅이 설정 되어 있는지 확인</span><span class="sxs-lookup"><span data-stu-id="4bfc1-133">- Make sure audit logging is turned on</span></span><br/><span data-ttu-id="4bfc1-134">-이 문서의 작업을 수행 하려면 PowerShell을 사용 합니다 (예: cmdlet이 제공 됨).</span><span class="sxs-lookup"><span data-stu-id="4bfc1-134">- Use PowerShell to perform the tasks in this article (example cmdlets are provided)</span></span><br/><span data-ttu-id="4bfc1-135">-Microsoft 팀의 정보 장벽에 대 한 관리자 동의 제공 (단계 포함)</span><span class="sxs-lookup"><span data-stu-id="4bfc1-135">- Provide admin consent for information barriers in Microsoft Teams (steps are included)</span></span>          |
|[<span data-ttu-id="4bfc1-136">1 부: 조직의 모든 사용자 분할</span><span class="sxs-lookup"><span data-stu-id="4bfc1-136">Part 1: Segment all the users in your organization</span></span>](#part-1-segment-users)     |<span data-ttu-id="4bfc1-137">-필요한 정책을 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4bfc1-137">- Determine what policies are needed</span></span><br/><span data-ttu-id="4bfc1-138">-정의할 세그먼트 목록을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="4bfc1-138">- Make a list of segments to define</span></span><br/><span data-ttu-id="4bfc1-139">-사용할 특성 식별</span><span class="sxs-lookup"><span data-stu-id="4bfc1-139">- Identify which attributes to use</span></span><br/><span data-ttu-id="4bfc1-140">-정책 필터 용어로 세그먼트를 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="4bfc1-140">- Define segments in terms of policy filters</span></span>        |
|[<span data-ttu-id="4bfc1-141">2 부: 정보 장벽 정책 정의</span><span class="sxs-lookup"><span data-stu-id="4bfc1-141">Part 2: Define information barrier policies</span></span>](#part-2-define-information-barrier-policies)     |<span data-ttu-id="4bfc1-142">-정책 정의 (아직 적용 되지 않음)</span><span class="sxs-lookup"><span data-stu-id="4bfc1-142">- Define your policies (do not apply yet)</span></span><br/><span data-ttu-id="4bfc1-143">-두 종류 (차단 또는 허용)를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="4bfc1-143">- Choose from two kinds (block or allow)</span></span> |
|[<span data-ttu-id="4bfc1-144">3 부: 정보 장벽 정책 적용</span><span class="sxs-lookup"><span data-stu-id="4bfc1-144">Part 3: Apply information barrier policies</span></span>](#part-3-apply-information-barrier-policies)     |<span data-ttu-id="4bfc1-145">-정책을 활성 상태로 설정</span><span class="sxs-lookup"><span data-stu-id="4bfc1-145">- Set policies to active status</span></span><br/><span data-ttu-id="4bfc1-146">-정책 응용 프로그램 실행</span><span class="sxs-lookup"><span data-stu-id="4bfc1-146">- Run the policy application</span></span><br/><span data-ttu-id="4bfc1-147">-정책 상태 확인</span><span class="sxs-lookup"><span data-stu-id="4bfc1-147">- Verify policy status</span></span>         |
|<span data-ttu-id="4bfc1-148">(필요한 경우) [세그먼트 또는 정책 편집](#edit-a-segment-or-a-policy)</span><span class="sxs-lookup"><span data-stu-id="4bfc1-148">(As needed) [Edit a segment or a policy](#edit-a-segment-or-a-policy)</span></span>     |<span data-ttu-id="4bfc1-149">-세그먼트 편집</span><span class="sxs-lookup"><span data-stu-id="4bfc1-149">- Edit a segment</span></span><br/><span data-ttu-id="4bfc1-150">-정책 편집 또는 제거</span><span class="sxs-lookup"><span data-stu-id="4bfc1-150">- Edit or remove a policy</span></span><br/><span data-ttu-id="4bfc1-151">-정책 응용 프로그램 실행</span><span class="sxs-lookup"><span data-stu-id="4bfc1-151">- Run the policy application</span></span><br/><span data-ttu-id="4bfc1-152">-정책 상태 확인</span><span class="sxs-lookup"><span data-stu-id="4bfc1-152">- Verify policy status</span></span>         |
|<span data-ttu-id="4bfc1-153">(필요한 경우) [문제 해결](information-barriers-troubleshooting.md)</span><span class="sxs-lookup"><span data-stu-id="4bfc1-153">(As needed) [Troubleshooting](information-barriers-troubleshooting.md)</span></span>|<span data-ttu-id="4bfc1-154">-정책이 예상 대로 작동 하지 않을 때 작업 수행</span><span class="sxs-lookup"><span data-stu-id="4bfc1-154">- Take action when policies are not working as expected</span></span>|

## <a name="prerequisites"></a><span data-ttu-id="4bfc1-155">필수 구성 요소</span><span class="sxs-lookup"><span data-stu-id="4bfc1-155">Prerequisites</span></span>

<span data-ttu-id="4bfc1-156">**현재 정보 장벽 기능은 개인 미리 보기에**있습니다.</span><span class="sxs-lookup"><span data-stu-id="4bfc1-156">**Currently, the information barrier feature is in private preview**.</span></span> <span data-ttu-id="4bfc1-157">일반적으로 이러한 기능을 사용할 수 있는 경우 다음과 같은 구독에 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4bfc1-157">When these features are generally available, they'll be included in subscriptions, such as:</span></span>

- <span data-ttu-id="4bfc1-158">Microsoft 365 E5</span><span class="sxs-lookup"><span data-stu-id="4bfc1-158">Microsoft 365 E5</span></span>
- <span data-ttu-id="4bfc1-159">Office 365 E5</span><span class="sxs-lookup"><span data-stu-id="4bfc1-159">Office 365 E5</span></span>
- <span data-ttu-id="4bfc1-160">Office 365 Advanced Compliance</span><span class="sxs-lookup"><span data-stu-id="4bfc1-160">Office 365 Advanced Compliance</span></span>
- <span data-ttu-id="4bfc1-161">Microsoft 365 E5 정보 보호 및 규정 준수</span><span class="sxs-lookup"><span data-stu-id="4bfc1-161">Microsoft 365 E5 Information Protection and Compliance</span></span>

<span data-ttu-id="4bfc1-162">자세한 내용은 [준수 솔루션](https://products.office.com/business/security-and-compliance/compliance-solutions)을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="4bfc1-162">For more details, see [Compliance Solutions](https://products.office.com/business/security-and-compliance/compliance-solutions).</span></span>

### <a name="permissions"></a><span data-ttu-id="4bfc1-163">사용 권한</span><span class="sxs-lookup"><span data-stu-id="4bfc1-163">Permissions</span></span>

<span data-ttu-id="4bfc1-164">정보 장벽 정책을 정의 하거나 편집 하려면 다음 중 하 나와 같은 **적절 한 역할을 할당 받아야 합니다**.</span><span class="sxs-lookup"><span data-stu-id="4bfc1-164">To define or edit information barrier policies, **you must be assigned an appropriate role**, such as one of the following:</span></span>
- <span data-ttu-id="4bfc1-165">Microsoft 365 Enterprise 전역 관리자</span><span class="sxs-lookup"><span data-stu-id="4bfc1-165">Microsoft 365 Enterprise Global Administrator</span></span>
- <span data-ttu-id="4bfc1-166">Office 365 전역 관리자</span><span class="sxs-lookup"><span data-stu-id="4bfc1-166">Office 365 Global Administrator</span></span>
- <span data-ttu-id="4bfc1-167">준수 관리자</span><span class="sxs-lookup"><span data-stu-id="4bfc1-167">Compliance Administrator</span></span>
- <span data-ttu-id="4bfc1-168">IB 준수 관리 (새 역할입니다.)</span><span class="sxs-lookup"><span data-stu-id="4bfc1-168">IB Compliance Management (this is a new role!)</span></span>

<span data-ttu-id="4bfc1-169">역할 및 사용 권한에 대 한 자세한 내용은 [permissions in The Office 365 Security & 준수 센터](permissions-in-the-security-and-compliance-center.md)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="4bfc1-169">To learn more about roles and permissions, see [Permissions in the Office 365 Security & Compliance Center](permissions-in-the-security-and-compliance-center.md).</span></span>
       
### <a name="directory-data"></a><span data-ttu-id="4bfc1-170">디렉터리 데이터</span><span class="sxs-lookup"><span data-stu-id="4bfc1-170">Directory data</span></span>

<span data-ttu-id="4bfc1-171">**조직의 구조가 디렉터리 데이터에 반영 되는지 확인**합니다.</span><span class="sxs-lookup"><span data-stu-id="4bfc1-171">**Make sure that your organization's structure is reflected in directory data**.</span></span> <span data-ttu-id="4bfc1-172">이렇게 하려면 그룹 구성원 자격, 부서 이름 등의 사용자 계정 특성이 Azure Active Directory 또는 Exchange Online에서 올바르게 채워졌는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="4bfc1-172">To do this, make sure that user account attributes, such as group membership, department name, etc. are populated correctly in Azure Active Directory (or Exchange Online).</span></span> <span data-ttu-id="4bfc1-173">자세한 내용은 다음 리소스를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="4bfc1-173">To learn more, see the following resources:</span></span>
- [<span data-ttu-id="4bfc1-174">정보 장벽 정책의 특성 (미리 보기)</span><span class="sxs-lookup"><span data-stu-id="4bfc1-174">Attributes for information barrier policies (Preview)</span></span>](information-barriers-attributes.md)
- [<span data-ttu-id="4bfc1-175">Azure Active Directory를 사용 하 여 사용자 프로필 정보 추가 또는 업데이트</span><span class="sxs-lookup"><span data-stu-id="4bfc1-175">Add or update a user's profile information using Azure Active Directory</span></span>](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-users-profile-azure-portal)
- [<span data-ttu-id="4bfc1-176">Office 365 PowerShell를 사용 하 여 사용자 계정 속성 구성</span><span class="sxs-lookup"><span data-stu-id="4bfc1-176">Configure user account properties with Office 365 PowerShell</span></span>](https://docs.microsoft.com/office365/enterprise/powershell/configure-user-account-properties-with-office-365-powershell)

### <a name="scoped-directory-search"></a><span data-ttu-id="4bfc1-177">범위 지정 디렉터리 검색</span><span class="sxs-lookup"><span data-stu-id="4bfc1-177">Scoped directory search</span></span>

<span data-ttu-id="4bfc1-178">**조직의 첫 번째 정보 장벽 정책을 정의 하기 전에 [Microsoft 팀에서 범위 지정 디렉터리 검색을 사용 하도록 설정](https://docs.microsoft.com/MicrosoftTeams/teams-scoped-directory-search)해야 합니다**.</span><span class="sxs-lookup"><span data-stu-id="4bfc1-178">**Before you define your organization's first information barrier policy, you must [enable scoped directory search in Microsoft Teams](https://docs.microsoft.com/MicrosoftTeams/teams-scoped-directory-search)**.</span></span> <span data-ttu-id="4bfc1-179">정보 장벽 정책을 설정 하거나 정의 하기 전에 범위 디렉터리 검색을 사용 하도록 설정한 후 24 시간 이상 기다립니다.</span><span class="sxs-lookup"><span data-stu-id="4bfc1-179">Wait at least 24 hours after enabling scoped directory search before you set up or define information barrier policies.</span></span>

### <a name="audit-logging"></a><span data-ttu-id="4bfc1-180">감사 로깅</span><span class="sxs-lookup"><span data-stu-id="4bfc1-180">Audit logging</span></span>

<span data-ttu-id="4bfc1-181">정책 응용 프로그램의 상태를 조회 하려면 감사 로깅이 설정 되어 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="4bfc1-181">In order to look up the status of a policy application, audit logging must be turned on.</span></span> <span data-ttu-id="4bfc1-182">세그먼트 또는 정책 정의를 시작 하기 전에이 작업을 수행 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="4bfc1-182">We recommend doing this before you begin to define segments or policies.</span></span> <span data-ttu-id="4bfc1-183">자세한 내용은 [Turn Office 365 감사 로그 검색 설정 또는 해제](turn-audit-log-search-on-or-off.md)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="4bfc1-183">To learn more, see [Turn Office 365 audit log search on or off](turn-audit-log-search-on-or-off.md).</span></span>

### <a name="powershell"></a><span data-ttu-id="4bfc1-184">PowerShell</span><span class="sxs-lookup"><span data-stu-id="4bfc1-184">PowerShell</span></span>

<span data-ttu-id="4bfc1-185">**현재 정보 장벽 정책은 PowerShell cmdlet을 사용 하 여 Office 365 보안 & 준수 센터에서 정의 되 고 관리 됩니다**.</span><span class="sxs-lookup"><span data-stu-id="4bfc1-185">**Currently, information barrier policies are defined and managed in the Office 365 Security & Compliance Center using PowerShell cmdlets**.</span></span> <span data-ttu-id="4bfc1-186">이 문서에서는 몇 가지 시나리오와 예를 제공 했지만 PowerShell cmdlet 및 매개 변수에 익숙해져야 합니다.</span><span class="sxs-lookup"><span data-stu-id="4bfc1-186">Although several scenarios and examples are provided in this article, you'll need to be familiar with PowerShell cmdlets and parameters.</span></span> 

<span data-ttu-id="4bfc1-187">[Office 365 보안 & 준수 센터 PowerShell에 연결](https://docs.microsoft.com/powershell/exchange/office-365-scc/connect-to-scc-powershell/connect-to-scc-powershell?view=exchange-ps)합니다.</span><span class="sxs-lookup"><span data-stu-id="4bfc1-187">[Connect to Office 365 Security & Compliance Center PowerShell](https://docs.microsoft.com/powershell/exchange/office-365-scc/connect-to-scc-powershell/connect-to-scc-powershell?view=exchange-ps).</span></span>

### <a name="provide-admin-consent-for-information-barriers-in-microsoft-teams"></a><span data-ttu-id="4bfc1-188">Microsoft 팀에서 정보 장벽에 대 한 관리자 동의 제공</span><span class="sxs-lookup"><span data-stu-id="4bfc1-188">Provide admin consent for information barriers in Microsoft Teams</span></span>

<span data-ttu-id="4bfc1-189">다음 절차를 사용 하 여 정보 장벽 정책이 Microsoft 팀에서 예상 대로 작동 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4bfc1-189">Use the following procedure to enable information barrier policies to work as expected in Microsoft Teams.</span></span> 

<span data-ttu-id="4bfc1-190">예를 들어 정책이 적용 된 경우 정보 장애물은에는 없는 채팅 세션에서 사용자를 제거할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4bfc1-190">For example, when your policies are in place, information barriers can remove people from chat sessions they are not supposed to be in.</span></span> <span data-ttu-id="4bfc1-191">이렇게 하면 조직이 정책 및 규정 준수 상태를 유지할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4bfc1-191">This helps ensure your organization remains compliant with policies and regulations.</span></span> 

1. <span data-ttu-id="4bfc1-192">다음 PowerShell cmdlet을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="4bfc1-192">Run the following PowerShell cmdlets:</span></span>

    ```
    Login-AzureRmAccount 
    $appId="bcf62038-e005-436d-b970-2a472f8c1982" 
    $sp=Get-AzureRmADServicePrincipal -ServicePrincipalName $appId
    if ($sp -eq $null) { New-AzureRmADServicePrincipal -ApplicationId $appId }
    Start-Process  "https://login.microsoftonline.com/common/adminconsent?client_id=$appId"
    ```

2. <span data-ttu-id="4bfc1-193">메시지가 나타나면 Office 365에 대 한 회사 또는 학교 계정을 사용 하 여 로그인 합니다.</span><span class="sxs-lookup"><span data-stu-id="4bfc1-193">When prompted, sign in using your work or school account for Office 365.</span></span>

3. <span data-ttu-id="4bfc1-194">요청 된 **사용 권한** 대화 상자에서 정보를 검토 하 고 **수락**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="4bfc1-194">In the **Permissions requested** dialog box, review the information, and then choose **Accept**.</span></span>

## <a name="part-1-segment-users"></a><span data-ttu-id="4bfc1-195">1 부: 사용자 분할</span><span class="sxs-lookup"><span data-stu-id="4bfc1-195">Part 1: Segment users</span></span>

<span data-ttu-id="4bfc1-196">이 단계에서는 필요한 정책을 확인 하 고 정의할 세그먼트 목록을 만든 다음 세그먼트를 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="4bfc1-196">During this phase, you determine what policies are needed, make a list of segments to define, and then define your segments.</span></span>

### <a name="determine-what-policies-are-needed"></a><span data-ttu-id="4bfc1-197">필요한 정책 결정</span><span class="sxs-lookup"><span data-stu-id="4bfc1-197">Determine what policies are needed</span></span>

<span data-ttu-id="4bfc1-198">정보 장벽 정책이 필요한 조직 내의 그룹 인 법률 및 업계 규정을 고려 하 고 계십니까?</span><span class="sxs-lookup"><span data-stu-id="4bfc1-198">Considering legal and industry regulations, who are the groups within your organization who will need information barrier policies?</span></span> <span data-ttu-id="4bfc1-199">목록을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="4bfc1-199">Make a list.</span></span> <span data-ttu-id="4bfc1-200">다른 그룹과 통신을 차단 해야 하는 그룹이 있습니까?</span><span class="sxs-lookup"><span data-stu-id="4bfc1-200">Are there any groups who should be prevented from communicating with another group?</span></span> <span data-ttu-id="4bfc1-201">하나 또는 두 개의 다른 그룹과만 통신 하도록 허용 해야 하는 그룹이 있습니까?</span><span class="sxs-lookup"><span data-stu-id="4bfc1-201">Are there any groups that should be allowed to communicate only with one or two other groups?</span></span> <span data-ttu-id="4bfc1-202">다음은 두 그룹 중 하나에 속하는 것으로 필요한 정책을 고려 합니다.</span><span class="sxs-lookup"><span data-stu-id="4bfc1-202">Think about the policies you need as belonging to one of two groups:</span></span>
- <span data-ttu-id="4bfc1-203">한 그룹이 다른 그룹과 통신 하지 못하게 하는 **차단 정책**</span><span class="sxs-lookup"><span data-stu-id="4bfc1-203">**Blocking policies** that prevent one group from communicating with another group</span></span>
- <span data-ttu-id="4bfc1-204">특정 그룹이 다른 특정 그룹과 통신 하도록 허용 하는 **정책 허용**</span><span class="sxs-lookup"><span data-stu-id="4bfc1-204">**Allow policies** that allow certain groups to communicate with only certain other groups.</span></span>

<span data-ttu-id="4bfc1-205">초기 그룹 및 정책 목록이 있으면 필요한 세그먼트를 확인 하기 위해 계속 진행 합니다.</span><span class="sxs-lookup"><span data-stu-id="4bfc1-205">When you have your initial list of groups and policies, proceed to identify the segments you'll need.</span></span>

<span data-ttu-id="4bfc1-206">( [예:이 문서의 Contoso 부서 및 계획](#contosos-departments-and-plan) 을 참조 하세요.)</span><span class="sxs-lookup"><span data-stu-id="4bfc1-206">(See [Example: Contoso's departments and plan](#contosos-departments-and-plan) in this article.)</span></span>

### <a name="identify-segments"></a><span data-ttu-id="4bfc1-207">세그먼트 식별</span><span class="sxs-lookup"><span data-stu-id="4bfc1-207">Identify segments</span></span>

<span data-ttu-id="4bfc1-208">초기 정책 목록 외에, 조직의 세그먼트 목록을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="4bfc1-208">In addition to your initial list of policies, make a list of segments for your organization.</span></span> <span data-ttu-id="4bfc1-209">조직의 모든 사용자는 세그먼트에 속해야 하며, 사용자는 두 개 이상의 세그먼트에 속해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="4bfc1-209">Every user in your organization should belong to a segment, and no user should belong to two or more segments.</span></span> <span data-ttu-id="4bfc1-210">각 세그먼트에는 하나의 정보 장벽 정책만 적용 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4bfc1-210">Each segment can have only one information barrier policy applied.</span></span> 

<span data-ttu-id="4bfc1-211">세그먼트를 정의 하는 데 사용할 조직의 디렉터리 데이터 특성을 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4bfc1-211">Determine which attributes in your organization's directory data you'll use to define segments.</span></span> <span data-ttu-id="4bfc1-212">*부서*, *MemberOf*또는 지원 되는 특성을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4bfc1-212">You can use *Department*, *MemberOf*, or any of the supported attributes.</span></span> <span data-ttu-id="4bfc1-213">모든 사용자에 대해 선택한 특성 값이 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="4bfc1-213">Make sure that you have values in the attribute you select for all users.</span></span> <span data-ttu-id="4bfc1-214">지원 되는 특성 목록을 보려면 [information 장벽 정책에 대 한 특성 (미리 보기)](information-barriers-attributes.md)을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="4bfc1-214">To see a list of supported attributes, refer to [Attributes for information barrier policies (Preview)](information-barriers-attributes.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4bfc1-215">**다음 섹션을 진행 하기 전에 디렉터리 데이터에 세그먼트를 정의 하는 데 사용할 수 있는 특성 값이 있는지 확인**합니다.</span><span class="sxs-lookup"><span data-stu-id="4bfc1-215">**Before you proceed to the next section, make sure your directory data has values for attributes that you can use to define segments**.</span></span> <span data-ttu-id="4bfc1-216">디렉터리 데이터에 사용 하려는 특성의 값이 없는 경우에는 정보 장애물을 계속 하기 전에 해당 정보를 포함 하도록 모든 사용자 계정을 업데이트 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="4bfc1-216">If your directory data does not have values for the attributes you want to use, then all user accounts must be updated to include that information before you proceed with information barriers.</span></span> <span data-ttu-id="4bfc1-217">이에 대 한 도움말을 보려면 다음 리소스를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="4bfc1-217">To get help with this, see the following resources:</span></span><br/><span data-ttu-id="4bfc1-218">- [Office 365 PowerShell을 사용 하 여 사용자 계정 속성 구성](https://docs.microsoft.com/office365/enterprise/powershell/configure-user-account-properties-with-office-365-powershell)</span><span class="sxs-lookup"><span data-stu-id="4bfc1-218">- [Configure user account properties with Office 365 PowerShell](https://docs.microsoft.com/office365/enterprise/powershell/configure-user-account-properties-with-office-365-powershell)</span></span><br/><span data-ttu-id="4bfc1-219">- [Azure Active Directory를 사용 하 여 사용자 프로필 정보 추가 또는 업데이트](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-users-profile-azure-portal)</span><span class="sxs-lookup"><span data-stu-id="4bfc1-219">- [Add or update a user's profile information using Azure Active Directory](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-users-profile-azure-portal)</span></span>

### <a name="define-segments-using-powershell"></a><span data-ttu-id="4bfc1-220">PowerShell을 사용 하 여 세그먼트 정의</span><span class="sxs-lookup"><span data-stu-id="4bfc1-220">Define segments using PowerShell</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4bfc1-221">**세그먼트가 겹치지 않는지 확인**합니다.</span><span class="sxs-lookup"><span data-stu-id="4bfc1-221">**Make sure that your segments do not overlap**.</span></span> <span data-ttu-id="4bfc1-222">조직의 각 사용자는 하나의 세그먼트에만 속해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="4bfc1-222">Each user in your organization should belong to one (and only one) segment.</span></span> <span data-ttu-id="4bfc1-223">두 개 이상의 세그먼트에 속해야 하는 사용자가 없습니다.</span><span class="sxs-lookup"><span data-stu-id="4bfc1-223">No user should belong to two or more segments.</span></span> <span data-ttu-id="4bfc1-224">세그먼트는 조직의 모든 사용자에 대해 정의 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="4bfc1-224">Segments should be defined for all users in your organization.</span></span> <span data-ttu-id="4bfc1-225">(예제:이 문서에 나와 있는 [Contoso의 정의 된 세그먼트](#contosos-defined-segments) 참조)</span><span class="sxs-lookup"><span data-stu-id="4bfc1-225">(See [Example: Contoso's defined segments](#contosos-defined-segments) in this article.)</span></span>

1. <span data-ttu-id="4bfc1-226">조직 세그먼트를 정의 하려면 사용 하려는 [특성](information-barriers-attributes.md) 에 해당 하는 **usergroupfilter** 매개 변수와 함께 **OrganizationSegment** cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="4bfc1-226">To define an organizational segment, use the **New-OrganizationSegment** cmdlet with the **UserGroupFilter** parameter that corresponds to the [attribute](information-barriers-attributes.md) you want to use.</span></span> 

    <span data-ttu-id="4bfc1-227">구문과`New-OrganizationSegment -Name "segmentname" -UserGroupFilter "attribute -eq 'attributevalue'"`</span><span class="sxs-lookup"><span data-stu-id="4bfc1-227">Syntax: `New-OrganizationSegment -Name "segmentname" -UserGroupFilter "attribute -eq 'attributevalue'"`</span></span>

    <span data-ttu-id="4bfc1-228">예제: `New-OrganizationSegment -Name "HR" -UserGroupFilter "Department -eq 'HR'"`</span><span class="sxs-lookup"><span data-stu-id="4bfc1-228">Example: `New-OrganizationSegment -Name "HR" -UserGroupFilter "Department -eq 'HR'"`</span></span>

    <span data-ttu-id="4bfc1-229">이 예제에서는 hr을 사용 하 \*\* 여 인사부 라는 세그먼트 \*\* 를 정의 하 고 부서 특성에 값을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4bfc1-229">In this example, a segment called *HR* is defined using *HR*, a value in the Department attribute.</span></span>

2. <span data-ttu-id="4bfc1-230">정의 하려는 각 세그먼트에 대해 1 단계를 반복 합니다.</span><span class="sxs-lookup"><span data-stu-id="4bfc1-230">Repeat step 1 for each segment you want to define.</span></span>

    <span data-ttu-id="4bfc1-231">각 cmdlet을 실행 하면 새 세그먼트에 대 한 세부 정보 목록이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4bfc1-231">After you run each cmdlet, you should see a list of details about the new segment.</span></span> <span data-ttu-id="4bfc1-232">세부 정보에는 세그먼트의 유형, 작성자가 작성 하거나 마지막으로 수정한 사람 등이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4bfc1-232">Details include the segment's type, who created or last modified it, and so on.</span></span> 

<span data-ttu-id="4bfc1-233">세그먼트를 정의한 후에는 정보 장벽 정책 정의로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="4bfc1-233">After you have defined your segments, proceed to define information barrier policies.</span></span>

## <a name="part-2-define-information-barrier-policies"></a><span data-ttu-id="4bfc1-234">2 부: 정보 장벽 정책 정의</span><span class="sxs-lookup"><span data-stu-id="4bfc1-234">Part 2: Define information barrier policies</span></span>

<span data-ttu-id="4bfc1-235">사용자 세그먼트 목록과 정의할 정보 장벽 정책을 사용 하 여 시나리오를 선택한 다음 단계를 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="4bfc1-235">With your list of user segments and the information barrier policies you want to define, select a scenario, and then follow the steps.</span></span> 

> [!IMPORTANT]
> <span data-ttu-id="4bfc1-236">**정책을 정의할 때 세그먼트에 두 개 이상의 정책을 할당 하지**않도록 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="4bfc1-236">**Make sure that as you define policies, you do not assign more than one policy to a segment**.</span></span> <span data-ttu-id="4bfc1-237">예를 들어 *sales*라는 세그먼트에 대해 하나의 정책을 정의 하는 경우에는 *sales*에 대 한 추가 정책을 정의 하지 마십시오.</span><span class="sxs-lookup"><span data-stu-id="4bfc1-237">For example, if you define one policy for a segment called *Sales*, do not define an additional policy for *Sales*.</span></span> 

<span data-ttu-id="4bfc1-238">특정 세그먼트 간 통신을 방지 해야 하는지 또는 특정 세그먼트에 대 한 통신을 제한할지 여부를 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4bfc1-238">Determine whether you need to prevent communications between certain segments, or limit communications to certain segments.</span></span> <span data-ttu-id="4bfc1-239">아래 시나리오 중에서 하나를 선택 하 여 정책을 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="4bfc1-239">Choose between the scenarios below to define your policies.</span></span>

- [<span data-ttu-id="4bfc1-240">시나리오 1: 세그먼트 간 통신 차단</span><span class="sxs-lookup"><span data-stu-id="4bfc1-240">Scenario 1: Block communications between segments</span></span>](#scenario-1-block-communications-between-segments)
- [<span data-ttu-id="4bfc1-241">시나리오 2: 특정 세그먼트가 다른 세그먼트와만 통신할 수 있도록 허용</span><span class="sxs-lookup"><span data-stu-id="4bfc1-241">Scenario 2: Allow a segment to communicate only with one other segment</span></span>](#scenario-2-allow-a-segment-to-communicate-only-with-one-other-segment)

> [!NOTE]
> <span data-ttu-id="4bfc1-242">정보 장벽 정책을 정의할 때 이러한 정책을 적용할 준비가 될 때까지이를 비활성 상태로 설정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="4bfc1-242">As you define information barrier policies, make sure to set those policies to inactive status until you are ready to apply them.</span></span> <span data-ttu-id="4bfc1-243">정책 정의 (또는 편집)는 해당 정책이 활성 상태로 설정 된 후에 야 사용자에 게 영향을 줍니다.</span><span class="sxs-lookup"><span data-stu-id="4bfc1-243">Defining (or editing) policies does not affect users until those policies are set to active status and then applied.</span></span>

<span data-ttu-id="4bfc1-244">(이 문서의 [예: Contoso의 정보 장벽 정책](#contosos-information-barrier-policies) 참조)</span><span class="sxs-lookup"><span data-stu-id="4bfc1-244">(See [Example: Contoso's information barrier policies](#contosos-information-barrier-policies) in this article.)</span></span>

### <a name="scenario-1-block-communications-between-segments"></a><span data-ttu-id="4bfc1-245">시나리오 1: 세그먼트 간 통신 차단</span><span class="sxs-lookup"><span data-stu-id="4bfc1-245">Scenario 1: Block communications between segments</span></span>

<span data-ttu-id="4bfc1-246">세그먼트 간의 통신을 차단 하려는 경우 각 방향에 하나씩 두 개의 정책을 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="4bfc1-246">When you want to block segments from communicating with each other, you define two policies: one for each direction.</span></span> <span data-ttu-id="4bfc1-247">각 정책은 통신을 단방향 으로만 차단 합니다.</span><span class="sxs-lookup"><span data-stu-id="4bfc1-247">Each policy blocks communication one way only.</span></span>

<span data-ttu-id="4bfc1-248">예를 들어 세그먼트 A와 세그먼트 B 간의 통신을 차단 하려는 경우를 가정해 보겠습니다. 이 경우 세그먼트 A가 세그먼트 B와 통신 하는 것을 방지 하는 정책을 하나 정의한 다음, 두 번째 정책을 정의 하 여 세그먼트 B가 세그먼트 A와 통신 하는 것을 방지 합니다.</span><span class="sxs-lookup"><span data-stu-id="4bfc1-248">For example, suppose you want to block communications between Segment A and Segment B. In this case, you define one policy preventing Segment A from communicating with Segment B, and then define a second policy to prevent Segment B from communicating with Segment A.</span></span>

1. <span data-ttu-id="4bfc1-249">첫 번째 차단 정책을 정의 하려면 **InformationBarrierPolicy** Cmdlet에 **SegmentsBlocked** 매개 변수를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="4bfc1-249">To define your first blocking policy, use the **New-InformationBarrierPolicy** cmdlet with the **SegmentsBlocked** parameter.</span></span> 

    <span data-ttu-id="4bfc1-250">구문과`New-InformationBarrierPolicy -Name "policyname" -AssignedSegment "segmentname" -SegmentsBlocked "segmentname"`</span><span class="sxs-lookup"><span data-stu-id="4bfc1-250">Syntax: `New-InformationBarrierPolicy -Name "policyname" -AssignedSegment "segmentname" -SegmentsBlocked "segmentname"`</span></span>

    <span data-ttu-id="4bfc1-251">예제: `New-InformationBarrierPolicy -Name "Sales-Research" -AssignedSegment "Sales" -SegmentsBlocked "Research" -State Inactive`</span><span class="sxs-lookup"><span data-stu-id="4bfc1-251">Example: `New-InformationBarrierPolicy -Name "Sales-Research" -AssignedSegment "Sales" -SegmentsBlocked "Research" -State Inactive`</span></span>

    <span data-ttu-id="4bfc1-252">이 예에서는 *sales*라는 세그먼트에 대 한 *영업 조사* 라는 정책을 정의 했습니다.</span><span class="sxs-lookup"><span data-stu-id="4bfc1-252">In this example, we defined a policy called *Sales-Research* for a segment called *Sales*.</span></span> <span data-ttu-id="4bfc1-253">이 정책을 사용 하면 *영업* 직원이 *조사*라는 세그먼트에 있는 사람들과 통신할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="4bfc1-253">When active and applied, this policy prevents people in *Sales* from communicating with people in a segment called *Research*.</span></span>

2. <span data-ttu-id="4bfc1-254">두 번째 차단 세그먼트를 정의 하려면 **SegmentsBlocked** 매개 변수와 함께 **InformationBarrierPolicy** cmdlet을 사용 하 여 세그먼트를 거꾸로 된 상태로 다시 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4bfc1-254">To define your second blocking segment, use the **New-InformationBarrierPolicy** cmdlet with the **SegmentsBlocked** parameter again, this time with the segments reversed.</span></span>

    <span data-ttu-id="4bfc1-255">예제: `New-InformationBarrierPolicy -Name "Research-Sales" -AssignedSegment "Research" -SegmentsBlocked "Sales" -State Inactive`</span><span class="sxs-lookup"><span data-stu-id="4bfc1-255">Example: `New-InformationBarrierPolicy -Name "Research-Sales" -AssignedSegment "Research" -SegmentsBlocked "Sales" -State Inactive`</span></span>

    <span data-ttu-id="4bfc1-256">이 예에서는 연구가 영업과의 통신을 방지 하기 위해 *research-Sales* 라는 정책을 정의 했습니다.</span><span class="sxs-lookup"><span data-stu-id="4bfc1-256">In this example, we defined a policy called *Research-Sales* to prevent Research from communicating with Sales.</span></span>
 
2. <span data-ttu-id="4bfc1-257">다음 중 하나로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="4bfc1-257">Proceed to one of the following:</span></span>

   - <span data-ttu-id="4bfc1-258">(필요한 경우) [다른 세그먼트 하나로만 통신할 수 있도록 정책 정의](#scenario-2-allow-a-segment-to-communicate-only-with-one-other-segment)</span><span class="sxs-lookup"><span data-stu-id="4bfc1-258">(If needed) [Define a policy to allow a segment to communicate only with one other segment](#scenario-2-allow-a-segment-to-communicate-only-with-one-other-segment)</span></span> 
   - <span data-ttu-id="4bfc1-259">(모든 정책이 정의 된 후) [정보 장벽 정책 적용](#part-3-apply-information-barrier-policies)</span><span class="sxs-lookup"><span data-stu-id="4bfc1-259">(After all your policies are defined) [Apply information barrier policies](#part-3-apply-information-barrier-policies)</span></span>

### <a name="scenario-2-allow-a-segment-to-communicate-only-with-one-other-segment"></a><span data-ttu-id="4bfc1-260">시나리오 2: 특정 세그먼트가 다른 세그먼트와만 통신할 수 있도록 허용</span><span class="sxs-lookup"><span data-stu-id="4bfc1-260">Scenario 2: Allow a segment to communicate only with one other segment</span></span>

1. <span data-ttu-id="4bfc1-261">하나의 세그먼트가 다른 하나의 세그먼트와만 통신할 수 있도록 하려면 **SegmentsAllowed** 매개 변수와 함께 **InformationBarrierPolicy** cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="4bfc1-261">To allow one segment to communicate with only one other segment, use the **New-InformationBarrierPolicy** cmdlet with the **SegmentsAllowed** parameter.</span></span> 

    <span data-ttu-id="4bfc1-262">구문과`New-InformationBarrierPolicy -Name "policyname" -AssignedSegment "segmentname" -SegmentsAllowed "segmentname"`</span><span class="sxs-lookup"><span data-stu-id="4bfc1-262">Syntax: `New-InformationBarrierPolicy -Name "policyname" -AssignedSegment "segmentname" -SegmentsAllowed "segmentname"`</span></span>

    <span data-ttu-id="4bfc1-263">예제: `New-InformationBarrierPolicy -Name "Manufacturing-HR" -AssignedSegment "Manufacturing" -SegmentsAllowed "HR" -State Inactive`</span><span class="sxs-lookup"><span data-stu-id="4bfc1-263">Example: `New-InformationBarrierPolicy -Name "Manufacturing-HR" -AssignedSegment "Manufacturing" -SegmentsAllowed "HR" -State Inactive`</span></span>

    <span data-ttu-id="4bfc1-264">이 예에서는 *manufacturing*이라는 세그먼트에 대해 *제조-HR* 이라는 정책을 정의 했습니다.</span><span class="sxs-lookup"><span data-stu-id="4bfc1-264">In this example, we defined a policy called *Manufacturing-HR* for a segment called *Manufacturing*.</span></span> <span data-ttu-id="4bfc1-265">이 정책을 사용 하면 *제조* 중인 사용자가 *HR*이라는 세그먼트에 있는 사용자와만 통신할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4bfc1-265">When active and applied, this policy allows people in *Manufacturing* to communicate only with people in a segment called *HR*.</span></span> <span data-ttu-id="4bfc1-266">(이 경우, Manufacturing은 HR에 속하지 않는 사용자와 통신할 수 없습니다.)</span><span class="sxs-lookup"><span data-stu-id="4bfc1-266">(In this case, Manufacturing cannot communicate with users who are not part of HR.)</span></span>

    <span data-ttu-id="4bfc1-267">**필요한 경우 다음의 두 예에 표시 된 것 처럼이 cmdlet을 사용 하 여 여러 세그먼트를 지정할 수 있습니다.**</span><span class="sxs-lookup"><span data-stu-id="4bfc1-267">**If needed, you can specify multiple segments with this cmdlet, as shown in the following two examples.**</span></span>

    <span data-ttu-id="4bfc1-268">구문과`New-InformationBarrierPolicy -Name "policyname" -AssignedSegment "segmentname" -SegmentsAllowed "segmentname, segmentname"`</span><span class="sxs-lookup"><span data-stu-id="4bfc1-268">Syntax: `New-InformationBarrierPolicy -Name "policyname" -AssignedSegment "segmentname" -SegmentsAllowed "segmentname, segmentname"`</span></span>

    <span data-ttu-id="4bfc1-269">**예 1: 여러 세그먼트가 다른 세그먼트 한 개와만 통신할 수 있도록 하는 정책 정의**</span><span class="sxs-lookup"><span data-stu-id="4bfc1-269">**Example 1: Define a policy to allow multiple segments to communicate with only one other segment**</span></span>

    `New-InformationBarrierPolicy -Name "ResearchManufacturing-HR" -AssignedSegment "Research, Manufacturing" -SegmentsAllowed "HR" -State Inactive`

    <span data-ttu-id="4bfc1-270">이 예에서는 *연구* 및 *제조* 부문에서 *HR*과의 통신을 허용 하는 정책을 정의 했습니다.</span><span class="sxs-lookup"><span data-stu-id="4bfc1-270">In this example, we defined a policy that allows the *Research* and *Manufacturing* segments to communicate only with *HR*.</span></span>

    <span data-ttu-id="4bfc1-271">**예 2: 여러 세그먼트가 특정 다른 세그먼트와도 통신할 수 있도록 정책을 정의 합니다.**</span><span class="sxs-lookup"><span data-stu-id="4bfc1-271">**Example 2: Define a policy to allow multiple segments to communicate with only certain other segments**</span></span>    

    `New-InformationBarrierPolicy -Name "SalesMarketing-HRManufacturing" -AssignedSegment "Sales, Marketing" -SegmentsAllowed "HR, Manufacturing" -State Inactive`

    <span data-ttu-id="4bfc1-272">이 예에서는 *영업* 및 *마케팅* 세그먼트가 *HR* 및 *제조*와도 통신할 수 있도록 하는 정책을 정의 했습니다.</span><span class="sxs-lookup"><span data-stu-id="4bfc1-272">In this example, we defined a policy that allows the *Sales* and *Marketing* segments to communicate with only *HR* and *Manufacturing*.</span></span>

    <span data-ttu-id="4bfc1-273">특정 세그먼트가 다른 특정 세그먼트와만 통신할 수 있도록 정의 하려는 각 정책에 대해이 단계를 반복 합니다.</span><span class="sxs-lookup"><span data-stu-id="4bfc1-273">Repeat this step for each policy you want to define to allow specific segments to communicate with only certain other specific segments.</span></span>

2. <span data-ttu-id="4bfc1-274">다음 중 하나로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="4bfc1-274">Proceed to one of the following:</span></span>

   - <span data-ttu-id="4bfc1-275">(필요한 경우) [세그먼트 간 통신을 차단 하는 정책 정의](#scenario-1-block-communications-between-segments)</span><span class="sxs-lookup"><span data-stu-id="4bfc1-275">(If needed) [Define a policy to block communications between segments](#scenario-1-block-communications-between-segments)</span></span> 
   - <span data-ttu-id="4bfc1-276">(모든 정책이 정의 된 후) [정보 장벽 정책 적용](#part-3-apply-information-barrier-policies)</span><span class="sxs-lookup"><span data-stu-id="4bfc1-276">(After all your policies are defined) [Apply information barrier policies](#part-3-apply-information-barrier-policies)</span></span>

## <a name="part-3-apply-information-barrier-policies"></a><span data-ttu-id="4bfc1-277">3 부: 정보 장벽 정책 적용</span><span class="sxs-lookup"><span data-stu-id="4bfc1-277">Part 3: Apply information barrier policies</span></span>

<span data-ttu-id="4bfc1-278">정보 장벽 정책은 활성 상태로 설정 하 고 정책을 적용할 때까지 적용 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4bfc1-278">Information barrier policies are not in effect until you set them to active status, and then apply the policies.</span></span>

1. <span data-ttu-id="4bfc1-279">**InformationBarrierPolicy** cmdlet을 사용 하 여 정의 된 정책 목록을 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4bfc1-279">Use the **Get-InformationBarrierPolicy** cmdlet to see a list of policies that have been defined.</span></span> <span data-ttu-id="4bfc1-280">각 정책의 상태 및 id (GUID)를 적어둡니다.</span><span class="sxs-lookup"><span data-stu-id="4bfc1-280">Note the status and identity (GUID) of each policy.</span></span>

    <span data-ttu-id="4bfc1-281">구문과`Get-InformationBarrierPolicy`</span><span class="sxs-lookup"><span data-stu-id="4bfc1-281">Syntax: `Get-InformationBarrierPolicy`</span></span>

2. <span data-ttu-id="4bfc1-282">정책을 활성 상태로 설정 하려면 **Identity** 매개 변수와 함께 **InformationBarrierPolicy** cmdlet을 사용 하 고 **State** 매개 변수를 **active**로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4bfc1-282">To set a policy to active status, use the **Set-InformationBarrierPolicy** cmdlet with an **Identity** parameter, and the **State** parameter set to **Active**.</span></span> 

    <span data-ttu-id="4bfc1-283">구문과`Set-InformationBarrierPolicy -Identity GUID -State Active`</span><span class="sxs-lookup"><span data-stu-id="4bfc1-283">Syntax: `Set-InformationBarrierPolicy -Identity GUID -State Active`</span></span>

    <span data-ttu-id="4bfc1-284">예제: `Set-InformationBarrierPolicy -Identity 43c37853-ea10-4b90-a23d-ab8c93772471 -State Active`</span><span class="sxs-lookup"><span data-stu-id="4bfc1-284">Example: `Set-InformationBarrierPolicy -Identity 43c37853-ea10-4b90-a23d-ab8c93772471 -State Active`</span></span>
    
    <span data-ttu-id="4bfc1-285">이 예에서는 GUID가 *43c37853-ea10-4b90-a23d-ab8c93772471* 인 정보 장벽 정책을 active status로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4bfc1-285">In this example, we set an information barrier policy that has the GUID *43c37853-ea10-4b90-a23d-ab8c93772471* to active status.</span></span>

    <span data-ttu-id="4bfc1-286">각 정책에 대해 적절 하 게이 단계를 반복 합니다.</span><span class="sxs-lookup"><span data-stu-id="4bfc1-286">Repeat this step as appropriate for each policy.</span></span>

3. <span data-ttu-id="4bfc1-287">정보 장벽 정책 설정이 활성 상태로 끝나면 Office 365 보안 & 준수 센터의 **InformationBarrierPoliciesApplication** cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="4bfc1-287">When you have finished setting your information barrier policies to active status, use the **Start-InformationBarrierPoliciesApplication** cmdlet in the Office 365 Security & Compliance Center.</span></span>

    <span data-ttu-id="4bfc1-288">구문과`Start-InformationBarrierPoliciesApplication`</span><span class="sxs-lookup"><span data-stu-id="4bfc1-288">Syntax: `Start-InformationBarrierPoliciesApplication`</span></span>

    <span data-ttu-id="4bfc1-289">약 1 시간 후에는 조직에 대해 사용자에 게 정책이 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4bfc1-289">After approximately a half hour, policies are applied, user by user, for your organization.</span></span> <span data-ttu-id="4bfc1-290">대규모 조직에서는이 프로세스를 완료 하는 데 24 시간 이상 소요 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4bfc1-290">If your organization is large, it can take 24 hours (or more) for this process to complete.</span></span> <span data-ttu-id="4bfc1-291">일반적으로 5000 사용자 계정을 처리 하는 데 한 시간 정도 소요 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4bfc1-291">(As a general guideline, it takes about an hour to process 5,000 user accounts.)</span></span>

## <a name="verify-status-of-user-accounts-segments-policies-or-policy-application"></a><span data-ttu-id="4bfc1-292">사용자 계정, 세그먼트, 정책 또는 정책 응용 프로그램의 상태 확인</span><span class="sxs-lookup"><span data-stu-id="4bfc1-292">Verify status of user accounts, segments, policies, or policy application</span></span>

<span data-ttu-id="4bfc1-293">PowerShell을 사용 하 여 다음 표에 나와 있는 것 처럼 사용자 계정, 세그먼트, 정책 및 정책 응용 프로그램의 상태를 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4bfc1-293">Using PowerShell, you can verify status of user accounts, segments, policies, and policy application, as listed in the following table.</span></span>

|<span data-ttu-id="4bfc1-294">이를 확인 하려면</span><span class="sxs-lookup"><span data-stu-id="4bfc1-294">To verify this</span></span>  |<span data-ttu-id="4bfc1-295">수행 작업</span><span class="sxs-lookup"><span data-stu-id="4bfc1-295">Do this</span></span>  |
|---------|---------|
|<span data-ttu-id="4bfc1-296">사용자 계정</span><span class="sxs-lookup"><span data-stu-id="4bfc1-296">User accounts</span></span>     |<span data-ttu-id="4bfc1-297">Identity 매개 변수와 함께 **InformationBarrierRecipientStatus** cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="4bfc1-297">Use the **Get-InformationBarrierRecipientStatus** cmdlet with Identity parameters.</span></span> <p><span data-ttu-id="4bfc1-298">구문과`Get-InformationBarrierRecipientStatus -Identity <value> -Identity2 <value>`</span><span class="sxs-lookup"><span data-stu-id="4bfc1-298">Syntax: `Get-InformationBarrierRecipientStatus -Identity <value> -Identity2 <value>`</span></span> <p><span data-ttu-id="4bfc1-299">이름, 별칭, 고유 이름, 정식 도메인 이름, 전자 메일 주소 또는 GUID와 같은 각 사용자를 고유 하 게 식별 하는 모든 값을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4bfc1-299">You can use any value that uniquely identifies each user, such as name, alias, distinguished name, canonical domain name, email address, or GUID.</span></span> <p><span data-ttu-id="4bfc1-300">예제: `Get-InformationBarrierRecipientStatus -Identity meganb -Identity2 alexw`</span><span class="sxs-lookup"><span data-stu-id="4bfc1-300">Example: `Get-InformationBarrierRecipientStatus -Identity meganb -Identity2 alexw`</span></span> <p><span data-ttu-id="4bfc1-301">이 예에서는 Office 365의 두 사용자 계정 ( *Megan*용 *meganb* 및 *Alex*용 *alexw* )을 참조 합니다.</span><span class="sxs-lookup"><span data-stu-id="4bfc1-301">In this example, we refer to two user accounts in Office 365: *meganb* for *Megan*, and *alexw* for *Alex*.</span></span> <p><span data-ttu-id="4bfc1-302">(단일 사용자에 대해이 cmdlet을 사용할 수도 있습니다. `Get-InformationBarrierRecipientStatus -Identity <value>`)</span><span class="sxs-lookup"><span data-stu-id="4bfc1-302">(You can also use this cmdlet for a single user: `Get-InformationBarrierRecipientStatus -Identity <value>`)</span></span> <p><span data-ttu-id="4bfc1-303">이 cmdlet은 특성 값 및 적용 되는 정보 장벽 정책과 같은 사용자에 대 한 정보를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="4bfc1-303">This cmdlet returns information about users, such as attribute values and any information barrier policies that are applied.</span></span>|
|<span data-ttu-id="4bfc1-304">세그먼트</span><span class="sxs-lookup"><span data-stu-id="4bfc1-304">Segments</span></span>     |<span data-ttu-id="4bfc1-305">**OrganizationSegment** cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="4bfc1-305">Use the **Get-OrganizationSegment** cmdlet.</span></span><p><span data-ttu-id="4bfc1-306">구문과`Get-OrganizationSegment`</span><span class="sxs-lookup"><span data-stu-id="4bfc1-306">Syntax: `Get-OrganizationSegment`</span></span> <p><span data-ttu-id="4bfc1-307">이렇게 하면 조직에 대해 정의 된 모든 세그먼트의 목록이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4bfc1-307">This will display a list of all segments defined for your organization.</span></span>         |
|<span data-ttu-id="4bfc1-308">정보 장벽 정책</span><span class="sxs-lookup"><span data-stu-id="4bfc1-308">Information barrier policies</span></span>     |<span data-ttu-id="4bfc1-309">**InformationBarrierPolicy** cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="4bfc1-309">Use the **Get-InformationBarrierPolicy** cmdlet.</span></span> <p> <span data-ttu-id="4bfc1-310">구문과`Get-InformationBarrierPolicy`</span><span class="sxs-lookup"><span data-stu-id="4bfc1-310">Syntax: `Get-InformationBarrierPolicy`</span></span> <p><span data-ttu-id="4bfc1-311">이렇게 하면 정의 된 정보 장벽 정책 목록과 해당 상태가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4bfc1-311">This will display a list of information barrier policies that were defined, and their status.</span></span>       |
|<span data-ttu-id="4bfc1-312">가장 최근 정보 장벽 정책 응용 프로그램</span><span class="sxs-lookup"><span data-stu-id="4bfc1-312">The most recent information barrier policy application</span></span>     | <span data-ttu-id="4bfc1-313">**InformationBarrierPoliciesApplicationStatus** cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="4bfc1-313">Use the **Get-InformationBarrierPoliciesApplicationStatus** cmdlet.</span></span> <p><span data-ttu-id="4bfc1-314">구문과`Get-InformationBarrierPoliciesApplicationStatus`</span><span class="sxs-lookup"><span data-stu-id="4bfc1-314">Syntax: `Get-InformationBarrierPoliciesApplicationStatus`</span></span><p>    <span data-ttu-id="4bfc1-315">이렇게 하면 정책 응용 프로그램이 완료, 실패 또는 진행 중인지에 대 한 정보가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4bfc1-315">This will display information about whether policy application completed, failed, or is in progress.</span></span>       |
|<span data-ttu-id="4bfc1-316">모든 정보 장벽 정책 응용 프로그램</span><span class="sxs-lookup"><span data-stu-id="4bfc1-316">All information barrier policy applications</span></span>|<span data-ttu-id="4bfc1-317">하십시오`Get-InformationBarrierPoliciesApplicationStatus -All $true`</span><span class="sxs-lookup"><span data-stu-id="4bfc1-317">Use `Get-InformationBarrierPoliciesApplicationStatus -All $true`</span></span><p><span data-ttu-id="4bfc1-318">이렇게 하면 정책 응용 프로그램이 완료, 실패 또는 진행 중인지에 대 한 정보가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4bfc1-318">This will display information about whether policy application completed, failed, or is in progress.</span></span>|

## <a name="stop-a-policy-application"></a><span data-ttu-id="4bfc1-319">정책 응용 프로그램 중지</span><span class="sxs-lookup"><span data-stu-id="4bfc1-319">Stop a policy application</span></span>

<span data-ttu-id="4bfc1-320">정보 장벽 정책 적용을 시작 하 고 나면 해당 정책을 적용 하지 않으려면 다음 절차를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="4bfc1-320">If, after you have started applying information barrier policies, you want to stop those policies from being applied, use the following procedure.</span></span> <span data-ttu-id="4bfc1-321">프로세스를 시작 하는 데 약 30-35 분이 소요 됨을 염두에 두어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="4bfc1-321">Keep in mind that it will take approximately 30-35 minutes for the process to begin.</span></span>

1. <span data-ttu-id="4bfc1-322">가장 최근 정보 장벽 정책 응용 프로그램의 상태를 확인 하려면 **InformationBarrierPoliciesApplicationStatus** cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="4bfc1-322">To view the status of the most recent information barrier policy application, use the **Get-InformationBarrierPoliciesApplicationStatus** cmdlet.</span></span>

    <span data-ttu-id="4bfc1-323">구문과`Get-InformationBarrierPoliciesApplicationStatus`</span><span class="sxs-lookup"><span data-stu-id="4bfc1-323">Syntax: `Get-InformationBarrierPoliciesApplicationStatus`</span></span>

    <span data-ttu-id="4bfc1-324">응용 프로그램의 GUID를 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="4bfc1-324">Note the application's GUID.</span></span>

2. <span data-ttu-id="4bfc1-325">**InformationBarrierPoliciesApplication** Cmdlet을 Identity 매개 변수와 함께 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="4bfc1-325">Use the **Stop-InformationBarrierPoliciesApplication** cmdlet with an Identity parameter.</span></span>

    <span data-ttu-id="4bfc1-326">구문과`Stop-InformationBarrierPoliciesApplication -Identity GUID`</span><span class="sxs-lookup"><span data-stu-id="4bfc1-326">Syntax:  `Stop-InformationBarrierPoliciesApplication -Identity GUID`</span></span>

    <span data-ttu-id="4bfc1-327">예제: `InformationBarrierPoliciesApplication -Identity 46237888-12ca-42e3-a541-3fcb7b5231d1`</span><span class="sxs-lookup"><span data-stu-id="4bfc1-327">Example: `InformationBarrierPoliciesApplication -Identity 46237888-12ca-42e3-a541-3fcb7b5231d1`</span></span>

## <a name="edit-a-segment-or-a-policy"></a><span data-ttu-id="4bfc1-328">세그먼트 또는 정책 편집</span><span class="sxs-lookup"><span data-stu-id="4bfc1-328">Edit a segment or a policy</span></span>

### <a name="edit-a-segment"></a><span data-ttu-id="4bfc1-329">세그먼트 편집</span><span class="sxs-lookup"><span data-stu-id="4bfc1-329">Edit a segment</span></span>

1. <span data-ttu-id="4bfc1-330">모든 기존 세그먼트를 보려면 **OrganizationSegment** cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="4bfc1-330">To view all existing segments, use the **Get-OrganizationSegment** cmdlet.</span></span>
    
    <span data-ttu-id="4bfc1-331">구문과`Get-OrganizationSegment`</span><span class="sxs-lookup"><span data-stu-id="4bfc1-331">Syntax: `Get-OrganizationSegment`</span></span>

    <span data-ttu-id="4bfc1-332">세그먼트 유형, UserGroupFilter 값, 해당 개체를 만들거나 마지막으로 수정한 사람, GUID 등의 각 세그먼트와 세부 정보에 대 한 목록이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4bfc1-332">You will see a list of segments and details for each, such as segment type, its UserGroupFilter value, who created or last modified it, GUID, and so on.</span></span>

    > [!TIP]
    > <span data-ttu-id="4bfc1-333">나중에 참조 하기 위해 세그먼트 목록을 인쇄 하거나 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="4bfc1-333">Print or save your list of segments for reference later.</span></span> <span data-ttu-id="4bfc1-334">예를 들어 세그먼트를 편집 하려면 해당 이름을 확인 하거나 값을 식별 해야 합니다 (이는 Identity 매개 변수와 함께 사용 됨).</span><span class="sxs-lookup"><span data-stu-id="4bfc1-334">For example, if you want to edit a segment, you will need to know its name or identify value (this is used with the Identity parameter).</span></span>

2. <span data-ttu-id="4bfc1-335">세그먼트를 편집 하려면 **Identity** 매개 변수와 관련 세부 정보와 함께 **OrganizationSegment** cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="4bfc1-335">To edit a segment, use the **Set-OrganizationSegment** cmdlet with the **Identity** parameter and relevant details.</span></span> 

    <span data-ttu-id="4bfc1-336">구문과`Set-OrganizationSegment -Identity GUID -UserGroupFilter "attribute -eq 'attributevalue'"`</span><span class="sxs-lookup"><span data-stu-id="4bfc1-336">Syntax: `Set-OrganizationSegment -Identity GUID -UserGroupFilter "attribute -eq 'attributevalue'"`</span></span>

    <span data-ttu-id="4bfc1-337">예제: `Set-OrganizationSegment -Identity c96e0837-c232-4a8a-841e-ef45787d8fcd -UserGroupFilter "Department -eq 'HRDept'"`</span><span class="sxs-lookup"><span data-stu-id="4bfc1-337">Example: `Set-OrganizationSegment -Identity c96e0837-c232-4a8a-841e-ef45787d8fcd -UserGroupFilter "Department -eq 'HRDept'"`</span></span>

    <span data-ttu-id="4bfc1-338">이 예에서는 GUID가 *c96e0837-c232-4a8a-841e-ef45787d8fcd*인 세그먼트에 대해 부서 이름을 "hrdept"로 업데이트 했습니다.</span><span class="sxs-lookup"><span data-stu-id="4bfc1-338">In this example, for the segment that has the GUID *c96e0837-c232-4a8a-841e-ef45787d8fcd*, we updated the department name to "HRDept".</span></span>

<span data-ttu-id="4bfc1-339">조직의 세그먼트 편집을 마친 후에는 정보 장벽 정책 [정의](#part-2-define-information-barrier-policies) 또는 [편집](#edit-a-policy) 을 진행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4bfc1-339">When you have finished editing segments for your organization, you can proceed to [define](#part-2-define-information-barrier-policies) or [edit](#edit-a-policy) information barrier policies.</span></span>

### <a name="edit-a-policy"></a><span data-ttu-id="4bfc1-340">정책 편집</span><span class="sxs-lookup"><span data-stu-id="4bfc1-340">Edit a policy</span></span>

1. <span data-ttu-id="4bfc1-341">현재 정보 장벽 정책 목록을 보려면 **InformationBarrierPolicy** cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="4bfc1-341">To view a list of current information barrier policies, use the **Get-InformationBarrierPolicy** cmdlet.</span></span>

    <span data-ttu-id="4bfc1-342">구문과`Get-InformationBarrierPolicy`</span><span class="sxs-lookup"><span data-stu-id="4bfc1-342">Syntax: `Get-InformationBarrierPolicy`</span></span>

    <span data-ttu-id="4bfc1-343">결과 목록에서 변경 하려는 정책을 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="4bfc1-343">In the list of results, identify the policy that you want to change.</span></span> <span data-ttu-id="4bfc1-344">정책의 GUID 및 이름을 적어둡니다.</span><span class="sxs-lookup"><span data-stu-id="4bfc1-344">Note the policy's GUID and name.</span></span>

2. <span data-ttu-id="4bfc1-345">**InformationBarrierPolicy** Cmdlet에서 **Identity** 매개 변수를 사용 하 여 변경할 내용을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4bfc1-345">Use the **Set-InformationBarrierPolicy** cmdlet with an **Identity** parameter, and specify the changes you want to make.</span></span>

    <span data-ttu-id="4bfc1-346">구문 (차단 세그먼트가 다른 세그먼트와 통신할 때):</span><span class="sxs-lookup"><span data-stu-id="4bfc1-346">Syntax (blocking segments from communicating with other segments):</span></span> 

    `Set-InformationBarrierPolicy -Identity GUID -SegmentsBlocked "segmentname, segmentname"` 

    <span data-ttu-id="4bfc1-347">구문 (세그먼트가 특정 세그먼트와만 통신할 수 있도록 설정):</span><span class="sxs-lookup"><span data-stu-id="4bfc1-347">Syntax (enabling segments to communicate only with certain other segments):</span></span>
    
    ``Set-InformationBarrierPolicy -Identity GUID -SegmentsAllowed "segmentname, segmentname"``

    <span data-ttu-id="4bfc1-348">예: 정책이 영업 및 마케팅과의 의견 교환에 대 한 조사를 차단 하도록 정의 되었다고 가정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4bfc1-348">Example: Suppose a policy was defined to block Research from communicating with Sales and Marketing.</span></span> <span data-ttu-id="4bfc1-349">이 cmdlet을 사용 하 여 정책이 정의 되었습니다.`New-InformationBarrierPolicy -Name "Research-SalesMarketing" -AssignedSegment "Research" -SegmentsBlocked "Sales, Marketing"`</span><span class="sxs-lookup"><span data-stu-id="4bfc1-349">The policy was defined by using this cmdlet: `New-InformationBarrierPolicy -Name "Research-SalesMarketing" -AssignedSegment "Research" -SegmentsBlocked "Sales, Marketing"`</span></span>
    
    <span data-ttu-id="4bfc1-350">리서치 담당자가 HR 사용자와만 통신할 수 있도록이를 변경 하려는 경우를 가정해 보겠습니다.</span><span class="sxs-lookup"><span data-stu-id="4bfc1-350">Suppose we want to change it so that people in Research can only communicate with people in HR.</span></span> <span data-ttu-id="4bfc1-351">이 변경 작업을 수행 하려면 다음 cmdlet을 사용 합니다.`Set-InformationBarrierPolicy -Identity 43c37853-ea10-4b90-a23d-ab8c93772471 -SegmentsAllowed "HR"`</span><span class="sxs-lookup"><span data-stu-id="4bfc1-351">To make this change, we use this cmdlet: `Set-InformationBarrierPolicy -Identity 43c37853-ea10-4b90-a23d-ab8c93772471 -SegmentsAllowed "HR"`</span></span>

3. <span data-ttu-id="4bfc1-352">정책 편집을 마친 후에는 변경 내용을 적용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="4bfc1-352">When you are finished editing a policy, make sure to apply your changes.</span></span> <span data-ttu-id="4bfc1-353">( [정보 장벽 정책 적용](#part-3-apply-information-barrier-policies)참조)</span><span class="sxs-lookup"><span data-stu-id="4bfc1-353">(See [Apply information barrier policies](#part-3-apply-information-barrier-policies).)</span></span>

### <a name="remove-a-policy"></a><span data-ttu-id="4bfc1-354">정책 제거</span><span class="sxs-lookup"><span data-stu-id="4bfc1-354">Remove a policy</span></span>

1. <span data-ttu-id="4bfc1-355">현재 정보 장벽 정책 목록을 보려면 **InformationBarrierPolicy** cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="4bfc1-355">To view a list of current information barrier policies, use the **Get-InformationBarrierPolicy** cmdlet.</span></span>

    <span data-ttu-id="4bfc1-356">구문과`Get-InformationBarrierPolicy`</span><span class="sxs-lookup"><span data-stu-id="4bfc1-356">Syntax: `Get-InformationBarrierPolicy`</span></span>

    <span data-ttu-id="4bfc1-357">결과 목록에서 제거할 정책을 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="4bfc1-357">In the list of results, identify the policy that you want to remove.</span></span> <span data-ttu-id="4bfc1-358">정책의 GUID 및 이름을 적어둡니다.</span><span class="sxs-lookup"><span data-stu-id="4bfc1-358">Note the policy's GUID and name.</span></span> <span data-ttu-id="4bfc1-359">정책이 비활성 상태로 설정 되어 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="4bfc1-359">Make sure the policy is set to inactive status.</span></span>

2. <span data-ttu-id="4bfc1-360">**InformationBarrierPolicy** Cmdlet을 Identity 매개 변수와 함께 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="4bfc1-360">Use the **Remove-InformationBarrierPolicy** cmdlet with an Identity parameter.</span></span>

    <span data-ttu-id="4bfc1-361">구문과`Remove-InformationBarrierPolicy -Identity GUID`</span><span class="sxs-lookup"><span data-stu-id="4bfc1-361">Syntax: `Remove-InformationBarrierPolicy -Identity GUID`</span></span>

    <span data-ttu-id="4bfc1-362">예: GUID *43c37853-ea10-4b90-a23d-ab8c93772471*가 있는 정책을 제거 하려고 한다고 가정 합시다.</span><span class="sxs-lookup"><span data-stu-id="4bfc1-362">Example: Suppose we want to remove a policy that has GUID *43c37853-ea10-4b90-a23d-ab8c93772471*.</span></span> <span data-ttu-id="4bfc1-363">이렇게 하려면 다음과 같은 cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="4bfc1-363">To do this, we use this cmdlet:</span></span>
    
    `Remove-InformationBarrierPolicy -Identity 43c37853-ea10-4b90-a23d-ab8c93772471`

    <span data-ttu-id="4bfc1-364">메시지가 표시 되 면 변경 내용을 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="4bfc1-364">When prompted, confirm the change.</span></span>

3. <span data-ttu-id="4bfc1-365">제거할 각 정책에 대해 1-2 단계를 반복 합니다.</span><span class="sxs-lookup"><span data-stu-id="4bfc1-365">Repeat steps 1-2 for each policy you want to remove.</span></span>

4. <span data-ttu-id="4bfc1-366">정책을 제거한 후에는 변경 내용을 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="4bfc1-366">When you are finished removing policies, apply your changes.</span></span> <span data-ttu-id="4bfc1-367">이 작업을 수행 하려면 **InformationBarrierPoliciesApplication** cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="4bfc1-367">To do this, use the **Start-InformationBarrierPoliciesApplication** cmdlet.</span></span>

    <span data-ttu-id="4bfc1-368">구문과`Start-InformationBarrierPoliciesApplication`</span><span class="sxs-lookup"><span data-stu-id="4bfc1-368">Syntax: `Start-InformationBarrierPoliciesApplication`</span></span>

    <span data-ttu-id="4bfc1-369">사용자가 조직에 대해 변경 내용을 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="4bfc1-369">Changes are applied, user by user, for your organization.</span></span> <span data-ttu-id="4bfc1-370">대규모 조직에서는이 프로세스를 완료 하는 데 24 시간 이상 소요 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4bfc1-370">If your organization is large, it can take 24 hours (or more) for this process to complete.</span></span>

### <a name="set-a-policy-to-inactive-status"></a><span data-ttu-id="4bfc1-371">정책을 비활성 상태로 설정</span><span class="sxs-lookup"><span data-stu-id="4bfc1-371">Set a policy to inactive status</span></span>

1. <span data-ttu-id="4bfc1-372">현재 정보 장벽 정책 목록을 보려면 **InformationBarrierPolicy** cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="4bfc1-372">To view a list of current information barrier policies, use the **Get-InformationBarrierPolicy** cmdlet.</span></span>

    <span data-ttu-id="4bfc1-373">구문과`Get-InformationBarrierPolicy`</span><span class="sxs-lookup"><span data-stu-id="4bfc1-373">Syntax: `Get-InformationBarrierPolicy`</span></span>

    <span data-ttu-id="4bfc1-374">결과 목록에서 변경 하거나 제거할 정책을 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="4bfc1-374">In the list of results, identify the policy that you want to change (or remove).</span></span> <span data-ttu-id="4bfc1-375">정책의 GUID 및 이름을 적어둡니다.</span><span class="sxs-lookup"><span data-stu-id="4bfc1-375">Note the policy's GUID and name.</span></span>

2. <span data-ttu-id="4bfc1-376">정책의 상태를 비활성으로 설정 하려면 Identity 매개 변수와 함께 **InformationBarrierPolicy** cmdlet을 사용 하 고 State 매개 변수는 비활성으로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4bfc1-376">To set the policy's status to inactive, use the **Set-InformationBarrierPolicy** cmdlet with an Identity parameter and the State parameter set to Inactive.</span></span>

    <span data-ttu-id="4bfc1-377">구문과`Set-InformationBarrierPolicy -Identity GUID -State Inactive`</span><span class="sxs-lookup"><span data-stu-id="4bfc1-377">Syntax: `Set-InformationBarrierPolicy -Identity GUID -State Inactive`</span></span>

    `Set-InformationBarrierPolicy -Identity 43c37853-ea10-4b90-a23d-ab8c9377247 -State Inactive`

    <span data-ttu-id="4bfc1-378">이 예에서는 GUID *43c37853-ea10-4b90-a23d-ab8c9377247을 사용* 하는 정보 장벽 정책을 비활성 상태로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4bfc1-378">In this example, we set an information barrier policy that has GUID *43c37853-ea10-4b90-a23d-ab8c9377247* to an inactive status.</span></span>

3. <span data-ttu-id="4bfc1-379">변경 내용을 적용 하려면 **InformationBarrierPoliciesApplication** cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="4bfc1-379">To apply your changes, use the **Start-InformationBarrierPoliciesApplication** cmdlet.</span></span>

    <span data-ttu-id="4bfc1-380">구문과`Start-InformationBarrierPoliciesApplication`</span><span class="sxs-lookup"><span data-stu-id="4bfc1-380">Syntax: `Start-InformationBarrierPoliciesApplication`</span></span>

    <span data-ttu-id="4bfc1-381">사용자가 조직에 대해 변경 내용을 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="4bfc1-381">Changes are applied, user by user, for your organization.</span></span> <span data-ttu-id="4bfc1-382">대규모 조직에서는이 프로세스를 완료 하는 데 24 시간 이상 소요 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4bfc1-382">If your organization is large, it can take 24 hours (or more) for this process to complete.</span></span> <span data-ttu-id="4bfc1-383">일반적으로 5000 사용자 계정을 처리 하는 데 한 시간 정도 소요 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4bfc1-383">(As a general guideline, it takes about an hour to process 5,000 user accounts.)</span></span>

<span data-ttu-id="4bfc1-384">이때 하나 이상의 정보 장벽 정책이 비활성 상태로 설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4bfc1-384">At this point, one or more information barrier policies are set to inactive status.</span></span> <span data-ttu-id="4bfc1-385">여기서는 다음 작업을 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4bfc1-385">From here, you can do any of the following:</span></span>
- <span data-ttu-id="4bfc1-386">그대로 유지 (비활성 상태로 설정 된 정책이 사용자에 게 영향을 주지 않음)</span><span class="sxs-lookup"><span data-stu-id="4bfc1-386">Leave it as is (a policy set to inactive status has no effect on users)</span></span>
- [<span data-ttu-id="4bfc1-387">정책 편집</span><span class="sxs-lookup"><span data-stu-id="4bfc1-387">Edit a policy</span></span>](#edit-a-policy) 
- [<span data-ttu-id="4bfc1-388">정책 제거</span><span class="sxs-lookup"><span data-stu-id="4bfc1-388">Remove a policy</span></span>](#remove-a-policy)

## <a name="example-contosos-departments-segments-and-policies"></a><span data-ttu-id="4bfc1-389">예: Contoso의 부서, 세그먼트 및 정책</span><span class="sxs-lookup"><span data-stu-id="4bfc1-389">Example: Contoso's departments, segments, and policies</span></span>

<span data-ttu-id="4bfc1-390">조직에서 세그먼트와 정책을 정의 하는 방법에 대 한 자세한 내용은 다음 예를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="4bfc1-390">To see how an organization might approach defining segments and policies, consider the following example.</span></span>

### <a name="contosos-departments-and-plan"></a><span data-ttu-id="4bfc1-391">Contoso의 부서 및 계획</span><span class="sxs-lookup"><span data-stu-id="4bfc1-391">Contoso's departments and plan</span></span>

<span data-ttu-id="4bfc1-392">Contoso에는 HR, Sales, Marketing, Research 및 Manufacturing의 다섯 가지 부서가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4bfc1-392">Contoso has five departments: HR, Sales, Marketing, Research, and Manufacturing.</span></span> <span data-ttu-id="4bfc1-393">업계 규정 준수를 유지 하기 위해 일부 부서의 사용자는 다음 표에 나열 된 것 처럼 다른 부서와 통신 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4bfc1-393">In order to remain compliant with industry regulations, people in some departments are not supposed to communicate with other departments, as listed in the following table:</span></span>

|<span data-ttu-id="4bfc1-394">단편</span><span class="sxs-lookup"><span data-stu-id="4bfc1-394">Segment</span></span>  |<span data-ttu-id="4bfc1-395">에 게 문의할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4bfc1-395">Can talk to</span></span>  |<span data-ttu-id="4bfc1-396">통신할 수 없음</span><span class="sxs-lookup"><span data-stu-id="4bfc1-396">Cannot talk to</span></span>  |
|---------|---------|---------|
|<span data-ttu-id="4bfc1-397">인력</span><span class="sxs-lookup"><span data-stu-id="4bfc1-397">HR</span></span>     |<span data-ttu-id="4bfc1-398">모든 사람</span><span class="sxs-lookup"><span data-stu-id="4bfc1-398">Everyone</span></span>         |<span data-ttu-id="4bfc1-399">(제한 없음)</span><span class="sxs-lookup"><span data-stu-id="4bfc1-399">(no restrictions)</span></span>         |
|<span data-ttu-id="4bfc1-400">세율</span><span class="sxs-lookup"><span data-stu-id="4bfc1-400">Sales</span></span>     |<span data-ttu-id="4bfc1-401">HR, 마케팅, 제조</span><span class="sxs-lookup"><span data-stu-id="4bfc1-401">HR, Marketing, Manufacturing</span></span>         |<span data-ttu-id="4bfc1-402">리서치</span><span class="sxs-lookup"><span data-stu-id="4bfc1-402">Research</span></span>         |
|<span data-ttu-id="4bfc1-403">마케팅</span><span class="sxs-lookup"><span data-stu-id="4bfc1-403">Marketing</span></span>     |<span data-ttu-id="4bfc1-404">모든 사람</span><span class="sxs-lookup"><span data-stu-id="4bfc1-404">Everyone</span></span>         |<span data-ttu-id="4bfc1-405">(제한 없음)</span><span class="sxs-lookup"><span data-stu-id="4bfc1-405">(no restrictions)</span></span>         |
|<span data-ttu-id="4bfc1-406">리서치</span><span class="sxs-lookup"><span data-stu-id="4bfc1-406">Research</span></span>     |<span data-ttu-id="4bfc1-407">HR, 마케팅, 제조</span><span class="sxs-lookup"><span data-stu-id="4bfc1-407">HR, Marketing, Manufacturing</span></span>        |<span data-ttu-id="4bfc1-408">세율</span><span class="sxs-lookup"><span data-stu-id="4bfc1-408">Sales</span></span>     |
|<span data-ttu-id="4bfc1-409">제조</span><span class="sxs-lookup"><span data-stu-id="4bfc1-409">Manufacturing</span></span> |<span data-ttu-id="4bfc1-410">HR, 마케팅</span><span class="sxs-lookup"><span data-stu-id="4bfc1-410">HR, Marketing</span></span> |<span data-ttu-id="4bfc1-411">HR 또는 Marketing 이외의 모든 사람</span><span class="sxs-lookup"><span data-stu-id="4bfc1-411">Anyone other than HR or Marketing</span></span> |

<span data-ttu-id="4bfc1-412">이러한 점을 고려 하 여 Contoso의 계획에는 다음과 같은 세 가지 정보 장벽 정책이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4bfc1-412">With this in mind, Contoso's plan includes three information barrier policies:</span></span>

1. <span data-ttu-id="4bfc1-413">영업이 연구와의 통신을 차단 하 고, 다른 정책으로 영업과의 통신을 차단 하도록 설계 된 정책</span><span class="sxs-lookup"><span data-stu-id="4bfc1-413">A policy designed to prevent Sales from communicating with Research (and another policy to prevent Research from communicating with Sales)</span></span>
2. <span data-ttu-id="4bfc1-414">제조에서 HR 및 Marketing과의 통신을 허용 하도록 설계 된 정책</span><span class="sxs-lookup"><span data-stu-id="4bfc1-414">A policy designed to allow Manufacturing to communicate with HR and Marketing only</span></span> 

<span data-ttu-id="4bfc1-415">HR 또는 Marketing에 대 한 정책을 정의할 필요는 없습니다.</span><span class="sxs-lookup"><span data-stu-id="4bfc1-415">It's not necessary to define policies for HR or Marketing.</span></span>

### <a name="contosos-defined-segments"></a><span data-ttu-id="4bfc1-416">Contoso의 정의 된 세그먼트</span><span class="sxs-lookup"><span data-stu-id="4bfc1-416">Contoso's defined segments</span></span>

<span data-ttu-id="4bfc1-417">Contoso는 다음과 같이 Azure Active Directory에서 부서 특성을 사용 하 여 세그먼트를 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="4bfc1-417">Contoso will use the Department attribute in Azure Active Directory to define segments, as follows:</span></span>

|<span data-ttu-id="4bfc1-418">부서</span><span class="sxs-lookup"><span data-stu-id="4bfc1-418">Department</span></span>  |<span data-ttu-id="4bfc1-419">세그먼트 정의</span><span class="sxs-lookup"><span data-stu-id="4bfc1-419">Segment Definition</span></span>  |
|---------|---------|
|<span data-ttu-id="4bfc1-420">인력</span><span class="sxs-lookup"><span data-stu-id="4bfc1-420">HR</span></span>     | `New-OrganizationSegment -Name "HR" -UserGroupFilter "Department -eq 'HR'"`        |
|<span data-ttu-id="4bfc1-421">세율</span><span class="sxs-lookup"><span data-stu-id="4bfc1-421">Sales</span></span>     | `New-OrganizationSegment -Name "Sales" -UserGroupFilter "Department -eq 'Sales'"`        |
|<span data-ttu-id="4bfc1-422">마케팅</span><span class="sxs-lookup"><span data-stu-id="4bfc1-422">Marketing</span></span>     | `New-OrganizationSegment -Name "Marketing" -UserGroupFilter "Department -eq 'Marketing'"`        |
|<span data-ttu-id="4bfc1-423">리서치</span><span class="sxs-lookup"><span data-stu-id="4bfc1-423">Research</span></span>     | `New-OrganizationSegment -Name "Research" -UserGroupFilter "Department -eq 'Research'"`        |
|<span data-ttu-id="4bfc1-424">제조</span><span class="sxs-lookup"><span data-stu-id="4bfc1-424">Manufacturing</span></span>     | `New-OrganizationSegment -Name "Manufacturing" -UserGroupFilter "Department -eq 'Manufacturing'"`        |

<span data-ttu-id="4bfc1-425">정의 된 세그먼트가 있으면 Contoso는 정책 정의를 진행 합니다.</span><span class="sxs-lookup"><span data-stu-id="4bfc1-425">With the segments defined, Contoso proceeds to define policies.</span></span> 

### <a name="contosos-information-barrier-policies"></a><span data-ttu-id="4bfc1-426">Contoso의 정보 장벽 정책</span><span class="sxs-lookup"><span data-stu-id="4bfc1-426">Contoso's information barrier policies</span></span>

<span data-ttu-id="4bfc1-427">Contoso는 다음 표에 설명 된 세 가지 정책을 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="4bfc1-427">Contoso defines three polices, as described in the following table:</span></span>

|<span data-ttu-id="4bfc1-428">정책</span><span class="sxs-lookup"><span data-stu-id="4bfc1-428">Policy</span></span>  |<span data-ttu-id="4bfc1-429">정책 정의</span><span class="sxs-lookup"><span data-stu-id="4bfc1-429">Policy Definition</span></span>  |
|---------|---------|
|<span data-ttu-id="4bfc1-430">정책 1: 영업에서 연구와의 통신을 방지 합니다.</span><span class="sxs-lookup"><span data-stu-id="4bfc1-430">Policy 1: Prevent Sales from communicating with Research</span></span>     | `New-InformationBarrierPolicy -Name "Sales-Research" -AssignedSegment "Sales" -SegmentsBlocked "Research" -State Inactive` <p> <span data-ttu-id="4bfc1-431">이 예에서 정보 장벽 정책을 *판매 조사*라고 합니다.</span><span class="sxs-lookup"><span data-stu-id="4bfc1-431">In this example, the information barrier policy is called *Sales-Research*.</span></span> <span data-ttu-id="4bfc1-432">이 정책이 활성 상태이 고 적용 되 면 Sales 세그먼트에 있는 사용자가 리서치 세그먼트의 사용자와 통신할 수 없도록 하는 데 도움이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4bfc1-432">When this policy is active and applied, it will help prevent users who are in the Sales segment from communicating with users in the Research segment.</span></span> <span data-ttu-id="4bfc1-433">이는 단방향 정책입니다. 이로 인해 연구가 영업과의 통신을 방지할 수는 없습니다.</span><span class="sxs-lookup"><span data-stu-id="4bfc1-433">This is a one-way policy; it won't prevent Research from communicating with Sales.</span></span> <span data-ttu-id="4bfc1-434">따라서 정책 2가 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="4bfc1-434">For that, Policy 2 is needed.</span></span>      |
|<span data-ttu-id="4bfc1-435">정책 2: 영업 담당자가 리서치를 진행 하지 못하도록 방지</span><span class="sxs-lookup"><span data-stu-id="4bfc1-435">Policy 2: Prevent Research from communicating with Sales</span></span>     | `New-InformationBarrierPolicy -Name "Research-Sales" -AssignedSegment "Research" -SegmentsBlocked "Sales" -State Inactive` <p> <span data-ttu-id="4bfc1-436">이 예에서는 정보 장벽 정책을 *리서치-판매*라고 합니다.</span><span class="sxs-lookup"><span data-stu-id="4bfc1-436">In this example, the information barrier policy is called *Research-Sales*.</span></span> <span data-ttu-id="4bfc1-437">이 정책이 활성화 및 적용 되 면 리서치 세그먼트에 있는 사용자가 Sales 세그먼트의 사용자와 통신할 수 없도록 하는 데 도움이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4bfc1-437">When this policy is active and applied, it will help prevent users who are in the Research segment from communicating with users in the Sales segment.</span></span>       |
|<span data-ttu-id="4bfc1-438">정책 3: 제조에서 HR 및 마케팅과의 통신만 허용</span><span class="sxs-lookup"><span data-stu-id="4bfc1-438">Policy 3: Allow Manufacturing to communicate with HR and Marketing only</span></span>     | `New-InformationBarrierPolicy -Name "Manufacturing-HRMarketing" -AssignedSegment "Manufacturing" -SegmentsAllowed "HR, Marketing" -State Inactive` <p><span data-ttu-id="4bfc1-439">이 경우 정보 장벽 정책은 *제조-HRMarketing*이라고 합니다.</span><span class="sxs-lookup"><span data-stu-id="4bfc1-439">In this case, the information barrier policy is called *Manufacturing-HRMarketing*.</span></span> <span data-ttu-id="4bfc1-440">이 정책이 활성 상태이 고 적용 되 면 Manufacturing은 HR 및 Marketing과만 통신할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4bfc1-440">When this policy is active and applied, Manufacturing can communicate only with HR and Marketing.</span></span> <span data-ttu-id="4bfc1-441">HR 및 Marketing은 다른 세그먼트와 통신 하는 것이 제한 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4bfc1-441">Note that HR and Marketing are not restricted from communicating with other segments.</span></span> |

<span data-ttu-id="4bfc1-442">**InformationBarrierPoliciesApplication** cmdlet을 실행 하 여 모든 세그먼트와 정책을 정의 하 고, Contoso는 정책을 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="4bfc1-442">With segments and policies defined, Contoso applies the policies by running the **Start-InformationBarrierPoliciesApplication** cmdlet.</span></span> 

<span data-ttu-id="4bfc1-443">이 작업이 완료 되 면 Contoso는 법적 및 업계 요구 사항을 준수 합니다.</span><span class="sxs-lookup"><span data-stu-id="4bfc1-443">When that finishes, Contoso is compliant with legal and industry requirements.</span></span>

## <a name="related-articles"></a><span data-ttu-id="4bfc1-444">관련 문서</span><span class="sxs-lookup"><span data-stu-id="4bfc1-444">Related articles</span></span>

[<span data-ttu-id="4bfc1-445">정보 장벽에 대 한 개요 보기</span><span class="sxs-lookup"><span data-stu-id="4bfc1-445">Get an overview of information barriers</span></span>](information-barriers.md)

[<span data-ttu-id="4bfc1-446">Microsoft 팀의 정보 장벽에 대해 자세히 알아보기</span><span class="sxs-lookup"><span data-stu-id="4bfc1-446">Learn more about information barriers in Microsoft Teams</span></span>](https://docs.microsoft.com/MicrosoftTeams/information-barriers-in-teams)

[<span data-ttu-id="4bfc1-447">정보 장벽 정책의 특성 (미리 보기)</span><span class="sxs-lookup"><span data-stu-id="4bfc1-447">Attributes for information barrier policies (Preview)</span></span>](information-barriers-attributes.md)

[<span data-ttu-id="4bfc1-448">정보 장벽 문제 해결 (미리 보기)</span><span class="sxs-lookup"><span data-stu-id="4bfc1-448">Troubleshooting information barriers (Preview)</span></span>](information-barriers-troubleshooting.md)
