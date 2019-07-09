---
title: 정보 장벽 정책 정의
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
description: Microsoft 팀에서 정보 장벽에 대 한 정책을 정의 하는 방법에 대해 알아봅니다.
ms.openlocfilehash: 527f059eb0bccb97429c649d055496c06710c2a9
ms.sourcegitcommit: a6f046f1529b0515f4f0e918a19ec83f4138b871
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/08/2019
ms.locfileid: "35587087"
---
# <a name="define-policies-for-information-barriers"></a>정보 장벽에 대 한 정책 정의

## <a name="overview"></a>개요

정보 장애물을 사용 하 여 특정 사용자 세그먼트가 서로 통신 하지 못하도록 설계 된 정책을 정의 하거나 특정 세그먼트가 다른 특정 세그먼트와만 통신할 수 있습니다. 정보 장벽 정책은 조직에서 관련 업계 표준 및 규정 준수를 유지 하 고, 잠재적으로 발생할 수 있는 충돌을 방지 하는 데 도움이 됩니다. 자세한 내용은 [정보 장벽](information-barriers.md)를 참조 하십시오. 

이 문서에서는 정보 장벽 정책을 계획, 정의, 구현 및 관리 하는 방법에 대해 설명 합니다. 여러 단계를 수행 하 고 작업 흐름을 여러 부분으로 분할 합니다. 정보 장벽 정책 정의 또는 편집을 시작 하기 전에 [필수 구성 요소](#prerequisites) 및 전체 프로세스를 확인 해야 합니다.

> [!TIP]
> 이 문서에는 정보 장벽 정책을 계획 하 고 정의 하는 데 도움이 되는 [예제 시나리오](#example-contosos-departments-segments-and-policies) 및 [다운로드 가능한 Excel 통합 문서가](https://github.com/MicrosoftDocs/OfficeDocs-O365SecComp/raw/public/SecurityCompliance/media/InfoBarriers-PowerShellGenerator.xlsx) 포함 되어 있습니다.

## <a name="concepts-of-information-barrier-policies"></a>정보 장벽 정책의 개념

정보 장벽에 대 한 정책을 정의 하는 경우에는 사용자 계정 특성, 세그먼트, "차단" 및/또는 정책 응용 프로그램을 사용 하 여 작업 합니다.

- **사용자 계정 특성** 은 Azure Active Directory (또는 Exchange Online)에서 정의 됩니다. 이러한 특성에는 부서, 직함, 위치, 팀 이름 및 기타 작업 프로필 정보가 포함 될 수 있습니다. 

- **세그먼트** 는 선택한 **사용자 계정 특성**을 사용 하 여 Office 365 보안 & 준수 센터에 정의 된 사용자 집합입니다. ( [지원 되는 특성 목록](information-barriers-attributes.md)참조) 

- **정보 장벽 정책** 에 따라 통신 제한 또는 제한이 결정 됩니다. 정보 장벽 정책을 정의할 때는 두 가지 정책 유형 중에서 선택 합니다.
    - "차단" 정책은 한 세그먼트가 다른 세그먼트와 통신 하지 못하도록 합니다.
    - "허용" 정책은 한 세그먼트가 다른 특정 세그먼트와도 통신할 수 있도록 허용 합니다.

- **정책 응용 프로그램** 은 모든 정보 장벽 정책이 정의 된 후에 수행 되며, 조직에 적용할 준비가 된 것입니다.

## <a name="the-work-flow-at-a-glance"></a>작업 흐름 살펴보기

|단계    |관련 기능  |
|---------|---------|
|[필수 구성 요소를 충족 하는지 확인](#prerequisites)     |- [필요한 라이선스 및 사용 권한이](information-barriers.md#required-licenses-and-permissions) 있는지 확인<br/>-디렉터리에 조각화 된 사용자에 대 한 데이터가 포함 되어 있는지 확인<br/>-Microsoft 팀에 대해 범위 디렉터리 검색 사용<br/>-감사 로깅이 설정 되어 있는지 확인<br/>-Exchange 주소록 정책이 현재 위치에 없는지 확인<br/>-PowerShell 사용 (예제가 제공 됨)<br/>-Microsoft 팀에 관리자 동의를 제공 합니다 (단계 포함).          |
|[1 부: 조직의 사용자 분류](#part-1-segment-users)     |-필요한 정책을 결정 합니다.<br/>-정의할 세그먼트 목록을 만듭니다.<br/>-사용할 특성 식별<br/>-정책 필터 용어로 세그먼트를 정의 합니다.        |
|[2 부: 정보 장벽 정책 정의](#part-2-define-information-barrier-policies)     |-정책 정의 (아직 적용 되지 않음)<br/>-두 종류 (차단 또는 허용)를 선택 합니다. |
|[3 부: 정보 장벽 정책 적용](#part-3-apply-information-barrier-policies)     |-정책을 활성 상태로 설정<br/>-정책 응용 프로그램 실행<br/>-정책 상태 보기         |
|(필요한 경우) [세그먼트 또는 정책 편집](information-barriers-edit-segments-policies.md.md)    |-세그먼트 편집<br/>-정책 편집 또는 제거<br/>-정책 응용 프로그램 다시 실행<br/>-정책 상태 보기         |
|(필요한 경우) [문제 해결](information-barriers-troubleshooting.md)|-항목이 정상적으로 작동 하지 않을 때 작업 수행|

## <a name="prerequisites"></a>필수 구성 요소

[필요한 라이선스 및 사용 권한](information-barriers.md#required-licenses-and-permissions)외에도 다음과 같은 요구 사항을 충족 하는지 확인 합니다. 
     
- **디렉터리 데이터** 조직의 구조가 디렉터리 데이터에 반영 되는지 확인 합니다. 이렇게 하려면 그룹 구성원 자격, 부서 이름 등의 사용자 계정 특성이 Azure Active Directory 또는 Exchange Online에서 올바르게 채워졌는지 확인 합니다. 자세한 내용은 다음 리소스를 참조 하십시오.
  - [정보 장벽 정책의 특성](information-barriers-attributes.md)
  - [Azure Active Directory를 사용 하 여 사용자 프로필 정보 추가 또는 업데이트](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-users-profile-azure-portal)
  - [Office 365 PowerShell를 사용 하 여 사용자 계정 속성 구성](https://docs.microsoft.com/office365/enterprise/powershell/configure-user-account-properties-with-office-365-powershell)

- **범위 디렉터리 검색** 조직의 첫 번째 정보 장벽 정책을 정의 하기 전에 [Microsoft 팀에서 범위 지정 디렉터리 검색을 사용 하도록 설정](https://docs.microsoft.com/MicrosoftTeams/teams-scoped-directory-search)해야 합니다. 정보 장벽 정책을 설정 하거나 정의 하기 전에 범위 디렉터리 검색을 사용 하도록 설정한 후 24 시간 이상 기다립니다.

- **감사 로깅** 정책 응용 프로그램의 상태를 조회 하려면 감사 로깅이 설정 되어 있어야 합니다. 세그먼트 또는 정책 정의를 시작 하기 전에이 작업을 수행 하는 것이 좋습니다. 자세한 내용은 [Turn Office 365 감사 로그 검색 설정 또는 해제](turn-audit-log-search-on-or-off.md)를 참조 하세요.

- 주소록 **정책 없음** 정보 장벽 정책을 정의 하 고 적용 하기 전에 Exchange 주소록 정책이 없는지 확인 합니다. 정보 장애물은 주소록 정책에 따라 다르지만 두 가지 종류의 정책은 서로 호환 되지 않습니다. 이러한 정책이 있는 경우 먼저 주소록 [정책을 제거](https://docs.microsoft.com/exchange/address-books/address-book-policies/remove-an-address-book-policy) 해야 합니다.

- **PowerShell**입니다. 현재 정보 장벽 정책은 PowerShell cmdlet을 사용 하 여 Office 365 보안 & 준수 센터에서 정의 되 고 관리 됩니다. 이 문서에서는 몇 가지 예를 제공 했지만 PowerShell cmdlet 및 매개 변수에 익숙해져야 합니다. AzureRM 모듈도 필요 합니다.
    - [Office 365 보안 및 준수 센터 PowerShell에 연결](https://docs.microsoft.com/powershell/exchange/office-365-scc/connect-to-scc-powershell/connect-to-scc-powershell?view=exchange-ps)
    - [Azure PowerShell 모듈 설치](https://docs.microsoft.com/powershell/azure/install-az-ps?view=azps-2.3.2)

- **Microsoft 팀의 정보 장벽에 대 한 관리자 동의** 정책이 적용 되 면 정보 장애물은에는 없는 채팅 세션에서 사용자를 제거할 수 있습니다. 이렇게 하면 조직이 정책 및 규정 준수 상태를 유지할 수 있습니다. 다음 절차를 사용 하 여 정보 장벽 정책이 Microsoft 팀에서 예상 대로 작동 하도록 설정 합니다. 

   1. 다음 PowerShell cmdlet을 실행 합니다.

      ```
      Login-AzureRmAccount 
      $appId="bcf62038-e005-436d-b970-2a472f8c1982" 
      $sp=Get-AzureRmADServicePrincipal -ServicePrincipalName $appId
      if ($sp -eq $null) { New-AzureRmADServicePrincipal -ApplicationId $appId }
      Start-Process  "https://login.microsoftonline.com/common/adminconsent?client_id=$appId"
      ```

   2. 메시지가 나타나면 Office 365에 대 한 회사 또는 학교 계정을 사용 하 여 로그인 합니다.

   3. 요청 된 **사용 권한** 대화 상자에서 정보를 검토 하 고 **수락**을 선택 합니다.

모든 필수 구성 요소가 충족 되 면 다음 섹션으로 이동 합니다.

> [!TIP]
> 계획을 준비 하는 데 도움이 되도록이 문서에 예제 시나리오가 포함 되어 있습니다. [Contoso의 부서, 세그먼트 및 정책을 참조 하세요](#example-contosos-departments-segments-and-policies).<p>또한 다운로드 가능한 Excel 통합 문서를 사용 하 여 세그먼트와 정책을 계획 하 고 정의 하 고 PowerShell cmdlet을 만들 수 있습니다. [통합 문서를 가져옵니다](https://github.com/MicrosoftDocs/OfficeDocs-O365SecComp/raw/public/SecurityCompliance/media/InfoBarriers-PowerShellGenerator.xlsx). 

## <a name="part-1-segment-users"></a>1 부: 사용자 분할

이 단계에서는 필요한 정보 장벽 정책이 무엇 인지 결정 하 고, 정의할 세그먼트 목록을 만든 다음, 세그먼트를 정의 합니다.

### <a name="determine-what-policies-are-needed"></a>필요한 정책 결정

정보 장벽 정책이 필요한 조직 내의 그룹 인 법률 및 업계 규정을 고려 하 고 계십니까? 목록을 만듭니다. 다른 그룹과 통신을 차단 해야 하는 그룹이 있습니까? 하나 또는 두 개의 다른 그룹과만 통신 하도록 허용 해야 하는 그룹이 있습니까? 다음은 두 그룹 중 하나에 속하는 것으로 필요한 정책을 고려 합니다.
- "차단" 정책은 한 그룹이 다른 그룹과 통신 하지 못하도록 합니다.
- "허용" 정책을 사용 하면 그룹이 다른 특정 그룹과 통신할 수 있습니다.

초기 그룹 및 정책 목록이 있으면 필요한 세그먼트를 확인 하기 위해 계속 진행 합니다. 

### <a name="identify-segments"></a>세그먼트 식별

초기 정책 목록 외에, 조직의 세그먼트 목록을 만듭니다. 정보 장벽 정책에 포함 될 사용자는 세그먼트에 속해야 하며, 사용자는 둘 이상의 세그먼트에 속해야 합니다. 각 세그먼트에는 하나의 정보 장벽 정책만 적용 될 수 있습니다. 

세그먼트를 정의 하는 데 사용할 조직의 디렉터리 데이터 특성을 결정 합니다. *부서*, *MemberOf*또는 지원 되는 특성을 사용할 수 있습니다. 사용자에 대해 선택한 특성에 값이 있는지 확인 합니다. [정보 장벽에 대해 지원 되는 특성 목록을 참조 하세요](information-barriers-attributes.md).

> [!IMPORTANT]
> **다음 섹션을 진행 하기 전에 디렉터리 데이터에 세그먼트를 정의 하는 데 사용할 수 있는 특성 값이 있는지 확인**합니다. 사용할 특성 값이 디렉터리 데이터에 없는 경우에는 정보 장애물을 계속 하기 전에 해당 정보를 포함 하도록 사용자 계정을 업데이트 해야 합니다. 이에 대 한 도움말을 보려면 다음 리소스를 참조 하세요.<br/>- [Office 365 PowerShell을 사용 하 여 사용자 계정 속성 구성](https://docs.microsoft.com/office365/enterprise/powershell/configure-user-account-properties-with-office-365-powershell)<br/>- [Azure Active Directory를 사용 하 여 사용자 프로필 정보 추가 또는 업데이트](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-users-profile-azure-portal)

### <a name="define-segments-using-powershell"></a>PowerShell을 사용 하 여 세그먼트 정의

세그먼트를 정의 해도 사용자에 게 영향을 주지 않습니다. 정보 장벽 정책을 정의 하 고 적용 하기 위한 단계를 설정 하기만 하면 됩니다.

1. 사용 하려는 [특성](information-barriers-attributes.md) 에 해당 하는 **usergroupfilter** 매개 변수와 함께 **OrganizationSegment** cmdlet을 사용 합니다.

    |구문과   |예제  |
    |---------|---------|
    |`New-OrganizationSegment -Name "segmentname" -UserGroupFilter "attribute -eq 'attributevalue'"`     |`New-OrganizationSegment -Name "HR" -UserGroupFilter "Department -eq 'HR'"` <p>이 예제에서는 hr을 사용 하 ** 여 인사부 라는 세그먼트 ** 를 정의 하 고 *부서* 특성에 값을 지정 합니다. Cmdlet의 **-eq** 부분은 "equals"를 참조 합니다. 또는 **-ne** 를 사용 하 여 "같지 않음"을 계산할 수도 있습니다. [세그먼트 정의에서 "같음" 및 "같지 않음" 사용](#using-equals-and-not-equals-in-segment-definitions)을 참조 하십시오.        |

    각 cmdlet을 실행 하면 새 세그먼트에 대 한 세부 정보 목록이 표시 됩니다. 세부 정보에는 세그먼트의 유형, 작성자가 작성 하거나 마지막으로 수정한 사람 등이 포함 됩니다. 

2. 정의 하려는 각 세그먼트에 대해이 프로세스를 반복 합니다.

    > [!IMPORTANT]
    > **세그먼트가 겹치지 않는지 확인**합니다. 정보 장벽에 영향을 받게 되는 각 사용자는 하나의 세그먼트에만 속해야 합니다. 두 개 이상의 세그먼트에 속해야 하는 사용자가 없습니다. (예제:이 문서에 나와 있는 [Contoso의 정의 된 세그먼트](#contosos-defined-segments) 참조)


세그먼트를 정의한 후에는 [정보 장벽 정책 정의](#part-2-define-information-barrier-policies)로 이동 합니다.

### <a name="using-equals-and-not-equals-in-segment-definitions"></a>세그먼트 정의에서 "같음" 및 "같지 않음" 사용

다음 예제에서는 "부서가 HR과 같음"을 나타내는 세그먼트를 정의 합니다. 

|예제  |
|---------|
|`New-OrganizationSegment -Name "HR" -UserGroupFilter "Department -eq 'HR'"` <p>이 예제에서 세그먼트 정의에는 **-eq**로 표시 되는 "equals" 매개 변수가 포함 되어 있습니다. 
  |

다음 표에 나와 있는 것 처럼 "같지 않음" 매개 변수를 사용 하 **** 여 세그먼트를 정의할 수도 있습니다.

|구문과  |예제  |
|---------|---------|
|`New-OrganizationSegment -Name "segmentname" -UserGroupFilter "attribute -ne 'attributevalue'"`    |`New-OrganizationSegment -Name "NotSales" -UserGroupFilter "Department -ne 'Sales'"` <p>이 예에서는 *sales*에 없는 모든 사용자를 포함 하는 *notsales* 라는 세그먼트를 정의 했습니다. Cmdlet의 **-ne** 부분은 "같지 않음"을 참조 합니다.  |

"같음" 또는 "같지 않음"을 사용 하 여 세그먼트를 정의 하는 것 외에도 "같음" 및 "같지 않음" 매개 변수를 모두 사용 하 여 세그먼트를 정의할 수 있습니다.

|예제  |
|---------|
|`New-OrganizationSegment -Name "LocalFTE" -UserGroupFilter "Location -eq 'Local'" and "Position -ne 'Temporary'"` <p>이 예에서는 로컬로 위치 하 고 위치가 *임시*로 나열 되지 않은 사용자를 포함 하는 *LocalFTE* 라는 세그먼트를 정의 했습니다.    |

> [!TIP]
> 가능한 경우 "-eq" 또는 "-ne"를 포함 하는 세그먼트 정의를 사용 합니다. 복잡 한 세그먼트 정의를 정의 하지 마십시오. 

## <a name="part-2-define-information-barrier-policies"></a>2 부: 정보 장벽 정책 정의

특정 세그먼트 간 통신을 방지 해야 하는지 또는 특정 세그먼트에 대 한 통신을 제한할지 여부를 결정 합니다. 조직에서 법적 및 업계 요구 사항을 준수 하는 데 필요한 최소 정책 수를 사용 하는 것이 이상적입니다.

사용자 세그먼트 목록과 정의할 정보 장벽 정책을 사용 하 여 시나리오를 선택한 다음 단계를 수행 합니다. 

- [시나리오 1: 세그먼트 간 통신 차단](#scenario-1-block-communications-between-segments)
- [시나리오 2: 특정 세그먼트가 다른 세그먼트와만 통신할 수 있도록 허용](#scenario-2-allow-a-segment-to-communicate-only-with-one-other-segment)

> [!IMPORTANT]
> **정책을 정의할 때 세그먼트에 두 개 이상의 정책을 할당 하지**않도록 해야 합니다. 예를 들어 *sales*라는 세그먼트에 대해 하나의 정책을 정의 하는 경우에는 *sales*에 대 한 추가 정책을 정의 하지 마십시오.<p>또한 정보 장벽 정책을 정의 하는 동안 이러한 정책을 적용할 준비가 될 때까지 해당 정책이 비활성 상태로 설정 되었는지 확인 합니다. 정책 정의 (또는 편집)는 해당 정책이 활성 상태로 설정 된 후에 야 사용자에 게 영향을 줍니다.

(이 문서의 [예: Contoso의 정보 장벽 정책](#contosos-information-barrier-policies) 참조)

### <a name="scenario-1-block-communications-between-segments"></a>시나리오 1: 세그먼트 간 통신 차단

세그먼트 간의 통신을 차단 하려는 경우 각 방향에 하나씩 두 개의 정책을 정의 합니다. 각 정책은 통신을 단방향 으로만 차단 합니다.

예를 들어 세그먼트 A와 세그먼트 B 간의 통신을 차단 하려는 경우를 가정해 보겠습니다. 이 경우 세그먼트 A가 세그먼트 B와 통신 하는 것을 방지 하는 정책을 하나 정의한 다음, 두 번째 정책을 정의 하 여 세그먼트 B가 세그먼트 A와 통신 하는 것을 방지 합니다.

1. 첫 번째 차단 정책을 정의 하려면 **InformationBarrierPolicy** Cmdlet에 **SegmentsBlocked** 매개 변수를 사용 합니다. 

    |구문과  |예제  |
    |---------|---------|
    |`New-InformationBarrierPolicy -Name "policyname" -AssignedSegment "segment1name" -SegmentsBlocked "segment2name"`     |`New-InformationBarrierPolicy -Name "Sales-Research" -AssignedSegment "Sales" -SegmentsBlocked "Research" -State Inactive` <p>    이 예에서는 *sales*라는 세그먼트에 대 한 *영업 조사* 라는 정책을 정의 했습니다. 이 정책을 사용 하면 *영업* 직원이 *조사*라는 세그먼트에 있는 사람들과 통신할 수 없습니다.         |

2. 두 번째 차단 세그먼트를 정의 하려면 **SegmentsBlocked** 매개 변수와 함께 **InformationBarrierPolicy** cmdlet을 사용 하 여 세그먼트를 거꾸로 된 상태로 다시 지정 합니다.

    |예제  |
    |---------|
    |`New-InformationBarrierPolicy -Name "Research-Sales" -AssignedSegment "Research" -SegmentsBlocked "Sales" -State Inactive` <p>    이 예에서는 *연구가* *영업*과의 통신을 방지 하기 위해 *research-Sales* 라는 정책을 정의 했습니다.     |

2. 다음 중 하나로 이동 합니다.

   - (필요한 경우) [다른 세그먼트 하나로만 통신할 수 있도록 정책 정의](#scenario-2-allow-a-segment-to-communicate-only-with-one-other-segment) 
   - (모든 정책이 정의 된 후) [정보 장벽 정책 적용](#part-3-apply-information-barrier-policies)

### <a name="scenario-2-allow-a-segment-to-communicate-only-with-one-other-segment"></a>시나리오 2: 특정 세그먼트가 다른 세그먼트와만 통신할 수 있도록 허용

1. 하나의 세그먼트가 다른 하나의 세그먼트와만 통신할 수 있도록 하려면 **SegmentsAllowed** 매개 변수와 함께 **InformationBarrierPolicy** cmdlet을 사용 합니다. 

    |구문과  |예제  |
    |---------|---------|
    |`New-InformationBarrierPolicy -Name "policyname" -AssignedSegment "segment1name" -SegmentsAllowed "segment2name"`     |`New-InformationBarrierPolicy -Name "Manufacturing-HR" -AssignedSegment "Manufacturing" -SegmentsAllowed "HR" -State Inactive` <p>    이 예에서는 *manufacturing*이라는 세그먼트에 대해 *제조-HR* 이라는 정책을 정의 했습니다. 이 정책을 사용 하면 *제조* 중인 사용자가 *HR*이라는 세그먼트에 있는 사용자와만 통신할 수 있습니다. (이 경우, *Manufacturing* 은 *HR*에 속하지 않는 사용자와 통신할 수 없습니다.)         |

    **필요한 경우 다음 예와 같이이 cmdlet을 사용 하 여 여러 세그먼트를 지정할 수 있습니다.**

    |구문과  |예제  |
    |---------|---------|
    |`New-InformationBarrierPolicy -Name "policyname" -AssignedSegment "segment1name" -SegmentsAllowed "segment2name", "segment3name"`     |`New-InformationBarrierPolicy -Name "Research-HRManufacturing" -AssignedSegment "Research" -SegmentsAllowed "HR","Manufacturing" -State Inactive` <p>이 예에서는 *조사* 세그먼트가 *HR* 및 *제조*와만 통신할 수 있도록 하는 정책을 정의 했습니다.        |

    특정 세그먼트가 다른 특정 세그먼트와만 통신할 수 있도록 정의 하려는 각 정책에 대해이 단계를 반복 합니다.

2. 다음 중 하나로 이동 합니다.

   - (필요한 경우) [세그먼트 간 통신을 차단 하는 정책 정의](#scenario-1-block-communications-between-segments) 
   - (모든 정책이 정의 된 후) [정보 장벽 정책 적용](#part-3-apply-information-barrier-policies)

## <a name="part-3-apply-information-barrier-policies"></a>3 부: 정보 장벽 정책 적용

정보 장벽 정책은 활성 상태로 설정 하 고 정책을 적용할 때까지 적용 되지 않습니다.

1. **InformationBarrierPolicy** cmdlet을 사용 하 여 정의 된 정책 목록을 볼 수 있습니다. 각 정책의 상태 및 id (GUID)를 적어둡니다.

    구문과`Get-InformationBarrierPolicy`

2. 정책을 활성 상태로 설정 하려면 **Identity** 매개 변수와 함께 **InformationBarrierPolicy** cmdlet을 사용 하 고 **State** 매개 변수를 **active**로 설정 합니다. 

    |구문과  |예제  |
    |---------|---------|
    |`Set-InformationBarrierPolicy -Identity GUID -State Active`     |`Set-InformationBarrierPolicy -Identity 43c37853-ea10-4b90-a23d-ab8c93772471 -State Active` <p>    이 예에서는 GUID가 *43c37853-ea10-4b90-a23d-ab8c93772471* 인 정보 장벽 정책을 active status로 설정 합니다.   |

    각 정책에 대해 적절 하 게이 단계를 반복 합니다.

3. 정보 장벽 정책 설정이 활성 상태로 끝나면 Office 365 보안 & 준수 센터의 **InformationBarrierPoliciesApplication** cmdlet을 사용 합니다.

    구문과`Start-InformationBarrierPoliciesApplication`

    약 1 시간 후에는 조직에 대해 사용자에 게 정책이 적용 됩니다. 대규모 조직에서는이 프로세스를 완료 하는 데 24 시간 이상 소요 될 수 있습니다. 일반적으로 5000 사용자 계정을 처리 하는 데 한 시간 정도 소요 됩니다.

## <a name="view-status-of-user-accounts-segments-policies-or-policy-application"></a>사용자 계정, 세그먼트, 정책 또는 정책 응용 프로그램의 상태 보기

PowerShell을 사용 하 여 다음 표에 나와 있는 것 처럼 사용자 계정, 세그먼트, 정책 및 정책 응용 프로그램의 상태를 볼 수 있습니다.

|이를 보려면  |수행 작업  |
|---------|---------|
|사용자 계정     |Identity 매개 변수와 함께 **InformationBarrierRecipientStatus** cmdlet을 사용 합니다. <p>구문과`Get-InformationBarrierRecipientStatus -Identity <value> -Identity2 <value>` <p>이름, 별칭, 고유 이름, 정식 도메인 이름, 전자 메일 주소 또는 GUID와 같은 각 사용자를 고유 하 게 식별 하는 모든 값을 사용할 수 있습니다. <p>예제: `Get-InformationBarrierRecipientStatus -Identity meganb -Identity2 alexw` <p>이 예에서는 Office 365의 두 사용자 계정 ( *Megan*용 *meganb* 및 *Alex*용 *alexw* )을 참조 합니다. <p>(단일 사용자에 대해이 cmdlet을 사용할 수도 있습니다. `Get-InformationBarrierRecipientStatus -Identity <value>`) <p>이 cmdlet은 특성 값 및 적용 되는 정보 장벽 정책과 같은 사용자에 대 한 정보를 반환 합니다.|
|세그먼트     |**OrganizationSegment** cmdlet을 사용 합니다.<p>구문과`Get-OrganizationSegment` <p>이렇게 하면 조직에 대해 정의 된 모든 세그먼트의 목록이 표시 됩니다.         |
|정보 장벽 정책     |**InformationBarrierPolicy** cmdlet을 사용 합니다. <p> 구문과`Get-InformationBarrierPolicy` <p>이렇게 하면 정의 된 정보 장벽 정책 목록과 해당 상태가 표시 됩니다.       |
|가장 최근 정보 장벽 정책 응용 프로그램     | **InformationBarrierPoliciesApplicationStatus** cmdlet을 사용 합니다. <p>구문과`Get-InformationBarrierPoliciesApplicationStatus`<p>    이렇게 하면 정책 응용 프로그램이 완료, 실패 또는 진행 중인지에 대 한 정보가 표시 됩니다.       |
|모든 정보 장벽 정책 응용 프로그램|하십시오`Get-InformationBarrierPoliciesApplicationStatus -All $true`<p>이렇게 하면 정책 응용 프로그램이 완료, 실패 또는 진행 중인지에 대 한 정보가 표시 됩니다.|

## <a name="what-if-i-need-to-remove-or-change-policies"></a>정책을 제거 하거나 변경 해야 하는 경우

정보 장벽 정책을 관리 하는 데 도움이 되는 리소스를 제공 합니다.

- 정보 장벽에 문제가 있는 경우 [정보 장벽 문제 해결](information-barriers-troubleshooting.md)을 참조 하세요.

- 정책이 적용 되지 않도록 하려면 [정책 응용 프로그램 중지](information-barriers-edit-segments-policies.md.md#stop-a-policy-application)를 참조 하세요.

- 정보 장벽 정책을 제거 하려면 [정책 제거](information-barriers-edit-segments-policies.md.md#remove-a-policy)를 참조 하십시오.

- 세그먼트 또는 정책을 변경 하려면 [정보 장벽 정책 편집 (또는 제거)](information-barriers-edit-segments-policies.md.md)을 참조 하십시오.

## <a name="example-contosos-departments-segments-and-policies"></a>예: Contoso의 부서, 세그먼트 및 정책

조직에서 세그먼트와 정책을 정의 하는 방법에 대 한 자세한 내용은 다음 예를 참조 하십시오.

### <a name="contosos-departments-and-plan"></a>Contoso의 부서 및 계획

Contoso에는 HR, Sales, Marketing, Research 및 Manufacturing의 다섯 가지 부서가 있습니다. 업계 규정 준수를 유지 하기 위해 일부 부서의 사용자는 다음 표에 나열 된 것 처럼 다른 부서와 통신 하지 않습니다.

|단편  |에 게 문의할 수 있습니다.  |통신할 수 없음  |
|---------|---------|---------|
|인력     |모든 사람         |(제한 없음)         |
|세율     |HR, 마케팅, 제조         |리서치         |
|마케팅     |모든 사람         |(제한 없음)         |
|리서치     |HR, 마케팅, 제조        |세율     |
|제조 |HR, 마케팅 |HR 또는 Marketing 이외의 모든 사람 |

이러한 점을 고려 하 여 Contoso의 계획에는 다음과 같은 세 가지 정보 장벽 정책이 포함 됩니다.

1. 영업이 연구와의 통신을 차단 하 고, 다른 정책으로 영업과의 통신을 차단 하도록 설계 된 정책
2. 제조에서 HR 및 Marketing과의 통신을 허용 하도록 설계 된 정책 

HR 또는 Marketing에 대 한 정책을 정의할 필요는 없습니다.

### <a name="contosos-defined-segments"></a>Contoso의 정의 된 세그먼트

Contoso는 다음과 같이 Azure Active Directory에서 부서 특성을 사용 하 여 세그먼트를 정의 합니다.

|부서  |세그먼트 정의  |
|---------|---------|
|인력     | `New-OrganizationSegment -Name "HR" -UserGroupFilter "Department -eq 'HR'"`        |
|세율     | `New-OrganizationSegment -Name "Sales" -UserGroupFilter "Department -eq 'Sales'"`        |
|마케팅     | `New-OrganizationSegment -Name "Marketing" -UserGroupFilter "Department -eq 'Marketing'"`        |
|리서치     | `New-OrganizationSegment -Name "Research" -UserGroupFilter "Department -eq 'Research'"`        |
|제조     | `New-OrganizationSegment -Name "Manufacturing" -UserGroupFilter "Department -eq 'Manufacturing'"`        |

정의 된 세그먼트가 있으면 Contoso는 정책 정의를 진행 합니다. 

### <a name="contosos-information-barrier-policies"></a>Contoso의 정보 장벽 정책

Contoso는 다음 표에 설명 된 세 가지 정책을 정의 합니다.

|정책  |정책 정의  |
|---------|---------|
|정책 1: 영업에서 연구와의 통신을 방지 합니다.     | `New-InformationBarrierPolicy -Name "Sales-Research" -AssignedSegment "Sales" -SegmentsBlocked "Research" -State Inactive` <p> 이 예에서 정보 장벽 정책을 *판매 조사*라고 합니다. 이 정책이 활성 상태이 고 적용 되 면 Sales 세그먼트에 있는 사용자가 리서치 세그먼트의 사용자와 통신할 수 없도록 하는 데 도움이 됩니다. 이는 단방향 정책입니다. 이로 인해 연구가 영업과의 통신을 방지할 수는 없습니다. 따라서 정책 2가 필요 합니다.      |
|정책 2: 영업 담당자가 리서치를 진행 하지 못하도록 방지     | `New-InformationBarrierPolicy -Name "Research-Sales" -AssignedSegment "Research" -SegmentsBlocked "Sales" -State Inactive` <p> 이 예에서는 정보 장벽 정책을 *리서치-판매*라고 합니다. 이 정책이 활성화 및 적용 되 면 리서치 세그먼트에 있는 사용자가 Sales 세그먼트의 사용자와 통신할 수 없도록 하는 데 도움이 됩니다.       |
|정책 3: 제조에서 HR 및 마케팅과의 통신만 허용     | `New-InformationBarrierPolicy -Name "Manufacturing-HRMarketing" -AssignedSegment "Manufacturing" -SegmentsAllowed "HR","Marketing" -State Inactive` <p>이 경우 정보 장벽 정책은 *제조-HRMarketing*이라고 합니다. 이 정책이 활성 상태이 고 적용 되 면 Manufacturing은 HR 및 Marketing과만 통신할 수 있습니다. HR 및 Marketing은 다른 세그먼트와 통신 하는 것이 제한 되지 않습니다. |

**InformationBarrierPoliciesApplication** cmdlet을 실행 하 여 모든 세그먼트와 정책을 정의 하 고, Contoso는 정책을 적용 합니다. 

이 작업이 완료 되 면 Contoso는 법적 및 업계 요구 사항을 준수 합니다.

## <a name="related-articles"></a>관련 문서

- [정보 장벽에 대 한 개요 보기](information-barriers.md)

- [Microsoft 팀의 정보 장벽](https://docs.microsoft.com/MicrosoftTeams/information-barriers-in-teams)
