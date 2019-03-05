---
title: Office 365에서 스팸 메일을 줄이는 방법
ms.author: tracyp
author: MSFTTracyP
manager: laurawi
ms.date: 6/7/2018
ms.audience: Admin
ms.topic: overview
ms.service: O365-seccomp
localization_priority: Priority
search.appverid:
- MOE150
- MET150
ms.assetid: 07824c51-2c45-4005-8596-03c0d7c4ff2a
ms.collection:
- Strat_O365_IP
- M365-security-compliance
- Strat_O365_IP
description: Office 365에서 스팸 및 정크 메일을 줄이는 데 도움이 되는 가장 일반적인 방법을 알아봅니다.
ms.openlocfilehash: 5dac207393864f95f769ac205277b0c969f2fe32
ms.sourcegitcommit: 7adfd8eda038cf25449bdf3df78b5e2fcc1999e7
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/01/2019
ms.locfileid: "30357549"
---
# <a name="how-to-reduce-spam-email-in-office-365"></a><span data-ttu-id="9e71f-103">Office 365에서 스팸 메일을 줄이는 방법</span><span class="sxs-lookup"><span data-stu-id="9e71f-103">How to reduce spam email in Office 365</span></span>

 <span data-ttu-id="9e71f-104">**Office 365에서 스팸이 너무 많이 늘어나나요? 그렇다면 다음을 수행하세요.**</span><span class="sxs-lookup"><span data-stu-id="9e71f-104">**Are you getting too much spam in Office 365? Do this.**</span></span>
  
<span data-ttu-id="9e71f-p101">[보고 메시지 추가 기능을 통해](https://support.office.com/article/b5caa9f1-cdf3-4443-af8c-ff724ea719d2) 거짓 부정 메시지를 보고하여 필터 개선에 도움을 주시기 바랍니다. 또한 메시지를 *첨부 파일로* junk@office365.microsoft.com 또는 phish@office365.microsoft.com(피싱인 경우)으로 전달할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9e71f-p101">We strongly recommend that you report False Negative messages by [using the Report Message add-in](https://support.office.com/article/b5caa9f1-cdf3-4443-af8c-ff724ea719d2) to help us improve our filters. Additionally, you can forward the message *as an attachment* to junk@office365.microsoft.com or phish@office365.microsoft.com (if it was phish).</span></span>

> [!TIP]
> <span data-ttu-id="9e71f-p102">이 메시지가 정크 메일이며 정크 메일 폴더에 있으면 문제가 아닙니다. 어떤 사서함에도 들어 있지 않으면 메시지를 격리하도록 스팸 방지 정책을 변경해야 합니다. 메시지 격리에 대한 자세한 내용은 [Office 365에서 전자 메일 메시지 격리](quarantine-email-messages.md)에서 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9e71f-p102">If you think the message is junk and it is in the Junk Email folder, that should not be a problem. If you don't want to see it at all in the mailbox, you should change the antispam policy to quarantine the message. More information on quarantining a message can be found in [Quarantine email messages in Office 365](quarantine-email-messages.md).</span></span>

## <a name="fixing-allowed-spam"></a><span data-ttu-id="9e71f-110">허용된 스팸 해결</span><span class="sxs-lookup"><span data-stu-id="9e71f-110">Fixing allowed spam</span></span>

<span data-ttu-id="9e71f-p103">잘못된 구성으로 인해 고객의 받은 편지함으로 정크 메일이 들어오는 경우가 많습니다. 가장 일반적인 경우는 메일 흐름 규칙(전송 규칙이라고도 함)의 도메인이 필터를 무시하도록 구성하거나 사용자 도메인이 허용/수신 허용 - 보낸 사람 목록에 포함되는 경우입니다. 이러한 메시지는 스팸 필터링에 걸리지 않고 받은 편지함에 들어올 수 있으므로 바람직하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9e71f-p103">We often see that customers get junk mail into their inbox because of incorrect configurations. The most common of which is configuring your domains in a mail flow rule (also known as a transport rule) to bypass filters or listing your domain(s) in the allowed/safe-senders list. This is not good because these messages skip spam filtering and could have otherwise been caught.</span></span>  

## <a name="solutions-to-other-common-causes-of-getting-too-much-spam"></a><span data-ttu-id="9e71f-114">스팸을 너무 많이 증가하는 다른 일반적인 원인에 대한 해결 방법</span><span class="sxs-lookup"><span data-stu-id="9e71f-114">Solutions to common causes of getting too much spam</span></span>

<span data-ttu-id="9e71f-p104">스팸이 너무 많이 증가하지 않도록 하기 위해 EOP(Exchange Online Protection)는 관리자가 몇 가지 작업을 완료하도록 요구합니다. Office 365 테넌트의 관리자가 아니며 스팸이 너무 많이 발생하는 경우 관리자와 함께 이러한 문제를 해결할 수 있습니다. 그렇지 않은 경우 사용자 작업으로 건너뛸 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9e71f-p104">In order to protect you from getting too much spam, Exchange Online Protection (EOP) requires that administrators complete a few tasks. If you are not the administrator for your Office 365 tenant and you are getting too much spam, then you may want to work with your administrator on these tasks. Otherwise, you can skip to the user section.</span></span>
  
### <a name="for-admins"></a><span data-ttu-id="9e71f-118">관리자</span><span class="sxs-lookup"><span data-stu-id="9e71f-118">For admins</span></span>

- <span data-ttu-id="9e71f-p105">**Office 365를 가리키도록 DNS 레코드 지정** EOP를 통해 최상의 보호를 제공하려면 모든 도메인의 MX(메일 교환기)가 Office 365만 가리켜야 합니다. [DNS 레코드를 관리할 때 Office 365용 DNS 레코드 만들기](https://support.office.com/article/b0f3fdca-8a80-4e8e-9ef3-61e8a2a9ab23)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="9e71f-p105">**Point your DNS records to Office 365** In order for EOP to provide the best protection, your mail exchanger (MX) DNS record(s) for all domains must be pointed to Office 365 -- and only to Office 365. See [Create DNS records for Office 365 when you manage your DNS records](https://support.office.com/article/b0f3fdca-8a80-4e8e-9ef3-61e8a2a9ab23).</span></span>
    
- <span data-ttu-id="9e71f-p106">**모든 사서함에서 정크 메일 규칙 사용** 기본적으로 스팸 필터링 작업은 **정크 메일 폴더로 메시지 이동**으로 설정되어 있습니다. 이것이 기본 설정 및 현재 스팸 정책 작업인 경우 각 사서함에서 [정크 메일 규칙도 사용되도록 설정](https://support.office.com/ko-KR/article/overview-of-the-junk-email-filter-5ae3ea8e-cf41-4fa0-b02a-3b96e21de089)되어야 합니다. 이를 확인하려면 하나 이상의 사서함에 대해 Get-MailboxJunkEmailConfiguration cmdlet을 실행할 수 있습니다. 예를 들어, Get-MailboxJunkEmailConfiguration -Identity \* | Where {$_.Enabled -eq $false}를 실행하여 모든 사서함에 대해 이러한 설정을 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9e71f-p106">**Enable the junk mail rule on all mailboxes** By default, the spam filtering action is set to **Move message to Junk Email folder**. If this is the preferred and current spam policy action, then each mailbox [must also have the junk mail rule enabled](https://support.office.com/ko-KR/article/overview-of-the-junk-email-filter-5ae3ea8e-cf41-4fa0-b02a-3b96e21de089). To check this, you can run the Get-MailboxJunkEmailConfiguration cmdlet against one or more mailboxes. For example, you might check all mailboxes for this by running the following: Get-MailboxJunkEmailConfiguration -Identity \* | Where {$_.Enabled -eq $false}</span></span>
    
    <span data-ttu-id="9e71f-p107">결과에서 Enable 속성이 True로 설정되어야 합니다. False로 설정된 경우 Set-MailboxJunkEmailConfiguration을 실행하여 True로 변경할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9e71f-p107">When viewing the output, the Enable property should be set to True. If it is set to False, you can run Set-MailboxJunkEmailConfiguration to change it to True.</span></span>
    
- <span data-ttu-id="9e71f-p108">**온-프레미스 Exchange Server에서 메일 흐름 규칙 만들기** Exchange Online Protection을 사용하지만 사서함 이 온-프레미스 Exchange 서버에 있는 경우 온-프레미스 Exchange Server에서 몇 가지 메일 흐름 규칙을 만들어야 합니다. [EOP 전용 지침](https://docs.microsoft.com/previous-versions/exchange-server/exchange-150/jj900470(v=exchg.150))을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="9e71f-p108">**Create mail flow rules in on-premises Exchange Server** If you are using Exchange Online Protection, but your mailboxes are located in on-premises Exchange Server, then you will need to create a couple of mail flow rules in on-premises Exchange Server. See the [instructions for EOP-only](https://docs.microsoft.com/previous-versions/exchange-server/exchange-150/jj900470(v=exchg.150)).</span></span>
    
- <span data-ttu-id="9e71f-p109">**대량 전자 메일을 스팸으로 표시** 대량 전자 메일은 사용자가 등록했을 수 있지만 여전히 원치 않을 수 있는 전자 메일입니다. 메시지 헤더에서 X-Microsoft-Antispam 헤더의 BCL(대량 불만 수준) 속성을 찾으세요. BCL 값이 스팸 필터에 설정된 임계값보다 낮으면 이러한 유형의 대량 메시지를 스팸으로 대신 표시하도록 임계값을 조정할 수 있습니다. 사용자마다 [대량 전자 메일을 처리하는 방법](https://docs.microsoft.com/ko-KR/office365/SecurityCompliance/bulk-complaint-level-values)에 대해 다른 임계값 및 기본 설정을 사용할 수 있습니다. 사용자 기본 설정마다 다른 정책 또는 규칙을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9e71f-p109">**Mark bulk email as spam** Bulk email is email which users may have signed up for, but may still be undesirable. In the message header, find the BCL (Bulk Confidence Level) property in the X-Microsoft-Antispam header. If the BCL value is less than the threshold set in the spam filter, you may want to adjust the threshold to instead mark these types of bulk messages as spam. Different users have different tolerances and preferences for [how bulk email](https://docs.microsoft.com/ko-KR/office365/SecurityCompliance/bulk-complaint-level-values) is handled. You can create different policies or rules for different user preferences.</span></span> 
    
- <span data-ttu-id="9e71f-p110">**보낸 사람 즉시 차단** 보낸 사람을 즉시 차단해야 하는 경우 전자 메일 주소, 도메인 또는 IP 주소를 차단할 수 있습니다. [EAC를 사용하여 도메인 또는 사용자가 전송하는 메시지를 차단하는 메일 흐름 규칙 생성](create-organization-wide-safe-sender-or-blocked-sender-lists-in-office-365.md#use-the-eac-to-create-a-mail-flow-rule-that-blocks-messages-sent-from-a-domain-or-user)을 참조하세요. 최종 사용자 허용 목록의 항목이 관리자가 설정한 차단 목록을 재정의할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9e71f-p110">**Immediately block a sender** In the case where you need to immediately block a sender, you can block by email address, domain, or IP address. See [Block email spam with the Office 365 spam filter to prevent false negative issues](create-organization-wide-safe-sender-or-blocked-sender-lists-in-office-365.md#use-the-eac-to-create-a-mail-flow-rule-that-blocks-messages-sent-from-a-domain-or-user). An entry in an end-user allow list can override a block set by the administrator.</span></span>
    
- <span data-ttu-id="9e71f-p111">**사용자에 대한 보고서 메시지 추가 기능 켜기** [사용자에 대한 보고서 메시지 추가 기능을 사용하도록 설정](enable-the-report-message-add-in.md)하는 것이 좋습니다. 관리자는 사용자가 보내는 의견을 보고, 패턴을 사용하여 문제를 유발할 수 있는 설정을 조정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9e71f-p111">**Turn on the report message add-in for users** We strongly recommend that you [enable the report message add-in for you users](enable-the-report-message-add-in.md). As an administrator, you may also be able to view the feedback your users are sending and use any patterns to adjust any settings that may be causing problems.</span></span>
    
### <a name="for-users"></a><span data-ttu-id="9e71f-139">사용자</span><span class="sxs-lookup"><span data-stu-id="9e71f-139">For users</span></span>

- <span data-ttu-id="9e71f-p112">**정크 메일 규칙 사용 및 허용 목록 확인** 정크 메일 작업 규칙이 사용되도록 설정되어 있는지와 보낸 사람 또는 보낸 사람 도메인이 개인 허용 목록에서 우회되도록 설정되어 있지 않은지 확인합니다. 이러한 설정에 액세스하는 가장 좋은 방법은 [차단 또는 허용(정크 전자 메일 설정)](https://support.office.com/article/48c9f6f7-2309-4f95-9a4d-de987e880e46)을 사용하는 것입니다. 여기에서 보낸 사람의 전자 메일 주소 또는 도메인을 차단 하도록 선택할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9e71f-p112">**Enable the junk mail rule and check your allow list** Check that the junk mail action rule is enabled and that the sender or sender's domain is not set to bypass in your personal allow list. The best way to access these settings is from [Block or allow (junk email settings)](https://support.office.com/article/48c9f6f7-2309-4f95-9a4d-de987e880e46). While you are there, you may also choose to block the sender's email address or domain.</span></span>
    
- <span data-ttu-id="9e71f-p113">**Microsoft에 스팸 보고** [보고서 메시지 추가 기능을 사용](https://support.office.com/article/b5caa9f1-cdf3-4443-af8c-ff724ea719d2)하여 Microsoft에 스팸 메시지를 보고합니다. 또한 junk@office365.microsoft.com으로 메시지를 보내고 보고서에 하나 이상의 메시지를 첨부할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9e71f-p113">**Report spam to Microsoft** Report spam messages to Microsoft by using the [Use the Report Message add-in](https://support.office.com/article/b5caa9f1-cdf3-4443-af8c-ff724ea719d2). Additionally, you can send a message to junk@office365.microsoft.com and attach one or more messages to report.</span></span>
    
    <span data-ttu-id="9e71f-145">**중요** 메시지를 첨부 파일로 전달하지 않는 경우 헤더가 누락되며 Office 365에서 스팸 메일 필터링을 개선할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="9e71f-145">**Important** If you do not forward the messages as attachments, then the headers will be missing and we will be unable to improve the junk mail filtering in Office 365.</span></span> 
    
- <span data-ttu-id="9e71f-p114">**대량 전자 메일에서 구독 취소** 사용자가 등록한 메시지이지만(뉴스레터, 제품 알림 등) 신뢰할 수 있는 원본에서 구독 취소 링크가 포함된 경우 구독을 간단히 취소할 수 있습니다. Office 365는 일반적으로 메시지를 스팸으로 처리하지 않습니다. 보낸 사람을 차단하도록 선택할 수도 있고, 관리자에게 모든 대량 메일을 스팸으로 처리하도록 설정 변경을 요청할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9e71f-p114">**Unsubscribe from bulk email** If the message was something that you signed up for (newsletters, product announcements, etc.) and contains an unsubscribe link from a reputable source, you may want to simply unsubscribe. Office 365 does not typically treat these messages as spam. You can also choose to block the sender, or ask your administrator to make a change that will cause all bulk mail to be treated as spam.</span></span>
