---
title: Office 365의 스푸핑 방지 보호 기능
ms.author: tracyp
author: MSFTtracyp
manager: laurawi
ms.date: 3/6/2019
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Priority
search.appverid:
- MET150
ms.assetid: d24bb387-c65d-486e-93e7-06a4f1a436c0
ms.collection:
- M365-security-compliance
- Strat_O365_IP
description: 이 문서에서는 Office 365에서 위조 된 보낸 사람 도메인, 즉 스푸핑된 도메인을 사용 하는 피싱 공격을 완화 하는 방법을 설명 합니다. 이를 위해 표준 전자 메일 인증 방법 및 기타 보낸 사람 신뢰도 기법을 사용 하 여 메시지를 분석 하 고, 인증 되지 않은 항목을 차단 합니다. 이 변경 사항은 Office 365의 조직이 제공 하는 피싱 공격의 수를 줄이기 위해 구현 되었습니다.
ms.openlocfilehash: 422bac2ad5fd0c58928d79467721204b20583fd7
ms.sourcegitcommit: 5d6be2b208dbe28d5d5da057c60cf97729799c1b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/07/2019
ms.locfileid: "30465485"
---
# <a name="anti-spoofing-protection-in-office-365"></a>Office 365의 스푸핑 방지 보호 기능

이 문서에서는 Office 365에서 위조 된 보낸 사람 도메인, 즉 스푸핑된 도메인을 사용 하는 피싱 공격을 완화 하는 방법을 설명 합니다. 이를 위해 메시지를 분석 하 고 표준 전자 메일 인증 방법 및 기타 보낸 사람 신뢰도 기법을 사용 하 여 인증할 수 없는 항목을 차단 합니다. 이 변경 사항은 Office 365의 조직이 제공 하는 피싱 공격의 수를 줄이기 위해 구현 되었습니다.
  
이 문서에서는 이러한 변경 작업을 수행 하는 이유, 고객이이 변경 내용을 준비 하는 방법, 영향을 받는 메시지를 확인 하는 방법, 메시지를 보고 하는 방법, 가양성을 완화 하는 방법 및 Microsoft에서이를 위해 준비 해야 하는 방법에 대해서도 설명 합니다. 내용이.
  
Microsoft의 스푸핑 방지 기술은 처음에 office 365 Enterprise E5 구독을 사용 하거나 구독을 위한 office 365 Advanced Threat Protection (ATP) 추가 기능을 구매한 조직에 배포 되었습니다. 10 월, 2018 Exchange Online protection (EOP)이 있는 조직에 대 한 보호도 확장 되었습니다. 또한 모든 필터가 서로의 정보를 파악 하는 방식으로 인해 Outlook.com 사용자에 게 영향을 줄 수 있습니다.
  
## <a name="how-spoofing-is-used-in-phishing-attacks"></a>피싱 공격에서 스푸핑이 사용 되는 방식

Microsoft는 사용자를 보호 하는 데 있어 피싱 위협을 심각 하 게 받아들입니다. 스팸 발송자와 phishers가 일반적으로 사용 하는 방법 중 하나는 보낸 사람이 위조 되는 경우, 메시지가 실제 원본이 아닌 다른 사람 또는 다른 곳에서 시작 된 것으로 표시 되는 스푸핑입니다. 이 기술은 사용자 자격 증명을 얻기 위해 설계 된 피싱 캠페인에서 주로 사용 됩니다. Microsoft의 스푸핑 방지 기술은 특히 Outlook과 같은 전자 메일 클라이언트에 표시 되는 ' From: 헤더 '의 위조를 검사 합니다. Microsoft에서 From: 헤더를 스푸핑 하는 것이 높은 확신을 갖는 경우 메시지를 스푸핑으로 식별 합니다.
  
스푸핑 메시지는 실제 사용자에 대해 다음과 같은 두 가지 부정적인 의미를 갖습니다.
  
### <a name="1-spoofed-messages-deceive-users"></a>1. 스푸핑된 메시지 속이기 users
  
먼저 스푸핑된 메시지는 사용자가 링크를 클릭 하 여 자격 증명을 제공 하 고, 맬웨어를 다운로드 하거나, 중요 한 콘텐츠 (예: 비즈니스 전자 메일 손상)로 메시지에 회신할 수 있습니다. 예를 들어 msoutlook94@service.outlook.com의 스푸핑된 보낸 사람을 포함 하는 피싱 메시지는 다음과 같습니다.
  
![service.outlook.com 가장 피싱 메시지](media/1a441f21-8ef7-41c7-90c0-847272dc5350.jpg)
  
위의 내용은 실제로 service.outlook.com에서 제공 되지 않았지만 phisher에서 위장 되었기 때문에 원래는 것 처럼 보입니다. 사용자가 메시지 내에서 링크를 클릭 하도록 속이는 시도를 하 고 있습니다.
  
다음 예에서는 스푸핑 contoso.com 합니다.
  
![피싱 메시지-비즈니스 전자 메일 손상](media/da15adaa-708b-4e73-8165-482fc9182090.jpg)
  
메시지는 합법적인 것으로 보이지만 실제로는 스푸핑입니다. 이 피싱 메시지는 피싱의 하위 범주에 해당 하는 비즈니스 전자 메일 손상의 한 유형입니다.

### <a name="2-users-confuse-real-messages-for-fake-ones"></a>2. 사용자가 가짜 1로 실제 메시지를 혼동 합니다.
  
둘째, 스푸핑된 메시지는 피싱 메시지를 알고 있지만 실제 메시지와 스푸핑된 간의 차이를 알 수 없는 사용자에 대해 불확실성을 만듭니다. 예를 들어 다음은 Microsoft 보안 계정 전자 메일 주소에서 실제로 암호를 다시 설정한 예입니다.
  
![Microsoft 적법 한 암호 재설정](media/58a3154f-e83d-4f86-bcfe-ae9e8c87bd37.jpg)
  
위의 메시지는 Microsoft에서 제공 되었지만 동시에 사용자가 링크를 클릭 하 여 자격 증명을 제공 하 고, 맬웨어를 다운로드 하거나, 중요 한 콘텐츠를 사용 하 여 메시지에 회신할 수 있는 피싱 메시지를 가져오는 데 사용 됩니다. 실제 암호 재설정 및 가짜 일대일를 구별 하기 어렵기 때문에 많은 사용자가 이러한 메시지를 무시 하 고 스팸으로 보고 하거나 불필요 한 피싱 사기로 메시지를 Microsoft에 다시 보고 하지 않습니다.

스푸핑을 중지 하려면 전자 메일 필터링 업계에서 [SPF](https://docs.microsoft.com/office365/SecurityCompliance/set-up-spf-in-office-365-to-help-prevent-spoofing), [dkim](https://docs.microsoft.com/office365/SecurityCompliance/use-dkim-to-validate-outbound-email)및 [DMARC](https://docs.microsoft.com/office365/SecurityCompliance/use-dmarc-to-validate-email)와 같은 전자 메일 인증 프로토콜을 개발 해야 합니다. DMARC은 SPF 또는 dkim을 통과 한 도메인과 함께 사용자가 전자 메일 클라이언트 (위의 예에서는 service.outlook.com, outlook.com 및 accountprotection.microsoft.com)에 게 표시 되는 메시지의 보낸 사람을 검사 하는 스푸핑을 방지 합니다. 즉, 사용자에 게 표시 되는 도메인은 인증 된 것 이므로 스푸핑 되지 않습니다. 자세한 내용은이 문서 뒷부분에 나오는 "*전자 메일 인증이 항상 적절 하지는 않는 이유 이해"* 섹션을 참조 하십시오.
  
그러나이 문제는 전자 메일 인증 레코드가 필요 하지 않은 선택 사항 이기 때문에 발생 합니다. 따라서 microsoft.com 및 skype.com와 같은 강력한 인증 정책을 사용 하는 도메인은 스푸핑 으로부터 보호 되지만 더 약한 인증 정책을 게시 하는 도메인 이나 정책 없이는 스푸핑 대상이 됩니다. 3 월 2018 일, Fortune 500에 있는 회사 도메인의 9%만 강력한 전자 메일 인증 정책을 게시 합니다. 나머지 91%는 phisher에 의해 위장 될 수 있으며, 전자 메일 필터에서 다른 정책을 사용 하 여이를 검색 하지 않으면 최종 사용자에 게 배달 되어이를 속일 수 있습니다.
  
![Fortune 500 회사의 DMARC 정책](media/84e77d34-2073-4a8e-9f39-f109b32d06df.jpg)
  
강력 하지 않은 전자 메일 인증 정책을 게시 하는 Fortune 500에 속하지 않는 중소 규모의 회사에 대 한 비율이 작고 북미 및 서유럽 외부의 도메인에 비해 여전히 작습니다.
  
엔터프라이즈에서는 전자 메일 인증의 작동 방식을 알 수 없는 경우에는이 문제가 발생 하기 때문에 phishers을 이해 하 고이에 대 한 부족 한 이점을 활용할 수 있습니다.
  
SPF, dkim 및 DMARC을 설정 하는 방법에 대 한 자세한 내용은이 문서 뒷부분의 "*Office 365 고객 소개"* 섹션을 참조 하십시오. 
  
## <a name="stopping-spoofing-with-implicit-email-authentication"></a>암시적 전자 메일 인증을 사용 하 여 스푸핑 중지

피싱 및 스피어 피싱은 이와 같은 문제 이며, 강력한 전자 메일 인증 정책이 제한적으로 채택 되었기 때문에 Microsoft는 고객을 보호 하기 위한 기능을 계속 해 서 투자 합니다. 따라서 microsoft는 *암시적 전자 메일 인증* 을 계속 진행 하 고, 도메인이 인증 되지 않으면 microsoft는 전자 메일 인증 레코드를 게시 한 것으로 간주 하 고이를 통과 하지 못한 경우에는 적절 하 게 취급 합니다. 
  
이를 위해 Microsoft는 보낸 사람 신뢰도, 보낸 사람/받는 사람의 기록, 행태 분석 및 기타 고급 기법을 포함 하 여 정기적인 전자 메일 인증에 대 한 다양 한 확장을 구축 했습니다. 전자 메일 인증을 게시 하지 않는 도메인에서 보낸 메시지는 합법적인 상태임을 나타내는 다른 신호가 포함 되어 있지 않으면 스푸핑으로 표시 됩니다.
  
이렇게 하면 최종 사용자가 보낸 전자 메일이 위장 되지 않은 것으로 확신 하 고, 보낸 사람이 도메인을 가장 하는 것을 확신할 수 있으며, Office 365의 고객은 가장을 보호 하는 것과 같은 더 나은 보호 기능을 제공할 수 있습니다.
  
Microsoft의 일반 알림을 보려면 [Office 365의 피싱 부분 2-향상 된 스푸핑 방지](https://techcommunity.microsoft.com/t5/Security-Privacy-and-Compliance/Schooling-A-Sea-of-Phish-Part-2-Enhanced-Anti-spoofing/ba-p/176209)를 참조 하세요.
  
## <a name="identifying-that-a-message-is-classified-as-spoofed"></a>메시지가 스푸핑된로 분류 됨 확인

### <a name="composite-authentication"></a>복합 인증

SPF, dkim 및 DMARC는 자체적으로 모두 유용 하지만, 메시지에 명시적 인증 레코드가 없는 경우에는 충분 한 인증 상태를 통신 하지 않습니다. 따라서 Microsoft는 여러 신호를 복합 인증 이라고 하는 단일 값으로 결합 하는 알고리즘을 개발 했거나, 인증 방식을 짧게 했습니다. Office 365의 고객은 메시지 헤더의 *인증 결과* 헤더에 압축기 인증 값이 기록 되어 있습니다. 
  
```
Authentication-Results:
  compauth=<fail|pass|softpass|none> reason=<yyy>

```

|**compauth 결과**|**설명**|
|:-----|:-----|
|작동|메시지에 명시적 인증 (dns에서 도메인 게시 된 레코드를 명시적으로 보냄) 또는 암시적 인증 (보내는 도메인에서 dns에 레코드를 게시 하지 않음), 즉 Office 365에서 결과를 게시 된 레코드 처럼 보간합니다.|
|pass|메시지가 통과 된 명시적 인증 (메시지 전달 DMARC 또는 [Best Guess DMARC](https://blogs.msdn.microsoft.com/tzink/2015/05/06/what-is-dmarc-bestguesspass-in-office-365)) 또는 신뢰도가 높은 암시적 인증 (보내는 도메인은 전자 메일 인증 레코드를 게시 하지 않음) 이지만 Office 365에는 강력한 백 엔드 신호가 있습니다. 메시지가 합법적 일 것을 나타냅니다.|
|소프트 통과|메시지가 낮은 간 신뢰도의 암시적 인증을 통과 했지만 (보내는 도메인은 전자 메일 인증을 게시 하지 않음) Office 365에는 메시지가 합법적 임을 나타내는 백엔드 신호가 있지만 신호의 강도가 더 취약 합니다.|
|없음|메시지가 인증 되지 않았거나 (인증을 했지만 정렬 하지 못했습니다.) 보낸 사람 신뢰도 또는 기타 요인으로 인해 복합 인증이 적용 되지 않습니다.|
   
|||
|:-----|:-----|
|**이유**|**설명**|
|0xx|메시지가 복합 인증을 수행 하지 못했습니다.<br/>**000** 은 거부 또는 격리 작업을 사용 하 여 메시지를 DMARC 실패 함을 의미 합니다.  <br/>**001** 은 메시지가 암시적 전자 메일 인증을 수행 하지 못했음을 의미 합니다. 즉, 보내는 도메인에 게시 된 전자 메일 인증 레코드가 없거나, 완료 된 경우 오류 정책 (SPF 소프트 fail 또는 중립, DMARC policy p = 없음)이 발생 한 것입니다.  <br/>**002** 은 조직이 스푸핑된 전자 메일을 명시적으로 허용 하지 않는 보낸 사람/도메인 쌍에 대 한 정책을 소유 하 고 있으며, 관리자가이 설정을 수동으로 설정 함을 의미 합니다.  <br/>**010** 은 거부 또는 격리 작업을 사용 하 여 메시지를 DMARC 것이 고, 보내는 도메인은 조직의 허용 도메인 중 하나입니다 (자체 간 또는 조직 내 스푸핑에 포함 됨).  <br/>**011** 은 메시지가 암시적 전자 메일 인증을 실패 했다는 것을 의미 하며, 보내는 도메인은 조직의 허용 도메인 중 하나입니다 (자체 간 또는 조직 내 스푸핑에 포함 됨).|
|기타 모든 코드 (1xx, 2xx, 3xx, 4xx, 5xx)|메시지가 암시적 인증을 통과 하거나 인증을 받지 않았지만 아무 작업도 적용 되지 않은 다양 한 내부 코드에 해당 합니다.|
   
관리자 또는 최종 사용자는 메시지의 헤더를 확인 하 여 보낸 사람이 스푸핑 되었을 수 있는 결론에 따라 Office 365이 도착 하는 방식을 결정할 수 있습니다.
  
### <a name="differentiating-between-different-types-of-spoofing"></a>서로 다른 스푸핑 유형 간 구별

Microsoft는 서로 다른 두 가지 유형의 스푸핑 메시지를 구별 합니다.
  
 **조직 내 스푸핑**
  
자체 스푸핑 위장이 라고도 하는이는 보낸 사람: 주소에 있는 도메인을 받는 사람 도메인과 동일 하 게 또는이 도메인의 [허용](https://technet.microsoft.com/en-us/library/jj945194%28v=exchg.150%29.aspx)도메인 중 하나에 맞출 때 발생 합니다. 또는 보낸 사람: 주소에 있는 도메인이 같은 조직의 일부인 경우
  
예를 들어 다음은 같은 도메인 (contoso.com)에서 보낸 사람과 받는 사람을 포함 하는 경우입니다. 이 페이지에서 스팸 봇 수집을 방지 하기 위해 전자 메일 주소에 공백이 삽입 됩니다.
  
보낸 사람: sender @ contoso.com
  
받는 사람: recipient @ contoso.com
  
다음은 fabrikam.com (조직 도메인)와 함께 보낸 사람 및 받는 사람 도메인을 정렬 하는 예제입니다.
  
보낸 사람: sender @ foo.fabrikam.com
  
받는 사람: recipient @ bar.fabrikam.com
  
다음 보낸 사람 및 받는 사람 도메인이 서로 다릅니다 (microsoft.com 및 bing.com). 하지만 이러한 도메인은 조직의 허용 도메인의 일부인 같은 조직에 속합니다.
  
보낸 사람: sender @ microsoft.com
  
받는 사람: recipient @ bing.com
  
조직 내 스푸핑에 실패 하는 메시지에는 헤더에 다음 값이 포함 됩니다.
  
스팸 방지-Report: ... CAT: SPM/HSPM/PHSH; ... SFTY: 9.11
  
CAT은 메시지 범주이 고 일반적으로 SPM (스팸)으로 스탬프 처리 되지만, 메시지에서 발생 하는 다른 유형의 패턴에 따라 hspm (신뢰도가 높은 스팸) 또는 피싱 (피싱) 일 수도 있습니다.
  
SFTY는 메시지의 보안 수준 이며, 첫 번째 숫자 (9)는 메시지가 피싱 임을 의미 하며, 점 (11) 다음에 오는 두 번째 숫자 집합은 조직 내 스푸핑 임을 의미 합니다.
  
이전에는 2018 (아직 정의 되지 않은 시간 표시줄)에서 스탬프 처리 되는 조직 내 스푸핑에 대 한 복합 인증을 위한 특정 이유 코드가 없습니다.
  
 **도메인 간 스푸핑**
  
보낸 사람: 주소에 있는 보내는 도메인이 받는 조직에 대 한 외부 도메인인 경우 이러한 상황이 발생 합니다. 도메인 간 스푸핑로 인 한 복합 인증에 실패 한 메시지에는 헤더에 다음 값이 포함 됩니다.
  
인증-결과: ... compauth = 실패 이유 = 000/001
  
스팸 방지-Report: ... CAT: 스푸핑 SFTY: 9.22
  
두 경우 모두에서 다음의 빨간색 안전 팁이 메시지에 스탬프 처리 되거나 받는 사람 사서함의 언어로 사용자 지정 된 것과 같습니다.
  
![위험 보안 팁-사기 감지](media/a366156a-14e8-4c14-bfe5-2031b21936f8.jpg)
  
이는 보낸 사람 및 도메인 간 스푸핑 간의 구별이 가능 하 고 받는 사람의 전자 메일을 확인 하거나 전자 메일 헤더를 검사 하는 방법 뿐입니다.
  
## <a name="how-customers-of-office-365-can-prepare-themselves-for-the-new-anti-spoofing-protection"></a>Office 365의 고객이 새로운 스푸핑 방지 보호를 위해 스스로를 준비할 수 있는 방법

### <a name="information-for-administrators"></a>관리자를 위한 정보

Office 365의 조직 관리자는 몇 가지 주요 정보를 알고 있어야 합니다.
  
### <a name="understanding-why-email-authentication-is-not-always-enough-to-stop-spoofing"></a>전자 메일 인증이 항상 스푸핑을 중지 하는 데 충분 하지 않은 이유 이해

새 스푸핑 방지 보호 기능은 전자 메일 인증 (SPF, dkim 및 DMARC)을 사용 하 여 메시지를 스푸핑으로 표시 하지 않습니다. 일반적인 예로는 보내는 도메인에서 SPF 레코드를 게시 하지 않은 경우를 들 수 있습니다. SPF 레코드가 없거나 제대로 설정 되지 않은 경우 Microsoft에 메시지가 합법적인 것을 알리는 백 엔드 인텔리전스가 없으면 보낸 메시지는 스푸핑된로 표시 됩니다.
  
예를 들어 앤티 스푸핑이 배포 되기 전에 메시지는 SPF 레코드 없이 다음과 같이 나타날 수 있으며, dkim 레코드와 DMARC 레코드가 없습니다. 
  
```
Authentication-Results: spf=none (sender IP is 1.2.3.4)
  smtp.mailfrom=example.com; contoso.com; dkim=none
  (message not signed) header.d=none; contoso.com; dmarc=none
  action=none header.from=example.com;
From: sender @ example.com
To: receiver @ contoso.com
```
스푸핑 방지 후에 Office 365 Enterprise E5, EOP 또는 ATP가 있는 경우 compauth 값은 다음과 같습니다.
  
```
Authentication-Results: spf=none (sender IP is 1.2.3.4)
  smtp.mailfrom=example.com; contoso.com; dkim=none
  (message not signed) header.d=none; contoso.com; dmarc=none
  action=none header.from=example.com; compauth=fail reason=001
From: sender @ example.com
To: receiver @ contoso.com

```

example.com에서 spf 레코드를 설정 하 여이를 해결 했지만 dkim 레코드를 사용 하지 않는 경우에는 spf가 통과 한 도메인이 보낸 사람: 주소에 있는 도메인과 맞춰져 있기 때문에 복합 인증을 통과 하 게 됩니다. 
  
```
Authentication-Results: spf=pass (sender IP is 1.2.3.4)
  smtp.mailfrom=example.com; contoso.com; dkim=none
  (message not signed) header.d=none; contoso.com; dmarc=bestguesspass
  action=none header.from=example.com; compauth=pass reason=109
From: sender @ example.com
To: receiver @ contoso.com
```

또한 SPF 레코드가 아닌 dkim 레코드를 설정 하는 경우에는 From: 주소에서 도메인과의 맞춤이 통과 한 dkim 시그니처의 도메인 때문에 복합 인증도 통과 합니다. 
  
```
Authentication-Results: spf=none (sender IP is 1.2.3.4)
  smtp.mailfrom=example.com; contoso.com; dkim=pass
  (signature was verified) header.d=outbound.example.com;
  contoso.com; dmarc=bestguesspass action=none
  header.from=example.com; compauth=pass reason=109
From: sender @ example.com
To: receiver @ contoso.com
```

그러나 phisher에서 SPF 및 dkim을 설정 하 고 메시지에 자체 도메인을 서명할 수도 있지만 보낸 사람: 주소에 다른 도메인을 지정 해야 합니다. SPF 또는 dkim은 도메인을 From: 주소에서 도메인에 맞춰야 하지만 example.com이 DMARC 레코드가 없는 경우에는 DMARC을 사용 하 여 스푸핑으로 표시 되지 않습니다. 
  
```
Authentication-Results: spf=pass (sender IP is 5.6.7.8)
  smtp.mailfrom=maliciousDomain.com; contoso.com; dkim=pass
  (signature was verified) header.d=maliciousDomain.com;
  contoso.com; dmarc=none action=none header.from=example.com;
From: sender @ example.com
To: receiver @ contoso.com
```

전자 메일 클라이언트 (Outlook, 웹의 outlook 또는 다른 전자 메일 클라이언트)에서 SPF 또는 dkim의 도메인이 아닌 보낸 사람: 도메인만 표시 되며, 사용자가 메시지를 example.com에서 보낸 것으로 생각 하지 못하게 할 수 있으며, 실제로는 maliciousDomain.com에서 제공 됩니다. .
  
![인증 된 메시지는 도메인에서 통과 한 SPF 또는 dkim과 일치 하지 않습니다.](media/a9b5ab2a-dfd3-47c6-8ee8-e3dab2fae528.jpg)
  
따라서 Office 365에서 보낸 사람: 주소에 있는 도메인은 SPF 또는 dkim 시그니처의 도메인과 정렬 되 고 그렇지 않으면 메시지가 합법적 임을 나타내는 다른 내부 신호가 포함 되어 있어야 합니다. 그렇지 않으면 메시지가 compauth가 실패 합니다. 
  
```
Authentication-Results: spf=none (sender IP is 5.6.7.8)
  smtp.mailfrom=maliciousDomain.com; contoso.com; dkim=pass
  (signature was verified) header.d=maliciousDomain.com;
  contoso.com; dmarc=none action=none header.from=contoso.com;
  compauth=fail reason=001
From: sender@contoso.com
To: someone@example.com
```

따라서 Office 365 스푸핑 방지는 인증을 사용 하지 않고 도메인을 보호 하 고, 인증을 설정 하지만, 사용자가 확인 하 여 메시지를 보낸 것으로 간주 되는 도메인에 대 한 것과 비교 합니다. 조직 내의 도메인과 조직 외부의 도메인 모두에 적용 됩니다.
  
따라서 복합 인증을 실패 하 고 스푸핑된로 표시 된 메시지를 수신 하는 경우, 메시지가 spf 및 dkim을 통과 한 도메인은 보낸 사람: 주소에 있는 도메인과 맞지 않기 때문입니다.
  
### <a name="understanding-changes-in-how-spoofed-emails-are-treated"></a>스푸핑된 전자 메일이 처리 되는 방식에 대 한 변경 내용 이해

현재, Office 365에서 모든 조직에 대해 거부 또는 격리 정책과 함께 DMARC에 실패 하는 메시지는 스팸으로 표시 되며, 일반적으로 신뢰도가 높은 스팸 작업을 수행 하거나, 간혹 다른 스팸 작업을 실행 합니다. 규칙을 먼저 스팸으로 식별 합니다. 조직 내 스푸핑 검색은 일반 스팸 작업을 수행 합니다. 이 동작을 사용 하도록 설정할 필요는 없으며, 사용 하지 않도록 설정할 수는 없습니다.
  
그러나 도메인 간 스푸핑 메시지의 경우이 변경 이전에는 일반 스팸, 피싱 및 맬웨어 검사를 통과 하 고, 필터의 다른 부분에서 의심 스러운 것으로 식별 한 경우 각각을 스팸, 피싱 또는 맬웨어로 표시 합니다. 새로운 도메인 간 스푸핑 보호를 사용 하면 인증할 수 없는 모든 메시지는 기본적으로 피싱 \> 방지 스푸핑 방지 정책에 정의 된 작업을 수행 합니다. 정의 되지 않은 경우 사용자 정크 메일 폴더로 이동 됩니다. 경우에 따라 의심 스러운 메시지에는 메시지에 빨간색 보안 팁이 추가 될 수도 있습니다.
  
이로 인해 이전에는 스팸으로 표시 되었지만 여전히 스팸으로 표시 되었지만 이제는 빨간색 안전 팁이 있는 메시지가 발생할 수 있습니다. 다른 경우에는 이전에 스팸이 아닌 것으로 표시 되었던 메시지가 스팸으로 표시 되 고 (CAT: 스푸핑) 빨간색 보안 팁이 추가 됩니다. 여전히 모든 스팸 및 피싱을 격리로 이동 하는 고객은 이제 정크 메일 폴더 (이 동작을 변경할 수 있음)에 표시 되는 것을 보게 됩니다. [](#changing-your-anti-spoofing-settings)
  
메시지는 여러 가지 방법으로 스푸핑 될 수 있습니다 (이 문서 앞부분의 [서로 다른 스푸핑 유형 간 구분](#differentiating-between-different-types-of-spoofing) 참조). 그러나 Office 365에서 이러한 메시지가 아직 통합 되지 않은 방식으로는 3 월 2018 다음 표에서는 도메인 간 스푸핑 보호 기능이 새로운 동작인 빠른 요약을 소개 합니다. 
  
|**스푸핑 유형**|**범주**|**보안 팁이 추가 되었습니까?**|**적용 대상**|
|:-----|:-----|:-----|:-----|
|DMARC fail (격리 또는 거부)  <br/> |hspm (기본값), SPM 또는 phsh 일 수도 있습니다.  <br/> |아니요 (아직 없음)  <br/> |모든 Office 365 고객, Outlook.com  <br/> |
|자체에서 자체  <br/> |SPM  <br/> |예  <br/> |모든 Office 365 조직, Outlook.com  <br/> |
|도메인 간  <br/> |신분을  <br/> |예  <br/> |Office 365 Advanced Threat Protection 및 E5 고객  <br/> |

### <a name="changing-your-anti-spoofing-settings"></a>스푸핑 방지 설정 변경

(도메인 간) 스푸핑 방지 설정을 만들거나 업데이트 하려면 보안 \> \> &amp; 및 준수 센터의 위협 관리 정책 탭 아래에서 피싱 방지 스푸핑 설정으로 이동 합니다. 피싱 방지 설정을 작성 한 적이 없는 경우에는 다음을 만들어야 합니다.
  
![피싱 방지-새 정책 만들기](media/9337ec91-270e-4fa7-9dfa-a51a2d1eb95e.jpg)
  
이미 만든 경우에는 해당 항목을 선택 하 여 수정할 수 있습니다.
  
![피싱 방지-기존 정책 수정](media/75457a7c-882e-4984-80d1-21a12b42c53a.jpg)
  
방금 만든 정책을 선택 하 고 [스푸핑 인텔리전스에 대 한 자세한](learn-about-spoof-intelligence.md)정보에 설명 된 대로 단계를 진행 합니다.
  
![스푸핑 방지 사용 또는 사용 안 함](media/c49e2147-c954-443c-9144-1cbd139e1166.jpg)
  
![스푸핑 방지 보안 팁을 사용 하거나 사용 하지 않도록 설정](media/eec7c407-31fc-4f73-8325-307d82d1fb53.jpg)
  
PowerShell을 사용 하 여 새 정책을 만들려면 다음을 수행 합니다. 
  
```powershell
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

그런 다음 [AntiphishPolicy](https://docs.microsoft.com/powershell/module/exchange/advanced-threat-protection/Set-AntiPhishPolicy?view=exchange-ps)의 설명서에 따라 PowerShell을 사용 하 여 피싱 방지 정책 매개 변수를 수정할 수 있습니다. $name를 매개 변수로 지정할 수 있습니다.
  
```powershell
Set-AntiphishPolicy -Identity $name <fill in rest of parameters>
```

나중에 기본 정책을 만들 필요 없이 2018에서 조직의 모든 받는 사람에 대 한 범위를 지정 하 여 해당 사용자가 수동으로 지정할 필요가 없도록 하 고 (아래 스크린샷은 최종 구현 전에 변경 될 수 있습니다.)
  
![피싱 방지에 대 한 기본 정책](media/1f27a0bf-e202-4e12-bbac-24baf013c8f9.jpg)
  
만드는 정책과 달리 기본 정책을 삭제 하거나, 해당 우선 순위를 수정 하거나, 범위를 지정할 사용자, 도메인 또는 그룹을 선택할 수 없습니다.
  
![피싱 방지 기본 정책 세부 정보](media/30c21ceb-df52-4c93-aa65-f44a55dc1009.jpg)
  
PowerShell을 사용 하 여 기본 보호를 설정 하려면
  
```powershell
$defaultAntiphishPolicy = Get-AntiphishPolicy | ? {$_.IsDefault -eq $true}
Set-AntiphishPolicy -Identity $defaultAntiphishPolicy.Name -EnableAntispoofEnforcement <$true|$false>
```

Office 365 앞에 다른 메일 서버 또는 서버가 있는 경우 스푸핑 방지 보호를 사용 하지 않도록 설정 해야 합니다 (자세한 내용은 스푸핑을 사용 하지 않도록 설정 하는 합법적인 시나리오 참조).
  
```powershell
$defaultAntiphishPolicy = Get-AntiphishiPolicy | ? {$_.IsDefault $true}
Set-AntiphishPolicy -Identity $defaultAntiphishPolicy.Name -EnableAntispoofEnforcement $false 

```
> [!IMPORTANT]
> 전자 메일 경로의 첫 번째 홉이 Office 365이 고 위장로 표시 된 합법적인 메일이 너무 많이 있는 경우 먼저 스푸핑된 전자 메일을 보낼 수 있는 보낸 사람을 도메인에 설정 해야 합니다 ( *"보내는 합법적인 보낸 사람 관리" 섹션 참조). nauthenticated 전자 메일 "* ) 여전히 너무 많은 가양성 (즉, 스푸핑으로 표시 된 합법적인 메시지)을 사용 하는 경우 스푸핑 방지 보호 기능을 완전히 해제 하지 않는 것이 좋습니다. 대신, 고급 보호 대신 기본을 선택 하는 것이 좋습니다. 장기적으로 비용이 훨씬 더 많이 부과 되는 스푸핑된 전자 메일에 조직을 공개 하는 것 보다 가양성을 통해 작업 하는 것이 좋습니다.

### <a name="managing-legitimate-senders-who-are-sending-unauthenticated-email"></a>인증 되지 않은 전자 메일을 보내는 합법적인 보낸 사람 관리

Office 365에서는 인증 되지 않은 전자 메일을 조직에 보내는 사용자를 추적 합니다. 서비스가 보낸 사람이 합법적이 아닌 것으로 생각 하는 경우에는이를 *compauth* 실패로 표시 합니다. 이는 메시지에 적용 된 스푸핑 방지 정책에 따라 결정 되지만 스푸핑으로 분류 됩니다.
  
그러나 관리자는 스푸핑된 전자 메일을 전송 하는 데 허용 되는 보낸 사람을 지정 하 여 Office 365의 결정을 무시할 수 있습니다.
  
**방법 1-조직에서 도메인을 소유 하는 경우 전자 메일 인증 설정**
  
이 방법을 사용 하 여 조직 내 스푸핑 및 여러 테 넌 트를 소유 하거나 상호 작용 하는 경우 도메인 간 스푸핑을 확인할 수 있습니다. 또한 Office 365 내의 다른 고객에 게 보내는 도메인 간 스푸핑 및 다른 공급자에서 호스트 되는 타사를 확인 하는 데에도 도움이 됩니다.
  
자세한 내용은 [Office 365 고객](#customers-of-office-365)을 참조 하세요.

**방법 2-스푸핑 인텔리전스를 사용 하 여 인증 되지 않은 전자 메일의 허용 된 보낸 사람 구성**
  
또한 [스푸핑 인텔리전스](https://support.office.com/article/Learn-more-about-spoof-intelligence-978c3173-3578-4286-aaf4-8a10951978bf) 를 사용 하 여 보낸 사람이 조직에 인증 되지 않은 메시지를 전송 하도록 허용할 수도 있습니다. 
  
외부 도메인의 경우 스푸핑된 사용자는 보낸 사람 주소의 도메인 이지만, 보내는 인프라는 보내는 ip 주소 (/24 CIDR 범위) 또는 PTR 레코드의 조직 도메인 (아래 스크린샷, 즉, 전송 ip가 사용 됨) 일 수 있습니다. 해당 PTR 레코드가 outbound.mail.protection.outlook.com 되 고이를 보내는 인프라에 대 한 outlook.com 131.107.18.4 표시 됩니다.
  
이 보낸 사람이 인증 되지 않은 전자 메일을 보내도록 허용 하려면 **아니요** 를 **예**로 변경 합니다.
  
![스푸핑 방지 허용-보낸 사람 설정](media/d4334921-d820-4334-8217-788279701e94.jpg)
  
또한 PowerShell을 사용 하 여 특정 보낸 사람이 도메인을 스푸핑할 수 있도록 할 수 있습니다.
  
```powershell
$file = "C:\My Documents\Summary Spoofed Internal Domains and Senders.csv"
```

```powershell
Get-PhishFilterPolicy -Detailed -SpoofAllowBlockList -SpoofType External | Export-CSV $file
```

![Powershell에서 스푸핑된 보낸 사람 가져오기](media/0e27ffcf-a5db-4c43-a19b-fa62326d5118.jpg)
  
이전 이미지에서이 스크린샷을 맞추도록 추가 줄 바꿈이 추가 되었습니다. 일반적으로 모든 값이 한 줄에 표시 됩니다.
  
파일을 편집 하 여 outlook.com 및 bing.com에 해당 하는 줄을 찾고 allowedtospoof 항목을 아니요에서 예로 변경 합니다.
  
![Powershell에서 스푸핑 허용을 예로 설정](media/62340452-62d3-4958-9ce9-afe5275a870d.jpg)
  
파일을 저장 하 고 다음을 실행 합니다.
  
```powershell
$UpdateSpoofedSenders = Get-Content -Raw "C:\My Documents\Spoofed Senders.csv"
Set-PhishFilterPolicy -Identity Default -SpoofAllowBlockList $UpdateSpoofedSenders
```

이제 bing.com가 outlook.com에서 \*인증 되지 않은 전자 메일을 보낼 수 있습니다.

**방법 3-보낸 사람/받는 사람 쌍에 대해 허용 항목 만들기**
  
특정 보낸 사람에 대해 모든 스팸 필터링을 무시 하도록 선택할 수도 있습니다. 자세한 내용은 [Office 365에서 허용 목록에 안전 하 게 보낸 사람을 추가](https://blogs.msdn.microsoft.com/tzink/2017/11/29/how-to-securely-add-a-sender-to-an-allow-list-in-office-365/)하는 방법을 참조 하세요.
  
이 방법을 사용 하는 경우 스팸 및 일부 피싱 필터링은 건너뛰고 맬웨어 필터링은 제외 됩니다.
  
**방법 4-보낸 사람에 게 문의 하 여 전자 메일 인증을 설정 하도록 요청**
  
스팸 및 피싱 문제로 인해 모든 보낸 사람에 게 전자 메일 인증을 설정 하는 것이 좋습니다. 보내는 도메인의 관리자를 알고 있는 경우에는 해당 사용자에 게 연락 하 여 재정의를 추가할 필요가 없도록 전자 메일 인증 레코드를 설정 하도록 요청 합니다. 자세한 내용은이 문서 뒷부분의 [Office 365 고객 이외의 도메인 관리자](#administrators-of-domains-that-are-not-office-365-customers)를 참조 하세요. 
  
전송 도메인을 처음으로 확인 하는 것이 어려운 일 이지만 시간이 지남에 따라 전자 메일 필터는 junking을 시작 하거나 전자 메일을 거부 하 게 되므로 적절 한 레코드를 설정 하 여 배달을 향상 시킬 수 있습니다.
  
### <a name="viewing-reports-of-how-many-messages-were-marked-as-spoofed"></a>스푸핑된로 표시 된 메시지의 수 보고

스푸핑 방지 정책을 사용 하도록 설정한 후에는 위협 인텔리전스를 사용 하 여 피싱로 표시 된 메시지의 수를 확인할 수 있습니다. 이렇게 하려면 Threat Management &amp; \> Explorer 아래에서 SCC (보안 준수 센터)로 이동 하 여 보기를 피싱으로 설정 하 고 보낸 사람 도메인 또는 보호 상태별로 그룹화 합니다.
  
![피싱으로 표시 되는 메시지 수 보기](media/de25009a-44d4-4c5f-94ba-9c75cd9c64b3.jpg)
  
다양 한 보고서와 상호 작용 하 여 스푸핑으로 표시 된 메시지를 포함 하 여 피싱로 표시 한 항목을 확인할 수 있습니다. 자세한 내용은 [Office 365 위협 인텔리전스 시작](get-started-with-ti.md)하기를 참조 하세요.
  
다른 유형의 피싱 (일반 피싱, 도메인 또는 사용자 가장 등)과 달리 위장로 인해 표시 된 메시지는 아직 분할할 수 없습니다. 그러나 나중에는 보안 &amp; 및 준수 센터를 통해이 작업을 수행할 수 있습니다. 이렇게 하 고 나면이 보고서를 시작 위치로 사용 하 여 인증 오류가 발생 한 것으로 확인 된 합법적 일 수 있는 전송 도메인을 확인할 수 있습니다.
  
다음 스크린샷은이 데이터를 표시 하는 방법에 대 한 제안이 며, 출시 시 변경 될 수 있습니다.
  
![검색 유형별 피싱 보고서 보기](media/dd25d63f-152c-4c55-a07b-184ecda2de81.jpg)
  
ATP 및 E5 고객의 경우 이러한 보고서는 나중에 TPS (Threat Protection 상태) 보고서 아래에서 사용할 수 있지만 최소 24 시간 이상 지연 됩니다. 이 페이지는 보안 &amp; 및 준수 센터에 통합 될 때 업데이트 됩니다.
  
### <a name="predicting-how-many-messages-will-be-marked-as-spoof"></a>스푸핑으로 표시 되는 메시지 수 예측

Office 365에서 설정을 업데이트 하 여 스푸핑 방지 적용을 해제 하거나 기본 또는 높은 적용을 사용 하는 경우에는 다양 한 설정에서 메시지 처리가 변경 되는 방식을 확인할 수 있습니다. 즉, 스푸핑 방지가 해제 된 경우 기본으로 설정 하는 경우 스푸핑으로 검색 되는 메시지 수를 확인할 수 있습니다. 그렇지 않은 경우에는 스푸핑으로 검색 되는 메시지 수를 높게 볼 수 있습니다.
  
이 기능은 현재 개발 중입니다. 세부 정보가 더 정의 되 면이 페이지는 보안 및 준수 센터의 스크린샷 및 PowerShell 예제와 함께 업데이트 됩니다.
  
![스푸핑 방지를 사용 하도록 설정 하는 "What If" 보고서](media/fdd085ae-02c1-4327-a063-bfe9a32ff1eb.jpg)
  
![스푸핑된 보낸 사람을 허용 하기 위한 가능한 UX](media/53f9f73e-fb01-47f3-9a6d-850c1aef5efe.jpg)
  
### <a name="understanding-how-spam-phishing-and-advanced-phishing-detections-are-combined"></a>스팸, 피싱 및 고급 피싱 감지의 결합 방식 이해

교환의 유무에 관계 없이 Exchange Online을 사용 하는 조직에서는 서비스에서 맬웨어, 스팸, 높은 신뢰도 스팸, 피싱 및 대량으로 메시지를 식별할 때 수행할 작업을 지정할 수 있습니다. atp 고객에 대 한 atp 피싱 방지 정책 및 EOP 고객을 위한 피싱 방지 정책 및 메시지가 여러 검색 유형 (예: 맬웨어, 피싱 및 사용자 가장)을 적중 할 수 있다는 사실은 몇 가지 혼동이 있을 수 있습니다. 정책이 적용 됩니다.
  
일반적으로 메시지에 적용 되는 정책은 CAT (Category) 속성의 스팸 방지-Report 헤더에서 식별 됩니다.
  
|**우선 순위**|**정책**|**범주**|**관리 되는 위치**|**적용 대상**|
|:-----|:-----|:-----|:-----|:-----|
|개  <br/> |맬웨어  <br/> |MALW  <br/> |[맬웨어 정책](configure-anti-malware-policies.md) <br/> |모든 조직  <br/> |
|2  <br/> |메시지일  <br/> |phsh  <br/> |[스팸 필터 정책 구성](configure-your-spam-filter-policies.md) <br/> |모든 조직  <br/> |
|3(sp3)  <br/> |높은 정확도 스팸  <br/> |hspm  <br/> |[스팸 필터 정책 구성](configure-your-spam-filter-policies.md) <br/> |모든 조직  <br/> |
|1-4  <br/> |방지할  <br/> |신분을  <br/> |[피싱 방지 정책](https://go.microsoft.com/fwlink/?linkid=864553), [스푸핑 인텔리전스](learn-about-spoof-intelligence.md) <br/> |모든 조직  <br/> |
|2-5  <br/> |스팸일  <br/> |SPM  <br/> |[스팸 필터 정책 구성](configure-your-spam-filter-policies.md) <br/> |모든 조직  <br/> |
|번  <br/> |대량  <br/> |대량  <br/> |[스팸 필터 정책 구성](configure-your-spam-filter-policies.md) <br/> |모든 조직  <br/> |
|연중  <br/> |도메인 가장  <br/> |dimp  <br/> |[Office 365 ATP 피싱 방지 및 피싱 방지 정책 설정](set-up-anti-phishing-policies.md) <br/> |ATP만 있는 조직  <br/> |
|8  <br/> |사용자 가장  <br/> |uimp  <br/> |[Office 365 ATP 피싱 방지 및 피싱 방지 정책 설정](set-up-anti-phishing-policies.md) <br/> |ATP만 있는 조직 <br/> |

다양 한 피싱 방지 정책이 여러 개 있는 경우 우선 순위가 가장 높은 정책 중 하나가 적용 됩니다. 예를 들어 다음과 같은 두 가지 정책이 있다고 가정 합니다.

|**정책**|**우선 순위**|**사용자/도메인 가장**|**스푸핑 방지**|
|:-----|:-----|:-----|:-----|
|A  <br/> |개  <br/> |켜짐  <br/> |Off  <br/> |
|B  <br/> |2  <br/> |Off  <br/> |켜짐  <br/> |

메시지가 스푸핑 및 사용자 가장으로 식별 되 고 동일한 사용자 집합이 정책 a 및 정책 B로 범위가 지정 된 경우에는 메시지가 스푸핑으로 취급 되지만 스푸핑 방지 기능이 해제 된 이후에는 아무 작업도 적용 되지 않습니다. 은 사용자 가장 (8) 보다 높은 우선 순위 (4)에서 실행 됩니다.
  
다른 유형의 피싱 정책이 적용 되도록 하려면 다양 한 정책이 적용 되는 사용자의 설정을 조정 해야 합니다.
  
### <a name="legitimate-scenarios-to-disable-anti-spoofing"></a>스푸핑 방지를 사용 하지 않도록 설정 하는 합법적인 시나리오

스푸핑 방지 기능은 피싱 공격 으로부터 고객을 보호 하므로 스푸핑 방지 보호 기능을 사용 하지 않는 것이 좋습니다. 이를 사용 하지 않도록 설정 하면 일부 단기 가양성을 해결할 수 있지만 긴 용어를 통해 더 많은 위험에 노출 됩니다. 보낸 사람에 게 인증을 설정 하거나 피싱 정책에서 조정을 수행 하는 데 드는 비용은 일반적으로 일회성 이벤트 이거나 최소한의 정기적인 유지 관리만을 필요로 합니다. 그러나 데이터가 노출 되거나 자산이 손상 된 경우에는 피싱 공격에서 복구 하는 데 드는 비용이 더 많이 듭니다.
  
따라서 스푸핑 방지 보호를 사용 하지 않도록 설정 하는 것 보다 위조 방지 가양성을 통해 작업 하는 것이 좋습니다.
  
그러나 메시지 라우팅에 추가 메일 필터링 제품이 있고 Office 365이 전자 메일 경로의 첫 번째 홉이 아닌 경우에는 위조를 사용 하지 않도록 설정 해야 하 고, 다음과 같은 경우에 해당 하는 합법적인 시나리오가 있습니다.
  
![고객 MX 레코드가 Office 365를 가리키지 않음](media/62127c16-cfb8-4880-9cad-3c12d827c67e.jpg)
  
다른 서버는 Exchange 온-프레미스 메일 서버, ironpor와 같은 메일 필터링 장치 또는 다른 클라우드 호스팅 서비스 일 수 있습니다.
  
받는 사람 도메인의 mx 레코드가 office 365를 가리키지 않으면 office 365에서 수신 하는 도메인의 MX 레코드를 조회 하 고 다른 서비스를 가리키면 스푸핑 방지를 표시 하지 않으므로 위조를 사용 하지 않도록 설정할 필요가 없습니다. 도메인에 프런트에 다른 서버가 있는지 모르는 경우 mx 도구 상자와 같은 웹 사이트를 사용 하 여 mx 레코드를 조회할 수 있습니다. 예를 들면 다음과 같습니다.
  
![도메인이 Office 365를 가리키지 않음을 나타내는 MX 레코드](media/d868bb9f-3462-49aa-baea-9447a3ce4877.jpg)
  
이 도메인에는 office 365을 가리키지 않는 MX 레코드가 있으므로 office 365에서 스푸핑 방지 적용을 적용 하지 않습니다.
  
그러나 받는 사람 도메인의 MX 레코드가 office 365을 ** 가리키고 있어도 office 365에 다른 서비스가 있더라도 스푸핑 방지를 사용 하지 않도록 설정 해야 합니다. 가장 일반적인 예는 받는 사람 재작성을 사용 하는 것입니다. 
  
![받는 사람 다시 쓰기에 대 한 라우팅 다이어그램](media/070d90d1-50a0-42e4-9fd3-920bc99a7cad.jpg)
  
contoso의 mx 레코드는 온-프레미스 서버를 가리키며 @office365 도메인의 mx 레코드는 mx 레코드에 protection.outlook.com 또는 \* \*eo.outlook.com을 포함 하므로 Office 365을 가리킵니다.
  
![MX 레코드가 Office 365를 가리키며, 받는 사람 재작성](media/4101ad51-ef92-4907-b466-b41d14d344ca.jpg)
  
받는 사람 도메인의 MX 레코드가 Office 365를 가리키지 않는 경우 및 받는 사람이 다시 쓰기를 수행 했을 때를 구분 해야 합니다. 두 경우의 차이점을 반드시 고려해 야 합니다.
  
수신 도메인이 받는 사람을 재작성 했는지 여부를 확실 하지 않으면 메시지 헤더를 확인 하 여 확인할 수 있는 경우가 있습니다.
  
a) 먼저 인증-결과 헤더에서 받는 사람 도메인에 대 한 메시지의 헤더를 확인 합니다.
  
```
Authentication-Results: spf=fail (sender IP is 1.2.3.4)
  smtp.mailfrom=example.com; office365.contoso.net; dkim=fail
  (body hash did not verify) header.d=simple.example.com;
  office365.contoso.net; dmarc=none action=none
  header.from=example.com; compauth=fail reason=001
```

받는 사람 도메인은 위의 굵은 빨강 텍스트 (이 경우 office365.contoso.net)에서 찾을 수 있습니다. 받는 사람: 헤더에는 다음과 같은 차이가 있을 수 있습니다.
  
To: Example recipient \<recipient @ contoso.com\>
  
실제 받는 사람 도메인의 MX 레코드 조회를 수행 합니다. protection.outlook.com, mail.messaging.microsoft.com \*, \*eo.outlook.com 또는 mail.global.frontbridge.com를 포함 하는 경우 MX가 Office 365을 가리킵니다.
  
이러한 값이 포함 되어 있지 않으면 MX가 Office 365를 가리키지 않습니다. 라는 의미입니다. 이 도구를 사용 하 여 MX 도구 상자를 확인할 수 있습니다.
  
이 특정 예에서는 contoso.com가 To: 헤더 이후로 받는 사람 처럼 보이는 도메인에 온-프레미스 서버에 대 한 MX 레코드가 있음을 알리는 다음과 같은 메시지가 표시 됩니다.
  
![온-프레미스 서버를 가리키는 MX 레코드](media/2444144a-9a90-4319-96b2-d115041f669f.jpg)
  
그러나 실제 받는 사람은 MX 레코드가 Office 365를 가리키는 office365.contoso.net입니다.
  
![Office 365에 대 한 MX 점, 받는 사람 재작성 이어야 함](media/10cf3245-9b50-475a-b655-d8a51f99d812.jpg)
  
따라서이 메시지는 받는 사람이 재작성 될 수 있습니다.
  
b) 두 번째에는 받는 사람 다시 쓰기의 일반적인 사용 사례를 구분 해야 합니다. 받는 사람 도메인을 onmicrosoft.com에 \*다시 쓰도록 하려면 대신 mail.onmicrosoft.com로 \*다시 씁니다.
  
다른 서버 뒤에 라우팅되는 최종 받는 사람 도메인을 확인 하 고 받는 사람 도메인의 MX 레코드가 실제로 해당 DNS 레코드에 게시 된 Office 365를 가리키면 스푸핑 방지 기능을 사용 하지 않도록 설정할 수 있습니다.
  
라우팅 경로에서 도메인의 첫 번째 홉이 Office 365이 고 하나 이상의 서비스가 뒤에 있는 경우에만 스푸핑 방지를 사용 하지 않도록 설정 하는 것은 좋습니다.
  
### <a name="how-to-disable-anti-spoofing"></a>스푸핑 방지를 사용 하지 않도록 설정 하는 방법

이미 피싱 방지 정책을 만든 경우에는 EnableAntispoofEnforcement 매개 변수를 $false로 설정 합니다.
  
```
$name = "<name of policy>"
Set-AntiphishPolicy -Identity $name -EnableAntiSpoofEnforcement $false

```

사용 하지 않도록 설정할 정책 (또는 정책)의 이름을 모르는 경우 다음을 표시할 수 있습니다.
  
```
Get-AntiphishPolicy | fl Name
```

기존 피싱 방지 정책이 없는 경우에는 하나를 만든 다음 사용 하지 않도록 설정할 수 있습니다 (정책이 없는 경우에도, 스푸핑 방지는 계속 적용 되며 나중에 2018에 대 한 기본 정책이 생성 되며이를 만들지 않고 사용 하지 않도록 설정할 수 있음) . 여러 단계에서이 작업을 수행 해야 합니다.
  
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
# Finally, scope the anti-phishing policy to the domains
Set-AntiphishPolicy -Identity $name -EnableAntispoofEnforcement $false

```

스푸핑 해제는 cmdlet을 통해서만 사용할 수 있습니다 (나중에는 보안 &amp; 준수 센터에서 사용할 수 있음). PowerShell에 액세스할 수 없는 경우 지원 티켓을 만듭니다.
  
이는 Office 365로 전송 될 때 간접 라우팅을 수행 하는 도메인에만 적용 해야 합니다. temptation에서 잘못 된 판정으로 인해 스푸핑 방지를 사용 하지 않도록 설정 하는 것은 오랫동안 실행 하는 것이 좋습니다.
  
### <a name="information-for-individual-users"></a>개별 사용자에 대 한 정보

개별 사용자가 스푸핑 방지 안전 팁과 상호 작용 하는 방법으로 제한 됩니다. 그러나 일반적인 시나리오를 해결 하기 위해 수행할 수 있는 몇 가지 작업은 다음과 같습니다.
  
### <a name="common-scenario-1---mailbox-forwarding"></a>일반적인 시나리오 #1-사서함 전달

다른 전자 메일 서비스를 사용 하 고 전자 메일을 Office 365 또는 Outlook.com로 전달 하는 경우 전자 메일이 스푸핑으로 표시 되 고 빨간색 안전 팁이 표시 될 수 있습니다. Outlook.com가 Outlook.com, office 365, Gmail 또는 [ARC 프로토콜](https://arc-spec.org)을 사용 하는 다른 서비스 중 하나인 경우 Office 365 및에서는이를 자동으로 처리할 계획입니다. 그러나 수정 프로그램을 배포할 때까지 사용자는 전달 옵션을 사용 하는 대신 연결 된 계정 기능을 사용 하 여 메시지를 직접 가져와야 합니다.
  
office 365에서 연결 된 계정을 설정 하려면 office 365 웹 \> 인터페이스 메일 \> \> 계정 \> 연결 된 계정의 오른쪽 위 모서리에 있는 기어 아이콘을 선택 합니다.
  
![Office 365-연결 된 계정 옵션](media/e8e841ca-8861-4d83-8506-2a0858c51010.jpg)
  
Outlook.com에서이 프로세스는 기어 \> 아이콘 옵션 \> 메일 \> 계정 \> 연결 된 계정입니다.
  
### <a name="common-scenario-2---discussion-lists"></a>일반적인 시나리오 #2-토론 목록

토론 목록은 메시지를 전달 하는 방식으로 인해 스푸핑 방지와 관련 된 문제를 해결 하는 것으로 알려져 있지만 원본 위치: 주소는 그대로 유지 됩니다.
  
예를 들어 사용자의 전자 메일 주소가 user @ contoso.com 라고 가정 하면 토론 목록 birdwatchers @ example.com에 대 한 자세한 내용을 확인 하 고 참가 하는 데 관심이 있습니다. 토론 목록으로 메시지를 보낼 때 다음과 같은 방식으로 보낼 수 있습니다.
  
**보낸 사람:** John Doe \<사용자 @ contoso.com\> 
  
**대상:** Birdwatcher의 토론 목록 \<birdwatchers @ example.com\> 
  
**제목:** Mt 위쪽에 파란색 jays 잘 표시 됩니다. 이번 주 Rainier 
  
모든 사용자가이 주를 Mt에서 확인 하려고 합니다. Rainier?
  
전자 메일 목록이 메시지를 받으면 해당 메시지의 서식을 지정 하 고 해당 내용을 수정한 다음 여러 다른 전자 메일 수신기의 참가자로 구성 된 토론 목록의 나머지 구성원에 게 다시 재생 합니다.
  
**보낸 사람:** John Doe \<사용자 @ contoso.com\> 
  
**대상:** Birdwatcher의 토론 목록 \<birdwatchers @ example.com\> 
  
**제목:** [BIRDWATCHERS] Mt 위쪽에 파란색 jays 잘 표시 됩니다. 이번 주 Rainier 
  
모든 사용자가이 주를 Mt에서 확인 하려고 합니다. Rainier?
  
---
  
이 메시지는 Birdwatchers 토론 목록으로 전송 되었습니다. 언제 든 지 구독을 취소할 수 있습니다.
  
위의 경우 재생 된 메시지의 보낸 사람: address (user @ contoso.com) 그러나 제목 줄에 태그를 추가 하 고 메시지 아래쪽에 바닥글을 추가한 후 원본 메시지를 수정 했습니다. 이 유형의 메시지 수정은 메일링 리스트에서 공통적 이며 가양성이 발생할 수 있습니다.
  
자신이 나 조직의 다른 사람이 메일 그룹의 관리자 인 경우 스푸핑 방지 검사를 통과 하도록 구성할 수 있습니다.
  
- DMARC.org에서 FAQ를 확인 하세요. 메일 그룹을 [작동 했으며 DMARC과 상호 작용 하려면 어떻게 해야 하나요?](https://dmarc.org/wiki/FAQ#I_operate_a_mailing_list_and_I_want_to_interoperate_with_DMARC.2C_what_should_I_do.3F)

- [오류를 방지 하기 위해 DMARC와 상호 작용 하는 우편물 목록 운영자에 대 한 지침을](https://blogs.msdn.microsoft.com/tzink/2017/03/22/a-tip-for-mailing-list-operators-to-interoperate-with-dmarc-to-avoid-failures/) 읽어 보십시오.

- ARC를 지원 하기 위해 메일링 리스트 서버에 업데이트를 설치 하는 것을 고려 하세요.[https://arc-spec.org](https://arc-spec.org/)

메일 그룹의 소유권이 없는 경우 다음을 수행 합니다.
  
- 위의 옵션 중 하나를 구현 하기 위해 메일 그룹의 유지 관리자에 게 요청할 수 있습니다 (메일링 리스트가 릴레이 되는 도메인에 대해서도 전자 메일 인증을 설정 해야 함).

- 전자 메일 클라이언트에 사서함 규칙을 만들어 메시지를 받은 편지 함으로 이동할 수 있습니다. 인증 되지 않은 전자 메일을 보내는 합법적인 보낸 사람 관리 섹션에 설명 된 대로 허용 규칙 또는 재정의를 설정 하도록 조직의 관리자에 게 요청할 수도 있습니다.

- Office 365에서 지원 티켓을 만들어 메일 그룹에 대 한 재정의를 만들어 합법적인 것으로 취급할 수 있습니다.

### <a name="other-scenarios"></a>기타 시나리오

1. 위의 일반적인 시나리오가 모두 상황에 해당 되지 않는 경우에는 메시지를 가양성으로 Microsoft에 보고 합니다. 자세한 내용은이 문서 뒷부분에 나오는 ["스팸 또는 스팸이 아닌 메시지를 다시 Microsoft에 보고 하는 방법"](#how-can-i-report-spam-or-non-spam-messages-back-to-microsoft) 섹션을 참조 하십시오. 

2. 또한 Microsoft와의 지원 티켓을 받을 수 있는 전자 메일 관리자에 게 문의할 수 있습니다. Microsoft 엔지니어링 팀은 메시지가 스푸핑으로 표시 된 이유를 조사 합니다.

3. 또한 보낸 사람을 확인 하 고 악의적으로 위장 되는 것을 확신할 수 없는 경우 보낸 사람에 게 다시 응답 하 여 인증 되지 않은 메일 서버에서 메시지를 보내도록 합니다. 이 경우 원래 보낸 사람이 필요한 전자 메일 인증 레코드를 설정할 IT 관리자에 게 연락 하 게 됩니다.
  
보낸 사람이 도메인 소유자에 게 다시 회신할 경우 전자 메일 인증 레코드를 설정 해야 하는 경우에는 해당 사용자가 작업을 수행 하는 데 spurs 합니다. Microsoft는 또한 도메인 소유자와 함께 필요한 레코드를 게시 하는 경우에도 개별 사용자가 요청 하는 경우에도 더욱 편리 하 게 사용할 수 있습니다.

4. 원하는 경우 수신 허용-보낸 사람 목록에 보낸 사람을 추가 합니다. 그러나 phisher가 해당 계정을 위장 하면 사서함으로 배달 됩니다. 따라서이 옵션은 가끔씩만 사용 해야 합니다.

## <a name="how-senders-to-microsoft-should-prepare-for-anti-spoofing-protection"></a>Microsoft의 보낸 사람이 스푸핑 방지 보호를 준비 해야 하는 방식

현재 Microsoft에 메시지를 전송 하는 관리자 인 경우 (예: Office 365 또는 Outlook.com) 전자 메일이 제대로 인증 되는지 확인 해야 합니다 (스팸 또는 피싱으로 표시할 수 있음).
  
### <a name="customers-of-office-365"></a>Office 365의 고객

office 365 고객이 고 office 365을 사용 하 여 아웃 바운드 전자 메일을 보내는 경우:
  
- 도메인의 경우 [스푸핑을 방지 하기 위해 Office 365에서 SPF를 설정](set-up-spf-in-office-365-to-help-prevent-spoofing.md) 합니다.

- 주 도메인의 경우 [dkim을 사용 하 여 Office 365의 사용자 지정 도메인에서 전송 되는 아웃 바운드 전자 메일의 유효성을 검사](use-dkim-to-validate-outbound-email.md) 합니다.

- 도메인에 대해 [DMARC 레코드를 설정](use-dmarc-to-validate-email.md) 하 여 합법적인 보낸 사람을 확인할 수 있습니다.

Microsoft에서는 각 SPF, dkim 및 DMARC에 대 한 자세한 구현 지침을 제공 하지 않습니다. 그러나 온라인에 게시 된 정보가 많이 있습니다. 조직에서 전자 메일 인증 레코드를 설정 하는 데 도움이 되는 타사 회사도 있습니다.
  
### <a name="administrators-of-domains-that-are-not-office-365-customers"></a>Office 365 고객이 아닌 도메인 관리자

도메인 관리자 이지만 Office 365 고객이 아닌 경우:
  
- 도메인의 전송 IP 주소를 게시 하도록 SPF를 설정 하 고 메시지에 디지털 서명을 하는 dkim (사용 가능한 경우)도 설정 해야 합니다. DMARC 레코드를 설정 하는 것도 고려할 수 있습니다.

- 사용자를 대신 하 여 전자 메일을 전송 하는 대량 보낸 사람이 있는 경우 전자 메일을 사용 하 여 보낸 사람: 주소 (사용자가 속한 경우)의 보내는 도메인이 SPF 또는 DMARC를 통과 하는 도메인과 부합 되도록 해야 합니다.

- 온-프레미스 메일 서버를 사용 하거나, Microsoft Azure, godaddy, Rackspace, Amazon Web Services 또는 이와 유사한 클라우드 호스팅 서비스를 통해 보내거나,이를 사용자가 SPF 레코드에 추가할지 확인 해야 합니다.

- isp가 호스트 하는 소규모 도메인인 경우 isp에서 제공 하는 지침에 따라 SPF 레코드를 설정 해야 합니다. 대부분의 isp는 이러한 유형의 지침을 제공 하며 회사의 지원 페이지에서 찾을 수 있습니다.

- 이전에 전자 메일 인증 레코드를 게시 해야 하는 경우에도 정상적으로 작동 했지만 Microsoft로 보내려면 전자 메일 인증 레코드를 게시 하는 것이 좋습니다. 이를 통해 피싱에 대 한 싸 우기, 또는 사용자가 전송 하는 조직이 phished을 얻게 되는 가능성을 줄일 수 있습니다.

### <a name="what-if-you-dont-know-who-sends-email-as-your-domain"></a>도메인으로 전자 메일을 보낸 사람을 모르는 경우에는 어떻게 하나요?

많은 도메인은 모든 보낸 사람을 알 수 없기 때문에 SPF 레코드를 게시 하지 않습니다. 모든 사용자가 누구 인지 알 필요가 없습니다. 대신, 특히 회사 트래픽이 있는 위치에 대 한 SPF 레코드를 게시 하 고 중립 spf 정책을 게시 하는 것이 좋습니다.
  
TXT의 example.com "v = spf1 include::spf. example? all"
  
중립 SPF 정책은 회사 인프라에서 보내는 모든 전자 메일이 다른 모든 전자 메일 수신자에 게 전자 메일 인증을 통과 함을 의미 합니다. 알 수 없는 보낸 사람이 보낸 전자 메일은 중립으로 변경 되며,이는 SPF 레코드를 게시 하는 것과 거의 동일 합니다.
  
office 365로 보낼 때 회사 트래픽에 제공 되는 전자 메일은 인증 된 것으로 표시 되지만 알지 못하는 출처 로부터의 전자 메일은 여전히 스푸핑으로 표시 될 수 있습니다 (Office 365에서 암시적으로 인증할 수 있는지 여부에 따라 다름). 그러나이 기능은 Office 365에서 스푸핑으로 표시 되는 모든 전자 메일에서 여전히 개선 되었습니다.
  
대체 정책이? all 인 SPF 레코드를 시작한 후에는 더 많은 송신 인프라를 점진적으로 포함 한 다음 보다 엄격한 정책을 게시할 수 있습니다. 
  
### <a name="what-if-you-are-the-owner-of-a-mailing-list"></a>메일 그룹의 소유자 인 경우에는 어떻게 하나요?

[일반적인 시나리오 #2 토론 목록](#common-scenario-2---discussion-lists)섹션을 참고 하십시오.
  
### <a name="what-if-you-are-an-infrastructure-provider-such-as-an-internet-service-provider-isp-email-service-provider-esp-or-cloud-hosting-service"></a>ISP (인터넷 서비스 공급자), ESP (전자 메일 서비스 공급자) 또는 클라우드 호스팅 서비스와 같은 인프라 공급자는 무엇 인가요?

도메인의 전자 메일을 호스팅하고 전자 메일을 보내거나 전자 메일을 보낼 수 있는 호스팅 인프라를 제공 하는 경우 다음을 수행 해야 합니다.
  
- 고객에 게 SPF 레코드에 게시할 내용을 자세히 설명 하는 문서가 있는지 확인

- 고객은 아웃 바운드 전자 메일에 대해 dkim-서명 (기본 도메인에 서명)을 명시적으로 설정 하지 않아도 서명을 사용 하는 것이 좋습니다. 주소를 설정한 경우 고객의 도메인을 사용 하 여 전자 메일에 이중 서명을 하 고, 회사의 dkim 서명을 사용 하 여 두 번째 시간을 사용할 수도 있습니다.

microsoft에 대 한 배달 기능은 플랫폼에서 보내는 전자 메일을 인증 하는 경우에도 보장 되지 않지만 최소한 microsoft는 인증 되지 않아 전자 메일을 정크로 보내지 않습니다. Outlook.com에서 전자 메일을 필터링 하는 방법에 대 한 자세한 내용은 [Outlook.com 전자](https://postmaster.live.com/pm/postmaster.aspx)메일 프로그램 페이지를 참조 하세요.
  
서비스 공급자 모범 사례에 대 한 자세한 내용은 [M3AAWG Mobile Messaging 모범 사례 서비스 공급자](https://www.m3aawg.org/sites/default/files/M3AAWG-Mobile-Messaging-Best-Practices-Service-Providers-2015-08.pdf)를 참조 하세요.
  
## <a name="frequently-asked-questions"></a>질문과 대답

### <a name="why-is-microsoft-making-this-change"></a>Microsoft에서이 변경 사항을 수행 하는 이유는 무엇 인가요?

피싱 공격이 미치는 영향과 15 년 동안 전자 메일 인증을 사용 하는 중에는 Microsoft가 인증 되지 않은 전자 메일을 계속 허용 하는 위험이 합법적인 전자 메일이 손실 되는 위험 보다 높다는 것을 생각 합니다.
  
### <a name="will-this-change-cause-legitimate-email-to-be-marked-as-spam"></a>이 변경으로 인해 합법적인 전자 메일이 스팸으로 표시 됩니까?

먼저 스팸으로 표시 되는 몇 가지 메시지가 있습니다. 그러나 시간이 지남에 따라 보낸 사람이 조정 되 고 스푸핑된로 mislabeled 된 메시지의 양은 대부분의 전자 메일 경로에서 무시 됩니다.
  
Microsoft 자체는이 기능을 몇 주 전에 먼저 채택 했으며 나머지 고객에 게 배포할 수 있습니다. 처음에 장애 발생 했지만, 서서히 거절 됩니다.
  
### <a name="will-microsoft-bring-this-feature-to-outlookcom-and-non-advanced-threat-protection-customers-of-office-365"></a>Microsoft가 Office 365의 Outlook.com 및 고급 위협 보호 고객에 게이 기능을 제공할 것인가?

Microsoft의 스푸핑 방지 기술은 처음에 office 365 Enterprise E5 구독을 사용 하거나 구독을 위한 office 365 Advanced Threat Protection (ATP) 추가 기능을 구매한 조직에 배포 되었습니다. 2018 년 10 월 이전에는 EOP (Exchange Online protection)를 포함 하는 조직에 대 한 보호 기능이 확장 되었습니다. 향후에는 Outlook.com에 대 한 릴리스를 출시할 수 있을 것입니다. 그러나 이렇게 하면 보고 및 사용자 지정 재정의와 같은 일부 기능이 적용 되지 않을 수 있습니다.
  
### <a name="how-can-i-report-spam-or-non-spam-messages-back-to-microsoft"></a>스팸 또는 스팸이 아닌 메시지를 Microsoft에 다시 신고 하려면 어떻게 해야 합니까?

[Outlook 용 보고서 메시지 추가 기능](https://support.office.com/article/use-the-report-message-add-in-b5caa9f1-cdf3-4443-af8c-ff724ea719d2)을 사용 하거나, 설치 되어 있지 않은 경우에는 [스팸, 스팸이 아닌 사용자 및 피싱 사기 메시지를 분석을 위해 Microsoft에 제출](https://technet.microsoft.com/en-us/library/jj200769%28v=exchg.150%29.aspx)합니다.
  
### <a name="im-a-domain-administrator-who-doesnt-know-who-all-my-senders-are"></a>내 모든 보낸 사람을 모르는 도메인 관리자입니다.

[Office 365 고객이 아닌 도메인의 관리자에 게](#administrators-of-domains-that-are-not-office-365-customers)문의 하세요.
  
### <a name="what-happens-if-i-disable-anti-spoofing-protection-for-my-organization-even-though-office-365-is-my-primary-filter"></a>조직에서 스푸핑 방지 보호 기능을 사용 하지 않도록 설정한 경우 Office 365이 기본 필터 이더라도 어떻게 되나요?

더 이상 누락 된 피싱 및 스팸 메시지에 노출 되므로이 작업을 수행 하지 않는 것이 좋습니다. 모든 피싱이 스푸핑 중인 것은 아니며 일부 스푸핑도 누락 되지 않습니다. 그러나 보안 스푸핑을 사용 하도록 설정 하는 고객에 게는 위험이 더 커집니다.
  
### <a name="does-enabling-anti-spoofing-protection-mean-i-will-be-protected-from-all-phishing"></a>스푸핑 방지 보호를 사용 하도록 설정 하 여 모든 피싱 으로부터 보호 합니다.

아쉽게도 phishers는 손상 된 계정 등의 다른 기술을 사용 하거나 무료 서비스의 계정을 설정 하는 데에는 적합 하지 않습니다. 그러나 Office 365의 보호 레이어가 함께 작동 하 고 서로의 위쪽에 구축 되므로 피싱 방지 보호 기능은 이러한 다른 유형의 피싱 방법을 보다 효율적으로 검색 하는 데 도움이 됩니다.
  
### <a name="do-other-large-email-receivers-block-unauthenticated-email"></a>다른 대규모 전자 메일 수신기가 인증 되지 않은 전자 메일을 차단 하나요?

거의 모든 대규모 전자 메일 수신기는 기존 SPF, dkim 및 DMARC을 구현 합니다. 일부 수신기는 이러한 표준 보다 엄격한 다른 검사를 하지만, 인증 되지 않은 전자 메일을 차단 하 고이를 스푸핑으로 취급 하기 위해 Office 365 만큼 이동 하는 것은 거의 안 됩니다. 그러나 대부분의 산업은 특히 피싱 문제로 인해이 특정 유형의 전자 메일에 비해 점점 더 엄격 합니다.
  
### <a name="do-i-still-need-the-advanced-spam-filtering-option-enabled-for-spf-hard-fail-if-i-enable-anti-spoofing"></a>스푸핑 방지를 사용 하도록 설정한 경우에도 "SPF 하드 실패"에 대해 고급 스팸 필터링 옵션이 사용 되도록 설정 되어 있어야 합니까?

아니요, SPF 하드에 오류가 발생 하는 것을 고려 하지 않고 보다 광범위 한 기준 집합을 사용 하므로이 옵션은 더 이상 필요 하지 않습니다. 스푸핑 방지를 사용 하도록 설정 하 고 SPF 하드 실패 옵션을 사용 하도록 설정한 경우에는 가양성 결과가 더 많이 얻게 됩니다. 스팸 또는 피싱에 대 한 추가 catch를 거의 제공 하지 않고 대신 대부분의 가양성을 생성 하는 것과 같은 기능을 사용 하지 않는 것이 좋습니다.
  
### <a name="does-sender-rewriting-scheme-srs-help-fix-forwarded-email"></a>보낸 사람 다시 쓰기 구성표 (SRS)가 전달 된 전자 메일을 수정 합니까?

SRS는 전달 된 전자 메일의 문제만 부분적으로 수정 합니다. SRS는에서 SMTP 메일을 다시 작성 하 여 전달 된 메시지가 다음 목적지에서 SPF를 통과 하도록 할 수 있습니다. 그러나 스푸핑 방지는 보낸 사람 또는 dkim 도메인 (또는 기타 신호의)과 함께 from: 주소를 기반으로 하므로 전달 된 전자 메일이 스푸핑된로 표시 되지 않도록 하는 것은 충분 하지 않습니다.