---
title: 파일 계획 관리자 개요
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: ''
audience: Admin
ms.topic: conceptual
ms.service: O365-seccomp
localization_priority: Priority
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: af398293-c69d-465e-a249-d74561552d30
description: 파일 계획 관리자는 보존 레이블 및 보존 레이블 정책에 대한 고급 관리 기능을 제공하고, 생성부터 공동 작업, 레코드 선언, 보존 및 최종 처리에 이르는 전체 콘텐츠 수명 주기 동안 레이블 및 레이블-콘텐츠 간 활동을 트래버스하는 통합 방법을 제공합니다.
ms.openlocfilehash: 38bfb1e6a6cde931804e518660ddf6c2b45205b0
ms.sourcegitcommit: f443de08971da2fe200a159b8efbed40effba125
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2019
ms.locfileid: "36430015"
---
# <a name="overview-of-file-plan-manager"></a><span data-ttu-id="d8df4-103">파일 계획 관리자 개요</span><span class="sxs-lookup"><span data-stu-id="d8df4-103">Overview of file plan manager</span></span>

<span data-ttu-id="d8df4-104">파일 계획 관리자는 보존 레이블 및 보존 레이블 정책에 대한 고급 관리 기능을 제공하고, 생성부터 공동 작업, 레코드 선언, 보존 및 최종 처리에 이르는 전체 콘텐츠 수명 주기 동안 레이블 및 레이블-콘텐츠 간 활동을 트래버스하는 통합 방법을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="d8df4-104">File plan manager provides advanced management capabilities for retention labels and policies, and provides an integrated way to traverse label and label-to-content activity for your entire content lifecycle – from creation, through collaboration, record declaration, retention, and finally disposition.</span></span>

![파일 계획 페이지](media/file-plan-page.png)

## <a name="accessing-file-plan-manager"></a><span data-ttu-id="d8df4-106">파일 계획 관리자 액세스</span><span class="sxs-lookup"><span data-stu-id="d8df4-106">Accessing file plan manager</span></span>

<span data-ttu-id="d8df4-107">파일 계획 관리자에 액세스하려면 다음 두 가지 요구 사항이 충족되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d8df4-107">There are two requirements to access file plan manager, they are:</span></span>
- <span data-ttu-id="d8df4-108">Office 365 Enterprise E5 구독</span><span class="sxs-lookup"><span data-stu-id="d8df4-108">An Office 365 Enterprise E5 subscription.</span></span>
- <span data-ttu-id="d8df4-109">사용자에게 보안 및 준수 센터의 다음 역할 중 하나가 할당되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d8df4-109">The user has been in assigned one of the following roles of the Security &amp; Compliance Center:</span></span>
    - <span data-ttu-id="d8df4-110">보존 관리자</span><span class="sxs-lookup"><span data-stu-id="d8df4-110">Retention Manager</span></span>
    - <span data-ttu-id="d8df4-111">보기 전용 보존 관리자</span><span class="sxs-lookup"><span data-stu-id="d8df4-111">View-only Retention Manager</span></span>

## <a name="default-retention-labels-and-label-policy"></a><span data-ttu-id="d8df4-112">기본 보존 레이블 및 레이블 정책</span><span class="sxs-lookup"><span data-stu-id="d8df4-112">Default retention labels and label policy</span></span>

<span data-ttu-id="d8df4-113">보안 및 규정 준수 센터에 보존 레이블이 없는 경우, 왼쪽 탐색에서 **파일 계획**을 처음 선택하면 **Default Data Governance Publishing Policy**라는 레이블 정책이 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="d8df4-113">If there are no retention labels in the Security & Compliance Center, the first time you choose **File plan** in the left nav, this creates a label policy called **Default Data Governance Publishing Policy**.</span></span> 

<span data-ttu-id="d8df4-114">이 레이블 정책에는 세 가지 보존 레이블이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d8df4-114">This label policy contains three retention labels:</span></span>

- <span data-ttu-id="d8df4-115">**운영 프로시저**</span><span class="sxs-lookup"><span data-stu-id="d8df4-115">**Operational procedure**</span></span>
- <span data-ttu-id="d8df4-116">**비즈니스 일반**</span><span class="sxs-lookup"><span data-stu-id="d8df4-116">**Business general**</span></span>
- <span data-ttu-id="d8df4-117">**계약**</span><span class="sxs-lookup"><span data-stu-id="d8df4-117">**Contract agreement**</span></span>

<span data-ttu-id="d8df4-118">이 보존 레이블은 콘텐츠를 삭제하지 않고 보존하도록 구성됩니다.</span><span class="sxs-lookup"><span data-stu-id="d8df4-118">These retention labels are configured only to retain content, not delete content.</span></span> <span data-ttu-id="d8df4-119">이 레이블 정책은 전체 조직에 게시되고 비활성화하거나 제거할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d8df4-119">This label policy will be published to the entire organization and can be disabled or removed.</span></span> 

<span data-ttu-id="d8df4-120">**보존 정책을 만들었습니다** 및 **보존 정책에 대한 보존 구성을 만들었습니다**와 같은 활동에 대한 감사 로그를 검토하여 파일 계획 관리자를 열고 첫 번째 실행 환경을 시작한 사용자를 판별할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d8df4-120">You can determine who opened file plan manager and kicked off the first-run experience by reviewing the audit log for the activities **Created retention policy** and **Created retention configuration for a retention policy**.</span></span>

> [!NOTE]
> <span data-ttu-id="d8df4-121">고객 피드백으로 인해, 위에 언급된 기본 보존 레이블과 보존 레이블 정책을 만드는 이 기능을 제거했습니다.</span><span class="sxs-lookup"><span data-stu-id="d8df4-121">Due to customer feedback, we have removed this feature that creates the default retention labels and label policy mentioned above.</span></span> <span data-ttu-id="d8df4-122">2019년 4월 11일 이전에 파일 계획 관리자를 연 경우에만 이러한 보존 레이블과 보존 레이블 정책을 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d8df4-122">You will only see this policy and labels if you used file plan manager before April 11, 2019.</span></span>

## <a name="navigating-your-file-plan"></a><span data-ttu-id="d8df4-123">파일 계획 탐색</span><span class="sxs-lookup"><span data-stu-id="d8df4-123">Navigating your file plan</span></span>

<span data-ttu-id="d8df4-124">파일 계획 관리자를 사용하면 하나의 보기에서 모든 보존 레이블 및 정책의 설정을 보다 쉽게 검토할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d8df4-124">File plan manager makes it easier see into and across the settings of all your retention labels and policies from one view.</span></span>

<span data-ttu-id="d8df4-125">파일 계획 외부에서 만들어진 보존 레이블도 파일 계획에서 사용할 수 있고 그 반대의 경우도 가능합니다.</span><span class="sxs-lookup"><span data-stu-id="d8df4-125">Note that retention labels created outside of the file plan will be available in the file plan and vice versa.</span></span>

<span data-ttu-id="d8df4-126">**파일 계획 레이블** 탭에서 다음과 같은 추가 정보 및 기능을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d8df4-126">On the **file plan labels** tab, the following additional information and capabilities are available:</span></span>

### <a name="label-settings-columns"></a><span data-ttu-id="d8df4-127">레이블 설정 열</span><span class="sxs-lookup"><span data-stu-id="d8df4-127">Label settings columns</span></span>

- <span data-ttu-id="d8df4-p103">**기준**은 보존 기간을 시작할 트리거 유형을 식별합니다. 유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="d8df4-p103">**Based on** identifies the type of trigger that will start the retention period. Valid values are:</span></span>
    - <span data-ttu-id="d8df4-130">이벤트</span><span class="sxs-lookup"><span data-stu-id="d8df4-130">Event</span></span>
    - <span data-ttu-id="d8df4-131">만든 날짜</span><span class="sxs-lookup"><span data-stu-id="d8df4-131">When created</span></span>
    - <span data-ttu-id="d8df4-132">마지막으로 수정한 날짜</span><span class="sxs-lookup"><span data-stu-id="d8df4-132">When last modified</span></span>
    - <span data-ttu-id="d8df4-133">레이블을 지정한 날짜</span><span class="sxs-lookup"><span data-stu-id="d8df4-133">When labeled</span></span>
- <span data-ttu-id="d8df4-p104">**레코드**는 레이블이 적용될 때 항목이 선언된 레코드가 될지를 식별합니다. 유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="d8df4-p104">**Record** identifies if the item will become a declared record when the label is applied. Valid values are:</span></span>
    - <span data-ttu-id="d8df4-136">아니요</span><span class="sxs-lookup"><span data-stu-id="d8df4-136">No</span></span>
    - <span data-ttu-id="d8df4-137">예</span><span class="sxs-lookup"><span data-stu-id="d8df4-137">Yes</span></span>
    - <span data-ttu-id="d8df4-138">예(규정)</span><span class="sxs-lookup"><span data-stu-id="d8df4-138">Yes(Regulatory)</span></span>
- <span data-ttu-id="d8df4-p105">**보존**은 보존 유형을 식별합니다. 유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="d8df4-p105">**Retention** identifies the retention type. Valid values are:</span></span>
    - <span data-ttu-id="d8df4-141">유지</span><span class="sxs-lookup"><span data-stu-id="d8df4-141">Keep</span></span>
    - <span data-ttu-id="d8df4-142">유지 및 삭제</span><span class="sxs-lookup"><span data-stu-id="d8df4-142">Keep and delete</span></span>
    - <span data-ttu-id="d8df4-143">삭제</span><span class="sxs-lookup"><span data-stu-id="d8df4-143">Delete</span></span>
- <span data-ttu-id="d8df4-p106">**처리**는 보존 기간이 끝날 때 콘텐츠에 대해 수행할 작업을 식별합니다. 유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="d8df4-p106">**Disposition** identifies what will happen to the content at the end of the retention period. Valid values are:</span></span>
    - <span data-ttu-id="d8df4-146">null</span><span class="sxs-lookup"><span data-stu-id="d8df4-146">null</span></span>
    - <span data-ttu-id="d8df4-147">작업 없음</span><span class="sxs-lookup"><span data-stu-id="d8df4-147">No action</span></span>
    - <span data-ttu-id="d8df4-148">자동 삭제</span><span class="sxs-lookup"><span data-stu-id="d8df4-148">Auto-delete</span></span>
    - <span data-ttu-id="d8df4-149">검토 필요(즉, 처리 검토)</span><span class="sxs-lookup"><span data-stu-id="d8df4-149">Review required (aka Disposition review)</span></span>

![파일 계획의 레이블 설정](media/file-plan-label-columns.png)

### <a name="retention-label-file-plan-descriptors-columns"></a><span data-ttu-id="d8df4-151">보존 레이블 파일 계획 설명자 열</span><span class="sxs-lookup"><span data-stu-id="d8df4-151">Label file plan descriptors columns</span></span>

<span data-ttu-id="d8df4-p107">이제 보존 레이블 구성에 더 많은 정보를 포함할 수 있습니다. 보존 레이블에 파일 계획 설명자를 삽입하면 파일 계획의 관리 효율성과 구성이 개선됩니다.</span><span class="sxs-lookup"><span data-stu-id="d8df4-p107">You can now include more information in the configuration of your retention labels. Inserting file plan descriptors into labels will improve the manageability and organization of your file plan.</span></span>

<span data-ttu-id="d8df4-p108">시작하기 위해 파일 계획 관리자에서는 직무/부서, 범주, 권한 유형 및 프로비저닝/인용에 대한 기본 제공 값을 제공합니다. 보존 레이블을 만들거나 편집할 때 새 파일 계획 설명자 값을 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d8df4-p108">To get you started, file plan manager provides some out-of-box values for: Function/department, Category, Authority type and Provision/citation. You can add new file plan descriptor values when creating or editing a retention label.</span></span>

<span data-ttu-id="d8df4-156">보존 레이블을 만들거나 편집할 때의 파일 계획 설명자 단계 보기는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="d8df4-156">Here's a view of the file plan descriptors step when creating or editing a retention label.</span></span>

![파일 계획 설명자](media/file-plan-descriptors.png)

<span data-ttu-id="d8df4-158">파일 계획 관리자의 레이블 탭에 표시되는 파일 계획 설명자 열 보기는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="d8df4-158">Here's a view of the file plan descriptors columns on the labels tab of file plan manager.</span></span>

![file-plan-descriptors-on-labels-tab.png](media/file-plan-descriptors-on-labels-tab.png)

## <a name="export-all-existing-retention-labels-to-analyze-andor-perform-offline-reviews"></a><span data-ttu-id="d8df4-160">모든 기존 보존 레이블을 내보내어 오프라인 검토를 분석 및/또는 수행</span><span class="sxs-lookup"><span data-stu-id="d8df4-160">Export all existing retention labels to analyze and/or perform offline reviews</span></span>

<span data-ttu-id="d8df4-161">파일 계획 관리자에서 모든 보존 레이블의 세부 정보를 .csv 파일로 내보내 조직의 데이터 거버넌스 이해 관계자와 함께 정기적인 검토를 편리하게 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d8df4-161">From file plan manager, you can export the details of all retention labels into a .csv file to assist you in facilitating periodic compliance reviews with data governance stakeholders in your organization.</span></span>

<span data-ttu-id="d8df4-162">모든 보존 레이블의 내보내려면 **파일 계획 관리자** \> **파일 계획 작업** \> **레이블 내보내기**로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="d8df4-162">To export all retention labels, go to **file plan manager** \> **file plan actions** \> **export labels**.</span></span>

![파일 계획 내보내기 옵션](media/file-plan-export-labels-option.png)

<span data-ttu-id="d8df4-164">모든 기존 보존 레이블을 포함하는 \*.csv 파일이 열립니다.</span><span class="sxs-lookup"><span data-stu-id="d8df4-164">A \*.csv file containing all existing retention labels will open.</span></span>

![모든 보존 레이블이 표시되는 CSV 파일](media/file-plan-csv-file.png)

## <a name="import-retention-labels-into-your-file-plan"></a><span data-ttu-id="d8df4-166">파일 계획에 보존 레이블 가져오기</span><span class="sxs-lookup"><span data-stu-id="d8df4-166">Import labels into your file plan</span></span>

<span data-ttu-id="d8df4-167">파일 계획 관리자에서 기존 보존 레이블을 수정할 수 있을 뿐만 아니라 새 보존 레이블을 대량으로 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d8df4-167">From file plan manager, you can bulk import new labels as well as modify existing retention labels.</span></span>

<span data-ttu-id="d8df4-168">새 보존 레이블이 가져오고 기존 보존 레이블을 업데이트하려면 **파일 계획 관리자** \> **파일 계획 작업** \> **레이블 가져오기**로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="d8df4-168">To import new retention labels and make updates existing retention labels, go to **file plan manager** \> **file plan actions** \> **import labels**.</span></span>

![파일 계획 가져오기 옵션](media/file-plan-import-labels-option.png)

![빈 파일 계획 서식 파일 다운로드 옵션](media/file-plan-blank-template-option.png)

<span data-ttu-id="d8df4-171">빈 서식 파일을 다운로드합니다(또는 현재 파일 계획의 내보내기 기능을 통해 시작).</span><span class="sxs-lookup"><span data-stu-id="d8df4-171">Download a blank template (or start from an export of your current file plan).</span></span>

![Excel에서 빈 파일 계획 서식 파일 열기](media/file-plan-blank-template.png)

<span data-ttu-id="d8df4-173">서식 파일 채우기</span><span class="sxs-lookup"><span data-stu-id="d8df4-173">Fill-out the template.</span></span> <span data-ttu-id="d8df4-174">이 표에서는 유효한 값을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="d8df4-174">This table provides valid values.</span></span>

|<span data-ttu-id="d8df4-175">**속성**</span><span class="sxs-lookup"><span data-stu-id="d8df4-175">**Property**</span></span>|<span data-ttu-id="d8df4-176">**유형**</span><span class="sxs-lookup"><span data-stu-id="d8df4-176">**Type**</span></span>|<span data-ttu-id="d8df4-177">**유효한 값**</span><span class="sxs-lookup"><span data-stu-id="d8df4-177">**Valid values**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="d8df4-178">LabelName</span><span class="sxs-lookup"><span data-stu-id="d8df4-178">LabelName</span></span>|<span data-ttu-id="d8df4-179">문자열</span><span class="sxs-lookup"><span data-stu-id="d8df4-179">String</span></span>|<span data-ttu-id="d8df4-180">값에 공백이 포함되어 있으면 값을 큰따옴표(")로 묶습니다.</span><span class="sxs-lookup"><span data-stu-id="d8df4-180">If the value contains spaces, enclose the value in quotation marks (").</span></span>|
|<span data-ttu-id="d8df4-181">설명</span><span class="sxs-lookup"><span data-stu-id="d8df4-181">Comment</span></span>|<span data-ttu-id="d8df4-182">문자열</span><span class="sxs-lookup"><span data-stu-id="d8df4-182">String</span></span>|<span data-ttu-id="d8df4-183">값에 공백이 포함되어 있으면 값을 큰따옴표(")로 묶습니다.</span><span class="sxs-lookup"><span data-stu-id="d8df4-183">If the value contains spaces, enclose the value in quotation marks (").</span></span> |
|<span data-ttu-id="d8df4-184">참고</span><span class="sxs-lookup"><span data-stu-id="d8df4-184">Notes</span></span>|<span data-ttu-id="d8df4-185">문자열</span><span class="sxs-lookup"><span data-stu-id="d8df4-185">String</span></span>|<span data-ttu-id="d8df4-186">사용자 지정</span><span class="sxs-lookup"><span data-stu-id="d8df4-186">Custom</span></span>|
|<span data-ttu-id="d8df4-187">IsRecordLabel</span><span class="sxs-lookup"><span data-stu-id="d8df4-187">IsRecordLabel</span></span>|<span data-ttu-id="d8df4-188">문자열</span><span class="sxs-lookup"><span data-stu-id="d8df4-188">String</span></span>|<span data-ttu-id="d8df4-189">$true: 레이블이 레코드 레이블입니다.</span><span class="sxs-lookup"><span data-stu-id="d8df4-189">$true: The label is a record label.</span></span></br><span data-ttu-id="d8df4-190">$false: 레이블이 레코드 레이블이 아닙니다.</span><span class="sxs-lookup"><span data-stu-id="d8df4-190">$false: The label isn't a record label.</span></span> <span data-ttu-id="d8df4-191">이 값은 기본값입니다.</span><span class="sxs-lookup"><span data-stu-id="d8df4-191">This is the default value.</span></span>|
|<span data-ttu-id="d8df4-192">RetentionAction</span><span class="sxs-lookup"><span data-stu-id="d8df4-192">RetentionAction</span></span>|<span data-ttu-id="d8df4-193">문자열</span><span class="sxs-lookup"><span data-stu-id="d8df4-193">String</span></span>|<span data-ttu-id="d8df4-194">삭제</span><span class="sxs-lookup"><span data-stu-id="d8df4-194">Delete</span></span></br><span data-ttu-id="d8df4-195">유지</span><span class="sxs-lookup"><span data-stu-id="d8df4-195">Keep</span></span></br><span data-ttu-id="d8df4-196">KeepAndDelete</span><span class="sxs-lookup"><span data-stu-id="d8df4-196">KeepAndDelete</span></span> |
|<span data-ttu-id="d8df4-197">RetentionDuration</span><span class="sxs-lookup"><span data-stu-id="d8df4-197">RetentionDuration</span></span>|<span data-ttu-id="d8df4-198">문자열</span><span class="sxs-lookup"><span data-stu-id="d8df4-198">String</span></span>|<span data-ttu-id="d8df4-199">이 속성은 콘텐츠를 보관할 일 수를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="d8df4-199">The RetentionDuration parameter specifies the number of days to retain the content.</span></span> <span data-ttu-id="d8df4-200">사용할 수 있는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="d8df4-200">Valid values are:</span></span></br><span data-ttu-id="d8df4-201">양의 정수</span><span class="sxs-lookup"><span data-stu-id="d8df4-201">A positive integer.</span></span></br><span data-ttu-id="d8df4-202">값은 제한이 없습니다.</span><span class="sxs-lookup"><span data-stu-id="d8df4-202">The default value is unlimited.</span></span>|
|<span data-ttu-id="d8df4-203">RetentionType</span><span class="sxs-lookup"><span data-stu-id="d8df4-203">RetentionType</span></span>|<span data-ttu-id="d8df4-204">문자열</span><span class="sxs-lookup"><span data-stu-id="d8df4-204">String</span></span>|<span data-ttu-id="d8df4-205">이 속성은 콘텐츠 작성 날짜, 레이블이(태그가) 지정된 날짜 또는 마지막으로 수정한 날짜에서 보존 기간을 계산하는지 여부를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="d8df4-205">This property specifies whether the retention duration is calculated from the content creation date, labeled (tagged) date, or last modified date.</span></span> <span data-ttu-id="d8df4-206">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="d8df4-206">Valid values are:</span></span></br><span data-ttu-id="d8df4-207">CreationAgeInDays</span><span class="sxs-lookup"><span data-stu-id="d8df4-207">CreationAgeInDays</span></span></br><span data-ttu-id="d8df4-208">EventAgeInDays</span><span class="sxs-lookup"><span data-stu-id="d8df4-208">EventAgeInDays</span></span></br><span data-ttu-id="d8df4-209">ModificationAgeInDays</span><span class="sxs-lookup"><span data-stu-id="d8df4-209">ModificationAgeInDays</span></span></br><span data-ttu-id="d8df4-210">TaggedAgeInDays</span><span class="sxs-lookup"><span data-stu-id="d8df4-210">TaggedAgeInDays</span></span> |
|<span data-ttu-id="d8df4-211">ReviewerEmail</span><span class="sxs-lookup"><span data-stu-id="d8df4-211">ReviewerEmail</span></span>|<span data-ttu-id="d8df4-212">SmtpAddress[]</span><span class="sxs-lookup"><span data-stu-id="d8df4-212">PARAMVALUE: SmtpAddress[]</span></span>|<span data-ttu-id="d8df4-213">이 속성은 삭제와 KeepAndDelete 보존 작업에 대한 검토자의 전자 메일 주소를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="d8df4-213">This property specifies the email address of a reviewer for Delete and KeepAndDelete retention actions.</span></span> <span data-ttu-id="d8df4-214">전자 메일 주소가 여러 개인 경우 각 주소를 쉼표로 구분하여 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d8df4-214">You can specify multiple email addresses separated by commas.</span></span>|
|<span data-ttu-id="d8df4-215">ReferenceId</span><span class="sxs-lookup"><span data-stu-id="d8df4-215">ReferenceId</span></span>|<span data-ttu-id="d8df4-216">문자열</span><span class="sxs-lookup"><span data-stu-id="d8df4-216">String</span></span>|<span data-ttu-id="d8df4-217">사용자 지정</span><span class="sxs-lookup"><span data-stu-id="d8df4-217">Custom</span></span>|
|<span data-ttu-id="d8df4-218">Departmentname</span><span class="sxs-lookup"><span data-stu-id="d8df4-218">DepartmentName</span></span>|<span data-ttu-id="d8df4-219">문자열</span><span class="sxs-lookup"><span data-stu-id="d8df4-219">String</span></span>|<span data-ttu-id="d8df4-220">사용자 지정</span><span class="sxs-lookup"><span data-stu-id="d8df4-220">Custom</span></span>|
|<span data-ttu-id="d8df4-221">범주</span><span class="sxs-lookup"><span data-stu-id="d8df4-221">Category</span></span>|<span data-ttu-id="d8df4-222">문자열</span><span class="sxs-lookup"><span data-stu-id="d8df4-222">String</span></span>|<span data-ttu-id="d8df4-223">사용자 지정</span><span class="sxs-lookup"><span data-stu-id="d8df4-223">Custom</span></span>|
|<span data-ttu-id="d8df4-224">하위 범주</span><span class="sxs-lookup"><span data-stu-id="d8df4-224">SubCategory</span></span>|<span data-ttu-id="d8df4-225">문자열</span><span class="sxs-lookup"><span data-stu-id="d8df4-225">String</span></span>|<span data-ttu-id="d8df4-226">사용자 지정</span><span class="sxs-lookup"><span data-stu-id="d8df4-226">Custom</span></span>|
|<span data-ttu-id="d8df4-227">AuthorityType</span><span class="sxs-lookup"><span data-stu-id="d8df4-227">AuthorityType</span></span>|<span data-ttu-id="d8df4-228">문자열</span><span class="sxs-lookup"><span data-stu-id="d8df4-228">String</span></span>|<span data-ttu-id="d8df4-229">사용자 지정</span><span class="sxs-lookup"><span data-stu-id="d8df4-229">Custom</span></span>|
|<span data-ttu-id="d8df4-230">CitationName</span><span class="sxs-lookup"><span data-stu-id="d8df4-230">CitationName</span></span>|<span data-ttu-id="d8df4-231">문자열</span><span class="sxs-lookup"><span data-stu-id="d8df4-231">String</span></span>|<span data-ttu-id="d8df4-232">사용자 지정</span><span class="sxs-lookup"><span data-stu-id="d8df4-232">Custom</span></span>|
|<span data-ttu-id="d8df4-233">CitationUrl</span><span class="sxs-lookup"><span data-stu-id="d8df4-233">CitationUrl</span></span>|<span data-ttu-id="d8df4-234">문자열</span><span class="sxs-lookup"><span data-stu-id="d8df4-234">String</span></span>|<span data-ttu-id="d8df4-235">사용자 지정</span><span class="sxs-lookup"><span data-stu-id="d8df4-235">Custom</span></span>|
|<span data-ttu-id="d8df4-236">CitationJurisdiction</span><span class="sxs-lookup"><span data-stu-id="d8df4-236">CitationJurisdiction</span></span>|<span data-ttu-id="d8df4-237">문자열</span><span class="sxs-lookup"><span data-stu-id="d8df4-237">String</span></span>|<span data-ttu-id="d8df4-238">사용자 지정</span><span class="sxs-lookup"><span data-stu-id="d8df4-238">Custom</span></span>|
|<span data-ttu-id="d8df4-239">규정</span><span class="sxs-lookup"><span data-stu-id="d8df4-239">Regulatory</span></span>|<span data-ttu-id="d8df4-240">문자열</span><span class="sxs-lookup"><span data-stu-id="d8df4-240">String</span></span>|<span data-ttu-id="d8df4-241">사용자 지정</span><span class="sxs-lookup"><span data-stu-id="d8df4-241">Custom</span></span>|
|<span data-ttu-id="d8df4-242">EventType</span><span class="sxs-lookup"><span data-stu-id="d8df4-242">EventType</span></span>|<span data-ttu-id="d8df4-243">문자열</span><span class="sxs-lookup"><span data-stu-id="d8df4-243">String</span></span>|<span data-ttu-id="d8df4-244">이 속성은 레이블과 연결된 보존 규칙을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="d8df4-244">This property specifies the retention rule that's associated with the label.</span></span> <span data-ttu-id="d8df4-245">규칙을 고유하게 식별하는 모든 값을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d8df4-245">You can use any value that uniquely identifies the rule.</span></span> <span data-ttu-id="d8df4-246">예:</span><span class="sxs-lookup"><span data-stu-id="d8df4-246">For example:</span></span></br><span data-ttu-id="d8df4-247">이름</span><span class="sxs-lookup"><span data-stu-id="d8df4-247">Name</span></span></br><span data-ttu-id="d8df4-248">DN(고유 이름)</span><span class="sxs-lookup"><span data-stu-id="d8df4-248">Distinguished name (DN)</span></span></br><span data-ttu-id="d8df4-249">GUID</span><span class="sxs-lookup"><span data-stu-id="d8df4-249">GUID</span></span> </br><span data-ttu-id="d8df4-250">[Get-RetentionComplianceRule](https://docs.microsoft.com/ko-KR/powershell/module/exchange/policy-and-compliance-retention/get-retentioncompliancerule?view=exchange-ps) cmdlet를 사용하여 사용 가능한 보존 규칙을 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d8df4-250">You can use the [Get-DataEncryptionPolicy](https://docs.microsoft.com/en-us/powershell/module/exchange/policy-and-compliance-retention/get-retentioncompliancerule?view=exchange-ps) cmdlet to view the available policies.</span></span>|

![정보가 채워진 파일 계획 서식 파일](media/file-plan-filled-out-template.png)

<span data-ttu-id="d8df4-252">채운 서식 파일을 업로드하면 파일 계획 관리자에서 항목의 유효성을 검사하고 가져오기 통계를 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="d8df4-252">Upload the filled-out template, and file plan manager will validate the entries and display import statistics.</span></span>

![파일 계획 가져오기 통계](media/file-plan-import-statistics.png)

<span data-ttu-id="d8df4-254">유효성 검사 오류가 발생하면 파일 계획 가져오기가 가져오기 파일로 돌아가서 해당 오류를 손쉽게 수정할 수 있도록 계속해서 가져오기 파일의 모든 항목에 대한 유효성 검사를 수행하고 가져오기 파일의 줄/행 번호를 참조하는 모든 오류를 표시하며, 표시된 오류 결과를 복사합니다.</span><span class="sxs-lookup"><span data-stu-id="d8df4-254">In the event there is a validation error, file plan import will continue to validate every entry in the import file and display all errors referencing line/row numbers in the import file, copy the displayed error results so that you can easilly return to the import file and correct the errors.</span></span> 

<span data-ttu-id="d8df4-255">가져오기가 완료되면 파일 계획 관리자로 돌아가서 새 보존 레이블을 새 보존 레이블 및 기존 보존 레이블 정책과 연결합니다.</span><span class="sxs-lookup"><span data-stu-id="d8df4-255">When the import is complete, return to file plan manager to assign new labels to new or existing policies.</span></span>

![레이블 게시 옵션](media/file-plan-publish-labels-option.png)

