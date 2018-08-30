---
title: 후방 분산 메시지 및 EOP
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 12/9/2016
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 6f64f2de-d626-48ed-8084-03cc72301aa4
description: 후방 분산 메시지는 수신 스팸의 결과 일반적으로 메일 서버에서 전송 되는 자동화 된 튀어오르 메시지입니다. Backscatterer 이해는 목록 후방 분산 메시지를 보낼 수 있는 IP 주소입니다. 발신자 목록 없으며 Backscatterer 이해에서이 서버를 제거 하려고 하지 않습니다.
ms.openlocfilehash: 2ab5c6a3bec347446452acd3bdfd8c5d309994a9
ms.sourcegitcommit: e9dca2d6a7838f98bb7eca127fdda2372cda402c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/21/2018
ms.locfileid: "23002689"
---
# <a name="backscatter-messages-and-eop"></a><span data-ttu-id="31277-105">후방 분산 메시지 및 EOP</span><span class="sxs-lookup"><span data-stu-id="31277-105">Backscatter messages and EOP</span></span>

<span data-ttu-id="31277-p102">후방 분산 메시지는 수신 스팸의 결과 일반적으로 메일 서버에서 전송 되는 자동화 된 튀어오르 메시지입니다. Exchange Online Protection (EOP) 서비스를 필터링 하는 스팸 이기 때문에 전자 메일 메시지를 존재 하지 않는 받는 사람에 게 보내고 의심 스러운 다른 대상으로이 서비스에 의해 거부 됩니다. 이 경우 EOP 배달 못함 보고서 (NDR) 메시지를 생성 하 고 "보낸" 사람에 게 전달 스팸 위조 또는 "에서" 잘못 된 주소를 해당 메시지에 자주 사용 하기 때문에 NDR 전송 되는 보낸사람 주소 후방 분산 메시지 늘어날 수 있습니다. 이 경우 EOP 네트워크와 연결 된 보내는 서버 Backscatterer DNS 차단 목록 (이해)에 나열 될 수 있습니다. Backscatterer 이해는 목록 후방 분산 메시지를 보낼 수 있는 IP 주소입니다. 발신자 목록 없으며 Backscatterer 이해에서이 서버를 제거 하려고 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="31277-p102">Backscatter messages are the automated bounce messages that are sent by mail servers, typically as a result of incoming spam. Because Exchange Online Protection (EOP) is a spam filtering service, email messages sent to nonexistent recipients and to other suspicious destinations are rejected by our service. When this happens, EOP generates a non-delivery report (NDR) message and delivers it back to the "sender." Because spammers frequently use a forged or invalid "From" address in their messages, the sender address to which the NDR is sent may result in a backscatter message. When this happens, outgoing servers that are associated with the EOP network may be listed on the Backscatterer DNS Block List (DNSBL). The Backscatterer DNSBL is a list of IP addresses that send backscatter messages. It isn't a spammer list, and we don't try to remove our servers from the Backscatterer DNSBL.</span></span> 
  
> [!TIP]
> <span data-ttu-id="31277-p103">후방 분산 웹 사이트의 지침에 따르면 들어오는 모든 메일에 대해 거부 모드를 사용하는 것은 해당 서비스의 권장 구성 또는 사용 방식이 아닙니다. 대신 안전 모드에서 사용해야 합니다. 올바른 후방 분산 구성을 구현하는 방법에 대한 자세한 내용은 [Backscatterer.org 웹 사이트](http://www.backscatterer.org/?target=usage)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="31277-p103">According to the instructions on the Backscatterer website, the use of reject mode for all incoming mail isn't a recommended configuration or use of that service. It should be used in safe mode instead. For more information about implementing the correct backscatter configuration, visit the [Backscatterer.org website](http://www.backscatterer.org/?target=usage).</span></span> 
  
## <a name="for-more-information"></a><span data-ttu-id="31277-116">자세한 내용</span><span class="sxs-lookup"><span data-stu-id="31277-116">For more information</span></span>

[<span data-ttu-id="31277-117">Backscatterer.org IP 목록</span><span class="sxs-lookup"><span data-stu-id="31277-117">The Backscatterer.org IP list</span></span>](https://blogs.msdn.com/b/tzink/archive/2012/08/22/the-backscatterer-org-ip-list.aspx)
  
<span data-ttu-id="31277-118">[고급 스팸 필터링 옵션에](advanced-spam-filtering-asf-options.md) 있는 항목을 "NDR 후방 분산"를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="31277-118">See the "NDR backscatter" entry in [Advanced spam filtering  options](advanced-spam-filtering-asf-options.md)</span></span>
  

