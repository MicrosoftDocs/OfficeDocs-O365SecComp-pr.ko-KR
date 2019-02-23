---
title: 스팸 방지 메시지 헤더
ms.author: krowley
author: kccross
manager: laurawi
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 2e3fcfc5-5604-4b88-ac0a-c5c45c03f1db
ms.collection:
- M365-security-compliance
description: Exchange Online Protection에서 인바운드 전자 메일 메시지를 검사 하면 각 메시지에 **X-스팸 방지-Report** 헤더가 삽입 됩니다.
ms.openlocfilehash: 4851c05f4db8d120eb54b9c22025fe2972e1e515
ms.sourcegitcommit: a80bd8626720fabdf592b84e4424cd3a83d08280
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30223587"
---
# <a name="anti-spam-message-headers"></a>스팸 방지 메시지 헤더

Exchange Online Protection에서 인바운드 전자 메일 메시지를 검사 하면 각 메시지에 **X-스팸 방지-Report** 헤더가 삽입 됩니다. 이 헤더의 필드를 사용 하면 관리자가 메시지에 대 한 정보를 제공 하 고 처리 된 방법을 확인할 수 있습니다. **스팸 방지** 헤더의 필드는 대량 메일 및 피싱에 대 한 추가 정보를 제공 합니다. Exchange Online Protection은 이러한 두 헤더 외에도 **인증 결과** 헤더에 처리 되는 각 메시지에 대 한 전자 메일 인증 결과를 삽입 합니다.
  
> [!TIP]
> 다양 한 전자 메일 클라이언트에서 전자 메일 메시지 헤더를 보는 방법에 대 한 자세한 내용은 [메시지 헤더 분석기](https://go.microsoft.com/fwlink/p/?LinkId=306583)를 참조 하십시오. 메시지 헤더의 내용을 복사 하 여 [메시지 헤더 분석기](https://testconnectivity.microsoft.com/?tabid=mha) 도구에 붙여 넣을 수 있습니다. Exchange 관리 센터의 격리에서 메시지를 선택 하는 경우 메시지 헤더 텍스트 **** 를 복사 하 여 도구에 붙여 넣을 수도 있습니다. 메시지 헤더 분석 도구에서 머리글 **분석** 을 클릭 하 여 헤더에 대 한 정보를 검색 합니다.
  
## <a name="x-forefront-antispam-report-message-header-fields"></a>스팸 방지-Report 메시지 헤더 필드
<a name="sectionSection0"> </a>

메시지 헤더 정보에 액세스 한 후에는 **스팸 방지-Report** 를 검색 한 다음 이러한 필드를 찾습니다. 이 헤더의 다른 필드는 Microsoft 스팸 방지 팀에서 진단을 위해 단독으로 사용 합니다.

|**헤더 필드**|**설명**|
|:-----|:-----|
|CIP: [IP address]|연결 IP 주소입니다. 연결 필터에 ip 허용 목록 또는 ip 차단 목록을 만들 때이 ip 주소를 지정 해야 할 수 있습니다. 자세한 내용은 [Configure the connection filter policy](configure-the-connection-filter-policy.md)을 참조 하십시오.|
|CTRY|메시지가 서비스에 연결된 국가입니다. 연결하는 IP 주소(원래 메시지를 보낸 IP 주소와 다를 수도 있음)를 통해 확인됩니다.|
|LANG|국가 코드로 지정된 메시지 작성 언어입니다. 예를 들어 ru_RU는 러시아어입니다.|
|SCL|메시지의 SCL (스팸 지 수) 값입니다. 이러한 값을 해석 하는 방법에 대 한 자세한 내용은 [스팸 신뢰 수준](spam-confidence-levels.md)를 참조 하십시오.|
|PCL|메시지의 PCL (피싱 신뢰 수준) 값입니다. |
|SRV:BULK|메시지가 대량 전자 메일 메시지로 식별 되었습니다. **모든 대량 전자 메일 메시지 차단 고급 스팸 필터링 옵션** 을 사용 하도록 설정 하면 스팸으로 표시 됩니다. 이 옵션을 사용 하도록 설정 하지 않으면 나머지 필터링 규칙에 따라 메시지가 스팸으로 확인 되는 경우에만 스팸으로 표시 됩니다.|
|SFV:SFE|개인의 수신 허용-보낸 사람 목록에 있는 주소에서 보낸 메시지 이므로 필터링을 건너 뛰 었으 며 메시지가 허용 됩니다.|
|SFV:BLK|개인의 수신 거부 목록에 있는 주소에서 보낸 메시지 이므로 필터링을 건너 뛰 었으 며 메시지가 차단 되었습니다.  <br/> **팁**: 최종 사용자가 수신 허용 및 차단 된 보낸 사람 목록을 만드는 방법에 대 한 자세한 내용은 [차단 또는 허용 (정크 메일 설정)](https://go.microsoft.com/fwlink/p/?LinkId=294862) (웹용 outlook) 및 [요약 정크 메일 필터](https://go.microsoft.com/fwlink/p/?LinkId=270065) (outlook)를 참조 하세요.|
|IPV:CAL|연결 필터의 IP 허용 목록에 IP 주소가 지정되어 있어 메시지가 스팸 필터를 통과하도록 허용되었습니다.|
|IPV:NLI|IP 주소가 IP 신뢰도 목록에 포함되지 않았습니다.|
|SFV:SPM|메시지가 콘텐츠 필터에 의해 스팸으로 표시되었습니다.|
|SFV:SKS|메시지가 콘텐츠 필터에 의해 처리되기 전에 이미 스팸으로 표시되었습니다. 전송 규칙과 일치하여 스팸으로 자동 표시되고 모든 추가 필터링을 무시하는 메시지가 여기에 포함됩니다.|
|SFV: 고 대 중 A|메시지가 필터링을 무시 하 고 **보낸 사람 허용** 목록과 같은 스팸 필터 정책의 허용 목록과 일치 하 여 받은 편지 함으로 배달 되었습니다.|
|SFV: SKB|메시지가 수신 허용- **차단** 목록과 같은 스팸 필터 정책의 차단 목록과 일치 하므로 스팸으로 표시 되었습니다.|
|SFV:SKN|메시지가 콘텐츠 필터에 의해 처리 되기 전에 스팸이 아닌 것으로 표시 되어 있습니다. 여기에는 메시지가 전송 규칙과 일치 하 여 자동으로 스팸이 아닌 것으로 표시 되 고 모든 추가 필터링을 무시 하는 메시지가 포함 됩니다.|
|SFV:SKI|SFV:SKN와 마찬가지로 다른 이유 때문에 메시지 필터링을 건너뛰었습니다(예: 테넌트 내의 조직 내 전자 메일).|
|SFV:SKQ|메시지가 격리에서 해제되었으며 받는 사람에게 전송되었습니다.|
|SFV:NSPM|메시지가 스팸이 아닌 것으로 표시되었으며 받는 사람에게 전송되었습니다.|
|H: [helostring]|연결하는 메일 서버의 HELO 또는 EHLO 문자열입니다.|
|PTR: [ReverseDNS]|보내는 IP 주소의 PTR 레코드 또는 포인터 레코드 (역방향 DNS 주소 라고도 함)|
|SFTY|메시지가 피싱 메일로 확인 되었으며 다음 값 중 하나로 표시 됩니다. <br/>• 9.1: 기본값 메시지에 피싱 URL이 있거나 다른 피싱 콘텐츠가 포함 될 수 있거나, Office 365에 메시지를 릴레이 하기 전에 Exchange Server 온-프레미스 버전의 다른 메일 필터에서 피싱 메일로 표시 했을 수 있습니다. <br/>• 9.11: 메시지가 실패 함 스푸핑 방지 확인에서 보낸 도메인을 받는 도메인과 동일 하거나 같은 조직의 일부인 경우 메시지를 보내지 못합니다. 이는 조직 내 스푸핑 보안 팁이 메시지에 추가 됨을 나타냅니다. <br/>• 9.19: 보내는 도메인에서 받는 사람이 소유한 도메인을 가장 하는 중이거나 피싱 방지 정책에 의해 보호 되는 사용자 지정 도메인을 사용 하려고 시도 하는 메시지가 실패 함 도메인 가장 검사입니다. 이는 Phishig 정책을 통해 사용 하도록 설정 된 경우 메시지에 가장 안전 팁이 추가 됨을 의미 합니다. <br/>• 9.20: 메시지 실패 사용자 가장은 보내는 사용자가 수신자 조직 내에서 사용자를 가장 하 려 하는지, 아니면 피싱 방지 정책으로 보호 되는 사용자 지정 사용자 인지를 확인 합니다. 이는 Phishig 정책을 통해 사용 하도록 설정 된 경우 메시지에 가장 안전 팁이 추가 됨을 의미 합니다. <br/>• 9.21: 메시지에서 스푸핑 방지 검사를 수행 하지 못했으며 From: 헤더의 보내는 도메인이 인증 되지 않으며 외부 도메인에서 온 것입니다. compauth와 함께 사용 됩니다 (인증-결과 참조). <br/>• 9.22: 사용자에 게 재정의 된 수신 허용 보낸 사람이 있다는 점을 제외 하 고 9.21과 동일 합니다. <br/>• 9.23: 조직에 재정의 된 허용 된 보낸 사람 또는 도메인이 있다는 점을 제외 하 고 9.22과 동일 합니다. <br/>• 9.24: 사용자에 게 재정의 된 Exchange 메일 흐름 규칙이 있다는 점을 제외 하 고는 9.23와 동일 합니다.|
|X-CustomSpam: [ASFOption]|메시지가 고급 스팸 필터링 옵션과 일치 합니다. 예를 들어, **X-customspam: 원격 사이트에 대** 한 이미지 링크는 **원격 사이트에 대 한 이미지 링크** ASF 옵션을 일치 시키는 것을 나타냅니다. 각 특정 ASF 옵션에 대해 추가 된 X-헤더 텍스트를 확인 하려면 [고급 스팸 필터링 옵션](advanced-spam-filtering-asf-options.md)을 참조 하십시오.|
   
## <a name="x-microsoft-antispam-message-header-fields"></a>스팸 방지 메시지 헤더 필드
<a name="sectionSection1"> </a>

다음 표에서는 **스팸 방지** 메시지 헤더의 유용한 필드에 대해 설명 합니다. 이 헤더의 다른 필드는 Microsoft 스팸 방지 팀에서 진단을 위해 단독으로 사용 합니다.
  
|**헤더 필드**|**설명**|
|:-----|:-----|
|c|메시지의 BCL (대량 불만 수준)입니다. 자세한 내용은 [대량 불만 수준 값](bulk-complaint-level-values.md)을 참조 하십시오.|
|PCL|메시지의 PCL (피싱 신뢰 수준)으로, 피싱 메시지 인지 여부를 나타냅니다. 이 상태는 다음 숫자 값 중 하나로 반환 될 수 있습니다.<br/>• **0-3**: 메시지의 콘텐츠가 피싱 일 가능성이 없습니다. <br/>• **4-8**: 메시지의 콘텐츠가 피싱 일 가능성이 있습니다. <br/>• **-9990**: (Exchange Online Protection만 해당) 메시지의 콘텐츠가 피싱 일 가능성이 있습니다.  <br/>  값은 전자 메일 클라이언트가 메시지에 대해 수행 하는 작업을 확인 하는 데 사용 됩니다. 예를 들어 Outlook에서는 PCL 스탬프를 사용 하 여 의심 스러운 메시지의 콘텐츠를 차단 합니다. 피싱에 대 한 자세한 내용과 Outlook에서 피싱 메시지를 처리 하는 방법에 대 한 자세한 내용은 [전자 메일 메시지에서 링크 설정 또는 해제](https://support.office.com/article/2D79B907-93B6-4774-82E6-1F0385CF20F8)를 참조 하세요.|
   
## <a name="authentication-results-message-header"></a>인증-결과 메시지 헤더
<a name="sectionSection2"> </a>

메일 서버에서 전자 메일 메시지를 받을 때 SPF, dkim 및 DMARC에 대 한 검사 결과는 **인증 결과** 메시지 헤더의 Office 365에 의해 기록 되거나 스탬프 처리 됩니다.
  
### <a name="check-stamp-syntax-and-examples"></a>검사 스탬프 구문 및 예
<a name="referenceSPFstamp"> </a>

다음 구문 예에서는 메일 서버에서 받은 전자 메일 인증 검사를 수행 하는 각 전자 메일에 대해 Office 365에서 메시지 헤더에 적용 되는 "스탬프" 텍스트 부분을 보여 줍니다. 스탬프가 **인증 결과** 헤더에 추가 됩니다.
  
 **구문: SPF 검사 스탬프**
  
SPF의 경우 다음 구문이 적용 됩니다.
  
```
spf=<pass (IP address)|fail (IP address)|softfail (reason)|neutral|none|temperror|permerror> smtp.mailfrom=<domain>
```

 **예: SPF 체크 스탬프**
  
```
spf=pass (sender IP is 192.168.0.1) smtp.mailfrom=contoso.com
spf=fail (sender IP is 127.0.0.1) smtp.mailfrom=contoso.com
```

 **구문: dkim 검사 스탬프**
  
dkim의 경우 다음 구문이 적용 됩니다.
  
```
dkim=<pass|fail (reason)|none> header.d=<domain>
```

 **예: dkim 검사 스탬프**
  
```
dkim=pass (signature was verified) header.d=contoso.com
dkim=fail (body hash did not verify) header.d=contoso.com
```

 **구문: DMARC 검사 스탬프**
  
DMARC의 경우 다음 구문이 적용 됩니다.
  
```
dmarc=<pass|fail|bestguesspass|none> action=<permerror|temperror|oreject|pct.quarantine|pct.reject> header.from=<domain>
```

 **예: DMARC check 스탬프**
  
```
dmarc=pass action=none header.from=contoso.com
dmarc=bestguesspass action=none header.from=contoso.com
dmarc=fail action=none header.from=contoso.com
dmarc=fail action=oreject header.from=contoso.com
```

### <a name="authentication-results-message-header-fields-used-by-office-365-email-authentication"></a>인증-Office 365 전자 메일 인증에서 사용 되는 결과 메시지 헤더 필드
<a name="referenceSPFstamp"> </a>

이 표에서는 각 전자 메일 인증 확인에 사용할 수 있는 필드 및 값을 설명 합니다.
  
|**헤더 필드**|**설명**|
|:-----|:-----|
|spf|메시지에 대 한 SPF 확인 결과를 설명 합니다. 가능한 값은 다음과 같습니다.<br/>• **통과 (IP 주소)**: 전달 된 메시지에 대 한 SPF 확인을 나타내고 보낸 사람의 IP 주소를 포함 합니다. 클라이언트에는 보낸 사람의 도메인을 대신 하 여 전자 메일을 보내거나 릴레이할 수 있는 권한이 부여 됩니다.<br/>• **fail (IP 주소)**: 메시지에 대 한 SPF 검사가 실패 했음을 나타내고 보낸 사람의 IP 주소를 포함 합니다. 이것을 _하드 오류가_라고도 합니다.<br/>• **소프트 실패 (이유)**: SPF 레코드에서 호스트가 송신이 허용 되지 않고 전환 중인 것으로 지정 되었음을 나타냅니다. <br/>• **중립**: SPF 레코드에 IP 주소에 대 한 권한 부여 여부를 어설션 하지 않음을 명시적으로 언급 했음을 나타냅니다. <br/>• **없음**: 도메인에 spf 레코드가 없거나 spf 레코드가 결과를 평가 하지 않음을 나타냅니다. <br/>• **temperror**: 예를 들어 DNS 오류와 같이 일시적인 오류로 인해 오류가 발생 했음을 나타냅니다. 나중에 다시 시도 하면 관리자 작업 없이 성공할 수 있습니다.<br/>• **permerror**: 영구 오류가 발생 했음을 나타냅니다. 예를 들어 도메인에 잘못 된 형식의 SPF 레코드가 있는 경우 이러한 상황이 발생 합니다.|
|smtp. 보낸 사람|메시지를 보낸 원본 도메인을 포함 합니다. 이 전자 메일 메시지에 대 한 모든 오류는 전자 메일 관리자 또는 도메인을 담당 하는 엔터티로 전송 됩니다. 이를 메시지 봉투의 5321 주소 또는 역 경로 주소 라고도 합니다.|
|dkim|메시지에 대 한 dkim 검사 결과를 설명 합니다. 가능한 값은 다음과 같습니다.<br/>• **pass**: 전달 된 메시지에 대 한 dkim 확인을 나타냅니다. <br/>• **fail (reason)**: 메시지에 대 한 dkim 확인이 실패 하 고 이유를 나타냅니다. 예를 들어 메시지에 서명이 없거나 서명이 확인 되지 않은 경우에 발생 합니다.<br/>• **없음**: 메시지가 서명 되지 않았음을 나타냅니다. 이는 도메인에 dkim 레코드가 있거나 dkim 레코드가 결과를 확인 하지 않거나 해당 메시지가 서명 되지 않았다는 것을 나타낼 수도 있고 그렇지 않을 수도 있습니다.|
|머리말. d|dkim 서명 (있는 경우)에서 식별 된 도메인 공개 키에 대해 쿼리 된 도메인입니다.|
|dmarc|메시지에 대 한 DMARC 검사 결과를 설명 합니다. 가능한 값은 다음과 같습니다.<br/>• **pass**: 전달 된 메시지에 대 한 DMARC 확인을 나타냅니다. <br/>• **fail**: 메시지에 대 한 DMARC 확인이 실패 했음을 나타냅니다. <br/>• **bestguesspass**: 도메인에 대 한 DMARC TXT 레코드가 없으며, 이미 존재 하는 경우에는 메시지에 대 한 DMARC 확인이 통과 되었음을 나타냅니다. 이는 5321 보낸 사람 주소의 도메인이 5322.from 주소의 주소에 있는 도메인과 일치 하기 때문입니다.<br/>• **none**: DNS에 보내는 도메인에 대 한 dkim TXT 레코드가 없음을 나타냅니다.|
|동작|DMARC 검사 결과에 따라 스팸 필터가 수행 하는 작업을 나타냅니다. 예를 들어:<br/>• **permerror**: DNS에서 잘못 된 형식의 DMARC TXT 레코드를 발생 하는 등 DMARC 평가 중에 영구 오류가 발생 했습니다. 이 메시지를 다시 전송 하는 것이 다른 결과로 끝나는 것은 아닙니다. 대신, 문제를 해결 하기 위해 도메인 소유자에 게 문의 해야 할 수도 있습니다.<br/>• **temperror**: DMARC 평가 중에 일시적인 오류가 발생 했습니다. 전자 메일을 제대로 처리 하기 위해 보낸 사람이 나중에 메시지를 다시 보내도록 요청할 수 있습니다.<br/>• **oreject** 않음 ****: 무시 거부를 나타냅니다. 이 경우 Office 365에서는 DMARC TXT 레코드의 정책이 p = 거부 인 도메인의 DMARC 확인이 실패 하는 메시지를 받을 때이 동작을 사용 합니다. 메시지를 삭제 하거나 거부 하는 대신 Office 365에서 메시지를 스팸으로 표시 합니다. 이러한 방식으로 office 365이 구성 되는 이유에 대 한 자세한 내용은 [office 365에서 DMARC에 실패 한 인바운드 전자 메일을 처리 하는 방법을](use-dmarc-to-validate-email.md#inbounddmarcfail)참조 하세요.<br/>• **pct**: DMARC을 통과 하지 않는 메시지의 100% 미만이 배달 됨을 나타냅니다. 즉, 메시지가 DMARC 실패 하 고 정책이 격리로 설정 되었지만 지정 된 도메인의 정책에 따라 pct 필드가 100%로 설정 되지 않았으므로 시스템에서 DMARC 작업을 적용 하지 않도록 임의로 결정 됩니다.<br/>• **pct**: DMARC를 통과 하지 못하는 메시지의 비율 (%)이 배달 되지 않음을 나타냅니다. 즉, 메시지가 DMARC 실패 하 고 정책이 거부로 설정 되었는데, pct 필드가 지정 된 도메인의 정책에 따라 DMARC 작업을 적용 하지 않도록 임의로 결정 됩니다.|
|머리글 원본|전자 메일 메시지 헤더에 있는 보낸 사람 주소의 도메인입니다. 이를 _5322.from 주소의_ 주소 라고도 합니다.|
|compauth|복합 인증 결과입니다. Office 365에서 사용 하 여 SPF, dkim, DMARC 또는 기타 메시지 부분과 같은 여러 유형의 인증을 결합 하 여 메시지가 인증 되는지 여부를 확인 합니다. 평가의 기반으로 From: 도메인을 사용 합니다.|
|이유|복합 인증이 통과 또는 실패 한 이유입니다. 원인 값은 세 자리 숫자로 구성 됩니다.<br/>• **000**: 메시지가 명시적으로 인증에 실패 했습니다. 예를 들어 메시지에 격리 또는 거부 작업을 포함 하 여 DMARC가 수신 되지 않습니다.<br/>• **001**: 메시지가 암시적으로 인증에 실패 했으며, 보내는 도메인에서 인증 정책을 게시 하지 않았습니다. 예를 들어 DMARC 정책을 p = 없음으로 만듭니다.<br/>• **1xx**: 메시지가 인증을 통과 했습니다. 두 번째 두 자리 숫자는 Office 365에서 사용 되는 내부 코드입니다.<br/>• **2xx**: 메시지 소프트 통과 인증 두 번째 두 자리 숫자는 Office 365에서 사용 되는 내부 코드입니다.<br/>• **3xx**: 메시지의 복합 인증을 확인 하지 않았습니다. <br/>• **4xx**: 메시지가 복합 인증을 무시 했습니다. 두 번째 두 자리 숫자는 Office 365에서 사용 되는 내부 코드입니다.|
