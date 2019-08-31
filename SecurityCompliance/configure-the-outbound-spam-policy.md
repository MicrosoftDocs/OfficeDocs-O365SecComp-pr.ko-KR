---
title: 아웃바운드 스팸 정책 구성
ms.author: tracyp
author: MSFTTracyP
manager: dansimp
ms.date: 11/10/2016
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: a44764e9-a5d2-4c67-8888-e7fb871c17c7
ms.collection:
- M365-security-compliance
description: 아웃바운드 전자 메일 보내기 서비스를 사용하는 경우 아웃바운드 스팸 필터링이 항상 사용하도록 설정되므로 서비스와 받는 사람을 사용하여 조직을 보호할 수 있습니다.
ms.openlocfilehash: 9c8c2f7e9ff0be02f11fa66409690cbb854d8c56
ms.sourcegitcommit: 769b506c828c475c713dbb337e115714dcc7f17c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/31/2019
ms.locfileid: "36699243"
---
# <a name="configure-the-outbound-spam-policy"></a><span data-ttu-id="e6472-103">아웃바운드 스팸 정책 구성</span><span class="sxs-lookup"><span data-stu-id="e6472-103">Configure the outbound spam policy</span></span>

<span data-ttu-id="e6472-p101">아웃바운드 전자 메일 보내기 서비스를 사용하는 경우 아웃바운드 스팸 필터링이 항상 사용하도록 설정되므로 서비스와 받는 사람을 사용하여 조직을 보호할 수 있습니다. 인바운드 필터링과 마찬가지로 아웃바운드 스팸 필터링도 연결 필터링과 콘텐츠 필터링으로 구성되지만, 아웃바운드 필터 설정은 구성할 수 없습니다. 스팸으로 확인된 아웃바운드 메시지는 위험성이 높은 배달 풀을 통해 라우팅되므로 일반 아웃바운드 IP 풀이 차단 목록에 추가될 가능성이 줄어듭니다. 서비스를 통해 아웃바운드 스팸을 계속 보내는 고객에 대해서는 메시지 보내기가 차단됩니다. 아웃바운드 스팸 필터링을 사용하지 않도록 설정하거나 변경할 수는 없지만 기본 아웃바운드 스팸 정책을 통해 다양한 회사 전체 아웃바운드 스팸 설정을 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e6472-p101">Outbound spam filtering is always enabled if you use the service for sending outbound email, thereby protecting organizations using the service and their intended recipients. Similar to inbound filtering, outbound spam filtering is comprised of connection filtering and content filtering, however the outbound filter settings are not configurable. If an outbound message is determined to be spam, it is routed through the higher risk delivery pool, which reduces the probability of the normal outbound-IP pool being added to a block list. If a customer continues to send outbound spam through the service, they will be blocked from sending messages. Although outbound spam filtering cannot be disabled or changed, you can configure several company-wide outbound spam settings via the default outbound spam policy.</span></span> 
  
<span data-ttu-id="e6472-109">다음 비디오에서는 아웃바운드 스팸 정책을 구성하는 방법을 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="e6472-109">The following video shows how to configure the outbound spam policy:</span></span>
  
> [!VIDEO https://www.microsoft.com/videoplayer/embed/1f20d655-0d3d-4141-9cae-e57f5a6cffe8?autoplay=false]
  
> [!NOTE]
> <span data-ttu-id="e6472-110">가장 적합 한 필터링 결과를 보려면 위 비디오의 콘텐츠를 적절 한 설정에 사용 하 고 [Office 365의 아웃 바운드 스팸 제어](https://docs.microsoft.com/office365/securitycompliance/outbound-spam-controls)에 친숙 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e6472-110">For the best filtering results, the content in the video above should used with a proper setup, and familiarity with [Outbound spam controls in Office 365](https://docs.microsoft.com/office365/securitycompliance/outbound-spam-controls).</span></span>

## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="e6472-111">시작하기 전에 알아야 할 내용</span><span class="sxs-lookup"><span data-stu-id="e6472-111">What do you need to know before you begin?</span></span>
<span data-ttu-id="e6472-112"><a name="sectionSection0"> </a></span><span class="sxs-lookup"><span data-stu-id="e6472-112"></span></span>

<span data-ttu-id="e6472-113">예상 완료 시간: 5분</span><span class="sxs-lookup"><span data-stu-id="e6472-113">Estimated time to complete: 5 minutes</span></span>
  
<span data-ttu-id="e6472-114">이러한 절차를 수행하려면 먼저 사용 권한을 할당받아야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e6472-114">You need to be assigned permissions before you can perform this procedure or procedures.</span></span> <span data-ttu-id="e6472-115">필요한 사용 권한을 확인 하려면 [Exchange Online의 기능 사용 권한](http://technet.microsoft.com/library/15073ce1-0917-403b-8839-02a2ebc96e16.aspx) 에서 "스팸 방지 항목" 항목을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="e6472-115">To see what permissions you need, see the "Anti-spam entry in the [Feature Permissions in Exchange Online](http://technet.microsoft.com/library/15073ce1-0917-403b-8839-02a2ebc96e16.aspx) topic.</span></span> 
  
<span data-ttu-id="e6472-116">이 항목의 절차에 적용할 수 있는 바로 가기 키에 대 한 자세한 내용은 [Exchange Online에서 exchange 관리 센터에 대 한 바로 가기 키](https://docs.microsoft.com/Exchange/accessibility/keyboard-shortcuts-in-admin-center)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="e6472-116">For information about keyboard shortcuts that may apply to the procedures in this topic, see [Keyboard shortcuts for the Exchange admin center in Exchange Online](https://docs.microsoft.com/Exchange/accessibility/keyboard-shortcuts-in-admin-center).</span></span>
  
<span data-ttu-id="e6472-117">또한 원격 PowerShell을 통해 다음 절차를 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e6472-117">The following procedure can also be performed via remote PowerShell.</span></span> <span data-ttu-id="e6472-118">[Get-HostedOutboundSpamFilterPolicy](http://technet.microsoft.com/library/8f15c83c-c10a-4d9d-b135-35321430bdc2.aspx) cmdlet을 사용하여 설정을 검토하고 [Set-HostedOutboundSpamFilterPolicy](http://technet.microsoft.com/library/665d1b04-d4b5-4a0e-811a-4e37096ccbfd.aspx) cmdlet을 사용하여 아웃바운드 스팸 정책 설정을 편집할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e6472-118">Use the [Get-HostedOutboundSpamFilterPolicy](http://technet.microsoft.com/library/8f15c83c-c10a-4d9d-b135-35321430bdc2.aspx) cmdlet to review your settings, and the [Set-HostedOutboundSpamFilterPolicy](http://technet.microsoft.com/library/665d1b04-d4b5-4a0e-811a-4e37096ccbfd.aspx) to edit your outbound spam policy settings.</span></span> <span data-ttu-id="e6472-119">Windows PowerShell을 사용 하 여 Exchange Online Protection에 연결 하는 방법에 대 한 자세한 내용은 [connect To Exchange Online Protection PowerShell](https://go.microsoft.com/fwlink/p/?linkid=627290)을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="e6472-119">To learn how to use Windows PowerShell to connect to Exchange Online Protection, see [Connect to Exchange Online Protection PowerShell](https://go.microsoft.com/fwlink/p/?linkid=627290).</span></span> <span data-ttu-id="e6472-120">Windows PowerShell을 사용하여 Exchange Online에 연결하는 방법에 대한 자세한 내용은 [Connect to Exchange Online Using Remote PowerShell](https://go.microsoft.com/fwlink/p/?linkid=396554)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="e6472-120">To learn how to use Windows PowerShell to connect to Exchange Online, see [Connect to Exchange Online PowerShell](https://go.microsoft.com/fwlink/p/?linkid=396554).</span></span>
  
## <a name="use-the-eac-to-edit-the-default-outbound-spam-policy"></a><span data-ttu-id="e6472-121">EAC를 사용하여 기본 아웃바운드 스팸 정책 편집</span><span class="sxs-lookup"><span data-stu-id="e6472-121">Use the EAC to edit the default outbound spam policy</span></span>
<span data-ttu-id="e6472-122"><a name="sectionSection1"> </a></span><span class="sxs-lookup"><span data-stu-id="e6472-122"></span></span>

<span data-ttu-id="e6472-123">다음 절차에 따라 기본 아웃바운드 스팸 정책을 편집합니다.</span><span class="sxs-lookup"><span data-stu-id="e6472-123">Use the following procedure to edit the default outbound spam policy:</span></span>
  
### <a name="to-configure-the-default-outbound-spam-policy"></a><span data-ttu-id="e6472-124">기본 아웃바운드 스팸 정책을 구성하려면 다음을 수행합니다.</span><span class="sxs-lookup"><span data-stu-id="e6472-124">To configure the default outbound spam policy</span></span>

1. <span data-ttu-id="e6472-125">EAC(Exchange 관리 센터)에서 **보호** \> **아웃바운드 스팸**으로 이동한 다음 기본 정책을 두 번 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="e6472-125">In the Exchange admin center (EAC), navigate to **Protection** \> **Outbound spam**, and then double-click the default policy.</span></span>
    
2. <span data-ttu-id="e6472-126">**아웃바운드 스팸 기본 설정** 메뉴 옵션을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="e6472-126">Select the **Outbound spam preferences** menu option.</span></span> 
    
3. <span data-ttu-id="e6472-127">아웃바운드 메시지와 관련된 다음 확인란을 선택하고 함께 제공되는 입력란에 연관된 전자 메일 주소를 하나 이상 지정합니다. 전자 메일 주소가 유효한 SMTP 대상으로 확인되는 경우에는 메일 그룹을 입력할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e6472-127">Select the following check boxes pertaining to outbound messages, and then specify an associated email address or addresses in the accompanying input box (these can be distribution lists if they resolve as valid SMTP destinations):</span></span>
    
1. <span data-ttu-id="e6472-p104">**의심스러운 모든 아웃바운드 전자 메일 메시지의 복사본을 다음 전자 메일 주소로 보내기**. 이러한 메시지는 SCL 등급에 관계없이 필터에 의해 스팸으로 표시되며, 필터에서 거부되지는 않지만 위험성이 높은 배달 풀을 통해 라우팅됩니다. 주소가 여러 개인 경우 세미콜론으로 구분합니다. 지정된 받는 사람은 보낸 사람 및 받는 사람 필드에 원래 보낸 사람 및 받는 사람이 표시되는 Bcc(숨은 참조) 주소로 메시지를 받습니다.</span><span class="sxs-lookup"><span data-stu-id="e6472-p104">**Send a copy of all suspicious outbound email messages to the following email address or addresses**. These are messages that are marked as spam by the filter (regardless of the SCL rating). They are not rejected by the filter but are routed through the higher risk delivery pool. Separate multiple addresses with a semicolon. Note that the recipients specified will receive the messages as a Blind carbon copy (Bcc) address (the From and To fields are the original sender and recipient).</span></span>
    
2. <span data-ttu-id="e6472-p105">**보낸 사람이 아웃바운드 스팸을 보낼 수 없도록 차단된 경우 다음 전자 메일 주소로 알림 보내기**. 주소가 여러 개인 경우 세미콜론으로 구분합니다.</span><span class="sxs-lookup"><span data-stu-id="e6472-p105">**Send a notification to the following email address when a sender is blocked sending outbound spam**. Separate multiple addresses with a semicolon.</span></span>
    
    <span data-ttu-id="e6472-135">특정 사용자로부터 스팸이 많이 생성되는 경우 해당 사용자가 전자 메일 메시지를 보낼 수 없도록 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="e6472-135">When a significant amount of spam is originating from a particular user, the user is disabled from sending email messages.</span></span> <span data-ttu-id="e6472-136">이 설정을 사용하여 지정되는 도메인의 관리자에게는 해당 사용자의 아웃바운드 메시지가 차단되었다는 알림이 제공됩니다.</span><span class="sxs-lookup"><span data-stu-id="e6472-136">The administrator for the domain, who is specified using this setting, will be informed that outbound messages are blocked for this user.</span></span> <span data-ttu-id="e6472-137">이 알림의 모양을 보려면 [보낸 사람이 보내는 아웃 바운드 스팸 차단 되 면 샘플 알림](sample-notification-when-a-sender-is-blocked-sending-outbound-spam.md)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="e6472-137">To see what this notification looks like, see [Sample notification when a sender is blocked sending outbound spam](sample-notification-when-a-sender-is-blocked-sending-outbound-spam.md).</span></span> <span data-ttu-id="e6472-138">다시 사용 하도록 설정 하는 방법에 대 한 자세한 내용은 [스팸 메일을 보낸 후 차단 목록에서 사용자, 도메인 또는 IP 주소 제거](http://technet.microsoft.com/library/712cfcc1-31e8-4e51-8561-b64258a8f1e5.aspx)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="e6472-138">For information about getting re-enabled, see [Removing a user, domain, or IP address from a block list after sending spam email](http://technet.microsoft.com/library/712cfcc1-31e8-4e51-8561-b64258a8f1e5.aspx).</span></span>
    
4. <span data-ttu-id="e6472-p107">**저장**을 클릭합니다. 기본 정책 설정에 대한 요약이 오른쪽 창에 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="e6472-p107">Click **save**. A summary of your default policy settings appears in the right pane.</span></span>
    
## <a name="for-more-information"></a><span data-ttu-id="e6472-141">자세한 내용</span><span class="sxs-lookup"><span data-stu-id="e6472-141">For more information</span></span>
<span data-ttu-id="e6472-142"><a name="sectionSection2"> </a></span><span class="sxs-lookup"><span data-stu-id="e6472-142"></span></span>

[<span data-ttu-id="e6472-143">아웃 바운드 메시지에 대 한 위험성이 높은 배달 풀</span><span class="sxs-lookup"><span data-stu-id="e6472-143">High-risk delivery pool for outbound messages</span></span>](high-risk-delivery-pool-for-outbound-messages.md)
  
[<span data-ttu-id="e6472-144">스팸 방지 보호 기능 FAQ</span><span class="sxs-lookup"><span data-stu-id="e6472-144">Anti-spam protection FAQ</span></span>](anti-spam-protection-faq.md)
  

