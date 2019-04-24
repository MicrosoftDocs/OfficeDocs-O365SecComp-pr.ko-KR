---
title: Office 365에서 권한이 부여 된 액세스 관리 구성
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
description: 이 항목을 사용 하 여 Office 365에서 권한이 부여 된 액세스 관리 구성에 대 한 자세한 내용을 알아보세요.
ms.openlocfilehash: e086e93c268fe4de627bef30d3ac7aed8e6b1f98
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32265240"
---
# <a name="configuring-privileged-access-management-in-office-365"></a>Office 365에서 권한이 부여 된 액세스 관리 구성

> [!IMPORTANT]
> 이 항목에서는 현재 Office 365 E5 및 고급 규정 준수 sku에서 사용할 수 있는 기능에 대 한 배포 및 구성 지침에 대해 설명 합니다.

이 항목에서는 Office 365 조직에서 권한이 부여 된 액세스 관리를 사용 하도록 설정 하 고 구성 하는 과정을 안내 합니다. Microsoft 365 관리 센터 또는 Exchange 관리 PowerShell을 사용 하 여 권한 있는 액세스를 관리 하 고 사용할 수 있습니다. 

## <a name="enable-and-configure-privileged-access-management"></a>권한 있는 액세스 관리 사용 및 구성

Office 365 조직에서 권한 있는 액세스를 설정 및 사용 하려면 다음 단계를 수행 합니다.

- [1 단계: 승인자 그룹 만들기](privileged-access-management-configuration.md#step1)

    권한 액세스 사용을 시작 하기 전에 관리자 권한 및 권한 있는 작업에 대 한 들어오는 요청 액세스에 대 한 승인 권한이 필요한 사람을 결정 합니다. 승인자 그룹에 속하는 모든 사용자는 액세스 요청을 승인할 수 있습니다. 이 기능은 Office 365에서 메일 사용이 가능한 보안 그룹을 만들어 사용할 수 있습니다.

- [2 단계: 권한 있는 액세스 사용](privileged-access-management-configuration.md#step2)

    권한 있는 액세스 관리 액세스 제어에서 제외 하려는 시스템 계정 집합을 비롯 하 여 Office 365에서 기본 승인자 그룹을 사용 하 여 권한이 부여 된 access를 명시적으로 사용 하도록 설정 해야 합니다.

- [3 단계: 액세스 정책 만들기](privileged-access-management-configuration.md#step3)

    승인 정책을 만들면 개별 작업에서 범위가 지정 되는 특정 승인 요구 사항을 정의할 수 있습니다. 승인 유형 옵션은 **자동** 또는 **수동**입니다.

- [4 단계: 권한 있는 액세스 요청 제출/승인](privileged-access-management-configuration.md#step4)

    권한 있는 액세스를 사용 하도록 설정 하 고 나면 연결 된 승인 정책이 정의 된 모든 작업에 대 한 승인이 필요 합니다. 승인 정책에 포함 된 작업의 경우 사용자는 작업을 실행 하는 데 필요한 권한을 요청 하 고 액세스 승인을 받아야 합니다.

승인을 받은 후에는 요청 하는 사용자가 원하는 작업을 실행할 수 있으며, 권한이 부여 된 access에서는 사용자를 대신 하 여 작업을 승인 하 고 실행 합니다. 요청 된 기간 (기본 기간: 4 시간)에 대 한 승인은 유효한 상태로 유지 되므로 요청 자가 원하는 작업을 여러 번 실행할 수 있습니다. 이러한 모든 실행이 기록 되 고 보안 및 준수 감사를 위해 사용할 수 있게 됩니다. 

> [!NOTE]
> exchange 관리 powershell을 사용 하 여 권한 있는 액세스를 사용 하도록 설정 하 고 구성 하려면 [다단계 인증을 사용 하 여 exchange online powershell에 연결](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/mfa-connect-to-exchange-online-powershell?view=exchange-ps) 의 단계를 수행 하 여 Office 365와 함께 exchange online powershell에 연결 합니다. 증명. Office 365 조 직에 대해 Exchange Online PowerShell에 연결 하는 동안 권한 있는 액세스를 사용 하도록 설정 하는 단계를 사용 하기 위해 multi-factor authentication을 사용 하도록 설정할 필요는 없습니다. 다단계 인증을 사용 하 여 연결-요청에 서명 하기 위해 특권 수준의 액세스에서 사용 되는 OAuth 토큰을 만듭니다.

<a name="step1"> </a>

## <a name="step-1-create-an-approvers-group"></a>1 단계: 승인자 그룹 만들기

1. 조직의 관리자 계정에 대 한 자격 증명을 사용 하 여 [Microsoft 365 관리 센터](https://admin.microsoft.com) 에 로그인 합니다.

2. 관리 센터에서 그룹으로 이동 **** > 하 여**그룹을 추가**합니다.

3. **메일 사용이 가능한 보안 그룹** 을 선택 하 고 새 그룹에 대 한 **이름**, **그룹 전자 메일 주소**및 **설명** 필드를 입력 합니다.

4. 그룹을 저장 합니다. 그룹을 완전히 구성 하 고 Microsoft 365 관리 센터에 표시 하는 데 몇 분 정도 걸릴 수 있습니다.

5. 새 승인자의 그룹을 선택 하 고 **편집** 을 선택 하 여 그룹에 사용자를 추가 합니다.

6. 그룹을 저장 합니다.

<a name="step2"> </a>

## <a name="step-2-enable-privileged-access"></a>2 단계: 권한 있는 액세스 사용

### <a name="in-the-microsoft-365-admin-center"></a>Microsoft 365 관리 센터에서

1. 조직의 관리자 계정에 대 한 자격 증명을 사용 하 여 [Microsoft 365 관리 센터](https://admin.microsoft.com) 에 로그인 합니다.

2. 관리 센터에서 **Settings > Security & 개인 정보** > **권한 액세스**로 이동 합니다.

3. 권한 있는 **액세스 제어에 대 한 승인 필요** 를 사용 하도록 설정 합니다.

4. 1 단계에서 만든 승인자 그룹을 **기본 승인자 그룹**으로 지정 합니다.

5. **저장** 하 고 **닫습니다**.

### <a name="in-exchange-management-powershell"></a>Exchange 관리 PowerShell에서

권한 있는 액세스를 사용 하도록 설정 하 고 승인자의 그룹을 할당 하려면 Exchange Online PowerShell에서 다음 명령을 실행 합니다.
```
Enable-ElevatedAccessControl -AdminGroup '<default approver group>' -SystemAccounts @('<systemAccountUPN1>','<systemAccountUPN2>')
```
예제:
```
Enable-ElevatedAccessControl -AdminGroup 'pamapprovers@fabrikam.onmicrosoft.com' -SystemAccounts @('sys1@fabrikamorg.onmicrosoft.com', sys2@fabrikamorg.onmicrosoft.com')
```

> [!NOTE]
> 시스템 계정 기능을 사용 하 여 조직 내의 특정 자동화 기능이 권한 있는 액세스에 대 한 종속성 없이 작동할 수 있지만, 이러한 제외가 예외적인 경우에도 허용 되며 승인 되 고 감사 되도록 하는 것이 권장 됩니다. 자주.

<a name="step3"> </a>

## <a name="step-3-create-an-access-policy"></a>3 단계: 액세스 정책 만들기

Office 365 조 직에 대해 최대 30 개의 권한이 부여 된 액세스 정책을 만들고 구성할 수 있습니다.

### <a name="in-the-microsoft-365-admin-center"></a>Microsoft 365 관리 센터에서

1. 조직의 관리자 계정에 대 한 자격 증명을 사용 하 여 [Microsoft 365 관리 센터](https://admin.microsoft.com) 에 로그인 합니다.

2. 관리 센터에서 **설정** > **보안 & 개인 정보** > **권한이 부여 된 액세스**로 이동 합니다.

3. **액세스 정책 및 요청 관리를**선택 합니다.

4. 정책 **구성을** 선택 하 고 **정책 추가**를 선택 합니다.

5. 드롭다운 필드에서 조직에 적합 한 값을 선택 합니다.
    
    **정책 유형**: 작업, 역할 또는 역할 그룹

    **정책 범위**: Exchange

    **정책 이름**: 사용 가능한 정책에서 선택

    **승인 유형**: 수동 또는 자동

    **승인 그룹**: 1 단계에서 만든 승인자 그룹을 선택 합니다.

6. **만들기** 를 선택한 다음 **닫기를**선택 합니다. 정책을 완전히 구성 및 사용 하도록 설정 하는 데 몇 분 정도 걸릴 수 있습니다.

### <a name="in-exchange-management-powershell"></a>Exchange 관리 PowerShell에서

승인 정책을 만들고 정의 하려면 Exchange Online PowerShell에서 다음 명령을 실행 합니다.

```
New-ElevatedAccessApprovalPolicy -Task 'Exchange\<exchange management cmdlet name>' -ApprovalType <Manual, Auto> -ApproverGroup '<default/custom approver group>'
```
예제:
```
New-ElevatedAccessApprovalPolicy -Task 'Exchange\New-MoveRequest' -ApprovalType Manual -ApproverGroup 'mbmanagers@fabrikamorg.onmicrosoft.com'
```

<a name="step4"> </a>

## <a name="step-4-submitapprove-privileged-access-requests"></a>4 단계: 권한 있는 액세스 요청 제출/승인

### <a name="requesting-elevation-authorization-to-execute-privileged-tasks"></a>권한 있는 작업 실행을 위한 권한 상승 요청

권한 있는 액세스에 대 한 요청은 요청이 제출 된 후 최대 24 시간 동안 유효 합니다. 승인 되거나 거부 되지 않으면 요청이 만료 되 고 액세스가 승인 되지 않은 것입니다.

#### <a name="in-the-microsoft-365-admin-center"></a>Microsoft 365 관리 센터에서

1. 자격 증명을 사용 하 여 [Microsoft 365 관리 센터](https://admin.microsoft.com) 에 로그인 합니다.

2. 관리 센터에서 **설정** > **보안 & 개인 정보** > **권한이 부여 된 액세스**로 이동 합니다.

3. **액세스 정책 및 요청 관리를**선택 합니다.

4. **새 요청**을 선택 합니다. 드롭다운 필드에서 조직에 적합 한 값을 선택 합니다.

    **요청 유형**: 작업, 역할 또는 역할 그룹

    **요청 범위**: Exchange

    **요청**: 사용 가능한 정책에서 선택

    **기간 (시간)**: 요청 된 액세스에 대 한 시간 수입니다. 요청할 수 있는 시간에 제한이 없습니다.

    **설명**: 액세스 요청과 관련 된 설명에 대 한 텍스트 필드입니다.

5. **저장** 을 선택한 다음 **닫기를**선택 합니다. 요청은 전자 메일을 통해 승인자 그룹에 전송 됩니다.

#### <a name="in-exchange-management-powershell"></a>Exchange 관리 PowerShell에서

Exchange Online PowerShell에서 다음 명령을 실행 하 여 승인자 그룹에 대 한 승인 요청을 만들고 제출 합니다.
```
New-ElevatedAccessRequest -Task 'Exchange\<exchange management cmdlet name>' -Reason '<appropriate reason>' -DurationHours <duration in hours>
```
예제:
```
New-ElevatedAccessRequest -Task 'Exchange\New-MoveRequest' -Reason 'Attempting to fix the user mailbox error' -DurationHours 4
```
### <a name="view-status-of-elevation-requests"></a>권한 상승 요청의 상태 보기
승인 요청을 만든 후에는 요청 ID와 연결 된을 사용 하 여 관리 센터 또는 Exchange 관리 PowerShell에서 권한 상승 요청 상태를 검토할 수 있습니다.

#### <a name="in-the-microsoft-365-admin-center"></a>Microsoft 365 관리 센터에서

1. 자격 증명을 사용 하 여 [Microsoft 365 관리 센터](https://admin.microsoft.com) 에 로그인 합니다.

2. 관리 센터에서 **설정** > **보안 & 개인 정보** > **권한이 부여 된 액세스**로 이동 합니다.

3. **액세스 정책 및 요청 관리를**선택 합니다.

4. **보기** 를 선택 하 여 **대기**, **승인**, **거부**또는 **사용자 Lockbox** 상태를 기준으로 제출 된 요청을 필터링 합니다.

#### <a name="in-exchange-management-powershell"></a>Exchange 관리 PowerShell에서

Exchange Online PowerShell에서 다음 명령을 실행 하 여 특정 요청 ID에 대 한 승인 요청 상태를 확인 합니다.
```
Get-ElevatedAccessRequest -Identity <request ID> | select RequestStatus
```
예제:
```
Get-ElevatedAccessRequest -Identity 28560ed0-419d-4cc3-8f5b-603911cbd450 | select RequestStatus
```

### <a name="approving-an-elevation-authorization-request"></a>권한 상승 인증 요청 승인
승인 요청이 작성 되 면 관련 승인자 그룹의 구성원은 전자 메일 알림을 수신 하 고 요청 ID와 연결 된 요청을 승인할 수 있습니다. 요청자에 게는 전자 메일 메시지를 통한 승인 또는 거부 요청이 통지 됩니다.

#### <a name="in-the-microsoft-365-admin-center"></a>Microsoft 365 관리 센터에서

1. 자격 증명을 사용 하 여 [Microsoft 365 관리 센터](https://admin.microsoft.com) 에 로그인 합니다.

2. 관리 센터에서 **설정** > **보안 & 개인 정보** > **권한이 부여 된 액세스**로 이동 합니다.

3. **액세스 정책 및 요청 관리를**선택 합니다.

4. 나열 된 요청을 선택 하 여 세부 정보를 보고 요청에 대해 작업을 수행 합니다.

5. 요청을 승인 하려면 **승인을** 선택 하 고 요청을 거부 하려면 **거부** 를 선택 합니다. 이전에 승인 된 요청은 **취소**를 선택 하 여 액세스를 취소할 수 있습니다.

#### <a name="in-exchange-management-powershell"></a>Exchange 관리 PowerShell에서

권한 상승 요청을 승인 하려면 Exchange Online PowerShell에서 다음 명령을 실행 합니다.

```
Approve-ElevatedAccessRequest -RequestId <request id> -Comment '<approval comment>'
```
예제:
```
Approve-ElevatedAccessRequest -RequestId a4bc1bdf-00a1-42b4-be65-b6c63d6be279 -Comment '<approval comment>'
```

권한 상승 요청을 거부 하려면 Exchange Online PowerShell에서 다음 명령을 실행 합니다.

```
Deny-ElevatedAccessRequest -RequestId <request id> -Comment '<denial comment>'
```
예제:
```
Deny-ElevatedAccessRequest -RequestId a4bc1bdf-00a1-42b4-be65-b6c63d6be279 -Comment '<denial comment>'
```

## <a name="delete-a-privileged-access-policy-in-office-365"></a>Office 365에서 권한이 부여 된 액세스 정책 삭제
조직에서 더 이상 필요 하지 않은 액세스 정책을 삭제할 수 있습니다.

### <a name="in-the-microsoft-365-admin-center"></a>Microsoft 365 관리 센터에서

1. 조직의 관리자 계정에 대 한 자격 증명을 사용 하 여 [Microsoft 365 관리 센터](https://admin.microsoft.com) 에 로그인 합니다.

2. 관리 센터에서 **설정** > **보안 & 개인 정보** > **권한이 부여 된 액세스**로 이동 합니다.

3. **액세스 정책 및 요청 관리를**선택 합니다.

4. **정책 구성을**선택 합니다.

5. 삭제할 정책을 선택 하 고 **정책 제거**를 선택 합니다.

6. **닫기를**선택 합니다.

### <a name="in-exchange-management-powershell"></a>Exchange 관리 PowerShell에서

권한이 부여 된 액세스 정책을 삭제 하려면 Exchange Online Powershell에서 다음 명령을 실행 합니다.

```
Remove-ElevatedAccessApprovalPolicy -Identity <identity GUID of the policy you want to delete>
```

## <a name="disable-privileged-access-in-office-365"></a>Office 365에서 권한이 부여 된 액세스를 사용 하지 않도록 설정

필요한 경우 조직에 대해 권한이 부여 된 액세스 관리를 사용 하지 않도록 설정할 수 있습니다. 권한 있는 액세스를 사용 하지 않도록 설정 해도 연결 된 승인 정책이 나 승인자 그룹은 삭제 되지 않습니다.

### <a name="in-the-microsoft-365-admin-center"></a>Microsoft 365 관리 센터에서

1. 조직의 관리자 계정에 대 한 자격 증명을 사용 하 여 [Microsoft 365 관리 센터](https://admin.microsoft.com) 에 로그인 합니다.

2. 관리 센터에서 **설정** > **보안 & 개인 정보** > **권한이 부여 된 액세스**로 이동 합니다.

3. 권한 있는 **액세스 제어에 대 한 승인 필요** 를 사용 하도록 설정 합니다.

### <a name="in-exchange-management-powershell"></a>Exchange 관리 PowerShell에서

권한 있는 액세스를 사용 하지 않도록 설정 하려면 Exchange Online Powershell에서 다음 명령을 실행 합니다.

```
Disable-ElevatedAccessControl
```