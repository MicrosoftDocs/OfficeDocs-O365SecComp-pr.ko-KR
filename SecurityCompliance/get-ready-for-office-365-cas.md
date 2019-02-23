---
title: Office 365 Cloud App Security 시작
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.audience: ITPro
ms.topic: overview
ms.date: 02/15/2019
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: d9ee4d67-f2b3-42b4-9c9e-c4529904990a
description: Office 365 Cloud App Security를 사용 하 여 시작 하기
ms.openlocfilehash: d6049bb1a36a078c6e5e33c60928bd3ae872c33f
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30219898"
---
# <a name="get-ready-for-office-365-cloud-app-security"></a>Office 365 Cloud App Security 시작
  
|계산 * *\>**|계획 * *\>**|배포 * *\>**|사용률 * * * *|
|:-----|:-----|:-----|:-----|
|[평가 시작](office-365-cas-overview.md) <br/> |사용자가 여기 있어!  <br/> [다음 단계](turn-on-office-365-cas.md) <br/> |[배포 시작](turn-on-office-365-cas.md) <br/> |[활용 시작](utilization-activities-for-ocas.md) <br/> |
   
조직에 대 한 Office 365 Cloud App Security를 설정 하 고 구현할 때 몇 가지 사항을 고려해 야 합니다. 이 문서를 Office 365 Cloud App Security 계획에 대 한 지침으로 사용 하세요.
    
## <a name="step-1-identify-and-protect-your-global-and-security-administrator-accounts"></a>1 단계: 전역 및 보안 관리자 계정 식별 및 보호

전역 관리자, 보안 관리자 및 보안 독자는 Office 365 Cloud App security 포털에 액세스 하 여 정책을 보고, 경고를 검토 하 고, 보고서를 사용할 수 있습니다. 전역 관리자 및 보안 관리자는 정책을 정의 하 고 다른 작업을 수행 하 여 조직을 보호할 수 있습니다. 자세한 내용은 [Office 365 보안 &amp; 및 준수 센터의 사용 권한을](permissions-in-the-security-and-compliance-center.md)참조 하세요. 예방 조치로 향상 된 사용 권한을 가진 조직의 사용자 계정을 검토 합니다. 
  
 **[Office 365 전역 관리자 계정을 보호](https://docs.microsoft.com/office365/enterprise/protect-your-global-administrator-accounts)** 합니다. 
  
## <a name="step-2-turn-on-audit-logging-for-your-organization"></a>2 단계: 조직에 대 한 감사 로깅 설정

Office 365 Cloud App Security가 올바르게 작동 하려면 감사 로깅을 켜야 합니다. 이 작업은 일반적으로 Exchange Online 관리자 또는 전역 관리자가 수행 합니다.
  
 **[Office 365 감사 로그 검색을 설정 하거나 해제](turn-audit-log-search-on-or-off.md)** 합니다. 
  
## <a name="step-3-go-to-the-office-365-cloud-app-security-portal"></a>3 단계: Office 365 Cloud App Security 포털로 이동 합니다.

Office 365 Cloud App Security portal로 이동 [https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com) 하 여 로그인 해 볼 수 있습니다. 

Office 365 보안 &amp; 및 준수 센터에서 찾을 수도 있습니다. 이 작업을 수행 하는 좋은 방법은 다음과 같습니다.

1. [https://protection.office.com](https://protection.office.com) 으로 이동 하 여 로그인 합니다. (보안 &amp; 및 준수 센터로 이동 합니다.)
    
2. **경고** \> 로 이동 하 여 **고급 알림을 관리**합니다.
    
3. office **365 cloud app security로 이동을** 선택 하 여 office 365 cloud app security 포털로 이동 합니다.<br> ![Office 365 Cloud App Security로 이동 하려면 고급 알림 관리를 선택 합니다.](media/958632d4-03e3-4ade-8e22-d5509db6fca7.png)<br>Office 365 Cloud App Security 포털로 이동 하면 첫 번째로 표시 되는 페이지는 다음과 같은 이미지의 정책 페이지입니다.<br>![Office 365 Cloud App Security 포털로 이동 하면 정책 페이지부터 시작 합니다.](media/5cb8833c-4e08-438c-bab3-91b5106f6f3f.png)<br>
  
## <a name="step-4-define-policies-and-set-up-alerts-amp-actions"></a>4 단계: 정책 정의 및 알림 &amp; 작업 설정

전역 관리자 및 보안 관리자는 Office 365 Cloud App security에서 정책을 정의 합니다. 정책 정의 프로세스 중에는 알림 및 작업도 설정 됩니다. 알림은 보기에 표시 되거나 전자 메일을 통해 전송 되는 기준 기반 알림입니다. 
  
Office 365 Cloud App Security에는 두 가지 유형의 경고가 있으며, 의심 스러운 활동을 검색 하는 변칙 검색 알림과 조직의 이례적인 일이 될 수 있는 활동에 대해 정의 된 활동 경고가 있습니다. 경고는 조직에 익숙하지 않은 Office 365 환경에서 활동이 발생 하는 경우 전역 관리자 및 보안 관리자에 게 알립니다.
  
자세히 알아보려면 다음 리소스를 참조 하세요.
  
- [Office 365 Cloud App Security 활동 정책 및 알림](activity-policies-and-alerts.md)
    
- [Office 365 Cloud App Security 변칙 검색 정책](anomaly-detection-policies-in-ocas.md)
    
- [Office 365 Cloud App Security alerts에 대 한 검토 및 조치 수행](review-office-365-cas-alerts.md)
    

## <a name="step-5-set-up-conditional-access-app-control"></a>5 단계: 조건부 액세스 앱 컨트롤 설정

사용자가 어떤 앱을 사용할 수 있는지와 같은 특정 조건에 따라 조직의 앱에 컨트롤을 설정 하 고 적용 합니다. 사용자 앱 액세스 및 세션 정책을 정의 하 여 중요 한 문서를 다운로드 및 암호화할 수 있는지 여부를 결정 하 고, 특정 앱에 대 한 액세스를 차단 하 고, 특정 앱에 대 한 읽기 전용 모드를 설정 하 고, 회사 이외의 네트워크에서 사용자 세션을 제한 합니다.

자세히 알아보려면 다음 리소스를 참조 하세요.

- [Office 365 Cloud App Security 조건부 액세스 앱 컨트롤을 사용하여 앱 보호](ocas-conditional-access-app-control.md)

- [Office 365 앱용 조건부 액세스 앱 컨트롤 배포](ocas-deploy-conditional-access-app-control.md)

## <a name="step-6-learn-about-your-organizations-cloud-usage"></a>6 단계: 조직의 클라우드 사용에 대 한 자세한 정보

전역 관리자, 보안 관리자 또는 보안 독자는 보고서 및 클라우드 검색 대시보드 (생산성 앱 검색이 라고도 함)를 통해 조직의 클라우드 사용에 대 한 정보를 확인할 수 있습니다. 이 대시보드는 사용자, 앱, 웹 트래픽 및 위험 수준에 대 한 정보를 표시 합니다.
  
![Office 365 CAS 포털에서 클라우드 검색 대시보드 검색 \> 을 선택 합니다.](media/61269290-fd82-4d4b-8045-aea1ebc82287.png)
  
생산성 앱 검색 대시보드로 이동 하려면 Office 365 cloud App Security 포털에서 **클라우드 검색 대시보드** **검색** \> 을 선택 합니다.
  
![Office 365 CAS 포털에서 검색을 선택 합니다.](media/73b5299f-94b5-49dd-a00f-154d188eb2c5.png)
  
보고서를 필요한 정보로 채우려면 조직의 방화벽 및 프록시에서 로그 파일을 업로드 합니다. 자세한 내용은 다음 리소스를 참조 하십시오.
  
- [Office 365 Cloud app Security에서 앱 검색 보고서 만들기](create-app-discovery-reports-in-ocas.md)
    
- [Office 365 Cloud App Security을 사용하여 앱 검색 결과 검토](review-app-discovery-findings-in-ocas.md)
    
## <a name="step-7-manage-apps-that-your-organization-is-using-to-access-office-365"></a>7 단계: 조직에서 Office 365에 액세스 하는 데 사용 하는 앱 관리

전역 관리자 또는 보안 관리자로 서 조직의 사용자가 Office 365을 통해 장치에서 사용 하는 응용 프로그램, 타사 앱 등의 앱을 관리할 수 있습니다. 예를 들어 사용자가 Office 365에서 사용 하려는 사용자 지정 앱을 다운로드 했다고 가정 합니다. 사용자가 사용 중인 앱을 검토 하거나, 신뢰할 수 없는 앱을 차단 하거나, 추적 목적으로 앱을 승인 된 것으로 표시할 수 있습니다. [Office 365 Cloud App Security를 사용 하 여 OAuth 앱을 관리](manage-app-permissions-in-ocas.md)합니다.
  
## <a name="step-8-create-a-maintenance-plan"></a>8 단계: 유지 관리 계획 만들기

office 365 Cloud App Security를 설정 하 고 구성한 후에는 특정 사용률 작업을 조직의 Office 365 전역 관리자 또는 보안 관리자로 수행 하는 것이 좋습니다. 이러한 작업을 수행 하 여 office 365 Cloud App Security가 올바르게 구성 되어 있고, 정책이 최신 상태 이며, 조직에서 office 365의 가치를 인식 하도록 하는 데 도움이 됩니다. 이 문서를 참조 하 여 이러한 작업을 계획 하는 데 도움을 받을 수 있습니다. [Office 365 Cloud App Security를 시작한 후 사용률 작업](utilization-activities-for-ocas.md)을 참조 하세요.

## <a name="optional-step-9-use-your-siem-server-with-office-365-cloud-app-security"></a>반드시 9 단계: Office 365 Cloud App Security에서 siem 서버 사용

조직에서 siem (보안 정보 및 이벤트 관리) 서버를 사용 하 고 있나요? Office 365 Cloud App Security는 이제 siem server와 통합 하 여 경고에 대 한 중앙 집중식 모니터링을 사용할 수 있습니다. siem 서비스와 통합 하면 일반적인 보안 워크플로를 유지 관리 하면서 클라우드 응용 프로그램을 보다 효율적으로 보호 하 고, 클라우드 기반 및 온-프레미스 이벤트 간의 보안 절차를 자동화 하 고 상관 관계를 유지할 수 있습니다. siem 에이전트는 서버에서 실행 되며, Office 365 Cloud App Security의 알림을 가져오고, 해당 알림을 siem 서버로 스트리밍합니다. [siem integration과 Office 365 Cloud App Security를](integrate-your-siem-server-with-office-365-cas.md)참조 하세요.
  
## <a name="next-steps"></a>다음 단계

- [Office 365 Cloud App Security 켜기](turn-on-office-365-cas.md)
    
- Office 365 Cloud App Security의 강력한 기능을 시연 하 고 개념 증명을 만들 수 있는 실무 환경에 대 한 [테스트 랩 가이드](https://docs.microsoft.com/office365/enterprise/cloud-app-security-for-your-office-365-dev-test-environment) 를 사용해 보십시오. 
    

