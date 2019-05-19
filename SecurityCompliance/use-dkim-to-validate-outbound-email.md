---
title: Office 365의 사용자 지정 도메인에서 DKIM을 사용 하 여 전자 메일 보내기
ms.author: tracyp
author: MSFTTracyP
manager: laurawi
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 56fee1c7-dc37-470e-9b09-33fff6d94617
ms.collection:
- M365-security-compliance
description: 요약:이 문서에서는 대상 전자 메일 시스템이 사용자 지정 도메인에서 보낸 메시지를 신뢰 하도록 하기 위해 Office 365에서 DomainKeys 식별 메일 (DKIM)을 사용 하는 방법에 대해 설명 합니다.
ms.openlocfilehash: 35df7cdd1a95311dac612aa486670e03f6f23d07
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/17/2019
ms.locfileid: "34158010"
---
# <a name="use-dkim-to-validate-outbound-email-sent-from-your-custom-domain-in-office-365"></a><span data-ttu-id="b9298-103">DKIM을 사용 하 여 Office 365의 사용자 지정 도메인에서 전송 되는 아웃 바운드 전자 메일의 유효성 검사</span><span class="sxs-lookup"><span data-stu-id="b9298-103">Use DKIM to validate outbound email sent from your custom domain in Office 365</span></span>

 <span data-ttu-id="b9298-104">**요약:** 이 문서에서는 사용자 지정 도메인에서 보낸 아웃 바운드 메시지를 대상 전자 메일 시스템에서 신뢰 하도록 하기 위해 Office 365의 DKIM (DomainKeys 확인 메일)을 사용 하는 방법에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9298-104">**Summary:** This article describes how you use DomainKeys Identified Mail (DKIM) with Office 365 to ensure that destination email systems trust messages sent outbound from your custom domain.</span></span> 
  
<span data-ttu-id="b9298-105">SPF 및 DMARC 외에 DKIM을 사용 하 여 spoofers가 도메인에서 오는 것 처럼 보이지만 메시지를 보내지 않도록 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9298-105">You should use DKIM in addition to SPF and DMARC to help prevent spoofers from sending messages that look like they are coming from your domain.</span></span> <span data-ttu-id="b9298-106">DKIM을 사용 하 여 메시지 헤더에 전자 메일 메시지에 디지털 서명을 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b9298-106">DKIM lets you add a digital signature to email messages in the message header.</span></span> <span data-ttu-id="b9298-107">복잡 하 게 들리지만 실제로는 그렇지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b9298-107">Sounds complicated, but it's really not.</span></span> <span data-ttu-id="b9298-108">DKIM을 구성 하는 경우 암호화 인증을 사용 하 여 전자 메일 메시지에 해당 이름을 연결 하거나 서명 하도록 도메인에 권한을 부여 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9298-108">When you configure DKIM, you authorize your domain to associate, or sign, its name to an email message by using cryptographic authentication.</span></span> <span data-ttu-id="b9298-109">도메인에서 전자 메일을 수신 하는 전자 메일 시스템은이 디지털 서명을 사용 하 여 받는 전자 메일이 합법적인 지 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b9298-109">Email systems that receive email from your domain can use this digital signature to help determine if incoming email that they receive is legitimate.</span></span>
  
<span data-ttu-id="b9298-110">기본적으로 개인 키를 사용 하 여 도메인의 보내는 전자 메일에 있는 헤더를 암호화 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9298-110">Basically, you use a private key to encrypt the header in your domain's outgoing email.</span></span> <span data-ttu-id="b9298-111">받는 서버에서 서명을 디코딩하는 데 사용할 수 있는 도메인의 DNS 레코드에 공개 키를 게시 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9298-111">You publish a public key to your domain's DNS records that receiving servers can then use to decode the signature.</span></span> <span data-ttu-id="b9298-112">공개 키를 사용 하 여 메시지가 실제로 사용자 로부터 온 것이 고 사용자가 도메인을 위장 하지 못하게 하는 것을 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9298-112">They use the public key to verify that the messages are really coming from you and not coming from someone spoofing your domain.</span></span>
  
<span data-ttu-id="b9298-113">Office 365에서는 초기 도메인에 대해 DKIM을 자동으로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9298-113">Office 365 automatically sets up DKIM for initial domains.</span></span> <span data-ttu-id="b9298-114">초기 도메인은 contoso.onmicrosoft.com과 같이 서비스에 등록 했을 때 Office 365에서 만든 도메인입니다.</span><span class="sxs-lookup"><span data-stu-id="b9298-114">The initial domain is the domain that Office 365 created for you when you signed up with the service, for example, contoso.onmicrosoft.com.</span></span> <span data-ttu-id="b9298-115">초기 도메인에 대해 DKIM을 설정 하는 작업은 필요 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b9298-115">You don't need to do anything to set up DKIM for your initial domain.</span></span> <span data-ttu-id="b9298-116">도메인에 대 한 자세한 내용은 [도메인 FAQ](https://support.office.com/article/Domains-FAQ-1272bad0-4bd4-4796-8005-67d6fb3afc5a#bkmk_whydoihaveanonmicrosoft.comdomain)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="b9298-116">For more information about domains, see [Domains FAQ](https://support.office.com/article/Domains-FAQ-1272bad0-4bd4-4796-8005-67d6fb3afc5a#bkmk_whydoihaveanonmicrosoft.comdomain).</span></span>
  
<span data-ttu-id="b9298-117">사용자 지정 도메인에 대 한 DKIM에 대해서도 작업을 수행 하지 않도록 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b9298-117">You can choose to do nothing about DKIM for your custom domain too.</span></span> <span data-ttu-id="b9298-118">사용자 지정 도메인에 대해 DKIM을 설정 하지 않으면 Office 365에서 개인 및 공개 키 쌍을 만들고 DKIM 서명을 사용 하도록 설정한 다음 사용자 지정 도메인에 대해 Office 365 기본 정책을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9298-118">If you do not set up DKIM for your custom domain, Office 365 creates a private and public key pair, enables DKIM signing, and then configures the Office 365 default policy for your custom domain.</span></span> <span data-ttu-id="b9298-119">대부분의 Office 365 고객에 게는 충분 한 범위를 제공 하지만 다음과 같은 상황에서는 사용자 지정 도메인에 대해 DKIM을 수동으로 구성 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9298-119">While this is sufficient coverage for most Office 365 customers, you should manually configure DKIM for your custom domain in the following circumstances:</span></span>
  
- <span data-ttu-id="b9298-120">Office 365에 사용자 지정 도메인이 두 개 이상 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b9298-120">You have more than one custom domain in Office 365</span></span>
    
- <span data-ttu-id="b9298-121">DMARC를 설정 하겠습니다 (권장).</span><span class="sxs-lookup"><span data-stu-id="b9298-121">You're going to set up DMARC too (recommended)</span></span>
    
- <span data-ttu-id="b9298-122">개인 키를 제어할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b9298-122">You want control over your private key</span></span>
    
- <span data-ttu-id="b9298-123">CNAME 레코드를 사용자 지정 하려는 경우</span><span class="sxs-lookup"><span data-stu-id="b9298-123">You want to customize your CNAME records</span></span>
    
- <span data-ttu-id="b9298-124">타사의 대량 메일 프로그램을 사용 하는 경우와 같이 타사 도메인에서 시작 되는 사용자에 대해 DKIM 키를 설정 하려는 경우</span><span class="sxs-lookup"><span data-stu-id="b9298-124">You want to set up DKIM keys for email originating out of a third-party domain, for example, if you use a third-party bulk mailer.</span></span>
    
<span data-ttu-id="b9298-125">이 문서의 내용</span><span class="sxs-lookup"><span data-stu-id="b9298-125">In this article:</span></span>
  
- [<span data-ttu-id="b9298-126">DKIM이 SPF 단독으로 작동 하 여 Office 365에서 악의적인 스푸핑을 방지 하는 방법</span><span class="sxs-lookup"><span data-stu-id="b9298-126">How DKIM works better than SPF alone to prevent malicious spoofing in Office 365</span></span>](use-dkim-to-validate-outbound-email.md#HowDKIMWorks)
    
- [<span data-ttu-id="b9298-127">Office 365에서 DKIM을 수동으로 설정 하기 위해 수행 해야 하는 작업</span><span class="sxs-lookup"><span data-stu-id="b9298-127">What you need to do to manually set up DKIM in Office 365</span></span>](use-dkim-to-validate-outbound-email.md#SetUpDKIMO365)
    
- [<span data-ttu-id="b9298-128">Office 365에서 둘 이상의 사용자 지정 도메인에 대해 DKIM을 구성 하려면</span><span class="sxs-lookup"><span data-stu-id="b9298-128">To configure DKIM for more than one custom domain in Office 365</span></span>](use-dkim-to-validate-outbound-email.md#DKIMMultiDomain)
    
- [<span data-ttu-id="b9298-129">Office 365에서 사용자 지정 도메인에 대해 DKIM 서명 정책 사용 안 함</span><span class="sxs-lookup"><span data-stu-id="b9298-129">Disabling the DKIM signing policy for a custom domain in Office 365</span></span>](use-dkim-to-validate-outbound-email.md#DisableDKIMSigningPolicy)
    
- [<span data-ttu-id="b9298-130">DKIM 및 Office 365에 대 한 기본 동작</span><span class="sxs-lookup"><span data-stu-id="b9298-130">Default behavior for DKIM and Office 365</span></span>](use-dkim-to-validate-outbound-email.md#DefaultDKIMbehavior)
    
- [<span data-ttu-id="b9298-131">타사 서비스가 사용자 지정 도메인을 대신 하 여 전자 메일을 보내거나 스푸핑할 수 있도록 DKIM을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9298-131">Set up DKIM so that a third-party service can send, or spoof, email on behalf of your custom domain</span></span>](use-dkim-to-validate-outbound-email.md#SetUp3rdPartyspoof)
    
- [<span data-ttu-id="b9298-132">다음 단계: Office 365에 대 한 DKIM을 설정한 후</span><span class="sxs-lookup"><span data-stu-id="b9298-132">Next steps: After you set up DKIM for Office 365</span></span>](use-dkim-to-validate-outbound-email.md#DKIMNextSteps)
    
## <a name="how-dkim-works-better-than-spf-alone-to-prevent-malicious-spoofing-in-office-365"></a><span data-ttu-id="b9298-133">DKIM이 SPF 단독으로 작동 하 여 Office 365에서 악의적인 스푸핑을 방지 하는 방법</span><span class="sxs-lookup"><span data-stu-id="b9298-133">How DKIM works better than SPF alone to prevent malicious spoofing in Office 365</span></span>
<span data-ttu-id="b9298-134"><a name="HowDKIMWorks"> </a></span><span class="sxs-lookup"><span data-stu-id="b9298-134"></span></span>

<span data-ttu-id="b9298-135">SPF는 정보를 메시지 봉투에 추가 하지만 DKIM은 메시지 헤더 내의 서명을 실제로 암호화 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9298-135">SPF adds information to a message envelope but DKIM actually encrypts a signature within the message header.</span></span> <span data-ttu-id="b9298-136">메시지를 전달 하면 메시지 봉투의 일부를 전달 서버에서 제거할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b9298-136">When you forward a message, portions of that message's envelope can be stripped away by the forwarding server.</span></span> <span data-ttu-id="b9298-137">디지털 서명이 전자 메일 헤더의 일부 이기 때문에 전자 메일 메시지에 남아 있으므로 다음 예제와 같이 메시지가 전달 된 경우에도 DKIM은 작동 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9298-137">Since the digital signature stays with the email message because it's part of the email header, DKIM works even when a message has been forwarded as shown in the following example.</span></span>
  
![SPF 확인이 실패하는 경우 DKIM 인증을 제공하는 전달된 메시지를 보여주는 다이어그램](media/28f93b4c-97e7-4309-acc4-fd0d2e0e3377.jpg)
  
<span data-ttu-id="b9298-139">이 예에서는 도메인에 대 한 SPF TXT 레코드만 게시 했을 때 받는 사람의 메일 서버에서 전자 메일을 스팸으로 표시 했을 수 있고 가양성 결과를 생성 했습니다.</span><span class="sxs-lookup"><span data-stu-id="b9298-139">In this example, if you had only published an SPF TXT record for your domain, the recipient's mail server could have marked your email as spam and generated a false positive result.</span></span> <span data-ttu-id="b9298-140">이 시나리오에서 DKIM을 추가 하면 가양성 스팸 보고를 줄일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b9298-140">The addition of DKIM in this scenario reduces false positive spam reporting.</span></span> <span data-ttu-id="b9298-141">DKIM은 공개 키 암호화를 통해 IP 주소를 인증 하는 데 의존 하므로 DKIM은 SPF 보다 더 강력한 형태의 인증으로 간주 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b9298-141">Because DKIM relies on public key cryptography to authenticate and not just IP addresses, DKIM is considered a much stronger form of authentication than SPF.</span></span> <span data-ttu-id="b9298-142">SPF 및 DKIM과 DMARC을 모두 사용 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="b9298-142">We recommend using both SPF and DKIM, as well as DMARC in your deployment.</span></span>
  
<span data-ttu-id="b9298-143">Nitty 주요: DKIM은 개인 키를 사용 하 여 메시지 헤더에 암호화 된 서명을 삽입 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9298-143">The nitty gritty: DKIM uses a private key to insert an encrypted signature into the message headers.</span></span> <span data-ttu-id="b9298-144">서명 도메인 또는 아웃 바운드 도메인은 헤더에서 **d =** 필드의 값으로 삽입 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b9298-144">The signing domain, or outbound domain, is inserted as the value of the **d=** field in the header.</span></span> <span data-ttu-id="b9298-145">확인 도메인 또는 받는 사람 도메인에서 **d =** 필드를 사용 하 여 DNS에서 공개 키를 조회 하 고 메시지를 인증 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9298-145">The verifying domain, or recipient's domain, then use the **d=** field to look up the public key from DNS and authenticate the message.</span></span> <span data-ttu-id="b9298-146">메시지가 확인 되 면 DKIM 검사가 통과 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9298-146">If the message is verified, the DKIM check passes.</span></span> 
  
## <a name="what-you-need-to-do-to-manually-set-up-dkim-in-office-365"></a><span data-ttu-id="b9298-147">Office 365에서 DKIM을 수동으로 설정 하기 위해 수행 해야 하는 작업</span><span class="sxs-lookup"><span data-stu-id="b9298-147">What you need to do to manually set up DKIM in Office 365</span></span>
<span data-ttu-id="b9298-148"><a name="SetUpDKIMO365"> </a></span><span class="sxs-lookup"><span data-stu-id="b9298-148"></span></span>

<span data-ttu-id="b9298-149">DKIM을 구성 하려면 다음 단계를 완료 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9298-149">To configure DKIM, you will complete these steps:</span></span>
  
- [<span data-ttu-id="b9298-150">DNS에서 사용자 지정 도메인에 대 한 두 개의 CNAME 레코드 게시</span><span class="sxs-lookup"><span data-stu-id="b9298-150">Publish two CNAME records for your custom domain in DNS</span></span>](use-dkim-to-validate-outbound-email.md#Publish2CNAME)
    
- [<span data-ttu-id="b9298-151">Office 365에서 사용자 지정 도메인에 대해 DKIM 서명 사용</span><span class="sxs-lookup"><span data-stu-id="b9298-151">Enable DKIM signing for your custom domain in Office 365</span></span>](use-dkim-to-validate-outbound-email.md#EnableDKIMinO365)
    
### <a name="publish-two-cname-records-for-your-custom-domain-in-dns"></a><span data-ttu-id="b9298-152">DNS에서 사용자 지정 도메인에 대 한 두 개의 CNAME 레코드 게시</span><span class="sxs-lookup"><span data-stu-id="b9298-152">Publish two CNAME records for your custom domain in DNS</span></span>
<span data-ttu-id="b9298-153"><a name="Publish2CNAME"> </a></span><span class="sxs-lookup"><span data-stu-id="b9298-153"></span></span>

<span data-ttu-id="b9298-154">DNS에서 DKIM 서명을 추가 하려는 각 도메인에 대해 두 개의 CNAME 레코드를 게시 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9298-154">For each domain for which you want to add a DKIM signature in DNS, you need to publish two CNAME records.</span></span> <span data-ttu-id="b9298-155">DNS에서 CNAME 레코드를 사용 하 여 도메인의 정식 이름이 다른 도메인 이름의 별칭을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9298-155">A CNAME record is used by DNS to specify that the canonical name of a domain is an alias for another domain name.</span></span> <span data-ttu-id="b9298-156">사용자 지정 된 도메인에 대해 공개적으로 사용 가능한 DNS 서버에 CNAME 레코드를 만들어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9298-156">The CNAME records should be created on the publicly available DNS servers for your customized domains.</span></span> <span data-ttu-id="b9298-157">DNS의 CNAME 레코드는 이미 만들어진 Microsoft DNS 서버 (Office 365 용)의 DNS에 있는 레코드를 가리킵니다.</span><span class="sxs-lookup"><span data-stu-id="b9298-157">The CNAME records in your DNS will point to already created A records that exist in DNS on the Microsoft DNS servers for Office 365.</span></span>
  
 <span data-ttu-id="b9298-158">Office 365에서는 설정한 두 레코드를 사용 하 여 자동 키 회전을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9298-158">Office 365 performs automatic key rotation using the two records that you establish.</span></span> <span data-ttu-id="b9298-159">Office 365의 초기 도메인 외에 사용자 지정 도메인을 프로 비전 한 경우에는 각 추가 도메인에 대해 두 개의 CNAME 레코드를 게시 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9298-159">If you have provisioned custom domains in addition to the initial domain in Office 365, you must publish two CNAME records for each additional domain.</span></span> <span data-ttu-id="b9298-160">따라서 도메인이 두 개 있는 경우 두 개의 추가 CNAME 레코드를 게시 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9298-160">So, if you have two domains, you must publish two additional CNAME records, and so on.</span></span>
  
<span data-ttu-id="b9298-161">CNAME 레코드에는 다음 형식을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9298-161">Use the following format for the CNAME records.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b9298-162">GCC High 고객 중 하나인 경우 _domainGuid_ 을 다르게 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9298-162">If you are one of our GCC High customers, we calculate _domainGuid_ differently!</span></span> <span data-ttu-id="b9298-163">_DomainGuid_를 계산 하기 위해 _INITIALDOMAIN_ 의 MX 레코드를 조회 하는 대신 사용자 지정 된 도메인에서 직접 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9298-163">Instead of looking up the MX record for your _initialDomain_ to calculate _domainGuid_, instead we calculate it directly from the customized domain.</span></span> <span data-ttu-id="b9298-164">예를 들어 사용자 지정 된 도메인이 "contoso.com" 이면 domainGuid가 "contoso-com"이 되 고 모든 기간은 대시로 바뀝니다.</span><span class="sxs-lookup"><span data-stu-id="b9298-164">For example, if your customized domain is “contoso.com” your domainGuid becomes “contoso-com”, any periods are replaced with a dash.</span></span> <span data-ttu-id="b9298-165">따라서, initialDomain가 가리키는 MX 레코드에 관계 없이 항상 위의 메서드를 사용 하 여 CNAME 레코드에 사용할 domainGuid를 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9298-165">So, regardless of what MX record your initialDomain points to, you’ll always use the above method to calculate the domainGuid to use in your CNAME records.</span></span>

  
```
Host name:          selector1._domainkey
Points to address or value: selector1-<domainGUID>._domainkey.<initialDomain> 
TTL:                3600

Host name:          selector2._domainkey
Points to address or value: selector2-<domainGUID>._domainkey.<initialDomain> 
TTL:                3600
```

<span data-ttu-id="b9298-166">여기서 각 부분이 나타내는 의미는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="b9298-166">Where:</span></span>
  
- <span data-ttu-id="b9298-167">Office 365의 경우 선택기는 항상 "selector1" 또는 "selector2"입니다.</span><span class="sxs-lookup"><span data-stu-id="b9298-167">For Office 365, the selectors will always be "selector1" or "selector2".</span></span> 
    
- <span data-ttu-id="b9298-168">_domainGUID_ 는 mail.protection.outlook.com 앞에 표시 되는 사용자 지정 도메인에 대 한 사용자 정의 MX 레코드의 _domainGUID_ 과 동일 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9298-168">_domainGUID_ is the same as the _domainGUID_ in the customized MX record for your custom domain that appears before mail.protection.outlook.com.</span></span> <span data-ttu-id="b9298-169">예를 들어 contoso.com 도메인에 대 한 다음 MX 레코드에서 _domainGUID_ 는 contoso-com입니다.</span><span class="sxs-lookup"><span data-stu-id="b9298-169">For example, in the following MX record for the domain contoso.com, the _domainGUID_ is contoso-com:</span></span> 
    
    ```
    contoso.com.  3600  IN  MX   5 contoso-com.mail.protection.outlook.com
    ```

- <span data-ttu-id="b9298-170">_Initialdomain_ 은 Office 365에 등록할 때 사용한 도메인입니다.</span><span class="sxs-lookup"><span data-stu-id="b9298-170">_initialDomain_ is the domain that you used when you signed up for Office 365.</span></span> <span data-ttu-id="b9298-171">초기 도메인은 항상 onmicrosoft.com으로 끝납니다.</span><span class="sxs-lookup"><span data-stu-id="b9298-171">Initial domains always end in onmicrosoft.com.</span></span> <span data-ttu-id="b9298-172">초기 도메인을 결정 하는 방법에 대 한 자세한 내용은 [DOMAINS FAQ](https://support.office.com/article/1272bad0-4bd4-4796-8005-67d6fb3afc5a#bkmk_whydoihaveanonmicrosoft.comdomain)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="b9298-172">For information about determining your initial domain, see [Domains FAQ](https://support.office.com/article/1272bad0-4bd4-4796-8005-67d6fb3afc5a#bkmk_whydoihaveanonmicrosoft.comdomain).</span></span>
    
<span data-ttu-id="b9298-173">예를 들어 cohovineyardandwinery.onmicrosoft.com의 초기 도메인과 두 개의 사용자 지정 도메인 cohovineyard.com 및 cohowinery.com가 있는 경우에는 각 추가 도메인에 대해 두 개의 CNAME 레코드를 설정 해야 하 고 총 4 개의 CNAME 레코드를 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b9298-173">For example, if you have an initial domain of cohovineyardandwinery.onmicrosoft.com, and two custom domains cohovineyard.com and cohowinery.com, you would need to set up two CNAME records for each additional domain, for a total of four CNAME records.</span></span>
  
```
Host name:          selector1._domainkey
Points to address or value: **selector1-cohovineyard-com**._domainkey.cohovineyardandwinery.onmicrosoft.com
TTL:                3600

Host name:          selector2._domainkey
Points to address or value: **selector2-cohovineyard-com**._domainkey.cohovineyardandwinery.onmicrosoft.com
TTL:                3600

Host name:          selector1._domainkey
Points to address or value: **selector1-cohowinery-com**._domainkey.cohovineyardandwinery.onmicrosoft.com 
TTL:                3600
 
Host name:          selector2._domainkey
Points to address or value: **selector2-cohowinery-com**._domainkey.cohovineyardandwinery.onmicrosoft.com 
TTL:                3600
```

### <a name="enable-dkim-signing-for-your-custom-domain-in-office-365"></a><span data-ttu-id="b9298-174">Office 365에서 사용자 지정 도메인에 대해 DKIM 서명 사용</span><span class="sxs-lookup"><span data-stu-id="b9298-174">Enable DKIM signing for your custom domain in Office 365</span></span>
<span data-ttu-id="b9298-175"><a name="EnableDKIMinO365"> </a></span><span class="sxs-lookup"><span data-stu-id="b9298-175"></span></span>

<span data-ttu-id="b9298-176">CNAME 레코드를 DNS에 게시 한 후에는 Office 365을 통해 DKIM 서명을 사용 하도록 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b9298-176">Once you have published the CNAME records in DNS, you are ready to enable DKIM signing through Office 365.</span></span> <span data-ttu-id="b9298-177">Microsoft 365 관리 센터를 통해 또는 PowerShell을 사용 하 여이 작업을 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b9298-177">You can do this either through the Microsoft 365 admin center or by using PowerShell.</span></span>
  
#### <a name="to-enable-dkim-signing-for-your-custom-domain-through-the-admin-center"></a><span data-ttu-id="b9298-178">관리 센터를 통해 사용자 지정 도메인에 대해 DKIM 서명을 사용 하도록 설정 하려면</span><span class="sxs-lookup"><span data-stu-id="b9298-178">To enable DKIM signing for your custom domain through the admin center</span></span>

1. <span data-ttu-id="b9298-179">회사 또는 학교 계정로 [Office 365에 로그인](https://support.office.microsoft.com/article/e9eb7d51-5430-4929-91ab-6157c5a050b4)합니다.</span><span class="sxs-lookup"><span data-stu-id="b9298-179">[Sign in to Office 365](https://support.office.microsoft.com/article/e9eb7d51-5430-4929-91ab-6157c5a050b4) with your work or school account.</span></span> 
    
2. <span data-ttu-id="b9298-180">왼쪽 위에서 앱 시작 관리자 아이콘을 선택하고 **관리자**를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="b9298-180">Select the app launcher icon in the upper-left and choose **Admin**.</span></span>
    
3. <span data-ttu-id="b9298-181">왼쪽 아래 탐색에서 **관리자** 를 확장 하 고 **Exchange**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9298-181">In the lower-left navigation, expand **Admin** and choose **Exchange**.</span></span>
    
4. <span data-ttu-id="b9298-182">**보호** \> **dkim**으로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9298-182">Go to **Protection** \> **dkim**.</span></span>
    
5. <span data-ttu-id="b9298-183">DKIM을 사용 하도록 설정할 도메인을 선택 하 고 **이 도메인에 대해 dkim 서명을 사용 하 여 메시지를 서명**하려면 **사용**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9298-183">Select the domain for which you want to enable DKIM and then, for **Sign messages for this domain with DKIM signatures**, choose **Enable**.</span></span> <span data-ttu-id="b9298-184">각 사용자 지정 도메인에 대해이 단계를 반복 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9298-184">Repeat this step for each custom domain.</span></span>
    
#### <a name="to-enable-dkim-signing-for-your-custom-domain-by-using-powershell"></a><span data-ttu-id="b9298-185">PowerShell을 사용 하 여 사용자 지정 도메인에 대해 DKIM 서명을 사용 하도록 설정 하려면</span><span class="sxs-lookup"><span data-stu-id="b9298-185">To enable DKIM signing for your custom domain by using PowerShell</span></span>

1. <span data-ttu-id="b9298-186">[Exchange Online PowerShell에 연결합니다](https://technet.microsoft.com/library/jj984289.aspx).</span><span class="sxs-lookup"><span data-stu-id="b9298-186">[Connect to Exchange Online PowerShell](https://technet.microsoft.com/library/jj984289.aspx).</span></span>
    
2. <span data-ttu-id="b9298-187">다음 명령을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="b9298-187">Run the following command:</span></span>
    
    ```
    New-DkimSigningConfig -DomainName <domain> -Enabled $true
    ```

   <span data-ttu-id="b9298-188">여기서 _domain_ 은 dkim 서명을 사용 하도록 설정 하려는 사용자 지정 도메인의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b9298-188">Where _domain_ is the name of the custom domain that you want to enable DKIM signing for.</span></span> 
    
   <span data-ttu-id="b9298-189">예를 들어 contoso.com 도메인의 경우 다음을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9298-189">For example, for the domain contoso.com:</span></span>
    
    ```
    New-DkimSigningConfig -DomainName contoso.com -Enabled $true
    ```

#### <a name="to-confirm-dkim-signing-is-configured-properly-for-office-365"></a><span data-ttu-id="b9298-190">DKIM 서명이 Office 365에 맞게 구성 되었는지 확인 하려면</span><span class="sxs-lookup"><span data-stu-id="b9298-190">To Confirm DKIM signing is configured properly for Office 365</span></span>

<span data-ttu-id="b9298-191">이 단계를 수행 하 여 DKIM을 올바르게 구성 했는지 확인 하려면 몇 분 정도 기다립니다.</span><span class="sxs-lookup"><span data-stu-id="b9298-191">Wait a few minutes before you follow these steps to confirm that you have properly configured DKIM.</span></span> <span data-ttu-id="b9298-192">이를 통해 도메인에 대 한 DKIM 정보가 네트워크 전체에 분산 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b9298-192">This allows time for the DKIM information about the domain to be spread throughout the network.</span></span>
  
- <span data-ttu-id="b9298-193">Office 365 DKIM을 사용 하는 도메인 내의 계정에서 outlook.com 또는 Hotmail.com 등의 다른 전자 메일 계정으로 메시지를 보냅니다.</span><span class="sxs-lookup"><span data-stu-id="b9298-193">Send a message from an account within your Office 365 DKIM-enabled domain to another email account such as outlook.com or Hotmail.com.</span></span>
    
- <span data-ttu-id="b9298-194">테스트 목적으로 aol.com 계정을 사용 하지 마십시오.</span><span class="sxs-lookup"><span data-stu-id="b9298-194">Do not use an aol.com account for testing purposes.</span></span> <span data-ttu-id="b9298-195">SPF 검사가 통과 하는 경우에는 AOL에서 DKIM 검사를 건너뛸 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b9298-195">AOL may skip the DKIM check if the SPF check passes.</span></span> <span data-ttu-id="b9298-196">이렇게 하면 테스트가 무효화 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b9298-196">This will nullify your test.</span></span>
    
- <span data-ttu-id="b9298-197">메시지를 열고 머리글을 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9298-197">Open the message and look at the header.</span></span> <span data-ttu-id="b9298-198">메시지 헤더를 확인 하는 방법은 메시징 클라이언트에 따라 다릅니다.</span><span class="sxs-lookup"><span data-stu-id="b9298-198">Instructions for viewing the header for the message will vary depending on your messaging client.</span></span> <span data-ttu-id="b9298-199">Outlook에서 메시지 헤더를 보는 방법에 대 한 자세한 내용은 [전자 메일 메시지 헤더 보기](https://support.office.com/article/CD039382-DC6E-4264-AC74-C048563D212C)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="b9298-199">For instructions on viewing message headers in Outlook, see [View e-mail message headers](https://support.office.com/article/CD039382-DC6E-4264-AC74-C048563D212C).</span></span>

  <span data-ttu-id="b9298-200">DKIM 서명 된 메시지는 CNAME 항목을 게시할 때 정의한 호스트 이름과 도메인을 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9298-200">The DKIM-signed message will contain the host name and domain you defined when you published the CNAME entries.</span></span> <span data-ttu-id="b9298-201">이 메시지는 다음과 같이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b9298-201">The message will look something like this example:</span></span> 
    
    ```
    From: Example User <example@contoso.com> 
    DKIM-Signature: v=1; a=rsa-sha256; q=dns/txt; c=relaxed/relaxed; 
        s=selector1; d=contoso.com; t=1429912795; 
        h=From:To:Message-ID:Subject:MIME-Version:Content-Type; 
        bh=<body hash>; 
        b=<signed field>;
    ```

- <span data-ttu-id="b9298-202">인증-결과 헤더를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="b9298-202">Look for the Authentication-Results header.</span></span> <span data-ttu-id="b9298-203">각 수신 서비스가 약간 다른 형식을 사용 하 여 받는 메일을 스탬프 처리 하지만이 결과에는 **dkim = pass** 또는 **dkim = OK**와 같은 내용이 포함 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9298-203">While each receiving service uses a slightly different format to stamp the incoming mail, the result should include something like **DKIM=pass** or **DKIM=OK**.</span></span> 
    
## <a name="to-configure-dkim-for-more-than-one-custom-domain-in-office-365"></a><span data-ttu-id="b9298-204">Office 365에서 둘 이상의 사용자 지정 도메인에 대해 DKIM을 구성 하려면</span><span class="sxs-lookup"><span data-stu-id="b9298-204">To configure DKIM for more than one custom domain in Office 365</span></span>
<span data-ttu-id="b9298-205"><a name="DKIMMultiDomain"> </a></span><span class="sxs-lookup"><span data-stu-id="b9298-205"></span></span>

<span data-ttu-id="b9298-206">앞으로 다른 사용자 지정 도메인을 추가 하기로 결정 하 고 새 도메인에 대해 DKIM을 사용 하도록 설정 하려는 경우에는 각 도메인에 대해이 문서의 단계를 완료 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9298-206">If at some point in the future you decide to add another custom domain and you want to enable DKIM for the new domain, you must complete the steps in this article for each domain.</span></span> <span data-ttu-id="b9298-207">특히, [Office 365에서 DKIM을 수동으로 설정 하기 위해 수행 해야](use-dkim-to-validate-outbound-email.md#SetUpDKIMO365)하는 작업에 대 한 모든 단계를 완료 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9298-207">Specifically, complete all steps in [What you need to do to manually set up DKIM in Office 365](use-dkim-to-validate-outbound-email.md#SetUpDKIMO365).</span></span>
  
## <a name="disabling-the-dkim-signing-policy-for-a-custom-domain-in-office-365"></a><span data-ttu-id="b9298-208">Office 365에서 사용자 지정 도메인에 대해 DKIM 서명 정책 사용 안 함</span><span class="sxs-lookup"><span data-stu-id="b9298-208">Disabling the DKIM signing policy for a custom domain in Office 365</span></span>
<span data-ttu-id="b9298-209"><a name="DisableDKIMSigningPolicy"> </a></span><span class="sxs-lookup"><span data-stu-id="b9298-209"></span></span>

<span data-ttu-id="b9298-210">서명 정책을 사용 하지 않도록 설정 해도 DKIM은 완전히 사용 하지 않도록 설정 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b9298-210">Disabling the signing policy does not completely disable DKIM.</span></span> <span data-ttu-id="b9298-211">일정 시간 후에 Office 365은 도메인에 대 한 기본 Office 365 정책을 자동으로 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9298-211">After a period of time, Office 365 will automatically apply the default Office 365 policy for your domain.</span></span> <span data-ttu-id="b9298-212">자세한 내용은 [DKIM 및 Office 365에 대 한 기본 동작](use-dkim-to-validate-outbound-email.md#DefaultDKIMbehavior)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="b9298-212">For more information, see [Default behavior for DKIM and Office 365](use-dkim-to-validate-outbound-email.md#DefaultDKIMbehavior).</span></span>
  
### <a name="to-disable-the-dkim-signing-policy-by-using-windows-powershell"></a><span data-ttu-id="b9298-213">Windows PowerShell을 사용 하 여 DKIM 서명 정책을 사용 하지 않도록 설정 하려면</span><span class="sxs-lookup"><span data-stu-id="b9298-213">To disable the DKIM signing policy by using Windows PowerShell</span></span>

1. <span data-ttu-id="b9298-214">[Exchange Online PowerShell에 연결합니다](https://technet.microsoft.com/library/jj984289.aspx).</span><span class="sxs-lookup"><span data-stu-id="b9298-214">[Connect to Exchange Online PowerShell](https://technet.microsoft.com/library/jj984289.aspx).</span></span>
    
2. <span data-ttu-id="b9298-215">DKIM 서명을 사용 하지 않도록 설정할 각 도메인에 대해 다음 명령 중 하나를 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9298-215">Run one of the following commands for each domain for which you want to disable DKIM signing.</span></span>
    
    ```
    $p=Get-DkimSigningConfig -identity <domain>
    $p[0] | set-DkimSigningConfig -enabled $false
    ```

   <span data-ttu-id="b9298-216">예를 들면 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="b9298-216">For example:</span></span>
    
    ```
    $p=Get-DkimSigningConfig -identity contoso.com
    $p[0] | set-DkimSigningConfig -enabled $false
    ```

   <span data-ttu-id="b9298-217">또는</span><span class="sxs-lookup"><span data-stu-id="b9298-217">Or</span></span>
    
    ```
    Set-DkimSigningConfig -identity $p[<number>].identity -enabled $false
    ```

    <span data-ttu-id="b9298-218">여기서 _number_ 는 정책의 인덱스입니다.</span><span class="sxs-lookup"><span data-stu-id="b9298-218">Where _number_ is the index of the policy.</span></span> <span data-ttu-id="b9298-219">예를 들면 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="b9298-219">For example:</span></span> 
    
    ```
    Set-DkimSigningConfig -identity $p[0].identity -enabled $false
    ```

## <a name="default-behavior-for-dkim-and-office-365"></a><span data-ttu-id="b9298-220">DKIM 및 Office 365에 대 한 기본 동작</span><span class="sxs-lookup"><span data-stu-id="b9298-220">Default behavior for DKIM and Office 365</span></span>
<span data-ttu-id="b9298-221"><a name="DefaultDKIMbehavior"> </a></span><span class="sxs-lookup"><span data-stu-id="b9298-221"></span></span>

<span data-ttu-id="b9298-222">DKIM을 사용 하도록 설정 하지 않으면 Office 365에서 사용자 지정 도메인에 대 한 1024 비트 DKIM 공개 키와 내부 데이터 센터에 저장 되는 연결 된 개인 키를 자동으로 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b9298-222">If you do not enable DKIM, Office 365 automatically creates a 1024-bit DKIM public key for your custom domain and the associated private key which we store internally in our datacenter.</span></span> <span data-ttu-id="b9298-223">기본적으로 Office 365에서는 정책이 적용 되지 않은 도메인에 대해 기본 서명 구성을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9298-223">By default, Office 365 uses a default signing configuration for domains that do not have a policy in place.</span></span> <span data-ttu-id="b9298-224">즉, DKIM을 직접 설정 하지 않으면 Office 365에서 도메인에 대해 DKIM을 사용 하기 위해 만든 기본 정책과 키를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9298-224">This means that if you do not set up DKIM yourself, Office 365 will use its default policy and keys it creates in order to enable DKIM for your domain.</span></span>
  
<span data-ttu-id="b9298-225">또한 DKIM 서명을 사용 하지 않도록 설정한 후에는 일정 기간 후 Office 365에서 도메인에 대 한 Office 365 기본 정책을 자동으로 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9298-225">Also, if you disable DKIM signing after enabling it, after a period of time, Office 365 will automatically apply the Office 365 default policy for your domain.</span></span>
  
<span data-ttu-id="b9298-226">다음 예제에서는 도메인 관리자가 아니라 fabrikam.com에 대 한 DKIM을 Office 365에서 사용 하도록 설정 했다고 가정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9298-226">In the following example, suppose that DKIM for fabrikam.com was enabled by Office 365, not by the administrator of the domain.</span></span> <span data-ttu-id="b9298-227">이는 필수 CNAMEs가 DNS에 없음을 의미 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9298-227">This means that the required CNAMEs do not exist in DNS.</span></span> <span data-ttu-id="b9298-228">이 도메인의 전자 메일에 대 한 DKIM 서명이 다음과 같이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b9298-228">DKIM signatures for email from this domain will look something like this:</span></span>
  
```
From: Second Example <second.example@fabrikam.com> 
DKIM-Signature: v=1; a=rsa-sha256; q=dns/txt; c=relaxed/relaxed; 
    s=selector1-fabrikam-com; d=contoso.onmicrosoft.com; t=1429912795; 
    h=From:To:Message-ID:Subject:MIME-Version:Content-Type; 
    bh=<body hash>; 
    b=<signed field>;
```

<span data-ttu-id="b9298-229">이 예에서 호스트 이름 및 도메인에는 fabrikam.com에 대 한 DKIM 서명이 도메인 관리자에 의해 사용 하도록 설정 된 경우 CNAME이 가리킬 값이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b9298-229">In this example, the host name and domain contain the values to which the CNAME would point if DKIM-signing for fabrikam.com had been enabled by the domain administrator.</span></span> <span data-ttu-id="b9298-230">결국 Office 365에서 전송 되는 모든 단일 메시지는 DKIM에 서명 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b9298-230">Eventually, every single message sent from Office 365 will be DKIM-signed.</span></span> <span data-ttu-id="b9298-231">DKIM을 직접 사용 하도록 설정 하는 경우 도메인은 From: 주소에서 도메인 (이 경우에는 fabrikam.com)과 동일 하 게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b9298-231">If you enable DKIM yourself, the domain will be the same as the domain in the From: address, in this case fabrikam.com.</span></span> <span data-ttu-id="b9298-232">그렇지 않은 경우에는이를 정렬 하지 않고 조직의 초기 도메인을 대신 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9298-232">If you don't, it will not align and instead will use your organization's initial domain.</span></span> <span data-ttu-id="b9298-233">초기 도메인을 결정 하는 방법에 대 한 자세한 내용은 [DOMAINS FAQ](https://support.office.com/article/1272bad0-4bd4-4796-8005-67d6fb3afc5a#bkmk_whydoihaveanonmicrosoft.comdomain)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="b9298-233">For information about determining your initial domain, see [Domains FAQ](https://support.office.com/article/1272bad0-4bd4-4796-8005-67d6fb3afc5a#bkmk_whydoihaveanonmicrosoft.comdomain).</span></span>
  
## <a name="set-up-dkim-so-that-a-third-party-service-can-send-or-spoof-email-on-behalf-of-your-custom-domain"></a><span data-ttu-id="b9298-234">타사 서비스가 사용자 지정 도메인을 대신 하 여 전자 메일을 보내거나 스푸핑할 수 있도록 DKIM을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9298-234">Set up DKIM so that a third-party service can send, or spoof, email on behalf of your custom domain</span></span>
<span data-ttu-id="b9298-235"><a name="SetUp3rdPartyspoof"> </a></span><span class="sxs-lookup"><span data-stu-id="b9298-235"></span></span>

<span data-ttu-id="b9298-236">일부 대량 전자 메일 서비스 공급자 또는 a-a-서비스 공급자를 사용 하 여 서비스에서 보낸 전자 메일에 대해 DKIM 키를 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b9298-236">Some bulk email service providers, or software-as-a-service providers, let you set up DKIM keys for email that originates from their service.</span></span> <span data-ttu-id="b9298-237">이를 위해서는 필요한 DNS 레코드를 설정 하기 위해 자신과 타사 간의 조정이 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9298-237">This requires coordination between yourself and the third-party in order to set up the necessary DNS records.</span></span> <span data-ttu-id="b9298-238">두 조직이 동일 하 게 똑같은 방식으로 작업을 수행 하지는 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b9298-238">No two organizations do it exactly the same way.</span></span> <span data-ttu-id="b9298-239">대신, 프로세스는 전적으로 조직에 따라 달라 집니다.</span><span class="sxs-lookup"><span data-stu-id="b9298-239">Instead, the process depends entirely on the organization.</span></span>
  
<span data-ttu-id="b9298-240">Contoso.com 및 bulkemailprovider.com에 대해 올바르게 구성 된 DKIM을 보여 주는 예제 메시지는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="b9298-240">An example message showing a properly configured DKIM for contoso.com and bulkemailprovider.com might look like this:</span></span>
  
```
Return-Path: <communication@bulkemailprovider.com>
 From: <sender@contoso.com>
 DKIM-Signature: s=s1024; d=contoso.com
 Subject: Here is a message from Bulk Email Provider's infrastructure, but with a DKIM signature authorized by contoso.com
```

<span data-ttu-id="b9298-241">이 예에서는 다음과 같은 결과를 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b9298-241">In this example, in order to achieve this result:</span></span>
  
1. <span data-ttu-id="b9298-242">대량 전자 메일 공급자는 Contoso에 공개 DKIM 키를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9298-242">Bulk Email Provider gave Contoso a public DKIM key.</span></span>
    
2. <span data-ttu-id="b9298-243">Contoso는 DKIM 키를 해당 DNS 레코드에 게시 했습니다.</span><span class="sxs-lookup"><span data-stu-id="b9298-243">Contoso published the DKIM key to its DNS record.</span></span>
    
3. <span data-ttu-id="b9298-244">전자 메일을 보낼 때 대량 전자 메일 공급자는 해당 개인 키를 사용 하 여 키에 서명 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9298-244">When sending email, Bulk Email Provider signs the key with the corresponding private key.</span></span> <span data-ttu-id="b9298-245">이렇게 하면 대량 전자 메일 공급자가 메시지 헤더에 DKIM 서명을 첨부 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9298-245">By doing so, Bulk Email Provider attached the DKIM signature to the message header.</span></span>
    
4. <span data-ttu-id="b9298-246">수신 전자 메일 시스템 메시지의 보낸 사람: (5322.from 주소의) 주소에서 도메인에 대해\<dkim-Signature d = 도메인\> 값을 인증 하 여 dkim 검사를 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9298-246">Receiving email systems perform a DKIM check by authenticating the DKIM-Signature d=\<domain\> value against the domain in the From: (5322.From) address of the message.</span></span> <span data-ttu-id="b9298-247">이 예에서는 값이 다음과 같이 일치 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9298-247">In this example, the values match:</span></span>
    
    <span data-ttu-id="b9298-248">보낸 사람 @**contoso.com**</span><span class="sxs-lookup"><span data-stu-id="b9298-248">sender@**contoso.com**</span></span>
    
    <span data-ttu-id="b9298-249">d =**contoso.com**</span><span class="sxs-lookup"><span data-stu-id="b9298-249">d=**contoso.com**</span></span>
    
## <a name="next-steps-after-you-set-up-dkim-for-office-365"></a><span data-ttu-id="b9298-250">다음 단계: Office 365에 대 한 DKIM을 설정한 후</span><span class="sxs-lookup"><span data-stu-id="b9298-250">Next steps: After you set up DKIM for Office 365</span></span>
<span data-ttu-id="b9298-251"><a name="DKIMNextSteps"> </a></span><span class="sxs-lookup"><span data-stu-id="b9298-251"></span></span>

<span data-ttu-id="b9298-252">DKIM은 스푸핑을 방지 하기 위해 디자인 되었지만 SPF 및 DMARC에서는 DKIM이 더 효율적으로 작동 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9298-252">Although DKIM is designed to help prevent spoofing, DKIM works better with SPF and DMARC.</span></span> <span data-ttu-id="b9298-253">DKIM을 설정한 후에 SPF를 설정 하지 않은 경우에는이 작업을 수행 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9298-253">Once you have set up DKIM, if you have not already set up SPF you should do so.</span></span> <span data-ttu-id="b9298-254">SPF에 대 한 간략 한 소개 및 신속한 구성에 대 한 자세한 내용은 [스푸핑을 방지 하기 위해 Office 365에서 spf를 설정](set-up-spf-in-office-365-to-help-prevent-spoofing.md)합니다 .를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="b9298-254">For a quick introduction to SPF and to get it configured quickly, see [Set up SPF in Office 365 to help prevent spoofing](set-up-spf-in-office-365-to-help-prevent-spoofing.md).</span></span> <span data-ttu-id="b9298-255">Office 365에서 SPF를 사용 하는 방법과 하이브리드 배포와 같은 문제 해결 또는 비표준 배포를 자세히 이해 [하려면 office 365에서 spf (Sender Policy Framework)를 사용 하 여 스푸핑을 방지](how-office-365-uses-spf-to-prevent-spoofing.md)하는 방법을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9298-255">For a more in-depth understanding of how Office 365 uses SPF, or for troubleshooting or non-standard deployments such as hybrid deployments, start with [How Office 365 uses Sender Policy Framework (SPF) to prevent spoofing](how-office-365-uses-spf-to-prevent-spoofing.md).</span></span> <span data-ttu-id="b9298-256">그런 다음 [Office 365에서 DMARC을 사용 하 여 전자 메일의 유효성 검사를](use-dmarc-to-validate-email.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="b9298-256">Next, see [Use DMARC to validate email in Office 365](use-dmarc-to-validate-email.md).</span></span> <span data-ttu-id="b9298-257">[스팸 방지 메시지 헤더](anti-spam-message-headers.md) 에는 dkim 검사에 대 한 Office 365에서 사용 하는 구문 및 헤더 필드가 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b9298-257">[Anti-spam message headers](anti-spam-message-headers.md) includes the syntax and header fields used by Office 365 for DKIM checks.</span></span> 
  

