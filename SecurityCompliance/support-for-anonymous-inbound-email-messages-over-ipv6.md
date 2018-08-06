---
title: IPv6을 통한 익명 인바운드 전자 메일 메시지 지원
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 10/4/2017
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
ms.assetid: b68df621-0a5f-4824-8abc-41e0c4fd1398
description: Exchange Online Protection (EOP) 및 Exchange Online 전송 계층 보안 (TLS)를 통해 메시지를 보내지 않음 발신자의 i p v 6 통신을 통한 익명 인바운드 전자 메일 메시지를 수신을 지원 합니다. 하면 수 옵트인에서 Office 365 관리 센터를 열어 UNRESOLVED_TOKEN_VAL(exMCSS)에서이 기능을 요청 하 여 i p v 6을 통해 메시지를 받을 https://portal.office.com/adminportal/home, 지원를 클릭 한 다음 새 서비스 요청을 클릭 하). 하면 하지 옵트인 i p v 6을 하는 경우에 i p v 4를 통해 메시지를 받을를 계속 수 있습니다.
ms.openlocfilehash: a07e79732e9027d5848b787101be11066b5f0cb5
ms.sourcegitcommit: 22bca85c3c6d946083d3784f72e886c068d49f4a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/06/2018
ms.locfileid: "22026295"
---
# <a name="support-for-anonymous-inbound-email-messages-over-ipv6"></a><span data-ttu-id="c9611-105">IPv6을 통한 익명 인바운드 전자 메일 메시지 지원</span><span class="sxs-lookup"><span data-stu-id="c9611-105">Support for anonymous inbound email messages over IPv6</span></span>

<span data-ttu-id="c9611-p102">Exchange Online Protection (EOP) 및 Exchange Online 전송 계층 보안 (TLS)를 통해 메시지를 보내지 않음 발신자의 i p v 6 통신을 통한 익명 인바운드 전자 메일 메시지를 수신을 지원 합니다. 하면 수 옵트인에서 Office 365 관리 센터를 열어 UNRESOLVED_TOKEN_VAL(exMCSS)에서이 기능을 요청 하 여 i p v 6을 통해 메시지를 받을 [https://portal.office.com/adminportal/home](https://portal.office.com/adminportal/home), **지원**를 클릭 한 다음 **새 서비스 요청**을 클릭 하). 하면 하지 옵트인 i p v 6을 하는 경우에 i p v 4를 통해 메시지를 받을를 계속 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c9611-p102">Exchange Online Protection (EOP) and Exchange Online support receiving anonymous inbound email messages over IPv6 communications from senders who don't send messages over Transport Layer Security (TLS). You can opt-in to receive messages over IPv6 by requesting this functionality from UNRESOLVED_TOKEN_VAL(exMCSS) by opening the Office 365 admin center at [https://portal.office.com/adminportal/home](https://portal.office.com/adminportal/home), clicking **Support**, and then clicking **New service request**). If you don't opt-in to IPv6 you'll continue to receive messages over IPv4.</span></span>
  
<span data-ttu-id="c9611-109">IPv6을 통해 서비스로 메시지를 전송하는 보낸 사람은 다음의 두 가지 요구 사항을 준수해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c9611-109">Senders who transmit messages to the service over IPv6 must comply with the following two requirements:</span></span>
  
1. <span data-ttu-id="c9611-110">보내는 IPv6 주소에는 보내는 IPv6 주소의 유효한 PTR 레코드([역방향 DNS 레코드](https://en.wikipedia.org/wiki/Reverse_DNS_lookup))가 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c9611-110">The sending IPv6 address must have a valid PTR record ([reverse DNS record](https://en.wikipedia.org/wiki/Reverse_DNS_lookup) of the sending IPv6 address).</span></span> 
    
2. <span data-ttu-id="c9611-111">보낸 사람은 [RFC 7208](https://tools.ietf.org/html/rfc7208)에 정의되어 있는 SPF 확인 또는 [RFC 6376](http://dkim.org/)에 정의되어 있는 [DKIM 확인](https://www.rfc-editor.org/rfc/rfc6376.txt)을 통과해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c9611-111">The sender must pass either SPF verification (defined in [RFC 7208](https://tools.ietf.org/html/rfc7208)) or [DKIM verification](http://dkim.org/) (defined in [RFC 6376](https://www.rfc-editor.org/rfc/rfc6376.txt)).</span></span>
    
<span data-ttu-id="c9611-p103">이러한 요구 사항을 충족 하는 것은 i p v 6에을 사용 하 고 이전 구성에 관계 없이 필수입니다. 요구 사항을 모두 충족 되 면 서비스에 의해 제공 된 기본 전자 메일 메시지 필터링을 통해 메시지가 전달 됩니다. 하나 또는 다른 충족 되지 않습니다 메시지 다음 450 응답 중 하 나와 함께 거부 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c9611-p103">Meeting these requirements is mandatory regardless of your configuration prior to opting-in to IPv6. If both requirements are met, the message will go through normal email message filtering provided by the service. If one or the other isn't met, the message will be rejected with one of the following 450 responses:</span></span>
  
-  `450 4.7.25 Service unavailable, sending IPv6 address [2a01:111:f200:2004::240] must have reverse DNS record.`
    
-  `450 4.7.26 Service unavailable, message sent over IPv6 [2a01:111:f200:2004::240] must pass either SPF or DKIM validation.`
    
<span data-ttu-id="c9611-115">IPv6을 통해 메시지를 받도록 설정하지 않은 상태에서 보낸 사람이 메일 서버에 수동으로 연결하여 IPv6을 통해 메시지를 강제로 보내려고 하면 메시지가 거부되며 다음과 같은 550 응답이 반환됩니다.</span><span class="sxs-lookup"><span data-stu-id="c9611-115">If you aren't opted in to receive messages over IPv6 and the sender tries to force a message over IPv6 by manually connecting to the mail server, the message will be rejected with a 550 response that looks similar to the following:</span></span>
  
 `550 5.2.1 Service unavailable, [contoso.com] does not accept email over IPv6.`
  
## <a name="for-more-information"></a><span data-ttu-id="c9611-116">자세한 내용</span><span class="sxs-lookup"><span data-stu-id="c9611-116">For more information</span></span>

[<span data-ttu-id="c9611-117">DKIM으로 서명된 메시지의 유효성 검사 지원</span><span class="sxs-lookup"><span data-stu-id="c9611-117">Support for validation of DKIM signed messages</span></span>](support-for-validation-of-dkim-signed-messages.md)
  

