---
title: 큐 경고 및 큐
ms.author: chrisda
author: chrisda
manager: serdars
ms.date: ''
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 37640c80-ce6f-47e2-afd1-bc1d3c50e637
description: 관리자가 Office 365 보안 & 준수 센터에서에서 메일 흐름 대시보드에서 큐 경고 및 큐에 대 한 알아보십시오.
ms.openlocfilehash: fe750e32136af095bb0ccff8544306db76a7a667
ms.sourcegitcommit: 25fb33a1f8b2844fde15f6c03db2936c610824e0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28685577"
---
# <a name="queue-alerts-and-queues"></a><span data-ttu-id="314bd-103">큐 경고 및 큐</span><span class="sxs-lookup"><span data-stu-id="314bd-103">Queue alerts and Queues</span></span>

## <a name="queue-alerts"></a><span data-ttu-id="314bd-104">큐 알림</span><span class="sxs-lookup"><span data-stu-id="314bd-104">Queue alerts</span></span>

<span data-ttu-id="314bd-p101">온-프레미스에 Office 365 조직에서 메시지를 보낼 수 없는 경우 또는 커넥터를 사용 하 여 파트너 전자 메일 서버, 메시지는 Office 365에서 대기 됩니다. 이 조건은 발생 하는 일반적인 예는.</span><span class="sxs-lookup"><span data-stu-id="314bd-p101">When messages can't be sent from your Office 365 organization to your on-premises or partner email servers using connectors, the messages are queued in Office 365. Common examples that cause this condition are:</span></span>

- <span data-ttu-id="314bd-107">커넥터는 잘못 구성 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="314bd-107">The connector is incorrectly configured.</span></span>

- <span data-ttu-id="314bd-108">온-프레미스 환경에서 네트워킹 또는 방화벽 변경 사항이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="314bd-108">There have been networking or firewall changes in your on-premises environment.</span></span>

<span data-ttu-id="314bd-p102">Office 365 48 시간에 대 한 배달에 다시 시도를 계속 됩니다. 48 시간이 지나면 메시지 만료 됩니다 및 배달 못함 보고서에서 보낸 사람에 게 반환 됩니다 (Ndr로도 알려져 메시지 바운드 또는).</span><span class="sxs-lookup"><span data-stu-id="314bd-p102">Office 365 will continue to retry to delivery for 48 hours. After 48 hours, the messages will expire and will be returned to the senders in non-delivery reports (also known as a NDRs or bounce messages).</span></span>

<span data-ttu-id="314bd-p103">알림 **최근 경고**메일 흐름 대시보드에서 사용할 수 있습니다 및 관리자가 대체 전자 메일 주소) (에 전자 메일 알림을 받게 됩니다 (기본값은 2000 메시지) 미리 정의 된 임계값을 초과 하는 큐에 대기 중인된 전자 메일 볼륨을 하는 경우 . 경고 임계값, 일별 알림 제한 및/또는 받는 사람에 게 경고를 구성 하려면 아래의 **사용자 지정 큐 알림** 섹션을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="314bd-p103">If the queued email volume exceeds the pre-defined threshold (the default value is 2000 messages), the alerts will be available in the mail flow dashboard at **Recent alerts**, and admins will receive an email notification (to their alternative email address). To configure the alert threshold, daily notification limit, and/or recipients of the alert, see the **Customize queue alerts** section below.</span></span>

![Office 365 보안 & 준수 센터의에서 메일 흐름 대시보드의 최근 알림 영역에서 큐 알림](media/5fc4a51c-6118-4270-960b-c6b176ef94ae.png)

## <a name="customize-queue-alerts"></a><span data-ttu-id="314bd-114">큐 경고를 사용자 지정</span><span class="sxs-lookup"><span data-stu-id="314bd-114">Customize queue alerts</span></span>

<span data-ttu-id="314bd-p104">메일 흐름 통찰력 **알림** 에 있는 명명 된 **메시지가 지연 되었습니다** ( **전자 메일 알림 메시지 보내기** 확인란 아래 예제 스크린샷에서) 경고 정책 만들기 \> **경고 정책**입니다. 정책에서를 클릭 하 여 임계값 및 알림을 받는 사람을 수정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="314bd-p104">Mail flow insights create an alert policy named **Messages have been delayed** (the **Send email notifications** check box in the example screen shot below) found in **Alerts** \> **Alert Policies**. You can modify the threshold and alert recipients by clicking on the policy.</span></span>

![알림 탐색](media/efb95976-9e0b-484e-a2fd-093c5bc7a40f.png)

<span data-ttu-id="314bd-118">새 정책 정보 블레이드를 볼 수 있습니다, **정책 편집**을 클릭할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="314bd-118">You'll see a new policy information blade, you can now click **Edit Policy**.</span></span>

![정책 편집 ](media/ed2aceae-3ee2-4849-a17e-87915987a7dd.png)

<span data-ttu-id="314bd-p105">**정책 편집**정보 블레이드 변경 됩니다. 이제 경고 전자 메일 알림 (200 개 이상의) 경고를 트리거할 수 일 및 최소 임계값 당 보낸 개수에 제한에 대 한 받는 사람을 변경할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="314bd-p105">The information blade will change to the **Edit Policy**. You can now change the recipients for the alert email, the limit on the number of notifications sent per day, and the minimum threshold to trigger the alert (200 or more).</span></span>

![정책 블레이드 편집](media/c657cc74-7867-474c-b2c9-dc478449f990.png)

## <a name="queue-alert-details"></a><span data-ttu-id="314bd-123">큐 알림 세부 정보</span><span class="sxs-lookup"><span data-stu-id="314bd-123">Queue alert details</span></span>

<span data-ttu-id="314bd-124">알림을 클릭 하면 경고 세부 정보가 플라이 아웃 창에 나타납니다.</span><span class="sxs-lookup"><span data-stu-id="314bd-124">When you click the alert, the alert details appear in a flyout pane.</span></span>

![Office 365 보안 & 준수 센터의에서 메일 흐름 대시보드의 최근 알림 영역에서 큐 경고를 선택 합니다.](media/1f6b0e96-5b2c-41ef-9684-9d813b3fabe6.png)

![큐 경고 세부 정보 플라이 아웃 Office 365 보안 & 준수 센터의](media/105c8fff-912f-4763-8806-2740ebdecd4b.png)

<span data-ttu-id="314bd-127">큐 세부 정보, 문제 및 새 플라이 아웃 창에서 사용할 수 있는 수정 사항에 대 한 링크를 참조 하는 경고 정보에 **큐 보기를** 클릭 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="314bd-127">You can click **View queue** in the alert details to see the queue details, problems, and links to the available fixes in a new flyout pane.</span></span>

![큐 경고 세부 정보 플라이 아웃 Office 365 보안 & 준수 센터의](media/8ff60955-55ef-4f32-a966-85e02cb608d1.png)

![경고 세부 정보에 큐 보기](media/4eb088fe-5dd9-4bf4-b959-c1bb2545c515.png)

## <a name="queues"></a><span data-ttu-id="314bd-130">큐</span><span class="sxs-lookup"><span data-stu-id="314bd-130">Queues</span></span>

<span data-ttu-id="314bd-p106">큐에 대기 중인된 메시지 볼륨 임계값을 초과 하지 않은, 하는 경우에 1 시간 이상에 대 한 큐에 대기 중인 메시지를 참조 하는 메일 흐름 대시보드의 **큐** 영역을 사용할 수 있습니다. (값이 0 임을 메일 흐름 확인) 큐에 대기 중인된 메시지 수를 모니터링 하 고 큐에 대기 중인된 메시지 수가 너무 커지면 전에 작업을 수행 하려면 **큐** 영역을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="314bd-p106">Even if the queued message volume hasn't exceeded the threshold, you can still use the **Queues** area of the mail flow dashboard to see messages that have been queued for more than one hour. You can use the **Queues** area to monitor the number of queued messages (the value 0 indicates mail flow is OK) and take action before the number of queued messages becomes too large.</span></span>

![Office 365 보안 & 준수 센터에서에서 메일 흐름 대시보드에서 큐](media/0ef6e2ef-dd22-4363-9d4a-b20a00babc9f.png)

<span data-ttu-id="314bd-134">때 **큐**의 큐 세부 정보에서에서 큐에 대기 중인된 메시지의 번호를 클릭 하 고 문제를 해결 하는 방법에 대 한 지침 (동일한 플라이 아웃 큐 경고의 세부 정보에 **큐 보기를** 클릭 한 후 표시 되 면) 플라이 아웃 창에 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="314bd-134">When you click the number of queued messages in **Queues**, the queue details and guidance for how to fix the issue will appear in a flyout pane (the same flyout that appears after you click **View queue** in the details of a queue alert).</span></span>

![큐 세부 정보](media/4eb088fe-5dd9-4bf4-b959-c1bb2545c515.png)
