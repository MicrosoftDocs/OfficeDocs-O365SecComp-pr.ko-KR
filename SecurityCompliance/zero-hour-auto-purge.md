---
title: 제로 아워 자동 비우기 - 스팸 및 맬웨어로부터 보호
ms.author: tracyp
author: MSFTTracyP
manager: dansimp
ms.date: 04/11/2019
audience: Admin
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
ms.openlocfilehash: ceb5a973a65406527de3361a354247908b4cab63
ms.sourcegitcommit: 986f40a00ab454093b21e724d58594b8b8b4a9ba
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/10/2019
ms.locfileid: "35613666"
---
# <a name="zero-hour-auto-purge---protection-against-spam-and-malware"></a><span data-ttu-id="46365-104">제로 아워 자동 비우기 - 스팸 및 맬웨어로부터 보호</span><span class="sxs-lookup"><span data-stu-id="46365-104">Zero-hour auto purge - protection against spam and malware</span></span>

## <a name="overview"></a><span data-ttu-id="46365-105">개요</span><span class="sxs-lookup"><span data-stu-id="46365-105">Overview</span></span>

<span data-ttu-id="46365-106">ZAP (자동 삭제)은 사용자의 받은 편지 함으로 이미 배달 된 피싱, 스팸 또는 맬웨어가 있는 메시지를 검색 한 다음 악성 콘텐츠 무해 함을 렌더링 하는 전자 메일 보호 기능입니다.</span><span class="sxs-lookup"><span data-stu-id="46365-106">Zero-hour auto purge (ZAP) is an email protection feature that detects messages with phish, spam, or malware that have already been delivered to your users' inboxes, and then renders the malicious content harmless.</span></span> <span data-ttu-id="46365-107">ZAP이 수행 하는 방법은 검색 된 악의적인 콘텐츠의 유형에 따라 다릅니다. 메일은 mail content, Url 또는 attachments로 인해 zapped 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="46365-107">How ZAP does this depends on the type of malicious content detected; mail can be zapped due to mail content, URLs, or attachments.</span></span>
  
<span data-ttu-id="46365-108">ZAP은 Exchange Online 사서함이 포함 된 모든 Office 365 구독에 포함 된 기본 Exchange Online Protection에서 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="46365-108">ZAP is available with the default Exchange Online Protection that is included with any Office 365 subscription that contains Exchange Online mailboxes.</span></span>

<span data-ttu-id="46365-109">ZAP은 기본적으로 설정 되어 있지만 다음 조건을 충족 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="46365-109">ZAP is turned on by default, but the following conditions must be met:</span></span>
  
- <span data-ttu-id="46365-110">**스팸 작업** 은 **정크 메일 폴더로 메시지를 이동**하도록 설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="46365-110">**Spam action** is set to **Move message to Junk Email folder**.</span></span> <span data-ttu-id="46365-111">또한 모든 사서함을 ZAP에 게 표시 하지 않으려는 경우 사용자 집합에만 적용 되는 새 스팸 필터 정책을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="46365-111">You can also create a new spam filter policy that applies only to a set of users if you don't want all mailboxes to be screened by ZAP.</span></span>

- <span data-ttu-id="46365-112">사용자가 기본 정크 메일 설정을 유지 했으며 정크 메일 보호를 해제 하지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="46365-112">Users have kept their default junk mail settings, and have not turned off junk email protection.</span></span> <span data-ttu-id="46365-113">(Outlook의 사용자 옵션에 대 한 자세한 내용은 [정크 메일 필터의 보호 수준 변경을](https://support.office.com/article/change-the-level-of-protection-in-the-junk-email-filter-e89c12d8-9d61-4320-8c57-d982c8d52f6b) 참조 하세요.)</span><span class="sxs-lookup"><span data-stu-id="46365-113">(See [Change the level of protection in the Junk Email Filter](https://support.office.com/article/change-the-level-of-protection-in-the-junk-email-filter-e89c12d8-9d61-4320-8c57-d982c8d52f6b) for details about user options in Outlook.)</span></span> 
  
## <a name="how-zap-works"></a><span data-ttu-id="46365-114">ZAP 작동 방식</span><span class="sxs-lookup"><span data-stu-id="46365-114">How ZAP works</span></span>

<span data-ttu-id="46365-115">Office 365에서는 매일 실시간으로 스팸 방지 엔진 및 맬웨어 서명을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="46365-115">Office 365 updates anti-spam engine and malware signatures in real-time on a daily basis.</span></span> <span data-ttu-id="46365-116">그러나 사용자에 게 콘텐츠를 배달 한 후에 weaponized를 포함 하 여 여러 가지 이유로 인해 사용자가 여전히 해당 받은 편지함에 악성 메시지를 배달 하도록 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="46365-116">However, your users might still get malicious messages delivered to their inboxes for a variety of reasons, including if content is weaponized after being delivered to users.</span></span> <span data-ttu-id="46365-117">ZAP은 Office 365 스팸 및 맬웨어 서명에 대 한 업데이트를 지속적으로 모니터링 하 여이를 해결 합니다.</span><span class="sxs-lookup"><span data-stu-id="46365-117">ZAP addresses this by continually monitoring updates to the Office 365 spam and malware signatures.</span></span> <span data-ttu-id="46365-118">ZAP은 이전에 전달한 메시지 중 사용자의 받은 편지함에 이미 배달 된 메시지가 있는지 찾아 제거할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="46365-118">ZAP can find and remove previously delivered messages that are already in users' inboxes.</span></span>

<span data-ttu-id="46365-119">사서함 사용자에 게는 ZAP 동작이 원활 하 게 수행 됩니다. 전자 메일 메시지를 이동 하는 경우이 사용자에 게 알림이 제공 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="46365-119">The ZAP action is seamless for the mailbox user; they are not notified if an email message is moved.</span></span> <span data-ttu-id="46365-120">메시지가 2 일 보다 오래 된 것은 아니어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="46365-120">Message must not be older than 2 days.</span></span>
  
<span data-ttu-id="46365-121">허용 목록, [메일 흐름 규칙](https://go.microsoft.com/fwlink/p/?LinkId=722755), 최종 사용자 규칙 또는 추가 필터는 ZAP 보다 우선 합니다.</span><span class="sxs-lookup"><span data-stu-id="46365-121">Allow lists, [mail flow rules](https://go.microsoft.com/fwlink/p/?LinkId=722755), and end user rules or additional filters take precedence over ZAP.</span></span>

<span data-ttu-id="46365-122">**맬웨어 ZAP** 새로 검색 된 맬웨어의 경우 ZAP은 전자 메일 메시지에서 첨부 파일을 제거 하 고 사용자 사서함에는 메시지 본문을 남겨 둡니다.</span><span class="sxs-lookup"><span data-stu-id="46365-122">**Malware ZAP** For newly detected malware, ZAP removes attachments from email messages, leaving the body of the message in the user's mailbox.</span></span> <span data-ttu-id="46365-123">메일의 읽기 상태에 관계 없이 첨부 파일이 제거 됩니다.</span><span class="sxs-lookup"><span data-stu-id="46365-123">Attachments are removed regardless of the read status of the mail.</span></span>

<span data-ttu-id="46365-124">맬웨어 ZAP은 맬웨어 정책에서 기본적으로 사용 하도록 설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="46365-124">Malware ZAP is enabled by default in the Malware Policy.</span></span> <span data-ttu-id="46365-125">EOP cmdlet의 **ZapEnabled** 매개 변수를 사용 하 여 [](https://docs.microsoft.com/en-us/powershell/module/exchange/antispam-antimalware/set-malwarefilterpolicy?view=exchange-ps)맬웨어 ZAP을 사용 하지 않도록 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="46365-125">Malware ZAP can be disabled using the **ZapEnabled** parameter of [Set-MalwareFilterPolicy](https://docs.microsoft.com/en-us/powershell/module/exchange/antispam-antimalware/set-malwarefilterpolicy?view=exchange-ps), an EOP cmdlet.</span></span>

<span data-ttu-id="46365-126">**피싱 ZAP** 배달 후에 피싱으로 식별 되는 메일의 경우에는 사용자에 게 적용 되는 스팸 정책에 따라 ZAP이 작업을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="46365-126">**Phish ZAP** For mail that is identified as phish after delivery, ZAP takes action according to the Spam policy that the user is covered by.</span></span> <span data-ttu-id="46365-127">피싱 action이 메일에 대해 작업을 수행 하도록 설정 된 경우 (리디렉션, 삭제, 격리, 정크로 이동) ZAP은 메일의 읽기 상태에 관계 없이 사용자의 받은 편지함에 있는 정크 메일 폴더로 메시지를 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="46365-127">If the policy Phish action is set to take action on a mail (Redirect, Delete, Quarantine, Move to Junk) then ZAP will move the message to the Junk mail folder of the user's inbox, regardless of the read status of the mail.</span></span> <span data-ttu-id="46365-128">정책 피싱 동작이 작업을 수행 하도록 설정 되지 않은 경우 (X-헤더 추가, 주체 수정, 작업 없음) ZAP은 메일에 대해 작업을 수행 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="46365-128">If the policy Phish action is not set to take action (Add X-header, Modify subject, No action) then ZAP will not take action on the mail.</span></span> <span data-ttu-id="46365-129">[스팸 필터 정책을 구성](https://docs.microsoft.com/en-us/office365/securitycompliance/configure-your-spam-filter-policies) 하는 방법에 대 한 자세한 내용은 여기에서 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="46365-129">Learn more about how to [configure your spam filter policies](https://docs.microsoft.com/en-us/office365/securitycompliance/configure-your-spam-filter-policies) here.</span></span>

<span data-ttu-id="46365-130">피싱 ZAP은 스팸 정책에서 기본적으로 사용 하도록 설정 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="46365-130">Phish ZAP is enabled by default in the Spam Policy.</span></span> <span data-ttu-id="46365-131">EOP cmdlet의 **ZapEnabled** 매개 변수를 사용 하 여 [](https://go.microsoft.com/fwlink/p/?LinkId=722758)피싱 ZAP을 사용 하지 않도록 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="46365-131">Phish ZAP can be disabled using the **ZapEnabled** parameter of [Set-HostedContentFilterPolicy](https://go.microsoft.com/fwlink/p/?LinkId=722758), an EOP cmdlet.</span></span>
<span data-ttu-id="46365-132">참고: ZapEnabled에서 피싱 ZAP 및 스팸 ZAP을 모두 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="46365-132">Note: Disabling -ZapEnabled will disable both Phish ZAP and Spam ZAP</span></span>

<span data-ttu-id="46365-133">**스팸 ZAP** 배달 후 스팸으로 확인 된 메일의 경우에는 사용자에 게 적용 되는 스팸 정책에 따라 ZAP이 작업을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="46365-133">**Spam ZAP** For mail that is identified as spam after delivery, ZAP takes action according to the Spam policy that the user is covered by.</span></span> <span data-ttu-id="46365-134">메일에 대해 작업을 수행 하도록 정책 스팸 작업을 설정한 경우 (리디렉션, 삭제, 격리, 정크로 이동), 메시지가 읽지 않은 경우에는 메시지가 사용자의 받은 편지함에 있는 정크 메일 폴더로 이동 됩니다.</span><span class="sxs-lookup"><span data-stu-id="46365-134">If the policy Spam action is set to take action on a mail (Redirect, Delete, Quarantine, Move to Junk) then ZAP will move the message to the Junk mail folder of the user's inbox, if the message is unread.</span></span> <span data-ttu-id="46365-135">정책 스팸 작업이 작업을 수행 하도록 설정 되지 않은 경우 (X-헤더 추가, 주체 수정, 작업 없음) ZAP은 메일에 대해 작업을 수행 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="46365-135">If the policy Spam action is not set to take action (Add X-header, Modify subject, No action) then ZAP will not take action on the mail.</span></span> <span data-ttu-id="46365-136">[스팸 필터 정책을 구성](https://docs.microsoft.com/en-us/office365/securitycompliance/configure-your-spam-filter-policies) 하는 방법에 대 한 자세한 내용은 여기에서 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="46365-136">Learn more about how to [configure your spam filter policies](https://docs.microsoft.com/en-us/office365/securitycompliance/configure-your-spam-filter-policies) here.</span></span>

<span data-ttu-id="46365-137">스팸 ZAP은 스팸 정책에서 기본적으로 사용 하도록 설정 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="46365-137">Spam ZAP is enabled by default in the Spam Policy.</span></span> <span data-ttu-id="46365-138">EOP cmdlet의 **ZapEnabled** 매개 변수를 사용 하 여 [](https://go.microsoft.com/fwlink/p/?LinkId=722758)스팸 ZAP을 사용 하지 않도록 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="46365-138">Spam ZAP can be disabled using the **ZapEnabled** parameter of [Set-HostedContentFilterPolicy](https://go.microsoft.com/fwlink/p/?LinkId=722758), an EOP cmdlet.</span></span>
<span data-ttu-id="46365-139">참고: ZapEnabled에서 피싱 ZAP 및 스팸 ZAP을 모두 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="46365-139">Note: Disabling -ZapEnabled will disable both Phish ZAP and Spam ZAP</span></span>

## <a name="to-see-if-zap-moved-your-message"></a><span data-ttu-id="46365-140">메시지가 ZAP에서 이동 된 것을 확인 하려면</span><span class="sxs-lookup"><span data-stu-id="46365-140">To see if ZAP moved your message</span></span>

<span data-ttu-id="46365-141">ZAP에서 메시지를 이동 했는지 확인 하려면 [위협 방지 상태 보고서](view-email-security-reports.md#threat-protection-status-report) 또는 [위협 탐색기 (및 실시간 검색)](threat-explorer.md)를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="46365-141">If you want to see if ZAP moved your message, you can use either the [Threat Protection Status report](view-email-security-reports.md#threat-protection-status-report) or [Threat Explorer (and real-time detections)](threat-explorer.md).</span></span>

## <a name="to-disable-zap"></a><span data-ttu-id="46365-142">ZAP을 사용 하지 않도록 설정 하려면</span><span class="sxs-lookup"><span data-stu-id="46365-142">To disable ZAP</span></span>
<span data-ttu-id="46365-143">**맬웨어 ZAP 사용 안 함** O365 테 넌 트 또는 사용자 집합에 대해 맬웨어 ZAP을 사용 하지 않도록 설정 하려면 EOP cmdlet의 [](https://docs.microsoft.com/en-us/powershell/module/exchange/antispam-antimalware/set-malwarefilterpolicy?view=exchange-ps) **ZapEnabled** 매개 변수를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="46365-143">**Disabling Malware ZAP** To disable Malware ZAP for your O365 tenant, or a set of users, use the **ZapEnabled** parameter of [Set-MalwareFilterPolicy](https://docs.microsoft.com/en-us/powershell/module/exchange/antispam-antimalware/set-malwarefilterpolicy?view=exchange-ps), an EOP cmdlet.</span></span>

<span data-ttu-id="46365-144">다음 예제에서는 "Test" 라는 콘텐츠 필터 정책에 대해 ZAP을 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="46365-144">In the following example, ZAP is disabled for a content filter policy named "Test".</span></span>

```Powershell
  Set-HostedContentFilterPolicy -Identity Test -ZapEnabled $false
```
<span data-ttu-id="46365-145">**피싱 및 스팸 ZAP 사용 안 함** O365 테 넌 트 또는 사용자 집합에 대해 피싱 및 스팸 ZAP을 모두 사용 하지 않도록 설정 하려면 EOP cmdlet의 [](https://go.microsoft.com/fwlink/p/?LinkId=722758) **ZapEnabled** 매개 변수를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="46365-145">**Disabling Phish and Spam ZAP** To disable both Phish and Spam ZAP for your O365 tenant, or a set of users, use the **ZapEnabled** parameter of [Set-HostedContentFilterPolicy](https://go.microsoft.com/fwlink/p/?LinkId=722758), an EOP cmdlet.</span></span>

<span data-ttu-id="46365-146">다음 예제에서는 "Test" 라는 콘텐츠 필터 정책에 대해 ZAP을 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="46365-146">In the following example, ZAP is disabled for a content filter policy named "Test".</span></span>

```Powershell
  Set-HostedContentFilterPolicy -Identity Test -ZapEnabled $false
```

## <a name="faq"></a><span data-ttu-id="46365-147">FAQ</span><span class="sxs-lookup"><span data-stu-id="46365-147">FAQ</span></span>

### <a name="what-happens-if-a-legitimate-message-is-moved-to-the-junk-mail-folder"></a><span data-ttu-id="46365-148">합법적인 메시지를 정크 메일 폴더로 이동 하면 어떻게 되나요?</span><span class="sxs-lookup"><span data-stu-id="46365-148">What happens if a legitimate message is moved to the junk mail folder?</span></span>
  
<span data-ttu-id="46365-149">[가양성](prevent-email-from-being-marked-as-spam.md)에 대 한 일반 보고 프로세스를 따라야 합니다.</span><span class="sxs-lookup"><span data-stu-id="46365-149">You should follow the normal reporting process for [false-positives](prevent-email-from-being-marked-as-spam.md).</span></span> <span data-ttu-id="46365-150">메시지를 받은 편지함에서 정크 메일 폴더로 이동 하는 유일한 이유는 서비스가 스팸 또는 악성 메시지를 받는 것으로 확인 되었기 때문입니다.</span><span class="sxs-lookup"><span data-stu-id="46365-150">The only reason the message would be moved from the inbox to the junk mail folder would be because the service has determined that the message was spam or malicious.</span></span>
  
### <a name="what-if-i-use-the-office-365-quarantine-instead-of-the-junk-mail-folder"></a><span data-ttu-id="46365-151">정크 메일 폴더 대신 Office 365 검역을 사용 하는 경우에는 어떻게 하나요?</span><span class="sxs-lookup"><span data-stu-id="46365-151">What if I use the Office 365 quarantine instead of the junk mail folder?</span></span>
  
<span data-ttu-id="46365-152">지금은 메시지를 받은 편지함에서 격리로 이동 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="46365-152">ZAP doesn't move messages into quarantine from the Inbox at this time.</span></span>
  
### <a name="what-if-i-have-a-custom-mail-flow-rule-block-allow-rule"></a><span data-ttu-id="46365-153">사용자 지정 메일 흐름 규칙 (차단/허용 규칙)이 있는 경우 어떻게 하나요?</span><span class="sxs-lookup"><span data-stu-id="46365-153">What if I have a custom mail flow rule (Block/ Allow Rule)?</span></span>
  
<span data-ttu-id="46365-154">관리자가 만든 규칙 (메일 흐름 규칙) 또는 차단 및 허용 규칙을 우선적으로 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="46365-154">Rules created by admins (mail flow rules) or Block and Allow rules take precedence.</span></span> <span data-ttu-id="46365-155">이러한 메시지는 기능 조건에서 제외 되므로 메일 흐름은 규칙 동작 (차단/허용 규칙)을 따릅니다.</span><span class="sxs-lookup"><span data-stu-id="46365-155">Such messages are excluded from the feature criteria so the mail flow will follow the rule action (Block/Allow Rule).</span></span>

### <a name="what-if-a-message-is-moved-to-another-folder-eg-inbox-rule"></a><span data-ttu-id="46365-156">다른 폴더 (예: 받은 편지함 규칙)로 메시지를 이동 하는 경우</span><span class="sxs-lookup"><span data-stu-id="46365-156">What if a message is moved to another folder (e.g. Inbox rule)?</span></span>
<span data-ttu-id="46365-157">메시지가 삭제 되었거나 정크 상태인 경우가 아니면이 경우에도 ZAP이 작동 합니다.</span><span class="sxs-lookup"><span data-stu-id="46365-157">ZAP still works in this case, unless the message has been deleted or is in Junk.</span></span>

## <a name="related-topics"></a><span data-ttu-id="46365-158">관련 주제</span><span class="sxs-lookup"><span data-stu-id="46365-158">Related Topics</span></span>

[<span data-ttu-id="46365-159">Office 365 이메일 스팸 방지 보호</span><span class="sxs-lookup"><span data-stu-id="46365-159">Office 365 Email Anti-Spam Protection</span></span>](anti-spam-protection.md)
  
[<span data-ttu-id="46365-160">Office 365 스팸 필터로 전자 메일 스팸을 차단하여 거짓 부정 문제 방지</span><span class="sxs-lookup"><span data-stu-id="46365-160">Block email spam with the Office 365 spam filter to prevent false negative issues</span></span>](reduce-spam-email.md)
