---
title: 보류된 사물함의 복구 가능한 항목 할당량 증가
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 10/12/2018
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
ms.collection: M365-security-compliance
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: a8bdcbdd-9298-462f-b889-df26037a990c
description: '보관 사서함을 사용 하도록 설정 하 고 자동 확장 보관을 설정 하 여 Office 365에서 사서함에 대 한 복구 가능한 항목 폴더의 크기를 늘립니다. '
ms.openlocfilehash: f419da5b1b42d52433e9fc288aa5b401a2123c1c
ms.sourcegitcommit: e7a776a04ef6ed5e287a33cfdc36aa2d72862b55
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/29/2019
ms.locfileid: "30998971"
---
# <a name="increase-the-recoverable-items-quota-for-mailboxes-on-hold"></a>보류된 사물함의 복구 가능한 항목 할당량 증가

Exchange Online의 새 사서함에 자동으로 적용 되는 기본 mrm 정책 이라는 기본 보존 정책에는 복구 가능한 항목 14 일 후 보관 함으로 이동 되는 보존 태그가 포함 되어 있습니다. 이 보존 태그는 특정 항목의 보존 기간 14일이 만료되면 사용자의 기본 사서함에 있는 복구 가능한 항목 폴더의 항목이 사용자의 보관 사서함에 있는 복구 가능한 항목 폴더로 이동합니다. 이렇게 항목이 이동하려면 사용자의 보관 사서함을 반드시 사용하도록 설정해야 합니다. 보관 사서함을 사용하도록 설정하지 않은 경우, 어떠한 조치도 취하지 않으면 보류된 사서함의 복구 가능한 항목 폴더에 있는 항목이 보존 기간 14일이 만료된 후에도 보관 사서함으로 이동하지 않습니다. 보류된 사서함에서 어떤 항목도 삭제되지 않기 때문에 복구 가능한 항목 폴더의 저장소 할당량이 초과될 수 있으며 사용자의 보관 사서함을 사용하도록 설정하지 않으면 특히 이러한 경우가 발생할 수 있습니다. 
  
Exchange Online의 사서함에 대 한 보존을 설정 하면이 제한을 초과할 가능성을 줄이기 위해 복구 가능한 항목 폴더의 저장소 할당량이 자동으로 30gb에서 100 GB로 증가 합니다. 보관 사서함을 사용하도록 설정하는 경우에도 보관 사서함에 있는 복구 가능한 항목 폴더의 저장소 할당량이 30GB에서 100GB로 증가합니다. Exchange Online의 자동 확장 보관 기능이 사용 하도록 설정 된 경우 사용자 보관의 복구 가능한 항목 폴더에 대 한 저장소 할당량은 무제한으로 지정 됩니다.
  
  다음 표는 복구 가능한 항목 폴더의 저장소 할당량을 간략하게 보여줍니다. 
  
|**복구 가능한 항목 폴더 위치**|**보류되지 않은 사서함**|**보류된 사서함**|
|:-----|:-----|:-----|
|기본 사서함  <br/> |30GB  <br/> |100GB  <br/> |
|보관 사서함<sup>\*</sup> <br/> |무제한  <br/> |무제한  <br/> |
|**복구 가능한 항목 폴더 할당량** <br/> |무제한  <br/> |무제한  <br/> |
   
> [!NOTE]
> <sup>\*</sup>Exchange Online (계획 2) 라이선스가 있는 사용자의 경우 보관 사서함의 초기 저장소 할당량은 100 GB입니다. 그러나 보류 중인 사서함에 대해 자동 확장 보관을 설정 하면 보관 사서함 및 복구 가능한 항목 폴더의 저장소 할당량이 110 GB로 증가 합니다. 필요한 경우 추가 보관 저장소 공간이 프로 비전 되어 보관 저장소의 크기가 무제한으로 제공 됩니다. 자동 확장 보관에 대 한 자세한 내용은 [Office 365의 무제한 보관 개요](unlimited-archiving.md)를 참조 하세요. 
  
보류된 사서함의 기본 사서함에 있는 복구 가능한 항목 폴더의 저장소 할당량이 한도에 도달하려는 경우 다음 항목을 수행할 수 있습니다.
  
- **보관 사서함을 사용 하도록 설정 하 고 자동 확장 보관을 설정** 하면 보관 사서함을 사용 하도록 설정 하 고 Exchange에서 자동 확장 보관 기능을 설정 하 여 복구 가능한 항목 폴더에 대해 무제한 저장소 용량을 사용 하도록 설정할 수 있습니다. 온라인. 이를 통해 기본 사서함의 복구 가능한 항목 폴더에 대해 110이 발생 하 고 사용자 보관의 복구 가능한 항목 폴더에 대해 무제한의 저장 용량을 사용할 수 있습니다. 방법: [보안 & 준수 센터에서 보관 사서함을 사용 하도록 설정](enable-archive-mailboxes.md) 하 고 [Office 365에서 무제한 보관을 사용 하도록 설정](enable-unlimited-archiving.md)합니다.
    
    > [!NOTE]
    > 복구 가능한 항목 폴더가 저장소 할당량을 초과하기 직전인 사서함에서 보관함을 사용하도록 설정하고 난 다음에는 관리되는 폴더 도우미를 실행함으로써 도우미를 수동으로 실행시켜 도우미가 사서함을 보관 사서함의 복구 가능한 항목 폴더에서 만료된 항목이 이동되도록 합니다. [4단계](#optional-step-4-run-the-managed-folder-assistant-to-apply-the-new-retention-settings)에서 지침을 확인하세요. 사용자의 사서함에 있는 다른 항목이 새로운 보관 사서함으로 이동되었을 수 있다는 점에 유의하시기 바랍니다. 보관 사서함을 사용 하도록 설정한 후 사용자에 게이를 알리는 것을 고려할 수 있습니다. 
  
- **보류 중인 사서함에 대 한 사용자 지정 보존 정책 만들기** -보관 사서함을 사용 하도록 설정 하 고 사서함에 대해 소송 보존 또는 원본 위치 유지를 자동 확장 하는 데 사용할 수 있습니다. 놓습니다. 이를 통해 보류 중인 사서함에 적용 되는 기본 mrm 정책과는 다른 보류 중인 사서함에 보존 정책을 적용할 수 있습니다. 이를 통해 특별히 사서함에 맞게 디자인 된 보존 태그를 적용할 수 있습니다. 여기에는 복구 가능한 항목 폴더에 대 한 새 보존 태그를 만드는 작업이 포함 됩니다. 
    
이 항목의 나머지 부분에서는 보류된 사서함에 대한 사용자 지정 보존 정책을 만드는 단계별 절차를 설명합니다.
  
[1단계: 복구 가능한 항목 폴더에 대한 사용자 지정 보존 태그를 만듭니다.](#step-1-create-a-custom-retention-tag-for-the-recoverable-items-folder)

[[2 단계: 보류 된 사서함에 대 한 새 보존 정책 만들기](#step-2-create-a-new-retention-policy-for-mailboxes-on-hold)

[3단계: 보류된 사서함에 새로운 보존 정책을 적용합니다.](#step-3-apply-the-new-retention-policy-to-mailboxes-on-hold)

[(옵션)4단계: 관리되는 폴더 도우미를 실행하여 새로운 보존 설정을 적용합니다.](#optional-step-4-run-the-managed-folder-assistant-to-apply-the-new-retention-settings)
  
## <a name="step-1-create-a-custom-retention-tag-for-the-recoverable-items-folder"></a>1단계: 복구 가능한 항목 폴더에 대한 사용자 지정 보존 태그를 만듭니다.

첫 번째 단계는 복구 가능한 항목 폴더에 대하여 사용자 지정 보존 태그(보존 정책 태그 또는 RPT라고 함)를 만드는 것입니다. 앞서 설명된 바와 같이 이 RPT는 사용자의 기본 사서함에 있는 복구 가능한 항목 폴더의 항목을 사용자의 보관 사서함에 있는 복구 가능한 항목 폴더로 이동합니다. PowerShell을 사용 하 여 복구 가능한 항목 폴더에 대 한 RPT를 만들어야 합니다. EAC(Exchange 관리 센터)는 사용할 수 없습니다. 
  
1. [Connect to Exchange Online using remote PowerShell](https://go.microsoft.com/fwlink/p/?LinkId=517283)(원격 PowerShell을 사용하여 Exchange Online에 연결)
    
2. 복구할 수 있는 항목 폴더에 대한 새로운 RPT를 만들려면 다음 명령을 실행합니다.  
    
    ```
    New-RetentionPolicyTag -Name <Name of RPT> -Type RecoverableItems -AgeLimitForRetention <Number of days> -RetentionAction MoveToArchive
    ```

    예를 들어 다음 명령을 사용하면 보존 기간이 30일인 “보류된 사서함의 30일 복구 가능한 항목”이라는 복구 가능한 항목 폴더에 대한 RPT가 만들어집니다. 이는 어떤 항목이 복구 가능한 항목 폴더에서 30일 동안 있은 후 사용자의 보관 사서함에 있는 복구 가능한 항목 폴더로 이동함을 의미합니다.
    
    ```
    New-RetentionPolicyTag -Name "Recoverable Items 30 days for mailboxes on hold" -Type RecoverableItems -AgeLimitForRetention 30 -RetentionAction MoveToArchive
    ```

    > [!TIP]
    > 복구 가능한 항목 rpt의 보존 기간은 rpt가 적용 __ 될 사서함에 대 한 삭제 된 항목 보존 기간과 동일 하 게 유지 하는 것이 좋습니다. 이렇게 하면 사용자가 삭제된 항목 보존 기간을 전부 활용하여 삭제된 항목이 보관 사서함으로 이동하기 전에 삭제된 항목을 복구할 수 있습니다. 이전 예에서는 사서함의 삭제된 항목 보존 기간도 30일이라는 가정 하에 보존 기간이 30일로 설정되었습니다. 기본적으로 Exchange Online 사서함은 14일 동안 삭제된 항목을 보존하도록 구성됩니다. 하지만 이 설정을 최대 30일로 변경할 수 있습니다. 자세한 내용은 [Exchange Online에서 사서함에 대 한 삭제 된 항목 보존 기간 변경을](https://go.microsoft.com/fwlink/p/?LinkId=286940)참조 하십시오. 
  
## <a name="step-2-create-a-new-retention-policy-for-mailboxes-on-hold"></a>2단계: 보류된 사서함에 대한 새로운 보존 정책을 만듭니다.

다음 단계는 새로운 보존 정책을 만들고 1단계에서 만든 복구 가능한 항목 RPT 등 이 새로운 보존 정책에 보존 태그를 추가하는 것입니다. 새로운 보존 정책은 다음 단계에서 보류된 사서함에 적용됩니다.  
  
새로운 보존 정책을 만들기 전에 추가할 추가적인 보존 태그를 결정합니다. 기본 MRM 정책에 추가되는 보존 태그의 목록 및 새로운 보존 태그에 대한 정보를 확인하려면 다음을 참조하세요.
  
- [Exchange Online의 기본 보존 정책](https://go.microsoft.com/fwlink/p/?LinkId=746954)
    
- [보존 정책 태그를 지원하는 기본 폴더](https://go.microsoft.com/fwlink/p/?LinkId=746957)
    
- [보존 정책 만들기](https://go.microsoft.com/fwlink/p/?LinkId=404422) 항목의 "보존 태그 만들기" 섹션
    
EAC 또는 Exchange Online PowerShell을 사용 하 여 보존 정책을 만들 수 있습니다.
  
### <a name="use-the-eac-to-create-a-retention-policy"></a>EAC를 사용하여 보존 정책 만들기
  
1. EAC에서 **준수 관리** \> **보존 정책**으로 이동한 다음 **** ![추가 아이콘](media/ITPro-EAC-AddIcon.gif)추가를 클릭 합니다.
    
2. **새 보존 정책** 페이지의 **이름**에서 **MRM Policy for Mailboxes on Hold** 등 보존 정책의 목적을 설명하는 이름을 입력합니다.  
    
3. **보존 태그**에서 **** ![추가 아이콘](media/ITPro-EAC-AddIcon.gif)추가를 클릭 합니다.
    
4. 보존 태그 목록에서 1단계에서 만든 복구 가능한 항목 RPT를 선택한 다음 **추가**를 클릭합니다.
    
    ![사용자 지정 복구 가능한 항목 보존 태그 선택](media/eb49866b-bdef-4fcd-a6d9-01607c01249b.png)
  
5. 보존 정책에 추가할 추가적인 보존 태그를 선택합니다. 예를 들어 기존 MRM 정책에 포함되어 있는 것과 동일한 태그를 추가하는 것이 좋습니다.
    
6. 보존 태그 추가가 완료되면 **확인**을 클릭합니다.
    
7. **저장**을 클릭하여 새 보존 정책을 만듭니다. 
    
    보존 정책에 연결된 보존 태그가 세부 정보 창에 표시된다는 점에 유의하시기 바랍니다.
    
    ![보존 정책에 연결된 보존 태그가 세부 정보 창에 표시됩니다.](media/dad1c8f4-9928-4d6d-991a-6f6c5194eceb.png)
  
### <a name="use-exchange-online-powershell-to-create-a-retention-policy"></a>Exchange Online PowerShell을 사용 하 여 보존 정책 만들기
  
보류된 사서함에 대한 새 보존 정책을 만들려면 다음 명령을 실행합니다.  
  
```
New-RetentionPolicy <Name of retention policy>  -RetentionPolicyTagLinks <list of retention tags>

```

예를 들어 다음 명령을 사용하면 보존 정책 및 이전 그림에 표시되어 있는 연결된 보존 태그가 생성됩니다.
  
```
New-RetentionPolicy "MRM Policy for Mailboxes on Hold"  -RetentionPolicyTagLinks "Recoverable Items 30 days for mailboxes on hold","1 Month Delete","1 Week Delete","1 Year Delete","5 Year Delete","6 Month Delete","Default 2 year move to archive","Junk Email","Never Delete","Personal 1 year move to archive","Personal 5 year move to archive"
```
  
## <a name="step-3-apply-the-new-retention-policy-to-mailboxes-on-hold"></a>3단계: 보류된 사서함에 새로운 보존 정책을 적용합니다.

마지막 단계는 조직의 보류된 사서함에 2단계에서 만든 새로운 보존 정책을 적용하는 것입니다. EAC 또는 Exchange Online PowerShell을 사용 하 여 단일 사서함 이나 여러 사서함에 보존 정책을 적용할 수 있습니다. 
  
### <a name="use-the-eac-to-apply-the-new-retention-policy"></a>EAC를 사용하여 새 보존 정책 적용하기
  
1. **받는 사람** \> **사서함**으로 이동 합니다.
    
2. 목록 보기에서 보존 정책을 적용할 사서함을 선택 하 고 편집 아이콘](media/ebd260e4-3556-4fb0-b0bb-cc489773042c.gif) **편집** ![을 클릭 합니다.
    
3. **사용자 사서함** 페이지에서 **사서함 기능**을 클릭합니다.
    
4. **보존 정책**에서 2단계에서 만든 보존 정책을 선택하고 **저장**을 클릭합니다.
    
EAC를 사용하여 여러 사서함에 보존 정책을 적용할 수도 있습니다.
  
1. **받는 사람** \> **사서함**으로 이동 합니다.
    
2. 목록 보기에서 Shift 또는 Ctrl 키를 사용하여 여러 개의 사서함을 선택합니다.
    
3. 세부 정보 창에서 **기타 옵션**을 클릭합니다.
    
4. **보존 정책**에서 **업데이트**를 클릭합니다.
    
5. **대량 할당 보존 정책** 페이지에서 2단계에서 만든 보존 정책을 선택하고  **저장**을 클릭합니다.  
    
### <a name="use-exchange-online-powershell-to-apply-the-new-retention-policy"></a>Exchange Online PowerShell을 사용 하 여 새 보존 정책 적용
  
Exchange Online PowerShell을 사용 하 여 단일 사서함에 새 보존 정책을 적용할 수 있습니다. 그러나 PowerShell의 실제 기능은 조직의 모든 사서함을 소송 보존 또는 원본 위치 유지 상태로 빠르게 식별 한 다음 단일 명령으로 보류 중인 모든 사서함에 새 보존 정책을 적용 하는 데 사용할 수 있다는 것입니다. 다음은 Exchange PowerShell을 사용 하 여 하나 이상의 사서함에 보존 정책을 적용 하는 몇 가지 예입니다. 모든 예에서는 2단계에서 만든 보존 정책을 적용합니다.
  
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

보류 중인 사서함에 새 보존 정책을 적용 하 고 나면 Exchange Online에서 관리 되는 폴더 도우미가 새 보존 정책의 설정을 사용 하 여 이러한 사서함을 처리 하는 데 최대 7 일이 걸릴 수 있습니다. 관리되는 폴더 도우미가 실행되기를 기다리는 대신 **Start-ManagedFolderAssistant** cmdlet를 사용하여 새로운 보존 정책이 적용된 사서함을 처리하도록 도우미를 수동으로 트리거할 수 있습니다. 
  
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

- 사용자의 보관 사서함을 사용하도록 설정한 후 사용자에게 사서함에 있는 다른 항목(복구 가능한 항목 폴더에 있는 항목 외)이 보관 사서함으로 이동될 수 있다는 점을 안내하는 것이 좋습니다. 이는 Exchange Online 사서함에 할당 된 기본 mrm 정책에 항목이 사서함으로 배달 된 후 2 년 후에 항목을 보관 사서함으로 이동 하는 보존 태그 (기본 2 년을 보관 함으로 이동 함)가 포함 되어 있기 때문입니다. 가. 자세한 내용은 [Exchange Online의 기본 보존 정책](https://go.microsoft.com/fwlink/p/?LinkId=746954) 를 참조 하세요.
    
- 사용자의 보관 사서함을 사용하도록 설정한 후 사용자에게 보관 사서함의 복구 가능한 항목 폴더에서 삭제된 항목을 복구할 수 있다고 안내하시기 바랍니다. 보관 사서함에서 **지운** 편지함 폴더를 선택 하 고 **홈** 탭의 **서버에서 지운 편지함 복구** 를 클릭 하 여 Outlook에서이 작업을 수행할 수 있습니다. 삭제 된 항목을 복구 하는 방법에 대 한 자세한 내용은 [Windows 용 Outlook에서 삭제 된 항목 복구](https://go.microsoft.com/fwlink/p/?LinkId=624829)를 참조 하십시오. 
