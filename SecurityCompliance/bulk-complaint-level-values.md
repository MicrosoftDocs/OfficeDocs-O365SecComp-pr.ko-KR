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
search.appverid:
- MET150
ms.assetid: a5b03b3c-37dd-429e-8e9b-2c1b25031794
ms.collection:
- M365-security-compliance
description: 대량 메일 발송은 해당 보내는 패턴, 콘텐츠 작성 및 목록 가져오기 방법에 따라 달라 집니다. 일부는 관련 콘텐츠가 포함 된 메시지를 구독자에 게 보내는 좋은 대량 메일입니다. 이러한 메시지는 받는 사람의 불만을 거의 발생 시킵니다. 기타 대량 메일 전송 스팸과 유사한 원치 않는 메시지를 보내며 받는 사람 으로부터 많은 불만을 생성 합니다. 이러한 유형의 대량 메일을 구별 하기 위해 대량 우편물의 메시지에 BCL (대량 불만 수준) 등급이 할당 됩니다. BCL 등급은 대량 메일에 불만을 생성 하기 위해 얼마나 큰 지에 따라 1에서 9 사이의 범위를 가집니다. bcl 9의 등급이 있는 보낸 사람은 받는 사람에 게 많은 불만을 생성할 수 있는 반면, bcl 3의 등급은 많은 불만을 생성할 가능성이 적습니다. Microsoft에서는 내부 및 타사 소스를 모두 사용 하 여 대량 메일을 식별 하 고 적절 한 BCL을 결정 합니다. 이 등급은 모든 메시지의 스팸 방지 헤더에 표시 됩니다. 이 메시지 헤더에 대 한 자세한 내용은 스팸 방지 메시지 헤더를 참조 하세요.
ms.openlocfilehash: a948e90ba436dcfdb78df856e090983e6015bb0a
ms.sourcegitcommit: 686bc9a8f7a7b6810a096f07d36751d10d334409
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/26/2019
ms.locfileid: "30276018"
---
# <a name="bulk-complaint-level-values"></a><span data-ttu-id="2ed44-112">대량 불만 수준 값</span><span class="sxs-lookup"><span data-stu-id="2ed44-112">Bulk Complaint Level values</span></span>

<span data-ttu-id="2ed44-p102">대량 메일 발송은 해당 보내는 패턴, 콘텐츠 작성 및 목록 가져오기 방법에 따라 달라 집니다. 일부는 관련 콘텐츠가 포함 된 메시지를 구독자에 게 보내는 좋은 대량 메일입니다. 이러한 메시지는 받는 사람의 불만을 거의 발생 시킵니다. 기타 대량 메일 전송 스팸과 유사한 원치 않는 메시지를 보내며 받는 사람 으로부터 많은 불만을 생성 합니다. 이러한 유형의 대량 메일을 구별 하기 위해 대량 우편물의 메시지에 BCL (대량 불만 수준) 등급이 할당 됩니다. BCL 등급은 대량 메일에 불만을 생성 하기 위해 얼마나 큰 지에 따라 1에서 9 사이의 범위를 가집니다. bcl 9의 등급이 있는 보낸 사람은 받는 사람에 게 많은 불만을 생성할 수 있는 반면, bcl 3의 등급은 많은 불만을 생성할 가능성이 적습니다. Microsoft에서는 내부 및 타사 소스를 모두 사용 하 여 대량 메일을 식별 하 고 적절 한 BCL을 결정 합니다. 이 등급은 모든 메시지의 **스팸 방지** 헤더에 표시 됩니다. 이 메시지 헤더에 대 한 자세한 내용은 [스팸 방지 메시지 헤더](anti-spam-message-headers.md)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="2ed44-p102">Bulk mailers vary in their sending patterns, content creation, and list acquisition practices. Some are good bulk mailers that send wanted messages with relevant content to their subscribers. These messages generate few complaints from recipients. Other bulk mailers send unsolicited messages that closely resemble spam and generate many complaints from recipients. To distinguish these types of bulk mailers, messages from bulk mailers are assigned a Bulk Complaint Level (BCL) rating. BCL ratings range from 1 to 9 depending on how likely the bulk mailer is to generate complaints. A sender that has a rating of BCL 9 is likely to generate many complaints from recipients, whereas a rating of BCL 3 is unlikely to generate many complaints. Microsoft uses both internal and third-party sources to identify bulk mail and determine the appropriate BCL. This rating is exposed in the **X-Microsoft-Antispam** header of every message. For more information about this message header, see [Anti-spam message headers](anti-spam-message-headers.md).</span></span> 
  
<span data-ttu-id="2ed44-123">BCL 값을 사용 하 여 조직에서 필요한 대량 필터링 수준을 설정 하려면 [스팸 필터 정책 구성](configure-your-spam-filter-policies.md)의 단계를 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ed44-123">You can use BCL values to set the desired level of bulk filtering your organization requires by following the steps in [Configure your spam filter policies](configure-your-spam-filter-policies.md).</span></span>
  
<span data-ttu-id="2ed44-p103">더 많은 BCL 값이 추가 되었으며 나중에 여기에 포함 될 예정입니다. 다음 표에서는 현재 사용 중인 BCL 값을 나열 하 고 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ed44-p103">More BCL values are being added and will be included here in the future. The following table lists and describes the BCL values that are currently in use.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="2ed44-126">**BCL 값**</span><span class="sxs-lookup"><span data-stu-id="2ed44-126">**BCL Value**</span></span> <br/> |<span data-ttu-id="2ed44-127">**설명**</span><span class="sxs-lookup"><span data-stu-id="2ed44-127">**Description**</span></span> <br/> |
|<span data-ttu-id="2ed44-128">개</span><span class="sxs-lookup"><span data-stu-id="2ed44-128">0</span></span>  <br/> |<span data-ttu-id="2ed44-129">메시지가 대량 보낸 사람 으로부터 온 것이 아닙니다.</span><span class="sxs-lookup"><span data-stu-id="2ed44-129">The message isn't from a bulk sender.</span></span>  <br/> |
|<span data-ttu-id="2ed44-130">1, 2, 3</span><span class="sxs-lookup"><span data-stu-id="2ed44-130">1, 2, 3</span></span>  <br/> |<span data-ttu-id="2ed44-131">메시지가 몇 가지 불만을 생성 하는 대량 보낸 사람의 메시지입니다.</span><span class="sxs-lookup"><span data-stu-id="2ed44-131">The message is from a bulk sender that generates few complaints.</span></span>  <br/> |
|<span data-ttu-id="2ed44-132">4, 5, 6, 7</span><span class="sxs-lookup"><span data-stu-id="2ed44-132">4, 5, 6, 7</span></span>  <br/> |<span data-ttu-id="2ed44-133">이 메시지는 수많은 불만을 생성 하는 대량 보낸 사람 으로부터 온 것입니다.</span><span class="sxs-lookup"><span data-stu-id="2ed44-133">The message is from a bulk sender that generates a mixed number of complaints.</span></span>  <br/> |
|<span data-ttu-id="2ed44-134">8, 9</span><span class="sxs-lookup"><span data-stu-id="2ed44-134">8, 9</span></span>  <br/> |<span data-ttu-id="2ed44-135">이 메시지는 많은 수의 불만을 생성 하는 대량 보낸 사람 으로부터 온 것입니다.</span><span class="sxs-lookup"><span data-stu-id="2ed44-135">The message is from a bulk sender that generates a high number of complaints</span></span>  <br/> |
   

