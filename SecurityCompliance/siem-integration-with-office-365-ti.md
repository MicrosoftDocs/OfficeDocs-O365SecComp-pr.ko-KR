---
title: siem과 Office 365 Advanced Threat Protection의 통합
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
description: office 365 활동 관리 API에서 조직의 siem server를 office 365 Advanced Threat Protection 및 관련 위협 이벤트와 통합 합니다.
ms.openlocfilehash: 6c0468f8f3fdd25082bff8a3008d2abf00ed9d4d
ms.sourcegitcommit: 74ad22a5c6c3c9d9324f0f97070909e323a4e9cf
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/11/2019
ms.locfileid: "30523992"
---
# <a name="siem-integration-with-office-365-advanced-threat-protection"></a><span data-ttu-id="e8406-103">siem과 Office 365 Advanced Threat Protection의 통합</span><span class="sxs-lookup"><span data-stu-id="e8406-103">SIEM integration with Office 365 Advanced Threat Protection</span></span>

<span data-ttu-id="e8406-104">조직에서 siem (보안 인시던트 및 이벤트 관리) 서버를 사용 하는 경우 Office 365 Advanced Threat Protection을 siem 서버와 통합할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e8406-104">If your organization is using a security incident and event management (SIEM) server, you can integrate Office 365 Advanced Threat Protection with your SIEM server.</span></span> <span data-ttu-id="e8406-105">siem 통합을 사용 하면 siem server reports에서 Office 365 고급 보호를 통해 검색 된 맬웨어 또는 피싱 같은 정보를 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e8406-105">SIEM integration enables you to view information, such as malware or phish detected by Office 365 Advanced Protection, in your SIEM server reports.</span></span> <span data-ttu-id="e8406-106">siem 통합을 설정 하려면 [Office 365 활동 관리 API](https://docs.microsoft.com/office/office-365-management-api/office-365-management-activity-api-reference)를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8406-106">To set up SIEM integration, you use the [Office 365 Activity Management API](https://docs.microsoft.com/office/office-365-management-api/office-365-management-activity-api-reference).</span></span> 

<span data-ttu-id="e8406-107">office 365 활동 관리 API는 조직의 Office 365 및 Azure Active Directory 활동 로그에서 사용자, 관리자, 시스템 및 정책 작업과 이벤트에 대 한 정보를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8406-107">The Office 365 Activity Management API retrieves information about user, admin, system, and policy actions and events from your organization's Office 365 and Azure Active Directory activity logs.</span></span> <span data-ttu-id="e8406-108">[office 365 advanced threat protection 스키마](https://docs.microsoft.com/office/office-365-management-api/office-365-management-activity-api-schema#office-365-advanced-threat-protection-and-threat-intelligence-schema) 는 advanced threat protection과 함께 작동 하므로 조직에 Office 365 Advanced Threat protection 계획 1 또는 계획 2 또는 Office 365 E5가 있는 경우에도이 API를 사용 하 여 siem 서버 통합에 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e8406-108">The [Office 365 Advanced Threat Protection schema](https://docs.microsoft.com/office/office-365-management-api/office-365-management-activity-api-schema#office-365-advanced-threat-protection-and-threat-intelligence-schema) works with Advanced Threat Protection, so if your organization has the Office 365 Advanced Threat Protection Plan 1 or Plan 2 or Office 365 E5, you can still use that same API for your SIEM server integration.</span></span> 

<span data-ttu-id="e8406-109">siem 서버 또는 기타 유사한 시스템에서 **감사의 일반적인** 작업을 폴링하여 검색 이벤트에 액세스 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8406-109">The SIEM server or other similar system should poll the **audit.general** workload to access detection events.</span></span> <span data-ttu-id="e8406-110">자세한 내용은 [Office 365 관리 api 시작](https://docs.microsoft.com/office/office-365-management-api/get-started-with-office-365-management-apis)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="e8406-110">To learn more see [Get started with Office 365 Management APIs](https://docs.microsoft.com/office/office-365-management-api/get-started-with-office-365-management-apis).</span></span> 

> [!IMPORTANT]
> <span data-ttu-id="e8406-111">office 365 Advanced Threat Protection과 함께 siem 통합을 설정 하려면 office 365 전역 관리자 이거나 보안 & 준수 센터에 대해 보안 관리자 역할이 할당 되어 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8406-111">You must be an Office 365 global administrator or have the security administrator role assigned for the Security & Compliance Center to set up SIEM integration with Office 365 Advanced Threat Protection.</span></span><br/><span data-ttu-id="e8406-112">Office 365 환경에 대해 감사 로깅을 켜야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8406-112">Audit logging must be turned on for your Office 365 environment.</span></span> <span data-ttu-id="e8406-113">이에 대 한 도움말을 보려면 [Turn Office 365 감사 로그 검색 설정 또는 해제](turn-audit-log-search-on-or-off.md)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="e8406-113">To get help with this, see [Turn Office 365 audit log search on or off](turn-audit-log-search-on-or-off.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="e8406-114">관련 항목</span><span class="sxs-lookup"><span data-stu-id="e8406-114">Related topics</span></span>

[<span data-ttu-id="e8406-115">Office 365 위협 조사 및 응답</span><span class="sxs-lookup"><span data-stu-id="e8406-115">Office 365 Threat Investigation and Response</span></span>](office-365-ti.md)

[<span data-ttu-id="e8406-116">Office 365 Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="e8406-116">Office 365 Advanced Threat Protection</span></span>](office-365-atp.md)

[<span data-ttu-id="e8406-117">Office 365 보안 &amp; 및 준수 센터의 Smart reports 및 정보</span><span class="sxs-lookup"><span data-stu-id="e8406-117">Smart reports and insights in the Office 365 Security &amp; Compliance Center</span></span>](reports-and-insights-in-security-and-compliance.md)
  
[<span data-ttu-id="e8406-118">Permissions in the Office 365 Security &amp; Compliance Center</span><span class="sxs-lookup"><span data-stu-id="e8406-118">Permissions in the Office 365 Security &amp; Compliance Center</span></span>](permissions-in-the-security-and-compliance-center.md)
  