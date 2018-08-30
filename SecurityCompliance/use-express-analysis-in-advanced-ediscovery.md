---
title: Office 365 Advanced eDiscovery 빠른 분석 사용
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
ms.assetid: 50580099-3dc0-44a1-a9b6-5ca6d396316b
description: Office 365 고급 eDiscovery의 Express 분석 모드를 실행 하는 방법에 알아봅니다.
ms.openlocfilehash: a71e6775b1116e805e455815dca53a727d887809
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22533362"
---
# <a name="use-express-analysis-in-office-365-advanced-ediscovery"></a><span data-ttu-id="aa9e3-103">Office 365 Advanced eDiscovery 빠른 분석 사용</span><span class="sxs-lookup"><span data-stu-id="aa9e3-103">Use Express Analysis in Office 365 Advanced eDiscovery</span></span>

> [!NOTE]
> <span data-ttu-id="aa9e3-p101">고급 eDiscovery 조직에 대 한 고급 준수 추가 기능 또는 e 5 구독은 Office 365 E3 필요합니다. 해당 요금제에 가입한 상태 고급 eDiscovery 시도 하려는 하지 경우에 [Office 365 Enterprise e 5의 평가판 등록](https://go.microsoft.com/fwlink/p/?LinkID=698279)할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="aa9e3-p101">Advanced eDiscovery requires an Office 365 E3 with the Advanced Compliance add-on or an E5 subscription for your organization. If you don't have that plan and want to try Advanced eDiscovery, you can [sign up for a trial of Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span></span> 
  
<span data-ttu-id="aa9e3-106">**분석 Express** 를 신속 하 게 사례를 분석 하 고 결과 내보냅니다를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="aa9e3-106">You can use **Express analysis** to quickly analyze a case and export the results.</span></span> 
  
<span data-ttu-id="aa9e3-p102">거의 중복 항목을 계산 하 고 스레드를 전자 메일 및 테마를 계산 하려면 express 분석을 사용할 수 있습니다. [Express 분석에 대 한 고급 설정](use-express-analysis-in-advanced-ediscovery.md#BK_AdvancedSettings)에서 테마, 문서 다음과 비슷한 및 내보내기 파일에 대 한 특정 매개 변수를 설정할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="aa9e3-p102">You can use express analysis to calculate near-duplicates and email threads and calculate themes. You can also set certain parameters for themes, document similarity and the export files in the [Advanced settings for Express analysis](use-express-analysis-in-advanced-ediscovery.md#BK_AdvancedSettings).</span></span>
  
## <a name="run-express-analysis"></a><span data-ttu-id="aa9e3-109">Express 분석 실행</span><span class="sxs-lookup"><span data-stu-id="aa9e3-109">Run Express analysis</span></span>

1. <span data-ttu-id="aa9e3-110">**Express 분석** (1) 탭에서 사용 하도록 설정 하는 컨테이너를 선택은 * * 분석 Express * * (2) 및 **고급 설정** 단추입니다.</span><span class="sxs-lookup"><span data-stu-id="aa9e3-110">In the **Express analysis** (1) tab, select a container to enable the ** Express analysis ** (2), and **Advanced settings** buttons.</span></span> 
    
    ![Express 분석 페이지의 스크린샷](media/60009974-5d1f-4971-8ebe-e5ec74e7fd2a.jpg)
  
2. <span data-ttu-id="aa9e3-112">**분석 매개 변수**아래에서:</span><span class="sxs-lookup"><span data-stu-id="aa9e3-112">Under **Analyze parameters**:</span></span>
    
  - <span data-ttu-id="aa9e3-p103">분석을 실행 하려는 경우 **거의 중복 항목을 계산 하 고 스레드도 전자 메일을** 확인 합니다. 기본적으로 선택 됩니다.</span><span class="sxs-lookup"><span data-stu-id="aa9e3-p103">Check **Calculate near-duplicates and email threads** if you want to run the analysis. It is selected by default.</span></span> 
    
  - <span data-ttu-id="aa9e3-p104">모든 파일을 처리 하 고 테마 자신에 게 할당 하려면 **계산 테마** 확인 합니다. 기본적으로 선택 됩니다.</span><span class="sxs-lookup"><span data-stu-id="aa9e3-p104">Check **Calculate Themes** to process all files and assign themes to them. It is selected by default.</span></span> 
    
3. <span data-ttu-id="aa9e3-117">**내보낼 대상**아래에서:</span><span class="sxs-lookup"><span data-stu-id="aa9e3-117">Under **Export destination**:</span></span>
    
  - <span data-ttu-id="aa9e3-118">로컬 컴퓨터에 다운로드 하려면 **로컬 컴퓨터에 다운로드** 를 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="aa9e3-118">Check **Download to local machine** to download to your local computer.</span></span> 
    
  - <span data-ttu-id="aa9e3-119">**사용자 정의 Azure blob로 내보내기** 를 확인 하는 경우 컨테이너 URL 및 SAS 토큰을 지정할 수 합니다.</span><span class="sxs-lookup"><span data-stu-id="aa9e3-119">If you check **Export to user-defined Azure blob** then you can also specify a container URL and SAS token.</span></span> 
    
    > [!NOTE]
    > <span data-ttu-id="aa9e3-p105">내보내기 패키지에 저장 된 후에 사용자 정의 Azure blob, 고급 eDiscovery 더이상 데이터를 관리 하는 합니다. Azure blob 하 여이 기능을 관리 합니다. 내보낸된 파일 Azure blob에 그대로 남습니다 대/소문자를 삭제 하면 것을 의미 합니다.</span><span class="sxs-lookup"><span data-stu-id="aa9e3-p105">Once an export package is stored to the user defined Azure blob, the data is no longer managed by Advanced eDiscovery. it is managed by the Azure blob. This means if you delete the case, the exported files will still remain on the Azure blob.</span></span> 
  
  - <span data-ttu-id="aa9e3-123">**향후 내보내기 세션에 대 한 저장 SAS 토큰**: SAS 토큰 선택 하는 경우 나중에 사용할 수에 대 한 고급 eDiscovery의 내부 데이터베이스에서 암호화 됩니다.</span><span class="sxs-lookup"><span data-stu-id="aa9e3-123">**Save SAS token for future export session**: If checked, the SAS token will be encrypted in the Advanced eDiscovery's internal database for future use.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="aa9e3-p106">현재 달 후 SAS 토큰 만료 됩니다. 마지막 세션을 취소 하려면 해야 달 이상 후 다운로드 하려고 하는 경우 다시 내보내기 합니다.</span><span class="sxs-lookup"><span data-stu-id="aa9e3-p106">Currently the SAS token expires after a month. If you try to download after more than a month you have to undo last session, then export again.</span></span> 
  
4. <span data-ttu-id="aa9e3-126">기본 사용 하 여 명시적 분석을 시작 하려면 설정, **분석 Express**를 선택 하 고 **작업 상태** 페이지에 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="aa9e3-126">To start the express analysis with default settings, choose **Express analysis**, and the **Task status** page will display</span></span> 
    
    <span data-ttu-id="aa9e3-127">**작업 상태** 페이지에서 빠른 실행에 대 한 세부 정보를 표시 하는 **프로세스**, **분석** 및 **내보내기** 탭을 확장할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="aa9e3-127">On the **Task status** page you can expand the **Process**, **Analyze** and **Export** tabs to display details about the express run.</span></span> 
    
    ![EDiscovery Express 분석 작업 상태 페이지 고급 스크린샷](media/bf30ab02-9828-4a6d-a485-0babc2c49ae5.jpg)
  
5. <span data-ttu-id="aa9e3-129">실행 하는 방법에 대 한 자세한 정보를 나열 하려면 **Express 분석 요약** 페이지를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="aa9e3-129">Choose the **Express analysis summary** page to list detailed information about the run.</span></span> 
    
    <span data-ttu-id="aa9e3-p107">**분석 요약 Express** 페이지 아래쪽에서 분석 파일 tp 로컬 컴퓨터를 다운로드 하려면 **마지막 세션 다운로드** 를 선택 합니다. 먼저 eDiscovery 내보내기 도구를 다운로드 하 고 eDiscovery 내보내기 도구를 내보내기 키를 붙여넣고 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="aa9e3-p107">On the bottom of the **Express analysis summary** page, choose **Download last session** to download the analysis files tp your local computer. You will first have to download eDiscovery Export tool and paste the Export key to the eDiscovery Export tool.</span></span> 
    
## <a name="advanced-settings-for-express-analysis"></a><span data-ttu-id="aa9e3-132">Express 분석에 대 한 고급 설정</span><span class="sxs-lookup"><span data-stu-id="aa9e3-132">Advanced settings for Express analysis</span></span>
<span data-ttu-id="aa9e3-133"><a name="BK_AdvancedSettings"> </a></span><span class="sxs-lookup"><span data-stu-id="aa9e3-133"></span></span>

<span data-ttu-id="aa9e3-134">필요에 따라 기본 Express 분석 매개 변수를 변경 하려면 **고급 설정을** 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="aa9e3-134">You can optionally set **Advanced settings** to change the default Express analysis parameters.</span></span> 
  
1. <span data-ttu-id="aa9e3-135">**분석** 섹션:</span><span class="sxs-lookup"><span data-stu-id="aa9e3-135">In the **Analyze** section:</span></span> 
    
  - <span data-ttu-id="aa9e3-136">**중복 되는 값 및 전자 메일 스레드 근처**,에서 **문서 다음과 비슷한** 값을 입력 하거나 65%의 기본값을 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="aa9e3-136">In the **Near duplicates and email threads**, enter the **Document similarity** value, or accept the default of 65%.</span></span> 
    
  - <span data-ttu-id="aa9e3-p108">**테마의 최대 수** 를 입력 하거나 만들려는 테마의 수에 대 한 값을 선택 합니다. 기본값은 200입니다.</span><span class="sxs-lookup"><span data-stu-id="aa9e3-p108">In the **Max number of themes** enter or select a value for the number of themes to create. The default is 200.</span></span> 
    
    > [!NOTE]
    > <span data-ttu-id="aa9e3-p109">테마의 수를 늘리면 성능이 될 일반화 하는 테마의 기능에 영향을 줍니다. 테마 수가 많을 수록, 보다 세부적인 됩니다. 예: 50 테마 집합이 "농구, 저비용과, Lakers 전 정가 위"; 테마를 포함 하는 경우 300 테마 별도 테마에 포함 될 수 있습니다. "저비용과", "전 정가 위", "Lakers"입니다. 테마를 인식 하지 "농구" 명의 ECA에 대 한이 기능을 사용 하는 경우 테마 특정인 "농구" 유용할 수 있습니다. 하지만 "농구" 라는 단어를 표시 하지 될 수는 처리 한 너무 많은 테마가 하는 경우 및는 저비용과 및 전 정가 위는 좋은 농구 테마를 검토 하는 대신에 포함할 항목 부팅 되 고 머리에 사용 되는 알 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="aa9e3-p109">Increasing the number of themes affects performance, as well as the ability of a theme to generalize. The higher the number of themes, the more granular they are. For example, if a set of 50 themes include a theme such as "Basketball, Spurs, Clippers, Lakers"; 300 themes may include separate themes: "Spurs", "Clippers", "Lakers". If you had no awareness of the theme "Basketball" and use this feature for ECA, seeing the theme "Basketball" could be useful. But, if the processing had too many themes, you may never see the word "Basketball" and may not know that Spurs and Clippers are good Basketball themes to review, rather than items that go on boots and used for hair.</span></span> 
  
  - <span data-ttu-id="aa9e3-p110">**추천 테마** 에서 테마를 처리 하는 테마를 제어 하는 단어를 추천 하도록 **수정** 선택 합니다. 고급 eDiscovery 중점적으로 이러한 추천된 단어 및 "테마 수가 Max" 설정에 따라 하나 이상의 관련 된 테마를 만들려고 시도 합니다.</span><span class="sxs-lookup"><span data-stu-id="aa9e3-p110">In the **Suggested themes** choose **Modify** to suggest theme words to control Themes processing. Advanced eDiscovery will focus on these suggested words and try to create one or more relevant themes, based on the "Max number of themes" settings.</span></span> 
    
    <span data-ttu-id="aa9e3-p111">예, 추천된 단어를 "computer", "테마의 최대 개수"으로 "2"을 지정 하는 경우 고급 eDiscovery "computer" 라는 단어와 관련 된 두 테마를 생성 하려고 합니다. 예 두 테마: "컴퓨터 소프트웨어" 및 "컴퓨터 하드웨어" 있을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="aa9e3-p111">For example, if the suggested word is "computer", and you specified "2" as the "Max number of Themes", Advanced eDiscovery will try to generate two themes that relate to the word "computer". The two themes might be "computer software" and "computer hardware", for example.</span></span>
    
    ![추천된 테마 추가](media/06e9ffd3-a76c-423b-b450-9e465eb9a02f.png)
  
  - <span data-ttu-id="aa9e3-149">**모드** 드롭다운 목록에서 **테마** 옵션을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="aa9e3-149">**Mode** From the drop-down list, select a **Themes** option:</span></span> 
    
  - <span data-ttu-id="aa9e3-150">**만들기 모델을 적용 하 고**: 파일의 세그먼트에서 모델을 통해 테마를 계산 하 고 다음 사항을 포함 하는 파일을 분산 합니다.</span><span class="sxs-lookup"><span data-stu-id="aa9e3-150">**Create and apply model**: Calculates themes by models from a segment of the files and then distributes files among them.</span></span>
    
  - <span data-ttu-id="aa9e3-p112">**모델 만들기**: 세그먼트의 파일에서 테마 모델을 계산 합니다. 파일을 나눈 적용 프로세스는 나중에 개별적으로 수행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="aa9e3-p112">**Create model**: Calculates a themes model from a segment of the files. The Apply process of dividing files is done separately at another time.</span></span>
    
  - <span data-ttu-id="aa9e3-p113">**적용 모델**:이 옵션은 모델을 이전에 생성 되어 아직 적용 하는 경우에 표시 됩니다. 이 테마에 따라 파일 나눌 됩니다.</span><span class="sxs-lookup"><span data-stu-id="aa9e3-p113">**Apply model**: This option is only shown if a model was created previously and not yet applied. This will divide the files based on the themes.</span></span>
    
2. <span data-ttu-id="aa9e3-155">**내보내기** 섹션:</span><span class="sxs-lookup"><span data-stu-id="aa9e3-155">In the **Export** section:</span></span> 
    
1. <span data-ttu-id="aa9e3-156">**Select 내보내기 일괄 처리**합니다.</span><span class="sxs-lookup"><span data-stu-id="aa9e3-156">In the **Select export batch**:</span></span>
    
  - <span data-ttu-id="aa9e3-157">**일괄 처리를 내보내기** 목록에서 일괄 처리 이름을 선택 하거나 내보내기 일괄 01, (기본 일괄 처리)에 결과 내보냅니다.</span><span class="sxs-lookup"><span data-stu-id="aa9e3-157">From the **Export batch** list, select the batch name or export results to Export batch 01, (the default batch).</span></span> 
    
  - <span data-ttu-id="aa9e3-p114">기존 사례에 추가한 새 파일에 대 한 결과 내보내려면 계속 하 여 현재 일괄 처리 진행 합니다. 일괄 처리의 세션을 만들려면 동일한 일괄 처리 수를 선택 하 고 **만들기 내보내기 세션을** 클릭 하는 증분 방식으로 이전 일괄 처리로 동일한 매개 변수를 내보내려면이 옵션을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="aa9e3-p114">To export results for new files that you added to an existing case, continue with your current batch. To create a session in the batch, select the same batch number and click **Create export session** You can use this option to export the same parameters as the previous batch, in an incremental manner.</span></span> 
    
  - <span data-ttu-id="aa9e3-p115">새 일괄 처리를 내보내려면 **추가**클릭![추가 아이콘](media/c2dd8b3a-5a22-412c-a7fa-143f5b2b5612.png) 및 **일괄 처리 이름** 에 새 이름을 입력 (하거나 기본값을 그대로) 및 **일괄 처리 설명**에서 설명 합니다. **확인**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="aa9e3-p115">To export to a new batch, click **Add**![add icon](media/c2dd8b3a-5a22-412c-a7fa-143f5b2b5612.png) and enter a new name in **Batch name** (or accept the default) and a description in **Batch description**. Click **OK**.</span></span>
    
  - <span data-ttu-id="aa9e3-162">일괄 처리 이름 또는 설명을 편집 하려면 **일괄 내보내기**의 이름을 선택, **편집** 을 클릭 하 ![편집 아이콘](media/3d613660-7602-4df2-bdb9-14e9ca2f9cf2.png), 다음 필드를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="aa9e3-162">To edit a batch name or description, select the name in **Export batch**, click **Edit** ![Edit icon](media/3d613660-7602-4df2-bdb9-14e9ca2f9cf2.png), and then modify the fields.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="aa9e3-p116">내보내기 일괄 처리에 대 한 세션을 실행 했을 때 한 후에 삭제할 수 없습니다. 또한 첫번째 세션 실행 되 면 일부 매개 변수를 편집할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="aa9e3-p116">After you've run sessions for an export batch, they cannot be deleted. In addition, only some parameters can be edited once the first session is run.</span></span> 
  
  - <span data-ttu-id="aa9e3-165">중복 내보내기 일괄 처리를 만들려면 **중복 내보내기 일괄 처리**를 선택![중복 내보내기 일괄 처리 아이콘을 만드는](media/3f6d5f59-e842-4946-a493-473528af0119.jpg) 하 고 패널에 이름과 중복 일괄 처리에 대 한 설명을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="aa9e3-165">To create a duplicate export batch, choose **Duplicate export batch**![Create a duplicate export batch icon](media/3f6d5f59-e842-4946-a493-473528af0119.jpg) and enter a name and a description for the duplicate batch in the panel.</span></span> 
    
  - <span data-ttu-id="aa9e3-166">내보내기 일괄 처리를 삭제 하려면 **삭제**를 선택![내보내기 일괄 처리 아이콘을 삭제](media/92a9f8e0-d469-48da-addb-69365e7ffb6f.jpg)합니다.</span><span class="sxs-lookup"><span data-stu-id="aa9e3-166">To delete an export batch, choose **Delete**![Delete an export batch icon](media/92a9f8e0-d469-48da-addb-69365e7ffb6f.jpg).</span></span>
    
  - <span data-ttu-id="aa9e3-167">일괄 처리의 기록을 보려면, **일괄 처리 기록**선택![보기 기록 아이콘](media/a80cc320-d96c-4d91-8884-75fe2cb147e2.jpg)합니다.</span><span class="sxs-lookup"><span data-stu-id="aa9e3-167">To view the history of a batch, choose **Batch history**![View history icon](media/a80cc320-d96c-4d91-8884-75fe2cb147e2.jpg).</span></span>
    
2. <span data-ttu-id="aa9e3-p117">정의 p에서 **opulation:** 내보내기 일괄 처리에 대 한 설정을 세부적으로 조정 하려는 경우 **관련성 제한 점수 위에 파일만 포함** 및/또는 **구체화 내보내기 일괄 처리** 를 선택 합니다. **관련성 제한 점수 위에 파일만 포함**을 선택 하는 경우 **문제** 를 사용 하도록 설정, 파일의 관련성 점수를 선택한 문제에 대 한 제한 점수 보다 더 높은 경우 다음 파일은 내보내야 합니다. 통해 제외 되는 파일을 내보낼 수는 ' **검토에 대 한** 필터입니다. **구체화 내보내기 일괄 처리**선택 하는 경우는 다음 **dupe 해제** 하 고 **'에 대 한 검토' 하 여 필터 필드** 라디오 단추를 사용할 수 있습니다. 선택 하는 경우 **취소 dupe**, 다음 중복 파일이 될 필터링 아웃 정의 된 정책에 따라: [수준 (기본값) 경우: 모든 집합이 중복 파일을 사용할 수 있는 전체 대/소문자에서 하나를 제외한 모든 파일 duped 해제 됩니다. 더불어 수준: 모든 집합이 중복 파일을 동일한 더불어 중에서 하나를 제외한 모든 파일 duped 해제 됩니다. 모든 중복 파일의 레코드는 내보내기 출력에 사용할 수 있습니다. **'검토용' 하 여 필터** 필드를 선택 하는 경우 **'검토용'** 필드 설정을 입력 하 **는 메타 데이터에서 수정** 선택 합니다. 패키지 콘텐츠의 원본 파일을 포함 하도록 **포함 입력된 파일**선택 합니다. 내보내기 프로세스의 속도 하려면이 옵션을 선택 취소할 수 있습니다. 참고 네이티브 파일을 사용 하 든 내보낼 수는 있습니다.</span><span class="sxs-lookup"><span data-stu-id="aa9e3-p117">Under Define p **opulation:** Select **Include only files above Relevance cut-off score** and/or **Refine export batch** if you want to fine-tune the settings for your export batch. If you select **Include only files above Relevance cut-off score**, then the **Issue** is enabled, and if the file's relevance score is higher than the cut-off score for the selected issue, then the file is exported. The file will be exported unless it's excluded by the ' **For review** filter. If you select **Refine export batch**, then the **De-dupe** and **Filter by 'For review' field** radio buttons are enabled. If you choose **De-dupe**, then duplicates files will be filtered-out according to the policy defined: [Case level (default): from every set of duplicate files in the entire case, all but one file will be de-duped. Custodian level: from every set of duplicate files of the same custodian, all but one file will be de-duped. A record of all duplicate files is available in export output. If you choose **Filter by 'For review'** field, select **Modify under Metadata** to enter your **'For review'** field settings. Select **Include input files**to include source files in the package content. You can clear this option to speed up the export process. Note that the Native files will be exported in any case.</span></span>
    
3. <span data-ttu-id="aa9e3-179">**메타 데이터 정의**(세션) 당한 번씩 **서식 파일 내보내기** 목록에서 다음 옵션 중에서 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="aa9e3-179">Under **Define metadata**, select from the following options in the **Export template** list (once per session).</span></span> 
    
  - <span data-ttu-id="aa9e3-p118">**표준**: 데이터 항목, 메타 데이터, 및 속성의 기본 설정 합니다. 데이터 가져오기 고급 eDiscovery에 이미 처리 된 및 내보내기 데이터는 이미 있는 파일을 포함 하는 시스템에 업로드 하는 경우이 옵션을 사용 합니다. 기본적으로 열을 만들고 채워야는 서식 파일을 내보냅니다.</span><span class="sxs-lookup"><span data-stu-id="aa9e3-p118">**Standard**: Basic set of data items, metadata, and properties. Use this option when import data was already processed in Advanced eDiscovery and export data is uploaded to a system that already contains the files. By default, export template columns are created and filled.</span></span>
    
  - <span data-ttu-id="aa9e3-p119">**모든**: 모든 처리 데이터와 분석 및 관련성 점수를 포함 하 여 표준 메타 데이터의 전체 집합입니다. 이 서식 파일은 처리를 수행 하는 고급 eDiscovery 및 파일 데이터를 처음으로 외부 시스템에 업로드 되는 경우에 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="aa9e3-p119">**All**: Full set of standard metadata including all processing data, as well as Analyze and Relevance scores. This template is required when Advanced eDiscovery performs the processing and file data is uploaded to an external system for the first time.</span></span>
    
  - <span data-ttu-id="aa9e3-185">**문제**: **모든 문제** 를 선택 하거나 만든 특정 문제를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="aa9e3-185">**Issues**: Select **All Issues** or select a particular issue you have created.</span></span> 
    
<span data-ttu-id="aa9e3-186">**확인**고급 설정을 저장 하려면 기본값을 사용 하 여 **기본값을 복원** 또는 고급 설정을 설정 하는 취소 하려면 **취소** 를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="aa9e3-186">Choose **OK**to save the advanced settings, **Restore defaults** to use default values, or **Cancel** to cancel setting the advanced settings.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="aa9e3-187">참고 항목</span><span class="sxs-lookup"><span data-stu-id="aa9e3-187">See also</span></span>
<span data-ttu-id="aa9e3-188"><a name="BK_AdvancedSettings"> </a></span><span class="sxs-lookup"><span data-stu-id="aa9e3-188"></span></span>

[<span data-ttu-id="aa9e3-189">Office 365 Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="aa9e3-189">Office 365 Advanced eDiscovery</span></span>](office-365-advanced-ediscovery.md)

