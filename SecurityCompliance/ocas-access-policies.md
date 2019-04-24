---
title: Office 365 Cloud App Security 액세스 정책
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.reviewer: alesibov
ms.audience: Admin
ms.topic: reference
ms.date: 02/27/2019
ms.service: O365-seccomp
localization_priority: Normal
description: Office 365 cloud App Security access 정책을 사용 하면 사용자, 위치, 장치 및 앱을 기반으로 클라우드 앱 액세스를 실시간으로 모니터링 하 고 제어할 수 있습니다. 관리 되는 장치에 클라이언트 인증서를 배포 하거나 타사 MDM 인증서와 같은 기존 인증서를 사용 하 여 도메인에 가입 되지 않은 장치를 포함 하 여 Windows Intune에서 관리 되지 않는 장치에 대 한 액세스 정책을 만들 수 있습니다. 예를 들어 관리 되는 장치에 클라이언트 인증서를 배포한 다음 인증서 없이 장치에서 액세스 하는 것을 차단할 수 있습니다.
ms.openlocfilehash: 5e8b8fa293420bc9ff3616daf288b8e02a2eb768
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32263009"
---
# <a name="access-policies-in-office-365-cloud-app-security"></a>Office 365 Cloud App Security 액세스 정책

|계산 * *\>**|계획 * *\>**|배포 * *\>**|사용률 * * * *|
|:-----|:-----|:-----|:-----|
|[평가 시작](office-365-cas-overview.md) <br/> |[계획 시작](get-ready-for-office-365-cas.md) <br/> |사용자가 여기 있어!  <br/> [다음 단계](group-your-ip-addresses-in-ocas.md) <br/> |[활용 시작](utilization-activities-for-ocas.md) <br/> |

Office 365 cloud App Security access 정책을 사용 하면 사용자, 위치, 장치 및 앱을 기반으로 클라우드 앱 액세스를 실시간으로 모니터링 하 고 제어할 수 있습니다. 관리 되는 장치에 클라이언트 인증서를 배포 하거나 타사 MDM 인증서와 같은 기존 인증서를 사용 하 여 도메인에 가입 되지 않은 장치를 포함 하 여 Windows Intune에서 관리 되지 않는 장치에 대 한 액세스 정책을 만들 수 있습니다. 예를 들어 관리 되는 장치에 클라이언트 인증서를 배포한 다음 인증서 없이 장치에서 액세스 하는 것을 차단할 수 있습니다.

 [세션 정책을](ocas-session-policies.md) 사용 하 여 액세스를 완전히 허용 하거나 차단 하지 않고 세션을 모니터링 하 고 특정 세션 작업을 제한 하는 동안 액세스를 허용할 수 있습니다.

## <a name="prerequisites-to-using-access-policies"></a>액세스 정책 사용을 위한 필수 구성 요소

- Azure AD Premium P1 라이선스

- 관련 앱을 [조건부 액세스 앱 컨트롤을 사용 하 여 배포](https://docs.microsoft.com/en-us/cloud-app-security/proxy-deployment-aad) 해야 합니다.

- 아래에 설명 된 대로 사용자를 Office 365 Cloud App Security로 리디렉션하는 [Azure AD 조건부 액세스 정책이](https://docs.microsoft.com/azure/active-directory/active-directory-conditional-access-azure-portal) 있어야 합니다.

## <a name="create-an-azure-ad-conditional-access-policy"></a>Azure AD 조건부 액세스 정책 만들기

Azure Active Directory 조건부 액세스 정책 및 클라우드 응용 프로그램 보안 세션 정책은 각 사용자 세션을 검사 하 고 각 앱에 대 한 정책 결정을 내리는 동시에 작동 합니다. Azure AD에서 조건부 액세스 정책을 설정 하려면 다음 절차를 수행 합니다.

1. 사용자 또는 사용자 그룹에 대 한 할당과 조건부 액세스 앱 컨트롤을 사용 하 여 제어할 앱에 대 한 할당을 사용 하 여 [Azure AD 조건부 액세스 정책을](https://docs.microsoft.com/azure/active-directory/active-directory-conditional-access-azure-portal) 구성 합니다.<br>참고:  [조건부 Access 앱 컨트롤을 사용 하 여 배포한](https://docs.microsoft.com/cloud-app-security/proxy-deployment-aad)앱만이 정책의 영향을 받습니다.

2.  **Session**에서 **조건부 액세스 앱 제어 적용 제한** 사용을 선택 하 여 Office 365 Cloud App Security로 사용자를 라우팅합니다.

## <a name="create-a-cloud-app-security-access-policy"></a>Cloud App Security access 정책 만들기

새 액세스 정책을 만들려면 다음 절차를 수행 합니다.

1. 포털에서 **제어** 다음에 **정책을**선택 합니다.

2.  **정책** 페이지에서 **정책** 만들기를 클릭 하 고 **액세스 정책을**선택 합니다.

3.  **액세스 정책** 창에서 *관리 되지 않는 장치 로부터의 액세스 차단*같은 정책의 이름을 할당 합니다.

4.   **다음의 모든**항목에 해당 하는 활동의 **활동 원본**에서 정책에 적용할 추가 활동 필터를 선택 합니다. 필터에는 다음 옵션이 포함 됩니다.
    
    - **장치 태그**:이 필터를 사용 하 여 관리 되지 않는 장치를 식별 합니다.
    
    - **위치**:이 필터를 사용 하 여 알 수 없는 (또는 위험한) 위치를 식별 합니다.
    
    - **ip 주소**:이 필터를 사용 하 여 ip 주소당 필터링 하거나 이전에 할당 된 ip 주소 태그를 사용 합니다.
    
    - **사용자 에이전트 태그**:이 필터를 사용 하 여 추론에서 모바일 및 데스크톱 앱을 식별 하도록 설정 합니다. 이 필터는 같음 또는 같지 않음으로 설정할 수 있습니다. 각 클라우드 앱에 대해 모바일 및 데스크톱 앱에 대해 값을 테스트 해야 합니다.

5.  **작업**에서 다음 옵션 중 하나를 선택 합니다.
    
    - **Allow**: 설정한 정책 필터에 따라 명시적으로 액세스를 허용 하도록이 작업을 설정 합니다.
    
    - **차단**: 설정한 정책 필터에 따라 액세스를 명시적으로 차단 하려면이 작업을 설정 합니다.

6.  **정책의 심각도로 각 일치 이벤트에 대 한 알림을 만들고** 경고 제한을 설정 하 고 알림을 전자 메일, 문자 메시지 또는 둘 다 중에서 선택할 수 있습니다.

## <a name="next-steps"></a>다음 단계

- [IP를 그룹화하여 Office 365 Cloud App Security 관리를 단순화](group-your-ip-addresses-in-ocas.md)