---
title: Office 365 Cloud App Security와 SIEM 서버 통합
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: dd6d2417-49c4-4de6-9294-67fdabbf8532
description: siem server를 Office 365 Cloud App Security와 통합할 수 있습니다. 이 문서를 읽으면 작동 방식 및 설정 방법에 대 한 개요를 볼 수 있습니다.
ms.openlocfilehash: 82b5e0e6467bd42acba3c40d67e4e0363a7e0f72
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32254788"
---
# <a name="integrate-your-siem-server-with-office-365-cloud-app-security"></a>Office 365 Cloud App Security와 SIEM 서버 통합
  
|계산 * *\>**|계획 * *\>**|배포 * *\>**|사용률 * * * *|
|:-----|:-----|:-----|:-----|
|[평가 시작](office-365-cas-overview.md) <br/> |[계획 시작](get-ready-for-office-365-cas.md) <br/> |사용자가 여기 있어!  <br/> [다음 단계](utilization-activities-for-ocas.md) <br/> |[활용 시작](utilization-activities-for-ocas.md) <br/> |
   
## <a name="overview-and-prerequisites"></a>개요 및 필수 구성 요소

[Office 365 Cloud App security](get-ready-for-office-365-cas.md) 을 siem (보안 정보 및 이벤트 관리) 서버와 통합 하 여 중앙 집중식 경고 모니터링을 사용 하도록 설정할 수 있습니다. 이는 클라우드 서비스 및 온-프레미스 서버 응용 프로그램을 사용 하는 조직에 특히 유용 합니다. siem 서버를 통합 하 여 Office 365 Cloud App Security의 알림 및 활동을 siem 서버로 가져올 수 있습니다. siem server와의 통합을 통해 보안 팀은 일반적인 보안 절차를 자동화 하 고 클라우드 기반 및 온-프레미스 이벤트 간의 상관 관계를 자동으로 유지 하 여 Office 365 응용 프로그램을 보다 효율적으로 보호할 수 있습니다.  
  
siem server를 Office 365 Cloud App Security와 처음 통합 하면 지난 2 일의 알림이 siem 서버에 전달 되 고, 선택한 모든 필터를 기반으로 하는 모든 경고가 전송 됩니다. 또한 연장 된 기간에 대해이 기능을 사용 하지 않도록 설정 하면 다시 사용 하도록 설정할 때 이전의 두 날의 알림을 전달 하 고 이후의 모든 경고를 전송 합니다.

### <a name="siem-integration-architecture"></a>siem 통합 아키텍처

siem 에이전트는 조직의 네트워크에 설정 됩니다. siem 에이전트는 배포 및 구성 된 경우 Office 365 Cloud App Security RESTful api를 사용 하 여 구성 된 (경고) 데이터 형식을 가져옵니다. 그런 다음 포트 443에서 암호화 된 HTTPS 채널을 통해 트래픽을 전송 합니다.
  
siem 에이전트가 Office 365 Cloud App Security에서 데이터를 검색 하는 경우 설치 중에 제공 되는 네트워크 구성 (TCP 또는 사용자 지정 포트를 사용 하 여 UDP)을 사용 하 여 로컬 siem 서버에 Syslog 메시지를 보냅니다.

![siem 및 Cloud App Security 아키텍처](media/siem-architecture.png)

### <a name="supported-siem-servers"></a>지원 되는 siem 서버

Office 365 Cloud App Security에서는 현재 다음과 같은 siem 서버를 지원 합니다.
- 마이크로 포커스 arcsight
- 일반 cef

### <a name="prerequisites"></a>필수 구성 요소

- 이 문서에서 설명 하는 작업을 수행 하려면 전역 관리자 또는 보안 관리자 여야 합니다. [Office 365 보안 &amp; 및 준수 센터의 사용 권한](permissions-in-the-security-and-compliance-center.md) 보기

- 조직에 대해 [Office 365 Cloud App Security가 사용 하도록 설정](turn-on-office-365-cas.md) 되어 있어야 합니다.

- Office 365에 대해 [감사 로깅을](turn-audit-log-search-on-or-off.md) 켜야 함

- siem 서버 통합을 구성 하기 위해 다음 요구 사항을 충족 하는 표준 서버가 있어야 합니다.
    - OS: Windows 또는 Linux (가상 컴퓨터 일 수 있음)
    - CPU: 2
    - 디스크 공간: 20gb
    - RAM: 2gb
    - [Oracle Java 8](http://www.oracle.com/technetwork/java/javase/downloads/index.html) 설치
    - [네트워크 요구 사항](https://docs.microsoft.com/cloud-app-security/network-requirements) 에 설명 된 대로 방화벽이 구성 됨

- **원격 syslog 호스트** 및 **syslot 포트 번호**에 대 한 세부 정보가 있어야 합니다. 네트워크 관리자 또는 보안 관리자는 해당 정보를 찾는 데 도움을 드릴 수 있어야 합니다. 

- siem 서버를 통합 하는 데 필요한 [JAR 파일](https://go.microsoft.com/fwlink/?linkid=838596) 을 다운로드 하려면 [소프트웨어 사용 조건](https://go.microsoft.com/fwlink/?linkid=862491) 에 동의 해야 합니다.
 
## <a name="step-1-set-it-up-a-siem-agent-in-office-365-cloud-app-security"></a>1 단계: Office 365 Cloud App Security에서 siem 에이전트로 설정

1. Cloud App Security portal ([https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com))로 이동 하 여 로그인 합니다.
  
2. **설정** \> **보안 확장**을 클릭 한 다음 siem 에이전트를 선택 합니다.<br/>
![설정 > 보안 확장을 선택 합니다.](media/Settings-SecurityExtensions.png)

3. **siem 에이전트 추가**를 선택 합니다.<br/>![siem 에이전트 추가를 선택 합니다.](media/SIEMAgents.png)
    
4. **마법사 시작**을 선택 합니다.<br/>![도움말 보기 또는 마법사 시작](media/HelpOrWizard.png) 
    
5. **일반** 단계에서 이름을 지정 하 고 **siem 형식을 선택한** 다음 해당 형식과 관련 된 **고급 설정을** 설정 합니다. 다음을 **** 선택 합니다.<br/>![이름 및 유형 지정](media/ChooseAgentTypeAndName.png)
    
6. **원격 syslog** 단계에서 **원격 syslog 호스트** 의 IP 주소 또는 호스트 이름 및 **Syslog 포트 번호**를 지정 합니다. 원격 Syslog 프로토콜로 TCP 또는 UDP를 선택 합니다. (사용자가 없는 경우 네트워크 관리자 또는 보안 관리자와 함께 작업 하 여 이러한 세부 정보를 얻을 수 있습니다.) 다음을 **** 선택 합니다.<br/>![원격 Syslog 세부 정보 지정](media/ArcSightS1Syslog.png)
  
7. **데이터 형식** 단계에서 다음 중 하나를 수행한 후 **Next (다음**)를 클릭 합니다.
    - **모든 알림의** 기본 설정 유지<br/>또는
    - **모든 경고**를 클릭 한 다음 **특정 필터**를 선택 합니다. siem 서버에 보낼 알림 종류를 선택 하는 필터를 정의 합니다.
<br/>![마법사의 데이터 형식 단계](media/ArcSightS1ExportOptions.png)
  
8. 축 하 합니다 화면에서 토큰을 복사 하 고 나중에 저장 합니다.<br/>![siem 에이전트 만들어짐 화면](media/SIEMAgentFinished.png) 

> [!IMPORTANT]
> 이제 Office 365 Cloud App Security에서 siem 에이전트를 설정 했지만 siem server 통합은 아직 완료 되지 않았습니다. 다음 단계로 이동 하 여 siem server 통합을 계속 합니다.

닫기를 클릭 하 고 마법사를 종료 한 후에는 보안 확장 화면에서 테이블에 추가한 siem 에이전트를 볼 수 있습니다. 나중에 연결 될 때까지 **만들어진** 상태가 표시 됩니다.

![siem 에이전트를 만들었습니다.](media/SIEMAgentCreated.png)
    
## <a name="step-2-download-a-jar-file-and-run-it-on-your-siem-server"></a>2 단계: siem 서버에서 JAR 파일 다운로드 및 실행

1. [Microsoft Cloud App Security siem 에이전트](https://go.microsoft.com/fwlink/?linkid=838596) 를 다운로드 하 고 폴더의 압축을 풉니다. (계속 하려면 [소프트웨어 사용권 조항](https://go.microsoft.com/fwlink/?linkid=862491) 에 동의 해야 합니다.) 
    
2. 압축 폴더에서 .jar 파일을 추출 하 여 siem 서버에서 실행 합니다.
    
3. 파일을 실행 한 후 다음 명령을 실행 합니다.<br/>
  ```
  java -jar mcas-siemagent-0.87.20-signed.jar [--logsDirectory DIRNAME] [--proxy ADDRESS[:PORT]] --token TOKEN
  ```
### <a name="important-notes"></a>중요 참고 사항

- 파일 이름은 siem 에이전트 버전에 따라 다를 수 있습니다. 

- 서버 설치 중에 siem 서버에서 JAR 파일을 실행 하는 것이 좋습니다.

    - **Windows**: 예약 된 작업으로 실행 하 고, **사용자의 로그온 여부에 관계 없이 실행** 되도록 작업을 구성 하 고, 작업이 다음 **보다 오래 실행 되 면 중지** 옵션의 선택을 취소 합니다.

    - **Linux**: **&** `rc.local` 파일에 with를 사용 하 여 run 명령을 추가 합니다. <br/>예제:<br/> 
    ```
    java -jar mcas-siemagent-0.87.20-signed.jar [--logsDirectory DIRNAME] [--proxy ADDRESS[:PORT]] --token TOKEN &
    ```

- 대괄호의 매개 변수는 선택 사항이 며 관련성이 있는 경우에만 사용 해야 합니다. 다음 변수를 사용 합니다.

    - **tname** 은 로컬 에이전트 디버그 로그에 사용 하려는 디렉터리의 경로입니다.

    - **ADDRESS [:P ort]** 는 서버에서 인터넷에 연결 하는 데 사용 하는 프록시 서버 주소 및 포트입니다.

    - **TOKEN** 은 첫 번째 절차에서 복사한 siem 에이전트 토큰입니다.

    - 도움말을 보려면를 입력 `-h`합니다. 
  
## <a name="step-3-validate-that-the-siem-agent-is-working"></a>3 단계: siem 에이전트가 작동 하는지 확인

1. Office 365 Cloud App Security 포털의 siem 에이전트 상태가 **연결 오류** 또는 **연결이 끊어져** 표시 되지 않으며 에이전트 알림이 없음을 확인 합니다.<br/>예를 들어 다음과 같이 siem server가 연결 된 것을 볼 수 있습니다.<br/>![siem 서버 연결 됨](media/siem-connected.png)<br/>여기서는 siem server의 연결이 끊어져 있는 것을 볼 수 있습니다.<br/>![siem 서버가 연결 되지 않음](media/siem-not-connected.png) 
  
2. Syslog/siem server에서는 Office 365 Cloud App Security에서 알림이 수신 되었음을 확인 합니다.
  
## <a name="what-the-logfiles-look-like"></a>로그 파일이 어떤 모습 인지 확인

다음은 siem 서버로 전송 될 수 있는 경고 로그 파일 예입니다.

```
2017-07-15T20:42:30.531Z CEF:0|MCAS|SIEM_Agent|0.102.17|ALERT_CABINET_EVENT_MATCH_AUDIT|myPolicy|3|externalId=596a7e360c204203a335a3fb start=1500151350531 end=1500151350531 msg=Activity policy ''myPolicy'' was triggered by ''admin@box-contoso.com'' suser=admin@box-contoso.com destinationServiceName=Box cn1Label=riskScore cn1= cs1Label=portalURL cs1=https://cloud-app-security.com/#/alerts/596a7e360c204203a335a3fb cs2Label=uniqueServiceAppIds cs2=APPID_BOX cs3Label=relatedAudits cs3=1500151288183_acc891bf-33e1-424b-a021-0d4370789660 cs4Label=policyIDs cs4=59f0ab82f797fa0681e9b1c7

2017-07-16T09:36:26.550Z CEF:0|MCAS|SIEM_Agent|0.102.17|ALERT_CABINET_EVENT_MATCH_AUDIT|test-activity-policy|3|externalId=596b339b0c204203a33a51ae start=1500197786550 end=1500197786550 msg=Activity policy ''test-activity-policy'' was triggered by ''user@contoso.com'' suser=user@contoso.com destinationServiceName=Salesforce cn1Label=riskScore cn1= cs1Label=portalURL cs1=https://cloud-app-security.com/#/alerts/596b339b0c204203a33a51ae cs2Label=uniqueServiceAppIds cs2=APPID_SALESFORCE cs3Label=relatedAudits cs3=1500197720691_b7f6317c-b8de-476a-bc8f-dfa570e00349 cs4Label=policyIDs cs4=

2017-07-16T09:17:03.361Z CEF:0|MCAS|SIEM_Agent|0.102.17|ALERT_CABINET_EVENT_MATCH_AUDIT|test-activity-policy3|3|externalId=596b2fd70c204203a33a3eeb start=1500196623361 end=1500196623361 msg=Activity policy ''test-activity-policy3'' was triggered by ''admin@contoso.com'' suser=admin@contoso.com destinationServiceName=Office 365 cn1Label=riskScore cn1= cs1Label=portalURL cs1=https://cloud-app-security.com/#/alerts/596b2fd70c204203a33a3eeb cs2Label=uniqueServiceAppIds cs2=APPID_O365 cs3Label=relatedAudits cs3=1500196549157_a0e01f8a-e29a-43ae-8599-783c1c11597d cs4Label=policyIDs cs4=

2017-07-16T09:17:15.426Z CEF:0|MCAS|SIEM_Agent|0.102.17|ALERT_CABINET_EVENT_MATCH_AUDIT|test-activity-policy|3|externalId=596b2fd70c204203a33a3eec start=1500196635426 end=1500196635426 msg=Activity policy ''test-activity-policy'' was triggered by ''admin@contoso.com'' suser=admin@contoso.com destinationServiceName=Microsoft Office 365 admin center cn1Label=riskScore cn1= cs1Label=portalURL cs1=https://cloud-app-security.com/#/alerts/596b2fd70c204203a33a3eec cs2Label=uniqueServiceAppIds cs2=APPID_O365_PORTAL cs3Label=relatedAudits cs3=1500196557398_3e102b20-d9fa-4f66-b550-8c7a403bb4d8 cs4Label=policyIDs cs4=59f0ab35f797fa9811e9b1c7

2017-07-16T09:17:46.290Z CEF:0|MCAS|SIEM_Agent|0.102.17|ALERT_CABINET_EVENT_MATCH_AUDIT|test-activity-policy4|3|externalId=596b30200c204203a33a4765 start=1500196666290 end=1500196666290 msg=Activity policy ''test-activity-policy4'' was triggered by ''admin@contoso.com'' suser=admin@contoso.com destinationServiceName=Microsoft Exchange Online cn1Label=riskScore cn1= cs1Label=portalURL cs1=https://cloud-app-security.com/#/alerts/596b30200c204203a33a4765 cs2Label=uniqueServiceAppIds cs2=APPID_OUTLOOK cs3Label=relatedAudits cs3=1500196587034_a8673602-7e95-46d6-a1fe-c156c4709c5d cs4Label=policyIDs cs4=

2017-07-16T09:41:04.369Z CEF:0|MCAS|SIEM_Agent|0.102.17|ALERT_CABINET_EVENT_MATCH_AUDIT|test-activity-policy2|3|externalId=596b34b10c204203a33a5240 start=1500198064369 end=1500198064369 msg=Activity policy ''test-activity-policy2'' was triggered by ''user2@test15-adallom.com'' suser=user2@test15-adallom.com destinationServiceName=Google cn1Label=riskScore cn1= cs1Label=portalURL cs1=https://cloud-app-security.com/#/alerts/596b34b10c204203a33a5240 cs2Label=uniqueServiceAppIds cs2=APPID_33626 cs3Label=relatedAudits cs3=1500197996117_fd71f265-1e46-4f04-b372-2e32ec874cd3 cs4Label=policyIDs cs4=
```

다음은 cef 형식에서이에 해당 하는 다른 샘플입니다.


|cef 필드 이름  | 설명  |
|---------|---------|
|우선     | 경고 타임 스탬프        |
|끝나야     | 경고 타임 스탬프        |
|rt     | 경고 타임 스탬프        |
|.msg     | Office 365 Cloud App Security 포털에 표시 되는 경고 설명        |
|suser     | 알림 주체 사용자        |
|destinationservicename     | Office 365, SharePoint 또는 OneDrive와 같은 시작 응용 프로그램 알림        |
|cslabel     | 다양 한 의미를 갖는 레이블로 변경 합니다. 일반적으로 레이블은 targetobjects와 같은 설명이 필요 하지 않습니다.        |
|진단     | 레이블에 해당 하는 정보 (예: 레이블 예제에 대 한 경고의 대상 사용자)        |

## <a name="additional-tasks-as-needed"></a>추가 작업 (필요한 경우)

siem 서버를 구성 하 고 Office 365 Cloud App Security과 통합 한 후에는 토큰을 다시 생성 하거나, siem 에이전트를 편집 하거나, siem 에이전트를 삭제 해야 할 수 있습니다. 다음 섹션에서는 이러한 작업을 수행 하는 방법에 대해 설명 합니다.

### <a name="regenerate-a-token"></a>토큰 다시 생성

토큰을 분실 한 경우 다시 생성할 수 있습니다. 

1. Office 365[https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com)Cloud App Security portal ()에서 **설정** > **보안 확장**을 선택 합니다.

2. 표에서 siem 에이전트에 대 한 행을 찾습니다. 

3. 줄임표를 클릭 한 다음 **토큰 다시 생성**을 선택 합니다.<br/>![siem 에이전트에 대 한 줄임표를 클릭 하 여 토큰 다시 생성](media/04de368a-b88e-4a9c-a830-58025cb98db6.png)
  
### <a name="edit-a-siem-agent"></a>siem 에이전트 편집

1. Office 365[https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com)Cloud App Security portal ()에서 **설정** > **보안 확장**을 선택 합니다.

2. siem 에이전트에 대 한 행을 찾습니다. 

3. 줄임표를 클릭 한 다음 **편집**을 선택 합니다. siem 에이전트를 편집 하는 경우에는 .jar 파일을 다시 실행할 필요가 없으며 자동으로 업데이트 됩니다. <br/>![siem 에이전트를 편집 하려면 줄임표를 선택 하 고 편집을 선택 합니다.](media/96d0b362-3e0c-4dff-b2b4-d7af5b1bfb91.png)
  
### <a name="delete-a-siem-agent"></a>siem 에이전트 삭제

1. Office 365[https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com)Cloud App Security portal ()에서 **설정** > **보안 확장**을 선택 합니다.

2. siem 에이전트에 대 한 행을 찾습니다. 

3. 줄임표를 클릭 한 다음 **삭제**를 선택 합니다.<br/>![siem 에이전트를 삭제 하려면 줄임표를 선택한 다음 삭제를 선택 합니다.](media/540b5bdf-5574-4ecc-a7b0-92a499a387d7.png)

  
## <a name="next-steps"></a>다음 단계

- [Office 365 Cloud App Security 적용한 후 사용률 활동](utilization-activities-for-ocas.md)
    
- [경고 검토 및 알림 작업 수행](review-office-365-cas-alerts.md)
    
- [관리를 간소화 하는 IP 주소 그룹화](group-your-ip-addresses-in-ocas.md)
    

