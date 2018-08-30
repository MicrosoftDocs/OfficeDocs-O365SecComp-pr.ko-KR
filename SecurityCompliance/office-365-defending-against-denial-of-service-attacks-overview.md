---
title: Office 365에서에서 서비스 거부 공격을 방어
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
description: 서비스 거부 (DoS) 공격을 간략하게 설명 합니다.
ms.openlocfilehash: b5a51ae332b32142d9ab993a29763b2160c3ce97
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22532891"
---
# <a name="defending-against-denial-of-service-attacks-in-office-365"></a><span data-ttu-id="c6eeb-103">Office 365에서에서 서비스 거부 공격을 방어</span><span class="sxs-lookup"><span data-stu-id="c6eeb-103">Defending Against Denial-of-Service Attacks in Office 365</span></span>

## <a name="introduction"></a><span data-ttu-id="c6eeb-104">소개</span><span class="sxs-lookup"><span data-stu-id="c6eeb-104">Introduction</span></span>
<span data-ttu-id="c6eeb-105">Microsoft는 200 개 이상의 클라우드 서비스에 대 한 Microsoft Azure, Microsoft Bing, Microsoft Office 365, Microsoft Dynamics 365, Microsoft OneDrive, Skype, 및 Xbox Live를 포함 하 여이 글로벌 클라우드에서 호스팅되는 신뢰할 수 있는 인프라를 제공 100 개가 넘는 데이터 센터의 인프라를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6eeb-105">Microsoft delivers a trustworthy infrastructure for more than 200 cloud services, including Microsoft Azure, Microsoft Bing, Microsoft Office 365, Microsoft Dynamics 365, Microsoft OneDrive, Skype, and Xbox Live that are hosted in our global cloud infrastructure of more than 100 datacenters.</span></span>

<span data-ttu-id="c6eeb-p101">중요 한 인터넷 현재 상태 및 클라우드 서비스를 제공 하는 많은 많이 사용 되 인터넷 속성을 글로벌 조직으로 Microsoft에는 해커 및 기타 악성 개인에 대 한 대규모, 일반적인 대상이 됩니다. 네트워크--클라이언트와 Microsoft 클라우드-간의 통신 계층의 악의적인 공격 가장 큰 목표 중 하나입니다. 실제로 지난 수년간, Microsoft 되었고 지속적으로 영구적으로 네트워크 기반 cyberattack 형태의 아래 있습니다. 거의 항상 공격의 일종을 발생 하는 Microsoft의 인터넷 속성 중 하나 이상이 합니다. 이러한 공격 으로부터 방어 수 있는 안정적이 고 영구 완화 시스템을 하지 않고 Microsoft 클라우드 서비스는 오프 라인 및 고객에 게 사용할 수 없는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="c6eeb-p101">As a global organization with a significant Internet presence and many prominent Internet properties that provide cloud services, Microsoft is a large, common target for hackers and other malicious individuals. The network--the communication layer between clients and the Microsoft Cloud--is one of the biggest targets of malicious attacks. In fact, for many years, Microsoft has been continuously and persistently under some form of network-based cyberattack. At almost all times, at least one of Microsoft's Internet properties is experiencing some form of attack. Without reliable and persistent mitigation systems that can defend against these attacks, Microsoft's cloud services would be offline and unavailable to customers.</span></span>

<span data-ttu-id="c6eeb-111">Microsoft의 클라우드 서비스 및 네트워크를 보호 하기 위해 심층 방어 보안 원칙을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6eeb-111">Microsoft uses defense-in-depth security principles to protect its cloud services and networks.</span></span> 

## <a name="definition-and-symptoms-of-denial-of-service-attacks"></a><span data-ttu-id="c6eeb-112">정 및 서비스 거부 공격 증상이 나타날 수 있습니다</span><span class="sxs-lookup"><span data-stu-id="c6eeb-112">Definition and Symptoms of Denial-of-Service Attacks</span></span>
<span data-ttu-id="c6eeb-p102">네트워크 서비스 공격에 한 가지 방법은 네트워크 및 서버 합법적인 사용자에 게 서비스를 거부 하려면 발생 하는 서비스의 호스트에 대해 많은 요청을 만드는 것입니다. 이것은 서비스 거부 (DoS) 공격을 이라고 합니다. 공격 작업자, 끝점 및/또는 벡터 여러 하 여를 수행 하는 경우에 분산된 서비스 거부 (DDoS) 공격으로 참조 됩니다. 의미, 동기 및 목표에 따라, 다르기는 하지만 DoS 및 DDoS 공격 명 이상의 사용자의 활동을 정상적으로 작동 중에서 또는 모두를 일시적으로 또는 무기한에 인터넷 사이트 또는 서비스를 방지 하기 위해 일반적으로 구성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c6eeb-p102">One way to attack network services is to create many requests against a service's hosts to overwhelm the network and servers to deny service to legitimate users. This is referred to as a denial-of-service (DoS) attack. When the attack is performed by multiple actors, endpoints, and/or vectors, it is referred to as a distributed denial-of-service (DDoS) attack. Although the means, motives, and targets vary, DoS and DDoS attacks generally consist of the efforts of a person or persons to prevent an Internet site or service from functioning correctly or at all, either temporarily or indefinitely.</span></span>

<span data-ttu-id="c6eeb-117">[미국, 대한민국 컴퓨터 응급 준비 팀](https://www.us-cert.gov/) (미국-CERT) 포함 하는 DoS 공격 증상이 나타날 수 있습니다를 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6eeb-117">The [United States Computer Emergency Readiness Team](https://www.us-cert.gov/) (US-CERT) defines symptoms of DoS attacks to include:</span></span>
- <span data-ttu-id="c6eeb-118">네트워크 성능을 일반적으로 느린 (때 파일을 열 또는 인터넷 사이트에 액세스)</span><span class="sxs-lookup"><span data-stu-id="c6eeb-118">Unusually slow network performance (when opening files or accessing Internet sites)</span></span>
- <span data-ttu-id="c6eeb-119">웹사이트의 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="c6eeb-119">Unavailability of a Web site</span></span>
- <span data-ttu-id="c6eeb-120">웹사이트에 액세스할 수 없음</span><span class="sxs-lookup"><span data-stu-id="c6eeb-120">Inability to access a Web site</span></span>
- <span data-ttu-id="c6eeb-121">수신된 스팸에 급격 하 게 증가</span><span class="sxs-lookup"><span data-stu-id="c6eeb-121">Dramatic increase in received spam</span></span>
- <span data-ttu-id="c6eeb-122">유선 또는 무선 인터넷 연결의 연결 해제</span><span class="sxs-lookup"><span data-stu-id="c6eeb-122">Disconnection of a wireless or wired Internet connection</span></span>
- <span data-ttu-id="c6eeb-123">웹 또는 인터넷 서비스에 대 한 액세스의 장기 손실</span><span class="sxs-lookup"><span data-stu-id="c6eeb-123">Long-term loss of access to the Web or any Internet services</span></span>

## <a name="related-topics"></a><span data-ttu-id="c6eeb-124">관련 항목</span><span class="sxs-lookup"><span data-stu-id="c6eeb-124">Related Topics</span></span>
- [<span data-ttu-id="c6eeb-125">서비스 거부 공격에 대한 보안 핵심 원칙</span><span class="sxs-lookup"><span data-stu-id="c6eeb-125">Core Principles of Defense Against Denial-of-Service Attacks</span></span>](office-365-core-principles-of-defense-against-dos-attacks.md)
- [<span data-ttu-id="c6eeb-126">Microsoft의 서비스 거부 방어 전략</span><span class="sxs-lookup"><span data-stu-id="c6eeb-126">Microsoft's Denial-of-Service Defense Strategy</span></span>](office-365-microsoft-dos-defense-strategy.md)
- [<span data-ttu-id="c6eeb-127">Microsoft 클라우드 서비스 서비스 거부 공격을 방어</span><span class="sxs-lookup"><span data-stu-id="c6eeb-127">Defending Microsoft Cloud Services Against Denial-of-Service Attacks</span></span>](office-365-defending-cloud-services-against-dos-attacks.md)
