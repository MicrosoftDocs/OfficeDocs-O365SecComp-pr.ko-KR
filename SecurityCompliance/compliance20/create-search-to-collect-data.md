---
title: Create a search
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: ''
ms.openlocfilehash: 1aa4ce6e406e4b3a3b72b9d93f651416b1fc65f9
ms.sourcegitcommit: 803baca9f99a6691fb41a3308e799752e4d8f20c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/25/2019
ms.locfileid: "35222252"
---
# <a name="create-a-search"></a><span data-ttu-id="518be-102">Create a search</span><span class="sxs-lookup"><span data-stu-id="518be-102">Create a search</span></span>

<span data-ttu-id="518be-103">사례에 있는 **검색** 탭에서 **새 검색** 을 클릭 하 고 마법사를 수행 하 여 새 검색을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="518be-103">On the **Searches** tab in your case, you can create a new search by clicking **New search** and following the wizard.</span></span>

## <a name="name-your-search-and-give-it-a-description"></a><span data-ttu-id="518be-104">검색의 이름을 지정 하 고 설명을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="518be-104">Name your search and give it a description</span></span>

<span data-ttu-id="518be-105">케이스가 포함 된 각 검색의 이름은 고유 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="518be-105">Each search with a case should have a unique name.</span></span> <span data-ttu-id="518be-106">선택적으로 검색에 대 한 설명을 제공할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="518be-106">You can optionally provide a description for your search.</span></span> 

## <a name="define-your-search-query-and-conditions"></a><span data-ttu-id="518be-107">검색 쿼리 및 조건 정의</span><span class="sxs-lookup"><span data-stu-id="518be-107">Define your search query and conditions</span></span>

<span data-ttu-id="518be-108">미리 작성 된 조건 카드를 사용 하거나 KQL (키워드 쿼리 언어)를 사용 하 여 검색에 대 한 키워드 쿼리 및 조건을 정의할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="518be-108">You can define the keywords query and any conditions for the search by using the pre-built condition cards or using Keyword Query Language (KQL).</span></span> <span data-ttu-id="518be-109">자세한 내용은 [빌드 검색 쿼리](building-search-queries.md)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="518be-109">For more information, see [Build search queries](building-search-queries.md).</span></span>

## <a name="choose-the-custodians-to-search-from"></a><span data-ttu-id="518be-110">검색할 custodians 선택</span><span class="sxs-lookup"><span data-stu-id="518be-110">Choose the custodians to search from</span></span>

<span data-ttu-id="518be-111">조건을 정의한 후에는 검색 하려는 위치를 선택 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="518be-111">Once you have defined your conditions, you need to choose which locations you want to search.</span></span> <span data-ttu-id="518be-112">이 작업을 수행 하는 한 가지 방법은 검색 하려는 사례에 이미 추가한 custodians를 지정 하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="518be-112">One way to do it is by specifying which custodians you have already added to the case you want to search.</span></span> <span data-ttu-id="518be-113">Custodian를 선택 하 여 custodian에 매핑된 모든 데이터 원본에 대해 검색을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="518be-113">By selecting a custodian, you will run the search against all data sources mapped to the custodian.</span></span> <span data-ttu-id="518be-114">사례에 custodians을 추가 하 고 해당 데이터 원본을 관리 하는 방법에 대 한 자세한 내용은 [custodians With Work](managing-custodians.md) 를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="518be-114">See [Work with custodians](managing-custodians.md) for more information on how to add custodians to your case and manage their data sources.</span></span>

## <a name="choose-non-custodial-locations"></a><span data-ttu-id="518be-115">비 custodial 위치 선택</span><span class="sxs-lookup"><span data-stu-id="518be-115">Choose non-custodial locations</span></span>

<span data-ttu-id="518be-116">어떤 경우에는 custodian에 매핑되지 않은 데이터 원본을 검색할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="518be-116">In some cases, you may wish to search data sources that are not mapped to a custodian.</span></span> <span data-ttu-id="518be-117">이 경우 검색할 위치를 지정 하거나, 모든 Exchange 사서함 또는 모든 SharePoint 및 비즈니스용 OneDrive 사이트 검색과 같은 특정 Office 365 서비스의 모든 콘텐츠 위치를 검색 하도록 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="518be-117">In this case, you can specify the locations you would like to search, or choose to search all content locations for a specific Office 365 service (such as searching all Exchange mailboxes or all SharePoint and OneDrive for Business sites).</span></span>