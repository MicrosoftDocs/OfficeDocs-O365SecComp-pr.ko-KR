---
title: Office 365에 대한 보안 모범 사례
ms.author: tracyp
author: MSFTTracyP
manager: laurawi
ms.date: 5/22/2018
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MOE150
- MED150
- MBS150
- BCS160
- MET150
ms.assetid: 9295e396-e53d-49b9-ae9b-0b5828cdedc3
ms.collection:
- M365-security-compliance
- Strat_O365_IP
description: 권장 되는 모범 사례를 수행 하 여 데이터 위반 이나 손상 된 계정을 최소화 합니다.
ms.openlocfilehash: bd4b911cd5972b7d6dc9b55c17e375d326b1d571
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32264640"
---
# <a name="security-best-practices-for-office-365"></a>Office 365에 대한 보안 모범 사례

권장 되는 모범 사례를 수행 하 여 데이터 위반 이나 손상 된 계정을 최소화 합니다.
  
이 문서에는 모범 사례에 대 한 간략 한 목록이 포함 되어 있습니다. 보안 설정에 대 한 자세한 분석 및 정보는 [Office 365 보안 로드맵: 처음 30 일, 90 일 및 그 이상에 대 한 최고 우선 순위](security-roadmap.md)를 참조 하세요. 이 문서에서는 cybersecurity 전문가가 위험을 평가 하 고 가장 중요 한 보안, 규정 준수 및 정보를 구현 하는 방법에 대 한 교육를 제공 하는 실제 세계 공격 조사를 기반으로 하는 정보를 찾을 수 있습니다. Office 365 테 넌 트를 보호 하기 위한 보호 제어 위협의 우선 순위를 지정 하 고 위협을 기술적 전략으로 번역 한 다음, 특징과 컨트롤을 구현 하는 체계적인 방법을 알아봅니다.
  
## <a name="use-office-365-secure-score"></a>Office 365 보안 점수 사용

보안 점수는 위험을 더 완화 하기 위해 수행할 수 있는 작업을 권장 하는 보안 분석 도구입니다. 보안 점수가 Office 365 설정 및 활동을 살펴보고 Microsoft에서 설정한 기준과 비교 합니다. 최선의 보안 관례에 따라 정렬 된 방식을 기준으로 점수를 얻게 됩니다. 보안 점수를 얻고이를 사용 하 여 office 365 조 직의 보안을 강화 하는 방법에 대 한 자세한 내용은 [office 365 보안 점수 소개](office-365-secure-score.md)를 참조 하세요.
  
보안 점수를 보 시겠습니까?
  
office 365- [office 365 관리자 역할 역할에](https://support.office.com/article/da585eea-f576-4f55-a1e0-87090b6aaa9d) 할당 된 회사 또는 학교 계정을 사용 하 여 [office 365에 로그인](https://www.office.com/signin)합니다.
  
보안 점수에 [https://SecureScore.office.com](https://SecureScore.office.com)액세스 합니다.
  
## <a name="use-multi-factor-authentication-mfa"></a>MFA (multi-factor authentication) 사용

MFA는 사용자가 자신의 암호를 올바르게 입력 한 후 전화 통화, 문자 메시지 또는 스마트 전화에서 앱 알림을 승인 하도록 요구 하 여 강력한 암호 전략에 추가 보호 계층을 추가 합니다. 현재 위치에서 MFA를 사용 하는 경우 Office 365 사용자 계정은 사용자의 암호가 노출 되더라도 무단으로 액세스 하지 못하도록 보호 됩니다. 추가 챌린지를 만족할 때까지 계정에 대 한 액세스가 허용 되지 않으므로 계정이 보호 됩니다. 손상 되었거나 도난당 한 암호가 충분 하지 않습니다.
  
- [Office 365 배포에 대 한 다단계 인증 계획](https://support.office.com/article/043807b2-21db-4d5c-b430-c8a6dee0e6ba)

- [Office 365에 대한 다단계 인증 설정](https://support.office.com/article/8f0454b2-f51a-4d9c-bcde-2c48e41621c6)하려면

## <a name="use-office-365-cloud-app-security"></a>Office 365 Cloud App Security 사용

비즈니스 요구 사항에 따라 정책을 설정 하 여 비정상적인 활동을 추적 하 고 작업을 수행 합니다. 관리자가 많은 양의 데이터를 다운로드 하거나, 로그인을 여러 번 수행 하거나, 알 수 없는 또는 위험한 IP 주소에서 로그인 하는 등의 비정상적 이거나 위험한 사용자 활동을 검토 하도록 Office 365 Cloud App Security를 사용 하 여 알림을 설정 합니다. office 365 Enterprise E5 요금제를 사용 하는 조직의 경우 즉시 Office 365 Cloud App Security를 사용 하 여 시작할 수 있습니다. 다른 enterprise 요금제를 사용 하는 경우 Office 365 Cloud App Security를 추가 기능으로 구입할 수 있습니다.
  
- [O365 Cloud App Security 개요](office-365-cas-overview.md)

- [Office 365 Cloud App Security 사용](turn-on-office-365-cas.md)

## <a name="secure-mail-flow"></a>보안 메일 흐름

Exchange Online Protection에서 다양 한 기능 집합을 구현 하 고 각 전자 메일 메시지의 보낸 사람 id에 대 한 보다 강력한 보증을 얻고 전자 메일을 통해 전송 되는 알려지지 않은 맬웨어, 바이러스 및 악의적인 url을 보호 합니다.
  
- 조직에 대 한 [Office 365 전자 메일 스팸 방지 보호](anti-spam-protection.md) 정책을 구성 합니다.

- [안전한 첨부 파일 및 안전한 링크에](https://technet.microsoft.com/library/mt148491.aspx)대 한 자세한 내용을 알아보고 Advanced threat protection을 사용 합니다.

- [조직에 맬웨어 방지 보호 기능을 추가](https://technet.microsoft.com/en-us/library/jj200669%28v=exchg.150%29.aspx)합니다.

- 사용자를 위해 [Office 365의 전자 메일 메시지에 대 한 보안 팁](safety-tips-in-office-365.md) 을 알아보고 사용 하도록 설정 합니다.

- Office 365에서 조직에 대 한 사용자 지정 도메인을 사용 하는 경우에는 SPF, dkim을 설정한 다음 DMARC이 조직에서 보낸 메일의 유효성을 검사 하 고 스푸핑을 방지 하는 데 도움이 됩니다.

  - [스푸핑 방지를 위해 Office 365에서 SPF를 설정](https://docs.microsoft.com/office365/SecurityCompliance/set-up-spf-in-office-365-to-help-prevent-spoofing)합니다.

  - [dkim을 사용 하 여 Office 365의 사용자 지정 도메인에서 보낸 아웃 바운드 전자 메일의 유효성을 검사](https://docs.microsoft.com/office365/SecurityCompliance/set-up-spf-in-office-365-to-help-prevent-spoofing)합니다.

  - [DMARC을 사용 하 여 Office 365의 전자 메일 유효성을 검사](https://technet.microsoft.com/library/mt734386%28v=exchg.150%29.aspx)합니다.

## <a name="enable-mailbox-audit-logging"></a>사서함 감사 로깅 사용

일부 감사 로깅은 Office 365에서 자동으로 사용 하도록 설정 됩니다. 그러나 사서함 감사 로깅은 기본적으로 설정 되지 않습니다. Exchange Online PowerShell을 사용 하 여 Office 365에서 모든 사용자 사서함에 대 한 감사 로깅을 설정 합니다. 자세한 내용은 [Office 365에서 사서함 감사 사용](https://go.microsoft.com/fwlink/p/?LinkID=626109)을 참조 하십시오.
  
감사 로깅을 사용 하도록 설정한 후 [Office 365 보안 &amp; 및 준수 센터에서 감사 로그를 검색](search-the-audit-log-in-security-and-compliance.md) 하 여 사용자 사서함에 로그인 한 사람, 보낸 메시지 및 사서함 소유자가 수행한 기타 작업을 확인할 수 있습니다. 관리자에 게 문의 하십시오. 기본적으로 Office 365 감사 로그에 포함 된 사서함 활동 목록은 [Exchange 사서함 활동](search-the-audit-log-in-security-and-compliance.md#exchange-mailbox-activities)을 참조 하십시오.
  
감사 로그를 사용 하 여 수행할 수 있는 기타 작업에 대 한 자세한 내용은 [Exchange 2016에서 사서함 감사 로깅](https://technet.microsoft.com/en-us/library/ff459237%28v=exchg.160%29.aspx)를 참조 하십시오.
  
## <a name="configure-data-loss-prevention-dlp"></a>DLP (데이터 손실 방지) 구성

DLP를 사용 하면 중요 한 데이터를 식별 하 고 사용자가 실수로 또는 의도적으로 데이터를 공유 하지 못하게 하는 정책을 만들 수 있습니다. DLP는 Exchange online, SharePoint Online 및 OneDrive를 포함 하는 Office 365에서 작동 하 여 사용자가 워크플로를 중단 하지 않고 준수 상태를 유지할 수 있도록 합니다. 자세한 내용은 [데이터 손실 방지 정책 개요](data-loss-prevention-policies.md)를 참조하세요.
  
## <a name="use-customer-lockbox"></a>고객 Lockbox 사용

Office 365 관리자는 Customer Lockbox를 사용하여 Microsoft 기술 지원 엔지니어가 도움말 세션 동안 사용자의 데이터에 액세스하는 방법을 제어할 수 있습니다. 엔지니어가 문제를 해결하기 위해 사용자 데이터에 대한 액세스 권한을 요구하는 경우 Customer Lockbox를 사용하여 액세스 요청을 승인하거나 거부할 수 있습니다. 이를 승인 하면 엔지니어가 데이터에 액세스할 수 있습니다. 각 요청에는 만료 시간이 있으며 문제가 해결되면 요청이 닫히고 액세스 권한이 취소됩니다. 고객 Lockbox가 office 365 enterprise E5 계획에 포함 되어 있거나 다른 Office 365 Enterprise 요금제를 사용 하 여 별도의 구독을 구입할 수도 있습니다. 자세한 내용은 [Office 365 고객 Lockbox 요청](https://support.office.com/article/36f9cdd1-e64c-421b-a7e4-4a54d16440a2)을 참조 하세요.
  
## <a name="try-it-yourself"></a>직접 사용해 보기
<a name="SecureScore"> </a>

프로덕션 환경에 Office 365 평가판 구독을 채택 하기 전에 이러한 보안 기능을 통해 작동 하는 방법을 확인 하세요.
  
- [Office 365 평가판 구독 만들기](https://technet.microsoft.com/library/mt736406.aspx)

- [사용자 계정에 대 한 MFA 구성 및 테스트](https://technet.microsoft.com/library/mt492459.aspx)

- [전역 관리자 활동을 알리기 위해 Office 365 Cloud App Security를 구성 하 고 테스트 합니다.](https://technet.microsoft.com/library/mt757250.aspx)

- [의심 스러운 전자 메일에 대 한 ATP 구성 및 테스트](https://technet.microsoft.com/library/mt490479.aspx)

- 위의 각 단계에 대 한 [Office 365 보안 점수](https://securescore.office.com/) 에서 평가판 구독을 확인 합니다.