---
title: 정치적 캠페인, 비영리 조직 및 기타 기밀 조직에 대한 Microsoft 보안 지침
ms.author: bcarter
author: brendacarter
manager: laurawi
ms.date: 12/15/2017
ms.audience: ITPro
ms.topic: overview
ms.collection:
- Ent_O365
- Strat_O365_Enterprise
- M365-security-compliance
ms.service: O365-seccomp
localization_priority: Priority
search.appverid:
- MET150
ms.custom: Strat_O365_Enterprise
ms.assetid: 10d1004b-42b6-4e2b-aaa2-18ddd9118f64
description: '요약: 증가된 위협 프로필을 가진 빠르게 변화하는 조직에 대한 계획 및 구현 지침입니다.'
ms.openlocfilehash: 99539c2480aef3329f517fc855776f1bae463904
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32261342"
---
# <a name="microsoft-security-guidance-for-political-campaigns-nonprofits-and-other-agile-organizations"></a><span data-ttu-id="dc8bd-103">정치적 캠페인, 비영리 조직 및 기타 기밀 조직에 대한 Microsoft 보안 지침</span><span class="sxs-lookup"><span data-stu-id="dc8bd-103">Microsoft Security Guidance for Political Campaigns, Nonprofits, and Other Agile Organizations</span></span>

 <span data-ttu-id="dc8bd-104">**요약:** 증가된 위협 프로필을 가진 빠르게 변화하는 조직에 대한 계획 및 구현 지침입니다.</span><span class="sxs-lookup"><span data-stu-id="dc8bd-104">**Summary:** Planning and implementation guidance for fast-moving organizations that have an increased threat profile.</span></span>
  
<span data-ttu-id="dc8bd-p101">기밀 조직으로서 작은 IT 팀을 보유하고 위협 프로필이 평균보다 더 높은 경우 이 지침이 적용됩니다. 이 솔루션은 처음부터 보안 컨트롤을 포함한 필수 클라우드 서비스를 포함하는 환경을 빨리 구축하는 방법을 보여 줍니다. 이 지침은 데이터, ID, 메일 및 액세스를 모바일 장치로부터 보호하기 위한 규정 보안 권장 사항을 포함합니다.</span><span class="sxs-lookup"><span data-stu-id="dc8bd-p101">If your organization is agile, you have a small IT team, and your threat profile is higher than average, this guidance is designed for you. This solution demonstrates how to quickly build an environment with essential cloud services that include secure controls from the start. This guidance includes prescriptive security recommendations for protecting data, identities, email, and access from mobile devices.</span></span>
  
## <a name="security-solution-guidance"></a><span data-ttu-id="dc8bd-108">보안 솔루션 지침</span><span class="sxs-lookup"><span data-stu-id="dc8bd-108">Security solution guidance</span></span>

<span data-ttu-id="dc8bd-p102">이 지침은 보안 클라우드 환경을 구현하는 방법에 대해 설명합니다. 이 솔루션 지침을 어떤 조직에서도 사용할 수 있습니다. 이 지침은 BYOD 액세스 및 게스트 계정을 가진 기밀 조직에 도움이 되는 내용을 포함합니다. 이 지침을 자신의 환경 설계를 위한 시작점으로 사용할 수 있습니다. 의견이 있으시면 언제든지 보내주세요[CloudAdopt@microsoft.com](mailto:CloudAdopt@microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="dc8bd-p102">This guidance describes how to implement a secure cloud environment. The solution guidance can be used by any organization. It includes extra help for agile organizations with BYOD access and guest accounts. You can use this guidance as a starting-point for designing your own environment. We welcome your feedback at [CloudAdopt@microsoft.com](mailto:CloudAdopt@microsoft.com).</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="dc8bd-114">**항목**</span><span class="sxs-lookup"><span data-stu-id="dc8bd-114">**Item**</span></span> <br/> |<span data-ttu-id="dc8bd-115">**설명**</span><span class="sxs-lookup"><span data-stu-id="dc8bd-115">**Description**</span></span> <br/> |
|<span data-ttu-id="dc8bd-116">**정치적 캠페인을 위한 Microsoft 보안 지침**</span><span class="sxs-lookup"><span data-stu-id="dc8bd-116">**Microsoft Security Guidance for Political Campaigns**</span></span> <br/> <span data-ttu-id="dc8bd-117">[![미니 포스터 집합에 대한 미리 보기입니다.](media/d370ce28-ca40-4930-9a2c-907312aa06c8.png)          ](http://download.microsoft.com/download/B/4/D/B4D520C3-4D0C-4B4D-BFB9-09F0651C2775/MSFT_Cloud_architecture_security%20for%20political%20campaigns.pdf)</span><span class="sxs-lookup"><span data-stu-id="dc8bd-117">[![Thumb nail for mini poster set.](media/d370ce28-ca40-4930-9a2c-907312aa06c8.png)          ](http://download.microsoft.com/download/B/4/D/B4D520C3-4D0C-4B4D-BFB9-09F0651C2775/MSFT_Cloud_architecture_security%20for%20political%20campaigns.pdf)</span></span> <br/> <span data-ttu-id="dc8bd-118">[PDF](http://download.microsoft.com/download/B/4/D/B4D520C3-4D0C-4B4D-BFB9-09F0651C2775/MSFT_Cloud_architecture_security%20for%20political%20campaigns.pdf)  \| [Visio](http://download.microsoft.com/download/B/4/D/B4D520C3-4D0C-4B4D-BFB9-09F0651C2775/MSFT_Cloud_architecture_security%20for%20political%20campaigns.vsdx)</span><span class="sxs-lookup"><span data-stu-id="dc8bd-118">[PDF](http://download.microsoft.com/download/B/4/D/B4D520C3-4D0C-4B4D-BFB9-09F0651C2775/MSFT_Cloud_architecture_security%20for%20political%20campaigns.pdf)  \| [Visio](http://download.microsoft.com/download/B/4/D/B4D520C3-4D0C-4B4D-BFB9-09F0651C2775/MSFT_Cloud_architecture_security%20for%20political%20campaigns.vsdx)</span></span> <br/> |<span data-ttu-id="dc8bd-p103">이 지침에서는 정치적 캠페인 조직을 보기로 사용합니다. 이 지침을 어떤 환경에 대해서도 시작점으로 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dc8bd-p103">This guidance uses a political campaign organization as an example. Use this guidance as a starting point for any environment.</span></span>  <br/> |
|<span data-ttu-id="dc8bd-121">**비영리 조직을 위한 Microsoft 보안 지침**</span><span class="sxs-lookup"><span data-stu-id="dc8bd-121">**Microsoft Security Guidance for Nonprofits**</span></span> <br/> <span data-ttu-id="dc8bd-122">[![다운로드 가능한 파일에 대한 미리 보기 이미지](media/e4784889-1c69-4067-9a8f-31d31d1eceea.png)          ](http://download.microsoft.com/download/9/4/3/94389612-C679-4061-8DF2-D9A15D72B65F/Microsoft_Cloud%20Architecture_Security%20for%20Nonprofits.pdf)</span><span class="sxs-lookup"><span data-stu-id="dc8bd-122">[![Thumnail image for downloadable file](media/e4784889-1c69-4067-9a8f-31d31d1eceea.png)          ](http://download.microsoft.com/download/9/4/3/94389612-C679-4061-8DF2-D9A15D72B65F/Microsoft_Cloud%20Architecture_Security%20for%20Nonprofits.pdf)</span></span> <br/> <span data-ttu-id="dc8bd-123">[PDF](http://download.microsoft.com/download/9/4/3/94389612-C679-4061-8DF2-D9A15D72B65F/Microsoft_Cloud%20Architecture_Security%20for%20Nonprofits.pdf)  \| [Visio](http://download.microsoft.com/download/9/4/3/94389612-C679-4061-8DF2-D9A15D72B65F/Microsoft_Cloud%20Architecture_Security%20for%20Nonprofits.vsdx)</span><span class="sxs-lookup"><span data-stu-id="dc8bd-123">[PDF](http://download.microsoft.com/download/9/4/3/94389612-C679-4061-8DF2-D9A15D72B65F/Microsoft_Cloud%20Architecture_Security%20for%20Nonprofits.pdf)  \| [Visio](http://download.microsoft.com/download/9/4/3/94389612-C679-4061-8DF2-D9A15D72B65F/Microsoft_Cloud%20Architecture_Security%20for%20Nonprofits.vsdx)</span></span> <br/> |<span data-ttu-id="dc8bd-p104">이 지침은 비영리 조직을 위해 약간 수정하였습니다. 예를 들어 Office 365 비영리 조직 계획을 참조합니다. 기술 지침은 정치적 캠페인 솔루션 가이드와 같습니다.</span><span class="sxs-lookup"><span data-stu-id="dc8bd-p104">This guide is slightly revised for nonprofit organizations. For example, it references Office 365 Nonprofit plans. The technical guidance is the same as the political campaign solution guide.</span></span>  <br/> |
   
## <a name="test-lab-guides"></a><span data-ttu-id="dc8bd-127">테스트 랩 가이드</span><span class="sxs-lookup"><span data-stu-id="dc8bd-127">Test Lab Guides</span></span>

<span data-ttu-id="dc8bd-128">이 솔루션에 대한 개발/테스트 환경을 만들려면 다음 테스트 랩 가이드를 사용하세요.</span><span class="sxs-lookup"><span data-stu-id="dc8bd-128">To create a dev/test environment for this solution, use the following test lab guides:</span></span> 
  
- [<span data-ttu-id="dc8bd-129">정치적 캠페인 개발/테스트 환경에 대해 그룹 및 사용자 구성</span><span class="sxs-lookup"><span data-stu-id="dc8bd-129">Configure groups and users for a political campaign dev/test environment</span></span>](https://docs.microsoft.com/office365/enterprise/configure-groups-and-users-for-a-political-campaign-dev-test-environment)
    
     <span data-ttu-id="dc8bd-130">Office 365 및 EMS용 평가판 구독을 만들고 대표적인 정치적 캠페인에 대한 그룹 및 사용자를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="dc8bd-130">Create trial subscriptions for Office 365 and EMS and then create groups and users for a representative political campaign.</span></span>
    
- [<span data-ttu-id="dc8bd-131">정치적 캠페인 개발/테스트 환경에서 팀 사이트 만들기</span><span class="sxs-lookup"><span data-stu-id="dc8bd-131">Create team sites in a political campaign dev/test environment</span></span>](https://docs.microsoft.com/office365/enterprise/create-team-sites-in-a-political-campaign-dev-test-environment)
    
    <span data-ttu-id="dc8bd-132">내부, 개인, 중요 및 극비 보안 수준으로 SharePoint Online 팀 사이트를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="dc8bd-132">Create four SharePoint Online team sites with Internal, Private, Sensitive, and Highly Confidential levels of security.</span></span>
    
<span data-ttu-id="dc8bd-133">데모 또는 개념 증명을 위한 추가 보안 기능에 대해서는 [Office 365 테스트 랩 가이드](http://aka.ms/o365tlgs)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="dc8bd-133">For additional security features for demonstration or proof of concept, see [Office 365 Test Lab Guides](http://aka.ms/o365tlgs).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="dc8bd-134">참고 항목</span><span class="sxs-lookup"><span data-stu-id="dc8bd-134">See Also</span></span>

[<span data-ttu-id="dc8bd-135">클라우드 도입 TLG(테스트 랩 가이드)</span><span class="sxs-lookup"><span data-stu-id="dc8bd-135">Cloud adoption Test Lab Guides (TLGs)</span></span>](https://docs.microsoft.com/office365/enterprise/cloud-adoption-test-lab-guides-tlgs)
  
[<span data-ttu-id="dc8bd-136">Microsoft 클라우드 IT 아키텍처 리소스</span><span class="sxs-lookup"><span data-stu-id="dc8bd-136">Microsoft Cloud IT architecture resources</span></span>](https://docs.microsoft.com/office365/enterprise/microsoft-cloud-it-architecture-resources)



