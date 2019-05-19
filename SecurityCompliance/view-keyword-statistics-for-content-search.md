---
title: 콘텐츠 검색 결과에 대한 키워드 통계 보기
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 1/30/2017
audience: Admin
ms.topic: article
ms.service: O365-seccomp
ms.collection: M365-security-compliance
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: 9701a024-c52e-43f0-b545-9a53478aec04
description: 검색 통계 기능을 사용 하 여 보안 & 준수 센터의 여러 콘텐츠 검색에 대 한 통계를 표시 하 고 비교할 수 있습니다. 검색 쿼리를 만들거나 편집할 때 키워드 목록을 구성 하 여 각 키워드나 키워드 구와 일치 하는 항목 수를 표시 하는 통계를 향상 시킬 수도 있습니다.
ms.openlocfilehash: 558d8bd269d1c1d8bfcf3f15452a83de74f3e38d
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/17/2019
ms.locfileid: "34157910"
---
# <a name="view-keyword-statistics-for-content-search-results"></a><span data-ttu-id="c2b5c-104">콘텐츠 검색 결과에 대한 키워드 통계 보기</span><span class="sxs-lookup"><span data-stu-id="c2b5c-104">View keyword statistics for Content Search results</span></span>

<span data-ttu-id="c2b5c-105">콘텐츠 검색을 만들고 실행 한 후에는 예상 검색 결과에 대 한 통계 정보를 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c2b5c-105">After you create and run a Content Search, you can view statistics about the estimated search results.</span></span> <span data-ttu-id="c2b5c-106">여기에는 검색 결과에 대 한 요약, 세부 정보 창에 표시 되는 예상 검색 결과 요약, 검색 쿼리와 일치 하는 항목이 있는 콘텐츠 위치 수, 콘텐츠 위치 이름 등의 쿼리 통계도 포함 됩니다. 가장 일치 하는 항목이 있는 항목입니다.</span><span class="sxs-lookup"><span data-stu-id="c2b5c-106">This includes a summary of the search results (similar to the summary of the estimated search results displayed in the details pane), the query statistics such as the number of content locations with items that match the search query, and the name of content locations that have the most matching items.</span></span> <span data-ttu-id="c2b5c-107">하나 이상의 콘텐츠 검색에 대 한 통계를 표시할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c2b5c-107">You can display statistics for one or more content searches.</span></span> <span data-ttu-id="c2b5c-108">이렇게 하면 여러 검색에 대 한 결과를 빠르게 비교 하 고 검색 쿼리의 효율성을 결정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c2b5c-108">This lets you to quickly compare the results for multiple searches and make decisions about the effectiveness of your search queries.</span></span>
  
<span data-ttu-id="c2b5c-109">또한 검색 쿼리의 각 키워드에 대 한 통계를 반환 하도록 신규 및 기존 검색을 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c2b5c-109">Additionally, you can configure new and existing searches to return statistics for each keyword in a search query.</span></span> <span data-ttu-id="c2b5c-110">이를 통해 쿼리의 각 키워드에 대 한 결과 수를 비교 하 고 여러 검색의 키워드 통계를 비교할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c2b5c-110">This lets you compare the number of results for each keyword in a query and to compare the keyword statistics from multiple searches.</span></span>
  
<span data-ttu-id="c2b5c-111">또한 검색 통계 및 키워드 통계를 CSV 파일에 다운로드할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c2b5c-111">You can also download the search statistics and keyword statistics to a CSV file.</span></span> <span data-ttu-id="c2b5c-112">이렇게 하면 Excel의 필터링 및 정렬 기능을 사용 하 여 결과를 비교 하 고 보고서를 검색 결과에 대해 준비할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c2b5c-112">This lets you use the filtering and sorting features in Excel to compare results, and prepare reports for your search results.</span></span>
  
## <a name="get-statistics-for-content-searches"></a><span data-ttu-id="c2b5c-113">콘텐츠 검색에 대 한 통계 가져오기</span><span class="sxs-lookup"><span data-stu-id="c2b5c-113">Get statistics for Content Searches</span></span>

<span data-ttu-id="c2b5c-114">콘텐츠 검색에 대 한 통계를 표시 하려면:</span><span class="sxs-lookup"><span data-stu-id="c2b5c-114">To display statistics for Content Searches:</span></span>
  
1. <span data-ttu-id="c2b5c-115">보안 & 준수 센터에서 **검색** \> **콘텐츠 검색**으로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2b5c-115">In the Security & Compliance Center, go to **Search** \> **Content search**.</span></span>
    
2. <span data-ttu-id="c2b5c-116">검색 목록에서 검색을 하나 이상 선택 하 고 **검색 통계**![검색 통계 단추](media/9bf56d43-25bf-4f53-a4be-f4d55102310c.png)를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2b5c-116">In the list of searches, select one or more searches, and then click **Search statistics**![Search Statistics button](media/9bf56d43-25bf-4f53-a4be-f4d55102310c.png).</span></span>
    
    ![여러 검색을 선택한 다음 검색 통계를 클릭 합니다.](media/1195c6c3-2e00-469d-8c29-85c1c7ebe6c7.png)
  
3. <span data-ttu-id="c2b5c-118">**검색 통계** 페이지에서 다음 링크 중 하나를 클릭 하 여 선택한 검색에 대 한 통계를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2b5c-118">On the **Search statistics** page, click one of the following links to display statistics about the selected searches.</span></span> 
    
    <span data-ttu-id="c2b5c-119">**간략하게**</span><span class="sxs-lookup"><span data-stu-id="c2b5c-119">**Summary**</span></span>
    
    <span data-ttu-id="c2b5c-120">이 페이지는 **콘텐츠 검색** 페이지의 세부 정보 창에 표시 되는 것과 비슷한 통계를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2b5c-120">This page displays statistics similar to the ones displayed in the details pane on the **Content search** page.</span></span> <span data-ttu-id="c2b5c-121">선택한 모든 검색에 대 한 통계가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c2b5c-121">Statistics for all selected searches are displayed.</span></span> <span data-ttu-id="c2b5c-122">이 페이지에서 선택한 검색을 다시 실행 하 여 통계를 업데이트할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c2b5c-122">Note that you can also re-run the selected searches from this page to update the statistics.</span></span> 
    
    ![선택한 검색 통계 요약](media/abb663eb-b3d6-4f4c-a99f-55d20b0848af.png)
  
    <span data-ttu-id="c2b5c-124">위한.</span><span class="sxs-lookup"><span data-stu-id="c2b5c-124">a.</span></span>  <span data-ttu-id="c2b5c-125">콘텐츠 검색의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c2b5c-125">The name of the Content Search.</span></span> <span data-ttu-id="c2b5c-126">앞서 설명한 것 처럼 여러 검색에 대 한 통계를 표시 하 고 비교할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c2b5c-126">As previously stated, you can display and compare statistics for multiple searches.</span></span>
    
    <span data-ttu-id="c2b5c-127">b.</span><span class="sxs-lookup"><span data-stu-id="c2b5c-127">b.</span></span> <span data-ttu-id="c2b5c-128">검색 된 콘텐츠 위치의 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="c2b5c-128">The type of content location that was searched.</span></span> <span data-ttu-id="c2b5c-129">각 행은 지정 된 검색에서 사서함, 사이트 및 공용 폴더에 대 한 통계를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2b5c-129">Each row displays statistics for mailboxes, sites, and public folders from the specified search.</span></span>
    
    <span data-ttu-id="c2b5c-130">&.</span><span class="sxs-lookup"><span data-stu-id="c2b5c-130">c.</span></span> <span data-ttu-id="c2b5c-131">검색 쿼리와 일치 하는 항목을 포함 하는 콘텐츠 위치의 수입니다.</span><span class="sxs-lookup"><span data-stu-id="c2b5c-131">The number of content locations containing items that match the search query.</span></span> <span data-ttu-id="c2b5c-132">사서함의 경우이 통계에는 검색 쿼리와 일치 하는 항목을 포함 하는 보관 사서함의 수도 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c2b5c-132">For mailboxes, this statistic also includes the number of archive mailboxes that contain items that match the search query.</span></span>
    
    <span data-ttu-id="c2b5c-133">&.</span><span class="sxs-lookup"><span data-stu-id="c2b5c-133">d.</span></span> <span data-ttu-id="c2b5c-134">검색 쿼리와 일치 하는 지정 된 모든 콘텐츠 위치의 총 항목 수입니다.</span><span class="sxs-lookup"><span data-stu-id="c2b5c-134">The total number of items of all specified content locations that match the search query.</span></span> <span data-ttu-id="c2b5c-135">항목 유형의 예로는 전자 메일 메시지, 일정 항목, 문서 등이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c2b5c-135">Examples of item types include email messages, calendar items, and documents.</span></span> <span data-ttu-id="c2b5c-136">항목에 검색 중인 키워드의 인스턴스가 여러 개 포함 되어 있으면 총 항목 수에 한 번만 계산 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c2b5c-136">If an item contains multiple instances of a keyword that is being searched for, it's only counted once in the total number of items.</span></span> <span data-ttu-id="c2b5c-137">예를 들어 "stock" 또는 "사기" 라는 단어를 검색 하는 경우 전자 메일 메시지에 단어 "stock"의 인스턴스가 세 개 포함 되어 있으면 **항목** 열에서 한 번만 계산 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c2b5c-137">For example, if you're searching for words "stock" or "fraud" and an email message contains three instances of the word "stock", it's only counted once in the **Items** column.</span></span> 
    
    <span data-ttu-id="c2b5c-138">e-learning.</span><span class="sxs-lookup"><span data-stu-id="c2b5c-138">e.</span></span> <span data-ttu-id="c2b5c-139">지정한 콘텐츠 위치에서 검색 쿼리와 일치 하는 모든 항목의 총 크기입니다.</span><span class="sxs-lookup"><span data-stu-id="c2b5c-139">The total size of all items that were found in the specified content location that match the search query.</span></span> 
    
    <span data-ttu-id="c2b5c-140">**쿼리하도록**</span><span class="sxs-lookup"><span data-stu-id="c2b5c-140">**Queries**</span></span>
    
    <span data-ttu-id="c2b5c-141">이 페이지에는 검색 쿼리에 대 한 통계가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c2b5c-141">This page displays statistics about the search query.</span></span>
    
    ![선택한 검색에 대 한 검색 쿼리 통계](media/dc817526-dfb9-43d3-a14c-4c58077eb7bb.png)
  
    <span data-ttu-id="c2b5c-143">위한.</span><span class="sxs-lookup"><span data-stu-id="c2b5c-143">a.</span></span> <span data-ttu-id="c2b5c-144">행이 쿼리 통계를 포함 하는 콘텐츠 검색의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c2b5c-144">The name of the Content Search that the row contains query statistics for.</span></span>
    
    <span data-ttu-id="c2b5c-145">b.</span><span class="sxs-lookup"><span data-stu-id="c2b5c-145">b.</span></span> <span data-ttu-id="c2b5c-146">쿼리 통계를 적용할 수 있는 콘텐츠 위치의 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="c2b5c-146">The type of content location that the query statistics are applicable to.</span></span>
    
    <span data-ttu-id="c2b5c-147">&.</span><span class="sxs-lookup"><span data-stu-id="c2b5c-147">c.</span></span> <span data-ttu-id="c2b5c-148">이 열은 검색 쿼리 중에서 통계를 적용할 수 있는 부분을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="c2b5c-148">This column indicates which part of the search query the statistics are applicable to.</span></span> <span data-ttu-id="c2b5c-149">**Primary** 전체 검색 쿼리를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="c2b5c-149">**Primary** indicates the entire search query.</span></span> <span data-ttu-id="c2b5c-150">검색 쿼리를 만들거나 편집할 때 키워드 목록을 사용 하면 쿼리의 각 구성 요소에 대 한 통계가이 테이블에 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c2b5c-150">If you use a keyword list when you create or edit a search query, statistics for each component of the query are included in this table.</span></span> <span data-ttu-id="c2b5c-151">자세한 내용은이 문서의 [콘텐츠 검색에 대 한 키워드 통계 받기](#get-keyword-statistics-for-content-searches) 섹션을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="c2b5c-151">See the [Get keyword statistics for Content Searches](#get-keyword-statistics-for-content-searches) section in this article for more information.</span></span> 
    
    <span data-ttu-id="c2b5c-152">&.</span><span class="sxs-lookup"><span data-stu-id="c2b5c-152">d.</span></span> <span data-ttu-id="c2b5c-153">이 열에는 콘텐츠 검색 도구에서 실행 되는 실제 검색 쿼리가 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c2b5c-153">This column contains the actual search query that run by the Content Search tool.</span></span> <span data-ttu-id="c2b5c-154">이 도구는 사용자가 만드는 쿼리에 몇 가지 추가 구성 요소를 자동으로 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2b5c-154">Note that the tool automatically adds a few additional components to the query that you create.</span></span> 

    - <span data-ttu-id="c2b5c-155">키워드를 지정 하지 않고 사서함의 모든 콘텐츠를 검색 하는 경우 실제 키 단어 쿼리는 모든 항목이 반환 `size>=0` 되도록 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c2b5c-155">When you search for all content in mailboxes (by not specifying any keywords), the actual key word query is  `size>=0` so that all items are returned.</span></span> 
    
     - <span data-ttu-id="c2b5c-156">SharePoint Online 및 비즈니스용 OneDrive 사이트를 검색 하면 다음과 같은 두 가지 구성 요소가 추가 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c2b5c-156">When you search SharePoint Online and OneDrive for Business sites, the two following components are added:</span></span>
    
          <span data-ttu-id="c2b5c-157">**IsExternalContent NOT: 1** -온-프레미스 SharePoint 조직에서 모든 콘텐츠를 제외 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2b5c-157">**NOT IsExternalContent:1** - Excludes any content from an on-premises SharePoint organization.</span></span> 
    
          <span data-ttu-id="c2b5c-158">**NOT IsOneNotePage: 1** -모든 OneNote 파일은 검색 쿼리와 일치 하는 모든 문서와 중복 되므로 제외 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2b5c-158">**NOT IsOneNotePage:1** - Excludes all OneNote files because these would be duplicates of any document that matches the search query.</span></span> 

    
    <span data-ttu-id="c2b5c-159">e-learning.</span><span class="sxs-lookup"><span data-stu-id="c2b5c-159">e.</span></span> <span data-ttu-id="c2b5c-160">**쿼리** 열에 나열 된 검색 쿼리와 일치 하는 항목을 포함 하는 콘텐츠 위치 (\* \* 위치 유형 \* \* 열로 지정)의 번호입니다.</span><span class="sxs-lookup"><span data-stu-id="c2b5c-160">The number of the content locations (specified by the \*\* Location type \*\* column) that contain items that match the search query listed in the **Query** column.</span></span> 
    
    <span data-ttu-id="c2b5c-161">식량.</span><span class="sxs-lookup"><span data-stu-id="c2b5c-161">f.</span></span> <span data-ttu-id="c2b5c-162">지정한 콘텐츠 위치에서 **쿼리** 열에 나열 된 검색 쿼리와 일치 하는 항목의 개수입니다.</span><span class="sxs-lookup"><span data-stu-id="c2b5c-162">The number of items (from the specified content location) that match the search query listed in the **Query** column.</span></span> <span data-ttu-id="c2b5c-163">앞에서 설명한 것 처럼 항목에 검색 중인 키워드의 인스턴스가 여러 개 포함 되어 있으면이 열에서 한 번만 계산 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c2b5c-163">As previously explained, if an item contains multiple instances of a keyword that is being searched for, it's only counted once in the this column.</span></span> 
    
    <span data-ttu-id="c2b5c-164">1g.</span><span class="sxs-lookup"><span data-stu-id="c2b5c-164">g.</span></span> <span data-ttu-id="c2b5c-165">지정한 콘텐츠 위치에 있는 검색 쿼리와 일치 하는 모든 항목의 총 크기입니다. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="c2b5c-165">The total size of all items that were found (in the specified content location) that match the search query in the **Query** column.</span></span> 
    
    <span data-ttu-id="c2b5c-166">**상위 위치**</span><span class="sxs-lookup"><span data-stu-id="c2b5c-166">**Top locations**</span></span>
    
    <span data-ttu-id="c2b5c-167">이 페이지에는 검색 쿼리와 일치 하는 항목 수에 대 한 통계를 검색 된 각 콘텐츠 위치에서 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2b5c-167">This page displays statistics about the number of items that match the search query in each content location that was searched.</span></span> <span data-ttu-id="c2b5c-168">주요 1000 위치가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c2b5c-168">The top 1,000 locations are displayed.</span></span> <span data-ttu-id="c2b5c-169">여러 검색에 대 한 통계를 확인 하는 경우 각 검색에 대 한 최상위 1000 위치가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c2b5c-169">If you view statistics for multiple searches, the top 1,000 locations for each search are displayed.</span></span> <span data-ttu-id="c2b5c-170">검색 쿼리와 일치 하는 항목이 포함 되어 있지 않은 콘텐츠 위치는이 페이지에 포함 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c2b5c-170">Note that a content location isn't included on this page if it doesn't contain any items that match the search query.</span></span>
    
    ![검색 된 콘텐츠 위치에 있는 항목 수에 대 한 통계](media/35a820b0-85d9-45d1-9a0c-c74bec803e67.png)
  
    <span data-ttu-id="c2b5c-172">위한.</span><span class="sxs-lookup"><span data-stu-id="c2b5c-172">a.</span></span> <span data-ttu-id="c2b5c-173">콘텐츠 위치의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c2b5c-173">The name of the content location.</span></span>
    
    <span data-ttu-id="c2b5c-174">b.</span><span class="sxs-lookup"><span data-stu-id="c2b5c-174">b.</span></span> <span data-ttu-id="c2b5c-175">위치 통계를 적용할 수 있는 콘텐츠 위치의 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="c2b5c-175">The type of content location that the location statistics are applicable to.</span></span>
    
    <span data-ttu-id="c2b5c-176">&.</span><span class="sxs-lookup"><span data-stu-id="c2b5c-176">c.</span></span> <span data-ttu-id="c2b5c-177">통계를 표시 하는 각 검색에 대 한 열이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c2b5c-177">There are columns for each search that you're displaying statistics for.</span></span> <span data-ttu-id="c2b5c-178">이 열에는 각 콘텐츠 위치의 검색 쿼리와 일치 하는 항목의 수와 총 크기가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c2b5c-178">This column shows the number (and total size) of items that match the search query in each content location.</span></span> <span data-ttu-id="c2b5c-179">여러 검색에 대 한 통계를 표시 하는 경우이 열에서 "NA"는 콘텐츠 위치가 해당 검색에 포함 되지 않았음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="c2b5c-179">Note that when you're displaying statistics for multiple searches, the "NA" in this column indicates that the content location wasn't included in that search.</span></span> 

## <a name="get-keyword-statistics-for-content-searches"></a><span data-ttu-id="c2b5c-180">콘텐츠 검색에 대 한 키워드 통계 가져오기</span><span class="sxs-lookup"><span data-stu-id="c2b5c-180">Get keyword statistics for Content Searches</span></span>

<span data-ttu-id="c2b5c-181">앞에서 설명한 것 처럼, **쿼리** 페이지에는 검색 쿼리와 쿼리와 일치 하는 항목의 수와 크기가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c2b5c-181">As previous explained, the **Queries** page shows the search query and the number (and size) of items that match the query.</span></span> <span data-ttu-id="c2b5c-182">검색 쿼리를 만들거나 편집할 때 키워드 목록을 사용 하는 경우 각 키워드나 키워드 구와 일치 하는 항목 수를 보여 주는 통계를 향상 시킬 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c2b5c-182">If you use a keyword list when you create or edit a search query, you can get enhanced statistics that show how many items match each keyword or keyword phrase.</span></span> <span data-ttu-id="c2b5c-183">이를 통해 가장 (및 최소) 쿼리 부분을 빠르게 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c2b5c-183">This can help you quickly identify which parts of the query are the most (and least) effective.</span></span> <span data-ttu-id="c2b5c-184">예를 들어 키워드에서 많은 수의 항목을 반환 하는 경우 키워드 쿼리를 구체화 하 여 검색 결과의 범위를 좁힐 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c2b5c-184">For example, if a keyword returns a large number of items, you might choose to refine the keyword query to narrow the search results.</span></span> <span data-ttu-id="c2b5c-185">콘텐츠 검색을 만들거나 편집할 때 키워드 목록을 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c2b5c-185">You can set up a keyword list when you create or edit a Content Search.</span></span> 


<span data-ttu-id="c2b5c-186">콘텐츠 검색에 대 한 키워드 목록을 만들고 키워드 통계를 보려면:</span><span class="sxs-lookup"><span data-stu-id="c2b5c-186">To create a keyword list and view keyword statistics for a Content Search:</span></span>
  
1. <span data-ttu-id="c2b5c-187">보안 & 준수 센터에서 **검색** \> **콘텐츠 검색**으로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2b5c-187">In the Security & Compliance Center, go to **Search** \> **Content search**.</span></span>
    
2. <span data-ttu-id="c2b5c-188">콘텐츠 검색 목록에서 및 검색을 클릭 하 고 편집 아이콘](media/ebd260e4-3556-4fb0-b0bb-cc489773042c.gif) **편집** ![을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2b5c-188">In the list of Content Searches, click and a search, and then click **Edit** ![Edit icon](media/ebd260e4-3556-4fb0-b0bb-cc489773042c.gif).</span></span>
    
3. <span data-ttu-id="c2b5c-189">**쿼리** 를 클릭 하 고 다음 작업을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2b5c-189">Click **Query** and then do the following things:</span></span> 
    
    ![키워드 목록 표시 확인란을 클릭 하 고 각 행에 키워드를 입력 합니다.](media/73ef46dd-3d5c-415d-b5e7-c3559caaafe2.png)
  
    <span data-ttu-id="c2b5c-191">위한.</span><span class="sxs-lookup"><span data-stu-id="c2b5c-191">a.</span></span> <span data-ttu-id="c2b5c-192">**키워드 목록 표시** 확인란을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2b5c-192">Click the **Show keyword list** check box.</span></span> 
    
    <span data-ttu-id="c2b5c-193">b.</span><span class="sxs-lookup"><span data-stu-id="c2b5c-193">b.</span></span> <span data-ttu-id="c2b5c-194">키워드 테이블의 행에 키워드나 키워드 단계를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2b5c-194">Type a keyword or keyword phase in a row in the keywords table.</span></span> <span data-ttu-id="c2b5c-195">예를 들어 첫 번째 행에 **예산을** 입력 한 다음 두 번째 행에 **security** 를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2b5c-195">For example, type **budget** in the first row and then type **security** in the second row.</span></span> 
    
4. <span data-ttu-id="c2b5c-196">검색 하려는 키워드를 추가 하 고 통계를 가져오려면 **검색** 을 클릭 하 여 수정 된 검색을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2b5c-196">After adding the keywords that you want to search and get statistics for, click **Search** to run the revised search.</span></span> 
    
5. <span data-ttu-id="c2b5c-197">검색이 완료 되 면 검색 목록에서 검색을 선택 하 고 **검색 통계** ![검색 통계 단추](media/9bf56d43-25bf-4f53-a4be-f4d55102310c.png)를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2b5c-197">When the search is completed, select it in the list of searches, and then click **Search statistics** ![Search Statistics button](media/9bf56d43-25bf-4f53-a4be-f4d55102310c.png).</span></span> <span data-ttu-id="c2b5c-198">또한 여러 검색에 대 한 키워드 통계를 표시 하 고 비교할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c2b5c-198">You can also display and compare keyword statistics for multiple searches.</span></span>
    
6. <span data-ttu-id="c2b5c-199">**검색 통계** 페이지에서 **쿼리** 를 클릭 하 여 선택한 검색에 대 한 키워드 통계를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2b5c-199">On the **Search statistics** page, click **Query** to display the keyword statistics for the selected searches.</span></span> 
    
    ![선택한 검색의 각 키워드에 대 한 통계가 표시 됩니다.](media/e7910fa9-af93-4df9-92d0-e1e3e089e14f.png)
  
    <span data-ttu-id="c2b5c-201">이전 스크린샷에 표시 된 것 처럼 각 키워드에 대 한 통계가 표시 됩니다. 여기에는 다음이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c2b5c-201">As shown in the previous screenshot, the statistics for each keyword are displayed; this includes:</span></span> 
    
    - <span data-ttu-id="c2b5c-202">검색에 포함 된 각 콘텐츠 위치 유형의 키워드 통계입니다.</span><span class="sxs-lookup"><span data-stu-id="c2b5c-202">The keyword statistics for each type of content location included in the search.</span></span>
    
    - <span data-ttu-id="c2b5c-203">각 키워드에 대 한 실제 검색 쿼리는 검색 쿼리의 모든 조건을 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2b5c-203">The actual search query for each keyword, which includes any conditions from the search query.</span></span> 
    
    - <span data-ttu-id="c2b5c-204">전체 검색 쿼리 ( **파트** 열에서 **기본** 으로 식별 됨) 및 전체 쿼리에 대 한 통계입니다.</span><span class="sxs-lookup"><span data-stu-id="c2b5c-204">The complete search query (identified as **Primary** in the **Part** column) and the statistics for the complete query.</span></span> <span data-ttu-id="c2b5c-205">참고이 통계는 **요약** 페이지에 표시 되는 것과 동일 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2b5c-205">Note these are the same statistics displayed on the **Summary** page.</span></span> 

> [!NOTE]
> <span data-ttu-id="c2b5c-206">큰 키워드 목록으로 인해 발생 하는 문제를 줄이기 위해 이제는 검색 쿼리의 키워드 목록에서 최대 20 개의 행으로 제한 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c2b5c-206">To help reduce issues caused by large keyword lists, you're now limited to a maximum of 20 rows in the keyword list of a search query.</span></span>
