---
title: 정보 장벽 문제 해결
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 06/28/2019
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.collection:
- M365-security-compliance
localization_priority: None
description: 이 문서를 정보 장벽 문제 해결을 위한 지침으로 사용 하십시오.
ms.openlocfilehash: 20937fa4ee050dfa1e3bb4fcfcd582b1c78ccead
ms.sourcegitcommit: 011bfa60cafdf47900aadf96a17eb275efa877c4
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/29/2019
ms.locfileid: "35394303"
---
# <a name="troubleshooting-information-barriers-preview"></a>정보 장벽 문제 해결 (미리 보기)

[정보 장벽 (미리 보기)](information-barriers.md) 을 사용 하면 조직이 법적 요구 사항 및 업계 규정을 준수 하는 데 도움이 됩니다. 예를 들어 정보 장벽에서는 특정 사용자 그룹 간의 통신을 제한 하 여 관심 있는 문제나 다른 문제가 발생 하지 않도록 할 수 있습니다. 정보 장애물을 설정 하는 방법에 대 한 자세한 내용은 [Define information for about about (Preview)](information-barriers-policies.md)을 참조 하십시오.

정보 장벽에 따라 예기치 않은 문제가 발생 하는 경우 이러한 문제를 해결 하기 위해 몇 가지 단계를 수행할 수 있습니다. 이 문서를 참조 하십시오.

> [!IMPORTANT]
> 이 문서에서 설명 하는 작업을 수행 하려면 다음 중 하 나와 같은 적절 한 역할을 할당 받아야 합니다.<br/>-Microsoft 365 Enterprise 전역 관리자<br/>-Office 365 전역 관리자<br/>-준수 관리자<br/>-IB 준수 관리 (새 역할입니다.)<p>정보 장벽에 대 한 필수 구성 요소에 대 한 자세한 내용은 [필수 구성 요소 (정보 장벽 정책)](information-barriers-policies.md#prerequisites)를 참조 하세요.<p>[Office 365 Security & 준수 센터 PowerShell에 연결](https://docs.microsoft.com/powershell/exchange/office-365-scc/connect-to-scc-powershell/connect-to-scc-powershell?view=exchange-ps)되어 있는지 확인 합니다.

## <a name="issue-users-are-unexpectedly-blocked-from-communicating-with-others-in-microsoft-teams"></a>문제: 사용자가 Microsoft 팀의 다른 사람과 통신할 수 없도록 예기치 않게 차단 되었습니다. 

이 경우 사용자는 Microsoft 팀에서 다른 사용자와 통신 하는 동안 예기치 않은 문제를 보고 하 게 됩니다. 예제:
- 사용자가 Microsoft 팀에서 다른 사용자를 검색 하지만 찾을 수는 없습니다.
- 사용자는 Microsoft 팀에서 다른 사용자를 찾을 수 있지만 선택할 수는 없습니다.
- 사용자가 다른 사용자를 볼 수 있지만 Microsoft 팀에서 해당 사용자에 게 메시지를 보낼 수는 없습니다.

### <a name="what-to-do"></a>수행할 작업

사용자가 정보 장벽 정책의 영향을 받는지 여부를 확인 합니다. 정책이 구성 되는 방식에 따라 정보 장벽이 정상적으로 작동할 수 있습니다. 또는 조직의 정책을 구체화 해야 할 수도 있습니다.

1. **InformationBarrierRecipientStatus** Cmdlet을 Identity 매개 변수와 함께 사용 합니다. 

    |구문과  |예제  |
    |---------|---------|
    | `Get-InformationBarrierRecipientStatus -Identity` <p>각 받는 사람을 고유 하 게 식별 하는 모든 id 값 (예: 이름, 별칭, DN (고유 이름), 정식 DN, 전자 메일 주소 또는 GUID)을 사용할 수 있습니다.     |`Get-InformationBarrierRecipientStatus -Identity meganb` <p>이 예제에서는 Identity 매개 변수에 별칭 (*meganb*)을 사용 합니다. 이 cmdlet은 사용자가 정보 장벽 정책의 영향을 받는지 여부를 나타내는 정보를 반환 합니다. (* ExoPolicyId: \<GUID>를 찾아보십시오.)         |

    **사용자가 정보 장벽 정책에 포함 되어 있지 않은 경우 지원 서비스에 문의 하세요**. 그렇지 않으면 다음 단계를 진행 합니다.

2. 정보 장벽 정책에 포함 된 세그먼트를 찾습니다. 이 작업을 수행 하려면 Identity `Get-InformationBarrierPolicy` 매개 변수와 함께 cmdlet을 사용 합니다. 

    |구문과  |예제  |
    |---------|---------|
    |`Get-InformationBarrierPolicy` <p>이전 단계에서 받은 정책 GUID (ExoPolicyId)와 같은 세부 정보를 id 값으로 사용 합니다.     | `Get-InformationBarrierPolicy -Identity b42c3d0f-49e9-4506-a0a5-bf2853b5df6f` <p>이 예에서는 ExoPolicyId *b42c3d0f-49e9-4506-a0a5-bf2853b5df6f*가 있는 정보 장벽 정책에 대 한 자세한 정보를 가져옵니다.         |

    Cmdlet을 실행 한 후 결과에서 **AssignedSegment**, **SegmentsAllowed**및 **SegmentsBlocked** 값을 찾습니다.

    예를 들어 `Get-InformationBarrierPolicy` cmdlet을 실행 한 후에는 결과 목록에서 다음을 살펴보았습니다.

    ```powershell
        AssignedSegment      : Sales
        SegmentsAllowed      : {}
        SegmentsBlocked      : {Research}
    ```
    이 경우 정보 장벽 정책이 Sales 및 Research 세그먼트에 있는 사용자에 게 영향을 줄 수 있습니다. 이 경우에는 영업 직원이 조사 담당자와 의견을 교환할 수 없습니다. 
    
    이 문제가 올바른 것 같으면 정보 장애가 예상 대로 작동 하는 것입니다. 그렇지 않으면 다음 단계를 진행 합니다.

4. 세그먼트가 올바르게 정의 되었는지 확인 합니다. 이 작업을 수행 하려면 `Get-OrganizationSegment` cmdlet을 사용 하 여 결과 목록을 검토 합니다. 

    |구문과  |예제  |
    |---------|---------|
    |`Get-OrganizationSegment`<p>이 cmdlet은 Identity 매개 변수와 함께 사용 합니다.     |`Get-OrganizationSegment -Identity c96e0837-c232-4a8a-841e-ef45787d8fcd` <p>이 예에서는 GUID *c96e0837-c232-4a8a-841e-ef45787d8fcd*가 있는 세그먼트에 대 한 정보를 가져옵니다.         |

    해당 세그먼트에 대 한 세부 정보를 검토 합니다. 필요한 경우 [세그먼트를 편집](information-barriers-edit-segments-policies.md.md#edit-a-segment)하 고 `Start-InformationBarrierPoliciesApplication` cmdlet을 다시 사용 합니다.

    **정보 장벽 정책에 여전히 문제가 있는 경우 고객 지원에 문의 하세요**.

## <a name="issue-communications-are-allowed-between-users-who-should-be-blocked-in-microsoft-teams"></a>문제: Microsoft 팀에서 차단 해야 하는 사용자 간에 통신이 허용 됩니다.

이 경우에는 정보 장벽에 대 한 정의, 활성 및 적용이 가능 하지만 서로 통신 하지 못하게 되는 사용자는 Microsoft 팀에서 서로 채팅할 수 있습니다.

### <a name="what-to-do"></a>수행할 작업

해당 사용자가 정보 장벽 정책에 포함 되어 있는지 확인 합니다. 

1. Identity 매개 변수와 함께 **InformationBarrierRecipientStatus** cmdlet을 사용 합니다.

    |구문과  |예제  |
    |---------|---------|
    |`Get-InformationBarrierRecipientStatus -Identity <value> -Identity2 <value>` <p>이름, 별칭, 고유 이름, 정식 도메인 이름, 전자 메일 주소 또는 GUID와 같은 각 사용자를 고유 하 게 식별 하는 모든 값을 사용할 수 있습니다.     |`Get-InformationBarrierRecipientStatus -Identity meganb -Identity2 alexw` <p>이 예에서는 Office 365의 두 사용자 계정 ( *Megan*용 *meganb* 및 *Alex*용 *alexw* )을 참조 합니다.          |

    
    > [!TIP]
    > 단일 사용자에 대해이 cmdlet을 사용할 수도 있습니다.`Get-InformationBarrierRecipientStatus -Identity <value>`
    
2. 발견 된 내용을 검토 합니다. **InformationBarrierRecipientStatus** cmdlet은 특성 값 및 적용 되는 정보 장벽 정책과 같은 사용자에 대 한 정보를 반환 합니다. 

    결과를 검토 하 고 다음 표에 설명 된 대로 다음 단계를 수행 합니다.
    
    |결과  |다음에 수행할 작업  |
    |---------|---------|
    |선택한 사용자에 대 한 세그먼트가 나열 되지 않음     |다음 중 하나를 수행합니다.<br/>-Azure Active Directory에서 사용자 프로필을 편집 하 여 기존 세그먼트에 사용자를 할당 합니다. ( [Office 365 PowerShell을 사용 하 여 사용자 계정 속성 구성](https://docs.microsoft.com/office365/enterprise/powershell/configure-user-account-properties-with-office-365-powershell)참조)<br/>- [정보 장벽에 대해 지원 되는 특성](information-barriers-attributes.md)을 사용 하 여 세그먼트를 정의 합니다. 그런 다음 [새 정책을 정의](information-barriers-policies.md#part-2-define-information-barrier-policies) 하거나 [기존 정책을 편집](information-barriers-edit-segments-policies.md.md#edit-a-policy) 하 여 해당 세그먼트를 포함 합니다.  |
    |세그먼트는 나열 되지만 해당 세그먼트에 정보 장벽 정책이 할당 되지 않음     |다음 중 하나를 수행합니다.<br/>- 문제의 각 세그먼트에 대 한 [새 정보 장벽 정책 정의](information-barriers-policies.md#part-2-define-information-barrier-policies)<br/>- [기존 정보 장벽 정책을 편집](information-barriers-edit-segments-policies.md.md#edit-a-policy) 하 여 올바른 세그먼트에 할당         |
    |나열 된 세그먼트는 정보 장벽 정책에 포함 되어 있습니다.     |- `Get-InformationBarrierPolicy` Cmdlet을 실행 하 여 정보 장벽 정책이 활성 상태 인지 확인 합니다.<br/>-정책이 적용 `Get-InformationBarrierPoliciesApplicationStatus` 되었는지 확인 하는 cmdlet을 실행 합니다.<br/>- `Start-InformationBarrierPoliciesApplication` Cmdlet을 실행 하 여 모든 활성 정보 장벽 정책 적용          |
    

## <a name="issue-i-need-to-remove-a-single-user-from-an-information-barrier-policy"></a>문제: 정보 장벽 정책에서 단일 사용자를 제거 해야 합니다.

이 경우에는 정보 장벽 정책이 적용 되며 한 명 이상의 사용자가 Microsoft 팀의 다른 사람들과 통신할 수 없도록 예기치 않게 차단 됩니다. 정보 장벽 정책을 모두 제거 하는 대신, 정보 장벽 정책에서 개별 사용자를 한 명 이상 제거할 수 있습니다. 

### <a name="what-to-do"></a>수행할 작업

정보 장벽 정책은 사용자의 세그먼트에 할당 됩니다. 세그먼트는 [사용자 계정 프로필의 특정 특성](information-barriers-attributes.md)을 사용 하 여 정의 됩니다. 단일 사용자 로부터 정책을 제거 해야 하는 경우에는 사용자가 정보 장벽에 의해 영향을 받는 세그먼트에 더 이상 포함 되지 않도록 Azure Active Directory에서 해당 사용자의 프로필을 편집 하는 것이 좋습니다.

1. Identity 매개 변수와 함께 **InformationBarrierRecipientStatus** cmdlet을 사용 합니다. 이 cmdlet은 특성 값 및 적용 되는 정보 장벽 정책과 같은 사용자에 대 한 정보를 반환 합니다.

    |구문과  |예제  |
    |---------|---------|
    |`Get-InformationBarrierRecipientStatus -Identity <value> -Identity2 <value>`<p>이름, 별칭, 고유 이름, 정식 도메인 이름, 전자 메일 주소 또는 GUID와 같은 각 사용자를 고유 하 게 식별 하는 모든 값을 사용할 수 있습니다.     |`Get-InformationBarrierRecipientStatus -Identity meganb -Identity2 alexw` <p>이 예에서는 Office 365의 두 사용자 계정 ( *Megan*용 *meganb* 및 *Alex*용 *alexw* )을 참조 합니다.          |
    |`Get-InformationBarrierRecipientStatus -Identity <value>` <p>이름, 별칭, 고유 이름, 정식 도메인 이름, 전자 메일 주소 또는 GUID와 같은 사용자를 고유 하 게 식별 하는 모든 값을 사용할 수 있습니다.|`Get-InformationBarrierRecipientStatus -Identity jeanp`<p>이 예에서는 Office 365: *jeanp*의 단일 계정을 참조 합니다. |

2. 결과를 검토 하 여 정보 장벽 정책이 할당 되어 있는지와 사용자가 속한 세그먼트 (s)를 확인 합니다. 

3. 정보 장벽에 영향을 받는 세그먼트에서 사용자를 제거 하려면 [Azure Active Directory에서 사용자의 프로필 정보를 업데이트](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-users-profile-azure-portal)합니다.

4. FwdSync가 발생할 때까지 30 분 정도 기다립니다. 또는 `Start-InformationBarrierPoliciesApplication` cmdlet을 실행 하 여 모든 활성 정보 장벽 정책을 적용 합니다.

## <a name="issue-the-information-barrier-application-process-is-taking-too-long"></a>문제: 정보 장벽 응용 프로그램 프로세스가 너무 오래 걸립니다.

**InformationBarrierPoliciesApplication** cmdlet을 실행 한 후 프로세스를 완료 하는 데 시간이 너무 오래 걸립니다.

### <a name="what-to-do"></a>수행할 작업

정책 응용 프로그램 cmdlet을 실행 하는 경우 조직의 모든 계정에 대 한 정보 장벽 정책이 사용자에 의해 적용 되거나 제거 됩니다. 사용자 수가 많은 경우 처리 하는 데 시간이 오래 걸릴 것입니다. 일반적으로 5000 사용자 계정을 처리 하는 데 한 시간 정도 소요 됩니다.

1. **InformationBarrierPoliciesApplicationStatus** cmdlet을 사용 하 여 가장 최근 정책 응용 프로그램의 상태를 확인할 수 있습니다.

    |최신 정책 응용 프로그램을 보려면  |모든 정책 응용 프로그램의 상태를 보려면  |
    |---------|---------|
    |`Get-InformationBarrierPoliciesApplicationStatus`     |`Get-InformationBarrierPoliciesApplicationStatus -All $true`         |


    이렇게 하면 정책 응용 프로그램이 완료, 실패 또는 진행 중인지에 대 한 정보가 표시 됩니다.

2. 이전 단계의 결과에 따라 다음 단계 중 하나를 수행 합니다.
  
    |상태  |다음 단계  |
    |---------|---------|
    |**시작 되지 않음**     |**InformationBarrierPoliciesApplication** cmdlet을 실행 한 후 45 분이 경과 하면 감사 로그를 검토 하 여 정책 정의에 오류가 있는지 또는 응용 프로그램이 시작 되지 않은 다른 이유가 있는지를 확인 합니다. |
    |**실패**     |응용 프로그램이 실패 한 경우 감사 로그를 검토 합니다. 또한 세그먼트 및 정책도 검토 합니다. 두 개 이상의 세그먼트에 할당 된 사용자가 있나요? 모든 세그먼트에 두 개 이상의 poliicy이 할당 됩니까? 필요한 경우 세그먼트 및/또는 [편집 정책을](information-barriers-edit-segments-policies.md.md#edit-a-policy) [편집](information-barriers-edit-segments-policies.md.md#edit-a-segment) 하 고 **InformationBarrierPoliciesApplication** cmdlet을 다시 실행 합니다.  |
    |**진행 중**     |응용 프로그램이 계속 진행 되 고 있는 경우 완료 하는 데 더 많은 시간이 걸릴 수 있습니다. 기간이 며칠 이면 감사 로그를 수집한 다음 고객 지원에 문의 하세요. |

## <a name="issue-information-barrier-policies-are-not-being-applied-at-all"></a>문제: 정보 장벽 정책이 전혀 적용 되지 않음

이 경우에는 세그먼트, 정의 된 정보 장벽 정책 및 해당 정책을 적용 하려고 했습니다. 그러나 `Get-InformationBarrierPoliciesApplicationStatus` cmdlet을 실행 하면 정책 응용 프로그램에 오류가 발생 한 것을 확인할 수 있습니다.

### <a name="what-to-do"></a>수행할 작업

조직에 [Exchange 주소록 정책이](https://docs.microsoft.com/exchange/address-books/address-book-policies/address-book-policies) 구축 되어 있지 않은지 확인 합니다. 이러한 정책을 통해 정보 장벽 정책이 적용 되지 않습니다.

1. [Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell?view=exchange-ps)에 연결 합니다. 

2. [Get-AddressBookPolicy](https://docs.microsoft.com/powershell/module/exchange/email-addresses-and-address-books/get-addressbookpolicy?view=exchange-ps) cmdlet을 실행 하 고 결과를 검토 합니다.

    |결과  |다음 단계  |
    |---------|---------|
    |Exchange 주소록 정책이 나열 됩니다.     |[주소록 정책 제거](https://docs.microsoft.com/exchange/address-books/address-book-policies/remove-an-address-book-policy)         |
    |주소록 정책이 없습니다. |감사 로그를 검토 하 여 정책 응용 프로그램에 오류가 발생 하는 이유 찾기 |

3. [사용자 계정, 세그먼트, 정책 또는 정책 응용 프로그램의 상태를 확인](information-barriers-policies.md#view-status-of-user-accounts-segments-policies-or-policy-application)합니다.

## <a name="related-topics"></a>관련 항목

[Microsoft 팀의 정보 장벽에 대 한 정책 정의 (미리 보기)](information-barriers-policies.md)

[정보 장벽 (미리 보기)](information-barriers.md)



