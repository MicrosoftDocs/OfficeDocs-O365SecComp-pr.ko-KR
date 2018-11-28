---
title: 연습 - 대시보드에서 통찰력에 이르기까지
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 6/4/2018
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 703c41df-b3e2-4e7e-9eeb-1a0b8d60fb56
description: 방법으로 이동할 수 있습니다는 대시보드의 보안에서 권장된 작업으로는 정보에 알아봅니다 &amp; 준수 센터입니다.
ms.openlocfilehash: 933bf6e86bc1ddce9259d071b69654f68e4dd370
ms.sourcegitcommit: 2cf7f5bb282c971d33e00f65d9982a3f14aec74e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/27/2018
ms.locfileid: "26706152"
---
# <a name="walkthrough---from-a-dashboard-to-an-insight"></a><span data-ttu-id="36a1a-103">연습 - 대시보드에서 통찰력에 이르기까지</span><span class="sxs-lookup"><span data-stu-id="36a1a-103">Walkthrough - From a dashboard to an insight</span></span>

<span data-ttu-id="36a1a-104">처음 사용 하는 경우 [보고서 및 Office 365 보안에 대 한 의견 &amp; 준수 센터](reports-and-insights-in-security-and-compliance.md), 권장 되는 작업 없으며 방법을 쉽게 탐색할 수 대시보드에서 정보를 확인 하는 데 도움이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="36a1a-104">If you're new to [reports and insights in the Office 365 Security &amp; Compliance Center](reports-and-insights-in-security-and-compliance.md), it might help to see how you can easily navigate from a dashboard to an insight and recommended actions.</span></span> 
  
<span data-ttu-id="36a1a-p101">보안에 대 한 여러 연습 중 하나가 &amp; 준수 센터입니다. 추가 연습 [관련된 항목](#related-topics) 섹션을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="36a1a-p101">This is one of several walkthroughs for the Security &amp; Compliance Center. To see additional walkthroughs, see the [Related topics](#related-topics) section.</span></span> 
  
## <a name="walkthrough-from-a-dashboard-to-an-insight"></a><span data-ttu-id="36a1a-107">연습:에서 파악 하는 대시보드</span><span class="sxs-lookup"><span data-stu-id="36a1a-107">Walkthrough: From a dashboard to an insight</span></span>

<span data-ttu-id="36a1a-p102">과정을 살펴보겠습니다 흐름에서 대시보드를 파악 하 고 작업을 보고서에 합니다. ( [스푸핑 인텔리전스](learn-about-spoof-intelligence.md) 간단한 예제입니다.)</span><span class="sxs-lookup"><span data-stu-id="36a1a-p102">Let's walk through the flow from a dashboard to a report to an insight and action. (This is a brief [spoof intelligence](learn-about-spoof-intelligence.md) example.)</span></span> 
  
1. <span data-ttu-id="36a1a-p103">보안 대시보드로 시작 하는 것은 [보안 &amp; 준수 센터](https://security.microsoft.com)합니다. ( **위협 관리** 로 이동 \> **대시보드**.)</span><span class="sxs-lookup"><span data-stu-id="36a1a-p103">We begin with the Security dashboard in the [Security &amp; Compliance Center](https://security.microsoft.com). (Go to **Threat management** \> **Dashboard**.)</span></span>
    
    ![보안에서 &amp; 준수 센터 위협 관리를 선택 \> 대시보드](media/05a38660-eb13-4960-a266-11809c453d95.png)
  
2. <span data-ttu-id="36a1a-p104">**정보** 행에는 필요한 정보를 나타내는 의심 스러운 될 수 있는 일부 도메인을 검토 해야을 발견 했습니다. ( **통찰력** 행 **도메인 쌍**를 클릭 합니다.)</span><span class="sxs-lookup"><span data-stu-id="36a1a-p104">In the **Insights** row, we notice an insight indicating we need to review some domains that might be suspicious. (In the **Insights** row, click **Domain pairs**.)</span></span>
    
    ![정보 행 스푸핑 잠재적인 문제를 언급합니다.](media/dd1d0cb3-3201-45d7-b41d-18a0944fe85d.png)
  
3. <span data-ttu-id="36a1a-p105">인텔리전스 스푸핑할와 관련 된 작업의 목록을 살펴봅니다. 현재 조직에서 제공 되지만, 실제로 보낸 다른 조직에서 처럼 보이게 하는 전자 메일 메시지를 보낸 여기서 인스턴스는입니다. 목표 여부 위장 된 메시지는 권한이 있는지 여부를 결정 하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="36a1a-p105">We get a list of activities related to spoof intelligence. These are instances where email messages were sent that look like they came from our organization but were, in fact, sent from another organization. The goal is to determine whether the spoofed messages are authorized or not.</span></span>
    
    ![스푸핑 인텔리전스 정보](media/a2e2b4fd-0c1e-499f-8401-cf3089da82fa.png)
  
    <span data-ttu-id="36a1a-p106">이 목록에 메시지 수, 마지막 찾았습니다 스푸핑을 날짜 등으로 정보를 정렬할 수 있습니다. (예: **메시지를 계산** 또는 **마지막으로 본** 어떻게 정렬 works을 참조 하려면 열 머리글을 클릭 합니다.)</span><span class="sxs-lookup"><span data-stu-id="36a1a-p106">In this list, we can sort the information by message count, date the spoofing was last detected, and more. (Click column headings, such as **Message count** or **Last seen** to see how sorting works.)</span></span> 
    
4. <span data-ttu-id="36a1a-p107">목록에서 항목을 선택 하면 검색 된 비슷한 전자 메일 메시지를 포함 하 여 추가 정보를 볼 수는 세부 정보 창을 열립니다. (목록에서 항목을 클릭 하 고 정보 및 권장 사항을 검토 합니다.)</span><span class="sxs-lookup"><span data-stu-id="36a1a-p107">Selecting an item in the list opens a details pane where we can see additional information, including similar email messages that were detected. (Click an item in the list, and review the information and recommendations.)</span></span>
    
    ![세부 정보 창에 열립니다 항목을 선택 하면](media/7ad1faa5-6ca2-474e-a609-eb275e0a8e59.png)
  
5. <span data-ttu-id="36a1a-p108">주의 표시 창 맨 보낸 사람이 조직의 수신 허용된 목록에 추가 하는 옵션을 포함 했습니다. (선택 하지 마십시오 **'AllowedtoSpoof' 보낸 사람에 게 추가 목록에서 허용** 하는이 작업을 수행 하 시겠습니까 때까지. [스푸핑 인텔리전스에 자세히 알아보십시오](learn-about-spoof-intelligence.md).)</span><span class="sxs-lookup"><span data-stu-id="36a1a-p108">Notice that at the top of the pane, we have the option to add the sender to our organization's allowed senders list. (Do not select **Add to 'AllowedtoSpoof' sender allow list** until you are sure you want to do this. [Learn more about spoof intelligence](learn-about-spoof-intelligence.md).)</span></span>
    
    ![보낸사람을 인증할 수 있습니다.](media/caf0c20a-6047-486d-8060-5a229a3de49f.png)
  
<span data-ttu-id="36a1a-129">이와 같은 방식으로 대시보드에서 인 사이트를 이동할 수는 및 권장 되는 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="36a1a-129">In this way, we can move from a dashboard to insights and recommended actions.</span></span>
  
## <a name="related-topics"></a><span data-ttu-id="36a1a-130">관련 항목</span><span class="sxs-lookup"><span data-stu-id="36a1a-130">Related topics</span></span>

[<span data-ttu-id="36a1a-131">연습:는 정보에 대 한 자세한 보고서에서</span><span class="sxs-lookup"><span data-stu-id="36a1a-131">Walkthrough: From an insight to a detailed report</span></span>](from-an-insight-to-a-detailed-report.md)
  
[<span data-ttu-id="36a1a-132">연습:는 정보에 대 한 자세한 보고서에서</span><span class="sxs-lookup"><span data-stu-id="36a1a-132">Walkthrough: From a detailed report to an insight</span></span>](from-a-detailed-report-to-an-insight.md)
  

