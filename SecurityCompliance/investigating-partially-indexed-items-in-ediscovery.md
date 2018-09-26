---
title: Office 365 eDiscovery에서 부분적으로 인덱싱된 항목 조사
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 1/26/2018
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid: MOE150
ms.assetid: 4e8ff113-6361-41e2-915a-6338a7e2a1ed
description: 부분적으로 인덱싱된 항목 (도 통화는 인덱싱되지 않은 항목)은 Exchange 사서함 항목 및 SharePoint에서 문서 및 일부 오류로 콘텐츠 검색을 위해 인덱싱되 완전히 받지 용 OneDrive 사이트는 합니다. 이 문서에서 항목 검색에 대 한 인덱싱할 수 없는 이유 및 부분적으로 인덱싱된 항목으로 반환 됩니다, 부분적으로 인덱싱된 항목에 대 한 검색 오류를 식별 및 내용은 PowerShell 스크립트를 사용 하 여 인덱싱된 부분적으로 전자 메일에 대 한 조직의 노출 결정 항목입니다.
ms.openlocfilehash: 98f794e80ea8a6016887ff139bc5b546c438f093
ms.sourcegitcommit: 7956955cd919f6e00b64e4506605a743c5872549
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/26/2018
ms.locfileid: "25038081"
---
# <a name="investigating-partially-indexed-items-in-office-365-ediscovery"></a><span data-ttu-id="deb92-104">Office 365 eDiscovery에서 부분적으로 인덱싱된 항목 조사</span><span class="sxs-lookup"><span data-stu-id="deb92-104">Investigating partially indexed items in Office 365 eDiscovery</span></span>

<span data-ttu-id="deb92-p102">Office 365 보안에서 실행 하는 콘텐츠 검색 &amp; 준수 센터 검색을 실행 하는 경우 예상된 검색 결과에 부분적으로 인덱싱된 항목 자동으로 포함 합니다. 부분적으로 인덱싱된 항목은 Exchange 사서함 항목 및 어떤 이유로 검색을 위해 인덱싱되 완전히 받지는 비즈니스 사이트에 대 한 SharePoint OneDrive에 있는 문서입니다. [전자 메일 메시지에 대 한 인덱싱 제한](limits-for-content-search.md#indexinglimits)에 속하는 때문에 대부분의 전자 메일 메시지와 사이트 문서 인덱스 성공적으로 됩니다. 그러나 일부 항목은 이러한 인덱싱 제한을 초과할 수 고 부분적으로 인덱싱할 합니다. 항목 검색에 대 한 인덱싱할 수 없는 및 콘텐츠 검색을 실행 하는 경우 부분적으로 인덱싱된 항목으로 반환 되는 다른 이유는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="deb92-p102">A Content Search that you run from the Office 365 Security &amp; Compliance Center automatically includes partially indexed items in the estimated search results when you run a search. Partially indexed items are Exchange mailbox items and documents on SharePoint and OneDrive for Business sites that for some reason weren't completely indexed for search. Most email messages and site documents are successfully indexed because they fall within the [Indexing limits for email messages](limits-for-content-search.md#indexinglimits). However, some items may exceed these indexing limits, and will be partially indexed. Here are other reasons why items can't be indexed for search and are returned as partially indexed items when you run a Content Search:</span></span>
  
- <span data-ttu-id="deb92-110">전자 메일 메시지는; 인덱싱할 수 없는 파일 형식의 첨부 파일 대부분의 경우에는 파일 형식이 [인식할 수 없거나 인덱싱에 대 한 지원 되지않는](partially-indexed-items-in-content-search.md#file-types-not-indexed-for-search)</span><span class="sxs-lookup"><span data-stu-id="deb92-110">Email messages have an attached file of a file type that can't be indexed; in most cases, the file type is [unrecognized or unsupported for indexing](partially-indexed-items-in-content-search.md#file-types-not-indexed-for-search)</span></span>
    
- <span data-ttu-id="deb92-111">전자 메일 메시지 예: 이미지 파일, 유효한 처리기를 없이 첨부 파일 포함 이것은 부분적으로 인덱싱된 전자 메일 항목의 가장 일반적인 원인</span><span class="sxs-lookup"><span data-stu-id="deb92-111">Email messages have an attached file without a valid handler, such as image files; this is the most common cause of partially indexed email items</span></span>
    
- <span data-ttu-id="deb92-112">전자 메일 메시지에 첨부 된 너무 많은 파일</span><span class="sxs-lookup"><span data-stu-id="deb92-112">Too many files attached to an email message</span></span>
    
- <span data-ttu-id="deb92-113">전자 메일 메시지에 첨부 파일이 너무 큽니다.</span><span class="sxs-lookup"><span data-stu-id="deb92-113">A file attached to an email message is too large</span></span>
    
- <span data-ttu-id="deb92-114">파일 형식 인덱싱은 지원 되지만 특정 파일에 대 한 인덱싱 오류가 발생 했습니다.</span><span class="sxs-lookup"><span data-stu-id="deb92-114">The file type is supported for indexing but an indexing error occurred for a specific file</span></span>
    
<span data-ttu-id="deb92-p103">해당 달라 집니다 대부분의 Office 365 조직 고객 되어 있지만 콘텐츠의 1% 미만 볼륨 및 콘텐츠의 12% 미만으로 부분적으로 인덱싱되는 크기에 따라. 크기를 비교 하 여 볼륨 간의 차이 대 한 설명 더 큰 파일 완전히 인덱싱할 수 없는 콘텐츠를 포함 하는 더 높은 확률입니다.</span><span class="sxs-lookup"><span data-stu-id="deb92-p103">Although it varies, most Office 365 organizations customers have less than 1% of content by volume and less than 12% of content by size that is partially indexed. The reason for the difference between the volume versus size is that larger files have a higher probability of containing content that can't be completely indexed.</span></span>
  
## <a name="why-does-the-partially-indexed-item-count-change-for-a-search"></a><span data-ttu-id="deb92-117">검색에 대 한 부분적으로 인덱싱된 항목 수 변경 하는 이유</span><span class="sxs-lookup"><span data-stu-id="deb92-117">Why does the partially indexed item count change for a search?</span></span>

<span data-ttu-id="deb92-p104">Office 365 보안에서 콘텐츠 검색을 실행 하 고 나면 &amp; 총 수와 검색 된 위치에 부분적으로 인덱싱된 항목의 크기, 준수 센터에 대 한 자세한 통계에 표시 되는 검색 결과 통계에 나열 된 검색 합니다. Note 이러한 *인덱싱되지 않은 항목* 검색 통계에서의 연결을 이라고 합니다. 다음은 검색 결과에 반환 되는 부분적으로 인덱싱된 항목 수에 영향을 주는 몇가지 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="deb92-p104">After you run a Content Search in the Office 365 Security &amp; Compliance Center, the total number and size of partially indexed items in the locations that were searched are listed in the search result statistics that are displayed in the detailed statistics for the search. Note these are called  *unindexed items*  in the search statistics. Here are a few things that will affect the number of partially indexed items that are returned in the search results:</span></span> 
  
- <span data-ttu-id="deb92-p105">항목은 부분적으로 인덱싱되는 항목과 일치 하는 검색 쿼리를 하는 경우 count (와 크기)의 검색 결과 항목과 부분적으로 인덱싱된 항목에 포함 됩니다. 그러나 해당 같은 검색의 결과 내보낼 때 항목은 검색 결과; 집합에만 포함 부분적으로 인덱싱된 항목으로 포함 하지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="deb92-p105">If an item is partially indexed and matches the search query, it's included in both the count (and size) of search result items and partially indexed items. However, when the results of that same search are exported, the item is included only with set of search results; it's not included as a partially indexed item.</span></span>
    
- <span data-ttu-id="deb92-p106">(키워드 쿼리에 포함) 또는 사용 하 여 조건을 검색 쿼리에 대 한 날짜 범위를 지정 하면 날짜 범위와 일치 하지 않는 모든 부분적으로 인덱싱된 항목 부분적으로 인덱싱된 항목 수에 포함 되지 않습니다. 부분적으로 인덱싱된 항목 날짜 범위 내에 속하는 부분적으로 인덱싱된 항목 수에 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="deb92-p106">If you specify a date range for a search query (by including it in the keyword query or by using a condition), any partially indexed item that doesn't match the date range isn't included in the count of partially indexed items. Only the partially indexed items that fall within date range are included in the count of partially indexed items.</span></span>
    
 <span data-ttu-id="deb92-p107">**참고:** SharePoint에 있는 부분적으로 인덱싱된 항목을 선택 하 고 OneDrive 사이트는 *아닌* 검색에 대 한 자세한 통계에 표시 되는 부분적으로 인덱싱된 항목의 예상에 포함 합니다. 그러나 콘텐츠 검색의 결과 내보낼 때 부분적으로 인덱싱된 항목을 내보낼 수 있습니다. 예, 검색 하는 경우만 사이트 콘텐츠 검색, 예상된 수에에서 부분적으로 인덱싱된 항목에 0이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="deb92-p107">**Note:** Partially indexed items located in SharePoint and OneDrive sites  *are not*  included in the estimate of partially indexed items that's displayed in the detailed statistics for the search. However, partially indexed items can be exported when you export the results of a Content Search. For example, if you only search sites in a Content Search, the estimated number partially indexed items will be zero.</span></span> 
  
## <a name="calculating-the-ratio-of-partially-indexed-items-in-your-organization"></a><span data-ttu-id="deb92-128">조직에서 부분적으로 인덱싱된 항목의 비율을 계산</span><span class="sxs-lookup"><span data-stu-id="deb92-128">Calculating the ratio of partially indexed items in your organization</span></span>

<span data-ttu-id="deb92-p108">부분적으로 인덱싱된 항목에 대 한 조직의 노출을 이해 하려면 (빈 키워드 쿼리를 사용 하 여) 하 여 모든 사서함에 있는 모든 콘텐츠에 대 한 검색을 실행할 수 있습니다. 아래의 다음 예제는 56,208 (4,830 MB) 완벽 하 게 인덱싱된 항목 및 470 (316 MB) 부분적으로 인덱싱된 항목입니다.</span><span class="sxs-lookup"><span data-stu-id="deb92-p108">To understand your organization's exposure to partially indexed items, you can run a search for all content in all mailboxes (by using a blank keyword query). In the following example below, there are 56,208 (4,830 MB) fully indexed items and 470 (316 MB) partially indexed items.</span></span>
  
![부분적으로 인덱싱된 항목 검색 통계 표시의 예](media/0f6a5cf7-4c98-44a0-a0dd-5aed67124641.png)
  
<span data-ttu-id="deb92-132">다음 계산을 사용 하 여 부분적으로 인덱싱된 항목의 백분율을 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="deb92-132">You can determine the percentage of partially indexed items by using the following calculations.</span></span>
  
 <span data-ttu-id="deb92-133">**조직에서 부분적으로 인덱싱된 항목의 비율을 계산 합니다.**</span><span class="sxs-lookup"><span data-stu-id="deb92-133">**To calculate the ratio of partially indexed items in your organization:**</span></span>

`(Total number of partially indexed items/Total number of items) x 100`


`(470/56,208) x 100 = 0.84%`
 
<span data-ttu-id="deb92-134">이전 예제에서 검색 결과 사용 하 여. 모든 사서함 항목의 84% 부분적으로 인덱싱됩니다.</span><span class="sxs-lookup"><span data-stu-id="deb92-134">By using the search results from the previous example, .84% of all mailboxes items are partially indexed.</span></span>
  
 <span data-ttu-id="deb92-135">**조직에서 부분적으로 인덱싱된 항목의 크기의 백분율을 계산 합니다.**</span><span class="sxs-lookup"><span data-stu-id="deb92-135">**To calculate the percentage of the size of partially indexed items in your organization:**</span></span>

`(Size of all partially indexed items/Size of all items) x 100`

`(316 MB/4830 MB) x 100 = 6.54%`

<span data-ttu-id="deb92-p109">따라서 앞의 예제에서는 사서함 항목의 총 크기의 6.54% 부분적으로 인덱싱된 항목에서 됩니다. 듯이 대부분의 Office 365 조직에서는 고객 볼륨 및 콘텐츠의 12% 미만으로 부분적으로 인덱싱되는 크기에 따라 콘텐츠의 1% 미만가지고 있습니다.</span><span class="sxs-lookup"><span data-stu-id="deb92-p109">So in the previous example, 6.54% of the total size of mailbox items are from partially indexed items. As previously stated, most Office 365 organizations customers have less than 1% of content by volume and less than 12% of content by size that is partially indexed.</span></span>

## <a name="working-with-partially-indexed-items"></a><span data-ttu-id="deb92-138">인덱싱된 항목 사용 (영문) 부분적으로</span><span class="sxs-lookup"><span data-stu-id="deb92-138">Working with partially indexed items</span></span>

<span data-ttu-id="deb92-p110">경우에는 관련 정보를 포함 하지, [콘텐츠 검색 보고서를 내보낼](export-a-content-search-report.md) 수의 유효성을 검사 하는 항목을 부분적으로 검사 해야 하는 부분적으로 인덱싱된 항목에 대 한 정보가 들어 있습니다. 콘텐츠 검색 보고서를 내보낼 때 부분적으로 인덱싱된 항목을 포함 하는 내보내기 옵션 중 하나를 선택 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="deb92-p110">In cases when you need to examine partially items to validate that they don't contain relevant information, you can [export a content search report](export-a-content-search-report.md) that contains information about partially indexed items. When you export a content search report, be sure to choose one of the export options that includes partially indexed items.</span></span> 
  
![부분적으로 인덱싱된 항목을 내보내는 데 두번째 또는 세번째 옵션 선택](media/624a62b4-78f7-4329-ab5d-e62e3b369885.png)
  
<span data-ttu-id="deb92-p111">콘텐츠 검색 결과 또는 이러한 옵션 중 하나를 사용 하 여 콘텐츠 검색 보고서를 내보낼 때 내보내기 인덱싱되지 않은 Items.csv 라는 보고서를 포함 합니다. 이 보고서에는 대부분의 ResultsLog.csv 파일로 동일한 정보가 포함 됩니다. 그러나, 인덱싱되지 않은 Items.csv 파일도 포함 되어 부분적으로 인덱싱된 항목에 관련 된 두 필드: **오류 태그** 및 **오류 속성**입니다. 이러한 필드는 각 부분적으로 인덱싱된 항목에 대 한 인덱싱 오류에 대 한 정보를 포함 합니다. 두 필드에 정보를 사용 하 여 특정 작업에 대해 인덱싱 오류 검사 영향을 주는 여부 결정 하는데 도움이 수 있습니다. 않으면 대상된 콘텐츠 검색을 수행 하 고 검색 및 내보내기 있습니다 특정 전자 메일 메시지와 SharePoint 또는 OneDrive 문서 하 여 조사 관련는 결정를 검토할 수 있습니다. 단계별 지침은 [준비 Office 365에서 대상으로 지정 된 콘텐츠 검색에 대 한 CSV 파일을](csv-file-for-an-id-list-content-search.md)참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="deb92-p111">When you export content search results or a content search report using one of these options, the export includes a report named Unindexed Items.csv. This report includes most of the same information as the ResultsLog.csv file; however, the Unindexed Items.csv file also includes two fields related to partially indexed items: **Error Tags** and **Error Properties**. These fields contain information about the indexing error for each partially indexed item. Using the information in these two fields can help you determine whether or not the indexing error for a particular impacts your investigation. If it does, you can perform a targeted content search and retrieve and export specific email messages and SharePoint or OneDrive documents so that you can examine them to determine if they're relevant to your investigation. For step-by-step instructions, see [Prepare a CSV file for a targeted Content Search in Office 365](csv-file-for-an-id-list-content-search.md).</span></span>
  
 <span data-ttu-id="deb92-p112">**참고:** 인덱싱되지 않은 Items.csv 파일에는 **오류 유형** 및 **오류 메시지**를 이라는 필드가 들어 있습니다. 이들은 덜 자세한 정보 만한 **오류 태그** 및 **오류 속성** 필드의 정보를 비슷한 정보를 포함 하는 레거시 필드입니다. 레거시 이러한 필드는 무시 해도 됩니다.</span><span class="sxs-lookup"><span data-stu-id="deb92-p112">**Note:** The Unindexed Items.csv file also contains fields named **Error Type** and **Error Message**. These are legacy fields that contain information that is similar to the information in the **Error Tags** and **Error Properties** fields, but with less detailed information. You can safely ignore these legacy fields.</span></span> 
  
## <a name="errors-related-to-partially-indexed-items"></a><span data-ttu-id="deb92-151">부분적으로 인덱싱된 항목에 관련 된 오류</span><span class="sxs-lookup"><span data-stu-id="deb92-151">Errors related to partially indexed items</span></span>

<span data-ttu-id="deb92-p113">오류 태그 정보, 오류 및 파일 형식의 두 부분으로 이루어져 있습니다. 이 오류/filetype 쌍의 예:</span><span class="sxs-lookup"><span data-stu-id="deb92-p113">Error tags are made up of two pieces of information, the error and the file type. For example, in this error/filetype pair:</span></span>

```
 parseroutputsize_xls
```

   
 <span data-ttu-id="deb92-p114">`parseroutputsize`발생 한 오류 및 `xls` 에서 오류가 발생 한 파일의 파일 유형입니다. 파일 형식을 인식 되지 않은 또는 파일 형식이 지정 되었습니다 된 경우에는 적용 되지 않습니다 값을 참조 하는 오류가 발생 합니다. `noformat` 파일 형식을 대신 합니다.</span><span class="sxs-lookup"><span data-stu-id="deb92-p114">`parseroutputsize` is the error and  `xls` is the file type of the file the error occurred on. In cases were the file type wasn't recognized or the file type was doesn't apply to the error, you will see the value  `noformat` in place of the file type.</span></span> 
  
<span data-ttu-id="deb92-156">다음은 오류 및 오류의 가능한 원인에 대 한 설명을 인덱싱의 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="deb92-156">The following is a list of indexing errors and a description of the possible cause of the error.</span></span>
  
|<span data-ttu-id="deb92-157">**오류 태그**</span><span class="sxs-lookup"><span data-stu-id="deb92-157">**Error tag**</span></span>|<span data-ttu-id="deb92-158">**설명**</span><span class="sxs-lookup"><span data-stu-id="deb92-158">**Description**</span></span>|
|:-----|:-----|
| `attachmentcount` <br/> |<span data-ttu-id="deb92-159">처리 되지 않은 이러한 첨부 파일의 일부 고 전자 메일 메시지에 너무 많은 경우 첨부 파일 해야 했습니다.</span><span class="sxs-lookup"><span data-stu-id="deb92-159">An email message had too many attachments, and some of these attachments weren't processed.</span></span>  <br/> |
| `attachmentdepth` <br/> |<span data-ttu-id="deb92-p115">콘텐츠 검색기 및 문서 파서 발견 다른 첨부 파일 내에 중첩 된 첨부 파일의 수준이 너무 많습니다. 이러한 첨부 파일 중 일부는 처리 되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="deb92-p115">The content retriever and document parser found too many levels of attachments nested inside other attachments. Some of these attachments were not processed.</span></span>  <br/> |
| `attachmentrms` <br/> |<span data-ttu-id="deb92-162">첨부 파일 디코딩 RMS로 보호 되는 것이 되었기 때문에 실패 했습니다.</span><span class="sxs-lookup"><span data-stu-id="deb92-162">An attachment failed decoding because it was RMS-protected.</span></span>  <br/> |
| `attachmentsize` <br/> |<span data-ttu-id="deb92-163">전자 메일 메시지에 첨부 파일을 너무 커서 및 처리할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="deb92-163">A file attached to an email message was too large and couldn't be processed.</span></span>  <br/> |
| `indexingtruncated` <br/> |<span data-ttu-id="deb92-p116">인덱스에 처리 된 전자 메일 메시지를 작성할 때이 너무 커서 인덱싱할 수 속성 중 하나 및 잘렸습니다. 잘린된 속성 오류 속성 필드에 나열 됩니다.</span><span class="sxs-lookup"><span data-stu-id="deb92-p116">When writing the processed email message to the index, one of the indexable properties was too large and was truncated. The truncated properties are listed in Error Properties field.</span></span>  <br/> |
| `invalidunicode` <br/> |<span data-ttu-id="deb92-p117">전자 메일 메시지 유효한 유니코드도 처리할 수 없고 텍스트를 포함 합니다. 이 항목에 대 한 인덱싱 완료 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="deb92-p117">An email message contained text that couldn't be processed as valid Unicode. Indexing for this item may be incomplete.</span></span>  <br/> |
| `parserencrypted` <br/> |<span data-ttu-id="deb92-168">첨부 파일 또는 전자 메일 메시지의 콘텐츠를 암호화 하 고 Office 365의 콘텐츠를 디코딩할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="deb92-168">The content of attachment or email message is encrypted, and Office 365 couldn't decode the content.</span></span>  <br/> |
| `parsererror` <br/> |<span data-ttu-id="deb92-p118">구문 분석 하는 동안 알 수 없는 오류가 발생 했습니다. 이 일반적으로 소프트웨어 버그 또는 서비스 크래시에서 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="deb92-p118">An unknown error occurred during parsing. This typically results from a software bug or a service crash.</span></span>  <br/> |
| `parserinputsize` <br/> |<span data-ttu-id="deb92-171">첨부 파일을 처리 하기 위해 파서 너무 큽니다 및 발생 하지 않았으므로 해당 첨부 파일을 구문 분석 또는 완료할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="deb92-171">An attachment was too large for the parser to handle, and the parsing of that attachment didn't happen or wasn't completed.</span></span>  <br/> |
| `parsermalformed` <br/> |<span data-ttu-id="deb92-p119">첨부 파일 형식이 잘못 되었습니다 및 파서 처리할 수 없습니다. 이 결과 수 있는 이전 파일에서 서식을 호환 되지않는 소프트웨어 또는 바이러스를 요구 하는 외에 다른 수를 가장 하 여 만든 파일입니다.</span><span class="sxs-lookup"><span data-stu-id="deb92-p119">An attachment was malformed and couldn't be handled by the parser. This result from can old file formats, files created by incompatible software, or viruses pretending to be something other than claimed.</span></span>  <br/> |
| `parseroutputsize` <br/> |<span data-ttu-id="deb92-174">첨부 파일을 구문 분석에서 출력 너무 커서 및 잘릴 수 있었습니다.</span><span class="sxs-lookup"><span data-stu-id="deb92-174">The output from the parsing of an attachment was too large and had to be truncated.</span></span>  <br/> |
| `parserunknowntype` <br/> |<span data-ttu-id="deb92-175">첨부 파일에는 Office 365 검색할 수 없는 파일 형식을 했습니다.</span><span class="sxs-lookup"><span data-stu-id="deb92-175">An attachment had a file type that Office 365 couldn't detect.</span></span>  <br/> |
| `parserunsupportedtype` <br/> |<span data-ttu-id="deb92-176">첨부 파일에는 Office 365could 감지 하 고 해당 파일 형식을 구문 분석할 수 없습니다 파일 형식을 했습니다.</span><span class="sxs-lookup"><span data-stu-id="deb92-176">An attachment had a file type that Office 365could detect, but parsing that file type isn't supported.</span></span>  <br/> |
| `propertytoobig` <br/> |<span data-ttu-id="deb92-p120">전자 메일 속성의 값 Exchange 저장소 너무 커서 검색할 수 없는 되었으며 메시지를 처리할 수 없습니다. 이 일반적으로 수행 되는 전자 메일 메시지의 본문 속성에 해당 합니다.</span><span class="sxs-lookup"><span data-stu-id="deb92-p120">The value of an email property in Exchange Store was too large to be retrieved and the message couldn't be processed. This typically only happens to the body property of an email message.</span></span>  <br/> |
| `retrieverrms` <br/> |<span data-ttu-id="deb92-179">RMS로 보호 된 메시지를 디코딩할 콘텐츠 검색기 하지 못했습니다.</span><span class="sxs-lookup"><span data-stu-id="deb92-179">The content retriever failed to decode an RMS-protected message.</span></span>  <br/> |
| `wordbreakertruncated` <br/> |<span data-ttu-id="deb92-p121">너무 많은 단어를 인덱싱하는 동안 다음은 문서에서 확인 했습니다. 제한에 도달 하면 속성은 처리를 중지 하 고 속성은 잘립니다.</span><span class="sxs-lookup"><span data-stu-id="deb92-p121">Too many words were identified in the document during indexing. Processing of the property stopped when reaching the limit, and the property is truncated.</span></span>  <br/> |
   
<span data-ttu-id="deb92-p122">오류 필드에서는 오류 태그 필드에 나열 된 처리 오류에 있는 필드 미치는 영향에 대해 설명 합니다. 와 같은 속성을 검색 하는 경우 `subject` 또는 `participants`, 오류 메시지의 본문에 검색 결과 영향을 줄 되지 않습니다. 이 더 자세히 조사 해야할 부분적으로 인덱싱된 항목 정확 하 게 결정할 때 유용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="deb92-p122">Error fields describe which fields are affected by the processing error listed in the Error Tags field. If you're searching a property such as  `subject` or  `participants`, errors in the body of the message won't impact the results of your search. This can be useful when determining exactly which partially indexed items you might need to further investigate.</span></span>
  
## <a name="using-a-powershell-script-to-determine-your-organizations-exposure-to-partially-indexed-email-items"></a><span data-ttu-id="deb92-185">PowerShell 스크립트를 사용 하 여 인덱싱된 부분적으로 전자 메일 항목에 대 한 조직의 노출을 확인 하려면</span><span class="sxs-lookup"><span data-stu-id="deb92-185">Using a PowerShell script to determine your organization's exposure to partially indexed email items</span></span>

<span data-ttu-id="deb92-p123">다음 단계에서는 모든 Exchange 사서함에 있는 모든 항목을 검색 하 고 다음 (개수 및 크기) 부분적으로 인덱싱된 전자 메일 항목의 경우 조직의 비율에 대 한 보고서를 생성 하 고 항목 수를 표시 하는 PowerShell 스크립트를 실행 하는 방법 설명 (및 해당 파일 형식을) 발생 하는 각 인덱싱 오류에 대 한 합니다. 이전 섹션에서 오류 태그 설명을 사용 하 여 인덱싱 오류를 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="deb92-p123">The following steps show you how to run a PowerShell script that searches for all items in all Exchange mailboxes, and then generates a report about your organization's ratio of partially indexed email items (by count and by size) and displays the number of items (and their file type) for each indexing error that occurs. Use the error tag descriptions in the previous section to identify the indexing error.</span></span>
  
1. <span data-ttu-id="deb92-188">.Ps1 파일 이름 접미사를 사용 하 여 Windows PowerShell 스크립트 파일에 다음 텍스트를 저장 예, `PartiallyIndexedItems.ps1`합니다.</span><span class="sxs-lookup"><span data-stu-id="deb92-188">Save the following text to a Windows PowerShell script file by using a filename suffix of .ps1; for example, `PartiallyIndexedItems.ps1`.</span></span>

```
  write-host "**************************************************"
  write-host "     Office 365 Security &amp; Compliance Center      " -foregroundColor yellow -backgroundcolor darkgreen
  write-host "   eDiscovery Partially Indexed Item Statistics   " -foregroundColor yellow -backgroundcolor darkgreen
  write-host "**************************************************"
  " " 
  # Create a search with Error Tags Refinders enabled
  Remove-ComplianceSearch "RefinerTest" -Confirm:$false -ErrorAction 'SilentlyContinue'
  New-ComplianceSearch -Name "RefinerTest" -ContentMatchQuery "size>0" -RefinerNames ErrorTags -ExchangeLocation ALL
  Start-ComplianceSearch "RefinerTest"
  # Loop while search is in progress
  do{
      Write-host "Waiting for search to complete..."
      Start-Sleep -s 5
      $complianceSearch = Get-ComplianceSearch "RefinerTest"
  }while ($complianceSearch.Status -ne 'Completed')
  $refiners = $complianceSearch.Refiners | ConvertFrom-Json
  $errorTagProperties = $refiners.Entries | Get-Member -MemberType NoteProperty
  $partiallyIndexedRatio = $complianceSearch.UnindexedItems / $complianceSearch.Items
  $partiallyIndexedSizeRatio = $complianceSearch.UnindexedSize / $complianceSearch.Size
  " "
  "===== Partially indexed items ====="
  "         Total          Ratio"
  "Count    {0:N0}{1:P2}" -f $complianceSearch.Items.ToString("N0").PadRight(15, " "), $partiallyIndexedRatio
  "Size(GB) {0:N2}{1:P2}" -f ($complianceSearch.Size / 1GB).ToString("N2").PadRight(15, " "), $partiallyIndexedSizeRatio
  " "
  Write-Host ===== Reasons for partially indexed items =====
  foreach($errorTagProperty in $errorTagProperties)
  {
      $name = $refiners.Entries.($errorTagProperty.Name).Name
      $count = $refiners.Entries.($errorTagProperty.Name).TotalCount
      $frag = $name.Split("{_}")
      $errorTag = $frag[0]
      $fileType = $frag[1]
      if ($errorTag -ne $lastErrorTag)
      {
          $errorTag
      }
      "    " + $fileType + " => " + $count
      $lastErrorTag = $errorTag
  }
  
```
   
2. <span data-ttu-id="deb92-189">[Office 365 보안 연결할 &amp; 준수 센터 PowerShell](https://go.microsoft.com/fwlink/p/?linkid=627084)합니다.</span><span class="sxs-lookup"><span data-stu-id="deb92-189">[Connect to Office 365 Security &amp; Compliance Center PowerShell](https://go.microsoft.com/fwlink/p/?linkid=627084).</span></span>
    
3. <span data-ttu-id="deb92-190">보안에서 &amp; 준수 센터 PowerShell 1 단계에서 스크립트를 저장 위치 폴더로 이동 하 고, 스크립트를 실행 하는 다음 예를 들어:</span><span class="sxs-lookup"><span data-stu-id="deb92-190">In Security &amp; Compliance Center PowerShell, go to the folder where you saved the script in step 1, and then run the script; for example:</span></span>

    ```
    .\PartiallyIndexedItems.ps1
    ```
   
<span data-ttu-id="deb92-191">다음은 한 예 중 스크립트에 의해 반환 되는 출력 합니다.</span><span class="sxs-lookup"><span data-stu-id="deb92-191">Here's an example fo the output returned by the script.</span></span>
  
![부분적으로 인덱싱된 전자 메일 항목에 대 한 조직의 노출에 대 한 보고서를 생성 하는 스크립트에서 출력의 예](media/aeab5943-c15d-431a-bdb2-82f135abc2f3.png)
  
<span data-ttu-id="deb92-193">다음에 유의하세요.</span><span class="sxs-lookup"><span data-stu-id="deb92-193">Note the following:</span></span>
  
1. <span data-ttu-id="deb92-194">총 수와 전자 메일 항목의 크기 및 인덱싱된 부분적으로 전자 메일 항목 (개수 및 크기)의 경우 조직의 비율</span><span class="sxs-lookup"><span data-stu-id="deb92-194">The total number and size of email items, and your organization's ratio of partially indexed email items (by count and by size)</span></span>
    
2. <span data-ttu-id="deb92-195">목록 오류 태그 및 오류가 발생 한 해당 파일 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="deb92-195">A list error tags and the corresponding file types for which the error occurred.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="deb92-196">참고 항목</span><span class="sxs-lookup"><span data-stu-id="deb92-196">See also</span></span>

[<span data-ttu-id="deb92-197">Office 365의 콘텐츠 검색에서 부분적으로 인덱싱된 항목</span><span class="sxs-lookup"><span data-stu-id="deb92-197">Partially indexed items in Content Search in Office 365</span></span>](partially-indexed-items-in-content-search.md)
