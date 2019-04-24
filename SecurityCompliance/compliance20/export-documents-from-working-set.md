---
title: 작업 집합에서 문서 내보내기
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
ms.openlocfilehash: 815b92b13ed09d8aec64f5207f1c82d910e2dce0
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32252054"
---
# <a name="export-documents-from-a-working-set"></a><span data-ttu-id="7ef74-102">작업 집합에서 문서 내보내기</span><span class="sxs-lookup"><span data-stu-id="7ef74-102">Export documents from a working set</span></span>

<span data-ttu-id="7ef74-103">다음과 같은 세 가지 방법을 통해 작업 집합에서 콘텐츠를 내보낼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7ef74-103">Exporting content from a working set can be accomplished via 3 different methods:</span></span>

## <a name="download"></a><span data-ttu-id="7ef74-104">다운로드</span><span class="sxs-lookup"><span data-stu-id="7ef74-104">Download</span></span>

<span data-ttu-id="7ef74-105">다운로드에서는 작업 집합에서 콘텐츠를 기본 형식으로 다운로드 하는 간단한 방법을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="7ef74-105">Download offers a simple way to download content from a working set in Native format.</span></span> <span data-ttu-id="7ef74-106">다운로드 준비가 완료 되 면 브라우저 음성 안내가 표시 되도록 브라우저의 데이터 전송 기능을 활용 합니다.</span><span class="sxs-lookup"><span data-stu-id="7ef74-106">It leverages the browser’s data transfer features so a browser prompt will appear once a download is ready.</span></span> <span data-ttu-id="7ef74-107">이 방법을 사용 하 여 다운로드 한 파일은 컨테이너 파일로 압축 되 고 항목 수준 파일이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7ef74-107">Files downloaded using this method will be zipped into a container file and will be item level files.</span></span> <span data-ttu-id="7ef74-108">즉, 첨부 파일을 선택 하면 첨부 파일이 포함 된 전자 메일이 자동으로 수신 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7ef74-108">This means that if you select an attachment, you will automatically receive the email with the attachment included.</span></span> <span data-ttu-id="7ef74-109">마찬가지로 word 문서에 포함 된 excel 스프레드시트를 선택 하면 excel 스프레드시트가 포함 된 word 문서를 받게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7ef74-109">Similarly, if you select an excel spreadsheet that was embedded in a word document, you will receive the word document with the excel spreadsheet embedded.</span></span> <span data-ttu-id="7ef74-110">다운로드 한 항목은 파일 속성으로 표시 될 수 있는 마지막으로 수정한 날짜를 보존 합니다.</span><span class="sxs-lookup"><span data-stu-id="7ef74-110">Downloaded items will preserve the last modified date which can be viewed as a file property.</span></span>

<span data-ttu-id="7ef74-111">작업 집합에서 콘텐츠를 다운로드 하려면 먼저 다운로드 하려는 파일을 선택 하 고 작업 메뉴에서 "다운로드"를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="7ef74-111">To download content from a working set, start by selecting the files you want to download then select “Download” under the Actions menu.</span></span>

![자동으로 생성 되는 컴퓨터 설명 스크린샷](../media/eDiscoDownload.png)

## <a name="export"></a><span data-ttu-id="7ef74-113">내보내기</span><span class="sxs-lookup"><span data-stu-id="7ef74-113">Export</span></span>

<span data-ttu-id="7ef74-114">내보내기를 사용 하면 다운로드 패키지에 포함 된 콘텐츠를 사용자 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7ef74-114">Export allows users to customize the content that is included in the download package.</span></span> <span data-ttu-id="7ef74-115">다음 설정을 사용 하 여 구성 페이지를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="7ef74-115">It provides a configuration page with the following settings:</span></span>

### <a name="metadata-file"></a><span data-ttu-id="7ef74-116">메타 데이터 파일</span><span class="sxs-lookup"><span data-stu-id="7ef74-116">Metadata file</span></span>

> <span data-ttu-id="7ef74-117">내보낸 파일에 연결 된 메타 데이터를 포함 하는 "로드 파일"으로 간주 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7ef74-117">This can be considered your “load file” that contains metadata associated with the files you exported.</span></span> <span data-ttu-id="7ef74-118">메타 데이터 파일에서 사용할 수 있는 필드 목록은 link \[\]를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="7ef74-118">For a list of fields available in the metadata file, see \[link\].</span></span> <span data-ttu-id="7ef74-119">이 파일은 일반적으로 3 개<sup>rd</sup> 파티 도구 ingested 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7ef74-119">This file can typically be ingested by 3<sup>rd</sup> party tools downstream.</span></span>

### <a name="tag-data"></a><span data-ttu-id="7ef74-120">태그 데이터</span><span class="sxs-lookup"><span data-stu-id="7ef74-120">Tag data</span></span>

> <span data-ttu-id="7ef74-121">이 콘텐츠는 메타 데이터 파일에서 필드로 추가 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7ef74-121">This content would be added as fields in the metadata file.</span></span> <span data-ttu-id="7ef74-122">여기에는 작업 집합에 적용 된 태그 정보가 모두 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7ef74-122">It contains all of the tag information applied in working sets.</span></span>

### <a name="text-files"></a><span data-ttu-id="7ef74-123">텍스트 파일</span><span class="sxs-lookup"><span data-stu-id="7ef74-123">Text files</span></span>

> <span data-ttu-id="7ef74-124">작업 집합에서 내보낸 각 파일에 대해 텍스트 파일을 생성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7ef74-124">Text files can be generated for each file exported from a working set.</span></span> <span data-ttu-id="7ef74-125">ingesting 데이터의 일부로 서비스 파트너가 이러한 파일을 3 개의<sup>rd</sup> 파티 도구 다운스트림으로 필요로 하는 경우가 종종 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7ef74-125">Often times these files are required by service partners as part of ingesting data into 3<sup>rd</sup> party tools downstream.</span></span>

### <a name="redacted-files"></a><span data-ttu-id="7ef74-126">Redacted 파일</span><span class="sxs-lookup"><span data-stu-id="7ef74-126">Redacted files</span></span>

> <span data-ttu-id="7ef74-127">검토 중에 redacted pdf가 생성 되 면 내보내는 동안 이러한 파일을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7ef74-127">If redacted PDFs are generated during review, these files are available during export.</span></span> <span data-ttu-id="7ef74-128">사용자는 기본 파일만 내보낼지 아니면 redactions가 포함 된 natives를 pdf에서 구운 것으로 바꿀지를 결정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7ef74-128">Users can decide whether to export native files only or to replace natives that have redactions with the burned in PDFs.</span></span>

### <a name="export-location"></a><span data-ttu-id="7ef74-129">내보내기 위치</span><span class="sxs-lookup"><span data-stu-id="7ef74-129">Export Location</span></span>

> <span data-ttu-id="7ef74-130">내보낸 콘텐츠가 Microsoft에서 제공한 Azure blob로 배달 되거나, 내보내기에서 세부 정보를 제공 하는 경우 고객의 blob를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7ef74-130">Exported content is delivered to either a Microsoft provided Azure blob or a customer’s blob can be used if the details are provided at export.</span></span>

## <a name="export-structure"></a><span data-ttu-id="7ef74-131">내보내기 구조</span><span class="sxs-lookup"><span data-stu-id="7ef74-131">Export Structure</span></span>

<span data-ttu-id="7ef74-132">콘텐츠를 작업 집합에서 내보내는 경우 콘텐츠는 다음 구조로 구성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7ef74-132">When content is exported from a working set, the content is organized in the following structure.</span></span>

  - <span data-ttu-id="7ef74-133">루트 폴더-다운로드 ID</span><span class="sxs-lookup"><span data-stu-id="7ef74-133">Root folder – Download ID</span></span>
    
      - <span data-ttu-id="7ef74-134">로드\_\_파일 .csv = 메타 데이터 파일 내보내기</span><span class="sxs-lookup"><span data-stu-id="7ef74-134">Export\_load\_file.csv = metadata file</span></span>
    
      - <span data-ttu-id="7ef74-135">요약 .txt = 내보내기 통계가 포함 된 요약 파일</span><span class="sxs-lookup"><span data-stu-id="7ef74-135">Summary.txt = a summary file with export statistics</span></span>
    
      - <span data-ttu-id="7ef74-136">입력\_또는 네이티브\_파일 = 모든 네이티브 파일 포함</span><span class="sxs-lookup"><span data-stu-id="7ef74-136">Input\_or native\_files = contains all native files</span></span>
    
      - <span data-ttu-id="7ef74-137">오류\_파일 = 내보내기에 포함 된 오류 파일을 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="7ef74-137">Error\_files = contains any error files included in the export</span></span>
        
          - <span data-ttu-id="7ef74-138">extractionerror-상위 파일에서 제대로 추출 되지 않은 파일의 사용 가능한 메타 데이터가 포함 된 csv입니다.</span><span class="sxs-lookup"><span data-stu-id="7ef74-138">ExtractionError – a csv that contains any available metadata of files that were not properly extracted from parent files</span></span>
        
          - <span data-ttu-id="7ef74-139">ProcessingError – 처리 오류가 발생 한 콘텐츠입니다.</span><span class="sxs-lookup"><span data-stu-id="7ef74-139">ProcessingError – content with processing errors.</span></span> <span data-ttu-id="7ef74-140">이 콘텐츠는 항목 수준 이므로 첨부 파일에 처리 오류가 발생 한 경우 첨부 파일이 포함 된 전자 메일이이 폴더에 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7ef74-140">This content is item level meaning if an attachment experienced a processing error, the email that contains the attachment will be included in this folder.</span></span>
    
      - <span data-ttu-id="7ef74-141">추출\_된\_텍스트 파일 = 처리 시 생성 되는 모든 추출한 텍스트 파일을 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="7ef74-141">Extracted\_text\_files = contains all of the extracted text files generated at processing.</span></span>

## <a name="working-set"></a><span data-ttu-id="7ef74-142">Working Set</span><span class="sxs-lookup"><span data-stu-id="7ef74-142">Working Set</span></span>

<span data-ttu-id="7ef74-143">다른 작업 집합에 콘텐츠를 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7ef74-143">Content can be added to another working set.</span></span>