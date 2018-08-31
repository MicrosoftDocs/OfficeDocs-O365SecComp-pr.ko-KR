---
title: 아웃 바운드 메시지 용 위험성이 높은 배달 풀
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 8/24/2016
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: ac11edd9-2da3-462d-8ea3-bbf9dbc6f948
description: 맬웨어 또는 악의적인 스팸 공격을 여는 고객의 전자 메일 시스템 암호가 손상 된 호스팅된 필터링 서비스를 통해 아웃 바운드 스팸 발송 하는 경우이 될 수 있습니다 제 3 자 블록에 나열 되는 Office 365 데이터 센터 서버의 IP 주소 나열합니다.
ms.openlocfilehash: 69548488f70944a319a449bfc4ac1cb1bffd7b1c
ms.sourcegitcommit: e9dca2d6a7838f98bb7eca127fdda2372cda402c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/21/2018
ms.locfileid: "23003137"
---
# <a name="high-risk-delivery-pool-for-outbound-messages"></a><span data-ttu-id="2e8d7-103">아웃 바운드 메시지 용 위험성이 높은 배달 풀</span><span class="sxs-lookup"><span data-stu-id="2e8d7-103">High-risk delivery pool for outbound messages</span></span>

<span data-ttu-id="2e8d7-p101">맬웨어 또는 악의적인 스팸 공격을 여는 고객의 전자 메일 시스템 암호가 손상 된 호스팅된 필터링 서비스를 통해 아웃 바운드 스팸 발송 하는 경우이 될 수 있습니다 제 3 자 블록에 나열 되는 Office 365 데이터 센터 서버의 IP 주소 나열합니다. 수행 하는 대상 서버 하지 호스팅된 필터링 서비스를 사용 하지만 수행 이러한 차단 목록을 사용 하 여, 모든 해당 목록에 추가 된 호스팅된 필터링 IP 주소에서 보낸 모든 전자 메일을 거부 합니다. 이 방지 하려면 위험성이 높은 배달 풀을 통해 스팸 임계값을 초과 하는 모든 아웃 바운드 메시지 전송 됩니다. 이 보조 아웃 바운드 전자 메일 풀 저품질 유용할 수 있는 메시지를 보낼 수만 사용 됩니다. 이 네트워크의 나머지 부분을 차단 하 고 보내는 IP 주소에서 발생 하는 메시지를 보내지 못하도록 보호할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2e8d7-p101">When a customer's email system has been compromised by malware or a malicious spam attack, and it's sending outbound spam through the hosted filtering service, this can result in the IP addresses of the Office 365 data center servers being listed on third-party block lists. Destination servers that do not use the hosted filtering service, but do use these block lists, reject all email sent from any of the hosted filtering IP addresses that have been added to those lists. To prevent this, all outbound messages that exceed the spam threshold are sent through a high-risk delivery pool. This secondary outbound email pool is only used to send messages that may be of low quality. This helps to protect the rest of the network from sending messages that are more likely to result in the sending IP address being blocked.</span></span>
  
<span data-ttu-id="2e8d7-p102">기본 아웃 바운드 풀 높은 품질의 것으로 알려진 된 메시지를 보내지만 전용된 위험성이 높은 배달 풀을 사용 하면. 이 보조 IP 풀을 사용 하 여 차단된 목록에 추가 되는 기본 아웃 바운드 IP 풀의 확률을 줄일 수 있습니다. 차단된 목록에 배치 되 고 위험성이 높은 배달 풀의 가능성을 사전에는 위험 유지 됩니다. 의도적인 것입니다.</span><span class="sxs-lookup"><span data-stu-id="2e8d7-p102">The use of a dedicated high-risk delivery pool helps ensure that the normal outbound pool is only sending messages that are known to be of a high-quality. Using this secondary IP pool helps to reduce the probability of the normal outbound-IP pool being added to a blocked list. The possibility of the high-risk delivery pool being placed on a blocked list remains a risk. This is by design.</span></span>
  
<span data-ttu-id="2e8d7-113">보내는 도메인의 도메인의 IP 주소를 제공 하는 없는 주소 record (레코드) 및 DNS에서 특정 도메인에 대 한 메일을 수신 해야 하는 서버에 직접 메일을 사용 하면, MX 레코드가 없습니다 사람이 없는 메시지를 통해 항상 라우팅되는 스팸 대비한에 관계 없이 위험성이 높은 배달 풀입니다.</span><span class="sxs-lookup"><span data-stu-id="2e8d7-113">Messages where the sending domain has no address record (A record), which gives you the IP address of the domain, and no MX record, which helps direct mail to the servers that should receive the mail for a particular domain in the DNS, are always routed through the high-risk delivery pool regardless of their spam disposition.</span></span>
  
## <a name="understanding-delivery-status-notification-dsn-messages"></a><span data-ttu-id="2e8d7-114">배달 상태 알림 (DSN) 메시지 이해 (영문)</span><span class="sxs-lookup"><span data-stu-id="2e8d7-114">Understanding Delivery Status Notification (DSN) messages</span></span>

<span data-ttu-id="2e8d7-115">아웃 바운드 위험성이 높은 배달 풀은 모든 "반송 됨" 또는 "실패" (DSN) 메시지 배달을 관리합니다.</span><span class="sxs-lookup"><span data-stu-id="2e8d7-115">The outbound high-risk delivery pool manages the delivery for all "bounced" or "failed" (DSN) messages.</span></span>
  
<span data-ttu-id="2e8d7-116">DSN 메시지가 갑자기 증가하는 경우의 가능한 원인은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="2e8d7-116">Possible causes for a surge in DSN messages include the following:</span></span>
  
- <span data-ttu-id="2e8d7-117">서비스 사용 고객 중 한 명에게 영향을 주는 스푸핑 캠페인</span><span class="sxs-lookup"><span data-stu-id="2e8d7-117">A spoofing campaign affecting one of the customers using the service</span></span>
    
- <span data-ttu-id="2e8d7-118">디렉터리 수집 공격</span><span class="sxs-lookup"><span data-stu-id="2e8d7-118">A directory harvest attack</span></span>
    
- <span data-ttu-id="2e8d7-119">스팸 공격</span><span class="sxs-lookup"><span data-stu-id="2e8d7-119">A spam attack</span></span>
    
- <span data-ttu-id="2e8d7-120">Rogue SMTP 서버</span><span class="sxs-lookup"><span data-stu-id="2e8d7-120">A rogue SMTP server</span></span>
    
<span data-ttu-id="2e8d7-p103">이러한 문제는 모든 서비스에 의해 처리 중인 DSN 메시지의 수에 갑자기 증가 하는 될 수 있습니다. 여러 번 반복, 이러한 DSN 메시지는 다른 전자 메일 서버 및 서비스에 대 한 스팸 것 같습니다.</span><span class="sxs-lookup"><span data-stu-id="2e8d7-p103">All of these issues can result in a sudden increase in the number of DSN messages being processed by the service. Many times, these DSN messages appear to be spam to other email servers and services.</span></span>
  
## <a name="for-more-information"></a><span data-ttu-id="2e8d7-123">자세한 내용</span><span class="sxs-lookup"><span data-stu-id="2e8d7-123">For more information</span></span>

[<span data-ttu-id="2e8d7-124">아웃바운드 스팸 정책 구성</span><span class="sxs-lookup"><span data-stu-id="2e8d7-124">Configure the outbound spam policy</span></span>](configure-the-outbound-spam-policy.md)
  
[<span data-ttu-id="2e8d7-125">스팸 방지 보호 FAQ</span><span class="sxs-lookup"><span data-stu-id="2e8d7-125">Anti-spam protection FAQ</span></span>](anti-spam-protection-faq.md)
  

