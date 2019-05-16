---
title: Office 365 보안 로드맵-처음 30 일, 90 일 및 그 이상에 대 한 주요 우선 순위
ms.author: bcarter
author: BrendaCarter
manager: laurawi
ms.date: 10/08/2018
ms.audience: Admin
ms.topic: conceptual
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- Ent_O365
- Strat_O365_IP
- M365-security-compliance
search.appverid:
- MET150
ms.assetid: 28c86a1c-e4dd-4aad-a2a6-c768a21cb352
description: 'Office 365 환경을 보호 하기 위한 보안 기능을 구현 하기 위한 Microsoft의 cybersecurity 팀의 주요 권장 사항입니다. '
ms.openlocfilehash: d6ac885d2517a7933df52b34124654784012c677
ms.sourcegitcommit: 7be8617ce75909f0fa1a2f6e72749e2ef4bb2d3e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/16/2019
ms.locfileid: "34088821"
---
# <a name="office-365-security-roadmap---top-priorities-for-the-first-30-days-90-days-and-beyond"></a>Office 365 보안 로드맵-처음 30 일, 90 일 및 그 이상에 대 한 주요 우선 순위

이 문서에는 Office 365 환경을 보호 하기 위한 보안 기능을 구현 하기 위한 Microsoft의 cybersecurity 팀의 주요 권장 사항이 포함 되어 있습니다. 이 문서는 Microsoft Ignite session [, cybersecurity pro와 같은 보안 Office 365, 처음 30 일, 90 일 및 그 이상에 대 한 최고 우선 순위](https://www.youtube.com/watch?v=luignzNyR-o)를 통해 적용 됩니다. 이 세션은 Mark Simos 및 Matt Kemelhar, Enterprise Cybersecurity 설계자를 통해 개발 및 제시 되었습니다.
  
이 문서의 내용
  
- [로드맵 결과](security-roadmap.md#Roadmap)
    
- [30 일-빠른 신속한 wins](security-roadmap.md#Thirdaydays)
    
- [90 일-향상 된 보호](security-roadmap.md#Ninetydays)
    
- [많은](security-roadmap.md#Beyond)
    
## <a name="roadmap-outcomes"></a>로드맵 결과
<a name="Roadmap"> </a>

이러한 로드맵 권장 사항은 다음과 같은 목표에 따라 논리적 순서로 세 단계에 걸쳐 있습니다.

|||
|:-----|:-----|
| |결과
|30일|빠른 구성:  <br/> • 기본 관리자 보호  <br/> • 로깅 및 분석  <br/> • 기본 id 보호  <br/> 테 넌 트 구성  <br/>  관련자 준비  <br/> |
|90일|고급 보호:  <br/> • 관리자 계정  <br/>  • 데이터 &amp; 사용자 계정  <br/>  준수, 위협 및 사용자 요구에 대 한 가시성  <br/>  기본 정책 및 보호 적용 및 구현  <br/> |
|많은|주요 정책 및 제어 조정 및 구체화  <br/> 온-프레미스 종속성에 대 한 보호 확장  <br/> 비즈니스 및 보안 프로세스 (법적, 참가자 위협 등)와 통합  <br/> |
  

   
## <a name="30-days--powerful-quick-wins"></a>30 일-빠른 신속한 wins
<a name="Thirdaydays"> </a>

이러한 태스크는 빠르게 완료될 수 있으며 사용자에게 많은 영향을 미치지 않습니다.
  
|||
|:-----|:-----|
|영역  <br/> |작업  <br/> |
|보안 관리  <br/> |• 보안 점수를 확인 하 고 현재 점수를 기록해 둡니다 [https://securescore.office.com](https://securescore.office.com)().  <br/>  • Office 365에 대 한 감사 로깅을 설정 합니다. [감사 로그 검색을](search-the-audit-log-in-security-and-compliance.md)참조 하세요.  <br/> • [보안 강화를 위해 Office 365 테 넌 트를 구성](tenant-wide-setup-for-increased-security.md) 합니다.  <br/>  • Microsoft 365 보안 센터 및 Cloud App Security에서 대시보드 및 보고서를 정기적으로 검토 합니다.  <br/> |
|위협 방지  <br/> |[Office 365을 Microsoft Cloud App Security에 연결](https://docs.microsoft.com/cloud-app-security/connect-office-365-to-microsoft-cloud-app-security) 하 여 비정상 동작에 대 한 기본 위협 검색 정책을 사용 하 여 모니터링을 시작 합니다. 변칙 검색을 위한 기준을 작성 하는 데 7 일이 걸립니다.  <br><br/>  관리자 계정에 대 한 보호 구현:  <br/> • 관리 활동에 전용 관리자 계정을 사용 합니다.  <br/>  • 관리자 계정에 대해 MFA (multi-factor authentication)를 적용 합니다.  <br/>  • 관리 활동에 [높은 보안 Windows 10 장치](https://docs.microsoft.com/windows-hardware/design/device-experiences/oem-highly-secure) 를 사용 합니다.  <br/> |
|ID 및 액세스 관리  <br/> |• [Azure Active Directory Id 보호를 사용 하도록 설정](https://docs.microsoft.com/azure/active-directory/active-directory-identityprotection-enable)합니다.  <br/> • 페더레이션 id 환경의 경우 계정 보안 (암호 길이, 연령, 복잡도 등)을 적용 합니다.  <br/> |
|정보 보호  <br/> | 정보 보호 권장 사항 예를 검토 합니다. 정보 보호를 사용 하려면 조직 전체를 조정 해야 합니다. 다음 리소스를 사용해서 시작하세요.  <br/> • [GDPR에 대 한 Office 365 정보 보호](http://aka.ms/o365gdpr) <br/> • [SharePoint Online 사이트 및 파일 보호](https://docs.microsoft.com/Office365/enterprise/secure-sharepoint-online-sites-and-files) (공유, 분류, 데이터 손실 방지 및 Azure Information Protection 포함)  <br/> |
   
## <a name="90-days--enhanced-protections"></a>90 일-향상 된 보호
<a name="Ninetydays"> </a>

이러한 태스크는 계획하고 구현하는 데 다소 시간이 소요되지만 보안 태세를 갖추는 데 큰 도움이 됩니다. 
  
|||
|:-----|:-----|
|영역  <br/> |작업  <br/> |
|보안 관리  <br/> | • 환경에 대 한 권장 작업 ( [https://securescore.office.com](https://securescore.office.com))에 대 한 보안 점수를 확인 합니다.  <br/>  • Microsoft 365 보안 센터, Cloud App Security 및 SIEM 도구에서 대시보드 및 보고서를 정기적으로 계속 검토 합니다.  <br/>  • 소프트웨어 업데이트를 찾고 구현 합니다.  <br/>  • [Attack 시뮬레이터](https://support.office.com/article/attack-simulator-office-365-da5845db-c578-4a41-b2cb-5a09689a551b) ( [Office 365 위협 인텔리전스](office-365-ti.md)에 포함)를 사용 하 여 스피어-피싱, 암호-스프레이 및 무작위 암호 공격에 대 한 공격 시뮬레이션을 수행 합니다.  <br/>  • Cloud App Security의 기본 제공 보고서 (조사 탭)를 검토 하 여 공유 위험을 확인 합니다.  <br/>  • [준수 관리자](meet-data-protection-and-regulatory-reqs-using-microsoft-cloud.md) 를 확인 하 여 조직에 적용 되는 규정에 대 한 상태를 검토 합니다 (예: GDPR, NIST 800-171).  <br/> |
|위협 방지  <br/> | 관리자 계정에 대해 향상 된 보호를 구현 합니다.  <br/>  • 관리 활동에 대 한 PAWs ( [권한이 부여 된 액세스 워크스테이션](https://docs.microsoft.com/windows-server/identity/securing-privileged-access/privileged-access-workstations) )를 구성 합니다.  <br/>  • [AZURE AD 권한이 부여 된 Id 관리](https://docs.microsoft.com/azure/active-directory/active-directory-privileged-identity-management-configure)를 구성 합니다.  <br/>  • Office 365, Cloud App Security 및 AD FS를 비롯 한 기타 서비스에서 로깅 데이터를 수집 하도록 SIEM (보안 정보 및 이벤트 관리) 도구를 구성 합니다. Office 365 감사 로그에는 90 일 동안만 데이터가 저장 됩니다. SIEM 도구에서이 데이터를 캡처하면 더 긴 기간에 대 한 데이터를 저장할 수 있습니다.  <br/> |
|ID 및 액세스 관리  <br/> | • 모든 사용자에 대해 MFA를 사용 하도록 설정 하 고 적용 합니다.  <br/>  • [조건부 액세스 및 관련 정책](https://docs.microsoft.com/en-us/microsoft-365/enterprise/microsoft-365-policies-configurations)집합을 구현 합니다. |
|정보 보호  <br/> | 정보 보호 정책을 적용 하 고 구현 합니다. 이러한 리소스에는 다음 예가 포함 됩니다.  <br/> • [GDPR에 대 한 Office 365 정보 보호](http://aka.ms/o365gdpr) <br/> • [SharePoint Online 사이트 및 파일 보호](https://docs.microsoft.com/Office365/enterprise/secure-sharepoint-online-sites-and-files) <br/> <br> Cloud App Security 대신 Office 365에 저장 된 데이터에 대 한 Office 365의 데이터 손실 방지 정책 및 모니터링 도구를 사용 합니다. <br><br>데이터 손실 방지를 제외 하 고 고급 경고 기능을 위해 Cloud App Security with Office 365을 사용 합니다.  <br/> |
   
## <a name="beyond"></a>많은
<a name="Beyond"> </a>

다음은 이전 작업을 구성 하는 중요 한 보안 조치입니다. 
  
|||
|:-----|:-----|
|영역  <br/> |작업  <br/> |
|보안 관리  <br/> |• 보안 점수 ( [https://securescore.office.com](https://securescore.office.com))를 사용 하 여 다음 작업을 계속 계획 합니다.  <br/>  • Microsoft 365 보안 센터, Cloud App Security 및 SIEM 도구에서 대시보드 및 보고서를 정기적으로 계속 검토 합니다.  <br/>  • 계속 해 서 소프트웨어 업데이트를 찾고 구현 합니다.  <br/>  • EDiscovery를 법적 및 위협 대응 프로세스에 통합 합니다.  <br/> |
|위협 방지  <br/> | • 온-프레미스 (AD, AD FS)에서 id 구성 요소에 대 한 SPA ( [보안 액세스 권한](https://docs.microsoft.com/windows-server/identity/securing-privileged-access/securing-privileged-access) )를 구현 합니다.  <br/>  • Cloud App Security를 사용 하 여 참가자 위협을 모니터링 합니다.  <br/>  • Cloud App Security를 사용 하 여 섀도 IT SaaS 사용 현황을 알아봅니다.  <br/> |
|ID 및 액세스 관리  <br/> | • 정책 및 운영 프로세스를 구체화 합니다.  <br/>  • Azure AD Id 보호를 사용 하 여 참가자 위협을 식별 합니다.  |
|정보 보호  <br/> | 정보 보호 정책 구체화:  <br/>  • Microsoft 365 및 Office 365 민감도 레이블 및 DLP (데이터 손실 방지) 또는 Azure Information Protection  <br/>  • Cloud App Security 정책 및 알림  <br/> |
   
또한 [Petya 및 WannaCrypt 등의 신속한 고 사이버 공격을 완화 하는 방법을](https://cloudblogs.microsoft.com/microsoftsecure/2018/02/21/how-to-mitigate-rapid-cyberattacks-such-as-petya-and-wannacrypt/)참조 하세요. 
  

