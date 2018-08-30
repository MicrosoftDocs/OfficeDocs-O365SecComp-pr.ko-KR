---
title: Office 365로 전송한 문제 해결 메일
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 5/2/2016
ms.audience: ITPro
ms.topic: troubleshooting
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: f4caa4e1-e414-4b21-8822-31c08064c059
description: 이 문서에서는 Office 365 및 Office 365 고객에 게 대량 메일로 대 한 모범 사례에 받은 편지함에 전자 메일을 보내려고 할 때 문제를 발생 하는 발신자에 대 한 문제해결 정보를 제공 합니다.
ms.openlocfilehash: 3d8c0a05d096da87b9f686222055d76a6ae96ff2
ms.sourcegitcommit: e9dca2d6a7838f98bb7eca127fdda2372cda402c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/21/2018
ms.locfileid: "23003207"
---
# <a name="troubleshooting-mail-sent-to-office-365"></a>Office 365로 전송한 문제 해결 메일

이 문서에서는 Office 365 및 Office 365 고객에 게 대량 메일로 대 한 모범 사례에 받은 편지함에 전자 메일을 보내려고 할 때 문제를 발생 하는 발신자에 대 한 문제해결 정보를 제공 합니다.
  
## <a name="troubleshooting-common-problems-with-mail-delivery-to-office-365"></a>Office 365에 대 한 메일 배달의 일반적인 문제를 해결

이러한 일반적으로 발생 한 문제 중 하나를 선택 합니다.
  
- [신뢰도 보내는 IP 및 도메인의 관리 수 있습니까?](troubleshooting-mail-sent-to-office-365.md#ManageRep)
    
- [새 IP 주소에서 보내는 메일 적용 되어 있습니까?](troubleshooting-mail-sent-to-office-365.md#NewIPs)
    
- [DNS가 올바르게 설정 되었는지 확인 합니다.](troubleshooting-mail-sent-to-office-365.md#ConfirmDNSsetup)
    
- [하면 보급 안함 사용자가 직접 라우팅할 수 없는 IP로 확인](troubleshooting-mail-sent-to-office-365.md#NoReverseDNS)
    
- [받은 배달 못함 보고서 (NDR) 전자 메일을 보낼 때 Office 365에서 사용자에 게](troubleshooting-mail-sent-to-office-365.md#NDRInbound)
    
- [EOP에서 받는 사람의 정크 메일 폴더에 착륙 내 전자 메일](troubleshooting-mail-sent-to-office-365.md#JunkMailBox)
    
- [내 IP 주소에서 보낸 트래픽에 EOP에 의해 제한](troubleshooting-mail-sent-to-office-365.md#AllowEOPIPs)
    
### <a name="are-you-managing-your-ip-and-domains-sending-reputation"></a>신뢰도 보내는 IP 및 도메인의 관리 수 있습니까?
<a name="ManageRep"> </a>

EOP 필터링 기술은 Microsoft Office 365 Exchange 서버, Microsoft Office Outlook 및 Windows Live 메일 같은 다른 Microsoft 제품에 대 한 스팸 방지 보호 기능을 제공 하도록 디자인 되었습니다. 활용 SPF, DKIM, 및 DMARC;는 주소는 데 도움이 되는 인증 기술 스푸핑 및 피싱 문제 그렇게 전자 메일을 보내는 도메인에 있는 권한이 있는지 확인 하 여 전자 메일. 다양 한 요인 보내는 IP, 도메인, 인증, 목록 정확성, 불만 속도, 콘텐츠 및 자세한 관련 하 여 EOP 필터링 하는 영향을 받습니다. 이러한, 주체의 하나 영향을 미치는 보낸 사람의 신뢰도 운전 하 고 전자 메일을 제공 하는 능력은 자신의 정크 메일 불만 속도입니다. 
  
### <a name="are-you-sending-email-from-new-ip-addresses"></a>새 IP 주소에서 보내는 메일 적용 되어 있습니까?
<a name="NewIPs"> </a>

적이 없는 전자 메일을 보낼 일반적으로 사용 하는 IP 주소는 시스템에서 구축 된 신뢰도 필요는 없습니다. 결과적으로, 새 Ip에서 보내는 전자 메일은 배달 문제가 발생할 가능성이 높습니다. IP가 스팸을 보내지 않으려면에 대 한 신뢰도 작성 되 면 EOP 더 나은 전자 메일 배달 경험에 대 한 일반적으로 허용 됩니다.
  
일반적으로 기존 SPF 레코드에서 인증 하는 도메인에 대 한 추가 되는 새 Ip 상속 하는 도메인의 보내는 신뢰도 중 일부의 이점도 경험이 있어야 합니다. 도메인에 좋은 경우 신뢰도 보내는 새 Ip 발생할 수는 더 빠른 시간 향상. 새 IP 수 완벽 하 게 단계적 몇 주 또는 볼륨, 목록 정확성 및 정크 메일 불만 비율에 따라 빨리 내에서 예상할 수 있습니다.
  
### <a name="confirm-that-your-dns-is-set-up-correctly"></a>DNS가 올바르게 설정 되었는지 확인 합니다.
<a name="ConfirmDNSsetup"> </a>

만들고 메일 라우팅에 필요한 MX 레코드를 포함 하는 DNS 레코드를 유지 관리 하는 방법에 대 한 지침은 DNS 호스팅 공급자에 게 문의 해야 합니다.
  
### <a name="ensure-that-you-do-not-advertise-yourself-as-a-non-routable-ip"></a>하면 보급 안함 사용자가 직접 라우팅할 수 없는 IP로 확인
<a name="NoReverseDNS"> </a>

역방향 DNS 조회 실패 사람이 보낸 전자 메일을 허용 하지 않습니다 했습니다. 일부 경우에 적법 한 보낸 사람이 광고 하지 자신 올바르게 인터넷 간 라우팅 가능한 IP로 EOP에 대 한 연결을 열려고 시도할 때 합니다. 개인 (라우팅할 수 없는) 네트워킹에 대 한 예약 된 IP 주소에는 다음이 포함 됩니다.
  
- 192.168.0.0/16 (또는 192.168.0.0-192.168.255.255)
    
- 10.0.0.0/8 (또는 10.0.0.0-10.255.255.255)
    
- 172.16.0.0/11 (또는 172.16.0.0-172.31.255.255)
    
### <a name="you-received-a-non-delivery-report-ndr-when-sending-email-to-a-user-in-office-365"></a>받은 배달 못함 보고서 (NDR) 전자 메일을 보낼 때 Office 365에서 사용자에 게
<a name="NDRInbound"> </a>

일부 배달 문제는 보낸 사람의 IP 주소가 Microsoft에 의해 차단 되 고 발생 했거나 사용자 계정은 이전 스팸 활동으로 인해 차단된 sender로 식별 됩니다. 오류는 NDR 받았는지 생각 되는 경우 먼저 문제를 해결 하려면 NDR 메시지의 지침을 따릅니다. 
  
받은 오류에 대 한 자세한 내용은 [온-프레미스 Exchange 2013 및 Office 365의 Dsn 및 Ndr에](http://technet.microsoft.com/library/8e91de84-76fa-49b2-898c-c5eface76560.aspx)SMTP 오류 코드의 전체 목록은 참조 하십시오.
  
 예는 다음과 같은 NDR을 수신 하는 경우 나타냅니다 보내는 IP 주소가 Microsoft에 의해 차단 된는. 
  
 `550 5.7.606-649 Access denied, banned sending IP [x.x.x.x]; To request removal from this list please visit https://sender.office.com/ and follow the directions.`
  
이 목록에서 제거를 요청 하려면 [Office 365 수신된 거부 목록에서 자신을 제거 하려면 delist 포털을 사용할](use-the-delist-portal-to-remove-yourself-from-the-office-365-blocked-senders-lis.md)수 있습니다.
  
### <a name="my-email-landed-in-the-recipients-junk-folder-in-eop"></a>EOP에서 받는 사람의 정크 메일 폴더에 착륙 내 전자 메일
<a name="JunkMailBox"> </a>

메시지를 올바르게 하지 스팸으로 식별 EOP에 의해, 받는 사람에 게 평가 하 고 메시지를 분석 Microsoft 스팸 분석 팀에 게이 false 이면 가양성 메시지 제출 작업할 수 있습니다. 분석의 결과 따라 서비스 수준 스팸 콘텐츠 필터 규칙을 통해 메시지를 허용 하도록 조정 될 수 있습니다. 전자 메일을 사용 하 여 스팸으로 분류 되지 않도록 해야 하는 Microsoft에 게 메시지를 전송할 수 있습니다. 이렇게 하는 경우에 다음 절차의 단계를 사용 해야 합니다.
  
### <a name="to-use-email-to-submit-false-positive-messages-to-the-microsoft-spam-analysis-team"></a>사용 하 여 전자 메일을 Microsoft 스팸 분석 팀 가양성 메시지 전송

1. 스팸이 아닌으로 전송 하려는 메시지를 저장 합니다.
    
2. 비어 있는 새 메시지를 작성하여 스팸이 아니라는 메시지를 첨부합니다.
    
    필요한 경우에 여러 스팸이 아닌 메시지를 첨부할 수 있습니다.
    
3. 원본 메시지의 제목 줄을 복사하여 새 메시지의 제목 줄에 붙여 넣습니다.
    
    > [!IMPORTANT]
    > 새 메시지의 본문은 비워 둡니다. 
  
4. 새 메시지를 [not_junk@office365.microsoft.com](mailto:not_junk@office365.microsoft.com)으로 보냅니다.
    
### <a name="traffic-from-my-ip-address-is-throttled-by-eop"></a>내 IP 주소에서 보낸 트래픽에 EOP에 의해 제한
<a name="AllowEOPIPs"> </a>

하 고 있음을 나타내는 EOP에서 NDR을 수신 하는 경우 사용자의 IP 주소는 되 고 제한 EOP에 의해 예:
  
 `host xxxx.outlook.com [x.x.x.x]: 451 4.7.550 Access denied, please try again later`
  
IP 주소에서 의심 스러운 작업에서 발견 하 고 확인 되는 추가 하는 동안에 일시적으로 제한 된가 때문에 NDR을 수신 합니다. 평가 통해의 생각을 선택 취소 하면이 제한 사항은 잠시 후에 변경 됩니다.
  
### <a name="i-cant-receive-email-from-senders-in-office-365"></a>Office 365에 있는 사람이 보낸 전자 메일을 받을 수 없습니다.
<a name="AllowEOPIPs"> </a>

 사용자에 게에서 메시지를 수신 하기 위해 네트워크 EOP 데이터 센터에서 사용 하는 IP 주소에서 연결을 허용 하는지 확인 합니다. 자세한 내용은 [Exchange Online Protection IP 주소](eop/exchange-online-protection-ip-addresses.md)를 참조 하십시오. 모든 IP의 레코드에 대 한 추가 된 주소 변경 또는 [EOP IP 주소에 대 한 변경 알림](eop/change-notification-for-eop-ip-addresses.md)참조 작년 사용 되지 않습니다.
  
## <a name="best-practices-for-bulk-emailing-to-office-365-users"></a>Office 365 사용자에 게 대량 전자 메일 보내기에 대 한 모범 사례
<a name="BulkMailer"> </a>

자주 Office 365 사용자에 게 대량 전자 메일 캠페인을 수행 하 고 안전 하 고 시기 적절 한 방식으로 사용자 전자 메일 도착 되었는지 확인 하려면, 하는 경우이 섹션의 팁을 따릅니다.
  
### <a name="ensure-that-the-from-name-reflects-who-is-sending-the-message"></a>From 확인: 메시지를 보내는 사람 이름 반영

어떤 메시지의 간단한 요약의, 및 메시지 본문 명확 하 게 하 고 간결 하 게 나타내야 구축, 서비스 또는 제품 란에 대 한 제목 여야 합니다. 예를 들어:
  
맞는
  
 ` From: marketing@shoppershandbag.com `
  
 `Subject: Updated catalog for the Christmas season!`
  
잘못 된
  
 `From: someone@outlook.com`
  
 `Subject: Catalogs`
  
사용자는 누구에 게 쉽게 하 고 수행 중인, 덜 난이도 대부분의 스팸 필터를 통해 제공 해야 합니다.
  
### <a name="always-include-an-unsubscribe-option-in-campaign-emails"></a>항상 캠페인 전자 메일에서 구독 취소 옵션을 포함

특히 뉴스레터를 전자 메일: 마케팅 하 향후 전자 메일에서 구독을 취소 하는 방법의 항상 포함 되어야 합니다. 예를 들어:
  
 `This email was sent to example@contoso.com by sender@fabrikam.com.`
  
 `Update Profile/Email Address | Instant removal with SafeUnsubscribe™ | Privacy Policy`
  
일부 보낸사람을 특정 별칭으로 "취소"와 제목에 전자 메일을 보낼 받는 사람을 요구 하 여이 옵션을 포함 합니다. 위의 한번 클릭 예제를 원합니다 아닙니다. 메일을 보낼 받는 사람을 요구 하도록 수행 하려는 경우에 사용자에 대 한 링크를 클릭 하면 모든 필수 필드는 미리 채워진 확인 합니다.
  
### <a name="use-the-double-opt-in-option-for-marketing-email-or-newsletter-registration"></a>이중 옵트인 옵션을 사용 하 여 마케팅 전자 메일 또는 뉴스레터 등록

회사 필요 하거나 제품 또는 서비스에 액세스 하기 위해 사용자 연락처 정보를 등록을 권장 하는 경우에이 업계 모범 사례는 것이 좋습니다. 일부 회사에서는 쉽게 사용자에 게 전자 메일 마케팅에 자동으로 등록 하는 방법 또는 e-뉴스레터 등록 프로세스 하지만이 하는 동안에 전자 메일 필터링의 세계에서 의심 스러운 마케팅 연습 것으로 간주 됩니다.
  
등록 하는 동안 하는 경우는 "예, 보내 주시기 바랍니다 회보" 또는 "예, 보내 주시기 바랍니다 특수 제공" 확인란이 선택 되어 기본적으로, 사용자에 게 닫기 주의 하지 마케팅 전자 메일 또는 하지 않는 뉴스레터 등록 실수로 될 수 있습니다 수신 하려고 합니다.
  
 것이 좋습니다 이중 옵트인 옵션을 대신 하는 마케팅 전자 메일 또는 회보의 확인란은 기본적으로 선택 하지 것을 의미 합니다. 또한 등록 양식이 제출 되 면 확인 전자 메일을 자신의 결정 마케팅 전자 메일을 받을 수를 확인 하도록 허용 하는 URL 가진 사용자에 게 전송 됩니다. 
  
 그러면이 있는 마케팅 전자 메일을 받도록 하려는 사용자만 서명는 전자 메일에 대 한 이후에 사례 마케팅 하는 의심 스러운 전자 메일의 보내는 회사의 선택을 취소 합니다. 
  
### <a name="ensure-that-email-message-content-is-transparent-and-traceable"></a>전자 메일 메시지 콘텐츠를 투명 하 게 하 고 추적 가능한 있는지 확인

것도 마찬가지로 중요 전자 메일 전송 하는 방법을 포함 하는 콘텐츠를 그대로 합니다. 전자 메일 콘텐츠를 만들 때 다음과 같은 모범 사례를 사용 하 여 확인 전자 메일 서비스를 필터링 하 여 사용자 전자 메일을 플래그가 지정 수 되지 것입니다.
  
- 전자 메일 메시지는 받는 사람에 게 주소록에 보낸사람 추가를 명확 하 게 명시 해야 것을 요청 하는 경우 이러한 작업은 하지 배달이 보장 합니다.
    
- 유사 하 고 일관 되 고 있지 여러 메시지의 본문에 포함 된 리디렉션하거나 수 있어야 하 고 다양 한 합니다. 이 컨텍스트에서 리디렉션 링크 및 문서와 같은 메시지 로부터 가리키는 되는 합니다. 광고 또는 구독 취소 링크의 많은 했거나 프로필 파일에 대 한 링크를 업데이트 하는 경우 모든 가리켜야 동일한 도메인에 있습니다. 예를 들어:
    
    맞는
    
     `unsubscribe.bulkmailer.com`
    
     `profile.bulkmailer.com`
    
     `options.bulkmailer.com`
    
    잘못 된
    
     `unsubscribe.bulkmailer.com`
    
     `profiles.excite.com`
    
     `options.yahoo.com`
    
- 큰 이미지 및 첨부 파일, 또는 이미지로 구성 된 메시지를 사용 하 여 콘텐츠를 방지 합니다.
    
- 공개 개인정보 또는 P3P 설정 추적 픽셀 (웹 버그 또는 탐지 장치)의 현재를 상태 명확 하 게 해야 합니다.
    
### <a name="remove-incorrect-email-aliases-from-your-databases"></a>데이터베이스에서 잘못 된 전자 메일 별칭을 제거 합니다.

튀어오르 저장에서 만들어지는 데이터베이스의 모든 전자 메일 별칭 필요 하지 않으며 사용자 아웃 바운드 전자 메일이 추가 조사를 수행 하는 위험에 전자 메일 서비스를 필터링 하 여 내리지 못할 수 있습니다. 전자 메일 데이터베이스 최신 상태 인지 확인 합니다.
  

