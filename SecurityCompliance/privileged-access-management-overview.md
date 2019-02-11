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
ms.openlocfilehash: 85141ae885132095692683b766d5550cc538e2e8
ms.sourcegitcommit: 7e2a0185cadea7f3a6afc5ddc445eac2e1ce22eb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/11/2019
ms.locfileid: "29652263"
---
# <a name="privileged-access-management-in-office-365"></a>Office 365의에서 관리 기능에 액세스 권한

> [!IMPORTANT]
> 이 항목에서는 Office 365 e 5 및 고급 준수 Sku에만 현재 제공 되는 기능에 대 한 배포 및 구성 지침에 설명 합니다.

액세스 권한 관리 Office 365에서 권한이 부여 된 관리 작업을 통해 세분화 된 액세스 제어를 허용 합니다. 기존 관리자가 권한이 부여 된 사용자 계정은 중요 한 데이터에 대 한 순위 액세스 또는 중요 한 구성 설정에 대 한 액세스를 사용할 수 있는 침해에서 조직을 보호 하는 것이 도움이 됩니다. 권한이 부여 된 액세스 관리를 사용 하도록 설정한 후 사용자가 높은 범위가 지정 되며 시간 제한이 있는 승인 워크플로 통해 관리자 권한 및 권한 있는 작업을 완료 하려면 적시에 액세스를 요청 해야 합니다. 이 사용자가 액세스할 수 방금-만큼 충분히-중요 한 데이터 나 중요 한 구성 설정의 노출 시 키 지 않고, 수행 중인 작업을 수행할 수 있습니다. Office 365에서 권한이 부여 된 액세스 관리를 사용 하도록 설정 하면 조직 0 순위 권한으로 작동 하 고 이러한 순위 관리 액세스로 인해 발생 하는 취약점에 대 한 방어 계층을 제공할 수 있습니다.

통합 된 고객 Lockbox 및 액세스 권한을된 관리-종단간 워크플로 빠른 개요를이 [고객 Lockbox 및 Office 365 비디오에서 권한이 부여 된 액세스 관리를](https://go.microsoft.com/fwlink/?linkid=2066800)참조 하십시오.

## <a name="layers-of-protection"></a>보호의 레이어

액세스 권한이 부여 된 관리는 Office 365 보안 아키텍처 내의 다른 데이터 및 액세스 기능 보호를 보완 합니다. 보안에는 통합 된 접근 방법의 일부로 권한이 부여 된 액세스 관리를 사용 하도록 설정 하 고 조직 보호를 계층화 된 보안 모델의 중요 한 정보 및 Office 365 구성 설정을 보호 최대화 하기 위해 사용할 수 있습니다. 표시 된 것 처럼 수 있도록 아래 다이어그램에 권한이 부여 된 액세스 관리를 통해 Office 365 데이터의 기본 암호화 및 Office 365 서비스의 역할 기반 액세스 제어 보안 모델 제공 하는 보호에 작성 합니다. [Azure AD 권한 있는 Id 관리](https://docs.microsoft.com/azure/active-directory/active-directory-privileged-identity-management-configure)와 함께 사용 하면 이러한 두 기능은 다양 한 범위에서 적시에 액세스할 수 있는 액세스 제어를 제공 합니다.

![Office 365의 계층화 된 보호](media/pam-layered-protection.png)

액세스 권한이 부여 된 Office 365의 관리를 정의 하 고 여러 작업을 실행 하는 기능 **역할** 수준에서 보호를 적용 하는 Azure AD 권한 있는 Id 관리 하는 동안 **작업** 수준으로 범위가 지정 수 있습니다.  Office 365의 관리 작업 수준 에서만 적용 권한에 액세스 하는 동안를 azure AD 권한 Id 관리 주로 AD 역할과 역할 그룹에 대 한 액세스를 관리할 수 있습니다.

- **이미 Azure AD 권한 있는 Id 관리를 사용 하는 동안 Office 365의에서 관리 기능에 대 한 사용 권한 액세스:** Office 365에서 액세스 권한을된 관리 추가 (영문) 다른 세분화 된 계층 Office 365 데이터에 대 한 권한이 부여 된 액세스에 대 한 보호 및 감사 기능을 제공 합니다.

- **이미 사용 하는 동안 Id 관리를 사용 하도록 설정 Azure AD 권한 있는 사용자는 Office 365에 대 한 액세스 관리 권한이:**  Azure AD 권한 있는 Id 관리 권한 추가 Office 365에서 액세스 관리는 주로 사용자의 역할 또는 id에 의해 정의 된 Office 365의 외부 데이터에 대 한 액세스 권한을된를 확장할 수 있습니다.  

## <a name="privileged-access-management-architecture-and-process-flow"></a>액세스 권한을된 관리 아키텍처 및 프로세스 흐름

다음 프로세스 흐름의 각 아키텍처 priveleged 액세스와 Office 365 substrate, Office 365 감사 및 Exchange 관리 실행과 상호작용 하는 방법을 간략하게 설명 합니다.

### <a name="step-1-configuring-a-privileged-access-policy"></a>1 단계: 권한이 부여 된 액세스 정책 구성

Office 365 substrate 및 로그에서 정책 특성을 처리 하는 액세스 권한을된 기능 및 Office 365 관리 센터 또는 Exchange 관리 PowerShell을 사용 하 여 권한이 부여 된 액세스 정책을 구성할 때 만들고 정책을 정의 하 여는 Office 365 보안 및 규정 준수 센터의 활동입니다. 정책을 이제이 활성화 하 고 승인에 대 한 들어오는 요청을 처리할 준비가 되었습니다.

![1 단계-정책 만들기](media/pam-step1-policy-creation.jpg)

### <a name="step-2-access-request"></a>2 단계: 액세스 요청

Office 365 관리 센터 또는 Exchange 관리 PowerShell을 사용 하 여, 사용자가 상승 된 권한 또는 권한 있는 작업에 대 한 액세스를 요청할 수 있습니다. 권한이 부여 된 액세스 기능이 구성 된 권한 액세스 정책에 대 한 처리를 위해 Office 365 substrate에 요청을 보내고 Office 365 보안에는 sctivity를 기록 하 고 준수 센터 기록 합니다.

![단계 2-액세스 요청](media/pam-step2-access-request.jpg)

### <a name="step-3-access-approval"></a>3 단계: 액세스 승인

승인 요청을 생성 하 고 승인 그룹 대기 중인 요청을 전자 메일로 알립니다. 승인 부여 되 면 액세스 권한이 부여 된 요청이 승인으로 처리 되 하 고 작업을 완료 하도록 준비가 되었습니다. 요청이 거부 되 면 작업은 차단 하 고 액세스할 수 없습니다는 reqeustor에 부여 됩니다. 검토자가 요청자의 요청 승인 또는 거부 전자 메일 메시지를 통해 알림을 받게 됩니다.

![단계 3-액세스 승인](media/pam-step3-access-approval.jpg)

### <a name="step-4-access-processing"></a>4 단계: 액세스 처리

승인 된 요청에 대 한 Exchange 관리 실행 하 여 작업 처리 됩니다. 승인 하는 권한이 부여 된 액세스 정책에 대해 확인 이며 Office 365 substrate에 의해 처리 됩니다. Office 365 보안 및 규정 준수 센터의 작업에 대 한 모든 작업 기록 됩니다.

![단계 4-액세스 처리](media/pam-step4-access-processing.jpg)

## <a name="frequently-asked-questions"></a>자주하는 질문

### <a name="what-skus-do-i-need-to-use-privileged-access-in-office-365"></a>Office 365에서 권한이 부여 된 액세스를 사용 하 여 어떤 Sku를 필요 합니까?
액세스 권한이 부여 된 현재 관리는 Office 365 e 5 및 고급 준수 Sku와 고객을 위해 사용할 수만 있습니다.

### <a name="when-will-privileged-access-be-available-for-office-365-workloads-beyond-exchange"></a>액세스 권한을된 사용할 수 있게 될 Exchange 이외 Office 365 작업 부하에 대 한?
다른 Office 365 작업에서이 기능을 곧 제공 예정입니다. 시간 표시 막대를 공유할 준비가 되었습니다, [Microsoft 365 로드맵](https://www.microsoft.com/microsoft-365/roadmap)을 통해 사용할 수 있습니다.

### <a name="my-organization-needs-more-than-30-privileged-access-polices-will-this-limit-be-increased"></a>내 조직 요구 사항 둘 이상의 30 권한이 부여 된 액세스 정책,이 한도 증가 합니까?

Office 365 조직 곧 당 30 권한이 부여 된 액세스 정책의 현재 한계를 늘리려면 계획 합니다.

### <a name="do-i-need-to-be-a-global-admin-to-manage-privileged-access-in-office-365"></a>Office 365에 대 한 액세스 권한을된 관리 하는 전역 관리자 되도록 필요 합니까?
아니요, Office 365에 대 한 액세스 권한을된 관리 하는 계정에 할당 된 Exchange 역할 관리 역할을 해야 합니다. 그러나 전역 관리자 역할 기본적으로이 역할을 포함 하 고는 독립 실행형 계정 사용 권한으로 역할 관리 역할을 구성 하지 않을 경우 권한이 부여 된 액세스를 관리 하는데 사용할 수 있습니다. 승인자의 그룹에 포함 된 사용자는 전역 관리자 이거나 요청 검토 및 승인에 할당 된 역할 관리 역할을 가질 필요가 없습니다. 

### <a name="how-is-privileged-access-management-in-office-365-related-to-customer-lockbox"></a>Office 365와 관련 된 고객 Lockbox에서에서 액세스 권한을된 관리는 어떻게 합니까?
[고객 Lockbox](https://docs.microsoft.com/office365/admin/manage/customer-lockbox-requests) 서비스 공급자, 즉, Microsoft가 데이터에 대 한 액세스에 대 한 조직에 대 한 액세스 제어의 수준 수 있습니다. 액세스 권한이 부여 된 Office 365의 관리는 모든 Office 365의 권한 있는 작업에 대 한 조직 내에서 세분화 된 액세스 제어를 허용 합니다.
