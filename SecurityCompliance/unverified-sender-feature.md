---
title: 확인 되지 않은 보낸 사람
ms.author: tracyp
author: MSFTTracyP
manager: dansimp
ms.date: 07/11/2019
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.collection:
- M365-security-compliance
description: 피싱 메시지가 사서함에 도착 하지 않도록 하기 위해 웹에서 Outlook.com 및 Outlook은 보낸 사람이 누구 인지를 확인 하 고 의심 스러운 메시지를 정크 메일로 표시 합니다.
ms.openlocfilehash: 233474dbfff430be8dd95d513adeb257bb26c5c7
ms.sourcegitcommit: 9e2df36b05a2c93ce2629a7a5eda8f44159d114d
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/11/2019
ms.locfileid: "35628511"
---
# <a name="unverified-sender"></a><span data-ttu-id="ceeb1-103">확인 되지 않은 보낸 사람</span><span class="sxs-lookup"><span data-stu-id="ceeb1-103">Unverified Sender</span></span>

> [!NOTE] 
> <span data-ttu-id="ceeb1-104">이러한 업데이트는 현재 롤아웃 중 이며, 아직 모든 사용자에 대해 사용이 가능 하지 않을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ceeb1-104">These updates are rolling out now, and might not be available yet for all users.</span></span>

<span data-ttu-id="ceeb1-105">피싱 메시지가 사서함에 도착 하지 않도록 하기 위해 웹에서 Outlook.com 및 Outlook은 보낸 사람이 누구 인지를 확인 하 고 의심 스러운 메시지를 정크 메일로 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ceeb1-105">To prevent phishing messages from reaching your mailbox, Outlook.com and Outlook on the web verify that the sender is who they say they are and mark suspicious messages as junk email.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ceeb1-106">메시지가 피싱 사기로 표시 되 면 Outlook.com 및 웹용 Outlook의 페이지 맨 위에 경고가 표시 되지만 메시지의 모든 링크는 계속 열 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ceeb1-106">When a message is marked as a phishing scam, Outlook.com and Outlook on the web display a warning at the top of the page, but any links in the message can still be opened.</span></span>

## <a name="how-can-i-identify-a-suspicious-message-in-my-inbox"></a><span data-ttu-id="ceeb1-107">받은 편지함에서 의심 스러운 메시지를 어떻게 확인할 수 있나요?</span><span class="sxs-lookup"><span data-stu-id="ceeb1-107">How can I identify a suspicious message in my inbox?</span></span>

<span data-ttu-id="ceeb1-108">Outlook.com and Outlook에서 메시지를 보낸 사람이 식별 되지 않거나 id가 보낸 사람 주소에 표시 되는 내용과 다를 때 나타나는 지표를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ceeb1-108">Outlook.com and Outlook on the web show indicators when the sender of a message either can't be identified or their identity is different from what you see in the From address.</span></span>

## <a name="how-to-manage-which-messages-receive-the-unverified-sender-treatment"></a><span data-ttu-id="ceeb1-109">확인 되지 않은 보낸 사람 처리를 수신 하는 메시지를 관리 하는 방법</span><span class="sxs-lookup"><span data-stu-id="ceeb1-109">How to manage which messages receive the unverified sender treatment</span></span> 

<span data-ttu-id="ceeb1-110">Office 365 고객 인 경우 보안 & 준수 센터를 통해이 기능을 관리할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ceeb1-110">If you are an Office 365 customer you can manage this feature through the Security & Compliance Center.</span></span> 

- <span data-ttu-id="ceeb1-111">Office 365 보안 & 준수 센터에서 전역 또는 보안 관리자는 피싱 정책 아래에 있는 스푸핑 방지 보호를 통해이 기능을 설정 하거나 해제할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ceeb1-111">In the Office 365 Security & Compliance Center, global or security administrators can turn the feature on or off, through anti-spoofing protection under the Anti-Phish policy.</span></span> <span data-ttu-id="ceeb1-112">또한 ' AntiPhishPolicy ' cmdlet을 통해 관리할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ceeb1-112">Additionally, it can be managed through the ‘Set-AntiPhishPolicy’ cmdlet.</span></span> <span data-ttu-id="ceeb1-113">자세한 내용은 [Office 365 및 AntiPhishPolicy의 피싱 방지 보호](anti-phishing-protection.md) 를 참조 하세요 [](https://docs.microsoft.com/powershell/module/exchange/advanced-threat-protection/set-antiphishpolicy?view=exchange-ps).</span><span class="sxs-lookup"><span data-stu-id="ceeb1-113">For more details, see [Anti-phishing protection in Office 365](anti-phishing-protection.md) and [Set-AntiPhishPolicy](https://docs.microsoft.com/powershell/module/exchange/advanced-threat-protection/set-antiphishpolicy?view=exchange-ps).</span></span>

    ![그래픽 인터페이스에서 인증 되지 않은 보낸 사람 편집](media/unverified-sender-article-editing-unauthenticated-senders.jpg)

- <span data-ttu-id="ceeb1-115">관리자가 가양성을 식별 했 고 보낸 사람이 확인 되지 않은 보낸 사람 처리를 수신 하지 않아야 하는 경우 다음 작업 중 하나를 수행 하 여 위장 인텔리전스 스푸핑 허용 목록에 보낸 사람을 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ceeb1-115">If an admin has identified a false positive, and a sender should not be receiving the unverified sender treatment they can take one of the following actions to add the sender to the Spoof Intelligence spoof allow list:</span></span>
        
    - <span data-ttu-id="ceeb1-116">스푸핑 인텔리전스 이해를 통해 도메인 쌍을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="ceeb1-116">Add the domain pair through the Spoof Intelligence Insight.</span></span> <span data-ttu-id="ceeb1-117">자세한 내용은 연습: 스푸핑 인텔리전스 이해를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="ceeb1-117">For more details, see Walkthrough: spoof intelligence insight</span></span>
                
    - <span data-ttu-id="ceeb1-118">Get-phishfilterpolicy cmdlet을 통해 도메인 쌍을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="ceeb1-118">Add the domain pair through the PhishFilterPolicy cmdlet.</span></span> <span data-ttu-id="ceeb1-119">자세한 내용은 Office 365의 Get-phishfilterpolicy 및 스푸핑 방지 보호를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="ceeb1-119">For more details, see Set-PhishFilterPolicy and Anti-spoofing protection in Office 365</span></span>

<span data-ttu-id="ceeb1-120">또한 ETRs (전자 메일 전송 규칙), 안전한 도메인 목록 (스팸 방지 정책), 수신 허용-보낸 사람 목록 또는 사용자가 해당 사용자를 "안전한 보낸 사람"으로 설정 하 여 관리자 허용 목록을 통해 받은 편지 함으로 배달 된 경우에는 확인 되지 않은 보낸 사람 처리가 적용 되지 않습니다. 받은 편지함.</span><span class="sxs-lookup"><span data-stu-id="ceeb1-120">Additionally, we do not apply the unverified sender treatment if it was delivered to the inbox via an admin allow list, including Email Transport Rules (ETRs), Safe Domain List (Anti-Spam Policy), Safe Sender List or a user has set this user as a “Safe Sender” in their inbox.</span></span>

### <a name="you-see-a--in-the-sender-image"></a><span data-ttu-id="ceeb1-121">보낸 사람 이미지에 '? '가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ceeb1-121">You see a '?' in the sender image</span></span>

<span data-ttu-id="ceeb1-122">Outlook.com 및 웹용 Outlook에서 전자 메일 인증 기술을 사용 하 여 보낸 사람의 id를 확인할 수 없는 경우 보낸 사람 사진에 '? '가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ceeb1-122">When Outlook.com and Outlook on the web can't verify the identity of the sender using email authentication techniques, they display a '?' in the sender photo.</span></span> 

![메시지가 확인 통과 되지 않음](media/message-did-not-pass-verification.jpg)

<span data-ttu-id="ceeb1-124">인증에 실패 한 모든 메시지는 악성이 아닙니다.</span><span class="sxs-lookup"><span data-stu-id="ceeb1-124">Not every message that fails to authenticate is malicious.</span></span> <span data-ttu-id="ceeb1-125">그러나 보낸 사람을 인식 하지 못하는 경우 인증을 받지 않는 메시지와 상호 작용할 때는 주의 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ceeb1-125">However, you should be careful about interacting with messages that don't authenticate if you don't recognize the sender.</span></span> <span data-ttu-id="ceeb1-126">또는 일반적으로 보낸 사람 이미지에 '? '가 포함 되지 않는 보낸 사람을 인식할 수 있지만이를 갑자기 보면 보낸 사람이 위장 중 이라고 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ceeb1-126">Or, if you recognize a sender that normally doesn't have a '?' in the sender image, but you suddenly start seeing it, that could be a sign the sender is being spoofed.</span></span>

## <a name="frequently-asked-questions"></a><span data-ttu-id="ceeb1-127">자주하는 질문</span><span class="sxs-lookup"><span data-stu-id="ceeb1-127">Frequently asked questions</span></span>

### <a name="what-criteria-does-outlookcom-and-outlook-on-the-web-use-to-add-the--and-the-via-properties"></a><span data-ttu-id="ceeb1-128">Outlook.com 및 웹용 Outlook에서 '? ' 및 ' via ' 속성을 추가 하는 데 사용 하는 기준은 무엇입니까?</span><span class="sxs-lookup"><span data-stu-id="ceeb1-128">What criteria does Outlook.com and Outlook on the web use to add the '?' and the 'via' properties?</span></span>

<span data-ttu-id="ceeb1-129">보낸 사람 이미지의 '? '에 대해: Outlook.com에서는 메시지가 SPF 또는 DKIM 인증을 통과 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ceeb1-129">For the '?' in the sender image:  Outlook.com requires that the message pass either SPF or DKIM authentication.</span></span> <span data-ttu-id="ceeb1-130">자세한 내용은 office 365에서 [스푸핑 방지](set-up-spf-in-office-365-to-help-prevent-spoofing.md) 및 [Dkim을 사용 하 여 사용자 지정 365 도메인에서 보낸 아웃 바운드 전자 메일의 유효성을 검사 하](use-dkim-to-validate-outbound-email.md)는 데 도움을 주는 방법에 SPF를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ceeb1-130">For more details, see [Set up SPF in Office 365 to help prevent spoofing](set-up-spf-in-office-365-to-help-prevent-spoofing.md) and [Use DKIM to validate outbound email sent from your custom domain in Office 365](use-dkim-to-validate-outbound-email.md).</span></span>

<span data-ttu-id="ceeb1-131">Via 태그의 경우: 보낸 사람 주소에 있는 도메인이 DKIM 서명 또는 SMTP 메일에서 보낸 도메인과 다른 경우 Outlook.com는 해당 두 필드 중 하나에 도메인을 표시 합니다 (DKIM 서명 우선).</span><span class="sxs-lookup"><span data-stu-id="ceeb1-131">For the via tag: If the domain in the From address is different from the domain in the DKIM signature or the SMTP MAIL FROM, Outlook.com displays the domain in one of those two fields (preferring the DKIM signature).</span></span>

### <a name="how-do-i-remove-the-"></a><span data-ttu-id="ceeb1-132">'? '를 제거 하려면 어떻게 해야 합니까?</span><span class="sxs-lookup"><span data-stu-id="ceeb1-132">How do I remove the '?'</span></span>

<span data-ttu-id="ceeb1-133">보낸 사람 이미지의 '? '에 대해 보낸 사람으로 서 SPF 또는 DKIM 중 하나를 사용 하 여 메시지를 인증 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ceeb1-133">For the '?' in the sender image: As a sender, you should authenticate your message with either SPF or DKIM.</span></span>

<span data-ttu-id="ceeb1-134">Via 태그: 보낸 사람으로 서, DKIM 서명 또는 SMTP 메일의 도메인은 From 주소에 있는 도메인과 같거나 그 하위 도메인 인지 확인 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ceeb1-134">For the via tag: As a sender, you should ensure that either the domain in the DKIM signature or the SMTP MAIL FROM is the same as, or is a subdomain of, the domain in the From address.</span></span>

### <a name="does-outlookcom-and-outlook-on-the-web-show-this-for-every-message-that-doesnt-pass-authentication"></a><span data-ttu-id="ceeb1-135">Outlook.com 및 웹용 Outlook에서 인증을 통과 하지 않는 모든 메시지를 표시 하나요?</span><span class="sxs-lookup"><span data-stu-id="ceeb1-135">Does Outlook.com and Outlook on the web show this for every message that doesn’t pass authentication?</span></span>

<span data-ttu-id="ceeb1-136">꼭 필요 하지는 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ceeb1-136">Not necessarily.</span></span> <span data-ttu-id="ceeb1-137">Outlook.com 및 웹용 Outlook의 메시지에는 보낸 사람을 인증 하기 위한 다른 속성이 있을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ceeb1-137">Outlook.com and Outlook on the web may have other properties within the message to authenticate the sender.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ceeb1-138">관련 항목</span><span class="sxs-lookup"><span data-stu-id="ceeb1-138">Related topics</span></span>

[<span data-ttu-id="ceeb1-139">Outlook.com 전자 메일 계정 보호</span><span class="sxs-lookup"><span data-stu-id="ceeb1-139">Help protect your Outlook.com email account</span></span>](https://support.office.com/article/a4f20fc5-4307-4ece-8231-6d4d4bd8a9ba)

[<span data-ttu-id="ceeb1-140">Outlook.com에서 불건전, 피싱 또는 스푸핑 처리</span><span class="sxs-lookup"><span data-stu-id="ceeb1-140">Deal with abuse, phishing, or spoofing in Outlook.com</span></span>](https://support.office.com/article/0d882ea5-eedc-4bed-aebc-079ffa1105a3)

[<span data-ttu-id="ceeb1-141">웹용 Outlook에서 정크 메일 및 스팸 필터링</span><span class="sxs-lookup"><span data-stu-id="ceeb1-141">Filter junk email and spam in Outlook on the web</span></span>](https://support.office.com/article/db786e79-54e2-40cc-904f-d89d57b7f41d)
