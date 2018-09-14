---
title: Office 365에서 아웃 바운드 스팸 제어
ms.author: krowley
author: kccross
manager: laurawi
ms.audience: Admin
ms.topic: overview
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 6a601501-a6a8-4559-b2e7-56b59c96a586
description: 조직으로 표시 된 대량 메일 많은 스팸으로 보내는 경우 Office 365를 사용한 전자 메일을 보내지 못하도록 차단 될 수 있습니다. 이 문제가 발생 하는 이유 및 그에 대 한 수행할 수 있는 작업에 대 한 자세한 내용은이 문서를 읽어보십시오.
ms.openlocfilehash: 916a062d08e01954e7736b6f22d297aea04baf28
ms.sourcegitcommit: 17dda7ece5c9e884944a92ac0f842cf1e62ec506
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/14/2018
ms.locfileid: "23977583"
---
# <a name="controlling-outbound-spam-in-office-365"></a><span data-ttu-id="fd37b-104">Office 365에서 아웃 바운드 스팸 제어</span><span class="sxs-lookup"><span data-stu-id="fd37b-104">Controlling outbound spam in Office 365</span></span>

<span data-ttu-id="fd37b-p102">취할 우리는 공유 서비스 때문에 아웃 바운드 스팸을 심각 하 게 관리 합니다.  다 수의 고객 및 리소스에 있는 한 고객 아웃 바운드 스팸 메일을 보내는 경우 해당 서비스의 아웃 바운드 IP 신뢰도 저하 될 수 있습니다 다른 고객에 대 한 전자 메일의 성공적인 스팸과 영향을의 공유 풀 뒤에 있습니다. 고객 B spams 및 다양 한 제 3 자 IP blocklists 것을 사용 하는 IP 주소를 나열 하는 경우에 A 고객에 게 공정 없습니다.</span><span class="sxs-lookup"><span data-stu-id="fd37b-p102">We take managing outbound spam seriously because ours is a shared service.  There are many customers behind a shared pool of resources, where if one customer sends outbound spam, it can degrade the outbound IP reputation of the service and affects the successful deliverability of email for other customers. It is unfair to Customer A if Customer B spams and various 3rd party IP blocklists list the IP address that it uses.</span></span>

## <a name="what-admins-can-do-to-control-outbound-spam"></a><span data-ttu-id="fd37b-108">아웃 바운드 스팸 제어 관리자가 수행할 수 있는 작업</span><span class="sxs-lookup"><span data-stu-id="fd37b-108">What admins can do to control outbound spam</span></span>

- <span data-ttu-id="fd37b-p103">**계정이 보내는 스팸 지 또는 종료 하는 경우 알림을 사용 하도록 설정**합니다. 관리자가 메시지 높은 위험 수준 풀을 통해 보내고 아웃 바운드 스팸으로 표시 때마다 중을 얻을 수 있습니다. 관리자는이 사서함을 모니터링 하 여 자신의 네트워크에서 손상 된 계정 있는지 또는 스팸 필터는 전자 메일에 스팸으로 표시 실수로 하는 경우를 검색할 수 있습니다.  아웃 바운드 스팸 정책 설정에 자세한 정보를 찾을 수 [여기](configure-the-outbound-spam-policy.md)합니다.</span><span class="sxs-lookup"><span data-stu-id="fd37b-p103">**Enable notifications when an account is sending spam or shut down**. Administrators can get bcc’ed whenever a message is marked as outbound spam and sent through the High Risk pool. By monitoring this mailbox, an admin can detect if they have a compromised account in their network or if the spam filter is mistakenly marking their email as spam.  More information on setting up the outbound spam policy can be found [here](configure-the-outbound-spam-policy.md).</span></span>
 
- <span data-ttu-id="fd37b-p104">**수동으로 타사 전자 메일 공급 업체에서 스팸 불만 검토**합니다. 많은 타사 전자 메일 서비스 Outlook.com, yahoo 및 AOL와 같은 위치 스팸으로 서비스에서 전자 메일을 표시 하는 모든 사용자가 서비스에, 하는 경우 메시지 패키지 이며 검토를 위해를 보면 보낸 피드백 루프를 제공 합니다. Outlook.com에 대 한 보낸사람 지원에 대 한 자세한 내용은, 클릭 [여기](https://sendersupport.olc.protection.outlook.com/pm/services.aspx)합니다.</span><span class="sxs-lookup"><span data-stu-id="fd37b-p104">**Manually review spam complaints from 3rd party email providers**. Many 3rd party email services like Outlook.com, Yahoo and AOL provide a Feedback Loop where if any user in their service marks an email from our service as spam, the message is packaged up and sent back to us for review. To learn more about sender support for Outlook.com, click [here](https://sendersupport.olc.protection.outlook.com/pm/services.aspx).</span></span>

## <a name="what-eop-does-to-control-outbound-spam"></a><span data-ttu-id="fd37b-116">아웃 바운드 스팸 제어 EOP 수행 하는 작업</span><span class="sxs-lookup"><span data-stu-id="fd37b-116">What EOP does to control outbound spam</span></span> 

1. <span data-ttu-id="fd37b-p105">**Ip의 별도 풀으로 아웃 바운드 트래픽을 격리**합니다. 고객 서비스를 통해 아웃 바운드 전송 하는 모든 메시지는 스팸에 대 한 검색 됩니다. 메시지가 스팸 인 경우 높은 위험 배달 풀을 통해 라우팅됩니다. 이 IP 풀 배달할 수 없는 상태 알림 및 스팸을 포함 합니다. 많은 제 3 자에서 내보내는 여러 전자 메일의 품질 때문에 전자 메일을 수락 하지 않습니다으로 의도 한 받는 사람에 게 배달 보장 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fd37b-p105">**Segregation of outbound traffic into separate pools of IPs**. Every message that customers send outbound through the service is scanned for spam. If the message is spam, it is routed through the High Risk Delivery pool. This IP pool contains non-deliverable status notifications and spam. Delivery to the intended recipient is not guaranteed as many third parties will not accept email because the quality of email it emits.</span></span>

<span data-ttu-id="fd37b-p106">트래픽이 이러한 방식으로 분할 하면 낮은 품질 전자 메일 (스팸, 후방 분산 하는 Ndr) 일반 아웃 바운드 전자 메일 풀의 신뢰도 아래로 끌어 놓습니다 하지 않습니다. 높은 위험 수준 풀 일반적으로 낮은 신뢰도 인터넷을 중심으로 많은 수신기에서 유니버설은 아니지만 합니다.</span><span class="sxs-lookup"><span data-stu-id="fd37b-p106">Splitting the traffic this way ensures that the lower quality email (spam, backscatter NDRs) does not drag down the reputation of the regular outbound email pools. The high risk pool typically has low reputation at many receivers around the Internet, although this is not universal.</span></span> 

2. <span data-ttu-id="fd37b-p107">**모니터링의 IP 신뢰도**합니다. Office 365 다양 한 제 3 자 IP blocklists를 쿼리하고 사용해 아웃 바운드 Ip 중 하나에 나열 되 면 경고를 생성 합니다. 이 옵션을 사용 하면 스팸 저하를 사용해 신뢰도 유발한 때 신속 하 게 대응 수 있도록 합니다. 알림이 생성 될 때 저희도 잘 외곽 내부 설명서 목록 가져오기 하기 위해 수행 해야할 단계.</span><span class="sxs-lookup"><span data-stu-id="fd37b-p107">**Monitoring of IP reputation**. Office 365 queries various 3rd party IP blocklists and generates alerts if any of our outbound IPs are listed on them. This allows us to react quickly when spam has caused our reputation to degrade. When an alert is generated, we have internal documentation outlying what steps to take to get delisted.</span></span> 

3. <span data-ttu-id="fd37b-p108">**너무 많은 전자 메일을 보낼 때 확인 된 유해한 계정 비활성화 스팸으로 표시**됩니다. 분리 된 스팸 및 스팸이 아닌 별도 두 아웃 바운드 IP 풀으로, 하는 경우에 전자 메일 계정을 스팸 무기한 보낼 수 없습니다. 모니터링 하는 계정은 스팸 보내고 계정이 스팸을 보내지 못하도록 차단 되는 알려지지 않은 한도 초과 하는 경우.</span><span class="sxs-lookup"><span data-stu-id="fd37b-p108">**Disabling of offending accounts when they send too much email marked as spam**. Even though we segregate our spam and non-spam into two separate outbound IP pools,  the email accounts cannot send spam indefinitely. We monitor which accounts are sending spam and if it exceeds an undisclosed limit, the account is blocked from sending spam.</span></span>

<span data-ttu-id="fd37b-p109">단일 메시지에는 스팸 스팸 엔진 및로 알려져 가양성으로 misclassification 수 것으로 표시 합니다. 나가는;의 기회를 제공 하려면 높은 위험 수준 풀을 통해 보내기는 그러나 짧은 시간 내에 메시지 수가 많음 문제 및 발생 하는 것은, 더 많은 모든 전자 메일을 발송에서 계정 차단 했습니다. 전체 테 넌 트에 대 한 집계와 마찬가지로 개별 전자 메일 계정을 설정도 대 한 존재 하는 다른 임계값 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fd37b-p109">A single message marked as spam may be a misclassification by the spam engine and also known as a false positive. We send it through the High Risk pool to give it a chance of going out; however, a large number of messages in a short time frame is indicative of a problem and when that occurs, we block the account from sending any more email. There are different thresholds that exist for individual email accounts as well as in aggregate for the entire tenant.</span></span>

4. <span data-ttu-id="fd37b-p110">**너무 짧은 시간 프레임에서 너무 많은 전자 메일을 보낼 때 확인 된 유해한 계정을 비활성화**합니다. 해당 정보를 스팸으로 표시 된 메시지의 비율에 대 한 위의 제한, 외에도 메시지가 스팸으로 표시 되는 여부에 관계 없이 전체는 제한에 도달한 경우 계정을 차단 하는 제한도 있습니다. 이 제한은 존재 하는 이유 손상 된 계정에서 스팸 필터에 의해 부재중 제로 데가 스팸을 보낼 수 때문입니다. 이기 때문에 어려운 경우가 종종 합법적인 대량 메일 캠페인 및 대규모 스팸 캠페인 간의 차이 구별 하 불가능 모든 피해를 제한 하려면 이러한 제한을 활성화 합니다.</span><span class="sxs-lookup"><span data-stu-id="fd37b-p110">**Disabling of offending accounts when they send too much email in too short a time frame**. In addition to the limits above that look for a proportion of messages marked as spam, there are also limits that block accounts when they reach an overall limit regardless of whether or not the messages are marked as spam. The reason this limit exists is because a compromised account could send zero-day spam that is missed by the spam filter. Because it is difficult, if not impossible, to sometimes tell the difference between a legitimate mass mailing campaign and a massive spam campaign, these limits activate to limit any potential damage.</span></span>

> [!NOTE]
> <span data-ttu-id="fd37b-p111">#3 및 #4 모두에 대 한 정확한 제한 보급 안함 했습니다.  이것이 게임 시스템에서 스팸 방지 하 고 확인 필요한 경우 범위를 변경할 수 있습니다. 제한은 평균 비즈니스 사용자를에서 적중 하지는 않도록 충분히 높은 및 대부분의 스팸 메일을 보낸 수행할 수 있는 손상이 있음을 있을 정도로 낮은.</span><span class="sxs-lookup"><span data-stu-id="fd37b-p111">For both #3 and #4, we do not advertise the exact limits.  This is to prevent spammers from gaming the system and to ensure that we can change the limits when we need to. The limits are high enough such that an average business user will never hit them and low enough that it contains most of the damage a spammer can do.</span></span> 

## <a name="recommended-workarounds-for-customers-who-want-to-send-outbound-a-lot-of-email-through-eop"></a><span data-ttu-id="fd37b-141">아웃 바운드 많은 양의 EOP 통해 전자 메일을 보낼 고객에 대 한 권장된 해결</span><span class="sxs-lookup"><span data-stu-id="fd37b-141">Recommended workarounds for customers who want to send outbound a lot of email through EOP</span></span>

<span data-ttu-id="fd37b-p112">많은 양의 손상 된 계정 및 불량 목록 입수 방식으로 대량 메일에서 서비스를 보호 및 전자 메일을 보내려고 원하는 고객에 게 간의 균형을 두는 것이 어렵습니다. 다시, 제 3 자 blocklist에 방문 하는 아웃 바운드 ip 비용 아웃 바운드 전자 메일을 발송에서 고객을 차단 하는 보다 높습니다. [Exchange Online 서비스 설명](https://technet.microsoft.com/en-us/library/exchange-online-limits.aspx#Receiving and sending limits)에 설명된대로 EOP를 사용 하 여 없는 대량 전자 메일 보내기는 지원 되는 서비스를 사용 하 고 "최상의" 별로 허용 됩니다. 대량 전자 메일을 전송 하지 않으려는 고객에 대 한 다음을 권장 합니다.</span><span class="sxs-lookup"><span data-stu-id="fd37b-p112">It is difficult to strike a balance between customers who want to send a large volume of email vs. protecting the service from compromised accounts and bulk emailers with poor list acquisition practices. Again, the cost of an outbound IP landing on a 3rd party blocklist is higher than blocking a customer from sending outbound email. As described in the [Exchange Online Service Description](https://technet.microsoft.com/en-us/library/exchange-online-limits.aspx#Receiving and sending limits), using EOP to send bulk email is not a supported use of the service and is only permitted on a “best-effort” basis. For customers who do want to send bulk email, we recommend the following:</span></span>

<span data-ttu-id="fd37b-p113">a. **자체 온-프레미스 메일 서버를 통해 대량 전자 메일을 전송**합니다. 즉, 고객이이 유형의 전자 메일에 대 한 자체 전자 메일 인프라를 유지 관리 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="fd37b-p113">a. **Send the bulk email through its own on-premise mail servers**. This means that the customer will have to maintain its own email infrastructure for this type of email.</span></span>

<span data-ttu-id="fd37b-p114">b. **사용 하는 3 자 대량 emailer 대량 통신을 보낼 수**있습니다. 여러 제 3 자 대량 메일 대량 전자 메일을 전송 하는 것이 있는 유일한 비즈니스 있습니다. 좋은 전자 메일 보내기 사례를 포함 하 고 시행 하기 위한 전용 포리스트로 지정 하는 리소스를가지고 있습니다.를 확인 하려면 고객 작업할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fd37b-p114">b. **Use a 3rd party bulk emailer to send the mass communication**. There are several 3rd party bulk emailers whose sole business it is to send bulk email. They can work with customers to ensure that they have good emailing practices and they have resources dedicated to enforcing it.</span></span> 

<span data-ttu-id="fd37b-p115">메시징, 모바일, 맬웨어 방지 오용 작업 그룹 (MAAWG) 해당 멤버 자격 명단에 게시 [여기](http://www.maawg.org/about/roster)합니다. 여러 대량 전자 메일 공급자 목록에 있으며 책임 인터넷 시민 것으로 알려진 합니다.</span><span class="sxs-lookup"><span data-stu-id="fd37b-p115">The Messaging, Mobile, Malware Anti-Abuse Working Group (MAAWG) publishes its membership roster [here](http://www.maawg.org/about/roster). Several bulk email providers are on the list and are known to be responsible Internet citizens.</span></span> 
  
## <a name="for-more-information"></a><span data-ttu-id="fd37b-155">자세한 내용</span><span class="sxs-lookup"><span data-stu-id="fd37b-155">For more information</span></span>

[<span data-ttu-id="fd37b-156">보낸 사람이 보내는 아웃 바운드 스팸 차단 되 면 샘플 알림</span><span class="sxs-lookup"><span data-stu-id="fd37b-156">Sample notification when a sender is blocked sending outbound spam</span></span>](sample-notification-when-a-sender-is-blocked-sending-outbound-spam.md)

[<span data-ttu-id="fd37b-157">Office 365 스팸 방지 보호</span><span class="sxs-lookup"><span data-stu-id="fd37b-157">Office 365 email anti-spam protection</span></span>](anti-spam-protection.md)

[<span data-ttu-id="fd37b-158">Office 365의 스푸핑 방지 보호 기능</span><span class="sxs-lookup"><span data-stu-id="fd37b-158">Anti-spoofing protection in Office 365</span></span>](anti-spoofing-protection.md)

[<span data-ttu-id="fd37b-159">스팸 신뢰 수준</span><span class="sxs-lookup"><span data-stu-id="fd37b-159">Spam confidence levels</span></span>](spam-confidence-levels.md)
