---
title: DMARC을 사용 하 여 Office 365의 전자 메일 유효성 검사
ms.author: tracyp
author: MSFTTracyP
manager: laurawi
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 4a05898c-b8e4-4eab-bd70-ee912e349737
ms.collection:
- M365-security-compliance
description: Office 365 조직에서 보낸 메시지의 유효성을 검사 하기 위해 도메인 기반 메시지 인증, 보고 및 적합성 (DMARC)을 구성 하는 방법을 알아봅니다.
ms.openlocfilehash: 9e3c2cd21e411d775f621c8b353bee9e6b0e235e
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/17/2019
ms.locfileid: "34156190"
---
# <a name="use-dmarc-to-validate-email-in-office-365"></a><span data-ttu-id="3d34a-103">DMARC을 사용 하 여 Office 365의 전자 메일 유효성 검사</span><span class="sxs-lookup"><span data-stu-id="3d34a-103">Use DMARC to validate email in Office 365</span></span>

<span data-ttu-id="3d34a-104">도메인 기반 메시지 인증, 보고 및 적합성 ([DMARC](https://dmarc.org))은 SPF (Sender Policy Framework) 및 Dkim (보낸 사람 정책 프레임 워크)을 사용 하 여 메일 보낸 사람을 인증 하 고 대상 전자 메일 시스템에서 보낸 메시지를 신뢰 하는지 확인 합니다. 도메인</span><span class="sxs-lookup"><span data-stu-id="3d34a-104">Domain-based Message Authentication, Reporting, and Conformance ([DMARC](https://dmarc.org)) works with Sender Policy Framework (SPF) and DomainKeys Identified Mail (DKIM) to authenticate mail senders and ensure that destination email systems trust messages sent from your domain.</span></span> <span data-ttu-id="3d34a-105">SPF 및 DKIM을 사용 하 여 DMARC을 구현 하면 스푸핑 및 피싱 전자 메일에 대 한 추가 보호가 제공 됩니다.</span><span class="sxs-lookup"><span data-stu-id="3d34a-105">Implementing DMARC with SPF and DKIM provides additional protection against spoofing and phishing email.</span></span> <span data-ttu-id="3d34a-106">DMARC 메일 시스템 수신에 도움이 됩니다. 도메인에서 전송 된 메시지를 사용 하 여 수행 해야 하는 작업 (SPF 또는 DKIM 검사 실패)을 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d34a-106">DMARC helps receiving mail systems determine what to do with messages sent from your domain that fail SPF or DKIM checks.</span></span>
  
## <a name="how-do-spf-and-dmarc-work-together-to-protect-email-in-office-365"></a><span data-ttu-id="3d34a-107">SPF 및 DMARC이 함께 Office 365의 전자 메일을 보호 하는 방법</span><span class="sxs-lookup"><span data-stu-id="3d34a-107">How do SPF and DMARC work together to protect email in Office 365?</span></span>
<span data-ttu-id="3d34a-108"><a name="SPFandDMARC"> </a></span><span class="sxs-lookup"><span data-stu-id="3d34a-108"></span></span>

 <span data-ttu-id="3d34a-109">전자 메일 메시지에는 보낸 사람 또는 보낸 사람의 주소가 여러 개 포함 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3d34a-109">An email message may contain multiple originator, or sender, addresses.</span></span> <span data-ttu-id="3d34a-110">이러한 주소는 용도가 다른 용도로 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="3d34a-110">These addresses are used for different purposes.</span></span> <span data-ttu-id="3d34a-111">예를 들어 다음 주소를 고려 하십시오.</span><span class="sxs-lookup"><span data-stu-id="3d34a-111">For example, consider these addresses:</span></span> 
  
- <span data-ttu-id="3d34a-112">**"Mail From" 주소**: 보낸 사람을 식별 하 고 배달 못 함 알림과 같이 메시지를 배달 하는 동안 문제가 발생 한 경우 반환 알림을 보낼 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d34a-112">**"Mail From" address**: Identifies the sender and specifies where to send return notices if any problems occur with the delivery of the message, such as non-delivery notices.</span></span> <span data-ttu-id="3d34a-113">전자 메일 메시지의 봉투 부분에 표시 되며 일반적으로 전자 메일 응용 프로그램에서 표시 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3d34a-113">This appears in the envelope portion of an email message and is not usually displayed by your email application.</span></span> <span data-ttu-id="3d34a-114">이를 5321 보낸 사람 주소 또는 역 경로 주소 라고도 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d34a-114">This is sometimes called the 5321.MailFrom address or the reverse-path address.</span></span>
    
- <span data-ttu-id="3d34a-115">**"보낸 사람" 주소**: 메일 응용 프로그램에서 보낸 사람 주소로 표시 되는 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="3d34a-115">**"From" address**: The address displayed as the From address by your mail application.</span></span> <span data-ttu-id="3d34a-116">이 주소는 전자 메일의 작성자를 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d34a-116">This address identifies the author of the email.</span></span> <span data-ttu-id="3d34a-117">즉, 메시지 작성을 담당 하는 사람이 나 시스템의 사서함입니다.</span><span class="sxs-lookup"><span data-stu-id="3d34a-117">That is, the mailbox of the person or system responsible for writing the message.</span></span> <span data-ttu-id="3d34a-118">이를 5322.from 주소의 주소 라고도 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d34a-118">This is sometimes called the 5322.From address.</span></span>
    
<span data-ttu-id="3d34a-119">SPF에서는 DNS TXT 레코드를 사용 하 여 지정 된 도메인에 대해 권한이 부여 된 IP 주소 목록을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d34a-119">SPF uses a DNS TXT record to provide a list of authorized sending IP addresses for a given domain.</span></span> <span data-ttu-id="3d34a-120">일반적으로 SPF 확인은 5321 보낸 사람 주소에 대해서만 수행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="3d34a-120">Normally, SPF checks are only performed against the 5321.MailFrom address.</span></span> <span data-ttu-id="3d34a-121">즉, SPF를 단독으로 사용 하는 경우 5322.from 주소의 주소가 인증 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3d34a-121">This means that the 5322.From address is not authenticated when you use SPF by itself.</span></span> <span data-ttu-id="3d34a-122">이를 통해 사용자가 SPF 확인을 통과 하지만 스푸핑된 5322.from 주소의 보낸 사람 주소를 갖는 메시지를 받을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3d34a-122">This allows for a scenario where a user can receive a message which passes an SPF check but has a spoofed 5322.From sender address.</span></span> <span data-ttu-id="3d34a-123">예를 들어 다음과 같은 SMTP 녹음을 고려해 보십시오.</span><span class="sxs-lookup"><span data-stu-id="3d34a-123">For example, consider this SMTP transcript:</span></span>
  
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

<span data-ttu-id="3d34a-124">이 대화 내용에서 보낸 사람 주소는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="3d34a-124">In this transcript, the sender addresses are as follows:</span></span>
  
- <span data-ttu-id="3d34a-125">메일 보낸 사람 주소 (5321): phish@phishing.contoso.com</span><span class="sxs-lookup"><span data-stu-id="3d34a-125">Mail from address (5321.MailFrom): phish@phishing.contoso.com</span></span>
    
- <span data-ttu-id="3d34a-126">보낸 사람 주소 (5322.from 주소의): security@woodgrovebank.com</span><span class="sxs-lookup"><span data-stu-id="3d34a-126">From address (5322.From): security@woodgrovebank.com</span></span>
    
<span data-ttu-id="3d34a-127">SPF를 구성한 경우 받는 서버는 주소 phish@phishing.contoso.com에서 메일을 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d34a-127">If you configured SPF, then the receiving server performs a check against the Mail from address phish@phishing.contoso.com.</span></span> <span data-ttu-id="3d34a-128">메시지가 phishing.contoso.com 도메인에 대 한 유효한 원본에서 보낸 경우 SPF 확인이 통과 됩니다.</span><span class="sxs-lookup"><span data-stu-id="3d34a-128">If the message came from a valid source for the domain phishing.contoso.com then the SPF check passes.</span></span> <span data-ttu-id="3d34a-129">전자 메일 클라이언트는 보낸 사람 주소만 표시 하기 때문에 사용자는이 메시지를 security@woodgrovebank.com에서 보낸 것을 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3d34a-129">Since the email client only displays the From address, the user sees that this message came from security@woodgrovebank.com.</span></span> <span data-ttu-id="3d34a-130">SPF만을 사용 하는 경우 woodgrovebank.com의 유효성은 인증 되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="3d34a-130">With SPF alone, the validity of woodgrovebank.com was never authenticated.</span></span>
  
<span data-ttu-id="3d34a-131">DMARC을 사용 하는 경우 받는 서버는 보낸 사람 주소에 대해서도 확인을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d34a-131">When you use DMARC, the receiving server also performs a check against the From address.</span></span> <span data-ttu-id="3d34a-132">위 예에서 woodgrovebank.com에 대 한 DMARC TXT 레코드가 있는 경우에는 보낸 사람 주소에 대 한 확인이 실패 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d34a-132">In the example above, if there is a DMARC TXT record in place for woodgrovebank.com, then the check against the From address fails.</span></span>
  
## <a name="what-is-a-dmarc-txt-record"></a><span data-ttu-id="3d34a-133">DMARC TXT 레코드 란?</span><span class="sxs-lookup"><span data-stu-id="3d34a-133">What is a DMARC TXT record?</span></span>
<span data-ttu-id="3d34a-134"><a name="WhatisDMARC"> </a></span><span class="sxs-lookup"><span data-stu-id="3d34a-134"></span></span>

<span data-ttu-id="3d34a-135">SPF의 DNS 레코드와 마찬가지로 DMARC의 레코드는 스푸핑 및 피싱을 방지 하는 데 도움이 되는 DNS 텍스트 (TXT) 레코드입니다.</span><span class="sxs-lookup"><span data-stu-id="3d34a-135">Like the DNS records for SPF, the record for DMARC is a DNS text (TXT) record that helps prevent spoofing and phishing.</span></span> <span data-ttu-id="3d34a-136">DMARC TXT 레코드를 DNS에 게시 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d34a-136">You publish DMARC TXT records in DNS.</span></span> <span data-ttu-id="3d34a-137">DMARC TXT 레코드는 보내는 도메인의와 대조 소유자에 대해 전자 메일 작성자의 IP 주소를 확인 하 여 전자 메일 메시지의 출처를 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d34a-137">DMARC TXT records validate the origin of email messages by verifying the IP address of an email's author against the alleged owner of the sending domain.</span></span> <span data-ttu-id="3d34a-138">DMARC TXT 레코드는 권한 있는 아웃 바운드 전자 메일 서버를 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d34a-138">The DMARC TXT record identifies authorized outbound email servers.</span></span> <span data-ttu-id="3d34a-139">그러면 대상 전자 메일 시스템에서 권한이 부여 된 아웃 바운드 전자 메일 서버 로부터 받는 메시지가 수신 되는지 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3d34a-139">Destination email systems can then verify that messages they receive originate from authorized outbound email servers.</span></span>
  
<span data-ttu-id="3d34a-140">Microsoft의 DMARC TXT 레코드는 다음과 같이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="3d34a-140">Microsoft's DMARC TXT record looks something like this:</span></span>
  
```
_dmarc.microsoft.com.   3600    IN      TXT     "v=DMARC1; p=none; pct=100; rua=mailto:d@rua.agari.com; ruf=mailto:d@ruf.agari.com; fo=1" 
```

<span data-ttu-id="3d34a-141">Microsoft는 DMARC 보고서를 [Agari](https://agari.com), 타사로 보냅니다.</span><span class="sxs-lookup"><span data-stu-id="3d34a-141">Microsoft sends its DMARC reports to [Agari](https://agari.com), a 3rd party.</span></span> <span data-ttu-id="3d34a-142">Agari DMARC 보고서를 수집 하 고 분석 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d34a-142">Agari collects and analyzes DMARC reports.</span></span>
  
## <a name="implement-dmarc-for-inbound-mail"></a><span data-ttu-id="3d34a-143">인바운드 메일용 DMARC 구현</span><span class="sxs-lookup"><span data-stu-id="3d34a-143">Implement DMARC for inbound mail</span></span>
<span data-ttu-id="3d34a-144"><a name="implementDMARCinbound"> </a></span><span class="sxs-lookup"><span data-stu-id="3d34a-144"></span></span>

<span data-ttu-id="3d34a-145">Office 365에서 받은 메일에 대해 DMARC을 설정 하는 작업을 수행할 필요가 없습니다.</span><span class="sxs-lookup"><span data-stu-id="3d34a-145">You don't have to do a thing to set up DMARC for mail that you receive in Office 365.</span></span> <span data-ttu-id="3d34a-146">Microsoft에서는 모든 것을 자동으로 처리 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d34a-146">We've taken care of everything for you.</span></span> <span data-ttu-id="3d34a-147">DMARC 검사를 통과 하지 못한 메일에 대 한 자세한 내용은 [Office 365에서 DMARC에 오류가 발생 한 인바운드 전자 메일을 처리 하는 방법을](use-dmarc-to-validate-email.md#inbounddmarcfail)참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="3d34a-147">If you want to learn what happens to mail that fails to pass our DMARC checks, see [How Office 365 handles inbound email that fails DMARC](use-dmarc-to-validate-email.md#inbounddmarcfail).</span></span>
  
## <a name="implement-dmarc-for-outbound-mail-from-office-365"></a><span data-ttu-id="3d34a-148">Office 365에서 아웃 바운드 메일용 DMARC 구현</span><span class="sxs-lookup"><span data-stu-id="3d34a-148">Implement DMARC for outbound mail from Office 365</span></span>
<span data-ttu-id="3d34a-149"><a name="implementDMARCoutbound"> </a></span><span class="sxs-lookup"><span data-stu-id="3d34a-149"></span></span>

<span data-ttu-id="3d34a-150">Office 365를 사용 하지만 사용자 지정 도메인을 사용 하지 않는 경우, 즉 onmicrosoft.com를 사용 하는 경우에는 조직에 대해 DMARC을 구성 하거나 구현 하기 위해 다른 작업을 수행할 필요가 없습니다.</span><span class="sxs-lookup"><span data-stu-id="3d34a-150">If you use Office 365 but you aren't using a custom domain, that is, you use onmicrosoft.com, you don't need to do anything else to configure or implement DMARC for your organization.</span></span> <span data-ttu-id="3d34a-151">SPF가 이미 설정 되어 있으며 Office 365에서는 보내는 메일에 대해 DKIM 서명을 자동으로 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d34a-151">SPF is already set up for you and Office 365 automatically generates a DKIM signature for your outgoing mail.</span></span> <span data-ttu-id="3d34a-152">이 서명에 대 한 자세한 내용은 [DKIM 및 Office 365에 대 한 기본 동작](use-dkim-to-validate-outbound-email.md#DefaultDKIMbehavior)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="3d34a-152">For more information about this signature, see [Default behavior for DKIM and Office 365](use-dkim-to-validate-outbound-email.md#DefaultDKIMbehavior).</span></span>
  
 <span data-ttu-id="3d34a-153">사용자 지정 도메인이 있거나 Office 365 외에도 온-프레미스 Exchange 서버를 사용 하는 경우 아웃 바운드 메일에 대해 DMARC를 수동으로 구현 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d34a-153">If you have a custom domain or you are using on-premises Exchange servers in addition to Office 365, you need to manually implement DMARC for your outbound mail.</span></span> <span data-ttu-id="3d34a-154">사용자 지정 도메인에 대해 DMARC을 구현 하는 단계는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="3d34a-154">Implementing DMARC for your custom domain includes these steps:</span></span> 
  
- [<span data-ttu-id="3d34a-155">1 단계: 도메인에 대 한 유효한 메일 원본 식별</span><span class="sxs-lookup"><span data-stu-id="3d34a-155">Step 1: Identify valid sources of mail for your domain</span></span>](use-dmarc-to-validate-email.md#IdentifyValidSources)
    
- [<span data-ttu-id="3d34a-156">2 단계: Office 365에서 도메인에 대 한 SPF 설정</span><span class="sxs-lookup"><span data-stu-id="3d34a-156">Step 2: Set up SPF for your domain in Office 365</span></span>](use-dmarc-to-validate-email.md#ConfigSPF)
    
- [<span data-ttu-id="3d34a-157">3 단계: Office 365에서 사용자 지정 도메인에 대 한 DKIM을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d34a-157">Step 3: Set up DKIM for your custom domain in Office 365</span></span>](use-dmarc-to-validate-email.md#ConfigDKIM)
    
- [<span data-ttu-id="3d34a-158">4 단계: Office 365에서 도메인에 대 한 DMARC TXT 레코드를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d34a-158">Step 4: Form the DMARC TXT record for your domain in Office 365</span></span>](use-dmarc-to-validate-email.md#CreateDMARCRecord)
    
### <a name="step-1-identify-valid-sources-of-mail-for-your-domain"></a><span data-ttu-id="3d34a-159">1 단계: 도메인에 대 한 유효한 메일 원본 식별</span><span class="sxs-lookup"><span data-stu-id="3d34a-159">Step 1: Identify valid sources of mail for your domain</span></span>
<span data-ttu-id="3d34a-160"><a name="IdentifyValidSources"> </a></span><span class="sxs-lookup"><span data-stu-id="3d34a-160"></span></span>

<span data-ttu-id="3d34a-161">SPF를 이미 설정한 경우에는이 연습이 이미 진행 된 것입니다.</span><span class="sxs-lookup"><span data-stu-id="3d34a-161">If you have already set up SPF then you have already gone through this exercise.</span></span> <span data-ttu-id="3d34a-162">그러나 DMARC의 경우에는 추가적인 고려 사항이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3d34a-162">However, for DMARC, there are additional considerations.</span></span> <span data-ttu-id="3d34a-163">도메인의 메일 원본을 확인할 때 다음 두 가지 사항을 확인 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d34a-163">When identifying sources of mail for your domain there are two questions you need to answer:</span></span>
  
- <span data-ttu-id="3d34a-164">어떤 IP 주소가 내 도메인에서 메시지를 전송 하나요?</span><span class="sxs-lookup"><span data-stu-id="3d34a-164">What IP addresses send messages from my domain?</span></span>
    
- <span data-ttu-id="3d34a-165">제 3 자가 사용자를 대신 하 여 보낸 메일의 경우 5321 From 및 5322.from 주소의가 일치 합니까?</span><span class="sxs-lookup"><span data-stu-id="3d34a-165">For mail sent from third parties on my behalf, will the 5321.MailFrom and 5322.From domains match?</span></span>
    
### <a name="step-2-set-up-spf-for-your-domain-in-office-365"></a><span data-ttu-id="3d34a-166">2 단계: Office 365에서 도메인에 대 한 SPF 설정</span><span class="sxs-lookup"><span data-stu-id="3d34a-166">Step 2: Set up SPF for your domain in Office 365</span></span>
<span data-ttu-id="3d34a-167"><a name="ConfigSPF"> </a></span><span class="sxs-lookup"><span data-stu-id="3d34a-167"></span></span>

<span data-ttu-id="3d34a-168">이제 유효한 모든 보낸 사람 목록을 만들었으므로 [Office 365에서 SPF를 설정](set-up-spf-in-office-365-to-help-prevent-spoofing.md)하는 단계를 수행 하 여 스푸핑을 방지할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3d34a-168">Now that you have a list of all your valid senders you can follow the steps to [Set up SPF in Office 365 to help prevent spoofing](set-up-spf-in-office-365-to-help-prevent-spoofing.md).</span></span>
  
<span data-ttu-id="3d34a-169">예를 들어 contoso.com가 Exchange Online에서 메일을 보내고 ip 주소가 192.168.0.1 인 온-프레미스 Exchange 서버와 IP 주소가 192.168.100.100 인 웹 응용 프로그램의 경우 SPF TXT 레코드는 다음과 같이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="3d34a-169">For example, assuming contoso.com sends mail from Exchange Online, an on-premises Exchange server whose IP address is 192.168.0.1, and a web application whose IP address is 192.168.100.100, the SPF TXT record would look like this:</span></span>
  
```
contoso.com  IN  TXT  " v=spf1 ip4:192.168.0.1 ip4:192.168.100.100 include:spf.protection.outlook.com -all"
```

<span data-ttu-id="3d34a-170">최상의 방법으로 SPF TXT 레코드가 타사 보낸 사람에 게 고려 되는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d34a-170">As a best practice, ensure that your SPF TXT record takes into account third-party senders.</span></span>
  
### <a name="step-3-set-up-dkim-for-your-custom-domain-in-office-365"></a><span data-ttu-id="3d34a-171">3 단계: Office 365에서 사용자 지정 도메인에 대 한 DKIM을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d34a-171">Step 3: Set up DKIM for your custom domain in Office 365</span></span>
<span data-ttu-id="3d34a-172"><a name="ConfigDKIM"> </a></span><span class="sxs-lookup"><span data-stu-id="3d34a-172"></span></span>

<span data-ttu-id="3d34a-173">SPF를 설정한 후에는 DKIM을 설정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d34a-173">Once you have set up SPF, you need to set up DKIM.</span></span> <span data-ttu-id="3d34a-174">DKIM을 사용 하 여 메시지 헤더에 전자 메일 메시지에 디지털 서명을 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3d34a-174">DKIM lets you add a digital signature to email messages in the message header.</span></span> <span data-ttu-id="3d34a-175">DKIM을 설정 하지 않고 Office 365이 도메인에 기본 DKIM 구성을 사용 하도록 허용 하는 경우 DMARC이 실패할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3d34a-175">If you do not set up DKIM and instead allow Office 365 to use the default DKIM configuration for your domain, DMARC may fail.</span></span> <span data-ttu-id="3d34a-176">이는 기본 DKIM 구성에서 사용자 지정 도메인이 아닌 초기 onmicrosoft.com 도메인을 5322.from 주소의 주소로 사용 하기 때문입니다.</span><span class="sxs-lookup"><span data-stu-id="3d34a-176">This is because the default DKIM configuration uses your initial onmicrosoft.com domain as the 5322.From address, not your custom domain.</span></span> <span data-ttu-id="3d34a-177">이로 인해 도메인에서 보낸 모든 전자 메일의 5321와 5322.from 주소의 간의 불일치가 발생 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d34a-177">This forces a mismatch between the 5321.MailFrom and the 5322.From addresses in all email sent from your domain.</span></span>
  
<span data-ttu-id="3d34a-178">사용자를 대신 하 여 메일을 전송 하는 타사 보낸 사람이 있는 경우 해당 전자 메일에 대해 5321 From 및 5322.from 주소의에서 DMARC가 일치 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3d34a-178">If you have third-party senders that send mail on your behalf and the mail they send has mismatched 5321.MailFrom and 5322.From addresses, DMARC will fail for that email.</span></span> <span data-ttu-id="3d34a-179">이를 방지 하려면 제 3 자 보낸 사람과 특별히 도메인에 대해 DKIM을 설정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d34a-179">To avoid this, you need to set up DKIM for your domain specifically with that third-party sender.</span></span> <span data-ttu-id="3d34a-180">이를 통해 Office 365이 타사 서비스에서 전자 메일을 인증할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3d34a-180">This allows Office 365 to authenticate email from this 3rd-party service.</span></span> <span data-ttu-id="3d34a-181">그러나 Yahoo, Gmail 및 Comcast와 같은 다른 사람도 사용자가 보낸 전자 메일 인 것 처럼 타사에서 보낸 전자 메일을 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3d34a-181">However, it also allows others, for example, Yahoo, Gmail, and Comcast, to verify email sent to them by the third-party as if it was email sent by you.</span></span> <span data-ttu-id="3d34a-182">이렇게 하면 고객이 사서함의 위치에 관계 없이 사용자의 도메인에 대 한 신뢰를 작성할 수 있으며, 마찬가지로 Office 365은 도메인에 대 한 인증 확인을 통과 하므로 위장으로 인해 메시지를 스팸으로 표시 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3d34a-182">This is beneficial because it allows your customers to build trust with your domain no matter where their mailbox is located, and at the same time Office 365 won't mark a message as spam due to spoofing because it passes authentication checks for your domain.</span></span>
  
<span data-ttu-id="3d34a-183">타사에서 도메인을 스푸핑할 수 있도록 DKIM을 설정 하는 방법을 비롯 하 여 도메인에 대 한 DKIM을 설정 하는 방법에 대 한 자세한 내용은 [USE DKIM을 사용 하 여 Office 365의 사용자 지정 도메인에서 보낸 아웃 바운드 전자 메일의 유효성 검사](use-dkim-to-validate-outbound-email.md)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="3d34a-183">For instructions on setting up DKIM for your domain, including how to set up DKIM for third-party senders so they can spoof your domain, see [Use DKIM to validate outbound email sent from your custom domain in Office 365](use-dkim-to-validate-outbound-email.md).</span></span>
  
### <a name="step-4-form-the-dmarc-txt-record-for-your-domain-in-office-365"></a><span data-ttu-id="3d34a-184">4 단계: Office 365에서 도메인에 대 한 DMARC TXT 레코드를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d34a-184">Step 4: Form the DMARC TXT record for your domain in Office 365</span></span>
<span data-ttu-id="3d34a-185"><a name="CreateDMARCRecord"> </a></span><span class="sxs-lookup"><span data-stu-id="3d34a-185"></span></span>

<span data-ttu-id="3d34a-186">여기에 나와 있지 않은 다른 구문 옵션도 있지만 Office 365에서 가장 일반적으로 사용 되는 옵션은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="3d34a-186">Although there are other syntax options that are not mentioned here, these are the most commonly used options for Office 365.</span></span> <span data-ttu-id="3d34a-187">도메인에 대 한 DMARC TXT 레코드를 다음 형식으로 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d34a-187">Form the DMARC TXT record for your domain in the format:</span></span>
  
```
_dmarc.domain  TTL  IN  TXT  "v=DMARC1; pct=100; p=policy"
```

<span data-ttu-id="3d34a-188">여기서 각 부분이 나타내는 의미는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="3d34a-188">where:</span></span>
  
- <span data-ttu-id="3d34a-189">*domain* 은 보호 하려는 도메인입니다.</span><span class="sxs-lookup"><span data-stu-id="3d34a-189">*domain* is the domain you want to protect.</span></span> <span data-ttu-id="3d34a-190">기본적으로 레코드는 도메인과 모든 하위 도메인의 메일을 보호 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d34a-190">By default, the record protects mail from the domain and all subdomains.</span></span> <span data-ttu-id="3d34a-191">예를 들어 dmarc.contoso.com를 지정 \_하는 경우 dmarc은 도메인 및 housewares.contoso.com 또는 plumbing.contoso.com와 같은 모든 하위 도메인과의 메일을 보호 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d34a-191">For example, if you specify \_dmarc.contoso.com, then DMARC protects mail from the domain and all subdomains, such as housewares.contoso.com or plumbing.contoso.com.</span></span> 
    
- <span data-ttu-id="3d34a-192">*TTL* 은 항상 1 시간에 해당 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d34a-192">*TTL* should always be the equivalent of one hour.</span></span> <span data-ttu-id="3d34a-193">TTL에 사용 되는 단위는 시간 (1 시간), 분 (60 분) 또는 초 (3600 초)는 도메인의 등록자에 따라 달라 집니다.</span><span class="sxs-lookup"><span data-stu-id="3d34a-193">The unit used for TTL, either hours (1 hour), minutes (60 minutes), or seconds (3600 seconds), will vary depending on the registrar for your domain.</span></span> 
    
- <span data-ttu-id="3d34a-194">*pct = 100* 은이 규칙을 전자 메일의 100%에 사용 해야 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="3d34a-194">*pct=100* indicates that this rule should be used for 100% of email.</span></span>
    
- <span data-ttu-id="3d34a-195">*정책은* DMARC에 오류가 발생 했을 때 수신 서버가 수행 하도록 할 정책을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d34a-195">*policy* specifies what policy you want the receiving server to follow if DMARC fails.</span></span> <span data-ttu-id="3d34a-196">정책을 없음, 격리 또는 거부로 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3d34a-196">You can set the policy to none, quarantine, or reject.</span></span> 
    
<span data-ttu-id="3d34a-197">사용할 옵션에 대 한 자세한 내용은 [Office 365에서 DMARC을 구현 하기 위한 모범 사례](use-dmarc-to-validate-email.md#DMARCbestpractices)에 대 한 개념을 익힙니다.</span><span class="sxs-lookup"><span data-stu-id="3d34a-197">For information about which options to use, become familiar with the concepts in [Best practices for implementing DMARC in Office 365](use-dmarc-to-validate-email.md#DMARCbestpractices).</span></span>
  
<span data-ttu-id="3d34a-198">예제:</span><span class="sxs-lookup"><span data-stu-id="3d34a-198">Examples:</span></span>
  
- <span data-ttu-id="3d34a-199">정책이 없음으로 설정</span><span class="sxs-lookup"><span data-stu-id="3d34a-199">Policy set to none</span></span>
  
    ```
    _dmarc.contoso.com 3600 IN  TXT  "v=DMARC1; p=none"
    ```

- <span data-ttu-id="3d34a-200">격리로 설정 되는 정책</span><span class="sxs-lookup"><span data-stu-id="3d34a-200">Policy set to quarantine</span></span>
  
    ```
    _dmarc.contoso.com 3600 IN  TXT  "v=DMARC1; p=quarantine"
    ```

- <span data-ttu-id="3d34a-201">거부로 설정 되는 정책</span><span class="sxs-lookup"><span data-stu-id="3d34a-201">Policy set to reject</span></span>
  
    ```
    _dmarc.contoso.com  3600 IN  TXT  "v=DMARC1; p=reject"
    ```

<span data-ttu-id="3d34a-202">레코드를 구성한 후에는 도메인 등록 기관에서 레코드를 업데이트 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d34a-202">Once you have formed your record, you need to update the record at your domain registrar.</span></span> <span data-ttu-id="3d34a-203">DMARC TXT 레코드를 Office 365의 DNS 레코드에 추가 하는 방법에 대 한 자세한 내용은 [dns 레코드를 관리할 때 office 365에 대 한 dns 레코드 만들기](https://support.office.com/article/b0f3fdca-8a80-4e8e-9ef3-61e8a2a9ab23)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="3d34a-203">For instructions on adding the DMARC TXT record to your DNS records for Office 365, see [Create DNS records for Office 365 when you manage your DNS records](https://support.office.com/article/b0f3fdca-8a80-4e8e-9ef3-61e8a2a9ab23).</span></span>
  
## <a name="best-practices-for-implementing-dmarc-in-office-365"></a><span data-ttu-id="3d34a-204">Office 365에서 DMARC을 구현 하기 위한 최상의 방법</span><span class="sxs-lookup"><span data-stu-id="3d34a-204">Best practices for implementing DMARC in Office 365</span></span>
<span data-ttu-id="3d34a-205"><a name="DMARCbestpractices"> </a></span><span class="sxs-lookup"><span data-stu-id="3d34a-205"></span></span>

<span data-ttu-id="3d34a-206">나머지 메일 흐름에 영향을 주지 않고 DMARC을 점차적으로 구현할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3d34a-206">You can implement DMARC gradually without impacting the rest of your mail flow.</span></span> <span data-ttu-id="3d34a-207">다음 단계를 수행 하는 롤아웃 계획을 만들고 구현 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d34a-207">Create and implement a roll out plan that follows these steps.</span></span> <span data-ttu-id="3d34a-208">다음 단계를 진행 하기 전에 먼저 각 단계를 하위 도메인, 다른 하위 도메인, 그리고 마지막으로 조직의 최상위 도메인으로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d34a-208">Do each of these steps first with a sub-domain, then other sub-domains, and finally with the top-level domain in your organization before moving on to the next step.</span></span>
  
1. <span data-ttu-id="3d34a-209">DMARC 구현에 따른 영향 모니터링</span><span class="sxs-lookup"><span data-stu-id="3d34a-209">Monitor the impact of implementing DMARC</span></span>
    
    <span data-ttu-id="3d34a-210">DMARC 수신기에 게 해당 도메인을 사용 하 여 표시 되는 메시지에 대 한 통계를 보내도록 요청 하는 하위 도메인 또는 도메인에 대 한 간단한 모니터링 모드 레코드를 사용 하 여 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d34a-210">Start with a simple monitoring-mode record for a sub-domain or domain that requests that DMARC receivers send you statistics about messages that they see using that domain.</span></span> <span data-ttu-id="3d34a-211">모니터링 모드 레코드는 정책이 없음 (p = 없음)으로 설정 된 DMARC TXT 레코드입니다.</span><span class="sxs-lookup"><span data-stu-id="3d34a-211">A monitoring-mode record is a DMARC TXT record that has its policy set to none (p=none).</span></span> <span data-ttu-id="3d34a-212">많은 회사에서는 보다 제한적인 DMARC 정책을 게시 하 여 손실 될 수 있는 전자 메일의 크기를 확실히 알지 못하기 때문에 DMARC TXT 레코드를 p = 없음으로 게시 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d34a-212">Many companies publish a DMARC TXT record with p=none because they are unsure about how much email they may lose by publishing a more restrictive DMARC policy.</span></span> 
    
    <span data-ttu-id="3d34a-213">메시징 인프라에서 SPF 또는 DKIM을 구현한 후에도이 작업을 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3d34a-213">You can do this even before you've implemented SPF or DKIM in your messaging infrastructure.</span></span> <span data-ttu-id="3d34a-214">그러나 SPF 및 DKIM을 구현 하기 전 까지는 DMARC를 사용 하 여 메일을 효과적으로 격리 하거나 거부할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="3d34a-214">However, you won't be able to effectively quarantine or reject mail by using DMARC until you also implement SPF and DKIM.</span></span> <span data-ttu-id="3d34a-215">SPF 및 DKIM을 도입 하는 경우 DMARC를 통해 생성 된 보고서는 이러한 검사를 통과 하는 메시지의 수와 원본을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d34a-215">As you introduce SPF and DKIM, the reports generated through DMARC will provide the numbers and sources of messages that pass these checks, and those that don't.</span></span> <span data-ttu-id="3d34a-216">합법적인 트래픽의 범위를 쉽게 확인 하 고 처리 하지 못하는 문제를 해결할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3d34a-216">You can easily see how much of your legitimate traffic is or isn't covered by them, and troubleshoot any problems.</span></span> <span data-ttu-id="3d34a-217">또한 보내는 사기 메시지 수 및 해당 위치에서 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d34a-217">You'll also begin to see how many fraudulent messages are being sent, and from where.</span></span>
    
2. <span data-ttu-id="3d34a-218">DMARC에서 실패 한 메일을 외부 메일 시스템에서 격리 하도록 요청</span><span class="sxs-lookup"><span data-stu-id="3d34a-218">Request that external mail systems quarantine mail that fails DMARC</span></span>
    
    <span data-ttu-id="3d34a-219">모든 또는 대부분의 합법적인 트래픽이 SPF 및 DKIM에 의해 보호 되 고 있다고 생각 하 고 DMARC 구현의 영향을 이해 하면 격리 정책을 구현할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3d34a-219">When you believe that all or most of your legitimate traffic is protected by SPF and DKIM, and you understand the impact of implementing DMARC, you can implement a quarantine policy.</span></span> <span data-ttu-id="3d34a-220">격리 정책은 정책이 격리 (p = 격리)로 설정 된 DMARC TXT 레코드입니다.</span><span class="sxs-lookup"><span data-stu-id="3d34a-220">A quarantine policy is a DMARC TXT record that has its policy set to quarantine (p=quarantine).</span></span> <span data-ttu-id="3d34a-221">이 작업을 수행 하는 경우 DMARC 수신기가 DMARC에 오류가 발생 하는 메시지를 고객의 받은 편지함 대신 스팸 폴더의 로컬에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d34a-221">By doing this, you are asking DMARC receivers to put messages from your domain that fail DMARC into the local equivalent of a spam folder instead of your customers' inboxes.</span></span>
    
3. <span data-ttu-id="3d34a-222">DMARC에 실패 한 메시지를 허용 하지 않도록 외부 메일 시스템에 요청</span><span class="sxs-lookup"><span data-stu-id="3d34a-222">Request that external mail systems not accept messages that fail DMARC</span></span>
    
    <span data-ttu-id="3d34a-223">마지막 단계는 거부 정책을 구현 하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="3d34a-223">The final step is implementing a reject policy.</span></span> <span data-ttu-id="3d34a-224">거부 정책은 정책이 거부로 설정 된 (p = 거부) DMARC TXT 레코드입니다.</span><span class="sxs-lookup"><span data-stu-id="3d34a-224">A reject policy is a DMARC TXT record that has its policy set to reject (p=reject).</span></span> <span data-ttu-id="3d34a-225">이 작업을 수행 하면 DMARC 수신자에 게 DMARC 검사를 통과 하지 못한 메시지를 수락 하지 않도록 요청 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d34a-225">When you do this, you're asking DMARC receivers not to accept messages that fail the DMARC checks.</span></span> 
    
## <a name="how-office-365-handles-outbound-email-that-fails-dmarc"></a><span data-ttu-id="3d34a-226">Office 365에서 DMARC에 실패 한 아웃 바운드 전자 메일을 처리 하는 방법</span><span class="sxs-lookup"><span data-stu-id="3d34a-226">How Office 365 handles outbound email that fails DMARC</span></span>
<span data-ttu-id="3d34a-227"><a name="outbounddmarcfail"> </a></span><span class="sxs-lookup"><span data-stu-id="3d34a-227"></span></span>

<span data-ttu-id="3d34a-228">메시지가 Office 365에서 아웃 바운드이 고 DMARC에 오류가 발생 하 여 정책을 p = 격리 또는 p = 거부로 설정한 경우 메시지가 [높은 위험 배달 풀을 통해 아웃 바운드 메시지에 대해](high-risk-delivery-pool-for-outbound-messages.md)라우팅됩니다.</span><span class="sxs-lookup"><span data-stu-id="3d34a-228">If a message is outbound from Office 365 and fails DMARC, and you have set the policy to p=quarantine or p=reject, the message is routed through the [High-risk delivery pool for outbound messages](high-risk-delivery-pool-for-outbound-messages.md).</span></span> <span data-ttu-id="3d34a-229">아웃 바운드 전자 메일에 대 한 재정의는 없습니다.</span><span class="sxs-lookup"><span data-stu-id="3d34a-229">There is no override for outbound email.</span></span>
  
<span data-ttu-id="3d34a-230">DMARC 거부 정책 (p = 거부)을 게시 하는 경우, 메시지는 서비스를 통해 아웃 바운드 메시지를 릴레이할 때 도메인에 대해 SPF 또는 DKIM을 전달할 수 없으므로, Office 365의 다른 고객은 도메인을 스푸핑할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="3d34a-230">If you publish a DMARC reject policy (p=reject), no other customer in Office 365 can spoof your domain because messages will not be able to pass SPF or DKIM for your domain when relaying a message outbound through the service.</span></span> <span data-ttu-id="3d34a-231">그러나 DMARC 거부 정책을 게시 하지만 Office 365을 통해 전자 메일을 모두 인증 하지 않은 경우, 일부 it는 인바운드 전자 메일 (위에 설명한)에 대 한 스팸으로 표시 될 수도 있고, SPF를 게시 하지 않은 경우에는 거부 될 수 있습니다. 서비스입니다.</span><span class="sxs-lookup"><span data-stu-id="3d34a-231">However, if you do publish a DMARC reject policy but don't have all of your email authenticated through Office 365, some of it may be marked as spam for inbound email (as described above), or it will be rejected if you do not publish SPF and try to relay it outbound through the service.</span></span> <span data-ttu-id="3d34a-232">예를 들어 DMARC TXT 레코드를 형성할 때 도메인을 대신 하 여 메일을 보내는 서버 및 응용 프로그램의 일부 IP 주소를 포함 하는 것을 잊은 경우 이러한 상황이 발생 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d34a-232">This happens, for example, if you forget to include some of the IP addresses for servers and apps that send mail on behalf of your domain when you form your DMARC TXT record.</span></span>
  
## <a name="how-office-365-handles-inbound-email-that-fails-dmarc"></a><span data-ttu-id="3d34a-233">Office 365에서 DMARC에 실패 한 인바운드 전자 메일을 처리 하는 방법</span><span class="sxs-lookup"><span data-stu-id="3d34a-233">How Office 365 handles inbound email that fails DMARC</span></span>
<span data-ttu-id="3d34a-234"><a name="inbounddmarcfail"> </a></span><span class="sxs-lookup"><span data-stu-id="3d34a-234"></span></span>

<span data-ttu-id="3d34a-235">보내는 서버의 DMARC 정책이 p = 거부 인 경우 EOP는 메시지를 거부 하는 대신 스팸으로 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d34a-235">If the DMARC policy of the sending server is p=reject, EOP marks the message as spam instead of rejecting it.</span></span> <span data-ttu-id="3d34a-236">즉, 인바운드 전자 메일의 경우 Office 365에서는 p = 거부 및 p = 격리를 동일한 방식으로 처리 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d34a-236">In other words, for inbound email, Office 365 treats p=reject and p=quarantine the same way.</span></span>
  
<span data-ttu-id="3d34a-237">일부 합법적인 전자 메일이 DMARC에 실패할 수 있으므로 Office 365는 이와 같이 구성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="3d34a-237">Office 365 is configured like this because some legitimate email may fail DMARC.</span></span> <span data-ttu-id="3d34a-238">예를 들어 메시지를 메일 그룹으로 보낸 후 모든 목록 참가자로 메시지를 릴레이 하면 DMARC에 오류가 발생할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3d34a-238">For example, a message might fail DMARC if it is sent to a mailing list that then relays the message to all list participants.</span></span> <span data-ttu-id="3d34a-239">Office 365에서 이러한 메시지를 거부 한 경우 사용자는 합법적인 전자 메일을 잃어 버릴 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="3d34a-239">If Office 365 rejected these messages, people could lose legitimate email and have no way to retrieve it.</span></span> <span data-ttu-id="3d34a-240">대신, 이러한 메시지는 계속 해 서 DMARC에 실패 하지만, 거부 되지 않고 스팸으로 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="3d34a-240">Instead, these messages will still fail DMARC but they will be marked as spam and not rejected.</span></span> <span data-ttu-id="3d34a-241">원하는 경우 사용자는 다음 방법을 통해 받은 편지함에 이러한 메시지를 받을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3d34a-241">If desired, users can still get these messages in their inbox through these methods:</span></span>
  
- <span data-ttu-id="3d34a-242">사용자가 전자 메일 클라이언트를 사용 하 여 개별적으로 수신 허용-보낸 사람 추가</span><span class="sxs-lookup"><span data-stu-id="3d34a-242">Users add safe senders individually by using their email client</span></span>
    
- <span data-ttu-id="3d34a-243">관리자는 특정 보낸 사람에 대 한 메시지를 허용 하는 모든 사용자에 대해 Exchange 메일 흐름 규칙 (전송 규칙이 라고도 함)을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3d34a-243">Administrators create an Exchange mail flow rule (also known as a transport rule) for all users that allows messages for those particular senders.</span></span> 
    
## <a name="troubleshooting-your-dmarc-implementation"></a><span data-ttu-id="3d34a-244">DMARC 구현 문제 해결</span><span class="sxs-lookup"><span data-stu-id="3d34a-244">Troubleshooting your DMARC implementation</span></span>
<span data-ttu-id="3d34a-245"><a name="dmarctroubleshoot"> </a></span><span class="sxs-lookup"><span data-stu-id="3d34a-245"></span></span>

<span data-ttu-id="3d34a-246">EOP가 첫 번째 항목이 아닌 경우 도메인의 MX 레코드를 구성한 경우 DMARC 오류가 도메인에 적용 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3d34a-246">If you have configured your domain's MX records where EOP is not the first entry, DMARC failures will not be enforced for your domain.</span></span> 
  
<span data-ttu-id="3d34a-247">사용자가 Office 365 고객이 고 도메인의 기본 MX 레코드가 EOP를 가리키지 않는 경우 DMARC의 이점을 얻을 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="3d34a-247">If you're an Office 365 customer, and your domain's primary MX record does not point to EOP, you will not get the benefits of DMARC.</span></span> <span data-ttu-id="3d34a-248">예를 들어 MX 레코드를 온-프레미스 메일 서버에 DMARC 다음 커넥터를 사용 하 여 EOP에 전자 메일을 라우팅하는 경우에는 작동 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3d34a-248">For example, DMARC won't work if you point the MX record to your on-premises mail server and then route email to EOP by using a connector.</span></span> <span data-ttu-id="3d34a-249">이 시나리오에서 받는 도메인은 허용 도메인 중 하나이 고 EOP는 기본 MX가 아닙니다.</span><span class="sxs-lookup"><span data-stu-id="3d34a-249">In this scenario, the receiving domain is one of your Accepted-Domains but EOP is not the primary MX.</span></span> <span data-ttu-id="3d34a-250">예를 들어 contoso.com에서 자체 MX를 가리키고 EOP를 보조 MX 레코드로 사용 한다고 가정해 보겠습니다.</span><span class="sxs-lookup"><span data-stu-id="3d34a-250">For example, suppose contoso.com points its MX at itself and uses EOP as a secondary MX record, contoso.com's MX record looks like the following:</span></span>
  
```
contoso.com     3600   IN  MX  0  mail.contoso.com
contoso.com     3600   IN  MX  10 contoso-com.mail.protection.outlook.com
```

<span data-ttu-id="3d34a-251">전체 또는 대부분의 전자 메일은 기본 MX 이기 때문에 먼저 mail.contoso.com로 라우팅되고, 메일은 EOP로 라우팅됩니다.</span><span class="sxs-lookup"><span data-stu-id="3d34a-251">All, or most, email will first be routed to mail.contoso.com since it's the primary MX, and then mail will get routed to EOP.</span></span> <span data-ttu-id="3d34a-252">어떤 경우에는 EOP를 MX 레코드로 나열 하지 않고 단순히 커넥터를 연결 하 여 전자 메일을 라우팅하도록 할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3d34a-252">In some cases, you might not even list EOP as an MX record at all and simply hook up connectors to route your email.</span></span> <span data-ttu-id="3d34a-253">EOP는 DMARC 유효성 검사를 수행 하기 위해 첫 번째 항목 일 필요는 없습니다.</span><span class="sxs-lookup"><span data-stu-id="3d34a-253">EOP does not have to be the first entry for DMARC validation to be done.</span></span> <span data-ttu-id="3d34a-254">모든 온-프레미스/비 O365 서버가 DMARC 검사를 수행 하는 것은 확실 하지 않으므로 유효성 검사를 확인 하기만 하면 됩니다.</span><span class="sxs-lookup"><span data-stu-id="3d34a-254">It just ensures the validation, as we cannot be certain that all on-premise/non-O365 servers will do DMARC checks.</span></span>  <span data-ttu-id="3d34a-255">DMARC는 DMARC TXT 레코드를 설정할 때 고객의 도메인 (서버 아님)에 적용할 수 있지만 실제로 적용을 수행 하기 위해 받는 서버로 작동 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d34a-255">DMARC is eligible to be enforced for a customer’s domain (not server) when you set up the DMARC TXT record, but it is up to the receiving server to actually do the enforcement.</span></span>  <span data-ttu-id="3d34a-256">EOP을 받는 서버로 설정 하는 경우 EOP는 DMARC 적용을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d34a-256">If you set up EOP as the receiving server, then EOP does the DMARC enforcement.</span></span>
  
## <a name="for-more-information"></a><span data-ttu-id="3d34a-257">자세한 내용</span><span class="sxs-lookup"><span data-stu-id="3d34a-257">For more information</span></span>
<span data-ttu-id="3d34a-258"><a name="sectionSection8"> </a></span><span class="sxs-lookup"><span data-stu-id="3d34a-258"></span></span>

<span data-ttu-id="3d34a-259">DMARC에 대 한 자세한 정보를 원하십니까?</span><span class="sxs-lookup"><span data-stu-id="3d34a-259">Want more information about DMARC?</span></span> <span data-ttu-id="3d34a-260">이러한 리소스를 통해 도움이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3d34a-260">These resources can help.</span></span>
  
- <span data-ttu-id="3d34a-261">[스팸 방지 메시지 헤더](anti-spam-message-headers.md) 에는 DMARC 검사를 위해 Office 365에서 사용 하는 구문 및 헤더 필드가 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3d34a-261">[Anti-spam message headers](anti-spam-message-headers.md) includes the syntax and header fields used by Office 365 for DMARC checks.</span></span> 
    
- <span data-ttu-id="3d34a-262">M <sup>3</sup>aawg (메시징, 맬웨어, 모바일 남용 작업 그룹)에서 [DMARC 교육 시리즈](https://www.m3aawg.org/activities/training/dmarc-training-series) 를 이용 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d34a-262">Take the [DMARC Training Series](https://www.m3aawg.org/activities/training/dmarc-training-series) from M <sup>3</sup>AAWG (Messaging, Malware, Mobile Anti-Abuse Working Group).</span></span>
    
- <span data-ttu-id="3d34a-263">[Dmarcian](https://space.dmarcian.com/deployment/)에서 검사 목록을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d34a-263">Use the checklist at [dmarcian](https://space.dmarcian.com/deployment/).</span></span>
    
- <span data-ttu-id="3d34a-264">[DMARC.org](https://dmarc.org)에서 원본으로 직접 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d34a-264">Go directly to the source at [DMARC.org](https://dmarc.org).</span></span>
    
## <a name="see-also"></a><span data-ttu-id="3d34a-265">참고 항목</span><span class="sxs-lookup"><span data-stu-id="3d34a-265">See also</span></span>
<span data-ttu-id="3d34a-266"><a name="sectionSection8"> </a></span><span class="sxs-lookup"><span data-stu-id="3d34a-266"></span></span>

[<span data-ttu-id="3d34a-267">Office 365에서 SPF (Sender Policy Framework)를 사용 하 여 스푸핑을 방지 하는 방법</span><span class="sxs-lookup"><span data-stu-id="3d34a-267">How Office 365 uses Sender Policy Framework (SPF) to prevent spoofing</span></span>](how-office-365-uses-spf-to-prevent-spoofing.md)
  
[<span data-ttu-id="3d34a-268">스푸핑을 방지할 수 있도록 Office 365에서 SPF 설정</span><span class="sxs-lookup"><span data-stu-id="3d34a-268">Set up SPF in Office 365 to help prevent spoofing</span></span>](set-up-spf-in-office-365-to-help-prevent-spoofing.md)
  
[<span data-ttu-id="3d34a-269">DKIM을 사용 하 여 Office 365의 사용자 지정 도메인에서 전송 되는 아웃 바운드 전자 메일의 유효성 검사</span><span class="sxs-lookup"><span data-stu-id="3d34a-269">Use DKIM to validate outbound email sent from your custom domain in Office 365</span></span>](use-dkim-to-validate-outbound-email.md)

