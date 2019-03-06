---
title: 파일 계획 관리자 개요
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 9/25/2018
ms.audience: Admin
ms.topic: conceptual
ms.service: O365-seccomp
localization_priority: Priority
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: af398293-c69d-465e-a249-d74561552d30
description: 파일 계획 관리자는 보존 레이블 및 정책에 대한 고급 관리 기능을 제공하고, 생성부터 공동 작업, 레코드 선언, 보존 및 최종 처리에 이르는 전체 콘텐츠 수명 주기 동안 레이블 및 레이블-콘텐츠 간 활동을 트래버스하는 통합 방법을 제공합니다.
ms.openlocfilehash: 328b8f1aeed3e25fb0ab5eb651fb3846b123747c
ms.sourcegitcommit: ed822a776d3419853453583e882f3c61ca26d4b2
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/05/2019
ms.locfileid: "30410523"
---
# <a name="overview-of-file-plan-manager"></a><span data-ttu-id="302c5-103">파일 계획 관리자 개요</span><span class="sxs-lookup"><span data-stu-id="302c5-103">Overview of file plan manager</span></span>

<span data-ttu-id="302c5-104">파일 계획 관리자는 보존 레이블 및 정책에 대한 고급 관리 기능을 제공하고, 생성부터 공동 작업, 레코드 선언, 보존 및 최종 처리에 이르는 전체 콘텐츠 수명 주기 동안 레이블 및 레이블-콘텐츠 간 활동을 트래버스하는 통합 방법을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="302c5-104">File plan manager provides advanced management capabilities for retention labels and policies, and provides an integrated way to traverse label and label-to-content activity for your entire content lifecycle – from creation, through collaboration, record declaration, retention, and finally disposition.</span></span>

![파일 계획 페이지](media/file-plan-page.png)

## <a name="accessing-file-plan-manager"></a><span data-ttu-id="302c5-106">파일 계획 관리자 액세스</span><span class="sxs-lookup"><span data-stu-id="302c5-106">Accessing file plan manager</span></span>

<span data-ttu-id="302c5-107">파일 계획 관리자에 액세스하려면 다음 두 가지 요구 사항이 충족되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="302c5-107">There are two requirements to access file plan manager, they are:</span></span>
- <span data-ttu-id="302c5-108">Office 365 Enterprise E5 구독</span><span class="sxs-lookup"><span data-stu-id="302c5-108">An Office 365 Enterprise E5 subscription.</span></span>
- <span data-ttu-id="302c5-109">사용자에게 보안 및 준수 센터의 다음 역할 중 하나가 할당되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="302c5-109">The user has been in assigned one of the following roles of the Security &amp; Compliance Center:</span></span> 
    - <span data-ttu-id="302c5-110">보존 관리자</span><span class="sxs-lookup"><span data-stu-id="302c5-110">Retention Manager</span></span>
    - <span data-ttu-id="302c5-111">보기 전용 보존 관리자</span><span class="sxs-lookup"><span data-stu-id="302c5-111">View-only Retention Manager</span></span>

## <a name="navigating-your-file-plan"></a><span data-ttu-id="302c5-112">파일 계획 탐색</span><span class="sxs-lookup"><span data-stu-id="302c5-112">Navigating your file plan</span></span>

<span data-ttu-id="302c5-113">파일 계획 관리자를 사용하면 하나의 보기에서 모든 보존 레이블 및 정책의 설정을 보다 쉽게 검토할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="302c5-113">File plan manager makes it easier see into and across the settings of all your retention labels and policies from one view.</span></span>

<span data-ttu-id="302c5-114">파일 계획 외부에서 만들어진 보존 레이블도 파일 계획에서 사용할 수 있고 그 반대의 경우도 가능합니다.</span><span class="sxs-lookup"><span data-stu-id="302c5-114">Note that retention labels created outside of the file plan will be available in the file plan and vice versa.</span></span>

<span data-ttu-id="302c5-115">**파일 계획 레이블** 탭에서 다음과 같은 추가 정보 및 기능을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="302c5-115">On the **file plan labels** tab, the following additional information and capabilities are available:</span></span>

### <a name="label-settings-columns"></a><span data-ttu-id="302c5-116">레이블 설정 열</span><span class="sxs-lookup"><span data-stu-id="302c5-116">Label settings columns</span></span>
 
- <span data-ttu-id="302c5-p101">**기준**은 보존 기간을 시작할 트리거 유형을 식별합니다. 유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="302c5-p101">**Based on** identifies the type of trigger that will start the retention period. Valid values are:</span></span> 
    - <span data-ttu-id="302c5-119">이벤트</span><span class="sxs-lookup"><span data-stu-id="302c5-119">Event</span></span>
    - <span data-ttu-id="302c5-120">만든 날짜</span><span class="sxs-lookup"><span data-stu-id="302c5-120">When created</span></span>
    - <span data-ttu-id="302c5-121">마지막으로 수정한 날짜</span><span class="sxs-lookup"><span data-stu-id="302c5-121">When last modified</span></span>
    - <span data-ttu-id="302c5-122">레이블을 지정한 날짜</span><span class="sxs-lookup"><span data-stu-id="302c5-122">When labeled</span></span>
- <span data-ttu-id="302c5-p102">**레코드**는 레이블이 적용될 때 항목이 선언된 레코드가 될지를 식별합니다. 유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="302c5-p102">**Record** identifies if the item will become a declared record when the label is applied. Valid values are:</span></span>
    - <span data-ttu-id="302c5-125">아니요</span><span class="sxs-lookup"><span data-stu-id="302c5-125">No</span></span>
    - <span data-ttu-id="302c5-126">예</span><span class="sxs-lookup"><span data-stu-id="302c5-126">Yes</span></span>
    - <span data-ttu-id="302c5-127">예(규정)</span><span class="sxs-lookup"><span data-stu-id="302c5-127">Yes(Regulatory)</span></span>
- <span data-ttu-id="302c5-p103">**보존**은 보존 유형을 식별합니다. 유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="302c5-p103">**Retention** identifies the retention type. Valid values are:</span></span>
    - <span data-ttu-id="302c5-130">유지</span><span class="sxs-lookup"><span data-stu-id="302c5-130">Keep</span></span>
    - <span data-ttu-id="302c5-131">유지 및 삭제</span><span class="sxs-lookup"><span data-stu-id="302c5-131">Keep and delete</span></span>
    - <span data-ttu-id="302c5-132">삭제</span><span class="sxs-lookup"><span data-stu-id="302c5-132">Delete</span></span>
- <span data-ttu-id="302c5-p104">**처리**는 보존 기간이 끝날 때 콘텐츠에 대해 수행할 작업을 식별합니다. 유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="302c5-p104">**Disposition** identifies what will happen to the content at the end of the retention period. Valid values are:</span></span> 
    - <span data-ttu-id="302c5-135">null</span><span class="sxs-lookup"><span data-stu-id="302c5-135">null</span></span>
    - <span data-ttu-id="302c5-136">작업 없음</span><span class="sxs-lookup"><span data-stu-id="302c5-136">No action</span></span>
    - <span data-ttu-id="302c5-137">자동 삭제</span><span class="sxs-lookup"><span data-stu-id="302c5-137">Auto-delete</span></span>
    - <span data-ttu-id="302c5-138">검토 필요(즉, 처리 검토)</span><span class="sxs-lookup"><span data-stu-id="302c5-138">Review required (aka Disposition review)</span></span>

![파일 계획의 레이블 설정](media/file-plan-label-columns.png)

### <a name="label-file-plan-descriptors-columns"></a><span data-ttu-id="302c5-140">레이블 파일 계획 설명자 열</span><span class="sxs-lookup"><span data-stu-id="302c5-140">Label file plan descriptors columns</span></span>

<span data-ttu-id="302c5-p105">이제 보존 레이블 구성에 더 많은 정보를 포함할 수 있습니다. 레이블에 파일 계획 설명자를 삽입하면 파일 계획의 관리 효율성과 구성이 개선됩니다.</span><span class="sxs-lookup"><span data-stu-id="302c5-p105">You can now include more information in the configuration of your retention labels. Inserting file plan descriptors into labels will improve the manageability and organization of your file plan.</span></span>

<span data-ttu-id="302c5-p106">시작하기 위해 파일 계획 관리자에서는 직무/부서, 범주, 권한 유형 및 프로비저닝/인용에 대한 기본 제공 값을 제공합니다. 보존 레이블을 만들거나 편집할 때 새 파일 계획 설명자 값을 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="302c5-p106">To get you started, file plan manager provides some out-of-box values for: Function/department, Category, Authority type and Provision/citation. You can add new file plan descriptor values when creating or editing a retention label.</span></span>

<span data-ttu-id="302c5-145">보존 레이블을 만들거나 편집할 때의 파일 계획 설명자 단계 보기는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="302c5-145">Here's a view of the file plan descriptors step when creating or editing a retention label.</span></span>

![파일 계획 설명자](media/file-plan-descriptors.png)

<span data-ttu-id="302c5-147">파일 계획 관리자의 레이블 탭에 표시되는 파일 계획 설명자 열 보기는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="302c5-147">Here's a view of the file plan descriptors columns on the labels tab of file plan manager.</span></span>

![file-plan-descriptors-on-labels-tab.png](media/file-plan-descriptors-on-labels-tab.png)

## <a name="export-labels-out-of-your-file-plan"></a><span data-ttu-id="302c5-149">파일 계획에서 레이블 내보내기</span><span class="sxs-lookup"><span data-stu-id="302c5-149">Export labels out of your file plan</span></span>

<span data-ttu-id="302c5-150">파일 계획 관리자에서 모든 보존 레이블의 세부 정보를 .csv 파일로 내보내 조직의 데이터 거버넌스 이해 관계자와 함께 정기적인 검토를 편리하게 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="302c5-150">From file plan manager, you can export the details of all retention labels into a .csv file to assist you in facilitating periodic compliance reviews with data governance stakeholders in your organization.</span></span>

<span data-ttu-id="302c5-151">모든 보존 레이블의 내보내려면 **파일 계획 관리자** \> **파일 계획 작업** \> **레이블 내보내기**로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="302c5-151">To export all retention labels, go to **file plan manager** \> **file plan actions** \> **export labels**.</span></span>

![파일 계획 내보내기 옵션](media/file-plan-export-labels-option.png)

<span data-ttu-id="302c5-153">모든 기존 보존 레이블을 포함하는 \*.csv 파일이 열립니다.</span><span class="sxs-lookup"><span data-stu-id="302c5-153">A \*.csv file containing all existing retention labels will open.</span></span>

![모든 보존 레이블이 표시되는 CSV 파일](media/file-plan-csv-file.png)

## <a name="import-labels-into-your-file-plan"></a><span data-ttu-id="302c5-155">파일 계획으로 레이블 가져오기</span><span class="sxs-lookup"><span data-stu-id="302c5-155">Import labels into your file plan</span></span>

<span data-ttu-id="302c5-156">파일 계획 관리자에서 기존 보존 레이블을 수정할 수 있을 뿐만 아니라 새 레이블을 대량으로 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="302c5-156">From file plan manager, you can bulk import new labels as well as modify existing retention labels.</span></span>

<span data-ttu-id="302c5-157">새 보존 레이블이 가져오고 기존 보존 레이블을 업데이트하려면 **파일 계획 관리자** \> **파일 계획 작업** \> **레이블 가져오기**로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="302c5-157">To import new retention labels and make updates existing retention labels, go to **file plan manager** \> **file plan actions** \> **import labels**.</span></span>

![파일 계획 가져오기 옵션](media/file-plan-import-labels-option.png)

![빈 파일 계획 서식 파일 다운로드 옵션](media/file-plan-blank-template-option.png)

<span data-ttu-id="302c5-160">빈 서식 파일을 다운로드합니다(또는 현재 파일 계획의 내보내기 기능을 통해 시작).</span><span class="sxs-lookup"><span data-stu-id="302c5-160">Download a blank template (or start from an export of your current file plan).</span></span>

![Excel에서 빈 파일 계획 서식 파일 열기](media/file-plan-blank-template.png)

<span data-ttu-id="302c5-162">서식 파일을 채웁니다(항목에 대한 유효한 값에 대한 참조 정보가 곧 제공될 예정임).</span><span class="sxs-lookup"><span data-stu-id="302c5-162">Fill-out the template (coming soon is reference information about valid values for entries).</span></span>

![정보가 채워진 파일 계획 서식 파일](media/file-plan-filled-out-template.png)

<span data-ttu-id="302c5-164">채운 서식 파일을 업로드하면 파일 계획 관리자에서 항목의 유효성을 검사하고 가져오기 통계를 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="302c5-164">Upload the filled-out template, and file plan manager will validate the entries and display import statistics.</span></span>

![파일 계획 가져오기 통계](media/file-plan-import-statistics.png)

<span data-ttu-id="302c5-166">가져오기가 완료되면 파일 계획 관리자로 돌아가 새 정책 또는 기존 정책에 새 레이블을 할당합니다.</span><span class="sxs-lookup"><span data-stu-id="302c5-166">When the import is complete, return to file plan manager to assign new labels to new or existing policies.</span></span>

![레이블 게시 옵션](media/file-plan-publish-labels-option.png)

