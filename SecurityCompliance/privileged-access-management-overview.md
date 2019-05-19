---
title: Office 365의 권한이 부여 된 액세스 관리
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
description: 이 항목을 사용 하 여 Office 365의 권한이 부여 된 액세스 관리에 대해 자세히 알아보세요.
ms.openlocfilehash: 7547568d6ea2a13de5391d5a827df2921833838c
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/17/2019
ms.locfileid: "34157330"
---
# <a name="privileged-access-management-in-office-365"></a>Office 365의 권한이 부여 된 액세스 관리

> [!IMPORTANT]
> 이 항목에서는 현재 Office 365 E5 및 고급 규정 준수 Sku에서 사용할 수 있는 기능에 대 한 배포 및 구성 지침에 대해 설명 합니다.

권한이 부여 된 액세스 관리를 통해 Office 365의 권한 있는 관리 작업을 세부적으로 제어할 수 있습니다. 이는 중요 한 데이터에 대 한 액세스 또는 중요 한 구성 설정에 대 한 액세스 권한이 있는 기존 권한 관리 계정을 사용 하는 행위 로부터 조직을 보호 하는 데 도움이 될 수 있습니다. 권한이 부여 된 액세스 관리를 사용 하려면 사용자가 높은 범위 및 시간 제한 승인 워크플로를 통해 권한 있는 작업을 완료 하기 위해 just-in-time 액세스를 요청 해야 합니다. 이렇게 하면 중요 한 데이터 나 중요 한 구성 설정을 노출 하지 않고 직접 작업을 수행할 수 있는 권한이 사용자에 게 제공 됩니다. Office 365에서 권한이 부여 된 액세스 관리를 사용 하도록 설정 하면 조직에서 단일 권한으로 작동 하 고 단일 관리 액세스 취약성에 대 한 방어 계층을 제공할 수 있습니다.

통합 고객 Lockbox 및 권한이 부여 된 액세스 관리 워크플로에 대 한 간략 한 개요를 보려면 [Office 365 비디오에서이 고객 lockbox 및 권한이 부여 된 액세스 관리](https://go.microsoft.com/fwlink/?linkid=2066800)를 참조 하세요.

## <a name="layers-of-protection"></a>보호 계층

권한이 부여 된 액세스 관리는 Office 365 보안 아키텍처 내에서 다른 데이터 및 액세스 기능 보호를 보완 합니다. 보안에 대 한 통합 및 계층화 방식의 일부로 권한 있는 액세스 관리를 포함 하면 중요 한 정보 및 Office 365 구성 설정의 보호를 최대화 하는 보안 모델을 제공 합니다. 다이어그램에 표시 된 것 처럼, 권한 있는 액세스 관리는 office 365 서비스의 역할 기반 액세스 제어 보안 모델 및 Office 365 데이터에 대 한 기본 암호화와 함께 제공 되는 보호 기능을 기반으로 합니다. 이러한 두 기능은 [AZURE AD 권한이 부여 된 Id 관리](https://docs.microsoft.com/azure/active-directory/active-directory-privileged-identity-management-configure)와 함께 사용 하는 경우 서로 다른 범위의 just-in-time 액세스를 사용 하 여 액세스 제어를 제공 합니다.

![Office 365의 계층화 된 보호 기능](media/pam-layered-protection.png)

Office 365의 권한이 부여 된 액세스 관리는 **작업** 수준에서 정의 되 고 범위가 지정 되는 반면 Azure AD 권한이 부여 된 id 관리는 **역할** 수준의 보호를 여러 작업을 실행 하는 기능과 함께 적용 합니다. Azure AD 권한 있는 Id 관리는 주로 AD 역할 및 역할 그룹에 대 한 액세스 관리를 허용 하지만, Office 365의 권한 있는 액세스 관리는 작업 수준 에서만 적용 됩니다.

- **이미 AZURE AD 권한 Id 관리를 사용 하는 동안 Office 365에서 권한이 부여 된 액세스 관리를 사용 하도록 설정:** Office 365에서 권한이 부여 된 액세스 관리를 추가 하면 Office 365 데이터에 대 한 권한 있는 액세스에 대 한 다양 한 보호 및 감사 기능 계층이 제공 됩니다.

- **Office 365에서 권한이 부여 된 액세스 관리를 이미 사용 하 고 있는 동안 AZURE AD 권한 Id 관리를 사용 하도록 설정:**  Office 365의 권한이 부여 된 액세스 관리에 Azure AD 권한 Id 관리를 추가 하면 사용자 역할 또는 id로 정의 되는 Office 365 외부의 데이터에 대 한 권한 있는 액세스를 확장할 수 있습니다.  

## <a name="privileged-access-management-architecture-and-process-flow"></a>권한 있는 액세스 관리 아키텍처 및 프로세스 흐름

다음 각 프로세스는 권한 있는 액세스의 아키텍처와 Office 365 기판, Office 365 감사 및 Exchange 관리 runspace와 상호 작용 하는 방식을 대략적으로 보여 줍니다.

### <a name="step-1-configure-a-privileged-access-policy"></a>1 단계: 권한이 부여 된 액세스 정책 구성

[Microsoft 365 관리 센터](https://admin.microsoft.com) 또는 Exchange 관리 PowerShell을 사용 하 여 권한 있는 액세스 정책을 구성 하는 경우 정책 및 권한 있는 액세스 기능 프로세스와 Office 365 기판의 정책 특성을 정의 합니다. 이 작업은 Office 365 보안 및 준수 센터에 기록 됩니다. 이제 정책이 사용 하도록 설정 되어 있으며 승인 된 승인을 요청을 처리할 준비가 되었습니다.

![1 단계: 정책 만들기](media/pam-step1-policy-creation.jpg)

### <a name="step-2-access-request"></a>2 단계: 액세스 요청

[Microsoft 365 관리 센터](https://admin.microsoft.com) 또는 Exchange 관리 PowerShell을 사용 하 여 사용자는 상승 되거나 권한 있는 작업에 대 한 액세스를 요청할 수 있습니다. 권한 있는 액세스 기능은 구성 된 권한 액세스 정책에 대 한 처리를 위해 Office 365 기판에 요청을 전송 하 고 Office 365 보안 및 준수 센터 로그에 해당 활동을 기록 합니다.

![2 단계: 액세스 요청](media/pam-step2-access-request.jpg)

### <a name="step-3-access-approval"></a>3 단계: 액세스 승인

승인 요청이 생성 되 고 대기 중인 요청 알림이 승인자에 게 전자 메일로 전송 됩니다. 승인 된 경우 권한 있는 액세스 요청이 승인으로 처리 되 고 작업이 완료 될 준비가 된 것입니다. 거부 되 면 작업이 차단 되 고 해당 요청에 대 한 액세스 권한이 부여 되지 않습니다. 요청자에 게는 전자 메일 메시지를 통한 승인 또는 거부 요청이 통지 됩니다.

![3 단계: 액세스 승인](media/pam-step3-access-approval.jpg)

### <a name="step-4-access-processing"></a>4 단계: 액세스 처리

승인 된 요청의 경우 Exchange 관리 runspace가 작업을 처리 합니다. 승인 된 액세스 정책을 확인 하 고 Office 365 기판에서 처리 합니다. 작업에 대 한 모든 활동은 Office 365 보안 및 준수 센터에 기록 됩니다.

![4 단계: 액세스 처리](media/pam-step4-access-processing.jpg)

## <a name="frequently-asked-questions"></a>자주하는 질문

### <a name="what-skus-can-use-privileged-access-in-office-365"></a>Office 365에서 어떤 Sku가 권한 있는 액세스를 사용할 수 있나요?
Office 365 E5 및 Advanced 준수 Sku가 있는 고객은 권한 있는 액세스 관리를 사용할 수 있습니다.

### <a name="when-will-privileged-access-support-office-365-workloads-beyond-exchange"></a>권한 있는 access가 Exchange 보다 Office 365 워크 로드를 지원 하나요?
권한 있는 액세스 관리는 곧 다른 Office 365 작업에서 사용할 수 있습니다. 자세한 내용은 [Microsoft 365 로드맵](https://www.microsoft.com/microsoft-365/roadmap) 를 방문 하세요.

### <a name="my-organization-needs-more-than-30-privileged-access-policies-will-this-limit-be-increased"></a>조직에서 사용 하는 액세스 정책이 30 개를 초과 하는 경우이 제한이 증가 하나요?
예, Office 365 조 직 당 권한 있는 액세스 정책 30 개를 최신으로 올리는 기능이 기능 로드맵에 있습니다.

### <a name="do-i-need-to-be-a-global-admin-to-manage-privileged-access-in-office-365"></a>Office 365에서 권한이 부여 된 액세스를 관리 하려면 전역 관리자 여야 하나요?
아니요, Office 365에서 권한이 부여 된 액세스를 관리 하는 계정에 할당 된 Exchange 역할 관리 역할이 필요 합니다. 역할 관리 역할을 독립 실행형 계정 권한으로 구성 하지 않을 경우 전역 관리자 역할에는 기본적으로이 역할이 포함 되며 권한이 부여 된 액세스를 관리할 수 있습니다. 승인자 그룹에 포함 된 사용자는 전역 관리자가 아니어도 되 고 요청을 검토 및 승인 하기 위해 역할 관리 역할을 할당할 필요가 없습니다.

### <a name="how-is-privileged-access-management-in-office-365-related-to-customer-lockbox"></a>Office 365의 권한이 부여 된 액세스 관리는 어떤 방식으로 고객 Lockbox와 관련 됩니까?
[고객 Lockbox](https://docs.microsoft.com/office365/admin/manage/customer-lockbox-requests) 는 Microsoft가 데이터에 액세스할 때 조직에 대 한 액세스 제어 수준을 허용 합니다. Office 365의 권한이 부여 된 액세스 관리를 통해 조직 내의 모든 Office 365 권한 작업에 대 한 세부적인 액세스 제어를 허용 합니다.

## <a name="ready-to-get-started"></a>시작할 준비가 되셨습니까?

[권한 있는 액세스 관리를 위한 조직 구성을](privileged-access-management-configuration.md)시작 합니다.

## <a name="learn-more"></a>자세한 정보

[대화형 가이드: 권한이 부여 된 액세스 관리로 관리자 작업 모니터링 및 제어](https://content.cloudguides.com/en-us/guides/Privileged%20Access%20Management)