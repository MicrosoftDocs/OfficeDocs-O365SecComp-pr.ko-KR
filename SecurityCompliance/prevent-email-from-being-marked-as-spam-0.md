---
title: Office 365 및 Exchange Online Protection의 스팸으로 표시 되 고에서 전자 메일을 방지
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 6/29/2018
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: 74aaade0-efc0-46ac-b949-f2d1d59256fa
description: 좋은 전자 메일을 방지 하기 위해 Office 365 관리자를 위한 팁 가양성으로 격리로 전송 되지 않도록 스팸으로 표시 합니다. 수신 허용 목록 및 스팸으로 표시 하는 효율적인 전자 메일을 방지 하기 위해 다른 옵션을 사용자 지정 합니다.
ms.openlocfilehash: 42b27d237592e95e6d175ab335959bc82269c0f7
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22532984"
---
# <a name="prevent-email-from-being-marked-as-spam-in-office-365-and-exchange-online-protection"></a>Office 365 및 Exchange Online Protection의 스팸으로 표시 되 고에서 전자 메일을 방지

적절 한 액세스 자격 증명을 사용 Exchange Online 또는 Exchange Online Protection (EOP) 관리자는 다음이 단계를 사용 하 여 서비스를 통해 이동 하는 전자 메일 메시지를 스팸으로 표시 되지 않습니다을 보장 하기 수 있습니다.
  
스팸 및 격리 폴더에 방문 차단 또는 격리 된 합법적인, 좋은 전자 메일을 실망 수 있습니다. 스팸 필터링 무시 하 고 효율적인 전자 메일 메시지를 정크 메일에 대해 된 것으로 표시 하지 못하도록 하는 수신 허용-보낸사람 목록이 나 메일 흐름 규칙을 사용할 수 있습니다. 메시지가 잘못 표시 되어 스팸이 스팸 필터에 의해, 때는 가양성을 이라고 합니다. Office 365 스팸 필터는 또한 가양성을 방지 하기 위해 최종 사용자를 사용자 지정할 수 있는 일부 옵션을 제공 합니다.
  
False 이면 음수 메일에 대 한 도움을 찾는 경우, 즉 스팸 메시지는 하지만 통해 팁 [false 이면 음수 문제를 방지 하기 위해 Office 365 스팸 필터와 함께 스팸 블록 전자 메일](block-email-spam-to-prevent-false-negatives.md)에 체크아웃 하지 말아야 합니다 됩니다.
  
## <a name="eop-only-customers-use-directory-synchronization"></a>EOP 전용 고객: 디렉터리 동기화를 사용 하 여

EOP은 클라우드 기반 전자 메일 스팸 및 맬웨어로부터 조직을 보호 하는 데 도움이 되는 서비스를 필터링 합니다. Office 365에서 사서함을 설치한 경우 자동으로 보호 EOP 서비스의 일부에 있기 때문입니다. 
  
즉, EOP 전용 고객, 인 경우 온-프레미스 Exchange 서버와 사용 하기 위해 EOP 서비스에 가입, 디렉터리 동기화를 사용 하 여 서비스를 사용 하 여 사용자 설정을 동기화 해야 합니다. 이렇게 하면 사용자 수신 허용-보낸사람 목록 EOP에 의해 사용 됩니다. 자세한 내용은 [EOP의 메일 사용자 관리](https://go.microsoft.com/fwlink/?LinkId=534098)에 "메일 사용자 관리를 사용 하 여 디렉터리 동기화를"를 참조 하십시오.
  
## <a name="prevent-false-positive-email-by-using-the-connection-filters-ip-allow-list"></a>False 이면 양의 전자 메일을 방지 연결을 사용 하 여 필터의 IP 허용 목록

보낸 사람의 전자 메일 조직에서 정크 폴더에 항상 이동, 연결 필터의 IP에 게 전자 메일 보낸 사람의 IP 주소를 추가할 수 있는지를 확인 하는 경우에 허용 목록입니다. 일반적으로 조직 내의 모든 받는 사람에 게이 보낸사람에 대 한 false 양의 응답 수 없습니다. 사용자는 옵션을 사용 하는 경우는 예외입니다 "안전 하 게 보호만 나열: 사람이 나 수신 허용-보낸사람 목록이 나 수신 허용-받는 사람 목록에 있는 도메인의 메일만 받은 편지 함으로 배달 됩니다" Outlook의 수신 허용-보낸사람 목록에 해당 보낸사람을 추가 하지 않습니다. 해당 옵션을 재정의에 대 한 정보를 참조 하십시오. [문제해결: 메시지를 완성 정크 폴더에 EOP 스팸이 아닌 메시지를 표시 하는 경우에](prevent-email-from-being-marked-as-spam-0.md#TroubleshootingJunkEOPNonSpam)합니다.
  
 **필터의 IP 허용 목록에 대 한 연결을 IP 주소를 추가 하려면**
  
1. 허용 하려는 보낸 사람이 보낸 메시지에서 헤더를 가져옵니다. [메시지 헤더 분석기](https://go.microsoft.com/fwlink/p/?LinkId=306583)의 설명에 따라 Outlook 또는 Outlook은 웹에서 같은 메일 클라이언트에서이 수행할 수 있습니다.
    
2. CIP 태그 X Forefront-스팸 방지 보고서 머리글에 또는 [원격 연결 분석기](https://testconnectivity.microsoft.com/?tabid=mha)의 **메시지 분석기** 탭을 사용 하 여 다음 IP 주소에 대 한 직접 검색 합니다.
    
3. 추가 IP 주소를 ip 허용 목록 "기본 연결 필터 정책을 편집 하려면 EAC 사용"의 단계를 수행 하 여 [연결 필터 정책 구성](https://go.microsoft.com/fwlink/?LinkId=534132)에 있습니다.
    
## <a name="prevent-false-positive-email-by-configuring-spam-filter-policies"></a>스팸 필터 정책을 구성 하 여 false 양의 전자 메일을 방지

[스팸 필터 정책 구성](https://go.microsoft.com/fwlink/?LinkID=534136)의 단계를 수행 하 여 도메인 또는 개별 전자 메일 주소는 허용 목록에 추가할 수 있습니다.
  
## <a name="review-your-advanced-spam-filter-policies"></a>고급 스팸 필터 정책에 검토

전체 도메인 차단한 경우 스팸 필터 정책 등을 설정 하는 특별 한 제한 경우 하는 경우 이러한를 일으킬 수 가양성을 확인 하 게 검토 해야 합니다. [스팸 필터 정책 구성](https://go.microsoft.com/fwlink/?LinkId=534136)을 참조 하 고 추가 [고급 스팸 필터링 옵션](https://go.microsoft.com/fwlink/?LinkId=534137) 스팸으로 표시 하는 메시지를 발생 시킬 수 있는 기능을 해제 합니다. 
  
## <a name="help-your-end-users-create-a-safe-sender-list-to-prevent-good-email-from-being-marked-as-spam"></a>스팸으로 표시 되 고에서 좋은 전자 메일을 방지 하기 위해 수신 허용-보낸사람 목록을 만드는 최종 사용자 지원
<a name="BKMK_email-user-help-safelist"> </a>

[Outlook](https://go.microsoft.com/fwlink/p/?LinkId=270065) 또는 [웹에서 Outlook](https://go.microsoft.com/fwlink/p/?LinkId=294862)의 수신 허용-보낸사람 목록에 신뢰 하는 사람이 보낸 주소를 추가 하려면 사용자에 게를 알려주십시오. Outlook에서 웹에 시작 **설정**을 선택![ConfigureAPowerBIAnalysisServicesConnector_settingsIcon](media/24bd5467-c8d2-4936-9c37-a179bd0e21ec.png) \> **옵션** \> **차단 또는 허용**합니다. 다음 다이어그램에는 수신 허용-보낸사람 목록에 무언가 추가 하는 예가 나와 있습니다.
  
![Outlook Web App에서 수신 허용-보낸사람 추가 (영문)](media/8de6b24e-429e-4e8f-8ce8-53ba659cbfcb.png)
  
사용자의 수신 허용-보낸사람 및 받는 사람, 하지만 안전 도메인 하지 EOP 제한이 됩니다. 이 도메인은 웹에서 Outlook을 통해 추가 하거나 Outlook에서 추가 여부에 관계 없이 true 이며 디렉터리 동기화를 사용 하 여 동기화 합니다.
  
## <a name="troubleshooting-a-message-ends-up-in-the-junk-folder-even-though-eop-marked-the-message-as-non-spam"></a>문제해결: 메시지를 완성 정크 폴더에 EOP 스팸이 아닌 메시지를 표시 하는 경우에
<a name="TroubleshootingJunkEOPNonSpam"> </a>

사용자가 있지만 옵션은를 사용 하도록 설정 하는 Outlook에서 "안전 하 게 보호만 나열: 사람이 나 수신 허용-보낸사람 목록이 나 수신 허용-받는 사람 목록에 있는 도메인의 유일한 메일 받은 편지 함으로 배달 됩니다"를 선택한 후 모든 전자 메일이 정크 메일 폴더로 보낸사람에 대 한 보낸 사람이 reci에 하지 않은 경우 pient의 수신 허용-보낸사람 목록을 제공 합니다. 이 값은 스팸이 아닌 메시지를 표시 하려면 EOP에서 규칙을 설정한 경우 또는 스팸이 아닌 메시지를 표시 하는 EOP 여부에 관계 없이 것입니다.
  
지침에 따라 Outlook 사용자에 대 한 수신 허용 목록 만으로 옵션을 비활성화할 수 [Outlook: 정크 메일 UI를 사용 하지 않도록 설정 하려면 정책 설정 및 메커니즘 필터링](https://support.microsoft.com/en-us/kb/2180568)합니다.
  
웹에 있는 Outlook에서 메시지를 표시 하는 경우 보낸 사람이 받는 사람의 수신 허용-보낸사람 목록에 없기 때문에 정크 폴더에 메시지 인지 여부를 나타내는 노란색 안전 팁이 됩니다.
  
메시지 머리글을 보면 스탬프 SFV:SKN (IP 허용 또는 ETR 허용) 또는 SFV:NSPM (스팸이 아닌)를 포함 될 수 있습니다 하지만 메시지는 여전히 사용자의 정크 메일 폴더에 배치 됩니다. 이 처럼 사용자가 "수신 허용 목록 만으로" 사용할 수 있는지 여부를 나타내는 메시지 헤더에서 합니다. 이러한 "수신 허용 목록 만으로" 옵션을 사용자가 Outlook에서 설정한 EOP 설정 보다 우선 하기 때문에 발생 합니다. 
  
 **확인 하려면 이유 수신 허용-보낸에서 사람의 메시지를 표시 스팸이 아닌 메시지 헤더 하지만 여전히 끝에서으로 사용자의 정크 폴더에서**
  
1. Exchange Online PowerShell에 연결 하는 방법을 알아보려면 [Exchange Online PowerShell 연결](https://go.microsoft.com/fwlink/p/?LinkId=396554)을 참조 하십시오. 
    
2. 사용자의 정크 메일 구성 설정을 보려면 다음 명령을 실행 합니다.
    
  ```
  Get-MailboxJunkEmailConfiguration example@contoso.com | fl TrustedListsOnly,ContactsTrusted,TrustedSendersAndDomains
  ```

    TrustedListsOnly가 True로 설정 하는 경우이 설정을 사용 하는 것을 의미 합니다. ContactsTrusted가 True로 설정 하는 경우 사용자 연락처 및 수신 허용-보낸사람 모두 신뢰 하는 것을 의미 합니다. TrustedSendersAndDomains 사용자의 수신 허용-보낸사람 목록의 내용을 나열합니다.
    
## <a name="still-need-help"></a>여전히 도움이 필요 하십니까?
<a name="TroubleshootingJunkEOPNonSpam"> </a>

[![Office 365 커뮤니티 포럼에서 도움말 보기](media/12a746cc-184b-4288-908c-f718ce9c4ba5.png)](https://go.microsoft.com/fwlink/p/?LinkId=518605)
  
[![관리자: 서비스 요청 로그인 및 만들기](media/10862798-181d-47a5-ae4f-3f8d5a2874d4.png)]( https://go.microsoft.com/fwlink/p/?LinkId=519124)
  
[![관리자: 지원 서비스 문의](media/9f262e67-e8c9-4fc0-85c2-b3f4cfbc064e.png)](https://go.microsoft.com/fwlink/p/?LinkID=518322)
  
## <a name="see-also"></a>참고 항목
<a name="TroubleshootingJunkEOPNonSpam"> </a>

[정크 메일 필터의 개요 (영문)](https://support.office.com/article/5AE3EA8E-CF41-4FA0-B02A-3B96E21DE089)
  
[차단 또는 허용 (정크 메일 설정)](https://support.office.com/article/48c9f6f7-2309-4f95-9a4d-de987e880e46)
  
[Office 365 스팸 필터로 전자 메일 스팸을 차단하여 거짓 부정 문제 방지](block-email-spam-to-prevent-false-negatives.md)

