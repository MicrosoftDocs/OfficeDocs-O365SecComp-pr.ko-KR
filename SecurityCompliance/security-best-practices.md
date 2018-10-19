---
title: Office 365에 대한 보안 모범 사례
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 5/22/2018
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MOE150
- MED150
- MBS150
- BCS160
- MET150
ms.assetid: 9295e396-e53d-49b9-ae9b-0b5828cdedc3
description: 이러한 권장된 모범 사례를 수행 하 여 데이터 위반 또는 손상 된 계정의 가능성을 최소화 합니다.
ms.openlocfilehash: 0d3dc30a9975f2ed8fe6d524b4fc67918b34e51d
ms.sourcegitcommit: 49b565f6a57febe53f331b2605d6a06d11e2d0be
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/18/2018
ms.locfileid: "25638002"
---
# <a name="security-best-practices-for-office-365"></a>Office 365에 대한 보안 모범 사례

이러한 권장된 모범 사례를 수행 하 여 데이터 위반 또는 손상 된 계정의 가능성을 최소화 합니다.
  
이 문서는 빠른 목록이 모범 사례를 포함합니다. 자세한 심도 깊은 분석 및 보안 설정에 대 한 정보를 참조 하십시오. [Office 365 보안 로드맵: 처음 30 일, 90 일 동안 및 이외 우선순위 가지 주요](security-roadmap.md)합니다. 이 문서의 정보를 제공 합니다 실제 공격에 대 한 조사에 따라 위험을 평가 하 고 가장 중요 한 보안, 규정 준수, 및 정보를 구현 하는 방법에 코칭 위쪽 Microsoft Office 365 cybersecurity 전문가 들을 제공 하는 위치 Office 365 테 넌 트를 보호 하기 위해 보호 제어 합니다. 위협 우선순위를 지정 기술 전략에 대 한 위협 요소를 변환 하 고 다음 기능 및 컨트롤을 구현 하려면 체계적인 방법을 활용 하는 방법을 알아봅니다.
  
## <a name="use-office-365-secure-score"></a>Office 365 보안 점수를 사용 하 여

보안 점수는 할 수 있는 추가 위험을 줄이는 것을 권장 하는 보안 분석 도구입니다. 보안 점수 Office 365 설정 및 작업을 확인 하 고 Microsoft에 의해 설정 된 초기 계획을 비교 합니다. 최상의 보안 방법으로는 어떻게 정렬 기준으로 점수를 얻을 수 있습니다. 보안 점수를 가져오고를 사용 하 여 Office 365 조직의 보안을 강화 하는 방법에 대 한 자세한 내용은 [Office 365 보안 점수 소개 (영문)을](office-365-secure-score.md)참조 하십시오.
  
보안 점수를 사용해 싶으십니까?
  
[Office 365에 로그인](https://www.office.com/signin)Office 365 [대 한 Office 365 관리자 역할](https://support.office.com/article/da585eea-f576-4f55-a1e0-87090b6aaa9d) 역할에 할당 된 작업이 나 교육용 계정을 사용 합니다.
  
Access 보안에서 점수 [https://SecureScore.office.com](https://SecureScore.office.com)합니다.
  
## <a name="use-multi-factor-authentication-mfa"></a>다단계 인증 (MFA)를 사용 하 여

MFA는 사용자를 전화 통화, 텍스트 메시지 또는 올바르게 자신의 암호를 입력 한 후 스마트 전화기에서 전자 app 알림을 확인을 요구 하 여 강력한 암호 전략에 추가 계층의 보호를 추가 합니다. Office 365 사용자 계정 전체에서 MFA와 여전히 사용자의 암호가 손상 된 경우에 무단된 액세스 로부터 보호 됩니다. 계정 추가 시도 충족 된 후 액세스까지 계정에 부여 하지 않기 때문에 보호 됩니다. 손상 된 또는 도난당 한 암호 충분 하지 않습니다.
  
- [Office 365 배포에 대 한 다중 요소 인증에 대 한 계획](https://support.office.com/article/043807b2-21db-4d5c-b430-c8a6dee0e6ba)
    
- [Office 365에 대한 다단계 인증 설정](https://support.office.com/article/8f0454b2-f51a-4d9c-bcde-2c48e41621c6)하려면
    
## <a name="use-office-365-cloud-app-security"></a>Office 365 클라우드 응용 프로그램 보안을 사용 하 여

비정상적인 활동을 추적 및 작업을 수행 하 여 비즈니스 요구 사항에 따라 정책을 설정 합니다. 여러 번 시도 로그인 또는 로그인 시 알 수 없거나 위험한 IP 주소에서 실패 한 관리자가 많은 양의 데이터를 다운로드 하는 등의 비정상 또는 위험한 사용자 작업을 검토할 수 있도록 Office 365 클라우드 응용 프로그램 보안 경고를 설정 합니다. Office 365 Enterprise E5 플랜과 조직용 귀하가 Office 365 클라우드 응용 프로그램 보안을 사용 하 여 시작할 수 있습니다. 다른 엔터프라이즈 계획을 설치한 경우에 추가 기능으로 Office 365 클라우드 응용 프로그램 보안을 구입할 수 있습니다.
  
- [O 365 클라우드 앱 보안 개요](office-365-cas-overview.md)
    
- [Office 365 Cloud App Security 켜기](turn-on-office-365-cas.md)
    
## <a name="secure-mail-flow"></a>보안 메일 흐름

전자 메일을 통해 전송 되는 풍부한 기능 집합에서 Exchange Online 보호 하 고 각 전자 메일 메시지의 보낸 사람의 id에 대 한 큰 보증을 확보 합니다.를 보호 하 고 알 수 없는 맬웨어, 바이러스 및 악의적인 Url 구현 합니다.
  
- 조직에 대 한 [Office 365 전자 메일 스팸 방지 보호](anti-spam-protection.md) 정책을 구성 합니다. 
    
- 소개 하 고 [안전한 첨부 파일 및 안전 링크에 대 한 고급 위협 보호](https://technet.microsoft.com/library/mt148491.aspx)를 사용 합니다.
    
- [조직에 맬웨어 방지 보호 기능을 추가](https://technet.microsoft.com/en-us/library/jj200669%28v=exchg.150%29.aspx)합니다.
    
- 소개 하 고 사용자를 위한 [Office 365에서 전자 메일 메시지에 안전 팁](safety-tips-in-office-365.md) 를 활성화 합니다. 
    
- Office 365의 조직에 대 한 사용자 지정 도메인을 사용 중인 경우 조직에서 보낸 메일의 유효성을 검사 하 고 스푸핑을 방지 하는 데 도움이 SPF, DKIM, 및 DMARC를 설정 합니다.
    
  - [SPF 스푸핑을 방지 하기 위해 Office 365에서 설정](https://docs.microsoft.com/office365/SecurityCompliance/set-up-spf-in-office-365-to-help-prevent-spoofing)합니다.
    
  - [Office 365에서 사용자 지정 도메인에서 보낸 아웃 바운드 전자 메일의 유효성을 검사를 사용 하 여 DKIM](https://docs.microsoft.com/office365/SecurityCompliance/set-up-spf-in-office-365-to-help-prevent-spoofing)합니다.
    
  - [Office 365의 전자 메일의 유효성을 검사를 사용 하 여 DMARC](https://technet.microsoft.com/library/mt734386%28v=exchg.150%29.aspx)합니다.
    
## <a name="enable-mailbox-audit-logging"></a>사서함 감사 로깅 사용

일부 감사 로깅이 Office 365; 하면 자동으로 활성화 되는지 그러나 사서함 감사 로깅 기본적으로 켜져 있지 됩니다. Exchange Online PowerShell을 사용 하 여 Office 365의 모든 사용자 사서함에 대 한 감사 로깅을 설정 합니다. 내용은 [Office 365의 감사 사서함 사용](https://go.microsoft.com/fwlink/p/?LinkID=626109)을 참조 하십시오.
  
감사 로그를 사용 하면 수 활성화 한 후 [Office 365 보안에서 감사 로그를 검색 &amp; 준수 센터](search-the-audit-log-in-security-and-compliance.md) 사용자가 보낸 메시지 및 기타 작업에 사서함 소유자, 위임된 된 사용자에 의해 수행 하 여 사용자 사서함에 로그인 확인 하려면 또는 관리자입니다. Office 365에 포함 된 사서함 활동의 목록에 대 한 감사 로그를 기본적으로 [Exchange 사서함 활동](search-the-audit-log-in-security-and-compliance.md#exchange-mailbox-activities)을 참조 하십시오.
  
감사 로그는 감사 로그 항목을 저장 하는 시간을 변경 하는 등로 수행할 수 있는 다른 작업에 대 한 내용은 [Exchange 2016에서 로깅 사서함 감사](https://technet.microsoft.com/en-us/library/ff459237%28v=exchg.160%29.aspx)를 참조 하십시오.
  
## <a name="configure-data-loss-prevention-dlp"></a>데이터 손실 방지 (DLP) 구성

DLP를 사용 하면 중요 한 데이터를 식별 하 고 사용자가 실수로 또는 의도적으로 데이터를 공유 하는 것을 방지 하는 정책을 만들 수 있습니다. DLP은 사용자에 게 잃지 규격 유지할 수 있도록 Exchange Online, SharePoint Online 및 OneDrive를 포함 하 여 Office 365에서 작동 합니다. 자세한 내용은 [데이터 손실 방지 정책 개요](data-loss-prevention-policies.md)를 참조 하십시오.
  
## <a name="use-customer-lockbox"></a>고객 Lockbox를 사용 하 여

Office 365 관리자를으로 Microsoft 기술 지원 엔지니어 도움말 세션 중에 데이터에 액세스 하는 방법을 제어 하려면 고객 Lockbox를 사용할 수 있습니다. 엔지니어가 문제를 해결 하 고 문제를 해결 하 여 데이터에 대 한 액세스를 필요로 하는의 경우, 고객 Lockbox를 사용 하면 승인 하거나 거부 하는 액세스 요청 수 있습니다. 를 승인 하는 경우는 엔지니어 데이터에 액세스할 수 있습니다. 각 요청에 만료 시간이 있어서는 하 고 문제를 해결 한 후 요청을 닫고 access가 해지 되었습니다. Office 365 Enterprise e 5 계획에 포함 된 고객 Lockbox 또는 다른 Office 365 enterprise 플랜과 별도 구독을 구입할 수 있습니다. 내용은 [Office 365 고객 Lockbox 요청](https://support.office.com/article/36f9cdd1-e64c-421b-a7e4-4a54d16440a2)을 참조 하십시오.
  
## <a name="try-it-yourself"></a>사용자가 직접 사용해 보기
<a name="SecureScore"> </a>

프로덕션 환경에서이 채택 하기 전에 Office 365 평가판 구독에서 작업 하는 이러한 보안 기능을 참조 하십시오.
  
- [Office 365 평가판 구독 만들기](https://technet.microsoft.com/library/mt736406.aspx)
    
- [구성 하 고 MFA 사용자 계정에 대 한 테스트](https://technet.microsoft.com/library/mt492459.aspx)
    
- [구성 및 테스트 사용자에 게 알리도록 전역 관리자 활동의 Office 365 클라우드 응용 프로그램 보안](https://technet.microsoft.com/library/mt757250.aspx)
    
- [구성 하 고 ATP 의심 스러운 전자 메일에 대 한 테스트](https://technet.microsoft.com/library/mt490479.aspx)
    
- 위의 단계를 각각에 대 한 평가판 구독에 대 한 [Office 365 보안 점수](https://securescore.office.com/) 를 확인 합니다. 
    

