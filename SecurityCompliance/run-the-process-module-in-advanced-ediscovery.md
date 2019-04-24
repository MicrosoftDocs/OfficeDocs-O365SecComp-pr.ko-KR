---
title: Office 365 Advanced eDiscovery에서 프로세스 모듈 실행
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
ms.assetid: dbc1e251-0596-443b-ac9b-f398ba955b73
description: 'office 365 Advanced eDiscovery를 사용 하 여 분석을 위해 office 365 데이터의 사례 파일을 준비 하기 위한 지침을 알아봅니다.  '
ms.openlocfilehash: 19d50bda21f752ec7c22fe52b6fa7272592de128
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32261036"
---
# <a name="run-the-process-module-in-office-365-advanced-ediscovery"></a><span data-ttu-id="715df-103">Office 365 Advanced eDiscovery에서 프로세스 모듈 실행</span><span class="sxs-lookup"><span data-stu-id="715df-103">Run the Process module in Office 365 Advanced eDiscovery</span></span>

<span data-ttu-id="715df-104">사례 파일은 **준비** \> **프로세스**중에 고급 eDiscovery에 로드 됩니다.</span><span class="sxs-lookup"><span data-stu-id="715df-104">Case files are loaded into the Advanced eDiscovery during **Prepare** \> **Process**.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="715df-p101">Advanced eDiscovery를 사용하려면 Office 365 E3의 고급 준수 추가 기능이나 조직을 위한 E5 구독이 필요합니다. 이 요금제가 없는 상태에서 Advanced eDiscovery를 사용하려는 경우에는 [Office 365 Enterprise E5 평가판을 등록](https://go.microsoft.com/fwlink/p/?LinkID=698279)할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="715df-p101">Advanced eDiscovery requires an Office 365 E3 with the Advanced Compliance add-on or an E5 subscription for your organization. If you don't have that plan and want to try Advanced eDiscovery, you can [sign up for a trial of Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span></span> 
  
## <a name="guidelines-preparing-data-for-advanced-ediscovery"></a><span data-ttu-id="715df-107">지침: 고급 eDiscovery에 대 한 데이터 준비</span><span class="sxs-lookup"><span data-stu-id="715df-107">Guidelines: Preparing data for Advanced eDiscovery</span></span>

- <span data-ttu-id="715df-108">**품질**: 사례에 대 한 사례 파일 채우기를 명확 하 게 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="715df-108">**Quality**: Clearly identify the case file population pertinent to the case.</span></span>
    
- <span data-ttu-id="715df-109">\*\*\*\* Load: 고급 eDiscovery에 액세스할 수 있는 위치에 파일을 로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="715df-109">**Loads**: Load the files into a location that is accessible to Advanced eDiscovery.</span></span>
    
- <span data-ttu-id="715df-110">**파일 ID**: Advanced eDiscovery의 고유한 파일 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="715df-110">**File ID**: A unique file identifier in Advanced eDiscovery.</span></span> <span data-ttu-id="715df-111">파일 식별자를 가져오지 않으면 고급 eDiscovery에서 자동으로 ID를 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="715df-111">If no file identifier is imported, Advanced eDiscovery automatically generates the ID.</span></span> <span data-ttu-id="715df-112">후속 프로세스 부하에서 ID를 매핑하고 초기 프로세스 부하와 다른 경로를 매핑하면 고급 eDiscovery는 경로 (새 파일 항목을 추가 하는 것이 아님)를 대체 합니다.</span><span class="sxs-lookup"><span data-stu-id="715df-112">If you map the ID in a subsequent Process load, and map a different path than in the initial Process load, Advanced eDiscovery will replace the path (rather than add a new file entry).</span></span> <span data-ttu-id="715df-113">이 ID는 내보내기 프로세스에서 참조로 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="715df-113">The ID can be used as a reference in the Export process.</span></span> <span data-ttu-id="715df-114">ID 값은 "-1"이 아니어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="715df-114">The ID value should not be "-1".</span></span>
    
- <span data-ttu-id="715df-115">**MD5**:이 서명은 파일을 구분 하는 데 사용 됩니다 (MD5가 같은 경우가 아니면 두 파일은 정확히 중복 된 것으로 간주 되지 않음).</span><span class="sxs-lookup"><span data-stu-id="715df-115">**MD5**: This signature is used to differentiate between files (two files are not considered exact duplicates unless they have the same MD5).</span></span> <span data-ttu-id="715df-116">기본적으로 고급 eDiscovery에서는 파일의 MD5를 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="715df-116">By default, Advanced eDiscovery calculates the MD5 of files.</span></span> <span data-ttu-id="715df-117">로드 된 파일이 텍스트 파일인 경우에는 고급 eDiscovery에서이를 계산 하는 대신 원래 MD5 값을 로드 하 여 매핑하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="715df-117">When the loaded files are text files, it is recommended to load and map the original MD5 value instead of calculating it in Advanced eDiscovery.</span></span>
    
- <span data-ttu-id="715df-118">**파일 형식 및 이름**:</span><span class="sxs-lookup"><span data-stu-id="715df-118">**File type and name**:</span></span>
    
  - <span data-ttu-id="715df-119">고급 eDiscovery에서는 다양 한 형식의 파일을 처리 하 고 로드 된 원시 파일을와 \*같은 표준 형식으로 추출할 수 있습니다. TXT, HTML 또는입니다. l.</span><span class="sxs-lookup"><span data-stu-id="715df-119">Advanced eDiscovery can process files of various formats and extract loaded native files into a standard format, such as \*.TXT, HTML, or .XML.</span></span> <span data-ttu-id="715df-120">텍스트 파일의 처리가 기본 파일 보다 빠릅니다.</span><span class="sxs-lookup"><span data-stu-id="715df-120">Processing of text files is faster than native files.</span></span> <span data-ttu-id="715df-121">추출 된 텍스트 파일은 사례 폴더에 저장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="715df-121">Extracted text files are stored in the case folder.</span></span>
    
  - <span data-ttu-id="715df-122">시스템 파일이 나 그래픽 이미지와 같이 추출할 수 없는 파일을 로드 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="715df-122">Do not load files that cannot be extracted, such as system files or graphic images.</span></span> <span data-ttu-id="715df-123">이러한 파일은 처리 지연 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="715df-123">These files may delay processing.</span></span>
    
  - <span data-ttu-id="715df-124">파일 이름의 이름이 정확 하 고 경로가 올바른지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="715df-124">Verify that file names are significantly named and paths are correct.</span></span>
    
- <span data-ttu-id="715df-125">**파일 경로**: 고급 eDiscovery에서는 경로 길이가 최대 400 자인 파일을 로드할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="715df-125">**File path**: Advanced eDiscovery can load files with path lengths up to 400 characters.</span></span>
    
- <span data-ttu-id="715df-126">**텍스트 추출**: 기본 파일에서 텍스트를 추출할 때 일반 텍스트 외에도 다음과 같은 추출 된 텍스트 (excel 및 .doc), 숨겨진 열 (excel), 변경 내용 (.doc), 발표자 노트 (.ppt), 포함 된 개체 (예: .ppt의 Excel 개체)</span><span class="sxs-lookup"><span data-stu-id="715df-126">**Text extraction**: When extracting text from native files, in addition to normal text, the following are also extracted: hidden text (Excel and .doc), hidden columns (Excel), track changes (.doc), speaker notes (.ppt), embedded objects (for example, Excel objects in a .ppt).</span></span> <span data-ttu-id="715df-127">텍스트 편집기에서 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="715df-127">These can be viewed in the Text editor.</span></span>
    
- <span data-ttu-id="715df-128">**텍스트 무시**:이 선택적 기능은 프로세스를 실행 한 후 분석 하기 전에 정의 됩니다.</span><span class="sxs-lookup"><span data-stu-id="715df-128">**Ignore Text**: This optional feature is defined after Process is run and before Analyze.</span></span> <span data-ttu-id="715df-129">Ignore 텍스트 사용은 파일 분석의 성능을 저하 시킬 수 있으므로 주의 해 서 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="715df-129">Ignore text should be used with caution because its use may reduce the performance of file analysis.</span></span>
    
- <span data-ttu-id="715df-130">**다국어 텍스트**: 고급 eDiscovery는 현재 태그, custodian 및 문제에 대 한 다국어 이름을 처리 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="715df-130">**Multilingual text**: Advanced eDiscovery does not currently handle multilingual names for tags, custodian, and issues.</span></span>
    
- <span data-ttu-id="715df-131">**메타 데이터**: 날짜 범위, 파일 크기, 파일 형식, custodian 및 제목과 같은 나중에 참조할 수 있도록 사례 데이터베이스에 저장할 메타 데이터가 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="715df-131">**Metadata**: Determine if there is metadata that you want to save in the case database for future reference, such as date range, file size, file type, custodian, and subject.</span></span> <span data-ttu-id="715df-132">인벤토리를 다시 실행 하거나 다시 처리 오버 헤드를 추가 하지 않고 파일을 이미 로드 한 후 메타 데이터를 로드할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="715df-132">Metadata can be loaded after files were already loaded without rerunning the inventory or adding reprocessing overhead.</span></span> 
    
  - <span data-ttu-id="715df-133">파일을 원래 경로로 로드 한 경우 나중에 메타 데이터를 가져올 때 path 열을 매핑합니다.</span><span class="sxs-lookup"><span data-stu-id="715df-133">If the files were originally loaded by path, map the path column when later importing metadata.</span></span> <span data-ttu-id="715df-134">ID로 파일을 참조 하 고 다른 경로를 매핑할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="715df-134">It is possible to refer to the file by ID and to map a different path.</span></span> <span data-ttu-id="715df-135">이는 파일 경로가 변경 되는 경우에 유용한 시나리오입니다.</span><span class="sxs-lookup"><span data-stu-id="715df-135">This is a useful scenario when the file paths change.</span></span>
    
  - <span data-ttu-id="715df-136">파일 id로 파일을 처음으로 로드 한 경우 메타 데이터를 로드할 때 ID 열을 매핑하십시오.</span><span class="sxs-lookup"><span data-stu-id="715df-136">If the files were originally loaded by File ID, map the ID column when loading metadata.</span></span> <span data-ttu-id="715df-137">경로를 기준으로 파일을 참조 하면 다른 id로 파일을 다시 로드할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="715df-137">Referring to the file by path (instead of ID) will cause files to be re-loaded with a different ID.</span></span> <span data-ttu-id="715df-138">고급 eDiscovery에서는 기존 파일의 메타 데이터를 로드 하는 대신 파일의 복사본을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="715df-138">Advanced eDiscovery creates copies of the files rather that loading metadata of the existing files.</span></span>
    
- <span data-ttu-id="715df-139">**제품군**: 상위 (패밀리 머리) 없이 패밀리를 로드할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="715df-139">**Families**: It is not possible to load a family without its parent (head of family).</span></span> 
    
- <span data-ttu-id="715df-140">**파일 크기**: 고급 eDiscovery로 로드 되는 파일의 크기에 제한이 없습니다.</span><span class="sxs-lookup"><span data-stu-id="715df-140">**File size**: There is no limitation on the size of files loaded to Advanced eDiscovery.</span></span> <span data-ttu-id="715df-141">분석 (분석, 관련성 등)을 위해이 제한은 추출 된 텍스트의 5242880 자입니다.</span><span class="sxs-lookup"><span data-stu-id="715df-141">For analysis (Analyze, Relevance, etc.), the limit is 5,242,880 characters of extracted text.</span></span> <span data-ttu-id="715df-142">예를 들어 관련성이 가장 큰 파일은 무시 되 고, 파일은 관련성이 있는 교육 프로세스에 참여 하지 않으며, 일괄 처리 후에는 관련성 점수를 받지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="715df-142">Larger files are ignored (for example, in Relevance, files do not participate in the Relevance training process and do not receive a Relevance score after batch calculation).</span></span>
    
- <span data-ttu-id="715df-143">**파일 수량**: 단일 사례에서 처리할 수 있는 파일 수에 대 한 권장 제한이 없습니다.</span><span class="sxs-lookup"><span data-stu-id="715df-143">**File quantity**: There is no recommended limit on the number of files that can be handled in a single case.</span></span> <span data-ttu-id="715df-144">성능은 시스템의 리소스에 따라 달라 집니다.</span><span class="sxs-lookup"><span data-stu-id="715df-144">Performance depends on the resources of your system.</span></span> 
    
## <a name="filtering-files"></a><span data-ttu-id="715df-145">파일 필터링</span><span class="sxs-lookup"><span data-stu-id="715df-145">Filtering files</span></span>

<span data-ttu-id="715df-146">사용자 정의 레이블을 파일 집합에 연결 하 여 프로세스나 다른 작업에서 제외할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="715df-146">A user-defined label can be associated with a set of files to exclude them from Process or other tasks.</span></span> <span data-ttu-id="715df-147">각 프로세스 세션은 일괄 처리 ID와 연결 됩니다.</span><span class="sxs-lookup"><span data-stu-id="715df-147">Each Process session is associated with a batch ID.</span></span> <span data-ttu-id="715df-148">일괄 처리 ID는 전문가가 볼 수 없지만 현재 일괄 처리에 대 한 필터를 추가 하 고 사용자 정의 레이블을 사용 하 여 적절 한 모든 파일에 태그를 지정 하 여 검색 유틸리티를 사용 하 여이 작업을 수행할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="715df-148">Although the batch ID is not visible to the expert in Relevance, this can be done using a search utility, by adding a filter for the current batch and tagging all appropriate files with a user-defined label.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="715df-149">참고 항목</span><span class="sxs-lookup"><span data-stu-id="715df-149">See also</span></span>

[<span data-ttu-id="715df-150">Office 365 Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="715df-150">Office 365 Advanced eDiscovery</span></span>](office-365-advanced-ediscovery.md)
  
[<span data-ttu-id="715df-151">프로세스 모듈 실행 및 데이터 로드</span><span class="sxs-lookup"><span data-stu-id="715df-151">Running the Process module and loading data</span></span>](run-the-process-module-and-load-data-in-advanced-ediscovery.md)
  
[<span data-ttu-id="715df-152">프로세스 모듈 결과 보기</span><span class="sxs-lookup"><span data-stu-id="715df-152">Viewing Process module results</span></span>](view-process-module-results-in-advanced-ediscovery.md)

