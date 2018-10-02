---
title: Office 365에서 사서함 감사 사용
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MOE150
- MET150
ms.assetid: aaca8987-5b62-458b-9882-c28476a66918
description: Office 365에서 사서함 감사 로깅 사서함 소유자, 대리인 및 관리자의 사서함 액세스를 기록 하도록 켤 수 있습니다. 기본적으로 Office 365에서 사서함 감사 설정 되지 않은 합니다. 사서함에 대 한 로깅 사서함 감사를 사용 하도록 설정한 후에 사서함에 수행 하는 작업에 대 한 Office 365 감사 로그를 검색할 수 있습니다.
ms.openlocfilehash: 9952cc94fe48e289e6eaf8de665a82cb3da4746d
ms.sourcegitcommit: b6473cd6ba3f9ac79dc6a2040fc148020dfbe464
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/02/2018
ms.locfileid: "25358387"
---
# <a name="enable-mailbox-auditing-in-office-365"></a>Office 365에서 사서함 감사 사용
  
Office 365에서 사서함 감사 로깅 사서함 소유자, 대리인 및 관리자의 사서함 액세스를 기록 하도록 켤 수 있습니다. 기본적으로 Office 365에서 사서함 감사 설정 되지 않은 합니다. 즉, 이벤트를 감사 해야 사서함은 사서함 활동에 대 한 Office 365 감사 로그를 검색 하는 경우 결과에 나타나지 않습니다. 하지만 사용자 사서함에 대 한 로깅 사서함 감사를 설정한 후 사서함 활동에 대 한 감사 로그를 검색할 수 있습니다. 또한 사서함 감사 로깅을 사용 대리인, 관리자가 수행 된 일부 작업에 및 소유자가 기본적으로 기록 됩니다. 로그 (한 다음 검색)에 추가 작업 단계 3을 참조 하십시오.

## <a name="before-you-begin"></a>시작하기 전에
  
- Exchange Online PowerShell을 사용 하 여 사서함을 사용 하도록 설정 해야하는 로깅 감사 합니다. Office 365 보안을 사용할 수 없습니다 &amp; 준수 센터 또는 Exchange 관리 센터입니다.
    
- 사서함 감사 사서함에 대해 로깅을 사용 하도록 설정 하면 사서함 및 특정 관리자와 대리인이 작업에 대 한 액세스는 기본적으로 기록 됩니다. 사서함 소유자가 취한 조치를 기록 하려면 어떤 소유자 동작을 감사할 사용자를 지정 해야 합니다. 사서함 감사 로깅 후 로깅되는 작업 목록의 사용 하도록 설정 하 고는 동작이 각 유형의 사용자 로그온에 사용할 수 있는 참조를 "추가 정보" 섹션을 참조 하십시오.
    
- 사서함 감사는 Office 365 그룹 또는 팀이 Microsoft에서 팀과 관련 된 사서함에 대 한 로깅을 활성화할 수 없습니다.
    
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
   
4. Exchange Online 조직에 연결 하려는 있는지를 확인 하려면 조직에 있는 모든 사서함의 목록을 가져오려면 다음 명령을 실행 합니다.
    
    ```
    Get-Mailbox
    ```
  
자세한 내용은 하거나 Exchange Online 조직에 연결할 때 문제가 있으면 [원격 PowerShell을 사용 하는 Exchange Online에 연결](https://go.microsoft.com/fwlink/p/?LinkId=517283)을 참조 하십시오.
  
## <a name="step-2-enable-mailbox-audit-logging"></a>2단계: 사서함 감사 로깅 사용

Exchange Online 조직에 연결한 후 PowerShell을 사용 하 여 사서함에 대 한 로깅 사서함 감사를 사용 하도록 설정 합니다. 또는 조직에서 모든 사서함에 대 한 사서함 감사를 설정할 수 있습니다.
  
사서함 감사 Pilar Pinilla의 사서함에 대 한 로깅을 설정 하는이 예제입니다.
  
```
Set-Mailbox -Identity "Pilar Pinilla" -AuditEnabled $true
```

아래 예에서는 조직의 모든 사용자 사서함에 대한 사서함 감사 로깅을 사용하도록 설정합니다.
  
```
Get-Mailbox -ResultSize Unlimited -Filter {RecipientTypeDetails -eq "UserMailbox"} | Set-Mailbox -AuditEnabled $true
```
  
## <a name="step-3-specify-owner-actions-to-audit"></a>3단계: 감사할 소유자 작업 지정

사서함에 대 한 감사를 사용 하면 사서함 소유자가 수행한 하나만 동작 ( **UpdateFolderPermissions** ) 기본적으로 감사 됩니다. 감사 하는 기타 소유자 작업을 지정 해야 합니다. 목록 및 설명은 감사할 수 있는 소유자 작업에 대 한 "사서함 작업" 섹션의 표를 참조 합니다. 
  
이 예에서는 Pilar Pinilla의 사서함에 대 한 감사 사서함에 **MailboxLogin** 및 **HardDelete** 소유자 작업을 추가 합니다. 이 예제는 사서함 감사 기능이 이미 활성화 된이 사서함에 대 한 가정 합니다. 

```
Set-Mailbox "Pilar Pinilla" -AuditOwner @{Add="MailboxLogin","HardDelete"}
```

이 예에서는 사서함 감사 Don 홀 사서함에 대 한 로깅을 사용 하도록 설정 하 고 사서함 소유자에 의해 수행 되는 **MailboxLogin** 작업만 기록 됩니다 지정 합니다. Note이 예제에서는 기본 UpdateFolderPermissions 작업을 덮어씁니다. 
  
```
Set-Mailbox "Don Hall" -AuditEnabled $true -AuditOwner MailboxLogin
```
   
조직에서 모든 사서함에 **MailboxLogin**, **HardDelete**및 **SoftDelete** 소유자 작업을 추가 하는이 예제입니다. 이 예제는 사서함 감사 기능이 이미 활성화 된 모든 사서함에 대 한 가정 합니다. 
  
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
   
**AuditEnabled** 속성의 **True** 값을 확인 해당 사서함 감사 로깅을 사용 하도록 설정 합니다. 
    
## <a name="mailbox-auditing-actions"></a>사서함 감사 작업
  
다음 표에서 사서함으로 기록 될 수 있는 작업이 나와 감사 로깅. 표에 서로 다른 사용자 로그온 유형에 대 한 동작을 기록할 수 있습니다를 포함 합니다. 테이블을 **No** 해당 로그온 형식에 대 한 동작을 기록할 수 없는 나타냅니다. 별표 ( **\*** )를 나타냅니다 사서함에 대해 활성화 되어 사서함 감사 로깅 때 기본적으로는 작업 기록 됩니다. 앞서 설명한 것 처럼 사서함 감사 기능을 설정 하면 기본적으로 감사 되는 유일한 소유자 작업 UpdateFolderPermissions 됩니다. 사서함 소유자가 수행 하는 다른 작업을 기록 하려면 감사 하기 위한 추가 소유자 작업을 지정 해야 합니다. 이 작업을 수행 하려면이 항목의 [3 단계를](#step-3-specify-owner-actions-to-audit) 참조 하십시오. 
  
|**작업**|**설명**|**Admin**|**대리인\*\*\***|**소유자**|
|:-----|:-----|:-----|:-----|:-----|
|**복사** <br/> |메시지가 다른 폴더에 복사되었습니다.  <br/> |예  <br/> |아니요  <br/> |아니요  <br/> |
|**만들기** <br/> |사서함, 일정, 연락처, 메모 또는 작업 폴더에서 항목을 만들 예, 새 모임 요청을 생성 됩니다. 참고는 만들기, 보내기 또는 메시지를 받는 감사 되지 않습니다. 또한 사서함 폴더 만들기 (영문)을 감사 하지 않습니다.  <br/> |예\*  <br/> |예\*  <br/> |예  <br/> |
|**FolderBind** <br/> |사서함 폴더에 액세스했습니다. 관리자 또는 대리인이 사서함을 열 때에도 작업이 기록됩니다.  <br/> |예  <br/> |예\*\*  <br/> |아니요  <br/> |
|**HardDelete** <br/> |메시지가 복구 가능한 항목 폴더에서 제거되었습니다.  <br/> |예\*  <br/> |예\*  <br/> |예  <br/> |
|**MailboxLogin** <br/> |사용자가 자신의 사서함에 로그인했습니다.  <br/> |아니요  <br/> |아니요  <br/> |예  <br/> |
|**MessageBind** <br/> |메시지가 미리 보기 창에 표시되거나 열렸습니다.  <br/> |예  <br/> |아니요  <br/> |아니요  <br/> |
|**Move** <br/> |메시지가 다른 폴더로 이동했습니다.  <br/> |예  <br/> |예  <br/> |예  <br/> |
|**MoveToDeletedItems** <br/> |메시지가 삭제되어 지운 편지함 폴더로 이동되었습니다.  <br/> |예\*  <br/> |예\*  <br/> |예  <br/> |
|**SendAs** <br/> |메시지가 SendAs 권한을 사용하여 전송되었습니다. 즉 사서함 소유자가 보낸 것처럼 보이도록 하여 다른 사용자가 메시지를 보냈습니다.  <br/> |예\*  <br/> |예\*  <br/> |아니요  <br/> |
|**SendOnBehalf** <br/> |메시지가 SendOnBehalf 권한을 사용하여 전송되었습니다. 즉 다른 사용자가 사서함 소유자 대신에 메시지를 보냈습니다. 받는 사람은 메시지를 대신 보낸 사용자와 해당 메시지를 실제로 보낸 사용자를 메시지에서 확인할 수 있습니다.  <br/> |예\*  <br/> |예\*  <br/> |아니요  <br/> |
|**SoftDelete** <br/> |메시지가 지운 편지함 폴더에서 삭제되어가 영구적으로 삭제되었습니다. 소프트 삭제된 항목이 복구 가능한 항목 폴더로 이동됩니다.  <br/> |예\*  <br/> |예\*  <br/> |예  <br/> |
|**업데이트** <br/> |메시지 또는 해당 속성이 변경되었습니다.  <br/> |예\*  <br/> |예\*  <br/> |예  <br/> |
|**UpdateCalendarDelegation** <br/> |일정 위임 사서함에 할당 합니다. 일정 위임에 사서함 소유자의 일정을 관리 하는 동일한 조직 권한을에서 다른 사용자를 제공 합니다.  <br/> |예\*  <br/> |아니요  <br/> |예\*  <br/> |
|**UpdateFolderPermissions** <br/> |폴더 사용 권한 변경 되었습니다. 폴더 사용 권한 제어 조직에 있는 사용자 사서함 및 해당 폴더에 있는 메시지의 폴더에 액세스할 수 있습니다.  <br/> |예\*  <br/> |예\*  <br/> |예\*  <br/> |
|**UpdateInboxRules** <br/> |받은 편지함 규칙 추가, 제거 또는 변경 되었음을 합니다. 받은 편지함 규칙을 지정 된 조건에 따라 사용자의 받은 편지함의 메시지를 처리 하는 데 사용 되 하 고 지정 된 폴더로 메시지 이동 하거나 삭제 하는 메시지와 같은 규칙의 조건이 충족 되 면 작업을 수행 합니다.  <br/> |예\*  <br/> |예\*  <br/> |예\*  <br/> |
   
> [!NOTE]
> <sup>\*</sup>사서함에 대 한 감사 사용 하도록 설정 하는 경우 기본적으로 감사 됩니다.<br/><br/>  <sup>\*\*</sup>대리자에 의해 수행 되는 폴더 바인딩 작업에 대 한 항목 통합 됩니다. 하나의 로그 항목은 24 시간의 시간 범위 내에서 개별 폴더 액세스에 대 한 생성 됩니다.<br/><br/><sup>\*\*\*</sup>관리자에 게 사용자의 사서함에 대 한 전체 액세스 권한을 할당 된 대리인 사용자로 간주 됩니다. 
  
특정 유형의 사서함 감사 하기 위한 작업을 더이상 필요 하는 경우에 이러한 작업을 사용 하지 않도록 설정 하는 사서함 감사 로깅 구성을 수정 해야 합니다. 기존 로그 항목의 외에 감사 로그 항목에 대 한는 90 일 기간 한도 도달할 때까지 삭제 되지 않습니다.
  
## <a name="more-infotab"></a>[추가 정보](#tab/)
  
- Office 365 감사 로그를 사용 하 여 기록 된 사서함 활동에 대 한 검색 합니다. 특정 사용자 사서함에 대 한 활동을 검색할 수 있습니다. 다음 스크린샷에서 Office 365 감사 로그에서 검색할 수 있는 사서함 작업의 목록을 보여줍니다. 이러한 작업은과 같은 작업을 설명 하는이 항목의 "사서함 작업을 감사" 섹션에는 note 합니다.
    
    ![활동 드롭다운 목록에서 "Exchange 사서함 작업"을 선택 하 여 사서함 감사 작업에 대 한 Office 365 감사 로그를 검색할 수 있습니다.](media/fadc34f8-9de2-4688-8b1a-bc5540e69a23.png)
  
    다음 표에서 각 사서함 활동을 검색할 수 하 고 작업을 감사 하는 해당 사서함을 보여줍니다.
    
    |**감사 로그에 활동**|**사서함 감사 동작**|
    |:-----|:-----|
    |생성된 된 사서함 항목  <br/> |만들기  <br/> |
    |다른 폴더에 복사 된 메시지  <br/> |복사  <br/> |
    |사용자 사서함에 로그인 합니다.  <br/> |MailboxLogin  <br/> |
    |대신 보내기 권한을 사용 하 여 메시지를 보낸 사람이  <br/> |SendOnBehalf  <br/> |
    |사서함에서 제거 된 메시지  <br/> |HardDelete  <br/> |
    |지운 편지함 폴더로 메시지 이동  <br/> |MoveToDeletedItems  <br/> |
    |다른 폴더로 메시지 이동  <br/> |이동  <br/> |
    |다른 사람 이름으로 보내기 권한을 사용 하 여 메시지를 전송 합니다.  <br/> |SendAs  <br/> |
    |업데이트 된 메시지  <br/> |업데이트  <br/> |
    |지운 편지함 폴더에서 삭제 된 메시지  <br/> |SoftDelete  <br/> |
    |폴더에 추가 된 사용 권한  <br/> |UpdateFolderPermissions  <br/> |
    |폴더의 수정 된 사용 권한  <br/> |UpdateFolderPermissions  <br/> |
    |폴더에서 제거 된 사용 권한  <br/> |UpdateFolderPermissions  <br/> |
    |일정 폴더에 대 한 대리인 액세스와 추가 되거나 제거 된 사용자  <br/> |UpdateCalendarDelegation  <br/> |
   
    이전 화면에 표시 된 **추가 대리인 사서함 사용 권한** 및 **제거 됨, 사서함 권한 위임** 활동 작업을 감사 하는 사서함과 관련이 없는 note 합니다. 관리자가 할당 또는 FullAccess 사서함 권한이 제거 하는지 여부를 나타냅니다. 
    
    Office 365 감사 로그에 대 한 정보를 참조 하십시오. [Office 365 보안에서 감사 로그를 검색 &amp; 준수 센터](search-the-audit-log-in-security-and-compliance.md)합니다.
    
- 다음 시나리오에서는 관리자만 사서함에 액세스한다고 간주합니다.
    
  - Exchange Online 또는 Office 365에서 콘텐츠 검색에서 원본 위치 eDiscovery는 사서함을 검색 하는데 사용 됩니다.
    
  - [Microsoft Exchange Server MAPI 편집기](https://go.microsoft.com/fwlink/p/?linkId=204086)를 사용하여 사서함에 액세스합니다. 
    
- 사서함 감사 로깅을 사용하도록 설정할 때 로그온 유형(관리자, 대리인 또는 소유자)별로 기록할 사용자 작업(예: 메시지 액세스, 이동 또는 삭제)도 지정할 수 있습니다. 
    
- 사서함 감사 로깅을 사용하도록 설정하지 않으려면 다음 명령을 실행합니다.

  ```
  Set-Mailbox -Identity <identity of mailbox> -AuditEnabled $false
   ```

- **Get-mailbox** cmdlet을 실행 하는 경우 각 유형의 사용자에 대해 감사 되는 작업을 표시 되지 않습니다. 하지만 특정 사용자 로그온 형식에 대 한 감사 된 모든 작업을 표시 하려면 다음 명령을 실행할 수 있습니다. 

    ```
    Get-Mailbox <identity of mailbox> | Select-Object -ExpandProperty AuditAdmin
    ```

    ```
    Get-Mailbox <identity of mailbox> | Select-Object -ExpandProperty AuditDelegate
    ```

    ```
    Get-Mailbox <identity of mailbox> | Select-Object -ExpandProperty AuditOwner
    ```

- 사서함 감사 로그 내보내기 하 고 하나 이상의 사용자에 대 한 포함할 항목을 지정할 수도 있습니다. 보고서 및 감사 로그의 각 항목에는 해당 작업을 수행한 사용자에 대 한 때 수행 되는 작업 및 작업의 성공 여부를 정보가 포함 됩니다. 자세한 내용은 [사서함 감사 로그 내보내기](https://go.microsoft.com/fwlink/p/?LinkID=404104)를 참조 하십시오.
