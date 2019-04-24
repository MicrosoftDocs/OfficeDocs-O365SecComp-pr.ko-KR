---
title: 스팸 지수
ms.author: tracyp
author: MSFTTracyP
manager: laurawi
ms.date: 10/2/2017
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 34681000-0022-4b92-b38a-e32b3ed96bf6
ms.collection:
- M365-security-compliance
description: 전자 메일 메시지가 스팸 필터링을 통과 하면 스팸 점수가 할당 됩니다. 이 점수는 개별 SCL (스팸 지 수) 등급에 매핑되며 X-헤더에 스탬프 처리 됩니다. 이 서비스는 SCL 등급의 스팸 신뢰 해석에 따라 메시지에 대 한 작업을 수행 합니다. 다음 표에서는 각 등급에 대 한 인바운드 메시지에 대해 수행 되는 필터 및 각 SCL 등급이 해석 되는 방식을 보여 줍니다.
ms.openlocfilehash: 48ca02bf3f6549c5acc1147ea477b9d22f1c76e1
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32260676"
---
# <a name="spam-confidence-levels"></a><span data-ttu-id="0f6ea-106">스팸 지수</span><span class="sxs-lookup"><span data-stu-id="0f6ea-106">Spam confidence levels</span></span>

<span data-ttu-id="0f6ea-107">전자 메일 메시지가 스팸 필터링을 통과 하면 스팸 점수가 할당 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0f6ea-107">When an email message goes through spam filtering it is assigned a spam score.</span></span> <span data-ttu-id="0f6ea-108">이 점수는 개별 SCL (스팸 지 수) 등급에 매핑되며 X-헤더에 스탬프 처리 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0f6ea-108">That score is mapped to an individual Spam Confidence Level (SCL) rating and stamped in an X-header.</span></span> <span data-ttu-id="0f6ea-109">이 서비스는 SCL 등급의 스팸 신뢰 해석에 따라 메시지에 대 한 작업을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f6ea-109">The service takes actions upon the messages depending upon the spam confidence interpretation of the SCL rating.</span></span> <span data-ttu-id="0f6ea-110">다음 표에서는 각 등급에 대 한 인바운드 메시지에 대해 수행 되는 필터 및 각 SCL 등급이 해석 되는 방식을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="0f6ea-110">The following table shows how the different SCL ratings are interpreted by the filters and the default action that is taken on inbound messages for each rating.</span></span>
  
|<span data-ttu-id="0f6ea-111">**SCL 등급**</span><span class="sxs-lookup"><span data-stu-id="0f6ea-111">**SCL Rating**</span></span>|<span data-ttu-id="0f6ea-112">**scl (스팸 지 수) 해석**</span><span class="sxs-lookup"><span data-stu-id="0f6ea-112">**Spam Confidence Interpretation**</span></span>|<span data-ttu-id="0f6ea-113">**기본 작업**</span><span class="sxs-lookup"><span data-stu-id="0f6ea-113">**Default Action**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="0f6ea-114">-1</span><span class="sxs-lookup"><span data-stu-id="0f6ea-114">-1</span></span>|<span data-ttu-id="0f6ea-115">수신 허용-보낸 사람, 수신 허용-받는 사람 또는 안전한 것으로 표시 된 IP 주소 (신뢰할 수 있는 파트너)에서 오는 스팸 방지</span><span class="sxs-lookup"><span data-stu-id="0f6ea-115">Non-spam coming from a safe sender, safe recipient, or safe listed IP address (trusted partner).</span></span>|<span data-ttu-id="0f6ea-116">받는 사람의 받은 편지 함으로 메시지를 배달 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f6ea-116">Deliver the message to the recipients' inbox.</span></span>|
|<span data-ttu-id="0f6ea-117">0, 1</span><span class="sxs-lookup"><span data-stu-id="0f6ea-117">0, 1</span></span>|<span data-ttu-id="0f6ea-118">메시지가 검사 되었으며 깨끗 한 것으로 확인 되었기 때문에 스팸 아님</span><span class="sxs-lookup"><span data-stu-id="0f6ea-118">Non-spam because the message was scanned and determined to be clean.</span></span>|<span data-ttu-id="0f6ea-119">받는 사람의 받은 편지 함으로 메시지를 배달 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f6ea-119">Deliver the message to the recipients' inbox.</span></span>|
|<span data-ttu-id="0f6ea-120">5, 6</span><span class="sxs-lookup"><span data-stu-id="0f6ea-120">5, 6</span></span>|<span data-ttu-id="0f6ea-121">스팸</span><span class="sxs-lookup"><span data-stu-id="0f6ea-121">Spam</span></span>|<span data-ttu-id="0f6ea-122">받는 사람의 정크 메일 폴더로 메시지를 배달 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f6ea-122">Deliver the message to the recipients' Junk Email folder.</span></span>|
|<span data-ttu-id="0f6ea-123">7, 8, 9</span><span class="sxs-lookup"><span data-stu-id="0f6ea-123">7, 8, 9</span></span>|<span data-ttu-id="0f6ea-124">높은 정확도 스팸</span><span class="sxs-lookup"><span data-stu-id="0f6ea-124">High confidence spam</span></span>|<span data-ttu-id="0f6ea-125">받는 사람의 정크 메일 폴더로 메시지를 배달 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f6ea-125">Deliver the message to the recipients' Junk Email folder.</span></span>|
   
> [!TIP]
> <span data-ttu-id="0f6ea-126">2, 3, 4, 7 및 8의 SCL 등급이 서비스에 의해 설정 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0f6ea-126">SCL ratings of 2, 3, 4, 7, and 8 are not set by the service.</span></span> <span data-ttu-id="0f6ea-127">scl 등급 5 또는 6은 스팸이 아닌 것으로 간주 되며, scl 등급 9 보다 스팸을 덜 하 여 특정 스팸으로 간주 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0f6ea-127">An SCL rating of 5 or 6 is considered suspected spam, which is less certain to be spam than an SCL rating of 9, which is considered certain spam.</span></span> <span data-ttu-id="0f6ea-128">스팸 및 높은 신뢰도 스팸에 대 한 다양 한 작업은 Exchange 관리 센터에서 콘텐츠 필터 정책을 통해 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0f6ea-128">Different actions for spam and high confidence spam can be configured via your content filter policies in the Exchange admin center.</span></span> <span data-ttu-id="0f6ea-129">자세한 내용은 [스팸 필터 정책 구성을](configure-your-spam-filter-policies.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="0f6ea-129">For more information, see [Configure your spam filter policies](configure-your-spam-filter-policies.md).</span></span> <span data-ttu-id="0f6ea-130">또한 [메일 흐름 규칙을 사용 하 여 메시지에 scl (스팸 지 수)을 설정 하는 방법](use-mail-flow-rules-to-set-the-spam-confidence-level-scl-in-messages.md)에 설명 된 대로 메일 흐름 규칙 (전송 규칙이 라고도 함)을 사용 하 여 특정 조건과 일치 하는 메시지에 대 한 SCL 등급을 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0f6ea-130">You can also set the SCL rating for messages that match specific conditions by using mail flow rules (also known as transport rules), as described in [Use mail flow rules to set the spam confidence level (SCL) in messages](use-mail-flow-rules-to-set-the-spam-confidence-level-scl-in-messages.md).</span></span> <span data-ttu-id="0f6ea-131">메일 흐름 규칙을 사용 하 여 SCL 7, 8 또는 9를 설정 하는 경우 메시지가 높은 신뢰도 스팸으로 취급 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0f6ea-131">If you use a mail flow rule to set SCL of 7, 8, or 9 the message will be treated as high confidence spam.</span></span> 
  
||
|:-----|
|<span data-ttu-id="0f6ea-p104">![LinkedIn Learning용 단축 아이콘](media/eac8a413-9498-4220-8544-1e37d1aaea13.png) **Office 365를 처음 사용하시나요?**         LinkedIn Learning에서 제공하는 **Office 365 admins and IT pros**의 무료 비디오 과정을 확인해보세요.</span><span class="sxs-lookup"><span data-stu-id="0f6ea-p104">![The short icon for LinkedIn Learning](media/eac8a413-9498-4220-8544-1e37d1aaea13.png) **New to Office 365?**         Discover free video courses for **Office 365 admins and IT pros**, brought to you by LinkedIn Learning.</span></span>|
   

