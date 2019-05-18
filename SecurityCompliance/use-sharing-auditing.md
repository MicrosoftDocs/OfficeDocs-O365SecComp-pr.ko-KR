---
title: 외부 사용자와 공유된 리소스를 찾기 위한 감사 공유
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 2/13/2018
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
ms.openlocfilehash: a363ebe2e8b1697521ab5f84df0b3fc221a2abcd
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/17/2019
ms.locfileid: "34157900"
---
# <a name="use-sharing-auditing-in-the-office-365-audit-log"></a><span data-ttu-id="6eda6-104">외부 사용자와 공유된 리소스를 찾기 위한 감사 공유</span><span class="sxs-lookup"><span data-stu-id="6eda6-104">Use sharing auditing in the Office 365 audit log</span></span>

<span data-ttu-id="6eda6-105">공유는 SharePoint Online 및 비즈니스용 OneDrive의 주요 활동 이며, Office 365 조직에서 널리 사용 되 고 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6eda6-105">Sharing is a key activity in SharePoint Online and OneDrive for Business, and it's widely used in Office 365 organizations.</span></span> <span data-ttu-id="6eda6-106">이제 관리자는 Office 365 감사 로그의 공유 감사를 사용 하 여 조직에서 공유가 사용 되는 방식을 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6eda6-106">Administrators can now use sharing auditing in the Office 365 audit log to determine how sharing is being used in their organization.</span></span> 
  
## <a name="the-sharepoint-sharing-schema"></a><span data-ttu-id="6eda6-107">SharePoint 공유 스키마</span><span class="sxs-lookup"><span data-stu-id="6eda6-107">The SharePoint Sharing schema</span></span>

<span data-ttu-id="6eda6-108">공유 정책 및 공유 링크 이벤트를 제외 하 고 이벤트 공유가 파일 및 폴더 관련 이벤트와는 다른 사용자에 게 영향을 주는 한 가지 기본 방법으로 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6eda6-108">Sharing events (excluding sharing policy and sharing link events) are different from file- and folder-related events in one primary way: one user is taking an action that has some effect on another user.</span></span> <span data-ttu-id="6eda6-109">예를 들어 User A는 사용자 B에 게 파일에 대 한 액세스 권한을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="6eda6-109">For example, User A gives User B access to a file.</span></span> <span data-ttu-id="6eda6-110">이 예에서는 사용자 A가 작업 중인 *사용자* 이 고 사용자 B가 *대상 사용자*입니다.</span><span class="sxs-lookup"><span data-stu-id="6eda6-110">In this example, User A is the  *acting user*  and User B is the  *target user*.</span></span> <span data-ttu-id="6eda6-111">SharePoint 파일 스키마에서 작동 중인 사용자의 작업은 파일 자체에만 영향을 줍니다.</span><span class="sxs-lookup"><span data-stu-id="6eda6-111">In the SharePoint File schema, the acting user's action only affects the file itself.</span></span> <span data-ttu-id="6eda6-112">사용자 A가 파일을 여는 경우, **Fileaccessed** 한 이벤트에서 필요한 정보는 작업 중인 사용자입니다.</span><span class="sxs-lookup"><span data-stu-id="6eda6-112">When User A opens a file, the only information needed in the **FileAccessed** event is the acting user.</span></span> <span data-ttu-id="6eda6-113">이러한 차이를 해결 하기 위해 *SharePoint 공유 스키마*라고 하는 별도의 스키마를 통해 공유 이벤트에 대 한 추가 정보를 캡처할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6eda6-113">To address this difference, there is a separate schema, called the  *SharePoint Sharing schema*, that captures more information about sharing events.</span></span> <span data-ttu-id="6eda6-114">이렇게 하면 관리자가 리소스를 공유 하는 사람 및 리소스를 공유한 사용자에 대 한 자세한 정보를 파악할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6eda6-114">This ensures that administrators have more insight into who shared a resource and the user the resource was shared with.</span></span> 
  
<span data-ttu-id="6eda6-115">공유 스키마는 감사 로그에서 공유 이벤트와 관련 된 두 가지 추가 필드를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="6eda6-115">The Sharing schema provides two additional fields in the audit log related to sharing events:</span></span> 
  
- <span data-ttu-id="6eda6-116">**Targetuserorgroupname** -리소스를 공유 하는 대상 사용자 또는 그룹의 UPN 이나 이름을 저장 합니다 (이전 예제에서는 user B).</span><span class="sxs-lookup"><span data-stu-id="6eda6-116">**TargetUserOrGroupName** - Stores the UPN or name of the target user or group that a resource was shared with (User B in the previous example).</span></span> 
    
- <span data-ttu-id="6eda6-117">**TargetUserOrGroupType** -대상 사용자 또는 그룹이 구성원, 게스트, 그룹 또는 파트너 인지를 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="6eda6-117">**TargetUserOrGroupType** - Identifies whether the target user or group is a Member, Guest, Group, or Partner.</span></span> 
    
<span data-ttu-id="6eda6-118">이러한 두 필드는 사용자, 작업 및 날짜와 같은 Office 365 감사 로그 스키마의 다른 속성 외에, *누가 누구* 에 게 *어떤* 리소스를 공유 \*\* 하는지를 알려 줄 수 있습니다. \*\*</span><span class="sxs-lookup"><span data-stu-id="6eda6-118">These two fields, in addition to other properties from the Office 365 audit log schema such as User, Operation, and Date can tell the full story about  *which*  user shared  *what*  resource with  *whom*  and  *when*.</span></span> 
  
<span data-ttu-id="6eda6-119">공유 스토리에 중요 한 또 다른 스키마 속성이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6eda6-119">There's another schema property that's important to the sharing story.</span></span> <span data-ttu-id="6eda6-120">**EventData** 속성은 공유 이벤트에 대 한 추가 정보를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="6eda6-120">The **EventData** property stores additional information about sharing events.</span></span> <span data-ttu-id="6eda6-121">예를 들어 사용자가 다른 사용자와 사이트를 공유 하는 경우이 작업을 수행 하려면 SharePoint 그룹에 대상 사용자를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="6eda6-121">For example, when a user shares a site with another user, this is accomplished by adding the target user to a SharePoint group.</span></span> <span data-ttu-id="6eda6-122">**EventData** 속성은이 추가 정보를 캡처하여 관리자에 게 컨텍스트를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="6eda6-122">The **EventData** property captures this additional information to provide context for administrators.</span></span> 

## <a name="the-sharepoint-sharing-model-and-sharing-events"></a><span data-ttu-id="6eda6-123">SharePoint 공유 모델 및 공유 이벤트</span><span class="sxs-lookup"><span data-stu-id="6eda6-123">The SharePoint Sharing model and sharing events</span></span>

<span data-ttu-id="6eda6-124">공유는 실제로 세 가지 개별 이벤트 인 **SharingSet**, **SharingInvitationCreated**및 **SharingInvitaitonAccepted**에 의해 정의 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6eda6-124">Sharing is actually defined by three separate events: **SharingSet**, **SharingInvitationCreated**, and **SharingInvitaitonAccepted**.</span></span> <span data-ttu-id="6eda6-125">다음은 공유 이벤트가 Office 365 감사 로그에 기록 되는 방식에 대 한 워크플로입니다.</span><span class="sxs-lookup"><span data-stu-id="6eda6-125">Here's the work flow for how sharing events are logged in the Office 365 audit log.</span></span> 
  
![공유 감사가 작동 하는 방식에 대 한 순서도](media/d83dd40f-919b-484f-bfd6-5dc8de31bff6.png)
  
<span data-ttu-id="6eda6-127">사용자 (작업 중인 사용자)가 다른 사용자 (대상 사용자)와 리소스를 공유 하려는 경우 먼저 SharePoint (또는 비즈니스용 OneDrive)가 대상 사용자의 전자 메일 주소가 조직의 디렉터리에 있는 사용자 계정과 이미 연결 되어 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="6eda6-127">When a user (the acting user) wants to share a resource with another user (the target user), SharePoint (or OneDrive for Business) first checks if the email address of the target user is already associated with a user account in the organization's directory.</span></span> <span data-ttu-id="6eda6-128">대상 사용자가 조직의 디렉터리에 있는 경우 SharePoint는 다음을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="6eda6-128">If the target user is in the organization's directory, SharePoint does the following:</span></span>
  
-  <span data-ttu-id="6eda6-129">리소스에 액세스할 수 있는 대상 사용자 권한을 즉시 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="6eda6-129">Immediately assigns the target user permissions to access the resource.</span></span> 
    
- <span data-ttu-id="6eda6-130">대상 사용자의 전자 메일 주소로 공유 알림을 보냅니다.</span><span class="sxs-lookup"><span data-stu-id="6eda6-130">Sends a sharing notification to the email address of the target user.</span></span>
    
- <span data-ttu-id="6eda6-131">**SharingSet** 이벤트를 기록 합니다.</span><span class="sxs-lookup"><span data-stu-id="6eda6-131">Logs a **SharingSet** event.</span></span> 
    
 <span data-ttu-id="6eda6-132">대상 사용자에 대 한 사용자 계정이 조직의 디렉터리에 없으면 SharePoint는 다음을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="6eda6-132">If a user account for the target user isn't in the organization's directory, SharePoint does the following:</span></span> 
  
- <span data-ttu-id="6eda6-133">공유 초대를 만들어 대상 사용자의 전자 메일 주소로 보냅니다.</span><span class="sxs-lookup"><span data-stu-id="6eda6-133">Creates a sharing invitation and sends it to the email address of the target user.</span></span>
    
- <span data-ttu-id="6eda6-134">**SharingInvitationCreated** 이벤트를 기록 합니다.</span><span class="sxs-lookup"><span data-stu-id="6eda6-134">Logs a **SharingInvitationCreated** event.</span></span> 
    
    > [!NOTE]
    > <span data-ttu-id="6eda6-135">**SharingInvitationCreated** 이벤트는 대상 사용자가 공유 된 리소스에 액세스할 수 없는 경우 항상 외부 또는 게스트 공유와 연결 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6eda6-135">The **SharingInvitationCreated** event is most always associated with external or guest sharing when the target user doesn't have access to the resource that was shared.</span></span> 
  
<span data-ttu-id="6eda6-136">대상 사용자가 초대의 링크를 클릭 하 여 전송 된 공유 초대를 수락 하면 SharePoint에서 **SharingInvitationAccepted** 이벤트를 기록 하 고 리소스에 액세스 하기 위한 대상 사용자 권한을 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="6eda6-136">When the target user accepts the sharing invitation that's sent to them (by clicking the link in the invitation), SharePoint logs a **SharingInvitationAccepted** event and assigns the target user permissions to access the resource.</span></span> <span data-ttu-id="6eda6-137">초대를 보낸 사용자의 id와 실제로 초대를 수락한 사용자에 대 한 정보를 비롯 하 여 대상 사용자에 대 한 추가 정보도 기록 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6eda6-137">Additional information about the target user is also logged, such as the identity of the user that the invitation was sent to and the user who actually accepted the invitation.</span></span> <span data-ttu-id="6eda6-138">경우에 따라 이러한 사용자 (또는 전자 메일 주소)는 다를 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6eda6-138">In some case, these users (or email addresses) might be different.</span></span> 
  

  
## <a name="how-to-identify-resources-shared-with-external-users"></a><span data-ttu-id="6eda6-139">외부 사용자와 공유 된 리소스를 확인 하는 방법</span><span class="sxs-lookup"><span data-stu-id="6eda6-139">How to identify resources shared with external users</span></span>

<span data-ttu-id="6eda6-140">관리자에 대 한 일반적인 요구 사항에는 조직 외부의 사용자와 공유 된 모든 리소스의 목록이 작성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6eda6-140">A common requirement for administrators is creating a list of all resources that have been shared with users outside of the organization.</span></span> <span data-ttu-id="6eda6-141">이제 관리자는 Office 365의 공유 감사를 사용 하 여이 목록을 생성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6eda6-141">By using sharing auditing in Office 365, administrators can now generate this list.</span></span> <span data-ttu-id="6eda6-142">이 작업을 수행하는 방법은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="6eda6-142">Here's how.</span></span>
  
### <a name="step-1-search-for-sharing-events-and-export-the-results-to-a-csv-file"></a><span data-ttu-id="6eda6-143">1 단계: 공유 이벤트 검색 및 결과를 CSV 파일로 내보내기</span><span class="sxs-lookup"><span data-stu-id="6eda6-143">Step 1: Search for sharing events and export the results to a CSV file</span></span>

<span data-ttu-id="6eda6-144">첫 번째 단계는 공유 이벤트에 대 한 Office 365 감사 로그를 검색 하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="6eda6-144">The first step is to search the Office 365 audit log for sharing events.</span></span> <span data-ttu-id="6eda6-145">감사 로그 검색에 대 한 자세한 내용 (필요한 권한 포함)은 [Security _AMP_ 준수 센터에서 감사 로그 검색](search-the-audit-log-in-security-and-compliance.md)을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="6eda6-145">For more details (including the required permissions) about searching the audit log, see [Search the audit log in the Security & Compliance Center](search-the-audit-log-in-security-and-compliance.md).</span></span>
  
1. <span data-ttu-id="6eda6-146">[https://protection.office.com](https://protection.office.com)으로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="6eda6-146">Go to [https://protection.office.com](https://protection.office.com).</span></span>
    
2. <span data-ttu-id="6eda6-147">회사 또는 학교 계정을 사용하여 Office 365에 로그인합니다.</span><span class="sxs-lookup"><span data-stu-id="6eda6-147">Sign in to Office 365 using your work or school account.</span></span>
    
3. <span data-ttu-id="6eda6-148">Security & 준수 센터의 왼쪽 창에서 **검색**  > **감사 로그 검색**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="6eda6-148">In the left pane of the Security & Compliance Center, click **Search**  > **Audit log search**.</span></span>
    
    <span data-ttu-id="6eda6-149">**감사 로그 검색** 페이지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6eda6-149">The **Audit log search** page is displayed.</span></span> 
    
4. <span data-ttu-id="6eda6-150">**작업**아래에서 **공유 작업** 을 클릭 하 여 공유 이벤트만 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="6eda6-150">Under **Activities**, click **Sharing activities** to search only for sharing events.</span></span> 
    
    ![활동 아래에서 공유 작업을 선택 합니다.](media/46bb25b7-1eb2-4adf-903a-cc9ab58639f9.png)
  
5.  <span data-ttu-id="6eda6-152">날짜 및 시간 범위를 선택 하 여 해당 기간 내에 발생 한 공유 이벤트를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="6eda6-152">Select a date and time range to find the sharing events that occurred within that period.</span></span> 
    
6. <span data-ttu-id="6eda6-153">검색 \*\*\*\* 을 클릭 하 여 검색을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="6eda6-153">Click **Search** to run the search.</span></span> 
    
7. <span data-ttu-id="6eda6-154">검색 실행이 완료 되 고 결과가 표시 되 면 결과 **내보내기** \> **모든 결과 다운로드**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="6eda6-154">When the search is finished running and the results are displayed , click **Export results** \> **Download all results**.</span></span>
    
    <span data-ttu-id="6eda6-155">내보내기 옵션을 선택한 후에는 CSV 파일을 열거나 저장 하 라는 메시지가 창 맨 아래에 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6eda6-155">After you select the export option, a message is displayed at the bottom of the window that prompts you to open or save the CSV file.</span></span>
    
8. <span data-ttu-id="6eda6-156">다른 \*\*\*\* \> **이름으로 저장** 저장을 클릭 하 고 로컬 컴퓨터의 폴더에 CSV 파일을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="6eda6-156">Click **Save** \> **Save as** and save the CSV file to a folder on your local computer.</span></span> 
    

  
### <a name="step-2-filter-the-csv-file-for-resources-shared-with-external-users"></a><span data-ttu-id="6eda6-157">2 단계: 외부 사용자와 공유 되는 리소스에 대 한 CSV 파일 필터링</span><span class="sxs-lookup"><span data-stu-id="6eda6-157">Step 2: Filter the CSV file for resources shared with external users</span></span>

<span data-ttu-id="6eda6-158">다음 단계는 **SharingSet** 및 **SharingInvitationCreated** 이벤트에 대 한 CSV를 필터링 하 고 **TargetUserOrGroupType** 속성이 **Guest**인 이벤트를 표시 하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="6eda6-158">The next step is to filter the CSV for the **SharingSet** and **SharingInvitationCreated** events, and to display those events where the **TargetUserOrGroupType** property is **Guest**.</span></span> <span data-ttu-id="6eda6-159">Excel에서 파워 쿼리 기능을 사용 하 여이 작업을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="6eda6-159">You'll use the Power Query feature in Excel to do this.</span></span> <span data-ttu-id="6eda6-160">다음은 Excel 2016에서 수행 하는 절차입니다.</span><span class="sxs-lookup"><span data-stu-id="6eda6-160">The following procedure is performed in Excel 2016.</span></span> 
  
1. <span data-ttu-id="6eda6-161">Excel 2016에서 빈 통합 문서를 엽니다.</span><span class="sxs-lookup"><span data-stu-id="6eda6-161">In Excel 2016, open a blank workbook.</span></span>
    
2. <span data-ttu-id="6eda6-162">**데이터** 탭을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="6eda6-162">Click the **Data** tab.</span></span> 
    
3. <span data-ttu-id="6eda6-163">\> **CSV에서** **파일에서** **새 쿼리** \> 를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="6eda6-163">Click **New Query** \> **From file** \> **From CSV**.</span></span>
    
    ![데이터 탭에서 새 쿼리를 선택 하 고 파일을 선택한 다음 CSV를 선택 합니다.](media/5170ab34-b449-40ea-bd3f-f1432c1c5973.png)
  
4. <span data-ttu-id="6eda6-165">1 단계에서 다운로드 한 CSV 파일을 엽니다.</span><span class="sxs-lookup"><span data-stu-id="6eda6-165">Open the CSV file that you downloaded in Step 1.</span></span>
    
    <span data-ttu-id="6eda6-166">CSV 파일이 쿼리 편집기에서 열립니다.</span><span class="sxs-lookup"><span data-stu-id="6eda6-166">The CSV file is opened in the Query Editor.</span></span> <span data-ttu-id="6eda6-167">여기에는 **Time**, **User**, **Action**및 **Detail**이라는 네 가지 열이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6eda6-167">Note that there are four columns: **Time**, **User**, **Action**, and **Detail**.</span></span> <span data-ttu-id="6eda6-168">**세부 정보** 열은 다중 속성 필드입니다.</span><span class="sxs-lookup"><span data-stu-id="6eda6-168">The **Detail** column is a multi-property field.</span></span> <span data-ttu-id="6eda6-169">다음 단계에서는 **세부** 정보 열의 각 속성에 대해 새 열을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6eda6-169">The next step is to create a new column for each of the properties in the **Detail** column.</span></span> 
    
5. <span data-ttu-id="6eda6-170">**세부 정보** 열을 선택한 다음 **홈** 탭에서 **구분 기호로** **분할 열** \> 을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="6eda6-170">Select the **Detail** column, and then on the **Home** tab, click **Split Column** \> **By Delimiter**.</span></span>
    
    ![홈 탭에서 열 분할을 클릭 한 다음 구분 기호를 클릭 합니다.](media/aeb503e8-565b-42ea-91e2-9f127a74c00c.png)
  
6. <span data-ttu-id="6eda6-172">**구분 기호 단위로 열 분할** 창에서 다음을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="6eda6-172">In the **Split Column by Delimiter** window, do the following:</span></span> 
    
      - <span data-ttu-id="6eda6-173">**구분 기호 선택 또는 입력**에서 **쉼표**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="6eda6-173">Under **Select or enter delimiter**, select **Comma**.</span></span>
    
      - <span data-ttu-id="6eda6-174">**분할**에서 **구분 기호의 각 항목**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="6eda6-174">Under **Split**, select **At each occurrence of the delimiter**.</span></span>
    
7. <span data-ttu-id="6eda6-175">**확인**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="6eda6-175">Click **OK**.</span></span>
    
    <span data-ttu-id="6eda6-176">**세부 정보** 열이 여러 열로 분할 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6eda6-176">The **Detail** column is split into multiple columns.</span></span> <span data-ttu-id="6eda6-177">각각의 새 열에는 Detail 이라는 이름이 지정 됩니다. **1**, **detail. 2**, **세부 정보 3**등.</span><span class="sxs-lookup"><span data-stu-id="6eda6-177">Each new column is named **Detail.1**, **Detail.2**, **Detail.3**, and so on.</span></span> <span data-ttu-id="6eda6-178">**자세한 내용은 Detail** 의 각 셀에 있는 값에 속성 이름을 접두사로 사용 합니다. 예 **: SharingSet**, **Operation: SharingInvitationAccepted**및 **Operation: SharingInvitationCreated**</span><span class="sxs-lookup"><span data-stu-id="6eda6-178">You'll notice the values in each cell in the **Detail.n** columns are prefixed with the name of the property; for example, **Operation:SharingSet**, **Operation:SharingInvitationAccepted**, and **Operation:SharingInvitationCreated**.</span></span>
    
    ![세부 정보 열은 각 속성에 하나씩 여러 열로 분할 됩니다.](media/4b104ead-0313-4bd4-b2a9-f143ccb378ac.png)
  
8. <span data-ttu-id="6eda6-180">**파일** 탭에서 \*\*로드 닫기를 &amp; \*\* 클릭 하 여 쿼리 편집기를 닫고 Excel 통합 문서에서 파일을 엽니다.</span><span class="sxs-lookup"><span data-stu-id="6eda6-180">On the **File** tab, click **Close &amp; Load** to close the Query Editor and open the file in an Excel workbook.</span></span> 
    
    <span data-ttu-id="6eda6-181">다음 단계는 **SharingSet** 및 **SharingInvitationCreated** 이벤트만 표시 하도록 파일을 필터링 하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="6eda6-181">The next step is to filter the file to only display the **SharingSet** and **SharingInvitationCreated** events.</span></span> 
    
9. <span data-ttu-id="6eda6-182">**홈** 탭으로 이동한 다음 **작업** 열을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="6eda6-182">Go to the **Home** tab, and then select the **Action** column.</span></span> 
    
10. <span data-ttu-id="6eda6-183">**정렬 &amp; 필터** 드롭다운 목록에서 모든 선택을 취소 하 고 **SharingSet** 및 **SharingInvitationCreated**을 선택한 다음 **확인**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="6eda6-183">In the **Sort &amp; Filter** drop-down list, clear all selections, then select **SharingSet** and **SharingInvitationCreated**, and click **OK**.</span></span>
    
    <span data-ttu-id="6eda6-184">Excel에 **SharingSet** 및 **SharingInvitationCreated** 이벤트에 대 한 행이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6eda6-184">Excel displays the rows for the **SharingSet** and **SharingInvitationCreated** events.</span></span> 
    
11. <span data-ttu-id="6eda6-185">**Detail. 17** (또는 **TargetUserOrGroupType** 속성을 포함 하는 열)로 이동 하 여 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="6eda6-185">Go to the column named **Detail.17** (or whichever column contains the **TargetUserOrGroupType** property) and select it.</span></span> 
    
12. <span data-ttu-id="6eda6-186">**정렬 &amp; 필터** 드롭다운 목록에서 모든 선택을 취소 하 고 **TargetUserOrGroupType: Guest**를 선택한 다음 **확인**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="6eda6-186">In the **Sort &amp; Filter** drop-down list, clear all selections, then select **TargetUserOrGroupType:Guest**, and click **OK**.</span></span>
    
    <span data-ttu-id="6eda6-187">이제 외부 사용자는 **TargetUserOrGroupType: Guest**값으로 식별 되므로 **SharingInvitationCreated** 및 **SharingSet** 이벤트와 대상 사용자가 조직 외부에 있는 위치에 대 한 행이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6eda6-187">Now Excel displays the rows for **SharingInvitationCreated** and **SharingSet** events AND where the target user is outside of your organization, because external users are identified by the value **TargetUserOrGroupType:Guest**.</span></span> 
    
<span data-ttu-id="6eda6-188">다음 표에는 지정 된 날짜 범위 내에서 게스트 사용자와 리소스를 공유 하는 조직의 모든 사용자가 나와 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6eda6-188">The following table shows all users in the organization who shared resources with a guest user within a specified date range.</span></span>
  
![Office 365 감사 로그에서 이벤트 공유](media/0e0ecbe3-c794-4ca6-a2ca-63478fb3bb34.png)
  
<span data-ttu-id="6eda6-190">이 속성은 이전 표에는 포함 되어 있지 않지만, **자세히. 10 개** 열 또는 **ObjectId** 속성이 포함 된 모든 열에는 대상 사용자와 공유 된 리소스를 식별 합니다. 예를 `ObjectId:https:\/\/contoso-my.sharepoint.com\/personal\/sarad_contoso_com\/Documents\/Southwater Proposal.docx`들어</span><span class="sxs-lookup"><span data-stu-id="6eda6-190">Although it's not included in the previous table, the **Detail.10** column (or whichever column contains the **ObjectId** property) identifies the resource that was shared with the target user; for example  `ObjectId:https:\/\/contoso-my.sharepoint.com\/personal\/sarad_contoso_com\/Documents\/Southwater Proposal.docx`.</span></span>
  
> [!TIP]
> <span data-ttu-id="6eda6-191">게스트 사용자에 게 실제로 리소스에 액세스 하기 위한 사용 권한이 할당 된 시간을 확인 하려면 (이러한 리소스와 공유 하는 리소스만 해당) 10, 11 및 12 단계를 반복 하 고 **SharingInvitationAccepted** 및 SharingSet의 필터를 적용 합니다. \*\* \*\*10 단계의 이벤트</span><span class="sxs-lookup"><span data-stu-id="6eda6-191">If you want to identify when a guest user was actually assigned permissions to access a resource (as opposed to just the resources that where shared with them), repeat Steps 10, 11, and 12, and filter on the **SharingInvitationAccepted** and **SharingSet** events in Step 10.</span></span> 
