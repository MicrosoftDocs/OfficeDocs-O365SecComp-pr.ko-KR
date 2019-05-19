---
title: 보안 및 준수 센터의 메일 흐름 파악
ms.author: chrisda
author: chrisda
manager: serdars
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.assetid: beb6acaa-6016-4d54-ba7e-3d6d035e2b46
description: 관리자는 Security & 준수 센터의 메일 흐름 대시보드에 대해 알아볼 수 있습니다.
ms.openlocfilehash: c7c1a6a16c908f42098500c1015b3c3994175818
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/17/2019
ms.locfileid: "34155880"
---
# <a name="mail-flow-insights-in-the-security--compliance-center"></a><span data-ttu-id="c8369-103">보안 및 준수 센터의 메일 흐름 파악</span><span class="sxs-lookup"><span data-stu-id="c8369-103">Mail flow insights in the Security & Compliance Center</span></span>

<span data-ttu-id="c8369-104">관리자는 Security & 준수 센터의 메일 흐름 대시보드를 사용 하 여 경향 및 통찰력을 검색 하 고, Office 365 조직의 메일 흐름과 관련 된 문제를 해결 하는 조치를 취할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c8369-104">Admins can use mail flow dashboard in the Security & Compliance Center to discover trends, insights and take actions to fix issues related to mail flow in their Office 365 organization.</span></span>

<span data-ttu-id="c8369-105">메일 흐름 대시보드에서 사용할 수 있는 다음과 같은 정보를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="c8369-105">The insights, reports, and widgets that are available in the mail flow dashboard are:</span></span>

- [<span data-ttu-id="c8369-106">메일 흐름 맵 보고서</span><span class="sxs-lookup"><span data-stu-id="c8369-106">Mail flow map report</span></span>](mfi-mail-flow-map-report.md)

- [<span data-ttu-id="c8369-107">도메인 메일 흐름 상태 파악</span><span class="sxs-lookup"><span data-stu-id="c8369-107">Domain mail flow status insight</span></span>](mfi-domain-mail-flow-status-insight.md)

- [<span data-ttu-id="c8369-108">SMTP 인증 클라이언트 보고서</span><span class="sxs-lookup"><span data-stu-id="c8369-108">SMTP Auth clients report</span></span>](mfi-smtp-auth-clients-report.md)

- [<span data-ttu-id="c8369-109">보낸 사람 도메인 통찰력</span><span class="sxs-lookup"><span data-stu-id="c8369-109">Sender domain insight</span></span>](mfi-sender-domain-insight.md)

- [<span data-ttu-id="c8369-110">미실행 보고서</span><span class="sxs-lookup"><span data-stu-id="c8369-110">Non-delivery report</span></span>](mfi-non-delivery-report.md)

- [<span data-ttu-id="c8369-111">비허용 도메인 보고서</span><span class="sxs-lookup"><span data-stu-id="c8369-111">Non-accepted domain report</span></span>](mfi-non-accepted-domain-report.md)

- [<span data-ttu-id="c8369-112">아웃바운드 및 인바운드 메일 흐름</span><span class="sxs-lookup"><span data-stu-id="c8369-112">Outbound and inbound mail flow</span></span>](mfi-outbound-and-inbound-mail-flow.md)

- [<span data-ttu-id="c8369-113">큐 알림 및 큐</span><span class="sxs-lookup"><span data-stu-id="c8369-113">Queue alerts and Queues</span></span>](mfi-queue-alerts-and-queues.md)

- [<span data-ttu-id="c8369-114">자동 전달 메시지 보고서</span><span class="sxs-lookup"><span data-stu-id="c8369-114">Auto-forwarded messages report</span></span>](mfi-auto-forwarded-messages-report.md)

- [<span data-ttu-id="c8369-115">메일 루프 파악</span><span class="sxs-lookup"><span data-stu-id="c8369-115">Mail loop insight</span></span>](mfi-mail-loop-insight.md)

- [<span data-ttu-id="c8369-116">느린 메일 흐름 규칙 파악</span><span class="sxs-lookup"><span data-stu-id="c8369-116">Slow mail flow rules insight</span></span>](mfi-slow-mail-flow-rules-insight.md)

## <a name="permissions-required-to-view-the-mail-flow-dashboard"></a><span data-ttu-id="c8369-117">메일 흐름 대시보드를 보는 데 필요한 사용 권한</span><span class="sxs-lookup"><span data-stu-id="c8369-117">Permissions required to view the mail flow dashboard</span></span>

<span data-ttu-id="c8369-118">메일 흐름 대시보드는 다음 위치에서 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c8369-118">The mail flow dashboard is available to:</span></span>

- <span data-ttu-id="c8369-119">**Office 365 전역 관리자** 역할의 구성원</span><span class="sxs-lookup"><span data-stu-id="c8369-119">Members of the **Office 365 global administrator** role.</span></span>

- <span data-ttu-id="c8369-120">**Office 365 Exchange 관리자** 역할의 구성원</span><span class="sxs-lookup"><span data-stu-id="c8369-120">Members of **Office 365 Exchange administrator** role.</span></span>

- <span data-ttu-id="c8369-121">Security & 준수 센터에서 **메일 흐름 관리자 역할** 의 구성원</span><span class="sxs-lookup"><span data-stu-id="c8369-121">Members of the **Mail flow administrator role** in the Security & Compliance Center.</span></span> <span data-ttu-id="c8369-122">이 역할이 전역 관리자 또는 Exchange 관리자 역할의 구성원이 아닌 사용자에 게 명시적으로 할당 된 경우 다음을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="c8369-122">If this role is explicitly assigned to a user who isn't a member of the global administrator or Exchange administrator roles:</span></span>

  - <span data-ttu-id="c8369-123">사용자는에서 [https://protection.office.com](https://protection.office.com)직접 보안 _AMP_ 준수 센터에 로그인 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c8369-123">The user must log in to the Security & Compliance Center directly at [https://protection.office.com](https://protection.office.com).</span></span>

  - <span data-ttu-id="c8369-124">사용자에 게는 메일 흐름 대시보드에 대 한 읽기 전용 권한만 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c8369-124">The user will only have read-only permission to the mail flow dashboard.</span></span>

  - <span data-ttu-id="c8369-125">사용자에 게 Office 365 관리 포털에 대 한 액세스 권한이 없습니다.</span><span class="sxs-lookup"><span data-stu-id="c8369-125">The user won't have access to the Office 365 admin portal.</span></span>

<span data-ttu-id="c8369-126">Office 365 전역 관리자 역할에 대 한 자세한 내용은 [office 365 관리자 역할 정보](https://docs.microsoft.com/office365/admin/add-users/about-admin-roles)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="c8369-126">For more information about the Office 365 global administrator role, see [About Office 365 admin roles](https://docs.microsoft.com/office365/admin/add-users/about-admin-roles).</span></span>

<span data-ttu-id="c8369-127">사용자에 게 보안 & 준수 센터 역할을 할당 하는 방법에 대 한 자세한 내용은 사용자에 게 [보안 _AMP_ 준수 센터에 대 한 액세스 권한을 부여](https://docs.microsoft.com/office365/securitycompliance/grant-access-to-the-security-and-compliance-center)합니다.</span><span class="sxs-lookup"><span data-stu-id="c8369-127">For information on assigning Security & Compliance Center roles to users, see [Give users access to the Security & Compliance Center](https://docs.microsoft.com/office365/securitycompliance/grant-access-to-the-security-and-compliance-center).</span></span>

## <a name="where-to-find-the-mail-flow-dashboard"></a><span data-ttu-id="c8369-128">메일 흐름 대시보드를 찾는 위치</span><span class="sxs-lookup"><span data-stu-id="c8369-128">Where to find the mail flow dashboard</span></span>

1. <span data-ttu-id="c8369-129">의 Security & 준수 센터로 이동 [https://protection.office.com](https://protection.office.com)합니다.</span><span class="sxs-lookup"><span data-stu-id="c8369-129">Go to the Security & Compliance Center at [https://protection.office.com](https://protection.office.com).</span></span>

2. <span data-ttu-id="c8369-130">**메일 흐름** 을 확장 한 다음 **대시보드**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="c8369-130">Expand **Mail flow** and then select **Dashboard**.</span></span>

   ![Office 365 보안 & 준수 센터의 메일 흐름 대시보드](media/mail-flow-dashboard-v2.png)
