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
ms.openlocfilehash: 2a464bacaa568515e470e29a0c9c45a91a79cf8e
ms.sourcegitcommit: e7a776a04ef6ed5e287a33cfdc36aa2d72862b55
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/29/2019
ms.locfileid: "31001251"
---
# <a name="privileged-access-management-in-office-365"></a><span data-ttu-id="956c0-103">Office 365의 권한이 부여 된 액세스 관리</span><span class="sxs-lookup"><span data-stu-id="956c0-103">Privileged access management in Office 365</span></span>

> [!IMPORTANT]
> <span data-ttu-id="956c0-104">이 항목에서는 현재 Office 365 E5 및 고급 규정 준수 sku에서 사용할 수 있는 기능에 대 한 배포 및 구성 지침에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="956c0-104">This topic covers deployment and configuration guidance for features only currently available in Office 365 E5 and Advanced Compliance SKUs.</span></span>

<span data-ttu-id="956c0-105">권한이 부여 된 액세스 관리를 통해 Office 365의 권한 있는 관리 작업을 세부적으로 제어할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="956c0-105">Privileged access management allows granular access control over privileged admin tasks in Office 365.</span></span> <span data-ttu-id="956c0-106">중요 한 데이터에 대 한 액세스 권한이 나 중요 한 구성 설정에 대 한 액세스 권한이 있는 기존 권한 관리 계정을 사용 하는 보안 침해 로부터 조직을 보호 하는 데 도움이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="956c0-106">It can help protect your organization from breaches that may use existing privileged admin accounts with standing access to sensitive data or access to critical configuration settings.</span></span> <span data-ttu-id="956c0-107">권한이 부여 된 액세스 관리를 사용 하도록 설정한 후에는 사용자가 높은 범위의 액세스 및 시간 범위를 지정 하는 승인 워크플로를 통해 관리자 권한 및 권한 있는 작업을 완료 하기 위한 요청을 수행 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="956c0-107">After enabling privileged access management, users will need to request just-in-time access to complete elevated and privileged tasks through an approval workflow that is highly scoped and time-bound.</span></span> <span data-ttu-id="956c0-108">이렇게 하면 중요 한 데이터 나 중요 한 구성 설정을 노출 하지 않고 직접 작업을 수행할 수 있는 권한이 사용자에 게 제공 됩니다.</span><span class="sxs-lookup"><span data-stu-id="956c0-108">This gives users just-enough-access to perform the task at hand, without risking exposure of sensitive data or critical configuration settings.</span></span> <span data-ttu-id="956c0-109">Office 365에서 권한이 부여 된 액세스 관리를 사용 하도록 설정 하면 조직이 제로 권한을 사용 하 여 작업을 수행 하 고 해당 하는 관리 액세스로 인해 발생 하는 취약성에 대 한 방어 계층을 제공할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="956c0-109">Enabling privileged access management in Office 365 will enable your organization to operate with zero standing privileges and provide a layer of defense against vulnerabilities arising because of such standing administrative access.</span></span>

<span data-ttu-id="956c0-110">통합 고객 lockbox 및 권한이 부여 된 액세스 관리 종단간 워크플로에 대 한 간략 한 개요를 보려면 [Office 365 비디오에서이 고객 lockbox 및 권한이 부여 된 액세스 관리](https://go.microsoft.com/fwlink/?linkid=2066800)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="956c0-110">For a quick overview of the integrated Customer Lockbox and privileged access management end-to-end workflow, see this [Customer Lockbox and privileged access management in Office 365 video](https://go.microsoft.com/fwlink/?linkid=2066800).</span></span>

## <a name="layers-of-protection"></a><span data-ttu-id="956c0-111">보호 계층</span><span class="sxs-lookup"><span data-stu-id="956c0-111">Layers of protection</span></span>

<span data-ttu-id="956c0-112">권한이 부여 된 액세스 관리는 Office 365 보안 아키텍처 내에서 다른 데이터 및 액세스 기능 보호를 보완 합니다.</span><span class="sxs-lookup"><span data-stu-id="956c0-112">Privileged access management complements other data and access feature protections within the Office 365 security architecture.</span></span> <span data-ttu-id="956c0-113">보안에 대 한 통합 된 접근 방식의 일부로 권한 있는 액세스 관리를 사용 하도록 설정 하면 계층화 된 보안 모델을 사용 하 여 중요 한 정보 및 Office 365 구성 설정의 보호를 최대화할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="956c0-113">By enabling privileged access management as part of an integrated approach to security and protecting your organization, a layered security model can be used to maximize protection of sensitive information and Office 365 configuration settings.</span></span> <span data-ttu-id="956c0-114">아래 다이어그램에 나와 있는 것 처럼, 권한이 부여 된 액세스 관리를 사용 하도록 설정 하면 office 365 서비스의 역할 기반 액세스 제어 보안 모델 및 기본 암호화를 통해 제공 되는 보호 기능을 구축할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="956c0-114">As shown in the diagram below, enabling privileged access management helps builds on the protection provided with native encryption of Office 365 data and the role based access control security model of Office 365 services.</span></span> <span data-ttu-id="956c0-115">이러한 두 기능은 [Azure AD 권한 부여 id 관리](https://docs.microsoft.com/azure/active-directory/active-directory-privileged-identity-management-configure)와 함께 사용 되는 경우 서로 다른 범위의 just-in-time 액세스를 사용 하 여 액세스 제어를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="956c0-115">When used in conjunction with [Azure AD Privileged Identity Management](https://docs.microsoft.com/azure/active-directory/active-directory-privileged-identity-management-configure), these two features provide access control with just-in-time access at different scopes.</span></span>

![Office 365의 계층화 된 보호 기능](media/pam-layered-protection.png)

<span data-ttu-id="956c0-117">Office 365의 권한이 부여 된 액세스 관리는 **작업** 수준에서 정의 하 고 범위를 지정할 수 있으며, Azure AD 권한이 부여 된 id 관리는 **역할** 수준의 보호를 여러 작업을 실행 하는 기능과 함께 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="956c0-117">Privileged access management in Office 365 can be defined and scoped at the **task** level, while Azure AD Privileged Identity Management applies protection at the **role** level with the ability to execute multiple tasks.</span></span>  <span data-ttu-id="956c0-118">Azure ad 권한 있는 id 관리는 주로 AD 역할 및 역할 그룹에 대 한 액세스 관리를 허용 하지만, Office 365의 권한 있는 액세스 관리는 작업 수준에만 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="956c0-118">Azure AD Privileged Identity Management primarily allows managing accesses for AD roles and role groups, while privileged access management in Office 365 is applied only at the task level.</span></span>

- <span data-ttu-id="956c0-119">**이미 Azure AD 권한 id 관리를 사용 하는 동안 Office 365에서 권한이 부여 된 액세스 관리를 사용 하도록 설정:** office 365에서 권한이 부여 된 액세스 관리를 추가 하면 office 365 데이터에 대 한 권한 있는 액세스에 대 한 다양 한 보호 및 감사 기능 계층이 제공 됩니다.</span><span class="sxs-lookup"><span data-stu-id="956c0-119">**Enabling privileged access management in Office 365 while already using Azure AD Privileged Identity Management:** Adding privileged access management in Office 365 provides another granular layer of protection and audit capabilities for privileged access to Office 365 data.</span></span>

- <span data-ttu-id="956c0-120">**Office 365에서 권한이 부여 된 액세스 관리를 이미 사용 하 고 있는 동안 Azure AD 권한 id 관리를 사용 하도록 설정:**  office 365의 권한이 부여 된 액세스 관리에 Azure AD 권한 id 관리를 추가 하면 사용자 역할 또는 id로 정의 되는 office 365 외부의 데이터에 대 한 권한 있는 액세스를 확장할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="956c0-120">**Enabling Azure AD Privileged Identity Management while already using privileged access management in Office 365:**  Adding Azure AD Privileged Identity Management to privileged access management in Office 365 can extend privileged access to data outside of Office 365 that’s primarily defined by a user’s role or identity.</span></span>  

## <a name="privileged-access-management-architecture-and-process-flow"></a><span data-ttu-id="956c0-121">권한 있는 액세스 관리 아키텍처 및 프로세스 흐름</span><span class="sxs-lookup"><span data-stu-id="956c0-121">Privileged access management architecture and process flow</span></span>

<span data-ttu-id="956c0-122">다음 각 프로세스는 권한 있는 액세스의 아키텍처와 office 365 기판, office 365 감사 및 Exchange 관리 runspace와 상호 작용 하는 방식을 대략적으로 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="956c0-122">Each of the following process flows outline the architecture of privileged access and how it interacts with the Office 365 substrate, Office 365 auditing, and the Exchange Management runspace.</span></span>

### <a name="step-1-configuring-a-privileged-access-policy"></a><span data-ttu-id="956c0-123">1 단계: 권한이 부여 된 액세스 정책 구성</span><span class="sxs-lookup"><span data-stu-id="956c0-123">Step 1: Configuring a privileged access policy</span></span>

<span data-ttu-id="956c0-124">[Microsoft 365 관리 센터](https://admin.microsoft.com) 또는 Exchange 관리 PowerShell을 사용 하 여 권한 있는 액세스 정책을 구성 하는 경우 정책을 만들고 정의 하며, 권한이 부여 된 액세스 기능은 Office 365 기판의 정책 특성을 처리 하 고 Office 365 보안 및 준수 센터에서 활동을 기록 합니다.</span><span class="sxs-lookup"><span data-stu-id="956c0-124">When configuring a privileged access policy using either the [Microsoft 365 admin center](https://admin.microsoft.com) or Exchange Management PowerShell, you create and define the policy and the privileged access feature processes the policy attributes in the Office 365 substrate and logs the activity in the Office 365 Security and Compliance Center.</span></span> <span data-ttu-id="956c0-125">이제 정책이 사용 하도록 설정 되어 있으며 승인 된 승인을 요청을 처리할 준비가 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="956c0-125">The policy is now enabled and ready to handle incoming requests for approvals.</span></span>

![1 단계-정책 만들기](media/pam-step1-policy-creation.jpg)

### <a name="step-2-access-request"></a><span data-ttu-id="956c0-127">2 단계: 액세스 요청</span><span class="sxs-lookup"><span data-stu-id="956c0-127">Step 2: Access request</span></span>

<span data-ttu-id="956c0-128">사용자는 [Microsoft 365 관리 센터](https://admin.microsoft.com) 또는 Exchange 관리 PowerShell을 사용 하 여 상승 되거나 권한이 부여 된 작업에 대 한 액세스를 요청할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="956c0-128">Using the [Microsoft 365 admin center](https://admin.microsoft.com) or Exchange Management PowerShell, users can request access to elevated or privileged tasks.</span></span> <span data-ttu-id="956c0-129">권한 있는 액세스 기능은 구성 된 권한 액세스 정책에 대 한 처리를 위해 office 365 기판에 요청을 전송 하 고 office 365 보안 및 준수 센터 로그에 해당 활동을 기록 합니다.</span><span class="sxs-lookup"><span data-stu-id="956c0-129">The privileged access feature sends the request to the Office 365 substrate for processing against the configured privilege access policy and records the Activity in the Office 365 Security and Compliance Center logs.</span></span>

![2 단계-액세스 요청](media/pam-step2-access-request.jpg)

### <a name="step-3-access-approval"></a><span data-ttu-id="956c0-131">3 단계: 액세스 승인</span><span class="sxs-lookup"><span data-stu-id="956c0-131">Step 3: Access approval</span></span>

<span data-ttu-id="956c0-132">승인 요청이 생성 되 고, 승인 그룹은 대기 중인 요청의 전자 메일로 알림을 받습니다.</span><span class="sxs-lookup"><span data-stu-id="956c0-132">An approval request is generated and the approval group is notified by email of the pending request.</span></span> <span data-ttu-id="956c0-133">승인이 부여 되 면 권한 있는 액세스 요청이 승인으로 처리 되 고 작업을 완료할 준비가 완료 된 것입니다.</span><span class="sxs-lookup"><span data-stu-id="956c0-133">If approval is granted, the privileged access request is processed as an approval and the task is ready to be completed.</span></span> <span data-ttu-id="956c0-134">요청이 거부 되 면 작업이 차단 되 고 요청자에 게 액세스 권한이 부여 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="956c0-134">If the request is denied, task is blocked and no access is granted to the requestor.</span></span> <span data-ttu-id="956c0-135">요청자에 게는 전자 메일 메시지를 통한 승인 요청 또는 거부 메시지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="956c0-135">The requestor will be notified of the request approval or denial via email message.</span></span>

![3 단계-액세스 승인](media/pam-step3-access-approval.jpg)

### <a name="step-4-access-processing"></a><span data-ttu-id="956c0-137">4 단계: 액세스 처리</span><span class="sxs-lookup"><span data-stu-id="956c0-137">Step 4: Access processing</span></span>

<span data-ttu-id="956c0-138">승인 된 요청의 경우 Exchange 관리 runspace가 작업을 처리 합니다.</span><span class="sxs-lookup"><span data-stu-id="956c0-138">For approved requests, the task is processed by the Exchange Management runspace.</span></span> <span data-ttu-id="956c0-139">승인 된 액세스 정책을 확인 하 고 Office 365 기판에서 처리 합니다.</span><span class="sxs-lookup"><span data-stu-id="956c0-139">The approval is checked against the privileged access policy and processed by the Office 365 substrate.</span></span> <span data-ttu-id="956c0-140">작업에 대 한 모든 활동은 Office 365 보안 및 준수 센터에 기록 됩니다.</span><span class="sxs-lookup"><span data-stu-id="956c0-140">All activity for the task is logged in the Office 365 Security and Compliance Center.</span></span>

![4 단계-액세스 처리](media/pam-step4-access-processing.jpg)

## <a name="frequently-asked-questions"></a><span data-ttu-id="956c0-142">자주하는 질문</span><span class="sxs-lookup"><span data-stu-id="956c0-142">Frequently asked questions</span></span>

### <a name="what-skus-do-i-need-to-use-privileged-access-in-office-365"></a><span data-ttu-id="956c0-143">Office 365에서 권한이 부여 된 access를 사용 하려면 어떤 sku가 필요 한가요?</span><span class="sxs-lookup"><span data-stu-id="956c0-143">What SKUs do I need to use privileged access in Office 365?</span></span>
<span data-ttu-id="956c0-144">권한 있는 액세스 관리는 현재 Office 365 E5 및 고급 규정 준수 sku가 있는 고객 에게만 제공 됩니다.</span><span class="sxs-lookup"><span data-stu-id="956c0-144">Privileged access management is currently only available for customers with Office 365 E5 and Advanced Compliance SKUs.</span></span>

### <a name="when-will-privileged-access-be-available-for-office-365-workloads-beyond-exchange"></a><span data-ttu-id="956c0-145">Exchange 이상에서 Office 365 워크 로드에 대 한 액세스 권한을 언제 사용할 수 있나요?</span><span class="sxs-lookup"><span data-stu-id="956c0-145">When will privileged access be available for Office 365 workloads beyond Exchange?</span></span>
<span data-ttu-id="956c0-146">이 기능은 곧 다른 Office 365 작업에 제공 될 예정입니다.</span><span class="sxs-lookup"><span data-stu-id="956c0-146">We plan to offer this feature in other Office 365 workloads soon.</span></span> <span data-ttu-id="956c0-147">일정을 공유할 준비가 되 면 [Microsoft 365 로드맵을](https://www.microsoft.com/microsoft-365/roadmap)통해 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="956c0-147">When we’re ready to share a timeline, it will be available through the [Microsoft 365 Roadmap](https://www.microsoft.com/microsoft-365/roadmap).</span></span>

### <a name="my-organization-needs-more-than-30-privileged-access-polices-will-this-limit-be-increased"></a><span data-ttu-id="956c0-148">조직에서 사용 하는 액세스 정책이 30 개를 초과 하는 경우이 제한이 증가 하나요?</span><span class="sxs-lookup"><span data-stu-id="956c0-148">My organization needs more than 30 privileged access polices, will this limit be increased?</span></span>

<span data-ttu-id="956c0-149">microsoft는 Office 365 조 직 당 최대 30 개의 권한이 부여 된 액세스 정책에 대 한 현재 제한을 증대 시킬 계획입니다.</span><span class="sxs-lookup"><span data-stu-id="956c0-149">We're planning to increase the current limit of 30 privileged access policies per Office 365 organization soon.</span></span>

### <a name="do-i-need-to-be-a-global-admin-to-manage-privileged-access-in-office-365"></a><span data-ttu-id="956c0-150">Office 365에서 권한이 부여 된 액세스를 관리 하려면 전역 관리자 여야 하나요?</span><span class="sxs-lookup"><span data-stu-id="956c0-150">Do I need to be a Global Admin to manage privileged access in Office 365?</span></span>
<span data-ttu-id="956c0-151">아니요, Office 365에서 권한이 부여 된 액세스를 관리할 계정에 Exchange 역할 관리 역할을 할당 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="956c0-151">No, you need to have the Exchange Role Management role assigned to accounts that will manage privileged access in Office 365.</span></span> <span data-ttu-id="956c0-152">그러나 전역 관리자 역할은 기본적으로이 역할을 포함 하며, 역할 관리 역할을 독립 실행형 계정 권한으로 구성 하지 않으려는 경우에는 권한 있는 액세스를 관리 하는 데 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="956c0-152">However, the Global Administrator role includes this role by default and can be used to manage privileged access if you don’t want to configure the Role Management role as a stand-alone account permission.</span></span> <span data-ttu-id="956c0-153">승인자 그룹에 포함 된 사용자는 전역 관리자 일 필요는 없으며, 요청을 검토 및 승인 하기 위해 역할 관리 역할을 할당할 필요가 없습니다.</span><span class="sxs-lookup"><span data-stu-id="956c0-153">Users who are included in an approvers’ group don't need to be a Global Admin or have the Role Management role assigned to review and approve requests.</span></span>

### <a name="how-is-privileged-access-management-in-office-365-related-to-customer-lockbox"></a><span data-ttu-id="956c0-154">Office 365의 권한이 부여 된 액세스 관리는 어떤 방식으로 고객 Lockbox와 관련 됩니까?</span><span class="sxs-lookup"><span data-stu-id="956c0-154">How is privileged access management in Office 365 related to Customer Lockbox?</span></span>
<span data-ttu-id="956c0-155">[고객 Lockbox](https://docs.microsoft.com/office365/admin/manage/customer-lockbox-requests) 는 조직에 대해 서비스 공급자 (예: Microsoft)가 데이터에 액세스 하는 데 사용할 수 있는 액세스 제어 수준을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="956c0-155">[Customer Lockbox](https://docs.microsoft.com/office365/admin/manage/customer-lockbox-requests) allows a level of access control for organizations for access to to data by their service provider, i.e. Microsoft.</span></span> <span data-ttu-id="956c0-156">office 365의 권한이 부여 된 액세스 관리를 통해 조직 내의 모든 Office 365 권한 작업에 대 한 세부적인 액세스 제어를 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="956c0-156">Privileged access management in Office 365 allows granular access control within an organization for all Office 365 privileged tasks.</span></span>
