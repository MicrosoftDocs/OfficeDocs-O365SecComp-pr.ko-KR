---
title: Office 365 Cloud App Security의 새로운 사항
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.audience: Admin
ms.topic: reference
ms.date: 01/25/2019
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
description: Office 365 Cloud App Security에서 2018 중 릴리스된 항목을 참조 하세요.
ms.openlocfilehash: 986fb64eedf8184e7835d1fec41845fde13b294b
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32263172"
---
# <a name="office-365-cloud-app-security-updates-during-2018"></a>2018 중 Office 365 Cloud App Security 업데이트

## <a name="office-365-cloud-app-security-release-138"></a>Office 365 Cloud App Security release 138

*2018 년 12 월 23 일*

**다음 [Microsoft Cloud App Security release 138](https://docs.microsoft.com/cloud-app-security/release-notes#cloud-app-security-release-138)**:

- **Windows에서 Docker를 사용 하 여 자동 로그 업로드** Cloud App Security에서는 이제 windows에 Docker를 사용 하 여 windows 10 ([낙하 작성자 업데이트](https://docs.microsoft.com/windows/whats-new/whats-new-windows-10-version-1709) 이상) 및 windows Server ([버전 1709](https://docs.microsoft.com/windows-server/get-started/whats-new-in-windows-server-1709) 이상)에 대 한 자동 로그 업로드를 지원 합니다. 자세한 내용과 Docker 구성을 보려면 [이 문서](https://docs.microsoft.com/cloud-app-security/discovery-docker-windows) 를 참조 하세요.  

- **Microsoft Flow 통합** 이제 Cloud App Security은 [Microsoft 흐름과](https://docs.microsoft.com/flow/getting-started) 통합 되어 사용자 지정 경고 자동화 및 오케스트레이션 playbooks 제공 합니다. Microsoft Flow 통합에 대해 자세히 알아보고 구성 하려면 [이 문서](https://docs.microsoft.com/cloud-app-security/flow-integration) 를 참조 하세요. 

## <a name="office-365-cloud-app-security-release-137"></a>Office 365 Cloud App Security release 137

*출시 되는 2018 년 12 월 8 일*

**다음 [Microsoft Cloud App Security release 137](https://docs.microsoft.com/cloud-app-security/release-notes#cloud-app-security-release-137)**:

- **Dynamics에 대 한 지원이 추가 되었습니다** . Cloud App Security에는 이제 Office 365 감사 로그에서 지원 되는 Microsoft Dynamics 작업에 대 한 지원이 포함 됩니다. 

- **새 용어를 준비 합니다.** 앱 사용 권한 기능의 이름이 명확 하 게 변경 되었으며 이제는 OAuth 앱 이라고 합니다. 

## <a name="office-365-cloud-app-security-release-136"></a>Office 365 Cloud App Security release 136

*2018 년 11 월 25 일 출시*

**다음 [Microsoft Cloud App Security release 136](https://docs.microsoft.com/cloud-app-security/release-notes#cloud-app-security-release-136)**:

- **클라우드 검색 업데이트** 추가 및 보다 복잡 한 웹 트래픽 로그 형식을 지원 하기 위해 사용자 지정 로그 파서가 향상 되었습니다. 이러한 향상 된 기능을 통해 사용자는 이제 headerless CSV 로그 파일에 대 한 사용자 지정 헤더를 입력 하 고, 키-값 파일, 프로세스 Syslog 파일 형식 등에 대해 특수 구분 기호를 사용할 수 있습니다.

- **새 변칙 검색 정책: 의심 스러운 받은 편지함 조작 규칙** 이 정책은 사용자의 받은 편지함에 메시지나 폴더를 삭제 하거나 이동 하는 의심 스러운 규칙이 설정 된 경우 환경에 프로 파일을 만들고 경고를 트리거합니다. 이는 사용자의 계정이 손상 되었음을 나타내거나, 메시지를 의도적으로 숨김 중 이며, 사서함이 조직에 스팸 또는 맬웨어를 배포 하는 데 사용 되 고 있음을 나타낼 수 있습니다.

- **앱 권한 정책의 그룹 지원** 이제 Cloud app Security에서는 앱 권한을 부여한 사용자의 그룹 멤버 자격을 기반으로 앱 권한 정책을 보다 granularly 정의 하는 기능을 제공 합니다. 예를 들어 관리자는 권한을 권한이 부여 된 사용자가 administrators 그룹의 구성원 인 경우에만 사용 권한이 높은 앱을 해지 하는 정책을 설정할 수 있습니다.

## <a name="office-365-cloud-app-security-releases-133-134-and-135"></a>Office 365 Cloud App Security 릴리스 133, 134 및 135

*2018 년 10 월에 릴리스*

** [Microsoft Cloud App Security release 133, 134 및 135에](https://docs.microsoft.com/cloud-app-security/release-notes#cloud-app-security-release-133-134-135)따라 다음**이 수행 됩니다.

- **새로운 변칙 검색 정책이** 점차적으로 롤아웃 됩니다.
    
    - 사용자 또는 IP 주소가 될 때 경고 아닌 앱을 사용 하 여 조직에서 정보를 exfiltrate 하는 것과 유사한 작업을 수행 하는 경우 **unsanctioned 앱에 대 한 새 데이터 exfiltration** 이 자동으로 사용 하도록 설정 됩니다.
    
    - 새 **다중 delete VM 활동** 정책은 환경에 프로필을 만들고 사용자가 조직의 기준을 기준으로 단일 세션에서 여러 vm을 삭제할 때 경고를 트리거합니다.

- **i 필터에 대 한 클라우드 검색 지원** 이제 Cloud App Security Cloud Discovery 기능을 통해 i 필터 syslog 파서에서 향상 된 지원을 받을 수 있습니다.

## <a name="office-365-cloud-app-security-release-131"></a>Office 365 Cloud App Security release 131

*2018 년 9 월 16 일 출시*

**다음 [Microsoft Cloud App Security release 131](https://docs.microsoft.com/cloud-app-security/release-notes#cloud-app-security-release-131)**:

- **위험한 OAuth 앱에 대 한 사용 권한 자동 해지** 이제 Office의 oauth 앱에 대 한 앱 권한을 해지 하 여 사용자에 게 액세스 권한이 있는 oauth 앱을 제어할 수 있습니다. 앱 사용 권한 정책을 만들 때 이제 앱의 권한을 해지 하도록 정책을 설정할 수 있습니다.

- **클라우드 검색 지원 되는 추가 기본 제공 파서** 이제 클라우드 검색에서 forcepoint Web Security 클라우드 로그 형식을 지원 합니다.
  
## <a name="office-365-cloud-app-security-release-130"></a>Office 365 Cloud App Security release 130

*2018 년 9 월 5 일 출시*

**다음 [Microsoft Cloud App Security release 130](https://docs.microsoft.com/cloud-app-security/release-notes#cloud-app-security-release-130)**:

- **새 메뉴 모음** microsoft 365 제품에서 보다 일관성 있는 관리 환경을 제공 하 고 microsoft 보안 솔루션을 보다 쉽게 피벗할 수 있도록 하기 위해 Cloud App security portal 메뉴 표시줄이 화면 왼쪽으로 이동 되었습니다. 이러한 일관적인 탐색 환경을 통해 Microsoft 보안 포털 간에 이동할 때 직접 방향을 설정할 수 있습니다.<br/>![Office Cloud App Security의 메뉴 모음](media/OCAS-MenuBar.png)<br/>

- **영향 OAuth 앱 점수** 이제 클라우드 앱 보안 팀의 의견을 보내 악의적인 앱이 악성에 게 보이는 것으로 확인 된 경우이를 알 수 있습니다. 이 새로운 기능을 사용 하면 보안 커뮤니티의 일부로 서 OAuth 앱 위험 점수 및 분석을 향상 시킬 수 있습니다. 자세한 내용은 [OAuth 앱 관리](manage-app-permissions-in-ocas.md)를 참조 하세요.

- **새 클라우드 검색 파서** 이제 클라우드 검색 파서가 iboss 보안 클라우드 게이트웨이 및 Sophos xg를 지원 합니다.

## <a name="office-365-cloud-app-security-release-128"></a>Office 365 Cloud App Security release 128

*출시 2018 년 8 월 5 일* 
  
**다음 [Microsoft Cloud App Security release 128](https://docs.microsoft.com/cloud-app-security/release-notes#cloud-app-security-release-128)**: 
  
- **여러 앱에 걸친 OAuth 앱** OAuth 앱의 경우 이제 단일 작업으로 여러 앱을 금지 하거나 승인할 수 있습니다. 예를 들어 조직의 사용자가 사용 권한을 부여 받은 모든 앱을 검토 하 고, 금지 하려는 모든 앱을 선택 하 고, 앱 금지를 클릭 하 여 사용자가 해당 앱에 대 한 사용 권한을 더 이상 부여 하지 못하게 할 수 있습니다. 자세한 내용은 [Office 365 Cloud App Security를 사용 하 여 OAuth 앱 관리](manage-app-permissions-in-ocas.md)를 참조 하세요. 
    
- **새 제안 된 쿼리: gdpr-ready 클라우드 앱** 사용 가능한 검색 된 앱을 식별 하는 데 사용할 수 있는 새로운 추천 쿼리가 제공 됩니다. 이미 알고 있는 것 처럼, gdpr은 최근에 보안 관리자의 우선 순위를 얻었습니다. 이 쿼리는 gdpr이 준비 된 앱을 쉽게 식별 하 고, 앱이 아닌 응용 프로그램의 위험을 평가 하 여 위협을 완화 하는 데 도움이 됩니다. 새 쿼리를 사용 하려면 **클라우드 검색** 대시보드의 **검색 된 앱** 탭에서**gdpr ready 클라우드 앱** **쿼리** > 를 선택 합니다.<br/>![gdpr-ready 클라우드 앱 쿼리](media/OCAS-FindGDPRQueries.png)<br/>
    
## <a name="office-365-cloud-app-security-release-126"></a>Office 365 Cloud App Security release 126

*2018 년 7 월 7 일 출시* 
  
**다음 [Microsoft Cloud App Security release 126](https://docs.microsoft.com/cloud-app-security/release-notes#cloud-app-security-release-126)**: 
  
- **의심 스러운 활동에 대 한 자동화 된 재구성** 이제 변칙 검색 정책에 의해 트리거되는 의심 스러운 세션에 대 한 자동 재구성 작업을 설정할 수 있습니다. 이 향상 된 기능을 사용 하면 위반이 발생 하는 경우 즉시 알림을 받을 수 있으며 사용자 일시 중단과 같은 거 버 넌 스 작업을 자동으로 적용할 수도 있습니다. 자세한 내용은 [Office 365 Cloud App Security의 변칙 검색 정책](anomaly-detection-policies-in-ocas.md)를 참조 하세요.
    
- **위험한 OAuth 앱의 자동 검색** 현재 환경에 연결 된 oauth 앱에 대 한 기존 조사 외에도, Office 365 Cloud app Security에서는 OAuth 앱이 특정 조건을 충족 하는 경우를 알려 주는 자동 알림을 설정할 수 있습니다. 예를 들어 높은 권한 수준이 필요한 앱이 있고, 50 명 이상의 사용자가 인증을 받아야 하는 경우 자동으로 알림을 받을 수 있습니다. 자세한 내용은 [Office 365 Cloud App Security를 사용 하 여 OAuth 앱 관리](manage-app-permissions-in-ocas.md)를 참조 하세요.
    
- **관리 되는 mssp (보안 서비스 공급자 관리) 지원** office 365 cloud app security는 이제 mssps에 보다 효율적인 관리 환경을 제공 하며, 외부 파트너는 현재 Office 365 Cloud App Security에서 사용할 수 있는 모든 역할을 가진 관리자로 구성할 수 있습니다. 또한 두 개 이상의 테 넌 트에 대 한 액세스 권한이 있는 관리자는 이제 테 넌 트에서 서로 쉽게 피벗할 수 있습니다. 
    
## <a name="office-365-cloud-app-security-release-124"></a>Office 365 Cloud App Security release 124

*2018 년 6 월 10 일 출시* 
  
**다음 [Microsoft Cloud App Security release 124](https://docs.microsoft.com/cloud-app-security/release-notes#cloud-app-security-release-124)**: 
  
- **범위 배포** 엔터프라이즈 조직은 그룹 구성원을 기반으로 모니터링 하 고 보호할 사용자를 granularly 결정할 수 있습니다. 이 기능을 사용 하면 보호 된 응용 프로그램에 대해 활동을 표시 하지 않을 사용자를 선택할 수 있습니다. 범위 지정 모니터링은 특히 준수 및 라이선스에 유용 합니다. 일부 규정 준수 규정에 따라 지역 규정으로 인 한 특정 국가에서 사용자를 모니터링 하는 것이 필요할 수 있습니다. 또한 Office 365 Cloud App Security 라이선스의 범위 내에서 유지 되도록 할 사용자 수를 줄일 수 있습니다. 
    
- **새 전자 메일 서버** Office 365 용 전자 메일 서버 보안 Cloud App Security가 변경 되었으며 다른 IP 주소 범위를 사용 합니다. 알림을 받을 수 있는지 확인 하려면 스팸 방지 허용 목록에 새 IP 주소를 추가 합니다. 알림을 사용자 지정 하는 조직의 경우 Cloud App Security에서는 MailChimp, 타사 전자 메일 서비스를 사용 하 여이를 사용할 수 있습니다. 메일 서버 IP 주소 목록 및 MailChimp에서 작업을 사용 하도록 설정 하는 방법에 대 한 지침은 [네트워크 요구 사항 (microsoft cloud app security)](https://docs.microsoft.com/cloud-app-security/network-requirements) 및 [mail settings (microsoft cloud app security)](https://docs.microsoft.com/cloud-app-security/mail-settings)을 참조 하십시오.
    
## <a name="office-365-cloud-app-security-release-121"></a>Office 365 Cloud App Security release 121

*출시 5 월 6 일 2018* 
  
**다음 [Microsoft Cloud App Security release 121](https://docs.microsoft.com/cloud-app-security/release-notes#cloud-app-security-release-121)**: 
  
- **변칙 검색 정책 개선** Office 365 Cloud App Security의 변칙 검색 정책에는 점진적으로 롤아웃 되는 두 가지 새로운 유형의 위협 검색을 포함 하도록 개선 되었습니다. 
    
  - **랜 섬 웨어 활동** 랜 섬 웨어 감지 기능은 변칙 검색 기능을 사용 하 여 복잡 한 랜 섬 웨어 공격에 대 한 보다 포괄적인 범위를 제공 합니다. 
    
  - **사용자 작업이 종료 되었습니다.** 종료 된 사용자 활동을 사용 하면 회사 응용 프로그램에서 프로 비전 해제 되었지만 특정 회사 리소스에 계속 액세스할 수 있는 종료 한 사용자의 계정을 모니터링할 수 있습니다. 
    
    [변칙 검색 정책을](anomaly-detection-policies-in-ocas.md)보려면 Office 365 Cloud App Security 포털에서 **제어** \> **정책을**선택 합니다.
    
## <a name="office-365-cloud-app-security-release-120"></a>Office 365 Cloud App Security release 120

*2018 년 4 월 22 일 출시* 
  
**다음 [Microsoft Cloud App Security release 120](https://docs.microsoft.com/cloud-app-security/release-notes#cloud-app-security-release-120)**: 
  
- **사용자 활동으로 사용 되는 내부 응용 프로그램** office 365 및 azure ad (Active Directory)의 경우 office 365 및 azure ad 응용 프로그램 (내부 및 외부 모두)에서 수행 하는 사용자 계정 활동으로 내부 응용 프로그램을 검색 하는 기능을 점차적으로 배포 하 고 있습니다. 이를 통해 응용 프로그램에서 예기치 않은 작업을 수행 하는 경우 경고를 알리는 정책을 만들 수 있습니다. 
    
- **OAuth 앱 목록 내보내기에서 추가 필드가**있습니다. OAuth 앱 목록을 csv로 내보낼 때, 게시자, 사용 권한 수준 및 커뮤니티 사용과 같은 추가 필드는 준수 및 조사 프로세스를 지원 하기 위해 포함 됩니다. 
    
## <a name="office-365-cloud-app-security-release-119"></a>Office 365 Cloud App Security release 119

*2018 년 4 월 1 일 출시* 
  
**다음 [Microsoft Cloud App Security release 119](https://docs.microsoft.com/cloud-app-security/release-notes#cloud-app-security-release-119)**: 
  
- **클라우드 검색 향상** 클라우드 검색에서는 상위 사용자 및 IP 주소에 대 한 자세한 정보를 제공 하므로 Office 365 및 기타 앱에 대 한 사용 현황 세부 정보를 보다 쉽게 확인할 수 있습니다. 자세한 내용은 [Office 365 Cloud app Security에서 앱 검색 결과 검토](review-app-discovery-findings-in-ocas.md)를 참조 하세요.
    
    ![클라우드 검색 대시보드가 업데이트 되었습니다.](media/12712681-c0b3-4cb3-b7fd-2cf2ad4e825f.png)
  
## <a name="office-365-cloud-app-security-release-118"></a>Office 365 Cloud App Security release 118

*2018 년 3 월 18 일 출시* 
  
**다음 [Microsoft Cloud App Security release 118](https://docs.microsoft.com/cloud-app-security/release-notes#cloud-app-security-release-118)**: 
  
- **Barracuda 지원** 이제 클라우드 검색에서는 Barracuda f 시리즈 방화벽과 Barracuda f 시리즈 방화벽 웹 로그 스트리밍을 지원 합니다. 
    
## <a name="office-365-cloud-app-security-release-117"></a>Office 365 Cloud App Security release 117

*2018 년 3 월 6 일* 
  
**다음 [Microsoft Cloud App Security release 117](https://docs.microsoft.com/cloud-app-security/release-notes#cloud-app-security-release-117)**: 
  
- **i 필터 지원**. 이제 클라우드 검색에서 i 필터를 지원 합니다. 
    
## <a name="office-365-cloud-app-security-release-116"></a>Office 365 Cloud App Security release 116

*2018 년 2 월 18 일 출시* 
  
**다음 [Microsoft Cloud App Security release 116](https://docs.microsoft.com/cloud-app-security/release-notes#cloud-app-security-release-116)**: 
  
- **변칙 검색 정책 향상** Office 365의 변칙 검색 정책 클라우드 앱 보안은 불가능 한 여행, 의심 스러운 IP 주소에서의 활동 및 여러 번 로그인 시도가 실패 한 새로운 시나리오 기반 검색을 통해 향상 되었습니다. 클라우드 환경에서 기본 위협 감지 기능을 제공 하는 새 정책이 자동으로 사용 하도록 설정 됩니다. 또한 새 정책은 Office 365 Cloud App Security detection engine에서 더 많은 데이터를 제공 하므로 조사 프로세스의 속도를 향상 시키고 진행 중인 위협을 포함할 수 있습니다. 자세한 내용은 Microsoft Cloud App Security 문서, [순간 행동 분석 및 변칙 검색](https://docs.microsoft.com/cloud-app-security/anomaly-detection-policy)을 참조 하세요.
    
- **검사점 형식에 대 한 로그 파서 지원** 이제 클라우드 검색 로그 파서는 두 개의 추가 검사점 형식인 XML 및 kpc를 지원 합니다. 
    
## <a name="office-365-cloud-app-security-release-114"></a>Office 365 Cloud App Security release 114

*출시 되는 2018 년 1 월 21 일* 
  
**다음 [Microsoft Cloud App Security release 114](https://docs.microsoft.com/cloud-app-security/release-notes#cloud-app-security-release-114)**: 
  
- **서비스 상태** 이제 **도움말** \> **시스템 상태**를 확인 하 여 현재 Office 365 Cloud App Security 서비스 상태를 확인할 수 있습니다. 
    
    ![\> 시스템 상태 확인을 클릭 하 여 시스템 상태 보기](media/2b496dac-ed9d-4480-83b6-85f9510d3aea.png)
  
- **활동 로그에 대 한 사용자 지정 쿼리** 버전 114 부터는 활동 로그에 사용자 지정 쿼리를 만들고 저장 하는 기능이 점진적으로 롤아웃 됩니다. 사용자 지정 쿼리를 사용 하면 심층 조사를 위해 다시 사용할 수 있는 필터 서식 파일을 만들 수도 있습니다. 또한 권장 되는 쿼리가 추가 되어 활동과 검색 된 앱을 필터링 하는 기본 조사 템플릿을 제공 합니다. 제안 되는 쿼리에는 가장 작업, 관리자 활동, 위험한 비트랜잭션 클라우드 저장소 앱, 취약 한 암호화의 엔터프라이즈 앱, 보안 위험 등의 위험을 식별 하는 사용자 지정 필터를 포함 합니다. 제안 된 쿼리를 시작 점으로 사용 하 고 필요에 따라 수정한 다음 새 쿼리로 저장 합니다. 
    
## <a name="office-365-cloud-app-security-release-113"></a>Office 365 Cloud App Security release 113

*출시 되는 2018 년 1 월 8 일* 
  
**다음 [Microsoft Cloud App Security release 113](https://docs.microsoft.com/cloud-app-security/release-notes#cloud-app-security-release-113)**: 
  
- **제네릭 형식에 대 한 로그 파서 지원** 이제 클라우드 검색 로그 파서가 다음과 같은 제네릭 형식인 leef, cef 및 W3C를 지원 합니다. 

## <a name="related-topics"></a>관련 항목

[Office 365 Cloud App Security의 새로운 사항](new-in-office-365-cas.md)

[Office 365 Cloud App Security 용 2017 업데이트를 참조 하세요.](new-in-office-365-cas-2017.md)
    
[Office 365 Cloud App Security 적용한 후 사용률 활동](utilization-activities-for-ocas.md)