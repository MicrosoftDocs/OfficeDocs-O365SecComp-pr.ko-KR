---
title: 정보 장벽 문제 해결
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 05/31/2019
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.collection:
- M365-security-compliance
localization_priority: None
description: 이 문서를 정보 장벽 문제 해결을 위한 지침으로 사용 하십시오.
ms.openlocfilehash: b37585469ec8bb299b7976f8a330f4c6b29e3f95
ms.sourcegitcommit: 4fedeb06a6e7796096fc6279cfb091c7b89d484d
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/31/2019
ms.locfileid: "34668325"
---
# <a name="troubleshooting-information-barriers-preview"></a>정보 장벽 문제 해결 (미리 보기)

정보 장애물은 조직이 법적 요구 사항 및 업계 규정을 준수 하는 데 도움이 될 수 있습니다. 예를 들어 정보 장벽에서는 특정 사용자 그룹 간의 통신을 제한 하 여 관심 있는 문제나 다른 문제가 발생 하지 않도록 할 수 있습니다. 자세한 내용은 [정보 장벽 (미리 보기)](information-barriers.md)을 참조 하십시오.

이 문서에서는 질문에 대 한 대답을 가져오거나 정보 장벽에서 발생할 수 있는 문제를 해결 하는 데 사용할 수 있는 지침을 제공 합니다.  

## <a name="before-you-begin"></a>시작 하기 전에

이 문서에서 설명 하는 작업을 수행 하려면 다음 중 하 나와 같은 적절 한 역할을 할당 받아야 합니다.
- Microsoft 365 Enterprise 전역 관리자
- Office 365 전역 관리자
- 준수 관리자
- IB 준수 관리 (새 역할입니다.)

역할 및 사용 권한에 대 한 자세한 내용은 [permissions in The Office 365 Security & 준수 센터](permissions-in-the-security-and-compliance-center.md)를 참조 하십시오.

정보 장벽에 대 한 필수 구성 요소에 대 한 자세한 내용은 [필수 구성 요소 (정보 장벽 정책)](information-barriers-policies.md#prerequisites)를 참조 하세요.

또한 [Office 365 Security & 준수 센터 PowerShell에 연결](https://docs.microsoft.com/powershell/exchange/office-365-scc/connect-to-scc-powershell/connect-to-scc-powershell?view=exchange-ps)해야 합니다.

## <a name="issue-people-are-unexpectedly-blocked-from-communicating-in-microsoft-teams"></a>문제: 사용자가 Microsoft 팀에서 의견을 교환할 수 없도록 예기치 않게 차단 되었습니다. 

이 경우 사용자는 Microsoft 팀에서 예기치 않은 문제를 보고 하 게 됩니다. 예제:
- 사용자가 Microsoft 팀에서 다른 사용자를 찾거나 통신할 수 없습니다.
- 사용자가 Microsoft 팀에서 다른 사용자를 보거나 선택할 수 없습니다.
- 사용자는 Microsoft 팀의 다른 사용자에 게 메시지를 볼 수는 있지만 보낼 수는 없습니다.

### <a name="what-to-do"></a>수행할 작업

1. 사용자가 정보 장벽 정책의 영향을 받는지 여부를 확인 합니다. 이 작업을 수행 하려면 **InformationBarrierRecipientStatus** Cmdlet을 Identity 매개 변수와 함께 사용 합니다. 

    구문은`Get-InformationBarrierRecipientStatus -Identity`

    각 받는 사람을 고유 하 게 식별 하는 모든 id 값 (예: 이름, 별칭, DN (고유 이름), 정식 DN, 전자 메일 주소 또는 GUID)을 사용할 수 있습니다.

    예제: `Get-InformationBarrierRecipientStatus -Identity meganb`

    이 예제에서는 Identity 매개 변수에 별칭 (*meganb*)을 사용 합니다. 이 cmdlet은 사용자가 정보 장벽 정책의 영향을 받는지 여부를 나타내는 정보를 반환 합니다. (* ExoPolicyId: \<GUID>를 찾아보십시오.)

    사용자가 정보 장벽 정책에 포함 되어 있지 않은 경우 지원 서비스에 문의 하세요. 그렇지 않으면 다음 단계를 진행 합니다.

2. 정보 장벽 정책에 포함 된 세그먼트를 찾습니다. 이 작업을 수행 하려면 Identity `Get-InformationBarrierPolicy` 매개 변수와 함께 cmdlet을 사용 합니다. 이전 단계에서 받은 정책 GUID (ExoPolicyId)와 같은 세부 정보를 id 값으로 사용 합니다.

    예제: `Get-InformationBarrierPolicy -Identity b42c3d0f-49e9-4506-a0a5-bf2853b5df6f`

    이 예에서는 ExoPolicyId *b42c3d0f-49e9-4506-a0a5-bf2853b5df6f*가 있는 정보 장벽 정책에 대 한 자세한 정보를 가져옵니다.
    
    Cmdlet을 실행 한 후 결과에서 **AssignedSegment**, **SegmentsAllowed**및 **SegmentsBlocked** 값을 찾습니다.

    예: `Get-InformationBarrierPolicy` cmdlet을 실행 한 후 결과 목록에서 다음을 살펴보았습니다.

    ```powershell
        AssignedSegment      : Sales
        SegmentsAllowed      : {}
        SegmentsBlocked      : {Research}
    ```
    이 경우 정보 장벽 정책이 Sales 및 Research 세그먼트에 있는 사용자에 게 영향을 줄 수 있습니다. 이 경우에는 영업 직원이 조사 담당자와 의견을 교환할 수 없습니다. 이 문제가 올바른 것 같으면 정보 장애가 예상 대로 작동 하는 것입니다. 그렇지 않으면 다음 단계를 진행 합니다.

4. 세그먼트가 올바르게 정의 되었는지 확인 합니다. 이 작업을 수행 하려면 `Get-OrganizationSegment` cmdlet을 사용 하 여 결과 목록을 검토 합니다. 

    특정 세그먼트에 대 한 세부 정보를 보려면 Identity `Get-OrganizationSegment` 매개 변수와 함께 cmdlet을 사용 합니다. 

    예제: `Get-OrganizationSegment -Identity c96e0837-c232-4a8a-841e-ef45787d8fcd`

    이 예에서는 GUID *c96e0837-c232-4a8a-841e-ef45787d8fcd*가 있는 세그먼트에 대 한 정보를 가져옵니다.

    해당 세그먼트에 대 한 세부 정보를 검토 합니다. 필요한 경우 [세그먼트를 편집](information-barriers-policies.md#edit-a-segment)하 고 `Start-InformationBarrierPoliciesApplication` cmdlet을 다시 사용 합니다.

    정보 장벽 정책에 여전히 문제가 있는 경우 고객 지원에 문의 하세요.
    
## <a name="issue-the-information-barrier-application-process-is-taking-too-long"></a>문제: 정보 장벽 응용 프로그램 프로세스가 너무 오래 걸립니다.

**InformationBarrierPoliciesApplication** cmdlet을 실행 한 후 프로세스를 완료 하는 데 시간이 너무 오래 걸립니다.

### <a name="what-to-do"></a>수행할 작업

1. 정책 응용 프로그램 cmdlet을 실행 하는 경우 조직의 모든 계정에 대 한 정보 장벽 정책이 사용자에 의해 적용 되거나 제거 됩니다. 사용자 수가 많은 경우 처리 하는 데 시간이 오래 걸릴 것입니다. 일반적으로 5000 사용자 계정을 처리 하는 데 한 시간 정도 소요 됩니다. 

2. **InformationBarrierPoliciesApplicationStatus** cmdlet을 사용 하 여 상태를 확인 합니다.

    구문과`Get-InformationBarrierPoliciesApplicationStatus`

    모든 정보 장벽 정책 응용 프로그램의 상태를 표시 하려면 다음을 사용 합니다.`Get-InformationBarrierPoliciesApplicationStatus -All $true`

    이렇게 하면 정책 응용 프로그램을 완료, 실패 또는 진행 중인지 여부에 대 한 정보가 표시 됩니다.

3. 2 단계의 결과에 따라 다음 단계 중 하나를 수행 합니다.

    - 응용 프로그램이 시작 되지 않은 경우 **InformationBarrierPoliciesApplication** cmdlet을 실행 한 후 45 분이 지난 후에는 감사 로그를 검토 하 여 정책 정의에 오류가 있는지 또는 다른 이유를 확인 하십시오. 응용 프로그램이 시작 되지 않았습니다.

    - 응용 프로그램에 오류가 발생 한 경우에는 사용자의 세그먼트와 정책을 검토 합니다. 필요한 경우 세그먼트 및/또는 [편집 정책을](information-barriers-policies.md#edit-a-policy) [편집](information-barriers-policies.md#edit-a-segment) 하 고 **InformationBarrierPoliciesApplication** cmdlet을 다시 실행 합니다.

    - 응용 프로그램이 계속 진행 되 고 있는 경우 완료 하는 데 더 많은 시간이 걸릴 수 있습니다. 며칠 이내에 지원 담당자에 게 문의 하세요.

## <a name="related-topics"></a>관련 항목

[Microsoft 팀의 정보 장벽에 대 한 정책 정의 (미리 보기)](information-barriers-policies.md)

[정보 장벽 (미리 보기)](information-barriers.md)



