---
title: Exchange Online 사서함의 보류 유형을 식별하는 방법
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 6/22/2018
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 6057daa8-6372-4e77-a636-7ea599a76128
description: 다양 한 유형의 Office 365 사서함에 배치할 수 있는 보류를 식별 하는 방법에 알아봅니다. 이러한 유형의 보류 소송 보존으로 설정, eDiscovery 보류 및 Office 365 보존 정책에 포함 됩니다. 사용자는 조직 전체의 보존 정책에서 제외 되었는지 하는 경우 확인할 수 있습니다.
ms.openlocfilehash: 375bd86df370fe34fbe59f6581836da7e9d06515
ms.sourcegitcommit: 82fd4c85b952819157fbb13175c7b2dbbdff510f
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/13/2018
ms.locfileid: "23965265"
---
# <a name="how-to-identify-the-type-of-hold-placed-on-an-exchange-online-mailbox"></a>Exchange Online 사서함의 보류 유형을 식별하는 방법

이 문서에서는 Office 365의 Exchange Online 사서함에 배치 하는 보류를 식별 하는 방법에 설명 합니다.

Office 365에는 다양 한 조직에서 영구적으로 삭제 되 고 사서함 콘텐츠를 방지할 수 있는 방법 제공 합니다. 이렇게 하면 준수 사람은 충족 하기 위해 콘텐츠를 유지 하려면 조직 또는 법률 또는 기타 유형의 조사의 기간에 대 한 합니다. Office 365의 (도 호출 *을 포함 하 고*) 보존 기능 목록은 다음과 같습니다.

- **소송 보존으로 설정** -Exchange Online에서 사용자 사서함에 적용 되는 보류 합니다.

- **eDiscovery 보류** -보안 및 규정 준수 센터의 eDiscovery 사례와 연결 된 보류 합니다. eDiscovery 보류 Office 365 그룹 및 Microsoft 팀의 사용자 사서함 및 해당 사서함에 적용할 수 있습니다.

- **원본 위치 유지** -Exchange 관리자의 원본 위치 eDiscovery & 유지 도구를 사용 하 여 사용자 사서함에 적용 되는 보류를 가운데에 Exchange Online.

- **Office 365 보존 정책** -Office 365 그룹 및 팀이 Microsoft Exchange Online 및 해당 사서함에서 사용자 사서함의 콘텐츠를 유지 합니다. 보존을 만들 수 정책 사용자 사서함에 저장 되는 비즈니스 대화에 대 한 Skype를 유지 합니다.

  사서함에 할당 될 수 있는 Office 365 보존 정책에는 다음과 같은 두가지 유형이 있습니다.

    - **특정 위치 보존 정책** -이것은 특정 사용자의 콘텐츠 위치에 할당 된 정책입니다. Exchange Online PowerShell에서 **Get-mailbox** cmdlet를 사용 하 여 특정 사서함에 할당 된 보존 정책에 대 한 정보를 얻을 수 있습니다.

    - **조직 전체의 보존 정책** -이것은 조직에서 모든 콘텐츠 위치에 할당 된 정책입니다. Exchange Online PowerShell에서 **Get-organizationconfig** cmdlet를 사용 하 여 조직 전체의 보존 정책에 대 한 정보를 얻을 수 있습니다. 자세한 내용은 [Office 365 개요 (영문) 보존 정책](retention-policies.md#applying-a-retention-policy-to-an-entire-organization-or-specific-locations)에서 "전체 조직 또는 특정 위치에 보존 정책 적용" 섹션을 참조 하십시오.

- **Office 365 레이블** -사용자를 *모든* 폴더 또는 항목 보류 자신의 사서함에는 Office 365 레이블 (콘텐츠 또는 유지 하 고 다음 콘텐츠를 삭제 하도록 구성 된 하나)를 적용 하는 경우이 경우 사서함 소송 보존에 배치 된 대로 사서함에 놓입니다. 대기 또는 Office 365 보존 정책에 할당 합니다. 자세한 내용은이 문서의 [식별 사서함에 보관 폴더 또는 항목 레이블을 적용 된 때문에](#identifying-mailboxes-on-hold-because-a-label-has-been-applied-to-a-folder-or-item) 섹션을 참조 하십시오.

보류에 있는 사서함을 관리 하려면 보류에 보존 기간을 변경, 일시적 또는 영구적으로 제거 보류를 또는 사서함을 제외 하 고 Office 365 보존 정책에서 등의 작업을 수행할 수 있도록 사서함에 배치 되는 형식을 식별 해야할 수 있습니다. 이러한 경우 첫 단계는 사서함에 배치 하는 보류의 형식을 식별 하기 위해입니다. 및 여러 보류 (및 다양 한 유형의 보류) 단일 사서함에 배치할 수, 하기 때문에 해야 하거나 제거 하거나 해당 보류를 변경 하려는 경우 사서함에 배치 하는 모든 보류를 식별 합니다.

## <a name="step-1-obtaining-the-guid-for-holds-placed-on-a-mailbox"></a>1 단계: 사서함에 배치 보류에 대 한 GUID 가져오기

사서함에 배치 되는 보류의 GUID를 가져올 Exchange Online PowerShell에서 다음 두 cmdlet을 실행할 수 있습니다. GUID를 확인 한 후 2 단계에서에서 특정 보류를 식별 하는데 사용 합니다. GUID로 소송 보존을 포함 하 고는 식별 되지를 메모 합니다. 소송 보존 사용 하거나 사서함을 사용할 수 없게 됩니다.

- **Get-mailbox** -사용 하 여 사서함에 대 한 소송 보존을 사용할지 여부를 확인 하 고 eDiscovery에 대 한 Guid를 가져오려면이 cmdlet을 포함 하 고, 원본 위치 유지 및 구체적으로 사서함에 할당 된 Office 365 보존 정책입니다. 또한 조직 전체의 보존 정책에서 사서함 명시적으로 제외 되었는지 하는 경우이 cmdlet의 출력을 알려줍니다.

- **Get-organizationconfig** -조직 전체의 보존 정책에 대 한 Guid를 가져올이 cmdlet 사용 합니다.

Exchange Online PowerShell 연결할 [Connect to Exchange Online PowerShell를](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell?view=exchange-ps)참조 하십시오.

### <a name="get-mailbox"></a>Get-Mailbox

보류 및 사서함에 적용 하는 Office 365 보존 정책에 대 한 정보를 가져오려면 다음 명령을 실행 합니다.

```
Get-Mailbox <username> | FL LitigationHoldEnabled,InPlaceHolds
```

> [!TIP]
> 실행할 수 InPlaceHolds 속성에 너무 많은 값이 모두 하지 표시 하는 경우는 `Get-Mailbox <username> | Select-Object -ExpandProperty InPlaceHolds` 별도 줄에 각 GUID를 표시 하는 명령입니다.

다음 표에서 다양 한 유형의 **Get-mailbox** cmdlet을 실행 하는 경우 *InPlaceHolds* 속성의 값에 따라 보류를 식별 하는 방법을 설명 합니다.


|종류를 유지 합니다.  |예제 값  |보류를 식별 하는 방법  |
|---------|---------|---------|
|소송 보존     |    `True`     |     *LitigationHoldEnabled* 속성이로 설정 된 경우 사서함에 대 한 소송 보존 상태가 `True`합니다.    |
|eDiscovery 보류     |  `UniH7d895d48-7e23-4a8d-8346-533c3beac15d`       |   *InPlaceHolds 속성* 은 보안 및 규정 준수 센터에서 eDiscovery 사례와 관련 된 모든 보류의 GUID를 포함 합니다. 이런 현상이 발생 eDiscovery 보류도 시작 하는 GUID를 알 수는 `UniH` 접두사 (하는 통합 유지 나타냅니다).      |
|원본 위치 유지     |     `c0ba3ce811b6432a8751430937152491` <br/> 또는 <br/> `cld9c0a984ca74b457fbe4504bf7d3e00de`  |     *InPlaceHolds* 속성의 사서함에 배치 되는 원본 위치 유지의 GUID를 포함 합니다. 이런 현상이 발생 한 원본 위치 유지 하거나 GUID를 접두사로 시작 되지 않으면 또는로 시작 하는 것을 알 수는 `cld` 접두사입니다.     |
|구체적으로 사서함에 적용 되는 office 365 보존 정책     |    `mbxcdbbb86ce60342489bff371876e7f224:1` <br/> 또는 <br/> `skp127d7cf1076947929bf136b7a2a8c36f:3`     |     InPlaceHolds 속성에는 사서함에 적용 되는 모든 특정 위치 보존 정책의 guid가 포함 됩니다. 으로 시작 하는 GUID 때문에 보존 정책을 식별할 수는 `mbx` 또는 `skp` 접두사입니다. `skp` 접두사는 사용자의 사서함에서 비즈니스 대화에 대 한의 보존 정책 Skype 적용 되었음을 나타냅니다.    |
|조직 전체의 Office 365 보존 정책에서 제외     |   `-mbxe9b52bf7ab3b46a286308ecb29624696`      |     사서함은 조직 전체의 Office 365 보존 정책에서 제외 하 고, 사서함에서 제외 보존 정책에 대 한 GUID InPlaceHolds 속성에 표시 되 고으로 식별 되는 `-mbx` 접두사입니다.    |

### <a name="get-organizationconfig"></a>Get-organizationconfig
**Get-mailbox** cmdlet을 실행 하는 경우 *InPlaceHolds* 속성이 비어 있는 경우 발생할 수 있습니다 하나 이상의 조직 전체의 Office 365 보존 정책 사서함에 적용 합니다. 다음 명령을 실행 Exchange Online 조직 전체의 Office 365 보존 정책에 대 한 Guid의 목록을 표시 하려면 PowerShell 합니다.

```
Get-OrganizationConfig | FL InPlaceHolds
```

> [!TIP]
> 실행할 수 InPlaceHolds 속성에 너무 많은 값이 모두 하지 표시 하는 경우는 `Get-OrganizationConfig | Select-Object -ExpandProperty InPlaceHolds` 별도 줄에 각 GUID를 표시 하는 명령입니다.

다음 표에서 다양 한 유형의 조직 전체의 보류 및 **Get-organizationconfig** cmdlet을 실행 하는 경우 *InPlaceHolds* 속성에 포함 된 Guid에 따라 각 유형을 식별 하는 방법을 설명 합니다.


|종류를 유지 합니다.  |예제 값  |설명  |
|---------|---------|---------|
|채팅을 통해 Exchange 사서함, Exchange 공용 폴더 및 팀에 office 365 보존 정책 적용    |      `mbx7cfb30345d454ac0a989ab3041051209:2`   |   Exchange 사서함을 Exchange 공용 폴더에 적용 된 조직 전체의 보존 정책 및 Microsoft 팀의 1xN 채팅으로 시작 하는 Guid로 식별 됩니다는 `mbx` 접두사입니다. Note 1xN 채팅은 개별 채팅 참가자의 사서함에 저장 됩니다.      |
|Office 365 그룹 및 팀에 해당 하는 채널의 메시지에 적용 되는 office 365 보존 정책     |   `grp1a0a132ee8944501a4bb6a452ec31171:3`      |    Office 365 그룹과 팀이 Microsoft에서 채널 메시지에 적용 된 조직 전체의 보존 정책으로 시작 하는 Guid로 식별 됩니다는 `grp` 접두사입니다. Note는 채널 메시지 Microsoft 팀과 연결 된 그룹 사서함에 저장 됩니다.     |

자세한 내용은 보존 정책 Microsoft 팀에 적용 된 [보존 정책 개요](retention-policies.md#applying-a-retention-policy-to-an-entire-organization-or-specific-locations)"팀 위치" 섹션을 참조 하십시오.

### <a name="understanding-the-format-of-the-inplaceholds-value-for-retention-policies"></a>보존 정책에 대 한 InPlaceHolds 값의 형식을 이해 (영문)

접두사 (mbx, skp, 또는 그룹)는 Office 365 보존 정책으로 InPlaceHolds 속성에서 항목을 식별 하는, 외에도 값도 정책에 대해 구성 된 보존 작업 유형을 식별 하는 접미사를 포함 합니다. 예, 작업 접미사는 다음 예제에서 굵은 글꼴로 강조 표시 됩니다.

   `skp127d7cf1076947929bf136b7a2a8c36f`**: 1**

   `mbx7cfb30345d454ac0a989ab3041051209`**: 2**

   `grp1a0a132ee8944501a4bb6a452ec31171`**: 3**

다음 표에서 세 가능한 보존 작업을 정의합니다.

|값  |설명  |
|---------|---------|
|**1**     | 보존 정책 항목을 삭제 하도록 구성 된를 나타냅니다. 정책 항목을 유지 하지 않습니다.        |
|**2**    |    보존 정책 항목을 유지 하도록 구성 된를 나타냅니다. 보존 기간이 만료 후 정책 항목을 삭제 하지 않습니다.     |
|**3**     |   보존 정책 항목을 유지 하 고 다음 보존 기간이 만료 후 삭제 하도록 구성 된를 나타냅니다.      |

보존 작업에 대 한 자세한 내용은 [보존 정책의 개요 (영문)](retention-policies.md#retaining-content-for-a-specific-period-of-time)의 "특정 기간에 대 한 콘텐츠 유지" 섹션을 참조 하십시오.
   
## <a name="step-2-using-the-guid-to-identify-the-hold"></a>2 단계: 보류를 식별 하는 GUID를 사용 하 여

사서함에 적용 되는 보류에 대 한 GUID를 가져오려면 후 보류를 식별 하는 GUID를 사용 하 여 다음 단계가입니다. 다음 섹션에서는 보류 GUID를 사용 하 여 보류 (및 기타 정보)의 이름을 식별 하는 방법을 보여줍니다.

### <a name="ediscovery-holds"></a>eDiscovery 보류

사서함에 적용 되는 eDiscovery 보류를 식별 하는 보안 및 규정 준수 센터 PowerShell에서 다음 명령을 실행 합니다. (UniH 접두사) 포함 하지 GUID를 사용 하 여 eDiscovery에 대 한 1 단계에서에서 확인 된를 보관 합니다. 첫번째 명령은 보류; 하는 방법에 대 한 정보가 포함 된 변수를 만듭니다. 이 변수는 다른 명령에서 사용 됩니다. 두번째 명령은 eDiscovery 대/소문자와 연결 된 보류의 이름을 표시 합니다. 세번째 명령은 보류를 적용 하는 사서함의 목록과 보류의 이름을 표시 합니다.

```
$CaseHold = Get-CaseHoldPolicy <hold GUID without prefix>
```

```
Get-ComplianceCase $CaseHold.CaseId | FL Name
```

```
$CaseHold | FL Name,ExchangeLocation
```

보안 및 규정 준수 센터 PowerShell에 연결할 [하 고 Office 365 보안 및 규정 준수 센터 PowerShell 연결](https://docs.microsoft.com/powershell/exchange/office-365-scc/connect-to-scc-powershell/connect-to-scc-powershell?view=exchange-ps)을 참조 하십시오.

### <a name="in-place-holds"></a>원본 위치 유지

사서함에 적용 되는 원본 위치 유지를 식별 하는 Exchange Online PowerShell에서 다음 명령을 실행 합니다. 1 단계에서에서 식별 된 원본 위치 유지 하는 GUID를 사용 합니다. 명령은 보류를 적용 하는 사서함의 목록과 보류의 이름을 표시 합니다.

```
Get-MailboxSearch -InPlaceHoldIdentity <hold GUID> | FL Name,SourceMailboxes
```
경우에는 GUID로 시작 하는 원본 위치 유지에 대 한 참고는 `cld` 접두사, 이전 명령을 실행할 때 접두사를 포함 해야 합니다.

### <a name="office-365-retention-policies"></a>Office 365 보존 정책

다음 명령을 실행에서 보안 및 규정 준수 센터 PowerShell id에는 사서함에 적용 되는 Office 365 보존 정책 (조직 차원의 또는 특정 위치). 1 단계에서에서 식별 하는 GUID (포함 안 mbx, skp, 또는 그룹 접두사 또는 작업 접미사)을 사용 합니다.

```
Get-RetentionCompliancePolicy <hold GUID without prefix or suffix> -DistributionDetail  | FL Name,*Location
```

## <a name="identifying-mailboxes-on-hold-because-a-label-has-been-applied-to-a-folder-or-item"></a>폴더 또는 항목 레이블을 적용 된 때문에 식별 사서함에 유지

다음은 콘텐츠를 보존 또는 유지 하 고 다음 콘텐츠를 모든 폴더 또는 사서함의 항목을 삭제 하도록 구성 된 레이블을 적용 하는 사용자, 때마다 *ComplianceTagHoldApplied* 사서함 속성을 **True**로 설정 됩니다. 이러한 상황이 발생 하는 경우에 사서함 수, 기다리는 경우 처럼 소송 보존에 배치 또는 Office 365 보존 정책에 할당 된 것으로 간주 됩니다. *ComplianceTagHoldApplied* 속성은 **True**로 설정 하는 경우에 다음과 같은 작업 발생할 수 있습니다.

- 사서함 또는 사용자의 Office 365 사용자 계정이 삭제 되 면 경우 사서함을 [비활성 사서함](inactive-mailboxes-in-office-365.md)이 됩니다.
- 사서함 (주 사서함 또는 보관 사서함에 설정 된 경우)를 사용 하지 않도록 설정할 수 없습니다.
- 사서함의 항목은 예상 보다 오래 유지 될 수 있습니다. 이런 현상이 발생 사서함 보류에 있고 따라서 항목이 없는 영구적으로 삭제 됩니다 (비우기).

*ComplianceTagHoldApplied* 속성의 값을 보려면 Exchange Online PowerShell에서 다음 명령을 실행 합니다.

```
Get-Mailbox <username> |FL ComplianceTagHoldApplied
```

레이블에 대 한 자세한 내용은 [Office 365 개요 레이블](labels.md)을 참조 하십시오.

## <a name="managing-mailboxes-on-delay-hold"></a>지연 관리 사서함 보류

모든 유형의 대기 사서함에서 제거 되 면 후 *DelayHoldApplied* 사서함 속성의 값을 **True**로 설정 됩니다. *지연 유지* 라고 하 고 영구적으로 삭제 되 고에서 데이터를 방지 하기 위해 30 일 동안 보류의 실제 제거 배달이 지연 된 것을 의미이 사서함에서 (비우기). 이렇게 admins를 검색 하거나 경과한 후 보존이 제거 실제로 사서함 항목을 복구 합니다. 지연 보류의 사서함에 배치 되 면 때 사서함은 여전히 사서함에 소송 보존으로 설정 된 하는 경우으로 대기는 무제한 기간에 대 한 것으로 간주 됩니다. 30 일 후 지연 보류 만료 되 면 및 Office 365 됩니다 ( *DelayHoldApplied* 속성을 **False**로 설정) 하 여 지연 보류를 제거 하려고 자동으로 보류를 실제로 제거할 수 있도록 합니다. *DelayHoldApplied* 속성을 **False**로 후 제거를 위해 표시 된 항목을 사서함 관리 되는 폴더 도우미에 의해 처리 되는 다음에 제거 됩니다.

사서함에 대 한 *DelayHoldApplied* 속성에 대 한 값을 보려면 Exchange Online PowerShell에서 다음 명령을 실행 합니다.

```
Get-Mailbox <username> | FL DelayHoldApplied
```

만료 되기 전에 지연 보류를 제거 하려면 Exchange Online PowerShell에서 다음 명령을 실행 수 있습니다. 
 
```
Set-Mailbox <username> -RemoveDelayHoldApplied
```
할당 되어야 합니다 법적 보존 역할 Exchange 온라인 *RemoveDelayHoldApplied* 매개 변수를 사용 하 여 note 

비활성 사서함에서 지연 보류를 제거 하려면 Exchange Online PowerShell에서 다음 명령을 실행 합니다.

```
Set-Mailbox <DN or Exchange GUID> -InactiveMailbox -RemoveDelayHoldApplied
```

> [!TIP]
> 이전 명령에서 비활성 사서함을 지정 하는 가장 좋은 방법은 고유 이름 또는 Exchange GUID 값을 사용 하는 것입니다. 이러한 값 중 하나를 사용 하 여 실수로 잘못 된 사서함을 지정 방지할 수 있습니다. 

## <a name="next-steps"></a>다음 단계

사서함에 적용 되는 보류를 파악 한 후 비활성 사서함 정책에서 제외 하 고 작업 예: 일시적으로 보류를 기간을 변경 또는 보류를 영구적으로 제거 또는 Office 365 보존 정책의 경우 수행할 수 있습니다. 보류와 관련 된 작업을 수행 하는 방법에 대 한 자세한 내용은 다음 항목 중 하나를 참조 하십시오.

- 실행 하는 [집합 RetentionCompliancePolicy AddExchangeLocationException \<사용자 사서함 >](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-retention/Set-RetentionCompliancePolicy?view=exchange-ps) 보안 및 규정 준수 센터 PowerShell 조직 전체의 Office 365 보존 정책에서 사서함을 제외 하도록 명령 합니다. 이 명령을 사용할 수 있도록만 보존 정책에 대 한 *ExchangeLocation* 속성에 대 한 값과 일치 하는 여기서 참고 `All`합니다.

- 실행 하는 [Set-mailbox ExcludeFromOrgHolds \<접두사 또는 접미사 하지 않고 GUID를 보유할 >](https://docs.microsoft.com/powershell/module/exchange/mailboxes/set-mailbox?view=exchange-ps) 는 조직 전체의 Office 365 보존 정책에서 비활성 사서함을 제외 하는 Exchange Online PowerShell에서 명령 합니다.

- [Office 365에서 비활성 사서함에 대 한 보존 기간 변경](change-the-hold-duration-for-an-inactive-mailbox.md)

- [Office 365에서 비활성 사서함 삭제](delete-an-inactive-mailbox.md)

- [보류 중인 클라우드 기반 사서함의 복구 가능한 항목 폴더에서 항목 삭제](delete-items-in-the-recoverable-items-folder-of-mailboxes-on-hold.md)
