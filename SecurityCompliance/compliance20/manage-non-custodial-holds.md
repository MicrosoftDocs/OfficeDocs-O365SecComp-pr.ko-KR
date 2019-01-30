---
title: 고급 eDiscovery (미리 보기)에서 보류를 관리 합니다.
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection: ''
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: ''
ms.openlocfilehash: 75ddbcfb401d285dfb7a4b610e3f0709e21946f2
ms.sourcegitcommit: ee28ee2b2bdfd049333c2f495d7f7780d13af4a6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2019
ms.locfileid: "29608142"
---
# <a name="rename-this-page-and-md-file-to-managing-holds"></a><span data-ttu-id="27da5-102">이 페이지와 "유지 관리"를 MD 파일 이름바꾸기</span><span class="sxs-lookup"><span data-stu-id="27da5-102">Rename this page and MD File to "Managing Holds"</span></span>

# <a name="holds-in-advanced-ediscovery-preview"></a><span data-ttu-id="27da5-103">고급 eDiscovery (미리 보기)에서 보류</span><span class="sxs-lookup"><span data-stu-id="27da5-103">Holds in Advanced eDiscovery (Preview)</span></span>
<span data-ttu-id="27da5-p101">사례에 관련 될 수 있는 콘텐츠를 유지 하기 위해 보류를 만들려면 (미리 보기) 고급 eDiscovery 사례를 사용할 수 있습니다. 기능을 보유할 고급 eDiscovery (미리 보기)를 사용 하 여, 보류를 배치할 수 custodians 및 해당 데이터 원본에 있습니다. 또한 비즈니스 사이트에 대 한 사서함과 OneDrive에서 custodial 아닌 보류를 배치할 수 있습니다. Office 365 그룹에 대해 비즈니스 사이트에 대 한 그룹 사서함, SharePoint 사이트 및 OneDrive에서 보류를 배치할 수도 있습니다. 마찬가지로, 사서함 및 Microsoft 팀과 연결 된 사이트에 보류를 배치할 수 있습니다. 대기 콘텐츠 위치를 배치 하는 경우 콘텐츠 더불어 릴리스 특정 데이터 위치를 제거 하거나 완전히 보류 정책을 삭제할 때까지 유지 됩니다.</span><span class="sxs-lookup"><span data-stu-id="27da5-p101">You can use an Advanced eDiscovery (Preview) case to create holds to preserve content that might be relevant to your case. Using the Advanced eDiscovery (Preview) hold capabilities, you can place holds on custodians and their data sources. Additionally, you can place a non-custodial hold on mailboxes and OneDrive for Business sites. You can also place a hold on the group mailbox, SharePoint site, and OneDrive for Business site for an Office 365 Group. Similarly, you can place a hold on the mailbox and site that are associated with Microsoft Teams. When you place content locations on hold, content is held until you release the custodian, remove a specific data location, or delete the hold policy entirely.</span></span>

## <a name="manage-custodian-based-holds"></a><span data-ttu-id="27da5-110">관리 더불어 기반 보존</span><span class="sxs-lookup"><span data-stu-id="27da5-110">Manage Custodian Based Holds</span></span>

<span data-ttu-id="27da5-p102">경우에 따라 유지 하기 위해 선택 및 식별 한 데이터 custodians의 집합을 할 수 있습니다. 고급 eDiscovery (미리 보기)에서 이러한 custodians thold에 배치 되는 사용자 및 선택한 데이터 원본을 더불어에 자동으로 추가 됩니다 정책을 유지 합니다.</span><span class="sxs-lookup"><span data-stu-id="27da5-p102">In some cases, you may have a set of data custodians that you have identified and choosen to preserve. In Advanced eDiscovery (Preview), when these custodians are placed on thold, the user and their selected data sources are automatically added to a custodian hold policy.</span></span> 

<span data-ttu-id="27da5-113">더불어 보류 정책을 보려면</span><span class="sxs-lookup"><span data-stu-id="27da5-113">To view the custodian hold policy:</span></span>

1. <span data-ttu-id="27da5-114">**보안 & 준수 센터**, **eDiscovery gt_ 고급 eDiscovery (미리 보기)를** 조직에서의 경우 목록이 표시를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="27da5-114">In the **Security & Compliance Center**, click **eDiscovery > Advanced eDiscovery (Preview)** to display the list of cases in your organization.</span></span>
   
2. <span data-ttu-id="27da5-p103">케이스 내에서 custodians를 추가 하려면 **Custodians** 탭으로 이동 합니다. 추가할 수 있습니다 (미리 보기) 고급 eDiscovery 사례 내에서 전체 custodians 보류 방법과 알아보려면 **사례 내 관리 Custodians** 섹션을 참조 하십시오. Custodians 추가 이미 있고 대기 상태로 설정 하는 경우에 3 단계로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="27da5-p103">Navigate to the **Custodians** tab to add custodians within your case. To learn how you can add and place custodians on hold within an Advanced eDiscovery (Preview) case, visit the **Managing Custodians within a Case** section. If you have already added custodians and placed them on hold, move to Step 3.</span></span>
   
3. <span data-ttu-id="27da5-118">**포함 하 고** 탭으로 이동 ' 더불어 정책 '을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="27da5-118">Navigate to the **Holds** tab and select the 'Custodian Policy'.</span></span>
   
4. <span data-ttu-id="27da5-p104">자세한 내용은 플라이 아웃에서 확인할 수 있습니다 사용자 정책에 대 한 통계를 유지 합니다. 또한 더불어 기반 대기를 사용 하 여 쿼리를 적용할와 동일 하 게 작업을 수행할 수 있습니다. 보류 쿼리 만들기 및 조건을 사용 하는 방법에 대 한 자세한 내용은 [키워드 쿼리 및 콘텐츠 검색에 대 한 검색 조건을](https://docs.microsoft.com/en-us/office365/SecurityCompliance/keyword-queries-and-search-conditions ) 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="27da5-p104">In the details flyout, you can see hold statistics for your policy. You can also perform actions like apply a query to your custodian-based hold. For more information about creating a hold query and using conditions, see [Keyword queries and search conditions for Content Search](https://docs.microsoft.com/en-us/office365/SecurityCompliance/keyword-queries-and-search-conditions )</span></span>
 
## <a name="manage-non-custodial-holds"></a><span data-ttu-id="27da5-122">비 Custodial 보류를 관리 합니다.</span><span class="sxs-lookup"><span data-stu-id="27da5-122">Manage Non-Custodial Holds</span></span>
<span data-ttu-id="27da5-123">보류를 만들 때 지정 된 콘텐츠 위치에 보관 되는 콘텐츠를 범위를 지정 하는 다음 옵션 있습니다.</span><span class="sxs-lookup"><span data-stu-id="27da5-123">When you create a hold, you have the following options to scope the content that is held in the specified content locations:</span></span>
  - <span data-ttu-id="27da5-p105">보류에서 모든 콘텐츠를 배치할 위치 무한 보류를 만듭니다. 또는 쿼리 기반 보류 검색 쿼리와 일치 하는 유일한 콘텐츠 보류에 배치 되는 위치를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="27da5-p105">You create an infinite hold where all content is placed on hold. Alternatively, you can create a query-based hold where only content that matches a search query is placed on hold.</span></span>
  - <span data-ttu-id="27da5-p106">콘텐츠 전송, 수신, 또는 해당 날짜 범위 내에서 생성 된를 포함 하는 날짜 범위를 지정할 수 있습니다. 또는 면 전송, 수신, 또는 만든에 관계 없이 모든 콘텐츠를 보관할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="27da5-p106">You can specify a date range to hold only the content that was sent, received, or created within that date range. Alternatively, you can hold all content regardless of when it was sent, received, or created.</span></span>

<span data-ttu-id="27da5-128">EDiscovery 사례에 대 한 보류를 만들려면:</span><span class="sxs-lookup"><span data-stu-id="27da5-128">To create a hold for an eDiscovery case:</span></span>
  1. <span data-ttu-id="27da5-129">**보안 & 준수 센터**, **eDiscovery gt_ 고급 eDiscovery (미리 보기)를** 조직에서의 경우 목록이 표시를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="27da5-129">In the **Security & Compliance Center**, click **eDiscovery > Advanced eDiscovery (Preview)** to display the list of cases in your organization.</span></span>
  
  2. <span data-ttu-id="27da5-130">보류를 만들려는 경우 다음 열기를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="27da5-130">Click Open next to the case that you want to create the holds in.</span></span>
  
  3. <span data-ttu-id="27da5-131">대/소문자에 대 한**홈** 탭 **을 포함 하 고** 탭을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="27da5-131">On the**Home** tab for the case, click the **Holds** tab.</span></span>
  
  4. <span data-ttu-id="27da5-132">**포함 하 고** 탭에서 **만들기**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="27da5-132">On the **Holds** tab, click  **Create**.</span></span>
  
  5. <span data-ttu-id="27da5-p107">보류 페이지에서 제품 키 이름 뒤에 보류에 이름을 지정 합니다. 보류의 이름을 조직에서 고유 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="27da5-p107">On the Name your hold page, give the hold a name. The name of the hold must be unique in your organization.</span></span>
 
  6. <span data-ttu-id="27da5-135">(선택 사항) 설명 상자에 보류에 대 한 설명을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="27da5-135">(Optional) In the Description box, add a description of the hold.</span></span>
  
  7. <span data-ttu-id="27da5-136">**다음**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="27da5-136">Click **Next**.</span></span>
  
  8. <span data-ttu-id="27da5-p108">보류에 배치 하려는 콘텐츠 위치를 선택 합니다. 보류 중인 사서함, 사이트 및 공용 폴더를 배치할 수 있습니다. a. **Exchange 전자 메일** - **선택 사용자, 그룹 또는 팀을** 클릭 하 고 **선택 사용자, 그룹 또는 팀을** 다시 클릭 합니다. 사서함을 보류를 지정 합니다. 검색 상자를 사용 하 여를 대기 시키려면 사용자 사서함 및 그룹 구성원의 사서함에 보류를 배치 하) (에 메일 그룹을 찾을 수 있습니다. Office 365 그룹 또는 팀이 Microsoft에 대 한 연결 된 사서함에서 보류를 배치할 수 있습니다. 사용자, 그룹, 팀 확인란을 선택 하 고 **선택**를클릭하고 **완료**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="27da5-p108">Choose the content locations that you want to place on hold. You can place mailboxes, sites, and public folders on hold. a. **Exchange email** - Click **Choose users, groups, or teams** and then click **Choose users, groups, or teams** again. to specify mailboxes to place on hold. Use the search box to find user mailboxes and distribution groups (to place a hold on the mailboxes of group members) to place on hold. You can also place a hold on the associated mailbox for an Office 365 Group or a Microsoft Team. Select the user, group, team check box, click **Choose**, and then click **Done**.</span></span>
 
    [!NOTE]
    <span data-ttu-id="27da5-p109">**선택의 사용자, 그룹 또는 팀을** 지정 하려면 사서함을 보류를 클릭 하면 표시 되는 사서함 선택 비어 있습니다. 성능 향상을 위해 디자인입니다. 이 목록에 사용자를 추가할 검색 상자에 이름 (최소 3 자)를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="27da5-p109">When you click **Choose users, groups, or teams** to specify mailboxes to place on hold, the mailbox picker that's displayed is empty. This is by design to enhance performance. To add people to this list, type a name (a minimum of 3 characters) in the search box.</span></span>


    <span data-ttu-id="27da5-p110">b. **SharePoint 사이트** - **선택 사이트** 를 클릭 하 고에 배치 하는 SharePoint 및 비즈니스 사이트에 대 한 OneDrive 대기중 지정을 다시 **선택 사이트** 클릭 합니다. 보류에 배치 하려는 각 사이트에 대 한 URL을 입력 합니다. Office 365 그룹 또는 팀이 Microsoft에 대 한 SharePoint 사이트에 대 한 URL을 추가할 수도 있습니다. **Choose**클릭 하 고 **완료**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="27da5-p110">b. **SharePoint Sites** - Click **Choose sites** and then click **Choose sites** again to specify SharePoint and OneDrive for Business sites to place on hold. Type the URL for each site that you want to place on hold. You can also add the URL for the SharePoint site for an Office 365 Group or a Microsoft Team. Click **Choose**, and then click **Done**.</span></span>
    
     <span data-ttu-id="27da5-153">보류에서 Office 365 그룹 및 Microsoft 팀의 배치에 대 한 팁 **FAQ** 섹션을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="27da5-153">See the **FAQ** section for tips on putting Office 365 Groups and Microsoft Teams on hold.</span></span>

    [!NOTE]
    <span data-ttu-id="27da5-p111">사용자의 사용자 계정 이름 (UPN)가 변경 하는 특수 한 경우 해당 OneDrive 계정에 대 한 URL 새 UPN을 통합 하기 위해 변경 됩니다. 이 경우 사용자의 새 OneDrive URL을 추가 하 고 이전 하나를 제거 하 여 보류를 수정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="27da5-p111">In the rare case that a person's user principal name (UPN) has changed, the URL for their OneDrive account will also be changed to incorporate the new UPN. If this happens, you'll have to modify the hold by adding the user's new OneDrive URL and removing the old one.</span></span>

     <span data-ttu-id="27da5-p112">c. **Exchange 공용 폴더** -조직에 유지 하면 Exchange Online의 모든 공용 폴더를 모든 위치 설정/해제 스위치 이동 합니다. 특정 공용 폴더 배치를 선택할 수는 없으며 메모를 보관 합니다. 공용 폴더에 대 한 보류를 배치 하지 않을 경우 **None** 으로 설정 하는 토글 스위치를 그대로 둡니다.</span><span class="sxs-lookup"><span data-stu-id="27da5-p112">c. **Exchange public folders** - Move the toggle switch to the All position to put all public folders in your Exchange Online organization on hold. Note that you can't choose specific public folders to put on hold. Leave the toggle switch set to **None** if you don't want to put a hold on public folders.</span></span>

  9. <span data-ttu-id="27da5-160">보류에 추가 콘텐츠 위치를 완료 했으면 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="27da5-160">When you're done adding content locations to the hold, click **Next**.</span></span>
  
  10. <span data-ttu-id="27da5-p113">조건을 사용 하 여 쿼리 기반 보류를 만들려면 다음 절차를 완료 합니다. 그렇지 않은 경우 바로 **다음**을 클릭 합니다. 1.1 키워드 아래 상자에 종류 상자에 검색 쿼리를 검색 조건에 맞는 콘텐츠만 상태에 있을 수 있도록 보관 합니다. 키워드, 메시지 속성 또는 파일 이름 등의 문서 속성을 지정할 수 있습니다. 또한 여부에 AND, OR 등의 부울 연산자를 사용 하는 보다 복잡 한 쿼리를 사용할 수 있습니다. 생략 하면 지정한 콘텐츠 위치에 있는 모든 콘텐츠에 배치 될 다음에 빈 키워드 상자를 보관 합니다.</span><span class="sxs-lookup"><span data-stu-id="27da5-p113">To create a query-based hold with conditions, complete the following. Otherwise, just click **Next**. 1.1 In the box under Keywords, type a search query in the box so that only the content that meets the search criteria is placed on hold. You can specify keywords, message properties, or document properties, such as file names. You can also use more complex queries that use a Boolean operator, such as AND, OR, or NOT. If you leave the keyword box empty, then all content located in the specified content locations will be placed on hold.</span></span>

    <span data-ttu-id="27da5-p114">1.2 보류에 대 한 검색 쿼리 범위를 좁힐 수 있는 하나 이상의 조건을 추가 하려면 **추가** 조건을 클릭 합니다. 각 조건은 만들고 보류를 만들 때 실행 되는 KQL 검색 쿼리 절을 추가 합니다. 같은 날짜 범위 내에서 만든 문서를 전자 메일 또는 사이트는 대기 상태에 놓일 수 있도록 날짜 범위를 지정할 수 있습니다. 조건에 AND 연산자가 (키워드 상자에 지정 된) 키워드 쿼리를 논리적으로 연결 됩니다. 항목 모두 만족 하는 의미 키워드 쿼리 및 조건에 배치할 수를 유지 합니다.</span><span class="sxs-lookup"><span data-stu-id="27da5-p114">1.2 Click  **Add** conditions to add one or more conditions to narrow the search query for the hold. Each condition adds a clause to the KQL search query that is created and run when you create the hold. For example you can specify a date range so that email or site documents that were created within the date ranged are placed on hold. A condition is logically connected to the keyword query (specified in the keyword box) by the AND operator. That means that items have to satisfy both the keyword query and the condition to be placed on hold.</span></span>

     <span data-ttu-id="27da5-172">검색 쿼리 만들기 (영문) 및 조건을 사용 하는 방법에 대 한 자세한 내용은 [키워드 쿼리 및 콘텐츠 검색에 대 한 검색 조건을](https://docs.microsoft.com/en-us/office365/SecurityCompliance/keyword-queries-and-search-conditions)참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="27da5-172">For more information about creating a search query and using conditions, see [Keyword queries and search conditions for Content Search](https://docs.microsoft.com/en-us/office365/SecurityCompliance/keyword-queries-and-search-conditions).</span></span>

  11. <span data-ttu-id="27da5-173">쿼리 기반 구성한 후 유지, **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="27da5-173">After configuring a query-based hold, click **Next**.</span></span>
 
  12. <span data-ttu-id="27da5-174">설정을 검토 하 고 **이 보류 만들기**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="27da5-174">Review your settings, and then click **Create this hold**.</span></span>


## <a name="view-hold-statistics"></a><span data-ttu-id="27da5-175">보류 통계 보기</span><span class="sxs-lookup"><span data-stu-id="27da5-175">View Hold Statistics</span></span>
<span data-ttu-id="27da5-p115">몇 시간 후 새 대기 하는 방법에 대 한 정보는 탭의 확장 **을 포함 하 고** 선택한 보류에 대 한 세부 정보 창에 표시 됩니다. 사서함 수를 포함 하는이 정보에는 사이트 누른 상태와 같은 항목의 크기와 총 대기 상태에 놓일 마지막 통계도 계산 된 대기 시간에 배치 된 콘텐츠에 대 한 통계 유지 합니다. 이러한 대기 통계 도움말 eDiscovery 사례와 관련 된 콘텐츠 양에 열리는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="27da5-p115">After some time, information about the new hold is displayed in the details pane on the **Holds** tab for the selected hold. This information includes the number of mailboxes and sites on hold and statistics about the content that was placed on hold, such as the total number and size of items placed on hold and the last time the hold statistics were calculated. These hold statistics help you identify how much content that's related to the eDiscovery case is being held.</span></span>

<span data-ttu-id="27da5-179">보류 통계에 대 한 염두에 다음과 같은 사항에 유의 하십시오.</span><span class="sxs-lookup"><span data-stu-id="27da5-179">Keep the following things in mind about hold statistics:</span></span>

  - <span data-ttu-id="27da5-p116">보류 중인 항목의 총 수 보류에 배치 되는 모든 콘텐츠 원본에서 항목의 수를 나타냅니다. 만들었고 쿼리 기반 기다리는 경우,이 통계는 쿼리 일치 하는 항목 수를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="27da5-p116">The total number of items on hold indicates the number of items from all content sources that are placed on hold. If you've created a query-based hold, this statistic indicates the number of items that match the query.</span></span>
  - <span data-ttu-id="27da5-p117">보류 중인 항목의 수에는 콘텐츠 위치에 인덱싱되지 않은 항목이 포함 됩니다. 참고 쿼리 기반 보류를 만드는 경우 콘텐츠 위치에 있는 모든 인덱싱되지 않은 항목 보류에 배치 됩니다. 쿼리 기반 보류의 검색 조건과 일치 하지 않는 인덱싱되지 않은 항목과 인덱싱되지 않은 항목의 날짜 범위 조건을 외부 빠질 수에 포함 됩니다. 이것은 검색 결과에 포함 되지 않습니다 인덱싱되지 않은 항목을 검색 쿼리 일치 하지 않는 또는 날짜 범위 조건에 따라 제외 되는 콘텐츠 검색을 실행 하는 경우 다릅니다. 인덱싱되지 않은 항목에 대 한 자세한 내용은 [Office 365에서 콘텐츠 검색에 부분적으로 인덱싱된 항목]을 참조 하십시오. (https://docs.microsoft.com/en-us/office365/SecurityCompliance/partially-indexed-items-in-content-search)합니다.</span><span class="sxs-lookup"><span data-stu-id="27da5-p117">The number of items on hold also includes unindexed items found in the content locations. Note that if you create a query-based hold, all unindexed items in the content locations are placed on hold. This includes unindexed items that don't match the search criteria of a query-based hold and unindexed items that might fall outside of a date range condition. This is different than what happens when you run a Content Search, in which unindexed items that don't match the search query or are excluded by a date range condition aren't included in the search results. For more information about unindexed items, see [Partially indexed items in Content Search in Office 365] (https://docs.microsoft.com/en-us/office365/SecurityCompliance/partially-indexed-items-in-content-search).</span></span> 
  - <span data-ttu-id="27da5-187">보류 중인 항목의 현재 수를 계산 하는 검색 estimate를 다시 실행 하려면 통계 업데이트를 클릭 하 여 최신 보류 통계를 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="27da5-187">You can get the latest hold statistics by clicking Update statistics to re-run a search estimate that calculates the current number of items on hold.</span></span>
  - <span data-ttu-id="27da5-188">필요한 경우 세부 정보 창에서 보류 통계를 업데이트 하려면 도구 모음에서 새로고침을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="27da5-188">If necessary, click Refresh in the toolbar to update the hold statistics in the details pane.</span></span>
  - <span data-ttu-id="27da5-189">에 있는 항목의 수에 대 한 표준의 해당 사서함 이나 사이트 보류 중인 사용자는 일반적으로 또는 새 전자 메일 메시지를 받는 보내고 비즈니스 문서에 대 한 새 SharePoint와 OneDrive 만들기 때문에 시간이 지남에 따라 증가에 대해 유지 합니다.</span><span class="sxs-lookup"><span data-stu-id="27da5-189">It's normal for the number of items on hold to increase over time because users whose mailbox or site is on hold are typically sending or receiving new email message and creating new SharePoint and OneDrive for Business documents.</span></span>

[!NOTE]
<span data-ttu-id="27da5-p118">SharePoint 사이트 또는 OneDrive 계정 다중-지리적으로 분산 환경에서 다른 지역으로 이동 하는 경우 해당 사이트에 대 한 통계를 보류 통계에 포함 되지 않습니다. 그러나 사이트의 콘텐츠에 계속 대기 됩니다. 또한 사이트는 다른 지역으로 이동 하는 경우 보류에 표시 되는 URL 업데이트 되지 않습니다. 보류를 편집 하는 URL을 업데이트 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="27da5-p118">If a SharePoint site or OneDrive account is moved to a different region in a multi-geo environment, the statistics for that site won't be included in the hold statistics. However, the content in the site will still be on hold. Also, if a site is moved to a different region the URL that's displayed in the hold will not be updated. You'll have to edit the hold and update the URL.</span></span>

## <a name="faq"></a><span data-ttu-id="27da5-194">FAQ</span><span class="sxs-lookup"><span data-stu-id="27da5-194">FAQ</span></span>
- <span data-ttu-id="27da5-p119">프로그램 관리자를 추가 Office 365 그룹 또는 Microsoft 팀 사이트는 어떻게 매핑할 수행 **? 및 Office 365 그룹 및 팀이 Microsoft에서 유지 비 Custodial 배치 어떻습니까?** 팀이 Microsoft Office 365 그룹 기반으로 구축 됩니다. 따라서 대기 eDiscovery 사례에 배치 하는 매우 유사 합니다. Office 365 그룹 및 Microsoft 팀에 배치할 유지 하는 경우 다음 사항에 주의 유지 합니다.</span><span class="sxs-lookup"><span data-stu-id="27da5-p119">**How do I map an additional Office 365 Groups or Microsoft Teams site to a custodian? And what about placing a non-Custodial hold on Office 365 Groups and Microsoft Teams?** Microsoft Teams are built on Office 365 Groups. Therefore, placing them on hold in an eDiscovery case is very similar. Keep the following things in mind when placing Office 365 Groups and Microsoft Teams on hold.</span></span>
  - <span data-ttu-id="27da5-199">보류에서 Office 365 그룹 및 팀이 Microsoft에 있는 콘텐츠를 배치 하려면 사서함을 지정할 필요가 및 SharePoint 사이트의 그룹 또는 팀와 연결 합니다.</span><span class="sxs-lookup"><span data-stu-id="27da5-199">To place content located in Office 365 Groups and Microsoft Teams on hold, you have to specify the mailbox and SharePoint site that associated with a group or team.</span></span>
  
  - <span data-ttu-id="27da5-p120">Exchange Online에서 하는 Office 365 그룹 또는 Microsoft 팀에 대 한 속성을 볼 **Get UnifiedGroup** cmdlet을 실행 합니다. 이것은 Office 365 그룹 또는 팀이 Microsoft와 관련 된 사이트의 URL을 얻으려면 좋은 방법입니다. 예, 다음 수석 지도 팀 이라는 하는 Office 365 그룹에 대 한 하는 선택 된 속성을 표시 하는 다음 명령을:</span><span class="sxs-lookup"><span data-stu-id="27da5-p120">Run the **Get-UnifiedGroup** cmdlet in Exchange Online to view properties for an Office 365 Group or Microsoft Team. This is a good way to get the URL for the site that's associated with an Office 365 Group or a Microsoft Team. For example, the following command displays selected properties for an Office 365 Group named Senior Leadership Team:</span></span>

<span data-ttu-id="27da5-203">' ' powershell</span><span class="sxs-lookup"><span data-stu-id="27da5-203">''' powershell</span></span>

    Get-UnifiedGroup "Senior Leadership Team" | FL DisplayName,Alias,PrimarySmtpAddress,SharePointSiteUrl
    DisplayName            : Senior Leadership Team
    Alias                  : seniorleadershipteam
    PrimarySmtpAddress     : seniorleadershipteam@contoso.onmicrosoft.com
    SharePointSiteUrl      : https://contoso.sharepoint.com/sites/seniorleadershipteam
    '''

 [!NOTE]
 <span data-ttu-id="27da5-204">Get UnifiedGroup cmdlet를 실행 하려면 역할을 할당 보기 권한만 있는 받는 사람에 게 Exchange 온라인 해야 하거나 역할 그룹의 구성원 이어야 하는 할당 보기 권한만 있는 받는 사람에 게 역할입니다.</span><span class="sxs-lookup"><span data-stu-id="27da5-204">To run the Get-UnifiedGroup cmdlet, you have to be assigned the View-Only Recipients role in Exchange Online or be a member of a role group that's assigned the View-Only Recipients role.</span></span>

 - <span data-ttu-id="27da5-p121">사용자의 사서함을 검색 하는 경우 모든 Office 365 그룹 또는 Microsoft 팀의 구성원 인 사용자를 검색할 수 없습니다. 마찬가지로,는 Office 365 그룹 놓거나 Microsoft 팀 유지 그룹 사서함 및 사이트 그룹에 배치 되는 경우 보류 합니다. 명시적으로 custodians로 추가 하거나 해당 데이터 원본 보류를 배치 하지 않는 한 사서함 및 그룹 구성원의 비즈니스 사이트에 대 한 OneDrive 보류에 추가 되지 않습니다. 따라서 특정 더불어에 대 한 보유 하는 Office 365 그룹 또는 Microsoft 팀에 배치 해야 하는 경우에 매핑 (영문) 사이트 그룹 및 그룹 사서함 더불어 (참조 관리 Custodians 고급 eDiscovery (미리 보기)에서)을 하는 것이 좋습니다. Office 365 그룹 또는 Microsoft 팀 단일 더불어 영향을 주는 없는 경우에 추가 (영문) 비 custodial를 원본 유지 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="27da5-p121">When a user's mailbox is searched, any Office 365 Group or Microsoft Team that the user is a member of won't be searched. Similarly, when you place an Office 365 Group or Microsoft Team hold, only the group mailbox and group site are placed on hold; the mailboxes and OneDrive for Business sites of group members aren't placed on hold unless you explicitly add them as custodians or place their data sources hold. Therefore, if you the need to place an Office 365 Group or Microsoft Team on hold for a specific custodian, consider mapping the group site and group mailbox to the custodian (See Managing Custodians in Advanced eDiscovery (Preview)). If the Office 365 Group or Microsoft Team is not attributable to a single custodian, consider adding the source to a non-custodial hold.</span></span> 
 
 - <span data-ttu-id="27da5-p122">Office 365 그룹 또는 Microsoft 팀의 구성원 목록을 가져오려면, Office 365 관리 센터에서 홈 gt_ 그룹 페이지에서 속성을 볼 수 있습니다. 또는 Exchange Online PowerShell에서 다음 명령을 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="27da5-p122">To get a list of the members of a Office 365 Group or Microsoft Team, you can view the properties on the Home > Groups page in the Office 365 admin center. Alternatively, you can run the following command in Exchange Online PowerShell:</span></span>

    <span data-ttu-id="27da5-211">' ' powershell</span><span class="sxs-lookup"><span data-stu-id="27da5-211">''' powershell</span></span>
    
        Get-UnifiedGroupLinks <group or team name> -LinkType Members | FL DisplayName,PrimarySmtpAddress
        '''

[!NOTE]
<span data-ttu-id="27da5-212">Get UnifiedGroupLinks cmdlet를 실행 하려면 역할을 할당 보기 권한만 있는 받는 사람에 게 Exchange 온라인 해야 하거나 역할 그룹의 구성원 이어야 하는 할당 보기 권한만 있는 받는 사람에 게 역할입니다.</span><span class="sxs-lookup"><span data-stu-id="27da5-212">To run the Get-UnifiedGroupLinks cmdlet, you have to be assigned the View-Only Recipients role in Exchange Online or be a member of a role group that's assigned the View-Only Recipients role.</span></span>

- <span data-ttu-id="27da5-p123">Microsoft 팀의 채널의 일부인 채널 대화 하는 팀과 연결 된 사서함에 저장 됩니다. 마찬가지로, 채널에서 팀 구성원을 공유 하는 파일은 팀의 SharePoint 사이트에 저장 됩니다. 따라서 Microsoft 팀 사서함 시키려면 있고 대화 및 채널에서 파일을 유지 하려면 SharePoint 사이트에 유지 합니다.</span><span class="sxs-lookup"><span data-stu-id="27da5-p123">Channel conversations that are part of a Microsoft Teams channel are stored in the mailbox that's associated with the Team. Similarly, files that team members share in a channel are stored on the team's SharePoint site. Therefore, you have to place the Microsoft Team mailbox and SharePoint site on hold to retain conversations and files in a channel.</span></span>
  
- <span data-ttu-id="27da5-p124">또는 Microsoft 팀의 채팅 목록에 포함 된 대화는 사용자의 대화방에 참가의 사서함에 저장 됩니다.  채팅 대화에 사용자를 공유 하는 파일은 파일을 공유 하는 사용자의 비즈니스 사이트에 대 한 OneDrive에 저장 됩니다. 따라서 개별 사용자 사서함을 했는지와 비즈니스 사이트에 대 한 OneDrive 대화 및 채팅 목록에서 파일을 유지 하려면 유지 합니다.</span><span class="sxs-lookup"><span data-stu-id="27da5-p124">Alternatively, conversations that are part of the Chat list in Microsoft Teams are stored in the mailbox of the user's who participate in the chat.  Files that a user shares in Chat conversations are stored in the OneDrive for Business site of the user who shares the file. Therefore, you have to place the individual user mailboxes and OneDrive for Business sites on hold to retain conversations and files in the Chat list.</span></span> 
  
- <span data-ttu-id="27da5-p125">모든 Microsoft 팀 또는 팀 채널 노트 작성 및 공동 작업에 대 한 Wiki를 포함합니다. Wiki 콘텐츠.mht 서식 사용 하 여 파일을 자동으로 저장 됩니다. 이 파일은 팀의 SharePoint 사이트에 팀이 위 키 데이터 문서 라이브러리에 저장 됩니다. 보류에서 팀의 SharePoint 사이트를 배치 하 여 대기 Wiki의 콘텐츠를 배치할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="27da5-p125">Every Microsoft Team or team channel contains a Wiki for note-taking and collaboration. The Wiki content is automatically saved to a file with a .mht format. This file is stored in the Teams Wiki Data document library on the team's SharePoint site. You can place the content in the Wiki on hold by placing the team's SharePoint site on hold.</span></span>

[!Note]
<span data-ttu-id="27da5-p126">(대기 팀의 SharePoint 사이트에 배치) 하는 경우 Microsoft 팀 또는 팀 채널에 대 한 Wiki 콘텐츠를 유지 하는 기능은 2017 년 6 월 22에 릴리스 되었습니다. 팀 사이트에는 기다리는 경우, Wiki 해당 날짜에 시작 하 여 콘텐츠를 유지 됩니다. 그러나 팀 사이트를 보류에 있고 2017 년 6 월 22, 이전 Wiki 콘텐츠 삭제 하는 경우에 Wiki 콘텐츠 보존 되지 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="27da5-p126">The capability to retain Wiki content for a Microsoft Team or team channel (when you place the team's SharePoint site on hold) was released on June 22, 2017. If a team site is on hold, the Wiki content will be retained starting on that date. However, if a team site is on hold and the Wiki content was deleted before June 22, 2017, the Wiki content was not retained.</span></span>
   