---
title: Office 365의 스푸핑 방지 보호 기능
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 12/06/2018
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: d24bb387-c65d-486e-93e7-06a4f1a436c0
description: 이 문서에서는 방법 Office 365을 완화 피싱 공격에 대해 사용 하 여 보낸 사람이 도메인, 위장 된 도메인, 즉 위조를 설명 합니다. 메시지를 분석 하 여이 기능을 수행 하기 및 neithe 표준 전자 메일 인증 방법 및 기타 보낸사람 신뢰도 기술을 사용 하 여 인증 될 수 있는 위치를 차단 합니다. 이 변경 피싱 공격에 노출 되는 조직에서 Office 365의 수를 줄이는 구현 됩니다.
ms.openlocfilehash: 19e7ea957592a486a559dac222a51139bf79b574
ms.sourcegitcommit: 03e64ead7805f3dfa9149252be8606efe50375df
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/08/2019
ms.locfileid: "27769862"
---
# <a name="anti-spoofing-protection-in-office-365"></a>Office 365의 스푸핑 방지 보호 기능

이 문서에서는 방법 Office 365을 완화 피싱 공격에 대해 사용 하 여 보낸 사람이 도메인, 위장 된 도메인, 즉 위조를 설명 합니다. 메시지를 분석 하 고 전자 메일 표준 인증 방법 및 기타 보낸사람 신뢰도 기술을 사용 하 여 인증할 수 없는 것을 차단 하 여 수행 합니다. 이 변경 피싱 공격에 노출 되는 고객의 수를 줄이는 구현 됩니다.
  
이 문서에서는 또한이 변경이 수행 되는 이유, 수이 변경에 대 한 고객을 준비 하는 방법을, 영향을 받을 메시지를 확인 하는 방법, 메시지를 보고 하는 방법, 가양성을 완화 하는 방법으로 해야이 대 한 Microsoft에 보낸사람을 준비 하는 방법을 설명합니다 이 옵션을 변경 합니다.
  
Microsoft의 스푸핑 방지 기술 Office 365 Enterprise e 5 구독 명의 또는 구독에 대 한 Office 365 고급 위협 보호 (ATP) 추가 기능을 구입 명의 하는 해당 조직에 처음 배포 되었습니다. 년 10 월 2018를 기준으로 보호 하는 조직에서는 Exchange Online Protection (EOP)도를 확장 했을 때 했습니다. 또한이 필터는 모든 서로에서 설명 하는 방식 때문에 Outlook.com 사용자도 영향을 받을 수 있습니다.
  
## <a name="how-spoofing-is-used-in-phishing-attacks"></a>피싱 공격에 스푸핑 사용 방법

와 관련해 서 해당 사용자를 보호 하기 위해 Microsoft 피싱의 위협을 심각 하 게 됩니다. 스팸 및 피셔 일반적으로 사용 하는 방법 중 하나는 스푸핑, 보낸 사람이 위조는 때은 하 고 보낸 사람이 보낸 또는 실제 원본 이외의 라는 메시지가 나타납니다. 이 기술은 사용자 자격 증명을 받을 수 있도록 디자인 피싱 캠페인에 종종 사용 됩니다. Microsoft의 스푸핑 방지 기술 특히 위조를 검사 하는 '에서: 헤더 ' Outlook 같은 전자 메일 클라이언트에 표시 되는 것은 합니다. Microsoft는 높은 정확도 하는 경우는 From: 헤더를 위장, 스푸핑은으로 메시지를 식별 합니다.
  
스푸핑 메시지에 영향을 두 음수 실제 사용자에 대 한:
  
### <a name="1-spoofed-messages-deceive-users"></a>1. 위조 메시지 속이기 사용자
  
첫째, 위장 된 메시지 수 유인 사용자 링크를 클릭 하 고 자격 증명을 포기, 맬웨어, 다운로드 또는 (후자는 이라고 비즈니스 전자 메일 손상) 중요 한 콘텐츠가 포함 된 메시지에 회신 하기 합니다. 예, 다음은 msoutlook94@service.outlook.com의 위장 된 발신자가 포함 된 피싱 메시지:
  
![피싱 메시지 service.outlook.com 가장](media/1a441f21-8ef7-41c7-90c0-847272dc5350.jpg)
  
위의 service.outlook.com에서 실제로 제공 하지 않은 하지만 대신와 같게 보이도록 하기 위해 phisher에 의해 위장 되었습니다. 사용자가 메시지 내 링크를 클릭 하는 것을 유인를 시도 합니다.
  
다음 예제에서는 contoso.com을 스푸핑 됩니다.
  
![피싱 메시지-비즈니스 전자 메일 손상](media/da15adaa-708b-4e73-8165-482fc9182090.jpg)
  
메시지 합법적인, 실제로 있어 보이지만 스푸핑은 합니다. 이 피싱 메시지는 피싱의 하위 범주는 비즈니스 전자 메일 손상의 유형입니다.
    
### <a name="2-users-confuse-real-messages-for-fake-ones"></a>2. 사용자가 혼동 위조 오류에 대 한 실제 메시지
  
둘째, 위장 된 메시지 피싱 메시지에 대 한 알 수 있지만 실제 메시지와 위장 된 1 간의 차이 알 수 없으므로 사용자에 대 한 불확실성을 만듭니다. 예, 다음은 Microsoft 보안 계정 전자 메일 주소에서 다시 설정 하는 실제 암호의 예:
  
![Microsoft 합법적인 암호 다시 설정](media/58a3154f-e83d-4f86-bcfe-ae9e8c87bd37.jpg)
  
위의 메시지가 Microsoft에서 제공 않은 이지만 속성을 동시에 사용자를 사용 하는 피싱 메시지를 가져오는 수 유인 사용자 링크를 클릭 하 고 자격 증명을 포기, 맬웨어, 다운로드 또는 중요 한 콘텐츠가 포함 된 메시지에 회신 하기 합니다. 실제 암호 다시 설정 하 고 위조 하나 간의 차이 구분 하기 어려운 이기 때문에 많은 사용자는 이러한 메시지를 무시 하 스팸 보고 또는 불필요 하 게 하는 메시지를 다시 보고 Microsoft 부재중된 피싱 메일으로 합니다.
    
스푸핑를 중지 하려면 산업을 필터링 하는 전자 메일 [SPF](https://docs.microsoft.com/office365/SecurityCompliance/set-up-spf-in-office-365-to-help-prevent-spoofing), [DKIM](https://docs.microsoft.com/office365/SecurityCompliance/use-dkim-to-validate-outbound-email)및 [DMARC](https://docs.microsoft.com/office365/SecurityCompliance/use-dmarc-to-validate-email)와 같은 전자 메일 인증 프로토콜을 개발 했습니다. DMARC 메시지의 보낸 사람이-사용자에 게 자신의 전자 메일 클라이언트에 표시 한 검토 스푸핑 방지 (위의 예제에서 이것은 service.outlook.com, outlook.com, 및 accountprotection.microsoft.com)-SPF 또는 DKIM를 전달 하는 도메인과 합니다. 즉, 사용자에 게 표시 되는 도메인 인증 된 및 따라서 스푸핑 하지 않습니다. 보다 완전 한 토론 섹션을 참조 하십시오. "*전자 메일 인증 없는 이유 항상 스푸핑 중지 하기에 충분 해"* 이 문서에서 나중에 있습니다. 
  
그러나 문제 레코드는 필요 하지 않은 선택 사항, 전자 메일 인증을 사용 하는. 따라서 강력한 인증 정책 사용 하 여 도메인을 선택 하는 동안 microsoft.com 및 skype.com 스푸핑, 약한 인증 정책 또는 정책이 없으면 전혀 게시, 위장 된 대상 도메인에서 보호 됩니다. 3 월 2018 이후로 Fortune 500에서 회사의 도메인의 9%만 강력한 전자 메일 인증 정책을 게시합니다. 나머지 91%는 phisher에 의해 위장 될 수 있습니다 하 고 전자 메일 필터를 감지 하지 않으면 다른 정책을 사용 하 여 최종 사용자에 게 전달 될 수 있습니다 하 속이기:
  
![Fortune 500 계열사 DMARC 정책](media/84e77d34-2073-4a8e-9f39-f109b32d06df.jpg)
  
수 있는 작은-중간 규모의 회사의 비율로 not 강력한 전자 메일 인증 정책을 게시 하는 Fortune 500에서이 고, 북미 및 서유럽 외부에 있는 도메인에 대해 여전히 작은 합니다.
  
기업에서는 전자 메일 인증 작동 하는 방법에 대해 인식 하지 못할 수 있습니다, 하는 동안 피셔 수행을 이해 하 고는 부족을 활용 하기 때문에 중요 한 문제입니다.
  
SPF, DKIM, 및 DMARC 설정에 대 한 정보를 섹션을 참조 하십시오. "이이 문서에서 나중에*고객의 Office 365"* 합니다. 
  
## <a name="stopping-spoofing-with-implicit-email-authentication"></a>암시적 전자 메일 인증 스푸핑 중지

피싱 및 창 피싱 이러한 문제가 발생 하 고 때문에 강력한 전자 메일 인증 정책 제한 채택으로 인해, Microsoft 고객을 보호 하는 기능에 대 한 투자를 계속 합니다. 따라서 *암시적 전자 메일 인증* -를 사용 하 여 Microsoft는 앞에 이동 하는 경우 도메인 인증 하지 않습니다 Microsoft 전자 메일 인증 레코드를 게시 했습니다 하는 경우에 따라 처리를 전달 하지 않습니다을 적절 하 게 취급 합니다. 
  
이를 위해 Microsoft에서는 보낸사람 신뢰도, 보낸사람/받는 사람 기록, 동작 분석 및 기타 고급 기술을 포함 하는 일반 전자 메일 인증에 대 한 다양 한 확장을 작성 합니다. 전자 메일 인증을 게시 하지는 도메인에서 보낸 메시지를 합법적인 임을 나타내는 신호 다른을 포함 하지 않으면 스푸핑으로 표시 됩니다.
  
이렇게, 최종 사용자가 자신에 게 보내는 전자 메일 스푸핑 하지는 신뢰도 보낸 사람은 해당 도메인을 가장 하 고 아무도 값과 Office 365의 고객 가장 보호와 같은 더 나은 보호를 제공할 수 될 수 있습니다.
  
Microsoft의 일반 알림 [A 해의 Phish 제 2 부-Office 365의 향상 된 방지 스푸핑](https://techcommunity.microsoft.com/t5/Security-Privacy-and-Compliance/Schooling-A-Sea-of-Phish-Part-2-Enhanced-Anti-spoofing/ba-p/176209)을 참조 하십시오.
  
## <a name="identifying-that-a-message-is-classified-as-spoofed"></a>스푸핑으로 메시지 분류 된 식별

### <a name="composite-authentication"></a>복합 인증

SPF, DKIM, 및 DMARC는 자신 하 여 모든 유용한, 하는 동안 이벤트는 이벤트에 메시지가 표시 되는 명시적 인증 레코드가 없는 충분 한 인증 상태를 통신 하지 않습니다. 따라서, Microsoft 줄여서 복합 인증 또는 compauth를 호출 하는 단일 값으로 여러 신호를 결합 하는 알고리즘을 개발 했습니다. Office 365의 고객 메시지 헤더에 *인증 결과* 헤더에 스탬프 처리 하는 compauth 값을 갖습니다. 
  
```
Authentication-Results:
  compauth=<fail|pass|softpass|none> reason=<yyy>

```

|**CompAuth 결과**|**설명**|
|:-----|:-----|
|실패|메시지에 명시적 인증 하지 못했습니다 (보내는 도메인에에서 게시 된 레코드 명시적으로 DNS) 또는 암시적 인증 (도메인 게시 하지 않았습니다 레코드에서 DNS 레코드를 게시 했습니다 하는 경우 Office 365의 결과 삽입 하도록 보내기).|
|전달|메시지 전달 명시적 인증 (메시지 전달 DMARC, 또는 [최상의 추측 전달 DMARC](https://blogs.msdn.microsoft.com/tzink/2015/05/06/what-is-dmarc-bestguesspass-in-office-365)) 또는 도메인 전자 메일 인증 레코드를 게시 하지 않습니다 했으나 Office 365에 강력한 백엔드 신호 높은 정확도와 암시적 인증 (보내기 이 메시지는 가능성이 나타내기 합법적인).|
|softpass|메시지 낮은-중간 안심할 수 있는 암시적 인증 전달 (도메인에 전자 메일 인증을 게시 하지 않습니다 했으나 Office 365 메시지 합법적인 이지만 신호 강도 약한 나타내려면 백엔드 신호를 보내는).|
|없음|메시지를 인증 하지 않았습니다 (또는 인증 않았습니다 하지만 정렬 되지 않은 것) 하지만 복합 인증 보낸사람 신뢰도 또는 기타 요인으로 인해 적용 되지 않습니다.|
   
|||
|:-----|:-----|
|**이유**|**설명**|
|0xx|메시지에는 복합 인증 하지 못했습니다.<br/>**000** 메시지에는 다른 작업을 거부 또는 격리의 DMARC 실패 한 것을 의미 합니다.                    -001 이면 메시지 암시적 전자 메일 인증에 실패 합니다. 즉, 보내는 도메인에서 전자 메일 인증 레코드를 게시 하지 않았습니다 또는 약한 오류 정책 사용 했던 문제가 있었다면 (SPF 소프트 실패 또는 중립, DMARC 정책 p = 없음).<br/>조직에 위장 된 전자 메일을 발송에서 명시적으로 금지 된 보낸사람/도메인 쌍에 대 한 정책을 **002** 의미,이 설정은 관리자가 설정 수동으로 됩니다.  <br/>메시지는 다른 작업을 거부 또는 격리의 DMARC 실패 하 고 보내는 도메인을 사용 하면 조직의 허용 도메인 중 하나가 **010** 의미 (자체를 자체 또는 조직 내의 일부인이 스푸핑).  <br/>**011** 의미는 메시지가 암시적 전자 메일 인증 실패 하 고 보내는 도메인을 사용 하면 조직의 허용된 도메인 중 하나가 (자체를 자체 또는 조직 내의 일부인이 스푸핑).|
|다른 모든 코드 (1xx, 2xx, 3xx, 4xx, 5xx)|아무 작업도 적용 된 메시지를 전달 되는 암시적 인증 또는 없음 인증 명의 있는데 이유는 다양 한 내부 코드 (영문)에 해당 합니다.|
   
메시지 헤더 봐서는 관리자 또는 최종 사용자를 확인할 수 Office 365 보낸을 스푸핑 될 수 있습니다 결론에 도착 하는 방법.
  
### <a name="differentiating-between-different-types-of-spoofing"></a>다양 한 유형의 스푸핑 구별

Microsoft 두 다양 한 유형의 메시지를 스푸핑 구분해 서 사용 합니다.
  
 **조직 내 스푸핑**
  
로 알려져 자체를 자체 스푸핑, 발생이 때 from에서 도메인: 주소와 동일 또는 (도메인이 있는 경우 받는 사람 조직의 [허용 도메인](https://technet.microsoft.com/en-us/library/jj945194%28v=exchg.150%29.aspx)중 하나) 도메인의 받는 사람;에 맞춥니다 또는 때 from에서 도메인: 주소는 동일한 조직에 속해 있습니다.
  
예, 다음에 보낸사람 및 받는 사람 같은 도메인 (contoso.com)에서 있습니다. 공백은 삽입 될이 페이지에 spambot harvesting 방지 하기 위해 전자 메일 주소):
  
@ Contoso.com:에서 보낸사람
  
Contoso.com @ 받는 사람: 받는 사람
  
다음에 조직 도메인 (fabrikam.com)와 조율 보낸사람 및 받는 사람 도메인 있습니다.
  
Foo.fabrikam.com @:에서 보낸사람
  
받는 사람: 받는 사람 bar.fabrikam.com @
  
다음은 보낸사람 및 받는 사람 도메인은 서로 다른 (microsoft.com 및 반응을) 있지만 동일한 조직에 속한 (즉, 모두의 일부인 조직의 허용 도메인):
  
Microsoft.com @:에서 보낸사람
  
받는 사람: 받는 사람 반응 @
  
조직 내 스푸핑 실패 하는 메시지 헤더에 다음 값이 포함 합니다.
  
X-Forefront-스팸 방지-보고서:... CAT:SPM/HSPM/PHSH;... SFTY:9.11
  
고양이 메시지의 범주 및 SPM (스팸)으로 스탬프 처리 정상적으로 이지만 필요에 따라 발생할 수 있습니다 (높은 정확도 스팸) HSPM 수 또는 PHISH (피싱) 어떤 다른 따라 패턴 유형의 메시지에 있습니다.
  
SFTY은 메시지의 보안 수준, 첫번째 자리 숫자 (9) 의미는 메시지는 피싱, 및 자릿수 것을 의미 하는 점 (11) 한 후 두 번째 집합은 조직 내 스푸핑 합니다.
  
복합 인증에 대 한 조직 내 스푸핑, 2018 (아직 정의 되지 않은 시간 표시 막대)의 뒷부분에 나오는 스탬프가 지정 된 수에 대 한 특별 한 이유가 코드가 없는 합니다.
  
 **도메인간 스푸핑**
  
이 문제가 발생 때 from에서을 보내는 도메인: 주소를 받는 조직 외부 도메인은 합니다. 도메인간 스푸핑으로 인해 복합 인증에 실패 하는 메시지 헤더에 다음 값이 포함 합니다.
  
인증-결과:... compauth 실패 이유 = 000/001 =
  
X-Forefront-스팸 방지-보고서:... CAT:SPOOF;... SFTY:9.22
  
두 경우 모두 다음 빨간색 안전 팁은, 메시지 또는 받는 사람 사서함의 언어를 사용자 지정 된 동일한 스탬프 처리:
  
![빨간색 안전 팁-사기 감지](media/a366156a-14e8-4c14-bfe5-2031b21936f8.jpg)
  
만 봐서는 From은: 주소 및 받는 사람 전자 메일 이란, 파악 하거나 하 여 조직 내 및 도메인간 스푸핑 구분할 수 있는 전자 메일 머리글를 검사 합니다.
  
## <a name="how-customers-of-office-365-can-prepare-themselves-for-the-new-anti-spoofing-protection"></a>Office 365의 고객 수 준비 방법을 직접 새 스푸핑 방지 보호에 대 한

### <a name="information-for-administrators"></a>관리자를 위한 정보

Office 365에서 조직 관리자로 알고 있어야 하는 정보의 몇 가지 핵심 있습니다.
  
### <a name="understanding-why-email-authentication-is-not-always-enough-to-stop-spoofing"></a>전자 메일 인증 없는 이유 항상 스푸핑 중지 하기에 충분 이해

새 스푸핑 방지 보호 (SPF, DKIM, 및 DMARC) 하지 스푸핑으로 메시지를 표시 하려면 전자 메일 인증에 의존 합니다. 일반적인 예로 보내는 도메인 SPF 레코드를 게시 하지 않았으므로 때 수 있습니다. SPF 레코드가 없는 하거나는 올바르게 설정 하지 않으면 Microsoft에는 메시지는 합법적인 없다는 백엔드 인텔리전스 없으면 스푸핑으로 보낸된 메시지가 표시 됩니다.
  
등 스푸핑 방지 배포 되 고, 하기 전에 메시지 없는 SPF 레코드, DKIM 레코드가 없으면 및 DMARC 레코드가 없으면 다음과 같은 소개한 수 있습니다.: 
  
```
Authentication-Results: spf=none (sender IP is 1.2.3.4)
  smtp.mailfrom=example.com; contoso.com; dkim=none
  (message not signed) header.d=none; contoso.com; dmarc=none
  action=none header.from=example.com;
From: sender @ example.com
To: receiver @ contoso.com
```
스푸핑 방지 후 Office 365 엔터프라이즈 e 5, EOP, 또는 ATP, 있는 경우 compauth 값은 스탬프 처리 합니다.
  
```
Authentication-Results: spf=none (sender IP is 1.2.3.4)
  smtp.mailfrom=example.com; contoso.com; dkim=none
  (message not signed) header.d=none; contoso.com; dmarc=none
  action=none header.from=example.com; compauth=fail reason=001
From: sender @ example.com
To: receiver @ contoso.com

```

Example.com SPF 레코드를 삽입 했지만 DKIM 레코드가 아닙니다.을 설정 하 여이 고정을 하는 경우이 인증을 통과 복합 SPF를 전달 하는 도메인에서에서 도메인에 맞춰집니다 때문에: 주소: 
  
```
Authentication-Results: spf=pass (sender IP is 1.2.3.4)
  smtp.mailfrom=example.com; contoso.com; dkim=none
  (message not signed) header.d=none; contoso.com; dmarc=bestguesspass
  action=none header.from=example.com; compauth=pass reason=109
From: sender @ example.com
To: receiver @ contoso.com
```

속성이 DKIM 레코드가 삭제 되었지만 SPF 레코드를 설정 하는 경우이 인증을 통과 복합 전달 하는 DKIM 서명에서 도메인에서에서 도메인에 맞춰집니다 때문에 또는: 주소: 
  
```
Authentication-Results: spf=none (sender IP is 1.2.3.4)
  smtp.mailfrom=example.com; contoso.com; dkim=pass
  (signature was verified) header.d=outbound.example.com;
  contoso.com; dmarc=bestguesspass action=none
  header.from=example.com; compauth=pass reason=109
From: sender @ example.com
To: receiver @ contoso.com
```

phisher 될 수 있습니다도 SPF 및 DKIM를 설정 하 고 자신의 도메인을 사용 하 여 메시지에 서명 하지만 From에서 다른 도메인을 지정: 주소입니다. SPF 아니고 DKIM 필요는 도메인에서에서 도메인에 맞춰: example.com DMARC 레코드를 게시 하지 않으면이 것으로 표시할 수 DMARC를 사용 하 여 스푸핑 있으므로 주소: 
  
```
Authentication-Results: spf=pass (sender IP is 5.6.7.8)
  smtp.mailfrom=maliciousDomain.com; contoso.com; dkim=pass
  (signature was verified) header.d=maliciousDomain.com;
  contoso.com; dmarc=none action=none header.from=example.com;
From: sender @ example.com
To: receiver @ contoso.com
```

전자 메일 클라이언트 (Outlook, 웹, 또는 다른 전자 메일 클라이언트에서 Outlook), From만: 도메인 표시 되 면에는 SPF 또는 DKIM, 속하고 도메인이 아닌 메시지 example.com에서 제공 하지만 실제로 maliciousDomain.com에서 가져온에 답변에 사용자를 판단할 수 있습니다 .
  
![인증 된 메시지에서 하지만: 도메인 SPF 또는 DKIM 전달 하는 된와 일치 하지 않습니다](media/a9b5ab2a-dfd3-47c6-8ee8-e3dab2fae528.jpg)
  
Office 365 필요는 이런 이유로 from에서 도메인: 주소 SPF 또는 DKIM 서명에서 도메인으로 정렬 하 고 메시지는 합법적인 하 고 있음을 나타내는 일부 다른 내부 신호를 포함 하지, 하는 경우. 그렇지 않은 경우 메시지 compauth 실패 한 것입니다. 
  
```
Authentication-Results: spf=none (sender IP is 5.6.7.8)
  smtp.mailfrom=maliciousDomain.com; contoso.com; dkim=pass
  (signature was verified) header.d=maliciousDomain.com;
  contoso.com; dmarc=none action=none header.from=contoso.com;
  compauth=fail reason=001
From: sender@contoso.com
To: someone@example.com
```

따라서 Office 365 스푸핑 방지 보호 하는 없는 인증을 사용 하면 도메인에 대해 및 인증 하지만 from에서 도메인에 대해 불일치를 설정 하는 도메인에 대해: 주소 즉 같이 다른 사용자에 게 표시 하 고 생각 되는 메시지를 보낸 사람이 합니다. 모두 해당 조직의 외부에 도메인 조직 내에서 도메인의 마찬가지입니다.
  
따라서 것으로 표시 되며, 스푸핑 SPF 및 DKIM는 메시지를 전달 하는 경우에 및 복합 인증 실패 하 여 메시지를 받지 못하도록 하는 경우 있기 때문에 SPF 및 DKIM를 통과 하는 도메인에서에서 도메인으로 정렬 되지 않습니다: 주소입니다.
  
### <a name="understanding-changes-in-how-spoofed-emails-are-treated"></a>어떻게 위장 된 전자 메일에서 이해 변경 내용은 처리

현재 Office 365-모든 조직에 대 한 ATP 및 비-ATP-메시지를 거부 또는 격리의 정책 사용 하 여 DMARC에 스팸 및 일반적으로 지수가 높은 스팸 동작 또는 경우에 따라 일반 스팸 동작을 수행 하는 것으로 표시 되는 실패 하는 (여부에 따라 다른 스팸 규칙 먼저로 식별할 스팸). 조직 내 스푸핑 감지 된 일반 스팸 작업을 수행 합니다. 이 동작을 사용 하도록 설정 하지 않아도 것을 비활성화할 수 있습니다.
  
그러나 도메인간 스푸핑 메시지에 대 한이 변경 하기 전에 일반 스팸, phish, 및 맬웨어 검사를 통과 있으며 필터의 다른 부분, 의심 스러운으로 식별 하는 경우 것으로 표시할 스팸, phish, 또는 맬웨어 각각. 새 도메인간 스푸핑 보호와 인증할 수 없는 모든 메시지에서, 기본적으로 작업을 수행 피싱 방지에 정의 된 \> 백신 스푸핑 정책입니다. 정의 되지 않은 경우 사용자가 정크 메일 폴더로 이동 됩니다. 경우에 따라 더 의심 스러운 메시지는 메시지에 추가 된 빨간색 안전 팁도를 갖습니다.
  
여전히 시작로 표시 된 스팸 있지만 빨간색 안전 팁;도 이제는 스팸으로 이전에 표시 된 일부 메시지에 발생할 수 있습니다. 또 어떤 경우에는 스팸이 아닌가 시작 된 것으로 표시 빨간색 안전 팁이 있는 (CAT:SPOOF) 스팸으로으로 이전에 표시 된 메시지 추가 되었습니다. 다른 경우에 모든 스팸 및 phish 격리로 이동 된 고객은 이제 볼 정크 메일 폴더로 일어나 고 있어 (이 동작을 변경할 수 있습니다, [스푸핑 방지 설정 변경](#changing-your-anti-spoofing-settings)을 참조).
  
여러 다른 방식 (이 문서 앞부분의 [다양 한 유형의 스푸핑 간의 Differentiating](#differentiating-between-different-types-of-spoofing) 참조)는 메시지를 스푸핑 될 수 있지만 년 3 월 2018를 기준으로 Office 365에서 이러한 메시지를 처리 하는 방법은 되지 아직 통합 합니다. 다음 표에 새 동작 되 고 도메인간 스푸핑 보호와 요약 합니다. 
  
|**스푸핑의 유형**|**종류**|**안전 팁 추가 합니까?**|**적용 대상**|
|:-----|:-----|:-----|:-----|
|DMARC 실패 (격리 또는 거부)  <br/> |SPM 또는 PHSH에도 HSPM (기본값) 수 있습니다.  <br/> |아니요 (아직)  <br/> |모든 Office 365 고객, Outlook.com  <br/> |
|자체를 자체  <br/> |SPM  <br/> |예  <br/> |모든 Office 365 조직, Outlook.com  <br/> |
|도메인간  <br/> |스푸핑  <br/> |예  <br/> |Office 365 고급 위협 보호 및 e 5 고객  <br/> |
   
### <a name="changing-your-anti-spoofing-settings"></a>스푸핑 방지 설정 변경

피싱 방지로 이동를 만들거나 (도메인간) 스푸핑 방지 설정 업데이트 \> 위협 관리에서 설정 스푸핑 방지 \> 보안에서 정책 탭 &amp; 준수 센터입니다. 모든 피싱 방지 설정 하지 만들었으면 만들 해야 합니다.
  
![피싱 방지-새 정책 만들기](media/9337ec91-270e-4fa7-9dfa-a51a2d1eb95e.jpg)
  
이미 만든 경우 하나를 수정 하도록 선택할 수 있습니다.
  
![피싱 방지-기존 정책 수정](media/75457a7c-882e-4984-80d1-21a12b42c53a.jpg)
  
방금 만든 정책을 선택 하 고에서 설명한 대로 하는 단계를 진행 [스푸핑 인텔리전스에 대 한 자세히 알아보기.](https://support.office.com/article/Learn-more-about-spoof-intelligence-978c3173-3578-4286-aaf4-8a10951978bf)
  
![사용 하도록 설정 하거나 antispoofing를 사용 하지 않도록 설정](media/c49e2147-c954-443c-9144-1cbd139e1166.jpg)
  
![사용 하도록 설정 하거나 antispoofing 안전 팁을 사용 하지 않도록 설정](media/eec7c407-31fc-4f73-8325-307d82d1fb53.jpg)
  
PowerShell 통해 새 정책을 만들려면: 
  
```
$org = Get-OrganizationConfig
$name = "My first anti-phishing policy for " + $org.Name
# Note: The name should not exclude 64 characters, including spaces.
# If it does, you will need to pick a smaller name.
# Next, create a new anti-phishing policy with the default values
New-AntiphishPolicy -Name $Name
# Select the domains to scope it to
# Multiple domains are specified in a comma-separated list
$domains = "domain1.com, domain2.com, domain3.com"
# Next, create the anti-phishing rule, scope it to the anti-phishing rule
New-AntiphishRule -Name $name -AntiphishPolicy $name -RecipientDomainIs $domains
```

그런 다음 [집합 AntiphishPolicy](https://docs.microsoft.com/powershell/module/exchange/advanced-threat-protection/Set-AntiPhishPolicy?view=exchange-ps)에서 설명서에 따라 PowerShell을 사용 하 여 피싱 방지 정책 매개 변수를 수정할 수 있습니다. 매개 변수로 $name를 지정할 수 있습니다.
  
```
Set-AntiphishPolicy -Identity $name <fill in rest of parameters>
```

2018의 뒷부분에 나오는 하면 기본 정책을 만들 수 있는 것이 아닌 하나 만들어질 하므로 수동으로 지정할 필요가 없습니다 조직에서 모든 받는 사람에 게 범위가 지정 된 있습니다 (아래 스크린샷이 최종 구현 하기 전에 변경 될 수)입니다.
  
![피싱 방지에 대 한 기본 정책](media/1f27a0bf-e202-4e12-bbac-24baf013c8f9.jpg)
  
만든 정책와는 달리 기본 정책을 삭제할 해당 우선순위를 수정 하거나 선택 하는 사용자, 도메인 또는 그룹에 범위를 지정 하 수 없습니다.
  
![피싱 방지 기본 정책 세부 정보](media/30c21ceb-df52-4c93-aa65-f44a55dc1009.jpg)
  
PowerShell 통해 기본 보호를 설정 하려면:
  
```
$defaultAntiphishPolicy = Get-AntiphishPolicy | ? {$_.IsDefault -eq $true}
Set-AntiphishPolicy -Identity $defaultAntiphishPolicy.Name -EnableAntispoofEnforcement <$true|$false>
```

다른 메일 서버 또는 서버 Office 365 앞에 있는 경우에 스푸핑 방지 보호를 해제 해야 (자세한 내용은 스푸핑 방지를 사용 하지 않도록 설정 하는 합법적인 시나리오 참조). 
  
```
$defaultAntiphishPolicy = Get-AntiphishiPolicy | ? {$_.IsDefault $true}
Set-AntiphishPolicy -Identity $defaultAntiphishPolicy.Name -EnableAntispoofEnforcement $false 

```
> [!IMPORTANT]
> 전자 메일 경로에 있는 첫번째 홉은 Office 365 스푸핑으로 표시 되는 너무 많은 경우 합법적인 전자 메일을 액세스 하는 경우 먼저 설정 해야 위장 된 전자 메일을 보낼 사용자의 도메인에 허용 되는 대화 보낸사람 ( *"관리 합법적인 보낸사람 에게만 u 보내는 섹션을 참조 하십시오. nauthenticated 전자 메일"* ). 너무 많은 경우 가양성 액세스 하는 경우 (예: 스푸핑으로 표시 된 메시지 합법적) 스푸핑 방지 보호를 전혀 사용 하지 않도록 설정 하지 않는 것이 좋습니다. 대신, 높은 보호 하는 대신 기본을 선택 하는 것이 좋습니다.                    노출 장기간에 훨씬 더 높은 비용 부과 될 수 있는 위장 된 전자 메일을 조직에 보다 가양성을 통해 작동 하는 것이 좋습니다.

### <a name="managing-legitimate-senders-who-are-sending-unauthenticated-email"></a>인증 되지 않은 전자 메일을 발송 하 게 합법적으로 보낸사람 관리

Office 365는 추적 조직에 인증 되지 않은 전자 메일을 보내는 사람입니다. 서비스 보낸사람 합법적인 없는 것으로 생각을 하는 경우에 *compauth* 오류도 표시 됩니다 것입니다. 메시지에 적용 된 스푸핑 방지 정책에 따라 달라 집니다 있지만이 스푸핑으로 분류 됩니다. 
  
그러나를 관리자로 위장 된 전자 메일을 보낼 Office 365 의사 결정을 재정의 하는 어떤 보낸사람은 허용 지정할 수 있습니다.
  
**방법 1-조직에서 도메인을 소유 하는 경우 전자 메일 인증 설정**
  
조직 내 스푸핑 및 여러 테 넌 트와 소유 하거나 상호 작용 하는 경우에서 도메인 간 스푸핑 확인 하기 위해이 메서드를 사용할 수 있습니다. 또한도 Office 365 내에서 다른 고객에 게 보내면 도메인간 스푸핑 및 다른 공급자에서 호스팅되는 제 3 자 해결 하는데 도움이 됩니다.
  
자세한 내용은 [Office 365 고객을](#customers-of-office-365)참조 하십시오. 
 
**방법 2-사용 스푸핑 인텔리전스 인증 되지 않은 전자 메일의 허용 된 거부 목록을 구성 하려면**
  
조직에 인증 되지 않은 메시지를 전송 하는 보낸사람을 허용 하도록 [스푸핑 인텔리전스](https://support.office.com/article/Learn-more-about-spoof-intelligence-978c3173-3578-4286-aaf4-8a10951978bf) 를 사용할 수도 있습니다. 
  
외부 도메인에 대 한 위장 된 사용자가 도메인 보낸사람 주소에서 보내는 인프라는 보내는 IP 주소 (/24로 나눌 CIDR 범위), 또는 PTR 레코드의 조직 도메인 (아래 스크린샷에서 보내는 IP 수 해당 PTR 레코드는 outbound.mail.protection.outlook.com, 131.107.18.4 수 및 보내는 인프라에 대 한 outlook.com으로 표시 됩니다).
  
이 보낸 인증 되지 않은 전자 메일을 보낼 수 있도록 **아니요** 를 **Yes**로 변경 합니다.
  
![보낸사람 허용 antispoofing 설정](media/d4334921-d820-4334-8217-788279701e94.jpg)
  
PowerShell을 사용 하 여 특정 보낸 사람이 도메인 스푸핑할를 허용 하도록 수도 있습니다. 
  
```
$file = "C:\My Documents\Summary Spoofed Internal Domains and Senders.csv"
```

```
Get-PhishFilterPolicy -Detailed -SpoofAllowBlockList -SpoofType External | Export-CSV $file
```

![Powershell 통해 위장 된 보낸사람 시작](media/0e27ffcf-a5db-4c43-a19b-fa62326d5118.jpg)
  
이전 그림에서 추가 줄바꿈 추가 되었습니다이 스크린샷 하도록에 맞게, 하지만 단일 줄에 표시 되는 모든 값 실제로.
  
파일을 편집 하 고 outlook.com 및 반응을에 해당 하는 줄을 찾습니다를 아니요에서 AllowedToSpoof 항목을 변경 합니다.
  
![Powershell 통해 ' 예 '로 설정 스푸핑 허용](media/62340452-62d3-4958-9ce9-afe5275a870d.jpg)
  
파일을 저장 하 고을 실행 합니다. 
  
```
$UpdateSpoofedSenders = Get-Content -Raw "C:\My Documents\Spoofed Senders.csv"
Set-PhishFilterPolicy -Identity Default -SpoofAllowBlockList $UpdateSpoofedSenders
```

이렇게 하면에서 인증 되지 않은 전자 메일을 보낼 반응을 받을 이제 \*. outlook.com입니다.

**방법 3-보낸사람/받는 사람 쌍에 대 한 허용 항목 만들기**
  
모든 스팸 특정 보낸사람에 대 한 필터링을 무시 하도록 선택할 수 있습니다. 자세한 내용은 [안전 하 게 Office 365의 허용 목록에 보낸사람을 추가 하는 방법](https://blogs.msdn.microsoft.com/tzink/2017/11/29/how-to-securely-add-a-sender-to-an-allow-list-in-office-365/)을 참조 하십시오.
  
이 메서드를 사용 하는 경우 것을 건너뜁니다 스팸 및 phish 필터링의 일부가 아니라 맬웨어 필터링 합니다.
  
**보낸사람에 게 문의 하 고 전자 메일 인증을 설정 하도록 요청 하는 방법 4-**
  
스팸 및 피싱의 문제 때문에 전자 메일 인증을 설정 하는 모든 보낸사람을 좋습니다. 보내는 도메인의 관리자를 알고 있는 경우 해당 하 고 모든 재정의 추가 하지 않아도 되므로 전자 메일 인증 레코드를 설정 하는 요청에 게 문의 합니다. 자세한 내용은 [Office 365 고객 되지 않은 도메인의 관리자](#administrators-of-domains-that-are-not-office-365-customers)를 참조 "이이 문서의 뒷부분에 있습니다. 
  
가져올 보내는 도메인 인증 하기 위해 먼저에 하기가 어려울 수 있지만, 시간이 지남에 따라으로 더 많은 전자 메일 필터 시작 junking 또는 전자 메일을 거부 하는,를 일으킬 수 있는 적절 한 레코드를 더 나은 배달 되도록 설정할 수 있습니다.
  
### <a name="viewing-reports-of-how-many-messages-were-marked-as-spoofed"></a>얼마나 많은 메시지에 스푸핑 하는 것으로 표시 된 보고서를 확인

스푸핑 방지 정책에 설정 되 면 번호 문제를 해결 하려면 얼마나 많은 메시지 phish 것으로 표시 되며 위협 인텔리전스를 사용할 수 있습니다. 이 작업을 수행 하려면 보안으로 이동 &amp; 준수 센터 (SCC) 위협 관리에서 \> 탐색기, Phish, 및 그룹에 보낸 도메인 또는 보호 상태 보기를 설정 합니다.
  
![얼마나 많은 메시지 phish로 표시 된 보기](media/de25009a-44d4-4c5f-94ba-9c75cd9c64b3.jpg)
  
얼마나 많은 스푸핑으로 표시 된 메시지를 포함 하 여 피싱으로 표시 된 참조를 다양 한 보고서와 상호작용할 수 있습니다. 자세한 내용은 [Office 365 위협 인텔리전스 시작 하기](https://support.office.com/article/get-started-with-office-365-threat-intelligence-38e9b67f-d188-490f-bc91-a1ae4b270441)를 참조 합니다.
  
아직 수행 하는 메시지 다른 유형의 (일반 피싱, 도메인 또는 사용자 가장 등에) 피싱 및 스푸핑으로 인해 표시 된 것을 분리할 수 없습니다. 그러나 2018, 뒷부분에 나오는 됩니다 보안을 통해이 작업을 수행할 수 &amp; 준수 센터입니다. 그렇게 할 경우에 인증에 실패으로 인해 스푸핑으로 표시 되는 합법적인 될 수 있는 보내는 도메인을 식별 하기 시작 지점으로이 보고서를 사용할 수 있습니다.
  
다음 스크린샷에 제안 어떻게이 데이터를 확인 되지 않은 놓을 때 변경 될 수 있습니다.
  
![검색 유형별 피싱 보고서 보기](media/dd25d63f-152c-4c55-a07b-184ecda2de81.jpg)
  
비 ATP 및 e 5 고객에 대 한 이러한 보고서 위협 보호 상태 (TPS) 보고서에서 2018 뒷부분에 나오는 사용할 수 있지만 24 시간 이상으로 지연 됩니다. 이 페이지의 보안에 통합으로 업데이트 됩니다 &amp; 준수 센터입니다.
  
### <a name="predicting-how-many-messages-will-be-marked-as-spoof"></a>예측 스푸핑 얼마나 많은 메시지가 표시 됩니다.

2018, 뒷부분에 나오는 Office 365 스푸핑 방지 적용을 해제할 수 있도록 해당 설정을 업데이트 하는 한번 또는에서 기본 또는 높은 적용을 사용 하면 하 게 할 메시지 처리는 다양 한 설정에서 어떻게 변경 되는지 확인 하는 기능입니다. 즉, 스푸핑 방지을 해제 하는 경우 됩니다; 인증 방법이 기본 설정 하는 경우 스푸핑으로 얼마나 많은 메시지를 검색할 수 됩니다를 볼 수 또는 Basic 인 경우에 얼마나 많은 자세한 메시지 높음으로 설정 하는 경우 스푸핑으로 검색 됩니다 참조 수 있습니다.
  
이 기능은 현재 개발입니다. 자세한 내용은 정의된대로이 페이지는 보안 및 규정 준수 센터의 스크린샷이 텔 레 프레 및 PowerShell 예제와 함께 업데이트 됩니다.
  
![Antispoofing를 사용 하도록 설정 하는 것에 대 한 보고서 "경우"](media/fdd085ae-02c1-4327-a063-bfe9a32ff1eb.jpg)
  
![위장 된 보낸사람 허용 하는 것에 대 한 가능한 UX](media/53f9f73e-fb01-47f3-9a6d-850c1aef5efe.jpg)
  
### <a name="understanding-how-spam-phishing-and-advanced-phishing-detections-are-combined"></a>이해 어떻게 스팸, 피싱, 및 고급 피싱 감지 결합 되어

함께 또는 따로 ATP, Exchange Online을 사용 하는 조직은 서비스 맬웨어, 스팸, 높은 정확도 스팸, 피싱, 및 대량으로 메시지를 식별 하는 경우에 실행할 동작을 지정할 수 있습니다. ATP 고객에 대 한 ATP 피싱 방지 정책 및 EOP 고객에 대 한 피싱 방지 정책 및 메시지를 여러 검색 형식 (예: 맬웨어, 피싱, 및 사용자 가장)을 적중 수 팩트를 있을 수 있는 계정으로 일부 혼란 정책이 적용 됩니다. 
  
일반적으로 X Forefront-스팸 방지 보고서 머리글 고양이 (범주) 속성에는 메시지에 적용 되는 정책을 식별 됩니다. 
  
|**우선 순위**|**정책**|**종류**|**여기서 관리?**|**적용 대상**|
|:-----|:-----|:-----|:-----|:-----|
|1  <br/> |Malware  <br/> |MALW  <br/> |[맬웨어 정책](https://technet.microsoft.com/en-us/library/jj200745%28v=exchg.150%29.aspx) <br/> |모든 조직  <br/> |
|2  <br/> |피싱  <br/> |PHSH  <br/> |[호스팅된 콘텐츠 필터 정책](https://technet.microsoft.com/library/jj200684%28v=exchg.150%29.aspx) <br/> |모든 조직  <br/> |
|3  <br/> |높은 정확도 스팸  <br/> |HSPM  <br/> |[호스팅된 콘텐츠 필터 정책](https://technet.microsoft.com/library/jj200684%28v=exchg.150%29.aspx) <br/> |모든 조직  <br/> |
|4  <br/> |스푸핑  <br/> |스푸핑  <br/> |[피싱 방지 정책](https://go.microsoft.com/fwlink/?linkid=864553), [스푸핑 인텔리전스](https://support.office.com/article/Learn-more-about-spoof-intelligence-978c3173-3578-4286-aaf4-8a10951978bf) <br/> |모든 조직  <br/> |
|5  <br/> |스팸  <br/> |SPM  <br/> |[호스팅된 콘텐츠 필터 정책](https://technet.microsoft.com/library/jj200684%28v=exchg.150%29.aspx) <br/> |모든 조직  <br/> |
|6  <br/> |대량  <br/> |대량  <br/> |[호스팅된 콘텐츠 필터 정책](https://technet.microsoft.com/library/jj200684%28v=exchg.150%29.aspx) <br/> |모든 조직  <br/> |
|7  <br/> |도메인 가장  <br/> |DIMP  <br/> |[피싱 방지 정책](https://go.microsoft.com/fwlink/?linkid=864553) <br/> |ATP와 조직에만 해당  <br/> |
|8  <br/> |사용자 가장  <br/> |UIMP  <br/> |[피싱 방지 정책](https://go.microsoft.com/fwlink/?linkid=864553) <br/> |ATP와 조직에만 해당 <br/> |
   
여러 다른 피싱 방지 정책을 가장 높은 우선순위에 하나씩 적용 됩니다. 예, 두 정책이 있다고 가정 합니다.
  
|**정책**|**우선 순위**|**사용자/도메인 가장**|**스푸핑 방지**|
|:-----|:-----|:-----|:-----|
|A  <br/> |1  <br/> |On  <br/> |Off  <br/> |
|B  <br/> |2  <br/> |Off  <br/> |On  <br/> |
   
메시지에는 및 스푸핑 및 사용자 가장으로 식별 된 및 사용자의 동일한 집합 정책 A와 B 정책으로 범위가 지정 된 후 메시지 스푸핑은으로 처리 됩니다 하 고 아무 작업도 이후 적용 되 백신 스푸핑 꺼져 스푸핑 사용자 가장 (8) 보다 더 높은 우선순위 (4)에서 실행 되 고 있습니다.
  
피싱의 다른 형식을 사용 하려면 정책 적용, 다양 한 정책에 적용 되는의 설정을 조정 해야 합니다.
  
### <a name="legitimate-scenarios-to-disable-anti-spoofing"></a>스푸핑 방지를 사용 하지 않도록 설정 하는 합법적인 시나리오

피싱 공격 으로부터 고객을 보호 더 잘 스푸핑 방지 하 고 사용 하지 않도록 설정 스푸핑 방지 보호 권장 되지 않으므로 합니다. 을 해제 하 여 일부 단기 가양성을 더 위험에 노출 되는 장기 하지만 해결할 수 있습니다. 발신자 측에서 인증을 설정 하거나 피싱 정책에서 조정에 대 한 비용에는 일반적으로 일회성 이벤트 또는 최소한의 고 정기적인 유지 관리가 필요 합니다. 그러나 여기서 데이터 노출 된, 피싱 공격에서 복구 하기 위한 비용은 또는 자산 된 손상 매우 높습니다.
  
이러한 이유로 스푸핑 방지 가양성 스푸핑 방지 보호를 사용 하지 않도록 설정 하려면 보다을 통해 작동 하는 것이 좋습니다.
  
그러나은 합법적인 시나리오를 스푸핑 방지 해제 해야 하 고은 추가 메일 필터링 있을 때 사용할 수 없는 전자 메일 경로에 있는 첫번째 홉 메시지 라우팅 및 Office 365의 제품:
  
![Office 365를 고객 MX 레코드를 가리키지 않습니다.](media/62127c16-cfb8-4880-9cad-3c12d827c67e.jpg)
  
Exchange 온-프레미스 메일 서버, Ironport, 예: 장치를 필터링 하는 메일 또는 다른 클라우드 서비스를 호스팅하는 다른 서버 수 있습니다.
  
받는 사람 도메인의 MX 레코드를 가리키지 않을 Office 365를 하는 경우 사용 하지 않으려면 스푸핑 방지 Office 365 받는 도메인의 MX 레코드를 조회 하 고 다른 서비스를 가리키는 경우 스푸핑 방지를 생략 하기 때문에 필요 하지 않은 됩니다. 도메인의 다른 서버를 앞에는 경우를 모르는 경우에 MX 레코드를 조회 MX 도구 상자와 같은 웹사이트를 사용할 수 있습니다. 다음과 같은 라고 표시 될 수 있습니다.
  
![Office 365에 도메인 가리키지 않을 MX 레코드를 나타냅니다.](media/d868bb9f-3462-49aa-baea-9447a3ce4877.jpg)
  
이 도메인은 Office 365 스푸핑 방지 적용 적용 되지 않도록 Office 365를 가리키지 않는 MX 레코드를 가집니다.
  
그러나 *않는* 받는 사람 도메인의 MX 레코드는 Office 365 앞에 다른 서비스는 경우에 Office 365를 가리키도록, 하는 경우 다음 사용 하지 않도록 스푸핑 방지 합니다. 받는 사람 다시 쓰기를 사용 하 여 가장 일반적인 예제는입니다. 
  
![받는 사람 다시 쓰기에 대 한 라우팅 다이어그램](media/070d90d1-50a0-42e4-9fd3-920bc99a7cad.jpg)
  
Contoso.com 도메인의 MX 레코드를 포함 하기 때문에 Office 365에 도메인 @office365.contoso.net MX 레코드를 가리키는 하는 동안 온-프레미스 서버를 가리키는 \*. protection.outlook.com, 또는 \*. eo.outlook.com MX 레코드에서:
  
![MX 레코드를 가리키는 Office 365, 따라서 아마도 받는 사람을 다시 작성](media/4101ad51-ef92-4907-b466-b41d14d344ca.jpg)
  
Office 365에 받는 사람 도메인의 MX 레코드를 가리키지 않 및 받는 사람 다시 쓰기의 경우 되었기 때문에 해당 하는 경우를 구분 해야 합니다. 이러한 두 경우 간의 차이 구분을 고려해 야 합니다.
  
수신 도메인 받는 사람-재작성 경우 되었기 때문에 여부 확실 하지 않은 경우 메시지 헤더를 검토 하 여 알 수 경우가 종종 있습니다.
  
먼저 a) 인증 결과 헤더에서 받는 사람 도메인에 대 한 메시지에서 머리글을 살펴봅니다. 
  
```
Authentication-Results: spf=fail (sender IP is 1.2.3.4)
  smtp.mailfrom=example.com; office365.contoso.net; dkim=fail
  (body hash did not verify) header.d=simple.example.com;
  office365.contoso.net; dmarc=none action=none
  header.from=example.com; compauth=fail reason=001
```

이 경우 office365.contoso.net에서 위의 굵은 빨간색 텍스트로에서 받는 사람 도메인 발견 합니다. 다를 수 있습니다이 하에서 받는 사람: 헤더:
  
받는 사람: 예에서는 받는 사람 \<contoso.com @ 받는 사람\>
  
실제 받는 사람 도메인의 MX 레코드 조회를 수행 합니다. 포함 하는 경우 \*. protection.outlook.com, mail.messaging.microsoft.com, \*. eo.outlook.com, 또는 mail.global.frontbridge.com는 MX Office 365를 가리키고 있는지를 의미 합니다.
  
이러한 값을 포함 하지는 않는 하는 경우의 MX Office 365를 가리키지 않을 의미 합니다. 이 확인 하기 위해 사용할 수 있는 도구를 둘은 MX 도구 상자를 클릭 합니다.
  
이 예의 경우에 대 한 다음 이라는 해당 contoso.com To 되었기 때문에 받는 사람 처럼 보이는 도메인: 헤더에 MX 레코드가 가리키는 prem에서 서버:
  
![Prem에서 서버를 가리키는 MX 레코드](media/2444144a-9a90-4319-96b2-d115041f669f.jpg)
  
그러나 실제 받는 사람이 office365.contoso.net 해당 MX 레코드는 Office 365를 가리킵니다.
  
![Office 365를 가리키는 MX 받는 사람 재작성 이어야 합니다.](media/10cf3245-9b50-475a-b655-d8a51f99d812.jpg)
  
따라서이 메시지에 받는 사람-다시 쓰기 되었습니다 가능성이 있습니다.
  
b) 둘째, 받는 사람 다시 작성의 일반적인 사용 사례를 구분 해야 합니다. 받는 사람 도메인을 다시 작성 하려는 경우 \*. onmicrosoft.com를 대신 하도록 다시 작성 \*. mail.onmicrosoft.com 합니다.
  
다른 서버 뒤에 라우팅되는 최종 받는 사람 도메인을 식별 한 되 고 실제로 Office 365 (해당 DNS 레코드에 게시)으로 받는 사람 도메인의 MX 레코드를 가리키는 스푸핑 방지 사용 하지 않으려면 작업을 진행할 수 있습니다.
  
기억 스푸핑 방지 라우팅 경로에 도메인의 첫번째 홉은 Office 365 하나 이상의 서비스가 뒤에 하는 경우에 하는 경우 사용 하지 않도록 설정할 표시 하지 않습니다.
  
### <a name="how-to-disable-anti-spoofing"></a>스푸핑 방지를 사용 하지 않도록 설정 하는 방법

이미 만든는 피싱 방지 정책 경우 $false EnableAntispoofEnforcement 매개 변수를 설정 합니다. 
  
```
$name = "<name of policy>"
Set-AntiphishPolicy -Identity $name -EnableAntiSpoofEnforcement $false 

```

사용 하지 않으려면 정책 (또는 정책)의 이름을 모르는 경우에 표시할 수 있습니다. 
  
```
Get-AntiphishPolicy | fl Name
```

모든 기존 피싱 방지 정책을 설치 하지 않은 경우 하나 만들고 수 (경우에 정책이 없는 경우, 여전히 적용 된; 2018에서 나중에 스푸핑 방지, 수에 대 한 기본 정책을 만들 하나를 만드는 대신 하는 다음 비활성화할 수) 사용 안함 . 여러 단계에서이 작업을 수행 해야 합니다. 
  
```
$org = Get-OrganizationConfig
$name = "My first anti-phishing policy for " + $org.Name
# Note: If the name is more than 64 characters, you will need to choose a smaller one
```

```
# Next, create a new anti-phishing policy with the default values
New-AntiphishPolicy -Name $Name
# Select the domains to scope it to
# Multiple domains are specified in a comma-separated list
$domains = "domain1.com, domain2.com, domain3.com"
# Next, create the anti-phishing rule, scope it to the anti-phishing rule
New-AntiphishRule -Name $name -AntiphishPolicy -RecipientDomainIs $domains
# Finally, scope the antiphishing policy to the domains
Set-AntiphishPolicy -Identity $name -EnableAntispoofEnforcement $false 

```

Cmdlet을 통해 사용할 수만 스푸핑 방지를 사용 하지 않도록 설정 (Q2 2018 뒷부분에 나오는 보안에서 사용할 수 있습니다 &amp; 준수 센터). PowerShell에 액세스할 수 없는 경우 지원 티켓을 만듭니다.
  
Office 365로 전송 하는 경우에 간접 라우팅을 수행할 수 있는 도메인에만 적용할 수 해야이 기억 합니다. 일부 가양성으로 인해 스푸핑 방지를 사용 하지 않도록 하는 유혹, 통해 작동 하는 장기적으로 개선 됩니다.
  
### <a name="information-for-individual-users"></a>개별 사용자에 대 한 정보

개별 사용자에 게 안전 스푸핑 방지 팁과 작용 하는 방법 제한 됩니다. 그러나 몇 가지 일반적인 시나리오를 해결 하려면 수행할 수 있습니다.
  
### <a name="common-scenario-1---mailbox-forwarding"></a>일반적인 시나리오 #1-사서함 착신 전환

다른 전자 메일 서비스를 사용 하 고 Office 365 또는 Outlook.com에 전자 메일을 전달 하는 경우 전자 메일 스푸핑으로 표시 될 수 있습니다 및 빨간색 안전 팁을 수신 합니다. Office 365 및 Outlook.com Outlook.com, Office 365, Gmail, 또는 [호 프로토콜](https://arc-spec.org)을 사용 하는 다른 서비스 중 하나는 전달 자가 때 자동으로이 주소를 계획 합니다. 그러나 해당 수정 프로그램을 배포할 때까지 사용자는 착신 전환 옵션을 사용 하는 대신 해당 메시지를 직접 가져올 계정 연결 기능을 사용 해야 합니다.
  
Office 365에 연결 된 계정을 설정 하는 Office 365 웹 인터페이스의 오른쪽 위 모서리에서 기어 아이콘을 선택 \> 메일 \> 메일 \> 계정 \> 계정에 연결 합니다.
  
![Office 365-연결 된 계정 옵션](media/e8e841ca-8861-4d83-8506-2a0858c51010.jpg)
  
Outlook.com을 하는 프로세스는 기어 아이콘 \> 옵션 \> 메일 \> 계정 \> 계정에 연결 합니다.
  
### <a name="common-scenario-2---discussion-lists"></a>일반적인 시나리오 #2-토론 목록

토론 목록 메시지 스푸핑 방지 하는 방식 때문은 앞에 문제가 있는 수정 내용을 알려주지에서 원래 유지 것으로 알려져 있습니다: 주소입니다.
  
예, 전자 메일 주소는 @ contoso.com, 사용자 및 감 감시에 관심이 있는 및 example.com @ 토론 목록 birdwatchers 참가 경우를 가정해 보겠습니다. 토론 목록에 메시지를 보낼 때 이러한 방식으로 보낼 수 있습니다.
  
**에서:** John Doe \<contoso.com @ 사용자\> 
  
**를:** Birdwatcher의 토론 목록 \<birdwatchers @ example.com\> 
  
**제목:** 이번 주의 산 Rainier 상단의 파랑 제비의 뛰어난 보기 
  
보기를 체크아웃 하려면 누구나 산 Rainier에서 이번주?
  
전자 메일 목록 메시지를 받으면 메시지의 서식, 해당 내용을 수정 있으며 많은 다른 전자 메일 수신기에서 참가자의 구성 된 있는 토론 목록에서 구성원의 나머지 부분을 재생 합니다.
  
**에서:** John Doe \<contoso.com @ 사용자\> 
  
**를:** Birdwatcher의 토론 목록 \<birdwatchers @ example.com\> 
  
**제목:** [BIRDWATCHERS] 이번 주의 산 Rainier 상단의 파랑 제비의 뛰어난 보기 
  
보기를 체크아웃 하려면 누구나 산 Rainier에서 이번주?
  
---
  
Birdwatchers 토론 목록에이 메시지를 보냈습니다. 언제 든 지 구독을 취소할 수 있습니다.
  
위의에서 재생 된 메시지에서 동일한에: 주소 (사용자 @ contoso.com) 하지만 원본 메시지의 제목줄 및 메시지의 아래쪽에 바닥글에 태그를 추가 하 여 수정 되었습니다. 이 유형의 메시지 수정 메일 그룹에서 일반적으로 이며 가양성에서 발생할 수 있습니다.
  
사용자 또는 조직에서 다른 사용자가 메일 그룹의 관리자 인 경우 스푸핑 방지 검사를 통과 하도록 구성할 수 있습니다.
  
- DMARC.org에서 FAQ 확인: [메일 그룹을 작동 하 고 DMARC와 상호 운용 될 하려고 하는 경우, 어떻게 해야 합니까?](https://dmarc.org/wiki/FAQ#I_operate_a_mailing_list_and_I_want_to_interoperate_with_DMARC.2C_what_should_I_do.3F)
    
- 이 블로그 게시물에 대 한 지침을 읽어: [오류를 방지 하기 위해 DMARC와 상호 운용 하는 메일 그룹 연산자에 대 한 팁](https://blogs.msdn.microsoft.com/tzink/2017/03/22/a-tip-for-mailing-list-operators-to-interoperate-with-dmarc-to-avoid-failures/)
    
- 호를 지원 하기 위한 참조 하 여 메일 그룹 서버에 업데이트를 설치 하는 것이 좋습니다.[https://arc-spec.org](https://arc-spec.org/)
    
메일 그룹의 소유권 없는 경우
  
- (도 해야하는 메일 그룹에서 릴레이 도메인에 대 한 설정 하는 전자 메일 인증) 위의 옵션 중 하나를 구현 하는 메일 그룹의 유지 관리자를 요청할 수 있습니다.
    
- 받은 편지함에 메시지를 이동 하 여 전자 메일 클라이언트에서 사서함 규칙을 만들 수 있습니다. 또한 조직의 관리자를 설정 하는 규칙, 허용 또는 관리 적법 한 보낸 사람이 인증 되지 않은 전자 메일을 발송 하 게 섹션에서 설명으로 재정의 요청할 수 있습니다.
    
- Office 365를 합법적으로 처리 하는 메일 그룹에 대 한 재정의 만드는 지원 티켓을 만들 수 있습니다.
    
### <a name="other-scenarios"></a>다른 시나리오

1. 상황에 맞는 위의 일반적인 시나리오의 두가지가 모두 적용 하는 경우 메시지 false 양의 백업용으로 Microsoft에 보고 합니다. 자세한 내용은 섹션을 참조 하십시오. [Microsoft에 스팸 또는 스팸이 아닌 메시지를 다시 보고 합니까?](#how-can-i-report-spam-or-non-spam-messages-back-to-microsoft) 이 문서의 뒷부분에 나오는 합니다. 
    
2. 또한 것으로 microsoft 지원 티켓을 발생 시킬 수 있는 전자 메일 관리자에 게 문의 수 있습니다. Microsoft 엔지니어링 팀 스푸핑은으로 메시지를 표시 하는 이유를 조사 합니다.
    
3. 또한 보낸 이며 이러한 하지 침입 되 고 악의적으로 확신 사용자를 알고 있는 경우 인증 하지 않는 메일 서버에서 메시지를 보내고 있기를 나타내는 보낸 사람에 게 회신할 수 있습니다. 이 경우에 따라 필요한 전자 메일 인증 레코드를 설정 하는 자신의 IT 관리자에 게 문의 하는 원래 보낸사람에 만들어집니다.
  
충분 한 보낸사람 전자 메일 인증 레코드를 설정 해야 이러한 도메인 소유자에 게 회신을 하는 경우 해당 spurs 하에 작업을 수행 합니다. Microsoft의도 필요한 레코드를 게시 하려면 도메인 소유자와 함께 작동 하는 동안 훨씬 더 때 개별 사용자가 요청 도움이 됩니다.
    
4. 필요에 따라 수신 허용-보낸사람 목록에 보낸사람을 추가 합니다. 그러나 하는 phisher 해당 계정을 스푸핑, 하는 경우 해당 배달 됩니다 사서함에 유의 합니다. 따라서이 옵션은 자주 사용 되어야 합니다.
    
## <a name="how-senders-to-microsoft-should-prepare-for-anti-spoofing-protection"></a>스푸핑 방지 보호에 대 한 Microsoft에 보낸사람 해야 준비 하는 방법

관리자에 게 현재 Microsoft로 메시지를 보내는 경우 전자 메일 적절히 인증 되었는지 확인 해야 Office 365 또는 Outlook.com, 그렇지 않은 경우 스팸 또는 phish로 표시 될 수 있습니다. 
  
### <a name="customers-of-office-365"></a>Office 365의 고객

Office 365 고객 인 경우 Office 365를 사용 하 여 아웃 바운드 전자 메일을 보낼:
  
- 도메인, [SPF 스푸핑을 방지 하기 위해 Office 365의 설정](https://docs.microsoft.com/office365/SecurityCompliance/set-up-spf-in-office-365-to-help-prevent-spoofing) 에 대 한
    
- 기본 도메인을 [Office 365에서 사용자 지정 도메인에서 보낸 아웃 바운드 전자 메일의 유효성을 검사를 사용 하 여 DKIM](https://docs.microsoft.com/office365/SecurityCompliance/use-dkim-to-validate-outbound-email) 에 대 한
    
- 적법 한 보낸 사람이 확인 하려면 도메인에 대 한 [DMARC 레코드 설정](https://docs.microsoft.com/office365/SecurityCompliance/use-dmarc-to-validate-email) 을 
    
Microsoft는 SPF, DKIM, 그리고 DMARC 각각에 대 한 자세한 구현 지침을 제공 하지 않습니다. 그러나 많은 온라인 게시 하는 정보는. 제 3 자 회사 전자 메일 인증 레코드를 설정 하 여 조직의 도움말을 전용 밖에도 합니다.
  
### <a name="administrators-of-domains-that-are-not-office-365-customers"></a>Office 365 고객 되지 않은 도메인 관리자

도메인 관리자에 게는 하 고 Office 365 고객 되지 않습니다.
  
- 도메인의 보내는 IP 주소를 게시 하도록 SPF를 설정 하 고도 DKIM (가능한 경우)를 설정 메시지에 디지털 서명 해야 합니다. 또한 설정 DMARC 레코드를 고려할 수 있습니다.
    
- 방식으로 전자 메일을 보낼 수 있도록 함께 작업 해야하는 사용자를 대신 하 여 전자 메일을 전송 하는 동안 대량 발신자가 되도록 from에서을 보내는 도메인: 주소 (에 속해) 하는 경우 SPF 또는 DMARC를 전달 하는 도메인에 맞춥니다.
    
- 온-프레미스 메일 서버, 또는 소프트웨어로-서비스 공급자 로부터 보내거나 Microsoft Azure, GoDaddy, Rackspace, Amazon 웹 서비스와 같은 클라우드 호스팅 서비스에서와 마찬가지로 확인 해야 하는 경우 SPF 레코드에 추가 됩니다.
    
- ISP에서 호스트 하는 작은 도메인 인 경우 ISP에 문의 하 여 제공 하는 지침에 따라 SPF 레코드를 설정 해야 합니다. 대부분의 Isp 이러한 유형의 지침을 제공 하 고 회사의 지원 페이지에서 찾을 수 있습니다.
    
- 이전에 전자 메일 인증 레코드를 게시 하지 했습니다 하 고 제대로 작동 하는지, 하는 경우에 Microsoft로 보낼 전자 메일 인증 레코드 여전히 게시 해야 합니다. 이렇게 하 여 피싱, 퇴치에서 내리도록 하, 또는 조직에 보낼 phished 얻을 수 가능성 감소 합니다.
    
### <a name="what-if-you-dont-know-who-sends-email-as-your-domain"></a>경우에 어떻게 도메인으로 전자 메일을 보내는 사용자에 대해 모르는?

여러 도메인의 모든 보낸사람에 있는 모르는 때문에 SPF 레코드를 게시 하지 않습니다. 하는 방법을 배우게, 사용자를 알 필요가 없습니다 모두 됩니다. 대신,의 특히 회사 트래픽 있는 위치를 알고 있는 않으며 중립 SPF 정책을 게시 위치에 대 한 SPF 레코드를 게시 하 여 시작 해야 합니까? 모든:
  
IN TXT example.com "v = spf1 include:spf.example.com? 모든"
  
중립 SPF 정책은 조직의 인프라에서 해제 되는 모든 전자 메일은 전달 전자 메일 인증 전혀 다른 전자 메일 수신자를 의미 합니다. 전자 메일에 대 한 모르는 사람이 보낸 채워지도록으로 거의 동일 전혀 없는 SPF 레코드를 게시 하는 중립으로 다시 실패 합니다.
  
회사 트래픽에서 제공 되는 전자 메일, 인증 된 것으로 표시 됩니다 Office 365 메시지를 보내면 하지만 원본에 대 한 모르는에서 제공 되는 전자 메일 (여부 Office 365 암시적으로 인증할 수 그에 따라) 스푸핑으로 계속 표시 될 수 있습니다. 그러나이 Office 365 스푸핑으로 표시 되는 모든 전자 메일에서 향상 된 여전히입니다.
  
SPF 레코드의 대체 정책과 함께 시작 참조 했으면? 모든 점진적으로 더 많은 보내는 인프라를 포함 하 고 다음 보다 엄격 하 게 정책을 게시할 수 있습니다. 
  
### <a name="what-if-you-are-the-owner-of-a-mailing-list"></a>메일 그룹의 소유자 하는 경우에 어떻게 합니까?

[일반적인 시나리오 #2-토론 목록](#common-scenario-2---discussion-lists)섹션을 참조 하십시오. 
  
### <a name="what-if-you-are-an-infrastructure-provider-such-as-an-internet-service-provider-isp-email-service-provider-esp-or-cloud-hosting-service"></a>예: 인터넷 서비스 공급자 (ISP), 전자 메일 서비스 공급자 (ESP) 또는 서비스를 호스트 하는 클라우드 인프라 공급자를 하는 경우에 어떻게 합니까?

도메인의 전자 메일을 호스트 하 고 전자 메일을 보내거나 전자 메일을 보낼 수 있는 호스팅 인프라를 제공 하는 경우 다음을 수행 해야 합니다.
  
- 확보할 수 있도록 고객이 자신의 SPF 레코드에서 게시 기능을 설명 하는 설명서
    
- 고객 하지 명시적으로 설정 (기본 도메인으로 기호) 하는 경우에 DKIM 서명 아웃 바운드 전자 메일에 서명 하는 것이 좋습니다. 짝수 이중 기호 (+) (한번와 상대가 설정한 것을 하는 경우에 고객의 도메인 및 회사의 DKIM 서명 사용 하 여 두번째 시간) DKIM 서명 사용 하 여 전자 메일을 수행할 수 있습니다.
    
사용 중인 플랫폼에서 발생 하는 전자 메일을 인증 하지만 Microsoft 인증 되지 않은 때문에 전자 메일 정크 하지 않는 보장 적어도 하는 경우에 Microsoft에 스팸과 보장 되지 않습니다. Outlook.com에서 전자 메일을 필터링 하는 방법에 대 한 자세한 내용은 [Outlook.com 전자 메일 관리자 페이지](https://postmaster.live.com/pm/postmaster.aspx)를 참조 하십시오.
  
서비스 공급자에 대 한 유용한 정보에 대 한 자세한 내용은 [M3AAWG 모바일 메시징에 대 한 유용한 서비스 공급자를](https://www.m3aawg.org/sites/default/files/M3AAWG-Mobile-Messaging-Best-Practices-Service-Providers-2015-08.pdf)참조 하십시오.
  
## <a name="frequently-asked-questions"></a>질문과 대답

### <a name="why-is-microsoft-making-this-change"></a>Microsoft는 이러한 변경을 수행 하는 이유

하기 때문에 피싱 영향 공격 및 Microsoft 생각 하는 전자 메일 인증 15 년에 대 한 되었으며, 때문에 합법적인 전자 메일을 빼앗길 위험이 보다는 위험을 계속 인증 되지 않은 전자 메일을 허용 합니다.
  
### <a name="will-this-change-cause-legitimate-email-to-be-marked-as-spam"></a>이 변경 스팸으로 표시 하는 합법적인 전자 메일 포함 될?

처음에 스팸으로 표시 되는 일부 메시지 없을 것입니다. 그러나 시간이 지남에 따라 보낸사람을 조정 하 고 위장 된으로 레이블이 메시지의 양 대부분 전자 메일 경로 대 한 무시할 수 됩니다.
  
Microsoft 자체는 먼저이 기능 고객의 나머지 부분에 배포 하기 전에 몇 주가 채택 합니다. 처음에는 중단 동안 점진적으로 거부 됩니다.
  
### <a name="will-microsoft-bring-this-feature-to-outlookcom-and-non-advanced-threat-protection-customers-of-office-365"></a>Microsoft은 Office 365의 Outlook.com 및 비-고급 위협 보호 고객에 게이 기능을 가져오려면가?

Microsoft의 스푸핑 방지 기술 Office 365 Enterprise e 5 구독 명의 또는 구독에 대 한 Office 365 고급 위협 보호 (ATP) 추가 기능을 구입 명의 하는 해당 조직에 처음 배포 되었습니다. 년 10 월 2018를 기준으로 보호 하는 조직에서는 Exchange Online Protection (EOP)도를 확장 했을 때 했습니다. 나중에 Outlook.com에 대 한 릴리스 수는 있습니다. 그러나이 경우 보고와 같은 적용 되지 않은 일부 기능이 있을 수 및 사용자 정의 재정의 합니다.
  
### <a name="how-can-i-report-spam-or-non-spam-messages-back-to-microsoft"></a>어떻게 수 있습니까 스팸 또는 스팸이 아닌 메시지를 다시 보고 Microsoft?

[보고서 메시지 용 추가 기능에서 Outlook를](https://support.office.com/article/use-the-report-message-add-in-b5caa9f1-cdf3-4443-af8c-ff724ea719d2)사용 하거나 [전송 스팸, 스팸이 아닌 및 분석을 위해 Microsoft에 피싱 사기 메시지](https://technet.microsoft.com/en-us/library/jj200769%28v=exchg.150%29.aspx)아닌 경우 설치 합니다.
  
### <a name="im-a-domain-administrator-who-doesnt-know-who-all-my-senders-are"></a>내 모든 보낸사람은 누구 인지 모릅니다 있는 도메인 관리자 결정!

[Office 365 고객 되지 않은 도메인의 관리자](#administrators-of-domains-that-are-not-office-365-customers)를 참조 하십시오.
  
### <a name="what-happens-if-i-disable-anti-spoofing-protection-for-my-organization-even-though-office-365-is-my-primary-filter"></a>수행 되는 스푸핑 방지 보호 내 조직에 대 한 사용 하지 않도록 하는 경우 Office 365는 내 기본 필터 하는 경우에 작업

좋지 않습니다이 되므로 보다 부재중된 피싱 및 스팸 메시지를 노출할 수 있습니다. 일부 피싱 스푸핑은 하 고 일부 스푸핑을 누락 됩니다. 그러나 위험성이 고객에 게 스푸핑 방지를 사용 하면 보다 높은 됩니다.
  
### <a name="does-enabling-anti-spoofing-protection-mean-i-will-be-protected-from-all-phishing"></a>스푸핑 방지 보호 기능을 사용을 의미 합니까 모든 피싱으로부터 보호 합니까?

그러나 아니요, 피셔는 같은 기술을 사용 하 여 적용할 때문에 손상 된 계정 또는 무료 서비스 계정 설정 합니다. 그러나 피싱 방지 보호 기능 레이어는 Office 365의 보호 작업을 함께 설계 되었기 때문에 감지 다른 유형의 피싱 방법 이러한 하 여 서로 기반으로 구축 훨씬 더 잘 작동 합니다.
  
### <a name="do-other-large-email-receivers-block-unauthenticated-email"></a>다른 큰 전자 메일 수신자 인증 되지 않은 전자 메일을 차단 마십시오?

거의 모든 큰 전자 메일 수신자 전통적인 SPF, DKIM, 및 DMARC를 구현합니다. 일부 수신기가 다른 확인 하 고 해당 표준 하지만 적은 이동 관련해 서 Office 365를 차단 하려면 인증 되지 않은 것 보다 더 엄격한 수 있는 전자 메일을 스푸핑은 동일 하 게 취급 합니다. 그러나 대부분 업계의 피싱의 문제 때문에 특히 점차이 특정 유형의 전자 메일에 대 한 더 많은 엄격 하 게 합니다.
  
### <a name="do-i-still-need-the-advanced-spam-filtering-option-enabled-for-spf-hard-fail-if-i-enable-anti-spoofing"></a>고급 스팸 필터링 옵션을 설정 하는 스푸핑 방지 하는 경우 "SPF 하드 실패"에 대해 활성화 여전히 필요 합니까?

아니요, SPF 하드 실패 하지만 조건의 훨씬 더 넓은 집합에만 아니라 스푸핑 방지 기능 고려 하기 때문에이 옵션은 필요한 나타나지 않습니다. 스푸핑 방지 사용 하도록 설정 해야 하 고 사용 하도록 설정 하는 SPF 하드 실패 옵션을 아마도 받게 됩니다 더 가양성 합니다. 이 기능을 해제 하는 거의 없는 별도 catch 스팸 또는 phish을 제공 하 고 대신 대개 가양성을 생성 하는 것이 좋습니다.
  
### <a name="does-sender-rewriting-scheme-srs-help-fix-forwarded-email"></a>보낸 사람이 다시 쓰기 체계 (SRS) 어떤 도움이 됩니까 전달 된 전자 메일을 수정?

SRS는 부분적 으로만 전달 된 전자 메일의 문제를 해결합니다. SMTP 메일을 다시를 작성 하 여 SRS 되도록 할 수 있는 다음 대상에 전달 된 메시지 전달 SPF. 그러나 From에 따라이 스푸핑 방지 하기 때문에: 주소 MAIL FROM 또는 DKIM 서명 도메인 (또는 다른 신호)와 함께, 않은 스푸핑 하는 것으로 표시 되 고에서 전달 된 전자 메일을 방지 하기 위해 충분 합니다.
  

