---
title: Office 365에서 수신 거부 목록 만들기
ms.author: tracyp
author: MSFTTracyP
manager: dansimp
ms.date: 5/6/2019
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150s
description: 보낸 사람 목록 옵션에는 Outlook 수신 거부, 스팸 방지 보낸 사람/도메인 차단 목록, IP 차단 목록 및 ETRs (Exchange 전송 규칙)가 메일 흐름 규칙이 라고도 합니다.
ms.openlocfilehash: 861fa0e47980a6bc295672cf1e8e35954c6f1dfb
ms.sourcegitcommit: 32ecff689ae32c59a39b7633ca0f36a304e7516e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/09/2019
ms.locfileid: "35599994"
---
# <a name="create-block-sender-lists-in-office-365"></a>Office 365에서 수신 거부 목록 만들기

보낸 사람 으로부터 원치 않는 전자 메일을 차단 해야 하는 경우가 있습니다. 선택할 수 있는 몇 가지 방법이 있습니다. 이러한 옵션에는 Outlook 수신 거부, 스팸 방지/도메인 차단 목록, IP 차단 목록 및 Exchange 전송 규칙 (메일 흐름 규칙이 라고도 함)이 있습니다.

> [!NOTE]
> 조직 차단 목록을 사용 하 여 거짓 네거티브 (부재 중 스팸)를 처리할 수 있지만, 이러한 후보자도 분석을 위해 Microsoft에 제출 해야 합니다. 차단 목록을 사용 하 여 거짓 네거티브를 관리 하면 관리 오버 헤드가 크게 증가 합니다. 이 용도로 차단 목록을 사용 하려는 경우에는 준비 상태에서 [스팸, 스팸 아님 및 피싱 사기 메시지를 분석을 위해 Microsoft로 전송](https://docs.microsoft.com/en-us/office365/SecurityCompliance/submit-spam-non-spam-and-phishing-scam-messages-to-microsoft-for-analysis)하기 위한 문서도 유지 해야 합니다.

차단 된 보낸 사람 목록을 구성 하는 적절 한 방법은 영향 범위에 따라 달라 집니다. 단일 사용자에 게 영향을 주는 경우 적절 한 솔루션은 Outlook 차단 된 보낸 사람을 사용할 수 있지만, 여러 사용자나 모든 사용자에 게 영향을 주는 경우 다른 옵션 중 하나를 사용 하는 것이 좋습니다.

## <a name="options-from-least-to-broadest-scope"></a>이상 범위에서 가장 넓은 범위의 옵션

차단 방법 목록을 만들 때는 영향 범위 (영향을 받을 사용자 수)에 따라 적절 한 방법을 선택 하 여 차단 방법의 범위와 일치 하도록 하는 것이 중요 합니다. 아래 나열 된 옵션은 범위와 범위로 모두 순위가 지정 됩니다. 이 목록은 좁은 범위에서 광범위 하 게 제공 ** 되지만, 전체 권장 사항에 대 한 자세한 내용은 여기에서 설명 합니다.

- Outlook 수신 거부
- 스팸 방지 정책: 보낸 사람/도메인 차단 목록
- Exchange 전송 규칙 (메일 흐름 규칙이 라고도 함)
- 스팸 방지 정책: IP 차단 목록

## <a name="use-outlook-blocked-senders"></a>Outlook 수신 거부 사용

소수의 사용자 에게만 영향을 주는 경우 Outlook 차단 된 보낸 사람을 사용 해야 하는 경우에는 메일 전송에만 영향을 줍니다.

> [!IMPORTANT]
> 원치 않는 메시지가 믿을 수 있는 출처의 뉴스레터가 면 전자 메일을 구독 하지 않는 것이 나중에 사용자가 전자 메일을 받지 못하도록 하는 또 다른 옵션입니다.

이 작업을 설정 하는 단계는 [Outlook Web App](https://support.office.com/en-us/article/block-or-allow-junk-email-settings-48c9f6f7-2309-4f95-9a4d-de987e880e46) 과 [outlook 클라이언트](https://support.office.com/en-us/article/overview-of-the-junk-email-filter-5ae3ea8e-cf41-4fa0-b02a-3b96e21de089)간에 다릅니다. **수신 거부로 인해 메시지가 성공적으로 차단 되 면 SFV: BLK에서** 메시지가 차단 중임을 나타내는 스팸 방지가 표시 됩니다.

## <a name="use-anti-spam-policy-senderdomain-block-lists"></a>스팸 방지 정책 보낸 사람/도메인 차단 목록 사용

여러 사용자에 게 영향을 주는 경우 범위가 더 넓고 회사 전체의 보낸 사람/도메인 차단 목록 스팸 방지 정책을 사용 해야 합니다. 자세한 단계는 [스팸 필터 정책 문서 구성](https://docs.microsoft.com/en-us/office365/securitycompliance/configure-your-spam-filter-policies) 에서 찾을 수 있습니다. 이 방법을 통해 차단 된 모든 메시지는 정책에 구성 된 대로 스팸 작업을 따릅니다.

이러한 목록의 최대 제한은 약 1000 엔트리입니다.

## <a name="use-exchange-transport-rules-etrs-to-block-specific-senders"></a>ETRs (Exchange 전송 규칙)를 사용 하 여 특정 보낸 사람 차단

특정 사용자에 게 또는 전체 조직에서 메시지를 차단 해야 하는 경우에는 메일 흐름 규칙이 라고도 하는 ETRs를 사용할 수 있습니다. ETRs는 보낸 사람 전자 메일 주소 또는 도메인을 비롯 하 여 메시지의 주요 단어 및 기타 속성을 트리거할 수 있기 때문에 유연성이 뛰어납니다. 이러한 유연성을 통해 부분-전체 블록을 만들 수 있습니다. [메일 흐름 규칙이 라고도 하는 ETR을 만드는 단계를 클릭](https://docs.microsoft.com/en-us/office365/SecurityCompliance/use-mail-flow-rules-to-set-the-spam-confidence-level-scl-in-messages)합니다.

> [!IMPORTANT]
> 매우 적극적인 규칙을 쉽게 만들 수 있으며 ** , 따라서 사용 되는 기준이 가능한 한 구체적이 되는 것이 중요 합니다. 또한 만드는 규칙에 대 한 감사를 사용 하도록 설정 하 고 테스트를 수행 하 여 모든 항목이 예상 대로 작동 하는지 확인 해야 합니다.

## <a name="use-anti-spam-policy-ip-block-lists"></a>스팸 방지 정책 IP 차단 목록 사용

다른 옵션 중 하나를 사용 하 여 보낸 사람을 차단할 수 없는 경우 스팸 방지 ** 정책 IP 차단 목록을 사용할 수 있습니다. [자세한 단계는 Configure the connection filter policy 문서에 나와 있습니다](https://docs.microsoft.com/en-us/office365/securitycompliance/configure-the-connection-filter-policy). 차단 된 Ip 목록을 *최소로* 유지 하 고 IP 주소 범위를 사용 하는 것이 좋습니다. **

*특히* 소비자 서비스 또는 공유 인프라에 속하는 ip 주소 범위를 추가 하는 것을 피하고, 일반 유지 관리의 일부로 허용 되는 ip 주소 목록을 검토 하는 것이 좋습니다. **허용-항목은 공격할 경로를 열 수 있으므로이 목록을 면밀 하 게 관리 하 고 더 이상 필요 하지 않은 허용 항목을 정기적으로 제거 해야 합니다.** 또한 안전한 보낸 사람 목록에서 허용 되는 경우에는 *[Office 365에서 수신 허용-보낸 사람 목록 만들기](create-safe-sender-lists-in-office-365.md)* 의 위험과 주의 사항을 읽고 이해 해야 합니다.
