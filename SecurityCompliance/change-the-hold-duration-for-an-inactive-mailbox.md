---
title: Office 365에서 비활성 사서함에 대 한 보존 기간 변경
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 8/29/2017
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: bdee24ed-b8cf-4dd0-92ae-b86ec4661e6b
description: Office 365 사서함 비활성 이루어진 후 보류 또는 비활성 사서함에 할당 하는 Office 365 보존 정책의 기간을 변경할 수 있습니다. 보류 기간 폴더에 보관 된 복구 가능한 항목에 얼마나 오래 항목을 정의 합니다.
ms.openlocfilehash: 22bd9f9294b625a38d243f6235097d1aee437121
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22533534"
---
# <a name="change-the-hold-duration-for-an-inactive-mailbox-in-office-365"></a>Office 365에서 비활성 사서함에 대 한 보존 기간 변경

비활성 사서함을 사용 하 여가 자신이 조직을 떠난 후 이전 직원의 전자 메일을 유지 합니다. 사서함이 소송 보존, In-place Hold, Office 365 보존 정책 때 비활성화 또는 eDiscovery 사례와 관련 된 보류의 사서함에 배치 하 고 해당 하는 Office 365 사용자 계정의 삭제 됩니다. 비활성 사서함의 내용은 비활성 적용 되기 전에 사서함에 배치 된 보류의 기간에 대 한 보관 됩니다. 보류 기간 폴더에 보관 된 복구 가능한 항목에 얼마나 오래 항목을 정의 합니다. 복구 가능한 항목 폴더에 있는 항목에 대 한 보존 기간 만료 되 면 해당 항목은 영구적으로 삭제 (비우기) 비활성 사서함에서. 사서함 비활성 이루어진 후 보류 또는 비활성 사서함에 할당 하는 Office 365 보존 정책의 기간을 변경할 수 있습니다.
  
> [!IMPORTANT]
> 사서함을 비활성화하기 위해 새 원본 위치 유지를 만들 수 있는 2017년 7월 1일 마감 날짜를 연기했습니다. 하지만 올해 말이나 내년 초에는 Exchange Online에 새 원본 위치 유지를 만들 수 없습니다. 그때는 소송 보존과 Office 365 보존 정책만 사용하여 비활성화 사서함을 만들 수 있습니다. 그러나 원본 위치 유지에 있는 기존 비활성화 사서함은 계속 지원되며 비활성화 사서함에서 원본 위치 유지를 계속 관리할 수 있습니다. 관리 항목으로는 원본 위치 유지 기간 변경 및 원본 위치 유지를 삭제하여 비활성화 사서함을 영구 삭제하는 작업이 포함됩니다. 
  
## <a name="before-you-begin"></a>시작하기 전에

- 비활성 사서함에 소송 보존에 대 한 보존 기간을 변경 하려면 Exchange Online PowerShell을 사용 해야 합니다. Exchange 관리 센터 (EAC)를 사용할 수 없습니다. 하지만 유지 하는 위치에 대 한 보존 기간을 변경 하려면 Exchange Online PowerShell 또는 EAC를 사용할 수 있습니다. Office 365 보안을 사용 하 여 수 &amp; 준수 센터 또는 보안 &amp; 는 Office 365 보존 정책에 대 한 보존 기간을 변경 하려면 준수 센터 PowerShell 합니다.
    
- Exchange Online PowerShell 또는 보안 연결을 &amp; 준수 센터 PowerShell, 다음 항목 중 하나를 참조 합니다.
    
  - [원격 PowerShell을 사용하여 Exchange Online에 연결](https://go.microsoft.com/fwlink/p/?linkid=396554)
    
  - [Office 365 보안 연결할 &amp; 준수 센터 PowerShell](https://go.microsoft.com/fwlink/?linkid=799771)
    
- EDiscovery 사례와 관련 된 메모를 포함 하는 변경할 수 있는 보존 기간이 없는 것을 의미 하는 무한 보존 됩니다. 항목 보류에서 제거 되 고 비활성 사서함 삭제 될 때까지 또는 무제한 보관 됩니다.
    
- 비활성 사서함에 대 한 자세한 내용은 [Office 365에서 비활성 사서함](inactive-mailboxes-in-office-365.md)을 참조 하십시오.
    
## <a name="step-1-identify-the-holds-on-an-inactive-mailbox"></a>1 단계: 비활성 사서함에서 보류를 식별 합니다.

다양 한 유형의 보류 또는 하나 이상의 Office 365 보존 정책을 비활성 사서함에 배치 될 수 있습니다, 때문에 비활성 사서함에서 보류를 식별 하는 첫번째 단계가입니다.
  
다음 명령을 실행 Exchange Online 조직에서 모든 비활성 사서함에 대 한 보류 정보를 표시 하는 PowerShell 합니다.
  
```
Get-Mailbox -InactiveMailboxOnly | FL DisplayName,Name,IsInactiveMailbox,LitigationHoldEnabled,LitigationHoldDuration,InPlaceHolds
```
   
**LitigationHoldEnabled** 속성에 대 한 값 **True** 소송 보존으로 설정에서 비활성 사서함 인지를 나타냅니다. EDiscovery 유지 원본 위치 유지 또는 Office 365 보존 정책 비활성 사서함에 배치 되는 경우 보류 또는 보존 정책에 대 한 GUID **InPlaceHolds** 속성에 대 한 값으로 표시 됩니다. 예 다음 5 비활성 사서함에 대 한 결과 표시 합니다. 
  
||
|:-----|
|
```
DisplayName           : Ann Beebe
Name                  : annb
IsInactiveMailbox     : True
LitigationHoldEnabled : True
LitigationHoldDuration: 365.00:00:00
InPlaceHolds          : {}
...
DisplayName           : Pilar Pinilla
Name                  : pilarp
IsInactiveMailbox     : True
LitigationHoldEnabled : False
LitigationHoldDuration: Unlimited
InPlaceHolds          : {c0ba3ce811b6432a8751430937152491}
...
DisplayName           : Mario Necaise
Name                  : marion
IsInactiveMailbox     : True
LitigationHoldEnabled : False
LitigationHoldDuration: Unlimited
InPlaceHolds          : {}
...
DisplayName           : Carol Olson
Name                  : carolo
IsInactiveMailbox     : True
LitigationHoldEnabled : False
LitigationHoldDuration: Unlimited
InPlaceHolds          : {mbxcdbbb86ce60342489bff371876e7f224}
...
DisplayName           : Abraham McMahon
Name                  : abrahamm
IsInactiveMailbox     : True
LitigationHoldEnabled : False
LitigationHoldDuration: Unlimited
InPlaceHolds          : {UniH7d895d48-7e23-4a8d-8346-533c3beac15d}
```
   
다음 표에서 각 사서함을 비활성화 하려면 사용 된 다섯 개의 서로 다른 보류 형식을 식별 합니다.
  
|**비활성 사서함**|**종류를 유지 합니다.**|**비활성 사서함에서 보류를 식별 하는 방법**|
|:-----|:-----|:-----|
|Ann Beebe  <br/> |소송 보존  <br/> |*LitigationHoldEnabled* 속성이로 설정 된 `True`합니다.  <br/> |
|Pilar Pinilla  <br/> |원본 위치 유지  <br/> |*InPlaceHolds* 속성은 비활성 사서함에 배치 된 원본 위치 유지의 GUID를 포함 합니다. 이 In-place Hold ID를 접두사로 시작 되지 않으면 때문에 알 수 있습니다.<br/> 사용할 수는 ' Get-mailboxsearch InPlaceHoldIdentity<hold GUID> | FL' 비활성 사서함에서 원본 위치 유지 하는 방법에 대 한 정보를 얻을 수 있는 Exchange Online PowerShell에서 명령 합니다.  <br/> |
|Mario 씨 Necaise  <br/> |보안에서 조직 전체의 Office 365 보존 정책 &amp; 준수 센터  <br/> |*InPlaceHolds* 속성이 비어 있습니다. 이 하나 이상의 조직 차원의 또는 (Exchange 전체) Office 365 보존 정책 비활성 사서함에 적용 되는 것을 나타냅니다. 이 경우에 실행할 수 있습니다는 ' Get-organizationconfig | Select-object-ExpandProperty InPlaceHolds` command in Exchange Online PowerShell to get a list of the GUIDs for organization-wide Office 365 retention policies. The GUID for organization-wide retention policies that are applied to Exchange mailboxes start with the  `mbx` prefix; for example  `mbxa3056bb15562480fadb46ce523ff7b02`.  <br/> <br/>To identity the Office 365 retention policy that's applied to the inactive mailbox, run the following command in Security &amp; Compliance Center PowerShell.  <br/><br/> `Get RetentionCompliancePolicy<retention policy GUID without prefix> | FL 이름 '<br/><br/>
|Carol Olson  <br/> |보안에서 office 365 보존 정책 &amp; 준수 센터 특정 사서함에 적용  <br/> |*InPlaceHolds* 속성은 비활성 사서함에 적용 되는 Office 365 보존 정책의 GUID가 포함 됩니다. 이 보존 정책으로 시작 하는 GUID 하기 때문에 특정 사서함에 적용 하는 것을 알 수 있습니다는 `mbx` 접두사입니다. 비활성 사서함에 적용 된 보존 정책의 GUID를 시작 하는 경우는 `skp` 접두사를 나타내는 것 비즈니스 대화에 대 한 보존 정책이 Skype에 적용 됩니다.<br/><br/> 비활성 사서함에 적용 되는 Office 365 identity 보존 정책, 보안에서 다음 명령을 실행 &amp; 준수 센터 PowerShell 합니다.<br/><br/> ' Get RetentionCompliancePolicy<retention policy GUID without prefix> | FL 이름` <br/><br/>Be sure to remove the  `mbx` or  `skp'이 명령을 실행 하면 접두사입니다.  <br/> |
|Abraham McMahon  <br/> |eDiscovery 사례 유지 (영문) 보안 &amp; 준수 센터  <br/> |*InPlaceHolds* 속성은 비활성 사서함에 배치 되는 eDiscovery 사례 보류의 GUID를 포함 합니다. 이런 현상이 발생 eDiscovery 사례 보류도 시작 하는 GUID를 알 수는 `UniH` 접두사입니다.<br/> 사용할 수 있습니다는 `Get-CaseHoldPolicy` 보안에서 cmdlet &amp; 준수 센터 PowerShell 보류 비활성 사서함에 연결 된 eDiscovery 사례에 대 한 정보를 얻을 수 있습니다. 명령을 실행할 수 등 ' Get CaseHoldPolicy<hold GUID without prefix> | FL 이름` to display the name of the case hold that's on the inactive mailbox. Be sure to remove the  `UniH` prefix when you run this command.  <br/><br/> To identity the eDiscovery case that the hold on the inactive mailbox is associated with, run the following commands.  <br/><br/> `$CaseHold Get CaseHoldPolicy = <hold GUID without prefix> `<br/><br/> `Get ComplianceCase $CaseHold.CaseId | FL 이름 '<br/><br/><br/> **참고:** 비활성 사서함에 대 한을 포함 하 고 eDiscovery를 사용 하 여 하지 것이 좋습니다. 법적 문제와 관련 된 특정, 시간 제한이 사례를 위한 eDiscovery 사례 때문입니다. 특정 시점 법률 사례 아마도 종료 하 고 대/소문자와 관련 된 보류 제거 되 고 eDiscovery 사례 됩니다 (닫히거나 삭제). 실제로 비활성 사서함에 배치 되는 보류 eDiscovery 사례와 연결 하 고 보류가 이거나 eDiscovery 사례 닫히거나 삭제 하는 경우 비활성 사서함 영구적으로 삭제 됩니다. 

Office 365 보존 정책에 대 한 자세한 내용은 [보존 정책 개요](retention-policies.md)를 참조 하십시오.
  
## <a name="step-2-change-the-hold-duration-for-an-inactive-mailbox"></a>비활성 사서함에 대 한 보존 기간을 변경 하는 2 단계:

비활성 사서함에 어떤 유형의 보류 놓입니다 파악 한 후 (및 여러 보존 한지), 다음 단계를 보류에 대 한 기간을 변경 하는 것입니다. 
  
### <a name="change-the-duration-for-a-litigation-hold"></a>소송 보존에 대 한 기간을 변경 합니다.

비활성 사서함에 배치 되는 소송 보존에 대 한 보존 기간을 변경 하려면 Exchange Online PowerShell을 사용 하는 방법을 다음과 같습니다. EAC를 사용할 수 없습니다. 보존 기간을 변경 하려면 다음 명령을 실행 합니다. 이 예제에서는 대기 기간 제한 없음된 기간으로 변경 됩니다.
  
```
Set-Mailbox -InactiveMailbox -Identity <identity of inactive mailbox> -LitigationHoldDuration unlimited
```

비활성 사서함의 항목은 무기한 또는 보존이 제거 되거나 보존 기간의 다른 값으로 변경 될 때까지 유지 되는 것이 반환이 됩니다.
  
> [!TIP]
> 비활성 사서함을 식별 하는 가장 좋은 방법은 **고유 이름** 또는 **Exchange GUID** 값을 사용 하 여 됩니다. 이러한 값 중 하나를 사용 하 여 실수로 잘못 된 사서함을 지정 방지할 수 있습니다. 
  
### <a name="change-the-duration-for-an-in-place-hold"></a>원본 위치 유지 하는 것에 대 한 기간을 변경 합니다.

 EAC 또는 Exchange Online PowerShell 유지 하는 위치에 대 한 보존 기간을 변경 하려면 사용할 수 있습니다. 
  
#### <a name="use-the-eac-to-change-the-hold-duration"></a>EAC를 사용 하 여 보존 기간을 변경 하려면

1. 이름을 변경 하려는 원본 위치 유지를 알고 있는 경우에 다음 단계로 이동 합니다. 그렇지 않은 경우 비활성 사서함에 배치 된 원본 위치 유지의 이름을 가져오려면 다음 명령을 실행 합니다. [1 단계에서](#step-1-identify-the-holds-on-an-inactive-mailbox)에서 구한는 원본 위치 유지 GUID를 사용 합니다.

    ```
    Get-MailboxSearch -InPlaceHoldIdentity <In-Place Hold GUID> | FL Name
    ```

2. EAC에서 **규정 준수 관리** 로 이동 \> **원본 위치 eDiscovery &amp; 유지**합니다.
    
3. 변경 하려는 원본 위치 유지를 선택 하 고 **편집** 을 클릭 한 다음 ![편집 아이콘](media/ebd260e4-3556-4fb0-b0bb-cc489773042c.gif)합니다.
    
4. **원본 위치 eDiscovery &amp; 유지** 속성 페이지에서 **원본 위치 유지**를 클릭 합니다. 
    
5. 기간을 유지 현재에 따라 다음 중 하나:
    
1. 무제한 기간에 대 한 항목을 보존 하려면 **무기한 유지** 를 클릭 합니다. 
    
2. 특정 기간에 대 한 항목을 유지 하려면 **자신의 받은 날짜를 기준으로 항목을 보관할 일 번호 지정** 클릭 합니다. 항목에 대 한 유지 하려는 일 수를 입력 합니다. 
    
    ![원본 위치 유지 기간을 변경하는 작업의 스크린샷입니다.](media/cfcfd92a-9d65-40c0-90ef-ab72697b0166.png)
  
6. **저장**을 클릭합니다.
    
#### <a name="use-exchange-online-powershell-to-change-the-hold-duration"></a>Exchange Online PowerShell을 사용 하 여 보존 기간을 변경 하려면

1. 이름을 변경 하려는 원본 위치 유지를 알고 있는 경우에 다음 단계로 이동 합니다. 그렇지 않은 경우 비활성 사서함에 배치 된 원본 위치 유지의 이름을 가져오려면 다음 명령을 실행 합니다. [1 단계에서](#step-1-identify-the-holds-on-an-inactive-mailbox)에서 구한는 원본 위치 유지 GUID를 사용 합니다.

    ```
    Get-MailboxSearch -InPlaceHoldIdentity <In-Place Hold GUID> | FL Name
    ```

2. 보존 기간을 변경 하려면 다음 명령을 실행 합니다. 이 예제에서는 대기 기간 2,555 일 (약 7 년)로 변경 됩니다. 
    
    ```
    Set-MailboxSearch <identity of In-Place Hold> -ItemHoldPeriod 2555
    ```

     보존 기간 제한 없음된 기간을 변경 하려면 _-ItemHoldPeriod 무제한으로_사용 합니다.
  
## <a name="more-information"></a>추가 정보

- **비활성 사서함에 있는 항목에 대 한 보존 기간 계산 방법?** 사서함 항목을 받거나 만든 원래 날짜에서 기간 계산 됩니다. 
    
- **보존 기간이 만료 될 때 수행 하는 작업?** 복구 가능한 항목 폴더에서 사서함 항목에 대 한 보존 기간 만료 되 면 해당 항목은 영구적으로 삭제 (비우기) 비활성 사서함에서. 비활성 사서함에 배치 보류에 대해 지정 된 기간이 있으면 복구 가능한 항목 폴더의 항목 (하지 않는 경우 비활성 사서함에 대 한 보존 기간 변경 된) 되지 비워집니다 수 있습니다. 
    
- **은 비활성 사서함에서 아직 처리 하는 Exchange 보존 정책?** (인, 보존 태그를 **삭제** 하는 보존 작업을 사용 하 여 구성) 삭제 정책 됩니다 (의 메시징 레코드 관리 또는 MRM, Exchange Online의 기능)는 Exchange 보존 정책 비활성 이었습니다 때 사서함에 적용 된, 하는 경우 비활성 사서함에서 처리를 계속 합니다. 즉, 보존 기간이 만료 될 때 삭제 정책을 사용 하 여 태그가 지정 된 항목을 복구 가능한 항목 폴더를 이동 됩니다. 이러한 항목 항목에 대 한 보존 기간이 만료 될 때 다음 비활성 사서함에서 비워집니다. 
    
    이와 반대로 비활성 사서함에 할당 된 보존 정책에 포함 된 모든 보관 정책 (인, **보관 폴더로 이동** 보존 작업을 사용 하 여 구성 하는 보존 태그)은 무시 됩니다. 즉, 보존 기간이 만료 되는 기본 사서함에 남아 있을 하는 보관 정책을 사용 하 여 태그가 지정 된 비활성 사서함의 항목입니다. 보관 사서함으로 또는 보관 사서함의 복구 가능한 항목 폴더를 이동 하지는 합니다. 사용자는 비활성 사서함에 로그인 할 수 없습니다 되므로 보관 정책을 처리를 데이터 센터 리소스를 사용할 필요가 없습니다. 
    
- **새 보존 기간을 확인 하려면 다음 명령 중 하나를 실행 합니다.** 첫번째 명령은 소송 보존으로 설정 합니다. 두번째 사용자 계정의 원본 위치 유지입니다. 

    ```
    Get-Mailbox -InactiveMailboxOnly -Identity <identity of inactive mailbox> | FL LitigationHoldDuration
    ```

    ```
    Get-MailboxSearch <identity of In-Place Hold> | FL ItemHoldPeriod
    ```

- **같은 일반 사서함의 관리 되는 폴더 도우미 (MFA)도 비활성 사서함 처리.** Exchange Online에서 7 일 마다 한번씩 약 MFA는이 사서함을 처리합니다. 비활성 사서함에 대 한 보존 기간을 변경한 후에 즉시 처리를 시작 하려면 비활성 사서함에 대 한 새 보존 기간의 **Start-managedfolderassistant** cmdlet을 사용할 수 있습니다. 다음 명령을 실행 합니다. 

    ```
    Start-ManagedFolderAssistant -InactiveMailbox <identity of inactive mailbox>
    ```
   
- **보류 많은 guid가 표시 되는 보류 중 일부만 비활성 사서함에 배치 되는 경우.** 비활성 사서함에 배치 되는 (소송 보존을 포함 하 고)를 제외한 모든 보류에 대 한 Guid를 표시 하려면 다음 명령을 실행할 수 있습니다. 
    
    ```
    Get-Mailbox -InactiveMailboxOnly -Identity <identity of inactive mailbox> | Select-Object -ExpandProperty InPlaceHolds
    ```
