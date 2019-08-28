---
title: 연결 필터 정책, 허용 목록, 차단 목록 구성
ms.author: tracyp
author: MSFTTracyP
manager: dansimp
ms.date: 8/27/2019
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 6ae78c12-7bbe-44fa-ab13-c3768387d0e3
ms.collection:
- M365-security-compliance
description: 사용자가 신뢰 하는 사람이 보낸 전자 메일이 차단 되지 않도록 하려면 연결 필터 정책을 사용 하 여 신뢰할 수 있는 보낸 사람 목록이 라고도 하는 허용 목록을 만든 IP 주소를 만듭니다. 수신 거부 목록도 만들 수 있습니다.
ms.openlocfilehash: a3d9703bc90c0bc1000c2aa755451ffc2cb7d060
ms.sourcegitcommit: 1947ad3c0dde9163ba9b6834d8b38bd04b4264a5
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/27/2019
ms.locfileid: "36643220"
---
# <a name="configure-the-connection-filter-policy"></a><span data-ttu-id="f9606-104">연결 필터 정책 구성</span><span class="sxs-lookup"><span data-stu-id="f9606-104">Configure the connection filter policy</span></span>
 
<span data-ttu-id="f9606-105">누구에게나 대부분 신뢰할 수 있는 친구와 비즈니스 파트너가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f9606-105">Most of us have friends and business partners we trust.</span></span> <span data-ttu-id="f9606-106">그리고 이러한 사용자들로부터 받은 전자 메일이 스팸 메일 폴더로 가거나 스팸 필터를 통해 완전히 차단되는 난처한 경우가 생길 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f9606-106">It can be frustrating to find email from them in your junk email folder, or even blocked entirely by a spam filter.</span></span> <span data-ttu-id="f9606-107">사용자가 신뢰 하는 사람이 보낸 전자 메일이 차단 되지 않도록 하려면 연결 필터 정책을 사용 하 여 신뢰할 수 있는 보낸 사람 목록이 라고도 하는 허용 목록을 만든 IP 주소를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f9606-107">If you want to make sure that email sent from people you trust isn't blocked, you can use the connection filter policy to create an Allow list, also known as a safe sender list, of IP addresses that you trust.</span></span> <span data-ttu-id="f9606-108">그리고 앞으로는 전자 메일 메시지를 받지 않을 IP 주소 목록(대개 알려진 스패머의 주소로 구성)인 수신 거부 목록도 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f9606-108">You can also create a blocked senders list, which is a list of IP addresses, typically from known spammers, that you don't ever want to receive email messages from.</span></span>
  
- <span data-ttu-id="f9606-109">*[허용 목록](create-safe-sender-lists-in-office-365.md)* 에 대해 생각 하는 경우 연결 필터 정책에 따라 필터에서 허용 하는 *신뢰할 수 있는 계정을* 사용 하는 것이 중요 합니다.</span><span class="sxs-lookup"><span data-stu-id="f9606-109">When thinking about *[Allow lists](create-safe-sender-lists-in-office-365.md)*, keep in mind connection filter policies concern themselves with the *trusted accounts allowed* by the filter.</span></span> <span data-ttu-id="f9606-110">이 작업은 신뢰할 수 없거나 신뢰할 수 없는 우편물을 보다 정확 하 게 필터링 하기 위해 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="f9606-110">This is done in the interest of more accurately filtering out less trusted or untrusted mailers while keeping what you need.</span></span> <span data-ttu-id="f9606-111">연결 필터 정책 허용 목록은 훨씬 더 큰 계정 및 Ip 풀에서 몇 가지 신뢰할 수 있는 Ip로 필터링 하 고 신뢰할 수 있는 메일 사용이 쉬운 액세스를 보장 하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="f9606-111">A connection filter policy Allow list is about filtering to the few trusted IPs from a much larger pool of accounts and IPs, and assuring your trusted mailers easier access.</span></span>

- <span data-ttu-id="f9606-112">차단 목록을 만드는 연결 필터 정책에는 대신, 필터에서 더 적은 수의 계정 또는 신뢰 되지 않는 계정이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f9606-112">A connection filter policy creating a Block list can be thought of as catching less, or untrustworthy accounts in the filter instead.</span></span>

 <span data-ttu-id="f9606-113">[전체 조직에 적용되는 추가 스팸 설정은 메시지가 스팸으로 표시되지 않는지 확인하는 방법](https://go.microsoft.com/fwlink/p/?LinkId=534224) 또는 [Office 365 스팸 필터로 전자 메일 스팸을 차단하여 거짓 부정 문제 방지](https://go.microsoft.com/fwlink/p/?LinkId=534225)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="f9606-113">For more spam settings that apply to the whole organization, take a look at [How to help ensure that a message isn't marked as spam](https://go.microsoft.com/fwlink/p/?LinkId=534224) or [Block email spam with the Office 365 spam filter to prevent false negative issues](https://go.microsoft.com/fwlink/p/?LinkId=534225).</span></span> <span data-ttu-id="f9606-114">사용자가 관리자 수준 제어를 가지고 있고 가양성이나 거짓 부정을 방지하려고 할 때 유용합니다.</span><span class="sxs-lookup"><span data-stu-id="f9606-114">These are helpful if you have administrator-level control and you want to prevent false positives or false negatives.</span></span>

> [!TIP]
> <span data-ttu-id="f9606-115">[허용-(또는 안전한 보낸 사람)](create-safe-sender-lists-in-office-365.md) 및 [차단 목록을](create-block-sender-lists-in-office-365.md)만드는 방법을 일시 중지 하 고 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f9606-115">You may want to pause and read up on how to create [Allow- (or safe sender)](create-safe-sender-lists-in-office-365.md) and [Block lists](create-block-sender-lists-in-office-365.md).</span></span>
  
<span data-ttu-id="f9606-116">다음 비디오에서는 연결 필터 정책의 구성 단계를 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="f9606-116">The following video shows the configuration steps for the connection filter policy:</span></span>
  
> [!VIDEO https://www.microsoft.com/videoplayer/embed/b2f5bea3-e1a7-44b3-b7e2-07fac0d0ca40?autoplay=false]
  
## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="f9606-117">시작하기 전에 알아야 할 내용</span><span class="sxs-lookup"><span data-stu-id="f9606-117">What do you need to know before you begin?</span></span>
<span data-ttu-id="f9606-118"><a name="sectionSection0"> </a></span><span class="sxs-lookup"><span data-stu-id="f9606-118"></span></span>

- <span data-ttu-id="f9606-119">예상 완료 시간: 15분</span><span class="sxs-lookup"><span data-stu-id="f9606-119">Estimated time to complete: 15 minutes</span></span>
    
- <span data-ttu-id="f9606-120">이러한 절차를 수행하려면 먼저 사용 권한을 할당받아야 합니다.</span><span class="sxs-lookup"><span data-stu-id="f9606-120">You need to be assigned permissions before you can perform this procedure or procedures.</span></span> <span data-ttu-id="f9606-121">필요한 사용 권한을 확인 하려면 [Exchange Online의 기능 사용 권한](http://technet.microsoft.com/library/15073ce1-0917-403b-8839-02a2ebc96e16.aspx) 항목에서 "스팸 방지" 항목을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="f9606-121">To see what permissions you need, see the "Anti-spam" entry in the [Feature Permissions in Exchange Online](http://technet.microsoft.com/library/15073ce1-0917-403b-8839-02a2ebc96e16.aspx) topic.</span></span> 
    
- <span data-ttu-id="f9606-122">해당 메시지를 허용하거나 차단할 보낸 사람의 IP 주소를 가져오려면 메시지의 인터넷 머리글을 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="f9606-122">To obtain the IP address of the sender whose messages you want to allow or block, you can check the Internet header of the message.</span></span> <span data-ttu-id="f9606-123">[스팸 방지 메시지 헤더](anti-spam-message-headers.md)에 설명된 대로 CIP 머리글을 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="f9606-123">Look for the CIP header as described in [Anti-spam message headers](anti-spam-message-headers.md).</span></span> <span data-ttu-id="f9606-124">다양 한 전자 메일 클라이언트에서 메시지 헤더를 보는 방법에 대 한 자세한 내용은 [메시지 헤더 분석기](https://go.microsoft.com/fwlink/p/?LinkId=306583)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="f9606-124">For information about how to view a message header in various email clients, see [Message Header Analyzer](https://go.microsoft.com/fwlink/p/?LinkId=306583).</span></span> 
    
- <span data-ttu-id="f9606-125">IP 차단 목록의 IP 주소에서 보낸 전자 메일 메시지는 거부 되며 스팸으로 표시 되지 않으며 추가 필터링이 수행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f9606-125">Email messages sent from an IP address on the IP Block list are rejected, not marked as spam, and no additional filtering occurs.</span></span>
    
- <span data-ttu-id="f9606-126">또한 원격 PowerShell을 통해 다음 연결 필터 절차를 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f9606-126">The following connection filter procedure can also be performed via remote PowerShell.</span></span> <span data-ttu-id="f9606-127">[Get-HostedConnectionFilterPolicy](http://technet.microsoft.com/library/bd751db2-3f26-495b-8e5a-4fcab53b17fd.aspx) cmdlet을 사용하여 설정을 검토하고 [Set-HostedConnectionFilterPolicy](http://technet.microsoft.com/library/ccb5731b-3fca-4d69-a91f-5049ea963fac.aspx) cmdlet을 사용하여 연결 필터 정책 설정을 편집할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f9606-127">Use the [Get-HostedConnectionFilterPolicy](http://technet.microsoft.com/library/bd751db2-3f26-495b-8e5a-4fcab53b17fd.aspx) cmdlet to review your settings, and the [Set-HostedConnectionFilterPolicy](http://technet.microsoft.com/library/ccb5731b-3fca-4d69-a91f-5049ea963fac.aspx) to edit your connection filter policy settings.</span></span> <span data-ttu-id="f9606-128">Windows PowerShell을 사용 하 여 Exchange Online Protection에 연결 하는 방법에 대 한 자세한 내용은 [connect To Exchange Online Protection PowerShell](https://go.microsoft.com/fwlink/p/?linkid=627290)을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="f9606-128">To learn how to use Windows PowerShell to connect to Exchange Online Protection, see [Connect to Exchange Online Protection PowerShell](https://go.microsoft.com/fwlink/p/?linkid=627290).</span></span> <span data-ttu-id="f9606-129">Windows PowerShell을 사용하여 Exchange Online에 연결하는 방법에 대한 자세한 내용은 [Connect to Exchange Online Using Remote PowerShell](https://go.microsoft.com/fwlink/p/?linkid=396554)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="f9606-129">To learn how to use Windows PowerShell to connect to Exchange Online, see [Connect to Exchange Online PowerShell](https://go.microsoft.com/fwlink/p/?linkid=396554).</span></span>
    
## <a name="use-the-eac-to-edit-the-default-connection-filter-policy"></a><span data-ttu-id="f9606-130">EAC를 사용하여 기본 연결 필터 정책 편집</span><span class="sxs-lookup"><span data-stu-id="f9606-130">Use the EAC to edit the default connection filter policy</span></span>
<span data-ttu-id="f9606-131"><a name="sectionSection1"> </a></span><span class="sxs-lookup"><span data-stu-id="f9606-131"></span></span>

<span data-ttu-id="f9606-p108">EAC(Exchange 관리 센터)에서 연결 필터 정책을 편집하여 IP 허용 목록 또는 IP 차단 목록을 만듭니다. 연결 필터 정책 설정은 인바운드 메시지에만 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="f9606-p108">You create an IP Allow list or IP Block list by editing the connection filter policy in the Exchange admin center (EAC). The connection filter policy settings are applied to inbound messages only.</span></span>
  
1. <span data-ttu-id="f9606-134">EAC(Exchange 관리 센터)에서 **보호** \> **연결 필터**로 이동한 후 기본 정책을 두 번 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="f9606-134">In the Exchange admin center (EAC), navigate to **Protection** \> **Connection filter**, and then double-click the default policy.</span></span>
    
2. <span data-ttu-id="f9606-135">**연결 필터링** 메뉴 항목을 클릭한 후 원하는 목록을 만듭니다. IP 허용 목록이나 IP 차단 목록 중 하나를 만들거나 두 목록을 모두 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f9606-135">Click the **Connection filtering** menu item and then create the lists you want: an IP Allow list, an IP Block list, or both.</span></span> 
    
    <span data-ttu-id="f9606-p109">이 목록을 만들려면 ![아이콘 추가](media/ITPro-EAC-AddIcon.gif)를 클릭합니다. 이후 표시되는 대화 상자에서 IP 주소나 주소 범위를 지정한 후 **확인**을 클릭합니다. 주소를 추가하려면 이 프로세스를 반복합니다. 주소를 추가한 후 IP 주소를 편집하거나 제거할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f9606-p109">To create these lists, click ![Add Icon](media/ITPro-EAC-AddIcon.gif). In the subsequent dialog box, specify the IP address or address range, and then click **ok**. Repeat this process to add additional addresses. (You can also edit or remove IP addresses after they have been added.)</span></span>
    
    > [!NOTE]
    >  <span data-ttu-id="f9606-140">두 목록에 IP 주소를 추가 하는 경우 해당 IP 주소에서 보낸 전자 메일을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f9606-140">If you add an IP address to both lists, email sent from that IP address is allowed.</span></span> 

    <span data-ttu-id="f9606-141">Nnn은 0에서 255 사이의 숫자로 IPV4 IP 주소를 지정 합니다. nnn</span><span class="sxs-lookup"><span data-stu-id="f9606-141">Specify IPV4 IP addresses in the format nnn.nnn.nnn.nnn where nnn is a number from 0 to 255.</span></span> <span data-ttu-id="f9606-142">또한 a r t. nnn/rr 형식으로 클래스 간 라우팅 (CIDR) 범위를 지정할 수 있습니다 (여기서 rr은 24에서 32 사이의 숫자).</span><span class="sxs-lookup"><span data-stu-id="f9606-142">You can also specify Classless Inter-Domain Routing (CIDR) ranges in the format nnn.nnn.nnn.nnn/rr where rr is a number from 24 to 32.</span></span> <span data-ttu-id="f9606-143">24 ~ 32 범위를 벗어나는 범위를 지정 하려면 [IP 허용 목록을 구성할 때 추가 고려 사항을](configure-the-connection-filter-policy.md#bkmk_addtionalconsiderationswhenconfiguringipallowlists)참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="f9606-143">To specify ranges outside of the 24 to 32 range, see [Additional considerations when configuring IP Allow lists](configure-the-connection-filter-policy.md#bkmk_addtionalconsiderationswhenconfiguringipallowlists).</span></span> 

    <span data-ttu-id="f9606-144">최대 1273 개의 항목을 지정할 수 있는데,이 항목은 단일 IP 주소 이거나 IP 주소의 CIDR 범위/24 ~/32입니다.</span><span class="sxs-lookup"><span data-stu-id="f9606-144">You can specify a maximum of 1273 entries, where an entry is either a single IP address or a CIDR range of IP addresses from /24 to /32.</span></span> <span data-ttu-id="f9606-145">> TLS 암호화 된 메시지를 보내는 경우 IPv6 주소 및 주소 범위는 지원 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f9606-145">>  If you're sending TLS-encrypted messages, IPv6 addresses and address ranges are not supported.</span></span> 
  
3. <span data-ttu-id="f9606-146">원하는 경우 수신 허용 **목록 사용** 확인란을 선택 하 여 잘 알려진 특정 보낸 사람의 전자 메일이 손실 되지 않도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="f9606-146">Optionally, select the **Enable safe list** check box to prevent missing email from certain well-known senders.</span></span> <span data-ttu-id="f9606-147">미치는?</span><span class="sxs-lookup"><span data-stu-id="f9606-147">How?</span></span> <span data-ttu-id="f9606-148">Microsoft는 신뢰할 수 있는 보낸 사람에 대 한 타사 소스를 구독 합니다.</span><span class="sxs-lookup"><span data-stu-id="f9606-148">Microsoft subscribes to third-party sources of trusted senders.</span></span> <span data-ttu-id="f9606-149">이 수신 허용 목록을 사용 하는 것은 해당 신뢰할 수 있는 보낸 사람이 실수로 스팸으로 표시 되지 않았음을 의미 합니다.</span><span class="sxs-lookup"><span data-stu-id="f9606-149">Using this safe list means that these trusted senders aren't mistakenly marked as spam.</span></span> <span data-ttu-id="f9606-150">이 옵션을 선택 하는 것이 좋습니다 (스팸으로 분류 되는 가짜 메일) 수를 줄여야 하기 때문입니다.</span><span class="sxs-lookup"><span data-stu-id="f9606-150">We recommend selecting this option because it should reduce the number of false positives (good mail that's classified as spam) that you receive.</span></span> 
    
4. <span data-ttu-id="f9606-151">**저장**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="f9606-151">Click **save**.</span></span> <span data-ttu-id="f9606-152">기본 정책 설정에 대한 요약이 오른쪽 창에 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="f9606-152">A summary of your default policy settings appears in the right pane.</span></span>
    
## <a name="additional-considerations-when-configuring-ip-allow-lists"></a><span data-ttu-id="f9606-153">IP 허용 목록 구성 시 추가 고려 사항</span><span class="sxs-lookup"><span data-stu-id="f9606-153">Additional considerations when configuring IP Allow lists</span></span>
<span data-ttu-id="f9606-154"><a name="bkmk_addtionalconsiderationswhenconfiguringipallowlists"> </a></span><span class="sxs-lookup"><span data-stu-id="f9606-154"></span></span>

<span data-ttu-id="f9606-155">다음은 IP 허용 목록 구성 시 고려해야 하거나 알고 있어야 하는 추가 고려 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="f9606-155">The following are additional considerations you may want to consider or that you should be aware of when configuring an IP Allow list.</span></span>
  
### <a name="specifying-a-cidr-range-that-falls-outside-of-the-recommended-range"></a><span data-ttu-id="f9606-156">권장되는 범위를 벗어나는 CIDR 범위 지정</span><span class="sxs-lookup"><span data-stu-id="f9606-156">Specifying a CIDR range that falls outside of the recommended range</span></span>

<span data-ttu-id="f9606-157">/1에서/23 까지의 CIDR IP 주소 범위를 지정 하려면 SCL (스팸 지 수)이이 IP 주소 범위 내에서 수신 되는 모든 메시지를 **무시** 하도록 설정 하는 ip 주소 범위에서 작동 하는 메일 흐름 규칙을 만들어야 합니다. "스팸 아님"으로 설정 되 고 서비스에서 추가 필터링을 수행 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f9606-157">To specify a CIDR IP address range from /1 to /23, you must create a mail flow rule that operates on the IP address range that sets the spam confidence level (SCL) to **Bypass spam filtering** (meaning that all messages received from within this IP address range are set to "not spam") and no additional filtering is performed by the service).</span></span> <span data-ttu-id="f9606-158">하지만 Microsoft 전용 차단 목록이나 타사의 차단 목록에 이러한 IP 주소가 표시된 경우 이러한 메시지는 계속해서 차단됩니다.</span><span class="sxs-lookup"><span data-stu-id="f9606-158">However, if any of these IP addresses appear on any of Microsoft's proprietary block lists or on any of our third-party block lists, these messages will still be blocked.</span></span> <span data-ttu-id="f9606-159">따라서/24 ~/32 IP 주소 범위를 사용 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="f9606-159">It is therefore strongly recommended that you use the /24 to /32 IP address range.</span></span> 
  
<span data-ttu-id="f9606-160">이 메일 흐름 규칙을 만들려면 다음 단계를 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="f9606-160">To create this mail flow rule, perform the following steps.</span></span>
  
1. <span data-ttu-id="f9606-161">EAC에서 **메일 흐름** \> **규칙**으로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="f9606-161">In the EAC, navigate to **Mail flow** \> **Rules**.</span></span>
    
2. <span data-ttu-id="f9606-162">![아이콘 추가](media/ITPro-EAC-AddIcon.gif)를 클릭한 다음 **새 규칙 만들기**를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="f9606-162">Click ![Add Icon](media/ITPro-EAC-AddIcon.gif) and then select **Create a new rule**.</span></span>
    
3. <span data-ttu-id="f9606-163">규칙 이름을 지정하고 **기타 옵션**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="f9606-163">Give the rule a name and then click **More options**.</span></span>
    
4. <span data-ttu-id="f9606-164">**다음의 경우 이 규칙 적용**에서 **보낸 사람**을 선택하고 **IP 주소가 이 범위에 속하거나 정확하게 일치함**을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="f9606-164">Under **Apply this rule if**, select **The sender** and then choose **IP address is in any of these ranges or exactly matches**.</span></span>
    
5. <span data-ttu-id="f9606-165">**Ip 주소 지정**에서 ip 주소 범위를 지정 하 고 추가 아이콘 \*\*\*\* ![](media/ITPro-EAC-AddIcon.gif)추가를 클릭 한 다음 **확인**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="f9606-165">In the **specify IP addresses**, specify the IP address range, click **Add** ![Add Icon](media/ITPro-EAC-AddIcon.gif), and then click **ok**.</span></span>
    
6. <span data-ttu-id="f9606-p115">**다음 작업 수행** 상자에서 **메시지 속성 수정**을 선택한 다음 **SCL(스팸 지수) 설정**을 선택하여 동작을 설정합니다. **SCL 지정** 상자에서 **스팸 필터링 무시**를 선택한 후 **확인**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="f9606-p115">Under **Do the following** box, set the action by choosing **Modify the message properties** and then **set the spam confidence level (SCL)**. In the **specify SCL** box, select **Bypass spam filtering**, and click **ok**.</span></span>
    
7. <span data-ttu-id="f9606-168">원하는 경우 규칙을 감사하고 규칙을 테스트하며 특정 기간 동안 규칙을 활성화하는 등 기타 옵션을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f9606-168">If you'd like, you can make selections to audit the rule, test the rule, activate the rule during a specific time period, and other selections.</span></span> <span data-ttu-id="f9606-169">옵션을 적용하기 전에 규칙을 테스트하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="f9606-169">We recommend testing the rule for a period before you enforce it.</span></span> <span data-ttu-id="f9606-170">[Exchange Server의 메일 흐름 규칙에 대 한 절차에는](https://docs.microsoft.com/en-us/Exchange/policy-and-compliance/mail-flow-rules/mail-flow-rule-procedures) 이러한 선택 항목에 대 한 자세한 정보가 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f9606-170">[Procedures for mail flow rules in Exchange Server](https://docs.microsoft.com/en-us/Exchange/policy-and-compliance/mail-flow-rules/mail-flow-rule-procedures) contains more information about these selections.</span></span> 
    
8. <span data-ttu-id="f9606-171">**저장** 을 클릭 하 여 규칙을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="f9606-171">Click **save** to save the rule.</span></span> <span data-ttu-id="f9606-172">규칙이 규칙 목록에 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f9606-172">The rule appears in your list of rules.</span></span> 
    
<span data-ttu-id="f9606-173">규칙을 만들고 적용 한 후에는 서비스에서 지정한 IP 주소 범위에 대 한 스팸 필터링을 무시 합니다.</span><span class="sxs-lookup"><span data-stu-id="f9606-173">After you create and enforce the rule, the service bypasses spam filtering for the IP address range you specified.</span></span>
  
### <a name="scoping-an-ip-allow-list-exception-for-a-specific-domain"></a><span data-ttu-id="f9606-174">특정 도메인에 대해 IP 허용 목록 예외 범위 지정</span><span class="sxs-lookup"><span data-stu-id="f9606-174">Scoping an IP Allow list exception for a specific domain</span></span>

<span data-ttu-id="f9606-175">일반적으로 안전한 것으로 간주되는 모든 도메인에 대한 IP 주소(또는 IP 주소 범위)를 IP 허용 목록에 추가하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="f9606-175">In general, we recommend that you add the IP addresses (or IP address ranges) for all your domains that you consider safe to the IP Allow list.</span></span> <span data-ttu-id="f9606-176">그러나 IP 허용 목록 항목을 모든 도메인에 적용 하지 않으려면 특정 도메인을 제외 하는 메일 흐름 규칙 (전송 규칙이 라고도 함)을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f9606-176">However, if you don't want your IP Allow List entry to apply to all your domains, you can create a mail flow rule (also known as a transport rule) that excepts specific domains.</span></span> 
  
<span data-ttu-id="f9606-177">예를 들어, 세 개의 도메인인 ContosoA.com, ContosoB.com 및 ContosoC.com이 있으며 IP 주소(단순하게 표현하기 위해 1.2.3.4 사용)를 추가하고 도메인 ContosoB.com에 대해서만 필터링을 건너뛰려 한다고 가정합니다.</span><span class="sxs-lookup"><span data-stu-id="f9606-177">For example, let's say you have three domains: ContosoA.com, ContosoB.com, and ContosoC.com, and you want to add the IP address (for simplicity's sake, let's use 1.2.3.4) and skip filtering only for domain ContosoB.com.</span></span> <span data-ttu-id="f9606-178">모든 도메인에 대해 SCL(스팸 지수)을 -1(스팸이 아닌 것으로 분류됨을 의미함)로 설정하는 IP 허용 목록을 1.2.3.4에 대해 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f9606-178">You would create an IP Allow list for 1.2.3.4, which sets the spam confidence level (SCL) to -1 (meaning it is classified as non-spam) for all domains.</span></span> <span data-ttu-id="f9606-179">그런 다음 ContosoB.com를 제외한 모든 도메인에 대해 SCL을 설정 하는 메일 흐름 규칙을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f9606-179">You can then create a mail flow rule that sets the SCL for all domains except ContosoB.com to 0.</span></span> <span data-ttu-id="f9606-180">그러면 ContosoB.com(규칙에서 예외로 나열되는 도메인)을 제외하고 IP 주소와 연결된 모든 도메인에 대해 메시지가 다시 검색됩니다.</span><span class="sxs-lookup"><span data-stu-id="f9606-180">This results in the message being rescanned for all domains associated with the IP address except for ContosoB.com which is the domain listed as the exception in the rule.</span></span> <span data-ttu-id="f9606-181">ContosoB.com의 SCL은 여전히 -1(필터링 건너뜀을 의미함)인 반면, ContosoA.com 및 ContosoC.com의 SCL은 0(콘텐츠 필터에 의해 다시 검색됨을 의미함)입니다.</span><span class="sxs-lookup"><span data-stu-id="f9606-181">ContosoB.com still has an SCL of -1 which means skip filtering, whereas ContosoA.com and ContosoC.com have SCLs of 0, meaning they will be rescanned by the content filter.</span></span>
  
<span data-ttu-id="f9606-182">이렇게 하려면 다음 단계를 수행합니다.</span><span class="sxs-lookup"><span data-stu-id="f9606-182">To do this, perform the following steps:</span></span>
  
1. <span data-ttu-id="f9606-183">EAC에서 **메일 흐름** \> **규칙**으로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="f9606-183">In the EAC, navigate to **Mail flow** \> **Rules**.</span></span>
    
2. <span data-ttu-id="f9606-184">![아이콘 추가](media/ITPro-EAC-AddIcon.gif)를 클릭한 다음 **새 규칙 만들기**를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="f9606-184">Click ![Add Icon](media/ITPro-EAC-AddIcon.gif) and then select **Create a new rule**.</span></span>
    
3. <span data-ttu-id="f9606-185">규칙 이름을 지정하고 **기타 옵션**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="f9606-185">Give the rule a name and then click **More options**.</span></span>
    
4. <span data-ttu-id="f9606-186">**다음의 경우 이 규칙 적용**에서 **보낸 사람**을 선택하고 **IP 주소가 이 범위에 속하거나 정확하게 일치함**을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="f9606-186">Under **Apply this rule if**, select **The sender** and then choose **IP address is in any of these ranges or exactly matches**.</span></span>
    
5. <span data-ttu-id="f9606-187">**Ip 주소 지정** 상자에서 ip 허용 목록에 입력 한 ip 주소 또는 ip 주소 범위를 지정 하 고 추가 아이콘](media/ITPro-EAC-AddIcon.gif) **추가** ![를 클릭 한 다음 **확인**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="f9606-187">In the **specify IP addresses** box, specify the IP address or IP address range you entered in the IP Allow list, click **Add** ![Add Icon](media/ITPro-EAC-AddIcon.gif), and then click **ok**.</span></span>
    
6. <span data-ttu-id="f9606-p120">**다음 작업 실행**에서 **메시지 속성 수정**을 선택한 후 **SCL(스팸 지수) 설정**을 선택하여 동작을 설정합니다. **SCL 지정** 상자에서 **0**을 선택한 후 **확인**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="f9606-p120">Under **Do the following**, set the action by choosing **Modify the message properties** and then **set the spam confidence level (SCL)**. In the **specify SCL** box, select **0**, and click **ok**.</span></span>
    
7. <span data-ttu-id="f9606-190">**예외 추가**를 클릭하고 **다음의 경우 제외**에서 **보낸 사람**을 선택하고 **도메인**을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="f9606-190">Click **add exception**, and under **Except if**, select **The sender** and choose **domain is**.</span></span> 
    
8. <span data-ttu-id="f9606-191">**도메인 지정** 상자에 스팸 필터링을 무시할 도메인을 입력합니다(예: **contosob.com**).</span><span class="sxs-lookup"><span data-stu-id="f9606-191">In the **specify domain** box, enter the domain for which you want to bypass spam filtering, such as **contosob.com**.</span></span> <span data-ttu-id="f9606-192">추가 아이콘](media/ITPro-EAC-AddIcon.gif) 추가를 클릭 하 여 구 목록으로 이동 합니다. \*\*\*\* ![</span><span class="sxs-lookup"><span data-stu-id="f9606-192">Click **Add** ![Add Icon](media/ITPro-EAC-AddIcon.gif) to move it to the list of phrases.</span></span> <span data-ttu-id="f9606-193">도메인을 예외로 더 추가하려면 이 단계를 반복하고 완료되면 **확인**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="f9606-193">Repeat this step if you want to add additional domains as exceptions, and click **ok** when you are finished.</span></span> 
    
9. <span data-ttu-id="f9606-194">원하는 경우 규칙을 감사하고 규칙을 테스트하며 특정 기간 동안 규칙을 활성화하는 등 기타 옵션을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f9606-194">If you'd like, you can make selections to audit the rule, test the rule, activate the rule during a specific time period, and other selections.</span></span> <span data-ttu-id="f9606-195">옵션을 적용하기 전에 규칙을 테스트하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="f9606-195">We recommend testing the rule for a period before you enforce it.</span></span> <span data-ttu-id="f9606-196">[Exchange Server의 메일 흐름 규칙에 대 한 절차에는](https://docs.microsoft.com/en-us/Exchange/policy-and-compliance/mail-flow-rules/mail-flow-rule-procedures) 이러한 선택 항목에 대 한 자세한 정보가 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f9606-196">[Procedures for mail flow rules in Exchange Server](https://docs.microsoft.com/en-us/Exchange/policy-and-compliance/mail-flow-rules/mail-flow-rule-procedures) contains more information about these selections.</span></span> 
    
10. <span data-ttu-id="f9606-197">**저장** 을 클릭 하 여 규칙을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="f9606-197">Click **save** to save the rule.</span></span> <span data-ttu-id="f9606-198">규칙이 규칙 목록에 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f9606-198">The rule appears in your list of rules.</span></span> 
    
<span data-ttu-id="f9606-199">규칙을 만들어 적용하고 나면 지정한 IP 주소 또는 IP 주소 범위에 대한 스팸 필터링이 입력한 도메인 예외에 대해서만 무시됩니다.</span><span class="sxs-lookup"><span data-stu-id="f9606-199">After you create and enforce the rule, spam filtering for the IP address or IP address range you specified is bypassed only for the domain exception you entered.</span></span>
  
## <a name="new-to-office-365"></a><span data-ttu-id="f9606-200">Office 365의 새로운 기능</span><span class="sxs-lookup"><span data-stu-id="f9606-200">New to Office 365?</span></span>
<span data-ttu-id="f9606-201"><a name="sectionSection3"> </a></span><span class="sxs-lookup"><span data-stu-id="f9606-201"></span></span>

||
|:-----|
|<span data-ttu-id="f9606-p124">![LinkedIn Learning용 단축 아이콘](media/eac8a413-9498-4220-8544-1e37d1aaea13.png) **Office 365를 처음 사용하시나요?**         LinkedIn Learning에서 제공하는 **Office 365 admins and IT pros**의 무료 비디오 과정을 확인해보세요.</span><span class="sxs-lookup"><span data-stu-id="f9606-p124">![The short icon for LinkedIn Learning](media/eac8a413-9498-4220-8544-1e37d1aaea13.png) **New to Office 365?**         Discover free video courses for **Office 365 admins and IT pros**, brought to you by LinkedIn Learning.</span></span> |
   
## <a name="for-more-information"></a><span data-ttu-id="f9606-204">자세한 내용</span><span class="sxs-lookup"><span data-stu-id="f9606-204">For more information</span></span>
<span data-ttu-id="f9606-205"><a name="sectionSection4"> </a></span><span class="sxs-lookup"><span data-stu-id="f9606-205"></span></span>

[<span data-ttu-id="f9606-206">Exchange Online의 수신 허용-보낸 사람 및 수신 거부 목록</span><span class="sxs-lookup"><span data-stu-id="f9606-206">Safe sender and blocked sender lists in Exchange Online</span></span>](safe-sender-and-blocked-sender-lists-faq.md)
  
[<span data-ttu-id="f9606-207">스팸 필터 정책 구성</span><span class="sxs-lookup"><span data-stu-id="f9606-207">Configure your spam filter policies</span></span>](configure-your-spam-filter-policies.md)
  
[<span data-ttu-id="f9606-208">아웃바운드 스팸 정책 구성</span><span class="sxs-lookup"><span data-stu-id="f9606-208">Configure the outbound spam policy</span></span>](configure-the-outbound-spam-policy.md)
  
[<span data-ttu-id="f9606-209">메시지가 스팸으로 표시되지 않는지 확인하는 방법</span><span class="sxs-lookup"><span data-stu-id="f9606-209">How to help ensure that a message isn't marked as spam</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=534224)
  
[<span data-ttu-id="f9606-210">Office 365 스팸 필터로 전자 메일 스팸을 차단하여 거짓 부정 문제 방지</span><span class="sxs-lookup"><span data-stu-id="f9606-210">Block email spam with the Office 365 spam filter to prevent false negative issues</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=534225)
  

