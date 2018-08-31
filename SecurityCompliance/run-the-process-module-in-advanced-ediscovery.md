---
title: Office 365 Advanced eDiscovery 프로세스 모듈 실행
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
ms.assetid: dbc1e251-0596-443b-ac9b-f398ba955b73
description: 'Office 365 고급 eDiscovery 사용 하 여 분석에 대 한 Office 365 데이터의 경우 준비 파일에 대 한 지침에 알아봅니다.  '
ms.openlocfilehash: 52b1dce9fb778c6628d90c39135f0c93f08134d7
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22534049"
---
# <a name="run-the-process-module-in-office-365-advanced-ediscovery"></a><span data-ttu-id="40e87-103">Office 365 Advanced eDiscovery 프로세스 모듈 실행</span><span class="sxs-lookup"><span data-stu-id="40e87-103">Run the Process module in Office 365 Advanced eDiscovery</span></span>

<span data-ttu-id="40e87-104">사례 파일을 **준비** 하는 동안 고급 eDiscovery에 로드 \> **프로세스**입니다.</span><span class="sxs-lookup"><span data-stu-id="40e87-104">Case files are loaded into the Advanced eDiscovery during **Prepare** \> **Process**.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="40e87-p101">고급 eDiscovery 조직에 대 한 고급 준수 추가 기능 또는 e 5 구독은 Office 365 E3 필요합니다. 해당 요금제에 가입한 상태 고급 eDiscovery 시도 하려는 하지 경우에 [Office 365 Enterprise e 5의 평가판 등록](https://go.microsoft.com/fwlink/p/?LinkID=698279)할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="40e87-p101">Advanced eDiscovery requires an Office 365 E3 with the Advanced Compliance add-on or an E5 subscription for your organization. If you don't have that plan and want to try Advanced eDiscovery, you can [sign up for a trial of Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span></span> 
  
## <a name="guidelines-preparing-data-for-advanced-ediscovery"></a><span data-ttu-id="40e87-107">고급 eDiscovery에 대 한 데이터를 준비 하는 지침:</span><span class="sxs-lookup"><span data-stu-id="40e87-107">Guidelines: Preparing data for Advanced eDiscovery</span></span>

- <span data-ttu-id="40e87-108">**품질**: 대/소문자와 관련 된 사례 파일 모집단을 명확 하 게 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="40e87-108">**Quality**: Clearly identify the case file population pertinent to the case.</span></span>
    
- <span data-ttu-id="40e87-109">**로드**: 고급 eDiscovery에 액세스할 수 있는 위치에 파일을 로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="40e87-109">**Loads**: Load the files into a location that is accessible to Advanced eDiscovery.</span></span>
    
- <span data-ttu-id="40e87-p102">**파일 ID**: 고급 eDiscovery의 고유 식별자입니다. 고급 eDiscovery ID를 자동으로 생성 되지 파일 식별자를 가져오는 경우 사용 하 여 이후에 프로세스 로드의 ID를 매핑할은 초기 프로세스 중에 다른 경로 매핑합니다 하는 경우 고급 eDiscovery는 대체 경로 (되지 않고 새 파일 항목을 추가). ID는 내보내기 프로세스에 대 한 참조로 사용할 수 있습니다. ID 값을 "-1" 해서는 안됩니다.</span><span class="sxs-lookup"><span data-stu-id="40e87-p102">**File ID**: A unique file identifier in Advanced eDiscovery. If no file identifier is imported, Advanced eDiscovery automatically generates the ID. If you map the ID in a subsequent Process load, and map a different path than in the initial Process load, Advanced eDiscovery will replace the path (rather than add a new file entry). The ID can be used as a reference in the Export process. The ID value should not be "-1".</span></span>
    
- <span data-ttu-id="40e87-p103">**M d 5**:이 서명 (두 파일 간주 되지 않습니다 정확히 중복 동일한 MD5 없는 경우) 파일을 구분 하기 위해 사용 됩니다. 기본적으로 고급 eDiscovery 파일의 MD5을 계산합니다. 로드 된 파일은 텍스트 파일을 하는 경우에 로드 하 고 고급 ediscovery에서 계산 하는 대신 원래 MD5 값을 매핑하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="40e87-p103">**MD5**: This signature is used to differentiate between files (two files are not considered exact duplicates unless they have the same MD5). By default, Advanced eDiscovery calculates the MD5 of files. When the loaded files are text files, it is recommended to load and map the original MD5 value instead of calculating it in Advanced eDiscovery.</span></span>
    
- <span data-ttu-id="40e87-118">**파일 형식 및 이름**:</span><span class="sxs-lookup"><span data-stu-id="40e87-118">**File type and name**:</span></span>
    
  - <span data-ttu-id="40e87-p104">고급 eDiscovery 수 있는 다양 한 형식의 파일을 처리 하 고와 같은 표준 형식으로 로드 된 기본 파일을 추출 \*합니다. TXT, HTML 또는 합니다. 텍스트 파일의 처리 되는 XML. 네이티브 파일 보다 더 빠릅니다. 추출 된 텍스트 파일의 경우 폴더에 저장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="40e87-p104">Advanced eDiscovery can process files of various formats and extract loaded native files into a standard format, such as \*.TXT, HTML, or .XML. Processing of text files is faster than native files. Extracted text files are stored in the case folder.</span></span>
    
  - <span data-ttu-id="40e87-p105">시스템 파일 또는 그래픽 이미지와 같은 추출할 수 없는 파일을 로드 하지 않습니다. 이러한 파일 처리를 지연 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="40e87-p105">Do not load files that cannot be extracted, such as system files or graphic images. These files may delay processing.</span></span>
    
  - <span data-ttu-id="40e87-124">파일 이름은 명명 된 크게 경로가 올바른지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="40e87-124">Verify that file names are significantly named and paths are correct.</span></span>
    
- <span data-ttu-id="40e87-125">**파일 경로**: 고급 eDiscovery 최대 400 자까지 입력할 경로 길이 함께 파일을 로드할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="40e87-125">**File path**: Advanced eDiscovery can load files with path lengths up to 400 characters.</span></span>
    
- <span data-ttu-id="40e87-p106">**텍스트 추출**: 다음에도 압축을 푼 일반 텍스트 외에도 네이티브 파일에서 텍스트를 추출 하는 경우: 숨겨진된 텍스트 (Excel 및.doc) 숨겨진 열 (Excel) (예: 변경 내용 (.doc), 발표자 노트 (.ppt)가 포함 된 개체를 추적 합니다 Excel의에서 개체는.ppt)입니다. 이러한 텍스트 편집기에서 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="40e87-p106">**Text extraction**: When extracting text from native files, in addition to normal text, the following are also extracted: hidden text (Excel and .doc), hidden columns (Excel), track changes (.doc), speaker notes (.ppt), embedded objects (for example, Excel objects in a .ppt). These can be viewed in the Text editor.</span></span>
    
- <span data-ttu-id="40e87-p107">**텍스트를 무시**: 후 프로세스를 실행 하 고 분석 하기 전에이 선택적 기능 정의 됩니다. 무시 용도 파일 분석의 성능을 저하 시킬 수 주의 하 여 텍스트를 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="40e87-p107">**Ignore Text**: This optional feature is defined after Process is run and before Analyze. Ignore text should be used with caution because its use may reduce the performance of file analysis.</span></span>
    
- <span data-ttu-id="40e87-130">**다국어 텍스트**: 고급 eDiscovery 태그, 더불어, 및 문제에 대 한 다국어 이름을 현재 처리 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="40e87-130">**Multilingual text**: Advanced eDiscovery does not currently handle multilingual names for tags, custodian, and issues.</span></span>
    
- <span data-ttu-id="40e87-p108">**메타 데이터**: 메타 데이터를 더불어, 나중에 참조할 수 날짜 범위, 파일 크기, 파일 형식에 대 한 사례 데이터베이스에 저장 하 고 주체 인지 확인 합니다. 파일이 이미 인벤토리를 다시 실행 하거나 재처리 오버 헤드를 추가 하지 않고 로드 된 후에 메타 데이터를 로드할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="40e87-p108">**Metadata**: Determine if there is metadata that you want to save in the case database for future reference, such as date range, file size, file type, custodian, and subject. Metadata can be loaded after files were already loaded without rerunning the inventory or adding reprocessing overhead.</span></span> 
    
  - <span data-ttu-id="40e87-p109">원래 파일 경로 의해 로드 하는 경우 나중에 메타 데이터를 가져올 때 경로 열을 매핑하십시오. 될 ID 하 여 파일을 참조 하 고 다른 경로 매핑할 수 있습니다. 파일 경로 변경할 때 유용한 시나리오입니다.</span><span class="sxs-lookup"><span data-stu-id="40e87-p109">If the files were originally loaded by path, map the path column when later importing metadata. It is possible to refer to the file by ID and to map a different path. This is a useful scenario when the file paths change.</span></span>
    
  - <span data-ttu-id="40e87-p110">원래 파일 파일 ID로 로드 하는 경우 메타 데이터를 로드할 때 ID 열을 매핑하십시오. 다른 id 다시 로드할 파일 포함 될 파일 경로 (ID) 하는 대신 하 여 참조 고급 eDiscovery의 기존 파일 로드 메타 데이터를 보다 파일의 복사본을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="40e87-p110">If the files were originally loaded by File ID, map the ID column when loading metadata. Referring to the file by path (instead of ID) will cause files to be re-loaded with a different ID. Advanced eDiscovery creates copies of the files rather that loading metadata of the existing files.</span></span>
    
- <span data-ttu-id="40e87-139">**제품군**: 부모 (제품군의 헤드) 없이 제품군을 로드할 수 없는 합니다.</span><span class="sxs-lookup"><span data-stu-id="40e87-139">**Families**: It is not possible to load a family without its parent (head of family).</span></span> 
    
- <span data-ttu-id="40e87-p111">**파일 크기**:는 고급 eDiscovery로 로드 되는 파일의 크기에 제한이 없습니다. 분석 (분석, 관련성 등)에 대 한 제한은 추출 된 텍스트의 5,242,880 문자입니다. 더 큰 파일은 무시 됩니다 (등 관련성에서 관련성 교육 프로세스에 참여 하지 않는 파일과 일괄 처리 계산 후 관련성 점수를 받지 못하므로).</span><span class="sxs-lookup"><span data-stu-id="40e87-p111">**File size**: There is no limitation on the size of files loaded to Advanced eDiscovery. For analysis (Analyze, Relevance, etc.), the limit is 5,242,880 characters of extracted text. Larger files are ignored (for example, in Relevance, files do not participate in the Relevance training process and do not receive a Relevance score after batch calculation).</span></span>
    
- <span data-ttu-id="40e87-p112">**파일 수량**: 단일 사례에서 처리 될 수 있는 파일의 수에 권장 제한은 없습니다. 성능은 시스템의 리소스에 따라 달라 집니다.</span><span class="sxs-lookup"><span data-stu-id="40e87-p112">**File quantity**: There is no recommended limit on the number of files that can be handled in a single case. Performance depends on the resources of your system.</span></span> 
    
## <a name="filtering-files"></a><span data-ttu-id="40e87-145">파일 필터링</span><span class="sxs-lookup"><span data-stu-id="40e87-145">Filtering files</span></span>

<span data-ttu-id="40e87-p113">사용자 정의 레이블 프로세스 또는 다른 작업에서 제외 하도록 파일 집합으로 연결할 수 있습니다. 각 프로세스 세션 일괄 처리 id 연결 됩니다. 게시할 수도 있지만 일괄 처리 ID 관련성에 전문가 게 표시 되지 않으면 현재 일괄 처리에 대 한 필터를 추가 하 고 사용자 정의 레이블 포함 된 모든 해당 파일에 태그를 지정 하 여 검색 유틸리티를 사용 하 여 합니다.</span><span class="sxs-lookup"><span data-stu-id="40e87-p113">A user-defined label can be associated with a set of files to exclude them from Process or other tasks. Each Process session is associated with a batch ID. Although the batch ID is not visible to the expert in Relevance, this can be done using a search utility, by adding a filter for the current batch and tagging all appropriate files with a user-defined label.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="40e87-149">참고 항목</span><span class="sxs-lookup"><span data-stu-id="40e87-149">See also</span></span>

[<span data-ttu-id="40e87-150">Office 365 Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="40e87-150">Office 365 Advanced eDiscovery</span></span>](office-365-advanced-ediscovery.md)
  
[<span data-ttu-id="40e87-151">프로세스 모듈을 실행 하 고 데이터 로드</span><span class="sxs-lookup"><span data-stu-id="40e87-151">Running the Process module and loading data</span></span>](run-the-process-module-and-load-data-in-advanced-ediscovery.md)
  
[<span data-ttu-id="40e87-152">프로세스 모듈 결과 보기</span><span class="sxs-lookup"><span data-stu-id="40e87-152">Viewing Process module results</span></span>](view-process-module-results-in-advanced-ediscovery.md)

