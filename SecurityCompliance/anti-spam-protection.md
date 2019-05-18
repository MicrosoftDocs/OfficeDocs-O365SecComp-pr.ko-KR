---
title: Office 365 전자 메일 스팸 방지 보호
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 6/29/2018
audience: Admin
ms.topic: overview
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 6a601501-a6a8-4559-b2e7-56b59c96a586
ms.collection:
- M365-security-compliance
description: Exchange Online 및 Office 365에서 스팸을 방지 하는 데 도움이 되는 스팸 방지 설정 및 필터에 대해 알아봅니다. Office 365에서 너무 많은 스팸 받기 스팸 필터 및 스팸 방지 정책 설정을 사용자 지정할 수 있습니다.
ms.openlocfilehash: 64048e2621082edae21285df8b8fd1bcbd2e7c4a
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/17/2019
ms.locfileid: "34152330"
---
# <a name="office-365-email-anti-spam-protection"></a>Office 365 전자 메일 스팸 방지 보호

Office 365에서 너무 많은 스팸을 걱정 하나요? Microsoft는 Office 365 또는 Exchange Online Protection (EOP) 서비스에 여러 개의 스팸 필터를 작성 하 여 첫 번째 메시지를 받은 순간 로부터 전자 메일을 보호 합니다. Office 365에서 스팸을 방지 하기 위해 조직의 특정 문제를 처리 하는 보호 설정을 변경 하 고, 예를 들어 특정 보낸 사람 으로부터 많은 스팸 메일을 받거나, 단순히 설정을 미세 조정 하 여 조직의 요구에 가장 잘 맞는 조정 이렇게 하려면 Office 365 보안 &amp; 및 준수 센터에서 스팸 방지 설정을 변경 하면 됩니다.
  
이 문서는 Office 365 관리자를 위한 것입니다. 관리자가 아니지만 Office 365 사용자가 수신 하는 스팸 자료를 처리 하는 방법을 알아보려면 원하는 문서가 아닙니다. 대신, Outlook for PC 또는 Mac 용 Outlook을 사용 하는 경우에 [는 정크 메일 필터 개요](https://support.office.com/article/5ae3ea8e-cf41-4fa0-b02a-3b96e21de089)를 사용 하 여 시작 합니다. 웹에서 Outlook을 사용 하는 경우에는 [정크 메일 및 피싱에 대 한 자세한](https://support.office.com/article/86c1d76f-4d5a-4967-9647-35665dc17c31)정보부터 확인 하세요.
  
## <a name="these-options-help-you-prevent-spam-in-office-365"></a>이러한 옵션은 Office 365에서 스팸을 방지 하는 데 도움이 됩니다.

 **연결 필터링**: 연결 필터링을 사용 하는 경우 Office 365에서는 메시지를 받기 전에 보낸 사람의 신뢰도를 확인 합니다. 특정 IP 주소 또는 IP 주소 범위에서 전송 되는 모든 메시지를 수신 하도록 허용 목록 또는 안전한 보낸 사람 목록을 만들 수 있습니다. 또한 차단 목록 이라는 메시지를 차단 하는 데 사용할 IP 주소 목록을 만들 수도 있습니다. 자세한 내용은 [Configure the Connection Filter Policy](https://technet.microsoft.com/library/jj200718%28v=exchg.150%29.aspx)을 참조하세요. Office 365의 스팸이 염려 되는 경우에는 연결 필터링을 사용 하 여 스팸을 방지 합니다.
  
Office 365 Enterprise e 5가 있고, Advanced Threat Protection (ATP) 라이선스를 구매한 고객의 경우에는 스푸핑 인텔리전스에서 연결 필터링을 사용 하 여 도메인을 위장 하는 보낸 사람 목록을 만들고 차단 합니다. 자세한 내용은 [스푸핑 인텔리전스에 대 한 자세한 내용을](https://go.microsoft.com/fwlink/?LinkID=735009)참조 하세요.
  
 **스팸 필터링**: Office 365에서 스팸 필터링을 사용 하 여 메시지 특성이 스팸으로 일치 하는지 확인 합니다. 스팸으로 식별된 메시지에 대해 수행할 작업을 변경할 수 있으며, 특정 언어로 작성되었거나 특정 국가 또는 지역에서 보낸 메시지를 필터링할지 여부를 선택할 수 있습니다. 적극적인 스팸 필터링 방식을 원하는 경우에는 고급 스팸 필터링 옵션을 설정할 수도 있습니다. 또한 메시지가 격리되면 해당 메시지의 대상이었던 받는 사람에게 알림을 표시하도록 최종 사용자 스팸 알림을 구성할 수도 있습니다. (격리로 메시지를 보내는 것은 구성 가능한 작업 중 하나입니다.) 이러한 알림에서 최종 사용자는 가양성을 릴리스하고 분석을 위해 Microsoft에 보고할 수 있습니다. 자세한 내용은 [스팸 필터 정책 구성을](https://go.microsoft.com/fwlink/p/?LinkId=617147)참조 하세요. Office 365에서 스팸을 방지 하려면 스팸 필터링을 사용 하 고, Office 365에서 스팸을 너무 많이 걱정 되는 경우에는 연결 필터링을 사용 하 여 스팸을 방지 합니다.
  
> [!NOTE]
> EOP 독립 실행형 고객의 경우: 기본적으로 EOP 스팸 필터는 스팸 검색 메시지를 각 받는 사람의 정크 메일 폴더로 보냅니다. 그러나 온-프레미스 사서함을 사용 하 여 **정크 메일 폴더로 메시지 이동** 작업을 수행 하려면 온-프레미스 서버에서 두 개의 Exchange 메일 흐름 규칙 (전송 규칙이 라고도 함)을 구성 하 여 사용자가 추가한 스팸 헤더를 검색 해야 합니다. EOP. 자세한 내용은 [스팸이 각 사용자의 정크 메일 폴더로 라우팅되는지 확인](https://technet.microsoft.com/library/jj837173%28v=exchg.150%29.aspx)을 참조하십시오. 
  
## <a name="extra-information-if-you-receive-too-much-spam-in-office-365"></a>Office 365에서 스팸이 너무 많이 수신 되는 경우 추가 정보

다음 비디오에서는 EOP에서 스팸 필터링을 구성 하는 방법에 대해 간략하게 설명 합니다.
  
> [!VIDEO https://www.microsoft.com/videoplayer/embed/608be94c-d763-4c47-af94-99e7cb277713?autoplay=false]
  
자세한 내용은 [스팸 필터 정책 구성](https://go.microsoft.com/fwlink/p/?LinkId=617147) 항목을 참조 하십시오.
  
## <a name="check-your-outgoing-messages-to-prevent-spam-in-office-365"></a>Office 365에서 스팸을 방지 하기 위해 보내는 메시지 확인

 **아웃 바운드 필터링**: Office 365 에서도 사용자가 스팸을 보내지 않는지 확인 합니다. 예를 들어 사용자의 컴퓨터가 스팸 메시지를 보내도록 하는 맬웨어를 감염 시킬 수 있으므로 *아웃 바운드 필터링*이라고 하는 보호 기능을 구축 합니다. 아웃 바운드 필터링을 해제할 수는 없지만, [아웃 바운드 스팸 정책 구성](https://technet.microsoft.com/library/jj200737%28v=exchg.150%29.aspx)에서 설명 하는 설정을 구성할 수도 있습니다. Office 365에서 너무 많은 스팸 메일이 염려 되는 경우 아웃 바운드 필터링을 사용 하 여 Exchange Online에서 스팸을 방지 합니다.
  
## <a name="beyond-the-basics-more-ways-to-prevent-spam-in-office-365"></a>기본 사항 외에도, Office 365에서 스팸을 방지 하는 다른 방법이 있습니다.

 **메일 흐름 규칙**: 기본 제공 되는 스팸 필터링 이상의 기능을 사용 하 고 비즈니스 정책을 기반으로 하는 사용자 지정 규칙을 만들려면 _[메일 흐름 규칙](https://technet.microsoft.com/library/jj919238%28v=exchg.150%29.aspx)_ ( _전송 규칙이_라고도 함)은 Office에서 스팸을 방지 하는 데 도움이 되는 또 다른 필터입니다. 365 예를 들어 메일 흐름 규칙을 사용 하 여 [메시지의 scl (스팸 지 수) 설정](use-mail-flow-rules-to-set-the-spam-confidence-level-scl-in-messages.md)에 설명 된 대로 특정 조건과 일치 하는 메시지에 대 한 SCL (스팸 지 수) 값을 설정할 수 있습니다.
  
 **전자 메일 인증**: DNS (Domain Name System)를 사용 하 여 전자 메일 메시지를 보낸 사람에 대 한 전자 메일 메시지에 안정형 정보를 추가 하는 기법을 전자 메일 인증 이라고 합니다. 고급 Office 365 관리자는 다음과 같은 전자 메일 인증 방법을 사용할 수 있습니다.
  
- **Spf (Sender Policy Framework)**: 전송 도메인의와 대조 소유자에 대해 보낸 사람의 IP 주소를 확인 하 여 전자 메일 메시지의 원본에 대 한 유효성을 검사 합니다. SPF에 대 한 간략 한 소개 및 신속한 구성에 대 한 자세한 내용은 [스푸핑을 방지 하기 위해 Office 365에서 spf를 설정](https://technet.microsoft.com/library/dn789058%28v=exchg.150%29.aspx)합니다 .를 참조 하세요. Office 365에서 SPF를 사용 하는 방법과 하이브리드 배포와 같은 문제 해결 또는 비표준 배포를 자세히 이해 [하려면 office 365에서 spf (Sender Policy Framework)를 사용 하 여 스푸핑을 방지](https://technet.microsoft.com/library/mt712724%28v=exchg.150%29.aspx)하는 방법을 시작 합니다.

- **Domainkeys 확인 메일 (dkim)**: dkim을 사용 하면 전자 메일 메시지에 디지털 서명을 첨부 하 여 보내는 전자 메일의 메시지 헤더에 첨부할 수 있습니다. 도메인에서 전자 메일을 수신 하는 전자 메일 시스템은이 디지털 서명을 사용 하 여 수신 하는 받는 전자 메일이 합법적인 지를 확인 합니다. DKIM 및 Office 365에 대 한 자세한 내용은 [office 365에서 도메인에서 보낸 아웃 바운드 전자 메일의 유효성 검사를 위해 DKIM을 사용](https://technet.microsoft.com/library/mt695945%28v=exchg.150%29.aspx)합니다 .를 참조 하세요.

- **도메인 기반 메시지 인증, 보고 및 적합성 (DMARC)**: DMARC에서는 전자 메일 시스템 수신에 도움이 되는 메시지에 대해 수행할 작업을 결정 하 고, SPF 또는 dkim을 검사 하는 데에는 어떤 작업을 수행 하는 것이 좋습니다. DMARC 설정에 대 한 자세한 내용은 [Office 365에서 DMARC를 사용 하 여 전자 메일의 유효성 검사를](https://technet.microsoft.com/library/mt734386%28v=exchg.150%29.aspx)참조 하세요.

Office 365의 스팸, 피싱 및 스푸핑에 대해 염려 되는 경우 SPF, DKIM 및 DMARC을 함께 사용 하 여 스팸 및 원치 않는 스푸핑 방지를 방지할 수 있습니다.
  
 **최종 사용자 관리 설정**: 최종 사용자가 자신의 스팸 설정을 관리 하는 방법에 대 한 자세한 내용은 [정크 메일 필터 개요](https://go.microsoft.com/fwlink/?LinkId=270065) (Microsoft Outlook 사용자의 경우) 또는 [정크 메일 및 피싱에 대 한](https://go.microsoft.com/fwlink/?LinkId=270068) 자세한 정보 (를 참조 하세요. 웹용 Outlook 사용자의 경우). EOP을 사용 하 여 온-프레미스 사서함을 보호 하는 경우에는 디렉터리 동기화를 사용 하 여 이러한 설정이 서비스에 동기화 되었는지 확인 해야 합니다. 디렉터리 동기화 설정에 대한 자세한 내용은 [EOP에서 메일 사용자 관리](https://technet.microsoft.com/library/dn636911%28v=exchg.150%29.aspx)에서 "디렉터리 동기화를 사용하여 메일 사용자 관리"를 참조하세요.
  
## <a name="for-more-information"></a>자세한 내용

[블로그: 스팸 및 피싱이 Office 365를 통해 제공 되는 이유는 무엇 인가요?](https://go.microsoft.com/fwlink/?LinkId=528179 )
  
[Anti-Spam Protection FAQ](https://technet.microsoft.com/library/jj937231%28v=exchg.150%29.aspx)
  
[수신 허용 목록 또는 기타 방법으로 스팸으로 표시된 거짓 부정 전자 메일 차단](prevent-email-from-being-marked-as-spam-0.md)
  
[정크 메시지를 차단할 수 있도록 Office 365 스팸 필터링을 설정 하는 방법](reduce-spam-email.md)
  
[정크 메일과 대량 전자 메일의 차이점은 무엇 인가요?](https://technet.microsoft.com/library/dn720441%28v=exchg.150%29.aspx)
  
[스팸 방지 메시지 헤더](https://technet.microsoft.com/library/dn205071%28v=exchg.150%29.aspx)
  
[Backscatter 메시지 및 EOP](https://technet.microsoft.com/library/dn499795%28v=exchg.150%29.aspx)

## <a name="more-resources"></a>추가 리소스

[Office 365 커뮤니티 포럼에서 도움 받기](https://go.microsoft.com/fwlink/p/?LinkId=518605)
  
[관리자: 로그인 및 서비스 요청 만들기](https://go.microsoft.com/fwlink/p/?LinkId=519124)
  
[관리자: 전화 지원](https://go.microsoft.com/fwlink/p/?LinkID=518322)
