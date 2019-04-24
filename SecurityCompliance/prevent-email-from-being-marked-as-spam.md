---
title: Office 365에서 가양성을 발생을 방지하는 방법
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 6/7/2018
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
ms.collection:
- M365-security-compliance
localization_priority: Priority
search.appverid:
- MOE150
- MET150
description: 가양성을 방지하고 Office 365에서 실제 전자 메일을 쓸모없는 상태로 유지하는 방법에 대해 알아보십시오.
ms.openlocfilehash: ecce497269030945457344122a9a218105369be2
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32261242"
---
# <a name="how-to-prevent-real-email-from-being-marked-as-spam-in-office-365"></a><span data-ttu-id="32a8f-103">Office 365에서 실제 전자 메일이 스팸으로 표시되는 일을 방지하는 방법</span><span class="sxs-lookup"><span data-stu-id="32a8f-103">How to prevent real email from being marked as spam in Office 365</span></span>

 <span data-ttu-id="32a8f-104">**실제 전자 메일이 Office 365에서 스팸으로 표시되나요? 그렇다면 다음을 수행하세요.**</span><span class="sxs-lookup"><span data-stu-id="32a8f-104">**Is your real email getting marked as spam in Office 365? Do this.**</span></span>
  
<span data-ttu-id="32a8f-p101">거짓 부정이 있는 경우 [보고서 메시지 추가 기능 사용](https://support.office.com/article/b5caa9f1-cdf3-4443-af8c-ff724ea719d2)을 사용하여 Microsoft에 메시지를 보고해야 합니다. 또한 메시지 *을 첨부 파일*로 not_junk@office365.microsoft.com으로 전달할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="32a8f-p101">If you get a false positive, you should report the message to Microsoft by using the [Use the Report Message add-in](https://support.office.com/article/b5caa9f1-cdf3-4443-af8c-ff724ea719d2). Additionally, you can forward the message *as an attachment* to not_junk@office365.microsoft.com.</span></span>

<span data-ttu-id="32a8f-107">**중요** 메시지를 첨부 파일로 전달하지 않는 경우 헤더가 누락되며 Office 365에서 스팸 메일 필터링을 개선할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="32a8f-107">**Important** If you do not forward the messages as an attachment, then the headers will be missing and we will be unable to improve the junk mail filtering in Office 365.</span></span>
    
## <a name="determine-the-reason-why-the-message-was-marked-as-spam"></a><span data-ttu-id="32a8f-108">메시지가 스팸으로 표시되는 이유 확인</span><span class="sxs-lookup"><span data-stu-id="32a8f-108">Determine the reason why the message was marked as spam</span></span>

<span data-ttu-id="32a8f-p102">Office 365의 스팸 문제는 [전자 메일 메시지 머리글 보기](https://support.office.com/article/cd039382-dc6e-4264-ac74-c048563d212c)를 통해 해결할 수 있으며 잘못된 내용을 파악할 수 있습니다. X-Forefront-Antispam-Report라는 헤더를 찾아야합니다. [스팸 방지 메시지 헤더에 대해 자세히 알아](https://technet.microsoft.com/library/dn205071%28v=exchg.150%29.aspx)볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="32a8f-p102">Many issues with spam in Office 365 can be resolved by [View e-mail message headers](https://support.office.com/article/cd039382-dc6e-4264-ac74-c048563d212c) and determining what went wrong. You will need to look for a header named X-Forefront-Antispam-Report. You can [learn more about anti-spam message headers](https://technet.microsoft.com/library/dn205071%28v=exchg.150%29.aspx).</span></span>
  
<span data-ttu-id="32a8f-112">헤더에서 다음 머리글 및 값을 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="32a8f-112">In the header, look for the following headings and values.</span></span>
  
### <a name="x-forefront-antispam-report"></a><span data-ttu-id="32a8f-113">X-Forefront-Antispam-Report</span><span class="sxs-lookup"><span data-stu-id="32a8f-113">X-Forefront-Antispam-Report</span></span>

- <span data-ttu-id="32a8f-114">**SFV:SPM** EOP 스팸 필터도 인해 메시지가 스팸으로 표시되지 않았음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="32a8f-114">**SFV:SPM** Indicates that the message was marked as spam because of the EOP spam filters.</span></span> 

- <span data-ttu-id="32a8f-115">**SFV:BLK** 보내는 주소가 받는 사람의 수신 거부 보낸 사람 목록에 있기 때문에 메시지가 스팸으로 표시되었음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="32a8f-115">**SFV:BLK** Indicates that the message was marked as spam because the sending address is on the recipient's Blocked Senders List.</span></span> 
    
- <span data-ttu-id="32a8f-p103">**SFV:SKS** 메시지가 콘텐츠 필터 전에 스팸으로 표시되었음을 나타냅니다. 여기에는 메시지를 스팸으로 표시하는 메일 흐름 규칙(전송 규칙이라고도 함)이 포함될 수 있습니다. 메시지 추적을 실행하여 SCL(스팸 지수)이 높게 설정되었을 수 있는 메일 흐름 규칙이 트리거되었는지 알아봅니다.</span><span class="sxs-lookup"><span data-stu-id="32a8f-p103">**SFV:SKS** Indicates that the message was marked as spam prior to the content filter. This could include a mail flow rule (also known as a transport rule) marking the message as spam. Run a message trace to see if a mail flow rule triggered which may have set a high spam confidence level (SCL).</span></span> 
    
- <span data-ttu-id="32a8f-119">**SFV:SKB** 스팸 필터 정책의 차단 목록과 일치하므로 메시지가 스팸으로 표시되었음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="32a8f-119">**SFV:SKB** Indicates that the message was marked as spam because it matched a block list in the spam filter policy.</span></span> 
    
- <span data-ttu-id="32a8f-p104">**SFV:BULK** x-microsoft-antispam 헤더에 있는 BCL(대량 불만 수준) 값이 콘텐츠 필터에 대해 설정된 대량 임계값보다 높음을 나타냅니다. 대량 전자 메일은 사용자가 등록했을 수 있지만 여전히 원치 않을 수 있는 전자 메일입니다. 메시지 헤더에서 X-Microsoft-Antispam 헤더의 BCL(대량 불만 수준) 속성을 찾으세요. BCL 값이 스팸 필터에 설정된 임계값보다 낮으면 이러한 유형의 대량 메시지를 스팸으로 대신 표시하도록 임계값을 조정할 수 있습니다. 사용자마다 [대량 전자 메일을 처리하는 방법](https://docs.microsoft.com/ko-KR/office365/SecurityCompliance/bulk-complaint-level-values)에 대해 다른 임계값 및 기본 설정을 사용할 수 있습니다. 사용자 기본 설정마다 다른 정책 또는 규칙을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="32a8f-p104">**SFV:BULK** Indicates that the Bulk Complaint Level (BCL) value located in the x-microsoft-antispam header is above the Bulk threshold that has been set for the content filter. Bulk email is email which users may have signed up for, but may still be undesirable. In the message header find the BCL (Bulk Confidence Level) property in the X-Microsoft-Antispam header. If the BCL value is less than the threshold set in the Spam Filter, you may want to adjust the threshold to instead mark these types of bulk messages as spam. Different users have different tolerances and preferences for [how bulk email is handled](https://docs.microsoft.com/ko-KR/office365/SecurityCompliance/bulk-complaint-level-values). You can create different policies or rules for different user preferences.</span></span>
    
- <span data-ttu-id="32a8f-p105">**CAT:SPOOF** 또는 **CAT: PHISH** 메시지가 스푸핑된 것을 나타냅니다. 즉, 메시지 원본이 유효한지 검사할 수 없으며 의심스러운 경우를 의미합니다. 유효한 경우 보낸 사람은 SPF 및 DKIM 구성이 올바른지 확인해야 합니다. 자세한 내용은 Authentication-Results 헤더를 확인합니다. 모든 보낸 사람이 적절한 전자 메일 인증 방법을 사용하도록 하는 것은 쉽지 않을 수 있지만 이러한 검사를 우회하는 것은 매우 위험할 수 있으며 보안 위반의 가장 큰 원인이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="32a8f-p105">**CAT:SPOOF** or **CAT:PHISH** Indicates that the message appears to be spoofed, meaning that the message source cannot be validated and could be suspicious. If valid, the sender will need to make sure that they have proper SPF and DKIM configuration. Check the Authentication-Results header for more information. Although it may be difficult to get all senders to use proper email authentication methods, bypassing these checks can be extremely dangerous and is the top cause of compromises.</span></span> 
    
### <a name="x-customspam"></a><span data-ttu-id="32a8f-130">x-customspam</span><span class="sxs-lookup"><span data-stu-id="32a8f-130">x-customspam</span></span>

- <span data-ttu-id="32a8f-p106">이 헤더가 있으면 스팸 필터에서 [고급 스팸 옵션 중 하나가 사용되도록 설정](https://technet.microsoft.com/library/jj200750%28v=exchg.150%29.aspx)되어 있기 때문에 메시지가 스팸으로 표시되었음을 나타냅니다. 이러한 기능이 필요하지 않으면 기본 설정을 사용하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="32a8f-p106">The presence of this header indicates that the message was marked as spam because one of the [advanced spam options is enabled](https://technet.microsoft.com/library/jj200750%28v=exchg.150%29.aspx) in your spam filter. Unless you need these features, we recommend that you use the default settings.</span></span> 
    
## <a name="solutions-to-additional-causes-of-too-much-spam"></a><span data-ttu-id="32a8f-133">너무 많은 스팸을 유발하는 추가 원인에 대한 해결 방법</span><span class="sxs-lookup"><span data-stu-id="32a8f-133">Solutions to additional causes of too much spam</span></span>

<span data-ttu-id="32a8f-p107">효과적인 작동을 위해 EOP(Exchange Online Protection)는 관리자가 몇 가지 작업을 완료하도록 요구합니다. Office 365 테넌트의 관리자가 아니며 스팸이 너무 많이 발생하는 경우 관리자와 함께 이러한 문제를 해결할 수 있습니다. 그렇지 않은 경우 사용자 작업으로 건너뛸 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="32a8f-p107">In order to work effectively, Exchange Online Protection (EOP) requires that administrators complete a few tasks. If you are not the administrator for your Office 365 tenant and you are getting too much spam, then you may want to work with your administrator on these tasks. Otherwise, you can skip to the user section.</span></span>
  
### <a name="for-admins"></a><span data-ttu-id="32a8f-137">관리자</span><span class="sxs-lookup"><span data-stu-id="32a8f-137">For admins</span></span>

- <span data-ttu-id="32a8f-p108">**Office 365를 가리키도록 DNS 레코드 지정** EOP를 통해 보호를 제공하려면 모든 도메인의 MX(메일 교환기)가 Office 365만 가리켜야 합니다. MX가 Office 365를 가리키지 않는 경우, EOP는 사용자를 위해 스팸 필터링를 제공하지 않습니다. 다른 서비스 또는 어플라이언스를 사용하여 도메인에 대한 스팸 필터링을 제공하려는 경우 EOP에서 스팸 보호 기능을 사용하지 않도록 설정하는 것이 좋습니다. SCL 값을 -1로 설 하는 메일 흐름 규칙을 만들어 이렇게 할 수 있습니다. 나중에 EOP를 사용하기로 결정하면 이 메일 흐름 규칙을 제거해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="32a8f-p108">**Point your DNS records to Office 365** In order for EOP to provide protection, your mail exchanger (MX) DNS record(s) for all domains must be pointed to Office 365 -- and only to Office 365. If your MX does not point to Office 365, then EOP will not provide spam filtering for your users. In the situation where you wish to use another service or appliance to provide spam filtering for your domain, you should consider disabling the spam protection in EOP. You can do this by creating a mail flow rule that sets the SCL value to -1. If you later decide to use EOP, make sure to remove this mail flow rule.</span></span> 
    
- <span data-ttu-id="32a8f-p109">**사용자에 대한 보고서 메시지 추가 기능 켜기** [사용자가 보고서 메시지 추가 기능을 사용할 수 있도록 설정](enable-the-report-message-add-in.md)하는 것이 좋습니다. 관리자는 사용자가 보내는 의견을 보고, 패턴을 사용하여 문제를 유발할 수 있는 설정을 조정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="32a8f-p109">**Turn on the report message add-in for users** We strongly recommend that you [enable the report message add-in for your users](enable-the-report-message-add-in.md). As an administrator, you may also be able to view the feedback your users are sending and use any patterns to adjust any settings that may be causing problems.</span></span>

- <span data-ttu-id="32a8f-145">[여기](https://docs.microsoft.com/ko-KR/office365/servicedescriptions/exchange-online-service-description/exchange-online-limits)에 표시된 대로 **사용자가 전자 메일을 송수신하기 위한 허용 한계 내에 있는지 확인하십시오**.</span><span class="sxs-lookup"><span data-stu-id="32a8f-145">**Make sure that your users are inside the allowed limits** for sending and receiving emails as showed [here](https://docs.microsoft.com/ko-KR/office365/servicedescriptions/exchange-online-service-description/exchange-online-limits).</span></span>

 - <span data-ttu-id="32a8f-146">[여기](bulk-complaint-level-values.md)에 명시된 대로 **대량 레벨을 다시 확인하십시오**</span><span class="sxs-lookup"><span data-stu-id="32a8f-146">**Double-check the bulk levels** as specified [here](bulk-complaint-level-values.md)</span></span>
    
### <a name="for-users"></a><span data-ttu-id="32a8f-147">사용자</span><span class="sxs-lookup"><span data-stu-id="32a8f-147">For users</span></span>
    
- <span data-ttu-id="32a8f-p110">**안전한 발신자 목록 만들기** 사용자는 신뢰할 수 있는 발신인의 주소를 [Outlook](https://go.microsoft.com/fwlink/p/?LinkId=270065) 또는 [웹상의 Outlook](https://go.microsoft.com/fwlink/p/?LinkId=294862)에 안전한 발신자 목록에 추가할 수 있습니다. 웹에서 Outlook을 시작하려면 **설정**![을 선택합니다. ](media/24bd5467-c8d2-4936-9c37-a179bd0e21ec.png) \> \*\* 옵션 \*\* \> **차단 또는 허용**합니다. 다음 다이어그램은 안전한 발신자 목록에 무언가를 추가하는 예를 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="32a8f-p110">**Create a safe sender list** Users can add addresses from senders that they trust to their safe sender list in [Outlook](https://go.microsoft.com/fwlink/p/?LinkId=270065) or [Outlook on the Web](https://go.microsoft.com/fwlink/p/?LinkId=294862). To get started in Outlook on the Web, choose **Settings**![ConfigureAPowerBIAnalysisServicesConnector_settingsIcon](media/24bd5467-c8d2-4936-9c37-a179bd0e21ec.png) \> **Options** \> **Block or allow**. The following diagram shows an example of adding something to a safe sender list.</span></span>
  
![웹용 Outlook에 안전한 발신자 추가](media/8de6b24e-429e-4e8f-8ce8-53ba659cbfcb.png)
  
<span data-ttu-id="32a8f-p111">EOP는 사용자의 수신 허용 - 보낸 사람 및 받는 사람을 존중하지만 Safe Domains는 사용하지 않습니다. 이는 도메인이 웹에서 Outlook을 통해 추가되거나 Outlook에서 추가되고 Directory Sync를 사용하여 동기화되는지 여부에 관계없이 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="32a8f-p111">EOP will honor your users' Safe Senders and Recipients, but not Safe Domains. This is true regardless of whether the domain is added through the Outlook on the Web, or added in Outlook and synchronized using Directory Sync.</span></span>

- <span data-ttu-id="32a8f-p112">**Outlook에서 SmartScreen 사용 안 함** 이전 Outlook 데스크톱 클라이언트를 사용하는 경우 지원이 중단된 SmartScreen 필터링 기능을 사용하지 않도록 설정해야 합니다. 이 기능을 사용하도록 설정하면 가양성이 발생할 수 있습니다. 업데이트된 데스크톱 Outlook 클라이언트를 실행하는 경우에는 이 작업이 필요하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="32a8f-p112">**Disable SmartScreen filtering in Outlook** If you are using an older Outlook desktop client, you should disable the SmartScreen filtering functionality, which has been discontinued. If enabled, it can cause false positives. This should not be required if running an updated desktop Outlook client.</span></span>

## <a name="troubleshooting-a-message-ends-up-in-the-junk-folder-even-though-eop-marked-the-message-as-non-spam"></a><span data-ttu-id="32a8f-157">문제 해결 : EOP가 메시지를 스팸이 아닌 것으로 표시했더라도 메시지는 정크 폴더에 놓입니다.</span><span class="sxs-lookup"><span data-stu-id="32a8f-157">Troubleshooting: A message ends up in the Junk folder even though EOP marked the message as non-spam</span></span>


<span data-ttu-id="32a8f-p113">사용자가 Outlook에서 "수신 허용 목록만 허용 : 수신 허용 - 보낸 사람 목록 또는 수신 허용 - 받는 사람 목록의 사람 또는 도메인에게서 온 메일만 받은 편지함으로 배달됩니다" 옵션을 사용하는 경우 모든 전자 메일은 보낸 사람의 정크 메일 폴더로 이동합니다. 보낸 사람이 받는 사람의 수신 허용 목록에 있지 않은 경우 이것은 EOP가 메시지를 스팸이 아닌 것으로 표시했는지 여부와 관계없이 또는 EOP에서 메시지를 스팸이 아닌 것으로 표시하도록 설정한 경우에도 발생합니다.</span><span class="sxs-lookup"><span data-stu-id="32a8f-p113">If your users have the option in Outlook enabled for "Safe Lists Only: Only mail from people or domains on your Safe Senders list or Safe Recipients List will be delivered to your Inbox", then all email will go to the junk folder for a sender unless the sender is on the recipient's Safe Sender list. This will happen regardless of whether EOP marks a message as non-spam, or if you have set up a rule in EOP to mark a message as non-spam.</span></span>
  
<span data-ttu-id="32a8f-160">[ Outlook : 정크 메일 UI를 비활성화하는 정책 설정 및 필터링 메커니즘](https://support.microsoft.com/ko-KR/kb/2180568)의 지침에 따라 Outlook 사용자의 수신 허용 목록 전용 옵션을 비활성화할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="32a8f-160">You can disable the Safe Lists Only option for your Outlook users by following the instructions in [Outlook: Policy setting to disable the Junk E-mail UI and filtering mechanism](https://support.microsoft.com/ko-KR/kb/2180568).</span></span>
  
<span data-ttu-id="32a8f-161">웹용 Outlook에서 메시지를 보면 보낸 사람이 수신자의 보낸 사람 목록에 없기 때문에 메시지가 정크 폴더에 있음을 나타내는 노란색 안전 팁이 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="32a8f-161">If you view the message in Outlook on the Web, there will be a yellow safety tip that indicates that the message is in the Junk folder because the sender is not on the recipient's Safe Senders list.</span></span>
  
<span data-ttu-id="32a8f-p114">메시지의 헤더를 보면 스탬프 SFV: SKN(IP 허용 또는 ETR 허용) 또는 SFV: NSPM(스팸 아님) 스탬프가 포함될 수 있지만 메시지는 여전히 사용자의 정크 폴더에 있습니다. 사용자가 "수신 허용 목록"만 사용하도록 설정한 메시지 헤더에는 아무 것도 없습니다. 이는 Outlook의 사용자가 설정한 "안전 목록 전용" 옵션이 EOP 설정을 무시하기 때문에 발생합니다.</span><span class="sxs-lookup"><span data-stu-id="32a8f-p114">If you look at the header of a message, it may include the stamp SFV:SKN (IP Allow or ETR Allow) or SFV:NSPM (non-spam), but the message is still placed in the user's junk folder. There is nothing in the message header that indicates that the user has "Safe Lists Only" enabled. This happens because the "Safe Lists Only" option set by users in Outlook overrides the EOP setting.</span></span> 
  
 <span data-ttu-id="32a8f-165">\*\*수신 허용 목록의 메시지가 메시지 헤더에 스팸이 아닌 것으로 표시되지만 여전히 사용자의 정크 폴더로 분류되는 이유를 확인하려면 \*\*</span><span class="sxs-lookup"><span data-stu-id="32a8f-165">**To verify why a message from a safe sender is marked as non-spam in the message header, but still ends up in the user's Junk folder**</span></span>
  
1. <span data-ttu-id="32a8f-166">Exchange Online PowerShell로 연결하는 방법을 알아보려면 [Exchange Online PowerShell에 연결](https://go.microsoft.com/fwlink/p/?LinkId=396554)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="32a8f-166">To learn how to connect to Exchange Online PowerShell, see [Connect to Exchange Online PowerShell](https://go.microsoft.com/fwlink/p/?LinkId=396554).</span></span> 
    
2. <span data-ttu-id="32a8f-167">다음 명령을 실행하여 사용자의 정크 메일 구성 설정을 봅니다.</span><span class="sxs-lookup"><span data-stu-id="32a8f-167">Run the following command to view the user's junk email configuration settings:</span></span>
    
  ```Powershell
  Get-MailboxJunkEmailConfiguration example@contoso.com | fl TrustedListsOnly,ContactsTrusted,TrustedSendersAndDomains
  ```

- <span data-ttu-id="32a8f-168">TrustedListsOnly가 True로 설정되면 이 설정이 사용 가능하다는 의미입니다.</span><span class="sxs-lookup"><span data-stu-id="32a8f-168">If TrustedListsOnly is set to True, it means that this setting is enabled</span></span>
- <span data-ttu-id="32a8f-169">ContactsTrusted가 True로 설정되면 사용자가 연락처와 수신 허용 - 보낸 사람 모두를 신뢰함을 의미합니다.</span><span class="sxs-lookup"><span data-stu-id="32a8f-169">If ContactsTrusted is set to True, it means that the user trusts both Contacts and Safe Senders</span></span>
- <span data-ttu-id="32a8f-170">TrustedSendersAndDomains는 사용자의 수신 허용 - 보낸 사람 목록의 내용을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="32a8f-170">The TrustedSendersAndDomains lists the contents of the user's Safe Senders list</span></span>


## <a name="eop-only-customers-use-directory-synchronization"></a><span data-ttu-id="32a8f-171"> EOP 전용 고객: 디렉터리 동기화를 사용</span><span class="sxs-lookup"><span data-stu-id="32a8f-171">EOP-only customers: use directory synchronization</span></span>

<span data-ttu-id="32a8f-p115">EOP 전용 고객의 경우, 즉 온 - 프레미스(Exchange) 전자 메일 서버와 함께 사용하기 위해 EOP 서비스에 가입한 경우 디렉터리 동기화를 사용하여 사용자 설정을 서비스와 동기화해야 합니다. 이렇게 하면 수신 허용 - 보낸 사람 목록이 EOP에 의해 존중되도록 할 수 있습니다. 자세한 내용은 [EOP](https://go.microsoft.com/fwlink/?LinkId=534098)의 메일 사용자 관리에서 "디렉터리 동기화를 사용하여 메일 사용자 관리"를 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="32a8f-p115">If you're an EOP-only customer, that is, you subscribe to the EOP service for use with your on-premises (Exchange) email server, you should sync user settings with the service by using directory synchronization. Doing this ensures that your safe senders lists are respected by EOP. For more information, see "Use directory synchronization to manage mail users" in [Manage Mail Users in EOP](https://go.microsoft.com/fwlink/?LinkId=534098).</span></span>
