---
title: Office 365에서 실제 전자 메일이 스팸으로 표시되는 일을 방지하는 방법
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 6/7/2018
ms.audience: Admin
ms.topic: overview
ms.service: o365-administration
localization_priority: Priority
ms.collection: Strat_O365_IP
search.appverid: MOE150
ms.assetid: 34823bbc-a3e3-4949-ba42-97c73997eeed
description: 실제 전자 메일이 Office 365에서 스팸으로 표시되고 분류되는 일을 방지하는 방법을 알아봅니다.
ms.openlocfilehash: d092dc0a1a222f51f48102eb8c07e8e6051aa1bd
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22533120"
---
# <a name="how-to-prevent-real-email-from-being-marked-as-spam-in-office-365"></a><span data-ttu-id="6474c-103">Office 365에서 실제 전자 메일이 스팸으로 표시되는 일을 방지하는 방법</span><span class="sxs-lookup"><span data-stu-id="6474c-103">How to prevent real email from being marked as spam in Office 365</span></span>

 <span data-ttu-id="6474c-104">**실제 전자 메일이 Office 365에서 스팸으로 표시되나요? 그렇다면 다음을 수행하세요.**</span><span class="sxs-lookup"><span data-stu-id="6474c-104">**Is your real email getting marked as spam in Office 365? Do this.**</span></span>
  
<span data-ttu-id="6474c-p101">EOP(Exchange Online Protection)는 스팸을 필터링하여 사용자가 원치 않는 콘텐츠를 받은 편지함에서 지우려고 합니다. 그렇지만 경우에 따라 EOP가 필요한 콘텐츠를 필터링하기도 합니다.</span><span class="sxs-lookup"><span data-stu-id="6474c-p101">Exchange Online Protection (EOP) attempts to filter out spam, keeping your Inbox clear of content that users don't want to see. But sometimes, EOP filters out things that you do want to see.</span></span>
  
## <a name="determine-the-reason-why-the-message-was-marked-as-spam"></a><span data-ttu-id="6474c-107">메시지가 스팸으로 표시되는 이유 확인</span><span class="sxs-lookup"><span data-stu-id="6474c-107">Determine the reason why the message was marked as spam</span></span>

<span data-ttu-id="6474c-p102">Office 365의 여러 스팸 문제는 [전자 메일 메시지 헤더를 확인](https://support.office.com/article/cd039382-dc6e-4264-ac74-c048563d212c)하고 잘못된 부분을 파악하여 해결할 수 있습니다. SFV:NSPM 문자열이 포함된 X-Forefront-Antispam-Report 메시지 헤더가 표시될 경우 EOP(Exchange Online Protection)가 해당 메시지를 검색했으며 스팸으로 간주했음을 의미합니다. 이 경우 [보고 메시지 추가 기능을 사용](https://support.office.com/article/b5caa9f1-cdf3-4443-af8c-ff724ea719d2)하여 필터를 개선하는 것이 좋습니다. 헤더에 이 값이 표시되지 않으면 전자 메일이 스팸 검사를 통과하지 못했거나 메시지를 스팸으로 잘못 분류하게 만드는 구성 문제가 있는 것입니다. [스팸 방지 메시지 헤더에 대한 자세한 내용](https://technet.microsoft.com/library/dn205071%28v=exchg.150%29.aspx)을 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6474c-p102">Many issues with spam in Office 365 can be resolved by [View e-mail message headers](https://support.office.com/article/cd039382-dc6e-4264-ac74-c048563d212c) and determining what went wrong. If you see a message header named X-Forefront-Antispam-Report that contains the string SFV:NSPM, this means that Exchange Online Protection (EOP) scanned the message and thought it was spam. In this case, we strongly recommend that you [Use the Report Message add-in](https://support.office.com/article/b5caa9f1-cdf3-4443-af8c-ff724ea719d2) to help us improve our filters. If you don't see this value in the headers, it could mean either that the mail didn't pass through spam scanning, or that there was a configuration issue which caused the message to be incorrectly classified as spam. You can [learn more about anti-spam message headers](https://technet.microsoft.com/library/dn205071%28v=exchg.150%29.aspx).</span></span>
  
<span data-ttu-id="6474c-113">헤더에서 다음 머리글 및 값을 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="6474c-113">In the header, look for the following headings and values.</span></span>
  
### <a name="x-forefront-antispam-report"></a><span data-ttu-id="6474c-114">X-Forefront-Antispam-Report</span><span class="sxs-lookup"><span data-stu-id="6474c-114">X-Forefront-Antispam-Report</span></span>

- <span data-ttu-id="6474c-115">**SFV:BLK** 보내는 주소가 받는 사람의 수신 거부 보낸 사람 목록에 있기 때문에 메시지가 스팸으로 표시되었음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="6474c-115">**SFV:BLK** Indicates that the message was marked as spam because the sending address is on the recipient's Blocked Senders List.</span></span> 
    
- <span data-ttu-id="6474c-p103">**SFV:SKS** 메시지가 콘텐츠 필터 전에 스팸으로 표시되었음을 나타냅니다. 여기에는 메시지를 스팸으로 표시하는 전송 규칙이 포함될 수 있습니다. 메시지 추적을 실행하여 SCL(스팸 지수)이 높게 설정되었을 수 있는 전송 규칙이 트리거되었는지 알아봅니다.</span><span class="sxs-lookup"><span data-stu-id="6474c-p103">**SFV:SKS** Indicates that the message was marked as spam prior to the content filter. This could include a transport rule marking the message as spam. Run a message trace to see if a transport rule triggered which may have set a high spam confidence level (SCL).</span></span> 
    
- <span data-ttu-id="6474c-119">**SFV:SKB** 스팸 필터 정책의 차단 목록과 일치하므로 메시지가 스팸으로 표시되었음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="6474c-119">**SFV:SKB** Indicates that the message was marked as spam because it matched a block list in the spam filter policy.</span></span> 
    
- <span data-ttu-id="6474c-p104">**SFV:BULK** x-microsoft-antispam 헤더에 있는 BCL(대량 불만 수준) 값이 콘텐츠 필터에 대해 설정된 대량 임계값보다 높음을 나타냅니다. 대량 전자 메일은 사용자가 등록했을 수 있지만 여전히 원치 않을 수 있는 전자 메일입니다. 메시지 헤더에서 X-Microsoft-Antispam 헤더의 BCL(대량 불만 수준) 속성을 찾으세요. BCL 값이 스팸 필터에 설정된 임계값보다 낮으면 이러한 유형의 대량 메시지를 스팸으로 대신 표시하도록 임계값을 조정할 수 있습니다. 사용자마다 [대량 전자 메일을 처리하는 방법](https://blogs.msdn.microsoft.com/tzink/2014/08/25/different-levels-of-bulk-mail-filtering-in-office-365/)에 대해 다른 임계값 및 기본 설정을 사용할 수 있습니다. 사용자 기본 설정마다 다른 정책 또는 규칙을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6474c-p104">**SFV:BULK** Indicates that the Bulk Complaint Level (BCL) value located in the x-microsoft-antispam header is above the Bulk threshold that has been set for the content filter. Bulk email is email which users may have signed up for, but may still be undesirable. In the message header find the BCL (Bulk Confidence Level) property in the X-Microsoft-Antispam header. If the BCL value is less than the threshold set in the Spam Filter, you may want to adjust the threshold to instead mark these types of bulk messages as spam. Different users have different tolerances and preferences for [how bulk email is handled](https://blogs.msdn.microsoft.com/tzink/2014/08/25/different-levels-of-bulk-mail-filtering-in-office-365/). You can create different policies or rules for different user preferences.</span></span>
    
- <span data-ttu-id="6474c-p105">**CAT:SPOOF** 또는 **CAT: PHISH** 메시지가 스푸핑된 것을 나타냅니다. 즉, 메시지 원본이 유효한지 검사할 수 없으며 의심스러운 경우를 의미합니다. 유효한 경우 보낸 사람은 SPF 및 DKIM 구성이 올바른지 확인해야 합니다. 자세한 내용은 Authentication-Results 헤더를 확인합니다. 모든 보낸 사람이 적절한 전자 메일 인증 방법을 사용하도록 하는 것은 쉽지 않을 수 있지만 이러한 검사를 우회하는 것은 매우 위험할 수 있으며 보안 위반의 가장 큰 원인이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6474c-p105">**CAT:SPOOF** or **CAT:PHISH** Indicates that the message appears to be spoofed, meaning that the message source cannot be validated and could be suspicious. If valid, the sender will need to make sure that they have proper SPF and DKIM configuration. Check the Authentication-Results header for more information. Although it may be difficult to get all senders to use proper email authentication methods, bypassing these checks can be extremely dangerous and is the top cause of compromises.</span></span> 
    
### <a name="x-customspam"></a><span data-ttu-id="6474c-130">x-customspam</span><span class="sxs-lookup"><span data-stu-id="6474c-130">x-customspam</span></span>

- <span data-ttu-id="6474c-p106">이 헤더가 있으면 스팸 필터에서 [고급 스팸 옵션 중 하나가 사용되도록 설정](https://technet.microsoft.com/library/jj200750%28v=exchg.150%29.aspx)되어 있기 때문에 메시지가 스팸으로 표시되었음을 나타냅니다. 이러한 기능이 필요하지 않으면 기본 설정을 사용하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="6474c-p106">The presence of this header indicates that the message was marked as spam because one of the [advanced spam options is enabled](https://technet.microsoft.com/library/jj200750%28v=exchg.150%29.aspx) in your spam filter. Unless you need these features, we recommend that you use the default settings.</span></span> 
    
## <a name="solutions-to-additional-causes-of-too-much-spam"></a><span data-ttu-id="6474c-133">너무 많은 스팸을 유발하는 추가 원인에 대한 해결 방법</span><span class="sxs-lookup"><span data-stu-id="6474c-133">Solutions to additional causes of too much spam</span></span>

<span data-ttu-id="6474c-p107">효과적인 작동을 위해 EOP(Exchange Online Protection)는 관리자가 몇 가지 작업을 완료하도록 요구합니다. Office 365 테넌트의 관리자가 아니며 스팸이 너무 많이 발생하는 경우 관리자와 함께 이러한 문제를 해결할 수 있습니다. 그렇지 않은 경우 사용자 작업으로 건너뛸 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6474c-p107">In order to work effectively, Exchange Online Protection (EOP) requires that administrators complete a few tasks. If you are not the administrator for your Office 365 tenant and you are getting too much spam, then you may want to work with your administrator on these tasks. Otherwise, you can skip to the user section.</span></span>
  
### <a name="for-admins"></a><span data-ttu-id="6474c-137">관리자</span><span class="sxs-lookup"><span data-stu-id="6474c-137">For IT admins:</span></span>

- <span data-ttu-id="6474c-p108">**Office 365를 가리키도록 DNS 레코드 지정** EOP를 통해 보호를 제공하려면 모든 도메인의 MX(메일 교환기)가 Office 365만 가리켜야 합니다. MX가 Office 365를 가리키지 않는 경우, EOP는 사용자를 위해 스팸 필터링를 제공하지 않습니다. 다른 서비스 또는 어플라이언스를 사용하여 도메인에 대한 스팸 필터링을 제공하려는 경우 EOP에서 스팸 보호 기능을 사용하지 않도록 설정하는 것이 좋습니다. SCL 값을 -1로 설 하는 전송 규칙을 만들어 이렇게 할 수 있습니다. 나중에 EOP를 사용하기로 결정하면 이 전송 규칙을 제거해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="6474c-p108">**Point your DNS records to Office 365** In order for EOP to provide protection, your mail exchanger (MX) DNS record(s) for all domains must be pointed to Office 365 -- and only to Office 365. If your MX does not point to Office 365, then EOP will not provide spam filtering for your users. In the situation where you wish to use another service or appliance to provide spam filtering for your domain, you should consider disabling the spam protection in EOP. You can do this by creating a transport rule that sets the SCL value to -1. If you later decide to use EOP, make sure to remove this transport rule.</span></span> 
    
- <span data-ttu-id="6474c-p109">**Outlook에서 SmartScreen 사용 안 함** 사용자가 Outlook 데스크톱 클라이언트를 사용하는 경우 지원이 중단된 SmartScreen 필터링 기능을 사용하지 않도록 설정해야 합니다. 이 기능을 사용하도록 설정하면 가양성이 발생할 수 있습니다. 업데이트된 데스크톱 Outlook 클라이언트를 실행하는 경우에는 이 작업이 필요하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6474c-p109">**Disable SmartScreen filtering in Outlook** If your users are using the Outlook desktop client, they should disable the SmartScreen filtering functionality, which has been discontinued. If enabled, it can cause false positives. This should not be required if running an updated desktop Outlook client.</span></span> 
    
- <span data-ttu-id="6474c-p110">**사용자에 대한 보고서 메시지 추가 기능 켜기** [사용자에 대한 보고서 메시지 추가 기능을 사용하도록 설정](enable-the-report-message-add-in.md)하는 것이 좋습니다. 관리자는 사용자가 보내는 의견을 보고, 패턴을 사용하여 문제를 유발할 수 있는 설정을 조정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6474c-p110">**Turn on the report message add-in for users** We strongly recommend that you [enable the report message add-in for you users](enable-the-report-message-add-in.md). As an administrator, you may also be able to view the feedback your users are sending and use any patterns to adjust any settings that may be causing problems.</span></span>
    
- <span data-ttu-id="6474c-p111">**보낸 사람 허용 즉시** 보낸 사람을 즉시 허용해야 하는 경우, **특정 보낸 사람의 IP 주소만 허용**하는 것이 좋습니다. 또는 보낸 사람을 허용하고, 보낸 사람 도메인과 성공적인 Authentication-Results 헤더를 **둘 다** 찾는 전송 규칙을 만들어 보낸 사람이 SPF 또는 DKIM과 같은 인증 검사를 통과하는지 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6474c-p111">**Immediately allow a sender** In the case where you need to immediately allow a sender, we strongly recommend that you **ONLY allow a particular sender's IP address**. Alternately, you can allow a sender and also make sure that the sender passes an authentication check like SPF or DKIM by creating a transport rule that looks for **both** the sender domain and a successful Authentication-Results header.</span></span> 
    
### <a name="for-users"></a><span data-ttu-id="6474c-150">사용자</span><span class="sxs-lookup"><span data-stu-id="6474c-150">For users</span></span>

- <span data-ttu-id="6474c-p112">**Microsoft에 스팸 보고** [보고서 메시지 추가 기능을 사용](https://support.office.com/article/b5caa9f1-cdf3-4443-af8c-ff724ea719d2)하여 Microsoft에 스팸 메시지를 보고합니다. 또한 junk@office365.microsoft.com으로 메시지를 보내고 보고서에 하나 이상의 메시지를 첨부할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6474c-p112">**Report spam to Microsoft** Report spam messages to Microsoft by using the [Use the Report Message add-in](https://support.office.com/article/b5caa9f1-cdf3-4443-af8c-ff724ea719d2). Additionally, you can send a message to junk@office365.microsoft.com and attach one or more messages to report.</span></span>
    
    <span data-ttu-id="6474c-153">**중요** 메시지를 첨부 파일로 전달하지 않는 경우 [헤더가 누락되며 Office 365에서 스팸 메일 필터링을 개선할 수 없습니다](https://blogs.msdn.microsoft.com/tzink/2017/11/30/when-creating-support-tickets-about-spam-be-sure-to-include-message-headers/).</span><span class="sxs-lookup"><span data-stu-id="6474c-153">**Important** If you do not forward the messages as attachments, then [the headers will be missing and we will be unable to improve](https://blogs.msdn.microsoft.com/tzink/2017/11/30/when-creating-support-tickets-about-spam-be-sure-to-include-message-headers/) the junk mail filtering in Office 365.</span></span> 
    
- <span data-ttu-id="6474c-p113">**허용 목록에 보낸 사람 추가(제한적으로만 사용)** 마지막 수단으로 [차단 또는 허용(정크 메일 설정)](https://support.office.com/article/48c9f6f7-2309-4f95-9a4d-de987e880e46)할 수 있습니다. 이렇게 하면 대상이 지정된 피싱 시도가 받은 편지함에 대해 허용될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6474c-p113">**Add a sender to your allow list - but use sparingly** As a last resort, you can [Block or allow (junk email settings)](https://support.office.com/article/48c9f6f7-2309-4f95-9a4d-de987e880e46). If you do so, you should beware that a targeted phishing attempt may be allowed into your inbox.</span></span>
    

