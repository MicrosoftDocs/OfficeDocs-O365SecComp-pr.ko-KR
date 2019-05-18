---
title: Office 365에서 사용자 및 관리 활동에 대 한 감사 로그 검색
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 5/18/2018
audience: Admin
ms.topic: hub-page
ms.service: O365-seccomp
localization_priority: Normal
ROBOTS: NOINDEX, NOFOLLOW
search.appverid: MOE150
ms.assetid: 57ca5138-0ae0-4d34-bd40-240441ef2fb6
description: Office 365 감사 로그는 통합 된 감사 로그입니다. 통합 감사 로그가 왜 있나요? 조직에서 구독 하는 대부분의 Office 365 서비스에서 발생 한 이벤트는 검색할 수 있는 단일 감사 로그에 기록 됩니다. 즉, 다음 서비스에서 사용자 및 관리자 활동을 검색할 수 있습니다.
ms.openlocfilehash: 1d3f45d24a8d1a83c20f5d36b12ced761e00f936
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/17/2019
ms.locfileid: "34158780"
---
# <a name="search-the-audit-log-for-user-and-admin-activity-in-office-365"></a><span data-ttu-id="69c82-106">Office 365에서 사용자 및 관리 활동에 대 한 감사 로그 검색</span><span class="sxs-lookup"><span data-stu-id="69c82-106">Search the audit log for user and admin activity in Office 365</span></span>

<span data-ttu-id="69c82-107">Office 365 감사 로그는 통합 된 감사 로그입니다.</span><span class="sxs-lookup"><span data-stu-id="69c82-107">The Office 365 audit log is a unified audit log.</span></span> <span data-ttu-id="69c82-108">통합 감사 로그가 왜 있나요?</span><span class="sxs-lookup"><span data-stu-id="69c82-108">Why a unified audit log?</span></span> <span data-ttu-id="69c82-109">조직에서 구독 하는 대부분의 Office 365 서비스에서 발생 한 이벤트는 검색할 수 있는 단일 감사 로그에 기록 됩니다.</span><span class="sxs-lookup"><span data-stu-id="69c82-109">Because events from most Office 365 services that you're organization subscribes to are recorded in a single audit log that you can search.</span></span> <span data-ttu-id="69c82-110">즉, 다음 서비스에서 사용자 및 관리자 활동을 검색할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="69c82-110">That means you can search for user and admin activity in these services:</span></span> 
  
- <span data-ttu-id="69c82-111">SharePoint</span><span class="sxs-lookup"><span data-stu-id="69c82-111">SharePoint</span></span>
- <span data-ttu-id="69c82-112">OneDrive</span><span class="sxs-lookup"><span data-stu-id="69c82-112">OneDrive</span></span>
- <span data-ttu-id="69c82-113">Exchange</span><span class="sxs-lookup"><span data-stu-id="69c82-113">Exchange</span></span>
- <span data-ttu-id="69c82-114">Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="69c82-114">Azure Active Directory</span></span>
- <span data-ttu-id="69c82-115">Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="69c82-115">Microsoft Teams</span></span>
- <span data-ttu-id="69c82-116">eDiscovery</span><span class="sxs-lookup"><span data-stu-id="69c82-116">eDiscovery</span></span>
- <span data-ttu-id="69c82-117">Power BI</span><span class="sxs-lookup"><span data-stu-id="69c82-117">Power BI</span></span>
- <span data-ttu-id="69c82-118">Yammer</span><span class="sxs-lookup"><span data-stu-id="69c82-118">Yammer</span></span>
- <span data-ttu-id="69c82-119">Sway</span><span class="sxs-lookup"><span data-stu-id="69c82-119">Sway</span></span>
- <span data-ttu-id="69c82-120">Microsoft Stream</span><span class="sxs-lookup"><span data-stu-id="69c82-120">Microsoft Stream</span></span>
   
 ## <a name="set-up-auditing"></a><span data-ttu-id="69c82-121">감사 설정</span><span class="sxs-lookup"><span data-stu-id="69c82-121">Set up auditing</span></span>
  
<span data-ttu-id="69c82-122">Office 365 감사 로그를 검색 하려면 몇 가지 작업을 수행 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="69c82-122">There's few things you have to do before you can search the Office 365 audit log.</span></span>
  
- <span data-ttu-id="69c82-123">검색할 수 있는 이벤트 기록을 시작 하려면 [감사 로그 검색 켜기를 설정](turn-audit-log-search-on-or-off.md) 합니다.</span><span class="sxs-lookup"><span data-stu-id="69c82-123">[Turn on audit log search](turn-audit-log-search-on-or-off.md) to start recording events that you can search for</span></span> 
    
- <span data-ttu-id="69c82-124">사서함 관련 이벤트를 검색할 수 있도록 [사서함 감사를 사용 하도록 설정](enable-mailbox-auditing.md) 합니다. 사용자가 사서함에 로그인 하거나 복구 가능한 항목 폴더에서 항목을 제거 하는 경우와 같이</span><span class="sxs-lookup"><span data-stu-id="69c82-124">[Enable mailbox auditing](enable-mailbox-auditing.md) so you can search for mailbox-related events; such as when a user signs in to their mailbox or purges items from their Recoverable Items folder</span></span> 
    
 ## <a name="search-the-audit-log"></a><span data-ttu-id="69c82-125">감사 로그 검색</span><span class="sxs-lookup"><span data-stu-id="69c82-125">Search the audit log</span></span>
  
<span data-ttu-id="69c82-126">감사를 설정한 후에는 여러 Office 365 서비스에서 수백 개의 개별 이벤트 유형을 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="69c82-126">After you turn on auditing, you search for hundreds of individual types of events from multiple Office 365 services.</span></span>
  
- <span data-ttu-id="69c82-127">사용자 및 관리 작업에 대 한 [감사 로그 검색](search-the-audit-log-in-security-and-compliance.md)</span><span class="sxs-lookup"><span data-stu-id="69c82-127">[Search the audit log](search-the-audit-log-in-security-and-compliance.md) for user and admin activities</span></span> 
    
- <span data-ttu-id="69c82-128">검색 결과에 포함 된 각 감사 레코드의 [자세한 속성 이해](detailed-properties-in-the-office-365-audit-log.md)</span><span class="sxs-lookup"><span data-stu-id="69c82-128">[Understand the detailed properties](detailed-properties-in-the-office-365-audit-log.md) in each auditing record included in the search results</span></span> 
    
- <span data-ttu-id="69c82-129">관리자 및 준수 관리자가 수행한 [eDiscovery 관련 활동 검색](search-for-ediscovery-activities-in-the-audit-log.md)</span><span class="sxs-lookup"><span data-stu-id="69c82-129">[Search for eDiscovery-related activities](search-for-ediscovery-activities-in-the-audit-log.md) performed by admins and compliance managers</span></span> 
