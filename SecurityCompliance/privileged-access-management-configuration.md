---
title: Office 365에서 액세스 권한을된 관리 구성
ms.author: robmazz
author: robmazz
manager: laurawi
ms.audience: ITPro
ms.topic: overview
ms.service: o365-solutions
localization_priority: Normal
search.appverid:
- MET150
ms.collection: Strat_O365_IP
ms.custom: Ent_Solutions
ms.assetid: ''
description: Office 365에서 권한이 부여 된 액세스 관리를 구성 하는 방법에 대 한 자세한 내용은이 항목을 사용 하 여
ms.openlocfilehash: 47cae93a41b0fd60645021f6f299645777a9a2e1
ms.sourcegitcommit: c168410974bc90aaf55f1dcaa9e05c09b2b78d76
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/25/2018
ms.locfileid: "25011844"
---
# <a name="configuring-privileged-access-management-in-office-365"></a><span data-ttu-id="35ad2-103">Office 365에서 액세스 권한을된 관리 구성</span><span class="sxs-lookup"><span data-stu-id="35ad2-103">Configuring privileged access management in Office 365</span></span>

> [!IMPORTANT]
> <span data-ttu-id="35ad2-104">이 항목에서는 Office 365 e 5 및 고급 준수 Sku에만 현재 제공 되는 기능에 대 한 배포 및 구성 지침에 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="35ad2-104">This topic covers deployment and configuration guidance for features only currently available in Office 365 E5 and Advanced Compliance SKUs.</span></span>

<span data-ttu-id="35ad2-p101">이 항목은 통해 사용 하도록 설정 하 고 Office 365 조직에서 권한이 부여 된 액세스 관리를 구성 하는 것을 안내 합니다. 하나를 사용할 수는 Microsoft 365 관리 센터 또는 Exchange 관리 PowerShell 관리를 사용 하는 액세스 권한이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="35ad2-p101">This topic will guide you through enabling and configuring privileged access management in your Office 365 organization. You can use either the the Microsoft 365 Admin Center or Exchange Management PowerShell to manage and use privileged access.</span></span> 

## <a name="enable-and-configure-privileged-access-management"></a><span data-ttu-id="35ad2-107">설정 하 고 액세스 권한을된 관리 구성</span><span class="sxs-lookup"><span data-stu-id="35ad2-107">Enable and configure privileged access management</span></span>

<span data-ttu-id="35ad2-108">설정 하 고 Office 365 조직에서 액세스 권한을된 사용 하려면 다음이 단계를 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="35ad2-108">Follow these steps to set up and use privileged access in your Office 365 organization:</span></span>

- [<span data-ttu-id="35ad2-109">1 단계: 승인자의 그룹 만들기</span><span class="sxs-lookup"><span data-stu-id="35ad2-109">Step 1: Create an approver's group</span></span>](privileged-access-management-configuration.md#step1)

    <span data-ttu-id="35ad2-p102">권한 액세스를 사용 하 여를 시작 하기 전에 관리자 권한 및 권한 있는 작업에 대 한 액세스에 대 한 수신 요청에 대 한 승인 권한을 갖고 결정 합니다. 승인자 그룹의 구성원 인 모든 사용자 액세스 요청 승인 됩니다. Office 365의 메일 사용이 가능한 보안 그룹을 만들어 사용 하도록 설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="35ad2-p102">Before you start using privilege access, determine who will have approval authority for incoming requests for access to elevated and privileged tasks. Any user who is part of the Approvers’ group will be able to approve access requests. This is enabled by creating a mail-enabled security group in Office 365.</span></span>

- [<span data-ttu-id="35ad2-113">2 단계: 사용 권한이 부여 된 액세스</span><span class="sxs-lookup"><span data-stu-id="35ad2-113">Step 2: Enable privileged access</span></span>](privileged-access-management-configuration.md#step2)

    <span data-ttu-id="35ad2-114">액세스 권한을된 명시적으로 켜져 있어야 Office 365의 기본 승인자 그룹 및 액세스 권한을된 관리 액세스 제어에서 제외 하려는 시스템 계정 집합을 포함 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="35ad2-114">Privileged access needs to be explicitly turned on in Office 365 with the default approver group and including a set of system accounts that you’d want to be excluded from the privileged access management access control.</span></span>

- [<span data-ttu-id="35ad2-115">3 단계: 액세스 정책 만들기</span><span class="sxs-lookup"><span data-stu-id="35ad2-115">Step 3: Create an access policy</span></span>](privileged-access-management-configuration.md#step3)

    <span data-ttu-id="35ad2-p103">승인 정책 만들기 (영문)를 사용 하면 개별 작업에서 범위가 지정 된 특정 승인 요구 사항을 정의할 수 있습니다. 승인 유형 옵션은 **자동** 또는 **수동**입니다.</span><span class="sxs-lookup"><span data-stu-id="35ad2-p103">Creating an approval policy allows you to define the specific approval requirements scoped at individual tasks. The approval type options are **Auto** or **Manual**.</span></span>

- [<span data-ttu-id="35ad2-118">4 단계: 전송/요청을 승인 권한이 부여 된 액세스</span><span class="sxs-lookup"><span data-stu-id="35ad2-118">Step 4: Submit/approve privileged access requests</span></span>](privileged-access-management-configuration.md#step4)

    <span data-ttu-id="35ad2-p104">한번 사용 하도록 설정, 권한이 부여 된 액세스는 연결 된 승인 정책 정의 된 모든 작업을 실행 하는 것에 대 한 승인 필요 합니다. 필요에 포함 된 작업을 실행 하는 사용자는 승인 정책을 요청 해야 하 고 작업을 실행 하는 데 필요한 사용 권한이 하기 위해 액세스 승인에 게 부여 합니다.</span><span class="sxs-lookup"><span data-stu-id="35ad2-p104">Once enabled, privileged access requires approvals for executing any task that has an associated approval policy defined. Users needing to execute tasks included in the an approval policy must request and be granted access approval in order to have permissions necessary to execute the task.</span></span>

<span data-ttu-id="35ad2-p105">승인 권한이 부여 되 면 요청 하는 사용자 의도 한 작업을 실행할 수 있고 권한이 부여 된 액세스 권한을 부여 하 고 사용자를 대신 하 여 작업을 실행 됩니다. 승인의 요청에 대해 유효 기간 (기본 기간은 4 시간)을 하는 동안 요청자 수 의도 한 작업을 여러 번 실행 합니다. 이러한 모든 실행 기록 하 고 보안 및 규정 준수 감사를 위해 사용할 수 있게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="35ad2-p105">After approval is granted, the requesting user can execute the intended task and privileged access will authorize and execute the task on users’ behalf. The approval remains valid for the requested duration (default duration is 4 hours), during which the requester can execute the intended task multiple times. All such executions are logged and made available for security and compliance auditing.</span></span> 

> [!NOTE]
> <span data-ttu-id="35ad2-p106">Exchange Online PowerShell Office 365에 연결할 [다단계 인증을 사용 하 여 Exchange Online powershell 연결](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/mfa-connect-to-exchange-online-powershell?view=exchange-ps) 의 단계에 따라 사용 하도록 설정 하 고 액세스 권한을된 구성 하려면 Exchange 관리 PowerShell을 사용 하려는 경우 자격 증명입니다. Exchange Online PowerShell에 연결 하는 동안 액세스 권한을된 사용 하도록 설정 하는 단계를 사용 하 여 Office 365 조직에 대해 다단계 인증을 사용할 필요가 없습니다. 다단계 인증을 통해 연결 요청에 서명 하는 것에 대 한 권한이 부여 된 액세스에 사용 되는 OAuth 토큰을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="35ad2-p106">If you want to use Exchange Management PowerShell to enable and configure privileged access, follow the steps in [Connect to Exchange Online PowerShell using Multi-Factor authentication](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/mfa-connect-to-exchange-online-powershell?view=exchange-ps) to connect to Exchange Online PowerShell with your Office 365 credentials. You do not need to enable multi-factor authentication for your Office 365 organization to use the steps to enable privileged access while connecting to Exchange Online PowerShell. Connecting with multi-factor authentication creates an OAuth token that is used by privileged access for signing your requests.</span></span>

<span data-ttu-id="35ad2-127"><a name="step1"> </a></span><span class="sxs-lookup"><span data-stu-id="35ad2-127"></span></span>

## <a name="step-1---create-an-approvers-group"></a><span data-ttu-id="35ad2-128">1 단계-승인자의 그룹 만들기</span><span class="sxs-lookup"><span data-stu-id="35ad2-128">Step 1 - Create an approver's group</span></span>

1. <span data-ttu-id="35ad2-129">조직에서 관리 계정에 대 한 자격 증명을 사용 하 여 [Microsoft 365 관리 센터](https://portal.office.com) 에 로그인 합니다.</span><span class="sxs-lookup"><span data-stu-id="35ad2-129">Sign into the [Microsoft 365 Admin Center](https://portal.office.com) using credentials for an admin account in your organization.</span></span>

2. <span data-ttu-id="35ad2-130">관리 센터에서 **그룹**으로 이동 > **그룹을 추가**합니다.</span><span class="sxs-lookup"><span data-stu-id="35ad2-130">In the Admin Center, go to **Groups** > **Add a group**.</span></span>

3. <span data-ttu-id="35ad2-131">**메일 사용이 가능한 보안 그룹** 그룹 종류를 선택 하 고 새 그룹에 대 한 **이름**, **그룹 전자 메일 주소**및 **설명** 필드에 입력 한 다음 키를 누릅니다.</span><span class="sxs-lookup"><span data-stu-id="35ad2-131">Select the **mail-enabled security group** group type and then complete the **Name**, **Group email address**, and **Description** fields for the new group.</span></span>

4. <span data-ttu-id="35ad2-p107">그룹을 저장 합니다. 완전 하 게 구성 하 고 Office 365 관리 센터에 표시 되는 그룹에 대 한 몇 분정도 걸릴 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="35ad2-p107">Save the group. It may take a few minutes for the group to be fully configured and to appear in the Office 365 Admin Center.</span></span>

5. <span data-ttu-id="35ad2-134">새 승인자의 그룹을 선택 하 고 그룹에 사용자를 추가 하려면 **편집** 을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="35ad2-134">Select the new approver's group and select **edit** to add users to the group.</span></span>

6. <span data-ttu-id="35ad2-135">그룹을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="35ad2-135">Save the group.</span></span>

<span data-ttu-id="35ad2-136"><a name="step2"> </a></span><span class="sxs-lookup"><span data-stu-id="35ad2-136"></span></span>

## <a name="step-2---enable-privileged-access"></a><span data-ttu-id="35ad2-137">2 단계-권한이 부여 된 액세스 사용</span><span class="sxs-lookup"><span data-stu-id="35ad2-137">Step 2 - Enable privileged access</span></span>

### <a name="using-the-microsoft-365-admin-center"></a><span data-ttu-id="35ad2-138">Microsoft 365 관리 센터를 사용 하 여</span><span class="sxs-lookup"><span data-stu-id="35ad2-138">Using the Microsoft 365 Admin Center</span></span>

1. <span data-ttu-id="35ad2-139">조직에서 관리 계정에 대 한 자격 증명을 사용 하 여 [Microsoft 365 관리 센터](https://portal.office.com) 에 로그인 합니다.</span><span class="sxs-lookup"><span data-stu-id="35ad2-139">Sign into the [Microsoft 365 Admin Center](https://portal.office.com) using credentials for an admin account in your organization.</span></span>

2. <span data-ttu-id="35ad2-140">관리 센터에서로 이동 **설정 > 보안 및 개인정보** > **권한이 부여 된 액세스**합니다.</span><span class="sxs-lookup"><span data-stu-id="35ad2-140">In the Admin Center, go to **Settings > Security & Privacy** > **Privileged access**.</span></span>

3. <span data-ttu-id="35ad2-141">**권한이 부여 된 액세스에 대 한 승인 필요** 제어를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="35ad2-141">Enable the **Require approvals for privileged access** control.</span></span>

4. <span data-ttu-id="35ad2-142">**승인자 그룹을 기본**으로 1 단계에서에서 만든 승인자의 그룹을 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="35ad2-142">Assign the approver's group you created in Step 1 as the **Default approvers group**.</span></span>

5. <span data-ttu-id="35ad2-143">**저장** 하 고 **닫기**.</span><span class="sxs-lookup"><span data-stu-id="35ad2-143">**Save** and **Close**.</span></span>

### <a name="using-exchange-management-powershell"></a><span data-ttu-id="35ad2-144">Exchange 관리 PowerShell을 사용 하 여</span><span class="sxs-lookup"><span data-stu-id="35ad2-144">Using Exchange Management PowerShell</span></span>

<span data-ttu-id="35ad2-145">액세스 권한을된 사용 하도록 설정 하 고 승인자의 그룹을 할당 하려면 Exchange Online PowerShell에서 다음 명령을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="35ad2-145">Run the following command in Exchange Online PowerShell to enable privileged access and to assign the approver's group:</span></span>
```
Enable-ElevatedAccessControl -AdminGroup '<default approver group>' -SystemAccounts @('<systemAccountUPN1>','<systemAccountUPN2>')
```
<span data-ttu-id="35ad2-146">예제:</span><span class="sxs-lookup"><span data-stu-id="35ad2-146">Example:</span></span>
```
Enable-ElevatedAccessControl -AdminGroup 'pamapprovers@fabrikam.onmicrosoft.com' -SystemAccounts @('sys1@fabrikamorg.onmicrosoft.com', sys2@fabrikamorg.onmicrosoft.com')
```

> [!NOTE]
> <span data-ttu-id="35ad2-147">그러나 기능 사용 가능 조직 내에서 특정 자동화가 되도록 시스템 계정 액세스 권한을된 의존 관계 없이 사용할 수 있는, 것이 좋습니다 이러한 제외 뛰어난 수 및 승인 고 감사를 수행 해야 허용 된 정기적으로 합니다.</span><span class="sxs-lookup"><span data-stu-id="35ad2-147">System accounts feature is made available to ensure certain automations within your organizations can work without dependency on privileged access, however it is recommended that such exclusions be exceptional and those allowed should be approved and audited regularly.</span></span>

<span data-ttu-id="35ad2-148"><a name="step3"> </a></span><span class="sxs-lookup"><span data-stu-id="35ad2-148"></span></span>

## <a name="step-3---create-an-access-policy"></a><span data-ttu-id="35ad2-149">3 단계-액세스 정책 만들기</span><span class="sxs-lookup"><span data-stu-id="35ad2-149">Step 3 - Create an access policy</span></span>

<span data-ttu-id="35ad2-150">만들 수 있으며 Office 365 조직에 대 한 최대 30 개의 권한이 부여 된 액세스 정책 구성.</span><span class="sxs-lookup"><span data-stu-id="35ad2-150">You can create and configure up to 30 privileged access policies for your Office 365 organization.</span></span>

### <a name="using-the-microsoft-365-admin-center"></a><span data-ttu-id="35ad2-151">Microsoft 365 관리 센터를 사용 하 여</span><span class="sxs-lookup"><span data-stu-id="35ad2-151">Using the Microsoft 365 Admin Center</span></span>

1. <span data-ttu-id="35ad2-152">조직에서 관리 계정에 대 한 자격 증명을 사용 하 여 [Microsoft 365 관리 센터](https://portal.office.com) 에 로그인 합니다.</span><span class="sxs-lookup"><span data-stu-id="35ad2-152">Sign into the [Microsoft 365 Admin Center](https://portal.office.com) using credentials for an admin account in your organization.</span></span>

2. <span data-ttu-id="35ad2-153">관리 센터에서 **설정**으로 이동 > **보안 및 개인정보** > **권한이 부여 된 액세스**합니다.</span><span class="sxs-lookup"><span data-stu-id="35ad2-153">In the Admin Center, go to **Settings** > **Security & Privacy** > **Privileged access**.</span></span>

3. <span data-ttu-id="35ad2-154">**관리 액세스 정책 및 요청을**선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="35ad2-154">Select **Manage access policies and requests**.</span></span>

4. <span data-ttu-id="35ad2-155">**정책을 구성을** 선택 하 고 **정책 추가**선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="35ad2-155">Select **Configure policies** and select **Add a policy**.</span></span>

5. <span data-ttu-id="35ad2-156">드롭다운 필드에서 조직에 대 한 적절 한 값을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="35ad2-156">From the drop-down fields, select the appropriate values for your organization:</span></span>
    
    <span data-ttu-id="35ad2-157">**정책 유형**: 작업, 역할 또는 역할 그룹</span><span class="sxs-lookup"><span data-stu-id="35ad2-157">**Policy type**: Task, Role, or Role Group</span></span>

    <span data-ttu-id="35ad2-158">**정책 범위**: Exchange 또는 Office 365</span><span class="sxs-lookup"><span data-stu-id="35ad2-158">**Policy scope**: Exchange or Office 365</span></span>

    <span data-ttu-id="35ad2-159">**정책 이름**: 사용 가능한 정책에서 선택</span><span class="sxs-lookup"><span data-stu-id="35ad2-159">**Policy name**: Select from the available policies</span></span>

    <span data-ttu-id="35ad2-160">**승인 유형**: 수동 또는 자동</span><span class="sxs-lookup"><span data-stu-id="35ad2-160">**Approval type**: Manual or Auto</span></span>

    <span data-ttu-id="35ad2-161">**승인 그룹**: 1 단계에서 만든 승인자 그룹을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="35ad2-161">**Approval group**: Select the approvers group created in Step 1</span></span>

6. <span data-ttu-id="35ad2-p108">\*\*만들고 다음 \*\*닫기\*\*\*\* 를 선택 합니다. 완벽 하 게 구성 하 고 사용을 정책에 대 한 몇 분정도 걸릴 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="35ad2-p108">Select **Create** and then **Close**. It may take a few minutes for the policy to be fully configured and enabled.</span></span>

### <a name="using-exchange-management-powershell"></a><span data-ttu-id="35ad2-164">Exchange 관리 PowerShell을 사용 하 여</span><span class="sxs-lookup"><span data-stu-id="35ad2-164">Using Exchange Management PowerShell</span></span>

<span data-ttu-id="35ad2-165">다음 명령을 실행 Exchange 온라인를 만들고 승인 정책을 정의 하는 PowerShell:</span><span class="sxs-lookup"><span data-stu-id="35ad2-165">Run the following command in Exchange Online PowerShell to create and define an approval policy:</span></span>

```
New-ElevatedAccessApprovalPolicy -Task 'Exchange\<exchange management cmdlet name>' -ApprovalType <Manual, Auto> -ApproverGroup '<default/custom approver group>'
```
<span data-ttu-id="35ad2-166">예제:</span><span class="sxs-lookup"><span data-stu-id="35ad2-166">Example:</span></span>
```
New-ElevatedAccessApprovalPolicy -Task 'Exchange\New-MoveRequest' -ApprovalType Manual -ApproverGroup 'mbmanagers@fabrikamorg.onmicrosoft.com'
```

<span data-ttu-id="35ad2-167"><a name="step4"> </a></span><span class="sxs-lookup"><span data-stu-id="35ad2-167"></span></span>

## <a name="step-4-submitapprove-privileged-access-requests"></a><span data-ttu-id="35ad2-168">4 단계: 전송/요청을 승인 권한이 부여 된 액세스</span><span class="sxs-lookup"><span data-stu-id="35ad2-168">Step 4: Submit/approve privileged access requests</span></span>

### <a name="requesting-elevation-authorization-to-execute-privileged-tasks"></a><span data-ttu-id="35ad2-169">권한이 부여 된 작업을 실행할 수 상승 권한 부여를 요청 합니다.</span><span class="sxs-lookup"><span data-stu-id="35ad2-169">Requesting elevation authorization to execute privileged tasks</span></span>

<span data-ttu-id="35ad2-p109">권한이 부여 된 액세스에 대 한 요청은 요청을 제출 하는 최대 24 시간 동안 유효 합니다. 요청은 만료 되지 승인 또는 거부 하는 경우 및 액세스 승인 되지 않은 합니다.</span><span class="sxs-lookup"><span data-stu-id="35ad2-p109">Requests for privileged access are valid for up to 24 hours after the request is submitted. If not approved or denied, the requests expire and access is not approved.</span></span>

#### <a name="using-the-microsoft-365-admin-center"></a><span data-ttu-id="35ad2-172">Microsoft 365 관리 센터를 사용 하 여</span><span class="sxs-lookup"><span data-stu-id="35ad2-172">Using the Microsoft 365 Admin Center</span></span>

1. <span data-ttu-id="35ad2-173">사용자의 자격 증명을 사용 하 여 [Microsoft 365 관리 센터](https://portal.office.com) 에 로그인 합니다.</span><span class="sxs-lookup"><span data-stu-id="35ad2-173">Sign into the [Microsoft 365 Admin Center](https://portal.office.com) using your credentials.</span></span>

2. <span data-ttu-id="35ad2-174">관리 센터에서 **설정**으로 이동 > **보안 및 개인정보** > **권한이 부여 된 액세스**합니다.</span><span class="sxs-lookup"><span data-stu-id="35ad2-174">In the Admin Center, go to **Settings** > **Security & Privacy** > **Privileged access**.</span></span>

3. <span data-ttu-id="35ad2-175">**관리 액세스 정책 및 요청을**선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="35ad2-175">Select **Manage access policies and requests**.</span></span>

4. <span data-ttu-id="35ad2-p110">**새 요청**을 선택 합니다. 드롭다운 필드에서 조직에 대 한 적절 한 값을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="35ad2-p110">Select **New request**. From the drop-down fields, select the appropriate values for your organization:</span></span>

    <span data-ttu-id="35ad2-178">**요청 유형**: 작업, 역할 또는 역할 그룹</span><span class="sxs-lookup"><span data-stu-id="35ad2-178">**Request type**: Task, Role, or Role Group</span></span>

    <span data-ttu-id="35ad2-179">**범위 요청**: Exchange</span><span class="sxs-lookup"><span data-stu-id="35ad2-179">**Request scope**: Exchange</span></span>

    <span data-ttu-id="35ad2-180">**에 대 한 요청**: 사용 가능한 정책에서 선택</span><span class="sxs-lookup"><span data-stu-id="35ad2-180">**Request for**: Select from the available policies</span></span>

    <span data-ttu-id="35ad2-p111">**기간 (시간)**: 요청 된 액세스의 시간입니다. 요청할 수 있는 시간 수에 대 한 제한이 없습니다.</span><span class="sxs-lookup"><span data-stu-id="35ad2-p111">**Duration (hours)**: Number of hours of requested access. There isn't a limit on the number of hours that can be requested.</span></span>

    <span data-ttu-id="35ad2-183">**설명**: 액세스 요청에 관련 된 메모에 대 한 텍스트 필드</span><span class="sxs-lookup"><span data-stu-id="35ad2-183">**Comments**: Text field for comments related to your access request</span></span>

5. <span data-ttu-id="35ad2-p112">**저장** 한 다음 **닫기**를 선택 합니다. 전자 메일을 통해 승인자의 그룹에 사용자의 요청을 전송 됩니다.</span><span class="sxs-lookup"><span data-stu-id="35ad2-p112">Select **Save** and then **Close**. Your request will be sent to the approver's group via email.</span></span>

#### <a name="using-exchange-management-powershell"></a><span data-ttu-id="35ad2-186">Exchange 관리 PowerShell을 사용 하 여</span><span class="sxs-lookup"><span data-stu-id="35ad2-186">Using Exchange Management PowerShell</span></span>

<span data-ttu-id="35ad2-187">다음 명령을 실행 Exchange Online을 만들고 승인자의 그룹에 대 한 승인 요청을 제출 하는 PowerShell:</span><span class="sxs-lookup"><span data-stu-id="35ad2-187">Run the following command in Exchange Online PowerShell to create and submit an approval request to the approver's group:</span></span>
```
New-ElevatedAccessRequest -Task 'Exchange\<exchange management cmdlet name>' -Reason '<appropriate reason>' -DurationHours <duration in hours>
```
<span data-ttu-id="35ad2-188">예제:</span><span class="sxs-lookup"><span data-stu-id="35ad2-188">Example:</span></span>
```
New-ElevatedAccessRequest -Task 'Exchange\New-MoveRequest' -Reason 'Attempting to fix the user mailbox error' -DurationHours 4
```
### <a name="view-status-of-elevation-requests"></a><span data-ttu-id="35ad2-189">권한 상승 요청 상태 보기</span><span class="sxs-lookup"><span data-stu-id="35ad2-189">View status of elevation requests</span></span>
<span data-ttu-id="35ad2-190">승인 요청을 만든 후 상승 요청 상태를 검토 하 여 관리 센터의 수 또는 Exchange 관리 PowerShell을 사용 하 여 연결 된 요청 id를.합니다</span><span class="sxs-lookup"><span data-stu-id="35ad2-190">After an approval request is created, elevation request status can be reviewed in the Admin Center or in Exchange Management PowerShell using the associated with request ID.</span></span>

#### <a name="using-the-microsoft-365-admin-center"></a><span data-ttu-id="35ad2-191">Microsoft 365 관리 센터를 사용 하 여</span><span class="sxs-lookup"><span data-stu-id="35ad2-191">Using the Microsoft 365 Admin Center</span></span>

1. <span data-ttu-id="35ad2-192">사용자의 자격 증명을 사용 하 여 [Microsoft 365 관리 센터](https://portal.office.com) 에 로그인 합니다.</span><span class="sxs-lookup"><span data-stu-id="35ad2-192">Sign into the [Microsoft 365 Admin Center](https://portal.office.com) using your credentials.</span></span>

2. <span data-ttu-id="35ad2-193">관리 센터에서 **설정**으로 이동 > **보안 및 개인정보** > **권한이 부여 된 액세스**합니다.</span><span class="sxs-lookup"><span data-stu-id="35ad2-193">In the Admin Center, go to **Settings** > **Security & Privacy** > **Privileged access**.</span></span>

3. <span data-ttu-id="35ad2-194">**관리 액세스 정책 및 요청을**선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="35ad2-194">Select **Manage access policies and requests**.</span></span>

4. <span data-ttu-id="35ad2-195">**보류 중인**, **승인**, **거부**또는 **고객 Lockbox** 상태별으로 제출 된 요청을 필터링 하려면 **보기** 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="35ad2-195">Select **View** to filter submitted requests by **Pending**, **Approved**, **Denied**, or **Customer Lockbox** status.</span></span>

#### <a name="using-exchange-management-powershell"></a><span data-ttu-id="35ad2-196">Exchange 관리 PowerShell을 사용 하 여</span><span class="sxs-lookup"><span data-stu-id="35ad2-196">Using Exchange Management PowerShell</span></span>

<span data-ttu-id="35ad2-197">다음 명령을 실행 Exchange 온라인 PowerShell 특정 요청 ID에 대 한 승인 요청 상태를 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="35ad2-197">Run the following command in Exchange Online PowerShell to view a approval request status for a specific request ID:</span></span>
```
Get-ElevatedAccessRequest -Identity <request ID> | select RequestStatus
```
<span data-ttu-id="35ad2-198">예제:</span><span class="sxs-lookup"><span data-stu-id="35ad2-198">Example:</span></span>
```
Get-ElevatedAccessRequest -Identity 28560ed0-419d-4cc3-8f5b-603911cbd450 | select RequestStatus
```

### <a name="approving-an-elevation-authorization-request"></a><span data-ttu-id="35ad2-199">권한 상승 권한 부여 요청이 승인</span><span class="sxs-lookup"><span data-stu-id="35ad2-199">Approving an elevation authorization request</span></span>
<span data-ttu-id="35ad2-p113">관련 승인자 그룹의 구성원이 전자 메일 알림을 받게 됩니다 및 요청 ID와 연결 된 요청을 승인할 수를 승인 요청을 만들 때 검토자가 요청자의 요청 승인 또는 거부 전자 메일 메시지를 통해 알림을 받게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="35ad2-p113">When an approval request is created, members of the relevant approver group will receive an email notification and can approve the request associated with the request ID. The requestor will be notified of the request approval or denial via email message.</span></span>

#### <a name="using-the-microsoft-365-admin-center"></a><span data-ttu-id="35ad2-202">Microsoft 365 관리 센터를 사용 하 여</span><span class="sxs-lookup"><span data-stu-id="35ad2-202">Using the Microsoft 365 Admin Center</span></span>

1. <span data-ttu-id="35ad2-203">사용자의 자격 증명을 사용 하 여 [Microsoft 365 관리 센터](https://portal.office.com) 에 로그인 합니다.</span><span class="sxs-lookup"><span data-stu-id="35ad2-203">Sign into the [Microsoft 365 Admin Center](https://portal.office.com) using your credentials.</span></span>

2. <span data-ttu-id="35ad2-204">관리 센터에서 **설정**으로 이동 > **보안 및 개인정보** > **권한이 부여 된 액세스**합니다.</span><span class="sxs-lookup"><span data-stu-id="35ad2-204">In the Admin Center, go to **Settings** > **Security & Privacy** > **Privileged access**.</span></span>

3. <span data-ttu-id="35ad2-205">**관리 액세스 정책 및 요청을**선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="35ad2-205">Select **Manage access policies and requests**.</span></span>

4. <span data-ttu-id="35ad2-206">나열 된 요청 세부 정보를 표시 하 고 요청 시 조치를 취할 수를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="35ad2-206">Select a listed request to view the details and to take action on the request.</span></span>

5. <span data-ttu-id="35ad2-p114">**승인** 요청을 승인 요청을 거부 하려면 **거부** 선택 하거나 선택 합니다. 이전에 승인 된 요청이 **해지**를 선택 하 여 해지 액세스를 가질 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="35ad2-p114">Select **Approve** to approve the request or select **Deny** to deny the request. Previously approved requests can have access revoked by selecting **Revoke**.</span></span>

#### <a name="using-exchange-management-powershell"></a><span data-ttu-id="35ad2-209">Exchange 관리 PowerShell을 사용 하 여</span><span class="sxs-lookup"><span data-stu-id="35ad2-209">Using Exchange Management PowerShell</span></span>

<span data-ttu-id="35ad2-210">다음 명령을 실행 Exchange 온라인는 상승 인증 요청을 승인 하는 PowerShell:</span><span class="sxs-lookup"><span data-stu-id="35ad2-210">Run the following command in Exchange Online PowerShell to approve an elevation authorization request:</span></span>

```
Approve-ElevatedAccessRequest -RequestId <request id> -Comment '<approval comment>'
```
<span data-ttu-id="35ad2-211">예제:</span><span class="sxs-lookup"><span data-stu-id="35ad2-211">Example:</span></span>
```
Approve-ElevatedAccessRequest -RequestId a4bc1bdf-00a1-42b4-be65-b6c63d6be279 -Comment '<approval comment>'
```

<span data-ttu-id="35ad2-212">다음 명령을 실행 Exchange Online PowerShell는 상승 인증 요청을 거부 하려면:</span><span class="sxs-lookup"><span data-stu-id="35ad2-212">Run the following command in Exchange Online PowerShell to deny an elevation authorization request:</span></span>

```
Deny-ElevatedAccessRequest -RequestId <request id> -Comment '<denial comment>'
```
<span data-ttu-id="35ad2-213">예제:</span><span class="sxs-lookup"><span data-stu-id="35ad2-213">Example:</span></span>
```
Deny-ElevatedAccessRequest -RequestId a4bc1bdf-00a1-42b4-be65-b6c63d6be279 -Comment '<denial comment>'
```

## <a name="delete-a-privileged-access-policy-in-office-365"></a><span data-ttu-id="35ad2-214">Office 365에서 권한이 부여 된 액세스 정책 삭제</span><span class="sxs-lookup"><span data-stu-id="35ad2-214">Delete a privileged access policy in Office 365</span></span>
<span data-ttu-id="35ad2-215">조직에서 더이상 필요할 경우 권한이 부여 된 액세스 정책을 삭제할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="35ad2-215">You can delete a privileged access policy if it is no longer needed in your organization.</span></span>

### <a name="using-the-microsoft-365-admin-center"></a><span data-ttu-id="35ad2-216">Microsoft 365 관리 센터를 사용 하 여</span><span class="sxs-lookup"><span data-stu-id="35ad2-216">Using the Microsoft 365 Admin Center</span></span>

1. <span data-ttu-id="35ad2-217">조직에서 관리 계정에 대 한 자격 증명을 사용 하 여 [Microsoft 365 관리 센터](https://portal.office.com) 에 로그인 합니다.</span><span class="sxs-lookup"><span data-stu-id="35ad2-217">Sign into the [Microsoft 365 Admin Center](https://portal.office.com) using credentials for an admin account in your organization.</span></span>

2. <span data-ttu-id="35ad2-218">관리 센터에서 **설정**으로 이동 > **보안 및 개인정보** > **권한이 부여 된 액세스**합니다.</span><span class="sxs-lookup"><span data-stu-id="35ad2-218">In the Admin Center, go to **Settings** > **Security & Privacy** > **Privileged access**.</span></span>

3. <span data-ttu-id="35ad2-219">**관리 액세스 정책 및 요청을**선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="35ad2-219">Select **Manage access policies and requests**.</span></span>

4. <span data-ttu-id="35ad2-220">**Configure 정책**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="35ad2-220">Select **Configure policies**.</span></span>

5. <span data-ttu-id="35ad2-221">삭제 하려는 정책을 선택 하 고 **정책 제거**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="35ad2-221">Select the policy you want to delete, then select **Remove Policy**.</span></span>

6. <span data-ttu-id="35ad2-222">**Close**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="35ad2-222">Select **Close**.</span></span>

### <a name="using-exchange-management-powershell"></a><span data-ttu-id="35ad2-223">Exchange 관리 PowerShell을 사용 하 여</span><span class="sxs-lookup"><span data-stu-id="35ad2-223">Using Exchange Management PowerShell</span></span>

<span data-ttu-id="35ad2-224">다음 명령을 실행 Exchange Online Powershell 권한이 부여 된 액세스 정책을 삭제 하려면:</span><span class="sxs-lookup"><span data-stu-id="35ad2-224">Run the following command in Exchange Online Powershell to delete a privileged access policy:</span></span>

```
Remove-ElevatedAccessApprovalPolicy -Identity <identity GUID of the policy you want to delete>
```

## <a name="disable-privileged-access-in-office-365"></a><span data-ttu-id="35ad2-225">Office 365에 대 한 액세스 권한을된 사용 하지 않도록 설정</span><span class="sxs-lookup"><span data-stu-id="35ad2-225">Disable privileged access in Office 365</span></span>

<span data-ttu-id="35ad2-p115">필요한 경우에 조직에 대 한 액세스 권한을된 관리를 비활성화할 수 있습니다. 권한 사용 하지 않도록 설정 액세스 삭제 되지 않습니다 모든 관련된 승인 정책 또는 승인자 그룹.</span><span class="sxs-lookup"><span data-stu-id="35ad2-p115">If needed, you can disable privileged access management for your organization. Disabling privileged access does not delete any associated approval policies or approver groups.</span></span>

### <a name="using-the-microsoft-365-admin-center"></a><span data-ttu-id="35ad2-228">Microsoft 365 관리 센터를 사용 하 여</span><span class="sxs-lookup"><span data-stu-id="35ad2-228">Using the Microsoft 365 Admin Center</span></span>

1. <span data-ttu-id="35ad2-229">조직에서 관리 계정에 대 한 자격 증명을 사용 하 여 [Microsoft 365 관리 센터](https://portal.office.com) 에 로그인 합니다.</span><span class="sxs-lookup"><span data-stu-id="35ad2-229">Sign into the [Microsoft 365 Admin Center](https://portal.office.com) using credentials for an admin account in your organization.</span></span>

2. <span data-ttu-id="35ad2-230">관리 센터에서 **설정**으로 이동 > **보안 및 개인정보** > **권한이 부여 된 액세스**합니다.</span><span class="sxs-lookup"><span data-stu-id="35ad2-230">In the Admin Center, go to **Settings** > **Security & Privacy** > **Privileged access**.</span></span>

3. <span data-ttu-id="35ad2-231">**권한이 부여 된 액세스에 대 한 승인 필요** 제어를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="35ad2-231">Enable the **Require approvals for privileged access** control.</span></span>

### <a name="using-exchange-management-powershell"></a><span data-ttu-id="35ad2-232">Exchange 관리 PowerShell을 사용 하 여</span><span class="sxs-lookup"><span data-stu-id="35ad2-232">Using Exchange Management PowerShell</span></span>

<span data-ttu-id="35ad2-233">다음 명령을 실행 Exchange Online Powershell 액세스 권한을된 사용 하지 않도록 설정 하려면:</span><span class="sxs-lookup"><span data-stu-id="35ad2-233">Run the following command in Exchange Online Powershell to disable privileged access:</span></span>

```
Disable-ElevatedAccessControl
```