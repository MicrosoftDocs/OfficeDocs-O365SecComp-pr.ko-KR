---
title: 레이블 분석을 통한 레이블 사용량 보기
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Priority
ms.collection:
- M365-security-compliance
search.appverid:
- MOE150
- MET150
description: 보존 레이블 및 민감도 레이블을 만든 이후 테넌트 전체에서 얼마나 사용되는지 알고자 할 것입니다. Microsoft 365 규정 준수 센터 및 Microsoft 365 보안 센터의 레이블 분석을 사용하여 어떤 레이블이 사장 많이 사용되고 레이블이 적용된 위치를 빠르게 알 수 있습니다.
ms.openlocfilehash: d0289eb79dca04262ef61d58a8e622ae6d7cbe93
ms.sourcegitcommit: 54d58da1777eb83adb82826d1bb1adb94903c8e1
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/29/2019
ms.locfileid: "30994884"
---
# <a name="view-label-usage-with-label-analytics"></a><span data-ttu-id="68619-104">레이블 분석을 통한 레이블 사용량 보기</span><span class="sxs-lookup"><span data-stu-id="68619-104">View label usage with label analytics</span></span>

<span data-ttu-id="68619-105">보존 레이블 및 민감도 레이블을 만든 이후 테넌트 전체에서 얼마나 사용되는지 알고자 할 것입니다.</span><span class="sxs-lookup"><span data-stu-id="68619-105">After you create your retention labels and sensitivity labels, you’ll want to see how they’re being used across your tenant.</span></span> <span data-ttu-id="68619-106">Microsoft 365 규정 준수 센터 및 Microsoft 365 보안 센터의 레이블 분석을 사용하여 어떤 레이블이 사장 많이 사용되고 레이블이 적용된 위치를 빠르게 알 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="68619-106">With label analytics in the Microsoft 365 compliance center and Microsoft 365 security center, you can quickly see which labels are used the most and where they’re being applied.</span></span>

<span data-ttu-id="68619-107">예를 들어 레이블 분석을 사용하여 다음을 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="68619-107">For example, with label analytics, you can view the:</span></span>

- <span data-ttu-id="68619-108">콘텐츠에 적용된 보존 레이블 및 민감도 레이블의 총 수.</span><span class="sxs-lookup"><span data-stu-id="68619-108">Total number of retention labels and sensitivity labels applied to content.</span></span>
- <span data-ttu-id="68619-109">상단 레이블 및 각 레벨이 적용된 횟수.</span><span class="sxs-lookup"><span data-stu-id="68619-109">Top labels and the count of how many times each label was applied.</span></span>
- <span data-ttu-id="68619-110">레이블이 적용된 위치와 각 위치의 수.</span><span class="sxs-lookup"><span data-stu-id="68619-110">Locations where labels are applied and the count for each location.</span></span>
- <span data-ttu-id="68619-111">보존 레이블이 변경 또는 제거된 파일 및 폴더의 수.</span><span class="sxs-lookup"><span data-stu-id="68619-111">Count for how many files and folders had their retention label changed or removed.</span></span>

<span data-ttu-id="68619-112">[Microsoft 365 규정 준수 센터](https://compliance.microsoft.com/labelanalytics) 또는 [Microsoft 365 보안 센터](https://security.microsoft.com/labelanalytics) > **분류** > **레이블 분석**에서 레이블 분석을 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="68619-112">You can find label analytics in the [Microsoft 365 compliance center](https://compliance.microsoft.com/labelanalytics) or [Microsoft 365 security center](https://security.microsoft.com/labelanalytics) > **Classification** > **Label analytics**.</span></span>

![레이블 분석 페이지](media/label-analytics-page.png)

## <a name="sensitivity-label-usage"></a><span data-ttu-id="68619-114">민감도 레이블 사용량</span><span class="sxs-lookup"><span data-stu-id="68619-114">Sensitivity label usage</span></span>

<span data-ttu-id="68619-115">민감도 레이블 사용량에 대한 데이터는 Azure Information Protection 보고서에서 가져옵니다. 자세한 내용은 [Azure Information Protection에 대한 중앙 보고](https://docs.microsoft.com/ko-KR/azure/information-protection/reports-aip)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="68619-115">The data on sensitivity label usage is pulled from the reports for Azure Information Protection – for more information, see [Central reporting for Azure Information Protection](https://docs.microsoft.com/ko-KR/azure/information-protection/reports-aip).</span></span>

<span data-ttu-id="68619-116">Azure Information Protection 보고서에는 Microsoft 365 규정 준수 센터 및 Microsofot 365 보안 센터의 민감도 레이블에 레이블 분석을 적용하는 [필수 조건](https://docs.microsoft.com/ko-KR/azure/information-protection/reports-aip#prerequisites-for-azure-information-protection-analytics)이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="68619-116">Note that the Azure Information Protection reports have [prerequisites](https://docs.microsoft.com/ko-KR/azure/information-protection/reports-aip#prerequisites-for-azure-information-protection-analytics) that also apply to label analytics on sensitivity labels in the Microsoft 365 compliance center and Microsoft 365 security center.</span></span> <span data-ttu-id="68619-117">예를 들어 Log Analytics를 포함한 Azure 구독이 필요한데, 이러한 보고서가 Azure Information Protection 클라이언트 및 스캐너에서 Azure Log Analytics 서비스를 기준으로 중앙화된 위치로 정보 보호 감사 이벤트를 전송한 결과이기 때문입니다.</span><span class="sxs-lookup"><span data-stu-id="68619-117">For example, you need an Azure subscription that includes the Log Analytics because these reports are a result of sending information protection audit events from Azure Information Protection clients and scanners to a centralized location based on Azure Log Analytics service.</span></span>

<span data-ttu-id="68619-118">민감도 레이블 사용량:</span><span class="sxs-lookup"><span data-stu-id="68619-118">For sensitivity label usage:</span></span>

- <span data-ttu-id="68619-119">데이터에 대기 시간이 없습니다.</span><span class="sxs-lookup"><span data-stu-id="68619-119">There is no latency in the data.</span></span> <span data-ttu-id="68619-120">실시간 보고서입니다.</span><span class="sxs-lookup"><span data-stu-id="68619-120">This is a real-time report.</span></span>
- <span data-ttu-id="68619-121">각 상단 레이블의 수를 보려면 막대 그래프를 가리킨 다음 표시되는 도구 설명을 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="68619-121">To see the count for each top label, point to the bar graph and read the tool tip that appears.</span></span>
- <span data-ttu-id="68619-122">보고서는 앱별로 민감도 레이블이 적용된 위치를 보여줍니다(보존 레이블은 위치별로 표시됨).</span><span class="sxs-lookup"><span data-stu-id="68619-122">The report shows where sensitivity labels are applied per app (whereas retention labels are shown per location).</span></span>

![민감도 레이블 사용량 보고서](media/sensitivity-label-usage-report.png)

## <a name="retention-label-usage"></a><span data-ttu-id="68619-124">보존 레이블 사용량</span><span class="sxs-lookup"><span data-stu-id="68619-124">Retention label usage</span></span>

<span data-ttu-id="68619-125">이 보고서는 상단 레이블과 적용된 위치를 간단하게 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="68619-125">This report shows a quick view of what the top labels are and where they’re applied.</span></span> <span data-ttu-id="68619-126">SharePoint 및 OneDrive에서 콘텐츠에 레이블이 지정되는 방법에 대한 자세한 내용은 [문서에 대한 레이블 지정 활동 보기](view-label-activity-for-documents.md)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="68619-126">For more detailed information on how content in SharePoint and OneDrive is labeled, see [View label activity for documents](view-label-activity-for-documents.md).</span></span>

<span data-ttu-id="68619-127">보존 레이블 사용량:</span><span class="sxs-lookup"><span data-stu-id="68619-127">For retention label usage:</span></span>

- <span data-ttu-id="68619-128">데이터는 주 단위로 집계되므로 데이터가 보고서에 표시되려면 최대 7일이 소요될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="68619-128">Data is aggregated weekly, so it may take up to seven days for data to appear in the report.</span></span>
- <span data-ttu-id="68619-129">각 상단 레이블의 수를 보려면 막대 그래프를 가리킨 다음 표시되는 도구 설명을 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="68619-129">To see the count for each top label, point to the bar graph and read the tool tip that appears.</span></span>
- <span data-ttu-id="68619-130">보고서는 위치별로 보존 레이블이 적용된 위치를 보여줍니다(민감도 레이블은 앱별로 표시됨).</span><span class="sxs-lookup"><span data-stu-id="68619-130">The report shows where retention labels are applied per location (whereas sensitivity labels are shown per app).</span></span>
- <span data-ttu-id="68619-131">보존 레이블의 경우 특정 날짜 범위로 필터링되지 않은 테넌트의 전체 시간 데이터 요약입니다.</span><span class="sxs-lookup"><span data-stu-id="68619-131">For retention labels, this is a summary of the all-time data in your tenant; it’s not filtered to a specific date range.</span></span> <span data-ttu-id="68619-132">반대로 [레이블 활동 탐색기](view-label-activity-for-documents.md)는 지난 30일 동안만의 데이터를 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="68619-132">By contrast, the [Label Activity Explorer](view-label-activity-for-documents.md) shows data from only the past 30 days.</span></span>

![보존 레이블 사용량 보고서](media/retention-label-usage-report.png)

## <a name="view-all-content-with-a-specific-retention-label"></a><span data-ttu-id="68619-134">특정 보존 레이블이 포함된 모든 콘텐츠를 봅니다.</span><span class="sxs-lookup"><span data-stu-id="68619-134">View all content with a specific retention label</span></span>

<span data-ttu-id="68619-135">보존 레이블 사용량 보고서에서 해당 레이블이 적용된 모든 콘텐츠를 탐색할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="68619-135">From the retention label usage report, you can quickly explore all content with that label applied.</span></span> <span data-ttu-id="68619-136">(현재 이 기능을 개선하는 중이며 레이블 지정된 모든 콘텐츠를 보는 단계가 감소할 것입니다.)</span><span class="sxs-lookup"><span data-stu-id="68619-136">(Note that we're currently working on this feature, so that it will take fewer steps to view all the labeled content.)</span></span>

<span data-ttu-id="68619-137">먼저 보고서 하단에서 **자세히 보기**를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="68619-137">First, choose **View Details** at the bottom of the report.</span></span>

![보존 레이블 사용량 보고서 하단의 자세히 보기 옵션](media/retention-label-usage-view-details.png)

<span data-ttu-id="68619-139">그런 다음 오른쪽 창에 있는 보존 레이블 > **항목 탐색**을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="68619-139">Then choose a retention label > **Explore items** in the right pane.</span></span>

![오른쪽 창에 있는 항목 탐색 옵션](media/retention-label-usage-explore-items.png)

<span data-ttu-id="68619-141">해당 레이블에 대해 **활동** 탭을 선택하고 위치별로 레이블이 포함된 항목 수를 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="68619-141">For that label, you can choose the **Activity** tab to view a count of items with that label by location.</span></span>

![보존 레이블에 대한 활동 탭](media/retention-label-usage-activity-tab.png)

<span data-ttu-id="68619-143">**이 레이블이 포함된 항목** 탭을 선택할 수도 있습니다. 그런 다음 특정 위치를 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="68619-143">You can also choose the **Items with this label** tab. Then you can drill into specific locations:</span></span>

- <span data-ttu-id="68619-144">Exchange Online의 경우 각 사서함에서 레이블 지정된 항목 수를 포함하여 사서함의 목록이 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="68619-144">For Exchange Online, you see a list of mailboxes with the count of labeled items in each mailbox.</span></span>
- <span data-ttu-id="68619-145">SharePoint Online 및 비즈니스용 OneDrive의 경우 사이트 모음 및 OneDrive 계정 목록과 각 위치에 레이블 지정된 항목의 수가 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="68619-145">For SharePoint Online and OneDrive for Business, you see a list of site collections and OneDrive accounts with the count of labeled items in each location.</span></span>

<span data-ttu-id="68619-146">사서함 또는 사이트 모음을 선택하면 해당 위치의 해당 보존 레이블이 포함된 항목의 목록을 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="68619-146">When you choose a mailbox or site collection, you can view a list of items with that retention label in that location.</span></span>

![이 레이블이 포함된 항목 탭에서 해당 보존 레이블이 포함된 모든 항목을 표시](media/retention-label-usage-content-explorer.png)

## <a name="permissions"></a><span data-ttu-id="68619-148">사용 권한</span><span class="sxs-lookup"><span data-stu-id="68619-148">Permissions</span></span>

<span data-ttu-id="68619-149">레이블 분석을 보려면 Azure Active Directory에서 다음 역할 중 하나가 할당되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="68619-149">To view label analytics, you must be assigned one of the following roles in Azure Active Directory:</span></span>

- <span data-ttu-id="68619-150">전역 관리자</span><span class="sxs-lookup"><span data-stu-id="68619-150">Global administrator</span></span>
- <span data-ttu-id="68619-151">준수 관리자</span><span class="sxs-lookup"><span data-stu-id="68619-151">Compliance administrator</span></span>
- <span data-ttu-id="68619-152">보안 관리자</span><span class="sxs-lookup"><span data-stu-id="68619-152">Security administrator</span></span>
- <span data-ttu-id="68619-153">보안 읽기 권한자</span><span class="sxs-lookup"><span data-stu-id="68619-153">Security reader</span></span>

<span data-ttu-id="68619-154">또한 이러한 보고서는 Azure Monitor를 사용하여 조직이 소유한 Log Analytics 작업 영역에 있는 데이터를 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="68619-154">In addition, note these reports use Azure Monitor to store the data in a Log Analytics workspace that your organization owns.</span></span> <span data-ttu-id="68619-155">따라서 사용자가 데이터를 보유한 Azure Monitor 작업 영역에 읽기 권한자로 추가되어야 합니다. 자세한 내용은 [Azure Information Protection 분석에 대해 필요한 권한](https://docs.microsoft.com/ko-KR/azure/information-protection/reports-aip#permissions-required-for-azure-information-protection-analytics)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="68619-155">Therefore, the user should be added as a reader to the Azure Monitoring worksapce that holds the data - for more information, see [Permissions required for Azure Information Protection analytics](https://docs.microsoft.com/ko-KR/azure/information-protection/reports-aip#permissions-required-for-azure-information-protection-analytics).</span></span>

