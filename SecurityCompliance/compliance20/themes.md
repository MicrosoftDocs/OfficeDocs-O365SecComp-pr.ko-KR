---
title: 테마
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
description: ''
ms.openlocfilehash: 7c9d1a52acef48d96816fefbb1c836032d262b93
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32240980"
---
# <a name="themes"></a><span data-ttu-id="da782-102">테마</span><span class="sxs-lookup"><span data-stu-id="da782-102">Themes</span></span>
<span data-ttu-id="da782-103">사용자가 문서를 작성 하는 방법은 무엇 인가요?</span><span class="sxs-lookup"><span data-stu-id="da782-103">How does a person write a document?</span></span> <span data-ttu-id="da782-104">일반적으로 문서에서 전달 하려는 하나 이상의 아이디어를 시작 하 고 아이디어와 일치 하는 단어를 사용 하 여 작성 합니다.</span><span class="sxs-lookup"><span data-stu-id="da782-104">They generally start with one or more ideas they want to convey in the document, and compose using words that align with the ideas.</span></span> <span data-ttu-id="da782-105">가장 많이 알려진 개념은 해당 아이디어와 관련 된 단어의 빈도가 가장 많습니다.</span><span class="sxs-lookup"><span data-stu-id="da782-105">The more prevalent an idea is, the more frequent the words that are related to that idea tend to be.</span></span> <span data-ttu-id="da782-106">사용자가 문서를 사용 하는 방법에 대 한 정보가 들어 있습니다. 문서를 읽을 때 고려해 야 할 중요 한 사항은 문서에서 전달을 시도 하 고 있는 위치 및 아이디어 간의 관계와 관련 된 아이디어입니다.</span><span class="sxs-lookup"><span data-stu-id="da782-106">This informs how people consume documents as well; the important thing to get from reading a document is the ideas that the document is trying to convey, and which ideas appear where, and what the relationships between the ideas are.</span></span>

<span data-ttu-id="da782-107">이를 통해 사용자가 문서 집합을 사용 하는 방법으로 확장할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="da782-107">This can be extended to how a person wants to consume a set of documents.</span></span> <span data-ttu-id="da782-108">이러한 사용자는 집합에 있는 아이디어와 이러한 아이디어에 대해 어떤 문서를 말하고 있는지 확인 하고자 합니다.</span><span class="sxs-lookup"><span data-stu-id="da782-108">They want to see which ideas are present in the sets, and which documents are talking about those ideas.</span></span> <span data-ttu-id="da782-109">또한 관심 있는 특정 문서를 찾으면 비슷한 내용을 설명 하는 문서를 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="da782-109">Also, if they find a particular document of interest, they want to be able to see documents that discuss similar ideas.</span></span>

<span data-ttu-id="da782-110">Themes 모듈은 작업 집합에 설명 되어 있는 "테마"를 분석 하 고 문서에 할당 하 여 문서에 대 한 사용자의 이유를 모방 합니다.</span><span class="sxs-lookup"><span data-stu-id="da782-110">Themes module tries to mimic how humans reason about documents, by analyzing the "themes" that are discussed in a working set and assigning them to documents.</span></span> <span data-ttu-id="da782-111">테마는 한 단계 더 나아가 문서 별로 "주요 테마"로 식별 됩니다. 즉, 가장 많이 나타나는 테마</span><span class="sxs-lookup"><span data-stu-id="da782-111">Themes goes one step further and identifies per document the "dominant theme"; i.e. the theme that appears the most.</span></span>

## <a name="how-does-themes-work"></a><span data-ttu-id="da782-112">테마는 어떻게 작동 하나요?</span><span class="sxs-lookup"><span data-stu-id="da782-112">How does Themes work?</span></span>
<span data-ttu-id="da782-113">테마는 작업 집합의 텍스트로 문서를 분석 하 여 문서 전체에 표시 되는 일반 테마를 구문 분석 합니다.</span><span class="sxs-lookup"><span data-stu-id="da782-113">Themes analyzes documents with text in a working set to parse out common themes that appear accross the documents.</span></span> <span data-ttu-id="da782-114">그런 다음 해당 테마를 표시 되는 문서에 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="da782-114">Then, it assigns those themes to the documents in which they appear.</span></span> <span data-ttu-id="da782-115">또한 테마를 대표 하는 문서에 사용 되는 각 단어에 레이블을 붙입니다.</span><span class="sxs-lookup"><span data-stu-id="da782-115">It also labels each with words used in the documents that are representative of the theme.</span></span> <span data-ttu-id="da782-116">문서는 여러 주제에 대 한 정보 일 수 있으므로 대부분의 경우 문서에 둘 이상의 테마가 할당 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="da782-116">Since a document can be about more than one subject matter, in many cases a document has more than one themes assigned to it.</span></span> <span data-ttu-id="da782-117">문서에서 가장 두드러지게 표시 되는 테마는 기준 테마로 지정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="da782-117">The theme that appears most prominently in a document is designated as its dominant theme.</span></span>