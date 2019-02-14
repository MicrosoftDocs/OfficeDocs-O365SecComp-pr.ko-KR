---
title: Office 365 보안 로드맵-처음 30 일, 90 일 동안 및 이외 위쪽 우선순위
ms.author: bcarter
author: BrendaCarter
manager: laurawi
ms.date: 10/08/2018
ms.audience: Admin
ms.topic: conceptual
ms.service: o365-administration
localization_priority: Normal
ms.collection:
- Ent_O365
- Strat_O365_IP
- M365-security-compliance
search.appverid:
- MET150
ms.assetid: 28c86a1c-e4dd-4aad-a2a6-c768a21cb352
description: 'Office 365 환경을 보호 하기 위해 보안 기능을 구현 하기 위한 Microsoft의 cybersecurity 팀에서 위쪽 권장 합니다. '
ms.openlocfilehash: ce7b4371a284763c506ea4e1a06a63dbf2968ae5
ms.sourcegitcommit: efccf5b4f22d34a9674bc55ebf3d88bc8bda2972
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/14/2019
ms.locfileid: "29995289"
---
# <a name="office-365-security-roadmap---top-priorities-for-the-first-30-days-90-days-and-beyond"></a>Office 365 보안 로드맵-처음 30 일, 90 일 동안 및 이외 위쪽 우선순위

이 문서에는 Office 365 환경을 보호 하기 위해 보안 기능을 구현 하기 위한 Microsoft의 cybersecurity 팀에서 위쪽 권장 사항이 포함 됩니다. 이 문서는 Microsoft Ignite 세션에서 적용할- [전문가 cybersecurity와 같은 Office 365 보안: 처음 30 일, 90 일 동안 및 이외 우선순위 가지 주요](https://www.youtube.com/watch?v=luignzNyR-o)합니다. 이 세션을 개발 하 고 Mark Simos 및 Matt Kemelhar, 엔터프라이즈 Cybersecurity 설계자가 프레젠테이션한 합니다.
  
이 문서의 내용
  
- [로드맵 성과](security-roadmap.md#Roadmap)
    
- [30 일-강력한 빠른 wins](security-roadmap.md#Thirdaydays)
    
- [90 일-보호 기능이 향상](security-roadmap.md#Ninetydays)
    
- [기능 이외에](security-roadmap.md#Beyond)
    
## <a name="roadmap-outcomes"></a>로드맵 성과
<a name="Roadmap"> </a>

이러한 로드맵 권장 논리적 순서에 따라 다음과 같은 목표와 세 단계로 별 준비 됩니다.

|||
|:-----|:-----|
| |결과
|30일|신속 하 게 구성 합니다.  <br/> • 기본 관리 보호  <br/> • 기록 및 분석  <br/> • 기본적인 id 보호  <br/> 테 넌 트 구성  <br/>  이해 관계자에 게 준비  <br/> |
|90일|고급 보호:  <br/> • 관리자 계정  <br/>  • 데이터 &amp; 사용자 계정  <br/>  규정 준수, 위협 및 사용자 요구 사항에 대 한 가시성  <br/>  적응 및 기본 정책 및 보호 기능을 구현 합니다.  <br/> |
|기능 이외에|주요 정책 및 컨트롤을 구체화 및 조정  <br/> 온-프레미스 종속성을 보호 기능을 확장 합니다.  <br/> 비즈니스 및 보안 프로세스 (예: 법률, 내부 인 위협)와 통합  <br/> |
  

   
## <a name="30-days--powerful-quick-wins"></a>30 일-강력한 빠른 wins
<a name="Thirdaydays"> </a>

이러한 태스크는 빠르게 완료될 수 있으며 사용자에게 많은 영향을 미치지 않습니다.
  
|||
|:-----|:-----|
|영역  <br/> |Tasks  <br/> |
|보안 관리  <br/> |• 보안 점수를 확인 하 고 현재 점수를 기록해둡니다 ( [https://securescore.office.com](https://securescore.office.com)).  <br/>  •는 Office 365에 대 한 감사 로깅을 설정 합니다. 참조 [Office 365 보안에서 감사 로그를 검색 &amp; 준수 센터](search-the-audit-log-in-security-and-compliance.md)합니다.<br/> • [보안 향상된을 위해 Office 365 테 넌 트를 구성](tenant-wide-setup-for-increased-security.md) 합니다.  <br/>  •는 정기적으로 대시보드 및 Office 365 보안 및 규정 준수 센터와 클라우드 응용 프로그램 보안에 대 한 보고서를 검토 합니다.  <br/> |
|위협 방지  <br/> |비정상적인 동작에 대 한 기본 위협 탐지 정책을 사용 하 여 모니터링을 시작 하려면 [Microsoft 클라우드 응용 프로그램 보안을 Office 365에 연결](https://docs.microsoft.com/cloud-app-security/connect-office-365-to-microsoft-cloud-app-security) 을 선택 합니다. 걸리는 7 일 이상 탐지에 대 한 초기 계획을 작성 합니다.<br><br/>  관리 계정에 대 한 보호를 구현 합니다.  <br/> • 사용 전용 관리 관리 작업에 대 한 계정입니다.  <br/>  • 관리 계정에 대 한 다단계 인증 (MFA)를 적용 합니다.  <br/>  • 관리 작업에 대 한 [매우 Windows 10 장치 보안](https://docs.microsoft.com/windows-hardware/design/device-experiences/oem-highly-secure) 을 사용 합니다.  <br/> |
|ID 및 액세스 관리  <br/> |• [Azure Active Directory Id 보호를 사용 하도록 설정](https://docs.microsoft.com/azure/active-directory/active-directory-identityprotection-enable)합니다.  <br/> • 페더레이션된 id 환경에 대 한 계정 보안 (암호 길이, 기간, 복잡성 등)를 적용 합니다.  <br/> |
|정보 보호  <br/> | 예제 정보 보호 권장 사항을 검토 합니다. 정보 보호 조직 전체에서 조정을 해야합니다. 이러한 리소스 시작 하기:<br/> • [GDPR에 대 한 office 365 정보 보호](http://aka.ms/o365gdpr) <br/> • [Secure SharePoint Online 사이트 및 파일](https://docs.microsoft.com/Office365/enterprise/secure-sharepoint-online-sites-and-files) (공유, 분류, 데이터 손실 방지 및 Azure 정보 보호 포함)  <br/> |
   
## <a name="90-days--enhanced-protections"></a>90 일-보호 기능이 향상
<a name="Ninetydays"> </a>

이러한 태스크는 계획하고 구현하는 데 다소 시간이 소요되지만 보안 태세를 갖추는 데 큰 도움이 됩니다. 
  
|||
|:-----|:-----|
|영역  <br/> |작업  <br/> |
|보안 관리  <br/> | • 환경에 대 한 권장된 작업에 대 한 보안 점수를 확인 합니다 ( [https://securescore.office.com](https://securescore.office.com)).  <br/>  •는 정기적으로 검토 하는 대시보드 및 Office 365 보안 및 규정 준수 센터, 클라우드 응용 프로그램 보안 및 SIEM 도구에서 보고서를 계속 합니다.  <br/>  • 살펴보고 소프트웨어 업데이트를 구현 합니다.  <br/>  • 행위 공격 시뮬레이션 창 피싱, 암호-스프레이 및 무차별 암호에 대 한 [공격 시뮬레이터](https://support.office.com/article/attack-simulator-office-365-da5845db-c578-4a41-b2cb-5a09689a551b) ( [Office 365 위협 정보를 바탕](office-365-ti.md)으로 포함)를 사용 하 여 공격 합니다.  <br/>  • 정보를 표시 하 (조사 탭)에 클라우드 응용 프로그램 보안의 기본 제공 보고서를 검토 하 여 위험을 공유 합니다.  <br/>  • [규정 준수 관리자](meet-data-protection-and-regulatory-reqs-using-microsoft-cloud.md) 검토 (예: GDPR, 800 171 NIST) 조직에 적용 되는 규정에 대 한 상태를 확인 합니다.  <br/> |
|위협 방지  <br/> | 관리 계정에 대 한 향상 된 보호를 구현 합니다.  <br/>  • 관리 작업에 대 한 [권한이 부여 된 액세스 워크스테이션](https://docs.microsoft.com/windows-server/identity/securing-privileged-access/privileged-access-workstations) (PAWs)을 구성 합니다.  <br/>  • [Azure AD 권한 Id 관리](https://docs.microsoft.com/azure/active-directory/active-directory-privileged-identity-management-configure)를 구성 합니다.  <br/>  •는 Office 365, 클라우드 응용 프로그램 보안 및 AD FS 등의 기타 서비스에서 로깅 데이터를 수집 하는 보안 정보 및 이벤트 (SIEM) 관리 도구를 구성 합니다. Office 365 감사 로그만 90 일 동안 데이터를 저장합니다. SIEM 도구에서이 데이터를 캡처하기를 사용 하면 더 긴 기간에 대 한 데이터를 저장할 수 있습니다.<br/> |
|ID 및 액세스 관리  <br/> | • 사용 하도록 설정 하 고 모든 사용자에 대 한 MFA를 적용 합니다.  <br/>  • [조건부 액세스 및 관련된 정책](https://docs.microsoft.com/en-us/microsoft-365/enterprise/microsoft-365-policies-configurations)집합을 구현 합니다. |
|정보 보호  <br/> | 적응 및 정보 보호 정책을 구현 합니다. 이러한 리소스 예가 포함 되어있습니다.<br/> • [GDPR에 대 한 office 365 정보 보호](http://aka.ms/o365gdpr) <br/> • [보안 SharePoint Online 사이트 및 파일](https://docs.microsoft.com/Office365/enterprise/secure-sharepoint-online-sites-and-files) <br/> <br> Office 365에서 데이터 손실 방지 정책 및 모니터링 도구를 사용 하 여 클라우드 응용 프로그램 보안) 하는 경우 (대신 Office 365에 저장 된 데이터에 대 한. <br><br>고급 경고 (아닌 다른 데이터 손실 방지) 기능에 대 한 Office 365와 클라우드 응용 프로그램 보안을 사용 합니다.  <br/> |
   
## <a name="beyond"></a>기능 이외에
<a name="Beyond"> </a>

다음은 이전 작업에서 작성 하는 것이 중요 보안 조치입니다. 
  
|||
|:-----|:-----|
|영역  <br/> |작업  <br/> |
|보안 관리  <br/> |• 보안 점수를 사용 하 여 다음 작업을 계획을 계속 ( [https://securescore.office.com](https://securescore.office.com)).  <br/>  •는 정기적으로 검토 하는 대시보드 및 Office 365 보안 및 규정 준수 센터, 클라우드 응용 프로그램 보안 및 SIEM 도구에서 보고서를 계속 합니다.  <br/>  • 계속에 대 한 확인 하 고 소프트웨어 업데이트를 구현 합니다.  <br/>  • 대화 법률에 eDiscovery 및 위협 응답 프로세스를 통합 합니다.  <br/> |
|위협 방지  <br/> | • 온-프레미스 (AD, AD FS) identity 구성 요소에 대 한 [액세스 권한을 보안](https://docs.microsoft.com/windows-server/identity/securing-privileged-access/securing-privileged-access) (SPA)을 구현 합니다.  <br/>  • 클라우드 앱 보안 내부 인 위협에 대 한 모니터링을 사용 합니다.  <br/>  • 클라우드 응용 프로그램 보안을 사용 하 여 그림자 IT SaaS 사용 현황을 파악 합니다.  <br/> |
|ID 및 액세스 관리  <br/> | • 구체화 정보 보호 정책:  <br/>  • Azure 정보 보호 및 Office 365 데이터 손실 방지 (DLP).  <br/>  • 클라우드 응용 프로그램 보안 정책 및 경고 합니다.  <br/> |
|정보 보호  <br/> | • 구체화 정책 및 운영 프로세스입니다.  <br/>  • Azure AD Id 보호를 사용 하 여 내부 인 위협을 파악.  <br/> |
   
또한 참조: [Petya 및 WannaCrypt와 같은 신속 하 게 cyberattacks 완화 하는 방법](https://cloudblogs.microsoft.com/microsoftsecure/2018/02/21/how-to-mitigate-rapid-cyberattacks-such-as-petya-and-wannacrypt/)입니다. 
  

