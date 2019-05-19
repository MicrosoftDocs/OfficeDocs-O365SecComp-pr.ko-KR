---
title: DMARC을 사용 하 여 Office 365의 전자 메일 유효성 검사
ms.author: tracyp
author: MSFTTracyP
manager: laurawi
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 4a05898c-b8e4-4eab-bd70-ee912e349737
ms.collection:
- M365-security-compliance
description: Office 365 조직에서 보낸 메시지의 유효성을 검사 하기 위해 도메인 기반 메시지 인증, 보고 및 적합성 (DMARC)을 구성 하는 방법을 알아봅니다.
ms.openlocfilehash: 9e3c2cd21e411d775f621c8b353bee9e6b0e235e
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/17/2019
ms.locfileid: "34156190"
---
# <a name="use-dmarc-to-validate-email-in-office-365"></a>DMARC을 사용 하 여 Office 365의 전자 메일 유효성 검사

도메인 기반 메시지 인증, 보고 및 적합성 ([DMARC](https://dmarc.org))은 SPF (Sender Policy Framework) 및 Dkim (보낸 사람 정책 프레임 워크)을 사용 하 여 메일 보낸 사람을 인증 하 고 대상 전자 메일 시스템에서 보낸 메시지를 신뢰 하는지 확인 합니다. 도메인 SPF 및 DKIM을 사용 하 여 DMARC을 구현 하면 스푸핑 및 피싱 전자 메일에 대 한 추가 보호가 제공 됩니다. DMARC 메일 시스템 수신에 도움이 됩니다. 도메인에서 전송 된 메시지를 사용 하 여 수행 해야 하는 작업 (SPF 또는 DKIM 검사 실패)을 결정 합니다.
  
## <a name="how-do-spf-and-dmarc-work-together-to-protect-email-in-office-365"></a>SPF 및 DMARC이 함께 Office 365의 전자 메일을 보호 하는 방법
<a name="SPFandDMARC"> </a>

 전자 메일 메시지에는 보낸 사람 또는 보낸 사람의 주소가 여러 개 포함 될 수 있습니다. 이러한 주소는 용도가 다른 용도로 사용 됩니다. 예를 들어 다음 주소를 고려 하십시오. 
  
- **"Mail From" 주소**: 보낸 사람을 식별 하 고 배달 못 함 알림과 같이 메시지를 배달 하는 동안 문제가 발생 한 경우 반환 알림을 보낼 위치를 지정 합니다. 전자 메일 메시지의 봉투 부분에 표시 되며 일반적으로 전자 메일 응용 프로그램에서 표시 되지 않습니다. 이를 5321 보낸 사람 주소 또는 역 경로 주소 라고도 합니다.
    
- **"보낸 사람" 주소**: 메일 응용 프로그램에서 보낸 사람 주소로 표시 되는 주소입니다. 이 주소는 전자 메일의 작성자를 식별 합니다. 즉, 메시지 작성을 담당 하는 사람이 나 시스템의 사서함입니다. 이를 5322.from 주소의 주소 라고도 합니다.
    
SPF에서는 DNS TXT 레코드를 사용 하 여 지정 된 도메인에 대해 권한이 부여 된 IP 주소 목록을 제공 합니다. 일반적으로 SPF 확인은 5321 보낸 사람 주소에 대해서만 수행 됩니다. 즉, SPF를 단독으로 사용 하는 경우 5322.from 주소의 주소가 인증 되지 않습니다. 이를 통해 사용자가 SPF 확인을 통과 하지만 스푸핑된 5322.from 주소의 보낸 사람 주소를 갖는 메시지를 받을 수 있습니다. 예를 들어 다음과 같은 SMTP 녹음을 고려해 보십시오.
  
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

이 대화 내용에서 보낸 사람 주소는 다음과 같습니다.
  
- 메일 보낸 사람 주소 (5321): phish@phishing.contoso.com
    
- 보낸 사람 주소 (5322.from 주소의): security@woodgrovebank.com
    
SPF를 구성한 경우 받는 서버는 주소 phish@phishing.contoso.com에서 메일을 확인 합니다. 메시지가 phishing.contoso.com 도메인에 대 한 유효한 원본에서 보낸 경우 SPF 확인이 통과 됩니다. 전자 메일 클라이언트는 보낸 사람 주소만 표시 하기 때문에 사용자는이 메시지를 security@woodgrovebank.com에서 보낸 것을 볼 수 있습니다. SPF만을 사용 하는 경우 woodgrovebank.com의 유효성은 인증 되지 않았습니다.
  
DMARC을 사용 하는 경우 받는 서버는 보낸 사람 주소에 대해서도 확인을 수행 합니다. 위 예에서 woodgrovebank.com에 대 한 DMARC TXT 레코드가 있는 경우에는 보낸 사람 주소에 대 한 확인이 실패 합니다.
  
## <a name="what-is-a-dmarc-txt-record"></a>DMARC TXT 레코드 란?
<a name="WhatisDMARC"> </a>

SPF의 DNS 레코드와 마찬가지로 DMARC의 레코드는 스푸핑 및 피싱을 방지 하는 데 도움이 되는 DNS 텍스트 (TXT) 레코드입니다. DMARC TXT 레코드를 DNS에 게시 합니다. DMARC TXT 레코드는 보내는 도메인의와 대조 소유자에 대해 전자 메일 작성자의 IP 주소를 확인 하 여 전자 메일 메시지의 출처를 확인 합니다. DMARC TXT 레코드는 권한 있는 아웃 바운드 전자 메일 서버를 식별 합니다. 그러면 대상 전자 메일 시스템에서 권한이 부여 된 아웃 바운드 전자 메일 서버 로부터 받는 메시지가 수신 되는지 확인할 수 있습니다.
  
Microsoft의 DMARC TXT 레코드는 다음과 같이 표시 됩니다.
  
```
_dmarc.microsoft.com.   3600    IN      TXT     "v=DMARC1; p=none; pct=100; rua=mailto:d@rua.agari.com; ruf=mailto:d@ruf.agari.com; fo=1" 
```

Microsoft는 DMARC 보고서를 [Agari](https://agari.com), 타사로 보냅니다. Agari DMARC 보고서를 수집 하 고 분석 합니다.
  
## <a name="implement-dmarc-for-inbound-mail"></a>인바운드 메일용 DMARC 구현
<a name="implementDMARCinbound"> </a>

Office 365에서 받은 메일에 대해 DMARC을 설정 하는 작업을 수행할 필요가 없습니다. Microsoft에서는 모든 것을 자동으로 처리 합니다. DMARC 검사를 통과 하지 못한 메일에 대 한 자세한 내용은 [Office 365에서 DMARC에 오류가 발생 한 인바운드 전자 메일을 처리 하는 방법을](use-dmarc-to-validate-email.md#inbounddmarcfail)참조 하십시오.
  
## <a name="implement-dmarc-for-outbound-mail-from-office-365"></a>Office 365에서 아웃 바운드 메일용 DMARC 구현
<a name="implementDMARCoutbound"> </a>

Office 365를 사용 하지만 사용자 지정 도메인을 사용 하지 않는 경우, 즉 onmicrosoft.com를 사용 하는 경우에는 조직에 대해 DMARC을 구성 하거나 구현 하기 위해 다른 작업을 수행할 필요가 없습니다. SPF가 이미 설정 되어 있으며 Office 365에서는 보내는 메일에 대해 DKIM 서명을 자동으로 생성 합니다. 이 서명에 대 한 자세한 내용은 [DKIM 및 Office 365에 대 한 기본 동작](use-dkim-to-validate-outbound-email.md#DefaultDKIMbehavior)을 참조 하세요.
  
 사용자 지정 도메인이 있거나 Office 365 외에도 온-프레미스 Exchange 서버를 사용 하는 경우 아웃 바운드 메일에 대해 DMARC를 수동으로 구현 해야 합니다. 사용자 지정 도메인에 대해 DMARC을 구현 하는 단계는 다음과 같습니다. 
  
- [1 단계: 도메인에 대 한 유효한 메일 원본 식별](use-dmarc-to-validate-email.md#IdentifyValidSources)
    
- [2 단계: Office 365에서 도메인에 대 한 SPF 설정](use-dmarc-to-validate-email.md#ConfigSPF)
    
- [3 단계: Office 365에서 사용자 지정 도메인에 대 한 DKIM을 설정 합니다.](use-dmarc-to-validate-email.md#ConfigDKIM)
    
- [4 단계: Office 365에서 도메인에 대 한 DMARC TXT 레코드를 구성 합니다.](use-dmarc-to-validate-email.md#CreateDMARCRecord)
    
### <a name="step-1-identify-valid-sources-of-mail-for-your-domain"></a>1 단계: 도메인에 대 한 유효한 메일 원본 식별
<a name="IdentifyValidSources"> </a>

SPF를 이미 설정한 경우에는이 연습이 이미 진행 된 것입니다. 그러나 DMARC의 경우에는 추가적인 고려 사항이 있습니다. 도메인의 메일 원본을 확인할 때 다음 두 가지 사항을 확인 해야 합니다.
  
- 어떤 IP 주소가 내 도메인에서 메시지를 전송 하나요?
    
- 제 3 자가 사용자를 대신 하 여 보낸 메일의 경우 5321 From 및 5322.from 주소의가 일치 합니까?
    
### <a name="step-2-set-up-spf-for-your-domain-in-office-365"></a>2 단계: Office 365에서 도메인에 대 한 SPF 설정
<a name="ConfigSPF"> </a>

이제 유효한 모든 보낸 사람 목록을 만들었으므로 [Office 365에서 SPF를 설정](set-up-spf-in-office-365-to-help-prevent-spoofing.md)하는 단계를 수행 하 여 스푸핑을 방지할 수 있습니다.
  
예를 들어 contoso.com가 Exchange Online에서 메일을 보내고 ip 주소가 192.168.0.1 인 온-프레미스 Exchange 서버와 IP 주소가 192.168.100.100 인 웹 응용 프로그램의 경우 SPF TXT 레코드는 다음과 같이 표시 됩니다.
  
```
contoso.com  IN  TXT  " v=spf1 ip4:192.168.0.1 ip4:192.168.100.100 include:spf.protection.outlook.com -all"
```

최상의 방법으로 SPF TXT 레코드가 타사 보낸 사람에 게 고려 되는지 확인 합니다.
  
### <a name="step-3-set-up-dkim-for-your-custom-domain-in-office-365"></a>3 단계: Office 365에서 사용자 지정 도메인에 대 한 DKIM을 설정 합니다.
<a name="ConfigDKIM"> </a>

SPF를 설정한 후에는 DKIM을 설정 해야 합니다. DKIM을 사용 하 여 메시지 헤더에 전자 메일 메시지에 디지털 서명을 추가할 수 있습니다. DKIM을 설정 하지 않고 Office 365이 도메인에 기본 DKIM 구성을 사용 하도록 허용 하는 경우 DMARC이 실패할 수 있습니다. 이는 기본 DKIM 구성에서 사용자 지정 도메인이 아닌 초기 onmicrosoft.com 도메인을 5322.from 주소의 주소로 사용 하기 때문입니다. 이로 인해 도메인에서 보낸 모든 전자 메일의 5321와 5322.from 주소의 간의 불일치가 발생 합니다.
  
사용자를 대신 하 여 메일을 전송 하는 타사 보낸 사람이 있는 경우 해당 전자 메일에 대해 5321 From 및 5322.from 주소의에서 DMARC가 일치 하지 않습니다. 이를 방지 하려면 제 3 자 보낸 사람과 특별히 도메인에 대해 DKIM을 설정 해야 합니다. 이를 통해 Office 365이 타사 서비스에서 전자 메일을 인증할 수 있습니다. 그러나 Yahoo, Gmail 및 Comcast와 같은 다른 사람도 사용자가 보낸 전자 메일 인 것 처럼 타사에서 보낸 전자 메일을 확인할 수 있습니다. 이렇게 하면 고객이 사서함의 위치에 관계 없이 사용자의 도메인에 대 한 신뢰를 작성할 수 있으며, 마찬가지로 Office 365은 도메인에 대 한 인증 확인을 통과 하므로 위장으로 인해 메시지를 스팸으로 표시 하지 않습니다.
  
타사에서 도메인을 스푸핑할 수 있도록 DKIM을 설정 하는 방법을 비롯 하 여 도메인에 대 한 DKIM을 설정 하는 방법에 대 한 자세한 내용은 [USE DKIM을 사용 하 여 Office 365의 사용자 지정 도메인에서 보낸 아웃 바운드 전자 메일의 유효성 검사](use-dkim-to-validate-outbound-email.md)를 참조 하세요.
  
### <a name="step-4-form-the-dmarc-txt-record-for-your-domain-in-office-365"></a>4 단계: Office 365에서 도메인에 대 한 DMARC TXT 레코드를 구성 합니다.
<a name="CreateDMARCRecord"> </a>

여기에 나와 있지 않은 다른 구문 옵션도 있지만 Office 365에서 가장 일반적으로 사용 되는 옵션은 다음과 같습니다. 도메인에 대 한 DMARC TXT 레코드를 다음 형식으로 구성 합니다.
  
```
_dmarc.domain  TTL  IN  TXT  "v=DMARC1; pct=100; p=policy"
```

여기서 각 부분이 나타내는 의미는 다음과 같습니다.
  
- *domain* 은 보호 하려는 도메인입니다. 기본적으로 레코드는 도메인과 모든 하위 도메인의 메일을 보호 합니다. 예를 들어 dmarc.contoso.com를 지정 \_하는 경우 dmarc은 도메인 및 housewares.contoso.com 또는 plumbing.contoso.com와 같은 모든 하위 도메인과의 메일을 보호 합니다. 
    
- *TTL* 은 항상 1 시간에 해당 합니다. TTL에 사용 되는 단위는 시간 (1 시간), 분 (60 분) 또는 초 (3600 초)는 도메인의 등록자에 따라 달라 집니다. 
    
- *pct = 100* 은이 규칙을 전자 메일의 100%에 사용 해야 함을 나타냅니다.
    
- *정책은* DMARC에 오류가 발생 했을 때 수신 서버가 수행 하도록 할 정책을 지정 합니다. 정책을 없음, 격리 또는 거부로 설정할 수 있습니다. 
    
사용할 옵션에 대 한 자세한 내용은 [Office 365에서 DMARC을 구현 하기 위한 모범 사례](use-dmarc-to-validate-email.md#DMARCbestpractices)에 대 한 개념을 익힙니다.
  
예제:
  
- 정책이 없음으로 설정
  
    ```
    _dmarc.contoso.com 3600 IN  TXT  "v=DMARC1; p=none"
    ```

- 격리로 설정 되는 정책
  
    ```
    _dmarc.contoso.com 3600 IN  TXT  "v=DMARC1; p=quarantine"
    ```

- 거부로 설정 되는 정책
  
    ```
    _dmarc.contoso.com  3600 IN  TXT  "v=DMARC1; p=reject"
    ```

레코드를 구성한 후에는 도메인 등록 기관에서 레코드를 업데이트 해야 합니다. DMARC TXT 레코드를 Office 365의 DNS 레코드에 추가 하는 방법에 대 한 자세한 내용은 [dns 레코드를 관리할 때 office 365에 대 한 dns 레코드 만들기](https://support.office.com/article/b0f3fdca-8a80-4e8e-9ef3-61e8a2a9ab23)를 참조 하십시오.
  
## <a name="best-practices-for-implementing-dmarc-in-office-365"></a>Office 365에서 DMARC을 구현 하기 위한 최상의 방법
<a name="DMARCbestpractices"> </a>

나머지 메일 흐름에 영향을 주지 않고 DMARC을 점차적으로 구현할 수 있습니다. 다음 단계를 수행 하는 롤아웃 계획을 만들고 구현 합니다. 다음 단계를 진행 하기 전에 먼저 각 단계를 하위 도메인, 다른 하위 도메인, 그리고 마지막으로 조직의 최상위 도메인으로 이동 합니다.
  
1. DMARC 구현에 따른 영향 모니터링
    
    DMARC 수신기에 게 해당 도메인을 사용 하 여 표시 되는 메시지에 대 한 통계를 보내도록 요청 하는 하위 도메인 또는 도메인에 대 한 간단한 모니터링 모드 레코드를 사용 하 여 시작 합니다. 모니터링 모드 레코드는 정책이 없음 (p = 없음)으로 설정 된 DMARC TXT 레코드입니다. 많은 회사에서는 보다 제한적인 DMARC 정책을 게시 하 여 손실 될 수 있는 전자 메일의 크기를 확실히 알지 못하기 때문에 DMARC TXT 레코드를 p = 없음으로 게시 합니다. 
    
    메시징 인프라에서 SPF 또는 DKIM을 구현한 후에도이 작업을 수행할 수 있습니다. 그러나 SPF 및 DKIM을 구현 하기 전 까지는 DMARC를 사용 하 여 메일을 효과적으로 격리 하거나 거부할 수 없습니다. SPF 및 DKIM을 도입 하는 경우 DMARC를 통해 생성 된 보고서는 이러한 검사를 통과 하는 메시지의 수와 원본을 제공 합니다. 합법적인 트래픽의 범위를 쉽게 확인 하 고 처리 하지 못하는 문제를 해결할 수 있습니다. 또한 보내는 사기 메시지 수 및 해당 위치에서 시작 합니다.
    
2. DMARC에서 실패 한 메일을 외부 메일 시스템에서 격리 하도록 요청
    
    모든 또는 대부분의 합법적인 트래픽이 SPF 및 DKIM에 의해 보호 되 고 있다고 생각 하 고 DMARC 구현의 영향을 이해 하면 격리 정책을 구현할 수 있습니다. 격리 정책은 정책이 격리 (p = 격리)로 설정 된 DMARC TXT 레코드입니다. 이 작업을 수행 하는 경우 DMARC 수신기가 DMARC에 오류가 발생 하는 메시지를 고객의 받은 편지함 대신 스팸 폴더의 로컬에 저장 합니다.
    
3. DMARC에 실패 한 메시지를 허용 하지 않도록 외부 메일 시스템에 요청
    
    마지막 단계는 거부 정책을 구현 하는 것입니다. 거부 정책은 정책이 거부로 설정 된 (p = 거부) DMARC TXT 레코드입니다. 이 작업을 수행 하면 DMARC 수신자에 게 DMARC 검사를 통과 하지 못한 메시지를 수락 하지 않도록 요청 합니다. 
    
## <a name="how-office-365-handles-outbound-email-that-fails-dmarc"></a>Office 365에서 DMARC에 실패 한 아웃 바운드 전자 메일을 처리 하는 방법
<a name="outbounddmarcfail"> </a>

메시지가 Office 365에서 아웃 바운드이 고 DMARC에 오류가 발생 하 여 정책을 p = 격리 또는 p = 거부로 설정한 경우 메시지가 [높은 위험 배달 풀을 통해 아웃 바운드 메시지에 대해](high-risk-delivery-pool-for-outbound-messages.md)라우팅됩니다. 아웃 바운드 전자 메일에 대 한 재정의는 없습니다.
  
DMARC 거부 정책 (p = 거부)을 게시 하는 경우, 메시지는 서비스를 통해 아웃 바운드 메시지를 릴레이할 때 도메인에 대해 SPF 또는 DKIM을 전달할 수 없으므로, Office 365의 다른 고객은 도메인을 스푸핑할 수 없습니다. 그러나 DMARC 거부 정책을 게시 하지만 Office 365을 통해 전자 메일을 모두 인증 하지 않은 경우, 일부 it는 인바운드 전자 메일 (위에 설명한)에 대 한 스팸으로 표시 될 수도 있고, SPF를 게시 하지 않은 경우에는 거부 될 수 있습니다. 서비스입니다. 예를 들어 DMARC TXT 레코드를 형성할 때 도메인을 대신 하 여 메일을 보내는 서버 및 응용 프로그램의 일부 IP 주소를 포함 하는 것을 잊은 경우 이러한 상황이 발생 합니다.
  
## <a name="how-office-365-handles-inbound-email-that-fails-dmarc"></a>Office 365에서 DMARC에 실패 한 인바운드 전자 메일을 처리 하는 방법
<a name="inbounddmarcfail"> </a>

보내는 서버의 DMARC 정책이 p = 거부 인 경우 EOP는 메시지를 거부 하는 대신 스팸으로 표시 합니다. 즉, 인바운드 전자 메일의 경우 Office 365에서는 p = 거부 및 p = 격리를 동일한 방식으로 처리 합니다.
  
일부 합법적인 전자 메일이 DMARC에 실패할 수 있으므로 Office 365는 이와 같이 구성 됩니다. 예를 들어 메시지를 메일 그룹으로 보낸 후 모든 목록 참가자로 메시지를 릴레이 하면 DMARC에 오류가 발생할 수 있습니다. Office 365에서 이러한 메시지를 거부 한 경우 사용자는 합법적인 전자 메일을 잃어 버릴 수 없습니다. 대신, 이러한 메시지는 계속 해 서 DMARC에 실패 하지만, 거부 되지 않고 스팸으로 표시 됩니다. 원하는 경우 사용자는 다음 방법을 통해 받은 편지함에 이러한 메시지를 받을 수 있습니다.
  
- 사용자가 전자 메일 클라이언트를 사용 하 여 개별적으로 수신 허용-보낸 사람 추가
    
- 관리자는 특정 보낸 사람에 대 한 메시지를 허용 하는 모든 사용자에 대해 Exchange 메일 흐름 규칙 (전송 규칙이 라고도 함)을 만듭니다. 
    
## <a name="troubleshooting-your-dmarc-implementation"></a>DMARC 구현 문제 해결
<a name="dmarctroubleshoot"> </a>

EOP가 첫 번째 항목이 아닌 경우 도메인의 MX 레코드를 구성한 경우 DMARC 오류가 도메인에 적용 되지 않습니다. 
  
사용자가 Office 365 고객이 고 도메인의 기본 MX 레코드가 EOP를 가리키지 않는 경우 DMARC의 이점을 얻을 수 없습니다. 예를 들어 MX 레코드를 온-프레미스 메일 서버에 DMARC 다음 커넥터를 사용 하 여 EOP에 전자 메일을 라우팅하는 경우에는 작동 하지 않습니다. 이 시나리오에서 받는 도메인은 허용 도메인 중 하나이 고 EOP는 기본 MX가 아닙니다. 예를 들어 contoso.com에서 자체 MX를 가리키고 EOP를 보조 MX 레코드로 사용 한다고 가정해 보겠습니다.
  
```
contoso.com     3600   IN  MX  0  mail.contoso.com
contoso.com     3600   IN  MX  10 contoso-com.mail.protection.outlook.com
```

전체 또는 대부분의 전자 메일은 기본 MX 이기 때문에 먼저 mail.contoso.com로 라우팅되고, 메일은 EOP로 라우팅됩니다. 어떤 경우에는 EOP를 MX 레코드로 나열 하지 않고 단순히 커넥터를 연결 하 여 전자 메일을 라우팅하도록 할 수도 있습니다. EOP는 DMARC 유효성 검사를 수행 하기 위해 첫 번째 항목 일 필요는 없습니다. 모든 온-프레미스/비 O365 서버가 DMARC 검사를 수행 하는 것은 확실 하지 않으므로 유효성 검사를 확인 하기만 하면 됩니다.  DMARC는 DMARC TXT 레코드를 설정할 때 고객의 도메인 (서버 아님)에 적용할 수 있지만 실제로 적용을 수행 하기 위해 받는 서버로 작동 합니다.  EOP을 받는 서버로 설정 하는 경우 EOP는 DMARC 적용을 수행 합니다.
  
## <a name="for-more-information"></a>자세한 내용
<a name="sectionSection8"> </a>

DMARC에 대 한 자세한 정보를 원하십니까? 이러한 리소스를 통해 도움이 될 수 있습니다.
  
- [스팸 방지 메시지 헤더](anti-spam-message-headers.md) 에는 DMARC 검사를 위해 Office 365에서 사용 하는 구문 및 헤더 필드가 포함 되어 있습니다. 
    
- M <sup>3</sup>aawg (메시징, 맬웨어, 모바일 남용 작업 그룹)에서 [DMARC 교육 시리즈](https://www.m3aawg.org/activities/training/dmarc-training-series) 를 이용 합니다.
    
- [Dmarcian](https://space.dmarcian.com/deployment/)에서 검사 목록을 사용 합니다.
    
- [DMARC.org](https://dmarc.org)에서 원본으로 직접 이동 합니다.
    
## <a name="see-also"></a>참고 항목
<a name="sectionSection8"> </a>

[Office 365에서 SPF (Sender Policy Framework)를 사용 하 여 스푸핑을 방지 하는 방법](how-office-365-uses-spf-to-prevent-spoofing.md)
  
[스푸핑을 방지할 수 있도록 Office 365에서 SPF 설정](set-up-spf-in-office-365-to-help-prevent-spoofing.md)
  
[DKIM을 사용 하 여 Office 365의 사용자 지정 도메인에서 전송 되는 아웃 바운드 전자 메일의 유효성 검사](use-dkim-to-validate-outbound-email.md)

