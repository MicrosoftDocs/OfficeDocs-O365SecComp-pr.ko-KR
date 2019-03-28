---
title: Office 365에서 피싱 방지 보호 기능 조정
ms.author: chrisda
author: chrisda
manager: serdars
ms.date: ''
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
description: 관리자는 피싱 메시지의 원인과 방법을 파악 하 고, 향후 피싱 메시지를 더 많이 차단 하기 위해 수행 해야 하는 작업에 대해 알아볼 수 있습니다.
ms.openlocfilehash: efda9e16c23e4533b6951e43ac085b7640e84576
ms.sourcegitcommit: 8a65a29aa3bfe5dcad0ff152a7cd795e02877dd9
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/28/2019
ms.locfileid: "30937828"
---
# <a name="tune-anti-phishing-protection-in-office-365"></a>Office 365에서 피싱 방지 보호 기능 조정

Office 365에는 기본적으로 사용 하도록 설정 되는 다양 한 피싱 방지 기능이 있지만 일부 피싱 메시지가 여전히 사서함으로 이동할 수 있습니다. 이 항목에서는 피싱 메시지가 발생 한 이유를 파악 하기 위해 수행할 수 있는 작업과 _실수로 작업을 더 어렵게 만들지 않고_Exchange Online 조직에서 피싱 방지 설정을 조정 하기 위해 수행할 수 있는 작업에 대해 설명 합니다.

## <a name="first-things-first-deal-with-any-compromised-accounts-and-make-sure-you-block-any-more-phishing-messages-from-getting-through"></a>첫 번째 작업: 손상 된 계정을 처리 하 고 더 이상 피싱 메시지를 수신 하지 못하도록 차단 합니다.

피싱 메시지의 결과로 받는 사람의 계정이 손상 된 경우 [Office 365에서 손상 된 전자 메일 계정에 응답 하](responding-to-a-compromised-email-account.md)는 단계를 따르세요.

구독에 ATP (Advanced Threat Protection)가 포함 되어 있으면 [Office 365 위협 인텔리전스](office-365-ti.md) 를 사용 하 여 피싱 메시지도 받은 다른 사용자를 식별할 수 있습니다. 피싱 메시지를 차단 하는 추가 옵션은 다음과 같습니다.

- [ATP 안전한 링크](set-up-atp-safe-links-policies.md)

- [ATP 안전한 첨부 파일](set-up-atp-safe-attachments-policies.md)

- [ATP 피싱 방지 정책](set-up-anti-phishing-policies.md) 정책의 **고급 피싱 임계값** 을 **표준** 에서 일시적으로, 적극적으로 또는 **적극적인**로 높일 **** 수 있습니다 ****.

ATP 기능이 설정 되어 있는지 확인 합니다.

## <a name="report-the-phishing-message-to-microsoft"></a>Microsoft에 피싱 메시지 보고

보고 피싱 메시지는 Office 365의 모든 고객을 보호 하는 데 사용 되는 필터를 조정할 때 유용 합니다.

피싱 메시지를 새 메시지의 _첨부_ 파일로 전송 하 고 비어 있지 않으면 **phish@office365.microsoft.com**. 원본 메시지를 전달 하는 것이 아니라 그렇지 않은 경우에는 원본 메시지 헤더를 확인할 수 없습니다. 또는 outlook 또는 웹용 outlook (이전의 outlook web App)에서 [보고서 메시지](https://docs.microsoft.com/office365/securitycompliance/enable-the-report-message-add-in) 추가 기능을 사용할 수 있습니다.

자세한 내용은 [분석을 위해 Microsoft에 스팸 및 스팸이 아닌 메시지 제출을](submit-spam-non-spam-and-phishing-scam-messages-to-microsoft-for-analysis.md)참조 하세요.

## <a name="inspect-the-message-headers"></a>메시지 헤더를 검사 합니다.

피싱 메시지의 헤더를 검사 하 여 더 많은 피싱 메시지를 통해 들어오는 것을 방지 하기 위해 수행할 수 있는 작업이 있는지 확인할 수 있습니다. 즉 메시지 헤더를 검사 하면에서 피싱 메시지를 허용 하는 일을 담당 하는 조직의 설정을 식별 하는 데 도움이 될 수 있습니다.

특히 sfv (스팸 필터링 결과) 값에서 건너뛴 스팸 또는 피싱 필터링이 표시 되는 메시지 헤더에서 **스팸 방지-Report** 헤더 필드를 확인 해야 합니다. 필터링을 건너뛰지 않는 메시지에는 항목이 있는데 `SCL:-1`,이는 설정 중 하나에서 서비스에 의해 결정 된 스팸 또는 피싱 verdicts를 재정의 하 여이 메시지를 허용 한다는 것을 의미 합니다. 사용 가능한 모든 스팸 방지 및 피싱 메시지 헤더의 전체 목록과 메시지 헤더를 가져오는 방법에 대 한 자세한 내용은 [스팸 방지 메시지 헤더](https://docs.microsoft.com/office365/SecurityCompliance/anti-spam-message-headers)를 참조 하십시오.

## <a name="best-practices-to-stay-protected"></a>보호를 유지 하기 위한 모범 사례

- 매달 office [365 보안 점수](office-365-secure-score.md) 를 실행 하 여 office 365 조직의 보안 설정을 평가 합니다.

- 피싱 사기 [보고서](learn-about-spoof-intelligence.md) 를 주기적으로 검토 하 고 [위조 방지 정책에서 스푸핑 방지 보호](learn-about-spoof-intelligence.md#configuring-the-anti-spoofing-policy) 기능을 사용 하 여 의심 스러운 메시지를 사용자의 정크 메일 폴더로 배달 하는 대신 **격리** 합니다.

- [위협 방지 상태 보고서](view-reports-for-atp.md#threat-protection-status-report)를 주기적으로 검토 합니다.

- 일부 고객은 스팸 방지 정책의 보낸 사람 허용 또는 허용 도메인 목록에 자신의 도메인을 추가 하 여 피싱 메시지를 통과 하도록 할 수 있습니다. 이 작업을 선택 하는 경우에는 매우 주의 해야 합니다. 이 구성에서는 일부 합법적인 메시지를 허용 하지만, 일반적으로 Office 365 스팸 및/또는 피싱 필터에 의해 차단 되는 악성 메시지도 허용 됩니다.

  도메인의 보낸 사람과 관련 하 여 office 365 (가양성)에 의해 차단 되는 합법적인 메시지를 처리 하는 가장 좋은 방법은 office 365에서 _모든_ 전자 메일 도메인에 대해 DNS의 SPF, dkim 및 DMARC 레코드를 완전 하 고 완전 하 게 구성 하는 것입니다.

  - SPF 레코드에 도메인의 보낸 사람에 대 한 _모든_ 전자 메일 원본이 식별 되는지 확인 합니다 (타사 서비스를 잊지 마십시오.).

  - 권한 없는 보낸 사람이\-이를 수행 하도록 구성 된 전자 메일 시스템에 의해 거부 되도록 하려면 hard fail ()을 사용 합니다. [스푸핑 인텔리전스](https://docs.microsoft.com/office365/securitycompliance/learn-about-spoof-intelligence) 를 사용 하면 SPF 레코드에 권한이 부여 된 타사 보낸 사람을 포함할 수 있도록 도메인을 사용 중인 보낸 사람을 식별 하는 데 도움이 됩니다.

  구성 지침에 대해서는 다음을 참조 하세요.
  
  - [스푸핑을 방지할 수 있도록 Office 365에서 SPF 설정](set-up-spf-in-office-365-to-help-prevent-spoofing.md)

  - [dkim을 사용 하 여 Office 365의 사용자 지정 도메인에서 전송 되는 아웃 바운드 전자 메일의 유효성 검사](use-dkim-to-validate-outbound-email.md)

  - [DMARC을 사용 하 여 Office 365의 전자 메일 유효성 검사](use-dmarc-to-validate-email.md)

- 가능한 경우에는 항상 도메인에 대 한 전자 메일을 Office 365에 직접 배달 하는 것이 좋습니다. 즉, office 365 도메인의 MX 레코드를 office 365에 가리키도록 합니다. EOP (Exchange Online Protection)은 메일이 Office 365로 직접 배달 될 때 클라우드 사용자에 게 최상의 보호를 제공할 수 있습니다. EOP 앞에 타사 전자 메일 바이러스 예방 시스템을 사용 해야 하는 경우 [여기](https://docs.microsoft.com/exchange/mail-flow-best-practices/manage-mail-flow-using-third-party-cloud)에서 지침을 따랐는지 확인 합니다.

- MFA (multi-factor authentication)는 손상 된 계정을 방지 하는 매우 좋은 방법입니다. 모든 사용자에 대해 MFA를 사용 하도록 설정 하는 것이 좋습니다. 단계적 접근 방식에서는 모든 사용자에 대해 mfa를 사용 하도록 설정 하기 전에 가장 중요 한 사용자 (관리자, 임원 등)에 대해 mfa를 사용 하도록 설정 하는 것부터 시작 합니다. 자세한 내용은 [다단계 인증 설정을](https://docs.microsoft.com/office365/admin/security-and-compliance/set-up-multi-factor-authentication)참조 하십시오.

- 외부 받는 사람에 게 규칙을 전달 하는 경우 공격자가 데이터를 추출 하는 경우가 많습니다. [Office 365 보안 점수](office-365-secure-score.md) 에 있는 **사서함 전달 규칙 검토** 정보를 사용 하 여 외부의 받는 사람에 게 전달 규칙을 찾고이를 방지할 수도 있습니다. 자세한 내용은 [보안 점수를 사용한 클라이언트 외부 전달 규칙 완화](https://blogs.technet.microsoft.com/office365security/mitigating-client-external-forwarding-rules-with-secure-score/)를 참조 하세요.
