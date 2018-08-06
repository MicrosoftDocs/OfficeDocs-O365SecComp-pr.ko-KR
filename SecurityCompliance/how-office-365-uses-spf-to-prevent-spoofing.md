---
title: Office 365 스푸핑 방지 하기 위해 보낸 사람이 정책 프레임 워크 (SPF)을 사용 하는 방법
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 12/15/2016
ms.audience: ITPro
ms.topic: reference
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
ms.assetid: 3aff33c5-1416-4867-a23b-e0c0c5b4d2be
description: '요약: Office 365 사용 하는 방법 보낸 사람이 정책 프레임 워크 (SPF) TXT 레코드 DNS에서 대상 전자 메일 시스템 사용자 지정 도메인에서 보낸 메시지를 신뢰 하도록이 문서에 설명 합니다. 이 Office 365에서 보낸 아웃 바운드 메일에 적용 됩니다. Office 365 내에서 받는 사람에 게 Office 365에서 보낸 메시지는 항상 SPF를 전달 합니다.'
ms.openlocfilehash: aea7f740a67ce282424efc409d25f3f135546ada
ms.sourcegitcommit: 22bca85c3c6d946083d3784f72e886c068d49f4a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/06/2018
ms.locfileid: "22026465"
---
# <a name="how-office-365-uses-sender-policy-framework-spf-to-prevent-spoofing"></a>Office 365 스푸핑 방지 하기 위해 보낸 사람이 정책 프레임 워크 (SPF)을 사용 하는 방법

 **요약:** 이 문서에서는 Office 365 사용 하는 방법 보낸 사람이 정책 프레임 워크 (SPF) TXT 레코드 DNS에서 대상 전자 메일 시스템 사용자 지정 도메인에서 보낸 메시지를 신뢰 하도록에 대해 설명 합니다. 이 Office 365에서 보낸 아웃 바운드 메일에 적용 됩니다. Office 365 내에서 받는 사람에 게 Office 365에서 보낸 메시지는 항상 SPF를 전달 합니다. 
  
SPF TXT 레코드를 전자 메일 메시지를 보낼 하는 도메인 이름을 확인 하 여 피싱 및 스푸핑 방지 하는 DNS 레코드를은 합니다. SPF을 보내는 도메인의 공식된 소유자에 대해 보낸 사람의 IP 주소를 확인 하 여 전자 메일 메시지의 출처의 유효성을 검사 합니다. 
  
> [!NOTE]
> SPF 레코드 종류는 하 여 Internet Engineering Task Force (IETF) 지원이 중단 된 2014 년에 했습니다. 대신, DNS에서 TXT 레코드를 사용 하 여 SPF 정보를 게시할 수 있는지 확인 합니다. 이 문서의 나머지 부분 명확 하 게 하기에 대 한 용어 SPF TXT 레코드를 사용합니다. 
  
도메인 관리자는 DNS에서 TXT 레코드에 SPF 정보를 게시 합니다. SPF 정보 권한이 부여 된 아웃 바운드 전자 메일 서버를 식별합니다. 대상 전자 메일 시스템 메시지 권한이 부여 된 아웃 바운드 전자 메일 서버에서 시작 되었는지 확인 합니다. SPF에 이미 익숙한 또는 간단한 배포 하 고 Office 365에 대 한 사용자의 DNS에서 SPF TXT 레코드에 포함 된 내용을 싶습니까을 하는 경우에 [스푸핑을 방지 하기 위해 Office 365에서 SPF를 설정](set-up-spf-in-office-365-to-help-prevent-spoofing.md)하려면 이동할 수 있습니다. Office 365에 완전히 호스트 되는 배포 하지 않은 경우 SPF 작동 하는 방법 또는 Office 365에 대 한 SPF 문제를 해결, 읽기 유지 하는 방법에 대 한 자세한 정보를 원하는.
  
> [!NOTE]
> 이전에 사용 하는 경우 SharePoint Online 사용자 지정 도메인에 다른 SPF TXT 레코드를 추가 했습니다. 이 더이상 필요 합니다. 이 변경의 정크 메일 폴더에서 종료 하는 SharePoint Online 알림 메시지의 위험을 줄이려면 해야 합니다. 변경 내용을 즉시, 하지만 "너무 많은 경우 조회" 오류 메시지가 표시 되는 경우 [SPF 스푸핑을 방지 하기 위해 Office 365에서 설정](set-up-spf-in-office-365-to-help-prevent-spoofing.md)의 설명에 따라 SPF TXT 레코드를 수정할 필요가 없습니다. 
     
## <a name="how-spf-works-to-prevent-spoofing-and-phishing-in-office-365"></a>SPF 위조 및 Office 365의 피싱 방지 하기 위해 작동 하는 방법
<a name="HowSPFWorks"> </a>

SPF는 보낸사람에서 도메인을 대신 하 여 보낼 수 있는지 여부를 결정 합니다. 경우 그렇게 보낸은 사용할 수 없습니다 즉, 전자 메일 받는 서버에서 SPF 검사에 실패 하는 경우 해당 서버에 구성 된 스팸 정책 결정 메시지와 함께 수행할 작업을 합니다.
  
각 SPF TXT 레코드는 세 부분으로 구성: SPF TXT 인지 선언 기록, 도메인 및 도메인 대신 및 적용 규칙에 보낼 수 있는 외부 도메인에서 메일을 보낼 수 있는 IP 주소입니다. 유효한 SPF TXT 레코드에 세 모두 필요합니다. 이 문서는 SPF TXT 레코드를 형성 하는 방법에 대해 설명 하 고 Office 365에서 서비스 사용 (영문)에 대 한 유용한 정보를 제공 합니다. Dns 레코드를 게시 하려면 도메인 등록 (영문)의 지침에 대 한 링크가 제공 됩니다.
  
### <a name="spf-basics-ip-addresses-allowed-to-send-from-your-custom-domain"></a>SPF 기본 사항: 사용자 지정 도메인에서 보낼 수 있는 IP 주소
<a name="SPFBasicsIPaddresses"> </a>

SPF 규칙에 대 한 기본 구문에 대 한 정보를 수행 합니다.
  
v = spf1 \<IP\> \<적용 규칙\>
  
예: contoso.com에 대 한 다음 해당 SPF 규칙이 존재 가정해 보겠습니다.
  
v = spf1 \<IP 주소 #1\> \<#2 IP 주소\> \<IP 주소 #3\> \<적용 규칙\>
  
이 예제에서는 SPF 규칙만 contoso.com 도메인에 대 한 이러한 IP 주소에서 메일을 수락 하도록 받는 전자 메일 서버를 지정 합니다.
  
- IP 주소 #1
    
- IP 주소 #2
    
- IP 주소 #3
    
이 SPF 규칙 해당 메시지에는 contoso.com에서 하지만 이러한 세 IP 주소 중 하나에서 하지 상태가 되 면 하는 경우 받는 서버에 적용 되도록 강제 적용 규칙 메시지의 받는 전자 메일 서버에 지시 합니다. 적용 규칙은 일반적으로 이러한 옵션 중 하나입니다.
  
- **영구 실패.** 메시지 봉투의 '영구 실패'를 사용 하 여 메시지를 표시 하 고이 유형의 메시지에 대 한 수신 서버 구성 된 스팸 정책을 따르는 것이 다음 키를 누릅니다. 
    
- **부드러운 실패.** 메시지 봉투의 '소프트 실패'를 사용 하 여 메시지를 표시 합니다. 일반적으로 전자 메일 서버는 이러한 메시지를 계속 제공 하도록 구성 됩니다. 대부분의 최종 사용자는이 기호를 표시 되지 않습니다. 
    
- **중립.** 이 무 것, 즉, 메시지 봉투를 표시 하지는 마십시오. 이 일반적으로 테스트 목적으로 예약 하 고 거의 사용 되지 않습니다. 
    
다음 예제는 SPF 다양 한 상황에서 작동 하는 방법을 보여줍니다. 이 예제에서는 contoso.com 보낸 이며 woodgrovebank.com 수화기 합니다.
  
### <a name="example-1-email-authentication-of-a-message-sent-directly-from-sender-to-receiver"></a>수신자에 게 보낸에서 직접 보내는 메시지의 예 1: 전자 메일 인증
<a name="spfExample1"> </a>

SPF는 수신자에 게 보낸에서 경로 같은 직접 하는 경우에 가장 적합 합니다.
  
![서버 간에 직접 전자 메일이 전송될 때 SPF에서 전자 메일을 인증하는 방법을 보여주는 다이어그램입니다.](media/835c20a7-ed4c-49c4-91fe-b8ebb3e452a1.jpg)
  
Woodgrovebank.com IP 주소 #1 contoso.com에 대 한 SPF TXT 레코드에 있으면 메시지를 받을 경우 메시지는 SPF 검사를 통과 하 고 인증 됩니다.
  
### <a name="example-2-spoofed-sender-address-fails-the-spf-check"></a>예 2: 위장 된 보낸사람 주소 SPF 검사에 실패
<a name="spfExample2"> </a>

phisher contoso.com 스푸핑할 하는 방법을 찾는 경우를 가정해 보겠습니다.
  
![스푸핑된 서버에서 보낸 전자 메일을 SPF에서 인증하는 방법을 보여주는 다이어그램입니다.](media/235dac3d-cdc5-466e-86e0-37b5979de198.jpg)
  
IP 주소 #12 contoso.com의 SPF TXT 레코드에 없기 때문에 메시지 SPF 확인 실패 하 고 수신자 스팸으로 표시 하도록 선택할 수 있습니다.
  
### <a name="example-3-spf-and-forwarded-messages"></a>예 3: SPF 및 전달된 하는 메시지
<a name="spfExample3"> </a>

하나의 SPF의 단점은 전자 메일 전달 된 경우 작동 하지 않는 것입니다. 예, woodgrovebank.com에서 사용자가 모든 전자 메일을 보낼 outlook.com 계정에 착신 전환 규칙 설정 있다고 가정 합니다.
  
![메시지가 전달될 때 SPF에서 전자 메일을 인증할 수 없는 상황을 보여주는 다이어그램입니다.](media/6e92acd6-463e-4a1b-8327-fb1cf861f356.jpg)
  
메시지 woodgrovebank.com에서 원래 SPF 검사를 전달 하지만 outlook.com에서 SPF 확인 IP #25 contoso.com의 SPF TXT 레코드에 없기 때문에 실패 하면 합니다. Outlook.com 스팸으로 메시지를 표시할 수 있습니다. 이 문제를 해결 하려면 함께에서 SPF를 사용 하 여 DKIM 및 DMARC와 같은 다른 전자 메일 인증 방법을 사용 합니다.
  
### <a name="spf-basics-including-third-party-domains-that-can-send-mail-on-behalf-of-your-domain"></a>SPF 기본 사항: 도메인을 대신 하 여 메일을 보낼 수 있는 타사 도메인을 포함 하 여
<a name="SPFBasicsIncludes"> </a>

IP 주소 외에도 보낸사람 등의 도메인을 포함 하 여 SPF TXT 레코드를 구성할 수 있습니다. 이러한 "포함" 문으로 SPF TXT 레코드에 추가 됩니다. 예: contoso.com contoso.net 및 contoso.org도 소유 하는 메일 서버의 IP 주소를 모두 포함 하고자 하는 수 있습니다. Contoso.com이 작업을 수행 하는 SPF TXT 레코드는 다음과 같은 게시 합니다.
  
```
IN TXT "v=spf1 include:contoso.net include:contoso.org -all"
```

받는 서버는 DNS에이 레코드를 표시, contoso.net 및 다음 contoso.org SPF TXT 레코드에도 DNS 조회를 수행 합니다. 추가로 발견 되 면 contoso.net 또는 contoso.org에 대 한 레코드 내에 문을 포함, 이러한 너무 대로 됩니다. 서비스 거부 공격을 방지 하기 위해 단일 전자 메일 메시지에 대 한 DNS 조회의 최대 수는 10을 사용 합니다. 각 포함 문을 나타냅니다 DNS 조회를 추가 합니다. 10 제한을 초과 하는 메시지, 메시지 SPF 오류가 발생 합니다. 보낸 메시지는 "너무 많은 경우 조회" 또는 생성 되었다는 메시지가 나타날 수 메시지를 받는 서버를 구성 하는 방식에 따라이 제한에 도달 하면는 "메시지에 대 한 최대 홉 수 초과 했습니다."입니다. 이 문제를 방지 하는 방법에 대 한 팁을 참조 하십시오. [문제해결: Office 365에서 SPF에 대 한 모범 사례](how-office-365-uses-spf-to-prevent-spoofing.md#SPFTroubleshoot)합니다.
  
## <a name="requirements-for-your-spf-txt-record-and-office-365"></a>SPF TXT 레코드 및 Office 365에 대 한 요구 사항
<a name="SPFReqsinO365"> </a>

Office 365를 설정 하는 경우 메일을 설정 하면 사용자의 도메인에 대 한 메일의 합법적인 소스로 Microsoft 메시징 서버를 식별 하는 SPF TXT 레코드를 이미 만든 합니다. 이 레코드 아마도 다음과 같습니다.
  
```
v=spf1 include:spf.protection.outlook.com -all
```

즉, 완벽 하 게 호스팅 Office 365 고객 인 경우 아웃 바운드 메일을 보내도록 온-프레미스 메일 서버 없음 해야, Office 365에 대 한 게시 하는 유일한 SPF TXT 레코드입니다.
  
하이브리드 배포 하는 경우 (즉, 일부 사서함 온-프레미스 및 Office 365에서 호스팅된 일부)에 있는 Exchange Online Protection (EOP) 독립 실행형 고객 인 경우 또는 (즉, 조직을 사용 하 여 EOP가 온-프레미스 사서함을 보호 하기 위해)를 수행 해야 합니다 DNS에서 TXT SPF 레코드를 각에 지 온-프레미스 메일 서버에 대 한 아웃 바운드 IP 주소를 추가 합니다.
  
## <a name="form-your-spf-txt-record-for-office-365"></a>Office 365에 대 한 SPF TXT 레코드를 양식
<a name="FormYourSPF"> </a>

이 문서의 구문 정보를 사용 하 여 사용자 지정 도메인에 대 한 SPF TXT 레코드를 형성 합니다. 다른 이지만 가장 일반적으로 여기에 언급 되지 않은 구문 옵션 옵션을 사용 합니다. 사용자의 레코드를 세운 후에 도메인 등록자에서 레코드를 업데이트 해야 합니다.
  
Office 365에 대 한 포함 해야하는 도메인에 대 한 정보를 [SPF에 필요한 외부 DNS 레코드를](https://support.office.com/en-us/article/External-Domain-Name-System-records-for-Office-365-c0531a6f-9e25-4f2d-ad0e-a70bfef09ac0?ui=en-US&amp;rs=en-US&amp;ad=US)참조 하십시오. 도메인 등록자에 대 한 SPF (TXT) 레코드를 업데이트 하기 위한 [단계별 지침](https://office.microsoft.com/en-us/office365-suite-help/create-dns-records-for-office-365-HA102851099.aspx?CTT=5&amp;origin=HA102818404) 을 사용 합니다. 등록 기관과 목록에 없는 경우에 사용자의 레코드를 업데이트 하는 방법을 설명 하는 개별적으로 연락할 해야 합니다. 
  
### <a name="spf-txt-record-syntax-for-office-365"></a>Office 365에 대 한 SPF TXT 레코드 구문
<a name="SPFSyntaxO365"> </a>

Office 365에 대 한 일반적인 SPF TXT 레코드는 다음 구문을 사용 합니다.
  
```
v=spf1 [<ip4>|<ip6>:<IP address>] [include:<domain name>] <enforcement rule>
```

예를 들면 다음과 같습니다.
  
```
v=spf1 ip4:192.168.0.1 ip4:192.168.0.2 include:spf.protection.outlook.com -all
```

여기서 각 부분이 나타내는 의미는 다음과 같습니다.
  
- **v = spf1** 가 필요 합니다. SPF TXT 레코드를으로 TXT 레코드를 정의합니다. 
    
- **ip4** IP 버전 4 주소를 사용 하 고 있음을 나타냅니다. **i p 6** IP 버전 6 주소를 사용 하 고 있음을 나타냅니다. I p v 6 IP 주소를 사용 하는 경우이 문서의 예제에 **i p 6** **ip4를** 대체 합니다. CIDR 표기법을 **ip4:192.168.0.1/26**예를 사용 하 여 IP 주소 범위를 지정할 수 있습니다.
    
-  _IP 주소_ 는 SPF TXT 레코드를 추가 하려면 IP 주소입니다. 일반적으로 조직에 대 한 아웃 바운드 메일 서버의 IP 주소입니다. 여러 아웃 바운드 메일 서버를 나열할 수 있습니다. 자세한 내용은 참조 [예제: 여러 아웃 바운드 온-프레미스 메일 서버 및 Office 365에 대 한 SPF TXT 기록](how-office-365-uses-spf-to-prevent-spoofing.md#ExampleSPFMultipleMailServerO365)합니다.
    
-  _도메인_ 이름은 합법적인 보낸사람으로 추가 하려는 도메인입니다. Office 365에 대 한 포함 되어야 하는 도메인 이름 목록에 대 한 [SPF에 필요한 외부 DNS 레코드를](https://support.office.com/en-us/article/External-Domain-Name-System-records-for-Office-365-c0531a6f-9e25-4f2d-ad0e-a70bfef09ac0?ui=en-US&amp;rs=en-US&amp;ad=US)참조 합니다.
    
- 적용 규칙은 일반적으로 다음 중 하나입니다.
    
  - <0.0.0.0> 또는 <mail.contoso.com> 값은 도메인에 대한 전자 메일을 보내는 다른 메일 시스템이어야 합니다.

    
    영구 실패를 나타냅니다. SPF TXT 레코드에 나열 하 고 사용 하 여 도메인에 대 한 모든 권한이 부여 된 IP 주소를 알고 있으면-모든 (영구 실패) 한정자입니다. 또한만 사용할 경우 SPF, 즉, DMARC 또는 DKIM를 사용 하지 않는을 사용 해야-모든 한정자입니다. 사용 하는 항상이 한정자는 것이 좋습니다.
    
  - ~ 모든
    
    부드러운 실패를 나타냅니다. 확실 하지 않은 IP 주소의 전체 목록은 합니다를 사용 해야 하는 경우는 ~ 모든 (소프트 실패) 한정자입니다. P로 DMARC를 사용 하는 경우 격리 또는 p = 하는 또한 사용할 수 있는 다음 reject = ~ 모든 합니다. 그렇지 않은 경우-을 모두 사용.
    
  - ? 모든
    
    중립을 나타냅니다. 이 SPF를 테스트할 때 사용 됩니다. 이 한정자를 사용 하 여 라이브 배포에서 하는 것은 좋지 않습니다.
    
### <a name="example-spf-txt-record-to-use-when-all-of-your-mail-is-sent-by-office-365"></a>예: SPF TXT 레코드 될 때 사용 하 여 Office 365에서 보내는 모든 메일
<a name="ExampleSPFNoSP"> </a>

Office 365에서 전송 되는 모든 사용자의 메일 하는 경우에이 사용 하 여 SPF TXT 레코드에서:
  
```
v=spf1 include:spf.protection.outlook.com -all
```

### <a name="example-spf-txt-record-for-a-hybrid-scenario-with-one-on-premises-exchange-server-and-office-365"></a>예: SPF TXT 레코드 하나를 사용 하 여 하이브리드 시나리오에 대 한 온-프레미스 Exchange 서버와 Office 365
<a name="ExampleSPFHybridOneExchangeServer"> </a>

하이브리드 환경에서 온-프레미스 Exchange 서버의 IP 주소 192.168.0.1 이면 하드 실패 함 SPF 적용 규칙을 설정 하기 위해 양식 SPF TXT 레코드 다음과 같습니다.
  
```
v=spf1 ip4:192.168.0.1 include:spf.protection.outlook.com -all
```

### <a name="example-spf-txt-record-for-multiple-outbound-on-premises-mail-servers-and-office-365"></a>예: 여러 아웃 바운드 온-프레미스에 대 한 SPF TXT 레코드 메일 서버 및 Office 365
<a name="ExampleSPFMultipleMailServerO365"> </a>

여러 아웃 바운드 메일 서버를 사용 하는 경우 SPF TXT 레코드에 각 메일 서버에 대 한 IP 주소를 포함 하 고 각 IP 주소 앞에 오는 공백을 구분 하는 "ip4:" 문입니다. 예를 들어:
  
```
v=spf1 ip4:192.168.0.1 ip4:192.168.0.2 ip4:192.168.0.3 include:spf.protection.outlook.com -all
```

## <a name="next-steps-set-up-spf-for-office-365"></a>다음 단계: Office 365에 대 한 SPF 설정
<a name="SPFNextSteps"> </a>

SPF TXT 레코드를 작성 한 한번, 도메인을 추가 하려면 [스푸핑을 방지 하기 위해 Office 365에서 SPF 설정](set-up-spf-in-office-365-to-help-prevent-spoofing.md) 의 단계를 수행 합니다. 
  
SPF 위조를 방지 설계 되었지만 스푸핑 하는 방법은 있지만 해당 SPF 보호 수는 없습니다. SPF를 설정 하 고 나면 이러한 경우에 대해 보호 하기 위해도 구성 해야 DKIM 및 DMARC Office 365에 대 한 합니다. 시작 하기 위해 [Office 365에서 사용자 지정 도메인에서 보낸 아웃 바운드 전자 메일의 유효성을 검사를 사용 하 여 DKIM](use-dkim-to-validate-outbound-email.md)를 참조 합니다. 다음으로, [Office 365의 전자 메일의 유효성을 검사를 사용 하 여 DMARC](use-dmarc-to-validate-email.md)를 참조 하십시오.
  
## <a name="troubleshooting-best-practices-for-spf-in-office-365"></a>Office 365에서 SPF에 대 한 모범 사례 문제를 해결 합니다.
<a name="SPFTroubleshoot"> </a>

만 사용자 지정 도메인에 대 한 하나의 SPF TXT 레코드를 만들 수 있습니다. 라운드 로빈 상황을 사용 하면 여러 레코드를 만드는 및 SPF 실패 합니다. 이 문제를 방지 하려면 각 하위 도메인에 대 한 별도 레코드를 만들 수 있습니다. 예, contoso.com에 대 한 레코드가 둘 및 bulkmail.contoso.com에 대 한 다른 레코드를 만듭니다.
  
배달 전에 10 개 이상의 DNS 조회를 설정 하는 전자 메일 메시지를 받는 메일 서버를 _permerror_이 라고도 하는 영구 오류를 사용 하 여 응답 및 SPF 확인 실패 메시지가 발생 합니다. 다음과 유사한 오류가 포함 된 배달 못함 보고서 (NDR)와 함께 받는 서버 응답도 않을 수 있습니다.
  
- 홉 수를 초과 하는 메시지입니다.
    
- 메시지에 너무 많은 경우 조회 필요합니다.
    
## <a name="avoiding-the-too-many-lookups-error-when-you-use-third-party-domains-with-office-365"></a>제 3 자 도메인을 사용 하 여 Office 365를 사용 하는 경우에 "너무 많은 경우 조회" 오류를 방지 하기
<a name="SPFTroubleshoot"> </a>

제 3 자 도메인에 대 한 일부 SPF TXT 레코드 직접 많은 DNS 조회를 수행 하려면 받는 서버입니다. 예 5 포함 Salesforce.com이 문서를이 작성할 때 해당 레코드에 문을 포함 합니다.
  
```
v=spf1 include:_spf.google.com
include:_spfblock.salesforce.com
include:_qa.salesforce.com
include:_spfblock1.salesforce.com
include:spf.mandrillapp.com mx ~all
```

이 오류를 방지 하려면이 목적을 위해 특별히 하위 도메인을 사용 하 여 대량 메일을 보내는 모든 사용자가 정책을 구현할 수 있습니다. 대량 전자 메일을 포함 하는 하위 도메인에 대 한 다른 SPF TXT 레코드를 정의 합니다.
  
 Salesforce.com 예제와 같은 일부 경우에 사용자의 SPF TXT 레코드에서 도메인을 사용 해야 하지만 또 어떤 경우에는 타사 수를 이미 만든이 목적을 위해 사용 하 여 하위 도메인이 합니다. 예 exacttarget.com SPF TXT 레코드를 사용 하는 하위 도메인을 만들었습니다. 
  
```
cust-spf.exacttarget.com
```

SPF TXT 레코드에서 타사 도메인을 포함 하는 경우 확인 하도록 요청 타사 어떤 도메인 또는 하위 도메인에 10 조회 하는 것을 방지 하기 위해 사용할 수를 제한 해야 합니다.
  
## <a name="how-to-view-your-current-spf-txt-record-and-determine-the-number-of-lookups-that-it-requires"></a>사용자의 현재 SPF TXT 레코드를 확인 하 고 필요 조회 수를 결정 하는 방법
<a name="SPFTroubleshoot"> </a>

Nslookup을 사용 하 여 SPF TXT 레코드를 포함 하 여 DNS 레코드를 볼 수 있습니다. 또는 원할 경우 다양 한 SPF TXT 레코드의 콘텐츠를 보려면 사용할 수 있는 무료, 온라인 도구가 있습니다. SPF TXT 봐서는 레코드와의 연결 고리 과정을 따라 포함 문과 리디렉션하거나, 레코드가 필요 얼마나 많은 DNS 조회를 확인할 수 있습니다. 일부 온라인 도구 count에도 하 고 이러한 조회 표시 됩니다. 이 번호는 추적을 permerror 받는 서버에서 호출 영구적 오류를 트리거에서 조직에서 보낸 메시지를 차단 하는 데 도움이 됩니다.
  
## <a name="for-more-information"></a>자세한 내용
<a name="SPFTroubleshoot"> </a>

도움이 필요 하십니까 SPF TXT 레코드 추가 (영문)? 다양 한 인기 있는 도메인 등록자에서 SPF (TXT) 레코드를 업데이트 하는 것에 대 한 [단계별 지침](https://office.microsoft.com/en-us/office365-suite-help/create-dns-records-for-office-365-HA102851099.aspx?CTT=5&amp;origin=HA102818404) 은 사용할 수 있습니다. [스팸 방지 메시지 헤더](anti-spam-message-headers.md) SPF 확인을 위한 Office 365에서 사용 되는 구문과 헤더 필드를 포함 합니다. 
  

