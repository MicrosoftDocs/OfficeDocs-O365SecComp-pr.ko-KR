---
title: 정보 장벽 정책 편집
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
description: 정보 장벽에 대 한 정책을 편집 하거나 제거 하는 방법을 알아봅니다.
ms.openlocfilehash: c55ffac0984fe83fec1ef7b995d1589ea770bfef
ms.sourcegitcommit: a6f046f1529b0515f4f0e918a19ec83f4138b871
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/08/2019
ms.locfileid: "35587077"
---
# <a name="edit-or-remove-information-barrier-policies"></a>정보 장벽 정책 편집 또는 제거

[정보 장벽 정책을 정의한](information-barriers-policies.md)후에는 [문제 해결](information-barriers-troubleshooting.md) 또는 일반 유지 관리의 일환으로 이러한 정책 또는 사용자 세그먼트를 변경 해야 할 수 있습니다. 이 문서를 참조 하십시오.

## <a name="what-do-you-want-to-do"></a>무슨 작업을 하고 싶으십니까?

|동작은  |설명 |
|---------|---------|
|[사용자 계정 특성 편집](#edit-user-account-attributes)     |세그먼트를 정의 하는 데 사용할 수 있는 특성을 Azure Active Directory에 입력 합니다.<br/>사용자 계정 특성을 편집 해야 하는 세그먼트에 사용자가 포함 되어 있지 않거나, 사용자가 속한 세그먼트를 변경 하거나, 다른 특성을 사용 하 여 세그먼트를 정의할 수 있습니다.         |
|[세그먼트 편집](#edit-a-segment)     |세그먼트 정의 방법을 변경 하려면 세그먼트를 편집 합니다. <br/>예를 들어 처음에 *부서* 를 사용 하 여 세그먼트를 정의 했을 때, 이제 *MemberOf*와 같은 다른 특성을 사용 하려고 할 수 있습니다.         |
|[정책 편집](#edit-a-policy)     |정책 작동 방식을 변경 하려면 정보 장벽 정책 편집을 클릭 합니다.<br/>예를 들어 두 세그먼트 간의 통신을 차단 하는 대신 특정 세그먼트 간에만 통신을 수행 하도록 할지 결정할 수 있습니다.         |
|[정책을 비활성 상태로 설정](#set-a-policy-to-inactive-status)     |정책을 변경 하려는 경우 또는 정책을 적용 하지 않으려는 경우에는 정책을 비활성 상태로 설정 합니다.         |
|[정책 제거](#remove-a-policy)     |특정 정책이 더 이상 필요 하지 않은 경우 정보 장벽 정책을 제거 합니다.         |
|[정책 응용 프로그램 중지](#stop-a-policy-application)     |정보 장벽 정책을 적용 하는 프로세스를 중지 하려면이 작업을 수행 합니다.<br/>정책 응용 프로그램을 중지 하는 것은 즉각적이 아니며 사용자에 게 이미 적용 된 정책을 실행 취소 하지 않습니다.         |
|[정보 장벽에 대 한 정책 정의](information-barriers-policies.md)     |해당 정책이 아직 위치에 없는 경우 정보 장벽 정책을 정의 하 고, 특정 사용자 그룹 간의 통신을 제한 하거나 제한 해야 합니다.         |
|[정보 장벽 문제 해결](information-barriers-troubleshooting.md)     |정보 장벽에서 예기치 않은 문제가 발생 하는 경우이 문서를 참조 하세요.         |

> [!IMPORTANT]
> 이 문서에서 설명 하는 작업을 수행 하려면 다음 중 하 나와 같은 적절 한 역할을 할당 받아야 합니다.<br/>-Microsoft 365 Enterprise 전역 관리자<br/>-Office 365 전역 관리자<br/>-준수 관리자<br/>-IB 준수 관리 (새 역할입니다.)<p>정보 장벽에 대 한 필수 구성 요소에 대 한 자세한 내용은 [필수 구성 요소 (정보 장벽 정책)](information-barriers-policies.md#prerequisites)를 참조 하세요.<p>[Office 365 Security & 준수 센터 PowerShell에 연결](https://docs.microsoft.com/powershell/exchange/office-365-scc/connect-to-scc-powershell/connect-to-scc-powershell?view=exchange-ps)되어 있는지 확인 합니다.

## <a name="edit-user-account-attributes"></a>사용자 계정 특성 편집

다음 절차에 사용 하 여 사용자 조각화에 사용 되는 특성을 편집 합니다. 

예를 들어 부서 특성을 사용 하는 경우 현재 하나 이상의 사용자 계정에 부서에 대해 나열 된 값이 없는 경우 부서 정보를 포함 하도록 해당 사용자 계정을 편집 해야 합니다. 

사용자 계정 특성은 정보 장벽 정책을 할당할 수 있도록 세그먼트를 정의 하는 데 사용 됩니다.

1. 특성 값 및 할당 된 세그먼트와 같은 특정 사용자 계정에 대 한 세부 정보를 보려면 **InformationBarrierRecipientStatus** Cmdlet을 Identity 매개 변수와 함께 사용 합니다. 

    |구문과  |예제  |
    |---------|---------|
    |`Get-InformationBarrierRecipientStatus -Identity <value> -Identity2 <value>` <p>   이름, 별칭, 고유 이름, 정식 도메인 이름, 전자 메일 주소 또는 GUID와 같은 각 사용자를 고유 하 게 식별 하는 모든 값을 사용할 수 있습니다. <p>   (단일 사용자에 대해이 cmdlet을 사용할 수도 있습니다. `Get-InformationBarrierRecipientStatus -Identity <value>`)      |`Get-InformationBarrierRecipientStatus -Identity meganb -Identity2 alexw`  <p>   이 예에서는 Office 365의 두 사용자 계정 ( *Megan*용 *meganb* 및 *Alex*용 *alexw* )을 참조 합니다.         |

2. 사용자 계정 프로필에 대해 편집 하려는 특성을 결정 합니다. 자세한 [내용은 Attributes 장벽 정책의 특성](information-barriers-attributes.md) 을 참조 하세요. 

3. 이전 단계에서 선택한 특성에 대 한 값을 포함 하도록 하나 이상의 사용자 계정을 편집 합니다. 이렇게 하려면 다음 절차 중 하나를 사용 합니다.

    - 단일 계정을 편집 하려면 [Azure Active Directory를 사용 하 여 사용자 프로필 정보 추가 또는 업데이트](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-users-profile-azure-portal)를 참조 하세요.

    - 여러 계정을 편집 하거나 PowerShell을 사용 하 여 단일 계정을 편집 하려면 [Office 365 PowerShell을 사용 하 여 사용자 계정 속성 구성을](https://docs.microsoft.com/office365/enterprise/powershell/configure-user-account-properties-with-office-365-powershell)참조 하십시오.

## <a name="edit-a-segment"></a>세그먼트 편집

이 절차를 사용 하 여 사용자 세그먼트의 정의를 편집 합니다. 예를 들어 세그먼트 이름을 변경 하거나 세그먼트에 포함 된 사용자를 확인 하는 데 사용 되는 필터를 변경할 수 있습니다.

1. 모든 기존 세그먼트를 보려면 **OrganizationSegment** cmdlet을 사용 합니다.
    
    구문과`Get-OrganizationSegment`

    세그먼트 유형, UserGroupFilter 값, 해당 개체를 만들거나 마지막으로 수정한 사람, GUID 등의 각 세그먼트와 세부 정보에 대 한 목록이 표시 됩니다.

    > [!TIP]
    > 나중에 참조 하기 위해 세그먼트 목록을 인쇄 하거나 저장 합니다. 예를 들어 세그먼트를 편집 하려면 해당 이름을 확인 하거나 값을 식별 해야 합니다 (이는 Identity 매개 변수와 함께 사용 됨).

2. 세그먼트를 편집 하려면 **Identity** 매개 변수와 관련 세부 정보와 함께 **OrganizationSegment** cmdlet을 사용 합니다. 

    |구문과  |예제  |
    |---------|---------|
    |`Set-OrganizationSegment -Identity GUID -UserGroupFilter "attribute -eq 'attributevalue'"`     |`Set-OrganizationSegment -Identity c96e0837-c232-4a8a-841e-ef45787d8fcd -UserGroupFilter "Department -eq 'HRDept'"` <p>이 예에서는 GUID가 *c96e0837-c232-4a8a-841e-ef45787d8fcd*인 세그먼트에 대해 부서 이름을 "hrdept"로 업데이트 했습니다.         |

조직의 세그먼트 편집을 마친 후에는 정보 장벽 정책을 [정의](information-barriers-policies.md#part-2-define-information-barrier-policies) 하거나 [편집할](#edit-a-policy) 수 있습니다.

## <a name="edit-a-policy"></a>정책 편집

1. 현재 정보 장벽 정책 목록을 보려면 **InformationBarrierPolicy** cmdlet을 사용 합니다.

    구문과`Get-InformationBarrierPolicy`

    결과 목록에서 변경 하려는 정책을 식별 합니다. 정책의 GUID 및 이름을 적어둡니다.

2. **InformationBarrierPolicy** Cmdlet에서 **Identity** 매개 변수를 사용 하 여 변경할 내용을 지정 합니다.

    예: *연구* 세그먼트가 *영업* 및 *마케팅* 세그먼트와 통신 하지 못하도록 차단 하도록 정책이 정의 되어 있다고 가정 합니다. 이 cmdlet을 사용 하 여 정책이 정의 되었습니다.`New-InformationBarrierPolicy -Name "Research-SalesMarketing" -AssignedSegment "Research" -SegmentsBlocked "Sales","Marketing"`
    
    *리서치* 세그먼트의 사람들이 *HR* 세그먼트의 사용자와만 통신할 수 있도록이를 변경 하려는 경우를 가정해 보겠습니다. 이 변경 작업을 수행 하려면 다음 cmdlet을 사용 합니다.`Set-InformationBarrierPolicy -Identity 43c37853-ea10-4b90-a23d-ab8c93772471 -SegmentsAllowed "HR"`

    이 예에서는 "SegmentsBlocked"를 "SegmentsAllowed"로 변경 하 고 *HR* 세그먼트를 지정 했습니다.

3. 정책 편집을 마친 후에는 변경 내용을 적용 해야 합니다. ( [정보 장벽 정책 적용](information-barriers-policies.md#part-3-apply-information-barrier-policies)참조)

## <a name="set-a-policy-to-inactive-status"></a>정책을 비활성 상태로 설정

1. 현재 정보 장벽 정책 목록을 보려면 **InformationBarrierPolicy** cmdlet을 사용 합니다.

    구문과`Get-InformationBarrierPolicy`

    결과 목록에서 변경 하거나 제거할 정책을 식별 합니다. 정책의 GUID 및 이름을 적어둡니다.

2. 정책의 상태를 비활성으로 설정 하려면 Identity 매개 변수와 함께 **InformationBarrierPolicy** cmdlet을 사용 하 고 State 매개 변수는 비활성으로 설정 합니다.

    |구문과  |예제  |
    |---------|---------|
    |`Set-InformationBarrierPolicy -Identity GUID -State Inactive`     |`Set-InformationBarrierPolicy -Identity 43c37853-ea10-4b90-a23d-ab8c9377247 -State Inactive` <p>이 예에서는 GUID *43c37853-ea10-4b90-a23d-ab8c9377247을 사용* 하는 정보 장벽 정책을 비활성 상태로 설정 합니다.         |

3. 변경 내용을 적용 하려면 **InformationBarrierPoliciesApplication** cmdlet을 사용 합니다.

    구문과`Start-InformationBarrierPoliciesApplication`

    사용자가 조직에 대해 변경 내용을 적용 합니다. 대규모 조직에서는이 프로세스를 완료 하는 데 24 시간 이상 소요 될 수 있습니다. 일반적으로 5000 사용자 계정을 처리 하는 데 한 시간 정도 소요 됩니다.

이때 하나 이상의 정보 장벽 정책이 비활성 상태로 설정 됩니다. 여기서는 다음 작업을 수행할 수 있습니다.
- 그대로 유지 (비활성 상태로 설정 된 정책이 사용자에 게 영향을 주지 않음)
- [정책 편집](#edit-a-policy) 
- [정책 제거](#remove-a-policy)

## <a name="remove-a-policy"></a>정책 제거

1. 현재 정보 장벽 정책 목록을 보려면 **InformationBarrierPolicy** cmdlet을 사용 합니다.

    구문과`Get-InformationBarrierPolicy`

    결과 목록에서 제거할 정책을 식별 합니다. 정책의 GUID 및 이름을 적어둡니다. 정책이 비활성 상태로 설정 되어 있는지 확인 합니다.

2. **InformationBarrierPolicy** Cmdlet을 Identity 매개 변수와 함께 사용 합니다.

    |구문과  |예제  |
    |---------|---------|
    |`Remove-InformationBarrierPolicy -Identity GUID`     |`Remove-InformationBarrierPolicy -Identity 43c37853-ea10-4b90-a23d-ab8c93772471` <p>이 예에서는 GUID가 *43c37853-ea10-4b90-a23d-ab8c93772471*인 정책을 제거 합니다.          |

    메시지가 표시 되 면 변경 내용을 확인 합니다.

3. 제거할 각 정책에 대해 1-2 단계를 반복 합니다.

4. 정책을 제거한 후에는 변경 내용을 적용 합니다. 이 작업을 수행 하려면 **InformationBarrierPoliciesApplication** cmdlet을 사용 합니다.

    구문과`Start-InformationBarrierPoliciesApplication`

    사용자가 조직에 대해 변경 내용을 적용 합니다. 대규모 조직에서는이 프로세스를 완료 하는 데 24 시간 이상 소요 될 수 있습니다.

## <a name="stop-a-policy-application"></a>정책 응용 프로그램 중지

정보 장벽 정책 적용을 시작 하 고 나면 해당 정책을 적용 하지 않으려면 다음 절차를 사용 합니다. 프로세스를 시작 하는 데 약 30-35 분이 소요 됨을 염두에 두어야 합니다.

1. 가장 최근 정보 장벽 정책 응용 프로그램의 상태를 확인 하려면 **InformationBarrierPoliciesApplicationStatus** cmdlet을 사용 합니다.

    구문과`Get-InformationBarrierPoliciesApplicationStatus`

    응용 프로그램의 GUID를 확인 합니다.

2. **InformationBarrierPoliciesApplication** Cmdlet을 Identity 매개 변수와 함께 사용 합니다.

    |구문과  |예제  |
    |---------|---------|
    |`Stop-InformationBarrierPoliciesApplication -Identity GUID`     |`Stop-InformationBarrierPoliciesApplication -Identity 46237888-12ca-42e3-a541-3fcb7b5231d1` <p>이 예에서는 정보 장벽 정책이 적용 되지 않도록 중지 합니다.         |

## <a name="related-articles"></a>관련 문서

[정보 장벽에 대 한 개요 보기](information-barriers.md)

[정보 장벽에 대 한 정책 정의](information-barriers-policies.md)

[Microsoft 팀의 정보 장벽에 대해 자세히 알아보기](https://docs.microsoft.com/MicrosoftTeams/information-barriers-in-teams)

[정보 장벽 정책의 특성](information-barriers-attributes.md)

[정보 장벽 문제 해결](information-barriers-troubleshooting.md)
