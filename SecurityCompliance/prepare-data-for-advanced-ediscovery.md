---
title: Office 365 Advanced eDiscovery에 대 한 데이터 준비
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
ms.assetid: 2fb94c23-1846-4a0e-994d-da6d02445f15
description: 'Microsoft 365 보안 &amp; 및 준수 센터를 사용 하 여 office 365 Advanced eDiscovery로 analysis for office 365 데이터를 준비 하는 방법을 알아봅니다. '
ms.openlocfilehash: d9d81c145a86075affd76761eb6dcff0f84a1eac
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32265510"
---
# <a name="prepare-data-for-office-365-advanced-ediscovery"></a><span data-ttu-id="0806a-103">Office 365 Advanced eDiscovery에 대 한 데이터 준비</span><span class="sxs-lookup"><span data-stu-id="0806a-103">Prepare data for Office 365 Advanced eDiscovery</span></span>

<span data-ttu-id="0806a-104">이 항목에서는 Advanced eDiscovery의 사례에 대 한 콘텐츠 검색 결과를 로드 하는 방법에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="0806a-104">This topic describes how to load the results of a Content Search in to a case in Advanced eDiscovery.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="0806a-p101">Advanced eDiscovery를 사용하려면 Office 365 E3의 고급 준수 추가 기능이나 조직을 위한 E5 구독이 필요합니다. 이 요금제가 없는 상태에서 Advanced eDiscovery를 사용하려는 경우에는 [Office 365 Enterprise E5 평가판을 등록](https://go.microsoft.com/fwlink/p/?LinkID=698279)할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0806a-p101">Advanced eDiscovery requires an Office 365 E3 with the Advanced Compliance add-on or an E5 subscription for your organization. If you don't have that plan and want to try Advanced eDiscovery, you can [sign up for a trial of Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span></span> 
  
## <a name="step-1-prepare-office-365-data-for-advanced-ediscovery"></a><span data-ttu-id="0806a-107">1 단계: 고급 eDiscovery 용 Office 365 데이터 준비</span><span class="sxs-lookup"><span data-stu-id="0806a-107">Step 1: Prepare Office 365 data for Advanced eDiscovery</span></span>

<span data-ttu-id="0806a-108">고급 eDiscovery를 사용 하 여 데이터를 분석 하기 위해 microsoft 365 보안 <b0></b0> <b2></b2> 및 준수 센터의 <b1>콘텐츠 검색</b1> 페이지에 나열 된 < 365 보안 준수 센터에서 실행 한 콘텐츠 검색의 결과를 사용할 수 있습니다. ediscovery 사례에 연결 된 검색 (보안 <b4></b4> 및 준수 센터의 <b3>ediscovery</b3> 페이지에 나열 됨)</span><span class="sxs-lookup"><span data-stu-id="0806a-108">To analyze data with Advanced eDiscovery, you can use the results of a Content Search that you run in the Microsoft 365 Security &amp; Compliance Center (listed on the **Content search** page in the Microsoft 365 Security &amp; Compliance Center) or a search associated with an eDiscovery case (listed on the **eDiscovery** page in the Security &amp; Compliance Center).</span></span> 
  
<span data-ttu-id="0806a-109">고급 ediscovery에서 분석에 대 한 검색 결과를 준비 하는 방법에 대 한 자세한 단계는 [Office 365 Advanced eDiscovery에 대 한 검색 결과 준비](prepare-search-results-for-advanced-ediscovery.md)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="0806a-109">For the detailed steps on preparing search results for analysis in Advanced eDiscovery, see [Prepare search results for Office 365 Advanced eDiscovery](prepare-search-results-for-advanced-ediscovery.md).</span></span>
  
> [!NOTE]
> <span data-ttu-id="0806a-110">office 365 외부에 데이터가 있고이를 office 365로 가져와서 고급 eDiscovery에서이를 준비 하 고 분석할 수 있도록 하려면 office 365에서 [PST 파일을 office로 가져오기 개요](https://support.office.com/article/ba688e0a-0fcb-4bd7-8e57-2b669564ea84) 및 [타사 데이터 보관](https://go.microsoft.com/fwlink/p/?linkid=716918)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="0806a-110">If you have data outside of Office 365 and want to import it to Office 365 so that you can prepare and analyze it in Advanced eDiscovery, a see [Overview of importing PST files to Office 365](https://support.office.com/article/ba688e0a-0fcb-4bd7-8e57-2b669564ea84) and [Archiving third-party data in Office 365](https://go.microsoft.com/fwlink/p/?linkid=716918).</span></span> 
  
## <a name="step-2-load-search-result-data-in-to-a-case-in-advanced-ediscovery"></a><span data-ttu-id="0806a-111">2 단계: Advanced eDiscovery에서 사례에 검색 결과 데이터 로드</span><span class="sxs-lookup"><span data-stu-id="0806a-111">Step 2: Load search result data in to a case in Advanced eDiscovery</span></span>

<span data-ttu-id="0806a-112">분석을 위해 보안 &amp; 및 준수 센터에서 검색 결과를 준비한 다음에는 Advanced eDiscovery의 사례에 검색 결과를 로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="0806a-112">After you prepare the search results in the Security &amp; Compliance Center for analysis, the next step is to load the search results in to a case in Advanced eDiscovery.</span></span> <span data-ttu-id="0806a-113">자세한 내용은 [Process 모듈 실행](run-the-process-module-in-advanced-ediscovery.md)을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="0806a-113">For more detailed information, see [Run the Process module](run-the-process-module-in-advanced-ediscovery.md).</span></span>
  
1. <span data-ttu-id="0806a-114">[https://protection.office.com](https://protection.office.com)으로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="0806a-114">Go to [https://protection.office.com](https://protection.office.com).</span></span>
    
2. <span data-ttu-id="0806a-115">회사 또는 학교 계정을 사용하여 Office 365에 로그인합니다.</span><span class="sxs-lookup"><span data-stu-id="0806a-115">Sign in to Office 365 using your work or school account.</span></span>
    
3. <span data-ttu-id="0806a-116">보안 및 준수 센터에서 **검색 &amp; 조사** \> **eDiscovery**를 클릭하여 조직의 사례 목록을 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="0806a-116">In the Security &amp; Compliance Center, click **Search &amp; investigation** \> **eDiscovery** to display the list of cases in your organization.</span></span> 
    
4. <span data-ttu-id="0806a-117">고급 eDiscovery에서 데이터를 로드 하려는 사례 옆에 있는 **열기** 를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="0806a-117">Click **Open** next to the case that you want to load data in to in Advanced eDiscovery.</span></span> 
    
5. <span data-ttu-id="0806a-118">사례에 대한 **홈** 페이지에서 **Advanced eDiscovery**를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="0806a-118">On the **Home** page for the case, click **Advanced eDiscovery**.</span></span> 
    
    ![advanced ediscovery로 전환을 클릭 하 여 advanced ediscovery의 케이스 열기](media/8e34ba23-62e3-4e68-a530-b6ece39b54be.png)
  
    <span data-ttu-id="0806a-120">**고급 eDiscovery 진행률 표시줄에 연결 하** 는 중입니다.</span><span class="sxs-lookup"><span data-stu-id="0806a-120">The **Connecting to Advanced eDiscovery** progress bar is displayed.</span></span> <span data-ttu-id="0806a-121">고급 eDiscovery에 연결 되어 있는 경우 서비스 케이스의 설정 페이지에 컨테이너 목록이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0806a-121">When you're connected to Advanced eDiscovery, a list of containers is displayed on the setup page for the case.</span></span> 
    
    ![이 사례는 Advanced eDiscovery에 표시 됩니다.](media/8036e152-70dc-4bb7-9379-61c1ed8326b4.png)
  
     <span data-ttu-id="0806a-123">이러한 컨테이너는 1 단계에서 고급 eDiscovery를 분석 하기 위해 준비한 검색 결과를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="0806a-123">These containers represent the search results that you prepared for analysis in Advanced eDiscovery in Step 1.</span></span> <span data-ttu-id="0806a-124">컨테이너의 이름은 보안 &amp; 및 준수 센터의 사례에 있는 콘텐츠 검색과 이름이 같습니다.</span><span class="sxs-lookup"><span data-stu-id="0806a-124">Note that the name of the container has the same name as the Content Search in the case in the Security &amp; Compliance Center.</span></span> <span data-ttu-id="0806a-125">이 목록에는 사용자가 준비한 컨테이너 들이 나열 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0806a-125">The containers in the list are the ones that you prepared.</span></span> <span data-ttu-id="0806a-126">다른 사용자가 고급 eDiscovery를 위해 준비 된 검색 결과를 사용 하는 경우 해당 컨테이너가 목록에 포함 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0806a-126">If a different user prepared search results for Advanced eDiscovery, the corresponding containers won't be included in the list.</span></span> 
    
6. <span data-ttu-id="0806a-127">컨테이너의 검색 결과 데이터를 Advanced eDiscovery의 사례에 로드 하려면 컨테이너를 선택 하 고 **처리**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="0806a-127">To load the search result data from a container in to the case in Advanced eDiscovery, select a container and then click **Process**.</span></span>
    
<span data-ttu-id="0806a-128">보안 &amp; 및 준수 센터의 검색 결과가 advanced ediscovery의 사례에 추가 되 면 다음 단계는 advanced ediscovery의 도구를 사용 하 여 사례와 관련 된 데이터를 분석 하 고 cull 합니다.</span><span class="sxs-lookup"><span data-stu-id="0806a-128">After the search results from the Security &amp; Compliance Center are added to the case in Advanced eDiscovery, the next step is to use the tools in Advanced eDiscovery to analyze and cull the data that's relevant to the case.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="0806a-129">참고 항목</span><span class="sxs-lookup"><span data-stu-id="0806a-129">See also</span></span>

[<span data-ttu-id="0806a-130">Office 365 Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="0806a-130">Office 365 Advanced eDiscovery</span></span>](office-365-advanced-ediscovery.md)
  
[<span data-ttu-id="0806a-131">사용자 및 사례 설정</span><span class="sxs-lookup"><span data-stu-id="0806a-131">Set up users and cases</span></span>](set-up-users-and-cases-in-advanced-ediscovery.md)
  
[<span data-ttu-id="0806a-132">사례 데이터 분석</span><span class="sxs-lookup"><span data-stu-id="0806a-132">Analyzing case data</span></span>](analyze-case-data-with-advanced-ediscovery.md)
  
[<span data-ttu-id="0806a-133">관련성 설정 관리</span><span class="sxs-lookup"><span data-stu-id="0806a-133">Managing Relevance setup</span></span>](manage-relevance-setup-in-advanced-ediscovery.md)
  
[<span data-ttu-id="0806a-134">관련성 모듈 사용</span><span class="sxs-lookup"><span data-stu-id="0806a-134">Using the Relevance module</span></span>](use-relevance-in-advanced-ediscovery.md)
  
[<span data-ttu-id="0806a-135">사례 데이터 내보내기</span><span class="sxs-lookup"><span data-stu-id="0806a-135">Exporting case data</span></span>](export-case-data-in-advanced-ediscovery.md)

