---
title: Office 365 스푸핑 방지 하기 위해 보낸 사람이 정책 프레임 워크 (SPF)을 사용 하는 방법
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 12/15/2016
ms.audience: ITPro
ms.topic: reference
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 3aff33c5-1416-4867-a23b-e0c0c5b4d2be
description: '요약: Office 365 사용 하는 방법 보낸 사람이 정책 프레임 워크 (SPF) TXT 레코드 DNS에서 대상 전자 메일 시스템 사용자 지정 도메인에서 보낸 메시지를 신뢰 하도록이 문서에 설명 합니다. 이 Office 365에서 보낸 아웃 바운드 메일에 적용 됩니다. Office 365 내에서 받는 사람에 게 Office 365에서 보낸 메시지는 항상 SPF를 전달 합니다.'
ms.openlocfilehash: b42c2528f7a6a272e11d2434cce1e1735649962a
ms.sourcegitcommit: e9dca2d6a7838f98bb7eca127fdda2372cda402c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/21/2018
ms.locfileid: "23003287"
---
# <a name="how-office-365-uses-sender-policy-framework-spf-to-prevent-spoofing"></a><span data-ttu-id="ec663-105">Office 365 스푸핑 방지 하기 위해 보낸 사람이 정책 프레임 워크 (SPF)을 사용 하는 방법</span><span class="sxs-lookup"><span data-stu-id="ec663-105">How Office 365 uses Sender Policy Framework (SPF) to prevent spoofing</span></span>

 <span data-ttu-id="ec663-p102">**요약:** 이 문서에서는 Office 365 사용 하는 방법 보낸 사람이 정책 프레임 워크 (SPF) TXT 레코드 DNS에서 대상 전자 메일 시스템 사용자 지정 도메인에서 보낸 메시지를 신뢰 하도록에 대해 설명 합니다. 이 Office 365에서 보낸 아웃 바운드 메일에 적용 됩니다. Office 365 내에서 받는 사람에 게 Office 365에서 보낸 메시지는 항상 SPF를 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec663-p102">**Summary:** This article describes how Office 365 uses the Sender Policy Framework (SPF) TXT record in DNS to ensure that destination email systems trust messages sent from your custom domain. This applies to outbound mail sent from Office 365. Messages sent from Office 365 to a recipient within Office 365 will always pass SPF.</span></span> 
  
<span data-ttu-id="ec663-p103">SPF TXT 레코드를 전자 메일 메시지를 보낼 하는 도메인 이름을 확인 하 여 피싱 및 스푸핑 방지 하는 DNS 레코드를은 합니다. SPF을 보내는 도메인의 공식된 소유자에 대해 보낸 사람의 IP 주소를 확인 하 여 전자 메일 메시지의 출처의 유효성을 검사 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec663-p103">An SPF TXT record is a DNS record that helps prevent spoofing and phishing by verifying the domain name from which email messages are sent. SPF validates the origin of email messages by verifying the IP address of the sender against the alleged owner of the sending domain.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="ec663-p104">SPF 레코드 종류는 하 여 Internet Engineering Task Force (IETF) 지원이 중단 된 2014 년에 했습니다. 대신, DNS에서 TXT 레코드를 사용 하 여 SPF 정보를 게시할 수 있는지 확인 합니다. 이 문서의 나머지 부분 명확 하 게 하기에 대 한 용어 SPF TXT 레코드를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="ec663-p104">SPF record types were deprecated by the Internet Engineering Task Force (IETF) in 2014. Instead, ensure that you use TXT records in DNS to publish your SPF information. The rest of this article uses the term SPF TXT record for clarity.</span></span> 
  
<span data-ttu-id="ec663-p105">도메인 관리자는 DNS에서 TXT 레코드에 SPF 정보를 게시 합니다. SPF 정보 권한이 부여 된 아웃 바운드 전자 메일 서버를 식별합니다. 대상 전자 메일 시스템 메시지 권한이 부여 된 아웃 바운드 전자 메일 서버에서 시작 되었는지 확인 합니다. SPF에 이미 익숙한 또는 간단한 배포 하 고 Office 365에 대 한 사용자의 DNS에서 SPF TXT 레코드에 포함 된 내용을 싶습니까을 하는 경우에 [스푸핑을 방지 하기 위해 Office 365에서 SPF를 설정](set-up-spf-in-office-365-to-help-prevent-spoofing.md)하려면 이동할 수 있습니다. Office 365에 완전히 호스트 되는 배포 하지 않은 경우 SPF 작동 하는 방법 또는 Office 365에 대 한 SPF 문제를 해결, 읽기 유지 하는 방법에 대 한 자세한 정보를 원하는.</span><span class="sxs-lookup"><span data-stu-id="ec663-p105">Domain administrators publish SPF information in TXT records in DNS. The SPF information identifies authorized outbound email servers. Destination email systems verify that messages originate from authorized outbound email servers. If you are already familiar with SPF, or you have a simple deployment, and just need to know what to include in your SPF TXT record in DNS for Office 365, you can go to [Set up SPF in Office 365 to help prevent spoofing](set-up-spf-in-office-365-to-help-prevent-spoofing.md). If you do not have a deployment that is fully-hosted in Office 365, or you want more information about how SPF works or how to troubleshoot SPF for Office 365, keep reading.</span></span>
  
> [!NOTE]
> <span data-ttu-id="ec663-p106">이전에 사용 하는 경우 SharePoint Online 사용자 지정 도메인에 다른 SPF TXT 레코드를 추가 했습니다. 이 더이상 필요 합니다. 이 변경의 정크 메일 폴더에서 종료 하는 SharePoint Online 알림 메시지의 위험을 줄이려면 해야 합니다. 변경 내용을 즉시, 하지만 "너무 많은 경우 조회" 오류 메시지가 표시 되는 경우 [SPF 스푸핑을 방지 하기 위해 Office 365에서 설정](set-up-spf-in-office-365-to-help-prevent-spoofing.md)의 설명에 따라 SPF TXT 레코드를 수정할 필요가 없습니다.</span><span class="sxs-lookup"><span data-stu-id="ec663-p106">Previously, you had to add a different SPF TXT record to your custom domain if you also used SharePoint Online. This is no longer required. This change should reduce the risk of SharePoint Online notification messages ending up in the Junk Email folder. You do not need to make any changes immediately, but if you receive the "too many lookups" error, modify your SPF TXT record as described in [Set up SPF in Office 365 to help prevent spoofing](set-up-spf-in-office-365-to-help-prevent-spoofing.md).</span></span> 
     
## <a name="how-spf-works-to-prevent-spoofing-and-phishing-in-office-365"></a><span data-ttu-id="ec663-123">SPF 위조 및 Office 365의 피싱 방지 하기 위해 작동 하는 방법</span><span class="sxs-lookup"><span data-stu-id="ec663-123">How SPF works to prevent spoofing and phishing in Office 365</span></span>
<span data-ttu-id="ec663-124"><a name="HowSPFWorks"> </a></span><span class="sxs-lookup"><span data-stu-id="ec663-124"></span></span>

<span data-ttu-id="ec663-p107">SPF는 보낸사람에서 도메인을 대신 하 여 보낼 수 있는지 여부를 결정 합니다. 경우 그렇게 보낸은 사용할 수 없습니다 즉, 전자 메일 받는 서버에서 SPF 검사에 실패 하는 경우 해당 서버에 구성 된 스팸 정책 결정 메시지와 함께 수행할 작업을 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec663-p107">SPF determines whether or not a sender is permitted to send on behalf of a domain. If the sender is not permitted to do so, that is, if the email fails the SPF check on the receiving server, the spam policy configured on that server determines what to do with the message.</span></span>
  
<span data-ttu-id="ec663-p108">각 SPF TXT 레코드는 세 부분으로 구성: SPF TXT 인지 선언 기록, 도메인 및 도메인 대신 및 적용 규칙에 보낼 수 있는 외부 도메인에서 메일을 보낼 수 있는 IP 주소입니다. 유효한 SPF TXT 레코드에 세 모두 필요합니다. 이 문서는 SPF TXT 레코드를 형성 하는 방법에 대해 설명 하 고 Office 365에서 서비스 사용 (영문)에 대 한 유용한 정보를 제공 합니다. Dns 레코드를 게시 하려면 도메인 등록 (영문)의 지침에 대 한 링크가 제공 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ec663-p108">Each SPF TXT record contains three parts: the declaration that it is an SPF TXT record, the IP addresses that are allowed to send mail from your domain and the external domains that can send on your domain's behalf, and an enforcement rule. You need all three in a valid SPF TXT record. This article describes how you form your SPF TXT record and provides best practices for working with the services in Office 365. Links to instructions on working with your domain registrar to publish your record to DNS are also provided.</span></span>
  
### <a name="spf-basics-ip-addresses-allowed-to-send-from-your-custom-domain"></a><span data-ttu-id="ec663-131">SPF 기본 사항: 사용자 지정 도메인에서 보낼 수 있는 IP 주소</span><span class="sxs-lookup"><span data-stu-id="ec663-131">SPF basics: IP addresses allowed to send from your custom domain</span></span>
<span data-ttu-id="ec663-132"><a name="SPFBasicsIPaddresses"> </a></span><span class="sxs-lookup"><span data-stu-id="ec663-132"></span></span>

<span data-ttu-id="ec663-133">SPF 규칙에 대 한 기본 구문에 대 한 정보를 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec663-133">Take a look at the basic syntax for an SPF rule:</span></span>
  
<span data-ttu-id="ec663-134">v = spf1 \<IP\> \<적용 규칙\></span><span class="sxs-lookup"><span data-stu-id="ec663-134">v=spf1 \<IP\> \<enforcement rule\></span></span>
  
<span data-ttu-id="ec663-135">예: contoso.com에 대 한 다음 해당 SPF 규칙이 존재 가정해 보겠습니다.</span><span class="sxs-lookup"><span data-stu-id="ec663-135">For example, let's say the following SPF rule exists for contoso.com:</span></span>
  
<span data-ttu-id="ec663-136">v = spf1 \<IP 주소 #1\> \<#2 IP 주소\> \<IP 주소 #3\> \<적용 규칙\></span><span class="sxs-lookup"><span data-stu-id="ec663-136">v=spf1 \<IP address #1\> \<IP address #2\> \<IP address #3\> \<enforcement rule\></span></span>
  
<span data-ttu-id="ec663-137">이 예제에서는 SPF 규칙만 contoso.com 도메인에 대 한 이러한 IP 주소에서 메일을 수락 하도록 받는 전자 메일 서버를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec663-137">In this example, the SPF rule instructs the receiving email server to only accept mail from these IP addresses for the domain contoso.com:</span></span>
  
- <span data-ttu-id="ec663-138">IP 주소 #1</span><span class="sxs-lookup"><span data-stu-id="ec663-138">IP address #1</span></span>
    
- <span data-ttu-id="ec663-139">IP 주소 #2</span><span class="sxs-lookup"><span data-stu-id="ec663-139">IP address #2</span></span>
    
- <span data-ttu-id="ec663-140">IP 주소 #3</span><span class="sxs-lookup"><span data-stu-id="ec663-140">IP address #3</span></span>
    
<span data-ttu-id="ec663-p109">이 SPF 규칙 해당 메시지에는 contoso.com에서 하지만 이러한 세 IP 주소 중 하나에서 하지 상태가 되 면 하는 경우 받는 서버에 적용 되도록 강제 적용 규칙 메시지의 받는 전자 메일 서버에 지시 합니다. 적용 규칙은 일반적으로 이러한 옵션 중 하나입니다.</span><span class="sxs-lookup"><span data-stu-id="ec663-p109">This SPF rule tells the receiving email server that if a message comes from contoso.com, but not from one of these three IP addresses, the receiving server should apply the enforcement rule to the message. The enforcement rule is usually one of these options:</span></span>
  
- <span data-ttu-id="ec663-p110">**영구 실패.** 메시지 봉투의 '영구 실패'를 사용 하 여 메시지를 표시 하 고이 유형의 메시지에 대 한 수신 서버 구성 된 스팸 정책을 따르는 것이 다음 키를 누릅니다.</span><span class="sxs-lookup"><span data-stu-id="ec663-p110">**Hard fail.** Mark the message with 'hard fail' in the message envelope and then follow the receiving server's configured spam policy for this type of message.</span></span> 
    
- <span data-ttu-id="ec663-p111">**부드러운 실패.** 메시지 봉투의 '소프트 실패'를 사용 하 여 메시지를 표시 합니다. 일반적으로 전자 메일 서버는 이러한 메시지를 계속 제공 하도록 구성 됩니다. 대부분의 최종 사용자는이 기호를 표시 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ec663-p111">**Soft fail.** Mark the message with 'soft fail' in the message envelope. Typically, email servers are configured to deliver these messages anyway. Most end users do not see this mark.</span></span> 
    
- <span data-ttu-id="ec663-p112">**중립.** 이 무 것, 즉, 메시지 봉투를 표시 하지는 마십시오. 이 일반적으로 테스트 목적으로 예약 하 고 거의 사용 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ec663-p112">**Neutral.** Do nothing, that is, do not mark the message envelope. This is usually reserved for testing purposes and is rarely used.</span></span> 
    
<span data-ttu-id="ec663-p113">다음 예제는 SPF 다양 한 상황에서 작동 하는 방법을 보여줍니다. 이 예제에서는 contoso.com 보낸 이며 woodgrovebank.com 수화기 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec663-p113">The following examples show how SPF works in different situations. In these examples, contoso.com is the sender and woodgrovebank.com is the receiver.</span></span>
  
### <a name="example-1-email-authentication-of-a-message-sent-directly-from-sender-to-receiver"></a><span data-ttu-id="ec663-154">수신자에 게 보낸에서 직접 보내는 메시지의 예 1: 전자 메일 인증</span><span class="sxs-lookup"><span data-stu-id="ec663-154">Example 1: Email authentication of a message sent directly from sender to receiver</span></span>
<span data-ttu-id="ec663-155"><a name="spfExample1"> </a></span><span class="sxs-lookup"><span data-stu-id="ec663-155"></span></span>

<span data-ttu-id="ec663-156">SPF는 수신자에 게 보낸에서 경로 같은 직접 하는 경우에 가장 적합 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec663-156">SPF works best when the path from sender to receiver is direct, for example:</span></span>
  
![서버 간에 직접 전자 메일이 전송될 때 SPF에서 전자 메일을 인증하는 방법을 보여주는 다이어그램입니다.](media/835c20a7-ed4c-49c4-91fe-b8ebb3e452a1.jpg)
  
<span data-ttu-id="ec663-158">Woodgrovebank.com IP 주소 #1 contoso.com에 대 한 SPF TXT 레코드에 있으면 메시지를 받을 경우 메시지는 SPF 검사를 통과 하 고 인증 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ec663-158">When woodgrovebank.com receives the message, if IP address #1 is in the SPF TXT record for contoso.com, the message passes the SPF check and is authenticated.</span></span>
  
### <a name="example-2-spoofed-sender-address-fails-the-spf-check"></a><span data-ttu-id="ec663-159">예 2: 위장 된 보낸사람 주소 SPF 검사에 실패</span><span class="sxs-lookup"><span data-stu-id="ec663-159">Example 2: Spoofed sender address fails the SPF check</span></span>
<span data-ttu-id="ec663-160"><a name="spfExample2"> </a></span><span class="sxs-lookup"><span data-stu-id="ec663-160"></span></span>

<span data-ttu-id="ec663-161">phisher contoso.com 스푸핑할 하는 방법을 찾는 경우를 가정해 보겠습니다.</span><span class="sxs-lookup"><span data-stu-id="ec663-161">Suppose a phisher finds a way to spoof contoso.com:</span></span>
  
![스푸핑된 서버에서 보낸 전자 메일을 SPF에서 인증하는 방법을 보여주는 다이어그램입니다.](media/235dac3d-cdc5-466e-86e0-37b5979de198.jpg)
  
<span data-ttu-id="ec663-163">IP 주소 #12 contoso.com의 SPF TXT 레코드에 없기 때문에 메시지 SPF 확인 실패 하 고 수신자 스팸으로 표시 하도록 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ec663-163">Since IP address #12 is not in contoso.com's SPF TXT record, the message fails the SPF check and the receiver may choose to mark it as spam.</span></span>
  
### <a name="example-3-spf-and-forwarded-messages"></a><span data-ttu-id="ec663-164">예 3: SPF 및 전달된 하는 메시지</span><span class="sxs-lookup"><span data-stu-id="ec663-164">Example 3: SPF and forwarded messages</span></span>
<span data-ttu-id="ec663-165"><a name="spfExample3"> </a></span><span class="sxs-lookup"><span data-stu-id="ec663-165"></span></span>

<span data-ttu-id="ec663-p114">하나의 SPF의 단점은 전자 메일 전달 된 경우 작동 하지 않는 것입니다. 예, woodgrovebank.com에서 사용자가 모든 전자 메일을 보낼 outlook.com 계정에 착신 전환 규칙 설정 있다고 가정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec663-p114">One drawback of SPF is that it doesn't work when an email has been forwarded. For example, suppose the user at woodgrovebank.com has set up a forwarding rule to send all email to an outlook.com account:</span></span>
  
![메시지가 전달될 때 SPF에서 전자 메일을 인증할 수 없는 상황을 보여주는 다이어그램입니다.](media/6e92acd6-463e-4a1b-8327-fb1cf861f356.jpg)
  
<span data-ttu-id="ec663-p115">메시지 woodgrovebank.com에서 원래 SPF 검사를 전달 하지만 outlook.com에서 SPF 확인 IP #25 contoso.com의 SPF TXT 레코드에 없기 때문에 실패 하면 합니다. Outlook.com 스팸으로 메시지를 표시할 수 있습니다. 이 문제를 해결 하려면 함께에서 SPF를 사용 하 여 DKIM 및 DMARC와 같은 다른 전자 메일 인증 방법을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec663-p115">The message originally passes the SPF check at woodgrovebank.com but it fails the SPF check at outlook.com because IP #25 is not in contoso.com's SPF TXT record. Outlook.com might then mark the message as spam. To work around this problem, use SPF in conjunction with other email authentication methods such as DKIM and DMARC.</span></span>
  
### <a name="spf-basics-including-third-party-domains-that-can-send-mail-on-behalf-of-your-domain"></a><span data-ttu-id="ec663-172">SPF 기본 사항: 도메인을 대신 하 여 메일을 보낼 수 있는 타사 도메인을 포함 하 여</span><span class="sxs-lookup"><span data-stu-id="ec663-172">SPF basics: Including third-party domains that can send mail on behalf of your domain</span></span>
<span data-ttu-id="ec663-173"><a name="SPFBasicsIncludes"> </a></span><span class="sxs-lookup"><span data-stu-id="ec663-173"></span></span>

<span data-ttu-id="ec663-p116">IP 주소 외에도 보낸사람 등의 도메인을 포함 하 여 SPF TXT 레코드를 구성할 수 있습니다. 이러한 "포함" 문으로 SPF TXT 레코드에 추가 됩니다. 예: contoso.com contoso.net 및 contoso.org도 소유 하는 메일 서버의 IP 주소를 모두 포함 하고자 하는 수 있습니다. Contoso.com이 작업을 수행 하는 SPF TXT 레코드는 다음과 같은 게시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec663-p116">In addition to IP addresses, you can also configure your SPF TXT record to include domains as senders. These are added to the SPF TXT record as "include" statements. For example, contoso.com might want to include all of the IP addresses of the mail servers from contoso.net and contoso.org which it also owns. To do this, contoso.com publishes an SPF TXT record that looks like this:</span></span>
  
```
IN TXT "v=spf1 include:contoso.net include:contoso.org -all"
```

<span data-ttu-id="ec663-p117">받는 서버는 DNS에이 레코드를 표시, contoso.net 및 다음 contoso.org SPF TXT 레코드에도 DNS 조회를 수행 합니다. 추가로 발견 되 면 contoso.net 또는 contoso.org에 대 한 레코드 내에 문을 포함, 이러한 너무 대로 됩니다. 서비스 거부 공격을 방지 하기 위해 단일 전자 메일 메시지에 대 한 DNS 조회의 최대 수는 10을 사용 합니다. 각 포함 문을 나타냅니다 DNS 조회를 추가 합니다. 10 제한을 초과 하는 메시지, 메시지 SPF 오류가 발생 합니다. 보낸 메시지는 "너무 많은 경우 조회" 또는 생성 되었다는 메시지가 나타날 수 메시지를 받는 서버를 구성 하는 방식에 따라이 제한에 도달 하면는 "메시지에 대 한 최대 홉 수 초과 했습니다."입니다. 이 문제를 방지 하는 방법에 대 한 팁을 참조 하십시오. [문제해결: Office 365에서 SPF에 대 한 모범 사례](how-office-365-uses-spf-to-prevent-spoofing.md#SPFTroubleshoot)합니다.</span><span class="sxs-lookup"><span data-stu-id="ec663-p117">When the receiving server sees this record in DNS, it also performs a DNS lookup on the SPF TXT record for contoso.net and then for contoso.org. If it finds an additional include statement within the records for contoso.net or contoso.org, it will follow those too. In order to help prevent denial of service attacks, the maximum number of DNS lookups for a single email message is 10. Each include statement represents an additional DNS lookup. If a message exceeds the 10 limit, the message fails SPF. Once a message reaches this limit, depending on the way the receiving server is configured, the sender may receive a message that states that the message generated "too many lookups" or that the "maximum hop count for the message has been exceeded". For tips on how to avoid this, see [Troubleshooting: Best practices for SPF in Office 365](how-office-365-uses-spf-to-prevent-spoofing.md#SPFTroubleshoot).</span></span>
  
## <a name="requirements-for-your-spf-txt-record-and-office-365"></a><span data-ttu-id="ec663-184">SPF TXT 레코드 및 Office 365에 대 한 요구 사항</span><span class="sxs-lookup"><span data-stu-id="ec663-184">Requirements for your SPF TXT record and Office 365</span></span>
<span data-ttu-id="ec663-185"><a name="SPFReqsinO365"> </a></span><span class="sxs-lookup"><span data-stu-id="ec663-185"></span></span>

<span data-ttu-id="ec663-p118">Office 365를 설정 하는 경우 메일을 설정 하면 사용자의 도메인에 대 한 메일의 합법적인 소스로 Microsoft 메시징 서버를 식별 하는 SPF TXT 레코드를 이미 만든 합니다. 이 레코드 아마도 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="ec663-p118">If you set up mail when you set up Office 365, you already created an SPF TXT record that identifies the Microsoft messaging servers as a legitimate source of mail for your domain. This record probably looks like this:</span></span>
  
```
v=spf1 include:spf.protection.outlook.com -all
```

<span data-ttu-id="ec663-188">즉, 완벽 하 게 호스팅 Office 365 고객 인 경우 아웃 바운드 메일을 보내도록 온-프레미스 메일 서버 없음 해야, Office 365에 대 한 게시 하는 유일한 SPF TXT 레코드입니다.</span><span class="sxs-lookup"><span data-stu-id="ec663-188">If you're a fully-hosted Office 365 customer, that is, you have no on-premises mail servers that send outbound mail, this is the only SPF TXT record that you need to publish for Office 365.</span></span>
  
<span data-ttu-id="ec663-189">하이브리드 배포 하는 경우 (즉, 일부 사서함 온-프레미스 및 Office 365에서 호스팅된 일부)에 있는 Exchange Online Protection (EOP) 독립 실행형 고객 인 경우 또는 (즉, 조직을 사용 하 여 EOP가 온-프레미스 사서함을 보호 하기 위해)를 수행 해야 합니다 DNS에서 TXT SPF 레코드를 각에 지 온-프레미스 메일 서버에 대 한 아웃 바운드 IP 주소를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec663-189">If you have a hybrid deployment (that is, you have some mailboxes on-premises and some hosted in Office 365), or if you're an Exchange Online Protection (EOP) standalone customer (that is, your organization uses EOP to protect your on-premises mailboxes), you should add the outbound IP address for each of your on-premises edge mail servers to the SPF TXT record in DNS.</span></span>
  
## <a name="form-your-spf-txt-record-for-office-365"></a><span data-ttu-id="ec663-190">Office 365에 대 한 SPF TXT 레코드를 양식</span><span class="sxs-lookup"><span data-stu-id="ec663-190">Form your SPF TXT record for Office 365</span></span>
<span data-ttu-id="ec663-191"><a name="FormYourSPF"> </a></span><span class="sxs-lookup"><span data-stu-id="ec663-191"></span></span>

<span data-ttu-id="ec663-p119">이 문서의 구문 정보를 사용 하 여 사용자 지정 도메인에 대 한 SPF TXT 레코드를 형성 합니다. 다른 이지만 가장 일반적으로 여기에 언급 되지 않은 구문 옵션 옵션을 사용 합니다. 사용자의 레코드를 세운 후에 도메인 등록자에서 레코드를 업데이트 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec663-p119">Use the syntax information in this article to form the SPF TXT record for your custom domain. Although there are other syntax options that are not mentioned here, these are the most commonly used options. Once you have formed your record, you need to update the record at your domain registrar.</span></span>
  
<span data-ttu-id="ec663-p120">Office 365에 대 한 포함 해야하는 도메인에 대 한 정보를 [SPF에 필요한 외부 DNS 레코드를](https://support.office.com/article/External-Domain-Name-System-records-for-Office-365-c0531a6f-9e25-4f2d-ad0e-a70bfef09ac0?ui=en-US&amp;rs=en-US&amp;ad=US)참조 하십시오. 도메인 등록자에 대 한 SPF (TXT) 레코드를 업데이트 하기 위한 [단계별 지침](https://office.microsoft.com/en-us/office365-suite-help/create-dns-records-for-office-365-HA102851099.aspx?CTT=5&amp;origin=HA102818404) 을 사용 합니다. 등록 기관과 목록에 없는 경우에 사용자의 레코드를 업데이트 하는 방법을 설명 하는 개별적으로 연락할 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec663-p120">For information about the domains you will need to include for Office 365, see [External DNS records required for SPF](https://support.office.com/article/External-Domain-Name-System-records-for-Office-365-c0531a6f-9e25-4f2d-ad0e-a70bfef09ac0?ui=en-US&amp;rs=en-US&amp;ad=US). Use the [step-by-step instructions](https://office.microsoft.com/en-us/office365-suite-help/create-dns-records-for-office-365-HA102851099.aspx?CTT=5&amp;origin=HA102818404) for updating SPF (TXT) records for your domain registrar. If your registrar is not listed, you will need to contact them separately to learn how to update your record.</span></span> 
  
### <a name="spf-txt-record-syntax-for-office-365"></a><span data-ttu-id="ec663-198">Office 365에 대 한 SPF TXT 레코드 구문</span><span class="sxs-lookup"><span data-stu-id="ec663-198">SPF TXT record syntax for Office 365</span></span>
<span data-ttu-id="ec663-199"><a name="SPFSyntaxO365"> </a></span><span class="sxs-lookup"><span data-stu-id="ec663-199"></span></span>

<span data-ttu-id="ec663-200">Office 365에 대 한 일반적인 SPF TXT 레코드는 다음 구문을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec663-200">A typical SPF TXT record for Office 365 has the following syntax:</span></span>
  
```
v=spf1 [<ip4>|<ip6>:<IP address>] [include:<domain name>] <enforcement rule>
```

<span data-ttu-id="ec663-201">예를 들면 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="ec663-201">For example:</span></span>
  
```
v=spf1 ip4:192.168.0.1 ip4:192.168.0.2 include:spf.protection.outlook.com -all
```

<span data-ttu-id="ec663-202">여기서 각 부분이 나타내는 의미는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="ec663-202">where:</span></span>
  
- <span data-ttu-id="ec663-p121">**v = spf1** 가 필요 합니다. SPF TXT 레코드를으로 TXT 레코드를 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="ec663-p121">**v=spf1** is required. This defines the TXT record as an SPF TXT record.</span></span> 
    
- <span data-ttu-id="ec663-p122">**ip4** IP 버전 4 주소를 사용 하 고 있음을 나타냅니다. **i p 6** IP 버전 6 주소를 사용 하 고 있음을 나타냅니다. I p v 6 IP 주소를 사용 하는 경우이 문서의 예제에 **i p 6** **ip4를** 대체 합니다. CIDR 표기법을 **ip4:192.168.0.1/26**예를 사용 하 여 IP 주소 범위를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ec663-p122">**ip4** indicates that you are using IP version 4 addresses. **ip6** indicates that you are using IP version 6 addresses. If you are using IPv6 IP addresses, replace **ip4** with **ip6** in the examples in this article. You can also specify IP address ranges using CIDR notation, for example **ip4:192.168.0.1/26**.</span></span>
    
-  <span data-ttu-id="ec663-p123">_IP 주소_ 는 SPF TXT 레코드를 추가 하려면 IP 주소입니다. 일반적으로 조직에 대 한 아웃 바운드 메일 서버의 IP 주소입니다. 여러 아웃 바운드 메일 서버를 나열할 수 있습니다. 자세한 내용은 참조 [예제: 여러 아웃 바운드 온-프레미스 메일 서버 및 Office 365에 대 한 SPF TXT 기록](how-office-365-uses-spf-to-prevent-spoofing.md#ExampleSPFMultipleMailServerO365)합니다.</span><span class="sxs-lookup"><span data-stu-id="ec663-p123">_IP address_ is the IP address that you want to add to the SPF TXT record. Usually, this is the IP address of the outbound mail server for your organization. You can list multiple outbound mail servers. For more information, see [Example: SPF TXT record for multiple outbound on-premises mail servers and Office 365](how-office-365-uses-spf-to-prevent-spoofing.md#ExampleSPFMultipleMailServerO365).</span></span>
    
-  <span data-ttu-id="ec663-p124">_도메인_ 이름은 합법적인 보낸사람으로 추가 하려는 도메인입니다. Office 365에 대 한 포함 되어야 하는 도메인 이름 목록에 대 한 [SPF에 필요한 외부 DNS 레코드를](https://support.office.com/article/External-Domain-Name-System-records-for-Office-365-c0531a6f-9e25-4f2d-ad0e-a70bfef09ac0?ui=en-US&amp;rs=en-US&amp;ad=US)참조 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec663-p124">_domain name_ is the domain you want to add as a legitimate sender. For a list of domain names you should include for Office 365, see [External DNS records required for SPF](https://support.office.com/article/External-Domain-Name-System-records-for-Office-365-c0531a6f-9e25-4f2d-ad0e-a70bfef09ac0?ui=en-US&amp;rs=en-US&amp;ad=US).</span></span>
    
- <span data-ttu-id="ec663-215">적용 규칙은 일반적으로 다음 중 하나입니다.</span><span class="sxs-lookup"><span data-stu-id="ec663-215">Enforcement rule is usually one of the following:</span></span>
    
  - <span data-ttu-id="ec663-216"><0.0.0.0> 또는 <mail.contoso.com> 값은 도메인에 대한 전자 메일을 보내는 다른 메일 시스템이어야 합니다.
</span><span class="sxs-lookup"><span data-stu-id="ec663-216">-all</span></span>
    
    <span data-ttu-id="ec663-p125">영구 실패를 나타냅니다. SPF TXT 레코드에 나열 하 고 사용 하 여 도메인에 대 한 모든 권한이 부여 된 IP 주소를 알고 있으면-모든 (영구 실패) 한정자입니다. 또한만 사용할 경우 SPF, 즉, DMARC 또는 DKIM를 사용 하지 않는을 사용 해야-모든 한정자입니다. 사용 하는 항상이 한정자는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="ec663-p125">Indicates hard fail. If you know all of the authorized IP addresses for your domain, list them in the SPF TXT record and use the -all (hard fail) qualifier. Also, if you are only using SPF, that is, you are not using DMARC or DKIM, you should use the -all qualifier. We recommend that you use always this qualifier.</span></span>
    
  - <span data-ttu-id="ec663-221">~ 모든</span><span class="sxs-lookup"><span data-stu-id="ec663-221">~all</span></span>
    
    <span data-ttu-id="ec663-p126">부드러운 실패를 나타냅니다. 확실 하지 않은 IP 주소의 전체 목록은 합니다를 사용 해야 하는 경우는 ~ 모든 (소프트 실패) 한정자입니다. P로 DMARC를 사용 하는 경우 격리 또는 p = 하는 또한 사용할 수 있는 다음 reject = ~ 모든 합니다. 그렇지 않은 경우-을 모두 사용.</span><span class="sxs-lookup"><span data-stu-id="ec663-p126">Indicates soft fail. If you're not sure that you have the complete list of IP addresses, then you should use the ~all (soft fail) qualifier. Also, if you are using DMARC with p=quarantine or p=reject, then you can use ~all. Otherwise, use -all.</span></span>
    
  - <span data-ttu-id="ec663-226">? 모든</span><span class="sxs-lookup"><span data-stu-id="ec663-226">?all</span></span>
    
    <span data-ttu-id="ec663-p127">중립을 나타냅니다. 이 SPF를 테스트할 때 사용 됩니다. 이 한정자를 사용 하 여 라이브 배포에서 하는 것은 좋지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ec663-p127">Indicates neutral. This is used when testing SPF. We do not recommend that you use this qualifier in your live deployment.</span></span>
    
### <a name="example-spf-txt-record-to-use-when-all-of-your-mail-is-sent-by-office-365"></a><span data-ttu-id="ec663-230">예: SPF TXT 레코드 될 때 사용 하 여 Office 365에서 보내는 모든 메일</span><span class="sxs-lookup"><span data-stu-id="ec663-230">Example: SPF TXT record to use when all of your mail is sent by Office 365</span></span>
<span data-ttu-id="ec663-231"><a name="ExampleSPFNoSP"> </a></span><span class="sxs-lookup"><span data-stu-id="ec663-231"></span></span>

<span data-ttu-id="ec663-232">Office 365에서 전송 되는 모든 사용자의 메일 하는 경우에이 사용 하 여 SPF TXT 레코드에서:</span><span class="sxs-lookup"><span data-stu-id="ec663-232">If all of your mail is sent by Office 365, use this in your SPF TXT record:</span></span>
  
```
v=spf1 include:spf.protection.outlook.com -all
```

### <a name="example-spf-txt-record-for-a-hybrid-scenario-with-one-on-premises-exchange-server-and-office-365"></a><span data-ttu-id="ec663-233">예: SPF TXT 레코드 하나를 사용 하 여 하이브리드 시나리오에 대 한 온-프레미스 Exchange 서버와 Office 365</span><span class="sxs-lookup"><span data-stu-id="ec663-233">Example: SPF TXT record for a hybrid scenario with one on-premises Exchange Server and Office 365</span></span>
<span data-ttu-id="ec663-234"><a name="ExampleSPFHybridOneExchangeServer"> </a></span><span class="sxs-lookup"><span data-stu-id="ec663-234"></span></span>

<span data-ttu-id="ec663-235">하이브리드 환경에서 온-프레미스 Exchange 서버의 IP 주소 192.168.0.1 이면 하드 실패 함 SPF 적용 규칙을 설정 하기 위해 양식 SPF TXT 레코드 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="ec663-235">In a hybrid environment, if the IP address of your on-premises Exchange Server is 192.168.0.1, in order to set the SPF enforcement rule to hard fail, form the SPF TXT record as follows:</span></span>
  
```
v=spf1 ip4:192.168.0.1 include:spf.protection.outlook.com -all
```

### <a name="example-spf-txt-record-for-multiple-outbound-on-premises-mail-servers-and-office-365"></a><span data-ttu-id="ec663-236">예: 여러 아웃 바운드 온-프레미스에 대 한 SPF TXT 레코드 메일 서버 및 Office 365</span><span class="sxs-lookup"><span data-stu-id="ec663-236">Example: SPF TXT record for multiple outbound on-premises mail servers and Office 365</span></span>
<span data-ttu-id="ec663-237"><a name="ExampleSPFMultipleMailServerO365"> </a></span><span class="sxs-lookup"><span data-stu-id="ec663-237"></span></span>

<span data-ttu-id="ec663-p128">여러 아웃 바운드 메일 서버를 사용 하는 경우 SPF TXT 레코드에 각 메일 서버에 대 한 IP 주소를 포함 하 고 각 IP 주소 앞에 오는 공백을 구분 하는 "ip4:" 문입니다. 예를 들어:</span><span class="sxs-lookup"><span data-stu-id="ec663-p128">If you have multiple outbound mail servers, include the IP address for each mail server in the SPF TXT record and separate each IP address with a space followed by an "ip4:" statement. For example:</span></span>
  
```
v=spf1 ip4:192.168.0.1 ip4:192.168.0.2 ip4:192.168.0.3 include:spf.protection.outlook.com -all
```

## <a name="next-steps-set-up-spf-for-office-365"></a><span data-ttu-id="ec663-240">다음 단계: Office 365에 대 한 SPF 설정</span><span class="sxs-lookup"><span data-stu-id="ec663-240">Next steps: Set up SPF for Office 365</span></span>
<span data-ttu-id="ec663-241"><a name="SPFNextSteps"> </a></span><span class="sxs-lookup"><span data-stu-id="ec663-241"></span></span>

<span data-ttu-id="ec663-242">SPF TXT 레코드를 작성 한 한번, 도메인을 추가 하려면 [스푸핑을 방지 하기 위해 Office 365에서 SPF 설정](set-up-spf-in-office-365-to-help-prevent-spoofing.md) 의 단계를 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec663-242">Once you have formulated your SPF TXT record, follow the steps in [Set up SPF in Office 365 to help prevent spoofing](set-up-spf-in-office-365-to-help-prevent-spoofing.md) to add it to your domain.</span></span> 
  
<span data-ttu-id="ec663-p129">SPF 위조를 방지 설계 되었지만 스푸핑 하는 방법은 있지만 해당 SPF 보호 수는 없습니다. SPF를 설정 하 고 나면 이러한 경우에 대해 보호 하기 위해도 구성 해야 DKIM 및 DMARC Office 365에 대 한 합니다. 시작 하기 위해 [Office 365에서 사용자 지정 도메인에서 보낸 아웃 바운드 전자 메일의 유효성을 검사를 사용 하 여 DKIM](use-dkim-to-validate-outbound-email.md)를 참조 합니다. 다음으로, [Office 365의 전자 메일의 유효성을 검사를 사용 하 여 DMARC](use-dmarc-to-validate-email.md)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="ec663-p129">Although SPF is designed to help prevent spoofing, but there are spoofing techniques that SPF cannot protect against. In order to protect against these, once you have set up SPF, you should also configure DKIM and DMARC for Office 365. To get started, see [Use DKIM to validate outbound email sent from your custom domain in Office 365](use-dkim-to-validate-outbound-email.md). Next, see [Use DMARC to validate email in Office 365](use-dmarc-to-validate-email.md).</span></span>
  
## <a name="troubleshooting-best-practices-for-spf-in-office-365"></a><span data-ttu-id="ec663-247">Office 365에서 SPF에 대 한 모범 사례 문제를 해결 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec663-247">Troubleshooting: Best practices for SPF in Office 365</span></span>
<span data-ttu-id="ec663-248"><a name="SPFTroubleshoot"> </a></span><span class="sxs-lookup"><span data-stu-id="ec663-248"></span></span>

<span data-ttu-id="ec663-p130">만 사용자 지정 도메인에 대 한 하나의 SPF TXT 레코드를 만들 수 있습니다. 라운드 로빈 상황을 사용 하면 여러 레코드를 만드는 및 SPF 실패 합니다. 이 문제를 방지 하려면 각 하위 도메인에 대 한 별도 레코드를 만들 수 있습니다. 예, contoso.com에 대 한 레코드가 둘 및 bulkmail.contoso.com에 대 한 다른 레코드를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ec663-p130">You can only create one SPF TXT record for your custom domain. Creating multiple records causes a round robin situation and SPF will fail. To avoid this, you can create separate records for each subdomain. For example, create one record for contoso.com and another record for bulkmail.contoso.com.</span></span>
  
<span data-ttu-id="ec663-p131">배달 전에 10 개 이상의 DNS 조회를 설정 하는 전자 메일 메시지를 받는 메일 서버를 _permerror_이 라고도 하는 영구 오류를 사용 하 여 응답 및 SPF 확인 실패 메시지가 발생 합니다. 다음과 유사한 오류가 포함 된 배달 못함 보고서 (NDR)와 함께 받는 서버 응답도 않을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ec663-p131">If an email message causes more than 10 DNS lookups before it is delivered, the receiving mail server will respond with a permanent error, also called a  _permerror_, and cause the message to fail the SPF check. The receiving server may also respond with a non-delivery report (NDR) that contains an error similar to these:</span></span>
  
- <span data-ttu-id="ec663-255">홉 수를 초과 하는 메시지입니다.</span><span class="sxs-lookup"><span data-stu-id="ec663-255">The message exceeded the hop count.</span></span>
    
- <span data-ttu-id="ec663-256">메시지에 너무 많은 경우 조회 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="ec663-256">The message required too many lookups.</span></span>
    
## <a name="avoiding-the-too-many-lookups-error-when-you-use-third-party-domains-with-office-365"></a><span data-ttu-id="ec663-257">제 3 자 도메인을 사용 하 여 Office 365를 사용 하는 경우에 "너무 많은 경우 조회" 오류를 방지 하기</span><span class="sxs-lookup"><span data-stu-id="ec663-257">Avoiding the "too many lookups" error when you use third-party domains with Office 365</span></span>
<span data-ttu-id="ec663-258"><a name="SPFTroubleshoot"> </a></span><span class="sxs-lookup"><span data-stu-id="ec663-258"></span></span>

<span data-ttu-id="ec663-p132">제 3 자 도메인에 대 한 일부 SPF TXT 레코드 직접 많은 DNS 조회를 수행 하려면 받는 서버입니다. 예 5 포함 Salesforce.com이 문서를이 작성할 때 해당 레코드에 문을 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec663-p132">Some SPF TXT records for third-party domains direct the receiving server to perform a large number of DNS lookups. For example, at the time of this writing, Salesforce.com contains 5 include statements in its record:</span></span>
  
```
v=spf1 include:_spf.google.com
include:_spfblock.salesforce.com
include:_qa.salesforce.com
include:_spfblock1.salesforce.com
include:spf.mandrillapp.com mx ~all
```

<span data-ttu-id="ec663-p133">이 오류를 방지 하려면이 목적을 위해 특별히 하위 도메인을 사용 하 여 대량 메일을 보내는 모든 사용자가 정책을 구현할 수 있습니다. 대량 전자 메일을 포함 하는 하위 도메인에 대 한 다른 SPF TXT 레코드를 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec663-p133">To avoid the error, you can implement a policy where anyone sending bulk email, for example, has to use a subdomain specifically for this purpose. You then define a different SPF TXT record for the subdomain that includes the bulk email.</span></span>
  
 <span data-ttu-id="ec663-p134">Salesforce.com 예제와 같은 일부 경우에 사용자의 SPF TXT 레코드에서 도메인을 사용 해야 하지만 또 어떤 경우에는 타사 수를 이미 만든이 목적을 위해 사용 하 여 하위 도메인이 합니다. 예 exacttarget.com SPF TXT 레코드를 사용 하는 하위 도메인을 만들었습니다.</span><span class="sxs-lookup"><span data-stu-id="ec663-p134">In some cases, like the salesforce.com example, you have to use the domain in your SPF TXT record, but in other cases, the third-party may have already created a subdomain for you to use for this purpose. For example, exacttarget.com has created a subdomain that you need to use for your SPF TXT record:</span></span> 
  
```
cust-spf.exacttarget.com
```

<span data-ttu-id="ec663-265">SPF TXT 레코드에서 타사 도메인을 포함 하는 경우 확인 하도록 요청 타사 어떤 도메인 또는 하위 도메인에 10 조회 하는 것을 방지 하기 위해 사용할 수를 제한 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec663-265">When you include third-party domains in your SPF TXT record, you need to confirm with the third-party which domain or subdomain to use in order to avoid running into the 10 lookup limit.</span></span>
  
## <a name="how-to-view-your-current-spf-txt-record-and-determine-the-number-of-lookups-that-it-requires"></a><span data-ttu-id="ec663-266">사용자의 현재 SPF TXT 레코드를 확인 하 고 필요 조회 수를 결정 하는 방법</span><span class="sxs-lookup"><span data-stu-id="ec663-266">How to view your current SPF TXT record and determine the number of lookups that it requires</span></span>
<span data-ttu-id="ec663-267"><a name="SPFTroubleshoot"> </a></span><span class="sxs-lookup"><span data-stu-id="ec663-267"></span></span>

<span data-ttu-id="ec663-p135">Nslookup을 사용 하 여 SPF TXT 레코드를 포함 하 여 DNS 레코드를 볼 수 있습니다. 또는 원할 경우 다양 한 SPF TXT 레코드의 콘텐츠를 보려면 사용할 수 있는 무료, 온라인 도구가 있습니다. SPF TXT 봐서는 레코드와의 연결 고리 과정을 따라 포함 문과 리디렉션하거나, 레코드가 필요 얼마나 많은 DNS 조회를 확인할 수 있습니다. 일부 온라인 도구 count에도 하 고 이러한 조회 표시 됩니다. 이 번호는 추적을 permerror 받는 서버에서 호출 영구적 오류를 트리거에서 조직에서 보낸 메시지를 차단 하는 데 도움이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ec663-p135">You can use nslookup to view your DNS records, including your SPF TXT record. Or, if you prefer, there are a number of free, online tools available that you can use to view the contents of your SPF TXT record. By looking at your SPF TXT record and following the chain of include statements and redirects, you can determine how many DNS lookups the record requires. Some online tools will even count and display these lookups for you. Keeping track of this number will help prevent messages sent from your organization from triggering a permanent error, called a permerror, from the receiving server.</span></span>
  
## <a name="for-more-information"></a><span data-ttu-id="ec663-273">자세한 내용</span><span class="sxs-lookup"><span data-stu-id="ec663-273">For more information</span></span>
<span data-ttu-id="ec663-274"><a name="SPFTroubleshoot"> </a></span><span class="sxs-lookup"><span data-stu-id="ec663-274"></span></span>

<span data-ttu-id="ec663-p136">도움이 필요 하십니까 SPF TXT 레코드 추가 (영문)? 다양 한 인기 있는 도메인 등록자에서 SPF (TXT) 레코드를 업데이트 하는 것에 대 한 [단계별 지침](https://office.microsoft.com/en-us/office365-suite-help/create-dns-records-for-office-365-HA102851099.aspx?CTT=5&amp;origin=HA102818404) 은 사용할 수 있습니다. [스팸 방지 메시지 헤더](anti-spam-message-headers.md) SPF 확인을 위한 Office 365에서 사용 되는 구문과 헤더 필드를 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec663-p136">Need help adding the SPF TXT record? [Step-by-step instructions](https://office.microsoft.com/en-us/office365-suite-help/create-dns-records-for-office-365-HA102851099.aspx?CTT=5&amp;origin=HA102818404) for updating SPF (TXT) records at a variety of popular domain registrars is available. [Anti-spam message headers](anti-spam-message-headers.md) includes the syntax and header fields used by Office 365 for SPF checks.</span></span> 
  

