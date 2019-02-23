---
title: Office 365 고급 eDiscovery 검색 결과 준비
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: article
f1_keywords:
- ms.o365.cc.CustomizeExportWithZoom
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid: MOE150
ms.assetid: 0b6fac2d-8627-4b05-9df0-03609db6248b
description: 고급 eDiscovery 도구로 추가 분석을 위해 Office 365 보안 &amp; 및 준수 센터에서 콘텐츠 검색의 결과를 준비 하는 방법을 알아봅니다.
ms.openlocfilehash: 52573169692c2457e51898f9f36d2c586c7e7a4b
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30212678"
---
# <a name="prepare-search-results-for-office-365-advanced-ediscovery"></a><span data-ttu-id="c70ce-103">Office 365 고급 eDiscovery 검색 결과 준비</span><span class="sxs-lookup"><span data-stu-id="c70ce-103">Prepare search results for Office 365 Advanced eDiscovery</span></span>

<span data-ttu-id="c70ce-p101">office 365 보안 &amp; 및 준수 센터에서 eDiscovery 사례와 관련 된 검색을 성공적으로 실행 한 후에는 검색 결과를 준비 하 여 더 많은 분석을 수행할 수 있는 office 365 Advanced eDiscovery를 사용 하 여 구조화 되지 않은 데이터를 설정 하 고 법적 사례와 관련 된 데이터의 양을 줄입니다. 고급 eDiscovery 기능에는 다음이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c70ce-p101">After a search that's associated with an eDiscovery case in the Office 365 Security &amp; Compliance Center is successfully run, you can prepare the search results for further analysis with Office 365 Advanced eDiscovery, which lets you analyze large, unstructured data sets and reduce the amount of data that's relevant to a legal case. Advanced eDiscovery features include:</span></span>
  
- <span data-ttu-id="c70ce-p102">**광학 인식** -고급 eDiscovery에 대 한 검색 결과를 준비할 때 OCR (광학 인식) 기능은 이미지에서 텍스트를 자동으로 추출 하며 여기에 로드 된 검색 결과를 포함 합니다. 고급 eDiscovery for analysis OCR은 느슨한 파일, 전자 메일 첨부 파일 및 포함 된 이미지에 대해 지원 됩니다. 이를 통해 이미지 파일의 텍스트 콘텐츠에 고급 eDiscovery (근거리 복제, 전자 메일 스레딩, 테마 및 예측 코딩)의 텍스트 분석 기능을 적용할 수 있습니다. Advanced eDiscovery OCR은 다음과 같은 이미지 파일 형식을 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c70ce-p102">**Optical character recognition** - When you prepare search results for Advanced eDiscovery, optical character recognition (OCR) functionality automatically extracts text from images, and includes this with the search results that are loaded in to Advanced eDiscovery for analysis. OCR is supported for loose files, email attachments, and embedded images. This allows you to apply the text analytic capabilities of Advanced eDiscovery (near-duplicates, email threading, themes, and predictive coding) to the text content in image files. Advanced eDiscovery OCR supports the following formats for image files:</span></span>

    - <span data-ttu-id="c70ce-110">GIF</span><span class="sxs-lookup"><span data-stu-id="c70ce-110">GIF</span></span>
    - <span data-ttu-id="c70ce-111">JPEG</span><span class="sxs-lookup"><span data-stu-id="c70ce-111">JPEG</span></span>
    - <span data-ttu-id="c70ce-112">.jpg</span><span class="sxs-lookup"><span data-stu-id="c70ce-112">JPG</span></span>
    - <span data-ttu-id="c70ce-113">PNG</span><span class="sxs-lookup"><span data-stu-id="c70ce-113">PNG</span></span>
    - <span data-ttu-id="c70ce-114">TIFF</span><span class="sxs-lookup"><span data-stu-id="c70ce-114">TIFF</span></span>
    
- <span data-ttu-id="c70ce-p103">유사 **중복 검색** -데이터 검토를 보다 효율적으로 구성할 수 있으므로 한 명의 사용자가 비슷한 문서 그룹을 검토 합니다. 이렇게 하면 여러 명의 검토자가 같은 문서의 다른 버전을 볼 필요가 없습니다.</span><span class="sxs-lookup"><span data-stu-id="c70ce-p103">**Near-duplicate detection** - Lets you structure your data review more efficiently, so one person reviews a group of similar documents. This helps prevent multiple reviewers from having to view different versions of the same document.</span></span> 
    
- <span data-ttu-id="c70ce-p104">**전자 메일 스레딩** -전자 메일 스레드에서 고유한 메시지를 식별 하 여 각 메시지의 새 정보에만 집중할 수 있도록 도와줍니다. 전자 메일 스레드에서 두 번째 메시지에는 첫 번째 메시지가 포함 됩니다. 마찬가지로 나중에 메시지는 모두 이전 메시지를 포함 합니다. 전자 메일 스레딩은 전자 메일 스레드에서 모든 메시지를 검토할 필요가 없습니다.</span><span class="sxs-lookup"><span data-stu-id="c70ce-p104">**Email threading** - Helps you identify the unique messages in an email thread so you can focus on only the new information in each message. In an email thread, the second message contains the first message. Likewise, later messages contain all the previous messages. Email threading removes the need to review every message in its entirety in an email thread.</span></span> 
    
- <span data-ttu-id="c70ce-p105">**Themes** -키워드 검색 통계 외에 데이터에 대 한 중요 한 정보를 얻을 수 있도록 지원 합니다. 컨텍스트에서 문서를 볼 수 있도록 관련 문서를 그룹화 하 여 조사를 지원 합니다. 테마를 사용 하는 경우 문서 집합에 대 한 관련 테마를 보고, 겹치기를 결정 한 다음 관련 데이터의 여러 섹션을 식별할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c70ce-p105">**Themes** - Help you get valuable insight about your data beyond just keyword search statistics. Themes help investigations by grouping related documents so you can look at the documents in context. When using themes, you can view the related themes for a set of documents, determine any overlap, and then identify cross-sections of related data.</span></span> 
    
- <span data-ttu-id="c70ce-p106">**예측 코딩** -소수의 문서 집합에 대 한 결정을 내릴 수 있도록 하 여 원하는 내용을 시스템에 교육할 수 있습니다. 그러면 고급 eDiscovery가 데이터 집합의 모든 문서를 분석할 때 지침을 기반으로 하 여 해당 학습을 적용 합니다. 이 학습에 따라 Advanced eDiscovery는 사례와 관련이 있을 가능성이 가장 높은 문서에 따라 검토할 문서를 결정할 수 있도록 관련성 순위를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="c70ce-p106">**Predictive coding** - Lets you train the system on what you're looking for, by allowing you to make decisions (about whether something is relevant or not) on a small set of documents. Advanced eDiscovery then applies that learning (based on your guidance) when analyzing all of the documents in the data set. Based on that learning, Advanced eDiscovery provides a relevance ranking so you can decide which documents to review based on what document are the most likely to be relevant to the case.</span></span> 
    
- <span data-ttu-id="c70ce-p107">**검토 응용 프로그램에 대 한 데이터 내보내기** -분석을 완료 하 고 데이터 집합을 줄이고 나면 고급 eDiscovery 및 Office 365에서 데이터를 내보낼 수 있습니다. 내보내기 패키지에는 내보낸 콘텐츠 및 analytics 메타 데이터의 속성을 포함 하는 CSV 파일이 포함 됩니다. 내보낸 패키지는 eDiscovery 검토 응용 프로그램으로 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c70ce-p107">**Exporting data for review applications**  - You can export data from Advanced eDiscovery and Office 365 after you've completed your analysis and reduced the data set. The export package includes a CSV file that contains the properties from the exported content and analytics metadata. This export package can then be imported to an eDiscovery review application.</span></span> 
    
## <a name="before-you-begin"></a><span data-ttu-id="c70ce-130">시작하기 전에</span><span class="sxs-lookup"><span data-stu-id="c70ce-130">Before you begin</span></span>

- <span data-ttu-id="c70ce-p108">고급 eDiscovery를 사용 하 여 사용자 데이터를 분석 하려면 데이터의 custodian 사용자에 게 Office 365 E5 라이선스를 할당 해야 합니다. 또는 Office 365 E1 또는 E3 라이선스를 사용 하는 사용자에 게 고급 eDiscovery 독립 실행형 라이선스를 할당할 수 있습니다. 서비스 케이스에 할당 되 고 고급 eDiscovery를 사용 하 여 데이터를 분석 하는 관리자 및 규정 준수 직원은 E5 라이선스가 필요 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c70ce-p108">To analyze a user's data using Advanced eDiscovery, the user (the custodian of the data) must be assigned an Office 365 E5 license. Alternatively, users with an Office 365 E1 or E3 license can be assigned an Advanced eDiscovery standalone license. Administrators and compliance officers who are assigned to cases and use Advanced eDiscovery to analyze data don't need an E5 license.</span></span> 
    
- <span data-ttu-id="c70ce-p109">고급 eDiscovery에 대 한 검색 결과를 준비 하려면 ediscovery 관리자 또는 Office 365 보안 &amp; 및 준수 센터의 ediscovery 관리자 여야 합니다. ediscovery 관리자는 ediscovery 관리자 역할 그룹의 구성원 이어야 합니다. ediscovery 관리자는 ediscovery 관리자 역할 그룹의 구성원 일 수도 있지만 추가 ediscovery 권한이 할당 되었습니다. ediscovery 관리자 권한을 할당 하는 방법에 대 한 자세한 내용은 [Office 365 Security & 준수 센터의 ediscovery 사례](ediscovery-cases.md#step-1-assign-ediscovery-permissions-to-potential-case-members)에서 1 단계를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="c70ce-p109">You have to be an eDiscovery Manager or an eDiscovery Administrator in the Office 365 Security &amp; Compliance Center to prepare search results for Advanced eDiscovery. An eDiscovery Manager is a member of the eDiscovery Manager role group. An eDiscovery Administrator is also member of the eDiscovery Manager role group, but has been assigned additional eDiscovery privileges. For instructions about assigning eDiscovery Administrator permissions, see Step 1 in [eDiscovery cases in the Office 365 Security & Compliance Center](ediscovery-cases.md#step-1-assign-ediscovery-permissions-to-potential-case-members).</span></span>
    
## <a name="step-1-prepare-search-results-for-advanced-ediscovery"></a><span data-ttu-id="c70ce-138">1 단계: 고급 eDiscovery에 대 한 검색 결과 준비</span><span class="sxs-lookup"><span data-stu-id="c70ce-138">Step 1: Prepare search results for Advanced eDiscovery</span></span>

<span data-ttu-id="c70ce-p110">eDiscovery 사례와 연결 된 검색의 결과를 준비할 수 있습니다. 고급 eDiscovery에 대 한 검색 결과를 준비 하면 데이터가 업로드 되 고 임시로 Microsoft 클라우드의 고유한 Windows Azure 저장소 영역에 저장 됩니다. 이 시점에서 OCR 기능은 검색 결과의 이미지에서 텍스트를 추출 합니다. [2 단계](#step-2-add-the-search-results-data-to-the-case-in-advanced-ediscovery)에서이 텍스트와 기타 검색 결과 데이터는 고급 eDiscovery의 사례에 로드 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c70ce-p110">You can prepare the results of a search that's associated with an eDiscovery case. When you prepare search results for Advanced eDiscovery, the data is uploaded and temporarily stored in a unique Windows Azure storage area in the Microsoft cloud. It's at this point that the OCR functionality extracts text from images in the search results. In [Step 2](#step-2-add-the-search-results-data-to-the-case-in-advanced-ediscovery), this text and the other search results data is loaded in to the case in Advanced eDiscovery.</span></span>
  
1. <span data-ttu-id="c70ce-143">보안 및 준수 센터에서 **검색 &amp; 조사** \> **eDiscovery**를 클릭하여 조직의 사례 목록을 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="c70ce-143">In the Security &amp; Compliance Center, click **Search &amp; investigation** \> **eDiscovery** to display the list of cases in your organization.</span></span> 
    
2. <span data-ttu-id="c70ce-144">고급 eDiscovery에서 분석에 대 한 검색 결과를 준비 하려는 사례 옆에 있는 **열기** 를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="c70ce-144">Click **Open** next to the case that you want to prepare search results for analysis in Advanced eDiscovery.</span></span> 
    
3. <span data-ttu-id="c70ce-145">사례에 대 한 **홈** 페이지에서 **검색**을 클릭 하 고 검색을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="c70ce-145">On the **Home** page for the case, click **Search**, and then select the search.</span></span>
    
4. <span data-ttu-id="c70ce-146">세부 정보 창의 **고급 eDiscovery를 사용한 결과 분석**에서 **분석 결과 준비**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="c70ce-146">In the details pane, under **Analyze results with Advanced eDiscovery**, click **Prepare results for analysis**.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="c70ce-147">검색 결과가 7일보다 오래된 경우 검색을 다시 시작하여 검색 결과를 새로 고치라는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="c70ce-147">If the search results are older than 7 days, you will be prompted to update the search results.</span></span> 
  
5. <span data-ttu-id="c70ce-148">**결과 분석 준비** 페이지에서 다음을 수행합니다. </span><span class="sxs-lookup"><span data-stu-id="c70ce-148">On the **Prepare results for analysis** page, do the following:</span></span> 
    
    - <span data-ttu-id="c70ce-149">고급 eDiscovery에서 분석을 위해 인덱싱된 항목, 인덱싱된 및 인덱싱되지 않은 항목 또는 인덱싱되지 않은 항목만 준비 하도록 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="c70ce-149">Choose to prepare indexed items, indexed and unindexed items, or only unindexed items for analysis in Advanced eDiscovery.</span></span>
    
    - <span data-ttu-id="c70ce-p111">SharePoint에서 찾은 검색 조건을 충족 하는 모든 버전의 문서를 포함할지 여부를 선택 합니다. 이 옵션은 검색에 대 한 콘텐츠 원본에 사이트가 포함 되는 경우에만 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c70ce-p111">Choose whether to include all versions of documents found on SharePoint that met the search criteria. This option appears only if the content sources for the search includes sites.</span></span>
    
    - <span data-ttu-id="c70ce-152">준비 프로세스가 완료 되 고 데이터를 고급 eDiscovery에서 처리할 준비가 된 경우 사용자에 게 알림 메시지를 전송 (또는 복사) 할 지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c70ce-152">Specify whether you want a notification message sent (or copied) to a person when the preparation process is completed and the data is ready to be processed in Advanced eDiscovery.</span></span>
    
6. <span data-ttu-id="c70ce-153">**준비**를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="c70ce-153">Click **Prepare**.</span></span>
    
    <span data-ttu-id="c70ce-154">고급 eDiscovery를 사용 하 여 분석을 위해 검색 결과를 준비 합니다.</span><span class="sxs-lookup"><span data-stu-id="c70ce-154">The search results are prepared for analysis with Advanced eDiscovery.</span></span>
    
7. <span data-ttu-id="c70ce-p112">세부 정보 창에서 **준비 상태 확인** 을 클릭 하 여 준비 프로세스에 대 한 정보를 표시 합니다. 준비 프로세스가 완료 되 면 Advanced eDiscovery의 사례를 방문 하 여 분석을 위해 데이터를 처리할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c70ce-p112">In the details pane, click **Check preparation status** to display information about the preparation process. When the preparation process is finished, you can go to the case in Advanced eDiscovery to process the data for analysis.</span></span> 
    
## <a name="step-2-add-the-search-results-data-to-the-case-in-advanced-ediscovery"></a><span data-ttu-id="c70ce-157">2 단계: Advanced eDiscovery의 사례에 검색 결과 데이터 추가</span><span class="sxs-lookup"><span data-stu-id="c70ce-157">Step 2: Add the search results data to the case in Advanced eDiscovery</span></span>
<span data-ttu-id="c70ce-158"><a name="step2"> </a></span><span class="sxs-lookup"><span data-stu-id="c70ce-158"></span></span>

<span data-ttu-id="c70ce-p113">준비가 완료 되 면 다음 단계는 advanced ediscovery로 이동한 후 검색 결과 데이터 (Microsoft 클라우드의 Azure storage 영역에 업로드 된)를 advanced ediscovery의 사례에 로드 하는 것입니다. 앞에서 설명한 것 처럼 고급 ediscovery에 액세스 하려면 보안 &amp; 준수 센터의 eDiscovery 관리자 이거나 고급 ediscovery의 관리자 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c70ce-p113">When the preparation is finished, the next step is to go to Advanced eDiscovery and load the search results data (which have been uploaded to an Azure storage area in the Microsoft cloud ) to the case in Advanced eDiscovery. As previously explained, to access Advanced eDiscovery you have to be an eDiscovery Administrator in the Security &amp; Compliance Center or an administrator in Advanced eDiscovery.</span></span>
  
> [!NOTE]
> <span data-ttu-id="c70ce-161">보안 &amp; 준수 센터의 데이터를 고급 eDiscovery의 사례에 추가 하는 데 걸리는 시간은 eDiscovery 검색 결과의 크기에 따라 달라 집니다.</span><span class="sxs-lookup"><span data-stu-id="c70ce-161">The time it takes for the data from the Security &amp; Compliance Center to be available to add to a case in Advanced eDiscovery varies, depending on the size of the results from the eDiscovery search.</span></span> 
  
1. <span data-ttu-id="c70ce-162">보안 및 준수 센터에서 **검색 &amp; 조사** \> **eDiscovery**를 클릭하여 조직의 사례 목록을 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="c70ce-162">In the Security &amp; Compliance Center, click **Search &amp; investigation** \> **eDiscovery** to display the list of cases in your organization.</span></span> 
    
2. <span data-ttu-id="c70ce-163">고급 eDiscovery에서 데이터를 로드 하려는 사례 옆에 있는 **열기** 를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="c70ce-163">Click **Open** next to the case that you want to load data in to in Advanced eDiscovery.</span></span> 
    
3. <span data-ttu-id="c70ce-164">사례에 대한 **홈** 페이지에서 **Advanced eDiscovery**를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="c70ce-164">On the **Home** page for the case, click **Advanced eDiscovery**.</span></span> 
    
    ![advanced ediscovery로 전환을 클릭 하 여 advanced ediscovery의 케이스 열기](media/8e34ba23-62e3-4e68-a530-b6ece39b54be.png)
  
    <span data-ttu-id="c70ce-p114">**고급 eDiscovery 진행률 표시줄에 연결 하** 는 중입니다. 고급 eDiscovery에 연결 되어 있는 경우 서비스 케이스의 설정 페이지에 컨테이너 목록이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c70ce-p114">The **Connecting to Advanced eDiscovery** progress bar is displayed. When you're connected to Advanced eDiscovery, a list of containers is displayed on the setup page for the case.</span></span> 
    
    ![이 사례는 Advanced eDiscovery에 표시 됩니다.](media/8036e152-70dc-4bb7-9379-61c1ed8326b4.png)
  
     <span data-ttu-id="c70ce-p115">이러한 컨테이너는 1 단계에서 고급 eDiscovery를 분석 하기 위해 준비한 검색 결과를 나타냅니다. 컨테이너의 이름은 보안 &amp; 및 준수 센터의 사례에 있는 검색과 이름이 같습니다. 이 목록에는 사용자가 준비한 컨테이너 들이 나열 됩니다. 다른 사용자가 고급 eDiscovery를 위해 준비 된 검색 결과를 사용 하는 경우 해당 컨테이너가 목록에 포함 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c70ce-p115">These containers represent the search results that you prepared for analysis in Advanced eDiscovery in Step 1. Note that the name of the container has the same name as the search in the case in the Security &amp; Compliance Center. The containers in the list are the ones that you prepared. If a different user prepared search results for Advanced eDiscovery, the corresponding containers won't be included in the list.</span></span> 
    
4. <span data-ttu-id="c70ce-173">컨테이너의 검색 결과 데이터를 Advanced eDiscovery의 사례에 로드 하려면 컨테이너를 선택 하 고 **처리**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="c70ce-173">To load the search result data from a container in to the case in Advanced eDiscovery, select a container and then click **Process**.</span></span>
    
## <a name="next-steps"></a><span data-ttu-id="c70ce-174">다음 단계</span><span class="sxs-lookup"><span data-stu-id="c70ce-174">Next steps</span></span>

<span data-ttu-id="c70ce-p116">eDiscovery 검색의 결과를 사례에 추가한 후에는 고급 eDiscovery 도구를 사용 하 여 데이터를 분석 하 고 특정 법적 사례에 대응 되는 콘텐츠를 식별 합니다. 고급 ediscovery를 사용 하는 방법에 대 한 자세한 내용은 [Office 365 Advanced eDiscovery](office-365-advanced-ediscovery.md)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="c70ce-p116">After the results of an eDiscovery search are added to a case, the next step is to use the Advanced eDiscovery tools to analyze the data and identify the content that's responsive to a specific legal case. For information about using Advanced eDiscovery, see [Office 365 Advanced eDiscovery](office-365-advanced-ediscovery.md).</span></span>
  
## <a name="more-information"></a><span data-ttu-id="c70ce-177">추가 정보</span><span class="sxs-lookup"><span data-stu-id="c70ce-177">More information</span></span>

<span data-ttu-id="c70ce-p117">검색 결과에 포함 된 모든 RMS 암호화 전자 메일 메시지는 고급 eDiscovery에서 분석을 위해 준비할 때 암호가 해독 됩니다. 이 암호 해독 기능은 eDiscovery 관리자 역할 그룹의 구성원에 대해 기본적으로 사용 하도록 설정 됩니다. RMS 암호 해독 관리 역할이이 역할 그룹에 할당 되었기 때문입니다. 전자 메일 메시지의 암호 해독에 대해서는 다음 사항을 염두에 두어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c70ce-p117">Any RMS-encrypted email messages that are included in the search results will be decrypted when you prepare them for analysis in Advanced eDiscovery. This decryption capability is enabled by default for members of the eDiscovery Manager role group. This is because the RMS Decrypt management role is assigned to this role group. Keep the following things in mind about decrypting email messages:</span></span>
  
- <span data-ttu-id="c70ce-p118">현재이 암호 해독 기능에는 SharePoint 및 비즈니스용 OneDrive 사이트의 암호화 된 콘텐츠가 포함 되지 않습니다. RMS 암호화 전자 메일 메시지만 내보낼 때 암호가 해독 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c70ce-p118">Currently, this decryption capability doesn't include encrypted content from SharePoint and OneDrive for Business sites. Only RMS-encrypted email messages will be decrypted when you export them.</span></span>
    
- <span data-ttu-id="c70ce-184">RMS 암호화 전자 메일 메시지에 암호화 된 첨부 파일 (예: 문서 또는 다른 전자 메일 메시지)이 있는 경우 최상위 전자 메일 메시지만 해독 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c70ce-184">If an RMS-encrypted email message has an attachment (such as a document or another email message) that's also encrypted, only the top-level email message will be decrypted.</span></span>
    
- <span data-ttu-id="c70ce-p119">고급 eDiscovery에서 분석에 대 한 검색 결과를 준비할 때 누군가 RMS 암호화 메시지의 암호를 해독할 수 없도록 하려면 기본 제공 ediscovery 관리자 역할 그룹을 복사 하 여 사용자 지정 역할 그룹을 만든 다음 RMS를 제거 해야 합니다. 사용자 지정 역할 그룹에서 관리 역할의 암호를 해독 합니다. 그런 다음 메시지의 암호를 해독 하지 않으려는 사용자를 사용자 지정 역할 그룹의 구성원으로 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="c70ce-p119">If you need to prevent someone from decrypting RMS-encrypted messages when preparing search results for analysis in Advanced eDiscovery, you'll have to create a custom role group (by copying the built-in eDiscovery Manager role group) and then remove the RMS Decrypt management role from the custom role group. Then add the person who you don't want to decrypt messages as a member of the custom role group.</span></span>
