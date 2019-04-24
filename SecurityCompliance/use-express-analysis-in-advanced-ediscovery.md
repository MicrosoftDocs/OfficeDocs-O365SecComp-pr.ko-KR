---
title: Office 365 Advanced eDiscovery에서 빠른 분석 사용
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
ms.assetid: 50580099-3dc0-44a1-a9b6-5ca6d396316b
description: Office 365 Advanced eDiscovery의 빠른 분석 모드를 실행 하는 방법에 대해 알아봅니다.
ms.openlocfilehash: d8457587c9c1a1237ddc076ce803a46382a04ed8
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32264496"
---
# <a name="use-express-analysis-in-office-365-advanced-ediscovery"></a><span data-ttu-id="788cf-103">Office 365 Advanced eDiscovery에서 빠른 분석 사용</span><span class="sxs-lookup"><span data-stu-id="788cf-103">Use Express Analysis in Office 365 Advanced eDiscovery</span></span>

> [!NOTE]
> <span data-ttu-id="788cf-p101">Advanced eDiscovery를 사용하려면 Office 365 E3의 고급 준수 추가 기능이나 조직을 위한 E5 구독이 필요합니다. 이 요금제가 없는 상태에서 Advanced eDiscovery를 사용하려는 경우에는 [Office 365 Enterprise E5 평가판을 등록](https://go.microsoft.com/fwlink/p/?LinkID=698279)할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="788cf-p101">Advanced eDiscovery requires an Office 365 E3 with the Advanced Compliance add-on or an E5 subscription for your organization. If you don't have that plan and want to try Advanced eDiscovery, you can [sign up for a trial of Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span></span> 
  
<span data-ttu-id="788cf-106">**빠른 분석** 을 사용 하 여 사례를 빠르게 분석 하 고 결과를 내보낼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="788cf-106">You can use **Express analysis** to quickly analyze a case and export the results.</span></span> 
  
<span data-ttu-id="788cf-107">빠른 분석을 사용 하 여 거의 중복 항목 및 전자 메일 스레드를 계산 하 고 테마를 계산할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="788cf-107">You can use express analysis to calculate near-duplicates and email threads and calculate themes.</span></span> <span data-ttu-id="788cf-108">또한 [빠른 분석을 위해 고급 설정](use-express-analysis-in-advanced-ediscovery.md#BK_AdvancedSettings)에서 테마, 문서 유사성 및 내보내기 파일에 대 한 특정 매개 변수를 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="788cf-108">You can also set certain parameters for themes, document similarity and the export files in the [Advanced settings for Express analysis](use-express-analysis-in-advanced-ediscovery.md#BK_AdvancedSettings).</span></span>
  
## <a name="run-express-analysis"></a><span data-ttu-id="788cf-109">빠른 분석 실행</span><span class="sxs-lookup"><span data-stu-id="788cf-109">Run Express analysis</span></span>

1. <span data-ttu-id="788cf-110">**빠른 분석** (1) 탭에서 컨테이너를 선택 하 여 \* \* Express 분석 \* \* (2) 및 **고급 설정** 단추를 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="788cf-110">In the **Express analysis** (1) tab, select a container to enable the \*\* Express analysis \*\* (2), and **Advanced settings** buttons.</span></span> 
    
    ![빠른 분석 페이지 스크린샷](media/60009974-5d1f-4971-8ebe-e5ec74e7fd2a.jpg)
  
2. <span data-ttu-id="788cf-112">다음 **매개 변수 분석**:</span><span class="sxs-lookup"><span data-stu-id="788cf-112">Under **Analyze parameters**:</span></span>
    
  - <span data-ttu-id="788cf-113">분석을 실행 하려면 **거의 중복 되지 않은 항목 및 전자 메일 스레드를 계산** 합니다.</span><span class="sxs-lookup"><span data-stu-id="788cf-113">Check **Calculate near-duplicates and email threads** if you want to run the analysis.</span></span> <span data-ttu-id="788cf-114">이 옵션은 기본적으로 선택되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="788cf-114">It is selected by default.</span></span> 
    
  - <span data-ttu-id="788cf-115">**테마 계산** 을 선택 하 여 모든 파일을 처리 하 고 테마를 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="788cf-115">Check **Calculate Themes** to process all files and assign themes to them.</span></span> <span data-ttu-id="788cf-116">이 옵션은 기본적으로 선택되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="788cf-116">It is selected by default.</span></span> 
    
3. <span data-ttu-id="788cf-117">**내보내기 대상**:</span><span class="sxs-lookup"><span data-stu-id="788cf-117">Under **Export destination**:</span></span>
    
  - <span data-ttu-id="788cf-118">로컬 컴퓨터에 **다운로드** 를 확인 하 여 로컬 컴퓨터로 다운로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="788cf-118">Check **Download to local machine** to download to your local computer.</span></span> 
    
  - <span data-ttu-id="788cf-119">**사용자 정의 Azure blob로 내보내기를** 선택 하는 경우 컨테이너 URL 및 SAS 토큰도 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="788cf-119">If you check **Export to user-defined Azure blob** then you can also specify a container URL and SAS token.</span></span> 
    
    > [!NOTE]
    > <span data-ttu-id="788cf-120">내보내기 패키지가 사용자 정의 Azure blob에 저장 되 면 더 이상 고급 eDiscovery를 통해 데이터가 관리 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="788cf-120">Once an export package is stored to the user defined Azure blob, the data is no longer managed by Advanced eDiscovery.</span></span> <span data-ttu-id="788cf-121">Azure blob에서 관리 됩니다.</span><span class="sxs-lookup"><span data-stu-id="788cf-121">it is managed by the Azure blob.</span></span> <span data-ttu-id="788cf-122">즉, 사례를 삭제 하는 경우 내보낸 파일은 여전히 Azure blob에 남아 있게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="788cf-122">This means if you delete the case, the exported files will still remain on the Azure blob.</span></span> 
  
  - <span data-ttu-id="788cf-123">**향후 내보내기 세션을 위해 sas 토큰 저장**:이 옵션을 선택 하면 나중에 사용할 수 있도록 sas 토큰이 고급 eDiscovery의 내부 데이터베이스에 암호화 됩니다.</span><span class="sxs-lookup"><span data-stu-id="788cf-123">**Save SAS token for future export session**: If checked, the SAS token will be encrypted in the Advanced eDiscovery's internal database for future use.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="788cf-124">현재 SAS 토큰은 매달 만료 됩니다.</span><span class="sxs-lookup"><span data-stu-id="788cf-124">Currently the SAS token expires after a month.</span></span> <span data-ttu-id="788cf-125">1 개월 이상 후에 다운로드 하려고 하면 마지막 세션을 실행 취소 한 다음 다시 내보내십시오.</span><span class="sxs-lookup"><span data-stu-id="788cf-125">If you try to download after more than a month you have to undo last session, then export again.</span></span> 
  
4. <span data-ttu-id="788cf-126">기본 설정으로 빠른 분석을 시작 하려면 **빠른 분석**을 선택 하 고 **작업 상태** 페이지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="788cf-126">To start the express analysis with default settings, choose **Express analysis**, and the **Task status** page will display</span></span> 
    
    <span data-ttu-id="788cf-127">**작업 상태** 페이지에서 **프로세스**, **분석** 및 **내보내기** 탭을 확장 하 여 빠른 실행에 대 한 세부 정보를 표시할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="788cf-127">On the **Task status** page you can expand the **Process**, **Analyze** and **Export** tabs to display details about the express run.</span></span> 
    
    ![Advanced eDiscovery Express analysis 작업 상태 페이지의 스크린샷](media/bf30ab02-9828-4a6d-a485-0babc2c49ae5.jpg)
  
5. <span data-ttu-id="788cf-129">실행에 대 한 자세한 정보를 나열 하려면 **빠른 분석 요약** 페이지를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="788cf-129">Choose the **Express analysis summary** page to list detailed information about the run.</span></span> 
    
    <span data-ttu-id="788cf-130">**빠른 분석 요약** 페이지 아래쪽에서 **마지막 세션 다운로드** 를 선택 하 여 로컬 컴퓨터에 분석 파일 tp를 다운로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="788cf-130">On the bottom of the **Express analysis summary** page, choose **Download last session** to download the analysis files tp your local computer.</span></span> <span data-ttu-id="788cf-131">먼저 ediscovery 내보내기 도구를 다운로드 하 고 내보내기 키를 ediscovery 내보내기 도구에 붙여 넣어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="788cf-131">You will first have to download eDiscovery Export tool and paste the Export key to the eDiscovery Export tool.</span></span> 
    
## <a name="advanced-settings-for-express-analysis"></a><span data-ttu-id="788cf-132">빠른 분석에 대 한 고급 설정</span><span class="sxs-lookup"><span data-stu-id="788cf-132">Advanced settings for Express analysis</span></span>
<span data-ttu-id="788cf-133"><a name="BK_AdvancedSettings"> </a></span><span class="sxs-lookup"><span data-stu-id="788cf-133"></span></span>

<span data-ttu-id="788cf-134">선택적으로 **고급 설정을** 설정 하 여 기본 Express analysis 매개 변수를 변경할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="788cf-134">You can optionally set **Advanced settings** to change the default Express analysis parameters.</span></span> 
  
1. <span data-ttu-id="788cf-135">**분석** 섹션에서 다음을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="788cf-135">In the **Analyze** section:</span></span> 
    
  - <span data-ttu-id="788cf-136">**근접 복제 및 전자 메일 스레드에서** **문서 유사성** 값을 입력 하거나 기본값인 65%를 그대로 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="788cf-136">In the **Near duplicates and email threads**, enter the **Document similarity** value, or accept the default of 65%.</span></span> 
    
  - <span data-ttu-id="788cf-137">**테마의 최대 수** 에서 만들 테마 수를 입력 하거나 값을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="788cf-137">In the **Max number of themes** enter or select a value for the number of themes to create.</span></span> <span data-ttu-id="788cf-138">기본값은 200입니다.</span><span class="sxs-lookup"><span data-stu-id="788cf-138">The default is 200.</span></span> 
    
    > [!NOTE]
    > <span data-ttu-id="788cf-139">테마 수를 늘리면 성능에 영향을 미치며 테마를 일반화할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="788cf-139">Increasing the number of themes affects performance, as well as the ability of a theme to generalize.</span></span> <span data-ttu-id="788cf-140">테마 수가 높을수록 더 세밀 하 게 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="788cf-140">The higher the number of themes, the more granular they are.</span></span> <span data-ttu-id="788cf-141">예를 들어 50 테마 집합에 "농구, Spurs, Clippers, Lakers"와 같은 테마가 포함 된 경우 300 테마에는 별도의 테마 ("Spurs", "Clippers", "Lakers")가 포함 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="788cf-141">For example, if a set of 50 themes include a theme such as "Basketball, Spurs, Clippers, Lakers"; 300 themes may include separate themes: "Spurs", "Clippers", "Lakers".</span></span> <span data-ttu-id="788cf-142">"농구" 테마에 대 한 인식이 없고 ECA에 대해이 기능을 사용 하는 경우 "농구" 라는 테마를 표시 하는 것이 유용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="788cf-142">If you had no awareness of the theme "Basketball" and use this feature for ECA, seeing the theme "Basketball" could be useful.</span></span> <span data-ttu-id="788cf-143">그러나 처리에 너무 많은 테마가 포함 되어 있는 경우에는 "농구" 라는 단어가 표시 되지 않으며 Spurs 및 Clippers는 시작 하는 데 사용 되는 항목을 나타내는 것이 아니라 더 나은 농구 테마 인지 알 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="788cf-143">But, if the processing had too many themes, you may never see the word "Basketball" and may not know that Spurs and Clippers are good Basketball themes to review, rather than items that go on boots and used for hair.</span></span> 
  
  - <span data-ttu-id="788cf-144">**추천** 테마에서 테마 처리를 제어 하기 위해 **수정** 을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="788cf-144">In the **Suggested themes** choose **Modify** to suggest theme words to control Themes processing.</span></span> <span data-ttu-id="788cf-145">고급 eDiscovery는 이러한 추천 단어에 집중 하 고 "최대 테마 수" 설정에 따라 하나 이상의 관련 테마를 만들려고 시도 합니다.</span><span class="sxs-lookup"><span data-stu-id="788cf-145">Advanced eDiscovery will focus on these suggested words and try to create one or more relevant themes, based on the "Max number of themes" settings.</span></span> 
    
    <span data-ttu-id="788cf-146">예를 들어 추천 단어가 "computer"이 고 "2"를 "최대 테마 수"로 지정한 경우 Advanced eDiscovery에서는 "computer" 라는 단어와 관련 된 두 테마를 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="788cf-146">For example, if the suggested word is "computer", and you specified "2" as the "Max number of Themes", Advanced eDiscovery will try to generate two themes that relate to the word "computer".</span></span> <span data-ttu-id="788cf-147">"컴퓨터 소프트웨어" 및 "컴퓨터 하드웨어"와 같은 두 가지 테마를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="788cf-147">The two themes might be "computer software" and "computer hardware", for example.</span></span>
    
    ![추천된 테마 추가](media/06e9ffd3-a76c-423b-b450-9e465eb9a02f.png)
  
  - <span data-ttu-id="788cf-149">**모드** 드롭다운 목록에서 **테마** 옵션을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="788cf-149">**Mode** From the drop-down list, select a **Themes** option:</span></span> 
    
  - <span data-ttu-id="788cf-150">**모델 만들기 및 적용**: 파일 세그먼트에서 모델 별로 테마를 계산 하 여 파일 간에 배포 합니다.</span><span class="sxs-lookup"><span data-stu-id="788cf-150">**Create and apply model**: Calculates themes by models from a segment of the files and then distributes files among them.</span></span>
    
  - <span data-ttu-id="788cf-151">**모델 만들기**: 파일의 세그먼트에서 테마 모델을 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="788cf-151">**Create model**: Calculates a themes model from a segment of the files.</span></span> <span data-ttu-id="788cf-152">파일을 나눌 때의 적용 프로세스는 별도로 수행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="788cf-152">The Apply process of dividing files is done separately at another time.</span></span>
    
  - <span data-ttu-id="788cf-153">**모델 적용**:이 옵션은 모델을 이전에 만들었지만 아직 적용 하지 않은 경우에만 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="788cf-153">**Apply model**: This option is only shown if a model was created previously and not yet applied.</span></span> <span data-ttu-id="788cf-154">이렇게 하면 테마에 따라 파일이 구분 됩니다.</span><span class="sxs-lookup"><span data-stu-id="788cf-154">This will divide the files based on the themes.</span></span>
    
2. <span data-ttu-id="788cf-155">**내보내기** 섹션에서 다음을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="788cf-155">In the **Export** section:</span></span> 
    
1. <span data-ttu-id="788cf-156">**내보내기 일괄 처리 선택**:</span><span class="sxs-lookup"><span data-stu-id="788cf-156">In the **Select export batch**:</span></span>
    
  - <span data-ttu-id="788cf-157">일괄 **처리 내보내기** 목록에서 일괄 처리 이름 (기본 일괄 처리)을 내보내려면 배치 이름이 나 내보내기 결과를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="788cf-157">From the **Export batch** list, select the batch name or export results to Export batch 01, (the default batch).</span></span> 
    
  - <span data-ttu-id="788cf-158">기존 사례에 추가한 새 파일에 대 한 결과를 내보내려면 현재 일괄 처리를 계속 합니다.</span><span class="sxs-lookup"><span data-stu-id="788cf-158">To export results for new files that you added to an existing case, continue with your current batch.</span></span> <span data-ttu-id="788cf-159">일괄 처리에서 세션을 만들려면 동일한 일괄 처리 번호를 선택 하 고 **내보내기 세션 만들기** 를 클릭 합니다 .이 옵션을 사용 하면 이전 일괄 처리와 같은 매개 변수를 증분 방식으로 내보낼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="788cf-159">To create a session in the batch, select the same batch number and click **Create export session** You can use this option to export the same parameters as the previous batch, in an incremental manner.</span></span> 
    
  - <span data-ttu-id="788cf-160">새 \*\*\*\* ![일괄 처리로 내보내려면 추가 아이콘](media/c2dd8b3a-5a22-412c-a7fa-143f5b2b5612.png) 추가를 클릭 하 고 **일괄 이름** 에 새 이름 (또는 기본값 적용)과 설명을 **일괄 처리 설명**에 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="788cf-160">To export to a new batch, click **Add** ![add icon](media/c2dd8b3a-5a22-412c-a7fa-143f5b2b5612.png) and enter a new name in **Batch name** (or accept the default) and a description in **Batch description**.</span></span> <span data-ttu-id="788cf-161">**확인**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="788cf-161">Click **OK**.</span></span>
    
  - <span data-ttu-id="788cf-162">일괄 처리 이름 또는 설명을 편집 하려면 **내보내기 일괄 처리**에서 이름을 선택 하 고 편집 \*\*\*\* ![아이콘](media/3d613660-7602-4df2-bdb9-14e9ca2f9cf2.png)편집을 클릭 한 다음 필드를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="788cf-162">To edit a batch name or description, select the name in **Export batch**, click **Edit** ![Edit icon](media/3d613660-7602-4df2-bdb9-14e9ca2f9cf2.png), and then modify the fields.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="788cf-163">내보내기 일괄 처리에 대 한 세션을 실행 한 후에는 삭제할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="788cf-163">After you've run sessions for an export batch, they cannot be deleted.</span></span> <span data-ttu-id="788cf-164">또한 첫 번째 세션을 실행 한 후에는 일부 매개 변수만 편집할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="788cf-164">In addition, only some parameters can be edited once the first session is run.</span></span> 
  
  - <span data-ttu-id="788cf-165">중복 된 내보내기 일괄 처리를 만들려면 복제 \*\*\*\* ![된 내보내기 일괄 처리 만들기를 선택 하](media/3f6d5f59-e842-4946-a493-473528af0119.jpg) 고 패널에 중복 일괄 처리에 대 한 이름 및 설명을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="788cf-165">To create a duplicate export batch, choose **Duplicate export batch** ![Create a duplicate export batch icon](media/3f6d5f59-e842-4946-a493-473528af0119.jpg) and enter a name and a description for the duplicate batch in the panel.</span></span> 
    
  - <span data-ttu-id="788cf-166">내보내기 일괄 처리를 삭제 하려면 **삭제** ![를 선택 하 여 일괄 처리](media/92a9f8e0-d469-48da-addb-69365e7ffb6f.jpg)내보내기 아이콘을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="788cf-166">To delete an export batch, choose **Delete** ![Delete an export batch icon](media/92a9f8e0-d469-48da-addb-69365e7ffb6f.jpg).</span></span>
    
  - <span data-ttu-id="788cf-167">일괄 처리 기록을 보려면 **일괄 처리 기록** ![보기 히스토리 아이콘](media/a80cc320-d96c-4d91-8884-75fe2cb147e2.jpg)을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="788cf-167">To view the history of a batch, choose **Batch history** ![View history icon](media/a80cc320-d96c-4d91-8884-75fe2cb147e2.jpg).</span></span>
    
2. <span data-ttu-id="788cf-168">정의 p **opulation:** 내보내기 일괄 처리에 대 한 설정을 세부적으로 조정 하려는 경우에 **는 위의 파일을 포함** 합니다. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="788cf-168">Under Define p **opulation:** Select **Include only files above Relevance cut-off score** and/or **Refine export batch** if you want to fine-tune the settings for your export batch.</span></span> <span data-ttu-id="788cf-169">**관련성이 높은 별 파일을 포함**하는 경우에는 **문제가** 사용 하도록 설정 되며, 파일의 관련성 점수가 선택한 문제에 대 한 컷오프 점수 보다 높으면 파일을 내보냅니다.</span><span class="sxs-lookup"><span data-stu-id="788cf-169">If you select **Include only files above Relevance cut-off score**, then the **Issue** is enabled, and if the file's relevance score is higher than the cut-off score for the selected issue, then the file is exported.</span></span> <span data-ttu-id="788cf-170">' **검토 필터 For** '에 의해 제외 되지 않으면 파일을 내보냅니다.</span><span class="sxs-lookup"><span data-stu-id="788cf-170">The file will be exported unless it's excluded by the ' **For review** filter.</span></span> <span data-ttu-id="788cf-171">**일괄 처리**해제를 선택 하면 \*\*\*\* **' 검토용으로 ' 및 필터 사용 ' 필드** 라디오 단추를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="788cf-171">If you select **Refine export batch**, then the **De-dupe** and **Filter by 'For review' field** radio buttons are enabled.</span></span> <span data-ttu-id="788cf-172">**비-dupe**를 선택한 경우 정의 된 정책에 따라 파일을 필터링 합니다. [대/소문자 수준 (기본값): 전체 경우에 해당 하는 모든 중복 파일 집합에서 파일 하나를 제외 하 고 duped 합니다.</span><span class="sxs-lookup"><span data-stu-id="788cf-172">If you choose **De-dupe**, then duplicates files will be filtered-out according to the policy defined: [Case level (default): from every set of duplicate files in the entire case, all but one file will be de-duped.</span></span> <span data-ttu-id="788cf-173">Custodian level: 동일한 Custodian의 모든 중복 파일 집합에서 하나의 파일을 제외 하 고 모두 duped 합니다.</span><span class="sxs-lookup"><span data-stu-id="788cf-173">Custodian level: from every set of duplicate files of the same custodian, all but one file will be de-duped.</span></span> <span data-ttu-id="788cf-174">내보내기 출력에서는 모든 중복 파일의 레코드를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="788cf-174">A record of all duplicate files is available in export output.</span></span> <span data-ttu-id="788cf-175">**' 검토용으로 필터링 '** 필드를 선택 하는 경우 **메타 데이터 아래 수정을** 선택 하 여 **' 검토용 '** 필드 설정을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="788cf-175">If you choose **Filter by 'For review'** field, select **Modify under Metadata** to enter your **'For review'** field settings.</span></span> <span data-ttu-id="788cf-176">패키지 콘텐츠에 원본 파일을 포함할 **입력 파일 포함**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="788cf-176">Select **Include input files**to include source files in the package content.</span></span> <span data-ttu-id="788cf-177">이 옵션의 선택을 취소 하 여 내보내기 프로세스의 속도를 높일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="788cf-177">You can clear this option to speed up the export process.</span></span> <span data-ttu-id="788cf-178">네이티브 파일은 모든 경우에 내보내집니다.</span><span class="sxs-lookup"><span data-stu-id="788cf-178">Note that the Native files will be exported in any case.</span></span>
    
3. <span data-ttu-id="788cf-179">**메타 데이터 정의**에서 **템플릿 내보내기** 목록 (세션당 한 번)의 다음 옵션 중에서 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="788cf-179">Under **Define metadata**, select from the following options in the **Export template** list (once per session).</span></span> 
    
  - <span data-ttu-id="788cf-180">**표준**: 데이터 항목, 메타 데이터 및 속성의 기본 집합입니다.</span><span class="sxs-lookup"><span data-stu-id="788cf-180">**Standard**: Basic set of data items, metadata, and properties.</span></span> <span data-ttu-id="788cf-181">고급 eDiscovery에서 데이터 가져오기가 이미 처리 된 경우이 옵션을 사용 하면 파일이 이미 들어 있는 시스템에 내보내기 데이터를 업로드할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="788cf-181">Use this option when import data was already processed in Advanced eDiscovery and export data is uploaded to a system that already contains the files.</span></span> <span data-ttu-id="788cf-182">기본적으로 내보내기 템플릿 열은 만들어지고 채워집니다.</span><span class="sxs-lookup"><span data-stu-id="788cf-182">By default, export template columns are created and filled.</span></span>
    
  - <span data-ttu-id="788cf-183">**all**: 모든 처리 데이터를 포함 하는 표준 메타 데이터의 전체 집합 및 분석 및 관련성 점수</span><span class="sxs-lookup"><span data-stu-id="788cf-183">**All**: Full set of standard metadata including all processing data, as well as Analyze and Relevance scores.</span></span> <span data-ttu-id="788cf-184">이 서식 파일은 고급 eDiscovery에서 처리를 수행 하 고 파일 데이터를 처음으로 외부 시스템에 업로드 하는 경우에 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="788cf-184">This template is required when Advanced eDiscovery performs the processing and file data is uploaded to an external system for the first time.</span></span>
    
  - <span data-ttu-id="788cf-185">**문제**: **모든 문제** 를 선택 하거나 만든 특정 문제를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="788cf-185">**Issues**: Select **All Issues** or select a particular issue you have created.</span></span> 
    
<span data-ttu-id="788cf-186">**확인**을 클릭 하 여 고급 설정을 저장 하 고 기본값을 사용 하 여 기본값을 **복원** 하거나, **취소** 를 선택 하 여 고급 설정 설정을 취소 합니다.</span><span class="sxs-lookup"><span data-stu-id="788cf-186">Choose **OK**to save the advanced settings, **Restore defaults** to use default values, or **Cancel** to cancel setting the advanced settings.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="788cf-187">참고 항목</span><span class="sxs-lookup"><span data-stu-id="788cf-187">See also</span></span>
<span data-ttu-id="788cf-188"><a name="BK_AdvancedSettings"> </a></span><span class="sxs-lookup"><span data-stu-id="788cf-188"></span></span>

[<span data-ttu-id="788cf-189">Office 365 Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="788cf-189">Office 365 Advanced eDiscovery</span></span>](office-365-advanced-ediscovery.md)

