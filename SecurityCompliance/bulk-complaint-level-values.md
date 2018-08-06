---
title: 대량 불만 수준 값
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 3/5/2015
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
ms.assetid: a5b03b3c-37dd-429e-8e9b-2c1b25031794
description: 대량 우편물 보내는 패턴, 콘텐츠 제작 및 목록 입수 방식에는 다릅니다. 일부는 자신의 구독자에 관련 콘텐츠가 포함 된 메시지는 이와 더불어 보내는 좋은 대량 우편물입니다. 이러한 메시지의 받는 몇 불만 생성합니다. 다른 대량 우편물 밀접 하 게 스팸 유사 하 고 받는 사람에 게에서 많은 불만 생성 하는 원치 않는 메시지를 보냅니다. 이러한 유형의 대량 우편물을 구별 하기 위해 대량 우편물에서 메시지를 대량 불만 수준 (BCL) 등급을 할당 됩니다. BCL 등급 범위는 1에서 9 가능성 벌크 메일 발송에 따라 불만 생성 하는 것입니다. BCL 3의 등급은 많은 불만 생성 하지 않을 BCL 9의 등급이 있는 보낸 사람이 받는 사람에서 많은 불만 생성 하는 것 같습니다. Microsoft 내부 및 제 3 자 소스를 사용 하 여 대량 메일을 파악 하 고 적절 한 BCL를 결정 합니다. 이 등급은 모든 메시지의 스팸 방지 Microsoft-X-헤더에 노출 됩니다. 이 메시지 머리글에 대 한 자세한 내용은 스팸 방지 메시지 헤더를 참조 하십시오.
ms.openlocfilehash: adf179ba4a309f2ed22275179013b576888960c6
ms.sourcegitcommit: 22bca85c3c6d946083d3784f72e886c068d49f4a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/06/2018
ms.locfileid: "22026265"
---
# <a name="bulk-complaint-level-values"></a><span data-ttu-id="874e9-112">대량 불만 수준 값</span><span class="sxs-lookup"><span data-stu-id="874e9-112">Bulk Complaint Level values</span></span>

<span data-ttu-id="874e9-p102">대량 우편물 보내는 패턴, 콘텐츠 제작 및 목록 입수 방식에는 다릅니다. 일부는 자신의 구독자에 관련 콘텐츠가 포함 된 메시지는 이와 더불어 보내는 좋은 대량 우편물입니다. 이러한 메시지의 받는 몇 불만 생성합니다. 다른 대량 우편물 밀접 하 게 스팸 유사 하 고 받는 사람에 게에서 많은 불만 생성 하는 원치 않는 메시지를 보냅니다. 이러한 유형의 대량 우편물을 구별 하기 위해 대량 우편물에서 메시지를 대량 불만 수준 (BCL) 등급을 할당 됩니다. BCL 등급 범위는 1에서 9 가능성 벌크 메일 발송에 따라 불만 생성 하는 것입니다. BCL 3의 등급은 많은 불만 생성 하지 않을 BCL 9의 등급이 있는 보낸 사람이 받는 사람에서 많은 불만 생성 하는 것 같습니다. Microsoft 내부 및 제 3 자 소스를 사용 하 여 대량 메일을 파악 하 고 적절 한 BCL를 결정 합니다. 이 등급은 모든 메시지의 **스팸 방지 Microsoft-X-** 헤더에 노출 됩니다. 이 메시지 머리글에 대 한 자세한 내용은 [스팸 방지 메시지 헤더](anti-spam-message-headers.md)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="874e9-p102">Bulk mailers vary in their sending patterns, content creation, and list acquisition practices. Some are good bulk mailers that send wanted messages with relevant content to their subscribers. These messages generate few complaints from recipients. Other bulk mailers send unsolicited messages that closely resemble spam and generate many complaints from recipients. To distinguish these types of bulk mailers, messages from bulk mailers are assigned a Bulk Complaint Level (BCL) rating. BCL ratings range from 1 to 9 depending on how likely the bulk mailer is to generate complaints. A sender that has a rating of BCL 9 is likely to generate many complaints from recipients, whereas a rating of BCL 3 is unlikely to generate many complaints. Microsoft uses both internal and third-party sources to identify bulk mail and determine the appropriate BCL. This rating is exposed in the **X-Microsoft-Antispam** header of every message. For more information about this message header, see [Anti-spam message headers](anti-spam-message-headers.md).</span></span> 
  
<span data-ttu-id="874e9-123">대량 [스팸 필터 정책 구성](configure-your-spam-filter-policies.md)의 단계를 수행 하 여 조직에 필요한 필터링의 원하는 수준을 설정 하려면 BCL 값을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="874e9-123">You can use BCL values to set the desired level of bulk filtering your organization requires by following the steps in [Configure your spam filter policies](configure-your-spam-filter-policies.md).</span></span>
  
<span data-ttu-id="874e9-p103">더 많은 BCL 값 추가 되 고 포함 됩니다 여기 나중에 합니다. 다음 표에서 나열 하 고 현재 사용 중인 BCL 값에 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="874e9-p103">More BCL values are being added and will be included here in the future. The following table lists and describes the BCL values that are currently in use.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="874e9-126">**BCL 값**</span><span class="sxs-lookup"><span data-stu-id="874e9-126">**BCL Value**</span></span> <br/> |<span data-ttu-id="874e9-127">**설명**</span><span class="sxs-lookup"><span data-stu-id="874e9-127">**Description**</span></span> <br/> |
|<span data-ttu-id="874e9-128">0</span><span class="sxs-lookup"><span data-stu-id="874e9-128">0</span></span>  <br/> |<span data-ttu-id="874e9-129">대량 사용자가 보낸에서 메시지 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="874e9-129">The message isn't from a bulk sender.</span></span>  <br/> |
|<span data-ttu-id="874e9-130">1, 2, 3</span><span class="sxs-lookup"><span data-stu-id="874e9-130">1, 2, 3</span></span>  <br/> |<span data-ttu-id="874e9-131">사용자가 보낸 대량 몇 불만 생성 하는 메시지가입니다.</span><span class="sxs-lookup"><span data-stu-id="874e9-131">The message is from a bulk sender that generates few complaints.</span></span>  <br/> |
|<span data-ttu-id="874e9-132">4, 5, 6, 7</span><span class="sxs-lookup"><span data-stu-id="874e9-132">4, 5, 6, 7</span></span>  <br/> |<span data-ttu-id="874e9-133">사용자가 보낸 대량 불만 사항 혼합 번호를 생성 하는 메시지가입니다.</span><span class="sxs-lookup"><span data-stu-id="874e9-133">The message is from a bulk sender that generates a mixed number of complaints.</span></span>  <br/> |
|<span data-ttu-id="874e9-134">8, 9</span><span class="sxs-lookup"><span data-stu-id="874e9-134">8, 9</span></span>  <br/> |<span data-ttu-id="874e9-135">사용자가 보낸 대량 많은 불만 생성 하는 메시지는</span><span class="sxs-lookup"><span data-stu-id="874e9-135">The message is from a bulk sender that generates a high number of complaints</span></span>  <br/> |
   

