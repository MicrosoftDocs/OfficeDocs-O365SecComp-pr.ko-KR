---
title: 검색을 만들어서 데이터 수집
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: ''
ms.openlocfilehash: 14f90b29cbff9c1a588b816563178039c7af7da6
ms.sourcegitcommit: baf23be44f1ed5abbf84f140b5ffa64fce605478
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/26/2019
ms.locfileid: "30295961"
---
# <a name="create-a-search-to-collect-data"></a><span data-ttu-id="76547-102">검색을 만들어서 데이터 수집</span><span class="sxs-lookup"><span data-stu-id="76547-102">Create a search to collect data</span></span>

<span data-ttu-id="76547-103">사례에 있는 **검색** 탭에서 **새 검색** 을 클릭 하 고 마법사를 수행 하 여 새 검색을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="76547-103">On the **Searches** tab in your case, you can create a new search by clicking **New search** and following the wizard.</span></span>

## <a name="name-your-search-and-give-description"></a><span data-ttu-id="76547-104">검색 이름 지정 및 설명 입력</span><span class="sxs-lookup"><span data-stu-id="76547-104">Name your search and give description</span></span>

<span data-ttu-id="76547-p101">케이스가 포함 된 각 검색의 이름은 고유 해야 합니다. 선택적으로 검색에 대 한 설명을 제공할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="76547-p101">Each search with a case should have a unique name. You can optionally provide a description for your search.</span></span> 

## <a name="define-your-conditions"></a><span data-ttu-id="76547-107">조건 정의</span><span class="sxs-lookup"><span data-stu-id="76547-107">Define your conditions</span></span>

<span data-ttu-id="76547-p102">미리 작성 된 조건 카드를 사용 하거나 KQL (키워드 쿼리 언어)를 사용 하 여 검색 조건을 정의할 수 있습니다. 자세한 내용은 [빌드 검색 쿼리](building-search-queries.md)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="76547-p102">You can define the conditions for your search using the pre-built condition cards or using Keyword Query Language (KQL). For more information, see [Build search queries](building-search-queries.md).</span></span>

## <a name="choose-the-custodians-to-search-from"></a><span data-ttu-id="76547-110">검색할 custodians 선택</span><span class="sxs-lookup"><span data-stu-id="76547-110">Choose the custodians to search from</span></span>

<span data-ttu-id="76547-p103">조건을 정의한 후에는 검색 하려는 위치를 선택 해야 합니다. 이 작업을 수행 하는 한 가지 방법은 검색 하려는 사례에 이미 추가한 custodians를 지정 하는 것입니다. custodian를 선택 하 여 custodian에 매핑된 모든 데이터 원본에 대해 검색을 실행 합니다. 사례에 custodians을 추가 하 고 해당 데이터 원본을 관리 하는 방법에 대 한 자세한 내용은 [custodians with Work](managing-custodians.md) 를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="76547-p103">Once you have defined your conditions, you need to choose which locations you want to search. One way to do it is by specifying which custodians you have already added to the case you want to search. By selecting a custodian, you will run the search against all data sources mapped to the custodian. See [Work with custodians](managing-custodians.md) for more information on how to add custodians to your case and manage their data sources.</span></span>

## <a name="choose-non-custodial-locations"></a><span data-ttu-id="76547-115">비 custodial 위치 선택</span><span class="sxs-lookup"><span data-stu-id="76547-115">Choose non-custodial locations</span></span>

<span data-ttu-id="76547-p104">어떤 경우에는 custodian에 매핑되지 않은 데이터 원본을 검색할 수도 있습니다. 이 경우 검색할 위치를 지정 하거나, 모든 Exchange 사서함 또는 모든 SharePoint 및 비즈니스용 OneDrive 사이트 검색과 같은 특정 Office 365 서비스의 모든 콘텐츠 위치를 검색 하도록 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="76547-p104">In some cases, you may wish to search data sources that are not mapped to a custodian. In this case, you can specify the locations you would like to search, or choose to search all content locations for a specific Office 365 service (such as searching all Exchange mailboxes or all SharePoint and OneDrive for Business sites).</span></span>