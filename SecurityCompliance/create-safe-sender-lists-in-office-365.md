---
title: Office 365에서 수신 허용-보낸 사람 목록 만들기
ms.author: tracyp
author: MSFTTracyP
manager: laurawi
ms.date: 4/29/2019
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150s
ms.assetid: 9721b46d-cbea-4121-be51-542395e6fd21
description: 특정 보낸 사람의 메일을 수신 하는 경우 해당 사용자와 해당 메시지를 신뢰 하기 때문에 Exchange 관리 센터의 스팸 필터 정책에서 허용 목록을 조정할 수 있습니다.
ms.openlocfilehash: b97767a3ee4882b1a9b052bc845e8758a6402534
ms.sourcegitcommit: e834d4168f584f2efb22479aec108497eea267f6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/04/2019
ms.locfileid: "34709116"
---
# <a name="create-safe-sender-lists-in-office-365"></a>Office 365에서 수신 허용-보낸 사람 목록 만들기

사용자가 특정 보낸 사람이 나 보낸 사람에 게 메시지를 신뢰 하 여 전자 메일을 받을 수 있도록 하려면 여러 가지 방법을 선택할 수 있습니다. 이러한 옵션에는 ETRs (Exchange 전송 규칙), Outlook 수신 허용-보낸 사람, IP 허용 목록, 스팸 방지 보낸 사람/도메인 허용 목록이 있습니다.

> [!IMPORTANT]
> 조직 허용 목록을 사용 하 여 가양성을 처리 하는 경우에는이를 임시 솔루션으로 간주 하 여 가능한 경우 피해 야 합니다. 실수로 조직을 위장, 가장 및 기타 공격까지 쉽게 열 수 있으므로 허용 목록을 사용 하 여 가양성을 관리 하는 것은 권장 되지 않습니다. 이 용도로 허용 목록을 사용 하는 경우에는 준비 상태에서 [스팸, 스팸 아님 및 피싱 메일을 분석용으로 Microsoft에 제출](https://docs.microsoft.com/en-us/office365/SecurityCompliance/submit-spam-non-spam-and-phishing-scam-messages-to-microsoft-for-analysis)하기 위한 문서를 vigilant 야 합니다.

안전한 보낸 사람 목록을 구성 하는 권장 방법은 다음과 같이 ETRs (Exchange 전송 규칙)를 사용 하 여 올바른 메시지만 허용 되도록 하는 것입니다. *스팸 방지 정책 전자 메일 주소* 및 *도메인 기반 허용 목록은* 도메인을 쉽게 스푸핑 가능으로 하기 때문에 *IP 주소 기반 목록* 만큼 안전 하지 않습니다. 그러나 스팸 방지 정책 IP 기반 허용 목록에는 해당 IP를 통해 전송 되는 모든 도메인에서 스팸 필터링을 우회 하도록 허용 되는 위험도 표시 됩니다. 신중 하 게 수행 하 ** 고 예외를 자세히 모니터링 하세요.

> [!IMPORTANT]
> **차단 된 보낸 사람 목록을** 만드는 방법에 대 한 정보는 [여기에 나와](create-block-sender-lists-in-office-365.md)있습니다.

## <a name="options-from-most-to-least-recommended"></a>가장 이상 권장 하지 않는 옵션

대부분의 보안 조치를 우회 하므로 허용 목록은 항상 제한 해야 합니다. 무시할 수 있는 사용자를 확인 하려면 표준 유지 관리의 일부로 모든 허용 목록을 다시 검사 해야 합니다. 가능한 경우 제한적 ETRs를 사용 하는 것이 좋습니다.

- Exchange 전송 규칙 (메일 흐름 규칙이 라고도 함)
- Outlook 수신 허용-보낸 사람
- 스팸 방지 정책: IP 허용 목록
- 스팸 방지 정책: 보낸 사람/도메인 허용 목록

## <a name="using-exchange-transport-rules-etrs-to-allow-specific-senders-recommended"></a>ETRs (Exchange 전송 규칙)를 사용 하 여 특정 보낸 사람 허용 (권장)

조직에서 합법적인 메시지만 허용 되도록 하려면 조건이 다음 중 하나 여야 합니다.

- 보내는 도메인의 보낸 사람 인증 상태를 사용 합니다. 이 작업을 수행 하려면 인증-결과 헤더를 확인 하 여 "dmarc = pass" 또는 "dmarc = bestguesspass"가 포함 되어 있는지 확인 합니다. 이렇게 하면 보내는 도메인이 인증 되었으며 위장 되지 않습니다. [SPF](https://docs.microsoft.com/en-us/office365/SecurityCompliance/set-up-spf-in-office-365-to-help-prevent-spoofing), [Dkim](https://docs.microsoft.com/en-us/office365/SecurityCompliance/use-dkim-to-validate-outbound-email)및 [DMARC](https://docs.microsoft.com/en-us/office365/SecurityCompliance/use-dmarc-to-validate-email) 전자 메일 인증에 대 한 자세한 내용을 보려면을 클릭 합니다.

- 또는 보내는 도메인에 인증이 없는 경우 보내는 도메인 *및* 송신 ip (또는 IP 범위)를 사용 합니다. 가능한 한 안전 하 게 작업을 수행 하는 목표를 *최대한 제한적*으로 유지 해야 합니다. /24 보다 큰 IP 범위는 권장 *되지 않습니다* . 소비자 서비스 또는 공유 인프라에 속하는 IP 주소 범위를 추가 하지 않도록 합니다.

> [!IMPORTANT]
> NATted IP 주소를 허용 하는 경우 허용 범위를 파악 하기 위해 해당 NAT 풀에 포함 된 컴퓨터를 알고 있어야 합니다. IP 주소도 변경 될 수 있으며, NAT 참석자도 바뀔 수 있습니다. 표준 유지 관리의 일부로 IP가 허용 되는 모든 목록을 다시 검사 해야 합니다.

- *필요*에 따라 메시지가 조직 외부에서 발생 하는 조건을 추가 합니다 (이는 암시적 이지만 올바르게 구성 되지 않았을 수 있는 온-프레미스 서버를 고려 하는 조건으로 추가 하는 것은 적절 함).

- *필요한*경우 전자 메일 제목 또는 본문에서 고유한 키워드나 구를 확인할 수 있는 경우이 정보를 추가 조건으로 사용 하 여 메일 흐름 규칙에서 허용 하는 전자 메일 메시지를 추가로 제한 합니다.

규칙에 대 한 작업은 다음 패턴을 따라야 합니다.

1. SCL (스팸 지 수)을-1 (스팸 필터링 바이패스)로 설정 합니다.

2. 규칙이 수행 하는 작업을 표시 하는 X-헤더를 추가 합니다. 아래 예제에서는 간단한 헤더 "X-y r: 인증 된 보낸 사람 `contoso.com`에 대 한 스팸 필터링 바이패스"를 추가할 수 있습니다. 이 규칙에 도메인이 두 개 이상 있는 경우 머리글 텍스트를 적절 하 게 변경할 수 있습니다. **ETR로 인 한 메시지에 대 한 필터링을 생략 하면 스팸 방지-Report 헤더의 SFV를 스탬프** 처리 합니다. (**IP 허용 목록에 있는 경우 IPV: CAL에도 스탬프**처리 됩니다. 이는 문제 해결을 지원 합니다.

![스팸 필터링 바이패스 용 GUI](media/1_AllowList_SkipFilteringFromContoso.png)

> [!CAUTION]
> 메일 흐름 규칙을 *보낸 사람 도메인이* 스팸 필터링을 건너뛰도록 하는 조건으로 구성 하지 마십시오. 이 방법을 통해 스팸 발송자가 보내는 도메인을 스푸핑할 수 있는 위험을 대폭 증가 시킵니다 (또는 전체 전자 메일 주소 가장). 모든 스팸 필터링, 보낸 사람 인증 검사를 건너뛰고 메시지가 사용자의 받은 편지함에 도착 합니다.

![SCL을-1로 설정 하는 방법](media/2_AllowList_SetsSCLMinus1.png)

소유한 도메인 또는 인기 있는 도메인 (예: `microsoft.com`)을 메일 흐름 규칙의 조건으로 추가 하지 마십시오. 이는 잘못 된 행위자가 메일을 필터링 할 수 있는 영업 기회를 만들기 때문에 높은 위험으로 간주 됩니다.

[메일 흐름 규칙이 라고도 하는 ETR을 만드는 단계를 클릭](https://docs.microsoft.com/en-us/office365/SecurityCompliance/use-mail-flow-rules-to-set-the-spam-confidence-level-scl-in-messages)합니다.

## <a name="use-outlook-safe-senders-end-user-managed"></a>Outlook 수신 허용-보낸 사람 (최종 사용자 관리) 사용

최종 사용자는 주소, 도메인 또는 IP 주소에 전역적으로 권한을 부여 하는 대신 Outlook 수신 허용-보낸 사람을 통한 주소 보내기를 허용할 수도 있습니다. 이 작업을 설정 하는 단계는 [Outlook Web App](https://support.office.com/en-us/article/block-or-allow-junk-email-settings-48c9f6f7-2309-4f95-9a4d-de987e880e46) 과 [outlook 클라이언트](https://support.office.com/en-us/article/overview-of-the-junk-email-filter-5ae3ea8e-cf41-4fa0-b02a-3b96e21de089)간에 서로 다릅니다. **수신 허용-보낸 사람으로 인해 메시지가 성공적으로 인증 되 면 SFV: 스팸 방지-Report의 SFV에서** 스팸/스푸핑/피싱 필터링이 무시 된다는 것을 표시 합니다.

## <a name="use-anti-spam-policy-ip-allow-lists"></a>스팸 방지 정책 IP 허용 목록 사용

ETRs를 사용 하 여 보낸 사람 인증의 유효성을 검사 하는 동안 특정 보낸 사람에 게 전역적으로 허용 하거나 도메인과 IP를 함께 연결할 수 없는 경우에는 해당 보낸 사람을 *스팸 방지 정책 IP 허용 목록*에 추가 하는 것이 좋습니다. [자세한 단계는 연결 필터 정책 문서 구성에서 찾을 수 있습니다](https://docs.microsoft.com/en-us/office365/securitycompliance/configure-the-connection-filter-policy). 허용 되는 IP 주소 목록을 최소로 유지 하 고 IP 주소 범위를 사용 하지 않는 것이 중요 합니다. 소비자 서비스 또는 공유 인프라에 속하는 IP 주소 범위를 추가 하는 것을 ** 방지 하 고, 허용 되는 ip 주소 목록을 정기적으로 검토 하 고 더 이상 필요 하지 않은 항목을 제거 하는 것이 좋습니다.

> [!CAUTION]
> 보낸 사람 IP 주소만을 기준으로 허용 하도록 스팸 방지 정책을 구성 하면 허용 규칙의 해당 IP 주소에 해당 하는 모든 메시지에 대 한 스팸 필터링이 무시 됩니다. 이렇게 하면 메일을 보내는 불량 행위자가 높은 위험을 초래할 수 있습니다. 또한이 방법은 모든 스팸 필터링, 보낸 사람 인증 확인 및 사용자의 받은 편지함에 있는 메시지를 건너뛰고 위험을 증가 시킵니다.

## <a name="use-anti-spam-policy-senderdomain-allow-lists"></a>스팸 방지 정책 보낸 사람/도메인 허용 목록 사용

가장 바람직한 방법은 보낸 사람/도메인을 통해 권한을 부여 하는 것입니다. 이 옵션은 스팸/스푸핑/피싱 보호를 완전히 건너뛰고, 보낸 사람 인증을 평가 하지 않는 *경우에* 는 피해 야 합니다. 이 방법을 사용할 경우 잘못 된 행위자가 메일을 수신 하는 위험성이 높아지고 테스트할 때에만 일시적으로 권장 됩니다. 자세한 단계는 [스팸 필터 정책 문서 구성](https://docs.microsoft.com/en-us/office365/securitycompliance/configure-your-spam-filter-policies) 에서 찾을 수 있습니다.

> [!CAUTION]
> *보낸 사람/허용 도메인을 허용* 하도록 스팸 방지 정책을 구성 하면 허용 목록의 보낸 사람 또는 b)가 허용 된 도메인의 보낸 사람 으로부터 메시지를 건너뛰는 메시지가 생성 됩니다. 이 방법을 통해 스팸 발송자가 보내는 도메인을 스푸핑할 수 있는 위험을 크게 증가 시키며, 모든 스팸 필터링, 보낸 사람 인증 검사를 건너뛰고 메시지를 사용자의 받은 편지 함으로 직접 전송 하는 전체 전자 메일 주소를 가장 합니다.
> 
> 보유 하 고 있는 도메인 이나 인기 있는 도메인 (예: `microsoft.com`)을 메일 흐름 규칙의 조건으로 추가 하지 마십시오. 이 방법은 잘못 된 행위자가 메일을 보내 위험을 높일 수 있는 기회를 만들기 때문에 높은 위험으로 간주 됩니다.

> [!IMPORTANT]
> **차단 된 보낸 사람 목록을** 만드는 방법에 대 한 정보는 [여기에 나와](create-block-sender-lists-in-office-365.md)있습니다.