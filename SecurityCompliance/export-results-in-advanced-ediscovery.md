---
title: Office 365 Advanced eDiscovery 결과 내보내기
ms.author: chrfox
author: chrfox
manager: laurawi
ms.date: 9/14/2017
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: a9951a07-10b3-48cb-b37a-0ffaa24931ad
description: '결과 내보내기 일괄 처리에 대 한 매개 변수를 지정 하는 절차를 포함 하 여 Office 365 고급 eDiscovery에서 내보내기에 대 한 옵션을 정의 하는 방법에 알아봅니다. '
ms.openlocfilehash: 49dab9820735af3bf5c322fc531c78a6baab2f8e
ms.sourcegitcommit: 7e2a0185cadea7f3a6afc5ddc445eac2e1ce22eb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/11/2019
ms.locfileid: "29559051"
---
# <a name="export-results-in-office-365-advanced-ediscovery"></a><span data-ttu-id="61136-103">Office 365 Advanced eDiscovery 결과 내보내기</span><span class="sxs-lookup"><span data-stu-id="61136-103">Export results in Office 365 Advanced eDiscovery</span></span>

> [!NOTE]
> <span data-ttu-id="61136-p101">Advanced eDiscovery를 사용하려면 Office 365 E3의 고급 준수 추가 기능이나 조직을 위한 E5 구독이 필요합니다. 이 요금제가 없는 상태에서 Advanced eDiscovery를 사용하려는 경우에는 [Office 365 Enterprise E5 평가판을 등록](https://go.microsoft.com/fwlink/p/?LinkID=698279)할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="61136-p101">Advanced eDiscovery requires an Office 365 E3 with the Advanced Compliance add-on or an E5 subscription for your organization. If you don't have that plan and want to try Advanced eDiscovery, you can [sign up for a trial of Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span></span> 
  
<span data-ttu-id="61136-106">이 항목에서는 고급 eDiscovery 내보내기 설치 옵션에 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="61136-106">This topic describes the Advanced eDiscovery Export Setup options.</span></span>
  
 <span data-ttu-id="61136-107">**이 항목의 내용:**</span><span class="sxs-lookup"><span data-stu-id="61136-107">**In this topic:**</span></span>
  
- [<span data-ttu-id="61136-108">내보내기 일괄 처리 및 세션 정의</span><span class="sxs-lookup"><span data-stu-id="61136-108">Defining export batches and sessions</span></span>](export-results-in-advanced-ediscovery.md#BK_Define)
    
- [<span data-ttu-id="61136-109">증분 및 추가 내보내기</span><span class="sxs-lookup"><span data-stu-id="61136-109">Incremental and additional exports</span></span>](export-results-in-advanced-ediscovery.md#BK_IncrementalReports)
    
- [<span data-ttu-id="61136-110">일괄 내보내기 매개 변수를 설정</span><span class="sxs-lookup"><span data-stu-id="61136-110">Set up batch export parameters</span></span>](export-results-in-advanced-ediscovery.md#BK_SetUpExport)
    
- [<span data-ttu-id="61136-111">보고서 출력 파일 내보내기</span><span class="sxs-lookup"><span data-stu-id="61136-111">Export report output files</span></span>](export-results-in-advanced-ediscovery.md#BK_ExportOutputFIles)
    
## <a name="defining-export-batches-and-sessions"></a><span data-ttu-id="61136-112">내보내기 일괄 처리 및 세션 정의</span><span class="sxs-lookup"><span data-stu-id="61136-112">Defining export batches and sessions</span></span>
<span data-ttu-id="61136-113"><a name="BK_Define"> </a></span><span class="sxs-lookup"><span data-stu-id="61136-113"></span></span>

<span data-ttu-id="61136-p102">정의 된 매개 변수 집합을 사용 하 여 내보내기 처리를 허용 하는 내보내기 배치 합니다. 고급 eDiscovery를 사용 하면 각 내보내기 사용자 지정 하려면 일괄 처리를 정의할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="61136-p102">An export batch allows export processing using a set of defined parameters. Advanced eDiscovery enables you to define batches to customize each export.</span></span>
  
<span data-ttu-id="61136-p103">매개 변수는 일괄 내보내기 당 정의 됩니다. "01 일괄 내보내기" 라는 일괄 처리의 경우 첫번째 일괄 처리에 대 한 기본적으로 만들어집니다. 일괄 처리 이름 및 설명을 편집할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="61136-p103">Parameters are defined per export batch. A batch named "Export batch 01" is created by default for the first batch of a case. You can also edit the batch name and description.</span></span>
  
<span data-ttu-id="61136-119">내보내기 세션은 내보내기 일괄 내에서 고급 eDiscovery 내보내기를 실행 하는 세션입니다.</span><span class="sxs-lookup"><span data-stu-id="61136-119">An export session is an execution of Advanced eDiscovery Export within an export batch.</span></span>
  
## <a name="incremental-and-additional-exports"></a><span data-ttu-id="61136-120">증분 및 추가 내보내기</span><span class="sxs-lookup"><span data-stu-id="61136-120">Incremental and additional exports</span></span>
<span data-ttu-id="61136-121"><a name="BK_IncrementalReports"> </a></span><span class="sxs-lookup"><span data-stu-id="61136-121"></span></span>

<span data-ttu-id="61136-p104">동일한 내보내기 서식 파일 및 매개 변수를 기준으로 일관 된 결과 확인 하는 내보내기 일괄 처리 내의 여러 내보내기 세션을 실행할 수 있습니다. 일괄 처리 내에서 각 세션에 대해 내보낼 수 새로 사례 데이터를 처리 하 고 각 "늘립니다." 처리에 대 한 분석</span><span class="sxs-lookup"><span data-stu-id="61136-p104">You can run multiple export sessions within an export batch, to ensure consistent results based on the same export template and parameters. For each session within a batch, you can export analytics for newly processed case data and process each "incrementally."</span></span>
  
<span data-ttu-id="61136-p105">다른 매개 변수 집합을 사용 하 여 내보내기, 하기 위해 먼저 해야 새 일괄 처리를 만듭니다. 새 일괄 처리의 첫번째 세션에는 이러한 파일 가져오고 하나 또는 여러 Imports를 통해 처리 된 여부에 따라 대/소문자 지금까지 처리 하는 파일에 대 한 결과가 생성 됩니다. 위치별, 다음과 비슷한, inclusives 등에 다시 계산 하는 각 일괄 처리 합니다. 세션 일괄 처리에 대해 정의 된 매개 변수를 사용 하 고 각 세션 실행에 대해 위치별, 다음과 비슷한, inclusives 등 다시 계산 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="61136-p105">In order to export using a different set of parameters, you first need to create a new batch. The first session in the new batch will produce results for files processed in the case so far, whether or not these files were imported and processed over one or multiple Imports. Each batch recalculates pivots, similarity, inclusives, etc. Sessions use the parameters defined for the batch and do not recalculate pivots, similarity, inclusives, etc. for each session execution.</span></span>
  
<span data-ttu-id="61136-p106">예, 해당 데이터를 분석 하 고 사례를 가져온 가정 합니다. 중복 근처 및 증분 데이터에 대 한 전자 메일 스레딩 결과 검색 하기 위해 이전에 데이터를 내보낼 때 사용한 동일한 일괄 처리의 **만들기 내보내기 세션을** 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="61136-p106">For example, assume a case was imported and its data analyzed. In order to retrieve Near-duplicates and Email Threading results for the incremental data, click **Create export session** in the same batch that was previously used to export data.</span></span> 
  
## <a name="set-up-batch-export-parameters"></a><span data-ttu-id="61136-129">일괄 내보내기 매개 변수를 설정</span><span class="sxs-lookup"><span data-stu-id="61136-129">Set up batch export parameters</span></span>
<span data-ttu-id="61136-130"><a name="BK_SetUpExport"> </a></span><span class="sxs-lookup"><span data-stu-id="61136-130"></span></span>

<span data-ttu-id="61136-p107">EDiscovery 내보내기 도구는 로컬 컴퓨터에 고급 eDiscovery에서 검색 결과 내보내는 데 사용 됩니다. 데이터 전송 처리량과 인해 물거품이 내보내기 프로세스를 늘리려면 검색 결과 내보내는 데 사용 하는 컴퓨터에서 Windows 레지스트리 설정을 구성할 수 있습니다. 다운로드 속도 높입니다. 하려는 경우 내보내기 매개 변수를 설정 하기 전에 레지스트리 설정을 구성 합니다. 자세한 내용은 [Office 365에서 eDiscovery 검색 결과 내보낼 때 다운로드 속도 높입니다.](increase-download-speeds-when-exporting-ediscovery-results.md)을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="61136-p107">The eDiscovery Export Tool is used to export search results from Advanced eDiscovery to your local computer. To increase the data transfer throughput and speed-up the export process, you can configure a Windows Registry setting on the computer that you use to export the search results. If you'd like to increase the download speed, configure the registry setting before you set up the export parameters. For more information, see [Increase the download speed when exporting eDiscovery search results from Office 365](increase-download-speeds-when-exporting-ediscovery-results.md).</span></span>
  
1. <span data-ttu-id="61136-135">고급 ediscovery에서 사례를 선택 하 고 **내보내기를** 클릭 \> **설치**합니다.</span><span class="sxs-lookup"><span data-stu-id="61136-135">In Advanced eDiscovery, select a Case and click **Export** \> **Setup**.</span></span>
    
    - <span data-ttu-id="61136-136">**일괄 처리를 내보내기** 목록에서 일괄 처리 이름을 선택 하거나 내보내기 일괄 01, (기본 일괄 처리)에 결과 내보냅니다.</span><span class="sxs-lookup"><span data-stu-id="61136-136">From the **Export batch** list, select the batch name or export results to Export batch 01, (the default batch).</span></span> 
    
    - <span data-ttu-id="61136-p108">기존 사례에 추가한 새 파일에 대 한 결과 내보내려면 계속 하 여 현재 일괄 처리 진행 합니다. 일괄 처리의 세션을 만들려면 동일한 일괄 처리 수를 선택 하 고 **만들기 내보내기 세션을** 클릭 하는 증분 방식으로 이전 일괄 처리로 동일한 매개 변수를 내보내려면이 옵션을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="61136-p108">To export results for new files that you added to an existing case, continue with your current batch. To create a session in the batch, select the same batch number and click **Create export session** You can use this option to export the same parameters as the previous batch, in an incremental manner.</span></span> 
    
    - <span data-ttu-id="61136-p109">새 일괄 처리를 내보내려면 **추가** 클릭 ![추가 아이콘](media/c2dd8b3a-5a22-412c-a7fa-143f5b2b5612.png)및 **일괄 처리 이름** 에 새 이름을 입력 (하거나 기본값을 그대로) 및 **일괄 처리 설명**에서 설명 합니다. **확인**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="61136-p109">To export to a new batch, click **Add** ![add icon](media/c2dd8b3a-5a22-412c-a7fa-143f5b2b5612.png)and enter a new name in **Batch name** (or accept the default) and a description in **Batch description**. Click **OK**.</span></span>
    
    - <span data-ttu-id="61136-141">일괄 처리 이름 또는 설명을 편집 하려면 **일괄 내보내기**의 이름을 선택, **편집** 을 클릭 하 ![편집 아이콘](media/3d613660-7602-4df2-bdb9-14e9ca2f9cf2.png), 다음 필드를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="61136-141">To edit a batch name or description, select the name in **Export batch**, click **Edit** ![Edit icon](media/3d613660-7602-4df2-bdb9-14e9ca2f9cf2.png), and then modify the fields.</span></span>
    
      > [!NOTE]
      > <span data-ttu-id="61136-p110">내보내기 일괄 처리에 대 한 세션을 실행 했을 때 한 후에 삭제할 수 없습니다. 또한 첫번째 세션 실행 되 면 일부 매개 변수를 편집할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="61136-p110">After you've run sessions for an export batch, they cannot be deleted. In addition, only some parameters can be edited once the first session is run.</span></span> 
  
    - <span data-ttu-id="61136-144">중복 내보내기 일괄 처리를 만들려면 **중복 내보내기 일괄 처리** 를 선택 ![중복 내보내기 일괄 처리 아이콘을 만드는](media/3f6d5f59-e842-4946-a493-473528af0119.jpg) 하 고 패널에 이름과 중복 일괄 처리에 대 한 설명을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="61136-144">To create a duplicate export batch, choose **Duplicate export batch** ![Create a duplicate export batch icon](media/3f6d5f59-e842-4946-a493-473528af0119.jpg) and enter a name and a description for the duplicate batch in the panel.</span></span> 
    
    - <span data-ttu-id="61136-145">내보내기 일괄 처리를 삭제 하려면 **삭제** 를 선택 ![내보내기 일괄 처리 아이콘을 삭제](media/92a9f8e0-d469-48da-addb-69365e7ffb6f.jpg)합니다.</span><span class="sxs-lookup"><span data-stu-id="61136-145">To delete an export batch, choose **Delete** ![Delete an export batch icon](media/92a9f8e0-d469-48da-addb-69365e7ffb6f.jpg).</span></span>
    
    - <span data-ttu-id="61136-146">일괄 처리의 기록을 보려면, **일괄 처리 기록** 선택 ![보기 기록 아이콘](media/a80cc320-d96c-4d91-8884-75fe2cb147e2.jpg)합니다.</span><span class="sxs-lookup"><span data-stu-id="61136-146">To view the history of a batch, choose **Batch history** ![View history icon](media/a80cc320-d96c-4d91-8884-75fe2cb147e2.jpg).</span></span>
    
2. <span data-ttu-id="61136-147">**모집단**내보내기 일괄 처리에 대 한 설정을 세부적으로 조정 하려는 경우 **관련성 제한 점수 위에 파일만 포함** 및/또는 **구체화 내보내기 일괄 처리** 를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="61136-147">Under **Population**, select **Include only files above Relevance cut-off score** and/or **Refine export batch** if you want to fine-tune the settings for your export batch.</span></span> 
    
3. <span data-ttu-id="61136-p111">**관련성 제한 점수 위에 파일만 포함**을 선택 하는 경우 **문제** 를 사용할 수 있습니다. 파일의 관련성 점수를 선택한 문제에 대 한 제한 점수 보다 더 높은 경우에 '검토'에 대 한 필터에 의해 제외 되는 파일이 내보내집니다.</span><span class="sxs-lookup"><span data-stu-id="61136-p111">If you select **Include only files above Relevance cut-off score**, then the **Issue** is enabled. If the file's relevance score is higher than the cut-off score for the selected issue, the file will be exported unless it's excluded by the 'For review' filter.</span></span> 
  
    <span data-ttu-id="61136-p112">**구체화 내보내기 일괄 처리**선택 하는 경우는 **dupe 해제** 하 고 필터 '검토' 하 여 필드 라디오 단추를 사용할 수 있습니다. 선택 하는 경우 **취소 dupe**, 중복 파일에 정의 된 정책에 따라 필터링 됩니다 다음 [수준 (기본값) 경우: 모든 집합이 중복 파일을 사용할 수 있는 전체 대/소문자에서 하나를 제외한 모든 파일 duped 해제 됩니다. 더불어 수준: 모든 집합이 중복 파일을 동일한 더불어 중에서 하나를 제외한 모든 파일 duped 해제 됩니다.] 모든 중복 파일의 레코드를 포함 하는 내보내기 출력 합니다. **'검토용' 하 여 필터** 필드를 선택 하는 경우 **'검토용'** 필드 설정을 입력 하 **는 메타 데이터에서 수정** 선택 합니다. 패키지 콘텐츠의 원본 파일을 포함 하도록 **포함 입력된 파일** 선택 합니다. 이 설정은 내보내기 프로세스의 속도 지울 수 있습니다. 참고 네이티브 파일을 사용 하 든 내보낼 수는 있습니다.</span><span class="sxs-lookup"><span data-stu-id="61136-p112">If you select **Refine export batch**, the **De-dupe** and Filter by 'For review' field radio buttons are enabled. If you choose **De-dupe**, then duplicate files will be filtered out according to the policy defined [Case level (default): from every set of duplicate files in the entire case, all but one file will be de-duped. Custodian level: from every set of duplicate files of the same custodian, all but one file will be de-duped.] The export output contains a record of all duplicate files. If you choose **Filter by 'For review'** field, select **Modify under Metadata** to enter your **'For review'** field settings. Select **Include input files** to include source files in the package content. You can clear this setting to speed up the export process. Note that the Native files will be exported in any case.</span></span> 
    
4. <span data-ttu-id="61136-157">**메타 데이터**(세션) 당한 번씩 **서식 파일 내보내기** 목록에서 다음 옵션 중에서 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="61136-157">Under **Metadata**, select from the following options in the **Export template** list (once per session).</span></span> 
    
    - <span data-ttu-id="61136-p113">**표준**: 데이터 항목, 메타 데이터, 및 속성의 기본 설정 합니다. 데이터 가져오기 고급 eDiscovery에 이미 처리 된 및 내보내기 데이터는 이미 있는 파일을 포함 하는 시스템에 업로드 하는 경우이 옵션을 사용 합니다. 기본적으로 열을 만들고 채워야는 서식 파일을 내보냅니다.</span><span class="sxs-lookup"><span data-stu-id="61136-p113">**Standard**: Basic set of data items, metadata, and properties. Use this option when import data was already processed in Advanced eDiscovery and export data is uploaded to a system that already contains the files. By default, export template columns are created and filled.</span></span>
    
    - <span data-ttu-id="61136-p114">**모든**: 모든 처리 데이터와 분석 및 관련성 점수를 포함 하 여 표준 메타 데이터의 전체 집합입니다. 이 서식 파일은 처리를 수행 하는 고급 eDiscovery 및 파일 데이터를 처음으로 외부 시스템에 업로드 되는 경우에 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="61136-p114">**All**: Full set of standard metadata including all processing data, as well as Analyze and Relevance scores. This template is required when Advanced eDiscovery performs the processing and file data is uploaded to an external system for the first time.</span></span>
    
    - <span data-ttu-id="61136-163">**문제**: **모든 문제** 를 선택 하거나 만든 특정 문제를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="61136-163">**Issues**: Select **All Issues** or select a particular issue you have created.</span></span> 
    
5. <span data-ttu-id="61136-164">**대상**아래에서:</span><span class="sxs-lookup"><span data-stu-id="61136-164">Under **Destination**:</span></span>
    
    - <span data-ttu-id="61136-165">**로컬 컴퓨터에 다운로드**</span><span class="sxs-lookup"><span data-stu-id="61136-165">**Download to local machine**</span></span>
    
    - <span data-ttu-id="61136-166">**사용자 정의 Azure blob로 내보내기**:이 검사 하는 경우에 컨테이너 URL 및 SAS 토큰을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="61136-166">**Export to user-defined Azure blob**: If this is checked, you can specify a container URL and SAS token.</span></span>
    
      > [!NOTE]
      > <span data-ttu-id="61136-p115">사용자 정의 Azure blob, 고급 eDiscovery; 더이상 데이터를 관리 하는 내보내기 패키지에 저장 된 후 Azure blob 하 여이 기능을 관리 합니다. 내보낸된 파일 Azure blob에 그대로 남습니다 대/소문자를 삭제 하면 것을 의미 합니다.</span><span class="sxs-lookup"><span data-stu-id="61136-p115">Once an export package is stored to the user defined Azure blob, the data is no longer managed by Advanced eDiscovery; it's managed by the Azure blob. This means if you delete the case, the exported files will still remain on the Azure blob.</span></span> 
  
    - <span data-ttu-id="61136-169">**향후 내보내기 세션에 대 한 저장 SAS 토큰**: SAS 토큰 선택 하는 경우 나중에 사용할 수에 대 한 고급 eDiscovery의 내부 데이터베이스에서 암호화 됩니다.</span><span class="sxs-lookup"><span data-stu-id="61136-169">**Save SAS token for future export session**: If checked, the SAS token will be encrypted in the Advanced eDiscovery's internal database for future use.</span></span>
    
      > [!NOTE]
      > <span data-ttu-id="61136-p116">현재 달 후 SAS 토큰 만료 됩니다. 마지막 세션을 취소 하려면 해야 달 이상 후 다운로드 하려고 하는 경우 다시 내보내기 합니다.</span><span class="sxs-lookup"><span data-stu-id="61136-p116">Currently the SAS token expires after a month. If you try to download after more than a month you have to undo last session, then export again.</span></span> 
  
6. <span data-ttu-id="61136-172">**수정** '검토용' 필드 설정을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="61136-172">Click **Modify** to set the 'for review' field settings.</span></span> 
    
    ![내보내기 배치에 대 한 검토 필드 설정에 대 한 설정](media/39451aba-f6fe-4a01-8ed0-0be6a6ce889a.png)
  
   - <span data-ttu-id="61136-p117">에서 **검토 필드 설정에 대 한** **시나리오 선택** 풀 다운 목록에서 시나리오 및 검토의 범위를 선택 합니다. 설정은 선택에 따라 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="61136-p117">Under **For review field settings**, in **Select scenario** pull-down list, select the scenario and scope of the review. The settings are displayed based on your selection.</span></span>
    
      - <span data-ttu-id="61136-176">**모든 검토** (기본값): 모든 전자 메일, 첨부 파일 및 문서는 기본적으로 선택 됩니다.</span><span class="sxs-lookup"><span data-stu-id="61136-176">**Review all** (default): All emails, attachments, and documents are selected by default.</span></span> 
    
      - <span data-ttu-id="61136-177">**집합의 모든 고유한 콘텐츠 검토**: 전자 메일에서 고유한 첨부 파일 설정 수준, 정확 하 게 중복 되는 값의 모든 집합에서 대표 Inclusives 및 고유 포괄 복사본입니다.</span><span class="sxs-lookup"><span data-stu-id="61136-177">**Review all unique content in a set**: Inclusives and unique inclusive copies, unique attachments in email set level, representative from every set of exact duplicates.</span></span>
    
      - <span data-ttu-id="61136-178">**설정-없음 (포함) 복사본의에서 모든 고유한 콘텐츠 검토**: Inclusives, 전자 메일에서 고유한 첨부 파일 수준, 정확 하 게 중복 되는 값의 모든 집합에서 담당자를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="61136-178">**Review all unique content in a set - no inclusive copies**: Inclusives, unique attachments in email set level, representative from every set of exact duplicates.</span></span>
    
      - <span data-ttu-id="61136-179">**파일을 검토 모든 고유한 콘텐츠 및 관련 가족**: Inclusives, 전자 메일 설정 수준, 정확 하 게 중복 항목의 모든 집합에서 담당자에 게 고유 첨부 파일을 가족 파일을 포함 하도록 확장 합니다.</span><span class="sxs-lookup"><span data-stu-id="61136-179">**Review all unique content and related family files**: Inclusives, unique attachments in email set level, representative from every set of exact duplicates, expand to include family files.</span></span>
    
      - <span data-ttu-id="61136-p118">**사용자 정의** (옵션 대화 상자에서 정의할 수 있습니다): 기본적으로 현재 선택 항목을 유지 하 고 해당 선택 영역을 허용 하려면 모든 대화 상자 옵션을 사용 하도록 설정 됩니다. 이 옵션을 선택 하는 경우 다음 사용자 지정할 수 있습니다 전자 메일, 문서, 첨부 파일에 대 한 설정 및 기타 합니다.</span><span class="sxs-lookup"><span data-stu-id="61136-p118">**Custom** (allows you to define the options in the dialog): The default is to keep current selections and enable all dialog options, to allow their selection. If you select this option, you can then customize the settings for emails, documents, attachments and miscellaneous.</span></span>
    
    - <span data-ttu-id="61136-182">**전자 메일**내보낼 전자 메일을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="61136-182">Under **Emails**, select the emails you want to export.</span></span>
    
      - <span data-ttu-id="61136-183">**모든 전자 메일**: (기본값) 모든 전자 메일을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="61136-183">**All emails**: (default) All emails are selected.</span></span>
    
      - <span data-ttu-id="61136-184">**Inclusives**: (포함) 전자 메일은 마지막 전자 메일 프로그램 스레드의 되 고 스레드에서 모든 전자 메일이 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="61136-184">**Inclusives**: An inclusive email is a last email of a thread, and it contains all the other emails from the thread.</span></span>
    
      - <span data-ttu-id="61136-185">**고유 (포함) 복사본 및 Inclusives**: 포괄 복사본과 동일한 제목, 본문 및 첨부 파일; inclusives 고유 (포함) 복사본은 이러한 전자 메일의 고유한 복사본입니다.</span><span class="sxs-lookup"><span data-stu-id="61136-185">**Inclusives and unique inclusive copies**: Inclusive copies and inclusives with the same subject, body and attachments; unique inclusive copies are unique copies of these emails .</span></span>
    
    - <span data-ttu-id="61136-186">**문서**내보낼 문서를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="61136-186">Under **Documents**, select the documents you want to export.</span></span> 
    
      - <span data-ttu-id="61136-187">**모든 문서**: (기본값) 모든 문서를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="61136-187">**All documents**: (default) All documents are selected.</span></span>
    
      - <span data-ttu-id="61136-188">**위치별**: 파일 집합을 검토할 때 기준선으로 일반적으로 사용 되는 중복 근처 집합의 대표으로 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="61136-188">**Pivots**: A file chosen as representative of near-duplicates set, which is typically used as the baseline when reviewing the set.</span></span>
    
      - <span data-ttu-id="61136-189">**정확 하 게 중복 되는 값의 모든 집합에서 대표**: 고유 거의 중복 된 파일 (피벗 포함).</span><span class="sxs-lookup"><span data-stu-id="61136-189">**Representative from every set of exact duplicates**: Unique near-duplicate files (including the pivot).</span></span>
    
    - <span data-ttu-id="61136-190">**첨부 파일**을 내보낼 첨부 파일을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="61136-190">Under **Attachments**, select the attachments you want to export.</span></span> 
    
      - <span data-ttu-id="61136-191">**모든 첨부 파일**: (기본값) 모든 첨부 파일이 선택 됩니다.</span><span class="sxs-lookup"><span data-stu-id="61136-191">**All attachments**: (default) All attachments are selected.</span></span>
    
      - <span data-ttu-id="61136-192">**사례 수준에서 고유한 첨부 파일**: 지정된 된 사례 내에서 고유 첨부 파일입니다.</span><span class="sxs-lookup"><span data-stu-id="61136-192">**Unique attachment in case level**: Unique attachment files within the specified case.</span></span>
    
      - <span data-ttu-id="61136-193">**전자 메일에 고유한 첨부 파일 수준 설정**: 지정 된 전자 메일 대/소문자 내에서 고유 첨부 파일입니다.</span><span class="sxs-lookup"><span data-stu-id="61136-193">**Unique attachment in email set level**: Unique attachment files within the specified email case.</span></span>
    
   - <span data-ttu-id="61136-p119">**Micellaneous** **문서로 첨부 파일 처리**, **전자 메일 문서도 취급**, 또는 **가족 파일을 포함 하도록 확장**하도록 선택할 수 있습니다. 검토를 위해 플래그가 지정 되는 각 파일에 대 한 **가족 파일을 포함 하도록 확장**선택 하는 경우에 동일한 제품군의 모든 파일 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="61136-p119">Under**Micellaneous**, you can choose to **Treat attachments as documents**, **Treat emails as documents**, or **Expand to include family files**. When you choose **Expand to include family files**, for each file that is flagged for review, all files of the same family will also be flagged.</span></span>
    
7. <span data-ttu-id="61136-196">설정을 저장 하려면 **저장** 을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="61136-196">Choose **Save** to save the settings.</span></span> 
    
8. <span data-ttu-id="61136-197">내보내기 매개 변수를 지정한 후 내보내기 일괄 처리를 시작 하려면 **Create 세션 내보내기**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="61136-197">After you specify export parameters, to start export batch, click **Create export session**.</span></span>
    
    <span data-ttu-id="61136-p120">내보내기 작업 중 상태 **작업 상태**에 표시 됩니다. 결과는 **내보내기 요약**에 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="61136-p120">During export, the status is displayed in **Task status**. The results are displayed in **Export summary**.</span></span>
    
9. <span data-ttu-id="61136-200">**파일 다운로드** 창에서 내보내기 키에 복사를 **클립보드에 복사** 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="61136-200">In the **Download files** window, click **Copy to clipboard** to copy the Export key.</span></span> 
    
    ![파일 다운로드](media/99cf2c13-4954-479f-9741-80d7458c1a15.png)
  
10. <span data-ttu-id="61136-202">**닫기**를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="61136-202">Click **Close**.</span></span> 
    
    <span data-ttu-id="61136-203">EDiscovery 내보내기 도구 시작 됩니다.</span><span class="sxs-lookup"><span data-stu-id="61136-203">The eDiscovery Export Tool is started.</span></span>
    
    ![eDiscovery 내보내기](media/705756ca-ee97-4d24-b70f-8b23513f6d11.gif)
  
11. <span data-ttu-id="61136-205">**EDiscovery 내보내기 도구**:</span><span class="sxs-lookup"><span data-stu-id="61136-205">In the **eDiscovery Export Tool**:</span></span>
    
    -  <span data-ttu-id="61136-206">**원본에 연결 하는데 사용할 공유 액세스 서명 붙여**에서 내보내기 키를 7 단계에서 해당 youcopied를 클립보드에 붙여넣습니다.</span><span class="sxs-lookup"><span data-stu-id="61136-206">In **Paste the Shared Access Signature that will be used to connect to the source**, paste the Export key that youcopied to the clipboard in step 7.</span></span>
    
    - <span data-ttu-id="61136-207">로컬 컴퓨터에 다운로드 한 내보내기 파일을 저장 하기 위해 대상 위치를 선택 하려면 **찾아보기** 를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="61136-207">Click **Browse** to select the target location for storing the downloaded export files on the local machine.</span></span> 
    
    - <span data-ttu-id="61136-p121">**시작**을 클릭 합니다. 내보내기 파일은 로컬 컴퓨터에 다운로드 됩니다. 4 단계에서 **사용자 정의 Azure blob로 내보내기** 를 선택한 경우에 적절 Blob 저장소 URL 대상에 게 세션이 내보내집니다.</span><span class="sxs-lookup"><span data-stu-id="61136-p121">Click **Start**.The export files are downloaded to the local machine. If you chose **Export to user-defined Azure blob** in step 4, the session is exported to a Blob storage URL destination of your choosing.</span></span>
    
<span data-ttu-id="61136-210">내보내기 보고서의 필드에 대 한 전체 설명을, [내보내기 보고서 필드를](export-report-fields-in-advanced-ediscovery.md)참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="61136-210">For a full description of the fields in the export report, see [Export report fields](export-report-fields-in-advanced-ediscovery.md).</span></span>
  
## <a name="export-report-output-files"></a><span data-ttu-id="61136-211">보고서 출력 파일 내보내기</span><span class="sxs-lookup"><span data-stu-id="61136-211">Export report output files</span></span>
<span data-ttu-id="61136-212"><a name="BK_ExportOutputFIles"> </a></span><span class="sxs-lookup"><span data-stu-id="61136-212"></span></span>

<span data-ttu-id="61136-213">다음 표에서 내보내기 일괄 처리를 실행할 때 생성 되는 출력 파일을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="61136-213">The following table lists the output files that are generated when you run an Export batch.</span></span>
  
|<span data-ttu-id="61136-214">**파일 이름**</span><span class="sxs-lookup"><span data-stu-id="61136-214">**File name**</span></span>|<span data-ttu-id="61136-215">**파일 형식**</span><span class="sxs-lookup"><span data-stu-id="61136-215">**File type**</span></span>|<span data-ttu-id="61136-216">**설명**</span><span class="sxs-lookup"><span data-stu-id="61136-216">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="61136-217">내보내기 요약</span><span class="sxs-lookup"><span data-stu-id="61136-217">Export summary</span></span>  <br/> |<span data-ttu-id="61136-218">csv</span><span class="sxs-lookup"><span data-stu-id="61136-218">csv</span></span>  <br/> |<span data-ttu-id="61136-219">EDiscovery 내보내기 도구에서 생성 된 로그 파일입니다.</span><span class="sxs-lookup"><span data-stu-id="61136-219">A log file generated by the eDiscovery Export Tool.</span></span>  <br/> |
|<span data-ttu-id="61136-220">추적</span><span class="sxs-lookup"><span data-stu-id="61136-220">Trace</span></span>  <br/> |<span data-ttu-id="61136-221">txt</span><span class="sxs-lookup"><span data-stu-id="61136-221">txt</span></span>  <br/> |<span data-ttu-id="61136-222">EDiscovery 내보내기 도구에서 생성 된 로그 파일입니다.</span><span class="sxs-lookup"><span data-stu-id="61136-222">A log file generated by the eDiscovery Export Tool.</span></span>  <br/> |
|<span data-ttu-id="61136-223">추출 된 텍스트 파일</span><span class="sxs-lookup"><span data-stu-id="61136-223">Extracted text files</span></span>  <br/> |<span data-ttu-id="61136-224">파일 폴더</span><span class="sxs-lookup"><span data-stu-id="61136-224">File folder</span></span>  <br/> |<span data-ttu-id="61136-225">내보낸된 파일의 압축 푼된 텍스트 파일이 있는 폴더입니다.</span><span class="sxs-lookup"><span data-stu-id="61136-225">Folder that contains the extracted text files of the exported files.</span></span>  <br/> |
|<span data-ttu-id="61136-226">입력 또는 네이티브 파일</span><span class="sxs-lookup"><span data-stu-id="61136-226">Input or native files</span></span>  <br/> |<span data-ttu-id="61136-227">파일 폴더</span><span class="sxs-lookup"><span data-stu-id="61136-227">File folder</span></span>  <br/> |<span data-ttu-id="61136-228">내보낸된 파일의 기본 및 입력 파일이 있는 폴더입니다.</span><span class="sxs-lookup"><span data-stu-id="61136-228">Folder that contains the native and input files of the exported files.</span></span>  <br/> |
|<span data-ttu-id="61136-229">목록 내보내기</span><span class="sxs-lookup"><span data-stu-id="61136-229">Export list</span></span>  <br/> |<span data-ttu-id="61136-230">xlsx</span><span class="sxs-lookup"><span data-stu-id="61136-230">xlsx</span></span>  <br/> |<span data-ttu-id="61136-p122">Xlsx 형식에서 메타 데이터를 내보낸된 파일입니다. 파일의 필드를 내보내려면 서식 파일 사용자 선택에 따라 다릅니다. 필요한 경우 여러 파일을 만들, 각 100-150 K 행을 포함 합니다. 특정 값을 Excel 셀 포함 될 수 있는 것 보다 더 많은 문자를 포함 하는 경우 (현재 제한 길이 32, 767 자)를 다음 값을 허용 하는 최대 길이를 잘립니다. 값은 조정이 적용 하는 경우 셀의 배경색은 사용자에 게이 나타내기 위해 빨간색입니다. " 대규모 배포에는 전자 메일 전송 된 경우 전자 메일 참가자 "은 길이 제한을 초과 하는 필드의 예입니다. 출력 필드에 대 한 자세한 내용은 [보고서 필드 내보내기](export-report-fields-in-advanced-ediscovery.md) 를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="61136-p122">Exported files metadata in xlsx format. Fields in files are according to template user selects to export. If needed, several files are created, each contains 100-150K rows. If a certain value contains more characters than an Excel cell can contain (currently the limit is 32,767 characters), then the value will be trimmed to the maximum length allowed. If a value is trimmed, the cell's background color is red to indicate this to the user."Email participants" is an example of a field that can exceed the length limit, if the email was sent to a large distribution. See [Export report fields](export-report-fields-in-advanced-ediscovery.md) for details about the output fields.  </span></span><br/> |
|<span data-ttu-id="61136-237">파일 로드</span><span class="sxs-lookup"><span data-stu-id="61136-237">Load file</span></span>  <br/> |<span data-ttu-id="61136-238">csv</span><span class="sxs-lookup"><span data-stu-id="61136-238">csv</span></span>  <br/> |<span data-ttu-id="61136-p123">다른 응용 프로그램으로 로드에 대 한 csv 형식에서 메타 데이터를 내보낸된 파일입니다. 파일의 필드를 내보내려면 서식 파일 사용자 선택에 따라 다릅니다.</span><span class="sxs-lookup"><span data-stu-id="61136-p123">Exported files metadata in csv format for loading into a different application. Fields in files are according to template user selects to export.</span></span>  <br/> |
|<span data-ttu-id="61136-241">성공 표시기</span><span class="sxs-lookup"><span data-stu-id="61136-241">Success indicator</span></span>  <br/> |<span data-ttu-id="61136-242">txt</span><span class="sxs-lookup"><span data-stu-id="61136-242">txt</span></span>  <br/> |<span data-ttu-id="61136-p124">타사의 Azure blob로 내보낼 때에 만들어집니다. 내보내기 성공 완전히, 파일이 만들어집니다. 오류를 발생 하는 경우 또는 부분 성공 파일이 만들어지지 않습니다. 파일에서 서로 다른 내보내기 일괄 처리/세션 상태를 확인 하는 자동화 된 추적 허용의 루트 폴더에 만들어집니다. 이 빈 파일입니다. 해당 이름은: TenantId_CaseId_ExternalCaseId_CaseName_ExportBatchId_SessionId_DateTime.txt 합니다.</span><span class="sxs-lookup"><span data-stu-id="61136-p124">Only created when exporting to a 3rd party Azure blob. If export succeed completely, the file will be created. In case of failure, or partial success the file will not be created. File will be created in the root folder, allowing automated tracking on different Export batches/sessions statuses. This is an empty file. Its name is: TenantId_CaseId_ExternalCaseId_CaseName_ExportBatchId_SessionId_DateTime.txt.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="61136-249">참고 항목</span><span class="sxs-lookup"><span data-stu-id="61136-249">See also</span></span>

[<span data-ttu-id="61136-250">Office 365 Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="61136-250">Office 365 Advanced eDiscovery</span></span>](office-365-advanced-ediscovery.md)
  
[<span data-ttu-id="61136-251">일괄 처리 기록 보기 및 이전 결과 내보내기</span><span class="sxs-lookup"><span data-stu-id="61136-251">Viewing batch history and exporting past results</span></span>](view-batch-history-and-export-past-results.md)
  
[<span data-ttu-id="61136-252">Office 365 Advanced eDiscovery에 대한 빠른 설정</span><span class="sxs-lookup"><span data-stu-id="61136-252">Quick setup for Office 365 Advanced eDiscovery</span></span>](quick-setup-for-advanced-ediscovery.md)

[<span data-ttu-id="61136-253">보고서 필드 내보내기</span><span class="sxs-lookup"><span data-stu-id="61136-253">Export report fields</span></span>](export-report-fields-in-advanced-ediscovery.md)
  
[<span data-ttu-id="61136-254">Office 365에서 eDiscovery 검색 결과 내보낼 때 다운로드 속도를 높입니다 합니다.</span><span class="sxs-lookup"><span data-stu-id="61136-254">Increase the download speed when exporting eDiscovery search results from Office 365</span></span>](increase-download-speeds-when-exporting-ediscovery-results.md)

