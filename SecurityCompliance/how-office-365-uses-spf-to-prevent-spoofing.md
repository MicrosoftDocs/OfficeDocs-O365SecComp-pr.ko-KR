---
title: Office 365에서 SPF (Sender Policy Framework)를 사용 하 여 스푸핑을 방지 하는 방법
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 12/15/2016
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 3aff33c5-1416-4867-a23b-e0c0c5b4d2be
description: 요약:이 문서에서는 Office 365에서 DNS의 SPF (Sender Policy Framework) TXT 레코드를 사용 하 여 대상 전자 메일 시스템이 사용자 지정 도메인에서 보낸 메시지를 신뢰 하는지 확인 하는 방법을 설명 합니다. 이는 Office 365에서 보내는 아웃 바운드 메일에 적용 됩니다. office 365에서 office 365 내의 받는 사람에 게 전송 되는 메시지는 항상 SPF를 통과 합니다.
ms.openlocfilehash: b4898bf8b607e7ad600455c915f99baaab21f6f6
ms.sourcegitcommit: a80bd8626720fabdf592b84e4424cd3a83d08280
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30223567"
---
# <a name="how-office-365-uses-sender-policy-framework-spf-to-prevent-spoofing"></a>Office 365에서 SPF (Sender Policy Framework)를 사용 하 여 스푸핑을 방지 하는 방법

 **요약:** 이 문서에서는 Office 365에서 DNS의 SPF (Sender Policy Framework) TXT 레코드를 사용 하 여 대상 전자 메일 시스템이 사용자 지정 도메인에서 보낸 메시지를 신뢰 하는지 확인 하는 방법에 대해 설명 합니다. 이는 Office 365에서 보내는 아웃 바운드 메일에 적용 됩니다. office 365에서 office 365 내의 받는 사람에 게 전송 되는 메시지는 항상 SPF를 통과 합니다. 
  
SPF TXT 레코드는 전자 메일 메시지를 보낸 도메인 이름을 확인 하 여 스푸핑 및 피싱을 방지 하는 데 도움이 되는 DNS 레코드입니다. SPF는 보내는 도메인의와 대조 소유자에 대해 보낸 사람의 IP 주소를 확인 하 여 전자 메일 메시지의 출처를 확인 합니다. 
  
> [!NOTE]
> SPF 레코드 유형은 2014의 IETF (인터넷 엔지니어링 작업)에서 더 이상 사용 되지 않습니다. 대신 DNS에서 TXT 레코드를 사용 하 여 SPF 정보를 게시 해야 합니다. 이 문서의 나머지 부분에서는 명확성을 위해 SPF TXT 레코드 용어를 사용 합니다. 
  
도메인 관리자는 DNS의 TXT 레코드에 SPF 정보를 게시 합니다. SPF 정보는 권한 있는 아웃 바운드 전자 메일 서버를 식별 합니다. 대상 전자 메일 시스템 인증 된 아웃 바운드 전자 메일 서버에서 보낸 메시지를 확인 합니다. spf에 이미 익숙한 경우 또는 간단한 배포를 수행 하 고 office 365 용 DNS에서 spf TXT 레코드에 포함할 사항을 확인 해야 하는 경우 [스푸핑 방지를 위해 office 365에서 spf를 설정할](set-up-spf-in-office-365-to-help-prevent-spoofing.md)수 있습니다. office 365에서 완전히 호스트 되는 배포가 없거나 spf 작동 방식에 대 한 자세한 정보나 Office 365에 대 한 spf 문제를 해결 하는 방법에 대 한 자세한 내용은 계속 읽어 보십시오.
  
> [!NOTE]
> 이전에는 SharePoint Online도 함께 사용 하는 경우 다른 SPF TXT 레코드를 사용자 지정 도메인에 추가 해야 했습니다. 더 이상 필요 하지 않습니다. 이렇게 변경 하면 SharePoint Online 알림 메시지가 정크 메일 폴더에서 끝나는 위험을 줄일 것입니다. 즉시 변경 작업을 수행할 필요가 없지만 "너무 많은 조회" 오류가 표시 되는 경우 [스푸핑을 방지 하기 위해 Office 365에서 설정 된 spf](set-up-spf-in-office-365-to-help-prevent-spoofing.md)에 설명 된 대로 spf TXT 레코드를 수정 합니다. 
     
## <a name="how-spf-works-to-prevent-spoofing-and-phishing-in-office-365"></a>SPF가 Office 365에서 스푸핑 및 피싱 문제를 방지 하는 방법
<a name="HowSPFWorks"> </a>

SPF는 보낸 사람이 도메인을 대신 하 여 메일을 보낼 수 있는지 여부를 결정 합니다. 보낸 사람이이 작업을 수행할 수 없는 경우 즉, 전자 메일이 받는 서버에서 SPF 확인을 통과 하지 못하는 경우 해당 서버에 구성 된 스팸 정책에 따라 메시지와 관련 하 여 수행 해야 하는 작업이 결정 됩니다.
  
각 spf txt 레코드에는 해당 레코드가 SPF txt 레코드이 고 도메인에서 메일을 보낼 수 있는 IP 주소, 도메인 대신 메시지를 보내도록 허용 되는 외부 도메인 및 적용 규칙 이라는 세 개의 부분이 포함 되어 있습니다. 유효한 SPF TXT 레코드에서는 3 개가 모두 필요 합니다. 이 문서에서는 SPF TXT 레코드를 작성 하는 방법에 대해 설명 하 고 Office 365에서 서비스 작업을 수행 하기 위한 모범 사례를 제공 합니다. 도메인 등록자를 사용 하 여 레코드를 DNS에 게시 하는 방법에 대 한 지침에 대 한 링크도 제공 됩니다.
  
### <a name="spf-basics-ip-addresses-allowed-to-send-from-your-custom-domain"></a>SPF 기본 사항: 사용자 지정 도메인에서 보낼 수 있는 IP 주소
<a name="SPFBasicsIPaddresses"> </a>

SPF 규칙에 대 한 기본 구문을 살펴보겠습니다.
  
v = spf1 \<IP\> \<적용 규칙\>
  
예를 들어 contoso.com에 대 한 다음과 같은 SPF 규칙이 있다고 가정해 보겠습니다.
  
v = spf1 \<ip 주소 #1\> \<ip 주소 #2\> \<ip 주소 #3\> \<적용 규칙\>
  
이 예에서 SPF 규칙은 받는 전자 메일 서버에 contoso.com 도메인에 대 한 이러한 IP 주소 로부터의 메일만 수락 하도록 지시 합니다.
  
- IP 주소 #1
    
- IP 주소 #2
    
- IP 주소 #3
    
이 SPF 규칙은 받는 전자 메일 서버에 게 메시지를 보내는 경우, 즉 이러한 세 가지 IP 주소 중 하나에서 보낸 메시지가 아닌 경우 받는 서버에서 메시지에 적용 규칙을 contoso.com 합니다. 적용 규칙은 일반적으로 다음 옵션 중 하나입니다.
  
- **하드 디스크에 오류가 발생 했습니다.** 메시지 봉투에 메시지를 ' hard fail '로 표시 한 다음이 유형의 메시지에 대해 받는 서버의 구성 된 스팸 정책을 따릅니다. 
    
- **소프트 오류가 발생 합니다.** 메시지 봉투에 ' 소프트 실패 ' 메시지를 표시 합니다. 일반적으로 전자 메일 서버는 이러한 메시지를 배달 하도록 구성 됩니다. 대부분의 최종 사용자에 게는이 표시가 표시 되지 않습니다. 
    
- **중립** 아무 작업도 하지 않고 메시지 봉투를 표시 하지 않습니다. 이 작업은 일반적으로 테스트 목적으로 예약 되어 있으며 거의 사용 되지 않습니다. 
    
다음 예에서는 여러 상황에서 SPF가 작동 하는 방식을 보여 줍니다. 이 예에서는 contoso.com가 보낸 사람 및 woodgrovebank.com가 수신자입니다.
  
### <a name="example-1-email-authentication-of-a-message-sent-directly-from-sender-to-receiver"></a>예 1: 보낸 사람이 받는 사람에 게 직접 전송 되는 메시지의 전자 메일 인증
<a name="spfExample1"> </a>

SPF는 보낸 사람에서 받는 사람으로의 경로가 direct와 같은 경우에 가장 적합 합니다.
  
![서버 간에 직접 전자 메일이 전송될 때 SPF에서 전자 메일을 인증하는 방법을 보여주는 다이어그램입니다.](media/835c20a7-ed4c-49c4-91fe-b8ebb3e452a1.jpg)
  
woodgrovebank.com에서 메시지를 수신 하는 경우 IP 주소 #1 contoso.com의 spf TXT 레코드에 있는 경우 메시지가 spf 확인을 통과 하 고 인증 됩니다.
  
### <a name="example-2-spoofed-sender-address-fails-the-spf-check"></a>예 2: 스푸핑된 보낸 사람 주소가 SPF 확인에 실패 함
<a name="spfExample2"> </a>

phisher에서 contoso.com을 스푸핑할 수 있는 방법을 찾는 경우를 가정해 보겠습니다.
  
![스푸핑된 서버에서 보낸 전자 메일을 SPF에서 인증하는 방법을 보여주는 다이어그램입니다.](media/235dac3d-cdc5-466e-86e0-37b5979de198.jpg)
  
IP 주소 #12는 contoso의 SPF TXT 레코드에 없으므로 메시지가 SPF 검사를 통과 하지 못하고 수신자가 해당 메시지를 스팸으로 표시 하도록 선택할 수 있습니다.
  
### <a name="example-3-spf-and-forwarded-messages"></a>예제 3: SPF 및 전달 메시지
<a name="spfExample3"> </a>

SPF의 한 가지 단점은 전자 메일이 전달 된 경우에도 작동 하지 않는다는 것입니다. 예를 들어 woodgrovebank.com의 사용자가 모든 전자 메일을 outlook.com 계정으로 보내도록 전달 규칙을 설정 했다고 가정 합니다.
  
![메시지가 전달될 때 SPF에서 전자 메일을 인증할 수 없는 상황을 보여주는 다이어그램입니다.](media/6e92acd6-463e-4a1b-8327-fb1cf861f356.jpg)
  
이 메시지는 원래 woodgrovebank.com에서 spf 검사를 통과 했지만, IP #25이 contoso의 spf TXT 레코드에 없기 때문에 outlook.com에서 spf 검사에 실패 했습니다. 그러면 Outlook.com에서 메시지를 스팸으로 표시할 수 있습니다. 이 문제를 해결 하려면 SPF를 dkim 및 DMARC 같은 다른 전자 메일 인증 방법과 함께 사용 합니다.
  
### <a name="spf-basics-including-third-party-domains-that-can-send-mail-on-behalf-of-your-domain"></a>SPF 기본 사항: 도메인을 대신 하 여 메일을 보낼 수 있는 타사 도메인을 포함 합니다.
<a name="SPFBasicsIncludes"> </a>

IP 주소 외에 도메인을 보낸 사람으로 포함 하도록 SPF TXT 레코드를 구성할 수도 있습니다. 이러한 기능은 SPF TXT 레코드에 "include" 문으로 추가 됩니다. 예를 들어 contoso.com는 contoso.net 및 contoso.org에서 메일 서버의 모든 IP 주소를 포함 하는 것이 좋습니다. 이 작업을 수행 하기 위해 contoso.com에서는 다음과 같은 SPF TXT 레코드를 게시 합니다.
  
```
IN TXT "v=spf1 include:contoso.net include:contoso.org -all"
```

받는 서버가 DNS에서이 레코드를 볼 때 contoso.net의 SPF TXT 레코드에 대 한 DNS 조회를 수행한 다음 contoso.org 용으로도이를 수행 합니다. contoso.net 또는 contoso.org에 대 한 레코드 내에 추가 포함 문을 찾으면이를 팔 로우 합니다. 서비스 거부 공격을 방지 하기 위해 단일 전자 메일 메시지에 대 한 최대 DNS 조회 수는 10 개입니다. 각 포함 문은 추가 DNS 조회를 나타냅니다. 메시지가 10 개 제한을 초과 하면 메시지가 SPF에 실패 합니다. 메시지가이 제한에 도달 하면 받는 서버가 구성 된 방식에 따라 보낸 사람에 게 "너무 많은 조회"가 생성 되었거나 메시지의 "최대 홉 수가 초과 되었습니다." 라는 메시지가 표시 될 수 있습니다. 이를 방지 하는 방법에 대 한 팁은 [문제 해결: Office 365에서 SPF에 대 한 모범 사례](how-office-365-uses-spf-to-prevent-spoofing.md#SPFTroubleshoot)를 참조 하세요.
  
## <a name="requirements-for-your-spf-txt-record-and-office-365"></a>SPF TXT 레코드 및 Office 365에 대 한 요구 사항
<a name="SPFReqsinO365"> </a>

Office 365을 설정할 때 메일을 설정 하는 경우 Microsoft 메시징 서버를 도메인에 대 한 합법적인 메일 원본으로 식별 하는 SPF TXT 레코드를 이미 만든 것입니다. 이 레코드는 다음과 같이 표시 될 수 있습니다.
  
```
v=spf1 include:spf.protection.outlook.com -all
```

완전히 호스팅된 Office 365 고객 인 경우 아웃 바운드 메일을 전송 하는 온-프레미스 메일 서버가 없으면 Office 365 용으로 게시 해야 하는 유일한 SPF TXT 레코드입니다.
  
하이브리드 배포를 수행 하는 경우 (예: 일부 사서함은 온-프레미스에 있고 일부는 Office 365에 호스트 됨), EOP (Exchange Online Protection) 독립 실행형 고객 인 경우 (즉, 조직에서 EOP를 사용 하 여 온-프레미스 사서함을 보호 하는 경우) 각 온-프레미스에 지 메일 서버에 대 한 아웃 바운드 IP 주소를 DNS의 SPF TXT 레코드에 추가 합니다.
  
## <a name="form-your-spf-txt-record-for-office-365"></a>Office 365에 대 한 SPF TXT 레코드를 구성 합니다.
<a name="FormYourSPF"> </a>

이 문서의 구문 정보를 사용 하 여 사용자 지정 도메인에 대 한 SPF TXT 레코드를 구성 합니다. 여기에 나와 있지 않은 다른 구문 옵션도 있지만 가장 일반적으로 사용 되는 옵션은 다음과 같습니다. 레코드를 구성한 후에는 도메인 등록 기관에서 레코드를 업데이트 해야 합니다.
  
Office 365에 대해 포함 해야 하는 도메인에 대 한 자세한 내용은 [SPF에 필요한 외부 DNS 레코드](https://support.office.com/article/External-Domain-Name-System-records-for-Office-365-c0531a6f-9e25-4f2d-ad0e-a70bfef09ac0?ui=en-US&amp;rs=en-US&amp;ad=US)를 참조 하세요. 도메인 등록 기관에 대 한 SPF (TXT) 레코드를 업데이트 하는 단계별 [지침](https://office.microsoft.com/en-us/office365-suite-help/create-dns-records-for-office-365-HA102851099.aspx?CTT=5&amp;origin=HA102818404) 을 사용 합니다. 등록 자가 나열 되지 않으면 레코드를 업데이트 하는 방법을 알아보려면 별도로 문의 해야 합니다. 
  
### <a name="spf-txt-record-syntax-for-office-365"></a>Office 365에 대 한 SPF TXT 레코드 구문
<a name="SPFSyntaxO365"> </a>

Office 365의 일반적인 SPF TXT 레코드는 다음 구문을 포함 합니다.
  
```
v=spf1 [<ip4>|<ip6>:<IP address>] [include:<domain name>] <enforcement rule>
```

예를 들면 다음과 같습니다.
  
```
v=spf1 ip4:192.168.0.1 ip4:192.168.0.2 include:spf.protection.outlook.com -all
```

여기서 각 부분이 나타내는 의미는 다음과 같습니다.
  
- **v = spf1** 가 필요 합니다. TXT 레코드를 SPF TXT 레코드로 정의 합니다. 
    
- **ip4** 는 IP 버전 4 주소를 사용 중임을 나타냅니다. **ip6** 는 IP 버전 6 주소를 사용 중임을 나타냅니다. IPv6 IP 주소를 사용 하는 경우이 문서의 예제에서 **ip4** with **ip6** 를 대체 합니다. 또한 **ip4:192.168.0.1/26**과 같이 CIDR 표기법을 사용 하 여 IP 주소 범위를 지정할 수도 있습니다.
    
-  _ip 주소_ 는 SPF TXT 레코드에 추가 하려는 ip 주소입니다. 일반적으로 조직에 대 한 아웃 바운드 메일 서버의 IP 주소입니다. 여러 아웃 바운드 메일 서버를 나열할 수 있습니다. 자세한 내용은 [예: SPF TXT record for a outbound 온-프레미스 메일 서버 및 Office 365](how-office-365-uses-spf-to-prevent-spoofing.md#ExampleSPFMultipleMailServerO365)을 참조 하세요.
    
-  _도메인 이름은_ 합법적인 보낸 사람으로 추가 하려는 도메인입니다. Office 365에 대해 포함 해야 하는 도메인 이름 목록은 [SPF에 필요한 외부 DNS 레코드](https://support.office.com/article/External-Domain-Name-System-records-for-Office-365-c0531a6f-9e25-4f2d-ad0e-a70bfef09ac0?ui=en-US&amp;rs=en-US&amp;ad=US)를 참조 하세요.
    
- 적용 규칙은 일반적으로 다음 중 하나입니다.
    
  - -모두
    
    하드 실패를 나타냅니다. 도메인에 대해 모든 권한이 부여 된 IP 주소를 알고 있는 경우 SPF TXT 레코드에이를 나열 하 고-all (hard fail) 한정자를 사용 합니다. 또한 SPF만 사용 하는 경우, 즉 DMARC 또는 dkim을 사용 하지 않는 경우에는-all 한정자를 사용 해야 합니다. 항상이 한정자를 사용 하는 것이 좋습니다.
    
  - ~ all
    
    소프트 장애를 나타냅니다. 전체 IP 주소 목록이 있는지 잘 모를 경우 ~ all (소프트 오류) 한정자를 사용 해야 합니다. 또한 p = 격리 또는 p = 거부와 함께 DMARC을 사용 하는 경우 ~ all을 사용할 수 있습니다. 그렇지 않으면-all을 사용 합니다.
    
  - ? all
    
    중립을 나타냅니다. 이는 SPF을 테스트할 때 사용 됩니다. 실제 배포에서는이 한정자를 사용 하지 않는 것이 좋습니다.
    
### <a name="example-spf-txt-record-to-use-when-all-of-your-mail-is-sent-by-office-365"></a>예: Office 365에서 모든 메일을 보낼 때 사용할 SPF TXT 레코드
<a name="ExampleSPFNoSP"> </a>

모든 메일이 Office 365에서 전송 되는 경우 SPF TXT 레코드에서 다음을 사용 합니다.
  
```
v=spf1 include:spf.protection.outlook.com -all
```

### <a name="example-spf-txt-record-for-a-hybrid-scenario-with-one-on-premises-exchange-server-and-office-365"></a>예: 단일 온-프레미스 Exchange Server 및 Office 365을 사용 하는 하이브리드 시나리오에 대 한 SPF TXT 레코드
<a name="ExampleSPFHybridOneExchangeServer"> </a>

하이브리드 환경에서 온-프레미스 Exchange 서버의 IP 주소가 192.168.0.1 이면 spf 적용 규칙을 하드 실패로 설정 하기 위해 spf TXT 레코드를 다음과 같이 구성 합니다.
  
```
v=spf1 ip4:192.168.0.1 include:spf.protection.outlook.com -all
```

### <a name="example-spf-txt-record-for-multiple-outbound-on-premises-mail-servers-and-office-365"></a>예: 여러 아웃 바운드 온-프레미스 메일 서버 및 Office 365에 대 한 SPF TXT 레코드
<a name="ExampleSPFMultipleMailServerO365"> </a>

아웃 바운드 메일 서버가 여러 개인 경우에는 각 메일 서버의 ip 주소를 SPF TXT 레코드에 포함 하 고 각 IP 주소를 공백으로 구분 하 고 "ip4:" 문을 입력 합니다. 예를 들어:
  
```
v=spf1 ip4:192.168.0.1 ip4:192.168.0.2 ip4:192.168.0.3 include:spf.protection.outlook.com -all
```

## <a name="next-steps-set-up-spf-for-office-365"></a>다음 단계: Office 365에 대 한 SPF 설정
<a name="SPFNextSteps"> </a>

SPF TXT 레코드를 만든 후에는 [스푸핑을 Set up the Office 365](set-up-spf-in-office-365-to-help-prevent-spoofing.md) 의 단계를 수행 하 여 스푸핑이 도메인에 추가 되지 않도록 합니다. 
  
spf는 스푸핑을 방지 하는 데 도움이 되지만 spf에서 보호할 수 없는 스푸핑 기법이 있습니다. 이를 방지 하기 위해 SPF를 설정한 후에는 Office 365에 대해 dkim 및 DMARC도 구성 해야 합니다. 시작 하려면 [dkim을 사용 하 여 Office 365의 사용자 지정 도메인에서 전송 되는 아웃 바운드 전자 메일의 유효성 검사](use-dkim-to-validate-outbound-email.md)를 참조 하세요. 그런 다음 [Office 365에서 DMARC을 사용 하 여 전자 메일의 유효성 검사를](use-dmarc-to-validate-email.md)참조 하세요.
  
## <a name="troubleshooting-best-practices-for-spf-in-office-365"></a>문제 해결: Office 365의 SPF에 대 한 모범 사례
<a name="SPFTroubleshoot"> </a>

사용자 지정 도메인에 대해 SPF TXT 레코드를 하나만 만들 수 있습니다. 여러 레코드를 만들면 라운드 로빈 상황이 발생 하 고 SPF가 실패 합니다. 이를 방지 하기 위해 각 하위 도메인에 대해 별도의 레코드를 만들 수 있습니다. 예를 들어 contoso.com에 대 한 레코드 하나 및 bulkmail.contoso.com에 대 한 다른 레코드를 만듭니다.
  
전자 메일 메시지가 배달 되기 전에 10 개 보다 많은 DNS 조회가 발생 하는 경우 받는 메일 서버는 _permerror_라고도 하는 영구 오류로 응답 하 고 메시지에 SPF 확인이 실패 합니다. 받는 서버는 다음과 같은 오류가 포함 된 배달 못 함 보고서 (NDR)와 함께 응답할 수도 있습니다.
  
- 메시지가 홉 수를 초과 했습니다.
    
- 메시지에 너무 많은 조회가 필요 합니다.
    
## <a name="avoiding-the-too-many-lookups-error-when-you-use-third-party-domains-with-office-365"></a>Office 365에서 타사 도메인을 사용 하는 경우 "너무 많은 조회" 오류가 발생 하지 않음
<a name="SPFTroubleshoot"> </a>

타사 도메인에 대 한 일부 SPF TXT 레코드는 받는 서버가 연결 하 여 많은 수의 DNS 조회를 수행 합니다. 예를 들어이 문서를 작성 하는 시점에 Salesforce.com에는 레코드에 5 개의 include 문이 포함 되어 있습니다.
  
```
v=spf1 include:_spf.google.com
include:_spfblock.salesforce.com
include:_qa.salesforce.com
include:_spfblock1.salesforce.com
include:spf.mandrillapp.com mx ~all
```

이 오류가 발생 하지 않도록 하려면 예를 들어 대량 전자 메일을 보내는 모든 사람이이 용도로만 하위 도메인을 사용 해야 하는 정책을 구현할 수 있습니다. 그런 다음 대량 전자 메일이 포함 된 하위 도메인에 대해 다른 SPF TXT 레코드를 정의 합니다.
  
 salesforce.com 예제와 같이 SPF TXT 레코드에서 도메인을 사용 해야 하는 경우도 있지만 타사에서이 목적으로 사용할 하위 도메인을 이미 만들었을 수도 있습니다. 예를 들어 exacttarget.com은 SPF TXT 레코드에 사용 해야 하는 하위 도메인을 만들었습니다. 
  
```
cust-spf.exacttarget.com
```

SPF TXT 레코드에 타사 도메인을 포함 하는 경우에는 10 개의 조회 제한으로 실행 되지 않도록 하기 위해 사용 하는 도메인 또는 하위 도메인이 있는 타사에 대 한 확인을 받아야 합니다.
  
## <a name="how-to-view-your-current-spf-txt-record-and-determine-the-number-of-lookups-that-it-requires"></a>현재 SPF TXT 레코드를 확인 하 고 필요한 조회 수를 결정 하는 방법
<a name="SPFTroubleshoot"> </a>

nslookup을 사용 하 여 SPF TXT 레코드를 비롯 한 DNS 레코드를 볼 수 있습니다. 또는 원하는 경우 SPF TXT 레코드의 콘텐츠를 보는 데 사용할 수 있는 무료 온라인 도구가 많이 있습니다. SPF TXT 레코드를 확인 하 고 포함 문 및 리디렉션 체인을 따라 레코드에 필요한 DNS 조회 수를 확인할 수도 있습니다. 일부 온라인 도구는 이러한 조회 수를 계산 하 여 표시 하기도 합니다. 이 번호를 추적 하면 조직에서 보내는 메시지가 받는 서버에서 permerror 라는 영구 오류를 발생 시 가지 못하도록 방지할 수 있습니다.
  
## <a name="for-more-information"></a>자세한 내용
<a name="SPFTroubleshoot"> </a>

SPF TXT 레코드를 추가 하는 데 도움이 필요 하세요? 다양 한 인기 도메인 등록 기관에서 SPF (TXT) 레코드를 업데이트 하는 단계별 [지침](https://office.microsoft.com/en-us/office365-suite-help/create-dns-records-for-office-365-HA102851099.aspx?CTT=5&amp;origin=HA102818404) 을 제공 합니다. [스팸 방지 메시지 헤더](anti-spam-message-headers.md) 에는 SPF 확인을 위해 Office 365에서 사용 하는 구문 및 헤더 필드가 포함 되어 있습니다. 
  

