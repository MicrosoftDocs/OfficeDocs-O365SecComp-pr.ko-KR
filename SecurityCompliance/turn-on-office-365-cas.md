---
title: Office 365 Cloud App Security 켜기
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: ba919c73-d021-404d-9850-eec57e78678c
description: 이 문서를 읽으면 Microsoft Azure에서 cloud app security에서 제공 하는 Office 365 Cloud app security를 설정 하는 방법을 확인할 수 있습니다.
ms.openlocfilehash: 1227545b1e4d1521dc1820342f09aabdf16ec2c6
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30220368"
---
# <a name="turn-on-office-365-cloud-app-security"></a><span data-ttu-id="aa1dc-103">Office 365 Cloud App Security 켜기</span><span class="sxs-lookup"><span data-stu-id="aa1dc-103">Turn on Office 365 Cloud App Security</span></span>
  
|<span data-ttu-id="aa1dc-104">계산 \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="aa1dc-104">\*\*\*\*Evaluation\*\* \>\*\*</span></span>|<span data-ttu-id="aa1dc-105">계획 \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="aa1dc-105">\*\*\*\*Planning\*\* \>\*\*</span></span>|<span data-ttu-id="aa1dc-106">배포 \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="aa1dc-106">\*\*\*\*Deployment\*\* \>\*\*</span></span>|<span data-ttu-id="aa1dc-107">사용률 \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="aa1dc-107">\*\*\*\*Utilization\*\*\*\*</span></span>|
|:-----|:-----|:-----|:-----|
|[<span data-ttu-id="aa1dc-108">평가 시작</span><span class="sxs-lookup"><span data-stu-id="aa1dc-108">Start evaluating</span></span>](office-365-cas-overview.md) <br/> |[<span data-ttu-id="aa1dc-109">계획 시작</span><span class="sxs-lookup"><span data-stu-id="aa1dc-109">Start planning</span></span>](get-ready-for-office-365-cas.md) <br/> |<span data-ttu-id="aa1dc-110">사용자가 여기 있어!</span><span class="sxs-lookup"><span data-stu-id="aa1dc-110">You are here!</span></span>  <br/> [<span data-ttu-id="aa1dc-111">다음 단계</span><span class="sxs-lookup"><span data-stu-id="aa1dc-111">Next step</span></span>](activity-policies-and-alerts.md) <br/> |[<span data-ttu-id="aa1dc-112">활용 시작</span><span class="sxs-lookup"><span data-stu-id="aa1dc-112">Start utilizing</span></span>](utilization-activities-for-ocas.md) <br/> |
  
## <a name="turn-on-office-365-cloud-app-security"></a><span data-ttu-id="aa1dc-113">Office 365 Cloud App Security 켜기</span><span class="sxs-lookup"><span data-stu-id="aa1dc-113">Turn on Office 365 Cloud App Security</span></span>

> [!IMPORTANT]
> <span data-ttu-id="aa1dc-p101">다음 작업을 수행 하려면 전역 관리자 이거나 보안 관리자 여야 합니다. 자세한 내용은 [Office 365 보안 &amp; 및 준수 센터의 사용 권한](permissions-in-the-security-and-compliance-center.md)를 참조 하세요. office 365 Cloud App Security이 올바르게 작동 하려면 office 365 환경에 대해 **감사 로깅을 켜야 합니다** . 자세한 내용은 [Turn Office 365 감사 로그 검색 켜기 또는 끄기를](turn-audit-log-search-on-or-off.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="aa1dc-p101">You must be a global administrator or security administrator to perform the following task. To learn more, see [Permissions in the Office 365 Security &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md). In order for Office 365 Cloud App Security to work correct, **audit logging must be turned on** for your Office 365 environment. For more information, see [Turn Office 365 audit log search on or off](turn-audit-log-search-on-or-off.md).</span></span> 
  
1. <span data-ttu-id="aa1dc-p102">전역 관리자 또는 보안 관리자로 이동 [https://protection.office.com](https://security.microsoft.com) 하 여 회사 또는 Office 365의 학교 계정을 사용 하 여 로그인 합니다. (보안 &amp; 및 준수 센터로 이동 합니다.)</span><span class="sxs-lookup"><span data-stu-id="aa1dc-p102">As a global administrator or security administrator, go to [https://protection.office.com](https://security.microsoft.com) and sign in using your work or school account for Office 365. (This takes you to the Security &amp; Compliance Center.)</span></span> 
    
2. <span data-ttu-id="aa1dc-120">**경고** \> 로 이동 하 여 **고급 알림을 관리**합니다.</span><span class="sxs-lookup"><span data-stu-id="aa1dc-120">Go to **Alerts** \> **Manage advanced alerts**.</span></span>
    
3. <span data-ttu-id="aa1dc-121">**Office 365 Cloud App Security 사용을**선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="aa1dc-121">Select **Turn on Office 365 Cloud App Security**.</span></span>
    
4. <span data-ttu-id="aa1dc-122">**Office 365 Cloud App Security로 이동을**선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="aa1dc-122">Choose **Go to Office 365 Cloud App Security**.</span></span><br/><span data-ttu-id="aa1dc-123">![보안 &amp; 및 준수 센터에서 Office 365 Cloud App Security로 이동 하려면 고급 알림 관리를 선택 합니다.](media/958632d4-03e3-4ade-8e22-d5509db6fca7.png)</span><span class="sxs-lookup"><span data-stu-id="aa1dc-123">![In the Security &amp; Compliance Center, choose Manage Advanced Alerts to go to Office 365 Cloud App Security](media/958632d4-03e3-4ade-8e22-d5509db6fca7.png)</span></span><br/><span data-ttu-id="aa1dc-124">이렇게 하면 보고서를 보고, 정책을 만들거나 편집할 수 있는 Office 365 Cloud App Security 포털로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="aa1dc-124">This takes you to the Office 365 Cloud App Security portal, where you can view reports and create or edit your policies.</span></span>

<span data-ttu-id="aa1dc-125">Office 365 cloud app security를 설정한 후에 방문 [https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com) 하 여 로그인 하 여 Cloud app security 포털로 이동할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="aa1dc-125">After you have turned on Office 365 Cloud App Security, you can go to the Cloud App Security portal by visiting [https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com) and signing in.</span></span>
    
> [!NOTE]
> <span data-ttu-id="aa1dc-p103">office 365 Cloud app security를 켜면 office 365 사용자 계정 및 사용자 활동에 대 한 감사 정보가 [Microsoft Cloud App security](https://aka.ms/whatiscas)로 전송 됩니다. 이를 통해 Office 365에서 고급 경고, 필터링 및 기타 기능을 제공 하 여 의심 스러운 활동에 대 한 정보를 얻고 작업을 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="aa1dc-p103">When you turn on Office 365 Cloud App Security, auditing information about your Office 365 user accounts and user activities is transferred to [Microsoft Cloud App Security](https://aka.ms/whatiscas). This allows Office 365 to provide advanced alerts, filtering, and other features so you can get information and take action about suspicious activities.</span></span> 
  
## <a name="next-steps"></a><span data-ttu-id="aa1dc-128">다음 단계</span><span class="sxs-lookup"><span data-stu-id="aa1dc-128">Next steps</span></span>

- [<span data-ttu-id="aa1dc-129">활동 정책</span><span class="sxs-lookup"><span data-stu-id="aa1dc-129">Activity policies</span></span>](activity-policies-and-alerts.md)
    
- [<span data-ttu-id="aa1dc-130">변칙 검색 정책</span><span class="sxs-lookup"><span data-stu-id="aa1dc-130">Anomaly detection policies</span></span>](anomaly-detection-policies-in-ocas.md)
    
- [<span data-ttu-id="aa1dc-131">siem 서버 통합</span><span class="sxs-lookup"><span data-stu-id="aa1dc-131">Integrate your SIEM server</span></span>](integrate-your-siem-server-with-office-365-cas.md)
    
- [<span data-ttu-id="aa1dc-132">관리를 간소화 하는 IP 주소 그룹화</span><span class="sxs-lookup"><span data-stu-id="aa1dc-132">Group your IP addresses to simplify management</span></span>](group-your-ip-addresses-in-ocas.md)
    

