---
title: Office 365 위협 조사 및 응답
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 03/09/2019
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
ms.openlocfilehash: 1d076ed6ca48b8423ad92d5ea71bd87167b8519a
ms.sourcegitcommit: 74ad22a5c6c3c9d9324f0f97070909e323a4e9cf
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/11/2019
ms.locfileid: "30524002"
---
# <a name="office-365-threat-investigation-and-response"></a><span data-ttu-id="50d07-103">Office 365 위협 조사 및 응답</span><span class="sxs-lookup"><span data-stu-id="50d07-103">Office 365 Threat Investigation and Response</span></span>

<span data-ttu-id="50d07-104">위협 조사 및 Office 365 Advanced threat Protection의 응답 기능은 보안 분석가와 관리자가 조직의 Office 365 사용자를 보호 하는 데 도움이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="50d07-104">Threat investigation and response capabilities in Office 365 Advanced Threat Protection help security analysts and administrators protect their organization's Office 365 users by:</span></span>
  
1. <span data-ttu-id="50d07-105">공격을 쉽게 식별 하 고 모니터링 하 고 이해할 수 있도록 설정</span><span class="sxs-lookup"><span data-stu-id="50d07-105">Making it easy to identify, monitor and understand attacks</span></span>
    
2. <span data-ttu-id="50d07-106">Exchange online, SharePoint Online, 비즈니스 및 Microsoft 팀을 위한 하나의 드라이브에서 위협에 빠르게 문제를 해결 하는 데 도움을 줍니다.</span><span class="sxs-lookup"><span data-stu-id="50d07-106">Helping to quickly address threats in Exchange Online, SharePoint Online, One Drive for Business and Microsoft Teams</span></span>
    
3. <span data-ttu-id="50d07-107">조직에서 공격을 방지 하는 데 도움이 되는 정보를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="50d07-107">Providing insights and knowledge to help prevent attacks against their organization</span></span>

4. <span data-ttu-id="50d07-108">중요 전자 메일 기반 위협에 대 한 자동화 된 조사 및 응답</span><span class="sxs-lookup"><span data-stu-id="50d07-108">Automated investigation and response for critical email based threats</span></span>
    
> [!IMPORTANT]
> <span data-ttu-id="50d07-109">office **365 위협 조사 및 응답 (이전에 office 365 위협 인텔리전스)은 현재 office 365 Advanced threat Protection 계획 2의 일부로**, [Microsoft 365 Enterprise](https://www.microsoft.com/microsoft-365/enterprise/home)와 같은 특정 구독에 포함 되어 있습니다. [Microsoft 365 Business](https://www.microsoft.com/microsoft-365/business), office 365 Enterprise E5, Office 365 교육 A5 등입니다. 조직에서 Office 365 ATP를 포함 하지 않는 구독을 사용 하는 경우 ATP를 추가 기능으로 구입할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="50d07-109">**Office 365 THreat Investigation and Responses (previously known as Office 365 Threat Intelligence) is now part of in Office 365 Advanced Threat Protection Plan 2**, which is included in in certain subscriptions, such as [Microsoft 365 Enterprise](https://www.microsoft.com/microsoft-365/enterprise/home), [Microsoft 365 Business](https://www.microsoft.com/microsoft-365/business), Office 365 Enterprise E5, Office 365 Education A5, etc. If your organization has a subscription that does not include Office 365 ATP, you can potentially purchase ATP as an add-on.</span></span> <span data-ttu-id="50d07-110">자세한 내용은 [office 365 advanced threat protection 요금제 및 가격](https://products.office.com/exchange/advance-threat-protection) 및 [office 365 advanced threat protection 서비스 설명을](https://docs.microsoft.com/en-us/office365/servicedescriptions/office-365-advanced-threat-protection-service-description#whats-new-in-office-365-advanced-threat-protection-atp)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="50d07-110">For more information, see [Office 365 Advanced Threat Protection plans and pricing](https://products.office.com/exchange/advance-threat-protection) and the [Office 365 Advanced Threat Protection Service Description](https://docs.microsoft.com/en-us/office365/servicedescriptions/office-365-advanced-threat-protection-service-description#whats-new-in-office-365-advanced-threat-protection-atp).</span></span> 
  
## <a name="whats-changing"></a><span data-ttu-id="50d07-111">변경 된 기능</span><span class="sxs-lookup"><span data-stu-id="50d07-111">What's changing?</span></span>

<span data-ttu-id="50d07-112">이전의 office 365 위협 조사 및 응답 기능은 office 365 Enterprise E5와 같은 구독에 포함 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="50d07-112">Formerly, Office 365 Threat investigation and responses capabilities were included in subscriptions, such as Office 365 Enterprise E5.</span></span> <span data-ttu-id="50d07-113">여전히 이러한 기능을 사용할 수 있으며, 이제 이러한 기능은 office 365 Advanced Threat Protection 계획 2에 포함 되어 있으며,이는 office 365 Enterprise E5에 들어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="50d07-113">This is still the case, and now these features are now part of Office 365 Advanced Threat Protection Plan 2 (and this is included in Office 365 Enterprise E5).</span></span> 

<span data-ttu-id="50d07-114">또한 office 365 위협 조사 및 응답 capbailities는 이전에 office 365 for business 고객을 위한 추가 기능으로 구매할 수 있었습니다.</span><span class="sxs-lookup"><span data-stu-id="50d07-114">In addition, Office 365 Threat investigation and response capbailities were formerly available for purchase as an add-on for Office 365 for business customers.</span></span> <span data-ttu-id="50d07-115">이제 이러한 기능은 office 365 advanced threat protection 계획 2 (office 365 advanced threat protection plan 1 포함)에 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="50d07-115">Now, these capabilities are included in Office 365 Advanced Threat Protection Plan 2 (which also includes Office 365 Advanced Threat Protection Plan 1).</span></span> <span data-ttu-id="50d07-116">자세한 내용은 [Office 365 Advanced Threat Protection 요금제 및 가격 책정](https://products.office.com/exchange/advance-threat-protection)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="50d07-116">To learn more, see [Office 365 Advanced Threat Protection plans and pricing](https://products.office.com/exchange/advance-threat-protection).</span></span>

<span data-ttu-id="50d07-117">이 모든 것을 의미 하는 것은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="50d07-117">Here's what all this means:</span></span>

- <span data-ttu-id="50d07-118">**조직에 이미 Office 365 Enterprise E5가 있는 경우**Advanced threat Protection 계획 2가 이미 있고, 위협 조사 및 대응 기능도 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="50d07-118">**If your organization already has Office 365 Enterprise E5**, then you already have Advanced Threat Protection Plan 2, and this includes Threat investigation and response capabilities.</span></span>

- <span data-ttu-id="50d07-119">**조직에서 이전에 office 365 위협 인텔리전스 (office 365 Advanced threat Protection 제외)** 가 다른 office 365 구독에 대 한 추가 기능으로 사용 되는 경우 office 365 Advanced threat protection 계획 2가 됩니다.</span><span class="sxs-lookup"><span data-stu-id="50d07-119">**If your organization previously had Office 365 Threat Intelligence (but not Office 365 Advanced Threat Protection) as an add-on** to another Office 365 subscription, then you will have Office 365 Advanced Threat Protection Plan 2.</span></span> <span data-ttu-id="50d07-120">여기에는 Advanced threat Protection 계획 1 및 위협 조사 및 응답 기능이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="50d07-120">This includes Advanced Threat Protection Plan 1 and Threat investigation and response capabilities.</span></span> 

- <span data-ttu-id="50d07-121">**조직에서 이전에 office 365 advanced threat protection (office 365 위협 인텔리전스)** 을 다른 office 365 구독에 추가 기능으로 사용 하는 경우 office 365 Advanced threat protection 계획 1이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="50d07-121">**If your organization previously had Office 365 Advanced Threat Protection (but not Office 365 Threat Intelligence) as an add-on** to another Office 365 subscription, then you will have Office 365 Advanced Threat Protection Plan 1.</span></span> <span data-ttu-id="50d07-122">여기에는 Advanced threat Protection (위협 investigaiton 및 응답 기능이 아님)이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="50d07-122">This includes Advanced Threat Protection (but not Threat investigaiton and response capabilities).</span></span>

<span data-ttu-id="50d07-123">자세한 내용은 [office 365 advanced threat protection 요금제 및 가격](https://products.office.com/exchange/advance-threat-protection) 및 [office 365 advanced threat protection 서비스 설명](https://docs.microsoft.com/en-us/office365/servicedescriptions/office-365-advanced-threat-protection-service-description#whats-new-in-office-365-advanced-threat-protection-atp) 를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="50d07-123">For more information, see [Office 365 Advanced Threat Protection plans and pricing](https://products.office.com/exchange/advance-threat-protection) and the [Office 365 Advanced Threat Protection Service Description](https://docs.microsoft.com/en-us/office365/servicedescriptions/office-365-advanced-threat-protection-service-description#whats-new-in-office-365-advanced-threat-protection-atp)</span></span>

## <a name="get-started-with-threat-investigaiton-and-response-capabilities"></a><span data-ttu-id="50d07-124">위협 investigaiton 및 응답 기능 시작</span><span class="sxs-lookup"><span data-stu-id="50d07-124">Get started with threat investigaiton and response capabilities</span></span>

<span data-ttu-id="50d07-125">다음 리소스를 사용 하 여 Office 365의 위협 조사 및 응답 기능에 대해 자세히 알아보고 조직의 사용자를 보다 안전 하 게 유지 하는 방법을 알아보세요.</span><span class="sxs-lookup"><span data-stu-id="50d07-125">Use the following resources to learn more about threat investigation and response capabilities in Office 365, and how you can use it to keep people in your organization safer.</span></span>
  
- <span data-ttu-id="50d07-126">[위협 조사 및 응답 시작](get-started-with-ti.md) (필수 역할에 대 한 정보가 포함 됩니다.)</span><span class="sxs-lookup"><span data-stu-id="50d07-126">[Get started with Threat Investigation and Response](get-started-with-ti.md) (this includes information about required roles)</span></span> 
    
- [<span data-ttu-id="50d07-127">위협 추적기에 대해 알아보기-신규 및 중요</span><span class="sxs-lookup"><span data-stu-id="50d07-127">Learn about Threat Trackers - New and Noteworthy</span></span>](threat-trackers.md)
    
- [<span data-ttu-id="50d07-128">배달 된 악성 전자 메일 찾기 및 조사</span><span class="sxs-lookup"><span data-stu-id="50d07-128">Find and investigate malicious email that was delivered</span></span>](investigate-malicious-email-that-was-delivered.md)
    
- [<span data-ttu-id="50d07-129">공격 시뮬레이터 사용</span><span class="sxs-lookup"><span data-stu-id="50d07-129">Use Attack Simulator</span></span>](attack-simulator.md)
    
- [<span data-ttu-id="50d07-130">Windows Defender Advanced Threat Protection을 통한 위협 조사 및 대응 통합</span><span class="sxs-lookup"><span data-stu-id="50d07-130">Integrate Threat Investigation and Response with Windows Defender Advanced Threat Protection</span></span>](integrate-office-365-ti-with-wdatp.md)
    
## <a name="related-topics"></a><span data-ttu-id="50d07-131">관련 항목</span><span class="sxs-lookup"><span data-stu-id="50d07-131">Related topics</span></span>

[<span data-ttu-id="50d07-132">Office 365에서 위협 으로부터 보호</span><span class="sxs-lookup"><span data-stu-id="50d07-132">Protect against threats in Office 365</span></span>](protect-against-threats.md)
  
[<span data-ttu-id="50d07-133">Office 365 Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="50d07-133">Office 365 Advanced Threat Protection</span></span>](office-365-atp.md)
  
[<span data-ttu-id="50d07-134">Permissions in the Office 365 Security &amp; Compliance Center</span><span class="sxs-lookup"><span data-stu-id="50d07-134">Permissions in the Office 365 Security &amp; Compliance Center</span></span>](permissions-in-the-security-and-compliance-center.md)
 