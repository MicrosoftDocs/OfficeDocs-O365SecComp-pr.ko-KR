---
title: Office 365 Advanced eDiscovery에서 프로세스 모듈 실행 및 데이터 로드
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
ms.assetid: c87bb0e5-301c-4d1d-958e-aabeb7990f44
description: 'Office 365 보안 &amp; 및 준수 센터를 사용 하 여 Office 365 Advanced eDiscovery에 액세스 하 고 서비스 케이스에 대해 프로세스 모듈을 실행 하는 방법에 대해 알아봅니다.  '
ms.openlocfilehash: 89a4be9bf56f35d9d9cbd88494bcae5a5a10fe7a
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/17/2019
ms.locfileid: "34157020"
---
# <a name="run-the-process-module-and-load-data-in-office-365-advanced-ediscovery"></a><span data-ttu-id="ee1b4-103">Office 365 Advanced eDiscovery에서 프로세스 모듈 실행 및 데이터 로드</span><span class="sxs-lookup"><span data-stu-id="ee1b4-103">Run the Process module and load data in Office 365 Advanced eDiscovery</span></span>

> [!NOTE]
> <span data-ttu-id="ee1b4-p101">Advanced eDiscovery를 사용하려면 Office 365 E3의 고급 준수 추가 기능이나 조직을 위한 E5 구독이 필요합니다. 이 요금제가 없는 상태에서 Advanced eDiscovery를 사용하려는 경우에는 [Office 365 Enterprise E5 평가판을 등록](https://go.microsoft.com/fwlink/p/?LinkID=698279)할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ee1b4-p101">Advanced eDiscovery requires an Office 365 E3 with the Advanced Compliance add-on or an E5 subscription for your organization. If you don't have that plan and want to try Advanced eDiscovery, you can [sign up for a trial of Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span></span> 
  
<span data-ttu-id="ee1b4-106">이 섹션에서는 고급 eDiscovery 프로세스 모듈의 기능에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="ee1b4-106">This section describes the functionality of the Advanced eDiscovery Process module.</span></span> 
  
<span data-ttu-id="ee1b4-107">파일 데이터 외에도 파일 형식, 확장명, 위치 또는 경로, 만든 날짜 및 시간, 만든이, custodian, 제목 등의 메타 데이터가 고급 eDiscovery로 로드 되 고 각 사례에 대해 저장 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ee1b4-107">In addition to file data, metadata such as file type, extension, location or path, creation date and time, author, custodian, and subject, can be loaded into Advanced eDiscovery and saved for each case.</span></span> <span data-ttu-id="ee1b4-108">일부 메타 데이터는 고급 eDiscovery (예: 네이티브 파일을 로드할 때)에서 계산 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ee1b4-108">Some metadata is calculated by Advanced eDiscovery, for example, when native files are loaded.</span></span> 
  
<span data-ttu-id="ee1b4-109">Advanced eDiscovery는 거의 중복 된 그룹 또는 관련성 점수와 같은 시스템 메타 데이터 값을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="ee1b4-109">Advanced eDiscovery provides system metadata values, such as Near-duplicate groupings or Relevance scores.</span></span> <span data-ttu-id="ee1b4-110">파일 주석과 같은 다른 메타 데이터는 관리자가 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ee1b4-110">Other metadata, such as file annotations, can be added by the Administrator.</span></span> 
  
## <a name="running-process"></a><span data-ttu-id="ee1b4-111">실행 중인 프로세스</span><span class="sxs-lookup"><span data-stu-id="ee1b4-111">Running Process</span></span>

> [!NOTE]
> <span data-ttu-id="ee1b4-112">파일 추적을 허용 하기 위해 프로세스 중에 파일에 일괄 처리 번호가 할당 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ee1b4-112">Batch numbers are assigned to a file during Process to allow the tracking of files.</span></span> <span data-ttu-id="ee1b4-113">일괄 처리 번호를 사용 하 여 처리 옵션에 대해 프로세스 일괄 처리를 식별할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ee1b4-113">The batch number also enables identification of Process batches for reprocessing options.</span></span> <span data-ttu-id="ee1b4-114">일괄 처리 번호 및 세션을 기준으로 필터링 하는 데 사용할 수 있는 추가 필터가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ee1b4-114">Additional filters are available for filtering by batch number and sessions.</span></span> 
  
<span data-ttu-id="ee1b4-115">다음 단계를 수행 하 여 프로세스를 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="ee1b4-115">Perform the following steps to run Process.</span></span>
  
1. <span data-ttu-id="ee1b4-116">[Office 365 보안 &amp; 및 준수 센터를 엽니다](go-to-the-securitycompliance-center.md) .</span><span class="sxs-lookup"><span data-stu-id="ee1b4-116">[Open the Office 365 Security &amp; Compliance Center](go-to-the-securitycompliance-center.md) .</span></span> 
    
2. <span data-ttu-id="ee1b4-117">\*\* &amp; 검색 조사\*\* \> **eDiscovery** 로 이동한 후 **Advanced eDiscovery로 이동을**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="ee1b4-117">Go to **Search &amp; investigation** \> **eDiscovery** and then click **Go to Advanced eDiscovery**.</span></span>
    
3. <span data-ttu-id="ee1b4-118">고급 eDiscovery의 경우 표시 되는 **사례** 페이지에서 적절 한 사례를 선택 하 고 **대/소문자로 이동을**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="ee1b4-118">In Advanced eDiscovery, select the appropriate case in the displayed **Cases** page and click **Go to case**.</span></span>
    
4. <span data-ttu-id="ee1b4-119">\> **프로세스** \*\*\*\* \> 준비 **설정**의 사용 가능한 컨테이너 목록에서 컨테이너를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="ee1b4-119">In **Prepare** \> **Process** \> **Setup**, select a container from the list of available containers.</span></span>
    
    ![프로세스를 클릭 하 여 검색 결과를 사례에 추가 합니다.](media/50bdc55c-d378-4881-b302-31ef785fa359.png)
  
5. <span data-ttu-id="ee1b4-121">컨테이너를 시드 파일 또는 미리 태그가 지정 된 파일로 추가 하려면 **고급 설정 ...** 을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="ee1b4-121">Click **Advanced settings...** if you want to add the container as seed files or as pre-tagged files.</span></span> 
    
    <span data-ttu-id="ee1b4-122">시드 파일을 사용 하 여 낮은 다양성 (대개 2% 이하의 값)으로 문제에 대 한 교육을 가속화할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ee1b4-122">Use seed files to accelerate training for issues with low richness (usually 2%, or less).</span></span> <span data-ttu-id="ee1b4-123">시드 파일의 경우에는 명확 하지 않은 관련 파일을 여러 개 선택 하 고 문제와 관련 된 약 20-50 시드 프로세스를 처리 하는 것이 좋습니다 (시드 파일이 너무 많아 관련성 결과를 기울일 수 있음).</span><span class="sxs-lookup"><span data-stu-id="ee1b4-123">For seed files, it is recommended that you select a variety of distinctly relevant files and process about 20-50 seeds per issue (too many seed files can skew Relevance results).</span></span> <span data-ttu-id="ee1b4-124">시드 파일은 문제를 훈련 받을 사용자가 검토 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ee1b4-124">Seed files should be reviewed by the same person who will train the issue.</span></span>
    
    <span data-ttu-id="ee1b4-125">미리 태그가 지정 된 파일을 사용 하 여 관련성 있는 교육을 자동화 합니다.</span><span class="sxs-lookup"><span data-stu-id="ee1b4-125">Use pre-tagged files to automate Relevance training.</span></span> <span data-ttu-id="ee1b4-126">적어도 1500 개 파일에 태그를 추가 하 고 관련성이 높은 파일에 대 한 관련성을 관련에 추가한 컬렉션에서와 동일한 비율로 유지 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ee1b4-126">You should tag at least 1,500 files, and keep the proportion of relevant to non-relevant files the same as in the collection added to Relevance.</span></span> <span data-ttu-id="ee1b4-127">이러한 파일에는 수동으로 태그를 지정 해야 하며 태깅 품질이 확실 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ee1b4-127">These files should be manually tagged, and you should be confident in the quality of tagging.</span></span>
    
    ![배치 파일 처리에 대 한 고급 설정 페이지 스크린샷](media/3c25cb78-4484-41e5-bd34-3753c7ab6cf2.jpg)
  
  - <span data-ttu-id="ee1b4-129">**Seed** 섹션에서 다음을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="ee1b4-129">In the **Seed** section:</span></span> 
    
    <span data-ttu-id="ee1b4-130">**Seed 파일로 표시** 를 선택 하 여 컨테이너를 시드 파일로 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ee1b4-130">Choose **Mark as seed files** to mark the container as seed files.</span></span> <span data-ttu-id="ee1b4-131">또한 **문제점** 드롭다운을 통해 문제점 당 해당 사용자를 할당 하도록 선택 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ee1b4-131">You also need choose to assign them per issue from the **For issue** drop-down.</span></span> <span data-ttu-id="ee1b4-132">**태그** 드롭다운을 사용 하 여 **관련성** 또는 관련성을 선택 **하지 않습니다** .</span><span class="sxs-lookup"><span data-stu-id="ee1b4-132">Choose either **Relevant** or **Not relevant** from the **Tag** drop-down.</span></span> 
    
    > [!NOTE]
    > <span data-ttu-id="ee1b4-133">파일을 **시드로**설정한 후에는 **미리 태그가 지정**된 것으로 표시할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="ee1b4-133">Once you set files as **Seed**, you cannot mark them as **Pre-tagged**.</span></span> 
  
  - <span data-ttu-id="ee1b4-134">**미리 태그가 지정 된 파일** 섹션에서 다음을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="ee1b4-134">In the **Pre-tagged files** section:</span></span> 
    
    <span data-ttu-id="ee1b4-135">컨테이너를 미리 태그가 지정 된 파일로 표시 하려면 **미리 태그 지정 파일로 표시** 를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="ee1b4-135">Choose **Mark as pre-tagged files** to mark the container as pre-tagged files.</span></span> <span data-ttu-id="ee1b4-136">또한 **문제 해결을 위해** 문제점 당 각 문제를 할당 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ee1b4-136">You also need to assign them per issue from the **For issue** drop-down.</span></span> <span data-ttu-id="ee1b4-137">**태그** 드롭다운을 사용 하 여 **관련성** 또는 관련성을 선택 **하지 않습니다** .</span><span class="sxs-lookup"><span data-stu-id="ee1b4-137">Choose either **Relevant** or **Not relevant** from the **Tag** drop-down.</span></span> 
    
    > [!NOTE]
    > <span data-ttu-id="ee1b4-138">파일을 **미리 태그가 지정**된 것으로 설정 하는 경우에는 해당 항목을 **시드로**표시할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="ee1b4-138">Once you set files as **Pre-tagged**, you cannot mark them as **Seed**.</span></span> 
  
  - <span data-ttu-id="ee1b4-139">**전자 메일 태그** 지정 섹션</span><span class="sxs-lookup"><span data-stu-id="ee1b4-139">In the **Email tagging** section.</span></span> <span data-ttu-id="ee1b4-140">전송 되는 전자 메일 중 시드 또는 미리 태그가 지정 된 부분을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ee1b4-140">set which part of a processed email are to be marked as Seed or Pre-tagged.</span></span> 
    
6. <span data-ttu-id="ee1b4-141">시작 하려면 **프로세스**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="ee1b4-141">To begin, click **Process**.</span></span> <span data-ttu-id="ee1b4-142">완료 되 면 프로세스 결과가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ee1b4-142">When completed, the Process results are displayed.</span></span>
    
7. <span data-ttu-id="ee1b4-143">반드시 특정 custodian에 데이터 원본을 할당 해야 하는 경우에 \*\*\*\* \> \*\*\*\* 는 **Custodians** \> 에서 custodian를 **관리** 하 고 Custodians을 할당할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="ee1b4-143">(Optional) If you need to assign data sources to a specific custodian, you can add and edit custodian names in **Custodians** \> **Manage** and assign custodians in **Custodians** \> **Assign**.</span></span> 
    
<span data-ttu-id="ee1b4-144">사례에 추가 하는 경우 다시 처리할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ee1b4-144">If you add to the case, then you can process again.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="ee1b4-145">참고 항목</span><span class="sxs-lookup"><span data-stu-id="ee1b4-145">See also</span></span>

[<span data-ttu-id="ee1b4-146">Office 365 Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="ee1b4-146">Office 365 Advanced eDiscovery</span></span>](office-365-advanced-ediscovery.md)
  
[<span data-ttu-id="ee1b4-147">프로세스 모듈 결과 보기</span><span class="sxs-lookup"><span data-stu-id="ee1b4-147">Viewing Process module results</span></span>](view-process-module-results-in-advanced-ediscovery.md)

