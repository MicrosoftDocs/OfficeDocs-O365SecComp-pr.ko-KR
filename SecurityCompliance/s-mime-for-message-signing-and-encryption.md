---
title: Exchange Online의 메시지 서명 및 암호화를 위한 S/MIME
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 12/9/2016
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 887c710b-0ec6-4ff0-8065-5f05f74afef3
description: S/MIME을 사용 하면 전자 메일을 암호화 하 고 디지털 서명을 할 수 있습니다. 전자 메일 메시지와 함께 S/MIME을 사용 하는 경우 해당 메시지를 받는 사용자에 게 받은 편지함에 표시 되는 내용이 보낸 사람과 정확히 일치 하는 메시지 인지 확인 하는 데 도움이 됩니다.
ms.openlocfilehash: 41a84d5332092748f9a8cc8fe4936c39e5fd2012
ms.sourcegitcommit: 06d6e63225f912d0f3c6bb836c61eb11c1dbe97a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/22/2019
ms.locfileid: "30206511"
---
# <a name="smime-for-message-signing-and-encryption"></a><span data-ttu-id="2d912-104">메시지 서명 및 암호화를 위한 S/MIME</span><span class="sxs-lookup"><span data-stu-id="2d912-104">S/MIME for message signing and encryption</span></span>

<span data-ttu-id="2d912-p102">S/MIME(Secure/Multipurpose Internet Mail Extensions)은 디지털 서명된 메시지와 암호화된 메시지를 보내는 데 널리 사용되는 방법(정확하게는 프로토콜)입니다. S/MIME을 사용하면 전자 메일을 암호화하고 디지털로 서명할 수 있습니다. 전자 메일 메시지에 S/MIME을 사용하면 해당 메시지를 받는 사람이 받은 편지함에 표시된 메시지가 보낸 사람이 작성한 것과 정확히 일치하는 메시지이며, 특정 보낸 사람을 가장하는 사람이 아닌 실제 보낸 사람이 메시지를 보냈음을 확신할 수 있습니다. 이를 위해 S/MIME에서는 디지털 서명을 사용하여 인증, 메시지 무결성, 원본 거부 없음 등의 암호화 보안 서비스가 제공됩니다. 또한 전자 방식 메시징을 위해 암호화를 사용하여 개인 정보와 데이터 보안이 개선될 수 있도록 합니다. 전자 메일 분야에서 S/MIME의 발전 이력과 구조에 대한 전체 배경 정보를 파악하려면 [S/MIME 이해](https://go.microsoft.com/fwlink/?LinkID=393948)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="2d912-p102">S/MIME (Secure/Multipurpose Internet Mail Extensions) is a widely accepted method, or more precisely a protocol, for sending digitally signed and encrypted messages. S/MIME allows you to encrypt emails and digitally sign them. When you use S/MIME with an email message, it helps the people who receive that message to be certain that what they see in their inbox is the exact message that started with the sender. It will also help people who receive messages to be certain that the message came from the specific sender and not from someone pretending to be the sender. To do this, S/MIME provides for cryptographic security services such as authentication, message integrity, and non-repudiation of origin (using digital signatures). It also helps enhance privacy and data security (using encryption) for electronic messaging. For a more complete background about the history and architecture of S/MIME in the context of email, see [Understanding S/MIME](https://go.microsoft.com/fwlink/?LinkID=393948).</span></span> 
  
<span data-ttu-id="2d912-p103">Exchange 2013 SP1 또는 Exchange Online(Office 365의 일부분)에 사서함이 있는 경우 관리자는 조직에 대해 S/MIME 기반 보안을 사용하도록 설정할 수 있습니다. 아래에 링크되어 있는 항목의 지침에 따라 Exchange 관리 셸을 사용하여 S/MIME을 설정합니다. Exchange 2013 SP1 또는 Exchange Online을 통해 지원되는 Outlook 또는 ActiveSync 버전에서 S/MIME을 사용하려면 조직의 사용자에게 서명 및 암호화용으로 발급된 인증서가 있어야 하며 데이터를 온-프레미스 AD DS(Active Directory 도메인 서비스)에 게시해야 합니다. AD DS는 인터넷의 클라우드 서비스 또는 원격 시설이 아닌 관리자가 제어할 수 있는 물리적 위치의 컴퓨터에 있어야 합니다. AD DS에 대한 자세한 내용은 [Active Directory 도메인 서비스](https://go.microsoft.com/fwlink/?LinkID=394064)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="2d912-p103">As an administrator, you can enable S/MIME-based security for your organization if you have mailboxes in either Exchange 2013 SP1 or Exchange Online, a part of Office 365. Use the guidance in the topics linked here along with the Exchange Management Shell to set up S/MIME. To use S/MIME in supported versions of Outlook or ActiveSync, with either Exchange 2013 SP1 or Exchange Online, the users in your organization must have certificates issued for signing and encryption purposes and data published to your on-premises Active Directory Domain Service (AD DS). Your AD DS must be located on computers at a physical location that you control and not at a remote facility or cloud-based service somewhere on the internet. For more information about AD DS, see [Active Directory Domain Services](https://go.microsoft.com/fwlink/?LinkID=394064).</span></span>
  
## <a name="supported-scenarios-and-technical-considerations"></a><span data-ttu-id="2d912-117">지원되는 시나리오 및 기술 고려 사항</span><span class="sxs-lookup"><span data-stu-id="2d912-117">Supported scenarios and technical considerations</span></span>
<span data-ttu-id="2d912-118"><a name="sectionSection0"> </a></span><span class="sxs-lookup"><span data-stu-id="2d912-118"></span></span>

<span data-ttu-id="2d912-119">다음과 같은 끝점에서 작동 하도록 S/MIME을 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2d912-119">You can set up S/MIME to work with any of the following end points:</span></span> 
  
- <span data-ttu-id="2d912-120">Outlook 2010 이상</span><span class="sxs-lookup"><span data-stu-id="2d912-120">Outlook 2010 or later</span></span>
    
- <span data-ttu-id="2d912-121">웹용 Outlook(이전 Outlook Web App)</span><span class="sxs-lookup"><span data-stu-id="2d912-121">Outlook on the web (formerly known as Outlook Web App)</span></span>
    
- <span data-ttu-id="2d912-122">EAS(Exchange ActiveSync)</span><span class="sxs-lookup"><span data-stu-id="2d912-122">Exchange ActiveSync (EAS)</span></span>
    
<span data-ttu-id="2d912-p104">이러한 각 끝점에 대해 S/MIME을 설정하기 위해 수행하는 단계는 선택하는 항목에 따라 약간씩 다릅니다. 일반적으로는 다음 작업을 수행해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="2d912-p104">The steps that you follow to set up S/MIME with each of these end points is slightly different depending on which you choose. Generally, you will need to accomplish the following:</span></span>
  
- <span data-ttu-id="2d912-p105">S/MIME 인증서를 발급하도록 Windows 기반 인증 기관을 설치하고 공개 키 인프라를 설정합니다. 타사 인증서 공급자가 발급한 인증서도 지원됩니다. 자세한 내용은 [Active Directory 인증서 서비스 개요](https://technet.microsoft.com/library/hh831740.aspx)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="2d912-p105">Install a Windows-based Certification Authority and set up a public key infrastructure to issue S/MIME certificates. Certificates issued by third-party certificate providers are also supported. For details, see [Active Directory Certificate Services Overview](https://technet.microsoft.com/library/hh831740.aspx).</span></span>
    
- <span data-ttu-id="2d912-128">UserSMIMECertificate 및/또는 UserCertificate 특성의 온-프레미스 AD DS 계정으로 사용자 인증서를 게시합니다.</span><span class="sxs-lookup"><span data-stu-id="2d912-128">Publish the user certificate in an on-premises AD DS account in the UserSMIMECertificate and/or UserCertificate attributes.</span></span>
    
- <span data-ttu-id="2d912-p106">Exchange Online 조직의 경우 해당하는 DirSync 버전을 사용하여 AD DS에서 Azure Active Directory로 사용자 인증서를 동기화합니다. 그러면 이러한 인증서가 Azure Active Directory에서 Exchange Online 디렉터리로 동기화되며 받는 사람에 대한 메시지를 암호화할 때 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="2d912-p106">For Exchange Online organizations, synchronize the user certificates from AD DS to Azure Active Directory by using an appropriate version of DirSync. These certificates will then get synchronized from Azure Active Directory to Exchange Online directory and will be used when encrypting a message to a recipient.</span></span>
    
- <span data-ttu-id="2d912-p107">S/MIME의 유효성을 검사 하기 위해 가상 인증서 컬렉션을 설정 합니다. 이 정보는 전자 메일의 서명 유효성을 검사 하 고 신뢰할 수 있는 인증서에 의해 서명 되었는지 확인할 때 웹 (이전에는 웹에서 outlook 이라고 함)의 outlook에서 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="2d912-p107">Set up a virtual certificate collection in order to validate S/MIME. This information is used by Outlook on the web (formerly known as Outlook on the web) when validating the signature of an email and ensuring that it was signed by a trusted certificate.</span></span>
    
- <span data-ttu-id="2d912-133">S/MIME을 사용하도록 Outlook 또는 EAS 끝점을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="2d912-133">Set up the Outlook or EAS end point to use S/MIME.</span></span> 
    
## <a name="setup-smime-with-outlook-on-the-web"></a><span data-ttu-id="2d912-134">웹에서 Outlook을 사용 하 여 S/MIME 설정</span><span class="sxs-lookup"><span data-stu-id="2d912-134">Setup S/MIME with Outlook on the web</span></span>
<span data-ttu-id="2d912-135"><a name="sectionSection1"> </a></span><span class="sxs-lookup"><span data-stu-id="2d912-135"></span></span>

<span data-ttu-id="2d912-136">Exchange Online에 대해 S/MIME을 설정 하려면 다음과 같은 주요 단계를 수행 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="2d912-136">Setting up S/MIME for Exchange Online with Outlook on the web involves the following key steps:</span></span>
  
1. [<span data-ttu-id="2d912-137">웹용 Outlook에 대 한 S/MIME 설정 구성</span><span class="sxs-lookup"><span data-stu-id="2d912-137">Configure S/MIME settings for Outlook on the web</span></span>](configure-s-mime-settings-for-outlook-web-app.md)
    
2. [<span data-ttu-id="2d912-138">S/MIME 유효성 검사를 위한 가상 인증서 컬렉션 설정</span><span class="sxs-lookup"><span data-stu-id="2d912-138">Set up virtual certificate collection to validate S/MIME</span></span>](set-up-virtual-certificate-collection-to-validate-s-mime.md)
    
3. <span data-ttu-id="2d912-139">[S/MIME 용으로 Office 365에 사용자 인증서 동기화](sync-user-certificates-to-office-365-for-s-mime.md) 이 단계는 Exchange Online에만 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="2d912-139">[Sync user certificates to Office 365 for S/MIME](sync-user-certificates-to-office-365-for-s-mime.md) This step applies to Exchange Online only.</span></span> 
    
## <a name="related-message-encryption-technologies"></a><span data-ttu-id="2d912-140">관련 메시지 암호화 기술</span><span class="sxs-lookup"><span data-stu-id="2d912-140">Related message encryption technologies</span></span>
<span data-ttu-id="2d912-141"><a name="sectionSection2"> </a></span><span class="sxs-lookup"><span data-stu-id="2d912-141"></span></span>

<span data-ttu-id="2d912-p108">메시지 보안의 중요도가 높아지면서 관리자는 메시지 보호 원칙 및 개념을 이해해야 합니다. 특히 S/MIME 등의 다양한 보호 관련 기술이 제공되면서 이러한 이해의 중요성도 더욱 높아지고 있습니다. S/MIME 및 전자 메일과 관련하여 S/MIME이 작동하는 방식에 대해 자세히 알아보려면 [S/MIME 이해](https://go.microsoft.com/fwlink/?LinkID=393948)를 참조하세요. 다양한 암호화 기술이 연동되어 저장된 메시지 및 전송 중인 메시지를 보호합니다. S/MIME은 다음 기술과 동시에 사용할 수 있지만 이러한 기술에 종속되는 것은 아닙니다.</span><span class="sxs-lookup"><span data-stu-id="2d912-p108">As message security becomes more important, administrators need to understand the principles and concepts of secure messaging. This understanding is especially important because of the growing variety of protection-related technologies, such as S/MIME, that have become available. To understand more about S/MIME and how it works in context of email, see [Understanding S/MIME](https://go.microsoft.com/fwlink/?LinkID=393948). A variety of encryption technologies work together to provide protection for messages at rest and in-transit. S/MIME can work simultaneously with the following technologies but is not dependent on them:</span></span>
  
> <span data-ttu-id="2d912-147">**TLS(전송 계층 보안)** 는 스누핑 및 도청을 방지하기 위해 전자 메일 서버 간의 터널/경로를 암호화합니다.</span><span class="sxs-lookup"><span data-stu-id="2d912-147">**Transport Layer Security (TLS)** encrypts the tunnel or the route between email servers in order to help prevent snooping and eavesdropping.</span></span> 
    
> <span data-ttu-id="2d912-148">**SSL(Secure Sockets Layer)** 은 전자 메일 클라이언트와 Office 365 서버 간의 연결을 암호화합니다.</span><span class="sxs-lookup"><span data-stu-id="2d912-148">**Secure Sockets Layer (SSL)** encrypts the connection between email clients and Office 365 servers.</span></span> 
    
> <span data-ttu-id="2d912-149">**BitLocker**는 데이터 센터의 하드 드라이브에 저장된 데이터를 암호화하여 무단으로 액세스하는 사용자가 해당 데이터를 읽을 수 없도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="2d912-149">**BitLocker** encrypts the data on a hard drive in a datacenter so that if someone gets unauthorized access, they can't read it.</span></span> 
    
### <a name="smime-compared-with-office-365-message-encryption"></a><span data-ttu-id="2d912-150">Office 365 메시지 암호화와 S/MIME 비교</span><span class="sxs-lookup"><span data-stu-id="2d912-150">S/MIME compared with Office 365 Message Encryption</span></span>

<span data-ttu-id="2d912-p109">S/MIME을 사용하려면 대개 기업 간, 그리고 기업과 소비자 간에 사용되는 게시 인프라와 인증서가 필요합니다. 사용자는 S/MIME의 암호화 키를 제어하며 보내는 각 메시지에 해당 키를 사용할지 여부를 선택할 수 있습니다. Outlook 등의 전자 메일 프로그램에서는 디지털 서명 및 서명 확인을 수행하기 위한 신뢰할 수 있는 루트 인증 기관 위치를 검색합니다. Office 365 메시지 암호화는 조직 내부 또는 외부의 모든 사용자에게 보내는 메일을 암호화하기 위해 개별 사용자가 아닌 관리자가 구성할 수 있는 정책 기반 암호화 서비스이며, RMS(Azure 권한 관리)를 기반으로 구축되며 공개 키 인프라를 사용하지 않는 온라인 서비스입니다. 또한 Office 365 메시지 암호화에서는 조직의 브랜드로 메일을 사용자 지정하는 기능 같은 추가 기능도 제공됩니다. Office 365 메시지 암호화에 대한 자세한 내용은 [Office 365 메시지 암호화](https://go.microsoft.com/fwlink/?LinkID=392525)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="2d912-p109">S/MIME requires a certificate and publishing infrastructure that is often used in business-to-business and business-to-consumer situations. The user controls the cryptographic keys in S/MIME and can choose whether to use them for each message they send. Email programs such as Outlook search a trusted root certificate authority location to perform digital signing and verification of the signature. Office 365 Message Encryption is a policy-based encryption service that can be configured by an administrator, and not an individual user, to encrypt mail sent to anyone inside or outside of the organization. It's an online service that's built on Azure Rights Management (RMS) and does not rely on a public key infrastructure. Office 365 Message Encryption also provides additional capabilities, such as the capability to customize the mail with organization's brand. For more information about Office 365 Message Encryption, see [Office 365 Message Encryption](https://go.microsoft.com/fwlink/?LinkID=392525).</span></span>
  
## <a name="more-information"></a><span data-ttu-id="2d912-158">추가 정보</span><span class="sxs-lookup"><span data-stu-id="2d912-158">More information</span></span>
<span data-ttu-id="2d912-159"><a name="sectionSection3"> </a></span><span class="sxs-lookup"><span data-stu-id="2d912-159"></span></span>

[<span data-ttu-id="2d912-160">웹용 Outlook</span><span class="sxs-lookup"><span data-stu-id="2d912-160">Outlook on the web</span></span>](http://technet.microsoft.com/library/3814b665-01e8-4881-9a44-163f14789ee4.aspx)
  
[<span data-ttu-id="2d912-161">보안 메일(2000)</span><span class="sxs-lookup"><span data-stu-id="2d912-161">Secure Mail (2000)</span></span>](https://technet.microsoft.com/en-us/library/cc962043.aspx)
  

