---
title: Office 365에서 콘텐츠 검색 하는 ID 목록에 대 한 CSV 파일을 준비
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 3/21/2018
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid: MOE150
ms.assetid: 82c97bb4-2b64-4edc-804d-cedbda525d22
description: 기존 콘텐츠 검색에서 Results.csv 또는 인덱싱되지 않은 Items.csv 파일을 사용 하 여 특정 전자 메일 메시지를 반환 하는 ID 목록 검색을 만들 수 있습니다. ID 목록 검색은 부분적으로 인덱싱된 사서함 항목을 반환 하려면 일반적으로 사용 됩니다.
ms.openlocfilehash: 9a7583c8f83626afb8dc0452bf72d834c8a28275
ms.sourcegitcommit: 7956955cd919f6e00b64e4506605a743c5872549
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/26/2018
ms.locfileid: "25038281"
---
# <a name="prepare-a-csv-file-for-an-id-list-content-search-in-office-365"></a><span data-ttu-id="a7d5b-104">Office 365에서 콘텐츠 검색 하는 ID 목록에 대 한 CSV 파일을 준비</span><span class="sxs-lookup"><span data-stu-id="a7d5b-104">Prepare a CSV file for an ID list Content Search in Office 365</span></span>

<span data-ttu-id="a7d5b-p102">특정 사서함 전자 메일 메시지 및 Exchange Id의 목록을 사용 하 여 다른 사서함 항목을 검색할 수 있습니다. ID 목록 검색 (공식적으로 대상이 지정 된 검색 이라고 함)를 만드는, 특정 사서함 항목에 대 한 검색을 식별 하는 쉼표로 구분 된 값 (CSV) 파일로 전송할 수 있습니다. 이 CSV 파일에 대 한 **Results.csv** 파일 또는 콘텐츠 검색 결과 내보내거나에서 콘텐츠 검색 보고서 및 기존 콘텐츠 검색을 내보낼 때 포함 된 **인덱싱되지 않은 Items.csv** 파일을 사용 합니다. 다음 중 하나를 수정할 이러한 파일을 검색 하 고 다음 새 ID 목록 검색을 만들어 CSV 파일 전송에 특정 항목을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="a7d5b-p102">You can search for specific mailbox email messages and other mailbox items using a list of Exchange IDs. To create an ID list search (formally called a targeted search), you submit a comma separated value (CSV) file that identifies the specific mailbox items to search for. For this CSV file you use the **Results.csv** file or the **Unindexed Items.csv** file that are included when you export the Content Search results or export a Content Search report from and existing Content Search. Then you edit one of these files to indicate the specific items to search for, and then create a new ID list search and submit the CSV file.</span></span> 
  
<span data-ttu-id="a7d5b-109">ID 목록 검색 프로그램을 만들기 위한 프로세스에 대 한 빠른 개요는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="a7d5b-109">Here's a quick overview of the process for creating an ID list search.</span></span>
  
1. <span data-ttu-id="a7d5b-110">쿼리 만들기 및 보안에서 새롭게 제공 되거나 안내식 콘텐츠 검색을 실행 &amp; 준수 센터입니다.</span><span class="sxs-lookup"><span data-stu-id="a7d5b-110">Create and run a new or guided Content Search in the Security &amp; Compliance Center.</span></span>
    
2. <span data-ttu-id="a7d5b-p103">콘텐츠 검색 결과 내보내기 또는 콘텐츠 검색 보고서를 내보냅니다. 자세한 내용은 다음을 참조 합니다.</span><span class="sxs-lookup"><span data-stu-id="a7d5b-p103">Export the content search results or export the content search report. For more information, see:</span></span>
    
    - [<span data-ttu-id="a7d5b-113">Office 365 보안에서 콘텐츠 검색 결과 내보낼 &amp; 준수 센터</span><span class="sxs-lookup"><span data-stu-id="a7d5b-113">Export Content Search results from the Office 365 Security &amp; Compliance Center</span></span>](export-search-results.md)
    
    - [<span data-ttu-id="a7d5b-114">콘텐츠 검색 보고서 내보내기</span><span class="sxs-lookup"><span data-stu-id="a7d5b-114">Export a Content Search report</span></span>](export-a-content-search-report.md)
    
3. <span data-ttu-id="a7d5b-p104">**인덱싱되지 않은 Items.csv** 또는 **Results.csv** 파일을 편집 하 고 ID 목록 검색에 포함 하려는 특정 사서함 항목을 식별 합니다. ID 목록 검색에 대 한 CSV 파일을 준비 하기 위한 [지침](#prepare-the-csv-file-for-an-id-list-search) 을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="a7d5b-p104">Edit the **Results.csv** file or the **Unindexed Items.csv** and identify the specific mailbox items that you want to include in the ID list search. See the [instructions](#prepare-the-csv-file-for-an-id-list-search) for preparing a CSV file for an ID list search.</span></span> 
    
4. <span data-ttu-id="a7d5b-p105">새 ID 목록 만들기 ( [지침](#create-an-id-list-search)을 참조 하십시오.)를 검색 하 고 준비한 CSV 파일에 제출 합니다. 생성 된 검색 쿼리 CSV 파일에서 선택한 항목에 대 한만 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="a7d5b-p105">Create a new ID list search (see the [instructions](#create-an-id-list-search)) and submit the CSV file that you prepared. The search query that's created will only search for the items selected in the CSV file.</span></span>
    
> [!NOTE]
> <span data-ttu-id="a7d5b-p106">사서함 항목에 대 한 ID 목록 검색 에서만 지원 됩니다. SharePoint를 검색할 수 없습니다 및 ID의 OneDrive 문서 목록을 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="a7d5b-p106">ID list searches are only supported for mailbox items. You can't search for SharePoint and OneDrive documents in an ID list search.</span></span> 
  
 <span data-ttu-id="a7d5b-p107">**이유 ID 목록 검색을 만들기?** 항목이 **Results.csv** 또는 **인덱싱되지 않은 Items.csv** 파일에서 메타 데이터에 따라 eDiscovery 요청에 응답 하는 경우는 ID 목록 검색을 사용 하 여 찾을 수 있습니다를 확인할 수 모르는 경우 미리 보기를 한 후에 해당 하는 경우를 확인 하려면 항목을 나타내는 내보내려면 조사 하는 경우에 응답 합니다. ID 목록 검색 검색 하 고 인덱싱되지 않은 항목의 특정 집합을 반환할 일반적으로 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a7d5b-p107">**Why create an ID list search?** If you're unable to determine if an item is responsive to an eDiscovery request based on the metadata in the **Results.csv** or **Unindexed Items.csv** files, you can use an ID list search to find, preview, and then export that item to determine if it's responsive to the case you're investigating. ID list searches are typically used to search for and return a specific set of unindexed items.</span></span> 
  
## <a name="prepare-the-csv-file-for-an-id-list-search"></a><span data-ttu-id="a7d5b-124">ID 목록 검색에 대 한 CSV 파일을 준비</span><span class="sxs-lookup"><span data-stu-id="a7d5b-124">Prepare the CSV file for an ID list search</span></span>

<span data-ttu-id="a7d5b-p108">검색 결과 또는 콘텐츠 검색에 대 한 보고서를 내보낸 후에 ID 목록 검색에 대 한 CSV 파일을 준비 하려면 다음 단계를 수행할 수 있습니다. 이 CSV 파일은 ID 목록 검색에 있는 모든 항목을 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="a7d5b-p108">After you export the search results or report for a content search, you can perform the following steps to prepare the CSV file for an ID list search. This CSV file will identify every item in the ID list search.</span></span>
  
<span data-ttu-id="a7d5b-p109">Note는 SharePoint 사이트 및 OneDrive 계정을 포함 하는 검색에서 CSV 파일을 사용할 수 있지만 *ID 목록 검색에 대 한 사서함 항목을* 선택할 수 있습니다. SharePoint 또는 OneDrive에서 문서를 선택 하는 경우에 CSV 파일에서 ID 목록 검색을 만들 때 유효성 검사에 실패 합니다.</span><span class="sxs-lookup"><span data-stu-id="a7d5b-p109">Note that you can use a CSV file from a search that included SharePoint sites and OneDrive accounts, but you can select  *only*  mailbox items for an ID list search. If you select a document in SharePoint or OneDrive, the CSV file will fail validation when you create an ID list search.</span></span> 
  
1. <span data-ttu-id="a7d5b-129">Excel에서 **Results.csv** 또는 **인덱싱되지 않은 Items.csv** 파일을 엽니다.</span><span class="sxs-lookup"><span data-stu-id="a7d5b-129">Open the **Results.csv** or **Unindexed Items.csv** file in Excel.</span></span> 
    
2. <span data-ttu-id="a7d5b-p110">새 열을 삽입 하 고 **선택한**라는 이름을 지정 합니다. 열을 삽입 하면 영향을 받지 않습니다. 편의 위해 열 1의 왼쪽에 삽입 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="a7d5b-p110">Insert a new column and name it **Selected**. It doesn't matter where you insert the column. For convenience, consider inserting it to the left of the first column.</span></span>
    
3. <span data-ttu-id="a7d5b-p111">**선택한** 열에서 **예** 를 검색 하려는 항목에 해당 하는 셀에를 입력 합니다. 검색 하려는 모든 항목에 대해이 단계를 반복 합니다.</span><span class="sxs-lookup"><span data-stu-id="a7d5b-p111">In the **Selected** column, type **Yes** in the cell that corresponds to the item that you want to search for. Repeat this step for every item that you want to search for.</span></span> 
    
    > [!IMPORTANT]
    > <span data-ttu-id="a7d5b-p112">Excel에서 CSV 파일을 열 때 **문서 ID** 열에 대 한 데이터 형식은 **일반**로 변경 됩니다. 표기법에 있는 항목에 대 한 문서 ID 표시 (영문)이 만들어집니다. 예, ID "481037338205"의 "4.81037E + 11"으로 표시 되는 문서 해야 문서 id를 올바른 형식으로 돌아갈 **수** 는 **문서 ID** 열의 데이터 형식을 변경 하려면 다음 단계를 수행 하려면 이렇게 하지 않으면 CSV 파일을 사용 하는 ID 목록 검색 실패 합니다.</span><span class="sxs-lookup"><span data-stu-id="a7d5b-p112">When you open the CSV file in Excel, the data format for the **Document ID** column is changed to **General**. This results in displaying the document ID for an item in scientific notation. For example, the document ID of "481037338205" is displayed as "4.81037E+11" You have to perform the next steps to change the data format of the **Document ID** column to **Number** to restore the correct format for the document ID. If you don't do this, the ID list search that uses the CSV file will fail.</span></span> 
  
4. <span data-ttu-id="a7d5b-139">**문서 ID** 열 전체를 마우스 오른쪽 단추로 클릭 하 고 **Format 셀**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="a7d5b-139">Right-click the entire **Document ID** column and select **Format Cells**.</span></span>
    
5. <span data-ttu-id="a7d5b-140">**범주** 상자에 **번호**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="a7d5b-140">In the **Category** box, click **Number**.</span></span>
    
6. <span data-ttu-id="a7d5b-p113">소수 자릿수를 **0**으로 변경 하 고 변경 내용을 저장 하려면 **확인** 클릭 합니다. 번호에 문서 ID 열에서 값이 변경 되었는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="a7d5b-p113">Change the number of decimal places to **0**, and then click **OK** to save your changes. Notice that the values in the Document ID column are changed to numbers.</span></span> 
    
    <span data-ttu-id="a7d5b-143">다음은의 한 예는 ID 목록 콘텐츠 검색을 위한 전송할 준비가 된 CSV 파일입니다.</span><span class="sxs-lookup"><span data-stu-id="a7d5b-143">Here's an example of the a CSV file that's ready to be submitted for a ID list content search.</span></span>
    
    ![대상된 콘텐츠 검색에 대 한 CSV 파일의 예](media/8371b8cb-1638-496e-9be1-fe1565757d67.png)
  
7. <span data-ttu-id="a7d5b-p114">CSV 파일을 저장 또는 **다른이름으로** 저장 사용 하 여 다른 파일 이름 사용 하 여 파일입니다. 두 경우 모두 CSV 형식으로 파일을 저장 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a7d5b-p114">Save the CSV file or use **Save As** to the save the file with different file name. In both cases, be sure to save the file with the CSV format.</span></span> 
  
## <a name="create-an-id-list-search"></a><span data-ttu-id="a7d5b-147">ID 목록 검색 만들기</span><span class="sxs-lookup"><span data-stu-id="a7d5b-147">Create an ID list search</span></span>

<span data-ttu-id="a7d5b-148">다음 단계는 새 ID 목록 콘텐츠 검색을 작성 하 고 이전 단계에서 준비한 CSV 파일을 제출 하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="a7d5b-148">The next step is to create a new ID list Content Search and submit the CSV file that you prepared in the previous step.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="a7d5b-p115">콘텐츠 검색의 결과 또는 보고서를 내보낸 후 2 개 이상의 일 ID 목록 검색을 더 만들기 해야 합니다. 검색 결과 또는 2 일이 경과 하지 않았습니다을 내보낸 위치를 보고 하는 경우 검색 결과 또는 업데이트 된 CSV 파일을 생성 하는 보고서 다시 내보내기 해야 합니다. 다음 업데이트 된 CSV 파일 중 하나를 준비 하 고 ID 목록 검색 만들기를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a7d5b-p115">You should create an ID list search no more than 2 days after exporting the results or report from a Content Search. If the search results or report where exported more than 2 days ago, you should re-export the search results or report to generate updated CSV files. Then you can prepare one of the updated CSV files and use it to create an ID list search.</span></span> 
  
1. <span data-ttu-id="a7d5b-152">보안에서 &amp; 준수 센터, 이동 **검색 &amp; 조사** \> **콘텐츠 검색**합니다.</span><span class="sxs-lookup"><span data-stu-id="a7d5b-152">In the Security &amp; Compliance Center, go to **Search &amp; investigation** \> **Content search**.</span></span>
    
2. <span data-ttu-id="a7d5b-153">**검색** 페이지에 있는 화살표를 옆에 클릭 ![추가 아이콘](media/8ee52980-254b-440b-99a2-18d068de62d3.gif) **새 검색** **ID 목록에서 검색**을 클릭 하 고 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a7d5b-153">On the **Search** page, click the arrow next to ![Add icon](media/8ee52980-254b-440b-99a2-18d068de62d3.gif) **New search**, and then click **Search by ID List**.</span></span>
    
    ![새 검색 드롭다운 목록에서 ID 목록에서 검색을 클릭 합니다.](media/e65f9942-09b2-4127-865e-e64029a590df.png)
  
3. <span data-ttu-id="a7d5b-155">**ID 목록으로 검색** 플라이 아웃에는 검색에 이름을 (및 선택적으로 설명) 하 고 다음 **찾아보기** 를 클릭 하 고 이전 단계에서 준비한 CSV 파일을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="a7d5b-155">On the **Search by ID List** flyout, name the search (and optionally describe it) and then click **Browse** and select the CSV file that you prepared in the previous step.</span></span> 
    
    <span data-ttu-id="a7d5b-p116">Office 365 CSV 파일의 유효성을 검사 하려고 합니다. 오류 메시지가 표시 되는 유효성 검사가 실패할 경우 유효성 검사 오류를 해결 하는데 도움이 되는 것입니다. CSV 파일 ID 목록 검색 만드는 성공적으로 유효성을 검사 하려면에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a7d5b-p116">Office 365 attempts to validate the CSV file. If the validation is unsuccessful, an error message is displayed that might help you troubleshoot the validation errors. The CSV file has to be successfully validated to create an ID list search.</span></span>
    
4. <span data-ttu-id="a7d5b-159">후에서 CSV 파일은 성공적으로 유효성을 검사, ID 목록 검색을 만들 수 있는 **검색** 을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="a7d5b-159">After the CSV file is successfully validated, click **Search** to create the ID list search.</span></span> 
    
    <span data-ttu-id="a7d5b-160">ID 목록 검색용 생성 되는 쿼리 및 예상된 검색 결과의 예는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="a7d5b-160">Here's an example of the estimated search results and the query that's generated for an ID list search.</span></span>
    
    ![세부 정보 창에서 대상으로 지정 된 콘텐츠 검색에 대 한 검색 쿼리](media/dbd9e570-c04b-4056-a8a7-37e9916ec683.png)
  
    <span data-ttu-id="a7d5b-162">참고 ID 검색에 대 한 통계에 표시 되는 예상된 항목 수가 CSV 파일에서 선택한 항목의 번호를 일치 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a7d5b-162">Note that the number of estimated items displayed in statistics for the ID search should match the number of items that you selected in the CSV file.</span></span>
    
5. <span data-ttu-id="a7d5b-163">미리 보기 또는 ID 목록 검색에서 반환 된 항목을 내보냅니다.</span><span class="sxs-lookup"><span data-stu-id="a7d5b-163">Preview or export the items returned by the ID list search.</span></span>
    
> [!NOTE]
> <span data-ttu-id="a7d5b-p117">ID 목록 검색 프로그램을 만든 후 사서함을 이동 하는 경우 검색에 대 한 쿼리는 지정된 된 항목 반환 되지 않습니다. 사서함이 이동할 때 사서함 항목에 대 한 **DocumentId** 속성이 변경 되는 때문입니다. 특수 한 인스턴스에 사서함 ID 목록 검색 프로그램을 만든 후를 이동 해야 새 콘텐츠 검색 (만들거나 업데이트 하는 기존 콘텐츠 검색에 대 한 검색 결과) 하 고 내보내기 검색 결과 또는 사용할 수 있는 업데이트 된 CSV 파일을 생성 하려면 보고서  새 ID 목록 검색을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="a7d5b-p117">If you move a mailbox after creating an ID list search, the query for the search won't return the specified items. That's because the **DocumentId** property for mailbox items are changed when a mailbox is moved. In the rare instance when a mailbox is moved after you create an ID list search, you should create a new content search (or update the search results for the existing content search) and then export the search results or report to generate updated CSV files that can be used to create a new ID list search.</span></span> 
