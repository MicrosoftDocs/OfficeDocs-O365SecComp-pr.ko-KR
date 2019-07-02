---
title: 고급 eDiscovery에서 변호사 설정-클라이언트 권한 검색
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: ''
ROBOTS: NOINDEX, NOFOLLOW
description: 고급 eDiscovery 사례에서 콘텐츠를 검토할 때 권한 있는 콘텐츠의 컴퓨터 학습 기반 검색을 사용 하려면 변호사-클라이언트 권한 검색 모델을 사용 합니다.
ms.openlocfilehash: 16a6a215484c35d20fbe071cac033133270b7ea6
ms.sourcegitcommit: e323610df2df71c84f536e8a38650d33d8069e41
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/04/2019
ms.locfileid: "34703900"
---
# <a name="set-up-attorney-client-privilege-detection-in-advanced-ediscovery"></a><span data-ttu-id="0ac0f-103">고급 eDiscovery에서 변호사 설정-클라이언트 권한 검색</span><span class="sxs-lookup"><span data-stu-id="0ac0f-103">Set up attorney-client privilege detection in Advanced eDiscovery</span></span>

<span data-ttu-id="0ac0f-104">EDiscovery 프로세스의 검토 단계에서 주요 및 비용이 많이 드는 부분은 권한 있는 콘텐츠에 대 한 문서를 검토 하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="0ac0f-104">A major and costly aspect of the review phase of any eDiscovery process is reviewing documents for privileged content.</span></span> <span data-ttu-id="0ac0f-105">고급 eDiscovery에서는이 프로세스를 보다 효율적으로 수행할 수 있도록 권한 있는 콘텐츠에 대 한 컴퓨터 학습 기반 검색 기능을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ac0f-105">Advanced eDiscovery provides machine learning-based detection of privileged content to make this process more efficient.</span></span> <span data-ttu-id="0ac0f-106">이 기능을 *변호사-클라이언트 권한 검색*이라고 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ac0f-106">This feature is called *attorney-client privilege detection*.</span></span>

> [!NOTE]
> <span data-ttu-id="0ac0f-107">사용 하려면 먼저 변호사-클라이언트 권한 검색 모델을 선택 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ac0f-107">You must opt in to the attorney-client privilege detection model before you can use it.</span></span> <span data-ttu-id="0ac0f-108">지침은 [1 단계](#step-1-opt-in-to-attorney-client-privilege-detection) 를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="0ac0f-108">See [Step 1](#step-1-opt-in-to-attorney-client-privilege-detection) for instructions.</span></span>

## <a name="how-does-it-work"></a><span data-ttu-id="0ac0f-109">작동 방식</span><span class="sxs-lookup"><span data-stu-id="0ac0f-109">How does it work?</span></span>

<span data-ttu-id="0ac0f-110">변호사-클라이언트 권한 검색이 사용 하도록 설정 되 면 검토 집합의 모든 문서가 검토 집합의 [데이터를 분석할](analyzing-data-in-review-set.md) 때 변호사-클라이언트 권한 검색 모델에 의해 처리 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0ac0f-110">When attorney-client privilege detection is enabled, all documents in a review set will be processed by the attorney-client privilege detection model when you [analyze the data](analyzing-data-in-review-set.md) in the review set.</span></span> <span data-ttu-id="0ac0f-111">모델에서는 다음과 같은 두 가지 항목을 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="0ac0f-111">The model looks for two things:</span></span>

- <span data-ttu-id="0ac0f-112">권한 있는 콘텐츠-모델에서 기계 학습을 사용 하 여 문서에 특성으로 적합 한 콘텐츠가 포함 될 가능성을 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ac0f-112">Privileged content – The model uses machine learning to determine the likelihood that the document contains content that is legal in nature.</span></span>

- <span data-ttu-id="0ac0f-113">참석자-변호사-클라이언트 권한 검색을 설정 하는 과정에서 조직의 변호사 목록을 제출 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ac0f-113">Participants – As part of setting up attorney-client privilege detection, you have to submit a list of attorneys for your organization.</span></span> <span data-ttu-id="0ac0f-114">그런 다음이 모델은 문서 참여자와 변호사 목록을 비교 하 여 문서에 변호사 참가자가 한 명 이상 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ac0f-114">The model then compares the participants of the document with the attorney list to determine if a document has at least one attorney participant.</span></span>

<span data-ttu-id="0ac0f-115">모델은 모든 문서에 대해 다음과 같은 세 가지 속성을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ac0f-115">The model produces the following three properties for every document:</span></span>

- <span data-ttu-id="0ac0f-116">**AttorneyClientPrivilegeScore** – 문서가 합법적으로 법적 되는 확률입니다. 점수 값은 **0** 에서 **1**사이입니다.</span><span class="sxs-lookup"><span data-stu-id="0ac0f-116">**AttorneyClientPrivilegeScore** – The likelihood the document is legal in nature; the values for the score are between **0** and **1**.</span></span>

- <span data-ttu-id="0ac0f-117">**Hasattorney** – 문서 참가자 중 하나가 변호사 목록에 나열 되 면이 속성은 **true** 로 설정 됩니다. 그렇지 않으면 값이 **false**입니다.</span><span class="sxs-lookup"><span data-stu-id="0ac0f-117">**HasAttorney** – This property is set to **true** if one of the document participants is listed in the attorney list; otherwise the value is **false**.</span></span> <span data-ttu-id="0ac0f-118">조직에서 변호사 목록을 업로드 하지 않은 경우에도이 값은 **false** 로 설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0ac0f-118">The value is also set to **false** if your organization didn't upload an attorney list.</span></span>

- <span data-ttu-id="0ac0f-119">**IsPrivilege** - **AttorneyClientPrivilegeScore** 의 값이 임계값을 초과 *하거나* 문서에 변호사 참가자가 있는 경우이 속성은 **true** 로 설정 됩니다. 그렇지 않으면 값이 **false**로 설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0ac0f-119">**IsPrivilege** – This property is set to **true** if the value for **AttorneyClientPrivilegeScore** is above the threshold *or* if the document has an attorney participant; otherwise the value is set to **false**.</span></span>

<span data-ttu-id="0ac0f-120">이러한 속성 및 해당 값은 다음 스크린샷에 표시 된 것 처럼 검토 집합에 있는 문서의 파일 메타 데이터에 추가 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0ac0f-120">These properties (and their corresponding values) are added to the file metadata of the documents in a review set, as shown in the following screenshot:</span></span>

![변호사-파일 메타 데이터에 표시 되는 클라이언트 권한 속성](../media/AeDAttorneyClientPrivilegeMetadata.png)

<span data-ttu-id="0ac0f-122">검토 집합 내 에서도 이러한 세 가지 속성을 검색할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0ac0f-122">These three properties are also searchable within a review set.</span></span> <span data-ttu-id="0ac0f-123">자세한 내용은 [검토 집합에서 데이터 쿼리](review-set-search.md)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="0ac0f-123">For more information, see [Query the data in a review set](review-set-search.md).</span></span>

## <a name="set-up-the-attorney-client-privilege-detection-model"></a><span data-ttu-id="0ac0f-124">변호사 설정-클라이언트 권한 검색 모델</span><span class="sxs-lookup"><span data-stu-id="0ac0f-124">Set up the attorney-client privilege detection model</span></span>

<span data-ttu-id="0ac0f-125">변호사 클라이언트 권한 검색 모델을 사용 하도록 설정 하려면 조직에서 변호사 목록을 옵트인 한 다음 업로드 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ac0f-125">To enable the attorney-client privilege detection model, your organization has to opt-in and then upload an attorney list.</span></span>

### <a name="step-1-opt-in-to-attorney-client-privilege-detection"></a><span data-ttu-id="0ac0f-126">1 단계: 변호사에 게 옵트인-클라이언트 권한 검색</span><span class="sxs-lookup"><span data-stu-id="0ac0f-126">Step 1: Opt-in to attorney-client privilege detection</span></span>

<span data-ttu-id="0ac0f-127">앞에서 언급 했 듯이 변호사-클라이언트 권한 검색 모델이 미리 보기에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0ac0f-127">As previously stated, the attorney-client privilege detection model is in Preview.</span></span> <span data-ttu-id="0ac0f-128">따라서 조직 eDiscovery 관리자 (eDiscovery 관리자 역할 그룹의 eDiscovery 관리자 그룹의 구성원)가 해당 사용자에 게 고급 eDiscovery 사례에서 모델을 사용할 수 있도록 옵트인 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ac0f-128">Therefore a person in your organization eDiscovery Administrator (a member of the eDiscovery Administrator subgroup in the eDiscovery Manager role group) must opt in to make the model available in your Advanced eDiscovery cases.</span></span>

1. <span data-ttu-id="0ac0f-129">보안 & 준수 센터에서 **eDiscovery > Advanced ediscovery**로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ac0f-129">In the Security & Compliance Center, go to **eDiscovery > Advanced eDiscovery**.</span></span>

2. <span data-ttu-id="0ac0f-130">**고급 eDiscovery** 홈 페이지의 **설정** 타일에서 **실험적 기능 구성을**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ac0f-130">On the **Advanced eDiscovery** home page, in the **Settings** tile, click **Configure experimental features**.</span></span>

   !["실험적 기능 구성"을 클릭 합니다.](../media/AeDExperimentalFeatures.png)

3. <span data-ttu-id="0ac0f-132">**실험적 기능** 탭에서 **변호사 관리-클라이언트 권한 설정을**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ac0f-132">On the **Experimental features** tab, click **Manage attorney-client privilege setting**.</span></span>

4. <span data-ttu-id="0ac0f-133">**변호사-클라이언트 권한** 플라이 아웃 페이지에서 기능을 설정 하려면 설정/해제를 클릭 한 다음 **저장**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ac0f-133">On the **Attorney-client privilege** flyout page, click the toggle to turn on the feature and then click **Save**.</span></span>

### <a name="step-2-upload-a-list-of-attorneys-optional"></a><span data-ttu-id="0ac0f-134">2 단계: 변호사 목록 업로드 (선택 사항)</span><span class="sxs-lookup"><span data-stu-id="0ac0f-134">Step 2: Upload a list of attorneys (optional)</span></span>

<span data-ttu-id="0ac0f-135">변호사-클라이언트 권한 검색 모델을 최대한 활용 하 고 앞에서 설명한 **변호사** 또는 **잠재적으로 권한이 부여** 된 검색의 결과를 사용 하려면 다음에 대 한 전자 메일 주소 목록을 업로드 하는 것이 좋습니다. 조직에 대 한 작업을 수행 하는 변호사 및 법적 담당자</span><span class="sxs-lookup"><span data-stu-id="0ac0f-135">To take full advantage of the attorney-client privilege detection model and use the results of the **Has Attorney** or **Potentially Privileged** detection that was previously described, we recommend that you upload a list of email addresses for the lawyers and legal personnel who work for your organization.</span></span> 

<span data-ttu-id="0ac0f-136">변호사-클라이언트 권한 검색 모델에서 사용할 변호사 목록을 업로드 하려면 다음을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ac0f-136">To upload an attorney list for use by the attorney-client privilege detection model:</span></span>

1. <span data-ttu-id="0ac0f-137">머리글 행 없이 .csv 파일을 만들고 각 사용자의 전자 메일 주소를 별도의 줄에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ac0f-137">Create a .csv file (without a header row) and add the email address for each appropriate person on a separate line.</span></span> <span data-ttu-id="0ac0f-138">이 파일을 로컬 컴퓨터에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ac0f-138">Save this file to your local computer.</span></span>

2. <span data-ttu-id="0ac0f-139">**고급 eDiscovery** 홈 페이지의 **설정** 타일에서 **실험적 기능 구성을**클릭 하 고 **변호사 관리-클라이언트 권한 설정을**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ac0f-139">On the **Advanced eDiscovery** home page, in the **Settings** tile, click **Configure experimental features**, and then click **Manage attorney-client privilege setting**.</span></span>

   <span data-ttu-id="0ac0f-140">**변호사-클라이언트** 권한 **검색** 전환 기능이 설정 된 상태로 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0ac0f-140">The **Attorney-client privilege** page is displayed, and the **Attorney-client privilege detection** toggle is turned on.</span></span>

   ![변호사-클라이언트 권한 플라이 아웃 페이지](../media/AeDUploadAttorneyList.png)

3. <span data-ttu-id="0ac0f-142">**찾아보기를** 클릭 한 다음 1 단계에서 만든 .csv 파일을 찾아 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ac0f-142">Click **Browse** and then find and select the .csv file that you created in step 1.</span></span>

4. <span data-ttu-id="0ac0f-143">**저장** 을 클릭 하 여 변호사 목록을 업로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ac0f-143">Click **Save** to upload the attorney list.</span></span>

## <a name="use-the-attorney-client-privilege-detection-model"></a><span data-ttu-id="0ac0f-144">변호사-클라이언트 권한 검색 모델 사용</span><span class="sxs-lookup"><span data-stu-id="0ac0f-144">Use the attorney-client privilege detection model</span></span>

<span data-ttu-id="0ac0f-145">검토 집합의 문서에 대해 변호사-클라이언트 권한 검색을 사용 하려면이 섹션의 단계를 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ac0f-145">Follow the steps in this section to use attorney-client privilege detection for documents in a review set.</span></span>

### <a name="step-1-create-a-smart-tag-group-with-attorney-client-privilege-detection-model"></a><span data-ttu-id="0ac0f-146">1 단계: 변호사-클라이언트 권한 검색 모델을 사용 하 여 스마트 태그 그룹 만들기</span><span class="sxs-lookup"><span data-stu-id="0ac0f-146">Step 1: Create a smart tag group with attorney-client privilege detection model</span></span>

<span data-ttu-id="0ac0f-147">검토 프로세스에서 변호사의 결과를 확인 하는 기본 방법 중 하나는 스마트 태그 그룹을 사용 하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="0ac0f-147">One of the primary ways to see the results of attorney-client privilege detection in your review process is by using a smart tag group.</span></span> <span data-ttu-id="0ac0f-148">스마트 태그 그룹은 변호사-클라이언트 권한 검색 결과를 나타내며 스마트 태그 그룹의 태그 옆에 줄에 결과를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ac0f-148">A smart tag group indicates the results of the attorney-client privilege detection and shows the results in-line next to the tags in a smart tag group.</span></span> <span data-ttu-id="0ac0f-149">이렇게 하면 문서 검토 중에 잠재적으로 권한이 부여 된 문서를 빠르게 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0ac0f-149">This lets you quickly identify potentially privileged documents during document review.</span></span> <span data-ttu-id="0ac0f-150">또한 스마트 태그 그룹의 태그를 사용 하 여 문서에 권한이 있거나 권한이 없는 것으로 태그를 지정할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0ac0f-150">Additionally, you can also use the tags in the smart tag group to tag documents as privileged or non-privileged.</span></span> <span data-ttu-id="0ac0f-151">스마트 태그에 대 한 자세한 내용은 [Advanced eDiscovery에서 스마트 태그 설정을](smart-tags.md)참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="0ac0f-151">For more information about smart tags, see [Set up smart tags in Advanced eDiscovery](smart-tags.md).</span></span>

1. <span data-ttu-id="0ac0f-152">1 단계에서 분석 한 문서가 포함 된 검토 집합에서 **검토 설정 관리** 를 클릭 한 다음 **태그 관리**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ac0f-152">In the review set that contains the documents that you analyzed in Step 1, click **Manage review set** and then click **Manage tags**.</span></span>
 
2. <span data-ttu-id="0ac0f-153">**태그**에서 **그룹 추가** 옆에 있는 풀을 클릭 한 다음 **스마트 태그 그룹 추가**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ac0f-153">Under **Tags**, click the pull-down next to **Add group** and then click **Add smart tag group**.</span></span>

   !["스마트 태그 그룹 추가"를 클릭 합니다.](../media/AeDCreateSmartTag.png)

3. <span data-ttu-id="0ac0f-155">**스마트 태그에 대 한 모델 선택** 페이지에서 **변호사-클라이언트 권한**옆에 있는 **선택을** 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ac0f-155">On the **Choose a model for your smart tag** page, click **Select** next to **Attorney-client privilege**.</span></span>

   <span data-ttu-id="0ac0f-156">**변호사-클라이언트 권한** 이라는 태그 그룹이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0ac0f-156">A tag group named **Attorney-client privilege** is displayed.</span></span> <span data-ttu-id="0ac0f-157">여기에는 **양수** 및 **음수**라는 두 개의 하위 태그가 있으며 모델에서 생성 되는 가능한 결과에 해당 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ac0f-157">It contains two child tags named **Positive** and **Negative**, which correspond to the possible results produced by the model.</span></span>

   ![변호사-클라이언트 권한 스마트 태그 그룹](../media/AeDAttorneyClientSmartTagGroup.png)

3. <span data-ttu-id="0ac0f-159">태그 그룹 및 태그의 이름을 검토에 적합 하 게 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="0ac0f-159">Rename the tag group and tags as appropriate for your review.</span></span> <span data-ttu-id="0ac0f-160">예를 들어 **양수** 에서 **특권** 으로, 아니면 **음수가** **아닌 것**으로 이름을 바꿀 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0ac0f-160">For example, you can rename **Positive** to **Privileged** and **Negative** to **Not privileged**.</span></span>

### <a name="step-2-analyze-a-review-set"></a><span data-ttu-id="0ac0f-161">2 단계: 검토 집합 분석</span><span class="sxs-lookup"><span data-stu-id="0ac0f-161">Step 2: Analyze a review set</span></span>

<span data-ttu-id="0ac0f-162">검토 집합의 문서를 분석할 때 변호사 클라이언트 권한 검색 모델도 실행 되며 해당 속성 ([작동 방법](#how-does-it-work) 에 설명 됨)이 검토 집합의 모든 문서에 추가 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0ac0f-162">When you analyze the documents in a review set, the attorney-client privilege detection model will also be run and the corresponding properties (described in[How does it work?](#how-does-it-work) will be added to every document in the review set.</span></span> <span data-ttu-id="0ac0f-163">검토 집합에서 데이터를 분석 하는 방법에 대 한 자세한 내용은 [Advanced eDiscovery의 검토 집합에서 데이터 분석](analyzing-data-in-review-set.md)을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="0ac0f-163">For more information about analyzing data in review set, see [Analyze data in a review set in Advanced eDiscovery](analyzing-data-in-review-set.md).</span></span>

### <a name="step-3-use-the-smart-tag-group-for-review-of-privileged-content"></a><span data-ttu-id="0ac0f-164">3 단계: 스마트 태그 그룹을 사용 하 여 권한 있는 콘텐츠 검토</span><span class="sxs-lookup"><span data-stu-id="0ac0f-164">Step 3: Use the smart tag group for review of privileged content</span></span>

<span data-ttu-id="0ac0f-165">검토 집합을 분석 하 고 스마트 태그를 설정한 다음에는 문서를 검토 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ac0f-165">After analyzing the review set and setting up smart tags, the next step is to review the documents.</span></span> <span data-ttu-id="0ac0f-166">모델이 문서에 잠재적으로 권한이 부여 된 것으로 확인 된 경우 **태그 지정 패널** 의 해당 스마트 태그는 변호사-클라이언트 권한 검색에 의해 생성 되는 다음 결과를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="0ac0f-166">If the model has determined the document is potentially privileged, the corresponding smart tag in the **Tagging panel** will indicate the following results produced by the attorney-client privilege detection:</span></span>

- <span data-ttu-id="0ac0f-167">문서에 기본적으로 사용할 수 있는 콘텐츠가 포함 되어 있는 경우 해당 스마트 태그 옆에 Legal (기본 **긍정** 태그) 이라는 레이블 **법적 콘텐츠가** 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0ac0f-167">If the document has content that may be legal in nature, the label **Legal content** is displayed next to the corresponding smart tag (which in this case is the default **Positive** tag).</span></span>

- <span data-ttu-id="0ac0f-168">문서에 조직의 변호사 목록에 있는 참가자가 있는 경우 해당 스마트 태그 옆에 레이블 **변호사** 가 표시 됩니다 (이 경우에는 기본 **긍정** 태그 이기도 합니다).</span><span class="sxs-lookup"><span data-stu-id="0ac0f-168">If the document has a participant who is found in your organization's attorney list, the label **Attorney** is displayed next to the corresponding smart tag (which in this case is also the default **Positive** tag).</span></span>

- <span data-ttu-id="0ac0f-169">문서에 특성상 법적으로 참여 하 *고* 해당 하는 참가자가 변호사 목록에 있는 경우 **법적 컨텐트와** **변호사** 레이블이 모두 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0ac0f-169">If the document has content that may be legal in nature *and* has a participant found in the attorney list, both the **Legal content**  and **Attorney** labels are displayed.</span></span> 

<span data-ttu-id="0ac0f-170">모델이 문서에 법적으로 적합 하거나 변호사 목록에서 참가자를 포함 하지 않는 콘텐츠를 포함 하지 않는 것으로 확인 되 면 태그 패널에 두 레이블이 모두 표시 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0ac0f-170">If the model determines that a document doesn't contain content that is legal in nature or doesn't contain a participant from the attorney list, then neither label is displayed in the tagging panel.</span></span>

<span data-ttu-id="0ac0f-171">예를 들어 다음 스크린샷에서는 두 개의 문서를 보여 줍니다. 첫 번째 항목에는 본질적으로 유효한 콘텐츠가 포함 되어 있으며 변호사 목록에 참가자가 있습니다. 두 번째는 둘 다를 포함 하지 않으므로 레이블을 표시 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0ac0f-171">For example, the following screenshots show two documents; the first one contains content that is legal in nature and has a participant found in the list of attorneys; the second contains neither and therefore doesn't display any labels.</span></span>

![변호사 및 법적 콘텐츠 레이블이 있는 문서](../media/AeDTaggingPanelLegalContentAttorney.png)

![레이블이 없는 문서](../media/AeDTaggingPanelNegative.png)

<span data-ttu-id="0ac0f-174">문서를 검토 하 여 권한 있는 콘텐츠가 포함 되어 있는지 여부를 확인 한 후에는 해당 태그를 사용 하 여 문서에 태그를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0ac0f-174">After you review a document to see if it contains privileged content, you can tag the document with the appropriate tag.</span></span>