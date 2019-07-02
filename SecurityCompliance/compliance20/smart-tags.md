---
title: 고급 eDiscovery에서 스마트 태그 설정
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
description: 스마트 태그를 사용 하면 고급 eDiscovery 사례에서 콘텐츠를 검토할 때 기계 학습 기능을 적용할 수 있습니다. 스마트 태그 그룹을 사용 하 여 변호사-클라이언트 권한 모델과 같은 기계 학습 검색 모델의 결과를 표시 합니다.
ms.openlocfilehash: 68b558cc2282cc388387f8d61825b9ee569ff32a
ms.sourcegitcommit: e323610df2df71c84f536e8a38650d33d8069e41
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/04/2019
ms.locfileid: "34703831"
---
# <a name="set-up-smart-tags-in-advanced-ediscovery"></a><span data-ttu-id="b4aa9-104">고급 eDiscovery에서 스마트 태그 설정</span><span class="sxs-lookup"><span data-stu-id="b4aa9-104">Set up smart tags in Advanced eDiscovery</span></span>

<span data-ttu-id="b4aa9-105">고급 eDiscovery의 ML (기계 학습) 기능은 검토 집합에서 사례 문서를 검토할 때 보다 효율적으로 결정 프로세스를 만드는 데 도움이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b4aa9-105">Machine learning (ML) capabilities in Advanced eDiscovery can help you make the decision process more efficient when reviewing case documents in a review set.</span></span> <span data-ttu-id="b4aa9-106">스마트 태그는 검토 중에 문서에 태그를 지정할 때 결정 내용이 기록 되는 위치에 대 한 ML 기능을 가져오는 방법입니다.</span><span class="sxs-lookup"><span data-stu-id="b4aa9-106">Smart tags are a way to bring the ML capabilities to where the decisions are recorded: when tagging documents during review.</span></span> <span data-ttu-id="b4aa9-107">스마트 태그 그룹을 만들 때 스마트 태그 그룹과 연결 된 ML 모델의 결과가 태그 그룹의 태그와 함께 줄에 표시 되는 결정 사항을 결정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b4aa9-107">When you create a smart tag group, then the decisions that are the result of the ML model that you've associated with the smart tag group are displayed in-line with the tags in the tag group.</span></span> <span data-ttu-id="b4aa9-108">이렇게 하면 특정 문서를 검토할 때 행에서 ML 결과 정보를 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b4aa9-108">This helps see the ML results information in-line when you're reviewing specific documents.</span></span>

## <a name="how-to-set-up-a-smart-tag-group"></a><span data-ttu-id="b4aa9-109">스마트 태그 그룹을 설정 하는 방법</span><span class="sxs-lookup"><span data-stu-id="b4aa9-109">How to set up a smart tag group</span></span>

1. <span data-ttu-id="b4aa9-110">검토 집합에서 **검토 설정 관리** 를 클릭 한 다음 **태그 관리**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4aa9-110">In a review set, click **Manage review set** and then click **Manage tags**.</span></span>

2. <span data-ttu-id="b4aa9-111">**태그 그룹 추가** 를 클릭 한 다음 **스마트 태그 그룹 추가**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4aa9-111">Click **Add tag group** and then select **Add smart tag group**.</span></span>

3. <span data-ttu-id="b4aa9-112">태그 그룹에 연결 하려는 ML 모델을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4aa9-112">Select the ML model that you want to associate to the tag group.</span></span>
    
   <span data-ttu-id="b4aa9-113">이렇게 하면 태그 그룹 및 *n* 개의 하위 태그가 생성 되며 여기에서 *n* 은 모델의 가능한 출력 수입니다.</span><span class="sxs-lookup"><span data-stu-id="b4aa9-113">This creates a tag group and *N* child tags, where *N* is the number of possible outputs of the model.</span></span> <span data-ttu-id="b4aa9-114">예를 들어, [변호사-클라이언트 권한 검색 모델](attorney-privilege-detection.md) 에는 다음과 같은 두 가지 가능한 출력이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b4aa9-114">For example, the [attorney-client privilege detection model](attorney-privilege-detection.md) has two possible outputs:</span></span> 

   - <span data-ttu-id="b4aa9-115">**긍정** -변호사 클라이언트의 권한 있는 콘텐츠가 포함 된 문서에 태그를 추가할 때 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4aa9-115">**Positive** – Use to tag documents that contain attorney-client privileged content.</span></span>
   
   - <span data-ttu-id="b4aa9-116">**음수** -변호사 클라이언트의 권한 있는 콘텐츠가 포함 되지 않은 문서에 태그를 표시 하는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b4aa9-116">**Negative** – Use to tag documents that don't contain attorney-client privileged content.</span></span>
    
    <span data-ttu-id="b4aa9-117">이 모델을 선택 하면 검토 집합에 대해 하위 태그가 두 개 있는 태그 그룹 ( **양수** 와 이름이 각각 **음수**라는 하위 태그)이 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="b4aa9-117">If you select this model, a tag group with two child tags is created (one child tag named **Positive** and the other named **Negative**) for the review set.</span></span> <span data-ttu-id="b4aa9-118">이 예에서 각 하위 태그는 변호사 클라이언트 권한 검색 모델의 가능한 출력 중 하나에 해당 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4aa9-118">In this example, each child tag corresponds to one of the possible outputs from the attorney-client privilege detection model.</span></span>

4. <span data-ttu-id="b4aa9-119">원하는 경우 태그 그룹 및 자식 태그의 이름을 바꿀 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b4aa9-119">Optionally, you can rename the tag group and the child tags.</span></span> <span data-ttu-id="b4aa9-120">예를 들어 **양수** 태그의 이름을 **특권** 으로 바꾸고 **음수** 태그를 **권한이 없는**이름으로 바꿀 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b4aa9-120">For example, you could rename the **Positive** tag to **Privileged** and the **Negative** tag to **Not privileged**.</span></span>

## <a name="how-to-use-smart-tags"></a><span data-ttu-id="b4aa9-121">스마트 태그 사용 방법</span><span class="sxs-lookup"><span data-stu-id="b4aa9-121">How to use smart tags</span></span>

<span data-ttu-id="b4aa9-122">문서를 검토 하면 해당 자식 태그 옆에 모델의 결과가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b4aa9-122">When reviewing a document, the model's results are displayed next to the appropriate child tag.</span></span> <span data-ttu-id="b4aa9-123">예를 들어 변호사-클라이언트 권한 검색을 위한 스마트 태그 그룹이 있고 잠재적으로 권한이 부여 된 문서를 검토 하는 경우 해당 결론에 대 한 이유가 해당 태그 옆에 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b4aa9-123">For example, if you have a smart tag group for attorney-client privilege detection and you review a document that is potentially privileged, the reason for that conclusion is displayed next to the appropriate tag.</span></span> <span data-ttu-id="b4aa9-124">태그가 문서에 자동으로 적용 되지 않는다는 점에 유의 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4aa9-124">It's important to note that the tag isn't automatically applied to the document.</span></span> <span data-ttu-id="b4aa9-125">검토자가 문서에 태그를 설정 하는 방법을 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4aa9-125">The reviewer makes the decision about how to tag the document.</span></span>