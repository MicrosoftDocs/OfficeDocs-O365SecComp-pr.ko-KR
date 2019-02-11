---
title: Exchange Online Protection 개요
ms.author: tracyp
author: MSFTTracyp
manager: laurawi
ms.date: 01/31/2019
ms.audience: ITPro
ms.topic: overview
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
ms.assetid: 1270a65f-ddc3-4430-b500-4d3a481efb1e
description: Microsoft EOP(Exchange Online Protection)는 스팸 및 맬웨어로부터 조직을 보호하는 클라우드 기반 전자 메일 필터링 서비스로, 메시징 정책 위반으로부터 조직을 보호하는 기능을 포함합니다.
ms.openlocfilehash: 16f2f423b6e517cf204e4b4f6a2949baebfd6223
ms.sourcegitcommit: 7e2a0185cadea7f3a6afc5ddc445eac2e1ce22eb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/11/2019
ms.locfileid: "29686367"
---
# <a name="exchange-online-protection-overview"></a><span data-ttu-id="89b91-103">Exchange Online Protection 개요</span><span class="sxs-lookup"><span data-stu-id="89b91-103">Exchange Online Protection overview</span></span>

<span data-ttu-id="89b91-p101">Microsoft EOP(Exchange Online Protection)는 스팸 및 맬웨어로부터 조직을 보호하는 클라우드 기반 전자 메일 필터링 서비스로, 메시징 정책 위반으로부터 조직을 보호하는 기능을 포함합니다. EOP를 사용하면 메시징 환경을 간편하게 관리할 수 있으며 온-프레미스 하드웨어와 소프트웨어 유지 관리 시의 작업 부담을 상당 부분 덜 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="89b91-p101">Microsoft Exchange Online Protection (EOP) is a cloud-based email filtering service that helps protect your organization against spam and malware, and includes features to safeguard your organization from messaging-policy violations. EOP can simplify the management of your messaging environment and alleviate many of the burdens that come with maintaining on-premises hardware and software.</span></span>
  
<span data-ttu-id="89b91-106">기본적으로 다음과 같은 방식을 통해 메시징 보호에 EOP를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="89b91-106">The following are the primary ways you can use EOP for messaging protection:</span></span>
  
- <span data-ttu-id="89b91-107">**독립 실행형 시나리오에서** EOP는 클라우드 기반 전자 메일 보호 온-프레미스 Microsoft Exchange Server 2013 환경, 레거시 Exchange Server 버전에 대해 또는 모든 기타 온-프레미스에 대 한 SMTP 전자 메일 솔루션을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="89b91-107">**In a standalone scenario** EOP provides cloud-based email protection for your on-premises Microsoft Exchange Server 2013 environment, legacy Exchange Server versions, or for any other on-premises SMTP email solution.</span></span> 
    
- <span data-ttu-id="89b91-108">**Microsoft Exchange Online의 일부로** 기본적으로 EOP는 Microsoft Exchange Online 클라우드 호스팅 사서함을 보호합니다.</span><span class="sxs-lookup"><span data-stu-id="89b91-108">**As a part of Microsoft Exchange Online** By default, EOP protects Microsoft Exchange Online cloud-hosted mailboxes.</span></span> 
    
- <span data-ttu-id="89b91-109">**하이브리드 배포에서** 온-프레미스 사서함과 클라우드 사서함을 함께 사용하는 경우 메시징 환경을 보호하고 메일 라우팅을 제어하도록 EOP를 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="89b91-109">**In a hybrid deployment** EOP can be configured to protect your messaging environment and control mail routing when you have a mix of on-premises and cloud mailboxes.</span></span> 
    
## <a name="how-eop-works"></a><span data-ttu-id="89b91-110">EOP의 작동 방식</span><span class="sxs-lookup"><span data-stu-id="89b91-110">How EOP works</span></span>

<span data-ttu-id="89b91-111">EOP가 받는 전자 메일을 처리하는 방법을 확인하면 EOP의 작동 방식을 이해하는 데 도움이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="89b91-111">To understand how EOP works, it helps to see how it processes incoming email:</span></span>
  
![EOP 전자 메일 처리](../media/EOP-email-processing.png)
  
<span data-ttu-id="89b91-p102">처음 들어오는 메시지 보낸 사람의 신뢰도 검사 하 고 맬웨어에 대 한 메시지를 검사 하는 연결 필터링을 통해 전달 합니다. 대부분의 스팸이 시점에서 중지 이며 EOP에 의해 삭제 됩니다. 정책 필터링 메시지를 만들거나 서식 파일에서 적용 하는 사용자 지정 전송 규칙에 대해 계산 되는 위치를 통해 메시지를 계속 합니다. 예, 특정 사용자가 보낸에서 메일 도착 했을 때 관리자에 게 알림을 전송 하는 규칙을 가질 수 있습니다. (데이터 손실 방지 검사에도 발생할이 시점 기능, 기능 사용 가능 여부에 대 한 정보를 [Exchange Online Protection Service Description](https://go.microsoft.com/fwlink/p/?LinkId=320619)을 참조 하는 경우.) 다음으로 메시지를 전달 콘텐츠 필터링을 통해 콘텐츠를 스팸에 용어 또는 공통 된 속성에 대 한 검사 합니다. 메시지가 스팸 콘텐츠 필터에 의해 사용자의 정크 메일 폴더로 또는 설정에 따라 다른 옵션 중에서 격리를 보낼 수를 결정 합니다. 지나면 메시지 이러한 보호 계층의 모든 성공적으로 받는 사람에 게 배달 됩니다.</span><span class="sxs-lookup"><span data-stu-id="89b91-p102">An incoming message initially passes through connection filtering, which checks the sender's reputation and inspects the message for malware. The majority of spam is stopped at this point and deleted by EOP. Messages continue through policy filtering, where messages are evaluated against custom transport rules that you create or enforce from a template. For example, you can have a rule that sends a notification to a manager when mail arrives from a specific sender. (Data loss prevention checks also occur at this point, if you have that feature; for information about feature availability, see the [Exchange Online Protection Service Description](https://go.microsoft.com/fwlink/p/?LinkId=320619).) Next, messages pass through content filtering, where content is checked for terminology or properties common to spam. A message determined to be spam by the content filter can be sent to a user's Junk Email folder or to the quarantine, among other options, based on your settings. After a message passes all of these protection layers successfully, it's delivered to the recipient.</span></span>
  
### <a name="eop-datacenters"></a><span data-ttu-id="89b91-120">EOP 데이터 센터</span><span class="sxs-lookup"><span data-stu-id="89b91-120">EOP datacenters</span></span>

<span data-ttu-id="89b91-p103">EOP는 최고 수준의 사용 가능성을 제공하도록 설계된 전 세계 데이터 센터 네트워크에서 실행됩니다. 예를 들어 데이터 센터를 사용할 수 없더라도 서비스 중단 없이 전자 메일 메시지가 다른 데이터 센터에 자동으로 라우팅됩니다. 각 데이터 센터의 서버는 사용자 대신 메시지를 수락하여 조직과 인터넷을 분리하는 계층을 제공함으로써 서버의 부하를 줄여 줍니다. 이처럼 가용성이 뛰어난 네트워크를 통해 Microsoft는 전자 메일이 제때에 조직으로 배달되도록 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="89b91-p103">EOP runs on a worldwide network of datacenters that are designed to provide the best availability. For example, if a datacenter becomes unavailable, email messages are automatically routed to another datacenter without any interruption in service. Servers in each datacenter accept messages on your behalf, providing a layer of separation between your organization and the Internet, thereby reducing load on your servers. Through this highly available network, Microsoft can ensure that email reaches your organization in a timely manner.</span></span> 
  
<span data-ttu-id="89b91-p104">EOP는 특정 지역 내에서만 데이터 센터 간 부하 분산을 수행합니다. 단일 지역에서 프로비전되는 경우에는 해당 영역에 대한 메일 라우팅을 사용하여 모든 메시지가 처리됩니다. 다음 목록에는 EOP 데이터 센터에 대한 영역 메일 라우팅의 작동 방식이 나와 있습니다.</span><span class="sxs-lookup"><span data-stu-id="89b91-p104">EOP performs load balancing between datacenters but only within a region. If you're provisioned in one region all your messages will be processed using the mail routing for that region. The following list shows the how regional mail routing works for the EOP datacenters:</span></span>
  
    
- <span data-ttu-id="89b91-128">EMEA(유럽, 중동 및 아프리카)에서는 모든 Exchange Online 사서함이 EMEA 데이터 센터에 있으며 모든 메시지가 EOP 필터링용으로 EMEA 데이터 센터를 통해 라우팅됩니다.</span><span class="sxs-lookup"><span data-stu-id="89b91-128">In Europe, the Middle East, and Africa (EMEA), all Exchange Online mailboxes are located in EMEA datacenters, and all messages are routed through EMEA datacenters for EOP filtering.</span></span>
    
- <span data-ttu-id="89b91-129">아시아 태평양 (APAC), APAC 데이터 센터에서 모든 Exchange Online 사서함이 있어야 하지만 메시지는 현재 EOP 필터링에 대 한 APAC 데이터 센터를 통해 라우팅됩니다.</span><span class="sxs-lookup"><span data-stu-id="89b91-129">In Asia-Pacific (APAC), all Exchange Online mailboxes are located in APAC datacenters, but messages are currently routed through APAC datacenters for EOP filtering.</span></span>
=======
- <span data-ttu-id="89b91-p105">(아메리카), 모든 Exchange Online 사서함 미국 데이터 센터, 남아메리카 데이터 센터 브라질 및 칠레에서 사용 되는 위치를 제외 하 고 및 캐나다의 데이터 센터 캐나다에서 사용 되는 위치에 있습니다. 모든 전자 메일 메시지, 남아메리카 및 캐나다의 경우에 고객에 대 한 메시지를 포함 하 여 EOP 필터링;에 대 한 로컬 데이터 센터를 통해 라우팅됩니다. quaratined 전자 메일 테 넌 트 위치한 데이터 센터에 저장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="89b91-p105">In the Americas, all Exchange Online mailboxes are located in U.S. datacenters, with the exception of South America where datacenters in Brazil and Chile are used and in Canada where datacenters in Canada are used. All email messages, including messages for customers in South America and Canada, are routed through local datacenters for EOP filtering; quaratined email is stored in the datacenter where the tenant is located.</span></span>
    
- <span data-ttu-id="89b91-132">EMEA(유럽, 중동 및 아프리카)에서는 모든 Exchange Online 사서함이 EMEA 데이터 센터에 있으며 모든 메시지가 EOP 필터링용으로 EMEA 데이터 센터를 통해 라우팅됩니다.</span><span class="sxs-lookup"><span data-stu-id="89b91-132">In Europe, the Middle East, and Africa (EMEA), all Exchange Online mailboxes are located in EMEA datacenters, and all messages are routed through EMEA datacenters for EOP filtering.</span></span>
    
- <span data-ttu-id="89b91-133">아시아 태평양 (APAC), APAC 데이터 센터에서 모든 Exchange Online 사서함이 있는 및 메시지에 현재 EOP 필터링에 대 한 APAC 데이터 센터를 통해 라우팅됩니다.</span><span class="sxs-lookup"><span data-stu-id="89b91-133">In Asia-Pacific (APAC), all Exchange Online mailboxes are located in APAC datacenters, and messages are currently routed through APAC datacenters for EOP filtering.</span></span>
    
- <span data-ttu-id="89b91-134">GCC(정부 커뮤니티 클라우드)의 경우에는 모든 Exchange Online 사서함이 미국 데이터 센터에 있으며 모든 메시지는 EOP 필터링용으로 미국 데이터 센터를 통해 라우팅됩니다.</span><span class="sxs-lookup"><span data-stu-id="89b91-134">For the Government Community Cloud (GCC), all Exchange Online mailboxes are located in U.S. datacenters and all messages are routed through U.S. datacenters for EOP filtering.</span></span>
    
## <a name="eop-plans-and-features"></a><span data-ttu-id="89b91-135">EOP 계획 및 기능</span><span class="sxs-lookup"><span data-stu-id="89b91-135">EOP plans and features</span></span>

<span data-ttu-id="89b91-136">다음은 사용 가능한 EOP 구독 계획입니다.</span><span class="sxs-lookup"><span data-stu-id="89b91-136">The following are the available EOP subscription plans:</span></span>
  
- <span data-ttu-id="89b91-137">**EOP 독립 실행형** EOP가 온-프레미스 사서함을 보호합니다.</span><span class="sxs-lookup"><span data-stu-id="89b91-137">**EOP standalone** Where EOP protects your on-premises mailboxes.</span></span> 
    
- <span data-ttu-id="89b91-138">**Exchange Online의 EOP 기능** EOP가 Exchange Online 클라우드 호스팅 사서함을 보호합니다.</span><span class="sxs-lookup"><span data-stu-id="89b91-138">**EOP features in Exchange Online** Where EOP protects your Exchange Online cloud-hosted mailboxes.</span></span> 
    
- <span data-ttu-id="89b91-139">**Exchange Enterprise CAL with Services** EOP가 EOP 독립 실행형과 마찬가지로 온-프레미스 사서함을 보호하고 웹 서비스를 사용한 DLP(데이터 손실 방지) 및 보고 기능이 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="89b91-139">**Exchange Enterprise CAL with Services** Where EOP protects your on-premises mailboxes, like EOP standalone, and includes data loss prevention (DLP) and reporting using web services.</span></span> 
    
<span data-ttu-id="89b91-140">모든 EOP 구독 계획의 요구 사항, 중요 제한 및 기능 가용성에 대한 자세한 내용은 [Exchange Online Protection 서비스 설명](https://go.microsoft.com/fwlink/p/?LinkId=320619)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="89b91-140">For information about requirements, important limits, and feature availability across all EOP subscription plans, see the [Exchange Online Protection Service Description](https://go.microsoft.com/fwlink/p/?LinkId=320619).</span></span>
  
## <a name="setting-up-eop"></a><span data-ttu-id="89b91-141">EOP 설정</span><span class="sxs-lookup"><span data-stu-id="89b91-141">Setting up EOP</span></span>

<span data-ttu-id="89b91-p106">EOP는 간단하게 설정할 수 있으며, 특히 준수 규칙이 많지 않은 소규모 조직의 경우에는 더욱 그렇습니다. 그러나 도메인이 여러 개이거나 사용자 지정 준수 규칙 또는 하이브리드 메일 흐름을 사용하는 대규모 조직의 경우에는 EOP 설정에 더 많은 시간과 계획이 필요할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="89b91-p106">Setting up EOP can be simple, especially in the case of a small organization with a handful of compliance rules. However, if you have a large organization with multiple domains, custom compliance rules, or hybrid mail flow, set up can take more planning and time.</span></span>
  
<span data-ttu-id="89b91-144">EOP를 이미 구입한 경우 [EOP 서비스 설정](set-up-your-eop-service.md)을 참조하여 메시징 환경을 보호하도록 EOP를 구성하는 데 필요한 모든 단계를 완료하십시오.</span><span class="sxs-lookup"><span data-stu-id="89b91-144">If you've already purchased EOP, see [Set up your EOP service](set-up-your-eop-service.md) to ensure that you complete all the steps necessary to configure EOP to protect your messaging environment.</span></span> 
  
## <a name="for-more-information"></a><span data-ttu-id="89b91-145">자세한 내용</span><span class="sxs-lookup"><span data-stu-id="89b91-145">For more information</span></span>

[<span data-ttu-id="89b91-146">EOP 기능</span><span class="sxs-lookup"><span data-stu-id="89b91-146">EOP features</span></span>](eop-features.md)
  
[<span data-ttu-id="89b91-147">EOP 시작을 위한 비디오</span><span class="sxs-lookup"><span data-stu-id="89b91-147">Videos for getting started with EOP</span></span>](videos-for-getting-started-with-eop.md)
  
[<span data-ttu-id="89b91-148">EOP 관련 일반 FAQ(질문과 대답)</span><span class="sxs-lookup"><span data-stu-id="89b91-148">EOP general FAQ</span></span>](eop-general-faq.md)
  
[<span data-ttu-id="89b91-149">EOP 대기, 지연 및 반송 메시지 FAQ</span><span class="sxs-lookup"><span data-stu-id="89b91-149">EOP queued, deferred, and bounced messages FAQ</span></span>](eop-queued-deferred-and-bounced-messages-faq.md)
  
[<span data-ttu-id="89b91-150">위임된 관리 FAQ</span><span class="sxs-lookup"><span data-stu-id="89b91-150">Delegated administration FAQ</span></span>](delegated-administration-faq.md)
  
[<span data-ttu-id="89b91-151">EOP 조직 간에 도메인 및 설정 이동</span><span class="sxs-lookup"><span data-stu-id="89b91-151">Move domains and settings from one EOP organization to another EOP organization</span></span>](move-domains-and-settings-from-one-eop-organization-to-another-eop-organization.md)
  

