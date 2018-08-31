---
title: Office 365 Advanced eDiscovery에서 가져온된 파일을 추가하도록 로드 설정
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
ms.assetid: 0e0a9d04-294f-4f54-8bf1-b32d81345126
description: '마지막으로 정의 된 로드, 또는 Office 365 고급 eDiscovery의 관련성 교육을 수행 하기 전에 파일의 일괄 처리에 가져온된 파일을 추가 하는 단계를 검토 합니다.  '
ms.openlocfilehash: 2c986578b969b671351930fd6939a90e3a821dc2
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22534021"
---
# <a name="set-up-loads-to-add-imported-files-in-office-365-advanced-ediscovery"></a><span data-ttu-id="98754-103">Office 365 Advanced eDiscovery에서 가져온된 파일을 추가하도록 로드 설정</span><span class="sxs-lookup"><span data-stu-id="98754-103">Set up loads to add imported files in Office 365 Advanced eDiscovery</span></span>

> [!NOTE]
> <span data-ttu-id="98754-p101">고급 eDiscovery 조직에 대 한 고급 준수 추가 기능 또는 e 5 구독은 Office 365 E3 필요합니다. 해당 요금제에 가입한 상태 고급 eDiscovery 시도 하려는 하지 경우에 [Office 365 Enterprise e 5의 평가판 등록](https://go.microsoft.com/fwlink/p/?LinkID=698279)할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="98754-p101">Advanced eDiscovery requires an Office 365 E3 with the Advanced Compliance add-on or an E5 subscription for your organization. If you don't have that plan and want to try Advanced eDiscovery, you can [sign up for a trial of Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span></span> 
  
<span data-ttu-id="98754-p102">고급 eDiscovery 부하를 사례에 추가 되는 파일의 새 일괄 처리를입니다. 기본적으로 하나의 부하를 정의 하 고 모든 가져온된 파일에 추가 됩니다. 관련성 교육을 수행 하기 전에 부하에 가져온된 파일을 추가 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="98754-p102">In Advanced eDiscovery, a load is a new batch of files added to a case. By default, one load is defined and all imported files are added to it. Before performing Relevance training, imported files must be added to the load.</span></span> 
  
<span data-ttu-id="98754-109">다음과 같은 시나리오를 고려 하십시오.</span><span class="sxs-lookup"><span data-stu-id="98754-109">Consider the following scenarios:</span></span>
  
- <span data-ttu-id="98754-p103">새 파일 사례 데이터베이스에 로드 된 이전 파일에서 다음과 같은 것으로 알려진 되었거나 파일의 이전 부하 파일 컬렉션에서 임의의 집합입니다. 이 인스턴스에서 현재 파일을 로드 하려면 가져온된 파일을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="98754-p103">New files are known to be similar to the previous files loaded to the case database, or the previous load of files was a random set from the file collection. In this instance, add the imported files to the current file load.</span></span>
    
- <span data-ttu-id="98754-p104">새 파일 (예: 다른 원본의 경우)에서 이전 위치에서 다른 중이거나 유사 하거나 이전 부하를 서로 다른 그들 사전 정보가 없는 있습니다. 이 시나리오에서는 새 파일 부하를 가져온된 파일을 추가 합니다. 고급 eDiscovery 롤링 부하 시나리오와이 인식 하 고 따라잡기 프로세스를 호출, 후속 작업 완료 되 고 새 부하를 통합 하 고 교육을 받은 때까지 관련성 교육 및 일괄 처리는 계산에 잠금을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="98754-p104">New files are different from previous ones (for example, from a different source), or you have no prior knowledge that they're similar or different to the previous loads. In this scenario, add the imported files to a new file load. Advanced eDiscovery recognizes this as a Rolling loads scenario, invokes a Catch-up process, locks Relevance training and Batch calculations until Catch-up is completed, and the new load is integrated and trained.</span></span> 
    
## <a name="adding-imported-files-to-the-current-load"></a><span data-ttu-id="98754-115">현재 부하를 가져온된 파일 추가 (영문)</span><span class="sxs-lookup"><span data-stu-id="98754-115">Adding imported files to the current load</span></span>

<span data-ttu-id="98754-p105">가져온된 파일을 모두 고급 ediscovery에서 처리 되도록 부하에 추가 해야 합니다. 가져온된 파일은 마지막으로 정의 된 로드에 추가 됩니다. 나중에 추가 파일을 가져오면 자신이 해야에 추가 부하입니다.</span><span class="sxs-lookup"><span data-stu-id="98754-p105">All imported files must be added to a load to be processed in Advanced eDiscovery. Imported files are added to the last defined load. If you import additional files later, they also must be added to the load.</span></span>
  
1. <span data-ttu-id="98754-119">**관련성 \> 관련성 설치** 탭에서 **부하**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="98754-119">In the **Relevance \> Relevance setup** tab, select **Loads**.</span></span>
    
    ![관련성 설정 로드 탭](media/278aac7f-655f-462f-852a-6baa5d818768.png)
  
2. <span data-ttu-id="98754-p106">**포함 파일**:를 포함 하는 파일에 대 한 옵션을 선택 합니다. 기본적으로 현재 부하에 파일 추가 (영문)는 모집단을 기반으로 "모든 파일" 합니다.</span><span class="sxs-lookup"><span data-stu-id="98754-p106">**Include files**: Select an option for files to include. By default, adding files to the current load is based on the "All files" population.</span></span>
    
    > [!TIP]
    > <span data-ttu-id="98754-p107">관련성에 사용 가능한 모든 culled 파일을 로드 합니다. 사용 가능한 파일의 하위 집합만 로드 하려는 경우 먼저를 참고 하십시오를 지 원하는 대로 하위 집합을 로드 관련성 교육 저하 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="98754-p107">Load all available culled files into Relevance. If you plan to load only a subset of the available files, please first consult with Support, as loading subsets can adversely affect Relevance training.</span></span> 
  
3. <span data-ttu-id="98754-125">**로드 관리**는 부하를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="98754-125">In **Loads management**, select a load.</span></span>
    
4. <span data-ttu-id="98754-p108">**파일 추가**클릭 합니다. 파일 로드에 추가 됩니다 하 고 확인 메시지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="98754-p108">Click **Add files**. The files are added to the load and a confirmation message is displayed.</span></span> 
    
5. <span data-ttu-id="98754-128">**확인**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="98754-128">Click **OK**.</span></span>
    
<span data-ttu-id="98754-129">이제 파일의 파일을 교육에 대 한 고급 eDiscovery 관련성에에서 처리할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="98754-129">The files can now be processed in Advanced eDiscovery Relevance for training the files.</span></span>
  
## <a name="editing-a-load-name-within-a-case"></a><span data-ttu-id="98754-130">사례 내 부하 이름 편집</span><span class="sxs-lookup"><span data-stu-id="98754-130">Editing a load name within a case</span></span>

<span data-ttu-id="98754-131">부하 이름을 변경 하는 경우에 대/소문자를 중요 하는 이름을 사용 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="98754-131">If changing the load name, it is recommended to use a name that is significant to the case.</span></span>
  
1. <span data-ttu-id="98754-132">**관련성 \> 관련성 설치** 탭에서 **부하**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="98754-132">In the **Relevance \> Relevance setup** tab, select **Loads**.</span></span>
    
2. <span data-ttu-id="98754-p109">**부하 관리** 목록에서 부하를 선택 하 고 **편집** 아이콘을 클릭 합니다. 편집 부하 창이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="98754-p109">From the **Loads management** list, select a load and click the **Edit** icon. The Edit load window is displayed.</span></span> 
    
3. <span data-ttu-id="98754-135">변경 내용을 입력 하 고 **확인**을 클릭 한 다음 키를 누릅니다.</span><span class="sxs-lookup"><span data-stu-id="98754-135">Enter the changes, and then click **OK**.</span></span>
    
## <a name="adding-imported-files-to-a-new-load"></a><span data-ttu-id="98754-136">새 부하를 가져온된 파일 추가 (영문)</span><span class="sxs-lookup"><span data-stu-id="98754-136">Adding imported files to a new load</span></span>

<span data-ttu-id="98754-137">관련성 교육 또는 일괄 처리 계산 수행를 시작한 후 가져오기 파일의 추가 집합을 처리 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="98754-137">After starting Relevance training or performing Batch calculation, you may want to import and process an additional set of files.</span></span> 
  
<span data-ttu-id="98754-p110">후속 작업을 하는 동안, 태그 지정을 만들고 수 후속 작업 집합을 분석 합니다. 고급 eDiscovery의 관련성 및 비 관련성 파일을 이전 부하에 게 새 부하에서의 평가 비교합니다. 결과에 따르면 하는 메시지가 후속 의사 결정을 필요에 따라 및 고급 eDiscovery 경과 관련성 정보를 기반으로 권장 사항을 제공 하는 경우.</span><span class="sxs-lookup"><span data-stu-id="98754-p110">During Catch-up, you can create, tag, and analyze the Catch-up set. Advanced eDiscovery compares its assessment of Relevant and Non-Relevant files in the new load to those in previous loads. Based on the results, you are prompted to make Catch-up decisions, if necessary, and Advanced eDiscovery provides recommendations based on the accrued Relevance information.</span></span> 
  
<span data-ttu-id="98754-141">부하 및 따라잡기 기능 롤링 달라 집니다 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="98754-141">Rolling Loads and Catch-up functionality varies as follows:</span></span> 
  
- <span data-ttu-id="98754-142">일괄 처리 계산 후 새 파일 부하를 가져올 때 고급 eDiscovery는 다음 범주 중 하나에 속합니다 파일 범위에 따라 결정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="98754-142">When you import a new file load after Batch calculation, Advanced eDiscovery determines to what extent the files fall into one of the following categories:</span></span>
    
  - <span data-ttu-id="98754-143">유사한 (동종): 관련성 교육의 새로운, 사용자 지정 라운드 필수 이며 이전 부하를 계산 하는 기술에 적용할 수 "있는 그대로" 새 부하입니다.</span><span class="sxs-lookup"><span data-stu-id="98754-143">Similar (homogeneous): A new, custom round of Relevance training is not required and the knowledge accrued from the previous load can be applied "as is" to the new load.</span></span> 
    
  - <span data-ttu-id="98754-144">Distinct (혼성): 관련성 교육의 새로운, 사용자 지정 라운드가 필요 하며, 이전 부하에서 계산 된 정보를 적용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="98754-144">Distinct (heterogeneous): A new, custom round of Relevance training is required, and the knowledge accrued from the previous load cannot be applied.</span></span> 
    
    <span data-ttu-id="98754-145">이러한 용어 간의 로드 하 고 부하 내에 있지 않은 파일의 유사의 수준을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="98754-145">These terms refer to the level of similarity of files between loads and not within the loads.</span></span> 
    
- <span data-ttu-id="98754-p111">관련성 교육 (하기 전에 일괄 처리 계산) 하는 동안 새 파일 부하를 가져올 때 후속 united 파일 집합에서 관련성 교육을 계속할 수 있습니다. 고급 eDiscovery 새 부하를 유사 하거나 이전 부하에서 고유한 인지 예상 하지 않습니다. 단순히 새 부하에 대 한 정보를 수집 하 고 관련성 수 있도록 설정 하는 파일의 새 및 이전에 계속 하려면 교육 합니다.</span><span class="sxs-lookup"><span data-stu-id="98754-p111">When importing a new file load during Relevance training (before Batch calculation), Catch-up enables you to continue Relevance training on the united file set. Advanced eDiscovery does not estimate whether the new load is similar to or distinct from the previous load. It simply collects information about the new load and enables Relevance training to continue on the new and previous sets of files.</span></span> 
    
- <span data-ttu-id="98754-149">일괄 처리 계산 후 관련성 교육의 여러 문제는 물론 문제 되 면 모든 문제에 대 한 후속 작업 프로세스를 한번씩 수행 및 결과 계산 하 고 각 문제에 대 한 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="98754-149">When there are multiple issues in Relevance training as well as issues after Batch calculation, the Catch-up process is performed once for all issues, and the results are calculated and displayed for each issue.</span></span>
    
> [!NOTE]
> <span data-ttu-id="98754-p112">후속 샘플의 크기를 다를 수 있습니다. 새 부하를 추가 하기 전에 완료 하는 샘플 수와 이전 부하를 기준으로 새 부하의 크기에 따라 다릅니다. 후속 샘플은 일반적으로 새 부하에서 200 2, 000 파일 집합이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="98754-p112">The size of the Catch-up sample may vary. It depends on the size of the new load relative to the previous loads, and on the number of samples completed before adding the new load. The Catch-up sample is typically a set of 200 to 2,000 files from the new load.</span></span> 
  
> [!TIP]
> <span data-ttu-id="98754-p113">후속 작업 다른 작업을 중지 하 고 개별 파일에 태그를 지정 하 고 이러한 검토 해야 합니다. 따라서을 줄일 수 있습니다 오버 헤드 대량 일괄 처리에서 새 파일을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="98754-p113">Catch-up stops any other tasks and requires individual file tagging and review. Therefore, you can reduce overhead when you add new files in large batches.</span></span> 
  
## <a name="adding-a-new-file-load-using-catch-up-and-rolling-loads"></a><span data-ttu-id="98754-155">로드 따라잡기 및 롤링을 사용 하 여 새 파일 부하를 추가 (영문)</span><span class="sxs-lookup"><span data-stu-id="98754-155">Adding a new file load using Catch-up and Rolling loads</span></span>

1. <span data-ttu-id="98754-156">**관련성 \> 관련성 설치** 탭에서 **부하**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="98754-156">In the **Relevance \> Relevance setup** tab, select **Loads**.</span></span>
    
2. <span data-ttu-id="98754-p114">**부하 관리**를 클릭은 **+** 부하를 추가 하는 아이콘입니다. 확인 메시지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="98754-p114">Under **Loads management**, click the **+** icon to add a load. A confirmation message is displayed.</span></span> 
    
3. <span data-ttu-id="98754-p115">**예** 를 계속을 클릭 합니다. **새 추가 로드** 대화 상자가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="98754-p115">Click **Yes** to continue. The **Add new load** dialog is displayed.</span></span> 
    
    > [!NOTE]
    > <span data-ttu-id="98754-161">이전 부하에 작업을 수행한 경우에 새 부하를 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="98754-161">You can only add a new load if actions were performed to the previous load.</span></span> 
  
4. <span data-ttu-id="98754-p116">**새 추가 로드** 대화 상자에서 **이름을 로드** 하 고 **설명** 에 정보를 입력 한 다음 **확인**을 클릭 합니다. 새 부하를 추가 하는 고급 eDiscovery입니다.</span><span class="sxs-lookup"><span data-stu-id="98754-p116">In the **Add new load** dialog, type information in **Load name** and **Description** and then click **OK**. Advanced eDiscovery adds a new load.</span></span>
    
5. <span data-ttu-id="98754-p117">새 부하 파일을 가져오려면 **파일 추가**클릭 합니다. 새 파일을 모두이 부하에 추가 됩니다. 고급 eDiscovery 가져옵니다 파일을 한 후 롤링 부하 시나리오를 인식 하 고 단계에서는으로 후속 작업을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="98754-p117">To import the new load file, click **Add files**. All new files are added to this load. After Advanced eDiscovery imports the files, it recognizes the Rolling loads scenario and indicates Catch-up as the next step.</span></span>
    
6. <span data-ttu-id="98754-167">시나리오를 실행 하는 대화 상자 맨아래에 있는 **후속 작업** 을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="98754-167">Click **Catch-up** at the bottom of the dialog to run the scenario.</span></span> 
    
    <span data-ttu-id="98754-168">일반적으로 새 부하에서 200 2, 000 파일이 포함 된 단일 후속 작업 집합을 동시 파일에 태그 지정을 허용 하려면 모든 문제에 대해 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="98754-168">A single Catch-up set, typically containing 200 to 2,000 files from the new load, is created for all issues to allow concurrent file tagging.</span></span>
    
    <span data-ttu-id="98754-169">유사 하거나 고유한 로드에는 여부, 고급 eDiscovery 병합 또는 부하를 자동으로 분할 여부 및 정보에 대 한 자세한 내용은 제공 다음 단계에서 처리과 관련 하 여 합니다.</span><span class="sxs-lookup"><span data-stu-id="98754-169">Details are provided about whether loads are similar or distinct, whether Advanced eDiscovery merged or split the loads automatically, and information regarding processing in the next step.</span></span>
    
    <span data-ttu-id="98754-p118">다음 파일에 태그 지정 하 고 실행할 수 계산 작업 합니다. 태그 지정 관련성을 유사 하거나 고유한 로드 되었는지 여부를 확인할 수 있도록 하 고 파일의 새 집합에 작업을 계속할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="98754-p118">You can then tag files and run a calculate operation. The tagging enables Relevance to determine if loads are similar or distinct and enables you to continue working on the new set of files.</span></span>
    
7. <span data-ttu-id="98754-172">후속 작업 집합을 검토 한 후 보기 **관련성 \> 추적** 후속 작업 결과 대 한 합니다.</span><span class="sxs-lookup"><span data-stu-id="98754-172">After the Catch-up set is reviewed, view **Relevance \> Track** for the Catch-up results.</span></span> 
    
1. <span data-ttu-id="98754-173">관련성 교육 하는 동안 추가 된 새 파일을 로드 하는 경우 (즉,이 문제는 아직 통과 하지 일괄 처리 계산), **계속** 교육은 후속 작업 결과 관계 없이 다음 단계입니다.</span><span class="sxs-lookup"><span data-stu-id="98754-173">If the new file load was added during Relevance training (meaning, the issue has not yet gone through Batch calculation), **Continue training** is the next step, regardless of the Catch-up results.</span></span> 
    
    <span data-ttu-id="98754-p119">새로 추가 되거나 이전 부하를 처리 하는 하나의 부하로 및 관련성 교육 united 집합으로 계속 합니다. 이 절차를 완료 됩니다 및 관련성 교육을 계속할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="98754-p119">The new and previous loads are processed as one load and Relevance training continues on the united set. You are now finished with this procedure and can continue Relevance training.</span></span> 
    
2. <span data-ttu-id="98754-176">사용자는 일괄 처리 계산 후 추가 되었지만 새 부하 하는 경우 다음 단계를 진행 합니다.</span><span class="sxs-lookup"><span data-stu-id="98754-176">If the new load was added after Batch calculation, proceed to the following steps.</span></span>
    
8. <span data-ttu-id="98754-177">일괄 처리 계산 뒤에 추가 하는 새 부하에 대 한 고급 eDiscovery 인지를 결정 하는 경우 새 부하와 비슷합니다 이전 부하에서 고유한 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="98754-177">For new loads added after Batch calculation, Advanced eDiscovery determines if the new load is similar to or distinct from previous loads, as follows:</span></span>
    
1. <span data-ttu-id="98754-p120">비슷한 되도록 부하를 찾았습니다: 필요는 없음 추가 관련성 교육 합니다. 대시보드는 권장된 다음 단계를 실행 하는 것을 보여주는 * * 계산 일괄 * * 새 부하에 대 한 관련성 점수 계산을 다시 합니다. 로드 이전 분류자 분석에서 새 파일에서 실행 될 수 있으므로 마찬가지로 될 것으로 밝혀졌습니다.</span><span class="sxs-lookup"><span data-stu-id="98754-p120">If loads were found to be similar: No additional Relevance training is necessary. The dashboard shows the recommended next step is to run ** Batch calculation ** again to calculate Relevance scores for the new load. Loads were found to be similar, so the previous classifier analysis can be run on the new files.</span></span> 
    
2. <span data-ttu-id="98754-p121">고유한 되도록 부하를 찾았습니다: 보다 관련성 교육 필요한 이며 다음 단계에서는 후속 결정 합니다. 후속 작업 의사 결정을 다음과 같이 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="98754-p121">If loads were found to be distinct: More Relevance training is necessary and the next step is Catch-up decision. Select a Catch-up decision as follows:</span></span>
    
    <span data-ttu-id="98754-p122">**부하를 병합**을 선택 하는 경우 고급 eDiscovery 교육 집합에 대 한 이전 버전과 새 부하를 병합 합니다. 첫번째 부하 일괄 처리 계산을 통해 제공 하기 위해, 하지만 더 많은 교육 필요 합니다. 새로 추가 되거나 이전 부하를 함께 교육을 계속 합니다. 일괄 처리 계산은 다음을 다시 실행 하 고 이전 일괄 처리 계산 점수를 무시할지 키를 누릅니다. 기존 부하에 대 한 관련성 점수 다시 계산할 수 있습니다, 예, 기존 파일 로드의 검토 시작 되지 않은 경우 하는 경우이 선택 영역을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="98754-p122">If you select **Merge loads**, Advanced eDiscovery merges previous and new loads for the training set. Although the first load went through Batch calculation, more training is needed. Continue training new and previous loads together. Batch calculation will then run again and the previous Batch calculation scores should be ignored. Choose this selection when Relevance scores for existing loads can be recalculated, for example, when review of existing file loads has not started.</span></span>
    
    <span data-ttu-id="98754-p123">**로드 하는 분할을**선택 하는 경우 새 부하에 대해서만 관련성 교육을 계속 합니다. 이 인스턴스에서 이전 일괄 처리 계산 점수 그대로 유지 됩니다. 기존 부하의 검토 이미 시작 된 경우 기존 부하에 대 한 관련성 점수가 포함 된 기존 다시 계산 되지, 예 하는 경우이 옵션을 선택 합니다. 관련성 점수가 포함 된 현재이 위치에서 별도로 관리 하 고 병합 될 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="98754-p123">If you select **Split loads**, continue Relevance training only on the new load. In this instance, previous Batch calculation scores will remain as is. Choose this option when existing Relevance scores for existing loads cannot be recalculated, for example, if review of existing loads has already started. Relevance scores are managed separately from this point onward and cannot be merged.</span></span>
    
3. <span data-ttu-id="98754-192">**계속 교육**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="98754-192">Click **Continue training**.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="98754-193">참고 항목</span><span class="sxs-lookup"><span data-stu-id="98754-193">See also</span></span>

[<span data-ttu-id="98754-194">Office 365 Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="98754-194">Office 365 Advanced eDiscovery</span></span>](office-365-advanced-ediscovery.md)
  
[<span data-ttu-id="98754-195">문제를 정의 하 고 사용자를 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="98754-195">Defining issues and assigning users</span></span>](define-issues-and-assign-users.md)
  
[<span data-ttu-id="98754-196">정의 키워드를 강조 표시 하 고 고급 옵션</span><span class="sxs-lookup"><span data-stu-id="98754-196">Defining highlighted keywords and advanced options</span></span>](define-highlighted-keywords-and-advanced-options.md)

