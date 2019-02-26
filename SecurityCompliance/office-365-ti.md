---
title: Office 365 위협 인텔리전스
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 02/08/2019
ms.audience: Admin
ms.topic: overview
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 32405da5-bee1-4a4b-82e5-8399df94c512
ms.collection:
- M365-security-compliance
description: Advanced threat Protection의 위협 인텔리전스 기능을 통해 조직에 대 한 위협을 조사 하 고, 맬웨어, 피싱 및 기타 공격에 대처 하 고, Office 365에서 사용자를 대신 하 여 검색 한 기타 공격과 위협 지표를 검색할 수 있는 방법을 알아봅니다.
ms.openlocfilehash: 81a986c4b47d740313356b22fd1c23bd5e472a24
ms.sourcegitcommit: 1c73c2f83703af0a30a5b0633db00d8e0e6b39b5
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/25/2019
ms.locfileid: "30241931"
---
# <a name="office-365-threat-intelligence"></a><span data-ttu-id="25559-103">Office 365 위협 인텔리전스</span><span class="sxs-lookup"><span data-stu-id="25559-103">Office 365 Threat Intelligence</span></span>

<span data-ttu-id="25559-104">Advanced threat Protection의 위협 인텔리전스 기능에서는 다음과 같은 방법으로 보안 분석가와 관리자가 조직의 Office 365 사용자를 보호 하는 데 도움을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="25559-104">Threat intelligence capabilities in Office 365 Advanced Threat Protection help security analysts and administrators protect their organization's Office 365 users by:</span></span>
  
1. <span data-ttu-id="25559-105">공격을 쉽게 식별 하 고 모니터링 하 고 이해할 수 있도록 설정</span><span class="sxs-lookup"><span data-stu-id="25559-105">Making it easy to identify, monitor and understand attacks</span></span>
    
2. <span data-ttu-id="25559-106">Exchange online 및 SharePoint online의 위협에 대 한 신속한 해결 지원</span><span class="sxs-lookup"><span data-stu-id="25559-106">Helping to quickly address threats in Exchange Online and SharePoint Online</span></span>
    
3. <span data-ttu-id="25559-107">조직에서 공격을 방지 하는 데 도움이 되는 정보를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="25559-107">Providing insights and knowledge to help prevent attacks against their organization</span></span>
    
> [!IMPORTANT]
> <span data-ttu-id="25559-p101">위협 인텔리전스는 이제 [microsoft 365 enterprise](https://www.microsoft.com/microsoft-365/enterprise/home), [microsoft 365 Business](https://www.microsoft.com/microsoft-365/business), office 365 Enterprise E5, office 365과 같은 특정 구독에 포함 된 **Office 365 Advanced Threat Protection 계획 2의 일부**입니다. 교육 A5 등 조직에서 Office 365 ATP를 포함 하지 않는 구독을 사용 하는 경우 ATP를 추가 기능으로 구입할 수 있습니다. 자세한 내용은 [office 365 advanced threat protection 요금제 및 가격](https://products.office.com/exchange/advance-threat-protection) 및 [office 365 advanced threat protection 서비스 설명을](https://docs.microsoft.com/en-us/office365/servicedescriptions/office-365-advanced-threat-protection-service-description#whats-new-in-office-365-advanced-threat-protection-atp)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="25559-p101">**Threat Intelligence is now part of in Office 365 Advanced Threat Protection Plan 2**, which is included in in certain subscriptions, such as [Microsoft 365 Enterprise](https://www.microsoft.com/microsoft-365/enterprise/home), [Microsoft 365 Business](https://www.microsoft.com/microsoft-365/business), Office 365 Enterprise E5, Office 365 Education A5, etc. If your organization has a subscription that does not include Office 365 ATP, you can potentially purchase ATP as an add-on. For more information, see [Office 365 Advanced Threat Protection plans and pricing](https://products.office.com/exchange/advance-threat-protection) and the [Office 365 Advanced Threat Protection Service Description](https://docs.microsoft.com/en-us/office365/servicedescriptions/office-365-advanced-threat-protection-service-description#whats-new-in-office-365-advanced-threat-protection-atp).</span></span> 
  
## <a name="whats-changing"></a><span data-ttu-id="25559-110">변경 된 기능</span><span class="sxs-lookup"><span data-stu-id="25559-110">What's changing?</span></span>

<span data-ttu-id="25559-p102">이전에는 office 365 Enterprise e 5와 같은 위험 인텔리전스가 구독에 포함 되었습니다. 여전히 위협 인텔리전스 기능이 office 365 Advanced Threat Protection 계획 2의 일부분이 긴 하지만이는 office 365 Enterprise E5에 포함 되어 있는 경우에도 해당 됩니다.</span><span class="sxs-lookup"><span data-stu-id="25559-p102">Formerly, Office 365 Threat Intelligence was included in subscriptions, such as Office 365 Enterprise E5. This is still the case, although Threat Intelligence features are now part of Office 365 Advanced Threat Protection Plan 2 (and this is included in Office 365 Enterprise E5).</span></span> 

<span data-ttu-id="25559-p103">또한 office 365 위협 인텔리전스는 이전에 office 365 for business 고객을 위한 추가 기능으로 구매할 수 있었습니다. 이제 위협 인텔리전스는 Office 365 Advanced Threat Protection 계획 2에 포함 되어 있습니다. 자세한 내용은 [Office 365 Advanced Threat Protection 요금제 및 가격 책정](https://products.office.com/exchange/advance-threat-protection)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="25559-p103">In addition, Office 365 Threat Intelligence was formerly available for purchase as an add-on for Office 365 for business customers. Now, Threat Intelligence is included in Office 365 Advanced Threat Protection Plan 2. To learn more, see [Office 365 Advanced Threat Protection plans and pricing](https://products.office.com/exchange/advance-threat-protection).</span></span>

<span data-ttu-id="25559-116">이 모든 것을 의미 하는 것은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="25559-116">Here's what all this means:</span></span>

- <span data-ttu-id="25559-117">**조직에 이미 Office 365 Enterprise E5가 있는 경우**Advanced threat Protection 계획 2가 이미 있고 여기에는 위협 인텔리전스 기능도 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="25559-117">**If your organization already has Office 365 Enterprise E5**, then you already have Advanced Threat Protection Plan 2, and this includes Threat Intelligence capabilities.</span></span>

- <span data-ttu-id="25559-p104">**조직에서 이전에 office 365 위협 인텔리전스 (office 365 Advanced threat Protection 제외)** 가 다른 office 365 구독에 대 한 추가 기능으로 사용 되는 경우 office 365 Advanced threat protection 계획 2가 됩니다. 여기에는 Advanced threat Protection 및 위협 인텔리전스 기능이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="25559-p104">**If your organization previously had Office 365 Threat Intelligence (but not Office 365 Advanced Threat Protection) as an add-on** to another Office 365 subscription, then you will have Office 365 Advanced Threat Protection Plan 2. This includes Advanced Threat Protection and Threat Intelligence capabilities.</span></span> 

- <span data-ttu-id="25559-p105">**조직에서 이전에 office 365 advanced threat protection (office 365 위협 인텔리전스)** 을 다른 office 365 구독에 추가 기능으로 사용 하는 경우 office 365 Advanced threat protection 계획 1이 됩니다. 여기에는 Advanced threat Protection (위협 인텔리전스 기능 제외)이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="25559-p105">**If your organization previously had Office 365 Advanced Threat Protection (but not Office 365 Threat Intelligence) as an add-on** to another Office 365 subscription, then you will have Office 365 Advanced Threat Protection Plan 1. This includes Advanced Threat Protection (but not Threat Intelligence capabilities).</span></span>

<span data-ttu-id="25559-122">자세한 내용은 [office 365 advanced threat protection 요금제 및 가격](https://products.office.com/exchange/advance-threat-protection) 및 [office 365 advanced threat protection 서비스 설명](https://docs.microsoft.com/en-us/office365/servicedescriptions/office-365-advanced-threat-protection-service-description#whats-new-in-office-365-advanced-threat-protection-atp) 를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="25559-122">For more information, see [Office 365 Advanced Threat Protection plans and pricing](https://products.office.com/exchange/advance-threat-protection) and the [Office 365 Advanced Threat Protection Service Description](https://docs.microsoft.com/en-us/office365/servicedescriptions/office-365-advanced-threat-protection-service-description#whats-new-in-office-365-advanced-threat-protection-atp)</span></span>

## <a name="get-started-with-threat-intelligence-capabilities"></a><span data-ttu-id="25559-123">위협 인텔리전스 기능 시작 하기</span><span class="sxs-lookup"><span data-stu-id="25559-123">Get started with threat intelligence capabilities</span></span>

<span data-ttu-id="25559-124">다음 리소스를 사용 하 여 위협 인텔리전스에 대해 자세히 알아보고,이를 사용 하 여 조직의 사용자를 안전 하 게 유지 하는 방법을 알아보세요.</span><span class="sxs-lookup"><span data-stu-id="25559-124">Use the following resources to learn more about threat intelligence, and how you can use it to keep people in your organization safer.</span></span>
  
- <span data-ttu-id="25559-125">[위협 인텔리전스 시작 하기](get-started-with-ti.md) (필수 역할에 대 한 정보가 포함 됩니다.)</span><span class="sxs-lookup"><span data-stu-id="25559-125">[Get started with Threat Intelligence](get-started-with-ti.md) (this includes information about required roles)</span></span> 
    
- [<span data-ttu-id="25559-126">위협 추적기에 대해 알아보기-신규 및 중요</span><span class="sxs-lookup"><span data-stu-id="25559-126">Learn about Threat Trackers - New and Noteworthy</span></span>](threat-trackers.md)
    
- [<span data-ttu-id="25559-127">배달 된 악성 전자 메일 찾기 및 조사</span><span class="sxs-lookup"><span data-stu-id="25559-127">Find and investigate malicious email that was delivered</span></span>](investigate-malicious-email-that-was-delivered.md)
    
- [<span data-ttu-id="25559-128">공격 시뮬레이터 사용</span><span class="sxs-lookup"><span data-stu-id="25559-128">Use Attack Simulator</span></span>](attack-simulator.md)
    
- [<span data-ttu-id="25559-129">위협 인텔리전스와 Windows Defender Advanced Threat Protection 통합</span><span class="sxs-lookup"><span data-stu-id="25559-129">Integrate Threat Intelligence with Windows Defender Advanced Threat Protection</span></span>](integrate-office-365-ti-with-wdatp.md)
    
## <a name="related-topics"></a><span data-ttu-id="25559-130">관련 항목</span><span class="sxs-lookup"><span data-stu-id="25559-130">Related topics</span></span>

[<span data-ttu-id="25559-131">Office 365에서 위협으로부터 보호</span><span class="sxs-lookup"><span data-stu-id="25559-131">Protect against threats in Office 365</span></span>](protect-against-threats.md)
  
[<span data-ttu-id="25559-132">Office 365 Advanced Threat Protection 방지</span><span class="sxs-lookup"><span data-stu-id="25559-132">Office 365 Advanced Threat Protection</span></span>](office-365-atp.md)
  
[<span data-ttu-id="25559-133">Office 365 보안 &amp; 및 준수 센터의 사용 권한</span><span class="sxs-lookup"><span data-stu-id="25559-133">Permissions in the Office 365 Security &amp; Compliance Center</span></span>](permissions-in-the-security-and-compliance-center.md)
  

