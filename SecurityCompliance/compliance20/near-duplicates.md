---
title: 중복에 가까운 검색
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
description: ''
ms.openlocfilehash: 7ae5e695091d140089f979f28793876a2df77251
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/17/2019
ms.locfileid: "34151570"
---
# <a name="near-duplicate-detection"></a><span data-ttu-id="585d7-102">중복에 가까운 검색</span><span class="sxs-lookup"><span data-stu-id="585d7-102">Near duplicate detection</span></span>

<span data-ttu-id="585d7-103">하위 집합이 같은 서식 파일을 기반으로 하며, 여기에 몇 가지 차이가 있는 같은 상용구 언어를 사용 하는 검토할 문서 집합을 가정해 봅니다.</span><span class="sxs-lookup"><span data-stu-id="585d7-103">Consider a set of documents to be reviewed in which a subset is based on the same template and has mostly the same boilerplate language, with a few differences here and there.</span></span> <span data-ttu-id="585d7-104">검토자가이 하위 집합을 식별 하 고, 그 중 하나를 철저히 검토 하 고, 나머지에 대 한 차이를 검토 하 고, 모든 문서를 읽을 수 있는 시간만 차지 하는 동안에는 고유한 정보를 놓치지 않을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="585d7-104">If a reviewer could identify this subset, review one of them thoroughly, and review the differences for the rest, they would not have missed any unique information while taking only a fraction of time that would have taken them to read all documents cover to cover.</span></span> <span data-ttu-id="585d7-105">유사 중복 검색 그룹은 검토 프로세스의 효율성을 높이기 위해 비슷한 문서를 함께 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="585d7-105">Near duplicate detection groups textually similar documents together to help you make your review process more efficient.</span></span>

## <a name="how-does-it-work"></a><span data-ttu-id="585d7-106">작동 방식</span><span class="sxs-lookup"><span data-stu-id="585d7-106">How does it work?</span></span>

<span data-ttu-id="585d7-107">근접 중복 검색이 실행 되 면 시스템은 텍스트를 사용 하 여 모든 문서를 구문 분석 합니다.</span><span class="sxs-lookup"><span data-stu-id="585d7-107">When near duplicate detection is run, the system parses every document with text.</span></span> <span data-ttu-id="585d7-108">그런 다음 모든 문서를 서로 비교 하 여 유사도가 설정 된 임계값 보다 큰지 여부를 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="585d7-108">Then, it compares every document against each other to determine whether their similarity is greater than the set threshold.</span></span> <span data-ttu-id="585d7-109">이 경우 문서가 함께 그룹화 됩니다.</span><span class="sxs-lookup"><span data-stu-id="585d7-109">If it is, the documents are grouped together.</span></span> <span data-ttu-id="585d7-110">모든 문서를 비교 하 고 그룹화 한 후에는 각 그룹의 문서가 "피벗"으로 표시 됩니다. 문서를 검토할 때 검토 중인 피벗 및 문서 간의 차이에 초점을 맞추어, 먼저 피벗을 검토 하 고 동일한 근거리 복제 세트로 다른 문서를 검토할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="585d7-110">Once all documents have been compared and grouped, a document from each group is marked as the "pivot"; in reviewing your documents, you can review a pivot first and review the other documents in the same near duplicate set, focusing on the difference between the pivot and the document that is in review.</span></span>