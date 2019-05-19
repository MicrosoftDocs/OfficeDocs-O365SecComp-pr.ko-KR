---
title: IPv6을 통한 익명 인바운드 전자 메일 메시지 지원
ms.author: tracyp
author: MSFTTracyP
manager: laurawi
ms.date: ''
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: b68df621-0a5f-4824-8abc-41e0c4fd1398
ms.collection:
- M365-security-compliance
description: Exchange Online Protection 및 Exchange Online에 대해 IPv6 원본에서 익명 메시지에 대 한 지원을 구성 하는 방법을 알아봅니다.
ms.openlocfilehash: 87317188a4564fccd968b00c9a93dc1b963c142b
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/17/2019
ms.locfileid: "34158190"
---
# <a name="support-for-anonymous-inbound-email-messages-over-ipv6"></a>IPv6을 통한 익명 인바운드 전자 메일 메시지 지원

EOP (exchange Online Protection) 및 Exchange Online 지원은 TLS (전송 계층 보안)를 통해 메시지를 보내지 않는 보낸 사람 으로부터 IPv6 통신을 통해 익명 인바운드 전자 메일 메시지를 수신 합니다. Microsoft 365 관리 센터 [https://admin.microsoft.com/adminportal/home](https://admin.microsoft.com/adminportal/home)를 열고 **지원을**클릭 한 다음 **새 서비스 요청**을 클릭 하 여 microsoft 지원에서이 기능을 요청 하면 IPv6을 통한 메시지를 수신 하도록 설정할 수 있습니다. I p v 6을 사용 하지 않는 경우에는 IPv4를 통해 메시지가 계속 수신 됩니다.
  
IPv6을 통해 서비스로 메시지를 전송하는 보낸 사람은 다음의 두 가지 요구 사항을 준수해야 합니다.
  
1. 보내는 IPv6 주소에는 보내는 IPv6 주소의 유효한 PTR 레코드([역방향 DNS 레코드](https://en.wikipedia.org/wiki/Reverse_DNS_lookup))가 있어야 합니다. 
    
2. 보낸 사람은 [RFC 7208](https://tools.ietf.org/html/rfc7208)에 정의되어 있는 SPF 확인 또는 [RFC 6376](http://dkim.org/)에 정의되어 있는 [DKIM 확인](https://www.rfc-editor.org/rfc/rfc6376.txt)을 통과해야 합니다.
    
IPv6에 옵트인하기 이전의 구성에 상관없이 이러한 요구 사항을 충족해야 합니다. 두 요구 사항이 모두 충족되면 메시지에 대해 서비스에서 제공되는 일반 전자 메일 메시지 필터링이 수행됩니다. 한 가지 또는 다른 조건이 충족 되지 않으면 다음 450 응답 중 하나로 메시지가 거부 됩니다.
  
-  `450 4.7.25 Service unavailable, sending IPv6 address [2a01:111:f200:2004::240] must have reverse DNS record.`
    
-  `450 4.7.26 Service unavailable, message sent over IPv6 [2a01:111:f200:2004::240] must pass either SPF or DKIM validation.`
    
IPv6을 통해 메시지를 받도록 설정하지 않은 상태에서 보낸 사람이 메일 서버에 수동으로 연결하여 IPv6을 통해 메시지를 강제로 보내려고 하면 메시지가 거부되며 다음과 같은 550 응답이 반환됩니다.
  
 `550 5.2.1 Service unavailable, [contoso.com] does not accept email over IPv6.`
  
## <a name="for-more-information"></a>자세한 내용

[DKIM으로 서명된 메시지의 유효성 검사 지원](support-for-validation-of-dkim-signed-messages.md)
  

