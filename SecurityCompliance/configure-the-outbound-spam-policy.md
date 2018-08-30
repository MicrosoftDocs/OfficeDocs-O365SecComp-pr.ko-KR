---
title: 아웃 바운드 스팸 정책 구성
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 11/10/2016
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: a44764e9-a5d2-4c67-8888-e7fb871c17c7
description: 아웃바운드 전자 메일 보내기 서비스를 사용하는 경우 아웃바운드 스팸 필터링이 항상 사용하도록 설정되므로 서비스와 받는 사람을 사용하여 조직을 보호할 수 있습니다.
ms.openlocfilehash: b6185cfded28613cb5a512882aefb1a99db158db
ms.sourcegitcommit: e9dca2d6a7838f98bb7eca127fdda2372cda402c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/21/2018
ms.locfileid: "23002422"
---
# <a name="configure-the-outbound-spam-policy"></a><span data-ttu-id="ad182-103">아웃 바운드 스팸 정책 구성</span><span class="sxs-lookup"><span data-stu-id="ad182-103">Configure the outbound spam policy</span></span>

<span data-ttu-id="ad182-p101">아웃바운드 전자 메일 보내기 서비스를 사용하는 경우 아웃바운드 스팸 필터링이 항상 사용하도록 설정되므로 서비스와 받는 사람을 사용하여 조직을 보호할 수 있습니다. 인바운드 필터링과 마찬가지로 아웃바운드 스팸 필터링도 연결 필터링과 콘텐츠 필터링으로 구성되지만, 아웃바운드 필터 설정은 구성할 수 없습니다. 스팸으로 확인된 아웃바운드 메시지는 위험성이 높은 배달 풀을 통해 라우팅되므로 일반 아웃바운드 IP 풀이 차단 목록에 추가될 가능성이 줄어듭니다. 서비스를 통해 아웃바운드 스팸을 계속 보내는 고객에 대해서는 메시지 보내기가 차단됩니다. 아웃바운드 스팸 필터링을 사용하지 않도록 설정하거나 변경할 수는 없지만 기본 아웃바운드 스팸 정책을 통해 다양한 회사 전체 아웃바운드 스팸 설정을 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ad182-p101">Outbound spam filtering is always enabled if you use the service for sending outbound email, thereby protecting organizations using the service and their intended recipients. Similar to inbound filtering, outbound spam filtering is comprised of connection filtering and content filtering, however the outbound filter settings are not configurable. If an outbound message is determined to be spam, it is routed through the higher risk delivery pool, which reduces the probability of the normal outbound-IP pool being added to a block list. If a customer continues to send outbound spam through the service, they will be blocked from sending messages. Although outbound spam filtering cannot be disabled or changed, you can configure several company-wide outbound spam settings via the default outbound spam policy.</span></span> 
  
<span data-ttu-id="ad182-109">다음 비디오에서는 아웃바운드 스팸 정책을 구성하는 방법을 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="ad182-109">The following video shows how to configure the outbound spam policy:</span></span>
  
> [!VIDEO https://www.microsoft.com/videoplayer/embed/1f20d655-0d3d-4141-9cae-e57f5a6cffe8?autoplay=false]
  
## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="ad182-110">시작하기 전에 알아야 할 내용</span><span class="sxs-lookup"><span data-stu-id="ad182-110">What do you need to know before you begin?</span></span>
<span data-ttu-id="ad182-111"><a name="sectionSection0"> </a></span><span class="sxs-lookup"><span data-stu-id="ad182-111"></span></span>

<span data-ttu-id="ad182-112">예상 완료 시간: 5분</span><span class="sxs-lookup"><span data-stu-id="ad182-112">Estimated time to complete: 5 minutes</span></span>
  
<span data-ttu-id="ad182-p102">이 절차를 수행 하기 전에 사용 권한을 할당 해야 합니다. 필요한 사용 권한을 참조 하십시오 [Exchange Online의 기능 사용 권한](http://technet.microsoft.com/library/15073ce1-0917-403b-8839-02a2ebc96e16.aspx) 항목의 스팸 방지 항목".</span><span class="sxs-lookup"><span data-stu-id="ad182-p102">You need to be assigned permissions before you can perform this procedure or procedures. To see what permissions you need, see the "Anti-spam entry in the [Feature Permissions in Exchange Online](http://technet.microsoft.com/library/15073ce1-0917-403b-8839-02a2ebc96e16.aspx) topic.</span></span> 
  
<span data-ttu-id="ad182-115">이 항목의 절차에 적용할 수 있는 바로 가기 키에 대한 자세한 내용은 **Exchange 관리 센터의 바로 가기 키**을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="ad182-115">For information about keyboard shortcuts that may apply to the procedures in this topic, see **Keyboard shortcuts in the Exchange admin center**.</span></span>
  
<span data-ttu-id="ad182-p103">원격 PowerShell을 통해 다음 절차를 수행할 수도 있습니다. 검토 하 여 설정과 아웃 바운드 스팸 정책 설정을 편집 하려면 [집합 HostedOutboundSpamFilterPolicy](http://technet.microsoft.com/library/665d1b04-d4b5-4a0e-811a-4e37096ccbfd.aspx) [Get HostedOutboundSpamFilterPolicy](http://technet.microsoft.com/library/8f15c83c-c10a-4d9d-b135-35321430bdc2.aspx) cmdlet을 사용 합니다. Exchange Online Protection에 연결 하려면 Windows PowerShell을 사용 하는 방법을 알아보려면 [Connect to Exchange Online Protection PowerShell를](https://go.microsoft.com/fwlink/p/?linkid=627290)참조 하십시오. Exchange Online에 연결 하려면 Windows PowerShell을 사용 하는 방법을 알아보려면 [Exchange Online PowerShell 연결](https://go.microsoft.com/fwlink/p/?linkid=396554)을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="ad182-p103">The following procedure can also be performed via remote PowerShell. Use the [Get-HostedOutboundSpamFilterPolicy](http://technet.microsoft.com/library/8f15c83c-c10a-4d9d-b135-35321430bdc2.aspx) cmdlet to review your settings, and the [Set-HostedOutboundSpamFilterPolicy](http://technet.microsoft.com/library/665d1b04-d4b5-4a0e-811a-4e37096ccbfd.aspx) to edit your outbound spam policy settings. To learn how to use Windows PowerShell to connect to Exchange Online Protection, see [Connect to Exchange Online Protection PowerShell](https://go.microsoft.com/fwlink/p/?linkid=627290). To learn how to use Windows PowerShell to connect to Exchange Online, see [Connect to Exchange Online PowerShell](https://go.microsoft.com/fwlink/p/?linkid=396554).</span></span>
  
## <a name="use-the-eac-to-edit-the-default-outbound-spam-policy"></a><span data-ttu-id="ad182-120">EAC를 사용하여 기본 아웃바운드 스팸 정책 편집</span><span class="sxs-lookup"><span data-stu-id="ad182-120">Use the EAC to edit the default outbound spam policy</span></span>
<span data-ttu-id="ad182-121"><a name="sectionSection1"> </a></span><span class="sxs-lookup"><span data-stu-id="ad182-121"></span></span>

<span data-ttu-id="ad182-122">다음 절차에 따라 기본 아웃바운드 스팸 정책을 편집합니다.</span><span class="sxs-lookup"><span data-stu-id="ad182-122">Use the following procedure to edit the default outbound spam policy:</span></span>
  
### <a name="to-configure-the-default-outbound-spam-policy"></a><span data-ttu-id="ad182-123">기본 아웃바운드 스팸 정책을 구성하려면 다음을 수행합니다.</span><span class="sxs-lookup"><span data-stu-id="ad182-123">To configure the default outbound spam policy</span></span>

1. <span data-ttu-id="ad182-124">EAC(Exchange 관리 센터)에서 **보호** \> **아웃바운드 스팸**으로 이동한 다음 기본 정책을 두 번 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="ad182-124">In the Exchange admin center (EAC), navigate to **Protection** \> **Outbound spam**, and then double-click the default policy.</span></span>
    
2. <span data-ttu-id="ad182-125">**아웃바운드 스팸 기본 설정** 메뉴 옵션을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="ad182-125">Select the **Outbound spam preferences** menu option.</span></span> 
    
3. <span data-ttu-id="ad182-126">아웃바운드 메시지와 관련된 다음 확인란을 선택하고 함께 제공되는 입력란에 연관된 전자 메일 주소를 하나 이상 지정합니다. 전자 메일 주소가 유효한 SMTP 대상으로 확인되는 경우에는 메일 그룹을 입력할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ad182-126">Select the following check boxes pertaining to outbound messages, and then specify an associated email address or addresses in the accompanying input box (these can be distribution lists if they resolve as valid SMTP destinations):</span></span>
    
1. <span data-ttu-id="ad182-p104">**의심스러운 모든 아웃바운드 전자 메일 메시지의 복사본을 다음 전자 메일 주소로 보내기**. 이러한 메시지는 SCL 등급에 관계없이 필터에 의해 스팸으로 표시되며, 필터에서 거부되지는 않지만 위험성이 높은 배달 풀을 통해 라우팅됩니다. 주소가 여러 개인 경우 세미콜론으로 구분합니다. 지정된 받는 사람은 보낸 사람 및 받는 사람 필드에 원래 보낸 사람 및 받는 사람이 표시되는 Bcc(숨은 참조) 주소로 메시지를 받습니다.</span><span class="sxs-lookup"><span data-stu-id="ad182-p104">**Send a copy of all suspicious outbound email messages to the following email address or addresses**. These are messages that are marked as spam by the filter (regardless of the SCL rating). They are not rejected by the filter but are routed through the higher risk delivery pool. Separate multiple addresses with a semicolon. Note that the recipients specified will receive the messages as a Blind carbon copy (Bcc) address (the From and To fields are the original sender and recipient).</span></span>
    
2. <span data-ttu-id="ad182-p105">**보낸 사람이 아웃바운드 스팸을 보낼 수 없도록 차단된 경우 다음 전자 메일 주소로 알림 보내기**. 주소가 여러 개인 경우 세미콜론으로 구분합니다.</span><span class="sxs-lookup"><span data-stu-id="ad182-p105">**Send a notification to the following email address when a sender is blocked sending outbound spam**. Separate multiple addresses with a semicolon.</span></span>
    
    <span data-ttu-id="ad182-p106">많은 양의 스팸에서 특정 사용자에 게 서 들어오는 때 전자 메일 메시지를 보내지 못하도록 사용할 수 없습니다. 이 설정을 사용 하 여 지정 된 도메인에 대 한 관리자는이 사용자에 대 한 아웃 바운드 메시지 차단 되는 알림을 받게 됩니다. 이 알림이 표시 되는 모양의 참조 [샘플 알림을 보낸 사람이 보내는 아웃 바운드 스팸 차단 되 면](sample-notification-when-a-sender-is-blocked-sending-outbound-spam.md). 사용할 다시 시작 하는 방법에 대 한 정보를 [사용자, 도메인 또는 IP 주소 스팸 전자 메일을 보낸 후 차단 목록에서 제거](http://technet.microsoft.com/library/712cfcc1-31e8-4e51-8561-b64258a8f1e5.aspx)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="ad182-p106">When a significant amount of spam is originating from a particular user, the user is disabled from sending email messages. The administrator for the domain, who is specified using this setting, will be informed that outbound messages are blocked for this user. To see what this notification looks like, see [Sample notification when a sender is blocked sending outbound spam](sample-notification-when-a-sender-is-blocked-sending-outbound-spam.md). For information about getting re-enabled, see [Removing a user, domain, or IP address from a block list after sending spam email](http://technet.microsoft.com/library/712cfcc1-31e8-4e51-8561-b64258a8f1e5.aspx).</span></span>
    
4. <span data-ttu-id="ad182-p107">**저장**을 클릭합니다. 기본 정책 설정에 대한 요약이 오른쪽 창에 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="ad182-p107">Click **save**. A summary of your default policy settings appears in the right pane.</span></span>
    
## <a name="for-more-information"></a><span data-ttu-id="ad182-140">자세한 내용</span><span class="sxs-lookup"><span data-stu-id="ad182-140">For more information</span></span>
<span data-ttu-id="ad182-141"><a name="sectionSection2"> </a></span><span class="sxs-lookup"><span data-stu-id="ad182-141"></span></span>

[<span data-ttu-id="ad182-142">아웃 바운드 메시지 용 위험성이 높은 배달 풀</span><span class="sxs-lookup"><span data-stu-id="ad182-142">High-risk delivery pool for outbound messages</span></span>](high-risk-delivery-pool-for-outbound-messages.md)
  
[<span data-ttu-id="ad182-143">스팸 방지 보호 FAQ</span><span class="sxs-lookup"><span data-stu-id="ad182-143">Anti-spam protection FAQ</span></span>](anti-spam-protection-faq.md)
  

