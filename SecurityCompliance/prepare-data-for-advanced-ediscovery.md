---
title: Office 365 Advanced eDiscovery에 대한 데이터 준비
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
ms.assetid: 2fb94c23-1846-4a0e-994d-da6d02445f15
description: 'Office 365 보안을 사용 하는 방법에 알아봅니다 &amp; 준수 센터 Office 365 고급 eDiscovery 사용 하 여 분석을 위해 Office 365 데이터를 준비 합니다. '
ms.openlocfilehash: cf0c76b0c274121da435de7829c769abf5111cab
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22533892"
---
# <a name="prepare-data-for-office-365-advanced-ediscovery"></a><span data-ttu-id="1e941-103">Office 365 Advanced eDiscovery에 대한 데이터 준비</span><span class="sxs-lookup"><span data-stu-id="1e941-103">Prepare data for Office 365 Advanced eDiscovery</span></span>

<span data-ttu-id="1e941-104">이 항목에서는 고급 ediscovery에서 사례에 콘텐츠 검색의 결과 로드 하는 방법에 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e941-104">This topic describes how to load the results of a Content Search in to a case in Advanced eDiscovery.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="1e941-p101">고급 eDiscovery 조직에 대 한 고급 준수 추가 기능 또는 e 5 구독은 Office 365 E3 필요합니다. 해당 요금제에 가입한 상태 고급 eDiscovery 시도 하려는 하지 경우에 [Office 365 Enterprise e 5의 평가판 등록](https://go.microsoft.com/fwlink/p/?LinkID=698279)할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1e941-p101">Advanced eDiscovery requires an Office 365 E3 with the Advanced Compliance add-on or an E5 subscription for your organization. If you don't have that plan and want to try Advanced eDiscovery, you can [sign up for a trial of Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span></span> 
  
## <a name="step-1-prepare-office-365-data-for-advanced-ediscovery"></a><span data-ttu-id="1e941-107">1 단계: 고급 eDiscovery에 대 한 Office 365 데이터 준비</span><span class="sxs-lookup"><span data-stu-id="1e941-107">Step 1: Prepare Office 365 data for Advanced eDiscovery</span></span>

<span data-ttu-id="1e941-108">고급 eDiscovery 사용 하 여 데이터를 분석 하려면 Office 365 보안에서 실행 하는 콘텐츠 검색의 결과 사용할 수 있습니다 &amp; 준수 센터 (Office 365 보안에서 **콘텐츠 검색** 페이지에 나열 된 &amp; 준수 센터) 또는 검색 eDiscovery 사례와 관련 된 (보안에서 **eDiscovery** 페이지에 나열 된 &amp; 준수 센터).</span><span class="sxs-lookup"><span data-stu-id="1e941-108">To analyze data with Advanced eDiscovery, you can use the results of a Content Search that you run in the Office 365 Security &amp; Compliance Center (listed on the **Content search** page in the Office 365 Security &amp; Compliance Center) or a search associated with an eDiscovery case (listed on the **eDiscovery** page in the Security &amp; Compliance Center).</span></span> 
  
<span data-ttu-id="1e941-109">고급 eDiscovery에 대 한 분석을 위해 검색 결과 준비 하는 중에 자세한 단계에 대 한 [Office 365 고급 eDiscovery에 대 한 검색 결과 준비를](prepare-search-results-for-advanced-ediscovery.md)참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="1e941-109">For the detailed steps on preparing search results for analysis in Advanced eDiscovery, see [Prepare search results for Office 365 Advanced eDiscovery](prepare-search-results-for-advanced-ediscovery.md).</span></span>
  
> [!NOTE]
> <span data-ttu-id="1e941-110">Office 365의 외부 데이터를 가지게 하 고 준비 하 고 고급 eDiscovery, 한 참조를에서 분석할 수 있도록 Office 365로 가져올 하는 경우 [Office 365에 PST 파일 가져오기 (영문)의 개요](https://support.office.com/article/ba688e0a-0fcb-4bd7-8e57-2b669564ea84) 및 [Office 365의 보관 제 3 자 데이터](https://go.microsoft.com/fwlink/p/?linkid=716918)입니다.</span><span class="sxs-lookup"><span data-stu-id="1e941-110">If you have data outside of Office 365 and want to import it to Office 365 so that you can prepare and analyze it in Advanced eDiscovery, a see [Overview of importing PST files to Office 365](https://support.office.com/article/ba688e0a-0fcb-4bd7-8e57-2b669564ea84) and [Archiving third-party data in Office 365](https://go.microsoft.com/fwlink/p/?linkid=716918).</span></span> 
  
## <a name="step-2-load-search-result-data-in-to-a-case-in-advanced-ediscovery"></a><span data-ttu-id="1e941-111">2 단계: 검색 결과에서 데이터 로드 고급 ediscovery에서 사례에</span><span class="sxs-lookup"><span data-stu-id="1e941-111">Step 2: Load search result data in to a case in Advanced eDiscovery</span></span>

<span data-ttu-id="1e941-p102">보안에서 검색 결과 준비한 후 &amp; 고급 ediscovery에서 사례에에서 검색 결과 로드 하는 분석을 위해 준수 센터, 다음 단계에서는 것입니다. 자세한 내용은 [프로세스 모듈을 실행](run-the-process-module-in-advanced-ediscovery.md)을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="1e941-p102">After you prepare the search results in the Security &amp; Compliance Center for analysis, the next step is to load the search results in to a case in Advanced eDiscovery. For more detailed information, see [Run the Process module](run-the-process-module-in-advanced-ediscovery.md).</span></span>
  
1. <span data-ttu-id="1e941-114">이동 [https://protection.office.com](https://protection.office.com)합니다.</span><span class="sxs-lookup"><span data-stu-id="1e941-114">Go to [https://protection.office.com](https://protection.office.com).</span></span>
    
2. <span data-ttu-id="1e941-115">작업이 나 교육용 계정을 사용 하 여 Office 365에 로그인 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e941-115">Sign in to Office 365 using your work or school account.</span></span>
    
3. <span data-ttu-id="1e941-116">보안에서 &amp; 준수 센터 클릭 **검색 &amp; 조사** \> **eDiscovery** 를 조직에서 사례의 목록을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e941-116">In the Security &amp; Compliance Center, click **Search &amp; investigation** \> **eDiscovery** to display the list of cases in your organization.</span></span> 
    
4. <span data-ttu-id="1e941-117">고급 ediscovery에서로 데이터 로드 하려는 경우 다음 **열기** 를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e941-117">Click **Open** next to the case that you want to load data in to in Advanced eDiscovery.</span></span> 
    
5. <span data-ttu-id="1e941-118">대/소문자에 대 한 **홈** 페이지에서 **고급 eDiscovery**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e941-118">On the **Home** page for the case, click **Advanced eDiscovery**.</span></span> 
    
    ![고급 eDiscovery의 대/소문자를 열려면 고급 ediscovery 스위치를 클릭 합니다.](media/8e34ba23-62e3-4e68-a530-b6ece39b54be.png)
  
    <span data-ttu-id="1e941-p103">**고급 ediscovery 연결** 진행률 표시줄이 표시 됩니다. 고급 eDiscovery에 연결 하는 경우 대/소문자에 대 한 설치 페이지에서 컨테이너의 목록이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1e941-p103">The **Connecting to Advanced eDiscovery** progress bar is displayed. When you're connected to Advanced eDiscovery, a list of containers is displayed on the setup page for the case.</span></span> 
    
    ![대/소문자 고급 eDiscovery에 표시 됩니다.](media/8036e152-70dc-4bb7-9379-61c1ed8326b4.png)
  
     <span data-ttu-id="1e941-p104">이러한 컨테이너 고급 eDiscovery (영문) 1 단계에서에서 분석을 위해 준비 하는 검색 결과를 나타냅니다. 보안에서 대/소문자에 콘텐츠 검색와 이름이 같은 미치지 않습니다 컨테이너의 이름을 &amp; 준수 센터입니다. 목록에서 컨테이너는 준비한 메시지입니다. 다른 사용자, 고급 ediscovery 검색 결과 준비 하는 경우 해당 컨테이너 목록에 포함 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1e941-p104">These containers represent the search results that you prepared for analysis in Advanced eDiscovery in Step 1. Note that the name of the container has the same name as the Content Search in the case in the Security &amp; Compliance Center. The containers in the list are the ones that you prepared. If a different user prepared search results for Advanced eDiscovery, the corresponding containers won't be included in the list.</span></span> 
    
6. <span data-ttu-id="1e941-127">검색 결과 데이터를 컨테이너에서 고급 eDiscovery의 대/소문자를 로드 하려면 컨테이너를 선택 하 고 **프로세스**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e941-127">To load the search result data from a container in to the case in Advanced eDiscovery, select a container and then click **Process**.</span></span>
    
<span data-ttu-id="1e941-128">검색 결과 보안에서 후 &amp; 준수 센터를 분석 하 고는 대/소문자와 관련이 있는 데이터를 cull 고급 eDiscovery의 도구를 사용 하 여 다음 단계는 고급 ediscovery에서 사례에 추가 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1e941-128">After the search results from the Security &amp; Compliance Center are added to the case in Advanced eDiscovery, the next step is to use the tools in Advanced eDiscovery to analyze and cull the data that's relevant to the case.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="1e941-129">참고 항목</span><span class="sxs-lookup"><span data-stu-id="1e941-129">See also</span></span>

[<span data-ttu-id="1e941-130">Office 365 Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="1e941-130">Office 365 Advanced eDiscovery</span></span>](office-365-advanced-ediscovery.md)
  
[<span data-ttu-id="1e941-131">사용자 및 사례 설정</span><span class="sxs-lookup"><span data-stu-id="1e941-131">Set up users and cases</span></span>](set-up-users-and-cases-in-advanced-ediscovery.md)
  
[<span data-ttu-id="1e941-132">사례 데이터 분석</span><span class="sxs-lookup"><span data-stu-id="1e941-132">Analyzing case data</span></span>](analyze-case-data-with-advanced-ediscovery.md)
  
[<span data-ttu-id="1e941-133">관련성 설정 관리</span><span class="sxs-lookup"><span data-stu-id="1e941-133">Managing Relevance setup</span></span>](manage-relevance-setup-in-advanced-ediscovery.md)
  
[<span data-ttu-id="1e941-134">관련성 모듈을 사용 하 여</span><span class="sxs-lookup"><span data-stu-id="1e941-134">Using the Relevance module</span></span>](use-relevance-in-advanced-ediscovery.md)
  
[<span data-ttu-id="1e941-135">사례 데이터 내보내기 (영문)</span><span class="sxs-lookup"><span data-stu-id="1e941-135">Exporting case data</span></span>](export-case-data-in-advanced-ediscovery.md)

