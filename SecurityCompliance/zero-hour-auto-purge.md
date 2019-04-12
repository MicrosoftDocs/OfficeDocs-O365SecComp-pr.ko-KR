---
title: 제로 아워 자동 비우기 - 스팸 및 맬웨어로부터 보호
ms.author: tracyp
author: MSFTTracyP
manager: laurawi
ms.date: 04/11/2019
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MOE150
- MED150
- MBS150
- MET150
ms.assetid: 96deb75f-64e8-4c10-b570-84c99c674e15
ms.collection:
- M365-security-compliance
description: ZAP (자동 삭제)은 사용자의 받은 편지 함으로 이미 배달 된 스팸 또는 맬웨어가 있는 메시지를 검색 한 다음 악의적인 콘텐츠를 렌더링 하는 전자 메일 보호 기능입니다. ZAP이 수행 하는 방법은 검색 된 악의적인 콘텐츠의 유형에 따라 다릅니다.
ms.openlocfilehash: 507cd6af5320a3b925841786136d518c996e4d29
ms.sourcegitcommit: 86ff2eba1d57b9d5288840788529e69ad9d836b6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/11/2019
ms.locfileid: "31818605"
---
# <a name="zero-hour-auto-purge---protection-against-spam-and-malware"></a>제로 아워 자동 비우기 - 스팸 및 맬웨어로부터 보호

## <a name="overview"></a>개요

ZAP (자동 삭제)은 사용자의 받은 편지 함으로 이미 배달 된 피싱, 스팸 또는 맬웨어가 있는 메시지를 검색 한 다음 악성 콘텐츠 무해 함을 렌더링 하는 전자 메일 보호 기능입니다. ZAP이 수행 하는 방법은 검색 된 악의적인 콘텐츠의 유형에 따라 다릅니다. 메일은 mail content, url 또는 attachments로 인해 zapped 될 수 있습니다.
  
ZAP은 exchange online 사서함이 포함 된 모든 Office 365 구독에 포함 된 기본 exchange online Protection에서 사용할 수 있습니다.

ZAP은 기본적으로 설정 되어 있지만 다음 조건을 충족 해야 합니다.
  
- **스팸 작업** 은 **정크 메일 폴더로 메시지를 이동**하도록 설정 됩니다. 또한 모든 사서함을 ZAP에 게 표시 하지 않으려는 경우 사용자 집합에만 적용 되는 새 스팸 필터 정책을 만들 수 있습니다.

- 사용자가 기본 정크 메일 설정을 유지 했으며 정크 메일 보호를 해제 하지 않았습니다. (Outlook의 사용자 옵션에 대 한 자세한 내용은 [정크 메일 필터의 보호 수준 변경을](https://support.office.com/article/change-the-level-of-protection-in-the-junk-email-filter-e89c12d8-9d61-4320-8c57-d982c8d52f6b) 참조 하세요.) 
  
## <a name="how-zap-works"></a>ZAP 작동 방식

Office 365에서는 매일 실시간으로 스팸 방지 엔진 및 맬웨어 서명을 업데이트 합니다. 그러나 사용자에 게 콘텐츠를 배달 한 후에 weaponized를 포함 하 여 여러 가지 이유로 인해 사용자가 여전히 해당 받은 편지함에 악성 메시지를 배달 하도록 할 수 있습니다. ZAP은 Office 365 스팸 및 맬웨어 서명에 대 한 업데이트를 지속적으로 모니터링 하 여이를 해결 합니다. ZAP은 이전에 전달한 메시지 중 사용자의 받은 편지함에 이미 배달 된 메시지가 있는지 찾아 제거할 수 있습니다.

- 스팸으로 식별 된 메일의 경우, ZAP은 읽지 않은 메시지를 사용자의 정크 메일 폴더로 이동 합니다.

- 피싱으로 식별 되는 메일의 경우 ZAP은 전자 메일을 읽은 적이 있는지 여부에 관계 없이 메시지를 사용자의 정크 메일 폴더로 이동 합니다.

- 새로 검색 된 맬웨어의 경우 ZAP은 전자 메일을 읽은 적이 있는지 여부에 관계 없이 전자 메일 메시지에서 첨부 파일을 제거 합니다.
  
사서함 사용자에 게는 ZAP 동작이 원활 하 게 수행 됩니다. 전자 메일 메시지를 이동 하는 경우이 사용자에 게 알림이 제공 되지 않습니다. 메시지가 2 일 보다 오래 된 것은 아니어야 합니다.
  
허용 목록, [메일 흐름 규칙](https://go.microsoft.com/fwlink/p/?LinkId=722755), 최종 사용자 규칙 또는 추가 필터는 ZAP 보다 우선 합니다.
  
## <a name="to-review-or-set-up-a-spam-filter-policy"></a>스팸 필터 정책을 검토 하거나 설정 하려면
  
1. [https://protection.office.com](https://protection.office.com) 으로 이동 하 여 Office 365에 대 한 회사 또는 학교 계정을 사용 하 여 로그인 합니다.

2. **위협 관리**에서 **스팸 방지**를 선택 합니다.

3. 표준 설정을 검토 합니다.

4. 설정을 사용자 지정 하려면 **사용자 지정** 탭을 선택 하 고 **사용자 지정 설정을**사용 하도록 설정 합니다. 설정을 편집 하 고, 원하는 경우 **+ 정책 만들기** 를 선택 하 여 새 정책을 추가 합니다.

## <a name="to-see-if-zap-moved-your-message"></a>메시지가 ZAP에서 이동 된 것을 확인 하려면

ZAP에서 메시지를 이동 했는지 확인 하려면 [위협 방지 상태 보고서](view-email-security-reports.md#threat-protection-status-report) ( [위협 탐색기](use-explorer-in-security-and-compliance.md))를 사용 합니다.

## <a name="to-disable-zap"></a>ZAP을 사용 하지 않도록 설정 하려면
  
Office 365 테 넌 트 또는 사용자 집합에 대해 ZAP을 사용 하지 않도록 설정 하려는 경우 EOP cmdlet의 **ZapEnabled** 매개 [](https://go.microsoft.com/fwlink/p/?LinkId=722758)변수를 사용 합니다.

다음 예제에서는 "Test" 라는 콘텐츠 필터 정책에 대해 ZAP을 사용할 수 없습니다.

```Powershell
  Set-HostedContentFilterPolicy -Identity Test -ZapEnabled $false
```

## <a name="faq"></a>FAQ

### <a name="what-happens-if-a-legitimate-message-is-moved-to-the-junk-mail-folder"></a>합법적인 메시지를 정크 메일 폴더로 이동 하면 어떻게 되나요?
  
[가양성](prevent-email-from-being-marked-as-spam.md)에 대 한 일반 보고 프로세스를 따라야 합니다. 메시지를 받은 편지함에서 정크 메일 폴더로 이동 하는 유일한 이유는 서비스가 스팸 또는 악성 메시지를 받는 것으로 확인 되었기 때문입니다.
  
### <a name="what-if-i-use-the-office-365-quarantine-instead-of-the-junk-mail-folder"></a>정크 메일 폴더 대신 Office 365 검역을 사용 하는 경우에는 어떻게 하나요?
  
지금은 메시지를 받은 편지함에서 격리로 이동 하지 않습니다.
  
### <a name="what-if-i-have-a-custom-mail-flow-rule-block-allow-rule"></a>사용자 지정 메일 흐름 규칙 (차단/허용 규칙)이 있는 경우 어떻게 하나요?
  
관리자가 만든 규칙 (메일 흐름 규칙) 또는 차단 및 허용 규칙을 우선적으로 사용 합니다. 이러한 메시지는 기능 조건에서 제외 되므로 메일 흐름은 규칙 동작 (차단/허용 규칙)을 따릅니다.

### <a name="what-if-a-message-is-moved-to-another-folder-eg-inbox-rule"></a>다른 폴더 (예: 받은 편지함 규칙)로 메시지를 이동 하는 경우
메시지가 삭제 되었거나 정크 상태인 경우가 아니면이 경우에도 ZAP이 작동 합니다.

## <a name="related-topics"></a>관련 항목

[Office 365 전자 메일 스팸 방지 보호](anti-spam-protection.md)
  
[Office 365 스팸 필터로 전자 메일 스팸을 차단하여 거짓 부정 문제 방지](reduce-spam-email.md)
