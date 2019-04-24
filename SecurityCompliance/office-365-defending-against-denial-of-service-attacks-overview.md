---
title: Office 365에서 서비스 거부 공격 으로부터 방어
ms.author: robmazz
author: robmazz
manager: laurawi
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.collection:
- Strat_O365_IP
- M365-security-compliance
description: DoS (서비스 거부) 공격의 개요
ms.openlocfilehash: a7e67fcc87867190f345c5dad14e38a473420eab
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32262820"
---
# <a name="defending-against-denial-of-service-attacks-in-office-365"></a><span data-ttu-id="ed9b4-103">Office 365에서 서비스 거부 공격 으로부터 방어</span><span class="sxs-lookup"><span data-stu-id="ed9b4-103">Defending Against Denial-of-Service Attacks in Office 365</span></span>

## <a name="introduction"></a><span data-ttu-id="ed9b4-104">소개</span><span class="sxs-lookup"><span data-stu-id="ed9b4-104">Introduction</span></span>
<span data-ttu-id="ed9b4-105">microsoft는 글로벌 클라우드에서 호스트 되는 microsoft Azure, microsoft Bing, microsoft Office 365, microsoft Dynamics 365, microsoft OneDrive, Skype 및 Xbox Live를 비롯 하 여 200 개 이상의 클라우드 서비스에 대 한 신뢰할 수 있는 인프라를 제공 합니다. 100 데이터 센터 보다 많은 인프라</span><span class="sxs-lookup"><span data-stu-id="ed9b4-105">Microsoft delivers a trustworthy infrastructure for more than 200 cloud services, including Microsoft Azure, Microsoft Bing, Microsoft Office 365, Microsoft Dynamics 365, Microsoft OneDrive, Skype, and Xbox Live that are hosted in our global cloud infrastructure of more than 100 datacenters.</span></span>

<span data-ttu-id="ed9b4-106">인터넷 현재 상태와 클라우드 서비스를 제공 하는 다양 한 인터넷 속성을 가진 전역 조직으로, Microsoft는 해커 및 기타 악의적인 개인이 사용할 수 있는 광범위 한 일반 목표입니다.</span><span class="sxs-lookup"><span data-stu-id="ed9b4-106">As a global organization with a significant Internet presence and many prominent Internet properties that provide cloud services, Microsoft is a large, common target for hackers and other malicious individuals.</span></span> <span data-ttu-id="ed9b4-107">네트워크--클라이언트와 Microsoft 클라우드 간의 통신 계층은 악의적인 공격의 가장 큰 목표 중 하나입니다.</span><span class="sxs-lookup"><span data-stu-id="ed9b4-107">The network--the communication layer between clients and the Microsoft Cloud--is one of the biggest targets of malicious attacks.</span></span> <span data-ttu-id="ed9b4-108">실제로 Microsoft는 지난 몇 년 동안 몇 가지 네트워크 기반에서는 사이버 공격과의 형태로 지속적이 고 영구적으로 사용 되 고 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ed9b4-108">In fact, for many years, Microsoft has been continuously and persistently under some form of network-based cyberattack.</span></span> <span data-ttu-id="ed9b4-109">거의 대부분의 Microsoft 인터넷 속성 중 하나 이상에 게 약간의 공격이 발생 합니다.</span><span class="sxs-lookup"><span data-stu-id="ed9b4-109">At almost all times, at least one of Microsoft's Internet properties is experiencing some form of attack.</span></span> <span data-ttu-id="ed9b4-110">이러한 공격 으로부터 방어할 수 있는 안정적이 고 지속적인 완화 시스템이 없는 경우 Microsoft의 클라우드 서비스는 오프 라인 상태 이며 고객에 게는 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="ed9b4-110">Without reliable and persistent mitigation systems that can defend against these attacks, Microsoft's cloud services would be offline and unavailable to customers.</span></span>

<span data-ttu-id="ed9b4-111">Microsoft는 심층 방어 보안 원칙을 사용 하 여 클라우드 서비스 및 네트워크를 보호 합니다.</span><span class="sxs-lookup"><span data-stu-id="ed9b4-111">Microsoft uses defense-in-depth security principles to protect its cloud services and networks.</span></span> 

## <a name="definition-and-symptoms-of-denial-of-service-attacks"></a><span data-ttu-id="ed9b4-112">서비스 거부 공격의 정의 및 증상</span><span class="sxs-lookup"><span data-stu-id="ed9b4-112">Definition and Symptoms of Denial-of-Service Attacks</span></span>
<span data-ttu-id="ed9b4-113">네트워크 서비스를 공격 하는 한 가지 방법은 서비스의 호스트에 대해 많은 요청을 만들어 합법적인 사용자에 대 한 서비스를 거부 하기 위해 네트워크 및 서버에 과부하가 발생 하도록 하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="ed9b4-113">One way to attack network services is to create many requests against a service's hosts to overwhelm the network and servers to deny service to legitimate users.</span></span> <span data-ttu-id="ed9b4-114">이를 DoS (서비스 거부) 공격 이라고 합니다.</span><span class="sxs-lookup"><span data-stu-id="ed9b4-114">This is referred to as a denial-of-service (DoS) attack.</span></span> <span data-ttu-id="ed9b4-115">여러 행위자, 끝점 및/또는 벡터로 공격을 수행 하는 경우 분산 서비스 거부 (DDoS) 공격 이라고 합니다.</span><span class="sxs-lookup"><span data-stu-id="ed9b4-115">When the attack is performed by multiple actors, endpoints, and/or vectors, it is referred to as a distributed denial-of-service (DDoS) attack.</span></span> <span data-ttu-id="ed9b4-116">수단, 동기 및 대상이 다를 수 있지만 일반적으로 DoS 및 DDoS 공격은 일시적으로 또는 무기한으로 인터넷 사이트 또는 서비스를 정상적으로 작동 하거나 무한정 작동할 수 없도록 하는 담당자의 노력으로 구성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ed9b4-116">Although the means, motives, and targets vary, DoS and DDoS attacks generally consist of the efforts of a person or persons to prevent an Internet site or service from functioning correctly or at all, either temporarily or indefinitely.</span></span>

<span data-ttu-id="ed9b4-117">[미국 컴퓨터 응급 준비 팀](https://www.us-cert.gov/) (미국-CERT)은 DoS 공격이 포함 될 증상을 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="ed9b4-117">The [United States Computer Emergency Readiness Team](https://www.us-cert.gov/) (US-CERT) defines symptoms of DoS attacks to include:</span></span>
- <span data-ttu-id="ed9b4-118">네트워크 성능이 비정상적으로 느립니다 (파일을 열거나 인터넷 사이트에 액세스 하는 경우).</span><span class="sxs-lookup"><span data-stu-id="ed9b4-118">Unusually slow network performance (when opening files or accessing Internet sites)</span></span>
- <span data-ttu-id="ed9b4-119">웹 사이트를 사용할 비 사용할 때</span><span class="sxs-lookup"><span data-stu-id="ed9b4-119">Unavailability of a Web site</span></span>
- <span data-ttu-id="ed9b4-120">웹 사이트에 액세스할 수 없음</span><span class="sxs-lookup"><span data-stu-id="ed9b4-120">Inability to access a Web site</span></span>
- <span data-ttu-id="ed9b4-121">받은 스팸의 급격 한 증가</span><span class="sxs-lookup"><span data-stu-id="ed9b4-121">Dramatic increase in received spam</span></span>
- <span data-ttu-id="ed9b4-122">무선 또는 유선 인터넷 연결 끊기</span><span class="sxs-lookup"><span data-stu-id="ed9b4-122">Disconnection of a wireless or wired Internet connection</span></span>
- <span data-ttu-id="ed9b4-123">웹 또는 인터넷 서비스에 대 한 장기간 액세스 권한 손실</span><span class="sxs-lookup"><span data-stu-id="ed9b4-123">Long-term loss of access to the Web or any Internet services</span></span>

## <a name="related-topics"></a><span data-ttu-id="ed9b4-124">관련 항목</span><span class="sxs-lookup"><span data-stu-id="ed9b4-124">Related Topics</span></span>
- [<span data-ttu-id="ed9b4-125">서비스 거부 공격에 대한 보안 핵심 원칙</span><span class="sxs-lookup"><span data-stu-id="ed9b4-125">Core Principles of Defense Against Denial-of-Service Attacks</span></span>](office-365-core-principles-of-defense-against-dos-attacks.md)
- [<span data-ttu-id="ed9b4-126">Microsoft의 서비스 거부 방어 전략</span><span class="sxs-lookup"><span data-stu-id="ed9b4-126">Microsoft's Denial-of-Service Defense Strategy</span></span>](office-365-microsoft-dos-defense-strategy.md)
- [<span data-ttu-id="ed9b4-127">서비스 거부 공격에 대해 Microsoft 클라우드 서비스 방어</span><span class="sxs-lookup"><span data-stu-id="ed9b4-127">Defending Microsoft Cloud Services Against Denial-of-Service Attacks</span></span>](office-365-defending-cloud-services-against-dos-attacks.md)
