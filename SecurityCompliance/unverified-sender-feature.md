---
title: Outlook.com 및 웹용 Outlook에서 의심 스러운 메시지 식별
ms.author: tracyp
author: MSFTTracyP
manager: laurawi
ms.date: 04/25/2019
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.collection:
- M365-security-compliance
description: 피싱 메시지가 사서함에 도착 하지 않도록 하기 위해 웹에서 Outlook.com 및 Outlook은 보낸 사람이 누구 인지를 확인 하 고 의심 스러운 메시지를 정크 메일로 표시 합니다.
ms.openlocfilehash: edba30bb2ac0f9dc6ebc12db957a518de0c1b543
ms.sourcegitcommit: 9907bebc5f225032f681c4952de0b0be2df278ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/26/2019
ms.locfileid: "33345918"
---
# <a name="identify-suspicious-messages-in-outlookcom-and-outlook-on-the-web"></a><span data-ttu-id="8f29f-103">Outlook.com 및 웹용 Outlook에서 의심 스러운 메시지 식별</span><span class="sxs-lookup"><span data-stu-id="8f29f-103">Identify suspicious messages in Outlook.com and Outlook on the web</span></span>

<span data-ttu-id="8f29f-104">피싱 메시지가 사서함에 도착 하지 않도록 하기 위해 웹에서 Outlook.com 및 Outlook은 보낸 사람이 누구 인지를 확인 하 고 의심 스러운 메시지를 정크 메일로 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f29f-104">To prevent phishing messages from reaching your mailbox, Outlook.com and Outlook on the web verify that the sender is who they say they are and mark suspicious messages as junk email.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8f29f-105">메시지가 피싱 사기로 표시 되 면 Outlook.com 및 웹용 Outlook의 페이지 맨 위에 경고가 표시 되지만 메시지의 모든 링크는 계속 열 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8f29f-105">When a message is marked as a phishing scam, Outlook.com and Outlook on the web display a warning at the top of the page, but any links in the message can still be opened.</span></span>

## <a name="how-can-i-identify-a-suspicious-message-in-my-inbox"></a><span data-ttu-id="8f29f-106">받은 편지함에서 의심 스러운 메시지를 어떻게 확인할 수 있나요?</span><span class="sxs-lookup"><span data-stu-id="8f29f-106">How can I identify a suspicious message in my inbox?</span></span>

<span data-ttu-id="8f29f-107">Outlook.com and Outlook에서 메시지를 보낸 사람이 식별 되지 않거나 id가 보낸 사람 주소에 표시 되는 내용과 다를 때 나타나는 지표를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f29f-107">Outlook.com and Outlook on the web show indicators when the sender of a message either can't be identified or their identity is different from what you see in the From address.</span></span>

### <a name="you-see-a--in-the-sender-image"></a><span data-ttu-id="8f29f-108">보낸 사람 이미지에 '? '가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8f29f-108">You see a '?' in the sender image</span></span>

<span data-ttu-id="8f29f-109">Outlook.com 및 웹용 Outlook에서 전자 메일 인증 기술을 사용 하 여 보낸 사람의 id를 확인할 수 없는 경우 보낸 사람 사진에 '? '가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8f29f-109">When Outlook.com and Outlook on the web can't verify the identity of the sender using email authentication techniques, they display a '?' in the sender photo.</span></span>

![메시지가 확인 통과 되지 않음](media/message-did-not-pass-verification.jpg)

<span data-ttu-id="8f29f-111">인증에 실패 한 모든 메시지는 악성이 아닙니다.</span><span class="sxs-lookup"><span data-stu-id="8f29f-111">Not every message that fails to authenticate is malicious.</span></span> <span data-ttu-id="8f29f-112">그러나 보낸 사람을 인식 하지 못하는 경우 인증을 받지 않는 메시지와 상호 작용할 때는 주의 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f29f-112">However, you should be careful about interacting with messages that don't authenticate if you don't recognize the sender.</span></span> <span data-ttu-id="8f29f-113">또는 일반적으로 보낸 사람 이미지에 '? '가 포함 되지 않는 보낸 사람을 인식할 수 있지만이를 갑자기 보면 보낸 사람이 위장 중 이라고 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8f29f-113">Or, if you recognize a sender that normally doesn't have a '?' in the sender image, but you suddenly start seeing it, that could be a sign the sender is being spoofed.</span></span>

### <a name="the-senders-address-is-different-than-what-appears-in-the-from-address"></a><span data-ttu-id="8f29f-114">보낸 사람의 주소가 보낸 사람 주소에 표시 되는 주소와 다릅니다.</span><span class="sxs-lookup"><span data-stu-id="8f29f-114">The sender's address is different than what appears in the From address</span></span>

<span data-ttu-id="8f29f-115">메시지에 표시 되는 전자 메일 주소가 보낸 사람 주소에 표시 되는 것과 다른 경우가 많습니다.</span><span class="sxs-lookup"><span data-stu-id="8f29f-115">Frequently, the email address you see in a message is different than what you see in the From address.</span></span> <span data-ttu-id="8f29f-116">때로는 보낸 사람이 실제 사용자가 아닌 다른 사람 이라고 생각 하는 것을 phishers 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f29f-116">Sometimes phishers try to trick you into thinking that the sender is someone other than who they really are.</span></span>

<span data-ttu-id="8f29f-117">웹에서 Outlook.com 및 Outlook이 보낸 사람의 실제 주소와 주소 간의 차이를 감지 하면 받는 사람 태그를 사용 하 여 해당 사용자에 게 밑줄이 그어져 있는 실제 보낸 사람이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8f29f-117">When Outlook.com and Outlook on the web detect a difference between the sender's actual address and the address on the From address, they show the actual sender using the via tag, which will be underlined.</span></span>

![확인 되지 않은 보낸 사람 대체 텍스트](media/unverified-sender-feature1.png)

<span data-ttu-id="8f29f-119">이 예에서는 보내는 도메인이 `suspicious.com` 인증 되지만 보낸 사람은 보낸 사람 주소에 추가 `unknown@contoso.com` 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8f29f-119">In this example, the sending domain `suspicious.com` is authenticated, but the sender put `unknown@contoso.com` in the From address.</span></span>

<span data-ttu-id="8f29f-120">via 태그를 포함 하는 모든 메시지를 의심 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8f29f-120">Not every message with a via tag is suspicious.</span></span> <span data-ttu-id="8f29f-121">그러나 via 태그가 있는 메시지를 모르는 경우에는 해당 태그와 상호 작용 하는 것이 조심 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f29f-121">However, if you don't recognize a message with a via tag, you should be cautious about interacting with it.</span></span>

<span data-ttu-id="8f29f-122">Outlook.com 및 웹용 새 Outlook에서는 메시지를 열지 않고도 메시지 목록에 있는 보낸 사람의 이름이 나 주소에 커서를 올려 놓아 해당 전자 메일 주소를 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8f29f-122">In Outlook.com and the new Outlook on the web, you can hover your cursor over a sender's name or address in the message list to see their email address, without needing to open the message.</span></span>

![OneDrive 시작](media/get-started-with-onedrive-message.png)

<span data-ttu-id="8f29f-124">웹에서 새 Outlook을 사용 하 고 있는지 어떻게 알 수 있나요?</span><span class="sxs-lookup"><span data-stu-id="8f29f-124">How do you know if you're using the new Outlook on the web?</span></span> <span data-ttu-id="8f29f-125">다음 예제를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="8f29f-125">See the following examples:</span></span>

![Outlook vs Office 365](media/outlook-vs-outlook365.png)

## <a name="frequently-asked-questions"></a><span data-ttu-id="8f29f-127">자주하는 질문</span><span class="sxs-lookup"><span data-stu-id="8f29f-127">Frequently asked questions</span></span>

### <a name="what-criteria-does-outlookcom-and-outlook-on-the-web-use-to-add-the--and-the-via-properties"></a><span data-ttu-id="8f29f-128">Outlook.com 및 웹용 Outlook에서 '? ' 및 ' via ' 속성을 추가 하는 데 사용 하는 기준은 무엇입니까?</span><span class="sxs-lookup"><span data-stu-id="8f29f-128">What criteria does Outlook.com and Outlook on the web use to add the '?' and the 'via' properties?</span></span>

<span data-ttu-id="8f29f-129">보낸 사람 이미지의 '? '에 대해: Outlook.com에서는 메시지가 SPF 또는 dkim 인증을 통과 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f29f-129">For the '?' in the sender image:  Outlook.com requires that the message pass either SPF or DKIM authentication.</span></span> <span data-ttu-id="8f29f-130">자세한 내용은 office 365에서 [스푸핑 방지](set-up-spf-in-office-365-to-help-prevent-spoofing.md) 및 [dkim을 사용 하 여 사용자 지정 도메인에서 보낸 아웃 바운드 전자 메일의 유효성을 검사 하](use-dkim-to-validate-outbound-email.md)는 데 도움을 주는 방법에 SPF를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f29f-130">For more details, see [Set up SPF in Office 365 to help prevent spoofing](set-up-spf-in-office-365-to-help-prevent-spoofing.md) and [Use DKIM to validate outbound email sent from your custom domain in Office 365](use-dkim-to-validate-outbound-email.md).</span></span>

<span data-ttu-id="8f29f-131">via 태그의 경우: 보낸 사람 주소에 있는 도메인이 dkim 서명 또는 SMTP 메일에서 보낸 도메인과 다른 경우 Outlook.com는 해당 두 필드 중 하나에 도메인을 표시 합니다 (dkim 서명 우선).</span><span class="sxs-lookup"><span data-stu-id="8f29f-131">For the via tag: If the domain in the From address is different from the domain in the DKIM signature or the SMTP MAIL FROM, Outlook.com displays the domain in one of those two fields (preferring the DKIM signature).</span></span>

### <a name="can-i-override-these-properties-with-ip-allows-exchange-transport-rule-allows-or-safe-senders"></a><span data-ttu-id="8f29f-132">IP 허용, Exchange 전송 규칙 허용 또는 수신 허용-보낸 사람을 사용 하 여 이러한 속성을 다시 정의할 수 있습니까?</span><span class="sxs-lookup"><span data-stu-id="8f29f-132">Can I override these properties with IP Allows, Exchange Transport Rule Allows, or safe senders?</span></span>

<span data-ttu-id="8f29f-133">이러한 속성은 재정의할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="8f29f-133">You can't override these properties.</span></span>

### <a name="how-do-i-remove-these-properties"></a><span data-ttu-id="8f29f-134">이러한 속성을 제거 하려면 어떻게 해야 합니까?</span><span class="sxs-lookup"><span data-stu-id="8f29f-134">How do I remove these properties?</span></span>

<span data-ttu-id="8f29f-135">보낸 사람 이미지의 '? '에 대해 보낸 사람으로 서 SPF 또는 dkim 중 하나를 사용 하 여 메시지를 인증 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f29f-135">For the '?' in the sender image: As a sender, you should authenticate your message with either SPF or DKIM.</span></span>

<span data-ttu-id="8f29f-136">via 태그: 보낸 사람으로 서, dkim 서명 또는 SMTP 메일의 도메인은 from 주소에 있는 도메인과 같거나 그 하위 도메인 인지 확인 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f29f-136">For the via tag: As a sender, you should ensure that either the domain in the DKIM signature or the SMTP MAIL FROM is the same as, or is a subdomain of, the domain in the From address.</span></span>

### <a name="does-outlookcom-and-outlook-on-the-web-show-this-for-every-message-that-doesnt-pass-authentication"></a><span data-ttu-id="8f29f-137">Outlook.com 및 웹용 Outlook에서 인증을 통과 하지 않는 모든 메시지를 표시 하나요?</span><span class="sxs-lookup"><span data-stu-id="8f29f-137">Does Outlook.com and Outlook on the web show this for every message that doesn’t pass authentication?</span></span>

<span data-ttu-id="8f29f-138">꼭 필요 하지는 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8f29f-138">Not necessarily.</span></span> <span data-ttu-id="8f29f-139">Outlook.com 및 웹용 Outlook의 메시지에는 보낸 사람을 인증 하기 위한 다른 속성이 있을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8f29f-139">Outlook.com and Outlook on the web may have other properties within the message to authenticate the sender.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8f29f-140">관련 항목</span><span class="sxs-lookup"><span data-stu-id="8f29f-140">Related topics</span></span>

[<span data-ttu-id="8f29f-141">Outlook.com 전자 메일 계정 보호</span><span class="sxs-lookup"><span data-stu-id="8f29f-141">Help protect your Outlook.com email account</span></span>](https://support.office.com/article/a4f20fc5-4307-4ece-8231-6d4d4bd8a9ba)

[<span data-ttu-id="8f29f-142">Outlook.com에서 불건전, 피싱 또는 스푸핑 처리</span><span class="sxs-lookup"><span data-stu-id="8f29f-142">Deal with abuse, phishing, or spoofing in Outlook.com</span></span>](https://support.office.com/article/0d882ea5-eedc-4bed-aebc-079ffa1105a3)

[<span data-ttu-id="8f29f-143">웹용 Outlook에서 정크 메일 및 스팸 필터링</span><span class="sxs-lookup"><span data-stu-id="8f29f-143">Filter junk email and spam in Outlook on the web</span></span>](https://support.office.com/article/db786e79-54e2-40cc-904f-d89d57b7f41d)
