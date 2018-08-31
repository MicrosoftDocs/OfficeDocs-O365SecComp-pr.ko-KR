---
title: Office 365에서 조직 차원의 수신 허용 - 보낸 사람 또는 수신 거부 목록 만들기
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 8/8/2015
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
search.appverid:
- MET150s
ms.assetid: 9721b46d-cbea-4121-be51-542395e6fd21
description: 조정할 수 하 고 해당 메시지를 신뢰 하기 때문에 특정 한 보낸에서 메일을 받을 해야 하려는 경우에 Exchange 관리 센터에서 스팸 필터 정책에서 허용 목록.
ms.openlocfilehash: a90679fc900ca5695904898af3627fc1900a8545
ms.sourcegitcommit: e9dca2d6a7838f98bb7eca127fdda2372cda402c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/21/2018
ms.locfileid: "23003167"
---
# <a name="create-organization-wide-safe-sender-or-blocked-sender-lists-in-office-365"></a><span data-ttu-id="c72d6-103">Office 365에서 조직 차원의 수신 허용 - 보낸 사람 또는 수신 거부 목록 만들기</span><span class="sxs-lookup"><span data-stu-id="c72d6-103">Create organization-wide safe sender or blocked sender lists in Office 365</span></span>
  
<span data-ttu-id="c72d6-p101">조정할 수 하 고 해당 메시지를 신뢰 하기 때문에 특정 한 보낸에서 메일을 받을 해야 하려는 경우 대화 **보호** 에 Exchange 관리 센터 (EAC)에서 스팸 필터 정책에서 허용 목록 \> **스팸 필터**입니다. [스팸 필터 정책 구성](configure-your-spam-filter-policies.md)에서이 대 한 자세한 내용을 알아봅니다. 다른 옵션 같은 도메인 또는 사용자 기반 works 허용 목록 스팸 필터에는 Exchange 전송 규칙을 만들 수 있습니다. 너무 비슷한 방법으로 특정 도메인 또는 사용자가 보낸 메시지를 차단할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c72d6-p101">If you want to be sure that you receive mail from a particular sender, because you trust them and their messages, you can adjust your allow list in a spam filter policy in the Exchange admin center (EAC) at **Protection** \> **Spam filter**. Learn more about this at [Configure your spam filter policies](configure-your-spam-filter-policies.md). Another option would be create an Exchange transport rule that works like the domain or user-based allow list in the spam filter. You can block messages sent from a particular domain or user in a similar manner too.</span></span>
  
<span data-ttu-id="c72d6-p102">전송 규칙에도 유용 하다이 이런 메시지 헤더 또는 첨부 파일의 이름을 확인 하는 등 복잡 한 조건을 지정 하기 위해 필터링 할 때 또는 메시지에는 고 지 사항을 추가 (영문) 또는 시간 간격을 적용 하는 등의 복잡 한 작업을 추가 하려는 경우에 rul e 활성 상태입니다. 그러나 특정 보낸 사람이 나 도메인에서 보내는 전자 메일 스팸 필터링 무시 되도록 것이 좋습니다 스팸 필터 정책에 추가 합니다. 시작 하기이 EAC에서 **보호** 를 이동 하 여 \> **스팸 필터**입니다. 자세한 내용은 [스팸 필터 정책 구성](configure-your-spam-filter-policies.md).</span><span class="sxs-lookup"><span data-stu-id="c72d6-p102">A transport rule would be useful in this situation if you need to filter for complex criteria such as checking message headers or the names of attachments or if you want to add complex actions such as adding a disclaimer to the message or applying a time period where the rule is active. However, the preferred method to make sure emails from a specific sender or domain bypass your spam filter is to add them to your spam filter policy. Get started with this in the EAC by going to **Protection** \> **Spam filter**. Learn more at [Configure your spam filter policies](configure-your-spam-filter-policies.md).</span></span>
  
> [!TIP]
> <span data-ttu-id="c72d6-p103">도메인 스푸핑 될 수 있으므로 도메인 기반 목록을 전송 규칙에는 IP 주소를 기준으로 목록으로 안전 하지 않습니다. 또한 보내는 IP 주소가 차단 목록에 있으면 해당 도메인에 대 한 필터링 하는 경우에에 여전히 차단 됩니다 또는 사용자가 무시 되 고 있습니다. 즉, 도메인 또는 사용자에 전송 규칙을 글로벌 IP 차단 목록 재정의 하지 않습니다. 대부분의 경우에서 IP 주소를 기준으로 목록을 사용 하는 것이 좋습니다. IP 주소를 기준으로 목록을 만들려면 IP 허용 목록 또는 IP 차단 목록 연결 필터에 사용할 수 있습니다. 콘텐츠 필터에 의해 이러한 IP 주소에서 보낸 모든 메시지가 확인 되지 않습니다. IP 허용 목록 또는 IP 차단 목록에 IP 주소를 추가 하 여 연결 필터 정책 구성 하는 방법에 대 한 자세한 내용은 [연결 필터 정책 구성](configure-the-connection-filter-policy.md)을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="c72d6-p103">A domain-based list in a transport rule isn't as secure as an IP address-based list, because domains can be spoofed. Also, if the sending IP address is on a Block list, it will still be blocked even if filtering for the domain or user is being bypassed. This is because a transport rule on a domain or user does not override the global IP Block list. We recommend using an IP address-based list in most cases. To create an IP address-based list, you can use the IP Allow list or IP Block list in the connection filter. Any messages sent from these IP addresses aren't checked by the content filter. For instructions on how to configure the connection filter policy by adding IP addresses to the IP Allow list or IP Block list, see [Configure the connection filter policy](configure-the-connection-filter-policy.md).</span></span> 
  
<span data-ttu-id="c72d6-119">전송 규칙과 관련된 추가 관리 작업에 대한 자세한 내용은 [Transport Rules](http://technet.microsoft.com/library/743bd525-0ca2-426d-b76c-b4a052bc8886.aspx)을 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="c72d6-119">For additional management tasks related to transport rules, see [Transport Rules](http://technet.microsoft.com/library/743bd525-0ca2-426d-b76c-b4a052bc8886.aspx).</span></span>
  
## <a name="use-the-eac-to-customize-a-block-or-allow-list-to-prevent-or-receive-email-from-a-domain-or-user"></a><span data-ttu-id="c72d6-120">EAC를 사용 하 여 블록을 사용자 지정 하거나 목록에서 방지 하거나 도메인 또는 사용자가 전자 메일을 수신 허용</span><span class="sxs-lookup"><span data-stu-id="c72d6-120">Use the EAC to customize a block or allow list to prevent or receive email from a domain or user</span></span>

1. <span data-ttu-id="c72d6-121">EAC에서 **보호** 로 이동 \> **스팸 필터**입니다.</span><span class="sxs-lookup"><span data-stu-id="c72d6-121">In the EAC, go to **Protection** \> **Spam filter**.</span></span> 
    
2. <span data-ttu-id="c72d6-122">**일반** 페이지에서 다음 중 하나를 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="c72d6-122">On the **general** page, do one of the following:</span></span> 
    
  - <span data-ttu-id="c72d6-123">기본 정책 또는 기존 정책을 편집 하는 것을 시작 하기 위해 두번클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="c72d6-123">Double-click the default policy or an existing policy in order to start editing it.</span></span>
    
  - <span data-ttu-id="c72d6-124">사용자, 그룹 및 조직에서 도메인에 적용할 수 있는 사용자 지정 스팸 필터 정책을 새로 만들려면 **새로 만들기** 를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="c72d6-124">Click **New** in order to create a new custom spam-filter policy that can be applied to users, groups, and domains in your organization.</span></span> 
    
3. <span data-ttu-id="c72d6-p104">**허용 목록** 페이지에서 항목을 보낸 사람이 나 도메인의 받은 편지 함으로 배달 될 항상 등을 지정할 수 있습니다. 이러한 항목에 대 한 전자 메일 스팸 필터에 의해 처리 되지 않습니다. 다음을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="c72d6-p104">On the **Allow Lists** page, you can specify entries, such as senders or domains, that will always be delivered to the inbox. Email from these entries is not processed by the spam filter. Do the following:</span></span> 
    
  - <span data-ttu-id="c72d6-p105">신뢰할 수 있는 보낸 사람이 보낸 사람에 게 허용 된 대화 상대를 추가 합니다. **추가**클릭 하 고 선택 대화 상자에서 허용 하려는 보낸사람 주소를 추가 합니다. 세미콜론으로 또는 새 줄을 사용 하 여 여러 항목을 구분할 수 있습니다. **허용 목록을** 페이지로 돌아가려면 확인을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="c72d6-p105">Add trusted senders to the Sender allow list. Click **Add**, and then in the selection dialog box, add the sender addresses you wish to allow. You can separate multiple entries using a semi-colon or a new line. Click ok to return to the **Allow Lists** page.</span></span> 
    
  - <span data-ttu-id="c72d6-p106">신뢰할 수 있는 도메인의 도메인을 허용 된 대화 상대를 추가 합니다. **추가**클릭 한 다음 선택 대화 상자에서 허용 하려는 도메인을 추가 합니다. 세미콜론으로 또는 새 줄을 사용 하 여 여러 항목을 구분할 수 있습니다. **허용 목록을** 페이지로 돌아가려면 확인을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="c72d6-p106">Add trusted domains to the Domain allow list. Click **Add**, and then in the selection dialog box, add the domains you wish to allow. You can separate multiple entries using a semi-colon or a new line. Click ok to return to the **Allow Lists** page.</span></span> 
    
    > [!CAUTION]
    > <span data-ttu-id="c72d6-136">최상위 도메인을 허용 하는 경우 될 하지 않으려고 전자 메일 하는 받은 편지 함으로 배달 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c72d6-136">If you allow top-level domains, it's likely that email you don't want will be delivered to an inbox.</span></span> 
  
4. <span data-ttu-id="c72d6-p107">**차단 목록** 페이지에서 항상 스팸으로 표시될 항목(예: 보낸 사람 또는 도메인)을 지정할 수 있습니다. 서비스는 이러한 항목과 일치하는 전자 메일에 구성된 높은 정확도 스팸 작업을 적용합니다.</span><span class="sxs-lookup"><span data-stu-id="c72d6-p107">On the **Block Lists** page, you can specify entries, such as senders or domains, that will always be marked as spam. The service will apply the configured high confidence spam action on email that matches these entries.</span></span> 
    
  - <span data-ttu-id="c72d6-p108">원하지 않는 보낸사람 보낸 사람이 차단 목록에 추가 합니다. **추가**클릭![아이콘 추가](media/ITPro-EAC-AddIcon.gif), 하 고 선택 대화 상자에서 차단할 보낸사람 주소를 추가 합니다. 세미콜론으로 또는 새 줄을 사용 하 여 여러 항목을 구분할 수 있습니다. **확인** **차단 목록** 페이지로 돌아가려면를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="c72d6-p108">Add unwanted senders to the Sender block list. Click **Add**![Add Icon](media/ITPro-EAC-AddIcon.gif), and then in the selection dialog box, add the sender addresses you want to block. You can separate multiple entries using a semi-colon or a new line. Click **Ok** to return to the **Block Lists** page.</span></span> 
    
  - <span data-ttu-id="c72d6-p109">도메인 차단 목록에 원치 않는 도메인을 추가 합니다. **추가**클릭![아이콘 추가](media/ITPro-EAC-AddIcon.gif), 하 고 선택 대화 상자에서 차단할 도메인을 추가 합니다. 세미콜론으로 또는 새 줄을 사용 하 여 여러 항목을 구분할 수 있습니다. **확인** **차단 목록** 페이지로 돌아가려면를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="c72d6-p109">Add unwanted domains to the Domain block list. Click **Add**![Add Icon](media/ITPro-EAC-AddIcon.gif), and then in the selection dialog box, add the domains you want to block. You can separate multiple entries using a semi-colon or a new line. Click **Ok** to return to the **Block Lists** page.</span></span> 
    
    > [!CAUTION]
    > <span data-ttu-id="c72d6-147">최상위 도메인을 차단 하는 경우에는 원하는 전자 메일 스팸으로 표시 되어야 하는 것 같습니다.</span><span class="sxs-lookup"><span data-stu-id="c72d6-147">If you block top-level domains, it's likely that email you want will be marked as spam.</span></span> 
  
## <a name="what-do-you-need-to-know-before-you-begin-creating-a-transport-rule"></a><span data-ttu-id="c72d6-148">전송 규칙 만들기 (영문)를 시작 하기 전에 필요한</span><span class="sxs-lookup"><span data-stu-id="c72d6-148">What do you need to know before you begin creating a transport rule?</span></span>
    
- <span data-ttu-id="c72d6-p110">스팸 필터링 무시 또는 전자 메일 보낸 사람이 나 도메인에 대 한 스팸으로 표시 하는 전송 규칙을 만들 필요가 없습니다. 차단 또는 특정 보낸 사람이 나 도메인을 허용 하 고 연결 하지 않고는 추가 조건의 하는 경우이 전송 규칙 대신 스팸 정책에서 허용 목록 및 Exchange Online Protection 블록을 사용 합니다. [스팸 필터 정책 구성](configure-your-spam-filter-policies.md)에서이 대 한 자세한 내용을 알아봅니다.</span><span class="sxs-lookup"><span data-stu-id="c72d6-p110">You don't need to create a transport rule to bypass spam filtering or mark email as spam for a sender or domain. Use the Exchange Online Protection block and allow lists in a spam policy instead of this transport rule if you simply want to block or allow a specific sender or domain and not attach any extra conditions. Learn more about this at [Configure your spam filter policies](configure-your-spam-filter-policies.md).</span></span>
    
- <span data-ttu-id="c72d6-p111">이러한 절차를 수행하려면 먼저 사용 권한을 할당받아야 합니다. 필요한 사용 권한을 확인하려면 다음을 참조하세요. [Messaging policy and compliance permissions](http://technet.microsoft.com/library/ec4d3b9f-b85a-4cb9-95f5-6fc149c3899b.aspx)의 "전송 규칙" 항목</span><span class="sxs-lookup"><span data-stu-id="c72d6-p111">You need to be assigned permissions before you can perform this procedure or procedures. To see what permissions you need, see the "Transport rules" entry in the [Messaging policy and compliance permissions](http://technet.microsoft.com/library/ec4d3b9f-b85a-4cb9-95f5-6fc149c3899b.aspx) topic.</span></span> 
    
- <span data-ttu-id="c72d6-154">이 항목의 절차에 적용할 수 있는 바로 가기 키에 대한 자세한 내용은 **Exchange 관리 센터의 바로 가기 키**을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="c72d6-154">For information about keyboard shortcuts that may apply to the procedures in this topic, see **Keyboard shortcuts in the Exchange admin center**.</span></span>
    
> [!TIP]
> <span data-ttu-id="c72d6-p112">문제가 있습니까? Exchange 포럼에 도움을 요청 합니다. [Exchange Server](https://go.microsoft.com/fwlink/p/?linkId=60612), [Exchange Online](https://go.microsoft.com/fwlink/p/?linkId=267542)또는 [Exchange Online Protection](https://go.microsoft.com/fwlink/p/?linkId=285351)에서 포럼을 방문 하십시오.</span><span class="sxs-lookup"><span data-stu-id="c72d6-p112">Having problems? Ask for help in the Exchange forums. Visit the forums at [Exchange Server](https://go.microsoft.com/fwlink/p/?linkId=60612), [Exchange Online](https://go.microsoft.com/fwlink/p/?linkId=267542), or [Exchange Online Protection](https://go.microsoft.com/fwlink/p/?linkId=285351).</span></span> 
  
## <a name="use-the-eac-to-create-a-transport-rule-to-bypass-spam-filtering-for-a-domain-or-user"></a><span data-ttu-id="c72d6-158">EAC를 사용 하 여 도메인 또는 사용자에 대해 스팸 필터링을 무시 하도록 전송 규칙을 만들려면</span><span class="sxs-lookup"><span data-stu-id="c72d6-158">Use the EAC to create a transport rule to bypass spam filtering for a domain or user</span></span>

1. <span data-ttu-id="c72d6-p113">EAC에서 **메일 흐름** 으로 이동 \> **규칙**입니다. **추가** 선택 ![아이콘 추가](media/ITPro-EAC-AddIcon.gif) **바이패스 스팸 필터링**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="c72d6-p113">In the EAC, navigate to **Mail flow** \> **Rules**. Choose **Add** ![Add Icon](media/ITPro-EAC-AddIcon.gif) and then choose **Bypass spam filtering**.</span></span>
    
2. <span data-ttu-id="c72d6-p114">규칙에 이름을 지정합니다. **다음의 경우 이 규칙 적용**에서 **보낸 사람**을 선택하고 다음 조건 중 하나를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="c72d6-p114">Give the rule a name. Under **Apply this rule if**, choose **The sender** and then select one of the following conditions:</span></span> 
    
  - <span data-ttu-id="c72d6-p115">도메인을 지정 하려는 경우에 **도메인을**선택 합니다. **도메인 지정** 대화 상자에서 안전 하 고, contoso.com 등으로 지정 하려는 경우 보낸 사람의 도메인을 입력 합니다. **추가** ![아이콘 추가](media/ITPro-EAC-AddIcon.gif) 는 구 목록으로 이동 합니다. 작업이 완료 되 면 **확인** 을 클릭 하 고 추가 도메인을 추가 하려는 경우이 단계를 반복 합니다.</span><span class="sxs-lookup"><span data-stu-id="c72d6-p115">If you want to specify a domain, choose **domain is**. In the **Specify domain** dialog box, enter the domain of the sender you want to designate as safe, such as contoso.com. **Add** ![Add Icon](media/ITPro-EAC-AddIcon.gif) to move it to the list of phrases. Repeat this step if you want to add additional domains, and click **OK** when you are finished.</span></span> 
    
  - <span data-ttu-id="c72d6-p116">사용자를 지정하려면 **이 사람**을 선택합니다. **구성원 선택** 대화 상자의 사용자 유형 목록에서 사용자를 추가하고 **이름 확인**을 클릭합니다. 사용자를 더 추가하려면 이 단계를 반복하고 완료되면 **확인**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="c72d6-p116">If you want to specify a user, choose **is this person**. In the **Select members** dialog box, add the user from the list or type the user and click **Check names**. Repeat this step if you want to add additional users, and click **OK** when you are finished.</span></span> 
    
3. <span data-ttu-id="c72d6-170">다른 규칙이 없는 바이패스 동작을 되돌릴 수 있는지 확인 하려면 **추가 규칙 처리 중지** 확인란을 선택</span><span class="sxs-lookup"><span data-stu-id="c72d6-170">Select the **Stop processing more rules** check box to ensure that no other rule can reverse the bypass action</span></span> 
    
4. <span data-ttu-id="c72d6-171">**메시지에서 일치 하는 보낸사람 주소** 옵션에 대 한 **헤더 또는 봉투를**선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="c72d6-171">For the **Match sender address in message** option, select **Header or envelope**.</span></span>
    
5. <span data-ttu-id="c72d6-p117">원하는 경우에 감사 규칙, 규칙을 테스트, 특정 기간 동안 규칙 활성화를 선택 하 고 다른 선택 항목을 만들 수 있습니다. 조직에 적용 하기 전에 시간 기간에 대 한 규칙을 테스트 하는 것이 좋습니다. 이러한 선택 항목에 대 한 자세한 내용은 [전송 규칙 관리](http://technet.microsoft.com/library/e7a81372-b6d7-4d1f-bc9e-a845a7facac2.aspx)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="c72d6-p117">If you'd like, you can make selections to audit the rule, test the rule, activate the rule during a specific time period, and other selections. We recommend testing the rule for a period of time before enforcing it in your organization. For more information about these selections, see [Manage Transport Rules](http://technet.microsoft.com/library/e7a81372-b6d7-4d1f-bc9e-a845a7facac2.aspx).</span></span>
    
6. <span data-ttu-id="c72d6-175">**저장**을 선택하여 규칙을 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="c72d6-175">Choose **Save** to save the rule.</span></span> 
    
<span data-ttu-id="c72d6-176">규칙을 만들어 적용하고 나면 지정한 도메인 또는 사용자에 대해 스팸 필터링이 무시됩니다.</span><span class="sxs-lookup"><span data-stu-id="c72d6-176">After you create and enforce the rule, spam filtering is bypassed for the domain or user you specified.</span></span>
  
## <a name="use-the-eac-to-create-a-transport-rule-that-blocks-messages-sent-from-a-domain-or-user"></a><span data-ttu-id="c72d6-177">EAC를 사용 하 여 도메인 또는 사용자가 보낸 메시지를 차단 하는 전송 규칙을 만들려면</span><span class="sxs-lookup"><span data-stu-id="c72d6-177">Use the EAC to create a transport rule that blocks messages sent from a domain or user</span></span>

1. <span data-ttu-id="c72d6-p118">EAC에서 **메일 흐름** 으로 이동 \> **규칙**입니다. **추가** 선택 ![아이콘 추가](media/ITPro-EAC-AddIcon.gif) 하 고 **새 규칙 만들기**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="c72d6-p118">In the EAC, navigate to **Mail flow** \> **Rules**. Choose **Add** ![Add Icon](media/ITPro-EAC-AddIcon.gif) and then choose **Create a new rule**.</span></span>
    
2. <span data-ttu-id="c72d6-180">규칙 이름을 지정하고 **기타 옵션**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="c72d6-180">Give the rule a name and then click **More options**.</span></span> 
    
3. <span data-ttu-id="c72d6-181">**다음의 경우 이 규칙 적용**에서 **보낸 사람**을 선택하고 다음 조건 중 하나를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="c72d6-181">Under **Apply this rule if**, choose **The sender** and then select one of the following conditions:</span></span> 
    
  - <span data-ttu-id="c72d6-p119">도메인을 지정 하려는 경우에 **도메인을**선택 합니다. 지정 도메인 대화 상자에서 contoso.com과 같은 메시지를 차단 하려는 보낸 사람이 도메인을 입력 합니다. **추가** 클릭 ![아이콘 추가](media/ITPro-EAC-AddIcon.gif) 는 구 목록으로 이동 합니다. 작업이 완료 되 면 **확인** 을 클릭 하 고 추가 도메인을 추가 하려는 경우이 단계를 반복 합니다.</span><span class="sxs-lookup"><span data-stu-id="c72d6-p119">If you want to specify a domain, choose **domain is**. In the Specify domain dialog box, enter the sender domain from which you want to block messages, such as contoso.com. Click **Add** ![Add Icon](media/ITPro-EAC-AddIcon.gif) to move it to the list of phrases. Repeat this step if you want to add additional domains, and click **OK** when you are finished.</span></span> 
    
  - <span data-ttu-id="c72d6-p120">사용자를 지정하려면 **이 사람**을 선택합니다. **구성원 선택** 대화 상자의 사용자 유형 목록에서 사용자를 추가하고 **이름 확인**을 클릭합니다. 사용자를 더 추가하려면 이 단계를 반복하고 완료되면 **확인**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="c72d6-p120">If you want to specify a user, choose **is this person**. In the **Select members** dialog box, add the user from the list or type the user and click **Check names**. Repeat this step if you want to add additional users, and click **OK** when you are finished.</span></span> 
    
4. <span data-ttu-id="c72d6-189">**다음 작업 실행**에서 **메시지 차단**을 선택한 다음 **아무에게도 알리지 않고 메시지 삭제**와 같은 다른 옵션 중 하나를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="c72d6-189">Under **Do the following**, choose **Block the message** and then click one of the other options such as **Delete the message without notifying anyone**.</span></span>
    
5. <span data-ttu-id="c72d6-190">**기타 옵션**을 클릭 한 다음 **메시지에서 일치 하는 보낸사람 주소** 옵션에 대 한 **헤더 또는 봉투를**선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="c72d6-190">Click **More options**, and then for the **Match sender address in message** option, select **Header or envelope**.</span></span>
    
6. <span data-ttu-id="c72d6-p121">원하는 경우에 감사 규칙, 규칙을 테스트, 특정 기간 동안 규칙 활성화를 선택 하 고 다른 선택 항목을 만들 수 있습니다. 조직에 적용 하기 전에 시간 기간에 대 한 규칙을 테스트 하는 것이 좋습니다. 이러한 선택 항목에 대 한 자세한 내용은 [전송 규칙 관리](http://technet.microsoft.com/library/e7a81372-b6d7-4d1f-bc9e-a845a7facac2.aspx)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="c72d6-p121">If you'd like, you can make selections to audit the rule, test the rule, activate the rule during a specific time period, and other selections. We recommend testing the rule for a period of time before enforcing it in your organization. For more information about these selections, see [Manage Transport Rules](http://technet.microsoft.com/library/e7a81372-b6d7-4d1f-bc9e-a845a7facac2.aspx).</span></span>
    
7. <span data-ttu-id="c72d6-194">**저장**을 선택하여 규칙을 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="c72d6-194">Choose **Save** to save the rule.</span></span> 
    
<span data-ttu-id="c72d6-195">규칙을 만들어 적용하고 나면 지정한 도메인 또는 사용자가 보내는 모든 메시지가 차단됩니다.</span><span class="sxs-lookup"><span data-stu-id="c72d6-195">After you create and enforce the rule, any messages sent from the domain or user you specify will be blocked.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="c72d6-196">참고 항목</span><span class="sxs-lookup"><span data-stu-id="c72d6-196">See also</span></span>

[<span data-ttu-id="c72d6-197">스팸 필터 정책 구성</span><span class="sxs-lookup"><span data-stu-id="c72d6-197">Configure your spam filter policies</span></span>](configure-your-spam-filter-policies.md)
  
[<span data-ttu-id="c72d6-198">전송 규칙을 사용하여 대량 전자 메일 필터링 구성</span><span class="sxs-lookup"><span data-stu-id="c72d6-198">Use transport rules to configure bulk email filtering</span></span>](use-transport-rules-to-configure-bulk-email-filtering.md)

