---
title: Office 365 위협 조사 및 응답
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 03/18/2019
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
description: office 365 Advanced threat Protection의 위협 인텔리전스 기능을 통해 조직에 대 한 위협을 파악 하 고, 맬웨어, 피싱 및 기타 공격에 대처 하 고 사용자를 대신 하 여 Office 365에서 검색 한 기타 공격과 위협을 검색할 수 있는 방법을 알아봅니다. 슬라이더.
ms.openlocfilehash: 6f7e6e0a49bb4035458af2e9d7e45fd954a1f9fc
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32265400"
---
# <a name="office-365-threat-investigation-and-response"></a><span data-ttu-id="ac756-103">Office 365 위협 조사 및 응답</span><span class="sxs-lookup"><span data-stu-id="ac756-103">Office 365 threat investigation and response</span></span>

<span data-ttu-id="ac756-104">위협 조사 및 [Office 365 Advanced threat Protection](office-365-atp.md) 의 응답 기능은 보안 분석가와 관리자가 조직의 Office 365 사용자를 보호 하는 데 도움이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ac756-104">Threat investigation and response capabilities in [Office 365 Advanced Threat Protection](office-365-atp.md) help security analysts and administrators protect their organization's Office 365 users by:</span></span>
  
1. <span data-ttu-id="ac756-105">공격을 쉽게 식별 하 고 모니터링 하 고 이해할 수 있도록 설정</span><span class="sxs-lookup"><span data-stu-id="ac756-105">Making it easy to identify, monitor and understand attacks</span></span>
    
2. <span data-ttu-id="ac756-106">Exchange online, SharePoint online, 비즈니스용 OneDrive 및 Microsoft 팀의 위협에 빠르게 문제를 해결 하는 데 도움을 줍니다.</span><span class="sxs-lookup"><span data-stu-id="ac756-106">Helping to quickly address threats in Exchange Online, SharePoint Online, OneDrive for Business and Microsoft Teams</span></span>
    
3. <span data-ttu-id="ac756-107">조직에서 공격을 방지 하는 데 도움이 되는 정보를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="ac756-107">Providing insights and knowledge to help prevent attacks against their organization</span></span>

4. <span data-ttu-id="ac756-108">중요 전자 메일 기반 위협에 대 한 자동화 된 조사 및 응답</span><span class="sxs-lookup"><span data-stu-id="ac756-108">Automated investigation and response for critical email based threats</span></span>
    
> [!IMPORTANT]
> <span data-ttu-id="ac756-109">office **365 advanced threat protection 및 위협 조사 및 응답 (이전에는 office 365 위협 인텔리전스)은 이제 office 365 advanced threat protection 계획 2**로,에 포함 된 추가 위협 방지 기능과 함께 [microsoft 365 Enterprise](https://www.microsoft.com/microsoft-365/enterprise/home), [microsoft 365 Business](https://www.microsoft.com/microsoft-365/business), office 365 Enterprise E5, office 365 교육용 A5 등의 특정 구독 조직에서 Office 365 ATP를 포함 하지 않는 구독을 사용 하는 경우 ATP를 추가 기능으로 구입할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ac756-109">**Office 365 Advanced Threat Protection and Threat Investigation and Response (previously known as Office 365 Threat Intelligence) are now Office 365 Advanced Threat Protection Plan 2**, along with additional threat protection capabilities included in in certain subscriptions, such as [Microsoft 365 Enterprise](https://www.microsoft.com/microsoft-365/enterprise/home), [Microsoft 365 Business](https://www.microsoft.com/microsoft-365/business), Office 365 Enterprise E5, Office 365 Education A5, etc. If your organization has a subscription that does not include Office 365 ATP, you can potentially purchase ATP as an add-on.</span></span> <span data-ttu-id="ac756-110">자세한 내용은 [office 365 advanced threat protection 요금제 및 가격](https://products.office.com/exchange/advance-threat-protection) 및 [office 365 advanced threat protection 서비스 설명을](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description#whats-new-in-office-365-advanced-threat-protection-atp)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="ac756-110">For more information, see [Office 365 Advanced Threat Protection plans and pricing](https://products.office.com/exchange/advance-threat-protection) and the [Office 365 Advanced Threat Protection Service Description](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description#whats-new-in-office-365-advanced-threat-protection-atp).</span></span> 
  
## <a name="whats-changing"></a><span data-ttu-id="ac756-111">변경 된 기능</span><span class="sxs-lookup"><span data-stu-id="ac756-111">What's changing?</span></span>

<span data-ttu-id="ac756-112">이전에는 office 365 Enterprise e 5와 같은 위험 인텔리전스가 구독에 포함 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="ac756-112">Formerly, Office 365 Threat Intelligence was included in subscriptions, such as Office 365 Enterprise E5.</span></span> <span data-ttu-id="ac756-113">이러한 경우에도 위협 조사 및 응답 기능이 office 365 Advanced threat Protection 계획 2에 속하며,이는 office 365 Enterprise e 3에 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ac756-113">This is still the case, as threat investigation and response capabilities are now part of Office 365 Advanced Threat Protection Plan 2 (and this is included in Office 365 Enterprise E5).</span></span> 

<span data-ttu-id="ac756-114">또한 office 365 위협 인텔리전스는 이전에 office 365 for business 고객을 위한 추가 기능으로 구매할 수 있었습니다.</span><span class="sxs-lookup"><span data-stu-id="ac756-114">In addition, Office 365 Threat Intelligence was formerly available for purchase as an add-on for Office 365 for business customers.</span></span> <span data-ttu-id="ac756-115">이제 이러한 기능은 office 365 advanced threat protection 계획 2 (office 365 advanced threat protection 계획 1의 모든 기능과 함께)에 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ac756-115">Now, these capabilities are included in Office 365 Advanced Threat Protection Plan 2 (along with all the features in Office 365 Advanced Threat Protection Plan 1).</span></span> <span data-ttu-id="ac756-116">자세한 내용은 [Office 365 Advanced Threat Protection 요금제 및 가격 책정](https://products.office.com/exchange/advance-threat-protection)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="ac756-116">To learn more, see [Office 365 Advanced Threat Protection plans and pricing](https://products.office.com/exchange/advance-threat-protection).</span></span>

<span data-ttu-id="ac756-117">이 모든 것을 의미 하는 것은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="ac756-117">Here's what all this means:</span></span>

- <span data-ttu-id="ac756-118">**조직에 이미 Office 365 Enterprise E5가 있는 경우**Advanced threat Protection 계획 2가 이미 있고, 위협 조사 및 대응 기능도 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ac756-118">**If your organization already has Office 365 Enterprise E5**, then you already have Advanced Threat Protection Plan 2, and this includes threat investigation and response capabilities.</span></span>

- <span data-ttu-id="ac756-119">조직에서 이전에 다른 office 365 구독에 대 한 **추가 기능으로 office 365 위협 인텔리전스 (office 365 Advanced threat protection이 아님)** 가 있는 경우 이제 office 365 Advanced threat protection 계획 2가 제공 되며, 여기에는 다음이 포함 됩니다. 위협 조사 및 응답 기능</span><span class="sxs-lookup"><span data-stu-id="ac756-119">**If your organization previously had Office 365 Threat Intelligence (but not Office 365 Advanced Threat Protection) as an add-on** to another Office 365 subscription, then you will now have Office 365 Advanced Threat Protection Plan 2, and this includes threat investigation and response capabilities.</span></span> 

- <span data-ttu-id="ac756-120">**조직에서 이전에 office 365 advanced threat protection (office 365 위협 인텔리전스)** 을 다른 office 365 구독에 추가 기능으로 사용 하는 경우에는 이제 office 365 Advanced threat protection 계획 1이 발생 합니다.</span><span class="sxs-lookup"><span data-stu-id="ac756-120">**If your organization previously had Office 365 Advanced Threat Protection (but not Office 365 Threat Intelligence) as an add-on** to another Office 365 subscription, then you will now have Office 365 Advanced Threat Protection Plan 1.</span></span> <span data-ttu-id="ac756-121">여기에는 Office 365 Advanced Threat Protection 계획 1 (위협 조사 및 응답 기능이 아님)이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ac756-121">This includes Office 365 Advanced Threat Protection Plan 1, (but not threat investigation and response capabilities).</span></span>

<span data-ttu-id="ac756-122">자세한 내용은 [office 365 advanced threat protection 요금제 및 가격](https://products.office.com/exchange/advance-threat-protection) 및 [office 365 advanced threat protection 서비스 설명](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description#whats-new-in-office-365-advanced-threat-protection-atp) 를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="ac756-122">For more information, see [Office 365 Advanced Threat Protection plans and pricing](https://products.office.com/exchange/advance-threat-protection) and the [Office 365 Advanced Threat Protection Service Description](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description#whats-new-in-office-365-advanced-threat-protection-atp)</span></span>

## <a name="get-started-with-threat-investigation-and-response-capabilities"></a><span data-ttu-id="ac756-123">위협 조사 및 응답 기능 시작</span><span class="sxs-lookup"><span data-stu-id="ac756-123">Get started with threat investigation and response capabilities</span></span>

<span data-ttu-id="ac756-124">다음 리소스를 사용 하 여 Office 365의 위협 조사 및 응답 기능에 대해 자세히 알아보고 조직의 사용자를 보다 안전 하 게 유지 하는 방법을 알아보세요.</span><span class="sxs-lookup"><span data-stu-id="ac756-124">Use the following resources to learn more about threat investigation and response capabilities in Office 365, and how you can use it to keep people in your organization safer.</span></span>
  
- <span data-ttu-id="ac756-125">[위협 조사 및 응답 시작](get-started-with-ti.md) (필수 역할에 대 한 정보가 포함 됩니다.)</span><span class="sxs-lookup"><span data-stu-id="ac756-125">[Get started with Threat Investigation and Response](get-started-with-ti.md) (this includes information about required roles)</span></span> 
    
- [<span data-ttu-id="ac756-126">위협 추적기에 대해 알아보기-신규 및 중요</span><span class="sxs-lookup"><span data-stu-id="ac756-126">Learn about Threat Trackers - New and Noteworthy</span></span>](threat-trackers.md)

- [<span data-ttu-id="ac756-127">Office 365 위협 인텔리전스를 사용한 자동화 된 조사 및 응답 (AIR)</span><span class="sxs-lookup"><span data-stu-id="ac756-127">Automated Investigation and Response (AIR) with Office 365 Threat Intelligence</span></span>](automated-investigation-response-office.md)

- [<span data-ttu-id="ac756-128">보안 &amp; 및 준수 센터에서 위협 탐색기 사용</span><span class="sxs-lookup"><span data-stu-id="ac756-128">Use Threat Explorer in the Security &amp; Compliance Center</span></span>](use-explorer-in-security-and-compliance.md)
    
- [<span data-ttu-id="ac756-129">배달된 악성 전자 메일 찾기 및 조사</span><span class="sxs-lookup"><span data-stu-id="ac756-129">Find and investigate malicious email that was delivered</span></span>](investigate-malicious-email-that-was-delivered.md)
    
- [<span data-ttu-id="ac756-130">공격 시뮬레이터 사용</span><span class="sxs-lookup"><span data-stu-id="ac756-130">Use Attack Simulator</span></span>](attack-simulator.md)
    
- [<span data-ttu-id="ac756-131">Windows Defender Advanced Threat Protection을 통한 위협 조사 및 대응 통합</span><span class="sxs-lookup"><span data-stu-id="ac756-131">Integrate Threat Investigation and Response with Windows Defender Advanced Threat Protection</span></span>](integrate-office-365-ti-with-wdatp.md)
    
## <a name="related-topics"></a><span data-ttu-id="ac756-132">관련 항목</span><span class="sxs-lookup"><span data-stu-id="ac756-132">Related topics</span></span>

[<span data-ttu-id="ac756-133">위협 탐색기 보기</span><span class="sxs-lookup"><span data-stu-id="ac756-133">Threat Explorer views</span></span>](threat-explorer-views.md)

[<span data-ttu-id="ac756-134">Office 365에서 위협 으로부터 보호</span><span class="sxs-lookup"><span data-stu-id="ac756-134">Protect against threats in Office 365</span></span>](protect-against-threats.md)
  
[<span data-ttu-id="ac756-135">Office 365 Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="ac756-135">Office 365 Advanced Threat Protection</span></span>](office-365-atp.md)
  
[<span data-ttu-id="ac756-136">Permissions in the Office 365 Security &amp; Compliance Center</span><span class="sxs-lookup"><span data-stu-id="ac756-136">Permissions in the Office 365 Security &amp; Compliance Center</span></span>](permissions-in-the-security-and-compliance-center.md)
 
