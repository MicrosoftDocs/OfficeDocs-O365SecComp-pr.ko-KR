---
title: Office 365의에서 콘텐츠 검색
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 6/28/2018
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MOE150
- MED150
- MET150
ms.assetid: 53390468-eec6-45cb-b6cd-7511f9c909e4
description: 콘텐츠 검색을 사용 하 여 Office 365 보안에서 &amp; 준수 센터 비즈니스 대화에 대 한 사서함, SharePoint Online 사이트, OneDrive 계정, Microsoft 팀의, Office 365 그룹 및 Skype에서 콘텐츠를 검색 합니다. 키워드 검색 쿼리를 사용 하 여 수 있으며 검색 조건 검색 결과 범위를 좁힐 수 있습니다. 다음 미리 볼 수 있으며 검색 결과 내보낼 수 있습니다. 콘텐츠 검색 GDPR 데이터 주체 요청에 관련 될 수 있는 콘텐츠를 검색 하는 효과적인 도구 이기도 합니다.
ms.openlocfilehash: f0064ae08226b1b0e864b25bb845054184f1efa4
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22534180"
---
# <a name="content-search-in-office-365"></a><span data-ttu-id="3cdbe-106">Office 365의에서 콘텐츠 검색</span><span class="sxs-lookup"><span data-stu-id="3cdbe-106">Content Search in Office 365</span></span>

<span data-ttu-id="3cdbe-p102">Office 365 보안에서 콘텐츠 검색 eDiscovery 도구를 사용할 수 있는 &amp; 준수 센터 전자 메일, 문서 및 인스턴트 메시징 대화 Office 365 조직에서 등의 원본 위치에 항목을 검색할 수 있습니다. 이 도구를 사용 하 여 이러한 Office 365 서비스에 있는 항목을 찾으려고 합니다.</span><span class="sxs-lookup"><span data-stu-id="3cdbe-p102">You can use the Content Search eDiscovery tool in the Office 365 Security &amp; Compliance Center to search for in-place items such as email, documents, and instant messaging conversations in your Office 365 organization. Use this tool to search for items in these Office 365 services:</span></span>
  
- <span data-ttu-id="3cdbe-109">Exchange Online 사서함과 공용 폴더</span><span class="sxs-lookup"><span data-stu-id="3cdbe-109">Exchange Online mailboxes and public folders</span></span>
    
- <span data-ttu-id="3cdbe-110">SharePoint Online 사이트 및 비즈니스 계정에 대 한 OneDrive</span><span class="sxs-lookup"><span data-stu-id="3cdbe-110">SharePoint Online sites and OneDrive for Business accounts</span></span>
    
- <span data-ttu-id="3cdbe-111">비즈니스 대화에 대 한 Skype</span><span class="sxs-lookup"><span data-stu-id="3cdbe-111">Skype for Business conversations</span></span>
    
- <span data-ttu-id="3cdbe-112">Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="3cdbe-112">Microsoft Teams</span></span> 
    
- <span data-ttu-id="3cdbe-113">Office 365 그룹</span><span class="sxs-lookup"><span data-stu-id="3cdbe-113">Office 365 Groups</span></span>
    
<span data-ttu-id="3cdbe-p103">콘텐츠 검색, 콘텐츠 위치 개수를 실행 하 고 검색 결과의 예상된 번호를 검색 프로필에 표시 됩니다. 또한 신속 하 게 검색 쿼리와 일치 하는 대부분의 항목에 있는 콘텐츠 위치와 같은 통계를 볼 수 있습니다. 검색을 실행 한 후 결과 미리 볼 수도 있고 로컬 컴퓨터에 내보낼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3cdbe-p103">After you run a Content Search, the number of content locations and an estimated number of search results are displayed in the search profile. You can also quickly view statistics, such as the content locations that have the most items that match the search query. After you run a search, you can preview the results or export them to a local computer.</span></span>


## <a name="create-a-new-search"></a><span data-ttu-id="3cdbe-117">새 검색 만들기</span><span class="sxs-lookup"><span data-stu-id="3cdbe-117">Create a new search</span></span>

<span data-ttu-id="3cdbe-p104">**콘텐츠 검색** 페이지를 검색 하 고 미리 보기를 실행 하 고 검색 결과 내보내기에 대 한 액세스를 관리자, 규정 준수 관리자 또는 eDiscovery 관리자 여야 보안에서 eDiscovery 관리자 역할 그룹의 구성원 &amp; 준수 센터입니다. 자세한 내용은 참조 [Office 365 보안에서 eDiscovery 사용 권한을 할당 &amp; 준수 센터](assign-ediscovery-permissions.md)합니다.</span><span class="sxs-lookup"><span data-stu-id="3cdbe-p104">To have access to the **Content search** page to run searches and preview and export search results, an administrator, compliance officer, or eDiscovery manager must be a member of the eDiscovery Manager role group in the Security &amp; Compliance Center. For more information, see [Assign eDiscovery permissions in the Office‍ 365 Security &amp; Compliance Center](assign-ediscovery-permissions.md).</span></span>
  
1. <span data-ttu-id="3cdbe-120">이동 [https://protection.office.com](https://protection.office.com)합니다.</span><span class="sxs-lookup"><span data-stu-id="3cdbe-120">Go to [https://protection.office.com](https://protection.office.com).</span></span>
    
2. <span data-ttu-id="3cdbe-121">Office 365 전자 메일 주소 및 암호를 사용 하 여 로그인 합니다.</span><span class="sxs-lookup"><span data-stu-id="3cdbe-121">Sign in using your Office 365 email address and password.</span></span> 
    
3. <span data-ttu-id="3cdbe-122">보안에서 &amp; 준수 센터 클릭 **검색 &amp; 조사** \> **콘텐츠 검색**합니다.</span><span class="sxs-lookup"><span data-stu-id="3cdbe-122">In the Security &amp; Compliance Center, click **Search &amp; investigation** \> **Content search**.</span></span>
    
4. <span data-ttu-id="3cdbe-123">**검색** 페이지에 있는 화살표를 옆에 클릭 ![추가 아이콘](media/8ee52980-254b-440b-99a2-18d068de62d3.gif) **새 검색**합니다.</span><span class="sxs-lookup"><span data-stu-id="3cdbe-123">On the **Search** page, click the arrow next to ![Add icon](media/8ee52980-254b-440b-99a2-18d068de62d3.gif) **New search**.</span></span> 
    
    ![새 검색 드롭다운 목록](media/76b25861-55c5-4f50-9d48-9e2be2d0d078.png)
  
    <span data-ttu-id="3cdbe-125">다음 옵션 중 하나를 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3cdbe-125">You can choose one of the following options:</span></span>
    
  - <span data-ttu-id="3cdbe-p105">**안내 검색** -이 옵션은 검색을 만드는 과정을 안내 하는 마법사를 시작 합니다. 콘텐츠 위치를 선택 하 고 검색 쿼리를 작성 하는 사용자 인터페이스 요소는 **새 검색** 옵션와 같습니다.</span><span class="sxs-lookup"><span data-stu-id="3cdbe-p105">**Guided search** - This option starts a wizard that guides you through the creating the search. The user interface to select content locations and build the search query are the same as the **New search** option.</span></span> 
    
  - <span data-ttu-id="3cdbe-p106">검색을 새로 만들 수는 업데이트 된 사용자 인터페이스를 표시 하는 **새로운 검색** -이 옵션입니다. **새 검색**을 클릭 하는 경우 기본 옵션입니다.</span><span class="sxs-lookup"><span data-stu-id="3cdbe-p106">**New search** - This option displays an updated user interface to create a new search. This is the default option if you click **New search**.</span></span>
    
  - <span data-ttu-id="3cdbe-p107">특정 전자 메일 메시지에 대 한 검색 및 Exchange Id의 목록을 사용 하 여 다른 사서함 항목 **ID 목록에서 검색** -이 옵션 수 있습니다. ID 목록 검색 (공식적으로 대상이 지정 된 검색 이라고 함)를 만드는, 특정 사서함 항목에 대 한 검색을 식별 하는 쉼표로 구분 된 값 (CSV) 파일로 전송할 수 있습니다. 자세한 내용은 [Office 365에서 콘텐츠 검색 하는 ID 목록에 대 한 CSV 파일을 준비](csv-file-for-an-id-list-content-search.md)를 참조 합니다.</span><span class="sxs-lookup"><span data-stu-id="3cdbe-p107">**Search by ID List** - This option lets you search for specific email messages and other mailbox items using a list of Exchange IDs. To create an ID list search (formally called a targeted search), you submit a comma separated value (CSV) file that identifies the specific mailbox items to search for. For instructions, see [Prepare a CSV file for an ID list Content Search in Office 365](csv-file-for-an-id-list-content-search.md).</span></span>
    
    <span data-ttu-id="3cdbe-133">이 절차의 단계의 나머지 부분에서는 기본 새 검색 워크플로 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="3cdbe-133">The remainder of the steps in this procedure will follow the default new search workflow.</span></span>
    
5. <span data-ttu-id="3cdbe-134">드롭다운 목록에서 **새 검색** 을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="3cdbe-134">Click **New search** in the drop-down list.</span></span> 
    
6. <span data-ttu-id="3cdbe-135">**검색 쿼리**를 아래에서 다음 작업을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3cdbe-135">Under **Search query**, specify the following things.</span></span>
    
    ![키워드, 조건 및 검색 하는 위치를 지정 합니다.](media/1e6de9dd-eac9-4e2a-819d-9740cf6c9106.png)
  
- <span data-ttu-id="3cdbe-p108">**키워드를 검색 하려면** - **키워드** 상자에 검색 쿼리 유형입니다. 키워드, 메시지 전송 및 받은 날짜 또는 파일 이름 등의 문서 속성 또는 문서를 마지막으로 변경한 날짜와 같은 속성을 지정할 수 있습니다. 예: **AND**, **또는**, **하지**및 **NEAR**부울 연산자를 사용 하는 보다 복잡 한 쿼리를 사용할 수 있습니다. 문서 또는 외부에서 공유 된 문서에 대 한 검색에서 중요 한 정보 (예: 주민등록 번호)을 검색할 수도 있습니다. 키워드 상자에 빈을 지정 하지 않으면 검색 결과에 지정 된 콘텐츠 위치에 있는 모든 콘텐츠를 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="3cdbe-p108">**Keywords to search for** - Type a search query in **Keywords** box. You can specify keywords, message properties such as sent and received dates, or document properties such as file names or the date that a document was last changed. You can use a more complex queries that use a Boolean operator, such as **AND**, **OR**, **NOT**, and **NEAR**. You can also search for sensitive information (such as social security numbers) in documents, or search for documents that have been shared externally. If you leave the keyword box empty, all content located in the specified content locations will be included in the search results.</span></span>
    
    <span data-ttu-id="3cdbe-p109">또는 수 **키워드 목록을 표시** 확인란을 및 누르면 형식은 각 행에 있는 키워드입니다. 이렇게 하면 각 행에 키워드와 비슷합니다 기능에서 생성 된 검색 쿼리에 **OR** 연산자는 논리 연산자 ( **c:s**)으로 연결 됩니다.</span><span class="sxs-lookup"><span data-stu-id="3cdbe-p109">Alternatively, you can click the **Show keyword list** checkbox and the type a keyword in each row. If you do this, the keywords on each row are connected by a logical operator ( **c:s**) that is similar in functionality to the **OR** operator in the search query that's created.</span></span> 
    
    <span data-ttu-id="3cdbe-p110">키워드 목록을 사용 하는 이유 각 키워드를 일치 하는 얼마나 많은 항목이 표시 하는 통계를 얻을 수 있습니다. 이 키워드는는 가장 (및 최소) 효과적인를 빠르게 식별할 수 있습니다. 행에서 (괄호로 묶입니다) 키워드 구의 사용할 수도 있습니다. 검색 통계에 대 한 자세한 내용은 [콘텐츠 검색 결과 대 한 키워드 통계 보기를](view-keyword-statistics-for-content-search.md)참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="3cdbe-p110">Why use the keyword list? You can get statistics that show how many items match each keyword. This can help you quickly identify which keywords are the most (and least) effective. You can also use a keyword phrase (surrounded by parentheses) in a row. For more information about search statistics, see [View keyword statistics for Content Search results](view-keyword-statistics-for-content-search.md).</span></span>
    
- <span data-ttu-id="3cdbe-p111">**조건** -검색 범위를 좁힐 하 고 보다 정교한 결과 집합이 반환 하는 검색 조건을 추가할 수 있습니다. KQL 검색 쿼리를 만들고 실행 하 여 검색을 시작 하는 경우에 절을 추가 하는 각 조건입니다. 조건 **및** 연산자 기능와 유사한 논리 연산자 ( **c:c**)에 의해 (키워드 상자에 지정 된) 키워드 쿼리를 논리적으로 연결 됩니다. 항목 키워드 쿼리 및 결과에 포함할 하나 이상의 조건을 모두 충족 해야 함을 의미 합니다. 결과 범위를 좁히려면 조건 도움이 되는 방식입니다. 목록 및 설명은 검색 쿼리에서 사용할 수 있는 조건에 대 한 [키워드 쿼리 및 콘텐츠 검색을 위한 검색 조건에서](keyword-queries-and-search-conditions.md#search-conditions)"검색 조건" 섹션을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="3cdbe-p111">**Conditions** - You can add search conditions to narrow a search and return a more refined set of results. Each condition adds a clause to the KQL search query that is created and run when you start the search. A condition is logically connected to the keyword query (specified in the keyword box) by a logical operator ( **c:c**) that is similar in functionality to the **AND** operator. That means that items have to satisfy both the keyword query and one or more conditions to be included in the results. This is how conditions help to narrow your results. For a list and description of conditions that you can use in a search query, see the "Search conditions" section in [Keyword queries and search conditions for Content Search](keyword-queries-and-search-conditions.md#search-conditions).</span></span>
    
- <span data-ttu-id="3cdbe-155">**위치** -설치할 콘텐츠 위치를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="3cdbe-155">**Locations** - hoose the content locations to search.</span></span>
    
  - <span data-ttu-id="3cdbe-p112">**모든 위치** -조직에서 모든 콘텐츠 위치를 검색 하려면이 옵션을 사용 합니다. 여기에 모든 비활성 사서함, 모든 Office 365 그룹에 대 한 사서함, 사서함에 대 한 Microsoft 팀의 모든 등 모든 Exchange 사서함에서 전자 메일 모든 SharePoint와 OneDrive (사이트를 포함 하는 비즈니스 사이트에 대 한 비즈니스 대화에 대 한 모든 Skype 모든 Office 365 그룹 및 Microsoft 팀의), 및 모든 Exchange 공용 폴더의 항목입니다.</span><span class="sxs-lookup"><span data-stu-id="3cdbe-p112">**All locations** - Use this option to search all content locations in your organization. This includes email in all Exchange mailboxes (including all inactive mailboxes, mailboxes for all Office 365 Groups, mailboxes for all Microsoft Teams), all Skype for Business conversations, all SharePoint and OneDrive for Business sites (including the sites for all Office 365 Groups and Microsoft Teams), and items in all Exchange public folders.</span></span>
    
  - <span data-ttu-id="3cdbe-p113">**특정 위치** -특정 콘텐츠 위치를 검색 하려면이 옵션을 사용 합니다. 특정 Office 365 서비스에 대 한 모든 콘텐츠 위치를 검색할 수 있습니다 (예: 모든 검색 Exchange 사서함 또는 모든 SharePoint 사이트를 검색) 하거나 표시 되는 Office 365 서비스 중 하나에서 특정 위치를 검색할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3cdbe-p113">**Specific locations** - Use this option to search specific content locations. You can search all content locations for a specific Office 365 service (such as searching all Exchange mailboxes or search all SharePoint sites) or you can search specific locations in any of the Office 365 services that are displayed.</span></span> 
    
    ![사용자 인터페이스를 검색 하려면 콘텐츠 위치를 선택 합니다.](media/9a09708b-f8a2-4382-8c4e-2c610ec33c72.png)
  
    <span data-ttu-id="3cdbe-p114">메모를 검색 하려면 Exchange 사서함의 목록에 메일 그룹을 추가할 수도 있습니다. 메일 그룹에 대 한 그룹 구성원의 사서함 검색 됩니다. Note 동적 메일 그룹 지원 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3cdbe-p114">Note that you can also add distribution groups to the list of Exchange mailboxes to search. For distribution groups, the mailboxes of group members are searched. Note that dynamic distribution groups aren't supported.</span></span>
    
    <span data-ttu-id="3cdbe-p115">**중요:** 모든 사서함 위치 또는 특정 사서함을 검색 콘텐츠 검색의 결과 내보낼 때 MyAnalytics 및 다른 Office 365 응용 프로그램에서 사용자 사서함에 저장 된 데이터에 포함 됩니다. 이 데이터는 예상된 검색 결과에 포함 되지 않습니다 및 미리 보기를 위해 사용할 수 없습니다. 만 볼 수 포함 내보내고, 검색 결과 다운로드 하는 경우 [MyAnalytics에서 내보내기 데이터 및 기타 Office 365 응용 프로그램에서](#exporting-data-from-myanalytics-and-other-office-365-applications) "콘텐츠 검색 하는 방법에 대 한 자세한 내용은" 섹션을 참조 합니다.</span><span class="sxs-lookup"><span data-stu-id="3cdbe-p115">**Important:** When you search all mailbox locations or just specific mailboxes, data from MyAnalytics and other Office 365 applications that's saved to user mailboxes will be included when you export the results of a Content Search. This data will not be included in the estimated search results and it won't be available for preview. It will only be included when you export and download the search results; see [Exporting data from MyAnalytics and other Office 365 applications](#exporting-data-from-myanalytics-and-other-office-365-applications) in the "More information about content search" section.</span></span> 
    
7. <span data-ttu-id="3cdbe-167">검색 쿼리를 설정한 후 클릭 **저장 &amp; 실행**합니다.</span><span class="sxs-lookup"><span data-stu-id="3cdbe-167">After you've set up your search query, click **Save &amp; run**.</span></span>
    
8. <span data-ttu-id="3cdbe-p116">**검색을 저장** 페이지에서은 검색과 검색을 식별 하는 데 도움이 되는 선택적 설명을 대 한 이름을 입력 합니다. 조직에서 고유 하 게 하는 검색의 이름이 되어있는지 메모 합니다.</span><span class="sxs-lookup"><span data-stu-id="3cdbe-p116">On the **Save search** page, type a name for the search, and an optional description that helps identify the search. Note that the name of the search has to be unique in your organization.</span></span> 
    
9. <span data-ttu-id="3cdbe-170">검색을 시작 하려면 **저장** 을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="3cdbe-170">Click **Save** to start the search.</span></span> 
    
    <span data-ttu-id="3cdbe-p117">저장 하 여 검색을 실행 한 후 검색에 의해 반환 된 결과 결과 창에 표시 됩니다. 미리 보기 설정을 구성한 방식에 따라 검색 결과 표시 하거나 보 **결과 미리 보기** 클릭 해야 합니다. 자세한 내용은 다음 섹션을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="3cdbe-p117">After you save and run the search, any results returned by the search are displayed in the results pane. Depending on how you have the preview setting configured, the search results are display or you have to click **Preview results** to view them. See the next section for details.</span></span> 
    
<span data-ttu-id="3cdbe-174">를이 콘텐츠 검색에 다시 액세스 하거나 **콘텐츠를 검색** 페이지에 나열 된 다른 콘텐츠 검색에 액세스 하려면 검색을 선택 하 고 **열기**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="3cdbe-174">To access this content search again or access other content searches listed on the **Content search** page, select the search and then click **Open**.</span></span> 
  
<span data-ttu-id="3cdbe-175">결과 취소 하거나 검색을 새로 만들기를 클릭 ![추가 아이콘](media/O365-MDM-CreatePolicy-AddIcon.gif) **새 검색**합니다.</span><span class="sxs-lookup"><span data-stu-id="3cdbe-175">To clear the results or create a new search, click ![Add icon](media/O365-MDM-CreatePolicy-AddIcon.gif) **New search**.</span></span> 

  
## <a name="preview-search-results"></a><span data-ttu-id="3cdbe-176">검색 결과 미리 보기</span><span class="sxs-lookup"><span data-stu-id="3cdbe-176">Preview search results</span></span>

<span data-ttu-id="3cdbe-p118">검색 결과 미리 보기에 두 구성 설정이 있습니다. 기존 검색을 열거나 새 새 검색을 실행 한 후를 클릭 * * 개별 결과 * * 다음 미리 보기 설정을 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3cdbe-p118">There are two configuration settings for previewing search results. After you run a new a new search or open an existing search, click ** Individual results ** to view the following preview settings:</span></span> 
  
![검색 결과 설정 미리 보기](media/83519477-1c85-4442-8886-481f186fd758.png)
  
1. <span data-ttu-id="3cdbe-180">**결과 자동으로 미리 보기** -이 설정을 검색 하 고 나면을 실행 하는 검색 결과가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="3cdbe-180">**Preview results automatically** - This setting displays the search results after you a run a search.</span></span>
    
2. <span data-ttu-id="3cdbe-p119">**결과 수동으로 미리 보기** -이 설정은 검색 결과 창에서 개체 틀을 표시 하 고 클릭 하 여 검색 결과 표시 하는 **결과 미리 보기** 단추를 표시 하는 합니다. 이것이 기본 설정입니다. 기존 검색을 열 때 자동으로 검색 결과 표시 하 여 검색 성능을 향상 시킬 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3cdbe-p119">**Preview results manually** - This setting displays placeholders in the search results pane, and displays the **Preview results** button that you have to click to display the search results. This is the default setting; it helps enhance search performance by not automatically displaying the search results when you open an existing search.</span></span> 
    
<span data-ttu-id="3cdbe-p120">제한 미리볼 수를 사용할 수 있는 항목 수와 관련이 있습니다. 자세한 내용은 참조 [검색 Office 365 보안에 대 한 제한 &amp; 준수 센터](limits-for-content-search.md)합니다.</span><span class="sxs-lookup"><span data-stu-id="3cdbe-p120">There are limits related to how many items are available to be previewed. For more information, see [Limits for Search in the Office 365 Security &amp; Compliance Center](limits-for-content-search.md).</span></span> 
  
<span data-ttu-id="3cdbe-p121">미리볼 수 있는 지원 되는 파일 형식 목록에 대 한 "콘텐츠 검색 하는 방법에 대 한 자세한 내용은" 섹션에서 [검색 결과 미리 보기를](#previewing-search-results) 참조 하십시오. 문서의 복사본을 다운로드 하려면 또는 미리 보기에 대 한 파일 형식을 지원 되지 않으면 로컬 컴퓨터에 다운로드 하려면 **원본 파일을 다운로드** 를 클릭 수 있습니다. 경우에 페이지에 액세스할 수 있는 권한이 없습니다 웹 페이지.aspx에 대 한 페이지에 대 한 URL을 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="3cdbe-p121">For a list of supported file types that can be previewed, see [Previewing search results](#previewing-search-results) in the "More information about content search" section. If a file type isn't supported for preview or to download a copy of a document, you can click **Download original file** to download it to your local computer. For .aspx Web pages, the URL for the page is included though you might not have permissions to access the page.</span></span> 
  
<span data-ttu-id="3cdbe-188">또한 인덱싱되지 않은 항목 미리 보기에서 사용할 수 없습니다는 note 합니다.</span><span class="sxs-lookup"><span data-stu-id="3cdbe-188">Also note that unindexed items aren't available for previewing.</span></span>
  
## <a name="view-information-and-statistics-about-a-search"></a><span data-ttu-id="3cdbe-189">정보 및 통계를 검색 하는 방법에 대 한 보기</span><span class="sxs-lookup"><span data-stu-id="3cdbe-189">View information and statistics about a search</span></span>

<span data-ttu-id="3cdbe-p122">만들어 콘텐츠 검색을 실행 하 고 예상된 검색 결과 대 한 통계를 볼 수 있습니다. 검색 결과 검색 쿼리와 일치 하는 항목이 있는 콘텐츠 위치 개수 등의 가장 일치 하는 항목이 있는 콘텐츠 위치 이름 쿼리 통계 요약 포함 됩니다. 하나 이상의 콘텐츠 검색에 대 한 통계를 표시할 수 있습니다. 이 통해 신속 하 게 여러 검색에 대 한 결과 비교 하 고 결정을 내릴 효과 대 한 검색 쿼리를 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3cdbe-p122">After you create and run a content search, you can view statistics about the estimated search results. This includes a summary of the search results, the query statistics such as the number of content locations with items that match the search query, and the name of content locations that have the most matching items. You can display statistics for one or more content searches. This lets you to quickly compare the results for multiple searches and make decisions about the effectiveness of your search queries.</span></span>
  
<span data-ttu-id="3cdbe-p123">또한 검색 통계 및 키워드 통계를 CSV 파일로 다운로드할 수 있습니다. 이렇게 하면 Excel에서 정렬 및 필터링 기능을 사용 하 여 결과 비교 하 고 검색 결과 대 한 보고서를 준비 합니다.</span><span class="sxs-lookup"><span data-stu-id="3cdbe-p123">You can also download the search statistics and keyword statistics to a CSV file. This lets you use the filtering and sorting features in Excel to compare results, and prepare reports for your search results.</span></span>
  
<span data-ttu-id="3cdbe-196">검색 통계를 보려면:</span><span class="sxs-lookup"><span data-stu-id="3cdbe-196">To view search statistics:</span></span>
  
1. <span data-ttu-id="3cdbe-197">**콘텐츠 검색** 페이지의 보안에서 &amp; 준수 센터 **열기** 를 클릭 하 고 다음에 대 한 통계를 보려는 하는 검색을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="3cdbe-197">On the **Content search** page in the Security &amp; Compliance Center, click **Open** and then click the search that you want to view the statistic for.</span></span> 
    
2. <span data-ttu-id="3cdbe-198">페이지 날아가기 **쿼리 열기**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="3cdbe-198">On the fly out page, click **Open query**.</span></span> 
    
3. <span data-ttu-id="3cdbe-199">**개별 결과** 드롭다운 목록에서에서 **검색 프로필**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="3cdbe-199">In the **Individual results** drop down list, click **Search profile**.</span></span>
    
4. <span data-ttu-id="3cdbe-200">**유형** 드롭다운 목록에서에서 보려는 검색 통계에 따라 다음 옵션 중 하나를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="3cdbe-200">In the **Type** drop down list, click one of the following options depending on the search statistics you want to view.</span></span> 
    
  - <span data-ttu-id="3cdbe-p124">**요약** -각 유형의 검색 가능한 콘텐츠 위치에 대 한 통계를 표시 합니다. 이 콘텐츠 검색 쿼리와 일치 하는 항목을 포함 하는 콘텐츠 위치 수가 총 수와 크기의 결과 항목을 검색 하 고 있습니다. 이것이 기본 설정입니다.</span><span class="sxs-lookup"><span data-stu-id="3cdbe-p124">**Summary** - Displays statistics for each type of content locations searched. This contents the number of content locations that contained items that matched the search query, and the total number and size of search result items. This is the default setting.</span></span>
    
  - <span data-ttu-id="3cdbe-p125">**쿼리** -검색 쿼리 하는 방법에 대 한 통계를 표시 합니다. 검색 쿼리 통계 중 일부는 적용할 수, 쿼리 통계에 적용할 수 있는 콘텐츠 위치 유형을 포함 됩니다 (참고: **기본** 있음을 나타내도록 전체 검색 쿼리)을 포함 하는 콘텐츠 위치의 된 항목 수 검색 쿼리 및 총 수와 크기 및 항목 (지정된 된 콘텐츠 위치)에서 발견 된 일치 하는 검색 쿼리와 일치 합니다. Note (부분적으로 인덱싱된 항목 라고도 함) 인덱싱되지 않은 항목에 대 한 통계도 표시 됩니다. 그러나 사서함에서 유일한 부분적으로 인덱싱된 항목 통계에 포함 됩니다. SharePoint와 OneDrive에서 부분적으로 인덱싱된 항목 통계에 포함 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3cdbe-p125">**Queries** - Displays statistics about the search query. This includes the type of content location the query statistics are applicable to, part of the search query the statistics are applicable to (note that **Primary** indicates the entire search query), the number of the content locations that contain items that match the search query, and the total number and size and items that were found (in the specified content location) that match the search query. Note that statistics for unindexed items (also called partially indexed items) are also displayed. However, only partially indexed items from mailboxes are included in the statistics. Partially indexed items from SharePoint and OneDrive are not included in the statistics.</span></span>
    
  - <span data-ttu-id="3cdbe-p126">**위쪽 위치** -검색 된 각 콘텐츠 위치에서 검색 쿼리와 일치 하는 항목 수에 대 한 통계를 표시 합니다. 1, 000 개 위쪽 위치가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="3cdbe-p126">**Top locations** - Displays statistics about the number of items that match the search query in each content location that was searched. The top 1,000 locations are displayed.</span></span>
    
<span data-ttu-id="3cdbe-211">검색 통계에 대 한 자세한 내용은 [콘텐츠 검색 결과 대 한 키워드 통계 보기를](view-keyword-statistics-for-content-search.md)참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="3cdbe-211">For more detailed information about search statistics, see [View keyword statistics for Content Search results](view-keyword-statistics-for-content-search.md).</span></span>
  
  
## <a name="export-search-results"></a><span data-ttu-id="3cdbe-212">검색 결과 내보내기</span><span class="sxs-lookup"><span data-stu-id="3cdbe-212">Export search results</span></span>

<span data-ttu-id="3cdbe-p127">검색을 성공적으로 실행 한 후에 로컬 컴퓨터에 검색 결과 내보낼 수 있습니다. 전자 메일 결과 내보낼 때 다운로드할 수 있습니다 사용자의 컴퓨터에 PST 파일로 구성원이 나 개별 메시지 (.msg 파일). OneDrive 및 SharePoint 사이트에서 콘텐츠를 내보낼 때 기본 Office 문서의 복사본을 내보냅니다. 추가 문서와 내보낸된 검색 결과에 포함 된 보고서 됩니다. 또한 방금 검색 결과 보고서 및 실제 항목이 아닌를 내보낼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3cdbe-p127">After a search is successfully run, you can export the search results to a local computer. When you export email results, they can be downloaded to your computer as PST files or as individual messages (.msg files). When you export content from SharePoint and OneDrive sites, copies of native Office documents are exported. There are also additional documents and reports that are included with the exported search results. You can also just export the search results report and not the actual items.</span></span>
  
<span data-ttu-id="3cdbe-218">검색 결과 내보내려면:</span><span class="sxs-lookup"><span data-stu-id="3cdbe-218">To export search results:</span></span>
  
1. <span data-ttu-id="3cdbe-219">**콘텐츠 검색** 페이지의 보안에서 &amp; 준수 센터 **열기** 를 클릭 하 고 다음에 대 한 검색 결과 내보내려는 하는 검색을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="3cdbe-219">On the **Content search** page in the Security &amp; Compliance Center, click **Open** and then click the search that you want to export the search results for.</span></span> 
    
2. <span data-ttu-id="3cdbe-p128">페이지 날아가기 클릭 ![내보내기 검색 결과 아이콘](media/47205c65-babd-4b3a-bd7b-98dfd92883ba.png) **더 많은**, 다음 **결과 내보내기**를 클릭 하 고 합니다. 결과 보고서를 참고 검색을 내보낼 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3cdbe-p128">On the fly out page, click ![Export search results icon](media/47205c65-babd-4b3a-bd7b-98dfd92883ba.png) **More**, and then click **Export results**. Note that you can also export a search results report.</span></span>
    
3. <span data-ttu-id="3cdbe-p129">**결과 내보내기** 플라이아웃 페이지의 섹션을 완료합니다. 스크롤 막대를 사용하여 모든 내보내기 옵션을 확인해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="3cdbe-p129">Complete the sections on the **Export results** fly out page. Be sure to use the scroll bar to view all export options.</span></span> 
    
<span data-ttu-id="3cdbe-224">자세한 지침 및 문제해결 팁을 참조 합니다.</span><span class="sxs-lookup"><span data-stu-id="3cdbe-224">For more detailed instructions and troubleshooting tips, see:</span></span>
  
- [<span data-ttu-id="3cdbe-225">Office 365 보안에서 검색 결과 내보내기 &amp; 준수 센터</span><span class="sxs-lookup"><span data-stu-id="3cdbe-225">Export search results from the Office 365 Security &amp; Compliance Center</span></span>](export-search-results.md)
    
- [<span data-ttu-id="3cdbe-226">콘텐츠 검색 보고서 내보내기</span><span class="sxs-lookup"><span data-stu-id="3cdbe-226">Export a Content Search report</span></span>](export-a-content-search-report.md)
    

  
## <a name="more-information-about-content-search"></a><span data-ttu-id="3cdbe-227">콘텐츠 검색 하는 방법에 대 한 자세한 내용</span><span class="sxs-lookup"><span data-stu-id="3cdbe-227">More information about content search</span></span>

<span data-ttu-id="3cdbe-228">콘텐츠를 검색 하는 방법에 대 한 자세한 내용은 다음 섹션을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="3cdbe-228">See the following sections for more information about content searches.</span></span>
  
[<span data-ttu-id="3cdbe-229">콘텐츠 검색 제한</span><span class="sxs-lookup"><span data-stu-id="3cdbe-229">Content search limits</span></span>](#content-search-limits)
  
[<span data-ttu-id="3cdbe-230">검색 쿼리 만들기 (영문)</span><span class="sxs-lookup"><span data-stu-id="3cdbe-230">Building a search query</span></span>](#building-a-search-query)
  
[<span data-ttu-id="3cdbe-231">OneDrive 계정을 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="3cdbe-231">Searching OneDrive accounts</span></span>](#searching-onedrive-accounts)
  
[<span data-ttu-id="3cdbe-232">팀이 Microsoft 및 Office 365 그룹 검색</span><span class="sxs-lookup"><span data-stu-id="3cdbe-232">Searching Microsoft Teams and Office 365 Groups</span></span>](#searching-microsoft-teams-and-office-365-groups)
  
[<span data-ttu-id="3cdbe-233">비활성 사서함 검색</span><span class="sxs-lookup"><span data-stu-id="3cdbe-233">Searching inactive mailboxes</span></span>](#searching-inactive-mailboxes)
  
[<span data-ttu-id="3cdbe-234">검색 결과 미리 보기</span><span class="sxs-lookup"><span data-stu-id="3cdbe-234">Previewing search results</span></span>](#previewing-search-results)
  
[<span data-ttu-id="3cdbe-235">부분적으로 인덱싱된 항목</span><span class="sxs-lookup"><span data-stu-id="3cdbe-235">Partially indexed items</span></span>](#partially-indexed-items)
  
[<span data-ttu-id="3cdbe-236">MyAnalytics 및 다른 Office 365 응용 프로그램에서 데이터 내보내기 (영문)</span><span class="sxs-lookup"><span data-stu-id="3cdbe-236">Exporting data from MyAnalytics and other Office 365 applications</span></span>](#exporting-data-from-myanalytics-and-other-office-365-applications)
  
### <a name="content-search-limits"></a><span data-ttu-id="3cdbe-237">콘텐츠 검색 제한</span><span class="sxs-lookup"><span data-stu-id="3cdbe-237">Content search limits</span></span>

- <span data-ttu-id="3cdbe-238">콘텐츠 검색 기능에 적용 되는 제한에 대 한 참조 [검색 Office 365 보안에 대 한 제한 &amp; 준수 센터](limits-for-content-search.md)합니다.</span><span class="sxs-lookup"><span data-stu-id="3cdbe-238">For a description of the limits that are applied to the Content Search feature, see [Limits for Search in the Office 365 Security &amp; Compliance Center](limits-for-content-search.md).</span></span>
    
- <span data-ttu-id="3cdbe-p130">Microsoft는 모든 Office 365 조직에 의해 실행 되는 콘텐츠 검색에 대 한 성능 정보를 수집 합니다. 복잡 한 검색 쿼리 검색 시간에 영향을 줄 수를 하는 동안 기간 검색 라인은 사서함의 수에 영향을 주는 가장 큰 요인 해야 검색 됩니다. Microsoft 검색 시간에 대 한 서비스 수준 계약을 제공 하지, 하지만 다음 표에서 검색에 포함 된 사서함 수에 따라 콘텐츠 검색에 대 한 평균 검색 시간을 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="3cdbe-p130">Microsoft collects performance information for Content Searches run by all Office 365 organizations. While the complexity of the search query can impact search times, the biggest factor that affects how long searches take is the number of mailboxes searched. Although Microsoft doesn't provide a Service Level Agreement for search times, the following table lists average search times for a Content Search based on the number of mailboxes included in the search.</span></span>
    
|<span data-ttu-id="3cdbe-242">**사서함 수**</span><span class="sxs-lookup"><span data-stu-id="3cdbe-242">**Number of mailboxes**</span></span>|<span data-ttu-id="3cdbe-243">**평균 검색 시간**</span><span class="sxs-lookup"><span data-stu-id="3cdbe-243">**Average search time**</span></span>|
|:-----|:-----|
|<span data-ttu-id="3cdbe-244">100</span><span class="sxs-lookup"><span data-stu-id="3cdbe-244">100</span></span>  <br/> |<span data-ttu-id="3cdbe-245">30초</span><span class="sxs-lookup"><span data-stu-id="3cdbe-245">30 seconds</span></span>  <br/> |
|<span data-ttu-id="3cdbe-246">1,000</span><span class="sxs-lookup"><span data-stu-id="3cdbe-246">1,000</span></span>  <br/> |<span data-ttu-id="3cdbe-247">45 초</span><span class="sxs-lookup"><span data-stu-id="3cdbe-247">45 seconds</span></span>  <br/> |
|<span data-ttu-id="3cdbe-248">10,000</span><span class="sxs-lookup"><span data-stu-id="3cdbe-248">10,000</span></span>  <br/> |<span data-ttu-id="3cdbe-249">4분</span><span class="sxs-lookup"><span data-stu-id="3cdbe-249">4 minutes</span></span>  <br/> |
|<span data-ttu-id="3cdbe-250">25000</span><span class="sxs-lookup"><span data-stu-id="3cdbe-250">25,000</span></span>  <br/> |<span data-ttu-id="3cdbe-251">10분</span><span class="sxs-lookup"><span data-stu-id="3cdbe-251">10 minutes</span></span>  <br/> |
|<span data-ttu-id="3cdbe-252">50000</span><span class="sxs-lookup"><span data-stu-id="3cdbe-252">50,000</span></span>  <br/> |<span data-ttu-id="3cdbe-253">20분</span><span class="sxs-lookup"><span data-stu-id="3cdbe-253">20 minutes</span></span>  <br/> |
|<span data-ttu-id="3cdbe-254">100,000</span><span class="sxs-lookup"><span data-stu-id="3cdbe-254">100,000</span></span>  <br/> |<span data-ttu-id="3cdbe-255">25분</span><span class="sxs-lookup"><span data-stu-id="3cdbe-255">25 minutes</span></span>  <br/> |
  
### <a name="building-a-search-query"></a><span data-ttu-id="3cdbe-256">검색 쿼리 만들기 (영문)</span><span class="sxs-lookup"><span data-stu-id="3cdbe-256">Building a search query</span></span>

<span data-ttu-id="3cdbe-257">검색 쿼리 만들기 (영문), 부울 검색 연산자 및 검색 조건을 사용 하 고 중요 한 정보 유형 및 조직 외부 사용자와 공유 하는 콘텐츠를 검색 하는 방법에 대 한 자세한 내용은 [키워드 쿼리를 참조 하 고 검색 조건 콘텐츠 검색에 대 한 ](keyword-queries-and-search-conditions.md)합니다.</span><span class="sxs-lookup"><span data-stu-id="3cdbe-257">For detailed information about creating a search query, using Boolean search operators and search conditions, and searching for sensitive information types and content shared with users outside your organization, see [Keyword queries and search conditions for Content Search ](keyword-queries-and-search-conditions.md).</span></span>
  
<span data-ttu-id="3cdbe-258">키워드 목록을 사용 하 여 검색 쿼리를 만들 때 다음 사항에 주의 유지 합니다.</span><span class="sxs-lookup"><span data-stu-id="3cdbe-258">Keeping the following things in mind when using the keyword list to create a search query.</span></span>
  
- <span data-ttu-id="3cdbe-p131">해야 **키워드 목록을 표시** 확인란을 선택 하 고 검색 쿼리를 만드는 별도 행에 각 키워드를 입력 한 다음 각 행의 키워드 (또는 키워드 구) **OR** 연산자로 연결 됩니다. 키워드 상자에 키워드 목록을 붙여 방금 또는 키워드를 입력 한 후 **Enter** 키를 눌러, 하는 경우 **또는** 연산자로 연결 되지 않습니다. 키워드 목록을 추가 하는 잘못 된 및 올바른 예는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="3cdbe-p131">You have to select the **Show keyword list** checkbox and then type each keyword in a separate row to create a search query where the keywords (or keyword phrases) in each row are connected by the **OR** operator. If you just paste a list of keywords in the keyword box or press the **Enter** key after typing a keyword, they won't be connected by the **OR** operator. Here are incorrect and correct example of adding a list of keywords.</span></span> 
    
    <span data-ttu-id="3cdbe-262">**잘못 된**</span><span class="sxs-lookup"><span data-stu-id="3cdbe-262">**Incorrect**</span></span>
    
    ![(키워드 상자에 목록을 붙여넣어) 하 여 키워드 목록 서식을 지정 하는 잘못 된 방법](media/fb54e3df-232a-439a-b3d7-27a60ec76a4c.png)
  
    <span data-ttu-id="3cdbe-264">**맞는**</span><span class="sxs-lookup"><span data-stu-id="3cdbe-264">**Correct**</span></span>
    
    ![(확인란을 차례로 선택 붙여넣기 목록) 하 여 키워드 목록 서식을 지정 하는 올바른 방법](media/5d511a7b-c1f9-499c-bffe-e075bfc9adec.png)
  
- <span data-ttu-id="3cdbe-p132">또한 키워드 또는 키워드 구를 Excel 파일 또는 일반 텍스트 파일을 목록을 준비 하 고 하 고 복사 하 고, 키워드 목록에 목록에 붙여 수 있습니다. 이 작업을 수행 하려면 **키워드 목록을 표시** 확인란을 선택 해야 합니다. 그런 다음, 키워드 목록에 있는 첫번째 행을 클릭 하 고 목록에 붙여넣습니다. 키워드 목록에서 행을 구분 하는 Excel 또는 텍스트 파일에서 각 줄에 붙여넣어집니다.</span><span class="sxs-lookup"><span data-stu-id="3cdbe-p132">You can also prepare a list of keywords or keyword phrases in an Excel file or a plain text file, and then copy and paste your list in to the keyword list. To do this, you have to select the **Show keyword list** check box. Then, click the first row in the keyword list and paste your list. Each line from the Excel or text file will be pasted in to separate row in the keyword list.</span></span> 
    
- <span data-ttu-id="3cdbe-p133">키워드 목록을 사용 하 여 쿼리를 만든 후 것이 검색 쿼리를 확인 하는 검색 쿼리 구문을 의도 확인 하는 것이 좋습니다. **쿼리** 아래에서 세부 정보 창에 표시 되는 검색 쿼리 키워드는 쉼표로 구분 하 여 텍스트 **(c:s)**. 키워드는 논리 연산자 **OR** 연산자 비슷합니다 기능에 의해 연결 되어 있음을 나타냅니다. 마찬가지로, 검색 쿼리 조건을 포함 하는 경우 조건과 키워드는 구분 하 여 텍스트 **(c:c)**. 키워드와 유사한 기능에는 **및** 논리 연산자를 사용 하 여 조건을에 연결 되어 있음을 나타냅니다. 연산자입니다. 키워드 목록 및 조건을 사용 하는 경우 발생 하는 검색 쿼리 (세부 정보 창에 표시 됨)의 예는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="3cdbe-p133">After you create a query using the keyword list, it's a good idea to verify the search query syntax to make the search query is what you intended. In the search query that's displayed under **Query** in the details pane, the keywords are separated by the text **(c:s)**. This indicates that the keywords are connected by a logical operator similar in functionality to the **OR** operator. Similarly, if your search query includes conditions, the keywords and the conditions are separated by the text **(c:c)**. This indicates that the keywords are connected to the conditions with a logical operator similar in functionality to the **AND** operator. Here's an example of the search query (displayed in the Details pane) that results when using the keyword list and a condition.</span></span> 
    
    ![쿼리 키워드 목록 및 조건을 사용할 때 만들어지는의 예](media/b463750c-57fa-4602-9fed-0d5a420db3ad.png)
  
- <span data-ttu-id="3cdbe-p134">콘텐츠 검색을 실행 하는 경우 Office 365는 자동으로 대문자로 표시 될 수 있는 부울 연산자 및 지원 되지않는 문자에 대 한 검색 쿼리를 확인 합니다. 지원 되지않는 문자는 종종 및 일반적으로 검색 오류를 발생 숨겨지거나 원하지 않는 결과 반환 합니다. 지원 되지않는 문자를 되는지 여부를 확인 하는 방법에 대 한 자세한 내용은 [오류에 대 한 콘텐츠 검색 쿼리와 확인](check-your-content-search-query-for-errors.md)을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="3cdbe-p134">When you run a content search, Office 365 automatically checks your search query for unsupported characters and for Boolean operators that might not be capitalized. Unsupported characters are often hidden and typically cause a search error or return unintended results. For more information about the unsupported characters that are checked, see [Check your Content Search query for errors](check-your-content-search-query-for-errors.md).</span></span>
    
- <span data-ttu-id="3cdbe-p135">**쿼리 언어-국가/지역**눌러도 영어가 아닌 문자 (예: 중국어 문자)에 대 한 키워드를 포함 하는 검색 쿼리를 사용 하는 경우![콘텐츠 검색에서 쿼리 언어-국가/지역 아이콘](media/8d4b60c8-e1f1-40f9-88ae-ee2a7eca0886.png) 을 선택 하 고 프로그램 검색에 대 한 언어-국가 문화권 코드 값입니다. 기본 언어/지역 중립 인지를 메모 합니다. 콘텐츠 검색에 대 한 언어 설정을 변경할 필요가 어떻게 알 수 있습니까? 인 경우 콘텐츠 위치를 검색 하는 영어가 아닌 문자를 포함 하지만 검색에서 반환 하는 결과가 없으면 특정 언어 설정이 원인일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3cdbe-p135">If you have a search query that contains keywords for non-English characters (such as Chinese characters), you can click **Query language-country/region**![Query language-country/region icon in Content search](media/8d4b60c8-e1f1-40f9-88ae-ee2a7eca0886.png) and select a language-country culture code value for the search. Note that the default language/region is neutral. How can you tell if you need to change the language setting for a content search? If you're certain content locations contain the non-English characters you're searching for, but the search returns no results, the language setting might be the cause.</span></span> 
  
### <a name="searching-onedrive-accounts"></a><span data-ttu-id="3cdbe-284">OneDrive 계정을 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="3cdbe-284">Searching OneDrive accounts</span></span>

- <span data-ttu-id="3cdbe-p136">조직에서 OneDrive 사이트에 대 한 Url의 목록을 수집 하려면 [조직에서 모든 OneDrive 위치의 목록 만들기](https://support.office.com/article/8e200cb2-c768-49cb-88ec-53493e8ad80a)를 참조 합니다. 이 문서에서이 스크립트는 모든 OneDrive 사이트의 목록을 포함 하는 텍스트 파일을 만듭니다. 이 스크립트를 실행 하려면 설치 하 고 SharePoint Online 관리 셸을 사용 해야 합니다. 검색 하려는 각 OneDrive 사이트를 조직의 내 사이트 도메인에 대 한 URL을 추가 해야 합니다. 모든 OneDrive; 포함 된 도메인입니다. 예, `https://contoso-my.sharepoint.com`합니다. 다음은 사용자의 OneDrive 사이트에 대 한 URL의 한 예: `https://contoso-my.sharepoint.com/personal/sarad_contoso_onmicrosoft.com`합니다.</span><span class="sxs-lookup"><span data-stu-id="3cdbe-p136">To collect a list of the URLs for the OneDrive sites in your organization, see [Create a list of all OneDrive locations in your organization](https://support.office.com/article/8e200cb2-c768-49cb-88ec-53493e8ad80a). This script in this article creates a text file that contains a list of all OneDrive sites. To run this script, you'll have to install and use the SharePoint Online Management Shell. Be sure to append the URL for your organization's MySite domain to each OneDrive site that you want to search. This is the domain that contains all your OneDrive; for example,  `https://contoso-my.sharepoint.com`. Here's an example of a URL for a user's OneDrive site:  `https://contoso-my.sharepoint.com/personal/sarad_contoso_onmicrosoft.com`.</span></span>
    
    <span data-ttu-id="3cdbe-p137">사용자의 사용자 계정 이름 (UPN) 변경 된 특수 한 경우에서 해당 OneDrive 위치에 대 한 URL 새 UPN을 통합 하기 위해 변경 됩니다. 이 경우 사용자의 새 OneDrive URL을 추가 하 고 이전 하나를 제거 하 여 콘텐츠 검색을 수정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="3cdbe-p137">In the rare case that a person's user principal name (UPN) is changed, the URL for their OneDrive location will also be changed to incorporate the new UPN. If this happens, you'll have to modify a content search by adding the user's new OneDrive URL and removing the old one.</span></span>
  
### <a name="searching-microsoft-teams-and-office-365-groups"></a><span data-ttu-id="3cdbe-293">팀이 Microsoft 및 Office 365 그룹 검색</span><span class="sxs-lookup"><span data-stu-id="3cdbe-293">Searching Microsoft Teams and Office 365 Groups</span></span>

<span data-ttu-id="3cdbe-p138">Office 365 그룹 또는 팀이 Microsoft와 관련 된 사서함을 검색할 수 있습니다. 팀이 Microsoft Office 365 그룹을 기반으로 하기 때문에 검색 하는 매우 유사 합니다. 두 경우 모두, 그룹 또는 팀 사서함이 검색 되지 않습니다. 그룹 또는 팀 구성원의 사서함 검색 되지 않습니다. 를 검색 하려면 구체적으로 검색에 추가할 필요가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3cdbe-p138">You can search the mailbox that's associated with an Office 365 Group or a Microsoft Team. Because Microsoft Teams are built on Office 365 Groups, searching them is very similar. In both cases, only the group or team mailbox is searched; the mailboxes of the group or team members aren't searched. To search them, you have to specifically add them to the search.</span></span>
  
<span data-ttu-id="3cdbe-298">팀이 Microsoft 및 Office 365 그룹의 콘텐츠를 검색할 때 다음 사항에 주의 유지 합니다.</span><span class="sxs-lookup"><span data-stu-id="3cdbe-298">Keep the following things in mind when searching for content in Microsoft Teams and Office 365 Groups.</span></span>
  
- <span data-ttu-id="3cdbe-299">팀이 Microsoft 및 Office 365 그룹에 있는 콘텐츠를 검색 하려면 사서함 및 팀 또는 그룹에 연결할 수 있는 SharePoint 사이트를 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="3cdbe-299">To search for content located in Microsoft Teams and Office 365 Groups, you have to specify the mailbox and SharePoint site that are associated with a team or group.</span></span>
    
- <span data-ttu-id="3cdbe-p139">Microsoft 팀 또는 Office 365 그룹에 대 한 속성을 보려면 Exchange Online에서 **Get UnifiedGroup** cmdlet을 실행 합니다. 이것은 팀 또는 그룹에 연결 된 사이트의 URL을 얻으려면 좋은 방법입니다. 예, 다음 수석 지도 팀 이라는 하는 Office 365 그룹에 대 한 하는 선택 된 속성을 표시 하는 다음 명령을:</span><span class="sxs-lookup"><span data-stu-id="3cdbe-p139">Run the **Get-UnifiedGroup** cmdlet in Exchange Online to view properties for a Microsoft Team or an Office 365 Group. This is a good way to get the URL for the site that's associated with a team or a group. For example, the following command displays selected properties for an Office 365 Group named Senior Leadership Team:</span></span> 
    
  ```
  Get-UnifiedGroup "Senior Leadership Team" | FL DisplayName,Alias,PrimarySmtpAddress,SharePointSiteUrl
  DisplayName            : Senior Leadership Team
  Alias                  : seniorleadershipteam
  PrimarySmtpAddress     : seniorleadershipteam@contoso.onmicrosoft.com
  SharePointSiteUrl      : https://contoso.sharepoint.com/sites/seniorleadershipteam
  
  ```

    > [!NOTE]
    > <span data-ttu-id="3cdbe-303">**Get UnifiedGroup** cmdlet를 실행 하려면 역할을 할당 보기 권한만 있는 받는 사람에 게 Exchange 온라인 해야 하거나 역할 그룹의 구성원 이어야 하는 할당 보기 권한만 있는 받는 사람에 게 역할입니다.</span><span class="sxs-lookup"><span data-stu-id="3cdbe-303">To run the **Get-UnifiedGroup** cmdlet, you have to be assigned the View-Only Recipients role in Exchange Online or be a member of a role group that's assigned the View-Only Recipients role.</span></span> 
  
- <span data-ttu-id="3cdbe-p140">사용자의 사서함을 검색 하는 경우 모든 Microsoft 팀 또는 Office 365 그룹의 구성원 인 사용자를 검색할 수 없습니다. 마찬가지로, 검색 하는 경우 Microsoft 팀 이나 그룹 사서함 및만 그룹 사이트 수를 지정 하는 Office 365 그룹 검색은 되지 않습니다. 사서함 및 그룹 구성원의 비즈니스 계정에 대 한 OneDrive 검색에 명시적으로 추가 하지 않으면 검색 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3cdbe-p140">When a user's mailbox is searched, any Microsoft Team or Office 365 Group that the user is a member of won't be searched. Similarly, when you search a Microsoft Team or an Office 365 Group, only the group mailbox and group site that you specify is searched; the mailboxes and OneDrive for Business accounts of group members aren't searched unless you explicitly add them to the search.</span></span>
    
- <span data-ttu-id="3cdbe-p141">Microsoft 팀 또는 Office 365 그룹의 구성원 목록을 가져오려면,에서 속성을 볼 수 있습니다는 **홈 \> 그룹** Office 365 관리 센터의 페이지입니다. 또는 Exchange Online PowerShell에서 다음 명령을 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3cdbe-p141">To get a list of the members of a Microsoft Team or an Office 365 Group, you can view the properties on the **Home \> Groups** page in the Office 365 admin center. Alternatively, you can run the following command in Exchange Online PowerShell:</span></span> 
    
  ```
  Get-UnifiedGroupLinks <group or team name> -LinkType Members | FL DisplayName,PrimarySmtpAddress 
  ```

    > [!NOTE]
    > <span data-ttu-id="3cdbe-308">**Get UnifiedGroupLinks** cmdlet를 실행 하려면 역할을 할당 보기 권한만 있는 받는 사람에 게 Exchange 온라인 해야 하거나 역할 그룹의 구성원 이어야 하는 할당 보기 권한만 있는 받는 사람에 게 역할입니다.</span><span class="sxs-lookup"><span data-stu-id="3cdbe-308">To run the **Get-UnifiedGroupLinks** cmdlet, you have to be assigned the View-Only Recipients role in Exchange Online or be a member of a role group that's assigned the View-Only Recipients role.</span></span> 
  
- <span data-ttu-id="3cdbe-p142">Microsoft 팀의 채널의 일부인 대화에 연결 된 Microsoft 팀의 사서함에 저장 됩니다. 마찬가지로, 채널에서 팀 구성원을 공유 하는 파일은 팀의 SharePoint 사이트에 저장 됩니다. 따라서 채널의 대화 및 파일을 검색 하는 콘텐츠 위치의 Microsoft 팀 사서함 및 SharePoint 사이트를 추가 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="3cdbe-p142">Conversations that are part of a Microsoft Teams channel are stored in the mailbox that's associated with the Microsoft Team. Similarly, files that team members share in a channel are stored on the team's SharePoint site. Therefore, you have to add the Microsoft Team mailbox and SharePoint site as a content location to search conversations and files in a channel.</span></span>
    
- <span data-ttu-id="3cdbe-p143">또는 Microsoft 팀의 채팅 목록에 포함 된 대화 대화방에 참가 한 사용자의 Exchange Online 사서함에 저장 됩니다. 및 채팅 대화에 사용자를 공유 하는 파일의 파일 공유는 사용자의 비즈니스 계정에 대 한 OneDrive에 저장 됩니다. 따라서 채팅 목록에서 대화 하 고 파일을 검색 하려면 콘텐츠 위치로 비즈니스 계정에 대 한 개별 사용자 사서함 및 OneDrive를 추가 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="3cdbe-p143">Alternatively, conversations that are part of the Chat list in Microsoft Teams are stored in the Exchange Online mailbox of the users who participate in the chat. And files that a user shares in Chat conversations are stored in the OneDrive for Business account of the user who shares the file. Therefore, you have to add the individual user mailboxes and OneDrive for Business accounts as content locations to search conversations and files in the Chat list.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="3cdbe-p144">Microsoft 팀의 채팅 목록에 포함 된 대화에 참가 한 사용자 채팅 대화를 검색 하는 순서에는 Exchange Online (클라우드 기반) 사서함이 있어야 합니다. 채팅 목록에 포함 된 대화 채팅 참가자의 클라우드 기반 사서함에 저장 된 때문입니다. 채팅 참가자가 없는 경우 Exchange Online 사서함, 채팅 대화를 검색할 수 없습니다. 예, Exchange 하이브리드 배포에서 온-프레미스 사서함이 있는 사용자 Microsoft 팀의 채팅 목록에 포함 된 대화에 참가할 수 있도록 수 있습니다. 그러나이 경우이 대화의 콘텐츠를 없는 검색 가능한 사용자 클라우드 기반 사서함이 없기 때문에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3cdbe-p144">Users who participate in conversations that are part of the Chat list in Microsoft Teams must have an Exchange Online (cloud-based) mailbox in order for you to search chat conversations. That's because conversations that are part of the Chat list are stored in the cloud-based mailboxes of the chat participants. If a chat participant doesn't have an Exchange Online mailbox, you won't be able to search chat conversations. For example, in an Exchange hybrid deployment, users with an on-premises mailbox might be able to participate in conversations that are part of the Chat list in Microsoft Teams. However in this case, content from these conversation aren't searchable because the users don't have cloud-based mailboxes.</span></span> 
  
- <span data-ttu-id="3cdbe-p145">모든 Microsoft 팀 또는 팀 채널 노트 작성 및 공동 작업에 대 한 Wiki를 포함합니다. Wiki 콘텐츠.mht 서식 사용 하 여 파일을 자동으로 저장 됩니다. 이 파일은 팀의 SharePoint 사이트에 팀이 위 키 데이터 문서 라이브러리에 저장 됩니다. 검색할 콘텐츠 위치로 팀의 SharePoint 사이트를 지정 하 여 Wiki를 검색 하는 콘텐츠 검색 도구를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3cdbe-p145">Every Microsoft Team or team channel contains a Wiki for note-taking and collaboration. The Wiki content is automatically saved to a file with a .mht format. This file is stored in the Teams Wiki Data document library on the team's SharePoint site. You can use the Content Search tool to search the Wiki by specifying the team's SharePoint site as the content location to search.</span></span> 
    
    > [!NOTE]
    > <span data-ttu-id="3cdbe-p146">(팀의 SharePoint 사이트를 검색) 하는 경우 Microsoft 팀 또는 채널에 대 한 Wiki를 검색 하는 기능은 2017 년 6 월 22에 릴리스 되었습니다. 위 키 페이지를 저장 되거나에서 업데이트 된 날짜 또는 후에 검색할 사용할 수 있는 합니다. 위 키 페이지 마지막으로 저장 하거나 해당 날짜 이전에 업데이트 검색에 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="3cdbe-p146">The capability to search the Wiki for a Microsoft Team or Channel (when you search the team's SharePoint site) was released on June 22, 2017. Wiki pages that were saved or updated on that date or after are available to be searched. Wiki pages last saved or updated before that date aren't available for search.</span></span> 
 
- <span data-ttu-id="3cdbe-p147">모임 및 전화 Microsoft 팀의 채널에 대 한 요약 정보는 모임 또는 전화에 전화를 건 사용자의 사서함에도 저장 됩니다. 즉, 이러한 요약 레코드를 검색 하려면 콘텐츠 검색을 사용할 수 있습니다. 요약 정보에는 다음이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="3cdbe-p147">Summary information for meetings and calls in a Microsoft Teams channel are also stored in the mailboxes of users who dialed into the meeting or call. This means you can use Content Search to search these summary records. Summary information includes:</span></span> 
  - <span data-ttu-id="3cdbe-330">날짜, 시작 시간과 종료 시간, 모임 또는 전화의 기간</span><span class="sxs-lookup"><span data-stu-id="3cdbe-330">Date, start time, end time, and duration of a meeting or call</span></span>

  - <span data-ttu-id="3cdbe-331">날짜 및 시간 각 참가자에 참가 또는 모임 또는 전화를 왼쪽 시간</span><span class="sxs-lookup"><span data-stu-id="3cdbe-331">The date and time when each participant joined or left the meeting or call</span></span>

  - <span data-ttu-id="3cdbe-332">통화를 음성 메일로 전송</span><span class="sxs-lookup"><span data-stu-id="3cdbe-332">Calls sent to voice mail</span></span>

  - <span data-ttu-id="3cdbe-333">부재중 또는 응답 하지 않는 통화</span><span class="sxs-lookup"><span data-stu-id="3cdbe-333">Missed or unanswered calls</span></span>

  - <span data-ttu-id="3cdbe-334">별도 두 대 한 호출으로 표시 되는 통화 전송</span><span class="sxs-lookup"><span data-stu-id="3cdbe-334">Call transfers, which are represented as two separate calls</span></span>

  <span data-ttu-id="3cdbe-335">검색할 수 모임 및 전화 요약 레코드에 대 한 최대 8 시간까지 걸릴 수 있다는 note 합니다.</span><span class="sxs-lookup"><span data-stu-id="3cdbe-335">Note that it can take up to 8 hours for meeting and call summary records to be available to be searched.</span></span>

  <span data-ttu-id="3cdbe-p148">모임 요약 **종류 필드**;에서 **모임** 식별 된 검색 결과에서 통화 요약 **호출**로 식별 됩니다. 또한 팀 채널 및 1xN 채팅의 일부인 대화 **유형** 필드에서 **IM** 식별 됩니다.</span><span class="sxs-lookup"><span data-stu-id="3cdbe-p148">In the search results, meeting summaries are identified as **Meeting** in the **Type field**; call summaries are identified as **Call**. Additionally, conversations that are part of a Teams channel and 1xN chats are identified as **IM** in the **Type** field.</span></span>
  
  ![팀 모임, 통화 및 1xN 채팅은 종류 필드에서 식별 합니다.](media/O365-ContentSearch-Teams-MessageKind.png)

- <span data-ttu-id="3cdbe-339">특히 Microsoft 팀의 콘텐츠를 검색 하려면 **종류** 전자 메일 속성 또는 **메시지 종류** 검색 조건을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3cdbe-339">You can use the **Kind** email property or the **Message kind** search condition to search specifically for content in Microsoft Teams.</span></span> 
  - <span data-ttu-id="3cdbe-340">검색 쿼리 **키워드** 상자에서 키워드 검색 쿼리의 일부로 **Kind** 속성을 사용 하 여 입력 `kind:microsoftteams`합니다.</span><span class="sxs-lookup"><span data-stu-id="3cdbe-340">To use the **Kind** property as part of the keyword search query, in the **Keywords** box of a search query, type `kind:microsoftteams`.</span></span>

    ![종류: microsoftteams를 사용 하 여 키워드 상자에](media/O365-ContentSearch-Teams-Keywords.png)
  
  - <span data-ttu-id="3cdbe-342">검색 조건을 사용 하려면 **메시지 종류** 조건을 추가 하 고 값을 사용 하 여 `microsoftteams`합니다.</span><span class="sxs-lookup"><span data-stu-id="3cdbe-342">To use a search condition, add the **Message kind** condition and use the value `microsoftteams`.</span></span> 

    ![메시지 kind 조건 값 microsoftteams 사용 합니다.](media/O365-ContentSearch-Teams-MessageKindCondition.png)

<span data-ttu-id="3cdbe-p149">Note **및** 연산자에 의해 조건은 키워드 쿼리에 논리적으로 연결 합니다. 즉, 키워드 쿼리 및 검색 결과에 반환 하는 검색 조건을 모두 항목이 일치 해야 합니다. 자세한 내용은에서 "사용 조건에 대 한 지침" 섹션을 참조 하십시오. [키워드 쿼리 및 콘텐츠 검색에 대 한 검색 조건을.](keyword-queries-and-search-conditions.md#guidelines-for-using-conditions)</span><span class="sxs-lookup"><span data-stu-id="3cdbe-p149">Note that conditions are logically connected to the keyword query by the **AND** operator. That means an item must match both the keyword query and the search condition to be returned in the search results. For more information, see the "Guidelines for using conditions" section in [Keyword queries and search conditions for Content Search.](keyword-queries-and-search-conditions.md#guidelines-for-using-conditions)</span></span>

  
### <a name="searching-inactive-mailboxes"></a><span data-ttu-id="3cdbe-347">비활성 사서함 검색</span><span class="sxs-lookup"><span data-stu-id="3cdbe-347">Searching inactive mailboxes</span></span>

<span data-ttu-id="3cdbe-p150">콘텐츠 검색에서 비활성 사서함을 검색할 수 있습니다. 명령을 실행 하면 조직에서 비활성 사서함의 목록을 가져오려면, `Get-Mailbox -InactiveMailboxOnly` Exchange Online PowerShell에서 합니다. 또는 **데이터 관리 방식** 으로 이동할 수 있습니다 \> 보안에서 **보존** &amp; 준수 센터 다음 **자세히**를 클릭 하 고![탐색 모음 타원](media/9723029d-e5cd-4740-b5b1-2806e4f28208.gif) \> **비활성 사서함**입니다.</span><span class="sxs-lookup"><span data-stu-id="3cdbe-p150">You can search inactive mailboxes in a content search. To get a list of the inactive mailboxes in your organization, run the command  `Get-Mailbox -InactiveMailboxOnly` in Exchange Online PowerShell. Alternatively, you can go to **Data governance** \> **Retention** in the Security &amp; Compliance Center, and then click **More**![Navigation Bar ellipses](media/9723029d-e5cd-4740-b5b1-2806e4f28208.gif) \> **Inactive mailboxes**.</span></span>
  
<span data-ttu-id="3cdbe-351">다음은 비활성 사서함을 검색할 때 주의 해야할 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="3cdbe-351">Here are a few things to keep in mind when searching inactive mailboxes.</span></span>
  
- <span data-ttu-id="3cdbe-352">콘텐츠 검색 사용자 사서함을 포함 하는 경우 해당 사서함 그런 다음 비활성 이루어집니다 비활성 하 게 되 면 검색을 다시 실행 하는 경우 비활성 사서함을 검색 하는 콘텐츠 검색을 계속 됩니다.</span><span class="sxs-lookup"><span data-stu-id="3cdbe-352">If a content search includes a user mailbox and that mailbox is then made inactive, the content search will continue to search the inactive mailbox when you re-run the search after it becomes inactive.</span></span>
    
- <span data-ttu-id="3cdbe-p151">일부 경우에는 사용자는 활성 사서함과 동일한 SMTP 주소를가지고 있는 비활성 사서함 있을 수 있습니다. 이 경우 콘텐츠 검색에 대 한 위치도를 선택 하면 특정 사서함만 검색 됩니다. 즉, 검색 하는 사용자의 사서함을 추가 하는 경우 가정할 수 없습니다는 자신의 활성 및 비활성 사서함 검색 됩니다 되지 않습니다. 검색에 명시적으로 추가 하는 사서함을 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="3cdbe-p151">In some cases, a user may have an active mailbox and an inactive mailbox that have the same SMTP address. In this case, only the specific mailbox that you select as a location for a content search will be searched. In other words, if you add a user's mailbox to a search, you can't assume that both their active and inactive mailboxes will be searched; only the mailbox that you explicitly add to the search will be searched.</span></span>
    
- <span data-ttu-id="3cdbe-p152">활성 사서함과 동일한 SMTP 주소를 사용 하 여 비활성 사서함 필요 하지 못하도록 하는 것이 좋습니다. 비활성 사서함을 복구 하거나 활성 사서함이 있는 (또는 활성 사서함의 보관) 비활성 사서함의 내용을 복원 하는 다음 삭제를 권장 비활성 사서함에 현재 할당 된 SMTP 주소를 다시 사용 해야하는 경우는 비활성 사서함입니다. 자세한 내용은 다음 항목 중 하나를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="3cdbe-p152">We strongly recommend that you avoid having an active mailbox and inactive mailbox with the same SMTP address. If you need to reuse the SMTP address that is currently assigned to an inactive mailbox, we recommend that you recover the inactive mailbox or restore the contents of an inactive mailbox to an active mailbox (or the archive of an active mailbox), and then delete the inactive mailbox. For more information, see one of the following topics:</span></span>
    
  - [<span data-ttu-id="3cdbe-359">Office 365에서 비활성 사서함 복구</span><span class="sxs-lookup"><span data-stu-id="3cdbe-359">Recover an inactive mailbox in Office 365</span></span>](recover-an-inactive-mailbox.md)
    
  - [<span data-ttu-id="3cdbe-360">Office 365에서 비활성 사서함 복원</span><span class="sxs-lookup"><span data-stu-id="3cdbe-360">Restore an inactive mailbox in Office 365</span></span>](restore-an-inactive-mailbox.md)
    
  - [<span data-ttu-id="3cdbe-361">Office 365에서 비활성 사서함 삭제</span><span class="sxs-lookup"><span data-stu-id="3cdbe-361">Delete an inactive mailbox in Office 365</span></span>](delete-an-inactive-mailbox.md)

  
### <a name="previewing-search-results"></a><span data-ttu-id="3cdbe-362">검색 결과 미리 보기</span><span class="sxs-lookup"><span data-stu-id="3cdbe-362">Previewing search results</span></span>

<span data-ttu-id="3cdbe-p153">미리 보기 창에서 지원 되는 파일 형식 미리볼 수 있습니다. 파일 형식을 지원 되지 않으면 보기에서 로컬 컴퓨터로 파일 복사본을 다운로드 해야 합니다. 다음과 같은 파일 형식 지원 되며 검색 결과 창에서 미리볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3cdbe-p153">You can preview supported file types in the preview pane. If a file type isn't supported, you'll have to download a copy of the file to your local computer to view it. The following file types are supported and can be previewed in the search results pane.</span></span>
  
- <span data-ttu-id="3cdbe-366">.txt,.html,.mhtml</span><span class="sxs-lookup"><span data-stu-id="3cdbe-366">.txt, .html, .mhtml</span></span>
    
- <span data-ttu-id="3cdbe-367">.eml</span><span class="sxs-lookup"><span data-stu-id="3cdbe-367">.eml</span></span>
    
- <span data-ttu-id="3cdbe-368">.doc,.docx,.docm</span><span class="sxs-lookup"><span data-stu-id="3cdbe-368">.doc, .docx, .docm</span></span>
    
- <span data-ttu-id="3cdbe-369">.pptm,.pptx</span><span class="sxs-lookup"><span data-stu-id="3cdbe-369">.pptm, .pptx</span></span>
    
- <span data-ttu-id="3cdbe-370">.pdf</span><span class="sxs-lookup"><span data-stu-id="3cdbe-370">.pdf</span></span>
    
<span data-ttu-id="3cdbe-p154">또한 다음과 같은 파일 컨테이너 형식 지원 됩니다. 미리 보기 창에서 컨테이너에 있는 파일 목록을 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3cdbe-p154">Additionally, the following file container types are supported. You can view the list of files in the container in the preview pane.</span></span>
  
- <span data-ttu-id="3cdbe-373">.zip</span><span class="sxs-lookup"><span data-stu-id="3cdbe-373">.zip</span></span>
    
- <span data-ttu-id="3cdbe-374">.gzip</span><span class="sxs-lookup"><span data-stu-id="3cdbe-374">.gzip</span></span>
    
### <a name="partially-indexed-items"></a><span data-ttu-id="3cdbe-375">부분적으로 인덱싱된 항목</span><span class="sxs-lookup"><span data-stu-id="3cdbe-375">Partially indexed items</span></span>

- <span data-ttu-id="3cdbe-376">사서함의 앞에서 설명한 것, 부분적으로 인덱싱된 항목; 예상된 검색 결과에 포함 된 대로 SharePoint와 OneDrive에서 부분적으로 인덱싱된 항목 예상된 검색 결과에 포함 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3cdbe-376">As previously explained, partially indexed items in mailboxes are included in the estimated search results; partially indexed items from SharePoint and OneDrive are not included in the estimated search results.</span></span> 
    
- <span data-ttu-id="3cdbe-p155">부분적으로 항목 일치 하는 경우 검색 쿼리 (하기 때문에 검색 조건을 충족 하는 다른 메시지 또는 문서 속성), 예상된 인덱싱되지 않은 항목 수에 포함 되지 않습니다. 하는 경우는 부분적으로 항목을 검색 조건에 의해 제외, 것도에 포함 되지 않습니다 예상된 부분적으로 인덱싱된 항목 수입니다. 자세한 내용은 [부분적으로 인덱싱된 되는 Office 365에서 콘텐츠 검색에서 항목을](partially-indexed-items-in-content-search.md)참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="3cdbe-p155">If a partially item matches the search query (because other message or document properties meet the search criteria), it won't be included in the estimated number of unindexed items. If an partially item is excluded by the search criteria, it also won't be included in the estimated number of partially indexed items. For more information, see [Partially indexed items in Content Search in Office 365](partially-indexed-items-in-content-search.md).</span></span>
    
### <a name="exporting-data-from-myanalytics-and-other-office-365-applications"></a><span data-ttu-id="3cdbe-380">MyAnalytics 및 다른 Office 365 응용 프로그램에서 데이터 내보내기 (영문)</span><span class="sxs-lookup"><span data-stu-id="3cdbe-380">Exporting data from MyAnalytics and other Office 365 applications</span></span>

- <span data-ttu-id="3cdbe-p156">MyAnalytics (예: 사용자가 자신의 사서함에 메일 및 일정 데이터를 기반으로 자신의 시간을 소비 하는 방법에 대 한 통찰력)에서 데이터 및 다른 Office 365 응용 프로그램의 데이터를 사용자의 클라우드 기반 사서함에서 숨겨진 위치 (비 IPM 하위 트리)에 저장 된입니다. 콘텐츠 검색을 실행 한 후이 데이터는 예상된 검색 결과 쿼리 통계에에서 포함 되지 않습니다 및 미리 보기에서는 사용할 수 없습니다. 그러나 검색 결과 내보낼 때이 데이터를 내보낼 수 됩니다.</span><span class="sxs-lookup"><span data-stu-id="3cdbe-p156">Data from MyAnalytics (such as insights on how users spend their time based on mail and calendar data in their mailbox) and data from other Office 365 applications is a saved to a hidden location (in a non-IPM subtree) in user's cloud-based mailbox. After you run a Content Search, this data isn't included in the estimated search results, the query statistics, and it isn't available for preview. However this data will be exported when you export the results of a search.</span></span>
    
- <span data-ttu-id="3cdbe-p157">MyAnalytics 데이터와 다른 Office 365 응용 프로그램에서 데이터 "다른 Office 365 데이터" 라는 폴더를 내보냅니다. 이 폴더의 각 사용자에 대 한 하위 폴더를 포함합니다.</span><span class="sxs-lookup"><span data-stu-id="3cdbe-p157">The MyAnalytics data and the data from other Office 365 applications is exported to a folder named "Other Office 365 data". This folder includes subfolders for each user.</span></span>
  