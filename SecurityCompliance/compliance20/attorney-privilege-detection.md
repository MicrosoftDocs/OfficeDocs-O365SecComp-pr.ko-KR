---
title: 고급 eDiscovery에서 변호사 설정-클라이언트 권한 검색
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: ''
ROBOTS: NOINDEX, NOFOLLOW
description: ''
ms.openlocfilehash: 6838203a500a4fe600d8186a4b848beed0730665
ms.sourcegitcommit: 865b3dc071150b20bf3967e1263fc54e75898284
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/09/2019
ms.locfileid: "33835068"
---
# <a name="set-up-attorney-client-privilege-detection-preview-in-advanced-ediscovery"></a><span data-ttu-id="19b73-102">고급 eDiscovery에서 변호사 설정-클라이언트 권한 검색 (미리 보기)</span><span class="sxs-lookup"><span data-stu-id="19b73-102">Set up attorney-client privilege detection (preview) in Advanced eDiscovery</span></span>

<span data-ttu-id="19b73-103">검색 프로세스 중 검토 부분의 주요 및 비용이 높은 측면은 권한 있는 콘텐츠를 검토 하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="19b73-103">A major and costly aspect of the review portion of any discovery process is reviewing for privileged content.</span></span> <span data-ttu-id="19b73-104">고급 eDiscovery는이 프로세스를 보다 효율적으로 수행할 수 있도록 사용자의 경우에 따라 권한 있는 콘텐츠를 AI 기반으로 감지 합니다.</span><span class="sxs-lookup"><span data-stu-id="19b73-104">Advanced eDiscovery provides an AI-based detection of privileged content in your case so that you can make this process more efficient.</span></span> <span data-ttu-id="19b73-105">현재이 기능이 베타에 있으므로 eDiscovery 관리자는이 기능을 사용 하도록 선택 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="19b73-105">As this feature is currently in beta, an eDiscovery Administrator has to opt into the feature to use it.</span></span>

## <a name="how-does-it-work"></a><span data-ttu-id="19b73-106">작동 방식</span><span class="sxs-lookup"><span data-stu-id="19b73-106">How does it work?</span></span>

<span data-ttu-id="19b73-107">기능을 설정 하 고 사례 내에서 검토 집합을 분석할 때 모든 문서가 변호사-클라이언트 권한 검색 모델을 통해 실행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="19b73-107">With the feature turned on, when you analyze a review set within a case, all documents run through the attorney-client privilege detection model.</span></span> <span data-ttu-id="19b73-108">모델은 다음 두 가지를 보여 주는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="19b73-108">The model looks at two things:</span></span>

- <span data-ttu-id="19b73-109">콘텐츠: ML 모델은 본질적으로 문서 콘텐츠가 법적 지 여부를 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="19b73-109">Content: the ML model determines the likelihood of the document's content being legal in nature.</span></span>

- <span data-ttu-id="19b73-110">참가자: 테 넌 트에 대해 사용자가 업로드 한 변호사가 있는 경우이 모델은 문서의 참석자와 목록을 비교 하 여 문서에 변호사 참가자가 한 명 이상 있는지를 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="19b73-110">Participants: if there is a user-uploaded list of attorneys for the tenant, the model compares the participants of the document against the list to determine whether the document has at least one attorney participant.</span></span>
<span data-ttu-id="19b73-111">모델은 모든 문서에 대해 세 개의 값을 출력 하며, 검토 집합 내에서는 모두 검색 됩니다.</span><span class="sxs-lookup"><span data-stu-id="19b73-111">The model outputs three values for every document, all of which will be searchable within a review set:</span></span>

- <span data-ttu-id="19b73-112">콘텐츠 점수: 문서에서 법적 법률을 사용할 가능성 (점수 범위는 0 ~ 1)입니다.</span><span class="sxs-lookup"><span data-stu-id="19b73-112">Content score: the likelihood of the document being legal in nature (score between 0 and 1)</span></span>

- <span data-ttu-id="19b73-113">변호사: 참여자 중 하나가 업로드 된 변호사 목록에 있으면 True이 고, 그렇지 않으면, 또는 변호사 목록이 없는 경우에 해당 합니다.</span><span class="sxs-lookup"><span data-stu-id="19b73-113">Has Attorney: True if one of the participants is found in the uploaded attorney list, false otherwise, or if there is no attorney list.</span></span>

-  <span data-ttu-id="19b73-114">잠재적으로 권한이 있음: 콘텐츠 점수가 임계값을 초과 하거나 변호사 참가자가 있는 경우 True이 고 그렇지 않으면 false입니다.</span><span class="sxs-lookup"><span data-stu-id="19b73-114">Potentially Privileged: True if content score is above threshold or has an attorney participant, false otherwise.</span></span>

## <a name="opting-into-attorney-client-privilege-detection"></a><span data-ttu-id="19b73-115">변호사에 게 클라이언트 권한 감지</span><span class="sxs-lookup"><span data-stu-id="19b73-115">Opting into Attorney-client privilege detection</span></span>

### <a name="step-1-opt-into-attorney-client-privilege-detection-ediscovery-admin"></a><span data-ttu-id="19b73-116">1 단계: 변호사에 게 옵트인-클라이언트 권한 감지 (eDiscovery 관리자)</span><span class="sxs-lookup"><span data-stu-id="19b73-116">Step 1: Opt into Attorney-client privilege detection (eDiscovery Admin)</span></span>

<span data-ttu-id="19b73-117">변호사-클라이언트 권한 검색이 미리 보기 기능 이므로 eDiscovery 관리자는 해당 상황에서 기능을 사용할 수 있도록 설정 하기 위해 옵트인 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="19b73-117">Because Attorney-client privilege detection is a preview feature, your eDiscovery Administrator needs to opt in to make the feature available in your cases.</span></span>

- <span data-ttu-id="19b73-118">Advanced eDiscovery 페이지에서 "실험적 기능 구성"으로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="19b73-118">Go to "Configure experimental features" from Advanced eDiscovery page</span></span>

- <span data-ttu-id="19b73-119">"변호사 관리-클라이언트 권한 검색"을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="19b73-119">Click on "Manage Attorney-Client Privilege detection".</span></span>

- <span data-ttu-id="19b73-120">기능을 설정 하려면 설정/해제를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="19b73-120">Click on the toggle to turn the feature on.</span></span>

### <a name="step-2-upload-a-list-of-attorneys-optional"></a><span data-ttu-id="19b73-121">2 단계: 변호사 목록 업로드 (선택 사항)</span><span class="sxs-lookup"><span data-stu-id="19b73-121">Step 2: Upload a list of attorneys (optional)</span></span>

<span data-ttu-id="19b73-122">변호사를 최대한 활용 하기 위해 회사에 대 한 작업을 수행 하는 전자 메일 주소 변호사 또는 법적 가상 사용자 목록을 제공 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="19b73-122">In order to take full advantage of attorney-client privilege detection we recommend providing a list of email addresses lawyers or legal personas who work for the company.</span></span> <span data-ttu-id="19b73-123">목록은 헤더-less CSV 이며 줄당 한 개의 전자 메일 주소를 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="19b73-123">The list should be a header-less CSV, with one email address per line.</span></span>

## <a name="leveraging-attorney-client-privilege-detection"></a><span data-ttu-id="19b73-124">변호사를 활용 하 여 클라이언트 권한 검색</span><span class="sxs-lookup"><span data-stu-id="19b73-124">Leveraging attorney-client privilege detection</span></span> 

### <a name="step-1-analyze-a-review-set"></a><span data-ttu-id="19b73-125">1 단계: 검토 집합 분석</span><span class="sxs-lookup"><span data-stu-id="19b73-125">Step 1: Analyze a review set</span></span>

<span data-ttu-id="19b73-126">검토 집합을 분석할 때 변호사 클라이언트 권한 감지도 함께 실행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="19b73-126">When you analyze your review set, attorney-client privilege detection will be run as well.</span></span> <span data-ttu-id="19b73-127">검토 집합의 데이터 분석에 대 한 자세한 내용은 [Advanced eDiscovery의 검토 집합에서 데이터 분석](analyzing-data-in-review-set.md)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="19b73-127">To learn more about analyzing data in review set, please refer to [Analyze data in a review set in Advanced eDiscovery](analyzing-data-in-review-set.md).</span></span>

### <a name="step-2-create-a-smart-tag-group-with-attorney-client-privilege-detection-model"></a><span data-ttu-id="19b73-128">2 단계: 변호사 클라이언트 권한 검색 모델을 사용 하 여 스마트 태그 그룹 만들기</span><span class="sxs-lookup"><span data-stu-id="19b73-128">Step 2: Create a smart tag group with attorney-client privilege detection model</span></span>

<span data-ttu-id="19b73-129">검토 프로세스에서 변호사 클라이언트 권한 검색 결과를 사용할 수 있는 주요 방법 중 하나는 스마트 태그 그룹을 사용 하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="19b73-129">One of the main ways you can consume the results of attorney-client privilege detection in your review process is by using a smart tag group.</span></span> <span data-ttu-id="19b73-130">스마트 태그 그룹은 ML 모델의 결과를 작성 하 고 태그 옆에 있는 인라인 모델의 결과를 표시 하 여 관련 된 모델의 결과를 쉽게 사용할 수 있도록 하 고, 태그 패널의 다른 태그와 마찬가지로 검토 프로세스의 태그를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="19b73-130">Smart tag groups take the results of an ML model and show the results of the model in-line next to the tags, so that you can easily consume the results of the model where relevant, and use the tags in your review process as you would any other tags in your tagging panel.</span></span>

- <span data-ttu-id="19b73-131">"태그 관리"에서 "스마트 태그 섹션 추가"를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="19b73-131">In "Manage tags", click on "Add smart tag section".</span></span>

- <span data-ttu-id="19b73-132">"변호사-클라이언트 권한 검색"을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="19b73-132">Select "Attorney-client privilege detection".</span></span> <span data-ttu-id="19b73-133">모델의 가능한 결과에 해당 하는 태그 그룹 및 두 개의 태그가 생성 된 것을 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="19b73-133">You will see that a tag group and two tags, corresponding to the possible results of the model, have been created.</span></span>

- <span data-ttu-id="19b73-134">검토에 맞게 표시 되는 대로 태그 그룹 및 태그의 이름을 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="19b73-134">Rename the tag group and tags as you see fit for your review.</span></span>

### <a name="step-3-use-the-smart-tag-group-for-privilege-review"></a><span data-ttu-id="19b73-135">3 단계: 권한 검토를 위해 스마트 태그 그룹 사용</span><span class="sxs-lookup"><span data-stu-id="19b73-135">Step 3: Use the smart tag group for privilege review</span></span>

<span data-ttu-id="19b73-136">문서를 검토할 때 모델이 문서에 잠재적으로 권한이 있는 것으로 확인 되 면 해당 스마트 태그가 결과를 노출 합니다.</span><span class="sxs-lookup"><span data-stu-id="19b73-136">When you review a document, if the model has determined that the document is potentially privileged, the corresponding smart tag will expose the result:</span></span>

- <span data-ttu-id="19b73-137">문서에 포함 된 콘텐츠가 합법적 이면 해당 스마트 태그 옆에 "법적 내용" 이라는 레이블이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="19b73-137">If the document has content that may be legal in nature, a "Legal content" label will appear next to the corresponding smart tag.</span></span>

- <span data-ttu-id="19b73-138">문서의 참가자가 업로드 된 변호사 목록에 있는 경우 해당 스마트 태그 옆에 "변호사" 레이블이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="19b73-138">If the document has a participant that is found in the uploaded attorney list, an "Attorney" label will appear next to the corresponding smart tag.</span></span>