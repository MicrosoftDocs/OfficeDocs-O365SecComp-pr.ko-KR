---
title: Office 365에서 비활성 사서함 삭제
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 9/5/2017
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: f5caf497-5e8d-4b7a-bfff-d02942f38150
description: 더 이상 Office 365 비활성 사서함의 내용을 보존 하지 않아도 되는 경우에는 보류를 제거 하 여 비활성 사서함을 영구적으로 삭제할 수 있습니다. 보류를 제거한 후 비활성 사서함은 삭제 되도록 표시 되 고 처리 된 후 영구적으로 삭제 됩니다.
ms.openlocfilehash: 0dddbb7c5093519914cbf3a2fc33daf709f0a160
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30220848"
---
# <a name="delete-an-inactive-mailbox-in-office-365"></a>Office 365에서 비활성 사서함 삭제

비활성 사서함은 조직에서 이전 직원의 전자 메일을 보존 하는 데 사용 됩니다. 비활성 사서함의 콘텐츠를 더 이상 보존할 필요가 없는 경우에는 보류를 제거 하 여 비활성 사서함을 영구적으로 삭제할 수 있습니다. 또한 비활성 사서함에 여러 보류가 있을 수 있습니다. 예를 들어 비활성 사서함은 소송 보존 및 하나 이상의 원본 위치 유지에 배치 될 수 있습니다. 또한 office 365 보안 &amp; 준수 센터에서 만든 office 365 보존 정책이 비활성 사서함에 적용 될 수 있습니다. 비활성 사서함에서 모든 보류 및 Office 365 보존 정책을 제거 하 여 삭제 해야 합니다. 보류 및 보존 정책을 제거한 후 비활성 사서함은 삭제 되도록 표시 되며 처리 된 후 영구적으로 삭제 됩니다.
  
> [!IMPORTANT]
> 사서함을 비활성화하기 위해 새 원본 위치 유지를 만들 수 있는 2017년 7월 1일 마감 날짜를 연기했습니다. 하지만 올해 말이나 내년 초에는 Exchange Online에 새 원본 위치 유지를 만들 수 없습니다. 그때는 소송 보존과 Office 365 보존 정책만 사용하여 비활성화 사서함을 만들 수 있습니다. 그러나 원본 위치 유지에 있는 기존 비활성화 사서함은 계속 지원되며 비활성화 사서함에서 원본 위치 유지를 계속 관리할 수 있습니다. 관리 항목으로는 원본 위치 유지 기간 변경 및 원본 위치 유지를 삭제하여 비활성화 사서함을 영구 삭제하는 작업이 포함됩니다. 
  
비활성 사서함에서 보류가 제거 된 후 발생 하는 작업에 대 한 설명을 보려면 [추가 정보](delete-an-inactive-mailbox.md#moreinfo) 섹션을 참조 하세요. 
  
## <a name="before-you-begin"></a>시작하기 전에

- Exchange Online PowerShell을 사용 하 여 비활성 사서함에서 소송 보존을 제거 해야 합니다. EAC (Exchange 관리 센터)를 사용할 수 없습니다. 단계별 지침은 [Exchange Online PowerShell에 연결을](https://go.microsoft.com/fwlink/?linkid=396554)참조 하십시오. Exchange Online PowerShell 또는 EAC를 사용 하 여 비활성 사서함에서 원본 위치 유지를 제거할 수 있습니다. 
    
- 보류를 제거 하 고 비활성 사서함을 삭제 하기 전에 비활성 사서함의 내용을 다른 사서함에 복사할 수 있습니다. 자세한 내용은 [Office 365에서 비활성 사서함 복원을](restore-an-inactive-mailbox.md)참조 하십시오.
    
- 비활성 사서함에서 보류 또는 Office 365 보존 정책을 제거 하는 경우 사서함의 일시 삭제 된 사서함 보존 기간이 만료 되 면 사서함이 영구적으로 삭제 됩니다. 삭제 된 후에는 복구할 수 없습니다. 보류를 제거 하기 전에 사서함의 내용이 더 이상 필요 하지 않은지 확인해 보십시오. 비활성 사서함을 다시 활성화 하려면 복구할 수 있습니다. 자세한 내용은 [Office 365에서 비활성 사서함 복구](recover-an-inactive-mailbox.md)를 참조 하십시오.
    
- 비활성 사서함에 대 한 자세한 내용은 [Office 365의 비활성 사서함](inactive-mailboxes-in-office-365.md)을 참조 하십시오.
    
## <a name="step-1-identify-the-holds-on-an-inactive-mailbox"></a>1 단계: 비활성 사서함의 보류 확인

앞에서 설명한 것 처럼 소송 보존, 원본 위치 유지 또는 Office 365 보관 정책이 비활성 사서함에 배치 될 수 있습니다. 첫 번째 단계는 비활성 사서함에 대 한 보류를 확인 하는 것입니다.
  
다음 명령을 실행 하 여 조직의 모든 비활성 사서함에 대 한 보류 정보를 표시 합니다.
  
```
Get-Mailbox -InactiveMailboxOnly | FL DisplayName,Name,IsInactiveMailbox,LitigationHoldEnabled,InPlaceHolds
```

**LitigationHoldEnabled** 속성의 **True** 값은 비활성 사서함이 소송 보존 상태를 나타냅니다. 비활성 사서함에 원본 위치 유지를 적용 하면 보류에 대 한 GUID가 **InPlaceHolds** 속성의 값으로 표시 됩니다. 예를 들어 두 비활성 사서함에 대 한 다음 결과는 소송 보존을 Ann Beebe에 배치 하 고 두 개의 원본 위치 유지가 Pilar Pinilla에 배치 된다는 것을 보여 줍니다. 
  
```
DisplayName           : Ann Beebe
Name                  : annb
IsInactiveMailbox     : True
LitigationHoldEnabled : True
InPlaceHolds          : {}
...
DisplayName           : Pilar Pinilla
Name                  : pilarp
IsInactiveMailbox     : True
LitigationHoldEnabled : False
InPlaceHolds          : {c0ba3ce811b6432a8751430937152491, ba6f4ba25b62490aaaa253eea27426ab}
```

> [!TIP]
> 전체 원본 위치 유지가 비활성 사서함에 배치 되는 경우에는 원본 위치 유지 guid 중 일부가 표시 되지 않습니다. 다음 명령을 실행 하 여 모든 원본 위치 유지 guid를 표시할 수 있습니다.`Get-Mailbox -InactiveMailboxOnly -Identity <identity of inactive mailbox> | Select-Object -ExpandProperty InPlaceHolds`
  
## <a name="step-2-remove-a-hold-from-an-inactive-mailbox"></a>2 단계: 비활성 사서함에서 보류 제거

비활성 사서함에 적용 되는 보존 유형 및 여러 보류가 있는지 확인 한 후에는 사서함에서 보류를 제거 합니다. 앞에서 설명한 것 처럼 비활성 사서함을 영구적으로 삭제 하려면 모든 보류를 제거 해야 합니다. 
  
### <a name="remove-a-litigation-hold"></a>소송 보존 제거

앞에서 설명한 것 처럼, Windows PowerShell을 사용 하 여 비활성 사서함에서 소송 보존을 제거 해야 합니다. EAC는 사용할 수 없습니다. 다음 명령을 실행 하 여 소송 보존을 제거 합니다.
  
```
Set-Mailbox -InactiveMailbox -Identity <identity of inactive mailbox> -LitigationHoldEnabled $false
```

> [!TIP]
> 비활성 사서함을 식별 하는 가장 좋은 방법은 해당 고유 이름이 나 Exchange GUID 값을 사용 하는 것입니다. 이러한 값 중 하나를 사용 하면 실수로 잘못 된 사서함을 지정 하는 것을 방지할 수 있습니다. 
  
### <a name="remove-in-place-holds"></a>원본 위치 유지 제거

 비활성 사서함에서 원본 위치 유지를 제거 하는 방법에는 두 가지가 있습니다. 
  
- 원본 **위치 유지 개체 삭제** 영구적으로 삭제 하려는 비활성 사서함이 원본 위치 유지를 위한 유일한 사서함 인 경우 현재 위치 유지 개체만 삭제 하면 됩니다. 
    
    > [!NOTE]
    > 원본 위치 유지 개체를 삭제 하려면 먼저 보류를 사용 하지 않도록 설정 해야 합니다. 보류가 사용 되도록 설정 된 원본 위치 유지 개체를 삭제 하려고 하면 오류 메시지가 표시 됩니다. 
  
- **비활성 사서함을 원본 위치 유지의 소스 사서함으로 제거** 원본 위치 유지를 위해 다른 원본 사서함을 유지 하려는 경우 소스 사서함 목록에서 비활성 사서함을 제거 하 고 현재 위치 유지 개체를 유지할 수 있습니다. 
    
#### <a name="use-the-eac-to-delete-an-in-place-hold"></a>EAC를 사용 하 여 원본 위치 유지 삭제

1. 삭제할 원본 위치 유지의 이름을 알고 있는 경우 다음 단계를 진행할 수 있습니다. 그렇지 않으면 다음 명령을 실행 하 여 영구적으로 삭제 하려는 비활성 사서함에 저장 된 원본 위치 유지의 이름을 가져옵니다. [1 단계: 비활성 사서함에서 보류 확인](delete-an-inactive-mailbox.md#step1)에서 얻은 원본 위치 유지 GUID를 사용 합니다.
    
```
  Get-MailboxSearch -InPlaceHoldIdentity <In-Place Hold GUID> | FL Name
```

2. EAC에서 **규정 준수 관리** \> 원본 ** &amp; 위치 eDiscovery 유지**로 이동 합니다.
    
3. 삭제할 원본 위치 유지를 선택 하 고 편집 아이콘](media/ebd260e4-3556-4fb0-b0bb-cc489773042c.gif) **편집** ![을 클릭 합니다.
    
4. 원본 ** &amp; 위치 eDiscovery 보류** 속성 페이지에서 원본 **위치 유지**를 클릭 하 고 **선택한 사서함에 있는 검색 쿼리와 일치 하는 콘텐츠를 보류에** 저장 상자를 선택 취소 한 후에 **Save**를 클릭 합니다.
    
5. 원본 **위치 eDiscovery &amp; 유지** 페이지에서 원본 위치 유지를 다시 선택한 다음 삭제 아이콘 ****![](media/87565fbb-5147-4f22-9ed7-1c18ce664392.png)삭제를 클릭 합니다.
    
6. 경고에서 **예** 를 클릭 하 여 원본 위치 유지를 삭제 합니다. 
    
#### <a name="use-exchange-online-powershell-to-delete-an-in-place-hold"></a>Exchange Online PowerShell을 사용 하 여 원본 위치 유지 삭제

1. 삭제할 원본 위치 유지의 속성을 포함 하는 변수를 만듭니다. [1 단계: 비활성 사서함에서 보류 확인](delete-an-inactive-mailbox.md#step1)에서 얻은 원본 위치 유지 GUID를 사용 합니다.
    
```
  $InPlaceHold = Get-MailboxSearch -InPlaceHoldIdentity <In-Place Hold GUID>
```

2. 원본 위치 유지에 대 한 보류를 사용 하지 않도록 설정 합니다.
    
```
  Set-MailboxSearch $InPlaceHold.Name -InPlaceHoldEnabled $false
```

3. 원본 위치 유지를 삭제 합니다.
    
```
  Remove-MailboxSearch $InPlaceHold.Name
```

#### <a name="use-the-eac-to-remove-an-inactive-mailbox-from-an-in-place-hold"></a>EAC를 사용 하 여 원본 위치 유지에서 비활성 사서함 제거

1. 비활성 사서함에 배치 된 원본 위치 유지의 이름을 알고 있는 경우 다음 단계를 진행할 수 있습니다. 그렇지 않으면 다음 명령을 실행 하 여 사서함에 배치 된 원본 위치 유지의 이름을 가져옵니다. [1 단계: 비활성 사서함에서 보류 확인](delete-an-inactive-mailbox.md#step1)에서 얻은 원본 위치 유지 GUID를 사용 합니다.
    
```
  Get-MailboxSearch -InPlaceHoldIdentity <In-Place Hold GUID> | FL Name
```

2. EAC에서 **규정 준수 관리** \> 원본 ** &amp; 위치 eDiscovery 유지**로 이동 합니다.
    
3. 비활성 사서함에 저장 된 원본 위치 유지를 선택 하 고 편집 아이콘](media/ebd260e4-3556-4fb0-b0bb-cc489773042c.gif) **편집** ![을 클릭 합니다.
    
4. 원본 **위치 eDiscovery &amp; 보류** 속성 페이지에서 **원본을**클릭 합니다.
    
5. 원본 사서함 목록에서 제거 하려는 비활성 사서함의 이름을 클릭 하 고 제거 아이콘](media/adf01106-cc79-475c-8673-065371c1897b.gif) **제거**![를 클릭 합니다.
    
6. **저장** 을 클릭 하 여 변경 내용을 저장 합니다. 작업이 성공적으로 완료 되었음을 알리는 메시지가 표시 됩니다. 
    
7. 비활성 사서함에 저장 된 다른 원본 위치 유지를 제거 하려면 1 ~ 6 단계를 반복 합니다.
    
#### <a name="use-exchange-online-powershell-to-remove-an-inactive-mailbox-from-an-in-place-hold"></a>Exchange Online PowerShell을 사용 하 여 원본 위치 유지에서 비활성 사서함 제거

원본 사서함의 수가 많은 경우에는 비활성 사서함이 EAC의 **원본** 페이지에 나열 되지 않을 수 있습니다. 원본 위치 유지를 편집 하면 **소스** 페이지에 최대 3000의 사서함이 표시 됩니다. 비활성 사서함이 **원본** 페이지에 나열 되지 않은 경우 Exchange Online PowerShell을 사용 하 여 현재 위치 유지에서 제거할 수 있습니다. 
  
1. 비활성 사서함에 배치 된 원본 위치 유지의 속성을 포함 하는 변수를 만듭니다. [1 단계: 비활성 사서함에서 보류 확인](delete-an-inactive-mailbox.md#step1)에서 얻은 원본 위치 유지 GUID를 사용 합니다.
    
```
  $InPlaceHold = Get-MailboxSearch -InPlaceHoldIdentity <In-Place Hold GUID>
```

2. 비활성 사서함이 현재 위치 유지에 대 한 원본 사서함으로 나열 되어 있는지 확인 합니다. 
    
```
  $InPlaceHold.Sources
```

   **참고:** 원본 위치 유지의 *Sources* 속성은 소스 사서함을 해당 *LegacyExchangeDN* 속성으로 식별 합니다. 이 속성은 비활성 사서함을 고유 하 게 식별 하므로 원본 위치 유지의 *Sources* 속성을 사용 하면 잘못 된 사서함을 제거할 수 없습니다. 이는 두 사서함의 별칭이 나 SMTP 주소가 같을 때 발생 하는 문제를 방지 하는 데도 도움이 됩니다. 
   
3. 변수의 원본 사서함 목록에서 비활성 사서함을 제거 합니다. 이전 단계에서 명령에 의해 반환 되는 비활성 사서함의 **LegacyExchangeDN** 을 사용 해야 합니다. 
    
```
  $InPlaceHold.Sources.Remove("<LegacyExchangeDN of the inactive mailbox>")
```

    For example, the following command removes the inactive mailbox for Pilar Pinilla.
    
  ```
  $InPlaceHold.Sources.Remove("/o=contoso/ou=Exchange Administrative Group (FYDIBOHF23SPDLT)/cn=Recipients/cn=9c8dfff651ec4908950f5df60cbbda06-pilarp")
  ```

4. 비활성 사서함이 변수의 원본 사서함 목록에서 제거 되었는지 확인 합니다.
    
```
  $InPlaceHold.Sources
```

5. 비활성 사서함이 포함 되지 않은 업데이트 된 원본 사서함 목록을 사용 하 여 현재 위치 유지를 수정 합니다.
    
```
  Set-MailboxSearch $InPlaceHold.Name -SourceMailboxes $InPlaceHold.Sources
```

6. 현재 위치 유지를 위해 비활성 사서함이 원본 사서함 목록에서 제거 되었는지 확인 합니다.
    
```
  Get-MailboxSearch $InPlaceHold.Name | FL Sources
```

## <a name="more-information"></a>추가 정보

- **비활성 사서함은 일시 삭제 된 사서함의 유형입니다.** Exchange Online에서 일시 삭제 된 사서함은 삭제 되었지만 특정 보존 기간 내에 복구할 수 있는 사서함입니다. Exchange Online의 일시 삭제 된 사서함 보존 기간은 30 일입니다. 즉, 사서함이 일시 삭제 된 30 일 이내에 복구 될 수 있습니다. 30 일이 지나면 일시 삭제 된 사서함이 영구적으로 삭제 되도록 표시 되며 복구할 수 없습니다. 
    
- **비활성 사서함에서 보류를 제거한 후에 수행 되는 작업** 사서함은 일시적으로 삭제 된 다른 사서함 처럼 취급 되며 30 일 일시 삭제 된 사서함 보존 기간이 만료 되 면 영구 삭제로 표시 됩니다. 이 보존 기간은 사서함을 처음으로 비활성화 한 날짜에 시작 됩니다. 이 날짜는 일시 삭제 된 날짜, 즉 해당 Office 365 사용자 계정이 삭제 되었거나 **사서함 제거** cmdlet을 사용 하 여 Exchange Online 사서함이 삭제 된 날짜입니다. 일시 삭제 된 날짜는 보류를 제거한 날짜가 아닙니다. 
    
- **비활성 사서함이 보존을 제거한 즉시 영구적으로 삭제 됩니까?** 비활성 사서함의 일시 삭제 된 날짜가 30 일 보다 오래 된 경우 보존을 제거 하는 즉시 사서함이 영구적으로 삭제 되지 않습니다. 사서함은 영구적으로 삭제 되도록 표시 되며 다음에 처리 될 때 삭제 됩니다. 
    
- **일시 삭제 된 사서함 보존 기간은 비활성 사서함에 어떤 영향을 줍니까?** 비활성 사서함의 일시 삭제 된 날짜가 보존을 제거한 날짜 보다 30 일 보다 많은 경우에는 사서함이 영구적으로 삭제 되도록 표시 됩니다. 그러나 비활성 사서함의 지난 30 일 이내에 일시 삭제 된 날짜가 있고 보존을 제거 하면 일시 삭제 된 사서함 보존 기간이 만료 될 때까지 사서함을 복구할 수 있습니다. 자세한 내용은 [Exchange Online에서 사용자 사서함 삭제 또는 복원을](https://go.microsoft.com/fwlink/?linkid=856835)참조 하십시오. 일시 삭제 된 사서함 보존 기간이 만료 되 면 비활성 사서함을 복구 하기 위한 절차를 따릅니다. 자세한 내용은 [Office 365에서 비활성 사서함 복구](recover-an-inactive-mailbox.md)를 참조 하십시오.
    
- **보류를 제거한 후 비활성 사서함에 대 한 정보를 표시 하는 방법은 무엇 인가요?** 보류를 제거 하 고 비활성 사서함이 일시 삭제 된 사서함으로 다시 되돌아간 후에는 **사서함** cmdlet과 함께 *inactivemailboxonly* 매개 변수를 사용 하 여 반환 되지 않습니다. 그러나 **undo-softdeletedmailbox** 명령을 사용 하 여 사서함에 대 한 정보를 표시할 수 있습니다. 예를 들어: 
    
```
  Get-Mailbox -SoftDeletedMailbox -Identity pilarp | FL Name,Identity,LitigationHoldEnabled,In
  Placeholds,WhenSoftDeleted,IsInactiveMailbox
  Name                   : pilarp
  Identity               : Soft Deleted Objects\pilarp
  LitigationHoldEnabled  : False
  InPlaceHolds           : {}
  WhenSoftDeleted        : 10/30/2014 1:19:04 AM
  IsInactiveMailbox      : False
```
  
위의 예제에서, 다음 예제 ** 에서는 일시 삭제 된 날짜를 식별 하며이 예에서는 10 월 30 일을 2014 합니다. 이 일시 삭제 된 사서함이 보존을 제거한 이전에 비활성화 된 사서함 인 경우에는 소송 *소프트 deleted* 속성 값 다음에 30 일이 영구적으로 삭제 됩니다. 이 경우 사서함은 11 월 30 일 이후에 영구적으로 삭제 됩니다.

