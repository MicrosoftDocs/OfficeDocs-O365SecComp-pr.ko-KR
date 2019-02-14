---
title: Office 365 위협 인텔리전스
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 02/08/2019
ms.audience: Admin
ms.topic: overview
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 32405da5-bee1-4a4b-82e5-8399df94c512
ms.collection: M365-security-compliance
description: 고급 위협 보호의 위협 인텔리전스 기능 하는 방법 조직에 대 한 위협을 조사, 맬웨어, 피싱와 파트너가 대신 Office 365에서 발견 하는 다른 공격에 응답 하 고 위협 지표에 대 한 검색에 대해 알아봅니다.
ms.openlocfilehash: 632a2387e7cb5a30745459383e670d08c9b84aff
ms.sourcegitcommit: efccf5b4f22d34a9674bc55ebf3d88bc8bda2972
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/14/2019
ms.locfileid: "29995099"
---
# <a name="office-365-threat-intelligence"></a><span data-ttu-id="fa99e-103">Office 365 위협 인텔리전스</span><span class="sxs-lookup"><span data-stu-id="fa99e-103">Office 365 Threat Intelligence</span></span>

<span data-ttu-id="fa99e-104">Office 365 고급 위협 보호의 위협 인텔리전스 기능 보안 분석가 도움말과 관리자 하 여 조직의 Office 365 사용자를 보호 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa99e-104">Threat intelligence capabilities in Office 365 Advanced Threat Protection help security analysts and administrators protect their organization's Office 365 users by:</span></span>
  
1. <span data-ttu-id="fa99e-105">쉽게 식별, 모니터링 및 공격을 이해</span><span class="sxs-lookup"><span data-stu-id="fa99e-105">Making it easy to identify, monitor and understand attacks</span></span>
    
2. <span data-ttu-id="fa99e-106">신속 하 게 주소 위협에 Exchange Online 및 SharePoint Online 도움말</span><span class="sxs-lookup"><span data-stu-id="fa99e-106">Helping to quickly address threats in Exchange Online and SharePoint Online</span></span>
    
3. <span data-ttu-id="fa99e-107">인 사이트 및 해당 조직에 대 한 공격을 방지 하려면 기술 제공</span><span class="sxs-lookup"><span data-stu-id="fa99e-107">Providing insights and knowledge to help prevent attacks against their organization</span></span>
    
> [!IMPORTANT]
> <span data-ttu-id="fa99e-p101">**위협 인텔리전스 지금의 일부인 Office 365 고급 위협 보호 계획 2에**,이에 포함 된 [Microsoft 365 Enterprise](https://www.microsoft.com/microsoft-365/enterprise/home), [Microsoft 365 비즈니스](https://www.microsoft.com/microsoft-365/business), Office 365 Enterprise E5, 예: 특정 구독에서 Office 365 교육 A5 등입니다. 조직에 Office 365 ATP 포함 되지 않은 구독을 하는 경우에 추가 기능으로 ATP을 잠재적으로 구입할 수 있습니다. 자세한 내용은 [Office 365 고급 위협 보호 계획 및 가격](https://products.office.com/exchange/advance-threat-protection) 및 [Office 365 고급 위협 Protection Service Description](https://docs.microsoft.com/en-us/office365/servicedescriptions/office-365-advanced-threat-protection-service-description#whats-new-in-office-365-advanced-threat-protection-atp)을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="fa99e-p101">**Threat Intelligence is now part of in Office 365 Advanced Threat Protection Plan 2**, which is included in in certain subscriptions, such as [Microsoft 365 Enterprise](https://www.microsoft.com/microsoft-365/enterprise/home), [Microsoft 365 Business](https://www.microsoft.com/microsoft-365/business), Office 365 Enterprise E5, Office 365 Education A5, etc. If your organization has a subscription that does not include Office 365 ATP, you can potentially purchase ATP as an add-on. For more information, see [Office 365 Advanced Threat Protection plans and pricing](https://products.office.com/exchange/advance-threat-protection) and the [Office 365 Advanced Threat Protection Service Description](https://docs.microsoft.com/en-us/office365/servicedescriptions/office-365-advanced-threat-protection-service-description#whats-new-in-office-365-advanced-threat-protection-atp).</span></span> 
  
## <a name="whats-changing"></a><span data-ttu-id="fa99e-110">변경 된 무엇입니까?</span><span class="sxs-lookup"><span data-stu-id="fa99e-110">What's changing?</span></span>

<span data-ttu-id="fa99e-p102">이전 버전에서는 Office 365 위협 인텔리전스 Office 365 Enterprise e 5와 같은 구독에 포함 되었습니다. 이것은 여전히 경우에는 있지만 위협 인텔리전스 기능은 이제 Office 365 고급 위협 보호 계획 2의 일부 (및 Office 365 Enterprise e 5에 포함 된이).</span><span class="sxs-lookup"><span data-stu-id="fa99e-p102">Formerly, Office 365 Threat Intelligence was included in subscriptions, such as Office 365 Enterprise E5. This is still the case, although Threat Intelligence features are now part of Office 365 Advanced Threat Protection Plan 2 (and this is included in Office 365 Enterprise E5).</span></span> 

<span data-ttu-id="fa99e-p103">또한 Office 365 위협 인텔리전스 된 비즈니스 고객을 위한 Office 365에 대 한 추가 기능으로 구입할 수 있는 이전 합니다. 이제, 위협 인텔리전스 Office 365 고급 위협 보호 계획 2에 포함 됩니다. 자세한 내용은 [Office 365 고급 위협 보호 계획 및 가격](https://products.office.com/exchange/advance-threat-protection)을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="fa99e-p103">In addition, Office 365 Threat Intelligence was formerly available for purchase as an add-on for Office 365 for business customers. Now, Threat Intelligence is included in Office 365 Advanced Threat Protection Plan 2. To learn more, see [Office 365 Advanced Threat Protection plans and pricing](https://products.office.com/exchange/advance-threat-protection).</span></span>

<span data-ttu-id="fa99e-116">이 모든 값의 의미 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="fa99e-116">Here's what all this means:</span></span>

- <span data-ttu-id="fa99e-117">고급 위협 보호 계획 2, 이미 **조직에 Office 365 Enterprise e 5에 있는 경우**, 다음 및 위협 인텔리전스 기능이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="fa99e-117">**If your organization already has Office 365 Enterprise E5**, then you already have Advanced Threat Protection Plan 2, and this includes Threat Intelligence capabilities.</span></span>

- <span data-ttu-id="fa99e-p104">**조직에는 이전에 Office 365 위협 인텔리전스 (하지만 하지 Office 365 고급 위협 보호) 추가 기능으로 없던 하는 경우** 다른 Office 365 구독 후에 Office 365 고급 위협 보호 계획 2 해야 합니다. 이 위협 보호 고급 및 위협 인텔리전스 기능이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="fa99e-p104">**If your organization previously had Office 365 Threat Intelligence (but not Office 365 Advanced Threat Protection) as an add-on** to another Office 365 subscription, then you will have Office 365 Advanced Threat Protection Plan 2. This includes Advanced Threat Protection and Threat Intelligence capabilities.</span></span> 

- <span data-ttu-id="fa99e-p105">**조직에는 이전에 Office 365 고급 위협 보호 (하지만 Office 365 위협 인텔리전스 하지) 추가 기능으로 없던 하는 경우** 다른 Office 365 구독 후에 Office 365 고급 위협 보호 계획 1 해야 합니다. 고급 위협 보호 있지만 (예: 하지 위협 인텔리전스 기능)이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="fa99e-p105">**If your organization previously had Office 365 Advanced Threat Protection (but not Office 365 Threat Intelligence) as an add-on** to another Office 365 subscription, then you will have Office 365 Advanced Threat Protection Plan 1. This includes Advanced Threat Protection (but not Threat Intelligence capabilities).</span></span>

<span data-ttu-id="fa99e-122">자세한 내용은 [Office 365 고급 위협 보호 계획 및 가격](https://products.office.com/exchange/advance-threat-protection) 및 [Office 365 고급 위협 Protection 서비스 설명](https://docs.microsoft.com/en-us/office365/servicedescriptions/office-365-advanced-threat-protection-service-description#whats-new-in-office-365-advanced-threat-protection-atp) 를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="fa99e-122">For more information, see [Office 365 Advanced Threat Protection plans and pricing](https://products.office.com/exchange/advance-threat-protection) and the [Office 365 Advanced Threat Protection Service Description](https://docs.microsoft.com/en-us/office365/servicedescriptions/office-365-advanced-threat-protection-service-description#whats-new-in-office-365-advanced-threat-protection-atp)</span></span>

## <a name="get-started-with-threat-intelligence-capabilities"></a><span data-ttu-id="fa99e-123">위협 인텔리전스 기능 시작</span><span class="sxs-lookup"><span data-stu-id="fa99e-123">Get started with threat intelligence capabilities</span></span>

<span data-ttu-id="fa99e-124">위협 인텔리전스 및 사용 하 여 조직에서 사람들을 안전 하 게 유지 하는 방법을 하는 방법에 대 한 자세한 내용은 다음 리소스를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa99e-124">Use the following resources to learn more about threat intelligence, and how you can use it to keep people in your organization safer.</span></span>
  
- <span data-ttu-id="fa99e-125">[위협 인텔리전스 시작](get-started-with-ti.md) (필요한 역할에 대 한 정보 포함)</span><span class="sxs-lookup"><span data-stu-id="fa99e-125">[Get started with Threat Intelligence](get-started-with-ti.md) (this includes information about required roles)</span></span> 
    
- [<span data-ttu-id="fa99e-126">위협 추적기-새로 추가 되거나 주목할 만한 하는 방법에 대 한 설명</span><span class="sxs-lookup"><span data-stu-id="fa99e-126">Learn about Threat Trackers - New and Noteworthy</span></span>](threat-trackers.md)
    
- [<span data-ttu-id="fa99e-127">찾기 및 지정 된 배달 된 악의적인 전자 메일을 조사</span><span class="sxs-lookup"><span data-stu-id="fa99e-127">Find and investigate malicious email that was delivered</span></span>](investigate-malicious-email-that-was-delivered.md)
    
- [<span data-ttu-id="fa99e-128">공격 시뮬레이터를 사용 하 여</span><span class="sxs-lookup"><span data-stu-id="fa99e-128">Use Attack Simulator</span></span>](attack-simulator.md)
    
- [<span data-ttu-id="fa99e-129">Windows Defender 위협 보호 고급와 위협 인텔리전스 통합</span><span class="sxs-lookup"><span data-stu-id="fa99e-129">Integrate Threat Intelligence with Windows Defender Advanced Threat Protection</span></span>](integrate-office-365-ti-with-wdatp.md)
    
## <a name="related-topics"></a><span data-ttu-id="fa99e-130">관련 항목</span><span class="sxs-lookup"><span data-stu-id="fa99e-130">Related topics</span></span>

[<span data-ttu-id="fa99e-131">Office 365에서 위협으로부터 보호</span><span class="sxs-lookup"><span data-stu-id="fa99e-131">Protect against threats in Office 365</span></span>](protect-against-threats.md)
  
[<span data-ttu-id="fa99e-132">Office 365 Advanced Threat Protection 방지</span><span class="sxs-lookup"><span data-stu-id="fa99e-132">Office 365 Advanced Threat Protection</span></span>](office-365-atp.md)
  
[<span data-ttu-id="fa99e-133">Office 365 보안에 대 한 사용 권한을 &amp; 준수 센터</span><span class="sxs-lookup"><span data-stu-id="fa99e-133">Permissions in the Office 365 Security &amp; Compliance Center</span></span>](permissions-in-the-security-and-compliance-center.md)
  

