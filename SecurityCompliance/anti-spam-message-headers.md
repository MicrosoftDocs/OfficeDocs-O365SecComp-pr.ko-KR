---
title: 스팸 방지 메시지 헤더
ms.author: tracyp
author: MSFTTracyP
manager: dansimp
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Priority
search.appverid:
- MET150
ms.assetid: 2e3fcfc5-5604-4b88-ac0a-c5c45c03f1db
ms.collection:
- M365-security-compliance
description: Exchange Online Protection에서 인바운드 전자 메일 메시지를 검색하는 경우 **X-Forefront-Antispam-Report** 헤더가 각 메시지에 삽입됩니다.
ms.openlocfilehash: b83cba8240ff27b9d6e872ad09bf23c2755478c5
ms.sourcegitcommit: 33c8e9c16143650ca443d73e91631f9180a9268e
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/25/2019
ms.locfileid: "35854622"
---
# <a name="anti-spam-message-headers"></a>스팸 방지 메시지 헤더

Exchange Online Protection에서 인바운드 전자 메일 메시지를 검색하는 경우 **X-Forefront-Antispam-Report** 헤더가 각 메시지에 삽입됩니다. 관리자는 이 헤더의 필드를 통해 메시지 및 메시지 처리 방법에 대한 정보를 확인할 수 있습니다. **X-Microsoft-Antispam** 헤더의 필드는 대량 메일 및 피싱에 대한 추가 정보를 제공합니다. 이러한 두 헤더 외에도, Exchange Online Protection은 **Authentication-results** 헤더에서 처리하는 각 메시지의 전자 메일 인증 결과를 삽입합니다.

다양한 전자 메일 클라이언트에서 전자 메일 메시지 헤더를 보는 방법에 대한 자세한 내용은 [메시지 헤더 분석기](https://go.microsoft.com/fwlink/p/?LinkId=306583)를 참조하세요. 
  
> [!TIP]
>  메시지 헤더의 내용을 복사하여 [Message Analyzer](https://testconnectivity.microsoft.com/?tabid=mha) 도구에 붙여 넣을 수 있습니다. 이 도구는 헤더를 구문 분석하여 더 판독하기 쉬운 형식으로 삽입합니다.
  
## <a name="x-forefront-antispam-report-message-header-fields"></a>X-Forefront-Antispam-Report 메시지 헤더 필드

메시지 헤더 정보에 액세스한 후 **X-X-Forefront-Antispam-Report**를 검색하여 이 필드를 찾습니다. 이 헤더의 다른 필드는 Microsoft 스팸 방지 팀에서 진단용으로만 사용합니다.

|**헤더 필드**|**설명**|
|:-----|:-----|
|CIP: [IP address]|연결할 IP 주소. 연결 필터에서 IP 허용 목록 또는 IP 차단 목록을 만들 때 이 IP를 지정하려고 할 수 있습니다. 자세한 내용은 [Configure the connection filter policy](configure-the-connection-filter-policy.md)를 참조하십시오.|
|CTRY|메시지가 서비스에 연결된 국가입니다. 연결하는 IP 주소(원래 메시지를 보낸 IP 주소와 다를 수도 있음)를 통해 확인됩니다.|
|LANG|국가 코드로 지정된 메시지 작성 언어입니다. 예를 들어 ru_RU는 러시아어입니다.|
|SCL|메시지의 SCL(스팸 지수) 값입니다. 이러한 값을 해석하는 방법에 대한 자세한 내용은 [Spam confidence levels](spam-confidence-levels.md)를 참조하세요.|
|PCL|메시지의 PCL(피싱 지수) 값입니다.|
|SRV:BULK|메시지가 대량 전자 메일 메시지로 확인되었습니다. **모든 대량 전자 메일 메시지 차단 고급 스팸 필터링 옵션**을 사용하도록 설정한 경우 해당 메시지는 스팸으로 표시됩니다. 이 옵션을 사용하도록 설정하지 않은 경우 메시지는 나머지 필터링 규칙에 의해 스팸으로 확인되는 경우에만 스팸으로 표시됩니다.|
|SFV:SFE|개인의 [수신 허용 - 보낸 사람] 목록에 포함된 주소에서 보낸 메시지이므로 필터링을 건너뛰었으며 메시지 통과가 허용되었습니다.|
|SFV:BLK|개인의 수신 거부 목록에 포함된 주소에서 보낸 메시지이므로 필터링을 건너뛰었으며 메시지가 차단되었습니다.  <br/> **팁:** 최종 사용자가 수신 허용 - 보낸 사람 목록 및 수신 거부 목록을 만드는 방법에 대한 자세한 내용은 [차단 또는 허용(정크 메일 설정)](https://go.microsoft.com/fwlink/p/?LinkId=294862)(OWA) 및 [정크 메일 필터 개요](https://go.microsoft.com/fwlink/p/?LinkId=270065)(Outlook)를 참조하세요.|
|IPV:CAL|연결 필터의 IP 허용 목록에 IP 주소가 지정되어 있어 메시지가 스팸 필터를 통과하도록 허용되었습니다.|
|IPV:NLI|IP 주소가 IP 신뢰도 목록에 포함되지 않았습니다.|
|SFV:SPM|메시지가 콘텐츠 필터에 의해 스팸으로 표시되었습니다.|
|SFV:SKS|메시지가 콘텐츠 필터에 의해 처리되기 전에 이미 스팸으로 표시되었습니다. 메일 흐름 규칙(전송 규칙이라고도 함)과 일치하여 스팸으로 자동 표시되고 모든 추가 필터링을 무시하는 메시지가 여기에 포함됩니다.|
|SFV:SKA|메시지가 **보낸 사람 허용** 목록과 같은 스팸 필터 정책의 허용 목록과 일치하므로 메시지가 필터링을 건너뛰고 편지함으로 배달되었습니다.|
|SFV: SKB|**보낸 사람 차단** 목록과 같은 스팸 필터 정책의 차단 목록과 일치하므로 메시지가 스팸으로 표시되었습니다.|
|SFV:SKN|메시지가 콘텐츠 필터에 의해 처리되기 전에 이미 스팸이 아닌 것으로 표시되었습니다. 메일 흐름 규칙과 일치하여 스팸이 아닌 것으로 자동 표시되고 모든 추가 필터링을 무시하는 메시지가 여기에 포함됩니다.|
|SFV:SKI|SFV:SKN와 마찬가지로 다른 이유 때문에 메시지 필터링을 건너뛰었습니다(예: 테넌트 내의 조직 내 전자 메일).|
|SFV:SKQ|메시지가 격리에서 해제되었으며 받는 사람에게 전송되었습니다.|
|SFV:NSPM|메시지가 스팸이 아닌 것으로 표시되었으며 받는 사람에게 전송되었습니다.|
|H: [helostring]|연결하는 메일 서버의 HELO 또는 EHLO 문자열입니다.|
|PTR: [ReverseDNS]|보내는 IP 주소의 PTR 레코드(또는 포인터 레코드)로, 역방향 DNS 주소라고도 합니다.|
|SFTY|메시지가 피싱 메일로 확인되었으므로 다음 값 중 하나로 표시됩니다. <br/>• 9.1: 기본값. 메시지에 피싱 URL이 포함되어 있거나, 다른 피싱 콘텐츠가 포함되어 있을 수도 있고, Office 365에 메시지를 릴레이하기 전에 Exchange Server의 온-프레미스 버전과 같은 다른 메일 필터에 의해 피싱로 표시되었을 수 있습니다. <br/>• 9.11:메시지가 보낸 사람: 헤더의 송신 도메인이 수신 도메인과 동일하거나, 수신 도메인에 적합하거나, 수신 도메인과 동일한 조직의 일부인지에 대한 스푸핑 방지 확인에 실패했습니다. 이는 조직 간 스푸핑 방지 팁이 메시지에 추가됨을 나타냅니다. <br/>• 9.19: 메시지가 송신 도메인이 받는 사람이 소유한 도메인 또는 피싱 방지 정책에 의해 보호되는 사용자 지정 도메인을 가장하는지에 대한 도메인 가장 확인에 실패했습니다. 이는 피싱 방지 정책을 통해 사용하는 경우 가장 보안 팁이 메시지에 추가됨을 의미합니다. <br/>• 9.20: 메시지가 송신 사용자가 받는 사람 조직 중 한 사용자 또는 피싱 방지 정책에 의해 보호되는 사용자 지정 사용자를 가장하는지에 대한 사용자 가장 확인에 실패했습니다. 이는 피싱 방지 정책을 통해 사용하는 경우 가장 보안 팁이 메시지에 추가됨을 의미합니다. <br/>• 9.21: 메시지를 스푸핑 방지 확인에 실패하고 보낸 사람: 헤더의 송신 도메인이 인증되지 않고 외부 도메인에서 발송되었습니다. CompAuth(인증 결과 참조)와 함께 사용합니다. <br/>• 9.22: 9.21과 동일하며, 다른 사항은 사용자에게 재정의된 [수신 허용 - 보낸 사람]이 있다는 점입니다. <br/>• 9.23: 9.22와 동일하며, 다른 사항은 조직에 재정의된 허용된 보낸 사람 또는 도메인이 있다는 점입니다. <br/>• 9.24: 9.23과 동일하며, 다른 사항은 사용자에게 재정의된 Exchange 메일 흐름 규칙이 있다는 점입니다.|
|X-CustomSpam: [ASFOption]|ASF(고급 스팸 필터링) 옵션과 일치하는 메시지. 예를 들어, **X-CustomSpam: 원격 사이트에 대한 이미지 링크**는 **원격 사이트에 대한 이미지 링크** ASF 옵션이 일치하는 것으로 확인되었음을 나타냅니다. 각 특정 ASF 옵션에 대해 추가된 X-헤더 텍스트를 확인하려면 [Advanced spam filtering options](advanced-spam-filtering-asf-options.md)을 참조하세요.|
   
## <a name="x-microsoft-antispam-message-header-fields"></a>X-Microsoft-Antispam 메시지 헤더 필드

다음 표에서는 **X-Microsoft-Antispam** 메시지 헤더의 유용한 필드에 대해 설명합니다. 이 헤더의 다른 필드는 Microsoft 스팸 방지 팀에서 진단용으로만 사용합니다.
  
|**헤더 필드**|**설명**|
|:-----|:-----|
|BCL|메시지의 BCL(대량 불만 수준)입니다. 자세한 내용은 [BCL(대량 불만 수준) 값](bulk-complaint-level-values.md)을 참조하세요.|
|PCL|피싱 메시지인지 여부를 나타내는 메시지의 PCL(피싱 신뢰 수준)입니다. 이 상태는 다음 숫자 값 중 하나로 반환될 수 있습니다. <br/>• **0-3**: 메시지의 콘텐츠가 피싱 메시지일 가능성이 크지 않을 수 있습니다. <br/>• **4-8**: 메시지의 콘텐츠가 피싱일 수 있습니다. <br/>• **-9990**: (Exchange Online Protection에만 해당) 메시지 내용이 피싱일 수 있습니다.  <br/>  값을 사용하여 전자 메일 클라이언트에서 메시지에 대해 수행하는 작업을 확인합니다. 예를 들어, Outlook은 PCL 스탬프를 사용하여 의심스러운 메시지의 내용을 차단합니다. 피싱에 대한 자세한 내용과 Outlook에서 피싱 메시지를 처리하는 방법에 대 한 자세한 내용은 [전자 메일 메시지에서 링크 설정 또는 해제](https://support.office.com/article/2D79B907-93B6-4774-82E6-1F0385CF20F8)를 참조하세요.|
   
## <a name="authentication-results-message-header"></a>Authentication-Results 메시지 헤더

전자 메일 서버에서 전자 메일 메시지를 수신 하는 경우 SPF, DKIM 및 DMARC에 대한 검사 결과는 **Authentication-results** 메시지 헤더의 Office 365를 통해 기록되거나 스탬프 처리됩니다.
  
### <a name="check-stamp-syntax-and-examples"></a>검사 스탬프 구문 및 예제

다음 구문 예제에서는 Office 365가 메일 서버에서 수신할 때 전자 메일 인증 확인을 실행하는 각 전자 메일의 메시지 헤더에 적용 되는 "스탬프"라는 텍스트 부분을 보여줍니다. 스탬프가 **Authentication-Results** 헤더에 추가됩니다.
  
**구문: SPF 체크 스탬프**
  
SPF의 경우, 다음 구문이 적용 됩니다.
  
```
spf=<pass (IP address)|fail (IP address)|softfail (reason)|neutral|none|temperror|permerror> smtp.mailfrom=<domain>
```

**예: SPF 체크 스탬프**
  
```
spf=pass (sender IP is 192.168.0.1) smtp.mailfrom=contoso.com
spf=fail (sender IP is 127.0.0.1) smtp.mailfrom=contoso.com
```

**구문: DKIM 체크 스탬프**
  
DKIM의 경우, 다음 구문이 적용됩니다.
  
```
dkim=<pass|fail (reason)|none> header.d=<domain>
```

**예: DKIM 체크 스탬프**
  
```
dkim=pass (signature was verified) header.d=contoso.com
dkim=fail (body hash did not verify) header.d=contoso.com
```

**구문: DMARC 체크 스탬프**
  
DMARC의 경우, 다음 구문이 적용됩니다.
  
```
dmarc=<pass|fail|bestguesspass|none> action=<permerror|temperror|oreject|pct.quarantine|pct.reject> header.from=<domain>
```

**예: DMARC 체크 스탬프**
  
```
dmarc=pass action=none header.from=contoso.com
dmarc=bestguesspass action=none header.from=contoso.com
dmarc=fail action=none header.from=contoso.com
dmarc=fail action=oreject header.from=contoso.com
```

### <a name="authentication-results-message-header-fields-used-by-office-365-email-authentication"></a>Office 365 전자 메일 인증에서 사용하는 Authentication-results 메시지 헤더 필드

이 표에서는 각 전자 메일 인증 확인에 대한 필드와 가능한 값에 대해 설명합니다.
  
|**헤더 필드**|**설명**|
|:-----|:-----|
|spf|메시지에 대한 SPF 검사 결과를 설명합니다. 가능한 값은 다음과 같습니다. <br/>• **통과(IP 주소)**: 전달된 메시지에 대한 SPF 검사를 나타내고 보낸 사람의 IP 주소를 포함합니다. 클라이언트는 보낸 사람의 도메인을 대신하 여 전자 메일을 보내거나 릴레이할 수 있습니다. <br/>• **실패(IP 주소)**: 메시지에 대한 SPF 검사가 실패했음을 나타내고 보낸 사람의 IP 주소를 포함합니다. 이를 종종 _하드 실패_이라고 합니다. <br/>• **소프트 실패(원인)**: SPF 레코드에서 호스트가 보낼 수 없는 것으로 지정되었지만 전환 중임을 나타냅니다. <br/>• **중립**: SPF 레코드에 IP 주소가 인증되었는지 여부를 어설션하지 않음을 명시적으로 지정되었음을 나타냅니다. <br/>• **없음**: 도메인에 SPF 레코드가 없거나 SPF 레코드에서 결과를 평가하지 않음을 나타냅니다. <br/>• **temperror**: 예를 들어 DNS 오류와 같은 일시적인 오류가 발생했음을 나타냅니다. 나중에 다시 시도하면 관리자 조치 없이도 성공할 수 있습니다. <br/>• **permerror**: 영구적인 오류가 발생했음을 나타냅니다. 예를 들어 도메인에 형식이 잘못된 SPF 레코드가 있을 때 발생합니다.|
|smtp.mailfrom|메시지를 보낸 원본 도메인을 포함합니다. 이 전자 메일 메시지의 오류는 전자 메일 관리자나 도메인을 담당하는 엔터티로 전송됩니다. 이를 메시지 봉투에서 5321.MailFrom 주소 또는 역-경로 주소라고도 합니다.|
|dkim|메시지의 DKIM 검사 결과를 설명합니다. 가능한 값은 다음과 같습니다. <br/>• **통과**: 통과한 메시지의 DKIM 검사를 나타냅니다. <br/>• **실패(원인)**: 실패한 메시지의 DKIM 검사와 오류를 나타냅니다. 예를 들어, 메시지에 서명이 없거나 서명이 확인되지 않은 경우입니다. <br/>• **없음**: 메시지에 서명이 없음을 나타냅니다. 이는 도메인에 DKIM 레코드가 있거나 DKIM 레코드가 결과에 대해 평가되지 않음을 의미하지 않으며, 이 메시지에 서명이 없음을 나타냅니다.|
|머리글. d|해당하는 경우, DKIM 서명에서 식별된 도메인입니다. 이는 공개 키에 대해 쿼리된 도메인입니다.|
|dmarc|메시지에 대한 DMARC 검사 결과를 설명합니다. 가능한 값은 다음과 같습니다. <br/>• **통과**: 메시지에 대한 DMARC 에 통과했음을 나타냅니다. <br/>• **실패**: 메시지에 대한 DMARC 검사에 실패했음을 나타냅니다. <br/>• **bestguesspass**: 도메인의 DMARC TXT 레코드가 없지만, 존재하는 경우에는 해당 메시지에 대한 DMARC 검사를 통과했음을 나타냅니다. 이는 5321.MailFrom 주소의 도메인과 5322.MailFrom 주소의 도메인와 일치하기 때문입니다.  <br/>• **없음**: DNS에 송신 도메인에 대한 DKIM TXT 레코드가 존재하지 않음을 나타냅니다.|
|조치|DMARC 검사 결과에 따라 스팸 필터에서 수행하는 작업을 표시합니다. 예: <br/>• **permerror**: DMARC 평가 중에 영구적 오류(예: DNS에서 잘못된 형식의 DMARC TXT 레코드 발생)가 발생했습니다. 이 메시지를 다시 보내도 결과가 달라지지 않을 수 있습니다. 대신, 이 문제를 해결하기 위해 도메인 소유자에 문의해야 합니다. <br/>• **temperror**: DMARC 평가 중에 일시적인 오류가 발생했습니다. 전자 메일을 제대로 처리할 수 있도록 보낸 사람이 메시지를 나중에 다시 보내도록 요청할 수 있습니다. <br/>• **oreject** 또는 **o.reject**: 재정의 거부를 나타냅니다. 이 경우, Office 365에서는 p=reject 정책을 사용하는 DMARC TXT 레코드의 도메인으로부터 DMARC 검사에 실패하는 메시지를 수신할 때 이 작업을 사용합니다.  메시지를 삭제하거나 거부하는 대신, Office 365에서는 해당 메시지를 스팸으로 표시합니다. Office 365를 이런 방식으로 구성하는 방법에 대한 자세한 내용은 [Office 365에서 DMARC에 실패한 인바운드 전자 메일을 처리하는 방법](use-dmarc-to-validate-email.md#inbounddmarcfail)을 참조하세요. <br/>• **pct.quarantine**: DMARC를 통과하지 못하는 메시지 중 100% 미만 백분율이 전달되는 것을 나타냅니다. 즉, 메시지가 DMARC에 실패하고 정책이 격리로 설정되어 있지만, pct 필드는 100%로 설정되지 않았고, 지정된 도메인의 정책에 따라, 시스템에서 DMARC 작업을 적용하지 않도록 임의로 결정했음을 의미합니다. <br/>• **pct.reject**: DMARC를 통과하지 못하는 메시지 중 100% 미만 백분율이 전달됨을 나타냅니다. 즉, 메시지가 DMARC에 실패하고 정책이 거부로 설정되어 있지만, pct 필드는 100%로 설정되지 않았고, 지정된 도메인의 정책에 따라, 시스템에서 DMARC 작업을 적용하지 않도록 임의로 결정했음을 나타냅니다.|
|header.from|전자 메일 메시지 헤더에서 보낸 사람 주소의 도메인입니다. 이를 _5322.From_이라고도 합니다.|
|compauth|복합 인증 결과 Office 365에서 SPF, DKIM, DMARC 또는 메시지의 기타 부분과 같은 다양한 유형의 인증을 결합하여 메시지의 인증 여부를 확인하는 데 사용됩니다. 평가 기준으로 보낸 사람: 도메인을 사용합니다.|
|이유|복합 인증을 통과 또는 실패한 이유입니다. 이유의 값은 세 자리로 구성됩니다. <br/>• **000**: 인증에 명시적으로 실패한 메시지입니다. 예를 들어, 메시지가 격리 또는 거부 조치와 함께 DMARC 실패를 수신한 경우입니다. <br/>• **001**: 메시지가 암시적으로 인증에 실패하고, 송신 도메인에서 인증 정책을 게시하지 않았습니다. 예를 들어, p=none이라는 DMARC 정책입니다. <br/>• **1xx**: 메시지가 인증을 통과했습니다. 두 번째 두 자리는 Office 365에서 사용하는 내부 코드입니다. <br/>• **2xx**: 메시지가 인증을 소프트 패스했습니다. 두 번째 두 자리는 Office 365에서 사용하는 내부 코드입니다. <br/>• **3xx**: 복합 인증에 대해 메시지를 확인하지 않았습니다. <br/>• **4xx**: 메시지에서 복합 인증을 바이패스했습니다. 두 번째 두 자리는 Office 365에서 사용하는 내부 코드입니다.|
