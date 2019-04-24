---
title: 사례 닫기 또는 삭제
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
ms.openlocfilehash: 016b87388a17bc5cb01eb1a90d88aedb6e2e133c
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32243771"
---
# <a name="close-or-delete-a-case"></a><span data-ttu-id="60832-102">사례 닫기 또는 삭제</span><span class="sxs-lookup"><span data-stu-id="60832-102">Close or delete a case</span></span>

<span data-ttu-id="60832-103">eDiscovery 사례에서 지 원하는 법적 사례 또는 조사가 완료 되 면 사례를 닫을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="60832-103">When the legal case or investigation supported by an eDiscovery case is completed, you can close the case.</span></span> <span data-ttu-id="60832-104">사례를 닫을 때 수행 되는 작업은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="60832-104">Here's what happens when you close a case:</span></span>

- <span data-ttu-id="60832-105">대/소문자에 보류 중인 콘텐츠 위치가 포함 되어 있으면 해당 보류를 해제 합니다.</span><span class="sxs-lookup"><span data-stu-id="60832-105">If the case contains any content locations on hold, those holds will be turned off.</span></span> <span data-ttu-id="60832-106">이로 인해 사용자 또는 자동화 된 프로세스 (예: 삭제 정책)에 의해 콘텐츠가 영구적으로 삭제 되거나 제거 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="60832-106">This might result in content being permanently deleted or purged, either by the user or by an automated process, such as a deletion policy.</span></span>

- <span data-ttu-id="60832-107">사례를 닫으면 해당 사례와 연결 된 보류만 해제 됩니다.</span><span class="sxs-lookup"><span data-stu-id="60832-107">Closing a case only turns off the holds that are associated with that case.</span></span> <span data-ttu-id="60832-108">다른 보류가 콘텐츠 위치 (예: 소송 보존)에 배치 되는 경우</span><span class="sxs-lookup"><span data-stu-id="60832-108">If other holds are place on a content location (such as a Litigation Hold.</span></span> <span data-ttu-id="60832-109">보존 정책 또는 다른 eDiscovery 사례의 보류는 계속 유지 관리 됩니다.</span><span class="sxs-lookup"><span data-stu-id="60832-109">a Preservation Policy, or a hold from a different eDiscovery case) those holds will still be maintained.</span></span>

- <span data-ttu-id="60832-110">이 사례는 여전히 Security & 준수 센터의 eDiscovery 페이지에 나열 됩니다.</span><span class="sxs-lookup"><span data-stu-id="60832-110">The case is still listed on the eDiscovery page in the Security & Compliance Center.</span></span> <span data-ttu-id="60832-111">닫힌 사례에 대 한 세부 정보, 보류, 검색 및 구성원은 그대로 유지 됩니다.</span><span class="sxs-lookup"><span data-stu-id="60832-111">The details, holds, searches, and members of a closed case are retained.</span></span>

- <span data-ttu-id="60832-112">해당 사례가 닫힌 후에 대/소문자를 편집할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="60832-112">You can edit a case after it's closed.</span></span> <span data-ttu-id="60832-113">예를 들어 고급 eDiscovery에서 구성원을 추가 하거나 제거 하 고, 검색을 만들고, 검색 결과를 내보내고, 검색 결과를 준비할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="60832-113">For example, you can add or removing members, create searches, export search results, and prepare search result for analysis in Advanced eDiscovery.</span></span> <span data-ttu-id="60832-114">활성 사례와 닫힌 사례의 주요 차이점은 사례를 닫을 때 보류가 해제 된다는 점입니다.</span><span class="sxs-lookup"><span data-stu-id="60832-114">The primary difference between active and closed cases is that holds are turned off when a case is closed.</span></span>

<span data-ttu-id="60832-115">사례를 닫으려면:</span><span class="sxs-lookup"><span data-stu-id="60832-115">To close a case:</span></span>

1. <span data-ttu-id="60832-116">**고급 eDiscovery (미리 보기)** 페이지에서 해당 사례로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="60832-116">From the **Advanced eDiscovery (Preview)** page, go to your case.</span></span>

2. <span data-ttu-id="60832-117">**설정** 으로 이동 하 여 **사례 정보**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="60832-117">Go to **Settings** and select **Case Information**.</span></span> 

3. <span data-ttu-id="60832-118">**대/소문자 닫기를**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="60832-118">Click **Close Case**.</span></span> 

<span data-ttu-id="60832-119">사례를 삭제 하려면 다음을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="60832-119">To delete a case:</span></span>

1. <span data-ttu-id="60832-120">**고급 eDiscovery (미리 보기)** 페이지에서 해당 사례로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="60832-120">From the **Advanced eDiscovery (Preview)** page, go to your case.</span></span>

2. <span data-ttu-id="60832-121">**설정** 으로 이동 하 여 **사례 정보**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="60832-121">Go to **Settings** and select **Case Information**.</span></span> 

3. <span data-ttu-id="60832-122">**대/소문자 삭제**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="60832-122">Click **Delete Case**.</span></span> 
