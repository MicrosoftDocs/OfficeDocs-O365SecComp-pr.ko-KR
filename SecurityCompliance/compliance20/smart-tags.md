---
title: 고급 eDiscovery에서 변호사에 대 한 스마트 태그 설정-클라이언트 권한 검색
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
description: ''
ms.openlocfilehash: 5310acad1aa1bc2e01cbabee69dd7bb38084bd9a
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/17/2019
ms.locfileid: "34153970"
---
# <a name="set-up-smart-tags-for-ml-assisted-review-in-advanced-ediscovery"></a><span data-ttu-id="b81d1-102">고급 eDiscovery에서 ML 지원 검토를 위한 스마트 태그 설정</span><span class="sxs-lookup"><span data-stu-id="b81d1-102">Set up smart tags for ML-assisted review in Advanced eDiscovery</span></span>

<span data-ttu-id="b81d1-103">Advanced eDiscovery의 기계 학습 기능은 문서에 대 한 의사 결정 프로세스를 보다 효율적으로 수행 하는 데 도움이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b81d1-103">Machine learning capabilities in Advanced eDiscovery are meant to help make decision process on documents more efficient.</span></span> <span data-ttu-id="b81d1-104">스마트 태그는 결정 내용이 기록 되는 위치 (태그 및 태그 그룹)로 컴퓨터 학습 기능을 가져오는 방법입니다.</span><span class="sxs-lookup"><span data-stu-id="b81d1-104">Smart tags is a way to bring the machine learning capabilities into where the decisions are recorded: tags and tag groups.</span></span> <span data-ttu-id="b81d1-105">스마트 태그 그룹을 만들 때 그룹에 매핑된 ML 모델에 대 한 결정 내용은 그룹의 태그와 함께 줄에 표시 되며,이를 통해 온라인으로 컨텍스트 되는 정보를 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b81d1-105">When you create a smart tag group, then the decisions of the ML model mapped to the group will be shown in-line with the tags in the group to help you see the information in-line, where they contextually make most sense.</span></span>

## <a name="how-to-set-up-a-smart-tag-group"></a><span data-ttu-id="b81d1-106">스마트 태그 그룹을 설정 하는 방법</span><span class="sxs-lookup"><span data-stu-id="b81d1-106">How to set up a smart tag group</span></span>

1. <span data-ttu-id="b81d1-107">검토 집합에서 **검토 설정** -> 관리**태그**관리로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="b81d1-107">In a review set, go to **Manage review set** -> **Manage tags**.</span></span>

2. <span data-ttu-id="b81d1-108">**태그 그룹 추가** 옆에 있는 드롭다운을 클릭 하 고 **스마트 태그 그룹 추가**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="b81d1-108">Click on the drop-down next to **Add tag group** and select **Add smart tag group**.</span></span>

3. <span data-ttu-id="b81d1-109">이 그룹에 매핑할 모델을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="b81d1-109">Select the model you want to map to this group.</span></span> <span data-ttu-id="b81d1-110">이렇게 하면 태그 구역과 N 개의 하위 태그가 생성 되며 여기에서 N은 모델의 가능한 출력 수입니다.</span><span class="sxs-lookup"><span data-stu-id="b81d1-110">This will create a tag section and N child tags, where N is the number of possible outputs of the model.</span></span> <span data-ttu-id="b81d1-111">예를 들어, 변호사-클라이언트 권한 감지 모델에는 두 가지 가능한 출력이 있고 권한이 부여 되지 않음이 있습니다. 이 모델을 선택 하면 검토 집합에 두 개의 하위 태그가 생성 되며 각각 가능한 출력 중 하나에 해당 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b81d1-111">For instance, attorney-client privilege detection model has two possible outputs - privileged and not privileged; selecting this model will create two child tags in the review set, each corresponding to one of the possible outputs.</span></span>

4. <span data-ttu-id="b81d1-112">표시 되는 대로 태그 그룹 및 태그의 이름을 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="b81d1-112">Rename the tag group and tags as you see fit.</span></span>

## <a name="how-to-use-a-smart-tag-group"></a><span data-ttu-id="b81d1-113">스마트 태그 그룹을 사용 하는 방법</span><span class="sxs-lookup"><span data-stu-id="b81d1-113">How to use a smart tag group</span></span>

<span data-ttu-id="b81d1-114">문서를 검토할 때 모델의 결과가 해당 태그 값 옆에 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b81d1-114">When reviewing a document, the model's results will be exposed next to the appropriate tag value.</span></span> <span data-ttu-id="b81d1-115">예를 들어, 변호사-클라이언트 권한 검색을 위한 스마트 태그 그룹을 사용 하 고 모델이 결정 한 문서를 검토 하면 해당 태그 옆에 해당 하는 이유가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b81d1-115">For instance, if you have a smart tag group for attorney-client privilege detection and you review a document that the model has decided is potentially privileged, you will see the reason for that next to the appropriate tag.</span></span> <span data-ttu-id="b81d1-116">이 태그는 자동으로 적용 되지 않습니다. 모든 목적에 따라 스마트 태그 그룹 내의 태그는 적절 한 경우 모델 결과를 표시 하는 것을 제외 하 고는 일반 태그와 동일 하 게 작동 합니다.</span><span class="sxs-lookup"><span data-stu-id="b81d1-116">It is important to note that the tag is not automatically applied; for all intents and purposes, tags within a smart tag group act just like normal tags, except that they expose the model results next to them when appropriate.</span></span>