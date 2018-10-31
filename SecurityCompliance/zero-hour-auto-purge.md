---
title: 제로 아워 자동 비우기 - 스팸 및 맬웨어로부터 보호
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 1/9/2018
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
ms.openlocfilehash: dabe4caf8916d3f0de7a70cb3d056dd9a7fdcc3f
ms.sourcegitcommit: ceb70ea863d8b97afea077a04fc7ec612b870695
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25857246"
---
# <a name="zero-hour-auto-purge---protection-against-spam-and-malware"></a><span data-ttu-id="171ee-104">제로 아워 자동 비우기 - 스팸 및 맬웨어로부터 보호</span><span class="sxs-lookup"><span data-stu-id="171ee-104">Zero-hour auto purge - protection against spam and malware</span></span>

<span data-ttu-id="171ee-p102">0-시간 자동 삭제 (ZAP) 스팸 또는 맬웨어로와 사용자의 받은 편지함에 이미 배달 된 메시지를 검색 하는 전자 메일 보호 기능 및 다음 치명적이 지 악의적인 콘텐츠를 렌더링 합니다. 어떻게 ZAP이 작업을 수행 하는 작업은 감지 악의적인 콘텐츠 형식에 따라 다릅니다.</span><span class="sxs-lookup"><span data-stu-id="171ee-p102">Zero-hour auto purge (ZAP) is an email protection feature that detects messages with spam or malware that have already been delivered to your users' inboxes, and then renders the malicious content harmless. How ZAP does this depends on the type of malicious content detected.</span></span>
  
<span data-ttu-id="171ee-107">ZAP은 Exchange Online 사서함이 포함 된 모든 Office 365 구독의 함께 제공 되는 Exchange Online Protection 기본 제공 됩니다.</span><span class="sxs-lookup"><span data-stu-id="171ee-107">ZAP is available with the default Exchange Online Protection that is included with any Office 365 subscription that contains Exchange Online mailboxes.</span></span>
  
## <a name="how-does-zap-work"></a><span data-ttu-id="171ee-108">ZAP는 어떻게 작동 합니까?</span><span class="sxs-lookup"><span data-stu-id="171ee-108">How does ZAP work?</span></span>

<span data-ttu-id="171ee-p103">Office 365에서 스팸 방지 엔진 및 맬웨어 서명 업데이트를 매일 실시간 합니다. 그러나 사용자에 게 다양 한 콘텐츠를 사용자에 게 처음 제공 된 후에 한번에 weaponized 다음을 수행할 때의 이유로 대 한 받은 편지함에 배달 된 악의적인 메시지를 계속 가져올 수 있습니다. Office 365 스팸 및 맬웨어로부터 서명을 업데이트 하는 계속 해 서를 모니터링 하 여이 주소 ZAP 하 고 따라서 찾아 수 받은 편지함에 이미 이전에 배달 된 메시지를 제거 합니다. 이미 스팸으로 식별 된 메일에 대 한 ZAP 읽지 않은 메시지를 사용자의 정크 메일 폴더로 이동 합니다. 새로 검색 된 맬웨어 ZAP 메일을 읽은 여부에 관계 없이 전자 메일 메시지에서 첨부 파일을 제거 합니다. 반대로 악성 소프트웨어로 하지 분류 잘못 된 메시지에 대 한 마찬가지입니다.</span><span class="sxs-lookup"><span data-stu-id="171ee-p103">Office 365 updates anti-spam engine and malware signatures in real-time on a daily basis. However, your users might still get malicious messages delivered to their inboxes for a variety of reasons, including when the content was weaponized at a time after it was first delivered to users. ZAP addresses this by continually monitoring updates to the Office 365 spam and malware signatures, and can therefore find and remove previously delivered messages already in inboxes. For mail that was already identified as spam, ZAP moves unread messages to the user's Junk mail folder. For newly detected malware, ZAP removes the attachments from the email message, regardless of whether the mail was read or not. The reverse is true for messages that were incorrectly classified as malicious.</span></span>
  
<span data-ttu-id="171ee-115">사서함 사용자, 자신이 통보 되지 않습니다 메일 옮긴 ZAP 함수는 원활 하 게 수행 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="171ee-115">The ZAP action is seamless for the mailbox user, he or she is not notified the mail has been moved.</span></span>
  
<span data-ttu-id="171ee-116">목록, [메일 흐름 규칙](https://go.microsoft.com/fwlink/p/?LinkId=722755)및 최종 사용자 규칙을 허용 또는 추가 필터를 ZAP 보다 우선 합니다.</span><span class="sxs-lookup"><span data-stu-id="171ee-116">Allow lists, [mail flow rules](https://go.microsoft.com/fwlink/p/?LinkId=722755), and end user rules or additional filters take precedence over ZAP.</span></span>
  
 <span data-ttu-id="171ee-117">**이 문서의 내용**</span><span class="sxs-lookup"><span data-stu-id="171ee-117">**In this article:**</span></span>
  
> [<span data-ttu-id="171ee-118">스팸 필터 정책 설정</span><span class="sxs-lookup"><span data-stu-id="171ee-118">Set spam filter policy</span></span>](zero-hour-auto-purge.md#BK_SetSpam)
    
> [<span data-ttu-id="171ee-119">ZAP 메시지를 이동 하는 경우를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="171ee-119">See if ZAP moved your message</span></span>](zero-hour-auto-purge.md#BK_DidZAPMove)
    
> [<span data-ttu-id="171ee-120">ZAP를 사용 하지 않도록 설정</span><span class="sxs-lookup"><span data-stu-id="171ee-120">Disable ZAP</span></span>](zero-hour-auto-purge.md#BK_Posh)
    
> [<span data-ttu-id="171ee-121">FAQ</span><span class="sxs-lookup"><span data-stu-id="171ee-121">FAQ</span></span>](zero-hour-auto-purge.md#BK_FAQ)
    
## <a name="working-with-zap"></a><span data-ttu-id="171ee-122">ZAP (영문)</span><span class="sxs-lookup"><span data-stu-id="171ee-122">Working with ZAP</span></span>

<span data-ttu-id="171ee-123">기본적으로 ZAP 켜져 있지만 조건 관련 된 몇가지를 충족 하는지 확인 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="171ee-123">ZAP is turned on by default, but you do have to make sure a couple of conditions are met:</span></span>
  
- <span data-ttu-id="171ee-124">스팸 필터 정책은 [정크 메일 폴더로 메시지 이동](zero-hour-auto-purge.md#BK_SetSpam)으로 설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="171ee-124">Spam filter policy is set to [Move message to Junk Email folder](zero-hour-auto-purge.md#BK_SetSpam).</span></span>
    
    <span data-ttu-id="171ee-125">모든 사서함 ZAP으로 검사 하지 않으려면 사용자 집합에만 적용 되는 스팸 필터 정책을 새로 만들 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="171ee-125">You can also create a new spam filter policy that applies only to a set of users if you don't want all mailboxes to be screened by ZAP.</span></span>
    
- <span data-ttu-id="171ee-126">사용자의 [옵션 \> 정크 메일](https://support.office.com/article/068FA430-F8D7-4518-A8DA-8BC74958F05F)합니다.</span><span class="sxs-lookup"><span data-stu-id="171ee-126">The user's [Options \> Junk Email](https://support.office.com/article/068FA430-F8D7-4518-A8DA-8BC74958F05F).</span></span>
    
<span data-ttu-id="171ee-127">[ZAP 메시지를 이동 하는 경우 확인](zero-hour-auto-purge.md#BK_DidZAPMove)하려는 경우에 Exchange Online 메시지 추적 도구를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="171ee-127">If you want [to see if ZAP moved your message](zero-hour-auto-purge.md#BK_DidZAPMove), you can use the Exchange Online message trace tool.</span></span>
  
<span data-ttu-id="171ee-128">관리자가 수도 [ZAP를 사용 하지 않도록 설정](zero-hour-auto-purge.md#BK_Posh) PowerShell을 사용 하 여.</span><span class="sxs-lookup"><span data-stu-id="171ee-128">Admins can also [disable ZAP](zero-hour-auto-purge.md#BK_Posh) by using PowerShell.</span></span> 
  
 <span data-ttu-id="171ee-129">**스팸 필터 정책을 설정 하려면**</span><span class="sxs-lookup"><span data-stu-id="171ee-129">**To set spam filter policy**</span></span>
  
1. <span data-ttu-id="171ee-130">[비즈니스를 위한 Office 365에 로그인 할 위치](https://support.office.com/article/e9eb7d51-5430-4929-91ab-6157c5a050b4) 에 로그인 하 고 **보호** 선택 \> **스팸 필터**입니다.</span><span class="sxs-lookup"><span data-stu-id="171ee-130">Sign in to the [Where to sign in to Office 365 for business](https://support.office.com/article/e9eb7d51-5430-4929-91ab-6157c5a050b4) and choose **protection** \> **spam filter**.</span></span> 
    
    ![EAC에서 보호를 선택 하 고 필터를 스팸](media/0463c879-63fa-4a6c-9b03-e980d5ef3954.PNG)
  
2. <span data-ttu-id="171ee-132">조정 하려는 필터 정책을 선택 하거나 **추가**선택![추가 아이콘](media/8ee52980-254b-440b-99a2-18d068de62d3.gif) 새 수신기를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="171ee-132">Either choose the filter policy you want to adjust, or choose **add**![Add icon](media/8ee52980-254b-440b-99a2-18d068de62d3.gif) to create a new one.</span></span> 
    
    <span data-ttu-id="171ee-p104">이전 스크린샷에서 정책 이름이 "기본" 있지만 추가 스팸 필터 정책을 만들 경우 있습니다 수에 다른 이름을 지정 합니다. 또한 제한 된 집합의 사용자에 정책을 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="171ee-p104">In the previous screen shot, the policy is named "Default", but if you create additional spam filter policies you can give them a different name. You can also apply the policy to only a limited set of users.</span></span>
    
3. <span data-ttu-id="171ee-135">정책 창에서 **스팸 및 대량 작업**선택 하 고 **스팸** 이 **정크 메일 폴더로 메시지 이동으로**설정 되었는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="171ee-135">In the policy window, choose **spam and bulk actions**, and make sure that **Spam** is set to **Move message to Junk Email folder**.</span></span> 
    
    <span data-ttu-id="171ee-136">이 시점에서 **저장** 을 선택 하는 경우 Office 365 테 넌 트에 정책을 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="171ee-136">If you choose **Save** at this point, the policy applies to your Office 365 tenant.</span></span> 
    
    ![정크 메일 폴더로 메시지 이동 하기 위한 설정 스팸 및 대량 작업](media/4332cfb3-89e1-48ba-8da8-9286f2fa1089.PNG)
  
4. <span data-ttu-id="171ee-p105">**받는 사람**, **도메인**또는 **그룹 구성원 자격** 메뉴 컨트롤 및 정책 필터 창에서 **적용** 섹션으로 스크롤한 선택 새 정책을 만든 경우 사용자의 하위 집합만에 정책을 적용 하려는 경우 정책에 적용 하려고 합니다. 추가 조건 및 예외를 설정할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="171ee-p105">If you created a new policy, and you want to apply the policy to only a set of users, scroll to the **Applied To** section in the policy filter window, and in the menu controls choose the **recipients**, **domain**, or **group memberships** you want to apply the policy to. You can also set additional conditions and exceptions.</span></span> 
    
    ![적용 된 주소 섹션에서 받는 사람을 선택](media/19ca10db-c0f4-432c-b3de-ad4101a23de6.PNG)
  
    <span data-ttu-id="171ee-141">선택한 사용자에 게 정책을 적용 하려면 **저장** 을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="171ee-141">Choose **Save** to apply the policy to the selected users.</span></span> 
    
 <span data-ttu-id="171ee-142">**ZAP 메시지를 이동 하는 경우를 확인 하려면**</span><span class="sxs-lookup"><span data-stu-id="171ee-142">**To see if ZAP moved your message**</span></span>
  
- <span data-ttu-id="171ee-143">메시지 ZAP 여 이동 된 경우 확인 하는 [찾기 및 비즈니스 관리자에 대 한 Office 365의 전자 메일 배달 문제를 해결](https://support.office.com/article/e7758b99-1896-41db-bf39-51e2dba21de6) 을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="171ee-143">You can use the [Find and fix email delivery issues as an Office 365 for business admin](https://support.office.com/article/e7758b99-1896-41db-bf39-51e2dba21de6) to determine if the message was moved by ZAP:</span></span> 
    
    <span data-ttu-id="171ee-144">ZAP 여 이동 된 메시지를 식별 하 여 추적 세부 정보에 "0 시간 자동 항목 지우기 (ZAP)" 텍스트를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="171ee-144">Look for the text "Zero-Hour Auto Purge (ZAP)" in your trace details to identify a message that was moved by ZAP.</span></span>
    
 <span data-ttu-id="171ee-145">**ZAP를 사용 하지 않도록 설정 하려면**</span><span class="sxs-lookup"><span data-stu-id="171ee-145">**To disable ZAP**</span></span>
  
- <span data-ttu-id="171ee-146">사용 하지 않도록 설정 하려는 경우 Office 365 테 넌 트에 대 한 ZAP 또는 사용자 집합을 [Set-hostedcontentfilterpolicy](https://go.microsoft.com/fwlink/p/?LinkId=722758), EOP cmdlet의 **ZapEnabled** 매개 변수를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="171ee-146">If you want to disable ZAP for your Office 365 tenant, or a set of users, use the **ZapEnabled** parameter of [Set-HostedContentFilterPolicy](https://go.microsoft.com/fwlink/p/?LinkId=722758), an EOP cmdlet.</span></span>
    
    <span data-ttu-id="171ee-147">다음 예제에서는 ZAP은 "Test" 라는 콘텐츠 필터 정책에 대해 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="171ee-147">In the following example, ZAP is disabled for a content filter policy named "Test".</span></span>
    
||
|:-----|
|
```
  Set-HostedContentFilterPolicy -Identity Test -ZapEnabled $false
```

|
   
## <a name="faq"></a><span data-ttu-id="171ee-148">FAQ</span><span class="sxs-lookup"><span data-stu-id="171ee-148">FAQ</span></span>
<span data-ttu-id="171ee-149"><a name="BK_FAQ"> </a></span><span class="sxs-lookup"><span data-stu-id="171ee-149"></span></span>

 <span data-ttu-id="171ee-150">**합법적인 메시지는 정크 메일 폴더로 이동 하는 경우 어떻게 됩니까?**</span><span class="sxs-lookup"><span data-stu-id="171ee-150">**What happens if a legitimate message is moved to the junk mail folder?**</span></span>
  
<span data-ttu-id="171ee-p106">False 양수에 대 한 일반 보고 프로세스를 따라야 합니다. 정크 메일 폴더로 메시지를 받은 편지함에서 이동할 수는 유일한 이유는 서비스에서 메시지 스팸 했음을 확인가 때문에 것 또는 악의적 합니다.</span><span class="sxs-lookup"><span data-stu-id="171ee-p106">You should follow the normal reporting process for false-positives. The only reason the message would be moved from the inbox to the junk mail folder would be because the service has determined that the message was spam or malicious.</span></span>
  
 <span data-ttu-id="171ee-153">**경우에 어떻게 정크 메일 폴더 대신 Office 365 격리를 사용 합니까?**</span><span class="sxs-lookup"><span data-stu-id="171ee-153">**What if I use the Office 365 quarantine instead of the junk mail folder?**</span></span>
  
<span data-ttu-id="171ee-154">ZAP 지금은 메시지를 격리에 받은 편지함에서 이동 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="171ee-154">ZAP doesn't move messages into quarantine from the Inbox at this time.</span></span>
  
 <span data-ttu-id="171ee-155">**사용자 지정 메일 흐름 규칙을 경우에 어떻게 해야 합니까 (차단 / 허용 규칙)?**</span><span class="sxs-lookup"><span data-stu-id="171ee-155">**What If I have a custom mail flow rule (Block/ Allow Rule)?**</span></span>
  
<span data-ttu-id="171ee-p107">관리자 (메일 흐름 규칙) 또는 허용 및 차단 규칙에서 만든 규칙이 우선 합니다. 이러한 메시지 기능 조건에서 제외 됩니다.</span><span class="sxs-lookup"><span data-stu-id="171ee-p107">Rules created by admins (mail flow rules) or Block and Allow rules take precedence. Such messages are excluded from the feature criteria.</span></span>
  
## <a name="related-topics"></a><span data-ttu-id="171ee-158">관련 항목</span><span class="sxs-lookup"><span data-stu-id="171ee-158">Related Topics</span></span>
<span data-ttu-id="171ee-159"><a name="BK_FAQ"> </a></span><span class="sxs-lookup"><span data-stu-id="171ee-159"></span></span>

[<span data-ttu-id="171ee-160">Office 365 전자 메일 스팸 방지 보호</span><span class="sxs-lookup"><span data-stu-id="171ee-160">Office 365 Email Anti-Spam Protection</span></span>](anti-spam-protection.md)
  
[<span data-ttu-id="171ee-161">Office 365 스팸 필터로 전자 메일 스팸을 차단하여 거짓 부정 문제 방지</span><span class="sxs-lookup"><span data-stu-id="171ee-161">Block email spam with the Office 365 spam filter to prevent false negative issues</span></span>](block-email-spam-to-prevent-false-negatives.md)
  

