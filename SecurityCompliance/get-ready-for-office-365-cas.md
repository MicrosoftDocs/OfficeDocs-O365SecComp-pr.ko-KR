---
title: Office 365 Cloud App Security 시작하기
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.audience: ITPro
ms.topic: overview
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: d9ee4d67-f2b3-42b4-9c9e-c4529904990a
description: Office 365 클라우드 응용 프로그램 보안을 사용 하 여 시작
ms.openlocfilehash: 906570c6607c70b63fa9d2059d56b50f7807124a
ms.sourcegitcommit: edf5db9357c0d34573f8cc406314525ef10d1eb9
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/28/2018
ms.locfileid: "23229990"
---
# <a name="get-ready-for-office-365-cloud-app-security"></a>Office 365 Cloud App Security 시작하기
  
|평가 * *\>**|계획 * *\>**|배포 * *\>**|사용률 * * *|
|:-----|:-----|:-----|:-----|
|[평가 시작 합니다.](office-365-cas-overview.md) <br/> |여기는!  <br/> [다음 단계](turn-on-office-365-cas.md) <br/> |[배포를 시작 합니다.](turn-on-office-365-cas.md) <br/> |[활용 하 여 시작](utilization-activities-for-ocas.md) <br/> |
   
설정 하 고 조직에 대 한 Office 365 클라우드 응용 프로그램 보안 (고급 보안 관리 이전의 함)를 구현 하려면 준비할 때는 다음과 같은 사항을 몇가지 사항을 고려 합니다. Office 365 클라우드 응용 프로그램 보안 계획 지침으로이 문서를 사용 합니다.
    
## <a name="step-1-identify-and-protect-your-global-and-security-administrator-accounts"></a>1 단계:를 식별 하 고 전역 및 보안 관리자 계정 보호

전역 관리자, 보안 관리자 및 보안 독자 정책을 보려면 경고를 검토 하 고 보고서를 사용 하 여를 Office 365 클라우드 응용 프로그램 보안 포털에 액세스할 수 있습니다. 전역 관리자 및 보안 관리자 정책을 정의 하 고 조직을 보호 하기 위한 다른 작업을 수행할 수 있습니다. (자세한 내용은 참조 [Office 365 보안에 대 한 사용 권한을 &amp; 준수 센터](permissions-in-the-security-and-compliance-center.md).) 더 높은 권한이 예방 조치로 조직의 사용자 계정을 검토 합니다. 
  
 **[암호로 보호 Office 365 전역 관리자 계정](https://docs.microsoft.com/office365/enterprise/protect-your-global-administrator-accounts)** 입니다. 
  
## <a name="step-2-turn-on-audit-logging-for-your-organization"></a>2 단계: 조직에 대해 감사 로깅을 설정합니다

올바른 작동 하도록 Office 365 클라우드 응용 프로그램 보안에 대 한 순서로 감사 로깅을 설정 해야 합니다. 이 Exchange Online 관리자 또는 전역 관리자가 일반적으로 수행 됩니다.
  
 **[Office 365 설정 또는 해제 로그 검색 감사](turn-audit-log-search-on-or-off.md)** 합니다. 
  
## <a name="step-3-go-to-the-office-365-cloud-app-security-portal"></a>3 단계: 포털로 이동 하는 Office 365 클라우드 응용 프로그램 보안

1. 이동 [https://protection.office.com](https://protection.office.com) 및 Office 365에 대 한 작업이 나 교육용 계정을 사용 하 여 로그인 합니다. (이렇게 하면 보안 &amp; 준수 센터.) 
    
2. **경고** 로 이동 \> **관리 고급 알림**입니다.
    
3. **Office 365 클라우드 앱 보안으로 이동** 하 여 Office 365 클라우드 응용 프로그램 보안 포털에 이동 하려면 선택 합니다. 
    
    ![보안에서 &amp; 준수 센터 Office 365 클라우드 앱 보안으로 이동 하려면 고급 알림 관리를 선택 합니다.](media/958632d4-03e3-4ade-8e22-d5509db6fca7.png)
  
    Office 365 클라우드 응용 프로그램 보안 포털에 이동할 때 표시 첫 페이지는 다음 이미지와 비슷합니다 정책 페이지의:
    
    ![정책 페이지로 시작 하 여 Office 365 클라우드 응용 프로그램 보안 포털에 이동할 때](media/5cb8833c-4e08-438c-bab3-91b5106f6f3f.png)
  
## <a name="step-4-define-policies-and-set-up-alerts-amp-actions"></a>4 단계: 정책을 정의 하 고 알림을 설정할 &amp; 작업

전역 관리자 및 보안 관리자가 Office 365 클라우드 응용 프로그램 보안에서 정책을 정의 합니다. 정책 정의 하는 과정 알림 및 작업은도 함께 설정 합니다. 알림을 보기에 표시 또는 전자 메일을 통해 전송 되는 조건 기반 알림입니다. 
  
Office 365 클라우드 응용 프로그램 보안에 대 한 알림 메시지에 두가지 유형이: 의심 스러운 활동을 검색 하는 예외 감지 경고 및 조직에 대 한 예외적인 될 수 있는 작업에 대해 정의 되는 활동 경고 합니다. 알림 조직에 대 한 일반적인 하지 않은 Office 365 환경에서 활동 때 전역 관리자 및 보안 관리자를 알립니다.
  
자세한 내용은 다음 리소스를 참조 하십시오.
  
- [Office 365 Cloud App Security 활동 정책 및 알림](activity-policies-and-alerts.md)
    
- [Office 365 Cloud App Security 변칙 검색 정책](anomaly-detection-policies-in-ocas.md)
    
- [검토 하 고 Office 365 클라우드 응용 프로그램 보안 경고에서 작업 수행](review-office-365-cas-alerts.md)
    
## <a name="step-5-learn-about-your-organizations-cloud-usage"></a>5 단계: 조직의 클라우드 사용 현황에 대 한 설명

전역 관리자, 보안 관리자 또는 보안 판독기, 보고서 및 (생산성 응용 프로그램 검색 라고도 함) 클라우드 검색 대시보드를 통해 조직의 클라우드 사용 하는 방법을 배울 수 있습니다. 이 대시보드는 사용자, 앱, 웹 트래픽 및 위험 수준에 대 한 정보를 표시 합니다.
  
![Office 365 CAS 포털에서 검색을 선택 \> 클라우드 검색 대시보드](media/61269290-fd82-4d4b-8045-aea1ebc82287.png)
  
Office 365 클라우드 응용 프로그램 보안 포털에서 생산성 응용 프로그램 검색 대시보드를 이동 하려면 **검색** 선택 \> **클라우드 검색 대시보드**합니다.
  
![Office 365 CAS 포털에서 검색을 선택](media/73b5299f-94b5-49dd-a00f-154d188eb2c5.png)
  
필요한 정보를 사용 하 여 보고서를 채우려면 조직의 방화벽 및 프록시에서 로그 파일을 업로드 합니다. 자세한 내용은 다음 리소스를 참조 합니다.
  
- [Office 365 클라우드 앱 보안에서 app 검색 보고서 만들기](create-app-discovery-reports-in-ocas.md)
    
- [Office 365 Cloud App Security을 사용하여 앱 검색 결과 검토](review-app-discovery-findings-in-ocas.md)
    
## <a name="step-6-manage-apps-that-your-organization-is-using-to-access-office-365"></a>조직에서 Office 365 액세스를 사용 하는 앱을 관리 하는 6 단계:

전역 관리자 또는 보안 관리자, 예: 사용자 지정 응용 프로그램 또는 Office 365를 통해 장치에 조직에서 사용자를 사용 하는 타사 응용 프로그램, 응용 프로그램을 관리할 수 있습니다. 예, Office 365와 함께 사용 하 여 원하는 사용자 지정 앱을 다운로드 한가 다른 사용자 경우를 가정해 보겠습니다. 사용자를 사용 하는 앱을 검토 하, 신뢰할 수 없는 앱을 금지 하거나을 추적 목적에 대 한 승인 앱을 표시할 수 있습니다. [Office 365 클라우드 응용 프로그램 보안을 사용 하는 응용 프로그램 사용 권한을 관리](manage-app-permissions-in-ocas.md)합니다.
  
## <a name="step-7-use-your-siem-server-with-office-365-cloud-app-security"></a>7 단계: SIEM 서버를 사용 하 여 Office 365 클라우드 응용 프로그램 보안

보안 정보 및 이벤트 관리 (SIEM) 서버를 사용 하 여 조직의? Office 365 클라우드 앱 보안 이제 알림 중앙 집중화 된 모니터링을 활성화 하려면 SIEM 서버와 통합할 수 있습니다. SIEM 서비스와 통합 하면 아주 좋음, 일반적인 보안 워크플로 유지 관리 하 고, 보안 절차를 자동화 하 고, 클라우드 기반 간의 상호 연관 시키는 하면서 클라우드 응용 프로그램을 보호 하기 위해 수 있으며 온-프레미스 이벤트입니다. 메뉴 및 도구 모음을 SIEM 에이전트 서버에서 실행 Office 365 클라우드 응용 프로그램 보안에서 알림을 가져오는 SIEM 서버에 이러한 알림을 스트리밍합니다. [Office 365 클라우드 응용 프로그램 보안 SIEM 통합](integrate-your-siem-server-with-office-365-cas.md)을 참조 하십시오.
  
## <a name="next-steps"></a>다음 단계

- [Office 365 Cloud App Security 켜기](turn-on-office-365-cas.md)
    
- Office 365 클라우드 응용 프로그램 보안의 강력한 기능을 설명 하 고 기술적 개념 증명을 만들 수 있는 실습 환경에 대 한 [테스트 랩 가이드](https://docs.microsoft.com/office365/enterprise/cloud-app-security-for-your-office-365-dev-test-environment) 를 시도 합니다. 
    

