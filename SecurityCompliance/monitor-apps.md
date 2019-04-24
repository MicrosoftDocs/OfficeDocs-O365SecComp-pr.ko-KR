---
title: Microsoft 365 보안에서 앱 상태 모니터링 및 보고
description: 조직에서 클라우드 앱 사용에 대 한 자세한 정보를 얻을 수 있는 방법에 대해 설명 합니다.
keywords: 보안, 맬웨어, Microsoft 365, M365, 보안 센터, 모니터, 보고서, 앱
ms.prod: w10
ms.mktglfcycl: deploy
ms.localizationpriority: medium
ms.author: ellevin
author: levinec
manager: dansimp
audience: ITPro
ms.collection: M365-security-compliance
ms.topic: article
search.appverid: met150
ms.openlocfilehash: 33a10996ceaf3023d5aee58aaabf3fef54372c30
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32263348"
---
# <a name="monitor-and-report-app-status-in-microsoft-365-security"></a><span data-ttu-id="77e6c-104">Microsoft 365 보안에서 앱 상태 모니터링 및 보고</span><span class="sxs-lookup"><span data-stu-id="77e6c-104">Monitor and report app status in Microsoft 365 security</span></span>


<span data-ttu-id="77e6c-105">이러한 보고서는 앱의 종류, 위험 수준 및 알림을 포함 하 여 조직에서 클라우드 앱을 사용 하는 방법에 대 한 자세한 정보를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="77e6c-105">These reports provide more insight into how cloud apps are being used in your organization, including what kinds of apps, their level of risk, and alerts.</span></span>

## <a name="monitor-email-accounts-at-risk"></a><span data-ttu-id="77e6c-106">위험에 대 한 전자 메일 계정 모니터링</span><span class="sxs-lookup"><span data-stu-id="77e6c-106">Monitor email accounts at risk</span></span>

<span data-ttu-id="77e6c-107">**전자 메일 보호** 는 위험의 전자 메일 계정을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="77e6c-107">**Email protection** shows email accounts at risk.</span></span> <span data-ttu-id="77e6c-108">Windows Defender 보안 센터에서 계정을 클릭 하 여 더 자세히 조사할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="77e6c-108">You can click an account to investigate further in Windows Defender Security Center.</span></span>

![전자 메일 보호 카드](./media/security-docs/email-protection.png)

## <a name="monitor-app-permissions-granted-by-users"></a><span data-ttu-id="77e6c-110">사용자가 허용한 앱 사용 권한 모니터링</span><span class="sxs-lookup"><span data-stu-id="77e6c-110">Monitor app permissions granted by users</span></span>

<span data-ttu-id="77e6c-111">**cloud app security-OAuth 앱** 은 사용자가 사용 권한을 부여 받은 Cloud app Security에서 검색 된 앱을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="77e6c-111">**Cloud App Security - OAuth apps** lists apps discovered by Cloud App Security that have been granted permissions by users.</span></span> <span data-ttu-id="77e6c-112">Cloud App Security의 위험 카탈로그에는 70 위험 요소를 사용 하 여 평가 되는 16000 개 이상의 앱이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="77e6c-112">Cloud App Security's risk catalog includes over 16,000 apps that are assessed using over 70 risk factors.</span></span>

<span data-ttu-id="77e6c-113">위험 요인은 앱 게시자와 같은 일반 정보에서 응용 프로그램이 rest 암호화에 대해 지원 되는지 여부, 사용자 작업의 감사 로그를 제공 하는지 등의 보안 조치 및 제어에서 시작 됩니다.</span><span class="sxs-lookup"><span data-stu-id="77e6c-113">The risk factors start from general information, such as the app publisher, to security measures and controls, such as whether the app supports for encryption at rest or provides an audit log of user activity.</span></span>

![Cloud App Security OAuth 앱 카드](./media/security-docs/cloud-app-security-oauth-apps.png)

## <a name="monitor-cloud-app-user-accounts"></a><span data-ttu-id="77e6c-115">cloud app 사용자 계정 모니터링</span><span class="sxs-lookup"><span data-stu-id="77e6c-115">Monitor cloud app user accounts</span></span>

<span data-ttu-id="77e6c-116">**검토를 위한 Cloud app accounts에** 는 주의가 필요한 계정이 나열 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="77e6c-116">**Cloud app accounts for review** lists accounts that may require attention.</span></span>

![검토 카드용 클라우드 앱 계정](./media/security-docs/cloud-app-accounts-for-review.png)

## <a name="understand-which-cloud-apps-are-used"></a><span data-ttu-id="77e6c-118">사용 되는 클라우드 앱 이해</span><span class="sxs-lookup"><span data-stu-id="77e6c-118">Understand which cloud apps are used</span></span>

<span data-ttu-id="77e6c-119">**검색 된 클라우드 앱 (범주)** 은 조직에서 사용 중인 앱의 종류와 cloud App Security의 클라우드 검색 대시보드에 연결 되는 링크를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="77e6c-119">**Discovered cloud apps (categories)** show what kinds of apps are being used in your organization and links to the Cloud Discovery dashboard in Cloud App Security.</span></span> <span data-ttu-id="77e6c-120">자세한 내용은 [퀵 스타트: 검색 된 앱에](https://docs.microsoft.com/cloud-app-security/discovered-apps)대 한 작업을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="77e6c-120">For more information, see [Quickstart: Work with discovered apps](https://docs.microsoft.com/cloud-app-security/discovered-apps).</span></span>  

![검색 된 클라우드 앱 범주 카드](./media/security-docs/discovered-cloud-apps-categories.png)

## <a name="monitor-where-users-access-cloud-apps"></a><span data-ttu-id="77e6c-122">사용자가 클라우드 앱에 액세스 하는 위치 모니터링</span><span class="sxs-lookup"><span data-stu-id="77e6c-122">Monitor where users access cloud apps</span></span>

<span data-ttu-id="77e6c-123">**클라우드 앱 활동 위치** 에는 사용자가 클라우드 앱에 액세스 하는 위치가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="77e6c-123">**Cloud app activity locations** show where users are accessing cloud apps.</span></span>

![Cloud App activity 위치 카드](./media/security-docs/cloud-app-activity-locations.png)

## <a name="monitor-health-for-infrastructure-workloads"></a><span data-ttu-id="77e6c-125">인프라 작업의 상태 모니터링</span><span class="sxs-lookup"><span data-stu-id="77e6c-125">Monitor health for infrastructure workloads</span></span>

<span data-ttu-id="77e6c-126">**인프라 상태** 는 Azure 보안 센터에서 인프라 작업에 대 한 상태 알림을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="77e6c-126">**Infrastructure health** shows health status alerts for infrastructure workloads in Azure Security Center.</span></span>

<span data-ttu-id="77e6c-127">Azure 보안 센터는 온-프레미스 및 클라우드 워크 로드에서 통합 된 보안 관리 및 advanced threat protection을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="77e6c-127">Azure Security Center provides unified security management and advanced threat protection across on-premises and cloud workloads.</span></span> <span data-ttu-id="77e6c-128">방화벽 및 기타 파트너 솔루션을 비롯 한 다양 한 원본의 보안 데이터를 수집, 검색 및 분석할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="77e6c-128">You can collect, search, and analyze security data from a variety of sources, including firewalls and other partner solutions.</span></span>

<span data-ttu-id="77e6c-129">자세한 내용은 [Azure 보안 센터 설명서](https://docs.microsoft.com/azure/security-center/)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="77e6c-129">For more information, see [Azure Security Center Documentation](https://docs.microsoft.com/azure/security-center/).</span></span>

![인프라 상태 카드](./media/security-docs/infrastructure-health.png)
