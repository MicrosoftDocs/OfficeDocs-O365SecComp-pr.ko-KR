---
title: 제로 아워 자동 비우기 - 스팸 및 맬웨어로부터 보호
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 12/05/2018
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MED150
- MBS150
- MET150
ms.assetid: 96deb75f-64e8-4c10-b570-84c99c674e15
description: 0-시간 자동 삭제 (ZAP) 스팸 또는 맬웨어로와 사용자의 받은 편지함에 이미 배달 된 메시지를 검색 하는 전자 메일 보호 기능 및 다음 치명적이 지 악의적인 콘텐츠를 렌더링 합니다. 어떻게 ZAP이 작업을 수행 하는 작업은 감지 악의적인 콘텐츠 형식에 따라 다릅니다.
ms.openlocfilehash: 1e90e69018b7640bb36011287abd5bcd77d43358
ms.sourcegitcommit: 30faa3ba91cab4c36e3d8d8ed5858d5269ea8a56
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/08/2019
ms.locfileid: "27749322"
---
# <a name="zero-hour-auto-purge---protection-against-spam-and-malware"></a>제로 아워 자동 비우기 - 스팸 및 맬웨어로부터 보호

## <a name="overview"></a>개요

0-시간 자동 삭제 (ZAP) phish, 스팸, 또는 맬웨어 사용자의 받은 편지함에 이미 배달 된 메시지를 검색 하는 전자 메일 보호 기능 및 다음 치명적이 지 악의적인 콘텐츠를 렌더링 합니다. 검색; 악의적인 콘텐츠 형식에 따라 달라 집니다 어떻게 ZAP이 작업을 수행합니다 메일 메일 콘텐츠, Url 또는 첨부 파일으로 인해 zapped 될 수 있습니다.
  
ZAP은 Exchange Online 사서함이 포함 된 모든 Office 365 구독의 함께 제공 되는 Exchange Online Protection 기본 제공 됩니다.

기본적으로 ZAP 켜져 있지만 다음과 같은 조건이 충족 되어야 합니다.
  
- **스팸 동작** 는 **정크 메일 폴더로 메시지 이동**으로 설정 됩니다. <br/>모든 사서함 ZAP으로 검사 하지 않으려면 사용자 집합에만 적용 되는 스팸 필터 정책을 새로 만들 수도 있습니다.

- 사용자가 유지가 기본 정크 메일 설정 하 고 정크 메일 보호를 해제 하지 않은. (Outlook에서 사용자 옵션에 대 한 자세한 내용은 [정크 메일 필터의 보호 기능 수준을 변경](https://support.office.com/article/change-the-level-of-protection-in-the-junk-email-filter-e89c12d8-9d61-4320-8c57-d982c8d52f6b) 을 참조 하십시오.) 
  
## <a name="how-does-zap-work"></a>ZAP는 어떻게 작동 합니까?

Office 365에서 스팸 방지 엔진 및 맬웨어 서명 업데이트를 매일 실시간 합니다. 그러나 사용자에 게 다양 한 콘텐츠를 사용자에 게 배달 되지 후 weaponized 하는 경우를 포함 하 여 이유 때문에 대 한 받은 편지함에 배달 된 악의적인 메시지를 계속 가져올 수 있습니다. ZAP 계속 해 서 Office 365 스팸 및 맬웨어로부터 서명에 대 한 업데이트를 모니터링 하 여이 해결 합니다. ZAP 검색 하 고 사용자의 받은 편지함에 이미 있는 이전에 배달 된 메시지를 제거할 수 있습니다. 

- 스팸으로 식별 되는 메일에 대 한 ZAP 읽지 않은 메시지를 사용자의 정크 메일 폴더로 이동 합니다. 

- ZAP는 스팸으로 식별 되는 메일에 대 한 전자 메일을 읽은 여부에 관계 없이 사용자의 정크 메일 폴더로 메시지 이동 합니다.

- 새로 검색 된 맬웨어 ZAP는 전자 메일을 읽은 여부에 관계 없이 전자 메일 메시지에서 첨부 파일을 제거 합니다. 
  
ZAP 매크로 함수는 사서함 사용자; 원활 하 게 전자 메일 메시지를 이동 하는 경우에 이러한는 알림을 받지 않습니다.
  
목록, [메일 흐름 규칙](https://go.microsoft.com/fwlink/p/?LinkId=722755)및 최종 사용자 규칙을 허용 또는 추가 필터를 ZAP 보다 우선 합니다.
  
## <a name="to-review-or-set-up-a-spam-filter-policy"></a>검토 하거나 스팸 필터 정책을 설정 하려면
  
1. 이동 [https://protection.office.com](https://protection.office.com) 및 Office 365에 대 한 작업이 나 교육용 계정을 사용 하 여 로그인 합니다.

2. **위협 관리** **스팸 방지**를 선택 합니다.

3. 표준 설정을 검토 합니다. 

4. 설정을 사용자 지정 하려는 경우 **사용자 지정** 탭을 선택 하 고 **사용자 지정 설정**사용 합니다. 설정을 편집 하 고 원할 경우 **+ 정책 만들기** 새 정책을 추가 하려면 선택 합니다. 
    
## <a name="to-see-if-zap-moved-your-message"></a>ZAP 메시지를 이동 하는 경우를 확인 하려면

ZAP 메시지를 이동 하는 경우 확인 하려는 경우에 또는 중 하나는 [위협 보호 상태 보고서](view-email-security-reports.md#threat-protection-status-report) ( [위협 탐색기](use-explorer-in-security-and-compliance.md))를 사용할 수 있습니다.
    
## <a name="to-disable-zap"></a>ZAP를 사용 하지 않도록 설정 하려면
  
사용 하지 않도록 설정 하려는 경우 Office 365 테 넌 트에 대 한 ZAP 또는 사용자 집합을 [Set-hostedcontentfilterpolicy](https://go.microsoft.com/fwlink/p/?LinkId=722758), EOP cmdlet의 **ZapEnabled** 매개 변수를 사용 합니다.
    
다음 예제에서는 ZAP은 "Test" 라는 콘텐츠 필터 정책에 대해 사용할 수 없습니다.
    
```
  Set-HostedContentFilterPolicy -Identity Test -ZapEnabled $false
```

## <a name="faq"></a>FAQ

### <a name="what-happens-if-a-legitimate-message-is-moved-to-the-junk-mail-folder"></a>합법적인 메시지는 정크 메일 폴더로 이동 하는 경우 어떻게 됩니까?
  
False 양수에 대 한 일반 보고 프로세스를 따라야 합니다. 정크 메일 폴더로 메시지를 받은 편지함에서 이동할 수는 유일한 이유는 서비스에서 메시지 스팸 했음을 확인가 때문에 것 또는 악의적 합니다.
  
### <a name="what-if-i-use-the-office-365-quarantine-instead-of-the-junk-mail-folder"></a>경우에 어떻게 정크 메일 폴더 대신 Office 365 격리를 사용 합니까?
  
ZAP 지금은 메시지를 격리에 받은 편지함에서 이동 하지 않습니다.
  
### <a name="what-if-i-have-a-custom-mail-flow-rule-block-allow-rule"></a>사용자 지정 메일 흐름 규칙을 경우에 어떻게 해야 합니까 (차단 / 허용 규칙)?
  
관리자 (메일 흐름 규칙) 또는 허용 및 차단 규칙에서 만든 규칙이 우선 합니다. 이러한 메시지 기능 조건에서 제외 됩니다.
  
## <a name="related-topics"></a>관련 항목

[Office 365 전자 메일 스팸 방지 보호](anti-spam-protection.md)
  
[Office 365 스팸 필터로 전자 메일 스팸을 차단하여 거짓 부정 문제 방지](block-email-spam-to-prevent-false-negatives.md)
  

