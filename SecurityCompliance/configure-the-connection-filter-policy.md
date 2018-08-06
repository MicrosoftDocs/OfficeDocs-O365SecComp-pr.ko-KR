---
title: 연결 필터 정책 구성
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 10/2/2017
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
ms.assetid: 6ae78c12-7bbe-44fa-ab13-c3768387d0e3
description: 사람을 신뢰 하에서 보낸 전자 메일 차단 되지 않습니다 있는지 확인 하십시오로 알려져는 수신 허용-보낸사람, IP 주소 목록에 신뢰할 수 있는 허용 목록을 만들려면 연결 필터 정책을 사용할 수 있습니다. 수신된 거부 목록을 만들 수도 있습니다.
ms.openlocfilehash: d106e55779c6246b77018fef3ab9d58fa759d99e
ms.sourcegitcommit: 22bca85c3c6d946083d3784f72e886c068d49f4a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/06/2018
ms.locfileid: "22027605"
---
# <a name="configure-the-connection-filter-policy"></a><span data-ttu-id="ad4c6-104">연결 필터 정책 구성</span><span class="sxs-lookup"><span data-stu-id="ad4c6-104">Configure the connection filter policy</span></span>
 
<span data-ttu-id="ad4c6-p102">대부분의 경우 친구 및 비즈니스 파트너는 신뢰 스팸 필터에 의해 완전히 차단도 또는 전자 메일을 정크 메일 폴더, 찾으려고 실망 수 있습니다. 사람을 신뢰 하에서 보낸 전자 메일 차단 되지 않습니다, 연결 필터 정책을 사용 하 여 수신 허용-보낸사람 목록으로도 알려져 허용 목록을 만들려면 않았는지 확인 하려는 경우 ip 주소를 트러스트 하. 전자 메일 메시지를 받을 전혀 원하지 않는 알려진된 스팸 메일에서 일반적으로 IP 주소 목록에 해당 하는 수신된 거부 목록을 만들 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ad4c6-p102">Most of us have friends and business partners we trust. It can be frustrating to find email from them in your junk email folder, or even blocked entirely by a spam filter. If you want to make sure that email sent from people you trust isn't blocked, you can use the connection filter policy to create an Allow list, also known as a safe sender list, of IP addresses that you trust. You can also create a blocked senders list, which is a list of IP addresses, typically from known spammers, that you don't ever want to receive email messages from.</span></span>
  
 <span data-ttu-id="ad4c6-p103">조직 전체에 적용 하는 자세한 스팸 설정에 대 한 [메시지를 스팸으로 표시 되지 않습니다을 보장 하는 방법](https://go.microsoft.com/fwlink/p/?LinkId=534224) 또는 [false 이면 음수 문제를 방지 하기 위해 Office 365 스팸 필터와 스팸 차단 전자 메일](https://go.microsoft.com/fwlink/p/?LinkId=534225)에 대 한 정보를 수행 합니다. 다음은 관리자 수준의 제어 있고 가양성 또는 잘못 된 음수가 되지 않도록 하려는 경우에 유용 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad4c6-p103">For more spam settings that apply to the whole organization, take a look at [How to help ensure that a message isn't marked as spam](https://go.microsoft.com/fwlink/p/?LinkId=534224) or [Block email spam with the Office 365 spam filter to prevent false negative issues](https://go.microsoft.com/fwlink/p/?LinkId=534225). These are helpful if you have administrator-level control and you want to prevent false positives or false negatives.</span></span>
  
<span data-ttu-id="ad4c6-111">다음 비디오에서는 연결 필터 정책의 구성 단계를 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="ad4c6-111">The following video shows the configuration steps for the connection filter policy:</span></span>
  
> [!VIDEO https://www.microsoft.com/videoplayer/embed/b2f5bea3-e1a7-44b3-b7e2-07fac0d0ca40?autoplay=false]
  
## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="ad4c6-112">시작하기 전에 알아야 할 내용</span><span class="sxs-lookup"><span data-stu-id="ad4c6-112">What do you need to know before you begin?</span></span>
<span data-ttu-id="ad4c6-113"><a name="sectionSection0"> </a></span><span class="sxs-lookup"><span data-stu-id="ad4c6-113"></span></span>

- <span data-ttu-id="ad4c6-114">예상 완료 시간: 15분</span><span class="sxs-lookup"><span data-stu-id="ad4c6-114">Estimated time to complete: 15 minutes</span></span>
    
- <span data-ttu-id="ad4c6-p104">이 절차를 수행 하기 전에 사용 권한을 할당 해야 합니다. 필요한 사용 권한을 [Exchange Online의 기능 사용 권한](http://technet.microsoft.com/library/15073ce1-0917-403b-8839-02a2ebc96e16.aspx) 항목의 "스팸 방지" 항목을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="ad4c6-p104">You need to be assigned permissions before you can perform this procedure or procedures. To see what permissions you need, see the "Anti-spam" entry in the [Feature Permissions in Exchange Online](http://technet.microsoft.com/library/15073ce1-0917-403b-8839-02a2ebc96e16.aspx) topic.</span></span> 
    
- <span data-ttu-id="ad4c6-p105">해당 메시지를 허용하거나 차단할 보낸 사람의 IP 주소를 가져오려면 메시지의 인터넷 머리글을 확인합니다. [스팸 방지 메시지 헤더](anti-spam-message-headers.md)에 설명된 대로 CIP 머리글을 찾습니다. 다양한 전자 메일 클라이언트에서 메시지 헤더를 확인하는 방법에 대한 자세한 내용은 [메시지 헤더 분석기](https://go.microsoft.com/fwlink/p/?LinkId=306583) 항목을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="ad4c6-p105">To obtain the IP address of the sender whose messages you want to allow or block, you can check the Internet header of the message. Look for the CIP header as described in [Anti-spam message headers](anti-spam-message-headers.md). For information about how to view a message header in various email clients, see the [Message Header Analyzer](https://go.microsoft.com/fwlink/p/?LinkId=306583) topic.</span></span> 
    
- <span data-ttu-id="ad4c6-120">스팸으로 표시도 하지 IP 차단 목록에 IP 주소에서 보내는 전자 메일 메시지는 거부 하 고 추가 필터링이 발생 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad4c6-120">Email messages sent from an IP address on the IP Block list are rejected, not marked as spam, and no additional filtering occurs.</span></span>
    
- <span data-ttu-id="ad4c6-p106">원격 PowerShell을 통해 다음 연결 필터 절차를 수행할 수도 있습니다. 검토 하 여 설정 하 고 연결 필터 정책 설정을 편집 하려면 [Set-hostedconnectionfilterpolicy](http://technet.microsoft.com/library/ccb5731b-3fca-4d69-a91f-5049ea963fac.aspx) [Get HostedConnectionFilterPolicy](http://technet.microsoft.com/library/bd751db2-3f26-495b-8e5a-4fcab53b17fd.aspx) cmdlet을 사용 합니다. Exchange Online Protection에 연결 하려면 Windows PowerShell을 사용 하는 방법을 알아보려면 [Connect to Exchange Online Protection PowerShell를](https://go.microsoft.com/fwlink/p/?linkid=627290)참조 하십시오. Exchange Online에 연결 하려면 Windows PowerShell을 사용 하는 방법을 알아보려면 [Exchange Online PowerShell 연결](https://go.microsoft.com/fwlink/p/?linkid=396554)을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="ad4c6-p106">The following connection filter procedure can also be performed via remote PowerShell. Use the [Get-HostedConnectionFilterPolicy](http://technet.microsoft.com/library/bd751db2-3f26-495b-8e5a-4fcab53b17fd.aspx) cmdlet to review your settings, and the [Set-HostedConnectionFilterPolicy](http://technet.microsoft.com/library/ccb5731b-3fca-4d69-a91f-5049ea963fac.aspx) to edit your connection filter policy settings. To learn how to use Windows PowerShell to connect to Exchange Online Protection, see [Connect to Exchange Online Protection PowerShell](https://go.microsoft.com/fwlink/p/?linkid=627290). To learn how to use Windows PowerShell to connect to Exchange Online, see [Connect to Exchange Online PowerShell](https://go.microsoft.com/fwlink/p/?linkid=396554).</span></span>
    
- <span data-ttu-id="ad4c6-125">이 항목의 절차에 적용할 수 있는 바로 가기 키에 대한 자세한 내용은 **Keyboard shortcuts in Exchange 2013**을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="ad4c6-125">For information about keyboard shortcuts that may apply to the procedures in this topic, see **Keyboard shortcuts in the Exchange admin center**.</span></span>
    
## <a name="use-the-eac-to-edit-the-default-connection-filter-policy"></a><span data-ttu-id="ad4c6-126">EAC를 사용하여 기본 연결 필터 정책 편집</span><span class="sxs-lookup"><span data-stu-id="ad4c6-126">Use the EAC to edit the default connection filter policy</span></span>
<span data-ttu-id="ad4c6-127"><a name="sectionSection1"> </a></span><span class="sxs-lookup"><span data-stu-id="ad4c6-127"></span></span>

<span data-ttu-id="ad4c6-p107">EAC(Exchange 관리 센터)에서 연결 필터 정책을 편집하여 IP 허용 목록 또는 IP 차단 목록을 만듭니다. 연결 필터 정책 설정은 인바운드 메시지에만 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="ad4c6-p107">You create an IP Allow list or IP Block list by editing the connection filter policy in the Exchange admin center (EAC). The connection filter policy settings are applied to inbound messages only.</span></span>
  
1. <span data-ttu-id="ad4c6-130">EAC(Exchange 관리 센터)에서 **보호** \> **연결 필터**로 이동한 후 기본 정책을 두 번 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="ad4c6-130">In the Exchange admin center (EAC), navigate to **Protection** \> **Connection filter**, and then double-click the default policy.</span></span>
    
2. <span data-ttu-id="ad4c6-131">**연결 필터링** 메뉴 항목을 클릭한 후 원하는 목록을 만듭니다. IP 허용 목록이나 IP 차단 목록 중 하나를 만들거나 두 목록을 모두 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ad4c6-131">Click the **Connection filtering** menu item and then create the lists you want: an IP Allow list, an IP Block list, or both.</span></span> 
    
    <span data-ttu-id="ad4c6-p108">이 목록을 만들려면 ![아이콘 추가](media/ITPro-EAC-AddIcon.png)를 클릭합니다. 이후 표시되는 대화 상자에서 IP 주소나 주소 범위를 지정한 후 **확인**을 클릭합니다. 주소를 추가하려면 이 프로세스를 반복합니다. 주소를 추가한 후 IP 주소를 편집하거나 제거할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ad4c6-p108">To create these lists, click ![Add Icon](media/ITPro-EAC-AddIcon.png). In the subsequent dialog box, specify the IP address or address range, and then click **ok**. Repeat this process to add additional addresses. (You can also edit or remove IP addresses after they have been added.)</span></span>
    
    > [!NOTE]
    >  <span data-ttu-id="ad4c6-p109">두 목록에 IP 주소를 추가 하는 경우에서 보내는 전자 메일 허용 됩니다. > 여기서 nnn는 0에서 255 까지의 숫자 형식 nnn.nnn.nnn.nnn에 IPV4 IP 주소를 지정 합니다. 여기서 rr는 24에서 32 사이의 숫자 형식 nnn.nnn.nnn.nnn/rr에서 도메인간 라우팅 CIDR (Classless) 범위를 지정할 수도 있습니다. 24-32 범위 외부의 범위를 지정 하려면 [IP 허용 구성 시 추가 고려 사항 목록](configure-the-connection-filter-policy.md#bkmk_addtionalconsiderationswhenconfiguringipallowlists)를 참조 합니다. > 최대 1273 항목, 항목은 단일 IP 주소 또는 CIDR의 IP 주소 범위에서 /24/32 지정할 수 있습니다. > TLS 암호화 된 메시지를 보내는 경우 IPv6 주소 및 주소 범위가 지원 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ad4c6-p109">If you add an IP address to both lists, email sent from it is allowed. >  IPV4 IP addresses must be specified in the format nnn.nnn.nnn.nnn where nnn is a number from 0 to 255. You can also specify Classless Inter-Domain Routing (CIDR) ranges in the format nnn.nnn.nnn.nnn/rr where rr is a number from 24 to 32. To specify ranges outside of the 24 to 32 range, see [Additional considerations when configuring IP Allow lists](configure-the-connection-filter-policy.md#bkmk_addtionalconsiderationswhenconfiguringipallowlists). >  You can specify a maximum of 1273 entries, where an entry is either a single IP address or a CIDR range of IP addresses from /24 to /32. >  If you're sending TLS-encrypted messages, IPv6 addresses and address ranges are not supported.</span></span> 
  
3. <span data-ttu-id="ad4c6-p110">필요한 경우를 방지 하기 위해 **수신 허용 목록 사용** 확인란을 선택 특정 잘 알려진 보낸에서 전자 메일이 누락 되었습니다. 어떻게 합니까? Microsoft의 신뢰할 수 있는 보낸사람 제 3 자 원본에 구독합니다. 수신 허용 목록에이 사용 하 여 이러한 신뢰할 수 있는 보낸사람 스팸으로 표시 실수로 되지 하는 것을 의미 합니다. 수를 줄일 해야 하기 때문에이 옵션을 선택 하는 것이 좋습니다 가양성 (스팸으로 분류 하는 효율적인 메일)의 수신 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad4c6-p110">Optionally, select the **Enable safe list** check box to prevent missing email from certain well-known senders. How? Microsoft subscribes to third-party sources of trusted senders. Using this safe list means that these trusted senders aren't mistakenly marked as spam. We recommend selecting this option because it should reduce the number of false positives (good mail that's classified as spam) you receive.</span></span> 
    
4. <span data-ttu-id="ad4c6-p111">**저장**을 클릭합니다. 기본 정책 설정에 대한 요약이 오른쪽 창에 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="ad4c6-p111">Click **save**. A summary of your default policy settings appears in the right pane.</span></span>
    
## <a name="additional-considerations-when-configuring-ip-allow-lists"></a><span data-ttu-id="ad4c6-149">IP 허용 목록 구성 시 추가 고려 사항</span><span class="sxs-lookup"><span data-stu-id="ad4c6-149">Additional considerations when configuring IP Allow lists</span></span>
<span data-ttu-id="ad4c6-150"><a name="bkmk_addtionalconsiderationswhenconfiguringipallowlists"> </a></span><span class="sxs-lookup"><span data-stu-id="ad4c6-150"></span></span>

<span data-ttu-id="ad4c6-151">다음은 IP 허용 목록 구성 시 고려해야 하거나 알고 있어야 하는 추가 고려 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="ad4c6-151">The following are additional considerations you may want to consider or that you should be aware of when configuring an IP Allow list.</span></span>
  
### <a name="specifying-a-cidr-range-that-falls-outside-of-the-recommended-range"></a><span data-ttu-id="ad4c6-152">권장되는 범위를 벗어나는 CIDR 범위 지정</span><span class="sxs-lookup"><span data-stu-id="ad4c6-152">Specifying a CIDR range that falls outside of the recommended range</span></span>

<span data-ttu-id="ad4c6-p112">**바이패스 스팸 필터링** (의미는이 IP 주소 범위 내에서 받은 모든 메시지를 포함 하는 신뢰도 scl (스팸)를 설정 하는 IP 주소 범위에서 작동 하는 전송 규칙을 생성 해야 하는 /23/1에서 CIDR IP 주소 범위를 지정 하려면 "스팸 하지로 설정? 및 서비스에 의해 수행 되 추가 필터링 하지 않고). 그러나 이러한 IP 주소 중 하나에 표시 하는 경우 목록 Microsoft의 소유 블록의 일부 또는 모든 타사 차단 목록, 이러한 메시지를 차단 계속 됩니다. 따라서 강력 하 게 좋습니다/32를 /24 IP 주소 범위를 사용 하는.</span><span class="sxs-lookup"><span data-stu-id="ad4c6-p112">To specify a CIDR IP address range from /1 to /23, you must create a Transport rule that operates on the IP address range that sets the spam confidence level (SCL) to **Bypass spam filtering** (meaning that all messages received from within this IP address range are set to "not spam�? and no additional filtering is performed by the service). However, if any of these IP addresses appear on any of Microsoft's proprietary block lists or on any of our third-party block lists, these messages will still be blocked. It is therefore strongly recommended that you use the /32 to /24 IP address range.</span></span> 
  
<span data-ttu-id="ad4c6-157">이 전송 규칙을 만들려면 다음 단계를 수행합니다.</span><span class="sxs-lookup"><span data-stu-id="ad4c6-157">To create this Transport rule, perform the following steps.</span></span>
  
1. <span data-ttu-id="ad4c6-158">EAC에서 **메일 흐름** \> **규칙**으로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="ad4c6-158">In the EAC, navigate to **Mail flow** \> **Rules**.</span></span>
    
2. <span data-ttu-id="ad4c6-159">![아이콘 추가](media/ITPro-EAC-AddIcon.png)를 클릭한 다음 **새 규칙 만들기**를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="ad4c6-159">Click ![Add Icon](media/ITPro-EAC-AddIcon.png) and then select **Create a new rule**.</span></span>
    
3. <span data-ttu-id="ad4c6-160">규칙 이름을 지정하고 **기타 옵션**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="ad4c6-160">Give the rule a name and then click **More options**.</span></span>
    
4. <span data-ttu-id="ad4c6-161">**다음의 경우에 이 규칙 적용**에서 **보낸 사람**을 선택하고 **IP 주소가 이 범위에 속하거나 정확하게 일치함**을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="ad4c6-161">Under **Apply this rule if**, select **The sender** and then choose **IP address is in any of these ranges or exactly matches**.</span></span>
    
5. <span data-ttu-id="ad4c6-162">**IP 주소 지정**에서 IP 주소 범위를 지정하고 **추가**![아이콘 추가](media/ITPro-EAC-AddIcon.png)를 클릭한 다음 **확인**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="ad4c6-162">In the **specify IP addresses**, specify the IP address range, click **Add**![Add Icon](media/ITPro-EAC-AddIcon.png), and then click **ok**.</span></span>
    
6. <span data-ttu-id="ad4c6-p113">**다음 작업 수행** 상자에서 **메시지 속성 수정**을 선택한 다음 **SCL(스팸 지수) 설정**을 선택하여 동작을 설정합니다. **SCL 지정** 상자에서 **스팸 필터링 무시**를 선택한 후 **확인**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="ad4c6-p113">Under **Do the following** box, set the action by choosing **Modify the message properties** and then **set the spam confidence level (SCL)**. In the **specify SCL** box, select **Bypass spam filtering**, and click **ok**.</span></span>
    
7. <span data-ttu-id="ad4c6-p114">원하는 경우 규칙을 감사하고 규칙을 테스트하며 특정 기간 동안 규칙을 활성화하는 등 기타 옵션을 지정할 수 있습니다. 옵션을 적용하기 전에 규칙을 테스트하는 것이 좋습니다. [Manage Transport Rules](http://technet.microsoft.com/library/e7a81372-b6d7-4d1f-bc9e-a845a7facac2.aspx)에는 이러한 옵션에 대한 추가 정보가 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ad4c6-p114">If you'd like, you can make selections to audit the rule, test the rule, activate the rule during a specific time period, and other selections. We recommend testing the rule for a period before you enforce it. [Manage Transport Rules](http://technet.microsoft.com/library/e7a81372-b6d7-4d1f-bc9e-a845a7facac2.aspx) contains more information about these selections.</span></span> 
    
8. <span data-ttu-id="ad4c6-p115">**저장** 단추를 클릭하여 규칙을 저장합니다. 규칙이 규칙 목록에 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="ad4c6-p115">Click the **save** button to save the rule. It appears in your list of rules.</span></span> 
    
<span data-ttu-id="ad4c6-170">규칙을 만들어 적용하고 나면 지정한 IP 주소 범위에 대해 스팸 필터링이 무시됩니다.</span><span class="sxs-lookup"><span data-stu-id="ad4c6-170">After you create and enforce the rule, spam filtering is bypassed for the IP address range you specified.</span></span>
  
### <a name="scoping-an-ip-allow-list-exception-for-a-specific-domain"></a><span data-ttu-id="ad4c6-171">특정 도메인에 대해 IP 허용 목록 예외 범위 지정</span><span class="sxs-lookup"><span data-stu-id="ad4c6-171">Scoping an IP Allow list exception for a specific domain</span></span>

<span data-ttu-id="ad4c6-p116">일반적으로 안전한 것으로 간주되는 모든 도메인에 대한 IP 주소(또는 IP 주소 범위)를 IP 허용 목록에 추가하는 것이 좋습니다. 그러나 IP 허용 목록 항목을 모든 도메인에 적용하지는 않으려면 특정 도메인을 제외하는 전송 규칙을 만들면 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ad4c6-p116">In general, we recommend that you add the IP addresses (or IP address ranges) for all your domains that you consider safe to the IP Allow list. However, if you don't want your IP Allow List entry to apply to all your domains, you can create a Transport rule that excepts specific domains.</span></span> 
  
<span data-ttu-id="ad4c6-p117">예를 들어, 세 개의 도메인인 ContosoA.com, ContosoB.com 및 ContosoC.com이 있으며 IP 주소(단순하게 표현하기 위해 1.2.3.4 사용)를 추가하고 도메인 ContosoB.com에 대해서만 필터링을 건너뛰려 한다고 가정합니다. 모든 도메인에 대해 SCL(스팸 지수)을 -1(스팸이 아닌 것으로 분류됨을 의미함)로 설정하는 IP 허용 목록을 1.2.3.4에 대해 만듭니다. 그런 다음 모든 도메인(ContosoB.com 제외)에 대해 SCL을 0으로 설정하는 전송 규칙을 만들 수 있습니다. 그러면 ContosoB.com(규칙에서 예외로 나열되는 도메인)을 제외하고 IP 주소와 연결된 모든 도메인에 대해 메시지가 다시 검색됩니다. ContosoB.com의 SCL은 여전히 -1(필터링 건너뜀을 의미함)인 반면, ContosoA.com 및 ContosoC.com의 SCL은 0(콘텐츠 필터에 의해 다시 검색됨을 의미함)입니다.</span><span class="sxs-lookup"><span data-stu-id="ad4c6-p117">For example, let's say you have three domains: ContosoA.com, ContosoB.com, and ContosoC.com, and you want to add the IP address (for simplicity's sake, let's use 1.2.3.4) and skip filtering only for domain ContosoB.com. You would create an IP Allow list for 1.2.3.4, which sets the spam confidence level (SCL) to -1 (meaning it is classified as non-spam) for all domains. You can then create a Transport rule that sets the SCL for all domains except ContosoB.com to 0. This results in the message being rescanned for all domains associated with the IP address except for ContosoB.com which is the domain listed as the exception in the rule. ContosoB.com still has an SCL of -1 which means skip filtering, whereas ContosoA.com and ContosoC.com have SCLs of 0, meaning they will be rescanned by the content filter.</span></span>
  
<span data-ttu-id="ad4c6-179">이렇게 하려면 다음 단계를 수행합니다.</span><span class="sxs-lookup"><span data-stu-id="ad4c6-179">To do this, perform the following steps:</span></span>
  
1. <span data-ttu-id="ad4c6-180">EAC에서 **메일 흐름** \> **규칙**으로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="ad4c6-180">In the EAC, navigate to **Mail flow** \> **Rules**.</span></span>
    
2. <span data-ttu-id="ad4c6-181">![아이콘 추가](media/ITPro-EAC-AddIcon.png)를 클릭한 다음 **새 규칙 만들기**를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="ad4c6-181">Click ![Add Icon](media/ITPro-EAC-AddIcon.png) and then select **Create a new rule**.</span></span>
    
3. <span data-ttu-id="ad4c6-182">규칙 이름을 지정하고 **기타 옵션**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="ad4c6-182">Give the rule a name and then click **More options**.</span></span>
    
4. <span data-ttu-id="ad4c6-183">**다음의 경우 이 규칙 적용**에서 **보낸 사람**을 선택하고 **IP 주소가 이 범위에 속하거나 정확하게 일치함**을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="ad4c6-183">Under **Apply this rule if**, select **The sender** and then choose **IP address is in any of these ranges or exactly matches**.</span></span>
    
5. <span data-ttu-id="ad4c6-184">**IP 주소 지정** 상자에서 IP 허용 목록에 입력한 IP 주소 또는 IP 주소 범위를 지정하고 **추가**![아이콘 추가](media/ITPro-EAC-AddIcon.png)를 클릭한 다음 **확인**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="ad4c6-184">In the **specify IP addresses** box, specify the IP address or IP address range you entered in the IP Allow list, click **Add**![Add Icon](media/ITPro-EAC-AddIcon.png), and then click **ok**.</span></span>
    
6. <span data-ttu-id="ad4c6-p118">**다음 작업 실행**에서 **메시지 속성 수정**을 선택한 후 **SCL(스팸 지수) 설정**을 선택하여 동작을 설정합니다. **SCL 지정** 상자에서 **0**을 선택한 후 **확인**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="ad4c6-p118">Under **Do the following**, set the action by choosing **Modify the message properties** and then **set the spam confidence level (SCL)**. In the **specify SCL** box, select **0**, and click **ok**.</span></span>
    
7. <span data-ttu-id="ad4c6-187">**예외 추가**를 클릭하고 **다음의 경우 제외**에서 **보낸 사람**을 선택하고 **도메인**을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="ad4c6-187">Click **add exception**, and under **Except if**, select **The sender** and choose **domain is**.</span></span> 
    
8. <span data-ttu-id="ad4c6-p119">**도메인 지정** 상자에 스팸 필터링을 무시할 도메인을 입력합니다(예: **contosob.com**). **추가**![아이콘 추가](media/ITPro-EAC-AddIcon.png)를 클릭하여 이 도메인을 구 목록으로 이동합니다. 도메인을 예외로 더 추가하려면 이 단계를 반복하고 완료되면 **확인**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="ad4c6-p119">In the **specify domain** box, enter the domain for which you want to bypass spam filtering, such as **contosob.com**. Click **Add**![Add Icon](media/ITPro-EAC-AddIcon.png) to move it to the list of phrases. Repeat this step if you want to add additional domains as exceptions, and click **ok** when you are finished.</span></span> 
    
9. <span data-ttu-id="ad4c6-p120">원하는 경우 규칙을 감사하고 규칙을 테스트하며 특정 기간 동안 규칙을 활성화하는 등 기타 옵션을 지정할 수 있습니다. 옵션을 적용하기 전에 규칙을 테스트하는 것이 좋습니다. [Manage Transport Rules](http://technet.microsoft.com/library/e7a81372-b6d7-4d1f-bc9e-a845a7facac2.aspx)에는 이러한 옵션에 대한 추가 정보가 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ad4c6-p120">If you'd like, you can make selections to audit the rule, test the rule, activate the rule during a specific time period, and other selections. We recommend testing the rule for a period before you enforce it. [Manage Transport Rules](http://technet.microsoft.com/library/e7a81372-b6d7-4d1f-bc9e-a845a7facac2.aspx) contains more information about these selections.</span></span> 
    
10. <span data-ttu-id="ad4c6-p121">**저장** 단추를 클릭하여 규칙을 저장합니다. 규칙이 규칙 목록에 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="ad4c6-p121">Click the **save** button to save the rule. It appears in your list of rules.</span></span> 
    
<span data-ttu-id="ad4c6-196">규칙을 만들어 적용하고 나면 지정한 IP 주소 또는 IP 주소 범위에 대한 스팸 필터링이 입력한 도메인 예외에 대해서만 무시됩니다.</span><span class="sxs-lookup"><span data-stu-id="ad4c6-196">After you create and enforce the rule, spam filtering for the IP address or IP address range you specified is bypassed only for the domain exception you entered.</span></span>
  
## <a name="new-to-office-365"></a><span data-ttu-id="ad4c6-197">Office 365의 새로운 기능</span><span class="sxs-lookup"><span data-stu-id="ad4c6-197">New to Office 365?</span></span>
<span data-ttu-id="ad4c6-198"><a name="sectionSection3"> </a></span><span class="sxs-lookup"><span data-stu-id="ad4c6-198"></span></span>

||
|:-----|
|<span data-ttu-id="ad4c6-p122">![LinkedIn Learning용 단축 아이콘](media/eac8a413-9498-4220-8544-1e37d1aaea13.png) **Office 365를 처음 사용하시나요?**         LinkedIn Learning에서 제공하는 **Office 365 admins and IT pros**의 무료 비디오 과정을 확인해보세요.</span><span class="sxs-lookup"><span data-stu-id="ad4c6-p122">![The short icon for LinkedIn Learning](media/eac8a413-9498-4220-8544-1e37d1aaea13.png) **New to Office 365?**         Discover free video courses for **Office 365 admins and IT pros**, brought to you by LinkedIn Learning.</span></span> |
   
## <a name="for-more-information"></a><span data-ttu-id="ad4c6-201">자세한 내용</span><span class="sxs-lookup"><span data-stu-id="ad4c6-201">For more information</span></span>
<span data-ttu-id="ad4c6-202"><a name="sectionSection4"> </a></span><span class="sxs-lookup"><span data-stu-id="ad4c6-202"></span></span>

[<span data-ttu-id="ad4c6-203">수신 허용-보낸사람 및 수신된 거부 목록 Exchange Online</span><span class="sxs-lookup"><span data-stu-id="ad4c6-203">Safe sender and blocked sender lists in Exchange Online</span></span>](safe-sender-and-blocked-sender-lists-faq.md)
  
[<span data-ttu-id="ad4c6-204">스팸 필터 정책 구성</span><span class="sxs-lookup"><span data-stu-id="ad4c6-204">Configure your spam filter policies</span></span>](configure-your-spam-filter-policies.md)
  
[<span data-ttu-id="ad4c6-205">아웃 바운드 스팸 정책 구성</span><span class="sxs-lookup"><span data-stu-id="ad4c6-205">Configure the outbound spam policy</span></span>](configure-the-outbound-spam-policy.md)
  
[<span data-ttu-id="ad4c6-206">메시지가 스팸으로 표시되지 않는지 확인하는 방법</span><span class="sxs-lookup"><span data-stu-id="ad4c6-206">How to help ensure that a message isn't marked as spam</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=534224)
  
[<span data-ttu-id="ad4c6-207">Office 365 스팸 필터로 전자 메일 스팸을 차단하여 거짓 부정 문제 방지</span><span class="sxs-lookup"><span data-stu-id="ad4c6-207">Block email spam with the Office 365 spam filter to prevent false negative issues</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=534225)
  

