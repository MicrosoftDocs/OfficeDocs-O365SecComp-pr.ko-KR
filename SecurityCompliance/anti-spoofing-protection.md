---
title: Office 365의 스푸핑 방지 보호 기능
ms.author: tracyp
author: MSFTtracyp
manager: laurawi
ms.date: 03/29/2019
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
search.appverid:
- MET150
ms.assetid: d24bb387-c65d-486e-93e7-06a4f1a436c0
ms.collection:
- M365-security-compliance
- Strat_O365_IP
ms.custom: TopSMBIssues
localization_priority: Priority
description: 이 문서에서는 Office 365가 위조된 보낸 사람 도메인, 즉 스푸핑된 도메인을 사용하는 피싱 공격을 줄이는 방법에 대해 설명합니다. 표준 전자 메일 인증 방법이나 다른 보낸 사람 신뢰도 기술을 사용하지 않고 메시지를 분석하고 인증할 수 있는 메시지를 차단하여 이 작업을 수행합니다. 이 변경 사항은 Office 365의 조직이 피싱 공격에 노출된 수를 줄이기 위해 구현되었습니다.
ms.openlocfilehash: 455ce577e4ffb3dc4d943004dd3c299e7e6f1eae
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/17/2019
ms.locfileid: "34155780"
---
# <a name="anti-spoofing-protection-in-office-365"></a><span data-ttu-id="fd2dd-105">Office 365의 스푸핑 방지 보호 기능</span><span class="sxs-lookup"><span data-stu-id="fd2dd-105">Anti-spoofing protection in Office 365</span></span>

<span data-ttu-id="fd2dd-106">이 문서에서는 Office 365가 위조된 보낸 사람 도메인, 즉 스푸핑된 도메인을 사용하는 피싱 공격을 줄이는 방법에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-106">This article describes how Office 365 mitigates against phishing attacks that use forged sender domains, that is, domains that are spoofed.</span></span> <span data-ttu-id="fd2dd-107">메시지를 분석하고 표준 전자 메일 인증 방법이나 다른 보낸 사람 신뢰도 기술을 이용해서는 인증될 수 없는 메시지를 차단하여 이 작업을 수행합니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-107">It accomplishes this by analyzing the messages and blocking the ones that cannot be authenticated using standard email authentication methods, nor other sender reputation techniques.</span></span> <span data-ttu-id="fd2dd-108">이 변경 사항은 Office 365의 조직이 피싱 공격에 노출된 수를 줄이기 위해 구현되었습니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-108">This change was implemented to reduce the number of phishing attacks to which organizations in Office 365 are exposed.</span></span>
  
<span data-ttu-id="fd2dd-109">또한 이 문서는 이러한 변경 사항이 발생한 이유, 고객이 변경에 대비할 수 있는 방법, 손상된 메시지를 보는 방법, 메시지에 대해 보고하는 방법, 잘못된 탐지를 완화하는 방법 및 Microsoft에 보내는  사람이 이 변경 사항에 대비할 수 있는 방법에 대해서도 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-109">This article also describes why this change is being made, how customers can prepare for this change, how to view messages that will be affected, how to report on messages, how to mitigate false positives, as well as how senders to Microsoft should prepare for this change.</span></span>
  
<span data-ttu-id="fd2dd-110">초기에 Microsoft의 스푸핑 방지 기술은 Office 365 Enterprise E5 구독이 있거나 해당 구독에 대한 Office 365 ATP(Advanced Threat Protection) 추가 기능을 구입 한 조직에 배포되었습니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-110">Microsoft's anti-spoofing technology was initially deployed to its organizations that had an Office 365 Enterprise E5 subscription or had purchased the Office 365 Advanced Threat Protection (ATP) add-on for their subscription.</span></span> <span data-ttu-id="fd2dd-111">2018 년 10월을 기준으로 Microsoft는 Exchange Online Protection(EOP)을 지닌 조직으로 보호를 확대했습니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-111">As of October, 2018 we extended the protection to organizations that have Exchange Online Protection (EOP) as well.</span></span> <span data-ttu-id="fd2dd-112">또한 모든 필터가 서로에게서 배우는 방식 때문에 Outlook.com 사용자에게도 영향을 줄 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-112">Additionally, because of the way all of our filters learn from each other, Outlook.com users may also be affected.</span></span>
  
## <a name="how-spoofing-is-used-in-phishing-attacks"></a><span data-ttu-id="fd2dd-113">피싱 공격에서 스푸핑 사용 방법</span><span class="sxs-lookup"><span data-stu-id="fd2dd-113">How spoofing is used in phishing attacks</span></span>

<span data-ttu-id="fd2dd-114">사용자 보호와 관련해 Microsoft는 피싱 위협을 심각한 위험으로 간주합니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-114">When it comes to protecting its users, Microsoft takes the threat of phishing seriously.</span></span> <span data-ttu-id="fd2dd-115">스팸 발송자와 피싱 사용자가 일반적으로 사용하는 기술 중 하나는 발신자가 위조 된 스푸핑이며 실제 발신자가 아닌 다른 사람이 메시지를 보낸 것처럼 보입니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-115">One of the techniques that spammers and phishers commonly use is spoofing, which is when the sender is forged, and a message appears to originate from someone or somewhere other than the actual source.</span></span> <span data-ttu-id="fd2dd-116">이 기법은 사용자 자격 증명을 얻기 위해 고안된 피싱 캠페인에서 주로 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-116">This technique is often used in phishing campaigns designed to obtain user credentials.</span></span> <span data-ttu-id="fd2dd-117">Microsoft의 스푸핑 방지 기술은 특히 Outlook과 같은 전자 메일 클라이언트에 나타나는 '보는 사람: 머리글'의 위조 여부를 검사합니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-117">Microsoft's Anti-spoof technology specifically examines forgery of the 'From: header' which is the one that shows up in an email client like Outlook.</span></span> <span data-ttu-id="fd2dd-118">Microsoft가 보낸 사람: 머리글이 스푸핑되었을 확률이 높다고 확신하는 경우, 이 메시지를 스푸핑으로 식별합니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-118">When Microsoft has high confidence that the From: header is spoofed, it identifies the message as a spoof.</span></span>
  
<span data-ttu-id="fd2dd-119">스푸핑 메시지는 실제 사용자에게 두 가지 부정적인 영향을 미칩니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-119">Spoofing messages have two negative implications for real life users:</span></span>
  
### <a name="1-spoofed-messages-deceive-users"></a><span data-ttu-id="fd2dd-120">1. 위조 메시지의 사용자 기만</span><span class="sxs-lookup"><span data-stu-id="fd2dd-120">1. Spoofed messages deceive users</span></span>
  
<span data-ttu-id="fd2dd-121">첫째, 스푸핑된 메시지는 사용자가 링크를 클릭하고 자격 증명을 포기하거나 맬웨어를 다운로드하거나 민감한 콘텐츠가 있는 메시지에 회신하도록 할 수 있습니다(후자는 비즈니스 전자 메일 손상이라고 함).</span><span class="sxs-lookup"><span data-stu-id="fd2dd-121">First, a spoofed message may trick a user into clicking a link and giving up their credentials, downloading malware, or replying to a message with sensitive content (the latter of which is known as Business Email Compromise).</span></span> <span data-ttu-id="fd2dd-122">예를 들어 다음은 스푸핑된 발신자가 포함된 msoutlook94@service.outlook.com이라는 피싱 메일입니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-122">For example, the following is a phishing message with a spoofed sender of msoutlook94@service.outlook.com:</span></span>
  
![ervice.outlook.com로 위장한 피싱 메일](media/1a441f21-8ef7-41c7-90c0-847272dc5350.jpg)
  
<span data-ttu-id="fd2dd-124">위의 메일은 실제로 service.outlook.com에서 발송되지 않았지만 마치 그런 것처럼 보이도록 phisher에 의해 스푸핑되었습니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-124">The above did not actually come from service.outlook.com, but instead was spoofed by the phisher to make it look like it did.</span></span> <span data-ttu-id="fd2dd-125">이 메일은 사용자가 메시지 안의 링크를 클릭하도록 유도합니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-125">It is attempting to trick a user into clicking the link within the message.</span></span>
  
<span data-ttu-id="fd2dd-126">다음 예시는 contoso.com을 스푸핑합니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-126">The next example is spoofing contoso.com:</span></span>
  
![피싱 메시지 - 비즈니스 전자 메일 손상](media/da15adaa-708b-4e73-8165-482fc9182090.jpg)
  
<span data-ttu-id="fd2dd-128">이 메시지는 적법한 것처럼 보이지만 실제로는 스푸핑입니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-128">The message looks legitimate, but in fact is a spoof.</span></span> <span data-ttu-id="fd2dd-129">이 피싱 메시지는 피싱의 하위 범주인 비즈니스 전자 메일 손상의 한 종류입니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-129">This phishing message is a type of Business Email Compromise which is a subcategory of phishing.</span></span>

### <a name="2-users-confuse-real-messages-for-fake-ones"></a><span data-ttu-id="fd2dd-130">2. 사용자가 실제 메시지를 가짜 메시지로 오인</span><span class="sxs-lookup"><span data-stu-id="fd2dd-130">2. Users confuse real messages for fake ones</span></span>
  
<span data-ttu-id="fd2dd-131">둘째, 스푸핑된 메시지는 피싱 메시지에 대해 알고 있지만 실제 메시지와 스푸핑된 메시지의 차이를 알 수 없는 사용자에게 불확실성을 유발합니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-131">Second, spoofed messages create uncertainty for users who know about phishing messages but cannot tell the difference between a real message and spoofed one.</span></span> <span data-ttu-id="fd2dd-132">예를 들어, 다음은 Microsoft 보안 계정 전자 메일 주소에서 발송된 실제 암호 재설정의 예입니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-132">For example, the following is an example of an actual password reset from the Microsoft Security account email address:</span></span>
  
![Microsoft의 합법적인 암호 재설정](media/58a3154f-e83d-4f86-bcfe-ae9e8c87bd37.jpg)
  
<span data-ttu-id="fd2dd-134">위의 메시지는 Microsoft에서 발송되었지만 사용자는 링크를 클릭해 자격 증명을 포기하거나 맬웨어를 다운로드하게 하고 또는 중요한 콘텐츠가 포함된 메시지에 회신하도록 만드는 피싱 메시지를 받는 데 익숙합니다. </span><span class="sxs-lookup"><span data-stu-id="fd2dd-134">The above message did come from Microsoft, but at the same time, users are used to getting phishing messages that may trick a user into clicking a link and giving up their credentials, downloading malware, or replying to a message with sensitive content.</span></span> <span data-ttu-id="fd2dd-135">실제 암호 재설정과 가짜 암호 변경의 차이점을 알기 어렵기 때문에 많은 사용자가 이러한 메시지를 무시하거나 스팸으로 신고하고 또는 불필요하게 Microsoft에 이를 누락된 피싱(Phishing) 메시지로 다시 보고합니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-135">Because it is difficult to tell the difference between a real password reset and a fake one, many users ignore these messages, report them as spam, or unnecessarily report the messages back to Microsoft as missed phishing scams.</span></span>

<span data-ttu-id="fd2dd-136">스푸핑을 중단하기 위해 이메일 필터링 업계에서는 [SPF](https://docs.microsoft.com/office365/SecurityCompliance/set-up-spf-in-office-365-to-help-prevent-spoofing), [DKIM](https://docs.microsoft.com/office365/SecurityCompliance/use-dkim-to-validate-outbound-email) 및 [DMARC](https://docs.microsoft.com/office365/SecurityCompliance/use-dmarc-to-validate-email)와 같은 전자 메일 인증 프로토콜을 개발했습니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-136">To stop spoofing, the email filtering industry has developed email authentication protocols such as [SPF](https://docs.microsoft.com/office365/SecurityCompliance/set-up-spf-in-office-365-to-help-prevent-spoofing), [DKIM](https://docs.microsoft.com/office365/SecurityCompliance/use-dkim-to-validate-outbound-email), and [DMARC](https://docs.microsoft.com/office365/SecurityCompliance/use-dmarc-to-validate-email).</span></span> <span data-ttu-id="fd2dd-137">DMARC는 SPF를 통과한 도메인 또는 DKIM를 통해 사용자가 전자 메일 클라이언트에서 볼 수 있는 메시지 보낸 사람(위의 예에서는 service.outlook.com, outlook.com 및 accountprotection.microsoft.com)을 검사해 스푸핑을 방지합니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-137">DMARC prevents spoofing examining a message's sender - the one that the user sees in their email client (in the examples above, this is service.outlook.com, outlook.com, and accountprotection.microsoft.com) - with the domain that passed SPF or DKIM.</span></span> <span data-ttu-id="fd2dd-138">즉, 사용자가 보는 도메인은 인증되었으므로 스푸핑되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-138">That is, the domain that the user sees has been authenticated and is therefore not spoofed.</span></span> <span data-ttu-id="fd2dd-139">더 자세한 내용은 이 문서의 "*전자 메일 인증만으로 스푸핑을 막을 수 없는 이유 이해하기"* 섹션을 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-139">For a more complete discussion, see the section "*Understanding why email authentication is not always enough to stop spoofing"*  later on in this article.</span></span>
  
<span data-ttu-id="fd2dd-140">그러나 문제는 전자 메일 인증 레코드가 선택 사항이며 의무가 아니라는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-140">However, the problem is that email authentication records are optional, not required.</span></span> <span data-ttu-id="fd2dd-141">따라서 microsoft.com 및 skype.com과 같은 강력한 인증 정책을 사용하는 도메인은 스푸핑으로부터 보호되지만, 인증 정책을 약하게 게시하거나 전혀 정책을 게시하지 않는 도메인은 스푸핑의 대상이 됩니다. 2018년 3월 현재 Fortune지 500대 기업 의 도메인 중 9%만이 강력한 전자 메일 인증 정책을 발표했습니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-141">Therefore, while domains with strong authentication policies like microsoft.com and skype.com are protected from spoofing, domains that publish weaker authentication policies, or no policy at all, are targets for being spoofed.As of March 2018, only 9% of domains of companies in the Fortune 500 publish strong email authentication policies.</span></span> <span data-ttu-id="fd2dd-142">나머지 91%는 피셔가 스푸핑을 할 수 있으며 전자 메일 필터가 다른 정책을 사용하여 이를 탐지하지 않는 한 최종 사용자에게 전달되어 사용자를 속일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-142">The remaining 91% may be spoofed by a phisher, and unless the email filter detects it using another policy, may be delivered to an end user and deceive them:</span></span>
  
![Fortune 500대 기업의 DMARC 정책](media/84e77d34-2073-4a8e-9f39-f109b32d06df.jpg)
  
<span data-ttu-id="fd2dd-144">Fortune 500 대 기업에 속하지 않은 중소 규모 기업의 전자 메일 인증 정책 강화 비율은 낮고, 이 비율은 북미 및 서유럽 이외의 지역에서는 더 낮습니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-144">The proportion of small-to-medium sized companies that are not in the Fortune 500 that publish strong email authentication policies is smaller, and smaller still for domains that are outside of North America and western Europe.</span></span>
  
<span data-ttu-id="fd2dd-145">이는 기업이 전자 메일 인증의 작동 방식을 알지 못하는 반면 피싱 사기업은 이를 이해하고 그 한계를 활용하기 때문에 큰 문제입니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-145">This is a big problem because while enterprises may not be aware of how email authentication works, phishers do understand and take advantage of the lack of it.</span></span>
  
<span data-ttu-id="fd2dd-146">SPF, DKIM, DMARC 설치에 대한 내용은 이 문서 뒷편의 "*Office 365 고객"* 섹션을 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-146">For information on setting up SPF, DKIM, and DMARC, see the section "*Customers of Office 365"*  later on in this document.</span></span> 
  
## <a name="stopping-spoofing-with-implicit-email-authentication"></a><span data-ttu-id="fd2dd-147">암시적 전자 메일 인증 스푸핑 중지</span><span class="sxs-lookup"><span data-stu-id="fd2dd-147">Stopping spoofing with implicit email authentication</span></span>

<span data-ttu-id="fd2dd-148">피싱 및 스피어 피싱은 큰 문제이고 강력한 전자 메일 인증 정책은 제한적으로 채택되어 있으므로 Microsoft는 고객 보호 기능에 투자를 계속하고 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-148">Because phishing and spear phishing is such a problem, and because of the limited adoption of strong email authentication policies, Microsoft continues to invest in capabilities to protect its customers.</span></span> <span data-ttu-id="fd2dd-149">따라서 Microsoft는 *암시적인 전자 메일 인증*으로 앞서나가고 있습니다. 도메인이 인증하지 않으면 Microsoft는 전자 메일 인증 레코드를 게시 한 것처럼 처리하고 통과하지 못하면 그에 맞게 처리합니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-149">Therefore, Microsoft is moving ahead with  *implicit email authentication* - if a domain doesn't authenticate, Microsoft will treat it as if it had published email authentication records and treat it accordingly if it doesn't pass.</span></span> 
  
<span data-ttu-id="fd2dd-150">이를 위해 Microsoft는 보낸 사람 신뢰도, 보낸 사람/받는 사람 기록, 동작 분석 및 기타 고급 기술을 비롯한 일반 전자 메일 인증에 대한 다양한 확장 기능을 구축했습니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-150">To accomplish this, Microsoft has built numerous extensions to regular email authentication including sender reputation, sender/recipient history, behavioral analysis, and other advanced techniques.</span></span> <span data-ttu-id="fd2dd-151">전자 메일 인증을 게시하지 않는 도메인에서 보낸 메시지는 합법적임을 나타내는 다른 신호가 포함되어 있지 않으면 스푸핑으로 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-151">A message sent from a domain that doesn't publish email authentication will be marked as spoof unless it contains other signals to indicate that it is legitimate.</span></span>
  
<span data-ttu-id="fd2dd-152">이를 통해 최종 사용자는 보낸 전자 메일이 스푸핑되지 않았다고 확신할 수 있고 보낸 사람은 아무도 자신의 도메인을 가장하지 못한다는 확신을 가질 수 있으며 Office 365 고객은 가장 보호와 같은 더 우수한 보호 기능을 제공할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-152">By doing this, end users can have confidence that an email sent to them has not been spoofed, senders can be confident that nobody is impersonating their domain, and customers of Office 365 can offer even better protection such as Impersonation protection.</span></span>
  
<span data-ttu-id="fd2dd-153">Microsoft의 일반 공지 사항을 확인ㅎ려면 [피싱의 세계 2장 - Office 365의 향상된 스푸핑 방지](https://techcommunity.microsoft.com/t5/Security-Privacy-and-Compliance/Schooling-A-Sea-of-Phish-Part-2-Enhanced-Anti-spoofing/ba-p/176209)를 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-153">To see Microsoft's general announcement, see [A Sea of Phish Part 2 - Enhanced Anti-spoofing in Office 365](https://techcommunity.microsoft.com/t5/Security-Privacy-and-Compliance/Schooling-A-Sea-of-Phish-Part-2-Enhanced-Anti-spoofing/ba-p/176209).</span></span>
  
## <a name="identifying-that-a-message-is-classified-as-spoofed"></a><span data-ttu-id="fd2dd-154">메시지가 스푸핑로 분류되는지 식별</span><span class="sxs-lookup"><span data-stu-id="fd2dd-154">Identifying that a message is classified as spoofed</span></span>

### <a name="composite-authentication"></a><span data-ttu-id="fd2dd-155">복합 인증</span><span class="sxs-lookup"><span data-stu-id="fd2dd-155">Composite authentication</span></span>

<span data-ttu-id="fd2dd-156">SPF, DKIM 및 DMARC는 모두 유용하지만 메시지에 명시적인 인증 레코드가 없는 경우 충분한 인증 상태를 전달하지 못합니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-156">While SPF, DKIM, and DMARC are all useful by themselves, they don't communicate enough authentication status in the event a message has no explicit authentication records.</span></span> <span data-ttu-id="fd2dd-157">따라서 Microsoft는 여러 신호를 복합 인증이라는 단일 값 또는 간략히 compauth로 결합한 알고리즘을 개발했습니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-157">Therefore, Microsoft has developed an algorithm that combines multiple signals into a single value called Composite Authentication, or compauth for short.</span></span> <span data-ttu-id="fd2dd-158">Office 365의 고객은 메시지 머리글의 *Authentication-Results* 머리글에 스탬프된 compauth 값을 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-158">Customers in Office 365 have compauth values stamped into the *Authentication-Results* header in the message headers.</span></span> 
  
```
Authentication-Results:
  compauth=<fail|pass|softpass|none> reason=<yyy>

```

|<span data-ttu-id="fd2dd-159">**CompAuth 결과**</span><span class="sxs-lookup"><span data-stu-id="fd2dd-159">**CompAuth result**</span></span>|<span data-ttu-id="fd2dd-160">**설명**</span><span class="sxs-lookup"><span data-stu-id="fd2dd-160">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="fd2dd-161">실패</span><span class="sxs-lookup"><span data-stu-id="fd2dd-161">fail</span></span>|<span data-ttu-id="fd2dd-162">메시지가 명시적 인증(DNS에 명시적으로 도메인 게시 레코드 전송) 또는 암시적 인증(도메인 전송이 DNS에 레코드를 게시하지 않아 Office 365에서 레코드를 게시한 것처럼 결과를 삽입)에 실패했습니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-162">Message failed explicit authentication (sending domain published records explicitly in DNS) or implicit authentication (sending domain did not publish records in DNS, so Office 365 interpolated the result as if it had published records).</span></span>|
|<span data-ttu-id="fd2dd-163">통과</span><span class="sxs-lookup"><span data-stu-id="fd2dd-163">pass</span></span>|<span data-ttu-id="fd2dd-164">메시지가 명시적 인증 (DMARC 또는 [최상의 추측 통과 DMARC ](https://blogs.msdn.microsoft.com/tzink/2015/05/06/what-is-dmarc-bestguesspass-in-office-365)) 또는 높은 신뢰성을 가진 암시적 인증(도메인은 전자 메일 인증 레코드를 게시하지 않지만 Office 365는 메시지가 적법할 가능성이 높음을 나타내는 강력한 백엔드 신호를 가짐)을 통과했습니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-164">Message passed explicit authentication (message passed DMARC, or [Best Guess Passed DMARC](https://blogs.msdn.microsoft.com/tzink/2015/05/06/what-is-dmarc-bestguesspass-in-office-365)) or implicit authentication with high confidence (sending domain does not publish email authentication records, but Office 365 has strong backend signals to indicate the message is likely legitimate).</span></span>|
|<span data-ttu-id="fd2dd-165">softpass</span><span class="sxs-lookup"><span data-stu-id="fd2dd-165">softpass</span></span>|<span data-ttu-id="fd2dd-166">메시지는 낮은 - 중간 신뢰도를 가진 암시적 인증(보내는 도메인은 전자 메일 인증을 게시하지 않지만 Office 365는 메시지가 합법적이지만 신호의 강도가 약함을 나타내는 백엔드 신호를 가짐)을 통과했습니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-166">Message passed implicit authentication with low-to-medium confidence (sending domain does not publish email authentication, but Office 365 has backend signals to indicate the message is legitimate but the strength of the signal is weaker).</span></span>|
|<span data-ttu-id="fd2dd-167">없음</span><span class="sxs-lookup"><span data-stu-id="fd2dd-167">none</span></span>|<span data-ttu-id="fd2dd-168">메시지가 인증되지 않았지만(인증되었지만 정렬되지 않음), 발신자 신뢰도 또는 기타 요인으로 인해 복합 인증이 적용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-168">Message did not authenticate (or it did authenticate but did not align), but composite authentication not applied due to sender reputation or other factors.</span></span>|
   
|||
|:-----|:-----|
|<span data-ttu-id="fd2dd-169">**이유**</span><span class="sxs-lookup"><span data-stu-id="fd2dd-169">**Reason**</span></span>|<span data-ttu-id="fd2dd-170">**설명**</span><span class="sxs-lookup"><span data-stu-id="fd2dd-170">**Description**</span></span>|
|<span data-ttu-id="fd2dd-171">0xx</span><span class="sxs-lookup"><span data-stu-id="fd2dd-171">0xx</span></span>|<span data-ttu-id="fd2dd-172">메시지가 복합 인증에 실패했습니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-172">Message failed composite authentication.</span></span><br/><span data-ttu-id="fd2dd-173">**000**이면 메시지 거부 또는 격리과 함께 메시지가DMARC에 실패합니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-173">**000** means the message failed DMARC with an action of reject or quarantine.</span></span>  <br/><span data-ttu-id="fd2dd-174">**001**이면 메시지가 암시적 전자 메일 인증에 실패합니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-174">**001** means the message failed implicit email authentication.</span></span> <span data-ttu-id="fd2dd-175">이는 보내는 도메인에 전자 메일 인증 레코드가 게시되지 않았거나 인증 레코드가 경우에는 실패 정책이 약함(SPF soft fail 또는 중립, p=none인 DMARC 정책)을 의미합니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-175">This means that the sending domain did not have email authentication records published, or if they did, they had a weaker failure policy (SPF soft fail or neutral, DMARC policy of p=none).</span></span>  <br/><span data-ttu-id="fd2dd-176">**002**은 보낸 사람/도메인 쌍에 대해 스푸핑된 전자 메일을 보내는 것을 명시적으로 금지하는 정책을 가지고 있음을 의미합니다. 이 설정은 관리자가 수동으로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-176">**002** means the organization has a policy for the sender/domain pair that is explicitly prohibited from sending spoofed email, this setting is manually set by an administrator.</span></span>  <br/><span data-ttu-id="fd2dd-177">**010**은 메시지가 거부 또는 격리 작업과 함께 DMARC에서 실패했음을 의미하며 전송 도메인은 조직에서 허용하는 도메인 중 하나입니다(이는 자체 대 자체 또는 내부 조직, 스푸핑의 일부).</span><span class="sxs-lookup"><span data-stu-id="fd2dd-177">**010** means the message failed DMARC with an action of reject or quarantine, and the sending domain is one of your organization's accepted-domains (this is part of self-to-self, or intra-org, spoofing).</span></span>  <br/><span data-ttu-id="fd2dd-178">**011**은 메시지가 암시적 전자 메일 인증에 실패했음을 의미하며 전송 도메인은 조직에서 허용하는 도메인 중 하나입니다(이는 자체 대 자체 또는 내부 조직, 스푸핑의 일부).</span><span class="sxs-lookup"><span data-stu-id="fd2dd-178">**011** means the message failed implicit email authentication, and the sending domain is one of your organization's accepted domains (this is part of self-to-self, or intra-org, spoofing).</span></span>|
|<span data-ttu-id="fd2dd-179">기타 모든 코드(1xx, 2xx, 3xx, 4xx, 5xx)</span><span class="sxs-lookup"><span data-stu-id="fd2dd-179">All other codes (1xx, 2xx, 3xx, 4xx, 5xx)</span></span>|<span data-ttu-id="fd2dd-180">메시지가 암시적 인증을 통과한 이유나 인증이 없지만 조치가 적용되지 않은 이유에 대한 다양한 내부 코드에 해당합니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-180">Corresponds to various internal codes for why a message passed implicit authentication, or had no authentication but no action was applied.</span></span>|
   
<span data-ttu-id="fd2dd-181">메시지의 머리글을 보고 관리자 또는 최종 사용자는 Office 365가 어떻게 보낸 사람이 스푸핑되었을 가능성이 있다는 결론을 내렸는지 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-181">By looking at the headers of a message, an administrator or even an end user can determine how Office 365 arrives at the conclusion that the sender may be spoofed.</span></span>
  
### <a name="differentiating-between-different-types-of-spoofing"></a><span data-ttu-id="fd2dd-182">다양한 유형의 스푸핑 구분</span><span class="sxs-lookup"><span data-stu-id="fd2dd-182">Differentiating between different types of spoofing</span></span>

<span data-ttu-id="fd2dd-183">Microsoft는 두 가지 유형의 스푸핑 메시지를 구분합니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-183">Microsoft differentiates between two different types of spoofing messages:</span></span>
  
 <span data-ttu-id="fd2dd-184">**조직 내 스푸핑**</span><span class="sxs-lookup"><span data-stu-id="fd2dd-184">**Intra-org spoofing**</span></span>
  
<span data-ttu-id="fd2dd-185">자체 스푸핑이라고도 하며 보낸 사람: 주소의 도메인이받는 사람 도메인과 동일하거나 일치할 때(수신자 도메인이 조직의 [수락 도메인](https://technet.microsoft.com/ko-KR/library/jj945194%28v=exchg.150%29.aspx) 중 하나인 경우) 또는 보낸 사람: 주소의 도메인이 동일한 조직의 일부인 경우에 발생합니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-185">Also known as self-to-self spoofing, this occurs when the domain in the From: address is the same as, or aligns with, the recipient domain (when recipient domain is one of your organization's [Accepted Domains](https://technet.microsoft.com/en-us/library/jj945194%28v=exchg.150%29.aspx)); or, when the domain in the From: address is part of the same organization.</span></span>
  
<span data-ttu-id="fd2dd-186">예를 들어, 다음은 동일한 도메인(contoso.com)의 보낸 사람과 받는 사람입니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-186">For example, the following has sender and recipient from the same domain (contoso.com).</span></span> <span data-ttu-id="fd2dd-187">이 페이지에서 스팸봇 수확을 방지하기 위해 전자 메일 주소에 공백이 삽입됩니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-187">Spaces are inserted into the email address to prevent spambot harvesting on this page):</span></span>
  
<span data-ttu-id="fd2dd-188">발신자: 보낸 사람@contoso.com </span><span class="sxs-lookup"><span data-stu-id="fd2dd-188">From: sender @ contoso.com</span></span>
  
<span data-ttu-id="fd2dd-189">수신자: 받는 사람@contoso.com</span><span class="sxs-lookup"><span data-stu-id="fd2dd-189">To: recipient @ contoso.com</span></span>
  
<span data-ttu-id="fd2dd-190">다음에는 보낸 사람 도메인과 받는 사람 도메인이 조직 도메인(fabrikam.com)과 정렬되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-190">The following has the sender and recipient domains aligning with the organizational domain (fabrikam.com):</span></span>
  
<span data-ttu-id="fd2dd-191">발신자: 보낸 사람@ foo.fabrikam.com</span><span class="sxs-lookup"><span data-stu-id="fd2dd-191">From: sender @ foo.fabrikam.com</span></span>
  
<span data-ttu-id="fd2dd-192">수신자: 받는 사람@ bar.fabrikam.com</span><span class="sxs-lookup"><span data-stu-id="fd2dd-192">To: recipient @ bar.fabrikam.com</span></span>
  
<span data-ttu-id="fd2dd-193">다음의 보낸 사람 도메인과 받는 사람 도메인은 다릅니다(microsoft.com 및 bing.com). 하지만 이들은 동일한 조직에 속합니다(즉, 둘 다 조직의 수락 도메인의 일부).</span><span class="sxs-lookup"><span data-stu-id="fd2dd-193">The following sender and recipient domains are different (microsoft.com and bing.com), but they belong to the same organization (that is, both are part of the organization's Accepted Domains):</span></span>
  
<span data-ttu-id="fd2dd-194">발신자: 보낸 사람@microsoft.com</span><span class="sxs-lookup"><span data-stu-id="fd2dd-194">From: sender @ microsoft.com</span></span>
  
<span data-ttu-id="fd2dd-195">수신자: 받는 사람@bing.com</span><span class="sxs-lookup"><span data-stu-id="fd2dd-195">To: recipient @ bing.com</span></span>
  
<span data-ttu-id="fd2dd-196">조직 내 스푸핑에 실패한 메시지에는 머리글에 다음 값이 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-196">Messages that fail intra-org spoofing contain the following values in the headers:</span></span>
  
<span data-ttu-id="fd2dd-197">X-Forefront-Antispam-Report: ...CAT:SPM/HSPM/PHSH;...SFTY:9.11</span><span class="sxs-lookup"><span data-stu-id="fd2dd-197">X-Forefront-Antispam-Report: ...CAT:SPM/HSPM/PHSH;...SFTY:9.11</span></span>
  
<span data-ttu-id="fd2dd-198">CAT은 메시지의 범주이며 일반적으로 SPM(스팸)으로 스탬프 처리되지만 때에 따라 메시지에서 패턴 유형이 어떻게 다르게 나타나는지에 따라 HSPM(높은 신뢰성을 가진 스팸) 또는 PHISH(피싱)일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-198">The CAT is the category of the message, and it is normally stamped as SPM (spam), but occasionally may be HSPM (high confidence spam) or PHISH (phishing) depending upon what other types of patterns occur in the message.</span></span>
  
<span data-ttu-id="fd2dd-199">SFTY는 메시지의 안전 수준이며 첫 번째 숫자 (9)는 메시지가 피싱을 의미하고 점 (11) 뒤에 오는 두 번째 숫자 집합은 조직 내 스푸핑을 의미합니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-199">The SFTY is the safety level of the message, the first digit (9) means the message is phishing, and second set of digits after the dot (11) means it is intra-org spoofing.</span></span>
  
<span data-ttu-id="fd2dd-200">조직 내 스푸핑에 대한 복합 인증의 구체적인 이유 코드는 없으며 향후 2018년 내에 스탬프 처리될 예정입니다(일정 미정).</span><span class="sxs-lookup"><span data-stu-id="fd2dd-200">There is no specific reason code for Composite Authentication for intra-org spoofing, that will be stamped later in 2018 (timeline not yet defined).</span></span>
  
 <span data-ttu-id="fd2dd-201">**도메인 간 스푸핑**</span><span class="sxs-lookup"><span data-stu-id="fd2dd-201">**Cross-domain spoofing**</span></span>
  
<span data-ttu-id="fd2dd-202">이 문제는 보낸 사람: 주소의 보내는 도메인이 받는 조직의 외부 도메인인 경우에 발생합니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-202">This occurs when the sending domain in the From: address is an external domain to the receiving organization.</span></span> <span data-ttu-id="fd2dd-203">도메인 간 스푸핑으로 인해 복합 인증에 실패하는 메시지에는 머리글에 다음과 같은 값이 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-203">Messages that fail Composite Authentication due to cross-domain spoofing contain the following values in the headers:</span></span>
  
<span data-ttu-id="fd2dd-204">Authentication-Results: …</span><span class="sxs-lookup"><span data-stu-id="fd2dd-204">Authentication-Results: …</span></span> <span data-ttu-id="fd2dd-205">compauth=fail reason=000/001</span><span class="sxs-lookup"><span data-stu-id="fd2dd-205">compauth=fail reason=000/001</span></span>
  
<span data-ttu-id="fd2dd-206">X-Forefront-Antispam-Report: ...CAT:SPOOF;...SFTY:9.22</span><span class="sxs-lookup"><span data-stu-id="fd2dd-206">X-Forefront-Antispam-Report: ...CAT:SPOOF;...SFTY:9.22</span></span>
  
<span data-ttu-id="fd2dd-207">두 경우 모두 다음의 빨간색 안전 팁이 메시지에 스탬프 처리되거나 받는 사람 사서함의 언어에 맞게 사용자 지정되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-207">In both cases, the following red safety tip is stamped in the message, or an equivalent that is customized to the recipient mailbox's language:</span></span>
  
![빨간색 보안 팁 - 사기 탐지](media/a366156a-14e8-4c14-bfe5-2031b21936f8.jpg)
  
<span data-ttu-id="fd2dd-209">보낸 사람: 주소를 봐야만 받는 사람 전자 메일이 무엇인지 파악하거나 전자 메일 머리말을 검사해야만 조직 내 및 도메인 간 스푸핑을 구분할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-209">It's only by looking at the From: address and knowing what your recipient email is, or by inspecting the email headers, that you can differentiate between intra-org and cross-domain spoofing.</span></span>
  
## <a name="how-customers-of-office-365-can-prepare-themselves-for-the-new-anti-spoofing-protection"></a><span data-ttu-id="fd2dd-210">Office 365의 고객이 새로운 스푸핑 방지 기능에 대비할 수 있는 방법</span><span class="sxs-lookup"><span data-stu-id="fd2dd-210">How customers of Office 365 can prepare themselves for the new anti-spoofing protection</span></span>

### <a name="information-for-administrators"></a><span data-ttu-id="fd2dd-211">관리자에 대한 정보</span><span class="sxs-lookup"><span data-stu-id="fd2dd-211">Information for administrators</span></span>

<span data-ttu-id="fd2dd-212">Office 365의 조직 관리자는 여러 가지 중요한 정보를 알고 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-212">As an administrator of an organization in Office 365, there are several key pieces of information you should be aware of.</span></span>
  
### <a name="understanding-why-email-authentication-is-not-always-enough-to-stop-spoofing"></a><span data-ttu-id="fd2dd-213">전자 메일 인증만으로 스푸핑을 막지 못하는 이유를 이해해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-213">Understanding why email authentication is not always enough to stop spoofing</span></span>

<span data-ttu-id="fd2dd-214">새로운 스푸핑 방지 보호 기능은 전자 메일 인증(SPF, DKIM 및 DMARC)을 사용하여 메시지를 스푸핑으로 표시하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-214">The new anti-spoofing protection relies on email authentication (SPF, DKIM, and DMARC) to not mark a message as spoofing.</span></span> <span data-ttu-id="fd2dd-215">일반적인 예는 보내는 도메인이 SPF 레코드를 게시한 적이 없는 경우입니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-215">A common example is when a sending domain has never published SPF records.</span></span> <span data-ttu-id="fd2dd-216">SPF 레코드가 없거나 잘못 설정된 경우 보낸 메시지는 메시지가 합법적이라고 표시하는 백엔드 인텔리전스가 없는 한 스푸핑된 것으로 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-216">If there are no SPF records or they are incorrectly set up, a sent message will be marked as spoofed unless Microsoft has back-end intelligence that says the message is legitimate.</span></span>
  
<span data-ttu-id="fd2dd-217">예를 들어 스푸핑 방지가 설치되기 이전의 메시지는 SPF 레코드, DKIM 레코드 및 DMARC 레코드 없이 다음과 같이 보일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-217">For example, prior to anti-spoofing being deployed, a message may have looked like the following with no SPF record, no DKIM record, and no DMARC record:</span></span> 
  
```
Authentication-Results: spf=none (sender IP is 1.2.3.4)
  smtp.mailfrom=example.com; contoso.com; dkim=none
  (message not signed) header.d=none; contoso.com; dmarc=none
  action=none header.from=example.com;
From: sender @ example.com
To: receiver @ contoso.com
```
<span data-ttu-id="fd2dd-218">스푸핑 방지 후 Office 365 Enterprise E5, EOP 또는 ATP를 사용하는 경우 compauth 값이 스탬핑 처리됩니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-218">After anti-spoofing, if you have Office 365 Enterprise E5, EOP, or ATP, the compauth value is stamped:</span></span>
  
```
Authentication-Results: spf=none (sender IP is 1.2.3.4)
  smtp.mailfrom=example.com; contoso.com; dkim=none
  (message not signed) header.d=none; contoso.com; dmarc=none
  action=none header.from=example.com; compauth=fail reason=001
From: sender @ example.com
To: receiver @ contoso.com

```

<span data-ttu-id="fd2dd-219">example.com이 SPF 레코드는 설정하고 DKIM 레코드를 설정하지 않은 채 이 문제를 해결한 경우, SPF를 통과한 도메인이 보낸 사람 : 주소의 도메인과 일치하기 때문에 복합 인증이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-219">If example.com fixed this by setting up an SPF record but not a DKIM record, this would pass composite authentication because the domain that passed SPF aligned with the domain in the From: address:</span></span> 
  
```
Authentication-Results: spf=pass (sender IP is 1.2.3.4)
  smtp.mailfrom=example.com; contoso.com; dkim=none
  (message not signed) header.d=none; contoso.com; dmarc=bestguesspass
  action=none header.from=example.com; compauth=pass reason=109
From: sender @ example.com
To: receiver @ contoso.com
```

<span data-ttu-id="fd2dd-220">또는 SPF 레코드가 아닌 DKIM 레코드를 설정하는 경우 전달된 DKIM-서명의 도메인이 보낸 사람: 주소의 도메인과 일치하기 때문에 복합 인증을 통과합니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-220">Or, if they set up a DKIM record but not an SPF record, this would also pass composite authentication because the domain in the DKIM-Signature that passed aligned with the domain in the From: address:</span></span> 
  
```
Authentication-Results: spf=none (sender IP is 1.2.3.4)
  smtp.mailfrom=example.com; contoso.com; dkim=pass
  (signature was verified) header.d=outbound.example.com;
  contoso.com; dmarc=bestguesspass action=none
  header.from=example.com; compauth=pass reason=109
From: sender @ example.com
To: receiver @ contoso.com
```

<span data-ttu-id="fd2dd-221">그러나 피셔는 SPF 및 DKIM을 설치하고 자체 도메인으로 메시지에 서명하지만 보낸 사람: 주소에서는 다른 도메인을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-221">However, a phisher may also set up SPF and DKIM and sign the message with their own domain, but specify a different domain in the From: address.</span></span> <span data-ttu-id="fd2dd-222">SPF나 DKIM 모두 보낸 사람: 주소에서 도메인을 정렬할 필요가 없으므로, example.com이 DMARC 레코드를 게시하지 않으면 이는  DMARC를 사용하여 스푸핑으로 표시되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-222">Neither SPF nor DKIM requires the domain to align with the domain in the From: address, so unless example.com published DMARC records, this would not be marked as a spoof using DMARC:</span></span> 
  
```
Authentication-Results: spf=pass (sender IP is 5.6.7.8)
  smtp.mailfrom=maliciousDomain.com; contoso.com; dkim=pass
  (signature was verified) header.d=maliciousDomain.com;
  contoso.com; dmarc=none action=none header.from=example.com;
From: sender @ example.com
To: receiver @ contoso.com
```

<span data-ttu-id="fd2dd-223">전자 메일 클라이언트 (Outlook, 웹상의 Outlook 또는 기타 전자 메일 클라이언트)에서는 SPF 또는 DKIM의 도메인이 아닌 보낸 사람: 도메인만 표시되며, 이는 메시지가 실제로는 maliciousDomain.com에서 왔지만 사용자는 메시지가 example.com에서 왔다고 착각하도록 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-223">In the email client (Outlook, Outlook on the web, or any other email client), only the From: domain is displayed, not the domain in the SPF or DKIM, and that can mislead the user into thinking the message came from example.com, but actually came from maliciousDomain.com.</span></span>
  
![인증된 메시지이지만 보낸 사람: 도메인이 SPF 또는 DKIM을 통과한 것과 일치하지 않습니다.](media/a9b5ab2a-dfd3-47c6-8ee8-e3dab2fae528.jpg)
  
<span data-ttu-id="fd2dd-225">따라서 Office 365에서는 보낸 사람: 주소의 도메인이 SPF 또는 DKIM 서명의 도메인과 일치해야 하며 그렇지 않은 경우 메시지가 합법적임을 나타내는 다른 내부 신호가 포함되어 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-225">For that reason, Office 365 requires that the domain in the From: address aligns with the domain in the SPF or DKIM signature, and if it doesn't, contains some other internal signals that indicates that the message is legitimate.</span></span> <span data-ttu-id="fd2dd-226">그렇지 않으면 메시지는 compauth 실패가 될 것입니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-226">Otherwise, the message would be a compauth fail.</span></span> 
  
```
Authentication-Results: spf=none (sender IP is 5.6.7.8)
  smtp.mailfrom=maliciousDomain.com; contoso.com; dkim=pass
  (signature was verified) header.d=maliciousDomain.com;
  contoso.com; dmarc=none action=none header.from=contoso.com;
  compauth=fail reason=001
From: sender@contoso.com
To: someone@example.com
```

<span data-ttu-id="fd2dd-227">따라서 Office 365 스푸핑 방지는 인증이 없는 도메인과 인증을 설정하지만 보낸 사람: 주소에서 사용자가 메시지의 보낸 사람이라고 보고 믿는 내용과 일치하지 않는 도메인으로부터 보호합니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-227">Thus, Office 365 anti-spoofing protects against domains with no authentication, and against domains who set up authentication but mismatch against the domain in the From: address as that is the one that the user sees and believes is the sender of the message.</span></span> <span data-ttu-id="fd2dd-228">이는 조직 외부의 도메인과 조직 내의 도메인에 모두 해당됩니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-228">This is true both of domains external to your organization, as well as domains within your organization.</span></span>
  
<span data-ttu-id="fd2dd-229">따라서 만약 메시지가 SPF와 DKIM을 통과하더라도 복합 인증에 실패하고 스푸핑된 것으로 표시된 수신했다면 이는 SPF와 DKIM을 통과한 도메인이 보낸 사람: 주소의 도메인과 정렬되지 않았기 때문입니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-229">Therefore, if you ever receive a message that failed composite authentication and is marked as spoofed, even though the message passed SPF and DKIM, it's because the domain that passed SPF and DKIM are not aligned with the domain in the From: address.</span></span>
  
### <a name="understanding-changes-in-how-spoofed-emails-are-treated"></a><span data-ttu-id="fd2dd-230">스푸핑된 전자 메일을 처리하는 방법의 변경 내용 이해</span><span class="sxs-lookup"><span data-stu-id="fd2dd-230">Understanding changes in how spoofed emails are treated</span></span>

<span data-ttu-id="fd2dd-231">현재 Office 365-ATP 및 비 ATP의 모든 조직에 대해 거부 또는 격리 정책으로 DMARC에 실패한 메시지는 스팸으로 표시되고, 일반적으로 높은 신뢰도의 스팸 작업 또는 때로는 일반적인 스팸 작업을 받게 됩니다(다른 스팸 규칙이 이를 먼저 스팸을 파악하는지에 따라).</span><span class="sxs-lookup"><span data-stu-id="fd2dd-231">Currently, for all organizations in Office 365 - ATP and non-ATP - messages that fail DMARC with a policy of reject or quarantine are marked as spam and usually take the high confidence spam action, or sometimes the regular spam action (depending on whether other spam rules first identify it as spam).</span></span> <span data-ttu-id="fd2dd-232">조직 내 스푸핑 탐지는 일반적인 스팸 조치를 취합니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-232">Intra-org spoof detections take the regular spam action.</span></span> <span data-ttu-id="fd2dd-233">이 동작은 활성화할 필요가 없으며 비활성화할 수도 없습니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-233">This behavior does not need to be enabled, nor can it be disabled.</span></span>
  
<span data-ttu-id="fd2dd-234">그러나 도메인 간 스푸핑 메시지의 경우 이 변경 전에 정기적인 스팸, 피싱 및 맬웨어 검사를 수행하고, 필터의 다른 부분에서 의심스러운 것으로 확인되면 스팸, 피싱 또는 맬웨어로 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-234">However, for cross-domain spoofing messages, before this change they would go through regular spam, phish, and malware checks and if other parts of the filter identified them as suspicious, would mark them as spam, phish, or malware respectively.</span></span> <span data-ttu-id="fd2dd-235">새로운 도메인 간 스푸핑 보호 기능을 사용하면 인증할 수 없는 메시지는 기본적으로 안티 피싱 \>안티 스푸핑 정책에 정의된 작업을 수행합니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-235">With the new cross-domain spoofing protection, any message that can't be authenticated will, by default, take the action defined in the Anti-phishing \> Anti-spoofing policy.</span></span> <span data-ttu-id="fd2dd-236">정의되지 않은 경우 사용자 정크 메일 폴더로 이동됩니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-236">If one is not defined, it will be moved to a users Junk Email folder.</span></span> <span data-ttu-id="fd2dd-237">경우에 따라, 더 의심스러운 메시지는 메시지에 빨간색 보안 팁이 추가됩니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-237">In some cases, more suspicious messages will also have the red safety tip added to the message.</span></span>
  
<span data-ttu-id="fd2dd-238">이로 인해 이전에 스팸으로 표시되었던 일부 메시지가 여전히 스팸으로 표시되지만, 이제는 빨간색 보안 팁도 함께 표시됩니다. 그 외의 경우에는 이전에 스팸이 아닌 것으로 표시된 메시지에 빨간색 안전 팁이 추가된 스팸(CAT : SPOOF)으로 표시되기 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-238">This may result in some messages that were previously marked as spam still getting marked as spam but will now also have a red safety tip; in other cases, messages that were previously marked as non-spam will start getting marked as spam (CAT:SPOOF) with a red safety tip added.</span></span> <span data-ttu-id="fd2dd-239">이 밖의 경우에는 스팸 및 피싱을 격리 저장소로 옮기는 고객이 스팸 메일 폴더로 이동하는 모습을 보게 될 것입니다(이 작업은 변경될 수 있습니다. [스푸핑 방지 설정 변경](#changing-your-anti-spoofing-settings)을 참조하십시오).</span><span class="sxs-lookup"><span data-stu-id="fd2dd-239">In still other cases, customers that were moving all spam and phish to the quarantine would now see them going to the Junk Mail Folder (this behavior can be changed, see [Changing your anti-spoofing settings](#changing-your-anti-spoofing-settings)).</span></span>
  
<span data-ttu-id="fd2dd-240">메시지를 스푸핑할 수 방법은 매우 다양합니다(이 문서 앞부분의 [여러 가지 유형의 스푸핑 구분](#differentiating-between-different-types-of-spoofing) 참조). 그러나 Office 365에서 이러한 메시지를 처리하는 방식은 아직 통합되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-240">There are multiple different ways a message can be spoofed (see  [Differentiating between different types of spoofing](#differentiating-between-different-types-of-spoofing) earlier in this article) but as of March 2018 the way Office 365 treats these messages is not yet unified.</span></span> <span data-ttu-id="fd2dd-241">다음 표에서 새로운 작업인 도메인 간 스푸핑 보호 기능이 포함된 간략한 요약본을 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-241">The following table is a quick summary, with Cross-domain spoofing protection being new behavior:</span></span> 
  
|<span data-ttu-id="fd2dd-242">**스푸핑 유형**</span><span class="sxs-lookup"><span data-stu-id="fd2dd-242">**Type of spoof**</span></span>|<span data-ttu-id="fd2dd-243">**범주**</span><span class="sxs-lookup"><span data-stu-id="fd2dd-243">**Category**</span></span>|<span data-ttu-id="fd2dd-244">**안전 팁 추가?**</span><span class="sxs-lookup"><span data-stu-id="fd2dd-244">**Safety tip added?**</span></span>|<span data-ttu-id="fd2dd-245">**적용 대상**</span><span class="sxs-lookup"><span data-stu-id="fd2dd-245">**Applies to**</span></span>|
|:-----|:-----|:-----|:-----|
|<span data-ttu-id="fd2dd-246">DMARC 실패(격리 또는 거부)</span><span class="sxs-lookup"><span data-stu-id="fd2dd-246">DMARC fail (quarantine or reject)</span></span>  <br/> |<span data-ttu-id="fd2dd-247">HSPM(기본)도 SPM 또는 PHSH일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-247">HSPM (default), may also be SPM or PHSH</span></span>  <br/> |<span data-ttu-id="fd2dd-248">아니오(아직 아님)</span><span class="sxs-lookup"><span data-stu-id="fd2dd-248">No (not yet)</span></span>  <br/> |<span data-ttu-id="fd2dd-249">모든 Office 365 고객, Outlook.com</span><span class="sxs-lookup"><span data-stu-id="fd2dd-249">All Office 365 customers, Outlook.com</span></span>  <br/> |
|<span data-ttu-id="fd2dd-250">자체</span><span class="sxs-lookup"><span data-stu-id="fd2dd-250">Self-to-self</span></span>  <br/> |<span data-ttu-id="fd2dd-251">SPM</span><span class="sxs-lookup"><span data-stu-id="fd2dd-251">SPM</span></span>  <br/> |<span data-ttu-id="fd2dd-252">예</span><span class="sxs-lookup"><span data-stu-id="fd2dd-252">Yes</span></span>  <br/> |<span data-ttu-id="fd2dd-253">모든 Office 365 조직, Outlook.com</span><span class="sxs-lookup"><span data-stu-id="fd2dd-253">All Office 365 organizations, Outlook.com</span></span>  <br/> |
|<span data-ttu-id="fd2dd-254">도메인 간</span><span class="sxs-lookup"><span data-stu-id="fd2dd-254">Cross-domain</span></span>  <br/> |<span data-ttu-id="fd2dd-255">스푸핑</span><span class="sxs-lookup"><span data-stu-id="fd2dd-255">SPOOF</span></span>  <br/> |<span data-ttu-id="fd2dd-256">예</span><span class="sxs-lookup"><span data-stu-id="fd2dd-256">Yes</span></span>  <br/> |<span data-ttu-id="fd2dd-257">Office 365 고급 위협 보호 기능 및 E5 고객</span><span class="sxs-lookup"><span data-stu-id="fd2dd-257">Office 365 Advanced Threat Protection and E5 customers</span></span>  <br/> |

### <a name="changing-your-anti-spoofing-settings"></a><span data-ttu-id="fd2dd-258">스푸핑 방지 설정 변경</span><span class="sxs-lookup"><span data-stu-id="fd2dd-258">Changing your anti-spoofing settings</span></span>

<span data-ttu-id="fd2dd-259">(도메인 간) 스푸핑 방지 설정을 만들거나 업데이트하려면 보안 &amp; 준수 센터의 위협 관리 \> 정책 탭에서 스팸 방지 \> 스푸핑 방지 설정으로 이동하십시오.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-259">To create or update your (cross-domain) anti-spoofing settings, navigate to the Anti-phishing \> Anti-spoofing settings under the Threat Management \> Policy tab in the Security &amp; Compliance Center.</span></span> <span data-ttu-id="fd2dd-260">피싱 방지 설정을 생성한 적이 없다면 다음 중 하나를 만들어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-260">If you have never created any anti-phishing settings, you will need to create one:</span></span>
  
![피싱 방지 - 새 정책 생성](media/9337ec91-270e-4fa7-9dfa-a51a2d1eb95e.jpg)
  
<span data-ttu-id="fd2dd-262">이전에 설정을 생성한 적이 있다면, 이를 선택하여 수정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-262">If you've already created one, you can select it to modify it:</span></span>
  
![피싱 방지 - 기존 정책 수정](media/75457a7c-882e-4984-80d1-21a12b42c53a.jpg)
  
<span data-ttu-id="fd2dd-264">방금 만든 정책을 선택하고 [스푸핑 인텔리전스에 대해 자세히 알아보기](learn-about-spoof-intelligence.md)에서 설명된 단계를 따라 진행합니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-264">Select the policy you just created and proceed through the steps as described in [Learn more about spoof intelligence](learn-about-spoof-intelligence.md).</span></span>
  
![스푸핑 방지 사용 또는 사용 안 함](media/c49e2147-c954-443c-9144-1cbd139e1166.jpg)
  
![스푸핑 방지 안전 팁 사용 또는 사용 안 함](media/eec7c407-31fc-4f73-8325-307d82d1fb53.jpg)
  
<span data-ttu-id="fd2dd-267">PowerShell을 사용하여 새로운 정책 생성하기:</span><span class="sxs-lookup"><span data-stu-id="fd2dd-267">To create a new policy by using PowerShell:</span></span> 
  
```powershell
$org = Get-OrganizationConfig
$name = "My first anti-phishing policy for " + $org.Name
# Note: The name should not exclude 64 characters, including spaces.
# If it does, you will need to pick a smaller name.
# Next, create a new anti-phishing policy with the default values
New-AntiphishPolicy -Name $Name
# Select the domains to scope it to
# Multiple domains are specified in a comma-separated list
$domains = "domain1.com, domain2.com, domain3.com"
# Next, create the anti-phishing rule, scope it to the anti-phishing rule
New-AntiphishRule -Name $name -AntiphishPolicy $name -RecipientDomainIs $domains
```

<span data-ttu-id="fd2dd-268">그 다음 [설정-AntiphishPolicy](https://docs.microsoft.com/powershell/module/exchange/advanced-threat-protection/Set-AntiPhishPolicy?view=exchange-ps)의 설명서에 따라 PowerShell을 사용하여 피싱 방지 정책 매개 변수를 수정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-268">You may then modify the anti-phishing policy parameters using PowerShell, following the documentation at [Set-AntiphishPolicy](https://docs.microsoft.com/powershell/module/exchange/advanced-threat-protection/Set-AntiPhishPolicy?view=exchange-ps).</span></span> <span data-ttu-id="fd2dd-269">$name을 매개 변수로 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-269">You may specify the $name as a parameter:</span></span>
  
```powershell
Set-AntiphishPolicy -Identity $name <fill in rest of parameters>
```

<span data-ttu-id="fd2dd-270">향후 2018년에 기본 정책을 만드는 대신 조직의 모든 수신자에게 적용되는 정책이 만들어질 예정이므로 수동으로 지정하지 않아도 됩니다 (아래 스크린 샷은 최종 구현 전에 변경 될 수 있습니다).</span><span class="sxs-lookup"><span data-stu-id="fd2dd-270">Later in 2018, rather than you having to create a default policy, one will be created for you that is scoped to all the recipients in your organization so you don't have to specify it manually (the screenshots below are subject to change before the final implementation).</span></span>
  
![피싱 방지에 대한 기본 정책](media/1f27a0bf-e202-4e12-bbac-24baf013c8f9.jpg)
  
<span data-ttu-id="fd2dd-272">사용자가 생성하는 정책과 달리 기본 정책을 삭제하거나 우선 순위를 수정하거나 범위를 지정할 사용자, 도메인 또는 그룹을 선택할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-272">Unlike a policy that you create, you cannot delete the default policy, modify its priority, or choose which users, domains, or groups to scope it to.</span></span>
  
![피싱 방지 기본 정책 세부 정보](media/30c21ceb-df52-4c93-aa65-f44a55dc1009.jpg)
  
<span data-ttu-id="fd2dd-274">PowerShell을 사용하여 기본 보호 설정하기:</span><span class="sxs-lookup"><span data-stu-id="fd2dd-274">To set up your default protection by using PowerShell:</span></span>
  
```powershell
$defaultAntiphishPolicy = Get-AntiphishPolicy | ? {$_.IsDefault -eq $true}
Set-AntiphishPolicy -Identity $defaultAntiphishPolicy.Name -EnableAntispoofEnforcement <$true|$false>
```

<span data-ttu-id="fd2dd-275">Office 365 앞에 다른 메일 서버가 있는 경우에만 스푸핑 방지 보호를 해제해야 합니다(자세한 내용은 스푸핑 방지를 해제하기 위한 합법적인 시나리오를 참조하십시오).</span><span class="sxs-lookup"><span data-stu-id="fd2dd-275">You should only disable anti-spoofing protection if you have another mail server or servers in front of Office 365 (see Legitimate scenarios to disable anti-spoofing for more details).</span></span>
  
```powershell
$defaultAntiphishPolicy = Get-AntiphishiPolicy | ? {$_.IsDefault $true}
Set-AntiphishPolicy -Identity $defaultAntiphishPolicy.Name -EnableAntispoofEnforcement $false 

```
> [!IMPORTANT]
> <span data-ttu-id="fd2dd-276">전자 메일 경로의 첫 번째 홉이 Office 365이고 합법적인 전자 메일이 너무 많이 스푸핑으로 표시된 경우에는 먼저 스푸핑된 전자 메일을 도메인에 보낼 수있는 보낸 사람을 설정해야 합니다(*"인증되지 않은 전자 메일을 보내는 합법적인 보낸 사람 관리하기"* 섹션을 참조하십시오).</span><span class="sxs-lookup"><span data-stu-id="fd2dd-276">If the first hop in your email path is Office 365, and you are getting too many legitimate emails marked as spoof, you should first set up your senders that are allowed to send spoofed email to your domain (see the section  *"Managing legitimate senders who are sending unauthenticated email"*  ).</span></span> <span data-ttu-id="fd2dd-277">여전히 너무 많은 오탐지가 발생하는 경우(즉, 스팸으로 분류된 합법적인 메시지가 너무 많은 경우), 스푸핑 방지 기능을 해제하지 않는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-277">If you are still getting too many false positives (that is, legitimate messages marked as spoof), we do NOT recommend disabling anti-spoofing protection altogether.</span></span> <span data-ttu-id="fd2dd-278">대신 높은 수준의 보호 대신 기본을 선택하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-278">Instead, we recommend choosing Basic instead of High protection.</span></span> <span data-ttu-id="fd2dd-279">조직을 스푸핑된 전자 메일에 노출시켜 장기적으로 훨씬 높은 비용을 부담하는 것보다 오탐지를 이용하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-279">It is better to work through false positives than to expose your organization to spoofed email which could end up imposing significantly higher costs in the long term.</span></span>

### <a name="managing-legitimate-senders-who-are-sending-unauthenticated-email"></a><span data-ttu-id="fd2dd-280">인증되지 않은 이메일을 보내는 합법적인 보낸 사람 관리</span><span class="sxs-lookup"><span data-stu-id="fd2dd-280">Managing legitimate senders who are sending unauthenticated email</span></span>

<span data-ttu-id="fd2dd-281">Office 365는 조직에 인증되지 않은 전자 메일을 보내는 사람을 추적합니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-281">Office 365 keeps track of who is sending unauthenticated email to your organization.</span></span> <span data-ttu-id="fd2dd-282">서비스가 보낸 사람이 합법적이지 않다고 생각하면 *compauth* 실패로 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-282">If the service thinks the sender is not legitimate, it will mark it as a *compauth* failure.</span></span> <span data-ttu-id="fd2dd-283">메시지에 적용된 스푸핑 방지 정책에 따라 다르지만 이는 SPOOF로 분류될 것입니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-283">This will be classified as SPOOF although it depends on your anti-spoofing policy that was applied to the message.</span></span>
  
<span data-ttu-id="fd2dd-284">그러나 관리자는 Office 365의 결정을 번복하여 스푸핑 된 전자 메일을 보낼 수 있는 보낸 사람을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-284">However, as an administrator, you can specify which senders are permitted to send spoofed email, overriding Office 365's decision.</span></span>
  
<span data-ttu-id="fd2dd-285">\*\*방법 1 - 조직에서 도메인을 소유한 경우 전자 메일 인증 \*\*을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-285">**Method 1 - If your organization owns the domain, set up email authentication**</span></span>
  
<span data-ttu-id="fd2dd-286">이 방법은 여러 명의 테넌트를 소유하거나 이들과 상호 작용하는 경우 조직 내 스푸핑 및 도메인 간 스푸핑 문제를 해결하는 데 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-286">This method can be used to resolve intra-org spoofing, and cross-domain spoofing in cases where you own or interact with multiple tenants.</span></span> <span data-ttu-id="fd2dd-287">또한 사용자가 Office 365 내의 다른 고객과 다른 공급업체에서 호스팅되는 타사에게 보내는 도메인 간 스푸핑 문제를 해결할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-287">It also helps resolve cross-domain spoofing where you send to other customers within Office 365, and also third parties that are hosted in other providers.</span></span>
  
<span data-ttu-id="fd2dd-288">자세한 내용은 [Office 365 고객](#customers-of-office-365)을 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-288">For more details, see [Customers of Office 365](#customers-of-office-365).</span></span>

<span data-ttu-id="fd2dd-289">**방법 2 - 스푸핑 인텔리전스를 사용하여 인증되지 않은 이메일의 허용된 보낸 사람 구성**</span><span class="sxs-lookup"><span data-stu-id="fd2dd-289">**Method 2 - Use Spoof intelligence to configure permitted senders of unauthenticated email**</span></span>
  
<span data-ttu-id="fd2dd-290">또한 [스푸핑 인텔리전스](https://support.office.com/article/Learn-more-about-spoof-intelligence-978c3173-3578-4286-aaf4-8a10951978bf)를 사용하여 보낸 사람이 인증되지 않은 메시지를 조직에 전송하도록 허용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-290">You can also use [Spoof Intelligence](https://support.office.com/article/Learn-more-about-spoof-intelligence-978c3173-3578-4286-aaf4-8a10951978bf) to permit senders to transmit unauthenticated messages to your organization.</span></span> 
  
<span data-ttu-id="fd2dd-291">외부 도메인의 경우 스푸핑 된 사용자는 보낸 사람 주소의 도메인이고 보내는 인프라는 보내는 IP 주 (/24 CIDR 범위로 나눈 값) 또는 PTR 레코드의 조직 도메인입니다 (아래 스크린 샷에서 보내는 IP는 PTR 레코드가 outbound.mail.protection.outlook.com인 131.107.18.4일 수 있으며, 보내는 인프라의 경우 outlook.com으로 표시됩니다).</span><span class="sxs-lookup"><span data-stu-id="fd2dd-291">For external domains, the spoofed user is the domain in the From address, while the sending infrastructure is either the sending IP address (divided up into /24 CIDR ranges), or the organizational domain of the PTR record (in the screenshot below, the sending IP might be 131.107.18.4 whose PTR record is outbound.mail.protection.outlook.com, and this would show up as outlook.com for the sending infrastructure).</span></span>
  
<span data-ttu-id="fd2dd-292">이 보낸 사람이 인증되지 않은 전자 메일을 보낼 수 있도록 허용하려면 **아니요**를 **예**로 변경하십시오.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-292">To permit this sender to send unauthenticated email, change the **No** to a **Yes**.</span></span>
  
![스푸핑 방지 허용된 보낸 사람 설정](media/d4334921-d820-4334-8217-788279701e94.jpg)
  
<span data-ttu-id="fd2dd-294">PowerShell을 사용하여 특정 보낸 사람이 도메인을 스푸핑하도록 허용할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-294">You can also use PowerShell to allow specific sender to spoof your domain:</span></span>
  
```powershell
$file = "C:\My Documents\Summary Spoofed Internal Domains and Senders.csv"
```

```powershell
Get-PhishFilterPolicy -Detailed -SpoofAllowBlockList -SpoofType External | Export-CSV $file
```

![Powershell에서 스푸핑된 보낸 사람 받기](media/0e27ffcf-a5db-4c43-a19b-fa62326d5118.jpg)
  
<span data-ttu-id="fd2dd-296">이전 이미지에서는 이 스크린 샷을 맞추기 위해 추가 줄 바꿈이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-296">In the previous image, additional line breaks have been added to make this screenshot fit.</span></span> <span data-ttu-id="fd2dd-297">일반적으로 모든 값은 한 줄에 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-297">Normally, all the values would appear on a single line.</span></span>
  
<span data-ttu-id="fd2dd-298">파일을 편집하고 outlook.com 및 bing.com에 해당하는 줄을 찾은 다음 AllowedToSpoof 항목을 아니요에서 예로 변경하십시오.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-298">Edit the file and look for the line that corresponds to outlook.com and bing.com, and change the AllowedToSpoof entry from No to Yes:</span></span>
  
![Powershell에서 스푸핑 허용용을 "예"로 설정](media/62340452-62d3-4958-9ce9-afe5275a870d.jpg)
  
<span data-ttu-id="fd2dd-300">파일을 저장하고 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-300">Save the file, and then run:</span></span>
  
```powershell
$UpdateSpoofedSenders = Get-Content -Raw "C:\My Documents\Spoofed Senders.csv"
Set-PhishFilterPolicy -Identity Default -SpoofAllowBlockList $UpdateSpoofedSenders
```

<span data-ttu-id="fd2dd-301">이제 bing.com이 \* .outlook.com에서 인증되지 않은 이메일을 보낼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-301">This will now allow bing.com to send unauthenticated email from \*.outlook.com.</span></span>

<span data-ttu-id="fd2dd-302">**방법 3 - 보낸 사람/받는 사람 쌍에 대한 허용 항목 만들기**</span><span class="sxs-lookup"><span data-stu-id="fd2dd-302">**Method 3 - Create an allow entry for the sender/recipient pair**</span></span>
  
<span data-ttu-id="fd2dd-303">특정 보낸 사람에 대해 모든 스팸 필터링을 우회하도록 선택할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-303">You can also choose to bypass all spam filtering for a particular sender.</span></span> <span data-ttu-id="fd2dd-304">자세한 내용은 [Office 365 의 허용 목록에 보낸 사람을 안전하게 추가하는 방법](https://blogs.msdn.microsoft.com/tzink/2017/11/29/how-to-securely-add-a-sender-to-an-allow-list-in-office-365/)을 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-304">For more details, see [How to securely add a sender to an allow list in Office 365](https://blogs.msdn.microsoft.com/tzink/2017/11/29/how-to-securely-add-a-sender-to-an-allow-list-in-office-365/).</span></span>
  
<span data-ttu-id="fd2dd-305">이 방법을 사용하면 스팸 및 일부 피싱 필터링(맬웨어 필터링 제외)을 건너 뜁니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-305">If you use this method, it will skip spam and some of the phish filtering, but not malware filtering.</span></span>
  
<span data-ttu-id="fd2dd-306">**방법 4 - 보낸 사람에게 연락하여 전자 메일 인증을 설정하도록 요청**</span><span class="sxs-lookup"><span data-stu-id="fd2dd-306">**Method 4 - Contact the sender and ask them to set up email authentication**</span></span>
  
<span data-ttu-id="fd2dd-307">스팸 및 피싱의 문제 때문에 보낸 사람이 모두 전자 메일 인증을 설정하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-307">Because of the problem of spam and phishing, Microsoft recommends all senders set up email authentication.</span></span> <span data-ttu-id="fd2dd-308">보내는 도메인의 관리자를 알고 있는 경우 전자 메일 인증 레코드를 설정하도록 요청하여 재정의를 추가할 필요가 없도록 하십시오.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-308">If you know an administrator of the sending domain, contact them and request that they set up email authentication records so you do not have to add any overrides.</span></span> <span data-ttu-id="fd2dd-309">자세한 내용은 이 문서 뒷부분의 [Office 365 고객이 아닌 도메인 관리자](#administrators-of-domains-that-are-not-office-365-customers)"를 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-309">For more information, see [Administrators of domains that are not Office 365 customers](#administrators-of-domains-that-are-not-office-365-customers)" later in this article.</span></span> 
  
<span data-ttu-id="fd2dd-310">처음에는 도메인을 인증 받기가 어려울 수 있지만 시간이 지남에 따라 더 많은 이메일 필터가 정킹 또는 전자 메일 거부를 시작하면 더 나은 전달을 보장하기 위해 적절한 레코드를 설정하게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-310">While it may be difficult at first to get sending domains to authenticate, over time, as more and more email filters start junking or even rejecting their email, it will cause them to set up the proper records to ensure better delivery.</span></span>
  
### <a name="viewing-reports-of-how-many-messages-were-marked-as-spoofed"></a><span data-ttu-id="fd2dd-311">스푸핑으로 표시된 메시지 수에 대한 보고서 보기</span><span class="sxs-lookup"><span data-stu-id="fd2dd-311">Viewing reports of how many messages were marked as spoofed</span></span>

<span data-ttu-id="fd2dd-312">스푸핑 방지 정책을 사용하면 위협 조사 및 응답 기능을 사용하여 피싱으로 표시된 메시지 수에 대한 정보를 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-312">Once your anti-spoofing policy is enabled, you can use threat investigation and response capabilities to get numbers around how many messages are marked as phish.</span></span> <span data-ttu-id="fd2dd-313">이렇게 하려면 위협 관리 \> 탐색기 아래의 보안 &amp; 준수 센터(SCC)로 가서 피싱으로보기를 설정하고 보낸 사람 도메인 또는 보호 상태별로 그룹화합니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-313">To do this, go into the Security &amp; Compliance Center (SCC) under Threat Management \> Explorer, set the View to Phish, and group by Sender Domain or Protection Status:</span></span>
  
![피싱으로 표시된 메시지 수 보기](media/de25009a-44d4-4c5f-94ba-9c75cd9c64b3.jpg)
  
<span data-ttu-id="fd2dd-315">다양한 보고서와 상호 작용하여 스푸핑으로 표시된 메시지 등 피싱으로 표시된 수를 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-315">You can interact with the various reports to see how many were marked as phishing, including messages marked as SPOOF.</span></span> <span data-ttu-id="fd2dd-316">자세한 내용은 [Office 365 위협 조사 및 응답 시작하기](get-started-with-ti.md)를 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-316">To learn more, see [Get started with Office 365 Threat investigation and response](get-started-with-ti.md).</span></span>
  
<span data-ttu-id="fd2dd-317">다른 유형의 피싱(일반 피싱, 도메인 또는 사용자 가장 등)과 달리 스푸핑으로 인해 표시된 메시지를 아직 분리할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-317">You can't yet split out which messages were marked due to spoofing as opposed to other types of phishing (general phishing, domain or user impersonation, and so on).</span></span> <span data-ttu-id="fd2dd-318">그러나 나중에 보안 &amp; 준수 센터를 통해 이 작업을 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-318">However, later, you will be able to do this through the Security &amp; Compliance Center.</span></span> <span data-ttu-id="fd2dd-319">일단 이 보고서를 사용하면 실패한 인증으로 인해 스푸핑으로 표시되는 합법적인 보내는 도메인을 식별할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-319">Once you do, you can use this report as a starting place to identify sending domains that may be legitimate that are being marked as spoof due to failing authentication.</span></span>
  
<span data-ttu-id="fd2dd-320">다음 스크린 샷은 이 데이터의 형태에 대한 제안이지만 릴리스될 때에는 변경될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-320">The following screenshot is a proposal for how this data will look, but may change when released:</span></span>
  
![탐지 유형별 피싱 보고서 보기](media/dd25d63f-152c-4c55-a07b-184ecda2de81.jpg)
  
<span data-ttu-id="fd2dd-322">비 ATP 및 E5 고객의 경우, 이 보고서는 나중에 Threat Protection Status(TPS) 보고서에서 볼 수 있지만 최소 24시간이 지연됩니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-322">For non-ATP and E5 customers, these reports will be available later under the Threat Protection Status (TPS) reports, but will be delayed by at least 24 hours.</span></span> <span data-ttu-id="fd2dd-323">이 페이지는 보안 &amp; 준수 센터에 통합되어 업데이트됩니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-323">This page will be updated as they are integrated into the Security &amp; Compliance Center.</span></span>
  
### <a name="predicting-how-many-messages-will-be-marked-as-spoof"></a><span data-ttu-id="fd2dd-324">얼마나 많은 메시지가 스푸핑으로 표시될지 예측</span><span class="sxs-lookup"><span data-stu-id="fd2dd-324">Predicting how many messages will be marked as spoof</span></span>

<span data-ttu-id="fd2dd-325">Office 365에서 스푸핑 방지 적용을 해제하거나 기본 또는 높음 적용으로 설정을 업데이트하면 다양한 설정에서 메시지 처리 방식이 어떻게 변경되는지 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-325">Once Office 365 updates its settings to let you turn the anti-spoofing enforcement Off, or on with Basic or High enforcement, you will be given the ability to see how message disposition will change at the various settings.</span></span> <span data-ttu-id="fd2dd-326">즉, 스푸핑 방지가 해제되어 있을 경우 기본으로 전환하면 스푸핑으로 탐지될 메시지 수를 확인할 수 있습니다. 기본 설정인 경우 이를 높음으로 바꾸면 얼마나 많은 메시지가 스푸핑으로 탐지될지 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-326">That is, if anti-spoofing is Off, you will be able to see how many messages will be detected as Spoof if you turn to Basic; or, if it's Basic, you will be able to see how many more messages will be detected as Spoof if you turn it to High.</span></span>
  
<span data-ttu-id="fd2dd-327">이 기능은 현재 개발 중입니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-327">This feature is currently under development.</span></span> <span data-ttu-id="fd2dd-328">자세한 내용이 정의되면 이 페이지는 보안 및 규정 준수 센터의 스크린 샷과 PowerShell 예제로 업데이트됩니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-328">As more details are defined, this page will be updated both with screenshots of the Security and Compliance Center, and with PowerShell examples.</span></span>
  
![스푸핑 방지를 사용하기 위한 "What If" 보고서](media/fdd085ae-02c1-4327-a063-bfe9a32ff1eb.jpg)
  
![스푸핑된 보낸 사람을 허용하는 UX](media/53f9f73e-fb01-47f3-9a6d-850c1aef5efe.jpg)
  
### <a name="legitimate-scenarios-to-disable-anti-spoofing"></a><span data-ttu-id="fd2dd-331">스푸핑 방지를 사용하지 않도록 설정하는 합법적인 시나리오</span><span class="sxs-lookup"><span data-stu-id="fd2dd-331">Legitimate scenarios to disable anti-spoofing</span></span>

<span data-ttu-id="fd2dd-332">스푸핑 방지는 피싱 공격으로부터 고객을 더욱 효과적으로 보호하므로 스푸핑 방지 기능을 해제하지 않는 것이 매우 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-332">Anti-spoofing better protects customers from phishing attacks, and therefore disabling anti-spoofing protection is strongly discouraged.</span></span> <span data-ttu-id="fd2dd-333">이를 사용 중지하면 일부 단기간 오 판정을 해결할 수 있지만 장기적으로 더 많은 위험에 노출됩니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-333">By disabling it, you may resolve some short-term false positives, but long term you will be exposed to more risk.</span></span> <span data-ttu-id="fd2dd-334">발신자 측에서 인증을 설정하거나 피싱 정책을 조정하는 데 드는 비용은 일반적으로 일회성 이벤트이거나 최소한의 주기적인 유지 관리 만 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-334">The cost for setting up authentication on the sender side, or making adjustments in the phishing policies, are usually one-time events or require only minimal, periodic maintenance.</span></span> <span data-ttu-id="fd2dd-335">그러나 데이터가 노출되거나 자산이 손상된 피싱 공격으로부터 복구하는 비용은 훨씬 높습니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-335">However, the cost to recover from a phishing attack where data has been exposed, or assets have been compromised is much higher.</span></span>
  
<span data-ttu-id="fd2dd-336">이러한 이유로 스푸핑 방지를 비활성화하는 것보다 스푸핑 방지 오작동을 통해 작업하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-336">For this reason, it is better to work through anti-spoofing false positives than to disable anti-spoof protection.</span></span>
  
<span data-ttu-id="fd2dd-337">그러나 메시지 스레딩에 추가 메일 필터링 제품이 있고 Office 365가 전자 메일 경로의 첫 번째 홉이 아닌 경우 스푸핑 방지를 해제해야 하는 적법한 시나리오가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-337">However, there is a legitimate scenario where anti-spoofing should be disabled, and that is when there are additional mail-filtering products in the message routing, and Office 365 is not the first hop in the email path:</span></span>
  
![Office 365를 가리키지 않는 고객 MX 레코드](media/62127c16-cfb8-4880-9cad-3c12d827c67e.jpg)
  
<span data-ttu-id="fd2dd-339">다른 서버는 Exchange 온 프레미스 메일 서버, Ironport와 같은 메일 필터링 장치 또는 다른 클라우드 호스팅 서비스일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-339">The other server may be an Exchange on-premises mail server, a mail filtering device such as Ironport, or another cloud hosted service.</span></span>
  
<span data-ttu-id="fd2dd-340">받는 사람 도메인의 MX 레코드가 Office 365를 가리키지 않으면 Office 365가 수신도메인의 MX 레코드를 조회하고 다른 서비스를 가리키는 경우 안티 스푸핑을 억제하므로 이를 해제할 필요가 없습니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-340">If the MX record of the recipient domain does not point to Office 365, then there is no need to disable anti-spoofing because Office 365 looks up your receiving domain's MX record and suppresses anti-spoofing if it points to another service.</span></span> <span data-ttu-id="fd2dd-341">앞쪽에서 도메인에 다른 서버가 있는지 여부를 모르는 경우 MX 도구 상자와 같은 웹 사이트를 사용하여 MX 레코드를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-341">If you don't know if your domain has another server in front, you can use a website like MX Toolbox to look up the MX record.</span></span> <span data-ttu-id="fd2dd-342">그것은 다음과 같이 말할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-342">It might say something like the following:</span></span>
  
![MX 레코드가 도메인이 Office 365를 가리키고 있지 않음을 나타냅니다.](media/d868bb9f-3462-49aa-baea-9447a3ce4877.jpg)
  
<span data-ttu-id="fd2dd-344">이 도메인에는 Office 365를 가리키지 않는 MX 레코드가 있으므로 Office 365는 스푸핑 방지 실행을 적용하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-344">This domain has an MX record that does not point to Office 365, so Office 365 would not apply anti-spoofing enforcement.</span></span>
  
<span data-ttu-id="fd2dd-345">그러나 받는 사람 도메인 \*의 MX 레코드가 Office 365를 가리키는 경우 \*, Office 365 앞에 다른 서비스가 있더라도 스푸핑 방지를 해제해야합니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-345">However, if the MX record of the recipient domain  *does*  point to Office 365, even though there is another service in front of Office 365, then you should disable anti-spoofing.</span></span> <span data-ttu-id="fd2dd-346">가장 일반적인 예는 받는 사람 다시 쓰기를 사용하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-346">The most common example is through the use of a recipient rewrite:</span></span> 
  
![받는 사람 다시 쓰기에 대한 라우팅 다이어그램](media/070d90d1-50a0-42e4-9fd3-920bc99a7cad.jpg)
  
<span data-ttu-id="fd2dd-348">도메인 contoso.com의 MX 레코드는 온 프레미스 서버를 가리키며 도메인 @office365.contoso.net의 MX 레코드는 \* .protection.outlook.com 또는  MX 레코드의 \* .eo.outlook.com를 포함하므로 Office 365를 가리킵니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-348">The domain contoso.com's MX record points to the on-premises server, while the domain @office365.contoso.net's MX record points to Office 365 because it contains \*.protection.outlook.com, or \*.eo.outlook.com in the MX record:</span></span>
  
![MX 레코드가 Office 365를 가리키므로 아마도 받는 사람이 다시 쓰게 됩니다.](media/4101ad51-ef92-4907-b466-b41d14d344ca.jpg)
  
<span data-ttu-id="fd2dd-350">받는 사람 도메인의 MX 레코드가 Office 365를 가리키지 않는 경우와 받는 사람 다시 쓰기를 거친 경우를 구별해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-350">Be sure to differentiate when a recipient domain's MX record does not point to Office 365, and when it has undergone a recipient rewrite.</span></span> <span data-ttu-id="fd2dd-351">이 두 경우의 차이점을 밝히는 것이 중요합니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-351">It is important to tell the difference between these two cases.</span></span>
  
<span data-ttu-id="fd2dd-352">보낸 도메인에서 보낸 사람이 다시 작성되었는지 여부를 잘 모르는 경우 메시지 머리글을 보고 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-352">If you are unsure whether or not your receiving domain has undergone a recipient-rewrite, sometimes you can tell by looking at the message headers.</span></span>
  
<span data-ttu-id="fd2dd-353">a) 먼저, 인증 결과 머리글에서 받는 사람 도메인에 대한 메시지의 머리글을 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-353">a) First, look at the headers in the message for the recipient domain in the Authentication-Results header:</span></span>
  
```
Authentication-Results: spf=fail (sender IP is 1.2.3.4)
  smtp.mailfrom=example.com; office365.contoso.net; dkim=fail
  (body hash did not verify) header.d=simple.example.com;
  office365.contoso.net; dmarc=none action=none
  header.from=example.com; compauth=fail reason=001
```

<span data-ttu-id="fd2dd-354">받는 사람 도메인은 위의 굵은 빨간색 텍스트(이 경우 Office 365.contoso.net)에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-354">The recipient domain is found in the bold red text above, in this case office365.contoso.net.</span></span> <span data-ttu-id="fd2dd-355">이는 받는 사람: 머리글:에 있는 받는 사람과 다를 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-355">This may be different that the recipient in the To: header:</span></span>
  
<span data-ttu-id="fd2dd-356">받는 사람: 받는 사람 \< recipient@contoso.com\></span><span class="sxs-lookup"><span data-stu-id="fd2dd-356">To: Example Recipient \<recipient @ contoso.com\></span></span>
  
<span data-ttu-id="fd2dd-357">실제 받는 사람 도메인의 MX 레코드 조회를 수행합니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-357">Perform an MX-record lookup of the actual recipient domain.</span></span> <span data-ttu-id="fd2dd-358">\*.protection.outlook.com, mail.messaging.microsoft.com, \*.eo.outlook.com 또는 mail.global.frontbridge.com이 포함되어 있으면 MX가 Office 365를 가리키는 것을 의미합니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-358">If it contains \*.protection.outlook.com, mail.messaging.microsoft.com, \*.eo.outlook.com, or mail.global.frontbridge.com, that means that the MX points to Office 365.</span></span>
  
<span data-ttu-id="fd2dd-359">이러한 값이 포함되어 있지 않으면 MX가 Office 365를 가리키지 않는다는 의미입니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-359">If it does not contain those values, then it means that the MX does not point to Office 365.</span></span> <span data-ttu-id="fd2dd-360">이를 확인하는 데 사용할 수있는 도구는 MX 도구 상자입니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-360">One tool you can use to verify this is MX Toolbox.</span></span>
  
<span data-ttu-id="fd2dd-361">이 특정 예제에서 다음은 받는 사람: 머리글이었기 때문에 받는 사람과 비슷한 도메인인 contoso.com이 온 프레미어 서버를 가리키는 MX 레코드 포인트를 가지고 있음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-361">For this particular example, the following says that contoso.com, the domain that looks like the recipient since it was the To: header, has MX record points to an on-prem server:</span></span>
  
![온 프레미스 서버를 가리키는 MX 레코드](media/2444144a-9a90-4319-96b2-d115041f669f.jpg)
  
<span data-ttu-id="fd2dd-363">그러나 실제로 받는 사람은 office365.contoso.net이며 MX 레코드는 Office 365를 가리킵니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-363">However, the actual recipient is office365.contoso.net whose MX record does point to Office 365:</span></span>
  
![MX는 Office 365를 가리키며받는 사람이 다시 작성해야합니다.](media/10cf3245-9b50-475a-b655-d8a51f99d812.jpg)
  
<span data-ttu-id="fd2dd-365">따라서 이 메시지는 받는 사람이 다시 썼을 것으로 추정됩니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-365">Therefore, this message has likely undergone a recipient-rewrite.</span></span>
  
<span data-ttu-id="fd2dd-366">b) 둘째, 받는 사람 재작성의 일반적인 사용 사례를 구분해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-366">b) Second, be sure to distinguish between common use cases of recipient rewrites.</span></span> <span data-ttu-id="fd2dd-367">받는 사람 도메인을 \*.onmicrosoft.com으로 다시 작성하려면 대신 이를 \*.mail.onmicrosoft.com으로 다시 작성하십시오.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-367">If you are going to rewrite the recipient domain to \*.onmicrosoft.com, instead rewrite it to \*.mail.onmicrosoft.com.</span></span>
  
<span data-ttu-id="fd2dd-368">다른 서버 뒤에 라우팅되는 최종 수신자 도메인을 식별하고 받는 사람 도메인의 MX 레코드가 실제로 Office 365를 가리키는 경우(DNS 레코드에 게시된 것처럼) 스푸핑 방지를 해제할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-368">Once you have identified the final recipient domain that is routed behind another server and the recipient domain's MX record actually points to Office 365 (as published in its DNS records), you may proceed to disable anti-spoofing.</span></span>
  
<span data-ttu-id="fd2dd-369">라우팅 경로에서 도메인의 첫 번째 홉이 Office 365인 경우 하나 이상의 서비스 뒤에있을 때에만 스푸핑 방지를 해제하지 않아야 함을 기억하십시오.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-369">Remember, you don't want to disable anti-spoofing if the domain's first hop in the routing path is Office 365, only when it's behind one or more services.</span></span>
  
### <a name="how-to-disable-anti-spoofing"></a><span data-ttu-id="fd2dd-370">스푸핑 방지 해제 방법</span><span class="sxs-lookup"><span data-stu-id="fd2dd-370">How to disable anti-spoofing</span></span>

<span data-ttu-id="fd2dd-371">피싱 방지 정책을 이미 만들었으면 EnableAntispoofEnforcement 매개 변수를 $false로 설정하십시오.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-371">If you already have an Anti-phishing policy created, set the EnableAntispoofEnforcement parameter to $false:</span></span>
  
```
$name = "<name of policy>"
Set-AntiphishPolicy -Identity $name -EnableAntiSpoofEnforcement $false

```

<span data-ttu-id="fd2dd-372">사용하지 않을 정책의 이름을 모르는 경우 다음과 같이 표시할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-372">If you don't know the name of the policy (or policies) to disable, you can display them:</span></span>
  
```
Get-AntiphishPolicy | fl Name
```

<span data-ttu-id="fd2dd-373">기존의 피싱 방지 정책이 없는 경우 하나의 정책을 만들고 사용 해제할 수 있습니다(정책이 없어도 스푸핑 방지가 적용됨, 사용자를 위해 향후 2018년에 기본 정책이 생성될 예정이며 사용자는 기본 정책을 생성하는 대신 비활성화할 수 있음).</span><span class="sxs-lookup"><span data-stu-id="fd2dd-373">If you don't have any existing anti-phishing policies, you can create one and then disable it (even if you don't have a policy, anti-spoofing is still applied; later on in 2018, a default policy will be created for you and you can then disable that instead of creating one).</span></span> <span data-ttu-id="fd2dd-374">여러 단계에서 이 작업을 수행해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-374">You will have to do this in multiple steps:</span></span>
  
```
$org = Get-OrganizationConfig
$name = "My first anti-phishing policy for " + $org.Name
# Note: If the name is more than 64 characters, you will need to choose a smaller one
```

```
# Next, create a new anti-phishing policy with the default values
New-AntiphishPolicy -Name $Name
# Select the domains to scope it to
# Multiple domains are specified in a comma-separated list
$domains = "domain1.com, domain2.com, domain3.com"
# Next, create the anti-phishing rule, scope it to the anti-phishing rule
New-AntiphishRule -Name $name -AntiphishPolicy -RecipientDomainIs $domains
# Finally, scope the anti-phishing policy to the domains
Set-AntiphishPolicy -Identity $name -EnableAntispoofEnforcement $false

```

<span data-ttu-id="fd2dd-375">스푸핑 방지를 사용하지 않도록 설정하는 것은 cmdlet을 통해서만 가능합니다(나중에 보안 &amp; 준수 센터에서 사용할 수 있습니다).</span><span class="sxs-lookup"><span data-stu-id="fd2dd-375">Disabling anti-spoofing is only available via cmdlet (later it will be available in the Security &amp; Compliance Center).</span></span> <span data-ttu-id="fd2dd-376">PowerShell에 액세스 할 수 없는 경우 지원 티켓을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-376">If you do not have access to PowerShell, create a support ticket.</span></span>
  
<span data-ttu-id="fd2dd-377">Office 365로 보낼 때 간접 라우팅을 수행하는 도메인에만 이 규칙을 적용해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-377">Remember, this should only be applied to domains that undergo indirect routing when sent to Office 365.</span></span> <span data-ttu-id="fd2dd-378">오탐지로 인해 스푸핑 방지를 해지 않도록 유의하십시오. 장기적으로는 이를 통해 작업하는 것이 더 낫습니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-378">Resist the temptation to disable anti-spoofing because of some false positives, it will be better in the long run to work through them.</span></span>
  
### <a name="information-for-individual-users"></a><span data-ttu-id="fd2dd-379">개별 사용자를 위한 정보</span><span class="sxs-lookup"><span data-stu-id="fd2dd-379">Information for individual users</span></span>

<span data-ttu-id="fd2dd-380">개별 사용자가 안티 스푸핑 안전 팁과 상호 작용하는 방법이 제한되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-380">Individual users are limited in how they can interact with the anti-spoofing safety tip.</span></span> <span data-ttu-id="fd2dd-381">그러나 일반적인 시나리오를 해결하기 위해 수행할 수 있는 작업이 몇 가지 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-381">However, there are several things you can do to resolve common scenarios.</span></span>
 
### <a name="common-scenario-1---discussion-lists"></a><span data-ttu-id="fd2dd-382">일반적인 시나리오 #1 - 토론 목록</span><span class="sxs-lookup"><span data-stu-id="fd2dd-382">Common scenario #1 - Discussion lists</span></span>

<span data-ttu-id="fd2dd-383">토론 목록은 메시지를 전달하고 내용을 수정하는 방식으로 인해 스푸핑 방지에 문제가 있는 것으로 알려져 있지만 당초 보낸 사람: 주소는 그대로 유지합니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-383">Discussion lists are known to have problems with anti-spoofing due to the way they forward the message and modify its contents yet retain the original From: address.</span></span>
  
<span data-ttu-id="fd2dd-384">예를 들어 이메일 주소가 user@contoso.com이고 Bird Watching에 관심이 있으며 토론 목록 birdwatchers@example.com에 참여한다고 가정합니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-384">For example, suppose your email address is user @ contoso.com, and you are interested in Bird Watching and join the discussion list birdwatchers @ example.com.</span></span> <span data-ttu-id="fd2dd-385">토론 목록에 메시지를 보내면 다음과 같이 보낼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-385">When you send a message to the discussion list, you might send it this way:</span></span>
  
<span data-ttu-id="fd2dd-386">**보낸 사람:** 이진민 \<사용자@contoso.com\></span><span class="sxs-lookup"><span data-stu-id="fd2dd-386">**From:** John Doe \<user @ contoso.com\></span></span> 
  
<span data-ttu-id="fd2dd-387">**받는 사람:** Birdwatcher의 토론 목록 \<birdwatchers@example.com\></span><span class="sxs-lookup"><span data-stu-id="fd2dd-387">**To:** Birdwatcher's Discussion List \<birdwatchers @ example.com\></span></span> 
  
<span data-ttu-id="fd2dd-388">**제목:** 산 정상에서 바라보는 파란색 제비의 장관</span><span class="sxs-lookup"><span data-stu-id="fd2dd-388">**Subject:** Great viewing of blue jays at the top of Mt.</span></span> <span data-ttu-id="fd2dd-389">레이니어 이번 주</span><span class="sxs-lookup"><span data-stu-id="fd2dd-389">Rainier this week</span></span> 
  
<span data-ttu-id="fd2dd-390">이번 주에 레이니어 산에서 이 광경을 확인하고 싶은 </span><span class="sxs-lookup"><span data-stu-id="fd2dd-390">Anyone want to check out the viewing this week from Mt.</span></span> <span data-ttu-id="fd2dd-391">사람이 있습니까?</span><span class="sxs-lookup"><span data-stu-id="fd2dd-391">Rainier?</span></span>
  
<span data-ttu-id="fd2dd-392">전자 메일 목록이 메시지를 받으면 메시지 서식을 지정하고 내용을 수정한 후 여러 전자 메일 받은 사람의 참가자로 구성된 토론 목록의 나머지 구성원에게 전자 메일 목록을 재생합니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-392">When the email list receives the message, they format the message, modify its contents, and replay it to the rest of the members on the discussion list which is made up of participants from many different email receivers.</span></span>
  
<span data-ttu-id="fd2dd-393">**보낸 사람:** 이진민 \<사용자@contoso.com\></span><span class="sxs-lookup"><span data-stu-id="fd2dd-393">**From:** John Doe \<user @ contoso.com\></span></span> 
  
<span data-ttu-id="fd2dd-394">**받는 사람:** Birdwatcher의 토론 목록 \<birdwatchers@example.com\></span><span class="sxs-lookup"><span data-stu-id="fd2dd-394">**To:** Birdwatcher's Discussion List \<birdwatchers @ example.com\></span></span> 
  
<span data-ttu-id="fd2dd-395">**제목:** [새 구경] 산 정상에서 바라보는 파란색 제비의 장관</span><span class="sxs-lookup"><span data-stu-id="fd2dd-395">**Subject:** [BIRDWATCHERS] Great viewing of blue jays at the top of Mt.</span></span> <span data-ttu-id="fd2dd-396">레이니어 이번 주</span><span class="sxs-lookup"><span data-stu-id="fd2dd-396">Rainier this week</span></span> 
  
<span data-ttu-id="fd2dd-397">이번 주에 레이니어 산에서 이 광경을 확인하고 싶은 </span><span class="sxs-lookup"><span data-stu-id="fd2dd-397">Anyone want to check out the viewing this week from Mt.</span></span> <span data-ttu-id="fd2dd-398">사람이 있습니까?</span><span class="sxs-lookup"><span data-stu-id="fd2dd-398">Rainier?</span></span>
  
---
  
<span data-ttu-id="fd2dd-399">Birdwatchers 토론 목록에 이 메시지가 전송되었습니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-399">This message was sent to the Birdwatchers Discussion List.</span></span> <span data-ttu-id="fd2dd-400">구독은 언제든지 취소할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-400">You can unsubscribe at any time.</span></span>
  
<span data-ttu-id="fd2dd-401">위에서 재생된 메시지의 보낸 사람: 주소(user@contoso.com)는 같지만 제목 줄에 태그를 추가하고 메시지의 맨 아래에 바닥글을 추가하여 원래 메시지가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-401">In the above, the replayed message has the same From: address (user @ contoso.com) but the original message has been modified by adding a tag to the Subject line, and a footer to the bottom of the message.</span></span> <span data-ttu-id="fd2dd-402">이러한 유형의 메시지 수정은 메일링 목록에서 일반적이며 오탐지를 초래할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-402">This type of message modification is common in mailing lists, and may result in false positives.</span></span>
  
<span data-ttu-id="fd2dd-403">귀하 또는 귀하의 조직 구성원이 메일링 목록의 관리자인 경우 스푸핑 방지 검사를 통과하도록 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-403">If you or someone in your organization is an administrator of the mailing list, you may be able to configure it to pass anti-spoofing checks.</span></span>
  
- <span data-ttu-id="fd2dd-404">DMARC.org의 FAQ를 확인하십시오. [메일링 목록을 운영 중이며 DMARC와 상호 운용하고 싶습니다. 어떻게 해야합니까? ](https://dmarc.org/wiki/FAQ#I_operate_a_mailing_list_and_I_want_to_interoperate_with_DMARC.2C_what_should_I_do.3F)</span><span class="sxs-lookup"><span data-stu-id="fd2dd-404">Check the FAQ at DMARC.org: [I operate a mailing list and I want to interoperate with DMARC, what should I do?](https://dmarc.org/wiki/FAQ#I_operate_a_mailing_list_and_I_want_to_interoperate_with_DMARC.2C_what_should_I_do.3F)</span></span>

- <span data-ttu-id="fd2dd-405">이 블로그 게시물의 지침을 읽으십시오: [메일링 목록 운영자가 DMARC와 상호 작용하여 실패를 방지하는 팁](https://blogs.msdn.microsoft.com/tzink/2017/03/22/a-tip-for-mailing-list-operators-to-interoperate-with-dmarc-to-avoid-failures/)</span><span class="sxs-lookup"><span data-stu-id="fd2dd-405">Read the instructions at this blog post: [A tip for mailing list operators to interoperate with DMARC to avoid failures](https://blogs.msdn.microsoft.com/tzink/2017/03/22/a-tip-for-mailing-list-operators-to-interoperate-with-dmarc-to-avoid-failures/)</span></span>

- <span data-ttu-id="fd2dd-406">ARC를 지원하기 위해 메일링 목록 서버에 업데이트를 설치하는 것을 고려한다면 [https://arc-spec.org](https://arc-spec.org/)을 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-406">Consider installing updates on your mailing list server to support ARC, see [https://arc-spec.org](https://arc-spec.org/)</span></span>

<span data-ttu-id="fd2dd-407">메일링 목록에 대한 소유권 없는 경우</span><span class="sxs-lookup"><span data-stu-id="fd2dd-407">If you do not have ownership of the mailing list:</span></span>
  
- <span data-ttu-id="fd2dd-408">위의 옵션 중 하나를 구현하도록 메일링 목록의 관리자에게 요청할 수 있습니다(메일링 목록이 중계되는 도메인에 대해 이메일 인증을 설정해야 함)</span><span class="sxs-lookup"><span data-stu-id="fd2dd-408">You can request the maintainer of the mailing list to implement one of the options above (they should also have email authentication set up for the domain the mailing list is relaying from)</span></span>

- <span data-ttu-id="fd2dd-409">이메일 클라이언트에 메일 함 규칙을 만들어 메시지를받은 편지함으로 이동할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-409">You can create mailbox rules in your email client to move messages to the Inbox.</span></span> <span data-ttu-id="fd2dd-410">인증되지 않은 전자 메일을 보내는 합법적인 보낸 사람 관리 섹션에서 설명한 대로 조직의 관리자에게 허용 규칙을 설정하거나 재정의하도록 요청할 수도 있습니다</span><span class="sxs-lookup"><span data-stu-id="fd2dd-410">You can also request your organization's administrators to set up allow rules, or overrides as discussed in the section Managing legitimate senders who are sending unauthenticated email</span></span>

- <span data-ttu-id="fd2dd-411">Office 365에서 지원 티켓을 만들어 메일링 목록에 대한 재정의를 만들어 합법적인 것으로 처리할 수 있습니다</span><span class="sxs-lookup"><span data-stu-id="fd2dd-411">You can create a support ticket with Office 365 to create an override for the mailing list to treat it as legitimate</span></span>

### <a name="other-scenarios"></a><span data-ttu-id="fd2dd-412">다른 시나리오</span><span class="sxs-lookup"><span data-stu-id="fd2dd-412">Other scenarios</span></span>

1. <span data-ttu-id="fd2dd-413">위의 일반적인 시나리오 중 어느 것도 사용자의 상황에 해당하지 않는 경우 Microsoft에 이 메시지를 오탐지로 보고하십시오.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-413">If neither of the above common scenarios applies to your situation, report the message as a false positive back to Microsoft.</span></span> <span data-ttu-id="fd2dd-414">자세한 내용은 이 문서 뒷부분의 [스팸 또는 비스팸 메일을 Microsoft에 다시 보고하는 방법](#how-can-i-report-spam-or-non-spam-messages-back-to-microsoft) 섹션을 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-414">For more information, see the section [How can I report spam or non-spam messages back to Microsoft?](#how-can-i-report-spam-or-non-spam-messages-back-to-microsoft) later in this article.</span></span> 

2. <span data-ttu-id="fd2dd-415">전자 메일 관리자에게 문의하여 Microsoft 지원 티켓으로 사용할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-415">You may also contact your email administrator who can raise it as a support ticket with Microsoft.</span></span> <span data-ttu-id="fd2dd-416">Microsoft 엔지니어링 팀은 메시지가 스푸핑으로 표시된 이유를 조사합니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-416">The Microsoft engineering team will investigate why the message was marked as a spoof.</span></span>

3. <span data-ttu-id="fd2dd-417">또한 보낸 사람이 누구인지 알고 악의적으로 스푸핑되지 않은 것으로 확신하는 경우 보낸 사람에게 회신하여 인증하지 않은 메일 서버에서 메시지를 보내고 있음을 나타낼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-417">Additionally, if you know who the sender is and are confident they are not being maliciously spoofed, you may reply back to the sender indicating that they are sending messages from a mail server that does not authenticate.</span></span> <span data-ttu-id="fd2dd-418">이로 인해 원래 보낸 사람이 IT 관리자에게 연락하여 필요한 전자 메일 인증 레코드를 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-418">This sometimes results in the original sender contacting their IT administrator who will set up the required email authentication records.</span></span>
  
<span data-ttu-id="fd2dd-419">충분한 수의 보낸 사람이 도메인 소유자에게 전자 메일 인증 레코드를 설정해야한다고 회신하면 이들은 작업을 수행하게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-419">When enough senders reply back to domain owners that they should set up email authentication records, it spurs them into taking action.</span></span> <span data-ttu-id="fd2dd-420">Microsoft는 도메인 소유자와 함께 필요한 레코드를 게시하기도 하지만 개별 사용자가 요청할 때 더 많은 도움을줍니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-420">While Microsoft also works with domain owners to publish the required records, it helps even more when individual users request it.</span></span>

4. <span data-ttu-id="fd2dd-421">필요에 따라 보낸 사람을 수신 허용 - 보낸 사람 목록에 추가하십시오.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-421">Optionally, add the sender to your Safe Senders list.</span></span> <span data-ttu-id="fd2dd-422">그러나 피셔가 이 계정을 스푸핑하면 해당 계정은 사서함으로 전달된다는 점을 기억하십시오.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-422">However, be aware that if a phisher spoofs that account, it will be delivered to your mailbox.</span></span> <span data-ttu-id="fd2dd-423">따라서 이 옵션은 자주 사용하서는 안 됩니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-423">Therefore, this option should be used sparingly.</span></span>

## <a name="how-senders-to-microsoft-should-prepare-for-anti-spoofing-protection"></a><span data-ttu-id="fd2dd-424">Microsoft에 보낸 사람이 스푸핑 방지 보호에 대비하는 방법</span><span class="sxs-lookup"><span data-stu-id="fd2dd-424">How senders to Microsoft should prepare for anti-spoofing protection</span></span>

<span data-ttu-id="fd2dd-425">사용자가 현재 Microsoft, Office 365 또는 Outlook.com에 메시지를 보내는 관리자인 경우 전자 메일이 올바르게 인증되었는지 확인해야 합니다. 그렇지 않으면 스팸 또는 피싱으로 표시될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-425">If you are an administrator who currently sends messages to Microsoft, either Office 365 or Outlook.com, you should ensure that your email is properly authenticated otherwise it may be marked as spam or phish.</span></span>
  
### <a name="customers-of-office-365"></a><span data-ttu-id="fd2dd-426">Office 365의 고객</span><span class="sxs-lookup"><span data-stu-id="fd2dd-426">Customers of Office 365</span></span>

<span data-ttu-id="fd2dd-427">Office 365 고객이고 Office 365를 사용하여 아웃 바운드 전자 메일을 보내는 경우:</span><span class="sxs-lookup"><span data-stu-id="fd2dd-427">If you are an Office 365 customer and you use Office 365 to send outbound email:</span></span>
  
- <span data-ttu-id="fd2dd-428">도메인에 대해 [스푸핑을 방지할 수 있도록 Office 365에서 SPF 설정](set-up-spf-in-office-365-to-help-prevent-spoofing.md)</span><span class="sxs-lookup"><span data-stu-id="fd2dd-428">For your domains, [Set up SPF in Office 365 to help prevent spoofing](set-up-spf-in-office-365-to-help-prevent-spoofing.md)</span></span>

- <span data-ttu-id="fd2dd-429">기본 도메인의 경우 [DKIM을 사용하여 Office 365에서 사용자 지정 도메인에서 전송한 발신 이메일을 확인](use-dkim-to-validate-outbound-email.md)</span><span class="sxs-lookup"><span data-stu-id="fd2dd-429">For your primary domains, [Use DKIM to validate outbound email sent from your custom domain in Office 365](use-dkim-to-validate-outbound-email.md)</span></span>

- <span data-ttu-id="fd2dd-430">[합법적인 발신자를 확인하기 위해 도메인에서 DMARC 레코드 설정](use-dmarc-to-validate-email.md)을 고려합니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-430">[Consider setting up DMARC records](use-dmarc-to-validate-email.md) for your domain to determine who are your legitimate senders</span></span>

<span data-ttu-id="fd2dd-431">Microsoft는 SPF, DKIM 및 DMARC 각각에 대한 세부 구현 지침을 제공하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-431">Microsoft does not provide detailed implementation guidelines for each of SPF, DKIM, and DMARC.</span></span> <span data-ttu-id="fd2dd-432">그러나 온라인 게시된 정보는 매우 많습니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-432">However, there is a lot of information published online.</span></span> <span data-ttu-id="fd2dd-433">조직에서 전자 메일 인증 레코드를 설정할 수 있도록 지원하는 제3자 회사도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-433">There are also 3rd party companies dedicated to helping your organization set up email authentication records.</span></span>
  
### <a name="administrators-of-domains-that-are-not-office-365-customers"></a><span data-ttu-id="fd2dd-434">Office 365 고객이 아닌 도메인 관리자</span><span class="sxs-lookup"><span data-stu-id="fd2dd-434">Administrators of domains that are not Office 365 customers</span></span>

<span data-ttu-id="fd2dd-435">도메인 관리자이지만 Office 365 고객이 아닌 경우:</span><span class="sxs-lookup"><span data-stu-id="fd2dd-435">If you are a domain administrator but are not an Office 365 customer:</span></span>
  
- <span data-ttu-id="fd2dd-436">도메인의 보내는 IP 주소를 게시하려면 SPF를 설정하고, DKIM(사용 가능한 경우)도 설정하여 메시지에 디지털 서명을 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-436">You should set up SPF to publish your domain's sending IP addresses, and also set up DKIM (if available) to digitally sign messages.</span></span> <span data-ttu-id="fd2dd-437">DMARC 레코드 설정도 고려할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-437">You may also consider setting up DMARC records.</span></span>

- <span data-ttu-id="fd2dd-438">사용자를 대신하여 전자 메일을 전송하는 대량 메일 발신자가 있는 경우 발신자 주소의 보낸 사람 도메인(자신이 속한 경우)이 SPF 또는 DMARC를 통과하는 도메인과 정렬되도록 전자 메일을 보내야 합니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-438">If you have bulk senders who are transmitting email on your behalf, you should work with them to send email in a way such that the sending domain in the From: address (if it belongs to you) aligns with the domain that passes SPF or DMARC.</span></span>

- <span data-ttu-id="fd2dd-439">온 프레미스 메일 서버가 있거나 Software-as-a-service 공급자에서 보내는 경우 또는 Microsoft Azure, GoDaddy, Rackspace, Amazon Web Services나 이와 유사한 클라우드 호스팅 서비스에서 보내는 경우, 해당 서비스가 추가되도록 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-439">If you have on-premises mail servers, or send from a Software-as-a-service provider, or from a cloud-hosting service like Microsoft Azure, GoDaddy, Rackspace, Amazon Web Services, or similar, you should ensure that they are added to your SPF record.</span></span>

- <span data-ttu-id="fd2dd-440">ISP에서 호스팅하는 소규모 도메인인 경우 ISP에서 제공 한 지침에 따라 SPF 레코드를 설정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-440">If you are a small domain that is hosted by an ISP, you should set up your SPF record according to the instructions that is provided to you by your ISP.</span></span> <span data-ttu-id="fd2dd-441">대부분의 ISP는 이러한 유형의 지침을 제공하며 회사의 지원 페이지에서 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-441">Most ISPs provide these types of instructions and can be found on the company's support pages.</span></span>

- <span data-ttu-id="fd2dd-442">이전에 전자 메일 인증 레코드를 게시할 필요가 없었고 제대로 작동했더라도, 전자 메일 인증 레코드를 게시하여 Microsoft에 보내야 합니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-442">Even if you have not had to publish email authentication records before, and it worked fine, you must still publish email authentication records to send to Microsoft.</span></span> <span data-ttu-id="fd2dd-443">이를 통해 사용자는 피싱 퇴치 작업에 동참하게 되며 사용자 또는 사용자가 메시지를 보내는 조직 중 어느 하나가 피싱받을 가능성을 줄입니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-443">By doing so, you are helping in the fight against phishing, and reducing the possibility that either you, or organizations you send to, will get phished.</span></span>

### <a name="what-if-you-dont-know-who-sends-email-as-your-domain"></a><span data-ttu-id="fd2dd-444">누가 도메인으로 전자 메일을 보내는지 모르는 경우에는 어떻게 해야 합니까?</span><span class="sxs-lookup"><span data-stu-id="fd2dd-444">What if you don't know who sends email as your domain?</span></span>

<span data-ttu-id="fd2dd-445">많은 도메인은 보낸 사람이 누구인지 모르기 때문에 SPF 레코드를 게시하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-445">Many domains do not publish SPF records because they do not know who all their senders are.</span></span> <span data-ttu-id="fd2dd-446">이는 문제가 되지 않습니다. 보내는 사람을 모두 알 필요는 없습니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-446">That's okay, you do not need to know who all of them are.</span></span> <span data-ttu-id="fd2dd-447">대신, 특히 회사 트래픽이있는 곳에서 알고 있는 SPF 레코드를 게시하고 중립 SPF 정책인 all을 게시하여 작업을 시작해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-447">Instead, you should get started by publishing an SPF record for the ones you do know of, especially where your corporate traffic is located, and publish a neutral SPF policy, ?all:</span></span>
  
<span data-ttu-id="fd2dd-448">example.com IN TXT "v=spf1 include:spf.example.com ?all"</span><span class="sxs-lookup"><span data-stu-id="fd2dd-448">example.com IN TXT "v=spf1 include:spf.example.com ?all"</span></span>
  
<span data-ttu-id="fd2dd-449">중립적인 SPF 정책은 기업 인프라에서 나오는 전자 메일이 다른 모든 전자 메일 수신자에서 이메일 인증을 통과한다는 것을 의미합니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-449">The neutral SPF policy means that any email that comes out of your corporate infrastructure will pass email authentication at all other email receivers.</span></span> <span data-ttu-id="fd2dd-450">귀하가 모르는 발신자가 보낸 이메일은 중립으로 돌아가며 SPF 레코드를 전혀 게시하지 않은 것과 유사합니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-450">Email that comes from senders you don't know about will fall back to neutral, which is almost the same as publishing no SPF record at all.</span></span>
  
<span data-ttu-id="fd2dd-451">Office 365로 전송할 때 회사 트래픽에서 오는 전자 메일은 인증된 것으로 표시되지만 출처를 알 수 없는 전자 메일은 (Office 365에서 암시 적으로 인증할 수 있는지 여부에 따라) 여전히 스푸핑으로 표시될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-451">When sending to Office 365, email that comes from your corporate traffic will be marked as authenticated, but the email that comes from sources you don't know about may still be marked as spoof (depending upon whether or not Office 365 can implicitly authenticate it).</span></span> <span data-ttu-id="fd2dd-452">그러나 이는 모든 전자 메일이 스푸핑으로 표시되던 문제를 Office 365이 개선한 사항에 해당합니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-452">However, this is still an improvement from all email being marked as spoof by Office 365.</span></span>
  
<span data-ttu-id="fd2dd-453">대체 정책 ?all을 통해 SPF 레코드를 시작한 후에 점차적으로 인프라를 더 많이 포함시킨 다음 더 엄격한 정책을 게시할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-453">Once you've gotten started with an SPF record with a fallback policy of ?all, you can gradually include more and more sending infrastructure and then publish a stricter policy.</span></span> 
  
### <a name="what-if-you-are-the-owner-of-a-mailing-list"></a><span data-ttu-id="fd2dd-454">메일링 목록의 소유자라면 어떻게 될까요?</span><span class="sxs-lookup"><span data-stu-id="fd2dd-454">What if you are the owner of a mailing list?</span></span>

<span data-ttu-id="fd2dd-455">[공통 시나리오 # 1 - 토론 목록](#common-scenario-1---discussion-lists) 섹션을 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-455">See the section [Common scenario #1 - Discussion lists](#common-scenario-1---discussion-lists).</span></span>
  
### <a name="what-if-you-are-an-infrastructure-provider-such-as-an-internet-service-provider-isp-email-service-provider-esp-or-cloud-hosting-service"></a><span data-ttu-id="fd2dd-456">인터넷 서비스 공급자(ISP), 이메일 서비스 공급자(ESP) 또는 클라우드 호스팅 서비스와 같은 인프라 공급자의 경우에는 어떻게 해야 합니까?</span><span class="sxs-lookup"><span data-stu-id="fd2dd-456">What if you are an infrastructure provider such as an Internet Service Provider (ISP), Email Service Provider (ESP), or cloud hosting service?</span></span>

<span data-ttu-id="fd2dd-457">도메인 전자 메일을 호스팅하고 전자 메일을 보내거나 전자 메일을 보낼 수있는 호스팅 인프라를 제공하는 경우 다음을 수행해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-457">If you host a domain's email, and it sends email, or provide hosting infrastructure that can send email, you should do the following:</span></span>
  
- <span data-ttu-id="fd2dd-458">고객이 SPF 레코드에 게시 할 내용을 자세히 설명하는 문서를 보유하고 있는지 확인하십시오.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-458">Ensure your customers have documentation detailing what to publish in their SPF records</span></span>

- <span data-ttu-id="fd2dd-459">고객이 명시적으로 설정하지 않은 경우에도 아웃 바운드 전자 메일에서 DKIM 서명에 서명하는 것을 고려해보십시오(기본 도메인으로 서명).</span><span class="sxs-lookup"><span data-stu-id="fd2dd-459">Consider signing DKIM-signatures on outbound email even if the customer doesn't explicitly set it up (sign with a default domain).</span></span> <span data-ttu-id="fd2dd-460">DKIM 서명을 사용하여 이메일을 이중 서명 할 수도 있습니다(고객 도메인을 설정한 경우 한 번, 회사의 DKIM 서명을 사용하는 경우 두 번째 서명).</span><span class="sxs-lookup"><span data-stu-id="fd2dd-460">You can even double-sign the email with DKIM signatures (once with the customer's domain if they have set it up, and a second time with your company's DKIM signature)</span></span>

<span data-ttu-id="fd2dd-461">플랫폼에서 발생하는 전자 메일을 인증하더라도 Microsoft에 대한 제공 가능성은 보장되지 않지만 적어도 Microsoft가 인증되지 않았기 때문에 전자 메일을 스팸으로 처리하지 않도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-461">Deliverability to Microsoft is not guaranteed even if you authenticate email originating from your platform, but at least it ensures that Microsoft does not junk your email because it is not authenticated.</span></span> <span data-ttu-id="fd2dd-462">Outlook.com에서 전자 메일을 필터링하는 방법에 대한 자세한 내용은 [Outlook.com 전자 메일 관리자 페이지](https://postmaster.live.com/pm/postmaster.aspx)를 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-462">For more details around how Outlook.com filters email, see the [Outlook.com Postmaster page](https://postmaster.live.com/pm/postmaster.aspx).</span></span>
  
<span data-ttu-id="fd2dd-463">서비스 공급자 모범 사례에 대한 자세한 내용은 [M3AAWG 모바일 메시징 모범 사례 서비스 제공자](https://www.m3aawg.org/sites/default/files/M3AAWG-Mobile-Messaging-Best-Practices-Service-Providers-2015-08.pdf)를 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-463">For more details on service providers best practices, see [M3AAWG Mobile Messaging Best Practices for Service Providers](https://www.m3aawg.org/sites/default/files/M3AAWG-Mobile-Messaging-Best-Practices-Service-Providers-2015-08.pdf).</span></span>
  
## <a name="frequently-asked-questions"></a><span data-ttu-id="fd2dd-464">질문과 대답</span><span class="sxs-lookup"><span data-stu-id="fd2dd-464">Frequently Asked Questions</span></span>

### <a name="why-is-microsoft-making-this-change"></a><span data-ttu-id="fd2dd-465">왜 Microsoft는 이러한 변경을 수행하는 이유는 무엇입니까?</span><span class="sxs-lookup"><span data-stu-id="fd2dd-465">Why is Microsoft making this change?</span></span>

<span data-ttu-id="fd2dd-466">피싱 공격의 영향으로 인해 전자 메일 인증이 15년 이상 지속되었기 때문에 Microsoft는 합법적인 전자 메일 손실 위험보다 인증되지 않은 전자 메일을 지속적으로 받을 위험이 높다고 생각합니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-466">Because of the impact of phishing attacks, and because email authentication has been around for over 15 years, Microsoft believes that the risk of continue to allow unauthenticated email is higher than the risk of losing legitimate email.</span></span>
  
### <a name="will-this-change-cause-legitimate-email-to-be-marked-as-spam"></a><span data-ttu-id="fd2dd-467">이 변경으로 합법적인 전자 메일이 스팸으로 표시됩니까?</span><span class="sxs-lookup"><span data-stu-id="fd2dd-467">Will this change cause legitimate email to be marked as spam?</span></span>

<span data-ttu-id="fd2dd-468">처음에는 스팸으로 표시되는 일부 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-468">At first, there will be some messages that are marked as spam.</span></span> <span data-ttu-id="fd2dd-469">그러나 시간이 지남에 따라 보낸 사람은 조정할 것이며, 이에 따라 스푸핑된 것으로 잘못 표시된 메일의 양은 대부분의 이메일 경로에서 무시해도 될 수준이 될 것입니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-469">However, over time, senders will adjust and then the amount of messages mislabeled as spoofed will be negligible for most email paths.</span></span>
  
<span data-ttu-id="fd2dd-470">Microsoft 자체는 처음에 다른 고객들에게 배포하기 몇 주 전에 이 기능을 채택했습니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-470">Microsoft itself first adopted this feature several weeks before deploying it to the rest of its customers.</span></span> <span data-ttu-id="fd2dd-471">처음에는 혼란이 있었지만 점차적으로 감소했습니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-471">While there was disruption at first, it gradually declined.</span></span>
  
### <a name="will-microsoft-bring-this-feature-to-outlookcom-and-non-advanced-threat-protection-customers-of-office-365"></a><span data-ttu-id="fd2dd-472">Microsoft는 Office 365의 Outlook.com 및 비 Advanced Threat Protection 고객에게 이 기능을 제공합니까?</span><span class="sxs-lookup"><span data-stu-id="fd2dd-472">Will Microsoft bring this feature to Outlook.com and non-Advanced Threat Protection customers of Office 365?</span></span>

<span data-ttu-id="fd2dd-473">초기에 Microsoft의 스푸핑 방지 기술은 Office 365 Enterprise E5 구독이 있거나 해당 구독에 대한 Office 365 ATP(Advanced Threat Protection) 추가 기능을 구입 한 조직에 배포되었습니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-473">Microsoft's anti-spoofing technology was initially deployed to its organizations that had an Office 365 Enterprise E5 subscription or had purchased the Office 365 Advanced Threat Protection (ATP) add-on for their subscription.</span></span> <span data-ttu-id="fd2dd-474">2018년 10월을 기준으로 Microsoft는 Exchange Online Protection(EOP)을 지닌 조직으로 보호를 확대했습니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-474">As of October, 2018 we've extended the protection to organizations that have Exchange Online Protection (EOP) as well.</span></span> <span data-ttu-id="fd2dd-475">나중에 Outlook.com을 위해 릴리스할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-475">In the future, we may release it for Outlook.com.</span></span> <span data-ttu-id="fd2dd-476">그러나 그렇게 하면 보고 및 사용자 지정 재정의와 같이 적용되지 않는 기능이 있을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-476">However, if we do, there may be some capabilities that are not applied such as reporting and custom overrides.</span></span>
  
### <a name="how-can-i-report-spam-or-non-spam-messages-back-to-microsoft"></a><span data-ttu-id="fd2dd-477">스팸 또는 비스팸 메시지를 Microsoft에 다시 보고하려면 어떻게 합니까?</span><span class="sxs-lookup"><span data-stu-id="fd2dd-477">How can I report spam or non-spam messages back to Microsoft?</span></span>

<span data-ttu-id="fd2dd-478">
  [Outlook용 보고서 메시지 추가 기능](https://support.office.com/article/use-the-report-message-add-in-b5caa9f1-cdf3-4443-af8c-ff724ea719d2)을 사용하거나 이것이 설치되어 있지 않은 경우 [분석용 Microsoft에 스팸, 스팸 방지 및 피싱 사기 메시지를 제출](https://technet.microsoft.com/ko-KR/library/jj200769%28v=exchg.150%29.aspx)할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-478">You can either use the [Report Message Add-in for Outlook](https://support.office.com/article/use-the-report-message-add-in-b5caa9f1-cdf3-4443-af8c-ff724ea719d2), or if it isn't installed, [Submit spam, non-spam, and phishing scam messages to Microsoft for analysis](https://technet.microsoft.com/en-us/library/jj200769%28v=exchg.150%29.aspx).</span></span>
  
### <a name="im-a-domain-administrator-who-doesnt-know-who-all-my-senders-are"></a><span data-ttu-id="fd2dd-479">저는 도메인 관리자이고 나의 보낸 사람을 모두 다 알지 못합니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-479">I'm a domain administrator who doesn't know who all my senders are!</span></span>

<span data-ttu-id="fd2dd-480">[Office 365 고객이 아닌 도메인 관리자](#administrators-of-domains-that-are-not-office-365-customers)를 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-480">Please see [Administrators of domains that are not Office 365 customers](#administrators-of-domains-that-are-not-office-365-customers).</span></span>
  
### <a name="what-happens-if-i-disable-anti-spoofing-protection-for-my-organization-even-though-office-365-is-my-primary-filter"></a><span data-ttu-id="fd2dd-481">Office 365가 기본 필터인데도 조직의 스푸핑 방지 기능을 해제하면 어떻게 됩니까?</span><span class="sxs-lookup"><span data-stu-id="fd2dd-481">What happens if I disable anti-spoofing protection for my organization, even though Office 365 is my primary filter?</span></span>

<span data-ttu-id="fd2dd-482">피싱 및 스팸 메일을 놓치는 경우가 많아질 것이므로 이는 권장하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-482">We do not recommend this because you will be exposed to more missed phishing and spam messages.</span></span> <span data-ttu-id="fd2dd-483">모든 피싱이 스푸핑이 되는 것은 아니며 모든 스푸핑이 누락되지는 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-483">Not all phishing is spoofing, and not all spoofs will be missed.</span></span> <span data-ttu-id="fd2dd-484">그러나 사용자의 위험은 스푸핑 방지를 사용하는 고객보다 높습니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-484">However, your risk will be higher than a customer who enables anti-spoofing.</span></span>
  
### <a name="does-enabling-anti-spoofing-protection-mean-i-will-be-protected-from-all-phishing"></a><span data-ttu-id="fd2dd-485">스푸핑 방지 기능을 사용하면 모든 피싱으로부터 보호받을 수 있습니까?</span><span class="sxs-lookup"><span data-stu-id="fd2dd-485">Does enabling anti-spoofing protection mean I will be protected from all phishing?</span></span>

<span data-ttu-id="fd2dd-486">안타깝게도 피싱 공격자는 손상된 계정과 같은 다른 기술을 사용하거나 무료 서비스 계정을 설정하기 때문에 적응할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-486">Unfortunately, no, because phishers will adapt to use other techniques such as compromised accounts, or setting up accounts of free services.</span></span> <span data-ttu-id="fd2dd-487">그러나 Office 365의 보호 레이어가 함께 작동하고 서로 위에 구축되기 때문에 피싱 방지 기능은 다른 유형의 피싱 방법을 탐지하는 데 훨씬 효과적입니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-487">However, anti-phishing protection works much better to detect these other types of phishing methods because Office 365's protection layers are designed work together and build on top of each other.</span></span>
  
### <a name="do-other-large-email-receivers-block-unauthenticated-email"></a><span data-ttu-id="fd2dd-488">다른 대형 전자 메일 수신자가 인증되지 않은 전자 메일을 차단합니까?</span><span class="sxs-lookup"><span data-stu-id="fd2dd-488">Do other large email receivers block unauthenticated email?</span></span>

<span data-ttu-id="fd2dd-489">거의 모든 대형 전자 메일 수신자는 기존의 SPF, DKIM 및 DMARC를 구현합니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-489">Nearly all large email receivers implement traditional SPF, DKIM, and DMARC.</span></span> <span data-ttu-id="fd2dd-490">일부 수신자에는 그 표준보다 엄격한 다른 검사가 있지만 인증되지 않은 전자 메일을 차단하고 이를 스푸핑으로 취급하는 Office 365는 거의 없습니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-490">Some receivers have other checks that are more strict than just those standards, but few go as far as Office 365 to block unauthenticated email and treat them as a spoof.</span></span> <span data-ttu-id="fd2dd-491">그러나 대부분의 업계에서는 이러한 특정 유형의 전자 메일에 대해 점점 더 엄격 해지고 있습니다. 특히 피싱 문제 때문입니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-491">However, most of the industry is becoming more and more strict about this particular type of email, particularly because of the problem of phishing.</span></span>
  
### <a name="do-i-still-need-the-advanced-spam-filtering-option-enabled-for-spf-hard-fail-if-i-enable-anti-spoofing"></a><span data-ttu-id="fd2dd-492">스푸핑 방지를 활성화하면 "SPF 하드 실패"에 대해 고급 스팸 필터링 옵션이 계속 설정되어 있어야 합니까?</span><span class="sxs-lookup"><span data-stu-id="fd2dd-492">Do I still need the Advanced Spam Filtering option enabled for "SPF Hard Fail" if I enable anti-spoofing?</span></span>

<span data-ttu-id="fd2dd-493">아니요, 이 옵션은 더 이상 필요하지 않습니다. 이는 스푸핑 방지 기능이 SPF 하드 실패 뿐 아니라 훨씬 더 광범위한 기준을 고려하기 때문입니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-493">No, this option is no longer required because the anti-spoofing feature not only considers SPF hard fails, but a much wider set of criteria.</span></span> <span data-ttu-id="fd2dd-494">스푸핑 방지를 사용하고 SPF 하드 실패 옵션을 사용하도록 설정한 경우 더 많은 오탐지가 발생할 것입니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-494">If you have anti-spoofing enabled and the SPF Hard Fail option enabled, you will probably get more false positives.</span></span> <span data-ttu-id="fd2dd-495">스팸이나 피싱을 추가로 포착하지 않아도되고 대부분 오탐지가 발생하기 때문에 이 기능을 비활성화하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-495">We recommend disabling this feature as it would provide almost no additional catch for spam or phish, and instead generate mostly false positives.</span></span>
  
### <a name="does-sender-rewriting-scheme-srs-help-fix-forwarded-email"></a><span data-ttu-id="fd2dd-496">보낸 사람 다시 작성 구상(SRS)이 전달된 전자 메일을 수정하는 데 도움이 됩니까?</span><span class="sxs-lookup"><span data-stu-id="fd2dd-496">Does Sender Rewriting Scheme (SRS) help fix forwarded email?</span></span>

<span data-ttu-id="fd2dd-497">SRS는 전달된 전자 메일 문제를 부분적으로만 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-497">SRS only partially fixes the problem of forwarded email.</span></span> <span data-ttu-id="fd2dd-498">SMTP MAIL FROM를 다시 쓰면 SRS는 전달된 메시지가 다음 대상에서 SPF를 통과하도록 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-498">By rewriting the SMTP MAIL FROM, SRS can ensure that the forwarded message passes SPF at the next destination.</span></span> <span data-ttu-id="fd2dd-499">그러나 스푸핑 방지는 MAIL FROM 또는 DKIM 서명 도메인(또는 다른 신호)과 함께 보낸 사람: 주소를 기반으로하기 때문에 전달된 전자 메일이 스푸핑으로 표시되는 것을 방지하기에 충분하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fd2dd-499">However, because anti-spoofing is based upon the From: address in combination with either the MAIL FROM or DKIM-signing domain (or other signals), it is not enough to prevent forwarded email from being marked as spoofed.</span></span>
