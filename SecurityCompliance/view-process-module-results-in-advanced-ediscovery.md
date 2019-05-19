---
title: Office 365 Advanced eDiscovery의 프로세스 모듈 결과 보기
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
ms.assetid: c6f016cb-409f-4ae9-911c-1395cf0c86ea
description: '작업 상태 및 프로세스 요약을 포함 하 여 Office 365 Advanced eDiscovery에서 실행 되는 프로세스 모듈의 결과를 찾는 방법에 대해 알아봅니다.  '
ms.openlocfilehash: 4bbdbf68f71e3459ff2ddcd8ba3fb33e52f16825
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/17/2019
ms.locfileid: "34157800"
---
# <a name="view-process-module-results-in-office-365-advanced-ediscovery"></a><span data-ttu-id="28c3a-103">Office 365 Advanced eDiscovery의 프로세스 모듈 결과 보기</span><span class="sxs-lookup"><span data-stu-id="28c3a-103">View Process module results in Office 365 Advanced eDiscovery</span></span>

<span data-ttu-id="28c3a-104">**준비** \> **프로세스가** 시작 되 면 진행률과 결과를 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="28c3a-104">After **Prepare** \> **Process** is initiated, you can view progress and results.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="28c3a-p101">Advanced eDiscovery를 사용하려면 Office 365 E3의 고급 준수 추가 기능이나 조직을 위한 E5 구독이 필요합니다. 이 요금제가 없는 상태에서 Advanced eDiscovery를 사용하려는 경우에는 [Office 365 Enterprise E5 평가판을 등록](https://go.microsoft.com/fwlink/p/?LinkID=698279)할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="28c3a-p101">Advanced eDiscovery requires an Office 365 E3 with the Advanced Compliance add-on or an E5 subscription for your organization. If you don't have that plan and want to try Advanced eDiscovery, you can [sign up for a trial of Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span></span> 
  
## <a name="process-task-status"></a><span data-ttu-id="28c3a-107">프로세스 작업 상태</span><span class="sxs-lookup"><span data-stu-id="28c3a-107">Process task status</span></span>

<span data-ttu-id="28c3a-108">**준비** \> \*\*\*\* 프로세스 \> **결과**에서 페이지에는 현재 상태가 (프로세스가 현재 실행 중인 경우) 또는 다음 예제와 같이 마지막 프로세스 상태 작업 상태가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="28c3a-108">In **Prepare** \> **Process** \> **Results**, the page shows the current status (if Process is currently running) or the last Process status task status as shown in the following example.</span></span>
  
![프로세스 모듈 작업 상태](media/9430f9e7-a4dd-47c7-ac2e-2c6a60fc948b.png)
  
<span data-ttu-id="28c3a-110">선택한 프로세스 옵션에 따라 표시 되는 작업이 다를 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="28c3a-110">The displayed tasks may vary depending on the Process options selected.</span></span> 
  
- <span data-ttu-id="28c3a-111">**인벤토리**: 고급 eDiscovery 프로세스를 위해 선택한 모든 파일을 반복 하 고 기본 데이터 수집을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="28c3a-111">**Inventory**: Advanced eDiscovery iterates through all files selected for Process and performs basic data collection.</span></span>
    
- <span data-ttu-id="28c3a-112">**서명 계산**: MD5 디지털 서명을 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="28c3a-112">**Calculate signatures**: Calculates the MD5 digital signatures.</span></span>
    
- <span data-ttu-id="28c3a-113">**Compounds 추출**: 복합 파일 (예: PST, ZIP, MSG)에서 내부 또는 포함 된 파일을 재귀적으로 추출 합니다.</span><span class="sxs-lookup"><span data-stu-id="28c3a-113">**Compounds extraction**: Extracts inner or contained files recursively from compound files (for example, PST, ZIP, MSG).</span></span> <span data-ttu-id="28c3a-114">추출 된 파일은 사례의 사례 폴더에 저장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="28c3a-114">Extracted files are stored in the case folder of the case.</span></span>
    
- <span data-ttu-id="28c3a-115">**데이터베이스 동기화**: 내부 데이터베이스 프로세스</span><span class="sxs-lookup"><span data-stu-id="28c3a-115">**Synchronizing database**: Internal database process.</span></span>
    
- <span data-ttu-id="28c3a-116">**파일 복사**: 프로세스 파일을 복사 합니다.</span><span class="sxs-lookup"><span data-stu-id="28c3a-116">**File copy**: Copies Process files.</span></span> <span data-ttu-id="28c3a-117">이 작업은 파일 복사 고급 옵션을 선택한 경우에도 항상 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="28c3a-117">This task is always displayed, even when the advanced Copy files option is selected.</span></span>
    
- <span data-ttu-id="28c3a-118">**텍스트 추출**: 네이티브 파일이 있는 경우 Advanced EDiscovery는 dtsearch를 사용 하 여 이러한 파일에서 텍스트를 추출 합니다.</span><span class="sxs-lookup"><span data-stu-id="28c3a-118">**Text extraction**: When there are native files, Advanced eDiscovery extracts text from these files using DTSearch.</span></span> <span data-ttu-id="28c3a-119">이러한 파일의 추출 된 텍스트는 case 폴더에 텍스트 파일로 저장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="28c3a-119">The extracted text of these files is stored as text files in the case folder.</span></span>
    
- <span data-ttu-id="28c3a-120">**메타 데이터 업데이트**: 로드 된 메타 데이터를 처리 합니다.</span><span class="sxs-lookup"><span data-stu-id="28c3a-120">**Updating metadata**: Processes the loaded metadata.</span></span> 
    
- <span data-ttu-id="28c3a-121">**마무리**: 로드 된 사례 파일의 데이터를 종료 하는 내부 처리 (예를 들어 오류 및 성공 파일 식별)입니다.</span><span class="sxs-lookup"><span data-stu-id="28c3a-121">**Finalizing**: Internal processing that finalizes data of loaded case files (for example, identify error and success files).</span></span> 
    
<span data-ttu-id="28c3a-122">작업 상태: 작업 완료 후에 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="28c3a-122">Task status: Displayed after task completion.</span></span> <span data-ttu-id="28c3a-123">작업이 실행 되는 동안 실행 기간이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="28c3a-123">While tasks are running, run duration is displayed.</span></span>
  
> [!NOTE]
> <span data-ttu-id="28c3a-124">완료 된 작업에는 처리를 완료 한 파일, 오류가 발생 한 파일에 대 한 요약도 포함 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="28c3a-124">Completed tasks may also include totals for files that completed processing or files with errors.</span></span> 
  
> [!TIP]
> <span data-ttu-id="28c3a-125">"취소"를 선택 하면 프로세스 실행을 중지 하 고 이전 데이터 채우기 또는 저장 처리 된 데이터로 롤백하는 롤백 옵션이 제공 됩니다.</span><span class="sxs-lookup"><span data-stu-id="28c3a-125">"Cancel" provides a rollback option to stop Process execution and then roll back to the previous data population or saved processed data.</span></span> <span data-ttu-id="28c3a-126">Rollback 처리 된 데이터를 모두 지웁니다.</span><span class="sxs-lookup"><span data-stu-id="28c3a-126">Rollback clears all processed data.</span></span> <span data-ttu-id="28c3a-127">처리 된 데이터를 손실 하지 않으려면 (예: 이러한 파일을 다시 로드 하려는 경우)이 창에서 "취소" 옵션을 선택 하 여 롤백하지 않도록 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="28c3a-127">If you do not want the processed data to be lost (for example, you plan to reload these files), select the "Cancel" option in this window to choose not to roll back.</span></span> 
  
## <a name="process-summary"></a><span data-ttu-id="28c3a-128">프로세스 요약</span><span class="sxs-lookup"><span data-stu-id="28c3a-128">Process summary</span></span>

<span data-ttu-id="28c3a-129">프로세스 \> \> 결과 \> 준비 프로세스 요약에서는 파일 처리 성공 및 오류 결과에 따라 로드 된 파일 결과를 분석 하 여 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="28c3a-129">In Prepare \> Process \> Results \> Process summary, a breakdown of loaded file results is displayed according to successful file processing and error results.</span></span>
  
<span data-ttu-id="28c3a-130">이 창은 다음과 같이 가져온 파일 통계를 그래픽으로 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="28c3a-130">The panes present a graphical display of imported file statistics, as follows:</span></span>
  
- <span data-ttu-id="28c3a-131">**프로세스 요약**이 사례에 있는 모든 파일을 누적 합니다.</span><span class="sxs-lookup"><span data-stu-id="28c3a-131">**Process summary accumulate**d: All files in the case.</span></span>
    
- <span data-ttu-id="28c3a-132">**프로세스 요약 마지막**: 마지막 세션 또는 작업에서 로드 된 파일입니다.</span><span class="sxs-lookup"><span data-stu-id="28c3a-132">**Process summary last**: Files loaded from the last session or action.</span></span> 
    
- <span data-ttu-id="28c3a-133">**성 계열**: 사례 (있는 경우)의 패밀리 정보</span><span class="sxs-lookup"><span data-stu-id="28c3a-133">**Families last**: Family information in the case (if any).</span></span>
    
- <span data-ttu-id="28c3a-134">**시드** 파일을 추가 하면 파일에 대해 정의 된 문제 당 시드 파일 수가 나열 됩니다.</span><span class="sxs-lookup"><span data-stu-id="28c3a-134">If **Seed** files were added, the number of seed files is listed per issue that was defined for the files.</span></span> 
    
    <span data-ttu-id="28c3a-135">**시드** 파일을 표시 하지 못한 경우에도 해당 됩니다.</span><span class="sxs-lookup"><span data-stu-id="28c3a-135">If the marking of **Seed** files failed, that is also noted.</span></span> 
    
- <span data-ttu-id="28c3a-136">**사전 태그가 지정** 된 파일이 추가 되 면 파일에 대해 정의 된 문제 당 미리 태그가 지정 된 파일의 수가 나열 됩니다.</span><span class="sxs-lookup"><span data-stu-id="28c3a-136">If **Pre-tagged** files were added, the number of pre-tagged files is listed per issue that was defined for the files.</span></span> 
    
    <span data-ttu-id="28c3a-137">**미리 태그가 지정** 된 파일을 표시 하는 데 실패 한 경우에도 해당 됩니다.</span><span class="sxs-lookup"><span data-stu-id="28c3a-137">If the marking of **Pre-tagged** files failed, that is also noted.</span></span> 
    
![프로세스 모듈 요약](media/2086a691-9e3d-4117-beb2-a5c3a9a4cc94.png)
  
## <a name="process-summary-accumulated-and-last-charts"></a><span data-ttu-id="28c3a-139">누적 프로세스 요약 및 마지막 차트</span><span class="sxs-lookup"><span data-stu-id="28c3a-139">Process summary accumulated and last charts</span></span>

<span data-ttu-id="28c3a-140">왼쪽 막대에는 원본 + 추출한 파일 (모든 파일)이 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="28c3a-140">The left bar includes Source + extracted files: which is all files found.</span></span> 
  
<span data-ttu-id="28c3a-141">처리 된 오른쪽 막대에는 다음이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="28c3a-141">The right bar, Processed, includes:</span></span>
  
- <span data-ttu-id="28c3a-142">로드 오류가 발생 한 파일</span><span class="sxs-lookup"><span data-stu-id="28c3a-142">Files with load errors</span></span>
    
- <span data-ttu-id="28c3a-143">파일을 성공적으로 로드 했으며, 다음을 포함할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="28c3a-143">Successfully loaded files, which may include:</span></span> 
    
  - <span data-ttu-id="28c3a-144">**기존**파일: 이전에 로드 되 고 다시 로드 되는 (중복 항목 포함).</span><span class="sxs-lookup"><span data-stu-id="28c3a-144">**Existing**: Files that were loaded before and are now loaded again (including duplicates).</span></span>
    
  - <span data-ttu-id="28c3a-145">**텍스트**: 텍스트를 포함 하는 고유한 파일입니다.</span><span class="sxs-lookup"><span data-stu-id="28c3a-145">**Text**: Unique files with text.</span></span>
    
  - <span data-ttu-id="28c3a-146">**텍스트가 아닌**경우: 빈 텍스트 파일, 빈 네이티브 텍스트 파일, 기본 텍스트가 아닌 파일</span><span class="sxs-lookup"><span data-stu-id="28c3a-146">**Non-text**: Empty text files, empty native text files, native non-text files.</span></span> 
    
  - <span data-ttu-id="28c3a-147">**중복**s: 텍스트와 중복 된 파일을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="28c3a-147">**Duplicate**s: Duplicate files with text.</span></span>
    
## <a name="last-process-errors"></a><span data-ttu-id="28c3a-148">마지막 프로세스 오류</span><span class="sxs-lookup"><span data-stu-id="28c3a-148">Last process errors</span></span>

<span data-ttu-id="28c3a-149">준비 \> 프로세스 \> 결과 \> 에서 마지막 프로세스 오류가 발생 하면 마지막 세션에 있는 오류 또는 수행 된 작업에 대 한 세부 정보가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="28c3a-149">In Prepare \> Process \> Results \> Last process errors, details of the errors in the last session or action performed are displayed.</span></span>
  
![프로세스 모듈 오류](media/4771d0f4-4217-445a-9ba4-8b6541c5ad09.png)
  
## <a name="see-also"></a><span data-ttu-id="28c3a-151">참고 항목</span><span class="sxs-lookup"><span data-stu-id="28c3a-151">See also</span></span>

[<span data-ttu-id="28c3a-152">Office 365 Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="28c3a-152">Office 365 Advanced eDiscovery</span></span>](office-365-advanced-ediscovery.md)
  
[<span data-ttu-id="28c3a-153">프로세스 모듈 실행 및 데이터 로드</span><span class="sxs-lookup"><span data-stu-id="28c3a-153">Running the Process module and loading data</span></span>](run-the-process-module-and-load-data-in-advanced-ediscovery.md)

