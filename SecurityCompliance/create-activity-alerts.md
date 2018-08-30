---
title: Office 365 보안에서 작업 알림 만들기 &amp; 준수 센터
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 11/7/2017
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MED150
- BCS160
- MET150
ms.assetid: 72bbad69-035b-4d33-b8f4-549a2743e97d
description: 추가 하 고 보안에서 작업 알림 관리 &amp; 준수 센터는 Office 365 사용자에 게 되므로 사용자는 Office 365의 특정 작업을 수행할 때 알림을으로 전자 메일을 합니다.
ms.openlocfilehash: 409c1ff4c7fdd0d2d071bdb2eab08ec49357ed8a
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22533891"
---
# <a name="create-activity-alerts-in-the-office-365-security-amp-compliance-center"></a><span data-ttu-id="f6c95-103">Office 365 보안에서 작업 알림 만들기 &amp; 준수 센터</span><span class="sxs-lookup"><span data-stu-id="f6c95-103">Create activity alerts in the Office 365 Security &amp; Compliance Center</span></span>

<span data-ttu-id="f6c95-p101">사용자에 게 알림 전자 메일 사용자가 Office 365의 특정 작업을 수행 하는 활동 알림을 만들 수 있습니다. 작업 알림 권장 사항과 비슷합니다 Office 365 감사 로그에 이벤트를 검색 하 때 사용자에 대 한 알림을 만든 활동에 대 한 이벤트 전자 메일 메시지를 전송 하는 점을 제외 하면 발생 합니다.</span><span class="sxs-lookup"><span data-stu-id="f6c95-p101">You can create an activity alert that will send you an email notification when users perform specific activities in Office 365. Activity alerts are similar to searching for events in the Office 365 audit log, except that you'll be sent an email message when an event for an activity that you've created an alert for happens.</span></span> 
  
 <span data-ttu-id="f6c95-p102">**감사 로그를 검색 하는 대신 작업 알림을 사용 하는 이유?** 특정 한 종류의 작업이 나 정말에 대 한 확인 하려는 특정 사용자에 의해 수행 되는 활동 있을 수 있습니다. 이러한 작업에 대 한 감사 로그를 검색 하려면 기억 하는 대신 Office 365 사용자에 게 보낼 전자 메일 메시지를 사용자가 이러한 작업을 수행 해야할 작업 알림을 사용할 수 있습니다. 예, SharePoint에서 파일을 삭제 하는 사용자 또는 사용자가 사서함에서 메시지를 영구적으로 삭제 하는 경우 알림을 생성 하는 경고를 만들 수 있는 경우 알림을 생성 하는 활동 경고를 만들 수 있습니다. 사용자가 보낸 전자 메일 알림 어떤 작업을 수행한 및 것을 수행한 사용자에 대 한 정보를 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="f6c95-p102">**Why use activity alerts instead of searching the audit log?** There might be certain kinds of activity or activity performed by specific users that you really want to know about. Instead of having to remember to search the audit log for those activities, you can use activity alerts to have Office 365 send you an email message when users perform those activities. For example, you can create an activity alert to notify you when a user deletes files in SharePoint or you can create an alert to notify you when a user permanently deletes messages from their mailbox. The email notification sent to you includes information about which activity was performed and the user who performed it.</span></span> 
  
## <a name="before-you-begin"></a><span data-ttu-id="f6c95-111">시작하기 전에</span><span class="sxs-lookup"><span data-stu-id="f6c95-111">Before you begin</span></span>

- <span data-ttu-id="f6c95-p103">보안에서 조직 구성 역할 할당 되어야 합니다 &amp; 준수 센터 활동 알림을 관리할 수 있습니다. 기본적으로이 역할은 규정 준수 관리자 및 조직 관리 역할 그룹에 할당 됩니다. 역할 그룹에 구성원을 추가 하는 방법에 대 한 자세한 내용은 참조 [Office 365 보안에 사용자가 액세스할 수 있도록 &amp; 준수 센터](grant-access-to-the-security-and-compliance-center.md)합니다.</span><span class="sxs-lookup"><span data-stu-id="f6c95-p103">You must be assigned the Organization Configuration role in the Security &amp; Compliance Center to manage activity alerts. By default, this role is assigned to the Compliance Administrator and Organization Management role groups. For more information about adding members to role groups, see [Give users access to the Office 365 Security &amp; Compliance Center](grant-access-to-the-security-and-compliance-center.md).</span></span>
    
- <span data-ttu-id="f6c95-p104">사용자 (또는 다른 관리자) 해야 먼저에서 로깅 기능 설정 감사 조직에 대 한 작업 경고를 사용 하 여를 시작할 수 있습니다. 이 작업을 수행 방금 **활동 알림** 페이지에서 **사용자 및 관리자 작업을 녹음/녹화 시작** 을 클릭 합니다. (이 링크 보이지 않으면 감사가 이미 설정 되어 조직에 대 한.) 보안에서 **감사 로그 검색** 페이지에 대 한 감사 켤 수도 있습니다 &amp; 준수 센터 (이동 **검색 &amp; 조사** \> **감사 로그 검색**). 조직에 대해 한번씩이 작업을 수행 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="f6c95-p104">You (or another admin) must first turn on audit logging for your organization before you can start using activity alerts. To do this, just click **Start recording user and admin activity** on the **Activity alerts** page. (If you don't see this link, auditing has already been turned on for your organization.) You can also turn on auditing on the **Audit log search** page in the Security &amp; Compliance Center (go to **Search &amp; investigation** \> **Audit log search**). You only have to do this once for your organization.</span></span>
    
- <span data-ttu-id="f6c95-p105">**알림** 페이지를 사용 하 여 보안에서 수 &amp; 준수 센터 조직의 주소록에 나열 된 사용자에 의해 수행 되는 작업에 대해서만 알림을 만들 수 있습니다. 이 페이지를 사용 하 여 외부 사용자에 의해 수행 되는 활동에 대 한 알림을 만들 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="f6c95-p105">You can use the **Alerts** page in the Security &amp; Compliance Center to create alerts only for activity performed by users who are listed in your organization's address book. You can't use this page to create alerts for activity performed by external users.</span></span> 
    
- <span data-ttu-id="f6c95-121">[자세한 내용은](#more-information) 참조 일반적인 시나리오 (및 모니터링할 특정 활동)의 목록에 대 한 섹션에 대 한 경고를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f6c95-121">See the [More information](#more-information) section for a list of common scenarios (and the specific activity to monitor) that you can create alerts for.</span></span> 
    
- <span data-ttu-id="f6c95-122">Office 365 감사 로그에서 검색할 수 있는 동일한 활동에 대 한 알림을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f6c95-122">You can create alerts for the same activities that you can search for in the Office 365 audit log.</span></span> 
    
## <a name="create-an-activity-alert"></a><span data-ttu-id="f6c95-123">작업 알림 만들기</span><span class="sxs-lookup"><span data-stu-id="f6c95-123">Create an activity alert</span></span>

1. <span data-ttu-id="f6c95-124">이동 [https://protection.office.com](https://protection.office.com)합니다.</span><span class="sxs-lookup"><span data-stu-id="f6c95-124">Go to [https://protection.office.com](https://protection.office.com).</span></span>
    
2. <span data-ttu-id="f6c95-125">작업이 나 교육용 계정을 사용 하 여 Office 365에 로그인 합니다.</span><span class="sxs-lookup"><span data-stu-id="f6c95-125">Sign in to Office 365 using your work or school account.</span></span>
    
3. <span data-ttu-id="f6c95-126">왼쪽된 창에서 **알림**을 클릭 한 다음 **관리 경고**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="f6c95-126">In the left pane, click **Alerts**, and then click **Manage alerts**.</span></span>
    
4. <span data-ttu-id="f6c95-127">**작업 알림** 페이지에서 **알림을 추가**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="f6c95-127">On the **Activity alerts** page, click **Add an alert**.</span></span>
    
    ![작업 알림 추가](media/53888bd5-9fa2-4398-8ccc-1a9dc72517ac.png)
  
5. <span data-ttu-id="f6c95-129">경고를 만들려면 다음 필드에 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="f6c95-129">Complete the following fields to create an alert:</span></span>
    
    <span data-ttu-id="f6c95-p106">a. **이름** -경고에 대 한 이름을 입력 합니다. 경고 이름은 조직 내에서 고유 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="f6c95-p106">a. **Name** - Type a name for the alert. Alert names must be unique within your organization.</span></span>
    
    <span data-ttu-id="f6c95-p107">b. **설명** (선택 사항)-활동 및 추적 되 고 있는 사용자와 같은 경고에 설명 하 고 알림 전자 메일을 하는 사용자가 전송 됩니다. 이 경고를 다른 관리자의 용도 설명 하기 위해 쉽고 빠르게를 제공 하는 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="f6c95-p107">b. **Description** (Optional) - Describe the alert, such as the activities and users being tracked, and the users that email notifications are sent to. Descriptions provide a quick and easy way to describe the purpose of the alert to other admins.</span></span>
    
    <span data-ttu-id="f6c95-p108">c. **될 때이 경고 보내기** -클릭 **될 때이 경고 보내기** 다음 두 필드를 구성 하 고 합니다.</span><span class="sxs-lookup"><span data-stu-id="f6c95-p108">c. **Send this alert when** - Click **Send this alert when** and then configure these two fields:</span></span>
    
    - <span data-ttu-id="f6c95-p109">**활동** -에 대 한 알림을 만들 수 있는 작업을 표시 하는 드롭다운 목록을 클릭 합니다. Office 365 감사 로그를 검색 하는 경우 표시 되는 동일한 활동 목록입니다. 하나 이상의 특정 작업을 선택할 수 또는 그룹의 모든 작업을 선택 하려면 작업 그룹 이름을 클릭 수 있습니다. 이러한 작업에 대 한 [Office 365 보안 및 규정 준수 센터에서 감사 로그 검색](search-the-audit-log-in-security-and-compliance.md#audited-activities)에 "작업 감사" 섹션을 참조 하십시오. 사용자가 경고에 추가한 작업 중 하나를 수행 하는 경우에 전자 메일 알림이 전송 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f6c95-p109">**Activities** - Click the drop-down list to display the activities that you can create an alert for. This is the same activities list that's displayed when you search the Office 365 audit log. You can select one or more specific activities or you can click the activity group name to select all activities in the group. For a description of these activities, see the "Audited activities" section in [Search the audit log in the Office 365 Security & Compliance Center](search-the-audit-log-in-security-and-compliance.md#audited-activities). When a user performs any of the activities that you've added to the alert, an email notification is sent.</span></span> 
    
     - <span data-ttu-id="f6c95-p110">**사용자가** -이 상자를 클릭 하 고 하나 이상의 사용자를 선택 합니다. 이 상자에 사용자가 **활동** 상자에 추가 하는 작업을 수행 하는 경우 알림이 전송 됩니다. 조직에서 모든 사용자 경고로 지정 된 작업을 수행 하는 경우 알림을 보낼 하려면 **사용자가** 상자를 비워둡니다.</span><span class="sxs-lookup"><span data-stu-id="f6c95-p110">**Users** - Click this box and then select one or more users. If the users in this box perform the activities that you added to the **Activities** box, an alert will be sent. Leave the **Users** box blank to send an alert when any user in your organization performs the activities specified by the alert.</span></span> 
    
    <span data-ttu-id="f6c95-p111">**이 경고를 보내도록** -d.이 **이 경고 보내기**를 클릭 하 고 다음 **받는 사람** 상자에서를 클릭 하 고 ( **사용자** 상자에 지정 된) 사용자 활동을 수행할 때 전자 메일 알림의 받을 사용자를 추가 하는 이름을 입력 (에 지정 된 **활동** 상자)입니다. 참고 기본적으로 받는 사람 목록에 추가 됩니다. 이 목록에서 사용자 이름을 제거할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f6c95-p111">d. **Send this alert to** - Click **Send this alert**, and then click in the **Recipients** box and type a name to add a users who will receive an email notification when a user (specified in the **Users** box) performs an activity (specified in the **Activities** box). Note that you are added to the list of recipients by default. You can remove your name from this list.</span></span>
    
6. <span data-ttu-id="f6c95-150">경고를 만들려면 **저장** 을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="f6c95-150">Click **Save** to create the alert.</span></span> 
    
    <span data-ttu-id="f6c95-151">**작업 알림** 페이지의 목록에 새 경고가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f6c95-151">The new alert is displayed in the list on the **Activity alerts** page.</span></span> 
    
    ![작업 알림 페이지의 보안에서 알림 목록이 표시 됩니다 &amp; 준수 센터](media/02b774f2-1719-41de-bbc9-5e5b7576f335.png)
  
    <span data-ttu-id="f6c95-p112">경고의 상태는 **On**으로 설정 됩니다. Note 받는 알림이 전송 될 때 전자 메일 알림을 받은 사람도 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f6c95-p112">The status of the alert is set to **On**. Note that the recipients who will received an email notification when an alert is sent are also listed.</span></span> 
  
## <a name="turn-off-an-activity-alert"></a><span data-ttu-id="f6c95-155">활동 경고 해제</span><span class="sxs-lookup"><span data-stu-id="f6c95-155">Turn off an activity alert</span></span>

<span data-ttu-id="f6c95-p113">전자 메일 알림을 전송 되지 않고 있도록 활동 알림을 해제할 수 있습니다. 작업 경고를 해제 한 후 조직에 대 한 작업 알림 목록에 표시 된 것은 여전히 하 고 해당 속성을 계속 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f6c95-p113">You can turn off an activity alert so that an email notification isn't sent. After you turn off the activity alert, it's still displayed in the list of activity alerts for your organization, and you can still view its properties.</span></span>
  
1. <span data-ttu-id="f6c95-158">이동 [https://protection.office.com](https://protection.office.com)합니다.</span><span class="sxs-lookup"><span data-stu-id="f6c95-158">Go to [https://protection.office.com](https://protection.office.com).</span></span>
    
2. <span data-ttu-id="f6c95-159">작업이 나 교육용 계정을 사용 하 여 Office 365에 로그인 합니다.</span><span class="sxs-lookup"><span data-stu-id="f6c95-159">Sign in to Office 365 using your work or school account.</span></span>
    
3. <span data-ttu-id="f6c95-160">왼쪽된 창에서 **알림**을 클릭 한 다음 **관리 작업 알림**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="f6c95-160">In the left pane, click **Alerts**, and then click **Manage activity alerts**.</span></span>
    
4. <span data-ttu-id="f6c95-161">조직에 대 한 알림 목록의 기능을 해제 하려면 경고를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="f6c95-161">In the list of alerts for your organization, click the alert that you want to turn off.</span></span>
    
5. <span data-ttu-id="f6c95-162">**알림 편집** 페이지 **에서** 설정/해제 스위치 **를 해제**하는 상태를 변경 하려면를 클릭 한 다음 **저장**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="f6c95-162">On the **Edit alert** page, click the **On** toggle switch to change the status to **Off**, and then click **Save**.</span></span>
    
    <span data-ttu-id="f6c95-163">작업 알림 페이지에서 경고의 상태는 **Off**로 설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f6c95-163">The status of the alert on the Activity alerts pages is set to **Off**.</span></span> 
    
<span data-ttu-id="f6c95-164">활동 알림을 다시 설정 하려면 이러한 단계를 반복 하 고 **해제** 토글 전환 **전환**상태를 변경 하려면을 클릭 방금 합니다.</span><span class="sxs-lookup"><span data-stu-id="f6c95-164">To turn an activity alert back on, just repeat these steps and click the **Off** toggle switch to change the status to **On**.</span></span>
  
## <a name="more-information"></a><span data-ttu-id="f6c95-165">추가 정보</span><span class="sxs-lookup"><span data-stu-id="f6c95-165">More information</span></span>

- <span data-ttu-id="f6c95-166">다음은 보안에서 필드 (및 **작업 알림** 페이지에서 아래 나열 된 **받는 사람** )에 경고 Sent에 지정 된 사용자에 게 전송 된 전자 메일 알림 메시지의 한 예 &amp; 준수 센터입니다.</span><span class="sxs-lookup"><span data-stu-id="f6c95-166">Here's an example of the email notification that is sent to the users that are specified in the Sent this alert to field (and listed under **Recipients** on the **Activity alerts** page ) in the Security &amp; Compliance Center.</span></span> 
    
    ![활동 경고에 대 한 전송 하는 전자 메일 notifcation의 예](media/a5f91611-fae6-4fe9-82f5-58521a2e2541.png)
  
- <span data-ttu-id="f6c95-p114">다음은 활동을 만들 수 있는 일부 일반적인 문서 및 전자 메일 활동에 대 한 경고를 보냅니다. 활동,에 대 한 알림을 만들려면 활동의 이름 및 활동 **활동** 드롭다운 목록에 나열 되는 작업 그룹의 이름을 테이블에 설명 합니다. 에 대 한 작업 알림을 만들 수 있는 작업의 전체 목록은 [Office 365 보안 및 규정 준수 센터에서 감사 로그 검색](search-the-audit-log-in-security-and-compliance.md#audited-activities)에 "작업 감사" 섹션을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="f6c95-p114">Here's are some common document and email activities that you can create an activity alerts for. The tables describes the activity, the name of the activity to create an alert for, and the name of the activity group that the activity is listed under in the **Activities** drop-down list. To see a complete list of the activities that you can create activity alerts for, see the "Audited activities" section in [Search the audit log in the Office 365 Security & Compliance Center](search-the-audit-log-in-security-and-compliance.md#audited-activities).</span></span>
    
    > [!TIP]
    > <span data-ttu-id="f6c95-p115">모든 사용자에 의해 수행 되는 하나의 활동에 대 한 작업 알림을 만들려고 할 수 있습니다. 하나 또는 mores에 의해 수행 되는 여러 작업을 추적 하는 활동 경고를 만들려고 할 수 또는 사용자가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f6c95-p115">You might want to create an activity alert for just one activity that's performed by any user. Or you might want to create an activity alert that track multiple activities performed by one or mores users.</span></span> 
  
    <span data-ttu-id="f6c95-173">다음 표에서 SharePoint 또는 비즈니스용 OneDrive의 일반적인 일부 문서 관련 작업을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="f6c95-173">The following table lists some common document-related activities in SharePoint or OneDrive for Business.</span></span>
    
    |<span data-ttu-id="f6c95-174">**사용자가이...**</span><span class="sxs-lookup"><span data-stu-id="f6c95-174">**When a user does this...**</span></span>|<span data-ttu-id="f6c95-175">**이 작업에 대 한 알림 만들기**</span><span class="sxs-lookup"><span data-stu-id="f6c95-175">**Create an alert for this activity**</span></span>|<span data-ttu-id="f6c95-176">**작업 그룹**</span><span class="sxs-lookup"><span data-stu-id="f6c95-176">**Activity group**</span></span>|
    |:-----|:-----|:-----|
    |<span data-ttu-id="f6c95-177">사이트에서 문서를 봅니다.</span><span class="sxs-lookup"><span data-stu-id="f6c95-177">Views a document on a site.</span></span>  <br/> |<span data-ttu-id="f6c95-178">액세스 파일</span><span class="sxs-lookup"><span data-stu-id="f6c95-178">Accessed file</span></span>  <br/> |<span data-ttu-id="f6c95-179">파일 및 폴더 활동</span><span class="sxs-lookup"><span data-stu-id="f6c95-179">File and folder activities</span></span>  <br/> |
    |<span data-ttu-id="f6c95-180">편집 하거나 문서를 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="f6c95-180">Edits or changes a document.</span></span>  <br/> |<span data-ttu-id="f6c95-181">수정 된 파일</span><span class="sxs-lookup"><span data-stu-id="f6c95-181">Modified file</span></span>  <br/> |<span data-ttu-id="f6c95-182">파일 및 폴더 활동</span><span class="sxs-lookup"><span data-stu-id="f6c95-182">File and folder activities</span></span>  <br/> |
    |<span data-ttu-id="f6c95-183">조직 외부의 사용자와 문서를 공유합니다.</span><span class="sxs-lookup"><span data-stu-id="f6c95-183">Shares a document with a user outside of your organization.</span></span>  <br/> |<span data-ttu-id="f6c95-184">파일, 폴더 또는 사이트를 공유 합니다.</span><span class="sxs-lookup"><span data-stu-id="f6c95-184">Share file, folder, or site</span></span>  <br/> <span data-ttu-id="f6c95-185">그리고</span><span class="sxs-lookup"><span data-stu-id="f6c95-185">And</span></span>  <br/> <span data-ttu-id="f6c95-186">공유 초대를 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="f6c95-186">Created sharing invitation</span></span>  <br/> <span data-ttu-id="f6c95-187">자세한 내용은 [Office 365 감사 로그에 감사 공유 사용](use-sharing-auditing.md)을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="f6c95-187">For more information, see [Use sharing auditing in the Office 365 audit log](use-sharing-auditing.md).</span></span>  <br/> |<span data-ttu-id="f6c95-188">공유 및 액세스 요청 활동</span><span class="sxs-lookup"><span data-stu-id="f6c95-188">Sharing and access request activities</span></span>  <br/> |
    |<span data-ttu-id="f6c95-189">업로드 하거나 문서를 다운로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="f6c95-189">Uploads or downloads a document.</span></span>  <br/> |<span data-ttu-id="f6c95-190">업로드 된 파일</span><span class="sxs-lookup"><span data-stu-id="f6c95-190">Uploaded file</span></span>  <br/> <span data-ttu-id="f6c95-191">및/또는</span><span class="sxs-lookup"><span data-stu-id="f6c95-191">And/or</span></span>  <br/> <span data-ttu-id="f6c95-192">다운로드 한 파일</span><span class="sxs-lookup"><span data-stu-id="f6c95-192">Downloaded file</span></span>  <br/> |<span data-ttu-id="f6c95-193">파일 및 폴더 활동</span><span class="sxs-lookup"><span data-stu-id="f6c95-193">File and folder activities</span></span>  <br/> |
    |<span data-ttu-id="f6c95-194">사이트에 대 한 액세스 권한을 변경합니다.</span><span class="sxs-lookup"><span data-stu-id="f6c95-194">Changes the access permissions to a site.</span></span>  <br/> |<span data-ttu-id="f6c95-195">수정 된 사이트 사용 권한</span><span class="sxs-lookup"><span data-stu-id="f6c95-195">Modified site permissions</span></span>  <br/> |<span data-ttu-id="f6c95-196">사이트 관리 작업</span><span class="sxs-lookup"><span data-stu-id="f6c95-196">Site administration activities</span></span>  <br/> |

    <span data-ttu-id="f6c95-197">다음 표에서 Exchange Online의 일반적인 일부 전자 메일 관련 작업을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="f6c95-197">The following table lists some common email-related activities in Exchange Online.</span></span>

    |<span data-ttu-id="f6c95-198">**사용자가이...**</span><span class="sxs-lookup"><span data-stu-id="f6c95-198">**When a user does this...**</span></span>|<span data-ttu-id="f6c95-199">**이 작업에 대 한 알림 만들기**</span><span class="sxs-lookup"><span data-stu-id="f6c95-199">**Create an alert for this activity**</span></span>|<span data-ttu-id="f6c95-200">**작업 그룹**</span><span class="sxs-lookup"><span data-stu-id="f6c95-200">**Activity group**</span></span>|
    |:-----|:-----|:-----|
    |<span data-ttu-id="f6c95-201">영구적으로 삭제 (제거) 전자 메일 메시지의 사서함에서 합니다.</span><span class="sxs-lookup"><span data-stu-id="f6c95-201">Permanently deletes (purges) an email message from their mailbox.</span></span>  <br/> |<span data-ttu-id="f6c95-202">사서함에서 제거 된 메시지</span><span class="sxs-lookup"><span data-stu-id="f6c95-202">Purged messages from mailbox</span></span>  <br/> | <span data-ttu-id="f6c95-203">Exchange 사서함 활동</span><span class="sxs-lookup"><span data-stu-id="f6c95-203">Exchange mailbox activities</span></span>  <br/> |
    |<span data-ttu-id="f6c95-204">공유 사서함에서 전자 메일 메시지를 보냅니다.</span><span class="sxs-lookup"><span data-stu-id="f6c95-204">Sends an email message from a shared mailbox.</span></span>  <br/> |<span data-ttu-id="f6c95-205">다른 사람 이름으로 보내기 권한을 사용 하 여 메시지를 전송 합니다.</span><span class="sxs-lookup"><span data-stu-id="f6c95-205">Sent message using Send As permissions</span></span>  <br/> <span data-ttu-id="f6c95-206">그리고</span><span class="sxs-lookup"><span data-stu-id="f6c95-206">And</span></span>  <br/> <span data-ttu-id="f6c95-207">대신 보내기 권한을 사용 하 여 메시지를 보낸 사람이</span><span class="sxs-lookup"><span data-stu-id="f6c95-207">Sent message using Send On Behalf permissions</span></span>  <br/> | <span data-ttu-id="f6c95-208">Exchange 사서함 활동</span><span class="sxs-lookup"><span data-stu-id="f6c95-208">Exchange mailbox activities</span></span>  <br/> |
   
- <span data-ttu-id="f6c95-p116">보안에서 **새로 만들기 ActivityAlert** 및 **집합 ActivityAlert** cmdlet을 사용할 수도 있습니다 &amp; 준수 센터 PowerShell을 만들고 작업 경고를 편집 합니다. 만들거나 활동 경고를 편집 하려면 이러한 cmdlet을 사용 하는 경우 다음 사항에 주의 유지 합니다.</span><span class="sxs-lookup"><span data-stu-id="f6c95-p116">You can also use the **New-ActivityAlert** and **Set-ActivityAlert** cmdlets in Security &amp; Compliance Center PowerShell to create and edit activity alerts. Keep the following things in mind if you use these cmdlets to create or edit activity alerts:</span></span> 
    
  - <span data-ttu-id="f6c95-211">"이이 경고에 사용자 지정 작업의 선택에 나열 되지 않습니다." 라는 경고에 대 한 속성 페이지에 메시지가 표시 됩니다 **활동** 드롭다운 목록에 나열 되지 않은 경고에 활동을 추가 하는 cmdlet을 사용 하는 경우</span><span class="sxs-lookup"><span data-stu-id="f6c95-211">If you use a cmdlet to add an activity to the alert that isn't listed in the **Activities** drop-down list, a message is displayed in on the property page for the alert that says, "This alert has custom operations not listed in the picker."</span></span> 
    
  - <span data-ttu-id="f6c95-p117">Cmdlet를 사용 하 여 만들거나 활동 경고를 편집 하는 것이 좋습니다 조직 외부에 있는 다른 사람에 게 전자 메일 알림을 보내도록 하는 것입니다. 이 외부 사용자는 경고에 대 한 받는 사람 목록에 나열 됩니다. 알림에서이 외부 사용자를 제거 하는 경우 해당 사용자는 사용할 수 없음 경고에 다시 추가 보안에서 **알림 편집** 페이지를 사용 하 여 &amp; 준수 센터입니다. 다시 **설정 ActivityAlert** cmdlet을 사용 하 여 외부 사용자를 추가 또는 동일한 (또는 다른) 외부 사용자는 새 경고를 추가 하려면 **새로 만들기 ActivityAlert** cmdlet을 사용 하면 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f6c95-p117">A good reason to use the cmdlets to create or edit an activity alert is to send email notifications to someone outside of your organization. This external user will be listed in the list of recipients for the alert. But if you remove this external user from the alert, that user can't be re-added to the alert by using **Edit alert** page in the Security &amp; Compliance Center. You'll have to re-add the external user using the **Set-ActivityAlert** cmdlet, or use the **New-ActivityAlert** cmdlet to add the same (or different) external user to a new alert.</span></span> 
    
  

