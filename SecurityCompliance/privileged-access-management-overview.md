---
title: Office 365의에서 관리 기능에 액세스 권한
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
description: 이 항목을 사용 하 여 권한 하는 방법에 대 한 자세한 내용은 Office 365의에서 관리 기능에 액세스
ms.openlocfilehash: 5056c19acb03b2486cc84fe085ffd6c2814007dc
ms.sourcegitcommit: a07b91723bae9ecee2cb092bfbc5b208b30b11a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/25/2018
ms.locfileid: "25793553"
---
# <a name="privileged-access-management-in-office-365"></a><span data-ttu-id="8aef8-103">Office 365의에서 관리 기능에 액세스 권한</span><span class="sxs-lookup"><span data-stu-id="8aef8-103">Privileged access management in Office 365</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8aef8-104">이 항목에서는 Office 365 e 5 및 고급 준수 Sku에만 현재 제공 되는 기능에 대 한 배포 및 구성 지침에 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="8aef8-104">This topic covers deployment and configuration guidance for features only currently available in Office 365 E5 and Advanced Compliance SKUs.</span></span>

<span data-ttu-id="8aef8-p101">액세스 권한 관리 Office 365에서 권한이 부여 된 관리 작업을 통해 세분화 된 액세스 제어를 허용 합니다.  기존 관리자가 권한이 부여 된 사용자 계정은 중요 한 데이터에 대 한 순위 액세스 또는 중요 한 구성 설정에 대 한 액세스를 사용할 수 있는 침해에서 조직을 보호 하는 것이 도움이 됩니다. 권한이 부여 된 액세스 관리를 사용 하도록 설정한 후 사용자가 높은 범위가 지정 되며 시간 제한이 있는 승인 워크플로 통해 관리자 권한 및 권한 있는 작업을 완료 하려면 적시에 액세스를 요청 해야 합니다. 이 사용자가 액세스할 수 방금-만큼 충분히-중요 한 데이터 나 중요 한 구성 설정의 노출 시 키 지 않고, 수행 중인 작업을 수행할 수 있습니다. Office 365에서 권한이 부여 된 액세스 관리를 사용 하도록 설정 하면 조직 0 순위 권한으로 작동 하 고 이러한 순위 관리 액세스로 인해 발생 하는 취약점에 대 한 방어 계층을 제공할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8aef8-p101">Privileged access management allows granular access control over privileged admin tasks in Office 365.  It can help protect your organization from breaches that may use existing privileged admin accounts with standing access to sensitive data or access to critical configuration settings. After enabling privileged access management, users will need to request just-in-time access to complete elevated and privileged tasks through an approval workflow that is highly scoped and time-bound. This gives users just-enough-access to perform the task at hand, without risking exposure of sensitive data or critical configuration settings. Enabling privileged access management in Office 365 will enable your organization to operate with zero standing privileges and provide a layer of defense against vulnerabilities arising because of such standing administrative access.</span></span> 

## <a name="layers-of-protection"></a><span data-ttu-id="8aef8-110">보호의 레이어</span><span class="sxs-lookup"><span data-stu-id="8aef8-110">Layers of protection</span></span>

<span data-ttu-id="8aef8-p102">액세스 권한이 부여 된 관리는 Office 365 보안 아키텍처 내의 다른 데이터 및 액세스 기능 보호를 보완 합니다. 보안에는 통합 된 접근 방법의 일부로 권한이 부여 된 액세스 관리를 사용 하도록 설정 하 고 조직 보호를 계층화 된 보안 모델의 중요 한 정보 및 Office 365 구성 설정을 보호 최대화 하기 위해 사용할 수 있습니다. 표시 된 것 처럼 수 있도록 아래 다이어그램에 권한이 부여 된 액세스 관리를 통해 Office 365 데이터의 기본 암호화 및 Office 365 서비스의 역할 기반 액세스 제어 보안 모델 제공 하는 보호에 작성 합니다. [Azure AD 권한 있는 Id 관리](https://docs.microsoft.com/azure/active-directory/active-directory-privileged-identity-management-configure)와 함께 사용 하면 이러한 두 기능은 다양 한 범위에서 적시에 액세스할 수 있는 액세스 제어를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="8aef8-p102">Privileged access management complements other data and access feature protections within the Office 365 security architecture. By enabling privileged access management as part of an integrated approach to security and protecting your organization, a layered security model can be used to maximize protection of sensitive information and Office 365 configuration settings. As shown in the diagram below, enabling privileged access management helps builds on the protection provided with native encryption of Office 365 data and the role based access control security model of Office 365 services. When used in conjunction with [Azure AD Privileged Identity Management](https://docs.microsoft.com/azure/active-directory/active-directory-privileged-identity-management-configure), these two features provide access control with just-in-time access at different scopes.</span></span>

![Office 365의 계층화 된 보호](media/pam-layered-protection.png)

<span data-ttu-id="8aef8-p103">액세스 권한이 부여 된 Office 365의 관리를 정의 하 고 여러 작업을 실행 하는 기능 **역할** 수준에서 보호를 적용 하는 Azure AD 권한 있는 Id 관리 하는 동안 **작업** 수준으로 범위가 지정 수 있습니다.  Office 365의 관리 작업 수준 에서만 적용 권한에 액세스 하는 동안를 azure AD 권한 Id 관리 주로 AD 역할과 역할 그룹에 대 한 액세스를 관리할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8aef8-p103">Privileged access management in Office 365 can be defined and scoped at the **task** level, while Azure AD Privileged Identity Management applies protection at the **role** level with the ability to execute multiple tasks.  Azure AD Privileged Identity Management primarily allows managing accesses for AD roles and role groups, while privileged access management in Office 365 is applied only at the task level.</span></span>

- <span data-ttu-id="8aef8-118">**이미 Azure AD 권한 있는 Id 관리를 사용 하는 동안 Office 365의에서 관리 기능에 대 한 사용 권한 액세스:** Office 365에서 액세스 권한을된 관리 추가 (영문) 다른 세분화 된 계층 Office 365 데이터에 대 한 권한이 부여 된 액세스에 대 한 보호 및 감사 기능을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="8aef8-118">**Enabling privileged access management in Office 365 while already using Azure AD Privileged Identity Management:** Adding privileged access management in Office 365 provides another granular layer of protection and audit capabilities for privileged access to Office 365 data.</span></span>

- <span data-ttu-id="8aef8-119">**이미 사용 하는 동안 Id 관리를 사용 하도록 설정 Azure AD 권한 있는 사용자는 Office 365에 대 한 액세스 관리 권한이:**  Azure AD 권한 있는 Id 관리 권한 추가 Office 365에서 액세스 관리는 주로 사용자의 역할 또는 id에 의해 정의 된 Office 365의 외부 데이터에 대 한 액세스 권한을된를 확장할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8aef8-119">**Enabling Azure AD Privileged Identity Management while already using privileged access management in Office 365:**  Adding Azure AD Privileged Identity Management to privileged access management in Office 365 can extend privileged access to data outside of Office 365 that’s primarily defined by a user’s role or identity.</span></span>  

## <a name="privileged-access-management-architecture-and-process-flow"></a><span data-ttu-id="8aef8-120">액세스 권한을된 관리 아키텍처 및 프로세스 흐름</span><span class="sxs-lookup"><span data-stu-id="8aef8-120">Privileged access management architecture and process flow</span></span>

<span data-ttu-id="8aef8-121">다음 프로세스 흐름의 각 아키텍처 priveleged 액세스와 Office 365 substrate, Office 365 감사 및 Exchange 관리 실행과 상호작용 하는 방법을 간략하게 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="8aef8-121">Each of the following process flows outline the architecture of priveleged access and how it interacts with the Office 365 substrate, Office 365 auditing, and the Exchange Management runspace.</span></span>

### <a name="step-1-configuring-a-privileged-access-policy"></a><span data-ttu-id="8aef8-122">1 단계: 권한이 부여 된 액세스 정책 구성</span><span class="sxs-lookup"><span data-stu-id="8aef8-122">Step 1: Configuring a privileged access policy</span></span>

<span data-ttu-id="8aef8-p104">Office 365 substrate 및 로그에서 정책 특성을 처리 하는 액세스 권한을된 기능 및 Office 365 관리 센터 또는 Exchange 관리 PowerShell을 사용 하 여 권한이 부여 된 액세스 정책을 구성할 때 만들고 정책을 정의 하 여는 Office 365 보안 및 규정 준수 센터의 활동입니다. 정책을 이제이 활성화 하 고 승인에 대 한 들어오는 요청을 처리할 준비가 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="8aef8-p104">When configuring a privileged access policy using either the Office 365 Admin Center or Exchange Management PowerShell, you create and define the policy and the privileged access feature processes the policy attributes in the Office 365 substrate and logs the activity in the Office 365 Security and Compliance Center. The policy is now enabled and ready to handle incoming requests for approvals.</span></span>

![1 단계-정책 만들기](media/pam-step1-policy-creation.jpg)

### <a name="step-2-access-request"></a><span data-ttu-id="8aef8-126">2 단계: 액세스 요청</span><span class="sxs-lookup"><span data-stu-id="8aef8-126">Step 2: Access request</span></span>

<span data-ttu-id="8aef8-p105">Office 365 관리 센터 또는 Exchange 관리 PowerShell을 사용 하 여, 사용자가 상승 된 권한 또는 권한 있는 작업에 대 한 액세스를 요청할 수 있습니다. 권한이 부여 된 액세스 기능이 구성 된 권한 액세스 정책에 대 한 처리를 위해 Office 365 substrate에 요청을 보내고 Office 365 보안에는 sctivity를 기록 하 고 준수 센터 기록 합니다.</span><span class="sxs-lookup"><span data-stu-id="8aef8-p105">Using the Office 365 Admin Center or Exchange Management PowerShell, users can request access to elevated or privileged tasks. The privileged access feature sends the request to the Office 365 substrate for processing against the configured privilege access policy and records the sctivity in the Office 365 Security and Compliance Center logs.</span></span>

![단계 2-액세스 요청](media/pam-step2-access-request.jpg)

### <a name="step-3-access-approval"></a><span data-ttu-id="8aef8-130">3 단계: 액세스 승인</span><span class="sxs-lookup"><span data-stu-id="8aef8-130">Step 3: Access approval</span></span>

<span data-ttu-id="8aef8-p106">승인 요청을 생성 하 고 승인 그룹 대기 중인 요청을 전자 메일로 알립니다. 승인 부여 되 면 액세스 권한이 부여 된 요청이 승인으로 처리 되 하 고 작업을 완료 하도록 준비가 되었습니다. 요청이 거부 되 면 작업은 차단 하 고 액세스할 수 없습니다는 reqeustor에 부여 됩니다. 검토자가 요청자의 요청 승인 또는 거부 전자 메일 메시지를 통해 알림을 받게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8aef8-p106">An approval request is generated and the approval group is notified by email of the pending request. If approval is granted, the privileged access request is processed as an approval and the task is ready to be completed. If the request is denied, task is block and no access is granted to the reqeustor. The requestor will be notified of the request approval or denial via email message.</span></span>

![단계 3-액세스 승인](media/pam-step3-access-approval.jpg)

### <a name="step-4-access-processing"></a><span data-ttu-id="8aef8-136">4 단계: 액세스 처리</span><span class="sxs-lookup"><span data-stu-id="8aef8-136">Step 4: Access processing</span></span>

<span data-ttu-id="8aef8-p107">승인 된 요청에 대 한 Exchange 관리 실행 하 여 작업 처리 됩니다. 승인 하는 권한이 부여 된 액세스 정책에 대해 확인 이며 Office 365 substrate에 의해 처리 됩니다. Office 365 보안 및 규정 준수 센터의 작업에 대 한 모든 작업 기록 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8aef8-p107">For approved requests, the task is processed by the Exchange Management runspace. The approval is checked against the privileged access policy and processed by the Office 365 substrate. All activity for the task is logged in the Office 365 Security and Compliance Center.</span></span>

![단계 4-액세스 처리](media/pam-step4-access-processing.jpg)

## <a name="frequently-asked-questions"></a><span data-ttu-id="8aef8-141">자주 묻는 질문</span><span class="sxs-lookup"><span data-stu-id="8aef8-141">Frequently asked questions</span></span>

### <a name="what-skus-do-i-need-to-use-privileged-access-in-office-365"></a><span data-ttu-id="8aef8-142">Office 365에서 권한이 부여 된 액세스를 사용 하 여 어떤 Sku를 필요 합니까?</span><span class="sxs-lookup"><span data-stu-id="8aef8-142">What SKUs do I need to use privileged access in Office 365?</span></span>
<span data-ttu-id="8aef8-143">액세스 권한이 부여 된 현재 관리는 Office 365 e 5 및 고급 준수 Sku와 고객을 위해 사용할 수만 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8aef8-143">Privileged access management is currently only available for customers with Office 365 E5 and Advanced Compliance SKUs.</span></span>

### <a name="when-will-privileged-access-be-available-for-office-365-workloads-beyond-exchange"></a><span data-ttu-id="8aef8-144">액세스 권한을된 사용할 수 있게 될 Exchange 이외 Office 365 작업 부하에 대 한?</span><span class="sxs-lookup"><span data-stu-id="8aef8-144">When will privileged access be available for Office 365 workloads beyond Exchange?</span></span>
<span data-ttu-id="8aef8-p108">다른 Office 365 작업에서이 기능을 곧 제공 예정입니다. 시간 표시 막대를 공유할 준비가 되었습니다, Office 365 로드맵을 통해 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8aef8-p108">We plan to offer this feature in other Office 365 workloads soon. When we’re ready to share a timeline, it will be available through the Office 365 roadmap.</span></span>

### <a name="my-organization-needs-more-than-30-privileged-access-polices-will-this-limit-be-increased"></a><span data-ttu-id="8aef8-147">내 조직 요구 사항 둘 이상의 30 권한이 부여 된 액세스 정책,이 한도 증가 합니까?</span><span class="sxs-lookup"><span data-stu-id="8aef8-147">My organization needs more than 30 privileged access polices, will this limit be increased?</span></span>

<span data-ttu-id="8aef8-148">Office 365 조직 곧 당 30 권한이 부여 된 액세스 정책의 현재 한계를 늘리려면 계획 합니다.</span><span class="sxs-lookup"><span data-stu-id="8aef8-148">We're planning to increase the current limit of 30 privileged access policies per Office 365 organization soon.</span></span>

### <a name="do-i-need-to-be-a-global-admin-to-manage-privileged-access-in-office-365"></a><span data-ttu-id="8aef8-149">Office 365에 대 한 액세스 권한을된 관리 하는 전역 관리자 되도록 필요 합니까?</span><span class="sxs-lookup"><span data-stu-id="8aef8-149">Do I need to be a Global Admin to manage privileged access in Office 365?</span></span>
<span data-ttu-id="8aef8-p109">아니요, Office 365에 대 한 액세스 권한을된 관리 하는 계정에 할당 된 Exchange 역할 관리 역할을 해야 합니다. 그러나 전역 관리자 역할 기본적으로이 역할을 포함 하 고는 독립 실행형 계정 사용 권한으로 역할 관리 역할을 구성 하지 않을 경우 권한이 부여 된 액세스를 관리 하는데 사용할 수 있습니다. 승인자의 그룹에 포함 된 사용자는 전역 관리자 이거나 요청 검토 및 승인에 할당 된 역할 관리 역할을 가질 필요가 없습니다.</span><span class="sxs-lookup"><span data-stu-id="8aef8-p109">No, you need to have the Exchange Role Management role assigned to accounts that will manage privileged access in Office 365. However, the Global Administrator role includes this role by default and can be used to manage privileged access if you don’t want to configure the Role Management role as a stand-alone account permission. Users who are included in an approvers’ group don't need to be a Global Admin or have the Role Management role assigned to review and approve requests.</span></span> 

### <a name="how-is-privileged-access-management-in-office-365-related-to-customer-lockbox"></a><span data-ttu-id="8aef8-153">Office 365와 관련 된 고객 Lockbox에서에서 액세스 권한을된 관리는 어떻게 합니까?</span><span class="sxs-lookup"><span data-stu-id="8aef8-153">How is privileged access management in Office 365 related to Customer Lockbox?</span></span>
<span data-ttu-id="8aef8-p110">[고객 Lockbox](https://support.office.com/article/Office-365-Customer-Lockbox-Requests-36f9cdd1-e64c-421b-a7e4-4a54d16440a2) 서비스 공급자, 즉, Microsoft가 데이터에 대 한 액세스에 대 한 조직에 대 한 액세스 제어의 수준 수 있습니다. 액세스 권한이 부여 된 Office 365의 관리는 모든 Office 365의 권한 있는 작업에 대 한 조직 내에서 세분화 된 액세스 제어를 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="8aef8-p110">[Customer Lockbox](https://support.office.com/article/Office-365-Customer-Lockbox-Requests-36f9cdd1-e64c-421b-a7e4-4a54d16440a2) allows a level of access control for organizations for access to to data by their service provider, i.e. Microsoft. Privileged access management in Office 365 allows granular access control within an organization for all Office 365 privileged tasks.</span></span>