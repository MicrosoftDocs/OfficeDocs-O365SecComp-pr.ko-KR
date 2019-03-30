---
title: 상위 도메인 메일 흐름 상태 파악
ms.author: chrisda
author: chrisda
manager: serdars
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.assetid: ''
description: 관리자는 Security & 준수 센터의 메일 흐름 대시보드에 있는 최상위 도메인 메일 흐름 상태 정보에 대해 알아볼 수 있습니다.
ROBOTS: NOINDEX, NOFOLLOW
ms.openlocfilehash: baa69c3373623d4742d6d957a5022012fb60f7e7
ms.sourcegitcommit: e7a776a04ef6ed5e287a33cfdc36aa2d72862b55
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/29/2019
ms.locfileid: "31000671"
---
# <a name="top-domain-mail-flow-status-insight"></a><span data-ttu-id="38ccf-103">상위 도메인 메일 흐름 상태 파악</span><span class="sxs-lookup"><span data-stu-id="38ccf-103">Top domain mail flow status insight</span></span>

> [!NOTE]
> <span data-ttu-id="38ccf-104">이 항목에서 설명 하는 기능은 모든 Office 365 조직에 배포 되지 않으며 변경 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="38ccf-104">The features described in this topic haven't been deployed to all Office 365 organizations, and are subject to change.</span></span>

<span data-ttu-id="38ccf-105">**최상위 도메인 메일 흐름 상태** 정보를 통해 메일 흐름 측면에서 조직의 도메인에 대 한 현재 상태를 알 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="38ccf-105">The **Top domain mail flow status** insight gives you the current status for your organization's domains in terms of mail flow.</span></span> <span data-ttu-id="38ccf-106">이러한 통찰력은 ***메일 흐름에 영향*** 을 주는 (예: 외부 전자 메일을 받을 수 없음), 특히 도메인 만료 또는 잘못 된 MX 레코드가 있는 도메인의 문제를 파악 하 고 문제를 해결 하는 데 도움이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="38ccf-106">This insight helps you identify and troubleshoot domains that are experiencing ***mail flow impacting*** issues (for example, unable to receive external email), especially domain expirations or domains with incorrect MX records.</span></span>

![보안 & 준수 센터의 메일 흐름 대시보드에서 가장 중요 한 도메인 흐름 상태를 파악 합니다.](media/domain-mail-flow-status-selected.png)

<span data-ttu-id="38ccf-108">**자세한 내용은 자세히 보기** 를 클릭 하면 각 도메인의 상태에 대 한 세부 정보를 보여 주는 플라이 아웃이 나타납니다.</span><span class="sxs-lookup"><span data-stu-id="38ccf-108">When you click **View details** in the insight, a flyout appears that shows you more details for the status of each domain.</span></span>

<span data-ttu-id="38ccf-109">도메인에 대 한 녹색 확인 표시는 현재 MX 레코드 (메일 흐름 insights 대시보드를 탐색할 때)가 레코드에 포함 된 값과 일치 하 고, 지난 2 시간 동안 도메인에서 전자 메일을 받은 것을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="38ccf-109">A green check mark for a domain indicates the current MX record (when you browsed to the mail flow insights dashboard) matches the value we have on record, and that the domain has received email during the past two hours.</span></span>

<span data-ttu-id="38ccf-110">도메인에 대 한 빨간색 x는 MX 레코드가 변경 되었으며 도메인에서 지난 6 시간 동안 전자 메일을 받지 못했음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="38ccf-110">A red x for a domain indicates the MX record has been changed, and that the domain has received no email during the past 6 hours.</span></span> <span data-ttu-id="38ccf-111">이는 사용자의 도메인이 만료 되었거나 MX 레코드가 잘못 업데이트 되었음을 나타내는 것일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="38ccf-111">This likely indicates that your domain has expired, or that the MX record has been incorrectly updated.</span></span> <span data-ttu-id="38ccf-112">도메인 등록 기관 또는 DNS 호스팅 서비스에 문의 하 여 도메인의 사용 기간이 만료 되었는지 여부 또는 도메인의 MX 레코드가 올바르지 않은 지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="38ccf-112">Check with your domain registrar or DNS hosting service to see if the domain has expired, or if the domain's MX record is incorrect.</span></span>

![최상위 도메인 흐름 상태 이해의 세부 정보 플라이 아웃](media/domain-mail-flow-status-flyout.png)

## <a name="see-also"></a><span data-ttu-id="38ccf-114">참고 항목</span><span class="sxs-lookup"><span data-stu-id="38ccf-114">See also</span></span>

<span data-ttu-id="38ccf-115">메일 흐름 대시보드의 다른 메일 흐름 정보에 대 한 자세한 내용은 [Security & 준수 센터의 메일 흐름 정보](mail-flow-insights-v2.md)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="38ccf-115">For more information about other mail flow insights in the mail flow dashboard, see [Mail flow insights in the Security & Compliance Center](mail-flow-insights-v2.md).</span></span>
