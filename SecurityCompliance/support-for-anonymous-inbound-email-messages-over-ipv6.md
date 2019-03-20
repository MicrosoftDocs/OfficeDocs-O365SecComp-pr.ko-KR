---
title: IPv6을 통한 익명 인바운드 전자 메일 메시지 지원
ms.author: tracyp
author: MSFTTracyP
manager: laurawi
ms.date: ''
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: b68df621-0a5f-4824-8abc-41e0c4fd1398
ms.collection:
- M365-security-compliance
description: exchange online Protection 및 exchange online에 대해 IPv6 원본에서 익명 메시지에 대 한 지원을 구성 하는 방법을 알아봅니다.
ms.openlocfilehash: 5d87dc929d2d67681b21eb46a4aaa52ca32caff9
ms.sourcegitcommit: 0f93b37c39d807dec91f118aa671a3430c47a9ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/20/2019
ms.locfileid: "30693357"
---
# <a name="support-for-anonymous-inbound-email-messages-over-ipv6"></a><span data-ttu-id="dcabd-103">IPv6을 통한 익명 인바운드 전자 메일 메시지 지원</span><span class="sxs-lookup"><span data-stu-id="dcabd-103">Support for anonymous inbound email messages over IPv6</span></span>

<span data-ttu-id="dcabd-104">EOP (exchange online Protection) 및 exchange online 지원은 TLS (전송 계층 보안)를 통해 메시지를 보내지 않는 보낸 사람 으로부터 IPv6 통신을 통해 익명 인바운드 전자 메일 메시지를 수신 합니다.</span><span class="sxs-lookup"><span data-stu-id="dcabd-104">Exchange Online Protection (EOP) and Exchange Online support receiving anonymous inbound email messages over IPv6 communications from senders who don't send messages over Transport Layer Security (TLS).</span></span> <span data-ttu-id="dcabd-105">microsoft 365 관리 센터 [https://admin.microsoft.com/adminportal/home](https://admin.microsoft.com/adminportal/home)를 열고 **지원을**클릭 한 다음 **새 서비스 요청**을 클릭 하 여 microsoft 지원에서이 기능을 요청 하면 IPv6을 통한 메시지를 수신 하도록 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dcabd-105">You can opt-in to receive messages over IPv6 by requesting this functionality from Microsoft Support by opening the Microsoft 365 admin center at [https://admin.microsoft.com/adminportal/home](https://admin.microsoft.com/adminportal/home), clicking **Support**, and then clicking **New service request**).</span></span> <span data-ttu-id="dcabd-106">i p v 6을 사용 하지 않는 경우에는 IPv4를 통해 메시지가 계속 수신 됩니다.</span><span class="sxs-lookup"><span data-stu-id="dcabd-106">If you don't opt-in to IPv6 you'll continue to receive messages over IPv4.</span></span>
  
<span data-ttu-id="dcabd-107">IPv6을 통해 서비스로 메시지를 전송하는 보낸 사람은 다음의 두 가지 요구 사항을 준수해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="dcabd-107">Senders who transmit messages to the service over IPv6 must comply with the following two requirements:</span></span>
  
1. <span data-ttu-id="dcabd-108">보내는 IPv6 주소에는 보내는 IPv6 주소의 유효한 PTR 레코드([역방향 DNS 레코드](https://en.wikipedia.org/wiki/Reverse_DNS_lookup))가 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="dcabd-108">The sending IPv6 address must have a valid PTR record ([reverse DNS record](https://en.wikipedia.org/wiki/Reverse_DNS_lookup) of the sending IPv6 address).</span></span> 
    
2. <span data-ttu-id="dcabd-109">보낸 사람은 [RFC 7208](https://tools.ietf.org/html/rfc7208)에 정의되어 있는 SPF 확인 또는 [RFC 6376](http://dkim.org/)에 정의되어 있는 [DKIM 확인](https://www.rfc-editor.org/rfc/rfc6376.txt)을 통과해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="dcabd-109">The sender must pass either SPF verification (defined in [RFC 7208](https://tools.ietf.org/html/rfc7208)) or [DKIM verification](http://dkim.org/) (defined in [RFC 6376](https://www.rfc-editor.org/rfc/rfc6376.txt)).</span></span>
    
<span data-ttu-id="dcabd-110">IPv6에 옵트인하기 이전의 구성에 상관없이 이러한 요구 사항을 충족해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="dcabd-110">Meeting these requirements is mandatory regardless of your configuration prior to opting-in to IPv6.</span></span> <span data-ttu-id="dcabd-111">두 요구 사항이 모두 충족되면 메시지에 대해 서비스에서 제공되는 일반 전자 메일 메시지 필터링이 수행됩니다.</span><span class="sxs-lookup"><span data-stu-id="dcabd-111">If both requirements are met, the message will go through normal email message filtering provided by the service.</span></span> <span data-ttu-id="dcabd-112">한 가지 또는 다른 조건이 충족 되지 않으면 다음 450 응답 중 하나로 메시지가 거부 됩니다.</span><span class="sxs-lookup"><span data-stu-id="dcabd-112">If one or the other isn't met, the message will be rejected with one of the following 450 responses:</span></span>
  
-  `450 4.7.25 Service unavailable, sending IPv6 address [2a01:111:f200:2004::240] must have reverse DNS record.`
    
-  `450 4.7.26 Service unavailable, message sent over IPv6 [2a01:111:f200:2004::240] must pass either SPF or DKIM validation.`
    
<span data-ttu-id="dcabd-113">IPv6을 통해 메시지를 받도록 설정하지 않은 상태에서 보낸 사람이 메일 서버에 수동으로 연결하여 IPv6을 통해 메시지를 강제로 보내려고 하면 메시지가 거부되며 다음과 같은 550 응답이 반환됩니다.</span><span class="sxs-lookup"><span data-stu-id="dcabd-113">If you aren't opted in to receive messages over IPv6 and the sender tries to force a message over IPv6 by manually connecting to the mail server, the message will be rejected with a 550 response that looks similar to the following:</span></span>
  
 `550 5.2.1 Service unavailable, [contoso.com] does not accept email over IPv6.`
  
## <a name="for-more-information"></a><span data-ttu-id="dcabd-114">자세한 내용</span><span class="sxs-lookup"><span data-stu-id="dcabd-114">For more information</span></span>

[<span data-ttu-id="dcabd-115">DKIM으로 서명된 메시지의 유효성 검사 지원</span><span class="sxs-lookup"><span data-stu-id="dcabd-115">Support for validation of DKIM signed messages</span></span>](support-for-validation-of-dkim-signed-messages.md)
  

