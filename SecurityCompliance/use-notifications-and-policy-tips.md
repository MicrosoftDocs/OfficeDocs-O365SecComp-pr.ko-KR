---
title: DLP 정책에 대한 전자 메일 알림 보내기 및 정책 팁 표시
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 3/21/2018
audience: Admin
ms.topic: article
f1_keywords:
- ms.o365.cc.UnifiedDLPRuleNotifyUser
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- M365-security-compliance
search.appverid:
- MOE150
- MET150
description: '정책 팁은 다른 사용자가 DLP 정책과 충돌 하는 콘텐츠로 작업할 때 표시 되는 알림 또는 경고입니다. 전자 메일 알림 및 정책 팁을 사용 하 여 인식을 향상 하 고 조직의 정책에 대 한 사용자를 교육 시킬 수 있습니다. 또한 사용자에 게 올바른 비즈니스 요구 사항이 있거나 정책이 가양성을 검색 하는 경우 차단 되지 않도록 정책을 재정의 하는 옵션을 제공할 수도 있습니다. '
ms.openlocfilehash: 487d3704b471b10ec876b0df3022d33d13583763
ms.sourcegitcommit: 0d5a863f48914eeaaf29f7d2a2022618de186247
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/15/2019
ms.locfileid: "34077364"
---
# <a name="send-email-notifications-and-show-policy-tips-for-dlp-policies"></a><span data-ttu-id="ae9eb-105">DLP 정책에 대한 전자 메일 알림 보내기 및 정책 팁 표시</span><span class="sxs-lookup"><span data-stu-id="ae9eb-105">Send email notifications and show policy tips for DLP policies</span></span>

<span data-ttu-id="ae9eb-106">DLP(데이터 손실 방지) 정책을 사용하여 Office 365에서 중요한 정보를 식별, 모니터링 및 보호할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ae9eb-106">You can use a data loss prevention (DLP) policy to identify, monitor, and protect sensitive information across Office 365.</span></span> <span data-ttu-id="ae9eb-107">조직의 사용자가 이러한 중요 한 정보를 사용 하 여 DLP 정책을 준수 하 고 불필요 하 게 작업을 수행 하는 것을 차단 하지 않으려고 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae9eb-107">You want people in your organization who work with this sensitive information to stay compliant with your DLP policies, but you don't want to block them unnecessarily from getting their work done.</span></span> <span data-ttu-id="ae9eb-108">이러한 경우 전자 메일 알림과 정책 팁이 도움이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ae9eb-108">This is where email notifications and policy tips can help.</span></span>
  
![메시지 표시줄에서는 Excel 2016 정책 팁](media/7002ff54-1656-4a6c-993f-37427d6508c8.png)
  
<span data-ttu-id="ae9eb-110">정책 팁은 사용자가 DLP 정책과 충돌 하는 콘텐츠 (예: PII (개인 식별 정보)를 포함 하는 비즈니스용 OneDrive 사이트에 있는 Excel 통합 문서)와 같은 콘텐츠를 사용 하는 경우 표시 되는 알림 또는 경고입니다. 외부 사용자와 공유 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ae9eb-110">A policy tip is a notification or warning that appears when someone is working with content that conflicts with a DLP policy—for example, content like an Excel workbook on a OneDrive for Business site that contains personally identifiable information (PII) and is shared with an external user.</span></span>
  
<span data-ttu-id="ae9eb-111">전자 메일 알림 및 정책 팁을 사용 하 여 인식을 향상 하 고 조직의 정책에 대 한 사용자를 교육 시킬 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ae9eb-111">You can use email notifications and policy tips to increase awareness and help educate people about your organization's policies.</span></span> <span data-ttu-id="ae9eb-112">또한 사용자에 게 올바른 비즈니스 요구 사항이 있거나 정책이 가양성을 검색 하는 경우 차단 되지 않도록 정책을 재정의 하는 옵션을 제공할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ae9eb-112">You can also give people the option to override the policy, so that they're not blocked if they have a valid business need or if the policy is detecting a false positive.</span></span>
  
<span data-ttu-id="ae9eb-113">Office 365 보안 &amp; 및 준수 센터에서 DLP 정책을 만들 때 다음 사용자에 게 알림을 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ae9eb-113">In the Office 365 Security &amp; Compliance Center, when you create a DLP policy, you can configure the user notifications to:</span></span>
  
- <span data-ttu-id="ae9eb-114">문제를 설명 하는 선택한 사람에 게 전자 메일 알림을 보냅니다.</span><span class="sxs-lookup"><span data-stu-id="ae9eb-114">Send an email notification to the people you choose that describes the issue.</span></span>
    
- <span data-ttu-id="ae9eb-115">DLP 정책과 충돌 하는 콘텐츠에 대 한 정책 팁을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae9eb-115">Display a policy tip for content that conflicts with the DLP policy:</span></span>
    
  - <span data-ttu-id="ae9eb-116">웹 및 Outlook 2013 이상에서 Outlook의 전자 메일의 경우 메시지를 작성 하는 동안 받는 사람 위의 메시지 맨 위에 정책 설명이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ae9eb-116">For email in Outlook on the web and Outlook 2013 and later, the policy tip appears at the top of a message above the recipients while the message is being composed.</span></span>
    
  - <span data-ttu-id="ae9eb-117">비즈니스용 OneDrive 계정 또는 SharePoint Online 사이트에 있는 문서의 경우 정책 팁은 항목에 경고 아이콘으로 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ae9eb-117">For documents in a OneDrive for Business account or SharePoint Online site, the policy tip is indicated by a warning icon that appears on the item.</span></span> <span data-ttu-id="ae9eb-118">자세한 내용을 보려면 항목을 선택 하 고 페이지 오른쪽 위 모서리에 있는 **정보**![정보 창](media/50b6d51b-92b4-4c5f-bb4b-4ca2d4aa3d04.png) 아이콘을 선택 하 여 세부 정보 창을 엽니다.</span><span class="sxs-lookup"><span data-stu-id="ae9eb-118">To view more information, you can select an item and then choose **Information**![Information pane icon](media/50b6d51b-92b4-4c5f-bb4b-4ca2d4aa3d04.png) in the upper-right corner of the page to open the details pane.</span></span> 
    
  - <span data-ttu-id="ae9eb-119">DLP 정책에 포함 된 비즈니스용 OneDrive 사이트 또는 SharePoint Online 사이트에 저장 된 Excel 2016, PowerPoint 2016 및 Word 2016 문서의 경우 정책 설명이 메시지 표시줄 및 Backstage 보기 ( **파일** 메뉴 \> **)에 표시 됩니다. Info**)</span><span class="sxs-lookup"><span data-stu-id="ae9eb-119">For Excel 2016, PowerPoint 2016, and Word 2016 documents that are stored on a OneDrive for Business site or SharePoint Online site that's included in the DLP policy, the policy tip appears on the Message Bar and the Backstage view ( **File** menu \> **Info**).</span></span>
    
## <a name="add-user-notifications-to-a-dlp-policy"></a><span data-ttu-id="ae9eb-120">DLP 정책에 사용자 알림 추가</span><span class="sxs-lookup"><span data-stu-id="ae9eb-120">Add user notifications to a DLP policy</span></span>

<span data-ttu-id="ae9eb-121">DLP 정책을 만들 때 전자 메일 알림과 정책 팁은 모두 **사용자 알림** 섹션의 일부입니다.</span><span class="sxs-lookup"><span data-stu-id="ae9eb-121">When you create a DLP policy, both email notifications and policy tips are part of the **User notifications** section.</span></span> 
  
1. <span data-ttu-id="ae9eb-122">[https://protection.office.com](https://protection.office.com)으로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="ae9eb-122">Go to [https://protection.office.com](https://protection.office.com).</span></span>
    
2. <span data-ttu-id="ae9eb-123">회사 또는 학교 계정을 사용하여 Office 365에 로그인합니다.</span><span class="sxs-lookup"><span data-stu-id="ae9eb-123">Sign in to Office 365 using your work or school account.</span></span> <span data-ttu-id="ae9eb-124">현재는 Office 365 보안 &amp; 및 준수 센터에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ae9eb-124">You're now in the Office 365 Security &amp; Compliance Center.</span></span>
    
3. <span data-ttu-id="ae9eb-125">보안 &amp; 준수 센터 \> 왼쪽 탐색 \> **데이터 손실 방지** \> **정책** \> **+ 정책 만들기**</span><span class="sxs-lookup"><span data-stu-id="ae9eb-125">In the Security &amp; Compliance Center \> left navigation \> **Data loss prevention** \> **Policy** \> **+ Create a policy**.</span></span>
    
    ![정책 만들기 단추](media/b1e48a08-92e2-47ca-abdc-4341694ddc7c.png)
  
4. <span data-ttu-id="ae9eb-127">\> **다음**에 필요한 중요 한 정보 유형을 보호 하는 DLP 정책 템플릿을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae9eb-127">Choose the DLP policy template that protects the types of sensitive information that you need \> **Next**.</span></span>
    
    <span data-ttu-id="ae9eb-128">빈 서식 파일로 시작 하려면 **사용자** \> **지정 정책** \> **다음**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae9eb-128">To start with an empty template, choose **Custom** \> **Custom policy** \> **Next**.</span></span>
    
5. <span data-ttu-id="ae9eb-129">정책 \> 이름을 **다음**으로 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae9eb-129">Name the policy \> **Next**.</span></span>
    
6. <span data-ttu-id="ae9eb-130">DLP 정책으로 보호 하려는 위치를 선택 하려면 다음 중 하나를 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae9eb-130">To choose the locations that you want the DLP policy to protect, do one of the following:</span></span>
    
  - <span data-ttu-id="ae9eb-131">\> \*\*\*\* **Office 365의 모든 위치를** 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae9eb-131">Choose **All locations in Office 365** \> **Next**.</span></span>
    
  - <span data-ttu-id="ae9eb-132">\> **다음**에 **특정 위치 선택을** 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae9eb-132">Choose **Let me choose specific locations** \> **Next**.</span></span>
    
    <span data-ttu-id="ae9eb-133">모든 Exchange 전자 메일 또는 모든 OneDrive 계정 등의 전체 위치를 포함 하거나 제외 하려면 해당 위치의 **상태** 를 전환 하거나 설정/해제 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae9eb-133">To include or exclude an entire location such as all Exchange email or all OneDrive accounts, switch the **Status** of that location on or off.</span></span> 
    
    <span data-ttu-id="ae9eb-134">특정 SharePoint 사이트 또는 OneDrive 계정만 포함 하려면 **상태** 를 설정으로 전환한 다음 **포함** 아래의 링크를 클릭 하 여 특정 사이트 또는 계정을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae9eb-134">To include only specific SharePoint sites or OneDrive accounts, switch the **Status** to on, and then click the links under **Include** to choose specific sites or accounts.</span></span> 
    
7. <span data-ttu-id="ae9eb-135">**고급 설정** \> 사용 **다음**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae9eb-135">Choose **Use advanced settings** \> **Next**.</span></span>
    
8. <span data-ttu-id="ae9eb-136">**+ 새 규칙**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae9eb-136">Choose **+ New rule**.</span></span>
    
9. <span data-ttu-id="ae9eb-137">규칙 편집기의 **사용자 알림에서**상태를 전환 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae9eb-137">In the rule editor, under **User notifications**, switch the status on.</span></span>
    
    ![규칙 편집기의 사용자 알림 섹션](media/47705927-c60b-4054-a072-ab914f33d15d.png)
  
## <a name="options-for-configuring-email-notifications"></a><span data-ttu-id="ae9eb-139">전자 메일 알림을 구성하기 위한 옵션</span><span class="sxs-lookup"><span data-stu-id="ae9eb-139">Options for configuring email notifications</span></span>

<span data-ttu-id="ae9eb-140">DLP 정책의 각 규칙에 대해 다음 작업을 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ae9eb-140">For each rule in a DLP policy, you can:</span></span>
  
- <span data-ttu-id="ae9eb-p106">선택한 사람에게 알림을 보냅니다. 이러한 사용자에는 콘텐츠의 소유자, 콘텐츠를 마지막으로 수정한 사람, 콘텐츠가 저장된 사이트의 소유자 또는 특정 사용자가 포함될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ae9eb-p106">Send the notification to the people you choose. These people can include the owner of the content, the person who last modified the content, the owner of the site where the content is stored, or a specific user.</span></span>
    
- <span data-ttu-id="ae9eb-143">HTML 또는 토큰을 사용 하 여 알림에 포함 되는 텍스트를 사용자 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae9eb-143">Customize the text that's included in the notification by using HTML or tokens.</span></span> <span data-ttu-id="ae9eb-144">자세한 내용은 아래 섹션을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="ae9eb-144">See the section below for more information.</span></span>
    
> [!NOTE]
>  <span data-ttu-id="ae9eb-145">전자 메일 알림은 그룹 또는 메일 그룹이 아닌 개별 받는 사람 에게만 보낼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ae9eb-145">Email notifications can be sent only to individual recipients—not groups or distribution lists.</span></span> <span data-ttu-id="ae9eb-146">새 콘텐츠만 전자 메일 알림을 트리거합니다.</span><span class="sxs-lookup"><span data-stu-id="ae9eb-146">Only new content will trigger an email notification.</span></span> <span data-ttu-id="ae9eb-147">기존 콘텐츠를 편집하면 정책 팁은 트리거되지만 전자 메일 알림은 트리거되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ae9eb-147">Editing existing content will trigger policy tips but not an email notification.</span></span> 
  
![전자 메일 알림 옵션](media/4e7b9500-2a78-44e6-9067-09f4bfd50301.png)
  
### <a name="default-email-notification"></a><span data-ttu-id="ae9eb-149">기본 전자 메일 알림</span><span class="sxs-lookup"><span data-stu-id="ae9eb-149">Default email notification</span></span>

<span data-ttu-id="ae9eb-150">알림에는 "알림", "메시지 차단 됨", 전자 메일에 대 한 "액세스 차단", 문서에 대해 수행 된 작업으로 시작 하는 제목 줄이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ae9eb-150">Notifications have a Subject line that begins with the action taken, such as "Notification", "Message Blocked" for email, or "Access Blocked" for documents.</span></span> <span data-ttu-id="ae9eb-151">문서에 대 한 알림이 있는 경우 알림 메시지 본문에는 문서가 저장 된 사이트로 이동 하 여 문서에 대 한 정책 팁이 표시 되는 링크가 포함 되어 있으므로 문제를 해결할 수 있습니다 (정책 팁에 대 한 자세한 내용은 아래 섹션 참조).</span><span class="sxs-lookup"><span data-stu-id="ae9eb-151">If the notification is about a document, the notification message body includes a link that takes you to the site where the document's stored and opens the policy tip for the document, where you can resolve any issues (see the section below about policy tips).</span></span> <span data-ttu-id="ae9eb-152">메시지에 대 한 알림이 면 해당 알림에는 DLP 정책과 일치 하는 메시지의 첨부 파일로 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ae9eb-152">If the notification is about a message, the notification includes as an attachment the message that matches a DLP policy.</span></span>
  
![알림 메시지](media/35813d40-5fd8-425f-9624-55655e74fa6b.png)
  
<span data-ttu-id="ae9eb-p110">기본적으로 알림에는 사이트의 항목에 대해 다음과 비슷한 텍스트가 표시됩니다. 알림 텍스트는 각 규칙에 대해 별도로 구성되므로 일치하는 규칙에 따라 표시되는 텍스트가 달라집니다.</span><span class="sxs-lookup"><span data-stu-id="ae9eb-p110">By default, notifications display text similar to the following for an item on a site. The notification text is configured separately for each rule, so the text that's displayed differs depending on which rule is matched.</span></span>

|<span data-ttu-id="ae9eb-156">**DLP 정책 규칙이 수행하는 작업...**</span><span class="sxs-lookup"><span data-stu-id="ae9eb-156">**If the DLP policy rule does this…**</span></span>|<span data-ttu-id="ae9eb-157">**그런 다음 SharePoint 또는 비즈니스용 OneDrive 문서에 대 한 기본 알림에는 다음과 같은 메시지가 표시 됩니다.**</span><span class="sxs-lookup"><span data-stu-id="ae9eb-157">**Then the default notification for SharePoint or OneDrive for Business documents says this…**</span></span>|<span data-ttu-id="ae9eb-158">**Outlook 메시지에 대 한 기본 알림에는 다음과 같은 메시지가 표시 됩니다.**</span><span class="sxs-lookup"><span data-stu-id="ae9eb-158">**Then the default notification for Outlook messages says this…**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="ae9eb-159">알림을 보내지만 재정의를 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ae9eb-159">Sends a notification but doesn't allow override</span></span>  <br/> |<span data-ttu-id="ae9eb-160">이 항목이 조직의 정책과 충돌합니다.</span><span class="sxs-lookup"><span data-stu-id="ae9eb-160">This item conflicts with a policy in your organization.</span></span>  <br/> |<span data-ttu-id="ae9eb-161">전자 메일 메시지가 조직의 정책과 충돌 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae9eb-161">Your email message conflicts with a policy in your organization.</span></span>  <br/> |
|<span data-ttu-id="ae9eb-162">액세스를 차단하고, 알림을 보내고, 재정의를 허용합니다.</span><span class="sxs-lookup"><span data-stu-id="ae9eb-162">Blocks access, sends a notification, and allows override</span></span>  <br/> |<span data-ttu-id="ae9eb-163">이 항목이 조직의 정책과 충돌합니다.</span><span class="sxs-lookup"><span data-stu-id="ae9eb-163">This item conflicts with a policy in your organization.</span></span> <span data-ttu-id="ae9eb-164">이 충돌을 해결 하지 않으면이 파일에 대 한 액세스가 차단 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ae9eb-164">If you don't resolve this conflict, access to this file might be blocked.</span></span>  <br/> |<span data-ttu-id="ae9eb-165">전자 메일 메시지가 조직의 정책과 충돌 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae9eb-165">Your email message conflicts with a policy in your organization.</span></span> <span data-ttu-id="ae9eb-166">메시지가 모든 받는 사람에 게 배달 되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="ae9eb-166">The message wasn't delivered to all recipients.</span></span>  <br/> |
|<span data-ttu-id="ae9eb-167">액세스를 차단하고 알림을 보냅니다.</span><span class="sxs-lookup"><span data-stu-id="ae9eb-167">Blocks access and sends a notification</span></span>  <br/> |<span data-ttu-id="ae9eb-p113">이 항목이 조직의 정책과 충돌합니다. 소유자, 마지막 수정자 및 주 사이트 모음 관리자를 제외한 모든 사람의 이 항목 액세스가 차단됩니다.</span><span class="sxs-lookup"><span data-stu-id="ae9eb-p113">This item conflicts with a policy in your organization. Access to this item is blocked for everyone except its owner, last modifier, and the primary site collection administrator.</span></span>  <br/> |<span data-ttu-id="ae9eb-170">전자 메일 메시지가 조직의 정책과 충돌 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae9eb-170">Your email message conflicts with a policy in your organization.</span></span> <span data-ttu-id="ae9eb-171">메시지가 모든 받는 사람에 게 배달 되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="ae9eb-171">The message wasn't delivered to all recipients.</span></span>  <br/> |
   
### <a name="custom-email-notification"></a><span data-ttu-id="ae9eb-172">사용자 지정 전자 메일 알림</span><span class="sxs-lookup"><span data-stu-id="ae9eb-172">Custom email notification</span></span>

<span data-ttu-id="ae9eb-173">최종 사용자 또는 관리자에 게 기본 전자 메일 알림을 보내는 대신 사용자 지정 전자 메일 알림을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ae9eb-173">You can create a custom email notification instead of sending the default email notification to your end users or admins.</span></span> <span data-ttu-id="ae9eb-174">사용자 지정 전자 메일 알림은 HTML을 지원 하며, 5000 자 제한이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ae9eb-174">The custom email notification supports HTML and has a 5,000-character limit.</span></span> <span data-ttu-id="ae9eb-175">HTML을 사용 하 여 알림에 이미지, 서식 및 기타 브랜딩을 포함할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ae9eb-175">You can use HTML to include images, formatting, and other branding in the notification.</span></span>
  
<span data-ttu-id="ae9eb-176">또한 다음 토큰을 사용 하 여 전자 메일 알림을 사용자 지정 하는 데 도움이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ae9eb-176">You can also use the following tokens to help customize the email notification.</span></span> <span data-ttu-id="ae9eb-177">이러한 토큰은 전송 된 알림에서 특정 정보로 대체 되는 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="ae9eb-177">These tokens are variables that are replaced by specific information in the notification that's sent.</span></span>

|<span data-ttu-id="ae9eb-178">**토큰만**</span><span class="sxs-lookup"><span data-stu-id="ae9eb-178">**Token**</span></span>|<span data-ttu-id="ae9eb-179">**설명**</span><span class="sxs-lookup"><span data-stu-id="ae9eb-179">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="ae9eb-180">%%% AppliedActions%%</span><span class="sxs-lookup"><span data-stu-id="ae9eb-180">%%AppliedActions%%</span></span>  <br/> |<span data-ttu-id="ae9eb-181">콘텐츠에 적용 되는 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="ae9eb-181">The actions applied to the content.</span></span>  <br/> |
|<span data-ttu-id="ae9eb-182">%% ContentURL%%</span><span class="sxs-lookup"><span data-stu-id="ae9eb-182">%%ContentURL%%</span></span>  <br/> |<span data-ttu-id="ae9eb-183">SharePoint Online 사이트 또는 비즈니스용 OneDrive 사이트에 있는 문서의 URL입니다.</span><span class="sxs-lookup"><span data-stu-id="ae9eb-183">The URL of the document on the SharePoint Online site or OneDrive for Business site.</span></span>  <br/> |
|<span data-ttu-id="ae9eb-184">%% (MatchedConditions%%)</span><span class="sxs-lookup"><span data-stu-id="ae9eb-184">%%MatchedConditions%%</span></span>  <br/> |<span data-ttu-id="ae9eb-185">콘텐츠와 일치 한 조건입니다.</span><span class="sxs-lookup"><span data-stu-id="ae9eb-185">The conditions that were matched by the content.</span></span> <span data-ttu-id="ae9eb-186">이 토큰을 사용 하 여 콘텐츠에 대 한 가능한 문제를 사용자에 게 알릴 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ae9eb-186">Use this token to inform people of possible issues with the content.</span></span>  <br/> |
   
![토큰이 표시 되는 위치를 보여 주는 알림 메시지](media/cd3f36b3-40db-4f30-99e4-190750bd1955.png)
  
## <a name="options-for-configuring-policy-tips"></a><span data-ttu-id="ae9eb-188">정책 팁 구성 옵션</span><span class="sxs-lookup"><span data-stu-id="ae9eb-188">Options for configuring policy tips</span></span>

<span data-ttu-id="ae9eb-189">DLP 정책의 각 규칙에 대해 다음을 수행하도록 정책을 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ae9eb-189">For each rule in a DLP policy, you can configure policy tips to:</span></span>
  
- <span data-ttu-id="ae9eb-190">콘텐츠가 DLP 정책과 충돌한다는 사실을 사용자에게 알려 충돌 해결을 위한 조치를 수행할 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae9eb-190">Simply notify the person that the content conflicts with a DLP policy, so that they can take action to resolve the conflict.</span></span> <span data-ttu-id="ae9eb-191">기본 텍스트 (아래 표 참조)를 사용 하거나 조직의 특정 정책에 대 한 사용자 지정 텍스트를 입력할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ae9eb-191">You can use the default text (see the tables below) or enter custom text about your organization's specific policies.</span></span>
    
- <span data-ttu-id="ae9eb-192">DLP 정책을 재정의할 수 있도록 허용합니다.</span><span class="sxs-lookup"><span data-stu-id="ae9eb-192">Allow the person to override the DLP policy.</span></span> <span data-ttu-id="ae9eb-193">필요에 따라 다음을 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ae9eb-193">Optionally, you can:</span></span>
    
  - <span data-ttu-id="ae9eb-194">사용자에게 정책을 재정의하기 위한 업무 정당성을 입력하도록 요구합니다.</span><span class="sxs-lookup"><span data-stu-id="ae9eb-194">Require the person to enter a business justification for overriding the policy.</span></span> <span data-ttu-id="ae9eb-195">이 정보는 기록 되며 보안 &amp; 및 준수 센터의 **보고서** 섹션에 있는 DLP 보고서에서 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ae9eb-195">This information is logged and you can view it in the DLP reports in the **Reports** section of the Security &amp; Compliance Center.</span></span> 
    
  - <span data-ttu-id="ae9eb-p121">가양성을 보고하고 DLP 정책을 재정의할 수 있도록 허용합니다. 이 정보 또한 보고를 위해 기록되므로 가양성을 사용하여 규칙을 미세 조정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ae9eb-p121">Allow the person to report a false positive and override the DLP policy. This information is also logged for reporting, so that you can use false positives to fine tune your rules.</span></span>
    
![정책 팁 옵션](media/0d2f2c68-028a-4900-afe6-1d9fce5303ef.png)
  
<span data-ttu-id="ae9eb-199">예를 들어 PII (개인 식별 정보)를 검색 하는 비즈니스용 OneDrive 사이트에 DLP 정책이 적용 될 수 있으며,이 정책에는 다음과 같은 세 가지 규칙이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ae9eb-199">For example, you may have a DLP policy applied to OneDrive for Business sites that detects personally identifiable information (PII), and this policy has three rules:</span></span>
  
1. <span data-ttu-id="ae9eb-p122">첫 번째 규칙: 문서에서 이 중요한 정보의 인스턴스가 5개 미만으로 검색되었으며 문서가 조직 내부의 사용자와 공유될 경우 **알림 보내기** 작업이 정책 팁을 표시합니다. 이 규칙은 단순히 사용자에게 알리고 액세스를 차단하지는 않으므로 정책 팁에 대해 재정의 옵션은 필요하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ae9eb-p122">First rule: If fewer than five instances of this sensitive information are detected in a document, and the document is shared with people inside the organization, the **Send a notification** action displays a policy tip. For policy tips, no override options are necessary because this rule is simply notifying people and not blocking access.</span></span> 
    
2. <span data-ttu-id="ae9eb-202">두 번째 규칙: 문서에서 이 중요한 정보의 인스턴스가 6개 이상으로 검색되었으며 문서가 조직 내부의 사용자와 공유될 경우 **콘텐츠에 대한 액세스 차단** 작업은 파일에 대한 사용 권한을 제한하고, **알림 보내기** 작업은 사용자가 업무 정당성을 제공하여 이 규칙의 작업을 재정의할 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae9eb-202">Second rule: If greater than five instances of this sensitive information are detected in a document, and the document is shared with people inside the organization, the **Block access to content** action restricts the permissions for the file, and the **Send a notification** action allows people to override the actions in this rule by providing a business justification.</span></span> <span data-ttu-id="ae9eb-203">조직의 비즈니스에서 내부 사용자가 PII 데이터를 공유 해야 하 고, DLP 정책이이 작업을 차단 하지 않도록 해야 하는 경우가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ae9eb-203">Your organization's business sometimes requires internal people to share PII data, and you don't want your DLP policy to block this work.</span></span> 
    
3. <span data-ttu-id="ae9eb-p124">세 번째 규칙: 문서에서 이 중요한 정보의 인스턴스가 6개 이상으로 검색되었으며 문서가 조직 외부의 사용자와 공유될 경우 **콘텐츠에 대한 액세스 차단** 작업은 파일에 대한 사용 권한을 제한하고, 이 정보가 외부로 공유될 수 있으므로 **알림 보내기** 작업은 사용자가 이 규칙의 작업을 재정의할 수 없도록 합니다. 어떠한 경우에도 조직의 사용자가 PII 데이터를 조직 외부와 공유하도록 허용하면 안 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ae9eb-p124">Third rule: If greater than five instances of this sensitive information are detected in a document, and the document is shared with people outside the organization, the **Block access to content** action restricts the permissions for the file, and the **Send a notification** action does not allow people to override the actions in this rule because the information is shared externally. Under no circumstances should people in your organization be allowed to share PII data outside the organization.</span></span> 
    
<span data-ttu-id="ae9eb-206">다음을 통해 정책 팁을 사용하여 규칙을 재정의하는 방법을 보다 잘 이해할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ae9eb-206">Here are some fine points to understand about using a policy tip to override a rule:</span></span>
  
- <span data-ttu-id="ae9eb-207">재정의 옵션은 규칙 별로 결정 되며 규칙의 모든 작업 (즉, 무시 될 수 없는 알림 보내기 제외)을 재정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae9eb-207">The option to override is per rule, and it overrides all of the actions in the rule (except sending a notification, which can't be overridden).</span></span>
    
- <span data-ttu-id="ae9eb-208">콘텐츠가 DLP 정책의 여러 규칙과 일치 하는 것이 가능 하지만 가장 제한적인 최상위 규칙의 정책 팁만 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ae9eb-208">It's possible for content to match several rules in a DLP policy, but only the policy tip from the most restrictive, highest-priority rule will be shown.</span></span> <span data-ttu-id="ae9eb-209">예를 들어 알림을 콘텐츠 액세스를 차단하는 규칙의 정책 팁은 단순히 알림을 보내는 규칙의 정책 팁보다 우선적으로 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="ae9eb-209">For example, a policy tip from a rule that blocks access to content will be shown over a policy tip from a rule that simply sends a notification.</span></span> <span data-ttu-id="ae9eb-210">따라서 정책 팁이 단계별로 표시되지는 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ae9eb-210">This prevents people from seeing a cascade of policy tips.</span></span>
    
- <span data-ttu-id="ae9eb-211">가장 제한적인 규칙의 정책 팁이 사용자의 규칙 재정의를 허용할 경우 이 규칙을 재정의하면 해당 콘텐츠가 일치하는 다른 모든 규칙이 함께 재정의됩니다.</span><span class="sxs-lookup"><span data-stu-id="ae9eb-211">If the policy tips in the most restrictive rule allow people to override the rule, then overriding this rule also overrides any other rules that the content matched.</span></span>
    
## <a name="policy-tips-on-onedrive-for-business-sites-and-sharepoint-online-sites"></a><span data-ttu-id="ae9eb-212">비즈니스용 OneDrive 사이트 및 SharePoint Online 사이트에 대한 정책 팁</span><span class="sxs-lookup"><span data-stu-id="ae9eb-212">Policy tips on OneDrive for Business sites and SharePoint Online sites</span></span>

<span data-ttu-id="ae9eb-213">비즈니스용 OneDrive 사이트 또는 SharePoint Online 사이트의 문서가 DLP 정책의 규칙과 일치 하 고 해당 규칙에서 정책 팁을 사용 하는 경우 정책 팁은 문서에 특수 아이콘을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae9eb-213">When a document on a OneDrive for Business site or SharePoint Online site matches a rule in a DLP policy, and that rule uses policy tips, the policy tips display special icons on the document:</span></span>
  
1. <span data-ttu-id="ae9eb-214">규칙이 파일에 대한 알림을 보내는 경우 경고 아이콘이 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="ae9eb-214">If the rule sends a notification about the file, the warning icon appears.</span></span>
    
2. <span data-ttu-id="ae9eb-215">규칙이 문서 액세스를 차단하는 경우 차단됨 아이콘이 나타납니다.</span><span class="sxs-lookup"><span data-stu-id="ae9eb-215">If the rule blocks access to the document, the blocked icon appears.</span></span>
    
![OneDrive 계정의 문서에 대 한 정책 팁 아이콘](media/d3e9f772-03f9-4d28-82f8-3064784332a2.png)
  
<span data-ttu-id="ae9eb-217">문서에 대해 작업을 수행 하려면 페이지 오른쪽 위 모서리에서 \> **정보**![정보 설정 창 아이콘](media/50b6d51b-92b4-4c5f-bb4b-4ca2d4aa3d04.png) 을 선택 하 여 세부 정보 창 \> **보기 정책 팁**을 열면 항목을 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ae9eb-217">To take action on a document, you can select an item \> choose **Information**![Information pane icon](media/50b6d51b-92b4-4c5f-bb4b-4ca2d4aa3d04.png) in the upper-right corner of the page to open the details pane \> **View policy tip**.</span></span>
  
<span data-ttu-id="ae9eb-218">정책 팁에 콘텐츠에 대한 문제가 표시되고, 정책 팁이 이러한 옵션을 사용하여 구성되어 있으면 정책 팁 **해결**, **재정의**를 선택하거나 가양성 **보고**를 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ae9eb-218">The policy tip lists the issues with the content, and if the policy tips are configured with these options, you can choose **Resolve**, and then **Override** the policy tip or **Report** a false positive.</span></span> 
  
![정책 팁이 표시 된 정보 창](media/0a191e70-80f0-4702-90f4-7a5b7aabcaab.png)
  
![무시 하는 옵션을 사용 하 여 정책 설명](media/e250bff9-41d5-4ce4-82ea-1dc2d043fab1.png)
  
<span data-ttu-id="ae9eb-p126">DLP 정책은 사이트와 동기화되고 정책을 기준으로 콘텐츠가 주기적으로 비동기적으로 평가되므로 DLP 정책을 만들고 빠른 시간 내에 정책 팁이 제공될 수 있습니다. 마찬가지로 정책 팁을 해결하거나 재정의한 다음 얼마 되지 않아 사이트에 있는 문서에서 해당 아이콘이 없어집니다.</span><span class="sxs-lookup"><span data-stu-id="ae9eb-p126">DLP policies are synced to sites and contented is evaluated against them periodically and asynchronously, so there may be a short delay between the time you create the DLP policy and the time you begin to see policy tips. There may be a similar delay from when you resolve or override a policy tip to when the icon on the document on the site goes away.</span></span>
  
### <a name="default-text-for-policy-tips-on-sites"></a><span data-ttu-id="ae9eb-223">사이트의 정책 팁 기본 텍스트</span><span class="sxs-lookup"><span data-stu-id="ae9eb-223">Default text for policy tips on sites</span></span>

<span data-ttu-id="ae9eb-p127">기본적으로 정책 팁에는 사이트의 항목에 대해 다음과 비슷한 텍스트가 표시됩니다. 알림 텍스트는 각 규칙에 대해 별도로 구성되므로 일치하는 규칙에 따라 표시되는 텍스트가 달라집니다.</span><span class="sxs-lookup"><span data-stu-id="ae9eb-p127">By default, policy tips display text similar to the following for an item on a site. The notification text is configured separately for each rule, so the text that's displayed differs depending on which rule is matched.</span></span>

|<span data-ttu-id="ae9eb-226">**DLP 정책 규칙이 수행하는 작업...**</span><span class="sxs-lookup"><span data-stu-id="ae9eb-226">**If the DLP policy rule does this…**</span></span>|<span data-ttu-id="ae9eb-227">**기본 정책 팁에 표시되는 내용...**</span><span class="sxs-lookup"><span data-stu-id="ae9eb-227">**Then the default policy tip says this…**</span></span>|
|:-----|:-----|
|<span data-ttu-id="ae9eb-228">알림을 보내지만 재정의를 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ae9eb-228">Sends a notification but doesn't allow override</span></span>  <br/> |<span data-ttu-id="ae9eb-229">이 항목이 조직의 정책과 충돌합니다.</span><span class="sxs-lookup"><span data-stu-id="ae9eb-229">This item conflicts with a policy in your organization.</span></span>  <br/> |
|<span data-ttu-id="ae9eb-230">액세스를 차단하고, 알림을 보내고, 재정의를 허용합니다.</span><span class="sxs-lookup"><span data-stu-id="ae9eb-230">Blocks access, sends a notification, and allows override</span></span>  <br/> |<span data-ttu-id="ae9eb-231">이 항목이 조직의 정책과 충돌합니다.</span><span class="sxs-lookup"><span data-stu-id="ae9eb-231">This item conflicts with a policy in your organization.</span></span> <span data-ttu-id="ae9eb-232">이 충돌을 해결 하지 않으면이 파일에 대 한 액세스가 차단 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ae9eb-232">If you don't resolve this conflict, access to this file might be blocked.</span></span>  <br/> |
|<span data-ttu-id="ae9eb-233">액세스를 차단하고 알림을 보냅니다.</span><span class="sxs-lookup"><span data-stu-id="ae9eb-233">Blocks access and sends a notification</span></span>  <br/> |<span data-ttu-id="ae9eb-p129">이 항목이 조직의 정책과 충돌합니다. 소유자, 마지막 수정자 및 주 사이트 모음 관리자를 제외한 모든 사람의 이 항목 액세스가 차단됩니다.</span><span class="sxs-lookup"><span data-stu-id="ae9eb-p129">This item conflicts with a policy in your organization. Access to this item is blocked for everyone except its owner, last modifier, and the primary site collection administrator.</span></span>  <br/> |
   
### <a name="custom-text-for-policy-tips-on-sites"></a><span data-ttu-id="ae9eb-236">사이트의 정책 팁에 대 한 사용자 지정 텍스트</span><span class="sxs-lookup"><span data-stu-id="ae9eb-236">Custom text for policy tips on sites</span></span>

<span data-ttu-id="ae9eb-237">전자 메일 알림과는 별도로 정책 팁 텍스트를 사용자 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ae9eb-237">You can customize the text for policy tips separately from the email notification.</span></span> <span data-ttu-id="ae9eb-238">전자 메일 알림에 대 한 사용자 지정 텍스트 (위 섹션 참조)와 달리 정책 팁에 대 한 사용자 지정 텍스트에는 HTML 또는 토큰을 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="ae9eb-238">Unlike custom text for email notifications (see above section), custom text for policy tips does not accept HTML or tokens.</span></span> <span data-ttu-id="ae9eb-239">대신, 정책 팁에 대 한 사용자 지정 텍스트는 256 자 제한이 있는 일반 텍스트입니다.</span><span class="sxs-lookup"><span data-stu-id="ae9eb-239">Instead, custom text for policy tips is plain text only with a 256-character limit.</span></span>
  
## <a name="policy-tips-in-outlook-on-the-web-and-outlook-2013-and-later"></a><span data-ttu-id="ae9eb-240">웹용 Outlook 및 Outlook 2013 이상 정책 팁</span><span class="sxs-lookup"><span data-stu-id="ae9eb-240">Policy tips in Outlook on the web and Outlook 2013 and later</span></span>

<span data-ttu-id="ae9eb-241">웹 및 Outlook 2013 이상에서 Outlook에서 새 전자 메일을 작성할 때 DLP 정책의 규칙과 일치 하는 콘텐츠를 추가 하는 경우 정책 팁이 표시 되며 해당 규칙은 정책 팁을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae9eb-241">When you compose a new email in Outlook on the web and Outlook 2013 and later, you'll see a policy tip if you add content that matches a rule in a DLP policy, and that rule uses policy tips.</span></span> <span data-ttu-id="ae9eb-242">메시지를 작성 하는 동안 메시지 위쪽, 받는 사람 위에 정책 설명이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ae9eb-242">The policy tip appears at the top of the message, above the recipients, while the message is being composed.</span></span>
  
![구성 하는 메시지의 맨 위에 정책 팁](media/9b3b6b74-17c5-4562-82d5-d17ecaaa8d95.png)
  
<span data-ttu-id="ae9eb-244">정책 팁은 중요 한 정보가 메시지 본문, 제목 줄에 표시 되는지, 아니면 여기에 표시 된 메시지 첨부 파일에 나타나는지를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="ae9eb-244">Policy tips work whether the sensitive information appears in the message body, subject line, or even a message attachment as shown here.</span></span>
  
![첨부 파일이 DLP 정책과 충돌 함을 보여주는 정책 팁](media/59ae6655-215f-47d9-ad1d-39c0d1e61740.png)
  
<span data-ttu-id="ae9eb-246">정책 팁이 재정의를 허용 하도록 구성 \*\*\*\* 된 경우 **세부 정보** \> 표시 **재정의** \> 를 선택 하 여 비즈니스 근거를 입력 하거나 가양성 \> 을 보고할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ae9eb-246">If the policy tips are configured to allow override, you can choose **Show Details** \> **Override** \> enter a business justification or report a false positive \> **Override**.</span></span>
  
![재정의 옵션을 표시 하도록 확장 된 메시지의 정책 설명](media/28bfb997-48a6-41f0-8682-d5e62488458a.png)
  
![정책 팁을 재정의할 수 있는 정책 팁 대화 상자](media/f97e836c-04bd-44b4-aec6-ed9526ea31f8.png)
  
<span data-ttu-id="ae9eb-249">전자 메일에 중요 한 정보를 추가 하는 경우 중요 한 정보를 추가 하는 경우와 정책 팁이 표시 될 때 사이에 대기 시간이 있을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ae9eb-249">Note that when you add sensitive information to an email, there may be latency between when the sensitive information is added and when the policy tip appears.</span></span>

### <a name="outlook-2013-and-later-supports-showing-policy-tips-for-only-some-conditions"></a><span data-ttu-id="ae9eb-250">Outlook 2013 이상에서는 일부 조건에 대 한 정책 팁 표시를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae9eb-250">Outlook 2013 and later supports showing policy tips for only some conditions</span></span>

<span data-ttu-id="ae9eb-251">현재 Outlook 2013 이상에서는 이러한 조건에 대 한 정책 팁 표시를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae9eb-251">Currently, Outlook 2013 and later supports showing policy tips only for these conditions:</span></span>

- <span data-ttu-id="ae9eb-252">콘텐츠에 포함 된 내용</span><span class="sxs-lookup"><span data-stu-id="ae9eb-252">Content contains</span></span>
- <span data-ttu-id="ae9eb-253">콘텐츠 공유</span><span class="sxs-lookup"><span data-stu-id="ae9eb-253">Content is shared</span></span>

<span data-ttu-id="ae9eb-254">현재는 추가 조건에 대 한 정책 팁을 표시 하는 작업을 수행 하 고 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ae9eb-254">We're currently working on support for showing policy tips for additional conditions.</span></span> <span data-ttu-id="ae9eb-255">다음과 같은 다양한 알고리즘과 방법이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ae9eb-255">These include:</span></span>

- <span data-ttu-id="ae9eb-256">모든 전자 메일 첨부 파일의 콘텐츠를 검색할 수 없음</span><span class="sxs-lookup"><span data-stu-id="ae9eb-256">Any email attachment's content could not be scanned</span></span>
- <span data-ttu-id="ae9eb-257">모든 전자 메일 첨부 파일의 콘텐츠가 검색을 완료 하지 못함</span><span class="sxs-lookup"><span data-stu-id="ae9eb-257">Any email attachment's content didn't complete scanning</span></span>
- <span data-ttu-id="ae9eb-258">첨부 파일 확장명</span><span class="sxs-lookup"><span data-stu-id="ae9eb-258">Attachment file extension is</span></span>
- <span data-ttu-id="ae9eb-259">첨부 파일이 암호로 보호 됨</span><span class="sxs-lookup"><span data-stu-id="ae9eb-259">Attachment is password protected</span></span>
- <span data-ttu-id="ae9eb-260">Document 속성은</span><span class="sxs-lookup"><span data-stu-id="ae9eb-260">Document property is</span></span>
- <span data-ttu-id="ae9eb-261">받는 사람 도메인</span><span class="sxs-lookup"><span data-stu-id="ae9eb-261">Recipient domain is</span></span>
- <span data-ttu-id="ae9eb-262">보낸 사람 IP 주소</span><span class="sxs-lookup"><span data-stu-id="ae9eb-262">Sender IP address is</span></span>

<span data-ttu-id="ae9eb-263">이러한 모든 조건은 Outlook에서 작동 하며 콘텐츠를 일치 시키고 콘텐츠에 대 한 보호 작업을 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae9eb-263">Note that all of these conditions work in Outlook, where they will match content and enforce protective actions on content.</span></span> <span data-ttu-id="ae9eb-264">하지만 사용자에 게 정책 팁을 표시 하는 기능은 아직 지원 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ae9eb-264">But showing policy tips to users is not yet supported.</span></span>
  
### <a name="policy-tips-in-the-exchange-admin-center-vs-the-office-365-security-amp-compliance-center"></a><span data-ttu-id="ae9eb-265">Exchange 관리 센터의 정책 팁과 Office 365 보안 &amp; 및 준수 센터</span><span class="sxs-lookup"><span data-stu-id="ae9eb-265">Policy tips in the Exchange admin center vs. the Office 365 Security &amp; Compliance Center</span></span>

<span data-ttu-id="ae9eb-266">정책 팁은 Exchange 관리 센터에서 만든 DLP 정책 및 메일 흐름 규칙 또는 Office 365 보안 &amp; 준수 센터에서 만든 dlp 정책을 사용 하거나 둘 다 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="ae9eb-266">Policy tips can work either with DLP policies and mail flow rules created in the Exchange admin center, or with DLP policies created in the Office 365 Security &amp; Compliance Center, but not both.</span></span> <span data-ttu-id="ae9eb-267">이러한 정책은 서로 다른 위치에 저장 되어 있지만 정책 팁은 단일 위치 에서만 그릴 수 있기 때문입니다.</span><span class="sxs-lookup"><span data-stu-id="ae9eb-267">This is because these policies are stored in different locations, but policy tips can draw only from a single location.</span></span>
  
<span data-ttu-id="ae9eb-268">Exchange 관리 센터에서 정책 팁을 구성한 경우에는 Exchange의 팁을 해제할 때까지 Office 365 보안 &amp; 준수 센터에서 구성한 정책 팁이 웹 및 outlook 2013 이상 outlook의 사용자에 게 표시 되지 않습니다. 관리 센터</span><span class="sxs-lookup"><span data-stu-id="ae9eb-268">If you've configured policy tips in the Exchange admin center, any policy tips that you configure in the Office 365 Security &amp; Compliance Center won't appear to users in Outlook on the web and Outlook 2013 and later until you turn off the tips in the Exchange admin center.</span></span> <span data-ttu-id="ae9eb-269">이렇게 하면 Office 365 보안 &amp; 및 준수 센터로 전환 하도록 선택할 때까지 현재 Exchange 메일 흐름 규칙 (전송 규칙이 라고도 함)이 계속 작동 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae9eb-269">This ensures that your current Exchange mail flow rules (also known as transport rules) will continue to work until you choose to switch over to the Office 365 Security &amp; Compliance Center.</span></span>
  
<span data-ttu-id="ae9eb-270">정책 팁은 단일 위치 에서만 그릴 수 있지만 Office 365 보안 &amp; 및 준수 센터와 Exchange 관리 센터 둘 다에서 DLP 정책을 사용 하는 경우에도 전자 메일 알림이 항상 전송 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ae9eb-270">Note that while policy tips can draw only from a single location, email notifications are always sent, even if you're using DLP policies in both the Office 365 Security &amp; Compliance Center and the Exchange admin center.</span></span>
  
### <a name="default-text-for-policy-tips-in-email"></a><span data-ttu-id="ae9eb-271">전자 메일의 정책 팁에 대 한 기본 텍스트</span><span class="sxs-lookup"><span data-stu-id="ae9eb-271">Default text for policy tips in email</span></span>

<span data-ttu-id="ae9eb-272">기본적으로 정책 팁은 전자 메일에 대해 다음과 같은 텍스트를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae9eb-272">By default, policy tips display text similar to the following for email.</span></span>

|<span data-ttu-id="ae9eb-273">**DLP 정책 규칙이 수행하는 작업...**</span><span class="sxs-lookup"><span data-stu-id="ae9eb-273">**If the DLP policy rule does this…**</span></span>|<span data-ttu-id="ae9eb-274">**기본 정책 팁에 표시되는 내용...**</span><span class="sxs-lookup"><span data-stu-id="ae9eb-274">**Then the default policy tip says this…**</span></span>|
|:-----|:-----|
|<span data-ttu-id="ae9eb-275">알림을 보내지만 재정의를 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ae9eb-275">Sends a notification but doesn't allow override</span></span>  <br/> |<span data-ttu-id="ae9eb-276">전자 메일이 조직의 정책과 충돌 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae9eb-276">Your email conflicts with a policy in your organization.</span></span>  <br/> |
|<span data-ttu-id="ae9eb-277">액세스를 차단하고, 알림을 보내고, 재정의를 허용합니다.</span><span class="sxs-lookup"><span data-stu-id="ae9eb-277">Blocks access, sends a notification, and allows override</span></span>  <br/> |<span data-ttu-id="ae9eb-278">전자 메일이 조직의 정책과 충돌 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae9eb-278">Your email conflicts with a policy in your organization.</span></span>  <br/> |
|<span data-ttu-id="ae9eb-279">액세스를 차단하고 알림을 보냅니다.</span><span class="sxs-lookup"><span data-stu-id="ae9eb-279">Blocks access and sends a notification</span></span>  <br/> |<span data-ttu-id="ae9eb-280">전자 메일이 조직의 정책과 충돌 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae9eb-280">Your email conflicts with a policy in your organization.</span></span>  <br/> |
   
## <a name="policy-tips-in-excel-2016-powerpoint-2016-and-word-2016"></a><span data-ttu-id="ae9eb-281">Excel 2016, PowerPoint 2016 및 Word 2016의 정책 팁</span><span class="sxs-lookup"><span data-stu-id="ae9eb-281">Policy tips in Excel 2016, PowerPoint 2016, and Word 2016</span></span>

<span data-ttu-id="ae9eb-p136">사용자가 데스크톱 버전의 Excel 2016, PowerPoint 2016 및 Word 2016에서 중요한 콘텐츠로 작업할 경우 정책 팁은 해당 콘텐츠가 DLP 정책과 충돌할 때 실시간으로 알릴 수 있습니다. 이를 위해 다음이 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="ae9eb-p136">When people work with sensitive content in the desktop versions of Excel 2016, PowerPoint 2016, and Word 2016, policy tips can notify them in real time that the content conflicts with a DLP policy. This requires that:</span></span>
  
- <span data-ttu-id="ae9eb-284">Office 문서가 비즈니스용 OneDrive 사이트 또는 SharePoint Online 사이트에 저장되어 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae9eb-284">The Office document is stored on a OneDrive for Business site or SharePoint Online site.</span></span>
    
- <span data-ttu-id="ae9eb-285">사이트는 정책 팁을 사용 하도록 구성 된 DLP 정책에 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ae9eb-285">The site is included in a DLP policy that's configured to use policy tips.</span></span>
    
<span data-ttu-id="ae9eb-286">이러한 Office 2016 데스크톱 프로그램은 자동으로 DLP 정책을 Office 365에서 직접 동기화 한 다음 문서를 검사 하 여 DLP 정책과 충돌 하지 않도록 하 고 정책 팁을 실시간으로 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae9eb-286">These Office 2016 desktop programs automatically sync DLP policies directly from Office 365, and then scan your documents to ensure that they don't conflict with your DLP policies and display policy tips in real time.</span></span>
  
<span data-ttu-id="ae9eb-287">DLP 정책에서 정책 팁을 구성한 방식에 따라, 사용자들은 간단히 정책 팁을 무시하거나, 업무 정당성을 지정하거나 지정하지 않은 상태로 정책을 재정의하거나, 가양성을 보고하도록 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ae9eb-287">Depending on how you configure the policy tips in the DLP policy, people can choose to simply ignore the policy tip, override the policy with or without a business justification, or report a false positive.</span></span>
  
<span data-ttu-id="ae9eb-288">메시지 표시줄에 정책 팁이 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="ae9eb-288">Policy tips appear on the Message Bar.</span></span>
  
![메시지 표시줄에서는 Excel 2016 정책 팁](media/7002ff54-1656-4a6c-993f-37427d6508c8.png)
  
<span data-ttu-id="ae9eb-290">또한 Backstage 보기에도 정책 팁이 나타납니다(**파일** 탭).</span><span class="sxs-lookup"><span data-stu-id="ae9eb-290">And policy tips also appear in the Backstage view (on the **File** tab).</span></span> 
  
![Backstage Excel 2016의 정책 정보를 표시](media/44c561f6-8f3f-4878-b1b0-b7543f8a4120.png)
  
<span data-ttu-id="ae9eb-292">DLP 정책의 정책 팁이 이러한 옵션으로 구성되어 있는 경우 정책 팁 **해결** 또는 **재정의**를 선택하거나 가양성 **보고**를 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ae9eb-292">If policy tips in the DLP policy are configured with these options, you can choose **Resolve** to **Override** a policy tip or **Report** a false positive.</span></span> 
  
![정책 옵션에서 Excel 2016 Backstage에서 팁](media/5b3857ba-907e-456e-ae43-888b594c049c.png)
  
<span data-ttu-id="ae9eb-p137">이러한 각 Office 2016 데스크톱 프로그램에서 정책 팁을 끄도록 선택할 수 있습니다. 정책 팁을 끄면, 단순히 알림에 불과한 정책 팁은 메시지 표시줄 또는 Backstage 보기에 표시되지 것입니다(**파일** 탭). 그러나 차단 및 재정의에 대한 정책 팁은 계속 표시되고, 해당 사용자는 전자 메일 알림을 받게 됩니다. 또한 정책 팁을 꺼도 문서에 적용된 모든 DLP 정책에서 해당 문서가 제외되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ae9eb-p137">In each of these Office 2016 desktop programs, people can choose to turn off policy tips. If turned off, policy tips that are simple notifications will not appear on the Message Bar or Backstage view (on the **File** tab). However, policy tips about blocking and overriding will still appear, and they will still receive the email notification. In addition, turning off policy tips does not exempt the document from any DLP policies that have been applied to it.</span></span> 
  
### <a name="default-text-for-policy-tips-in-excel-2016-powerpoint-2016-and-word-2016"></a><span data-ttu-id="ae9eb-298">Excel 2016, PowerPoint 2016 및 Word 2016 정책 팁에 대한 기본 텍스트</span><span class="sxs-lookup"><span data-stu-id="ae9eb-298">Default text for policy tips in Excel 2016, PowerPoint 2016, and Word 2016</span></span>

<span data-ttu-id="ae9eb-p138">기본적으로 열린 문서의 메시지 표시줄 및 Backstage 보기에 다음과 비슷한 텍스트가 정책 팁으로 표시됩니다. 알림 텍스트는 각 규칙에 대해 별도로 구성되므로 일치하는 규칙에 따라 표시되는 텍스트가 달라집니다.</span><span class="sxs-lookup"><span data-stu-id="ae9eb-p138">By default, policy tips display text similar to the following on the Message Bar and Backstage view of an open document. The notification text is configured separately for each rule, so the text that's displayed differs depending on which rule is matched.</span></span>

|<span data-ttu-id="ae9eb-301">**DLP 정책 규칙이 수행하는 작업...**</span><span class="sxs-lookup"><span data-stu-id="ae9eb-301">**If the DLP policy rule does this…**</span></span>|<span data-ttu-id="ae9eb-302">**기본 정책 팁에 표시되는 내용...**</span><span class="sxs-lookup"><span data-stu-id="ae9eb-302">**Then the default policy tip says this…**</span></span>|
|:-----|:-----|
|<span data-ttu-id="ae9eb-303">알림을 보내지만 재정의를 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ae9eb-303">Sends a notification but doesn't allow override</span></span>  <br/> |<span data-ttu-id="ae9eb-304">이 파일이 조직의 정책과 충돌합니다.</span><span class="sxs-lookup"><span data-stu-id="ae9eb-304">This file conflicts with a policy in your organization.</span></span> <span data-ttu-id="ae9eb-305">자세한 내용을 보려면 **파일** 메뉴로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae9eb-305">Go to the **File** menu for more information.</span></span>  <br/> |
|<span data-ttu-id="ae9eb-306">액세스를 차단하고, 알림을 보내고, 재정의를 허용합니다.</span><span class="sxs-lookup"><span data-stu-id="ae9eb-306">Blocks access, sends a notification, and allows override</span></span>  <br/> |<span data-ttu-id="ae9eb-307">이 파일이 조직의 정책과 충돌합니다.</span><span class="sxs-lookup"><span data-stu-id="ae9eb-307">This file conflicts with a policy in your organization.</span></span> <span data-ttu-id="ae9eb-308">이 충돌을 해결 하지 않으면이 파일에 대 한 액세스가 차단 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ae9eb-308">If you don't resolve this conflict, access to this file might be blocked.</span></span> <span data-ttu-id="ae9eb-309">자세한 내용을 보려면 **파일** 메뉴로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae9eb-309">Go to the **File** menu for more information.</span></span>  <br/> |
|<span data-ttu-id="ae9eb-310">액세스를 차단하고 알림을 보냅니다.</span><span class="sxs-lookup"><span data-stu-id="ae9eb-310">Blocks access and sends a notification</span></span>  <br/> |<span data-ttu-id="ae9eb-311">이 파일이 조직의 정책과 충돌합니다.</span><span class="sxs-lookup"><span data-stu-id="ae9eb-311">This file conflicts with a policy in your organization.</span></span> <span data-ttu-id="ae9eb-312">이 충돌을 해결 하지 않으면이 파일에 대 한 액세스가 차단 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ae9eb-312">If you don't resolve this conflict, access to this file might be blocked.</span></span> <span data-ttu-id="ae9eb-313">자세한 내용을 보려면 **파일** 메뉴로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae9eb-313">Go to the **File** menu for more information.</span></span>  <br/> |
   
### <a name="custom-text-for-policy-tips-in-excel-2016-powerpoint-2016-and-word-2016"></a><span data-ttu-id="ae9eb-314">Excel 2016, PowerPoint 2016 및 Word 2016의 정책 팁에 대 한 사용자 지정 텍스트</span><span class="sxs-lookup"><span data-stu-id="ae9eb-314">Custom text for policy tips in Excel 2016, PowerPoint 2016, and Word 2016</span></span>

<span data-ttu-id="ae9eb-315">전자 메일 알림과는 별도로 정책 팁 텍스트를 사용자 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ae9eb-315">You can customize the text for policy tips separately from the email notification.</span></span> <span data-ttu-id="ae9eb-316">전자 메일 알림에 대 한 사용자 지정 텍스트 (위 섹션 참조)와 달리 정책 팁에 대 한 사용자 지정 텍스트에는 HTML 또는 토큰을 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="ae9eb-316">Unlike custom text for email notifications (see above section), custom text for policy tips does not accept HTML or tokens.</span></span> <span data-ttu-id="ae9eb-317">대신, 정책 팁에 대 한 사용자 지정 텍스트는 256 자 제한이 있는 일반 텍스트입니다.</span><span class="sxs-lookup"><span data-stu-id="ae9eb-317">Instead, custom text for policy tips is plain text only with a 256-character limit.</span></span>
  
## <a name="more-information"></a><span data-ttu-id="ae9eb-318">추가 정보</span><span class="sxs-lookup"><span data-stu-id="ae9eb-318">More information</span></span>

- [<span data-ttu-id="ae9eb-319">데이터 손실 방지 정책 개요</span><span class="sxs-lookup"><span data-stu-id="ae9eb-319">Overview of data loss prevention policies</span></span>](data-loss-prevention-policies.md)
    
- [<span data-ttu-id="ae9eb-320">템플릿에서 DLP 정책 만들기</span><span class="sxs-lookup"><span data-stu-id="ae9eb-320">Create a DLP policy from a template</span></span>](create-a-dlp-policy-from-a-template.md)
    
- [<span data-ttu-id="ae9eb-321">FCI 또는 기타 속성을 갖는 문서를 보호하는 DLP 정책 만들기</span><span class="sxs-lookup"><span data-stu-id="ae9eb-321">Create a DLP policy to protect documents with FCI or other properties</span></span>](protect-documents-that-have-fci-or-other-properties.md)
    
- [<span data-ttu-id="ae9eb-322">DLP 정책 템플릿에 포함되는 내용</span><span class="sxs-lookup"><span data-stu-id="ae9eb-322">What the DLP policy templates include</span></span>](what-the-dlp-policy-templates-include.md)
    
- [<span data-ttu-id="ae9eb-323">중요한 정보 형식이 찾는 항목</span><span class="sxs-lookup"><span data-stu-id="ae9eb-323">What the sensitive information types look for</span></span>](what-the-sensitive-information-types-look-for.md)
    

