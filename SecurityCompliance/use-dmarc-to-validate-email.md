---
title: DMARC를 사용하여 Office 365에서 전자 메일 유효성 검사
ms.author: tracyp
author: MSFTTracyP
manager: dansimp
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Priority
search.appverid:
- MET150
ms.assetid: 4a05898c-b8e4-4eab-bd70-ee912e349737
ms.collection:
- M365-security-compliance
description: 사용자의 Office 365 조직에서 보낸 메시지의 유효성을 검사하기 위해 도메인 기반 메시지 인증, 보고 및 적합성 (DMARC)을 구성하는 방법에 대해 알아봅니다.
ms.openlocfilehash: 95d1220f065633d899d415800e7ad9c5e91e759f
ms.sourcegitcommit: 33c8e9c16143650ca443d73e91631f9180a9268e
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/25/2019
ms.locfileid: "35854752"
---
# <a name="use-dmarc-to-validate-email-in-office-365"></a><span data-ttu-id="c41d7-103">DMARC를 사용하여 Office 365에서 전자 메일 유효성 검사</span><span class="sxs-lookup"><span data-stu-id="c41d7-103">Use DMARC to validate email in Office 365</span></span>

<span data-ttu-id="c41d7-104">도메인 기반 메시지 인증, 보고 및 적합성 ([DMARC](https://dmarc.org))은 SPF (Sender Policy Framework) 및 DKIM (DomainKeys Identified Mail)과 함께 작동하여 메일 발신자를 인증하고 대상 전자 메일 시스템이 사용자의 도메인에서 보낸 메시지를 신뢰하도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="c41d7-104">Domain-based Message Authentication, Reporting, and Conformance ([DMARC](https://dmarc.org)) works with Sender Policy Framework (SPF) and DomainKeys Identified Mail (DKIM) to authenticate mail senders and ensure that destination email systems trust messages sent from your domain.</span></span> <span data-ttu-id="c41d7-105">SPF 및 DKIM과 함께 DMARC를 구현하면 스푸핑 및 피싱 전자 메일에 대한 추가 보호 기능이 제공됩니다.</span><span class="sxs-lookup"><span data-stu-id="c41d7-105">Implementing DMARC with SPF and DKIM provides additional protection against spoofing and phishing email.</span></span> <span data-ttu-id="c41d7-106">DMARC는 수신 메일 시스템이 사용자의 도메인에서 보낸 SPF 또는 DKIM 확인에 실패한 메시지에 대해 수행할 작업을 결정하는 데 도움을 줍니다.</span><span class="sxs-lookup"><span data-stu-id="c41d7-106">DMARC helps receiving mail systems determine what to do with messages sent from your domain that fail SPF or DKIM checks.</span></span>
  
## <a name="how-do-spf-and-dmarc-work-together-to-protect-email-in-office-365"></a><span data-ttu-id="c41d7-107">SPF와 DMARC는 Office 365에서 전자 메일을 보호하기 위해 어떻게 함께 작동하나요?</span><span class="sxs-lookup"><span data-stu-id="c41d7-107">How do SPF and DMARC work together to protect email in Office 365?</span></span>
<span data-ttu-id="c41d7-108"><a name="SPFandDMARC"> </a></span><span class="sxs-lookup"><span data-stu-id="c41d7-108"></span></span>

 <span data-ttu-id="c41d7-109">전자 메일 메시지에는 여러 작성자, 발신자 또는 주소가 포함될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c41d7-109">An email message may contain multiple originator, or sender, addresses.</span></span> <span data-ttu-id="c41d7-110">이러한 주소는 다양한 목적으로 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c41d7-110">These addresses are used for different purposes.</span></span> <span data-ttu-id="c41d7-111">예를 들어 다음 주소를 살펴보겠습니다.</span><span class="sxs-lookup"><span data-stu-id="c41d7-111">For example, consider these addresses:</span></span> 
  
- <span data-ttu-id="c41d7-112">**"Mail From" 주소**: 발신자를 식별하고 배달 못 함 알림과 같은 메시지의 배달에 문제가 발생할 경우 반송 알림을 보낼 위치를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c41d7-112">**"Mail From" address**: Identifies the sender and specifies where to send return notices if any problems occur with the delivery of the message, such as non-delivery notices.</span></span> <span data-ttu-id="c41d7-113">전자 메일 메시지의 봉투 부분에 표시되며 일반적으로 전자 메일 응용 프로그램에는 표시되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c41d7-113">This appears in the envelope portion of an email message and is not usually displayed by your email application.</span></span> <span data-ttu-id="c41d7-114">5321.MailFrom 주소 또는 역-경로 주소라고도 합니다.</span><span class="sxs-lookup"><span data-stu-id="c41d7-114">This is sometimes called the 5321.MailFrom address or the reverse-path address.</span></span>
    
- <span data-ttu-id="c41d7-115">**"From" 주소**: 메일 응용 프로그램에서 발신자 주소로 표시되는 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="c41d7-115">**"From" address**: The address displayed as the From address by your mail application.</span></span> <span data-ttu-id="c41d7-116">이 주소는 전자 메일의 작성자를 식별합니다.</span><span class="sxs-lookup"><span data-stu-id="c41d7-116">This address identifies the author of the email.</span></span> <span data-ttu-id="c41d7-117">즉, 메시지 작성을 담당하는 개인 또는 시스템의 사서함입니다.</span><span class="sxs-lookup"><span data-stu-id="c41d7-117">That is, the mailbox of the person or system responsible for writing the message.</span></span> <span data-ttu-id="c41d7-118">이를 5322.From이라고도 합니다.</span><span class="sxs-lookup"><span data-stu-id="c41d7-118">This is sometimes called the 5322.From address.</span></span>
    
<span data-ttu-id="c41d7-119">SPF는 DNS TXT 레코드를 사용하여 지정된 도메인에 대해 인증된 전송 IP 주소 목록을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="c41d7-119">SPF uses a DNS TXT record to provide a list of authorized sending IP addresses for a given domain.</span></span> <span data-ttu-id="c41d7-120">일반적으로 SPF 검사는 5321.MailFrom 주소에 대해서만 수행됩니다.</span><span class="sxs-lookup"><span data-stu-id="c41d7-120">Normally, SPF checks are only performed against the 5321.MailFrom address.</span></span> <span data-ttu-id="c41d7-121">즉, SPF를 단독으로 사용하는 경우 5322.From 주소가 인증되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c41d7-121">This means that the 5322.From address is not authenticated when you use SPF by itself.</span></span> <span data-ttu-id="c41d7-122">이를 통해 SPF 검사를 통과했지만 스푸핑된 5322.From 발신자 주소를 가지고 있는 메시지를 사용자가 받을 수 있게 되는 시나리오가 가능합니다.</span><span class="sxs-lookup"><span data-stu-id="c41d7-122">This allows for a scenario where a user can receive a message which passes an SPF check but has a spoofed 5322.From sender address.</span></span> <span data-ttu-id="c41d7-123">예를 들어 다음 SMTP 내용을 살펴봅니다.</span><span class="sxs-lookup"><span data-stu-id="c41d7-123">For example, consider this SMTP transcript:</span></span>
  
```
S: Helo woodgrovebank.com
S: Mail from: phish@phishing.contoso.com
S: Rcpt to: astobes@tailspintoys.com
S: data
S: To: "Andrew Stobes" <astobes@tailspintoys.com>
S: From: "Woodgrove Bank Security" <security@woodgrovebank.com>
S: Subject: Woodgrove Bank - Action required
S:
S: Greetings User,
S: 
S: We need to verify your banking details.
S: Please click the following link to verify that we have the right information for your account.
S: 
S: http://short.url/woodgrovebank/updateaccount/12-121.aspx
S:
S: Thank you,
S: Woodgrove Bank
S: .
```

<span data-ttu-id="c41d7-124">이 내용에서 발신자 주소는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="c41d7-124">In this transcript, the sender addresses are as follows:</span></span>
  
- <span data-ttu-id="c41d7-125">Mail from 주소 (5321.MailFrom): phish@phishing.contoso.com</span><span class="sxs-lookup"><span data-stu-id="c41d7-125">Mail from address (5321.MailFrom): phish@phishing.contoso.com</span></span>
    
- <span data-ttu-id="c41d7-126">From 주소 (5322.From): security@woodgrovebank.com</span><span class="sxs-lookup"><span data-stu-id="c41d7-126">From address (5322.From): security@woodgrovebank.com</span></span>
    
<span data-ttu-id="c41d7-127">SPF를 구성한 경우 수신 서버는 Mail from 주소인 phish@phishing.contoso.com에 대해 검사를 수행합니다.</span><span class="sxs-lookup"><span data-stu-id="c41d7-127">If you configured SPF, then the receiving server performs a check against the Mail from address phish@phishing.contoso.com.</span></span> <span data-ttu-id="c41d7-128">메시지가 도메인 phishing.contoso.com의 유효한 출처에서 온 경우 SPF 검사를 통과합니다.</span><span class="sxs-lookup"><span data-stu-id="c41d7-128">If the message came from a valid source for the domain phishing.contoso.com then the SPF check passes.</span></span> <span data-ttu-id="c41d7-129">전자 메일 클라이언트는 From 주소만 표시하므로 사용자에게 이 메시지는 security@woodgrovebank.com에서 온 것으로 보입니다.</span><span class="sxs-lookup"><span data-stu-id="c41d7-129">Since the email client only displays the From address, the user sees that this message came from security@woodgrovebank.com.</span></span> <span data-ttu-id="c41d7-130">SPF 단독으로는 woodgrovebank.com의 유효성이 인증되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="c41d7-130">With SPF alone, the validity of woodgrovebank.com was never authenticated.</span></span>
  
<span data-ttu-id="c41d7-131">DMARC를 사용하는 경우 수신 서버는 From 주소에 대해서도 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="c41d7-131">When you use DMARC, the receiving server also performs a check against the From address.</span></span> <span data-ttu-id="c41d7-132">위의 예제에서 woodgrovebank.com에 대한 DMARC TXT 레코드가 있는 경우 From 주소의 검사는 실패합니다.</span><span class="sxs-lookup"><span data-stu-id="c41d7-132">In the example above, if there is a DMARC TXT record in place for woodgrovebank.com, then the check against the From address fails.</span></span>
  
## <a name="what-is-a-dmarc-txt-record"></a><span data-ttu-id="c41d7-133">DMARC TXT 레코드란 무엇인가요?</span><span class="sxs-lookup"><span data-stu-id="c41d7-133">What is a DMARC TXT record?</span></span>
<span data-ttu-id="c41d7-134"><a name="WhatisDMARC"> </a></span><span class="sxs-lookup"><span data-stu-id="c41d7-134"></span></span>

<span data-ttu-id="c41d7-135">SPF의 DNS 레코드와 마찬가지로 DMARC의 레코드는 스푸핑 및 피싱을 방지하는 데 도움이 되는 DNS 텍스트 (TXT) 레코드입니다.</span><span class="sxs-lookup"><span data-stu-id="c41d7-135">Like the DNS records for SPF, the record for DMARC is a DNS text (TXT) record that helps prevent spoofing and phishing.</span></span> <span data-ttu-id="c41d7-136">DMARC TXT 레코드를 DNS에 게시합니다.</span><span class="sxs-lookup"><span data-stu-id="c41d7-136">You publish DMARC TXT records in DNS.</span></span> <span data-ttu-id="c41d7-137">DMARC TXT 레코드는 전자 메일을 보내는 도메인의 알려진 소유자와 대조하여 전자 메일 작성자의 IP 주소를 확인함으로써 전자 메일 메시지의 출처에 대한 유효성을 검사합니다.</span><span class="sxs-lookup"><span data-stu-id="c41d7-137">SPF records validate the origin of email messages by verifying the IP address of the sender against the alleged owner of the sending domain.</span></span> <span data-ttu-id="c41d7-138">DMARC TXT 레코드는 인증된 아웃바운드 전자 메일 서버를 식별합니다.</span><span class="sxs-lookup"><span data-stu-id="c41d7-138">The SPF record identifies authorized outbound email servers.</span></span> <span data-ttu-id="c41d7-139">그런 다음 대상 전자 메일 시스템은 수신한 메시지가 인증된 아웃바운드 전자 메일 서버에서 보낸 것인지 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c41d7-139">Destination email systems verify that messages originate from authorized outbound email servers.</span></span>
  
<span data-ttu-id="c41d7-140">Microsoft의 DMARC TXT 레코드는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="c41d7-140">Microsoft's DMARC TXT record looks something like this:</span></span>
  
```
_dmarc.microsoft.com.   3600    IN      TXT     "v=DMARC1; p=none; pct=100; rua=mailto:d@rua.agari.com; ruf=mailto:d@ruf.agari.com; fo=1" 
```

<span data-ttu-id="c41d7-141">Microsoft는 자사의 DMARC 보고서를 제3자인 [Agari](https://agari.com)에게 보냅니다.</span><span class="sxs-lookup"><span data-stu-id="c41d7-141">Microsoft sends its DMARC reports to [Agari](https://agari.com), a 3rd party.</span></span> <span data-ttu-id="c41d7-142">Agari는 DMARC 보고서를 수집하고 분석합니다.</span><span class="sxs-lookup"><span data-stu-id="c41d7-142">Agari collects and analyzes DMARC reports.</span></span>
  
## <a name="implement-dmarc-for-inbound-mail"></a><span data-ttu-id="c41d7-143">인바운드 메일에 대한 DMARC 구현</span><span class="sxs-lookup"><span data-stu-id="c41d7-143">Implement DMARC for inbound mail</span></span>
<span data-ttu-id="c41d7-144"><a name="implementDMARCinbound"> </a></span><span class="sxs-lookup"><span data-stu-id="c41d7-144"></span></span>

<span data-ttu-id="c41d7-145">Office 365에서 받는 메일에 대해 DMARC를 설정하지 않아도 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c41d7-145">You don't have to do a thing to set up DMARC for mail that you receive in Office 365.</span></span> <span data-ttu-id="c41d7-146">저희가 사용자를 위해 모든 것을 담당합니다.</span><span class="sxs-lookup"><span data-stu-id="c41d7-146">We've taken care of everything for you.</span></span> <span data-ttu-id="c41d7-147">DMARC 검사를 통과하지 못한 메일에 대해 알아보려면 [Office 365에서 DMARC에 실패한 인바운드 전자 메일을 처리하는 방법](use-dmarc-to-validate-email.md#inbounddmarcfail)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="c41d7-147">If you want to learn what happens to mail that fails to pass our DMARC checks, see [How Office 365 handles inbound email that fails DMARC](use-dmarc-to-validate-email.md#inbounddmarcfail).</span></span>
  
## <a name="implement-dmarc-for-outbound-mail-from-office-365"></a><span data-ttu-id="c41d7-148">Office 365의 아웃바운드 메일에 대한 DMARC 구현</span><span class="sxs-lookup"><span data-stu-id="c41d7-148">Implement DMARC for outbound mail from Office 365</span></span>
<span data-ttu-id="c41d7-149"><a name="implementDMARCoutbound"> </a></span><span class="sxs-lookup"><span data-stu-id="c41d7-149"></span></span>

<span data-ttu-id="c41d7-150">Office 365를 사용하지만 사용자 지정 도메인을 사용하지 않는 경우 (즉, onmicrosoft.com을 사용하는 경우) 사용자 조직의 DMARC를 구성하거나 구현하기 위해 다른 작업을 수행할 필요가 없습니다.</span><span class="sxs-lookup"><span data-stu-id="c41d7-150">If you use Office 365 but you aren't using a custom domain, that is, you use onmicrosoft.com, you don't need to do anything else to configure or implement DMARC for your organization.</span></span> <span data-ttu-id="c41d7-151">SPF는 이미 설정되어 있으며 Office 365는 보내는 메일에 대해 DKIM 서명을 자동으로 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="c41d7-151">SPF is already set up for you and Office 365 automatically generates a DKIM signature for your outgoing mail.</span></span> <span data-ttu-id="c41d7-152">이 서명에 대한 자세한 내용은 [DKIM 및 Office 365의 기본 동작](use-dkim-to-validate-outbound-email.md#DefaultDKIMbehavior)을 참조합니다.</span><span class="sxs-lookup"><span data-stu-id="c41d7-152">For more information about this signature, see [Default behavior for DKIM and Office 365](use-dkim-to-validate-outbound-email.md#DefaultDKIMbehavior).</span></span>
  
 <span data-ttu-id="c41d7-153">사용자 지정 도메인이 있거나 Office 365 외에 온-프레미스 Exchange 서버를 사용하는 경우 아웃바운드 메일에 대해 DMARC를 수동으로 구현해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c41d7-153">If you have a custom domain or you are using on-premises Exchange servers in addition to Office 365, you need to manually implement DMARC for your outbound mail.</span></span> <span data-ttu-id="c41d7-154">사용자 정의 도메인에 DMARC를 구현하는 단계는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="c41d7-154">Implementing DMARC for your custom domain includes these steps:</span></span> 
  
- [<span data-ttu-id="c41d7-155">1단계: 사용자 도메인의 유효한 메일 출처 식별</span><span class="sxs-lookup"><span data-stu-id="c41d7-155">Step 1: Identify valid sources of mail for your domain</span></span>](use-dmarc-to-validate-email.md#IdentifyValidSources)
    
- [<span data-ttu-id="c41d7-156">2단계: Office 365에서 사용자 도메인에 대한 SPF 설정</span><span class="sxs-lookup"><span data-stu-id="c41d7-156">Step 2: Set up SPF for your domain in Office 365</span></span>](use-dmarc-to-validate-email.md#ConfigSPF)
    
- [<span data-ttu-id="c41d7-157">3단계: Office 365에서 사용자 지정 도메인에 대한 DKIM 설정</span><span class="sxs-lookup"><span data-stu-id="c41d7-157">Step 3: Set up DKIM for your custom domain in Office 365</span></span>](use-dmarc-to-validate-email.md#ConfigDKIM)
    
- [<span data-ttu-id="c41d7-158">4단계: Office 365에서 사용자 도메인에 대한 DMARC TXT 레코드 형성</span><span class="sxs-lookup"><span data-stu-id="c41d7-158">Step 4: Form the DMARC TXT record for your domain in Office 365</span></span>](use-dmarc-to-validate-email.md#CreateDMARCRecord)
    
### <a name="step-1-identify-valid-sources-of-mail-for-your-domain"></a><span data-ttu-id="c41d7-159">1단계: 사용자 도메인의 유효한 메일 출처 식별</span><span class="sxs-lookup"><span data-stu-id="c41d7-159">Step 1: Identify valid sources of mail for your domain</span></span>
<span data-ttu-id="c41d7-160"><a name="IdentifyValidSources"> </a></span><span class="sxs-lookup"><span data-stu-id="c41d7-160"></span></span>

<span data-ttu-id="c41d7-161">이미 SPF를 설정한 경우 이 작업은 이미 진행한 것입니다.</span><span class="sxs-lookup"><span data-stu-id="c41d7-161">If you have already set up SPF then you have already gone through this exercise.</span></span> <span data-ttu-id="c41d7-162">그러나 DMARC의 경우 추가 고려 사항이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c41d7-162">However, for DMARC, there are additional considerations.</span></span> <span data-ttu-id="c41d7-163">사용자 도메인의 메일 출처를 식별할 때 두 가지 질문에 답해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c41d7-163">When identifying sources of mail for your domain there are two questions you need to answer:</span></span>
  
- <span data-ttu-id="c41d7-164">내 도메인에서 메시지를 보내는 IP 주소는 무엇인가요?</span><span class="sxs-lookup"><span data-stu-id="c41d7-164">What IP addresses send messages from my domain?</span></span>
    
- <span data-ttu-id="c41d7-165">나를 대신하여 제3자가 보낸 메일의 경우 5321.MailFrom과 5322.From 도메인이 일치하나요?</span><span class="sxs-lookup"><span data-stu-id="c41d7-165">For mail sent from third parties on my behalf, will the 5321.MailFrom and 5322.From domains match?</span></span>
    
### <a name="step-2-set-up-spf-for-your-domain-in-office-365"></a><span data-ttu-id="c41d7-166">2단계: Office 365에서 사용자 도메인에 대한 SPF 설정</span><span class="sxs-lookup"><span data-stu-id="c41d7-166">Step 2: Set up SPF for your domain in Office 365</span></span>
<span data-ttu-id="c41d7-167"><a name="ConfigSPF"> </a></span><span class="sxs-lookup"><span data-stu-id="c41d7-167"></span></span>

<span data-ttu-id="c41d7-168">이제 유효한 모든 발신자 목록이 있으므로 [스푸핑을 방지할 수 있도록 Office 365에서 SPF 설정](set-up-spf-in-office-365-to-help-prevent-spoofing.md) 단계를 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c41d7-168">Now that you have a list of all your valid senders you can follow the steps to [Set up SPF in Office 365 to help prevent spoofing](set-up-spf-in-office-365-to-help-prevent-spoofing.md).</span></span>
  
<span data-ttu-id="c41d7-169">예를 들어 contoso.com이 Exchange Online에서 메일을 보낸다고 가정하면, IP 주소가 192.168.0.1인 온-프레미스 Exchange 서버와 IP 주소가 192.168.100.100인 웹 응용 프로그램의 경우 SPF TXT 레코드는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="c41d7-169">For example, assuming contoso.com sends mail from Exchange Online, an on-premises Exchange server whose IP address is 192.168.0.1, and a web application whose IP address is 192.168.100.100, the SPF TXT record would look like this:</span></span>
  
```
contoso.com  IN  TXT  " v=spf1 ip4:192.168.0.1 ip4:192.168.100.100 include:spf.protection.outlook.com -all"
```

<span data-ttu-id="c41d7-170">모범 실무로서 SPF TXT 레코드에 제3자 발신자에 대한 고려를 해야합니다.</span><span class="sxs-lookup"><span data-stu-id="c41d7-170">As a best practice, ensure that your SPF TXT record takes into account third-party senders.</span></span>
  
### <a name="step-3-set-up-dkim-for-your-custom-domain-in-office-365"></a><span data-ttu-id="c41d7-171">3단계: Office 365에서 사용자 지정 도메인에 대한 DKIM 설정</span><span class="sxs-lookup"><span data-stu-id="c41d7-171">Step 3: Set up DKIM for your custom domain in Office 365</span></span>
<span data-ttu-id="c41d7-172"><a name="ConfigDKIM"> </a></span><span class="sxs-lookup"><span data-stu-id="c41d7-172"></span></span>

<span data-ttu-id="c41d7-173">SPF 설정을 마쳤으면 DKIM을 설정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c41d7-173">Once you have set up SPF, you need to set up DKIM.</span></span> <span data-ttu-id="c41d7-174">DKIM을 사용하면 메시지 머리글에 있는 전자 메일 메시지에 디지털 서명을 첨부할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c41d7-174">DKIM lets you add a digital signature to email messages in the message header.</span></span> <span data-ttu-id="c41d7-175">DKIM을 설정하지 않고 대신 Office 365에서 도메인의 기본 DKIM 구성을 사용하도록 허용하는 경우 DMARC가 실패할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c41d7-175">If you do not set up DKIM and instead allow Office 365 to use the default DKIM configuration for your domain, DMARC may fail.</span></span> <span data-ttu-id="c41d7-176">이는 기본 DKIM 구성은 사용자 지정 도메인이 아닌 초기 onmicrosoft.com 도메인을 5322.From 주소로 사용하기 때문입니다.</span><span class="sxs-lookup"><span data-stu-id="c41d7-176">This is because the default DKIM configuration uses your initial onmicrosoft.com domain as the 5322.From address, not your custom domain.</span></span> <span data-ttu-id="c41d7-177">이렇게 하면 사용자 도메인에서 보낸 모든 전자 메일의 5321.MailFrom과 5322.From 주소가 일치하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c41d7-177">This forces a mismatch between the 5321.MailFrom and the 5322.From addresses in all email sent from your domain.</span></span>
  
<span data-ttu-id="c41d7-178">사용자를 대신하여 메일을 발송하는 제3자 발신자가 있고 발신한 메일이 5321.MailFrom 및 5322.From 주소와 일치하지 않으면 해당 이메일에 대해 DMARC가 실패합니다.</span><span class="sxs-lookup"><span data-stu-id="c41d7-178">If you have third-party senders that send mail on your behalf and the mail they send has mismatched 5321.MailFrom and 5322.From addresses, DMARC will fail for that email.</span></span> <span data-ttu-id="c41d7-179">이를 방지하려면 해당 제3자 발신자와 함께 사용자 도메인에 DKIM을 설정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c41d7-179">To avoid this, you need to set up DKIM for your domain specifically with that third-party sender.</span></span> <span data-ttu-id="c41d7-180">이를 통해 Office 365는 이 제3자 서비스의 전자 메일을 인증할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c41d7-180">This allows Office 365 to authenticate email from this 3rd-party service.</span></span> <span data-ttu-id="c41d7-181">그러나 이는 또한 Yahoo, Gmail 및 Comcast와 같은 곳에서 메일을 수신할 때 제3자가 보낸 전자 메일이 마치 사용자가 보낸 전자 메일로 확인하도록 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c41d7-181">However, it also allows others, for example, Yahoo, Gmail, and Comcast, to verify email sent to them by the third-party as if it was email sent by you.</span></span> <span data-ttu-id="c41d7-182">이 기능은 사용자 고객의 사서함 위치에 관계없이 그들이 사용자 도메인과 신뢰를 구축할 수 있게 해주며 동시에 Office 365는 사용자 도메인의 인증 확인을 통과하기 때문에 스푸핑으로 인해 메시지를 스팸으로 표시하지 않는 이점이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c41d7-182">This is beneficial because it allows your customers to build trust with your domain no matter where their mailbox is located, and at the same time Office 365 won't mark a message as spam due to spoofing because it passes authentication checks for your domain.</span></span>
  
<span data-ttu-id="c41d7-183">사용자 도메인을 스푸핑할 수 있도록 제3자 발신자에 대해 DKIM을 설정하는 방법을 포함하여 도메인에 DKIM을 설정하는 방법에 대한 지침은 [DKIM을 사용하여 Office 365의 사용자 지정 도메인에서 전송한 아웃바운드 전자 메일의 유효성을 검사](use-dkim-to-validate-outbound-email.md)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="c41d7-183">For instructions on setting up DKIM for your domain, including how to set up DKIM for third-party senders so they can spoof your domain, see [Use DKIM to validate outbound email sent from your custom domain in Office 365](use-dkim-to-validate-outbound-email.md).</span></span>
  
### <a name="step-4-form-the-dmarc-txt-record-for-your-domain-in-office-365"></a><span data-ttu-id="c41d7-184">4단계: Office 365에서 사용자 도메인에 대한 DMARC TXT 레코드 형성</span><span class="sxs-lookup"><span data-stu-id="c41d7-184">Step 4: Form the DMARC TXT record for your domain in Office 365</span></span>
<span data-ttu-id="c41d7-185"><a name="CreateDMARCRecord"> </a></span><span class="sxs-lookup"><span data-stu-id="c41d7-185"></span></span>

<span data-ttu-id="c41d7-186">여기에 언급되지 않은 다른 구문 옵션도 있지만 이것이 Office 365에 가장 일반적으로 사용되는 옵션입니다.</span><span class="sxs-lookup"><span data-stu-id="c41d7-186">Although there are other syntax options that are not mentioned here, these are the most commonly used options for Office 365.</span></span> <span data-ttu-id="c41d7-187">사용자 도메인의 DMARC TXT 레코드를 다음 형식으로 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="c41d7-187">Form the DMARC TXT record for your domain in the format:</span></span>
  
```
_dmarc.domain  TTL  IN  TXT  "v=DMARC1; pct=100; p=policy"
```

<span data-ttu-id="c41d7-188">여기서 각 부분이 나타내는 의미는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="c41d7-188">where:</span></span>
  
- <span data-ttu-id="c41d7-189">*도메인*은 사용자가 보호할 도메인입니다.</span><span class="sxs-lookup"><span data-stu-id="c41d7-189">*domain* is the domain you want to protect.</span></span> <span data-ttu-id="c41d7-190">기본적으로 레코드는 도메인 및 모든 하위 도메인의 메일을 보호합니다.</span><span class="sxs-lookup"><span data-stu-id="c41d7-190">By default, the record protects mail from the domain and all subdomains.</span></span> <span data-ttu-id="c41d7-191">예를 들어 \_dmarc.contoso.com을 지정하면 DMARC는 housewares.contoso.com 또는 plumbing.contoso.com과 같은 도메인 및 모든 하위 도메인에서 메일을 보호합니다.</span><span class="sxs-lookup"><span data-stu-id="c41d7-191">For example, if you specify \_dmarc.contoso.com, then DMARC protects mail from the domain and all subdomains, such as housewares.contoso.com or plumbing.contoso.com.</span></span> 
    
- <span data-ttu-id="c41d7-192">*TTL*은 항상 1시간에 해당합니다.</span><span class="sxs-lookup"><span data-stu-id="c41d7-192">*TTL* should always be the equivalent of one hour.</span></span> <span data-ttu-id="c41d7-193">TTL에 사용되는 단위 (시간 (1시간), 분 (60분) 또는 초 (3,600초))는 도메인의 등록 기관에 따라 다릅니다.</span><span class="sxs-lookup"><span data-stu-id="c41d7-193">The unit used for TTL, either hours (1 hour), minutes (60 minutes), or seconds (3600 seconds), will vary depending on the registrar for your domain.</span></span> 
    
- <span data-ttu-id="c41d7-194">*pct = 100*은 이 규칙을 전자 메일의 100%에 사용해야 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="c41d7-194">*pct=100* indicates that this rule should be used for 100% of email.</span></span>
    
- <span data-ttu-id="c41d7-195">*정책*은 DMARC가 실패하는 경우 수신 서버에서 어떤 정책을 따를 것인지를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c41d7-195">*policy* specifies what policy you want the receiving server to follow if DMARC fails.</span></span> <span data-ttu-id="c41d7-196">정책을 없음, 격리 또는 거부로 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c41d7-196">You can set the policy to none, quarantine, or reject.</span></span> 
    
<span data-ttu-id="c41d7-197">사용할 옵션에 대한 자세한 내용은 [Office 365에서 DMARC를 구현하기 위한 모범 사례](use-dmarc-to-validate-email.md#DMARCbestpractices)의 개념을 숙지하세요.</span><span class="sxs-lookup"><span data-stu-id="c41d7-197">For information about which options to use, become familiar with the concepts in [Best practices for implementing DMARC in Office 365](use-dmarc-to-validate-email.md#DMARCbestpractices).</span></span>
  
<span data-ttu-id="c41d7-198">예제:</span><span class="sxs-lookup"><span data-stu-id="c41d7-198">Examples:</span></span>
  
- <span data-ttu-id="c41d7-199">정책을 없음으로 설정</span><span class="sxs-lookup"><span data-stu-id="c41d7-199">Policy set to none</span></span>
  
    ```
    _dmarc.contoso.com 3600 IN  TXT  "v=DMARC1; p=none"
    ```

- <span data-ttu-id="c41d7-200">정책을 격리로 설정</span><span class="sxs-lookup"><span data-stu-id="c41d7-200">Policy set to quarantine</span></span>
  
    ```
    _dmarc.contoso.com 3600 IN  TXT  "v=DMARC1; p=quarantine"
    ```

- <span data-ttu-id="c41d7-201">정책을 거부로 설정</span><span class="sxs-lookup"><span data-stu-id="c41d7-201">Policy set to reject</span></span>
  
    ```
    _dmarc.contoso.com  3600 IN  TXT  "v=DMARC1; p=reject"
    ```

<span data-ttu-id="c41d7-202">레코드를 구성한 후에는 도메인 등록 기관에서 레코드를 업데이트해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c41d7-202">Once you have formed your record, you need to update the record at your domain registrar.</span></span> <span data-ttu-id="c41d7-203">Office 365의 DNS 레코드에 DMARC TXT 레코드를 추가하는 방법에 대한 지침은 [DNS 레코드를 관리할 때 Office 365용 DNS 레코드 만들기](https://support.office.com/article/b0f3fdca-8a80-4e8e-9ef3-61e8a2a9ab23)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="c41d7-203">For instructions on adding the DMARC TXT record to your DNS records for Office 365, see [Create DNS records for Office 365 when you manage your DNS records](https://support.office.com/article/b0f3fdca-8a80-4e8e-9ef3-61e8a2a9ab23).</span></span>
  
## <a name="best-practices-for-implementing-dmarc-in-office-365"></a><span data-ttu-id="c41d7-204">Office 365에서 DMARC를 구현하는 모범 사례</span><span class="sxs-lookup"><span data-stu-id="c41d7-204">Best practices for implementing DMARC in Office 365</span></span>
<span data-ttu-id="c41d7-205"><a name="DMARCbestpractices"> </a></span><span class="sxs-lookup"><span data-stu-id="c41d7-205"></span></span>

<span data-ttu-id="c41d7-206">나머지 메일 흐름에 영향을 주지 않고 DMARC를 점진적으로 구현할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c41d7-206">You can implement DMARC gradually without impacting the rest of your mail flow.</span></span> <span data-ttu-id="c41d7-207">이 단계를 따르는 롤아웃 계획을 만들고 구현합니다.</span><span class="sxs-lookup"><span data-stu-id="c41d7-207">Create and implement a roll out plan that follows these steps.</span></span> <span data-ttu-id="c41d7-208">아래 단계를 진행하기 전에 먼저 하위 도메인, 다른 하위 도메인을 차례로 수행하고, 마지막으로 사용자 조직의 최상위 도메인을 수행합니다.</span><span class="sxs-lookup"><span data-stu-id="c41d7-208">Do each of these steps first with a sub-domain, then other sub-domains, and finally with the top-level domain in your organization before moving on to the next step.</span></span>
  
1. <span data-ttu-id="c41d7-209">DMARC 구현의 영향 모니터링</span><span class="sxs-lookup"><span data-stu-id="c41d7-209">Monitor the impact of implementing DMARC</span></span>
    
    <span data-ttu-id="c41d7-210">DMARC 수신자가 해당 도메인을 사용하여 볼 수 있는 메시지에 대한 통계를 사용자에게 보내도록 요청하는 하위 도메인 또는 도메인에 대한 간단한 모니터링 모드 레코드를 사용하여 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="c41d7-210">Start with a simple monitoring-mode record for a sub-domain or domain that requests that DMARC receivers send you statistics about messages that they see using that domain.</span></span> <span data-ttu-id="c41d7-211">모니터링 모드 레코드는 정책이 none (p=none)으로 설정된 DMARC TXT 레코드입니다.</span><span class="sxs-lookup"><span data-stu-id="c41d7-211">A monitoring-mode record is a DMARC TXT record that has its policy set to none (p=none).</span></span> <span data-ttu-id="c41d7-212">많은 회사에서는 더욱 제한적인 DMARC 정책을 게시했을 때 손실이 발생할 수 있는 이메일 양을 정확히 알 수 없기 때문에 p=none으로 DMARC TXT 레코드를 게시합니다.</span><span class="sxs-lookup"><span data-stu-id="c41d7-212">Many companies publish a DMARC TXT record with p=none because they are unsure about how much email they may lose by publishing a more restrictive DMARC policy.</span></span> 
    
    <span data-ttu-id="c41d7-213">메시징 인프라에서 SPF 또는 DKIM을 구현하기 전에도 이 작업을 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c41d7-213">You can do this even before you've implemented SPF or DKIM in your messaging infrastructure.</span></span> <span data-ttu-id="c41d7-214">그러나 SPF 및 DKIM을 구현할 때까지는 DMARC를 사용하여 메일을 효과적으로 격리하거나 거부할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="c41d7-214">However, you won't be able to effectively quarantine or reject mail by using DMARC until you also implement SPF and DKIM.</span></span> <span data-ttu-id="c41d7-215">SPF 및 DKIM을 도입하면서 DMARC를 통해 생성된 보고서에는 이러한 검사를 통과한 메시지 수와 출처를 제공하고 그렇지 않은 메시지에 대해서도 이를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="c41d7-215">As you introduce SPF and DKIM, the reports generated through DMARC will provide the numbers and sources of messages that pass these checks, and those that don't.</span></span> <span data-ttu-id="c41d7-216">이를 통해 다루어지는 정상/비정상적인 트래픽의 양을 쉽게 파악하고 이에 따른 문제를 해결할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c41d7-216">You can easily see how much of your legitimate traffic is or isn't covered by them, and troubleshoot any problems.</span></span> <span data-ttu-id="c41d7-217">또한 얼마나 많은 사기성 메시지가 전송되는지, 어디로부터 전송되는지 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c41d7-217">You'll also begin to see how many fraudulent messages are being sent, and from where.</span></span>
    
2. <span data-ttu-id="c41d7-218">DMARC 실패한 메일을 외부 메일 시스템에서 격리하도록 요청</span><span class="sxs-lookup"><span data-stu-id="c41d7-218">Request that external mail systems quarantine mail that fails DMARC</span></span>
    
    <span data-ttu-id="c41d7-219">정상적인 트래픽의 전부 또는 대부분이 SPF 및 DKIM에 의해 보호된다는 것을 믿고 DMARC 구현이 미치는 영향을 이해하고 있는 경우에는 격리 정책을 구현할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c41d7-219">When you believe that all or most of your legitimate traffic is protected by SPF and DKIM, and you understand the impact of implementing DMARC, you can implement a quarantine policy.</span></span> <span data-ttu-id="c41d7-220">격리 정책은 정책이 격리 (p=quarantine)으로 설정된 DMARC TXT 레코드입니다.</span><span class="sxs-lookup"><span data-stu-id="c41d7-220">A quarantine policy is a DMARC TXT record that has its policy set to quarantine (p=quarantine).</span></span> <span data-ttu-id="c41d7-221">이렇게 하면 DMARC 수신자에게 DMARC 검사에 실패한 사용자 도메인의 메시지를 사용자 고객의 받은 편지함 대신 스팸 폴더의 로컬과 같은 곳에 메시지를 넣도록 요청합니다.</span><span class="sxs-lookup"><span data-stu-id="c41d7-221">By doing this, you are asking DMARC receivers to put messages from your domain that fail DMARC into the local equivalent of a spam folder instead of your customers' inboxes.</span></span>
    
3. <span data-ttu-id="c41d7-222">외부 메일 시스템이 DMARC에 실패한 메시지를 허용하지 않도록 요청</span><span class="sxs-lookup"><span data-stu-id="c41d7-222">Request that external mail systems not accept messages that fail DMARC</span></span>
    
    <span data-ttu-id="c41d7-223">마지막 단계는 거부 정책을 구현하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="c41d7-223">The final step is implementing a reject policy.</span></span> <span data-ttu-id="c41d7-224">거부 정책은 정책이 거부 (p=reject)로 설정된 DMARC TXT 레코드입니다.</span><span class="sxs-lookup"><span data-stu-id="c41d7-224">A reject policy is a DMARC TXT record that has its policy set to reject (p=reject).</span></span> <span data-ttu-id="c41d7-225">이렇게 하면 DMARC 수신자에게 DMARC 검사에 실패한 메시지를 수락하지 않도록 요청합니다.</span><span class="sxs-lookup"><span data-stu-id="c41d7-225">When you do this, you're asking DMARC receivers not to accept messages that fail the DMARC checks.</span></span> 
    
## <a name="how-office-365-handles-outbound-email-that-fails-dmarc"></a><span data-ttu-id="c41d7-226">Office 365가 DMARC 검사에 실패한 아웃바운드 전자 메일을 처리하는 방법</span><span class="sxs-lookup"><span data-stu-id="c41d7-226">How Office 365 handles outbound email that fails DMARC</span></span>
<span data-ttu-id="c41d7-227"><a name="outbounddmarcfail"> </a></span><span class="sxs-lookup"><span data-stu-id="c41d7-227"></span></span>

<span data-ttu-id="c41d7-228">메시지가 Office 365로 부터 아웃바운드 되고 DMARC 검사에 실패하고 정책을 p=quarantne 또는 p=reject로 설정한 경우 메시지는 [아웃바운드 메시지용 높은 위험 배달 풀](high-risk-delivery-pool-for-outbound-messages.md)로 경로 지정됩니다.</span><span class="sxs-lookup"><span data-stu-id="c41d7-228">If a message is outbound from Office 365 and fails DMARC, and you have set the policy to p=quarantine or p=reject, the message is routed through the [High-risk delivery pool for outbound messages](high-risk-delivery-pool-for-outbound-messages.md).</span></span> <span data-ttu-id="c41d7-229">아웃바운드 전자 메일에 대한 오버라이드는 없습니다.</span><span class="sxs-lookup"><span data-stu-id="c41d7-229">There is no override for outbound email.</span></span>
  
<span data-ttu-id="c41d7-230">DMARC 거부 정책 (p=reject)을 게시하면 서비스를 통해 아웃바운드 메시지를 릴레이할 때 메시지가 사용자 도메인에 대해 SPF 또는 DKIM을 통과할 수 없으므로 Office 365의 다른 고객이 사용자 도메인을 스푸핑할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="c41d7-230">If you publish a DMARC reject policy (p=reject), no other customer in Office 365 can spoof your domain because messages will not be able to pass SPF or DKIM for your domain when relaying a message outbound through the service.</span></span> <span data-ttu-id="c41d7-231">그러나 DMARC 거부 정책을 게시했지만 Office 365를 통해 모든 전자 메일을 인증하지 않은 경우 그 중 일부는 인바운드 전자 메일에 대한 스팸으로 표시되거나 (위에 설명된 것처럼) 또는 SPF를 게시하지 않고 서비스를 통해 아웃바운드 릴레이하려고 시도하면 거부됩니다.</span><span class="sxs-lookup"><span data-stu-id="c41d7-231">However, if you do publish a DMARC reject policy but don't have all of your email authenticated through Office 365, some of it may be marked as spam for inbound email (as described above), or it will be rejected if you do not publish SPF and try to relay it outbound through the service.</span></span> <span data-ttu-id="c41d7-232">예를 들어, DMARC TXT 레코드를 형성할 때 사용자 도메인을 대신하여 메일을 보내는 서버 및 앱의 일부 IP 주소를 포함하지 않은 경우에 발생합니다.</span><span class="sxs-lookup"><span data-stu-id="c41d7-232">This happens, for example, if you forget to include some of the IP addresses for servers and apps that send mail on behalf of your domain when you form your DMARC TXT record.</span></span>
  
## <a name="how-office-365-handles-inbound-email-that-fails-dmarc"></a><span data-ttu-id="c41d7-233">Office 365가 DMARC 검사에 실패한 인바운드 전자 메일을 처리하는 방법</span><span class="sxs-lookup"><span data-stu-id="c41d7-233">How Office 365 handles inbound email that fails DMARC</span></span>
<span data-ttu-id="c41d7-234"><a name="inbounddmarcfail"> </a></span><span class="sxs-lookup"><span data-stu-id="c41d7-234"></span></span>

<span data-ttu-id="c41d7-235">발신 서버의 DMARC 정책이 p=reject이면 EOP는 메시지를 거부하는 대신 스팸으로 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="c41d7-235">If the DMARC policy of the sending server is p=reject, EOP marks the message as spam instead of rejecting it.</span></span> <span data-ttu-id="c41d7-236">즉, 인바운드 전자 메일의 경우 Office 365는 p=reject 및 p=quarantine을 동일한 방식으로 처리합니다.</span><span class="sxs-lookup"><span data-stu-id="c41d7-236">In other words, for inbound email, Office 365 treats p=reject and p=quarantine the same way.</span></span>
  
<span data-ttu-id="c41d7-237">일부 정상적인 전자 메일이 DMARC 검사에 실패할 수 있으므로 Office 365는 이와 같이 구성됩니다.</span><span class="sxs-lookup"><span data-stu-id="c41d7-237">Office 365 is configured like this because some legitimate email may fail DMARC.</span></span> <span data-ttu-id="c41d7-238">예를 들어, 메일 그룹에 전송된 메시지가 모든 목록 참가자에게 릴레이되는 경우 DMARC 검사에 실패할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c41d7-238">For example, a message might fail DMARC if it is sent to a mailing list that then relays the message to all list participants.</span></span> <span data-ttu-id="c41d7-239">Office 365에서 이러한 메시지를 거부하는 경우 사람들은 정상적인 전자 메일을 잃을 수 있으며 이를 되찾을 방법이 없습니다.</span><span class="sxs-lookup"><span data-stu-id="c41d7-239">If Office 365 rejected these messages, people could lose legitimate email and have no way to retrieve it.</span></span> <span data-ttu-id="c41d7-240">대신 이러한 메시지는 여전히 DMARC 검사에 실패하지만 스팸으로 표시되고 거부되지는 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c41d7-240">Instead, these messages will still fail DMARC but they will be marked as spam and not rejected.</span></span> <span data-ttu-id="c41d7-241">원하는 경우 사용자는 다음 방법을 통해 받은 편지함에서 이러한 메시지를 계속 받을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c41d7-241">If desired, users can still get these messages in their inbox through these methods:</span></span>
  
- <span data-ttu-id="c41d7-242">사용자가 전자 메일 클라이언트를 사용하여 개별적으로 안전한 발신자를 추가</span><span class="sxs-lookup"><span data-stu-id="c41d7-242">Users add safe senders individually by using their email client</span></span>
    
- <span data-ttu-id="c41d7-243">관리자는 특정 발신자의 메시지를 허용하는 모든 사용자에 대해 Exchange 메일 흐름 규칙 (전송 규칙이라고도 함)을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c41d7-243">Administrators create an Exchange mail flow rule (also known as a transport rule) for all users that allows messages for those particular senders.</span></span> 
    
## <a name="troubleshooting-your-dmarc-implementation"></a><span data-ttu-id="c41d7-244">DMARC 구현 문제 해결</span><span class="sxs-lookup"><span data-stu-id="c41d7-244">Troubleshooting your DMARC implementation</span></span>
<span data-ttu-id="c41d7-245"><a name="dmarctroubleshoot"> </a></span><span class="sxs-lookup"><span data-stu-id="c41d7-245"></span></span>

<span data-ttu-id="c41d7-246">EOP가 첫 번째 항목이 아닌 사용자 도메인의 MX 레코드를 구성한 경우 사용자 도메인에 대해 DMARC 검사 실패가 발생하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c41d7-246">If you have configured your domain's MX records where EOP is not the first entry, DMARC failures will not be enforced for your domain.</span></span> 
  
<span data-ttu-id="c41d7-247">사용자가 Office 365 고객이고 도메인의 기본 MX 레코드가 EOP를 가리키지 않는 경우에는 DMARC의 이점을 얻을 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="c41d7-247">If you're an Office 365 customer, and your domain's primary MX record does not point to EOP, you will not get the benefits of DMARC.</span></span> <span data-ttu-id="c41d7-248">예를 들어 MX 레코드를 온-프레미스 메일 서버로 지정한 다음 커넥터를 사용하여 전자 메일을 EOP로 경로 지정하는 경우에는 DMARC가 작동하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c41d7-248">For example, DMARC won't work if you point the MX record to your on-premises mail server and then route email to EOP by using a connector.</span></span> <span data-ttu-id="c41d7-249">이 시나리오에서 수신 도메인은 사용자의 허용된 도메인 중 하나이고 EOP는 기본 MX가 아닙니다.</span><span class="sxs-lookup"><span data-stu-id="c41d7-249">In this scenario, the receiving domain is one of your Accepted-Domains but EOP is not the primary MX.</span></span> <span data-ttu-id="c41d7-250">예를 들어 contoso.com이 MX를 자체적으로 가리키고 EOP를 보조 MX 레코드로 사용한다고 가정하면 contoso.com의 MX 레코드는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="c41d7-250">For example, suppose contoso.com points its MX at itself and uses EOP as a secondary MX record, contoso.com's MX record looks like the following:</span></span>
  
```
contoso.com     3600   IN  MX  0  mail.contoso.com
contoso.com     3600   IN  MX  10 contoso-com.mail.protection.outlook.com
```

<span data-ttu-id="c41d7-251">모든 또는 대부분의 전자 메일은 기본 MX인 mail.contoso.com으로 먼저 경로 지정된 다음, 메일은 EOP로 경로 지정됩니다.</span><span class="sxs-lookup"><span data-stu-id="c41d7-251">All, or most, email will first be routed to mail.contoso.com since it's the primary MX, and then mail will get routed to EOP.</span></span> <span data-ttu-id="c41d7-252">경우에 따라 EOP를 MX 레코드로 전혀 나열하지 않고 단순히 커넥터를 연결하여 전자 메일을 경로 지정할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c41d7-252">In some cases, you might not even list EOP as an MX record at all and simply hook up connectors to route your email.</span></span> <span data-ttu-id="c41d7-253">DMARC 유효성 검사를 수행하기 위해 EOP가 첫 번째 항목일 필요는 없습니다.</span><span class="sxs-lookup"><span data-stu-id="c41d7-253">EOP does not have to be the first entry for DMARC validation to be done.</span></span> <span data-ttu-id="c41d7-254">모든 온-프레미스/비O365 서버가 DMARC 검사를 수행할 것이라고 확신할 수 없기 때문에 이는 유효성 검사만을 보장합니다.</span><span class="sxs-lookup"><span data-stu-id="c41d7-254">It just ensures the validation, as we cannot be certain that all on-premise/non-O365 servers will do DMARC checks.</span></span>  <span data-ttu-id="c41d7-255">DMARC TXT 레코드를 설정할 때 DMARC는 고객의 도메인 (서버가 아님)에 대해 수행될 수 있지만, 실제로 수행을 적용하는 것은 수신 서버에 달려 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c41d7-255">DMARC is eligible to be enforced for a customer’s domain (not server) when you set up the DMARC TXT record, but it is up to the receiving server to actually do the enforcement.</span></span>  <span data-ttu-id="c41d7-256">수신 서버로 EOP를 설정하면 EOP가 DMARC 검사를 수행합니다.</span><span class="sxs-lookup"><span data-stu-id="c41d7-256">If you set up EOP as the receiving server, then EOP does the DMARC enforcement.</span></span>
  
## <a name="for-more-information"></a><span data-ttu-id="c41d7-257">자세한 내용</span><span class="sxs-lookup"><span data-stu-id="c41d7-257">For more information</span></span>
<span data-ttu-id="c41d7-258"><a name="sectionSection8"> </a></span><span class="sxs-lookup"><span data-stu-id="c41d7-258"></span></span>

<span data-ttu-id="c41d7-259">DMARC에 대한 자세한 정보가 필요하신가요?</span><span class="sxs-lookup"><span data-stu-id="c41d7-259">Want more information about DMARC?</span></span> <span data-ttu-id="c41d7-260">다음 리소스가 도움이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c41d7-260">Having trouble? These troubleshooting resources can help:</span></span>
  
- <span data-ttu-id="c41d7-261">[스팸 방지 메시지 헤더](anti-spam-message-headers.md)에는 Office 365에서 DMARC 검사에 사용하는 구문 및 헤더 필드가 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="c41d7-261">[Anti-spam message headers](anti-spam-message-headers.md) includes the syntax and header fields used by Office 365 for DMARC checks.</span></span> 
    
- <span data-ttu-id="c41d7-262">M <sup>3 </sup>AAWG (Messaging, Malware, Mobile Anti-Abuse Working Group)의 [DMARC 교육 시리즈](https://www.m3aawg.org/activities/training/dmarc-training-series)를 이용하세요.</span><span class="sxs-lookup"><span data-stu-id="c41d7-262">Take the [DMARC Training Series](https://www.m3aawg.org/activities/training/dmarc-training-series) from M <sup>3</sup>AAWG (Messaging, Malware, Mobile Anti-Abuse Working Group).</span></span>
    
- <span data-ttu-id="c41d7-263">[dmarcian](https://space.dmarcian.com/deployment/)의 검사 목록을 사용하세요.</span><span class="sxs-lookup"><span data-stu-id="c41d7-263">Use the checklist at [dmarcian](https://space.dmarcian.com/deployment/).</span></span>
    
- <span data-ttu-id="c41d7-264">[DMARC.org](https://dmarc.org)의 출처로 바로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="c41d7-264">Go directly to the source at [DMARC.org](https://dmarc.org).</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c41d7-265">참고 항목</span><span class="sxs-lookup"><span data-stu-id="c41d7-265">See also</span></span>
<span data-ttu-id="c41d7-266"><a name="sectionSection8"> </a></span><span class="sxs-lookup"><span data-stu-id="c41d7-266"></span></span>

[<span data-ttu-id="c41d7-267">Office 365에서 SPF (Sender Policy Framework)를 사용하여 스푸핑을 방지하는 방법</span><span class="sxs-lookup"><span data-stu-id="c41d7-267">How Office 365 uses Sender Policy Framework (SPF) to prevent spoofing</span></span>](how-office-365-uses-spf-to-prevent-spoofing.md)
  
[<span data-ttu-id="c41d7-268">스푸핑을 방지할 수 있도록 Office 365에서 SPF 설정</span><span class="sxs-lookup"><span data-stu-id="c41d7-268">Set up SPF in Office 365 to help prevent spoofing</span></span>](set-up-spf-in-office-365-to-help-prevent-spoofing.md)
  
<span data-ttu-id="c41d7-269">[DKIM을 사용하여 Office 365의 사용자 지정 도메인에서 전송한 아웃바운드 전자 메일의 유효성 검사](use-dkim-to-validate-outbound-email.md)</span><span class="sxs-lookup"><span data-stu-id="c41d7-269">For your primary domains, [Use DKIM to validate outbound email sent from your custom domain in Office 365](use-dkim-to-validate-outbound-email.md)</span></span>

