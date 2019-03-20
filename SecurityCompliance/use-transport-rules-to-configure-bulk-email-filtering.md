---
title: 메일 흐름 규칙을 사용 하 여 Exchange Online Protection에서 대량 전자 메일 필터링 구성
ms.author: tracyp
author: MSFTTracyP
manager: laurawi
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 2889c82e-fab0-4e85-87b0-b001b2ccd4f7
ms.collection:
- M365-security-compliance
description: 관리자는 대량 전자 메일 필터링에 대해 Exchange Online Protection의 메일 흐름 규칙을 사용 하는 방법에 대해 알아봅니다.
ms.openlocfilehash: 43f0af6fe41bc7f8f4a62d0d87dbd825fb868f7b
ms.sourcegitcommit: 0f93b37c39d807dec91f118aa671a3430c47a9ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/20/2019
ms.locfileid: "30693287"
---
# <a name="use-mail-flow-rules-to-configure-bulk-email-filtering-in-exchange-online-protection"></a><span data-ttu-id="2abcd-103">메일 흐름 규칙을 사용 하 여 Exchange Online Protection에서 대량 전자 메일 필터링 구성</span><span class="sxs-lookup"><span data-stu-id="2abcd-103">Use mail flow rules to configure bulk email filtering in Exchange Online Protection</span></span>

<span data-ttu-id="2abcd-104">기본 스팸 콘텐츠 필터 정책을 사용 하 여 스팸 및 대량 전자 메일에 대 한 회사 전체의 콘텐츠 필터를 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2abcd-104">You can set company-wide content filters for spam and bulk email using the default spam content-filter policies.</span></span> <span data-ttu-id="2abcd-105">이 문서에서는 [스팸 필터 정책 구성](configure-your-spam-filter-policies.md) 및 [get-hostedcontentfilterpolicy](https://docs.microsoft.com/powershell/module/exchange/antispam-antimalware/Set-HostedContentFilterPolicy?view=exchange-ps) 에서 콘텐츠 필터 정책을 설정 하는 방법에 대 한 설정을 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="2abcd-105">Check out [Configure your spam filter policies](configure-your-spam-filter-policies.md) and [Set-HostedContentFilterPolicy](https://docs.microsoft.com/powershell/module/exchange/antispam-antimalware/Set-HostedContentFilterPolicy?view=exchange-ps) on how to set the content filter policies.</span></span> 
  
<span data-ttu-id="2abcd-106">대량 메시지를 필터링 하는 더 많은 옵션을 원하는 경우 메일 흐름 규칙 (전송 규칙이 라고도 함)을 만들어 대량 전자 메일에서 자주 발견 되는 텍스트 패턴이 나 구를 검색할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2abcd-106">If you want to more options to filter bulk messages, you can create mail flow rules (also known as transport rules) to search for text patterns or phrases frequently found in bulk emails.</span></span> <span data-ttu-id="2abcd-107">이러한 특성을 포함 하는 모든 메시지는 스팸으로 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="2abcd-107">Any message containing these characteristics will be marked as spam.</span></span> <span data-ttu-id="2abcd-108">이러한 규칙을 사용하면 조직에 수신되는 원치 않는 대량 전자 메일을 줄일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2abcd-108">Using these rules can help reduce the amount of unwanted bulk email your organization receives.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2abcd-109">이 항목에서 설명 하는 메일 흐름 규칙을 만들기 전에 먼저 [정크 메일과 대량 전자 메일의 차이점](what-s-the-difference-between-junk-email-and-bulk-email.md) 을 읽고, [대량 불만 수준 값](bulk-complaint-level-values.md)을 확인 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="2abcd-109">Before creating the mail flow rules documented this topic, we recommend that you first read [What's the difference between junk email and bulk email?](what-s-the-difference-between-junk-email-and-bulk-email.md) and [Bulk Complaint Level values](bulk-complaint-level-values.md).</span></span><br> <span data-ttu-id="2abcd-110">다음 절차에서는 메시지를 전체 조직에 대한 스팸으로 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="2abcd-110">The following procedures mark a message as spam for your entire organization.</span></span> <span data-ttu-id="2abcd-111">그러나 다른 조건을 추가하여 조직의 특정 받는 사람에게만 이러한 규칙을 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2abcd-111">However, you can add another condition to apply these rules only to specific recipients in your organization.</span></span> <span data-ttu-id="2abcd-112">이러한 방식으로 대상이 높은 대규모 전자 메일 필터링 설정은 소수의 사용자에 게 적용할 수 있지만, 사용자의 나머지 (대부분의 경우 대량 전자 메일을 가장 많이 받는 사람)에는 영향을 주지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2abcd-112">This way, the aggressive bulk email filtering settings can apply to a few users who are highly targeted, while the rest of your users (who mostly get the bulk email they signed up for) aren't impacted.</span></span> 
  
## <a name="create-a-mail-flow-rule-to-filter-bulk-email-messages-based-on-text-patterns"></a><span data-ttu-id="2abcd-113">텍스트 패턴에 따라 대량 전자 메일 메시지를 필터링 하는 메일 흐름 규칙 만들기</span><span class="sxs-lookup"><span data-stu-id="2abcd-113">Create a mail flow rule to filter bulk email messages based on text patterns</span></span>

1. <span data-ttu-id="2abcd-114">**메일 흐름** 으로 이동 하는 Exchange 관리 센터 (EAC)에서 \> **규칙** 입니다.</span><span class="sxs-lookup"><span data-stu-id="2abcd-114">In the Exchange admin center (EAC), go to **Mail flow** \> **Rules**.</span></span>
    
2. <span data-ttu-id="2abcd-115">추가 아이콘](media/ITPro-EAC-AddIcon.gif) 추가를 클릭 한 다음 **새 규칙 만들기**를 선택 합니다. \*\*\*\* ![</span><span class="sxs-lookup"><span data-stu-id="2abcd-115">Click **Add** ![Add Icon](media/ITPro-EAC-AddIcon.gif) and then select **Create a new rule**.</span></span>
    
3. <span data-ttu-id="2abcd-116">규칙 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="2abcd-116">Specify a name for the rule.</span></span>
    
4. <span data-ttu-id="2abcd-117">**기타 옵션**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="2abcd-117">Click **More options**.</span></span> <span data-ttu-id="2abcd-118">다음의 **경우이 규칙 적용**에서 **제목 또는 본문** \> **제목 또는 본문이 다음 텍스트 패턴과 일치 하는 항목**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="2abcd-118">Under **Apply this rule if**, select **The subject or body** \> **subject or body matches these text patterns**.</span></span>
    
5. <span data-ttu-id="2abcd-119">**단어 또는 구 지정** 대화 상자에 대량 전자 메일에서 일반적으로 발견되는 다음 정규식을 한 번에 하나씩 추가하고 작업을 마치면 **확인**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="2abcd-119">In the **specify words or phrases** dialog box, add the following regular expressions commonly found in bulk emails, one at a time, and click **ok** when you're done:</span></span> 
    
   - `If you are unable to view the content of this email\, please`
    
   - `\>(safe )?unsubscribe( here)?\</a\>`
    
   - `If you do not wish to receive further communications like this\, please`
    
   - `\<img height\="?1"? width\="?1"? sr\c=.?http\://`
    
   - `To stop receiving these+emails\:http\://`
    
   - `To unsubscribe from \w+ (e\-?letter|e?-?mail|newsletter)`
    
   - `no longer (wish )?(to )?(be sent|receive) w+ email`
    
   - `If you are unable to view the content of this email\, please click here`
    
   - `To ensure you receive (your daily deals|our e-?mails)\, add`
    
   - `If you no longer wish to receive these emails`
    
   - `to change your (subscription preferences|preferences or unsubscribe)`
    
   - `click (here to|the) unsubscribe`
    
   <span data-ttu-id="2abcd-120">위의 목록은 대량 전자 메일에서 발견 되는 일반 정규식 집합입니다. 필요에 따라 추가 하거나 제거할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2abcd-120">The above list isn't an exhaustive set of regular expressions found in bulk emails; more can be added or removed as needed.</span></span> <span data-ttu-id="2abcd-121">그러나 이 목록에서 시작하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="2abcd-121">However, it's a good starting point.</span></span><br><span data-ttu-id="2abcd-122">ASCII 텍스트의 SMTP 서버 간에 이진 메시지를 전송 하는 데 사용 된 MIME 콘텐츠 전송 인코딩 방법 으로부터 메시지를 디코딩 *한 후* 메시지의 제목 또는 기타 헤더 필드에 대 한 단어 또는 텍스트 패턴 검색을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="2abcd-122">The search for words or text patterns in the subject or other header fields in the message occurs  *after*  the message has been decoded from the MIME content transfer encoding method that was used to transmit the binary message between SMTP servers in ASCII text.</span></span> <span data-ttu-id="2abcd-123">조건이나 예외를 사용하여 메시지의 제목이나 다른 머리글 필드에 있는 원시(일반적으로, Base64) 인코딩된 값을 검색할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="2abcd-123">You can't use conditions or exceptions to search for the raw (typically, Base64) encoded values of the subject or other header fields in messages.</span></span> 
    
6. <span data-ttu-id="2abcd-124">**다음 작업 실행**에서 **메시지 속성 수정** \> **SCL(스팸 지수) 설정**을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="2abcd-124">Under **Do the following**, select **Modify the message properties** \> **set the spam confidence level (SCL)**.</span></span>
    
7. <span data-ttu-id="2abcd-125">**SCL 지정** 대화 상자에서 SCL을 **5**, **6** 또는 **9**로 설정하고 **확인**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="2abcd-125">In the **specify SCL** dialog box, set the SCL to **5**, **6**, or **9**, and click **ok**.</span></span>
    
   <span data-ttu-id="2abcd-126">SCL을 5 또는 6으로 설정하면 **스팸** 동작이 수행되지만 SCL을 9로 설정하면 콘텐츠 필터 정책에 구성된 대로 **높은 정확도 스팸** 작업이 수행됩니다.</span><span class="sxs-lookup"><span data-stu-id="2abcd-126">Setting the SCL to 5 or 6 takes the **Spam** action, while setting the SCL to 9 takes the **High confidence spam** action, as configured in the content filter policy.</span></span> <span data-ttu-id="2abcd-127">서비스는 콘텐츠 필터 정책에 설정된 작업을 수행합니다.</span><span class="sxs-lookup"><span data-stu-id="2abcd-127">The service will perform the action set in the content filter policy.</span></span> <span data-ttu-id="2abcd-128">기본 작업은 받는 사람의 정크 메일 폴더로 메시지를 배달 하는 것 이지만, [스팸 필터 정책 구성](configure-your-spam-filter-policies.md)에 설명 된 대로 다른 작업을 구성할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2abcd-128">The default action is to deliver the message to the recipients' Junk Email folder, but different actions can be configured as described in [Configure your spam filter policies](configure-your-spam-filter-policies.md).</span></span>
    
   <span data-ttu-id="2abcd-129">메시지를 받는 사람의 정크 메일 폴더로 보내지 않고 격리 하는 작업을 수행 하는 경우 메시지는 메일 흐름 규칙 일치로 관리자 격리로 보내지며 최종 사용자 스팸 격리 또는 최종 사용자에 게는 제공 되지 않습니다. 스팸 알림</span><span class="sxs-lookup"><span data-stu-id="2abcd-129">If your configured action is to quarantine the message rather than send it to the recipients' Junk Email folder, the message will be sent to the administrator quarantine as a mail flow rule match, and it will not be available in the end user spam quarantine or via end-user spam notifications.</span></span> 
  
   <span data-ttu-id="2abcd-130">서비스의 SCL 값에 대한 자세한 내용은 [스팸 신뢰 수준](spam-confidence-levels.md)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="2abcd-130">For more information about SCL values in the service, see [Spam confidence levels](spam-confidence-levels.md).</span></span>
    
8. <span data-ttu-id="2abcd-131">규칙을 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="2abcd-131">Save the rule.</span></span>
    
## <a name="create-a-mail-flow-rule-to-filter-bulk-email-messages-based-on-phrases"></a><span data-ttu-id="2abcd-132">구에 따라 대량 전자 메일 메시지를 필터링 하는 메일 흐름 규칙 만들기</span><span class="sxs-lookup"><span data-stu-id="2abcd-132">Create a mail flow rule to filter bulk email messages based on phrases</span></span>

1. <span data-ttu-id="2abcd-133">EAC에서 **메일 흐름** \> **규칙**으로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="2abcd-133">In the EAC, go to **Mail flow** \> **Rules**.</span></span>
    
2. <span data-ttu-id="2abcd-134">추가 아이콘](media/ITPro-EAC-AddIcon.gif) 추가를 클릭 한 다음 **새 규칙 만들기**를 선택 합니다. \*\*\*\* ![</span><span class="sxs-lookup"><span data-stu-id="2abcd-134">Click **Add** ![Add Icon](media/ITPro-EAC-AddIcon.gif) and then select **Create a new rule**.</span></span>
    
3. <span data-ttu-id="2abcd-135">규칙 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="2abcd-135">Specify a name for the rule.</span></span>
    
4. <span data-ttu-id="2abcd-136">**기타 옵션**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="2abcd-136">Click **More options**.</span></span> <span data-ttu-id="2abcd-137">다음의 **경우이 규칙 적용**에서 **제목 또는 본문** \> 에 **다음 단어 포함 또는 본문**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="2abcd-137">Under **Apply this rule if**, select **The subject or body** \> **subject or body includes any of these words**.</span></span>
    
5. <span data-ttu-id="2abcd-138">**단어 또는 구 지정** 대화 상자에 대량 전자 메일에서 일반적으로 발견되는 다음 구를 한 번에 하나씩 추가하고 작업을 마치면 **확인**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="2abcd-138">In the **specify words or phrases** dialog box, add the following phrases commonly found in bulk emails, one at a time, and click **ok** when you're done:</span></span> 
    
   - `to change your preferences or unsubscribe`
    
   - `Modify email preferences or unsubscribe`
    
   - `This is a promotional email`
    
   - `You are receiving this email because you requested a subscription`
    
   - `click here to unsubscribe`
    
   - `You have received this email because you are subscribed`
    
   - `If you no longer wish to receive our email newsletter`
    
   - `to unsubscribe from this newsletter`
    
   - `If you have trouble viewing this email`
    
   - `This is an advertisement`
    
   - `you would like to unsubscribe or change your`
    
   - `view this email as a webpage`
    
   - `You are receiving this email because you are subscribed`
    
   <span data-ttu-id="2abcd-139">이 목록은 대량 전자 메일에서 발견 되는 포괄적인 구 집합이 아닙니다. 필요에 따라 추가 하거나 제거할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2abcd-139">This list isn't an exhaustive set of phrases found in bulk emails; more can be added or removed as needed.</span></span> <span data-ttu-id="2abcd-140">그러나 이 목록에서 시작하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="2abcd-140">However, it's a good starting point.</span></span>
    
6. <span data-ttu-id="2abcd-141">**다음 작업 실행**에서 **메시지 속성 수정** \> **SCL(스팸 지수) 설정**을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="2abcd-141">Under **Do the following**, select **Modify the message properties** \> **set the spam confidence level (SCL)**.</span></span>
    
7. <span data-ttu-id="2abcd-142">**SCL 지정** 대화 상자에서 SCL을 **5**, **6** 또는 **9**로 설정하고 **확인**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="2abcd-142">In the **specify SCL** dialog box, set the SCL to **5**, **6**, or **9**, and click **ok**.</span></span>
    
   <span data-ttu-id="2abcd-143">SCL을 5 또는 6으로 설정하면 **스팸** 동작이 수행되지만 SCL을 9로 설정하면 콘텐츠 필터 정책에 구성된 대로 **높은 정확도 스팸** 작업이 수행됩니다.</span><span class="sxs-lookup"><span data-stu-id="2abcd-143">Setting the SCL to 5 or 6 takes the **Spam** action, while setting the SCL to 9 takes the **High confidence spam** action, as configured in the content filter policy.</span></span> <span data-ttu-id="2abcd-144">서비스는 콘텐츠 필터 정책에 설정된 작업을 수행합니다.</span><span class="sxs-lookup"><span data-stu-id="2abcd-144">The service will perform the action set in the content filter policy.</span></span> <span data-ttu-id="2abcd-145">기본 작업은 받는 사람의 정크 메일 폴더로 메시지를 배달 하는 것 이지만, [스팸 필터 정책 구성](configure-your-spam-filter-policies.md)에 설명 된 대로 다른 작업을 구성할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2abcd-145">The default action is to deliver the message to the recipients' Junk Email folder, but different actions can be configured as described in [Configure your spam filter policies](configure-your-spam-filter-policies.md).</span></span>
    
   <span data-ttu-id="2abcd-146">메시지를 받는 사람의 정크 메일 폴더로 보내지 않고 격리 하는 작업을 수행 하는 경우 메시지는 메일 흐름 규칙 일치로 관리자 격리로 보내지며 최종 사용자 스팸 격리 또는 최종 사용자에 게는 제공 되지 않습니다. 스팸 알림</span><span class="sxs-lookup"><span data-stu-id="2abcd-146">If your configured action is to quarantine the message rather than send it to the recipients' Junk Email folder, the message will be sent to the administrator quarantine as a mail flow rule match, and it will not be available in the end user spam quarantine or via end-user spam notifications.</span></span> 
  
   <span data-ttu-id="2abcd-147">서비스의 SCL 값에 대한 자세한 내용은 [스팸 신뢰 수준](spam-confidence-levels.md)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="2abcd-147">For more information about SCL values in the service, see [Spam confidence levels](spam-confidence-levels.md).</span></span>

8. <span data-ttu-id="2abcd-148">규칙을 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="2abcd-148">Save the rule.</span></span>

## <a name="for-more-information"></a><span data-ttu-id="2abcd-149">자세한 내용</span><span class="sxs-lookup"><span data-stu-id="2abcd-149">For more information</span></span>

[<span data-ttu-id="2abcd-150">정크 메일과 대량 전자 메일의 차이점</span><span class="sxs-lookup"><span data-stu-id="2abcd-150">What's the difference between junk email and bulk email?</span></span>](what-s-the-difference-between-junk-email-and-bulk-email.md)

[<span data-ttu-id="2abcd-151">대량 불만 수준 값</span><span class="sxs-lookup"><span data-stu-id="2abcd-151">Bulk Complaint Level values</span></span>](bulk-complaint-level-values.md)

[<span data-ttu-id="2abcd-152">스팸 필터 정책 구성</span><span class="sxs-lookup"><span data-stu-id="2abcd-152">Configure your spam filter policies</span></span>](configure-your-spam-filter-policies.md)

[<span data-ttu-id="2abcd-153">고급 스팸 필터링 옵션</span><span class="sxs-lookup"><span data-stu-id="2abcd-153">Advanced spam filtering  options</span></span>](advanced-spam-filtering-asf-options.md)
