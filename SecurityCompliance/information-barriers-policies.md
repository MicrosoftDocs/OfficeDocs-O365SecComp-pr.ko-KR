---
title: 정보 장벽 정책 정의
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 06/13/2019
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.collection:
- M365-security-compliance
localization_priority: None
description: Microsoft 팀에서 정보 장벽에 대 한 정책을 정의 하는 방법에 대해 알아봅니다.
ms.openlocfilehash: 8d575d0cde4bfec7109cc302f68beaf1040cd894
ms.sourcegitcommit: eeb51470d8996e93fac28d7f12c6117e2aeb0cf0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/14/2019
ms.locfileid: "34935950"
---
# <a name="define-policies-for-information-barriers-preview"></a><span data-ttu-id="fbb09-103">정보 장벽에 대 한 정책 정의 (미리 보기)</span><span class="sxs-lookup"><span data-stu-id="fbb09-103">Define policies for information barriers (Preview)</span></span>

## <a name="overview"></a><span data-ttu-id="fbb09-104">개요</span><span class="sxs-lookup"><span data-stu-id="fbb09-104">Overview</span></span>

<span data-ttu-id="fbb09-105">정보 장애물을 사용 하 여 특정 사용자 세그먼트가 서로 통신 하지 못하도록 설계 된 정책을 정의 하거나 특정 세그먼트가 다른 특정 세그먼트와만 통신할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fbb09-105">With information barriers, you can define policies that are designed to prevent certain segments of users from communicating with each other, or allow specific segments to communicate only with certain other segments.</span></span> <span data-ttu-id="fbb09-106">정보 장벽 정책은 조직에서 관련 업계 표준 및 규정 준수를 유지 하 고, 잠재적으로 발생할 수 있는 충돌을 방지 하는 데 도움이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="fbb09-106">Information barrier policies can help your organization maintain compliance with relevant industry standards and regulations, and avoid potential conflicts of interest.</span></span> <span data-ttu-id="fbb09-107">자세한 내용은 [정보 장벽 (미리 보기)](information-barriers.md)을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="fbb09-107">To learn more, see [Information barriers (Preview)](information-barriers.md).</span></span> 

<span data-ttu-id="fbb09-108">이 문서에서는 정보 장벽 정책을 계획, 정의, 구현 및 관리 하는 방법에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="fbb09-108">This article describes how to plan, define, implement, and manage information barrier policies.</span></span> <span data-ttu-id="fbb09-109">여러 단계를 수행 하 고 작업 흐름을 여러 부분으로 분할 합니다.</span><span class="sxs-lookup"><span data-stu-id="fbb09-109">Several steps are involved, and the work flow is divided into several parts.</span></span> <span data-ttu-id="fbb09-110">정보 장벽 정책 정의 또는 편집을 시작 하기 전에 [필수 구성 요소](#prerequisites) 및 전체 프로세스를 확인 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="fbb09-110">Make sure to read through the [prerequisites](#prerequisites) and the entire process before you begin defining (or editing) information barrier policies.</span></span>

> [!TIP]
> <span data-ttu-id="fbb09-111">이 문서에는 정보 장벽 정책을 계획 하 고 정의 하는 데 도움이 되는 [예제 시나리오](#example-contosos-departments-segments-and-policies) 및 [다운로드 가능한 Excel 통합 문서가](https://github.com/MicrosoftDocs/OfficeDocs-O365SecComp/raw/public/SecurityCompliance/media/InfoBarriers-PowerShellGenerator.xlsx) 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fbb09-111">This article includes an [example scenario](#example-contosos-departments-segments-and-policies) and a [downloadable Excel workbook](https://github.com/MicrosoftDocs/OfficeDocs-O365SecComp/raw/public/SecurityCompliance/media/InfoBarriers-PowerShellGenerator.xlsx) to help you plan and define your information barrier policies.</span></span>

## <a name="concepts-of-information-barrier-policies"></a><span data-ttu-id="fbb09-112">정보 장벽 정책의 개념</span><span class="sxs-lookup"><span data-stu-id="fbb09-112">Concepts of information barrier policies</span></span>

<span data-ttu-id="fbb09-113">정보 장벽 정책의 기본 개념을 이해 하는 데 도움이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="fbb09-113">It's helpful to know the underlying concepts of information barrier policies:</span></span>

- <span data-ttu-id="fbb09-114">**사용자 계정 특성** 은 Azure Active Directory (또는 Exchange Online)에서 정의 됩니다.</span><span class="sxs-lookup"><span data-stu-id="fbb09-114">**User account attributes** are defined in Azure Active Directory (or Exchange Online).</span></span> <span data-ttu-id="fbb09-115">이러한 특성에는 부서, 직함, 위치, 팀 이름 및 기타 작업 프로필 정보가 포함 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fbb09-115">These attributes can include department, job title, location, team name, and other job profile details.</span></span> 

- <span data-ttu-id="fbb09-116">**세그먼트** 는 선택한 **사용자 계정 특성**을 사용 하 여 Office 365 보안 & 준수 센터에 정의 된 사용자 집합입니다.</span><span class="sxs-lookup"><span data-stu-id="fbb09-116">**Segments** are sets of users that are defined in the Office 365 Security & Compliance Center using a selected **user account attribute**.</span></span> <span data-ttu-id="fbb09-117">( [지원 되는 특성 목록](information-barriers-attributes.md)참조)</span><span class="sxs-lookup"><span data-stu-id="fbb09-117">(See the [list of supported attributes](information-barriers-attributes.md).)</span></span> 

- <span data-ttu-id="fbb09-118">**정보 장벽 정책** 에 따라 통신 제한 또는 제한이 결정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="fbb09-118">**Information barrier policies** determine communication limits or restrictions.</span></span> <span data-ttu-id="fbb09-119">정보 장벽 정책을 정의할 때는 두 가지 정책 유형 중에서 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="fbb09-119">When you define information barrier policies, you choose from two kinds of policies:</span></span>
    - <span data-ttu-id="fbb09-120">한 세그먼트가 다른 세그먼트와 통신할 수 없도록 하는 정책 차단</span><span class="sxs-lookup"><span data-stu-id="fbb09-120">"Block" policies that prevent one segment from communicating with another segment</span></span>
    - <span data-ttu-id="fbb09-121">한 세그먼트가 다른 특정 세그먼트와만 통신할 수 있도록 하는 정책 "허용"</span><span class="sxs-lookup"><span data-stu-id="fbb09-121">"Allow" policies that allow one segment to communicate with only certain other segments</span></span>

- <span data-ttu-id="fbb09-122">**정책 응용 프로그램** 은 모든 정보 장벽 정책이 정의 된 후에 수행 되며, 조직에 적용할 준비가 된 것입니다.</span><span class="sxs-lookup"><span data-stu-id="fbb09-122">**Policy application** is done after all information barrier policies are defined, and you are ready to apply them in your organization.</span></span>

## <a name="the-work-flow-at-a-glance"></a><span data-ttu-id="fbb09-123">작업 흐름 살펴보기</span><span class="sxs-lookup"><span data-stu-id="fbb09-123">The work flow at a glance</span></span>

|<span data-ttu-id="fbb09-124">단계</span><span class="sxs-lookup"><span data-stu-id="fbb09-124">Phase</span></span>    |<span data-ttu-id="fbb09-125">관련 기능</span><span class="sxs-lookup"><span data-stu-id="fbb09-125">What's involved</span></span>  |
|---------|---------|
|[<span data-ttu-id="fbb09-126">필수 구성 요소를 충족 하는지 확인</span><span class="sxs-lookup"><span data-stu-id="fbb09-126">Make sure prerequisites are met</span></span>](#prerequisites)     |<span data-ttu-id="fbb09-127">- [필요한 라이선스 및 사용 권한이](information-barriers.md#required-licenses-and-permissions) 있는지 확인</span><span class="sxs-lookup"><span data-stu-id="fbb09-127">- Verify that you have the [required licenses and permissions](information-barriers.md#required-licenses-and-permissions)</span></span><br/><span data-ttu-id="fbb09-128">-조직의 디렉터리에 조직의 구조를 반영 하는 데이터가 포함 되어 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="fbb09-128">- Make sure that your organization's directory includes data that reflects your organization's structure</span></span><br/><span data-ttu-id="fbb09-129">-Microsoft 팀에 대해 범위 디렉터리 검색 사용</span><span class="sxs-lookup"><span data-stu-id="fbb09-129">- Enable scoped directory search for Microsoft Teams</span></span><br/><span data-ttu-id="fbb09-130">-감사 로깅이 설정 되어 있는지 확인</span><span class="sxs-lookup"><span data-stu-id="fbb09-130">- Make sure audit logging is turned on</span></span><br/><span data-ttu-id="fbb09-131">-PowerShell 사용 (예제가 제공 됨)</span><span class="sxs-lookup"><span data-stu-id="fbb09-131">- Use PowerShell (examples are provided)</span></span><br/><span data-ttu-id="fbb09-132">-Microsoft 팀에 관리자 동의를 제공 합니다 (단계 포함).</span><span class="sxs-lookup"><span data-stu-id="fbb09-132">- Provide admin consent for Microsoft Teams (steps are included)</span></span>          |
|[<span data-ttu-id="fbb09-133">1 부: 조직의 모든 사용자 분할</span><span class="sxs-lookup"><span data-stu-id="fbb09-133">Part 1: Segment all the users in your organization</span></span>](#part-1-segment-users)     |<span data-ttu-id="fbb09-134">-필요한 정책을 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fbb09-134">- Determine what policies are needed</span></span><br/><span data-ttu-id="fbb09-135">-정의할 세그먼트 목록을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="fbb09-135">- Make a list of segments to define</span></span><br/><span data-ttu-id="fbb09-136">-사용할 특성 식별</span><span class="sxs-lookup"><span data-stu-id="fbb09-136">- Identify which attributes to use</span></span><br/><span data-ttu-id="fbb09-137">-정책 필터 용어로 세그먼트를 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="fbb09-137">- Define segments in terms of policy filters</span></span>        |
|[<span data-ttu-id="fbb09-138">2 부: 정보 장벽 정책 정의</span><span class="sxs-lookup"><span data-stu-id="fbb09-138">Part 2: Define information barrier policies</span></span>](#part-2-define-information-barrier-policies)     |<span data-ttu-id="fbb09-139">-정책 정의 (아직 적용 되지 않음)</span><span class="sxs-lookup"><span data-stu-id="fbb09-139">- Define your policies (do not apply yet)</span></span><br/><span data-ttu-id="fbb09-140">-두 종류 (차단 또는 허용)를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="fbb09-140">- Choose from two kinds (block or allow)</span></span> |
|[<span data-ttu-id="fbb09-141">3 부: 정보 장벽 정책 적용</span><span class="sxs-lookup"><span data-stu-id="fbb09-141">Part 3: Apply information barrier policies</span></span>](#part-3-apply-information-barrier-policies)     |<span data-ttu-id="fbb09-142">-정책을 활성 상태로 설정</span><span class="sxs-lookup"><span data-stu-id="fbb09-142">- Set policies to active status</span></span><br/><span data-ttu-id="fbb09-143">-정책 응용 프로그램 실행</span><span class="sxs-lookup"><span data-stu-id="fbb09-143">- Run the policy application</span></span><br/><span data-ttu-id="fbb09-144">-정책 상태 보기</span><span class="sxs-lookup"><span data-stu-id="fbb09-144">- View policy status</span></span>         |
|<span data-ttu-id="fbb09-145">(필요한 경우) [세그먼트 또는 정책 편집](#edit-a-segment-or-a-policy)</span><span class="sxs-lookup"><span data-stu-id="fbb09-145">(As needed) [Edit a segment or a policy](#edit-a-segment-or-a-policy)</span></span>     |<span data-ttu-id="fbb09-146">-세그먼트 편집</span><span class="sxs-lookup"><span data-stu-id="fbb09-146">- Edit a segment</span></span><br/><span data-ttu-id="fbb09-147">-정책 편집 또는 제거</span><span class="sxs-lookup"><span data-stu-id="fbb09-147">- Edit or remove a policy</span></span><br/><span data-ttu-id="fbb09-148">-정책 응용 프로그램 실행</span><span class="sxs-lookup"><span data-stu-id="fbb09-148">- Run the policy application</span></span><br/><span data-ttu-id="fbb09-149">-정책 상태 보기</span><span class="sxs-lookup"><span data-stu-id="fbb09-149">- View policy status</span></span>         |
|<span data-ttu-id="fbb09-150">(필요한 경우) [문제 해결](information-barriers-troubleshooting.md)</span><span class="sxs-lookup"><span data-stu-id="fbb09-150">(As needed) [Troubleshooting](information-barriers-troubleshooting.md)</span></span>|<span data-ttu-id="fbb09-151">-항목이 정상적으로 작동 하지 않을 때 작업 수행</span><span class="sxs-lookup"><span data-stu-id="fbb09-151">- Take action when things are not working as expected</span></span>|

## <a name="prerequisites"></a><span data-ttu-id="fbb09-152">필수 구성 요소</span><span class="sxs-lookup"><span data-stu-id="fbb09-152">Prerequisites</span></span>

<span data-ttu-id="fbb09-153">[필요한 라이선스 및 사용 권한](information-barriers.md#required-licenses-and-permissions)외에도 다음과 같은 요구 사항을 충족 하는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="fbb09-153">In addition to the [required licenses and permissions](information-barriers.md#required-licenses-and-permissions), make sure that the following requirements are met:</span></span> 
     
- <span data-ttu-id="fbb09-154">**디렉터리 데이터**</span><span class="sxs-lookup"><span data-stu-id="fbb09-154">**Directory data**.</span></span> <span data-ttu-id="fbb09-155">조직의 구조가 디렉터리 데이터에 반영 되는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="fbb09-155">Make sure that your organization's structure is reflected in directory data.</span></span> <span data-ttu-id="fbb09-156">이렇게 하려면 그룹 구성원 자격, 부서 이름 등의 사용자 계정 특성이 Azure Active Directory 또는 Exchange Online에서 올바르게 채워졌는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="fbb09-156">To do this, make sure that user account attributes, such as group membership, department name, etc. are populated correctly in Azure Active Directory (or Exchange Online).</span></span> <span data-ttu-id="fbb09-157">자세한 내용은 다음 리소스를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="fbb09-157">To learn more, see the following resources:</span></span>
  - [<span data-ttu-id="fbb09-158">정보 장벽 정책의 특성 (미리 보기)</span><span class="sxs-lookup"><span data-stu-id="fbb09-158">Attributes for information barrier policies (Preview)</span></span>](information-barriers-attributes.md)
  - [<span data-ttu-id="fbb09-159">Azure Active Directory를 사용 하 여 사용자 프로필 정보 추가 또는 업데이트</span><span class="sxs-lookup"><span data-stu-id="fbb09-159">Add or update a user's profile information using Azure Active Directory</span></span>](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-users-profile-azure-portal)
  - [<span data-ttu-id="fbb09-160">Office 365 PowerShell를 사용 하 여 사용자 계정 속성 구성</span><span class="sxs-lookup"><span data-stu-id="fbb09-160">Configure user account properties with Office 365 PowerShell</span></span>](https://docs.microsoft.com/office365/enterprise/powershell/configure-user-account-properties-with-office-365-powershell)

- <span data-ttu-id="fbb09-161">**범위 디렉터리 검색**</span><span class="sxs-lookup"><span data-stu-id="fbb09-161">**Scoped directory search**.</span></span> <span data-ttu-id="fbb09-162">조직의 첫 번째 정보 장벽 정책을 정의 하기 전에 [Microsoft 팀에서 범위 지정 디렉터리 검색을 사용 하도록 설정](https://docs.microsoft.com/MicrosoftTeams/teams-scoped-directory-search)해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="fbb09-162">Before you define your organization's first information barrier policy, you must [enable scoped directory search in Microsoft Teams](https://docs.microsoft.com/MicrosoftTeams/teams-scoped-directory-search).</span></span> <span data-ttu-id="fbb09-163">정보 장벽 정책을 설정 하거나 정의 하기 전에 범위 디렉터리 검색을 사용 하도록 설정한 후 24 시간 이상 기다립니다.</span><span class="sxs-lookup"><span data-stu-id="fbb09-163">Wait at least 24 hours after enabling scoped directory search before you set up or define information barrier policies.</span></span>

- <span data-ttu-id="fbb09-164">**감사 로깅**</span><span class="sxs-lookup"><span data-stu-id="fbb09-164">**Audit logging**.</span></span> <span data-ttu-id="fbb09-165">정책 응용 프로그램의 상태를 조회 하려면 감사 로깅이 설정 되어 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="fbb09-165">In order to look up the status of a policy application, audit logging must be turned on.</span></span> <span data-ttu-id="fbb09-166">세그먼트 또는 정책 정의를 시작 하기 전에이 작업을 수행 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="fbb09-166">We recommend doing this before you begin to define segments or policies.</span></span> <span data-ttu-id="fbb09-167">자세한 내용은 [Turn Office 365 감사 로그 검색 설정 또는 해제](turn-audit-log-search-on-or-off.md)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="fbb09-167">To learn more, see [Turn Office 365 audit log search on or off](turn-audit-log-search-on-or-off.md).</span></span>

- <span data-ttu-id="fbb09-168">**PowerShell**입니다.</span><span class="sxs-lookup"><span data-stu-id="fbb09-168">**PowerShell**.</span></span> <span data-ttu-id="fbb09-169">현재 정보 장벽 정책은 PowerShell cmdlet을 사용 하 여 Office 365 보안 & 준수 센터에서 정의 되 고 관리 됩니다.</span><span class="sxs-lookup"><span data-stu-id="fbb09-169">Currently, information barrier policies are defined and managed in the Office 365 Security & Compliance Center using PowerShell cmdlets.</span></span> <span data-ttu-id="fbb09-170">이 문서에서는 몇 가지 예를 제공 했지만 PowerShell cmdlet 및 매개 변수에 익숙해져야 합니다.</span><span class="sxs-lookup"><span data-stu-id="fbb09-170">Although several examples are provided in this article, you'll need to be familiar with PowerShell cmdlets and parameters.</span></span> <span data-ttu-id="fbb09-171">[Office 365 보안 & 준수 센터 PowerShell에 연결](https://docs.microsoft.com/powershell/exchange/office-365-scc/connect-to-scc-powershell/connect-to-scc-powershell?view=exchange-ps)합니다.</span><span class="sxs-lookup"><span data-stu-id="fbb09-171">[Connect to Office 365 Security & Compliance Center PowerShell](https://docs.microsoft.com/powershell/exchange/office-365-scc/connect-to-scc-powershell/connect-to-scc-powershell?view=exchange-ps).</span></span>

- <span data-ttu-id="fbb09-172">**Microsoft 팀의 정보 장벽에 대 한 관리자 동의**</span><span class="sxs-lookup"><span data-stu-id="fbb09-172">**Admin consent for information barriers in Microsoft Teams**.</span></span> <span data-ttu-id="fbb09-173">정책이 적용 되 면 정보 장애물은에는 없는 채팅 세션에서 사용자를 제거할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fbb09-173">When your policies are in place, information barriers can remove people from chat sessions they are not supposed to be in.</span></span> <span data-ttu-id="fbb09-174">이렇게 하면 조직이 정책 및 규정 준수 상태를 유지할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fbb09-174">This helps ensure your organization remains compliant with policies and regulations.</span></span> <span data-ttu-id="fbb09-175">다음 절차를 사용 하 여 정보 장벽 정책이 Microsoft 팀에서 예상 대로 작동 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fbb09-175">Use the following procedure to enable information barrier policies to work as expected in Microsoft Teams.</span></span> 

   1. <span data-ttu-id="fbb09-176">다음 PowerShell cmdlet을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="fbb09-176">Run the following PowerShell cmdlets:</span></span>

      ```
      Login-AzureRmAccount 
      $appId="bcf62038-e005-436d-b970-2a472f8c1982" 
      $sp=Get-AzureRmADServicePrincipal -ServicePrincipalName $appId
      if ($sp -eq $null) { New-AzureRmADServicePrincipal -ApplicationId $appId }
      Start-Process  "https://login.microsoftonline.com/common/adminconsent?client_id=$appId"
      ```

   2. <span data-ttu-id="fbb09-177">메시지가 나타나면 Office 365에 대 한 회사 또는 학교 계정을 사용 하 여 로그인 합니다.</span><span class="sxs-lookup"><span data-stu-id="fbb09-177">When prompted, sign in using your work or school account for Office 365.</span></span>

   3. <span data-ttu-id="fbb09-178">요청 된 **사용 권한** 대화 상자에서 정보를 검토 하 고 **수락**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="fbb09-178">In the **Permissions requested** dialog box, review the information, and then choose **Accept**.</span></span>

<span data-ttu-id="fbb09-179">모든 필수 구성 요소가 충족 되 면 다음 섹션으로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="fbb09-179">When all the prerequisites are met, proceed to the next section.</span></span>

> [!TIP]
> <span data-ttu-id="fbb09-180">계획을 준비 하는 데 도움이 되도록이 문서에 예제 시나리오가 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fbb09-180">To help you prepare your plan, an example scenario is included in this article.</span></span> <span data-ttu-id="fbb09-181">[Contoso의 부서, 세그먼트 및 정책을 참조 하세요](#example-contosos-departments-segments-and-policies).</span><span class="sxs-lookup"><span data-stu-id="fbb09-181">[See Contoso's departments, segments, and policies](#example-contosos-departments-segments-and-policies).</span></span><p><span data-ttu-id="fbb09-182">또한 다운로드 가능한 Excel 통합 문서를 사용 하 여 세그먼트와 정책을 계획 하 고 정의 하 고 PowerShell cmdlet을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fbb09-182">In addition, a downloadable Excel workbook is available to help you plan and define your segments and policies (and create your PowerShell cmdlets).</span></span> <span data-ttu-id="fbb09-183">[통합 문서를 가져옵니다](https://github.com/MicrosoftDocs/OfficeDocs-O365SecComp/raw/public/SecurityCompliance/media/InfoBarriers-PowerShellGenerator.xlsx).</span><span class="sxs-lookup"><span data-stu-id="fbb09-183">[Get the workbook](https://github.com/MicrosoftDocs/OfficeDocs-O365SecComp/raw/public/SecurityCompliance/media/InfoBarriers-PowerShellGenerator.xlsx).</span></span> 

## <a name="part-1-segment-users"></a><span data-ttu-id="fbb09-184">1 부: 사용자 분할</span><span class="sxs-lookup"><span data-stu-id="fbb09-184">Part 1: Segment users</span></span>

<span data-ttu-id="fbb09-185">이 단계에서는 필요한 정보 장벽 정책이 무엇 인지 결정 하 고, 정의할 세그먼트 목록을 만든 다음, 세그먼트를 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="fbb09-185">During this phase, you determine what information barrier policies are needed, make a list of segments to define, and then define your segments.</span></span>

### <a name="determine-what-policies-are-needed"></a><span data-ttu-id="fbb09-186">필요한 정책 결정</span><span class="sxs-lookup"><span data-stu-id="fbb09-186">Determine what policies are needed</span></span>

<span data-ttu-id="fbb09-187">정보 장벽 정책이 필요한 조직 내의 그룹 인 법률 및 업계 규정을 고려 하 고 계십니까?</span><span class="sxs-lookup"><span data-stu-id="fbb09-187">Considering legal and industry regulations, who are the groups within your organization who will need information barrier policies?</span></span> <span data-ttu-id="fbb09-188">목록을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="fbb09-188">Make a list.</span></span> <span data-ttu-id="fbb09-189">다른 그룹과 통신을 차단 해야 하는 그룹이 있습니까?</span><span class="sxs-lookup"><span data-stu-id="fbb09-189">Are there any groups who should be prevented from communicating with another group?</span></span> <span data-ttu-id="fbb09-190">하나 또는 두 개의 다른 그룹과만 통신 하도록 허용 해야 하는 그룹이 있습니까?</span><span class="sxs-lookup"><span data-stu-id="fbb09-190">Are there any groups that should be allowed to communicate only with one or two other groups?</span></span> <span data-ttu-id="fbb09-191">다음은 두 그룹 중 하나에 속하는 것으로 필요한 정책을 고려 합니다.</span><span class="sxs-lookup"><span data-stu-id="fbb09-191">Think about the policies you need as belonging to one of two groups:</span></span>
- <span data-ttu-id="fbb09-192">"차단" 정책은 한 그룹이 다른 그룹과 통신 하지 못하도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="fbb09-192">"Block" policies prevent one group from communicating with another group.</span></span>
- <span data-ttu-id="fbb09-193">"허용" 정책을 사용 하면 그룹이 다른 특정 그룹과 통신할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fbb09-193">"Allow" policies allow a group to communicate with only certain other, specific groups.</span></span>

<span data-ttu-id="fbb09-194">초기 그룹 및 정책 목록이 있으면 필요한 세그먼트를 확인 하기 위해 계속 진행 합니다.</span><span class="sxs-lookup"><span data-stu-id="fbb09-194">When you have your initial list of groups and policies, proceed to identify the segments you'll need.</span></span> 

### <a name="identify-segments"></a><span data-ttu-id="fbb09-195">세그먼트 식별</span><span class="sxs-lookup"><span data-stu-id="fbb09-195">Identify segments</span></span>

<span data-ttu-id="fbb09-196">초기 정책 목록 외에, 조직의 세그먼트 목록을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="fbb09-196">In addition to your initial list of policies, make a list of segments for your organization.</span></span> <span data-ttu-id="fbb09-197">조직의 모든 사용자는 세그먼트에 속해야 하며, 사용자는 두 개 이상의 세그먼트에 속해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="fbb09-197">Every user in your organization should belong to a segment, and no user should belong to two or more segments.</span></span> <span data-ttu-id="fbb09-198">각 세그먼트에는 하나의 정보 장벽 정책만 적용 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fbb09-198">Each segment can have only one information barrier policy applied.</span></span> 

<span data-ttu-id="fbb09-199">세그먼트를 정의 하는 데 사용할 조직의 디렉터리 데이터 특성을 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fbb09-199">Determine which attributes in your organization's directory data you'll use to define segments.</span></span> <span data-ttu-id="fbb09-200">*부서*, *MemberOf*또는 지원 되는 특성을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fbb09-200">You can use *Department*, *MemberOf*, or any of the supported attributes.</span></span> <span data-ttu-id="fbb09-201">모든 사용자에 대해 선택한 특성 값이 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="fbb09-201">Make sure that you have values in the attribute you select for all users.</span></span> <span data-ttu-id="fbb09-202">[정보 장벽 (미리 보기)에 대해 지원 되는 특성 목록을 참조 하세요](information-barriers-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="fbb09-202">[See the list of supported attributes for information barriers (Preview)](information-barriers-attributes.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="fbb09-203">**다음 섹션을 진행 하기 전에 디렉터리 데이터에 세그먼트를 정의 하는 데 사용할 수 있는 특성 값이 있는지 확인**합니다.</span><span class="sxs-lookup"><span data-stu-id="fbb09-203">**Before you proceed to the next section, make sure your directory data has values for attributes that you can use to define segments**.</span></span> <span data-ttu-id="fbb09-204">디렉터리 데이터에 사용 하려는 특성의 값이 없는 경우에는 정보 장애물을 계속 하기 전에 해당 정보를 포함 하도록 모든 사용자 계정을 업데이트 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="fbb09-204">If your directory data does not have values for the attributes you want to use, then all user accounts must be updated to include that information before you proceed with information barriers.</span></span> <span data-ttu-id="fbb09-205">이에 대 한 도움말을 보려면 다음 리소스를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="fbb09-205">To get help with this, see the following resources:</span></span><br/><span data-ttu-id="fbb09-206">- [Office 365 PowerShell을 사용 하 여 사용자 계정 속성 구성](https://docs.microsoft.com/office365/enterprise/powershell/configure-user-account-properties-with-office-365-powershell)</span><span class="sxs-lookup"><span data-stu-id="fbb09-206">- [Configure user account properties with Office 365 PowerShell](https://docs.microsoft.com/office365/enterprise/powershell/configure-user-account-properties-with-office-365-powershell)</span></span><br/><span data-ttu-id="fbb09-207">- [Azure Active Directory를 사용 하 여 사용자 프로필 정보 추가 또는 업데이트](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-users-profile-azure-portal)</span><span class="sxs-lookup"><span data-stu-id="fbb09-207">- [Add or update a user's profile information using Azure Active Directory](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-users-profile-azure-portal)</span></span>

### <a name="define-segments-using-powershell"></a><span data-ttu-id="fbb09-208">PowerShell을 사용 하 여 세그먼트 정의</span><span class="sxs-lookup"><span data-stu-id="fbb09-208">Define segments using PowerShell</span></span>

<span data-ttu-id="fbb09-209">세그먼트를 정의 해도 사용자에 게 영향을 주지 않습니다. 정보 장벽 정책을 정의 하 고 적용 하기 위한 단계를 설정 하기만 하면 됩니다.</span><span class="sxs-lookup"><span data-stu-id="fbb09-209">Defining segments does not effect users; it just sets the stage for information barrier policies to be defined and then applied.</span></span>

1. <span data-ttu-id="fbb09-210">조직 세그먼트를 정의 하려면 사용 하려는 [특성](information-barriers-attributes.md) 에 해당 하는 **usergroupfilter** 매개 변수와 함께 **OrganizationSegment** cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="fbb09-210">To define an organizational segment, use the **New-OrganizationSegment** cmdlet with the **UserGroupFilter** parameter that corresponds to the [attribute](information-barriers-attributes.md) you want to use.</span></span> 

    <span data-ttu-id="fbb09-211">구문과`New-OrganizationSegment -Name "segmentname" -UserGroupFilter "attribute -eq 'attributevalue'"`</span><span class="sxs-lookup"><span data-stu-id="fbb09-211">Syntax: `New-OrganizationSegment -Name "segmentname" -UserGroupFilter "attribute -eq 'attributevalue'"`</span></span>

    <span data-ttu-id="fbb09-212">예제: `New-OrganizationSegment -Name "HR" -UserGroupFilter "Department -eq 'HR'"`</span><span class="sxs-lookup"><span data-stu-id="fbb09-212">Example: `New-OrganizationSegment -Name "HR" -UserGroupFilter "Department -eq 'HR'"`</span></span>

    <span data-ttu-id="fbb09-213">이 예제에서는 hr을 사용 하 \*\* 여 인사부 라는 세그먼트 \*\* 를 정의 하 고 부서 특성에 값을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fbb09-213">In this example, a segment called *HR* is defined using *HR*, a value in the Department attribute.</span></span>

2. <span data-ttu-id="fbb09-214">정의 하려는 각 세그먼트에 대해 1 단계를 반복 합니다.</span><span class="sxs-lookup"><span data-stu-id="fbb09-214">Repeat step 1 for each segment you want to define.</span></span>

    <span data-ttu-id="fbb09-215">각 cmdlet을 실행 하면 새 세그먼트에 대 한 세부 정보 목록이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="fbb09-215">After you run each cmdlet, you should see a list of details about the new segment.</span></span> <span data-ttu-id="fbb09-216">세부 정보에는 세그먼트의 유형, 작성자가 작성 하거나 마지막으로 수정한 사람 등이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="fbb09-216">Details include the segment's type, who created or last modified it, and so on.</span></span> 

> [!IMPORTANT]
> <span data-ttu-id="fbb09-217">**세그먼트가 겹치지 않는지 확인**합니다.</span><span class="sxs-lookup"><span data-stu-id="fbb09-217">**Make sure that your segments do not overlap**.</span></span> <span data-ttu-id="fbb09-218">조직의 각 사용자는 하나의 세그먼트에만 속해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="fbb09-218">Each user in your organization should belong to one (and only one) segment.</span></span> <span data-ttu-id="fbb09-219">두 개 이상의 세그먼트에 속해야 하는 사용자가 없습니다.</span><span class="sxs-lookup"><span data-stu-id="fbb09-219">No user should belong to two or more segments.</span></span> <span data-ttu-id="fbb09-220">세그먼트는 조직의 모든 사용자에 대해 정의 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="fbb09-220">Segments should be defined for all users in your organization.</span></span> <span data-ttu-id="fbb09-221">(예제:이 문서에 나와 있는 [Contoso의 정의 된 세그먼트](#contosos-defined-segments) 참조)</span><span class="sxs-lookup"><span data-stu-id="fbb09-221">(See [Example: Contoso's defined segments](#contosos-defined-segments) in this article.)</span></span>

<span data-ttu-id="fbb09-222">세그먼트를 정의한 후에는 정보 장벽 정책 정의로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="fbb09-222">After you have defined your segments, proceed to define information barrier policies.</span></span>

## <a name="part-2-define-information-barrier-policies"></a><span data-ttu-id="fbb09-223">2 부: 정보 장벽 정책 정의</span><span class="sxs-lookup"><span data-stu-id="fbb09-223">Part 2: Define information barrier policies</span></span>

<span data-ttu-id="fbb09-224">특정 세그먼트 간 통신을 방지 해야 하는지 또는 특정 세그먼트에 대 한 통신을 제한할지 여부를 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fbb09-224">Determine whether you need to prevent communications between certain segments, or limit communications to certain segments.</span></span> <span data-ttu-id="fbb09-225">조직에서 법적 및 업계 요구 사항을 준수 하는 데 필요한 최소 정책 수를 사용 하는 것이 이상적입니다.</span><span class="sxs-lookup"><span data-stu-id="fbb09-225">Ideally, you'll use the minimum number of policies to ensure your organization is compliant with legal and industry requirements.</span></span>

<span data-ttu-id="fbb09-226">사용자 세그먼트 목록과 정의할 정보 장벽 정책을 사용 하 여 시나리오를 선택한 다음 단계를 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="fbb09-226">With your list of user segments and the information barrier policies you want to define, select a scenario, and then follow the steps.</span></span> 

- [<span data-ttu-id="fbb09-227">시나리오 1: 세그먼트 간 통신 차단</span><span class="sxs-lookup"><span data-stu-id="fbb09-227">Scenario 1: Block communications between segments</span></span>](#scenario-1-block-communications-between-segments)
- [<span data-ttu-id="fbb09-228">시나리오 2: 특정 세그먼트가 다른 세그먼트와만 통신할 수 있도록 허용</span><span class="sxs-lookup"><span data-stu-id="fbb09-228">Scenario 2: Allow a segment to communicate only with one other segment</span></span>](#scenario-2-allow-a-segment-to-communicate-only-with-one-other-segment)

> [!IMPORTANT]
> <span data-ttu-id="fbb09-229">**정책을 정의할 때 세그먼트에 두 개 이상의 정책을 할당 하지**않도록 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="fbb09-229">**Make sure that as you define policies, you do not assign more than one policy to a segment**.</span></span> <span data-ttu-id="fbb09-230">예를 들어 *sales*라는 세그먼트에 대해 하나의 정책을 정의 하는 경우에는 *sales*에 대 한 추가 정책을 정의 하지 마십시오.</span><span class="sxs-lookup"><span data-stu-id="fbb09-230">For example, if you define one policy for a segment called *Sales*, do not define an additional policy for *Sales*.</span></span><p><span data-ttu-id="fbb09-231">또한 정보 장벽 정책을 정의 하는 동안 이러한 정책을 적용할 준비가 될 때까지 해당 정책이 비활성 상태로 설정 되었는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="fbb09-231">In addition, as you define information barrier policies, make sure to set those policies to inactive status until you are ready to apply them.</span></span> <span data-ttu-id="fbb09-232">정책 정의 (또는 편집)는 해당 정책이 활성 상태로 설정 된 후에 야 사용자에 게 영향을 줍니다.</span><span class="sxs-lookup"><span data-stu-id="fbb09-232">Defining (or editing) policies does not affect users until those policies are set to active status and then applied.</span></span>

<span data-ttu-id="fbb09-233">(이 문서의 [예: Contoso의 정보 장벽 정책](#contosos-information-barrier-policies) 참조)</span><span class="sxs-lookup"><span data-stu-id="fbb09-233">(See [Example: Contoso's information barrier policies](#contosos-information-barrier-policies) in this article.)</span></span>

### <a name="scenario-1-block-communications-between-segments"></a><span data-ttu-id="fbb09-234">시나리오 1: 세그먼트 간 통신 차단</span><span class="sxs-lookup"><span data-stu-id="fbb09-234">Scenario 1: Block communications between segments</span></span>

<span data-ttu-id="fbb09-235">세그먼트 간의 통신을 차단 하려는 경우 각 방향에 하나씩 두 개의 정책을 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="fbb09-235">When you want to block segments from communicating with each other, you define two policies: one for each direction.</span></span> <span data-ttu-id="fbb09-236">각 정책은 통신을 단방향 으로만 차단 합니다.</span><span class="sxs-lookup"><span data-stu-id="fbb09-236">Each policy blocks communication one way only.</span></span>

<span data-ttu-id="fbb09-237">예를 들어 세그먼트 A와 세그먼트 B 간의 통신을 차단 하려는 경우를 가정해 보겠습니다. 이 경우 세그먼트 A가 세그먼트 B와 통신 하는 것을 방지 하는 정책을 하나 정의한 다음, 두 번째 정책을 정의 하 여 세그먼트 B가 세그먼트 A와 통신 하는 것을 방지 합니다.</span><span class="sxs-lookup"><span data-stu-id="fbb09-237">For example, suppose you want to block communications between Segment A and Segment B. In this case, you define one policy preventing Segment A from communicating with Segment B, and then define a second policy to prevent Segment B from communicating with Segment A.</span></span>

1. <span data-ttu-id="fbb09-238">첫 번째 차단 정책을 정의 하려면 **InformationBarrierPolicy** Cmdlet에 **SegmentsBlocked** 매개 변수를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="fbb09-238">To define your first blocking policy, use the **New-InformationBarrierPolicy** cmdlet with the **SegmentsBlocked** parameter.</span></span> 

    <span data-ttu-id="fbb09-239">구문과`New-InformationBarrierPolicy -Name "policyname" -AssignedSegment "segmentname" -SegmentsBlocked "segmentname"`</span><span class="sxs-lookup"><span data-stu-id="fbb09-239">Syntax: `New-InformationBarrierPolicy -Name "policyname" -AssignedSegment "segmentname" -SegmentsBlocked "segmentname"`</span></span>

    <span data-ttu-id="fbb09-240">예제: `New-InformationBarrierPolicy -Name "Sales-Research" -AssignedSegment "Sales" -SegmentsBlocked "Research" -State Inactive`</span><span class="sxs-lookup"><span data-stu-id="fbb09-240">Example: `New-InformationBarrierPolicy -Name "Sales-Research" -AssignedSegment "Sales" -SegmentsBlocked "Research" -State Inactive`</span></span>

    <span data-ttu-id="fbb09-241">이 예에서는 *sales*라는 세그먼트에 대 한 *영업 조사* 라는 정책을 정의 했습니다.</span><span class="sxs-lookup"><span data-stu-id="fbb09-241">In this example, we defined a policy called *Sales-Research* for a segment called *Sales*.</span></span> <span data-ttu-id="fbb09-242">이 정책을 사용 하면 *영업* 직원이 *조사*라는 세그먼트에 있는 사람들과 통신할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="fbb09-242">When active and applied, this policy prevents people in *Sales* from communicating with people in a segment called *Research*.</span></span>

2. <span data-ttu-id="fbb09-243">두 번째 차단 세그먼트를 정의 하려면 **SegmentsBlocked** 매개 변수와 함께 **InformationBarrierPolicy** cmdlet을 사용 하 여 세그먼트를 거꾸로 된 상태로 다시 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fbb09-243">To define your second blocking segment, use the **New-InformationBarrierPolicy** cmdlet with the **SegmentsBlocked** parameter again, this time with the segments reversed.</span></span>

    <span data-ttu-id="fbb09-244">예제: `New-InformationBarrierPolicy -Name "Research-Sales" -AssignedSegment "Research" -SegmentsBlocked "Sales" -State Inactive`</span><span class="sxs-lookup"><span data-stu-id="fbb09-244">Example: `New-InformationBarrierPolicy -Name "Research-Sales" -AssignedSegment "Research" -SegmentsBlocked "Sales" -State Inactive`</span></span>

    <span data-ttu-id="fbb09-245">이 예에서는 연구가 영업과의 통신을 방지 하기 위해 *research-Sales* 라는 정책을 정의 했습니다.</span><span class="sxs-lookup"><span data-stu-id="fbb09-245">In this example, we defined a policy called *Research-Sales* to prevent Research from communicating with Sales.</span></span>
 
2. <span data-ttu-id="fbb09-246">다음 중 하나로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="fbb09-246">Proceed to one of the following:</span></span>

   - <span data-ttu-id="fbb09-247">(필요한 경우) [다른 세그먼트 하나로만 통신할 수 있도록 정책 정의](#scenario-2-allow-a-segment-to-communicate-only-with-one-other-segment)</span><span class="sxs-lookup"><span data-stu-id="fbb09-247">(If needed) [Define a policy to allow a segment to communicate only with one other segment](#scenario-2-allow-a-segment-to-communicate-only-with-one-other-segment)</span></span> 
   - <span data-ttu-id="fbb09-248">(모든 정책이 정의 된 후) [정보 장벽 정책 적용](#part-3-apply-information-barrier-policies)</span><span class="sxs-lookup"><span data-stu-id="fbb09-248">(After all your policies are defined) [Apply information barrier policies](#part-3-apply-information-barrier-policies)</span></span>

### <a name="scenario-2-allow-a-segment-to-communicate-only-with-one-other-segment"></a><span data-ttu-id="fbb09-249">시나리오 2: 특정 세그먼트가 다른 세그먼트와만 통신할 수 있도록 허용</span><span class="sxs-lookup"><span data-stu-id="fbb09-249">Scenario 2: Allow a segment to communicate only with one other segment</span></span>

1. <span data-ttu-id="fbb09-250">하나의 세그먼트가 다른 하나의 세그먼트와만 통신할 수 있도록 하려면 **SegmentsAllowed** 매개 변수와 함께 **InformationBarrierPolicy** cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="fbb09-250">To allow one segment to communicate with only one other segment, use the **New-InformationBarrierPolicy** cmdlet with the **SegmentsAllowed** parameter.</span></span> 

    <span data-ttu-id="fbb09-251">구문과`New-InformationBarrierPolicy -Name "policyname" -AssignedSegment "segmentname" -SegmentsAllowed "segmentname"`</span><span class="sxs-lookup"><span data-stu-id="fbb09-251">Syntax: `New-InformationBarrierPolicy -Name "policyname" -AssignedSegment "segmentname" -SegmentsAllowed "segmentname"`</span></span>

    <span data-ttu-id="fbb09-252">예제: `New-InformationBarrierPolicy -Name "Manufacturing-HR" -AssignedSegment "Manufacturing" -SegmentsAllowed "HR" -State Inactive`</span><span class="sxs-lookup"><span data-stu-id="fbb09-252">Example: `New-InformationBarrierPolicy -Name "Manufacturing-HR" -AssignedSegment "Manufacturing" -SegmentsAllowed "HR" -State Inactive`</span></span>

    <span data-ttu-id="fbb09-253">이 예에서는 *manufacturing*이라는 세그먼트에 대해 *제조-HR* 이라는 정책을 정의 했습니다.</span><span class="sxs-lookup"><span data-stu-id="fbb09-253">In this example, we defined a policy called *Manufacturing-HR* for a segment called *Manufacturing*.</span></span> <span data-ttu-id="fbb09-254">이 정책을 사용 하면 *제조* 중인 사용자가 *HR*이라는 세그먼트에 있는 사용자와만 통신할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fbb09-254">When active and applied, this policy allows people in *Manufacturing* to communicate only with people in a segment called *HR*.</span></span> <span data-ttu-id="fbb09-255">(이 경우, Manufacturing은 HR에 속하지 않는 사용자와 통신할 수 없습니다.)</span><span class="sxs-lookup"><span data-stu-id="fbb09-255">(In this case, Manufacturing cannot communicate with users who are not part of HR.)</span></span>

    <span data-ttu-id="fbb09-256">**필요한 경우 다음의 두 예에 표시 된 것 처럼이 cmdlet을 사용 하 여 여러 세그먼트를 지정할 수 있습니다.**</span><span class="sxs-lookup"><span data-stu-id="fbb09-256">**If needed, you can specify multiple segments with this cmdlet, as shown in the following two examples.**</span></span>

    <span data-ttu-id="fbb09-257">구문과`New-InformationBarrierPolicy -Name "policyname" -AssignedSegment "segmentname" -SegmentsAllowed "segmentname, segmentname"`</span><span class="sxs-lookup"><span data-stu-id="fbb09-257">Syntax: `New-InformationBarrierPolicy -Name "policyname" -AssignedSegment "segmentname" -SegmentsAllowed "segmentname, segmentname"`</span></span>

    <span data-ttu-id="fbb09-258">**예 1: 여러 세그먼트가 다른 세그먼트 한 개와만 통신할 수 있도록 하는 정책 정의**</span><span class="sxs-lookup"><span data-stu-id="fbb09-258">**Example 1: Define a policy to allow multiple segments to communicate with only one other segment**</span></span>

    `New-InformationBarrierPolicy -Name "ResearchManufacturing-HR" -AssignedSegment "Research, Manufacturing" -SegmentsAllowed "HR" -State Inactive`

    <span data-ttu-id="fbb09-259">이 예에서는 *연구* 및 *제조* 부문에서 *HR*과의 통신을 허용 하는 정책을 정의 했습니다.</span><span class="sxs-lookup"><span data-stu-id="fbb09-259">In this example, we defined a policy that allows the *Research* and *Manufacturing* segments to communicate only with *HR*.</span></span>

    <span data-ttu-id="fbb09-260">**예 2: 여러 세그먼트가 특정 다른 세그먼트와도 통신할 수 있도록 정책을 정의 합니다.**</span><span class="sxs-lookup"><span data-stu-id="fbb09-260">**Example 2: Define a policy to allow multiple segments to communicate with only certain other segments**</span></span>    

    `New-InformationBarrierPolicy -Name "SalesMarketing-HRManufacturing" -AssignedSegment "Sales, Marketing" -SegmentsAllowed "HR, Manufacturing" -State Inactive`

    <span data-ttu-id="fbb09-261">이 예에서는 *영업* 및 *마케팅* 세그먼트가 *HR* 및 *제조*와도 통신할 수 있도록 하는 정책을 정의 했습니다.</span><span class="sxs-lookup"><span data-stu-id="fbb09-261">In this example, we defined a policy that allows the *Sales* and *Marketing* segments to communicate with only *HR* and *Manufacturing*.</span></span>

    <span data-ttu-id="fbb09-262">특정 세그먼트가 다른 특정 세그먼트와만 통신할 수 있도록 정의 하려는 각 정책에 대해이 단계를 반복 합니다.</span><span class="sxs-lookup"><span data-stu-id="fbb09-262">Repeat this step for each policy you want to define to allow specific segments to communicate with only certain other specific segments.</span></span>

2. <span data-ttu-id="fbb09-263">다음 중 하나로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="fbb09-263">Proceed to one of the following:</span></span>

   - <span data-ttu-id="fbb09-264">(필요한 경우) [세그먼트 간 통신을 차단 하는 정책 정의](#scenario-1-block-communications-between-segments)</span><span class="sxs-lookup"><span data-stu-id="fbb09-264">(If needed) [Define a policy to block communications between segments](#scenario-1-block-communications-between-segments)</span></span> 
   - <span data-ttu-id="fbb09-265">(모든 정책이 정의 된 후) [정보 장벽 정책 적용](#part-3-apply-information-barrier-policies)</span><span class="sxs-lookup"><span data-stu-id="fbb09-265">(After all your policies are defined) [Apply information barrier policies](#part-3-apply-information-barrier-policies)</span></span>

## <a name="part-3-apply-information-barrier-policies"></a><span data-ttu-id="fbb09-266">3 부: 정보 장벽 정책 적용</span><span class="sxs-lookup"><span data-stu-id="fbb09-266">Part 3: Apply information barrier policies</span></span>

<span data-ttu-id="fbb09-267">정보 장벽 정책은 활성 상태로 설정 하 고 정책을 적용할 때까지 적용 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fbb09-267">Information barrier policies are not in effect until you set them to active status, and then apply the policies.</span></span>

1. <span data-ttu-id="fbb09-268">**InformationBarrierPolicy** cmdlet을 사용 하 여 정의 된 정책 목록을 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fbb09-268">Use the **Get-InformationBarrierPolicy** cmdlet to see a list of policies that have been defined.</span></span> <span data-ttu-id="fbb09-269">각 정책의 상태 및 id (GUID)를 적어둡니다.</span><span class="sxs-lookup"><span data-stu-id="fbb09-269">Note the status and identity (GUID) of each policy.</span></span>

    <span data-ttu-id="fbb09-270">구문과`Get-InformationBarrierPolicy`</span><span class="sxs-lookup"><span data-stu-id="fbb09-270">Syntax: `Get-InformationBarrierPolicy`</span></span>

2. <span data-ttu-id="fbb09-271">정책을 활성 상태로 설정 하려면 **Identity** 매개 변수와 함께 **InformationBarrierPolicy** cmdlet을 사용 하 고 **State** 매개 변수를 **active**로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fbb09-271">To set a policy to active status, use the **Set-InformationBarrierPolicy** cmdlet with an **Identity** parameter, and the **State** parameter set to **Active**.</span></span> 

    <span data-ttu-id="fbb09-272">구문과`Set-InformationBarrierPolicy -Identity GUID -State Active`</span><span class="sxs-lookup"><span data-stu-id="fbb09-272">Syntax: `Set-InformationBarrierPolicy -Identity GUID -State Active`</span></span>

    <span data-ttu-id="fbb09-273">예제: `Set-InformationBarrierPolicy -Identity 43c37853-ea10-4b90-a23d-ab8c93772471 -State Active`</span><span class="sxs-lookup"><span data-stu-id="fbb09-273">Example: `Set-InformationBarrierPolicy -Identity 43c37853-ea10-4b90-a23d-ab8c93772471 -State Active`</span></span>
    
    <span data-ttu-id="fbb09-274">이 예에서는 GUID가 *43c37853-ea10-4b90-a23d-ab8c93772471* 인 정보 장벽 정책을 active status로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fbb09-274">In this example, we set an information barrier policy that has the GUID *43c37853-ea10-4b90-a23d-ab8c93772471* to active status.</span></span>

    <span data-ttu-id="fbb09-275">각 정책에 대해 적절 하 게이 단계를 반복 합니다.</span><span class="sxs-lookup"><span data-stu-id="fbb09-275">Repeat this step as appropriate for each policy.</span></span>

3. <span data-ttu-id="fbb09-276">정보 장벽 정책 설정이 활성 상태로 끝나면 Office 365 보안 & 준수 센터의 **InformationBarrierPoliciesApplication** cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="fbb09-276">When you have finished setting your information barrier policies to active status, use the **Start-InformationBarrierPoliciesApplication** cmdlet in the Office 365 Security & Compliance Center.</span></span>

    <span data-ttu-id="fbb09-277">구문과`Start-InformationBarrierPoliciesApplication`</span><span class="sxs-lookup"><span data-stu-id="fbb09-277">Syntax: `Start-InformationBarrierPoliciesApplication`</span></span>

    <span data-ttu-id="fbb09-278">약 1 시간 후에는 조직에 대해 사용자에 게 정책이 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="fbb09-278">After approximately a half hour, policies are applied, user by user, for your organization.</span></span> <span data-ttu-id="fbb09-279">대규모 조직에서는이 프로세스를 완료 하는 데 24 시간 이상 소요 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fbb09-279">If your organization is large, it can take 24 hours (or more) for this process to complete.</span></span> <span data-ttu-id="fbb09-280">일반적으로 5000 사용자 계정을 처리 하는 데 한 시간 정도 소요 됩니다.</span><span class="sxs-lookup"><span data-stu-id="fbb09-280">(As a general guideline, it takes about an hour to process 5,000 user accounts.)</span></span>

## <a name="view-status-of-user-accounts-segments-policies-or-policy-application"></a><span data-ttu-id="fbb09-281">사용자 계정, 세그먼트, 정책 또는 정책 응용 프로그램의 상태 보기</span><span class="sxs-lookup"><span data-stu-id="fbb09-281">View status of user accounts, segments, policies, or policy application</span></span>

<span data-ttu-id="fbb09-282">PowerShell을 사용 하 여 다음 표에 나와 있는 것 처럼 사용자 계정, 세그먼트, 정책 및 정책 응용 프로그램의 상태를 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fbb09-282">With PowerShell, you can view status of user accounts, segments, policies, and policy application, as listed in the following table.</span></span>

|<span data-ttu-id="fbb09-283">이를 보려면</span><span class="sxs-lookup"><span data-stu-id="fbb09-283">To view this</span></span>  |<span data-ttu-id="fbb09-284">수행 작업</span><span class="sxs-lookup"><span data-stu-id="fbb09-284">Do this</span></span>  |
|---------|---------|
|<span data-ttu-id="fbb09-285">사용자 계정</span><span class="sxs-lookup"><span data-stu-id="fbb09-285">User accounts</span></span>     |<span data-ttu-id="fbb09-286">Identity 매개 변수와 함께 **InformationBarrierRecipientStatus** cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="fbb09-286">Use the **Get-InformationBarrierRecipientStatus** cmdlet with Identity parameters.</span></span> <p><span data-ttu-id="fbb09-287">구문과`Get-InformationBarrierRecipientStatus -Identity <value> -Identity2 <value>`</span><span class="sxs-lookup"><span data-stu-id="fbb09-287">Syntax: `Get-InformationBarrierRecipientStatus -Identity <value> -Identity2 <value>`</span></span> <p><span data-ttu-id="fbb09-288">이름, 별칭, 고유 이름, 정식 도메인 이름, 전자 메일 주소 또는 GUID와 같은 각 사용자를 고유 하 게 식별 하는 모든 값을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fbb09-288">You can use any value that uniquely identifies each user, such as name, alias, distinguished name, canonical domain name, email address, or GUID.</span></span> <p><span data-ttu-id="fbb09-289">예제: `Get-InformationBarrierRecipientStatus -Identity meganb -Identity2 alexw`</span><span class="sxs-lookup"><span data-stu-id="fbb09-289">Example: `Get-InformationBarrierRecipientStatus -Identity meganb -Identity2 alexw`</span></span> <p><span data-ttu-id="fbb09-290">이 예에서는 Office 365의 두 사용자 계정 ( *Megan*용 *meganb* 및 *Alex*용 *alexw* )을 참조 합니다.</span><span class="sxs-lookup"><span data-stu-id="fbb09-290">In this example, we refer to two user accounts in Office 365: *meganb* for *Megan*, and *alexw* for *Alex*.</span></span> <p><span data-ttu-id="fbb09-291">(단일 사용자에 대해이 cmdlet을 사용할 수도 있습니다. `Get-InformationBarrierRecipientStatus -Identity <value>`)</span><span class="sxs-lookup"><span data-stu-id="fbb09-291">(You can also use this cmdlet for a single user: `Get-InformationBarrierRecipientStatus -Identity <value>`)</span></span> <p><span data-ttu-id="fbb09-292">이 cmdlet은 특성 값 및 적용 되는 정보 장벽 정책과 같은 사용자에 대 한 정보를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="fbb09-292">This cmdlet returns information about users, such as attribute values and any information barrier policies that are applied.</span></span>|
|<span data-ttu-id="fbb09-293">세그먼트</span><span class="sxs-lookup"><span data-stu-id="fbb09-293">Segments</span></span>     |<span data-ttu-id="fbb09-294">**OrganizationSegment** cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="fbb09-294">Use the **Get-OrganizationSegment** cmdlet.</span></span><p><span data-ttu-id="fbb09-295">구문과`Get-OrganizationSegment`</span><span class="sxs-lookup"><span data-stu-id="fbb09-295">Syntax: `Get-OrganizationSegment`</span></span> <p><span data-ttu-id="fbb09-296">이렇게 하면 조직에 대해 정의 된 모든 세그먼트의 목록이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="fbb09-296">This will display a list of all segments defined for your organization.</span></span>         |
|<span data-ttu-id="fbb09-297">정보 장벽 정책</span><span class="sxs-lookup"><span data-stu-id="fbb09-297">Information barrier policies</span></span>     |<span data-ttu-id="fbb09-298">**InformationBarrierPolicy** cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="fbb09-298">Use the **Get-InformationBarrierPolicy** cmdlet.</span></span> <p> <span data-ttu-id="fbb09-299">구문과`Get-InformationBarrierPolicy`</span><span class="sxs-lookup"><span data-stu-id="fbb09-299">Syntax: `Get-InformationBarrierPolicy`</span></span> <p><span data-ttu-id="fbb09-300">이렇게 하면 정의 된 정보 장벽 정책 목록과 해당 상태가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="fbb09-300">This will display a list of information barrier policies that were defined, and their status.</span></span>       |
|<span data-ttu-id="fbb09-301">가장 최근 정보 장벽 정책 응용 프로그램</span><span class="sxs-lookup"><span data-stu-id="fbb09-301">The most recent information barrier policy application</span></span>     | <span data-ttu-id="fbb09-302">**InformationBarrierPoliciesApplicationStatus** cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="fbb09-302">Use the **Get-InformationBarrierPoliciesApplicationStatus** cmdlet.</span></span> <p><span data-ttu-id="fbb09-303">구문과`Get-InformationBarrierPoliciesApplicationStatus`</span><span class="sxs-lookup"><span data-stu-id="fbb09-303">Syntax: `Get-InformationBarrierPoliciesApplicationStatus`</span></span><p>    <span data-ttu-id="fbb09-304">이렇게 하면 정책 응용 프로그램이 완료, 실패 또는 진행 중인지에 대 한 정보가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="fbb09-304">This will display information about whether policy application completed, failed, or is in progress.</span></span>       |
|<span data-ttu-id="fbb09-305">모든 정보 장벽 정책 응용 프로그램</span><span class="sxs-lookup"><span data-stu-id="fbb09-305">All information barrier policy applications</span></span>|<span data-ttu-id="fbb09-306">하십시오`Get-InformationBarrierPoliciesApplicationStatus -All $true`</span><span class="sxs-lookup"><span data-stu-id="fbb09-306">Use `Get-InformationBarrierPoliciesApplicationStatus -All $true`</span></span><p><span data-ttu-id="fbb09-307">이렇게 하면 정책 응용 프로그램이 완료, 실패 또는 진행 중인지에 대 한 정보가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="fbb09-307">This will display information about whether policy application completed, failed, or is in progress.</span></span>|

## <a name="stop-a-policy-application"></a><span data-ttu-id="fbb09-308">정책 응용 프로그램 중지</span><span class="sxs-lookup"><span data-stu-id="fbb09-308">Stop a policy application</span></span>

<span data-ttu-id="fbb09-309">정보 장벽 정책 적용을 시작 하 고 나면 해당 정책을 적용 하지 않으려면 다음 절차를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="fbb09-309">If, after you have started applying information barrier policies, you want to stop those policies from being applied, use the following procedure.</span></span> <span data-ttu-id="fbb09-310">프로세스를 시작 하는 데 약 30-35 분이 소요 됨을 염두에 두어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="fbb09-310">Keep in mind that it will take approximately 30-35 minutes for the process to begin.</span></span>

1. <span data-ttu-id="fbb09-311">가장 최근 정보 장벽 정책 응용 프로그램의 상태를 확인 하려면 **InformationBarrierPoliciesApplicationStatus** cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="fbb09-311">To view the status of the most recent information barrier policy application, use the **Get-InformationBarrierPoliciesApplicationStatus** cmdlet.</span></span>

    <span data-ttu-id="fbb09-312">구문과`Get-InformationBarrierPoliciesApplicationStatus`</span><span class="sxs-lookup"><span data-stu-id="fbb09-312">Syntax: `Get-InformationBarrierPoliciesApplicationStatus`</span></span>

    <span data-ttu-id="fbb09-313">응용 프로그램의 GUID를 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="fbb09-313">Note the application's GUID.</span></span>

2. <span data-ttu-id="fbb09-314">**InformationBarrierPoliciesApplication** Cmdlet을 Identity 매개 변수와 함께 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="fbb09-314">Use the **Stop-InformationBarrierPoliciesApplication** cmdlet with an Identity parameter.</span></span>

    <span data-ttu-id="fbb09-315">구문과`Stop-InformationBarrierPoliciesApplication -Identity GUID`</span><span class="sxs-lookup"><span data-stu-id="fbb09-315">Syntax:  `Stop-InformationBarrierPoliciesApplication -Identity GUID`</span></span>

    <span data-ttu-id="fbb09-316">예제: `InformationBarrierPoliciesApplication -Identity 46237888-12ca-42e3-a541-3fcb7b5231d1`</span><span class="sxs-lookup"><span data-stu-id="fbb09-316">Example: `InformationBarrierPoliciesApplication -Identity 46237888-12ca-42e3-a541-3fcb7b5231d1`</span></span>

## <a name="edit-a-segment-or-a-policy"></a><span data-ttu-id="fbb09-317">세그먼트 또는 정책 편집</span><span class="sxs-lookup"><span data-stu-id="fbb09-317">Edit a segment or a policy</span></span>

### <a name="edit-a-segment"></a><span data-ttu-id="fbb09-318">세그먼트 편집</span><span class="sxs-lookup"><span data-stu-id="fbb09-318">Edit a segment</span></span>

1. <span data-ttu-id="fbb09-319">모든 기존 세그먼트를 보려면 **OrganizationSegment** cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="fbb09-319">To view all existing segments, use the **Get-OrganizationSegment** cmdlet.</span></span>
    
    <span data-ttu-id="fbb09-320">구문과`Get-OrganizationSegment`</span><span class="sxs-lookup"><span data-stu-id="fbb09-320">Syntax: `Get-OrganizationSegment`</span></span>

    <span data-ttu-id="fbb09-321">세그먼트 유형, UserGroupFilter 값, 해당 개체를 만들거나 마지막으로 수정한 사람, GUID 등의 각 세그먼트와 세부 정보에 대 한 목록이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="fbb09-321">You will see a list of segments and details for each, such as segment type, its UserGroupFilter value, who created or last modified it, GUID, and so on.</span></span>

    > [!TIP]
    > <span data-ttu-id="fbb09-322">나중에 참조 하기 위해 세그먼트 목록을 인쇄 하거나 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="fbb09-322">Print or save your list of segments for reference later.</span></span> <span data-ttu-id="fbb09-323">예를 들어 세그먼트를 편집 하려면 해당 이름을 확인 하거나 값을 식별 해야 합니다 (이는 Identity 매개 변수와 함께 사용 됨).</span><span class="sxs-lookup"><span data-stu-id="fbb09-323">For example, if you want to edit a segment, you will need to know its name or identify value (this is used with the Identity parameter).</span></span>

2. <span data-ttu-id="fbb09-324">세그먼트를 편집 하려면 **Identity** 매개 변수와 관련 세부 정보와 함께 **OrganizationSegment** cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="fbb09-324">To edit a segment, use the **Set-OrganizationSegment** cmdlet with the **Identity** parameter and relevant details.</span></span> 

    <span data-ttu-id="fbb09-325">구문과`Set-OrganizationSegment -Identity GUID -UserGroupFilter "attribute -eq 'attributevalue'"`</span><span class="sxs-lookup"><span data-stu-id="fbb09-325">Syntax: `Set-OrganizationSegment -Identity GUID -UserGroupFilter "attribute -eq 'attributevalue'"`</span></span>

    <span data-ttu-id="fbb09-326">예제: `Set-OrganizationSegment -Identity c96e0837-c232-4a8a-841e-ef45787d8fcd -UserGroupFilter "Department -eq 'HRDept'"`</span><span class="sxs-lookup"><span data-stu-id="fbb09-326">Example: `Set-OrganizationSegment -Identity c96e0837-c232-4a8a-841e-ef45787d8fcd -UserGroupFilter "Department -eq 'HRDept'"`</span></span>

    <span data-ttu-id="fbb09-327">이 예에서는 GUID가 *c96e0837-c232-4a8a-841e-ef45787d8fcd*인 세그먼트에 대해 부서 이름을 "hrdept"로 업데이트 했습니다.</span><span class="sxs-lookup"><span data-stu-id="fbb09-327">In this example, for the segment that has the GUID *c96e0837-c232-4a8a-841e-ef45787d8fcd*, we updated the department name to "HRDept".</span></span>

<span data-ttu-id="fbb09-328">조직의 세그먼트 편집을 마친 후에는 정보 장벽 정책 [정의](#part-2-define-information-barrier-policies) 또는 [편집](#edit-a-policy) 을 진행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fbb09-328">When you have finished editing segments for your organization, you can proceed to [define](#part-2-define-information-barrier-policies) or [edit](#edit-a-policy) information barrier policies.</span></span>

### <a name="edit-a-policy"></a><span data-ttu-id="fbb09-329">정책 편집</span><span class="sxs-lookup"><span data-stu-id="fbb09-329">Edit a policy</span></span>

1. <span data-ttu-id="fbb09-330">현재 정보 장벽 정책 목록을 보려면 **InformationBarrierPolicy** cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="fbb09-330">To view a list of current information barrier policies, use the **Get-InformationBarrierPolicy** cmdlet.</span></span>

    <span data-ttu-id="fbb09-331">구문과`Get-InformationBarrierPolicy`</span><span class="sxs-lookup"><span data-stu-id="fbb09-331">Syntax: `Get-InformationBarrierPolicy`</span></span>

    <span data-ttu-id="fbb09-332">결과 목록에서 변경 하려는 정책을 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="fbb09-332">In the list of results, identify the policy that you want to change.</span></span> <span data-ttu-id="fbb09-333">정책의 GUID 및 이름을 적어둡니다.</span><span class="sxs-lookup"><span data-stu-id="fbb09-333">Note the policy's GUID and name.</span></span>

2. <span data-ttu-id="fbb09-334">**InformationBarrierPolicy** Cmdlet에서 **Identity** 매개 변수를 사용 하 여 변경할 내용을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fbb09-334">Use the **Set-InformationBarrierPolicy** cmdlet with an **Identity** parameter, and specify the changes you want to make.</span></span>

    <span data-ttu-id="fbb09-335">구문 (차단 세그먼트가 다른 세그먼트와 통신할 때):</span><span class="sxs-lookup"><span data-stu-id="fbb09-335">Syntax (blocking segments from communicating with other segments):</span></span> 

    `Set-InformationBarrierPolicy -Identity GUID -SegmentsBlocked "segmentname, segmentname"` 

    <span data-ttu-id="fbb09-336">구문 (세그먼트가 특정 세그먼트와만 통신할 수 있도록 설정):</span><span class="sxs-lookup"><span data-stu-id="fbb09-336">Syntax (enabling segments to communicate only with certain other segments):</span></span>
    
    ``Set-InformationBarrierPolicy -Identity GUID -SegmentsAllowed "segmentname, segmentname"``

    <span data-ttu-id="fbb09-337">예: 정책이 영업 및 마케팅과의 의견 교환에 대 한 조사를 차단 하도록 정의 되었다고 가정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fbb09-337">Example: Suppose a policy was defined to block Research from communicating with Sales and Marketing.</span></span> <span data-ttu-id="fbb09-338">이 cmdlet을 사용 하 여 정책이 정의 되었습니다.`New-InformationBarrierPolicy -Name "Research-SalesMarketing" -AssignedSegment "Research" -SegmentsBlocked "Sales, Marketing"`</span><span class="sxs-lookup"><span data-stu-id="fbb09-338">The policy was defined by using this cmdlet: `New-InformationBarrierPolicy -Name "Research-SalesMarketing" -AssignedSegment "Research" -SegmentsBlocked "Sales, Marketing"`</span></span>
    
    <span data-ttu-id="fbb09-339">리서치 담당자가 HR 사용자와만 통신할 수 있도록이를 변경 하려는 경우를 가정해 보겠습니다.</span><span class="sxs-lookup"><span data-stu-id="fbb09-339">Suppose we want to change it so that people in Research can only communicate with people in HR.</span></span> <span data-ttu-id="fbb09-340">이 변경 작업을 수행 하려면 다음 cmdlet을 사용 합니다.`Set-InformationBarrierPolicy -Identity 43c37853-ea10-4b90-a23d-ab8c93772471 -SegmentsAllowed "HR"`</span><span class="sxs-lookup"><span data-stu-id="fbb09-340">To make this change, we use this cmdlet: `Set-InformationBarrierPolicy -Identity 43c37853-ea10-4b90-a23d-ab8c93772471 -SegmentsAllowed "HR"`</span></span>

3. <span data-ttu-id="fbb09-341">정책 편집을 마친 후에는 변경 내용을 적용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="fbb09-341">When you are finished editing a policy, make sure to apply your changes.</span></span> <span data-ttu-id="fbb09-342">( [정보 장벽 정책 적용](#part-3-apply-information-barrier-policies)참조)</span><span class="sxs-lookup"><span data-stu-id="fbb09-342">(See [Apply information barrier policies](#part-3-apply-information-barrier-policies).)</span></span>

### <a name="remove-a-policy"></a><span data-ttu-id="fbb09-343">정책 제거</span><span class="sxs-lookup"><span data-stu-id="fbb09-343">Remove a policy</span></span>

1. <span data-ttu-id="fbb09-344">현재 정보 장벽 정책 목록을 보려면 **InformationBarrierPolicy** cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="fbb09-344">To view a list of current information barrier policies, use the **Get-InformationBarrierPolicy** cmdlet.</span></span>

    <span data-ttu-id="fbb09-345">구문과`Get-InformationBarrierPolicy`</span><span class="sxs-lookup"><span data-stu-id="fbb09-345">Syntax: `Get-InformationBarrierPolicy`</span></span>

    <span data-ttu-id="fbb09-346">결과 목록에서 제거할 정책을 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="fbb09-346">In the list of results, identify the policy that you want to remove.</span></span> <span data-ttu-id="fbb09-347">정책의 GUID 및 이름을 적어둡니다.</span><span class="sxs-lookup"><span data-stu-id="fbb09-347">Note the policy's GUID and name.</span></span> <span data-ttu-id="fbb09-348">정책이 비활성 상태로 설정 되어 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="fbb09-348">Make sure the policy is set to inactive status.</span></span>

2. <span data-ttu-id="fbb09-349">**InformationBarrierPolicy** Cmdlet을 Identity 매개 변수와 함께 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="fbb09-349">Use the **Remove-InformationBarrierPolicy** cmdlet with an Identity parameter.</span></span>

    <span data-ttu-id="fbb09-350">구문과`Remove-InformationBarrierPolicy -Identity GUID`</span><span class="sxs-lookup"><span data-stu-id="fbb09-350">Syntax: `Remove-InformationBarrierPolicy -Identity GUID`</span></span>

    <span data-ttu-id="fbb09-351">예: GUID *43c37853-ea10-4b90-a23d-ab8c93772471*가 있는 정책을 제거 하려고 한다고 가정 합시다.</span><span class="sxs-lookup"><span data-stu-id="fbb09-351">Example: Suppose we want to remove a policy that has GUID *43c37853-ea10-4b90-a23d-ab8c93772471*.</span></span> <span data-ttu-id="fbb09-352">이렇게 하려면 다음과 같은 cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="fbb09-352">To do this, we use this cmdlet:</span></span>
    
    `Remove-InformationBarrierPolicy -Identity 43c37853-ea10-4b90-a23d-ab8c93772471`

    <span data-ttu-id="fbb09-353">메시지가 표시 되 면 변경 내용을 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="fbb09-353">When prompted, confirm the change.</span></span>

3. <span data-ttu-id="fbb09-354">제거할 각 정책에 대해 1-2 단계를 반복 합니다.</span><span class="sxs-lookup"><span data-stu-id="fbb09-354">Repeat steps 1-2 for each policy you want to remove.</span></span>

4. <span data-ttu-id="fbb09-355">정책을 제거한 후에는 변경 내용을 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="fbb09-355">When you are finished removing policies, apply your changes.</span></span> <span data-ttu-id="fbb09-356">이 작업을 수행 하려면 **InformationBarrierPoliciesApplication** cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="fbb09-356">To do this, use the **Start-InformationBarrierPoliciesApplication** cmdlet.</span></span>

    <span data-ttu-id="fbb09-357">구문과`Start-InformationBarrierPoliciesApplication`</span><span class="sxs-lookup"><span data-stu-id="fbb09-357">Syntax: `Start-InformationBarrierPoliciesApplication`</span></span>

    <span data-ttu-id="fbb09-358">사용자가 조직에 대해 변경 내용을 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="fbb09-358">Changes are applied, user by user, for your organization.</span></span> <span data-ttu-id="fbb09-359">대규모 조직에서는이 프로세스를 완료 하는 데 24 시간 이상 소요 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fbb09-359">If your organization is large, it can take 24 hours (or more) for this process to complete.</span></span>

### <a name="set-a-policy-to-inactive-status"></a><span data-ttu-id="fbb09-360">정책을 비활성 상태로 설정</span><span class="sxs-lookup"><span data-stu-id="fbb09-360">Set a policy to inactive status</span></span>

1. <span data-ttu-id="fbb09-361">현재 정보 장벽 정책 목록을 보려면 **InformationBarrierPolicy** cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="fbb09-361">To view a list of current information barrier policies, use the **Get-InformationBarrierPolicy** cmdlet.</span></span>

    <span data-ttu-id="fbb09-362">구문과`Get-InformationBarrierPolicy`</span><span class="sxs-lookup"><span data-stu-id="fbb09-362">Syntax: `Get-InformationBarrierPolicy`</span></span>

    <span data-ttu-id="fbb09-363">결과 목록에서 변경 하거나 제거할 정책을 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="fbb09-363">In the list of results, identify the policy that you want to change (or remove).</span></span> <span data-ttu-id="fbb09-364">정책의 GUID 및 이름을 적어둡니다.</span><span class="sxs-lookup"><span data-stu-id="fbb09-364">Note the policy's GUID and name.</span></span>

2. <span data-ttu-id="fbb09-365">정책의 상태를 비활성으로 설정 하려면 Identity 매개 변수와 함께 **InformationBarrierPolicy** cmdlet을 사용 하 고 State 매개 변수는 비활성으로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fbb09-365">To set the policy's status to inactive, use the **Set-InformationBarrierPolicy** cmdlet with an Identity parameter and the State parameter set to Inactive.</span></span>

    <span data-ttu-id="fbb09-366">구문과`Set-InformationBarrierPolicy -Identity GUID -State Inactive`</span><span class="sxs-lookup"><span data-stu-id="fbb09-366">Syntax: `Set-InformationBarrierPolicy -Identity GUID -State Inactive`</span></span>

    `Set-InformationBarrierPolicy -Identity 43c37853-ea10-4b90-a23d-ab8c9377247 -State Inactive`

    <span data-ttu-id="fbb09-367">이 예에서는 GUID *43c37853-ea10-4b90-a23d-ab8c9377247을 사용* 하는 정보 장벽 정책을 비활성 상태로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fbb09-367">In this example, we set an information barrier policy that has GUID *43c37853-ea10-4b90-a23d-ab8c9377247* to an inactive status.</span></span>

3. <span data-ttu-id="fbb09-368">변경 내용을 적용 하려면 **InformationBarrierPoliciesApplication** cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="fbb09-368">To apply your changes, use the **Start-InformationBarrierPoliciesApplication** cmdlet.</span></span>

    <span data-ttu-id="fbb09-369">구문과`Start-InformationBarrierPoliciesApplication`</span><span class="sxs-lookup"><span data-stu-id="fbb09-369">Syntax: `Start-InformationBarrierPoliciesApplication`</span></span>

    <span data-ttu-id="fbb09-370">사용자가 조직에 대해 변경 내용을 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="fbb09-370">Changes are applied, user by user, for your organization.</span></span> <span data-ttu-id="fbb09-371">대규모 조직에서는이 프로세스를 완료 하는 데 24 시간 이상 소요 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fbb09-371">If your organization is large, it can take 24 hours (or more) for this process to complete.</span></span> <span data-ttu-id="fbb09-372">일반적으로 5000 사용자 계정을 처리 하는 데 한 시간 정도 소요 됩니다.</span><span class="sxs-lookup"><span data-stu-id="fbb09-372">(As a general guideline, it takes about an hour to process 5,000 user accounts.)</span></span>

<span data-ttu-id="fbb09-373">이때 하나 이상의 정보 장벽 정책이 비활성 상태로 설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="fbb09-373">At this point, one or more information barrier policies are set to inactive status.</span></span> <span data-ttu-id="fbb09-374">여기서는 다음 작업을 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fbb09-374">From here, you can do any of the following:</span></span>
- <span data-ttu-id="fbb09-375">그대로 유지 (비활성 상태로 설정 된 정책이 사용자에 게 영향을 주지 않음)</span><span class="sxs-lookup"><span data-stu-id="fbb09-375">Leave it as is (a policy set to inactive status has no effect on users)</span></span>
- [<span data-ttu-id="fbb09-376">정책 편집</span><span class="sxs-lookup"><span data-stu-id="fbb09-376">Edit a policy</span></span>](#edit-a-policy) 
- [<span data-ttu-id="fbb09-377">정책 제거</span><span class="sxs-lookup"><span data-stu-id="fbb09-377">Remove a policy</span></span>](#remove-a-policy)

## <a name="example-contosos-departments-segments-and-policies"></a><span data-ttu-id="fbb09-378">예: Contoso의 부서, 세그먼트 및 정책</span><span class="sxs-lookup"><span data-stu-id="fbb09-378">Example: Contoso's departments, segments, and policies</span></span>

<span data-ttu-id="fbb09-379">조직에서 세그먼트와 정책을 정의 하는 방법에 대 한 자세한 내용은 다음 예를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="fbb09-379">To see how an organization might approach defining segments and policies, consider the following example.</span></span>

### <a name="contosos-departments-and-plan"></a><span data-ttu-id="fbb09-380">Contoso의 부서 및 계획</span><span class="sxs-lookup"><span data-stu-id="fbb09-380">Contoso's departments and plan</span></span>

<span data-ttu-id="fbb09-381">Contoso에는 HR, Sales, Marketing, Research 및 Manufacturing의 다섯 가지 부서가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fbb09-381">Contoso has five departments: HR, Sales, Marketing, Research, and Manufacturing.</span></span> <span data-ttu-id="fbb09-382">업계 규정 준수를 유지 하기 위해 일부 부서의 사용자는 다음 표에 나열 된 것 처럼 다른 부서와 통신 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fbb09-382">In order to remain compliant with industry regulations, people in some departments are not supposed to communicate with other departments, as listed in the following table:</span></span>

|<span data-ttu-id="fbb09-383">단편</span><span class="sxs-lookup"><span data-stu-id="fbb09-383">Segment</span></span>  |<span data-ttu-id="fbb09-384">에 게 문의할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fbb09-384">Can talk to</span></span>  |<span data-ttu-id="fbb09-385">통신할 수 없음</span><span class="sxs-lookup"><span data-stu-id="fbb09-385">Cannot talk to</span></span>  |
|---------|---------|---------|
|<span data-ttu-id="fbb09-386">인력</span><span class="sxs-lookup"><span data-stu-id="fbb09-386">HR</span></span>     |<span data-ttu-id="fbb09-387">모든 사람</span><span class="sxs-lookup"><span data-stu-id="fbb09-387">Everyone</span></span>         |<span data-ttu-id="fbb09-388">(제한 없음)</span><span class="sxs-lookup"><span data-stu-id="fbb09-388">(no restrictions)</span></span>         |
|<span data-ttu-id="fbb09-389">세율</span><span class="sxs-lookup"><span data-stu-id="fbb09-389">Sales</span></span>     |<span data-ttu-id="fbb09-390">HR, 마케팅, 제조</span><span class="sxs-lookup"><span data-stu-id="fbb09-390">HR, Marketing, Manufacturing</span></span>         |<span data-ttu-id="fbb09-391">리서치</span><span class="sxs-lookup"><span data-stu-id="fbb09-391">Research</span></span>         |
|<span data-ttu-id="fbb09-392">마케팅</span><span class="sxs-lookup"><span data-stu-id="fbb09-392">Marketing</span></span>     |<span data-ttu-id="fbb09-393">모든 사람</span><span class="sxs-lookup"><span data-stu-id="fbb09-393">Everyone</span></span>         |<span data-ttu-id="fbb09-394">(제한 없음)</span><span class="sxs-lookup"><span data-stu-id="fbb09-394">(no restrictions)</span></span>         |
|<span data-ttu-id="fbb09-395">리서치</span><span class="sxs-lookup"><span data-stu-id="fbb09-395">Research</span></span>     |<span data-ttu-id="fbb09-396">HR, 마케팅, 제조</span><span class="sxs-lookup"><span data-stu-id="fbb09-396">HR, Marketing, Manufacturing</span></span>        |<span data-ttu-id="fbb09-397">세율</span><span class="sxs-lookup"><span data-stu-id="fbb09-397">Sales</span></span>     |
|<span data-ttu-id="fbb09-398">제조</span><span class="sxs-lookup"><span data-stu-id="fbb09-398">Manufacturing</span></span> |<span data-ttu-id="fbb09-399">HR, 마케팅</span><span class="sxs-lookup"><span data-stu-id="fbb09-399">HR, Marketing</span></span> |<span data-ttu-id="fbb09-400">HR 또는 Marketing 이외의 모든 사람</span><span class="sxs-lookup"><span data-stu-id="fbb09-400">Anyone other than HR or Marketing</span></span> |

<span data-ttu-id="fbb09-401">이러한 점을 고려 하 여 Contoso의 계획에는 다음과 같은 세 가지 정보 장벽 정책이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="fbb09-401">With this in mind, Contoso's plan includes three information barrier policies:</span></span>

1. <span data-ttu-id="fbb09-402">영업이 연구와의 통신을 차단 하 고, 다른 정책으로 영업과의 통신을 차단 하도록 설계 된 정책</span><span class="sxs-lookup"><span data-stu-id="fbb09-402">A policy designed to prevent Sales from communicating with Research (and another policy to prevent Research from communicating with Sales)</span></span>
2. <span data-ttu-id="fbb09-403">제조에서 HR 및 Marketing과의 통신을 허용 하도록 설계 된 정책</span><span class="sxs-lookup"><span data-stu-id="fbb09-403">A policy designed to allow Manufacturing to communicate with HR and Marketing only</span></span> 

<span data-ttu-id="fbb09-404">HR 또는 Marketing에 대 한 정책을 정의할 필요는 없습니다.</span><span class="sxs-lookup"><span data-stu-id="fbb09-404">It's not necessary to define policies for HR or Marketing.</span></span>

### <a name="contosos-defined-segments"></a><span data-ttu-id="fbb09-405">Contoso의 정의 된 세그먼트</span><span class="sxs-lookup"><span data-stu-id="fbb09-405">Contoso's defined segments</span></span>

<span data-ttu-id="fbb09-406">Contoso는 다음과 같이 Azure Active Directory에서 부서 특성을 사용 하 여 세그먼트를 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="fbb09-406">Contoso will use the Department attribute in Azure Active Directory to define segments, as follows:</span></span>

|<span data-ttu-id="fbb09-407">부서</span><span class="sxs-lookup"><span data-stu-id="fbb09-407">Department</span></span>  |<span data-ttu-id="fbb09-408">세그먼트 정의</span><span class="sxs-lookup"><span data-stu-id="fbb09-408">Segment Definition</span></span>  |
|---------|---------|
|<span data-ttu-id="fbb09-409">인력</span><span class="sxs-lookup"><span data-stu-id="fbb09-409">HR</span></span>     | `New-OrganizationSegment -Name "HR" -UserGroupFilter "Department -eq 'HR'"`        |
|<span data-ttu-id="fbb09-410">세율</span><span class="sxs-lookup"><span data-stu-id="fbb09-410">Sales</span></span>     | `New-OrganizationSegment -Name "Sales" -UserGroupFilter "Department -eq 'Sales'"`        |
|<span data-ttu-id="fbb09-411">마케팅</span><span class="sxs-lookup"><span data-stu-id="fbb09-411">Marketing</span></span>     | `New-OrganizationSegment -Name "Marketing" -UserGroupFilter "Department -eq 'Marketing'"`        |
|<span data-ttu-id="fbb09-412">리서치</span><span class="sxs-lookup"><span data-stu-id="fbb09-412">Research</span></span>     | `New-OrganizationSegment -Name "Research" -UserGroupFilter "Department -eq 'Research'"`        |
|<span data-ttu-id="fbb09-413">제조</span><span class="sxs-lookup"><span data-stu-id="fbb09-413">Manufacturing</span></span>     | `New-OrganizationSegment -Name "Manufacturing" -UserGroupFilter "Department -eq 'Manufacturing'"`        |

<span data-ttu-id="fbb09-414">정의 된 세그먼트가 있으면 Contoso는 정책 정의를 진행 합니다.</span><span class="sxs-lookup"><span data-stu-id="fbb09-414">With the segments defined, Contoso proceeds to define policies.</span></span> 

### <a name="contosos-information-barrier-policies"></a><span data-ttu-id="fbb09-415">Contoso의 정보 장벽 정책</span><span class="sxs-lookup"><span data-stu-id="fbb09-415">Contoso's information barrier policies</span></span>

<span data-ttu-id="fbb09-416">Contoso는 다음 표에 설명 된 세 가지 정책을 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="fbb09-416">Contoso defines three polices, as described in the following table:</span></span>

|<span data-ttu-id="fbb09-417">정책</span><span class="sxs-lookup"><span data-stu-id="fbb09-417">Policy</span></span>  |<span data-ttu-id="fbb09-418">정책 정의</span><span class="sxs-lookup"><span data-stu-id="fbb09-418">Policy Definition</span></span>  |
|---------|---------|
|<span data-ttu-id="fbb09-419">정책 1: 영업에서 연구와의 통신을 방지 합니다.</span><span class="sxs-lookup"><span data-stu-id="fbb09-419">Policy 1: Prevent Sales from communicating with Research</span></span>     | `New-InformationBarrierPolicy -Name "Sales-Research" -AssignedSegment "Sales" -SegmentsBlocked "Research" -State Inactive` <p> <span data-ttu-id="fbb09-420">이 예에서 정보 장벽 정책을 *판매 조사*라고 합니다.</span><span class="sxs-lookup"><span data-stu-id="fbb09-420">In this example, the information barrier policy is called *Sales-Research*.</span></span> <span data-ttu-id="fbb09-421">이 정책이 활성 상태이 고 적용 되 면 Sales 세그먼트에 있는 사용자가 리서치 세그먼트의 사용자와 통신할 수 없도록 하는 데 도움이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="fbb09-421">When this policy is active and applied, it will help prevent users who are in the Sales segment from communicating with users in the Research segment.</span></span> <span data-ttu-id="fbb09-422">이는 단방향 정책입니다. 이로 인해 연구가 영업과의 통신을 방지할 수는 없습니다.</span><span class="sxs-lookup"><span data-stu-id="fbb09-422">This is a one-way policy; it won't prevent Research from communicating with Sales.</span></span> <span data-ttu-id="fbb09-423">따라서 정책 2가 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="fbb09-423">For that, Policy 2 is needed.</span></span>      |
|<span data-ttu-id="fbb09-424">정책 2: 영업 담당자가 리서치를 진행 하지 못하도록 방지</span><span class="sxs-lookup"><span data-stu-id="fbb09-424">Policy 2: Prevent Research from communicating with Sales</span></span>     | `New-InformationBarrierPolicy -Name "Research-Sales" -AssignedSegment "Research" -SegmentsBlocked "Sales" -State Inactive` <p> <span data-ttu-id="fbb09-425">이 예에서는 정보 장벽 정책을 *리서치-판매*라고 합니다.</span><span class="sxs-lookup"><span data-stu-id="fbb09-425">In this example, the information barrier policy is called *Research-Sales*.</span></span> <span data-ttu-id="fbb09-426">이 정책이 활성화 및 적용 되 면 리서치 세그먼트에 있는 사용자가 Sales 세그먼트의 사용자와 통신할 수 없도록 하는 데 도움이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="fbb09-426">When this policy is active and applied, it will help prevent users who are in the Research segment from communicating with users in the Sales segment.</span></span>       |
|<span data-ttu-id="fbb09-427">정책 3: 제조에서 HR 및 마케팅과의 통신만 허용</span><span class="sxs-lookup"><span data-stu-id="fbb09-427">Policy 3: Allow Manufacturing to communicate with HR and Marketing only</span></span>     | `New-InformationBarrierPolicy -Name "Manufacturing-HRMarketing" -AssignedSegment "Manufacturing" -SegmentsAllowed "HR, Marketing" -State Inactive` <p><span data-ttu-id="fbb09-428">이 경우 정보 장벽 정책은 *제조-HRMarketing*이라고 합니다.</span><span class="sxs-lookup"><span data-stu-id="fbb09-428">In this case, the information barrier policy is called *Manufacturing-HRMarketing*.</span></span> <span data-ttu-id="fbb09-429">이 정책이 활성 상태이 고 적용 되 면 Manufacturing은 HR 및 Marketing과만 통신할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fbb09-429">When this policy is active and applied, Manufacturing can communicate only with HR and Marketing.</span></span> <span data-ttu-id="fbb09-430">HR 및 Marketing은 다른 세그먼트와 통신 하는 것이 제한 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fbb09-430">Note that HR and Marketing are not restricted from communicating with other segments.</span></span> |

<span data-ttu-id="fbb09-431">**InformationBarrierPoliciesApplication** cmdlet을 실행 하 여 모든 세그먼트와 정책을 정의 하 고, Contoso는 정책을 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="fbb09-431">With segments and policies defined, Contoso applies the policies by running the **Start-InformationBarrierPoliciesApplication** cmdlet.</span></span> 

<span data-ttu-id="fbb09-432">이 작업이 완료 되 면 Contoso는 법적 및 업계 요구 사항을 준수 합니다.</span><span class="sxs-lookup"><span data-stu-id="fbb09-432">When that finishes, Contoso is compliant with legal and industry requirements.</span></span>

## <a name="related-articles"></a><span data-ttu-id="fbb09-433">관련 문서</span><span class="sxs-lookup"><span data-stu-id="fbb09-433">Related articles</span></span>

[<span data-ttu-id="fbb09-434">정보 장벽에 대 한 개요 보기</span><span class="sxs-lookup"><span data-stu-id="fbb09-434">Get an overview of information barriers</span></span>](information-barriers.md)

[<span data-ttu-id="fbb09-435">Microsoft 팀의 정보 장벽에 대해 자세히 알아보기</span><span class="sxs-lookup"><span data-stu-id="fbb09-435">Learn more about information barriers in Microsoft Teams</span></span>](https://docs.microsoft.com/MicrosoftTeams/information-barriers-in-teams)

[<span data-ttu-id="fbb09-436">정보 장벽 정책의 특성 (미리 보기)</span><span class="sxs-lookup"><span data-stu-id="fbb09-436">Attributes for information barrier policies (Preview)</span></span>](information-barriers-attributes.md)

[<span data-ttu-id="fbb09-437">정보 장벽 문제 해결 (미리 보기)</span><span class="sxs-lookup"><span data-stu-id="fbb09-437">Troubleshooting information barriers (Preview)</span></span>](information-barriers-troubleshooting.md)
