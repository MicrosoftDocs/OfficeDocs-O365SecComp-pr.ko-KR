---
title: How Exchange Online secures your email secrets
ms.author: tracyp
author: MSFTTracyP
manager: laurawi
ms.date: 5/24/2018
ms.audience: ITPro
ms.topic: reference
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 989ba10c-f73f-4efb-ad1b-af3322e5f376
ms.collection:
- M365-security-compliance
description: office 365의 보안, 개인 정보 및 규정 준수 정보를 제공 하는 office 365 보안 센터 외에 office 365에서 데이터 센터에 제공 하는 비밀을 보호 하는 방법을 알고 싶을 수 있습니다. DKM (Distributed Key Manager) 라는 기술을 사용 합니다.
ms.openlocfilehash: ba4c661899273f5e07c2468631298f5500d0e32f
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32255486"
---
# <a name="how-exchange-online-secures-your-email-secrets"></a><span data-ttu-id="4b762-104">How Exchange Online secures your email secrets</span><span class="sxs-lookup"><span data-stu-id="4b762-104">How Exchange Online secures your email secrets</span></span>

<span data-ttu-id="4b762-105">이 문서에서는 Microsoft가 데이터 센터에서 사용자의 전자 메일 암호를 보호하는 방법을 서명합니다.</span><span class="sxs-lookup"><span data-stu-id="4b762-105">This article describes how Microsoft secures your email secrets in its datacenters.</span></span>
  
## <a name="how-do-we-secure-secret-information-provided-by-you"></a><span data-ttu-id="4b762-106">사용자가 제공한 암호 정보는 어떻게 보호됩니까?</span><span class="sxs-lookup"><span data-stu-id="4b762-106">How do we secure secret information provided by you?</span></span>

<span data-ttu-id="4b762-107">office [365의 보안, 개인 정보 및 규정 준수 정보](https://go.microsoft.com/fwlink/?linkid=874644)를 제공 하는 office 365 보안 센터 외에 office 365에서 데이터 센터에 제공 하는 비밀을 보호 하는 방법을 알고 싶을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4b762-107">In addition to the Office 365 Trust Center which provides [Security, Privacy and Compliance Information for Office 365](https://go.microsoft.com/fwlink/?linkid=874644), you might want to know how Office 365 helps protects secrets you provide in its datacenters.</span></span> <span data-ttu-id="4b762-108">DKM (Distributed Key Manager) 라는 기술을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="4b762-108">We use a technology called Distributed Key Manager (DKM).</span></span>
  
<span data-ttu-id="4b762-p103">DKM(Distributed Key Manager)은 암호 키 집합을 사용하여 정보를 암호화 및 해독하는 클라이언트 쪽 기능입니다. Active Directory 도메인 서비스에서 특정 보안 그룹의 구성원만 DKM으로 암호화된 데이터를 해독하기 위해 해당 키에 액세스할 수 있습니다. Exchange Online에서는 Exchange 프로세스가 실행되는 특정 서비스 계정만 해당 보안 그룹에 속합니다. 데이터 센터의 표준 운영 절차의 일부로, 이 보안 그룹에 속하는 사용자에게 자격 증명이 제공되지 않으므로 이러한 암호를 해독할 수 있는 키에 액세스할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="4b762-p103">Distributed Key Manager (DKM) is a client-side functionality that uses a set of secret keys to encrypt and decrypt information. Only members of a specific security group in Active Directory Domain Services can access those keys in order to decrypt the data that is encrypted by DKM. In Exchange Online, only certain service accounts under which the Exchange processes run are part of that security group. As part of standard operating procedure in the datacenter, no human is given credentials that are part of this security group and therefore no human has access to the keys that can decrypt these secrets.</span></span>
  
<span data-ttu-id="4b762-p104">디버깅, 문제 해결 또는 감사 목적으로, 데이터 센터 관리자는 보안 그룹에 속하는 임시 자격 증명을 획득하기 위해 승격된 액세스 권한을 요청해야 합니다. 이 프로세스에는 여러 수준의 법적 승인이 필요합니다. 액세스가 허용되면 모든 작업이 기록되고 감사됩니다. 또한 액세스 권한은 설정된 시간 간격 동안만 부여되며 그 이후에는 자동으로 만료됩니다.</span><span class="sxs-lookup"><span data-stu-id="4b762-p104">For debugging, troubleshooting, or auditing purposes, a datacenter administrator must request elevated access to gain temporary credentials that are part of the security group. This process requires multiple levels of legal approval. If access is granted, all activity is logged and audited. In addition access is only granted for a set interval of time after which it automatically expires.</span></span>
  
<span data-ttu-id="4b762-117">추가 보호를 위해 DKM 기술에는 자동화된 키 롤오버 및 보관 기능이 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="4b762-117">For extra protection, DKM technology includes automated key rollover and archiving.</span></span> <span data-ttu-id="4b762-118">따라서 동일한 키를 무제한으로 사용하지는 않으면서 이전 콘텐츠에 계속 액세스할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4b762-118">This also ensures that you can continue to access your older content without having to rely on the same key indefinitely.</span></span>
  
## <a name="where-does-exchange-online-make-use-of-dkm"></a><span data-ttu-id="4b762-119">Exchange Online은 어디에서 DKM을 사용합니까?</span><span class="sxs-lookup"><span data-stu-id="4b762-119">Where does Exchange Online make use of DKM?</span></span>

<span data-ttu-id="4b762-p106">Microsoft는 Exchange Online 데이터 센터에서 DKM을 사용하여 암호를 암호화합니다. 예를 들면 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="4b762-p106">Microsoft uses DKM to encrypt your secrets in Exchange Online datacenters. For example:</span></span>
  
- <span data-ttu-id="4b762-p107">연결된 계정에 대한 전자 메일 계정 자격 증명. 연결된 계정은 Hotmail, Gmail 및 yahoo! 메일 계정과 같은 타사 계정입니다.</span><span class="sxs-lookup"><span data-stu-id="4b762-p107">Email account credentials for connected accounts. Connected accounts are third-party accounts such as Hotmail, Gmail, and Yahoo! mail accounts.</span></span>
    
- <span data-ttu-id="4b762-125">RMS(권한 관리 서비스) 루트 키.</span><span class="sxs-lookup"><span data-stu-id="4b762-125">Rights Management service (RMS) root keys.</span></span> <span data-ttu-id="4b762-126">RMS 또는 Office 365 메시지 암호화 (OME)를 사용 하 여 전자 메일을 암호화 하 고 암호를 해독 하는 데 사용 되는 Azure rms 또는 고객의 온-프레미스 Active Directory 도메인 서비스 RMS 배포에서 가져오는 고객 키입니다.</span><span class="sxs-lookup"><span data-stu-id="4b762-126">These are customer keys that are either imported from Azure RMS or from customer's on-premises Active Directory Domain Services RMS deployments that are used for encrypting and decrypting emails with RMS or Office 365 Message Encryption (OME).</span></span>
    
## <a name="related-topics"></a><span data-ttu-id="4b762-127">관련 항목</span><span class="sxs-lookup"><span data-stu-id="4b762-127">Related topics</span></span>

[<span data-ttu-id="4b762-128">Office 365의 암호화</span><span class="sxs-lookup"><span data-stu-id="4b762-128">Encryption in Office 365</span></span>](encryption.md)
  
[<span data-ttu-id="4b762-129">Office 365의 암호화에 대한 기술 관련 세부 정보</span><span class="sxs-lookup"><span data-stu-id="4b762-129">Technical reference details about encryption in Office 365</span></span>](technical-reference-details-about-encryption.md)
  
[<span data-ttu-id="4b762-130">Office 365 보안 &amp; 및 준수 센터의 서비스 보증</span><span class="sxs-lookup"><span data-stu-id="4b762-130">Service assurance in the Office 365 Security &amp; Compliance Center</span></span>](https://go.microsoft.com/fwlink/?linkid=874645)
  

