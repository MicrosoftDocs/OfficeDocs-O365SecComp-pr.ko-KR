---
title: Office 365에서 제공 된 악성 전자 메일 찾기 및 조사
keywords: TIMailData-Inline, Security 인시던트, 인시던트, ATP PowerShell, 전자 메일 맬웨어, 손상 된 사용자, 전자 메일 피싱, 전자 메일 맬웨어, 읽기 전자 메일 머리글, 읽기 헤더, 공개 전자 메일 헤더
ms.author: deniseb
author: denisebmsft
manager: dansimp
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 8f54cd33-4af7-4d1b-b800-68f8818e5b2a
ms.collection:
- M365-security-compliance
description: 위협 조사 및 응답 기능을 사용 하 여 악성 전자 메일을 찾고 조사 하는 방법에 대해 알아봅니다.
ms.openlocfilehash: a57e72c74a7b2f819ecee7fbf604795e4a094693
ms.sourcegitcommit: 4a2bde56178609e75c1ad7ecad2db5e049fc0c45
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/05/2019
ms.locfileid: "36761684"
---
# <a name="find-and-investigate-malicious-email-that-was-delivered-in-office-365"></a><span data-ttu-id="247f7-104">Office 365에서 제공 된 악성 전자 메일 찾기 및 조사</span><span class="sxs-lookup"><span data-stu-id="247f7-104">Find and investigate malicious email that was delivered in Office 365</span></span>

<span data-ttu-id="247f7-105">[Office 365 Advanced Threat Protection](office-365-atp.md) 을 사용 하면 조직에 사용자를 추가 하 고 조직을 보호 하기 위한 작업을 수행 하는 활동을 조사할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="247f7-105">[Office 365 Advanced Threat Protection](office-365-atp.md) enables you to investigate activities that put people in your organization at risk, and to take action to protect your organization.</span></span> <span data-ttu-id="247f7-106">예를 들어 조직의 보안 팀에 속한 경우 배달 된 의심 스러운 전자 메일 메시지를 찾아서 조사할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="247f7-106">For example, if you are part of your organization's security team, you can find and investigate suspicious email messages that were delivered.</span></span> <span data-ttu-id="247f7-107">[위협 탐색기 (또는 실시간 검색)](threat-explorer.md)를 사용 하 여이 작업을 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="247f7-107">You can do this by using [Threat Explorer (or real-time detections)](threat-explorer.md).</span></span>
  
## <a name="before-you-begin"></a><span data-ttu-id="247f7-108">시작 하기 전에</span><span class="sxs-lookup"><span data-stu-id="247f7-108">Before you begin...</span></span>

<span data-ttu-id="247f7-109">다음 조건이 충족되었는지 확인하세요.</span><span class="sxs-lookup"><span data-stu-id="247f7-109">Make sure that the following requirements are met:</span></span>
  
- <span data-ttu-id="247f7-110">조직에 [Office 365 Advanced Threat Protection](office-365-atp.md) 이 있고 [라이선스가 사용자에 게 할당 되어](https://docs.microsoft.com/en-us/office365/admin/subscriptions-and-billing/assign-licenses-to-users)있습니다.</span><span class="sxs-lookup"><span data-stu-id="247f7-110">Your organization has [Office 365 Advanced Threat Protection](office-365-atp.md) and [licenses are assigned to users](https://docs.microsoft.com/en-us/office365/admin/subscriptions-and-billing/assign-licenses-to-users).</span></span>
    
- <span data-ttu-id="247f7-111">[Office 365](turn-audit-log-search-on-or-off.md) 조직에 대해 감사 로깅이 설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="247f7-111">[Office 365 audit logging](turn-audit-log-search-on-or-off.md) is turned on for your organization.</span></span> 
    
- <span data-ttu-id="247f7-112">조직에 스팸 방지, 맬웨어 방지, 피싱 방지 등을 위한 정책이 정의 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="247f7-112">Your organization has policies defined for anti-spam, anti-malware, anti-phishing, and so on.</span></span> <span data-ttu-id="247f7-113">[Office 365에서 위협 으로부터 보호를](protect-against-threats.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="247f7-113">See [Protect against threats in Office 365](protect-against-threats.md).</span></span>
    
- <span data-ttu-id="247f7-114">Office 365 전역 관리자 이거나 보안 관리자 또는 보안 &amp; 및 준수 센터에서 할당 된 검색 및 제거 역할 중 하나를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="247f7-114">You are an Office 365 global administrator, or you have either the Security Administrator or the Search and Purge role assigned in the Security &amp; Compliance Center.</span></span> <span data-ttu-id="247f7-115">[Office 365 보안 &amp; 및 준수 센터의 사용 권한을](permissions-in-the-security-and-compliance-center.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="247f7-115">See [Permissions in the Office 365 Security &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md).</span></span> <span data-ttu-id="247f7-116">일부 작업의 경우 새 미리 보기 역할이 할당 되어 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="247f7-116">For some actions, you must also have a new Preview role assigned.</span></span> 

#### <a name="preview-role-permissions"></a><span data-ttu-id="247f7-117">미리 보기 역할 권한</span><span class="sxs-lookup"><span data-stu-id="247f7-117">Preview role permissions</span></span>

<span data-ttu-id="247f7-118">메시지 헤더를 보거나 전자 메일 메시지 콘텐츠를 다운로드 하는 등의 특정 작업을 수행 하려면 다른 해당 Office 365 역할 그룹에 *Preview* 라는 새 역할이 추가 되어 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="247f7-118">To perform certain actions, such as viewing message headers or downloading email message content, you must have a new role called *Preview* added to another appropriate Office 365 role group.</span></span> <span data-ttu-id="247f7-119">다음 표에서는 필요한 역할 및 사용 권한을 명확 하 게 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="247f7-119">The following table clarifies required roles and permissions.</span></span>

|<span data-ttu-id="247f7-120">활동</span><span class="sxs-lookup"><span data-stu-id="247f7-120">Activity</span></span>  |<span data-ttu-id="247f7-121">역할 그룹</span><span class="sxs-lookup"><span data-stu-id="247f7-121">Role group</span></span> |<span data-ttu-id="247f7-122">미리 보기 역할이 필요 하나요?</span><span class="sxs-lookup"><span data-stu-id="247f7-122">Preview role needed?</span></span>  |
|---------|---------|---------|
|<span data-ttu-id="247f7-123">위협 탐색기 (및 실시간 검색)를 사용 하 여 위협 분석</span><span class="sxs-lookup"><span data-stu-id="247f7-123">Use Threat Explorer (and real-time detections) to analyze threats</span></span>     |<span data-ttu-id="247f7-124">Office 365 전역 관리자</span><span class="sxs-lookup"><span data-stu-id="247f7-124">Office 365 Global Administrator</span></span> <br> <span data-ttu-id="247f7-125">보안 관리자</span><span class="sxs-lookup"><span data-stu-id="247f7-125">Security Administrator</span></span> <br> <span data-ttu-id="247f7-126">보안 독자</span><span class="sxs-lookup"><span data-stu-id="247f7-126">Security Reader</span></span>     | <span data-ttu-id="247f7-127">아니요</span><span class="sxs-lookup"><span data-stu-id="247f7-127">No</span></span>   |
|<span data-ttu-id="247f7-128">위협 탐색기 (및 실시간 검색)를 사용 하 여 전자 메일 메시지의 헤더 보기 및 격리 된 전자 메일 메시지 미리 보기 및 다운로드</span><span class="sxs-lookup"><span data-stu-id="247f7-128">Use Threat Explorer (and real-time detections) to view headers for email messages as well as preview and download quarantined email messages</span></span>    |<span data-ttu-id="247f7-129">Office 365 전역 관리자</span><span class="sxs-lookup"><span data-stu-id="247f7-129">Office 365 Global Administrator</span></span> <br> <span data-ttu-id="247f7-130">보안 관리자</span><span class="sxs-lookup"><span data-stu-id="247f7-130">Security Administrator</span></span> <br><span data-ttu-id="247f7-131">보안 독자</span><span class="sxs-lookup"><span data-stu-id="247f7-131">Security Reader</span></span>   |       <span data-ttu-id="247f7-132">아니요</span><span class="sxs-lookup"><span data-stu-id="247f7-132">No</span></span>  |
|<span data-ttu-id="247f7-133">위협 탐색기를 사용 하 여 머리글 보기 및 사서함으로 배달 된 전자 메일 메시지 다운로드</span><span class="sxs-lookup"><span data-stu-id="247f7-133">Use Threat Explorer to view headers and download email messages delivered to mailboxes</span></span>     |<span data-ttu-id="247f7-134">Office 365 전역 관리자</span><span class="sxs-lookup"><span data-stu-id="247f7-134">Office 365 Global Administrator</span></span> <br><span data-ttu-id="247f7-135">보안 관리자</span><span class="sxs-lookup"><span data-stu-id="247f7-135">Security Administrator</span></span> <br> <span data-ttu-id="247f7-136">보안 독자</span><span class="sxs-lookup"><span data-stu-id="247f7-136">Security Reader</span></span> <br> <span data-ttu-id="247f7-137">미리 보기</span><span class="sxs-lookup"><span data-stu-id="247f7-137">Preview</span></span>   |   <span data-ttu-id="247f7-138">예</span><span class="sxs-lookup"><span data-stu-id="247f7-138">Yes</span></span>      |

> [!NOTE]
> <span data-ttu-id="247f7-139">*미리 보기* 는 역할 그룹이 아니라 역할입니다. 미리 보기 역할은 Office 365의 기존 역할 그룹에 추가 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="247f7-139">*Preview* is a role and not a role group; the Preview role must be added to an existing role group for Office 365.</span></span> <span data-ttu-id="247f7-140">Office 365 전역 관리자 역할은 Microsoft 365 관리 센터 ([https://admin.microsoft.com](https://admin.microsoft.com))에 할당 되며 보안 관리자 및 보안 독자 역할은 Office 365 Security & 준수 센터 ([https://protection.office.com](https://protection.office.com))에서 할당 됩니다.</span><span class="sxs-lookup"><span data-stu-id="247f7-140">The Office 365 Global Administrator role is assigned the Microsoft 365 admin center ([https://admin.microsoft.com](https://admin.microsoft.com)), and the Security Administrator and Security Reader roles are assigned in the Office 365 Security & Compliance Center ([https://protection.office.com](https://protection.office.com)).</span></span> <span data-ttu-id="247f7-141">역할 및 사용 권한에 대 한 자세한 내용은 [permissions in The Office 365 Security & 준수 센터](permissions-in-the-security-and-compliance-center.md)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="247f7-141">To learn more about roles and permissions, see [Permissions in the Office 365 Security & Compliance Center](permissions-in-the-security-and-compliance-center.md).</span></span>

## <a name="find-and-delete-suspicious-email-that-was-delivered"></a><span data-ttu-id="247f7-142">배달 된 의심 스러운 전자 메일 찾기 및 삭제</span><span class="sxs-lookup"><span data-stu-id="247f7-142">Find and delete suspicious email that was delivered</span></span>

<span data-ttu-id="247f7-143">위협 탐색기는 메시지 찾기 및 삭제, 악의적인 전자 메일 보낸 사람의 IP 주소 식별, 추가 조사를 위해 인시던트 시작 등의 여러 용도로 사용할 수 있는 강력한 보고서입니다.</span><span class="sxs-lookup"><span data-stu-id="247f7-143">Threat Explorer is a powerful report that can serve multiple purposes, such as finding and deleting messages, identifying the IP address of a malicious email sender, or starting an incident for further investigation.</span></span> <span data-ttu-id="247f7-144">다음 절차에서는 Explorer를 사용 하 여 받는 사람 사서함에서 악성 전자 메일을 찾아서 삭제 하는 방법에 대해 중점적으로 설명 합니다</span><span class="sxs-lookup"><span data-stu-id="247f7-144">The following procedure focuses on using Explorer to find and delete malicious email from recipients mailboxes.</span></span>

1. <span data-ttu-id="247f7-145">[https://protection.office.com](https://protection.office.com) 으로 이동 하 여 Office 365에 대 한 회사 또는 학교 계정을 사용 하 여 로그인 합니다.</span><span class="sxs-lookup"><span data-stu-id="247f7-145">Go to [https://protection.office.com](https://protection.office.com) and sign in using your work or school account for Office 365.</span></span> <span data-ttu-id="247f7-146">이렇게 하면 보안 &amp; 및 준수 센터로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="247f7-146">This takes you to the Security &amp; Compliance Center.</span></span> 
    
2. <span data-ttu-id="247f7-147">왼쪽 탐색 영역에서 **Threat management** \> **Explorer**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="247f7-147">In the left navigation, choose **Threat management** \> **Explorer**.</span></span>

    ![배달 작업 및 배달 위치 필드가 있는 탐색기입니다.](media/ThreatExFields.PNG)

    <span data-ttu-id="247f7-149">새 **특수 동작** 열을 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="247f7-149">You may notice the new **Special actions** column.</span></span> <span data-ttu-id="247f7-150">이 기능은 관리자에 게 전자 메일 처리 결과를 알려 주는 것을 목표로 합니다.</span><span class="sxs-lookup"><span data-stu-id="247f7-150">This feature is aimed at telling admins the outcome of processing an email.</span></span> <span data-ttu-id="247f7-151">**특수 작업** 열은 **배달 작업** 및 **배달 위치로**같은 위치에서 액세스할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="247f7-151">The **Special actions** column can be accessed in the same place as **Delivery action** and **Delivery location**.</span></span> <span data-ttu-id="247f7-152">위협 탐색기의 전자 메일 시간 표시 막대의 끝에서 특수 작업을 업데이트할 수 있으며,이는 관리자에 게 더 적합 한 사냥 환경을 구현 하기 위한 새로운 기능입니다.</span><span class="sxs-lookup"><span data-stu-id="247f7-152">Special actions might be updated at the end of Threat Explorer's email timeline, which is a new feature aimed at making the hunting experience better for admins.</span></span>

3. <span data-ttu-id="247f7-153">전자 메일 시간 표시 막대를 보려면 전자 메일 메시지의 제목을 클릭 하 고 **전자 메일 시간 표시 막대**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="247f7-153">To view an email timeline, click on the subject of an email message, and then click **Email timeline**.</span></span> <span data-ttu-id="247f7-154">(이 탭은 **요약** 또는 **세부 정보와**같은 패널의 다른 제목 사이에 표시 됩니다.)</span><span class="sxs-lookup"><span data-stu-id="247f7-154">(It appears among other headings on the panel like **Summary** or **Details**.)</span></span>

    <span data-ttu-id="247f7-155">전자 메일 시간 표시 막대를 연 후에는 해당 메일에 대 한 배달 후 이벤트를 알려 주는 표가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="247f7-155">Once you've opened the email timeline, you should see a table that tells you the post-delivery events for that mail.</span></span> <span data-ttu-id="247f7-156">전자 메일에 대 한 이벤트가 더 이상 없는 경우 원래 배달에 대해 결과와 같은 **차단** 된 결과를 나타내는 단일 이벤트가 표시 **됩니다.**</span><span class="sxs-lookup"><span data-stu-id="247f7-156">In the case of no further events for the email, you should see a single event for the original delivery that states a result like **Blocked** with a verdict like **Phish**.</span></span> <span data-ttu-id="247f7-157">또한이 탭에는 전체 전자 메일 시간 표시 막대를 내보낼 수 있는 옵션도 있으며,이를 통해 탭의 모든 세부 정보와 전자 메일에 대 한 세부 정보 (제목, 보낸 사람, 받는 사람, 네트워크 및 메시지 ID 등)가 내보내집니다.</span><span class="sxs-lookup"><span data-stu-id="247f7-157">The tab also has the option to export the entire email timeline, and this exports all the details on the tab and details on the email (things like Subject, Sender, Recipient, Network, and Message ID).</span></span>

    <span data-ttu-id="247f7-158">전자 메일이 도착 한 이후 발생 한 이벤트를 이해 하기 위해 다른 위치를 확인 하는 데 소요 되는 시간이 더 낮기 때문에 전자 메일 시간 표시 막대는 임의 변경에 따라 하향 합니다</span><span class="sxs-lookup"><span data-stu-id="247f7-158">The email timeline cuts down on randomization because there is less time spent checking different locations to try to understand events that happened since the email arrived.</span></span> <span data-ttu-id="247f7-159">전자 메일에서 여러 이벤트가 발생 하거나 같은 시간에 발생할 경우 이러한 이벤트는 시간 표시 막대 보기에 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="247f7-159">When multiple events happen at, or close to, the same time on an email, those events show up in a timeline view.</span></span> 
    
    <span data-ttu-id="247f7-160">메일에 대 한 배달이 후 발생 하는 일부 이벤트는 **특수 작업** 열에 캡처됩니다.</span><span class="sxs-lookup"><span data-stu-id="247f7-160">Some events that happen post-delivery to your mail are captured in the **Special actions** column.</span></span> <span data-ttu-id="247f7-161">전자 메일 시간 표시 막대와 이메일로 전송 되는 정보를 함께 사용 하면 관리자가 정책이 작동 하는 방식, 즉 전자 메일을 최종적으로 라우팅된 위치, 그리고 경우에 따라 최종 평가가 수행 된 방식을 파악할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="247f7-161">Combining the information from the email timeline along with special actions taken on email post-delivery gives admins insight into how their policies work, where the email was finally routed, and, in some cases, what the final assessment was.</span></span> 

4. <span data-ttu-id="247f7-162">**보기** 메뉴에서 **모든 전자 메일**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="247f7-162">In the **View** menu, choose **All email**.</span></span>

    ![보기 메뉴를 사용 하 여 전자 메일 및 콘텐츠 보고서 중에서 선택](media/d39013ff-93b6-42f6-bee5-628895c251c2.png)
  
    <span data-ttu-id="247f7-164">**배달**하거나 **알 수**없거나 **정크 메일에 배달**된 것과 같이 보고서에 표시 되는 레이블을 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="247f7-164">Notice the labels that appear in the report, such as **Delivered**, **Unknown**, or **Delivered to junk**.</span></span>

    ![모든 전자 메일에 대 한 데이터를 표시 하는 위협 탐색기](media/208826ed-a85e-446f-b276-b5fdc312fbcb.png)
    
    <span data-ttu-id="247f7-166">조직에 대 한 전자 메일 메시지에 대해 수행 된 작업에 따라 다른 레이블에서 **차단** 되거나 **바뀐**것을 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="247f7-166">(Depending on the actions that were taken on email messages for your organization, you might see other labels, such as **Blocked** or **Replaced**.)</span></span>
    
6. <span data-ttu-id="247f7-167">사용자의 받은 편지 함으로 끝난 전자 메일 메시지만 표시 되도록 보고서에 **배달** 을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="247f7-167">In the report, choose **Delivered** to view only email messages that ended up in users' inboxes.</span></span>

    !["정크로 배달"을 클릭 하면 보기에서 해당 데이터가 제거 됨](media/e6fb2e47-461e-4f6f-8c65-c331bd858758.png)
  
7. <span data-ttu-id="247f7-169">차트 아래에서 차트 아래에 있는 **전자 메일** 목록을 검토 합니다.</span><span class="sxs-lookup"><span data-stu-id="247f7-169">Below the chart, review the **Email** list below the chart.</span></span>

    ![차트 아래에서 검색 된 전자 메일 메시지의 목록 보기](media/dfb60590-1236-499d-97da-86c68621e2bc.png)
  
8. <span data-ttu-id="247f7-171">목록에서 항목을 선택 하 여 해당 전자 메일 메시지에 대 한 세부 정보를 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="247f7-171">In the list, choose an item to view more details about that email message.</span></span> <span data-ttu-id="247f7-172">예를 들어 제목 줄을 클릭 하 여 보낸 사람, 받는 사람, 첨부 파일 및 기타 유사한 전자 메일 메시지에 대 한 정보를 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="247f7-172">For example, you can click the subject line to view information about the sender, recipients, attachments, and other similar email messages.</span></span>

    ![항목에 대 한 추가 정보를 볼 수 있습니다.](media/5a5707c3-d62a-4610-ae7b-900fff8708b2.png)
  
9. <span data-ttu-id="247f7-174">전자 메일 메시지에 대 한 정보를 확인 한 후에는 목록에서 하나 이상의 항목을 선택 하 여 **+ 작업**을 활성화 합니다.</span><span class="sxs-lookup"><span data-stu-id="247f7-174">After viewing information about email messages, select one or more items in the list to activate **+ Actions**.</span></span>
    
10. <span data-ttu-id="247f7-175">**+ 작업** 목록을 사용 하 여 **지운 편지함으로 이동** 등의 작업을 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="247f7-175">Use the **+ Actions** list to apply an action, such as **Move to deleted** items.</span></span> <span data-ttu-id="247f7-176">이 명령은 받는 사람의 사서함에서 선택한 메시지를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="247f7-176">This deletes the selected messages from the recipients' mailboxes.</span></span>

    ![하나 이상의 전자 메일 메시지를 선택 하면 사용 가능한 여러 작업 중에서 선택할 수 있습니다.](media/ef12e10c-60a7-4f66-8f76-68d77ae26de1.png)

## <a name="dealing-with-suspicious-email-messages"></a><span data-ttu-id="247f7-178">의심 스러운 전자 메일 메시지 처리</span><span class="sxs-lookup"><span data-stu-id="247f7-178">Dealing with suspicious email messages</span></span>

<span data-ttu-id="247f7-179">악의적인 공격자가 자신의 자격 증명을 피싱 회사 비밀에 액세스 하기 위해 조직의 사용자에 게 메일을 보낼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="247f7-179">Malicious attackers might be sending mail to people in your organization in an attempt to phish their credentials and gain access to your corporate secrets.</span></span> <span data-ttu-id="247f7-180">이를 방지 하기 위해 [Exchange Online protection](eop/exchange-online-protection-overview.md) 및 [Advanced threat protection](office-365-atp.md)을 포함 하 여 Office 365의 위협 보호 서비스를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="247f7-180">To help prevent this, you use the threat protection services in Office 365, including [Exchange Online Protection](eop/exchange-online-protection-overview.md) and [Advanced Threat Protection](office-365-atp.md).</span></span> <span data-ttu-id="247f7-181">그러나 공격자가 나중에 악성 콘텐츠 (예: 맬웨어)를 가리키는 링크 (URL)가 포함 된 전자 메일을 보내는 경우 가끔씩 발생 합니다.</span><span class="sxs-lookup"><span data-stu-id="247f7-181">However, it occasionally happens that an attacker sends email that contains a link (URL) that only later points to malicious content (such as malware).</span></span> <span data-ttu-id="247f7-182">또는 조직의 다른 사용자가 공격을 당한 경우, 공격자가 자신의 계정을 사용 하 여 조직 내 기타 사람에 게 전자 메일을 보낼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="247f7-182">Or, you might realize too late that someone in your organization has been compromised, and while they were compromised, an attacker used their account to send email to other people in your organization.</span></span> <span data-ttu-id="247f7-183">이러한 시나리오를 처리 하는 과정의 일부로 사용자의 받은 편지함에서 의심 스러운 전자 메일 메시지를 제거할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="247f7-183">As part of dealing with either of these scenarios, you can remove suspicious email messages from user inboxes.</span></span> <span data-ttu-id="247f7-184">이 작업을 수행 하기 위해 [위협 탐색기](threat-explorer.md)를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="247f7-184">To do that, you can use [Threat Explorer](threat-explorer.md).</span></span>

## <a name="finding-re-routed-email-messages-after-actions-are-taken"></a><span data-ttu-id="247f7-185">작업이 수행 된 후 다시 라우팅된 전자 메일 메시지 찾기</span><span class="sxs-lookup"><span data-stu-id="247f7-185">Finding re-routed email messages after actions are taken</span></span>

<span data-ttu-id="247f7-186">위협 탐색기에서는 의심 스러운 전자 메일을 조사 하는 데 필요한 세부 정보를 보안 운영 팀에 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="247f7-186">Threat Explorer provides your security operations team with the details they need to investigate suspicious email.</span></span> <span data-ttu-id="247f7-187">보안 운영 팀은 다음과 같은 작업을 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="247f7-187">Your security operations team can:</span></span>

- [<span data-ttu-id="247f7-188">전자 메일 머리글 보기 및 전자 메일 본문 다운로드</span><span class="sxs-lookup"><span data-stu-id="247f7-188">View the email headers and download the email body</span></span>](#view-the-email-headers-and-download-the-email-body) 

- [<span data-ttu-id="247f7-189">배달 작업 및 위치 확인</span><span class="sxs-lookup"><span data-stu-id="247f7-189">Check the delivery action and location</span></span>](#check-the-delivery-action-and-location)

- [<span data-ttu-id="247f7-190">전자 메일의 시간 표시 막대 보기</span><span class="sxs-lookup"><span data-stu-id="247f7-190">View the timeline of your email</span></span>](#view-the-timeline-of-your-email)

### <a name="view-the-email-headers-and-download-the-email-body"></a><span data-ttu-id="247f7-191">전자 메일 머리글 보기 및 전자 메일 본문 다운로드</span><span class="sxs-lookup"><span data-stu-id="247f7-191">View the email headers and download the email body</span></span>

<span data-ttu-id="247f7-192">전자 메일 머리글을 미리 보고, 전자 메일 본문을 다운로드 하는 기능은 위협 탐색기에서 강력한 기능입니다.</span><span class="sxs-lookup"><span data-stu-id="247f7-192">The ability to preview email headers and download the body of an email body are powerful capabilities in Threat Explorer.</span></span> <span data-ttu-id="247f7-193">적절 한 [사용 권한을](permissions-in-the-security-and-compliance-center.md) 할당 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="247f7-193">Appropriate [permissions](permissions-in-the-security-and-compliance-center.md) must be assigned.</span></span> <span data-ttu-id="247f7-194">[역할 권한 미리 보기](#preview-role-permissions)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="247f7-194">See [Preview role permissions](#preview-role-permissions).</span></span>

<span data-ttu-id="247f7-195">메시지 헤더 및 전자 메일 다운로드 옵션에 액세스 하려면 다음 단계를 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="247f7-195">To access your message header and email download options, follow these steps:</span></span> 

1. <span data-ttu-id="247f7-196">[https://protection.office.com](https://protection.office.com) 으로 이동 하 여 Office 365에 대 한 회사 또는 학교 계정을 사용 하 여 로그인 합니다.</span><span class="sxs-lookup"><span data-stu-id="247f7-196">Go to [https://protection.office.com](https://protection.office.com) and sign in using your work or school account for Office 365.</span></span> <span data-ttu-id="247f7-197">이렇게 하면 보안 &amp; 및 준수 센터로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="247f7-197">This takes you to the Security &amp; Compliance Center.</span></span> 
    
2. <span data-ttu-id="247f7-198">왼쪽 탐색 영역에서 **Threat management** \> **Explorer**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="247f7-198">In the left navigation, choose **Threat management** \> **Explorer**.</span></span>

3. <span data-ttu-id="247f7-199">위협 탐색기 테이블에서 제목을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="247f7-199">Click on a subject in the Threat Explorer table.</span></span> 

    <span data-ttu-id="247f7-200">이렇게 하면 플라이 아웃이 열리고 머리글 미리 보기 및 전자 메일 다운로드 링크가 모두 배치 됩니다.</span><span class="sxs-lookup"><span data-stu-id="247f7-200">This opens the flyout, where both header preview and email download links are positioned.</span></span>

    ![페이지의 링크 다운로드 및 미리 보기를 포함 하는 위협 탐색기 플라이 아웃](media/ThreatExplorerDownloadandPreview.PNG)

> [!IMPORTANT]
> <span data-ttu-id="247f7-202">이 기능은 사용자 사서함에서 발견 되지 않은 전자 메일 메시지에 대해서는 표시 되지 않고 전자 메일이 삭제 되거나 배달이 실패 한 경우에 발생할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="247f7-202">This capability doesn't show up for email messages that were never found in a user's mailbox, which can happen if an email was dropped or its delivery failed.</span></span> <span data-ttu-id="247f7-203">전자 메일 메시지가 사용자 사서함에서 삭제 된 경우 관리자는 "메일을 찾을 수 없습니다." 라는 오류 메시지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="247f7-203">In cases where email messages were deleted from users' mailboxes, admins see a "Mail not found" error message.</span></span>

### <a name="check-the-delivery-action-and-location"></a><span data-ttu-id="247f7-204">배달 작업 및 위치 확인</span><span class="sxs-lookup"><span data-stu-id="247f7-204">Check the delivery action and location</span></span>

<span data-ttu-id="247f7-205">[위협 탐색기 (및 실시간 검색)](threat-explorer.md)에서는 이제 이전 **배달 상태** 열 대신 **배달 작업** 및 **배달 위치** 열이 제공 됩니다.</span><span class="sxs-lookup"><span data-stu-id="247f7-205">In [Threat Explorer (and real-time detections)](threat-explorer.md), you now have **Delivery Action** and **Delivery Location** columns instead of the former **Delivery Status** column.</span></span> <span data-ttu-id="247f7-206">이로 인해 전자 메일 메시지가 나타나는 위치를 보다 완전 하 게 파악할 수가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="247f7-206">This results in a more complete picture of where your email messages land.</span></span> <span data-ttu-id="247f7-207">이러한 변경의 목표는 보안 작업을 보다 쉽게 찾을 수 있도록 하기 위한 것 이지만, 네트워크 결과에 문제 전자 메일 메시지의 위치가 한눈에 파악 되는 것은 아닙니다.</span><span class="sxs-lookup"><span data-stu-id="247f7-207">Part of the goal of this change is to make hunting easier for security operations, but the net result is knowing the location of problem email messages at a glance.</span></span>

<span data-ttu-id="247f7-208">배달 상태는 이제 다음과 같은 두 개의 열로 나뉩니다.</span><span class="sxs-lookup"><span data-stu-id="247f7-208">Delivery Status is now broken out into two columns:</span></span>

- <span data-ttu-id="247f7-209">**배달 작업** -이 전자 메일의 상태는 무엇입니까?</span><span class="sxs-lookup"><span data-stu-id="247f7-209">**Delivery action** - What is the status of this email?</span></span>

- <span data-ttu-id="247f7-210">**배달 위치** -이 전자 메일의 경로가 어떻게 설정 되었습니까?</span><span class="sxs-lookup"><span data-stu-id="247f7-210">**Delivery location** - Where was this email routed as a result?</span></span>

<span data-ttu-id="247f7-211">배달 작업은 기존 정책 또는 검색으로 인해 전자 메일에 대해 수행 되는 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="247f7-211">Delivery action is the action taken on an email due to existing policies or detections.</span></span> <span data-ttu-id="247f7-212">다음은 전자 메일에 사용할 수 있는 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="247f7-212">Here are the possible actions an email can take:</span></span>

- <span data-ttu-id="247f7-213">**배달** 됨-전자 메일이 사용자의 받은 편지함 또는 폴더에 배달 되어 사용자가 직접 액세스할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="247f7-213">**Delivered** – email was delivered to inbox or folder of a user and the user can directly access it.</span></span>

- <span data-ttu-id="247f7-214">**Junked** – 전자 메일이 사용자의 정크 메일 폴더 또는 삭제 된 폴더에 전송 되었으며 사용자가 정크 또는 삭제 된 폴더에 있는 전자 메일 메시지에 액세스할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="247f7-214">**Junked** – email was sent to either user’s junk folder or deleted folder, and the user has access to email messages in their Junk or Deleted folder.</span></span>

- <span data-ttu-id="247f7-215">**차단 됨** -격리 되거나, 실패 했거나, 삭제 된 전자 메일 메시지</span><span class="sxs-lookup"><span data-stu-id="247f7-215">**Blocked** – any email messages that are quarantined, that failed, or were dropped.</span></span> <span data-ttu-id="247f7-216">(사용자가이를 액세스할 수 없습니다.)</span><span class="sxs-lookup"><span data-stu-id="247f7-216">(This is completely inaccessible by the user.)</span></span>

- <span data-ttu-id="247f7-217">**대체** 됨-첨부 파일이 악성 인 .txt 파일로 악성 첨부 파일이 교체 되는 모든 전자 메일입니다.</span><span class="sxs-lookup"><span data-stu-id="247f7-217">**Replaced** – any email where malicious attachments are replaced by .txt files that state the attachment was malicious.</span></span>
 
<span data-ttu-id="247f7-218">배달 위치는 배달 후 실행 되는 정책 및 검색의 결과를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="247f7-218">Delivery location shows the results of policies and detections that run post-delivery.</span></span> <span data-ttu-id="247f7-219">배달 작업에 연결 됩니다.</span><span class="sxs-lookup"><span data-stu-id="247f7-219">It's linked to a Delivery Action.</span></span> <span data-ttu-id="247f7-220">이 필드는 문제 메일을 찾은 경우 수행 되는 작업에 대 한 통찰력을 제공 하기 위해 추가 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="247f7-220">This field was added to give insight into the action taken when a problem mail is found.</span></span> <span data-ttu-id="247f7-221">배달 위치의 가능한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="247f7-221">Here are the possible values of delivery location:</span></span>

- <span data-ttu-id="247f7-222">**받은 편지함 또는 폴더** -전자 메일이 받은 편지함 또는 폴더 (전자 메일 규칙에 따라 다름)에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="247f7-222">**Inbox or folder** – The email is in the inbox or a folder (according to your email rules).</span></span>

- <span data-ttu-id="247f7-223">**온-프레미스 또는 external** -사서함이 클라우드에는 없지만 온-프레미스에 있는 경우</span><span class="sxs-lookup"><span data-stu-id="247f7-223">**On-prem or external** – The mailbox doesn’t exist on cloud but is on-premises.</span></span>

- <span data-ttu-id="247f7-224">**정크 메일 폴더** -전자 메일이 사용자의 정크 폴더에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="247f7-224">**Junk folder** – The email is in a user's Junk folder.</span></span>

- <span data-ttu-id="247f7-225">**지운 편지함 폴더** -전자 메일이 사용자의 지운 편지함 폴더에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="247f7-225">**Deleted items folder** – The email is in a user's Deleted items folder.</span></span>

- <span data-ttu-id="247f7-226">**격리** -사용자의 사서함이 아닌 격리 된 전자 메일입니다.</span><span class="sxs-lookup"><span data-stu-id="247f7-226">**Quarantine** – The email in quarantine, and not in a user’s mailbox.</span></span>

- <span data-ttu-id="247f7-227">**Failed** – 전자 메일이 사서함에 연결 하지 못했습니다.</span><span class="sxs-lookup"><span data-stu-id="247f7-227">**Failed** – The email failed to reach the mailbox.</span></span>

- <span data-ttu-id="247f7-228">**삭제** 됨-메일 흐름의 어딘가에 전자 메일이 손실 됩니다.</span><span class="sxs-lookup"><span data-stu-id="247f7-228">**Dropped** – The email gets lost somewhere in the mail flow.</span></span>

### <a name="view-the-timeline-of-your-email"></a><span data-ttu-id="247f7-229">전자 메일의 시간 표시 막대 보기</span><span class="sxs-lookup"><span data-stu-id="247f7-229">View the timeline of your email</span></span>
  
<span data-ttu-id="247f7-230">**전자 메일 시간 표시 막대** 는 보안 운영 팀에서 더 쉽게 찾을 수 있도록 하는 위협 탐색기의 필드입니다.</span><span class="sxs-lookup"><span data-stu-id="247f7-230">**Email Timeline** is a field in Threat Explorer that makes hunting easier for your security operations team.</span></span> <span data-ttu-id="247f7-231">전자 메일에서 여러 이벤트가 발생 하거나 같은 시간에 발생할 경우 이러한 이벤트는 시간 표시 막대 보기에 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="247f7-231">When multiple events happen at or close to the same time on an email, those events show up in a timeline view.</span></span> <span data-ttu-id="247f7-232">전자 메일로 배달 후 발생 하는 일부 이벤트는 **특수 작업** 열에 캡처됩니다.</span><span class="sxs-lookup"><span data-stu-id="247f7-232">Some events that happen post-delivery to email are captured in the **Special actions** column.</span></span> <span data-ttu-id="247f7-233">전자 메일 메시지의 시간 표시 막대와 정보를 결합 하 여 배달 후 발생 하는 모든 특수 작업을 통해 관리자는 정책 및 위협 처리 (예: 메일을 라우팅된 위치, 일부 경우에는 최종 평가)를 파악할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="247f7-233">Combining information from the timeline of an email message with any special actions that were taken post-delivery gives admins insight into policies and threat handling (such as where the mail was routed, and, in some cases, what the final assessment was).</span></span>
  
## <a name="related-topics"></a><span data-ttu-id="247f7-234">관련 항목</span><span class="sxs-lookup"><span data-stu-id="247f7-234">Related topics</span></span>

[<span data-ttu-id="247f7-235">Office 365 Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="247f7-235">Office 365 Advanced Threat Protection</span></span>](office-365-ti.md)
  
[<span data-ttu-id="247f7-236">Office 365에서 위협 으로부터 보호</span><span class="sxs-lookup"><span data-stu-id="247f7-236">Protect against threats in Office 365</span></span>](protect-against-threats.md)
  
[<span data-ttu-id="247f7-237">Office 365 Advanced Threat Protection에 대 한 보고서 보기</span><span class="sxs-lookup"><span data-stu-id="247f7-237">View reports for Office 365 Advanced Threat Protection</span></span>](view-reports-for-atp.md)
  

