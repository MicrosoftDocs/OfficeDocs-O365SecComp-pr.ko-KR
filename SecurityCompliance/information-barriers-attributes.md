---
title: 정보 장벽 정책의 특성
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 07/08/2019
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.collection:
- M365-security-compliance
localization_priority: None
description: 이 문서를 정보 장벽 정책에서 사용할 수 있는 다양 한 특성에 대 한 참조로 사용 합니다.
ms.openlocfilehash: 1e2e183da350308a57fa5d627b4867b9b3d30cee
ms.sourcegitcommit: a6f046f1529b0515f4f0e918a19ec83f4138b871
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/08/2019
ms.locfileid: "35587067"
---
# <a name="attributes-for-information-barrier-policies"></a>정보 장벽 정책의 특성

Azure Active Directory의 특정 특성을 사용 하 여 사용자를 분할할 수 있습니다. 세그먼트를 정의한 후에는 이러한 세그먼트를 정보 장벽 정책의 필터로 사용할 수 있습니다. 예를 들어 **부서** 를 사용 하 여 조직 내 부서별로 사용자 세그먼트를 정의할 수 있습니다 (두 부서가 동시에 단일 직원이 작동 하지 않는다고 가정). 

이 문서에서는 정보 장벽에서 특성을 사용 하는 방법에 대해 설명 하 고 사용할 수 있는 특성 목록을 제공 합니다. 정보 장벽에 대 한 자세한 내용은 다음 리소스를 참조 하십시오.
- [정보 장벽](information-barriers.md)
- [Microsoft 팀의 정보 장벽에 대 한 정책 정의](information-barriers-policies.md)
- [정보 장벽 정책 편집 또는 제거](information-barriers-edit-segments-policies.md.md)

## <a name="how-to-use-attributes-in-information-barrier-policies"></a>정보 장벽 정책에서 특성을 사용 하는 방법

이 문서에 나와 있는 특성을 사용 하 여 사용자의 세그먼트를 정의 하거나 편집할 수 있습니다. 정의 된 세그먼트는 [정보 장벽 정책](information-barriers-policies.md)에서 매개 변수 ( *usergroupfilter* 값 이라고 함)로 사용 됩니다.

1. 세그먼트를 정의 하는 데 사용할 특성을 결정 합니다. (이 문서의 [참조](#reference) 섹션 참조)

2. 사용자 계정에 1 단계에서 선택한 특성에 대 한 값이 입력 되어 있는지 확인 합니다. 사용자 계정 정보를 확인 하 고 필요한 경우 특성 값을 포함 하도록 사용자 계정을 편집 합니다. 

    - 여러 계정을 편집 하거나 PowerShell을 사용 하 여 단일 계정을 편집 하려면 [Office 365 PowerShell을 사용 하 여 사용자 계정 속성 구성을](https://docs.microsoft.com/office365/enterprise/powershell/configure-user-account-properties-with-office-365-powershell)참조 하십시오.

    - 단일 계정을 편집 하려면 [Azure Active Directory를 사용 하 여 사용자 프로필 정보 추가 또는 업데이트](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-users-profile-azure-portal)를 참조 하세요.

3. 다음 예와 같이 [PowerShell을 사용 하 여 세그먼트를 정의](information-barriers-policies.md#define-segments-using-powershell)합니다.

    |예제  |#A0  |
    |---------|---------|
    |부서 특성을 사용 하 여 Segment1 라는 세그먼트를 정의 합니다.     | `New-OrganizationSegment -Name "Segment1" -UserGroupFilter "Department -eq 'Department1'"`        |
    |MemberOf 특성을 사용 하 여 SegmentA 이라는 세그먼트를 정의 합니다 (이 특성에 그룹 이름 (예: "BlueGroup")이 포함 되어 있다고 가정).     | `New-OrganizationSegment -Name "SegmentA" -UserGroupFilter "MemberOf -eq 'BlueGroup'"`        |
    |ExtensionAttribute1을 사용 하 여 DayTraders 라는 세그먼트를 정의 합니다 (이 특성에 직함 (예: "Daytraders")이 포함 되어 있다고 가정 합니다.)|`New-OrganizationSegment -Name "DayTraders" -UserGroupFilter "ExtensionAttribute1 -eq 'DayTrader'"` |

    > [!TIP]
    > 세그먼트를 정의할 때 모든 세그먼트에 같은 특성을 사용 합니다. 예를 들어 *부서*를 사용 하 여 일부 세그먼트를 정의 하는 경우에는 *부서*를 사용 하 여 모든 세그먼트를 정의 합니다. *부서* 및 다른 사용자는 *MemberOf*를 사용 하 여 일부 세그먼트를 정의 하지 마세요. 세그먼트가 겹치지 않는지 확인 합니다. 각 사용자는 정확히 하나의 세그먼트에 할당 되어야 합니다. 

## <a name="reference"></a>참조

다음 표에는 정보 장벽에 사용할 수 있는 특성이 나와 있습니다.

|Azure Active Directory 속성 이름<br/>(LDAP 표시 이름)  |Exchange 속성 이름  |
|---------|---------|
|Co       | Co        |
|Company     |Company         |
|부서     |부서         |
|ExtensionAttribute1 |CustomAttribute1  |
|ExtensionAttribute2 |CustomAttribute2  |
|ExtensionAttribute3 |CustomAttribute3  |
|ExtensionAttribute4 |CustomAttribute4  |
|ExtensionAttribute5 |CustomAttribute5  |
|ExtensionAttribute6 |CustomAttribute6  |
|ExtensionAttribute7 |CustomAttribute7  |
|ExtensionAttribute8 |CustomAttribute8  |
|ExtensionAttribute9 |CustomAttribute9  |
|ExtensionAttribute10 |CustomAttribute10  |
|ExtensionAttribute11 |CustomAttribute11  |
|ExtensionAttribute12 |CustomAttribute12  |
|ExtensionAttribute13 |CustomAttribute13  |
|ExtensionAttribute14 |CustomAttribute14  |
|ExtensionAttribute15 |CustomAttribute15  |
|MSExchExtensionCustomAttribute1 |ExtensionCustomAttribute1 |
|MSExchExtensionCustomAttribute2 |ExtensionCustomAttribute2 |
|MSExchExtensionCustomAttribute3 |ExtensionCustomAttribute3 |
|MSExchExtensionCustomAttribute4 |ExtensionCustomAttribute4 |
|MSExchExtensionCustomAttribute5 |ExtensionCustomAttribute5 |
|MailNickname |별칭 |
|PhysicalDeliveryOfficeName |Office |
|PostalCode |PostalCode |
|ProxyAddresses |EmailAddresses |
|StreetAddress |StreetAddress |
|TargetAddress |ExternalEmailAddress |
|UsageLocation |UsageLocation |
|UserPrincipalName  |UserPrincipalName  |
|메일로   |WindowsEmailAddress    |
|설명    |설명    |
|소속   |MemberOfGroup  |

## <a name="related-topics"></a>관련 항목

[Microsoft 팀의 정보 장벽에 대 한 정책 정의](information-barriers-policies.md)

[정보 장벽 문제 해결](information-barriers-troubleshooting.md)

[정보 장벽](information-barriers.md)



