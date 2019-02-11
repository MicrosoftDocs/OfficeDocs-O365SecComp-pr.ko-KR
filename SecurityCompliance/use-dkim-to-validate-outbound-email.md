---
title: DKIM를 사용 하 여 Office 365에서 사용자 지정 도메인에서 보낸 아웃 바운드 전자 메일의 유효성을 검사 하려면
ms.author: krowley
author: kccross
manager: laurawi
ms.date: ''
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.custom: TN2DMC
search.appverid:
- MET150
ms.assetid: 56fee1c7-dc37-470e-9b09-33fff6d94617
description: '요약: 사용 DomainKeys 식별 된 메일 (DKIM) Office 365를 사용 하는 방법을 확인 대상 전자 메일 시스템 사용자 지정 도메인에서 보낸 메시지를 신뢰 하는이 문서에 설명 합니다.'
ms.openlocfilehash: 080d873c91c2dfb5910588113f2a6709b3ee9ab4
ms.sourcegitcommit: 7e2a0185cadea7f3a6afc5ddc445eac2e1ce22eb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/11/2019
ms.locfileid: "29696335"
---
# <a name="use-dkim-to-validate-outbound-email-sent-from-your-custom-domain-in-office-365"></a><span data-ttu-id="96323-103">DKIM를 사용 하 여 Office 365에서 사용자 지정 도메인에서 보낸 아웃 바운드 전자 메일의 유효성을 검사 하려면</span><span class="sxs-lookup"><span data-stu-id="96323-103">Use DKIM to validate outbound email sent from your custom domain in Office 365</span></span>

 <span data-ttu-id="96323-104">**요약:** 이 문서에서는 사용 DomainKeys 식별 된 메일 (DKIM) Office 365를 사용 하는 방법을 확인 대상 전자 메일 시스템 사용자 지정 도메인에서 보낸 메시지를 신뢰 하는 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="96323-104">**Summary:** This article describes how you use DomainKeys Identified Mail (DKIM) with Office 365 to ensure that destination email systems trust messages sent from your custom domain.</span></span> 
  
<span data-ttu-id="96323-p101">도메인에서 들어오는 처럼 보이게 하는 메시지를 보내지 못하도록 spoofers를 방지 하려면 SPF 및 DMARC 외에도 DKIM를 사용 해야 합니다. DKIM은 메시지 헤더에 전자 메일 메시지에 디지털 서명을 추가할 수 있습니다. 소리 복잡해 지는 없습니다. DKIM를 구성할 때에 대 한 권한 부여에 연결 하 고, 도메인 또는 서명, 암호화 인증을 사용 하 여 전자 메일 메시지에 해당 이름을 합니다. 도메인에서 전자 메일을 수신 하는 전자 메일 시스템 받는 전자 메일을 받을 수 있는 적절 한지 확인 하는 데 도움이 디지털 서명이 사용 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="96323-p101">You should use DKIM in addition to SPF and DMARC to help prevent spoofers from sending messages that look like they are coming from your domain. DKIM lets you add a digital signature to email messages in the message header. Sounds complicated, but it's really not. When you configure DKIM, you authorize your domain to associate, or sign, its name to an email message by using cryptographic authentication. Email systems that receive email from your domain can use this digital signature to help determine if incoming email that they receive is legitimate.</span></span>
  
<span data-ttu-id="96323-p102">개인 키를 사용 하 여 도메인의 보내는 전자 메일의 헤더를 암호화 하는 기본적으로, 합니다. 받는 서버에는 서명을 디코딩할 다음 사용할 수 있는 도메인의 DNS 레코드에는 공용 키를 게시 합니다. 때 확인 하는 메시지 사용자 로부터 실제로 연결 되 고 도메인 스푸핑 사람이 보낸 것이 아니라 공용 키를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="96323-p102">Basically, you use a private key to encrypt the header in your domain's outgoing email. You publish a public key to your domain's DNS records that receiving servers can then use to decode the signature. They use the public key to verify that the messages are really coming from you and not coming from someone spoofing your domain.</span></span>
  
<span data-ttu-id="96323-p103">Office 365 초기 도메인에 대 한 DKIM를 자동으로 설정합니다. 초기 도메인은 귀하가 등록 하면 contoso.onmicrosoft.com 등 서비스를 사용할 경우 Office 365를 생성 하는 도메인입니다. 초기 도메인에 대 한 DKIM를 설정 하는 모든 작업을 수행할 필요가 없습니다. 도메인에 대 한 자세한 내용은 [도메인 FAQ](https://support.office.com/article/Domains-FAQ-1272bad0-4bd4-4796-8005-67d6fb3afc5a#bkmk_whydoihaveanonmicrosoft.comdomain)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="96323-p103">Office 365 automatically sets up DKIM for initial domains. The initial domain is the domain that Office 365 created for you when you signed up with the service, for example, contoso.onmicrosoft.com. You don't need to do anything to set up DKIM for your initial domain. For more information about domains, see [Domains FAQ](https://support.office.com/article/Domains-FAQ-1272bad0-4bd4-4796-8005-67d6fb3afc5a#bkmk_whydoihaveanonmicrosoft.comdomain).</span></span>
  
<span data-ttu-id="96323-p104">사용자 지정 도메인에 대 한 너무 DKIM 조건에 대해 수행 하도록 선택할 수 있습니다. 설정 하지 않으면 DKIM를 사용자 지정 도메인을 하는 경우 Office 365 개인 및 공용 키 쌍을 만듭니다 활성화 DKIM 서명 하 고 사용자 지정 도메인에 대 한 Office 365 기본 정책을 구성 합니다. 대부분의 Office 365 고객에 대 한 충분 한 검사가 이지만, 다음과 같은 상황에서 사용자 지정 도메인에 대 한 DKIM을 수동으로 구성 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="96323-p104">You can choose to do nothing about DKIM for your custom domain too. If you do not set up DKIM for your custom domain, Office 365 creates a private and public key pair, enables DKIM signing, and then configures the Office 365 default policy for your custom domain. While this is sufficient coverage for most Office 365 customers, you should manually configure DKIM for your custom domain in the following circumstances:</span></span>
  
- <span data-ttu-id="96323-120">Office 365에서 사용자 지정 도메인을 둘 이상 있습니다</span><span class="sxs-lookup"><span data-stu-id="96323-120">You have more than one custom domain in Office 365</span></span>
    
- <span data-ttu-id="96323-121">너무 DMARC를 설정 하려면 (권장)</span><span class="sxs-lookup"><span data-stu-id="96323-121">You're going to set up DMARC too (recommended)</span></span>
    
- <span data-ttu-id="96323-122">사용자의 개인 키에 대 한 제어를 원합니다</span><span class="sxs-lookup"><span data-stu-id="96323-122">You want control over your private key</span></span>
    
- <span data-ttu-id="96323-123">CNAME 레코드를 사용자 지정</span><span class="sxs-lookup"><span data-stu-id="96323-123">You want to customize your CNAME records</span></span>
    
- <span data-ttu-id="96323-124">제 3 자 벌크 메일 발송을 사용 하는 경우 예 제 3 자 도메인 외부에서 들어오는 전자 메일에 대 한 DKIM 키를 설정 하려고 합니다.</span><span class="sxs-lookup"><span data-stu-id="96323-124">You want to set up DKIM keys for email originating out of a third-party domain, for example, if you use a third-party bulk mailer.</span></span>
    
<span data-ttu-id="96323-125">이 문서의 내용</span><span class="sxs-lookup"><span data-stu-id="96323-125">In this article:</span></span>
  
- [<span data-ttu-id="96323-126">DKIM은 Office 365의 악의적인 스푸핑 방지 단독으로 SPF 보다 더 잘 작동 하는 방법</span><span class="sxs-lookup"><span data-stu-id="96323-126">How DKIM works better than SPF alone to prevent malicious spoofing in Office 365</span></span>](use-dkim-to-validate-outbound-email.md#HowDKIMWorks)
    
- [<span data-ttu-id="96323-127">Office 365에서 DKIM를 수동으로 설정 하려면 수행 하는데 필요한</span><span class="sxs-lookup"><span data-stu-id="96323-127">What you need to do to manually set up DKIM in Office 365</span></span>](use-dkim-to-validate-outbound-email.md#SetUpDKIMO365)
    
- [<span data-ttu-id="96323-128">Office 365에서 둘 이상의 사용자 지정 도메인에 대 한 DKIM를 구성 하려면</span><span class="sxs-lookup"><span data-stu-id="96323-128">To configure DKIM for more than one custom domain in Office 365</span></span>](use-dkim-to-validate-outbound-email.md#DKIMMultiDomain)
    
- [<span data-ttu-id="96323-129">Office 365에서 사용자 지정 도메인에 대 한 정책 서명 DKIM를 사용 하지 않도록 설정</span><span class="sxs-lookup"><span data-stu-id="96323-129">Disabling the DKIM signing policy for a custom domain in Office 365</span></span>](use-dkim-to-validate-outbound-email.md#DisableDKIMSigningPolicy)
    
- [<span data-ttu-id="96323-130">DKIM 및 Office 365에 대 한 기본 동작</span><span class="sxs-lookup"><span data-stu-id="96323-130">Default behavior for DKIM and Office 365</span></span>](use-dkim-to-validate-outbound-email.md#DefaultDKIMbehavior)
    
- [<span data-ttu-id="96323-131">DKIM를 제 3 자 서비스 보내기, 또는 사용자 지정 도메인을 대신 하 여 전자 메일을 스푸핑할 수 있도록 설정</span><span class="sxs-lookup"><span data-stu-id="96323-131">Set up DKIM so that a third-party service can send, or spoof, email on behalf of your custom domain</span></span>](use-dkim-to-validate-outbound-email.md#SetUp3rdPartyspoof)
    
- [<span data-ttu-id="96323-132">다음 단계: Office 365에 대 한 DKIM를 설정한 후</span><span class="sxs-lookup"><span data-stu-id="96323-132">Next steps: After you set up DKIM for Office 365</span></span>](use-dkim-to-validate-outbound-email.md#DKIMNextSteps)
    
## <a name="how-dkim-works-better-than-spf-alone-to-prevent-malicious-spoofing-in-office-365"></a><span data-ttu-id="96323-133">DKIM은 Office 365의 악의적인 스푸핑 방지 단독으로 SPF 보다 더 잘 작동 하는 방법</span><span class="sxs-lookup"><span data-stu-id="96323-133">How DKIM works better than SPF alone to prevent malicious spoofing in Office 365</span></span>
<span data-ttu-id="96323-134"><a name="HowDKIMWorks"> </a></span><span class="sxs-lookup"><span data-stu-id="96323-134"></span></span>

<span data-ttu-id="96323-p105">정보 메시지 봉투를 추가 하는 SPF 하지만 DKIM 실제로 메시지 헤더 내에서 서명을 암호화 합니다. 메시지를 전달 하면 전달 서버에서 자리 비움으로 해당 메시지 봉투의 일부를 제거할 수 있습니다. 디지털 서명 전자 메일 머리글의 일부 이기 때문에 전자 메일 메시지와 함께 유지, 이후 DKIM도 때 메시지를 전달 된 다음 예제와 같이 작동 합니다.</span><span class="sxs-lookup"><span data-stu-id="96323-p105">SPF adds information to a message envelope but DKIM actually encrypts a signature within the message header. When you forward a message, portions of that message's envelope can be stripped away by the forwarding server. Since the digital signature stays with the email message because it's part of the email header, DKIM works even when a message has been forwarded as shown in the following example.</span></span>
  
![SPF 확인이 실패하는 경우 DKIM 인증을 제공하는 전달된 메시지를 보여주는 다이어그램](media/28f93b4c-97e7-4309-acc4-fd0d2e0e3377.jpg)
  
<span data-ttu-id="96323-p106">이 예제에서는 도메인에 대 한 SPF TXT 레코드를 게시만 했던 경우 받는 사람의 메일 서버도 전자 메일 스팸으로 표시 하 고 false 이면 양수 결과 생성 합니다. 이 시나리오에서 DKIM 추가 false 양의 스팸 보고 줄일 수 있습니다. 인증에 공개 키 암호화 및 아니라 IP 주소를 의존 하는 DKIM, 때문에 DKIM는 훨씬 더 강력한 형태의 인증 SPF 보다 것으로 간주 됩니다. SPF 및 DKIM, 모두를 사용 하는 것이 좋습니다 배포에서 DMARC와 합니다.</span><span class="sxs-lookup"><span data-stu-id="96323-p106">In this example, if you had only published an SPF TXT record for your domain, the recipient's mail server could have marked your email as spam and generated a false positive result. The addition of DKIM in this scenario reduces false positive spam reporting. Because DKIM relies on public key cryptography to authenticate and not just IP addresses, DKIM is considered a much stronger form of authentication than SPF. We recommend using both SPF and DKIM, as well as DMARC in your deployment.</span></span>
  
<span data-ttu-id="96323-p107">수행해 해보겠습니다: DKIM 개인 키를 사용 하 여 암호화 된 서명 된 메시지 헤더에 삽입 합니다. 서명 도메인 또는 아웃 바운드 도메인의 값으로 삽입 되는 **d =** 헤더에서 필드입니다. 확인 도메인 또는 받는 사람의 도메인을 사용 하 여는 **d =** DNS에서 공용 키를 조회 하 고 메시지 인증에 필드를 추가 합니다. 메시지를 확인 하는 경우 DKIM 검사를 통과 합니다.</span><span class="sxs-lookup"><span data-stu-id="96323-p107">The nitty gritty: DKIM uses a private key to insert an encrypted signature into the message headers. The signing domain, or outbound domain, is inserted as the value of the **d=** field in the header. The verifying domain, or recipient's domain, then use the **d=** field to look up the public key from DNS and authenticate the message. If the message is verified, the DKIM check passes.</span></span> 
  
## <a name="what-you-need-to-do-to-manually-set-up-dkim-in-office-365"></a><span data-ttu-id="96323-147">Office 365에서 DKIM를 수동으로 설정 하려면 수행 하는데 필요한</span><span class="sxs-lookup"><span data-stu-id="96323-147">What you need to do to manually set up DKIM in Office 365</span></span>
<span data-ttu-id="96323-148"><a name="SetUpDKIMO365"> </a></span><span class="sxs-lookup"><span data-stu-id="96323-148"></span></span>

<span data-ttu-id="96323-149">DKIM를 구성 하려면 다음이 단계를 완료 합니다.</span><span class="sxs-lookup"><span data-stu-id="96323-149">To configure DKIM, you will complete these steps:</span></span>
  
- [<span data-ttu-id="96323-150">DNS에 사용자 지정 도메인에 대 한 두 CNAME 레코드를 게시 합니다.</span><span class="sxs-lookup"><span data-stu-id="96323-150">Publish two CNAME records for your custom domain in DNS</span></span>](use-dkim-to-validate-outbound-email.md#Publish2CNAME)
    
- [<span data-ttu-id="96323-151">Office 365에서 사용자 지정 도메인에 대 한 서명 DKIM를 사용 하도록 설정</span><span class="sxs-lookup"><span data-stu-id="96323-151">Enable DKIM signing for your custom domain in Office 365</span></span>](use-dkim-to-validate-outbound-email.md#EnableDKIMinO365)
    
### <a name="publish-two-cname-records-for-your-custom-domain-in-dns"></a><span data-ttu-id="96323-152">DNS에 사용자 지정 도메인에 대 한 두 CNAME 레코드를 게시 합니다.</span><span class="sxs-lookup"><span data-stu-id="96323-152">Publish two CNAME records for your custom domain in DNS</span></span>
<span data-ttu-id="96323-153"><a name="Publish2CNAME"> </a></span><span class="sxs-lookup"><span data-stu-id="96323-153"></span></span>

<span data-ttu-id="96323-p108">DKIM 서명을 DNS에 추가 하려는 각 도메인에 대해 두 CNAME 레코드를 게시 해야 합니다. DNS CNAME 레코드를 사용 하는 도메인의 정식 이름은 다른 도메인 이름에 대 한 별칭을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="96323-p108">For each domain for which you want to add a DKIM signature in DNS, you need to publish two CNAME records. A CNAME record is used by DNS to specify that the canonical name of a domain is an alias for another domain name.</span></span> 
  
 <span data-ttu-id="96323-p109">Office 365 설정 하는 두 레코드를 사용 하 여 자동 키 회전을 수행 합니다. Office 365에서 초기 도메인 외에도 사용자 지정 도메인을 프로 비전 하는 경우에 각 추가 도메인에 대 한 두 CNAME 레코드를 게시 해야 합니다. 따라서 두 도메인을 사용 하는 경우 두 추가 CNAME 레코드를 게시 하 고 등 해야 있습니다.</span><span class="sxs-lookup"><span data-stu-id="96323-p109">Office 365 performs automatic key rotation using the two records that you establish. If you have provisioned custom domains in addition to the initial domain in Office 365, you must publish two CNAME records for each additional domain. So, if you have two domains, you must publish two additional CNAME records, and so on.</span></span>
  
<span data-ttu-id="96323-159">CNAME 레코드에 대 한 다음 형식을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="96323-159">Use the following format for the CNAME records.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="96323-p110">GCC 높은 고객 중 한 경우 _domainGuid_ 다르게 계산! _DomainGuid_를 계산 하 여 _initialDomain_ 에 대 한 MX 레코드를 조회 하는 대신 대신는 자동으로 계산 되도록 사용자 지정 된 도메인에서 직접 합니다. 등 사용자 지정 된 도메인이 "contoso.com" 되는 경우에 domainGuid는 "contoso com"가 됩니다., 마침표를 파선으로 대체 됩니다. 그렇다면 어떤 MX 레코드에 관계 없이 initialDomain 지점이 됩니다 항상는 위의 메서드를 사용 하면 CNAME 레코드에서 사용 하 여 domainGuid 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="96323-p110">If you are one of our GCC High customers, we calculate _domainGuid_ differently! Instead of looking up the MX record for your _initialDomain_ to calculate _domainGuid_, instead we calculate it directly from the customized domain. For example, if your customized domain is “contoso.com” your domainGuid becomes “contoso-com”, any periods are replaced with a dash. So, regardless of what MX record your initialDomain points to, you’ll always use the above method to calculate the domainGuid to use in your CNAME records.</span></span>

  
```
Host name:          selector1._domainkey
Points to address or value: selector1-<domainGUID>._domainkey.<initialDomain> 
TTL:                3600

Host name:          selector2._domainkey
Points to address or value: selector2-<domainGUID>._domainkey.<initialDomain> 
TTL:                3600
```

<span data-ttu-id="96323-164">여기서 각 부분이 나타내는 의미는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="96323-164">Where:</span></span>
  
- <span data-ttu-id="96323-165">Office 365에 대 한 선택기는 항상 "selector1" 또는 "selector2"입니다.</span><span class="sxs-lookup"><span data-stu-id="96323-165">For Office 365, the selectors will always be "selector1" or "selector2".</span></span> 
    
- <span data-ttu-id="96323-p111">_domainGUID_ mail.protection.outlook.com 하기 전에 표시 되는 사용자 지정 도메인에 대 한 사용자 지정 된 MX 레코드에 _domainGUID_ 와 동일 합니다. 예, contoso.com 도메인에 대 한 다음 MX 레코드를 _domainGUID_ 는 contoso com:</span><span class="sxs-lookup"><span data-stu-id="96323-p111">_domainGUID_ is the same as the _domainGUID_ in the customized MX record for your custom domain that appears before mail.protection.outlook.com. For example, in the following MX record for the domain contoso.com, the _domainGUID_ is contoso-com:</span></span> 
    
    ```
    contoso.com.  3600  IN  MX   5 contoso-com.mail.protection.outlook.com
    ```

- <span data-ttu-id="96323-p112">_initialDomain_ 은 도메인 Office 365에 등록할 수 있을 때 사용한 것입니다. 초기 도메인 onmicrosoft.com 항상 종료 됩니다. 초기 도메인을 결정 하는 방법에 대 한 정보를 [도메인 FAQ](https://support.office.com/article/1272bad0-4bd4-4796-8005-67d6fb3afc5a#bkmk_whydoihaveanonmicrosoft.comdomain)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="96323-p112">_initialDomain_ is the domain that you used when you signed up for Office 365. Initial domains always end in onmicrosoft.com. For information about determining your initial domain, see [Domains FAQ](https://support.office.com/article/1272bad0-4bd4-4796-8005-67d6fb3afc5a#bkmk_whydoihaveanonmicrosoft.comdomain).</span></span>
    
<span data-ttu-id="96323-171">예는 초기 cohovineyardandwinery.onmicrosoft.com, 도메인 및 두 사용자 지정 도메인 cohovineyard.com 및 cohowinery.com을 설치한 경우에 총 4 개의 CNAME 레코드에 대 한 각 추가 도메인에 대 한 두 CNAME 레코드를 설정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="96323-171">For example, if you have an initial domain of cohovineyardandwinery.onmicrosoft.com, and two custom domains cohovineyard.com and cohowinery.com, you would need to set up two CNAME records for each additional domain, for a total of four CNAME records.</span></span>
  
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

### <a name="enable-dkim-signing-for-your-custom-domain-in-office-365"></a><span data-ttu-id="96323-172">Office 365에서 사용자 지정 도메인에 대 한 서명 DKIM를 사용 하도록 설정</span><span class="sxs-lookup"><span data-stu-id="96323-172">Enable DKIM signing for your custom domain in Office 365</span></span>
<span data-ttu-id="96323-173"><a name="EnableDKIMinO365"> </a></span><span class="sxs-lookup"><span data-stu-id="96323-173"></span></span>

<span data-ttu-id="96323-p113">DNS에서 CNAME 레코드를 게시 한 후 Office 365를 통해 DKIM 서명을 활성화 준비가 된 것입니다. Office 365 관리 센터를 통해 또는 PowerShell을 사용 하 여 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="96323-p113">Once you have published the CNAME records in DNS, you are ready to enable DKIM signing through Office 365. You can do this either through the Office 365 admin center or by using PowerShell.</span></span>
  
#### <a name="to-enable-dkim-signing-for-your-custom-domain-through-the-office-365-admin-center"></a><span data-ttu-id="96323-176">Office 365 관리 센터를 통해 사용자 지정 도메인에 대 한 서명 DKIM를 사용 하도록 설정 하려면</span><span class="sxs-lookup"><span data-stu-id="96323-176">To enable DKIM signing for your custom domain through the Office 365 admin center</span></span>

1. <span data-ttu-id="96323-177">회사 또는 학교 계정로 [Office 365에 로그인](https://support.office.microsoft.com/article/e9eb7d51-5430-4929-91ab-6157c5a050b4)합니다.</span><span class="sxs-lookup"><span data-stu-id="96323-177">[Sign in to Office 365](https://support.office.microsoft.com/article/e9eb7d51-5430-4929-91ab-6157c5a050b4) with your work or school account.</span></span> 
    
2. <span data-ttu-id="96323-178">왼쪽 위에서 앱 시작 관리자 아이콘을 선택하고 **관리자**를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="96323-178">Select the app launcher icon in the upper-left and choose **Admin**.</span></span>
    
3. <span data-ttu-id="96323-179">왼쪽 탐색 영역에서 **관리** 를 확장 하 고 **Exchange**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="96323-179">In the lower-left navigation, expand **Admin** and choose **Exchange**.</span></span>
    
4. <span data-ttu-id="96323-180">**보호** 이동 \> **dkim**합니다.</span><span class="sxs-lookup"><span data-stu-id="96323-180">Go to **Protection** \> **dkim**.</span></span>
    
5. <span data-ttu-id="96323-p114">DKIM를 사용 하도록 설정 하 고 다음 **DKIM 서명 사용 하 여이 도메인에 대 한 로그인 메시지**대 한 **사용**을 선택 하려면 원하는 도메인을 선택 합니다. 각 사용자 지정 도메인에 대해이 단계를 반복 합니다.</span><span class="sxs-lookup"><span data-stu-id="96323-p114">Select the domain for which you want to enable DKIM and then, for **Sign messages for this domain with DKIM signatures**, choose **Enable**. Repeat this step for each custom domain.</span></span>
    
#### <a name="to-enable-dkim-signing-for-your-custom-domain-by-using-powershell"></a><span data-ttu-id="96323-183">PowerShell을 사용 하 여 사용자 지정 도메인에 대 한 서명 DKIM를 사용 하도록 설정 하려면</span><span class="sxs-lookup"><span data-stu-id="96323-183">To enable DKIM signing for your custom domain by using PowerShell</span></span>

1. <span data-ttu-id="96323-184">[Exchange Online PowerShell에 연결합니다](https://technet.microsoft.com/library/jj984289.aspx).</span><span class="sxs-lookup"><span data-stu-id="96323-184">[Connect to Exchange Online PowerShell](https://technet.microsoft.com/library/jj984289.aspx).</span></span>
    
2. <span data-ttu-id="96323-185">다음 명령을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="96323-185">Run the following command:</span></span>
    
    ```
    New-DkimSigningConfig -DomainName <domain> -Enabled $true
    ```

   <span data-ttu-id="96323-186">여기서 _도메인_ 은 DKIM에 대 한 로그인을 사용 하도록 설정 하려는 사용자 지정 도메인의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="96323-186">Where _domain_ is the name of the custom domain that you want to enable DKIM signing for.</span></span> 
    
   <span data-ttu-id="96323-187">예: contoso.com 도메인:</span><span class="sxs-lookup"><span data-stu-id="96323-187">For example, for the domain contoso.com:</span></span>
    
    ```
    New-DkimSigningConfig -DomainName contoso.com -Enabled $true
    ```

#### <a name="to-confirm-dkim-signing-is-configured-properly-for-office-365"></a><span data-ttu-id="96323-188">DKIM 확인 하려면 서명 제대로 구성 Office 365에 대 한</span><span class="sxs-lookup"><span data-stu-id="96323-188">To Confirm DKIM signing is configured properly for Office 365</span></span>

<span data-ttu-id="96323-p115">DKIM 제대로 구성 되었는지 확인 하려면 다음이 단계를 수행 하기 전에 몇 분정도 기다립니다. 이렇게 하면 네트워크 전체에 걸쳐 분산 될 도메인에 대 한 DKIM 정보에 대 한 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="96323-p115">Wait a few minutes before you follow these steps to confirm that you have properly configured DKIM. This allows time for the DKIM information about the domain to be spread throughout the network.</span></span>
  
- <span data-ttu-id="96323-191">예: outlook.com 또는 Hotmail.com 다른 전자 메일 계정에 Office 365 DKIM 사용이 가능한 도메인 내 계정에서 메시지를 보냅니다.</span><span class="sxs-lookup"><span data-stu-id="96323-191">Send a message from an account within your Office 365 DKIM-enabled domain to another email account such as outlook.com or Hotmail.com.</span></span>
    
- <span data-ttu-id="96323-p116">테스트 목적으로 aol.com 계정을 사용 하지 마십시오. AOL은 SPF 검사를 통과 하는 경우 DKIM 확인을 건너뛸 수 있습니다. 이 테스트를 무효화 됩니다.</span><span class="sxs-lookup"><span data-stu-id="96323-p116">Do not use an aol.com account for testing purposes. AOL may skip the DKIM check if the SPF check passes. This will nullify your test.</span></span>
    
- <span data-ttu-id="96323-p117">메시지를 열고 머리글을 살펴봅니다. 메시지에 대 한 헤더를 보기 위한 지침 메시징 클라이언트에 따라 달라 집니다. Outlook에서 메시지 헤더 보기에 대 한 지침을 [전자 메일 메시지 머리글 보기를](https://support.office.com/article/CD039382-DC6E-4264-AC74-C048563D212C)참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="96323-p117">Open the message and look at the header. Instructions for viewing the header for the message will vary depending on your messaging client. For instructions on viewing message headers in Outlook, see [View e-mail message headers](https://support.office.com/article/CD039382-DC6E-4264-AC74-C048563D212C).</span></span>

  <span data-ttu-id="96323-p118">DKIM 서명 된 메시지는 호스트 이름 및 CNAME 항목을 게시 하는 경우를 정의 하는 도메인에 포함 됩니다. 메시지는이 예제에서는 같습니다.</span><span class="sxs-lookup"><span data-stu-id="96323-p118">The DKIM-signed message will contain the host name and domain you defined when you published the CNAME entries. The message will look something like this example:</span></span> 
    
    ```
    From: Example User <example@contoso.com> 
    DKIM-Signature: v=1; a=rsa-sha256; q=dns/txt; c=relaxed/relaxed; 
        s=selector1; d=contoso.com; t=1429912795; 
        h=From:To:Message-ID:Subject:MIME-Version:Content-Type; 
        bh=<body hash>; 
        b=<signed field>;
    ```

- <span data-ttu-id="96323-p119">인증 결과 헤더를 찾습니다. 결과 다음과 같이 포함 되도록 각 수신 서비스에서는 약간 다른 형식을 받는 메일을 스탬프 처리 하는 동안 **DKIM 통과 =** 또는 **DKIM 확인 =** 합니다.</span><span class="sxs-lookup"><span data-stu-id="96323-p119">Look for the Authentication-Results header. While each receiving service uses a slightly different format to stamp the incoming mail, the result should include something like **DKIM=pass** or **DKIM=OK**.</span></span> 
    
## <a name="to-configure-dkim-for-more-than-one-custom-domain-in-office-365"></a><span data-ttu-id="96323-202">Office 365에서 둘 이상의 사용자 지정 도메인에 대 한 DKIM를 구성 하려면</span><span class="sxs-lookup"><span data-stu-id="96323-202">To configure DKIM for more than one custom domain in Office 365</span></span>
<span data-ttu-id="96323-203"><a name="DKIMMultiDomain"> </a></span><span class="sxs-lookup"><span data-stu-id="96323-203"></span></span>

<span data-ttu-id="96323-p120">특정 시점 나중에 다른 사용자 지정 도메인을 추가 하려는 하 고 새 도메인에 대 한 DKIM를 사용 하려면, 경우에 각 도메인에 대 한이 문서의 단계를 완료 해야 합니다. 특히, [Office 365에서 DKIM를 수동으로 설정 하려면 수행 하는데 필요한](use-dkim-to-validate-outbound-email.md#SetUpDKIMO365)모든 단계를 완료 합니다.</span><span class="sxs-lookup"><span data-stu-id="96323-p120">If at some point in the future you decide to add another custom domain and you want to enable DKIM for the new domain, you must complete the steps in this article for each domain. Specifically, complete all steps in [What you need to do to manually set up DKIM in Office 365](use-dkim-to-validate-outbound-email.md#SetUpDKIMO365).</span></span>
  
## <a name="disabling-the-dkim-signing-policy-for-a-custom-domain-in-office-365"></a><span data-ttu-id="96323-206">Office 365에서 사용자 지정 도메인에 대 한 정책 서명 DKIM를 사용 하지 않도록 설정</span><span class="sxs-lookup"><span data-stu-id="96323-206">Disabling the DKIM signing policy for a custom domain in Office 365</span></span>
<span data-ttu-id="96323-207"><a name="DisableDKIMSigningPolicy"> </a></span><span class="sxs-lookup"><span data-stu-id="96323-207"></span></span>

<span data-ttu-id="96323-p121">서명 정책을 사용 하지 않으면 DKIM 완전히 해제 하지 않습니다. 시간이 지나면 Office 365 도메인에 대 한 기본 Office 365 정책을 자동으로 적용 됩니다. 자세한 내용은 [DKIM 및 Office 365의 기본 동작을](use-dkim-to-validate-outbound-email.md#DefaultDKIMbehavior)참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="96323-p121">Disabling the signing policy does not completely disable DKIM. After a period of time, Office 365 will automatically apply the default Office 365 policy for your domain. For more information, see [Default behavior for DKIM and Office 365](use-dkim-to-validate-outbound-email.md#DefaultDKIMbehavior).</span></span>
  
### <a name="to-disable-the-dkim-signing-policy-by-using-windows-powershell"></a><span data-ttu-id="96323-211">Windows PowerShell을 사용 하 여 정책에 서명 DKIM를 사용 하지 않도록 설정 하려면</span><span class="sxs-lookup"><span data-stu-id="96323-211">To disable the DKIM signing policy by using Windows PowerShell</span></span>

1. <span data-ttu-id="96323-212">[Exchange Online PowerShell에 연결합니다](https://technet.microsoft.com/library/jj984289.aspx).</span><span class="sxs-lookup"><span data-stu-id="96323-212">[Connect to Exchange Online PowerShell](https://technet.microsoft.com/library/jj984289.aspx).</span></span>
    
2. <span data-ttu-id="96323-213">DKIM 로그인을 사용 하지 않도록 설정 하려는 각 도메인에 대 한 다음 명령 중 하나를 실행 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="96323-213">Run one of the following commands for each domain for which you want to disable DKIM signing.</span></span>
    
    ```
    $p=Get-DkimSigningConfig -identity <domain>
    $p[0] | set-DkimSigningConfig -enabled $false
    ```

   <span data-ttu-id="96323-214">예를 들면 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="96323-214">For example:</span></span>
    
    ```
    $p=Get-DkimSigningConfig -identity contoso.com
    $p[0] | set-DkimSigningConfig -enabled $false
    ```

   <span data-ttu-id="96323-215">또는</span><span class="sxs-lookup"><span data-stu-id="96323-215">Or</span></span>
    
    ```
    Set-DkimSigningConfig -identity $p[<number>].identity -enabled $false
    ```

    <span data-ttu-id="96323-p122">여기서 _번호_ 는 정책의 인덱스입니다. 예를 들어:</span><span class="sxs-lookup"><span data-stu-id="96323-p122">Where _number_ is the index of the policy. For example:</span></span> 
    
    ```
    Set-DkimSigningConfig -identity $p[0].identity -enabled $false
    ```

## <a name="default-behavior-for-dkim-and-office-365"></a><span data-ttu-id="96323-218">DKIM 및 Office 365에 대 한 기본 동작</span><span class="sxs-lookup"><span data-stu-id="96323-218">Default behavior for DKIM and Office 365</span></span>
<span data-ttu-id="96323-219"><a name="DefaultDKIMbehavior"> </a></span><span class="sxs-lookup"><span data-stu-id="96323-219"></span></span>

<span data-ttu-id="96323-p123">DKIM을 사용 하지 않는 경우 사용자 지정 도메인에 대 한 1024 비트 DKIM 공용 키 및이 데이터 센터에서 내부적으로 저장 하는 연결 된 개인 키가 자동으로 Office 365에 만듭니다. 기본적으로 Office 365에는 서명 되지 않은 정책을 전체에서 도메인에 대해 구성 하는 기본을 사용 합니다. 이 사용 함을 의미 설정 하지 않으면 DKIM를 자신을 하는 경우 Office 365가 해당 기본 정책 및 키 도메인에 대 한 DKIM을 사용 하기 위해 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="96323-p123">If you do not enable DKIM, Office 365 automatically creates a 1024-bit DKIM public key for your custom domain and the associated private key which we store internally in our datacenter. By default, Office 365 uses a default signing configuration for domains that do not have a policy in place. This means that if you do not set up DKIM yourself, Office 365 will use its default policy and keys it creates in order to enable DKIM for your domain.</span></span>
  
<span data-ttu-id="96323-223">또한 DKIM 서명 시간이 지난 후 활성화 한 후 사용 하지 않도록 설정 하는 경우 Office 365 도메인에 대 한 Office 365 기본 정책을 자동으로 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="96323-223">Also, if you disable DKIM signing after enabling it, after a period of time, Office 365 will automatically apply the Office 365 default policy for your domain.</span></span>
  
<span data-ttu-id="96323-p124">다음 예제에서는 DKIM fabrikam.com에 대해 사용 하도록 설정한 Office 365 도메인의 관리자가 아닌 경우를 가정해 보겠습니다. 이 필요한 Cname DNS에 존재 하지 않는 것을 의미 합니다. 이 도메인에서 전자 메일에 대 한 DKIM 서명은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="96323-p124">In the following example, suppose that DKIM for fabrikam.com was enabled by Office 365, not by the administrator of the domain. This means that the required CNAMEs do not exist in DNS. DKIM signatures for email from this domain will look something like this:</span></span>
  
```
From: Second Example <second.example@fabrikam.com> 
DKIM-Signature: v=1; a=rsa-sha256; q=dns/txt; c=relaxed/relaxed; 
    s=selector1-fabrikam-com; d=contoso.onmicrosoft.com; t=1429912795; 
    h=From:To:Message-ID:Subject:MIME-Version:Content-Type; 
    bh=<body hash>; 
    b=<signed field>;
```

<span data-ttu-id="96323-p125">이 예제에서는 호스트 이름 및 도메인 CNAME 도메인 관리자에 의해 활성화 되어 있던 fabrikam.com에 대 한 DKIM 서명 하는 경우에 가리키기 값이 포함 됩니다. 결국, Office 365에서 보낸 모든 단일 메시지 DKIM 서명 됩니다. 도메인에서에서 도메인 같을 수는 DKIM, 사용자가 직접 사용 하는 경우:이 사례 fabrikam.com 주소입니다. 이렇게 하지 않으면 맞추지 않습니다 하 고 대신 조직의 초기 도메인을 사용 합니다. 초기 도메인을 결정 하는 방법에 대 한 정보를 [도메인 FAQ](https://support.office.com/article/1272bad0-4bd4-4796-8005-67d6fb3afc5a#bkmk_whydoihaveanonmicrosoft.comdomain)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="96323-p125">In this example, the host name and domain contain the values to which the CNAME would point if DKIM-signing for fabrikam.com had been enabled by the domain administrator. Eventually, every single message sent from Office 365 will be DKIM-signed. If you enable DKIM yourself, the domain will be the same as the domain in the From: address, in this case fabrikam.com. If you don't, it will not align and instead will use your organization's initial domain. For information about determining your initial domain, see [Domains FAQ](https://support.office.com/article/1272bad0-4bd4-4796-8005-67d6fb3afc5a#bkmk_whydoihaveanonmicrosoft.comdomain).</span></span>
  
## <a name="set-up-dkim-so-that-a-third-party-service-can-send-or-spoof-email-on-behalf-of-your-custom-domain"></a><span data-ttu-id="96323-232">DKIM를 제 3 자 서비스 보내기, 또는 사용자 지정 도메인을 대신 하 여 전자 메일을 스푸핑할 수 있도록 설정</span><span class="sxs-lookup"><span data-stu-id="96323-232">Set up DKIM so that a third-party service can send, or spoof, email on behalf of your custom domain</span></span>
<span data-ttu-id="96323-233"><a name="SetUp3rdPartyspoof"> </a></span><span class="sxs-lookup"><span data-stu-id="96323-233"></span></span>

<span data-ttu-id="96323-p126">일부 대량 전자 메일 서비스 공급자 또는 소프트웨어로-서비스 공급자를 통해 해당 서비스에서 전송 되는 전자 메일에 대 한 DKIM 키를 설정할 수 있습니다. 이 사용자가 직접 및 제 3 자가 사이 조정이 필요한 DNS 레코드를 설정 하기 위해 필요 합니다. 두 조직 없음 동일한 방식으로 수행 합니다. 대신 하는 프로세스는 전적으로 조직에 따라 다릅니다.</span><span class="sxs-lookup"><span data-stu-id="96323-p126">Some bulk email service providers, or software-as-a-service providers, let you set up DKIM keys for email that originates from their service. This requires coordination between yourself and the third-party in order to set up the necessary DNS records. No two organizations do it exactly the same way. Instead, the process depends entirely on the organization.</span></span>
  
<span data-ttu-id="96323-238">Contoso.com 및 bulkemailprovider.com 올바르게 구성 된 DKIM를 표시 하는 예제 메시지는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="96323-238">An example message showing a properly configured DKIM for contoso.com and bulkemailprovider.com might look like this:</span></span>
  
```
Return-Path: <communication@bulkemailprovider.com>
 From: <sender@contoso.com>
 DKIM-Signature: s=s1024; d=contoso.com
 Subject: Here is a message from Bulk Email Provider's infrastructure, but with a DKIM signature authorized by contoso.com
```

<span data-ttu-id="96323-239">이 예제에서는이 결과 달성 하기 위해:</span><span class="sxs-lookup"><span data-stu-id="96323-239">In this example, in order to achieve this result:</span></span>
  
1. <span data-ttu-id="96323-240">대량 전자 메일 공급자 Contoso DKIM 공개키를 제공 했습니다.</span><span class="sxs-lookup"><span data-stu-id="96323-240">Bulk Email Provider gave Contoso a public DKIM key.</span></span>
    
2. <span data-ttu-id="96323-241">Contoso는 해당 DNS 레코드를 DKIM 키를 게시합니다.</span><span class="sxs-lookup"><span data-stu-id="96323-241">Contoso published the DKIM key to its DNS record.</span></span>
    
3. <span data-ttu-id="96323-p127">전자 메일을 보낼 때 대량 전자 메일 공급자는 해당 개인 키를 사용 하 여 키에 서명 합니다. 이렇게 하 여 대량 전자 메일 공급자는 DKIM 서명을 메시지 헤더에 연결 합니다.</span><span class="sxs-lookup"><span data-stu-id="96323-p127">When sending email, Bulk Email Provider signs the key with the corresponding private key. By doing so, Bulk Email Provider attached the DKIM signature to the message header.</span></span>
    
4. <span data-ttu-id="96323-p128">DKIM 서명 d를 인증 하 여 DKIM 확인을 수행 하는 받는 전자 메일 시스템 =\<도메인\> 에서 도메인에 대해 값: 메시지의 (5322.From) 주소입니다. 이 예제에서는 값과 일치합니다.</span><span class="sxs-lookup"><span data-stu-id="96323-p128">Receiving email systems perform a DKIM check by authenticating the DKIM-Signature d=\<domain\> value against the domain in the From: (5322.From) address of the message. In this example, the values match:</span></span>
    
    <span data-ttu-id="96323-246">**contoso.com** @ 보낸사람</span><span class="sxs-lookup"><span data-stu-id="96323-246">sender@**contoso.com**</span></span>
    
    <span data-ttu-id="96323-247">d**contoso.com** =</span><span class="sxs-lookup"><span data-stu-id="96323-247">d=**contoso.com**</span></span>
    
## <a name="next-steps-after-you-set-up-dkim-for-office-365"></a><span data-ttu-id="96323-248">다음 단계: Office 365에 대 한 DKIM를 설정한 후</span><span class="sxs-lookup"><span data-stu-id="96323-248">Next steps: After you set up DKIM for Office 365</span></span>
<span data-ttu-id="96323-249"><a name="DKIMNextSteps"> </a></span><span class="sxs-lookup"><span data-stu-id="96323-249"></span></span>

<span data-ttu-id="96323-p129">DKIM을 스푸핑을 방지 하기 위한 것 이지만 DKIM SPF 및 DMARC 더 잘 작동 합니다. SPF를 아직 설정 하지 않은 경우 DKIM을 설정한 후이 수행 해야 있습니다. SPF를 신속 하 게 구성 된 것을 간략하게 소개 합니다 [스푸핑을 방지 하기 위해 Office 365에서 SPF 설정](set-up-spf-in-office-365-to-help-prevent-spoofing.md)을 참조 하십시오. Office 365 SPF를 사용 하는 방법에 대 한 더 자세히 이해 또는 하이브리드 배포와 같은 문제해결 또는 비표준 배포에 대 한 [스푸핑을 방지 하기 위해 보낸 사람이 정책 프레임 워크 (SPF)을 사용 하 여 Office 365 방식](how-office-365-uses-spf-to-prevent-spoofing.md)으로 시작 합니다. 다음으로, [Office 365의 전자 메일의 유효성을 검사를 사용 하 여 DMARC](use-dmarc-to-validate-email.md)를 참조 하십시오. [스팸 방지 메시지 헤더](anti-spam-message-headers.md) DKIM 확인을 위한 Office 365에서 사용 되는 구문과 헤더 필드를 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="96323-p129">Although DKIM is designed to help prevent spoofing, DKIM works better with SPF and DMARC. Once you have set up DKIM, if you have not already set up SPF you should do so. For a quick introduction to SPF and to get it configured quickly, see [Set up SPF in Office 365 to help prevent spoofing](set-up-spf-in-office-365-to-help-prevent-spoofing.md). For a more in-depth understanding of how Office 365 uses SPF, or for troubleshooting or non-standard deployments such as hybrid deployments, start with [How Office 365 uses Sender Policy Framework (SPF) to prevent spoofing](how-office-365-uses-spf-to-prevent-spoofing.md). Next, see [Use DMARC to validate email in Office 365](use-dmarc-to-validate-email.md). [Anti-spam message headers](anti-spam-message-headers.md) includes the syntax and header fields used by Office 365 for DKIM checks.</span></span> 
  

