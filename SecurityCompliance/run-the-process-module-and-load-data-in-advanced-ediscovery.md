---
title: Office 365 Advanced eDiscovery 프로세스 모듈 실행 및 데이터 로드
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
ms.assetid: c87bb0e5-301c-4d1d-958e-aabeb7990f44
description: 'Office 365 보안을 사용 하는 방법에 알아봅니다 &amp; 준수 센터 Office 365 고급 eDiscovery를 액세스 하는 경우에 대 한 프로세스 모듈을 실행 합니다.  '
ms.openlocfilehash: 32052bccc37d20c8707a1efb0592f7c93daf3590
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22533509"
---
# <a name="run-the-process-module-and-load-data-in-office-365-advanced-ediscovery"></a><span data-ttu-id="7018a-103">Office 365 Advanced eDiscovery 프로세스 모듈 실행 및 데이터 로드</span><span class="sxs-lookup"><span data-stu-id="7018a-103">Run the Process module and load data in Office 365 Advanced eDiscovery</span></span>

> [!NOTE]
> <span data-ttu-id="7018a-p101">고급 eDiscovery 조직에 대 한 고급 준수 추가 기능 또는 e 5 구독은 Office 365 E3 필요합니다. 해당 요금제에 가입한 상태 고급 eDiscovery 시도 하려는 하지 경우에 [Office 365 Enterprise e 5의 평가판 등록](https://go.microsoft.com/fwlink/p/?LinkID=698279)할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7018a-p101">Advanced eDiscovery requires an Office 365 E3 with the Advanced Compliance add-on or an E5 subscription for your organization. If you don't have that plan and want to try Advanced eDiscovery, you can [sign up for a trial of Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span></span> 
  
<span data-ttu-id="7018a-106">이 섹션에서는 고급 eDiscovery 프로세스 모듈의 기능에 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="7018a-106">This section describes the functionality of the Advanced eDiscovery Process module.</span></span> 
  
<span data-ttu-id="7018a-p102">파일 데이터 외에도 각 사례에 대 한 저장 및 eDiscovery 고급에 파일 형식, 확장, 위치 또는 경로, 만든 날짜 및 시간, 작성자, 더불어, 및 제목, 등의 메타 데이터를 로드 수 있습니다. 기본 파일을 로드 하는지 일부 메타 데이터가 등 고급 eDiscovery 하 여 계산 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7018a-p102">In addition to file data, metadata such as file type, extension, location or path, creation date and time, author, custodian, and subject, can be loaded into Advanced eDiscovery and saved for each case. Some metadata is calculated by Advanced eDiscovery, for example, when native files are loaded.</span></span> 
  
<span data-ttu-id="7018a-p103">고급 eDiscovery 시스템 거의 중복 된 그룹화 또는 관련성 점수와 같은 메타 데이터 값을 제공합니다. 관리자가 파일 주석 등의 다른 메타 데이터를 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7018a-p103">Advanced eDiscovery provides system metadata values, such as Near-duplicate groupings or Relevance scores. Other metadata, such as file annotations, can be added by the Administrator.</span></span> 
  
## <a name="running-process"></a><span data-ttu-id="7018a-111">실행 중인 프로세스</span><span class="sxs-lookup"><span data-stu-id="7018a-111">Running Process</span></span>

> [!NOTE]
> <span data-ttu-id="7018a-p104">일괄 처리 번호는 파일의 추적할 수 있도록 프로세스 중 파일에 할당 됩니다. 일괄 처리 수에는 재처리 옵션에 대 한 프로세스 일괄 처리를 식별할 수 있습니다. 일괄 처리 번호와 세션으로 필터링에 대 한 추가 필터를 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7018a-p104">Batch numbers are assigned to a file during Process to allow the tracking of files. The batch number also enables identification of Process batches for reprocessing options. Additional filters are available for filtering by batch number and sessions.</span></span> 
  
<span data-ttu-id="7018a-115">프로세스를 실행 하려면 다음 단계를 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="7018a-115">Perform the following steps to run Process.</span></span>
  
1. <span data-ttu-id="7018a-116">[Office 365 보안 열고 &amp; 준수 센터](go-to-the-securitycompliance-center.md) 합니다.</span><span class="sxs-lookup"><span data-stu-id="7018a-116">[Open the Office 365 Security &amp; Compliance Center](go-to-the-securitycompliance-center.md) .</span></span> 
    
2. <span data-ttu-id="7018a-117">이동 **검색 &amp; 조사** \> **eDiscovery** 를 누른 다음 **고급 eDiscovery로 이동**합니다.</span><span class="sxs-lookup"><span data-stu-id="7018a-117">Go to **Search &amp; investigation** \> **eDiscovery** and then click **Go to Advanced eDiscovery**.</span></span>
    
3. <span data-ttu-id="7018a-118">고급 eDiscovery에 표시 된 **경우** 페이지에서 적절 한 대/소문자를 선택 하 고 **대/소문자로 이동**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="7018a-118">In Advanced eDiscovery, select the appropriate case in the displayed **Cases** page and click **Go to case**.</span></span>
    
4. <span data-ttu-id="7018a-119">**Prepare** 에 \> **프로세스** \> **설치 프로그램**을 사용할 수 있는 컨테이너의 목록에서 컨테이너를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="7018a-119">In **Prepare** \> **Process** \> **Setup**, select a container from the list of available containers.</span></span>
    
    ![대/소문자를 검색 결과 추가 하는 프로세스를 클릭 합니다.](media/50bdc55c-d378-4881-b302-31ef785fa359.png)
  
5. <span data-ttu-id="7018a-121">시드 파일 또는 미리 태그가 지정 된 파일로 컨테이너를 추가 하려는 경우에 **고급 설정...** 을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="7018a-121">Click **Advanced settings...** if you want to add the container as seed files or as pre-tagged files.</span></span> 
    
    <span data-ttu-id="7018a-p105">시드 파일을 사용 하 여 낮은 다양성와 문제에 대 한 교육을 신속 하 (일반적으로 2% 이하의). 시드 파일에 대 한 것이 좋습니다 다양 한 명확 하 게 관련 파일을 선택 하 고 처리에 대 한 문제 (너무 많은 시드 파일 관련성 결과 skew 수) 당 20 ~ 50 시드 합니다. 동일한 통화를 사용자가 문제를 교육 할지 시드 파일을 검토 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="7018a-p105">Use seed files to accelerate training for issues with low richness (usually 2%, or less). For seed files, it is recommended that you select a variety of distinctly relevant files and process about 20-50 seeds per issue (too many seed files can skew Relevance results). Seed files should be reviewed by the same person who will train the issue.</span></span>
    
    <span data-ttu-id="7018a-p106">관련성 교육을 자동화 하려면 미리 태그가 지정 된 파일을 사용 합니다. 최소한 1, 500 파일 태그를 지정 하 고 관련성에 추가 된 모음과 동일 하 게 관련 아닌 파일에 관련 된 비율을 유지 해야 합니다. 이러한 파일을 수동으로 태그를 지정, 하 고 태그의 품질에 판단 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="7018a-p106">Use pre-tagged files to automate Relevance training. You should tag at least 1,500 files, and keep the proportion of relevant to non-relevant files the same as in the collection added to Relevance. These files should be manually tagged, and you should be confident in the quality of tagging.</span></span>
    
    ![배치 파일을 처리 하기 위한 스크린샷의 고급 설정 페이지](media/3c25cb78-4484-41e5-bd34-3753c7ab6cf2.jpg)
  
  - <span data-ttu-id="7018a-129">**시드** 섹션:</span><span class="sxs-lookup"><span data-stu-id="7018a-129">In the **Seed** section:</span></span> 
    
    <span data-ttu-id="7018a-p107">**시드 파일로 표시** 시드 파일로 컨테이너를 표시할지를 선택 합니다. **문제에 대 한** 드롭다운 목록에서 문제 당 할당 하도록 선택할 필요는 있습니다. **태그** 드롭다운 메뉴에서 **다음과 관련 됨** 또는 **관련이 없는** 중 하나를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="7018a-p107">Choose **Mark as seed files** to mark the container as seed files. You also need choose to assign them per issue from the **For issue** drop-down. Choose either **Relevant** or **Not relevant** from the **Tag** drop-down.</span></span> 
    
    > [!NOTE]
    > <span data-ttu-id="7018a-133">**시드**으로 파일을 설정한 후 **태그가 지정 된 사전**으로 표시할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="7018a-133">Once you set files as **Seed**, you cannot mark them as **Pre-tagged**.</span></span> 
  
  - <span data-ttu-id="7018a-134">섹션에서 다음 **미리 태그가 지정 된 파일** .</span><span class="sxs-lookup"><span data-stu-id="7018a-134">In the **Pre-tagged files** section:</span></span> 
    
    <span data-ttu-id="7018a-p108">**미리 태그가 지정 된 파일로 표시** 미리 태그가 지정 된 파일로 컨테이너를 표시할지를 선택 합니다. **문제에 대 한** 드롭다운 목록에서 문제 당 할당 해야하는 합니다. **태그** 드롭다운 메뉴에서 **다음과 관련 됨** 또는 **관련이 없는** 중 하나를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="7018a-p108">Choose **Mark as pre-tagged files** to mark the container as pre-tagged files. You also need to assign them per issue from the **For issue** drop-down. Choose either **Relevant** or **Not relevant** from the **Tag** drop-down.</span></span> 
    
    > [!NOTE]
    > <span data-ttu-id="7018a-138">**태그가 지정 된 사전**으로 파일을 설정한 후 **시드**으로 표시할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="7018a-138">Once you set files as **Pre-tagged**, you cannot mark them as **Seed**.</span></span> 
  
  - <span data-ttu-id="7018a-p109">**전자 메일에 태그 지정** 섹션입니다. 시드 또는 태그가 지정 된 사전으로 표시할지는 처리 된 전자 메일의 부분 집합입니다.</span><span class="sxs-lookup"><span data-stu-id="7018a-p109">In the **Email tagging** section. set which part of a processed email are to be marked as Seed or Pre-tagged.</span></span> 
    
6. <span data-ttu-id="7018a-p110">먼저, **프로세스**를 클릭 합니다. 완료 되 면 프로세스 결과가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7018a-p110">To begin, click **Process**. When completed, the Process results are displayed.</span></span>
    
7. <span data-ttu-id="7018a-143">(선택 사항) 추가 하 고 **Custodians** 에 더불어 이름을 편집할 수 특정 더불어를 데이터 원본에 할당 해야하는 경우 \> **Custodians** 에서 **관리** 하 고 할당 custodians \> **할당**합니다.</span><span class="sxs-lookup"><span data-stu-id="7018a-143">(Optional) If you need to assign data sources to a specific custodian, you can add and edit custodian names in **Custodians** \> **Manage** and assign custodians in **Custodians** \> **Assign**.</span></span> 
    
<span data-ttu-id="7018a-144">대/소문자를 추가 하는 경우을 처리할 수 있습니다 다시 합니다.</span><span class="sxs-lookup"><span data-stu-id="7018a-144">If you add to the case, then you can process again.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="7018a-145">참고 항목</span><span class="sxs-lookup"><span data-stu-id="7018a-145">See also</span></span>

[<span data-ttu-id="7018a-146">Office 365 Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="7018a-146">Office 365 Advanced eDiscovery</span></span>](office-365-advanced-ediscovery.md)
  
[<span data-ttu-id="7018a-147">프로세스 모듈 결과 보기</span><span class="sxs-lookup"><span data-stu-id="7018a-147">Viewing Process module results</span></span>](view-process-module-results-in-advanced-ediscovery.md)

