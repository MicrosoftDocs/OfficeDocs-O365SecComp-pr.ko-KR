---
title: 파일 계획 관리자 개요
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 9/25/2018
ms.audience: Admin
ms.topic: overview
ms.service: O365-seccomp
localization_priority: Priority
ms.collection: Strat_O365_IP
search.appverid:
- MOE150
- MET150
ms.assetid: af398293-c69d-465e-a249-d74561552d30
description: 파일 계획 관리자는 보존 레이블 및 정책에 대한 고급 관리 기능을 제공하고, 생성부터 공동 작업, 레코드 선언, 보존 및 최종 처리에 이르는 전체 콘텐츠 수명 주기 동안 레이블 및 레이블-콘텐츠 간 활동을 트래버스하는 통합 방법을 제공합니다.
ms.openlocfilehash: 792729d55f7096114694a59d7202b36fc130e48c
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30221188"
---
# <a name="overview-of-file-plan-manager"></a><span data-ttu-id="6407c-103">파일 계획 관리자 개요</span><span class="sxs-lookup"><span data-stu-id="6407c-103">Overview of file plan manager</span></span>

<span data-ttu-id="6407c-104">파일 계획 관리자는 보존 레이블 및 정책에 대한 고급 관리 기능을 제공하고, 생성부터 공동 작업, 레코드 선언, 보존 및 최종 처리에 이르는 전체 콘텐츠 수명 주기 동안 레이블 및 레이블-콘텐츠 간 활동을 트래버스하는 통합 방법을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="6407c-104">File plan manager provides advanced management capabilities for retention labels and policies, and provides an integrated way to traverse label and label-to-content activity for your entire content lifecycle – from creation, through collaboration, record declaration, retention, and finally disposition.</span></span>

![파일 계획 페이지](media/file-plan-page.png)

## <a name="important-this-feature-is-currently-available-only-as-part-of-the-office-365-preview-program"></a><span data-ttu-id="6407c-106">중요: 이 기능은 현재 Office 365 미리 보기 프로그램의 일부로만 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6407c-106">Important: This feature is currently available only as part of the Office 365 Preview program</span></span>

<span data-ttu-id="6407c-107">조직이 Office 365 미리 보기 프로그램에 등록한 경우에만 테넌트에서 이 기능을 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6407c-107">You will see this feature in your tenant only if your organization has enrolled in the Office 365 Preview program.</span></span>

## <a name="accessing-file-plan-manager"></a><span data-ttu-id="6407c-108">파일 계획 관리자 액세스</span><span class="sxs-lookup"><span data-stu-id="6407c-108">Accessing file plan manager</span></span>

<span data-ttu-id="6407c-109">파일 계획 관리자에 액세스하려면 다음 두 가지 요구 사항이 충족되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="6407c-109">There are two requirements to access file plan manager, they are:</span></span>
- <span data-ttu-id="6407c-110">Office 365 Enterprise E5 구독</span><span class="sxs-lookup"><span data-stu-id="6407c-110">An Office 365 Enterprise E5 subscription.</span></span>
- <span data-ttu-id="6407c-111">사용자에게 보안 및 준수 센터의 다음 역할 중 하나가 할당되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="6407c-111">The user has been in assigned one of the following roles of the Security &amp; Compliance Center:</span></span> 
    - <span data-ttu-id="6407c-112">보존 관리자</span><span class="sxs-lookup"><span data-stu-id="6407c-112">Retention Manager</span></span>
    - <span data-ttu-id="6407c-113">보기 전용 보존 관리자</span><span class="sxs-lookup"><span data-stu-id="6407c-113">View-only Retention Manager</span></span>

## <a name="navigating-your-file-plan"></a><span data-ttu-id="6407c-114">파일 계획 탐색</span><span class="sxs-lookup"><span data-stu-id="6407c-114">Navigating your file plan</span></span>

<span data-ttu-id="6407c-115">파일 계획 관리자를 사용하면 하나의 보기에서 모든 보존 레이블 및 정책의 설정을 보다 쉽게 검토할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6407c-115">File plan manager makes it easier see into and across the settings of all your retention labels and policies from one view.</span></span>

<span data-ttu-id="6407c-116">파일 계획 외부에서 만들어진 보존 레이블도 파일 계획에서 사용할 수 있고 그 반대의 경우도 가능합니다.</span><span class="sxs-lookup"><span data-stu-id="6407c-116">Note that retention labels created outside of the file plan will be available in the file plan and vice versa.</span></span>

<span data-ttu-id="6407c-117">**파일 계획 레이블** 탭에서 다음과 같은 추가 정보 및 기능을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6407c-117">On the **file plan labels** tab, the following additional information and capabilities are available:</span></span>

### <a name="label-settings-columns"></a><span data-ttu-id="6407c-118">레이블 설정 열</span><span class="sxs-lookup"><span data-stu-id="6407c-118">Label settings columns</span></span>
 
- <span data-ttu-id="6407c-p101">**기준**은 보존 기간을 시작할 트리거 유형을 식별합니다. 유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="6407c-p101">**Based on** identifies the type of trigger that will start the retention period. Valid values are:</span></span> 
    - <span data-ttu-id="6407c-121">이벤트</span><span class="sxs-lookup"><span data-stu-id="6407c-121">Event</span></span>
    - <span data-ttu-id="6407c-122">만든 날짜</span><span class="sxs-lookup"><span data-stu-id="6407c-122">When created</span></span>
    - <span data-ttu-id="6407c-123">마지막으로 수정한 날짜</span><span class="sxs-lookup"><span data-stu-id="6407c-123">When last modified</span></span>
    - <span data-ttu-id="6407c-124">레이블을 지정한 날짜</span><span class="sxs-lookup"><span data-stu-id="6407c-124">When labeled</span></span>
- <span data-ttu-id="6407c-p102">**레코드**는 레이블이 적용될 때 항목이 선언된 레코드가 될지를 식별합니다. 유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="6407c-p102">**Record** identifies if the item will become a declared record when the label is applied. Valid values are:</span></span>
    - <span data-ttu-id="6407c-127">아니요</span><span class="sxs-lookup"><span data-stu-id="6407c-127">No</span></span>
    - <span data-ttu-id="6407c-128">예</span><span class="sxs-lookup"><span data-stu-id="6407c-128">Yes</span></span>
    - <span data-ttu-id="6407c-129">예(규정)</span><span class="sxs-lookup"><span data-stu-id="6407c-129">Yes(Regulatory)</span></span>
- <span data-ttu-id="6407c-p103">**보존**은 보존 유형을 식별합니다. 유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="6407c-p103">**Retention** identifies the retention type. Valid values are:</span></span>
    - <span data-ttu-id="6407c-132">유지</span><span class="sxs-lookup"><span data-stu-id="6407c-132">Keep</span></span>
    - <span data-ttu-id="6407c-133">유지 및 삭제</span><span class="sxs-lookup"><span data-stu-id="6407c-133">Keep and delete</span></span>
    - <span data-ttu-id="6407c-134">삭제</span><span class="sxs-lookup"><span data-stu-id="6407c-134">Delete</span></span>
- <span data-ttu-id="6407c-p104">**처리**는 보존 기간이 끝날 때 콘텐츠에 대해 수행할 작업을 식별합니다. 유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="6407c-p104">**Disposition** identifies what will happen to the content at the end of the retention period. Valid values are:</span></span> 
    - <span data-ttu-id="6407c-137">null</span><span class="sxs-lookup"><span data-stu-id="6407c-137">null</span></span>
    - <span data-ttu-id="6407c-138">작업 없음</span><span class="sxs-lookup"><span data-stu-id="6407c-138">No action</span></span>
    - <span data-ttu-id="6407c-139">자동 삭제</span><span class="sxs-lookup"><span data-stu-id="6407c-139">Auto-delete</span></span>
    - <span data-ttu-id="6407c-140">검토 필요(즉, 처리 검토)</span><span class="sxs-lookup"><span data-stu-id="6407c-140">Review required (aka Disposition review)</span></span>

![파일 계획의 레이블 설정](media/file-plan-label-columns.png)

### <a name="label-file-plan-descriptors-columns"></a><span data-ttu-id="6407c-142">레이블 파일 계획 설명자 열</span><span class="sxs-lookup"><span data-stu-id="6407c-142">Label file plan descriptors columns</span></span>

<span data-ttu-id="6407c-p105">이제 보존 레이블 구성에 더 많은 정보를 포함할 수 있습니다. 레이블에 파일 계획 설명자를 삽입하면 파일 계획의 관리 효율성과 구성이 개선됩니다.</span><span class="sxs-lookup"><span data-stu-id="6407c-p105">You can now include more information in the configuration of your retention labels. Inserting file plan descriptors into labels will improve the manageability and organization of your file plan.</span></span>

<span data-ttu-id="6407c-p106">시작하기 위해 파일 계획 관리자에서는 직무/부서, 범주, 권한 유형 및 프로비저닝/인용에 대한 기본 제공 값을 제공합니다. 보존 레이블을 만들거나 편집할 때 새 파일 계획 설명자 값을 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6407c-p106">To get you started, file plan manager provides some out-of-box values for: Function/department, Category, Authority type and Provision/citation. You can add new file plan descriptor values when creating or editing a retention label.</span></span>

<span data-ttu-id="6407c-147">보존 레이블을 만들거나 편집할 때의 파일 계획 설명자 단계 보기는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="6407c-147">Here's a view of the file plan descriptors step when creating or editing a retention label.</span></span>

![파일 계획 설명자](media/file-plan-descriptors.png)

<span data-ttu-id="6407c-149">파일 계획 관리자의 레이블 탭에 표시되는 파일 계획 설명자 열 보기는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="6407c-149">Here's a view of the file plan descriptors columns on the labels tab of file plan manager.</span></span>

![file-plan-descriptors-on-labels-tab.png](media/file-plan-descriptors-on-labels-tab.png)

## <a name="export-labels-out-of-your-file-plan"></a><span data-ttu-id="6407c-151">파일 계획에서 레이블 내보내기</span><span class="sxs-lookup"><span data-stu-id="6407c-151">Export labels out of your file plan</span></span>

<span data-ttu-id="6407c-152">파일 계획 관리자에서 모든 보존 레이블의 세부 정보를 .csv 파일로 내보내 조직의 데이터 거버넌스 이해 관계자와 함께 정기적인 검토를 편리하게 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6407c-152">From file plan manager, you can export the details of all retention labels into a .csv file to assist you in facilitating periodic compliance reviews with data governance stakeholders in your organization.</span></span>

<span data-ttu-id="6407c-153">모든 보존 레이블의 내보내려면 **파일 계획 관리자** \> **파일 계획 작업** \> **레이블 내보내기**로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="6407c-153">To export all retention labels, go to **file plan manager** \> **file plan actions** \> **export labels**.</span></span>

![파일 계획 내보내기 옵션](media/file-plan-export-labels-option.png)

<span data-ttu-id="6407c-155">모든 기존 보존 레이블을 포함하는 \*.csv 파일이 열립니다.</span><span class="sxs-lookup"><span data-stu-id="6407c-155">A \*.csv file containing all existing retention labels will open.</span></span>

![모든 보존 레이블이 표시되는 CSV 파일](media/file-plan-csv-file.png)

## <a name="import-labels-into-your-file-plan"></a><span data-ttu-id="6407c-157">파일 계획으로 레이블 가져오기</span><span class="sxs-lookup"><span data-stu-id="6407c-157">Import labels into your file plan</span></span>

<span data-ttu-id="6407c-158">파일 계획 관리자에서 기존 보존 레이블을 수정할 수 있을 뿐만 아니라 새 레이블을 대량으로 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6407c-158">From file plan manager, you can bulk import new labels as well as modify existing retention labels.</span></span>

<span data-ttu-id="6407c-159">새 보존 레이블이 가져오고 기존 보존 레이블을 업데이트하려면 **파일 계획 관리자** \> **파일 계획 작업** \> **레이블 가져오기**로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="6407c-159">To import new retention labels and make updates existing retention labels, go to **file plan manager** \> **file plan actions** \> **import labels**.</span></span>

![파일 계획 가져오기 옵션](media/file-plan-import-labels-option.png)

![빈 파일 계획 서식 파일 다운로드 옵션](media/file-plan-blank-template-option.png)

<span data-ttu-id="6407c-162">빈 서식 파일을 다운로드합니다(또는 현재 파일 계획의 내보내기 기능을 통해 시작).</span><span class="sxs-lookup"><span data-stu-id="6407c-162">Download a blank template (or start from an export of your current file plan).</span></span>

![Excel에서 빈 파일 계획 서식 파일 열기](media/file-plan-blank-template.png)

<span data-ttu-id="6407c-164">서식 파일을 채웁니다(항목에 대한 유효한 값에 대한 참조 정보가 곧 제공될 예정임).</span><span class="sxs-lookup"><span data-stu-id="6407c-164">Fill-out the template (coming soon is reference information about valid values for entries).</span></span>

![정보가 채워진 파일 계획 서식 파일](media/file-plan-filled-out-template.png)

<span data-ttu-id="6407c-166">채운 서식 파일을 업로드하면 파일 계획 관리자에서 항목의 유효성을 검사하고 가져오기 통계를 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="6407c-166">Upload the filled-out template, and file plan manager will validate the entries and display import statistics.</span></span>

![파일 계획 가져오기 통계](media/file-plan-import-statistics.png)

<span data-ttu-id="6407c-168">가져오기가 완료되면 파일 계획 관리자로 돌아가 새 정책 또는 기존 정책에 새 레이블을 할당합니다.</span><span class="sxs-lookup"><span data-stu-id="6407c-168">When the import is complete, return to file plan manager to assign new labels to new or existing policies.</span></span>

![레이블 게시 옵션](media/file-plan-publish-labels-option.png)

