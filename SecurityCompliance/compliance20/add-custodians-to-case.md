---
title: Custodians (미리 보기) 고급 eDiscovery 사례에 추가
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
ms.openlocfilehash: d9a7dc6b1c2eeffdcd49be64d1d09d4a2bda782b
ms.sourcegitcommit: ee28ee2b2bdfd049333c2f495d7f7780d13af4a6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2019
ms.locfileid: "29608147"
---
# <a name="add-custodians-to-an-advanced-ediscovery-preview-case"></a><span data-ttu-id="f70de-102">고급 eDiscovery (미리 보기)에 custodians 추가 대/소문자</span><span class="sxs-lookup"><span data-stu-id="f70de-102">Add custodians to an Advanced eDiscovery (Preview) Case</span></span>

<span data-ttu-id="f70de-p101">고급 eDiscovery (미리 보기)를 사용 하 여을 중심으로 custodians를 관리 하 고 사례 내 관련, custodial 데이터 원본을 식별 하 여 워크플로 조정 하는 기본 제공 더불어 관리 도구를 활용할 수 있습니다. 프로그램 관리자를 추가 하면 자동으로 식별 하 고 시스템 수, 전체를 포함 하 고 기본 Exchange 사서함 및 OneDrive에 비즈니스 사이트에 대 한 합니다. 사용자 검색을 수행 하는 대로 당기기 수 및 추가 사서함 또는 사이트는 한 더불어 액세스 과거 또는 팀에는 더불어 오늘날의 구성원 인지 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="f70de-p101">Using Advanced eDiscovery (Preview), you can leverage the built-in custodian management tool to coordinate your workflows around managing custodians and identifying relevant, custodial data sources within a case. When you add a custodian, the system can automatically identify, and place holds on their primary Exchange mailbox and OneDrive for Business site. As you conduct your discovery, you might also uncover and map additional mailboxes or sites that a custodian accessed in the past or Teams that a custodian is a member of today.</span></span>

<span data-ttu-id="f70de-106">다음 워크플로 사용 하 여 추가 하 고 보안 & 준수 센터 내에서 고급 eDiscovery (미리 보기)의 경우 custodians를 관리 합니다.</span><span class="sxs-lookup"><span data-stu-id="f70de-106">Use the following workflow to add and manage custodians in Advanced eDiscovery (Preview) cases within the Security & Compliance Center.</span></span> 

## <a name="step-1-identify-potential-custodians"></a><span data-ttu-id="f70de-107">1 단계: 잠재적 custodians를 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="f70de-107">Step 1: Identify potential custodians</span></span>

<span data-ttu-id="f70de-p102">첫번째 단계 프로그램 문제에 대 한 적절 한 custodians를 식별 하는 것입니다. Custodians 사례에 추가할 eDiscovery 관리자의 구성원 또는 eDiscovery 관리자 역할 그룹 이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="f70de-p102">The first step is to identify the appropriate custodians for your matter. To add custodians to a case, you must be a member of the eDiscovery Managers or eDiscovery Admins role group.</span></span>   

<span data-ttu-id="f70de-110">기존 고급 eDiscovery (미리 보기) 사례에 custodians를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="f70de-110">To add custodians to an existing Advanced eDiscovery (Preview) case:</span></span>

1. <span data-ttu-id="f70de-111">**고급 eDiscovery (미리 보기)** 페이지에서 케이스로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="f70de-111">From the **Advanced eDiscovery (Preview)** page, go to your case.</span></span>
 
2. <span data-ttu-id="f70de-112">사례를 선택한 후 **Custodians** 탭으로 이동 하 고 **추가 더불어 + 기호**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="f70de-112">After you have selected a case, go to the **Custodians** tab and click **+ Add Custodian**.</span></span> 
 
3. <span data-ttu-id="f70de-p103">대/소문자에 추가 하려는 custodians를 선택 합니다. 조직의 Azure Active Directory에서 사용자를 선택 하 고 검색을 입력 하 여 시작할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f70de-p103">Choose the custodians that you want to add to the case. You can start by typing to search and select the users from your organization's Azure Active Directory.</span></span>
 
4. <span data-ttu-id="f70de-115">Custodians 목록이 완성 한 후 **다음** 잠재적 데이터 원본 식별 시작을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="f70de-115">After you have finalized the list of custodians, click **Next** to begin identifying potential data sources.</span></span> 
   
## <a name="optional-step-2-select-custodian-data-sources"></a><span data-ttu-id="f70de-116">(선택 사항) 2 단계: 더불어 데이터 원본 선택</span><span class="sxs-lookup"><span data-stu-id="f70de-116">(Optional) Step 2: Select custodian data sources</span></span>

<span data-ttu-id="f70de-p104">Custodians 사례에 추가한 후 식별 하 고 기본 더불어 데이터 원본 유지 하는데 도움이 되는 Office 365를 활용할 수 있습니다. 이 워크플로에서 다음 단계에서는 1 단계에서에서 지정한 custodians 소유 하 고 데이터 원본을 선택 하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="f70de-p104">After you have added custodians to a case, you can leverage Office 365 to help you identify and preserve the primary custodian data sources. The next step in this workflow is to select the data sources owned by the custodians specified in Step 1.</span></span> 

<span data-ttu-id="f70de-119">식별 하려면 더불어 데이터 원본:</span><span class="sxs-lookup"><span data-stu-id="f70de-119">To identify custodian data sources:</span></span> 

1. <span data-ttu-id="f70de-120">각 더불어에 대 한 시스템 자동으로 식별 하 고 더불어의 기본 Exchange 사서함을 추가 하 고 싶은 경우 **Exchange** 를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="f70de-120">For each custodian, select **Exchange** if you would like the system to automatically identify and add the custodian's primary Exchange mailbox.</span></span> 
 
2. <span data-ttu-id="f70de-121">각 더불어에 대 한 시스템 자동으로 식별 하 고 더불어의 기본 OneDrive URL을 추가 하 고 싶은 경우 **OneDrive** 를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="f70de-121">For each custodian, select **OneDrive** if you would like the system to automatically identify and add the custodian's primary OneDrive URL.</span></span> 

    <span data-ttu-id="f70de-122">선택 항목을 변경한 후 이러한 시스템에서 자동으로 데이터 원본 식별 및 사례에 추가할을 시도 합니다.</span><span class="sxs-lookup"><span data-stu-id="f70de-122">After you've made your selections, they system will automatically try to identify the data sources and add them to your case.</span></span>
 
4. <span data-ttu-id="f70de-123">**다음** 을 시작 하려면 프로그램 더불어에 추가 데이터 원본 매핑 (영문)를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="f70de-123">Click **Next** to begin mapping additional data sources to your custodian.</span></span>

## <a name="optional-step-3-map-additional-data-sources"></a><span data-ttu-id="f70de-124">(선택 사항) 3 단계: 추가 데이터 원본 매핑</span><span class="sxs-lookup"><span data-stu-id="f70de-124">(Optional) Step 3: Map additional data sources</span></span>

<span data-ttu-id="f70de-p105">사용자의 경우에 따라 수도 추가 하려는 주어진된 더불어를 사용 하 여 과거에 있을 수 있는 사서함을는 더불어는 이전에 대 한 액세스 하는 관리자가 현재 구성원을 하거나 사이트 위치 그룹화 합니다. 기본 더불어 데이터 원본의 경우 외에도 프로그램 더불어 추가 Office 365 데이터 원본에 추가할 수도 있고 잠재적으로 관련 된 데이터 원본에도 확인할 수 있도록 Office 365를 활용 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f70de-p105">Depending on your case, you may also want to add mailboxes that a given custodian may have used in the past, groups where a custodian is currently a member, or sites that a custodian had access to in the past. In addition to primary custodian data sources, you can add additional Office 365 data sources to a custodian or leverage Office 365 to help you identify potentially relevant data sources as well.</span></span> 

<span data-ttu-id="f70de-127">사서함, 사이트 또는 팀에 매핑할 특정 더불어:</span><span class="sxs-lookup"><span data-stu-id="f70de-127">To map mailboxes, sites, or teams to a specific custodian:</span></span>
1. <span data-ttu-id="f70de-128">특정 더불어에 사서함, 사이트 및 팀과 같은 콘텐츠 위치를 할당 하려면 **업데이트** 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="f70de-128">Select **Update** to assign content locations, like mailboxes, sites, and Teams, to a specific custodian.</span></span> 

2. <span data-ttu-id="f70de-129">플라이 아웃에서 다음을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f70de-129">In the flyout, specify the following:</span></span>
   
  -  <span data-ttu-id="f70de-p106">**Exchange 사서함** - **선택 사용자, 그룹 또는 팀을** 클릭 하 고 **선택 사용자, 그룹 또는 팀을** 다시 클릭 합니다. 선택한 더불어에 할당 하는 사서함을 지정 하려면 검색 상자를 사용 하 여 사용자 사서함 및 메일 그룹을 찾을 수 있습니다. 또한는 Office 365 그룹 또는 팀이 Microsoft에 대 한 연결 된 사서함을 할당할 수 있습니다. 사용자, 그룹, 팀 확인란을 선택 하 고 **선택**를클릭하고 **완료**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="f70de-p106">**Exchange Mailboxes** - Click **Choose users, groups, or Teams** and then click **Choose users, groups, or teams** again. To specify mailboxes to assign to the selected custodian, use the search box to find user mailboxes and distribution groups. You can also assign the associated mailbox for an Office 365 Group or a Microsoft Team. Select the user, group, team check box, click **Choose**, and then click **Done**.</span></span>

      > [!NOTE]
      > <span data-ttu-id="f70de-p107">선택의 사용자, 그룹 또는 팀이 사서함을 지정 하려면를 클릭 하면 표시 되는 사서함 선택 비어 있습니다. 성능 향상을 위해 디자인입니다. 이 목록에 사용자를 추가할 검색 상자에 이름 (최소 3 자)를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="f70de-p107">When you click Choose users, groups, or teams to specify mailboxes, the mailbox picker that's displayed is empty. This is by design to enhance performance. To add people to this list, type a name (a minimum of 3 characters) in the search box.</span></span>
     
   - <span data-ttu-id="f70de-p108">**SharePoint 사이트** - **선택 사이트** 를 클릭 하 고 선택한 더불어에 할당 하려는 비즈니스 사이트에 대 한 추가 SharePoint와 OneDrive 지정을 다시 **선택 사이트** 클릭 합니다. Office 365 그룹 또는 팀이 Microsoft에 대 한 SharePoint 사이트에 대 한 URL을 추가할 수도 있습니다. 할당 하려는 각 사이트에 대 한 URL을 입력 합니다. **Choose**클릭 하 고 **완료**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="f70de-p108">**SharePoint Sites** - Click **Choose sites** and then click **Choose sites** again to specify additional SharePoint and OneDrive for Business sites that you would like to assign to the selected custodian. You can also add the URL for the SharePoint site for an Office 365 Group or a Microsoft Team. Type the URL for each site that you want to assign. Click **Choose**, and then click **Done**.</span></span>
   - <span data-ttu-id="f70de-p109">**Microsoft 팀의** - **팀 선택** 누르고 더불어 오늘날의 구성원 인지 Microsoft 팀 그룹의 목록을 보려면를 다시 **팀을 선택** 합니다. 더불어 대화에 추가 하려고 하는 팀을 선택 합니다. 이 옵션을 선택 되 면 시스템은 자동으로 해당 Microsoft 팀에 연결 된 SharePoint 사이트 및 그룹 사서함에 연결 하는 & 선택을 식별 합니다. **Choose**클릭 하 고 **완료**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="f70de-p109">**Microsoft Teams** – Click **Choose Teams** and then click **Choose Teams** again to view a list of Microsoft Team groups that the custodian is a member of today. Select the Teams that you would like to add to your custodian. Once selected, the system will automatically identify & select the associated SharePoint site and Group Mailbox associated to that Microsoft Team. Click **Choose**, and then click **Done**.</span></span>
        
      > [!NOTE]
      > <span data-ttu-id="f70de-145">Microsoft 팀의 추가 추가 하려면 별도로 사서함 및 위에 표시 된 것과 같이 SharePoint 사이트를 추가 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="f70de-145">To add additional Microsoft Teams, you will need to separately add the mailbox and SharePoint site as shown above.</span></span>

<span data-ttu-id="f70de-p110">원본에 매핑 (영문)를 완료 한 후 방금 추가한 custodians에 대 한 총 사서함 수, 사이트 및 팀을 볼 수 있습니다. 특정 더불어에 대 한 관련 데이터 원본을 완료 했을 때 때이 매핑을 유지 관리 하 고 eDiscovery 수집, 처리 및 검토 워크플로에 확장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f70de-p110">After you have finished mapping your sources, you can view the total mailboxes, sites, and Teams for the custodians that you have just added. When you've finalized the data sources relevant for a specific custodian, this mapping will be maintained and extended to the eDiscovery collection, processing, and review workflows.</span></span> 

## <a name="optional-step-4-place-custodians-on-hold"></a><span data-ttu-id="f70de-148">(선택 사항) 4 단계: 전체에 custodians 유지</span><span class="sxs-lookup"><span data-stu-id="f70de-148">(Optional) Step 4: Place custodians on hold</span></span>

 <span data-ttu-id="f70de-p111">Custodians 및 사례에 추가 하려는 데이터 원본, 종료한 후 일부 필요에 따라 배치할 수 있습니다 또는에서 custodians 대화의 모든 보류 합니다. 대기를 더불어를 배치 하는 경우 해당 사용자에 게 매핑된 콘텐츠는 대/소문자에서 또는 보류를 삭제할 때까지 더불어를 놓을 때까지 유지 됩니다. 경우에 따라 보류에서이 배치 하지 않고 custodians 사례에 추가 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="f70de-p111">After you have finalized the custodians and data sources that you would like to add to your case, you can optionally place some or all of your custodians on hold. When you place a custodian on hold, the content mapped to that user is held until you release the custodian from the case or until you delete the hold. In some cases, you may want to add custodians to a case without placing them on hold.</span></span> 

<span data-ttu-id="f70de-152">시키려면에서 선택한 custodians 및 데이터 원본 유지 합니다.</span><span class="sxs-lookup"><span data-stu-id="f70de-152">To place the selected custodians and data sources on hold:</span></span>

1. <span data-ttu-id="f70de-p112">더불어 선택 사항을 확인 하 고 각 더불어를 대기 시키려면 checkox를 선택 합니다. 더불어 보류에 배치 되 면 되 면 모든 custodial 소스를 포함 하는 더불어 보류 정책은 자동으로 만들어집니다. 옵션을 선택 하지 않으면 하는 경우 더불어 & 선택한 데이터 원본 대/소문자에 추가 되지만 콘텐츠 유지 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f70de-p112">Verify your custodian selections and select the checkox to place each custodian on hold.Once a custodian is placed on hold, a custodian hold policy containing all custodial sources will automatically be created. If the option is not checked, the custodian & selected data sources will be added to the case but the content will not be preserved.</span></span>

2. <span data-ttu-id="f70de-155">**포함 하 고** 탭으로 이동 하 고 **더불어 보관 정책**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="f70de-155">Go to the **Holds** tab and select the **Custodian Hold Policy**.</span></span> 

3. <span data-ttu-id="f70de-156">모든 선택한 더불어 데이터 원본 보기를 **편집** 을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="f70de-156">Click **Edit** to view all the selected custodian data sources.</span></span>
