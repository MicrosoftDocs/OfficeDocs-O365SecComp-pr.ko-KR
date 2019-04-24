---
title: Office 365의 권한이 부여 된 액세스 관리
ms.author: robmazz
author: robmazz
manager: laurawi
ms.audience: ITPro
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
description: 이 항목을 사용 하 여 Office 365의 권한이 부여 된 액세스 관리에 대해 자세히 알아보세요.
ms.openlocfilehash: e03b615971b90e8443f73c3ec8c4cd3febe90450
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32261857"
---
# <a name="privileged-access-management-in-office-365"></a><span data-ttu-id="e2207-103">Office 365의 권한이 부여 된 액세스 관리</span><span class="sxs-lookup"><span data-stu-id="e2207-103">Privileged access management in Office 365</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e2207-104">이 항목에서는 현재 Office 365 E5 및 고급 규정 준수 sku에서 사용할 수 있는 기능에 대 한 배포 및 구성 지침에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2207-104">This topic covers deployment and configuration guidance for features only currently available in Office 365 E5 and Advanced Compliance SKUs.</span></span>

<span data-ttu-id="e2207-105">권한이 부여 된 액세스 관리를 통해 Office 365의 권한 있는 관리 작업을 세부적으로 제어할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e2207-105">Privileged access management allows granular access control over privileged admin tasks in Office 365.</span></span> <span data-ttu-id="e2207-106">이는 중요 한 데이터에 대 한 액세스 또는 중요 한 구성 설정에 대 한 액세스 권한이 있는 기존 권한 관리 계정을 사용 하는 행위 로부터 조직을 보호 하는 데 도움이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e2207-106">It can help protect your organization from breaches that use existing privileged admin accounts with standing access to sensitive data or access to critical configuration settings.</span></span> <span data-ttu-id="e2207-107">권한이 부여 된 액세스 관리를 사용 하려면 사용자가 높은 범위 및 시간 제한 승인 워크플로를 통해 권한 있는 작업을 완료 하기 위해 just-in-time 액세스를 요청 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2207-107">Privileged access management requires users to request just-in-time access to complete elevated and privileged tasks through a highly scoped and time-bounded approval workflow.</span></span> <span data-ttu-id="e2207-108">이렇게 하면 중요 한 데이터 나 중요 한 구성 설정을 노출 하지 않고 직접 작업을 수행할 수 있는 권한이 사용자에 게 제공 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e2207-108">This gives users just-enough-access to perform the task at hand, without risking exposure of sensitive data or critical configuration settings.</span></span> <span data-ttu-id="e2207-109">Office 365에서 권한이 부여 된 액세스 관리를 사용 하도록 설정 하면 조직에서 단일 권한으로 작동 하 고 단일 관리 액세스 취약성에 대 한 방어 계층을 제공할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e2207-109">Enabling privileged access management in Office 365 allows your organization to operate with zero standing privileges and provide a layer of defense against standing administrative access vulnerabilities.</span></span>

<span data-ttu-id="e2207-110">통합 고객 lockbox 및 권한이 부여 된 액세스 관리 워크플로에 대 한 간략 한 개요를 보려면 [Office 365 비디오에서이 고객 lockbox 및 권한이 부여 된 액세스 관리](https://go.microsoft.com/fwlink/?linkid=2066800)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="e2207-110">For a quick overview of the integrated Customer Lockbox and privileged access management workflow, see this [Customer Lockbox and privileged access management in Office 365 video](https://go.microsoft.com/fwlink/?linkid=2066800).</span></span>

## <a name="layers-of-protection"></a><span data-ttu-id="e2207-111">보호 계층</span><span class="sxs-lookup"><span data-stu-id="e2207-111">Layers of protection</span></span>

<span data-ttu-id="e2207-112">권한이 부여 된 액세스 관리는 Office 365 보안 아키텍처 내에서 다른 데이터 및 액세스 기능 보호를 보완 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2207-112">Privileged access management complements other data and access feature protections within the Office 365 security architecture.</span></span> <span data-ttu-id="e2207-113">보안에 대 한 통합 및 계층화 방식의 일부로 권한 있는 액세스 관리를 포함 하면 중요 한 정보 및 Office 365 구성 설정의 보호를 최대화 하는 보안 모델을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2207-113">Including privileged access management as part of an integrated and layered approach to security provides a security model that maximizes protection of sensitive information and Office 365 configuration settings.</span></span> <span data-ttu-id="e2207-114">다이어그램에 표시 된 것 처럼, 권한 있는 액세스 관리는 office 365 서비스의 역할 기반 액세스 제어 보안 모델 및 office 365 데이터에 대 한 기본 암호화와 함께 제공 되는 보호 기능을 기반으로 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2207-114">As shown in the diagram, privileged access management builds on the protection provided with native encryption of Office 365 data and the role-based access control security model of Office 365 services.</span></span> <span data-ttu-id="e2207-115">이러한 두 기능은 [Azure AD 권한이 부여 된 id 관리](https://docs.microsoft.com/azure/active-directory/active-directory-privileged-identity-management-configure)와 함께 사용 하는 경우 서로 다른 범위의 just-in-time 액세스를 사용 하 여 액세스 제어를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2207-115">When used with [Azure AD Privileged Identity Management](https://docs.microsoft.com/azure/active-directory/active-directory-privileged-identity-management-configure), these two features provide access control with just-in-time access at different scopes.</span></span>

![Office 365의 계층화 된 보호 기능](media/pam-layered-protection.png)

<span data-ttu-id="e2207-117">Office 365의 권한이 부여 된 액세스 관리는 **작업** 수준에서 정의 되 고 범위가 지정 되는 반면 Azure AD 권한이 부여 된 id 관리는 **역할** 수준의 보호를 여러 작업을 실행 하는 기능과 함께 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2207-117">Privileged access management in Office 365 is defined and scoped at the **task** level, while Azure AD Privileged Identity Management applies protection at the **role** level with the ability to execute multiple tasks.</span></span> <span data-ttu-id="e2207-118">Azure ad 권한 있는 id 관리는 주로 AD 역할 및 역할 그룹에 대 한 액세스 관리를 허용 하지만, Office 365의 권한 있는 액세스 관리는 작업 수준 에서만 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e2207-118">Azure AD Privileged Identity Management primarily allows managing accesses for AD roles and role groups, while privileged access management in Office 365 applies only at the task level.</span></span>

- <span data-ttu-id="e2207-119">**이미 Azure AD 권한 id 관리를 사용 하는 동안 Office 365에서 권한이 부여 된 액세스 관리를 사용 하도록 설정:** office 365에서 권한이 부여 된 액세스 관리를 추가 하면 office 365 데이터에 대 한 권한 있는 액세스에 대 한 다양 한 보호 및 감사 기능 계층이 제공 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e2207-119">**Enabling privileged access management in Office 365 while already using Azure AD Privileged Identity Management:** Adding privileged access management in Office 365 provides another granular layer of protection and audit capabilities for privileged access to Office 365 data.</span></span>

- <span data-ttu-id="e2207-120">**Office 365에서 권한이 부여 된 액세스 관리를 이미 사용 하 고 있는 동안 Azure AD 권한 id 관리를 사용 하도록 설정:**  office 365의 권한이 부여 된 액세스 관리에 Azure AD 권한 id 관리를 추가 하면 사용자 역할 또는 id로 정의 되는 office 365 외부의 데이터에 대 한 권한 있는 액세스를 확장할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e2207-120">**Enabling Azure AD Privileged Identity Management while already using privileged access management in Office 365:**  Adding Azure AD Privileged Identity Management to privileged access management in Office 365 can extend privileged access to data outside of Office 365 that’s primarily defined by user roles or identity.</span></span>  

## <a name="privileged-access-management-architecture-and-process-flow"></a><span data-ttu-id="e2207-121">권한 있는 액세스 관리 아키텍처 및 프로세스 흐름</span><span class="sxs-lookup"><span data-stu-id="e2207-121">Privileged access management architecture and process flow</span></span>

<span data-ttu-id="e2207-122">다음 각 프로세스는 권한 있는 액세스의 아키텍처와 office 365 기판, office 365 감사 및 Exchange 관리 runspace와 상호 작용 하는 방식을 대략적으로 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="e2207-122">Each of the following process flows outline the architecture of privileged access and how it interacts with the Office 365 substrate, Office 365 auditing, and the Exchange Management runspace.</span></span>

### <a name="step-1-configure-a-privileged-access-policy"></a><span data-ttu-id="e2207-123">1 단계: 권한이 부여 된 액세스 정책 구성</span><span class="sxs-lookup"><span data-stu-id="e2207-123">Step 1: Configure a privileged access policy</span></span>

<span data-ttu-id="e2207-124">[Microsoft 365 관리 센터](https://admin.microsoft.com) 또는 Exchange 관리 PowerShell을 사용 하 여 권한 있는 액세스 정책을 구성 하는 경우 정책 및 권한 있는 액세스 기능 프로세스와 Office 365 기판의 정책 특성을 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2207-124">When you configure a privileged access policy with the [Microsoft 365 admin center](https://admin.microsoft.com) or the Exchange Management PowerShell, you define the policy and the privileged access feature processes and the policy attributes in the Office 365 substrate.</span></span> <span data-ttu-id="e2207-125">이 작업은 Office 365 보안 및 준수 센터에 기록 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e2207-125">The activities are logged in the Office 365 Security and Compliance Center.</span></span> <span data-ttu-id="e2207-126">이제 정책이 사용 하도록 설정 되어 있으며 승인 된 승인을 요청을 처리할 준비가 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e2207-126">The policy is now enabled and ready to handle incoming requests for approvals.</span></span>

![1 단계: 정책 만들기](media/pam-step1-policy-creation.jpg)

### <a name="step-2-access-request"></a><span data-ttu-id="e2207-128">2 단계: 액세스 요청</span><span class="sxs-lookup"><span data-stu-id="e2207-128">Step 2: Access request</span></span>

<span data-ttu-id="e2207-129">[Microsoft 365 관리 센터](https://admin.microsoft.com) 또는 Exchange 관리 PowerShell을 사용 하 여 사용자는 상승 되거나 권한 있는 작업에 대 한 액세스를 요청할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e2207-129">In the [Microsoft 365 admin center](https://admin.microsoft.com) or with the Exchange Management PowerShell, users can request access to elevated or privileged tasks.</span></span> <span data-ttu-id="e2207-130">권한 있는 액세스 기능은 구성 된 권한 액세스 정책에 대 한 처리를 위해 office 365 기판에 요청을 전송 하 고 office 365 보안 및 준수 센터 로그에 해당 활동을 기록 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2207-130">The privileged access feature sends the request to the Office 365 substrate for processing against the configured privilege access policy and records the Activity in the Office 365 Security and Compliance Center logs.</span></span>

![2 단계: 액세스 요청](media/pam-step2-access-request.jpg)

### <a name="step-3-access-approval"></a><span data-ttu-id="e2207-132">3 단계: 액세스 승인</span><span class="sxs-lookup"><span data-stu-id="e2207-132">Step 3: Access approval</span></span>

<span data-ttu-id="e2207-133">승인 요청이 생성 되 고 대기 중인 요청 알림이 승인자에 게 전자 메일로 전송 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e2207-133">An approval request is generated and the pending request notification is emailed to approvers.</span></span> <span data-ttu-id="e2207-134">승인 된 경우 권한 있는 액세스 요청이 승인으로 처리 되 고 작업이 완료 될 준비가 된 것입니다.</span><span class="sxs-lookup"><span data-stu-id="e2207-134">If approved, the privileged access request is processed as an approval and the task is ready to be completed.</span></span> <span data-ttu-id="e2207-135">거부 되 면 작업이 차단 되 고 해당 요청에 대 한 액세스 권한이 부여 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e2207-135">If denied, the task is blocked and no access is granted to the requestor.</span></span> <span data-ttu-id="e2207-136">요청자에 게는 전자 메일 메시지를 통한 승인 또는 거부 요청이 통지 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e2207-136">The requestor is notified of the request approval or denial via email message.</span></span>

![3 단계: 액세스 승인](media/pam-step3-access-approval.jpg)

### <a name="step-4-access-processing"></a><span data-ttu-id="e2207-138">4 단계: 액세스 처리</span><span class="sxs-lookup"><span data-stu-id="e2207-138">Step 4: Access processing</span></span>

<span data-ttu-id="e2207-139">승인 된 요청의 경우 Exchange 관리 runspace가 작업을 처리 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2207-139">For an approved request, the task is processed by the Exchange Management runspace.</span></span> <span data-ttu-id="e2207-140">승인 된 액세스 정책을 확인 하 고 Office 365 기판에서 처리 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2207-140">The approval is checked against the privileged access policy and processed by the Office 365 substrate.</span></span> <span data-ttu-id="e2207-141">작업에 대 한 모든 활동은 Office 365 보안 및 준수 센터에 기록 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e2207-141">All activity for the task is logged in the Office 365 Security and Compliance Center.</span></span>

![4 단계: 액세스 처리](media/pam-step4-access-processing.jpg)

## <a name="frequently-asked-questions"></a><span data-ttu-id="e2207-143">자주하는 질문</span><span class="sxs-lookup"><span data-stu-id="e2207-143">Frequently asked questions</span></span>

### <a name="what-skus-can-use-privileged-access-in-office-365"></a><span data-ttu-id="e2207-144">Office 365에서 어떤 sku가 권한 있는 액세스를 사용할 수 있나요?</span><span class="sxs-lookup"><span data-stu-id="e2207-144">What SKUs can use privileged access in Office 365?</span></span>
<span data-ttu-id="e2207-145">Office 365 E5 및 Advanced 준수 sku가 있는 고객은 권한 있는 액세스 관리를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e2207-145">Privileged access management is available for customers with Office 365 E5 and Advanced Compliance SKUs.</span></span>

### <a name="when-will-privileged-access-support-office-365-workloads-beyond-exchange"></a><span data-ttu-id="e2207-146">권한 있는 access가 Exchange 보다 Office 365 워크 로드를 지원 하나요?</span><span class="sxs-lookup"><span data-stu-id="e2207-146">When will privileged access support Office 365 workloads beyond Exchange?</span></span>
<span data-ttu-id="e2207-147">권한 있는 액세스 관리는 곧 다른 Office 365 작업에서 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e2207-147">Privileged access management will be available in other Office 365 workloads soon.</span></span> <span data-ttu-id="e2207-148">자세한 내용은 [Microsoft 365 로드맵](https://www.microsoft.com/microsoft-365/roadmap) 를 방문 하세요.</span><span class="sxs-lookup"><span data-stu-id="e2207-148">Visit the [Microsoft 365 Roadmap](https://www.microsoft.com/microsoft-365/roadmap) for more details.</span></span>

### <a name="my-organization-needs-more-than-30-privileged-access-policies-will-this-limit-be-increased"></a><span data-ttu-id="e2207-149">조직에서 사용 하는 액세스 정책이 30 개를 초과 하는 경우이 제한이 증가 하나요?</span><span class="sxs-lookup"><span data-stu-id="e2207-149">My organization needs more than 30 privileged access policies, will this limit be increased?</span></span>
<span data-ttu-id="e2207-150">예, Office 365 조 직 당 권한 있는 액세스 정책 30 개를 최신으로 올리는 기능이 기능 로드맵에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e2207-150">Yes, raising the current limit of 30 privileged access policies per Office 365 organization is on the feature roadmap.</span></span>

### <a name="do-i-need-to-be-a-global-admin-to-manage-privileged-access-in-office-365"></a><span data-ttu-id="e2207-151">Office 365에서 권한이 부여 된 액세스를 관리 하려면 전역 관리자 여야 하나요?</span><span class="sxs-lookup"><span data-stu-id="e2207-151">Do I need to be a Global Admin to manage privileged access in Office 365?</span></span>
<span data-ttu-id="e2207-152">아니요, Office 365에서 권한이 부여 된 액세스를 관리 하는 계정에 할당 된 Exchange 역할 관리 역할이 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2207-152">No, you need the Exchange Role Management role assigned to accounts that manage privileged access in Office 365.</span></span> <span data-ttu-id="e2207-153">역할 관리 역할을 독립 실행형 계정 권한으로 구성 하지 않을 경우 전역 관리자 역할에는 기본적으로이 역할이 포함 되며 권한이 부여 된 액세스를 관리할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e2207-153">If you don’t want to configure the Role Management role as a stand-alone account permission, the Global Administrator role includes this role by default and can manage privileged access.</span></span> <span data-ttu-id="e2207-154">승인자 그룹에 포함 된 사용자는 전역 관리자가 아니어도 되 고 요청을 검토 및 승인 하기 위해 역할 관리 역할을 할당할 필요가 없습니다.</span><span class="sxs-lookup"><span data-stu-id="e2207-154">Users included in an approvers’ group don't need to be a Global Admin or have the Role Management role assigned to review and approve requests.</span></span>

### <a name="how-is-privileged-access-management-in-office-365-related-to-customer-lockbox"></a><span data-ttu-id="e2207-155">Office 365의 권한이 부여 된 액세스 관리는 어떤 방식으로 고객 Lockbox와 관련 됩니까?</span><span class="sxs-lookup"><span data-stu-id="e2207-155">How is privileged access management in Office 365 related to Customer Lockbox?</span></span>
<span data-ttu-id="e2207-156">[고객 Lockbox](https://docs.microsoft.com/office365/admin/manage/customer-lockbox-requests) 는 Microsoft가 데이터에 액세스할 때 조직에 대 한 액세스 제어 수준을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2207-156">[Customer Lockbox](https://docs.microsoft.com/office365/admin/manage/customer-lockbox-requests) allows a level of access control for organizations when Microsoft accesses data.</span></span> <span data-ttu-id="e2207-157">office 365의 권한이 부여 된 액세스 관리를 통해 조직 내의 모든 Office 365 권한 작업에 대 한 세부적인 액세스 제어를 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2207-157">Privileged access management in Office 365 allows granular access control within an organization for all Office 365 privileged tasks.</span></span>

## <a name="ready-to-get-started"></a><span data-ttu-id="e2207-158">시작할 준비가 되셨습니까?</span><span class="sxs-lookup"><span data-stu-id="e2207-158">Ready to get started?</span></span>

<span data-ttu-id="e2207-159">[권한 있는 액세스 관리를 위한 조직 구성을](privileged-access-management-configuration.md)시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2207-159">Start [configuring your organization for privileged access management](privileged-access-management-configuration.md).</span></span>

## <a name="learn-more"></a><span data-ttu-id="e2207-160">자세한 정보</span><span class="sxs-lookup"><span data-stu-id="e2207-160">Learn more</span></span>

[<span data-ttu-id="e2207-161">대화형 가이드: 권한이 부여 된 액세스 관리로 관리자 작업 모니터링 및 제어</span><span class="sxs-lookup"><span data-stu-id="e2207-161">Interactive guide: Monitor and control administrator tasks with privileged access management</span></span>](https://content.cloudguides.com/en-us/guides/Privileged%20Access%20Management)