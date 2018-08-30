---
title: Office 365에서 사용자 및 관리자 작업에 대 한 감사 로그를 검색 합니다.
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 5/18/2018
ms.audience: Admin
ms.topic: hub-page
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: 57ca5138-0ae0-4d34-bd40-240441ef2fb6
description: Office 365 감사 로그는 통합된 감사 로그 합니다. 통합 된 감사 로그 그 이유? 조직 자신이 대부분의 Office 365 서비스에서 발생 한 이벤트를 구독 하기 때문에 검색할 수 있는 단일 감사 로그에 기록 됩니다. 즉, 사용자 및 이러한 서비스의 관리 작업에 대해 검색할 수 있습니다.
ms.openlocfilehash: 7a6a552b1d2569c9e21fe20b39d474dafc026172
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22533351"
---
# <a name="search-the-audit-log-for-user-and-admin-activity-in-office-365"></a><span data-ttu-id="bd5b2-106">Office 365에서 사용자 및 관리자 작업에 대 한 감사 로그를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="bd5b2-106">Search the audit log for user and admin activity in Office 365</span></span>

<span data-ttu-id="bd5b2-p102">Office 365 감사 로그는 통합된 감사 로그 합니다. 통합 된 감사 로그 그 이유? 조직 자신이 대부분의 Office 365 서비스에서 발생 한 이벤트를 구독 하기 때문에 검색할 수 있는 단일 감사 로그에 기록 됩니다. 즉, 사용자 및 이러한 서비스의 관리 작업에 대해 검색할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bd5b2-p102">The Office 365 audit log is a unified audit log. Why a unified audit log? Because events from most Office 365 services that you're organization subscribes to are recorded in a single audit log that you can search. That means you can search for user and admin activity in these services:</span></span> 
  
- <span data-ttu-id="bd5b2-111">SharePoint</span><span class="sxs-lookup"><span data-stu-id="bd5b2-111">SharePoint</span></span>
- <span data-ttu-id="bd5b2-112">OneDrive</span><span class="sxs-lookup"><span data-stu-id="bd5b2-112">OneDrive</span></span>
- <span data-ttu-id="bd5b2-113">Exchange</span><span class="sxs-lookup"><span data-stu-id="bd5b2-113">Exchange</span></span>
- <span data-ttu-id="bd5b2-114">Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="bd5b2-114">Azure Active Directory</span></span>
- <span data-ttu-id="bd5b2-115">Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="bd5b2-115">Microsoft Teams</span></span>
- <span data-ttu-id="bd5b2-116">eDiscovery</span><span class="sxs-lookup"><span data-stu-id="bd5b2-116">eDiscovery</span></span>
- <span data-ttu-id="bd5b2-117">Power BI</span><span class="sxs-lookup"><span data-stu-id="bd5b2-117">Power BI</span></span>
- <span data-ttu-id="bd5b2-118">Yammer</span><span class="sxs-lookup"><span data-stu-id="bd5b2-118">Yammer</span></span>
- <span data-ttu-id="bd5b2-119">Sway</span><span class="sxs-lookup"><span data-stu-id="bd5b2-119">Sway</span></span>
- <span data-ttu-id="bd5b2-120">Microsoft Stream</span><span class="sxs-lookup"><span data-stu-id="bd5b2-120">Microsoft Stream</span></span>
   
 ## <a name="set-up-auditing"></a><span data-ttu-id="bd5b2-121">감사 설정</span><span class="sxs-lookup"><span data-stu-id="bd5b2-121">Set up auditing</span></span>
  
<span data-ttu-id="bd5b2-122">Office 365 감사 로그를 검색 하기 전에 수행 해야할 사항 방법이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bd5b2-122">There's few things you have to do before you can search the Office 365 audit log.</span></span>
  
- <span data-ttu-id="bd5b2-123">[감사 로그 검색 켜기](turn-audit-log-search-on-or-off.md) 를 검색할 수 있는 녹음/녹화 이벤트를 시작 하려면</span><span class="sxs-lookup"><span data-stu-id="bd5b2-123">[Turn on audit log search](turn-audit-log-search-on-or-off.md) to start recording events that you can search for</span></span> 
    
- <span data-ttu-id="bd5b2-124">사서함과 관련 된 이벤트를 검색할 수 있도록 [사서함 감사 활성화](enable-mailbox-auditing.md) 때 사용자가 로그인 자신의 사서함 이나 제거 항목에 해당 복구 가능한 항목 폴더에서 같은</span><span class="sxs-lookup"><span data-stu-id="bd5b2-124">[Enable mailbox auditing](enable-mailbox-auditing.md) so you can search for mailbox-related events; such as when a user signs in to their mailbox or purges items from their Recoverable Items folder</span></span> 
    
 ## <a name="search-the-audit-log"></a><span data-ttu-id="bd5b2-125">감사 로그 검색</span><span class="sxs-lookup"><span data-stu-id="bd5b2-125">Search the audit log</span></span>
  
<span data-ttu-id="bd5b2-126">감사를 설정한 후 수백 개의 개별 유형의 여러 Office 365 서비스에서 발생 한 이벤트에 대 한 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="bd5b2-126">After you turn on auditing, you search for hundreds of individual types of events from multiple Office 365 services.</span></span>
  
- <span data-ttu-id="bd5b2-127">사용자 및 관리자 작업에 대 한 [감사 로그 검색](search-the-audit-log-in-security-and-compliance.md)</span><span class="sxs-lookup"><span data-stu-id="bd5b2-127">[Search the audit log](search-the-audit-log-in-security-and-compliance.md) for user and admin activities</span></span> 
    
- <span data-ttu-id="bd5b2-128">검색 결과에 포함 된 각 감사 레코드의 [자세한 속성을 이해](detailed-properties-in-the-office-365-audit-log.md)</span><span class="sxs-lookup"><span data-stu-id="bd5b2-128">[Understand the detailed properties](detailed-properties-in-the-office-365-audit-log.md) in each auditing record included in the search results</span></span> 
    
- <span data-ttu-id="bd5b2-129">관리자 및 규정 준수 관리자에 의해 수행 되는 [eDiscovery 관련 작업을 수행에 대 한 검색](search-for-ediscovery-activities-in-the-audit-log.md)</span><span class="sxs-lookup"><span data-stu-id="bd5b2-129">[Search for eDiscovery-related activities](search-for-ediscovery-activities-in-the-audit-log.md) performed by admins and compliance managers</span></span> 
