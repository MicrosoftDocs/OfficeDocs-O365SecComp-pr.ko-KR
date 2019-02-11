---
title: 메일 흐름 규칙을 사용 하 여 Exchange Online Protection에서 필터링 하는 대량 전자 메일을 구성 하려면
ms.author: krowley
author: kccross
manager: laurawi
ms.date: ''
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 2889c82e-fab0-4e85-87b0-b001b2ccd4f7
description: 관리자가 대량 전자 메일을 필터링 하기 위한 Exchange Online Protection에서 메일 흐름 규칙을 사용 하는 방법을 알아보십시오.
ms.openlocfilehash: ce95872d3d80436dce4c62037caea9a5f735726d
ms.sourcegitcommit: 7e2a0185cadea7f3a6afc5ddc445eac2e1ce22eb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/11/2019
ms.locfileid: "27382809"
---
# <a name="use-mail-flow-rules-to-configure-bulk-email-filtering-in-exchange-online-protection"></a><span data-ttu-id="7d29f-103">메일 흐름 규칙을 사용 하 여 Exchange Online Protection에서 필터링 하는 대량 전자 메일을 구성 하려면</span><span class="sxs-lookup"><span data-stu-id="7d29f-103">Use mail flow rules to configure bulk email filtering in Exchange Online Protection</span></span>

<span data-ttu-id="7d29f-p101">기본 스팸 콘텐츠 필터 정책을 사용 하 여 스팸 및 대량 전자 메일에 대 한 회사 전체의 콘텐츠 필터를 설정할 수 있습니다. 콘텐츠 필터 정책을 설정 하는 방법에 [스팸 필터 정책 구성](configure-your-spam-filter-policies.md) 및 [Set-hostedcontentfilterpolicy](http://technet.microsoft.com/library/f597aa65-baa7-49d0-8832-2a300073f211.aspx) 체크아웃 합니다.</span><span class="sxs-lookup"><span data-stu-id="7d29f-p101">You can set company-wide content filters for spam and bulk email using the default spam content-filter policies. Check out [Configure your spam filter policies](configure-your-spam-filter-policies.md) and [Set-HostedContentFilterPolicy](http://technet.microsoft.com/library/f597aa65-baa7-49d0-8832-2a300073f211.aspx) on how to set the content filter policies.</span></span> 
  
<span data-ttu-id="7d29f-p102">대량으로 메시지를 필터링 하려면 기타 옵션을 하려는 경우에 텍스트 패턴이 나 대량 전자 메일에서 자주 발생 하는 구를 검색 하는 메일 흐름 규칙 (전송 규칙이 라고도 함)을 만들 수 있습니다. 이러한 특성을 포함 하는 모든 메시지는 스팸으로 표시 됩니다. 이러한 규칙을 사용 하 여 조직에서 받을 원치 않는 대량 전자 메일의 양을 줄일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7d29f-p102">If you want to more options to filter bulk messages, you can create mail flow rules (also known as transport rules) to search for text patterns or phrases frequently found in bulk emails. Any message containing these characteristics will be marked as spam. Using these rules can help reduce the amount of unwanted bulk email your organization receives.</span></span>
  
<span data-ttu-id="7d29f-109">**참고:**</span><span class="sxs-lookup"><span data-stu-id="7d29f-109">**Notes**:</span></span>

- <span data-ttu-id="7d29f-110">이 항목을 문서화 만들기 (영문)의 메일 흐름 규칙, 전에 먼저 읽어보는 것이 좋습니다 [정크 메일과 대량 전자 메일의 차이점은 무엇입니까?](what-s-the-difference-between-junk-email-and-bulk-email.md) 및 [대량 불만 수준 값](bulk-complaint-level-values.md)입니다.</span><span class="sxs-lookup"><span data-stu-id="7d29f-110">Before creating the mail flow rules documented this topic, we recommend that you first read [What's the difference between junk email and bulk email?](what-s-the-difference-between-junk-email-and-bulk-email.md) and [Bulk Complaint Level values](bulk-complaint-level-values.md).</span></span> 
  
- <span data-ttu-id="7d29f-p103">다음 절차 전체 조직에 대 한 스팸 메시지를 표시 합니다. 그러나 조직에서 특정 받는 사람에만 이러한 규칙을 적용할 다른 조건을 추가할 수 있습니다. 이와 같은 방식이으로 소수의 사용자에 게 매우를 사용 하 여 대상 지정 필터링 설정을 적용할 수 적극적으로 대량 전자 메일 사용자 (대개 에이전트는 로그인에 대 한 대량 전자 메일을 가져오기 위해)의 나머지 부분 하는 동안 되지 않은 영향을 받습니다.</span><span class="sxs-lookup"><span data-stu-id="7d29f-p103">The following procedures mark a message as spam for your entire organization. However, you can add another condition to apply these rules only to specific recipients in your organization. This way, the aggressive bulk email filtering settings can apply to a few users who are highly targeted, while the rest of your users (who mostly get the bulk email they signed up for) aren't impacted.</span></span> 
  
### <a name="create-mail-flow-rule-to-filter-bulk-email-messages-based-on-text-patterns"></a><span data-ttu-id="7d29f-114">텍스트 패턴을 기반으로 대량 전자 메일 메시지를 필터링 하려면 메일 흐름 규칙 만들기</span><span class="sxs-lookup"><span data-stu-id="7d29f-114">Create mail flow rule to filter bulk email messages based on text patterns</span></span>

1. <span data-ttu-id="7d29f-115">EAC(Exchange 관리 센터)에서 **메일 흐름** \> **규칙**으로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="7d29f-115">In the Exchange admin center (EAC), go to **Mail flow** \> **Rules**.</span></span>
    
2. <span data-ttu-id="7d29f-116">**추가**![아이콘 추가](media/ITPro-EAC-AddIcon.gif)를 클릭한 다음 **새 규칙 만들기**를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="7d29f-116">Click **Add**![Add Icon](media/ITPro-EAC-AddIcon.gif) and then select **Create a new rule**.</span></span>
    
3. <span data-ttu-id="7d29f-117">규칙 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7d29f-117">Specify a name for the rule.</span></span>
    
4. <span data-ttu-id="7d29f-p104">**기타 옵션**을 클릭 합니다. **하는 경우이 규칙 적용**에서 **제목이 나 본문** 선택 \> **제목이 나 본문에 다음 텍스트 패턴과 일치**합니다.</span><span class="sxs-lookup"><span data-stu-id="7d29f-p104">Click **More options**. Under **Apply this rule if**, select **The subject or body** \> **subject or body matches these text patterns**.</span></span>
    
5. <span data-ttu-id="7d29f-120">**단어 또는 구 지정** 대화 상자에 대량 전자 메일에서 일반적으로 발견되는 다음 정규식을 한 번에 하나씩 추가하고 작업을 마치면 **확인**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="7d29f-120">In the **specify words or phrases** dialog box, add the following regular expressions commonly found in bulk emails, one at a time, and click **ok** when you're done:</span></span> 
    
   - <span data-ttu-id="7d29f-121">이 전자 메일의 내용을 볼 수 없는 경우\,</span><span class="sxs-lookup"><span data-stu-id="7d29f-121">If you are unable to view the content of this email\, please</span></span>
    
   - <span data-ttu-id="7d29f-122">\\>(safe )?구독 취소( here)?\\</a\\></span><span class="sxs-lookup"><span data-stu-id="7d29f-122">\\>(safe )?unsubscribe( here)?\\</a\\></span></span>
    
   - <span data-ttu-id="7d29f-123">이러한 메일을 더 이상 받지 않으려면\,</span><span class="sxs-lookup"><span data-stu-id="7d29f-123">If you do not wish to receive further communications like this\, please</span></span>
    
   - <span data-ttu-id="7d29f-p105">\\<img height\="?1"? width\="?1"? src\=.?http\://</span><span class="sxs-lookup"><span data-stu-id="7d29f-p105">\\<img height\="?1"? width\="?1"? src\=.?http\://</span></span>
    
   - <span data-ttu-id="7d29f-127">이러한 \s+전자 메일의 수신을 중지하려면\:http\://</span><span class="sxs-lookup"><span data-stu-id="7d29f-127">To stop receiving these\s+emails\:http\://</span></span>
    
   - <span data-ttu-id="7d29f-128">구독을 취소하려면 \w+ (e\-?letter|e?-?mail|newsletter)</span><span class="sxs-lookup"><span data-stu-id="7d29f-128">To unsubscribe from \w+ (e\-?letter|e?-?mail|newsletter)</span></span>
    
   - <span data-ttu-id="7d29f-129">더 이상 (wish )?(to )?(be sent|receive) \w+ email</span><span class="sxs-lookup"><span data-stu-id="7d29f-129">no longer (wish )?(to )?(be sent|receive) \w+ email</span></span>
    
   - <span data-ttu-id="7d29f-130">이 전자 메일의 내용을 볼 수 없는 경우\, 여기를 클릭하십시오</span><span class="sxs-lookup"><span data-stu-id="7d29f-130">If you are unable to view the content of this email\, please click here</span></span>
    
   - <span data-ttu-id="7d29f-131">(your daily deals|our e-?mails)의 수신을 확인하려면\,</span><span class="sxs-lookup"><span data-stu-id="7d29f-131">To ensure you receive (your daily deals|our e-?mails)\, add</span></span>
    
   - <span data-ttu-id="7d29f-132">이러한 메일을 더 이상 받지 않으려면</span><span class="sxs-lookup"><span data-stu-id="7d29f-132">If you no longer wish to receive these emails</span></span>
    
   - <span data-ttu-id="7d29f-133">(subscription preferences|preferences or unsubscribe)을(를) 변경하려면</span><span class="sxs-lookup"><span data-stu-id="7d29f-133">to change your (subscription preferences|preferences or unsubscribe)</span></span>
    
   - <span data-ttu-id="7d29f-134">구독을 취소하려면 (here to|the)을(를) 클릭</span><span class="sxs-lookup"><span data-stu-id="7d29f-134">click (here to|the) unsubscribe</span></span>
    
   <span data-ttu-id="7d29f-135">**참고:**</span><span class="sxs-lookup"><span data-stu-id="7d29f-135">**Notes**:</span></span>

   - <span data-ttu-id="7d29f-p106">위 목록에는 대량 전자 메일;에서 발견 되는 정규식의 광범위 한 집합 되지 않습니다. 더 추가 하거나 제거할 수 필요에 따라 합니다. 그러나 것이 좋은 시작점입니다.</span><span class="sxs-lookup"><span data-stu-id="7d29f-p106">The above list isn't an exhaustive set of regular expressions found in bulk emails; more can be added or removed as needed. However, it's a good starting point.</span></span>
    
   - <span data-ttu-id="7d29f-p107">단어 또는 제목에 텍스트 패턴 또는 메시지에 다른 헤더 필드에 대 한 검색 한 *후* 메시지 인코딩 방법 ASCII 텍스트에서 SMTP 서버 간의 이진 메시지를 전송 하는데 사용 된 MIME 콘텐츠 전송에서 디코딩된 되었는지가 발생 합니다. 원시에 대 한 검색 조건 또는 예외를 사용할 수 없습니다 (일반적으로 Base64) 인코딩된 제목 또는 메시지에 다른 헤더 필드의 값입니다.</span><span class="sxs-lookup"><span data-stu-id="7d29f-p107">The search for words or text patterns in the subject or other header fields in the message occurs  *after*  the message has been decoded from the MIME content transfer encoding method that was used to transmit the binary message between SMTP servers in ASCII text. You can't use conditions or exceptions to search for the raw (typically, Base64) encoded values of the subject or other header fields in messages.</span></span> 
    
6. <span data-ttu-id="7d29f-140">**다음 작업 실행**에서 **메시지 속성 수정** \> **SCL(스팸 지수) 설정**을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="7d29f-140">Under **Do the following**, select **Modify the message properties** \> **set the spam confidence level (SCL)**.</span></span>
    
7. <span data-ttu-id="7d29f-141">**SCL 지정** 대화 상자에서 SCL을 **5**, **6** 또는 **9**로 설정하고 **확인**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="7d29f-141">In the **specify SCL** dialog box, set the SCL to **5**, **6**, or **9**, and click **ok**.</span></span>
    
   <span data-ttu-id="7d29f-p108">SCL를 5 또는 6 인치로 설정 **스팸** 동작을 설정 하는 동안 9 SCL **높은 정확도 스팸** 에서 작업을 수행, 콘텐츠 필터 정책에 구성 된 대로 합니다. 서비스는 콘텐츠 필터 정책에 설정 된 작업을 수행 합니다. 받는 사람의 정크 메일 폴더로 메시지를 제공 하기 위해 기본 작업 이지만 [스팸 필터 정책 구성](configure-your-spam-filter-policies.md)의 설명에 따라 다른 작업을 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7d29f-p108">Setting the SCL to 5 or 6 takes the **Spam** action, while setting the SCL to 9 takes the **High confidence spam** action, as configured in the content filter policy. The service will perform the action set in the content filter policy. The default action is to deliver the message to the recipients' Junk Email folder, but different actions can be configured as described in [Configure your spam filter policies](configure-your-spam-filter-policies.md).</span></span>
    
   > [!NOTE]
   > <span data-ttu-id="7d29f-145">메일 흐름 규칙 일치 하며 대화할 수를 최종 사용자 스팸 격리에서 또는 최종 사용자를 통해으로 메시지가 관리자가 격리로 전송 됩니다를 받는 사람의 정크 메일 폴더로 전송 하는 것이 아니라는 메시지를 격리 하 여 구성 된 작업의 경우 스팸 알림입니다.</span><span class="sxs-lookup"><span data-stu-id="7d29f-145">If your configured action is to quarantine the message rather than send it to the recipients' Junk Email folder, the message will be sent to the administrator quarantine as a mail flow rule match, and it will not be available in the end user spam quarantine or via end-user spam notifications.</span></span> 
  
   <span data-ttu-id="7d29f-146">서비스의 SCL 값에 대한 자세한 내용은 [스팸 신뢰 수준](spam-confidence-levels.md)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="7d29f-146">For more information about SCL values in the service, see [Spam confidence levels](spam-confidence-levels.md).</span></span>
    
8. <span data-ttu-id="7d29f-147">규칙을 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="7d29f-147">Save the rule.</span></span>
    
### <a name="create-a-mail-flow-rule-to-filter-bulk-email-messages-based-on-phrases"></a><span data-ttu-id="7d29f-148">구에 따라 대량 전자 메일 메시지를 필터링 하는 메일 흐름 규칙 만들기</span><span class="sxs-lookup"><span data-stu-id="7d29f-148">Create a mail flow rule to filter bulk email messages based on phrases</span></span>

1. <span data-ttu-id="7d29f-149">EAC에서 **메일 흐름** \> **규칙**으로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="7d29f-149">In the EAC, go to **Mail flow** \> **Rules**.</span></span>
    
2. <span data-ttu-id="7d29f-150">**추가**![아이콘 추가](media/ITPro-EAC-AddIcon.gif)를 클릭한 다음 **새 규칙 만들기**를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="7d29f-150">Click **Add**![Add Icon](media/ITPro-EAC-AddIcon.gif) and then select **Create a new rule**.</span></span>
    
3. <span data-ttu-id="7d29f-151">규칙 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7d29f-151">Specify a name for the rule.</span></span>
    
4. <span data-ttu-id="7d29f-p109">**기타 옵션**을 클릭 합니다. **하는 경우이 규칙 적용**에서 **제목이 나 본문** 선택 \> **제목이 나 본문에 다음이 단어 중 하나라도 포함**합니다.</span><span class="sxs-lookup"><span data-stu-id="7d29f-p109">Click **More options**. Under **Apply this rule if**, select **The subject or body** \> **subject or body includes any of these words**.</span></span>
    
5. <span data-ttu-id="7d29f-154">**단어 또는 구 지정** 대화 상자에 대량 전자 메일에서 일반적으로 발견되는 다음 구를 한 번에 하나씩 추가하고 작업을 마치면 **확인**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="7d29f-154">In the **specify words or phrases** dialog box, add the following phrases commonly found in bulk emails, one at a time, and click **ok** when you're done:</span></span> 
    
   - <span data-ttu-id="7d29f-155">기본 설정을 변경하거나 구독을 취소하려면</span><span class="sxs-lookup"><span data-stu-id="7d29f-155">to change your preferences or unsubscribe</span></span>
    
   - <span data-ttu-id="7d29f-156">전자 메일 기본 설정을 수정하거나 구독을 취소하려면</span><span class="sxs-lookup"><span data-stu-id="7d29f-156">Modify email preferences or unsubscribe</span></span>
    
   - <span data-ttu-id="7d29f-157">이것은 홍보 메일입니다</span><span class="sxs-lookup"><span data-stu-id="7d29f-157">This is a promotional email</span></span>
    
   - <span data-ttu-id="7d29f-158">이것은 구독을 요청한 사용자에게 제공되는 메일입니다</span><span class="sxs-lookup"><span data-stu-id="7d29f-158">You are receiving this email because you requested a subscription</span></span>
    
   - <span data-ttu-id="7d29f-159">구독을 취소하려면 여기를 클릭</span><span class="sxs-lookup"><span data-stu-id="7d29f-159">click here to unsubscribe</span></span>
    
   - <span data-ttu-id="7d29f-160">이 전자 메일은 구독을 요청했기 때문에 제공된 것입니다</span><span class="sxs-lookup"><span data-stu-id="7d29f-160">You have received this email because you are subscribed</span></span>
    
   - <span data-ttu-id="7d29f-161">전자 메일 뉴스레터를 더 이상 받지 않으려면</span><span class="sxs-lookup"><span data-stu-id="7d29f-161">If you no longer wish to receive our email newsletter</span></span>
    
   - <span data-ttu-id="7d29f-162">이 뉴스레터에서 구독을 취소하려면</span><span class="sxs-lookup"><span data-stu-id="7d29f-162">to unsubscribe from this newsletter</span></span>
    
   - <span data-ttu-id="7d29f-163">이 전자 메일을 보는 데 문제가 있는 경우</span><span class="sxs-lookup"><span data-stu-id="7d29f-163">If you have trouble viewing this email</span></span>
    
   - <span data-ttu-id="7d29f-164">이것은 광고 메일입니다</span><span class="sxs-lookup"><span data-stu-id="7d29f-164">This is an advertisement</span></span>
    
   - <span data-ttu-id="7d29f-165">구독을 취소하거나</span><span class="sxs-lookup"><span data-stu-id="7d29f-165">you would like to unsubscribe or change your</span></span>
    
   - <span data-ttu-id="7d29f-166">이 전자 메일을 웹 페이지로 보려면</span><span class="sxs-lookup"><span data-stu-id="7d29f-166">view this email as a webpage</span></span>
    
   - <span data-ttu-id="7d29f-167">구독한 경우에 제공되는 메일입니다</span><span class="sxs-lookup"><span data-stu-id="7d29f-167">You are receiving this email because you are subscribed</span></span>
    
   <span data-ttu-id="7d29f-p110">**참고**: 다시이 목록 되어있지 대량 전자 메일;에서 발견 되는 구의 광범위 한 집합 더 추가 하거나 제거할 수 필요에 따라 합니다. 그러나 것이 좋은 시작점입니다.</span><span class="sxs-lookup"><span data-stu-id="7d29f-p110">**Note**: Once again, this list isn't an exhaustive set of phrases found in bulk emails; more can be added or removed as needed. However, it's a good starting point.</span></span>
    
6. <span data-ttu-id="7d29f-170">**다음 작업 실행**에서 **메시지 속성 수정** \> **SCL(스팸 지수) 설정**을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="7d29f-170">Under **Do the following**, select **Modify the message properties** \> **set the spam confidence level (SCL)**.</span></span>
    
7. <span data-ttu-id="7d29f-171">**SCL 지정** 대화 상자에서 SCL을 **5**, **6** 또는 **9**로 설정하고 **확인**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="7d29f-171">In the **specify SCL** dialog box, set the SCL to **5**, **6**, or **9**, and click **ok**.</span></span>
    
   <span data-ttu-id="7d29f-p111">SCL를 5 또는 6 인치로 설정 **스팸** 동작을 설정 하는 동안 9 SCL **높은 정확도 스팸** 에서 작업을 수행, 콘텐츠 필터 정책에 구성 된 대로 합니다. 서비스는 콘텐츠 필터 정책에 설정 된 작업을 수행 합니다. 받는 사람의 정크 메일 폴더로 메시지를 제공 하기 위해 기본 작업 이지만 [스팸 필터 정책 구성](configure-your-spam-filter-policies.md)의 설명에 따라 다른 작업을 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7d29f-p111">Setting the SCL to 5 or 6 takes the **Spam** action, while setting the SCL to 9 takes the **High confidence spam** action, as configured in the content filter policy. The service will perform the action set in the content filter policy. The default action is to deliver the message to the recipients' Junk Email folder, but different actions can be configured as described in [Configure your spam filter policies](configure-your-spam-filter-policies.md).</span></span>
    
   > [!NOTE]
   > <span data-ttu-id="7d29f-175">메일 흐름 규칙 일치 하며 대화할 수를 최종 사용자 스팸 격리에서 또는 최종 사용자를 통해으로 메시지가 관리자가 격리로 전송 됩니다를 받는 사람의 정크 메일 폴더로 전송 하는 것이 아니라는 메시지를 격리 하 여 구성 된 작업의 경우 스팸 알림입니다.</span><span class="sxs-lookup"><span data-stu-id="7d29f-175">If your configured action is to quarantine the message rather than send it to the recipients' Junk Email folder, the message will be sent to the administrator quarantine as a mail flow rule match, and it will not be available in the end user spam quarantine or via end-user spam notifications.</span></span> 
  
   <span data-ttu-id="7d29f-176">서비스의 SCL 값에 대한 자세한 내용은 [스팸 신뢰 수준](spam-confidence-levels.md)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="7d29f-176">For more information about SCL values in the service, see [Spam confidence levels](spam-confidence-levels.md).</span></span>

8. <span data-ttu-id="7d29f-177">규칙을 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="7d29f-177">Save the rule.</span></span>

## <a name="for-more-information"></a><span data-ttu-id="7d29f-178">자세한 내용</span><span class="sxs-lookup"><span data-stu-id="7d29f-178">For more information</span></span>

[<span data-ttu-id="7d29f-179">정크 메일과 대량 전자 메일의 차이점</span><span class="sxs-lookup"><span data-stu-id="7d29f-179">What's the difference between junk email and bulk email?</span></span>](what-s-the-difference-between-junk-email-and-bulk-email.md)

[<span data-ttu-id="7d29f-180">대량 불만 수준 값</span><span class="sxs-lookup"><span data-stu-id="7d29f-180">Bulk Complaint Level values</span></span>](bulk-complaint-level-values.md)

[<span data-ttu-id="7d29f-181">스팸 필터 정책 구성</span><span class="sxs-lookup"><span data-stu-id="7d29f-181">Configure your spam filter policies</span></span>](configure-your-spam-filter-policies.md)

[<span data-ttu-id="7d29f-182">고급 스팸 필터링 옵션</span><span class="sxs-lookup"><span data-stu-id="7d29f-182">Advanced spam filtering  options</span></span>](advanced-spam-filtering-asf-options.md)
