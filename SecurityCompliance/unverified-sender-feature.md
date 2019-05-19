---
title: 확인 되지 않은 보낸 사람
ms.author: tracyp
author: MSFTTracyP
manager: laurawi
ms.date: 04/25/2019
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.collection:
- M365-security-compliance
description: 피싱 메시지가 사서함에 도착 하지 않도록 하기 위해 웹에서 Outlook.com 및 Outlook은 보낸 사람이 누구 인지를 확인 하 고 의심 스러운 메시지를 정크 메일로 표시 합니다.
ms.openlocfilehash: ad94a2953b6fd53612b2fc15038a7157e97f3b39
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/17/2019
ms.locfileid: "34157990"
---
# <a name="unverified-sender"></a><span data-ttu-id="1e972-103">확인 되지 않은 보낸 사람</span><span class="sxs-lookup"><span data-stu-id="1e972-103">Unverified Sender</span></span>

<span data-ttu-id="1e972-104">피싱 메시지가 사서함에 도착 하지 않도록 하기 위해 웹에서 Outlook.com 및 Outlook은 보낸 사람이 누구 인지를 확인 하 고 의심 스러운 메시지를 정크 메일로 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e972-104">To prevent phishing messages from reaching your mailbox, Outlook.com and Outlook on the web verify that the sender is who they say they are and mark suspicious messages as junk email.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="1e972-105">메시지가 피싱 사기로 표시 되 면 Outlook.com 및 웹용 Outlook의 페이지 맨 위에 경고가 표시 되지만 메시지의 모든 링크는 계속 열 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1e972-105">When a message is marked as a phishing scam, Outlook.com and Outlook on the web display a warning at the top of the page, but any links in the message can still be opened.</span></span>

## <a name="how-can-i-identify-a-suspicious-message-in-my-inbox"></a><span data-ttu-id="1e972-106">받은 편지함에서 의심 스러운 메시지를 어떻게 확인할 수 있나요?</span><span class="sxs-lookup"><span data-stu-id="1e972-106">How can I identify a suspicious message in my inbox?</span></span>

<span data-ttu-id="1e972-107">Outlook.com and Outlook에서 메시지를 보낸 사람이 식별 되지 않거나 id가 보낸 사람 주소에 표시 되는 내용과 다를 때 나타나는 지표를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e972-107">Outlook.com and Outlook on the web show indicators when the sender of a message either can't be identified or their identity is different from what you see in the From address.</span></span>

## <a name="how-to-manage-which-messages-receive-the-unverified-sender-treatment"></a><span data-ttu-id="1e972-108">확인 되지 않은 보낸 사람 처리를 수신 하는 메시지를 관리 하는 방법</span><span class="sxs-lookup"><span data-stu-id="1e972-108">How to manage which messages receive the unverified sender treatment</span></span> 

<span data-ttu-id="1e972-109">Office 365 고객 인 경우 Security & 준수 센터를 통해이 기능을 관리할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1e972-109">If you are an Office 365 customer you can manage this feature through the Security & Compliance Center.</span></span> 

- <span data-ttu-id="1e972-110">Office 365 Security & 준수 센터에서 테 넌 트 관리자는 피싱 정책 아래에 있는 스푸핑 방지 보호를 통해이 기능을 켜거나 끌 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1e972-110">In the Office 365 Security & Compliance Center, tenant admins can turn the feature on, or off, through the Anti-spoofing protection under the Anti-Phish policy.</span></span> <span data-ttu-id="1e972-111">또한 ' AntiPhishPolicy ' cmdlet을 통해 관리할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1e972-111">Additionally, it can be managed through the ‘Set-AntiPhishPolicy’ cmdlet.</span></span> <span data-ttu-id="1e972-112">자세한 내용은 Office 365 및 AntiPhishPolicy의 피싱 방지 보호를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="1e972-112">For more details, see Anti-phishing protection in Office 365 and Set-AntiPhishPolicy.</span></span>

    ![그래픽 인터페이스에서 인증 되지 않은 보낸 사람 편집](media/unverified-sender-article-editing-unauthenticated-senders.jpg)

- <span data-ttu-id="1e972-114">관리자가 가양성을 식별 했 고 보낸 사람이 확인 되지 않은 보낸 사람 처리를 수신 하지 않아야 하는 경우 다음 작업 중 하나를 수행 하 여 위장 인텔리전스 스푸핑 허용 목록에 보낸 사람을 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1e972-114">If an admin has identified a false positive, and a sender should not be receiving the unverified sender treatment they can take one of the following actions to add the sender to the Spoof Intelligence spoof allow list:</span></span>
        
    - <span data-ttu-id="1e972-115">스푸핑 인텔리전스 이해를 통해 도메인 쌍을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e972-115">Add the domain pair through the Spoof Intelligence Insight.</span></span> <span data-ttu-id="1e972-116">자세한 내용은 연습: 스푸핑 인텔리전스 이해를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="1e972-116">For more details, see Walkthrough: spoof intelligence insight</span></span>
                
    - <span data-ttu-id="1e972-117">Get-phishfilterpolicy cmdlet을 통해 도메인 쌍을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e972-117">Add the domain pair through the PhishFilterPolicy cmdlet.</span></span> <span data-ttu-id="1e972-118">자세한 내용은 Office 365의 Get-phishfilterpolicy 및 스푸핑 방지 보호를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="1e972-118">For more details, see Set-PhishFilterPolicy and Anti-spoofing protection in Office 365</span></span>

<span data-ttu-id="1e972-119">또한 ETRs (전자 메일 전송 규칙), 안전한 도메인 목록 (스팸 방지 정책), 수신 허용-보낸 사람 목록 또는 사용자가 해당 사용자를 "안전한 보낸 사람"으로 설정 하 여 관리자 허용 목록을 통해 받은 편지 함으로 배달 된 경우에는 확인 되지 않은 보낸 사람 처리가 적용 되지 않습니다. 받은 편지함.</span><span class="sxs-lookup"><span data-stu-id="1e972-119">Additionally, we do not apply the unverified sender treatment if it was delivered to the inbox via an admin allow list, including Email Transport Rules (ETRs), Safe Domain List (Anti-Spam Policy), Safe Sender List or a user has set this user as a “Safe Sender” in their inbox.</span></span>

### <a name="you-see-a--in-the-sender-image"></a><span data-ttu-id="1e972-120">보낸 사람 이미지에 '? '가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1e972-120">You see a '?' in the sender image</span></span>

<span data-ttu-id="1e972-121">Outlook.com 및 웹용 Outlook에서 전자 메일 인증 기술을 사용 하 여 보낸 사람의 id를 확인할 수 없는 경우 보낸 사람 사진에 '? '가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1e972-121">When Outlook.com and Outlook on the web can't verify the identity of the sender using email authentication techniques, they display a '?' in the sender photo.</span></span> 

![메시지가 확인 통과 되지 않음](media/message-did-not-pass-verification.jpg)

<span data-ttu-id="1e972-123">인증에 실패 한 모든 메시지는 악성이 아닙니다.</span><span class="sxs-lookup"><span data-stu-id="1e972-123">Not every message that fails to authenticate is malicious.</span></span> <span data-ttu-id="1e972-124">그러나 보낸 사람을 인식 하지 못하는 경우 인증을 받지 않는 메시지와 상호 작용할 때는 주의 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e972-124">However, you should be careful about interacting with messages that don't authenticate if you don't recognize the sender.</span></span> <span data-ttu-id="1e972-125">또는 일반적으로 보낸 사람 이미지에 '? '가 포함 되지 않는 보낸 사람을 인식할 수 있지만이를 갑자기 보면 보낸 사람이 위장 중 이라고 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1e972-125">Or, if you recognize a sender that normally doesn't have a '?' in the sender image, but you suddenly start seeing it, that could be a sign the sender is being spoofed.</span></span>

### <a name="the-senders-address-is-different-than-what-appears-in-the-from-address"></a><span data-ttu-id="1e972-126">보낸 사람의 주소가 보낸 사람 주소에 표시 되는 주소와 다릅니다.</span><span class="sxs-lookup"><span data-stu-id="1e972-126">The sender's address is different than what appears in the From address</span></span>

<span data-ttu-id="1e972-127">메시지에 표시 되는 전자 메일 주소가 보낸 사람 주소에 표시 되는 것과 다른 경우가 많습니다.</span><span class="sxs-lookup"><span data-stu-id="1e972-127">Frequently, the email address you see in a message is different than what you see in the From address.</span></span> <span data-ttu-id="1e972-128">때로는 보낸 사람이 실제 사용자가 아닌 다른 사람 이라고 생각 하는 것을 phishers 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e972-128">Sometimes phishers try to trick you into thinking that the sender is someone other than who they really are.</span></span>

<span data-ttu-id="1e972-129">웹에서 Outlook.com 및 Outlook이 보낸 사람의 실제 주소와 주소 간의 차이를 감지 하면 받는 사람 태그를 사용 하 여 해당 사용자에 게 밑줄이 그어져 있는 실제 보낸 사람이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1e972-129">When Outlook.com and Outlook on the web detect a difference between the sender's actual address and the address on the From address, they show the actual sender using the via tag, which will be underlined.</span></span>

![확인 되지 않은 보낸 사람 대체 텍스트](media/unverified-sender-feature1.png)

<span data-ttu-id="1e972-131">이 예에서는 보내는 도메인이 `suspicious.com` 인증 되지만 보낸 사람은 보낸 사람 주소에 추가 `unknown@contoso.com` 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1e972-131">In this example, the sending domain `suspicious.com` is authenticated, but the sender put `unknown@contoso.com` in the From address.</span></span>

<span data-ttu-id="1e972-132">Via 태그를 포함 하는 모든 메시지를 의심 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1e972-132">Not every message with a via tag is suspicious.</span></span> <span data-ttu-id="1e972-133">그러나 via 태그가 있는 메시지를 모르는 경우에는 해당 태그와 상호 작용 하는 것이 조심 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e972-133">However, if you don't recognize a message with a via tag, you should be cautious about interacting with it.</span></span>

<span data-ttu-id="1e972-134">Outlook.com 및 웹용 새 Outlook에서는 메시지를 열지 않고도 메시지 목록에 있는 보낸 사람의 이름이 나 주소에 커서를 올려 놓아 해당 전자 메일 주소를 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1e972-134">In Outlook.com and the new Outlook on the web, you can hover your cursor over a sender's name or address in the message list to see their email address, without needing to open the message.</span></span>

![OneDrive 시작](media/get-started-with-onedrive-message.png)

<span data-ttu-id="1e972-136">웹에서 새 Outlook을 사용 하 고 있는지 어떻게 알 수 있나요?</span><span class="sxs-lookup"><span data-stu-id="1e972-136">How do you know if you're using the new Outlook on the web?</span></span> <span data-ttu-id="1e972-137">다음 예제를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="1e972-137">See the following examples:</span></span>

![Outlook vs Office 365](media/outlook-vs-outlook365.png)

## <a name="frequently-asked-questions"></a><span data-ttu-id="1e972-139">자주하는 질문</span><span class="sxs-lookup"><span data-stu-id="1e972-139">Frequently asked questions</span></span>

### <a name="what-criteria-does-outlookcom-and-outlook-on-the-web-use-to-add-the--and-the-via-properties"></a><span data-ttu-id="1e972-140">Outlook.com 및 웹용 Outlook에서 '? ' 및 ' via ' 속성을 추가 하는 데 사용 하는 기준은 무엇입니까?</span><span class="sxs-lookup"><span data-stu-id="1e972-140">What criteria does Outlook.com and Outlook on the web use to add the '?' and the 'via' properties?</span></span>

<span data-ttu-id="1e972-141">보낸 사람 이미지의 '? '에 대해: Outlook.com에서는 메시지가 SPF 또는 DKIM 인증을 통과 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e972-141">For the '?' in the sender image:  Outlook.com requires that the message pass either SPF or DKIM authentication.</span></span> <span data-ttu-id="1e972-142">자세한 내용은 office 365에서 스푸핑 방지 및 dkim을 사용 하 여 사용자 지정 365 도메인에서 보낸 아웃 바운드 전자 메일의 유효성을 검사 하는 데 도움을 주는 방법에 SPF를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e972-142">For more details, see [Set up SPF in Office 365 to help prevent spoofing](set-up-spf-in-office-365-to-help-prevent-spoofing.md) and [Use DKIM to validate outbound email sent from your custom domain in Office 365](use-dkim-to-validate-outbound-email.md).</span></span>

<span data-ttu-id="1e972-143">Via 태그의 경우: 보낸 사람 주소에 있는 도메인이 DKIM 서명 또는 SMTP 메일에서 보낸 도메인과 다른 경우 Outlook.com는 해당 두 필드 중 하나에 도메인을 표시 합니다 (DKIM 서명 우선).</span><span class="sxs-lookup"><span data-stu-id="1e972-143">For the via tag: If the domain in the From address is different from the domain in the DKIM signature or the SMTP MAIL FROM, Outlook.com displays the domain in one of those two fields (preferring the DKIM signature).</span></span>

### <a name="can-i-override-these-properties-with-ip-allows-exchange-transport-rule-allows-or-safe-senders"></a><span data-ttu-id="1e972-144">IP 허용, Exchange 전송 규칙 허용 또는 수신 허용-보낸 사람을 사용 하 여 이러한 속성을 다시 정의할 수 있습니까?</span><span class="sxs-lookup"><span data-stu-id="1e972-144">Can I override these properties with IP Allows, Exchange Transport Rule Allows, or safe senders?</span></span>

<span data-ttu-id="1e972-145">이러한 속성은 재정의할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="1e972-145">You can't override these properties.</span></span>

### <a name="how-do-i-remove-these-properties"></a><span data-ttu-id="1e972-146">이러한 속성을 제거 하려면 어떻게 해야 합니까?</span><span class="sxs-lookup"><span data-stu-id="1e972-146">How do I remove these properties?</span></span>

<span data-ttu-id="1e972-147">보낸 사람 이미지의 '? '에 대해 보낸 사람으로 서 SPF 또는 DKIM 중 하나를 사용 하 여 메시지를 인증 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e972-147">For the '?' in the sender image: As a sender, you should authenticate your message with either SPF or DKIM.</span></span>

<span data-ttu-id="1e972-148">Via 태그: 보낸 사람으로 서, DKIM 서명 또는 SMTP 메일의 도메인은 From 주소에 있는 도메인과 같거나 그 하위 도메인 인지 확인 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e972-148">For the via tag: As a sender, you should ensure that either the domain in the DKIM signature or the SMTP MAIL FROM is the same as, or is a subdomain of, the domain in the From address.</span></span>

### <a name="does-outlookcom-and-outlook-on-the-web-show-this-for-every-message-that-doesnt-pass-authentication"></a><span data-ttu-id="1e972-149">Outlook.com 및 웹용 Outlook에서 인증을 통과 하지 않는 모든 메시지를 표시 하나요?</span><span class="sxs-lookup"><span data-stu-id="1e972-149">Does Outlook.com and Outlook on the web show this for every message that doesn’t pass authentication?</span></span>

<span data-ttu-id="1e972-150">꼭 필요 하지는 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1e972-150">Not necessarily.</span></span> <span data-ttu-id="1e972-151">Outlook.com 및 웹용 Outlook의 메시지에는 보낸 사람을 인증 하기 위한 다른 속성이 있을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1e972-151">Outlook.com and Outlook on the web may have other properties within the message to authenticate the sender.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1e972-152">관련 항목</span><span class="sxs-lookup"><span data-stu-id="1e972-152">Related topics</span></span>

[<span data-ttu-id="1e972-153">Outlook.com 전자 메일 계정 보호</span><span class="sxs-lookup"><span data-stu-id="1e972-153">Help protect your Outlook.com email account</span></span>](https://support.office.com/article/a4f20fc5-4307-4ece-8231-6d4d4bd8a9ba)

[<span data-ttu-id="1e972-154">Outlook.com에서 불건전, 피싱 또는 스푸핑 처리</span><span class="sxs-lookup"><span data-stu-id="1e972-154">Deal with abuse, phishing, or spoofing in Outlook.com</span></span>](https://support.office.com/article/0d882ea5-eedc-4bed-aebc-079ffa1105a3)

[<span data-ttu-id="1e972-155">웹용 Outlook에서 정크 메일 및 스팸 필터링</span><span class="sxs-lookup"><span data-stu-id="1e972-155">Filter junk email and spam in Outlook on the web</span></span>](https://support.office.com/article/db786e79-54e2-40cc-904f-d89d57b7f41d)
