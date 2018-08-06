---
title: 스팸 방지 메시지 헤더
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 2/9/2018
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
ms.assetid: 2e3fcfc5-5604-4b88-ac0a-c5c45c03f1db
description: Exchange Online Protection 인바운드 전자 메일 메시지를 검색 하는 경우 **X Forefront-스팸 방지 보고서** 머리글은 각 메시지에 삽입 합니다.
ms.openlocfilehash: 7baa15f4d687c809d45461a135f64f0d18f49a7f
ms.sourcegitcommit: 22bca85c3c6d946083d3784f72e886c068d49f4a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/06/2018
ms.locfileid: "22026505"
---
# <a name="anti-spam-message-headers"></a>스팸 방지 메시지 헤더

Exchange Online Protection 인바운드 전자 메일 메시지를 검색 하는 경우 **X Forefront-스팸 방지 보고서** 머리글은 각 메시지에 삽입 합니다. 이 헤더의 필드 관리자에 게 메시지를 처리 한 방식에 대 한 정보가 제공 하는 데 도움이 됩니다. **스팸 방지 Microsoft-X-** 헤더에 있는 필드는 대량 메일 및 피싱에 대 한 추가 정보를 제공 합니다. 이러한 두 헤더 외에도 Exchange Online Protection **인증 결과** 헤더에서 처리 하는 각 메시지에 대 한 전자 메일 인증 결과 삽입 합니다. 
  
> [!TIP]
> 다양 한 전자 메일 클라이언트에서 전자 메일 메시지 머리글을 확인 하는 방법에 대 한 정보를 [메시지 헤더 분석기](https://go.microsoft.com/fwlink/p/?LinkId=306583)를 참조 하십시오. 복사 하 고 메시지 머리글의 내용을 [메시지 헤더 분석기](https://testconnectivity.microsoft.com/?tabid=mha) 도구에 붙여넣을 수 있습니다. Exchange 관리 센터에서 사용자를 격리에서 메시지를 선택 하는 경우 **메시지 헤더 보기** 링크도 쉽게 사용 하면 복사 하는 도구에 메시지 머리글 텍스트를 붙여넣습니다. 한번 메시지 헤더 분석기 도구에서 머리글에 대 한 정보를 검색 하기 위해 **분석 머리글** 을 클릭 합니다. 
  
## <a name="x-forefront-antispam-report-message-header-fields"></a>X-Forefront-스팸 방지-보고서 메시지 헤더 필드
<a name="sectionSection0"> </a>

메시지 헤더 정보에 액세스 한 후 **X Forefront-스팸 방지 보고서** 에 대 한 검색 하 고 이러한 필드를 찾습니다. 이 헤더의 다른 필드는 진단 목적을 위해 Microsoft 스팸 방지 팀에서 단독으로 사용 됩니다. 
  
|||
|:-----|:-----|
|**헤더 필드** <br/> |**설명** <br/> |
|CIP: [IP address]  <br/> |연결 IP 주소입니다. 연결 필터에서 IP 허용 목록 또는 IP 차단 목록을 만들 때이 IP 주소를 지정할 수도 있습니다. 자세한 내용은 [연결 필터 정책 구성](configure-the-connection-filter-policy.md)을 참조 하십시오.<br/> |
|CTRY  <br/> |메시지가 서비스에 연결된 국가입니다. 연결하는 IP 주소(원래 메시지를 보낸 IP 주소와 다를 수도 있음)를 통해 확인됩니다.  <br/> |
|LANG  <br/> |국가 코드로 지정된 메시지 작성 언어입니다. 예를 들어 ru_RU는 러시아어입니다.  <br/> |
|SCL  <br/> |메시지의 스팸 SCL () 값입니다. 이러한 값을 해석 하는 방법에 대 한 자세한 내용은 [Spam confidence levels](spam-confidence-levels.md)를 참조 하십시오.<br/> |
|PCL  <br/> |메시지의 피싱 신뢰 수준 (PCL) 값입니다. PCL 값에 대 한 자세한 내용은 [PCL](anti-spam-message-headers.md#PCL) 을 참조 하십시오.<br/> |
|SRV:BULK  <br/> |메시지는 대량 전자 메일 메시지를으로 확인 되었습니다. 사용 하는 **모든 대량 전자 메일 메시지 고급 스팸 필터링 옵션을 차단** 하는 경우 스팸으로 표시 됩니다. 사용할 수 없는 필터링 규칙의 나머지 부분 메시지가 스팸 인지를 결정 하는 경우 스팸으로 표시만 됩니다.<br/> |
|SFV:SFE  <br/> |필터링을 건너뛰었습니다 하 고 각 사용자의 수신 허용-보낸사람 목록에 있는 주소에서 보낸 메시지를 통해 허용 되었습니다.  <br/> |
|SFV:BLK  <br/> |필터링을 건너뛰었습니다 및 수신된 거부 목록에는 각 사용자의 주소에서 보낸 메시지 차단 되었습니다.  <br/> **팁:** 최종 사용자가 안전 하 고 차단 된 보낸사람 목록을 만들 수 있는 방법에 대 한 자세한 내용은 참조 [차단 또는 허용 (정크 메일 설정)](https://go.microsoft.com/fwlink/p/?LinkId=294862) (OWA) 및 [정크 메일 필터 개요](https://go.microsoft.com/fwlink/p/?LinkId=270065) (Outlook).  <br/> |
|IPV:CAL  <br/> |연결 필터의 IP 허용 목록에 IP 주소가 지정되어 있어 메시지가 스팸 필터를 통과하도록 허용되었습니다.  <br/> |
|IPV:NLI  <br/> |IP 주소가 IP 신뢰도 목록에 포함되지 않았습니다.  <br/> |
|SFV:SPM  <br/> |메시지가 콘텐츠 필터에 의해 스팸으로 표시되었습니다.  <br/> |
|SFV:SKS  <br/> |메시지가 콘텐츠 필터에 의해 처리되기 전에 이미 스팸으로 표시되었습니다. 전송 규칙과 일치하여 스팸으로 자동 표시되고 모든 추가 필터링을 무시하는 메시지가 여기에 포함됩니다.  <br/> |
|SFV:SKA  <br/> |메시지 필터링 및 스팸 필터 정책 등 **보낸사람 허용** 목록에에서는 허용 목록 일치 하기 때문에 받은 편지함에 배달 되었습니다.  <br/> |
|SFV:SKB  <br/> |메시지가 스팸 필터 정책 **보낸 사람이 차단** 목록 등의 차단 목록 일치 하기 때문에 스팸으로 표시 되었습니다.  <br/> |
|SFV:SKN  <br/> |메시지가 스팸이 아닌 콘텐츠 필터에 의해 처리 중인 하기 전에으로 표시 되었습니다. 이 메시지는 메시지를 자동으로 스팸이 아닌으로 표시 하 고 모든 추가 필터링이 무시 전송 규칙과 일치 하는 위치를 포함 합니다.  <br/> |
|SFV:SKI  <br/> |SFV:SKN와 마찬가지로 다른 이유 때문에 메시지 필터링을 건너뛰었습니다(예: 테넌트 내의 조직 내 전자 메일).  <br/> |
|SFV:SKQ  <br/> |메시지가 격리에서 해제되었으며 받는 사람에게 전송되었습니다.  <br/> |
|SFV:NSPM  <br/> |메시지가 스팸이 아닌 것으로 표시되었으며 받는 사람에게 전송되었습니다.  <br/> |
|H: [helostring]  <br/> |연결하는 메일 서버의 HELO 또는 EHLO 문자열입니다.  <br/> |
|PTR: [ReverseDNS]  <br/> |PTR 레코드 또는 포인터 레코드의 경우 보내는 IP 주소의 역방향 DNS 주소 라고도 합니다.  <br/> |
|SFTY  <br/> | 메시지 피싱으로 식별 된 하 고 다음 값 중 하나로 표시 됩니다.  <br/>  9.1-기본값입니다. 메시지 피싱 URL을 포함 하 고 다른 피싱 콘텐츠를 포함할 수 또는 수으로 표시 된 피싱은 온-프레미스 버전의 Exchange Server와 같은 다른 메일 필터에 의해 Office 365에 메시지를 릴레이 하기 전에 합니다.  <br/>  9.11-메시지 스푸핑 방지 검사 하지 못했습니다. 위치에서 보내는 도메인: 헤더에 맞춥니다 또는 도메인 수신을와 같은 조직의 일부인와 같습니다.  <br/>  9.21-메시지 실패 스푸핑 방지 검사 및 from에서을 보내는 도메인: 헤더를 인증 하지 않습니다. CompAuth과 함께 사용 (결과 인증 참조).  <br/>  9.22-사용자에 게 재정의 하는 수신 허용-보낸사람 된다는 점을 제외 하면 9.21와 동일 합니다.  <br/>  9.23-조직에는 허용 된 보낸 사람이 나 재정의 되었지만 도메인 된다는 점을 제외 하면 9.22와 동일 합니다.  <br/>  9.23, 동일 9.24-사용자에 게 하는 규칙 하는 Exchange 메일 흐름 된다는 점을 제외 하면 재정의 되었습니다.  <br/> |
|X-CustomSpam: [ASFOption]  <br/> |메시지는 고급 스팸 필터링 옵션을 일치 시킵니다. 예, **X-customspam: 원격 사이트에 대 한 링크를 이미지** **원격 사이트에 대 한 이미지 링크** ASF 옵션 일치를 나타냅니다. 어떤 X-헤더 텍스트를 각 특정 ASF 옵션에 대 한 추가 찾으려면 [고급 스팸 필터링 옵션을](advanced-spam-filtering-asf-options.md)참조 하십시오.<br/> |
   
## <a name="x-microsoft-antispam-message-header-fields"></a>X-Microsoft-스팸 방지 메시지 헤더 필드
<a name="sectionSection1"> </a>

다음 표에서 **X-Microsoft-스팸 방지** 메시지 헤더에 유용한 필드에 설명 합니다. 이 헤더의 다른 필드는 진단 목적을 위해 Microsoft 스팸 방지 팀에서 단독으로 사용 됩니다. 
  
|||
|:-----|:-----|
|**헤더 필드** <br/> |**설명** <br/> |
|BCL  <br/> |대량 불만 수준 (BCL) 메시지입니다. 자세한 내용은 [대량 불만 수준 값](bulk-complaint-level-values.md)을 참조 하십시오.<br/> |
|PCL  <br/> | 피싱 신뢰 수준 (PCL)의 메시지를 피싱 메시지 인지를 나타냅니다.  <br/>  이 상태는 다음 숫자 값 중 하나로 반환 될 수 있습니다.  <br/> **0-3** 에 메시지의 내용을 피싱 수 없습니다.  <br/> **4-8** 메시지의 콘텐츠를 피싱 될 가능성이 있습니다.  <br/> **-9990** (Exchange Online Protection만) 메시지의 콘텐츠를 피싱 될 가능성이 있습니다.  <br/>  메시지에 전자 메일 클라이언트는 작업을 결정 값 사용 됩니다. 예, Microsoft Office Outlook PCL 스탬프를 사용 하 여 의심 스러운 메시지의 콘텐츠를 차단 합니다. 피싱, 및 Outlook 피싱 메시지를 처리 하는 방법에 대 한 자세한 내용은 [설정 또는 해제 전자 메일 메시지에 대 한 링크를](https://support.office.com/article/2D79B907-93B6-4774-82E6-1F0385CF20F8)참조 하십시오.<br/> |
   
## <a name="authentication-results-message-header"></a>인증 결과 메시지 헤더
<a name="sectionSection2"> </a>

SPF, DKIM, 및 DMARC에 대 한 검사의 결과, 기록 또는 사용해 메일 서버 전자 메일 메시지를 받을 때 **인증 결과** 메시지 헤더에서 Office 365에서 스탬프 처리 합니다. 
  
### <a name="check-stamp-syntax-and-examples"></a>체크 스탬프 구문 및 예
<a name="referenceSPFstamp"> </a>

다음 구문 예제는 "스탬프" Office 365 명의 메일 서버에서 수신 되는 경우에 전자 메일 인증 검사를 거치는 각 전자 메일에 대 한 메시지 머리글에 적용 되는 텍스트의 일부를 보여줍니다. 스탬프 **인증 결과** 헤더에 추가 됩니다. 
  
 **구문: SPF 체크 스탬프**
  
SPF, 다음 구문을 적용 됩니다.
  
```
spf=<pass (IP address)|fail (IP address)|softfail (reason)|neutral|none|temperror|permerror> smtp.mailfrom=<domain>
```

 **예: SPF 체크 스탬프**
  
```
spf=pass (sender IP is 192.168.0.1) smtp.mailfrom=contoso.com
spf=fail (sender IP is 127.0.0.1) smtp.mailfrom=contoso.com

```

 **구문: DKIM 체크 스탬프**
  
DKIM, 다음 구문을 적용 됩니다.
  
```
dkim=<pass|fail (reason)|none> header.d=<domain>
```

 **예: DKIM 체크 스탬프**
  
```
dkim=pass (signature was verified) header.d=contoso.com
dkim=fail (body hash did not verify) header.d=contoso.com
```

 **구문: DMARC 체크 스탬프**
  
DMARC, 다음 구문을 적용 됩니다.
  
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

### <a name="authentication-results-message-header-fields-used-by-office-365-email-authentication"></a>인증 결과 메시지 헤더 필드를 사용 하 여 Office 365 전자 메일 인증
<a name="referenceSPFstamp"> </a>

이 테이블에 필드 및 각 전자 메일 인증 검사에 사용 가능한 값에 설명 합니다.
  
|**헤더 필드**|**설명**|
|:-----|:-----|
|spf  <br/> | 메시지에 대 한 SPF 검사의 결과 설명 합니다. 가능한 값은 다음과 같습니다.<br/> 메시지에 대 한 SPF 확인 전달 되 고 보낸 사람의 IP 주소가 포함을 나타냅니다 **(IP 주소)를 전달** 합니다. 클라이언트를 보내거나 보낸 사람의 도메인을 대신 하 여 전자 메일을 릴레이 권한이 있습니다.<br/> 실패 하 고 보낸 사람의 IP 주소를 포함 하는 메시지에 대 한 SPF 확인 **실패 (IP 주소)를** 나타냅니다. 이 하드 실패를 라고도 합니다.<br/> SPF 레코드를 보낼 수 없을으로 호스트 지정한 하지만 전환에 **softfail (이유)를** 나타냅니다.  <br/> **중립** 는 SPF 레코드는 명시적으로 지정 하지 IP 주소 권한이 있는지 여부 가정는 것을 나타냅니다.  <br/> **none** 또는 있음을 나타냅니다 SPF 레코드는 도메인에 없는 SPF 레코드 결과 계산 되지 않습니다.  <br/> **temperror** 오류가 발생 했음을 나타냅니다는 원래, 예: DNS 오류 임시 수 있습니다. 관리자 작업 없이 나중에 다시 성공할 수도 시도 합니다.<br/> **permerror** 영구 오류가 발생 했음을 나타냅니다. 이 예는 도메인에 SPF 레코드를 잘못 서식이 지정 된 경우 발생 합니다.<br/> |
|smtp.mailfrom  <br/> |메시지를 보낸 원본 도메인을 포함 합니다. 이 전자 메일 메시지에 대 한 모든 오류는 전자 메일 관리자 또는 도메인에 대 한 책임을 집니다 엔터티에 전송 됩니다. 이 방법을 라고도 5321.MailFrom 주소 또는 역방향 경로 주소 메시지 봉투의 합니다.  <br/> |
|dkim  <br/> | 메시지에 대 한 DKIM 검사의 결과 설명 합니다. 가능한 값은 다음과 같습니다.<br/> **전달** 전달 된 메시지에 대 한 DKIM 확인을 나타냅니다.  <br/> 실패 한 메시지에 대 한 DKIM 확인을 나타냅니다 **(이유) 실패** 및 그 이유입니다. 예, 메시지가 서명 되지 않은 경우 또는 서명을 확인 하지 못했습니다.<br/> **none** 메시지가 서명 되지 않은 것을 나타냅니다. 이 수도 있고 그렇지는 도메인에 DKIM 레코드 또는 DKIM 레코드를 결과에이 메시지 서명 되지 않았습니다 계산 되지 않습니다 표시 되지 않습니다.<br/> |
|header.d  <br/> |있는 경우에 DKIM 서명을에서 식별 하는 도메인입니다. 이것은 공용 키에 대 한 쿼리는 도메인입니다.  <br/> |
|dmarc  <br/> | 메시지에 대 한 DMARC 검사의 결과 설명 합니다. 가능한 값은 다음과 같습니다.<br/> **전달** 전달 된 메시지에 대 한 DMARC 검사를 나타냅니다.  <br/> **실패** 실패 메시지에 대 한 DMARC 검사를 나타냅니다.  <br/> 도메인에 대 한 DMARC TXT 레코드가 없으면이 있지만 여기에서 제공 했던 하나 하는 경우 메시지에 대해 DMARC 검사를 통과 하는 **bestguesspass** 를 나타냅니다. 5322.From 주소에 도메인을 일치 하는 5321.MailFrom 주소에 도메인 때문입니다.<br/> **none** DNS에서 보내는 도메인에 대 한 DKIM TXT 레코드가 있는지를 나타냅니다.  <br/> |
|동작  <br/> | DMARC 검사의 결과에 따라 스팸 필터에 의해 수행 되는 작업을 나타냅니다. 예를 들어:<br/> **permerror** DNS의 형식이 잘못 된 DMARC TXT 레코드를 발생 하는 등의 DMARC 평가 하는 동안 영구 오류가 발생 했습니다. 이 메시지를 재전송을 시도 하지 못하게 다른 결과 함께 될 수 없습니다. 대신, 문제를 해결 하기 위해 도메인의 소유자에 게 문의 해야할 수 있습니다.<br/> **temperror** DMARC 평가 하는 동안 일시적인 오류가 발생 했습니다. 보낸 전자 메일을 제대로 처리 하기 위해 나중에 메시지를 재전송를 요청할 수 있습니다.<br/> **oreject** 또는 **o.reject** 재정의 거부에 대 한 의미합니다. 이 경우 Office 365 사용 하 여이 작업은 DMARC 실패 하는 메시지를 받을 때 해당 DMARC TXT 레코드에는 정책이 p의 도메인 확인 = 거부 합니다. 삭제 또는 메시지를 거부 하는 대신 Office 365 스팸 메시지를 표시 합니다. 대 한 자세한 내용은 Office 365가 이러한 방식으로 구성 된 이유를 [DMARC에 실패 하는 전자 메일의 인바운드 Office 365 어떻게 핸들](use-dmarc-to-validate-email.md#inbounddmarcfail)을 참조 합니다.<br/> DMARC를 전달 하지 않는 메시지의 100% 보다 작은 백분율 엔터티입니다 배달 될 **pct.quarantine** 나타냅니다. 즉, 메시지 DMARC 실패 하 고 정책, 격리로 설정 된 하지만 pct 필드 100%로 설정 되지 않았습니다 시스템에 지정 된 도메인의 정책에 따라 DMARC 작업을 적용 하지 임의로 결정 합니다.<br/> DMARC를 전달 하지 않는 메시지의 100% 보다 작은 백분율 엔터티입니다 배달 될 **pct.reject** 나타냅니다. 즉, 메시지 DMARC 실패 하 고 정책을 거부 하 고로 설정 된 하지만 pct 필드 100%로 설정 되지 않았습니다 시스템에 지정 된 도메인의 정책에 따라 DMARC 작업을 적용 하지 임의로 결정 합니다.<br/> |
|header.from  <br/> |전자 메일 메시지 머리글에 보낸사람 주소의 도메인입니다. 이 방법을 5322.From 주소를 라고도 합니다.  <br/> |
|compauth  <br/> |복합 인증 결과입니다. Office 365 결합 하는 여러 유형의 SPF, DKIM, DMARC, 또는 다른 부분이 메시지 인증 된 여부를 결정 하는 메시지의 예: 인증에 사용 됩니다. From를 사용 하 여: 도메인 계산의 기준으로 합니다.  <br/> |
|이유  <br/> | 이유 복합 인증 통과 했는지 아니면 실패 합니다. 원인에 대 한 값은 세 자리 숫자의 요소로 이루어집니다.  <br/>  000-메시지 인증을 명시적으로 실패 합니다. 예, 메시지는 다른 작업을 격리 또는 reject의 DMARC 실패를 받았습니다.  <br/>  001-메시지 인증을를 암시적으로 실패 하 고 보내는 도메인 인증 정책을 게시 하지 않은 키를 누릅니다. 예: p의 DMARC 정책 = 없음.  <br/>  1xx-메시지 인증에 전달 합니다. 그 다음 두 자리 숫자는 Office 365에서 사용 하는 내부 코드입니다.  <br/>  2xx-메시지 일시 전달 인증 합니다. 그 다음 두 자리 숫자는 Office 365에서 사용 하는 내부 코드입니다.  <br/>  복합 인증에 대 한 3xx-메시지를 검사 하지 않았습니다.  <br/>  4xx-메시지가 복합 인증을 무시 합니다. 그 다음 두 자리 숫자는 Office 365에서 사용 하는 내부 코드입니다.  <br/> |
  