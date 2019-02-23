---
title: 전송 중인 데이터에 대 한 Office 365 암호화
ms.author: krowley
author: kccross
manager: laurawi
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: None
search.appverid:
- MET150
ms.collection: Strat_O365_Enterprise
description: '요약: Microsoft가 전송 중인 데이터를 암호화 하는 방법에 대 한 간략 한 설명입니다.'
ms.openlocfilehash: 987e923e242b47b07ad1ef65e5c7ce791c27d5bd
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30217508"
---
# <a name="office-365-encryption-for-data-in-transit"></a><span data-ttu-id="352be-103">전송 중인 데이터에 대 한 Office 365 암호화</span><span class="sxs-lookup"><span data-stu-id="352be-103">Office 365 encryption for data in transit</span></span>

<span data-ttu-id="352be-104">Microsoft는 휴지 시간에 고객 데이터를 보호 하는 것 외에도 암호화 기술을 사용 하 여 전송 중에 Office 365 고객 데이터를 보호 합니다.</span><span class="sxs-lookup"><span data-stu-id="352be-104">In addition to protecting customer data at rest, Microsoft uses encryption technologies to protect Office 365 customer data in transit.</span></span> 

<span data-ttu-id="352be-105">전송 중인 데이터:</span><span class="sxs-lookup"><span data-stu-id="352be-105">Data is in transit:</span></span>
- <span data-ttu-id="352be-106">클라이언트 시스템이 Office 365 서버와 통신 하는 경우</span><span class="sxs-lookup"><span data-stu-id="352be-106">when a client machine communicates with an Office 365 server;</span></span>
- <span data-ttu-id="352be-107">office 365 서버가 다른 office 365 서버와 통신 하는 경우 한</span><span class="sxs-lookup"><span data-stu-id="352be-107">when an Office 365 server communicates with another Office 365 server; and</span></span>
- <span data-ttu-id="352be-108">office 365 서버가 타사 365 서버와 통신 하는 경우 (예: Exchange Online에서 외부 전자 메일 서버로 전자 메일 배달)</span><span class="sxs-lookup"><span data-stu-id="352be-108">when an Office 365 server communicates with a non-Office 365 server (e.g., Exchange Online delivering email to a foreign email server).</span></span>

<span data-ttu-id="352be-p101">tls 또는 IPsec을 통해 Office 365 서버 간의 데이터 센터 간 통신을 수행 하 고, 모든 고객 연결 서버가 클라이언트 컴퓨터와 tls를 사용 하 여 보안 세션을 협상 합니다 (예: Exchange Online은 사용 하는 tls 1.2 with 256 비트 암호화 강도가 사용 됨) (FIPS 140-2 수준 2-유효성 검사 됨) office 365에서 지 원하는 TLS 암호 제품군 목록은 [office 365의 암호화에 대 한 기술 참조 세부 정보](https://support.office.com/article/Technical-reference-details-about-encryption-in-Office-365-862CBE93-4268-4EF9-BA79-277545ECF221) 를 참조 하세요. 이는 outlook, 비즈니스용 Skype, 웹에서 outlook과 같은 클라이언트에서 사용 하는 프로토콜에 적용 됩니다 (예: HTTP, POP3 등).</span><span class="sxs-lookup"><span data-stu-id="352be-p101">Inter-datacenter communications between Office 365 servers takes place over TLS or IPsec, and all customer-facing servers negotiate a secure session using TLS with client machines (e.g., Exchange Online uses TLS 1.2 with 256-bit cipher strength is used (FIPS 140-2 Level 2-validated). (See [Technical reference details about encryption in Office 365](https://support.office.com/article/Technical-reference-details-about-encryption-in-Office-365-862CBE93-4268-4EF9-BA79-277545ECF221) for a list of TLS cipher suites supported by Office 365.) This applies to the protocols that are used by clients such as Outlook, Skype for Business, and Outlook on the web (e.g., HTTP, POP3, etc.).</span></span>

<span data-ttu-id="352be-p102">공용 인증서는 전송 되는 정보의 기밀성을 보호 하기 위한 내부 microsoft 도구인 ssladmin을 사용 하 여 microsoft IT SSL에서 발급 합니다. microsoft IT에서 발급 한 모든 인증서의 길이는 최소 2048 비트 이며 [webtrust](http://www.webtrust.org/homepage-documents/item70372.pdf) 준수를 사용 하려면 인증서가 Microsoft에서 소유한 공용 IP 주소에만 발급 되도록 해야 합니다. 이 조건을 충족 하지 못하는 모든 IP 주소는 예외 프로세스를 통해 라우팅됩니다.</span><span class="sxs-lookup"><span data-stu-id="352be-p102">The public certificates are issued by Microsoft IT SSL using SSLAdmin, an internal Microsoft tool to protect confidentiality of transmitted information. All certificates issued by Microsoft IT have a minimum of 2048 bits in length, and [Webtrust](http://www.webtrust.org/homepage-documents/item70372.pdf) compliance requires SSLAdmin to make sure that certificates are issued only to public IP addresses owned by Microsoft. Any IP addresses that fail to meet this criterion are routed through an exception process.</span></span>

<span data-ttu-id="352be-p103">사용 중인 TLS 버전, 즉 정방향 보안 (FS)을 사용할 수 있는지 여부와 같은 모든 구현 세부 정보를 공개적으로 사용할 수 있습니다. 이러한 세부 정보를 확인 하는 한 가지 방법은 www.ssllabs.com (Qualys SSL lab)와 같은 타사 웹 사이트를 사용 하는 것입니다. 다음 서비스에 대 한 정보를 표시 하는 Qualys의 자동화 된 테스트 페이지에 대 한 링크는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="352be-p103">All implementation details such as the version of TLS being used, whether Forward Secrecy (FS) is enabled, the order of cipher suites, etc., are available publicly. One way to see these details is to use a third-party website, such as Qualys SSL Labs (www.ssllabs.com). Below are the links to automated test pages from Qualys that display information for the following services:</span></span>
- [<span data-ttu-id="352be-117">Office 365 포털</span><span class="sxs-lookup"><span data-stu-id="352be-117">Office 365 Portal</span></span>](https://www.ssllabs.com/ssltest/analyze.html?d=portal.office.com&hideResults=on)
- [<span data-ttu-id="352be-118">Exchange Online</span><span class="sxs-lookup"><span data-stu-id="352be-118">Exchange Online</span></span>](https://www.ssllabs.com/ssltest/analyze.html?d=outlook.office365.com&hideResults=on)
- [<span data-ttu-id="352be-119">SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="352be-119">SharePoint Online</span></span>](https://www.ssllabs.com/ssltest/analyze.html?d=microsoft-my.sharepoint.com&hideResults=on)
- [<span data-ttu-id="352be-120">비즈니스용 Skype (SIP)</span><span class="sxs-lookup"><span data-stu-id="352be-120">Skype for Business (SIP)</span></span>](https://www.ssllabs.com/ssltest/analyze.html?d=sipdir.online.lync.com)
- [<span data-ttu-id="352be-121">비즈니스용 Skype (웹)</span><span class="sxs-lookup"><span data-stu-id="352be-121">Skype for Business (Web)</span></span>](https://www.ssllabs.com/ssltest/analyze.html?d=webdir.online.lync.com&hideResults=on)
- [<span data-ttu-id="352be-122">Exchange Online Protection</span><span class="sxs-lookup"><span data-stu-id="352be-122">Exchange Online Protection</span></span>](https://ssl-tools.net/mailservers/microsoft-com.mail.protection.outlook.com)
- [<span data-ttu-id="352be-123">Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="352be-123">Microsoft Teams</span></span>](https://www.ssllabs.com/ssltest/analyze.html?d=teams.microsoft.com&latest)

<span data-ttu-id="352be-124">Exchange Online Protection의 경우 url은 테 넌 트 이름에 따라 다릅니다. 그러나 모든 고객은 **microsoft-com.mail.protection.outlook.com**를 사용 하 여 Office 365을 테스트할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="352be-124">For Exchange Online Protection, URLs vary by tenant names; however, all customers can test Office 365 using **microsoft-com.mail.protection.outlook.com**.</span></span>
