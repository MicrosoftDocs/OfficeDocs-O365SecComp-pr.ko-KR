---
title: 큐 알림 및 큐
ms.author: chrisda
author: chrisda
manager: serdars
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.assetid: 37640c80-ce6f-47e2-afd1-bc1d3c50e637
description: 관리자는 Office 365 Security & 준수 센터의 메일 흐름 대시보드의 큐 경고 및 큐에 대해 알아볼 수 있습니다.
ms.openlocfilehash: 6abfe9e8b3edfc6b0ca02e11a9713dcdb5c19b7c
ms.sourcegitcommit: 6aa82374eef09d2c1921f93bda3eabeeb28aadeb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/06/2019
ms.locfileid: "30454870"
---
# <a name="queue-alerts-and-queues"></a><span data-ttu-id="af6a3-103">큐 알림 및 큐</span><span class="sxs-lookup"><span data-stu-id="af6a3-103">Queue alerts and Queues</span></span>

## <a name="queue-alerts"></a><span data-ttu-id="af6a3-104">큐 알림</span><span class="sxs-lookup"><span data-stu-id="af6a3-104">Queue alerts</span></span>

<span data-ttu-id="af6a3-105">커넥터를 사용 하 여 office 365 조직에서 온-프레미스 또는 파트너 전자 메일 서버로 메시지를 보낼 수 없는 경우 해당 메시지는 Office 365에 대기 됩니다.</span><span class="sxs-lookup"><span data-stu-id="af6a3-105">When messages can't be sent from your Office 365 organization to your on-premises or partner email servers using connectors, the messages are queued in Office 365.</span></span> <span data-ttu-id="af6a3-106">이러한 상황을 일으키는 일반적인 예는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="af6a3-106">Common examples that cause this condition are:</span></span>

- <span data-ttu-id="af6a3-107">커넥터가 올바르게 구성 되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="af6a3-107">The connector is incorrectly configured.</span></span>

- <span data-ttu-id="af6a3-108">온-프레미스 환경에 네트워킹이 나 방화벽이 변경 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="af6a3-108">There have been networking or firewall changes in your on-premises environment.</span></span>

<span data-ttu-id="af6a3-109">Office 365는 48 시간 동안 배달 다시 시도를 계속 합니다.</span><span class="sxs-lookup"><span data-stu-id="af6a3-109">Office 365 will continue to retry to delivery for 48 hours.</span></span> <span data-ttu-id="af6a3-110">48 시간이 지난 후에는 메시지가 만료 되어 배달 못 함 보고서 (ndr 또는 바운스 메시지로도 알려짐)의 보낸 사람에 게 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="af6a3-110">After 48 hours, the messages will expire and will be returned to the senders in non-delivery reports (also known as a NDRs or bounce messages).</span></span>

<span data-ttu-id="af6a3-111">큐에 대기 중인 전자 메일 볼륨이 미리 정의 된 임계값을 초과 하는 경우 (기본값은 2000 메시지), 해당 경고는 **최근 경고**의 메일 흐름 대시보드에서 사용할 수 있으며 관리자는 전자 메일 알림 (대체 전자 메일 주소에 대 한)을 받게 됩니다. .</span><span class="sxs-lookup"><span data-stu-id="af6a3-111">If the queued email volume exceeds the pre-defined threshold (the default value is 2000 messages), the alerts will be available in the mail flow dashboard at **Recent alerts**, and admins will receive an email notification (to their alternative email address).</span></span> <span data-ttu-id="af6a3-112">경고 임계값, 일별 알림 제한 및/또는 받는 사람을 구성 하려면 아래의 **큐 경고 사용자 지정** 섹션을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="af6a3-112">To configure the alert threshold, daily notification limit, and/or recipients of the alert, see the **Customize queue alerts** section below.</span></span>

![Office 365 보안 & 준수 센터에서 메일 흐름 대시보드의 최근 경고 영역에 있는 큐 알림](media/5fc4a51c-6118-4270-960b-c6b176ef94ae.png)

## <a name="customize-queue-alerts"></a><span data-ttu-id="af6a3-114">큐 알림 사용자 지정</span><span class="sxs-lookup"><span data-stu-id="af6a3-114">Customize queue alerts</span></span>

<span data-ttu-id="af6a3-115">메일 흐름 정보 만들기 경고 정책에서 \*\*\*\* \> \*\*\*\* 찾은 메시지 (아래 예제 스크린샷의 **전자 메일 알림 보내기** 확인란) **가 지연 되었습니다** .</span><span class="sxs-lookup"><span data-stu-id="af6a3-115">Mail flow insights create an alert policy named **Messages have been delayed** (the **Send email notifications** check box in the example screen shot below) found in **Alerts** \> **Alert Policies**.</span></span> <span data-ttu-id="af6a3-116">정책을 클릭 하 여 임계값 및 알림 받는 사람을 수정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="af6a3-116">You can modify the threshold and alert recipients by clicking on the policy.</span></span>

![알림 탐색](media/efb95976-9e0b-484e-a2fd-093c5bc7a40f.png)

<span data-ttu-id="af6a3-118">이제 **정책 편집**을 클릭 하 여 새 정책 정보 블레이드에서 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="af6a3-118">You'll see a new policy information blade, you can now click **Edit Policy**.</span></span>

![정책 편집 ](media/ed2aceae-3ee2-4849-a17e-87915987a7dd.png)

<span data-ttu-id="af6a3-120">정보 블레이드에서 **편집 정책**으로 변경 됩니다.</span><span class="sxs-lookup"><span data-stu-id="af6a3-120">The information blade will change to the **Edit Policy**.</span></span> <span data-ttu-id="af6a3-121">이제 경고 전자 메일에 대 한 받는 사람, 하루에 전송 되는 알림 수에 대 한 제한 및 경고를 트리거하기 위한 최소 임계값 (200 이상)을 변경할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="af6a3-121">You can now change the recipients for the alert email, the limit on the number of notifications sent per day, and the minimum threshold to trigger the alert (200 or more).</span></span>

![정책 블레이드 편집](media/c657cc74-7867-474c-b2c9-dc478449f990.png)

## <a name="queue-alert-details"></a><span data-ttu-id="af6a3-123">큐 알림 세부 정보</span><span class="sxs-lookup"><span data-stu-id="af6a3-123">Queue alert details</span></span>

<span data-ttu-id="af6a3-124">알림을 클릭 하면 알림 세부 정보가 플라이 아웃 창에 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="af6a3-124">When you click the alert, the alert details appear in a flyout pane.</span></span>

![Office 365 보안 & 준수 센터의 메일 흐름 대시보드의 최근 경고 영역에서 큐 알림 선택](media/1f6b0e96-5b2c-41ef-9684-9d813b3fabe6.png)

![Office 365 Security & 준수 센터의 큐 알림 세부 정보 플라이 아웃](media/105c8fff-912f-4763-8806-2740ebdecd4b.png)

<span data-ttu-id="af6a3-127">알림 세부 정보에서 **큐 보기** 를 클릭 하 여 큐 세부 정보, 문제 및 새 플라이 아웃 창에서 사용 가능한 수정 사항에 대 한 링크를 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="af6a3-127">You can click **View queue** in the alert details to see the queue details, problems, and links to the available fixes in a new flyout pane.</span></span>

![Office 365 Security & 준수 센터의 큐 알림 세부 정보 플라이 아웃](media/8ff60955-55ef-4f32-a966-85e02cb608d1.png)

![알림 세부 정보의 큐 보기](media/4eb088fe-5dd9-4bf4-b959-c1bb2545c515.png)

## <a name="queues"></a><span data-ttu-id="af6a3-130">큐</span><span class="sxs-lookup"><span data-stu-id="af6a3-130">Queues</span></span>

<span data-ttu-id="af6a3-131">대기 중인 메시지 볼륨이 임계값을 초과 하지 않은 경우에도 메일 흐름 대시보드의 **queue (큐** ) 영역을 사용 하 여 1 시간 이상 대기 된 메시지를 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="af6a3-131">Even if the queued message volume hasn't exceeded the threshold, you can still use the **Queues** area of the mail flow dashboard to see messages that have been queued for more than one hour.</span></span> <span data-ttu-id="af6a3-132">**큐** 영역을 사용 하 여 대기 중인 메시지 수를 모니터링 하 고 (값은 메일 흐름이 양호 함을 나타냄) 대기 중인 메시지 수가 너무 커지지 않도록 조치를 취할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="af6a3-132">You can use the **Queues** area to monitor the number of queued messages (the value 0 indicates mail flow is OK) and take action before the number of queued messages becomes too large.</span></span>

![Office 365 Security & 준수 센터의 메일 흐름 대시보드의 큐](media/0ef6e2ef-dd22-4363-9d4a-b20a00babc9f.png)

<span data-ttu-id="af6a3-134">**큐**에서 대기 중인 메시지 수를 클릭 하면 문제를 해결 하는 방법에 대 한 큐 세부 정보 및 지침이 플라이 아웃 창 (큐 경고의 세부 정보에서 **큐 보기** 를 클릭 하면 표시 되는 동일한 플라이 아웃)에 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="af6a3-134">When you click the number of queued messages in **Queues**, the queue details and guidance for how to fix the issue will appear in a flyout pane (the same flyout that appears after you click **View queue** in the details of a queue alert).</span></span>

![큐 세부 정보](media/4eb088fe-5dd9-4bf4-b959-c1bb2545c515.png)
