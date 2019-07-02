---
title: 증거 데이터 검토
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
ms.openlocfilehash: a5c1c578f8d45cf7b95629e8053911d93b5b8583
ms.sourcegitcommit: 6bb40cf53374eaaae8da0a469f0248b1163184a4
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/07/2019
ms.locfileid: "34767339"
---
# <a name="review-the-data-in-evidence"></a><span data-ttu-id="4e898-102">증거 데이터 검토</span><span class="sxs-lookup"><span data-stu-id="4e898-102">Review the data in evidence</span></span>

<span data-ttu-id="4e898-103">데이터 조사에서 증명 정보 집합의 데이터는 수집 되어 증거 집합에 추가한 검색 결과의 스냅숏입니다.</span><span class="sxs-lookup"><span data-stu-id="4e898-103">The data in an evidence set in a data investigation is a snapshot of the search results that you collected and added to the evidence set.</span></span> <span data-ttu-id="4e898-104">검색 결과를 증거에 추가 하면 프로세스가 트리거되어 검색에서 반환 하는 항목에서 파일, 메타 데이터 및 텍스트를 추출 합니다.</span><span class="sxs-lookup"><span data-stu-id="4e898-104">When you add search results to evidence, a process is triggered to extract files, metadata, and text from the items returned by the search.</span></span> <span data-ttu-id="4e898-105">그런 다음 데이터 조사 (미리 보기) 도구는 모든 데이터의 새 인덱스 ( *고급 인덱싱*프로세스)를 작성 하 고 **증거** 탭의 증거 집합에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="4e898-105">Then the Data Investigations (Preview) tool then builds a new index (by a process called *Advanced indexing*) of all the data and adds to an evidence set on the **Evidence** tab.</span></span> 

<span data-ttu-id="4e898-106">이를 통해 시간에 민감한 조사를 통해 원래 데이터 원본에 있는 실제 또는 악성 데이터를 삭제 하 여 환경을 신속 하 게 포함할 수 있으며,이를 통해 동시에 다시 만들어진 증거를 조사할 수 있습니다. 격리 된 환경-이 경우 증명 정보 집합에 복사 되는 데이터입니다.</span><span class="sxs-lookup"><span data-stu-id="4e898-106">For time-sensitive investigations, this allows you to quickly contain the environment by deleting the actual spilled or malicious data located in the at original data source, while at the same time allowing you to investigate the re-created evidence in a quarantined environment, which in this case is the data copied to the evidence set).</span></span> <span data-ttu-id="4e898-107">증거를 수집 하 고 증명 정보 집합에 추가한 후에는 문서에 주석을 달고 수정 하는 데 사용할 수 있는 기본 형식, 텍스트 형식 또는 거의 네이티브 형식으로 개별 문서를 검토할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4e898-107">After the evidence is collected and added to the evidence set, you can review individual documents in their native format, text format, or a near-native format that you can use to annotate and redact documents.</span></span> <span data-ttu-id="4e898-108">또한 쿼리를 실행 하 여 시간 범위, 파일 형식, 데이터 소유자 및 기타 다양 한 속성과 검색 조건으로 데이터 집합의 범위를 좁힐 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4e898-108">Additionally, you can run queries to narrow the data set by time range, file types, data owners, and many other properties and search conditions.</span></span> <span data-ttu-id="4e898-109">예를 들어 만든이, 보낸 사람 또는 받는 사람 조건을 사용 하 여 사건과 관련 된 사용자를 빠르게 식별 하 고 조직의 데이터를 외부 사용자와 공유 하는 경우를 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4e898-109">For example, by using the Author, Sender, or Recipient conditions, you can quickly identify the people are involved in the incident and if any data from your organization has been shared with external users.</span></span> <span data-ttu-id="4e898-110">증명 정보 집합에서 데이터를 검색 하는 방법에 대 한 자세한 내용은 [데이터를 증거에 쿼리](evidence-query.md)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="4e898-110">For more information about searching through data in an evidence set, see [Query the data in evidence](evidence-query.md).</span></span>

<span data-ttu-id="4e898-111">문서를 그룹화 하 고 검토에 대 한 추가 지원을 받으려면 **증거** 탭에서 증명 정보 집합을 선택 하 고 **증거 관리**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="4e898-111">To group documents and get more assistance for your review, select an evidence set on the **Evidence** tab, and then click **Manage evidence**.</span></span> <span data-ttu-id="4e898-112">**분석** 타일에서 **전체 집합에 대해 분석 다시 작성**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="4e898-112">In the **Analytics** tile, click **Rebuild analytics for the whole set**.</span></span> <span data-ttu-id="4e898-113">이렇게 하면 중복 검색, 전자 메일 스레딩 및 테마 분석과 같은 고급 분석이 실행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4e898-113">This will run advanced analytics such as duplicate detection, email threading, and theme analysis.</span></span> <span data-ttu-id="4e898-114">나중에 데이터의 일반 테마를 보고, 전자 메일 스레드, 중복에 가깝게 문서를 구성 하 고, 정확히 중복 하 여 조사에 도움을 받을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4e898-114">Afterwards, you can see the general themes of the data and also organize documents by email threads, near duplicates, and exact duplicates to help your investigation.</span></span> <span data-ttu-id="4e898-115">자세한 내용은 [분석을 실행 하 여 더 빠르게 조사](run-analytics-to-investigate-faster.md)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="4e898-115">For more information, see [Run analytics to investigate faster](run-analytics-to-investigate-faster.md).</span></span>

## <a name="view-documents-in-evidence"></a><span data-ttu-id="4e898-116">증거에서 문서 보기</span><span class="sxs-lookup"><span data-stu-id="4e898-116">View documents in evidence</span></span>

<span data-ttu-id="4e898-117">데이터 조사 (미리 보기)를 사용 하면 서로 다른 용도로 각 뷰어를 사용 하 여 여러 다른 뷰어에 콘텐츠를 표시할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4e898-117">Data Investigations (Preview) allows you to display content in several different viewers, with each viewer having a different purpose.</span></span> <span data-ttu-id="4e898-118">이러한 뷰어는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="4e898-118">These viewers are:</span></span>

- <span data-ttu-id="4e898-119">파일 메타 데이터</span><span class="sxs-lookup"><span data-stu-id="4e898-119">File metadata</span></span>
- <span data-ttu-id="4e898-120">기본 보기</span><span class="sxs-lookup"><span data-stu-id="4e898-120">Native view</span></span>
- <span data-ttu-id="4e898-121">텍스트 보기</span><span class="sxs-lookup"><span data-stu-id="4e898-121">Text view</span></span>
- <span data-ttu-id="4e898-122">주석 달기 보기</span><span class="sxs-lookup"><span data-stu-id="4e898-122">Annotate view</span></span>

<span data-ttu-id="4e898-123">이러한 뷰어에 액세스 하려면 증거 집합에서 문서를 선택 하면 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4e898-123">To access any of these viewers, just select a document in an evidence set.</span></span>

## <a name="file-metadata"></a><span data-ttu-id="4e898-124">파일 메타 데이터</span><span class="sxs-lookup"><span data-stu-id="4e898-124">File metadata</span></span>

<span data-ttu-id="4e898-125">이 보기에는 선택한 문서와 연결 된 다양 한 메타 데이터 속성이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4e898-125">This view displays various metadata properties associated with the selected document.</span></span> <span data-ttu-id="4e898-126">**파일 메타 데이터**를 클릭 하 여이 보기를 설정 하거나 해제할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4e898-126">You can toggle this view on and off by clicking **File metadata**.</span></span> <span data-ttu-id="4e898-127">문서를 검토할 때 파일 메타 데이터를 볼 수 있으며 서로 다른 보는 사용자 간에 변경 내용이 계속 유지 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4e898-127">When reviewing a document, you can view the file metadata and still change between the different viewers.</span></span>

<span data-ttu-id="4e898-128">다음은 문서에 대 한 파일 메타 데이터의 예입니다.</span><span class="sxs-lookup"><span data-stu-id="4e898-128">Here's an example of the file metadata for a document.</span></span> <span data-ttu-id="4e898-129">메타 데이터 필드에 대 한 자세한 내용은 [데이터 조사 (Preview)의 문서 메타 데이터 필드](document-metadata-fields.md)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="4e898-129">For more information about the metadata fields, see [Document metadata fields in Data Investigations (Preview)](document-metadata-fields.md).</span></span>

![파일 메타 데이터 패널](../media/Reviewimage2.png)

## <a name="native-view"></a><span data-ttu-id="4e898-131">기본 보기</span><span class="sxs-lookup"><span data-stu-id="4e898-131">Native view</span></span>

<span data-ttu-id="4e898-132">기본 뷰어에는 문서의 기본 형식으로 가장 정확한 보기가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4e898-132">The Native viewer displays the most accurate view of a document in it's native format.</span></span> <span data-ttu-id="4e898-133">기본 보기는 수백 가지 파일 형식에서 지원 되며, truest 기본 환경에서 문서를 표시 하는 데 목적이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4e898-133">Native view is supported for hundreds of file types and is meant to display documents in the truest native experience possible.</span></span> <span data-ttu-id="4e898-134">Microsoft Office 파일의 경우 네이티브 뷰어는 웹 버전의 Office 앱을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="4e898-134">For Microsoft Office files, the Native viewer uses the web version of Office apps.</span></span> <span data-ttu-id="4e898-135">이렇게 하면 Excel의 여러 Office 문서, 수식 및 숨겨진 행/열과 PowerPoint의 메모 보기와 같은 콘텐츠를 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4e898-135">This allows you to view content such as comments in different Office documents, formulas and hidden rows/columns in Excel, and the Notes view in PowerPoint.</span></span>

![<span data-ttu-id="4e898-136">기본 보기</span><span class="sxs-lookup"><span data-stu-id="4e898-136">Native view</span></span>
](../media/Reviewimage3.png)

## <a name="text-view"></a><span data-ttu-id="4e898-137">텍스트 보기</span><span class="sxs-lookup"><span data-stu-id="4e898-137">Text view</span></span>

<span data-ttu-id="4e898-138">텍스트 뷰어는 파일의 추출 된 텍스트 보기를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="4e898-138">The Text viewer provides a view of the extracted text of a file.</span></span> <span data-ttu-id="4e898-139">이 보기는 포함 된 이미지 및 서식을 무시 하지만 문서 내용을 빠르게 검토 하 고 이해 하려는 경우에는이 보기가 매우 유용 합니다.</span><span class="sxs-lookup"><span data-stu-id="4e898-139">It ignores any embedded images and formatting, but this view is very useful if you're trying to quickly review and understand the content in a document.</span></span> <span data-ttu-id="4e898-140">텍스트 보기에도 다음 기능이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4e898-140">Text view also includes these features:</span></span>

  - <span data-ttu-id="4e898-141">줄 카운터를 사용 하 여 문서의 특정 부분을 보다 쉽게 참조할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4e898-141">A line counter, which makes it easier to reference specific portions of a document.</span></span>

  - <span data-ttu-id="4e898-142">문서에 있는 용어 뿐 아니라 스크롤 막대에 표시 되는 검색 결과 강조 표시</span><span class="sxs-lookup"><span data-stu-id="4e898-142">Search hit highlighting that highlight terms in the document as well as on the scrollbar</span></span>

  - <span data-ttu-id="4e898-143">Diff 보기는 **Near 복제** 패널을 사용 하 여 문서를 볼 때 텍스트 차이를 강조 하는 비교 보기를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="4e898-143">A diff view provides a comparison view that highlights the text differences when viewing documents using the **Near duplicates** panel.</span></span>

<span data-ttu-id="4e898-144">**텍스트 및 스크롤 막대의 선 카운터 및 검색 결과 강조 표시 예제**</span><span class="sxs-lookup"><span data-stu-id="4e898-144">**Example of line counter and search hit highlighting in text and scrollbar**</span></span>

![<span data-ttu-id="4e898-145">텍스트 보기</span><span class="sxs-lookup"><span data-stu-id="4e898-145">Text view</span></span>
](../media/Reviewimage4.png)

<span data-ttu-id="4e898-146">**Diff 보기의 예**</span><span class="sxs-lookup"><span data-stu-id="4e898-146">**Example of the diff view**</span></span>

![<span data-ttu-id="4e898-147">Diff 보기</span><span class="sxs-lookup"><span data-stu-id="4e898-147">Diff view</span></span>
](../media/Reviewimage5.png)

## <a name="annotate-view"></a><span data-ttu-id="4e898-148">주석 달기 보기</span><span class="sxs-lookup"><span data-stu-id="4e898-148">Annotate view</span></span>

<span data-ttu-id="4e898-149">주석 달기 보기는 검토 프로세스 중에 문서에 태그를 적용할 수 있는 기능을 제공 합니다. 여기에는 다음과 같은 도구가 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4e898-149">The Annotate view provides features that allow you to apply markup on a document during the review process; this  includes these tools:</span></span>

  - <span data-ttu-id="4e898-150">**영역 redactions** -문서에 중요 한 콘텐츠를 숨기는 불투명 상자를 그릴 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4e898-150">**Area redactions** – You can draw an opaque box on the document that hides sensitive content.</span></span>

  - <span data-ttu-id="4e898-151">**연필** -문서에서 자유롭게 그리기 기능을 사용 하 여 콘텐츠의 특정 부분에 주의를 가져갈 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4e898-151">**Pencil** – You can free-hand draw on a document to bring attention to certain portions of the content</span></span>

  - <span data-ttu-id="4e898-152">**주석 선택** -문서에서 주석을 선택 하 고 삭제할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4e898-152">**Select annotations** - You can select and delete annotations in a document.</span></span>

  - <span data-ttu-id="4e898-153">**주석 투명도 설정/해제** -주석 뒤에 있는 콘텐츠를 볼 수 있도록 주석의 투명도 (불투명 및 반투명 사이)를 전환할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4e898-153">**Toggle annotation transparency** – You can toggle the transparency of annotations (between opaque and semi-transparent)so you can view the content behind the annotation.</span></span> <span data-ttu-id="4e898-154">여기에는 연필 주석과 redactions의 투명도를 전환 하는 것이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4e898-154">This includes toggling the transparency of pencil annotations and redactions.</span></span>

<span data-ttu-id="4e898-155">또한 주석 달기 보기에서는 다음과 같은 탐색 기능을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="4e898-155">The Annotate view also provides the following navigation functionality:</span></span>

  - <span data-ttu-id="4e898-156">**이전 페이지**, **다음 페이지**및 페이지 탐색 컨트롤로 **이동** 하 여 여러 페이지 문서에 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="4e898-156">**Previous page**, **Next page**, and **Go to page** - Navigation controls to use for multi-page documents.</span></span>

  - <span data-ttu-id="4e898-157">**Zoom** -주석 보기에서 문서 크기를 늘리거나 줄입니다.</span><span class="sxs-lookup"><span data-stu-id="4e898-157">**Zoom** – Increases or decreases the size of documents in Annotate view.</span></span>

  - <span data-ttu-id="4e898-158">**회전** -문서를 시계 방향으로 회전 합니다.</span><span class="sxs-lookup"><span data-stu-id="4e898-158">**Rotate** – Rotate documents clockwise.</span></span>

  - <span data-ttu-id="4e898-159">**검색** -문서에서 키워드를 검색 한 다음 이전 및 다음 컨트롤을 사용 하 여 문서 내에서 강조 표시 된 방문 수를 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="4e898-159">**Search** – Search for keywords in a document, and then use Previous and Next controls to view the hits (which are highlighted) within the document.</span></span>

<span data-ttu-id="4e898-160">**주석 달기 보기의 예**</span><span class="sxs-lookup"><span data-stu-id="4e898-160">**Example of Annotate view**</span></span>

![주석 달기 보기](../media/Reviewimage1.png)

> [!NOTE]
> <span data-ttu-id="4e898-162">주석은 증거 집합에 추가 된 문서의 복사본에 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4e898-162">Annotations are applied to a copy of the document that was added to the evidence set.</span></span> <span data-ttu-id="4e898-163">라이브 서비스의 원본 문서에는 주석이 추가 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4e898-163">The original documents in the live service aren't annotated.</span></span>
