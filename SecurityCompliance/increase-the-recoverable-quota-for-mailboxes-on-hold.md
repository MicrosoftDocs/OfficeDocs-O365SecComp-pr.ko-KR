---
title: 보류된 사물함의 복구 가능한 항목 할당량 증가
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 8/22/2017
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: a8bdcbdd-9298-462f-b889-df26037a990c
description: '보관 사서함을 사용 하도록 설정 하 고 자동 확장을 Office 365의 사서함에 대 한 복구 가능한 항목 폴더의 크기를 늘리려면 보관 설정 합니다. '
ms.openlocfilehash: 2e7149ef10152a11dc638c04b61a261440b539b8
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22533023"
---
# <a name="increase-the-recoverable-items-quota-for-mailboxes-on-hold"></a>보류된 사물함의 복구 가능한 항목 할당량 증가

기본 보존 정책-기본 MRM 정책 이라는-즉 Exchange Online에서 새로 만들기를 자동으로 적용 된 사서함 명명 된 복구 가능한 항목 14 일 후 보관 함으로 이동 보존 태그를 포함 합니다. 팀에서 14 일 보존 기간이 만료 된 항목에 대 한이 보존 태그 항목을 사용자의 기본 사서함의 복구 가능한 항목 폴더에서 사용자의 보관 사서함의 복구 가능한 항목 폴더를 이동 합니다. 발생 하려면이 옵션을 사용자의 보관 사서함 사용 해야 합니다. 보관 사서함 설정 되지 않은 경우 아무 작업도 수행, 즉, 14 일 보존 기간이 만료 후의 복구 가능한 항목 폴더의 사서함에 대해 보류의 항목 보관 사서함으로 이동 되지 않습니다. 없기 때문에 아무것도 대기 사서함에서 삭제 되는 복구 가능한 항목 폴더에 대 한 저장소 할당량을 초과 될 수 있습니다, 사용자의 보관 사서함 설정 되지 않은 경우에 특히 합니다. 
  
이 제한을 초과 하면 가능성을 줄이려면 복구 가능한 항목 폴더에 대 한 저장소 할당량은 자동으로 늘어났습니다 30GB에서 100GB로 보류에 배치 될 때는 사서함 Exchange Online 합니다. 보관 사서함을 사용 하는 경우의 보관 사서함의 복구 가능한 항목 폴더에 대 한 저장소 할당량도 증가 30GB에서 100GB로 합니다. Exchange 기능 자동 확장 하는 보관 하는 경우에 온라인 상태가, 사용자의 보관에서 복구 가능한 항목 폴더에 대 한 저장소 할당량 제한 됩니다.
  
  다음 표는 복구 가능한 항목 폴더의 저장소 할당량을 간략하게 보여줍니다. 
  
|**복구 가능한 항목 폴더 위치**|**보류되지 않은 사서함**|**보류된 사서함**|
|:-----|:-----|:-----|
|기본 사서함  <br/> |30GB  <br/> |100GB  <br/> |
|보관 사서함<sup>\*</sup> <br/> |제한 없음  <br/> |제한 없음  <br/> |
|**복구 가능한 항목 폴더 할당량** <br/> |제한 없음  <br/> |제한 없음  <br/> |
   
> [!NOTE]
> <sup>\*</sup>보관 사서함에 대 한 초기 저장소 할당량은 Exchange Online (계획 2) 라이선스를 사용 하는 사용자에 대 한 100GB. 하지만, 자동 확장 보관을 설정 하는 경우 사용자의 보관 및 보관 사서함의 복구 가능한 항목 폴더에 대 한 저장소 할당량 제한 되지는 않습니다. 자동 확장 하는 방법에 대 한 자세한 내용은 [Office 365 무제한 보관의 개요](unlimited-archiving.md)를 참조 보관 하십시오. 
  
보류된 사서함의 기본 사서함에 있는 복구 가능한 항목 폴더의 저장소 할당량이 한도에 도달하려는 경우 다음 항목을 수행할 수 있습니다.
  
- **보관 사서함을 사용 하도록 설정 하 고 자동 확장 보관 설정** -보관 사서함을 사용 하도록 설정 하 고 다음 Exchange에서 자동을 확장 하면 보관 기능을 설정 하 여 복구 가능한 항목 폴더에 대 한 사용 하 여 무제한 저장 용량이 설정할 수 있습니다 온라인. 이 기본 사서함과 사용자의 보관에서 복구할 수 있는 항목 폴더에 대 한 저장 용량에 무제한 금액의 복구 가능한 항목 폴더에 100GB에서 만들어집니다. 참조 방법: [Office 365 보안에서 보관 사서함 사용 &amp; 준수 센터](enable-archive-mailboxes.md) 고 [Office 365에서 무제한 보관을 사용](enable-unlimited-archiving.md)합니다.
    
    > [!NOTE]
    > 수동으로 이동 되도록 만료 된 항목의 사서함을 처리 하는 데 길잡이 트리거하는 관리 되는 폴더 도우미가 실행 해야할 복구 가능한 항목 폴더에 대 한 저장소 할당량을 초과 하면 되는 사서함에 대 한 보관을 활성화 한 후의 보관 사서함의 복구 가능한 항목 폴더입니다. 지침에 대 한 [4 단계를](#optional-step-4-run-the-managed-folder-assistant-to-apply-the-new-retention-settings) 참조 하십시오. 참고 사용자의 사서함에서 다른 항목은 새 보관 사서함으로 이동할 수 있습니다. 보관 사서함을 사용 하도록 설정한 후 발생할 수 있습니다이 방향을 지시 하는 것이 좋습니다. 
  
- **보관 사서함에 대 한 사용자 지정 보존 정책 만들기** -보관 사서함을 사용 하도록 설정 하 고 자동 확장 사서함을 원본 위치 유지 또는 소송 보존으로 설정에 대 한 보관 외에 해야할 수에 사서함에 대 한 사용자 지정 보존 정책을 만들합니다 보류 합니다. 이 보겠습니다 정책을 적용 하면 보존 대기 대기 되지 않은 사서함에 적용 되는 기본 MRM 정책와에서는 다른 사서함에 있습니다. 이 보류에 있는 사서함에 대 한 특별히 설계 된 보존 태그를 적용할 수 있습니다. 복구 가능한 항목 폴더에 대 한 새 보존 태그 만들기 (영문) 포함 됩니다. 
    
이 항목의 나머지 부분에서는 보류된 사서함에 대한 사용자 지정 보존 정책을 만드는 단계별 절차를 설명합니다.
  
[1단계: 복구 가능한 항목 폴더에 대한 사용자 지정 보존 태그를 만듭니다.](#step-1-create-a-custom-retention-tag-for-the-recoverable-items-folder)

[[2 단계: 대기 사서함에 대 한 새 보존 정책 만들기](#step-2-create-a-new-retention-policy-for-mailboxes-on-hold)

[3단계: 보류된 사서함에 새로운 보존 정책을 적용합니다.](#step-3-apply-the-new-retention-policy-to-mailboxes-on-hold)

[(옵션)4단계: 관리되는 폴더 도우미를 실행하여 새로운 보존 설정을 적용합니다.](#optional-step-4-run-the-managed-folder-assistant-to-apply-the-new-retention-settings)
  
## <a name="step-1-create-a-custom-retention-tag-for-the-recoverable-items-folder"></a>1단계: 복구 가능한 항목 폴더에 대한 사용자 지정 보존 태그를 만듭니다.

첫번째 단계는 복구 가능한 항목 폴더에 대 한 사용자 지정 보존 태그 (보존 정책 태그 또는 RPT 라고 함)를 만드는 것입니다. 앞에서 설명한 것 처럼이 RPT 사용자의 기본 사서함의 복구 가능한 항목 폴더에서 항목을 복구할 수 있는 항목 폴더에 사용자의 보관 사서함 이동합니다. 복구 가능한 항목 폴더에 대 한 RPT를 만들 수 PowerShell을 사용 해야 합니다. Exchange 관리 센터 (EAC)를 사용할 수 없습니다. 
  
1. [원격 PowerShell을 사용하여 Exchange Online에 연결](https://go.microsoft.com/fwlink/p/?LinkId=517283)
    
2. 복구할 수 있는 항목 폴더에 대한 새로운 RPT를 만들려면 다음 명령을 실행합니다.  
    
    ```
    New-RetentionPolicyTag -Name <Name of RPT> -Type RecoverableItems -AgeLimitForRetention <Number of days> -RetentionAction MoveToArchive
    ```

    예를 들어 다음 명령을 사용하면 보존 기간이 30일인 “보류된 사서함의 30일 복구 가능한 항목”이라는 복구 가능한 항목 폴더에 대한 RPT가 만들어집니다. 이는 어떤 항목이 복구 가능한 항목 폴더에서 30일 동안 있은 후 사용자의 보관 사서함에 있는 복구 가능한 항목 폴더로 이동함을 의미합니다.
    
    ```
    New-RetentionPolicyTag -Name "Recoverable Items 30 days for mailboxes on hold" -Type RecoverableItems -AgeLimitForRetention 30 -RetentionAction MoveToArchive
    ```

    > [!TIP]
    > 복구 가능한 항목 RPT에 대 한 보존 기간 ( _AgeLimitForRetention_ 매개 변수에 의해 정의 된) RPT 적용할 수 있는 사서함에 대 한 삭제 된 항목 보존 기간와 동일 하 게 되는 것이 좋습니다. 이렇게 하면 사용자 전체 삭제 된 항목 보존 기간 보관 사서함으로 이동 하기 전에 삭제 된 항목을 복구할 수 있습니다. 이전 예제에서 보존 기간 사서함에 대 한 삭제 된 항목 보존 기간은 30 일 수도 있다는 가정에 따라 30 일로 설정 되었습니다. Exchange Online 사서함은 기본적으로 14 일에 대 한 삭제 된 항목을 유지 하도록 구성 됩니다. 하지만 최대 30 일에이 설정을 변경할 수 있습니다. 자세한 내용은 [온라인 Exchange 사서함에 대 한 삭제 된 항목 보존 기간 변경](https://go.microsoft.com/fwlink/p/?LinkId=286940)을 참조 하십시오. 
  
## <a name="step-2-create-a-new-retention-policy-for-mailboxes-on-hold"></a>2단계: 보류된 사서함에 대한 새로운 보존 정책을 만듭니다.

다음 단계는 새로운 보존 정책을 만들고 1단계에서 만든 복구 가능한 항목 RPT 등 이 새로운 보존 정책에 보존 태그를 추가하는 것입니다. 새로운 보존 정책은 다음 단계에서 보류된 사서함에 적용됩니다.  
  
새로운 보존 정책을 만들기 전에 추가할 추가적인 보존 태그를 결정합니다. 기본 MRM 정책에 추가되는 보존 태그의 목록 및 새로운 보존 태그에 대한 정보를 확인하려면 다음을 참조하세요.
  
- [기본 보존 정책 in Exchange Online](https://go.microsoft.com/fwlink/p/?LinkId=746954)
    
- [보존 정책 태그를 지 원하는 기본 폴더](https://go.microsoft.com/fwlink/p/?LinkId=746957)
    
- [보존 정책 만들기](https://go.microsoft.com/fwlink/p/?LinkId=404422) 항목의 "보존 태그 만들기" 섹션.
    
EAC 또는 Exchange Online PowerShell 보존 정책 만들기를 사용할 수 있습니다.
  
### <a name="use-the-eac-to-create-a-retention-policy"></a>EAC를 사용하여 보존 정책 만들기
  
1. EAC에서 **규정 준수 관리** 로 이동 \> **보존 정책**, 다음 **추가** 클릭 하 고 ![아이콘 추가](media/ITPro-EAC-AddIcon.gif)합니다.
    
2. **새 보존 정책** 페이지의 **이름**에서 **MRM Policy for Mailboxes on Hold** 등 보존 정책의 목적을 설명하는 이름을 입력합니다.  
    
3. **보존 태그** **추가** 클릭 ![아이콘 추가](media/ITPro-EAC-AddIcon.gif)합니다.
    
4. 보존 태그 목록에서 1단계에서 만든 복구 가능한 항목 RPT를 선택한 다음 **추가**를 클릭합니다.
    
    ![사용자 지정 복구 가능한 항목 보존 태그 선택](media/eb49866b-bdef-4fcd-a6d9-01607c01249b.png)
  
5. 보존 정책에 추가할 추가적인 보존 태그를 선택합니다. 예를 들어 기존 MRM 정책에 포함되어 있는 것과 동일한 태그를 추가하는 것이 좋습니다.
    
6. 보존 태그 추가가 완료되면 **확인**을 클릭합니다.
    
7. **저장**을 클릭하여 새 보존 정책을 만듭니다. 
    
    보존 정책에 연결된 보존 태그가 세부 정보 창에 표시된다는 점에 유의하시기 바랍니다.
    
    ![보존 정책에 연결된 보존 태그가 세부 정보 창에 표시됩니다.](media/dad1c8f4-9928-4d6d-991a-6f6c5194eceb.png)
  
### <a name="use-exchange-online-powershell-to-create-a-retention-policy"></a>Exchange Online PowerShell을 사용 하 여 보존 정책을 만들려면
  
보류된 사서함에 대한 새 보존 정책을 만들려면 다음 명령을 실행합니다.  
  
```
New-RetentionPolicy <Name of retention policy>  -RetentionPolicyTagLinks <list of retention tags>

```

예를 들어 다음 명령을 사용하면 보존 정책 및 이전 그림에 표시되어 있는 연결된 보존 태그가 생성됩니다.
  
```
New-RetentionPolicy "MRM Policy for Mailboxes on Hold"  -RetentionPolicyTagLinks "Recoverable Items 30 days for mailboxes on hold","1 Month Delete","1 Week Delete","1 Year Delete","5 Year Delete","6 Month Delete","Default 2 year move to archive","Junk Email","Never Delete","Personal 1 year move to archive","Personal 5 year move to archive"
```
  
## <a name="step-3-apply-the-new-retention-policy-to-mailboxes-on-hold"></a>3단계: 보류된 사서함에 새로운 보존 정책을 적용합니다.

조직에서 사서함 보류에 2 단계에서에서 만든 새 보존 정책을 적용 하려면 마지막 단계가입니다. EAC 또는 Exchange Online PowerShell를 사용 하 여 단일 사서함에 또는 여러 사서함에 보존 정책을 적용할 수 있습니다. 
  
### <a name="use-the-eac-to-apply-the-new-retention-policy"></a>EAC를 사용하여 새 보존 정책 적용하기
  
1. **받는 사람** 에 게 이동 \> **사서함**입니다.
    
2. 목록 보기에서 보존 정책을 적용 하려는 사서함을 선택 하 고 **편집** 을 클릭 한 다음 ![편집 아이콘](media/ebd260e4-3556-4fb0-b0bb-cc489773042c.gif)합니다.
    
3. **사용자 사서함** 페이지에서 **사서함 기능**을 클릭합니다.
    
4. **보존 정책**에서 2단계에서 만든 보존 정책을 선택하고 **저장**을 클릭합니다.
    
EAC를 사용하여 여러 사서함에 보존 정책을 적용할 수도 있습니다.
  
1. **받는 사람** 에 게 이동 \> **사서함**입니다.
    
2. 목록 보기에서 Shift 또는 Ctrl 키를 사용하여 여러 개의 사서함을 선택합니다.
    
3. 세부 정보 창에서 **기타 옵션**을 클릭합니다.
    
4. **보존 정책**에서 **업데이트**를 클릭합니다.
    
5. **대량 할당 보존 정책** 페이지에서 2단계에서 만든 보존 정책을 선택하고  **저장**을 클릭합니다.  
    
### <a name="use-exchange-online-powershell-to-apply-the-new-retention-policy"></a>Exchange Online PowerShell을 사용 하 여 새 보존 정책을 적용 하려면
  
Exchange Online PowerShell를 사용 하 여 단일 사서함에 새 보존 정책을 적용할 수 있습니다. 이지만 PowerShell의 실제 전원은 신속 하 게 식별할 원본 위치 유지 또는 소송 보존으로 설정 되며 다음에 새 보존 정책을 모든 사서함에 적용 하는 조직에서 사서함 유지 (영문) 단일 명령을 모두 사용할 수 있습니다. 다음은 하나 이상의 사서함에 보존 정책을 적용 하려면 Exchange PowerShell을 사용 하 여의 몇가지 예입니다. 이 예제에서는 모든 2 단계에서에서 만든 보존 정책을 적용 합니다.
  
이 예에서는 Pilar Pinilla의 사서함에 새로운 보존 정책을 적용합니다.
  
```
Set-Mailbox "Pilar Pinilla" -RetentionPolicy "MRM Policy for Mailboxes on Hold"
```

이 예에서는 조직의 모든 소송 보존 사서함에 새로운 보존 정책을 적용합니다.
  
```
$LitigationHolds = Get-Mailbox -ResultSize unlimited | Where-Object {$_.LitigationHoldEnabled -eq 'True'}
```

```
$LitigationHolds.DistinguishedName | Set-Mailbox -RetentionPolicy "MRM Policy for Mailboxes on Hold"
```

이 예에서는 조직의 모든 원본 위치 유지 사서함에 새로운 보존 정책을 적용합니다.
  
```
$InPlaceHolds = Get-Mailbox -ResultSize unlimited | Where-Object {$_.InPlaceHolds -ne $null}
```

```
$InPlaceHolds.DistinguishedName | Set-Mailbox -RetentionPolicy "MRM Policy for Mailboxes on Hold"
```

**Get-Mailbox** cmdlet를 사용하여 새로운 보존 정책이 적용되었는지 확인할 수 있습니다. 
  
다음은 이전 예에서 소송 보존 사서함 및 원본 위치 유지 사서함에 "보류된 사서함에 대한 MRM 정책" 보존 정책이 적용되었는지 확인하기 위한 몇 가지 예입니다.
  
```
Get-Mailbox "Pilar Pinilla" | Select RetentionPolicy
```

```
Get-Mailbox -ResultSize unlimited | Where-Object {$_.LitigationHoldEnabled -eq 'True'} | FT DisplayName,RetentionPolicy -Auto
```

```
Get-Mailbox -ResultSize unlimited | Where-Object {$_.InPlaceHolds -ne $null} | FT DisplayName,RetentionPolicy -Auto
```
  
## <a name="optional-step-4-run-the-managed-folder-assistant-to-apply-the-new-retention-settings"></a>(옵션) 4단계: 관리되는 폴더 도우미를 실행하여 새로운 보존 설정을 적용합니다.

보류에 있는 사서함에 새 보존 정책을 적용 한 후 걸릴 수 최대 7 일 Exchange 온라인는 관리 되는 폴더 도우미 설정을 사용 하 여 새 보존 정책에서 이러한 사서함을 처리 하는 데에 대 한 합니다. 관리 되는 폴더 도우미를 실행 하려면를 기다리지 않고 수동으로에 새 보존 정책을 적용 하는 사서함을 처리 하는 데 길잡이 트리거하 **Start-managedfolderassistant** cmdlet을 사용할 수 있습니다. 
  
다음 명령을 실행하여 Pilar Pinilla의 사서함에 관리되는 폴더 도우미를 실행합니다. 
  
```
Start-ManagedFolderAssistant "Pilar Pinilla"
```

다음 명령을 실행하여 보류된 모든 사서함에 관리되는 폴더 도우미를 실행합니다. 
  
```
$MailboxesOnHold = Get-Mailbox -ResultSize unlimited | Where-Object {($_.InPlaceHolds -ne $null) -or ($_.LitigationHoldEnabled -eq "True")}
```

```
$MailboxesOnHold.DistinguishedName | Start-ManagedFolderAssistant
```

## <a name="more-information"></a>추가 정보

- 사용자의 보관 사서함을 활성화 한 후에 (아니라 항목 복구 가능한 항목 폴더에서) 사서함의 다른 항목은 보관 사서함으로 이동할 수 있습니다는 방향을 지시 하는 것이 좋습니다. 이 Exchange Online 사서함에 할당 된 기본 MRM 정책 항목 된 사서함에 게 배달 되거나 사용자가 만든 날짜 로부터 2 년 항목 보관 사서함으로 이동 하는 보존 태그 (명명 된 기본 2 년 후 보관 함으로 이동)를 포함 하기 때문에 사용자입니다. 자세한 내용은 [Exchange Online의 기본 보존 정책](https://go.microsoft.com/fwlink/p/?LinkId=746954) 을 참조 하십시오.
    
- 사용자의 보관 사서함을 활성화 한 후 복구할 수 있는 사용자가 자신의 보관 사서함의 복구 가능한 항목 폴더에서 항목 삭제 알 수 있습니다. 보관 사서함의 **지운 편지함** 폴더를 선택 하 고 다음 **홈** 탭에서 **서버에서 지운 편지함 복구** 를 클릭 하 여 Outlook에서이 작업을 수행할 수 있습니다. 삭제 된 항목을 복구 하는 중에 대 한 자세한 내용은 [Windows 용 Outlook에서에서 항목 삭제 된 복구를](https://go.microsoft.com/fwlink/p/?LinkId=624829)참조 하십시오. 
