---
title: Office 365 Advanced eDiscovery에서 분석 옵션 설정
ms.author: chrfox
author: chrfox
manager: laurawi
ms.date: 9/14/2017
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: f6cd6588-f6b6-424a-a9ab-3782b842faee
description: '유사 복제, 전자 메일 스레드 및 테마를 포함 하 여 Office 365 Advanced eDiscovery의 분석 프로세스에 대 한 옵션을 설정 하는 단계를 검토 합니다.  '
ms.openlocfilehash: 6d853d701613fcbe61c6e98b3bf55ae99eefd901
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/17/2019
ms.locfileid: "34156670"
---
# <a name="set-analyze-options-in-office-365-advanced-ediscovery"></a><span data-ttu-id="fad9f-103">Office 365 Advanced eDiscovery에서 분석 옵션 설정</span><span class="sxs-lookup"><span data-stu-id="fad9f-103">Set Analyze options in Office 365 Advanced eDiscovery</span></span>

> [!NOTE]
> <span data-ttu-id="fad9f-p101">Advanced eDiscovery를 사용하려면 Office 365 E3의 고급 준수 추가 기능이나 조직을 위한 E5 구독이 필요합니다. 이 요금제가 없는 상태에서 Advanced eDiscovery를 사용하려는 경우에는 [Office 365 Enterprise E5 평가판을 등록](https://go.microsoft.com/fwlink/p/?LinkID=698279)할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fad9f-p101">Advanced eDiscovery requires an Office 365 E3 with the Advanced Compliance add-on or an E5 subscription for your organization. If you don't have that plan and want to try Advanced eDiscovery, you can [sign up for a trial of Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span></span> 
  
<span data-ttu-id="fad9f-106">고급 eDiscovery에서 분석을 실행 하기 전에 분석 옵션을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fad9f-106">In Advanced eDiscovery, set the Analyze options prior to running Analyze.</span></span>
  
## <a name="set-analyze-options"></a><span data-ttu-id="fad9f-107">분석 옵션 설정</span><span class="sxs-lookup"><span data-stu-id="fad9f-107">Set Analyze options</span></span>

<span data-ttu-id="fad9f-108">\*\* \> 준비 분석\*\* \> **설정을**엽니다.</span><span class="sxs-lookup"><span data-stu-id="fad9f-108">Open **Prepare \> Analyze** \> **Setup**.</span></span> <span data-ttu-id="fad9f-109">다음 창이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="fad9f-109">The following window is displayed.</span></span>
  
![세트 옵션 분석](media/c3ec7a92-8484-4812-b98c-aa3eb740e5b7.png)
  
 <span data-ttu-id="fad9f-111">**유사-중복 및 전자 메일 스레드** 분석을 실행 하려면이 확인란을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="fad9f-111">**Near-duplicates and email threads** Check this box if you want to run the analysis.</span></span> <span data-ttu-id="fad9f-112">이 옵션은 기본적으로 선택되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fad9f-112">It is selected by default.</span></span> 
  
 <span data-ttu-id="fad9f-113">**문서 유사성** 거의 모든 부분 복제 임계값을 입력 하거나 기본값인 65%를 그대로 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="fad9f-113">**Document similarity** Enter the Near-duplicates threshold value or accept the default of 65%.</span></span> 
  
 <span data-ttu-id="fad9f-114">**테마** 모든 파일을 처리 하 고 테마를 할당 하려면이 확인란을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="fad9f-114">**Themes**Check this box to process all files and assign themes to them.</span></span> <span data-ttu-id="fad9f-115">이 확인란은 기본적으로 선택 되어 있지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fad9f-115">By default, this check box is not selected.</span></span> <span data-ttu-id="fad9f-116">테마 처리를 수행 하려면 다음 옵션을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="fad9f-116">Enter the following options if you want to perform Themes processing.</span></span>
  
- <span data-ttu-id="fad9f-117">**최대 테마 수** 만들 테마 수 값을 입력 하거나 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="fad9f-117">**Max number of themes**Enter or select a value for the number of themes to create.</span></span> <span data-ttu-id="fad9f-118">기본값은 200입니다.</span><span class="sxs-lookup"><span data-stu-id="fad9f-118">The default is 200.</span></span> 
    
    > [!NOTE]
    > <span data-ttu-id="fad9f-119">테마 수를 늘리면 성능에 영향을 미치며 테마를 일반화할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fad9f-119">Increasing the number of themes affects performance, as well as the ability of a theme to generalize.</span></span> <span data-ttu-id="fad9f-120">테마 수가 높을수록 더 세밀 하 게 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="fad9f-120">The higher the number of themes, the more granular they are.</span></span> <span data-ttu-id="fad9f-121">예를 들어 50 테마 집합에 "농구, Spurs, Clippers, Lakers"와 같은 테마가 포함 된 경우 300 테마에는 별도의 테마 ("Spurs", "Clippers", "Lakers")가 포함 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fad9f-121">For example, if a set of 50 themes include a theme such as "Basketball, Spurs, Clippers, Lakers"; 300 themes may include separate themes: "Spurs", "Clippers", "Lakers".</span></span> <span data-ttu-id="fad9f-122">"농구" 테마에 대 한 인식이 없고 ECA에 대해이 기능을 사용 하는 경우 "농구" 라는 테마를 표시 하는 것이 유용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fad9f-122">If you had no awareness of the theme "Basketball" and use this feature for ECA, seeing the theme "Basketball" could be useful.</span></span> <span data-ttu-id="fad9f-123">그러나 처리에 너무 많은 테마가 포함 되어 있는 경우에는 "농구" 라는 단어가 표시 되지 않으며 Spurs 및 Clippers는 시작 하는 데 사용 되는 항목을 나타내는 것이 아니라 더 나은 농구 테마 인지 알 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="fad9f-123">But, if the processing had too many themes, you may never see the word "Basketball" and may not know that Spurs and Clippers are good Basketball themes to review, rather than items that go on boots and used for hair.</span></span> 
  
- <span data-ttu-id="fad9f-124">**추천 테마** 테마 처리를 제어 하는 theme 단어를 제안할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fad9f-124">**Suggested themes** You can suggest theme words to control Themes processing.</span></span> <span data-ttu-id="fad9f-125">고급 eDiscovery는 이러한 추천 단어에 집중 하 고 "최대 테마 수" 설정에 따라 하나 이상의 관련 테마를 만들려고 시도 합니다.</span><span class="sxs-lookup"><span data-stu-id="fad9f-125">Advanced eDiscovery will focus on these suggested words and try to create one or more relevant themes, based on the "Max number of themes" settings.</span></span> 
    
    <span data-ttu-id="fad9f-126">예를 들어 추천 단어가 "computer"이 고 "2"를 "최대 테마 수"로 지정한 경우 Advanced eDiscovery에서는 "computer" 라는 단어와 관련 된 두 테마를 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="fad9f-126">For example, if the suggested word is "computer", and you specified "2" as the "Max number of Themes", Advanced eDiscovery will try to generate two themes that relate to the word "computer".</span></span> <span data-ttu-id="fad9f-127">"컴퓨터 소프트웨어" 및 "컴퓨터 하드웨어"와 같은 두 가지 테마를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fad9f-127">The two themes might be "computer software" and "computer hardware", for example.</span></span> 
    
    ![추천된 테마 추가](media/06e9ffd3-a76c-423b-b450-9e465eb9a02f.png)
  
1. <span data-ttu-id="fad9f-129">제안 된 테마를 보거나 추가 하거나 편집 하려면 **수정을**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="fad9f-129">To view, add, or edit suggested themes, click **Modify**.</span></span>
    
2. <span data-ttu-id="fad9f-130">제안 된 **테마** 패널에서 추가 아이콘 \*\*\*\* ![](media/c2dd8b3a-5a22-412c-a7fa-143f5b2b5612.png) 추가 아이콘를 클릭 하 여 테마를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="fad9f-130">In the **Suggested themes** panel, click the **Add** ![add icon](media/c2dd8b3a-5a22-412c-a7fa-143f5b2b5612.png) icon to add a theme.</span></span> <span data-ttu-id="fad9f-131">**제안 테마 추가** 패널에서 단어를 쉼표로 구분 하 여 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="fad9f-131">In the **Add suggested theme** panel, add the words, separated by commas.</span></span> 
    
3. <span data-ttu-id="fad9f-132">**테마 수**에 따라 고급 eDiscovery에서 해당 단어에 대해 생성을 시도할 테마 수를 결정 하는 값 (기본값은 1 테마)을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="fad9f-132">In **Number of themes**, select a value to determine the number of themes Advanced eDiscovery will try to generate for these words (default is 1 theme).</span></span>
    
4. <span data-ttu-id="fad9f-133">**저장** 을 클릭 하 고 대화 상자를 닫습니다.</span><span class="sxs-lookup"><span data-stu-id="fad9f-133">Click **Save** and then close the dialogue.</span></span> 
    
    > [!NOTE]
    > <span data-ttu-id="fad9f-134">테마의 총 수에 추천 테마가 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fad9f-134">The total number of themes includes Suggested Themes.</span></span> <span data-ttu-id="fad9f-135">제안 된 총 테마는 총 테마를 초과할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="fad9f-135">The total Suggested Themes cannot exceed the total themes.</span></span> <span data-ttu-id="fad9f-136">전체 테마에 대 한 추천 테마가 여러 개 있는 경우 대부분의 테마가 추천 테마에 전용으로 제공 되므로 일부 "novel" 테마만 시스템에서 검색 됩니다.</span><span class="sxs-lookup"><span data-stu-id="fad9f-136">If there are many Suggested Themes relative to the total themes, only a few "novel" themes will be detected by the system because most of the themes will be dedicated to Suggested Themes.</span></span> 
  
- <span data-ttu-id="fad9f-137">**모드** 드롭다운 목록에서 **테마** 옵션을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="fad9f-137">**Mode** From the drop-down list, select a **Themes** option:</span></span> 
    
  - <span data-ttu-id="fad9f-138">**모델 만들기 및 적용**: 파일 세그먼트에서 모델 별로 테마를 계산 하 여 파일 간에 배포 합니다.</span><span class="sxs-lookup"><span data-stu-id="fad9f-138">**Create and apply model**: Calculates themes by models from a segment of the files and then distributes files among them.</span></span>
    
  - <span data-ttu-id="fad9f-139">**모델 만들기**: 파일의 세그먼트에서 테마 모델을 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="fad9f-139">**Create model**: Calculates a themes model from a segment of the files.</span></span> <span data-ttu-id="fad9f-140">파일을 나눌 때의 적용 프로세스는 별도로 수행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="fad9f-140">The Apply process of dividing files is done separately at another time.</span></span>
    
  - <span data-ttu-id="fad9f-141">**모델 적용**:이 옵션은 모델을 이전에 만들었지만 아직 적용 하지 않은 경우에만 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="fad9f-141">**Apply model**: This option is only shown if a model was created previously and not yet applied.</span></span> <span data-ttu-id="fad9f-142">이렇게 하면 테마에 따라 파일이 구분 됩니다.</span><span class="sxs-lookup"><span data-stu-id="fad9f-142">This will divide the files based on the themes.</span></span>
    
<span data-ttu-id="fad9f-143">또한 [ignore 텍스트를 설정](set-ignore-text-in-advanced-ediscovery.md) 하 고 분석할 [고급 설정 분석](set-analyze-advanced-settings-in-advanced-ediscovery.md) 을 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fad9f-143">You can also [set ignore text](set-ignore-text-in-advanced-ediscovery.md) and [set Analyze advanced settings](set-analyze-advanced-settings-in-advanced-ediscovery.md) for Analyze.</span></span> 
  
<span data-ttu-id="fad9f-144">이러한 옵션을 설정한 후에는 **분석** 을 클릭 하 여 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="fad9f-144">After you've set these options, click **Analyze** to run.</span></span> <span data-ttu-id="fad9f-145">[보기 분석 결과](view-analyze-results-in-advanced-ediscovery.md) 를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="fad9f-145">[View Analyze results](view-analyze-results-in-advanced-ediscovery.md) are displayed.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="fad9f-146">참고 항목</span><span class="sxs-lookup"><span data-stu-id="fad9f-146">See also</span></span>

[<span data-ttu-id="fad9f-147">Office 365 Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="fad9f-147">Office 365 Advanced eDiscovery</span></span>](office-365-advanced-ediscovery.md)
  
[<span data-ttu-id="fad9f-148">문서 유사성 이해</span><span class="sxs-lookup"><span data-stu-id="fad9f-148">Understanding document similarity</span></span>](understand-document-similarity-in-advanced-ediscovery.md)
  
[<span data-ttu-id="fad9f-149">무시 텍스트 설정</span><span class="sxs-lookup"><span data-stu-id="fad9f-149">Set Ignore text </span></span>](set-ignore-text-in-advanced-ediscovery.md)
  
[<span data-ttu-id="fad9f-150">고급 설정 설정 분석</span><span class="sxs-lookup"><span data-stu-id="fad9f-150">Set Analyze advanced settings</span></span>](set-analyze-advanced-settings-in-advanced-ediscovery.md)
  
[<span data-ttu-id="fad9f-151">결과 분석 보기</span><span class="sxs-lookup"><span data-stu-id="fad9f-151">View Analyze results</span></span>](view-analyze-results-in-advanced-ediscovery.md)

