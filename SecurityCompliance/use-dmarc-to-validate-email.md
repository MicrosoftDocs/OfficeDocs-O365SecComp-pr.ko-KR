---
title: DMARC를 사용 하 여 Office 365의 전자 메일의 유효성을 검사 하려면
ms.author: krowley
author: kccross
manager: laurawi
ms.date: ''
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.custom: TN2DMC
ms.assetid: 4a05898c-b8e4-4eab-bd70-ee912e349737
description: Office 365 조직에서 보낸 메시지의 유효성을 검사 하 여 도메인 기반 메시지 인증, 보고 및 적합성 (DMARC)를 구성 하는 방법에 알아봅니다.
ms.openlocfilehash: 2f8e712028b5b5ee8950b48780083a20c7dce6ab
ms.sourcegitcommit: bd1762ccf63c7d2ad8b49a936115171c72fb2c0f
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/08/2019
ms.locfileid: "27750047"
---
# <a name="use-dmarc-to-validate-email-in-office-365"></a><span data-ttu-id="84968-103">DMARC를 사용 하 여 Office 365의 전자 메일의 유효성을 검사 하려면</span><span class="sxs-lookup"><span data-stu-id="84968-103">Use DMARC to validate email in Office 365</span></span>

<span data-ttu-id="84968-p101">보낸 사람이 정책 프레임 워크 (SPF) 및 DomainKeys 식별 된 메일 (DKIM) 메일 보낸사람을 인증 하 고 대상 전자 메일 시스템에서 보낸 메시지를 신뢰 확인을 사용 하 여 도메인 기반 메시지 인증, 보고 및 적합성 ([DMARC](https://dmarc.org)) 작동 하는 도메인입니다. SPF 및 DKIM DMARC 구현 스푸핑 및 피싱 전자 메일에 대 한 추가 보호를 제공 합니다. 받는 메일 시스템 메시지와 함께 수행할 작업을 결정 하는 DMARC 도움이 실패 SPF 또는 DKIM 확인 하 여 도메인에서 보낸 합니다.</span><span class="sxs-lookup"><span data-stu-id="84968-p101">Domain-based Message Authentication, Reporting, and Conformance ([DMARC](https://dmarc.org)) works with Sender Policy Framework (SPF) and DomainKeys Identified Mail (DKIM) to authenticate mail senders and ensure that destination email systems trust messages sent from your domain. Implementing DMARC with SPF and DKIM provides additional protection against spoofing and phishing email. DMARC helps receiving mail systems determine what to do with messages sent from your domain that fail SPF or DKIM checks.</span></span>
  
## <a name="how-do-spf-and-dmarc-work-together-to-protect-email-in-office-365"></a><span data-ttu-id="84968-107">SPF 및 DMARC 작동 방법 함께 Office 365의 전자 메일을 보호 하기 위해</span><span class="sxs-lookup"><span data-stu-id="84968-107">How do SPF and DMARC work together to protect email in Office 365?</span></span>
<span data-ttu-id="84968-108"><a name="SPFandDMARC"> </a></span><span class="sxs-lookup"><span data-stu-id="84968-108"></span></span>

 <span data-ttu-id="84968-p102">전자 메일 메시지는 여러 송신자 또는 보낸사람 주소를 포함할 수 있습니다. 이 주소는 서로 다른 용도로 사용 됩니다. 이러한 주소 예로 들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="84968-p102">An email message may contain multiple originator, or sender, addresses. These addresses are used for different purposes. For example, consider these addresses:</span></span> 
  
- <span data-ttu-id="84968-p103">**"Mail From" 주소**: 보낸 사람을 식별 하 고 배달 못함 정보와 같은 메시지의 배달에 모든 문제가 발생 하는 경우 반환 알림을 보낼 위치를 지정 합니다. 이 전자 메일 메시지의 봉투 부분에 표시 되며 일반적으로 전자 메일 응용 프로그램에 의해 표시 되지 않습니다. 이 5321.MailFrom 주소 또는 역방향 경로 주소 라고도 합니다.</span><span class="sxs-lookup"><span data-stu-id="84968-p103">**"Mail From" address**: Identifies the sender and specifies where to send return notices if any problems occur with the delivery of the message, such as non-delivery notices. This appears in the envelope portion of an email message and is not usually displayed by your email application. This is sometimes called the 5321.MailFrom address or the reverse-path address.</span></span>
    
- <span data-ttu-id="84968-p104">**"From" 주소**: 전자 메일 응용 프로그램으로 From 주소로 표시 되는 주소입니다. 이 주소는 전자 메일의 작성자를 식별 합니다. 즉, 사용자 또는 메시지를 작성 하는 일을 담당 하는 시스템의 사서함입니다. 이 방법을 5322.From 주소를 라고도 합니다.</span><span class="sxs-lookup"><span data-stu-id="84968-p104">**"From" address**: The address displayed as the From address by your mail application. This address identifies the author of the email. That is, the mailbox of the person or system responsible for writing the message. This is sometimes called the 5322.From address.</span></span>
    
<span data-ttu-id="84968-p105">SPF는 DNS TXT 레코드를 사용 하 여 지정된 된 도메인에 대 한 권한이 부여 된 보내는 IP 주소 목록을 제공 합니다. 일반적으로 SPF 확인 5321.MailFrom 주소에 대해서만 수행 됩니다. 이 5322.From 주소는 인증 되지 않은 SPF를 사용 하는 경우 단독으로 것을 의미 합니다. 이 사용자 위장 된 5322.From 보낸사람 주소를 되었지만 SPF 검사를 통과 하는 메시지를 받을 수 있는 시나리오에 대 한 수 있습니다. 이 SMTP 대화 내용이 예로 들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="84968-p105">SPF uses a DNS TXT record to provide a list of authorized sending IP addresses for a given domain. Normally, SPF checks are only performed against the 5321.MailFrom address. This means that the 5322.From address is not authenticated when you use SPF by itself. This allows for a scenario where a user can receive a message which passes an SPF check but has a spoofed 5322.From sender address. For example, consider this SMTP transcript:</span></span>
  
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

<span data-ttu-id="84968-124">이 대화 내용이에서 보낸사람 주소는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="84968-124">In this transcript, the sender addresses are as follows:</span></span>
  
- <span data-ttu-id="84968-125">메일 주소 (5321.MailFrom): phish@phishing.contoso.com</span><span class="sxs-lookup"><span data-stu-id="84968-125">Mail from address (5321.MailFrom): phish@phishing.contoso.com</span></span>
    
- <span data-ttu-id="84968-126">보낸사람 주소 (5322.From): security@woodgrovebank.com</span><span class="sxs-lookup"><span data-stu-id="84968-126">From address (5322.From): security@woodgrovebank.com</span></span>
    
<span data-ttu-id="84968-p106">SPF를 구성 해 놓은 받는 서버에서 주소 phish@phishing.contoso.com 메일에 대해 확인을 수행 합니다. 도메인 phishing.contoso.com에 대 한 유효한 소스에서 메시지를 받은 경우 SPF 확인 전달 합니다. 전자 메일 클라이언트 보낸사람 주소를 표시 하므로 사용자에 게 security@woodgrovebank.com에서이 메시지 인지 표시 합니다. SPF 만으로는, woodgrovebank.com의 유효성을 검사 인증 되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="84968-p106">If you configured SPF, then the receiving server performs a check against the Mail from address phish@phishing.contoso.com. If the message came from a valid source for the domain phishing.contoso.com then the SPF check passes. Since the email client only displays the From address, the user sees that this message came from security@woodgrovebank.com. With SPF alone, the validity of woodgrovebank.com was never authenticated.</span></span>
  
<span data-ttu-id="84968-p107">DMARC를 사용 하면 수신 서버는 또한 보낸사람 주소에 대 한 검사를 수행 합니다. 위의 예제에서 woodgrovebank.com에 대 한 전체에 DMARC TXT 레코드 있으면 확인 보낸사람 주소에 대해이 실패 합니다.</span><span class="sxs-lookup"><span data-stu-id="84968-p107">When you use DMARC, the receiving server also performs a check against the From address. In the example above, if there is a DMARC TXT record in place for woodgrovebank.com, then the check against the From address fails.</span></span>
  
## <a name="what-is-a-dmarc-txt-record"></a><span data-ttu-id="84968-133">DMARC TXT 레코드 이란?</span><span class="sxs-lookup"><span data-stu-id="84968-133">What is a DMARC TXT record?</span></span>
<span data-ttu-id="84968-134"><a name="WhatisDMARC"> </a></span><span class="sxs-lookup"><span data-stu-id="84968-134"></span></span>

<span data-ttu-id="84968-p108">SPF에 대 한 DNS 레코드를 다음과 같이 DMARC에 대 한 레코드는 스푸핑 및 피싱 방지 하는 DNS 텍스트 (TXT) 레코드가입니다. DNS에 DMARC TXT 레코드를 게시 합니다. DMARC TXT 레코드 보내는 도메인의 공식된 소유자에 대 한 전자 메일의 작성자의 IP 주소를 확인 하 여 전자 메일 메시지의 출처의 유효성을 검사 합니다. DMARC TXT 레코드 권한이 부여 된 아웃 바운드 전자 메일 서버를 식별합니다. 대상 전자 메일 시스템 받은 메시지 권한이 부여 된 아웃 바운드 전자 메일 서버에서 시작 되었는지 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="84968-p108">Like the DNS records for SPF, the record for DMARC is a DNS text (TXT) record that helps prevent spoofing and phishing. You publish DMARC TXT records in DNS. DMARC TXT records validate the origin of email messages by verifying the IP address of an email's author against the alleged owner of the sending domain. The DMARC TXT record identifies authorized outbound email servers. Destination email systems can then verify that messages they receive originate from authorized outbound email servers.</span></span>
  
<span data-ttu-id="84968-140">Microsoft의 DMARC TXT 레코드는 다음과 유사 합니다.</span><span class="sxs-lookup"><span data-stu-id="84968-140">Microsoft's DMARC TXT record looks something like this:</span></span>
  
```
_dmarc.microsoft.com.   3600    IN      TXT     "v=DMARC1; p=none; pct=100; rua=mailto:d@rua.agari.com; ruf=mailto:d@ruf.agari.com; fo=1" 
```

<span data-ttu-id="84968-p109">Microsoft 보냅니다 해당 DMARC [Agari](https://agari.com)를 보고, 타사의 합니다. Agari를 수집 하 고 DMARC 보고서를 분석 합니다.</span><span class="sxs-lookup"><span data-stu-id="84968-p109">Microsoft sends its DMARC reports to [Agari](https://agari.com), a 3rd party. Agari collects and analyzes DMARC reports.</span></span>
  
## <a name="implement-dmarc-for-inbound-mail"></a><span data-ttu-id="84968-143">인바운드 메일에 대 한 DMARC 구현</span><span class="sxs-lookup"><span data-stu-id="84968-143">Implement DMARC for inbound mail</span></span>
<span data-ttu-id="84968-144"><a name="implementDMARCinbound"> </a></span><span class="sxs-lookup"><span data-stu-id="84968-144"></span></span>

<span data-ttu-id="84968-p110">Office 365에서 수신 하는 메일에 대 한 DMARC를 설정 하는 작업을 수행 필요가 없습니다. 우리 했을 때 주의 하지 않아도의 모든 있습니다. 싶으십니까 하는 메일을 수행 하는 작업 못해도 사용해 DMARC 검사를 통과 [인바운드 전자 메일 DMARC에 실패 하는 Office 365 어떻게 핸들](use-dmarc-to-validate-email.md#inbounddmarcfail)을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="84968-p110">You don't have to do a thing to set up DMARC for mail that you receive in Office 365. We've taken care of everything for you. If you want to learn what happens to mail that fails to pass our DMARC checks, see [How Office 365 handles inbound email that fails DMARC](use-dmarc-to-validate-email.md#inbounddmarcfail).</span></span>
  
## <a name="implement-dmarc-for-outbound-mail-from-office-365"></a><span data-ttu-id="84968-148">Office 365에서 아웃 바운드 메일에 대 한 DMARC를 구현 합니다.</span><span class="sxs-lookup"><span data-stu-id="84968-148">Implement DMARC for outbound mail from Office 365</span></span>
<span data-ttu-id="84968-149"><a name="implementDMARCoutbound"> </a></span><span class="sxs-lookup"><span data-stu-id="84968-149"></span></span>

<span data-ttu-id="84968-p111">즉, Office 365를 사용 하는 경우 사용자 지정 도메인을 사용 하지 않는 onmicrosoft.com를 사용 하 여, 구성 또는 조직에 대 한 DMARC를 구현 하는 다른 작업을 수행할 필요가 없습니다. 하면 SPF 이미 설정 하 고 Office 365에 보내는 메일에 대 한 DKIM 서명을 자동으로 생성 합니다. 이 서명 하는 방법에 대 한 자세한 내용은 [DKIM 및 Office 365의 기본 동작을](use-dkim-to-validate-outbound-email.md#DefaultDKIMbehavior)참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="84968-p111">If you use Office 365 but you aren't using a custom domain, that is, you use onmicrosoft.com, you don't need to do anything else to configure or implement DMARC for your organization. SPF is already set up for you and Office 365 automatically generates a DKIM signature for your outgoing mail. For more information about this signature, see [Default behavior for DKIM and Office 365](use-dkim-to-validate-outbound-email.md#DefaultDKIMbehavior).</span></span>
  
 <span data-ttu-id="84968-p112">사용자 지정 도메인 했거나 Office 365 외에도 온-프레미스 Exchange 서버를 사용 하는 경우에 수동으로 아웃 바운드 메일에 대 한 DMARC를 구현 해야 합니다. 사용자 지정 도메인에 대 한 DMARC 구현 다음이 단계에 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="84968-p112">If you have a custom domain or you are using on-premises Exchange servers in addition to Office 365, you need to manually implement DMARC for your outbound mail. Implementing DMARC for your custom domain includes these steps:</span></span> 
  
- [<span data-ttu-id="84968-155">1 단계: 도메인에 대 한 메일의 유효한 소스를 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="84968-155">Step 1: Identify valid sources of mail for your domain</span></span>](use-dmarc-to-validate-email.md#IdentifyValidSources)
    
- [<span data-ttu-id="84968-156">2 단계: Office 365에서 도메인에 대 한 SPF를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="84968-156">Step 2: Set up SPF for your domain in Office 365</span></span>](use-dmarc-to-validate-email.md#ConfigSPF)
    
- [<span data-ttu-id="84968-157">3 단계: Office 365에서 사용자 지정 도메인에 대 한 DKIM를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="84968-157">Step 3: Set up DKIM for your custom domain in Office 365</span></span>](use-dmarc-to-validate-email.md#ConfigDKIM)
    
- [<span data-ttu-id="84968-158">Office 365에서 도메인에 대 한 DMARC TXT 레코드를 형성 하는 4 단계:</span><span class="sxs-lookup"><span data-stu-id="84968-158">Step 4: Form the DMARC TXT record for your domain in Office 365</span></span>](use-dmarc-to-validate-email.md#CreateDMARCRecord)
    
### <a name="step-1-identify-valid-sources-of-mail-for-your-domain"></a><span data-ttu-id="84968-159">1 단계: 도메인에 대 한 메일의 유효한 소스를 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="84968-159">Step 1: Identify valid sources of mail for your domain</span></span>
<span data-ttu-id="84968-160"><a name="IdentifyValidSources"> </a></span><span class="sxs-lookup"><span data-stu-id="84968-160"></span></span>

<span data-ttu-id="84968-p113">SPF 이미 설정 하는 경우 다음 하면가 이미 모음은이 연습을 통해 돌아갑니다. 그러나 DMARC에 대 한 가지 추가 고려 사항입니다. 도메인에 대 한 메일의 출처를 식별 하는 경우 두 질문에 답해야 합니다 가지가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="84968-p113">If you have already set up SPF then you have already gone through this exercise. However, for DMARC, there are additional considerations. When identifying sources of mail for your domain there are two questions you need to answer:</span></span>
  
- <span data-ttu-id="84968-164">어떤 IP 주소 내 도메인에서 메시지를 보낼?</span><span class="sxs-lookup"><span data-stu-id="84968-164">What IP addresses send messages from my domain?</span></span>
    
- <span data-ttu-id="84968-165">내를 대신 하 여 제 3 자에서 보낸 메일에 대 한 5321.MailFrom 및 5322.From 도메인 일치시킬지 여부</span><span class="sxs-lookup"><span data-stu-id="84968-165">For mail sent from third parties on my behalf, will the 5321.MailFrom and 5322.From domains match?</span></span>
    
### <a name="step-2-set-up-spf-for-your-domain-in-office-365"></a><span data-ttu-id="84968-166">2 단계: Office 365에서 도메인에 대 한 SPF를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="84968-166">Step 2: Set up SPF for your domain in Office 365</span></span>
<span data-ttu-id="84968-167"><a name="ConfigSPF"> </a></span><span class="sxs-lookup"><span data-stu-id="84968-167"></span></span>

<span data-ttu-id="84968-168">유효한 모든 보낸 사람의 목록이 만들었으므로 [스푸핑을 방지 하기 위해 Office 365에서 SPF를 설정](set-up-spf-in-office-365-to-help-prevent-spoofing.md)하려면 단계를 따라 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="84968-168">Now that you have a list of all your valid senders you can follow the steps to [Set up SPF in Office 365 to help prevent spoofing](set-up-spf-in-office-365-to-help-prevent-spoofing.md).</span></span>
  
<span data-ttu-id="84968-169">예: contoso.com Exchange Online에서 해당 IP 주소 192.168.0.1, 및 해당 IP 주소는 192.168.100.100, 웹 응용 프로그램은 온-프레미스 Exchange 서버에서 메일을 보내는 것으로 가정 SPF TXT 레코드는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="84968-169">For example, assuming contoso.com sends mail from Exchange Online, an on-premises Exchange server whose IP address is 192.168.0.1, and a web application whose IP address is 192.168.100.100, the SPF TXT record would look like this:</span></span>
  
```
contoso.com  IN  TXT  " v=spf1 ip4:192.168.0.1 ip4:192.168.100.100 include:spf.protection.outlook.com -all"
```

<span data-ttu-id="84968-170">최상의 방법으로는 SPF TXT 레코드 수식의 계산 시간이 계정 제 3 자 보낸사람으로를 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="84968-170">As a best practice, ensure that your SPF TXT record takes into account third-party senders.</span></span>
  
### <a name="step-3-set-up-dkim-for-your-custom-domain-in-office-365"></a><span data-ttu-id="84968-171">3 단계: Office 365에서 사용자 지정 도메인에 대 한 DKIM를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="84968-171">Step 3: Set up DKIM for your custom domain in Office 365</span></span>
<span data-ttu-id="84968-172"><a name="ConfigDKIM"> </a></span><span class="sxs-lookup"><span data-stu-id="84968-172"></span></span>

<span data-ttu-id="84968-p114">SPF 설정한 후에 DKIM를 설정 해야 합니다. DKIM은 메시지 헤더에 전자 메일 메시지에 디지털 서명을 추가할 수 있습니다. DKIM를 설정 하지 않으며 대신 도메인에 대 한 기본 DKIM 구성을 사용 하 여 Office 365를 허용 하는 경우에 DMARC 실패할 수 있습니다. 기본 DKIM 구성 초기 onmicrosoft.com 도메인을 사용 하 여 사용자 지정 도메인 하지 5322.From 주소로 때문입니다. 이렇게 하면는 5321.MailFrom 도메인에서 보낸 모든 전자 메일의 5322.From 주소와 일치 하지 됩니다.</span><span class="sxs-lookup"><span data-stu-id="84968-p114">Once you have set up SPF, you need to set up DKIM. DKIM lets you add a digital signature to email messages in the message header. If you do not set up DKIM and instead allow Office 365 to use the default DKIM configuration for your domain, DMARC may fail. This is because the default DKIM configuration uses your initial onmicrosoft.com domain as the 5322.From address, not your custom domain. This forces a mismatch between the 5321.MailFrom and the 5322.From addresses in all email sent from your domain.</span></span>
  
<span data-ttu-id="84968-p115">사용자를 대신 하 여 메일을 보낼 있는 제 3 자가 발신자 있고 대리인이 보내는 메일에 짝이 맞지 않는 5321.MailFrom와 5322.From 주소 하는 경우 해당 전자 메일에 대 한 DMARC 실패 합니다. 이 문제를 방지 하려면 해당 제 3 자가 발신자 구체적으로 사용 하 여 도메인에 대 한 DKIM를 설정 해야 합니다. 따라서이 타사 서비스에서 전자 메일을 인증 하는 Office 365 수 있습니다. 그러나 수도 있습니다 다른 등 yahoo!, Gmail, 및 Comcast, 사용자가 보낸 전자 메일 되었으면 처럼 제 3 자에 의해 자신에 게 보낸 전자 메일을 확인 합니다. 이것은 해당 사서함이 있는 위치에 관계 없이 도메인 신뢰 관계를 구축 하 여 고객을 허용 하기 때문에 유용 하 고 동시에 Office 365 되지 않음 표시 메시지를 도메인에 대 한 인증 검사를 통과 하기 때문에 스푸핑 때문에 스팸으로 합니다.</span><span class="sxs-lookup"><span data-stu-id="84968-p115">If you have third-party senders that send mail on your behalf and the mail they send has mismatched 5321.MailFrom and 5322.From addresses, DMARC will fail for that email. To avoid this, you need to set up DKIM for your domain specifically with that third-party sender. This allows Office 365 to authenticate email from this 3rd-party service. However, it also allows others, for example, Yahoo, Gmail, and Comcast, to verify email sent to them by the third-party as if it was email sent by you. This is beneficial because it allows your customers to build trust with your domain no matter where their mailbox is located, and at the same time Office 365 won't mark a message as spam due to spoofing because it passes authentication checks for your domain.</span></span>
  
<span data-ttu-id="84968-183">사용자 도메인을 스푸핑할 수 있도록 제 3 자 보낸사람에 대 한 DKIM를 설정 하는 방법을 비롯 하 여 도메인에 대 한 DKIM 설정에 대 한 지침은 [Office 365에서 사용자 지정 도메인에서 보낸 아웃 바운드 전자 메일의 유효성을 검사를 사용 하 여 DKIM](use-dkim-to-validate-outbound-email.md)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="84968-183">For instructions on setting up DKIM for your domain, including how to set up DKIM for third-party senders so they can spoof your domain, see [Use DKIM to validate outbound email sent from your custom domain in Office 365](use-dkim-to-validate-outbound-email.md).</span></span>
  
### <a name="step-4-form-the-dmarc-txt-record-for-your-domain-in-office-365"></a><span data-ttu-id="84968-184">Office 365에서 도메인에 대 한 DMARC TXT 레코드를 형성 하는 4 단계:</span><span class="sxs-lookup"><span data-stu-id="84968-184">Step 4: Form the DMARC TXT record for your domain in Office 365</span></span>
<span data-ttu-id="84968-185"><a name="CreateDMARCRecord"> </a></span><span class="sxs-lookup"><span data-stu-id="84968-185"></span></span>

<span data-ttu-id="84968-p116">여기서 언급 되지 않은 다른 구문을 옵션 되지만, 다음은 Office 365에 대 한 가장 일반적으로 사용 되는 옵션입니다. 양식 형식으로 도메인에 대 한 DMARC TXT 레코드:</span><span class="sxs-lookup"><span data-stu-id="84968-p116">Although there are other syntax options that are not mentioned here, these are the most commonly used options for Office 365. Form the DMARC TXT record for your domain in the format:</span></span>
  
```
_dmarc.domain  TTL  IN  TXT  "v=DMARC1; pct=100; p=policy"
```

<span data-ttu-id="84968-188">여기서 각 부분이 나타내는 의미는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="84968-188">where:</span></span>
  
- <span data-ttu-id="84968-p117">*도메인* 은 보호 하려는 도메인은입니다. 기본적으로 레코드는 도메인 및 모든 하위 도메인의 메일을 보호합니다. 예: 지정 하는 경우 \_dmarc.contoso.com, 다음 DMARC 도메인 및 housewares.contoso.com 또는 plumbing.contoso.com 등의 모든 하위 도메인의 메일을 보호 합니다.</span><span class="sxs-lookup"><span data-stu-id="84968-p117">*domain* is the domain you want to protect. By default, the record protects mail from the domain and all subdomains. For example, if you specify \_dmarc.contoso.com, then DMARC protects mail from the domain and all subdomains, such as housewares.contoso.com or plumbing.contoso.com.</span></span> 
    
- <span data-ttu-id="84968-p118">*TTL* 1 시간에 해당 하는 항상 되어야 합니다. 두 시간 (1 시간) TTL에 사용 되는 단위 (60 분), 분 또는 초 (3600 초) 도메인에 대 한 등록자에 따라 달라 집니다.</span><span class="sxs-lookup"><span data-stu-id="84968-p118">*TTL* should always be the equivalent of one hour. The unit used for TTL, either hours (1 hour), minutes (60 minutes), or seconds (3600 seconds), will vary depending on the registrar for your domain.</span></span> 
    
- <span data-ttu-id="84968-194">*pct = 100* 전자 메일의 100%에 대해이 규칙을 사용 해야 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="84968-194">*pct=100* indicates that this rule should be used for 100% of email.</span></span>
    
- <span data-ttu-id="84968-p119">*정책* DMARC 실패 하는 경우에 따라를 받는 서버를 원하는 어떤 정책을 지정 합니다. 정책을 격리를 없음으로 설정 하거나 취소할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="84968-p119">*policy* specifies what policy you want the receiving server to follow if DMARC fails. You can set the policy to none, quarantine, or reject.</span></span> 
    
<span data-ttu-id="84968-197">에 사용할 옵션에 대 한 내용은 [Office 365에서 DMARC를 구현 하기 위한 모범 사례](use-dmarc-to-validate-email.md#DMARCbestpractices)에 설명 된 개념을 숙지 됩니다.</span><span class="sxs-lookup"><span data-stu-id="84968-197">For information about which options to use, become familiar with the concepts in [Best practices for implementing DMARC in Office 365](use-dmarc-to-validate-email.md#DMARCbestpractices).</span></span>
  
<span data-ttu-id="84968-198">예제:</span><span class="sxs-lookup"><span data-stu-id="84968-198">Examples:</span></span>
  
- <span data-ttu-id="84968-199">None으로 설정 하는 정책</span><span class="sxs-lookup"><span data-stu-id="84968-199">Policy set to none</span></span>
  
    ```
    _dmarc.contoso.com 3600 IN  TXT  "v=DMARC1; p=none"
    ```

- <span data-ttu-id="84968-200">격리로 정책 설정</span><span class="sxs-lookup"><span data-stu-id="84968-200">Policy set to quarantine</span></span>
  
    ```
    _dmarc.contoso.com 3600 IN  TXT  "v=DMARC1; p=quarantine"
    ```

- <span data-ttu-id="84968-201">거부로 설정 하는 정책</span><span class="sxs-lookup"><span data-stu-id="84968-201">Policy set to reject</span></span>
  
    ```
    _dmarc.contoso.com  3600 IN  TXT  "v=DMARC1; p=reject"
    ```

<span data-ttu-id="84968-p120">사용자의 레코드를 세운 후에 도메인 등록자에서 레코드를 업데이트 해야 합니다. Office 365에 대 한 DNS 레코드를 DMARC TXT 레코드를 추가 하는 지침에 대 한 [DNS 레코드를 관리 하는 경우 Office 365 용 DNS 레코드 만들기](https://support.office.com/article/b0f3fdca-8a80-4e8e-9ef3-61e8a2a9ab23)를 참조 합니다.</span><span class="sxs-lookup"><span data-stu-id="84968-p120">Once you have formed your record, you need to update the record at your domain registrar. For instructions on adding the DMARC TXT record to your DNS records for Office 365, see [Create DNS records for Office 365 when you manage your DNS records](https://support.office.com/article/b0f3fdca-8a80-4e8e-9ef3-61e8a2a9ab23).</span></span>
  
## <a name="best-practices-for-implementing-dmarc-in-office-365"></a><span data-ttu-id="84968-204">Office 365에서 DMARC를 구현 하기 위한 모범 사례</span><span class="sxs-lookup"><span data-stu-id="84968-204">Best practices for implementing DMARC in Office 365</span></span>
<span data-ttu-id="84968-205"><a name="DMARCbestpractices"> </a></span><span class="sxs-lookup"><span data-stu-id="84968-205"></span></span>

<span data-ttu-id="84968-p121">메일 흐름의 나머지 부분에 영향을 주지 않고도 DMARC를 점진적으로 구현할 수 있습니다. 페이지를 만들고 다음과 같은이 단계로 구성 하는 전체 계획 roll을 구현 합니다. 하위 도메인을 다음 다른 하위 도메인으로 먼저 이러한 각 단계를 수행 하 고 마지막으로 다음 단계로 이동 하기 전에 조직에서 최상위 도메인으로 합니다.</span><span class="sxs-lookup"><span data-stu-id="84968-p121">You can implement DMARC gradually without impacting the rest of your mail flow. Create and implement a roll out plan that follows these steps. Do each of these steps first with a sub-domain, then other sub-domains, and finally with the top-level domain in your organization before moving on to the next step.</span></span>
  
1. <span data-ttu-id="84968-209">모니터 DMARC 구현의 영향</span><span class="sxs-lookup"><span data-stu-id="84968-209">Monitor the impact of implementing DMARC</span></span>
    
    <span data-ttu-id="84968-p122">하위 도메인 이나는 DMARC 수신기 사용자에 게 보낼가 해당 도메인을 사용 하 여 표시 하는 메시지에 대 한 통계를 요청 하는 도메인에 대 한 간단한 모니터링 모드 레코드를 시작 합니다. 모니터링 모드 레코드는 none으로 설정 하는 정책 수 있는 DMARC TXT 레코드 (p = 없음). 많은 기업이 p 사용 하 여 DMARC TXT 레코드를 게시 = none 확실 하지 않은 때문에 얼마나 많은 전자 메일에 대 한 보다 제한적인 DMARC 정책을 게시 하 여 손실 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="84968-p122">Start with a simple monitoring-mode record for a sub-domain or domain that requests that DMARC receivers send you statistics about messages that they see using that domain. A monitoring-mode record is a DMARC TXT record that has its policy set to none (p=none). Many companies publish a DMARC TXT record with p=none because they are unsure about how much email they may lose by publishing a more restrictive DMARC policy.</span></span> 
    
    <span data-ttu-id="84968-p123">메시징 인프라에서 SPF 또는 DKIM를 구현 했을 때 하기 전에도 수행할 수 있습니다. 그러나 효과적으로 격리 하거나도 SPF 및 DKIM을 구현할 때까지 DMARC를 사용 하 여 메일을 거부할 수 없습니다. SPF 및 DKIM을 소개 하는 대로 DMARC을 통해 생성 된 보고서의 번호 및 하지 않는 및 이러한 검사를 통과 하는 메시지의 원본 나옵니다. 합법적인 트래픽을 비용을 쉽게 확인할 수 있습니다,에서 다루지 하 고 모든 문제를 해결 합니다. 얼마나 많은 사기 메시지 전송 되 고, 참조도 먼저 어디에서 하 고 있습니다.</span><span class="sxs-lookup"><span data-stu-id="84968-p123">You can do this even before you've implemented SPF or DKIM in your messaging infrastructure. However, you won't be able to effectively quarantine or reject mail by using DMARC until you also implement SPF and DKIM. As you introduce SPF and DKIM, the reports generated through DMARC will provide the numbers and sources of messages that pass these checks, and those that don't. You can easily see how much of your legitimate traffic is or isn't covered by them, and troubleshoot any problems. You'll also begin to see how many fraudulent messages are being sent, and from where.</span></span>
    
2. <span data-ttu-id="84968-218">외부 메일 시스템 DMARC 실패 하는 메일 격리를 요청 합니다.</span><span class="sxs-lookup"><span data-stu-id="84968-218">Request that external mail systems quarantine mail that fails DMARC</span></span>
    
    <span data-ttu-id="84968-p124">생각 되는 모든 또는 대부분의 합법적인 트래픽 SPF 및 DKIM로 보호 되 고 DMARC 구현의 영향을 이해를 격리 정책을 구현할 수 있습니다. 격리 정책은 해당 정책이 격리로 설정 된 DMARC TXT 레코드입니다 (p = 격리). 이 작업을 수행 하 여 고객의 받은 편지함 대신 스팸 폴더에 해당 하는 로컬에 DMARC에 실패 하는 도메인의 메시지를 저장할 DMARC 수신기가 요청 됩니다.</span><span class="sxs-lookup"><span data-stu-id="84968-p124">When you believe that all or most of your legitimate traffic is protected by SPF and DKIM, and you understand the impact of implementing DMARC, you can implement a quarantine policy. A quarantine policy is a DMARC TXT record that has its policy set to quarantine (p=quarantine). By doing this, you are asking DMARC receivers to put messages from your domain that fail DMARC into the local equivalent of a spam folder instead of your customers' inboxes.</span></span>
    
3. <span data-ttu-id="84968-222">요청 외부 메일 시스템 DMARC 실패 하는 메시지를 허용 하지 않습니다</span><span class="sxs-lookup"><span data-stu-id="84968-222">Request that external mail systems not accept messages that fail DMARC</span></span>
    
    <span data-ttu-id="84968-p125">마지막 단계 거부 정책을 구현 됩니다. 거부 정책은 해당 정책을 거부로 설정한 DMARC TXT 레코드입니다 (p = 거부). 이 작업을 수행 하면 것을 요청 하지 DMARC 검사에 실패 하는 메시지를 수락 하려면 DMARC 수신기 합니다.</span><span class="sxs-lookup"><span data-stu-id="84968-p125">The final step is implementing a reject policy. A reject policy is a DMARC TXT record that has its policy set to reject (p=reject). When you do this, you're asking DMARC receivers not to accept messages that fail the DMARC checks.</span></span> 
    
## <a name="how-office-365-handles-outbound-email-that-fails-dmarc"></a><span data-ttu-id="84968-226">Office 365 DMARC 실패 하는 아웃 바운드 전자 메일을 처리 하는 방법</span><span class="sxs-lookup"><span data-stu-id="84968-226">How Office 365 handles outbound email that fails DMARC</span></span>
<span data-ttu-id="84968-227"><a name="outbounddmarcfail"> </a></span><span class="sxs-lookup"><span data-stu-id="84968-227"></span></span>

<span data-ttu-id="84968-p126">메시지는 Office 365에서 아웃 바운드 DMARC, 실패 하 고 정책을 p를 설정한 경우 = 격리 또는 p = 거부, 메시지는 [아웃 바운드 메시지 용 위험성이 높은 배달 풀](high-risk-delivery-pool-for-outbound-messages.md)을 통해 라우팅됩니다. 아웃 바운드 전자 메일에 대 한 재정의 하지 않음</span><span class="sxs-lookup"><span data-stu-id="84968-p126">If a message is outbound from Office 365 and fails DMARC, and you have set the policy to p=quarantine or p=reject, the message is routed through the [High-risk delivery pool for outbound messages](high-risk-delivery-pool-for-outbound-messages.md). There is no override for outbound email.</span></span>
  
<span data-ttu-id="84968-p127">DMARC 거부 정책을 게시 하는 경우 (p 거부 =), 메시지 서비스를 통해 아웃 바운드 메시지를 릴레이 하는 경우 도메인에 대 한 SPF 또는 DKIM를 전달할 수 없기 때문에 없는 다른 고객 Office 365에서 도메인을 스푸핑할 수 있습니다. 그러나 DMARC 거부 정책 게시를 수행 하는 경우 하지 않은 모든 전자 메일의 인증 된 Office 365를 통해 그 중 일부를 (위에서 설명한 대로), 인바운드 전자 메일에 대 한 스팸으로 표시 될 수 있습니다 또는 SPF 게시 및 릴레이 통해 아웃 바운드 시도 수행 하는 경우 거부 됨 서비스입니다. 이런 등 서버와 DMARC TXT 레코드를 형성 하는 경우 도메인을 대신 하 여 메일을 보내는 응용 프로그램에 대 한 IP 주소 중 일부를 포함 하도록 잊어버린 경우.</span><span class="sxs-lookup"><span data-stu-id="84968-p127">If you publish a DMARC reject policy (p=reject), no other customer in Office 365 can spoof your domain because messages will not be able to pass SPF or DKIM for your domain when relaying a message outbound through the service. However, if you do publish a DMARC reject policy but don't have all of your email authenticated through Office 365, some of it may be marked as spam for inbound email (as described above), or it will be rejected if you do not publish SPF and try to relay it outbound through the service. This happens, for example, if you forget to include some of the IP addresses for servers and apps that send mail on behalf of your domain when you form your DMARC TXT record.</span></span>
  
## <a name="how-office-365-handles-inbound-email-that-fails-dmarc"></a><span data-ttu-id="84968-233">Office 365 DMARC 실패 하는 인바운드 전자 메일을 처리 하는 방법</span><span class="sxs-lookup"><span data-stu-id="84968-233">How Office 365 handles inbound email that fails DMARC</span></span>
<span data-ttu-id="84968-234"><a name="inbounddmarcfail"> </a></span><span class="sxs-lookup"><span data-stu-id="84968-234"></span></span>

<span data-ttu-id="84968-p128">보내는 서버에 대 한 DMARC 정책은 p = 거부, EOP 스팸이 작업을 거부 하는 대신 메시지를 표시 합니다. 즉, 인바운드 전자 메일을 Office 365에서 p = 거부 및 p = 격리 동일한 방식으로 합니다.</span><span class="sxs-lookup"><span data-stu-id="84968-p128">If the DMARC policy of the sending server is p=reject, EOP marks the message as spam instead of rejecting it. In other words, for inbound email, Office 365 treats p=reject and p=quarantine the same way.</span></span>
  
<span data-ttu-id="84968-p129">Office 365 일부 합법적인 전자 메일 DMARC 실패할 수 있으므로 다음과 같이 구성 됩니다. 예, 다음 모든 목록 참가자에 게 메시지를 릴레이 하는 메일 그룹에 전송 된 경우 메시지 DMARC 실패할 수 있습니다. Office 365 이러한 메시지를 거부 하는 경우 사용자 수 합법적인 전자 메일 끊어지고 검색을 할 수 없습니다. 대신 이러한 메시지는 계속 DMARC 하지만 스팸으로 표시 및 거부 되지 것입니다. 필요한 경우 사용자가 여전히 얻을 수 이러한 메시지 받은 편지함에 이러한 메서드를 통해:</span><span class="sxs-lookup"><span data-stu-id="84968-p129">Office 365 is configured like this because some legitimate email may fail DMARC. For example, a message might fail DMARC if it is sent to a mailing list that then relays the message to all list participants. If Office 365 rejected these messages, people could lose legitimate email and have no way to retrieve it. Instead, these messages will still fail DMARC but they will be marked as spam and not rejected. If desired, users can still get these messages in their inbox through these methods:</span></span>
  
- <span data-ttu-id="84968-242">사용자가 수신 허용-보낸사람을 개별적으로 추가 자신의 전자 메일 클라이언트를 사용 하 여</span><span class="sxs-lookup"><span data-stu-id="84968-242">Users add safe senders individually by using their email client</span></span>
    
- <span data-ttu-id="84968-243">관리자가 해당 특정 보낸사람에 대 한 메시지를 허용 하는 모든 사용자에 대 한 (ETR)는 Exchange 전송 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="84968-243">Administrators create an Exchange transport rule (ETR) for all users that allows messages for those particular senders.</span></span> 
    
## <a name="troubleshooting-your-dmarc-implementation"></a><span data-ttu-id="84968-244">DMARC 구현 문제해결</span><span class="sxs-lookup"><span data-stu-id="84968-244">Troubleshooting your DMARC implementation</span></span>
<span data-ttu-id="84968-245"><a name="dmarctroubleshoot"> </a></span><span class="sxs-lookup"><span data-stu-id="84968-245"></span></span>

<span data-ttu-id="84968-246">EOP는 첫번째 항목 하지 도메인의 MX 레코드를 구성 해 둔 DMARC 오류 도메인에 대해 적용 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="84968-246">If you have configured your domain's MX records where EOP is not the first entry, DMARC failures will not be enforced for your domain.</span></span> 
  
<span data-ttu-id="84968-p130">Office 365 고객 도메인의 기본 MX 레코드가 EOP를 가리키지 않을 경우에 DMARC의 장점을 부여 되지 않습니다. 예, 온-프레미스 메일 서버로 MX 레코드를 가리킨 다음 커넥터를 사용 하 여 EOP로 전자 메일을 라우팅하는 경우 DMARC 작동 하지 않습니다. 이 시나리오에서 받는 도메인을 사용 하 여 허용 도메인 중 하나가 EOP 아니지만 기본 MX 합니다. 예: contoso.com의 MX 자체에서 가리키는으로 사용 하 여 EOP 보조 MX 레코드를, 인스턴트 메시징 세션 contoso.com의 MX 레코드는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="84968-p130">If you're an Office 365 customer, and your domain's primary MX record does not point to EOP, you will not get the benefits of DMARC. For example, DMARC won't work if you point the MX record to your on-premises mail server and then route email to EOP by using a connector. In this scenario, the receiving domain is one of your Accepted-Domains but EOP is not the primary MX. For example, suppose contoso.com points its MX at itself and uses EOP as a secondary MX record, contoso.com's MX record looks like the following:</span></span>
  
```
contoso.com     3600   IN  MX  0  mail.contoso.com
contoso.com     3600   IN  MX  10 contoso-com.mail.protection.outlook.com
```

<span data-ttu-id="84968-p131">기본 MX 이며 EOP로 메일 라우팅됩니다 다음 이후 모두 또는 대부분, 전자 메일에는 mail.contoso.com 먼저 라우팅되는 합니다. 경우에 따라 전혀 MX 레코드를으로 EOP를 나열 하 고 전자 메일을 라우팅하는 커넥터를 간단 하 게 연결할 아니더라도 될 수 있습니다. EOP 해야할 필요가 DMARC 유효성 검사에 대 한 첫번째 항목을 사용할 필요가 없습니다. 방금 모든 온-프레미스/비-o 365 서버 DMARC 검사는 특정 수 없습니다는 유효성 검사를 보장 합니다.  DMARC는 고객의 도메인 (서버가 아님)에 대 한 적용 하 여이 가능한 경우 DMARC TXT 레코드를 설정 하지만 실제로 적용을 수행 하는 받는 서버 달려있습니다.  받는 서버와 EOP를 설정 하는 경우 EOP DMARC 적용을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="84968-p131">All, or most, email will first be routed to mail.contoso.com since it's the primary MX, and then mail will get routed to EOP. In some cases, you might not even list EOP as an MX record at all and simply hook up connectors to route your email. EOP does not have to be the first entry for DMARC validation to be done. It just ensures the validation, as we cannot be certain that all on-premise/non-O365 servers will do DMARC checks.  DMARC is eligible to be enforced for a customer’s domain (not server) when you set up the DMARC TXT record, but it is up to the receiving server to actually do the enforcement.  If you set up EOP as the receiving server, then EOP does the DMARC enforcement.</span></span>
  
## <a name="for-more-information"></a><span data-ttu-id="84968-257">자세한 내용</span><span class="sxs-lookup"><span data-stu-id="84968-257">For more information</span></span>
<span data-ttu-id="84968-258"><a name="sectionSection8"> </a></span><span class="sxs-lookup"><span data-stu-id="84968-258"></span></span>

<span data-ttu-id="84968-p132">DMARC 하는 방법에 대 한 자세한 내용은 지 여부 이러한 리소스 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="84968-p132">Want more information about DMARC? These resources can help.</span></span>
  
- <span data-ttu-id="84968-261">[스팸 방지 메시지 헤더](anti-spam-message-headers.md) DMARC 확인을 위한 Office 365에서 사용 되는 구문과 헤더 필드를 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="84968-261">[Anti-spam message headers](anti-spam-message-headers.md) includes the syntax and header fields used by Office 365 for DMARC checks.</span></span> 
    
- <span data-ttu-id="84968-262">M <sup>3</sup>AAWG (메시징, 맬웨어, 모바일 방지 오용 작업 그룹)에서 [DMARC 교육 시리즈](https://www.m3aawg.org/activities/training/dmarc-training-series) 를 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="84968-262">Take the [DMARC Training Series](https://www.m3aawg.org/activities/training/dmarc-training-series) from M <sup>3</sup>AAWG (Messaging, Malware, Mobile Anti-Abuse Working Group).</span></span>
    
- <span data-ttu-id="84968-263">[Dmarcian](https://space.dmarcian.com/deployment/)에서 검사 목록을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="84968-263">Use the checklist at [dmarcian](https://space.dmarcian.com/deployment/).</span></span>
    
- <span data-ttu-id="84968-264">[DMARC.org](https://dmarc.org)에서 원본에 직접 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="84968-264">Go directly to the source at [DMARC.org](https://dmarc.org).</span></span>
    
## <a name="see-also"></a><span data-ttu-id="84968-265">참고 항목</span><span class="sxs-lookup"><span data-stu-id="84968-265">See also</span></span>
<span data-ttu-id="84968-266"><a name="sectionSection8"> </a></span><span class="sxs-lookup"><span data-stu-id="84968-266"></span></span>

[<span data-ttu-id="84968-267">Office 365 스푸핑 방지 하기 위해 보낸 사람이 정책 프레임 워크 (SPF)을 사용 하는 방법</span><span class="sxs-lookup"><span data-stu-id="84968-267">How Office 365 uses Sender Policy Framework (SPF) to prevent spoofing</span></span>](how-office-365-uses-spf-to-prevent-spoofing.md)
  
[<span data-ttu-id="84968-268">스푸핑을 방지할 수 있도록 Office 365에서 SPF 설정</span><span class="sxs-lookup"><span data-stu-id="84968-268">Set up SPF in Office 365 to help prevent spoofing</span></span>](set-up-spf-in-office-365-to-help-prevent-spoofing.md)
  
[<span data-ttu-id="84968-269">DKIM를 사용 하 여 Office 365에서 사용자 지정 도메인에서 보낸 아웃 바운드 전자 메일의 유효성을 검사 하려면</span><span class="sxs-lookup"><span data-stu-id="84968-269">Use DKIM to validate outbound email sent from your custom domain in Office 365</span></span>](use-dkim-to-validate-outbound-email.md)

