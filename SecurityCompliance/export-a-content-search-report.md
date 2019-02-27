---
title: 콘텐츠 검색 보고서 내보내기
ms.author: markjjo
author: markjjo
manager: laurawi
ms.audience: Admin
ms.topic: article
f1_keywords:
- ms.o365.cc.CustomizeExportReport
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- Strat_O365_IP
- M365-security-compliance
search.appverid:
- MOE150
- MED150
- MBS150
- MET150
ms.assetid: 5c8c1db6-d8ac-4dbb-8a7a-f65d452169b9
description: Office 365 보안 &amp; 및 준수 센터에서 콘텐츠 검색의 실제 결과를 내보내는 대신 검색 결과 보고서를 간단히 내보낼 수 있습니다. 이 보고서에는 검색 결과에 대 한 요약과 내보낼 각 항목에 대 한 자세한 정보가 있는 문서가 포함 되어 있습니다.
ms.openlocfilehash: d98f70d4f38f524de8751aecb197d0f85ee7f088
ms.sourcegitcommit: baf23be44f1ed5abbf84f140b5ffa64fce605478
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/26/2019
ms.locfileid: "30295981"
---
# <a name="export-a-content-search-report"></a><span data-ttu-id="642b3-104">콘텐츠 검색 보고서 내보내기</span><span class="sxs-lookup"><span data-stu-id="642b3-104">Export a Content Search report</span></span>

<span data-ttu-id="642b3-105">Office 365 보안 &amp; 및 준수 센터 (및 eDiscovery 사례와 연결 된 콘텐츠 검색)의 콘텐츠 검색에서 전체 검색 결과 집합을 내보내는 대신, 다음을 수행할 때 생성 되는 것과 동일한 보고서를 내보낼 수 있습니다. 검색 결과를 내보냅니다.</span><span class="sxs-lookup"><span data-stu-id="642b3-105">Instead of exporting the full set of search results from a Content Search in the Office 365 Security &amp; Compliance Center (and from a Content Search that's associated with an eDiscovery case), you can just export the same reports that are generated when you export search results.</span></span>
  
<span data-ttu-id="642b3-p102">보고서를 내보낼 때는 콘텐츠 검색과 이름이 같은 폴더에 다운로드 되지만 *_ReportsOnly* 에 추가 됩니다.. 예를 들어 콘텐츠 검색의 이름이 *ContosoCase0815* 인 경우 보고서가 *ContosoCase0815_ReportsOnly* 라는 폴더에 다운로드 됩니다. 보고서에 포함 되는 문서 목록은 [보고서에 포함 된 항목](#whats-included-in-the-report)을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="642b3-p102">When you export a report, it's downloaded to a folder that has the same name as the Content Search, but that's appended with  *_ReportsOnly*  . For example, if the Content Search is named  *ContosoCase0815*  , then the report is downloaded to a folder named  *ContosoCase0815_ReportsOnly*  . For a list of documents that are included in the report, see [What's included in the report](#whats-included-in-the-report).</span></span>

## <a name="before-you-begin"></a><span data-ttu-id="642b3-109">시작하기 전에</span><span class="sxs-lookup"><span data-stu-id="642b3-109">Before you begin</span></span>

- <span data-ttu-id="642b3-p103">콘텐츠 검색 보고서를 내보내려면 Office 365 보안 &amp; 및 준수 센터에서 준수 검색 관리 역할을 할당 받아야 합니다. 이 역할은 기본 제공 eDiscovery 관리자 및 조직 관리 역할 그룹에 할당 됩니다. 기본적으로 조직 관리 역할 그룹에 할당 되지 않습니다. 자세한 내용은 [Office 365 보안 &amp; 및 준수 센터에서 eDiscovery 사용 권한 할당](assign-ediscovery-permissions.md)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="642b3-p103">To export a Content Search report, you have to be assigned the Compliance Search management role in the Office 365 Security &amp; Compliance Center. This role is assigned to the built-in eDiscovery Manager and Organization Management role groups. It isn't assigned by default to the Organization Management role group. For more information, see [Assign eDiscovery permissions in the Office 365 Security &amp; Compliance Center](assign-ediscovery-permissions.md).</span></span>
    
- <span data-ttu-id="642b3-p104">보고서를 내보낼 때 데이터는 로컬 컴퓨터로 다운로드 되기 전에 Microsoft 클라우드의 고유한 Windows Azure 저장소 영역에 임시로 저장 됩니다. 조직이 Azure의 끝점에 연결할 수 있는지 (와일드 카드는 내보내기에 대 한 고유 식별자를 나타냄) \*\* \*blob.core.windows.net 합니다\*\* . 검색 결과 데이터는 만들어진 후 2 주 후 Azure 저장소 영역에서 삭제 됩니다.</span><span class="sxs-lookup"><span data-stu-id="642b3-p104">When you export a report, the data is temporarily stored in a unique Windows Azure storage area in the Microsoft cloud before it's downloaded to your local computer. Be sure your organization can connect to the endpoint in Azure, which is **\*.blob.core.windows.net** (the wildcard represents a unique identifier for your export). The search results data is deleted from the Azure storage area two weeks after it's created.</span></span> 
    
- <span data-ttu-id="642b3-117">검색 결과를 PST 파일로 내보내는 데 사용하는 컴퓨터는 다음과 같은 시스템 요구 사항을 충족해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="642b3-117">The computer you use to export the search results has to meet the following system requirements:</span></span>
    
  - <span data-ttu-id="642b3-118">32비트 및 64비트 버전의 Windows 7 이상 버전


</span><span class="sxs-lookup"><span data-stu-id="642b3-118">32- or 64-bit versions of Windows 7 and later versions</span></span>
    
  - <span data-ttu-id="642b3-119">Microsoft .net Framework 4.7</span><span class="sxs-lookup"><span data-stu-id="642b3-119">Microsoft .NET Framework 4.7</span></span>
    
  - <span data-ttu-id="642b3-120">지원되는 브라우저:</span><span class="sxs-lookup"><span data-stu-id="642b3-120">A supported browser:</span></span>
    
    - <span data-ttu-id="642b3-121">Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="642b3-121">Microsoft Edge</span></span>
    
      <span data-ttu-id="642b3-122">또는</span><span class="sxs-lookup"><span data-stu-id="642b3-122">or</span></span>
    
    - <span data-ttu-id="642b3-123">Microsoft Internet Explorer 10 이상 버전</span><span class="sxs-lookup"><span data-stu-id="642b3-123">Microsoft Internet Explorer 10 and later versions</span></span>
    
    <span data-ttu-id="642b3-p105">**참고:** Microsoft는 ClickOnce 응용 프로그램에 대 한 타사 확장 또는 추가 기능을 제조 하지 않습니다. 타사 확장 또는 추가 기능에서 지원 되지 않는 브라우저를 사용 하 여 검색 결과를 내보낼 수는 없습니다.</span><span class="sxs-lookup"><span data-stu-id="642b3-p105">**Note:** Microsoft doesn't manufacture third-party extensions or add-ons for ClickOnce applications. Exporting search results using an unsupported browser with third-party extensions or add-ons isn't supported.</span></span> 

- <span data-ttu-id="642b3-p106">콘텐츠 검색에서 반환 되는 결과의 예상 전체 크기가 20tb&nbsp;를 초과 하면 보고서를 내보낼 수 없습니다. 보고서를 성공적으로 내보내려면 범위를 좁히고 검색을 다시 실행 하 여 예상 결과 크기를 20tb&nbsp;보다 작게 합니다.</span><span class="sxs-lookup"><span data-stu-id="642b3-p106">If the estimated total size of the results returned by a Content Search exceeds 20&nbsp;TB, exporting the report will fail. To successfully export the report, try to narrow the scope and re-run the search so the estimated size of the results is less than 20&nbsp;TB.</span></span>

- <span data-ttu-id="642b3-p107">콘텐츠 검색 보고서 내보내기 동시에 실행 되는 내보내기의 최대 수와 단일 사용자가 실행할 수 있는 최대 내보내기 수에 대해 계산 합니다. 내보내기 제한에 대 한 자세한 내용은 [export Content Search results in Office 365 Security & 준수 센터](export-search-results.md#export-limits)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="642b3-p107">Exporting Content Search reports counts against the maximum number of exports running at the same time and the maximum number of exports that a single user can run. For more information about export limits, see [Export Content Search results from the Office 365 Security & Compliance Center](export-search-results.md#export-limits).</span></span>

## <a name="generate-and-download-a-content-search-report"></a><span data-ttu-id="642b3-130">콘텐츠 검색 보고서 생성 및 다운로드</span><span class="sxs-lookup"><span data-stu-id="642b3-130">Generate and download a Content Search report</span></span>

<span data-ttu-id="642b3-131">콘텐츠 검색 보고서를 생성 하 고 다운로드 하는 단계는 실제로 검색 결과를 내보내는 경우와 매우 비슷합니다.</span><span class="sxs-lookup"><span data-stu-id="642b3-131">The steps to generate and download a Content Search report are very similar to actually exporting search results.</span></span>
  
## <a name="step-1-generate-the-report-for-export"></a><span data-ttu-id="642b3-132">1 단계: 내보내기에 대 한 보고서 생성</span><span class="sxs-lookup"><span data-stu-id="642b3-132">Step 1: Generate the report for export</span></span>

<span data-ttu-id="642b3-p108">첫 번째 단계는 컴퓨터 내보내기에 대 한 보고서를 다운로드 하기 위해 준비 하는 것입니다. 보고서를 만들면 보고서 문서가 Microsoft 클라우드의 Azure storage 영역에 업로드 됩니다.</span><span class="sxs-lookup"><span data-stu-id="642b3-p108">The first step is to prepare the report for downloading to your computer exporting. When you the report, the report documents are uploaded to an Azure storage area in the Microsoft cloud.</span></span>
  
1. <span data-ttu-id="642b3-135">[https://protection.office.com](https://protection.office.com)으로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="642b3-135">Go to [https://protection.office.com](https://protection.office.com).</span></span>
    
2. <span data-ttu-id="642b3-136">회사 또는 학교 계정을 사용하여 Office 365에 로그인합니다.</span><span class="sxs-lookup"><span data-stu-id="642b3-136">Sign in to Office 365 using your work or school account.</span></span>
    
3. <span data-ttu-id="642b3-137">보안 및 준수 센터의 왼쪽 창에서 **검색 및 조사** \> **콘텐츠 검색**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="642b3-137">In the left pane of the Security &amp; Compliance Center, click **Search &amp; investigation** \> **Content search**.</span></span>
    
4. <span data-ttu-id="642b3-138">**콘텐츠 검색** 페이지에서 검색을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="642b3-138">On the **Content search** page, select a search.</span></span> 
    
5. <span data-ttu-id="642b3-139">세부 정보 창에서 보고서를 **컴퓨터로 내보내기**에서 **보고서 생성**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="642b3-139">In the details pane, under **Export report to a computer**, click **Generate report**.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="642b3-p109">검색 결과가 7 일 보다 오래 된 경우 검색 결과를 업데이트 하 라는 메시지가 표시 됩니다. 이 경우 내보내기를 취소 하 고 선택한 검색에 대 한 세부 정보 창에서 **검색 결과 업데이트** 를 클릭 한 다음 결과를 업데이트 한 후에 보고서 내보내기를 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="642b3-p109">If the results for a search are older than 7 days, you are prompted to update the search results. If this happens, cancel the export, click **Update search results** in the details pane for the selected search, and then start the report export again after the results are updated.</span></span> 
  
6. <span data-ttu-id="642b3-142">**보고서 내보내기** 페이지의 **검색에서 다음 항목 포함**에서 다음 옵션 중 하나를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="642b3-142">On the **Export a report** page, under **Include these items from the search**, choose one of the following options:</span></span>
    
    - <span data-ttu-id="642b3-143">인덱싱된 항목만 내보내기</span><span class="sxs-lookup"><span data-stu-id="642b3-143">Export only indexed items</span></span>
    
    - <span data-ttu-id="642b3-144">인덱싱 및 인덱싱되지 않은 항목 내보내기</span><span class="sxs-lookup"><span data-stu-id="642b3-144">Export indexed and unindexed items</span></span>
    
    - <span data-ttu-id="642b3-145">인덱싱되지 않은 항목만 내보내기</span><span class="sxs-lookup"><span data-stu-id="642b3-145">Export only unindexed items</span></span>
    
    <span data-ttu-id="642b3-146">인덱싱되지 않은 항목에 대 한 자세한 내용은 [콘텐츠 검색에서 부분적으로 인덱싱된 항목](partially-indexed-items-in-content-search.md)을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="642b3-146">For more information about unindexed items, see [Partially indexed items in Content Search](partially-indexed-items-in-content-search.md).</span></span>
    
7. <span data-ttu-id="642b3-p110">모든 SharePoint 문서 버전에 대 한 검색 통계를 포함 하도록 선택 합니다. 이 옵션은 검색의 콘텐츠 원본에 SharePoint 또는 비즈니스용 OneDrive 사이트를 포함 하는 경우에만 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="642b3-p110">Choose to include search statistics for all versions of SharePoint documents. This option appears only if the content sources of the search includes SharePoint or OneDrive for Business sites.</span></span>
    
8. <span data-ttu-id="642b3-149">**보고서 생성**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="642b3-149">Click **Generate report**.</span></span>
    
    <span data-ttu-id="642b3-p111">검색 결과 보고서를 다운로드 준비 중 이며,이는 보고서 문서가 Microsoft 클라우드의 Azure storage 영역에 업로드 됨을 의미 합니다. 보고서를 다운로드할 준비가 되 면 세부 정보 창의 **컴퓨터로 보고서 내보내기** 아래에 보고서 **다운로드** 링크가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="642b3-p111">The search results report is prepared for downloading, which means the report documents will be uploaded to the Azure storage area in the Microsoft cloud. When the report is ready for download, the **Download report** link is displayed under **Export report to a computer** in the details pane.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="642b3-p112">eDiscovery 사례와 연결 된 콘텐츠 검색에 대 한 보고서를 내보낼 수도 있습니다. 이렇게 하려면 \*\* &amp; 검색 조사\*\* \> **eDiscovery**로 이동 하 여 사례를 선택 하 고 편집 아이콘 \*\*\*\* ![](media/ebd260e4-3556-4fb0-b0bb-cc489773042c.gif)편집을 클릭 합니다. 검색 페이지 \*\*\*\* 에서 검색을 선택 하 고 내보내기 검색 결과 아이콘 \*\*\*\* ![](media/47205c65-babd-4b3a-bd7b-98dfd92883ba.png) \> 내보내기를 클릭 하 **여 보고서를 내보냅니다**.</span><span class="sxs-lookup"><span data-stu-id="642b3-p112">You can also export a report for a Content Search that's associated with an eDiscovery case. To do this, go to **Search &amp; investigation** \> **eDiscovery**, select a case, and click **Edit** ![Edit icon](media/ebd260e4-3556-4fb0-b0bb-cc489773042c.gif). On the **Searches** page, select a search, and then click **Export** ![Export search results icon](media/47205c65-babd-4b3a-bd7b-98dfd92883ba.png) \> **Export a report**.</span></span> 
  
## <a name="step-2-download-the-report"></a><span data-ttu-id="642b3-155">2 단계: 보고서 다운로드</span><span class="sxs-lookup"><span data-stu-id="642b3-155">Step 2: Download the report</span></span>

<span data-ttu-id="642b3-156">다음 단계에서는 Azure storage 영역에서 로컬 컴퓨터로 보고서를 다운로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="642b3-156">The next step is to download the report from the Azure storage area to your local computer.</span></span>
  
1. <span data-ttu-id="642b3-157">보고서를 생성 한 검색에 대 한 세부 정보 창에서 **컴퓨터로 보고서 내보내기**에서 **보고서 다운로드**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="642b3-157">In the details pane for the search that you generated the report for, under **Export report to a computer**, click **Download report**.</span></span>
    
    <span data-ttu-id="642b3-158">보고서 **다운로드** 페이지가 표시 되 고 컴퓨터에 다운로드 될 때까지 보고에 대 한 다음과 같은 정보가 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="642b3-158">The **Download report** page is displayed and contains the following information about the report till be downloaded to your computer.</span></span> 
    
    - <span data-ttu-id="642b3-159">다운로드될 항목의 수</span><span class="sxs-lookup"><span data-stu-id="642b3-159">The number of items that will be downloaded.</span></span>
    
    - <span data-ttu-id="642b3-160">다운로드될 항목의 예상 총 크기</span><span class="sxs-lookup"><span data-stu-id="642b3-160">The estimated total size of the items that will be downloaded.</span></span>
    
    - <span data-ttu-id="642b3-p113">인덱싱된 또는 인덱싱되지 않을 지 여부입니다. 인덱싱되지 않은 항목은 인식할 수 있는 형식을 가진 항목, 암호화 됨 또는 다른 이유로 인덱싱되지 않은 항목이 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="642b3-p113">Whether indexed or unindexed will be exported. Unindexed items are items that have an recognized format, are encrypted, or weren't indexed for other reasons.</span></span>
    
    - <span data-ttu-id="642b3-163">SharePoint 문서의 버전을 다운로드할지 여부</span><span class="sxs-lookup"><span data-stu-id="642b3-163">Whether or not versions of SharePoint documents will be downloaded.</span></span>
    
    - <span data-ttu-id="642b3-p114">보고서 내보내기 프로세스의 상태입니다. 보고서 준비가 완료 되지 않은 경우에도 보고서를 다운로드 하기 시작할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="642b3-p114">The status of the report export process. You can start downloading the report even if the preparation of the report isn't complete.</span></span>
    
2. <span data-ttu-id="642b3-p115">**키 내보내기**에서 **클립보드에 복사**를 클릭 합니다. 5 단계에서이 키를 사용 하 여 보고서를 다운로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="642b3-p115">Under **Export key**, click **Copy to clipboard**. You will use this key in step 5 to download the report.</span></span>
    
    > [!IMPORTANT]
    > <span data-ttu-id="642b3-168">모든 사용자가 eDiscovery 내보내기 도구를 설치 하 고 시작한 다음이 키를 사용 하 여 검색 보고서를 다운로드할 수 있으므로 암호나 기타 보안 관련 정보를 보호 하는 것 처럼이 키를 보호 하는 예방 조치를 취해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="642b3-168">Because anyone can install and start the eDiscovery Export tool, and then use this key to download the search report, be sure to take precautions to protect this key just like you would protect passwords or other security-related information.</span></span> 
  
3. <span data-ttu-id="642b3-169">**보고서 다운로드**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="642b3-169">Click **Download report**.</span></span>
    
4. <span data-ttu-id="642b3-170">**MicrosoftOffice 365 eDiscovery 내보내기 도구**를 설치 하 라는 메시지가 표시 되 면 **설치**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="642b3-170">If you're prompted to install the **MicrosoftOffice 365 eDiscovery Export Tool**, click **Install**.</span></span>
    
5. <span data-ttu-id="642b3-171">**eDiscovery 내보내기 도구**에서 5단계에서 복사한 내보내기 키를 해당 상자에 붙여 넣습니다. </span><span class="sxs-lookup"><span data-stu-id="642b3-171">In the **eDiscovery Export Tool**, paste the export key that you copied in step 2 in the appropriate box.</span></span>
    
6. <span data-ttu-id="642b3-172">**찾아보기를** 클릭 하 여 보고서를 다운로드 하려는 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="642b3-172">Click **Browse** to specify the location where you want to download the report.</span></span> 
    
7. <span data-ttu-id="642b3-173">**시작**을 클릭하여 컴퓨터에 검색 결과를 다운로드합니다.</span><span class="sxs-lookup"><span data-stu-id="642b3-173">Click **Start** to download the search results to your computer.</span></span> 
    
    <span data-ttu-id="642b3-p116">**eDiscovery 내보내기 도구** 는 다운로드 되는 나머지 항목의 번호 및 크기를 포함 하 여 내보내기 프로세스에 대 한 상태 정보를 표시 합니다. 내보내기 프로세스가 완료 되 면 다운로드 한 위치에서 파일에 액세스할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="642b3-p116">The **eDiscovery Export Tool** displays status information about the export process, including an estimate of the number (and size) of the remaining items to be downloaded. When the export process is complete, you can access the files in the location where they were downloaded.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="642b3-p117">eDiscovery 사례와 연결 된 콘텐츠 검색에 대 한 보고서를 다운로드할 수 있습니다. 이렇게 하려면 \*\* &amp; 검색 조사\*\* \> **eDiscovery**로 이동 하 여 사례를 선택 하 고 편집 아이콘 \*\*\*\* ![](media/ebd260e4-3556-4fb0-b0bb-cc489773042c.gif)편집을 클릭 합니다. **내보내기** 페이지에서 보고서 내보내기를 선택 하 고 세부 정보 창에서 **보고서 다운로드** 를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="642b3-p117">You can download the report for a Content Search that's associated with an eDiscovery case. To do this, go to **Search &amp; investigation** \> **eDiscovery**, select a case, and click **Edit** ![Edit icon](media/ebd260e4-3556-4fb0-b0bb-cc489773042c.gif). On the **Exports** page, select an report export, and then click **Download report** in the details pane.</span></span> 
  
## <a name="whats-included-in-the-report"></a><span data-ttu-id="642b3-179">보고서에 포함 된 내용</span><span class="sxs-lookup"><span data-stu-id="642b3-179">What's included in the report</span></span>

<span data-ttu-id="642b3-180">콘텐츠 검색 결과에 대 한 보고서를 생성 하 고 내보내면 다음 문서를 다운로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="642b3-180">When you generate and export a report about the results of a Content Search, the following documents are downloaded:</span></span>
  
- <span data-ttu-id="642b3-p118">**내보내기 요약** -내보내기에 대 한 요약이 포함 된 Excel 문서입니다. 여기에는 검색 된 콘텐츠 원본 수, 각 콘텐츠 위치의 검색 결과 수, 예상 항목 수, 내보낸 항목의 실제 수, 항목의 예상 및 실제 크기 등의 정보가 포함 됩니다. 내보냅니다.</span><span class="sxs-lookup"><span data-stu-id="642b3-p118">**Export Summary** - An Excel document that contains a summary of the export. This includes information such as the number of content sources that were searched, the number of search results from each content location, the estimated number of items, the actual number of items that would be exported, and the estimated and actual size of items that would be exported.</span></span> 
    
    > [!NOTE]
    > <span data-ttu-id="642b3-p119">보고서를 내보낼 때 인덱싱되지 않은 항목을 포함 하면 총 예상 검색 결과 수에 포함 되 고, 검색 결과를 내보낼 때 다운로드 한 검색 결과의 총 수는 다음과 같습니다. 요약 보고서 내보내기 즉, 다운로드 되는 항목의 총 수는 총 예상 결과 수 및 인덱싱되지 않은 항목의 총 수와 같습니다.</span><span class="sxs-lookup"><span data-stu-id="642b3-p119">If you include unindexed items when exporting the report, the number of unindexed items are included in the total number of estimated search results and in the total number of downloaded search results (if you were to export the search results) that are listed in the Export Summary report. In other words, the total number of items that would be downloaded is equal to the total number of estimated results and the total number of unindexed items.</span></span> 
  
- <span data-ttu-id="642b3-185">**manifest** -검색 결과에 포함 된 각 항목에 대 한 정보를 포함 하는 매니페스트 파일 (XML 형식)입니다.</span><span class="sxs-lookup"><span data-stu-id="642b3-185">**Manifest** - A manifest file (in XML format) that contains information about each item included in the search results.</span></span> 
    
- <span data-ttu-id="642b3-p120">**Results** -검색 결과와 함께 내보낼 각 인덱싱된 항목에 대 한 정보가 있는 행이 포함 된 Excel 문서입니다. 전자 메일의 경우 결과 로그에 다음을 비롯 한 각 메시지에 대 한 정보가 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="642b3-p120">**Results** - An Excel document that contains a row with information about each indexed item that would be exported with the search results. For email, the result log contains information about each message, including:</span></span> 
    
  - <span data-ttu-id="642b3-188">원본 사서함에 있는 메시지의 위치 (포함 여부는 주 메시지는 보관 사서함 또는).</span><span class="sxs-lookup"><span data-stu-id="642b3-188">The location of the message in the source mailbox (including whether the message is in the primary or archive mailbox).</span></span>
    
  - <span data-ttu-id="642b3-189">메시지가 전송된 날짜</span><span class="sxs-lookup"><span data-stu-id="642b3-189">The date the message was sent or received.</span></span>
    
  - <span data-ttu-id="642b3-190">메시지의 제목 줄입니다.</span><span class="sxs-lookup"><span data-stu-id="642b3-190">The Subject line from the message.</span></span>
    
  - <span data-ttu-id="642b3-191">보낸 사람 및 메시지 받는 사람입니다.</span><span class="sxs-lookup"><span data-stu-id="642b3-191">The sender and recipients of the message.</span></span>
    
    <span data-ttu-id="642b3-192">SharePoint 및 비즈니스용 OneDrive 사이트의 문서에 대해 결과 로그에는 다음을 비롯 한 각 문서에 대 한 정보가 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="642b3-192">For documents from SharePoint and OneDrive for Business sites, the Results log contains information about each document, including:</span></span>
    
  - <span data-ttu-id="642b3-193">문서에 대 한 URL입니다.</span><span class="sxs-lookup"><span data-stu-id="642b3-193">The URL for the document.</span></span>
    
  - <span data-ttu-id="642b3-194">문서가 있는 사이트 모음의 URL입니다.</span><span class="sxs-lookup"><span data-stu-id="642b3-194">The URL for the site collection where the document is located.</span></span>
    
  - <span data-ttu-id="642b3-195">문서를 마지막으로 수정한 날짜입니다.</span><span class="sxs-lookup"><span data-stu-id="642b3-195">The date that the document was last modified.</span></span>
    
  - <span data-ttu-id="642b3-196">이름 (에 있는 제목 열 결과 로그에서) 문서입니다.</span><span class="sxs-lookup"><span data-stu-id="642b3-196">The name of the document (which is located in the Subject column in the result log).</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="642b3-197">**결과** 보고서의 행 수는 다운로드 되는 총 검색 결과 수에서 **인덱싱되지 않은 항목** 보고서에 나열 되는 총 항목 수를 뺀 값과 같아야 합니다.</span><span class="sxs-lookup"><span data-stu-id="642b3-197">The number of rows in the **Results** report should be equal to the total number of search results that would be downloaded minus the total number of items listed in the **Unindexed Items** report.</span></span> 
  
- <span data-ttu-id="642b3-p121">**인덱싱되지 않은 항목** -검색 결과에 포함 될 인덱싱되지 않은 항목에 대 한 정보가 포함 된 Excel 문서입니다. 검색 결과 보고서를 생성할 때 인덱싱되지 않은 항목을 포함 하지 않으면이 보고서는 계속 다운로드 되지만 비어 있게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="642b3-p121">**Unindexed Items** - An Excel document that contains information about any unindexed items that would be included in the search results. If you don't include unindexed items when you generate the search results report, this report will still be downloaded, but will be empty.</span></span>
