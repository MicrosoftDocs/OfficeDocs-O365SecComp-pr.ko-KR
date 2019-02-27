---
title: Exchange Online 사서함의 보류 유형을 식별하는 방법
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 6/22/2018
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.collection: M365-security-compliance
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 6057daa8-6372-4e77-a636-7ea599a76128
description: Office 365 사서함에 저장할 수 있는 다양 한 유형의 보존을 식별 하는 방법에 대해 알아봅니다. 이러한 보류 유형에는 소송 보존, eDiscovery 보류 및 Office 365 보존 정책이 포함 됩니다. 사용자가 조직 차원의 보존 정책에서 제외 되었는지 여부도 확인할 수 있습니다.
ms.openlocfilehash: 5b9e8437b688a5c1b35726834c3d80d07cc4ba50
ms.sourcegitcommit: baf23be44f1ed5abbf84f140b5ffa64fce605478
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/26/2019
ms.locfileid: "30296811"
---
# <a name="how-to-identify-the-type-of-hold-placed-on-an-exchange-online-mailbox"></a>Exchange Online 사서함의 보류 유형을 식별하는 방법

이 문서에서는 Office 365에서 Exchange Online 사서함에 적용 되는 보류를 확인 하는 방법에 대해 설명 합니다.

Office 365에서는 조직에서 사서함 콘텐츠가 영구적으로 삭제 되지 않도록 하는 여러 가지 방법을 제공 합니다. 이를 통해 조직은 준수 regulars을 충족 하거나 법률 또는 기타 조사 유형에 따라 콘텐츠를 보존할 수 있습니다. 다음은 Office 365에서 보존 기능 ( *보류*라고도 함)의 목록입니다.

- **소송 보존** -Exchange Online의 사용자 사서함에 적용 되는 보존입니다.

- **ediscovery 보류** -보안 & 준수 센터에서 eDiscovery 사례와 관련 된 보류입니다. eDiscovery 보류는 사용자 사서함 및 해당 하는 Office 365 그룹 및 Microsoft 팀의 해당 사서함에 적용할 수 있습니다.

- 원본 **위치 유지** -exchange Online의 exchange 관리 센터에서 원본 위치 eDiscovery & 보존 도구를 사용 하 여 사용자 사서함에 적용 됩니다.

- **office 365 보존 정책** -Exchange Online의 사용자 사서함과 Office 365 그룹 및 Microsoft 팀의 해당 사서함에 있는 콘텐츠를 유지 합니다. 사용자 사서함에 저장 되는 비즈니스용 Skype 대화를 보관 하는 보존 정책을 만들 수 있습니다.

  사서함에 할당할 수 있는 Office 365 보존 정책에는 두 가지 유형이 있습니다.

    - **특정 위치 보존 정책** -특정 사용자의 콘텐츠 위치에 할당 되는 정책입니다. Exchange Online PowerShell의 **Get-Mailbox** cmdlet을 사용 하 여 특정 사서함에 할당 된 보존 정책에 대 한 정보를 가져옵니다.

    - **조직 전체 보존 정책** -조직의 모든 콘텐츠 위치에 할당 되는 정책입니다. Exchange Online PowerShell에서 **set-organizationconfig** cmdlet을 사용 하 여 조직 차원의 보존 정책에 대 한 정보를 가져옵니다. 자세한 내용은 [Overview the Office 365 보존 정책 개요](retention-policies.md#applying-a-retention-policy-to-an-entire-organization-or-specific-locations)의 "전체 조직이 나 특정 위치에 보존 정책 적용" 섹션을 참조 하십시오.

- **office 365 보존 레이블** -사용자가 Office 365 보존 레이블 (콘텐츠를 보존 하 고 유지 한 다음 콘텐츠를 보존 하 고 사서함의 항목에 저장 ** )을 적용 하는 경우 사서함이 있는 것 처럼 사서함에 보류가 설정 됩니다. 소송 보존 또는 Office 365 유지 정책에 할당 된 위치 자세한 내용은이 문서의 [폴더 또는 항목 섹션에 보존 레이블이 적용 되었기 때문에 보류 중인 사서함 확인](#identifying-mailboxes-on-hold-because-a-label-has-been-applied-to-a-folder-or-item) 을 참조 하십시오.

보류 중인 사서함을 관리 하려면 대기 시간 변경, 일시적으로 또는 영구 제거 또는 Office 365 보존 정책에서 사서함을 제외 하는 등의 작업을 수행할 수 있도록 사서함에 저장 된 보류 유형을 확인 해야 할 수 있습니다. 이러한 경우 첫 번째 단계는 사서함에 적용 된 보류 유형을 식별 하는 것입니다. 또한 단일 사서함에 여러 보류 (및 서로 다른 형식 보존)을 적용할 수 있으므로 사서함에 저장 된 모든 보류를 확인 하 여 해당 보류를 제거 하거나 변경 해야 합니다.

## <a name="step-1-obtaining-the-guid-for-holds-placed-on-a-mailbox"></a>1 단계: 사서함에 저장 된 보류의 GUID 가져오기

Exchange Online PowerShell에서 다음 두 cmdlet을 실행 하 여 사서함에 저장 된 보류의 GUID를 가져올 수 있습니다. GUID를 얻은 후에는이를 사용 하 여 2 단계에서 특정 보류를 식별 합니다. 소송 보존은 GUID로 식별 되지 않습니다. 소송 보존은 사서함에 대해 사용 하거나 사용 하지 않도록 설정 되어 있습니다.

- **Get-mailbox** -이 cmdlet을 사용 하 여 사서함에 대해 소송 보존을 사용 하도록 설정 했는지 여부를 확인 하 고, eDiscovery 보류에 대 한 guid, 원본 위치 유지 및 사서함에 특별히 할당 된 Office 365 보존 정책을 가져옵니다. 이 cmdlet의 출력은 사서함이 조직 차원의 보존 정책에서 명시적으로 제외 되었는지 여부도 나타냅니다.

- **set-organizationconfig** -이 cmdlet을 사용 하 여 조직 전체 보존 정책의 guid를 가져옵니다.

exchange online powershell에 연결 하려면 [exchange online powershell에 연결](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell?view=exchange-ps)을 참조 하세요.

### <a name="get-mailbox"></a>Get-Mailbox

다음 명령을 실행 하 여 사서함에 적용 된 보류 및 Office 365 보존 정책에 대 한 정보를 가져옵니다.

```
Get-Mailbox <username> | FL LitigationHoldEnabled,InPlaceHolds
```

> [!TIP]
> InPlaceHolds 속성에 값이 너무 많고 이러한 속성이 모두 표시 되는 것은 아닌 경우 `Get-Mailbox <username> | Select-Object -ExpandProperty InPlaceHolds` 명령을 실행 하 여 각 GUID를 별도의 줄에 표시할 수 있습니다.

다음 표에는 *InPlaceHolds* 속성의 값에 따라 **Get-Mailbox** cmdlet을 실행할 때의 서로 다른 유형의 보류를 식별 하는 방법에 대 한 설명이 나와 있습니다.


|보류 유형  |예제 값  |보류를 확인 하는 방법  |
|---------|---------|---------|
|소송 보존     |    `True`     |     *LitigationHoldEnabled* 속성이로 `True`설정 된 경우 사서함에 대해 소송 보존을 사용 하도록 설정 합니다.    |
|eDiscovery 보류     |  `UniH7d895d48-7e23-4a8d-8346-533c3beac15d`       |   *InPlaceHolds 속성* 은 보안 & 준수 센터에서 eDiscovery 사례와 관련 된 보류의 GUID를 포함 합니다. GUID는 `UniH` 접두사 (통합 보류 표시)로 시작 되므로 eDiscovery 보류 임을 알릴 수 있습니다.      |
|원본 위치 유지     |     `c0ba3ce811b6432a8751430937152491` <br/> 또는 <br/> `cld9c0a984ca74b457fbe4504bf7d3e00de`  |     *InPlaceHolds* 속성은 사서함에 배치 된 원본 위치 유지의 GUID를 포함 합니다. GUID가 접두사로 시작 하지 않거나 `cld` 접두사로 시작 하지 않으므로 원본 위치 유지로 설정할 수 있습니다.     |
|Office 365 보존 정책이 특별히 사서함에 적용 되었습니다.     |    `mbxcdbbb86ce60342489bff371876e7f224:1` <br/> 또는 <br/> `skp127d7cf1076947929bf136b7a2a8c36f:3`     |     InPlaceHolds 속성은 사서함에 적용 된 특정 위치 보존 정책의 guid를 포함 합니다. GUID는 `mbx` 또는 `skp` 접두사로 시작 되므로 보존 정책을 식별할 수 있습니다. 접두사 `skp` 는 보존 정책이 사용자 사서함의 비즈니스용 Skype 대화에 적용 됨을 나타냅니다.    |
|조직 전체 Office 365 보존 정책에서 제외 됨     |   `-mbxe9b52bf7ab3b46a286308ecb29624696`      |     사서함이 조직 차원의 Office 365 보존 정책에서 제외 된 경우에는 사서함이 제외 된 보존 정책의 GUID가 InPlaceHolds 속성에 표시 되 고 `-mbx` 접두사로 식별 됩니다.    |

### <a name="get-organizationconfig"></a>set-organizationconfig
**사서함** cmdlet을 실행할 때 *InPlaceHolds* 속성이 비어 있으면 여전히 사서함에 적용 되는 하나 이상의 조직 수준 Office 365 보존 정책이 있을 수 있습니다. Exchange Online PowerShell에서 다음 명령을 실행 하 여 조직 전반의 Office 365 보존 정책에 대 한 guid 목록을 가져옵니다.

```
Get-OrganizationConfig | FL InPlaceHolds
```

> [!TIP]
> InPlaceHolds 속성에 값이 너무 많고 이러한 속성이 모두 표시 되는 것은 아닌 경우 `Get-OrganizationConfig | Select-Object -ExpandProperty InPlaceHolds` 명령을 실행 하 여 각 GUID를 별도의 줄에 표시할 수 있습니다.

다음 표에서는 여러 유형의 조직 차원의 보류와 **set-organizationconfig** cmdlet을 실행할 때 *InPlaceHolds* 속성에 포함 된 guid에 따라 각 형식을 식별 하는 방법에 대해 설명 합니다.


|보류 유형  |예제 값  |설명  |
|---------|---------|---------|
|exchange 사서함, exchange 공용 폴더 및 팀 대화방에 적용 되는 Office 365 보존 정책    |      `mbx7cfb30345d454ac0a989ab3041051209:2`   |   exchange 사서함, exchange 공용 폴더 및 1xn 채팅에 적용 되는 조직 차원의 보존 정책은 `mbx` 접두사를 사용 하 여 시작 되는 guid로 식별 됩니다. 1xn 채팅은 개별 채팅 참가자의 사서함에 저장 됩니다.      |
|office 365 그룹 및 팀 채널 메시지에 적용 되는 office 365 보존 정책     |   `grp1a0a132ee8944501a4bb6a452ec31171:3`      |    Microsoft 팀의 Office 365 그룹 및 채널 메시지에 적용 되는 조직 차원의 보존 정책은 `grp` 접두사로 시작 되는 guid로 식별 됩니다. 채널 메시지는 Microsoft 팀과 연결 된 그룹 사서함에 저장 됩니다.     |

Microsoft 팀에 적용 되는 자세한 정보 보존 정책은 "팀 위치" 섹션의 [보존 정책 개요](retention-policies.md#applying-a-retention-policy-to-an-entire-organization-or-specific-locations)를 참조 하세요.

### <a name="understanding-the-format-of-the-inplaceholds-value-for-retention-policies"></a>보존 정책에 대 한 InPlaceHolds 값의 형식 이해

InPlaceHolds 속성의 항목을 Office 365 보존 정책으로 식별 하는 접두사 (m b x, p 또는 grp) 외에,이 값에는 정책에 대해 구성 된 보존 작업 유형을 식별 하는 접미사도 포함 됩니다. 예를 들어 다음 예제에서는 동작 접미사가 굵은 형식으로 강조 표시 됩니다.

   `skp127d7cf1076947929bf136b7a2a8c36f`**주파수**

   `mbx7cfb30345d454ac0a989ab3041051209`**: 2**

   `grp1a0a132ee8944501a4bb6a452ec31171`**: 3**

다음 표에서는 가능한 세 가지 보존 작업을 정의 합니다.

|값  |설명  |
|---------|---------|
|**개**     | 보존 정책이 항목을 삭제 하도록 구성 되어 있음을 나타냅니다. 정책은 항목을 보존 하지 않습니다.        |
|**2**    |    항목을 포함 하도록 보존 정책이 구성 되었음을 나타냅니다. 보존 기간이 만료 된 후에는 정책이 항목을 삭제 하지 않습니다.     |
|**3(sp3)**     |   보존 정책이 항목을 보관 하도록 구성 되어 있음을 나타내고 보존 기간이 만료 되 면 삭제 합니다.      |

보존 작업에 대 한 자세한 내용은 [보존 정책 개요](retention-policies.md#retaining-content-for-a-specific-period-of-time)의 "특정 기간 동안 콘텐츠 보존" 섹션을 참조 하십시오.
   
## <a name="step-2-using-the-guid-to-identify-the-hold"></a>2 단계: GUID를 사용 하 여 보류 식별

사서함에 적용 되는 보류에 대 한 guid를 얻은 후에는 해당 guid를 사용 하 여 보류를 식별 합니다. 다음 섹션에서는 보류 GUID를 사용 하 여 보류 (및 기타 정보)의 이름을 식별 하는 방법을 보여 줍니다.

### <a name="ediscovery-holds"></a>eDiscovery 보류

Security & 준수 센터 PowerShell에서 다음 명령을 실행 하 여 사서함에 적용 된 eDiscovery 보존을 식별 합니다. 1 단계에서 확인 한 eDiscovery 보존에 대 한 GUID (a * 접두사를 포함 하지 않음)를 사용 합니다. 첫 번째 명령은 보류에 대 한 정보가 포함 된 변수를 만듭니다. 이 변수는 다른 명령에 사용 됩니다. 두 번째 명령은 보류가 연결 된 eDiscovery 사례의 이름을 표시 합니다. 세 번째 명령은 보류의 이름과 보류가 적용 되는 사서함 목록을 표시 합니다.

```
$CaseHold = Get-CaseHoldPolicy <hold GUID without prefix>
```

```
Get-ComplianceCase $CaseHold.CaseId | FL Name
```

```
$CaseHold | FL Name,ExchangeLocation
```

보안 & 준수 센터 powershell에 연결 하려면 [connect to Office 365 Security & 준수 센터 powershell](https://docs.microsoft.com/powershell/exchange/office-365-scc/connect-to-scc-powershell/connect-to-scc-powershell?view=exchange-ps)를 참조 하세요.

### <a name="in-place-holds"></a>원본 위치 유지

Exchange Online PowerShell에서 다음 명령을 실행 하 여 사서함에 적용 된 원본 위치 유지를 식별 합니다. 1 단계에서 확인 한 원본 위치 유지에 대해 GUID를 사용 합니다. 이 명령은 보류의 이름과 보류가 적용 되는 사서함 목록을 표시 합니다.

```
Get-MailboxSearch -InPlaceHoldIdentity <hold GUID> | FL Name,SourceMailboxes
```
원본 위치 유지의 GUID가 `cld` 접두사로 시작 되는 경우에는 이전 명령을 실행할 때 접두사를 포함 해야 합니다.

### <a name="office-365-retention-policies"></a>Office 365 보존 정책

Security & 준수 센터 PowerShell에서 다음 명령을 실행 하 여 사서함에 적용 되는 Office 365 보존 정책 (조직 전체 또는 특정 위치)을 식별 합니다. 1 단계에서 확인 한 GUID (m b x,로 p, 또는 grp 접두사 또는 작업 접미사는 포함 하지 않음)를 사용 합니다.

```
Get-RetentionCompliancePolicy <hold GUID without prefix or suffix> -DistributionDetail  | FL Name,*Location
```

## <a name="identifying-mailboxes-on-hold-because-a-retention-label-has-been-applied-to-a-folder-or-item"></a>폴더 또는 항목에 보존 레이블이 적용 되었기 때문에 보류 중인 사서함 확인

사용자가 콘텐츠를 보존 하도록 구성 된 보존 레이블을 적용 하거나 사서함의 모든 폴더 또는 항목에 대 한 콘텐츠를 삭제 하는 경우에는 *ComplianceTagHoldApplied* mailbox 속성을 **True**로 설정 합니다. 이 문제가 발생 하는 경우 사서함은 소송 보존에 적용 된 것으로 간주 되거나 Office 365 보관 정책에 할당 되는 것 처럼 유지 됩니다. *ComplianceTagHoldApplied* 속성을 **True**로 설정 하면 다음 작업이 수행 될 수 있습니다.

- 사서함 이나 사용자의 Office 365 사용자 계정이 삭제 되 면 사서함이 [비활성 사서함](inactive-mailboxes-in-office-365.md)이 됩니다.
- 사서함 (기본 사서함 또는 보관 사서함이 사용 하도록 설정 된 경우)을 사용 하지 않도록 설정할 수 없습니다.
- 사서함의 항목이 예상 보다 오래 보존 될 수 있습니다. 이는 사서함이 보류 중 이므로 영구적으로 삭제 (제거) 되는 것 이기 때문입니다.

*ComplianceTagHoldApplied* 속성의 값을 확인 하려면 Exchange Online PowerShell에서 다음 명령을 실행 합니다.

```
Get-Mailbox <username> |FL ComplianceTagHoldApplied
```

보존 레이블에 대 한 자세한 내용은 Overview For [Office 365 보존 레이블](labels.md)를 참조 하세요.

## <a name="managing-mailboxes-on-delay-hold"></a>지연 보류 시 사서함 관리

사서함에서 모든 유형의 보류가 제거 된 후에는 *DelayHoldApplied* mailbox 속성의 값이 **True**로 설정 됩니다. 다음 번에 관리 되는 폴더 도우미가 사서함을 처리 하 고 보류가 제거 되었음을 감지할 때 이러한 상황이 발생 합니다. 이를 *지연 보존* 이라고 하며, 사서함에서 데이터를 영구적으로 삭제 (제거) 하지 못하도록 30 일 동안 실제로 보존을 제거 하는 작업이 지연 됨을 의미 합니다. 이를 통해 관리자는 보존을 실제로 제거한 후 제거 되는 사서함 항목을 검색 하거나 복구할 수 있습니다. 사서함에 연기 대기를 설정 하면 사서함이 소송 보존 상태에 있는 것 처럼 여전히 무제한 기간 동안 유지 되는 것으로 간주 됩니다. 30 일 후에 지연 보류가 만료 되 고 Office 365에서 자동으로 지연 대기 ( *DelayHoldApplied* 속성을 **False**로 설정)을 제거 하 여 보류를 실제로 제거 하려고 합니다. *DelayHoldApplied* 속성을 False로 **설정**하면 다음에 관리 되는 폴더 도우미가 사서함을 처리할 때 제거 하도록 표시 된 항목이 제거 됩니다.

사서함에 대 한 *DelayHoldApplied* 속성의 값을 확인 하려면 Exchange Online PowerShell에서 다음 명령을 실행 합니다.

```
Get-Mailbox <username> | FL DelayHoldApplied
```

만료 되기 전에 지연 보존을 제거 하려면 Exchange Online PowerShell에서 다음 명령을 실행 하면 됩니다. 
 
```
Set-Mailbox <username> -RemoveDelayHoldApplied
```
*RemoveDelayHoldApplied* 매개 변수를 사용 하려면 Exchange Online의 법적 보존 역할을 할당 받아야 합니다. 

비활성 사서함에 대 한 지연 대기를 제거 하려면 Exchange Online PowerShell에서 다음 명령을 실행 합니다.

```
Set-Mailbox <DN or Exchange GUID> -InactiveMailbox -RemoveDelayHoldApplied
```

> [!TIP]
> 이전 명령에서 비활성 사서함을 지정 하는 가장 좋은 방법은 해당 고유 이름이 나 Exchange GUID 값을 사용 하는 것입니다. 이러한 값 중 하나를 사용 하면 실수로 잘못 된 사서함을 지정 하는 것을 방지할 수 있습니다. 

## <a name="next-steps"></a>다음 단계

사서함에 적용 되는 보류를 확인 한 후 보류 시간을 변경 하거나 보류를 일시적으로 또는 영구적으로 제거 하거나 정책에서 비활성 사서함을 제외 하 고 Office 365 보존 정책의 경우에는 작업을 수행할 수 있습니다. 보류와 관련 된 작업을 수행 하는 방법에 대 한 자세한 내용은 다음 항목 중 하나를 참조 하십시오.

- Security & 준수 센터 PowerShell에서 [ \<new-retentioncompliancepolicy-addexchangelocationexception user mailbox>](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-retention/Set-RetentionCompliancePolicy?view=exchange-ps) 명령을 실행 하 여 조직 차원의 Office 365 보존 정책에서 사서함을 제외 합니다. 이 명령은 *ExchangeLocation* 속성 값이 같은 `All`보존 정책에만 사용할 수 있습니다.

- Exchange Online PowerShell에서 [접두사 또는 suffix> \<명령 없이 ExcludeFromOrgHolds 보류 GUID](https://docs.microsoft.com/powershell/module/exchange/mailboxes/set-mailbox?view=exchange-ps) 를 실행 하 여 조직 차원의 Office 365 보존 정책에서 비활성 사서함을 제외 합니다.

- [Office 365에서 비활성 사서함에 대 한 보존 기간 변경](change-the-hold-duration-for-an-inactive-mailbox.md)

- [Office 365에서 비활성 사서함 삭제](delete-an-inactive-mailbox.md)

- [보류 중인 클라우드 기반 사서함의 복구 가능한 항목 폴더에서 항목 삭제](delete-items-in-the-recoverable-items-folder-of-mailboxes-on-hold.md)
