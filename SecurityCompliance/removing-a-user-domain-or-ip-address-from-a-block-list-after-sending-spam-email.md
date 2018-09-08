---
title: 스팸 전자 메일을 보낸 후 차단 목록에서 사용자, 도메인 또는 IP 주소를 제거
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 09/05/2018
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
ms.openlocfilehash: ff5bb010f45b0c89e08239f0e37885bd7ae5c7cd
ms.sourcegitcommit: 234a22c61859133ed5e7988a9551a569781518a4
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/07/2018
ms.locfileid: "23875790"
---
# <a name="removing-a-user-domain-or-ip-address-from-a-block-list-after-sending-spam-email"></a><span data-ttu-id="0ffa7-103">스팸 전자 메일을 보낸 후 차단 목록에서 사용자, 도메인 또는 IP 주소를 제거</span><span class="sxs-lookup"><span data-stu-id="0ffa7-103">Removing a user, domain, or IP address from a block list after sending spam email</span></span>

<span data-ttu-id="0ffa7-104">사용자는 계속 해 서 스팸으로 분류 하는 Office 365에서 전자 메일 메시지를 보내는, 모든 자세한 메시지를 보내지 못하도록 차단 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0ffa7-104">If a user continuously sends email messages from Office 365 that is classified as spam, they will be blocked from sending any more messages.</span></span> 
  
<span data-ttu-id="0ffa7-105">받은 배달 못함 보고서 (NDR 또는 전자 메일 메시지를 보내려면 실패) 보낸 전자 메일 메시지를 보내지 못하도록 차단 되 면 자신이 직접 차단을 해제 하기 위해 수행 해야하는 단계에 대 한 구체적인 정보를 제공 하는 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ffa7-105">When a sender is blocked from sending emails messages, they receive a Non-Delivery Report (NDR or email failed to send message) that provides specific information about the steps that they have to take to unblock themselves.</span></span>
  
<span data-ttu-id="0ffa7-p101">뿐 아니라 개별 사용자가 차단 될 수 있습니다,이 서비스는 하지만 특정 웹사이트, 도메인 및 IP 주소 차단 될 수 있습니다. 경우에 따라 도메인 이나 웹사이트 추가할 수 차단 목록에 스팸 메시지에 나타나는 해 서 합니다. Office 365 관리자, 사용자, 웹사이트, 도메인 및 타사 차단 목록에서 제거 하는 IP 주소를 가져올 시도할 수 있습니다. 이 항목의 맨 아래에 표에 링크를 사용 하 여 각 제 3 자에 게 문의 하 고 지침을 따릅니다. Office 365 계정에 메시지를 보낼 수 없는 Office 365 외부 사용자, 하는 경우 자신의 계정 외부 수신된 거부 목록에 결국 있을 수 있습니다. Office 365 외부 사용자가 자신 수신된 거부 목록에서 [목록 삭제 포털 자가 서비스](https://technet.microsoft.com/library/mt661881%28v=exchg.150%29.aspx)를 사용 하 여 제거 시도할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0ffa7-p101">Not only can individual users be blocked by the service, but specific websites, domains, and IP addresses can also be blocked. In some cases, domains or websites can be added to a block list just because they appear in a spam message. As the Office 365 admin, you can try to get users, websites, domains, and IP addresses removed from third-party block lists. Use the links in the table at the bottom of this topic to contact each third party, and then follow the instructions. If someone outside Office 365 cannot send messages to your Office 365 account, their account may have ended up on the external blocked senders list. Users outside Office 365 can try to remove themselves from the blocked senders list by using the [self-service delisting portal](https://technet.microsoft.com/library/mt661881%28v=exchg.150%29.aspx).</span></span>
  
<span data-ttu-id="0ffa7-p102">Office 365 사용자 스팸으로 분류 되는 전자 메일을 보내지 못하도록 차단 되 면 anotification를 받을 수 있도록 아웃 바운드 스팸 설정을 구성할 수 있습니다. 사용자의 사서함에 문제가 해결 되 면 해당 보낸사람에 블록을 제거할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0ffa7-p102">You can configure outbound spam settings so that you get anotification when an Office 365 user is blocked from sending email that's classified as spam. After the problem with the user's mailbox is resolved, you can remove the block on that sender.</span></span>
  
## <a name="unblock-a-blocked-office-365-email-account"></a><span data-ttu-id="0ffa7-114">차단 된 Office 365 전자 메일 계정 차단 해제</span><span class="sxs-lookup"><span data-stu-id="0ffa7-114">Unblock a blocked Office 365 email account</span></span>

<span data-ttu-id="0ffa7-p103">Office 365 보안 및 규정 준수 센터 (SCC)에서이 작업을 완료 합니다. 소스 코드 제어에 대 한 자세한 내용은 [Office 365 보안 및 규정 준수 센터로 이동](go-to-the-securitycompliance-center.md) 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ffa7-p103">You complete this task in the Office 365 Security & Compliance Center (SCC). [Go to the Office 365 Security & Compliance Center](go-to-the-securitycompliance-center.md) for more details about SCC.</span></span>

1. <span data-ttu-id="0ffa7-117">Office 365 전역 관리자 권한, Office 365 보안 및 규정 준수 센터에 로그인 한 왼쪽에 있는 목록의 **위협 관리**를 확장 하 고, **검토**, 선택 하 고 다음 **제한 된 사이트를 선택 된 작업이 나 교육용 계정을 사용 하 여 사용자가**합니다.</span><span class="sxs-lookup"><span data-stu-id="0ffa7-117">Using a work or school account that has Office 365 global administrator privileges, sign into the Office 365 Security and Compliance Center and in the list on the left, expand **Threat Management**, choose **Review**, and then choose **Restricted Users**.</span></span>
    
    > [!TIP]
    > <span data-ttu-id="0ffa7-118">**제한 된 사용자가** 페이지의 보안에서 직접 이동 &amp; 준수 센터가이 URL을 사용 하 여: >[https://protection.office.com/?hash=/restrictedusers](https://protection.office.com/?hash=/restrictedusers)</span><span class="sxs-lookup"><span data-stu-id="0ffa7-118">To go directly to the **Restricted Users** page in the Security &amp; Compliance Center, use this URL: > [https://protection.office.com/?hash=/restrictedusers](https://protection.office.com/?hash=/restrictedusers)</span></span>

2. <span data-ttu-id="0ffa7-p104">이 페이지에는 조직 외부에 있는 메일을 보내지 못하도록 차단 된 사용자 목록이 포함 됩니다.  **차단 해제**에 제한을 제거 하 고 다음을 클릭 하 고 싶지 사용자를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="0ffa7-p104">This page will contain the list of users that have been blocked from sending mail to outside of your organization.  Find the user you wish to remove restrictions on and then click on **Unblock**.</span></span>

3. <span data-ttu-id="0ffa7-121">**예** 하 여 변경 내용을 확인을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ffa7-121">Click **Yes** to confirm the change.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="0ffa7-p105">테 넌 트 관리자 계정을 차단을 해제 수 있는 횟수에 제한이 사용자에 대 한 제한을 초과 되 면 오류 메시지가 나타납니다. 다음은 사용자의 차단을 해제 하는 지원 서비스에 문의 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ffa7-p105">There's a limit to the number of times that an account can be unblocked by the tenant admin. If the limit for a user has been exceeded, an error message appears. You will then need to contact Support to unblock the user.</span></span> 
  
## <a name="third-party-block-lists"></a><span data-ttu-id="0ffa7-124">타사 차단 목록</span><span class="sxs-lookup"><span data-stu-id="0ffa7-124">Third-party block lists</span></span>

|<span data-ttu-id="0ffa7-125">**목록 이름**</span><span class="sxs-lookup"><span data-stu-id="0ffa7-125">**List Name**</span></span>|<span data-ttu-id="0ffa7-126">**목록 삭제 포털**</span><span class="sxs-lookup"><span data-stu-id="0ffa7-126">**Delisting Portal**</span></span>|<span data-ttu-id="0ffa7-127">**자세한 내용**</span><span class="sxs-lookup"><span data-stu-id="0ffa7-127">**For more information**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="0ffa7-128">URIBL</span><span class="sxs-lookup"><span data-stu-id="0ffa7-128">URIBL</span></span>  <br/> |[https://admin.uribl.com/?section=lookup](https://admin.uribl.com/?section=lookup) <br/> |[<span data-ttu-id="0ffa7-129">URIBL 웹사이트</span><span class="sxs-lookup"><span data-stu-id="0ffa7-129">URIBL website </span></span>](https://uribl.com/) <br/> |
|<span data-ttu-id="0ffa7-130">SURBL</span><span class="sxs-lookup"><span data-stu-id="0ffa7-130">SURBL</span></span>  <br/> |[http://www.surbl.org/surbl-analysis](http://www.surbl.org/surbl-analysis) <br/> |[<span data-ttu-id="0ffa7-131">SURBL URI 신뢰도 데이터 소개 (영문)</span><span class="sxs-lookup"><span data-stu-id="0ffa7-131">Introducing SURBL URI reputation data</span></span>](http://www.surbl.org/) <br/> |
|<span data-ttu-id="0ffa7-132">Spamhaus</span><span class="sxs-lookup"><span data-stu-id="0ffa7-132">Spamhaus</span></span>  <br/> |[https://www.spamhaus.org/lookup/](https://www.spamhaus.org/lookup/) <br/> |[<span data-ttu-id="0ffa7-133">이해 필터링 이해</span><span class="sxs-lookup"><span data-stu-id="0ffa7-133">Understanding DNSBL Filtering</span></span>](https://www.spamhaus.org/whitepapers/dnsbl_function/) <br/> |
|<span data-ttu-id="0ffa7-134">invaluement</span><span class="sxs-lookup"><span data-stu-id="0ffa7-134">invaluement</span></span>  <br/> |[http://dnsbl.invaluement.com/lookup/](http://dnsbl.invaluement.com/lookup/) <br/> |[<span data-ttu-id="0ffa7-135">invaluement 스팸 방지 목록</span><span class="sxs-lookup"><span data-stu-id="0ffa7-135">invaluement anti-spam list</span></span>](http://dnsbl.invaluement.com/) <br/> |
|<span data-ttu-id="0ffa7-136">Phishtank</span><span class="sxs-lookup"><span data-stu-id="0ffa7-136">Phishtank</span></span>  <br/> |[https://www.phishtank.com/](https://www.phishtank.com/) <br/> |[<span data-ttu-id="0ffa7-137">PhishTank FAQ</span><span class="sxs-lookup"><span data-stu-id="0ffa7-137">PhishTank FAQ</span></span>](https://www.phishtank.com/faq.php) <br/> |
   
> [!NOTE]
> <span data-ttu-id="0ffa7-138">Exchange Online Protection 제 3 자 차단 목록을 사용 하 여 스팸 필터링에 대 한 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ffa7-138">Exchange Online Protection also uses third-party block lists for spam filtering.</span></span> 
   
## <a name="for-more-information"></a><span data-ttu-id="0ffa7-139">자세한 내용</span><span class="sxs-lookup"><span data-stu-id="0ffa7-139">For more information</span></span>

[<span data-ttu-id="0ffa7-140">아웃바운드 스팸 정책 구성</span><span class="sxs-lookup"><span data-stu-id="0ffa7-140">Configure the outbound spam policy</span></span>](configure-the-outbound-spam-policy.md)
  
[<span data-ttu-id="0ffa7-141">아웃 바운드 메시지 용 위험성이 높은 배달 풀</span><span class="sxs-lookup"><span data-stu-id="0ffa7-141">High-risk delivery pool for outbound messages</span></span>](high-risk-delivery-pool-for-outbound-messages.md)

[<span data-ttu-id="0ffa7-142">목록 해제 포털을 사용하여 Office 365 수신 거부 목록에서 본인 제거</span><span class="sxs-lookup"><span data-stu-id="0ffa7-142">Use the delist portal to remove yourself from the Office 365 blocked senders list</span></span>](use-the-delist-portal-to-remove-yourself-from-the-office-365-blocked-senders-lis.md)
  

  

