---
title: 사서함 감사 관리
ms.author: chrisda
author: chrisda
manager: serdars
audience: Admin
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
ms.openlocfilehash: 8e5901586b6ee8e34d3e71b0b256f9aa7c86c7de
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/17/2019
ms.locfileid: "34154780"
---
# <a name="manage-mailbox-auditing"></a>사서함 감사 관리

2019 년 1 월부터 Microsoft가 모든 Microsoft 365 조 직에 대해 기본적으로 사서함 감사 로깅을 설정 하 고 있습니다. 즉, 사서함 소유자, 대리인 및 관리자가 수행 하는 특정 작업이 자동으로 기록 되며, 사서함 감사 로그에서 해당 사서함을 검색할 때 이러한 레코드를 사용할 수 있게 됩니다. 사서함 감사를 기본적으로 설정 하기 전에 조직의 모든 사용자 사서함에 대해이 기능을 수동으로 사용 하도록 설정 해야 했습니다.

아래에는 기본적으로 사서함을 감사 하는 몇 가지 이점이 있습니다.

- 새 사서함을 만들 때 감사가 자동으로 사용 하도록 설정 됩니다. 새 사용자에 대해 수동으로이 기능을 사용 하도록 설정할 필요는 없습니다.

- 감사 되는 사서함 작업을 관리할 필요는 없습니다. 미리 정의 된 사서함 작업 집합은 각 로그온 유형 (관리자, 위임 및 소유자)에 대해 기본적으로 감사 됩니다.

- Microsoft가 새 사서함 작업을 출시할 때 (특히 사용자의 조직 보호 및 법적 조사에 도움을 주는 작업) 작업이 기본적으로 감사 되는 사서함 작업 목록에 자동으로 추가 됩니다. 즉, 사서함에 대 한 새 작업 추가를 모니터링할 필요가 없습니다.

- 모든 사서함에 대해 동일한 작업을 감사 하 고 있으므로 조직 전체에 일관 된 사서함 감사 정책이 있습니다.

> [!TIP]
> 기본적으로 사서함 감사 릴리스를 고려해 야 할 중요 한 사항은 다음과 같습니다. 사서함 감사를 관리할 필요가 없습니다. 그러나 자세한 내용을 보거나 기본 설정에서 사서함 감사를 사용자 지정 하거나 완전히 해제 하려면이 항목을 참조 하십시오.

## <a name="verify-mailbox-auditing-on-by-default-is-turned-on"></a>기본적으로 사서함 감사가 설정 되어 있는지 확인

조직에 대해 기본적으로 사서함 감사가 설정 되어 있는지 확인 하려면 [Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell)에서 다음 명령을 실행 합니다.

```
Get-OrganizationConfig | Format-List AuditDisabled
```

**False** 값은 조직에 대해 기본적으로 사서함 감사가 사용 되도록 설정 됨을 나타냅니다. 기본적으로 조직 값은 특정 사서함에 대 한 사서함 감사 설정을 재정의 합니다. 예를 들어 사서함에 대해 사서함 감사를 사용 하지 않도록 설정 된 경우 (해당 사서함에서 *Auditenabled* 속성이 **False** 인 경우) 사서함에 대 한 mailbox 감사가 기본적으로 설정 되어 있으므로 사서함에 대해 기본 사서함 작업이 계속 감사 됩니다. 조직.

특정 사서함에 대해 사서함 감사를 사용 하지 않도록 설정 하려면 사서함 소유자 및 사서함에 대 한 액세스 권한을 위임 받은 다른 사용자에 대해 사서함 감사 바이패스를 구성 합니다. 자세한 내용은이 항목의 [사서함 감사 로깅 바이패스](#bypass-mailbox-audit-logging) 섹션을 참조 하십시오.

> [!NOTE]
> 조직에 대해 기본적으로 사서함 감사가 설정 되어 있으면 영향을 받는 사서함에 대 한 *Auditenabled* 속성은 **False** 에서 **True**로 변경 되지 않습니다. 즉 사서함에 대 한 *Auditenabled* 속성을 무시 합니다.

## <a name="supported-mailbox-types"></a>지원 되는 사서함 유형

다음 표에는 기본적으로 사서함 감사에서 현재 지원 되는 사서함 유형이 나와 있습니다.

|**사서함 유형**|**지원**|**지원되지 않음**|
|:---------|:---------:|:---------:|
|사용자 사서함|![확인 표시](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)||
|공유 사서함|![확인 표시](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)||
|Office 365 그룹 사서함|![확인 표시](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)||
|리소스 사서함||![확인 표시](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)|
|공용 폴더 사서함||![확인 표시](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)|

## <a name="logon-types-and-mailbox-actions"></a>로그온 유형 및 사서함 작업

로그온 유형은 사서함에 대해 감사 된 작업을 수행한 사용자를 분류 합니다. 다음 목록에서는 사서함 감사 로깅에 사용 되는 로그온 유형에 대해 설명 합니다.

- **소유자**: 사서함 소유자 (사서함과 연결 된 계정)입니다.

- **대리인**:

  - 다른 사서함에 대 한 SendAs, SendOnBehalf FullAccess 권한이 할당 된 사용자입니다.

  - 사용자의 사서함에 대 한 FullAccess 권한이 할당 된 관리자입니다.

- **관리자**:

  - 다음 Microsoft eDiscovery 도구 중 하나를 사용 하 여 사서함을 검색 합니다.

    - 준수 센터의 콘텐츠 검색

    - 준수 센터의 eDiscovery 또는 고급 eDiscovery

    - Exchange Online의 원본 위치 eDiscovery

  - [Microsoft Exchange SERVER MAPI 편집기](https://go.microsoft.com/fwlink/p/?linkId=204086)를 사용 하 여 사서함에 액세스 합니다.

### <a name="mailbox-actions-for-user-mailboxes-and-shared-mailboxes"></a>사용자 사서함 및 공유 사서함에 대 한 사서함 작업

다음 표에서는 사용자 사서함 및 공유 사서함에 대 한 사서함 감사 로깅에서 사용할 수 있는 사서함 작업에 대해 설명 합니다.

- 확인 표시 ( ![확인 표시](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png))는 사서함 작업이 로그온 유형에 대해 기록 될 수 있음을 나타냅니다 (모든 작업을 모든 로그온 유형에 사용할 수 있는 것은 아님).

- 확인 표시 후 <sup>\*</sup> 에 별표 ()는 로그온 유형에 대해 기본적으로 사서함 작업이 기록 됨을 나타냅니다.

- 사서함에 대 한 모든 권한이 있는 관리자는 대리인으로 간주 됩니다.

|**사서함 작업**|**설명**|**Admin**|**대리인**|**소유자**|
|:---------|:---------|:---------:|:---------:|:---------:|
|**AddFolderPermissions**|**참고**:이 값은 사서함 작업으로 허용 되지만 **updatefolderpermissions** 작업에 이미 포함 되어 있으며 별도로 감사 되지 않습니다. 즉,이 값을 사용 하지 마십시오.||||
|**ApplyRecord**|항목은 레코드로 레이블이 지정 됩니다.|![확인 표시](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)|![확인 표시](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)|![확인 표시](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)|
|**복사**|메시지가 다른 폴더에 복사되었습니다.|![확인 표시](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)|||
|**만들기**|사서함의 일정, 연락처, 메모 또는 작업 폴더 (예: 새 모임 요청이 만들어짐)에 항목이 만들어집니다. 메시지 만들기, 보내기 또는 받기는 감사 되지 않습니다. 또한 사서함 폴더를 만드는 것은 감사 되지 않습니다.|![확인 표시](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)<sup>\*</sup>|![확인 표시](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)<sup>\*</sup>|![확인 표시](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)|
|**FolderBind**|사서함 폴더에 액세스했습니다. 관리자 또는 대리인이 사서함을 열 때에도 작업이 기록됩니다.<br/><br/> **참고**: 대리인에 의해 수행 된 폴더 바인드 작업에 대 한 감사 기록이 통합 되어 있습니다. 24 시간 내에 개별 폴더 액세스에 대 한 감사 레코드 하나를 생성 합니다.|![확인 표시](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)|![확인 표시](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)||
|**HardDelete**|메시지가 복구 가능한 항목 폴더에서 제거되었습니다.|![확인 표시](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)<sup>\*</sup>|![확인 표시](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)<sup>\*</sup>|![확인 표시](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)<sup>\*</sup>|
|**MailboxLogin**|사용자가 사서함에 로그인 되어 있습니다. |||![확인 표시](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)|
|**대해 수행한 messagebind**|**참고**:이 작업은 Exchange Online에서 더 이상 사용 되지 않으며, 관리자 사서함 작업 목록에 더 이상 추가할 수 없습니다.<br/><br/> 메시지가 미리 보기 창에 표시되거나 열렸습니다.|![확인 표시](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)|||
|**ModifyFolderPermissions**|**참고**:이 값은 사서함 작업으로 허용 되지만 **updatefolderpermissions** 작업에 이미 포함 되어 있으며 별도로 감사 되지 않습니다. 즉,이 값을 사용 하지 마십시오.||||
|**Move**|메시지가 다른 폴더로 이동했습니다.|![확인 표시](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)|![확인 표시](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)|![확인 표시](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)|
|**MoveToDeletedItems**|메시지가 삭제되어 지운 편지함 폴더로 이동되었습니다.|![확인 표시](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)<sup>\*</sup>|![확인 표시](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)<sup>\*</sup>|![확인 표시](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)<sup>\*</sup>|
|**RecordDelete**|레코드로 레이블이 지정 된 항목은 일시 삭제 (복구 가능한 항목 폴더로 이동) 되었습니다. 레코드로 레이블이 지정 된 항목은 영구적으로 삭제할 수 없습니다 (복구 가능한 항목 폴더에서 제거).|![확인 표시](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)|![확인 표시](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)|![확인 표시](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)|
|**RemoveFolderPermissions**|**참고**:이 값은 사서함 작업으로 허용 되지만 **updatefolderpermissions** 작업에 이미 포함 되어 있으며 별도로 감사 되지 않습니다. 즉,이 값을 사용 하지 마십시오.||||
|**SendAs**|메시지가 SendAs 권한을 사용하여 전송되었습니다. 즉 사서함 소유자가 보낸 것처럼 보이도록 하여 다른 사용자가 메시지를 보냈습니다.|![확인 표시](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)<sup>\*</sup>|![확인 표시](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)<sup>\*</sup>||
|**SendOnBehalf**|메시지가 SendOnBehalf 권한을 사용하여 전송되었습니다. 즉 다른 사용자가 사서함 소유자 대신에 메시지를 보냈습니다. 받는 사람은 메시지를 대신 보낸 사용자와 해당 메시지를 실제로 보낸 사용자를 메시지에서 확인할 수 있습니다.|![확인 표시](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)<sup>\*</sup>|![확인 표시](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)<sup>\*</sup>||
|**SoftDelete**|메시지가 지운 편지함 폴더에서 삭제되어가 영구적으로 삭제되었습니다. 소프트 삭제된 항목이 복구 가능한 항목 폴더로 이동됩니다.|![확인 표시](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)<sup>\*</sup>|![확인 표시](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)<sup>\*</sup>|![확인 표시](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)<sup>\*</sup>|
|**업데이트**|메시지 또는 해당 속성이 변경되었습니다.|![확인 표시](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)<sup>\*</sup>|![확인 표시](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)<sup>\*</sup>|![확인 표시](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)<sup>\*</sup>|
|**UpdateCalendarDelegation**|일정 위임이 사서함에 할당 되었습니다. 일정 위임 같은 조직에서 사서함 소유자의 일정을 관리 하는 다른 사람에 게 제공 합니다.|![확인 표시](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)<sup>\*</sup>||![확인 표시](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)<sup>\*</sup>|
|**Updatefolderpermissions 작업이 로깅됩니다**|폴더 사용 권한이 변경 되었습니다. 폴더 사용 권한은 조직에서 사서함의 폴더에 액세스할 수 있는 사용자와 해당 폴더에 있는 메시지를 제어 합니다.|![확인 표시](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)<sup>\*</sup>|![확인 표시](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)<sup>\*</sup>|![확인 표시](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)<sup>\*</sup>|
|**UpdateInboxRules**|받은 편지함 규칙을 추가, 제거 또는 변경 했습니다. 받은 편지함 규칙은 지정 된 조건에 따라 사용자의 받은 편지함에서 메시지를 처리 하 고, 메시지를 지정 된 폴더로 이동 하거나 메시지를 삭제 하는 것과 같이 규칙의 조건이 충족 될 때 작업을 수행 하는 데 사용 됩니다.|![확인 표시](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)<sup>\*</sup>|![확인 표시](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)<sup>\*</sup>|![확인 표시](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)<sup>\*</sup>|

> [!IMPORTANT]
> 조직에서 기본적으로 사서함 감사를 사용 하도록 설정 *하기 전에* 모든 로그온 유형에 대해 감사를 위해 사서함 작업을 사용자 지정 하는 경우 사용자 지정 설정이 사서함에 보존 되며 기본 사서함 작업에 의해 덮어쓰기 되지 않습니다. 이 섹션에 설명 되어 있습니다. 감사 사서함 작업을 기본값으로 되돌리려면 (언제 든 지이 작업을 수행할 수 있음)이 항목의 뒷부분에 나오는 [기본 사서함 작업 복원](#restore-the-default-mailbox-actions) 섹션을 참조 하십시오.

### <a name="mailbox-actions-for-office-365-group-mailboxes"></a>Office 365 그룹 사서함에 대 한 사서함 작업

기본적으로 사서함 감사는 Office 365 그룹 사서함에 대 한 사서함 감사 로깅을 제공 하지만 로깅할 항목을 사용자 지정할 수 없습니다 (로그온 유형에 대해 기록 되는 사서함 작업을 추가 하거나 제거할 수 없음).

다음 표에서는 각 로그온 유형에 대해 Office 365 그룹 사서함에 기본적으로 기록 되는 사서함 작업에 대해 설명 합니다.

Office 365 그룹 사서함에 대 한 모든 권한이 있는 관리자는 대리인으로 간주 됩니다.

|**사서함 작업**|**설명**|**Admin**|**대리인**|**소유자**|
|:---------|:---------|:---------:|:---------:|:---------:|
|**만들기**|일정 항목 만들기 메시지 만들기, 보내기 또는 받기는 감사 되지 않습니다.|![확인 표시](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)<sup>\*</sup>|![확인 표시](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)<sup>\*</sup>||
|**HardDelete**|메시지가 복구 가능한 항목 폴더에서 제거되었습니다.|![확인 표시](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)<sup>\*</sup>|![확인 표시](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)<sup>\*</sup>|![확인 표시](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)<sup>\*</sup>|
|**MoveToDeletedItems**|메시지가 삭제되어 지운 편지함 폴더로 이동되었습니다.|![확인 표시](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)<sup>\*</sup>|![확인 표시](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)<sup>\*</sup>|![확인 표시](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)<sup>\*</sup>|
|**SendAs**|메시지가 SendAs 권한을 사용하여 전송되었습니다.|![확인 표시](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)<sup>\*</sup>|![확인 표시](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)<sup>\*</sup>||
|**SendOnBehalf**|메시지가 SendOnBehalf 권한을 사용하여 전송되었습니다. |![확인 표시](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)<sup>\*</sup>|![확인 표시](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)<sup>\*</sup>||
|**SoftDelete**|메시지가 지운 편지함 폴더에서 삭제되어가 영구적으로 삭제되었습니다. 소프트 삭제된 항목이 복구 가능한 항목 폴더로 이동됩니다.|![확인 표시](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)<sup>\*</sup>|![확인 표시](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)<sup>\*</sup>|![확인 표시](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)<sup>\*</sup>|
|**업데이트**|메시지 또는 해당 속성이 변경되었습니다.|![확인 표시](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)<sup>\*</sup>|![확인 표시](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)<sup>\*</sup>|![확인 표시](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)<sup>\*</sup>|

### <a name="verify-that-default-mailbox-actions-are-being-logged-for-each-logon-type"></a>각 로그온 유형에 대해 기본 사서함 작업이 기록 되는지 확인

기본적으로 사서함 감사는 모든 사서함에 새 *Defaultauditset* 속성을 추가 합니다. 이 속성의 값은 사서함에서 기본 사서함 작업 (Microsoft에서 관리)이 감사 되 고 있는지 여부를 나타냅니다.

사용자 사서함 또는 공유 사서함에 값을 표시 하려면 MailboxIdentity \<\> 를 이름, 별칭, 전자 메일 주소 또는 사서함의 upn (사용자 계정 이름)으로 바꾸고 Exchange Online PowerShell에서 다음 명령을 실행 합니다.

```
Get-Mailbox -Identity <MailboxIdentity> | Format-List DefaultAuditSet
```

Office 365 그룹 사서함에 값을 표시 하려면 MailboxIdentity \<\> 을 공유 사서함의 이름, 별칭 또는 전자 메일 주소로 바꾸고 Exchange Online PowerShell에서 다음 명령을 실행 합니다.

```
Get-Mailbox -Identity <MailboxIdentity> -GroupMailbox | Format-List DefaultAuditSet
```

값 `Admin, Delegate, Owner` 은 다음을 나타냅니다.

- 세 가지 로그온 유형에 대 한 기본 사서함 작업을 모두 감사 합니다. 이 값은 Office 365 그룹 사서함에만 표시 됩니다.

- 관리자가 사용자 사서함 또는 공유 사서함의 로그온 유형에 대해 감사 된 사서함 작업을 변경 *하지* 않았습니다. 참고 기본적으로 사서함 감사를 시작한 후의 기본 상태는 조직에서 처음으로 설정 됩니다.

관리자가 로그온 유형에 대해 감사 되는 사서함 작업 ( *Auditadmin*, *Auditadmin*또는 **Set mailbox** cmdlet의 *auditadmin* 매개 변수를 사용 하 여)을 변경한 적이 없는 경우이 속성 값은 서로 다릅니다.

예를 들어 사용자 사서함 `Owner` 또는 공유 사서함의 *defaultauditset* 속성에 대 한 값은 다음을 나타냅니다.

- 사서함 소유자에 대 한 기본 사서함 작업을 감사 하 고 있습니다.

- `Delegate` 및 `Admin` 로그온 유형에 대 한 감사 된 사서함 작업이 기본 작업에서 변경 되었습니다.

*Defaultauditset* 속성의 값이 비어 있으면 사용자 사서함 이나 공유 사서함에서 세 가지 로그온 유형에 대 한 사서함 작업이 모두 변경 되었음을 나타냅니다.

자세한 내용은이 항목의 " [사서함 작업을 기본값으로 기록](#change-or-restore-mailbox-actions-logged-by-default) " 섹션을 참조 하십시오.

### <a name="display-the-mailbox-actions-that-are-being-logged-on-mailboxes"></a>기록 중인 사서함 작업을 사서함에 표시 합니다.

현재 사용자 사서함 또는 공유 사서함에 대해 로그온 중인 사서함 작업을 확인 하려면 MailboxIdentity \<\> 를 이름, 별칭, 전자 메일 주소 또는 사서함의 사용자 이름 (username)으로 바꾸고 다음 중 하나 이상을 실행 합니다. Exchange Online PowerShell의 명령입니다.

> [!NOTE]
> Office 365 그룹 사서함의 `-GroupMailbox` 다음 **사서함** 명령에 스위치를 추가할 수는 있지만 표시 되는 값은 생각 하지 마십시오. Office 365 그룹 사서함에 대해 감사 되는 기본 및 정적 사서함 작업은이 항목 앞부분의 [office 365 그룹 사서함에 대 한 사서함 작업](#mailbox-actions-for-office-365-group-mailboxes) 섹션에 설명 되어 있습니다.

#### <a name="owner-actions"></a>소유자 작업

```
Get-Mailbox -Identity <MailboxIdentity> | Select-Object -ExpandProperty AuditOwner
```

#### <a name="delegate-actions"></a>대리인 작업

```
Get-Mailbox -Identity <MailboxIdentity> | Select-Object -ExpandProperty AuditDelegate
```

#### <a name="admin-actions"></a>관리 작업

```
Get-Mailbox -Identity <MailboxIdentity> | Select-Object -ExpandProperty AuditAdmin
```

## <a name="change-or-restore-mailbox-actions-logged-by-default"></a>기본적으로 기록 되는 사서함 작업 변경 또는 복원

앞에서 설명한 것 처럼 사서함 감사를 기본적으로 수행 하는 주요 이점은 다음과 같습니다. 감사 되는 사서함 작업을 관리할 필요는 없습니다. Microsoft는이 작업을 자동으로 수행 하므로 기본적으로 새로운 사서함 작업이 릴리스될 때 감사 되도록 추가 합니다.

그러나 조직에서 사용자 사서함 및 공유 사서함에 대 한 다른 사서함 작업 집합을 감사 해야 할 수 있습니다. 이 섹션의 절차에서는 각 로그온 유형에 대해 감사 되는 사서함 작업을 변경 하는 방법과 Microsoft가 관리 하는 기본 작업으로 되돌리는 방법을 보여 줍니다.

> [!IMPORTANT]
> 다음 절차를 사용 하 여 사용자 사서함 또는 공유 사서함에 기록 된 사서함 작업을 사용자 지정 하는 경우 Microsoft에서 릴리스한 모든 새 기본 사서함 작업은 해당 사서함에서 자동으로 감사 되지 않습니다. 사용자 지정한 작업 목록에 새 사서함 작업을 수동으로 추가 해야 합니다.

### <a name="change-the-mailbox-actions-to-audit"></a>감사로 사서함 작업 변경

**사서함** Cmdlet에서 *auditadmin*, *auditadmin*또는 *auditadmin* 매개 변수를 사용 하 여 사용자 사서함 및 공유 사서함에 대해 감사 되는 사서함 작업을 변경할 수 있습니다 (Office 365 그룹에 대 한 감사 된 작업). 사서함은 사용자 지정할 수 없습니다.

다음과 같은 두 가지 방법을 사용 하 여 사서함 작업을 지정할 수 있습니다.

- *교체* (덮어쓰기)이 구문을 `action1,action2,...actionN`사용 하 여 기존 사서함 작업을 덮어씁니다.

- 다음 `@{Add="action1","action2",..."actionN"}` 구문을 사용 하 여 기존 값에 영향을 주지 않고 사서함 작업을 `@{Remove="action1","action2",..."actionN"}` *추가 하거나 제거* 합니다.

이 예에서는 Gabriela Laureano "사서함에 대 한 관리자 사서함 작업을 소프트 삭제 및 하드 삭제의 기본 동작을 덮어쓰는 방법으로 변경 합니다.

```
Set-Mailbox -Identity "Gabriela Laureano" -AuditAdmin HardDelete,SoftDelete
```

이 예에서는 사서함 laura@contoso.onmicrosoft.com에 MailboxLogin owner 작업을 추가 합니다.

```
Set-Mailbox -Identity laura@contoso.onmicrosoft.com -AuditOwner @{Add="MailboxLogin"}
```

이 예에서는 팀 토론 사서함에 대 한 MoveToDeletedItems 대리인 작업을 제거 합니다.

```
Set-Mailbox -Identity "Team Discussion" -AuditDelegate @{Remove="MoveToDeletedItems"}
```

사용 하는 방법에 관계 없이 사용자 사서함 또는 공유 사서함에 대해 감사 된 사서함 작업을 사용자 지정 하면 다음과 같은 결과가 나타납니다.

- 사용자 지정한 로그온 유형의 경우 감사 된 사서함 작업은 더 이상 Microsoft에서 관리 되지 않습니다.

- 사용자 지정한 로그온 유형이 [앞에서 설명한](#verify-that-default-mailbox-actions-are-being-logged-for-each-logon-type)대로 사서함의 *defaultauditset* 속성 값에 더 이상 표시 되지 않습니다.

### <a name="restore-the-default-mailbox-actions"></a>기본 사서함 작업 복원

사용자 사서함 또는 공유 사서함에 대해 감사 되는 사서함 작업을 사용자 지정한 경우 다음 구문을 사용 하 여 하나 또는 모든 로그온 유형의 기본 사서함 작업을 복원할 수 있습니다.

```
Set-Mailbox -Identity <MailboxIdentity> -DefaultAuditSet <Admin | Delegate | Owner>
```

여러 *Defaultauditset* 값을 쉼표로 구분 하 여 지정할 수 있습니다.

**참고**: 다음 절차는 Office 365 그룹 사서함에는 적용 되지 않으며 [여기](#mailbox-actions-for-office-365-group-mailboxes)에 설명 된 기본 작업으로 제한 됩니다.

이 예에서는 사서함 mark@contoso.onmicrosoft.com의 모든 로그온 유형에 대해 감사 된 기본 사서함 작업을 복원 합니다.

```
Set-Mailbox -Identity mark@contoso.onmicrosoft.com -DefaultAuditSet Admin,Delegate,Owner
```

이 예에서는 사서함 chris@contoso.onmicrosoft.com의 관리 로그온 유형에 대해 감사 된 기본 사서함 작업을 복원 하지만 대리인 및 소유자 로그온 유형에 대해 사용자 지정 된 감사 사서함 작업은 그대로 둡니다.

```
Set-Mailbox -Identity chris@contoso.onmicrosoft.com -DefaultAuditSet Admin
```

로그온 유형에 대해 기본적으로 감사 된 사서함 작업을 복원 하면 다음과 같은 결과가 나타납니다.

- 현재 사서함 작업 목록은 로그온 유형의 기본 사서함 작업으로 대체 됩니다.

- Microsoft에서 릴리스한 모든 새 사서함 작업은 로그온 유형에 대 한 감사 된 작업 목록에 자동으로 추가 됩니다.

- 사서함에 대 한 *Defaultauditset* 속성 값이 복원 된 로그온 유형을 포함 하도록 업데이트 됩니다.

## <a name="turn-off-mailbox-auditing-on-by-default-for-your-organization"></a>조직에 대해 기본적으로 사서함 감사 해제

Exchange Online PowerShell에서 다음 명령을 실행 하 여 전체 조직에 대해 기본적으로 사서함 감사를 해제할 수 있습니다.

```
Set-OrganizationConfig -AuditDisabled $true
```

기본적으로 사서함 감사를 해제 하면 다음과 같은 결과가 나타납니다.

- 조직에서 사서함 감사를 사용 하지 않도록 설정 합니다.

- 기본적으로 사서함 감사를 사용 하지 않도록 설정한 시간부터 사서함에서 감사가 사용 되도록 설정 된 경우에도 사서함 작업이 감사 되지 않습니다 (사서함의 *Auditenabled* 속성이 **True**).

- 사서함 감사는 새 사서함에 대해 사용 하도록 설정 되지 않으며 새 사서함 이나 기존 우편함에서 *Auditenabled* 속성을 **True** 로 설정 하면 무시 됩니다.

- **Get-mailboxauditbypassassociation** cmdlet을 사용 하 여 구성 되는 모든 사서함 감사 바이패스 연결 설정은 무시 됩니다.

- 기존 사서함 감사 레코드는 레코드에 대 한 감사 로그 기간 제한이 만료 될 때까지 유지 됩니다.

### <a name="turn-on-mailbox-auditing-on-by-default"></a>기본적으로 사서함 감사 켜기

조직에 대 한 사서함 감사를 다시 설정 하려면 Exchange Online PowerShell에서 다음 명령을 실행 합니다.

```
Set-OrganizationConfig -AuditDisabled $false
```

## <a name="bypass-mailbox-audit-logging"></a>사서함 감사 로깅 바이패스

현재 조직에서 사서함 감사가 기본적으로 설정 된 경우에는 특정 사서함에 대해 사서함 감사를 사용 하지 않도록 설정할 수 없습니다. 예를 들어 *Auditenabled* mailbox 속성을 **False** 로 설정 하는 것은 무시 됩니다.

그러나 Exchange Online PowerShell에서 **get-mailboxauditbypassassociation** cmdlet을 사용 하 여 작업이 수행 되는 위치에 관계 없이 지정 된 사용자의 *모든* 사서함 작업이 로깅되지 않도록 할 수 있습니다. 예를 들면 다음과 같습니다.

- 바이패스 된 사용자가 수행한 사서함 소유자 작업은 로깅되지 않습니다.

- 공유 사서함을 포함 하 여 다른 사용자의 사서함에 대 한 바이패스 된 사용자가 수행 하는 위임 작업은 기록 되지 않습니다.

- 바이패스 된 사용자가 수행한 관리 작업은 로깅되지 않습니다.

특정 사용자에 대 한 사서함 감사 로깅을 무시 하려면 MailboxIdentity \<\> 을 사용자의 이름, 전자 메일 주소, 별칭 또는 upn (사용자 계정 이름)으로 바꾸고 다음 명령을 실행 합니다.

```
Set-MailboxAuditBypassAssociation -Identity <MailboxIdentity> -AuditByPassEnabled $true
```

지정한 사용자에 대해 감사가 무시 되는지 확인 하려면 다음 명령을 실행 합니다.

```
Get-MailboxAuditBypassAssociation -Identity <MailboxIdentity> | Format-List AuditByPassEnabled
```

**True** 값은 사용자에 대해 사서함 감사 로깅이 무시 됨을 나타냅니다.

## <a name="more-information"></a>추가 정보

- 기본적으로 사서함 감사 로그 레코드는 삭제 되기 전에 90 일 동안 보존 됩니다. Exchange Online PowerShell에서 **설정 된 사서함** Cmdlet의 *Auditlogagelimit* 매개 변수를 사용 하 여 감사 로그 레코드의 보존 기간을 변경할 수 있습니다. 그러나이 값을 높이면 Microsoft 365 감사 로그에서 90 일 보다 오래 된 이벤트를 검색할 수 없습니다.

  보존 기간을 늘릴 경우 Exchange Online PowerShell에서 [search-mailboxauditlog](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-audit/search-mailboxauditlog) cmdlet을 사용 하 여 사용자의 사서함 감사 로그에서 90 일 보다 오래 된 레코드를 검색 해야 합니다.

- 조직에 대해 기본적으로 사서함 감사를 수행 하기 전에 사서함에 대 한 *Auditlogagelimit* 속성을 변경한 경우 사서함의 기존 감사 로그 보존 기간은 변경 되지 않습니다. 즉, 기본적으로 사서함을 감사 하는 경우 사서함 감사 레코드의 현재 보존 기간에는 영향을 주지 않습니다.

- Office 365 그룹 사서함에서 *Auditlogagelimit* 값을 변경 하려면 `-GroupMailbox` **Set-mailbox** 명령에 스위치를 포함 해야 합니다.

- 사서함 감사 로그 레코드는 각 사용자의 사서함에 있는 복구할 수 있는 항목 폴더에 있는 하위 폴더 ( *감사*)에 저장 됩니다. 사서함 감사 레코드 및 복구할 수 있는 항목 폴더에 대해서는 다음 사항을 염두에 두어야 합니다.

  - 사서함 감사 레코드는 복구 가능한 항목 폴더의 저장소 할당량을 기준으로 계산 됩니다 (기본적으로 30GB) (경고 할당량은 20gb). 저장소 할당량은 다음과 같은 경우 자동으로 100 GB (90 GB 경고 할당량 포함)로 증가 합니다.

    - 보류가 사서함에 저장 됩니다.

    - 사서함이 준수 센터의 보존 정책에 할당 됩니다.

  - 또한 사서함 감사 레코드는 [복구 가능한 항목 폴더에 대 한 폴더 제한](https://docs.microsoft.com/office365/servicedescriptions/exchange-online-service-description/exchange-online-limits#mailbox-folder-limits)에 대해서도 계산 됩니다. 감사 하위 폴더에는 최대 300만 개의 항목을 저장할 수 있습니다.

    > [!NOTE]
    > 기본적으로 사서함 감사가 복구 가능한 항목 폴더의 저장소 할당량 또는 폴더 제한에 영향을 주는 것은 아닙니다.

    - Exchange Online PowerShell에서 다음 명령을 실행 하 여 복구 가능한 항목 폴더의 감사 하위 폴더에 있는 항목의 크기 및 수를 표시할 수 있습니다.

      ```
      Get-MailboxFolderStatistics -Identity <MailboxIdentity> -FolderScope RecoverableItems | Where-Object {$_.Name -eq 'Audits'} | Format-List FolderPath,FolderSize,ItemsInFolder
      ```

    - 복구 가능한 항목 폴더의 감사 로그 레코드에 직접 액세스할 수는 없습니다. 대신 **search-mailboxauditlog** cmdlet을 사용 하거나 Microsoft 365 감사 로그를 검색 하 여 사서함 감사 레코드를 찾아서 확인 합니다.

- 사서함이 보류 중이거나 준수 센터의 보존 정책에 할당 된 경우에는 사서함의 *Auditlogagelimit* 속성에 정의 된 기간 동안 감사 로그 레코드가 여전히 보존 됩니다 (기본적으로 90 days). 보류 중인 사서함에 대해 감사 로그 레코드를 더 오랫동안 보존 하려면 사서함의 *Auditlogagelimit* 값을 늘려야 합니다.
