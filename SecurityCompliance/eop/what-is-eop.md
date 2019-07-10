---
title: EOP 란
ms.author: tracyp
author: msfttracyp
ms.reviewer: andypunt
manager: dansimp
ms.date: 02/25/2019
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 393b0050-7c7e-49e6-a03d-b1e09fe4de9e
description: 이 소개 문서는 EOP (Exchange Online Protection) 및 몇 가지 중요 한 용어를 이해 하는 데 도움이 됩니다. 이 기능은 exchange Online 클라우드 호스팅 사서함을 보호 하는 Office 365 고객 및 Exchange Server 2016와 같은 온-프레미스 사서함을 보호 하는 EOP 독립 실행형 고객에 게 적용 됩니다.
ms.openlocfilehash: b0d3aac6e2c7e70ce298309d2053a7d6bb5920c1
ms.sourcegitcommit: 32ecff689ae32c59a39b7633ca0f36a304e7516e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/09/2019
ms.locfileid: "35599464"
---
## <a name="what-is-exchange-online-protection-eop"></a><span data-ttu-id="ba782-104">EOP (Exchange Online Protection)</span><span class="sxs-lookup"><span data-stu-id="ba782-104">What is Exchange Online Protection (EOP)</span></span>

<span data-ttu-id="ba782-105">EOP (Exchange Online Protection)는 스팸 및 맬웨어로부터 조직을 보호 하는 클라우드 기반 전자 메일 필터링 서비스입니다.</span><span class="sxs-lookup"><span data-stu-id="ba782-105">Exchange Online Protection (EOP) is a cloud-based email filtering service that helps protect your organization against spam and malware.</span></span> <span data-ttu-id="ba782-106">Office 365에 사서함이 있는 경우 서비스의 일부인 것 이므로 EOP에 의해 자동으로 보호 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ba782-106">If you have mailboxes in Office 365, they are automatically protected by EOP since it is part of the service.</span></span> <span data-ttu-id="ba782-107">여기에는 Office 365 및 온-프레미스 둘 다에 사서함이 있는 조직이 포함 되며, 이러한 조직은 일반적으로 하이브리드 시나리오 라고 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba782-107">This includes organizations that have mailboxes in both Office 365 and on-premise, which is commonly known as a hybrid scenario.</span></span> <span data-ttu-id="ba782-108">또한 클라우드에서 사서함이 없지만 온-프레미스 사서함을 보호 하려는 고객에 게는 EOP 독립 실행형을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ba782-108">EOP standalone is also available for customers who do not have mailboxes in the cloud but want to protect their on-premise mailboxes.</span></span> 

<span data-ttu-id="ba782-109">EOP에서 정크 메일 필터링을 시도 하며, 받은 편지함에 사용자가 원하지 않는 콘텐츠가 모두 표시 되지 않도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba782-109">EOP attempts to filter out junk, keeping your Inbox clear of content that users don't want to see.</span></span> <span data-ttu-id="ba782-110">일반적으로 정크 메일은 정크 메일 폴더로 배달 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ba782-110">Normally, junk mail is delivered to the Junk Email folder.</span></span> <span data-ttu-id="ba782-111">사용자가 정크 메일 폴더에서 원하는 작업을 수행 하 고 있는지 확인 하려는 일부 사용자는 자신의 직접 확인을 위한 편리한 방법입니다.</span><span class="sxs-lookup"><span data-stu-id="ba782-111">Some users like to check to make sure the filtering is doing what they want so the Junk Email folder is an easy way for users to check on their own.</span></span>  

> [!TIP]
> <span data-ttu-id="ba782-112">정크 메일 또는 메일 폴더로 잘못 된 전자 메일이 자동으로 배달 되는 경우에는 좋은 방법입니다.</span><span class="sxs-lookup"><span data-stu-id="ba782-112">It is a good thing when junk or otherwise bad email goes into the Junk Email folder automatically.</span></span> <span data-ttu-id="ba782-113">서비스는 기본 또는 사용자 지정 관리자 설정 상태에 따라 필요한 작업을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba782-113">The service will do what is necessary based on what the default or the custom admin settings state.</span></span> <span data-ttu-id="ba782-114">즉, 사용자는 정크 메일 폴더에 많은 스팸 메일을 표시 하는 것을 걱정할 필요가 없습니다.</span><span class="sxs-lookup"><span data-stu-id="ba782-114">In other words, users should not worry about seeing a lot of spam mail in the Junk Email folder.</span></span> <span data-ttu-id="ba782-115">관리자가 모든 정크 메일을 더 이상 이동 하지 않으려면 격리를 구성 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba782-115">If admins prefer to move all junk out of sight, then the Quarantine should be configured.</span></span> <span data-ttu-id="ba782-116">자세한 내용은 [Office 365에서 전자 메일 메시지 격리](../quarantine-email-messages.md) 문서를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="ba782-116">For more details, see the [Quarantine email messages in Office 365](../quarantine-email-messages.md) article.</span></span>

## <a name="important-terms"></a><span data-ttu-id="ba782-117">중요 한 용어</span><span class="sxs-lookup"><span data-stu-id="ba782-117">Important terms</span></span>

<span data-ttu-id="ba782-118">**인바운드:** Office 365에 제공 되는 메시지입니다.</span><span class="sxs-lookup"><span data-stu-id="ba782-118">**Inbound:** Messages that are coming into Office 365.</span></span>

<span data-ttu-id="ba782-119">**아웃 바운드:** 부재 중 365 메시지</span><span class="sxs-lookup"><span data-stu-id="ba782-119">**Outbound:** Messages that are going out of Office 365.</span></span>

<span data-ttu-id="ba782-120">**내부:** 조직 내부에 있는 사람이 조직 내부의 사람에 게 보내는 메시지입니다.</span><span class="sxs-lookup"><span data-stu-id="ba782-120">**Internal:** Messages that are from someone inside the organization to someone inside the organization.</span></span> <span data-ttu-id="ba782-121">여기에는 하이브리드 시나리오에 있고 하나의 사서함이 온-프레미스이 고 다른 사서함이 클라우드에 있을 수 있는 고객도 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ba782-121">This includes customers who are in hybrid scenarios and one mailbox could be on-premise and the other mailbox is in the cloud.</span></span>

<span data-ttu-id="ba782-122">**False 음수 (FN):** 받은 편지 함으로 잘못 전송 되는 스팸 및 기타 정크 메일</span><span class="sxs-lookup"><span data-stu-id="ba782-122">**False Negative (FN):** Spam and other junk that incorrectly gets sent into the inbox.</span></span>

<span data-ttu-id="ba782-123">**가양성 (FP):** 합법적인 메시지가 스팸으로 표시 되 고 정크 메일 폴더 또는 격리에 저장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ba782-123">**False Positive (FP):** Legitimate messages that incorrectly get marked as spam and put into the Junk Email folder or Quarantine.</span></span>

<span data-ttu-id="ba782-124">**스팸 (원치 않는 전자 메일도 알려짐):** 여기에는 상업용 광고, 연쇄 편지, 정치 우편물 등이 제공 됩니다. 사용자가 제품을 요청 하거나 사기를 커밋하려고 시도 하는 스팸 발송자에 대해 등록을 수행 하지 않는 전자 메일입니다.</span><span class="sxs-lookup"><span data-stu-id="ba782-124">**Spam, also known as unsolicited e-mail:** This comes in the form of commercial advertising, chain letters, political mailings, etc. This is email that users do not sign up for and from spammers who are trying to solicit products or attempting to commit fraud.</span></span>

<span data-ttu-id="ba782-125">**피싱:** 피싱은 id 도용 또는 사기를 커밋하기 위해 개인 정보를 제공 하도록 하기 위한 특수 한 유형의 스팸입니다.</span><span class="sxs-lookup"><span data-stu-id="ba782-125">**Phish:** Phishing is a special type of spam that is intended to trick you into giving up personal information for the purpose of committing identity theft or fraud.</span></span> <span data-ttu-id="ba782-126">이 메시지 유형은 일반적으로 악성 링크 또는 첨부 파일을 포함 하지만 항상은 아닙니다.</span><span class="sxs-lookup"><span data-stu-id="ba782-126">This type of message usually contains a malicious link or attachment, but not always.</span></span>

<span data-ttu-id="ba782-127">**스푸핑:** 스푸핑은 스팸 발송자가 보낸 사람 머리글을 위조 하 여 메시지가 실제 원본이 아닌 사람이 나 다른 곳에서 시작 된 것 처럼 보이게 하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="ba782-127">**Spoof:** Spoofing is when spammers forge the FROM header so that messages appear to have originated from someone or somewhere other than the actual source.</span></span> <span data-ttu-id="ba782-128">이는 스팸으로 가능 하지만 가장 일반적으로 사용자를 피싱 하는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ba782-128">This can be spam but most commonly used to phish users.</span></span>

<span data-ttu-id="ba782-129">**가장:** 이 유형의 스팸은 보낸 사람 주소를 위조 하는 방법 이기도 하지만 이름 또는 도메인의 일부를 수정 하 여 실제 원본 처럼 보이도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba782-129">**Impersonation:** This type of spam is also a way to forge the sender address, but it is done by modifying part of the name or domain so that it looks like the real source.</span></span> <span data-ttu-id="ba782-130">예를 들어 자재 명세서의 "l"은 실제로 11이 고 Microsoft의 "o"는 숫자 0으로 대체 되는 Bi11@micr0s0ft.com입니다.</span><span class="sxs-lookup"><span data-stu-id="ba782-130">For example, Bi11@micr0s0ft.com, where the "l" in Bill was actually the number eleven and the "o" in Microsoft was replaced with the number zero.</span></span>

<span data-ttu-id="ba782-131">**대량:** 대량 메일은 회사에서 다른 회사에 정보를 판매할 때 간접적으로 사용자에 게 요청 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba782-131">**Bulk:** Bulk mail is usually solicited by users, although sometimes indirectly when companies sell information to other companies.</span></span> <span data-ttu-id="ba782-132">사용자가 의도적으로 대량 메일 (예: newletters)을 등록 하는 것이 일반적 이지만 나중에는이를 방지 하 고 스팸으로 생각 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="ba782-132">It is common that users intentionally sign up for bulk mail (i.e. newletters) but forget later on and think it is spam.</span></span> <span data-ttu-id="ba782-133">대량 메일 전송에 사용자가 등록 및 불만 수준이 너무 높으면 대량 메일이 스팸으로 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ba782-133">Bulk mail becomes spam when bulk mailers send more than users sign up and complaint levels get too high.</span></span>
