---
title: DMARC를 사용 하 여 Office 365의 전자 메일의 유효성을 검사 하려면
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 10/9/2017
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.custom: TN2DMC
ms.assetid: 4a05898c-b8e4-4eab-bd70-ee912e349737
description: '보낸 사람이 정책 프레임 워크 (SPF) 및 DomainKeys 식별 된 메일 (DKIM) 메일 보낸사람을 인증 하 고 대상 전자 메일 시스템 도메인에서 보낸 메시지를 신뢰 확인을 사용 하 여 도메인 기반 메시지 인증, 보고 및 적합성 (DMARC) 작동 하는 . '
ms.openlocfilehash: 199ab67d17152fc0c4ed6b9f87cde66beaf913d5
ms.sourcegitcommit: e9dca2d6a7838f98bb7eca127fdda2372cda402c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/21/2018
ms.locfileid: "23003227"
---
# <a name="use-dmarc-to-validate-email-in-office-365"></a>DMARC를 사용 하 여 Office 365의 전자 메일의 유효성을 검사 하려면

Domain-based 메시지 인증, 보고 및 적합성 [DMARC)](https://dmarc.org) 메일 보낸사람을 인증 하 고 대상 전자 메일 시스템에서 보낸 메시지를 신뢰 되었는지 확인 하려면 보낸 사람이 정책 프레임 워크 (SPF) 및 DomainKeys 식별 된 메일 (DKIM)와 함께 작동 도메인입니다. SPF 및 DKIM DMARC 구현 스푸핑 및 피싱 전자 메일에 대 한 추가 보호를 제공 합니다. 받는 메일 시스템 메시지와 함께 수행할 작업을 결정 하는 DMARC 도움이 실패 SPF 또는 DKIM 확인 하 여 도메인에서 보낸 합니다. 
  
## <a name="how-do-spf-and-dmarc-work-together-to-protect-email-in-office-365"></a>SPF 및 DMARC 작동 방법 함께 Office 365의 전자 메일을 보호 하기 위해
<a name="SPFandDMARC"> </a>

 전자 메일 메시지는 여러 송신자 또는 보낸사람 주소를 포함할 수 있습니다. 이 주소는 서로 다른 용도로 사용 됩니다. 이러한 주소 예로 들 수 있습니다. 
  
- **"Mail From" 주소를 사용 합니다.** 보낸사람을 식별 하 고 배달 못함 정보와 같은 메시지의 배달에 모든 문제가 발생 하는 경우 반환 알림을 보낼 위치를 지정 합니다. 이 전자 메일 메시지의 봉투 부분에 표시 되며 일반적으로 전자 메일 응용 프로그램에 의해 표시 되지 않습니다. 이 5321.MailFrom 주소 또는 역방향 경로 주소 라고도 합니다.
    
- **"에서" 주소** 전자 메일 응용 프로그램으로 From 주소로 표시 되는 주소입니다. 이 주소는 전자 메일의 작성자를 식별 합니다. 즉, 사용자 또는 메시지를 작성 하는 일을 담당 하는 시스템의 사서함입니다. 이 방법을 5322.From 주소를 라고도 합니다.
    
SPF는 DNS TXT 레코드를 사용 하 여 지정된 된 도메인에 대 한 권한이 부여 된 보내는 IP 주소 목록을 제공 합니다. 일반적으로 SPF 확인 5321.MailFrom 주소에 대해서만 수행 됩니다. 이 5322.From 주소는 인증 되지 않은 SPF를 사용 하는 경우 단독으로 것을 의미 합니다. 이 사용자 위장 된 5322.From 보낸사람 주소를 되었지만 SPF 검사를 통과 하는 메시지를 받을 수 있는 시나리오에 대 한 수 있습니다. 이 SMTP 대화 내용이 예로 들 수 있습니다.
  
```
S: Helo woodgrovebank.com
S: Mail from: phish@phishing.contoso.com
S: Rcpt to: astobes@tailspintoys.com
S: data
S: To: "Andrew Stobes" <astobes@tailspintoys.com>
S: From: "Woodgrove Bank Security" <security@woodgrovebank.com>
S: Subject: Woodgrove Bank - Action required
S:
S: Greetings User,
S: 
S: We need to verify your banking details.
S: Please click the following link to verify that we have the right information for your account.
S: 
S: http://short.url/woodgrovebank/updateaccount/12-121.aspx
S:
S: Thank you,
S: Woodgrove Bank
S: .

```

이 대화 내용이에서 보낸사람 주소는 다음과 같습니다.
  
- 메일 주소 (5321.MailFrom): phish@phishing.contoso.com
    
- 보낸사람 주소 (5322.From): security@woodgrovebank.com
    
SPF를 구성 해 놓은 받는 서버에서 주소 phish@phishing.contoso.com 메일에 대해 확인을 수행 합니다. 도메인 phishing.contoso.com에 대 한 유효한 소스에서 메시지를 받은 경우 SPF 확인 전달 합니다. 전자 메일 클라이언트 보낸사람 주소를 표시 하므로 사용자에 게 security@woodgrovebank.com에서이 메시지 인지 표시 합니다. SPF 만으로는, woodgrovebank.com의 유효성을 검사 인증 되지 않았습니다.
  
DMARC를 사용 하면 수신 서버는 또한 보낸사람 주소에 대 한 검사를 수행 합니다. 위의 예제에서 woodgrovebank.com에 대 한 전체에 DMARC TXT 레코드 있으면 확인 보낸사람 주소에 대해이 실패 합니다.
  
## <a name="what-is-a-dmarc-txt-record"></a>DMARC TXT 레코드 이란?
<a name="WhatisDMARC"> </a>

SPF에 대 한 DNS 레코드를 다음과 같이 DMARC에 대 한 레코드는 스푸핑 및 피싱 방지 하는 DNS 텍스트 (TXT) 레코드가입니다. DNS에 DMARC TXT 레코드를 게시 합니다. DMARC TXT 레코드 보내는 도메인의 공식된 소유자에 대 한 전자 메일의 작성자의 IP 주소를 확인 하 여 전자 메일 메시지의 출처의 유효성을 검사 합니다. DMARC TXT 레코드 권한이 부여 된 아웃 바운드 전자 메일 서버를 식별합니다. 대상 전자 메일 시스템 받은 메시지 권한이 부여 된 아웃 바운드 전자 메일 서버에서 시작 되었는지 확인할 수 있습니다.
  
Microsoft의 DMARC TXT 레코드는 다음과 유사 합니다.
  
```
_dmarc.microsoft.com.   3600    IN      TXT     "v=DMARC1; p=none; pct=100; rua=mailto:d@rua.agari.com; ruf=mailto:d@ruf.agari.com; fo=1" 

```

Microsoft 보냅니다 해당 DMARC [Agari](https://agari.com)를 보고, 타사의 합니다. Agari를 수집 하 고 DMARC 보고서를 분석 합니다.
  
## <a name="implement-dmarc-for-inbound-mail"></a>인바운드 메일에 대 한 DMARC 구현
<a name="implementDMARCinbound"> </a>

Office 365에서 수신 하는 메일에 대 한 DMARC를 설정 하는 작업을 수행 필요가 없습니다. 우리 했을 때 주의 하지 않아도의 모든 있습니다. 싶으십니까 하는 메일을 수행 하는 작업 못해도 사용해 DMARC 검사를 통과 [인바운드 전자 메일 DMARC에 실패 하는 Office 365 어떻게 핸들](use-dmarc-to-validate-email.md#inbounddmarcfail)을 참조 하십시오.
  
## <a name="implement-dmarc-for-outbound-mail-from-office-365"></a>Office 365에서 아웃 바운드 메일에 대 한 DMARC를 구현 합니다.
<a name="implementDMARCoutbound"> </a>

즉, Office 365를 사용 하는 경우 사용자 지정 도메인을 사용 하지 않는 onmicrosoft.com를 사용 하 여, 구성 또는 조직에 대 한 DMARC를 구현 하는 다른 작업을 수행할 필요가 없습니다. 하면 SPF 이미 설정 하 고 Office 365에 보내는 메일에 대 한 DKIM 서명을 자동으로 생성 합니다. 이 서명 하는 방법에 대 한 자세한 내용은 [DKIM 및 Office 365의 기본 동작을](use-dkim-to-validate-outbound-email.md#DefaultDKIMbehavior)참조 하십시오.
  
 사용자 지정 도메인 했거나 Office 365 외에도 온-프레미스 Exchange 서버를 사용 하는 경우에 수동으로 아웃 바운드 메일에 대 한 DMARC를 구현 해야 합니다. 사용자 지정 도메인에 대 한 DMARC 구현 다음이 단계에 포함 됩니다. 
  
- [1 단계: 도메인에 대 한 메일의 유효한 소스를 식별 합니다.](use-dmarc-to-validate-email.md#IdentifyValidSources)
    
- [2 단계: Office 365에서 도메인에 대 한 SPF를 설정 합니다.](use-dmarc-to-validate-email.md#ConfigSPF)
    
- [3 단계: Office 365에서 사용자 지정 도메인에 대 한 DKIM를 설정 합니다.](use-dmarc-to-validate-email.md#ConfigDKIM)
    
- [Office 365에서 도메인에 대 한 DMARC TXT 레코드를 형성 하는 4 단계:](use-dmarc-to-validate-email.md#CreateDMARCRecord)
    
### <a name="step-1-identify-valid-sources-of-mail-for-your-domain"></a>1 단계: 도메인에 대 한 메일의 유효한 소스를 식별 합니다.
<a name="IdentifyValidSources"> </a>

SPF 이미 설정 하는 경우 다음 하면가 이미 모음은이 연습을 통해 돌아갑니다. 그러나 DMARC에 대 한 가지 추가 고려 사항입니다. 도메인에 대 한 메일의 출처를 식별 하는 경우 두 질문에 답해야 합니다 가지가 있습니다.
  
- 어떤 IP 주소 내 도메인에서 메시지를 보낼?
    
- 내를 대신 하 여 제 3 자에서 보낸 메일에 대 한 5321.MailFrom 및 5322.From 도메인 일치시킬지 여부
    
### <a name="step-2-set-up-spf-for-your-domain-in-office-365"></a>2 단계: Office 365에서 도메인에 대 한 SPF를 설정 합니다.
<a name="ConfigSPF"> </a>

유효한 모든 보낸 사람의 목록이 만들었으므로 [스푸핑을 방지 하기 위해 Office 365에서 SPF를 설정](set-up-spf-in-office-365-to-help-prevent-spoofing.md)하려면 단계를 따라 수 있습니다.
  
예: contoso.com Exchange Online에서 해당 IP 주소 192.168.0.1, 및 해당 IP 주소는 192.168.100.100, 웹 응용 프로그램은 온-프레미스 Exchange 서버에서 메일을 보내는 것으로 가정 SPF TXT 레코드는 다음과 같습니다.
  
```
contoso.com  IN  TXT  " v=spf1 ip4:192.168.0.1 ip4:192.168.100.100 include:spf.protection.outlook.com -all"
```

최상의 방법으로는 SPF TXT 레코드 수식의 계산 시간이 계정 제 3 자 보낸사람으로를 확인 합니다.
  
### <a name="step-3-set-up-dkim-for-your-custom-domain-in-office-365"></a>3 단계: Office 365에서 사용자 지정 도메인에 대 한 DKIM를 설정 합니다.
<a name="ConfigDKIM"> </a>

SPF 설정한 후에 DKIM를 설정 해야 합니다. DKIM은 메시지 헤더에 전자 메일 메시지에 디지털 서명을 추가할 수 있습니다. DKIM를 설정 하지 않으며 대신 도메인에 대 한 기본 DKIM 구성을 사용 하 여 Office 365를 허용 하는 경우에 DMARC 실패할 수 있습니다. 기본 DKIM 구성 초기 onmicrosoft.com 도메인을 사용 하 여 사용자 지정 도메인 하지 5322.From 주소로 때문입니다. 이렇게 하면는 5321.MailFrom 도메인에서 보낸 모든 전자 메일의 5322.From 주소와 일치 하지 됩니다.
  
사용자를 대신 하 여 메일을 보낼 있는 제 3 자가 발신자 있고 대리인이 보내는 메일에 짝이 맞지 않는 5321.MailFrom와 5322.From 주소 하는 경우 해당 전자 메일에 대 한 DMARC 실패 합니다. 이 문제를 방지 하려면 해당 제 3 자가 발신자 구체적으로 사용 하 여 도메인에 대 한 DKIM를 설정 해야 합니다. 따라서이 타사 서비스에서 전자 메일을 인증 하는 Office 365 수 있습니다. 그러나 수도 있습니다 다른 등 yahoo!, Gmail, 및 Comcast, 사용자가 보낸 전자 메일 되었으면 처럼 제 3 자에 의해 자신에 게 보낸 전자 메일을 확인 합니다. 이것은 해당 사서함이 있는 위치에 관계 없이 도메인 신뢰 관계를 구축 하 여 고객을 허용 하기 때문에 유용 하 고 동시에 Office 365 되지 않음 표시 메시지를 도메인에 대 한 인증 검사를 통과 하기 때문에 스푸핑 때문에 스팸으로 합니다.
  
사용자 도메인을 스푸핑할 수 있도록 제 3 자 보낸사람에 대 한 DKIM를 설정 하는 방법을 비롯 하 여 도메인에 대 한 DKIM 설정에 대 한 지침은 [Office 365에서 사용자 지정 도메인에서 보낸 아웃 바운드 전자 메일의 유효성을 검사를 사용 하 여 DKIM](use-dkim-to-validate-outbound-email.md)를 참조 하십시오.
  
### <a name="step-4-form-the-dmarc-txt-record-for-your-domain-in-office-365"></a>Office 365에서 도메인에 대 한 DMARC TXT 레코드를 형성 하는 4 단계:
<a name="CreateDMARCRecord"> </a>

여기서 언급 되지 않은 다른 구문을 옵션 되지만, 다음은 Office 365에 대 한 가장 일반적으로 사용 되는 옵션입니다. 양식 형식으로 도메인에 대 한 DMARC TXT 레코드:
  
```
_dmarc.domainTTL IN TXT "v=DMARC1; pct=100; p=policy
```

여기서 각 부분이 나타내는 의미는 다음과 같습니다.
  
-  *도메인* 은 보호 하려는 도메인은입니다. 기본적으로 레코드는 도메인 및 모든 하위 도메인의 메일을 보호합니다. 예, _dmarc.contoso.com을 지정 하는 경우 다음 DMARC 보호 하는 메일 도메인 및 housewares.contoso.com 또는 plumbing.contoso.com 등의 모든 하위 도메인의 합니다. 
    
-  *TTL* 1 시간에 해당 하는 항상 되어야 합니다. 두 시간 (1 시간) TTL에 사용 되는 단위 (60 분), 분 또는 초 (3600 초) 도메인에 대 한 등록자에 따라 달라 집니다. 
    
- pct = 100 전자 메일의 100%에 대해이 규칙을 사용 해야 함을 나타냅니다.
    
-  *정책* DMARC 실패 하는 경우에 따라를 받는 서버를 원하는 어떤 정책을 지정 합니다. 정책을 격리를 없음으로 설정 하거나 취소할 수 있습니다. 
    
에 사용할 옵션에 대 한 내용은 [Office 365에서 DMARC를 구현 하기 위한 모범 사례](use-dmarc-to-validate-email.md#DMARCbestpractices)에 설명 된 개념을 숙지 됩니다.
  
예제:
  
None으로 설정 하는 정책
  
```
_dmarc.contoso.com 3600 IN  TXT  "v=DMARC1; p=none"
```

격리로 정책 설정
  
```
_dmarc.contoso.com 3600 IN  TXT  "v=DMARC1; p=quarantine"
```

거부로 설정 하는 정책
  
```
_dmarc.contoso.com  3600 IN  TXT  "v=DMARC1; p=reject"
```

사용자의 레코드를 세운 후에 도메인 등록자에서 레코드를 업데이트 해야 합니다. Office 365에 대 한 DNS 레코드를 DMARC TXT 레코드를 추가 하는 지침에 대 한 [DNS 레코드를 관리 하는 경우 Office 365 용 DNS 레코드 만들기](https://support.office.com/article/Create-DNS-records-for-Office-365-when-you-manage-your-DNS-records-b0f3fdca-8a80-4e8e-9ef3-61e8a2a9ab23)를 참조 합니다.
  
## <a name="best-practices-for-implementing-dmarc-in-office-365"></a>Office 365에서 DMARC를 구현 하기 위한 모범 사례
<a name="DMARCbestpractices"> </a>

메일 흐름의 나머지 부분에 영향을 주지 않고도 DMARC를 점진적으로 구현할 수 있습니다. 페이지를 만들고 다음과 같은이 단계로 구성 하는 전체 계획 roll을 구현 합니다. 하위 도메인을 다음 다른 하위 도메인으로 먼저 이러한 각 단계를 수행 하 고 마지막으로 다음 단계로 이동 하기 전에 조직에서 최상위 도메인으로 합니다.
  
1. 모니터 DMARC 구현의 영향
    
    하위 도메인 이나는 DMARC 수신기 사용자에 게 보낼가 해당 도메인을 사용 하 여 표시 하는 메시지에 대 한 통계를 요청 하는 도메인에 대 한 간단한 모니터링 모드 레코드를 시작 합니다. 모니터링 모드 레코드는 none으로 설정 하는 정책 수 있는 DMARC TXT 레코드 (p = 없음). 많은 기업이 p 사용 하 여 DMARC TXT 레코드를 게시 = none 확실 하지 않은 때문에 얼마나 많은 전자 메일에 대 한 보다 제한적인 DMARC 정책을 게시 하 여 손실 될 수 있습니다. 
    
    메시징 인프라에서 SPF 또는 DKIM를 구현 했을 때 하기 전에도 수행할 수 있습니다. 그러나 효과적으로 격리 하거나도 SPF 및 DKIM을 구현할 때까지 DMARC를 사용 하 여 메일을 거부할 수 없습니다. SPF 및 DKIM을 소개 하는 대로 DMARC을 통해 생성 된 보고서의 번호 및 하지 않는 및 이러한 검사를 통과 하는 메시지의 원본 나옵니다. 합법적인 트래픽을 비용을 쉽게 확인할 수 있습니다,에서 다루지 하 고 모든 문제를 해결 합니다. 얼마나 많은 사기 메시지 전송 되 고, 참조도 먼저 어디에서 하 고 있습니다.
    
2. 외부 메일 시스템 DMARC 실패 하는 메일 격리를 요청 합니다.
    
    생각 되는 모든 또는 대부분의 합법적인 트래픽 SPF 및 DKIM로 보호 되 고 DMARC 구현의 영향을 이해를 격리 정책을 구현할 수 있습니다. 격리 정책은 해당 정책이 격리로 설정 된 DMARC TXT 레코드입니다 (p = 격리). 이 작업을 수행 하 여 고객의 받은 편지함 대신 스팸 폴더에 해당 하는 로컬에 DMARC에 실패 하는 도메인의 메시지를 저장할 DMARC 수신기가 요청 됩니다.
    
3. 요청 외부 메일 시스템 DMARC 실패 하는 메시지를 허용 하지 않습니다
    
    마지막 단계 거부 정책을 구현 됩니다. 거부 정책은 해당 정책을 거부로 설정한 DMARC TXT 레코드입니다 (p = 거부). 이 작업을 수행 하면 것을 요청 하지 DMARC 검사에 실패 하는 메시지를 수락 하려면 DMARC 수신기 합니다. 
    
## <a name="how-office-365-handles-outbound-email-that-fails-dmarc"></a>Office 365 DMARC 실패 하는 아웃 바운드 전자 메일을 처리 하는 방법
<a name="outbounddmarcfail"> </a>

메시지는 Office 365에서 아웃 바운드 DMARC, 실패 하 고 정책을 p를 설정한 경우 = 격리 또는 p = 거부, 메시지는 [아웃 바운드 메시지 용 위험성이 높은 배달 풀](high-risk-delivery-pool-for-outbound-messages.md)을 통해 라우팅됩니다. 아웃 바운드 전자 메일에 대 한 재정의 하지 않음
  
DMARC 거부 정책을 게시 하는 경우 (p 거부 =), 메시지 서비스를 통해 아웃 바운드 메시지를 릴레이 하는 경우 도메인에 대 한 SPF 또는 DKIM를 전달할 수 없기 때문에 없는 다른 고객 Office 365에서 도메인을 스푸핑할 수 있습니다. 그러나 DMARC 거부 정책 게시를 수행 하는 경우 하지 않은 모든 전자 메일의 인증 된 Office 365를 통해 그 중 일부를 (위에서 설명한 대로), 인바운드 전자 메일에 대 한 스팸으로 표시 될 수 있습니다 또는 SPF 게시 및 릴레이 통해 아웃 바운드 시도 수행 하는 경우 거부 됨 서비스입니다. 이런 등 서버와 DMARC TXT 레코드를 형성 하는 경우 도메인을 대신 하 여 메일을 보내는 응용 프로그램에 대 한 IP 주소 중 일부를 포함 하도록 잊어버린 경우.
  
## <a name="how-office-365-handles-inbound-email-that-fails-dmarc"></a>Office 365 DMARC 실패 하는 인바운드 전자 메일을 처리 하는 방법
<a name="inbounddmarcfail"> </a>

보내는 서버에 대 한 DMARC 정책은 p = 거부, EOP 스팸이 작업을 거부 하는 대신 메시지를 표시 합니다. 즉, 인바운드 전자 메일을 Office 365에서 p = 거부 및 p = 격리 동일한 방식으로 합니다.
  
Office 365 일부 합법적인 전자 메일 DMARC 실패할 수 있으므로 다음과 같이 구성 됩니다. 예, 다음 모든 목록 참가자에 게 메시지를 릴레이 하는 메일 그룹에 전송 된 경우 메시지 DMARC 실패할 수 있습니다. Office 365 이러한 메시지를 거부 하는 경우 사용자 수 합법적인 전자 메일 끊어지고 검색을 할 수 없습니다. 대신 이러한 메시지는 계속 DMARC 하지만 스팸으로 표시 및 거부 되지 것입니다. 필요한 경우 사용자가 여전히 얻을 수 이러한 메시지 받은 편지함에 이러한 메서드를 통해:
  
- 사용자가 수신 허용-보낸사람을 개별적으로 추가 자신의 전자 메일 클라이언트를 사용 하 여
    
- 관리자가 해당 특정 보낸사람에 대 한 메시지를 허용 하는 모든 사용자에 대 한 (ETR)는 Exchange 전송 규칙을 만듭니다. 
    
## <a name="troubleshooting-your-dmarc-implementation"></a>DMARC 구현 문제해결
<a name="dmarctroubleshoot"> </a>

EOP는 첫번째 항목 하지 도메인의 MX 레코드를 구성 해 둔 DMARC 오류 도메인에 대해 적용 되지 않습니다. 
  
Office 365 고객 도메인의 기본 MX 레코드가 EOP를 가리키지 않을 경우에 DMARC의 장점을 부여 되지 않습니다. 예, 온-프레미스 메일 서버로 MX 레코드를 가리킨 다음 커넥터를 사용 하 여 EOP로 전자 메일을 라우팅하는 경우 DMARC 작동 하지 않습니다. 이 시나리오에서 받는 도메인을 사용 하 여 허용 도메인 중 하나가 EOP 아니지만 기본 MX 합니다. 예: contoso.com의 MX 자체에서 가리키는으로 사용 하 여 EOP 보조 MX 레코드를, 인스턴트 메시징 세션 contoso.com의 MX 레코드는 다음과 같습니다.
  
```
contoso.com     3600   IN  MX  0  mail.contoso.com
contoso.com     3600   IN  MX  10 contoso-com.mail.protection.outlook.com

```

기본 MX 이며 EOP로 메일 라우팅됩니다 다음 이후 모두 또는 대부분, 전자 메일에는 mail.contoso.com 먼저 라우팅되는 합니다. 경우에 따라 전혀 MX 레코드를으로 EOP를 나열 하 고 전자 메일을 라우팅하는 커넥터를 간단 하 게 연결할 아니더라도 될 수 있습니다. EOP 해야할 필요가 DMARC 유효성 검사에 대 한 첫번째 항목을 사용할 필요가 없습니다. 방금 모든 온-프레미스/비-o 365 서버 DMARC 검사는 특정 수 없습니다는 유효성 검사를 보장 합니다.  DMARC는 고객의 도메인 (서버가 아님)에 대 한 적용 하 여이 가능한 경우 DMARC TXT 레코드를 설정 하지만 실제로 적용을 수행 하는 받는 서버 달려있습니다.  받는 서버와 EOP를 설정 하는 경우 EOP DMARC 적용을 수행 합니다.

  
## <a name="for-more-information"></a>자세한 내용
<a name="sectionSection8"> </a>

DMARC 하는 방법에 대 한 자세한 내용은 지 여부 이러한 리소스 수 있습니다.
  
- [스팸 방지 메시지 헤더](anti-spam-message-headers.md) DMARC 확인을 위한 Office 365에서 사용 되는 구문과 헤더 필드를 포함 합니다. 
    
- M <sup>3</sup>AAWG (메시징, 맬웨어, 모바일 방지 오용 작업 그룹)에서 [DMARC 교육 시리즈](https://www.m3aawg.org/activities/training/dmarc-training-series) 를 수행 합니다.
    
- [Dmarcian](https://space.dmarcian.com/deployment/)에서 검사 목록을 사용 합니다.
    
- [DMARC.org](https://dmarc.org)에서 원본에 직접 이동 합니다.
    
## <a name="see-also"></a>참고 항목
<a name="sectionSection8"> </a>

[Office 365 스푸핑 방지 하기 위해 보낸 사람이 정책 프레임 워크 (SPF)을 사용 하는 방법](how-office-365-uses-spf-to-prevent-spoofing.md)
  
[스푸핑을 방지할 수 있도록 Office 365에서 SPF 설정](set-up-spf-in-office-365-to-help-prevent-spoofing.md)
  
[DKIM를 사용 하 여 Office 365에서 사용자 지정 도메인에서 보낸 아웃 바운드 전자 메일의 유효성을 검사 하려면](use-dkim-to-validate-outbound-email.md)

