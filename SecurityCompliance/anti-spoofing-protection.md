---
title: Office 365의 스푸핑 방지 보호 기능
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 12/06/2018
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: d24bb387-c65d-486e-93e7-06a4f1a436c0
description: 이 문서에서는 방법 Office 365을 완화 피싱 공격에 대해 사용 하 여 보낸 사람이 도메인, 위장 된 도메인, 즉 위조를 설명 합니다. 메시지를 분석 하 여이 기능을 수행 하기 및 neithe 표준 전자 메일 인증 방법 및 기타 보낸사람 신뢰도 기술을 사용 하 여 인증 될 수 있는 위치를 차단 합니다. 이 변경 피싱 공격에 노출 되는 조직에서 Office 365의 수를 줄이는 구현 됩니다.
ms.openlocfilehash: 4ce195feae002e468d1b6ed61c6b186af7f8950d
ms.sourcegitcommit: 7e2a0185cadea7f3a6afc5ddc445eac2e1ce22eb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/11/2019
ms.locfileid: "29614512"
---
# <a name="anti-spoofing-protection-in-office-365"></a><span data-ttu-id="1b1b7-105">Office 365의 스푸핑 방지 보호 기능</span><span class="sxs-lookup"><span data-stu-id="1b1b7-105">Anti-spoofing protection in Office 365</span></span>

<span data-ttu-id="1b1b7-p102">이 문서에서는 방법 Office 365을 완화 피싱 공격에 대해 사용 하 여 보낸 사람이 도메인, 위장 된 도메인, 즉 위조를 설명 합니다. 메시지를 분석 하 고 전자 메일 표준 인증 방법 및 기타 보낸사람 신뢰도 기술을 사용 하 여 인증할 수 없는 것을 차단 하 여 수행 합니다. 이 변경 피싱 공격에 노출 되는 고객의 수를 줄이는 구현 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1b1b7-p102">This article describes how Office 365 mitigates against phishing attacks that uses forged sender domains, that is, domains that are spoofed. It accomplishes this by analyzing the messages and blocking the ones that cannot be authenticated using standard email authentication methods, nor other sender reputation techniques. This change is being implemented to reduce the number of phishing attacks customers are exposed to.</span></span>
  
<span data-ttu-id="1b1b7-109">이 문서에서는 또한이 변경이 수행 되는 이유, 수이 변경에 대 한 고객을 준비 하는 방법을, 영향을 받을 메시지를 확인 하는 방법, 메시지를 보고 하는 방법, 가양성을 완화 하는 방법으로 해야이 대 한 Microsoft에 보낸사람을 준비 하는 방법을 설명합니다 이 옵션을 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b1b7-109">This article also describes why this change is being made, how customers can prepare for this change, how to view messages that will be affected, how to report on messages, how to mitigate false positives, as well as how senders to Microsoft should prepare for this change.</span></span>
  
<span data-ttu-id="1b1b7-p103">Microsoft의 스푸핑 방지 기술 Office 365 Enterprise e 5 구독 명의 또는 구독에 대 한 Office 365 고급 위협 보호 (ATP) 추가 기능을 구입 명의 하는 해당 조직에 처음 배포 되었습니다. 년 10 월 2018를 기준으로 보호 하는 조직에서는 Exchange Online Protection (EOP)도를 확장 했을 때 했습니다. 또한이 필터는 모든 서로에서 설명 하는 방식 때문에 Outlook.com 사용자도 영향을 받을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1b1b7-p103">Microsoft's anti-spoofing technology was initially deployed to its organizations that had an Office 365 Enterprise E5 subscription or had purchased the Office 365 Advanced Threat Protection (ATP) add-on for their subscription. As of October, 2018 we've extended the protection to organizations that have Exchange Online Protection (EOP) as well. Additionally, because of the way all of our filters learn from each other, Outlook.com users may also be affected.</span></span>
  
## <a name="how-spoofing-is-used-in-phishing-attacks"></a><span data-ttu-id="1b1b7-113">피싱 공격에 스푸핑 사용 방법</span><span class="sxs-lookup"><span data-stu-id="1b1b7-113">How spoofing is used in phishing attacks</span></span>

<span data-ttu-id="1b1b7-p104">와 관련해 서 해당 사용자를 보호 하기 위해 Microsoft 피싱의 위협을 심각 하 게 됩니다. 스팸 및 피셔 일반적으로 사용 하는 방법 중 하나는 스푸핑, 보낸 사람이 위조는 때은 하 고 보낸 사람이 보낸 또는 실제 원본 이외의 라는 메시지가 나타납니다. 이 기술은 사용자 자격 증명을 받을 수 있도록 디자인 피싱 캠페인에 종종 사용 됩니다. Microsoft의 스푸핑 방지 기술 특히 위조를 검사 하는 '에서: 헤더 ' Outlook 같은 전자 메일 클라이언트에 표시 되는 것은 합니다. Microsoft는 높은 정확도 하는 경우는 From: 헤더를 위장, 스푸핑은으로 메시지를 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b1b7-p104">When it comes to protecting its users, Microsoft takes the threat of phishing seriously. One of the techniques that spammers and phishers commonly use is spoofing, which is when the sender is forged, and a message appears to originate from someone or somewhere other than the actual source. This technique is often used in phishing campaigns designed to obtain user credentials. Microsoft's Anti-spoof technology specifically examines forgery of the 'From: header' which is the one that shows up in an email client like Outlook. When Microsoft has high confidence that the From: header is spoofed, it identifies the message as a spoof.</span></span>
  
<span data-ttu-id="1b1b7-119">스푸핑 메시지에 영향을 두 음수 실제 사용자에 대 한:</span><span class="sxs-lookup"><span data-stu-id="1b1b7-119">Spoofing messages have two negative implications for real life users:</span></span>
  
### <a name="1-spoofed-messages-deceive-users"></a><span data-ttu-id="1b1b7-120">1. 위조 메시지 속이기 사용자</span><span class="sxs-lookup"><span data-stu-id="1b1b7-120">1. Spoofed messages deceive users</span></span>
  
<span data-ttu-id="1b1b7-p105">첫째, 위장 된 메시지 수 유인 사용자 링크를 클릭 하 고 자격 증명을 포기, 맬웨어, 다운로드 또는 (후자는 이라고 비즈니스 전자 메일 손상) 중요 한 콘텐츠가 포함 된 메시지에 회신 하기 합니다. 예, 다음은 msoutlook94@service.outlook.com의 위장 된 발신자가 포함 된 피싱 메시지:</span><span class="sxs-lookup"><span data-stu-id="1b1b7-p105">First, a spoofed message may trick a user into clicking a link and giving up their credentials, downloading malware, or replying to a message with sensitive content (the latter of which is known as Business Email Compromise). For example, the following is a phishing message with a spoofed sender of msoutlook94@service.outlook.com:</span></span>
  
![피싱 메시지 service.outlook.com 가장](media/1a441f21-8ef7-41c7-90c0-847272dc5350.jpg)
  
<span data-ttu-id="1b1b7-p106">위의 service.outlook.com에서 실제로 제공 하지 않은 하지만 대신와 같게 보이도록 하기 위해 phisher에 의해 위장 되었습니다. 사용자가 메시지 내 링크를 클릭 하는 것을 유인를 시도 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b1b7-p106">The above did not actually come from service.outlook.com, but instead was spoofed by the phisher to make it look like it did. It is attempting to trick a user into clicking the link within the message.</span></span>
  
<span data-ttu-id="1b1b7-126">다음 예제에서는 contoso.com을 스푸핑 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1b1b7-126">The next example is spoofing contoso.com:</span></span>
  
![피싱 메시지-비즈니스 전자 메일 손상](media/da15adaa-708b-4e73-8165-482fc9182090.jpg)
  
<span data-ttu-id="1b1b7-p107">메시지 합법적인, 실제로 있어 보이지만 스푸핑은 합니다. 이 피싱 메시지는 피싱의 하위 범주는 비즈니스 전자 메일 손상의 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="1b1b7-p107">The message looks legitimate, but in fact is a spoof. This phishing message is a type of Business Email Compromise which is a subcategory of phishing.</span></span>
    
### <a name="2-users-confuse-real-messages-for-fake-ones"></a><span data-ttu-id="1b1b7-130">2. 사용자가 혼동 위조 오류에 대 한 실제 메시지</span><span class="sxs-lookup"><span data-stu-id="1b1b7-130">2. Users confuse real messages for fake ones</span></span>
  
<span data-ttu-id="1b1b7-p108">둘째, 위장 된 메시지 피싱 메시지에 대 한 알 수 있지만 실제 메시지와 위장 된 1 간의 차이 알 수 없으므로 사용자에 대 한 불확실성을 만듭니다. 예, 다음은 Microsoft 보안 계정 전자 메일 주소에서 다시 설정 하는 실제 암호의 예:</span><span class="sxs-lookup"><span data-stu-id="1b1b7-p108">Second, spoofed messages create uncertainty for users who know about phishing messages but cannot tell the difference between a real message and spoofed one. For example, the following is an example of an actual password reset from the Microsoft Security account email address:</span></span>
  
![Microsoft 합법적인 암호 다시 설정](media/58a3154f-e83d-4f86-bcfe-ae9e8c87bd37.jpg)
  
<span data-ttu-id="1b1b7-p109">위의 메시지가 Microsoft에서 제공 않은 이지만 속성을 동시에 사용자를 사용 하는 피싱 메시지를 가져오는 수 유인 사용자 링크를 클릭 하 고 자격 증명을 포기, 맬웨어, 다운로드 또는 중요 한 콘텐츠가 포함 된 메시지에 회신 하기 합니다. 실제 암호 다시 설정 하 고 위조 하나 간의 차이 구분 하기 어려운 이기 때문에 많은 사용자는 이러한 메시지를 무시 하 스팸 보고 또는 불필요 하 게 하는 메시지를 다시 보고 Microsoft 부재중된 피싱 메일으로 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b1b7-p109">The above message did come from Microsoft, but at the same time, users are used to getting phishing messages that may trick a user into clicking a link and giving up their credentials, downloading malware, or replying to a message with sensitive content. Because it is difficult to tell the difference between a real password reset and a fake one, many users ignore these messages, report them as spam, or unnecessarily report the messages back to Microsoft as missed phishing scams.</span></span>
    
<span data-ttu-id="1b1b7-p110">스푸핑를 중지 하려면 산업을 필터링 하는 전자 메일 [SPF](https://docs.microsoft.com/office365/SecurityCompliance/set-up-spf-in-office-365-to-help-prevent-spoofing), [DKIM](https://docs.microsoft.com/office365/SecurityCompliance/use-dkim-to-validate-outbound-email)및 [DMARC](https://docs.microsoft.com/office365/SecurityCompliance/use-dmarc-to-validate-email)와 같은 전자 메일 인증 프로토콜을 개발 했습니다. DMARC 메시지의 보낸 사람이-사용자에 게 자신의 전자 메일 클라이언트에 표시 한 검토 스푸핑 방지 (위의 예제에서 이것은 service.outlook.com, outlook.com, 및 accountprotection.microsoft.com)-SPF 또는 DKIM를 전달 하는 도메인과 합니다. 즉, 사용자에 게 표시 되는 도메인 인증 된 및 따라서 스푸핑 하지 않습니다. 보다 완전 한 토론 섹션을 참조 하십시오. "*전자 메일 인증 없는 이유 항상 스푸핑 중지 하기에 충분 해"* 이 문서에서 나중에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1b1b7-p110">To stop spoofing, the email filtering industry has developed email authentication protocols such as [SPF](https://docs.microsoft.com/office365/SecurityCompliance/set-up-spf-in-office-365-to-help-prevent-spoofing), [DKIM](https://docs.microsoft.com/office365/SecurityCompliance/use-dkim-to-validate-outbound-email), and [DMARC](https://docs.microsoft.com/office365/SecurityCompliance/use-dmarc-to-validate-email). DMARC prevents spoofing examining a message's sender - the one that the user sees in their email client (in the examples above, this is service.outlook.com, outlook.com, and accountprotection.microsoft.com) - with the domain that passed SPF or DKIM. That is, the domain that the user sees has been authenticated and is therefore not spoofed. For a more complete discussion, see the section "*Understanding why email authentication is not always enough to stop spoofing"*  later on in this document.</span></span> 
  
<span data-ttu-id="1b1b7-p111">그러나 문제 레코드는 필요 하지 않은 선택 사항, 전자 메일 인증을 사용 하는. 따라서 강력한 인증 정책 사용 하 여 도메인을 선택 하는 동안 microsoft.com 및 skype.com 스푸핑, 약한 인증 정책 또는 정책이 없으면 전혀 게시, 위장 된 대상 도메인에서 보호 됩니다. 3 월 2018 이후로 Fortune 500에서 회사의 도메인의 9%만 강력한 전자 메일 인증 정책을 게시합니다. 나머지 91%는 phisher에 의해 위장 될 수 있습니다 하 고 전자 메일 필터를 감지 하지 않으면 다른 정책을 사용 하 여 최종 사용자에 게 전달 될 수 있습니다 하 속이기:</span><span class="sxs-lookup"><span data-stu-id="1b1b7-p111">However, the problem is that email authentication records are optional, not required. Therefore, while domains with strong authentication policies like microsoft.com and skype.com are protected from spoofing, domains that publish weaker authentication policies, or no policy at all, are targets for being spoofed.As of March 2018, only 9% of domains of companies in the Fortune 500 publish strong email authentication policies. The remaining 91% may be spoofed by a phisher, and unless the email filter detects it using another policy, may be delivered to an end user and deceive them:</span></span>
  
![Fortune 500 계열사 DMARC 정책](media/84e77d34-2073-4a8e-9f39-f109b32d06df.jpg)
  
<span data-ttu-id="1b1b7-144">수 있는 작은-중간 규모의 회사의 비율로 not 강력한 전자 메일 인증 정책을 게시 하는 Fortune 500에서이 고, 북미 및 서유럽 외부에 있는 도메인에 대해 여전히 작은 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b1b7-144">The proportion of small-to-medium sized companies that are not in the Fortune 500 that publish strong email authentication policies is smaller, and smaller still for domains that are outside of North America and western Europe.</span></span>
  
<span data-ttu-id="1b1b7-145">기업에서는 전자 메일 인증 작동 하는 방법에 대해 인식 하지 못할 수 있습니다, 하는 동안 피셔 수행을 이해 하 고는 부족을 활용 하기 때문에 중요 한 문제입니다.</span><span class="sxs-lookup"><span data-stu-id="1b1b7-145">This is a big problem because while enterprises may not be aware of how email authentication works, phishers do understand and take advantage of the lack of it.</span></span>
  
<span data-ttu-id="1b1b7-146">SPF, DKIM, 및 DMARC 설정에 대 한 정보를 섹션을 참조 하십시오. "이이 문서에서 나중에*고객의 Office 365"* 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b1b7-146">For information on setting up SPF, DKIM, and DMARC, see the section "*Customers of Office 365"*  later on in this document.</span></span> 
  
## <a name="stopping-spoofing-with-implicit-email-authentication"></a><span data-ttu-id="1b1b7-147">암시적 전자 메일 인증 스푸핑 중지</span><span class="sxs-lookup"><span data-stu-id="1b1b7-147">Stopping spoofing with implicit email authentication</span></span>

<span data-ttu-id="1b1b7-p112">피싱 및 창 피싱 이러한 문제가 발생 하 고 때문에 강력한 전자 메일 인증 정책 제한 채택으로 인해, Microsoft 고객을 보호 하는 기능에 대 한 투자를 계속 합니다. 따라서 *암시적 전자 메일 인증* -를 사용 하 여 Microsoft는 앞에 이동 하는 경우 도메인 인증 하지 않습니다 Microsoft 전자 메일 인증 레코드를 게시 했습니다 하는 경우에 따라 처리를 전달 하지 않습니다을 적절 하 게 취급 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b1b7-p112">Because phishing and spear phishing is such a problem, and because of the limited adoption of strong email authentication policies, Microsoft continues to invest in capabilities to protect its customers. Therefore, Microsoft is moving ahead with  *implicit email authentication* - if a domain doesn't authenticate, Microsoft will treat it as if it had published email authentication records and treat it accordingly if it doesn't pass.</span></span> 
  
<span data-ttu-id="1b1b7-p113">이를 위해 Microsoft에서는 보낸사람 신뢰도, 보낸사람/받는 사람 기록, 동작 분석 및 기타 고급 기술을 포함 하는 일반 전자 메일 인증에 대 한 다양 한 확장을 작성 합니다. 전자 메일 인증을 게시 하지는 도메인에서 보낸 메시지를 합법적인 임을 나타내는 신호 다른을 포함 하지 않으면 스푸핑으로 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1b1b7-p113">To accomplish this, Microsoft has built numerous extensions to regular email authentication including sender reputation, sender/recipient history, behavioral analysis, and other advanced techniques. A message sent from a domain that doesn't publish email authentication will be marked as spoof unless it contains other signals to indicate that it is legitimate.</span></span>
  
<span data-ttu-id="1b1b7-152">이렇게, 최종 사용자가 자신에 게 보내는 전자 메일 스푸핑 하지는 신뢰도 보낸 사람은 해당 도메인을 가장 하 고 아무도 값과 Office 365의 고객 가장 보호와 같은 더 나은 보호를 제공할 수 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1b1b7-152">By doing this, end users can have confidence that an email sent to them has not been spoofed, senders can be confident that nobody is impersonating their domain, and customers of Office 365 can offer even better protection such as Impersonation protection.</span></span>
  
<span data-ttu-id="1b1b7-153">Microsoft의 일반 알림 [A 해의 Phish 제 2 부-Office 365의 향상 된 방지 스푸핑](https://techcommunity.microsoft.com/t5/Security-Privacy-and-Compliance/Schooling-A-Sea-of-Phish-Part-2-Enhanced-Anti-spoofing/ba-p/176209)을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="1b1b7-153">To see Microsoft's general announcement, see [A Sea of Phish Part 2 - Enhanced Anti-spoofing in Office 365](https://techcommunity.microsoft.com/t5/Security-Privacy-and-Compliance/Schooling-A-Sea-of-Phish-Part-2-Enhanced-Anti-spoofing/ba-p/176209).</span></span>
  
## <a name="identifying-that-a-message-is-classified-as-spoofed"></a><span data-ttu-id="1b1b7-154">스푸핑으로 메시지 분류 된 식별</span><span class="sxs-lookup"><span data-stu-id="1b1b7-154">Identifying that a message is classified as spoofed</span></span>

### <a name="composite-authentication"></a><span data-ttu-id="1b1b7-155">복합 인증</span><span class="sxs-lookup"><span data-stu-id="1b1b7-155">Composite authentication</span></span>

<span data-ttu-id="1b1b7-p114">SPF, DKIM, 및 DMARC는 자신 하 여 모든 유용한, 하는 동안 이벤트는 이벤트에 메시지가 표시 되는 명시적 인증 레코드가 없는 충분 한 인증 상태를 통신 하지 않습니다. 따라서, Microsoft 줄여서 복합 인증 또는 compauth를 호출 하는 단일 값으로 여러 신호를 결합 하는 알고리즘을 개발 했습니다. Office 365의 고객 메시지 헤더에 *인증 결과* 헤더에 스탬프 처리 하는 compauth 값을 갖습니다.</span><span class="sxs-lookup"><span data-stu-id="1b1b7-p114">While SPF, DKIM, and DMARC are all useful by themselves, they don't communicate enough authentication status in the event a message has no explicit authentication records. Therefore, Microsoft has developed an algorithm that combines multiple signals into a single value called Composite Authentication, or compauth for short. Customers in Office 365 have compauth values stamped into the *Authentication-Results* header in the message headers.</span></span> 
  
```
Authentication-Results:
  compauth=<fail|pass|softpass|none> reason=<yyy>

```

|<span data-ttu-id="1b1b7-159">**CompAuth 결과**</span><span class="sxs-lookup"><span data-stu-id="1b1b7-159">**CompAuth result**</span></span>|<span data-ttu-id="1b1b7-160">**설명**</span><span class="sxs-lookup"><span data-stu-id="1b1b7-160">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="1b1b7-161">실패</span><span class="sxs-lookup"><span data-stu-id="1b1b7-161">fail</span></span>|<span data-ttu-id="1b1b7-162">메시지에 명시적 인증 하지 못했습니다 (보내는 도메인에에서 게시 된 레코드 명시적으로 DNS) 또는 암시적 인증 (도메인 게시 하지 않았습니다 레코드에서 DNS 레코드를 게시 했습니다 하는 경우 Office 365의 결과 삽입 하도록 보내기).</span><span class="sxs-lookup"><span data-stu-id="1b1b7-162">Message failed explicit authentication (sending domain published records explicitly in DNS) or implicit authentication (sending domain did not publish records in DNS, so Office 365 interpolated the result as if it had published records).</span></span>|
|<span data-ttu-id="1b1b7-163">전달</span><span class="sxs-lookup"><span data-stu-id="1b1b7-163">pass</span></span>|<span data-ttu-id="1b1b7-164">메시지 전달 명시적 인증 (메시지 전달 DMARC, 또는 [최상의 추측 전달 DMARC](https://blogs.msdn.microsoft.com/tzink/2015/05/06/what-is-dmarc-bestguesspass-in-office-365)) 또는 도메인 전자 메일 인증 레코드를 게시 하지 않습니다 했으나 Office 365에 강력한 백엔드 신호 높은 정확도와 암시적 인증 (보내기 이 메시지는 가능성이 나타내기 합법적인).</span><span class="sxs-lookup"><span data-stu-id="1b1b7-164">Message passed explicit authentication (message passed DMARC, or [Best Guess Passed DMARC](https://blogs.msdn.microsoft.com/tzink/2015/05/06/what-is-dmarc-bestguesspass-in-office-365)) or implicit authentication with high confidence (sending domain does not publish email authentication records, but Office 365 has strong backend signals to indicate the message is likely legitimate).</span></span>|
|<span data-ttu-id="1b1b7-165">softpass</span><span class="sxs-lookup"><span data-stu-id="1b1b7-165">softpass</span></span>|<span data-ttu-id="1b1b7-166">메시지 낮은-중간 안심할 수 있는 암시적 인증 전달 (도메인에 전자 메일 인증을 게시 하지 않습니다 했으나 Office 365 메시지 합법적인 이지만 신호 강도 약한 나타내려면 백엔드 신호를 보내는).</span><span class="sxs-lookup"><span data-stu-id="1b1b7-166">Message passed implicit authentication with low-to-medium confidence (sending domain does not publish email authentication, but Office 365 has backend signals to indicate the message is legitimate but the strength of the signal is weaker).</span></span>|
|<span data-ttu-id="1b1b7-167">없음</span><span class="sxs-lookup"><span data-stu-id="1b1b7-167">none</span></span>|<span data-ttu-id="1b1b7-168">메시지를 인증 하지 않았습니다 (또는 인증 않았습니다 하지만 정렬 되지 않은 것) 하지만 복합 인증 보낸사람 신뢰도 또는 기타 요인으로 인해 적용 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1b1b7-168">Message did not authenticate (or it did authenticate but did not align), but composite authentication not applied due to sender reputation or other factors.</span></span>|
   
|||
|:-----|:-----|
|<span data-ttu-id="1b1b7-169">**이유**</span><span class="sxs-lookup"><span data-stu-id="1b1b7-169">**Reason**</span></span>|<span data-ttu-id="1b1b7-170">**설명**</span><span class="sxs-lookup"><span data-stu-id="1b1b7-170">**Description**</span></span>|
|<span data-ttu-id="1b1b7-171">0xx</span><span class="sxs-lookup"><span data-stu-id="1b1b7-171">0xx</span></span>|<span data-ttu-id="1b1b7-172">메시지에는 복합 인증 하지 못했습니다.</span><span class="sxs-lookup"><span data-stu-id="1b1b7-172">Message failed composite authentication.</span></span><br/><span data-ttu-id="1b1b7-173">**000** 메시지에는 다른 작업을 거부 또는 격리의 DMARC 실패 한 것을 의미 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b1b7-173">**000** means the message failed DMARC with an action of reject or quarantine.</span></span>  <br/><span data-ttu-id="1b1b7-p115">**001** 이면 메시지 암시적 전자 메일 인증에 실패 합니다. 즉, 보내는 도메인에서 전자 메일 인증 레코드를 게시 하지 않았습니다 또는 약한 오류 정책 사용 했던 문제가 있었다면 (SPF 소프트 실패 또는 중립, DMARC 정책 p = 없음).</span><span class="sxs-lookup"><span data-stu-id="1b1b7-p115">**001** means the message failed implicit email authentication. This means that the sending domain did not have email authentication records published, or if they did, they had a weaker failure policy (SPF soft fail or neutral, DMARC policy of p=none).  </span></span><br/><span data-ttu-id="1b1b7-176">조직에 위장 된 전자 메일을 발송에서 명시적으로 금지 된 보낸사람/도메인 쌍에 대 한 정책을 **002** 의미,이 설정은 관리자가 설정 수동으로 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1b1b7-176">**002** means the organization has a policy for the sender/domain pair that is explicitly prohibited from sending spoofed email, this setting is manually set by an administrator.</span></span>  <br/><span data-ttu-id="1b1b7-177">메시지는 다른 작업을 거부 또는 격리의 DMARC 실패 하 고 보내는 도메인을 사용 하면 조직의 허용 도메인 중 하나가 **010** 의미 (자체를 자체 또는 조직 내의 일부인이 스푸핑).</span><span class="sxs-lookup"><span data-stu-id="1b1b7-177">**010** means the message failed DMARC with an action of reject or quarantine, and the sending domain is one of your organization's accepted-domains (this is part of self-to-self, or intra-org, spoofing).</span></span>  <br/><span data-ttu-id="1b1b7-178">**011** 의미는 메시지가 암시적 전자 메일 인증 실패 하 고 보내는 도메인을 사용 하면 조직의 허용된 도메인 중 하나가 (자체를 자체 또는 조직 내의 일부인이 스푸핑).</span><span class="sxs-lookup"><span data-stu-id="1b1b7-178">**011** means the message failed implicit email authentication, and the sending domain is one of your organization's accepted domains (this is part of self-to-self, or intra-org, spoofing).</span></span>|
|<span data-ttu-id="1b1b7-179">다른 모든 코드 (1xx, 2xx, 3xx, 4xx, 5xx)</span><span class="sxs-lookup"><span data-stu-id="1b1b7-179">All other codes (1xx, 2xx, 3xx, 4xx, 5xx)</span></span>|<span data-ttu-id="1b1b7-180">아무 작업도 적용 된 메시지를 전달 되는 암시적 인증 또는 없음 인증 명의 있는데 이유는 다양 한 내부 코드 (영문)에 해당 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b1b7-180">Corresponds to various internal codes for why a message passed implicit authentication, or had no authentication but no action was applied.</span></span>|
   
<span data-ttu-id="1b1b7-181">메시지 헤더 봐서는 관리자 또는 최종 사용자를 확인할 수 Office 365 보낸을 스푸핑 될 수 있습니다 결론에 도착 하는 방법.</span><span class="sxs-lookup"><span data-stu-id="1b1b7-181">By looking at the headers of a message, an administrator or even an end user can determine how Office 365 arrives at the conclusion that the sender may be spoofed.</span></span>
  
### <a name="differentiating-between-different-types-of-spoofing"></a><span data-ttu-id="1b1b7-182">다양 한 유형의 스푸핑 구별</span><span class="sxs-lookup"><span data-stu-id="1b1b7-182">Differentiating between different types of spoofing</span></span>

<span data-ttu-id="1b1b7-183">Microsoft 두 다양 한 유형의 메시지를 스푸핑 구분해 서 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b1b7-183">Microsoft differentiates between two different types of spoofing messages:</span></span>
  
 <span data-ttu-id="1b1b7-184">**조직 내 스푸핑**</span><span class="sxs-lookup"><span data-stu-id="1b1b7-184">**Intra-org spoofing**</span></span>
  
<span data-ttu-id="1b1b7-185">로 알려져 자체를 자체 스푸핑, 발생이 때 from에서 도메인: 주소와 동일 또는 (도메인이 있는 경우 받는 사람 조직의 [허용 도메인](https://technet.microsoft.com/en-us/library/jj945194%28v=exchg.150%29.aspx)중 하나) 도메인의 받는 사람;에 맞춥니다 또는 때 from에서 도메인: 주소는 동일한 조직에 속해 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1b1b7-185">Also known as self-to-self spoofing, this occurs when the domain in the From: address is the same as, or aligns with, the recipient domain (when recipient domain is one of your organization's [Accepted Domains](https://technet.microsoft.com/en-us/library/jj945194%28v=exchg.150%29.aspx)); or, when the domain in the From: address is part of the same organization.</span></span>
  
<span data-ttu-id="1b1b7-p116">예, 다음에 보낸사람 및 받는 사람 같은 도메인 (contoso.com)에서 있습니다. 공백은 삽입 될이 페이지에 spambot harvesting 방지 하기 위해 전자 메일 주소):</span><span class="sxs-lookup"><span data-stu-id="1b1b7-p116">For example, the following has sender and recipient from the same domain (contoso.com). Spaces are inserted into the email address to prevent spambot harvesting on this page):</span></span>
  
<span data-ttu-id="1b1b7-188">@ Contoso.com:에서 보낸사람</span><span class="sxs-lookup"><span data-stu-id="1b1b7-188">From: sender @ contoso.com</span></span>
  
<span data-ttu-id="1b1b7-189">Contoso.com @ 받는 사람: 받는 사람</span><span class="sxs-lookup"><span data-stu-id="1b1b7-189">To: recipient @ contoso.com</span></span>
  
<span data-ttu-id="1b1b7-190">다음에 조직 도메인 (fabrikam.com)와 조율 보낸사람 및 받는 사람 도메인 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1b1b7-190">The following has the sender and recipient domains aligning with the organizational domain (fabrikam.com):</span></span>
  
<span data-ttu-id="1b1b7-191">Foo.fabrikam.com @:에서 보낸사람</span><span class="sxs-lookup"><span data-stu-id="1b1b7-191">From: sender @ foo.fabrikam.com</span></span>
  
<span data-ttu-id="1b1b7-192">받는 사람: 받는 사람 bar.fabrikam.com @</span><span class="sxs-lookup"><span data-stu-id="1b1b7-192">To: recipient @ bar.fabrikam.com</span></span>
  
<span data-ttu-id="1b1b7-193">다음은 보낸사람 및 받는 사람 도메인은 서로 다른 (microsoft.com 및 반응을) 있지만 동일한 조직에 속한 (즉, 모두의 일부인 조직의 허용 도메인):</span><span class="sxs-lookup"><span data-stu-id="1b1b7-193">The following sender and recipient domains are different (microsoft.com and bing.com), but they belong to the same organization (that is, both are part of the organization's Accepted Domains):</span></span>
  
<span data-ttu-id="1b1b7-194">Microsoft.com @:에서 보낸사람</span><span class="sxs-lookup"><span data-stu-id="1b1b7-194">From: sender @ microsoft.com</span></span>
  
<span data-ttu-id="1b1b7-195">받는 사람: 받는 사람 반응 @</span><span class="sxs-lookup"><span data-stu-id="1b1b7-195">To: recipient @ bing.com</span></span>
  
<span data-ttu-id="1b1b7-196">조직 내 스푸핑 실패 하는 메시지 헤더에 다음 값이 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b1b7-196">Messages that fail intra-org spoofing contain the following values in the headers:</span></span>
  
<span data-ttu-id="1b1b7-197">X-Forefront-스팸 방지-보고서:... CAT:SPM/HSPM/PHSH;... SFTY:9.11</span><span class="sxs-lookup"><span data-stu-id="1b1b7-197">X-Forefront-Antispam-Report: ...CAT:SPM/HSPM/PHSH;...SFTY:9.11</span></span>
  
<span data-ttu-id="1b1b7-198">고양이 메시지의 범주 및 SPM (스팸)으로 스탬프 처리 정상적으로 이지만 필요에 따라 발생할 수 있습니다 (높은 정확도 스팸) HSPM 수 또는 PHISH (피싱) 어떤 다른 따라 패턴 유형의 메시지에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1b1b7-198">The CAT is the category of the message, and it is normally stamped as SPM (spam), but occasionally may be HSPM (high confidence spam) or PHISH (phishing) depending upon what other types of patterns occur in the message.</span></span>
  
<span data-ttu-id="1b1b7-199">SFTY은 메시지의 보안 수준, 첫번째 자리 숫자 (9) 의미는 메시지는 피싱, 및 자릿수 것을 의미 하는 점 (11) 한 후 두 번째 집합은 조직 내 스푸핑 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b1b7-199">The SFTY is the safety level of the message, the first digit (9) means the message is phishing, and second set of digits after the dot (11) means it is intra-org spoofing.</span></span>
  
<span data-ttu-id="1b1b7-200">복합 인증에 대 한 조직 내 스푸핑, 2018 (아직 정의 되지 않은 시간 표시 막대)의 뒷부분에 나오는 스탬프가 지정 된 수에 대 한 특별 한 이유가 코드가 없는 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b1b7-200">There is no specific reason code for Composite Authentication for intra-org spoofing, that will be stamped later in 2018 (timeline not yet defined).</span></span>
  
 <span data-ttu-id="1b1b7-201">**도메인간 스푸핑**</span><span class="sxs-lookup"><span data-stu-id="1b1b7-201">**Cross-domain spoofing**</span></span>
  
<span data-ttu-id="1b1b7-p117">이 문제가 발생 때 from에서을 보내는 도메인: 주소를 받는 조직 외부 도메인은 합니다. 도메인간 스푸핑으로 인해 복합 인증에 실패 하는 메시지 헤더에 다음 값이 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b1b7-p117">This occurs when the sending domain in the From: address is an external domain to the receiving organization. Messages that fail Composite Authentication due to cross-domain spoofing contain the following values in the headers:</span></span>
  
<span data-ttu-id="1b1b7-p118">인증-결과:... compauth 실패 이유 = 000/001 =</span><span class="sxs-lookup"><span data-stu-id="1b1b7-p118">Authentication-Results: … compauth=fail reason=000/001</span></span>
  
<span data-ttu-id="1b1b7-206">X-Forefront-스팸 방지-보고서:... CAT:SPOOF;... SFTY:9.22</span><span class="sxs-lookup"><span data-stu-id="1b1b7-206">X-Forefront-Antispam-Report: ...CAT:SPOOF;...SFTY:9.22</span></span>
  
<span data-ttu-id="1b1b7-207">두 경우 모두 다음 빨간색 안전 팁은, 메시지 또는 받는 사람 사서함의 언어를 사용자 지정 된 동일한 스탬프 처리:</span><span class="sxs-lookup"><span data-stu-id="1b1b7-207">In both cases, the following red safety tip is stamped in the message, or an equivalent that is customized to the recipient mailbox's language:</span></span>
  
![빨간색 안전 팁-사기 감지](media/a366156a-14e8-4c14-bfe5-2031b21936f8.jpg)
  
<span data-ttu-id="1b1b7-209">만 봐서는 From은: 주소 및 받는 사람 전자 메일 이란, 파악 하거나 하 여 조직 내 및 도메인간 스푸핑 구분할 수 있는 전자 메일 머리글를 검사 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b1b7-209">It's only by looking at the From: address and knowing what your recipient email is, or by inspecting the email headers, that you can differentiate between intra-org and cross-domain spoofing.</span></span>
  
## <a name="how-customers-of-office-365-can-prepare-themselves-for-the-new-anti-spoofing-protection"></a><span data-ttu-id="1b1b7-210">Office 365의 고객 수 준비 방법을 직접 새 스푸핑 방지 보호에 대 한</span><span class="sxs-lookup"><span data-stu-id="1b1b7-210">How customers of Office 365 can prepare themselves for the new anti-spoofing protection</span></span>

### <a name="information-for-administrators"></a><span data-ttu-id="1b1b7-211">관리자를 위한 정보</span><span class="sxs-lookup"><span data-stu-id="1b1b7-211">Information for administrators</span></span>

<span data-ttu-id="1b1b7-212">Office 365에서 조직 관리자로 알고 있어야 하는 정보의 몇 가지 핵심 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1b1b7-212">As an administrator of an organization in Office 365, there are several key pieces of information you should be aware of.</span></span>
  
### <a name="understanding-why-email-authentication-is-not-always-enough-to-stop-spoofing"></a><span data-ttu-id="1b1b7-213">전자 메일 인증 없는 이유 항상 스푸핑 중지 하기에 충분 이해</span><span class="sxs-lookup"><span data-stu-id="1b1b7-213">Understanding why email authentication is not always enough to stop spoofing</span></span>

<span data-ttu-id="1b1b7-p119">새 스푸핑 방지 보호 (SPF, DKIM, 및 DMARC) 하지 스푸핑으로 메시지를 표시 하려면 전자 메일 인증에 의존 합니다. 일반적인 예로 보내는 도메인 SPF 레코드를 게시 하지 않았으므로 때 수 있습니다. SPF 레코드가 없는 하거나는 올바르게 설정 하지 않으면 Microsoft에는 메시지는 합법적인 없다는 백엔드 인텔리전스 없으면 스푸핑으로 보낸된 메시지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1b1b7-p119">The new anti-spoofing protection relies on email authentication (SPF, DKIM, and DMARC) to not mark a message as spoofing. A common example is when a sending domain has never published SPF records. If there are no SPF records or they are incorrectly set up, a sent message will be marked as spoofed unless Microsoft has back-end intelligence that says the message is legitimate.</span></span>
  
<span data-ttu-id="1b1b7-217">등 스푸핑 방지 배포 되 고, 하기 전에 메시지 없는 SPF 레코드, DKIM 레코드가 없으면 및 DMARC 레코드가 없으면 다음과 같은 소개한 수 있습니다.:</span><span class="sxs-lookup"><span data-stu-id="1b1b7-217">For example, prior to anti-spoofing being deployed, a message may have looked like the following with no SPF record, no DKIM record, and no DMARC record:</span></span> 
  
```
Authentication-Results: spf=none (sender IP is 1.2.3.4)
  smtp.mailfrom=example.com; contoso.com; dkim=none
  (message not signed) header.d=none; contoso.com; dmarc=none
  action=none header.from=example.com;
From: sender @ example.com
To: receiver @ contoso.com
```
<span data-ttu-id="1b1b7-218">스푸핑 방지 후 Office 365 엔터프라이즈 e 5, EOP, 또는 ATP, 있는 경우 compauth 값은 스탬프 처리 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b1b7-218">After anti-spoofing, if you have Office 365 Enterprise E5, EOP, or ATP, the compauth value is stamped:</span></span>
  
```
Authentication-Results: spf=none (sender IP is 1.2.3.4)
  smtp.mailfrom=example.com; contoso.com; dkim=none
  (message not signed) header.d=none; contoso.com; dmarc=none
  action=none header.from=example.com; compauth=fail reason=001
From: sender @ example.com
To: receiver @ contoso.com

```

<span data-ttu-id="1b1b7-219">Example.com SPF 레코드를 삽입 했지만 DKIM 레코드가 아닙니다.을 설정 하 여이 고정을 하는 경우이 인증을 통과 복합 SPF를 전달 하는 도메인에서에서 도메인에 맞춰집니다 때문에: 주소:</span><span class="sxs-lookup"><span data-stu-id="1b1b7-219">If example.com fixed this by setting up an SPF record but not a DKIM record, this would pass composite authentication because the domain that passed SPF aligned with the domain in the From: address:</span></span> 
  
```
Authentication-Results: spf=pass (sender IP is 1.2.3.4)
  smtp.mailfrom=example.com; contoso.com; dkim=none
  (message not signed) header.d=none; contoso.com; dmarc=bestguesspass
  action=none header.from=example.com; compauth=pass reason=109
From: sender @ example.com
To: receiver @ contoso.com
```

<span data-ttu-id="1b1b7-220">속성이 DKIM 레코드가 삭제 되었지만 SPF 레코드를 설정 하는 경우이 인증을 통과 복합 전달 하는 DKIM 서명에서 도메인에서에서 도메인에 맞춰집니다 때문에 또는: 주소:</span><span class="sxs-lookup"><span data-stu-id="1b1b7-220">Or, if they set up a DKIM record but not an SPF record, this would also pass composite authentication because the domain in the DKIM-Signature that passed aligned with the domain in the From: address:</span></span> 
  
```
Authentication-Results: spf=none (sender IP is 1.2.3.4)
  smtp.mailfrom=example.com; contoso.com; dkim=pass
  (signature was verified) header.d=outbound.example.com;
  contoso.com; dmarc=bestguesspass action=none
  header.from=example.com; compauth=pass reason=109
From: sender @ example.com
To: receiver @ contoso.com
```

<span data-ttu-id="1b1b7-p120">phisher 될 수 있습니다도 SPF 및 DKIM를 설정 하 고 자신의 도메인을 사용 하 여 메시지에 서명 하지만 From에서 다른 도메인을 지정: 주소입니다. SPF 아니고 DKIM 필요는 도메인에서에서 도메인에 맞춰: example.com DMARC 레코드를 게시 하지 않으면이 것으로 표시할 수 DMARC를 사용 하 여 스푸핑 있으므로 주소:</span><span class="sxs-lookup"><span data-stu-id="1b1b7-p120">However, a phisher may also set up SPF and DKIM and sign the message with their own domain, but specify a different domain in the From: address. Neither SPF nor DKIM requires the domain to align with the domain in the From: address, so unless example.com published DMARC records, this would not be marked as a spoof using DMARC:</span></span> 
  
```
Authentication-Results: spf=pass (sender IP is 5.6.7.8)
  smtp.mailfrom=maliciousDomain.com; contoso.com; dkim=pass
  (signature was verified) header.d=maliciousDomain.com;
  contoso.com; dmarc=none action=none header.from=example.com;
From: sender @ example.com
To: receiver @ contoso.com
```

<span data-ttu-id="1b1b7-223">전자 메일 클라이언트 (Outlook, 웹, 또는 다른 전자 메일 클라이언트에서 Outlook), From만: 도메인 표시 되 면에는 SPF 또는 DKIM, 속하고 도메인이 아닌 메시지 example.com에서 제공 하지만 실제로 maliciousDomain.com에서 가져온에 답변에 사용자를 판단할 수 있습니다 .</span><span class="sxs-lookup"><span data-stu-id="1b1b7-223">In the email client (Outlook, Outlook on the web, or any other email client), only the From: domain is displayed, not the domain in the SPF or DKIM, and that can mislead the user into thinking the message came from example.com, but actually came from maliciousDomain.com.</span></span>
  
![인증 된 메시지에서 하지만: 도메인 SPF 또는 DKIM 전달 하는 된와 일치 하지 않습니다](media/a9b5ab2a-dfd3-47c6-8ee8-e3dab2fae528.jpg)
  
<span data-ttu-id="1b1b7-p121">Office 365 필요는 이런 이유로 from에서 도메인: 주소 SPF 또는 DKIM 서명에서 도메인으로 정렬 하 고 메시지는 합법적인 하 고 있음을 나타내는 일부 다른 내부 신호를 포함 하지, 하는 경우. 그렇지 않은 경우 메시지 compauth 실패 한 것입니다.</span><span class="sxs-lookup"><span data-stu-id="1b1b7-p121">For that reason, Office 365 requires that the domain in the From: address aligns with the domain in the SPF or DKIM signature, and if it doesn't, contains some other internal signals that indicates that the message is legitimate. Otherwise, the message would be a compauth fail.</span></span> 
  
```
Authentication-Results: spf=none (sender IP is 5.6.7.8)
  smtp.mailfrom=maliciousDomain.com; contoso.com; dkim=pass
  (signature was verified) header.d=maliciousDomain.com;
  contoso.com; dmarc=none action=none header.from=contoso.com;
  compauth=fail reason=001
From: sender@contoso.com
To: someone@example.com
```

<span data-ttu-id="1b1b7-p122">따라서 Office 365 스푸핑 방지 보호 하는 없는 인증을 사용 하면 도메인에 대해 및 인증 하지만 from에서 도메인에 대해 불일치를 설정 하는 도메인에 대해: 주소 즉 같이 다른 사용자에 게 표시 하 고 생각 되는 메시지를 보낸 사람이 합니다. 모두 해당 조직의 외부에 도메인 조직 내에서 도메인의 마찬가지입니다.</span><span class="sxs-lookup"><span data-stu-id="1b1b7-p122">Thus, Office 365 anti-spoofing protects against domains with no authentication, and against domains who set up authentication but mismatch against the domain in the From: address as that is the one that the user sees and believes is the sender of the message. This is true both of domains external to your organization, as well as domains within your organization.</span></span>
  
<span data-ttu-id="1b1b7-229">따라서 것으로 표시 되며, 스푸핑 SPF 및 DKIM는 메시지를 전달 하는 경우에 및 복합 인증 실패 하 여 메시지를 받지 못하도록 하는 경우 있기 때문에 SPF 및 DKIM를 통과 하는 도메인에서에서 도메인으로 정렬 되지 않습니다: 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="1b1b7-229">Therefore, if you ever receive a message that failed composite authentication and is marked as spoofed, even though the message passed SPF and DKIM, it's because the domain that passed SPF and DKIM are not aligned with the domain in the From: address.</span></span>
  
### <a name="understanding-changes-in-how-spoofed-emails-are-treated"></a><span data-ttu-id="1b1b7-230">어떻게 위장 된 전자 메일에서 이해 변경 내용은 처리</span><span class="sxs-lookup"><span data-stu-id="1b1b7-230">Understanding changes in how spoofed emails are treated</span></span>

<span data-ttu-id="1b1b7-p123">현재 Office 365-모든 조직에 대 한 ATP 및 비-ATP-메시지를 거부 또는 격리의 정책 사용 하 여 DMARC에 스팸 및 일반적으로 지수가 높은 스팸 동작 또는 경우에 따라 일반 스팸 동작을 수행 하는 것으로 표시 되는 실패 하는 (여부에 따라 다른 스팸 규칙 먼저로 식별할 스팸). 조직 내 스푸핑 감지 된 일반 스팸 작업을 수행 합니다. 이 동작을 사용 하도록 설정 하지 않아도 것을 비활성화할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1b1b7-p123">Currently, for all organizations in Office 365 - ATP and non-ATP - messages that fail DMARC with a policy of reject or quarantine are marked as spam and usually take the high confidence spam action, or sometimes the regular spam action (depending on whether other spam rules first identify it as spam). Intra-org spoof detections take the regular spam action. This behavior does not need to be enabled, nor can it be disabled.</span></span>
  
<span data-ttu-id="1b1b7-p124">그러나 도메인간 스푸핑 메시지에 대 한이 변경 하기 전에 일반 스팸, phish, 및 맬웨어 검사를 통과 있으며 필터의 다른 부분, 의심 스러운으로 식별 하는 경우 것으로 표시할 스팸, phish, 또는 맬웨어 각각. 새 도메인간 스푸핑 보호와 인증할 수 없는 모든 메시지에서, 기본적으로 작업을 수행 피싱 방지에 정의 된 \> 백신 스푸핑 정책입니다. 정의 되지 않은 경우 사용자가 정크 메일 폴더로 이동 됩니다. 경우에 따라 더 의심 스러운 메시지는 메시지에 추가 된 빨간색 안전 팁도를 갖습니다.</span><span class="sxs-lookup"><span data-stu-id="1b1b7-p124">However, for cross-domain spoofing messages, before this change they would go through regular spam, phish, and malware checks and if other parts of the filter identified them as suspicious, would mark them as spam, phish, or malware respectively. With the new cross-domain spoofing protection, any message that can't be authenticated will, by default, take the action defined in the Anti-phishing \> Anti-spoofing policy. If one is not defined, it will be moved to a users Junk Email folder. In some cases, more suspicious messages will also have the red safety tip added to the message.</span></span>
  
<span data-ttu-id="1b1b7-p125">여전히 시작로 표시 된 스팸 있지만 빨간색 안전 팁;도 이제는 스팸으로 이전에 표시 된 일부 메시지에 발생할 수 있습니다. 또 어떤 경우에는 스팸이 아닌가 시작 된 것으로 표시 빨간색 안전 팁이 있는 (CAT:SPOOF) 스팸으로으로 이전에 표시 된 메시지 추가 되었습니다. 다른 경우에 모든 스팸 및 phish 격리로 이동 된 고객은 이제 볼 정크 메일 폴더로 일어나 고 있어 (이 동작을 변경할 수 있습니다, [스푸핑 방지 설정 변경](#changing-your-anti-spoofing-settings)을 참조).</span><span class="sxs-lookup"><span data-stu-id="1b1b7-p125">This may result in some messages that were previously marked as spam still getting marked as spam but will now also have a red safety tip; in other cases, messages that were previously marked as non-spam will start getting marked as spam (CAT:SPOOF) with a red safety tip added. In still other cases, customers that were moving all spam and phish to the quarantine would now see them going to the Junk Mail Folder (this behavior can be changed, see [Changing your anti-spoofing settings](#changing-your-anti-spoofing-settings)).</span></span>
  
<span data-ttu-id="1b1b7-p126">여러 다른 방식 (이 문서 앞부분의 [다양 한 유형의 스푸핑 간의 Differentiating](#differentiating-between-different-types-of-spoofing) 참조)는 메시지를 스푸핑 될 수 있지만 년 3 월 2018를 기준으로 Office 365에서 이러한 메시지를 처리 하는 방법은 되지 아직 통합 합니다. 다음 표에 새 동작 되 고 도메인간 스푸핑 보호와 요약 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b1b7-p126">There are multiple different ways a message can be spoofed (see  [Differentiating between different types of spoofing](#differentiating-between-different-types-of-spoofing) earlier in this article) but as of March 2018 the way Office 365 treats these messages is not yet unified. The following table is a quick summary, with Cross-domain spoofing protection being new behavior:</span></span> 
  
|<span data-ttu-id="1b1b7-242">**스푸핑의 유형**</span><span class="sxs-lookup"><span data-stu-id="1b1b7-242">**Type of spoof**</span></span>|<span data-ttu-id="1b1b7-243">**종류**</span><span class="sxs-lookup"><span data-stu-id="1b1b7-243">**Category**</span></span>|<span data-ttu-id="1b1b7-244">**안전 팁 추가 합니까?**</span><span class="sxs-lookup"><span data-stu-id="1b1b7-244">**Safety tip added?**</span></span>|<span data-ttu-id="1b1b7-245">**적용 대상**</span><span class="sxs-lookup"><span data-stu-id="1b1b7-245">**Applies to**</span></span>|
|:-----|:-----|:-----|:-----|
|<span data-ttu-id="1b1b7-246">DMARC 실패 (격리 또는 거부)</span><span class="sxs-lookup"><span data-stu-id="1b1b7-246">DMARC fail (quarantine or reject)</span></span>  <br/> |<span data-ttu-id="1b1b7-247">SPM 또는 PHSH에도 HSPM (기본값) 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1b1b7-247">HSPM (default), may also be SPM or PHSH</span></span>  <br/> |<span data-ttu-id="1b1b7-248">아니요 (아직)</span><span class="sxs-lookup"><span data-stu-id="1b1b7-248">No (not yet)</span></span>  <br/> |<span data-ttu-id="1b1b7-249">모든 Office 365 고객, Outlook.com</span><span class="sxs-lookup"><span data-stu-id="1b1b7-249">All Office 365 customers, Outlook.com</span></span>  <br/> |
|<span data-ttu-id="1b1b7-250">자체를 자체</span><span class="sxs-lookup"><span data-stu-id="1b1b7-250">Self-to-self</span></span>  <br/> |<span data-ttu-id="1b1b7-251">SPM</span><span class="sxs-lookup"><span data-stu-id="1b1b7-251">SPM</span></span>  <br/> |<span data-ttu-id="1b1b7-252">예</span><span class="sxs-lookup"><span data-stu-id="1b1b7-252">Yes</span></span>  <br/> |<span data-ttu-id="1b1b7-253">모든 Office 365 조직, Outlook.com</span><span class="sxs-lookup"><span data-stu-id="1b1b7-253">All Office 365 organizations, Outlook.com</span></span>  <br/> |
|<span data-ttu-id="1b1b7-254">도메인간</span><span class="sxs-lookup"><span data-stu-id="1b1b7-254">Cross-domain</span></span>  <br/> |<span data-ttu-id="1b1b7-255">스푸핑</span><span class="sxs-lookup"><span data-stu-id="1b1b7-255">SPOOF</span></span>  <br/> |<span data-ttu-id="1b1b7-256">예</span><span class="sxs-lookup"><span data-stu-id="1b1b7-256">Yes</span></span>  <br/> |<span data-ttu-id="1b1b7-257">Office 365 고급 위협 보호 및 e 5 고객</span><span class="sxs-lookup"><span data-stu-id="1b1b7-257">Office 365 Advanced Threat Protection and E5 customers</span></span>  <br/> |
   
### <a name="changing-your-anti-spoofing-settings"></a><span data-ttu-id="1b1b7-258">스푸핑 방지 설정 변경</span><span class="sxs-lookup"><span data-stu-id="1b1b7-258">Changing your anti-spoofing settings</span></span>

<span data-ttu-id="1b1b7-p127">피싱 방지로 이동를 만들거나 (도메인간) 스푸핑 방지 설정 업데이트 \> 위협 관리에서 설정 스푸핑 방지 \> 보안에서 정책 탭 &amp; 준수 센터입니다. 모든 피싱 방지 설정 하지 만들었으면 만들 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b1b7-p127">To create or update your (cross-domain) anti-spoofing settings, navigate to the Anti-phishing \> Anti-spoofing settings under the Threat Management \> Policy tab in the Security &amp; Compliance Center. If you have never created any anti-phishing settings, you will need to create one:</span></span>
  
![피싱 방지-새 정책 만들기](media/9337ec91-270e-4fa7-9dfa-a51a2d1eb95e.jpg)
  
<span data-ttu-id="1b1b7-262">이미 만든 경우 하나를 수정 하도록 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1b1b7-262">If you've already created one, you can select it to modify it:</span></span>
  
![피싱 방지-기존 정책 수정](media/75457a7c-882e-4984-80d1-21a12b42c53a.jpg)
  
<span data-ttu-id="1b1b7-264">방금 만든 정책을 선택 하 고에서 설명한 대로 하는 단계를 진행 [스푸핑 인텔리전스에 대 한 자세히 알아보기.](https://support.office.com/article/Learn-more-about-spoof-intelligence-978c3173-3578-4286-aaf4-8a10951978bf)</span><span class="sxs-lookup"><span data-stu-id="1b1b7-264">Select the policy you just created and proceed through the steps as described on [Learn More about Spoof Intelligence.](https://support.office.com/article/Learn-more-about-spoof-intelligence-978c3173-3578-4286-aaf4-8a10951978bf)</span></span>
  
![사용 하도록 설정 하거나 antispoofing를 사용 하지 않도록 설정](media/c49e2147-c954-443c-9144-1cbd139e1166.jpg)
  
![사용 하도록 설정 하거나 antispoofing 안전 팁을 사용 하지 않도록 설정](media/eec7c407-31fc-4f73-8325-307d82d1fb53.jpg)
  
<span data-ttu-id="1b1b7-267">PowerShell 통해 새 정책을 만들려면:</span><span class="sxs-lookup"><span data-stu-id="1b1b7-267">To create a new policy via PowerShell:</span></span> 
  
```
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

<span data-ttu-id="1b1b7-p128">그런 다음 [집합 AntiphishPolicy](https://docs.microsoft.com/powershell/module/exchange/advanced-threat-protection/Set-AntiPhishPolicy?view=exchange-ps)에서 설명서에 따라 PowerShell을 사용 하 여 피싱 방지 정책 매개 변수를 수정할 수 있습니다. 매개 변수로 $name를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1b1b7-p128">You may then modify the anti-phishing policy parameters using PowerShell, following the documentation at [Set-AntiphishPolicy](https://docs.microsoft.com/powershell/module/exchange/advanced-threat-protection/Set-AntiPhishPolicy?view=exchange-ps). You may specify the $name as a parameter:</span></span>
  
```
Set-AntiphishPolicy -Identity $name <fill in rest of parameters>
```

<span data-ttu-id="1b1b7-270">2018의 뒷부분에 나오는 하면 기본 정책을 만들 수 있는 것이 아닌 하나 만들어질 하므로 수동으로 지정할 필요가 없습니다 조직에서 모든 받는 사람에 게 범위가 지정 된 있습니다 (아래 스크린샷이 최종 구현 하기 전에 변경 될 수)입니다.</span><span class="sxs-lookup"><span data-stu-id="1b1b7-270">Later in 2018, rather than you having to create a default policy, one will be created for you that is scoped to all the recipients in your organization so you don't have to specify it manually (the screenshots below are subject to change before the final implementation).</span></span>
  
![피싱 방지에 대 한 기본 정책](media/1f27a0bf-e202-4e12-bbac-24baf013c8f9.jpg)
  
<span data-ttu-id="1b1b7-272">만든 정책와는 달리 기본 정책을 삭제할 해당 우선순위를 수정 하거나 선택 하는 사용자, 도메인 또는 그룹에 범위를 지정 하 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="1b1b7-272">Unlike a policy that you create, you cannot delete the default policy, modify its priority, or choose which users, domains, or groups to scope it to.</span></span>
  
![피싱 방지 기본 정책 세부 정보](media/30c21ceb-df52-4c93-aa65-f44a55dc1009.jpg)
  
<span data-ttu-id="1b1b7-274">PowerShell 통해 기본 보호를 설정 하려면:</span><span class="sxs-lookup"><span data-stu-id="1b1b7-274">To set up your default protection via PowerShell:</span></span>
  
```
$defaultAntiphishPolicy = Get-AntiphishPolicy | ? {$_.IsDefault -eq $true}
Set-AntiphishPolicy -Identity $defaultAntiphishPolicy.Name -EnableAntispoofEnforcement <$true|$false>
```

<span data-ttu-id="1b1b7-275">다른 메일 서버 또는 서버 Office 365 앞에 있는 경우에 스푸핑 방지 보호를 해제 해야 (자세한 내용은 스푸핑 방지를 사용 하지 않도록 설정 하는 합법적인 시나리오 참조).</span><span class="sxs-lookup"><span data-stu-id="1b1b7-275">You should only disable anti-spoofing protection if you have another mail server or servers in front of Office 365 (see Legitimate scenarios to disable anti-spoofing for more details).</span></span> 
  
```
$defaultAntiphishPolicy = Get-AntiphishiPolicy | ? {$_.IsDefault $true}
Set-AntiphishPolicy -Identity $defaultAntiphishPolicy.Name -EnableAntispoofEnforcement $false 

```
> [!IMPORTANT]
> <span data-ttu-id="1b1b7-p129">전자 메일 경로에 있는 첫번째 홉은 Office 365 스푸핑으로 표시 되는 너무 많은 경우 합법적인 전자 메일을 액세스 하는 경우 먼저 설정 해야 위장 된 전자 메일을 보낼 사용자의 도메인에 허용 되는 대화 보낸사람 ( *"관리 합법적인 보낸사람 에게만 u 보내는 섹션을 참조 하십시오. nauthenticated 전자 메일"* ). 너무 많은 경우 가양성 액세스 하는 경우 (예: 스푸핑으로 표시 된 메시지 합법적) 스푸핑 방지 보호를 전혀 사용 하지 않도록 설정 하지 않는 것이 좋습니다. 대신, 높은 보호 하는 대신 기본을 선택 하는 것이 좋습니다.                    노출 장기간에 훨씬 더 높은 비용 부과 될 수 있는 위장 된 전자 메일을 조직에 보다 가양성을 통해 작동 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="1b1b7-p129">If the first hop in your email path is Office 365, and you are getting too many legitimate emails marked as spoof, you should first set up your senders that are allowed to send spoofed email to your domain (see the section  *"Managing legitimate senders who are sending unauthenticated email"*  ). If you are still getting too many false positives (e.g., legitimate messages marked as spoof), we do NOT recommend disabling anti-spoofing protection altogether. Instead, we recommend choosing Basic instead of High protection.                    It is better to work through false positives than to expose your organization to spoofed email which could end up imposing significantly higher costs in the long term.</span></span>

### <a name="managing-legitimate-senders-who-are-sending-unauthenticated-email"></a><span data-ttu-id="1b1b7-280">인증 되지 않은 전자 메일을 발송 하 게 합법적으로 보낸사람 관리</span><span class="sxs-lookup"><span data-stu-id="1b1b7-280">Managing legitimate senders who are sending unauthenticated email</span></span>

<span data-ttu-id="1b1b7-p130">Office 365는 추적 조직에 인증 되지 않은 전자 메일을 보내는 사람입니다. 서비스 보낸사람 합법적인 없는 것으로 생각을 하는 경우에 *compauth* 오류도 표시 됩니다 것입니다. 메시지에 적용 된 스푸핑 방지 정책에 따라 달라 집니다 있지만이 스푸핑으로 분류 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1b1b7-p130">Office 365 keeps track of who is sending unauthenticated email to your organization. If the service thinks the sender is not legitimate, it will mark it as a *compauth* failure. This will be classified as SPOOF although it depends on your anti-spoofing policy that was applied to the message.</span></span> 
  
<span data-ttu-id="1b1b7-284">그러나를 관리자로 위장 된 전자 메일을 보낼 Office 365 의사 결정을 재정의 하는 어떤 보낸사람은 허용 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1b1b7-284">However, as an administrator, you can specify which senders are permitted to send spoofed email, overriding Office 365's decision.</span></span>
  
<span data-ttu-id="1b1b7-285">**방법 1-조직에서 도메인을 소유 하는 경우 전자 메일 인증 설정**</span><span class="sxs-lookup"><span data-stu-id="1b1b7-285">**Method 1 - If your organization owns the domain, set up email authentication**</span></span>
  
<span data-ttu-id="1b1b7-p131">조직 내 스푸핑 및 여러 테 넌 트와 소유 하거나 상호 작용 하는 경우에서 도메인 간 스푸핑 확인 하기 위해이 메서드를 사용할 수 있습니다. 또한도 Office 365 내에서 다른 고객에 게 보내면 도메인간 스푸핑 및 다른 공급자에서 호스팅되는 제 3 자 해결 하는데 도움이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1b1b7-p131">This method can be used to resolve intra-org spoofing, and cross-domain spoofing in cases where you own or interact with multiple tenants. It also helps resolve cross-domain spoofing where you send to other customers within Office 365, and also third parties that are hosted in other providers.</span></span>
  
<span data-ttu-id="1b1b7-288">자세한 내용은 [Office 365 고객을](#customers-of-office-365)참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="1b1b7-288">For more details, see [Customers of Office 365](#customers-of-office-365).</span></span> 
 
<span data-ttu-id="1b1b7-289">**방법 2-사용 스푸핑 인텔리전스 인증 되지 않은 전자 메일의 허용 된 거부 목록을 구성 하려면**</span><span class="sxs-lookup"><span data-stu-id="1b1b7-289">**Method 2 - Use Spoof intelligence to configure permitted senders of unauthenticated email**</span></span>
  
<span data-ttu-id="1b1b7-290">조직에 인증 되지 않은 메시지를 전송 하는 보낸사람을 허용 하도록 [스푸핑 인텔리전스](https://support.office.com/article/Learn-more-about-spoof-intelligence-978c3173-3578-4286-aaf4-8a10951978bf) 를 사용할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1b1b7-290">You can also use [Spoof Intelligence](https://support.office.com/article/Learn-more-about-spoof-intelligence-978c3173-3578-4286-aaf4-8a10951978bf) to permit senders to transmit unauthenticated messages to your organization.</span></span> 
  
<span data-ttu-id="1b1b7-291">외부 도메인에 대 한 위장 된 사용자가 도메인 보낸사람 주소에서 보내는 인프라는 보내는 IP 주소 (/24로 나눌 CIDR 범위), 또는 PTR 레코드의 조직 도메인 (아래 스크린샷에서 보내는 IP 수 해당 PTR 레코드는 outbound.mail.protection.outlook.com, 131.107.18.4 수 및 보내는 인프라에 대 한 outlook.com으로 표시 됩니다).</span><span class="sxs-lookup"><span data-stu-id="1b1b7-291">For external domains, the spoofed user is the domain in the From address, while the sending infrastructure is either the sending IP address (divided up into /24 CIDR ranges), or the organizational domain of the PTR record (in the screenshot below, the sending IP might be 131.107.18.4 whose PTR record is outbound.mail.protection.outlook.com, and this would show up as outlook.com for the sending infrastructure).</span></span>
  
<span data-ttu-id="1b1b7-292">이 보낸 인증 되지 않은 전자 메일을 보낼 수 있도록 **아니요** 를 **Yes**로 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b1b7-292">To permit this sender to send unauthenticated email, change the **No** to a **Yes**.</span></span>
  
![보낸사람 허용 antispoofing 설정](media/d4334921-d820-4334-8217-788279701e94.jpg)
  
<span data-ttu-id="1b1b7-294">PowerShell을 사용 하 여 특정 보낸 사람이 도메인 스푸핑할를 허용 하도록 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1b1b7-294">You can also use PowerShell to allow specific sender to spoof your domain:</span></span> 
  
```
$file = "C:\My Documents\Summary Spoofed Internal Domains and Senders.csv"
```

```
Get-PhishFilterPolicy -Detailed -SpoofAllowBlockList -SpoofType External | Export-CSV $file
```

![Powershell 통해 위장 된 보낸사람 시작](media/0e27ffcf-a5db-4c43-a19b-fa62326d5118.jpg)
  
<span data-ttu-id="1b1b7-296">이전 그림에서 추가 줄바꿈 추가 되었습니다이 스크린샷 하도록에 맞게, 하지만 단일 줄에 표시 되는 모든 값 실제로.</span><span class="sxs-lookup"><span data-stu-id="1b1b7-296">In the previous image, additional line breaks have been added to make this screenshot fit, but in actuality all the values would appear on a single line.</span></span>
  
<span data-ttu-id="1b1b7-297">파일을 편집 하 고 outlook.com 및 반응을에 해당 하는 줄을 찾습니다를 아니요에서 AllowedToSpoof 항목을 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b1b7-297">Edit the file and look for the line that corresponds to outlook.com and bing.com, and change the AllowedToSpoof Entry from No to Yes:</span></span>
  
![Powershell 통해 ' 예 '로 설정 스푸핑 허용](media/62340452-62d3-4958-9ce9-afe5275a870d.jpg)
  
<span data-ttu-id="1b1b7-299">파일을 저장 하 고을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b1b7-299">Save the file, and then run:</span></span> 
  
```
$UpdateSpoofedSenders = Get-Content -Raw "C:\My Documents\Spoofed Senders.csv"
Set-PhishFilterPolicy -Identity Default -SpoofAllowBlockList $UpdateSpoofedSenders
```

<span data-ttu-id="1b1b7-300">이렇게 하면에서 인증 되지 않은 전자 메일을 보낼 반응을 받을 이제 \*. outlook.com입니다.</span><span class="sxs-lookup"><span data-stu-id="1b1b7-300">This will now allow bing.com to send unauthenticated email from \*.outlook.com.</span></span>

<span data-ttu-id="1b1b7-301">**방법 3-보낸사람/받는 사람 쌍에 대 한 허용 항목 만들기**</span><span class="sxs-lookup"><span data-stu-id="1b1b7-301">**Method 3 - Create an allow entry for the sender/recipient pair**</span></span>
  
<span data-ttu-id="1b1b7-p132">모든 스팸 특정 보낸사람에 대 한 필터링을 무시 하도록 선택할 수 있습니다. 자세한 내용은 [안전 하 게 Office 365의 허용 목록에 보낸사람을 추가 하는 방법](https://blogs.msdn.microsoft.com/tzink/2017/11/29/how-to-securely-add-a-sender-to-an-allow-list-in-office-365/)을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="1b1b7-p132">You can also choose to bypass all spam filtering for a particular sender. For more details, see [How to securely add a sender to an allow list in Office 365](https://blogs.msdn.microsoft.com/tzink/2017/11/29/how-to-securely-add-a-sender-to-an-allow-list-in-office-365/).</span></span>
  
<span data-ttu-id="1b1b7-304">이 메서드를 사용 하는 경우 것을 건너뜁니다 스팸 및 phish 필터링의 일부가 아니라 맬웨어 필터링 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b1b7-304">If you use this method, it will skip spam and some of the phish filtering, but not malware filtering.</span></span>
  
<span data-ttu-id="1b1b7-305">**보낸사람에 게 문의 하 고 전자 메일 인증을 설정 하도록 요청 하는 방법 4-**</span><span class="sxs-lookup"><span data-stu-id="1b1b7-305">**Method 4 - Contact the sender and ask them to set up email authentication**</span></span>
  
<span data-ttu-id="1b1b7-p133">스팸 및 피싱의 문제 때문에 전자 메일 인증을 설정 하는 모든 보낸사람을 좋습니다. 보내는 도메인의 관리자를 알고 있는 경우 해당 하 고 모든 재정의 추가 하지 않아도 되므로 전자 메일 인증 레코드를 설정 하는 요청에 게 문의 합니다. 자세한 내용은 [Office 365 고객 되지 않은 도메인의 관리자](#administrators-of-domains-that-are-not-office-365-customers)를 참조 "이이 문서의 뒷부분에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1b1b7-p133">Because of the problem of spam and phishing, Microsoft recommends all senders set up email authentication. If you know an administrator of the sending domain, contact them and request that they set up email authentication records so you do not have to add any overrides. For more information, see [Administrators of domains that are not Office 365 customers](#administrators-of-domains-that-are-not-office-365-customers)" later in this article.</span></span> 
  
<span data-ttu-id="1b1b7-309">가져올 보내는 도메인 인증 하기 위해 먼저에 하기가 어려울 수 있지만, 시간이 지남에 따라으로 더 많은 전자 메일 필터 시작 junking 또는 전자 메일을 거부 하는,를 일으킬 수 있는 적절 한 레코드를 더 나은 배달 되도록 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1b1b7-309">While it may be difficult at first to get sending domains to authenticate, over time, as more and more email filters start junking or even rejecting their email, it will cause them to set up the proper records to ensure better delivery.</span></span>
  
### <a name="viewing-reports-of-how-many-messages-were-marked-as-spoofed"></a><span data-ttu-id="1b1b7-310">얼마나 많은 메시지에 스푸핑 하는 것으로 표시 된 보고서를 확인</span><span class="sxs-lookup"><span data-stu-id="1b1b7-310">Viewing reports of how many messages were marked as spoofed</span></span>

<span data-ttu-id="1b1b7-p134">스푸핑 방지 정책에 설정 되 면 번호 문제를 해결 하려면 얼마나 많은 메시지 phish 것으로 표시 되며 위협 인텔리전스를 사용할 수 있습니다. 이 작업을 수행 하려면 보안으로 이동 &amp; 준수 센터 (SCC) 위협 관리에서 \> 탐색기, Phish, 및 그룹에 보낸 도메인 또는 보호 상태 보기를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b1b7-p134">Once your anti-spoofing policy is enabled, you can use Threat Intelligence to get numbers around how many messages are marked as phish. To do this, go into the Security &amp; Compliance Center (SCC) under Threat Management \> Explorer, set the View to Phish, and group by Sender Domain or Protection Status:</span></span>
  
![얼마나 많은 메시지 phish로 표시 된 보기](media/de25009a-44d4-4c5f-94ba-9c75cd9c64b3.jpg)
  
<span data-ttu-id="1b1b7-p135">얼마나 많은 스푸핑으로 표시 된 메시지를 포함 하 여 피싱으로 표시 된 참조를 다양 한 보고서와 상호작용할 수 있습니다. 자세한 내용은 [Office 365 위협 인텔리전스 시작 하기](https://support.office.com/article/get-started-with-office-365-threat-intelligence-38e9b67f-d188-490f-bc91-a1ae4b270441)를 참조 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b1b7-p135">You can interact with the various reports to see how many were marked as phishing, including messages marked as SPOOF. To learn more, see [Get started with Office 365 Threat Intelligence](https://support.office.com/article/get-started-with-office-365-threat-intelligence-38e9b67f-d188-490f-bc91-a1ae4b270441).</span></span>
  
<span data-ttu-id="1b1b7-p136">아직 수행 하는 메시지 다른 유형의 (일반 피싱, 도메인 또는 사용자 가장 등에) 피싱 및 스푸핑으로 인해 표시 된 것을 분리할 수 없습니다. 그러나 2018, 뒷부분에 나오는 됩니다 보안을 통해이 작업을 수행할 수 &amp; 준수 센터입니다. 그렇게 할 경우에 인증에 실패으로 인해 스푸핑으로 표시 되는 합법적인 될 수 있는 보내는 도메인을 식별 하기 시작 지점으로이 보고서를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1b1b7-p136">You cannot yet split out which messages were marked due to spoofing vs. other types of phishing (general phishing, domain or user impersonation, and so on). However, later in 2018, you will be able to do this through the Security &amp; Compliance Center. Once you do, you can use this report as a starting place to identify sending domains that may be legitimate that are being marked as spoof due to failing authentication.</span></span>
  
<span data-ttu-id="1b1b7-319">다음 스크린샷에 제안 어떻게이 데이터를 확인 되지 않은 놓을 때 변경 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1b1b7-319">The following screenshot is a proposal for how this data will look, but may change when released:</span></span>
  
![검색 유형별 피싱 보고서 보기](media/dd25d63f-152c-4c55-a07b-184ecda2de81.jpg)
  
<span data-ttu-id="1b1b7-p137">비 ATP 및 e 5 고객에 대 한 이러한 보고서 위협 보호 상태 (TPS) 보고서에서 2018 뒷부분에 나오는 사용할 수 있지만 24 시간 이상으로 지연 됩니다. 이 페이지의 보안에 통합으로 업데이트 됩니다 &amp; 준수 센터입니다.</span><span class="sxs-lookup"><span data-stu-id="1b1b7-p137">For non-ATP and E5 customers, these reports will be available later in 2018 under the Threat Protection Status (TPS) reports, but will be delayed by at least 24 hours. This page will be updated as they are integrated into the Security &amp; Compliance Center.</span></span>
  
### <a name="predicting-how-many-messages-will-be-marked-as-spoof"></a><span data-ttu-id="1b1b7-323">예측 스푸핑 얼마나 많은 메시지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1b1b7-323">Predicting how many messages will be marked as spoof</span></span>

<span data-ttu-id="1b1b7-p138">2018, 뒷부분에 나오는 Office 365 스푸핑 방지 적용을 해제할 수 있도록 해당 설정을 업데이트 하는 한번 또는에서 기본 또는 높은 적용을 사용 하면 하 게 할 메시지 처리는 다양 한 설정에서 어떻게 변경 되는지 확인 하는 기능입니다. 즉, 스푸핑 방지을 해제 하는 경우 됩니다; 인증 방법이 기본 설정 하는 경우 스푸핑으로 얼마나 많은 메시지를 검색할 수 됩니다를 볼 수 또는 Basic 인 경우에 얼마나 많은 자세한 메시지 높음으로 설정 하는 경우 스푸핑으로 검색 됩니다 참조 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1b1b7-p138">Later in 2018, once Office 365 updates its settings to let you turn the anti-spoofing enforcement Off, or on with Basic or High enforcement, you will be given the ability to see how message disposition will change at the various settings. That is, if anti-spoofing is Off, you will be able to see how many messages will be detected as Spoof if you turn to Basic; or, if it's Basic, you will be able to see how many more messages will be detected as Spoof if you turn it to High.</span></span>
  
<span data-ttu-id="1b1b7-p139">이 기능은 현재 개발입니다. 자세한 내용은 정의된대로이 페이지는 보안 및 규정 준수 센터의 스크린샷이 텔 레 프레 및 PowerShell 예제와 함께 업데이트 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1b1b7-p139">This feature is currently under development. As more details are defined, this page will be updated both with screenshots of the Security and Compliance Center, and with PowerShell examples.</span></span>
  
![Antispoofing를 사용 하도록 설정 하는 것에 대 한 보고서 "경우"](media/fdd085ae-02c1-4327-a063-bfe9a32ff1eb.jpg)
  
![위장 된 보낸사람 허용 하는 것에 대 한 가능한 UX](media/53f9f73e-fb01-47f3-9a6d-850c1aef5efe.jpg)
  
### <a name="understanding-how-spam-phishing-and-advanced-phishing-detections-are-combined"></a><span data-ttu-id="1b1b7-330">이해 어떻게 스팸, 피싱, 및 고급 피싱 감지 결합 되어</span><span class="sxs-lookup"><span data-stu-id="1b1b7-330">Understanding how spam, phishing, and advanced phishing detections are combined</span></span>

<span data-ttu-id="1b1b7-p140">함께 또는 따로 ATP, Exchange Online을 사용 하는 조직은 서비스 맬웨어, 스팸, 높은 정확도 스팸, 피싱, 및 대량으로 메시지를 식별 하는 경우에 실행할 동작을 지정할 수 있습니다. ATP 고객에 대 한 ATP 피싱 방지 정책 및 EOP 고객에 대 한 피싱 방지 정책 및 메시지를 여러 검색 형식 (예: 맬웨어, 피싱, 및 사용자 가장)을 적중 수 팩트를 있을 수 있는 계정으로 일부 혼란 정책이 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1b1b7-p140">Organizations that use Exchange Online, with or without ATP, can specify which actions to take when the service identifies messages as malware, spam, high confidence spam, phishing, and bulk. With the ATP Anti-phishing policies for ATP customers, and the Anti-phishing policies for EOP customers, and the fact that a message may hit multiple detection types (for example, malware, phishing, and user-impersonation), there may be some confusion as to which policy applies.</span></span> 
  
<span data-ttu-id="1b1b7-333">일반적으로 X Forefront-스팸 방지 보고서 머리글 고양이 (범주) 속성에는 메시지에 적용 되는 정책을 식별 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1b1b7-333">In general, the policy applied to a message is identified in the X-Forefront-Antispam-Report header in the CAT (Category) property.</span></span> 
  
|<span data-ttu-id="1b1b7-334">**우선 순위**</span><span class="sxs-lookup"><span data-stu-id="1b1b7-334">**Priority**</span></span>|<span data-ttu-id="1b1b7-335">**정책**</span><span class="sxs-lookup"><span data-stu-id="1b1b7-335">**Policy**</span></span>|<span data-ttu-id="1b1b7-336">**종류**</span><span class="sxs-lookup"><span data-stu-id="1b1b7-336">**Category**</span></span>|<span data-ttu-id="1b1b7-337">**여기서 관리?**</span><span class="sxs-lookup"><span data-stu-id="1b1b7-337">**Where managed?**</span></span>|<span data-ttu-id="1b1b7-338">**적용 대상**</span><span class="sxs-lookup"><span data-stu-id="1b1b7-338">**Applies to**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="1b1b7-339">1</span><span class="sxs-lookup"><span data-stu-id="1b1b7-339">1</span></span>  <br/> |<span data-ttu-id="1b1b7-340">Malware</span><span class="sxs-lookup"><span data-stu-id="1b1b7-340">Malware</span></span>  <br/> |<span data-ttu-id="1b1b7-341">MALW</span><span class="sxs-lookup"><span data-stu-id="1b1b7-341">MALW</span></span>  <br/> |[<span data-ttu-id="1b1b7-342">맬웨어 정책</span><span class="sxs-lookup"><span data-stu-id="1b1b7-342">Malware policy</span></span>](https://technet.microsoft.com/en-us/library/jj200745%28v=exchg.150%29.aspx) <br/> |<span data-ttu-id="1b1b7-343">모든 조직</span><span class="sxs-lookup"><span data-stu-id="1b1b7-343">All organizations</span></span>  <br/> |
|<span data-ttu-id="1b1b7-344">2 </span><span class="sxs-lookup"><span data-stu-id="1b1b7-344">2</span></span>  <br/> |<span data-ttu-id="1b1b7-345">피싱</span><span class="sxs-lookup"><span data-stu-id="1b1b7-345">Phishing</span></span>  <br/> |<span data-ttu-id="1b1b7-346">PHSH</span><span class="sxs-lookup"><span data-stu-id="1b1b7-346">PHSH</span></span>  <br/> |[<span data-ttu-id="1b1b7-347">호스팅된 콘텐츠 필터 정책</span><span class="sxs-lookup"><span data-stu-id="1b1b7-347">Hosted content filter policy</span></span>](https://technet.microsoft.com/library/jj200684%28v=exchg.150%29.aspx) <br/> |<span data-ttu-id="1b1b7-348">모든 조직</span><span class="sxs-lookup"><span data-stu-id="1b1b7-348">All organizations</span></span>  <br/> |
|<span data-ttu-id="1b1b7-349">3 </span><span class="sxs-lookup"><span data-stu-id="1b1b7-349">3</span></span>  <br/> |<span data-ttu-id="1b1b7-350">높은 정확도 스팸</span><span class="sxs-lookup"><span data-stu-id="1b1b7-350">High confidence spam</span></span>  <br/> |<span data-ttu-id="1b1b7-351">HSPM</span><span class="sxs-lookup"><span data-stu-id="1b1b7-351">HSPM</span></span>  <br/> |[<span data-ttu-id="1b1b7-352">호스팅된 콘텐츠 필터 정책</span><span class="sxs-lookup"><span data-stu-id="1b1b7-352">Hosted content filter policy</span></span>](https://technet.microsoft.com/library/jj200684%28v=exchg.150%29.aspx) <br/> |<span data-ttu-id="1b1b7-353">모든 조직</span><span class="sxs-lookup"><span data-stu-id="1b1b7-353">All organizations</span></span>  <br/> |
|<span data-ttu-id="1b1b7-354">4 </span><span class="sxs-lookup"><span data-stu-id="1b1b7-354">4</span></span>  <br/> |<span data-ttu-id="1b1b7-355">스푸핑</span><span class="sxs-lookup"><span data-stu-id="1b1b7-355">Spoofing</span></span>  <br/> |<span data-ttu-id="1b1b7-356">스푸핑</span><span class="sxs-lookup"><span data-stu-id="1b1b7-356">SPOOF</span></span>  <br/> |<span data-ttu-id="1b1b7-357">[피싱 방지 정책](https://go.microsoft.com/fwlink/?linkid=864553), [스푸핑 인텔리전스](https://support.office.com/article/Learn-more-about-spoof-intelligence-978c3173-3578-4286-aaf4-8a10951978bf)</span><span class="sxs-lookup"><span data-stu-id="1b1b7-357">[Anti-phishing policy](https://go.microsoft.com/fwlink/?linkid=864553),          [Spoof intelligence](https://support.office.com/article/Learn-more-about-spoof-intelligence-978c3173-3578-4286-aaf4-8a10951978bf)</span></span> <br/> |<span data-ttu-id="1b1b7-358">모든 조직</span><span class="sxs-lookup"><span data-stu-id="1b1b7-358">All organizations</span></span>  <br/> |
|<span data-ttu-id="1b1b7-359">5 </span><span class="sxs-lookup"><span data-stu-id="1b1b7-359">5</span></span>  <br/> |<span data-ttu-id="1b1b7-360">스팸</span><span class="sxs-lookup"><span data-stu-id="1b1b7-360">Spam</span></span>  <br/> |<span data-ttu-id="1b1b7-361">SPM</span><span class="sxs-lookup"><span data-stu-id="1b1b7-361">SPM</span></span>  <br/> |[<span data-ttu-id="1b1b7-362">호스팅된 콘텐츠 필터 정책</span><span class="sxs-lookup"><span data-stu-id="1b1b7-362">Hosted content filter policy</span></span>](https://technet.microsoft.com/library/jj200684%28v=exchg.150%29.aspx) <br/> |<span data-ttu-id="1b1b7-363">모든 조직</span><span class="sxs-lookup"><span data-stu-id="1b1b7-363">All organizations</span></span>  <br/> |
|<span data-ttu-id="1b1b7-364">6 </span><span class="sxs-lookup"><span data-stu-id="1b1b7-364">6</span></span>  <br/> |<span data-ttu-id="1b1b7-365">대량</span><span class="sxs-lookup"><span data-stu-id="1b1b7-365">Bulk</span></span>  <br/> |<span data-ttu-id="1b1b7-366">대량</span><span class="sxs-lookup"><span data-stu-id="1b1b7-366">BULK</span></span>  <br/> |[<span data-ttu-id="1b1b7-367">호스팅된 콘텐츠 필터 정책</span><span class="sxs-lookup"><span data-stu-id="1b1b7-367">Hosted content filter policy</span></span>](https://technet.microsoft.com/library/jj200684%28v=exchg.150%29.aspx) <br/> |<span data-ttu-id="1b1b7-368">모든 조직</span><span class="sxs-lookup"><span data-stu-id="1b1b7-368">All organizations</span></span>  <br/> |
|<span data-ttu-id="1b1b7-369">7 </span><span class="sxs-lookup"><span data-stu-id="1b1b7-369">7</span></span>  <br/> |<span data-ttu-id="1b1b7-370">도메인 가장</span><span class="sxs-lookup"><span data-stu-id="1b1b7-370">Domain Impersonation</span></span>  <br/> |<span data-ttu-id="1b1b7-371">DIMP</span><span class="sxs-lookup"><span data-stu-id="1b1b7-371">DIMP</span></span>  <br/> |[<span data-ttu-id="1b1b7-372">피싱 방지 정책</span><span class="sxs-lookup"><span data-stu-id="1b1b7-372">Anti-phishing policy</span></span>](https://go.microsoft.com/fwlink/?linkid=864553) <br/> |<span data-ttu-id="1b1b7-373">ATP와 조직에만 해당</span><span class="sxs-lookup"><span data-stu-id="1b1b7-373">Organizations with ATP only</span></span>  <br/> |
|<span data-ttu-id="1b1b7-374">8 </span><span class="sxs-lookup"><span data-stu-id="1b1b7-374">8</span></span>  <br/> |<span data-ttu-id="1b1b7-375">사용자 가장</span><span class="sxs-lookup"><span data-stu-id="1b1b7-375">User Impersonation</span></span>  <br/> |<span data-ttu-id="1b1b7-376">UIMP</span><span class="sxs-lookup"><span data-stu-id="1b1b7-376">UIMP</span></span>  <br/> |[<span data-ttu-id="1b1b7-377">피싱 방지 정책</span><span class="sxs-lookup"><span data-stu-id="1b1b7-377">Anti-phishing policy</span></span>](https://go.microsoft.com/fwlink/?linkid=864553) <br/> |<span data-ttu-id="1b1b7-378">ATP와 조직에만 해당</span><span class="sxs-lookup"><span data-stu-id="1b1b7-378">Organizations with ATP only</span></span> <br/> |
   
<span data-ttu-id="1b1b7-p141">여러 다른 피싱 방지 정책을 가장 높은 우선순위에 하나씩 적용 됩니다. 예, 두 정책이 있다고 가정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b1b7-p141">If you have multiple different Anti-phishing policies, the one at the highest priority will apply. For example, suppose you have two policies:</span></span>
  
|<span data-ttu-id="1b1b7-381">**정책**</span><span class="sxs-lookup"><span data-stu-id="1b1b7-381">**Policy**</span></span>|<span data-ttu-id="1b1b7-382">**우선 순위**</span><span class="sxs-lookup"><span data-stu-id="1b1b7-382">**Priority**</span></span>|<span data-ttu-id="1b1b7-383">**사용자/도메인 가장**</span><span class="sxs-lookup"><span data-stu-id="1b1b7-383">**User/Domain Impersonation**</span></span>|<span data-ttu-id="1b1b7-384">**스푸핑 방지**</span><span class="sxs-lookup"><span data-stu-id="1b1b7-384">**Anti-spoofing**</span></span>|
|:-----|:-----|:-----|:-----|
|<span data-ttu-id="1b1b7-385">A</span><span class="sxs-lookup"><span data-stu-id="1b1b7-385">A</span></span>  <br/> |<span data-ttu-id="1b1b7-386">1</span><span class="sxs-lookup"><span data-stu-id="1b1b7-386">1</span></span>  <br/> |<span data-ttu-id="1b1b7-387">On</span><span class="sxs-lookup"><span data-stu-id="1b1b7-387">On</span></span>  <br/> |<span data-ttu-id="1b1b7-388">Off</span><span class="sxs-lookup"><span data-stu-id="1b1b7-388">Off</span></span>  <br/> |
|<span data-ttu-id="1b1b7-389">B</span><span class="sxs-lookup"><span data-stu-id="1b1b7-389">B</span></span>  <br/> |<span data-ttu-id="1b1b7-390">2 </span><span class="sxs-lookup"><span data-stu-id="1b1b7-390">2</span></span>  <br/> |<span data-ttu-id="1b1b7-391">Off</span><span class="sxs-lookup"><span data-stu-id="1b1b7-391">Off</span></span>  <br/> |<span data-ttu-id="1b1b7-392">On</span><span class="sxs-lookup"><span data-stu-id="1b1b7-392">On</span></span>  <br/> |
   
<span data-ttu-id="1b1b7-393">메시지에는 및 스푸핑 및 사용자 가장으로 식별 된 및 사용자의 동일한 집합 정책 A와 B 정책으로 범위가 지정 된 후 메시지 스푸핑은으로 처리 됩니다 하 고 아무 작업도 이후 적용 되 백신 스푸핑 꺼져 스푸핑 사용자 가장 (8) 보다 더 높은 우선순위 (4)에서 실행 되 고 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1b1b7-393">If a message comes in and is identified as both spoofing and user impersonation, and the same set of users is scoped to Policy A and Policy B, then the message is treated as a spoof but no action is applied since Anti-spoofing is turned off, and SPOOF runs at a higher priority (4) than User Impersonation (8).</span></span>
  
<span data-ttu-id="1b1b7-394">피싱의 다른 형식을 사용 하려면 정책 적용, 다양 한 정책에 적용 되는의 설정을 조정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b1b7-394">To make other types of phishing policy apply, you will need to adjust the settings of who the various policies are applied to.</span></span>
  
### <a name="legitimate-scenarios-to-disable-anti-spoofing"></a><span data-ttu-id="1b1b7-395">스푸핑 방지를 사용 하지 않도록 설정 하는 합법적인 시나리오</span><span class="sxs-lookup"><span data-stu-id="1b1b7-395">Legitimate scenarios to disable anti-spoofing</span></span>

<span data-ttu-id="1b1b7-p142">피싱 공격 으로부터 고객을 보호 더 잘 스푸핑 방지 하 고 사용 하지 않도록 설정 스푸핑 방지 보호 권장 되지 않으므로 합니다. 을 해제 하 여 일부 단기 가양성을 더 위험에 노출 되는 장기 하지만 해결할 수 있습니다. 발신자 측에서 인증을 설정 하거나 피싱 정책에서 조정에 대 한 비용에는 일반적으로 일회성 이벤트 또는 최소한의 고 정기적인 유지 관리가 필요 합니다. 그러나 여기서 데이터 노출 된, 피싱 공격에서 복구 하기 위한 비용은 또는 자산 된 손상 매우 높습니다.</span><span class="sxs-lookup"><span data-stu-id="1b1b7-p142">Anti-spoofing better protects customers from phishing attacks, and therefore disabling anti-spoofing protection is strongly discouraged. By disabling it, you may resolve some short-term false positives, but long term you will be exposed to more risk. The cost for setting up authentication on the sender side, or making adjustments in the phishing policies, are usually one-time events or require only minimal, periodic maintenance. However, the cost to recover from a phishing attack where data has been exposed, or assets have been compromised is much higher.</span></span>
  
<span data-ttu-id="1b1b7-400">이러한 이유로 스푸핑 방지 가양성 스푸핑 방지 보호를 사용 하지 않도록 설정 하려면 보다을 통해 작동 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="1b1b7-400">For this reason, it is better to work through anti-spoofing false positives than to disable anti-spoof protection.</span></span>
  
<span data-ttu-id="1b1b7-401">그러나은 합법적인 시나리오를 스푸핑 방지 해제 해야 하 고은 추가 메일 필터링 있을 때 사용할 수 없는 전자 메일 경로에 있는 첫번째 홉 메시지 라우팅 및 Office 365의 제품:</span><span class="sxs-lookup"><span data-stu-id="1b1b7-401">However, there is a legitimate scenario where anti-spoofing should be disabled, and that is when there are additional mail-filtering products in the message routing, and Office 365 is not the first hop in the email path:</span></span>
  
![Office 365를 고객 MX 레코드를 가리키지 않습니다.](media/62127c16-cfb8-4880-9cad-3c12d827c67e.jpg)
  
<span data-ttu-id="1b1b7-403">Exchange 온-프레미스 메일 서버, Ironport, 예: 장치를 필터링 하는 메일 또는 다른 클라우드 서비스를 호스팅하는 다른 서버 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1b1b7-403">The other server may be an Exchange on-premises mail server, a mail filtering device such as Ironport, or another cloud hosted service.</span></span>
  
<span data-ttu-id="1b1b7-p143">받는 사람 도메인의 MX 레코드를 가리키지 않을 Office 365를 하는 경우 사용 하지 않으려면 스푸핑 방지 Office 365 받는 도메인의 MX 레코드를 조회 하 고 다른 서비스를 가리키는 경우 스푸핑 방지를 생략 하기 때문에 필요 하지 않은 됩니다. 도메인의 다른 서버를 앞에는 경우를 모르는 경우에 MX 레코드를 조회 MX 도구 상자와 같은 웹사이트를 사용할 수 있습니다. 다음과 같은 라고 표시 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1b1b7-p143">If the MX record of the recipient domain does not point to Office 365, then there is no need to disable anti-spoofing because Office 365 looks up your receiving domain's MX record and suppresses anti-spoofing if it points to another service. If you don't know if your domain has another server in front, you can use a website like MX Toolbox to look up the MX record. It might say something like the following:</span></span>
  
![Office 365에 도메인 가리키지 않을 MX 레코드를 나타냅니다.](media/d868bb9f-3462-49aa-baea-9447a3ce4877.jpg)
  
<span data-ttu-id="1b1b7-408">이 도메인은 Office 365 스푸핑 방지 적용 적용 되지 않도록 Office 365를 가리키지 않는 MX 레코드를 가집니다.</span><span class="sxs-lookup"><span data-stu-id="1b1b7-408">This domain has an MX record that does not point to Office 365, so Office 365 would not apply anti-spoofing enforcement.</span></span>
  
<span data-ttu-id="1b1b7-p144">그러나 *않는* 받는 사람 도메인의 MX 레코드는 Office 365 앞에 다른 서비스는 경우에 Office 365를 가리키도록, 하는 경우 다음 사용 하지 않도록 스푸핑 방지 합니다. 받는 사람 다시 쓰기를 사용 하 여 가장 일반적인 예제는입니다.</span><span class="sxs-lookup"><span data-stu-id="1b1b7-p144">However, if the MX record of the recipient domain  *does*  point to Office 365, even though there is another service in front of Office 365, then you should disable anti-spoofing. The most common example is through the use of a recipient rewrite:</span></span> 
  
![받는 사람 다시 쓰기에 대 한 라우팅 다이어그램](media/070d90d1-50a0-42e4-9fd3-920bc99a7cad.jpg)
  
<span data-ttu-id="1b1b7-412">Contoso.com 도메인의 MX 레코드를 포함 하기 때문에 Office 365에 도메인 @office365.contoso.net MX 레코드를 가리키는 하는 동안 온-프레미스 서버를 가리키는 \*. protection.outlook.com, 또는 \*. eo.outlook.com MX 레코드에서:</span><span class="sxs-lookup"><span data-stu-id="1b1b7-412">The domain contoso.com's MX record points to the on-premises server, while the domain @office365.contoso.net's MX record points to Office 365 because it contains \*.protection.outlook.com, or \*.eo.outlook.com in the MX record:</span></span>
  
![MX 레코드를 가리키는 Office 365, 따라서 아마도 받는 사람을 다시 작성](media/4101ad51-ef92-4907-b466-b41d14d344ca.jpg)
  
<span data-ttu-id="1b1b7-p145">Office 365에 받는 사람 도메인의 MX 레코드를 가리키지 않 및 받는 사람 다시 쓰기의 경우 되었기 때문에 해당 하는 경우를 구분 해야 합니다. 이러한 두 경우 간의 차이 구분을 고려해 야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b1b7-p145">Be sure to differentiate when a recipient domain's MX record does not point to Office 365, and when it has undergone a recipient rewrite. It is important to tell the difference between these two cases.</span></span>
  
<span data-ttu-id="1b1b7-416">수신 도메인 받는 사람-재작성 경우 되었기 때문에 여부 확실 하지 않은 경우 메시지 헤더를 검토 하 여 알 수 경우가 종종 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1b1b7-416">If you are unsure whether or not your receiving domain has undergone a recipient-rewrite, sometimes you can tell by looking at the message headers.</span></span>
  
<span data-ttu-id="1b1b7-417">먼저 a) 인증 결과 헤더에서 받는 사람 도메인에 대 한 메시지에서 머리글을 살펴봅니다.</span><span class="sxs-lookup"><span data-stu-id="1b1b7-417">a) First, look at the headers in the message for the recipient domain in the Authentication-Results header:</span></span> 
  
```
Authentication-Results: spf=fail (sender IP is 1.2.3.4)
  smtp.mailfrom=example.com; office365.contoso.net; dkim=fail
  (body hash did not verify) header.d=simple.example.com;
  office365.contoso.net; dmarc=none action=none
  header.from=example.com; compauth=fail reason=001
```

<span data-ttu-id="1b1b7-p146">이 경우 office365.contoso.net에서 위의 굵은 빨간색 텍스트로에서 받는 사람 도메인 발견 합니다. 다를 수 있습니다이 하에서 받는 사람: 헤더:</span><span class="sxs-lookup"><span data-stu-id="1b1b7-p146">The recipient domain is found in the bold red text above, in this case office365.contoso.net. This may be different that the recipient in the To: header:</span></span>
  
<span data-ttu-id="1b1b7-420">받는 사람: 예에서는 받는 사람 \<contoso.com @ 받는 사람\></span><span class="sxs-lookup"><span data-stu-id="1b1b7-420">To: Example Recipient \<recipient @ contoso.com\></span></span>
  
<span data-ttu-id="1b1b7-p147">실제 받는 사람 도메인의 MX 레코드 조회를 수행 합니다. 포함 하는 경우 \*. protection.outlook.com, mail.messaging.microsoft.com, \*. eo.outlook.com, 또는 mail.global.frontbridge.com는 MX Office 365를 가리키고 있는지를 의미 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b1b7-p147">Perform an MX-record lookup of the actual recipient domain. If it contains \*.protection.outlook.com, mail.messaging.microsoft.com, \*.eo.outlook.com, or mail.global.frontbridge.com, that means that the MX points to Office 365.</span></span>
  
<span data-ttu-id="1b1b7-p148">이러한 값을 포함 하지는 않는 하는 경우의 MX Office 365를 가리키지 않을 의미 합니다. 이 확인 하기 위해 사용할 수 있는 도구를 둘은 MX 도구 상자를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b1b7-p148">If it does not contain those values, then it means that the MX does not point to Office 365. One tool you can use to verify this is MX Toolbox.</span></span>
  
<span data-ttu-id="1b1b7-425">이 예의 경우에 대 한 다음 이라는 해당 contoso.com To 되었기 때문에 받는 사람 처럼 보이는 도메인: 헤더에 MX 레코드가 가리키는 prem에서 서버:</span><span class="sxs-lookup"><span data-stu-id="1b1b7-425">For this particular example, the following says that contoso.com, the domain that looks like the recipient since it was the To: header, has MX record points to an on-prem server:</span></span>
  
![Prem에서 서버를 가리키는 MX 레코드](media/2444144a-9a90-4319-96b2-d115041f669f.jpg)
  
<span data-ttu-id="1b1b7-427">그러나 실제 받는 사람이 office365.contoso.net 해당 MX 레코드는 Office 365를 가리킵니다.</span><span class="sxs-lookup"><span data-stu-id="1b1b7-427">However, the actual recipient is office365.contoso.net whose MX record does point to Office 365:</span></span>
  
![Office 365를 가리키는 MX 받는 사람 재작성 이어야 합니다.](media/10cf3245-9b50-475a-b655-d8a51f99d812.jpg)
  
<span data-ttu-id="1b1b7-429">따라서이 메시지에 받는 사람-다시 쓰기 되었습니다 가능성이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1b1b7-429">Therefore, this message has likely undergone a recipient-rewrite.</span></span>
  
<span data-ttu-id="1b1b7-p149">b) 둘째, 받는 사람 다시 작성의 일반적인 사용 사례를 구분 해야 합니다. 받는 사람 도메인을 다시 작성 하려는 경우 \*. onmicrosoft.com를 대신 하도록 다시 작성 \*. mail.onmicrosoft.com 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b1b7-p149">b) Second, be sure to distinguish between common use cases of recipient rewrites. If you are going to rewrite the recipient domain to \*.onmicrosoft.com, instead rewrite it to \*.mail.onmicrosoft.com.</span></span>
  
<span data-ttu-id="1b1b7-432">다른 서버 뒤에 라우팅되는 최종 받는 사람 도메인을 식별 한 되 고 실제로 Office 365 (해당 DNS 레코드에 게시)으로 받는 사람 도메인의 MX 레코드를 가리키는 스푸핑 방지 사용 하지 않으려면 작업을 진행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1b1b7-432">Once you have identified the final recipient domain that is routed behind another server and the recipient domain's MX record actually points to Office 365 (as published in its DNS records), you may proceed to disable anti-spoofing.</span></span>
  
<span data-ttu-id="1b1b7-433">기억 스푸핑 방지 라우팅 경로에 도메인의 첫번째 홉은 Office 365 하나 이상의 서비스가 뒤에 하는 경우에 하는 경우 사용 하지 않도록 설정할 표시 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1b1b7-433">Remember, you don't want to disable anti-spoofing if the domain's first hop in the routing path is Office 365, only when it's behind one or more services.</span></span>
  
### <a name="how-to-disable-anti-spoofing"></a><span data-ttu-id="1b1b7-434">스푸핑 방지를 사용 하지 않도록 설정 하는 방법</span><span class="sxs-lookup"><span data-stu-id="1b1b7-434">How to disable anti-spoofing</span></span>

<span data-ttu-id="1b1b7-435">이미 만든는 피싱 방지 정책 경우 $false EnableAntispoofEnforcement 매개 변수를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b1b7-435">If you already have an Anti-phishing policy created, set the EnableAntispoofEnforcement parameter to $false:</span></span> 
  
```
$name = "<name of policy>"
Set-AntiphishPolicy -Identity $name -EnableAntiSpoofEnforcement $false 

```

<span data-ttu-id="1b1b7-436">사용 하지 않으려면 정책 (또는 정책)의 이름을 모르는 경우에 표시할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1b1b7-436">If you don't know the name of the policy (or policies) to disable, you can display them:</span></span> 
  
```
Get-AntiphishPolicy | fl Name
```

<span data-ttu-id="1b1b7-p150">모든 기존 피싱 방지 정책을 설치 하지 않은 경우 하나 만들고 수 (경우에 정책이 없는 경우, 여전히 적용 된; 2018에서 나중에 스푸핑 방지, 수에 대 한 기본 정책을 만들 하나를 만드는 대신 하는 다음 비활성화할 수) 사용 안함 . 여러 단계에서이 작업을 수행 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b1b7-p150">If you don't have any existing anti-phishing policies, you can create one and then disable it (even if you don't have a policy, anti-spoofing is still applied; later on in 2018, a default policy will be created for you and you can then disable that instead of creating one). You will have to do this in multiple steps:</span></span> 
  
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
# Finally, scope the antiphishing policy to the domains
Set-AntiphishPolicy -Identity $name -EnableAntispoofEnforcement $false 

```

<span data-ttu-id="1b1b7-p151">Cmdlet을 통해 사용할 수만 스푸핑 방지를 사용 하지 않도록 설정 (Q2 2018 뒷부분에 나오는 보안에서 사용할 수 있습니다 &amp; 준수 센터). PowerShell에 액세스할 수 없는 경우 지원 티켓을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="1b1b7-p151">Disabling anti-spoofing is only available via cmdlet (later in Q2 2018 it will be available in the Security &amp; Compliance Center). If you do not have access to PowerShell, create a support ticket.</span></span>
  
<span data-ttu-id="1b1b7-p152">Office 365로 전송 하는 경우에 간접 라우팅을 수행할 수 있는 도메인에만 적용할 수 해야이 기억 합니다. 일부 가양성으로 인해 스푸핑 방지를 사용 하지 않도록 하는 유혹, 통해 작동 하는 장기적으로 개선 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1b1b7-p152">Remember, this should only be applied to domains that undergo indirect routing when sent to Office 365. Resist the temptation to disable anti-spoofing because of some false positives, it will be better in the long run to work through them.</span></span>
  
### <a name="information-for-individual-users"></a><span data-ttu-id="1b1b7-443">개별 사용자에 대 한 정보</span><span class="sxs-lookup"><span data-stu-id="1b1b7-443">Information for individual users</span></span>

<span data-ttu-id="1b1b7-p153">개별 사용자에 게 안전 스푸핑 방지 팁과 작용 하는 방법 제한 됩니다. 그러나 몇 가지 일반적인 시나리오를 해결 하려면 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1b1b7-p153">Individual users are limited in how they can interact with the anti-spoofing safety tip. However, there are several things you can do to resolve common scenarios.</span></span>
  
### <a name="common-scenario-1---mailbox-forwarding"></a><span data-ttu-id="1b1b7-446">일반적인 시나리오 #1-사서함 착신 전환</span><span class="sxs-lookup"><span data-stu-id="1b1b7-446">Common scenario #1 - Mailbox forwarding</span></span>

<span data-ttu-id="1b1b7-p154">다른 전자 메일 서비스를 사용 하 고 Office 365 또는 Outlook.com에 전자 메일을 전달 하는 경우 전자 메일 스푸핑으로 표시 될 수 있습니다 및 빨간색 안전 팁을 수신 합니다. Office 365 및 Outlook.com Outlook.com, Office 365, Gmail, 또는 [호 프로토콜](https://arc-spec.org)을 사용 하는 다른 서비스 중 하나는 전달 자가 때 자동으로이 주소를 계획 합니다. 그러나 해당 수정 프로그램을 배포할 때까지 사용자는 착신 전환 옵션을 사용 하는 대신 해당 메시지를 직접 가져올 계정 연결 기능을 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b1b7-p154">If you use another email service and forward your email to Office 365 or Outlook.com, your email may be marked as spoofing and receive a red safety tip. Office 365 and Outlook.com plan to address this automatically when the forwarder is one of Outlook.com, Office 365, Gmail, or any other service that uses the [ARC protocol](https://arc-spec.org). However, until that fix is deployed, users should use the Connected Accounts feature to import their messages directly, rather than using the forwarding option.</span></span>
  
<span data-ttu-id="1b1b7-450">Office 365에 연결 된 계정을 설정 하는 Office 365 웹 인터페이스의 오른쪽 위 모서리에서 기어 아이콘을 선택 \> 메일 \> 메일 \> 계정 \> 계정에 연결 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b1b7-450">To set up connected accounts in Office 365, select the Gear icon in the top right corner of the Office 365 web interface \> Mail \> Mail \> Accounts \> Connected accounts.</span></span>
  
![Office 365-연결 된 계정 옵션](media/e8e841ca-8861-4d83-8506-2a0858c51010.jpg)
  
<span data-ttu-id="1b1b7-452">Outlook.com을 하는 프로세스는 기어 아이콘 \> 옵션 \> 메일 \> 계정 \> 계정에 연결 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b1b7-452">In Outlook.com, the process is the Gear icon \> Options \> Mail \> Accounts \> Connected accounts.</span></span>
  
### <a name="common-scenario-2---discussion-lists"></a><span data-ttu-id="1b1b7-453">일반적인 시나리오 #2-토론 목록</span><span class="sxs-lookup"><span data-stu-id="1b1b7-453">Common scenario #2 - Discussion lists</span></span>

<span data-ttu-id="1b1b7-454">토론 목록 메시지 스푸핑 방지 하는 방식 때문은 앞에 문제가 있는 수정 내용을 알려주지에서 원래 유지 것으로 알려져 있습니다: 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="1b1b7-454">Discussion lists are known to have problems with anti-spoofing due to the way they forward the message and modify its contents yet retain the original From: address.</span></span>
  
<span data-ttu-id="1b1b7-p155">예, 전자 메일 주소는 @ contoso.com, 사용자 및 감 감시에 관심이 있는 및 example.com @ 토론 목록 birdwatchers 참가 경우를 가정해 보겠습니다. 토론 목록에 메시지를 보낼 때 이러한 방식으로 보낼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1b1b7-p155">For example, suppose your email address is user @ contoso.com, and you are interested in Bird Watching and join the discussion list birdwatchers @ example.com. When you send a message to the discussion list, you might send it this way:</span></span>
  
<span data-ttu-id="1b1b7-457">**에서:** John Doe \<contoso.com @ 사용자\></span><span class="sxs-lookup"><span data-stu-id="1b1b7-457">**From:** John Doe \<user @ contoso.com\></span></span> 
  
<span data-ttu-id="1b1b7-458">**를:** Birdwatcher의 토론 목록 \<birdwatchers @ example.com\></span><span class="sxs-lookup"><span data-stu-id="1b1b7-458">**To:** Birdwatcher's Discussion List \<birdwatchers @ example.com\></span></span> 
  
<span data-ttu-id="1b1b7-p156">**제목:** 이번 주의 산 Rainier 상단의 파랑 제비의 뛰어난 보기</span><span class="sxs-lookup"><span data-stu-id="1b1b7-p156">**Subject:** Great viewing of blue jays at the top of Mt. Rainier this week</span></span> 
  
<span data-ttu-id="1b1b7-p157">보기를 체크아웃 하려면 누구나 산 Rainier에서 이번주?</span><span class="sxs-lookup"><span data-stu-id="1b1b7-p157">Anyone want to check out the viewing this week from Mt. Rainier?</span></span>
  
<span data-ttu-id="1b1b7-463">전자 메일 목록 메시지를 받으면 메시지의 서식, 해당 내용을 수정 있으며 많은 다른 전자 메일 수신기에서 참가자의 구성 된 있는 토론 목록에서 구성원의 나머지 부분을 재생 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b1b7-463">When the email list receives the message, they format the message, modify its contents, and replay it to the rest of the members on the discussion list which is made up of participants from many different email receivers.</span></span>
  
<span data-ttu-id="1b1b7-464">**에서:** John Doe \<contoso.com @ 사용자\></span><span class="sxs-lookup"><span data-stu-id="1b1b7-464">**From:** John Doe \<user @ contoso.com\></span></span> 
  
<span data-ttu-id="1b1b7-465">**를:** Birdwatcher의 토론 목록 \<birdwatchers @ example.com\></span><span class="sxs-lookup"><span data-stu-id="1b1b7-465">**To:** Birdwatcher's Discussion List \<birdwatchers @ example.com\></span></span> 
  
<span data-ttu-id="1b1b7-p158">**제목:** [BIRDWATCHERS] 이번 주의 산 Rainier 상단의 파랑 제비의 뛰어난 보기</span><span class="sxs-lookup"><span data-stu-id="1b1b7-p158">**Subject:** [BIRDWATCHERS] Great viewing of blue jays at the top of Mt. Rainier this week</span></span> 
  
<span data-ttu-id="1b1b7-p159">보기를 체크아웃 하려면 누구나 산 Rainier에서 이번주?</span><span class="sxs-lookup"><span data-stu-id="1b1b7-p159">Anyone want to check out the viewing this week from Mt. Rainier?</span></span>
  
---
  
<span data-ttu-id="1b1b7-p160">Birdwatchers 토론 목록에이 메시지를 보냈습니다. 언제 든 지 구독을 취소할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1b1b7-p160">This message was sent to the Birdwatchers Discussion List. You can unsubscribe at any time.</span></span>
  
<span data-ttu-id="1b1b7-p161">위의에서 재생 된 메시지에서 동일한에: 주소 (사용자 @ contoso.com) 하지만 원본 메시지의 제목줄 및 메시지의 아래쪽에 바닥글에 태그를 추가 하 여 수정 되었습니다. 이 유형의 메시지 수정 메일 그룹에서 일반적으로 이며 가양성에서 발생할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1b1b7-p161">In the above, the replayed message has the same From: address (user @ contoso.com) but the original message has been modified by adding a tag to the Subject line, and a footer to the bottom of the message. This type of message modification is common in mailing lists, and may result in false positives.</span></span>
  
<span data-ttu-id="1b1b7-474">사용자 또는 조직에서 다른 사용자가 메일 그룹의 관리자 인 경우 스푸핑 방지 검사를 통과 하도록 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1b1b7-474">If you or someone in your organization is an administrator of the mailing list, you may be able to configure it to pass anti-spoofing checks.</span></span>
  
- <span data-ttu-id="1b1b7-475">DMARC.org에서 FAQ 확인: [메일 그룹을 작동 하 고 DMARC와 상호 운용 될 하려고 하는 경우, 어떻게 해야 합니까?](https://dmarc.org/wiki/FAQ#I_operate_a_mailing_list_and_I_want_to_interoperate_with_DMARC.2C_what_should_I_do.3F)</span><span class="sxs-lookup"><span data-stu-id="1b1b7-475">Check the FAQ at DMARC.org: [I operate a mailing list and I want to interoperate with DMARC, what should I do?](https://dmarc.org/wiki/FAQ#I_operate_a_mailing_list_and_I_want_to_interoperate_with_DMARC.2C_what_should_I_do.3F)</span></span>
    
- <span data-ttu-id="1b1b7-476">이 블로그 게시물에 대 한 지침을 읽어: [오류를 방지 하기 위해 DMARC와 상호 운용 하는 메일 그룹 연산자에 대 한 팁](https://blogs.msdn.microsoft.com/tzink/2017/03/22/a-tip-for-mailing-list-operators-to-interoperate-with-dmarc-to-avoid-failures/)</span><span class="sxs-lookup"><span data-stu-id="1b1b7-476">Read the instructions at this blog post: [A tip for mailing list operators to interoperate with DMARC to avoid failures](https://blogs.msdn.microsoft.com/tzink/2017/03/22/a-tip-for-mailing-list-operators-to-interoperate-with-dmarc-to-avoid-failures/)</span></span>
    
- <span data-ttu-id="1b1b7-477">호를 지원 하기 위한 참조 하 여 메일 그룹 서버에 업데이트를 설치 하는 것이 좋습니다.[https://arc-spec.org](https://arc-spec.org/)</span><span class="sxs-lookup"><span data-stu-id="1b1b7-477">Consider installing updates on your mailing list server to support ARC, see [https://arc-spec.org](https://arc-spec.org/)</span></span>
    
<span data-ttu-id="1b1b7-478">메일 그룹의 소유권 없는 경우</span><span class="sxs-lookup"><span data-stu-id="1b1b7-478">If you do not have ownership of the mailing list:</span></span>
  
- <span data-ttu-id="1b1b7-479">(도 해야하는 메일 그룹에서 릴레이 도메인에 대 한 설정 하는 전자 메일 인증) 위의 옵션 중 하나를 구현 하는 메일 그룹의 유지 관리자를 요청할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1b1b7-479">You can request the maintainer of the mailing list to implement one of the options above (they should also have email authentication set up for the domain the mailing list is relaying from)</span></span>
    
- <span data-ttu-id="1b1b7-p162">받은 편지함에 메시지를 이동 하 여 전자 메일 클라이언트에서 사서함 규칙을 만들 수 있습니다. 또한 조직의 관리자를 설정 하는 규칙, 허용 또는 관리 적법 한 보낸 사람이 인증 되지 않은 전자 메일을 발송 하 게 섹션에서 설명으로 재정의 요청할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1b1b7-p162">You can create mailbox rules in your email client to move messages to the Inbox. You can also request your organization's administrators to set up allow rules, or overrides as discussed in the section Managing legitimate senders who are sending unauthenticated email</span></span>
    
- <span data-ttu-id="1b1b7-482">Office 365를 합법적으로 처리 하는 메일 그룹에 대 한 재정의 만드는 지원 티켓을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1b1b7-482">You can create a support ticket with Office 365 to create an override for the mailing list to treat it as legitimate</span></span>
    
### <a name="other-scenarios"></a><span data-ttu-id="1b1b7-483">다른 시나리오</span><span class="sxs-lookup"><span data-stu-id="1b1b7-483">Other scenarios</span></span>

1. <span data-ttu-id="1b1b7-p163">상황에 맞는 위의 일반적인 시나리오의 두가지가 모두 적용 하는 경우 메시지 false 양의 백업용으로 Microsoft에 보고 합니다. 자세한 내용은 섹션을 참조 하십시오. [Microsoft에 스팸 또는 스팸이 아닌 메시지를 다시 보고 합니까?](#how-can-i-report-spam-or-non-spam-messages-back-to-microsoft) 이 문서의 뒷부분에 나오는 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b1b7-p163">If neither of the above common scenarios applies to your situation, report the message as a false positive back to Microsoft. For more information, see the section [How can I report spam or non-spam messages back to Microsoft?](#how-can-i-report-spam-or-non-spam-messages-back-to-microsoft) later in this article.</span></span> 
    
2. <span data-ttu-id="1b1b7-p164">또한 것으로 microsoft 지원 티켓을 발생 시킬 수 있는 전자 메일 관리자에 게 문의 수 있습니다. Microsoft 엔지니어링 팀 스푸핑은으로 메시지를 표시 하는 이유를 조사 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b1b7-p164">You may also contact your email administrator who can raise it as a support ticket with Microsoft. The Microsoft engineering team will investigate why the message was marked as a spoof.</span></span>
    
3. <span data-ttu-id="1b1b7-p165">또한 보낸 이며 이러한 하지 침입 되 고 악의적으로 확신 사용자를 알고 있는 경우 인증 하지 않는 메일 서버에서 메시지를 보내고 있기를 나타내는 보낸 사람에 게 회신할 수 있습니다. 이 경우에 따라 필요한 전자 메일 인증 레코드를 설정 하는 자신의 IT 관리자에 게 문의 하는 원래 보낸사람에 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="1b1b7-p165">Additionally, if you know who the sender is and are confident they are not being maliciously spoofed, you may reply back to the sender indicating that they are sending messages from a mail server that does not authenticate. This sometimes results in the original sender contacting their IT administrator who will set up the required email authentication records.</span></span>
  
<span data-ttu-id="1b1b7-p166">충분 한 보낸사람 전자 메일 인증 레코드를 설정 해야 이러한 도메인 소유자에 게 회신을 하는 경우 해당 spurs 하에 작업을 수행 합니다. Microsoft의도 필요한 레코드를 게시 하려면 도메인 소유자와 함께 작동 하는 동안 훨씬 더 때 개별 사용자가 요청 도움이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1b1b7-p166">When enough senders reply back to domain owners that they should set up email authentication records, it spurs them into taking action. While Microsoft also works with domain owners to publish the required records, it helps even more when individual users request it.</span></span>
    
4. <span data-ttu-id="1b1b7-p167">필요에 따라 수신 허용-보낸사람 목록에 보낸사람을 추가 합니다. 그러나 하는 phisher 해당 계정을 스푸핑, 하는 경우 해당 배달 됩니다 사서함에 유의 합니다. 따라서이 옵션은 자주 사용 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b1b7-p167">Optionally, add the sender to your Safe Senders list. However, be aware that if a phisher spoofs that account, it will be delivered to your mailbox. Therefore, this option should be used sparingly.</span></span>
    
## <a name="how-senders-to-microsoft-should-prepare-for-anti-spoofing-protection"></a><span data-ttu-id="1b1b7-495">스푸핑 방지 보호에 대 한 Microsoft에 보낸사람 해야 준비 하는 방법</span><span class="sxs-lookup"><span data-stu-id="1b1b7-495">How senders to Microsoft should prepare for anti-spoofing protection</span></span>

<span data-ttu-id="1b1b7-496">관리자에 게 현재 Microsoft로 메시지를 보내는 경우 전자 메일 적절히 인증 되었는지 확인 해야 Office 365 또는 Outlook.com, 그렇지 않은 경우 스팸 또는 phish로 표시 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1b1b7-496">If you are an administrator who currently sends messages to Microsoft, either Office 365 or Outlook.com, you should ensure that your email is properly authenticated otherwise it may be marked as spam or phish.</span></span> 
  
### <a name="customers-of-office-365"></a><span data-ttu-id="1b1b7-497">Office 365의 고객</span><span class="sxs-lookup"><span data-stu-id="1b1b7-497">Customers of Office 365</span></span>

<span data-ttu-id="1b1b7-498">Office 365 고객 인 경우 Office 365를 사용 하 여 아웃 바운드 전자 메일을 보낼:</span><span class="sxs-lookup"><span data-stu-id="1b1b7-498">If you are an Office 365 customer and you use Office 365 to send outbound email:</span></span>
  
- <span data-ttu-id="1b1b7-499">도메인, [SPF 스푸핑을 방지 하기 위해 Office 365의 설정](https://docs.microsoft.com/office365/SecurityCompliance/set-up-spf-in-office-365-to-help-prevent-spoofing) 에 대 한</span><span class="sxs-lookup"><span data-stu-id="1b1b7-499">For your domains, [Set up SPF in Office 365 to help prevent spoofing](https://docs.microsoft.com/office365/SecurityCompliance/set-up-spf-in-office-365-to-help-prevent-spoofing)</span></span>
    
- <span data-ttu-id="1b1b7-500">기본 도메인을 [Office 365에서 사용자 지정 도메인에서 보낸 아웃 바운드 전자 메일의 유효성을 검사를 사용 하 여 DKIM](https://docs.microsoft.com/office365/SecurityCompliance/use-dkim-to-validate-outbound-email) 에 대 한</span><span class="sxs-lookup"><span data-stu-id="1b1b7-500">For your primary domains, [Use DKIM to validate outbound email sent from your custom domain in Office 365](https://docs.microsoft.com/office365/SecurityCompliance/use-dkim-to-validate-outbound-email)</span></span>
    
- <span data-ttu-id="1b1b7-501">적법 한 보낸 사람이 확인 하려면 도메인에 대 한 [DMARC 레코드 설정](https://docs.microsoft.com/office365/SecurityCompliance/use-dmarc-to-validate-email) 을</span><span class="sxs-lookup"><span data-stu-id="1b1b7-501">[Consider setting up DMARC records](https://docs.microsoft.com/office365/SecurityCompliance/use-dmarc-to-validate-email) for your domain to determine who are your legitimate senders</span></span> 
    
<span data-ttu-id="1b1b7-p168">Microsoft는 SPF, DKIM, 그리고 DMARC 각각에 대 한 자세한 구현 지침을 제공 하지 않습니다. 그러나 많은 온라인 게시 하는 정보는. 제 3 자 회사 전자 메일 인증 레코드를 설정 하 여 조직의 도움말을 전용 밖에도 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b1b7-p168">Microsoft does not provide detailed implementation guidelines for each of SPF, DKIM, and DMARC. However, there is a lot of information published online. There are also 3rd party companies dedicated to helping your organization set up email authentication records.</span></span>
  
### <a name="administrators-of-domains-that-are-not-office-365-customers"></a><span data-ttu-id="1b1b7-505">Office 365 고객 되지 않은 도메인 관리자</span><span class="sxs-lookup"><span data-stu-id="1b1b7-505">Administrators of domains that are not Office 365 customers</span></span>

<span data-ttu-id="1b1b7-506">도메인 관리자에 게는 하 고 Office 365 고객 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1b1b7-506">If you are a domain administrator but are not an Office 365 customer:</span></span>
  
- <span data-ttu-id="1b1b7-p169">도메인의 보내는 IP 주소를 게시 하도록 SPF를 설정 하 고도 DKIM (가능한 경우)를 설정 메시지에 디지털 서명 해야 합니다. 또한 설정 DMARC 레코드를 고려할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1b1b7-p169">You should set up SPF to publish your domain's sending IP addresses, and also set up DKIM (if available) to digitally sign messages. You may also consider setting up DMARC records.</span></span>
    
- <span data-ttu-id="1b1b7-509">방식으로 전자 메일을 보낼 수 있도록 함께 작업 해야하는 사용자를 대신 하 여 전자 메일을 전송 하는 동안 대량 발신자가 되도록 from에서을 보내는 도메인: 주소 (에 속해) 하는 경우 SPF 또는 DMARC를 전달 하는 도메인에 맞춥니다.</span><span class="sxs-lookup"><span data-stu-id="1b1b7-509">If you have bulk senders who are transmitting email on your behalf, you should work with them to send email in a way such that the sending domain in the From: address (if it belongs to you) aligns with the domain that passes SPF or DMARC.</span></span>
    
- <span data-ttu-id="1b1b7-510">온-프레미스 메일 서버, 또는 소프트웨어로-서비스 공급자 로부터 보내거나 Microsoft Azure, GoDaddy, Rackspace, Amazon 웹 서비스와 같은 클라우드 호스팅 서비스에서와 마찬가지로 확인 해야 하는 경우 SPF 레코드에 추가 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1b1b7-510">If you have on-premises mail servers, or send from a Software-as-a-service provider, or from a cloud-hosting service like Microsoft Azure, GoDaddy, Rackspace, Amazon Web Services, or similar, you should ensure that they are added to your SPF record.</span></span>
    
- <span data-ttu-id="1b1b7-p170">ISP에서 호스트 하는 작은 도메인 인 경우 ISP에 문의 하 여 제공 하는 지침에 따라 SPF 레코드를 설정 해야 합니다. 대부분의 Isp 이러한 유형의 지침을 제공 하 고 회사의 지원 페이지에서 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1b1b7-p170">If you are a small domain that is hosted by an ISP, you should set up your SPF record according to the instructions that is provided to you by your ISP. Most ISPs provide these types of instructions and can be found on the company's support pages.</span></span>
    
- <span data-ttu-id="1b1b7-p171">이전에 전자 메일 인증 레코드를 게시 하지 했습니다 하 고 제대로 작동 하는지, 하는 경우에 Microsoft로 보낼 전자 메일 인증 레코드 여전히 게시 해야 합니다. 이렇게 하 여 피싱, 퇴치에서 내리도록 하, 또는 조직에 보낼 phished 얻을 수 가능성 감소 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b1b7-p171">Even if you have not had to publish email authentication records before, and it worked fine, you must still publish email authentication records to send to Microsoft. By doing so, you are helping in the fight against phishing, and reducing the possibility that either you, or organizations you send to, will get phished.</span></span>
    
### <a name="what-if-you-dont-know-who-sends-email-as-your-domain"></a><span data-ttu-id="1b1b7-515">경우에 어떻게 도메인으로 전자 메일을 보내는 사용자에 대해 모르는?</span><span class="sxs-lookup"><span data-stu-id="1b1b7-515">What if you don't know who sends email as your domain?</span></span>

<span data-ttu-id="1b1b7-p172">여러 도메인의 모든 보낸사람에 있는 모르는 때문에 SPF 레코드를 게시 하지 않습니다. 하는 방법을 배우게, 사용자를 알 필요가 없습니다 모두 됩니다. 대신,의 특히 회사 트래픽 있는 위치를 알고 있는 않으며 중립 SPF 정책을 게시 위치에 대 한 SPF 레코드를 게시 하 여 시작 해야 합니까? 모든:</span><span class="sxs-lookup"><span data-stu-id="1b1b7-p172">Many domains do not publish SPF records because they do not know who all their senders are. That's okay, you do not need to know who all of them are. Instead, you should get started by publishing an SPF record for the ones you do know of, especially where your corporate traffic is located, and publish a neutral SPF policy, ?all:</span></span>
  
<span data-ttu-id="1b1b7-519">IN TXT example.com "v = spf1 include:spf.example.com? 모든"</span><span class="sxs-lookup"><span data-stu-id="1b1b7-519">example.com IN TXT "v=spf1 include:spf.example.com ?all"</span></span>
  
<span data-ttu-id="1b1b7-p173">중립 SPF 정책은 조직의 인프라에서 해제 되는 모든 전자 메일은 전달 전자 메일 인증 전혀 다른 전자 메일 수신자를 의미 합니다. 전자 메일에 대 한 모르는 사람이 보낸 채워지도록으로 거의 동일 전혀 없는 SPF 레코드를 게시 하는 중립으로 다시 실패 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b1b7-p173">The neutral SPF policy means that any email that comes out of your corporate infrastructure will pass email authentication at all other email receivers. Email that comes from senders you don't know about will fall back to neutral, which is almost the same as publishing no SPF record at all.</span></span>
  
<span data-ttu-id="1b1b7-p174">회사 트래픽에서 제공 되는 전자 메일, 인증 된 것으로 표시 됩니다 Office 365 메시지를 보내면 하지만 원본에 대 한 모르는에서 제공 되는 전자 메일 (여부 Office 365 암시적으로 인증할 수 그에 따라) 스푸핑으로 계속 표시 될 수 있습니다. 그러나이 Office 365 스푸핑으로 표시 되는 모든 전자 메일에서 향상 된 여전히입니다.</span><span class="sxs-lookup"><span data-stu-id="1b1b7-p174">When sending to Office 365, email that comes from your corporate traffic will be marked as authenticated, but the email that comes from sources you don't know about may still be marked as spoof (depending upon whether or not Office 365 can implicitly authenticate it). However, this is still an improvement from all email being marked as spoof by Office 365.</span></span>
  
<span data-ttu-id="1b1b7-524">SPF 레코드의 대체 정책과 함께 시작 참조 했으면? 모든 점진적으로 더 많은 보내는 인프라를 포함 하 고 다음 보다 엄격 하 게 정책을 게시할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1b1b7-524">Once you've gotten started with an SPF record with a fallback policy of ?all, you can gradually include more and more sending infrastructure and then publish a stricter policy.</span></span> 
  
### <a name="what-if-you-are-the-owner-of-a-mailing-list"></a><span data-ttu-id="1b1b7-525">메일 그룹의 소유자 하는 경우에 어떻게 합니까?</span><span class="sxs-lookup"><span data-stu-id="1b1b7-525">What if you are the owner of a mailing list?</span></span>

<span data-ttu-id="1b1b7-526">[일반적인 시나리오 #2-토론 목록](#common-scenario-2---discussion-lists)섹션을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="1b1b7-526">See the section [Common scenario #2 - Discussion lists](#common-scenario-2---discussion-lists).</span></span> 
  
### <a name="what-if-you-are-an-infrastructure-provider-such-as-an-internet-service-provider-isp-email-service-provider-esp-or-cloud-hosting-service"></a><span data-ttu-id="1b1b7-527">예: 인터넷 서비스 공급자 (ISP), 전자 메일 서비스 공급자 (ESP) 또는 서비스를 호스트 하는 클라우드 인프라 공급자를 하는 경우에 어떻게 합니까?</span><span class="sxs-lookup"><span data-stu-id="1b1b7-527">What if you are an infrastructure provider such as an Internet Service Provider (ISP), Email Service Provider (ESP), or cloud hosting service?</span></span>

<span data-ttu-id="1b1b7-528">도메인의 전자 메일을 호스트 하 고 전자 메일을 보내거나 전자 메일을 보낼 수 있는 호스팅 인프라를 제공 하는 경우 다음을 수행 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b1b7-528">If you host a domain's email, and it sends email, or provide hosting infrastructure that can send email, you should do the following:</span></span>
  
- <span data-ttu-id="1b1b7-529">확보할 수 있도록 고객이 자신의 SPF 레코드에서 게시 기능을 설명 하는 설명서</span><span class="sxs-lookup"><span data-stu-id="1b1b7-529">Ensure your customers have documentation detailing what to publish in their SPF records</span></span>
    
- <span data-ttu-id="1b1b7-p175">고객 하지 명시적으로 설정 (기본 도메인으로 기호) 하는 경우에 DKIM 서명 아웃 바운드 전자 메일에 서명 하는 것이 좋습니다. 짝수 이중 기호 (+) (한번와 상대가 설정한 것을 하는 경우에 고객의 도메인 및 회사의 DKIM 서명 사용 하 여 두번째 시간) DKIM 서명 사용 하 여 전자 메일을 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1b1b7-p175">Consider signing DKIM-signatures on outbound email even if the customer doesn't explicitly set it up (sign with a default domain). You can even double-sign the email with DKIM signatures (once with the customer's domain if they have set it up, and a second time with your company's DKIM signature)</span></span>
    
<span data-ttu-id="1b1b7-p176">사용 중인 플랫폼에서 발생 하는 전자 메일을 인증 하지만 Microsoft 인증 되지 않은 때문에 전자 메일 정크 하지 않는 보장 적어도 하는 경우에 Microsoft에 스팸과 보장 되지 않습니다. Outlook.com에서 전자 메일을 필터링 하는 방법에 대 한 자세한 내용은 [Outlook.com 전자 메일 관리자 페이지](https://postmaster.live.com/pm/postmaster.aspx)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="1b1b7-p176">Deliverability to Microsoft is not guaranteed even if you authenticate email originating from your platform, but at least it ensures that Microsoft does not junk your email because it is not authenticated. For more details around how Outlook.com filters email, see the [Outlook.com Postmaster page](https://postmaster.live.com/pm/postmaster.aspx).</span></span>
  
<span data-ttu-id="1b1b7-534">서비스 공급자에 대 한 유용한 정보에 대 한 자세한 내용은 [M3AAWG 모바일 메시징에 대 한 유용한 서비스 공급자를](https://www.m3aawg.org/sites/default/files/M3AAWG-Mobile-Messaging-Best-Practices-Service-Providers-2015-08.pdf)참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="1b1b7-534">For more details on service providers best practices, see [M3AAWG Mobile Messaging Best Practices for Service Providers](https://www.m3aawg.org/sites/default/files/M3AAWG-Mobile-Messaging-Best-Practices-Service-Providers-2015-08.pdf).</span></span>
  
## <a name="frequently-asked-questions"></a><span data-ttu-id="1b1b7-535">질문과 대답</span><span class="sxs-lookup"><span data-stu-id="1b1b7-535">Frequently Asked Questions</span></span>

### <a name="why-is-microsoft-making-this-change"></a><span data-ttu-id="1b1b7-536">Microsoft는 이러한 변경을 수행 하는 이유</span><span class="sxs-lookup"><span data-stu-id="1b1b7-536">Why is Microsoft making this change?</span></span>

<span data-ttu-id="1b1b7-537">하기 때문에 피싱 영향 공격 및 Microsoft 생각 하는 전자 메일 인증 15 년에 대 한 되었으며, 때문에 합법적인 전자 메일을 빼앗길 위험이 보다는 위험을 계속 인증 되지 않은 전자 메일을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b1b7-537">Because of the impact of phishing attacks, and because email authentication has been around for over 15 years, Microsoft believes that the risk of continue to allow unauthenticated email is higher than the risk of losing legitimate email.</span></span>
  
### <a name="will-this-change-cause-legitimate-email-to-be-marked-as-spam"></a><span data-ttu-id="1b1b7-538">이 변경 스팸으로 표시 하는 합법적인 전자 메일 포함 될?</span><span class="sxs-lookup"><span data-stu-id="1b1b7-538">Will this change cause legitimate email to be marked as spam?</span></span>

<span data-ttu-id="1b1b7-p177">처음에 스팸으로 표시 되는 일부 메시지 없을 것입니다. 그러나 시간이 지남에 따라 보낸사람을 조정 하 고 위장 된으로 레이블이 메시지의 양 대부분 전자 메일 경로 대 한 무시할 수 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1b1b7-p177">At first, there will be some messages that are marked as spam. However, over time, senders will adjust and then the amount of messages mislabeled as spoofed will be negligible for most email paths.</span></span>
  
<span data-ttu-id="1b1b7-p178">Microsoft 자체는 먼저이 기능 고객의 나머지 부분에 배포 하기 전에 몇 주가 채택 합니다. 처음에는 중단 동안 점진적으로 거부 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1b1b7-p178">Microsoft itself first adopted this feature several weeks before deploying it to the rest of its customers. While there was disruption at first, it gradually declined.</span></span>
  
### <a name="will-microsoft-bring-this-feature-to-outlookcom-and-non-advanced-threat-protection-customers-of-office-365"></a><span data-ttu-id="1b1b7-543">Microsoft은 Office 365의 Outlook.com 및 비-고급 위협 보호 고객에 게이 기능을 가져오려면가?</span><span class="sxs-lookup"><span data-stu-id="1b1b7-543">Will Microsoft bring this feature to Outlook.com and non-Advanced Threat Protection customers of Office 365?</span></span>

<span data-ttu-id="1b1b7-p179">Microsoft의 스푸핑 방지 기술 Office 365 Enterprise e 5 구독 명의 또는 구독에 대 한 Office 365 고급 위협 보호 (ATP) 추가 기능을 구입 명의 하는 해당 조직에 처음 배포 되었습니다. 년 10 월 2018를 기준으로 보호 하는 조직에서는 Exchange Online Protection (EOP)도를 확장 했을 때 했습니다. 나중에 Outlook.com에 대 한 릴리스 수는 있습니다. 그러나이 경우 보고와 같은 적용 되지 않은 일부 기능이 있을 수 및 사용자 정의 재정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b1b7-p179">Microsoft's anti-spoofing technology was initially deployed to its organizations that had an Office 365 Enterprise E5 subscription or had purchased the Office 365 Advanced Threat Protection (ATP) add-on for their subscription. As of October, 2018 we've extended the protection to organizations that have Exchange Online Protection (EOP) as well. In the future, we may release it for Outlook.com. However, if we do, there may be some capabilities that are not applied such as reporting and custom overrides.</span></span>
  
### <a name="how-can-i-report-spam-or-non-spam-messages-back-to-microsoft"></a><span data-ttu-id="1b1b7-548">어떻게 수 있습니까 스팸 또는 스팸이 아닌 메시지를 다시 보고 Microsoft?</span><span class="sxs-lookup"><span data-stu-id="1b1b7-548">How can I report spam or non-spam messages back to Microsoft?</span></span>

<span data-ttu-id="1b1b7-549">[보고서 메시지 용 추가 기능에서 Outlook를](https://support.office.com/article/use-the-report-message-add-in-b5caa9f1-cdf3-4443-af8c-ff724ea719d2)사용 하거나 [전송 스팸, 스팸이 아닌 및 분석을 위해 Microsoft에 피싱 사기 메시지](https://technet.microsoft.com/en-us/library/jj200769%28v=exchg.150%29.aspx)아닌 경우 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b1b7-549">You can either use the [Report Message Add-in for Outlook](https://support.office.com/article/use-the-report-message-add-in-b5caa9f1-cdf3-4443-af8c-ff724ea719d2), or if it isn't installed, [Submit spam, non-spam, and phishing scam messages to Microsoft for analysis](https://technet.microsoft.com/en-us/library/jj200769%28v=exchg.150%29.aspx).</span></span>
  
### <a name="im-a-domain-administrator-who-doesnt-know-who-all-my-senders-are"></a><span data-ttu-id="1b1b7-550">내 모든 보낸사람은 누구 인지 모릅니다 있는 도메인 관리자 결정!</span><span class="sxs-lookup"><span data-stu-id="1b1b7-550">I'm a domain administrator who doesn't know who all my senders are!</span></span>

<span data-ttu-id="1b1b7-551">[Office 365 고객 되지 않은 도메인의 관리자](#administrators-of-domains-that-are-not-office-365-customers)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="1b1b7-551">Please see [Administrators of domains that are not Office 365 customers](#administrators-of-domains-that-are-not-office-365-customers).</span></span>
  
### <a name="what-happens-if-i-disable-anti-spoofing-protection-for-my-organization-even-though-office-365-is-my-primary-filter"></a><span data-ttu-id="1b1b7-552">수행 되는 스푸핑 방지 보호 내 조직에 대 한 사용 하지 않도록 하는 경우 Office 365는 내 기본 필터 하는 경우에 작업</span><span class="sxs-lookup"><span data-stu-id="1b1b7-552">What happens if I disable anti-spoofing protection for my organization, even though Office 365 is my primary filter?</span></span>

<span data-ttu-id="1b1b7-p180">좋지 않습니다이 되므로 보다 부재중된 피싱 및 스팸 메시지를 노출할 수 있습니다. 일부 피싱 스푸핑은 하 고 일부 스푸핑을 누락 됩니다. 그러나 위험성이 고객에 게 스푸핑 방지를 사용 하면 보다 높은 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1b1b7-p180">We do not recommend this because you will be exposed to more missed phishing and spam messages. Not all phishing is spoofing, and not all spoofs will be missed. However, your risk will be higher than a customer who enables anti-spoofing.</span></span>
  
### <a name="does-enabling-anti-spoofing-protection-mean-i-will-be-protected-from-all-phishing"></a><span data-ttu-id="1b1b7-556">스푸핑 방지 보호 기능을 사용을 의미 합니까 모든 피싱으로부터 보호 합니까?</span><span class="sxs-lookup"><span data-stu-id="1b1b7-556">Does enabling anti-spoofing protection mean I will be protected from all phishing?</span></span>

<span data-ttu-id="1b1b7-p181">그러나 아니요, 피셔는 같은 기술을 사용 하 여 적용할 때문에 손상 된 계정 또는 무료 서비스 계정 설정 합니다. 그러나 피싱 방지 보호 기능 레이어는 Office 365의 보호 작업을 함께 설계 되었기 때문에 감지 다른 유형의 피싱 방법 이러한 하 여 서로 기반으로 구축 훨씬 더 잘 작동 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b1b7-p181">Unfortunately, no, because phishers will adapt to use other techniques such as compromised accounts, or setting up accounts of free services. However, anti-phishing protection works much better to detect these other types of phishing methods because Office 365's protection layers are designed work together and build on top of each other.</span></span>
  
### <a name="do-other-large-email-receivers-block-unauthenticated-email"></a><span data-ttu-id="1b1b7-559">다른 큰 전자 메일 수신자 인증 되지 않은 전자 메일을 차단 마십시오?</span><span class="sxs-lookup"><span data-stu-id="1b1b7-559">Do other large email receivers block unauthenticated email?</span></span>

<span data-ttu-id="1b1b7-p182">거의 모든 큰 전자 메일 수신자 전통적인 SPF, DKIM, 및 DMARC를 구현합니다. 일부 수신기가 다른 확인 하 고 해당 표준 하지만 적은 이동 관련해 서 Office 365를 차단 하려면 인증 되지 않은 것 보다 더 엄격한 수 있는 전자 메일을 스푸핑은 동일 하 게 취급 합니다. 그러나 대부분 업계의 피싱의 문제 때문에 특히 점차이 특정 유형의 전자 메일에 대 한 더 많은 엄격 하 게 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b1b7-p182">Nearly all large email receivers implement traditional SPF, DKIM, and DMARC. Some receivers have other checks that are more strict than just those standards, but few go as far as Office 365 to block unauthenticated email and treat them as a spoof. However, most of the industry is becoming more and more strict about this particular type of email, particularly because of the problem of phishing.</span></span>
  
### <a name="do-i-still-need-the-advanced-spam-filtering-option-enabled-for-spf-hard-fail-if-i-enable-anti-spoofing"></a><span data-ttu-id="1b1b7-563">고급 스팸 필터링 옵션을 설정 하는 스푸핑 방지 하는 경우 "SPF 하드 실패"에 대해 활성화 여전히 필요 합니까?</span><span class="sxs-lookup"><span data-stu-id="1b1b7-563">Do I still need the Advanced Spam Filtering option enabled for "SPF Hard Fail" if I enable anti-spoofing?</span></span>

<span data-ttu-id="1b1b7-p183">아니요, SPF 하드 실패 하지만 조건의 훨씬 더 넓은 집합에만 아니라 스푸핑 방지 기능 고려 하기 때문에이 옵션은 필요한 나타나지 않습니다. 스푸핑 방지 사용 하도록 설정 해야 하 고 사용 하도록 설정 하는 SPF 하드 실패 옵션을 아마도 받게 됩니다 더 가양성 합니다. 이 기능을 해제 하는 거의 없는 별도 catch 스팸 또는 phish을 제공 하 고 대신 대개 가양성을 생성 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="1b1b7-p183">No, this option is no longer required because the anti-spoofing feature not only considers SPF hard fails, but a much wider set of criteria. If you have anti-spoofing enabled and the SPF Hard Fail option enabled, you will probably get more false positives. We recommend disabling this feature as it would provide almost no additional catch for spam or phish, and instead generate mostly false positives.</span></span>
  
### <a name="does-sender-rewriting-scheme-srs-help-fix-forwarded-email"></a><span data-ttu-id="1b1b7-567">보낸 사람이 다시 쓰기 체계 (SRS) 어떤 도움이 됩니까 전달 된 전자 메일을 수정?</span><span class="sxs-lookup"><span data-stu-id="1b1b7-567">Does Sender Rewriting Scheme (SRS) help fix forwarded email?</span></span>

<span data-ttu-id="1b1b7-p184">SRS는 부분적 으로만 전달 된 전자 메일의 문제를 해결합니다. SMTP 메일을 다시를 작성 하 여 SRS 되도록 할 수 있는 다음 대상에 전달 된 메시지 전달 SPF. 그러나 From에 따라이 스푸핑 방지 하기 때문에: 주소 MAIL FROM 또는 DKIM 서명 도메인 (또는 다른 신호)와 함께, 않은 스푸핑 하는 것으로 표시 되 고에서 전달 된 전자 메일을 방지 하기 위해 충분 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b1b7-p184">SRS only partially fixes the problem of forwarded email. By rewriting the SMTP MAIL FROM, SRS can ensure that the forwarded message passes SPF at the next destination. However, because anti-spoofing is based upon the From: address in combination with either the MAIL FROM or DKIM-signing domain (or other signals), it is not enough to prevent forwarded email from being marked as spoofed.</span></span>
  

