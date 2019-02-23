---
title: Office 365 Advanced eDiscovery에서 가져온된 파일을 추가하도록 로드 설정
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
ms.assetid: 0e0a9d04-294f-4f54-8bf1-b32d81345126
description: 'Office 365 Advanced eDiscovery에서 관련성 훈련을 수행 하기 전에 가져온 파일을 마지막으로 정의한 부하 또는 일괄 파일에 추가 하는 단계를 검토 합니다.  '
ms.openlocfilehash: 8c5101628b468719f8aa4f81a4c73cbbb226105f
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30215988"
---
# <a name="set-up-loads-to-add-imported-files-in-office-365-advanced-ediscovery"></a><span data-ttu-id="1b341-103">Office 365 Advanced eDiscovery에서 가져온된 파일을 추가하도록 로드 설정</span><span class="sxs-lookup"><span data-stu-id="1b341-103">Set up loads to add imported files in Office 365 Advanced eDiscovery</span></span>

> [!NOTE]
> <span data-ttu-id="1b341-p101">Advanced eDiscovery를 사용하려면 Office 365 E3의 고급 준수 추가 기능이나 조직을 위한 E5 구독이 필요합니다. 이 요금제가 없는 상태에서 Advanced eDiscovery를 사용하려는 경우에는 [Office 365 Enterprise E5 평가판을 등록](https://go.microsoft.com/fwlink/p/?LinkID=698279)할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1b341-p101">Advanced eDiscovery requires an Office 365 E3 with the Advanced Compliance add-on or an E5 subscription for your organization. If you don't have that plan and want to try Advanced eDiscovery, you can [sign up for a trial of Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span></span> 
  
<span data-ttu-id="1b341-p102">고급 eDiscovery에서는 사례에 추가 된 새 파일 배치가 로드 됩니다. 기본적으로 하나의 부하가 정의 되 고 가져온 모든 파일이 추가 됩니다. 관련성 있는 학습을 수행 하기 전에 가져온 파일을 로드에 추가 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b341-p102">In Advanced eDiscovery, a load is a new batch of files added to a case. By default, one load is defined and all imported files are added to it. Before performing Relevance training, imported files must be added to the load.</span></span> 
  
<span data-ttu-id="1b341-109">다음과 같은 시나리오를 고려해 야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b341-109">Consider the following scenarios:</span></span>
  
- <span data-ttu-id="1b341-p103">새 파일은 사례 데이터베이스에 로드 된 이전 파일에 해당 하는 것으로 알려져 있거나 파일의 이전 부하는 file 컬렉션에서 임의로 설정 된 것입니다. 이 인스턴스에서 가져온 파일을 현재 파일 로드에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b341-p103">New files are known to be similar to the previous files loaded to the case database, or the previous load of files was a random set from the file collection. In this instance, add the imported files to the current file load.</span></span>
    
- <span data-ttu-id="1b341-p104">새 파일이 이전 파일과는 다른 경우 (예: 다른 원본에서 가져온 파일) 또는 이전 부하와 비슷하거나 다른 이전 지식이 없는 경우 이 시나리오에서는 가져온 파일을 새 파일 로드에 추가 합니다. 고급 eDiscovery에서는이를 롤링 부하 시나리오로 인식 하 고, 보완 프로세스를 호출 하 고, 보완 작업을 완료 하 고, 새 부하를 통합 하 고 교육 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b341-p104">New files are different from previous ones (for example, from a different source), or you have no prior knowledge that they're similar or different to the previous loads. In this scenario, add the imported files to a new file load. Advanced eDiscovery recognizes this as a Rolling loads scenario, invokes a Catch-up process, locks Relevance training and Batch calculations until Catch-up is completed, and the new load is integrated and trained.</span></span> 
    
## <a name="adding-imported-files-to-the-current-load"></a><span data-ttu-id="1b341-115">가져온 파일을 현재 부하에 추가</span><span class="sxs-lookup"><span data-stu-id="1b341-115">Adding imported files to the current load</span></span>

<span data-ttu-id="1b341-p105">고급 eDiscovery에서 처리 되려면 가져온 모든 파일을 로드에 추가 해야 합니다. 가져온 파일은 마지막으로 정의 된 로드에 추가 됩니다. 나중에 추가 파일을 가져오는 경우 해당 파일도 로드에 추가 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b341-p105">All imported files must be added to a load to be processed in Advanced eDiscovery. Imported files are added to the last defined load. If you import additional files later, they also must be added to the load.</span></span>
  
1. <span data-ttu-id="1b341-119">**관련성 \> 관련성 설정** 탭에서 **로드**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b341-119">In the **Relevance \> Relevance setup** tab, select **Loads**.</span></span>
    
    ![관련성 설정 로드 탭](media/278aac7f-655f-462f-852a-6baa5d818768.png)
  
2. <span data-ttu-id="1b341-p106">**포함 파일**: 포함할 파일에 대 한 옵션을 선택 합니다. 기본적으로 현재 부하에 파일을 추가 하는 것은 "모든 파일" 채우기를 기반으로 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b341-p106">**Include files**: Select an option for files to include. By default, adding files to the current load is based on the "All files" population.</span></span>
    
    > [!TIP]
    > <span data-ttu-id="1b341-p107">사용 가능한 모든 culled 파일을 관련성 있게 로드 합니다. 사용 가능한 파일의 하위 집합만 로드 하려는 경우에는 하위 집합 로드에 따라 관련성 교육이 저하 될 수 있으므로 먼저 지원에 문의 하세요.</span><span class="sxs-lookup"><span data-stu-id="1b341-p107">Load all available culled files into Relevance. If you plan to load only a subset of the available files, please first consult with Support, as loading subsets can adversely affect Relevance training.</span></span> 
  
3. <span data-ttu-id="1b341-125">**로드 관리**에서 부하를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b341-125">In **Loads management**, select a load.</span></span>
    
4. <span data-ttu-id="1b341-p108">**파일 추가**를 클릭 합니다. 파일이 부하에 추가 되 고 확인 메시지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1b341-p108">Click **Add files**. The files are added to the load and a confirmation message is displayed.</span></span> 
    
5. <span data-ttu-id="1b341-128">**확인**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="1b341-128">Click **OK**.</span></span>
    
<span data-ttu-id="1b341-129">이제 파일을 교육 하는 데 필요한 고급 eDiscovery 관련성에 의해 파일이 처리 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1b341-129">The files can now be processed in Advanced eDiscovery Relevance for training the files.</span></span>
  
## <a name="editing-a-load-name-within-a-case"></a><span data-ttu-id="1b341-130">사례 내에서 부하 이름 편집</span><span class="sxs-lookup"><span data-stu-id="1b341-130">Editing a load name within a case</span></span>

<span data-ttu-id="1b341-131">로드 이름을 변경 하는 경우에는 사례에 중요 한 이름을 사용 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="1b341-131">If changing the load name, it is recommended to use a name that is significant to the case.</span></span>
  
1. <span data-ttu-id="1b341-132">**관련성 \> 관련성 설정** 탭에서 **로드**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b341-132">In the **Relevance \> Relevance setup** tab, select **Loads**.</span></span>
    
2. <span data-ttu-id="1b341-p109">**로드 관리** 목록에서 부하를 선택 하 고 **편집** 아이콘을 클릭 합니다. 로드 편집 창이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1b341-p109">From the **Loads management** list, select a load and click the **Edit** icon. The Edit load window is displayed.</span></span> 
    
3. <span data-ttu-id="1b341-135">변경 내용을 입력 하 고 **확인**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b341-135">Enter the changes, and then click **OK**.</span></span>
    
## <a name="adding-imported-files-to-a-new-load"></a><span data-ttu-id="1b341-136">가져온 파일을 새 부하에 추가</span><span class="sxs-lookup"><span data-stu-id="1b341-136">Adding imported files to a new load</span></span>

<span data-ttu-id="1b341-137">관련성 훈련을 시작 하거나 일괄 처리를 수행한 후에는 추가 파일 집합을 가져오고 처리할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1b341-137">After starting Relevance training or performing Batch calculation, you may want to import and process an additional set of files.</span></span> 
  
<span data-ttu-id="1b341-p110">보완 중에는 보완 집합을 만들고 태그를 작성 하 고 분석할 수 있습니다. Advanced eDiscovery에서는 새 부하의 관련 파일과 관련 없는 파일에 대 한 평가를 이전 로드의 경우와 비교 합니다. 결과에 따라, 필요한 경우 보완 결정을 내릴 것인지 묻는 메시지가 표시 되 고, 고급 eDiscovery는 계산 된 관련성 정보를 기반으로 하는 권장 사항을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b341-p110">During Catch-up, you can create, tag, and analyze the Catch-up set. Advanced eDiscovery compares its assessment of Relevant and Non-Relevant files in the new load to those in previous loads. Based on the results, you are prompted to make Catch-up decisions, if necessary, and Advanced eDiscovery provides recommendations based on the accrued Relevance information.</span></span> 
  
<span data-ttu-id="1b341-141">롤링 로드와 보완 기능은 다음과 같이 달라 집니다.</span><span class="sxs-lookup"><span data-stu-id="1b341-141">Rolling Loads and Catch-up functionality varies as follows:</span></span> 
  
- <span data-ttu-id="1b341-142">일괄 처리 후 새 파일 부하를 가져올 경우 Advanced eDiscovery에서는 파일이 다음 범주 중 하나에 속하는 범위를 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b341-142">When you import a new file load after Batch calculation, Advanced eDiscovery determines to what extent the files fall into one of the following categories:</span></span>
    
  - <span data-ttu-id="1b341-143">유사 (유형이 같은 항목): 새로운 사용자 지정 관련성 학습 라운드는 필요 하지 않으며 이전 부하 로부터 계산 된 정보를 새 부하에 "있는 그대로" 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1b341-143">Similar (homogeneous): A new, custom round of Relevance training is not required and the knowledge accrued from the previous load can be applied "as is" to the new load.</span></span> 
    
  - <span data-ttu-id="1b341-144">고유 (이기종): 새로운 사용자 지정 관련성 교육이 필요 하며 이전 부하 로부터 계산 된 정보를 적용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="1b341-144">Distinct (heterogeneous): A new, custom round of Relevance training is required, and the knowledge accrued from the previous load cannot be applied.</span></span> 
    
    <span data-ttu-id="1b341-145">이러한 용어는 로드 범위 내에서와 로드 사이에 있는 파일의 유사성 수준을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="1b341-145">These terms refer to the level of similarity of files between loads and not within the loads.</span></span> 
    
- <span data-ttu-id="1b341-p111">일괄 처리를 수행 하는 동안 새 파일 로드를 가져올 때의 보완 기능을 사용 하면 미국 파일 집합에 대 한 관련성 있는 교육을 계속할 수 있습니다. Advanced eDiscovery에서는 새 부하가 이전 부하와 비슷하거나 다른 지 여부를 예측 하지 않습니다. 이 명령은 새 부하에 대 한 정보를 수집 하 고, 새 파일 집합 및 이전에 실행 되는 다양 한 형식의 관련 교육을 가능 하 게 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b341-p111">When importing a new file load during Relevance training (before Batch calculation), Catch-up enables you to continue Relevance training on the united file set. Advanced eDiscovery does not estimate whether the new load is similar to or distinct from the previous load. It simply collects information about the new load and enables Relevance training to continue on the new and previous sets of files.</span></span> 
    
- <span data-ttu-id="1b341-149">일괄 처리를 수행한 후 발생 하는 문제와 관련 교육에 여러 문제가 있는 경우 모든 문제에 대해 보완 프로세스를 한 번 수행 하면 결과가 계산 되어 각 문제에 대해 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1b341-149">When there are multiple issues in Relevance training as well as issues after Batch calculation, the Catch-up process is performed once for all issues, and the results are calculated and displayed for each issue.</span></span>
    
> [!NOTE]
> <span data-ttu-id="1b341-p112">보완 샘플의 크기는 다를 수 있습니다. 이 도구는 이전 부하를 기준으로 하는 새 부하의 크기와 새 로드를 추가 하기 전에 완료 된 샘플 수에 따라 달라 집니다. 보완 샘플은 일반적으로 새 부하에서 200 ~ 2000 파일의 집합입니다.</span><span class="sxs-lookup"><span data-stu-id="1b341-p112">The size of the Catch-up sample may vary. It depends on the size of the new load relative to the previous loads, and on the number of samples completed before adding the new load. The Catch-up sample is typically a set of 200 to 2,000 files from the new load.</span></span> 
  
> [!TIP]
> <span data-ttu-id="1b341-p113">이 경우 다른 작업을 중지 하 고 개별 파일 태그 지정 및 검토를 수행 해야 합니다. 따라서 대규모 일괄 처리에서 새 파일을 추가할 때 오버 헤드를 줄일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1b341-p113">Catch-up stops any other tasks and requires individual file tagging and review. Therefore, you can reduce overhead when you add new files in large batches.</span></span> 
  
## <a name="adding-a-new-file-load-using-catch-up-and-rolling-loads"></a><span data-ttu-id="1b341-155">찾기 및 롤링 부하를 사용 하 여 새 파일 부하 추가</span><span class="sxs-lookup"><span data-stu-id="1b341-155">Adding a new file load using Catch-up and Rolling loads</span></span>

1. <span data-ttu-id="1b341-156">**관련성 \> 관련성 설정** 탭에서 **로드**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b341-156">In the **Relevance \> Relevance setup** tab, select **Loads**.</span></span>
    
2. <span data-ttu-id="1b341-p114">부하 **management**에서 **+** 아이콘을 클릭 하 여 로드를 추가 합니다. 확인 메시지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1b341-p114">Under **Loads management**, click the **+** icon to add a load. A confirmation message is displayed.</span></span> 
    
3. <span data-ttu-id="1b341-p115">**예** 를 클릭 하 여 계속 합니다. **새 부하 추가** 대화 상자가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1b341-p115">Click **Yes** to continue. The **Add new load** dialog is displayed.</span></span> 
    
    > [!NOTE]
    > <span data-ttu-id="1b341-161">이전 부하로 작업을 수행한 경우에만 새 부하를 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1b341-161">You can only add a new load if actions were performed to the previous load.</span></span> 
  
4. <span data-ttu-id="1b341-p116">**새 부하 추가** 대화 상자에서 **로드 이름** 및 **설명** 에 정보를 입력 하 고 **확인**을 클릭 합니다. 고급 eDiscovery 새 부하를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b341-p116">In the **Add new load** dialog, type information in **Load name** and **Description** and then click **OK**. Advanced eDiscovery adds a new load.</span></span>
    
5. <span data-ttu-id="1b341-p117">새 로드 파일을 가져오려면 **파일 추가**를 클릭 합니다. 모든 새 파일이이 부하에 추가 됩니다. Advanced eDiscovery에서는 파일을 가져오지만 롤링 로드 시나리오를 인식 하 고 다음 단계로 보완 됨을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="1b341-p117">To import the new load file, click **Add files**. All new files are added to this load. After Advanced eDiscovery imports the files, it recognizes the Rolling loads scenario and indicates Catch-up as the next step.</span></span>
    
6. <span data-ttu-id="1b341-167">대화 상자 아래쪽의 **보완** 을 클릭 하 여 시나리오를 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b341-167">Click **Catch-up** at the bottom of the dialog to run the scenario.</span></span> 
    
    <span data-ttu-id="1b341-168">동시 파일 태깅을 허용 하기 위해 모든 문제에 대해 새 부하의 200 파일을 포함 하는 단일 찾기 집합을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="1b341-168">A single Catch-up set, typically containing 200 to 2,000 files from the new load, is created for all issues to allow concurrent file tagging.</span></span>
    
    <span data-ttu-id="1b341-169">자세한 내용은 부하가 비슷하거나 비슷한지, Advanced eDiscovery가 자동으로 로드 되는지 여부 및 다음 단계의 처리와 관련 된 정보를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b341-169">Details are provided about whether loads are similar or distinct, whether Advanced eDiscovery merged or split the loads automatically, and information regarding processing in the next step.</span></span>
    
    <span data-ttu-id="1b341-p118">그런 다음 파일에 태그를 지정한 후 계산 작업을 실행할 수 있습니다. 태그 지정 기능을 사용 하면 부하가 비슷하거나 다른 지 여부를 확인 하 고 새 파일 집합에서 계속 작업할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1b341-p118">You can then tag files and run a calculate operation. The tagging enables Relevance to determine if loads are similar or distinct and enables you to continue working on the new set of files.</span></span>
    
7. <span data-ttu-id="1b341-172">보완 집합을 검토 한 후에는 검색 결과에 대 한 **관련성 \> 추적** 을 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1b341-172">After the Catch-up set is reviewed, view **Relevance \> Track** for the Catch-up results.</span></span> 
    
1. <span data-ttu-id="1b341-173">관련성 성향 습득 중에 새 파일 로드가 추가 된 경우 (즉, 문제가 아직 처리 되지 않은 경우), 보완 결과에 관계 없이 다음 단계를 **계속 진행** 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b341-173">If the new file load was added during Relevance training (meaning, the issue has not yet gone through Batch calculation), **Continue training** is the next step, regardless of the Catch-up results.</span></span> 
    
    <span data-ttu-id="1b341-p119">새 로드와 이전 부하는 미국에서 계속 해 서 한 부하 및 관련성 교육이 진행 되는 것으로 처리 됩니다. 이제이 절차를 마치고 관련성이 있는 교육을 계속할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1b341-p119">The new and previous loads are processed as one load and Relevance training continues on the united set. You are now finished with this procedure and can continue Relevance training.</span></span> 
    
2. <span data-ttu-id="1b341-176">일괄 처리를 수행한 후에 새 부하를 추가한 경우에는 다음 단계를 진행 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b341-176">If the new load was added after Batch calculation, proceed to the following steps.</span></span>
    
8. <span data-ttu-id="1b341-177">일괄 처리를 수행한 후 추가 되는 새 부하에 대해 Advanced eDiscovery는 다음과 같이 새 부하가 이전 로드와 비슷한지 또는 다른 지를 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b341-177">For new loads added after Batch calculation, Advanced eDiscovery determines if the new load is similar to or distinct from previous loads, as follows:</span></span>
    
1. <span data-ttu-id="1b341-p120">로드가 유사 하다 고 발견 되 면 추가 관련성 교육이 필요 하지 않습니다. 다음은 새 부하에 대 한 관련성 점수를 계산 하기 위해 \* \* 일괄 처리 계산 \* \*을 다시 실행 하는 것을 권장 하는 예제입니다. 로드가 유사한 것으로 확인 되어 이전 분류자 분석을 새 파일에서 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1b341-p120">If loads were found to be similar: No additional Relevance training is necessary. The dashboard shows the recommended next step is to run \*\* Batch calculation \*\* again to calculate Relevance scores for the new load. Loads were found to be similar, so the previous classifier analysis can be run on the new files.</span></span> 
    
2. <span data-ttu-id="1b341-p121">부하가 distinct 인 경우: 보다 관련성 있는 교육이 필요 하며 다음 단계는 보완 결정입니다. 다음과 같이 보완 결정 사항을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b341-p121">If loads were found to be distinct: More Relevance training is necessary and the next step is Catch-up decision. Select a Catch-up decision as follows:</span></span>
    
    <span data-ttu-id="1b341-p122">**병합 부하**를 선택 하면 학습 집합에 대 한 이전 및 새 부하 병합이 진행 됩니다. 첫 번째 부하는 일괄 계산을 통해 발생 했지만 더 많은 교육이 필요 합니다. 새 및 이전 부하를 함께 계속 해 서 교육 합니다. 그러면 일괄 처리가 다시 실행 되 고 이전 일괄 계산 점수가 무시 됩니다. 예를 들어 기존 파일 로드 검토가 시작 되지 않은 경우와 같이 기존 부하에 대 한 관련성 점수를 다시 계산할 수 있는 경우이 옵션을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b341-p122">If you select **Merge loads**, Advanced eDiscovery merges previous and new loads for the training set. Although the first load went through Batch calculation, more training is needed. Continue training new and previous loads together. Batch calculation will then run again and the previous Batch calculation scores should be ignored. Choose this selection when Relevance scores for existing loads can be recalculated, for example, when review of existing file loads has not started.</span></span>
    
    <span data-ttu-id="1b341-p123">**분할 부하**를 선택 하는 경우 새 부하에 대해서만 관련성 교육을 진행 합니다. 이 인스턴스에서 이전 일괄 계산 점수는 그대로 유지 됩니다. 기존 부하에 대 한 기존 관련 성적 점수를 이미 시작한 경우에는이 옵션을 선택 합니다. 관련성 점수는이 시점 이상에서 별도로 관리 되며 병합할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="1b341-p123">If you select **Split loads**, continue Relevance training only on the new load. In this instance, previous Batch calculation scores will remain as is. Choose this option when existing Relevance scores for existing loads cannot be recalculated, for example, if review of existing loads has already started. Relevance scores are managed separately from this point onward and cannot be merged.</span></span>
    
3. <span data-ttu-id="1b341-192">**교육 계속**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b341-192">Click **Continue training**.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1b341-193">참고 항목</span><span class="sxs-lookup"><span data-stu-id="1b341-193">See also</span></span>

[<span data-ttu-id="1b341-194">Office 365 Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="1b341-194">Office 365 Advanced eDiscovery</span></span>](office-365-advanced-ediscovery.md)
  
[<span data-ttu-id="1b341-195">문제 정의 및 사용자 할당</span><span class="sxs-lookup"><span data-stu-id="1b341-195">Defining issues and assigning users</span></span>](define-issues-and-assign-users.md)
  
[<span data-ttu-id="1b341-196">강조 표시된 키워드 및 고급 옵션 정의</span><span class="sxs-lookup"><span data-stu-id="1b341-196">Defining highlighted keywords and advanced options</span></span>](define-highlighted-keywords-and-advanced-options.md)

