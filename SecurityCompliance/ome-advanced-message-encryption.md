---
title: Office 365 고급 메시지 암호화
ms.author: krowley
author: kccross
manager: laurawi
ms.audience: Admin
ms.topic: conceptual
ms.service: O365-seccomp
localization_priority: Normal
ms.date: 4/30/2019
ms.collection:
- Strat_O365_IP
- M365-security-compliance
search.appverid:
- MET150
description: Advanced Message Encryption in office 365에서는 조직이 만료 되어 Office 365 웹 포털을 통해 암호화 된 전자 메일에 액세스할 수 있도록 하는 방식으로 관리자의 준수 의무를 충족할 수 있습니다.
ms.openlocfilehash: a775803a8d2678441f319c0145e96e7d19c26f7e
ms.sourcegitcommit: 8eb3cb4ec45ae0bb75fde249e35c4bc3d263b84f
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/30/2019
ms.locfileid: "33506731"
---
# <a name="office-365-advanced-message-encryption"></a>Office 365 고급 메시지 암호화

office 365에서는 특정 구독의 office 365 메시지 암호화 중 위에서 고급 메시지 암호화를 사용할 수 있습니다. 고급 메시지 암호화는 [Microsoft 365 enterprise e5](https://www.microsoft.com/microsoft-365/enterprise/home), Office 365 Enterprise e5 및 Office 365 교육 A5에 포함 되어 있습니다. 조직에 office 365 고급 메시지 암호화를 포함 하지 않는 office 365 구독이 있는 경우 고급 메시지 암호화는 advanced 준수 SKU의 E5 규격을 사용 하 여 추가 기능으로 구입할 수 있습니다.

이 문서는 [Office 365 메시지 암호화](ome.md)에 대 한 보다 광범위 한 문서에 포함 되어 있습니다.

Advanced Message Encryption in Office 365에서는 고객이 외부 받는 사람에 대 한 보다 유연한 제어 및 암호화 된 전자 메일 액세스를 필요로 하는 규정 준수 의무를 충족 하도록 지원 합니다. Office 365의 고급 메시지 암호화를 사용 하 여 조직 외부에서 공유 되는 중요 한 전자 메일을 자동 정책으로 제어할 수 있습니다. 이러한 정책을 구성 하 여 PII, 재무 또는 상태 id와 같은 중요 한 정보 유형을 식별 하거나 키워드를 사용 하 여 보호 기능을 향상 시킬 수 있습니다. 정책을 구성한 후에는 사용자 지정 브랜드 전자 메일 템플릿을 사용 하 여 정책을 제거한 다음 정책에 맞는 전자 메일에 대 한 추가 제어에 대 한 만료 날짜를 추가 합니다. 또한 관리자는 언제 든 지 메일에 대 한 액세스를 취소 하 여 보안 웹 포털을 통해 외부에서 액세스 하는 암호화 된 전자 메일을 제어할 수 있습니다.

외부의 받는 사람에 게 보내는 전자 메일에 대 한 만료만 설정 하 고 해지할 수 있습니다.

office 365 고급 메시지 암호화를 사용 하면 사용자 지정 브랜딩을 적용할 때마다 office 365에서 해당 래퍼를 서식 파일을 적용 하는 메일 흐름 규칙에 맞는 전자 메일에 적용 합니다. 또한 사용자 지정 브랜딩을 사용 하는 경우에만 만료를 사용할 수 있습니다. 포털을 통해 받은 메시지만 해지할 수 있습니다.

## <a name="get-started-with-office-365-advanced-message-encryption"></a>Office 365 Advanced Message Encryption 시작

다음 항목에서는 고급 메시지 암호화를 설정 하 고 사용 하는 방법에 대해 설명 합니다.

조직에 Office 365 고급 메시지 암호화를 포함 하는 구독이 있어야 합니다. 지원 되는 구독에 대 한 자세한 내용은 [메시지 정책 및 규정 준수 서비스 설명을](https://docs.microsoft.com/en-us/office365/servicedescriptions/exchange-online-service-description/message-policy-and-compliance)참조 하세요.

새 Office 365 메시지 암호화 기능이 설정 되어 있지 않은 경우 암호화 된 메시지를 외부에서 공유 하는 고급 메시지 암호화 기능을 활용 하도록 설정 되어 있지 않은 경우 office 365 메시지 암호화를 설정 하지 않은 경우에는 [새 Office 365 메시지 암호화 기능 설정을](set-up-new-message-encryption-capabilities.md)참조 하십시오.

[Office 365 고급 메시지 암호화로 암호화 된 전자 메일의 만료 날짜를 설정](ome-advanced-expiration.md)합니다. 조직 외부에서 공유 되는 중요 한 전자 메일 제어 보안 웹 포털을 통해 암호화 된 전자 메일을 통해 액세스를 만료 하는 자동 정책으로 보호를 강화 합니다.

[Office 365 고급 메시지 암호화로 암호화 된 전자 메일을 해지](revoke-ome-encrypted-mail.md)합니다. 조직 외부에서 공유 되는 중요 한 전자 메일 제어 및 보안 웹 포털을 통한 암호화 된 전자 메일에 대 한 액세스를 해지 하 여 보호 기능 향상  