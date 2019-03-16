---
title: Office 365에서 불법 동의 권한 부여 검색 및 교정
ms.author: chrfox
author: chrfox
manager: laurawi
ms.date: 4/23/2018
ms.audience: ITPro
ms.topic: article
ms.collection:
- o365_security_incident_response
- M365-security-compliance
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
description: Office 365에서 불법 동의 부여 공격을 인식 하 고 수정 하는 방법에 대해 알아봅니다.
ms.openlocfilehash: 454b1b0dcf7a6182895dcc97889286f3000c9626
ms.sourcegitcommit: 8657e003ab1ff49113f222d1ee8400eff174cb54
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/16/2019
ms.locfileid: "30656074"
---
# <a name="detect-and-remediate-illicit-consent-grants-in-office-365"></a>Office 365에서 불법 동의 권한 부여 검색 및 교정

**요약**  Office 365에서 불법 동의 부여 공격을 인식 하 고 수정 하는 방법에 대해 알아봅니다.

## <a name="what-is-the-illicit-consent-grant-attack-in-office-365"></a>Office 365의 불법 동의 허용 이란?
공격자는 불법 공격을 허용 하 여 연락처 정보, 전자 메일 또는 문서 등의 데이터에 대 한 액세스를 요청 하는 Azure 등록 응용 프로그램을 만듭니다. 그런 다음 공격자는 최종 사용자에 게 피싱 공격을 통해 데이터에 대 한 액세스를 허용 하거나 신뢰할 수 있는 웹 사이트에 불법 코드를 삽입 하는 방법으로 응용 프로그램에 동의 하도록 합니다. 불법 응용 프로그램에 동의 하면 조직 계정 없이도 데이터에 대 한 계정 수준의 액세스 권한이 부여 됩니다. 계정에 대 한 암호를 다시 설정 하거나 문제에 대 한 다단계 인증 (MFA)을 요청 하는 등의 일반 재구성 단계는 타사 응용 프로그램 이며 조직 외부에 있는 경우에는 이러한 유형의 공격에는 효과적이 지 않습니다. 이러한 공격은 정보를 호출 하는 엔터티가 사람이 아니라 자동화 인 것으로 가정 하는 상호 작용 모델을 활용 합니다.

## <a name="what-does-an-illicit-consent-grant-attack-look-like-in-office-365"></a>불법 동의는 Office 365에서 공격을 허용 하는 것과 유사 합니다.
Office 365 **감사 로그** 를 검색 하 여이 공격의 손상 (IOC) 라고도 하는 서명을 확인 해야 합니다. 많은 Azure 등록 응용 프로그램 및 대규모 사용자 기반 조직의 경우에는 조직에서 주 단위로 승인 권한을 검토 하는 것이 가장 좋습니다.
### <a name="steps-for-finding-signs-of-this-attack"></a>이 공격의 신호를 찾는 단계
1. Office 365 테 넌 트에서 **보안 및 준수 센터** 를 엽니다.
2. **검색 & 조사** 노드로 이동 하 고 **감사 로그** 검색을 선택 합니다.
3. 검색 (모든 작업 및 모든 사용자)을 만들고, 응용 프로그램에 대 한 승인 결과를 필터링 하 고, OAuth2PermissionGrant를 추가 합니다.
4. 확장 속성을 검사 하 고 isadmincontent가 True로 설정 되어 있는지 확인 합니다.


이 값이 true 이면 전역 관리자 액세스 권한이 있는 사용자가 데이터에 광범위 하 게 액세스할 수 있음을 나타냅니다. 예기치 않은 경우 [공격을 확인](detect-and-remediate-illicit-consent-grants.md#confirmattack)하기 위한 단계를 수행 합니다.

<a name="confirmattack"> </a>
## <a name="how-to-confirm-an-attack"></a>공격을 확인 하는 방법
위에 나열 된 iocs의 인스턴스가 하나 이상 있으면 공격이 발생 한 것을 확실 하 게 확인 하려면 추가 조사를 수행 해야 합니다. 이러한 세 가지 방법 중 하나를 사용 하 여 공격을 확인할 수 있습니다.
- Azure Active Directory 포털을 사용 하는 인벤토리 응용 프로그램 및 사용 권한 이 방법은 완벽 하지만 확인할 사용자가 많은 경우에는 한 번에 한 명의 사용자만 확인할 수 있습니다.
- PowerShell을 사용 하는 인벤토리 응용 프로그램 및 권한 오버 헤드가 가장 빠르고 대부분의 완벽 한 방법입니다.
- 사용자가 자신의 앱 및 사용 권한을 개별적으로 확인 하 고 재구성을 위해 관리자에 게 결과를 다시 보고 하도록 합니다.

## <a name="inventory-apps-with-access-in-your-organization"></a>조직에 대 한 액세스 권한이 있는 인벤토리 앱
Azure Active Directory Portal 또는 PowerShell을 사용 하 여 사용자에 게이 작업을 수행 하거나 사용자가 응용 프로그램 액세스를 개별적으로 열거할 수 있습니다.

### <a name="steps-for-using-the-azure-active-directory-portal"></a>Azure Active Directory 포털을 사용 하기 위한 단계
[Azure Active Directory 포털](https://portal.azure.com/)을 사용 하 여 개별 사용자가 사용 권한을 부여한 응용 프로그램을 조회할 수 있습니다. 
1. 관리 권한을 사용 하 여 Azure Portal에 로그인 합니다.
2. Azure Active Directory 블레이드를 선택 합니다.
3. **사용자**를 선택 합니다.
4. 검토할 사용자를 선택 합니다.
5. **응용 프로그램**을 선택 합니다.

여기에는 사용자에 게 할당 된 앱과 applcations에 게 부여 되는 사용 권한이 표시 됩니다.

### <a name="steps-for-having-your-users-enumerate-their-application-access"></a>사용자에 게 응용 프로그램 액세스를 열거 하기 위한 단계
사용자가으로 이동 하 https://myapps.microsoft.com 여 해당 응용 프로그램에 대 한 액세스를 검토 하도록 합니다. 액세스 권한이 있는 모든 앱을 볼 수 있고, 액세스 범위를 포함 하 여이에 대 한 세부 정보를 보고, 의심 스러운 앱 또는 불법 응용 프로그램에 대 한 권한을 해지할 수 있어야 합니다.

### <a name="steps-for-doing-this-with-powershell"></a>PowerShell에서이 작업을 수행 하기 위한 단계
불법도를 확인 하는 가장 간단한 방법은 테 넌 트의 모든 사용자에 대 한 모든 oauth 승인 권한 부여 및 oauth 앱을 하나의 .csv 파일로 덤프 하는 Get-AzureADPSPermissions를 실행 하는 것입니다 [.](https://gist.github.com/psignoret/41793f8c6211d2df5051d77ca3728c09) 

#### <a name="pre-requisites"></a>필수 구성 요소
- Azure AD PowerShell 라이브러리가 설치 되었습니다.
- 스크립트를 실행할 테 넌 트에 대 한 전역 관리자 권한
- 스크립트를 실행 하는 컴퓨터의 로컬 관리자입니다.

> [!IMPORTANT]
> 관리 계정에 대해 multi-factor authentication을 사용 하는 것이 좋습니다.  이 스크립트는 MFA 인증을 지원 합니다.

1. 로컬 관리자 권한이 있는 스크립트를 실행 하는 컴퓨터에 로그인 합니다.
2. GitHub에서 [Get-AzureADPSPermissions](https://gist.github.com/psignoret/41793f8c6211d2df5051d77ca3728c09) 스크립트를 다운로드 하거나 복사 하 여 scruipt를 실행 하는 데 사용할 폴더를 지정 합니다.  이 폴더는 출력이 "permissions" 파일을 작성할 때 사용 하는 폴더가 됩니다.
3. 관리자로 PowerShell 인스턴스를 열고 스크립트를 저장 한 폴더로 엽니다.
4. [AzureAD](https://docs.microsoft.com/powershell/module/azuread/connect-azuread?view=azureadps-2.0) cmdlet을 사용 하 여 디렉터리에 연결 합니다.
5. 이 PowerShell 명령줄을 다음과 같이 실행 합니다.`Get-AzureADPSPermissions.ps1 | Export-csv -path "Permissions.csv" -NoTypeInformation`

이 스크립트는 사용 권한 .csv 라는 파일 하나를 생성 합니다. 다음 단계에 따라 불법 응용 프로그램 권한 부여를 확인 합니다. 
1. ConsentType 열 (G 열)에서 "allprinciples" 값을 검색 합니다. allprincipals 사용 권한을 사용 하면 클라이언트 응용 프로그램에서 테 넌 시의 모든 사용자 콘텐츠에 액세스할 수 있습니다. 네이티브 Office 365 응용 프로그램은 올바르게 작동 하려면이 권한이 필요 합니다. 이 권한이 있는 Microsoft가 아닌 모든 응용 프로그램은 신중 하 게 검토 해야 합니다.
2.  사용 권한 열 (F 열)에서 각 위임 된 응용 프로그램의 콘텐츠에 적용 되는 사용 권한을 검토 합니다. "읽기" 및 "쓰기" 사용 권한 또는 "*"를 찾습니다. All "사용 권한 및 적절 하지 않을 수 있으므로 신중 하 게 검토 합니다.
3.  consents이 부여 된 특정 사용자를 검토 합니다. 높은 프로필 또는 높은 영향을 가진 사용자에 게 부적절 한 consents 부여 된 경우 더 자세히 조사 해야 합니다.
4.  clientdisplayname 열 (C 열)에서 의심 스러운 것으로 보이는 앱을 찾습니다. 이름이 철자가 잘못 된 앱, super bland name 또는 해커의 소리가 나 게 되는 이름은 신중 하 게 검토 해야 합니다.

## <a name="determine-the-scope-of-the-attack"></a>공격 범위 결정
응용 프로그램 액세스 인벤토리를 완료 한 후에는 Office 365 **감사 로그** 를 검토 하 여 위반의 전체 범위를 확인 합니다.  영향을 받는 사용자, 불법 응용 프로그램에서 조직에 액세스 하는 데 사용 하는 기간 및 앱에 대 한 권한을 검색 합니다. [Office 365 보안 및 준수 센터](https://support.office.com/article/Search-the-audit-log-in-the-Office-365-Security-Compliance-Center-0d4d0f35-390b-4518-800e-0c7ec95e946c)에서 **감사 로그** 를 검색할 수 있습니다. 

> [!IMPORTANT]
> [관리자 및 사용자에 대 한](https://support.office.com/article/turn-office-365-audit-log-search-on-or-off-e893b19a-660c-41f2-9074-d3631c95a014) [사서함 감사](https://support.office.com/article/Enable-mailbox-auditing-in-Office-365-aaca8987-5b62-458b-9882-c28476a66918) 및 활동 감사는이 정보를 받기 전에 사용 하도록 설정 되어 있어야 합니다.

## <a name="how-to-stop-and-remediate-an-illicit-consent-grant--attack"></a>불법 동의를 중지 하 고 수정 하는 방법 공격 허용
불법 사용 권한이 있는 응용 프로그램을 식별 한 후에는 여러 가지 방법으로 해당 액세스 권한을 제거할 수 있습니다.
- 다음을 수행 하 여 Azure Active Directory 포털에서 응용 프로그램의 권한을 해지할 수 있습니다.
    - **Azure Active Directory 사용자** 블레이드에서 영향을 받는 사용자로 이동 합니다.
    - **응용 프로그램**을 선택 합니다.
    - 불법 응용 프로그램을 선택 합니다.
    - 드릴 다운에서 **제거** 를 클릭 합니다.
- [AzureADOAuth2PermissionGrant](https://docs.microsoft.com/powershell/module/azuread/Remove-AzureADOAuth2PermissionGrant?view=azureadps-2.0)의 단계에 따라 PowerShell을 사용 하 여 OAuth 승인 부여를 해지할 수 있습니다.
- [AzureADServiceAppRoleAssignment](https://docs.microsoft.com/powershell/module/azuread/Remove-AzureADServiceAppRoleAssignment?view=azureadps-2.0)의 단계에 따라 PowerShell을 사용 하 여 서비스 앱 역할 할당을 해지할 수 있습니다.
- 영향을 받는 계정에 대해서도 로그인을 사용 하지 않도록 설정할 수 있으며,이는 해당 계정의 데이터에 대 한 앱 액세스를 사용 하지 않도록 설정 합니다. 이는 최종 사용자의 생산성을 유지 하는 데 이상적이 지 않지만, 영향을 빠르게 하는 작업을 수행 하는 경우에는 장기 관리가 가능한 단기 수정이 될 수 있습니다.
- 테 넌 시에 통합 된 응용 프로그램을 해제할 수 있습니다. 이 단계는 최종 사용자가 테 넌 트 전반에 대해 동의를 부여할 수 없도록 하는 절차입니다. 이렇게 하면 사용자가 악의적인 응용 프로그램에 실수로 액세스 하는 것을 방지할 수 있습니다. 이는 타사 응용 프로그램의 생산성을 높이기 위해 사용자의 능력을 엄격히 저하 시키기 것이 좋습니다.  [통합 앱을 설정 하거나 해제](https://support.office.com/article/Turning-Integrated-Apps-on-or-off-7e453a40-66df-44ab-92a1-96786cb7fb34)하는 단계를 수행 하 여이 작업을 수행할 수 있습니다.

## <a name="secure-office-365-like-a-cybersecurity-pro"></a>cybersecurity pro와 같은 Office 365 보호
Office 365 구독에는 데이터와 사용자를 보호 하는 데 사용할 수 있는 강력한 보안 기능 집합이 포함 되어 있습니다.  office 365 보안 로드맵: office 365 테 넌 트를 보호 하기 위한 Microsoft 권장 모범 사례를 구현 하는 데 [처음 30 일, 90 일 및 그 이상에 대 한 주요 우선 순위](https://support.office.com/article/office-365-security-roadmap-top-priorities-for-the-first-30-days-90-days-and-beyond-28c86a1c-e4dd-4aad-a2a6-c768a21cb352) 를 사용 합니다.
- 처음 30 일 이내에 수행 해야 하는 작업입니다.  이러한 설정은 즉시 영향을 미치며 사용자에 게 미치는 영향이 낮습니다.
- 90 일 이내에 수행할 작업입니다. 이러한 작업은 계획 하 고 구현 하는 데 다소 시간이 걸리고 보안 환경을 크게 향상 시킵니다.
- 90 일을 초과 합니다. 처음 90 일의 향상 된 기능 빌드는 다음과 같은 작업을 수행 합니다.

## <a name="see-also"></a>참고 항목:
- [내 응용 프로그램 목록에서 예기치 않은 응용 프로그램](https://docs.microsoft.com/azure/active-directory/application-access-unexpected-application) 은 데이터에 대 한 액세스 권한이 있는 예기치 않은 응용 프로그램이 있다는 것을 모르고 관리자에 게 필요한 다양 한 작업을 안내 합니다.
- [Azure Active Directory를 사용 하 여 응용 프로그램 통합]  (https://docs.microsoft.com/azure/active-directory/active-directory-apps-permissions-consent) 승인 및 사용 권한에 대 한 간략 한 개요입니다.)  [승인 프레임 워크 섹션의 개요](https://docs.microsoft.com/azure/active-directory/develop/active-directory-integrating-applications#overview-of-the-consent-framework) 에 특히 주의 합니다.
- [문제 내 응용 프로그램을 개발](https://docs.microsoft.com/azure/active-directory/active-directory-application-dev-development-content-map) 하는 경우 다양 한 승인 관련 문서의 링크를 제공 합니다.
- azure [Active Directory의 응용 프로그램 및 서비스 보안 주체 개체 (azure AD)](https://docs.microsoft.com/azure/active-directory/develop/active-directory-application-objects) 에서는 응용 프로그램 모델의 핵심 응용 프로그램 및 서비스 보안 주체 개체에 대 한 개요를 제공 합니다.
- [앱에 대 한 액세스 관리](https://docs.microsoft.com/azure/active-directory/active-directory-managing-access-to-apps) 는 관리자가 앱에 대 한 사용자 액세스를 관리 하기 위해 사용 해야 하는 기능에 대 한 개요입니다.
