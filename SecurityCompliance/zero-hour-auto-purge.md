---
title: 제로 아워 자동 비우기 - 스팸 및 맬웨어로부터 보호
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 10/23/2018
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MED150
- MBS150
- MET150
ms.assetid: 96deb75f-64e8-4c10-b570-84c99c674e15
description: 0-시간 자동 삭제 (ZAP) 스팸 또는 맬웨어로와 사용자의 받은 편지함에 이미 배달 된 메시지를 검색 하는 전자 메일 보호 기능 및 다음 치명적이 지 악의적인 콘텐츠를 렌더링 합니다. 어떻게 ZAP이 작업을 수행 하는 작업은 감지 악의적인 콘텐츠 형식에 따라 다릅니다.
ms.openlocfilehash: ac181a7c57b4b16a952ff9c046edbff1380828d1
ms.sourcegitcommit: 791d23e1c2dea622b6ef77a6e2bde32e1d31a41b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/06/2018
ms.locfileid: "25999981"
---
# <a name="zero-hour-auto-purge---protection-against-spam-and-malware"></a><span data-ttu-id="ae2b4-104">제로 아워 자동 비우기 - 스팸 및 맬웨어로부터 보호</span><span class="sxs-lookup"><span data-stu-id="ae2b4-104">Zero-hour auto purge - protection against spam and malware</span></span>

## <a name="overview"></a><span data-ttu-id="ae2b4-105">개요</span><span class="sxs-lookup"><span data-stu-id="ae2b4-105">Overview</span></span>

<span data-ttu-id="ae2b4-p102">0-시간 자동 삭제 (ZAP) 스팸 또는 맬웨어로와 사용자의 받은 편지함에 이미 배달 된 메시지를 검색 하는 전자 메일 보호 기능 및 다음 치명적이 지 악의적인 콘텐츠를 렌더링 합니다. 어떻게 ZAP이 작업을 수행 하는 작업은 감지 악의적인 콘텐츠 형식에 따라 다릅니다.</span><span class="sxs-lookup"><span data-stu-id="ae2b4-p102">Zero-hour auto purge (ZAP) is an email protection feature that detects messages with spam or malware that have already been delivered to your users' inboxes, and then renders the malicious content harmless. How ZAP does this depends on the type of malicious content detected.</span></span>
  
<span data-ttu-id="ae2b4-108">ZAP은 Exchange Online 사서함이 포함 된 모든 Office 365 구독의 함께 제공 되는 Exchange Online Protection 기본 제공 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ae2b4-108">ZAP is available with the default Exchange Online Protection that is included with any Office 365 subscription that contains Exchange Online mailboxes.</span></span>

<span data-ttu-id="ae2b4-109">기본적으로 ZAP 켜져 있지만 다음 조건이 충족 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae2b4-109">ZAP is turned on by default, but the folowing conditions must be met:</span></span>
  
- <span data-ttu-id="ae2b4-110">**스팸 동작** 는 **정크 메일 폴더로 메시지 이동**으로 설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ae2b4-110">**Spam action** is set to **Move message to Junk Email folder**.</span></span> <br/><span data-ttu-id="ae2b4-111">모든 사서함 ZAP으로 검사 하지 않으려면 사용자 집합에만 적용 되는 스팸 필터 정책을 새로 만들 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ae2b4-111">You can also create a new spam filter policy that applies only to a set of users if you don't want all mailboxes to be screened by ZAP.</span></span>

- <span data-ttu-id="ae2b4-p103">사용자가 유지가 기본 정크 메일 설정 하 고 정크 메일 보호를 해제 하지 않은. (Outlook에서 사용자 옵션에 대 한 자세한 내용은 [정크 메일 필터의 보호 기능 수준을 변경](https://support.office.com/article/change-the-level-of-protection-in-the-junk-email-filter-e89c12d8-9d61-4320-8c57-d982c8d52f6b) 을 참조 하십시오.)</span><span class="sxs-lookup"><span data-stu-id="ae2b4-p103">Users have kept their default junk mail settings, and have not turned off junk email protection. (See [Change the level of protection in the Junk Email Filter](https://support.office.com/article/change-the-level-of-protection-in-the-junk-email-filter-e89c12d8-9d61-4320-8c57-d982c8d52f6b) for details about user options in Outlook.)</span></span> 
  
## <a name="how-does-zap-work"></a><span data-ttu-id="ae2b4-114">ZAP는 어떻게 작동 합니까?</span><span class="sxs-lookup"><span data-stu-id="ae2b4-114">How does ZAP work?</span></span>

<span data-ttu-id="ae2b4-p104">Office 365에서 스팸 방지 엔진 및 맬웨어 서명 업데이트를 매일 실시간 합니다. 그러나 사용자에 게 다양 한 콘텐츠를 사용자에 게 배달 되지 후 weaponized 하는 경우를 포함 하 여 이유 때문에 대 한 받은 편지함에 배달 된 악의적인 메시지를 계속 가져올 수 있습니다. ZAP 계속 해 서 Office 365 스팸 및 맬웨어로부터 서명에 대 한 업데이트를 모니터링 하 여이 해결 합니다. ZAP 검색 하 고 사용자의 받은 편지함에 이미 있는 이전에 배달 된 메시지를 제거할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ae2b4-p104">Office 365 updates anti-spam engine and malware signatures in real-time on a daily basis. However, your users might still get malicious messages delivered to their inboxes for a variety of reasons, including if content is weaponized after being delivered to users. ZAP addresses this by continually monitoring updates to the Office 365 spam and malware signatures. ZAP can find and remove previously delivered messages that are already in users' inboxes.</span></span> 
- <span data-ttu-id="ae2b4-119">스팸으로 식별 되는 메일에 대 한 ZAP 읽지 않은 메시지를 사용자의 정크 메일 폴더로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae2b4-119">For mail that is identified as spam, ZAP moves unread messages to users' Junk mail folder.</span></span> 
- <span data-ttu-id="ae2b4-120">새로 검색 된 맬웨어 ZAP는 전자 메일을 읽은 여부에 관계 없이 전자 메일 메시지에서 첨부 파일을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae2b4-120">For newly detected malware, ZAP removes attachments from email messages, regardless of whether the email has been read.</span></span> 
  
<span data-ttu-id="ae2b4-121">ZAP 매크로 함수는 사서함 사용자; 원활 하 게 전자 메일 메시지를 이동 하는 경우에 이러한는 알림을 받지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ae2b4-121">The ZAP action is seamless for the mailbox user; they are not notified if an email message is moved.</span></span>
  
<span data-ttu-id="ae2b4-122">목록, [메일 흐름 규칙](https://go.microsoft.com/fwlink/p/?LinkId=722755)및 최종 사용자 규칙을 허용 또는 추가 필터를 ZAP 보다 우선 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae2b4-122">Allow lists, [mail flow rules](https://go.microsoft.com/fwlink/p/?LinkId=722755), and end user rules or additional filters take precedence over ZAP.</span></span>
  
## <a name="to-review-or-set-up-a-spam-filter-policy"></a><span data-ttu-id="ae2b4-123">검토 하거나 스팸 필터 정책을 설정 하려면</span><span class="sxs-lookup"><span data-stu-id="ae2b4-123">To review or set up a spam filter policy</span></span>
  
1. <span data-ttu-id="ae2b4-124">이동 [https://protection.office.com](https://protection.office.com) 및 Office 365에 대 한 작업이 나 교육용 계정을 사용 하 여 로그인 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae2b4-124">Go to [https://protection.office.com](https://protection.office.com) and sign in using your work or school account for Office 365.</span></span>
2. <span data-ttu-id="ae2b4-125">**위협 관리** **스팸 방지**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae2b4-125">Under **Threat management**, choose **Anti-spam**.</span></span>
3. <span data-ttu-id="ae2b4-126">표준 설정을 검토 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae2b4-126">Review the standard settings.</span></span> 
4. <span data-ttu-id="ae2b4-p105">설정을 사용자 지정 하려는 경우 **사용자 지정** 탭을 선택 하 고 **사용자 지정 설정**사용 합니다. 설정을 편집 하 고 원할 경우 **+ 정책 만들기** 새 정책을 추가 하려면 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae2b4-p105">If you want to customize your settings, select the **Custom** tab, and turn on **Custom settings**. Edit your settings and if you want, choose **+ Create a policy** to add a new policy.</span></span> 
    
## <a name="to-see-if-zap-moved-your-message"></a><span data-ttu-id="ae2b4-129">ZAP 메시지를 이동 하는 경우를 확인 하려면</span><span class="sxs-lookup"><span data-stu-id="ae2b4-129">To see if ZAP moved your message</span></span>

<span data-ttu-id="ae2b4-130">ZAP 메시지를 이동 하는 경우 확인 하려는 경우에 또는 중 하나는 [위협 보호 상태 보고서](view-email-security-reports.md#threat-protection-status-report-new) ( [위협 탐색기](use-explorer-in-security-and-compliance.md))를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ae2b4-130">If you want to see if ZAP moved your message, you can use either the [Threat Protection Status report](view-email-security-reports.md#threat-protection-status-report-new) (or [Threat Explorer](use-explorer-in-security-and-compliance.md)).</span></span>
    
## <a name="to-disable-zap"></a><span data-ttu-id="ae2b4-131">ZAP를 사용 하지 않도록 설정 하려면</span><span class="sxs-lookup"><span data-stu-id="ae2b4-131">To disable ZAP</span></span>
  
<span data-ttu-id="ae2b4-132">사용 하지 않도록 설정 하려는 경우 Office 365 테 넌 트에 대 한 ZAP 또는 사용자 집합을 [Set-hostedcontentfilterpolicy](https://go.microsoft.com/fwlink/p/?LinkId=722758), EOP cmdlet의 **ZapEnabled** 매개 변수를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae2b4-132">If you want to disable ZAP for your Office 365 tenant, or a set of users, use the **ZapEnabled** parameter of [Set-HostedContentFilterPolicy](https://go.microsoft.com/fwlink/p/?LinkId=722758), an EOP cmdlet.</span></span>
    
<span data-ttu-id="ae2b4-133">다음 예제에서는 ZAP은 "Test" 라는 콘텐츠 필터 정책에 대해 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="ae2b4-133">In the following example, ZAP is disabled for a content filter policy named "Test".</span></span>
    
```
  Set-HostedContentFilterPolicy -Identity Test -ZapEnabled $false
```

## <a name="faq"></a><span data-ttu-id="ae2b4-134">FAQ</span><span class="sxs-lookup"><span data-stu-id="ae2b4-134">FAQ</span></span>

### <a name="what-happens-if-a-legitimate-message-is-moved-to-the-junk-mail-folder"></a><span data-ttu-id="ae2b4-135">합법적인 메시지는 정크 메일 폴더로 이동 하는 경우 어떻게 됩니까?</span><span class="sxs-lookup"><span data-stu-id="ae2b4-135">What happens if a legitimate message is moved to the junk mail folder?</span></span>
  
<span data-ttu-id="ae2b4-p106">False 양수에 대 한 일반 보고 프로세스를 따라야 합니다. 정크 메일 폴더로 메시지를 받은 편지함에서 이동할 수는 유일한 이유는 서비스에서 메시지 스팸 했음을 확인가 때문에 것 또는 악의적 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae2b4-p106">You should follow the normal reporting process for false-positives. The only reason the message would be moved from the inbox to the junk mail folder would be because the service has determined that the message was spam or malicious.</span></span>
  
### <a name="what-if-i-use-the-office-365-quarantine-instead-of-the-junk-mail-folder"></a><span data-ttu-id="ae2b4-138">경우에 어떻게 정크 메일 폴더 대신 Office 365 격리를 사용 합니까?</span><span class="sxs-lookup"><span data-stu-id="ae2b4-138">What if I use the Office 365 quarantine instead of the junk mail folder?</span></span>
  
<span data-ttu-id="ae2b4-139">ZAP 지금은 메시지를 격리에 받은 편지함에서 이동 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ae2b4-139">ZAP doesn't move messages into quarantine from the Inbox at this time.</span></span>
  
### <a name="what-if-i-have-a-custom-mail-flow-rule-block-allow-rule"></a><span data-ttu-id="ae2b4-140">사용자 지정 메일 흐름 규칙을 경우에 어떻게 해야 합니까 (차단 / 허용 규칙)?</span><span class="sxs-lookup"><span data-stu-id="ae2b4-140">What If I have a custom mail flow rule (Block/ Allow Rule)?</span></span>
  
<span data-ttu-id="ae2b4-p107">관리자 (메일 흐름 규칙) 또는 허용 및 차단 규칙에서 만든 규칙이 우선 합니다. 이러한 메시지 기능 조건에서 제외 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ae2b4-p107">Rules created by admins (mail flow rules) or Block and Allow rules take precedence. Such messages are excluded from the feature criteria.</span></span>
  
## <a name="related-topics"></a><span data-ttu-id="ae2b4-143">관련 항목</span><span class="sxs-lookup"><span data-stu-id="ae2b4-143">Related Topics</span></span>

[<span data-ttu-id="ae2b4-144">Office 365 전자 메일 스팸 방지 보호</span><span class="sxs-lookup"><span data-stu-id="ae2b4-144">Office 365 Email Anti-Spam Protection</span></span>](anti-spam-protection.md)
  
[<span data-ttu-id="ae2b4-145">Office 365 스팸 필터로 전자 메일 스팸을 차단하여 거짓 부정 문제 방지</span><span class="sxs-lookup"><span data-stu-id="ae2b4-145">Block email spam with the Office 365 spam filter to prevent false negative issues</span></span>](block-email-spam-to-prevent-false-negatives.md)
  

