---
title: 검색 및 분석 설정 구성
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection: ''
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: ''
ms.openlocfilehash: d9528a4bcfaa77f2e232b25d03eda46cce42ebb9
ms.sourcegitcommit: ee28ee2b2bdfd049333c2f495d7f7780d13af4a6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2019
ms.locfileid: "29608129"
---
# <a name="configure-search-and-analytics-settings"></a><span data-ttu-id="e59d7-102">검색 및 분석 설정 구성</span><span class="sxs-lookup"><span data-stu-id="e59d7-102">Configure search and analytics settings</span></span>


## <a name="near-duplicates-and-email-threading"></a><span data-ttu-id="e59d7-103">중복 되는 값 및 전자 메일 스레딩 근처</span><span class="sxs-lookup"><span data-stu-id="e59d7-103">Near duplicates and email threading</span></span>

<span data-ttu-id="e59d7-104">이 섹션에서는 중복 검색 및 전자 메일 스레딩 근처 중복 검색에 대 한 매개 변수를 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e59d7-104">In this section, you can set parameters for duplicate detection, near duplicate detection, and email threading.</span></span>

- <span data-ttu-id="e59d7-p101">사용/사용 안함: 중복 항목 검색 및 전자 메일 사용 하는 경우에 분석 흐름의 일부로 스레딩 근처 중복 검색을 포함 합니다. 서로의 만드는 때문에 모두 사용 하도록 설정 하거나 모두를 사용 하지 않도록 설정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e59d7-p101">Enable/disable: include duplicate detection, near duplicate detection, and email threading as part of analytics flow if enabled. Because they build on top of each other, you must enable all of them or disable all of them.</span></span>

- <span data-ttu-id="e59d7-107">임계값: 두 문서의 다음과 비슷한 수준 임계값이 초과 된 경우 이러한은에 저장 됩니다 중복 집합 거의 동일 합니다.</span><span class="sxs-lookup"><span data-stu-id="e59d7-107">Threshold: if the similarity level of two documents are above the threshold, they will be put in the same near duplicate set.</span></span>

- <span data-ttu-id="e59d7-p102">기본적으로 중복 되는 값을 숨기기:이 설정은 켜져 경우 중복 된 문서를 숨기려면 필터 기본적으로 설정 하는 작업에 적용 됩니다. 필요한 경우 설정 작업에서 필터를 수동으로 제거할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e59d7-p102">Hide duplicates by default: if this setting is on, a filter to hide duplicate documents will be applied in the working set by default. The filter can be removed manually in the working set if necessary.</span></span>

- <span data-ttu-id="e59d7-p103">최소/최대 단어 수: 중복 항목 및 전자 메일 근처 단어의 최소 및 최대 단어의 최대 개수 이상의 있는 문서 에서만 실행 됩니다 스레딩 합니다. 자세한 내용은 [중복 검색 근처](near-duplicates.md) 및 [전자 메일 스레드](email-threading.md)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="e59d7-p103">Minimum/maximum number of words: near duplicates and email threading will run only on documents that have at least the minimum number of words and at most the maximum number of words. For more information, see [Near duplicate detection](near-duplicates.md) and [Email threading](email-threading.md).</span></span>

## <a name="themes"></a><span data-ttu-id="e59d7-112">테마</span><span class="sxs-lookup"><span data-stu-id="e59d7-112">Themes</span></span>

<span data-ttu-id="e59d7-113">이 섹션의 테마에 대 한 매개 변수를 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e59d7-113">In this section, you can set parameters for themes.</span></span>

- <span data-ttu-id="e59d7-114">사용/사용 안함: 테마를 사용 하는 경우에 분석 흐름의 일부로 클러스터링을 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="e59d7-114">Enable/disable: include themes clustering as part of analytics flow if enabled.</span></span>
- <span data-ttu-id="e59d7-p104">테마의 최대 수를 동적으로 동적으로 조정: 특정의 경우에서 없는 테마의 원하는 번호를 생성할 충분 한 문서입니다. 이 설정은 켜져 하는 경우 다음 테마, 원하는 최대 수를 강제 실행 하는 동안이 아닌 시스템 조정 하는 테마의 최대 수 동적으로 합니다.</span><span class="sxs-lookup"><span data-stu-id="e59d7-p104">Adjust maximum number of themes dynamically dynamically: in certain cases, there are not enough documents to produce the desired number of themes. If this setting is turned on, then rather than trying to force the desired maximum number of themes, the system adjusts maximum number of themes dynamically.</span></span>
- <span data-ttu-id="e59d7-117">테마의 최대 수: 필요한 테마 수</span><span class="sxs-lookup"><span data-stu-id="e59d7-117">Maximum number of themes: desired number of themes</span></span>
- <span data-ttu-id="e59d7-118">테마에 번호를 포함: 테마를 생성 하는 경우에 번호를 포함 됩니다이 옵션을 설정 하는 경우.</span><span class="sxs-lookup"><span data-stu-id="e59d7-118">Include numbers in themes: When enabled, it will include numbers in when generating themes.</span></span>  

## <a name="optical-character-recognition-ocr"></a><span data-ttu-id="e59d7-119">광학 문자 인식 (OCR)</span><span class="sxs-lookup"><span data-stu-id="e59d7-119">Optical character recognition (OCR)</span></span>

<span data-ttu-id="e59d7-120">이 설정은 켜져 OCR는 수집 된 작업 집합으로 검색할 수 있도록 하는 이미지에서 실행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e59d7-120">When this setting is turned on, OCR will be run on images that are ingested into working sets so that they can be searchable.</span></span>

## <a name="ignore-text"></a><span data-ttu-id="e59d7-121">텍스트를 무시 합니다.</span><span class="sxs-lookup"><span data-stu-id="e59d7-121">Ignore text</span></span>

<span data-ttu-id="e59d7-p105">특정 텍스트는 감소 하는 분석, 전자 메일의 내용에 관계 없이 특정 전자 메일에 추가 하는 시간이 오래 걸리는 고 지 사항 등의 품질 인스턴스가 있습니다. 이러한 경우를 인식 하는 경우에서 제외할 수 있습니다이 텍스트 분석을 지정 하 여 텍스트 (RegEx 지원) 하는 모듈에 대 한 텍스트를 제외 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e59d7-p105">There are instances where certain texts will diminish the quality of analytics, such as lengthy disclaimers that get added to certain emails regardless of the content of the email. If you are aware of such cases, you can exclude this text from analytics by specifying the text (RegEx is supported) and which modules that text should be excluded for.</span></span>