---
title: 콘텐츠 검색 보고서 내보내기
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: article
f1_keywords:
- ms.o365.cc.CustomizeExportReport
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MOE150
- MED150
- MBS150
- MET150
ms.assetid: 5c8c1db6-d8ac-4dbb-8a7a-f65d452169b9
description: Office 365 보안에서 콘텐츠 검색의 실제 결과 내보내기 (영문) 하는 대신 &amp; 준수 센터 하면 검색 결과 보고서를 방금 내보낼 수 있습니다. 보고서의 검색 결과 및이 내보낼 수 있는 각 항목에 대 한 자세한 내용은 사용 하 여 문서 요약을 포함 합니다.
ms.openlocfilehash: e15c6550d58701abe9b268455deca0aef60265fb
ms.sourcegitcommit: 1bc36cd57ab1604f057e2b5d336cf1893ba00125
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/15/2018
ms.locfileid: "27283144"
---
# <a name="export-a-content-search-report"></a><span data-ttu-id="ed998-104">콘텐츠 검색 보고서 내보내기</span><span class="sxs-lookup"><span data-stu-id="ed998-104">Export a Content Search report</span></span>

<span data-ttu-id="ed998-105">검색의 전체 집합 내보내기 (영문) 하는 대신 Office 365 보안 콘텐츠 검색 결과에서 결과 &amp; 준수 센터 (및 eDiscovery 사례와 관련 된 콘텐츠 검색을 통해)을 방금 되는 동일한 보고서를 내보낼 수 있습니다 시 생성 되는 경우 검색 결과 내보냅니다.</span><span class="sxs-lookup"><span data-stu-id="ed998-105">Instead of exporting the full set of search results from a Content Search in the Office 365 Security &amp; Compliance Center (and from a Content Search that's associated with an eDiscovery case), you can just export the same reports that are generated when you export search results.</span></span>
  
<span data-ttu-id="ed998-p102">보고서를 내보낼 때 있는 이름이 같은 콘텐츠 검색 하지만 *_ReportsOnly* 추가 되는 폴더로 다운로드 됩니다. 예, 콘텐츠 검색 *ContosoCase0815* 이름이 이면 보고서 *ContosoCase0815_ReportsOnly* 라는 폴더에 다운로드 됩니다. 보고서에 포함 되는 문서의 목록 [보고서에 포함 된 제품](#whats-included-in-the-report)을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="ed998-p102">When you export a report, it's downloaded to a folder that has the same name as the Content Search, but that's appended with  *_ReportsOnly*  . For example, if the Content Search is named  *ContosoCase0815*  , then the report is downloaded to a folder named  *ContosoCase0815_ReportsOnly*  . For a list of documents that are included in the report, see [What's included in the report](#whats-included-in-the-report).</span></span>

## <a name="before-you-begin"></a><span data-ttu-id="ed998-109">시작하기 전에</span><span class="sxs-lookup"><span data-stu-id="ed998-109">Before you begin</span></span>

- <span data-ttu-id="ed998-p103">Office 365 보안에서 준수 검색 관리 역할을 할당할 수 있는 콘텐츠 검색 보고서를 내보내려면 &amp; 준수 센터입니다. 이 역할은 기본 제공 eDiscovery 관리자 및 조직 관리 역할 그룹에 할당 됩니다. 조직 관리 역할 그룹에 기본적으로 할당 된 되지 않습니다. 자세한 내용은 참조 [Office 365 보안에서 eDiscovery 사용 권한을 할당 &amp; 준수 센터](assign-ediscovery-permissions.md)합니다.</span><span class="sxs-lookup"><span data-stu-id="ed998-p103">To export a Content Search report, you have to be assigned the Compliance Search management role in the Office 365 Security &amp; Compliance Center. This role is assigned to the built-in eDiscovery Manager and Organization Management role groups. It isn't assigned by default to the Organization Management role group. For more information, see [Assign eDiscovery permissions in the Office 365 Security &amp; Compliance Center](assign-ediscovery-permissions.md).</span></span>
    
- <span data-ttu-id="ed998-p104">보고서를 내보낼 때 데이터를 통해 로컬 컴퓨터로 다운로드 되기 전에 일시적으로 Microsoft 클라우드에서 고유한 Windows Azure 저장소 영역에 저장 됩니다. 조직은 Azure의 끝점에 연결할 수 있어야 \*\* \*. blob.core.windows.net\*\* (와일드 카드 내보내기에 대 한 고유 식별자를 나타냄). 검색 결과 데이터를 만든 후 2 주 Azure 저장소 영역에서 삭제 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ed998-p104">When you export a report, the data is temporarily stored in a unique Windows Azure storage area in the Microsoft cloud before it's downloaded to your local computer. Be sure your organization can connect to the endpoint in Azure, which is **\*.blob.core.windows.net** (the wildcard represents a unique identifier for your export). The search results data is deleted from the Azure storage area two weeks after it's created.</span></span> 
    
- <span data-ttu-id="ed998-117">검색 결과를 PST 파일로 내보내는 데 사용하는 컴퓨터는 다음과 같은 시스템 요구 사항을 충족해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ed998-117">The computer you use to export the search results has to meet the following system requirements:</span></span>
    
  - <span data-ttu-id="ed998-118">32비트 및 64비트 버전의 Windows 7 이상 버전


</span><span class="sxs-lookup"><span data-stu-id="ed998-118">32- or 64-bit versions of Windows 7 and later versions</span></span>
    
  - <span data-ttu-id="ed998-119">Microsoft.NET Framework 4.7</span><span class="sxs-lookup"><span data-stu-id="ed998-119">Microsoft .NET Framework 4.7</span></span>
    
  - <span data-ttu-id="ed998-120">지원되는 브라우저:</span><span class="sxs-lookup"><span data-stu-id="ed998-120">A supported browser:</span></span>
    
    - <span data-ttu-id="ed998-121">Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="ed998-121">Microsoft Edge</span></span>
    
      <span data-ttu-id="ed998-122"> 선택하거나 </span><span class="sxs-lookup"><span data-stu-id="ed998-122">or</span></span>
    
    - <span data-ttu-id="ed998-123">Microsoft Internet Explorer 10 및 그 이후 버전</span><span class="sxs-lookup"><span data-stu-id="ed998-123">Microsoft Internet Explorer 10 and later versions</span></span>
    
    <span data-ttu-id="ed998-p105">**참고:** ClickOnce 응용 프로그램에 대 한 추가 기능 사용 또는 제 3 자 확장 Microsoft 제조 하지 않습니다. 제 3 자 확장 또는 추가 기능 지원 되지않는 브라우저를 사용 하 여 검색 결과 내보내기 (영문)이 지원 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ed998-p105">**Note:** Microsoft doesn't manufacture third-party extensions or add-ons for ClickOnce applications. Exporting search results using an unsupported browser with third-party extensions or add-ons isn't supported.</span></span> 

- <span data-ttu-id="ed998-p106">콘텐츠 검색을 통해 반환 된 결과의 예상된 전체 크기는 20 개를 초과 하는 경우&nbsp;TB 보고서 내보내기 실패 합니다. 보고서를 성공적으로 내보내려면 하려고 결과의 예상된 크기는 20 개 미만 되므로 검색을 다시 실행 하 고 범위를 좁힐&nbsp;t B입니다.</span><span class="sxs-lookup"><span data-stu-id="ed998-p106">If the estimated total size of the results returned by a Content Search exceeds 20&nbsp;TB, exporting the report will fail. To successfully export the report, try to narrow the scope and re-run the search so the estimated size of the results is less than 20&nbsp;TB.</span></span>

## <a name="generate-and-download-a-content-search-report"></a><span data-ttu-id="ed998-128">생성 및 콘텐츠 검색 보고서를 다운로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="ed998-128">Generate and download a Content Search report</span></span>

<span data-ttu-id="ed998-129">생성 및 콘텐츠 검색 보고서를 다운로드 하는 단계는 실제로 내보내기 (영문) 검색 결과 매우 유사 합니다.</span><span class="sxs-lookup"><span data-stu-id="ed998-129">The steps to generate and download a Content Search report are very similar to actually exporting search results.</span></span>
  
## <a name="step-1-generate-the-report-for-export"></a><span data-ttu-id="ed998-130">1 단계: 내보내기에 대 한 보고서를 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="ed998-130">Step 1: Generate the report for export</span></span>

<span data-ttu-id="ed998-p107">첫번째 단계에서는 내보내기 하 여 컴퓨터에 다운로드에 대 한 보고서를 준비 하는 것입니다. 클라우드 하면 보고서를 Microsoft에서 Azure 저장소 영역에 문서 업로드 되는 보고서 때입니다.</span><span class="sxs-lookup"><span data-stu-id="ed998-p107">The first step is to prepare the report for downloading to your computer exporting. When you the report, the report documents are uploaded to an Azure storage area in the Microsoft cloud.</span></span>
  
1. <span data-ttu-id="ed998-133">[https://protection.office.com](https://protection.office.com)으로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="ed998-133">Go to [https://protection.office.com](https://protection.office.com).</span></span>
    
2. <span data-ttu-id="ed998-134">회사 또는 학교 계정을 사용하여 Office 365에 로그인합니다.</span><span class="sxs-lookup"><span data-stu-id="ed998-134">Sign in to Office 365 using your work or school account.</span></span>
    
3. <span data-ttu-id="ed998-135">보안 및 준수 센터의 왼쪽 창에서 **검색 및 조사** \> **콘텐츠 검색**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="ed998-135">In the left pane of the Security &amp; Compliance Center, click **Search &amp; investigation** \> **Content search**.</span></span>
    
4. <span data-ttu-id="ed998-136">**콘텐츠 검색** 페이지에서 검색을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="ed998-136">On the **Content search** page, select a search.</span></span> 
    
5. <span data-ttu-id="ed998-137">세부 정보 창에서 **컴퓨터에 보고서 내보내기**에서 **생성 보고서**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="ed998-137">In the details pane, under **Export report to a computer**, click **Generate report**.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="ed998-p108">검색에 대 한 결과 7 일 보다 오래 된 경우 검색 결과 업데이트 하 라는 메시지가 표시 됩니다. 이 경우 내보내기 취소, 클릭 **업데이트 검색 결과** 선택한 검색에 대 한 세부 정보 창에서 한 다음 시작 보고서 내보내기 다시 결과 업데이트 한 후 합니다.</span><span class="sxs-lookup"><span data-stu-id="ed998-p108">If the results for a search are older than 7 days, you are prompted to update the search results. If this happens, cancel the export, click **Update search results** in the details pane for the selected search, and then start the report export again after the results are updated.</span></span> 
  
6. <span data-ttu-id="ed998-140">**검색에서 이러한 항목을 포함**하십시오 아래에서 **보고서 내보내기** 페이지에서 다음 옵션 중 하나를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="ed998-140">On the **Export a report** page, under **Include these items from the search**, choose one of the following options:</span></span>
    
    - <span data-ttu-id="ed998-141">인덱싱된 항목만 내보내기</span><span class="sxs-lookup"><span data-stu-id="ed998-141">Export only indexed items</span></span>
    
    - <span data-ttu-id="ed998-142">인덱싱 및 인덱싱되지 않은 항목 내보내기</span><span class="sxs-lookup"><span data-stu-id="ed998-142">Export indexed and unindexed items</span></span>
    
    - <span data-ttu-id="ed998-143">인덱싱되지 않은 항목만 내보내기</span><span class="sxs-lookup"><span data-stu-id="ed998-143">Export only unindexed items</span></span>
    
    <span data-ttu-id="ed998-144">인덱싱되지 않은 항목에 대 한 자세한 내용은 [부분적으로 인덱싱된 콘텐츠 검색에는 항목을](partially-indexed-items-in-content-search.md)참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="ed998-144">For more information about unindexed items, see [Partially indexed items in Content Search](partially-indexed-items-in-content-search.md).</span></span>
    
7. <span data-ttu-id="ed998-p109">모든 버전의 SharePoint 문서에 대 한 검색 통계를 포함 하도록 선택 합니다. 이 옵션에는 검색의 콘텐츠 원본을 비즈니스 사이트에 대 한 SharePoint 또는 OneDrive를 포함 하는 경우에 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ed998-p109">Choose to include search statistics for all versions of SharePoint documents. This option appears only if the content sources of the search includes SharePoint or OneDrive for Business sites.</span></span>
    
8. <span data-ttu-id="ed998-147">**보고서 생성을**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="ed998-147">Click **Generate report**.</span></span>
    
    <span data-ttu-id="ed998-p110">검색 결과 보고서를 준비 다운로드 하 고, 즉, 보고서 문서를 Microsoft 클라우드 Azure 저장소 영역으로 업로드 됩니다. 보고서 다운로드를 수행할 준비가 되 면 세부 정보 창에서 **보고서 다운로드** 링크를 사용 하는 **컴퓨터에 보고서 내보내기** 에서 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ed998-p110">The search results report is prepared for downloading, which means the report documents will be uploaded to the Azure storage area in the Microsoft cloud. When the report is ready for download, the **Download report** link is displayed under **Export report to a computer** in the details pane.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="ed998-p111">EDiscovery 사례와 관련 된 콘텐츠 검색에 대 한 보고서를 내보낼 수도 있습니다. 이 작업을 수행 하려면로 이동 **검색 &amp; 조사** \> **eDiscovery**사례를 선택 하 고 **편집** 을 클릭 하 ![편집 아이콘](media/ebd260e4-3556-4fb0-b0bb-cc489773042c.gif)합니다. **검색** 페이지에서 검색을 선택 하 고 **내보내기** 를 클릭 한 다음 ![내보내기 검색 결과 아이콘](media/47205c65-babd-4b3a-bd7b-98dfd92883ba.png) \> **보고서를 내보냅니다**.</span><span class="sxs-lookup"><span data-stu-id="ed998-p111">You can also export a report for a Content Search that's associated with an eDiscovery case. To do this, go to **Search &amp; investigation** \> **eDiscovery**, select a case, and click **Edit** ![Edit icon](media/ebd260e4-3556-4fb0-b0bb-cc489773042c.gif). On the **Searches** page, select a search, and then click **Export** ![Export search results icon](media/47205c65-babd-4b3a-bd7b-98dfd92883ba.png) \> **Export a report**.</span></span> 
  
## <a name="step-2-download-the-report"></a><span data-ttu-id="ed998-153">2 단계: 보고서를 다운로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="ed998-153">Step 2: Download the report</span></span>

<span data-ttu-id="ed998-154">다음 단계를 통해 로컬 컴퓨터로 Azure 저장소 영역에서 보고서를 다운로드 하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="ed998-154">The next step is to download the report from the Azure storage area to your local computer.</span></span>
  
1. <span data-ttu-id="ed998-155">**컴퓨터에 보고서 내보내기**에서에 대 한 보고서를 생성 하는 검색에 대 한 세부 정보 창에서 **보고서 다운로드**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="ed998-155">In the details pane for the search that you generated the report for, under **Export report to a computer**, click **Download report**.</span></span>
    
    <span data-ttu-id="ed998-156">**보고서 다운로드** 페이지가 표시 되 고 다음을 포함까지 보고서에 대 한 정보는 사용자의 컴퓨터에 다운로드할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ed998-156">The **Download report** page is displayed and contains the following information about the report till be downloaded to your computer.</span></span> 
    
    - <span data-ttu-id="ed998-157">다운로드될 항목의 수</span><span class="sxs-lookup"><span data-stu-id="ed998-157">The number of items that will be downloaded.</span></span>
    
    - <span data-ttu-id="ed998-158">다운로드될 항목의 예상 총 크기</span><span class="sxs-lookup"><span data-stu-id="ed998-158">The estimated total size of the items that will be downloaded.</span></span>
    
    - <span data-ttu-id="ed998-p112">인덱싱된 또는 인덱싱되지 않은 있는지 여부를 내보냅니다. 인덱싱되지 않은 항목은를 인식 된 형식, 암호화 된 또는 다른 이유로 인덱싱된 받지 된 항목입니다.</span><span class="sxs-lookup"><span data-stu-id="ed998-p112">Whether indexed or unindexed will be exported. Unindexed items are items that have an recognized format, are encrypted, or weren't indexed for other reasons.</span></span>
    
    - <span data-ttu-id="ed998-161">SharePoint 문서의 버전을 다운로드할지 여부</span><span class="sxs-lookup"><span data-stu-id="ed998-161">Whether or not versions of SharePoint documents will be downloaded.</span></span>
    
    - <span data-ttu-id="ed998-p113">상태 보고서 내보내기 프로세스입니다. 보고서를 다운로드 하 여 보고서의 준비 완전 하지 않은 경우에 시작할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ed998-p113">The status of the report export process. You can start downloading the report even if the preparation of the report isn't complete.</span></span>
    
2. <span data-ttu-id="ed998-p114">**키를 내보낼**에서 **클립보드에 복사**를 클릭 합니다. 5 단계에서이 키를 사용 하 여 보고서를 다운로드 하려면 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ed998-p114">Under **Export key**, click **Copy to clipboard**. You will use this key in step 5 to download the report.</span></span>
    
    > [!IMPORTANT]
    > <span data-ttu-id="ed998-166">설치 하 고 eDiscovery 내보내기 도구를 시작 하 고 다음이 키를 사용 하 여 검색 보고서를 다운로드할 수 누구나, 때문에 암호 또는 기타 보안 관련 정보를 보호 하는 것 처럼이 키를 보호 하기 위한 예방 조치를 수행 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ed998-166">Because anyone can install and start the eDiscovery Export tool, and then use this key to download the search report, be sure to take precautions to protect this key just like you would protect passwords or other security-related information.</span></span> 
  
3. <span data-ttu-id="ed998-167">**보고서 다운로드**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="ed998-167">Click **Download report**.</span></span>
    
4. <span data-ttu-id="ed998-168">**MicrosoftOffice 365 eDiscovery 내보내기 도구를**설치 하 라는 메시지가 표시를 하는 경우에 **설치**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="ed998-168">If you're prompted to install the **MicrosoftOffice 365 eDiscovery Export Tool**, click **Install**.</span></span>
    
5. <span data-ttu-id="ed998-169">**eDiscovery 내보내기 도구**에서 5단계에서 복사한 내보내기 키를 해당 상자에 붙여 넣습니다. </span><span class="sxs-lookup"><span data-stu-id="ed998-169">In the **eDiscovery Export Tool**, paste the export key that you copied in step 2 in the appropriate box.</span></span>
    
6. <span data-ttu-id="ed998-170">보고서를 다운로드 하려면 위치를 지정 하려면 **찾아보기** 를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="ed998-170">Click **Browse** to specify the location where you want to download the report.</span></span> 
    
7. <span data-ttu-id="ed998-171">**시작**을 클릭하여 컴퓨터에 검색 결과를 다운로드합니다.</span><span class="sxs-lookup"><span data-stu-id="ed998-171">Click **Start** to download the search results to your computer.</span></span> 
    
    <span data-ttu-id="ed998-p115">**EDiscovery 내보내기 도구** 수 (및 크기)의 나머지 항목을 다운로드할 수 있는 예상을 포함 하는 내보내기 프로세스에 대 한 상태 정보를 표시 합니다. 내보내기 프로세스가 완료 되 면 파일 다운로드 한 있는 위치에 액세스할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ed998-p115">The **eDiscovery Export Tool** displays status information about the export process, including an estimate of the number (and size) of the remaining items to be downloaded. When the export process is complete, you can access the files in the location where they were downloaded.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="ed998-p116">EDiscovery 사례와 관련 된 콘텐츠 검색에 대 한 보고서를 다운로드할 수 있습니다. 이 작업을 수행 하려면로 이동 **검색 &amp; 조사** \> **eDiscovery**사례를 선택 하 고 **편집** 을 클릭 하 ![편집 아이콘](media/ebd260e4-3556-4fb0-b0bb-cc489773042c.gif)합니다. **내보내기** 페이지에서 보고서 내보내기를 선택한 다음 세부 정보 창에서 **보고서 다운로드** 를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="ed998-p116">You can download the report for a Content Search that's associated with an eDiscovery case. To do this, go to **Search &amp; investigation** \> **eDiscovery**, select a case, and click **Edit** ![Edit icon](media/ebd260e4-3556-4fb0-b0bb-cc489773042c.gif). On the **Exports** page, select an report export, and then click **Download report** in the details pane.</span></span> 
  
## <a name="whats-included-in-the-report"></a><span data-ttu-id="ed998-177">보고서에 포함 된 제품</span><span class="sxs-lookup"><span data-stu-id="ed998-177">What's included in the report</span></span>

<span data-ttu-id="ed998-178">생성 하 고 콘텐츠 검색의 결과 대 한 보고서를 내보낼 때 다음 문서는 다운로드 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ed998-178">When you generate and export a report about the results of a Content Search, the following documents are downloaded:</span></span>
  
- <span data-ttu-id="ed998-p117">**요약 내보내기** -내보내기의 요약을 포함 하는 Excel 문서입니다. 검색 된 콘텐츠 원본 수, 각 콘텐츠 위치, 예상된 항목 수,이 내보낼 수, 항목의 실제 번호에서 검색 결과의 수 및 항목의 예상 및 실제 크기와 같은 정보를 포함 됩니다. 내보낼 수는 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ed998-p117">**Export Summary** - An Excel document that contains a summary of the export. This includes information such as the number of content sources that were searched, the number of search results from each content location, the estimated number of items, the actual number of items that would be exported, and the estimated and actual size of items that would be exported.</span></span> 
    
    > [!NOTE]
    > <span data-ttu-id="ed998-p118">인덱싱되지 않은 항목 수에 나열 된 다운로드 한 검색 결과 (한다고 가정해봅니다. 검색 결과를 내보내려면) 하는 경우의 총 수 및 예상된 검색 결과의 총 수에 포함 된 보고서를 내보낼 때 인덱싱되지 않은 항목을 포함 하는 경우는 요약 보고서를 내보냅니다. 즉,이 다운로드할 수 있는 항목의 총 수는 예상된 결과의 총 수와 인덱싱되지 않은 항목의 총 수와 같은 합니다.</span><span class="sxs-lookup"><span data-stu-id="ed998-p118">If you include unindexed items when exporting the report, the number of unindexed items are included in the total number of estimated search results and in the total number of downloaded search results (if you were to export the search results) that are listed in the Export Summary report. In other words, the total number of items that would be downloaded is equal to the total number of estimated results and the total number of unindexed items.</span></span> 
  
- <span data-ttu-id="ed998-183">**매니페스트** -검색 결과에 포함 된 각 항목에 대 한 정보를 포함 하는 XML 형식으로 매니페스트 파일.</span><span class="sxs-lookup"><span data-stu-id="ed998-183">**Manifest** - A manifest file (in XML format) that contains information about each item included in the search results.</span></span> 
    
- <span data-ttu-id="ed998-p119">**결과** -검색 결과 함께 내보낼 각 인덱싱된 항목에 대 한 정보가 포함 된 행이 포함 된 Excel 문서입니다. 전자 메일, 결과 로그 각 메시지에 대 한 정보가 들어 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="ed998-p119">**Results** - An Excel document that contains a row with information about each indexed item that would be exported with the search results. For email, the result log contains information about each message, including:</span></span> 
    
  - <span data-ttu-id="ed998-186">원본 사서함에 있는 메시지의 위치 (포함 여부는 주 메시지는 보관 사서함 또는).</span><span class="sxs-lookup"><span data-stu-id="ed998-186">The location of the message in the source mailbox (including whether the message is in the primary or archive mailbox).</span></span>
    
  - <span data-ttu-id="ed998-187">메시지가 전송된 날짜</span><span class="sxs-lookup"><span data-stu-id="ed998-187">The date the message was sent or received.</span></span>
    
  - <span data-ttu-id="ed998-188">메시지의 제목 줄입니다.</span><span class="sxs-lookup"><span data-stu-id="ed998-188">The Subject line from the message.</span></span>
    
  - <span data-ttu-id="ed998-189">보낸 사람 및 메시지 받는 사람입니다.</span><span class="sxs-lookup"><span data-stu-id="ed998-189">The sender and recipients of the message.</span></span>
    
    <span data-ttu-id="ed998-190">SharePoint와 OneDrive에서 비즈니스 사이트에 대 한 문서에 대 한 결과 로그는 각 문서에 대 한 정보를 포함 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="ed998-190">For documents from SharePoint and OneDrive for Business sites, the Results log contains information about each document, including:</span></span>
    
  - <span data-ttu-id="ed998-191">문서에 대 한 URL입니다.</span><span class="sxs-lookup"><span data-stu-id="ed998-191">The URL for the document.</span></span>
    
  - <span data-ttu-id="ed998-192">문서가 있는 사이트 모음의 URL입니다.</span><span class="sxs-lookup"><span data-stu-id="ed998-192">The URL for the site collection where the document is located.</span></span>
    
  - <span data-ttu-id="ed998-193">문서를 마지막으로 수정한 날짜입니다.</span><span class="sxs-lookup"><span data-stu-id="ed998-193">The date that the document was last modified.</span></span>
    
  - <span data-ttu-id="ed998-194">이름 (에 있는 제목 열 결과 로그에서) 문서입니다.</span><span class="sxs-lookup"><span data-stu-id="ed998-194">The name of the document (which is located in the Subject column in the result log).</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="ed998-195">**결과** 보고서의 행 수가 **인덱싱되지 않은 항목** 보고서에 나열 된 항목의 총 수를 뺀 결과값을 다운로드할 수는 검색 결과의 총 수와 동일 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ed998-195">The number of rows in the **Results** report should be equal to the total number of search results that would be downloaded minus the total number of items listed in the **Unindexed Items** report.</span></span> 
  
- <span data-ttu-id="ed998-p120">**인덱싱되지 않은 항목** -검색 결과에 포함 되는 모든 인덱싱되지 않은 항목에 대 한 정보가 포함 된 Excel 문서입니다. 검색 결과 보고서를 생성 하는 경우에 인덱싱되지 않은 항목을 포함 하지 않으면 하는 경우이 보고서 다운로드 여전히 됩니다 있지만 비어 있게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ed998-p120">**Unindexed Items** - An Excel document that contains information about any unindexed items that would be included in the search results. If you don't include unindexed items when you generate the search results report, this report will still be downloaded, but will be empty.</span></span>
