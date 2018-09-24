---
title: Office 365 Cloud App Security와 SIEM 서버 통합
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: dd6d2417-49c4-4de6-9294-67fdabbf8532
description: Office 365 클라우드 앱 보안이 포함 된 SIEM 서버를 통합할 수 있습니다. 작동 방식 및를 설정 하는 방법에 대 한 개요를 얻으려면이 문서를 읽어보십시오.
ms.openlocfilehash: a2bd75e73ddccef9359ace304faa3c8b1dd4a728
ms.sourcegitcommit: 17c7e18d7d00135b1af40cbea117c9a817a41117
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/24/2018
ms.locfileid: "24972330"
---
# <a name="integrate-your-siem-server-with-office-365-cloud-app-security"></a>Office 365 Cloud App Security와 SIEM 서버 통합
  
|평가 * *\>**|계획 * *\>**|배포 * *\>**|사용률 * * *|
|:-----|:-----|:-----|:-----|
|[평가 시작 합니다.](office-365-cas-overview.md) <br/> |[계획을 시작합니다](get-ready-for-office-365-cas.md) <br/> |여기는!  <br/> [다음 단계](utilization-activities-for-ocas.md) <br/> |[활용 하 여 시작](utilization-activities-for-ocas.md) <br/> |
   
[Office 365 클라우드 앱 보안](get-ready-for-office-365-cas.md) 알림 중앙 집중화 된 모니터링을 활성화 하려면 보안 정보 및 이벤트 (SIEM) 관리 서버와 통합할 수 있습니다. 이것은 클라우드 서비스를 사용 하는 조직에 특히 유용 하 고 온-프레미스 서버 응용 프로그램입니다. SIEM 서버와 통합 보안 팀이 더 잘 특정 보안 절차를 자동화 하 고 클라우드 기반 간의 상호 연관 시키는 함으로써 일반적인 보안 워크플로 사용 하 여 유지 관리 하는 동안 Office 365 응용 프로그램을 보호할 수 있도록 온-프레미스 및 이벤트입니다.  
  
Office 365 클라우드 응용 프로그램 보안 SIEM 서버에 부합 먼저 때 마지막 2 일에서 알림은 전달 됩니다 모든 알림을 SIEM 서버를 다음에서에서 (선택한 필터 기준). 또한 오랫동안 때 클래스를 활성화 하면 다시이 기능을 해제 하는 경우 지난 2 일의 알림 및 모든 알림을 다음 그 보냅니다.
 
## <a name="siem-integration-architecture"></a>SIEM 통합 아키텍처

SIEM 에이전트 조직의 네트워크에 설정 됩니다. SIEM 에이전트 구성 된 데이터 형식 가져오는 배포 하 고 구성 하는 경우 Office 365 클라우드 앱 보안 RESTful Api를 사용 하 여 (경고). 트래픽이 포트 443에서 암호화 된 HTTPS 채널을 통해 전송 됩니다.
  
Office 365 클라우드 응용 프로그램 보안에서 데이터를 검색 하는 SIEM 에이전트를 하는 경우 (TCP 또는 사용자 지정 포트와 UDP) 설치 하는 동안 제공 되는 네트워크 구성을 사용 하 여 로컬 SIEM 서버 Syslog 메시지를 보냅니다.

![SIEM 및 클라우드 응용 프로그램 보안 아키텍처](media/siem-architecture.png)

## <a name="supported-siem-servers"></a>지원 되는 SIEM 서버

Office 365 클라우드 앱 보안 현재 다음 SIEM 서버를 지원합니다.
- 마이크로 포커스 ArcSight
- 일반 CEF

## <a name="prerequisites"></a>필수 구성 요소

- 이 문서에서 설명 하는 작업을 수행 하려면 전역 관리자 또는 보안 관리자 여야 합니다. 참조 [Office 365 보안에 대 한 사용 권한을 &amp; 준수 센터](permissions-in-the-security-and-compliance-center.md)

- 조직에 대 한 [Office 365 클라우드 앱 보안 사용 하도록 설정](turn-on-office-365-cas.md) 되어 있어야 합니다.

- [감사 로깅](turn-audit-log-search-on-or-off.md) 설정 해야 Office 365에 대 한

- SIEM 서버 통합을 구성 하려면 다음 요구 사항을 충족 하는 표준 서버가 있어야 합니다.
    - 운영 체제: Windows 또는 Linux (가상 컴퓨터 될 수 있음)
    - CPU: 2
    - 디스크 공간: 20GB
    - RAM: 2GB
    - [Oracle Java 8](http://www.oracle.com/technetwork/java/javase/downloads/index.html) 설치
    - [네트워크 요구 사항](https://docs.microsoft.com/cloud-app-security/network-requirements) 에서 설명한 대로 구성 하는 방화벽

- **원격 syslog 호스트** 및 **포트 번호 Syslot**하는 방법에 대 한 자세한 내용은 있어야 합니다. 보안 관리자나 네트워크 관리자에 게 해당 정보를 찾을 수 있도록 수 있어야 합니다. 

- [파일을 병](https://go.microsoft.com/fwlink/?linkid=838596) SIEM 서버에 통합 하는데 필요한을 다운로드 하려면 [소프트웨어 사용 조건](https://go.microsoft.com/fwlink/?linkid=862491) 에 동의 해야 합니다.
 
## <a name="integrate-office-365-cloud-app-security"></a>Office 365 클라우드 앱 보안 통합
    
### <a name="step-1-set-it-up-in-the-office-365-cloud-app-security-portal"></a>1 단계: Office 365 클라우드 응용 프로그램 보안 포털에서 설정

1. 이동 [https://protection.office.com](https://protection.office.com) 및 Office 365에 대 한 작업이 나 교육용 계정을 사용 하 여 로그인 합니다. (이렇게 하면 보안 &amp; 준수 센터.) 
    
2. **경고** 로 이동 \> **관리 고급 알림**입니다.
    
3. **Office 365 클라우드 응용 프로그램 보안으로 이동**을 선택 합니다.<br/>
    ![보안에서 &amp; 준수 센터 Office 365 클라우드 앱 보안으로 이동 하려면 고급 알림 관리를 선택 합니다.](media/958632d4-03e3-4ade-8e22-d5509db6fca7.png)
  
4. **설정** 을 클릭 \> **보안 확장**합니다.<br/>
![설정을 선택 > 보안 확장](media/Settings-SecurityExtensions.png)

5. **추가 SIEM 에이전트**를 선택 합니다.<br/>![추가 SIEM 에이전트를 선택 합니다.](media/SIEMAgents.png)
    
6. **마법사를 시작**을 선택 합니다.<br/>![마법사를 시작 하거나 대 한 도움말 보기](media/HelpOrWizard.png) 
    
7. **일반** 단계에서 이름 및 **SIEM 형식 선택** 지정 하 고 모든 **고급 설정** 해당 형식에 관련 된 설정입니다. **다음**을 선택 합니다.<br/>![이름 및 유형 지정](media/ChooseAgentTypeAndName.png)
    
8. **원격 Syslog** 단계에서 IP 주소 또는 호스트 이름을 **원격 syslog 호스트** 및 **Syslog 포트 번호**를 지정 합니다. 원격 Syslog 프로토콜로 TCP 또는 UDP를 선택 합니다. (네트워크 관리자나 보안 관리자가 없는 경우 해당 하는 경우 이러한 세부 정보를 가져오는데 함께 작업할 수 있습니다.) **다음**을 선택 합니다.<br/>![원격 Syslog 세부 정보를 지정 합니다.](media/ArcSightS1Syslog.png)
  
9. **데이터 형식** 단계에서 다음 중 하나를 수행 하 고 **다음**을 클릭 합니다.
    - **모든** 알림 기본 설정을 유지합니다<br/>또는
    - **모든 알림**을 클릭 하 고 **특정 필터**를 선택 합니다. SIEM 서버에 보낼 알림의 종류를 선택 하는 필터를 정의 합니다.<br/>![마법사의 데이터 형식 단계](media/ArcSightS1ExportOptions.png)
  
10. 축 하 합니다. 화면에서 토큰을 복사 하 고 나중에 저장 합니다.<br/>![SIEM 만든 에이전트 화면](media/SIEMAgentFinished.png) 

> [!IMPORTANT]
> 이 시점 Office 365 클라우드 응용 프로그램 보안에서 SIEM 에이전트를 설정한 경우 SIEM 서버 통합이 아직 완료 되지 않음 SIEM 서버 통합을 계속 하려면 다음 단계를 진행 합니다.

닫기를 클릭 하 고 보안 확장 화면에는 마법사를 유지 한 후에 테이블에 추가 된 SIEM 에이전트를 볼 수 있습니다. 나중에 연결 될 때까지 **Created** 상태가 표시 됩니다.

![만든 SIEM 에이전트](media/SIEMAgentCreated.png)
    
### <a name="step-2-download-the-jar-file-and-run-it-on-your-server"></a>2 단계: JAR 파일을 다운로드 하 고 서버에서 실행

1. [Microsoft 클라우드 응용 프로그램 보안 SIEM 에이전트](https://go.microsoft.com/fwlink/?linkid=838596) 를 다운로드 하 고 폴더 압축을 풉니다. (동의 해야 [소프트웨어 사용 조건](https://go.microsoft.com/fwlink/?linkid=862491) 에 진행 하기 위해.) 
    
2. 압축 된 폴더에서.jar 파일을 추출 하 고 서버에서 실행 합니다.
    
3. 파일을 실행 한 후 다음을 실행: 명령 합니다.<br/>
  ```
  java -jar mcas-siemagent-0.87.20-signed.jar [--logsDirectory DIRNAME] [--proxy ADDRESS[:PORT]] --token TOKEN
  ```
#### <a name="important-notes"></a>중요 한 참고 사항

- 파일 이름 SIEM 에이전트의 버전에 따라 다를 수 있습니다. 

- 서버 설치 하는 동안 서버에서 JAR 채우기를 실행 하는 것이 좋습니다.
    - **Windows**: 실행 된 예약 된 작업을 하 고 작업을 **실행 하는 사용자의 로그온 여부** 를 구성 하 고 **기간 이상 실행 하는 경우 작업을 중지** 옵션의 선택을 취소 합니다.

    - **Linux**: 함께 실행된 명령을 추가 **&** 에 `rc.local` 파일입니다. <br/>예제:<br/> 
    ```
    java -jar mcas-siemagent-0.87.20-signed.jar [--logsDirectory DIRNAME] [--proxy ADDRESS[:PORT]] --token TOKEN &
    ```

- 대괄호는 선택적 매개 변수와 관련 된 경우에 사용 해야 합니다. 다음 변수를 사용 합니다.
    - **DIRNAME** 는 경로에 로컬 에이전트 디버그 로그를 사용 하려는 디렉터리입니다.
    - **주소 [: 포트]** 프록시 서버 주소와 인터넷에 연결 하는 서버를 사용 하는 포트입니다.
    - **토큰** 은 첫번째 절차에서 복사한 SIEM 에이전트 토큰입니다.
    - 도움말을 보려면 다음을 입력 `-h`합니다. 
  
### <a name="step-3-validate-that-the-siem-agent-is-working"></a>3 단계: SIEM 에이전트 작동 하는지 확인

1. Office 365 클라우드 응용 프로그램 보안 포털에서 SIEM 에이전트의 상태 **연결** 오류로 표시 되지 않거나는 없는 에이전트 알림 **Disconnected** 하 고 있는 있는지 확인 합니다.<br/>예, 여기는 볼 수 SIEM 서버가 연결 된:<br/>![연결 된 SIEM 서버](media/siem-connected.png)<br/>및는 여기에 SIEM 서버 연결이 끊어지면 볼 수 있습니다.<br/>![연결 되지 않은 SIEM 서버](media/siem-not-connected.png) 
  
2. 프로그램 Syslog/SIEM 서버에서 Office 365 클라우드 응용 프로그램 보안에서 알림 도착 하는 것이 표시 되는지 확인 합니다.
  
## <a name="regenerating-your-token"></a>사용자 토큰을 다시 생성

사용자 토큰을 분실 하면 항상 재생성 수 있습니다. 테이블에서 SIEM 에이전트에 대 한 행을 찾습니다. 있는 줄임표를 클릭 하 고 **토큰을 다시 생성**을 선택 합니다.

![SIEM 에이전트에 대 한 줄임표를 클릭 하 여 토큰을 다시 생성](media/04de368a-b88e-4a9c-a830-58025cb98db6.png)
  
## <a name="editing-your-siem-agent"></a>SIEM 에이전트를 편집합니다.

테이블에서 SIEM 에이전트를 편집 하려면 SIEM 에이전트에 대 한 행을 찾습니다. 있는 줄임표를 클릭 하 고 **편집**을 선택 합니다. .Jar 파일;를 다시 실행 하지 필요가 SIEM 에이전트를 편집 하는 경우 자동으로 업데이트합니다.

![SIEM 에이전트를 편집 하려면 타원을 선택한 다음 편집을 선택 합니다.](media/96d0b362-3e0c-4dff-b2b4-d7af5b1bfb91.png)
  
## <a name="deleting-your-siem-agent"></a>SIEM 에이전트를 삭제합니다.

테이블에서 SIEM 에이전트를 삭제 하려면 SIEM 에이전트에 대 한 행을 찾습니다. 있는 줄임표를 클릭 한 다음 **삭제**를 선택 합니다.

![SIEM 에이전트를 삭제 하려면 타원을 선택한 다음 삭제를 선택 합니다.](media/540b5bdf-5574-4ecc-a7b0-92a499a387d7.png)

## <a name="sample-logfiles"></a>샘플 로그 파일

SIEM 서버로 전송 될 수 있는 알림 로그 파일 예는 다음과 같습니다.

```
2017-07-15T20:42:30.531Z CEF:0|MCAS|SIEM_Agent|0.102.17|ALERT_CABINET_EVENT_MATCH_AUDIT|myPolicy|3|externalId=596a7e360c204203a335a3fb start=1500151350531 end=1500151350531 msg=Activity policy ''myPolicy'' was triggered by ''admin@box-contoso.com'' suser=admin@box-contoso.com destinationServiceName=Box cn1Label=riskScore cn1= cs1Label=portalURL cs1=https://cloud-app-security.com/#/alerts/596a7e360c204203a335a3fb cs2Label=uniqueServiceAppIds cs2=APPID_BOX cs3Label=relatedAudits cs3=1500151288183_acc891bf-33e1-424b-a021-0d4370789660 cs4Label=policyIDs cs4=59f0ab82f797fa0681e9b1c7

2017-07-16T09:36:26.550Z CEF:0|MCAS|SIEM_Agent|0.102.17|ALERT_CABINET_EVENT_MATCH_AUDIT|test-activity-policy|3|externalId=596b339b0c204203a33a51ae start=1500197786550 end=1500197786550 msg=Activity policy ''test-activity-policy'' was triggered by ''user@contoso.com'' suser=user@contoso.com destinationServiceName=Salesforce cn1Label=riskScore cn1= cs1Label=portalURL cs1=https://cloud-app-security.com/#/alerts/596b339b0c204203a33a51ae cs2Label=uniqueServiceAppIds cs2=APPID_SALESFORCE cs3Label=relatedAudits cs3=1500197720691_b7f6317c-b8de-476a-bc8f-dfa570e00349 cs4Label=policyIDs cs4=

2017-07-16T09:17:03.361Z CEF:0|MCAS|SIEM_Agent|0.102.17|ALERT_CABINET_EVENT_MATCH_AUDIT|test-activity-policy3|3|externalId=596b2fd70c204203a33a3eeb start=1500196623361 end=1500196623361 msg=Activity policy ''test-activity-policy3'' was triggered by ''admin@contoso.com'' suser=admin@contoso.com destinationServiceName=Office 365 cn1Label=riskScore cn1= cs1Label=portalURL cs1=https://cloud-app-security.com/#/alerts/596b2fd70c204203a33a3eeb cs2Label=uniqueServiceAppIds cs2=APPID_O365 cs3Label=relatedAudits cs3=1500196549157_a0e01f8a-e29a-43ae-8599-783c1c11597d cs4Label=policyIDs cs4=

2017-07-16T09:17:15.426Z CEF:0|MCAS|SIEM_Agent|0.102.17|ALERT_CABINET_EVENT_MATCH_AUDIT|test-activity-policy|3|externalId=596b2fd70c204203a33a3eec start=1500196635426 end=1500196635426 msg=Activity policy ''test-activity-policy'' was triggered by ''admin@contoso.com'' suser=admin@contoso.com destinationServiceName=Microsoft Office 365 admin center cn1Label=riskScore cn1= cs1Label=portalURL cs1=https://cloud-app-security.com/#/alerts/596b2fd70c204203a33a3eec cs2Label=uniqueServiceAppIds cs2=APPID_O365_PORTAL cs3Label=relatedAudits cs3=1500196557398_3e102b20-d9fa-4f66-b550-8c7a403bb4d8 cs4Label=policyIDs cs4=59f0ab35f797fa9811e9b1c7

2017-07-16T09:17:46.290Z CEF:0|MCAS|SIEM_Agent|0.102.17|ALERT_CABINET_EVENT_MATCH_AUDIT|test-activity-policy4|3|externalId=596b30200c204203a33a4765 start=1500196666290 end=1500196666290 msg=Activity policy ''test-activity-policy4'' was triggered by ''admin@contoso.com'' suser=admin@contoso.com destinationServiceName=Microsoft Exchange Online cn1Label=riskScore cn1= cs1Label=portalURL cs1=https://cloud-app-security.com/#/alerts/596b30200c204203a33a4765 cs2Label=uniqueServiceAppIds cs2=APPID_OUTLOOK cs3Label=relatedAudits cs3=1500196587034_a8673602-7e95-46d6-a1fe-c156c4709c5d cs4Label=policyIDs cs4=

2017-07-16T09:41:04.369Z CEF:0|MCAS|SIEM_Agent|0.102.17|ALERT_CABINET_EVENT_MATCH_AUDIT|test-activity-policy2|3|externalId=596b34b10c204203a33a5240 start=1500198064369 end=1500198064369 msg=Activity policy ''test-activity-policy2'' was triggered by ''user2@test15-adallom.com'' suser=user2@test15-adallom.com destinationServiceName=Google cn1Label=riskScore cn1= cs1Label=portalURL cs1=https://cloud-app-security.com/#/alerts/596b34b10c204203a33a5240 cs2Label=uniqueServiceAppIds cs2=APPID_33626 cs3Label=relatedAudits cs3=1500197996117_fd71f265-1e46-4f04-b372-2e32ec874cd3 cs4Label=policyIDs cs4=
```

다음은 샘플 CEF 형식 및


|CEF 필드 이름  | 설명  |
|---------|---------|
|시작     | 경고 타임 스탬프        |
|끝     | 경고 타임 스탬프        |
|rt     | 경고 타임 스탬프        |
|msg     | Office 365 클라우드 응용 프로그램 보안 포털에 표시 된 대로 설명 경으십시오        |
|suser     | 알림 제목 사용자        |
|destinationServiceName     | Office 365, SharePoint, 또는 OneDrive와 같은 응용 프로그램에서 들어오는 경고        |
|csLabel     | 다름 (레이블에 다음과 같은 의미). 일반적으로 레이블이 targetObjects 같은 쉽게 이해할 수 있습니다.        |
|cs     | 정보에 해당 하는 레이블 (예: 레이블 예제에 따라 알림의 대상 사용자)        |
  
## <a name="next-steps"></a>다음 단계

- [Office 365 Cloud App Security 적용한 후 사용률 활동](utilization-activities-for-ocas.md)
    
- [검토 및 알림 작업을 수행 합니다.](review-office-365-cas-alerts.md)
    
- [관리를 단순화 하 여 IP 주소를 그룹화](group-your-ip-addresses-in-ocas.md)
    

