---
title: 스팸 전자 메일을 보낸 후 차단 목록에서 사용자, 도메인 또는 IP 주소를 제거
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 6/20/2018
ms.audience: ITPro
ms.topic: article
f1_keywords:
- ms.exch.eac.ActionCenter
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 712cfcc1-31e8-4e51-8561-b64258a8f1e5
description: 사용자는 계속 해 서 스팸으로 분류 하는 Office 365에서 전자 메일 메시지를 보내는, 모든 자세한 메시지를 보내지 못하도록 차단 됩니다.
ms.openlocfilehash: 87b7083fe1345a15ea582f12a5b0d417bbe6b568
ms.sourcegitcommit: e9dca2d6a7838f98bb7eca127fdda2372cda402c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/21/2018
ms.locfileid: "23002606"
---
# <a name="removing-a-user-domain-or-ip-address-from-a-block-list-after-sending-spam-email"></a><span data-ttu-id="4983b-103">스팸 전자 메일을 보낸 후 차단 목록에서 사용자, 도메인 또는 IP 주소를 제거</span><span class="sxs-lookup"><span data-stu-id="4983b-103">Removing a user, domain, or IP address from a block list after sending spam email</span></span>

<span data-ttu-id="4983b-104">사용자는 계속 해 서 스팸으로 분류 하는 Office 365에서 전자 메일 메시지를 보내는, 모든 자세한 메시지를 보내지 못하도록 차단 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4983b-104">If a user continuously sends email messages from Office 365 that is classified as spam, they will be blocked from sending any more messages.</span></span> 
  
<span data-ttu-id="4983b-105">받은 배달 못함 보고서 (NDR 또는 전자 메일 메시지를 보내려면 실패) 보낸 전자 메일 메시지를 보내지 못하도록 차단 되 면 자신이 직접 차단을 해제 하기 위해 수행 해야하는 단계에 대 한 구체적인 정보를 제공 하는 합니다.</span><span class="sxs-lookup"><span data-stu-id="4983b-105">When a sender is blocked from sending emails messages, they receive a Non-Delivery Report (NDR or email failed to send message) that provides specific information about the steps that they have to take to unblock themselves.</span></span>
  
<span data-ttu-id="4983b-p101">뿐 아니라 개별 사용자가 차단 될 수 있습니다,이 서비스는 하지만 특정 웹사이트, 도메인 및 IP 주소 차단 될 수 있습니다. 경우에 따라 도메인 이나 웹사이트 추가할 수 차단 목록에 스팸 메시지에 나타나는 해 서 합니다. Office 365 관리자, 사용자, 웹사이트, 도메인 및 타사 차단 목록에서 제거 하는 IP 주소를 가져올 시도할 수 있습니다. 이 항목의 맨 아래에 표에 링크를 사용 하 여 각 제 3 자에 게 문의 하 고 지침을 따릅니다. Office 365 계정에 메시지를 보낼 수 없는 Office 365 외부 사용자, 하는 경우 자신의 계정 외부 수신된 거부 목록에 결국 있을 수 있습니다. Office 365 외부 사용자가 자신 수신된 거부 목록에서 [목록 삭제 포털 자가 서비스](https://technet.microsoft.com/library/mt661881%28v=exchg.150%29.aspx)를 사용 하 여 제거 시도할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4983b-p101">Not only can individual users be blocked by the service, but specific websites, domains, and IP addresses can also be blocked. In some cases, domains or websites can be added to a block list just because they appear in a spam message. As the Office 365 admin, you can try to get users, websites, domains, and IP addresses removed from third-party block lists. Use the links in the table at the bottom of this topic to contact each third party, and then follow the instructions. If someone outside Office 365 cannot send messages to your Office 365 account, their account may have ended up on the external blocked senders list. Users outside Office 365 can try to remove themselves from the blocked senders list by using the [self-service delisting portal](https://technet.microsoft.com/library/mt661881%28v=exchg.150%29.aspx).</span></span>
  
<span data-ttu-id="4983b-p102">Office 365 사용자 스팸으로 분류 되는 전자 메일을 보내지 못하도록 차단 되 면 anotification를 받을 수 있도록 아웃 바운드 스팸 설정을 구성할 수 있습니다. 사용자의 사서함에 문제가 해결 되 면 해당 보낸사람에 블록을 제거할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4983b-p102">You can configure outbound spam settings so that you get anotification when an Office 365 user is blocked from sending email that's classified as spam. After the problem with the user's mailbox is resolved, you can remove the block on that sender.</span></span>
  
## <a name="unblock-a-blocked-office-365-email-account"></a><span data-ttu-id="4983b-114">차단 된 Office 365 전자 메일 계정 차단 해제</span><span class="sxs-lookup"><span data-stu-id="4983b-114">Unblock a blocked Office 365 email account</span></span>

<span data-ttu-id="4983b-p103">Exchange 관리 센터 (EAC)에서이 작업을 완료 합니다. EAC에 대 한 자세한 내용은 [Exchange 관리 센터의 Exchange Online Protection](exchange-admin-center-in-exchange-online-protection-eop.md) 아웃 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="4983b-p103">You complete this task in the Exchange admin center (EAC). Check out [Exchange admin center in Exchange Online Protection](exchange-admin-center-in-exchange-online-protection-eop.md) for details about the EAC.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="4983b-117">Exchange Online에 대 한 EAC 하 고 있는 경우가 아니면 관리 센터를 볼 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="4983b-117">You won't see the action center unless you're in the EAC for Exchange Online.</span></span> 
  
1. <span data-ttu-id="4983b-118">EAC에서 **보호** 이동 \> **관리 센터**입니다.</span><span class="sxs-lookup"><span data-stu-id="4983b-118">In the EAC, navigate to **protection** \> **action center**.</span></span>
    
    ![Exchange 관리 센터의 관리 센터로 이동](media/9bbf0844-7b34-4a86-a2b7-8c7e9c8519a3.png)
  
2. <span data-ttu-id="4983b-120">**검색** 아이콘을 선택 하 고 차단 된 사용자의 SMTP 주소를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="4983b-120">Select the **Search** icon, and then enter the SMTP address of the blocked user.</span></span> 
    
    ![관리 센터에서 차단된 사용자 검색](media/f931b5a0-7115-4d95-9f6f-b403436031ba.png)
  
3. <span data-ttu-id="4983b-122">설명 창에서 **계정을 차단 해제** 를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="4983b-122">Click **Unblock Account** in the description pane.</span></span> 
    
    ![관리 센터에서 사용자 차단 해제](media/c5d5b1b9-8416-45aa-9631-881e94d1d056.png)
  
4. <span data-ttu-id="4983b-124">**예** 하 여 변경 내용을 확인을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="4983b-124">Click **Yes** to confirm the change.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="4983b-p104">테 넌 트 관리자 계정을 차단을 해제 수 있는 횟수에 제한이 사용자에 대 한 제한을 초과 되 면 오류 메시지가 나타납니다. 사용자의 차단을 해제 하는 지원 서비스에 문의 합니다.</span><span class="sxs-lookup"><span data-stu-id="4983b-p104">There's a limit to the number of times that an account can be unblocked by the tenant admin. If the limit for a user has been exceeded, an error message appears. Contact Support to unblock the user.</span></span> 
  
## <a name="third-party-block-lists"></a><span data-ttu-id="4983b-127">타사 차단 목록</span><span class="sxs-lookup"><span data-stu-id="4983b-127">Third-party block lists</span></span>

|<span data-ttu-id="4983b-128">**목록 이름**</span><span class="sxs-lookup"><span data-stu-id="4983b-128">**List Name**</span></span>|<span data-ttu-id="4983b-129">**목록 삭제 포털**</span><span class="sxs-lookup"><span data-stu-id="4983b-129">**Delisting Portal**</span></span>|<span data-ttu-id="4983b-130">**자세한 내용**</span><span class="sxs-lookup"><span data-stu-id="4983b-130">**For more information**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="4983b-131">URIBL</span><span class="sxs-lookup"><span data-stu-id="4983b-131">URIBL</span></span>  <br/> |[https://admin.uribl.com/?section=lookup](https://admin.uribl.com/?section=lookup) <br/> |[<span data-ttu-id="4983b-132">URIBL 웹사이트</span><span class="sxs-lookup"><span data-stu-id="4983b-132">URIBL website </span></span>](https://uribl.com/) <br/> |
|<span data-ttu-id="4983b-133">SURBL</span><span class="sxs-lookup"><span data-stu-id="4983b-133">SURBL</span></span>  <br/> |[http://www.surbl.org/surbl-analysis](http://www.surbl.org/surbl-analysis) <br/> |[<span data-ttu-id="4983b-134">SURBL URI 신뢰도 데이터 소개 (영문)</span><span class="sxs-lookup"><span data-stu-id="4983b-134">Introducing SURBL URI reputation data</span></span>](http://www.surbl.org/) <br/> |
|<span data-ttu-id="4983b-135">Spamhaus</span><span class="sxs-lookup"><span data-stu-id="4983b-135">Spamhaus</span></span>  <br/> |[https://www.spamhaus.org/lookup/](https://www.spamhaus.org/lookup/) <br/> |[<span data-ttu-id="4983b-136">이해 필터링 이해</span><span class="sxs-lookup"><span data-stu-id="4983b-136">Understanding DNSBL Filtering</span></span>](https://www.spamhaus.org/whitepapers/dnsbl_function/) <br/> |
|<span data-ttu-id="4983b-137">invaluement</span><span class="sxs-lookup"><span data-stu-id="4983b-137">invaluement</span></span>  <br/> |[http://dnsbl.invaluement.com/lookup/](http://dnsbl.invaluement.com/lookup/) <br/> |[<span data-ttu-id="4983b-138">invaluement 스팸 방지 목록</span><span class="sxs-lookup"><span data-stu-id="4983b-138">invaluement anti-spam list</span></span>](http://dnsbl.invaluement.com/) <br/> |
|<span data-ttu-id="4983b-139">Phishtank</span><span class="sxs-lookup"><span data-stu-id="4983b-139">Phishtank</span></span>  <br/> |[https://www.phishtank.com/](https://www.phishtank.com/) <br/> |[<span data-ttu-id="4983b-140">PhishTank FAQ</span><span class="sxs-lookup"><span data-stu-id="4983b-140">PhishTank FAQ</span></span>](https://www.phishtank.com/faq.php) <br/> |
   
> [!NOTE]
> <span data-ttu-id="4983b-141">Exchange Online Protection 제 3 자 차단 목록을 사용 하 여 스팸 필터링에 대 한 합니다.</span><span class="sxs-lookup"><span data-stu-id="4983b-141">Exchange Online Protection also uses third-party block lists for spam filtering.</span></span> 
   
## <a name="for-more-information"></a><span data-ttu-id="4983b-142">자세한 내용</span><span class="sxs-lookup"><span data-stu-id="4983b-142">For more information</span></span>

[<span data-ttu-id="4983b-143">아웃바운드 스팸 정책 구성</span><span class="sxs-lookup"><span data-stu-id="4983b-143">Configure the outbound spam policy</span></span>](configure-the-outbound-spam-policy.md)
  
[<span data-ttu-id="4983b-144">아웃 바운드 메시지 용 위험성이 높은 배달 풀</span><span class="sxs-lookup"><span data-stu-id="4983b-144">High-risk delivery pool for outbound messages</span></span>](high-risk-delivery-pool-for-outbound-messages.md)

[<span data-ttu-id="4983b-145">목록 해제 포털을 사용하여 Office 365 수신 거부 목록에서 본인 제거</span><span class="sxs-lookup"><span data-stu-id="4983b-145">Use the delist portal to remove yourself from the Office 365 blocked senders list</span></span>](use-the-delist-portal-to-remove-yourself-from-the-office-365-blocked-senders-lis.md)
  

  

