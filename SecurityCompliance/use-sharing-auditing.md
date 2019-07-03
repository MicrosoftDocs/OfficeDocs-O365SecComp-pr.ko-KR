---
title: 외부 사용자와 공유된 리소스를 찾기 위한 감사 공유
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- SPO160
- MOE150
- BCS160
- MET150
ms.assetid: 50bbf89f-7870-4c2a-ae14-42635e0cfc01
description: '공유는 SharePoint Online 및 비즈니스용 OneDrive의 주요 활동입니다. 이제 관리자는 Office 365 감사 로그의 공유 감사를 사용 하 여 조직에서 공유가 사용 되는 방식을 확인할 수 있습니다. '
ms.openlocfilehash: e2865d35e988d8c0e42a6c51f78507db8b170d4c
ms.sourcegitcommit: b262d40f6daf06be26e7586f37b736e09f8a4511
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/02/2019
ms.locfileid: "35435245"
---
# <a name="use-sharing-auditing-in-the-office-365-audit-log"></a><span data-ttu-id="3d1f2-104">외부 사용자와 공유된 리소스를 찾기 위한 감사 공유</span><span class="sxs-lookup"><span data-stu-id="3d1f2-104">Use sharing auditing in the Office 365 audit log</span></span>

<span data-ttu-id="3d1f2-105">공유는 SharePoint Online 및 비즈니스용 OneDrive의 주요 활동 이며, Office 365 조직에서 널리 사용 되 고 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3d1f2-105">Sharing is a key activity in SharePoint Online and OneDrive for Business, and it's widely used in Office 365 organizations.</span></span> <span data-ttu-id="3d1f2-106">이제 관리자는 Office 365 감사 로그의 공유 감사를 사용 하 여 조직에서 공유가 사용 되는 방식을 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3d1f2-106">Administrators can now use sharing auditing in the Office 365 audit log to determine how sharing is being used in their organization.</span></span> 
  
## <a name="the-sharepoint-sharing-schema"></a><span data-ttu-id="3d1f2-107">SharePoint 공유 스키마</span><span class="sxs-lookup"><span data-stu-id="3d1f2-107">The SharePoint Sharing schema</span></span>

<span data-ttu-id="3d1f2-108">공유 정책 및 공유 링크 이벤트를 제외 하 고 이벤트 공유가 파일 및 폴더 관련 이벤트와는 다른 사용자에 게 영향을 주는 한 가지 기본 방법으로 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="3d1f2-108">Sharing events (excluding sharing policy and sharing link events) are different from file- and folder-related events in one primary way: one user is taking an action that has some effect on another user.</span></span> <span data-ttu-id="3d1f2-109">예를 들어 User A는 사용자 B에 게 파일에 대 한 액세스 권한을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d1f2-109">For example, User A gives User B access to a file.</span></span> <span data-ttu-id="3d1f2-110">이 예에서는 사용자 A가 작업 중인 *사용자* 이 고 사용자 B가 *대상 사용자*입니다.</span><span class="sxs-lookup"><span data-stu-id="3d1f2-110">In this example, User A is the  *acting user*  and User B is the  *target user*.</span></span> <span data-ttu-id="3d1f2-111">SharePoint 파일 스키마에서 작동 중인 사용자의 작업은 파일 자체에만 영향을 줍니다.</span><span class="sxs-lookup"><span data-stu-id="3d1f2-111">In the SharePoint File schema, the acting user's action only affects the file itself.</span></span> <span data-ttu-id="3d1f2-112">사용자 A가 파일을 여는 경우, **Fileaccessed** 한 이벤트에서 필요한 정보는 작업 중인 사용자입니다.</span><span class="sxs-lookup"><span data-stu-id="3d1f2-112">When User A opens a file, the only information needed in the **FileAccessed** event is the acting user.</span></span> <span data-ttu-id="3d1f2-113">이러한 차이를 해결 하기 위해 *SharePoint 공유 스키마*라고 하는 별도의 스키마를 통해 공유 이벤트에 대 한 추가 정보를 캡처할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3d1f2-113">To address this difference, there is a separate schema, called the  *SharePoint Sharing schema*, that captures more information about sharing events.</span></span> <span data-ttu-id="3d1f2-114">이렇게 하면 관리자가 리소스를 공유 하는 사람 및 리소스를 공유한 사용자에 대 한 자세한 정보를 파악할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3d1f2-114">This ensures that administrators have more insight into who shared a resource and the user the resource was shared with.</span></span> 
  
<span data-ttu-id="3d1f2-115">공유 스키마는 감사 로그에서 공유 이벤트와 관련 된 두 가지 추가 필드를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d1f2-115">The Sharing schema provides two additional fields in the audit log related to sharing events:</span></span> 
  
- <span data-ttu-id="3d1f2-116">**Targetuserorgroupname** – 리소스가 공유 된 대상 사용자 또는 그룹의 UPN 이나 이름을 저장 합니다 (이전 예제에서는 user B).</span><span class="sxs-lookup"><span data-stu-id="3d1f2-116">**TargetUserOrGroupName** – Stores the UPN or name of the target user or group that a resource was shared with (User B in the previous example).</span></span> 
    
- <span data-ttu-id="3d1f2-117">**TargetUserOrGroupType** – 대상 사용자 또는 그룹이 구성원, 게스트, 그룹 또는 파트너 인지 여부를 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d1f2-117">**TargetUserOrGroupType** – Identifies whether the target user or group is a Member, Guest, Group, or Partner.</span></span> 
    
<span data-ttu-id="3d1f2-118">이러한 두 필드는 사용자, 작업 및 날짜와 같은 Office 365 감사 로그 스키마의 다른 속성 외에, *누가 누구* 에 게 *어떤* 리소스를 공유 \*\* 하는지를 알려 줄 수 있습니다. \*\*</span><span class="sxs-lookup"><span data-stu-id="3d1f2-118">These two fields, in addition to other properties from the Office 365 audit log schema such as User, Operation, and Date can tell the full story about  *which*  user shared  *what*  resource with  *whom*  and  *when*.</span></span> 
  
<span data-ttu-id="3d1f2-119">공유 스토리에 중요 한 또 다른 스키마 속성이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3d1f2-119">There's another schema property that's important to the sharing story.</span></span> <span data-ttu-id="3d1f2-120">**EventData** 속성은 공유 이벤트에 대 한 추가 정보를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d1f2-120">The **EventData** property stores additional information about sharing events.</span></span> <span data-ttu-id="3d1f2-121">예를 들어 사용자가 다른 사용자와 사이트를 공유 하는 경우이 작업을 수행 하려면 SharePoint 그룹에 대상 사용자를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d1f2-121">For example, when a user shares a site with another user, this is accomplished by adding the target user to a SharePoint group.</span></span> <span data-ttu-id="3d1f2-122">**EventData** 속성은이 추가 정보를 캡처하여 관리자에 게 컨텍스트를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d1f2-122">The **EventData** property captures this additional information to provide context for administrators.</span></span> 

## <a name="the-sharepoint-sharing-model-and-sharing-events"></a><span data-ttu-id="3d1f2-123">SharePoint 공유 모델 및 공유 이벤트</span><span class="sxs-lookup"><span data-stu-id="3d1f2-123">The SharePoint Sharing model and sharing events</span></span>

<span data-ttu-id="3d1f2-124">공유는 세 가지 별도 이벤트 인 **SharingSet**, **SharingInvitationCreated**및 **SharingInvitaitonAccepted**로 정의 됩니다.</span><span class="sxs-lookup"><span data-stu-id="3d1f2-124">Sharing is defined by three separate events: **SharingSet**, **SharingInvitationCreated**, and **SharingInvitaitonAccepted**.</span></span> <span data-ttu-id="3d1f2-125">다음은 공유 이벤트가 Office 365 감사 로그에 기록 되는 방식에 대 한 워크플로입니다.</span><span class="sxs-lookup"><span data-stu-id="3d1f2-125">Here's the work flow for how sharing events are logged in the Office 365 audit log.</span></span> 
  
![공유 감사가 작동 하는 방식에 대 한 순서도](media/d83dd40f-919b-484f-bfd6-5dc8de31bff6.png)
  
<span data-ttu-id="3d1f2-127">사용자 (작업 중인 사용자)가 다른 사용자 (대상 사용자)와 리소스를 공유 하려는 경우 먼저 SharePoint (또는 비즈니스용 OneDrive)가 대상 사용자의 전자 메일 주소가 조직의 디렉터리에 있는 사용자 계정과 이미 연결 되어 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d1f2-127">When a user (the acting user) wants to share a resource with another user (the target user), SharePoint (or OneDrive for Business) first checks if the email address of the target user is already associated with a user account in the organization's directory.</span></span> <span data-ttu-id="3d1f2-128">대상 사용자가 조직의 디렉터리에 있는 경우 SharePoint는 다음을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d1f2-128">If the target user is in the organization's directory, SharePoint does the following:</span></span>
  
-  <span data-ttu-id="3d1f2-129">리소스에 액세스할 수 있는 대상 사용자 권한을 즉시 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d1f2-129">Immediately assigns the target user permissions to access the resource.</span></span> 
    
- <span data-ttu-id="3d1f2-130">대상 사용자의 전자 메일 주소로 공유 알림을 보냅니다.</span><span class="sxs-lookup"><span data-stu-id="3d1f2-130">Sends a sharing notification to the email address of the target user.</span></span>
    
- <span data-ttu-id="3d1f2-131">**SharingSet** 이벤트를 기록 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d1f2-131">Logs a **SharingSet** event.</span></span> 
    
 <span data-ttu-id="3d1f2-132">대상 사용자에 대 한 사용자 계정이 조직의 디렉터리에 없으면 SharePoint는 다음을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d1f2-132">If a user account for the target user isn't in the organization's directory, SharePoint does the following:</span></span> 
  
- <span data-ttu-id="3d1f2-133">공유 초대를 만들어 대상 사용자의 전자 메일 주소로 보냅니다.</span><span class="sxs-lookup"><span data-stu-id="3d1f2-133">Creates a sharing invitation and sends it to the email address of the target user.</span></span>
    
- <span data-ttu-id="3d1f2-134">**SharingInvitationCreated** 이벤트를 기록 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d1f2-134">Logs a **SharingInvitationCreated** event.</span></span> 
    
    > [!NOTE]
    > <span data-ttu-id="3d1f2-135">**SharingInvitationCreated** 이벤트는 대상 사용자가 공유 된 리소스에 액세스할 수 없는 경우 항상 외부 또는 게스트 공유와 연결 됩니다.</span><span class="sxs-lookup"><span data-stu-id="3d1f2-135">The **SharingInvitationCreated** event is most always associated with external or guest sharing when the target user doesn't have access to the resource that was shared.</span></span> 
  
<span data-ttu-id="3d1f2-136">대상 사용자가 초대의 링크를 클릭 하 여 전송 된 공유 초대를 수락 하면 SharePoint에서 **SharingInvitationAccepted** 이벤트를 기록 하 고 리소스에 액세스 하기 위한 대상 사용자 권한을 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d1f2-136">When the target user accepts the sharing invitation that's sent to them (by clicking the link in the invitation), SharePoint logs a **SharingInvitationAccepted** event and assigns the target user permissions to access the resource.</span></span> <span data-ttu-id="3d1f2-137">초대를 보낸 사용자의 id와 실제로 초대를 수락한 사용자에 대 한 정보를 비롯 하 여 대상 사용자에 대 한 추가 정보도 기록 됩니다.</span><span class="sxs-lookup"><span data-stu-id="3d1f2-137">Additional information about the target user is also logged, such as the identity of the user that the invitation was sent to and the user who actually accepted the invitation.</span></span> <span data-ttu-id="3d1f2-138">경우에 따라 이러한 사용자 (또는 전자 메일 주소)는 다를 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3d1f2-138">In some case, these users (or email addresses) might be different.</span></span> 
  

  
## <a name="how-to-identify-resources-shared-with-external-users"></a><span data-ttu-id="3d1f2-139">외부 사용자와 공유 된 리소스를 확인 하는 방법</span><span class="sxs-lookup"><span data-stu-id="3d1f2-139">How to identify resources shared with external users</span></span>

<span data-ttu-id="3d1f2-140">관리자에 대 한 일반적인 요구 사항에는 조직 외부의 사용자와 공유 된 모든 리소스의 목록이 작성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="3d1f2-140">A common requirement for administrators is creating a list of all resources that have been shared with users outside of the organization.</span></span> <span data-ttu-id="3d1f2-141">이제 관리자는 Office 365의 공유 감사를 사용 하 여이 목록을 생성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3d1f2-141">By using sharing auditing in Office 365, administrators can now generate this list.</span></span> <span data-ttu-id="3d1f2-142">이 작업을 수행하는 방법은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="3d1f2-142">Here's how.</span></span>
  
### <a name="step-1-search-for-sharing-events-and-export-the-results-to-a-csv-file"></a><span data-ttu-id="3d1f2-143">1 단계: 공유 이벤트 검색 및 결과를 CSV 파일로 내보내기</span><span class="sxs-lookup"><span data-stu-id="3d1f2-143">Step 1: Search for sharing events and export the results to a CSV file</span></span>

<span data-ttu-id="3d1f2-144">첫 번째 단계는 공유 이벤트에 대 한 Office 365 감사 로그를 검색 하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="3d1f2-144">The first step is to search the Office 365 audit log for sharing events.</span></span> <span data-ttu-id="3d1f2-145">감사 로그 검색에 대 한 자세한 내용 (필요한 권한 포함)은 [Security & 준수 센터에서 감사 로그 검색](search-the-audit-log-in-security-and-compliance.md)을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="3d1f2-145">For more information (including the required permissions) about searching the audit log, see [Search the audit log in the Security & Compliance Center](search-the-audit-log-in-security-and-compliance.md).</span></span>
  
1. <span data-ttu-id="3d1f2-146">[https://protection.office.com](https://protection.office.com)으로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="3d1f2-146">Go to [https://protection.office.com](https://protection.office.com).</span></span>
    
2. <span data-ttu-id="3d1f2-147">회사 또는 학교 계정을 사용하여 Office 365에 로그인합니다.</span><span class="sxs-lookup"><span data-stu-id="3d1f2-147">Sign in to Office 365 using your work or school account.</span></span>
    
3. <span data-ttu-id="3d1f2-148">보안 & 준수 센터의 왼쪽 창에서 **검색**  > **감사 로그 검색**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d1f2-148">In the left pane of the Security & Compliance Center, click **Search**  > **Audit log search**.</span></span>
    
    <span data-ttu-id="3d1f2-149">**감사 로그 검색** 페이지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="3d1f2-149">The **Audit log search** page is displayed.</span></span> 
    
4. <span data-ttu-id="3d1f2-150">**활동**아래에서 **공유 및 액세스 요청 활동** 을 클릭 하 여 공유 관련 이벤트를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d1f2-150">Under **Activities**, click **Sharing and access request activities** to search for sharing-related events.</span></span> 
    
    ![활동 아래에서 공유 및 액세스 요청 작업을 선택 합니다.](media/46bb25b7-1eb2-4adf-903a-cc9ab58639f9.png)
  
5.  <span data-ttu-id="3d1f2-152">날짜 및 시간 범위를 선택 하 여 해당 기간 내에 발생 한 공유 이벤트를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="3d1f2-152">Select a date and time range to find the sharing events that occurred within that period.</span></span> 
    
6. <span data-ttu-id="3d1f2-153">검색 \*\*\*\* 을 클릭 하 여 검색을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d1f2-153">Click **Search** to run the search.</span></span> 
    
7. <span data-ttu-id="3d1f2-154">검색 실행이 완료 되 고 결과가 표시 되 면 결과 **내보내기** \> **모든 결과 다운로드**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d1f2-154">When the search is finished running and the results are displayed, click **Export results** \> **Download all results**.</span></span>
    
    <span data-ttu-id="3d1f2-155">내보내기 옵션을 선택한 후에는 CSV 파일을 열거나 저장 하 라는 메시지가 창 맨 아래에 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="3d1f2-155">After you select the export option, a message is displayed at the bottom of the window that prompts you to open or save the CSV file.</span></span>
    
8. <span data-ttu-id="3d1f2-156">다른 \*\*\*\* \> **이름으로 저장** 저장을 클릭 하 고 로컬 컴퓨터의 폴더에 CSV 파일을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d1f2-156">Click **Save** \> **Save as** and save the CSV file to a folder on your local computer.</span></span> 

### <a name="step-2-filter-the-csv-file-for-resources-shared-with-external-users"></a><span data-ttu-id="3d1f2-157">2 단계: 외부 사용자와 공유 되는 리소스에 대 한 CSV 파일 필터링</span><span class="sxs-lookup"><span data-stu-id="3d1f2-157">Step 2: Filter the CSV file for resources shared with external users</span></span>

<span data-ttu-id="3d1f2-158">다음 단계는 **SharingSet** 및 **SharingInvitationCreated** 이벤트에 대 한 CSV를 필터링 하 고 **TargetUserOrGroupType** 속성이 **Guest**인 이벤트를 표시 하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="3d1f2-158">The next step is to filter the CSV for the **SharingSet** and **SharingInvitationCreated** events, and to display those events where the **TargetUserOrGroupType** property is **Guest**.</span></span> <span data-ttu-id="3d1f2-159">Excel에서 파워 쿼리 편집기 도구를 사용 하 여이 작업을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d1f2-159">You use the Power Query Editor tool in Excel to do this.</span></span> <span data-ttu-id="3d1f2-160">단계별 지침은 [Export, configure 및 view audit log records](export-view-audit-log-records.md)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="3d1f2-160">For step-by-step instructions, see [Export, configure, and view audit log records](export-view-audit-log-records.md).</span></span> 

<span data-ttu-id="3d1f2-161">이전 항목의 지침에 따라 CSV 파일을 준비한 후에는 다음을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d1f2-161">After you've followed the instructions in the previous topic to prepare the CSV file, do the following:</span></span>
    
1. <span data-ttu-id="3d1f2-162">파워 쿼리 편집기로 준비한 CSV 파일을 엽니다.</span><span class="sxs-lookup"><span data-stu-id="3d1f2-162">Open the CSV file that you prepared with the Power Query Editor.</span></span> 

2. <span data-ttu-id="3d1f2-163">**홈** 탭에서 **정렬 & 필터**를 클릭 하 고 **필터**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d1f2-163">On the **Home** tab, click **Sort & Filter**, and then click **Filter**.</span></span>
    
3. <span data-ttu-id="3d1f2-164">**작업** 열의 **정렬 & 필터** 드롭다운 목록에서 모든 선택을 취소 하 고 **SharingSet** 및 **SharingInvitationCreated**을 선택한 후 **확인**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d1f2-164">In the **Sort & Filter** dropdown list on the **Operations** column, clear all selections, then select **SharingSet** and **SharingInvitationCreated**, and click **OK**.</span></span>
    
    <span data-ttu-id="3d1f2-165">Excel에 **SharingSet** 및 **SharingInvitationCreated** 이벤트에 대 한 행이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="3d1f2-165">Excel displays the rows for the **SharingSet** and **SharingInvitationCreated** events.</span></span> 
    
4. <span data-ttu-id="3d1f2-166">**TargetUserOrGroupType** 라는 열로 이동 하 여 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d1f2-166">Go to the column named **TargetUserOrGroupType** and select it.</span></span> 
    
5. <span data-ttu-id="3d1f2-167">**정렬 & 필터** 드롭다운 목록에서 모든 선택을 취소 하 고 **TargetUserOrGroupType: Guest**를 선택한 다음 **확인**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d1f2-167">In the **Sort & Filter** dropdown list, clear all selections, then select **TargetUserOrGroupType:Guest**, and click **OK**.</span></span>
    
    <span data-ttu-id="3d1f2-168">이제 외부 사용자는 **TargetUserOrGroupType: Guest**값으로 식별 되므로 **SharingInvitationCreated** 및 **SharingSet** 이벤트와 대상 사용자가 조직 외부에 있는 위치에 대 한 행이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="3d1f2-168">Now Excel displays the rows for **SharingInvitationCreated** and **SharingSet** events AND where the target user is outside of your organization, because external users are identified by the value **TargetUserOrGroupType:Guest**.</span></span> 
    
<span data-ttu-id="3d1f2-169">다음 표에는 지정 된 날짜 범위 내에서 게스트 사용자와 리소스를 공유 하는 조직의 모든 사용자가 나와 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3d1f2-169">The following table shows all users in the organization who shared resources with a guest user within a specified date range.</span></span>
  
![Office 365 감사 로그에서 이벤트 공유](media/0e0ecbe3-c794-4ca6-a2ca-63478fb3bb34.png)
  
<span data-ttu-id="3d1f2-171">**ObjectId** 속성은 이전 표에 포함 되어 있지 않지만 대상 사용자와 공유 된 리소스를 식별 합니다. 예를 `ObjectId:https:\/\/contoso-my.sharepoint.com\/personal\/sarad_contoso_com\/Documents\/Southwater Proposal.docx`들어</span><span class="sxs-lookup"><span data-stu-id="3d1f2-171">Although it's not included in the previous table, the **ObjectId** property identifies the resource that was shared with the target user; for example  `ObjectId:https:\/\/contoso-my.sharepoint.com\/personal\/sarad_contoso_com\/Documents\/Southwater Proposal.docx`.</span></span>
  
> [!TIP]
> <span data-ttu-id="3d1f2-172">게스트 사용자에 게 실제로 리소스에 액세스 하기 위한 사용 권한이 할당 된 시간을 확인 하려면 (이러한 리소스와 공유 하는 리소스만 해당) 2, 3, 4 단계를 반복 하 고 **SharingInvitationAccepted** 및 **SharingSet** 의 필터를 적용 합니다. 5 단계의 이벤트</span><span class="sxs-lookup"><span data-stu-id="3d1f2-172">If you want to identify when a guest user was actually assigned permissions to access a resource (as opposed to just the resources that where shared with them), repeat Steps 2, 3, and 4, and filter on the **SharingInvitationAccepted** and **SharingSet** events in Step 5.</span></span> 
