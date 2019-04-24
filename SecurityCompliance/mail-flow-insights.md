---
title: 보안 및 준수 센터의 메일 흐름 파악
ms.author: chrisda
author: chrisda
manager: serdars
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.assetid: beb6acaa-6016-4d54-ba7e-3d6d035e2b46
description: 관리자는 Security & 준수 센터의 메일 흐름 대시보드에 대해 알아볼 수 있습니다.
ms.openlocfilehash: 1e18bcb381a6b557d3141c0c17b8433cfcd00049
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32252394"
---
# <a name="mail-flow-insights-in-the-security--compliance-center"></a><span data-ttu-id="cd959-103">보안 및 준수 센터의 메일 흐름 파악</span><span class="sxs-lookup"><span data-stu-id="cd959-103">Mail flow insights in the Security & Compliance Center</span></span>

<span data-ttu-id="cd959-104">관리자는 Security & 준수 센터의 메일 흐름 대시보드를 사용 하 여 경향 및 통찰력을 검색 하 고, Office 365 조직의 메일 흐름과 관련 된 문제를 해결 하는 조치를 취할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cd959-104">Admins can use mail flow dashboard in the Security & Compliance Center to discover trends, insights and take actions to fix issues related to mail flow in their Office 365 organization.</span></span>

<span data-ttu-id="cd959-105">메일 흐름 대시보드에서 사용할 수 있는 다음과 같은 정보를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd959-105">The insights, reports, and widgets that are available in the mail flow dashboard are:</span></span>

- [<span data-ttu-id="cd959-106">아웃바운드 및 인바운드 메일 흐름</span><span class="sxs-lookup"><span data-stu-id="cd959-106">Outbound and inbound mail flow</span></span>](mfi-outbound-and-inbound-mail-flow.md)

- [<span data-ttu-id="cd959-107">큐 알림 및 큐</span><span class="sxs-lookup"><span data-stu-id="cd959-107">Queue alerts and Queues</span></span>](mfi-queue-alerts-and-queues.md)

- [<span data-ttu-id="cd959-108">자동 전달 메시지 보고서</span><span class="sxs-lookup"><span data-stu-id="cd959-108">Auto-forwarded messages report</span></span>](mfi-auto-forwarded-messages-report.md)

- [<span data-ttu-id="cd959-109">메일 루프 파악</span><span class="sxs-lookup"><span data-stu-id="cd959-109">Mail loop insight</span></span>](mfi-mail-loop-insight.md)

- [<span data-ttu-id="cd959-110">느린 메일 흐름 규칙 파악</span><span class="sxs-lookup"><span data-stu-id="cd959-110">Slow mail flow rules insight</span></span>](mfi-slow-mail-flow-rules-insight.md)

## <a name="permissions-required-to-view-the-mail-flow-dashboard"></a><span data-ttu-id="cd959-111">메일 흐름 대시보드를 보는 데 필요한 사용 권한</span><span class="sxs-lookup"><span data-stu-id="cd959-111">Permissions required to view the mail flow dashboard</span></span>

<span data-ttu-id="cd959-112">메일 흐름 대시보드는 다음 위치에서 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cd959-112">The mail flow dashboard is available to:</span></span>

- <span data-ttu-id="cd959-113">**Office 365 전역 관리자** 역할의 구성원</span><span class="sxs-lookup"><span data-stu-id="cd959-113">Members of the **Office 365 global administrator** role.</span></span>

- <span data-ttu-id="cd959-114">**Office 365 Exchange 관리자** 역할의 구성원</span><span class="sxs-lookup"><span data-stu-id="cd959-114">Members of **Office 365 Exchange administrator** role.</span></span>

- <span data-ttu-id="cd959-115">Security & 준수 센터에서 **메일 흐름 관리자 역할** 의 구성원</span><span class="sxs-lookup"><span data-stu-id="cd959-115">Members of the **Mail flow administrator role** in the Security & Compliance Center.</span></span> <span data-ttu-id="cd959-116">이 역할이 전역 관리자 또는 Exchange 관리자 역할의 구성원이 아닌 사용자에 게 명시적으로 할당 된 경우 다음을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd959-116">If this role is explicitly assigned to a user who isn't a member of the global administrator or Exchange administrator roles:</span></span>

  - <span data-ttu-id="cd959-117">사용자는에서 [https://protection.office.com](https://protection.office.com)직접 보안 & 준수 센터에 로그인 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd959-117">The user must log in to the Security & Compliance Center directly at [https://protection.office.com](https://protection.office.com).</span></span>

  - <span data-ttu-id="cd959-118">사용자에 게는 메일 흐름 대시보드에 대 한 읽기 전용 권한만 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cd959-118">The user will only have read-only permission to the mail flow dashboard.</span></span>

  - <span data-ttu-id="cd959-119">사용자에 게 Office 365 관리 포털에 대 한 액세스 권한이 없습니다.</span><span class="sxs-lookup"><span data-stu-id="cd959-119">The user won't have access to the Office 365 admin portal.</span></span>

<span data-ttu-id="cd959-120">office 365 전역 관리자 역할에 대 한 자세한 내용은 [office 365 관리자 역할 정보](https://support.office.com/article/da585eea-f576-4f55-a1e0-87090b6aaa9d)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="cd959-120">For more information about the Office 365 global administrator role, see [About Office 365 admin roles](https://support.office.com/article/da585eea-f576-4f55-a1e0-87090b6aaa9d).</span></span>

<span data-ttu-id="cd959-121">사용자에 게 보안 & 준수 센터 역할을 할당 하는 방법에 대 한 자세한 내용은 사용자에 게 [보안 & 준수 센터에 대 한 액세스 권한을 부여](https://support.office.com/article/2cfce2c8-20c5-47f9-afc4-24b059c1bd76)합니다.</span><span class="sxs-lookup"><span data-stu-id="cd959-121">For information on assigning Security & Compliance Center roles to users, see [Give users access to the Security & Compliance Center](https://support.office.com/article/2cfce2c8-20c5-47f9-afc4-24b059c1bd76).</span></span>

## <a name="where-to-find-the-mail-flow-dashboard"></a><span data-ttu-id="cd959-122">메일 흐름 대시보드를 찾는 위치</span><span class="sxs-lookup"><span data-stu-id="cd959-122">Where to find the mail flow dashboard</span></span>

1. <span data-ttu-id="cd959-123">의 Security & 준수 센터로 이동 [https://protection.office.com](https://protection.office.com)합니다.</span><span class="sxs-lookup"><span data-stu-id="cd959-123">Go to the Security & Compliance Center at [https://protection.office.com](https://protection.office.com).</span></span>

2. <span data-ttu-id="cd959-124">**메일 흐름** 을 확장 한 다음 **대시보드**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd959-124">Expand **Mail flow** and then select **Dashboard**.</span></span>

   ![Office 365 보안 & 준수 센터의 메일 흐름 대시보드](media/f32f5c0a-ea32-4e47-a477-d070405d4ae8.png)
