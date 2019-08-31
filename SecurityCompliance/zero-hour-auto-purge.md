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
ms.openlocfilehash: 91bb167c988e49a40895f851a518ee255abdbf08
ms.sourcegitcommit: 769b506c828c475c713dbb337e115714dcc7f17c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/31/2019
ms.locfileid: "36698970"
---
# <a name="zero-hour-auto-purge---protection-against-spam-and-malware"></a><span data-ttu-id="ceef6-104">제로 아워 자동 비우기 - 스팸 및 맬웨어로부터 보호</span><span class="sxs-lookup"><span data-stu-id="ceef6-104">Zero-hour auto purge - protection against spam and malware</span></span>

## <a name="overview"></a><span data-ttu-id="ceef6-105">개요</span><span class="sxs-lookup"><span data-stu-id="ceef6-105">Overview</span></span>

<span data-ttu-id="ceef6-106">ZAP (자동 삭제)은 사용자의 받은 편지 함으로 이미 배달 된 피싱, 스팸 또는 맬웨어가 있는 메시지를 검색 한 다음 악성 콘텐츠 무해 함을 렌더링 하는 전자 메일 보호 기능입니다.</span><span class="sxs-lookup"><span data-stu-id="ceef6-106">Zero-hour auto purge (ZAP) is an email protection feature that detects messages with phish, spam, or malware that have already been delivered to your users' inboxes, and then renders the malicious content harmless.</span></span> <span data-ttu-id="ceef6-107">ZAP이 수행 하는 방법은 검색 된 악의적인 콘텐츠의 유형에 따라 다릅니다. 메일은 mail content, Url 또는 attachments로 인해 zapped 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ceef6-107">How ZAP does this depends on the type of malicious content detected; mail can be zapped due to mail content, URLs, or attachments.</span></span>
  
<span data-ttu-id="ceef6-108">ZAP은 Exchange Online 사서함이 포함 된 모든 Office 365 구독에 포함 된 기본 Exchange Online Protection에서 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ceef6-108">ZAP is available with the default Exchange Online Protection that is included with any Office 365 subscription that contains Exchange Online mailboxes.</span></span>

<span data-ttu-id="ceef6-109">ZAP은 기본적으로 설정 되어 있지만 다음 조건을 충족 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ceef6-109">ZAP is turned on by default, but the following conditions must be met:</span></span>
  
- <span data-ttu-id="ceef6-110">**스팸 작업** 은 **정크 메일 폴더로 메시지를 이동**하도록 설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ceef6-110">**Spam action** is set to **Move message to Junk Email folder**.</span></span> <span data-ttu-id="ceef6-111">또한 모든 사서함을 ZAP에 게 표시 하지 않으려는 경우 사용자 집합에만 적용 되는 새 스팸 필터 정책을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ceef6-111">You can also create a new spam filter policy that applies only to a set of users if you don't want all mailboxes to be screened by ZAP.</span></span>

- <span data-ttu-id="ceef6-112">사용자가 기본 정크 메일 설정을 유지 했으며 정크 메일 보호를 해제 하지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="ceef6-112">Users have kept their default junk mail settings, and have not turned off junk email protection.</span></span> <span data-ttu-id="ceef6-113">(Outlook의 사용자 옵션에 대 한 자세한 내용은 [정크 메일 필터의 보호 수준 변경을](https://support.office.com/article/e89c12d8-9d61-4320-8c57-d982c8d52f6b) 참조 하세요.)</span><span class="sxs-lookup"><span data-stu-id="ceef6-113">(See [Change the level of protection in the Junk Email Filter](https://support.office.com/article/e89c12d8-9d61-4320-8c57-d982c8d52f6b) for details about user options in Outlook.)</span></span>
  
## <a name="how-zap-works"></a><span data-ttu-id="ceef6-114">ZAP 작동 방식</span><span class="sxs-lookup"><span data-stu-id="ceef6-114">How ZAP works</span></span>

<span data-ttu-id="ceef6-115">Office 365에서는 매일 실시간으로 스팸 방지 엔진 및 맬웨어 서명을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="ceef6-115">Office 365 updates anti-spam engine and malware signatures in real-time on a daily basis.</span></span> <span data-ttu-id="ceef6-116">그러나 사용자에 게 콘텐츠를 배달 한 후에 weaponized를 포함 하 여 여러 가지 이유로 인해 사용자가 여전히 해당 받은 편지함에 악성 메시지를 배달 하도록 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ceef6-116">However, your users might still get malicious messages delivered to their inboxes for a variety of reasons, including if content is weaponized after being delivered to users.</span></span> <span data-ttu-id="ceef6-117">ZAP은 Office 365 스팸 및 맬웨어 서명에 대 한 업데이트를 지속적으로 모니터링 하 여이를 해결 합니다.</span><span class="sxs-lookup"><span data-stu-id="ceef6-117">ZAP addresses this by continually monitoring updates to the Office 365 spam and malware signatures.</span></span> <span data-ttu-id="ceef6-118">ZAP은 이전에 전달한 메시지 중 사용자의 받은 편지함에 이미 배달 된 메시지가 있는지 찾아 제거할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ceef6-118">ZAP can find and remove previously delivered messages that are already in users' inboxes.</span></span>

<span data-ttu-id="ceef6-119">사서함 사용자에 게는 ZAP 동작이 원활 하 게 수행 됩니다. 전자 메일 메시지를 이동 하는 경우이 사용자에 게 알림이 제공 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ceef6-119">The ZAP action is seamless for the mailbox user; they are not notified if an email message is moved.</span></span> <span data-ttu-id="ceef6-120">메시지가 2 일 보다 오래 된 것은 아니어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ceef6-120">Message must not be older than 2 days.</span></span>
  
<span data-ttu-id="ceef6-121">허용 목록, [메일 흐름 규칙](https://go.microsoft.com/fwlink/p/?LinkId=722755) (전송 규칙이 라고도 함) 및 최종 사용자 규칙 또는 추가 필터가 ZAP 보다 우선적으로 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ceef6-121">Allow lists, [mail flow rules](https://go.microsoft.com/fwlink/p/?LinkId=722755) (also known as transport rules), and end user rules or additional filters take precedence over ZAP.</span></span>

### <a name="malware-zap"></a><span data-ttu-id="ceef6-122">맬웨어 ZAP</span><span class="sxs-lookup"><span data-stu-id="ceef6-122">Malware ZAP</span></span>

<span data-ttu-id="ceef6-123">새로 검색 된 맬웨어의 경우 ZAP은 전자 메일 메시지에서 첨부 파일을 제거 하 고 사용자 사서함에는 메시지 본문을 남겨 둡니다.</span><span class="sxs-lookup"><span data-stu-id="ceef6-123">For newly detected malware, ZAP removes attachments from email messages, leaving the body of the message in the user's mailbox.</span></span> <span data-ttu-id="ceef6-124">메일의 읽기 상태에 관계 없이 첨부 파일이 제거 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ceef6-124">Attachments are removed regardless of the read status of the mail.</span></span>

<span data-ttu-id="ceef6-125">맬웨어 ZAP은 맬웨어 정책에서 기본적으로 사용 하도록 설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ceef6-125">Malware ZAP is enabled by default in the Malware Policy.</span></span> <span data-ttu-id="ceef6-126">Exchange Online PowerShell 또는 Exchange Online Protection PowerShell의 [get-malwarefilterpolicy](https://docs.microsoft.com/powershell/module/exchange/antispam-antimalware/set-malwarefilterpolicy) Cmdlet에서 *ZapEnabled* 매개 변수를 사용 하 여 맬웨어 ZAP을 사용 하지 않도록 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ceef6-126">You can disable Malware ZAP by using the *ZapEnabled* parameter on the [Set-MalwareFilterPolicy](https://docs.microsoft.com/powershell/module/exchange/antispam-antimalware/set-malwarefilterpolicy) cmdlet in Exchange Online PowerShell or Exchange Online Protection PowerShell.</span></span>

### <a name="phish-zap"></a><span data-ttu-id="ceef6-127">피싱 ZAP</span><span class="sxs-lookup"><span data-stu-id="ceef6-127">Phish ZAP</span></span>

<span data-ttu-id="ceef6-128">배달 후에 피싱으로 식별 되는 메일의 경우에는 사용자에 게 적용 되는 스팸 정책에 따라 ZAP이 작업을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="ceef6-128">For mail that is identified as phish after delivery, ZAP takes action according to the Spam policy that the user is covered by.</span></span> <span data-ttu-id="ceef6-129">피싱 action이 메일에 대해 작업을 수행 하도록 설정 된 경우 (리디렉션, 삭제, 격리, 정크로 이동) ZAP은 메일의 읽기 상태에 관계 없이 사용자의 받은 편지함에 있는 정크 메일 폴더로 메시지를 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="ceef6-129">If the policy Phish action is set to take action on a mail (Redirect, Delete, Quarantine, Move to Junk) then ZAP will move the message to the Junk mail folder of the user's inbox, regardless of the read status of the mail.</span></span> <span data-ttu-id="ceef6-130">정책 피싱 동작이 작업을 수행 하도록 설정 되지 않은 경우 (X-헤더 추가, 주체 수정, 작업 없음) ZAP은 메일에 대해 작업을 수행 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ceef6-130">If the policy Phish action is not set to take action (Add X-header, Modify subject, No action) then ZAP will not take action on the mail.</span></span> <span data-ttu-id="ceef6-131">[스팸 필터 정책을 구성](https://docs.microsoft.com//office365/securitycompliance/configure-your-spam-filter-policies) 하는 방법에 대 한 자세한 내용은 여기에서 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ceef6-131">Learn more about how to [configure your spam filter policies](https://docs.microsoft.com//office365/securitycompliance/configure-your-spam-filter-policies) here.</span></span>

<span data-ttu-id="ceef6-132">피싱 ZAP은 스팸 정책에서 기본적으로 사용 하도록 설정 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ceef6-132">Phish ZAP is enabled by default in the Spam Policy.</span></span> <span data-ttu-id="ceef6-133">Exchange Online PowerShell 또는 Exchange Online Protection PowerShell의 [get-hostedcontentfilterpolicy](https://go.microsoft.com/fwlink/p/?LinkId=722758) Cmdlet에서 *ZapEnabled* 매개 변수를 사용 하 여 피싱 ZAP을 사용 하지 않도록 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ceef6-133">You can disable Phish ZAP by using the *ZapEnabled* parameter on the [Set-HostedContentFilterPolicy](https://go.microsoft.com/fwlink/p/?LinkId=722758) cmdlet in Exchange Online PowerShell or Exchange Online Protection PowerShell.</span></span>

### <a name="spam-zap"></a><span data-ttu-id="ceef6-134">스팸 ZAP</span><span class="sxs-lookup"><span data-stu-id="ceef6-134">Spam ZAP</span></span>

<span data-ttu-id="ceef6-135">배달 후 스팸으로 확인 된 메일의 경우에는 사용자에 게 적용 되는 스팸 정책에 따라 ZAP이 작업을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="ceef6-135">For mail that is identified as spam after delivery, ZAP takes action according to the Spam policy that the user is covered by.</span></span> <span data-ttu-id="ceef6-136">메일에 대해 작업을 수행 하도록 정책 스팸 작업을 설정한 경우 (리디렉션, 삭제, 격리, 정크로 이동), 메시지가 읽지 않은 경우에는 메시지가 사용자의 받은 편지함에 있는 정크 메일 폴더로 이동 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ceef6-136">If the policy Spam action is set to take action on a mail (Redirect, Delete, Quarantine, Move to Junk) then ZAP will move the message to the Junk mail folder of the user's inbox, if the message is unread.</span></span> <span data-ttu-id="ceef6-137">정책 스팸 작업이 작업을 수행 하도록 설정 되지 않은 경우 (X-헤더 추가, 주체 수정, 작업 없음) ZAP은 메일에 대해 작업을 수행 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ceef6-137">If the policy Spam action is not set to take action (Add X-header, Modify subject, No action) then ZAP will not take action on the mail.</span></span> <span data-ttu-id="ceef6-138">[스팸 필터 정책을 구성](configure-your-spam-filter-policies.md) 하는 방법에 대 한 자세한 내용은 여기에서 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ceef6-138">Learn more about how to [Configure your spam filter policies](configure-your-spam-filter-policies.md) here.</span></span>

<span data-ttu-id="ceef6-139">스팸 ZAP은 스팸 정책에서 기본적으로 사용 하도록 설정 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ceef6-139">Spam ZAP is enabled by default in the Spam Policy.</span></span> <span data-ttu-id="ceef6-140">Exchange Online PowerShell 또는 Exchange Online Protection PowerShell에서 [get-hostedcontentfilterpolicy](https://go.microsoft.com/fwlink/p/?LinkId=722758) Cmdlet의 *ZapEnabled* 매개 변수를 사용 하 여 스팸 ZAP을 사용 하지 않도록 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ceef6-140">You can disable Spam ZAP by using the *ZapEnabled* parameter of [Set-HostedContentFilterPolicy](https://go.microsoft.com/fwlink/p/?LinkId=722758) cmdlet in Exchange Online PowerShell or Exchange Online Protection PowerShell.</span></span>

> [!NOTE]
> <span data-ttu-id="ceef6-141">**Get-hostedcontentfilterpolicy** Cmdlet의 *ZapEnabled* 매개 변수는 정책에 대해 피싱 ZAP 및 스팸 ZAP을 모두 사용 하지 않도록 설정 하거나 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ceef6-141">The *ZapEnabled* parameter on the **Set-HostedContentFilterPolicy** cmdlet disables or enables both Phish ZAP and Spam ZAP for the policy.</span></span> <span data-ttu-id="ceef6-142">동일한 정책 내에서 피싱 ZAP과 스팸 ZAP을 독립적으로 사용 하거나 사용 하지 않도록 설정할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="ceef6-142">You can't independently enable or disable Phish ZAP and Spam ZAP within the same policy.</span></span>

## <a name="how-to-see-if-zap-moved-your-message"></a><span data-ttu-id="ceef6-143">메시지가 ZAP에서 이동 된 것을 확인 하는 방법</span><span class="sxs-lookup"><span data-stu-id="ceef6-143">How to see if ZAP moved your message</span></span>

<span data-ttu-id="ceef6-144">ZAP이 메시지를 이동 했는지 확인 하려면 [위협 방지 상태 보고서](view-email-security-reports.md#threat-protection-status-report) 또는 [위협 탐색기 (및 실시간 검색)](threat-explorer.md)를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ceef6-144">To determine if ZAP moved your message, you can use either the [Threat Protection Status report](view-email-security-reports.md#threat-protection-status-report) or [Threat Explorer (and real-time detections)](threat-explorer.md).</span></span>

## <a name="disable-zap"></a><span data-ttu-id="ceef6-145">ZAP 사용 안 함</span><span class="sxs-lookup"><span data-stu-id="ceef6-145">Disable ZAP</span></span>

<span data-ttu-id="ceef6-146">Exchange Online PowerShell에 연결하려면 [Exchange Online PowerShell에 연결](https://go.microsoft.com/fwlink/p/?linkid=396554)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="ceef6-146">To connect to Exchange Online PowerShell, see [Connect to Exchange Online PowerShell](https://go.microsoft.com/fwlink/p/?linkid=396554).</span></span> <span data-ttu-id="ceef6-147">Exchange Online Protection PowerShell에 연결 하려면 [Exchange Online Protection powershell에 연결](https://go.microsoft.com/fwlink/p/?linkid=627290)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="ceef6-147">To connect to Exchange Online Protection PowerShell, see [Connect to Exchange Online Protection PowerShell](https://go.microsoft.com/fwlink/p/?linkid=627290).</span></span>

### <a name="disable-malware-zap"></a><span data-ttu-id="ceef6-148">맬웨어 ZAP 사용 안 함 \* \*</span><span class="sxs-lookup"><span data-stu-id="ceef6-148">Disable Malware ZAP\*\*</span></span>

<span data-ttu-id="ceef6-149">이 예에서는 "Test" 라는 맬웨어 필터 정책에서 ZAP을 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ceef6-149">This example disables ZAP in the malware filter policy named "Test".</span></span>

```Powershell
Set-MalwareFilterPolicy -Identity Test -ZapEnabled $false
```

<span data-ttu-id="ceef6-150">구문 및 매개 변수에 대 한 자세한 내용은 [get-malwarefilterpolicy](https://docs.microsoft.com/powershell/module/exchange/antispam-antimalware/set-malwarefilterpolicy)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="ceef6-150">For detailed syntax and parameter information, see [Set-MalwareFilterPolicy](https://docs.microsoft.com/powershell/module/exchange/antispam-antimalware/set-malwarefilterpolicy).</span></span>

### <a name="disable-phish-zap-and-spam-zap"></a><span data-ttu-id="ceef6-151">피싱 ZAP 및 스팸 ZAP 사용 안 함</span><span class="sxs-lookup"><span data-stu-id="ceef6-151">Disable Phish ZAP and Spam ZAP</span></span>

<span data-ttu-id="ceef6-152">이 예에서는 "Test" 라는 콘텐츠 필터 정책에서 피싱 ZAP 및 스팸 ZAP을 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ceef6-152">This example disables Phish ZAP and Spam ZAP in the content filter policy named "Test".</span></span>

```Powershell
Set-HostedContentFilterPolicy -Identity Test -ZapEnabled $false
```

<span data-ttu-id="ceef6-153">구문 및 매개 변수에 대 한 자세한 내용은 [get-hostedcontentfilterpolicy](https://go.microsoft.com/fwlink/p/?LinkId=722758)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="ceef6-153">For detailed syntax and parameter information, see [Set-HostedContentFilterPolicy](https://go.microsoft.com/fwlink/p/?LinkId=722758).</span></span>

## <a name="faq"></a><span data-ttu-id="ceef6-154">FAQ</span><span class="sxs-lookup"><span data-stu-id="ceef6-154">FAQ</span></span>

### <a name="what-happens-if-a-legitimate-message-is-moved-to-the-junk-mail-folder"></a><span data-ttu-id="ceef6-155">합법적인 메시지를 정크 메일 폴더로 이동 하면 어떻게 되나요?</span><span class="sxs-lookup"><span data-stu-id="ceef6-155">What happens if a legitimate message is moved to the junk mail folder?</span></span>
  
<span data-ttu-id="ceef6-156">[가양성](prevent-email-from-being-marked-as-spam.md)에 대 한 일반 보고 프로세스를 따라야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ceef6-156">You should follow the normal reporting process for [false-positives](prevent-email-from-being-marked-as-spam.md).</span></span> <span data-ttu-id="ceef6-157">메시지를 받은 편지함에서 정크 메일 폴더로 이동 하는 유일한 이유는 서비스가 스팸 또는 악성 메시지를 받는 것으로 확인 되었기 때문입니다.</span><span class="sxs-lookup"><span data-stu-id="ceef6-157">The only reason the message would be moved from the inbox to the junk mail folder would be because the service has determined that the message was spam or malicious.</span></span>
  
### <a name="what-if-i-use-the-office-365-quarantine-instead-of-the-junk-mail-folder"></a><span data-ttu-id="ceef6-158">정크 메일 폴더 대신 Office 365 검역을 사용 하는 경우에는 어떻게 하나요?</span><span class="sxs-lookup"><span data-stu-id="ceef6-158">What if I use the Office 365 quarantine instead of the junk mail folder?</span></span>
  
<span data-ttu-id="ceef6-159">지금은 메시지를 받은 편지함에서 격리로 이동 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ceef6-159">ZAP doesn't move messages into quarantine from the Inbox at this time.</span></span>
  
### <a name="what-if-i-have-a-custom-mail-flow-rule-block-allow-rule"></a><span data-ttu-id="ceef6-160">사용자 지정 메일 흐름 규칙 (차단/허용 규칙)이 있는 경우 어떻게 하나요?</span><span class="sxs-lookup"><span data-stu-id="ceef6-160">What if I have a custom mail flow rule (Block/ Allow Rule)?</span></span>
  
<span data-ttu-id="ceef6-161">관리자가 만든 규칙 (메일 흐름 규칙) 또는 차단 및 허용 규칙을 우선적으로 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="ceef6-161">Rules created by admins (mail flow rules) or Block and Allow rules take precedence.</span></span> <span data-ttu-id="ceef6-162">이러한 메시지는 기능 조건에서 제외 되므로 메일 흐름은 규칙 동작 (차단/허용 규칙)을 따릅니다.</span><span class="sxs-lookup"><span data-stu-id="ceef6-162">Such messages are excluded from the feature criteria so the mail flow will follow the rule action (Block/Allow Rule).</span></span>

### <a name="what-if-a-message-is-moved-to-another-folder-eg-inbox-rule"></a><span data-ttu-id="ceef6-163">다른 폴더 (예: 받은 편지함 규칙)로 메시지를 이동 하는 경우</span><span class="sxs-lookup"><span data-stu-id="ceef6-163">What if a message is moved to another folder (e.g. Inbox rule)?</span></span>

<span data-ttu-id="ceef6-164">메시지가 삭제 되었거나 정크 상태인 경우가 아니면이 경우에도 ZAP이 작동 합니다.</span><span class="sxs-lookup"><span data-stu-id="ceef6-164">ZAP still works in this case, unless the message has been deleted or is in Junk.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ceef6-165">관련 주제</span><span class="sxs-lookup"><span data-stu-id="ceef6-165">Related Topics</span></span>

[<span data-ttu-id="ceef6-166">Office 365 이메일 스팸 방지 보호</span><span class="sxs-lookup"><span data-stu-id="ceef6-166">Office 365 Email Anti-Spam Protection</span></span>](anti-spam-protection.md)
  
[<span data-ttu-id="ceef6-167">Office 365 스팸 필터로 전자 메일 스팸을 차단하여 거짓 부정 문제 방지</span><span class="sxs-lookup"><span data-stu-id="ceef6-167">Block email spam with the Office 365 spam filter to prevent false negative issues</span></span>](reduce-spam-email.md)
