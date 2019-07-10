---
title: Exchange Online의 메시지 서명 및 암호화를 위한 S/MIME
ms.author: chrisda
author: chrisda
manager: dansimp
ms.date: ''
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 887c710b-0ec6-4ff0-8065-5f05f74afef3
description: 관리자는 Exchange Online에서 S/MIME을 사용 하는 방법에 대해 알아볼 수 있습니다.
ms.openlocfilehash: ddb244e9e0cb189dbeb78af49e34ed90f64e77cc
ms.sourcegitcommit: 32ecff689ae32c59a39b7633ca0f36a304e7516e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/09/2019
ms.locfileid: "35601095"
---
# <a name="smime-for-message-signing-and-encryption-in-exchange-online"></a><span data-ttu-id="228b0-103">Exchange Online의 메시지 서명 및 암호화를 위한 S/MIME</span><span class="sxs-lookup"><span data-stu-id="228b0-103">S/MIME for message signing and encryption in Exchange Online</span></span>

<span data-ttu-id="228b0-104">S/MIME (Secure/Expressioninternet Mail Extensions)는 디지털 서명 및 암호화 된 메시지를 보내기 위한 광범위 하 게 사용할 수 있는 방법 (보다 정확한 프로토콜)입니다.</span><span class="sxs-lookup"><span data-stu-id="228b0-104">S/MIME (Secure/Multipurpose Internet Mail Extensions) is a widely accepted method (or more precisely, a protocol) for sending digitally signed and encrypted messages.</span></span> <span data-ttu-id="228b0-105">S/MIME을 사용 하면 전자 메일을 암호화 하 고 디지털 서명을 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="228b0-105">S/MIME allows you to encrypt emails and digitally sign them.</span></span> <span data-ttu-id="228b0-106">전자 메일 메시지와 함께 S/MIME을 사용 하는 경우 해당 메시지를 받는 사용자에 게 받은 편지함에 표시 되는 내용이 보낸 사람과 정확히 일치 하는 메시지 인지 확인 하는 데 도움이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="228b0-106">When you use S/MIME with an email message, it helps the people who receive that message to be certain that what they see in their inbox is the exact message that started with the sender.</span></span> <span data-ttu-id="228b0-107">또한 메시지를 수신 하는 사용자가 보낸 사람을 가장 하는 사람이 아닌 특정 보낸 사람 으로부터 온 것을 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="228b0-107">It will also help people who receive messages to be certain that the message came from the specific sender and not from someone pretending to be the sender.</span></span> <span data-ttu-id="228b0-108">이를 위해 S/MIME는 인증, 메시지 무결성 및 원본 비 부인 (디지털 서명 사용)와 같은 암호화 보안 서비스를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="228b0-108">To do this, S/MIME provides for cryptographic security services such as authentication, message integrity, and non-repudiation of origin (using digital signatures).</span></span> <span data-ttu-id="228b0-109">또한 전자 메시징에 대 한 개인 정보 보호 및 데이터 보안 (암호화 사용)을 향상 시킬 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="228b0-109">It also helps enhance privacy and data security (using encryption) for electronic messaging.</span></span> <span data-ttu-id="228b0-110">전자 메일 컨텍스트에서 S/MIME의 기록 및 아키텍처에 대 한 자세한 내용은 [s/Mime 이해](https://go.microsoft.com/fwlink/?LinkID=393948)(영문)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="228b0-110">For a more complete background about the history and architecture of S/MIME in the context of email, see [Understanding S/MIME](https://go.microsoft.com/fwlink/?LinkID=393948).</span></span>

<span data-ttu-id="228b0-111">Exchange Online 관리자로 서 조직의 사서함에 대해 S/MIME 기반 보안을 사용 하도록 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="228b0-111">As an Exchange Online admin, you can enable S/MIME-based security for the mailboxes in your organization.</span></span> <span data-ttu-id="228b0-112">여기에 연결 된 항목의 지침을 Exchange Online PowerShell과 함께 사용 하 여 S/MIME을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="228b0-112">Use the guidance in the topics linked here along with Exchange Online PowerShell to set up S/MIME.</span></span> <span data-ttu-id="228b0-113">지원 되는 전자 메일 클라이언트에서 S/MIME을 사용 하려면 조직의 사용자에 게 서명 및 암호화를 위해 발급 된 인증서와 온-프레미스 AD DS (Active Directory 도메인 서비스)에 게시 되는 데이터를 포함 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="228b0-113">To use S/MIME in supported email clients, the users in your organization must have certificates issued for signing and encryption purposes and data published to your on-premises Active Directory Domain Service (AD DS).</span></span> <span data-ttu-id="228b0-114">AD DS는 인터넷의 클라우드 서비스 또는 원격 시설이 아닌 관리자가 제어할 수 있는 물리적 위치의 컴퓨터에 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="228b0-114">Your AD DS must be located on computers at a physical location that you control and not at a remote facility or cloud-based service somewhere on the internet.</span></span> <span data-ttu-id="228b0-115">AD DS에 대한 자세한 내용은 [Active Directory 도메인 서비스](https://go.microsoft.com/fwlink/?LinkID=394064)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="228b0-115">For more information about AD DS, see [Active Directory Domain Services](https://go.microsoft.com/fwlink/?LinkID=394064).</span></span>

## <a name="supported-scenarios-and-technical-considerations"></a><span data-ttu-id="228b0-116">지원되는 시나리오 및 기술 고려 사항</span><span class="sxs-lookup"><span data-stu-id="228b0-116">Supported scenarios and technical considerations</span></span>

<span data-ttu-id="228b0-117">다음과 같은 끝점에서 작동 하도록 S/MIME을 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="228b0-117">You can set up S/MIME to work with any of the following end points:</span></span>

- <span data-ttu-id="228b0-118">Outlook 2010 이상</span><span class="sxs-lookup"><span data-stu-id="228b0-118">Outlook 2010 or later</span></span>

- <span data-ttu-id="228b0-119">웹용 Outlook(이전 Outlook Web App)</span><span class="sxs-lookup"><span data-stu-id="228b0-119">Outlook on the web (formerly known as Outlook Web App)</span></span>

- <span data-ttu-id="228b0-120">EAS(Exchange ActiveSync)</span><span class="sxs-lookup"><span data-stu-id="228b0-120">Exchange ActiveSync (EAS)</span></span>

<span data-ttu-id="228b0-121">이러한 각 끝점에 대해 S/MIME을 설정 하기 위해 수행 하는 단계는 약간 다릅니다.</span><span class="sxs-lookup"><span data-stu-id="228b0-121">The steps that you follow to set up S/MIME with each of these end points is slightly different.</span></span> <span data-ttu-id="228b0-122">일반적으로는 다음 단계를 수행 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="228b0-122">Generally, you will need to do the following steps:</span></span>

- <span data-ttu-id="228b0-p104">S/MIME 인증서를 발급하도록 Windows 기반 인증 기관을 설치하고 공개 키 인프라를 설정합니다. 타사 인증서 공급자가 발급한 인증서도 지원됩니다. 자세한 내용은 [Active Directory 인증서 서비스 개요](https://technet.microsoft.com/library/hh831740.aspx)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="228b0-p104">Install a Windows-based Certification Authority and set up a public key infrastructure to issue S/MIME certificates. Certificates issued by third-party certificate providers are also supported. For details, see [Active Directory Certificate Services Overview](https://technet.microsoft.com/library/hh831740.aspx).</span></span>

- <span data-ttu-id="228b0-126">**UserSMIMECertificate** 및/또는 **UserCertificate** 특성의 온-프레미스 AD DS 계정에 사용자 인증서를 게시 합니다.</span><span class="sxs-lookup"><span data-stu-id="228b0-126">Publish the user certificate in an on-premises AD DS account in the **UserSMIMECertificate** and/or **UserCertificate** attributes.</span></span>

- <span data-ttu-id="228b0-p105">Exchange Online 조직의 경우 해당하는 DirSync 버전을 사용하여 AD DS에서 Azure Active Directory로 사용자 인증서를 동기화합니다. 그러면 이러한 인증서가 Azure Active Directory에서 Exchange Online 디렉터리로 동기화되며 받는 사람에 대한 메시지를 암호화할 때 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="228b0-p105">For Exchange Online organizations, synchronize the user certificates from AD DS to Azure Active Directory by using an appropriate version of DirSync. These certificates will then get synchronized from Azure Active Directory to Exchange Online directory and will be used when encrypting a message to a recipient.</span></span>

- <span data-ttu-id="228b0-129">S/MIME의 유효성을 검사하기 위해 가상 인증서 모음을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="228b0-129">Set up a virtual certificate collection in order to validate S/MIME.</span></span> <span data-ttu-id="228b0-130">이 정보는 전자 메일의 서명 유효성을 검사 하 고 신뢰할 수 있는 인증서로 서명 되었는지 확인할 때 웹에서 Outlook에서 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="228b0-130">This information is used by Outlook on the web when validating the signature of an email and ensuring that it was signed by a trusted certificate.</span></span>

- <span data-ttu-id="228b0-131">S/MIME을 사용하도록 Outlook 또는 EAS 끝점을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="228b0-131">Set up the Outlook or EAS end point to use S/MIME.</span></span>

## <a name="setup-smime-with-outlook-on-the-web"></a><span data-ttu-id="228b0-132">웹에서 Outlook을 사용 하 여 S/MIME 설정</span><span class="sxs-lookup"><span data-stu-id="228b0-132">Setup S/MIME with Outlook on the web</span></span>

<span data-ttu-id="228b0-133">Exchange Online에 대해 S/MIME을 설정 하려면 다음과 같은 주요 단계를 수행 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="228b0-133">Setting up S/MIME for Exchange Online with Outlook on the web involves the following key steps:</span></span>

1. [<span data-ttu-id="228b0-134">웹용 Outlook용 S/MIME 설정 구성</span><span class="sxs-lookup"><span data-stu-id="228b0-134">Configure S/MIME settings for Outlook on the web</span></span>](configure-s-mime-settings-for-outlook-web-app.md)

2. [<span data-ttu-id="228b0-135">S/MIME 유효성 검사를 위한 가상 인증서 컬렉션 설정</span><span class="sxs-lookup"><span data-stu-id="228b0-135">Set up virtual certificate collection to validate S/MIME</span></span>](set-up-virtual-certificate-collection-to-validate-s-mime.md)

3. [<span data-ttu-id="228b0-136">S/MIME용으로 Office 365에 사용자 인증서 동기화</span><span class="sxs-lookup"><span data-stu-id="228b0-136">Sync user certificates to Office 365 for S/MIME</span></span>](sync-user-certificates-to-office-365-for-s-mime.md)

## <a name="related-message-encryption-technologies"></a><span data-ttu-id="228b0-137">관련 메시지 암호화 기술</span><span class="sxs-lookup"><span data-stu-id="228b0-137">Related message encryption technologies</span></span>

<span data-ttu-id="228b0-138">메시지 보안이 더 중요 해지면 관리자는 보안 메시징의 원리와 개념을 이해 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="228b0-138">As message security becomes more important, admins need to understand the principles and concepts of secure messaging.</span></span> <span data-ttu-id="228b0-139">이러한 이해는 사용 가능한 다양 한 보호 관련 기술 (S/MIME 포함)이 증가 하기 때문에 특히 중요 합니다.</span><span class="sxs-lookup"><span data-stu-id="228b0-139">This understanding is especially important because of the growing variety of protection-related technologies (including S/MIME) that are available.</span></span> <span data-ttu-id="228b0-140">S/MIME 및 전자 메일과 관련하여 S/MIME이 작동하는 방식에 대해 자세히 알아보려면 [S/MIME 이해](https://go.microsoft.com/fwlink/?LinkID=393948)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="228b0-140">To understand more about S/MIME and how it works in context of email, see [Understanding S/MIME](https://go.microsoft.com/fwlink/?LinkID=393948).</span></span> <span data-ttu-id="228b0-141">다양한 암호화 기술이 연동되어 저장된 메시지 및 전송 중인 메시지를 보호합니다.</span><span class="sxs-lookup"><span data-stu-id="228b0-141">A variety of encryption technologies work together to provide protection for messages at rest and in-transit.</span></span> <span data-ttu-id="228b0-142">S/MIME은 다음 기술과 동시에 사용할 수 있지만 이러한 기술에 종속되는 것은 아닙니다.</span><span class="sxs-lookup"><span data-stu-id="228b0-142">S/MIME can work simultaneously with the following technologies but is not dependent on them:</span></span>

- <span data-ttu-id="228b0-143">**TLS(전송 계층 보안)** 는 스누핑 및 도청을 방지하기 위해 전자 메일 서버 간의 터널/경로를 암호화합니다.</span><span class="sxs-lookup"><span data-stu-id="228b0-143">**Transport Layer Security (TLS)** encrypts the tunnel or the route between email servers in order to help prevent snooping and eavesdropping.</span></span>

- <span data-ttu-id="228b0-144">**SSL(Secure Sockets Layer)** 은 전자 메일 클라이언트와 Office 365 서버 간의 연결을 암호화합니다.</span><span class="sxs-lookup"><span data-stu-id="228b0-144">**Secure Sockets Layer (SSL)** encrypts the connection between email clients and Office 365 servers.</span></span>

- <span data-ttu-id="228b0-145">**BitLocker**는 데이터 센터의 하드 드라이브에 저장된 데이터를 암호화하여 무단으로 액세스하는 사용자가 해당 데이터를 읽을 수 없도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="228b0-145">**BitLocker** encrypts the data on a hard drive in a datacenter so that if someone gets unauthorized access, they can't read it.</span></span>

### <a name="smime-compared-with-office-365-message-encryption"></a><span data-ttu-id="228b0-146">Office 365 메시지 암호화와 S/MIME 비교</span><span class="sxs-lookup"><span data-stu-id="228b0-146">S/MIME compared with Office 365 Message Encryption</span></span>

<span data-ttu-id="228b0-p108">S/MIME을 사용하려면 대개 기업 간, 그리고 기업과 소비자 간에 사용되는 게시 인프라와 인증서가 필요합니다. 사용자는 S/MIME의 암호화 키를 제어하며 보내는 각 메시지에 해당 키를 사용할지 여부를 선택할 수 있습니다. Outlook 등의 전자 메일 프로그램에서는 디지털 서명 및 서명 확인을 수행하기 위한 신뢰할 수 있는 루트 인증 기관 위치를 검색합니다. Office 365 메시지 암호화는 조직 내부 또는 외부의 모든 사용자에게 보내는 메일을 암호화하기 위해 개별 사용자가 아닌 관리자가 구성할 수 있는 정책 기반 암호화 서비스이며, RMS(Azure 권한 관리)를 기반으로 구축되며 공개 키 인프라를 사용하지 않는 온라인 서비스입니다. 또한 Office 365 메시지 암호화에서는 조직의 브랜드로 메일을 사용자 지정하는 기능 같은 추가 기능도 제공됩니다. Office 365 메시지 암호화에 대한 자세한 내용은 [Office 365 메시지 암호화](https://go.microsoft.com/fwlink/?LinkID=392525)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="228b0-p108">S/MIME requires a certificate and publishing infrastructure that is often used in business-to-business and business-to-consumer situations. The user controls the cryptographic keys in S/MIME and can choose whether to use them for each message they send. Email programs such as Outlook search a trusted root certificate authority location to perform digital signing and verification of the signature. Office 365 Message Encryption is a policy-based encryption service that can be configured by an administrator, and not an individual user, to encrypt mail sent to anyone inside or outside of the organization. It's an online service that's built on Azure Rights Management (RMS) and does not rely on a public key infrastructure. Office 365 Message Encryption also provides additional capabilities, such as the capability to customize the mail with organization's brand. For more information about Office 365 Message Encryption, see [Office 365 Message Encryption](https://go.microsoft.com/fwlink/?LinkID=392525).</span></span>

## <a name="more-information"></a><span data-ttu-id="228b0-154">추가 정보</span><span class="sxs-lookup"><span data-stu-id="228b0-154">More information</span></span>

[<span data-ttu-id="228b0-155">웹용 Outlook</span><span class="sxs-lookup"><span data-stu-id="228b0-155">Outlook on the web</span></span>](http://technet.microsoft.com/library/3814b665-01e8-4881-9a44-163f14789ee4.aspx)

[<span data-ttu-id="228b0-156">보안 메일(2000)</span><span class="sxs-lookup"><span data-stu-id="228b0-156">Secure Mail (2000)</span></span>](https://technet.microsoft.com/en-us/library/cc962043.aspx)
