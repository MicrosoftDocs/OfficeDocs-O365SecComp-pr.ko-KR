---
title: 증거의 데이터 검토
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
ms.openlocfilehash: 279d2117a69e889f9e605e0ab211c03c5842a59d
ms.sourcegitcommit: 2c5834235c32b2616e1813ce24eeb3419a09629f
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/02/2019
ms.locfileid: "31030376"
---
# <a name="review-data-in-evidence"></a><span data-ttu-id="0644e-102">증거의 데이터 검토</span><span class="sxs-lookup"><span data-stu-id="0644e-102">Review data in evidence</span></span>

<span data-ttu-id="0644e-103">**증거** 는 수집한 검색 결과의 스냅숏입니다.</span><span class="sxs-lookup"><span data-stu-id="0644e-103">**Evidence** is a snapshot of search results that you collected.</span></span> <span data-ttu-id="0644e-104">검색 결과를 증거에 추가 하는 경우 프로세스를 트리거되어 파일, 메타 데이터 및 텍스트를 추출 합니다.</span><span class="sxs-lookup"><span data-stu-id="0644e-104">When you add search results to evidence, a process is triggered to extract files, metadata, and text.</span></span> <span data-ttu-id="0644e-105">그러면 시스템에서 모든 데이터의 새 인덱스를 작성 하 고 **증거**에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="0644e-105">Then, the system builds a new index of all the data and adds to **Evidence**.</span></span> 

<span data-ttu-id="0644e-106">이를 통해 모든 시간 관련 인시던트의 경우 격리 된 환경에서 다시 만든 증거를 조사 하면서 원래 위치에서 데이터를 삭제 하는 방식으로 환경을 빠르게 포함할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0644e-106">For any time-sensitive incidents, this allows you to quickly contain the environment by deleting data at original locations while investigating re-created evidence in a quarantined environment.</span></span> <span data-ttu-id="0644e-107">증거를 수집한 후에는 개별 문서를 원시 형식, 텍스트 형식 또는 거의 기본 형식으로 검토할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0644e-107">Once evidence is collected, you can review individual documents in their native format, text format, or a near-native format.</span></span> <span data-ttu-id="0644e-108">또한 쿼리를 실행 하 여 시간 범위, 파일 형식, 데이터 소유자 및 기타 다양 한 조건 카드로 데이터를 좁힐 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0644e-108">Additionally, you can run queries to narrow the data by time range, file types, data owners, and many other condition cards.</span></span> <span data-ttu-id="0644e-109">작성자/보낸 사람/받는 사람 조건 카드를 사용 하면 분산에 관여 하는 사람과 외부 공유가 있는지 신속 하 게 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0644e-109">Using Author/Sender/Recipient condition cards, you can quickly examine who are involved in the spill and if there have been any external shares.</span></span> <span data-ttu-id="0644e-110">자세한 내용은 다음을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="0644e-110">For more information, see:</span></span>

  - [<span data-ttu-id="0644e-111">증거에서 데이터 쿼리</span><span class="sxs-lookup"><span data-stu-id="0644e-111">Query the data in evidence</span></span>](evidence-query.md)

<span data-ttu-id="0644e-112">문서를 그룹화 하 고 검토에 대 한 추가 지원을 받으려면 **증거 관리**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="0644e-112">To group documents and get more assistance for your review, click **Manage evidence**.</span></span> <span data-ttu-id="0644e-113">**분석** 타일에서 **분석**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="0644e-113">In the **Analytics** tile, click **Analyze**.</span></span> <span data-ttu-id="0644e-114">이렇게 하면 중복 검색, 전자 메일 스레딩 및 테마 분석과 같은 고급 분석이 실행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0644e-114">This will run advanced analytics such as duplicate detection, email threading, and theme analysis.</span></span> <span data-ttu-id="0644e-115">나중에 데이터의 일반 테마를 확인 하 고 전자 메일 스레드, 정확히 복제 및 근접 한 중복을 통해 문서를 구성 하 여 조사를 용이 하 게 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0644e-115">Afterwards, you can see the general themes of the data and also organize documents by email threads, exact duplicates and near duplicates to facilitate your investigation.</span></span> <span data-ttu-id="0644e-116">자세한 내용은 다음을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="0644e-116">For more information, see:</span></span>

  - [<span data-ttu-id="0644e-117">분석을 실행 하 여 더 빠른 조사</span><span class="sxs-lookup"><span data-stu-id="0644e-117">Run analytics to investigate faster</span></span>](run-analytics-to-investigate-faster.md)

## <a name="view-documents-in-evidence"></a><span data-ttu-id="0644e-118">증거에서 문서 보기</span><span class="sxs-lookup"><span data-stu-id="0644e-118">View documents in evidence</span></span>

<span data-ttu-id="0644e-119">데이터 조사 (미리 보기)는 용도가 각각 다른 여러 viewer를 통해 콘텐츠를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="0644e-119">Data investigation (Preview) displays content via several viewers each with different purposes.</span></span> <span data-ttu-id="0644e-120">**증거**에서 문서를 클릭 하 여 다양 한 뷰어를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0644e-120">The various viewers can be used by clicking on any document in **Evidence**.</span></span> <span data-ttu-id="0644e-121">현재 제공 되는 뷰어는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="0644e-121">The viewers currently provided are:</span></span>

- <span data-ttu-id="0644e-122">파일 메타 데이터</span><span class="sxs-lookup"><span data-stu-id="0644e-122">File metadata</span></span>
- <span data-ttu-id="0644e-123">기본 보기</span><span class="sxs-lookup"><span data-stu-id="0644e-123">Native view</span></span>
- <span data-ttu-id="0644e-124">텍스트 보기</span><span class="sxs-lookup"><span data-stu-id="0644e-124">Text view</span></span>
- <span data-ttu-id="0644e-125">주석 달기 보기</span><span class="sxs-lookup"><span data-stu-id="0644e-125">Annotate view</span></span>
- <span data-ttu-id="0644e-126">변환 된 보기</span><span class="sxs-lookup"><span data-stu-id="0644e-126">Converted view</span></span>

## <a name="file-metadata"></a><span data-ttu-id="0644e-127">파일 메타 데이터</span><span class="sxs-lookup"><span data-stu-id="0644e-127">File metadata</span></span>

<span data-ttu-id="0644e-128">이 패널을 설정/해제 하 여 문서와 연결 된 다양 한 메타 데이터를 표시할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0644e-128">This panel can be toggled on/off to display various metadata associated with the document.</span></span> <span data-ttu-id="0644e-129">특정 메타 데이터를 표시 하도록 검색 결과 표를 사용자 지정할 수 있지만 데이터를 검토 하는 동안 가로로 스크롤 하기가 어려울 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0644e-129">Although the search results grid can be customized to display specific metadata, there are instances where scrolling horizontally can be difficult while reviewing data.</span></span> <span data-ttu-id="0644e-130">사용자는 파일 메타 데이터 패널을 사용 하 여 보기를 전환할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0644e-130">The File metadata panel allows a user to toggle on a view within the viewer.</span></span>

![<span data-ttu-id="0644e-131">파일 메타 데이터 패널</span><span class="sxs-lookup"><span data-stu-id="0644e-131">File metadata panel</span></span>
](../media/Reviewimage2.png)

## <a name="native-view"></a><span data-ttu-id="0644e-132">기본 보기</span><span class="sxs-lookup"><span data-stu-id="0644e-132">Native view</span></span>

<span data-ttu-id="0644e-133">기본 뷰어에 문서의 가장 다양 한 보기가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0644e-133">The Native viewer displays the richest view of a document.</span></span> <span data-ttu-id="0644e-134">이 형식은 수백 개의 파일 형식을 지원 하며, truest을 기본적으로 사용할 수 있는 환경에 표시 하기 위한 것입니다.</span><span class="sxs-lookup"><span data-stu-id="0644e-134">It supports hundreds of file types and is meant to display the truest to native experience possible.</span></span> <span data-ttu-id="0644e-135">예를 들어 Microsoft office 파일용으로 보는 사용자는 문서 설명, Excel 수식, 숨겨진 행/열, PowerPoint 메모 등의 콘텐츠를 표시 하기 위해 Office Online을 활용 합니다. Office Online 뷰어에 대 한 자세한 내용은 여기 \[를 참조 하세요.\]</span><span class="sxs-lookup"><span data-stu-id="0644e-135">For Microsoft Office files, for example, the viewer leverages Office Online in order to display content such as document comments, Excel formulas, hidden rows/columns, PowerPoint notes, etc. For more information regarding the Office Online viewers, visit here \[need link\]</span></span>

![<span data-ttu-id="0644e-136">기본 보기</span><span class="sxs-lookup"><span data-stu-id="0644e-136">Native view</span></span>
](../media/Reviewimage3.png)

## <a name="text-view"></a><span data-ttu-id="0644e-137">텍스트 보기</span><span class="sxs-lookup"><span data-stu-id="0644e-137">Text view</span></span>

<span data-ttu-id="0644e-138">텍스트 뷰어는 파일의 추출 된 텍스트 보기를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="0644e-138">The Text viewer provides a view of the extracted text of a file.</span></span> <span data-ttu-id="0644e-139">이 메서드는 포함 된 이미지 및 서식을 무시 하지만 사용자가 콘텐츠를 빠르게 이해 하려는 경우에는이 보기가 매우 유용 합니다.</span><span class="sxs-lookup"><span data-stu-id="0644e-139">It ignores any embedded images and formatting but will be a very performant view if a user is trying to understand the content quickly.</span></span> <span data-ttu-id="0644e-140">텍스트 보기에도 다른 기능이 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0644e-140">Text view also includes other features:</span></span>

  - <span data-ttu-id="0644e-141">선 카운터를 사용 하 여 문서의 특정 부분을 보다 쉽게 참조할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0644e-141">Line counter makes it easier to reference specific portions of a document</span></span>

  - <span data-ttu-id="0644e-142">문서 내에 있는 용어 및 스크롤 막대를 강조 표시 하는 검색 방문 횟수 강조 표시</span><span class="sxs-lookup"><span data-stu-id="0644e-142">Search hit highlighting that will highlight terms within the document as well as the scrollbar</span></span>

  - <span data-ttu-id="0644e-143">Diff 보기에서는 중복 문서 근처를 볼 때 텍스트 차이를 강조 표시 하는 비교 보기를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="0644e-143">Diff view provides a comparison view that highlights textual differences when viewing Near Duplicate documents</span></span>

![<span data-ttu-id="0644e-144">텍스트 보기</span><span class="sxs-lookup"><span data-stu-id="0644e-144">Text view</span></span>
](../media/Reviewimage4.png)

![<span data-ttu-id="0644e-145">Diff 보기</span><span class="sxs-lookup"><span data-stu-id="0644e-145">Diff view</span></span>
](../media/Reviewimage5.png)

## <a name="annotate-view"></a><span data-ttu-id="0644e-146">주석 달기 보기</span><span class="sxs-lookup"><span data-stu-id="0644e-146">Annotate view</span></span>

<span data-ttu-id="0644e-147">주석 달기 보기에서는 다음과 같은 기능을 통해 사용자가 검토 중에 문서에 태그를 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0644e-147">The Annotate view provides features that allow users to apply markup on a document during investigation including:</span></span>

  - <span data-ttu-id="0644e-148">Area redactions – 사용자가 중요 한 콘텐츠를 숨기기 위해 문서에 상자를 그릴 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0644e-148">Area redactions – users can draw a box on the document in order to hide sensitive content</span></span>

  - <span data-ttu-id="0644e-149">연필-사용자가 문서에서 특정 부분에 주의를 기울일 수 있도록 문서에 대 한 자유 그리기 기능을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="0644e-149">Pencil – users can free-hand draw on a document in order to bring attention to certain portions of a document</span></span>

  - <span data-ttu-id="0644e-150">주석 선택-사용자가 문서에서 주석을 선택 하 여 삭제할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0644e-150">Select annotations - users can select annotations on a document in order to delete</span></span>

  - <span data-ttu-id="0644e-151">주석 투명도 설정/해제-주석 뒤에 있는 콘텐츠를 보기 위해 반투명 하 게 주석 작성</span><span class="sxs-lookup"><span data-stu-id="0644e-151">Toggle annotation transparency – makes annotations semi-transparent in order to view the content behind the annotation</span></span>

  - <span data-ttu-id="0644e-152">이전 페이지-이전 페이지로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="0644e-152">Previous page – navigates to previous page</span></span>

  - <span data-ttu-id="0644e-153">다음 페이지-다음 페이지로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="0644e-153">Next page – navigates to the next page</span></span>

  - <span data-ttu-id="0644e-154">이동할 페이지 – 사용자가 특정 페이지 번호를 입력 하 여</span><span class="sxs-lookup"><span data-stu-id="0644e-154">Go to page – user can enter a specific page number to navigate to</span></span>

  - <span data-ttu-id="0644e-155">Zoom-주석 보기에 대 한 확대/축소 수준을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0644e-155">Zoom – set zoom level for annotate view</span></span>

  - <span data-ttu-id="0644e-156">회전-사용자가 시계 방향으로 문서를 회전할 수 있음</span><span class="sxs-lookup"><span data-stu-id="0644e-156">Rotate – user can rotate document clockwise</span></span>

  - <span data-ttu-id="0644e-157">검색-사용자가 문서 내에서 검색 하 고 문서 내의 다양 한 방문으로 이동할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0644e-157">Search – user can search within a document and navigate to the various hits within the document</span></span>
    
    ![<span data-ttu-id="0644e-158">주석 달기 보기</span><span class="sxs-lookup"><span data-stu-id="0644e-158">Annotate view</span></span>
    ](../media/Reviewimage1.png)

<span data-ttu-id="0644e-159">이러한 주석은 실제 시스템의 원래 위치에서가 아니라 증거로 수집 된 데이터에 대 한 정보입니다.</span><span class="sxs-lookup"><span data-stu-id="0644e-159">Note that these annotations are on data collected as evidence, not at its original location in live system.</span></span> 

## <a name="more-information"></a><span data-ttu-id="0644e-160">추가 정보</span><span class="sxs-lookup"><span data-stu-id="0644e-160">More information</span></span>

<span data-ttu-id="0644e-161">다음 표에는 데이터 조사 (미리 보기)의 증거에 대 한 한계가 나와 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0644e-161">The following table lists the limits for evidence in Data Investigations (Preview).</span></span>  <span data-ttu-id="0644e-162">단일 파일의 최대값을 초과 하는 항목은 처리 오류로 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0644e-162">Any items that exceed the single file maximums will show up as processing errors.</span></span>
    
  |<span data-ttu-id="0644e-163">**제한 설명**</span><span class="sxs-lookup"><span data-stu-id="0644e-163">**Description of limit**</span></span>|<span data-ttu-id="0644e-164">**제한 유형**</span><span class="sxs-lookup"><span data-stu-id="0644e-164">**Limit**</span></span>|
  |:-----|:-----|
  |<span data-ttu-id="0644e-165">최대 증거 수집 수</span><span class="sxs-lookup"><span data-stu-id="0644e-165">Maximum number of evidence collections</span></span>  <br/> |<span data-ttu-id="0644e-166">50</span><span class="sxs-lookup"><span data-stu-id="0644e-166">50</span></span>  <br/> |
  |<span data-ttu-id="0644e-167">ingested 수 있는 총 문서 수입니다 (조사에 있는 모든 증거 컬렉션의 경우).</span><span class="sxs-lookup"><span data-stu-id="0644e-167">Total number of documents that can be ingested into a case (for all evidence collections in the investigation)</span></span>  <br/> |<span data-ttu-id="0644e-168">1백만 개</span><span class="sxs-lookup"><span data-stu-id="0644e-168">1 million</span></span>  <br/> |
  |<span data-ttu-id="0644e-169">부하 당 총 파일 크기</span><span class="sxs-lookup"><span data-stu-id="0644e-169">Total file size per load</span></span>  <br/> |<span data-ttu-id="0644e-170">100GB</span><span class="sxs-lookup"><span data-stu-id="0644e-170">100 GB</span></span>  <br/> |
  |<span data-ttu-id="0644e-171">단일 파일의 최대 크기</span><span class="sxs-lookup"><span data-stu-id="0644e-171">Maximum size of single file</span></span>   <br/> |<span data-ttu-id="0644e-172">100MB</span><span class="sxs-lookup"><span data-stu-id="0644e-172">100 MB</span></span>  <br/> |
  |<span data-ttu-id="0644e-173">단일 파일에서 추출한 최대 문자 수</span><span class="sxs-lookup"><span data-stu-id="0644e-173">Maximum number of characters extracted from a single file</span></span>  <br/> |<span data-ttu-id="0644e-174">1000만</span><span class="sxs-lookup"><span data-stu-id="0644e-174">10 million</span></span>  <br/> |
  |<span data-ttu-id="0644e-175">문서에 포함 된 항목의 깊이</span><span class="sxs-lookup"><span data-stu-id="0644e-175">Depth of embedded items in a document</span></span>  <br/> |<span data-ttu-id="0644e-176">25@@</span><span class="sxs-lookup"><span data-stu-id="0644e-176">25</span></span>  <br/> |
  