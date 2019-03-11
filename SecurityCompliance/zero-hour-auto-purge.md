---
title: 제로 아워 자동 비우기 - 스팸 및 맬웨어로부터 보호
ms.author: tracyp
author: MSFTTracyP
manager: laurawi
ms.date: 12/05/2018
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MOE150
- MED150
- MBS150
- MET150
ms.assetid: 96deb75f-64e8-4c10-b570-84c99c674e15
ms.collection:
- M365-security-compliance
description: ZAP (자동 삭제)은 사용자의 받은 편지 함으로 이미 배달 된 스팸 또는 맬웨어가 있는 메시지를 검색 한 다음 악의적인 콘텐츠를 렌더링 하는 전자 메일 보호 기능입니다. ZAP이 수행 하는 방법은 검색 된 악의적인 콘텐츠의 유형에 따라 다릅니다.
ms.openlocfilehash: b28de1b05843e3f5b0f6e7fc905c96f094c277f9
ms.sourcegitcommit: 74ad22a5c6c3c9d9324f0f97070909e323a4e9cf
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/11/2019
ms.locfileid: "30524022"
---
# <a name="zero-hour-auto-purge---protection-against-spam-and-malware"></a><span data-ttu-id="5dfe1-104">제로 아워 자동 비우기 - 스팸 및 맬웨어로부터 보호</span><span class="sxs-lookup"><span data-stu-id="5dfe1-104">Zero-hour auto purge - protection against spam and malware</span></span>

## <a name="overview"></a><span data-ttu-id="5dfe1-105">개요</span><span class="sxs-lookup"><span data-stu-id="5dfe1-105">Overview</span></span>

<span data-ttu-id="5dfe1-106">ZAP (자동 삭제)은 사용자의 받은 편지 함으로 이미 배달 된 피싱, 스팸 또는 맬웨어가 있는 메시지를 검색 한 다음 악성 콘텐츠 무해 함을 렌더링 하는 전자 메일 보호 기능입니다.</span><span class="sxs-lookup"><span data-stu-id="5dfe1-106">Zero-hour auto purge (ZAP) is an email protection feature that detects messages with phish, spam, or malware that have already been delivered to your users' inboxes, and then renders the malicious content harmless.</span></span> <span data-ttu-id="5dfe1-107">ZAP이 수행 하는 방법은 검색 된 악의적인 콘텐츠의 유형에 따라 다릅니다. 메일은 mail content, url 또는 attachments로 인해 zapped 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5dfe1-107">How ZAP does this depends on the type of malicious content detected; mail can be zapped due to mail content, URLs, or attachments.</span></span>
  
<span data-ttu-id="5dfe1-108">ZAP은 exchange online 사서함이 포함 된 모든 Office 365 구독에 포함 된 기본 exchange online Protection에서 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5dfe1-108">ZAP is available with the default Exchange Online Protection that is included with any Office 365 subscription that contains Exchange Online mailboxes.</span></span>

<span data-ttu-id="5dfe1-109">ZAP은 기본적으로 설정 되어 있지만 다음 조건을 충족 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="5dfe1-109">ZAP is turned on by default, but the following conditions must be met:</span></span>
  
- <span data-ttu-id="5dfe1-110">**스팸 작업** 은 **정크 메일 폴더로 메시지를 이동**하도록 설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5dfe1-110">**Spam action** is set to **Move message to Junk Email folder**.</span></span> <br/><span data-ttu-id="5dfe1-111">또한 모든 사서함을 ZAP에 게 표시 하지 않으려는 경우 사용자 집합에만 적용 되는 새 스팸 필터 정책을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5dfe1-111">You can also create a new spam filter policy that applies only to a set of users if you don't want all mailboxes to be screened by ZAP.</span></span>

- <span data-ttu-id="5dfe1-112">사용자가 기본 정크 메일 설정을 유지 했으며 정크 메일 보호를 해제 하지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="5dfe1-112">Users have kept their default junk mail settings, and have not turned off junk email protection.</span></span> <span data-ttu-id="5dfe1-113">(Outlook의 사용자 옵션에 대 한 자세한 내용은 [정크 메일 필터의 보호 수준 변경을](https://support.office.com/article/change-the-level-of-protection-in-the-junk-email-filter-e89c12d8-9d61-4320-8c57-d982c8d52f6b) 참조 하세요.)</span><span class="sxs-lookup"><span data-stu-id="5dfe1-113">(See [Change the level of protection in the Junk Email Filter](https://support.office.com/article/change-the-level-of-protection-in-the-junk-email-filter-e89c12d8-9d61-4320-8c57-d982c8d52f6b) for details about user options in Outlook.)</span></span> 
  
## <a name="how-does-zap-work"></a><span data-ttu-id="5dfe1-114">ZAP의 작동 방식</span><span class="sxs-lookup"><span data-stu-id="5dfe1-114">How does ZAP work?</span></span>

<span data-ttu-id="5dfe1-115">Office 365에서는 매일 실시간으로 스팸 방지 엔진 및 맬웨어 서명을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="5dfe1-115">Office 365 updates anti-spam engine and malware signatures in real-time on a daily basis.</span></span> <span data-ttu-id="5dfe1-116">그러나 사용자에 게 콘텐츠를 배달 한 후에 weaponized를 포함 하 여 여러 가지 이유로 인해 사용자가 여전히 해당 받은 편지함에 악성 메시지를 배달 하도록 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5dfe1-116">However, your users might still get malicious messages delivered to their inboxes for a variety of reasons, including if content is weaponized after being delivered to users.</span></span> <span data-ttu-id="5dfe1-117">ZAP은 Office 365 스팸 및 맬웨어 서명에 대 한 업데이트를 지속적으로 모니터링 하 여이를 해결 합니다.</span><span class="sxs-lookup"><span data-stu-id="5dfe1-117">ZAP addresses this by continually monitoring updates to the Office 365 spam and malware signatures.</span></span> <span data-ttu-id="5dfe1-118">ZAP은 이전에 전달한 메시지 중 사용자의 받은 편지함에 이미 배달 된 메시지가 있는지 찾아 제거할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5dfe1-118">ZAP can find and remove previously delivered messages that are already in users' inboxes.</span></span> 

- <span data-ttu-id="5dfe1-119">스팸으로 식별 된 메일의 경우, ZAP은 읽지 않은 메시지를 사용자의 정크 메일 폴더로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="5dfe1-119">For mail that is identified as spam, ZAP moves unread messages to users' Junk mail folder.</span></span> 

- <span data-ttu-id="5dfe1-120">피싱으로 식별 되는 메일의 경우 ZAP은 전자 메일을 읽은 적이 있는지 여부에 관계 없이 메시지를 사용자의 정크 메일 폴더로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="5dfe1-120">For mail that is identified as phish, ZAP moves messages to users' Junk mail folder, regardless of whether the email has been read.</span></span>

- <span data-ttu-id="5dfe1-121">새로 검색 된 맬웨어의 경우 ZAP은 전자 메일을 읽은 적이 있는지 여부에 관계 없이 전자 메일 메시지에서 첨부 파일을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="5dfe1-121">For newly detected malware, ZAP removes attachments from email messages, regardless of whether the email has been read.</span></span> 
  
<span data-ttu-id="5dfe1-122">사서함 사용자에 게는 ZAP 동작이 원활 하 게 수행 됩니다. 전자 메일 메시지를 이동 하는 경우이 사용자에 게 알림이 제공 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5dfe1-122">The ZAP action is seamless for the mailbox user; they are not notified if an email message is moved.</span></span>
  
<span data-ttu-id="5dfe1-123">허용 목록, [메일 흐름 규칙](https://go.microsoft.com/fwlink/p/?LinkId=722755), 최종 사용자 규칙 또는 추가 필터는 ZAP 보다 우선 합니다.</span><span class="sxs-lookup"><span data-stu-id="5dfe1-123">Allow lists, [mail flow rules](https://go.microsoft.com/fwlink/p/?LinkId=722755), and end user rules or additional filters take precedence over ZAP.</span></span>
  
## <a name="to-review-or-set-up-a-spam-filter-policy"></a><span data-ttu-id="5dfe1-124">스팸 필터 정책을 검토 하거나 설정 하려면</span><span class="sxs-lookup"><span data-stu-id="5dfe1-124">To review or set up a spam filter policy</span></span>
  
1. <span data-ttu-id="5dfe1-125">[https://protection.office.com](https://protection.office.com) 으로 이동 하 여 Office 365에 대 한 회사 또는 학교 계정을 사용 하 여 로그인 합니다.</span><span class="sxs-lookup"><span data-stu-id="5dfe1-125">Go to [https://protection.office.com](https://protection.office.com) and sign in using your work or school account for Office 365.</span></span>

2. <span data-ttu-id="5dfe1-126">**위협 관리**에서 **스팸 방지**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="5dfe1-126">Under **Threat management**, choose **Anti-spam**.</span></span>

3. <span data-ttu-id="5dfe1-127">표준 설정을 검토 합니다.</span><span class="sxs-lookup"><span data-stu-id="5dfe1-127">Review the standard settings.</span></span> 

4. <span data-ttu-id="5dfe1-128">설정을 사용자 지정 하려면 **사용자 지정** 탭을 선택 하 고 **사용자 지정 설정을**사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5dfe1-128">If you want to customize your settings, select the **Custom** tab, and turn on **Custom settings**.</span></span> <span data-ttu-id="5dfe1-129">설정을 편집 하 고, 원하는 경우 **+ 정책 만들기** 를 선택 하 여 새 정책을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="5dfe1-129">Edit your settings and if you want, choose **+ Create a policy** to add a new policy.</span></span> 
    
## <a name="to-see-if-zap-moved-your-message"></a><span data-ttu-id="5dfe1-130">메시지가 ZAP에서 이동 된 것을 확인 하려면</span><span class="sxs-lookup"><span data-stu-id="5dfe1-130">To see if ZAP moved your message</span></span>

<span data-ttu-id="5dfe1-131">ZAP에서 메시지를 이동 했는지 확인 하려면 [위협 방지 상태 보고서](view-email-security-reports.md#threat-protection-status-report) ( [위협 탐색기](use-explorer-in-security-and-compliance.md))를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="5dfe1-131">If you want to see if ZAP moved your message, you can use either the [Threat Protection Status report](view-email-security-reports.md#threat-protection-status-report) (or [Threat Explorer](use-explorer-in-security-and-compliance.md)).</span></span>
    
## <a name="to-disable-zap"></a><span data-ttu-id="5dfe1-132">ZAP을 사용 하지 않도록 설정 하려면</span><span class="sxs-lookup"><span data-stu-id="5dfe1-132">To disable ZAP</span></span>
  
<span data-ttu-id="5dfe1-133">Office 365 테 넌 트 또는 사용자 집합에 대해 ZAP을 사용 하지 않도록 설정 하려는 경우 EOP cmdlet의 **ZapEnabled** 매개 [](https://go.microsoft.com/fwlink/p/?LinkId=722758)변수를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="5dfe1-133">If you want to disable ZAP for your Office 365 tenant, or a set of users, use the **ZapEnabled** parameter of [Set-HostedContentFilterPolicy](https://go.microsoft.com/fwlink/p/?LinkId=722758), an EOP cmdlet.</span></span>
    
<span data-ttu-id="5dfe1-134">다음 예제에서는 "Test" 라는 콘텐츠 필터 정책에 대해 ZAP을 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="5dfe1-134">In the following example, ZAP is disabled for a content filter policy named "Test".</span></span>
    
```
  Set-HostedContentFilterPolicy -Identity Test -ZapEnabled $false
```

## <a name="faq"></a><span data-ttu-id="5dfe1-135">FAQ</span><span class="sxs-lookup"><span data-stu-id="5dfe1-135">FAQ</span></span>

### <a name="what-happens-if-a-legitimate-message-is-moved-to-the-junk-mail-folder"></a><span data-ttu-id="5dfe1-136">합법적인 메시지를 정크 메일 폴더로 이동 하면 어떻게 되나요?</span><span class="sxs-lookup"><span data-stu-id="5dfe1-136">What happens if a legitimate message is moved to the junk mail folder?</span></span>
  
<span data-ttu-id="5dfe1-137">가양성에 대 한 일반 보고 프로세스를 따라야 합니다.</span><span class="sxs-lookup"><span data-stu-id="5dfe1-137">You should follow the normal reporting process for false-positives.</span></span> <span data-ttu-id="5dfe1-138">메시지를 받은 편지함에서 정크 메일 폴더로 이동 하는 유일한 이유는 서비스가 스팸 또는 악성 메시지를 받는 것으로 확인 되었기 때문입니다.</span><span class="sxs-lookup"><span data-stu-id="5dfe1-138">The only reason the message would be moved from the inbox to the junk mail folder would be because the service has determined that the message was spam or malicious.</span></span>
  
### <a name="what-if-i-use-the-office-365-quarantine-instead-of-the-junk-mail-folder"></a><span data-ttu-id="5dfe1-139">정크 메일 폴더 대신 Office 365 검역을 사용 하는 경우에는 어떻게 하나요?</span><span class="sxs-lookup"><span data-stu-id="5dfe1-139">What if I use the Office 365 quarantine instead of the junk mail folder?</span></span>
  
<span data-ttu-id="5dfe1-140">지금은 메시지를 받은 편지함에서 격리로 이동 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5dfe1-140">ZAP doesn't move messages into quarantine from the Inbox at this time.</span></span>
  
### <a name="what-if-i-have-a-custom-mail-flow-rule-block-allow-rule"></a><span data-ttu-id="5dfe1-141">사용자 지정 메일 흐름 규칙 (차단/허용 규칙)이 있는 경우 어떻게 하나요?</span><span class="sxs-lookup"><span data-stu-id="5dfe1-141">What If I have a custom mail flow rule (Block/ Allow Rule)?</span></span>
  
<span data-ttu-id="5dfe1-142">관리자가 만든 규칙 (메일 흐름 규칙) 또는 차단 및 허용 규칙을 우선적으로 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="5dfe1-142">Rules created by admins (mail flow rules) or Block and Allow rules take precedence.</span></span> <span data-ttu-id="5dfe1-143">이러한 메시지는 기능 조건에서 제외 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5dfe1-143">Such messages are excluded from the feature criteria.</span></span>
  
## <a name="related-topics"></a><span data-ttu-id="5dfe1-144">관련 주제</span><span class="sxs-lookup"><span data-stu-id="5dfe1-144">Related Topics</span></span>

[<span data-ttu-id="5dfe1-145">Office 365 이메일 스팸 방지 보호</span><span class="sxs-lookup"><span data-stu-id="5dfe1-145">Office 365 Email Anti-Spam Protection</span></span>](anti-spam-protection.md)
  
[<span data-ttu-id="5dfe1-146">Office 365 스팸 필터로 전자 메일 스팸을 차단하여 거짓 부정 문제 방지</span><span class="sxs-lookup"><span data-stu-id="5dfe1-146">Block email spam with the Office 365 spam filter to prevent false negative issues</span></span>](reduce-spam-email.md)
  

