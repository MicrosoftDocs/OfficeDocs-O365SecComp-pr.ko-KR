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
# <a name="configuring-privileged-access-management-in-office-365"></a>Office 365에서 액세스 권한을된 관리 구성

> [!IMPORTANT]
> 이 항목에서는 Office 365 e 5 및 고급 준수 Sku에만 현재 제공 되는 기능에 대 한 배포 및 구성 지침에 설명 합니다.

이 항목은 통해 사용 하도록 설정 하 고 Office 365 조직에서 권한이 부여 된 액세스 관리를 구성 하는 것을 안내 합니다. 하나를 사용할 수는 Microsoft 365 관리 센터 또는 Exchange 관리 PowerShell 관리를 사용 하는 액세스 권한이 있습니다. 

## <a name="enable-and-configure-privileged-access-management"></a>설정 하 고 액세스 권한을된 관리 구성

설정 하 고 Office 365 조직에서 액세스 권한을된 사용 하려면 다음이 단계를 수행 합니다.

- [1 단계: 승인자의 그룹 만들기](privileged-access-management-configuration.md#step1)

    권한 액세스를 사용 하 여를 시작 하기 전에 관리자 권한 및 권한 있는 작업에 대 한 액세스에 대 한 수신 요청에 대 한 승인 권한을 갖고 결정 합니다. 승인자 그룹의 구성원 인 모든 사용자 액세스 요청 승인 됩니다. Office 365의 메일 사용이 가능한 보안 그룹을 만들어 사용 하도록 설정 됩니다.

- [2 단계: 사용 권한이 부여 된 액세스](privileged-access-management-configuration.md#step2)

    액세스 권한을된 명시적으로 켜져 있어야 Office 365의 기본 승인자 그룹 및 액세스 권한을된 관리 액세스 제어에서 제외 하려는 시스템 계정 집합을 포함 해야 합니다.

- [3 단계: 액세스 정책 만들기](privileged-access-management-configuration.md#step3)

    승인 정책 만들기 (영문)를 사용 하면 개별 작업에서 범위가 지정 된 특정 승인 요구 사항을 정의할 수 있습니다. 승인 유형 옵션은 **자동** 또는 **수동**입니다.

- [4 단계: 전송/요청을 승인 권한이 부여 된 액세스](privileged-access-management-configuration.md#step4)

    한번 사용 하도록 설정, 권한이 부여 된 액세스는 연결 된 승인 정책 정의 된 모든 작업을 실행 하는 것에 대 한 승인 필요 합니다. 필요에 포함 된 작업을 실행 하는 사용자는 승인 정책을 요청 해야 하 고 작업을 실행 하는 데 필요한 사용 권한이 하기 위해 액세스 승인에 게 부여 합니다.

승인 권한이 부여 되 면 요청 하는 사용자 의도 한 작업을 실행할 수 있고 권한이 부여 된 액세스 권한을 부여 하 고 사용자를 대신 하 여 작업을 실행 됩니다. 승인의 요청에 대해 유효 기간 (기본 기간은 4 시간)을 하는 동안 요청자 수 의도 한 작업을 여러 번 실행 합니다. 이러한 모든 실행 기록 하 고 보안 및 규정 준수 감사를 위해 사용할 수 있게 됩니다. 

> [!NOTE]
> Exchange Online PowerShell Office 365에 연결할 [다단계 인증을 사용 하 여 Exchange Online powershell 연결](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/mfa-connect-to-exchange-online-powershell?view=exchange-ps) 의 단계에 따라 사용 하도록 설정 하 고 액세스 권한을된 구성 하려면 Exchange 관리 PowerShell을 사용 하려는 경우 자격 증명입니다. Exchange Online PowerShell에 연결 하는 동안 액세스 권한을된 사용 하도록 설정 하는 단계를 사용 하 여 Office 365 조직에 대해 다단계 인증을 사용할 필요가 없습니다. 다단계 인증을 통해 연결 요청에 서명 하는 것에 대 한 권한이 부여 된 액세스에 사용 되는 OAuth 토큰을 만듭니다.

<a name="step1"> </a>

## <a name="step-1---create-an-approvers-group"></a>1 단계-승인자의 그룹 만들기

1. 조직에서 관리 계정에 대 한 자격 증명을 사용 하 여 [Microsoft 365 관리 센터](https://portal.office.com) 에 로그인 합니다.

2. 관리 센터에서 **그룹**으로 이동 > **그룹을 추가**합니다.

3. **메일 사용이 가능한 보안 그룹** 그룹 종류를 선택 하 고 새 그룹에 대 한 **이름**, **그룹 전자 메일 주소**및 **설명** 필드에 입력 한 다음 키를 누릅니다.

4. 그룹을 저장 합니다. 완전 하 게 구성 하 고 Office 365 관리 센터에 표시 되는 그룹에 대 한 몇 분정도 걸릴 수 있습니다.

5. 새 승인자의 그룹을 선택 하 고 그룹에 사용자를 추가 하려면 **편집** 을 선택 합니다.

6. 그룹을 저장 합니다.

<a name="step2"> </a>

## <a name="step-2---enable-privileged-access"></a>2 단계-권한이 부여 된 액세스 사용

### <a name="using-the-microsoft-365-admin-center"></a>Microsoft 365 관리 센터를 사용 하 여

1. 조직에서 관리 계정에 대 한 자격 증명을 사용 하 여 [Microsoft 365 관리 센터](https://portal.office.com) 에 로그인 합니다.

2. 관리 센터에서로 이동 **설정 > 보안 및 개인정보** > **권한이 부여 된 액세스**합니다.

3. **권한이 부여 된 액세스에 대 한 승인 필요** 제어를 사용 합니다.

4. **승인자 그룹을 기본**으로 1 단계에서에서 만든 승인자의 그룹을 할당 합니다.

5. **저장** 하 고 **닫기**.

### <a name="using-exchange-management-powershell"></a>Exchange 관리 PowerShell을 사용 하 여

액세스 권한을된 사용 하도록 설정 하 고 승인자의 그룹을 할당 하려면 Exchange Online PowerShell에서 다음 명령을 실행 합니다.
```
Enable-ElevatedAccessControl -AdminGroup '<default approver group>' -SystemAccounts @('<systemAccountUPN1>','<systemAccountUPN2>')
```
예제:
```
Enable-ElevatedAccessControl -AdminGroup 'pamapprovers@fabrikam.onmicrosoft.com' -SystemAccounts @('sys1@fabrikamorg.onmicrosoft.com', sys2@fabrikamorg.onmicrosoft.com')
```

> [!NOTE]
> 그러나 기능 사용 가능 조직 내에서 특정 자동화가 되도록 시스템 계정 액세스 권한을된 의존 관계 없이 사용할 수 있는, 것이 좋습니다 이러한 제외 뛰어난 수 및 승인 고 감사를 수행 해야 허용 된 정기적으로 합니다.

<a name="step3"> </a>

## <a name="step-3---create-an-access-policy"></a>3 단계-액세스 정책 만들기

만들 수 있으며 Office 365 조직에 대 한 최대 30 개의 권한이 부여 된 액세스 정책 구성.

### <a name="using-the-microsoft-365-admin-center"></a>Microsoft 365 관리 센터를 사용 하 여

1. 조직에서 관리 계정에 대 한 자격 증명을 사용 하 여 [Microsoft 365 관리 센터](https://portal.office.com) 에 로그인 합니다.

2. 관리 센터에서 **설정**으로 이동 > **보안 및 개인정보** > **권한이 부여 된 액세스**합니다.

3. **관리 액세스 정책 및 요청을**선택 합니다.

4. **정책을 구성을** 선택 하 고 **정책 추가**선택 합니다.

5. 드롭다운 필드에서 조직에 대 한 적절 한 값을 선택 합니다.
    
    **정책 유형**: 작업, 역할 또는 역할 그룹

    **정책 범위**: Exchange 또는 Office 365

    **정책 이름**: 사용 가능한 정책에서 선택

    **승인 유형**: 수동 또는 자동

    **승인 그룹**: 1 단계에서 만든 승인자 그룹을 선택 합니다.

6. **만들고 다음 **닫기**** 를 선택 합니다. 완벽 하 게 구성 하 고 사용을 정책에 대 한 몇 분정도 걸릴 수 있습니다.

### <a name="using-exchange-management-powershell"></a>Exchange 관리 PowerShell을 사용 하 여

다음 명령을 실행 Exchange 온라인를 만들고 승인 정책을 정의 하는 PowerShell:

```
New-ElevatedAccessApprovalPolicy -Task 'Exchange\<exchange management cmdlet name>' -ApprovalType <Manual, Auto> -ApproverGroup '<default/custom approver group>'
```
예제:
```
New-ElevatedAccessApprovalPolicy -Task 'Exchange\New-MoveRequest' -ApprovalType Manual -ApproverGroup 'mbmanagers@fabrikamorg.onmicrosoft.com'
```

<a name="step4"> </a>

## <a name="step-4-submitapprove-privileged-access-requests"></a>4 단계: 전송/요청을 승인 권한이 부여 된 액세스

### <a name="requesting-elevation-authorization-to-execute-privileged-tasks"></a>권한이 부여 된 작업을 실행할 수 상승 권한 부여를 요청 합니다.

권한이 부여 된 액세스에 대 한 요청은 요청을 제출 하는 최대 24 시간 동안 유효 합니다. 요청은 만료 되지 승인 또는 거부 하는 경우 및 액세스 승인 되지 않은 합니다.

#### <a name="using-the-microsoft-365-admin-center"></a>Microsoft 365 관리 센터를 사용 하 여

1. 사용자의 자격 증명을 사용 하 여 [Microsoft 365 관리 센터](https://portal.office.com) 에 로그인 합니다.

2. 관리 센터에서 **설정**으로 이동 > **보안 및 개인정보** > **권한이 부여 된 액세스**합니다.

3. **관리 액세스 정책 및 요청을**선택 합니다.

4. **새 요청**을 선택 합니다. 드롭다운 필드에서 조직에 대 한 적절 한 값을 선택 합니다.

    **요청 유형**: 작업, 역할 또는 역할 그룹

    **범위 요청**: Exchange

    **에 대 한 요청**: 사용 가능한 정책에서 선택

    **기간 (시간)**: 요청 된 액세스의 시간입니다. 요청할 수 있는 시간 수에 대 한 제한이 없습니다.

    **설명**: 액세스 요청에 관련 된 메모에 대 한 텍스트 필드

5. **저장** 한 다음 **닫기**를 선택 합니다. 전자 메일을 통해 승인자의 그룹에 사용자의 요청을 전송 됩니다.

#### <a name="using-exchange-management-powershell"></a>Exchange 관리 PowerShell을 사용 하 여

다음 명령을 실행 Exchange Online을 만들고 승인자의 그룹에 대 한 승인 요청을 제출 하는 PowerShell:
```
New-ElevatedAccessRequest -Task 'Exchange\<exchange management cmdlet name>' -Reason '<appropriate reason>' -DurationHours <duration in hours>
```
예제:
```
New-ElevatedAccessRequest -Task 'Exchange\New-MoveRequest' -Reason 'Attempting to fix the user mailbox error' -DurationHours 4
```
### <a name="view-status-of-elevation-requests"></a>권한 상승 요청 상태 보기
승인 요청을 만든 후 상승 요청 상태를 검토 하 여 관리 센터의 수 또는 Exchange 관리 PowerShell을 사용 하 여 연결 된 요청 id를.합니다

#### <a name="using-the-microsoft-365-admin-center"></a>Microsoft 365 관리 센터를 사용 하 여

1. 사용자의 자격 증명을 사용 하 여 [Microsoft 365 관리 센터](https://portal.office.com) 에 로그인 합니다.

2. 관리 센터에서 **설정**으로 이동 > **보안 및 개인정보** > **권한이 부여 된 액세스**합니다.

3. **관리 액세스 정책 및 요청을**선택 합니다.

4. **보류 중인**, **승인**, **거부**또는 **고객 Lockbox** 상태별으로 제출 된 요청을 필터링 하려면 **보기** 선택 합니다.

#### <a name="using-exchange-management-powershell"></a>Exchange 관리 PowerShell을 사용 하 여

다음 명령을 실행 Exchange 온라인 PowerShell 특정 요청 ID에 대 한 승인 요청 상태를 볼 수 있습니다.
```
Get-ElevatedAccessRequest -Identity <request ID> | select RequestStatus
```
예제:
```
Get-ElevatedAccessRequest -Identity 28560ed0-419d-4cc3-8f5b-603911cbd450 | select RequestStatus
```

### <a name="approving-an-elevation-authorization-request"></a>권한 상승 권한 부여 요청이 승인
관련 승인자 그룹의 구성원이 전자 메일 알림을 받게 됩니다 및 요청 ID와 연결 된 요청을 승인할 수를 승인 요청을 만들 때 검토자가 요청자의 요청 승인 또는 거부 전자 메일 메시지를 통해 알림을 받게 됩니다.

#### <a name="using-the-microsoft-365-admin-center"></a>Microsoft 365 관리 센터를 사용 하 여

1. 사용자의 자격 증명을 사용 하 여 [Microsoft 365 관리 센터](https://portal.office.com) 에 로그인 합니다.

2. 관리 센터에서 **설정**으로 이동 > **보안 및 개인정보** > **권한이 부여 된 액세스**합니다.

3. **관리 액세스 정책 및 요청을**선택 합니다.

4. 나열 된 요청 세부 정보를 표시 하 고 요청 시 조치를 취할 수를 선택 합니다.

5. **승인** 요청을 승인 요청을 거부 하려면 **거부** 선택 하거나 선택 합니다. 이전에 승인 된 요청이 **해지**를 선택 하 여 해지 액세스를 가질 수 있습니다.

#### <a name="using-exchange-management-powershell"></a>Exchange 관리 PowerShell을 사용 하 여

다음 명령을 실행 Exchange 온라인는 상승 인증 요청을 승인 하는 PowerShell:

```
Approve-ElevatedAccessRequest -RequestId <request id> -Comment '<approval comment>'
```
예제:
```
Approve-ElevatedAccessRequest -RequestId a4bc1bdf-00a1-42b4-be65-b6c63d6be279 -Comment '<approval comment>'
```

다음 명령을 실행 Exchange Online PowerShell는 상승 인증 요청을 거부 하려면:

```
Deny-ElevatedAccessRequest -RequestId <request id> -Comment '<denial comment>'
```
예제:
```
Deny-ElevatedAccessRequest -RequestId a4bc1bdf-00a1-42b4-be65-b6c63d6be279 -Comment '<denial comment>'
```

## <a name="delete-a-privileged-access-policy-in-office-365"></a>Office 365에서 권한이 부여 된 액세스 정책 삭제
조직에서 더이상 필요할 경우 권한이 부여 된 액세스 정책을 삭제할 수 없습니다.

### <a name="using-the-microsoft-365-admin-center"></a>Microsoft 365 관리 센터를 사용 하 여

1. 조직에서 관리 계정에 대 한 자격 증명을 사용 하 여 [Microsoft 365 관리 센터](https://portal.office.com) 에 로그인 합니다.

2. 관리 센터에서 **설정**으로 이동 > **보안 및 개인정보** > **권한이 부여 된 액세스**합니다.

3. **관리 액세스 정책 및 요청을**선택 합니다.

4. **Configure 정책**을 선택 합니다.

5. 삭제 하려는 정책을 선택 하 고 **정책 제거**를 선택 합니다.

6. **Close**를 선택 합니다.

### <a name="using-exchange-management-powershell"></a>Exchange 관리 PowerShell을 사용 하 여

다음 명령을 실행 Exchange Online Powershell 권한이 부여 된 액세스 정책을 삭제 하려면:

```
Remove-ElevatedAccessApprovalPolicy -Identity <identity GUID of the policy you want to delete>
```

## <a name="disable-privileged-access-in-office-365"></a>Office 365에 대 한 액세스 권한을된 사용 하지 않도록 설정

필요한 경우에 조직에 대 한 액세스 권한을된 관리를 비활성화할 수 있습니다. 권한 사용 하지 않도록 설정 액세스 삭제 되지 않습니다 모든 관련된 승인 정책 또는 승인자 그룹.

### <a name="using-the-microsoft-365-admin-center"></a>Microsoft 365 관리 센터를 사용 하 여

1. 조직에서 관리 계정에 대 한 자격 증명을 사용 하 여 [Microsoft 365 관리 센터](https://portal.office.com) 에 로그인 합니다.

2. 관리 센터에서 **설정**으로 이동 > **보안 및 개인정보** > **권한이 부여 된 액세스**합니다.

3. **권한이 부여 된 액세스에 대 한 승인 필요** 제어를 사용 합니다.

### <a name="using-exchange-management-powershell"></a>Exchange 관리 PowerShell을 사용 하 여

다음 명령을 실행 Exchange Online Powershell 액세스 권한을된 사용 하지 않도록 설정 하려면:

```
Disable-ElevatedAccessControl
```