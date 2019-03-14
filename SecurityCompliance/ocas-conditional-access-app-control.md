---
title: Office 365 Cloud App Security 조건부 액세스 앱 컨트롤을 사용하여 앱 보호
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.reviewer: alesibov
ms.audience: Admin
ms.topic: reference
ms.date: 02/27/2019
ms.service: O365-seccomp
localization_priority: Normal
description: Office 365 Cloud app Security 조건부 Access 앱 컨트롤을 사용 하 여 실시간으로 위반 및 누출을 중단 합니다.
ms.openlocfilehash: d8370b1e02866db8f92ab7f6a46b06ddc3ed1055
ms.sourcegitcommit: 866d8cab6bcfdd124516a8369e47ec797bc7cf8a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/27/2019
ms.locfileid: "30312105"
---
# <a name="protect-apps-with-office-365-cloud-app-security-conditional-access-app-control"></a>Office 365 Cloud App Security 조건부 액세스 앱 컨트롤을 사용하여 앱 보호

|계산 * *\>**|계획 * *\>**|배포 * *\>**|사용률 * * * *|
|:-----|:-----|:-----|:-----|
|[평가 시작](office-365-cas-overview.md) <br/> |[계획 시작](get-ready-for-office-365-cas.md) <br/> |사용자가 여기 있어!  <br/> [다음 단계](ocas-deploy-conditional-access-app-control.md) <br/> |[활용 시작](utilization-activities-for-ocas.md) <br/> |

요즘에는 클라우드 환경에서 발생 하는 작업을 파악 하는 데 충분 하지 않은 경우가 많습니다. 직원 들이 고의적으로 또는 실수로 데이터와 조직을 위험에 노출 하기 전까지 실시간으로 침해 및 누출을 중단 하려는 경우 조직의 사용자가 클라우드 앱에서 사용 가능한 서비스와 도구를 대부분 사용할 수 있도록 설정 하 고 자체 장치를 사용 하도록 허용 하는 것이 중요 합니다. 동시에 조직에서 데이터 누출 및 데이터 절도를 실시간으로 보호 하는 데 도움이 되는 도구가 필요 합니다. Azure Active Directory와 함께 Office 365 Cloud App Security에서는 조건부 액세스 앱 컨트롤을 사용 하 여 전체적이 고 통합 된 환경에서 이러한 기능을 제공 합니다.

> [!IMPORTANT]
> Cloud app Security 조건부 Access 앱 컨트롤을 사용 하려면 [Azure active Directory P1 라이선스](https://azure.microsoft.com/pricing/details/active-directory/) 및 활성 [Office 365 Cloud App Security](office-365-cas-overview.md) 구독이 필요 합니다.

## <a name="how-it-works"></a>작업 방법

조건부 액세스 앱 컨트롤은 역방향 프록시 아키텍처를 사용 하며 Azure AD 조건부 액세스와 고유 하 게 통합 됩니다. Azure AD 조건부 액세스를 사용 하면 특정 조건에 따라 조직의 앱에 대 한 액세스 제어를 적용할 수 있습니다. 조건은 사용자 또는 ** 사용자 그룹을 정의 하 고, *어떤* 클라우드 앱 ** 을 지정 하 고, 조건부 액세스 정책을 적용할 위치와 네트워크를 지정 합니다. 조건을 확인 한 후 access 및 세션 제어를 적용 하 여 조건부 Access 앱 컨트롤을 사용 하 여 데이터를 보호할 수 있는 Office 365 Cloud App Security로 사용자를 라우팅할 수 있습니다.

조건부 액세스 앱 컨트롤을 사용 하면 access 및 세션 정책에 따라 실시간으로 사용자 앱 액세스와 세션을 모니터링 하 고 제어할 수 있습니다. 액세스 및 세션 정책은 Cloud App Security 포털에서 사용 되어 필터를 보다 구체화 하 고 사용자에 대해 수행할 작업을 설정 합니다. 액세스 및 세션 정책을 사용 하 여 다음을 수행할 수 있습니다.

- **다운로드 차단**: 중요 한 문서의 다운로드를 차단할 수 있습니다. 예를 들어 관리 되지 않는 장치

- **다운로드 시 보호**: 중요 한 문서 다운로드를 차단 하는 대신 다운로드 시 암호화를 통해 문서를 보호 해야 할 수 있습니다. 이 암호화를 사용 하면 데이터가 신뢰할 수 없는 장치로 다운로드 되는 경우 문서가 보호 되 고 사용자 액세스가 인증 됩니다.

- **낮은 신뢰 사용자 세션 모니터링**: 위험한 사용자가 앱에 로그인 할 때 모니터링 되 고 해당 작업이 세션 내에서 로그에 기록 되는 경우 나중에 세션 정책을 적용 해야 하는 위치를 이해 하기 위해 사용자 동작을 조사 하 고 분석할 수 있습니다.

- **차단 액세스**: 관리 되지 않는 장치 또는 회사 이외의 네트워크에서 들어오는 사용자에 대 한 특정 앱에 대 한 액세스를 완전히 차단할 수 있습니다.

- **읽기 전용 모드 만들기**: 사용자 지정 앱 내 활동을 모니터링 하 고 차단 하면 특정 사용자에 대 한 특정 앱에 대 한 읽기 전용 모드를 만들 수 있습니다.

- **비 회사 네트워크에서 사용자 세션 제한**: 회사 네트워크에 포함 되지 않은 위치에서 보호 된 앱에 액세스 하는 사용자는 제한 된 액세스를 허용 합니다. 중요 한 자료의 다운로드는 차단 되거나 보호 됩니다.

### <a name="how-session-control-works"></a>세션 제어 작동 방식

조건부 액세스 앱 컨트롤을 사용 하 여 세션 정책을 만들면 앱에 직접 연결 하는 대신 역방향 프록시를 통해 사용자 세션을 제어할 수 있습니다. 그런 다음, 사용자 요청 및 응답은 앱에 직접 실행 되는 것이 아니라 Office 365 Cloud App Security를 통해 진행 됩니다.

사용자를 세션 내에 유지 하기 위해 앱 세션 내의 모든 관련 url, Java 스크립트 및 쿠키가 Office 365 Cloud app Security url로 대체 됩니다. 예를 들어 앱이 myapp.com로 끝나는 링크가 있는 페이지를 반환 하는 경우 링크가 다음과 같이 끝나는 도메인으로 대체 됩니다.

이 방법에서는 장치에 아무것도 설치할 필요가 없습니다. 이 메서드는 관리 되지 않는 장치에서 세션을 모니터할 때 이상적입니다.

Office 365 Cloud App Security를 통해 세션이 전송 된 후에는 다음 작업을 수행할 수 있습니다.

1. 사용자 작업에 대 한 트래픽 조사

2. Office 365 Cloud App Security Activity log에서 식별 된 활동 표시

3. 트래픽 로그 저장 및 분석

4. 관리자가 트래픽 로그를 내보내도록 설정

5. 세션에 대 한 정책 적용

## <a name="managed-device-identification"></a>관리 되는 장치 식별

조건부 액세스 앱 컨트롤을 사용 하면 장치 관리 여부를 고려 하는 정책을 만들 수 있습니다. 장치가 관리 되는지 여부를 확인 하려면 다음 기능을 사용 합니다.

- 호환 되는 장치

- 도메인에 가입 된 장치

- 클라이언트 인증서 배포

### <a name="compliant-and-domain-joined-devices"></a>규격 및 도메인에 가입 된 장치

Azure AD 조건부 액세스를 사용 하면 호환 및 도메인에 가입 된 장치 정보를 Office 365 Cloud App Security로 직접 전달할 수 있습니다. 여기서는 장치 상태를 필터로 사용 하는 액세스 정책 또는 세션 정책을 개발할 수 있습니다. 자세한 내용은 [Azure Active Directory의 장치 관리 소개](https://docs.microsoft.com/azure/active-directory/device-management-introduction)를 참조 하세요.

### <a name="client-certificate-authenticated-devices"></a>클라이언트 인증서 인증 장치

장치 식별 메커니즘은 클라이언트 인증서를 사용 하 여 관련 디바이스에서 인증을 요청할 수 있습니다. 조직에 이미 배포 된 기존 클라이언트 인증서를 사용 하거나 관리 되는 장치에 새 클라이언트 인증서를 롤아웃할 수 있습니다. 그런 다음 이러한 인증서가 있는지 여부를 사용 하 여 액세스 및 세션 정책을 설정 합니다. 클라이언트 인증서를 배포 하는 방법에 대 한 자세한 내용은 [deploy 조건부 Access App Control for Office 365 apps](ocas-deploy-conditional-access-app-control.md)를 참조 하세요.

## <a name="supported-apps-and-clients"></a>지원 되는 앱 및 클라이언트

Office 365에 대 한 조건부 Access 앱 컨트롤은 다음과 같은 추천 앱을 지원 합니다.

- Exchange Online (미리 보기)

- 비즈니스용 OneDrive (미리 보기)

- Power BI (미리 보기)

- SharePoint Online (미리 보기)

- Microsoft 팀 (미리 보기)

- Yammer (미리 보기)

추가 앱이 계속 해 서 세션 제어에 boarded.

## <a name="next-steps"></a>다음 단계

- [Office 365 앱용 조건부 액세스 앱 컨트롤 배포](ocas-deploy-conditional-access-app-control.md)

- [Office 365 Cloud App Security의 세션 정책에 대해 자세히 알아보기](ocas-session-policies.md)

- [Office 365 Cloud App Security의 액세스 정책에 대해 자세히 알아보기](ocas-access-policies.md) 