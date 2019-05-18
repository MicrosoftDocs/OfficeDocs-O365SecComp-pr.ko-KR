---
title: 검색 및 분석 설정 구성
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
ms.openlocfilehash: 0456ee21087c7fe05c3ef96d517feb468c7cfe5e
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/17/2019
ms.locfileid: "34151000"
---
# <a name="configure-search-and-analytics-settings"></a><span data-ttu-id="2daca-102">검색 및 분석 설정 구성</span><span class="sxs-lookup"><span data-stu-id="2daca-102">Configure search and analytics settings</span></span>

## <a name="near-duplicates-and-email-threading"></a><span data-ttu-id="2daca-103">유사 중복 및 전자 메일 스레딩</span><span class="sxs-lookup"><span data-stu-id="2daca-103">Near duplicates and email threading</span></span>

<span data-ttu-id="2daca-104">이 섹션에서는 중복 검색, 중복 검색 및 전자 메일 스레딩에 대 한 매개 변수를 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2daca-104">In this section, you can set parameters for duplicate detection, near duplicate detection, and email threading.</span></span>

- <span data-ttu-id="2daca-105">사용/사용 안 함: 사용 하도록 설정 된 경우 중복 검색, 근접 중복 검색 및 전자 메일 스레딩을 분석 흐름의 일부로 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="2daca-105">Enable/disable: include duplicate detection, near duplicate detection, and email threading as part of analytics flow if enabled.</span></span> <span data-ttu-id="2daca-106">두 사용자는 서로의 상위에 구축 되므로 모든 기능을 사용 하거나 사용 하지 않도록 설정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="2daca-106">Because they build on top of each other, you must enable all of them or disable all of them.</span></span>

- <span data-ttu-id="2daca-107">임계값: 두 문서의 유사성 수준이 임계값을 초과 하는 경우 동일한 비슷한 중복 집합에 배치 됩니다.</span><span class="sxs-lookup"><span data-stu-id="2daca-107">Threshold: if the similarity level of two documents are above the threshold, they will be put in the same near duplicate set.</span></span>

- <span data-ttu-id="2daca-108">기본적으로 중복 항목 숨기기:이 설정이 설정 되어 있으면 중복 문서를 숨기는 필터가 기본적으로 작업 집합에 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="2daca-108">Hide duplicates by default: if this setting is on, a filter to hide duplicate documents will be applied in the working set by default.</span></span> <span data-ttu-id="2daca-109">필요한 경우 작업 집합에서 필터를 수동으로 제거할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2daca-109">The filter can be removed manually in the working set if necessary.</span></span>

- <span data-ttu-id="2daca-110">최소/최대 단어 수: 중복 및 전자 메일 스레딩은 최소 단어 수와 최대 단어 수를 포함 하는 문서에 대해서만 실행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="2daca-110">Minimum/maximum number of words: near duplicates and email threading will run only on documents that have at least the minimum number of words and at most the maximum number of words.</span></span>
<span data-ttu-id="2daca-111">자세한 내용은 [Near 중복 검색](near-duplicates.md) 및 [전자 메일 스레딩](email-threading.md)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="2daca-111">For more information, see [Near duplicate detection](near-duplicates.md) and [Email threading](email-threading.md).</span></span>

## <a name="themes"></a><span data-ttu-id="2daca-112">테마</span><span class="sxs-lookup"><span data-stu-id="2daca-112">Themes</span></span>

<span data-ttu-id="2daca-113">이 섹션에서는 테마에 대 한 매개 변수를 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2daca-113">In this section, you can set parameters for themes.</span></span>

- <span data-ttu-id="2daca-114">Enable/disable: 사용 하도록 설정 된 경우 분석 흐름의 일부로 테마 클러스터링을 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="2daca-114">Enable/disable: include themes clustering as part of analytics flow if enabled.</span></span>
- <span data-ttu-id="2daca-115">동적으로 동적으로 테마 수 조정: 필요한 수의 테마를 만들 수 있는 문서가 충분 하지 않은 경우도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2daca-115">Adjust maximum number of themes dynamically dynamically: in certain cases, there are not enough documents to produce the desired number of themes.</span></span> <span data-ttu-id="2daca-116">이 설정을 사용 하도록 설정 하는 경우 원하는 최대 테마 수를 강제 실행 하는 것이 아니라 시스템에서 최대 테마 수를 동적으로 조정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2daca-116">If this setting is turned on, then rather than trying to force the desired maximum number of themes, the system adjusts maximum number of themes dynamically.</span></span>
- <span data-ttu-id="2daca-117">최대 테마 수: 원하는 테마 수</span><span class="sxs-lookup"><span data-stu-id="2daca-117">Maximum number of themes: desired number of themes</span></span>
- <span data-ttu-id="2daca-118">테마에 번호 포함: 사용 하도록 설정 하는 경우 테마를 생성할 때 숫자가 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="2daca-118">Include numbers in themes: When enabled, it will include numbers in when generating themes.</span></span>  

## <a name="optical-character-recognition-ocr"></a><span data-ttu-id="2daca-119">OCR (광학 문자 인식)</span><span class="sxs-lookup"><span data-stu-id="2daca-119">Optical character recognition (OCR)</span></span>

<span data-ttu-id="2daca-120">이 설정을 사용 하도록 설정 하면 작업 집합으로 ingested는 이미지에서 OCR이 실행 되어 검색이 가능 하 게 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2daca-120">When this setting is turned on, OCR will be run on images that are ingested into working sets so that they can be searchable.</span></span>

## <a name="ignore-text"></a><span data-ttu-id="2daca-121">텍스트 무시</span><span class="sxs-lookup"><span data-stu-id="2daca-121">Ignore text</span></span>

<span data-ttu-id="2daca-122">특정 텍스트에는 전자 메일 내용에 관계 없이 특정 전자 메일에 추가 되는 긴 고 지 사항 등의 분석 품질이 감소 하는 경우가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2daca-122">There are instances where certain texts will diminish the quality of analytics, such as lengthy disclaimers that get added to certain emails regardless of the content of the email.</span></span> <span data-ttu-id="2daca-123">이러한 경우를 알고 있는 경우 텍스트 (RegEx가 지원 됨)와 텍스트를 제외 해야 하는 모듈을 지정 하 여 분석에서이 텍스트를 제외할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2daca-123">If you are aware of such cases, you can exclude this text from analytics by specifying the text (RegEx is supported) and which modules that text should be excluded for.</span></span>