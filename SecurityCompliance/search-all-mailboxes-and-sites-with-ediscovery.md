---
title: eDiscovery 센터를 사용하여 모든 사서함 및 사이트 검색
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 12/30/2016
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 56e2978f-71b6-4141-b769-ad856d31bbec
description: Office 365에서 eDiscovery 센터를 단일 eDiscovery 검색에서 비즈니스 사이트에 대 한 모든 Exchange Online 사서함, SharePoint Online 사이트 및 OneDrive을 검색할 수 있습니다. 조직에서 모든 콘텐츠 원본을 검색 하려면 eDiscovery 관리자 각 콘텐츠 원본에 대 한 적절 한 eDiscovery 권한은 할당 받아야 합니다.
ms.openlocfilehash: b3508d5929ca2b5b7a937eb2dccf677a2968cbbc
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22533339"
---
# <a name="search-all-mailboxes-and-sites-using-the-ediscovery-center"></a><span data-ttu-id="00a33-104">eDiscovery 센터를 사용하여 모든 사서함 및 사이트 검색</span><span class="sxs-lookup"><span data-stu-id="00a33-104">Search all mailboxes and sites using the eDiscovery Center</span></span>

<span data-ttu-id="00a33-p102">Office 365에서 eDiscovery 센터를 단일 eDiscovery 검색에서 비즈니스 사이트에 대 한 모든 Exchange Online 사서함, SharePoint Online 사이트 및 OneDrive을 검색할 수 있습니다. 조직에서 모든 콘텐츠 원본을 검색 하려면 eDiscovery 관리자 각 콘텐츠 원본에 대 한 적절 한 eDiscovery 권한은 할당 받아야 합니다.</span><span class="sxs-lookup"><span data-stu-id="00a33-p102">In the eDiscovery Center in Office 365, you can search all Exchange Online mailboxes, SharePoint Online sites, and OneDrive for Business sites in a single eDiscovery search. To search all content sources in the organization, an eDiscovery manager must be assigned the appropriate eDiscovery permissions for each content source.</span></span> 
  
## <a name="before-you-begin"></a><span data-ttu-id="00a33-107">시작하기 전에</span><span class="sxs-lookup"><span data-stu-id="00a33-107">Before you begin</span></span>

- <span data-ttu-id="00a33-p103">eDiscovery 관리자에게는 콘텐츠 원본을 검색하기 위한 적절한 권한이 할당되어야 합니다. 사서함 및 사이트에 eDiscovery 사용 권한을 할당하는 방법에 대한 자세한 내용은 다음을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="00a33-p103">An eDiscovery manager must be assigned the appropriate permissions to search a content source. For more information about assigning eDiscovery permissions to mailboxes and sites, see the following:</span></span> 
    
  - [<span data-ttu-id="00a33-110">검색 관리 역할 그룹의 구성원에 게 Exchange 설치를 통해 만들어진 검색 사서함에 대 한 전체 액세스 사서함 권한이 합니다.</span><span class="sxs-lookup"><span data-stu-id="00a33-110">Assign eDiscovery permissions in Exchange</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=526886)
    
  - [<span data-ttu-id="00a33-111">SharePoint Online에서 eDiscovery 권한 할당</span><span class="sxs-lookup"><span data-stu-id="00a33-111">Assign eDiscovery permissions in SharePoint Online</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=526885)
    
  - [<span data-ttu-id="00a33-112">비즈니스용 OneDrive 사이트에 eDiscovery 사용 권한 할당</span><span class="sxs-lookup"><span data-stu-id="00a33-112">Assign eDiscovery permissions to OneDrive for Business sites</span></span>](assign-permissions-to-onedrive-for-business-sites.md)
    
- <span data-ttu-id="00a33-p104">최대 10, 000 사서함 및 비즈니스 사이트에 대 한 SharePoint Online 및 OneDrive 무제한 단일 eDiscovery 검색 쿼리에서 검색할 수 있습니다. 그러나 검색 하려면 특정 사이트를 지정 하는 경우의 제한은 사이트 수가 100입니다.</span><span class="sxs-lookup"><span data-stu-id="00a33-p104">You can search a maximum of 10,000 mailboxes and an unlimited number of SharePoint Online and OneDrive for Business sites in a single eDiscovery search query. However, if you specify the specific sites to search, the limit is 100 sites.</span></span>
    
- <span data-ttu-id="00a33-115">모든 사서함 및 사이트를 검색 하는 경우의 결과 볼 때 제한의 설명에 대 한 [자세한 내용](search-all-mailboxes-and-sites-with-ediscovery.md#moreinfo) 은 섹션을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="00a33-115">See the [More information](search-all-mailboxes-and-sites-with-ediscovery.md#moreinfo) section for a description of the limits when viewing the results when searching all mailboxes and sites.</span></span> 
    
- <span data-ttu-id="00a33-116">EDiscovery 센터에서 검색 쿼리 만들기 (영문) 하는 방법에 대 한 자세한 내용은 [만들기 및 실행된 eDiscovery 쿼리를](https://go.microsoft.com/fwlink/p/?LinkID=404032)참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="00a33-116">For more information about creating search queries in the eDiscovery Center, see [Create and run eDiscovery queries](https://go.microsoft.com/fwlink/p/?LinkID=404032).</span></span>
    
## <a name="search-all-locations"></a><span data-ttu-id="00a33-117">모든 위치 검색</span><span class="sxs-lookup"><span data-stu-id="00a33-117">Search all locations</span></span>

1. <span data-ttu-id="00a33-118">eDiscovery 센터에서 검색 쿼리를 실행하려는 eDiscovery 사례를 엽니다.</span><span class="sxs-lookup"><span data-stu-id="00a33-118">In the eDiscovery Center, open the eDiscovery case that you want to run the search query for.</span></span>
    
2. <span data-ttu-id="00a33-119">**검색 및 내보내기**, 아래에서 기존 쿼리를 클릭 하거나 새 검색 쿼리를 만들려면 **새 항목** 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="00a33-119">Under **Search and Export**, click an existing query or click **New item** to create a new search query.</span></span> 
    
3. <span data-ttu-id="00a33-120">검색 쿼리 페이지의 **원본** 섹션에서 **쿼리 범위 수정**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="00a33-120">On the search query page, in the **Sources** section, click **Modify Query Scope**.</span></span>
    
4. <span data-ttu-id="00a33-121">**쿼리 범위 수정** 페이지에서 **모든 항목 검색**을 클릭한 후 검색할 콘텐츠 위치를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="00a33-121">On the **Modify Query Scope** page, click **Search everything**, and select the content locations to search.</span></span>
    
  - <span data-ttu-id="00a33-122">모든 사서함을 검색할 수 있는 **Exchange** 를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="00a33-122">Select **Exchange** to search all mailboxes.</span></span> 
    
  - <span data-ttu-id="00a33-123">**SharePoint** 비즈니스 사이트에 대 한 모든 SharePoint Online 및 OneDrive를 검색 하려면 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="00a33-123">Select **SharePoint** to search all SharePoint Online and OneDrive for Business sites.</span></span> 
    
  - <span data-ttu-id="00a33-124">조직에서 모든 콘텐츠 위치를 검색 하려면 **Exchange** 및 **SharePoint** 모두를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="00a33-124">Select both **Exchange** and **SharePoint** to search all content locations in your organization.</span></span> 
    
![모든 사서함 및 사이트 검색](media/e1f919ab-5596-43bb-a3c9-626cd41067b3.gif)
  
5. <span data-ttu-id="00a33-126">**확인**을 클릭하여 변경 내용을 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="00a33-126">Click **OK** to save the changes.</span></span> 
    
6. <span data-ttu-id="00a33-p105">검색 쿼리 페이지에서 키워드 쿼리, 날짜 범위 또는 검색할 특정 유형의 콘텐츠 범위 좁히기 등과 같은 기타 정보를 완성하거나 수정합니다. 쿼리를 실행할 준비가 되면 **검색**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="00a33-p105">Complete or revise other information on the search query page, such as the keyword query, the date range, or narrowing the specific types of content to search for. When you're ready to run the query, click **Search**.</span></span> 
    
## <a name="more-information"></a><span data-ttu-id="00a33-129">추가 정보</span><span class="sxs-lookup"><span data-stu-id="00a33-129">More information</span></span>
<span data-ttu-id="00a33-130"><a name="moreinfo"> </a></span><span class="sxs-lookup"><span data-stu-id="00a33-130"></span></span>

- <span data-ttu-id="00a33-131">최근 결과를 포함하는 상위 500개 사서함 및 상위 500개 사이트는 **쿼리** 페이지의 **원본**에 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="00a33-131">The top 500 mailboxes and the top 500 sites with the most results are listed under **Sources** on the **Query** page.</span></span> 
    
- <span data-ttu-id="00a33-132">모든 콘텐츠 원본에 포함된 총 항목 수와 전체 크기는 **쿼리** 페이지의 **원본**에 표시됩니다. 
</span><span class="sxs-lookup"><span data-stu-id="00a33-132">The total number of items found in all content sources and their combined total size are displayed under **Sources** on the **Query** page.</span></span> 
    
- <span data-ttu-id="00a33-133">Exchange 사서함 또는 **쿼리** 페이지의 SharePoint 사이트에서 가장 최근의 200개 검색 결과를 미리 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="00a33-133">You can preview the 200 most recent search results located in Exchange mailboxes or SharePoint sites on the **Query** page.</span></span> 
    
    <span data-ttu-id="00a33-134">다음 스크린 샷에는 모든 사서함 및 사이트를 검색할 때 **쿼리** 페이지에 표시되는 검색 결과의 예를 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="00a33-134">The following screenshot shows an example of the search results displayed on the **Query** page when you search all mailboxes and sites.</span></span> 
    
    ![모든 위치를 검색할 때의 결과 스크린 샷](media/4bf430f6-41ab-4bf6-afa9-33c3f6fd8b16.gif)
  

