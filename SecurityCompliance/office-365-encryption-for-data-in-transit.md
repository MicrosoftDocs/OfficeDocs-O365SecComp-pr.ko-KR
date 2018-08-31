---
title: 데이터 전송에 대 한 office 365 암호화
ms.author: robmazz
author: robmazz
manager: laurawi
ms.date: 8/21/2018
audience: ITPro
ms.topic: article
ms.service: Office 365 Administration
localization_priority: None
search.appverid:
- MET150
ms.collection: Strat_O365_Enterprise
description: '요약: Microsoft에서 전송 된 데이터를 암호화 하는 방법에 대 한 간략 한 설명 합니다.'
ms.openlocfilehash: 8f4781cf1127fb1b6bf742c267c76e3df39b8209
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22532952"
---
# <a name="office-365-encryption-for-data-in-transit"></a><span data-ttu-id="ba6a5-103">데이터 전송에 대 한 office 365 암호화</span><span class="sxs-lookup"><span data-stu-id="ba6a5-103">Office 365 encryption for data in transit</span></span>

<span data-ttu-id="ba6a5-104">보관 된 고객 데이터를 보호 하는 경우, 외에도 Microsoft 암호화 기술을 사용 하 여 전송 중에 Office 365 고객 데이터를 보호 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba6a5-104">In addition to protecting customer data at rest, Microsoft uses encryption technologies to protect Office 365 customer data in transit.</span></span> 

<span data-ttu-id="ba6a5-105">데이터를 전송에서 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba6a5-105">Data is in transit:</span></span>
- <span data-ttu-id="ba6a5-106">클라이언트 컴퓨터는 Office 365 서버와 통신 하는 경우</span><span class="sxs-lookup"><span data-stu-id="ba6a5-106">when a client machine communicates with an Office 365 server;</span></span>
- <span data-ttu-id="ba6a5-107">Office 365 서버는 다른 Office 365 서버와 통신 하는 경우 및</span><span class="sxs-lookup"><span data-stu-id="ba6a5-107">when an Office 365 server communicates with another Office 365 server; and</span></span>
- <span data-ttu-id="ba6a5-108">때 Office 365 서버를 Office 365가 아닌 서버 (예: Exchange Online 전달 전자 메일을 외부 전자 메일 서버)와 통신합니다.</span><span class="sxs-lookup"><span data-stu-id="ba6a5-108">when an Office 365 server communicates with a non-Office 365 server (e.g., Exchange Online delivering email to a foreign email server).</span></span>

<span data-ttu-id="ba6a5-p101">Office 365 서버 간의 데이터 센터 간 통신 TLS 또는 IPsec을 통해 이루어집니다 및 TLS를 사용 하 여 클라이언트 컴퓨터와 보안 세션을 협상 하는 모든 고객 관련 서버 (예: Exchange Online 사용 하 여 TLS 1.2 256 비트 암호화 강도 함께 사용 됩니다 (FIPS 2-유효성을 검사 하는 140-2 수준). (Office 365에서 지원 되는 TLS 암호화 제품군의 목록에 대 한 [Office 365의 암호화에 대 한 자세한 내용은 기술 참조 (영문)을](https://support.office.com/article/Technical-reference-details-about-encryption-in-Office-365-862CBE93-4268-4EF9-BA79-277545ECF221) 참조 하십시오.) 이 비즈니스 및 웹 (예: HTTP, POP3 등)에 Outlook에 대 한 Outlook, Skype와 같은 클라이언트에서 사용 되는 프로토콜에 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ba6a5-p101">Inter-datacenter communications between Office 365 servers takes place over TLS or IPsec, and all customer-facing servers negotiate a secure session using TLS with client machines (e.g., Exchange Online uses TLS 1.2 with 256-bit cipher strength is used (FIPS 140-2 Level 2-validated). (See [Technical reference details about encryption in Office 365](https://support.office.com/article/Technical-reference-details-about-encryption-in-Office-365-862CBE93-4268-4EF9-BA79-277545ECF221) for a list of TLS cipher suites supported by Office 365.) This applies to the protocols that are used by clients such as Outlook, Skype for Business, and Outlook on the web (e.g., HTTP, POP3, etc.).</span></span>

<span data-ttu-id="ba6a5-p102">공용 인증서는 SSLAdmin, 기밀성 전송 된 정보를 보호 하는 내부 Microsoft 도구를 사용 하 여 Microsoft IT SSL에서 발급 됩니다. Microsoft IT에서 발급 한 모든 인증서의 길이, 2048 비트의 최소 있고 [Webtrust](http://www.webtrust.org/homepage-documents/item70372.pdf) 준수 Microsoft가 소유 하는 공용 IP 주소에만 인증서가 발급 되었는지 확인 하려면 SSLAdmin 필요 합니다. 이 조건을 만족 하지 않아야 하는 모든 IP 주소는 예외 프로세스를 통해 라우팅됩니다.</span><span class="sxs-lookup"><span data-stu-id="ba6a5-p102">The public certificates are issued by Microsoft IT SSL using SSLAdmin, an internal Microsoft tool to protect confidentiality of transmitted information. All certificates issued by Microsoft IT have a minimum of 2048 bits in length, and [Webtrust](http://www.webtrust.org/homepage-documents/item70372.pdf) compliance requires SSLAdmin to make sure that certificates are issued only to public IP addresses owned by Microsoft. Any IP addresses that fail to meet this criterion are routed through an exception process.</span></span>

<span data-ttu-id="ba6a5-p103">사용 중인 TLS의 버전, 앞으로 완전 보안 (FS)의 사용 가능 여부, 암호화 제품군 등의 순서와 같은 모든 구현 세부 정보를 공개적으로 사용할 수 있습니다. 이러한 세부 정보를 참조 하는 한 가지 방법은 Qualys SSL 랩 (www.ssllabs.com)와 같은 제 3 자 웹사이트를 사용 하는 것입니다. 아래 링크에는 다음과 같은 서비스에 대 한 정보를 표시 하는 Qualys에서 자동화 된 테스트 페이지에는:</span><span class="sxs-lookup"><span data-stu-id="ba6a5-p103">All implementation details such as the version of TLS being used, whether Forward Secrecy (FS) is enabled, the order of cipher suites, etc., are available publicly. One way to see these details is to use a third-party website, such as Qualys SSL Labs (www.ssllabs.com). Below are the links to automated test pages from Qualys that display information for the following services:</span></span>
- [<span data-ttu-id="ba6a5-117">Office 365 포털</span><span class="sxs-lookup"><span data-stu-id="ba6a5-117">Office 365 Portal</span></span>](https://www.ssllabs.com/ssltest/analyze.html?d=portal.office.com&hideResults=on)
- [<span data-ttu-id="ba6a5-118">Exchange Online</span><span class="sxs-lookup"><span data-stu-id="ba6a5-118">Exchange Online</span></span>](https://www.ssllabs.com/ssltest/analyze.html?d=outlook.office365.com&hideResults=on)
- [<span data-ttu-id="ba6a5-119">SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="ba6a5-119">SharePoint Online</span></span>](https://www.ssllabs.com/ssltest/analyze.html?d=microsoft-my.sharepoint.com&hideResults=on)
- [<span data-ttu-id="ba6a5-120">비즈니스 (SIP)에 대 한 Skype</span><span class="sxs-lookup"><span data-stu-id="ba6a5-120">Skype for Business (SIP)</span></span>](https://www.ssllabs.com/ssltest/analyze.html?d=sipdir.online.lync.com)
- [<span data-ttu-id="ba6a5-121">비즈니스 (웹)에 대 한 Skype</span><span class="sxs-lookup"><span data-stu-id="ba6a5-121">Skype for Business (Web)</span></span>](https://www.ssllabs.com/ssltest/analyze.html?d=webdir.online.lync.com&hideResults=on)
- [<span data-ttu-id="ba6a5-122">Exchange Online Protection</span><span class="sxs-lookup"><span data-stu-id="ba6a5-122">Exchange Online Protection</span></span>](https://ssl-tools.net/mailservers/microsoft-com.mail.protection.outlook.com)
- [<span data-ttu-id="ba6a5-123">Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="ba6a5-123">Microsoft Teams</span></span>](https://www.ssllabs.com/ssltest/analyze.html?d=teams.microsoft.com&latest)

<span data-ttu-id="ba6a5-124">Exchange Online 보호에 대 한 Url 마다 다른 테 넌 트 이름입니다. 그러나 모든 고객 **microsoft com.mail.protection.outlook.com**를 사용 하 여 Office 365를 테스트할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ba6a5-124">For Exchange Online Protection, URLs vary by tenant names; however, all customers can test Office 365 using **microsoft-com.mail.protection.outlook.com**.</span></span>
