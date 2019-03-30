---
title: 스팸 방지 보호 기능 FAQ
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 12/9/2016
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: c534a35d-b121-45da-9d0a-ce738ce51fce
ms.collection:
- M365-security-compliance
description: 이 항목에서는 스팸 방지 보호 기능에 대한 질문과 대답을 제공합니다. 대답은 Microsoft Exchange Online 및 EOP(Exchange Online Protection) 고객에게 해당됩니다.
ms.openlocfilehash: fa2709c995ff9ef83213b86e079a778c61bef3a2
ms.sourcegitcommit: e7a776a04ef6ed5e287a33cfdc36aa2d72862b55
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/29/2019
ms.locfileid: "31000991"
---
# <a name="anti-spam-protection-faq"></a><span data-ttu-id="cf4de-104">스팸 방지 보호 기능 FAQ</span><span class="sxs-lookup"><span data-stu-id="cf4de-104">Anti-spam protection FAQ</span></span>

<span data-ttu-id="cf4de-p102">이 항목에서는 스팸 방지 보호 기능에 대한 질문과 대답을 제공합니다. 대답은 Microsoft Exchange Online 및 EOP(Exchange Online Protection) 고객에게 해당됩니다.</span><span class="sxs-lookup"><span data-stu-id="cf4de-p102">This topic provides frequently asked questions and answers about anti-spam protection. Answers are applicable for Microsoft Exchange Online and Exchange Online Protection (EOP) customers.</span></span> 
  
> [!TIP]
> <span data-ttu-id="cf4de-107">수신 허용-보낸 사람 및 수신 거부 목록에 대 한 질문과 대답은 [Exchange Online의 수신 허용-보낸 사람 및 수신 거부 목록을](safe-sender-and-blocked-sender-lists-faq.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="cf4de-107">For questions and answers about safe sender and blocked sender lists, see [Safe sender and blocked sender lists in Exchange Online](safe-sender-and-blocked-sender-lists-faq.md).</span></span> <span data-ttu-id="cf4de-108">격리에 대한 질문과 대답은 [격리 FAQ](quarantine-faq.md)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="cf4de-108">For questions and answers about the quarantine, see [Quarantine FAQ](quarantine-faq.md).</span></span> 
  
 <span data-ttu-id="cf4de-109">**질문. 스팸으로 검색된 메시지에 대해 기본적으로 수행되는 작업은 무엇입니까?**</span><span class="sxs-lookup"><span data-stu-id="cf4de-109">**Q. By default, what happens to a spam-detected message?**</span></span>
  
<span data-ttu-id="cf4de-p104">대답. **인바운드 메시지의 경우:** 스팸은 대부분 보낸 사람의 IP 주소를 기반으로 하는 연결 필터링을 통해 삭제됩니다. 그런 다음 서비스에서 메시지 내용을 검사합니다. 기본적으로 콘텐츠가 필터링된 스팸이 받는 사람의 정크 메일 폴더로 전송됩니다. 이 작업은 변경할 수 있습니다. 예를 들어 콘텐츠 필터 정책을 구성하여 스팸 메시지를 격리로 대신 보내도록 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cf4de-p104">A. **For inbound messages:** The majority of spam is deleted via connection filtering, which is based on the IP address of the sender. The service then inspects the contents of the message. By default, content-filtered spam is sent to the recipient's Junk Email folder. You can change this action. For example, you can choose to send spam messages to the quarantine instead by configuring the content filter policy.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="cf4de-116">EOP 독립 실행형 고객의 경우: 온-프레미스 사서함에서 **정크 메일 폴더로 메시지 이동** 작업을 수행 하려면 온-프레미스 서버에서 두 개의 Exchange 메일 흐름 규칙 (전송 규칙이 라고도 함)을 구성 하 여 검색 해야 합니다. EOP에서 추가 된 스팸 헤더입니다.</span><span class="sxs-lookup"><span data-stu-id="cf4de-116">For EOP standalone customers: In order to ensure that the **Move message to Junk Email folder** action will work with on-premises mailboxes, you must configure two Exchange mail flow rules (also known as transport rules) on your on-premises servers to detect spam headers added by EOP.</span></span> <span data-ttu-id="cf4de-117">자세한 내용은 [스팸이 각 사용자의 정크 메일 폴더로 라우팅되는지 확인](ensure-that-spam-is-routed-to-each-user-s-junk-email-folder.md)을 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="cf4de-117">For details, see [Ensure that spam is routed to each user's Junk Email folder](ensure-that-spam-is-routed-to-each-user-s-junk-email-folder.md).</span></span> 
  
 <span data-ttu-id="cf4de-118">**아웃바운드 메시지의 경우:** 메시지는 위험성이 높은 배달 풀을 통해 라우팅되거나 반송되어 배달되지 않습니다. 후자의 경우 보낸 사람은 메시지를 배달할 수 없음을 알리는 DSN(배달 상태 알림) 메시지를 받게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="cf4de-118">**For outbound messages:** The message is either routed through the higher risk delivery pool or is bounced and not delivered, in which case the sender should receive a delivery status notification (DSN) message telling them that the message couldn't be delivered.</span></span> 
  
 <span data-ttu-id="cf4de-119">**q. 제로 하루 스팸 변종, 서비스에서 처리 하는 방법**</span><span class="sxs-lookup"><span data-stu-id="cf4de-119">**Q. What's a zero-day spam variant and how is it handled by the service?**</span></span>
  
<span data-ttu-id="cf4de-120">대답.</span><span class="sxs-lookup"><span data-stu-id="cf4de-120">A.</span></span> <span data-ttu-id="cf4de-121">0 일의 스팸 변형은 첫 번째 세대 이며, 이전에는 캡처되지 않거나 분석 되지 않은 스팸의 변종 이며, 스팸 콘텐츠 필터에는 아직 정보를 검색할 수 있는 정보가 없습니다.</span><span class="sxs-lookup"><span data-stu-id="cf4de-121">A zero-day spam variant is a first generation, previously unknown variant of spam that's never been captured or analyzed, so our spam content filters don't yet have any information available for detecting it.</span></span> <span data-ttu-id="cf4de-122">스팸 분석가에 의해 하루 (제로) 스팸 샘플이 캡처 및 분석 된 후 스팸 분류 기준을 충족 하는 경우 스팸 콘텐츠 필터가 업데이트 되어 더 이상 "0 일"로 간주 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="cf4de-122">After a zero-day spam sample is captured and analyzed by our spam analysts, if it meets the spam classification criteria, our spam content filters are updated to detect it, and it's no longer considered "zero-day."</span></span> <span data-ttu-id="cf4de-123">( **참고:** 서비스를 개선 하는 데 도움이 되도록 0 일 동안의 스팸 변종 인 메시지를 받은 경우 microsoft에 [스팸, 스팸 아님 및 피싱 사기 메시지에 설명 된 방법 중 하나를 통해 microsoft에 메시지를 제출 하세요. 분석](submit-spam-non-spam-and-phishing-scam-messages-to-microsoft-for-analysis.md))</span><span class="sxs-lookup"><span data-stu-id="cf4de-123">( **Note:** If you receive a message that may be a zero-day spam variant, in order to help us improve the service, please submit the message to Microsoft using one of the methods described in [Submit spam, non-spam, and phishing scam messages to Microsoft for analysis](submit-spam-non-spam-and-phishing-scam-messages-to-microsoft-for-analysis.md).)</span></span>
  
 <span data-ttu-id="cf4de-124">**질문. 스팸 방지 보호 기능을 제공하도록 서비스를 구성해야 합니까?**</span><span class="sxs-lookup"><span data-stu-id="cf4de-124">**Q. Do I need to configure the service to provide anti-spam protection?**</span></span>
  
<span data-ttu-id="cf4de-p107">대답. 서비스에 등록하고 도메인을 추가하고 나면 기본 스팸 방지 정책을 통해 스팸 필터링이 회사 차원에서 자동으로 사용하도록 설정됩니다. EOP 독립 실행형 고객에게 적용되는 위의 예외를 제외하면 기본 정책은 추가 구성 없이도 사용자를 보호할 수 있도록 조정됩니다. 관리자는 기본 스팸 방지 정책을 편집하여 조직의 요구에 가장 잘 맞게 조정할 수 있습니다. 세분성을 높이기 위해 사용자 지정 콘텐츠 필터 정책을 만들어서 조직의 지정된 사용자, 그룹 또는 도메인에 적용할 수도 있습니다. 사용자 지정 정책은 기본 정책보다 항상 우선하지만 사용자 지정 정책의 우선 순위(즉 실행 순서)를 변경할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cf4de-p107">A. After you sign up for the service and add your domain, spam filtering is automatically enabled company-wide through the default anti-spam policies. The default policies are tuned to protect you without needing any additional configuration (aside from the exception noted above for EOP standalone customers). As an admin, you can edit the default anti-spam policies so that they're tailored to best meet the needs of your organization. For greater granularity, you can also create custom content filter policies and apply them to specified users, groups, or domains in your organization. Custom policies always take precedence over the default policy, but you can change the priority (that is, the running order) of your custom policies.</span></span>
  
<span data-ttu-id="cf4de-131">스팸 방지 정책을 구성하는 방법에 대한 자세한 내용은 다음 항목을 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="cf4de-131">For more about configuring your anti-spam policies, see the following topics:</span></span>
  
[<span data-ttu-id="cf4de-132">연결 필터 정책 구성</span><span class="sxs-lookup"><span data-stu-id="cf4de-132">Configure the connection filter policy</span></span>](configure-the-connection-filter-policy.md)
  
[<span data-ttu-id="cf4de-133">스팸 필터 정책 구성</span><span class="sxs-lookup"><span data-stu-id="cf4de-133">Configure your spam filter policies</span></span>](configure-your-spam-filter-policies.md)
  
[<span data-ttu-id="cf4de-134">아웃바운드 스팸 정책 구성</span><span class="sxs-lookup"><span data-stu-id="cf4de-134">Configure the outbound spam policy</span></span>](configure-the-outbound-spam-policy.md)
  
 <span data-ttu-id="cf4de-135">**질문. 스팸 방지 정책을 변경하는 경우 저장한 변경 내용이 적용될 때까지 시간이 얼마나 걸립니까?**</span><span class="sxs-lookup"><span data-stu-id="cf4de-135">**Q. If I make a change to an anti-spam policy, how long does it take after I save my changes for them to take effect?**</span></span>
  
<span data-ttu-id="cf4de-p108">대답. 변경 내용이 적용되기까지 최대 1시간 정도 걸릴 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cf4de-p108">A. It may take up to 1 hour for the changes to take effect.</span></span>
  
 <span data-ttu-id="cf4de-138">**질문. 대량 전자 메일 필터링은 자동으로 사용하도록 설정됩니까?**</span><span class="sxs-lookup"><span data-stu-id="cf4de-138">**Q. Is bulk email filtering automatically enabled?**</span></span>
  
<span data-ttu-id="cf4de-139">대답.</span><span class="sxs-lookup"><span data-stu-id="cf4de-139">A.</span></span> <span data-ttu-id="cf4de-140">기본적으로 새 고객이 **대량 메일** 고급 스팸 필터링 옵션을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cf4de-140">By default, the **Bulk mail** advanced spam filtering option is enabled for new customers.</span></span> <span data-ttu-id="cf4de-141">마이그레이션한 고객의 경우 이 설정은 FOPE의 구성과 일치합니다.</span><span class="sxs-lookup"><span data-stu-id="cf4de-141">For migrated customers, this setting will match your FOPE configuration.</span></span> <span data-ttu-id="cf4de-142">대량 전자 메일에 대한 자세한 내용은 [정크 메일과 대량 전자 메일의 차이점](what-s-the-difference-between-junk-email-and-bulk-email.md)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="cf4de-142">For more information about bulk email, see [What's the difference between junk email and bulk email?](what-s-the-difference-between-junk-email-and-bulk-email.md)</span></span>
  
 <span data-ttu-id="cf4de-143">**질문. 서비스에서 URL 필터링 기능을 제공합니까?**</span><span class="sxs-lookup"><span data-stu-id="cf4de-143">**Q. Does the service provide URL filtering?**</span></span>
  
<span data-ttu-id="cf4de-p110">대답. 예. 서비스에는 메시지 내의 URL을 확인하는 URL 필터가 포함되어 있습니다. URL이 알려진 스팸에 연결되어 있거나 악의적인 콘텐츠가 검색되면 메시지는 스팸으로 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="cf4de-p110">A. Yes the service has a URL filter that checks for URLs within messages. If URLs associated with known spam or malicious content are detected then the message is marked as spam.</span></span>
  
 <span data-ttu-id="cf4de-147">**질문. 서비스를 사용하는 고객이 거짓 부정(스팸) 및 가양성(스팸 아님) 메시지를 Microsoft로 보내려면 어떻게 해야 합니까?**</span><span class="sxs-lookup"><span data-stu-id="cf4de-147">**Q. How can customers using the service send false negative (spam) and false positive (non-spam) messages to Microsoft?**</span></span>
  
<span data-ttu-id="cf4de-148">대답.</span><span class="sxs-lookup"><span data-stu-id="cf4de-148">A.</span></span> <span data-ttu-id="cf4de-149">스팸 및 스팸이 아닌 메시지는 분석을 위해 여러 가지 방법으로 Microsoft에 제출할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cf4de-149">Spam and non-spam messages can be submitted to Microsoft for analysis in several ways.</span></span> <span data-ttu-id="cf4de-150">자세한 내용은 [분석을 위해 Microsoft에 스팸 및 스팸이 아닌 메시지 제출을](submit-spam-non-spam-and-phishing-scam-messages-to-microsoft-for-analysis.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="cf4de-150">For more information, see [Submit spam, non-spam, and phishing scam messages to Microsoft for analysis](submit-spam-non-spam-and-phishing-scam-messages-to-microsoft-for-analysis.md).</span></span> 
  
 <span data-ttu-id="cf4de-151">**질문. 스팸 보고서를 확인할 수 있습니까?**</span><span class="sxs-lookup"><span data-stu-id="cf4de-151">**Q. Can I get spam reports?**</span></span>
  
<span data-ttu-id="cf4de-152">대답.</span><span class="sxs-lookup"><span data-stu-id="cf4de-152">A.</span></span> <span data-ttu-id="cf4de-153">예를 들어 Microsoft 365 관리 센터에서 스팸 검색 보고서를 받을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cf4de-153">Yes, for example you can get a spam detection report in the Microsoft 365 admin center.</span></span> <span data-ttu-id="cf4de-154">이 보고서는 스팸 볼륨을 고유한 메시지의 수로 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf4de-154">This report shows spam volume as a count of unique messages.</span></span> <span data-ttu-id="cf4de-155">보고에 대한 자세한 내용은 다음 링크를 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="cf4de-155">For more information about reporting, see the following links:</span></span>
  
<span data-ttu-id="cf4de-156">exchange online 고객: [exchange online의 모니터링, 보고 및 메시지 추적](http://technet.microsoft.com/library/87bdeeae-bd80-4a3b-95c5-62fbaf97c2e8.aspx)</span><span class="sxs-lookup"><span data-stu-id="cf4de-156">Exchange Online customers: [Monitoring, Reporting, and Message Tracing in Exchange Online](http://technet.microsoft.com/library/87bdeeae-bd80-4a3b-95c5-62fbaf97c2e8.aspx)</span></span>
  
<span data-ttu-id="cf4de-157">exchange online protection 고객: [Reporting and message trace in exchange online protection](eop/reporting-and-message-trace-in-exchange-online-protection.md)</span><span class="sxs-lookup"><span data-stu-id="cf4de-157">Exchange Online Protection customers: [Reporting and message trace in Exchange Online Protection](eop/reporting-and-message-trace-in-exchange-online-protection.md)</span></span>
  
 <span data-ttu-id="cf4de-158">**질문: 전송된 메시지를 찾을 수 없습니다. 해당 메시지가 스팸으로 검색된 것 같습니다. 이를 확인하는 데 사용할 수 있는 도구가 있습니까?**</span><span class="sxs-lookup"><span data-stu-id="cf4de-158">**Q. Someone sent me a message and I can't find it. I suspect that it may have been detected as spam. Is there a tool that I can use to find out?**</span></span>
  
<span data-ttu-id="cf4de-p113">대답. 예. 메시지 추적 도구를 사용하면 서비스를 통과하는 전자 메일 메시지를 추적하여 메시지에 수행된 작업을 확인할 수 있습니다. 메시지 추적 도구를 사용하여 메시지가 스팸으로 표시된 이유를 확인하는 방법에 대한 자세한 내용은 [메시지가 스팸으로 표시되었습니까?](http://technet.microsoft.com/library/aa49e3f9-a5b1-4410-aac2-ddbbf3f5bfb2.aspx#BKMB_Whywasamessagemarkedasspam)를 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="cf4de-p113">A. Yes, the message trace tool enables you to follow email messages as they pass through the service, in order to find out what happened to them. For more information about how to use the message trace tool to find out why a message was marked as spam, see [Was a message marked as spam? ](http://technet.microsoft.com/library/aa49e3f9-a5b1-4410-aac2-ddbbf3f5bfb2.aspx#BKMB_Whywasamessagemarkedasspam)</span></span>
  
 <span data-ttu-id="cf4de-162">**질문: 사용자가 아웃바운드 스팸을 보내면 서비스에서 메일을 제한(속도 제한)합니까?**</span><span class="sxs-lookup"><span data-stu-id="cf4de-162">**Q. Will the service throttle (rate limit) my mail if my users send outbound spam?**</span></span>
  
<span data-ttu-id="cf4de-163">대답.</span><span class="sxs-lookup"><span data-stu-id="cf4de-163">A.</span></span> <span data-ttu-id="cf4de-164">특정 시간대 (예: 시간당)에서 서비스를 통해 사용자가 보낸 메일의 절반이 Office 365에서 스팸으로 확인 되 면 사용자는 메시지를 보낼 수 없게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="cf4de-164">If more than half of the mail that is sent from a user through the service within a certain time frame (for example, per hour), is determined to be spam by Office 365, the user will be blocked from sending messages.</span></span> <span data-ttu-id="cf4de-165">대부분의 경우 아웃 바운드 메시지가 스팸으로 확인 되 면이 메시지는 높은 위험 배달 풀을 통해 라우팅되며, 일반 아웃 바운드 IP 풀이 차단 목록에 추가 될 가능성을 줄입니다.</span><span class="sxs-lookup"><span data-stu-id="cf4de-165">In most cases, if an outbound message is determined to be spam, it is routed through the high-risk delivery pool, which reduces the probability of the normal outbound-IP pool being added to a block list.</span></span>
  
<span data-ttu-id="cf4de-166">보낸 사람이 아웃바운드 스팸을 보낼 수 없도록 차단된 경우 지정된 전자 메일 주소로 알림을 보낼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cf4de-166">You can send a notification to a specified email address when a sender is blocked sending outbound spam.</span></span> <span data-ttu-id="cf4de-167">이 설정에 대 한 자세한 내용은 [아웃 바운드 스팸 정책 구성을](configure-the-outbound-spam-policy.md)참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="cf4de-167">For more information about this setting, see [Configure the outbound spam policy](configure-the-outbound-spam-policy.md).</span></span>
  
 <span data-ttu-id="cf4de-168">**질문. 타사 스팸 방지 및 맬웨어 방지 공급자와 Exchange Online을 함께 사용할 수 있습니까?**</span><span class="sxs-lookup"><span data-stu-id="cf4de-168">**Q. Can I use a third-party anti-spam and anti-malware provider in conjunction with Exchange Online?**</span></span>
  
<span data-ttu-id="cf4de-p116">대답. 예. Exchange Online 사서함을 보호하도록 다른 스팸 및 맬웨어 필터링 서비스를 구성할 수 있습니다. 인바운드 메일에 대해 이렇게 하려면 타사 공급자를 가리키도록 MX 레코드를 변경하여 이메일 메시지를 타사 공급자로 리디렉션한 다음 추가 처리를 위해 메시지를 EOP로 리디렉션해야 합니다. 아웃바운드 메일에 대해 이렇게 하려면 [Scenario: Outbound Smart Hosting](http://technet.microsoft.com/library/431b3f02-4efd-4bd3-94e7-eecd03f8ef5e.aspx)에 표시된 대로 메시지 배달 대상을 타사 공급자(스마트 호스트)로 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="cf4de-p116">A. Yes, you may configure another spam and malware filtering service to protect your Exchange Online mailboxes. To do this for inbound mail, you should redirect your email messages to the third-party provider by changing your MX records to point to the third-party provider, and then redirect the messages to EOP for additional processing. To do this for outbound mail, please configure the message delivery destination to the third-party provider (smart host), as shown in [Scenario: Outbound Smart Hosting](http://technet.microsoft.com/library/431b3f02-4efd-4bd3-94e7-eecd03f8ef5e.aspx).</span></span>
  
 <span data-ttu-id="cf4de-173">**질문. Microsoft에 피싱 메일로부터 자기 자신을 보호할 수 있는 방법에 대한 설명서가 있습니까?**</span><span class="sxs-lookup"><span data-stu-id="cf4de-173">**Q. Does Microsoft have any documentation about how I can protect myself from phishing scams?**</span></span>
  
<span data-ttu-id="cf4de-p117">대답. 예. 있습니다. 다음 문서를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="cf4de-p117">A. Yes we do, please consult the following articles:</span></span>
  
[<span data-ttu-id="cf4de-176">피싱 메일, 복권 사기 및 기타 유형의 사기에 대한 도움말 보기</span><span class="sxs-lookup"><span data-stu-id="cf4de-176">Get help with phishing scams, lottery fraud, and other types of scams</span></span>](http://go.microsoft.com/fwlink/p/?LinkId=325606)
  
[<span data-ttu-id="cf4de-177">전자 메일 및 웹 사기: 사용자 자신을 보호하는 방법</span><span class="sxs-lookup"><span data-stu-id="cf4de-177">Email and web scams: How to help protect yourself</span></span>](http://go.microsoft.com/fwlink/p/?LinkID=325607)
  
 <span data-ttu-id="cf4de-178">**질문. 스팸 및 맬웨어 메시지의 경우 보낸 사람을 조사하거나 법 집행 기관으로 전송됩니까?**</span><span class="sxs-lookup"><span data-stu-id="cf4de-178">**Q. Are spam and malware messages being investigated as to who sent them, or being transferred to law enforcement entities?**</span></span>
  
<span data-ttu-id="cf4de-p118">대답. 이 서비스에서는 주로 스팸 및 맬웨어 검사와 제거에 집중합니다. 그러나 경우에 따라 특별히 위험하거나 피해를 입히는 스팸 또는 공격자를 조사하고 가해자를 추적하기도 합니다. 이 과정에서 법률 및 디지털 범죄 팀과 협력하여 스패머 봇넷(botnet)을 제거하고, 스패머가 아웃바운드 전자 메일을 보내는 데 서비스를 사용하는 경우 서비스 사용을 차단하고, 범죄 처벌을 위해 관련 정보를 법 집행 기관으로 보낼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cf4de-p118">A. The service focuses on spam and malware detection and removal, though we may occasionally investigate especially dangerous or damaging spam or attack campaigns and pursue the perpetrators. This may involve working with our legal and digital crime units to take down a spammer botnet, blocking the spammer from using the service (if they're using it for sending outbound email), and passing the information on to law enforcement for criminal prosecution.</span></span>
  
 <span data-ttu-id="cf4de-182">**질문. 메일 배달을 보장할 수 있는 가장 좋은 아웃바운드 메일 보내기 방법은 무엇입니까?**</span><span class="sxs-lookup"><span data-stu-id="cf4de-182">**Q. What are a set of best outbound mailing practices that will ensure that my mail is delivered?**</span></span>
  
<span data-ttu-id="cf4de-p119">대답. 아래에 나와 있는 지침이 아웃바운드 전자 메일 메시지를 보내는 모범 사례입니다.</span><span class="sxs-lookup"><span data-stu-id="cf4de-p119">A. The guidelines presented below are best practices for sending outbound email messages.</span></span>
  
1. <span data-ttu-id="cf4de-185">**전자 메일을 보내는 도메인을 DNS에서 확인할 수 있어야 합니다.**</span><span class="sxs-lookup"><span data-stu-id="cf4de-185">**The sending domain of the email should resolve in DNS.**</span></span>
    
    <span data-ttu-id="cf4de-186">보낸 사람이 user@example.com이고 example.com 도메인이 IP 주소 192.0.43.10으로 확인되는 경우를 예로 들어 보겠습니다.</span><span class="sxs-lookup"><span data-stu-id="cf4de-186">For example, if the sender is user@example.com, the domain example.com resolves to the IP address 192.0.43.10.</span></span> <span data-ttu-id="cf4de-187">보내는 도메인의 A 레코드와 MX 레코드가 DNS에 없으면 서비스에서는 메시지 내용이 스팸인지 여부에 관계없이 위험성이 높은 배달 풀을 통하여 해당 메시지를 라우팅합니다.</span><span class="sxs-lookup"><span data-stu-id="cf4de-187">If a sending domain has no A-record and no MX record in DNS, the service will route the message through its higher risk delivery pool regardless of whether or not the content of the message is spam.</span></span> <span data-ttu-id="cf4de-188">위험성이 높은 배달 풀에 대 한 자세한 내용은 [아웃 바운드 메시지에 대 한 위험성이 높은 배달 풀](high-risk-delivery-pool-for-outbound-messages.md)을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="cf4de-188">For more information about the higher risk delivery pool, see [High-risk delivery pool for outbound messages](high-risk-delivery-pool-for-outbound-messages.md).</span></span> 
    
2. <span data-ttu-id="cf4de-189">**아웃바운드 메일 서버의 보내는 IP 주소에 역방향 DNS(PTR) 항목이 있어야 합니다.**</span><span class="sxs-lookup"><span data-stu-id="cf4de-189">**The sending IP address of the outbound mail server should have a reverse DNS (PTR) entry.**</span></span>
    
    <span data-ttu-id="cf4de-190">예를 들어 IP 주소 192.0.43.10에서 메일을 보내는 경우 이 IP의 역방향 DNS 항목은 43-10.any.icann.org입니다.</span><span class="sxs-lookup"><span data-stu-id="cf4de-190">For example, if sending from the IP address 192.0.43.10, the reverse DNS entry for this IP is 43-10.any.icann.org.</span></span> 
    
3. <span data-ttu-id="cf4de-191">**HELO/EHLO 및 MAIL FROM 명령은 일관성이 있어야 하며 IP 주소가 아닌 도메인 이름 형식으로 지정해야 합니다.**</span><span class="sxs-lookup"><span data-stu-id="cf4de-191">**The HELO/EHLO and MAIL FROM commands should be consistent and be present in the form of a domain name rather than an IP address.**</span></span>
    
    <span data-ttu-id="cf4de-192">HELO/EHLO 명령은 보내는 IP 주소의 역방향 DNS와 일치하도록 구성해야 합니다. 그래야 메시지 헤더의 여러 부분에서 도메인이 동일하게 유지됩니다.</span><span class="sxs-lookup"><span data-stu-id="cf4de-192">The HELO/EHLO command should be configured to match the reverse DNS of the sending IP address so that the domain remains the same across the various parts of the message headers.</span></span>
    
4. <span data-ttu-id="cf4de-193">**DNS에서 적절한 SPF 레코드를 설정해야 합니다.**</span><span class="sxs-lookup"><span data-stu-id="cf4de-193">**Ensure that proper SPF records are set up in DNS.**</span></span>
    
    <span data-ttu-id="cf4de-p121">SPF 레코드는 도메인에서 전송된 메일이 실제로 해당 도메인에서 보낸 것이며 스푸핑되지 않았음을 검사하는 메커니즘입니다. SPF 레코드에 대한 자세한 내용은 다음 링크를 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="cf4de-p121">SPF records are a mechanism for validating that mail sent from a domain really is coming from that domain and is not spoofed. For more information about SPF records, see the following links:</span></span>
    
    [<span data-ttu-id="cf4de-196">스푸핑을 방지할 수 있도록 Office 365에서 SPF 설정</span><span class="sxs-lookup"><span data-stu-id="cf4de-196">Set up SPF in Office 365 to help prevent spoofing</span></span>](set-up-spf-in-office-365-to-help-prevent-spoofing.md)
    
    [<span data-ttu-id="cf4de-197">Office 365용 DNS 레코드 만들기</span><span class="sxs-lookup"><span data-stu-id="cf4de-197">Create DNS records for Office 365</span></span>](https://go.microsoft.com/fwlink/?LinkID=275414)
    
5. <span data-ttu-id="cf4de-198">**DKIM으로 전자 메일에 서명을 하는 경우 낮은 수준의 정규화로 서명합니다.**</span><span class="sxs-lookup"><span data-stu-id="cf4de-198">**Signing email with DKIM, sign with relaxed canonicalization.**</span></span>
    
    <span data-ttu-id="cf4de-p122">보낸 사람은 DKIM(Domain Keys Identified Mail)을 사용하여 메시지에 서명을 하고 서비스를 통해 아웃바운드 메일을 보내려는 경우 낮은 수준의 헤더 정규화 알고리즘을 사용하여 서명해야 합니다. 엄격한 헤더 정규화를 사용하여 서명을 하면 메시지가 서비스를 통과할 때 서명이 무효화될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cf4de-p122">If a sender wants to sign their messages using Domain Keys Identified Mail (DKIM) and they want to send outbound mail through the service, they should sign using the relaxed header canonicalization algorithm. Signing with strict header canonicalization may invalidate the signature when it passes through the service.</span></span>
    
6. <span data-ttu-id="cf4de-201">**도메인 소유자는 WHOIS 데이터베이스에 정확한 정보를 포함해야 합니다.**</span><span class="sxs-lookup"><span data-stu-id="cf4de-201">**Domain owners should have accurate information in the WHOIS database.**</span></span>
    
    <span data-ttu-id="cf4de-202">이렇게 하면 고정된 모회사, 담당자 및 이름 서버를 입력함으로써 도메인 소유자 및 소유자에게 연락하는 방법을 파악할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cf4de-202">This identifies the owners of the domain and how to contact them by entering the stable parent company, point of contact, and name servers.</span></span>
    
7. <span data-ttu-id="cf4de-203">**대량 메일러의 경우 보낸 사람: 이름이 메시지를 보내는 사람을 반영해야 하며 메시지의 제목 줄은 메시지 내용에 대한 간략한 요약을 포함해야 합니다.**</span><span class="sxs-lookup"><span data-stu-id="cf4de-203">**For bulk mailers, the From: name should reflect who is sending the message, while the subject line of the message should be a brief summary on what the message is about.**</span></span>
    
    <span data-ttu-id="cf4de-p123">메시지 본문에는 제공 사항, 서비스 또는 제품이 명확하게 표시되어 있어야 합니다. 예를 들어 보낸 사람이 Contoso라는 회사를 위해 대량의 메일을 보내는 경우 전자 메일의 보낸 사람 및 제목은 다음과 같아야 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf4de-p123">The message body should have a clear indication of the offering, service, or product. For example, if a sender is sending out a bulk mailing for the Contoso company, the following is what the email From and Subject should resemble:</span></span>
    
    <span data-ttu-id="cf4de-206">보낸 사람: marketing@contoso.com</span><span class="sxs-lookup"><span data-stu-id="cf4de-206">From: marketing@contoso.com</span></span>
    
    <span data-ttu-id="cf4de-207">제목: 업데이트된 크리스마스 시즌용 신규 카탈로그!</span><span class="sxs-lookup"><span data-stu-id="cf4de-207">Subject: New updated catalog for the Christmas season!</span></span> 
    
    <span data-ttu-id="cf4de-208">다음은 대량 메일임을 충분히 설명하지 않으므로 부적합한 메일의 예입니다.</span><span class="sxs-lookup"><span data-stu-id="cf4de-208">The following is an example of what not to do because it is not descriptive:</span></span>
    
    <span data-ttu-id="cf4de-209">보낸 사람: user@hotmail.com</span><span class="sxs-lookup"><span data-stu-id="cf4de-209">From: user@hotmail.com</span></span>
    
    <span data-ttu-id="cf4de-210">제목: 카탈로그</span><span class="sxs-lookup"><span data-stu-id="cf4de-210">Subject: Catalogs</span></span>
    
8. <span data-ttu-id="cf4de-211">**뉴스레터 형식의 메시지를 많은 수의 받는 사람에게 대량 메일로 보내는 경우에는 메시지 아래쪽에 구독을 취소할 수 있는 수단이 있어야 합니다.**</span><span class="sxs-lookup"><span data-stu-id="cf4de-211">**If sending a bulk mailing to many recipients and the message is in newsletter format, there should be a way of unsubscribing at the bottom of the message.**</span></span>
    
    <span data-ttu-id="cf4de-212">다음과 같은 구독 취소 옵션을 포함해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf4de-212">The unsubscribe option should resemble the following:</span></span>
    
    <span data-ttu-id="cf4de-p124">이 메시지는 sender@fabrikam.com에서 example.@contoso.com으로 전송된 것입니다. 프로필/전자 메일 주소 업데이트 | **SafeUnsubscribe**를 통해 주소 즉시 제거 | 개인 정보 보호 정책</span><span class="sxs-lookup"><span data-stu-id="cf4de-p124">This message was sent to example@contoso.com by sender@fabrikam.com. Update Profile/Email Address | Instant removal with **SafeUnsubscribe**™ | Privacy Policy</span></span>
    
9. <span data-ttu-id="cf4de-215">**대량 전자 메일을 보내는 경우에는 이중 옵트인(opt in)을 통해 목록을 확보해야 합니다. 이중 옵트인(opt in)은 대량 메일러에 대한 업계 모범 사례입니다.**</span><span class="sxs-lookup"><span data-stu-id="cf4de-215">**If sending bulk email, list acquisition should be performed using double opt-in. If you are a bulk mailer, double opt-in is an industry best practice.**</span></span>
    
    <span data-ttu-id="cf4de-216">이중 옵트인(opt in)은 사용자가 마케팅 메일을 신청할 때 두 가지 작업을 수행하도록 요구하는 방식입니다.</span><span class="sxs-lookup"><span data-stu-id="cf4de-216">Double opt-in is the practice of requiring a user to take two actions to sign up for marketing mail:</span></span>
    
1. <span data-ttu-id="cf4de-217">먼저, 사용자는 이전에는 선택하지 않았던 확인란을 클릭하여 마케팅 업체의 서비스 또는 전자 메일 메시지를 계속 받도록 옵트인(opt in)합니다.</span><span class="sxs-lookup"><span data-stu-id="cf4de-217">Once when the user clicks on a previously unchecked check box where they opt-in to receive further offers or email messages from the marketer.</span></span>
    
2. <span data-ttu-id="cf4de-218">다음으로, 사용자가 입력한 전자 메일 주소로 마케팅 업체가 확인 전자 메일을 보내 사용자가 일정 시간 이내에 링크를 클릭하여 확인을 완료하도록 요청합니다.</span><span class="sxs-lookup"><span data-stu-id="cf4de-218">A second time when the marketer sends a confirmation email to the user's provided email address asking them to click on a time-sensitive link that will complete their confirmation.</span></span>
    
    <span data-ttu-id="cf4de-219">이중 옵트인(opt in)을 사용하는 경우 대량 전자 메일 보낸 사람의 신뢰도가 높아집니다.</span><span class="sxs-lookup"><span data-stu-id="cf4de-219">Using double opt-in builds a good reputation for bulk email senders.</span></span>
    
10. <span data-ttu-id="cf4de-220">**대량 전자 메일 보낸 사람은 책임질 수 있는 명확한 콘텐츠를 작성해야 합니다.**</span><span class="sxs-lookup"><span data-stu-id="cf4de-220">**Bulk senders should create transparent content for which they can be held accountable:**</span></span>
    
1. <span data-ttu-id="cf4de-221">받는 사람이 보낸 사람을 주소록에 추가하도록 요청하는 장문의 메시지에서는 해당 작업을 수행해도 배달이 보장되지는 않음을 명확하게 설명해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf4de-221">Verbiage requesting that recipients add the sender to the address book should clearly state that such action is not a guarantee of delivery.</span></span>
    
2. <span data-ttu-id="cf4de-222">메시지 본문에 리디렉션을 구성하는 경우에는 일관성 있는 링크 스타일을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="cf4de-222">When constructing redirects in the body of the message, use a consistent link style.</span></span>
    
3. <span data-ttu-id="cf4de-223">큰 이미지나 첨부 파일, 또는 이미지로만 구성된 메시지를 보내지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="cf4de-223">Don't send large images or attachments, or messages that are solely composed of an image.</span></span>
    
4. <span data-ttu-id="cf4de-224">추적 픽셀(웹 버그 또는 탐지 장치)을 사용할 때는 공개 개인 정보 또는 P3P 설정에서 그러한 항목이 있음을 명기합니다.</span><span class="sxs-lookup"><span data-stu-id="cf4de-224">When employing tracking pixels (web bugs or beacons), clearly state their presence in your public privacy or P3P settings.</span></span>
    
11. <span data-ttu-id="cf4de-225">**아웃바운드 배달 상태 알림의 서식을 지정합니다.**</span><span class="sxs-lookup"><span data-stu-id="cf4de-225">**Format outbound delivery status notifications.**</span></span>
    
    <span data-ttu-id="cf4de-226">배달 상태 알림 메시지를 생성할 때 보낸 사람은 [RFC 3464](https://go.microsoft.com/fwlink/?LinkId=279715)에 지정된 반송 형식을 따라야 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf4de-226">When generating delivery status notification messages, senders should follow the format of a bounce as specified in [RFC 3464](https://go.microsoft.com/fwlink/?LinkId=279715).</span></span>
    
12. <span data-ttu-id="cf4de-227">**존재하지 않는 사용자의 반송된 전자 메일 주소를 제거합니다.**</span><span class="sxs-lookup"><span data-stu-id="cf4de-227">**Remove bounced email addresses for non-existent users.**</span></span>
    
    <span data-ttu-id="cf4de-p125">전자 메일 주소가 더 이상 사용되지 않음을 나타내는 NDR을 받으면 존재하지 않는 전자 메일 별칭을 목록에서 제거합니다. 전자 메일 주소는 시간이 지남에 따라 변경되며, 주소를 삭제하는 사용자도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cf4de-p125">If you receive an NDR indicating that an email address is no longer in use, remove the non-existent email alias from your list. Email addresses change over time, and people sometimes discard them.</span></span>
    
13. <span data-ttu-id="cf4de-230">**Hotmail의 SNDS(Smart Network Data Services) 프로그램을 사용합니다.**</span><span class="sxs-lookup"><span data-stu-id="cf4de-230">**Use Hotmail's Smart Network Data Services (SNDS) program.**</span></span>
    
    <span data-ttu-id="cf4de-p126">Hotmail에서는 최종 사용자가 전송한 불만 사항을 보낸 사람이 확인할 수 있도록 하는 Smart Network Data Services라는 프로그램을 사용합니다. SNDS는 Hotmail에 대한 배달 문제 해결을 위한 기본 포털입니다.</span><span class="sxs-lookup"><span data-stu-id="cf4de-p126">Hotmail uses a program called Smart Network Data Services that allows senders to check complaints submitted by end users. The SNDS is the primary portal for troubleshooting delivery problems to Hotmail.</span></span>
    
## <a name="for-more-information"></a><span data-ttu-id="cf4de-233">자세한 내용</span><span class="sxs-lookup"><span data-stu-id="cf4de-233">For more information</span></span>

[<span data-ttu-id="cf4de-234">Office 365 이메일 스팸 방지 보호</span><span class="sxs-lookup"><span data-stu-id="cf4de-234">Office 365 Email Anti-Spam Protection</span></span>](https://support.office.com/article/6a601501-a6a8-4559-b2e7-56b59c96a586)
  
[<span data-ttu-id="cf4de-235">Exchange Online의 수신 허용-보낸 사람 및 수신 거부 목록</span><span class="sxs-lookup"><span data-stu-id="cf4de-235">Safe sender and blocked sender lists in Exchange Online</span></span>](safe-sender-and-blocked-sender-lists-faq.md)
  
[<span data-ttu-id="cf4de-236">스팸 방지 메시지 헤더</span><span class="sxs-lookup"><span data-stu-id="cf4de-236">Anti-spam message headers</span></span>](anti-spam-message-headers.md)
  
[<span data-ttu-id="cf4de-237">후방 분산 메시지 및 EOP</span><span class="sxs-lookup"><span data-stu-id="cf4de-237">Backscatter messages and EOP</span></span>](backscatter-messages-and-eop.md)
  

