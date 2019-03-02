---
title: Office 365 위협 인텔리전스 및 Advanced Threat Protection과의 siem 통합
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.audience: ITPro
ms.topic: overview
ms.service: O365-seccomp
localization_priority: None
search.appverid:
- MET150
- MOE150
ms.assetid: eb56b69b-3170-4086-82cf-ba40a530fa1b
ms.collection:
- M365-security-compliance
description: office 365 활동 관리 API를 사용 하 여 조직의 siem 서버를 office 365 위협 인텔리전스 및 Advanced Threat Protection과 통합 합니다.
ms.openlocfilehash: 68d2b4387c1af2363fbb67d0671edeaaa4dc652d
ms.sourcegitcommit: 7adfd8eda038cf25449bdf3df78b5e2fcc1999e7
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/01/2019
ms.locfileid: "30357439"
---
# <a name="siem-integration-with-office-365-threat-intelligence-and-advanced-threat-protection"></a><span data-ttu-id="984d8-103">Office 365 위협 인텔리전스 및 Advanced Threat Protection과의 siem 통합</span><span class="sxs-lookup"><span data-stu-id="984d8-103">SIEM integration with Office 365 Threat Intelligence and Advanced Threat Protection</span></span>

<span data-ttu-id="984d8-p101">조직에서 siem (보안 인시던트 및 이벤트 관리) 서버를 사용 하는 경우 Office 365 위협 인텔리전스 및 Advanced Threat Protection을 siem 서버와 통합할 수 있습니다. siem 통합을 사용 하면 siem server reports에서 Office 365 Advanced Protection 및 위협 인텔리전스를 통해 검색 된 맬웨어 같은 정보를 볼 수 있습니다. siem 통합을 설정 하려면 [Office 365 활동 관리 API](https://docs.microsoft.com/office/office-365-management-api/office-365-management-activity-api-reference)를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="984d8-p101">If your organization is using a security incident and event management (SIEM) server, you can integrate Office 365 Threat Intelligence and Advanced Threat Protection with your SIEM server. SIEM integration enables you to view information, such as malware detected by Office 365 Advanced Protection and Threat Intelligence, in your SIEM server reports. To set up SIEM integration, you use the [Office 365 Activity Management API](https://docs.microsoft.com/office/office-365-management-api/office-365-management-activity-api-reference).</span></span> 

<span data-ttu-id="984d8-p102">office 365 활동 관리 API는 조직의 Office 365 및 Azure Active Directory 활동 로그에서 사용자, 관리자, 시스템 및 정책 작업과 이벤트에 대 한 정보를 검색 합니다. [Office 365 advanced threat protection 및 위협 인텔리전스 스키마](https://docs.microsoft.com/office/office-365-management-api/office-365-management-activity-api-schema#office-365-advanced-threat-protection-and-threat-intelligence-schema) 는 위협 인텔리전스 및/또는 advanced threat protection에서 작동 하므로 조직에서 Advanced threat protection을 사용 하는 경우에는 위협 인텔리전스 또는 그 반대의 경우도 가능 합니다. siem 서버 통합에도 동일한 API를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="984d8-p102">The Office 365 Activity Management API retrieves information about user, admin, system, and policy actions and events from your organization's Office 365 and Azure Active Directory activity logs. The [Office 365 Advanced Threat Protection and Threat Intelligence schema](https://docs.microsoft.com/office/office-365-management-api/office-365-management-activity-api-schema#office-365-advanced-threat-protection-and-threat-intelligence-schema) works with Threat Intelligence and/or Advanced Threat Protection, so if your organization has Advanced Threat Protection but not Threat Intelligence (or vice versa), you can still use that same API for your SIEM server integration.</span></span> 

<span data-ttu-id="984d8-p103">siem 서버 또는 기타 유사한 시스템에서 **감사의 일반적인** 작업을 폴링하여 검색 이벤트에 액세스 해야 합니다. 자세한 내용은 [Office 365 관리 api 시작](https://docs.microsoft.com/office/office-365-management-api/get-started-with-office-365-management-apis)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="984d8-p103">The SIEM server or other similar system should poll the **audit.general** workload to access detection events. To learn more see [Get started with Office 365 Management APIs](https://docs.microsoft.com/office/office-365-management-api/get-started-with-office-365-management-apis).</span></span> 

> [!IMPORTANT]
> <span data-ttu-id="984d8-111">office 365 Advanced Threat Protection과 함께 siem 통합을 설정 하려면 office 365 전역 관리자 이거나 보안 & 준수 센터에 대해 보안 관리자 역할이 할당 되어 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="984d8-111">You must be an Office 365 global administrator or have the security administrator role assigned for the Security & Compliance Center to set up SIEM integration with Office 365 Advanced Threat Protection.</span></span><br/><span data-ttu-id="984d8-p104">Office 365 환경에 대해 감사 로깅을 켜야 합니다. 이에 대 한 도움말을 보려면 [Turn Office 365 감사 로그 검색 설정 또는 해제](turn-audit-log-search-on-or-off.md)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="984d8-p104">Audit logging must be turned on for your Office 365 environment. To get help with this, see [Turn Office 365 audit log search on or off](turn-audit-log-search-on-or-off.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="984d8-114">관련 항목</span><span class="sxs-lookup"><span data-stu-id="984d8-114">Related topics</span></span>

[<span data-ttu-id="984d8-115">Office 365 위협 인텔리전스</span><span class="sxs-lookup"><span data-stu-id="984d8-115">Office 365 Threat Intelligence</span></span>](office-365-ti.md)

[<span data-ttu-id="984d8-116">Office 365 Advanced Threat Protection 방지</span><span class="sxs-lookup"><span data-stu-id="984d8-116">Office 365 Advanced Threat Protection</span></span>](office-365-atp.md)

[<span data-ttu-id="984d8-117">Office 365 보안 &amp; 및 준수 센터의 Smart reports 및 정보</span><span class="sxs-lookup"><span data-stu-id="984d8-117">Smart reports and insights in the Office 365 Security &amp; Compliance Center</span></span>](reports-and-insights-in-security-and-compliance.md)
  
[<span data-ttu-id="984d8-118">Office 365 보안 &amp; 및 준수 센터의 사용 권한</span><span class="sxs-lookup"><span data-stu-id="984d8-118">Permissions in the Office 365 Security &amp; Compliance Center</span></span>](permissions-in-the-security-and-compliance-center.md)
  

