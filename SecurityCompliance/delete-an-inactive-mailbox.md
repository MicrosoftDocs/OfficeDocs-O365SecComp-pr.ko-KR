---
title: Office 365에서 비활성 사서함 삭제
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 9/5/2017
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: f5caf497-5e8d-4b7a-bfff-d02942f38150
description: 더이상 Office 365 비활성 사서함의 내용을 보존 해야하는 경우에 보류를 제거 하 여 비활성 사서함을 영구적으로 삭제할 수 없습니다. 보류를 제거한 후 비활성 사서함 삭제 하도록 표시 하 고 처리 된 후에 영구적으로 삭제 됩니다.
ms.openlocfilehash: 91b73fff6ca319735289abe7ea9351b5fba931a0
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22532970"
---
# <a name="delete-an-inactive-mailbox-in-office-365"></a>Office 365에서 비활성 사서함 삭제

비활성 사서함이 자신이 조직을 떠난 후 이전 직원의 전자 메일을 유지 하기 위해 사용 됩니다. 더이상 비활성 사서함의 내용을 보존 해야하는 경우에 보류를 제거 하 여 비활성 사서함을 영구적으로 삭제할 수 없습니다. 또한 것 여러 보존 비활성 사서함에 배치 될 수 있습니다. 예, 하나 이상의 원본 위치 유지 및 소송 보존으로 설정에서 비활성 사서함에 배치할 수 수 있습니다. 또한는 Office 365 보존 정책 (Office 365 보안에서 만든 &amp; 준수 센터) 비활성 사서함에 적용할 수 있습니다. 모든 보류 및 Office 365 보존 정책을 삭제 하려면 비활성 사서함에서 제거 해야 합니다. 보류 및 보존 정책을 제거한 후 비활성 사서함 삭제 하도록 표시 하 고 처리 된 후에 영구적으로 삭제 됩니다.
  
> [!IMPORTANT]
> 사서함을 비활성화하기 위해 새 원본 위치 유지를 만들 수 있는 2017년 7월 1일 마감 날짜를 연기했습니다. 하지만 올해 말이나 내년 초에는 Exchange Online에 새 원본 위치 유지를 만들 수 없습니다. 그때는 소송 보존과 Office 365 보존 정책만 사용하여 비활성화 사서함을 만들 수 있습니다. 그러나 원본 위치 유지에 있는 기존 비활성화 사서함은 계속 지원되며 비활성화 사서함에서 원본 위치 유지를 계속 관리할 수 있습니다. 관리 항목으로는 원본 위치 유지 기간 변경 및 원본 위치 유지를 삭제하여 비활성화 사서함을 영구 삭제하는 작업이 포함됩니다. 
  
비활성 사서함에서 보류를 제거한 후 수행 하는 작업에 대 한 설명에 대 한 [자세한 내용](delete-an-inactive-mailbox.md#moreinfo) 은 섹션을 참조 하십시오. 
  
## <a name="before-you-begin"></a>시작하기 전에

- 비활성 사서함에서 소송 보존을 제거 하려면 Exchange Online PowerShell을 사용 해야 합니다. Exchange 관리 센터 (EAC)를 사용할 수 없습니다. 단계별 지침은 [Connect to Exchange Online PowerShell를](https://go.microsoft.com/fwlink/?linkid=396554)참조 하십시오. 비활성 사서함에서 유지 하는 위치를 제거 하려면 Exchange Online PowerShell 또는 EAC를 사용할 수 있습니다. 
    
- 보류를 제거 하 고 비활성 사서함을 삭제 하기 전에 비활성 사서함의 내용을 다른 사서함에 복사할 수 있습니다. 자세한 내용은 [Office 365에서 비활성 사서함 복원](restore-an-inactive-mailbox.md)을 참조 하십시오.
    
- 비활성 사서함에서 보류 또는 Office 365 보존 정책을 제거 하는 경우 사서함에 대 한 일시 삭제 된 사서함 보존 기간이 만료 된 사서함 영구적으로 삭제 됩니다. 삭제 한 후에 복구할 수 없습니다. 보류를 제거 하기 전에 사서함의 내용이 필요 없는 해야 합니다. 비활성 사서함을 다시 활성화 하려는 경우에이 복구할 수 있습니다. 자세한 내용은 [Office 365에서 비활성 사서함 복구](recover-an-inactive-mailbox.md)를 참조 합니다.
    
- 비활성 사서함에 대 한 자세한 내용은 [Office 365에서 비활성 사서함](inactive-mailboxes-in-office-365.md)을 참조 하십시오.
    
## <a name="step-1-identify-the-holds-on-an-inactive-mailbox"></a>1 단계: 비활성 사서함에서 보류를 식별 합니다.

앞서 설명한 것 처럼 비활성 사서함에 소송 보존으로 설정, 원본 위치 유지 또는 Office 365 보존 정책에 배치할 수 있습니다. 첫번째 단계 비활성 사서함에서 보류를 식별 하는 것입니다.
  
조직에서 모든 비활성 사서함에 대 한 보류 정보를 표시 하려면 다음 명령을 실행 합니다.
  
```
Get-Mailbox -InactiveMailboxOnly | FL DisplayName,Name,IsInactiveMailbox,LitigationHoldEnabled,InPlaceHolds
```

**LitigationHoldEnabled** 속성에 대 한 값 **True** 소송 보존으로 설정에서 비활성 사서함 인지를 나타냅니다. 비활성 사서함에 배치 되는 원본 위치 유지를 보류에 대 한 GUID **InPlaceHolds** 속성에 대 한 값으로 표시 됩니다. 예, 두 비활성 사서함에 대 한 다음과 같은 결과가 Ann Beebe에 배치 되는 소송 보존으로 설정 하 고는 Pilar Pinilla에 배치 되 두 원본 위치 유지를 표시 합니다. 
  
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
> 원본 위치 유지 많은 비활성 사서함에 배치 되, 원본 위치 유지 Guid 중 일부만 표시 됩니다. 모든 원본 위치 유지 Guid를 표시 하려면 다음 명령을 실행할 수 있습니다.`Get-Mailbox -InactiveMailboxOnly -Identity <identity of inactive mailbox> | Select-Object -ExpandProperty InPlaceHolds`
  
## <a name="step-2-remove-a-hold-from-an-inactive-mailbox"></a>2 단계: 비활성 사서함에서 보류를 제거 합니다.

비활성 사서함에 어떤 유형의 보류 놓입니다 파악 한 후 (및 여러 보존 한지), 다음 단계는 사서함에서 보류를 제거 하는 것입니다. 앞서 설명한 것 처럼 비활성 사서함을 영구적으로 삭제 하려면 모든 보류를 제거 해야 합니다. 
  
### <a name="remove-a-litigation-hold"></a>소송 보존을 제거 합니다.

앞서 설명한 것 처럼 비활성 사서함에서 소송 보존을 제거 하려면 Windows PowerShell을 사용 해야 합니다. EAC를 사용할 수 없습니다. 소송 보존을 제거 하려면 다음 명령을 실행 합니다.
  
```
Set-Mailbox -InactiveMailbox -Identity <identity of inactive mailbox> -LitigationHoldEnabled $false
```

> [!TIP]
> 비활성 사서함을 식별 하는 가장 좋은 방법은 고유 이름 또는 Exchange GUID 값을 사용 하 여 됩니다. 이러한 값 중 하나를 사용 하 여 실수로 잘못 된 사서함을 지정 방지할 수 있습니다. 
  
### <a name="remove-in-place-holds"></a>원본 위치 유지를 제거 합니다.

 두 가지 방법으로 비활성 사서함에서 In-place Hold를 제거할 수 있습니다. 
  
- **원본 위치 유지 개체를 삭제 합니다.** 원본 위치 유지 하는 것에 대 한 유일한 원본 사서함을 영구적으로 삭제 하려는 비활성 사서함을 사용 하는 경우에 In-place Hold 개체를 삭제할 수 있습니다. 
    
    > [!NOTE]
    > 원본 위치 유지 개체를 삭제 하기 전에 보류를 사용 하지 않도록 설정 해야 합니다. 원본 위치 유지 된 개체를 사용 하도록 설정 하는 보류를 삭제 하려고 하면 오류 메시지가 받게 됩니다. 
  
- **원본 위치 유지 원본 사서함으로 비활성 사서함 제거** In-place Hold에 대 한 다른 원본 사서함을 유지 하려는 경우에 원본 사서함의 목록에서 비활성 사서함을 제거할 수 있으며 In-place Hold 개체를 유지 수 있습니다. 
    
#### <a name="use-the-eac-to-delete-an-in-place-hold"></a>EAC를 사용 하 여 원본 위치 유지를 삭제 하려면

1. 삭제 하려는 원본 위치 유지의 이름을 알고 있는 경우에 다음 단계를 진행할 수 있습니다. 그렇지 않은 경우 비활성 사서함을 영구적으로 삭제 하려는에 배치 되는 원본 위치 유지의 이름을 가져오려면 다음 명령을 실행 합니다. 얻은 원본 위치 유지 GUID를 사용 하 여 [1 단계: 비활성 사서함에서 보류를 식별](delete-an-inactive-mailbox.md#step1)합니다.
    
```
  Get-MailboxSearch -InPlaceHoldIdentity <In-Place Hold GUID> | FL Name
```

2. EAC에서 **규정 준수 관리** 로 이동 \> **원본 위치 eDiscovery &amp; 유지**합니다.
    
<<<<<<< HEAD
3. 삭제 하려는 원본 위치 유지를 선택 하 고 **편집** 을 클릭 한 다음 ![편집 아이콘](media/ebd260e4-3556-4fb0-b0bb-cc489773042c.gif)합니다.
=======
3. 삭제 하려는 원본 위치 유지를 선택 하 고 **편집**을 클릭 한 다음! [아이콘 편집](media/ebd260e4-3556-4fb0-b0bb-cc489773042c.gif)합니다.
>>>>>>> markjjo 변환
    
4. **원본 위치 eDiscovery &amp; 유지** 속성 페이지, **원본 위치 유지**를 클릭, **선택한 사서함에서 검색 쿼리 일치에 전체 콘텐츠 유지** 확인란의 선택을 취소 한 다음 **저장**을 클릭 합니다.
    
5. **원본 위치 eDiscovery &amp; 유지** 페이지, 원본 위치 유지를 다시 선택 하 고 **삭제**를 클릭 한 다음![삭제 아이콘](media/87565fbb-5147-4f22-9ed7-1c18ce664392.png)합니다.
    
6. 경고에서 **예** 를 원본 위치 유지 삭제를 클릭 합니다. 
    
#### <a name="use-exchange-online-powershell-to-delete-an-in-place-hold"></a>Exchange Online PowerShell을 사용 하 여 원본 위치 유지를 삭제 하려면

1. 삭제 하려는 원본 위치 유지의 속성을 포함 하는 변수를 만듭니다. 얻은 원본 위치 유지 GUID를 사용 하 여 [1 단계: 비활성 사서함에서 보류를 식별](delete-an-inactive-mailbox.md#step1)합니다.
    
```
  $InPlaceHold = Get-MailboxSearch -InPlaceHoldIdentity <In-Place Hold GUID>
```

2. 원본 위치 유지에서 보류를 사용 하지 않도록 설정 합니다.
    
```
  Set-MailboxSearch $InPlaceHold.Name -InPlaceHoldEnabled $false
```

3. 원본 위치에 보류를 삭제 합니다.
    
```
  Remove-MailboxSearch $InPlaceHold.Name
```

#### <a name="use-the-eac-to-remove-an-inactive-mailbox-from-an-in-place-hold"></a>EAC를 사용 하 여 In-place Hold에서 비활성 사서함을 제거 하려면

1. 비활성 사서함에 배치 된 원본 위치 유지의 이름을 알고 있는 경우에 다음 단계를 진행할 수 있습니다. 그렇지 않은 경우 원본 위치 유지는 사서함에 배치의 이름을 가져오려면 다음 명령을 실행 합니다. 얻은 원본 위치 유지 GUID를 사용 하 여 [1 단계: 비활성 사서함에서 보류를 식별](delete-an-inactive-mailbox.md#step1)합니다.
    
```
  Get-MailboxSearch -InPlaceHoldIdentity <In-Place Hold GUID> | FL Name
```

2. EAC에서 **규정 준수 관리** 로 이동 \> **원본 위치 eDiscovery &amp; 유지**합니다.
    
3. 비활성 사서함에 배치 된 원본 위치 유지를 선택 하 고 **편집** 을 클릭 한 다음 ![편집 아이콘](media/ebd260e4-3556-4fb0-b0bb-cc489773042c.gif)합니다.
    
4. **원본 위치 eDiscovery &amp; 유지** 속성 페이지에서 **소스**를 클릭 합니다.
    
5. 원본 사서함의 목록에서 제거 하려는 비활성 사서함의 이름을 클릭 하 고 **제거**를 클릭 한 다음![제거 아이콘](media/adf01106-cc79-475c-8673-065371c1897b.gif)합니다.
    
6. 변경 내용을 저장 하려면 **저장** 을 클릭 합니다. 메시지는 작업이 성공적으로 완료 되었다는 표시 됩니다. 
    
7. 1 ~ 비활성 사서함에 배치 다른 원본 위치 유지를 제거 하는 6 단계를 반복 합니다.
    
#### <a name="use-exchange-online-powershell-to-remove-an-inactive-mailbox-from-an-in-place-hold"></a>Exchange Online PowerShell을 사용 하 여 In-place Hold에서 비활성 사서함을 제거 하려면

원본 위치 유지 많은 수의 원본 사서함을 포함 하는 경우에 가능한 EAC에서 **원본** 페이지에서 비활성 사서함은 표시 되지 않습니다. 최대 3, 000 사서함은 **원본** 페이지에서을 편집할 때 표시는 원본 위치 유지 합니다. 비활성 사서함이 있는 **원본** 페이지에 나열 되지 않으면 현재 위치 유지에서 제거 하려면 Exchange Online PowerShell를 사용할 수 있습니다. 
  
1. 비활성 사서함에 배치 원본 위치 유지의 속성을 포함 하는 변수를 만듭니다. 얻은 원본 위치 유지 GUID를 사용 하 여 [1 단계: 비활성 사서함에서 보류를 식별](delete-an-inactive-mailbox.md#step1)합니다.
    
```
  $InPlaceHold = Get-MailboxSearch -InPlaceHoldIdentity <In-Place Hold GUID>
```

2. 원본 위치 유지 하는 것에 대 한 비활성 사서함을 원본 사서함으로 표시 되는지 확인 합니다. 
    
```
  $InPlaceHold.Sources
```

   **참고:** 원본 위치 유지 *원본* 속성은 해당 *LegacyExchangeDN* 속성에 의해 원본 사서함을 식별합니다. 이 속성은 비활성 사서함 고유 하 게 식별, 원본 위치 유지에서 *원본* 속성을 사용 하는 잘못 된 사서함을 제거를 방지 합니다. 두 사서함 동일한 별칭 또는 SMTP 주소를 포함 하는 경우 문제를 방지 하기 위해도 도움이 됩니다. 
   
3. 변수에 원본 사서함 목록에서 비활성 사서함을 제거 합니다. 이전 단계에서 명령에 의해 반환 되는 비활성 사서함의 **LegacyExchangeDN** 을 사용 해야 합니다. 
    
```
  $InPlaceHold.Sources.Remove("<LegacyExchangeDN of the inactive mailbox>")
```

    For example, the following command removes the inactive mailbox for Pilar Pinilla.
    
  ```
  $InPlaceHold.Sources.Remove("/o=contoso/ou=Exchange Administrative Group (FYDIBOHF23SPDLT)/cn=Recipients/cn=9c8dfff651ec4908950f5df60cbbda06-pilarp")
  ```

4. 비활성 사서함 변수에 원본 사서함 목록에서 제거를 확인 합니다.
    
```
  $InPlaceHold.Sources
```

5. 비활성 사서함을 포함 하지는 원본 사서함의 업데이트 된 목록을 사용 하 여 원본 위치 유지를 수정 합니다.
    
```
  Set-MailboxSearch $InPlaceHold.Name -SourceMailboxes $InPlaceHold.Sources
```

6. 원본 위치 유지 하는 것에 대 한 원본 사서함 목록에서 비활성 사서함을 제거를 확인 합니다.
    
```
  Get-MailboxSearch $InPlaceHold.Name | FL Sources
```

## <a name="more-information"></a>추가 정보

- **비활성 사서함을 사용 하면 일시 삭제 된 사서함의 형식이.** Exchange Online에서 일시 삭제 된 사서함: 특정 보존 기간 내에서 복구할 수 있지만 삭제 된 사서함 Exchange Online에서 일시 삭제 된 사서함 보존 기간 30 일입니다. 즉, 사서함 삭제 되 고 소프트-30 일 이내 복구할 수 있습니다. 30 일 후 일시 삭제 된 사서함 영구적으로 삭제에 대 한 표시 하 고 복구할 수 없습니다. 
    
- **비활성 사서함에서 보류를 제거한 후 어떻게 됩니까?** 사서함 다른 일시 삭제 된 사서함 처럼 인식 되 고 30 일 일시 삭제 된 사서함 보존 기간이 만료 후 영구적으로 삭제를 위해 표시 됩니다. 이 보존 기간 때 사서함을 처음 설정한 비활성 날짜에 시작 합니다. 이 날짜를 날짜 해당 Office 365 사용자 계정이 삭제 되었습니다 또는 **Remove-mailbox** cmdlet을 통해 Exchange Online 사서함을 삭제 하는 경우 일시 삭제 된 날짜를 라고 합니다. 일시 삭제 된 날짜 보류를 제거 하는 날짜를 하지 않습니다. 
    
- **보존이 제거 된 후에 즉시 영구적으로 삭제 비활성 사서함은?** 비활성 사서함에 대 한 일시 삭제 된 날짜를 30 일 보다 오래 된 경우 보류를 제거 하는 즉시 영구적으로 사서함 삭제 되지 않습니다. 사서함은 영구적으로 삭제에 대 한 표시 하 고 처리 하는 다음 번 삭제 됩니다. 
    
- **일시 삭제 된 사서함 보존 기간에 주는 영향은 비활성 사서함?** 비활성 사서함에 대 한 일시 삭제 된 날짜 보류에서 제거 된 날짜 이전 30 일이 지난 경우 영구적으로 삭제에 대 한 사서함 된다고 나타납니다. 하지만 일시 삭제 된 사서함 보존 기간이 만료 될 때까지 사서함 비활성 사서함의 일시 삭제 된 날짜가 지난 30 일 내에서 보류를 제거 하는 경우 복구할 수 있습니다. 자세한 내용은, [삭제 또는 Exchange Online 사용자 사서함을 복원](https://go.microsoft.com/fwlink/?linkid=856835)을 참조 하십시오. 일시 삭제 된 사서함 보존 기간이 만료 되 면 후 비활성 사서함을 복구 하기 위한 절차에 따라 포함 합니다. 자세한 내용은 [Office 365에서 비활성 사서함 복구](recover-an-inactive-mailbox.md)를 참조 합니다.
    
- **을 표시 하려면 어떻게 비활성 사서함에 대 한 정보 보존이 제거 후?** 보류에서 제거 된 후 일시 삭제 된 사서함에 다시 비활성 사서함은으로 **Get-mailbox** cmdlet과 함께 *InactiveMailboxOnly* 매개 변수를 사용 하 여 반환 되지 않습니다. 하지만 **Get-mailbox SoftDeletedMailbox** 명령을 사용 하 여 사서함에 대 한 정보를 표시할 수 있습니다. 예를 들어: 
    
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
  
위의 예제에서는 *WhenSoftDeleted* 속성은이 예에서 2014 년 10 월 30,이 일시 삭제 된 날짜를 식별 합니다. 일시 삭제 된 사서함이 된 경우 이전에 보류 제거 된 비활성 사서함, *WhenSoftDeleted* 속성의 값 후 30 일을 영구적으로 삭제 됩니다. 이 경우에 사서함이 2014 년 11 월 30, 후 영구적으로 삭제 됩니다.

