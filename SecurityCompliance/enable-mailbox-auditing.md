---
title: Office 365에서 사서함 감사 사용
ms.author: markjjo
author: markjjo
manager: laurawi
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MOE150
- MET150
ms.assetid: aaca8987-5b62-458b-9882-c28476a66918
description: Office 365에서는 사서함 소유자, 대리인 및 관리자의 사서함 액세스에 대 한 사서함 감사 로깅을 설정할 수 있습니다. 기본적으로 Office 365의 사서함 감사는 설정 되어 있지 않습니다. 사서함에 대해 사서함 감사 로깅을 사용 하도록 설정한 후에는 사서함에 대해 수행 된 작업에 대 한 Office 365 감사 로그를 검색할 수 있습니다.
ms.openlocfilehash: bb110e95d27feb8ae82b62803d218a2b38528692
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30214608"
---
# <a name="enable-mailbox-auditing-in-office-365"></a>Office 365에서 사서함 감사 사용
  
Office 365에서는 사서함 소유자, 대리인 및 관리자의 사서함 액세스에 대 한 사서함 감사 로깅을 설정할 수 있습니다. 기본적으로 Office 365의 사서함 감사는 설정 되어 있지 않습니다. 즉, 사서함 활동에 대 한 Office 365 감사 로그를 검색 하면 결과에 사서함 감사 이벤트가 나타나지 않습니다. 그러나 사용자 사서함에 대 한 사서함 감사 로깅을 설정한 후에는 감사 로그에서 사서함 활동을 검색할 수 있습니다. 또한 사서함 감사 로깅이 설정 되 면 기본적으로 관리자, 대리인 및 소유자가 수행 하는 일부 작업이 기록 됩니다. 추가 작업을 로그 한 다음 검색 하려면 3 단계를 참조 하십시오.

## <a name="before-you-begin"></a>시작하기 전에
  
- 사서함 감사 로깅을 사용 하도록 설정 하려면 Exchange Online PowerShell을 사용 해야 합니다. Office 365 보안 &amp; 및 준수 센터 또는 Exchange 관리 센터는 사용할 수 없습니다.
    
- Microsoft 팀의 Office 365 그룹 또는 팀에 연결 된 사서함에 대해 사서함 감사 로깅을 사용 하도록 설정할 수 없습니다.
    
- 사용자의 사서함에 대해 모든 액세스 권한이 할당된 관리자는 대리인으로 간주됩니다.
  
## <a name="step-1-connect-to-exchange-online-powershell"></a>1 단계: Exchange Online PowerShell에 연결

1. 로컬 컴퓨터에서 Windows PowerShell을 열고 다음 명령을 실행합니다.
   
    ```
    $UserCredential = Get-Credential
    ```

2. **Windows PowerShell 자격 증명 요청** 대화 상자에서 Office 365 전역 관리자 계정의 사용자 이름 및 암호를 입력한 다음 **확인**을 클릭합니다.
    
3. 다음 명령을 실행합니다.
    
    ```
    $Session = New-PSSession -ConfigurationName Microsoft.Exchange -ConnectionUri https://outlook.office365.com/powershell-liveid/ -Credential $UserCredential -Authentication Basic -AllowRedirection
    ```

3. 다음 명령을 실행합니다.

    ```
    Import-PSSession $Session
    ```
   
4. Exchange Online 조직에 연결 되었는지 확인 하려면 다음 명령을 실행 하 여 조직의 모든 사서함 목록을 가져옵니다.
    
    ```
    Get-Mailbox
    ```
  
자세한 내용을 보거나 exchange online 조직에 연결 하는 데 문제가 있는 경우 [원격 PowerShell을 사용 하 여 exchange online에 연결](https://go.microsoft.com/fwlink/p/?LinkId=517283)을 참조 하세요.
  
## <a name="step-2-enable-mailbox-audit-logging"></a>2단계: 사서함 감사 로깅 사용

Exchange Online 조직에 연결한 후 PowerShell을 사용 하 여 사서함에 대 한 사서함 감사 로깅을 사용 하도록 설정 합니다. 또는 조직의 모든 사서함에 대해 사서함 감사를 사용 하도록 설정할 수 있습니다.
  
이 예에서는 Pilar Pinilla의 사서함에 대해 사서함 감사 로깅을 사용 하도록 설정 합니다.
  
```
Set-Mailbox -Identity "Pilar Pinilla" -AuditEnabled $true
```

아래 예에서는 조직의 모든 사용자 사서함에 대한 사서함 감사 로깅을 사용하도록 설정합니다.
  
```
Get-Mailbox -ResultSize Unlimited -Filter {RecipientTypeDetails -eq "UserMailbox"} | Set-Mailbox -AuditEnabled $true
```
  
## <a name="step-3-specify-owner-actions-to-audit"></a>3단계: 감사할 소유자 작업 지정

사서함에 대 한 감사를 사용 하도록 설정 하면 사서함 소유자가 수행 하는 일부 작업은 기본적으로 감사 됩니다. 감사를 위해 다른 소유자 작업을 지정 해야 합니다. [사서함 감사 작업](#mailbox-auditing-actions) 섹션의 표 및 기본적으로 기록 되는 소유자 작업에 대 한 설명과 감사할 수 있는 기타 작업에 대 한 설명을 참조 하십시오. 
  
이 예에서는 Pilar Pinilla의 사서함에 대 한 사서함 감사에 **MailboxLogin** 및 **하드 삭제** 소유자 작업을 추가 합니다. 이 예에서는이 사서함에 대해 사서함 감사가 이미 사용 하도록 설정 되어 있다고 가정 합니다. 

```
Set-Mailbox "Pilar Pinilla" -AuditOwner @{Add="MailboxLogin","HardDelete"}
```

이 예에서는 사서함에서 사서함 감사 로깅을 사용 하도록 설정 하 고 사서함 소유자가 수행한 **MailboxLogin** 작업만 기록 되도록 지정 합니다. 이 예제에서는 기본 updatefolderpermissions 작업을 덮어씁니다. 
  
```
Set-Mailbox "Don Hall" -AuditEnabled $true -AuditOwner MailboxLogin
```
   
이 예에서는 조직의 모든 사서함에 **MailboxLogin**, **하드 삭제**및 **소프트 삭제** 소유자 작업을 추가 합니다. 이 예에서는 모든 사서함에 대해 사서함 감사가 이미 사용 하도록 설정 되어 있다고 가정 합니다. 
  
```
Get-Mailbox -ResultSize Unlimited -Filter {RecipientTypeDetails -eq "UserMailbox"} | Set-Mailbox -AuditOwner @{Add="MailboxLogin","HardDelete","SoftDelete"}
```
  
## <a name="how-do-you-know-this-worked"></a>작동 여부는 어떻게 확인하나요?

사서함에 대한 사서함 감사 로깅이 사용하도록 설정되었는지 확인하려면 **Get-Mailbox** cmdlet을 사용하여 해당 사서함에 대한 감사 설정을 검색합니다. 
  
아래 예에서는 강진영에 대한 감사 설정을 검색합니다.

```
Get-Mailbox "Pilar Pinilla"| FL Audit*
```
   
아래 예에서는 조직 내 모든 사용자 사서함에 대한 감사 설정을 검색합니다.

```
Get-Mailbox -ResultSize Unlimited -Filter {RecipientTypeDetails -eq "UserMailbox"} | FL Name,Audit*
```
   
**auditenabled** 속성의 **True** 값은 사서함 감사 로깅이 사용 하도록 설정 되어 있는지 확인 합니다. 
    
## <a name="mailbox-auditing-actions"></a>사서함 감사 작업
  
다음 표에는 사서함 감사 로깅에서 로깅할 수 있는 작업이 나와 있습니다. 이 표에는 다른 사용자 로그온 유형에 대해 기록 가능한 작업에 대 한 정보가 나와 있습니다. 이 표에서 **아니요** 는 해당 로그온 유형에 대해 작업을 로그할 수 없음을 나타냅니다. 별표 ( **\*** )는 사서함에 대해 사서함 감사 로깅을 사용 하는 경우 작업이 기본적으로 기록 됨을 나타냅니다. 
  
|**작업**|**설명**|**관리자**|**대리인\*\*\***|**소유자**|
|:-----|:-----|:-----|:-----|:-----|
|**복사** <br/> |메시지가 다른 폴더에 복사되었습니다.  <br/> |예  <br/> |아니요  <br/> |아니요  <br/> |
|**만들기** <br/> |사서함의 일정, 연락처, 메모 또는 작업 폴더에 항목이 만들어집니다. 예를 들어 새 모임 요청이 만들어집니다. 메시지 만들기, 보내기 또는 받기는 감사 되지 않습니다. 또한 사서함 폴더를 만드는 것은 감사 되지 않습니다.  <br/> |예\*  <br/> |예\*  <br/> |예  <br/> |
|**FolderBind** <br/> |사서함 폴더에 액세스했습니다. 관리자 또는 대리인이 사서함을 열 때에도 작업이 기록됩니다.  <br/> |예  <br/> |예\*\*  <br/> |아니요  <br/> |
|**HardDelete** <br/> |메시지가 복구 가능한 항목 폴더에서 제거되었습니다.  <br/> |예\*  <br/> |예\*  <br/> |예  <br/> |
|**MailboxLogin** <br/> |사용자가 자신의 사서함에 로그인했습니다.  <br/> |아니요  <br/> |아니요  <br/> |예  <br/> |
|**대해 수행한 messagebind** <br/> |메시지가 미리 보기 창에 표시되거나 열렸습니다.  <br/> |예  <br/> |아니요  <br/> |아니요  <br/> |
|**Move** <br/> |메시지가 다른 폴더로 이동했습니다.  <br/> |예  <br/> |예   <br/> |예   <br/> |
|**MoveToDeletedItems** <br/> |메시지가 삭제되어 지운 편지함 폴더로 이동되었습니다.  <br/> |예\*  <br/> |예\*  <br/> |예  <br/> |
|**SendAs** <br/> |메시지가 SendAs 권한을 사용하여 전송되었습니다. 즉 사서함 소유자가 보낸 것처럼 보이도록 하여 다른 사용자가 메시지를 보냈습니다.  <br/> |예\*  <br/> |예\*  <br/> |아니요  <br/> |
|**SendOnBehalf** <br/> |메시지가 SendOnBehalf 권한을 사용하여 전송되었습니다. 즉 다른 사용자가 사서함 소유자 대신에 메시지를 보냈습니다. 받는 사람은 메시지를 대신 보낸 사용자와 해당 메시지를 실제로 보낸 사용자를 메시지에서 확인할 수 있습니다.  <br/> |예\*  <br/> |예\*  <br/> |아니요  <br/> |
|**SoftDelete** <br/> |메시지가 지운 편지함 폴더에서 삭제되어가 영구적으로 삭제되었습니다. 소프트 삭제된 항목이 복구 가능한 항목 폴더로 이동됩니다.  <br/> |예\*  <br/> |예\*  <br/> |예  <br/> |
|**업데이트** <br/> |메시지 또는 해당 속성이 변경되었습니다.  <br/> |예\*  <br/> |예\*  <br/> |예  <br/> |
|**UpdateCalendarDelegation** <br/> |일정 위임이 사서함에 할당 되었습니다. 일정 위임 같은 조직에서 사서함 소유자의 일정을 관리 하는 다른 사람에 게 제공 합니다.  <br/> |예\*  <br/> |아니요  <br/> |예\*  <br/> |
|**updatefolderpermissions 작업이 로깅됩니다** <br/> |폴더 사용 권한이 변경 되었습니다. 폴더 사용 권한은 조직에서 사서함의 폴더에 액세스할 수 있는 사용자와 해당 폴더에 있는 메시지를 제어 합니다.  <br/> |예\*  <br/> |예\*  <br/> |예\*  <br/> |
|**UpdateInboxRules** <br/> |받은 편지함 규칙이 추가, 제거 또는 변경 된 경우 받은 편지함 규칙은 지정 된 조건에 따라 사용자의 받은 편지함에서 메시지를 처리 하 고, 메시지를 지정 된 폴더로 이동 하거나 메시지를 삭제 하는 것과 같이 규칙의 조건이 충족 될 때 작업을 수행 하는 데 사용 됩니다.  <br/> |예\*  <br/> |예\*  <br/> |예\*  <br/> |
   
> [!NOTE]
> <sup>\*</sup>사서함에 대 한 감사를 사용 하도록 설정 된 경우 기본적으로 감사 됩니다.<br/><br/>  <sup>\*\*</sup>대리인에 의해 수행 된 폴더 바인드 작업에 대 한 항목이 통합 됩니다. 24 시간 내에 개별 폴더 액세스에 대 한 하나의 로그 항목이 생성 됩니다.<br/><br/><sup>\*\*\*</sup>사용자의 사서함에 대 한 모든 액세스 권한이 할당 된 관리자는 대리인 사용자로 간주 됩니다. 
  
특정 유형의 사서함 작업을 더 이상 감사할 필요가 없는 경우 사서함의 감사 로깅 구성을 수정 하 여 해당 작업을 사용 하지 않도록 설정 해야 합니다. 기존 로그 항목은 감사 로그 항목의 보존 기간 제한에 도달할 때까지 제거 되지 않습니다. 감사 로그 항목의 보존 기간에 대 한 자세한 내용은 [Search the audit log in the Office 365 Security & 준수 센터](search-the-audit-log-in-security-and-compliance.md#before-you-begin)의 "시작 하기 전에" 섹션을 참조 하십시오.
  
## <a name="more-infotab"></a>[추가 정보](#tab/)
  
- Office 365 감사 로그를 사용 하 여 로깅된 사서함 활동을 검색 합니다. 특정 사용자 사서함에 대 한 활동을 검색할 수 있습니다. 다음 스크린샷에서는 Office 365 감사 로그에서 검색할 수 있는 사서함 활동 목록을 보여 줍니다. 이러한 활동은이 항목의 "사서함 감사 작업" 섹션에 설명 된 것과 동일한 작업입니다.
    
    ![작업 드롭다운 목록에서 "Exchange 사서함 활동"을 선택 하 여 Office 365 감사 로그에서 사서함 감사 작업을 검색할 수 있습니다.](media/fadc34f8-9de2-4688-8b1a-bc5540e69a23.png)
  
    다음 표에서는 검색 가능한 각 사서함 활동에 대해 설명 하 고 해당 사서함 감사 작업을 보여 줍니다.
    
    |**감사 로그의 활동**|**사서함 감사 작업**|
    |:-----|:-----|
    |만든 사서함 항목  <br/> |만들기  <br/> |
    |다른 폴더로 복사한 메시지  <br/> |복사  <br/> |
    |사용자가 사서함에 로그인 되어 있음  <br/> |MailboxLogin  <br/> |
    |"대신 보내기" 권한을 사용 하 여 보낸 메시지  <br/> |SendOnBehalf  <br/> |
    |사서함에서 메시지 제거  <br/> |HardDelete  <br/> |
    |지운 편지함 폴더로 메시지 이동  <br/> |MoveToDeletedItems  <br/> |
    |메시지를 다른 폴더로 이동  <br/> |이동  <br/> |
    |메시지를 다른 사람 이름으로 보내기 권한을 사용 하 여 보냄  <br/> |SendAs  <br/> |
    |업데이트 된 메시지  <br/> |업데이트  <br/> |
    |지운 편지함 폴더에서 삭제 된 메시지  <br/> |SoftDelete  <br/> |
    |폴더에 대 한 사용 권한 추가  <br/> |updatefolderpermissions 작업이 로깅됩니다  <br/> |
    |폴더의 수정 된 사용 권한  <br/> |updatefolderpermissions 작업이 로깅됩니다  <br/> |
    |폴더에서 사용 권한을 제거 했습니다.  <br/> |updatefolderpermissions 작업이 로깅됩니다  <br/> |
    |일정 폴더에 대 한 대리인 액세스 권한이 있는 사용자 추가 또는 제거  <br/> |UpdateCalendarDelegation  <br/> |
   
    **추가 된 대리인 사서함 사용 권한** 및 **제거 된 대리인 사서함 사용 권한** 작업은 이전 스크린샷에 표시 되는 사서함 감사 작업과 관련이 없습니다. 관리자가 FullAccess 사서함 사용 권한을 할당 하거나 제거 했는지를 나타냅니다. 
    
    office 365 감사 로그에 대 한 자세한 내용은 [office 365 보안 &amp; 및 준수 센터에서 감사 로그 검색](search-the-audit-log-in-security-and-compliance.md)을 참조 하십시오.
    
- 다음 시나리오에서는 관리자만 사서함에 액세스한다고 간주합니다.
    
  - Exchange Online의 원본 위치 eDiscovery 또는 Office 365의 콘텐츠 검색은 사서함을 검색 하는 데 사용 됩니다.
    
  - [Microsoft Exchange Server MAPI 편집기](https://go.microsoft.com/fwlink/p/?linkId=204086)를 사용하여 사서함에 액세스합니다. 
    
- 사서함 감사 로깅을 사용하도록 설정할 때 로그온 유형(관리자, 대리인 또는 소유자)별로 기록할 사용자 작업(예: 메시지 액세스, 이동 또는 삭제)도 지정할 수 있습니다. 
    
- 사서함 감사 로깅을 사용하도록 설정하지 않으려면 다음 명령을 실행합니다.

  ```
  Set-Mailbox -Identity <identity of mailbox> -AuditEnabled $false
   ```

- **사서함** cmdlet을 실행할 때 각 사용자 유형에 대해 감사 되는 작업은 표시 되지 않습니다. 그러나 다음 명령을 실행 하 여 특정 사용자 로그온 유형에 대해 감사 된 모든 작업을 표시할 수 있습니다. 

    ```
    Get-Mailbox <identity of mailbox> | Select-Object -ExpandProperty AuditAdmin
    ```

    ```
    Get-Mailbox <identity of mailbox> | Select-Object -ExpandProperty AuditDelegate
    ```

    ```
    Get-Mailbox <identity of mailbox> | Select-Object -ExpandProperty AuditOwner
    ```

- 사서함 감사 로그를 내보내고 한 명 이상의 사용자에 대해 포함할 항목을 지정할 수도 있습니다. 보고서 및 감사 로그의 각 항목에는 해당 작업을 수행한 사용자, 수행 된 작업 및 작업 성공 여부에 대 한 정보가 포함 됩니다. 자세한 내용은 [Export mailbox audit logs](https://go.microsoft.com/fwlink/p/?LinkID=404104)를 참조 하십시오.
