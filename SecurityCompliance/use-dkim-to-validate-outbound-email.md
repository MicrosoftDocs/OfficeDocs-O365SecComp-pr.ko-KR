---
title: Office 365의 사용자 지정 도메인에서 전자 메일에 DKIM 사용
ms.author: tracyp
author: MSFTTracyP
manager: dansimp
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Priority
search.appverid:
- MET150
ms.assetid: 56fee1c7-dc37-470e-9b09-33fff6d94617
ms.collection:
- M365-security-compliance
description: '요약: 이 문서에서는 대상 전자 메일 시스템에서 사용자 지정 도메인에서 보낸 메시지를 신뢰하는지 확인하기 위해 Office 365에서 DomainKeys 식별 메일 (DKIM)을 사용하는 방법을 설명합니다.'
ms.openlocfilehash: d47a1e629952d65acdd9ecf05e4e521684775ae9
ms.sourcegitcommit: d4acce11a26536b9d6ca71ba4933fc95136198a4
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2019
ms.locfileid: "36407927"
---
# <a name="use-dkim-to-validate-outbound-email-sent-from-your-custom-domain-in-office-365"></a><span data-ttu-id="28be5-103">DKIM을 사용하여 Office 365의 사용자 지정 도메인에서 전송한 아웃바운드 전자 메일의 유효성을 검사합니다.</span><span class="sxs-lookup"><span data-stu-id="28be5-103">For your primary domains, Use DKIM to validate outbound email sent from your custom domain in Office 365</span></span>

 <span data-ttu-id="28be5-104">**요약:** 이 문서에서는 대상 전자 메일 시스템에서 사용자 지정 도메인에서 보낸 아웃바운드 메시지를 신뢰하는지 확인하기 위해 Office 365에서 DomainKeys 식별 메일 (DKIM)을 사용하는 방법을 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="28be5-104">**Summary:** This article describes how you use DomainKeys Identified Mail (DKIM) with Office 365 to ensure that destination email systems trust messages sent outbound from your custom domain.</span></span> 
  
<span data-ttu-id="28be5-105">SPF 및 DMARC와 함께 DKIM을 사용하여 spoofer로 하여금 사용자의 도메인에서 오는 것처럼 보이는 메시지를 보내지 못하도록 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="28be5-105">You should use DKIM in addition to SPF and DMARC to help prevent spoofers from sending messages that look like they are coming from your domain.</span></span> <span data-ttu-id="28be5-106">DKIM을 사용하면 메시지 머리글에 있는 전자 메일 메시지에 디지털 서명을 첨부할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="28be5-106">DKIM lets you add a digital signature to email messages in the message header.</span></span> <span data-ttu-id="28be5-107">복잡해 보이지만 실제로는 그렇지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="28be5-107">Sounds complicated, but it's really not.</span></span> <span data-ttu-id="28be5-108">DKIM을 구성할 때 암호화 인증을 사용하여 전자 메일 메시지에 해당 이름을 연결하거나 서명할 수 있는 권한을 도메인에 부여합니다.</span><span class="sxs-lookup"><span data-stu-id="28be5-108">When you configure DKIM, you authorize your domain to associate, or sign, its name to an email message by using cryptographic authentication.</span></span> <span data-ttu-id="28be5-109">사용자의 도메인으로부터 전자 메일을 수신하는 전자 메일 시스템에서는 이 디지털 서명을 사용하여 수신하는 전자 메일이 합법적인지 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="28be5-109">Email systems that receive email from your domain can use this digital signature to help determine if incoming email that they receive is legitimate.</span></span>
  
<span data-ttu-id="28be5-110">기본적으로 개인 키를 사용하여 사용자의 도메인의 보내는 전자 메일에서 머리글을 암호화 합니다.</span><span class="sxs-lookup"><span data-stu-id="28be5-110">Basically, you use a private key to encrypt the header in your domain's outgoing email.</span></span> <span data-ttu-id="28be5-111">사용자의 DNS 레코드에 공개 키를 게시하면 수신하는 서버에서 이를 이용하여 서명을 디코딩하는 데 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="28be5-111">You publish a public key to your domain's DNS records that receiving servers can then use to decode the signature.</span></span> <span data-ttu-id="28be5-112">공개 키를 사용하여 메시지가 실제로 사용자로부터 온 것인지 도메인을 스푸핑한 사람에게서 온 것이 아닌지 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="28be5-112">They use the public key to verify that the messages are really coming from you and not coming from someone spoofing your domain.</span></span>
  
<span data-ttu-id="28be5-113">Office 365는 초기 도메인에 대해 DKIM을 자동으로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="28be5-113">Office 365 automatically sets up DKIM for initial domains.</span></span> <span data-ttu-id="28be5-114">초기 도메인은 서비스에 가입할 때 Office 365가 사용자를 위해 만든 도메인입니다 (예: contoso.onmicrosoft.com).</span><span class="sxs-lookup"><span data-stu-id="28be5-114">The initial domain is the domain that Office 365 created for you when you signed up with the service, for example, contoso.onmicrosoft.com.</span></span> <span data-ttu-id="28be5-115">초기 도메인에 대해 DKIM을 설정하기 위해 별도의 작업을 수행할 필요가 없습니다.</span><span class="sxs-lookup"><span data-stu-id="28be5-115">You don't need to do anything to set up DKIM for your initial domain.</span></span> <span data-ttu-id="28be5-116">도메인에 대한 자세한 내용은 [도메인 FAQ](https://support.office.com/article/Domains-FAQ-1272bad0-4bd4-4796-8005-67d6fb3afc5a#bkmk_whydoihaveanonmicrosoft.comdomain)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="28be5-116">For more information about external relay domains, see [Accepted Domains](https://support.office.com/article/Domains-FAQ-1272bad0-4bd4-4796-8005-67d6fb3afc5a#bkmk_whydoihaveanonmicrosoft.comdomain).</span></span>
  
<span data-ttu-id="28be5-117">사용자 지정 도메인의 DKIM에 대해서 아무 것도 수행하지 않도록 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="28be5-117">You can choose to do nothing about DKIM for your custom domain too.</span></span> <span data-ttu-id="28be5-118">사용자 지정 도메인에 DKIM을 설정하지 않으면 Office 365는 개인 및 공개 키 쌍을 만들고 DKIM 서명을 사용하도록 설정 한 다음 사용자 지정 도메인에 대한 Office 365 기본 정책을 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="28be5-118">If you do not set up DKIM for your custom domain, Office 365 creates a private and public key pair, enables DKIM signing, and then configures the Office 365 default policy for your custom domain.</span></span> <span data-ttu-id="28be5-119">대부분의 Office 365 고객에게는 이 기능으로 충분하지만 다음과 같은 경우에는 사용자 지정 도메인에 대해 DKIM을 수동으로 구성해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="28be5-119">While this is sufficient coverage for most Office 365 customers, you should manually configure DKIM for your custom domain in the following circumstances:</span></span>
  
- <span data-ttu-id="28be5-120">Office 365에 두 개 이상의 사용자 지정 도메인이 있는 경우</span><span class="sxs-lookup"><span data-stu-id="28be5-120">You have more than one custom domain in Office 365</span></span>
    
- <span data-ttu-id="28be5-121">DMARC 또한 설정하려는 경우 (권장됨)</span><span class="sxs-lookup"><span data-stu-id="28be5-121">You're going to set up DMARC too (recommended)</span></span>
    
- <span data-ttu-id="28be5-122">개인 키를 제어하려는 경우</span><span class="sxs-lookup"><span data-stu-id="28be5-122">You want control over your private key</span></span>
    
- <span data-ttu-id="28be5-123">CNAME 레코드를 사용자 지정하려는 경우</span><span class="sxs-lookup"><span data-stu-id="28be5-123">You want to customize your CNAME records</span></span>
    
- <span data-ttu-id="28be5-124">타사 대량 메일 프로그램을 사용하는 경우와 같이 타사 도메인에서 시작되는 전자 메일에 대해 DKIM 키를 설정하려는 경우</span><span class="sxs-lookup"><span data-stu-id="28be5-124">You want to set up DKIM keys for email originating out of a third-party domain, for example, if you use a third-party bulk mailer.</span></span>
    
<span data-ttu-id="28be5-125">이 문서의 내용:</span><span class="sxs-lookup"><span data-stu-id="28be5-125">In this article:</span></span>
  
- [<span data-ttu-id="28be5-126">Office 365에서 악의적인 스푸핑을 방지하기 위해 DKIM이 SPF 단독보다 더욱 효율적인 방식인 이유</span><span class="sxs-lookup"><span data-stu-id="28be5-126">How DKIM works better than SPF alone to prevent malicious spoofing in Office 365</span></span>](use-dkim-to-validate-outbound-email.md#HowDKIMWorks)
    
- [<span data-ttu-id="28be5-127">Office 365에서 DKIM을 직접 설정하는 데 필요한 사항</span><span class="sxs-lookup"><span data-stu-id="28be5-127">What you need to do to manually set up DKIM in Office 365</span></span>](use-dkim-to-validate-outbound-email.md#SetUpDKIMO365)
    
- [<span data-ttu-id="28be5-128">Office 365에서 두 개 이상의 사용자 지정 도메인에 대해 DKIM을 구성</span><span class="sxs-lookup"><span data-stu-id="28be5-128">To configure DKIM for more than one custom domain in Office 365</span></span>](use-dkim-to-validate-outbound-email.md#DKIMMultiDomain)
    
- [<span data-ttu-id="28be5-129">Office 365에서 사용자 지정 도메인에 대해 DKIM 서명 정책을 사용 하지 않도록 설정</span><span class="sxs-lookup"><span data-stu-id="28be5-129">Disabling the DKIM signing policy for a custom domain in Office 365</span></span>](use-dkim-to-validate-outbound-email.md#DisableDKIMSigningPolicy)
    
- [<span data-ttu-id="28be5-130">DKIM 및 Office 365의 기본 동작</span><span class="sxs-lookup"><span data-stu-id="28be5-130">Default behavior for DKIM and Office 365</span></span>](use-dkim-to-validate-outbound-email.md#DefaultDKIMbehavior)
    
- [<span data-ttu-id="28be5-131">타사 서비스에서 사용자 지정 도메인을 대신하여 이메일을 보내거나 스푸핑할 수 있도록 DKIM을 설정</span><span class="sxs-lookup"><span data-stu-id="28be5-131">Set up DKIM so that a third-party service can send, or spoof, email on behalf of your custom domain</span></span>](use-dkim-to-validate-outbound-email.md#SetUp3rdPartyspoof)
    
- [<span data-ttu-id="28be5-132">다음 단계: Office 365에 대한 DKIM을 설정한 후</span><span class="sxs-lookup"><span data-stu-id="28be5-132">Next steps: After you set up DKIM for Office 365</span></span>](use-dkim-to-validate-outbound-email.md#DKIMNextSteps)
    
## <a name="how-dkim-works-better-than-spf-alone-to-prevent-malicious-spoofing-in-office-365"></a><span data-ttu-id="28be5-133">Office 365에서 악의적인 스푸핑을 방지하기 위해 DKIM이 SPF 단독보다 더욱 효율적인 방식인 이유</span><span class="sxs-lookup"><span data-stu-id="28be5-133">How DKIM works better than SPF alone to prevent malicious spoofing in Office 365</span></span>
<span data-ttu-id="28be5-134"><a name="HowDKIMWorks"> </a></span><span class="sxs-lookup"><span data-stu-id="28be5-134"></span></span>

<span data-ttu-id="28be5-135">SPF는 메시지 봉투에 정보를 추가하지만 DKIM은 실제로 메시지 머리글 내에서 서명을 암호화 합니다.</span><span class="sxs-lookup"><span data-stu-id="28be5-135">SPF adds information to a message envelope but DKIM actually encrypts a signature within the message header.</span></span> <span data-ttu-id="28be5-136">메시지를 전달할 때 메시지의 봉투 일부가 전달 서버에서 제거될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="28be5-136">When you forward a message, portions of that message's envelope can be stripped away by the forwarding server.</span></span> <span data-ttu-id="28be5-137">디지털 서명은 전자 메일 머리글의 일부이기 때문에 전자 메일 메시지와 함께 유지되므로 DKIM은 다음 예제와 같이 메시지가 전달된 경우에도 작동합니다.</span><span class="sxs-lookup"><span data-stu-id="28be5-137">Since the digital signature stays with the email message because it's part of the email header, DKIM works even when a message has been forwarded as shown in the following example.</span></span>
  
![SPF 확인이 실패하는 경우 DKIM 인증을 제공하는 전달된 메시지를 보여주는 다이어그램](media/28f93b4c-97e7-4309-acc4-fd0d2e0e3377.jpg)
  
<span data-ttu-id="28be5-139">이 예제에서 도메인에 대한 SPF TXT 레코드만 게시한 경우 받는 사람의 메일 서버에서 전자 메일을 스팸으로 표시하고 가양성 결과를 생성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="28be5-139">In this example, if you had only published an SPF TXT record for your domain, the recipient's mail server could have marked your email as spam and generated a false positive result.</span></span> <span data-ttu-id="28be5-140">이 시나리오에 DKIM을 추가하면 가양성 스팸 보고를 줄일 수가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="28be5-140">The addition of DKIM in this scenario reduces false positive spam reporting.</span></span> <span data-ttu-id="28be5-141">DKIM은 IP 주소뿐만 아니라 인증을 위해 공개 키 암호화를 사용하기 때문에 DKIM은 SPF보다 훨씬 강력한 인증 형식으로 간주됩니다.</span><span class="sxs-lookup"><span data-stu-id="28be5-141">Because DKIM relies on public key cryptography to authenticate and not just IP addresses, DKIM is considered a much stronger form of authentication than SPF.</span></span> <span data-ttu-id="28be5-142">배포시 SPF 및 DKIM과 DMARC를 모두 사용하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="28be5-142">We recommend using both SPF and DKIM, as well as DMARC in your deployment.</span></span>
  
<span data-ttu-id="28be5-143">핵심: DKIM은 개인 키를 사용하여 암호화 된 서명을 메시지 머리글에 삽입합니다.</span><span class="sxs-lookup"><span data-stu-id="28be5-143">The nitty gritty: DKIM uses a private key to insert an encrypted signature into the message headers.</span></span> <span data-ttu-id="28be5-144">서명 도메인 또는 아웃 바운드 도메인이 머리글의 **d =** 필드 값으로 삽입됩니다.</span><span class="sxs-lookup"><span data-stu-id="28be5-144">The signing domain, or outbound domain, is inserted as the value of the **d=** field in the header.</span></span> <span data-ttu-id="28be5-145">확인 도메인 또는 수신자 도메인은 **d =** 필드를 사용하여 DNS에서 공개 키를 조회하고 메시지를 인증합니다.</span><span class="sxs-lookup"><span data-stu-id="28be5-145">The verifying domain, or recipient's domain, then use the **d=** field to look up the public key from DNS and authenticate the message.</span></span> <span data-ttu-id="28be5-146">메시지를 확인하면 DKIM 검사가 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="28be5-146">If the message is verified, the DKIM check passes.</span></span> 
  
## <a name="what-you-need-to-do-to-manually-set-up-dkim-in-office-365"></a><span data-ttu-id="28be5-147">Office 365에서 DKIM을 직접 설정하는 데 필요한 사항</span><span class="sxs-lookup"><span data-stu-id="28be5-147">What you need to do to manually set up DKIM in Office 365</span></span>
<span data-ttu-id="28be5-148"><a name="SetUpDKIMO365"> </a></span><span class="sxs-lookup"><span data-stu-id="28be5-148"></span></span>

<span data-ttu-id="28be5-149">DKIM을 구성하려면 다음 단계를 수행합니다.</span><span class="sxs-lookup"><span data-stu-id="28be5-149">To configure DKIM, you will complete these steps:</span></span>
  
- [<span data-ttu-id="28be5-150">DNS에서 사용자 지정 도메인에 대해 두 개의 CNAME 레코드 게시</span><span class="sxs-lookup"><span data-stu-id="28be5-150">Publish two CNAME records for your custom domain in DNS</span></span>](use-dkim-to-validate-outbound-email.md#Publish2CNAME)
    
- [<span data-ttu-id="28be5-151">Office 365에서 사용자 지정 도메인에 DKIM 서명 사용</span><span class="sxs-lookup"><span data-stu-id="28be5-151">Enable DKIM signing for your custom domain in Office 365</span></span>](use-dkim-to-validate-outbound-email.md#EnableDKIMinO365)
    
### <a name="publish-two-cname-records-for-your-custom-domain-in-dns"></a><span data-ttu-id="28be5-152">DNS에서 사용자 지정 도메인에 대해 두 개의 CNAME 레코드 게시</span><span class="sxs-lookup"><span data-stu-id="28be5-152">Publish two CNAME records for your custom domain in DNS</span></span>
<span data-ttu-id="28be5-153"><a name="Publish2CNAME"> </a></span><span class="sxs-lookup"><span data-stu-id="28be5-153"></span></span>

<span data-ttu-id="28be5-154">DNS에 DKIM 서명을 추가하려는 각 도메인에 대해 두 개의 CNAME 레코드를 게시해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="28be5-154">For each domain for which you want to add a DKIM signature in DNS, you need to publish two CNAME records.</span></span> 

<span data-ttu-id="28be5-155">다음 명령을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="28be5-155">Run the following command:</span></span>    
   
    New-DkimSigningConfig -DomainName <domain> -Enabled $false
       
    Get-DkimSigningConfig -DomainName domain | fl Selector1CNAME, Selector2CNAME
    
<span data-ttu-id="28be5-156">Get-DkimSigningConfig 출력에서 참조되는 CNAME 만들기</span><span class="sxs-lookup"><span data-stu-id="28be5-156">Create CNAMEs referenced in Get-DkimSigningConfig output</span></span>
    
    Set-DkimSigningConfig -DomainName domain -Enabled $true
    
<span data-ttu-id="28be5-157">DNS의 CNAME 레코드는 Office 365용 Microsoft DNS 서버의 DNS에 생성되어 이미 존재하는 A 레코드를 가리킵니다.</span><span class="sxs-lookup"><span data-stu-id="28be5-157">The CNAME records in your DNS will point to already created A records that exist in DNS on the Microsoft DNS servers for Office 365.</span></span>
  
<span data-ttu-id="28be5-158">Office 365는 사용자가 설정한 두 개의 레코드를 사용하여 자동 키 순환을 수행합니다.</span><span class="sxs-lookup"><span data-stu-id="28be5-158">Office 365 performs automatic key rotation using the two records that you establish.</span></span> <span data-ttu-id="28be5-159">Office 365의 초기 도메인 외에 사용자 지정 도메인을 프로비저닝한 경우에는 추가 도메인마다 두 개의 CNAME 레코드를 게시해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="28be5-159">If you have provisioned custom domains in addition to the initial domain in Office 365, you must publish two CNAME records for each additional domain.</span></span> <span data-ttu-id="28be5-160">따라서 두 개의 도메인이 있는 경우 두 개의 CNAME 레코드를 모두 게시해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="28be5-160">So, if you have two domains, you must publish two additional CNAME records, and so on.</span></span>
  
<span data-ttu-id="28be5-161">CNAME 레코드에는 다음 형식을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="28be5-161">Use the following format for the CNAME records.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="28be5-162">사용자가 GCC High 고객인 경우 _domainGuid_를 다르게 계산합니다!</span><span class="sxs-lookup"><span data-stu-id="28be5-162">If you are one of our GCC High customers, we calculate _domainGuid_ differently!</span></span> <span data-ttu-id="28be5-163">_domainGuid_를 계산하기 위해 _initialDomain_에 대한 MX 레코드를 조회하는 대신 사용자 정의된 도메인에서 직접 계산합니다.</span><span class="sxs-lookup"><span data-stu-id="28be5-163">Instead of looking up the MX record for your _initialDomain_ to calculate _domainGuid_, instead we calculate it directly from the customized domain.</span></span> <span data-ttu-id="28be5-164">예를 들어, 사용자 지정 도메인이 "contoso.com"인 경우 domainGuid는 "contoso-com"이되고 마침표는 대시로 바뀝니다.</span><span class="sxs-lookup"><span data-stu-id="28be5-164">For example, if your customized domain is “contoso.com” your domainGuid becomes “contoso-com”, any periods are replaced with a dash.</span></span> <span data-ttu-id="28be5-165">따라서 initialDomain이 가리키는 MX 레코드와 상관없이 항상 위의 방법을 사용하여 CNAME 레코드에서 사용할 domainGuid를 계산합니다.</span><span class="sxs-lookup"><span data-stu-id="28be5-165">So, regardless of what MX record your initialDomain points to, you’ll always use the above method to calculate the domainGuid to use in your CNAME records.</span></span>

  
```
Host name:          selector1._domainkey
Points to address or value: selector1-<domainGUID>._domainkey.<initialDomain> 
TTL:                3600

Host name:          selector2._domainkey
Points to address or value: selector2-<domainGUID>._domainkey.<initialDomain> 
TTL:                3600
```

<span data-ttu-id="28be5-166">여기서,</span><span class="sxs-lookup"><span data-stu-id="28be5-166">Where:</span></span>
  
- <span data-ttu-id="28be5-167">Office 365의 경우 셀렉터는 항상 "selector1" 또는 "selector2"입니다.</span><span class="sxs-lookup"><span data-stu-id="28be5-167">For Office 365, the selectors will always be "selector1" or "selector2".</span></span> 
    
- <span data-ttu-id="28be5-168">_domainGUID_는 mail.protection.outlook.com 이전에 표시되는 사용자 정의 도메인에 대한 사용자 정의된 MX 레코드의 _domainGUID_와 동일합니다.</span><span class="sxs-lookup"><span data-stu-id="28be5-168">_domainGUID_ is the same as the _domainGUID_ in the customized MX record for your custom domain that appears before mail.protection.outlook.com.</span></span> <span data-ttu-id="28be5-169">예를 들어 도메인 contoso.com에 대한 다음 MX 레코드에서 _domainGUID_는 contoso-com입니다.</span><span class="sxs-lookup"><span data-stu-id="28be5-169">For example, in the following MX record for the domain contoso.com, the _domainGUID_ is contoso-com:</span></span> 
    
    ```
    contoso.com.  3600  IN  MX   5 contoso-com.mail.protection.outlook.com
    ```

- <span data-ttu-id="28be5-170">_initialdomain_ 은 Office 365에 등록할 때 사용한 도메인입니다.</span><span class="sxs-lookup"><span data-stu-id="28be5-170">_initialDomain_ is the domain that you used when you signed up for Office 365.</span></span> <span data-ttu-id="28be5-171">초기 도메인은 항상 onmicrosoft.com으로 끝납니다.</span><span class="sxs-lookup"><span data-stu-id="28be5-171">Initial domains always end in onmicrosoft.com.</span></span> <span data-ttu-id="28be5-172">초기 도메인을 확인하는 방법에 대한 자세한 내용은 [도메인 FAQ](https://support.office.com/article/1272bad0-4bd4-4796-8005-67d6fb3afc5a#bkmk_whydoihaveanonmicrosoft.comdomain)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="28be5-172">For information about determining your initial domain, see [Domains FAQ](https://support.office.com/article/1272bad0-4bd4-4796-8005-67d6fb3afc5a#bkmk_whydoihaveanonmicrosoft.comdomain).</span></span>
    
<span data-ttu-id="28be5-173">예를 들어 cohovineyardandwinery.onmicrosoft.com이라는 초기 도메인과 cohovineyard.com 및 cohowinery.com이라는 두 개의 사용자 지정 도메인이 있는 경우 추가 도메인마다 총 두 개의 CNAME 레코드를 설정해야 합니다 (총 네 개의 CNAME 레코드).</span><span class="sxs-lookup"><span data-stu-id="28be5-173">For example, if you have an initial domain of cohovineyardandwinery.onmicrosoft.com, and two custom domains cohovineyard.com and cohowinery.com, you would need to set up two CNAME records for each additional domain, for a total of four CNAME records.</span></span>
  
```
Host name:          selector1._domainkey
Points to address or value: selector1-cohovineyard-com._domainkey.cohovineyardandwinery.onmicrosoft.com
TTL:                3600

Host name:          selector2._domainkey
Points to address or value: selector2-cohovineyard-com._domainkey.cohovineyardandwinery.onmicrosoft.com
TTL:                3600

Host name:          selector1._domainkey
Points to address or value: selector1-cohowinery-com._domainkey.cohovineyardandwinery.onmicrosoft.com 
TTL:                3600
 
Host name:          selector2._domainkey
Points to address or value: selector2-cohowinery-com._domainkey.cohovineyardandwinery.onmicrosoft.com 
TTL:                3600
```

### <a name="enable-dkim-signing-for-your-custom-domain-in-office-365"></a><span data-ttu-id="28be5-174">Office 365에서 사용자 지정 도메인에 DKIM 서명 사용</span><span class="sxs-lookup"><span data-stu-id="28be5-174">Enable DKIM signing for your custom domain in Office 365</span></span>
<span data-ttu-id="28be5-175"><a name="EnableDKIMinO365"> </a></span><span class="sxs-lookup"><span data-stu-id="28be5-175"></span></span>

<span data-ttu-id="28be5-176">CNAME 레코드를 DNS에 게시하면 Office 365를 통해 DKIM 서명을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="28be5-176">Once you have published the CNAME records in DNS, you are ready to enable DKIM signing through Office 365.</span></span> <span data-ttu-id="28be5-177">Microsoft 365 관리 센터 또는 PowerShell을 사용하여 이 작업을 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="28be5-177">You can do this either through the Microsoft 365 admin center or by using PowerShell.</span></span>
  
#### <a name="to-enable-dkim-signing-for-your-custom-domain-through-the-admin-center"></a><span data-ttu-id="28be5-178">관리 센터를 통해 사용자 지정 도메인에 DKIM 서명 사용</span><span class="sxs-lookup"><span data-stu-id="28be5-178">To enable DKIM signing for your custom domain through the admin center</span></span>

1. <span data-ttu-id="28be5-179">회사 또는 학교 계정으로 [Office 365에 로그인](https://support.office.microsoft.com/article/e9eb7d51-5430-4929-91ab-6157c5a050b4)합니다.</span><span class="sxs-lookup"><span data-stu-id="28be5-179">[Sign in to Office 365](https://support.office.microsoft.com/article/e9eb7d51-5430-4929-91ab-6157c5a050b4) with your work or school account.</span></span> 
    
2. <span data-ttu-id="28be5-180">왼쪽 위에서 앱 시작 관리자 아이콘을 선택하고 **관리자**를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="28be5-180">Select the app launcher icon in the upper-left and choose **Admin**.</span></span>
    
3. <span data-ttu-id="28be5-181">왼쪽 아래 탐색에서 **관리자**를 확장하고 **Exchange**를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="28be5-181">In the lower-left navigation, expand **Admin** and choose **Compliance**.</span></span>
    
4. <span data-ttu-id="28be5-182">**보호**\>**dkim**으로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="28be5-182">Go to **Protection** \> **dkim**.</span></span>
    
5. <span data-ttu-id="28be5-183">DKIM을 활성화 할 도메인을 선택한 다음 **DKIM 서명을 사용하여 이 도메인의 메시지 서명**에 대해 **활성화**를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="28be5-183">Select the domain for which you want to enable DKIM and then, for **Sign messages for this domain with DKIM signatures**, choose **Enable**.</span></span> <span data-ttu-id="28be5-184">각 사용자 지정 도메인에 대해 이 단계를 반복합니다.</span><span class="sxs-lookup"><span data-stu-id="28be5-184">Repeat this step for each custom domain.</span></span>
    
#### <a name="to-enable-dkim-signing-for-your-custom-domain-by-using-powershell"></a><span data-ttu-id="28be5-185">PowerShell을 사용하여 사용자 지정 도메인에 DKIM 서명 사용</span><span class="sxs-lookup"><span data-stu-id="28be5-185">To enable DKIM signing for your custom domain by using PowerShell</span></span>

1. <span data-ttu-id="28be5-186">[Exchange Online PowerShell에 연결합니다](https://technet.microsoft.com/library/jj984289.aspx).</span><span class="sxs-lookup"><span data-stu-id="28be5-186">[Connect to Exchange Online PowerShell](https://technet.microsoft.com/library/jj984289.aspx).</span></span>
    
2. <span data-ttu-id="28be5-187">다음 명령을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="28be5-187">Run the following command:</span></span>
    
    ```
    Set-DkimSigningConfig -DomainName <domain> -Enabled $true
    ```

   <span data-ttu-id="28be5-188">여기서 _도메인_은 DKIM 서명을 활성화하려는 사용자 지정 도메인의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="28be5-188">Where _domain_ is the name of the custom domain that you want to enable DKIM signing for.</span></span> 
    
   <span data-ttu-id="28be5-189">예를 들어 contoso.com 도메인의 경우</span><span class="sxs-lookup"><span data-stu-id="28be5-189">This example uses a specific certificate for the domain contoso.com.</span></span>
    
    ```
    Set-DkimSigningConfig -DomainName contoso.com -Enabled $true
    ```

#### <a name="to-confirm-dkim-signing-is-configured-properly-for-office-365"></a><span data-ttu-id="28be5-190">Office 365에 DKIM 서명이 올바르게 구성되어 있는지 확인하려면</span><span class="sxs-lookup"><span data-stu-id="28be5-190">To Confirm DKIM signing is configured properly for Office 365</span></span>

<span data-ttu-id="28be5-191">다음 단계를 수행하여 DKIM을 올바르게 구성했는지 확인하기 전에 몇 분 정도 기다립니다.</span><span class="sxs-lookup"><span data-stu-id="28be5-191">Wait a few minutes before you follow these steps to confirm that you have properly configured DKIM.</span></span> <span data-ttu-id="28be5-192">이를 통해 도메인에 대한 DKIM 정보가 네트워크 전체에 전파될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="28be5-192">This allows time for the DKIM information about the domain to be spread throughout the network.</span></span>
  
- <span data-ttu-id="28be5-193">Office 365 DKIM 사용 가능한 도메인 내의 계정에서 outlook.com 또는 Hotmail.com과 같은 다른 전자 메일 계정으로 메시지를 보냅니다.</span><span class="sxs-lookup"><span data-stu-id="28be5-193">Send a message from an account within your Office 365 DKIM-enabled domain to another email account such as outlook.com or Hotmail.com.</span></span>
    
- <span data-ttu-id="28be5-194">테스트 목적으로 aol.com 계정을 사용하지 마세요.</span><span class="sxs-lookup"><span data-stu-id="28be5-194">Do not use an aol.com account for testing purposes.</span></span> <span data-ttu-id="28be5-195">SPF 검사가 통과되면 AOL에서 DKIM 검사를 건너뛸 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="28be5-195">AOL may skip the DKIM check if the SPF check passes.</span></span> <span data-ttu-id="28be5-196">이렇게 하면 테스트가 무효화 됩니다.</span><span class="sxs-lookup"><span data-stu-id="28be5-196">This will nullify your test.</span></span>
    
- <span data-ttu-id="28be5-197">메시지를 열고 머리글을 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="28be5-197">Open the message and look at the header.</span></span> <span data-ttu-id="28be5-198">메시지 머리글 보기에 대한 지침은 메시징 클라이언트에 따라 다릅니다.</span><span class="sxs-lookup"><span data-stu-id="28be5-198">Instructions for viewing the header for the message will vary depending on your messaging client.</span></span> <span data-ttu-id="28be5-199">Outlook에서 메시지 머리글을 보는 방법은 [전자 메일 메시지 머리글보기](https://support.office.com/article/CD039382-DC6E-4264-AC74-C048563D212C)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="28be5-199">For instructions on viewing message headers in Outlook, see [View e-mail message headers](https://support.office.com/article/CD039382-DC6E-4264-AC74-C048563D212C).</span></span>

  <span data-ttu-id="28be5-200">DKIM 서명 메시지에는 CNAME 항목을 게시할 때 정의한 호스트 이름과 도메인이 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="28be5-200">The DKIM-signed message will contain the host name and domain you defined when you published the CNAME entries.</span></span> <span data-ttu-id="28be5-201">메시지가 다음 예제와 같이 표시됩니다. </span><span class="sxs-lookup"><span data-stu-id="28be5-201">The message will look something like this example:</span></span> 
    
    ```
    From: Example User <example@contoso.com> 
    DKIM-Signature: v=1; a=rsa-sha256; q=dns/txt; c=relaxed/relaxed; 
        s=selector1; d=contoso.com; t=1429912795; 
        h=From:To:Message-ID:Subject:MIME-Version:Content-Type; 
        bh=<body hash>; 
        b=<signed field>;
    ```

- <span data-ttu-id="28be5-202">Authentication-Results 머리글을 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="28be5-202">Look for the Authentication-Results header.</span></span> <span data-ttu-id="28be5-203">각 수신 서비스는 수신 메일을 스탬프 처리하기 위해 약간씩 다른 형식을 사용하지만 결과에는 **DKIM=pass** 또는 **DKIM=OK**가 포함되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="28be5-203">While each receiving service uses a slightly different format to stamp the incoming mail, the result should include something like **DKIM=pass** or **DKIM=OK**.</span></span> 
    
## <a name="to-configure-dkim-for-more-than-one-custom-domain-in-office-365"></a><span data-ttu-id="28be5-204">Office 365에서 두 개 이상의 사용자 지정 도메인에 대해 DKIM을 구성</span><span class="sxs-lookup"><span data-stu-id="28be5-204">To configure DKIM for more than one custom domain in Office 365</span></span>
<span data-ttu-id="28be5-205"><a name="DKIMMultiDomain"> </a></span><span class="sxs-lookup"><span data-stu-id="28be5-205"></span></span>

<span data-ttu-id="28be5-206">나중에 다른 사용자 지정 도메인을 추가하기로 결정하고 새 도메인에 대해 DKIM을 활성화하려는 경우 각 도메인에 대해 이 문서의 단계를 완료해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="28be5-206">If at some point in the future you decide to add another custom domain and you want to enable DKIM for the new domain, you must complete the steps in this article for each domain.</span></span> <span data-ttu-id="28be5-207">특히 [Office 365에서 DKIM을 수동으로 설정하려면 수행해야 할 작업](use-dkim-to-validate-outbound-email.md#SetUpDKIMO365)의 모든 단계를 완료합니다.</span><span class="sxs-lookup"><span data-stu-id="28be5-207">Specifically, complete all steps in [What you need to do to manually set up DKIM in Office 365](use-dkim-to-validate-outbound-email.md#SetUpDKIMO365).</span></span>
  
## <a name="disabling-the-dkim-signing-policy-for-a-custom-domain-in-office-365"></a><span data-ttu-id="28be5-208">Office 365에서 사용자 지정 도메인에 대해 DKIM 서명 정책을 사용 하지 않도록 설정</span><span class="sxs-lookup"><span data-stu-id="28be5-208">Disabling the DKIM signing policy for a custom domain in Office 365</span></span>
<span data-ttu-id="28be5-209"><a name="DisableDKIMSigningPolicy"> </a></span><span class="sxs-lookup"><span data-stu-id="28be5-209"></span></span>

<span data-ttu-id="28be5-210">서명 정책을 비활성화해도 DKIM이 완전히 비활성화되지는 않습니다.</span><span class="sxs-lookup"><span data-stu-id="28be5-210">Disabling the signing policy does not completely disable DKIM.</span></span> <span data-ttu-id="28be5-211">일정 시간이 지나면 Office 365는 도메인에 대한 기본 Office 365 정책을 자동으로 적용합니다.</span><span class="sxs-lookup"><span data-stu-id="28be5-211">After a period of time, Office 365 will automatically apply the default Office 365 policy for your domain.</span></span> <span data-ttu-id="28be5-212">자세한 내용은 [DKIM 및 Office 365의 기본 동작](use-dkim-to-validate-outbound-email.md#DefaultDKIMbehavior)을 참조합니다.</span><span class="sxs-lookup"><span data-stu-id="28be5-212">For more information, see [Default behavior for DKIM and Office 365](use-dkim-to-validate-outbound-email.md#DefaultDKIMbehavior).</span></span>
  
### <a name="to-disable-the-dkim-signing-policy-by-using-windows-powershell"></a><span data-ttu-id="28be5-213">Windows PowerShell을 사용하여 DKIM 서명 정책을 비활성화하려면</span><span class="sxs-lookup"><span data-stu-id="28be5-213">To disable the DKIM signing policy by using Windows PowerShell</span></span>

1. <span data-ttu-id="28be5-214">[Exchange Online PowerShell에 연결합니다](https://technet.microsoft.com/library/jj984289.aspx).</span><span class="sxs-lookup"><span data-stu-id="28be5-214">[Connect to Exchange Online PowerShell](https://technet.microsoft.com/library/jj984289.aspx).</span></span>
    
2. <span data-ttu-id="28be5-215">DKIM 서명을 비활성화하려는 각 도메인에 대해 다음 명령 중 하나를 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="28be5-215">Run one of the following commands for each domain for which you want to disable DKIM signing.</span></span>
    
    ```
    $p=Get-DkimSigningConfig -identity <domain>
    $p[0] | set-DkimSigningConfig -enabled $false
    ```

   <span data-ttu-id="28be5-216">예:</span><span class="sxs-lookup"><span data-stu-id="28be5-216">For example:</span></span>
    
    ```
    $p=Get-DkimSigningConfig -identity contoso.com
    $p[0] | set-DkimSigningConfig -enabled $false
    ```

   <span data-ttu-id="28be5-217">또는</span><span class="sxs-lookup"><span data-stu-id="28be5-217">Or</span></span>
    
    ```
    Set-DkimSigningConfig -identity $p[<number>].identity -enabled $false
    ```

    <span data-ttu-id="28be5-218">여기에서 _numbe_r는 정책의 인덱스입니다.</span><span class="sxs-lookup"><span data-stu-id="28be5-218">Where _number_ is the index of the policy.</span></span> <span data-ttu-id="28be5-219">예:</span><span class="sxs-lookup"><span data-stu-id="28be5-219">For example:</span></span> 
    
    ```
    Set-DkimSigningConfig -identity $p[0].identity -enabled $false
    ```

## <a name="default-behavior-for-dkim-and-office-365"></a><span data-ttu-id="28be5-220">DKIM 및 Office 365의 기본 동작</span><span class="sxs-lookup"><span data-stu-id="28be5-220">Default behavior for DKIM and Office 365</span></span>
<span data-ttu-id="28be5-221"><a name="DefaultDKIMbehavior"> </a></span><span class="sxs-lookup"><span data-stu-id="28be5-221"></span></span>

<span data-ttu-id="28be5-222">DKIM을 사용하지 않도록 설정하면 Office 365는 기본 도메인에 대해 1024 비트 DKIM 공개 키와 데이터 센터에 내부적으로 저장되는 관련 개인 키를 자동으로 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="28be5-222">If you do not enable DKIM, Office 365 automatically creates a 1024-bit DKIM public key for your default domain and the associated private key which we store internally in our datacenter.</span></span> <span data-ttu-id="28be5-223">기본적으로 Office 365는 정책이 없는 도메인에 대해 기본 서명 구성을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="28be5-223">By default, Office 365 uses a default signing configuration for domains that do not have a policy in place.</span></span> <span data-ttu-id="28be5-224">즉, DKIM을 직접 설정하지 않으면 Office 365는 도메인에 DKIM을 사용하기 위해 만든 기본 정책과 키를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="28be5-224">This means that if you do not set up DKIM yourself, Office 365 will use its default policy and keys it creates in order to enable DKIM for your domain.</span></span>
  
<span data-ttu-id="28be5-225">또한 DKIM 서명을 사용하도록 설정 한 후 다시 사용하지 않도록 설정할 경우 일정 시간이 지나면 Office 365가 도메인에 대해 Office 365 기본 정책을 자동으로 적용합니다.</span><span class="sxs-lookup"><span data-stu-id="28be5-225">Also, if you disable DKIM signing after enabling it, after a period of time, Office 365 will automatically apply the Office 365 default policy for your domain.</span></span>
  
<span data-ttu-id="28be5-226">다음 예제에서는 fabrikam.com용 DKIM이 도메인 관리자가 아닌 Office 365에서 활성화되었다고 가정합니다.</span><span class="sxs-lookup"><span data-stu-id="28be5-226">In the following example, suppose that DKIM for fabrikam.com was enabled by Office 365, not by the administrator of the domain.</span></span> <span data-ttu-id="28be5-227">이는 필수적인 CNAME이 DNS에 존재하지 않음을 의미합니다.</span><span class="sxs-lookup"><span data-stu-id="28be5-227">This means that the required CNAMEs do not exist in DNS.</span></span> <span data-ttu-id="28be5-228">이 도메인의 전자 메일에 대한 DKIM 서명은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="28be5-228">DKIM signatures for email from this domain will look something like this:</span></span>
  
```
From: Second Example <second.example@fabrikam.com> 
DKIM-Signature: v=1; a=rsa-sha256; q=dns/txt; c=relaxed/relaxed; 
    s=selector1-fabrikam-com; d=contoso.onmicrosoft.com; t=1429912795; 
    h=From:To:Message-ID:Subject:MIME-Version:Content-Type; 
    bh=<body hash>; 
    b=<signed field>;
```

<span data-ttu-id="28be5-229">이 예제에서 도메인 관리자가 fabrikam.com에 대한 DKIM 서명을 활성화한 경우 호스트 이름과 도메인에는 CNAME이 가리키는 값이 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="28be5-229">In this example, the host name and domain contain the values to which the CNAME would point if DKIM-signing for fabrikam.com had been enabled by the domain administrator.</span></span> <span data-ttu-id="28be5-230">결국 Office 365에서 보낸 모든 단일 메시지는 DKIM 서명됩니다.</span><span class="sxs-lookup"><span data-stu-id="28be5-230">Eventually, every single message sent from Office 365 will be DKIM-signed.</span></span> <span data-ttu-id="28be5-231">DKIM을 직접 활성화하는 경우 도메인은 보낸 사람:주소의 도메인 (이 경우 fabrikam.com)과 동일합니다.</span><span class="sxs-lookup"><span data-stu-id="28be5-231">If you enable DKIM yourself, the domain will be the same as the domain in the From: address, in this case fabrikam.com.</span></span> <span data-ttu-id="28be5-232">직접 활성화하지 않는 경우 맞추는 대신 사용자 조직의 초기 도메인을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="28be5-232">If you don't, it will not align and instead will use your organization's initial domain.</span></span> <span data-ttu-id="28be5-233">초기 도메인을 확인하는 방법에 대한 자세한 내용은 [도메인 FAQ](https://support.office.com/article/1272bad0-4bd4-4796-8005-67d6fb3afc5a#bkmk_whydoihaveanonmicrosoft.comdomain)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="28be5-233">For information about determining your initial domain, see [Domains FAQ](https://support.office.com/article/1272bad0-4bd4-4796-8005-67d6fb3afc5a#bkmk_whydoihaveanonmicrosoft.comdomain).</span></span>
  
## <a name="set-up-dkim-so-that-a-third-party-service-can-send-or-spoof-email-on-behalf-of-your-custom-domain"></a><span data-ttu-id="28be5-234">타사 서비스에서 사용자 지정 도메인을 대신하여 이메일을 보내거나 스푸핑할 수 있도록 DKIM을 설정</span><span class="sxs-lookup"><span data-stu-id="28be5-234">Set up DKIM so that a third-party service can send, or spoof, email on behalf of your custom domain</span></span>
<span data-ttu-id="28be5-235"><a name="SetUp3rdPartyspoof"> </a></span><span class="sxs-lookup"><span data-stu-id="28be5-235"></span></span>

<span data-ttu-id="28be5-236">일부 대량 전자 메일 서비스 공급자 또는 소프트웨어를 서비스로 제공하는 공급자는 서비스에서 보낸 전자 메일에 대해 DKIM 키를 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="28be5-236">Some bulk email service providers, or software-as-a-service providers, let you set up DKIM keys for email that originates from their service.</span></span> <span data-ttu-id="28be5-237">따라서 필수 DNS 레코드를 설정하기 위해 본인과 타사 간의 조정이 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="28be5-237">This requires coordination between yourself and the third-party in order to set up the necessary DNS records.</span></span> <span data-ttu-id="28be5-238">두 조직이 정확히 동일한 방식으로 이 작업을 수행할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="28be5-238">No two organizations do it exactly the same way.</span></span> <span data-ttu-id="28be5-239">그 대신 프로세스는 전적으로 조직에 따라 다릅니다.</span><span class="sxs-lookup"><span data-stu-id="28be5-239">Instead, the process depends entirely on the organization.</span></span>
  
<span data-ttu-id="28be5-240">contoso.com 및 bulkemailprovider.com에 대해 올바르게 구성된 DKIM을 보여주는 메시지의 예는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="28be5-240">An example message showing a properly configured DKIM for contoso.com and bulkemailprovider.com might look like this:</span></span>
  
```
Return-Path: <communication@bulkemailprovider.com>
 From: <sender@contoso.com>
 DKIM-Signature: s=s1024; d=contoso.com
 Subject: Here is a message from Bulk Email Provider's infrastructure, but with a DKIM signature authorized by contoso.com
```

<span data-ttu-id="28be5-241">이 예제에서는 이 결과를 얻기 위해 다음과 같이 합니다.</span><span class="sxs-lookup"><span data-stu-id="28be5-241">In this example, in order to achieve this result:</span></span>
  
1. <span data-ttu-id="28be5-242">대량 전자 메일 공급자가 Contoso에 공개 DKIM 키를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="28be5-242">Bulk Email Provider gave Contoso a public DKIM key.</span></span>
    
2. <span data-ttu-id="28be5-243">Contoso는 DKIM 키를 해당 DNS 레코드에 게시합니다.</span><span class="sxs-lookup"><span data-stu-id="28be5-243">Contoso published the DKIM key to its DNS record.</span></span>
    
3. <span data-ttu-id="28be5-244">전자 메일을 보낼 때 대량 전자 메일 공급자는 해당하는 개인 키로 키에 서명합니다.</span><span class="sxs-lookup"><span data-stu-id="28be5-244">When sending email, Bulk Email Provider signs the key with the corresponding private key.</span></span> <span data-ttu-id="28be5-245">이렇게하면 대량 전자 메일 공급자가 메시지 머리글에 DKIM 서명을 첨부합니다.</span><span class="sxs-lookup"><span data-stu-id="28be5-245">By doing so, Bulk Email Provider attached the DKIM signature to the message header.</span></span>
    
4. <span data-ttu-id="28be5-246">수신 이메일 시스템은 메시지의 From:(5322.From) 주소에서 도메인에 대해 DKIM-Signature d= \<도메인\> 값을 인증하여 DKIM 확인을 수행합니다.</span><span class="sxs-lookup"><span data-stu-id="28be5-246">Receiving email systems perform a DKIM check by authenticating the DKIM-Signature d=\<domain\> value against the domain in the From: (5322.From) address of the message.</span></span> <span data-ttu-id="28be5-247">이 예제에서 값은 다음과 일치합니다.</span><span class="sxs-lookup"><span data-stu-id="28be5-247">In this example, the values match:</span></span>
    
    <span data-ttu-id="28be5-248">sender@**contoso.com**</span><span class="sxs-lookup"><span data-stu-id="28be5-248">sender@**contoso.com**</span></span>
    
    <span data-ttu-id="28be5-249">d=**contoso.com**</span><span class="sxs-lookup"><span data-stu-id="28be5-249">d=**contoso.com**</span></span>
    
## <a name="next-steps-after-you-set-up-dkim-for-office-365"></a><span data-ttu-id="28be5-250">다음 단계: Office 365에 대한 DKIM을 설정한 후</span><span class="sxs-lookup"><span data-stu-id="28be5-250">Next steps: After you set up DKIM for Office 365</span></span>
<span data-ttu-id="28be5-251"><a name="DKIMNextSteps"> </a></span><span class="sxs-lookup"><span data-stu-id="28be5-251"></span></span>

<span data-ttu-id="28be5-252">DKIM은 스푸핑을 방지하도록 설계되었지만 SPF 및 DMARC에서 더 잘 작동합니다.</span><span class="sxs-lookup"><span data-stu-id="28be5-252">Although DKIM is designed to help prevent spoofing, DKIM works better with SPF and DMARC.</span></span> <span data-ttu-id="28be5-253">DKIM을 설정한 후에 SPF를 아직 설정하지 않은 경우 설정을 수행해야합니다.</span><span class="sxs-lookup"><span data-stu-id="28be5-253">Once you have set up DKIM, if you have not already set up SPF you should do so.</span></span> <span data-ttu-id="28be5-254">SPF를 빠르게 도입하여 신속하게 구성하려면 [스푸핑 방지를 위해 Office 365에서 SPF 설정](set-up-spf-in-office-365-to-help-prevent-spoofing.md)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="28be5-254">For a quick introduction to SPF and to get it configured quickly, see [Set up SPF in Office 365 to help prevent spoofing](set-up-spf-in-office-365-to-help-prevent-spoofing.md).</span></span> <span data-ttu-id="28be5-255">Office 365에서 SPF를 사용하는 방법이나 문제 해결 또는 비표준 배포(예: 하이브리드 배포)에 대한 자세한 내용은 [Office 365에서 SPF(Sender Policy Framework)를 사용하여 스푸핑을 차단하는 방법](how-office-365-uses-spf-to-prevent-spoofing.md)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="28be5-255">For a more in-depth understanding of how Office 365 uses SPF, or for troubleshooting or non-standard deployments such as hybrid deployments, start with [How Office 365 uses Sender Policy Framework (SPF) to prevent spoofing](how-office-365-uses-spf-to-prevent-spoofing.md).</span></span> <span data-ttu-id="28be5-256">다음으로 [DMARC를 사용하여 Office 365에서 전자 메일 유효성 검사](use-dmarc-to-validate-email.md)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="28be5-256">Next, see [Use DMARC to validate email in Office 365](use-dmarc-to-validate-email.md).</span></span> <span data-ttu-id="28be5-257">[스팸 방지 메시지 헤드](anti-spam-message-headers.md)에는 Office 365에서 DKIM 검사에 사용하는 구문 및 헤드 필드가 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="28be5-257">[Anti-spam message headers](anti-spam-message-headers.md) includes the syntax and header fields used by Office 365 for DKIM checks.</span></span> 
  

