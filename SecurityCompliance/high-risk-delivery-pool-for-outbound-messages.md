---
title: 아웃 바운드 메시지에 대 한 위험성이 높은 배달 풀
ms.author: tracyp
author: MSFTTracyP
manager: dansimp
ms.date: 8/24/2016
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: ac11edd9-2da3-462d-8ea3-bbf9dbc6f948
ms.collection:
- M365-security-compliance
description: 고객의 전자 메일 시스템이 맬웨어 또는 악성 스팸 공격에 의해 손상 되 고 호스팅된 필터링 서비스를 통해 아웃 바운드 스팸 메일을 보내는 경우이로 인해 타사 블록에 나열 되는 Office 365 데이터 센터 서버의 IP 주소가 생성 될 수 있습니다. 주고.
ms.openlocfilehash: 5b9241dead5b40e9f216ecd3023d6f8b86fb0205
ms.sourcegitcommit: 32ecff689ae32c59a39b7633ca0f36a304e7516e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/09/2019
ms.locfileid: "35599165"
---
# <a name="high-risk-delivery-pool-for-outbound-messages"></a><span data-ttu-id="015bf-103">아웃 바운드 메시지에 대 한 위험성이 높은 배달 풀</span><span class="sxs-lookup"><span data-stu-id="015bf-103">High-risk delivery pool for outbound messages</span></span>

<span data-ttu-id="015bf-104">고객의 전자 메일 시스템이 맬웨어 또는 악성 스팸 공격에 의해 손상 되 고 호스팅된 필터링 서비스를 통해 아웃 바운드 스팸 메일을 보내는 경우이로 인해 타사 블록에 나열 되는 Office 365 데이터 센터 서버의 IP 주소가 생성 될 수 있습니다. 주고.</span><span class="sxs-lookup"><span data-stu-id="015bf-104">When a customer's email system has been compromised by malware or a malicious spam attack, and it's sending outbound spam through the hosted filtering service, this can result in the IP addresses of the Office 365 data center servers being listed on third-party block lists.</span></span> <span data-ttu-id="015bf-105">호스트 필터링 서비스를 사용 하지 않지만 이러한 차단 목록을 사용 하 여 해당 목록에 추가 된 호스트 필터링 IP 주소에서 보낸 모든 전자 메일은 거부 하는 대상 서버입니다.</span><span class="sxs-lookup"><span data-stu-id="015bf-105">Destination servers that do not use the hosted filtering service, but do use these block lists, reject all email sent from any of the hosted filtering IP addresses that have been added to those lists.</span></span> <span data-ttu-id="015bf-106">이를 방지 하기 위해 스팸 임계값을 초과 하는 모든 아웃 바운드 메시지는 위험성이 높은 배달 풀을 통해 전송 됩니다.</span><span class="sxs-lookup"><span data-stu-id="015bf-106">To prevent this, all outbound messages that exceed the spam threshold are sent through a high-risk delivery pool.</span></span> <span data-ttu-id="015bf-107">이 보조 아웃 바운드 전자 메일 풀은 저품질 일 수 있는 메시지를 보내는 데만 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="015bf-107">This secondary outbound email pool is only used to send messages that may be of low quality.</span></span> <span data-ttu-id="015bf-108">이렇게 하면 네트워크의 나머지 부분에서 보내는 IP 주소가 차단 될 가능성이 높은 메시지가 전송 되지 않도록 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="015bf-108">This helps to protect the rest of the network from sending messages that are more likely to result in the sending IP address being blocked.</span></span>
  
<span data-ttu-id="015bf-109">전용 위험성이 높은 배달 풀을 사용 하면 일반 아웃 바운드 풀이 높은 품질로 알려진 메시지만 보낼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="015bf-109">The use of a dedicated high-risk delivery pool helps ensure that the normal outbound pool is only sending messages that are known to be of a high-quality.</span></span> <span data-ttu-id="015bf-110">이 보조 IP 풀을 사용 하면 일반 아웃 바운드 IP 풀이 차단 된 목록에 추가 될 가능성을 줄일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="015bf-110">Using this secondary IP pool helps to reduce the probability of the normal outbound-IP pool being added to a blocked list.</span></span> <span data-ttu-id="015bf-111">위험성이 높은 배달 풀이 차단 된 목록에 포함 될 가능성은 여전히 위험에 노출 됩니다.</span><span class="sxs-lookup"><span data-stu-id="015bf-111">The possibility of the high-risk delivery pool being placed on a blocked list remains a risk.</span></span> <span data-ttu-id="015bf-112">이는 설계에 따른 것입니다.</span><span class="sxs-lookup"><span data-stu-id="015bf-112">This is by design.</span></span>
  
<span data-ttu-id="015bf-113">보내는 도메인에 도메인의 IP 주소를 제공 하는 주소 레코드 (A 레코드) 및 DNS의 특정 도메인에 대 한 메일을 받아야 하는 서버로 메일을 보낼 수 있도록 하는 MX 레코드가 없는 메시지는 항상 스팸 처리에 관계 없이 위험성이 높은 배달 풀</span><span class="sxs-lookup"><span data-stu-id="015bf-113">Messages where the sending domain has no address record (A record), which gives you the IP address of the domain, and no MX record, which helps direct mail to the servers that should receive the mail for a particular domain in the DNS, are always routed through the high-risk delivery pool regardless of their spam disposition.</span></span>
  
## <a name="understanding-delivery-status-notification-dsn-messages"></a><span data-ttu-id="015bf-114">DSN (배달 상태 알림) 메시지 이해</span><span class="sxs-lookup"><span data-stu-id="015bf-114">Understanding Delivery Status Notification (DSN) messages</span></span>

<span data-ttu-id="015bf-115">아웃 바운드 높은 위험 배달 풀은 모든 "반송" 또는 "실패" (DSN) 메시지의 배달을 관리 합니다.</span><span class="sxs-lookup"><span data-stu-id="015bf-115">The outbound high-risk delivery pool manages the delivery for all "bounced" or "failed" (DSN) messages.</span></span>
  
<span data-ttu-id="015bf-116">DSN 메시지가 갑자기 증가하는 경우의 가능한 원인은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="015bf-116">Possible causes for a surge in DSN messages include the following:</span></span>
  
- <span data-ttu-id="015bf-117">서비스 사용 고객 중 한 명에게 영향을 주는 스푸핑 캠페인</span><span class="sxs-lookup"><span data-stu-id="015bf-117">A spoofing campaign affecting one of the customers using the service</span></span>
    
- <span data-ttu-id="015bf-118">디렉터리 수집 공격</span><span class="sxs-lookup"><span data-stu-id="015bf-118">A directory harvest attack</span></span>
    
- <span data-ttu-id="015bf-119">스팸 공격</span><span class="sxs-lookup"><span data-stu-id="015bf-119">A spam attack</span></span>
    
- <span data-ttu-id="015bf-120">Rogue SMTP 서버</span><span class="sxs-lookup"><span data-stu-id="015bf-120">A rogue SMTP server</span></span>
    
<span data-ttu-id="015bf-121">이러한 모든 문제로 인해 서비스에서 처리하는 DSN 메시지의 수가 급증할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="015bf-121">All of these issues can result in a sudden increase in the number of DSN messages being processed by the service.</span></span> <span data-ttu-id="015bf-122">대부분의 경우 이러한 DSN 메시지는 다른 전자 메일 서버 및 서비스에 스팸으로 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="015bf-122">Many times, these DSN messages appear to be spam to other email servers and services.</span></span>
  
## <a name="for-more-information"></a><span data-ttu-id="015bf-123">자세한 내용</span><span class="sxs-lookup"><span data-stu-id="015bf-123">For more information</span></span>

[<span data-ttu-id="015bf-124">아웃바운드 스팸 정책 구성</span><span class="sxs-lookup"><span data-stu-id="015bf-124">Configure the outbound spam policy</span></span>](configure-the-outbound-spam-policy.md)
  
[<span data-ttu-id="015bf-125">스팸 방지 보호 기능 FAQ</span><span class="sxs-lookup"><span data-stu-id="015bf-125">Anti-spam protection FAQ</span></span>](anti-spam-protection-faq.md)
  

