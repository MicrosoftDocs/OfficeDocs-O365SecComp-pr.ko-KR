---
title: Office 365 감사 로그에 감사 공유를 사용 하 여
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 2/13/2018
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- SPO160
- MOE150
- BCS160
- MET150
ms.assetid: 50bbf89f-7870-4c2a-ae14-42635e0cfc01
description: 'SharePoint Online 및 비즈니스용 OneDrive의 주요 작업은 공유입니다. 관리자가 이제 사용할 수 Office 365 감사 로그에 감사 공유 어떻게 공유 사용 되 고 조직에서 결정 합니다. '
ms.openlocfilehash: 511f8b0e61d450659d78177d5b87fac9ee636cd4
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22533608"
---
# <a name="use-sharing-auditing-in-the-office-365-audit-log"></a><span data-ttu-id="b1dbf-104">Office 365 감사 로그에 감사 공유를 사용 하 여</span><span class="sxs-lookup"><span data-stu-id="b1dbf-104">Use sharing auditing in the Office 365 audit log</span></span>

<span data-ttu-id="b1dbf-p102">SharePoint Online 및, 비즈니스용 OneDrive의 주요 작업은 공유 하 고 Office 365 조직에서 사용 되는 광범위 하 게 됩니다. 관리자가 이제 사용할 수 Office 365 감사 로그에 감사 공유 어떻게 공유 사용 되 고 조직에서 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1dbf-p102">Sharing is a key activity in SharePoint Online and OneDrive for Business, and it's widely used in Office 365 organizations. Administrators can now use sharing auditing in the Office 365 audit log to determine how sharing is being used in their organization.</span></span> 
  
## <a name="the-sharepoint-sharing-schema"></a><span data-ttu-id="b1dbf-107">SharePoint 공유 스키마</span><span class="sxs-lookup"><span data-stu-id="b1dbf-107">The SharePoint Sharing schema</span></span>

<span data-ttu-id="b1dbf-p103">기본 방법 중 하나에서 (제외 공유 정책 및 공유 링크 이벤트) 공유 이벤트는 파일 및 폴더와 관련 된 이벤트에서 서로 다른: 한 명의 사용자가 다른 사용자에는 일부 적용 하는 동작을 수행 합니다. 예, 사용자 A 파일에 사용자 B 대 한 액세스를 제공합니다. 이 예제에서는 사용자 A가 *사용자 역할* 및 사용자 B는 *대상 사용자*입니다. SharePoint 파일 스키마에서 활성 사용자 작업 파일을 자체만 영향을 줍니다. 사용자 A **FileAccessed** 이벤트에 필요한 유일한 정보 파일을 열고가 경우 활성 사용자입니다. 이 차이 해결 하기 위해 별도 스키마를 호출 하는 *SharePoint 공유 스키마*, 이벤트를 공유 하는 방법에 대 한 자세한 정보를 캡처하는 방법이 있습니다. 이렇게 하면 관리자에 게는 리소스를 공유 있는 통찰력 하 고 리소스 사용자와 공유 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="b1dbf-p103">Sharing events (excluding sharing policy and sharing link events) are different from file- and folder-related events in one primary way: one user is taking an action that has some effect on another user. For example, User A gives User B access to a file. In this example, User A is the  *acting user*  and User B is the  *target user*. In the SharePoint File schema, the acting user's action only affects the file itself. When User A opens a file, the only information needed in the **FileAccessed** event is the acting user. To address this difference, there is a separate schema, called the  *SharePoint Sharing schema*, that captures more information about sharing events. This ensures that administrators have more insight into who shared a resource and the user the resource was shared with.</span></span> 
  
<span data-ttu-id="b1dbf-115">공유 스키마 이벤트 공유와 관련 된 감사 로그의 두 추가 필드를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1dbf-115">The Sharing schema provides two additional fields in the audit log related to sharing events:</span></span> 
  
- <span data-ttu-id="b1dbf-116">**TargetUserOrGroupName** -UPN 또는 대상 사용자 또는 리소스 (앞의 예제에서 사용자 B)와 공유 하는 그룹의 이름을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1dbf-116">**TargetUserOrGroupName** - Stores the UPN or name of the target user or group that a resource was shared with (User B in the previous example).</span></span> 
    
- <span data-ttu-id="b1dbf-117">**TargetUserOrGroupType** -대상 사용자 또는 그룹 구성원, 게스트, 그룹 또는 파트너 인지 여부를 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1dbf-117">**TargetUserOrGroupType** - Identifies whether the target user or group is a Member, Guest, Group, or Partner.</span></span> 
    
<span data-ttu-id="b1dbf-118">Office 365에서 다른 속성 외에도 두 필드, 사용자, 작업, 및 날짜 수 있는 차트를 만드는 방법 전체 리소스에 대 한 *어떤* 사용자 공유 *어떤* *누구에 게* 및 *시기*와 같은 로그 스키마를 감사 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1dbf-118">These two fields, in addition to other properties from the Office 365 audit log schema such as User, Operation, and Date can tell the full story about  *which*  user shared  *what*  resource with  *whom*  and  *when*.</span></span> 
  
<span data-ttu-id="b1dbf-p104">공유 텍스트 영역에 중요 한 스키마 속성을 다른 방법이 있습니다. **EventData** 속성은 이벤트를 공유 하는 방법에 대 한 추가 정보를 저장 합니다. 예, 다른 사용자와 사이트를 공유 하는 사용자 때 SharePoint 그룹에 대상 사용자를 추가 하 여 수행 됩니다. **EventData** 속성 관리자에 대 한 컨텍스트를 제공 하는이 추가 정보를 캡처합니다.</span><span class="sxs-lookup"><span data-stu-id="b1dbf-p104">There's another schema property that's important to the sharing story. The **EventData** property stores additional information about sharing events. For example, when a user shares a site with another user, this is accomplished by adding the target user to a SharePoint group. The **EventData** property captures this additional information to provide context for administrators.</span></span> 

## <a name="the-sharepoint-sharing-model-and-sharing-events"></a><span data-ttu-id="b1dbf-123">SharePoint 공유 모델 및 이벤트를 공유 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1dbf-123">The SharePoint Sharing model and sharing events</span></span>

<span data-ttu-id="b1dbf-p105">세 별도 이벤트에 의해 정의 된 실제로 공유: **SharingSet**, **SharingInvitationCreated**및 **SharingInvitaitonAccepted**합니다. 여기서의 일정 공유 이벤트에 대 한 작업 흐름 Office 365 감사 로그에 기록 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b1dbf-p105">Sharing is actually defined by three separate events: **SharingSet**, **SharingInvitationCreated**, and **SharingInvitaitonAccepted**. Here's the work flow for how sharing events are logged in the Office 365 audit log.</span></span> 
  
![감사 공유의 작동 방식을 보여주는 순서도](media/d83dd40f-919b-484f-bfd6-5dc8de31bff6.png)
  
<span data-ttu-id="b1dbf-p106">사용자 (활성 사용자)가 다른 사용자 (대상 사용자)와 리소스를 공유 하려는 경우 SharePoint (또는 비즈니스용 OneDrive) 먼저 확인 하는 경우 대상 사용자의 전자 메일 주소 이미 조직의 디렉터리에서 사용자 계정과 사용 하 여 연결 합니다. 대상 사용자 조직의 디렉터리에 포함 된 경우 SharePoint는 다음을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1dbf-p106">When a user (the acting user) wants to share a resource with another user (the target user), SharePoint (or OneDrive for Business) first checks if the email address of the target user is already associated with a user account in the organization's directory. If the target user is in the organization's directory, SharePoint does the following:</span></span>
  
-  <span data-ttu-id="b1dbf-129">즉시 리소스에 액세스 하는 대상 사용자 권한을 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1dbf-129">Immediately assigns the target user permissions to access the resource.</span></span> 
    
- <span data-ttu-id="b1dbf-130">대상 사용자의 전자 메일 주소를 공유 알림을 보냅니다.</span><span class="sxs-lookup"><span data-stu-id="b1dbf-130">Sends a sharing notification to the email address of the target user.</span></span>
    
- <span data-ttu-id="b1dbf-131">**SharingSet** 이벤트를 기록합니다.</span><span class="sxs-lookup"><span data-stu-id="b1dbf-131">Logs a **SharingSet** event.</span></span> 
    
 <span data-ttu-id="b1dbf-132">대상 사용자에 대 한 사용자 계정을 조직의 디렉터리에 없으면 SharePoint는 다음을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1dbf-132">If a user account for the target user isn't in the organization's directory, SharePoint does the following:</span></span> 
  
- <span data-ttu-id="b1dbf-133">공유 초대 메일을 만들고 대상 사용자의 전자 메일 주소로 보냅니다.</span><span class="sxs-lookup"><span data-stu-id="b1dbf-133">Creates a sharing invitation and sends it to the email address of the target user.</span></span>
    
- <span data-ttu-id="b1dbf-134">**SharingInvitationCreated** 이벤트를 기록합니다.</span><span class="sxs-lookup"><span data-stu-id="b1dbf-134">Logs a **SharingInvitationCreated** event.</span></span> 
    
    > [!NOTE]
    > <span data-ttu-id="b1dbf-135">**SharingInvitationCreated** 이벤트 외부 또는 게스트 공유 대상 사용자는 공유 된 리소스에 액세스할 수 없는 경우와 항상 가장 관련이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b1dbf-135">The **SharingInvitationCreated** event is most always associated with external or guest sharing when the target user doesn't have access to the resource that was shared.</span></span> 
  
<span data-ttu-id="b1dbf-p107">대상 사용자가 보낸 자신에 게 (을 클릭 하 여 초대장의 링크), SharePoint 공유 초대를 수락 하는 경우 **SharingInvitationAccepted** 이벤트를 기록 하 고 리소스에 액세스 하는 대상 사용자 권한을 할당 합니다. 초대를 받은 사용자 및 초대를 수락 실제로 사용자의 id와 같은 대상 사용자에 대 한 자세한 내용은, 기록 됩니다. 일부 경우에 이러한 사용자 (또는 전자 메일 주소) 다를 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b1dbf-p107">When the target user accepts the sharing invitation that's sent to them (by clicking the link in the invitation), SharePoint logs a **SharingInvitationAccepted** event and assigns the target user permissions to access the resource. Additional information about the target user is also logged, such as the identity of the user that the invitation was sent to and the user who actually accepted the invitation. In some case, these users (or email addresses) might be different.</span></span> 
  

  
## <a name="how-to-identify-resources-shared-with-external-users"></a><span data-ttu-id="b1dbf-139">외부 사용자와 공유 되는 리소스를 식별 하는 방법</span><span class="sxs-lookup"><span data-stu-id="b1dbf-139">How to identify resources shared with external users</span></span>

<span data-ttu-id="b1dbf-p108">관리자를 위한 공통 된 요구 사항에는 조직 외부의 사용자와 공유 되는 모든 리소스의 목록을 만드는 것입니다. Office 365에서 감사 공유를 사용 하 여 관리자가 이제이 목록을 생성할 수 있습니다. 다음은 방법입니다.</span><span class="sxs-lookup"><span data-stu-id="b1dbf-p108">A common requirement for administrators is creating a list of all resources that have been shared with users outside of the organization. By using sharing auditing in Office 365, administrators can now generate this list. Here's how.</span></span>
  
### <a name="step-1-search-for-sharing-events-and-export-the-results-to-a-csv-file"></a><span data-ttu-id="b1dbf-143">1 단계: 검색 이벤트를 공유 하 고 결과 CSV 파일로 내보내기</span><span class="sxs-lookup"><span data-stu-id="b1dbf-143">Step 1: Search for sharing events and export the results to a CSV file</span></span>

<span data-ttu-id="b1dbf-p109">이벤트를 공유 하기 위한 Office 365 감사 로그를 검색 하는 첫번째 단계가입니다. 자세한 내용은 (필요한 사용 권한 포함) 감사 로그를 검색 하는 방법에 대 한 참조 [Office 365 보안에서 감사 로그를 검색 &amp; 준수 센터](search-the-audit-log-in-security-and-compliance.md)합니다.</span><span class="sxs-lookup"><span data-stu-id="b1dbf-p109">The first step is to search the Office 365 audit log for sharing events. For more details (including the required permissions) about searching the audit log, see [Search the audit log in the Office 365 Security &amp; Compliance Center](search-the-audit-log-in-security-and-compliance.md).</span></span>
  
1. <span data-ttu-id="b1dbf-146">이동 [https://protection.office.com](https://protection.office.com)합니다.</span><span class="sxs-lookup"><span data-stu-id="b1dbf-146">Go to [https://protection.office.com](https://protection.office.com).</span></span>
    
2. <span data-ttu-id="b1dbf-147">작업이 나 교육용 계정을 사용 하 여 Office 365에 로그인 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1dbf-147">Sign in to Office 365 using your work or school account.</span></span>
    
3. <span data-ttu-id="b1dbf-148">보안의 왼쪽된 창에서 &amp; 준수 센터 클릭 **검색 &amp; 조사**, **감사 로그 검색**을 클릭 하 고 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b1dbf-148">In the left pane of the Security &amp; Compliance Center, click **Search &amp; investigation**, and then click **Audit log search**.</span></span>
    
    <span data-ttu-id="b1dbf-149">**감사 로그 검색** 페이지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b1dbf-149">The **Audit log search** page is displayed.</span></span> 
    
4. <span data-ttu-id="b1dbf-150">**활동**이벤트를 공유에 검색 하려면 **공유 작업** 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1dbf-150">Under **Activities**, click **Sharing activities** to search only for sharing events.</span></span> 
    
    ![활동을 공유 활동 선택](media/46bb25b7-1eb2-4adf-903a-cc9ab58639f9.png)
  
5.  <span data-ttu-id="b1dbf-152">해당 기간 내에 발생 하는 공유 이벤트를 찾는 날짜 및 시간 범위를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1dbf-152">Select a date and time range to find the sharing events that occurred within that period.</span></span> 
    
6. <span data-ttu-id="b1dbf-153">검색을 실행 하려면 **검색** 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1dbf-153">Click **Search** to run the search.</span></span> 
    
7. <span data-ttu-id="b1dbf-154">실행 및 결과 표시 검색이 완료 되 면, **결과 내보내기를** 클릭 \> **모든 결과 다운로드**합니다.</span><span class="sxs-lookup"><span data-stu-id="b1dbf-154">When the search is finished running and the results are displayed , click **Export results** \> **Download all results**.</span></span>
    
    <span data-ttu-id="b1dbf-155">내보내기 옵션을 선택한 후 열기 또는 CSV 파일을 저장 하 라는 메시지가 표시 되는 창 맨 아래에 메시지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b1dbf-155">After you select the export option, a message is displayed at the bottom of the window that prompts you to open or save the CSV file.</span></span>
    
8. <span data-ttu-id="b1dbf-156">**저장** 을 클릭 하 \> **로 저장** 하 고 로컬 컴퓨터의 폴더에 CSV 파일을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1dbf-156">Click **Save** \> **Save as** and save the CSV file to a folder on your local computer.</span></span> 
    

  
### <a name="step-2-filter-the-csv-file-for-resources-shared-with-external-users"></a><span data-ttu-id="b1dbf-157">외부 사용자와 공유 되는 리소스에 대 한 CSV 파일을 필터링 하는 2 단계:</span><span class="sxs-lookup"><span data-stu-id="b1dbf-157">Step 2: Filter the CSV file for resources shared with external users</span></span>

<span data-ttu-id="b1dbf-p110">다음 단계에서는 **TargetUserOrGroupType** 속성이 **게스트**으로 **SharingSet** 및 **SharingInvitationCreated** 이벤트에 대 한 CSV 필터링 하 고 해당 이벤트를 표시할 수입니다. Excel에서 파워 쿼리 기능을 사용 하 여이 작업을 수행 합니다. 다음 절차는 Excel 2016에서 수행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b1dbf-p110">The next step is to filter the CSV for the **SharingSet** and **SharingInvitationCreated** events, and to display those events where the **TargetUserOrGroupType** property is **Guest**. You'll use the Power Query feature in Excel to do this. The following procedure is performed in Excel 2016.</span></span> 
  
1. <span data-ttu-id="b1dbf-161">Excel 2016에서 빈 통합 문서를 엽니다.</span><span class="sxs-lookup"><span data-stu-id="b1dbf-161">In Excel 2016, open a blank workbook.</span></span>
    
2. <span data-ttu-id="b1dbf-162">**데이터** 탭을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="b1dbf-162">Click the **Data** tab.</span></span> 
    
3. <span data-ttu-id="b1dbf-163">**새 쿼리** 를 클릭 \> **파일에서** \> **에서 CSV**합니다.</span><span class="sxs-lookup"><span data-stu-id="b1dbf-163">Click **New Query** \> **From file** \> **From CSV**.</span></span>
    
    ![데이터 탭에서 새 쿼리를 선택, 파일을 선택한 다음 선택에서 CSV](media/5170ab34-b449-40ea-bd3f-f1432c1c5973.png)
  
4. <span data-ttu-id="b1dbf-165">1 단계에서에서 다운로드 한 CSV 파일을 엽니다.</span><span class="sxs-lookup"><span data-stu-id="b1dbf-165">Open the CSV file that you downloaded in Step 1.</span></span>
    
    <span data-ttu-id="b1dbf-p111">CSV 파일을 쿼리 편집기에서 열입니다. 4 개 열은: **시간**, **사용자**, **작업**및 **세부 정보**입니다. **세부 정보** 열은 다중 속성 필드입니다. 다음 단계에서는 각각의 **세부 정보** 열에서 속성에 대 한 새 열을 만드는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="b1dbf-p111">The CSV file is opened in the Query Editor. Note that there are four columns: **Time**, **User**, **Action**, and **Detail**. The **Detail** column is a multi-property field. The next step is to create a new column for each of the properties in the **Detail** column.</span></span> 
    
5. <span data-ttu-id="b1dbf-170">**세부 정보** 열을 선택 하 고 **홈** 탭에서 **분할 열** 을 클릭 한 다음 \> **하 여 구분**합니다.</span><span class="sxs-lookup"><span data-stu-id="b1dbf-170">Select the **Detail** column, and then on the **Home** tab, click **Split Column** \> **By Delimiter**.</span></span>
    
    ![홈 탭에서 분할 열을 클릭 한 다음 하 여 구분 기호를 클릭 합니다.](media/aeb503e8-565b-42ea-91e2-9f127a74c00c.png)
  
6. <span data-ttu-id="b1dbf-172">**구분 기호로 사용 하 여 분할 열** 창에서 다음을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1dbf-172">In the **Split Column by Delimiter** window, do the following:</span></span> 
    
      - <span data-ttu-id="b1dbf-173">**선택 하거나 구분 기호를 입력**하십시오 아래에서 **쉼표**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1dbf-173">Under **Select or enter delimiter**, select **Comma**.</span></span>
    
      - <span data-ttu-id="b1dbf-174">**분할** **대 한 구분 기호로 모두**선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1dbf-174">Under **Split**, select **At each occurrence of the delimiter**.</span></span>
    
7. <span data-ttu-id="b1dbf-175">**확인**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="b1dbf-175">Click **OK**.</span></span>
    
    <span data-ttu-id="b1dbf-p112">**세부 정보** 열은 여러 열으로 분할 됩니다. 새로 만든 각 열에 **Detail.1**, **Detail.2**, **Detail.3**등에 라고 합니다. **Detail.n** 열에 있는 각 셀의 값은 속성의 이름을 라는 접두사가 하는 것을 알 수 있습니다. 예: **작업: SharingSet**, **작업: SharingInvitationAccepted**및 **작업: SharingInvitationCreated**합니다.</span><span class="sxs-lookup"><span data-stu-id="b1dbf-p112">The **Detail** column is split into multiple columns. Each new column is named **Detail.1**, **Detail.2**, **Detail.3**, and so on. You'll notice the values in each cell in the **Detail.n** columns are prefixed with the name of the property; for example, **Operation:SharingSet**, **Operation:SharingInvitationAccepted**, and **Operation:SharingInvitationCreated**.</span></span>
    
    ![세부 정보 열에서 각 속성에 대 한 여러 열, 분할](media/4b104ead-0313-4bd4-b2a9-f143ccb378ac.png)
  
8. <span data-ttu-id="b1dbf-180">**파일** 탭을 클릭 **닫습니다 &amp; 부하** 를 쿼리 편집기를 닫고 Excel 통합 문서에서 파일을 엽니다.</span><span class="sxs-lookup"><span data-stu-id="b1dbf-180">On the **File** tab, click **Close &amp; Load** to close the Query Editor and open the file in an Excel workbook.</span></span> 
    
    <span data-ttu-id="b1dbf-181">다음 단계에서는 **SharingSet** 및 **SharingInvitationCreated** 이벤트를 표시 하려면 파일을 필터링 하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="b1dbf-181">The next step is to filter the file to only display the **SharingSet** and **SharingInvitationCreated** events.</span></span> 
    
9. <span data-ttu-id="b1dbf-182">**홈** 탭으로 이동 하 고 **작업** 열을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1dbf-182">Go to the **Home** tab, and then select the **Action** column.</span></span> 
    
10. <span data-ttu-id="b1dbf-183">**정렬 &amp; 필터** 드롭다운 목록, 지우기 모두 선택에서 다음 **SharingSet** 및 **SharingInvitationCreated**선택 하 고 **확인**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1dbf-183">In the **Sort &amp; Filter** drop-down list, clear all selections, then select **SharingSet** and **SharingInvitationCreated**, and click **OK**.</span></span>
    
    <span data-ttu-id="b1dbf-184">Excel은 **SharingSet** 및 **SharingInvitationCreated** 이벤트에 대 한 행을 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="b1dbf-184">Excel displays the rows for the **SharingSet** and **SharingInvitationCreated** events.</span></span> 
    
11. <span data-ttu-id="b1dbf-185">**Detail.17** (또는 열에 어떤 **TargetUserOrGroupType** 속성을 포함) 라는 열으로 이동 하 고 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1dbf-185">Go to the column named **Detail.17** (or whichever column contains the **TargetUserOrGroupType** property) and select it.</span></span> 
    
12. <span data-ttu-id="b1dbf-186">**정렬 &amp; 필터** 드롭다운 목록, 지우기 모든 선택 영역에서 다음 **TargetUserOrGroupType:Guest**선택 하 고 **확인**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1dbf-186">In the **Sort &amp; Filter** drop-down list, clear all selections, then select **TargetUserOrGroupType:Guest**, and click **OK**.</span></span>
    
    <span data-ttu-id="b1dbf-187">이제 Excel 외부 사용자는 **TargetUserOrGroupType:Guest**값에 의해 식별 하기 때문에 **SharingInvitationCreated** 및 **SharingSet** 이벤트에 대 한 조직 외부의 대상 사용자가 행을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1dbf-187">Now Excel displays the rows for **SharingInvitationCreated** and **SharingSet** events AND where the target user is outside of your organization, because external users are identified by the value **TargetUserOrGroupType:Guest**.</span></span> 
    
<span data-ttu-id="b1dbf-188">다음 표에서 지정한 날짜 범위 내에서 게스트 사용자와 리소스를 공유 하 여 조직의 모든 사용자를 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="b1dbf-188">The following table shows all users in the organization who shared resources with a guest user within a specified date range.</span></span>
  
![Office 365의 공유 이벤트 감사 로그](media/0e0ecbe3-c794-4ca6-a2ca-63478fb3bb34.png)
  
<span data-ttu-id="b1dbf-190">**Detail.10** 열 (또는 열에 어떤 **ObjectId** 속성을 포함), 대상 사용자와 공유 된 리소스를 식별 하는 앞의 표에 포함 되지 않습니다, 하지만 예 `ObjectId:https:\/\/contoso-my.sharepoint.com\/personal\/sarad_contoso_com\/Documents\/Southwater Proposal.docx`합니다.</span><span class="sxs-lookup"><span data-stu-id="b1dbf-190">Although it's not included in the previous table, the **Detail.10** column (or whichever column contains the **ObjectId** property) identifies the resource that was shared with the target user; for example  `ObjectId:https:\/\/contoso-my.sharepoint.com\/personal\/sarad_contoso_com\/Documents\/Southwater Proposal.docx`.</span></span>
  
> [!TIP]
> <span data-ttu-id="b1dbf-191">확인 하려는 경우 때 게스트 사용자 실제로 할당 된 리소스에 액세스할 수 있는 권한을 (방금 리소스 것과 반대로 해당 위치와 공유), 10, 11, 12, 단계를 반복 하 고 **SharingInvitationAccepted** 및 **SharingSet 필터링 **10 단계에서에서 이벤트입니다.</span><span class="sxs-lookup"><span data-stu-id="b1dbf-191">If you want to identify when a guest user was actually assigned permissions to access a resource (as opposed to just the resources that where shared with them), repeat Steps 10, 11, and 12, and filter on the **SharingInvitationAccepted** and **SharingSet** events in Step 10.</span></span> 
