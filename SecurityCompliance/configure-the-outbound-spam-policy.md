---
title: Office 365에서 아웃 바운드 스팸 정책 알림 구성
ms.author: tracyp
author: MSFTTracyP
manager: dansimp
ms.date: 11/10/2016
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: a44764e9-a5d2-4c67-8888-e7fb871c17c7
ms.collection:
- M365-security-compliance
description: 관리자는 Office 365에서 아웃 바운드 스팸 감지에 대 한 알림 설정을 수정 하는 방법을 확인할 수 있습니다.
ms.openlocfilehash: c48b6cd634417a00040fb5479313782b44f6aa8d
ms.sourcegitcommit: 81b3bff27bc60235a38004c5b0297ac454331b25
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/10/2019
ms.locfileid: "36822518"
---
# <a name="configure-outbound-spam-policy-notifications-in-office-365"></a>Office 365에서 아웃 바운드 스팸 정책 알림 구성

아웃바운드 전자 메일 보내기 서비스를 사용하는 경우 아웃바운드 스팸 필터링이 항상 사용하도록 설정되므로 서비스와 받는 사람을 사용하여 조직을 보호할 수 있습니다. 인바운드 필터링과 마찬가지로 아웃바운드 스팸 필터링도 연결 필터링과 콘텐츠 필터링으로 구성되지만, 아웃바운드 필터 설정은 구성할 수 없습니다. 스팸으로 확인된 아웃바운드 메시지는 위험성이 높은 배달 풀을 통해 라우팅되므로 일반 아웃바운드 IP 풀이 차단 목록에 추가될 가능성이 줄어듭니다. 서비스를 통해 아웃바운드 스팸을 계속 보내는 고객에 대해서는 메시지 보내기가 차단됩니다.

아웃 바운드 스팸 필터링을 사용 하지 않도록 설정 하거나 변경할 수는 없지만 다음과 같은 아웃 바운드 스팸 알림 설정을 구성할 수도 있습니다.

- **의심 스러운 메시지 복사본 보내기**: 이러한 메시지는 SCL 등급에 관계 없이 스팸으로 표시 되며, 필터에 의해 거부 되지 않으며, 위험성이 높은 배달 풀을 통해 라우팅됩니다. EAC (exchange 관리 센터) 또는 exchange online powershell 또는 exchange online Protection powershell의 ** \*-get-hostedoutboundspamfilterpolicy** cmdlet을 사용 하 여 검색 된 이러한 메시지에 대 한 받는 사람을 추가로 지정할 수 있습니다. 받는 사람이 **숨은 참조** 로 추가 됩니다 (보낸 **사람 및 받는 사람 필드는 원본** 에 **대** 한 sender 및 recipients).

- **보낸 사람이 차단 된 경우 알림 보내기**: 상당한 양의 스팸이 특정 사용자 로부터 들어오는 경우 사용자는 전자 메일 메시지를 보낼 수 없습니다. 기본적으로 관리자에 게 알림이 제공 되지만 Office 365 보안 & 준수 센터에서 **전자 메일을 보내는 사용자 제한** [정책을](alert-policies.md) 사용 하 여 추가 알림 받는 사람을 구성할 수 있습니다.

  이 알림의 모양을 보려면 [보낸 사람이 보내는 아웃 바운드 스팸 차단 되 면 샘플 알림](sample-notification-when-a-sender-is-blocked-sending-outbound-spam.md)을 참조하세요. 다시 사용 하도록 설정 하는 방법에 대 한 자세한 내용은 [스팸 메일을 보낸 후 차단 목록에서 사용자, 도메인 또는 IP 주소 제거](http://technet.microsoft.com/library/712cfcc1-31e8-4e51-8561-b64258a8f1e5.aspx)를 참조 하세요.

## <a name="what-do-you-need-to-know-before-you-begin"></a>시작하기 전에 알아야 할 내용

- 예상 완료 시간: 5분

- 보안 및 준수 센터를 열려면 [Office 365 보안 및 준수 센터로 이동](go-to-the-securitycompliance-center.md)을 참조하세요.

- EAC를 열려면 exchange online 또는 exchange online [Protection](exchange-admin-center-in-exchange-online-protection-eop.md)의 exchange [관리 센터](https://docs.microsoft.com/Exchange/exchange-admin-center) 를 참조 하십시오.

- Exchange Online PowerShell을 열려면 [Exchange Online powershell에 연결](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell)을 참조 하세요. Exchange Online Protection PowerShell을 열려면 [Exchange Online Protection powershell에 연결](https://docs.microsoft.com/powershell/exchange/exchange-eop/exchange-online-protection-powershell)을 참조 하세요.

- 이 절차를 수행 하려면 먼저 계정에 사용 권한을 할당 해야 합니다. 필요한 사용 권한을 확인 하려면 [Office 365 보안 & 준수 센터의 사용 권한](permissions-in-the-security-and-compliance-center.md)에서 "알림 관리" 역할 항목을 참조 하세요.

## <a name="use-the-eac-to-configure-additional-recipients-for-outbound-spam-messages"></a>EAC를 사용 하 여 아웃 바운드 스팸 메시지에 대 한 추가 받는 사람 구성

1. EAC에서 **보호** \> **아웃 바운드 스팸으로**이동 합니다.

2. **Default**라는 정책을 선택 하 고 편집 아이콘](media/ITPro-EAC-EditIcon.png) **편집** ![을 클릭 합니다.

3. 등록 정보 페이지가 열리면 **아웃 바운드 스팸 기본 설정** 탭이 선택 되어 있는지 확인 하 고 다음 설정을 구성 합니다.

   **의심 스러운 모든 아웃 바운드 전자 메일 메시지의 복사본을 다음 전자 메일 주소 또는 주소로 보내기**:이 확인란을 선택 하 고 검색 된 메시지의 **숨은 참조** 필드에 추가 해야 하는 하나 이상의 관리자 전자 메일 주소를 입력 합니다. 세미콜론 (;)을 사용 하 여 여러 전자 메일 주소를 구분 합니다.

   작업을 마친 후 **저장**을 클릭합니다.

### <a name="use-exchange-online-powershell-or-exchange-online-protection-powershell-to-configure-additional-recipients-for-outbound-spam-messages"></a>Exchange Online PowerShell 또는 Exchange Online Protection PowerShell을 사용 하 여 아웃 바운드 스팸 메시지에 대 한 추가 받는 사람 구성

아웃 바운드 스팸 메시지에 대 한 추가 받는 사람을 사용 하도록 설정 하 고 구성 하려면 다음 구문을 사용 합니다.

```PowerShell
Set-HostedOutboundSpamFilterPolicy -Identity Default -BccSuspiciousOutboundMail $true -BccSuspiciousOutboundAdditionalRecipients <recipients>
```

- 기존 값을 모두 덮어쓰는 받는 사람을 지정 하려면 구문을 `emailaddress1,emailaddress2,...emailaddressN`사용 합니다.

- 다른 항목에 영향을 주지 않고 받는 사람을 선택적으로 추가 하거나 제거 `@{Add="\<emailaddress1\>","\<emailaddress2\>"...; Remove="\<emailaddress1\>","\<emailaddress2\>"...}`하려면 구문을 사용 합니다.

이 예에서는 chris@contoso.com, laura@contoso.com 및 julia@contoso.com를 숨은 참조 받는 사람을 아웃 바운드 스팸 메시지에 대해 사용 하도록 설정 하 고 구성 합니다.

```PowerShell
Set-HostedOutboundSpamFilterPolicy -Identity Default -BccSuspiciousOutboundMail $true -BccSuspiciousOutboundAdditionalRecipients chris@contoso.com,laura@contoso.com,julia@contoso.com
```

이 예에서는 michelle@contoso.com를 추가 숨은 참조 받는 사람으로 추가 합니다.

```PowerShell
Set-HostedOutboundSpamFilterPolicy -Identity Default -BccSuspiciousOutboundAdditionalRecipients @{Add=michelle@contoso.com}
```

이 예에서는 숨은 참조 받는 사람 목록에서 chris@contoso.com 및 julia@contoso.com을 제거 합니다.

```PowerShell
Set-HostedOutboundSpamFilterPolicy -Identity Default -BccSuspiciousOutboundAdditionalRecipients @{Remove='chris@contoso.com','julia@contoso.com'}
```

구문 및 매개 변수에 대 한 자세한 내용은 [get-hostedoutboundspamfilterpolicy](https://docs.microsoft.com/powershell/module/exchange/antispam-antimalware/set-hostedoutboundspamfilterpolicy)를 참조 하십시오.

**Note**: 명령을 `Get-HostedOutboundSpamFilterPolicy | Format-List` 실행 하 여 *사람은 bccsuspiciousoutboundmail* 및 *BccSuspiciousOutboundAdditionalRecipients* 속성의 현재 값을 확인 합니다.

## <a name="use-the-security--compliance-center-to-configure-notifications-when-a-sender-is-blocked"></a>보안 & 준수 센터를 사용 하 여 보낸 사람이 차단 된 경우 알림을 구성 합니다.

1. 보안 & 준수 센터에서 **알림** \> **경고 정책**으로 이동 합니다.

2. **사용자가 전자 메일을 보낼 수 없도록 제한**된 정책을 찾아 선택 합니다.

3. 플라이 아웃이 열리면 **정책 편집**을 클릭 합니다.

4. 표시 된 **받는 사람 편집** 페이지에서 다음 설정을 구성 합니다.

   - **전자 메일 알림 보내기** **:가 선택 되어 있는지 확인** 합니다.

   - **전자 메일 받는 사람**: 기본적으로 **tenantadmins** 가 여기에 불과합니다. 받는 사람을 더 추가 하려면이 상자에서 비어 있는 지점을 클릭 하 고 받는 사람 입력을 시작한 다음 이름이 확인 되 면 받는 사람을 선택 합니다. 받는 사람을 제거 하려면 이름 옆에 있는 **X** 를 클릭 합니다.

   - **일별 알림 제한**: 기본값은 **제한이**없지만 1에서 200 사이의 다양 한 제한을 구성할 수 있습니다.

   작업을 마친 후 **저장**을 클릭합니다.

## <a name="for-more-information"></a>자세한 내용

[아웃 바운드 메시지에 대 한 위험성이 높은 배달 풀](high-risk-delivery-pool-for-outbound-messages.md)

[스팸 방지 보호 기능 FAQ](anti-spam-protection-faq.md)
