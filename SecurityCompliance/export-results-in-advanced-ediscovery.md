---
title: Office 365 Advanced eDiscovery 결과 내보내기
ms.author: chrfox
author: chrfox
manager: laurawi
ms.date: 9/14/2017
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: a9951a07-10b3-48cb-b37a-0ffaa24931ad
description: '내보내기 일괄 처리에 대 한 매개 변수를 지정 하는 절차를 포함 하 여 Office 365 Advanced eDiscovery에서 결과를 내보내기 위한 옵션을 정의 하는 방법을 알아봅니다. '
ms.openlocfilehash: 02314b0848d8e7bb37a7cb96fa4a721cf2622712
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30218098"
---
# <a name="export-results-in-office-365-advanced-ediscovery"></a><span data-ttu-id="166fc-103">Office 365 Advanced eDiscovery 결과 내보내기</span><span class="sxs-lookup"><span data-stu-id="166fc-103">Export results in Office 365 Advanced eDiscovery</span></span>

> [!NOTE]
> <span data-ttu-id="166fc-p101">Advanced eDiscovery를 사용하려면 Office 365 E3의 고급 준수 추가 기능이나 조직을 위한 E5 구독이 필요합니다. 이 요금제가 없는 상태에서 Advanced eDiscovery를 사용하려는 경우에는 [Office 365 Enterprise E5 평가판을 등록](https://go.microsoft.com/fwlink/p/?LinkID=698279)할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="166fc-p101">Advanced eDiscovery requires an Office 365 E3 with the Advanced Compliance add-on or an E5 subscription for your organization. If you don't have that plan and want to try Advanced eDiscovery, you can [sign up for a trial of Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span></span> 
  
<span data-ttu-id="166fc-106">이 항목에서는 Advanced eDiscovery 내보내기 설정 옵션에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="166fc-106">This topic describes the Advanced eDiscovery Export Setup options.</span></span>
  
 <span data-ttu-id="166fc-107">**이 항목의 내용:**</span><span class="sxs-lookup"><span data-stu-id="166fc-107">**In this topic:**</span></span>
  
- [<span data-ttu-id="166fc-108">내보내기 일괄 처리 및 세션 정의</span><span class="sxs-lookup"><span data-stu-id="166fc-108">Defining export batches and sessions</span></span>](export-results-in-advanced-ediscovery.md#BK_Define)
    
- [<span data-ttu-id="166fc-109">증분 및 추가 내보내기</span><span class="sxs-lookup"><span data-stu-id="166fc-109">Incremental and additional exports</span></span>](export-results-in-advanced-ediscovery.md#BK_IncrementalReports)
    
- [<span data-ttu-id="166fc-110">일괄 내보내기 매개 변수 설정</span><span class="sxs-lookup"><span data-stu-id="166fc-110">Set up batch export parameters</span></span>](export-results-in-advanced-ediscovery.md#BK_SetUpExport)
    
- [<span data-ttu-id="166fc-111">보고서 출력 파일 내보내기</span><span class="sxs-lookup"><span data-stu-id="166fc-111">Export report output files</span></span>](export-results-in-advanced-ediscovery.md#BK_ExportOutputFIles)
    
## <a name="defining-export-batches-and-sessions"></a><span data-ttu-id="166fc-112">내보내기 일괄 처리 및 세션 정의</span><span class="sxs-lookup"><span data-stu-id="166fc-112">Defining export batches and sessions</span></span>
<span data-ttu-id="166fc-113"><a name="BK_Define"> </a></span><span class="sxs-lookup"><span data-stu-id="166fc-113"></span></span>

<span data-ttu-id="166fc-p102">내보내기 일괄 처리는 정의 된 매개 변수 집합을 사용 하 여 내보내기 처리를 허용 합니다. 고급 eDiscovery를 사용 하면 각 내보내기를 사용자 지정할 일괄 처리를 정의할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="166fc-p102">An export batch allows export processing using a set of defined parameters. Advanced eDiscovery enables you to define batches to customize each export.</span></span>
  
<span data-ttu-id="166fc-p103">매개 변수는 내보내기 일괄 처리당 정의 됩니다. "Export batch 01" 이라는 일괄 처리는 첫 번째 사례 일괄 처리에 대해 기본적으로 만들어집니다. 일괄 처리 이름 및 설명을 편집할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="166fc-p103">Parameters are defined per export batch. A batch named "Export batch 01" is created by default for the first batch of a case. You can also edit the batch name and description.</span></span>
  
<span data-ttu-id="166fc-119">내보내기 세션은 내보내기 일괄 처리 내에서 고급 eDiscovery 내보내기의 실행입니다.</span><span class="sxs-lookup"><span data-stu-id="166fc-119">An export session is an execution of Advanced eDiscovery Export within an export batch.</span></span>
  
## <a name="incremental-and-additional-exports"></a><span data-ttu-id="166fc-120">증분 및 추가 내보내기</span><span class="sxs-lookup"><span data-stu-id="166fc-120">Incremental and additional exports</span></span>
<span data-ttu-id="166fc-121"><a name="BK_IncrementalReports"> </a></span><span class="sxs-lookup"><span data-stu-id="166fc-121"></span></span>

<span data-ttu-id="166fc-p104">내보내기 일괄 처리 내에서 여러 내보내기 세션을 실행 하 여 동일한 내보내기 템플릿 및 매개 변수에 따라 일관 된 결과를 유지할 수 있습니다. 일괄 처리 내의 각 세션에 대해 새로 처리 된 사례 데이터에 대 한 분석을 내보내고 각 "점진적" 처리를 처리할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="166fc-p104">You can run multiple export sessions within an export batch, to ensure consistent results based on the same export template and parameters. For each session within a batch, you can export analytics for newly processed case data and process each "incrementally."</span></span>
  
<span data-ttu-id="166fc-p105">다른 매개 변수 집합을 사용 하 여 내보내려면 먼저 새 일괄 처리를 만들어야 합니다. 새 일괄 처리의 첫 번째 세션에서는 이러한 파일을 가져와서 한 개 또는 여러 개의 가져오기에 대해 처리 했는지 여부에 관계 없이 현재까지 처리 된 파일에 대 한 결과를 생성 합니다. 각 일괄 처리는 피벗, 유사성, inclusives 등을 다시 계산 합니다. 세션에서는 일괄 처리에 대해 정의 된 매개 변수를 사용 하며, 세션을 실행할 때마다 피벗, 유사성, inclusives 등을 다시 계산 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="166fc-p105">In order to export using a different set of parameters, you first need to create a new batch. The first session in the new batch will produce results for files processed in the case so far, whether or not these files were imported and processed over one or multiple Imports. Each batch recalculates pivots, similarity, inclusives, etc. Sessions use the parameters defined for the batch and do not recalculate pivots, similarity, inclusives, etc. for each session execution.</span></span>
  
<span data-ttu-id="166fc-p106">예를 들어 사례를 가져오고 해당 데이터를 분석 했다고 가정 합니다. 증분 데이터에 대 한 중복 복제 및 전자 메일 스레딩 결과를 검색 하려면 이전에 데이터를 내보내기 위해 사용한 것과 동일한 일괄 처리에서 **내보내기 세션 만들기** 를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="166fc-p106">For example, assume a case was imported and its data analyzed. In order to retrieve Near-duplicates and Email Threading results for the incremental data, click **Create export session** in the same batch that was previously used to export data.</span></span> 
  
## <a name="set-up-batch-export-parameters"></a><span data-ttu-id="166fc-129">일괄 내보내기 매개 변수 설정</span><span class="sxs-lookup"><span data-stu-id="166fc-129">Set up batch export parameters</span></span>
<span data-ttu-id="166fc-130"><a name="BK_SetUpExport"> </a></span><span class="sxs-lookup"><span data-stu-id="166fc-130"></span></span>

<span data-ttu-id="166fc-p107">eDiscovery 내보내기 도구는 고급 eDiscovery의 검색 결과를 로컬 컴퓨터로 내보내는 데 사용 됩니다. 데이터 전송 처리량을 늘려 내보내기 프로세스의 속도를 높이려면 검색 결과를 내보내는 데 사용 하는 컴퓨터에서 Windows 레지스트리 설정을 구성 하면 됩니다. 다운로드 속도를 높이려면 내보내기 매개 변수를 설정 하기 전에 레지스트리 설정을 구성 합니다. 자세한 내용은 [Office 365에서 eDiscovery 검색 결과를 내보낼 때 다운로드 속도 높이기](increase-download-speeds-when-exporting-ediscovery-results.md)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="166fc-p107">The eDiscovery Export Tool is used to export search results from Advanced eDiscovery to your local computer. To increase the data transfer throughput and speed-up the export process, you can configure a Windows Registry setting on the computer that you use to export the search results. If you'd like to increase the download speed, configure the registry setting before you set up the export parameters. For more information, see [Increase the download speed when exporting eDiscovery search results from Office 365](increase-download-speeds-when-exporting-ediscovery-results.md).</span></span>
  
1. <span data-ttu-id="166fc-135">고급 eDiscovery에서 사례를 선택 하 고 설정 **내보내기를** \> \*\*\*\* 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="166fc-135">In Advanced eDiscovery, select a Case and click **Export** \> **Setup**.</span></span>
    
    - <span data-ttu-id="166fc-136">일괄 **처리 내보내기** 목록에서 일괄 처리 이름 (기본 일괄 처리)을 내보내려면 배치 이름이 나 내보내기 결과를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="166fc-136">From the **Export batch** list, select the batch name or export results to Export batch 01, (the default batch).</span></span> 
    
    - <span data-ttu-id="166fc-p108">기존 사례에 추가한 새 파일에 대 한 결과를 내보내려면 현재 일괄 처리를 계속 합니다. 일괄 처리에서 세션을 만들려면 동일한 일괄 처리 번호를 선택 하 고 **내보내기 세션 만들기** 를 클릭 합니다 .이 옵션을 사용 하면 이전 일괄 처리와 같은 매개 변수를 증분 방식으로 내보낼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="166fc-p108">To export results for new files that you added to an existing case, continue with your current batch. To create a session in the batch, select the same batch number and click **Create export session** You can use this option to export the same parameters as the previous batch, in an incremental manner.</span></span> 
    
    - <span data-ttu-id="166fc-p109">새 \*\*\*\* ![일괄 처리로 내보내려면 추가 아이콘](media/c2dd8b3a-5a22-412c-a7fa-143f5b2b5612.png)추가를 클릭 하 고 **일괄 이름** 에 새 이름 (또는 기본값 적용)과 설명을 **일괄 처리 설명**에 입력 합니다. **확인을**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="166fc-p109">To export to a new batch, click **Add** ![add icon](media/c2dd8b3a-5a22-412c-a7fa-143f5b2b5612.png)and enter a new name in **Batch name** (or accept the default) and a description in **Batch description**. Click **OK**.</span></span>
    
    - <span data-ttu-id="166fc-141">일괄 처리 이름 또는 설명을 편집 하려면 **내보내기 일괄 처리**에서 이름을 선택 하 고 편집 \*\*\*\* ![아이콘](media/3d613660-7602-4df2-bdb9-14e9ca2f9cf2.png)편집을 클릭 한 다음 필드를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="166fc-141">To edit a batch name or description, select the name in **Export batch**, click **Edit** ![Edit icon](media/3d613660-7602-4df2-bdb9-14e9ca2f9cf2.png), and then modify the fields.</span></span>
    
      > [!NOTE]
      > <span data-ttu-id="166fc-p110">내보내기 일괄 처리에 대 한 세션을 실행 한 후에는 삭제할 수 없습니다. 또한 첫 번째 세션을 실행 한 후에는 일부 매개 변수만 편집할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="166fc-p110">After you've run sessions for an export batch, they cannot be deleted. In addition, only some parameters can be edited once the first session is run.</span></span> 
  
    - <span data-ttu-id="166fc-144">중복 된 내보내기 일괄 처리를 만들려면 복제 \*\*\*\* ![된 내보내기 일괄 처리 만들기를 선택 하](media/3f6d5f59-e842-4946-a493-473528af0119.jpg) 고 패널에 중복 일괄 처리에 대 한 이름 및 설명을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="166fc-144">To create a duplicate export batch, choose **Duplicate export batch** ![Create a duplicate export batch icon](media/3f6d5f59-e842-4946-a493-473528af0119.jpg) and enter a name and a description for the duplicate batch in the panel.</span></span> 
    
    - <span data-ttu-id="166fc-145">내보내기 일괄 처리를 삭제 하려면 **삭제** ![를 선택 하 여 일괄 처리](media/92a9f8e0-d469-48da-addb-69365e7ffb6f.jpg)내보내기 아이콘을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="166fc-145">To delete an export batch, choose **Delete** ![Delete an export batch icon](media/92a9f8e0-d469-48da-addb-69365e7ffb6f.jpg).</span></span>
    
    - <span data-ttu-id="166fc-146">일괄 처리 기록을 보려면 **일괄 처리 기록** ![보기 히스토리 아이콘](media/a80cc320-d96c-4d91-8884-75fe2cb147e2.jpg)을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="166fc-146">To view the history of a batch, choose **Batch history** ![View history icon](media/a80cc320-d96c-4d91-8884-75fe2cb147e2.jpg).</span></span>
    
2. <span data-ttu-id="166fc-147">**채우기**에서 관련성 조정 **점수 위에 파일 하나만 포함** 을 선택 하 고 내보내기 일괄 처리에 대 한 설정을 세밀 하 게 조정할 경우 **일괄 처리 내보내기**</span><span class="sxs-lookup"><span data-stu-id="166fc-147">Under **Population**, select **Include only files above Relevance cut-off score** and/or **Refine export batch** if you want to fine-tune the settings for your export batch.</span></span> 
    
3. <span data-ttu-id="166fc-p111">**관련성 초과 점수 위에 파일만 포함**을 선택 하면 **문제가** 활성화 됩니다. 파일의 관련성 점수가 선택한 문제에 대 한 컷오프 점수 보다 높으면 ' 검토용으로 ' 필터로 제외 되지 않는 한 파일을 내보냅니다.</span><span class="sxs-lookup"><span data-stu-id="166fc-p111">If you select **Include only files above Relevance cut-off score**, then the **Issue** is enabled. If the file's relevance score is higher than the cut-off score for the selected issue, the file will be exported unless it's excluded by the 'For review' filter.</span></span> 
  
    <span data-ttu-id="166fc-p112">**일괄 처리**해제를 선택 하면 ' 검토용 \*\*\*\* 으로 ' 및 필터 사용 ' 필드 라디오 단추를 사용할 수 있습니다. **비-dupe**를 선택한 경우 중복 파일은 정의 된 정책에 따라 필터링 됩니다 [대/소문자 수준 (기본값). 전체 중복 파일 집합에서 모든 파일을 제외 하 고는 하나의 파일만 duped 됩니다. Custodian level: 동일한 Custodian의 모든 중복 파일 집합에서 하나의 파일을 제외 하 고 모두 duped 합니다.] 내보내기 출력에는 중복 된 모든 파일의 레코드가 포함 됩니다. **' 검토용으로 필터링 '** 필드를 선택 하는 경우 **메타 데이터 아래 수정을** 선택 하 여 **' 검토용 '** 필드 설정을 입력 합니다. 패키지 콘텐츠에 원본 파일을 포함할 **입력 파일 포함** 을 선택 합니다. 이 설정을 지워 내보내기 프로세스를 빠르게 진행할 수 있습니다. 네이티브 파일은 모든 경우에 내보내집니다.</span><span class="sxs-lookup"><span data-stu-id="166fc-p112">If you select **Refine export batch**, the **De-dupe** and Filter by 'For review' field radio buttons are enabled. If you choose **De-dupe**, then duplicate files will be filtered out according to the policy defined [Case level (default): from every set of duplicate files in the entire case, all but one file will be de-duped. Custodian level: from every set of duplicate files of the same custodian, all but one file will be de-duped.] The export output contains a record of all duplicate files. If you choose **Filter by 'For review'** field, select **Modify under Metadata** to enter your **'For review'** field settings. Select **Include input files** to include source files in the package content. You can clear this setting to speed up the export process. Note that the Native files will be exported in any case.</span></span> 
    
4. <span data-ttu-id="166fc-157">**메타 데이터**아래의 각 세션에 대해 **템플릿 내보내기** 목록에서 다음 옵션 중에서 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="166fc-157">Under **Metadata**, select from the following options in the **Export template** list (once per session).</span></span> 
    
    - <span data-ttu-id="166fc-p113">**표준**: 데이터 항목, 메타 데이터 및 속성의 기본 집합입니다. 고급 eDiscovery에서 데이터 가져오기가 이미 처리 된 경우이 옵션을 사용 하면 파일이 이미 들어 있는 시스템에 내보내기 데이터를 업로드할 수 있습니다. 기본적으로 내보내기 템플릿 열은 만들어지고 채워집니다.</span><span class="sxs-lookup"><span data-stu-id="166fc-p113">**Standard**: Basic set of data items, metadata, and properties. Use this option when import data was already processed in Advanced eDiscovery and export data is uploaded to a system that already contains the files. By default, export template columns are created and filled.</span></span>
    
    - <span data-ttu-id="166fc-p114">**all**: 모든 처리 데이터를 포함 하는 표준 메타 데이터의 전체 집합 및 분석 및 관련성 점수 이 서식 파일은 고급 eDiscovery에서 처리를 수행 하 고 파일 데이터를 처음으로 외부 시스템에 업로드 하는 경우에 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="166fc-p114">**All**: Full set of standard metadata including all processing data, as well as Analyze and Relevance scores. This template is required when Advanced eDiscovery performs the processing and file data is uploaded to an external system for the first time.</span></span>
    
    - <span data-ttu-id="166fc-163">**문제**: **모든 문제** 를 선택 하거나 만든 특정 문제를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="166fc-163">**Issues**: Select **All Issues** or select a particular issue you have created.</span></span> 
    
5. <span data-ttu-id="166fc-164">**대상**:</span><span class="sxs-lookup"><span data-stu-id="166fc-164">Under **Destination**:</span></span>
    
    - <span data-ttu-id="166fc-165">**로컬 컴퓨터에 다운로드**</span><span class="sxs-lookup"><span data-stu-id="166fc-165">**Download to local machine**</span></span>
    
    - <span data-ttu-id="166fc-166">**사용자 정의 Azure blob로 내보내기**:이 확인란을 선택 하는 경우 컨테이너 URL 및 SAS 토큰을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="166fc-166">**Export to user-defined Azure blob**: If this is checked, you can specify a container URL and SAS token.</span></span>
    
      > [!NOTE]
      > <span data-ttu-id="166fc-p115">내보내기 패키지가 사용자 정의 Azure blob에 저장 되 면 데이터는 더 이상 고급 eDiscovery로 관리 되지 않습니다. Azure blob에서 관리 됩니다. 즉, 사례를 삭제 하는 경우 내보낸 파일은 여전히 Azure blob에 남아 있게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="166fc-p115">Once an export package is stored to the user defined Azure blob, the data is no longer managed by Advanced eDiscovery; it's managed by the Azure blob. This means if you delete the case, the exported files will still remain on the Azure blob.</span></span> 
  
    - <span data-ttu-id="166fc-169">**향후 내보내기 세션을 위해 sas 토큰 저장**:이 옵션을 선택 하면 나중에 사용할 수 있도록 sas 토큰이 고급 eDiscovery의 내부 데이터베이스에 암호화 됩니다.</span><span class="sxs-lookup"><span data-stu-id="166fc-169">**Save SAS token for future export session**: If checked, the SAS token will be encrypted in the Advanced eDiscovery's internal database for future use.</span></span>
    
      > [!NOTE]
      > <span data-ttu-id="166fc-p116">현재 SAS 토큰은 매달 만료 됩니다. 1 개월 이상 후에 다운로드 하려고 하면 마지막 세션을 실행 취소 한 다음 다시 내보내십시오.</span><span class="sxs-lookup"><span data-stu-id="166fc-p116">Currently the SAS token expires after a month. If you try to download after more than a month you have to undo last session, then export again.</span></span> 
  
6. <span data-ttu-id="166fc-172">**수정을** 클릭 하 여 ' 검토용으로 ' 필드 설정을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="166fc-172">Click **Modify** to set the 'for review' field settings.</span></span> 
    
    ![내보내기 일괄 처리에 대 한 검토 필드 설정에 대 한 설정](media/39451aba-f6fe-4a01-8ed0-0be6a6ce889a.png)
  
   - <span data-ttu-id="166fc-p117">**검토 필드 설정**의 **시나리오 풀 선택** 목록에서 검토 시나리오 및 범위를 선택 합니다. 설정은 선택에 따라 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="166fc-p117">Under **For review field settings**, in **Select scenario** pull-down list, select the scenario and scope of the review. The settings are displayed based on your selection.</span></span>
    
      - <span data-ttu-id="166fc-176">**모두 검토** 기본값으로, 모든 전자 메일, 첨부 파일 및 문서가 기본적으로 선택 됩니다.</span><span class="sxs-lookup"><span data-stu-id="166fc-176">**Review all** (default): All emails, attachments, and documents are selected by default.</span></span> 
    
      - <span data-ttu-id="166fc-177">**한 집합의 모든 고유한 콘텐츠 검토**: Inclusives 및 고유 포함 복사본, 전자 메일 설정 수준의 고유 첨부 파일, 정확한 중복의 모든 집합에서 대표</span><span class="sxs-lookup"><span data-stu-id="166fc-177">**Review all unique content in a set**: Inclusives and unique inclusive copies, unique attachments in email set level, representative from every set of exact duplicates.</span></span>
    
      - <span data-ttu-id="166fc-178">**모든 고유한 콘텐츠를 집합-포함 안 함 복사본**(전자 메일 설정 수준의 Inclusives, 고유 첨부 파일)에서 모든 고유 항목을 검토 합니다.</span><span class="sxs-lookup"><span data-stu-id="166fc-178">**Review all unique content in a set - no inclusive copies**: Inclusives, unique attachments in email set level, representative from every set of exact duplicates.</span></span>
    
      - <span data-ttu-id="166fc-179">**모든 고유 콘텐츠 및 관련 패밀리 파일 검토**: Inclusives, 고유한 첨부 파일 전자 메일 집합 수준에서 정확한 복제본의 모든 집합에서 패밀리 파일을 포함 하도록 확장 합니다.</span><span class="sxs-lookup"><span data-stu-id="166fc-179">**Review all unique content and related family files**: Inclusives, unique attachments in email set level, representative from every set of exact duplicates, expand to include family files.</span></span>
    
      - <span data-ttu-id="166fc-p118">**사용자 지정** (대화 상자에서 옵션을 정의할 수 있음) 기본적으로는 현재 선택 항목을 유지 하 고 모든 대화 상자 옵션을 사용 하도록 설정 하 여 선택 항목을 허용 합니다. 이 옵션을 선택 하는 경우 전자 메일, 문서, 첨부 파일 및 기타에 대 한 설정을 사용자 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="166fc-p118">**Custom** (allows you to define the options in the dialog): The default is to keep current selections and enable all dialog options, to allow their selection. If you select this option, you can then customize the settings for emails, documents, attachments and miscellaneous.</span></span>
    
    - <span data-ttu-id="166fc-182">**전자 메일**에서 내보낼 전자 메일을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="166fc-182">Under **Emails**, select the emails you want to export.</span></span>
    
      - <span data-ttu-id="166fc-183">**모든 전자 메일**: (기본값) 모든 전자 메일이 선택 됩니다.</span><span class="sxs-lookup"><span data-stu-id="166fc-183">**All emails**: (default) All emails are selected.</span></span>
    
      - <span data-ttu-id="166fc-184">**Inclusives**: 포함 전자 메일은 스레드의 마지막 전자 메일이 며 스레드의 다른 모든 전자 메일을 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="166fc-184">**Inclusives**: An inclusive email is a last email of a thread, and it contains all the other emails from the thread.</span></span>
    
      - <span data-ttu-id="166fc-185">**Inclusives 및 고유 포함 복사본**: 제목, 본문 및 첨부 파일이 같은 포함 복사본과 Inclusives입니다. 고유한 포함 복사본은 이러한 전자 메일의 고유한 복사본입니다.</span><span class="sxs-lookup"><span data-stu-id="166fc-185">**Inclusives and unique inclusive copies**: Inclusive copies and inclusives with the same subject, body and attachments; unique inclusive copies are unique copies of these emails .</span></span>
    
    - <span data-ttu-id="166fc-186">**문서**아래에서 내보낼 문서를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="166fc-186">Under **Documents**, select the documents you want to export.</span></span> 
    
      - <span data-ttu-id="166fc-187">**모든 문서**: (기본값) 모든 문서를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="166fc-187">**All documents**: (default) All documents are selected.</span></span>
    
      - <span data-ttu-id="166fc-188">**피벗**: 집합을 검토할 때 일반적으로 기준으로 사용 되는 유사 항목 집합의 담당자로 선택한 파일입니다.</span><span class="sxs-lookup"><span data-stu-id="166fc-188">**Pivots**: A file chosen as representative of near-duplicates set, which is typically used as the baseline when reviewing the set.</span></span>
    
      - <span data-ttu-id="166fc-189">**모든 정확한 중복 집합의 담당자**: 고유한 중복 파일 (피벗 포함)입니다.</span><span class="sxs-lookup"><span data-stu-id="166fc-189">**Representative from every set of exact duplicates**: Unique near-duplicate files (including the pivot).</span></span>
    
    - <span data-ttu-id="166fc-190">**첨부 파일**에서 내보낼 첨부 파일을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="166fc-190">Under **Attachments**, select the attachments you want to export.</span></span> 
    
      - <span data-ttu-id="166fc-191">**모든 첨부 파일**: (기본값) 모든 첨부 파일이 선택 됩니다.</span><span class="sxs-lookup"><span data-stu-id="166fc-191">**All attachments**: (default) All attachments are selected.</span></span>
    
      - <span data-ttu-id="166fc-192">**대/소문자 수준에 지정 된 고유 첨부**파일: 지정한 대/소문자 내의 고유 첨부 파일이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="166fc-192">**Unique attachment in case level**: Unique attachment files within the specified case.</span></span>
    
      - <span data-ttu-id="166fc-193">**전자 메일 집합 수준의 고유 첨부**파일: 지정 된 전자 메일 사례 내의 고유한 첨부 파일이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="166fc-193">**Unique attachment in email set level**: Unique attachment files within the specified email case.</span></span>
    
   - <span data-ttu-id="166fc-p119">**Micellaneous**에서는 **첨부 파일을 문서로 취급**하거나, **전자 메일을 문서로 처리**하거나, **확장 하 여 패밀리 파일을 포함할**수 있습니다. 확장을 선택 하 여 **패밀리 파일을 포함**하는 경우, 검토에 플래그가 지정 된 각 파일에 대해 같은 패밀리의 모든 파일에도 플래그가 지정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="166fc-p119">Under**Micellaneous**, you can choose to **Treat attachments as documents**, **Treat emails as documents**, or **Expand to include family files**. When you choose **Expand to include family files**, for each file that is flagged for review, all files of the same family will also be flagged.</span></span>
    
7. <span data-ttu-id="166fc-196">**저장** 을 선택 하 여 설정을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="166fc-196">Choose **Save** to save the settings.</span></span> 
    
8. <span data-ttu-id="166fc-197">내보내기 매개 변수를 지정 하 고 일괄 처리 내보내기를 시작 하려면 **내보내기 세션 만들기**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="166fc-197">After you specify export parameters, to start export batch, click **Create export session**.</span></span>
    
    <span data-ttu-id="166fc-p120">내보내는 동안 상태는 **작업 상태**에 표시 됩니다. 결과가 **내보내기 요약**에 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="166fc-p120">During export, the status is displayed in **Task status**. The results are displayed in **Export summary**.</span></span>
    
9. <span data-ttu-id="166fc-200">**파일 다운로드** 창에서 **클립보드에 복사** 를 클릭 하 여 내보내기 키를 복사 합니다.</span><span class="sxs-lookup"><span data-stu-id="166fc-200">In the **Download files** window, click **Copy to clipboard** to copy the Export key.</span></span> 
    
    ![파일 다운로드](media/99cf2c13-4954-479f-9741-80d7458c1a15.png)
  
10. <span data-ttu-id="166fc-202">**닫기**를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="166fc-202">Click **Close**.</span></span> 
    
    <span data-ttu-id="166fc-203">eDiscovery 내보내기 도구가 시작 됩니다.</span><span class="sxs-lookup"><span data-stu-id="166fc-203">The eDiscovery Export Tool is started.</span></span>
    
    ![eDiscovery 내보내기](media/705756ca-ee97-4d24-b70f-8b23513f6d11.gif)
  
11. <span data-ttu-id="166fc-205">**eDiscovery 내보내기 도구**에서 다음을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="166fc-205">In the **eDiscovery Export Tool**:</span></span>
    
    -  <span data-ttu-id="166fc-206">**원본에 연결 하는 데 사용할 공유 액세스 서명 붙여넣기**에서 7 단계에서 클립보드에 복사 했던 내보내기 키를 붙여 넣습니다.</span><span class="sxs-lookup"><span data-stu-id="166fc-206">In **Paste the Shared Access Signature that will be used to connect to the source**, paste the Export key that youcopied to the clipboard in step 7.</span></span>
    
    - <span data-ttu-id="166fc-207">**찾아보기를** 클릭 하 여 다운로드 한 내보내기 파일을 로컬 컴퓨터에 저장할 대상 위치를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="166fc-207">Click **Browse** to select the target location for storing the downloaded export files on the local machine.</span></span> 
    
    - <span data-ttu-id="166fc-p121">**시작**을 클릭 합니다. 내보내기 파일이 로컬 컴퓨터로 다운로드 됩니다. 4 단계에서 **사용자 정의 Azure blob로 내보내기를** 선택한 경우 세션을 선택한 blob 저장소 URL 대상으로 내보냅니다.</span><span class="sxs-lookup"><span data-stu-id="166fc-p121">Click **Start**.The export files are downloaded to the local machine. If you chose **Export to user-defined Azure blob** in step 4, the session is exported to a Blob storage URL destination of your choosing.</span></span>
    
<span data-ttu-id="166fc-210">내보내기 보고서의 필드에 대 한 자세한 설명은 [보고서 필드 내보내기를](export-report-fields-in-advanced-ediscovery.md)참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="166fc-210">For a full description of the fields in the export report, see [Export report fields](export-report-fields-in-advanced-ediscovery.md).</span></span>
  
## <a name="export-report-output-files"></a><span data-ttu-id="166fc-211">보고서 출력 파일 내보내기</span><span class="sxs-lookup"><span data-stu-id="166fc-211">Export report output files</span></span>
<span data-ttu-id="166fc-212"><a name="BK_ExportOutputFIles"> </a></span><span class="sxs-lookup"><span data-stu-id="166fc-212"></span></span>

<span data-ttu-id="166fc-213">다음 표에서는 내보내기 일괄 처리를 실행할 때 생성 되는 출력 파일을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="166fc-213">The following table lists the output files that are generated when you run an Export batch.</span></span>
  
|<span data-ttu-id="166fc-214">**파일 이름**</span><span class="sxs-lookup"><span data-stu-id="166fc-214">**File name**</span></span>|<span data-ttu-id="166fc-215">**파일 형식**</span><span class="sxs-lookup"><span data-stu-id="166fc-215">**File type**</span></span>|<span data-ttu-id="166fc-216">**설명**</span><span class="sxs-lookup"><span data-stu-id="166fc-216">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="166fc-217">내보내기 요약</span><span class="sxs-lookup"><span data-stu-id="166fc-217">Export summary</span></span>  <br/> |<span data-ttu-id="166fc-218">cs</span><span class="sxs-lookup"><span data-stu-id="166fc-218">csv</span></span>  <br/> |<span data-ttu-id="166fc-219">eDiscovery 내보내기 도구에서 생성 하는 로그 파일입니다.</span><span class="sxs-lookup"><span data-stu-id="166fc-219">A log file generated by the eDiscovery Export Tool.</span></span>  <br/> |
|<span data-ttu-id="166fc-220">추적은</span><span class="sxs-lookup"><span data-stu-id="166fc-220">Trace</span></span>  <br/> |<span data-ttu-id="166fc-221">txt</span><span class="sxs-lookup"><span data-stu-id="166fc-221">txt</span></span>  <br/> |<span data-ttu-id="166fc-222">eDiscovery 내보내기 도구에서 생성 하는 로그 파일입니다.</span><span class="sxs-lookup"><span data-stu-id="166fc-222">A log file generated by the eDiscovery Export Tool.</span></span>  <br/> |
|<span data-ttu-id="166fc-223">추출 된 텍스트 파일</span><span class="sxs-lookup"><span data-stu-id="166fc-223">Extracted text files</span></span>  <br/> |<span data-ttu-id="166fc-224">파일 폴더</span><span class="sxs-lookup"><span data-stu-id="166fc-224">File folder</span></span>  <br/> |<span data-ttu-id="166fc-225">내보낸 파일의 추출 된 텍스트 파일이 들어 있는 폴더입니다.</span><span class="sxs-lookup"><span data-stu-id="166fc-225">Folder that contains the extracted text files of the exported files.</span></span>  <br/> |
|<span data-ttu-id="166fc-226">입력 또는 네이티브 파일</span><span class="sxs-lookup"><span data-stu-id="166fc-226">Input or native files</span></span>  <br/> |<span data-ttu-id="166fc-227">파일 폴더</span><span class="sxs-lookup"><span data-stu-id="166fc-227">File folder</span></span>  <br/> |<span data-ttu-id="166fc-228">내보낸 파일의 네이티브 파일 및 입력 파일이 들어 있는 폴더입니다.</span><span class="sxs-lookup"><span data-stu-id="166fc-228">Folder that contains the native and input files of the exported files.</span></span>  <br/> |
|<span data-ttu-id="166fc-229">목록 내보내기</span><span class="sxs-lookup"><span data-stu-id="166fc-229">Export list</span></span>  <br/> |<span data-ttu-id="166fc-230">xlsx</span><span class="sxs-lookup"><span data-stu-id="166fc-230">xlsx</span></span>  <br/> |<span data-ttu-id="166fc-p122">파일 메타 데이터를 .xlsx 형식으로 내보냈습니다. 파일의 필드는 사용자가 선택 하는 서식 파일에 따라 결정 됩니다. 필요한 경우 여러 파일이 생성 되 고 각 파일에는 150k 행이 포함 됩니다. Excel 셀에 포함할 수 있는 것 보다 많은 문자를 특정 값에 포함 하는 경우 (현재 제한은 32767 자)이 값은 허용 되는 최대 길이에 맞게 잘립니다. 값을 트리밍한 경우 셀의 배경색은 사용자에 게 표시 되는 빨간색입니다. " 전자 메일 참가자 "는 전자 메일이 대규모 배포로 전송 된 경우 길이 제한을 초과할 수 있는 필드의 예입니다. 출력 필드에 대 한 자세한 내용은 [보고서 필드 내보내기를](export-report-fields-in-advanced-ediscovery.md) 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="166fc-p122">Exported files metadata in xlsx format. Fields in files are according to template user selects to export. If needed, several files are created, each contains 100-150K rows. If a certain value contains more characters than an Excel cell can contain (currently the limit is 32,767 characters), then the value will be trimmed to the maximum length allowed. If a value is trimmed, the cell's background color is red to indicate this to the user."Email participants" is an example of a field that can exceed the length limit, if the email was sent to a large distribution. See [Export report fields](export-report-fields-in-advanced-ediscovery.md) for details about the output fields.  </span></span><br/> |
|<span data-ttu-id="166fc-237">파일 로드</span><span class="sxs-lookup"><span data-stu-id="166fc-237">Load file</span></span>  <br/> |<span data-ttu-id="166fc-238">cs</span><span class="sxs-lookup"><span data-stu-id="166fc-238">csv</span></span>  <br/> |<span data-ttu-id="166fc-p123">다른 응용 프로그램에 로드 하기 위해 내보낸 파일 메타 데이터가 csv 형식으로 내보내집니다. 파일의 필드는 사용자가 선택 하는 서식 파일에 따라 결정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="166fc-p123">Exported files metadata in csv format for loading into a different application. Fields in files are according to template user selects to export.</span></span>  <br/> |
|<span data-ttu-id="166fc-241">성공 지표</span><span class="sxs-lookup"><span data-stu-id="166fc-241">Success indicator</span></span>  <br/> |<span data-ttu-id="166fc-242">txt</span><span class="sxs-lookup"><span data-stu-id="166fc-242">txt</span></span>  <br/> |<span data-ttu-id="166fc-p124">타사 Azure blob로 내보낼 때만 만들어집니다. 내보내기가 완전히 완료 되 면 파일이 만들어집니다. 실패의 경우 또는 부분적으로 성공 하는 경우 파일을 만들지 않습니다. 파일은 루트 폴더에 만들어지므로 서로 다른 내보내기 일괄 처리/세션 상태에 대 한 자동화 된 추적을 허용 합니다. 빈 파일입니다. 이름은 TenantId_CaseId_ExternalCaseId_CaseName_ExportBatchId_SessionId_DateTime입니다.</span><span class="sxs-lookup"><span data-stu-id="166fc-p124">Only created when exporting to a 3rd party Azure blob. If export succeed completely, the file will be created. In case of failure, or partial success the file will not be created. File will be created in the root folder, allowing automated tracking on different Export batches/sessions statuses. This is an empty file. Its name is: TenantId_CaseId_ExternalCaseId_CaseName_ExportBatchId_SessionId_DateTime.txt.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="166fc-249">참고 항목</span><span class="sxs-lookup"><span data-stu-id="166fc-249">See also</span></span>

[<span data-ttu-id="166fc-250">Office 365 Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="166fc-250">Office 365 Advanced eDiscovery</span></span>](office-365-advanced-ediscovery.md)
  
[<span data-ttu-id="166fc-251">일괄 처리 기록 보기 및 이전 결과 내보내기</span><span class="sxs-lookup"><span data-stu-id="166fc-251">Viewing batch history and exporting past results</span></span>](view-batch-history-and-export-past-results.md)
  
[<span data-ttu-id="166fc-252">Office 365 Advanced eDiscovery에 대한 빠른 설정</span><span class="sxs-lookup"><span data-stu-id="166fc-252">Quick setup for Office 365 Advanced eDiscovery</span></span>](quick-setup-for-advanced-ediscovery.md)

[<span data-ttu-id="166fc-253">보고서 필드 내보내기</span><span class="sxs-lookup"><span data-stu-id="166fc-253">Export report fields</span></span>](export-report-fields-in-advanced-ediscovery.md)
  
[<span data-ttu-id="166fc-254">Office 365에서 eDiscovery 검색 결과를 내보낼 때 다운로드 속도 높이기</span><span class="sxs-lookup"><span data-stu-id="166fc-254">Increase the download speed when exporting eDiscovery search results from Office 365</span></span>](increase-download-speeds-when-exporting-ediscovery-results.md)

