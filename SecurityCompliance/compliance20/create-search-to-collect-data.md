---
title: 데이터 수집에 대 한 검색 만들기
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
ms.openlocfilehash: 3ebb9a40d3fb055fbb88b32175a4a22df3da44af
ms.sourcegitcommit: ee28ee2b2bdfd049333c2f495d7f7780d13af4a6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2019
ms.locfileid: "29608175"
---
# <a name="create-a-search-to-collect-data"></a><span data-ttu-id="68189-102">데이터 수집에 대 한 검색 만들기</span><span class="sxs-lookup"><span data-stu-id="68189-102">Create a search to collect data</span></span>

<span data-ttu-id="68189-103">사용자의 경우에서 **검색** 탭에서 마법사를 수행 하 고 **새로 만들기를 검색** 을 클릭 하 여 새 검색을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="68189-103">On the **Searches** tab in your case, you can create a new search by clicking **New search** and following the wizard.</span></span>

## <a name="name-your-search-and-give-description"></a><span data-ttu-id="68189-104">검색 이름을 지정 하 고 설명을 제공 하십시오.</span><span class="sxs-lookup"><span data-stu-id="68189-104">Name your search and give description</span></span>

<span data-ttu-id="68189-p101">사례와 각 검색 고유한 이름이 있어야 합니다. 필요에 따라 검색에 대 한 설명을 제공할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="68189-p101">Each search with a case should have a unique name. You can optionally provide a description for your search.</span></span> 

## <a name="define-your-conditions"></a><span data-ttu-id="68189-107">규칙의 조건과 정의</span><span class="sxs-lookup"><span data-stu-id="68189-107">Define your conditions</span></span>

<span data-ttu-id="68189-p102">미리 작성된 된 조건 카드를 사용 하 여 또는 키워드 쿼리 언어 (KQL)를 사용 하 여 검색에 대 한 조건을 정의할 수 있습니다. 자세한 내용은 [검색 쿼리 작성을](building-search-queries.md)참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="68189-p102">You can define the conditions for your search using the pre-built condition cards or using Keyword Query Language (KQL). For more information, see [Building search queries](building-search-queries.md).</span></span>

## <a name="choose-the-custodians-to-search-from"></a><span data-ttu-id="68189-110">검색 하려면 custodians를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="68189-110">Choose the custodians to search from</span></span>

<span data-ttu-id="68189-p103">규칙의 조건과 정의한 경우를 검색 하려면 하는 위치를 선택 해야 합니다. 작업을 수행 하는 한 가지 방법은 검색 하려는 경우에 이미 추가 하는 custodians를 지정 하 여 됩니다. 프로그램 관리자를 선택 하 여 더불어에 매핑된 모든 데이터 원본에 대 한 검색을 실행 합니다. 사례에 custodians를 추가 하 고 해당 데이터 원본을 관리 하는 방법에 대 한 자세한 내용은 [custodians (영문)을](managing-custodians.md) 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="68189-p103">Once you have defined your conditions, you need to choose which locations you want to search. One way to do it is by specifying which custodians you have already added to the case you want to search. By selecting a custodian, you will run the search against all data sources mapped to the custodian. See [Working with custodians](managing-custodians.md) for more information on how to add custodians to your case and manage their data sources.</span></span>

## <a name="choose-non-custodial-locations"></a><span data-ttu-id="68189-115">Custodial 아닌 위치를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="68189-115">Choose non-custodial locations</span></span>

<span data-ttu-id="68189-p104">일부 경우에는 더불어에 매핑되지 않은 데이터 원본을 검색 하는 것이 좋습니다. 이 경우 검색 하거나 특정 Office 365 서비스 (예: 비즈니스 사이트에 대 한 모든 Exchange 사서함 또는 모든 SharePoint와 OneDrive 검색)에 대 한 모든 콘텐츠 위치를 검색 하도록 선택 하려는 위치를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="68189-p104">In some cases, you may wish to search data sources that are not mapped to a custodian. In this case, you can specify the locations you would like to search, or choose to search all content locations for a specific Office 365 service (such as searching all Exchange mailboxes or all SharePoint and OneDrive for Business sites).</span></span>