---
title: Office 365 Cloud App Security 켜기
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: ba919c73-d021-404d-9850-eec57e78678c
description: Office 365 고급 보안 관리 설정, 클라우드 앱 보안 Microsoft Azure에 의해 구동 하는 방법을 알아보려면이 문서를 읽어보십시오.
ms.openlocfilehash: 057a7b3311384901b4c3683c350d1f26c91bf60d
ms.sourcegitcommit: 7e2a0185cadea7f3a6afc5ddc445eac2e1ce22eb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/11/2019
ms.locfileid: "29603779"
---
# <a name="turn-on-office-365-cloud-app-security"></a><span data-ttu-id="b7ffd-103">Office 365 Cloud App Security 켜기</span><span class="sxs-lookup"><span data-stu-id="b7ffd-103">Turn on Office 365 Cloud App Security</span></span>
  
|<span data-ttu-id="b7ffd-104">평가 \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="b7ffd-104">\*\*\*\*Evaluation\*\* \>\*\*</span></span>|<span data-ttu-id="b7ffd-105">계획 \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="b7ffd-105">\*\*\*\*Planning\*\* \>\*\*</span></span>|<span data-ttu-id="b7ffd-106">배포 \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="b7ffd-106">\*\*\*\*Deployment\*\* \>\*\*</span></span>|<span data-ttu-id="b7ffd-107">사용률 \* \* \*</span><span class="sxs-lookup"><span data-stu-id="b7ffd-107">\*\*\*\*Utilization\*\*\*\*</span></span>|
|:-----|:-----|:-----|:-----|
|[<span data-ttu-id="b7ffd-108">평가 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="b7ffd-108">Start evaluating</span></span>](office-365-cas-overview.md) <br/> |[<span data-ttu-id="b7ffd-109">계획을 시작합니다</span><span class="sxs-lookup"><span data-stu-id="b7ffd-109">Start planning</span></span>](get-ready-for-office-365-cas.md) <br/> |<span data-ttu-id="b7ffd-110">여기는!</span><span class="sxs-lookup"><span data-stu-id="b7ffd-110">You are here!</span></span>  <br/> [<span data-ttu-id="b7ffd-111">다음 단계</span><span class="sxs-lookup"><span data-stu-id="b7ffd-111">Next step</span></span>](activity-policies-and-alerts.md) <br/> |[<span data-ttu-id="b7ffd-112">활용 하 여 시작</span><span class="sxs-lookup"><span data-stu-id="b7ffd-112">Start utilizing</span></span>](utilization-activities-for-ocas.md) <br/> |
  
## <a name="turn-on-office-365-cloud-app-security"></a><span data-ttu-id="b7ffd-113">Office 365 Cloud App Security 켜기</span><span class="sxs-lookup"><span data-stu-id="b7ffd-113">Turn on Office 365 Cloud App Security</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b7ffd-p101">다음 작업을 수행 하려면 전역 관리자 또는 보안 관리자 여야 합니다. 자세한 내용은 참조 [Office 365 보안에 대 한 사용 권한을 &amp; 준수 센터](permissions-in-the-security-and-compliance-center.md)합니다. Office 365 클라우드 앱 보안 작동 하도록 하기 위해에서 수정, Office 365 환경에 대 한 **감사 로깅을 설정 해야** 합니다. 자세한 내용은 [Office 365 설정 또는 해제 로그 검색 감사](turn-audit-log-search-on-or-off.md)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="b7ffd-p101">You must be a global administrator or security administrator to perform the following task. To learn more, see [Permissions in the Office 365 Security &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md). In order for Office 365 Cloud App Security to work correct, **audit logging must be turned on** for your Office 365 environment. For more information, see [Turn Office 365 audit log search on or off](turn-audit-log-search-on-or-off.md).</span></span> 
  
1. <span data-ttu-id="b7ffd-p102">전역 관리자 또는 보안 관리자로 이동 [https://protection.office.com](https://security.microsoft.com) 및 Office 365에 대 한 작업이 나 교육용 계정을 사용 하 여 로그인 합니다. (이렇게 하면 보안 &amp; 준수 센터.)</span><span class="sxs-lookup"><span data-stu-id="b7ffd-p102">As a global administrator or security administrator, go to [https://protection.office.com](https://security.microsoft.com) and sign in using your work or school account for Office 365. (This takes you to the Security &amp; Compliance Center.)</span></span> 
    
2. <span data-ttu-id="b7ffd-120">**경고** 로 이동 \> **관리 고급 알림**입니다.</span><span class="sxs-lookup"><span data-stu-id="b7ffd-120">Go to **Alerts** \> **Manage advanced alerts**.</span></span>
    
3. <span data-ttu-id="b7ffd-121">**Office 365 클라우드 응용 프로그램 보안 설정**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="b7ffd-121">Select **Turn on Office 365 Cloud App Security**.</span></span>
    
4. <span data-ttu-id="b7ffd-122">**Office 365 클라우드 응용 프로그램 보안으로 이동**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="b7ffd-122">Choose **Go to Office 365 Cloud App Security**.</span></span><br/><span data-ttu-id="b7ffd-123">![보안에서 &amp; 준수 센터 Office 365 클라우드 앱 보안으로 이동 하려면 고급 알림 관리를 선택 합니다.](media/958632d4-03e3-4ade-8e22-d5509db6fca7.png)</span><span class="sxs-lookup"><span data-stu-id="b7ffd-123">![In the Security &amp; Compliance Center, choose Manage Advanced Alerts to go to Office 365 Cloud App Security](media/958632d4-03e3-4ade-8e22-d5509db6fca7.png)</span></span><br/><span data-ttu-id="b7ffd-124">이 Office 365 클라우드 응용 프로그램 보안 포털, 여기서 수 보고서 보기 및 만들거나 편집할 정책에 위치로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="b7ffd-124">This takes you to the Office 365 Cloud App Security portal, where you can view reports and create or edit your policies.</span></span>

<span data-ttu-id="b7ffd-125">방문 하 여 클라우드 응용 프로그램 보안 포털으로 이동할 수 Office 365 클라우드 응용 프로그램 보안을 설정 하면 [https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com) 로그인 하 고 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b7ffd-125">After you have turned on Office 365 Cloud App Security, you can go to the Cloud App Security portal by visiting [https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com) and signing in.</span></span>
    
> [!NOTE]
> <span data-ttu-id="b7ffd-p103">Office 365 클라우드 응용 프로그램 보안을 설정 하면 Office 365 사용자 계정 및 사용자 작업에 대 한 감사 정보는 [Microsoft 클라우드 응용 프로그램 보안](https://aka.ms/whatiscas)로 전송 됩니다. 이 정보를 가져올 하 고 의심 스러운 활동에 대 한 조치를 취할 수 있도록 고급 알림, 필터링 및 기타 기능을 제공 하는 Office 365 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b7ffd-p103">When you turn on Office 365 Cloud App Security, auditing information about your Office 365 user accounts and user activities is transferred to [Microsoft Cloud App Security](https://aka.ms/whatiscas). This allows Office 365 to provide advanced alerts, filtering, and other features so you can get information and take action about suspicious activities.</span></span> 
  
## <a name="next-steps"></a><span data-ttu-id="b7ffd-128">다음 단계</span><span class="sxs-lookup"><span data-stu-id="b7ffd-128">Next steps</span></span>

- [<span data-ttu-id="b7ffd-129">작업 정책</span><span class="sxs-lookup"><span data-stu-id="b7ffd-129">Activity policies</span></span>](activity-policies-and-alerts.md)
    
- [<span data-ttu-id="b7ffd-130">예외 탐지 정책</span><span class="sxs-lookup"><span data-stu-id="b7ffd-130">Anomaly detection policies</span></span>](anomaly-detection-policies-in-ocas.md)
    
- [<span data-ttu-id="b7ffd-131">SIEM 서버 통합</span><span class="sxs-lookup"><span data-stu-id="b7ffd-131">Integrate your SIEM server</span></span>](integrate-your-siem-server-with-office-365-cas.md)
    
- [<span data-ttu-id="b7ffd-132">관리를 단순화 하 여 IP 주소를 그룹화</span><span class="sxs-lookup"><span data-stu-id="b7ffd-132">Group your IP addresses to simplify management</span></span>](group-your-ip-addresses-in-ocas.md)
    

