---
title: 감사 로그 기록 내보내기, 구성 및 보기
ms.author: markjjo
author: markjjo
manager: laurawi
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- Strat_O365_IP
- M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: 0d4d0f35-390b-4518-800e-0c7ec95e946c
description: Office 365 감사 로그 검색 결과를 CSV 파일로 내보내고 다운로드 한 후 Excel의 파워 쿼리 편집기에서 JSON 변환 기능을 사용 하 여 AuditData 열에 있는 JSON 개체의 각 속성을 자체 열로 분할할 수 있습니다. 이를 통해 원하는 특정 감사 데이터를 빠르게 찾을 수 있습니다.
ms.openlocfilehash: 7dac373e8f25ead38dddbe2663e521b35b3153ef
ms.sourcegitcommit: b262d40f6daf06be26e7586f37b736e09f8a4511
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/02/2019
ms.locfileid: "35462939"
---
# <a name="export-configure-and-view-audit-log-records"></a><span data-ttu-id="cd579-104">감사 로그 기록 내보내기, 구성 및 보기</span><span class="sxs-lookup"><span data-stu-id="cd579-104">Export, configure, and view audit log records</span></span>

<span data-ttu-id="cd579-105">Office 365 감사 로그를 검색 하 고 검색 결과를 CSV 파일로 다운로드 한 후 해당 파일에는 각 이벤트에 대 한 추가 정보를 포함 하는 **Auditdata**라는 열이 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cd579-105">After you search the Office 365 audit log and download the search results to a CSV file, the file contains a column named **AuditData**, which contains additional information about each event.</span></span> <span data-ttu-id="cd579-106">이 열의 데이터는 JSON 개체로 형식이 지정 되며,이 개체는 쉼표로 구분 된 *값* 쌍으로 구성 된 여러 속성을 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd579-106">The data in this column is formatted as a JSON object, which contains multiple properties that are configured as *property:value* pairs separated by commas.</span></span> <span data-ttu-id="cd579-107">Excel의 파워 쿼리 편집기에서 JSON 변환 기능을 사용 하 여 각 속성에 자체 열이 포함 되도록 **Auditdata** 열에 있는 json 개체의 각 속성을 여러 열로 분할할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cd579-107">You can use the JSON transform feature in the Power Query Editor in Excel to split each property in the JSON object in the **AuditData** column into multiple columns so that each property has its own column.</span></span> <span data-ttu-id="cd579-108">이를 통해 이러한 속성 중 하나 이상을 정렬 및 필터링 하 여 원하는 특정 감사 데이터를 빠르게 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cd579-108">This lets you sort and filter on one or more of these properties, which can help you quickly locate the specific auditing data you're looking for.</span></span>

## <a name="step-1-export-audit-log-search-results"></a><span data-ttu-id="cd579-109">1 단계: 감사 로그 검색 결과 내보내기</span><span class="sxs-lookup"><span data-stu-id="cd579-109">Step 1: Export audit log search results</span></span>

<span data-ttu-id="cd579-110">첫 번째 단계는 감사 로그를 검색 한 다음 CSV (쉼표로 구분 된 값) 파일의 결과를 로컬 컴퓨터로 내보내는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="cd579-110">The first step is to search the audit log and then export the results in a comma-separated value (CSV) file to your local computer.</span></span>
  
1. <span data-ttu-id="cd579-111">[감사 로그 검색](search-the-audit-log-in-security-and-compliance.md#search-the-audit-log) 을 실행 하 고 필요한 경우 원하는 결과를 얻을 때까지 검색 조건을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd579-111">Run an [audit log search](search-the-audit-log-in-security-and-compliance.md#search-the-audit-log) and revise the search criteria if necessary until you have the desired results.</span></span>
    
2. <span data-ttu-id="cd579-112">**결과 내보내기를** 클릭 하 고 **모든 결과 다운로드**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd579-112">Click **Export results** and select **Download all results**.</span></span> 
    
   ![모든 결과 다운로드를 클릭 합니다.](media/ExportAuditSearchResults.png)

   <span data-ttu-id="cd579-114">이 옵션을 선택 하면 1 단계에서 실행 한 감사 로그 검색의 모든 감사 레코드를 내보내고, 감사 로그의 원시 데이터를 CSV 파일로 다운로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd579-114">This option to exports all the audit records from the audit log search you ran in step 1, and downloads the raw data from the audit log to a CSV file.</span></span> 

   <span data-ttu-id="cd579-115">CSV 파일을 열거나 저장 하 라는 메시지가 창 맨 아래에 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="cd579-115">A message is displayed at the bottom of the window that prompts you to open or save the CSV file.</span></span> 

3. <span data-ttu-id="cd579-116">**저장 > 다른 이름으로 저장** 을 클릭 하 여 로컬 컴퓨터에 CSV 파일을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd579-116">Click **Save > Save as** and save the CSV file to your local computer.</span></span> <span data-ttu-id="cd579-117">많은 검색 결과를 다운로드 하는 데 시간이 오래 걸립니다.</span><span class="sxs-lookup"><span data-stu-id="cd579-117">It takes a while to download many search results.</span></span> <span data-ttu-id="cd579-118">이는 일반적으로 모든 작업을 검색 하는 경우 또는 광범위 한 날짜 범위에 해당 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd579-118">This is typically the case when searching for all activities or a broad date range.</span></span> <span data-ttu-id="cd579-119">CSV 파일의 다운로드가 완료 되 면 windows 아래쪽에 메시지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="cd579-119">A message at the bottom of the windows is displayed when the CSV file is finished downloading.</span></span>
 
   ![CSV 파일 다운로드가 완료 되 면 표시 되는 메시지](media/ExportAuditSearchResultsFinish.png)

> [!NOTE]
  > <span data-ttu-id="cd579-121">단일 감사 로그 검색에서 최대 5만 개의 항목을 CSV 파일에 다운로드할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cd579-121">You can download a maximum of 50,000 entries to a CSV file from a single audit log search.</span></span> <span data-ttu-id="cd579-122">5만 항목이 CSV 파일에 다운로드 되는 경우 검색 조건을 충족 하는 이벤트가 5만 개 보다 많은 것으로 간주할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cd579-122">If 50,000 entries are downloaded to the CSV file, you can probably assume there are more than 50,000 events that met the search criteria.</span></span> <span data-ttu-id="cd579-123">이 제한 보다 많은 시간을 내보내려면 날짜 범위를 사용 하 여 감사 로그 레코드 수를 줄이십시오.</span><span class="sxs-lookup"><span data-stu-id="cd579-123">To export more than this limit, try using a date range to reduce the number of audit log records.</span></span> <span data-ttu-id="cd579-124">5만 개 보다 많은 항목을 내보내려면 날짜 범위가 더 작은 검색을 여러 개 실행 해야 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cd579-124">You might have to run multiple searches with smaller date ranges to export more than 50,000 entries.</span></span>

## <a name="step-2-format-the-exported-audit-log-using-the-power-query-editor"></a><span data-ttu-id="cd579-125">2 단계: 파워 쿼리 편집기를 사용 하 여 내보낸 감사 로그 서식 지정</span><span class="sxs-lookup"><span data-stu-id="cd579-125">Step 2: Format the exported audit log using the Power Query Editor</span></span>

<span data-ttu-id="cd579-126">다음 단계에서는 Excel의 파워 쿼리 편집기에서 JSON 변환 기능을 사용 하 여 **Auditdata** 열에 있는 json 개체의 각 속성을 자체 열로 분할 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd579-126">The next step is to use the JSON transform feature in the Power Query Editor in Excel to split each property in the JSON object in the **AuditData** column into its own column.</span></span> <span data-ttu-id="cd579-127">그런 다음 특정 속성의 값을 기반으로 레코드를 볼 수 있도록 열을 필터링 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd579-127">Then you filter columns to view records based on the values of specific properties.</span></span> <span data-ttu-id="cd579-128">이를 통해 원하는 특정 감사 데이터를 빠르게 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cd579-128">This can help you quickly locate the specific auditing data you're looking for.</span></span>

1. <span data-ttu-id="cd579-129">Excel에서 Office 365, Excel 2019 또는 Excel 2016의 빈 통합 문서를 엽니다.</span><span class="sxs-lookup"><span data-stu-id="cd579-129">Open a blank workbook in Excel for Office 365, Excel 2019, or Excel 2016.</span></span>
    
2.  <span data-ttu-id="cd579-130">**데이터** 탭의 **& 변환 데이터 가져오기** 리본 그룹에서 **텍스트/CSV를**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd579-130">On the **Data** tab, in the **Get & Transform Data** ribbon group, click **From Text/CSV**.</span></span>

    ![데이터 탭에서 Text/CSV를 클릭 합니다.](media/JSONTransformOpenCSVFile.png)

3. <span data-ttu-id="cd579-132">1 단계에서 다운로드 한 CSV 파일을 엽니다.</span><span class="sxs-lookup"><span data-stu-id="cd579-132">Open the CSV file that you downloaded in Step 1.</span></span>
    
4. <span data-ttu-id="cd579-133">표시 된 창에서 **데이터 변환을**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd579-133">In the window that's displayed, click **Transform Data**.</span></span>

   ![데이터 변환 클릭](media/JSONOpenPowerQuery.png)

<span data-ttu-id="cd579-135">CSV 파일이 **쿼리 편집기**에서 열립니다.</span><span class="sxs-lookup"><span data-stu-id="cd579-135">The CSV file is opened in the **Query Editor**.</span></span> <span data-ttu-id="cd579-136">**CreationDate**, **UserIds**, **Operations**및 **auditdata**의 네 가지 열이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cd579-136">There are four columns: **CreationDate**, **UserIds**, **Operations**, and **AuditData**.</span></span> <span data-ttu-id="cd579-137">**Auditdata** 열은 여러 속성을 포함 하는 JSON 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="cd579-137">The **AuditData** column is a JSON object that contains multiple properties.</span></span> <span data-ttu-id="cd579-138">다음 단계에서는 JSON 개체의 각 속성에 대 한 열을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="cd579-138">The next step is to create a column for each property in the JSON object.</span></span>
    
5. <span data-ttu-id="cd579-139">**Auditdata** 열에서 제목을 마우스 오른쪽 단추로 클릭 하 고 **변환**, **JSON**을 차례로 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd579-139">Right-click the title in the **AuditData** column, click **Transform**, and then click **JSON**.</span></span> 
 
   ![AuditData 열을 마우스 오른쪽 단추로 클릭 하 고 변환, JSON을 차례로 선택 합니다.](media/JSONTransform.png)

6. <span data-ttu-id="cd579-141">**Auditdata** 열의 오른쪽 위 모서리에서 확장 아이콘을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd579-141">In the upper-right corner of the **AuditData** column, click the expand icon.</span></span>
    
   ![AuditData 열에서 확장 아이콘](media/JSONTransformExpandIcon.png)

   <span data-ttu-id="cd579-143">**Auditdata** 열에 있는 JSON 개체의 속성 중 일부 목록이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="cd579-143">A partial list of the properties in the JSON objects in the **AuditData** column is displayed.</span></span>

7. <span data-ttu-id="cd579-144">모두 **로드** 를 클릭 하 여 **AUDITDATA** 열에 JSON 개체의 모든 속성을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd579-144">Click **Load more** to display all properties in the JSON objects in the **AuditData** column.</span></span>

   ![JSON 개체에 모든 속성을 표시 하려면 추가를 클릭 합니다.](media/JSONTransformLoadJSONProperties.png)

   <span data-ttu-id="cd579-146">포함 하지 않을 속성 옆의 확인란을 선택 취소할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cd579-146">You can unselect the checkbox next to any property that you don't want to include.</span></span> <span data-ttu-id="cd579-147">조사에 도움이 되지 않는 열을 제거 하는 것은 감사 로그에 표시 되는 데이터의 양을 줄이는 좋은 방법입니다.</span><span class="sxs-lookup"><span data-stu-id="cd579-147">Eliminating columns that aren't useful for your investigation is a good way to reduce the amount of data displayed in the audit log.</span></span> 

   > [!NOTE]
   > <span data-ttu-id="cd579-148">이전 스크린샷에 표시 된 JSON 속성 ( **더 이상 로드**를 클릭 한 후)은 CSV 파일의 첫 번째 1000 행에서 **auditdata** 열에 있는 속성을 기반으로 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd579-148">The JSON properties displayed in the previous screenshot (after you click **Load more**) are based on the properties found in the **AuditData** column from the first 1,000 rows in the CSV file.</span></span> <span data-ttu-id="cd579-149">첫 번째 1000 행 다음의 레코드에 다른 JSON 속성이 있는 경우에는 **Auditdata** 열이 여러 열로 분할 될 때 이러한 속성 및 해당 열이 포함 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="cd579-149">If there are different JSON properties in records after the first 1,000 rows, these properties (and a corresponding column) won't be included when the **AuditData** column is split into multiple columns.</span></span> <span data-ttu-id="cd579-150">이를 방지 하기 위해 감사 로그 검색을 다시 실행 하 고 검색 조건을 좁혀 더 작은 레코드가 반환 되도록 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="cd579-150">To help prevent this, consider re-running the audit log search and narrow the search criteria so that fewer records are returned.</span></span> <span data-ttu-id="cd579-151">또 다른 해결 방법은 **Auditdata** 열에서 JSON 개체를 변환 하기 전에 **작업** 열에서 항목을 필터링 하 여 행 수 (위의 5 단계를 수행 하기 전)를 줄이기 위한 것입니다.</span><span class="sxs-lookup"><span data-stu-id="cd579-151">Another workaround is to filter items in the **Operations** column to reduce the number of rows (before you perform step 5 above) before transforming the JSON object in the **AuditData** column.</span></span>

8. <span data-ttu-id="cd579-152">다음 중 하나를 수행 하 여 선택 된 각 JSON 속성에 추가 되는 열의 제목에 서식을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd579-152">Do one of the following things to format the title of the columns that are added for each JSON property that's selected.</span></span>

    - <span data-ttu-id="cd579-153">JSON 속성 이름을 열 이름으로 사용 하려면 **원래 열 이름을 접두사로 사용** 확인란의 선택을 취소 합니다. 예를 들어 **RecordType** 또는 **sourcefilename**을 사용할 때</span><span class="sxs-lookup"><span data-stu-id="cd579-153">Unselect the **Use original column name as prefix** checkbox to use the name of the JSON property as the column names; for example, **RecordType** or **SourceFileName**.</span></span>
    
   - <span data-ttu-id="cd579-154">열 이름에 AuditData 접두사를 추가 하려면 **원래 열 이름을 접두사로 사용** 확인란을 선택 된 상태로 유지 합니다. 예를 들어, **Auditdata** 또는 **Auditdata. sourcefilename**을 사용할 때</span><span class="sxs-lookup"><span data-stu-id="cd579-154">Leave the **Use original column name as prefix** checkbox selected to add the AuditData prefix to the column names; for example, **AuditData.RecordType** or **AuditData.SourceFileName**.</span></span>

9. <span data-ttu-id="cd579-155">**확인**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="cd579-155">Click **OK**.</span></span>
    
    <span data-ttu-id="cd579-156">**Auditdata** 열은 여러 열로 분할 됩니다.</span><span class="sxs-lookup"><span data-stu-id="cd579-156">The **AuditData** column is split into multiple columns.</span></span> <span data-ttu-id="cd579-157">각각의 새 열은 AuditData JSON 개체의 속성에 해당 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd579-157">Each new column corresponds to a property in the AuditData JSON object.</span></span> <span data-ttu-id="cd579-158">열의 각 행에는 속성의 값이 들어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cd579-158">Each row in the column contains the value for the property.</span></span> <span data-ttu-id="cd579-159">속성에 값이 포함 되어 있지 않으면 *null* 값이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="cd579-159">If the property doesn't contain a value, the *null* value is displayed.</span></span> <span data-ttu-id="cd579-160">Excel에서 null 값이 있는 셀은 비어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cd579-160">In Excel, cells with null values are empty.</span></span>
  
10. <span data-ttu-id="cd579-161">**홈** 탭에서 **& 로드 닫기를** 클릭 하 여 파워 쿼리 편집기를 닫고 Excel 통합 문서에서 변환 된 CSV 파일을 엽니다.</span><span class="sxs-lookup"><span data-stu-id="cd579-161">On the **Home** tab, click **Close & Load** to close the Power Query Editor and open the transformed CSV file in an Excel workbook.</span></span> 

## <a name="tips-for-exporting-and-viewing-the-audit-log"></a><span data-ttu-id="cd579-162">감사 로그 내보내기 및 보기에 대 한 팁</span><span class="sxs-lookup"><span data-stu-id="cd579-162">Tips for exporting and viewing the audit log</span></span>

<span data-ttu-id="cd579-163">다음은 JSON 변환 기능을 사용 하 여 **Auditdata** 열을 여러 열로 분할 하기 전과 수행한 후의 감사 로그 내보내기 및 보기에 대 한 몇 가지 팁과 예입니다.</span><span class="sxs-lookup"><span data-stu-id="cd579-163">Here are some tips and examples of exporting and viewing the audit log before and after you use the JSON transform feature to split the **AuditData** column into multiple columns.</span></span>

- <span data-ttu-id="cd579-164">**RecordType** 열을 필터링 하 여 특정 Office 365 서비스 또는 기능 영역의 레코드만 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd579-164">Filter the **RecordType** column to display only the records from a specific Office 365 service or functional area.</span></span> <span data-ttu-id="cd579-165">예를 들어 SharePoint 공유와 관련 된 이벤트를 표시 하려면 **14** (SharePoint 공유 활동에서 트리거된 레코드의 enum 값)를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd579-165">For example, to show events related to SharePoint sharing, you would select **14** (the enum value for records triggered by SharePoint sharing activities).</span></span> <span data-ttu-id="cd579-166">**RecordType** 열에 표시 된 열거형 값에 해당 하는 office 365 서비스의 목록은 [office 365 감사 로그의 자세한 속성](detailed-properties-in-the-office-365-audit-log.md)을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="cd579-166">For a list of the Office 365 services that correspond to the enum values displayed in the **RecordType** column, see [Detailed properties in the Office 365 audit log](detailed-properties-in-the-office-365-audit-log.md).</span></span>

- <span data-ttu-id="cd579-167">**작업** 열을 필터링 하 여 특정 활동에 대 한 레코드를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd579-167">Filter the **Operations** column to display the records for specific activities.</span></span> <span data-ttu-id="cd579-168">보안 & 준수 센터의 감사 로그 검색 도구에서 검색 가능한 활동에 해당 하는 대부분의 작업 목록을 보려면 [보안 & 준수 센터에서 감사 로그 검색](search-the-audit-log-in-security-and-compliance.md#audited-activities)의 "감사 된 작업" 섹션을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="cd579-168">For a list of most operations that correspond to a searchable activity in the audit log search tool in the Security & Compliance Center, see the "Audited activities" section in [Search the audit log in the Security & Compliance Center](search-the-audit-log-in-security-and-compliance.md#audited-activities).</span></span>

- <span data-ttu-id="cd579-169">보안 & 준수 센터에서 감사 로그 검색 도구를 사용 하는 대신 Exchange Online Powershell의 [search-unifiedauditlog](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-audit/search-unifiedauditlog) cmdlet을 사용 하 여 Office 365 감사 로그 검색의 결과를 CSV 파일로 내보낼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cd579-169">Instead of using the audit log search tool in the Security & Compliance Center, you can use the [Search-UnifiedAuditLog](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-audit/search-unifiedauditlog) cmdlet in Exchange Online Powershell to export the results of an Office 365 audit log search to a CSV file.</span></span> <span data-ttu-id="cd579-170">그런 다음 2 단계에서 설명한 것과 같은 절차에 따라 파워 쿼리 편집기를 사용 하 여 감사 로그를 포맷할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cd579-170">Then you can follow the same procedure described in Step 2 to format the audit log using the Power Query editor.</span></span> <span data-ttu-id="cd579-171">PowerShell cmdlet을 사용 하는 경우의 한 가지 이점은 *RecordType* 매개 변수를 사용 하 여 특정 Office 365 서비스에서 이벤트를 검색할 수 있다는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="cd579-171">One advantage of using the PowerShell cmdlet is that you can search for events from a specific Office 365 service by using the *RecordType* parameter.</span></span> <span data-ttu-id="cd579-172">다음은 PowerShell을 사용 하 여 감사 레코드를 CSV 파일로 내보낸 다음, 파워 쿼리 편집기를 사용 하 여 **Auditdata** 열에 있는 JSON 개체를 2 단계에 설명 된 대로 변환할 수 있는 몇 가지 예입니다.</span><span class="sxs-lookup"><span data-stu-id="cd579-172">Here are few examples of using PowerShell to export audit records to a CSV file so you can use the Power Query editor to transform the JSON object in the **AuditData** column as described in Step 2.</span></span>

   <span data-ttu-id="cd579-173">이 예제에서는 다음 명령을 실행 하 여 SharePoint 공유 작업과 관련 된 모든 레코드를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd579-173">In this example, run the following commands to return all records related to SharePoint sharing operations.</span></span> 
   
   ```
   $auditlog = Search-UnifiedAuditLog -StartDate 06/01/2019 -EndDate 06/30/2019 -RecordType SharePointSharingOperation
   ```

   ```
   $auditlog | Select-Object -Property CreationDate,UserIds,RecordType,AuditData | Export-Csv -Path c:\AuditLogs\PowerShellAuditlog.csv -NoTypeInformation
   ```

   - <span data-ttu-id="cd579-174">검색 결과는 CreationDate, UserIds, RecordType, AuditData와 같은 네 개의 열이 포함 된 *PowerShellAuditlog* 라는 CSV 파일로 내보내집니다.</span><span class="sxs-lookup"><span data-stu-id="cd579-174">The search results are exported to a CSV file named *PowerShellAuditlog* that contains four columns: CreationDate, UserIds, RecordType, AuditData).</span></span>

   - <span data-ttu-id="cd579-175">레코드 종류의 이름 또는 열거형 값을 *RecordType* 매개 변수의 값으로 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cd579-175">You can use the name or enum value for the record type as the value for the *RecordType* parameter.</span></span> <span data-ttu-id="cd579-176">레코드 유형 이름 및 해당 열거형 값의 목록은 *AuditLogRecordType* Table in [Office 365 Management Activity API schema](https://docs.microsoft.com/office/office-365-management-api/office-365-management-activity-api-schema#enum-auditlogrecordtype---type-edmint32)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="cd579-176">For a list of record type names and their corresponding enum values, see the *AuditLogRecordType* table in [Office 365 Management Activity API schema](https://docs.microsoft.com/office/office-365-management-api/office-365-management-activity-api-schema#enum-auditlogrecordtype---type-edmint32).</span></span>
   
   - <span data-ttu-id="cd579-177">이 매개 변수에는 단일 값만 포함할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cd579-177">You can only include a single value for this parameter.</span></span> <span data-ttu-id="cd579-178">다른 레코드 종류에 대 한 감사 레코드를 검색 하려면 이전 두 명령을 다시 실행 하 여 다른 레코드 종류를 지정 하 고 해당 결과를 원래의 CSV 파일에 추가 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd579-178">To search for audit records for other record types, you have to run the two previous commands again to specify a different record type and append those results to the original CSV file.</span></span> <span data-ttu-id="cd579-179">예를 들어 다음 두 명령을 실행 하 여 동일한 날짜 범위의 SharePoint 파일 활동을 PowerShellAuditlog 파일에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd579-179">For example, you would run these two commands to add SharePoint file activities from the same date range to the PowerShellAuditlog.csv file.</span></span>

       ```
      $auditlog = Search-UnifiedAuditLog -StartDate 06/01/2019 -EndDate 06/30/2019 -RecordType SharePointFileOperation
      ```

      ```
      $auditlog | Select-Object -Property CreationDate,UserIds,RecordType,AuditData | Export-Csv -Append -Path c:\AuditLogs\PowerShellAuditlog.csv -NoTypeInformation
      ```
