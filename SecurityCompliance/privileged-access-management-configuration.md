---
title: Office 365에서 권한이 부여 된 액세스 관리 구성
ms.author: robmazz
author: robmazz
manager: laurawi
audience: ITPro
ms.topic: overview
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.collection:
- Strat_O365_IP
- M365-security-compliance
ms.custom: Ent_Solutions
ms.assetid: ''
description: 이 항목을 사용 하 여 Office 365에서 권한이 부여 된 액세스 관리 구성에 대 한 자세한 내용을 알아보세요.
ms.openlocfilehash: 46bfeaf0c73c4598fcdaa65d654201620396600c
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/17/2019
ms.locfileid: "34157420"
---
# <a name="configuring-privileged-access-management-in-office-365"></a><span data-ttu-id="6e13f-103">Office 365에서 권한이 부여 된 액세스 관리 구성</span><span class="sxs-lookup"><span data-stu-id="6e13f-103">Configuring privileged access management in Office 365</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6e13f-104">이 항목에서는 현재 Office 365 E5 및 고급 규정 준수 Sku에서 사용할 수 있는 기능에 대 한 배포 및 구성 지침에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e13f-104">This topic covers deployment and configuration guidance for features only currently available in Office 365 E5 and Advanced Compliance SKUs.</span></span>

<span data-ttu-id="6e13f-105">이 항목에서는 Office 365 조직에서 권한이 부여 된 액세스 관리를 사용 하도록 설정 하 고 구성 하는 과정을 안내 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e13f-105">This topic guides you through enabling and configuring privileged access management in your Office 365 organization.</span></span> <span data-ttu-id="6e13f-106">Microsoft 365 관리 센터 또는 Exchange 관리 PowerShell을 사용 하 여 권한 있는 액세스를 관리 하 고 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6e13f-106">You can use either the Microsoft 365 Admin Center or Exchange Management PowerShell to manage and use privileged access.</span></span> 

## <a name="enable-and-configure-privileged-access-management"></a><span data-ttu-id="6e13f-107">권한 있는 액세스 관리 사용 및 구성</span><span class="sxs-lookup"><span data-stu-id="6e13f-107">Enable and configure privileged access management</span></span>

<span data-ttu-id="6e13f-108">Office 365 조직에서 권한 있는 액세스를 설정 및 사용 하려면 다음 단계를 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e13f-108">Follow these steps to set up and use privileged access in your Office 365 organization:</span></span>

- [<span data-ttu-id="6e13f-109">1 단계: 승인자 그룹 만들기</span><span class="sxs-lookup"><span data-stu-id="6e13f-109">Step 1: Create an approver's group</span></span>](privileged-access-management-configuration.md#step1)

    <span data-ttu-id="6e13f-110">권한 액세스 사용을 시작 하기 전에 관리자 권한 및 권한 있는 작업에 대 한 들어오는 요청 액세스에 대 한 승인 권한이 필요한 사람을 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e13f-110">Before you start using privilege access, determine who needs approval authority for incoming requests for access to elevated and privileged tasks.</span></span> <span data-ttu-id="6e13f-111">승인자 그룹에 속하는 모든 사용자는 액세스 요청을 승인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6e13f-111">Any user who is part of the Approvers’ group is able to approve access requests.</span></span> <span data-ttu-id="6e13f-112">이 기능은 Office 365에서 메일 사용이 가능한 보안 그룹을 만들어 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6e13f-112">This is enabled by creating a mail-enabled security group in Office 365.</span></span>

- [<span data-ttu-id="6e13f-113">2 단계: 권한 있는 액세스 사용</span><span class="sxs-lookup"><span data-stu-id="6e13f-113">Step 2: Enable privileged access</span></span>](privileged-access-management-configuration.md#step2)

    <span data-ttu-id="6e13f-114">권한 있는 액세스 관리 액세스 제어에서 제외 하려는 시스템 계정 집합을 비롯 하 여 Office 365에서 기본 승인자 그룹을 사용 하 여 권한이 부여 된 access를 명시적으로 사용 하도록 설정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e13f-114">Privileged access must be explicitly enabled in Office 365 with the default approver group, including a set of system accounts that you want excluded from the privileged access management access control.</span></span>

- [<span data-ttu-id="6e13f-115">3 단계: 액세스 정책 만들기</span><span class="sxs-lookup"><span data-stu-id="6e13f-115">Step 3: Create an access policy</span></span>](privileged-access-management-configuration.md#step3)

    <span data-ttu-id="6e13f-116">승인 정책을 만들면 개별 작업에서 범위가 지정 되는 특정 승인 요구 사항을 정의할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6e13f-116">Creating an approval policy allows you to define the specific approval requirements scoped at individual tasks.</span></span> <span data-ttu-id="6e13f-117">승인 유형 옵션은 **자동** 또는 **수동**입니다.</span><span class="sxs-lookup"><span data-stu-id="6e13f-117">The approval type options are **Auto** or **Manual**.</span></span>

- [<span data-ttu-id="6e13f-118">4 단계: 권한 있는 액세스 요청 제출/승인</span><span class="sxs-lookup"><span data-stu-id="6e13f-118">Step 4: Submit/approve privileged access requests</span></span>](privileged-access-management-configuration.md#step4)

    <span data-ttu-id="6e13f-119">권한 있는 액세스를 사용 하도록 설정 하 고 나면 연결 된 승인 정책이 정의 된 모든 작업에 대 한 승인이 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e13f-119">Once enabled, privileged access requires approvals for any task that has an associated approval policy defined.</span></span> <span data-ttu-id="6e13f-120">승인 정책에 포함 된 작업의 경우 사용자는 작업을 실행 하는 데 필요한 권한을 요청 하 고 액세스 승인을 받아야 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e13f-120">For tasks included in an approval policy, users must request and be granted access approval to have permissions necessary to execute the task.</span></span>

<span data-ttu-id="6e13f-121">승인을 받은 후에는 요청 하는 사용자가 원하는 작업을 실행할 수 있으며, 권한이 부여 된 access에서는 사용자를 대신 하 여 작업을 승인 하 고 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e13f-121">After approval is granted, the requesting user can execute the intended task and privileged access will authorize and execute the task on behalf of the user.</span></span> <span data-ttu-id="6e13f-122">요청 된 기간 (기본 기간: 4 시간)에 대 한 승인은 유효한 상태로 유지 되므로 요청 자가 원하는 작업을 여러 번 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6e13f-122">The approval remains valid for the requested duration (default duration is 4 hours), during which the requester can execute the intended task multiple times.</span></span> <span data-ttu-id="6e13f-123">이러한 모든 실행이 기록 되 고 보안 및 준수 감사를 위해 사용할 수 있게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6e13f-123">All such executions are logged and made available for security and compliance auditing.</span></span> 

> [!NOTE]
> <span data-ttu-id="6e13f-124">Exchange 관리 PowerShell을 사용 하 여 권한 있는 액세스를 사용 하도록 설정 하 고 구성 하려면 [다단계 인증을 사용 하 여 Exchange Online powershell에 연결](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/mfa-connect-to-exchange-online-powershell?view=exchange-ps) 의 단계를 수행 하 여 Office 365와 함께 Exchange online powershell에 연결 합니다. 증명.</span><span class="sxs-lookup"><span data-stu-id="6e13f-124">If you want to use Exchange Management PowerShell to enable and configure privileged access, follow the steps in [Connect to Exchange Online PowerShell using Multi-Factor authentication](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/mfa-connect-to-exchange-online-powershell?view=exchange-ps) to connect to Exchange Online PowerShell with your Office 365 credentials.</span></span> <span data-ttu-id="6e13f-125">Office 365 조 직에 대해 Exchange Online PowerShell에 연결 하는 동안 권한 있는 액세스를 사용 하도록 설정 하는 단계를 사용 하기 위해 multi-factor authentication을 사용 하도록 설정할 필요는 없습니다.</span><span class="sxs-lookup"><span data-stu-id="6e13f-125">You do not need to enable multi-factor authentication for your Office 365 organization to use the steps to enable privileged access while connecting to Exchange Online PowerShell.</span></span> <span data-ttu-id="6e13f-126">다단계 인증을 사용 하 여 연결-요청에 서명 하기 위해 특권 수준의 액세스에서 사용 되는 OAuth 토큰을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6e13f-126">Connecting with multi-factor authentication creates an OAuth token that is used by privileged access for signing your requests.</span></span>

<span data-ttu-id="6e13f-127"><a name="step1"> </a></span><span class="sxs-lookup"><span data-stu-id="6e13f-127"></span></span>

## <a name="step-1-create-an-approvers-group"></a><span data-ttu-id="6e13f-128">1 단계: 승인자 그룹 만들기</span><span class="sxs-lookup"><span data-stu-id="6e13f-128">Step 1: Create an approver's group</span></span>

1. <span data-ttu-id="6e13f-129">조직의 관리자 계정에 대 한 자격 증명을 사용 하 여 [Microsoft 365 관리 센터](https://admin.microsoft.com) 에 로그인 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e13f-129">Sign into the [Microsoft 365 Admin Center](https://admin.microsoft.com) using credentials for an admin account in your organization.</span></span>

2. <span data-ttu-id="6e13f-130">관리 센터에서 그룹으로 이동 \*\*\*\* > 하 여**그룹을 추가**합니다.</span><span class="sxs-lookup"><span data-stu-id="6e13f-130">In the Admin Center, go to **Groups** > **Add a group**.</span></span>

3. <span data-ttu-id="6e13f-131">**메일 사용이 가능한 보안 그룹** 을 선택 하 고 새 그룹에 대 한 **이름**, **그룹 전자 메일 주소**및 **설명** 필드를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e13f-131">Select **mail-enabled security group** and then complete the **Name**, **Group email address**, and **Description** fields for the new group.</span></span>

4. <span data-ttu-id="6e13f-132">그룹을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e13f-132">Save the group.</span></span> <span data-ttu-id="6e13f-133">그룹을 완전히 구성 하 고 Microsoft 365 관리 센터에 표시 하는 데 몇 분 정도 걸릴 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6e13f-133">It may take a few minutes for the group to be fully configured and to appear in the Microsoft 365 admin center.</span></span>

5. <span data-ttu-id="6e13f-134">새 승인자의 그룹을 선택 하 고 **편집** 을 선택 하 여 그룹에 사용자를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e13f-134">Select the new approver's group and select **edit** to add users to the group.</span></span>

6. <span data-ttu-id="6e13f-135">그룹을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e13f-135">Save the group.</span></span>

<span data-ttu-id="6e13f-136"><a name="step2"> </a></span><span class="sxs-lookup"><span data-stu-id="6e13f-136"></span></span>

## <a name="step-2-enable-privileged-access"></a><span data-ttu-id="6e13f-137">2 단계: 권한 있는 액세스 사용</span><span class="sxs-lookup"><span data-stu-id="6e13f-137">Step 2: Enable privileged access</span></span>

### <a name="in-the-microsoft-365-admin-center"></a><span data-ttu-id="6e13f-138">Microsoft 365 관리 센터에서</span><span class="sxs-lookup"><span data-stu-id="6e13f-138">In the Microsoft 365 Admin Center</span></span>

1. <span data-ttu-id="6e13f-139">조직의 관리자 계정에 대 한 자격 증명을 사용 하 여 [Microsoft 365 관리 센터](https://admin.microsoft.com) 에 로그인 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e13f-139">Sign into the [Microsoft 365 Admin Center](https://admin.microsoft.com) using credentials for an admin account in your organization.</span></span>

2. <span data-ttu-id="6e13f-140">관리 센터에서 **Settings > Security & 개인 정보** > **권한 액세스**로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e13f-140">In the Admin Center, go to **Settings > Security & Privacy** > **Privileged access**.</span></span>

3. <span data-ttu-id="6e13f-141">권한 있는 **액세스 제어에 대 한 승인 필요** 를 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e13f-141">Enable the **Require approvals for privileged access** control.</span></span>

4. <span data-ttu-id="6e13f-142">1 단계에서 만든 승인자 그룹을 **기본 승인자 그룹**으로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e13f-142">Assign the approver's group you created in Step 1 as the **Default approvers group**.</span></span>

5. <span data-ttu-id="6e13f-143">**저장** 하 고 **닫습니다**.</span><span class="sxs-lookup"><span data-stu-id="6e13f-143">**Save** and **Close**.</span></span>

### <a name="in-exchange-management-powershell"></a><span data-ttu-id="6e13f-144">Exchange 관리 PowerShell에서</span><span class="sxs-lookup"><span data-stu-id="6e13f-144">In Exchange Management PowerShell</span></span>

<span data-ttu-id="6e13f-145">권한 있는 액세스를 사용 하도록 설정 하 고 승인자의 그룹을 할당 하려면 Exchange Online PowerShell에서 다음 명령을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e13f-145">To enable privileged access and to assign the approver's group, run the following command in Exchange Online PowerShell:</span></span>
```
Enable-ElevatedAccessControl -AdminGroup '<default approver group>' -SystemAccounts @('<systemAccountUPN1>','<systemAccountUPN2>')
```
<span data-ttu-id="6e13f-146">예제:</span><span class="sxs-lookup"><span data-stu-id="6e13f-146">Example:</span></span>
```
Enable-ElevatedAccessControl -AdminGroup 'pamapprovers@fabrikam.onmicrosoft.com' -SystemAccounts @('sys1@fabrikamorg.onmicrosoft.com', sys2@fabrikamorg.onmicrosoft.com')
```

> [!NOTE]
> <span data-ttu-id="6e13f-147">시스템 계정 기능을 사용 하 여 조직 내의 특정 자동화 기능이 권한 있는 액세스에 대 한 종속성 없이 작동할 수 있지만, 이러한 제외가 예외적인 경우에도 허용 되며 승인 되 고 감사 되도록 하는 것이 권장 됩니다. 자주.</span><span class="sxs-lookup"><span data-stu-id="6e13f-147">System accounts feature is made available to ensure certain automations within your organizations can work without dependency on privileged access, however it is recommended that such exclusions be exceptional and those allowed should be approved and audited regularly.</span></span>

<span data-ttu-id="6e13f-148"><a name="step3"> </a></span><span class="sxs-lookup"><span data-stu-id="6e13f-148"></span></span>

## <a name="step-3-create-an-access-policy"></a><span data-ttu-id="6e13f-149">3 단계: 액세스 정책 만들기</span><span class="sxs-lookup"><span data-stu-id="6e13f-149">Step 3: Create an access policy</span></span>

<span data-ttu-id="6e13f-150">Office 365 조 직에 대해 최대 30 개의 권한이 부여 된 액세스 정책을 만들고 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6e13f-150">You can create and configure up to 30 privileged access policies for your Office 365 organization.</span></span>

### <a name="in-the-microsoft-365-admin-center"></a><span data-ttu-id="6e13f-151">Microsoft 365 관리 센터에서</span><span class="sxs-lookup"><span data-stu-id="6e13f-151">In the Microsoft 365 Admin Center</span></span>

1. <span data-ttu-id="6e13f-152">조직의 관리자 계정에 대 한 자격 증명을 사용 하 여 [Microsoft 365 관리 센터](https://admin.microsoft.com) 에 로그인 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e13f-152">Sign into the [Microsoft 365 Admin Center](https://admin.microsoft.com) using credentials for an admin account in your organization.</span></span>

2. <span data-ttu-id="6e13f-153">관리 센터에서 **설정** > **보안 & 개인 정보** > **권한이 부여 된 액세스**로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e13f-153">In the Admin Center, go to **Settings** > **Security & Privacy** > **Privileged access**.</span></span>

3. <span data-ttu-id="6e13f-154">**액세스 정책 및 요청 관리를**선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e13f-154">Select **Manage access policies and requests**.</span></span>

4. <span data-ttu-id="6e13f-155">정책 **구성을** 선택 하 고 **정책 추가**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e13f-155">Select **Configure policies** and select **Add a policy**.</span></span>

5. <span data-ttu-id="6e13f-156">드롭다운 필드에서 조직에 적합 한 값을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e13f-156">From the drop-down fields, select the appropriate values for your organization:</span></span>
    
    <span data-ttu-id="6e13f-157">**정책 유형**: 작업, 역할 또는 역할 그룹</span><span class="sxs-lookup"><span data-stu-id="6e13f-157">**Policy type**: Task, Role, or Role Group</span></span>

    <span data-ttu-id="6e13f-158">**정책 범위**: Exchange</span><span class="sxs-lookup"><span data-stu-id="6e13f-158">**Policy scope**: Exchange</span></span>

    <span data-ttu-id="6e13f-159">**정책 이름**: 사용 가능한 정책에서 선택</span><span class="sxs-lookup"><span data-stu-id="6e13f-159">**Policy name**: Select from the available policies</span></span>

    <span data-ttu-id="6e13f-160">**승인 유형**: 수동 또는 자동</span><span class="sxs-lookup"><span data-stu-id="6e13f-160">**Approval type**: Manual or Auto</span></span>

    <span data-ttu-id="6e13f-161">**승인 그룹**: 1 단계에서 만든 승인자 그룹을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e13f-161">**Approval group**: Select the approvers group created in Step 1</span></span>

6. <span data-ttu-id="6e13f-162">**만들기** 를 선택한 다음 **닫기를**선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e13f-162">Select **Create** and then **Close**.</span></span> <span data-ttu-id="6e13f-163">정책을 완전히 구성 및 사용 하도록 설정 하는 데 몇 분 정도 걸릴 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6e13f-163">It may take a few minutes for the policy to be fully configured and enabled.</span></span>

### <a name="in-exchange-management-powershell"></a><span data-ttu-id="6e13f-164">Exchange 관리 PowerShell에서</span><span class="sxs-lookup"><span data-stu-id="6e13f-164">In Exchange Management PowerShell</span></span>

<span data-ttu-id="6e13f-165">승인 정책을 만들고 정의 하려면 Exchange Online PowerShell에서 다음 명령을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e13f-165">To create and define an approval policy, run the following command in Exchange Online PowerShell:</span></span>

```
New-ElevatedAccessApprovalPolicy -Task 'Exchange\<exchange management cmdlet name>' -ApprovalType <Manual, Auto> -ApproverGroup '<default/custom approver group>'
```
<span data-ttu-id="6e13f-166">예제:</span><span class="sxs-lookup"><span data-stu-id="6e13f-166">Example:</span></span>
```
New-ElevatedAccessApprovalPolicy -Task 'Exchange\New-MoveRequest' -ApprovalType Manual -ApproverGroup 'mbmanagers@fabrikamorg.onmicrosoft.com'
```

<span data-ttu-id="6e13f-167"><a name="step4"> </a></span><span class="sxs-lookup"><span data-stu-id="6e13f-167"></span></span>

## <a name="step-4-submitapprove-privileged-access-requests"></a><span data-ttu-id="6e13f-168">4 단계: 권한 있는 액세스 요청 제출/승인</span><span class="sxs-lookup"><span data-stu-id="6e13f-168">Step 4: Submit/approve privileged access requests</span></span>

### <a name="requesting-elevation-authorization-to-execute-privileged-tasks"></a><span data-ttu-id="6e13f-169">권한 있는 작업 실행을 위한 권한 상승 요청</span><span class="sxs-lookup"><span data-stu-id="6e13f-169">Requesting elevation authorization to execute privileged tasks</span></span>

<span data-ttu-id="6e13f-170">권한 있는 액세스에 대 한 요청은 요청이 제출 된 후 최대 24 시간 동안 유효 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e13f-170">Requests for privileged access are valid for up to 24 hours after the request is submitted.</span></span> <span data-ttu-id="6e13f-171">승인 되거나 거부 되지 않으면 요청이 만료 되 고 액세스가 승인 되지 않은 것입니다.</span><span class="sxs-lookup"><span data-stu-id="6e13f-171">If not approved or denied, the requests expire and access is not approved.</span></span>

#### <a name="in-the-microsoft-365-admin-center"></a><span data-ttu-id="6e13f-172">Microsoft 365 관리 센터에서</span><span class="sxs-lookup"><span data-stu-id="6e13f-172">In the Microsoft 365 Admin Center</span></span>

1. <span data-ttu-id="6e13f-173">자격 증명을 사용 하 여 [Microsoft 365 관리 센터](https://admin.microsoft.com) 에 로그인 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e13f-173">Sign into the [Microsoft 365 Admin Center](https://admin.microsoft.com) using your credentials.</span></span>

2. <span data-ttu-id="6e13f-174">관리 센터에서 **설정** > **보안 & 개인 정보** > **권한이 부여 된 액세스**로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e13f-174">In the Admin Center, go to **Settings** > **Security & Privacy** > **Privileged access**.</span></span>

3. <span data-ttu-id="6e13f-175">**액세스 정책 및 요청 관리를**선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e13f-175">Select **Manage access policies and requests**.</span></span>

4. <span data-ttu-id="6e13f-176">**새 요청**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e13f-176">Select **New request**.</span></span> <span data-ttu-id="6e13f-177">드롭다운 필드에서 조직에 적합 한 값을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e13f-177">From the drop-down fields, select the appropriate values for your organization:</span></span>

    <span data-ttu-id="6e13f-178">**요청 유형**: 작업, 역할 또는 역할 그룹</span><span class="sxs-lookup"><span data-stu-id="6e13f-178">**Request type**: Task, Role, or Role Group</span></span>

    <span data-ttu-id="6e13f-179">**요청 범위**: Exchange</span><span class="sxs-lookup"><span data-stu-id="6e13f-179">**Request scope**: Exchange</span></span>

    <span data-ttu-id="6e13f-180">**요청**: 사용 가능한 정책에서 선택</span><span class="sxs-lookup"><span data-stu-id="6e13f-180">**Request for**: Select from the available policies</span></span>

    <span data-ttu-id="6e13f-181">**기간 (시간)**: 요청 된 액세스에 대 한 시간 수입니다.</span><span class="sxs-lookup"><span data-stu-id="6e13f-181">**Duration (hours)**: Number of hours of requested access.</span></span> <span data-ttu-id="6e13f-182">요청할 수 있는 시간에 제한이 없습니다.</span><span class="sxs-lookup"><span data-stu-id="6e13f-182">There isn't a limit on the number of hours that can be requested.</span></span>

    <span data-ttu-id="6e13f-183">**설명**: 액세스 요청과 관련 된 설명에 대 한 텍스트 필드입니다.</span><span class="sxs-lookup"><span data-stu-id="6e13f-183">**Comments**: Text field for comments related to your access request</span></span>

5. <span data-ttu-id="6e13f-184">**저장** 을 선택한 다음 **닫기를**선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e13f-184">Select **Save** and then **Close**.</span></span> <span data-ttu-id="6e13f-185">요청은 전자 메일을 통해 승인자 그룹에 전송 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6e13f-185">Your request will be sent to the approver's group via email.</span></span>

#### <a name="in-exchange-management-powershell"></a><span data-ttu-id="6e13f-186">Exchange 관리 PowerShell에서</span><span class="sxs-lookup"><span data-stu-id="6e13f-186">In Exchange Management PowerShell</span></span>

<span data-ttu-id="6e13f-187">Exchange Online PowerShell에서 다음 명령을 실행 하 여 승인자 그룹에 대 한 승인 요청을 만들고 제출 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e13f-187">Run the following command in Exchange Online PowerShell to create and submit an approval request to the approver's group:</span></span>
```
New-ElevatedAccessRequest -Task 'Exchange\<exchange management cmdlet name>' -Reason '<appropriate reason>' -DurationHours <duration in hours>
```
<span data-ttu-id="6e13f-188">예제:</span><span class="sxs-lookup"><span data-stu-id="6e13f-188">Example:</span></span>
```
New-ElevatedAccessRequest -Task 'Exchange\New-MoveRequest' -Reason 'Attempting to fix the user mailbox error' -DurationHours 4
```
### <a name="view-status-of-elevation-requests"></a><span data-ttu-id="6e13f-189">권한 상승 요청의 상태 보기</span><span class="sxs-lookup"><span data-stu-id="6e13f-189">View status of elevation requests</span></span>
<span data-ttu-id="6e13f-190">승인 요청을 만든 후에는 요청 ID와 연결 된을 사용 하 여 관리 센터 또는 Exchange 관리 PowerShell에서 권한 상승 요청 상태를 검토할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6e13f-190">After an approval request is created, elevation request status can be reviewed in the admin center or in Exchange Management PowerShell using the associated with request ID.</span></span>

#### <a name="in-the-microsoft-365-admin-center"></a><span data-ttu-id="6e13f-191">Microsoft 365 관리 센터에서</span><span class="sxs-lookup"><span data-stu-id="6e13f-191">In the Microsoft 365 admin center</span></span>

1. <span data-ttu-id="6e13f-192">자격 증명을 사용 하 여 [Microsoft 365 관리 센터](https://admin.microsoft.com) 에 로그인 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e13f-192">Sign into the [Microsoft 365 admin center](https://admin.microsoft.com) with your credentials.</span></span>

2. <span data-ttu-id="6e13f-193">관리 센터에서 **설정** > **보안 & 개인 정보** > **권한이 부여 된 액세스**로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e13f-193">In the admin center, go to **Settings** > **Security & Privacy** > **Privileged access**.</span></span>

3. <span data-ttu-id="6e13f-194">**액세스 정책 및 요청 관리를**선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e13f-194">Select **Manage access policies and requests**.</span></span>

4. <span data-ttu-id="6e13f-195">**보기** 를 선택 하 여 **대기**, **승인**, **거부**또는 **사용자 Lockbox** 상태를 기준으로 제출 된 요청을 필터링 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e13f-195">Select **View** to filter submitted requests by **Pending**, **Approved**, **Denied**, or **Customer Lockbox** status.</span></span>

#### <a name="in-exchange-management-powershell"></a><span data-ttu-id="6e13f-196">Exchange 관리 PowerShell에서</span><span class="sxs-lookup"><span data-stu-id="6e13f-196">In Exchange Management PowerShell</span></span>

<span data-ttu-id="6e13f-197">Exchange Online PowerShell에서 다음 명령을 실행 하 여 특정 요청 ID에 대 한 승인 요청 상태를 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e13f-197">Run the following command in Exchange Online PowerShell to view an approval request status for a specific request ID:</span></span>
```
Get-ElevatedAccessRequest -Identity <request ID> | select RequestStatus
```
<span data-ttu-id="6e13f-198">예제:</span><span class="sxs-lookup"><span data-stu-id="6e13f-198">Example:</span></span>
```
Get-ElevatedAccessRequest -Identity 28560ed0-419d-4cc3-8f5b-603911cbd450 | select RequestStatus
```

### <a name="approving-an-elevation-authorization-request"></a><span data-ttu-id="6e13f-199">권한 상승 인증 요청 승인</span><span class="sxs-lookup"><span data-stu-id="6e13f-199">Approving an elevation authorization request</span></span>
<span data-ttu-id="6e13f-200">승인 요청이 작성 되 면 관련 승인자 그룹의 구성원은 전자 메일 알림을 수신 하 고 요청 ID와 연결 된 요청을 승인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6e13f-200">When an approval request is created, members of the relevant approver group receive an email notification and can approve the request associated with the request ID.</span></span> <span data-ttu-id="6e13f-201">요청자에 게는 전자 메일 메시지를 통한 승인 또는 거부 요청이 통지 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6e13f-201">The requestor is notified of the request approval or denial via email message.</span></span>

#### <a name="in-the-microsoft-365-admin-center"></a><span data-ttu-id="6e13f-202">Microsoft 365 관리 센터에서</span><span class="sxs-lookup"><span data-stu-id="6e13f-202">In the Microsoft 365 admin center</span></span>

1. <span data-ttu-id="6e13f-203">자격 증명을 사용 하 여 [Microsoft 365 관리 센터](https://admin.microsoft.com) 에 로그인 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e13f-203">Sign into the [Microsoft 365 admin center](https://admin.microsoft.com) with your credentials.</span></span>

2. <span data-ttu-id="6e13f-204">관리 센터에서 **설정** > **보안 & 개인 정보** > **권한이 부여 된 액세스**로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e13f-204">In the admin center, go to **Settings** > **Security & Privacy** > **Privileged access**.</span></span>

3. <span data-ttu-id="6e13f-205">**액세스 정책 및 요청 관리를**선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e13f-205">Select **Manage access policies and requests**.</span></span>

4. <span data-ttu-id="6e13f-206">나열 된 요청을 선택 하 여 세부 정보를 보고 요청에 대해 작업을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e13f-206">Select a listed request to view the details and to take action on the request.</span></span>

5. <span data-ttu-id="6e13f-207">요청을 승인 하려면 **승인을** 선택 하 고 요청을 거부 하려면 **거부** 를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e13f-207">Select **Approve** to approve the request or select **Deny** to deny the request.</span></span> <span data-ttu-id="6e13f-208">이전에 승인 된 요청은 **취소**를 선택 하 여 액세스를 취소할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6e13f-208">Previously approved requests can have access revoked by selecting **Revoke**.</span></span>

#### <a name="in-exchange-management-powershell"></a><span data-ttu-id="6e13f-209">Exchange 관리 PowerShell에서</span><span class="sxs-lookup"><span data-stu-id="6e13f-209">In Exchange Management PowerShell</span></span>

<span data-ttu-id="6e13f-210">권한 상승 요청을 승인 하려면 Exchange Online PowerShell에서 다음 명령을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e13f-210">To approve an elevation authorization request, run the following command in Exchange Online PowerShell:</span></span>

```
Approve-ElevatedAccessRequest -RequestId <request id> -Comment '<approval comment>'
```
<span data-ttu-id="6e13f-211">예제:</span><span class="sxs-lookup"><span data-stu-id="6e13f-211">Example:</span></span>
```
Approve-ElevatedAccessRequest -RequestId a4bc1bdf-00a1-42b4-be65-b6c63d6be279 -Comment '<approval comment>'
```

<span data-ttu-id="6e13f-212">권한 상승 요청을 거부 하려면 Exchange Online PowerShell에서 다음 명령을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e13f-212">To deny an elevation authorization request, run the following command in Exchange Online PowerShell:</span></span>

```
Deny-ElevatedAccessRequest -RequestId <request id> -Comment '<denial comment>'
```
<span data-ttu-id="6e13f-213">예제:</span><span class="sxs-lookup"><span data-stu-id="6e13f-213">Example:</span></span>
```
Deny-ElevatedAccessRequest -RequestId a4bc1bdf-00a1-42b4-be65-b6c63d6be279 -Comment '<denial comment>'
```

## <a name="delete-a-privileged-access-policy-in-office-365"></a><span data-ttu-id="6e13f-214">Office 365에서 권한이 부여 된 액세스 정책 삭제</span><span class="sxs-lookup"><span data-stu-id="6e13f-214">Delete a privileged access policy in Office 365</span></span>
<span data-ttu-id="6e13f-215">조직에서 더 이상 필요 하지 않은 액세스 정책을 삭제할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6e13f-215">If it is no longer needed in your organization, you can delete a privileged access policy.</span></span>

### <a name="in-the-microsoft-365-admin-center"></a><span data-ttu-id="6e13f-216">Microsoft 365 관리 센터에서</span><span class="sxs-lookup"><span data-stu-id="6e13f-216">In the Microsoft 365 admin center</span></span>

1. <span data-ttu-id="6e13f-217">조직의 관리자 계정에 대 한 자격 증명을 사용 하 여 [Microsoft 365 관리 센터](https://admin.microsoft.com) 에 로그인 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e13f-217">Sign into the [Microsoft 365 admin center](https://admin.microsoft.com) using credentials for an admin account in your organization.</span></span>

2. <span data-ttu-id="6e13f-218">관리 센터에서 **설정** > **보안 & 개인 정보** > **권한이 부여 된 액세스**로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e13f-218">In the admin center, go to **Settings** > **Security & Privacy** > **Privileged access**.</span></span>

3. <span data-ttu-id="6e13f-219">**액세스 정책 및 요청 관리를**선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e13f-219">Select **Manage access policies and requests**.</span></span>

4. <span data-ttu-id="6e13f-220">**정책 구성을**선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e13f-220">Select **Configure policies**.</span></span>

5. <span data-ttu-id="6e13f-221">삭제할 정책을 선택 하 고 **정책 제거**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e13f-221">Select the policy you want to delete, then select **Remove Policy**.</span></span>

6. <span data-ttu-id="6e13f-222">**닫기를**선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e13f-222">Select **Close**.</span></span>

### <a name="in-exchange-management-powershell"></a><span data-ttu-id="6e13f-223">Exchange 관리 PowerShell에서</span><span class="sxs-lookup"><span data-stu-id="6e13f-223">In Exchange Management PowerShell</span></span>

<span data-ttu-id="6e13f-224">권한이 부여 된 액세스 정책을 삭제 하려면 Exchange Online Powershell에서 다음 명령을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e13f-224">To delete a privileged access policy, run the following command in Exchange Online Powershell:</span></span>

```
Remove-ElevatedAccessApprovalPolicy -Identity <identity GUID of the policy you want to delete>
```

## <a name="disable-privileged-access-in-office-365"></a><span data-ttu-id="6e13f-225">Office 365에서 권한이 부여 된 액세스를 사용 하지 않도록 설정</span><span class="sxs-lookup"><span data-stu-id="6e13f-225">Disable privileged access in Office 365</span></span>

<span data-ttu-id="6e13f-226">필요한 경우 조직에 대해 권한이 부여 된 액세스 관리를 사용 하지 않도록 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6e13f-226">If needed, you can disable privileged access management for your organization.</span></span> <span data-ttu-id="6e13f-227">권한 있는 액세스를 사용 하지 않도록 설정 해도 연결 된 승인 정책이 나 승인자 그룹은 삭제 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6e13f-227">Disabling privileged access does not delete any associated approval policies or approver groups.</span></span>

### <a name="in-the-microsoft-365-admin-center"></a><span data-ttu-id="6e13f-228">Microsoft 365 관리 센터에서</span><span class="sxs-lookup"><span data-stu-id="6e13f-228">In the Microsoft 365 admin center</span></span>

1. <span data-ttu-id="6e13f-229">조직의 관리자 계정에 대 한 자격 증명을 사용 하 여 [Microsoft 365 관리 센터](https://admin.microsoft.com) 에 로그인 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e13f-229">Sign into the [Microsoft 365 admin center](https://admin.microsoft.com) with credentials for an admin account in your organization.</span></span>

2. <span data-ttu-id="6e13f-230">관리 센터에서 **설정** > **보안 & 개인 정보** > **권한이 부여 된 액세스**로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e13f-230">In the Admin Center, go to **Settings** > **Security & Privacy** > **Privileged access**.</span></span>

3. <span data-ttu-id="6e13f-231">권한 있는 **액세스 제어에 대 한 승인 필요** 를 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e13f-231">Enable the **Require approvals for privileged access** control.</span></span>

### <a name="in-exchange-management-powershell"></a><span data-ttu-id="6e13f-232">Exchange 관리 PowerShell에서</span><span class="sxs-lookup"><span data-stu-id="6e13f-232">In Exchange Management PowerShell</span></span>

<span data-ttu-id="6e13f-233">권한 있는 액세스를 사용 하지 않도록 설정 하려면 Exchange Online Powershell에서 다음 명령을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e13f-233">To disable privileged access, run the following command in Exchange Online Powershell:</span></span>

```
Disable-ElevatedAccessControl
```