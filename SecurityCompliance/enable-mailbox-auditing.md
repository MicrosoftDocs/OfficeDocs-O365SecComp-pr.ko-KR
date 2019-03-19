---
title: 사서함 감사 관리
ms.author: markjjo
author: markjjo
manager: laurawi
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- Strat_O365_IP
- M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: aaca8987-5b62-458b-9882-c28476a66918
description: 사서함 감사 로깅은 기본적으로 Microsoft 365에서 설정 됩니다 (기본 사서함 감사 또는 사서함 감사가 기본적으로 라고도 함). 즉, 사서함 소유자, 대리인 및 관리자가 수행 하는 특정 작업이 사서함 감사 로그에 자동으로 기록 되므로 사서함에 대해 수행 된 작업을 검색할 수 있습니다.
ms.openlocfilehash: 604b7fc26c2e97a5efce28fe844fbd066196c4ce
ms.sourcegitcommit: b688d67935edb036658bb5aa1671328498d5ddd3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/19/2019
ms.locfileid: "30670633"
---
# <a name="manage-mailbox-auditing"></a>사서함 감사 관리
  
2019 년 1 월부터 microsoft가 모든 microsoft 365 조 직에 대해 기본적으로 사서함 감사 로깅을 설정 하 고 있습니다. 즉, 사서함 소유자, 대리인 및 관리자가 수행 하는 특정 작업이 자동으로 기록 되며, 사서함 감사 로그에서 해당 사서함을 검색할 때 이러한 레코드를 사용할 수 있게 됩니다. 사서함 감사를 기본적으로 설정 하기 전에 조직의 모든 사용자 사서함에 대해이 기능을 수동으로 사용 하도록 설정 해야 했습니다. 

아래에는 기본적으로 사서함을 감사 하는 몇 가지 이점이 있습니다.

- 새 사서함을 만들 때 감사를 기본적으로 사용 하도록 설정 됩니다. 새 사용자에 대해 수동으로이 기능을 사용 하도록 설정할 필요는 없습니다. 

- 감사 되는 사서함 작업을 관리할 수 없습니다. 정의 된 사서함 작업 집합은 각 로그온 유형에 서 기본적으로 감사 됩니다. 이러한 [로그온 유형은](#mailbox-actions-logged-by-default) 소유자, 대리인 및 관리자입니다.

- Microsoft에서 릴리스한 새 사서함 작업은 기본적으로 감사 됩니다. Microsoft가 새 사서함 작업 (특히 조직을 보호 하 고 법적 조사에 도움을 주는 경우)을 출시할 때 기본적으로 감사 되는 사서함 작업 목록에 자동으로 추가 됩니다. 즉, 소유자, 대리인 또는 관리자가 수행한 사서함 작업 목록에 새 작업을 추가할 필요가 없습니다. 

- 조직 전체에 일관 된 사서함 감사 정책이 적용 되도록 모든 사서함에 대해 동일한 작업을 감사 하 고 있는지 확인 합니다.

> [!TIP]
> 기본적으로 사서함 감사가 해제 된 상태에서 사서함 감사를 관리 하는 작업을 수행 하지 않아도 된다는 것이 중요 합니다. 그러나 더 자세히 알아보거나, 기본 설정에서 동작을 변경 하거나, 사용 하지 않도록 설정 하는 경우에는이 문서에서 해당 작업을 수행할 수 있습니다.

## <a name="verify-mailbox-auditing-on-by-default-is-turned-on"></a>기본적으로 사서함 감사가 설정 되어 있는지 확인

조직에 대해 기본적으로 사서함 감사가 설정 되어 있는지 확인 하려면 [Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell)에서 다음 명령을 실행 합니다.

```
Get-OrganizationConfig | FL AuditDisabled
``` 

**False** 값은 조직에 대해 기본적으로 사서함 감사가 사용 되도록 설정 됨을 나타냅니다. 

기본적으로 사서함 감사가 설정 된 경우 ( *auditdisabled* 속성이 **False**로 설정 된 경우) 조직 설정은 특정 사서함에 대 한 사서함 감사 설정을 재정의 합니다. 예를 들어 사서함에 대해 *auditenabled* 속성이 **False**로 설정 되어 있지만 조직에 대해 기본적으로 사서함 감사를 사용 하는 경우에는 해당 사서함에 대해 기본 사서함 작업이 감사 됩니다. 특정 사서함에 대해 사서함 감사가 명시적으로 사용 하지 않도록 설정 되어 있는 경우 사서함 소유자 및 사서함에 대 한 액세스 권한을 위임 받은 다른 사용자에 대해 사서함 감사 바이패스를 설정할 수 있습니다. 자세한 내용은이 문서의 [사서함 감사 로깅 바이패스](#bypass-mailbox-audit-logging) 섹션을 참조 하십시오.

> [!NOTE]
> 기본적으로 사서함 감사를 설정 하면 현재 **False**로 설정 된 경우 사서함에 대 한 *auditenabled* 속성이 **True** 로 변경 되지 않습니다. 즉, 기본적으로 사서함을 감사 하면 사서함에 대해 *auditenabled* 속성이 무시 됩니다.

## <a name="supported-mailbox-types"></a>지원 되는 사서함 유형

다음 표에는 기본적으로 사서함 감사에서 현재 지원 되는 사서함 유형이 나와 있습니다.

|사서함 유형|지원됨|지원되지 않음|
|:---------|:---------:|:---------:|
|사용자 사서함    |![확인 표시](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)       |         |
|공유 사서함    |![확인 표시](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)        |       |
|Office 365 그룹 사서함    |![확인 표시](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)         |         |
|리소스 사서함    |      |![확인 표시](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)        |
|공용 폴더 사서함    |       |![확인 표시](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)  |
||||

## <a name="mailbox-actions-logged-by-default"></a>기본적으로 기록 되는 사서함 작업

사서함 작업 집합은 다음과 같은 각 로그온 유형에 대해 기본적으로 기록 됩니다.  

   - **소유자** -사서함 소유자입니다. 
   
   - **위임** -사용자의 사서함에 대 한 SendAs, sendonbehalf FullAccess 권한이 할당 된 다른 사용자입니다. 사용자의 사서함에 대 한 FullAccess 권한이 할당 된 관리자도 대리인 사용자로 간주 됩니다.
   
    - **관리자** 는 다음과 같은 경우에만 관리자 로그온 유형에 서 액세스 하는 것으로 간주 됩니다.
    
       - 다음 Microsoft eDiscovery 도구 중 하나를 사용 하 여 사서함을 검색 하는 경우: 

         - 준수 센터의 콘텐츠 검색
       
         -  준수 센터의 eDiscovery 또는 고급 ediscovery
       
         - Exchange Online의 원본 위치 eDiscovery
       - [Microsoft Exchange Server MAPI 편집기](https://go.microsoft.com/fwlink/p/?linkId=204086) 를 사용 하 여 사서함에 액세스 하는 경우     

다음 표에서는 각 로그온 유형에 대해 현재 기본적으로 기록 되는 사서함 작업을 보여 줍니다.

|관리 작업|대리인 작업|소유자 작업|
|:---------|:---------|:---------|
|만들기    |만들기       | HardDelete        |
|HardDelete    |HardDelete        |MoveToDeletedItems       |
|MoveToDeletedItems    |MoveToDeletedItems         |SoftDelete         |
|SendAs    |SendAs      |    업데이트     |
|SendOnBehalf    |SendOnBehalf       |UpdateCalendarDelegation        |
|SoftDelete     |SoftDelete      | updatefolderpermissions 작업이 로깅됩니다        |
|업데이트    |업데이트       |UpdateInboxRules         |
|UpdateCalendarDelegation    | updatefolderpermissions 작업이 로깅됩니다        |         |
|updatefolderpermissions 작업이 로깅됩니다     | UpdateInboxRules        |         |
|UpdateInboxRules     |         |         |
||||

다음은 이러한 사서함 작업에 대 한 설명입니다. 

|사서함 작업|설명|
|:---------|:---------|
|**만들기** <br/> |사서함의 일정, 연락처, 메모 또는 작업 폴더에 항목이 만들어졌습니다. 예를 들어 새 모임 요청이 만들어집니다. 메시지 만들기, 보내기 또는 받기는 감사 되지 않습니다. 또한 사서함 폴더를 만드는 것은 감사 되지 않습니다.  <br/> |
|**HardDelete** <br/> |메시지가 복구 가능한 항목 폴더에서 제거되었습니다.  <br/> |
|**MoveToDeletedItems** <br/> |메시지가 삭제되어 지운 편지함 폴더로 이동되었습니다.  <br/> |
|**SendAs** <br/> |메시지가 SendAs 권한을 사용하여 전송되었습니다. 즉 사서함 소유자가 보낸 것처럼 보이도록 하여 다른 사용자가 메시지를 보냈습니다.  <br/> |
|**SendOnBehalf** <br/> |메시지가 SendOnBehalf 권한을 사용하여 전송되었습니다. 즉 다른 사용자가 사서함 소유자 대신에 메시지를 보냈습니다. 받는 사람은 메시지를 대신 보낸 사용자와 해당 메시지를 실제로 보낸 사용자를 메시지에서 확인할 수 있습니다.  <br/> |
|**SoftDelete** <br/> |메시지가 지운 편지함 폴더에서 삭제되어가 영구적으로 삭제되었습니다. 소프트 삭제된 항목이 복구 가능한 항목 폴더로 이동됩니다.  <br/> |
|**업데이트** <br/> |메시지 또는 해당 속성이 변경되었습니다.  <br/> |
|**UpdateCalendarDelegation** <br/> |일정 위임이 사서함에 할당 되었습니다. 일정 위임 같은 조직에서 사서함 소유자의 일정을 관리 하는 다른 사람에 게 제공 합니다.  <br/> |
|**updatefolderpermissions 작업이 로깅됩니다** <br/> |폴더 사용 권한이 변경 되었습니다. 폴더 사용 권한은 조직에서 사서함의 폴더에 액세스할 수 있는 사용자와 해당 폴더에 있는 메시지를 제어 합니다.  <br/> |
|**UpdateInboxRules** <br/> |받은 편지함 규칙을 추가, 제거 또는 변경 했습니다. 받은 편지함 규칙은 지정 된 조건에 따라 사용자의 받은 편지함에서 메시지를 처리 하 고, 메시지를 지정 된 폴더로 이동 하거나 메시지를 삭제 하는 것과 같이 규칙의 조건이 충족 될 때 작업을 수행 하는 데 사용 됩니다.  <br/> |
|||

사용 가능 하지만 기본 작업 집합에 포함 되지 않은 작업을 포함 하는 전체 사서함 작업 목록은이 문서의 [사서함 감사 작업](#mailbox-auditing-actions) 섹션을 참조 하십시오.

> [!IMPORTANT]
> 조직에 대해 기본적으로 사서함 감사를 수행 하기 전에 로그온 유형을 감사 하도록 사서함 작업을 명시적으로 구성한 경우에는 사서함에 대 한 기존 구성이 우선 하며 기본 사서함에 의해 덮어쓰기 되지 않습니다. 이 섹션에서 설명 하는 작업입니다. 언제 든 지 기본 사서함 작업으로 되돌릴 수 있도록 하려면 **Set-defaultauditset** 명령을 실행 하면 됩니다. 이 작업을 수행 하는 방법에 대 한 자세한 내용은이 문서의 [기본 사서함 작업 복원](#restore-the-default-mailbox-actions) 섹션을 참조 하십시오.

### <a name="verify-that-default-mailbox-actions-are-being-logged-for-each-logon-type"></a>각 로그온 유형에 대해 기본 사서함 작업이 기록 되는지 확인

기본적으로 사서함 감사 릴리스를 사용 하면 *defaultauditset* 이라는 새 사서함 속성이 추가 되었습니다. 이 속성은 지정 된 사서함의 각 로그온 유형에 대해 Microsoft에서 관리 하는 기본 사서함 작업을 감사 하는지 여부를 나타냅니다. 다음 명령을 실행 하 여이 속성의 값을 표시할 수 있습니다.

```
Get-Mailbox <username> | FL DefaultAuditSet
```

값은 세 `Admin, Delegate, Owner` 가지 로그온 유형에 대 한 기본 사서함 작업을 모두 감사 하며 조직의 관리자가 로그온 유형에 대 한 작업을 변경 *하지* 않았음을 나타냅니다. 참고 기본적으로 사서함 감사를 시작한 후의 기본 상태는 조직에서 처음으로 설정 됩니다. 

조직의 관리자가 로그온 유형에 대해 감사 되는 사서함 작업을 변경한 경우 ( *auditadmin*, *auditadmin*또는 *auditadmin* 매개 변수와 함께 **mailbox** cmdlet을 사용 하 여), 다음에 대 한 값 *defaultauditset* 속성은 기본값에 따라 달라 집니다. 예를 들어 값은 사서함 `Owner` 소유자에 대 한 기본 사서함 작업만 감사 되 고, 해당 작업을 수행 하 `Delegate` 고 `Admin` 변경 했는지를 나타냅니다. *defaultauditset* 속성 ( *null* 값이 라고도 함)에 대해 아무 값도 표시 되지 않으면 세 가지 로그온 유형에 대 한 사서함 작업이 모두 변경 된 것입니다.

감사 되는 사서함 작업을 변경 하는 방법에 대 한 자세한 내용은이 문서의 [사서함 작업 변경 또는 복원](#change-or-restore-mailbox-actions-logged-by-default) 섹션을 참조 하십시오.

### <a name="display-a-list-of-mailbox-actions-logged-by-default"></a>기본적으로 기록 되는 사서함 작업의 목록 표시

Exchange Online PowerShell에서 다음 명령을 실행 하 여 각 로그온 유형에 대해 현재 사서함에 대 한 사서함 작업 목록을 표시할 수 있습니다.

**소유자 작업**

```
Get-Mailbox <username> | Select-Object -ExpandProperty AuditOwner
```

**대리인 작업**

```
Get-Mailbox <username> | Select-Object -ExpandProperty AuditDelegate
```

**관리 작업**

```
Get-Mailbox <username> | Select-Object -ExpandProperty AuditAdmin
```

## <a name="change-or-restore-mailbox-actions-logged-by-default"></a>기본적으로 기록 되는 사서함 작업 변경 또는 복원

앞에서 설명한 것 처럼 사서함이 기본적으로 감사 되는 주요 장점 중 하나는 감사 되는 사서함 작업을 관리할 필요가 없다는 것입니다. Microsoft는이 작업을 자동으로 수행 하므로 기본적으로 새 사서함 작업이 릴리스될 때 감사 됩니다. 그러나 조직에서 기본 사서함과는 다른 일련의 작업을 감사 해야 할 수도 있습니다. 이 섹션에서는 각 로그온 유형에 대해 감사 되는 사서함 작업을 변경 하는 방법과 Microsoft가 관리 하는 기본 작업으로 되돌리는 방법을 설명 합니다.

> [!IMPORTANT]
> 다음 섹션에 설명 된 대로 기본적으로 기록 되는 사용자에 대 한 사서함 작업을 변경 하는 경우에는 Microsoft에서 릴리스한 모든 새 사서함 작업이 해당 사서함에 대해 감사 되지 않습니다. 로그온 유형에 대해 감사 되는 작업 목록에 새 사서함 작업을 명시적으로 추가 해야 합니다.

### <a name="change-the-mailbox-actions-to-audit"></a>감사로 사서함 작업 변경

**Set-Mailbox** cmdlet을 *auditadmin*, *auditadmin*또는 *auditadmin* 매개 변수와 함께 사용 하 여 로그온 유형에 따라 감사 되는 사서함 작업을 변경할 수 있습니다. 이러한 감사 관련 매개 변수는 여러 값 매개 변수 (둘 다 사용할 수 있는 값) 이므로 두 가지 방법으로 이러한 변경 작업을 수행할 수도 있습니다.

- 다음 구문을 `action1,action2,...actionN`사용 하 여 기존 작업을 덮어쓰는 여러 사서함 작업을 지정할 수 있습니다.

- 다음 구문을 `@{Add="action1","value2"}` `@{Remove="action1","action2"}`사용 하 여 기존 레코드에 영향을 주지 않고 하나 이상의 사서함 작업을 추가 하거나 제거할 수 있습니다.

감사 되는 사서함 작업을 변경 하는 데 사용 하는 방법에 관계 없이, 사용자가 변경한 로그온 유형에 대해 기본적으로 감사 되는 사서함 작업은 더 이상 Microsoft에서 관리 되지 않습니다. 또한 [이전에 설명한](#verify-that-default-mailbox-actions-are-being-logged-for-each-logon-type) *defaultauditset* mailbox 매개 변수에는 변경한 로그온 유형의 값이 표시 되지 않습니다.

다음은 이러한 방법 중 하나를 사용 하 여 각 서로 다른 로그온 유형에 대해 감사할 사서함 작업을 변경 하는 몇 가지 예입니다. 

이 예에서는 기본 작업을 소프트 삭제 및 하드 삭제로 덮어쓰면서 관리 사서함 작업을 변경 합니다. 

```
Set-Mailbox <username> -AuditAdmin HardDelete,SoftDelete
```

이 예제에서는 MailboxLogin owner 매크로 함수를 추가 합니다. 

```
Set-Mailbox <username> -AuditOwner @{Add="MailboxLogin"}
```

이 예에서는 MoveToDeletedItems 대리인 작업을 제거 합니다.

```
Set-Mailbox <username> -AuditDelegate @{Remove="MoveToDeletedItems"}
```

#### <a name="checking-the-defaultauditset-property"></a>defaultauditset 속성 확인

로그온 유형에 대 한 기본 사서함 작업을 변경한 후에는 사서함의 *defaultauditset* 속성이이 변경 내용을 반영 하도록 자동으로 업데이트 됩니다. 예를 들어 사서함 소유자 작업 `Get-Mailbox <username> | FL DefaultAuditSet` 을 처음 추가 하거나 제거 하 고 나를 실행 하는 경우에는이 명령만 값이 반환 됩니다 `Admin, Delegate`. 이는 소유자에 대 한 기본 사서함 작업이 변경 되었음을 나타내며,이는 Microsoft가 릴리스한 모든 새 사서함 소유자 작업이이 사서함에 자동으로 추가 되지 않음을 의미 합니다. 관리자 또는 대리인 로그온 유형의 사서함 작업을 변경 하는 경우에도 마찬가지입니다.

### <a name="restore-the-default-mailbox-actions"></a>기본 사서함 작업 복원

로그온 유형에 대해 감사 되는 사서함 작업을 변경한 경우에는 `Set-Mailbox -DefaultAuditSet` 명령을 실행 하 여 감사 되는 기본 사서함 작업을 복원할 수 있습니다. 이렇게 하면 다음과 같은 작업이 수행 됩니다.

- 현재 사서함 작업 목록이 해당 하는 로그온 유형에 대 한 기본 사서함 작업으로 대체 됩니다.
 
- Microsoft에서 릴리스한 모든 새 사서함 작업은 해당 하는 로그온 유형에 대 한 목록에 자동으로 추가 됩니다.

- [defaultauditset 사서함 속성](#checking-the-defaultauditset-property) 은 적절 한 로그온 유형을 포함 하도록 업데이트 됩니다.

모든 로그온 유형에 대해 기본 사서함 작업을 복원 하려면 다음 명령을 실행 합니다.

```
Set-Mailbox <username> -DefaultAuditSet Admin,Delegate,Owner
```

이 명령을 사용 하 여 *defaultauditset* 매개 변수에 대해 **관리자**, **대리인**또는 **소유자** 값을 사용 하 여 모든 로그온 유형에 대 한 기본 사서함 작업을 복원할 수 있습니다.

## <a name="turn-off-mailbox-auditing-on-by-default-for-your-organization"></a>조직에 대해 기본적으로 사서함 감사 해제

어떤 이유로 인해 조직에서 사서함 작업을 감사 하지 않을 것으로 판단 되는 경우 Exchange Online PowerShell에서 다음 명령을 실행 하 여 전체 조직에 대해 사서함 감사를 기본적으로 해제할 수 있습니다.

```
Set-OrganizationConfig -AuditDisabled $true
```

조직에 대해 기본적으로 사서함 감사가 해제 되 면 ( *auditdisabled* 속성이 **True**로 설정 됨)에는 다음과 같은 작업이 수행 됩니다.

- 조직에서 사서함 감사를 사용 하지 않도록 설정 합니다.

- 사서함에 대 한 *auditenabled* 속성이 **True**로 설정 된 경우에도 사서함 작업은 감사 되지 않으며 조직에서 감사가 사용 되지 않도록 설정 된 시간부터 시작 됩니다.

- 새 사서함에 대해 사서함 감사를 사용 하지 않도록 설정 하 고 새 (또는 기존) 사서함에서 *auditenabled* 속성을 **True** 로 설정 하는 것은 무시 됩니다.

- **get-mailboxauditbypassassociation** cmdlet을 사용 하 여 구성 되는 모든 사서함 감사 바이패스 연결 설정은 무시 됩니다.

- 기존 사서함 감사 레코드는 레코드에 대 한 감사 로그 기간 제한이 만료 될 때까지 보존 됩니다.

### <a name="turn-on-mailbox-auditing-on-by-default"></a>기본적으로 사서함 감사 켜기

조직에 대 한 사서함 감사를 다시 설정 하려면 Exchange Online PowerShell에서 다음 명령을 실행 하면 됩니다.

```
Set-OrganizationConfig -AuditDisabled $false
```

## <a name="bypass-mailbox-audit-logging"></a>사서함 감사 로깅 바이패스

현재 조직에서 사서함 감사가 기본적으로 설정 된 경우에는 특정 사서함에 대해 사서함 감사를 사용 하지 않도록 설정할 수 없습니다. 예를 들어 *auditenabled* mailbox 속성을 **False** 로 설정 하는 것은 무시 됩니다.  그러나 Exchange Online PowerShell에서 **get-mailboxauditbypassassociation** cmdlet을 사용 하 여 특정 사용자가 수행 하는 사서함 작업이 로깅되지 않도록 할 수 있습니다. 사서함 감사를 우회 하면 해당 작업을 수행 중인 사서함에 관계 없이 특정 사용자가 수행한 사서함 작업이 감사 되지 않습니다. 특정 사용자에 대해 사서함 감사를 우회 하면 해당 사용자가 수행한 사서함 소유자 작업이 로깅되지 않습니다. 또한 동일한 사용자에 게 다른 사용자의 사서함 (또는 공유 사서함)에 대 한 사용 권한이 할당 되 면 첫 번째 사용자가 수행한 위임 작업도 기록 되지 않습니다.

특정 사용자에 대 한 사서함 감사 로깅을 무시 하려면 다음 명령을 실행 합니다.

```
Set-MailboxAuditBypassAssociation -Identity <username> -AuditByPassEnabled $true
```

지정한 사용자에 대해 감사가 무시 되는지 확인 하려면 다음 명령을 실행 합니다.

```
Get-MailboxAuditBypassAssociation -Identity <username> | FL AuditByPassEnabled
```

**True** 값은 해당 사용자에 대해 사서함 감사 로깅이 무시 됨을 나타냅니다.

## <a name="mailbox-auditing-actions"></a>사서함 감사 작업
  
다음 표에서는 각 사용자 로그온 유형에 대해 감사 되는 작업을 요약 하 여 보여 줍니다. 표에서 별표 ( **\*** )는 동작이 기본적으로 기록 됨을 나타냅니다. **No** 는 해당 로그온 유형에 대해 작업을 로그할 수 없음을 나타냅니다. 사용자 사서함에 대 한 모든 액세스 권한이 할당 된 관리자는 대리인 사용자로 간주 됩니다. 
  
|**작업**|**설명**|**Admin**|**대리인**|**소유자**|
|:-----|:-----|:-----|:-----|:-----|
|**복사** <br/> |메시지가 다른 폴더에 복사되었습니다.  <br/> |예  <br/> |아니요  <br/> |아니요  <br/> |
|**만들기** <br/> |사서함의 일정, 연락처, 메모 또는 작업 폴더에 항목이 만들어집니다. 예를 들어 새 모임 요청이 만들어집니다. 메시지 만들기, 보내기 또는 받기는 감사 되지 않습니다. 또한 사서함 폴더를 만드는 것은 감사 되지 않습니다.  <br/> |예\*  <br/> |예\*  <br/> |예  <br/> |
|**FolderBind**\** <br/> |사서함 폴더에 액세스했습니다. 관리자 또는 대리인이 사서함을 열 때에도 작업이 기록됩니다.  <br/> |예  <br/> |예  <br/> |아니요  <br/> |
|**HardDelete** <br/> |메시지가 복구 가능한 항목 폴더에서 제거되었습니다.  <br/> |예\*  <br/> |예\*  <br/> |예\*  <br/> |
|**MailboxLogin** <br/> |사용자가 사서함에 로그인 되어 있습니다.  <br/> |아니요  <br/> |아니요  <br/> |예  <br/> |
|**대해 수행한 messagebind**\*** <br/> |메시지가 미리 보기 창에 표시되거나 열렸습니다.  <br/> |예  <br/> |아니요  <br/> |아니요  <br/> |
|**Move** <br/> |메시지가 다른 폴더로 이동했습니다.  <br/> |예  <br/> |예  <br/> |예  <br/> |
|**MoveToDeletedItems** <br/> |메시지가 삭제되어 지운 편지함 폴더로 이동되었습니다.  <br/> |예\*  <br/> |예\*  <br/> |예\*  <br/> |
|**SendAs** <br/> |메시지가 SendAs 권한을 사용하여 전송되었습니다. 즉 사서함 소유자가 보낸 것처럼 보이도록 하여 다른 사용자가 메시지를 보냈습니다.  <br/> |예\*  <br/> |예\*  <br/> |아니요  <br/> |
|**SendOnBehalf** <br/> |메시지가 SendOnBehalf 권한을 사용하여 전송되었습니다. 즉 다른 사용자가 사서함 소유자 대신에 메시지를 보냈습니다. 받는 사람은 메시지를 대신 보낸 사용자와 해당 메시지를 실제로 보낸 사용자를 메시지에서 확인할 수 있습니다.  <br/> |예\*  <br/> |예\*  <br/> |아니요  <br/> |
|**SoftDelete** <br/> |메시지가 지운 편지함 폴더에서 삭제되어가 영구적으로 삭제되었습니다. 소프트 삭제된 항목이 복구 가능한 항목 폴더로 이동됩니다.  <br/> |예\*  <br/> |예\*  <br/> |예\*  <br/> |
|**업데이트** <br/> |메시지 또는 해당 속성이 변경되었습니다.  <br/> |예\*  <br/> |예\*  <br/> |예\*  <br/> |
|**UpdateCalendarDelegation** <br/> |일정 위임이 사서함에 할당 되었습니다. 일정 위임 조직의 다른 사용자에 게 사서함 소유자의 일정을 관리 하는 권한을 부여 합니다.  <br/> |예\*  <br/> |아니요  <br/> |예\*  <br/> |
|**updatefolderpermissions 작업이 로깅됩니다** <br/> |폴더 사용 권한이 변경 되었습니다. 폴더 사용 권한은 조직에서 사서함의 폴더에 액세스할 수 있는 사용자와 해당 폴더에 있는 메시지를 제어 합니다.  <br/> |예\*  <br/> |예\*  <br/> |예\*  <br/> |
|**UpdateInboxRules** <br/> |받은 편지함 규칙이 추가, 제거 또는 변경 된 경우 받은 편지함 규칙은 지정 된 조건에 따라 사용자의 받은 편지함에서 메시지를 처리 하 고, 메시지를 지정 된 폴더로 이동 하거나 메시지를 삭제 하는 것과 같이 규칙의 조건이 충족 될 때 작업을 수행 하는 데 사용 됩니다.  <br/> |예\*  <br/> |예\*  <br/> |예\*  <br/> |
   
> [!NOTE]
> <sup>\*</sup>로그온 유형에 대해 기본 사서함 감사를 사용 하도록 설정 된 경우 기본적으로 감사 됩니다. <br/><br/>  <sup>\*\*</sup>폴더 바인드에 대 한 감사 레코드는 대리인이 수행 하는 작업을 통합 한 것입니다. 24 시간 내에 개별 폴더 액세스에 대 한 감사 레코드 하나를 생성 합니다. <br/><br/> messagebind 작업은 Exchange Online에서 더 이상 사용 되지 않으며, 관리자 로그온 유형에 대 한 사서함 작업 목록에 더 이상 추가할 수 없습니다. <sup> \* \* \* </sup> 

## <a name="more-information"></a>추가 정보

- 기본적으로 사서함 감사 로그 레코드는 90 일간 보존 된 다음 삭제 됩니다. Exchange Online PowerShell에서 **설정-사서함-auditlogagelimit** 명령을 사용 하 여 감사 로그 레코드의 보존 기간을 변경할 수 있습니다. 사서함 감사 레코드에 대 한 기본 보존 기간을 늘려도 Microsoft 365 감사 로그의 사서함 감사 로그 기록에 대 한 90 일의 기간 제한에 영향을 주지 않습니다. 예를 들어 사서함 감사 로그 레코드의 보존 기간을 365 days로 늘려도 해당 이벤트가 발생 한 후 Microsoft 365 감사 로그에서 90 일 동안 사서함 감사 레코드도 검색 가능 하 게 됩니다. 이 경우 사용자의 사서함 감사 로그에서 90 일 보다 오래 된 레코드를 검색 해야 합니다. 사서함 감사 로그를 검색 하는 방법에 대 한 자세한 내용은 [search-mailboxauditlog](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-audit/search-mailboxauditlog)를 참조 하십시오.

- 조직에 대해 기본적으로 사서함 감사를 수행 하기 전에 사서함에 대 한 *auditlogagelimit* 속성을 변경 하면 해당 사서함에 대 한 기존 감사 로그 보존 기간은 변경 되지 않습니다. 즉, 기본적으로 사서함을 감사 하는 경우 사서함 감사 레코드의 현재 보존 기간에는 영향을 주지 않습니다.

- 사서함 감사 로그 레코드는 각 사용자의 사서함에 있는 복구할 수 있는 항목 폴더에 있는 하위 폴더 ( *감사*)에 저장 됩니다. 사서함 감사 레코드 및 복구할 수 있는 항목 폴더에 대해서는 다음 사항을 염두에 두어야 합니다.
   
    - 사서함 감사 레코드는 복구 가능한 항목 폴더의 저장소 할당량을 기준으로 계산 됩니다 (기본적으로 30gb) (경고 할당량은 20gb). 사서함에 대 한 보류를 설정 하거나 사서함이 준수 센터의 보존 정책에 할당 되 면 복구 가능한 항목 폴더의 저장소 할당량이 자동으로 100 GB (90 MB 경고 할당량)로 증가 합니다.

    - 또한 사서함 감사 레코드는 [복구 가능한 항목 폴더에 대 한 폴더 제한](https://docs.microsoft.com/office365/servicedescriptions/exchange-online-service-description/exchange-online-limits#mailbox-folder-limits)수에 대해서도 계산 됩니다. 감사 하위 폴더에 저장할 수 있는 최대 항목 수 (이 경우 감사 레코드)는 300만 항목입니다. 

      > [!NOTE]
      > 기본적으로 사서함 감사가 복구 가능한 항목 폴더의 저장소 할당량 또는 폴더 제한에 영향을 주는 것은 아닙니다. 

    - Exchange Online PowerShell에서 다음 명령을 실행 하 여 복구 가능한 항목 폴더의 감사 하위 폴더에 있는 항목의 크기 및 수를 표시할 수 있습니다. 
       ```
       Get-MailboxFolderStatistics <username> -FolderScope RecoverableItems | Where-Object {$_.Name -eq 'Audits'} | FL FolderPath,FolderSize,ItemsInFolder
       ```

     - 복구 가능한 항목 폴더의 감사 로그 레코드에 직접 액세스할 수는 없습니다. 대신 **search-mailboxauditlog** cmdlet을 사용 하거나 Microsoft 365 감사 로그를 검색 하 여 사서함 감사 레코드를 찾아서 확인 합니다.

- 사서함이 보류 중이거나 준수 센터의 보존 정책에 할당 된 경우에는 사서함에 대 한 *auditlogagelimit* 속성에 정의 된 기간 동안 감사 로그 레코드가 여전히 보존 됩니다 (기본적으로 90 days로 설정 됨). 보류 중인 사서함에 대해 감사 로그 레코드를 더 오랫동안 보존 하려면 *auditlogagelimit* 속성 값을 늘려 보존 기간을 늘려야 합니다.