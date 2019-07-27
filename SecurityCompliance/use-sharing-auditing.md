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
description: '공유는 SharePoint Online 및 비즈니스용 OneDrive의 주요 활동입니다. 이제 관리자는 Office 365 감사 로그의 공유 감사를 사용 하 여 조직 외부의 사용자와 공유 되는 리소스를 식별할 수 있습니다. '
ms.openlocfilehash: 8996d404e2dbeaba01952c33a8699ca2f151ad5d
ms.sourcegitcommit: a8049055a48375bee7e6ed81fafcb27a7b2fcdff
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/26/2019
ms.locfileid: "35911778"
---
# <a name="use-sharing-auditing-in-the-office-365-audit-log"></a><span data-ttu-id="b90c7-104">외부 사용자와 공유된 리소스를 찾기 위한 감사 공유</span><span class="sxs-lookup"><span data-stu-id="b90c7-104">Use sharing auditing in the Office 365 audit log</span></span>

<span data-ttu-id="b90c7-105">공유는 SharePoint Online 및 비즈니스용 OneDrive의 주요 활동 이며, Office 365 조직에서 널리 사용 되 고 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b90c7-105">Sharing is a key activity in SharePoint Online and OneDrive for Business, and it's widely used in Office 365 organizations.</span></span> <span data-ttu-id="b90c7-106">관리자는 Office 365 감사 로그의 공유 감사를 사용 하 여 조직에서 공유를 사용 하는 방법을 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b90c7-106">Administrators can use sharing auditing in the Office 365 audit log to determine how sharing is used in their organization.</span></span> 
  
## <a name="the-sharepoint-sharing-schema"></a><span data-ttu-id="b90c7-107">SharePoint 공유 스키마</span><span class="sxs-lookup"><span data-stu-id="b90c7-107">The SharePoint Sharing schema</span></span>

<span data-ttu-id="b90c7-108">공유 정책 및 공유 링크와 관련 된 이벤트를 제외 하 고 발생 하는 관리 이벤트는 파일 및 폴더 관련 이벤트와는 다른 사용자에 게 영향을 주는 작업을 수행 하는 기본적인 방법 중 하나입니다.</span><span class="sxs-lookup"><span data-stu-id="b90c7-108">Sharing events (not including events related to sharing policy and sharing links) are different from file- and folder-related events in one primary way: one user is performing an action that has an effect on another user.</span></span> <span data-ttu-id="b90c7-109">예를 들어 자원 사용자 A가 사용자 B에 게 파일에 대 한 액세스 권한을 부여 하는 경우</span><span class="sxs-lookup"><span data-stu-id="b90c7-109">For example, when a resource User A gives User B access to a file.</span></span> <span data-ttu-id="b90c7-110">이 예에서는 사용자 A가 작업 중인 *사용자* 이 고 사용자 B가 *대상 사용자*입니다.</span><span class="sxs-lookup"><span data-stu-id="b90c7-110">In this example, User A is the  *acting user*  and User B is the  *target user*.</span></span> <span data-ttu-id="b90c7-111">SharePoint 파일 스키마에서 작동 중인 사용자의 작업은 파일 자체에만 영향을 줍니다.</span><span class="sxs-lookup"><span data-stu-id="b90c7-111">In the SharePoint File schema, the acting user's action only affects the file itself.</span></span> <span data-ttu-id="b90c7-112">사용자 A가 파일을 여는 경우, **Fileaccessed** 한 이벤트에서 필요한 정보는 작업 중인 사용자입니다.</span><span class="sxs-lookup"><span data-stu-id="b90c7-112">When User A opens a file, the only information needed in the **FileAccessed** event is the acting user.</span></span> <span data-ttu-id="b90c7-113">이러한 차이를 해결 하기 위해 *SharePoint 공유 스키마*라고 하는 별도의 스키마를 통해 공유 이벤트에 대 한 추가 정보를 캡처할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b90c7-113">To address this difference, there is a separate schema, called the  *SharePoint Sharing schema*, that captures more information about sharing events.</span></span> <span data-ttu-id="b90c7-114">이를 통해 관리자는 리소스를 공유 하는 사용자와 리소스를 공유 하는 사람을 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b90c7-114">This ensures that administrators have visibility into who shared a resource and the user the resource was shared with.</span></span> 
  
<span data-ttu-id="b90c7-115">공유 스키마는 공유 이벤트와 관련 된 감사 레코드에 두 개의 필드를 추가로 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="b90c7-115">The Sharing schema provides two additional fields in an audit record related to sharing events:</span></span> 
  
- <span data-ttu-id="b90c7-116">**TargetUserOrGroupType:** 대상 사용자 또는 그룹이 Member, Guest, SharePointGroup, SecurityGroup 또는 Partner 인지를 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="b90c7-116">**TargetUserOrGroupType:** Identifies whether the target user or group is a Member, Guest, SharePointGroup, SecurityGroup, or Partner.</span></span>

- <span data-ttu-id="b90c7-117">**Targetuserorgroupname:** 리소스를 공유 하는 대상 사용자 또는 그룹의 UPN 이나 이름을 저장 합니다 (이전 예제에서는 User B).</span><span class="sxs-lookup"><span data-stu-id="b90c7-117">**TargetUserOrGroupName:** Stores the UPN or name of the target user or group that a resource was shared with (User B in the previous example).</span></span> 

<span data-ttu-id="b90c7-118">이러한 두 필드는 사용자, 작업 및 날짜와 같은 Office 365 감사 로그 스키마의 다른 속성 외에, *누가 누구* 에 게 *어떤* 리소스를 공유 \*\* 하는지를 알려 줄 수 있습니다. \*\*</span><span class="sxs-lookup"><span data-stu-id="b90c7-118">These two fields, in addition to other properties from the Office 365 audit log schema such as User, Operation, and Date can tell the full story about  *which*  user shared  *what*  resource with  *whom*  and  *when*.</span></span> 
  
<span data-ttu-id="b90c7-119">공유 스토리에 중요 한 또 다른 스키마 속성이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b90c7-119">There's another schema property that's important to the sharing story.</span></span> <span data-ttu-id="b90c7-120">감사 로그 검색 결과를 내보낼 때 내보낸 CSV 파일의 **Auditdata** 열에는 공유 이벤트에 대 한 정보가 저장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b90c7-120">When you export audit log search results, the **AuditData** column in the exported CSV file stores information about sharing events.</span></span> <span data-ttu-id="b90c7-121">예를 들어 사용자가 다른 사용자와 사이트를 공유 하는 경우이 작업을 수행 하려면 SharePoint 그룹에 대상 사용자를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="b90c7-121">For example, when a user shares a site with another user, this is accomplished by adding the target user to a SharePoint group.</span></span> <span data-ttu-id="b90c7-122">**Auditdata** 열은 관리자에 게 컨텍스트를 제공 하기 위해이 정보를 캡처합니다.</span><span class="sxs-lookup"><span data-stu-id="b90c7-122">The **AuditData** column captures this information to provide context for administrators.</span></span> <span data-ttu-id="b90c7-123">**Auditdata** 열에서 정보를 구문 분석 하는 방법에 대 한 지침은 [2 단계](#step-2-use-the-powerquery-editor-to-format-the-exported-audit-log) 를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="b90c7-123">See [Step 2](#step-2-use-the-powerquery-editor-to-format-the-exported-audit-log) for instructions on how to parse the information in the **AuditData** column.</span></span>

## <a name="sharepoint-sharing-events"></a><span data-ttu-id="b90c7-124">SharePoint 공유 이벤트</span><span class="sxs-lookup"><span data-stu-id="b90c7-124">SharePoint sharing events</span></span>

<span data-ttu-id="b90c7-125">공유는 사용자 (작업 중인 사용자)가 \*\* 다른 사용자 ( *대상* 사용자)와 리소스를 공유 하려고 할 때 정의 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b90c7-125">Sharing is defined by when a user (the *acting* user) wants to share a resource with another user (the *target* user).</span></span> <span data-ttu-id="b90c7-126">외부 사용자 (조직 외부에 있고 조직의 Azure Active Directory에 게스트 계정이 없는 사용자)를 사용 하 여 리소스를 공유 하는 것과 관련 된 감사 레코드는 다음 이벤트 (Office 365에 기록 됨)로 식별 됩니다. 감사 로그:</span><span class="sxs-lookup"><span data-stu-id="b90c7-126">Audit records related to sharing a resource with an external user (a user who is outside of your organization and doesn't have a guest account in your organization's Azure Active Directory) are identified by the following events, which are logged in the Office 365 audit log:</span></span>

- <span data-ttu-id="b90c7-127">**SharingInvitationCreated:** 조직의 사용자가 외부 사용자와 리소스 (아마도 사이트)를 공유 하려고 했습니다.</span><span class="sxs-lookup"><span data-stu-id="b90c7-127">**SharingInvitationCreated:** A user in your organization tried to share a resource (likely a site) with an external user.</span></span> <span data-ttu-id="b90c7-128">이로 인해 외부 공유 초대가 대상 사용자에 게 전송 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b90c7-128">This results in an external sharing invitation sent to the target user.</span></span> <span data-ttu-id="b90c7-129">이때 리소스에 대 한 액세스 권한이 부여 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b90c7-129">No access to the resource is granted at this point.</span></span>

- <span data-ttu-id="b90c7-130">**SharingInvitationAccepted:** 외부 사용자가 작동 중인 사용자가 보낸 공유 초대를 수락 했으며 이제 해당 리소스에 액세스할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b90c7-130">**SharingInvitationAccepted:** The external user has accepted the sharing invitation sent by the acting user and now has access to the resource.</span></span>

- <span data-ttu-id="b90c7-131">**AnonymousLinkCreated:** 리소스에 대 한 익명 링크 ("모든 사용자" 링크 라고도 함)가 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="b90c7-131">**AnonymousLinkCreated:** An anonymous link (also called an "Anyone" link) is created for a resource.</span></span> <span data-ttu-id="b90c7-132">익명 링크를 만들고 복사할 수 있으므로 익명 링크가 포함 된 모든 문서가 대상 사용자와 공유 된 것으로 가정 하는 것이 합리적입니다.</span><span class="sxs-lookup"><span data-stu-id="b90c7-132">Because an anonymous link can be created and then copied, it's reasonable to assume that any document that has an anonymous link has been shared with a target user.</span></span>

- <span data-ttu-id="b90c7-133">**AnonymousLinkUsed:** 이름에서 알 수 있듯이이 이벤트는 익명 링크를 사용 하 여 리소스에 액세스할 때 기록 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b90c7-133">**AnonymousLinkUsed:** As the name implies, this event is logged when an anonymous link is used to access a resource.</span></span> 

- <span data-ttu-id="b90c7-134">**Securelinkcreated:** 사용자가 특정 사람과 리소스를 공유 하기 위한 "특정 사용자 링크"를 만든 경우</span><span class="sxs-lookup"><span data-stu-id="b90c7-134">**SecureLinkCreated:** A user has created a "specific people link" to share a resource with a specific person.</span></span> <span data-ttu-id="b90c7-135">이 대상 사용자는 조직 외부에 있는 사람도 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b90c7-135">This target user may be someone who is external to your organization.</span></span>

- <span data-ttu-id="b90c7-136">**Ad이상 Tosecurelink:** 사용자가 특정 사람 링크에 추가 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="b90c7-136">**AddedToSecureLink:** A user was added to a specific people link.</span></span> <span data-ttu-id="b90c7-137">이 대상 사용자는 조직 외부에 있는 사람도 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b90c7-137">This target user may be someone who is external to your organization.</span></span>

## <a name="sharing-auditing-work-flow"></a><span data-ttu-id="b90c7-138">감사 작업 흐름 공유</span><span class="sxs-lookup"><span data-stu-id="b90c7-138">Sharing auditing work flow</span></span>
  
<span data-ttu-id="b90c7-139">사용자 (작업 중인 사용자)가 다른 사용자 (대상 사용자)와 리소스를 공유 하려는 경우 먼저 SharePoint (또는 비즈니스용 OneDrive)가 대상 사용자의 전자 메일 주소가 조직의 디렉터리에 있는 사용자 계정과 이미 연결 되어 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="b90c7-139">When a user (the acting user) wants to share a resource with another user (the target user), SharePoint (or OneDrive for Business) first checks if the email address of the target user is already associated with a user account in the organization's directory.</span></span> <span data-ttu-id="b90c7-140">대상 사용자가 디렉터리에 있고 해당 게스트 사용자 계정이 있는 경우 SharePoint에서는 다음과 같은 작업을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="b90c7-140">If the target user is in the directory (and has a corresponding guest user account), SharePoint does the following things:</span></span>
  
-  <span data-ttu-id="b90c7-141">는 대상 사용자를 적절 한 SharePoint 그룹에 추가 하 여 리소스에 액세스할 수 있는 권한을 즉시 할당 하 고 Ad연결 된 **Togroup** 이벤트를 기록 합니다.</span><span class="sxs-lookup"><span data-stu-id="b90c7-141">Immediately assigns the target user permissions to access the resource by adding the target user to the appropriate SharePoint group, and logs an **AddedToGroup** event.</span></span> 
    
- <span data-ttu-id="b90c7-142">대상 사용자의 전자 메일 주소로 공유 알림을 보냅니다.</span><span class="sxs-lookup"><span data-stu-id="b90c7-142">Sends a sharing notification to the email address of the target user.</span></span>
    
- <span data-ttu-id="b90c7-143">**SharingSet** 이벤트를 기록 합니다.</span><span class="sxs-lookup"><span data-stu-id="b90c7-143">Logs a **SharingSet** event.</span></span> <span data-ttu-id="b90c7-144">이 이벤트에는 감사 로그 검색 도구의 활동 선택기에서 **공유 및 액세스 요청 작업** 의 "공유 파일, 폴더 또는 사이트" 라는 이름이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b90c7-144">This event has a friendly name of "Shared file, folder, or site" under **Sharing and access request activities** in the activities picker of the audit log search tool.</span></span> <span data-ttu-id="b90c7-145">[1 단계](#step-1-search-for-sharing-events-and-export-the-results-to-a-csv-file)에 있는 스크린샷를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="b90c7-145">See the screenshot in [Step 1](#step-1-search-for-sharing-events-and-export-the-results-to-a-csv-file).</span></span> 
    
<span data-ttu-id="b90c7-146">대상 사용자에 대 한 사용자 계정이 디렉터리에 없는 경우 SharePoint는 다음을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="b90c7-146">If a user account for the target user isn't in the directory, SharePoint does the following:</span></span> 
    
   - <span data-ttu-id="b90c7-147">리소스를 공유 하는 방법에 따라 다음 이벤트 중 하나를 기록 합니다.</span><span class="sxs-lookup"><span data-stu-id="b90c7-147">Logs one of the following events, based on how the resource is shared:</span></span>
   
      - <span data-ttu-id="b90c7-148">**AnonymousLinkCreated**</span><span class="sxs-lookup"><span data-stu-id="b90c7-148">**AnonymousLinkCreated**</span></span>
   
      - <span data-ttu-id="b90c7-149">**SecureLinkCreated**</span><span class="sxs-lookup"><span data-stu-id="b90c7-149">**SecureLinkCreated**</span></span>
   
      - <span data-ttu-id="b90c7-150">**Ad이상 Tosecurelink**</span><span class="sxs-lookup"><span data-stu-id="b90c7-150">**AddedToSecureLink**</span></span> 

      - <span data-ttu-id="b90c7-151">**SharingInvitationCreated** (이 이벤트는 공유 리소스가 사이트인 경우에만 기록 됨)</span><span class="sxs-lookup"><span data-stu-id="b90c7-151">**SharingInvitationCreated** (this event is logged only when the shared resource is a site)</span></span>
    
   - <span data-ttu-id="b90c7-152">대상 사용자가 초대의 링크를 클릭 하 여 전송 된 공유 초대를 수락 하면 SharePoint에서 **SharingInvitationAccepted** 이벤트를 기록 하 고 리소스에 액세스 하기 위한 대상 사용자 권한을 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="b90c7-152">When the target user accepts the sharing invitation that's sent to them (by clicking the link in the invitation), SharePoint logs a **SharingInvitationAccepted** event and assigns the target user permissions to access the resource.</span></span> <span data-ttu-id="b90c7-153">대상 사용자에 게 익명 링크가 전송 되는 경우 대상 사용자가 링크를 사용 하 여 해당 리소스에 액세스 한 후 **AnonymousLinkUsed** 이벤트가 기록 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b90c7-153">If the target user is sent an anonymous link, the **AnonymousLinkUsed** event is logged after the target user uses the link to access the resource.</span></span> <span data-ttu-id="b90c7-154">보안 링크의 경우에 \*\*\*\* 는 외부 사용자가 링크를 사용 하 여 리소스에 액세스할 때 파일에 액세스 한 이벤트가 기록 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b90c7-154">For secure links, a **FileAccessed** event is logged when an external user uses the link to access the resource.</span></span>

<span data-ttu-id="b90c7-155">초대 하는 사용자의 id 및 초대를 실제로 수락 하는 사용자와 같은 대상 사용자에 대 한 추가 정보도 로깅됩니다.</span><span class="sxs-lookup"><span data-stu-id="b90c7-155">Additional information about the target user is also logged, such as the identity of the user that the invitation is to and the user who actually accepts the invitation.</span></span> <span data-ttu-id="b90c7-156">경우에 따라 이러한 사용자 또는 전자 메일 주소는 다를 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b90c7-156">In some case, these users (or email addresses) can be different.</span></span> 

## <a name="how-to-identify-resources-shared-with-external-users"></a><span data-ttu-id="b90c7-157">외부 사용자와 공유 된 리소스를 확인 하는 방법</span><span class="sxs-lookup"><span data-stu-id="b90c7-157">How to identify resources shared with external users</span></span>

<span data-ttu-id="b90c7-158">관리자에 대 한 일반적인 요구 사항에는 조직 외부의 사용자와 공유 된 모든 리소스의 목록이 작성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b90c7-158">A common requirement for administrators is creating a list of all resources that have been shared with users outside of the organization.</span></span> <span data-ttu-id="b90c7-159">관리자는 Office 365의 공유 감사를 사용 하 여이 목록을 생성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b90c7-159">By using sharing auditing in Office 365, administrators can generate this list.</span></span> <span data-ttu-id="b90c7-160">이 작업을 수행하는 방법은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="b90c7-160">Here's how.</span></span>
  
### <a name="step-1-search-for-sharing-events-and-export-the-results-to-a-csv-file"></a><span data-ttu-id="b90c7-161">1 단계: 공유 이벤트 검색 및 결과를 CSV 파일로 내보내기</span><span class="sxs-lookup"><span data-stu-id="b90c7-161">Step 1: Search for sharing events and export the results to a CSV file</span></span>

<span data-ttu-id="b90c7-162">첫 번째 단계는 공유 이벤트에 대 한 Office 365 감사 로그를 검색 하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="b90c7-162">The first step is to search the Office 365 audit log for sharing events.</span></span> <span data-ttu-id="b90c7-163">감사 로그 검색에 대 한 자세한 내용 (필요한 권한 포함)은 [Security & 준수 센터에서 감사 로그 검색](search-the-audit-log-in-security-and-compliance.md)을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="b90c7-163">For more information (including the required permissions) about searching the audit log, see [Search the audit log in the Security & Compliance Center](search-the-audit-log-in-security-and-compliance.md).</span></span>
  
1. <span data-ttu-id="b90c7-164">[https://protection.office.com](https://protection.office.com)으로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="b90c7-164">Go to [https://protection.office.com](https://protection.office.com).</span></span>
    
2. <span data-ttu-id="b90c7-165">회사 또는 학교 계정을 사용하여 Office 365에 로그인합니다.</span><span class="sxs-lookup"><span data-stu-id="b90c7-165">Sign in to Office 365 using your work or school account.</span></span>
    
3. <span data-ttu-id="b90c7-166">보안 & 준수 센터의 왼쪽 창에서 **검색**  > **감사 로그 검색**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="b90c7-166">In the left pane of the Security & Compliance Center, click **Search**  > **Audit log search**.</span></span>
    
    <span data-ttu-id="b90c7-167">**감사 로그 검색** 페이지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b90c7-167">The **Audit log search** page is displayed.</span></span> 
    
4. <span data-ttu-id="b90c7-168">**활동**아래에서 **공유 및 액세스 요청 활동** 을 클릭 하 여 공유 관련 이벤트를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="b90c7-168">Under **Activities**, click **Sharing and access request activities** to search for sharing-related events.</span></span> 
    
    ![활동 아래에서 공유 및 액세스 요청 작업을 선택 합니다.](media/46bb25b7-1eb2-4adf-903a-cc9ab58639f9.png)
  
5.  <span data-ttu-id="b90c7-170">날짜 및 시간 범위를 선택 하 여 해당 기간 내에 발생 한 공유 이벤트를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="b90c7-170">Select a date and time range to find the sharing events that occurred within that period.</span></span> 
    
6. <span data-ttu-id="b90c7-171">검색 \*\*\*\* 을 클릭 하 여 검색을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="b90c7-171">Click **Search** to run the search.</span></span> 
    
7. <span data-ttu-id="b90c7-172">검색 실행이 완료 되 고 결과가 표시 되 면 결과 **내보내기** \> **모든 결과 다운로드**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="b90c7-172">When the search is finished running and the results are displayed, click **Export results** \> **Download all results**.</span></span>
    
    <span data-ttu-id="b90c7-173">내보내기 옵션을 선택한 후에는 CSV 파일을 열거나 저장 하 라는 메시지가 창 맨 아래에 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b90c7-173">After you select the export option, a message is displayed at the bottom of the window that prompts you to open or save the CSV file.</span></span>
    
8. <span data-ttu-id="b90c7-174">다른 \*\*\*\* \> **이름으로 저장** 저장을 클릭 하 고 로컬 컴퓨터의 폴더에 CSV 파일을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="b90c7-174">Click **Save** \> **Save as** and save the CSV file to a folder on your local computer.</span></span> 

### <a name="step-2-use-the-powerquery-editor-to-format-the-exported-audit-log"></a><span data-ttu-id="b90c7-175">2 단계: PowerQuery Editor를 사용 하 여 내보낸 감사 로그의 서식 지정</span><span class="sxs-lookup"><span data-stu-id="b90c7-175">Step 2: Use the PowerQuery Editor to format the exported audit log</span></span>

<span data-ttu-id="b90c7-176">다음 단계에서는 Excel의 파워 쿼리 편집기에서 JSON 변환 기능을 사용 하 여 **Auditdata** 열의 각 속성 (다중 속성 JSON 개체로 구성)을 자체 열로 분할 합니다.</span><span class="sxs-lookup"><span data-stu-id="b90c7-176">The next step is to use the JSON transform feature in the Power Query Editor in Excel to split each property in the **AuditData** column (which consists of a multi-property JSON object) into its own column.</span></span> <span data-ttu-id="b90c7-177">이렇게 하면 열을 필터링 하 여 공유와 관련 된 레코드를 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b90c7-177">This lets you filter columns to view records related to sharing</span></span>

<span data-ttu-id="b90c7-178">단계별 지침은 [Export, configure 및 view audit log records](export-view-audit-log-records.md#step-2-format-the-exported-audit-log-using-the-power-query-editor)에서 "2 단계: 검색 된 감사 로그를 Power Query Editor를 사용 하 여 서식 지정"을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="b90c7-178">For step-by-step instructions, see "Step 2: Format the exported audit log using the Power Query Editor" in [Export, configure, and view audit log records](export-view-audit-log-records.md#step-2-format-the-exported-audit-log-using-the-power-query-editor).</span></span>

### <a name="step-3-filter-the-csv-file-for-resources-shared-with-external-users"></a><span data-ttu-id="b90c7-179">3 단계: 외부 사용자와 공유 되는 리소스에 대 한 CSV 파일 필터링</span><span class="sxs-lookup"><span data-stu-id="b90c7-179">Step 3: Filter the CSV file for resources shared with external users</span></span>

<span data-ttu-id="b90c7-180">다음 단계에서는 이전에 [SharePoint 공유 이벤트](#sharepoint-sharing-events) 섹션에서 설명한 서로 다른 공유 관련 이벤트에 대 한 CSV를 필터링 합니다.</span><span class="sxs-lookup"><span data-stu-id="b90c7-180">The next step is to filter the CSV for the different sharing-related events that were previously described in the [SharePoint sharing events](#sharepoint-sharing-events) section.</span></span> <span data-ttu-id="b90c7-181">또는 **TargetUserOrGroupType** 열을 필터링 하 여이 속성의 값이 **Guest**인 모든 레코드를 표시할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b90c7-181">Alternatively, you can filter the **TargetUserOrGroupType** column to display all records where the value of this property is **Guest**.</span></span> 

<span data-ttu-id="b90c7-182">이전 단계의 지침에 따라 PowerQuery editor를 사용 하 여 CSV 파일을 준비한 후에 다음을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="b90c7-182">After you've followed the instructions in the previous step to prepare the CSV file by using the PowerQuery editor, do the following:</span></span>
    
1. <span data-ttu-id="b90c7-183">2 단계에서 만든 Excel 파일을 엽니다.</span><span class="sxs-lookup"><span data-stu-id="b90c7-183">Open the Excel file that you created in Step 2.</span></span> 

2. <span data-ttu-id="b90c7-184">**홈** 탭에서 **정렬 & 필터**를 클릭 하 고 **필터**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="b90c7-184">On the **Home** tab, click **Sort & Filter**, and then click **Filter**.</span></span>
    
3. <span data-ttu-id="b90c7-185">**작업** 열의 **정렬 & 필터** 드롭다운 목록에서 모든 선택을 취소 하 고 다음 공유 관련 이벤트를 하나 이상 선택 하 고 **확인**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="b90c7-185">In the **Sort & Filter** dropdown list on the **Operations** column, clear all selections, then select one or more the following sharing-related events and then click **Ok**.</span></span>
 
   - <span data-ttu-id="b90c7-186">**SharingInvitationCreated**</span><span class="sxs-lookup"><span data-stu-id="b90c7-186">**SharingInvitationCreated**</span></span>
   
   - <span data-ttu-id="b90c7-187">**AnonymousLinkCreated**</span><span class="sxs-lookup"><span data-stu-id="b90c7-187">**AnonymousLinkCreated**</span></span>
   
   - <span data-ttu-id="b90c7-188">**SecureLinkCreated**</span><span class="sxs-lookup"><span data-stu-id="b90c7-188">**SecureLinkCreated**</span></span>
   
   - <span data-ttu-id="b90c7-189">**Ad이상 Tosecurelink**</span><span class="sxs-lookup"><span data-stu-id="b90c7-189">**AddedToSecureLink**</span></span> 
    
    <span data-ttu-id="b90c7-190">선택한 이벤트에 대 한 행이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b90c7-190">Excel displays the rows for the events you selected.</span></span>
    
4. <span data-ttu-id="b90c7-191">**TargetUserOrGroupType** 라는 열로 이동 하 여 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="b90c7-191">Go to the column named **TargetUserOrGroupType** and select it.</span></span> 
    
5. <span data-ttu-id="b90c7-192">**정렬 & 필터** 드롭다운 목록에서 모든 선택을 취소 하 고 **TargetUserOrGroupType: Guest**를 선택한 다음 **확인**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="b90c7-192">In the **Sort & Filter** dropdown list, clear all selections, then select **TargetUserOrGroupType:Guest**, and click **Ok**.</span></span>
    
    <span data-ttu-id="b90c7-193">이제 외부 사용자는 **TargetUserOrGroupType: Guest**값으로 식별 되므로 공유 이벤트 및 대상 사용자가 조직 외부에 있는 위치에 대 한 행이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b90c7-193">Now Excel displays the rows for sharing events AND where the target user is outside of your organization, because external users are identified by the value **TargetUserOrGroupType:Guest**.</span></span> 
  
> [!TIP]
> <span data-ttu-id="b90c7-194">표시 되는 감사 레코드의 경우 **ObjectId** 열은 대상 사용자와 공유 된 리소스를 식별 합니다. 예를 `ObjectId:https:\/\/contoso-my.sharepoint.com\/personal\/sarad_contoso_com\/Documents\/Southwater Proposal.docx`들어</span><span class="sxs-lookup"><span data-stu-id="b90c7-194">For the audit records that are displayed, the **ObjectId** column identifies the resource that was shared with the target user; for example  `ObjectId:https:\/\/contoso-my.sharepoint.com\/personal\/sarad_contoso_com\/Documents\/Southwater Proposal.docx`.</span></span>
