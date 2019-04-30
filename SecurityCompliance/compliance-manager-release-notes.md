---
title: Microsoft 준수 관리자 릴리스 정보
ms.author: robmazz
author: robmazz
manager: laurawi
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
description: microsoft 준수 관리자는 microsoft Service Trust Portal의 무료 워크플로 기반 위험 평가 도구입니다. 준수 관리자를 사용 하면 Microsoft 클라우드 서비스와 관련 된 규정 준수 활동을 추적, 할당 및 확인할 수 있습니다.
ms.openlocfilehash: 5e18445e3f9ad2848f18174788ec6dd40bc4a178
ms.sourcegitcommit: 696c1ed6b270be3f9da7395b49a7d8fec98e6db0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/29/2019
ms.locfileid: "33473168"
---
# <a name="release-notes-for-compliance-manager-preview"></a><span data-ttu-id="e8fd0-104">준수 관리자를 위한 릴리스 정보 (미리 보기)</span><span class="sxs-lookup"><span data-stu-id="e8fd0-104">Release Notes for Compliance Manager (Preview)</span></span>

<span data-ttu-id="e8fd0-105">준수 관리자의 공개 미리 보기는 예정 된 기능과 업데이트에 빠르게 액세스할 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8fd0-105">The public preview of Compliance Manager provides you with early access to upcoming functionality and updates.</span></span>

<span data-ttu-id="e8fd0-106">[서비스 트러스트 포털](https://servicetrust.microsoft.com) 에서 업데이트 된 [준수 관리자](https://servicetrust.microsoft.com/ComplianceManager) 도구를 사용 하 여 Microsoft 클라우드 서비스와 관련 된 규정 준수 활동을 추적, 할당 및 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e8fd0-106">You can use the updated [Compliance Manager](https://servicetrust.microsoft.com/ComplianceManager) tool on the [Service Trust Portal](https://servicetrust.microsoft.com) to track, assign, and verify regulatory compliance activities related to Microsoft cloud services.</span></span>

## <a name="whats-new-in-compliance-manager-preview"></a><span data-ttu-id="e8fd0-107">준수 관리자의 새로운 기능 (미리 보기)</span><span class="sxs-lookup"><span data-stu-id="e8fd0-107">What’s new in Compliance Manager (Preview)</span></span>

- <span data-ttu-id="e8fd0-108">**Microsoft 보안 점수와의 통합:** 준수 관리자는 고객 관리 작업을 50 이상의 보안 점수 작업에 매핑하여 [Microsoft 보안 점수](microsoft-secure-score.md) 와의 통합을 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8fd0-108">**Integration with Microsoft Secure Score:** Compliance Manager supports integration with [Microsoft Secure Score](microsoft-secure-score.md) by mapping customer-managed Actions to more than 50 Secure Score actions.</span></span> <span data-ttu-id="e8fd0-109">보안 점수에서 매핑된 작업을 완료 하면 해당 하는 준수 관리자 작업이 자동으로 업데이트 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e8fd0-109">When you complete a mapped action in Secure Score, the corresponding Compliance Manager Action is automatically updated.</span></span>

- <span data-ttu-id="e8fd0-110">**사용자 지정 평가 가져오기:** 규정 준수 관리자는 기본 제공 평가 외에, 이제 사용자 지정 템플릿 가져오기를 지원 하므로 모든 제품 또는 서비스에 대 한 사용자 지정 평가를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e8fd0-110">**Import custom Assessments:** In addition to built-in Assessments, Compliance Manager now supports importing custom Templates, enabling you to create custom Assessments for any product or service and any standard or regulation.</span></span>

- <span data-ttu-id="e8fd0-111">**작업 항목:** 작업 항목은 이제 개별 항목이 며 Microsoft 보안 점수 그래프 API의 많은 원격 분석 컬렉션을 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8fd0-111">**Actions Items:** Action Items are now individual items and many include telemetry collection from the Microsoft Secure Score Graph API.</span></span> <span data-ttu-id="e8fd0-112">가능한 경우 기술 작업 권장 사항에는 이제 Office 365 서비스의 해당 구성 페이지에 대 한 링크가 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e8fd0-112">Where possible, technical action recommendations now have links to the applicable configuration page in the Office 365 service.</span></span>

- <span data-ttu-id="e8fd0-113">**테 넌 트 관리:** 준수 관리자의 새 데이터 요소를 관리 하기 위한 새 인터페이스 (미리 보기):</span><span class="sxs-lookup"><span data-stu-id="e8fd0-113">**Tenant Management:** New interface for managing new data elements in Compliance Manager (Preview):</span></span>
    - <span data-ttu-id="e8fd0-114">**차원:** 필터의 사용자 지정 피벗을 만들 수 있는 템플릿, 평가 및 작업 항목에 대 한 메타 데이터를 보고, 추가 하 고, 사용자 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8fd0-114">**Dimensions:** View, add and customize metadata for Templates, Assessments, and Action Items that allow you to create custom pivots for filters.</span></span>
    - <span data-ttu-id="e8fd0-115">**소유자:** 각 작업 항목의 소유자를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8fd0-115">**Owners:** Specify an owner for each Action Item.</span></span>
    - <span data-ttu-id="e8fd0-116">**고객 작업:** 준수 관리자에 포함 된 작업 항목의 전체 목록 (미리 보기)을 관리 하 고 보안 점수와 통합 된 작업 항목에 대해 보안 점수 모니터링을 사용 하거나 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8fd0-116">**Customer Actions:** Manage the complete list of Actions Items included in Compliance Manager (Preview) and enable/disable Secure Score monitoring for Action Items that are integrated with Secure Score.</span></span>

- <span data-ttu-id="e8fd0-117">**업데이트 된 준수 점수**: 방법론은 Microsoft 보안 점수와의 동기화를 지원 하기 위해 변경 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e8fd0-117">**Updated Compliance Score**: The methodology has changed to support syncing with Microsoft Secure Score.</span></span> <span data-ttu-id="e8fd0-118">점수 매기기 시스템은 Microsoft에서 관리 하는 컨트롤의 제작진을 제거 하며 고객 관리 컨트롤의 완성에만 초점을 집중 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8fd0-118">The scoring system removes the Microsoft-managed control credits and focuses solely on the completion of customer-managed controls.</span></span>

## <a name="known-issues-in-compliance-manager-preview"></a><span data-ttu-id="e8fd0-119">준수 관리자의 알려진 문제 (미리 보기)</span><span class="sxs-lookup"><span data-stu-id="e8fd0-119">Known issues in Compliance Manager (Preview)</span></span>

<span data-ttu-id="e8fd0-120">다음 섹션에서는 이후의 준수 관리자 릴리스에서 해결 해야 할 알려진 문제에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8fd0-120">The following sections cover known issues to be resolved in upcoming releases of Compliance Manager.</span></span>

### <a name="compliance-score"></a><span data-ttu-id="e8fd0-121">준수 점수</span><span class="sxs-lookup"><span data-stu-id="e8fd0-121">Compliance Score</span></span>

- <span data-ttu-id="e8fd0-122">작업 항목이 **범위 내에 없는**것으로 표시 된 경우에는 작업 항목에 할당 된 점수가 준수 점수 계산에서 제외 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e8fd0-122">When Action Items are marked as **Not in Scope**, the score assigned to the Action Item is not excluded from the Compliance Score calculation.</span></span> <span data-ttu-id="e8fd0-123">**범위에 없는** 것으로 표시 된 작업 항목은 준수 점수를 높일 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="e8fd0-123">Action Items marked **Not in Scope** should not increase your Compliance Score.</span></span>

### <a name="microsoft-managed-controls"></a><span data-ttu-id="e8fd0-124">Microsoft 관리 컨트롤</span><span class="sxs-lookup"><span data-stu-id="e8fd0-124">Microsoft-managed Controls</span></span>

- <span data-ttu-id="e8fd0-125">Microsoft 관리 컨트롤에 대 한 테스트 날짜는 평가에 포함 된 경우에도 UI에 나타나지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e8fd0-125">The test date for Microsoft-managed controls is not appearing in the UI, even when included in the Assessment.</span></span> <span data-ttu-id="e8fd0-126">테스트 날짜 정보를 보려면 평가를 내보내야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8fd0-126">To see test date information, you must export the Assessment.</span></span>

### <a name="customization"></a><span data-ttu-id="e8fd0-127">사용자 지정</span><span class="sxs-lookup"><span data-stu-id="e8fd0-127">Customization</span></span>

- <span data-ttu-id="e8fd0-128">사용자 지정 컨트롤을 추가 하면 기존 컨트롤 패밀리에 새 컨트롤을 추가할 수 있지만 새 컨트롤 패밀리를 추가할 수는 없습니다.</span><span class="sxs-lookup"><span data-stu-id="e8fd0-128">Adding custom Controls enables adding a new control to an existing control family, but it does not allow you to add a new Control Family.</span></span>
- <span data-ttu-id="e8fd0-129">이 릴리스는 작업 항목을 연결 하거나 평가에 작업 항목 또는 컨트롤을 추가 하는 것을 지원 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e8fd0-129">This release does not support linking Action Items or adding Actions Items or Controls to an Assessment.</span></span>
- <span data-ttu-id="e8fd0-130">사용자 지정 동작을 만드는 경우에는 편집 하거나 삭제할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="e8fd0-130">If you create a custom Action, you cannot edit or delete it.</span></span>

### <a name="control-families-not-shown-in-assessments"></a><span data-ttu-id="e8fd0-131">평가에 표시 되지 않는 컨트롤 패밀리</span><span class="sxs-lookup"><span data-stu-id="e8fd0-131">Control Families Not Shown in Assessments</span></span>

- <span data-ttu-id="e8fd0-132">템플릿을 가져올 때 해당 서식 파일을 기반으로 하는 모든 평가에는 서식 파일에 포함 된 모든 컨트롤 패밀리가 반영 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e8fd0-132">When you import a Template, all Assessments based on that Template will reflect all Control Families that are part of the Template.</span></span> <span data-ttu-id="e8fd0-133">그러나 서식 파일에 새 컨트롤 패밀리를 추가 하는 경우 기존 평가에 변경 내용이 반영 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e8fd0-133">But if you add new Control Families to the Template, any existing Assessments will not reflect the changes.</span></span> <span data-ttu-id="e8fd0-134">업데이트 된 서식 파일에서 만든 새 평가에만 변경 내용이 반영 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e8fd0-134">Only new Assessments created off the updated Template will reflect the changes.</span></span>

### <a name="filters"></a><span data-ttu-id="e8fd0-135">필터</span><span class="sxs-lookup"><span data-stu-id="e8fd0-135">Filters</span></span>

- <span data-ttu-id="e8fd0-136">작업 항목이 나 컨트롤을 필터링 하면 정확 하 게 올바른 결과가 생성 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e8fd0-136">Filtering on Action Items or Controls does not consistently produce correct results.</span></span>

### <a name="templates"></a><span data-ttu-id="e8fd0-137">템플릿</span><span class="sxs-lookup"><span data-stu-id="e8fd0-137">Templates</span></span>

- <span data-ttu-id="e8fd0-138">보관 된 템플릿은 편집이 가능 하 고 편집이 불가능 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8fd0-138">Archived templates are editable and they should not be editable.</span></span>
- <span data-ttu-id="e8fd0-139">잠긴 템플릿을 사용 하면 평가를 수행 하지 않아야 할 때 평가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e8fd0-139">Locked templates allow for Assessment creation when they should not.</span></span> <span data-ttu-id="e8fd0-140">템플릿을 잠그면 평가를 만드는 데 사용 되는 것을 방지 하기 위한 것입니다.</span><span class="sxs-lookup"><span data-stu-id="e8fd0-140">Locking a Template is meant to prevent it from being used to create Assessments.</span></span>

### <a name="export"></a><span data-ttu-id="e8fd0-141">내보내기</span><span class="sxs-lookup"><span data-stu-id="e8fd0-141">Export</span></span>

- <span data-ttu-id="e8fd0-142">서식 파일 내보내기가 **가져오기** 또는 **보류 중인 승인**으로 설정 된 경우 JSON으로 내보내기 작업이 실패 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8fd0-142">Template export to JSON fails when the template status is set to **Imported** or **Pending Approval**.</span></span>

### <a name="supported-browsers"></a><span data-ttu-id="e8fd0-143">지원되는 브라우저</span><span class="sxs-lookup"><span data-stu-id="e8fd0-143">Supported browsers</span></span>

- <span data-ttu-id="e8fd0-144">최신 버전의 Microsoft Edge, Chrome 및 Safari가 지원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e8fd0-144">The latest versions of Microsoft Edge, Chrome, and Safari are supported.</span></span>
- <span data-ttu-id="e8fd0-145">브라우저를 새로 고칠 때까지 업데이트 된 데이터가 표시 되지 않는 경우가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e8fd0-145">There may be instances where updated data does not appear until your browser is refreshed.</span></span>
- <span data-ttu-id="e8fd0-146">Microsoft Edge의 preview 버전은 지원 되지 않지만 알려진 문제는 없습니다.</span><span class="sxs-lookup"><span data-stu-id="e8fd0-146">The preview version of Microsoft Edge is not supported but has no known issues.</span></span>
- <span data-ttu-id="e8fd0-147">Internet Explorer가 지원 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e8fd0-147">Internet Explorer is not supported.</span></span>

### <a name="session-timeout"></a><span data-ttu-id="e8fd0-148">세션 제한 시간</span><span class="sxs-lookup"><span data-stu-id="e8fd0-148">Session timeout</span></span>

- <span data-ttu-id="e8fd0-149">세션 시간이 초과 되 면 "문제가 발생 했습니다." 오류가 나타날 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e8fd0-149">When a session times out, a “Something went wrong” error may appear.</span></span> <span data-ttu-id="e8fd0-150">문제를 해결 하려면 [준수 관리자로](https://servicetrust.microsoft.com/ComplianceManager) 이동 하 여 다시 로그인 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8fd0-150">To resolve, go to [Compliance Manager](https://servicetrust.microsoft.com/ComplianceManager) and log in again.</span></span>