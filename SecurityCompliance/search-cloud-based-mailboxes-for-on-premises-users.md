---
title: Office 365에서 온-프레미스 사용자에 대 한 클라우드 기반 사서함 검색
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 6/4/2018
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
ms.collection: M365-security-compliance
localization_priority: Normal
search.appverid:
- MOE150
- MST160
- MET150
ms.assetid: 3f7dde1a-a8ea-4366-86da-8ee6777f357c
description: 보안 & 준수 센터의 콘텐츠 검색 도구를 사용 하 여 Exchange 하이브리드 배포에서 온-프레미스 사용자에 대 한 MicrosoftTeams 채팅 데이터를 검색 하 고 내보냅니다 (1xn 채팅 이라고 함).
ms.openlocfilehash: 0c68023fdd4e1c9e06596937247270861cdbd2b3
ms.sourcegitcommit: e7a776a04ef6ed5e287a33cfdc36aa2d72862b55
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/29/2019
ms.locfileid: "31000011"
---
# <a name="searching-cloud-based-mailboxes-for-on-premises-users-in-office-365"></a><span data-ttu-id="c8673-103">Office 365에서 온-프레미스 사용자에 대 한 클라우드 기반 사서함 검색</span><span class="sxs-lookup"><span data-stu-id="c8673-103">Searching cloud-based mailboxes for on-premises users in Office 365</span></span>

<span data-ttu-id="c8673-104">조직에 Exchange 하이브리드 배포가 있고 Microsoft 팀을 사용 하도록 설정 하면 사용자는 인스턴트 메시징을 위해 팀 채팅 응용 프로그램을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c8673-104">If your organization has an Exchange hybrid deployment and has enabled Microsoft Teams, users can use the Teams chat application for instant messaging.</span></span> <span data-ttu-id="c8673-105">클라우드 기반 사용자의 경우 팀 채팅 데이터 (1xn 채팅이 라고도 함)가 기본 클라우드 기반 사서함에 저장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c8673-105">For the cloud-based user, the Teams chat data (also called 1xN chats) is saved to their primary cloud-based mailbox.</span></span> <span data-ttu-id="c8673-106">온-프레미스 사용자가 팀 채팅 응용 프로그램을 사용 하는 경우 기본 사서함은 온-프레미스에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c8673-106">When an on-premises user uses the Team chat application, their primary mailbox is located on-premises.</span></span> <span data-ttu-id="c8673-107">이러한 제한을 해결 하기 위해 Microsoft는 온-프레미스 사용자를 위한 팀 채팅 데이터를 저장 하기 위해 클라우드 기반 저장소 영역 (온-프레미스 사용자를 위한 클라우드 기반 사서함)을 만들기 위한 새로운 기능을 출시 했습니다.</span><span class="sxs-lookup"><span data-stu-id="c8673-107">To get around this limitation, Microsoft has released a new feature where a cloud-based storage area (called a cloud-based mailbox for on-premises users) is created to store Teams chat data for on-premises users.</span></span> <span data-ttu-id="c8673-108">이를 통해 보안 & 준수 센터의 콘텐츠 검색 도구를 사용 하 여 온-프레미스 사용자의 팀 채팅 데이터를 검색 하 고 내보낼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c8673-108">This lets you use the Content Search tool in the Security & Compliance Center to search and export Teams chat data for on-premises users.</span></span> 
  
<span data-ttu-id="c8673-109">온-프레미스 사용자에 대해 클라우드 기반 사서함을 설정 및 검색 하기 위한 요구 사항 및 제한 사항은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="c8673-109">Here are the requirements and limitation for setting up and to set up and search cloud-based mailboxes for on-premises users:</span></span>
  
- <span data-ttu-id="c8673-110">온-프레미스 디렉터리 서비스의 사용자 계정 (예: Active directory)은 Office 365의 디렉터리 서비스인 Azure Active directory와 동기화 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c8673-110">The user accounts in your on-premises directory service (such as Active Directory) must be synchronized with Azure Active Directory, the directory service in Office 365.</span></span> <span data-ttu-id="c8673-111">즉, 메일 사용자 계정이 Office 365에 만들어지고 기본 사서함이 온-프레미스 조직에 있는 사용자와 연결 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c8673-111">This means that a mail user account is created in Office 365 and is associated with a user whose primary mailbox is located in the on-premises organization.</span></span>
    
- <span data-ttu-id="c8673-112">온-프레미스 사용자를 위한 클라우드 기반 사서함은 팀 채팅 데이터를 저장 하는 경우에만 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c8673-112">The cloud-based mailbox for on-premises users is used only store Teams chat data.</span></span> <span data-ttu-id="c8673-113">온-프레미스 사용자가 클라우드 기반 사서함에 로그인 하거나 어떤 방식으로든 액세스를 수행할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="c8673-113">An on-premises user can't sign in to the cloud-based mailbox or access in any way.</span></span> <span data-ttu-id="c8673-114">전자 메일 메시지를 보내거나 받는 데 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="c8673-114">It can't be used to send or receive email messages.</span></span> 
    
- <span data-ttu-id="c8673-115">조직에서 온-프레미스 사용자의 클라우드 기반 사서함에서 팀 채팅 데이터를 검색할 수 있도록 하려면 Microsoft 지원 요청을 제출 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c8673-115">You have to submit a request to Microsoft Support to enable your organization to search for Teams chat data in the cloud-based mailboxes for on-premises users.</span></span> <span data-ttu-id="c8673-116">이 문서에서 [이 기능을 사용 하도록 설정 하려면 Microsoft Support에 대 한 요청 관리를](#filing-a-request-with-microsoft-support-to-enable-this-feature) 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="c8673-116">See [Filing a request with Microsoft Support to enable this feature](#filing-a-request-with-microsoft-support-to-enable-this-feature) in this article.</span></span> 
    
 <span data-ttu-id="c8673-117">**참고:** 팀 채널 대화는 항상 팀과 연결 된 클라우드 기반 사서함에 저장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c8673-117">**Note:** Teams channel conversations are always stored in the cloud-based mailbox that's associated with the Team.</span></span> <span data-ttu-id="c8673-118">즉, 지원 요청을 파일 하지 않고도 콘텐츠 검색을 통해 채널 대화를 검색할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c8673-118">That means you can use Content Search to search channel conversations without have to file a support request.</span></span> <span data-ttu-id="c8673-119">팀 채널 대화 검색에 대 한 자세한 내용은 [Microsoft 팀 및 Office 365 그룹 검색](content-search.md#searching-microsoft-teams-and-office-365-groups)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="c8673-119">For more information about searching Teams channel conversations, see [Searching Microsoft Teams and Office 365 Groups](content-search.md#searching-microsoft-teams-and-office-365-groups).</span></span>
  
## <a name="how-it-works"></a><span data-ttu-id="c8673-120">작업 방법</span><span class="sxs-lookup"><span data-stu-id="c8673-120">How it works</span></span>

<span data-ttu-id="c8673-121">microsoft 팀 사용 가능 사용자에 게 온-프레미스 사서함이 있고 해당 사용자 계정/id가 클라우드와 동기화 된 경우 microsoft는 클라우드 기반 사서함을 만들어 1xn 팀 채팅 데이터를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="c8673-121">If a Microsoft Teams-enabled user has an on-premises mailbox and their user account/identity has been synched to the cloud, Microsoft creates a cloud-based mailbox to store 1xN Teams chat data.</span></span> <span data-ttu-id="c8673-122">팀 채팅 데이터가 클라우드 기반 사서함에 저장 된 후에는 검색을 위해 인덱싱됩니다.</span><span class="sxs-lookup"><span data-stu-id="c8673-122">After the Teams chat data is stored in the cloud-based mailbox, it's indexed for search.</span></span> <span data-ttu-id="c8673-123">이를 통해 콘텐츠 검색 (및 eDiscovery 사례와 연결 된 검색)을 사용 하 여 온-프레미스 사용자에 대 한 팀 채팅 데이터를 검색, 미리 보기 및 내보낼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c8673-123">This lets you Use Content Search (and searches associated with eDiscovery cases) to search, preview, and export Teams chat data for on-premises users.</span></span> <span data-ttu-id="c8673-124">또한 Security & 준수 센터 PowerShell에서 \*\* \*ComplianceSearch\*\* cmdlet을 사용 하 여 온-프레미스 사용자의 팀 채팅 데이터를 검색할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c8673-124">You can also use **\*ComplianceSearch** cmdlets in the Security & Compliance Center PowerShell to search for Teams chat data for on-premises users.</span></span> 
  
<span data-ttu-id="c8673-125">다음 그림에서는 온-프레미스 사용자의 팀 채팅 데이터를 검색, 미리 보기 및 내보낼 수 있는 방식에 대 한 워크플로를 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="c8673-125">The following graphic shows the workflow of how Teams chat data for on-premises users is available to search, preview, and export.</span></span>
  
![Microsoft 팀의 온-프레미스 사용자를 위한 클라우드 기반 저장소](media/895845f8-2ceb-47ed-96c9-5ab7f1aea916.png)
  
<span data-ttu-id="c8673-127">이 새로운 기능 외에도, 콘텐츠 검색을 사용 하 여 클라우드 기반 SharePoint 사이트에서 팀 콘텐츠를 검색, 미리 보기 및 내보낼 수 있으며, 각 Microsoft 팀에 연결 된 exchange 사서함 및 exchange Online 사서함의 1xn 팀 채팅 데이터를 사용할 수도 있습니다. 클라우드 기반 사용자</span><span class="sxs-lookup"><span data-stu-id="c8673-127">In addition to this new capability, you can still use Content Search to search, preview, and export Teams content in the cloud-based SharePoint site and Exchange mailbox associated with each Microsoft Team and 1xN Teams chat data in the Exchange Online mailbox for cloud-based users.</span></span>

## <a name="filing-a-request-with-microsoft-support-to-enable-this-feature"></a><span data-ttu-id="c8673-128">이 기능을 사용 하도록 설정 하기 위해 Microsoft 지원 서비스에 요청</span><span class="sxs-lookup"><span data-stu-id="c8673-128">Filing a request with Microsoft Support to enable this feature</span></span>

<span data-ttu-id="c8673-129">조직이 온-프레미스 사용자의 클라우드 기반 사서함에서 팀 채팅 데이터를 검색할 수 있도록 하려면 Microsoft Support에 대 한 요청을 파일 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c8673-129">You must file a request with Microsoft Support to enable your organization to use the graphical user interface in the Security & Compliance Center to search for Teams chat data in the cloud-based mailboxes for on-premises users.</span></span> <span data-ttu-id="c8673-130">이 기능은 Security & 준수 센터 PowerShell에서 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c8673-130">Note that this feature is available in Security & Compliance Center PowerShell.</span></span> <span data-ttu-id="c8673-131">PowerShell을 사용 하 여 온-프레미스 사용자의 팀 채팅 데이터를 검색 하기 위해 지원 요청을 제출할 필요는 없습니다.</span><span class="sxs-lookup"><span data-stu-id="c8673-131">You don't have to submit a support request to use PowerShell to search for Teams chat data for on-premises users.</span></span> 
  
<span data-ttu-id="c8673-132">Microsoft 지원 서비스에 요청을 제출할 때 다음 정보를 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="c8673-132">Include the following information when you submit the request to Microsoft Support:</span></span>
  
- <span data-ttu-id="c8673-133">Office 365 조직의 기본 도메인 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c8673-133">The default domain name of your Office 365 organization.</span></span>
    
- <span data-ttu-id="c8673-134">Office 365 조직의 테 넌 트 이름 및 테 넌 트 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="c8673-134">The tenant name and tenant ID of your Office 365 organization.</span></span> <span data-ttu-id="c8673-135">Azure Active Directory 포털 ( **속성** **관리** \> )에서 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c8673-135">You can find these in the Azure Active Directory portal (under **Manage** \> **Properties**).</span></span> <span data-ttu-id="c8673-136">[Office 365 테 넌 트 ID 찾기를](https://support.office.com/article/6891b561-a52d-4ade-9f39-b492285e2c9b)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="c8673-136">See [Find your Office 365 tenant ID](https://support.office.com/article/6891b561-a52d-4ade-9f39-b492285e2c9b).</span></span>
    
- <span data-ttu-id="c8673-137">다음은 "온-프레미스 사용자를 위해 응용 프로그램 콘텐츠 검색을 사용 하도록 설정 합니다." 라는 지원 요청 목적에 대 한 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="c8673-137">The following title or description of the purpose of the support request: "Enable Application Content Search for On-premises Users".</span></span> <span data-ttu-id="c8673-138">이를 통해 요청을 구현할 Office 365 eDiscovery 엔지니어링 팀에 게 요청을 라우팅할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c8673-138">This will help route the request to the Office 365 eDiscovery engineering team who will implement the request.</span></span> 
    
<span data-ttu-id="c8673-139">엔지니어링이 변경 되 면 Microsoft Support에서 예상 배포 날짜를 보내 집니다.</span><span class="sxs-lookup"><span data-stu-id="c8673-139">After the engineering change is made, Microsoft Support will send you an estimated deployment date.</span></span> <span data-ttu-id="c8673-140">배포 프로세스는 일반적으로 지원 요청을 제출한 후 2-3 주 정도 걸립니다.</span><span class="sxs-lookup"><span data-stu-id="c8673-140">Note that the deployment process usually takes 2-3 weeks after you submit the support request.</span></span> 
  
### <a name="what-happens-after-this-feature-is-enabled"></a><span data-ttu-id="c8673-141">이 기능이 사용 하도록 설정 된 후에 수행 되는 작업</span><span class="sxs-lookup"><span data-stu-id="c8673-141">What happens after this feature is enabled?</span></span>

<span data-ttu-id="c8673-142">이 기능이 Office 365 조직에 배포 된 후에는 보안 & 준수 센터에서 eDiscovery 사례와 연결 된 콘텐츠 검색 및 검색에서 다음 변경 내용이 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c8673-142">After this feature is deployed in your Office 365 organization, the following changes are made in Content Search and in searches associated with an eDiscovery case in the Security & Compliance Center:</span></span>
  
- <span data-ttu-id="c8673-143">**온-프레미스 사용자에 대 한 Office 앱 콘텐츠 추가** 확인란은 콘텐츠 검색의 **위치** 아래에 추가 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c8673-143">The **Add Office app content for on-premises users** checkbox is added under the **Locations** in Content Search.</span></span> 
    
    ![콘텐츠 검색 UI에 "온-프레미스 사용자에 대 한 Office 앱 콘텐츠 추가" 확인란이 추가 됨](media/599e751e-17bd-408d-a18c-127538de6e85.png)
  
- <span data-ttu-id="c8673-145">온-프레미스 사용자는 검색할 사용자 사서함을 선택 하는 데 사용 하는 콘텐츠 위치 선택에 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c8673-145">On-premises users are displayed in the content locations picker that you use to select user mailboxes to search.</span></span> 
    

  
## <a name="searching-for-teams-chat-content-in-cloud-based-mailboxes-for-on-premises-users"></a><span data-ttu-id="c8673-146">온-프레미스 사용자에 대 한 클라우드 기반 사서함의 팀 채팅 콘텐츠 검색</span><span class="sxs-lookup"><span data-stu-id="c8673-146">Searching for Teams chat content in cloud-based mailboxes for on-premises users</span></span>

<span data-ttu-id="c8673-147">기능을 사용 하도록 설정한 후에는 Security & 준수 센터에서 콘텐츠 검색을 사용 하 여 온-프레미스 사용자의 클라우드 기반 사서함에서 팀 채팅 데이터를 검색할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c8673-147">After the feature has been enabled, you can use Content Search in the Security & Compliance Center to search for Teams chat data in the cloud-based mailboxes for on-premises users.</span></span> 
  
1. <span data-ttu-id="c8673-148">보안 & 준수 센터에서 **검색** \> **콘텐츠 검색** 으로 이동</span><span class="sxs-lookup"><span data-stu-id="c8673-148">In the Security & Compliance Center, go to **Search** \> **Content search**</span></span>
    
2. <span data-ttu-id="c8673-149">**검색** 페이지에서 ![](media/8ee52980-254b-440b-99a2-18d068de62d3.gif) **새 검색**아이콘 추가를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="c8673-149">On the **Search** page, click ![Add icon](media/8ee52980-254b-440b-99a2-18d068de62d3.gif) **New search**.</span></span>
    
    <span data-ttu-id="c8673-150">앞에서 설명한 것 처럼, 온 **-프레미스 사용자에 대 한 Office 앱 콘텐츠 추가** 확인란은 **위치**아래에 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c8673-150">As previously explained, the **Add Office app content for on-premises users** checkbox is displayed under **Locations**.</span></span> <span data-ttu-id="c8673-151">기본적으로 선택 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c8673-151">Note that it is selected by default.</span></span>
    
3. <span data-ttu-id="c8673-152">키워드 쿼리를 만들고 필요한 경우 검색 쿼리에 조건을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="c8673-152">Create the keyword query and add conditions to the search query if necessary.</span></span> <span data-ttu-id="c8673-153">팀 채팅 데이터만 검색 하려면 **키워드** 상자에 다음 쿼리를 추가 하면 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c8673-153">To only search for Team chats data, you can add the following query in the **Keywords** box:</span></span> 
    
    ```
    kind:im
    ``` 

4. <span data-ttu-id="c8673-154">이때 **위치**에서 다음 옵션 중 하나를 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c8673-154">At this point, you can choose one of the following options under **Locations**:</span></span>
    
    - <span data-ttu-id="c8673-155">**모든 위치** -조직의 모든 사용자에 대 한 사서함을 검색 하려면이 옵션을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="c8673-155">**All locations** - Select this option to search the mailboxes of all users in your organization.</span></span> <span data-ttu-id="c8673-156">이 확인란을 선택 하면 온-프레미스 사용자에 대 한 모든 클라우드 기반 사서함도 검색 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c8673-156">When the checkbox is selected, all cloud-based mailboxes for on-premises users will also be searched.</span></span> 
    
    - <span data-ttu-id="c8673-157">**특정 위치** -이 옵션을 선택 하 고 **수정** \> 을 클릭 하 여 특정 사서함을 검색할 사용자, 그룹 또는 팀을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="c8673-157">**Specific locations** - Select this option and then click **Modify** \> Choose user, groups, or teams to search specific mailboxes.</span></span> <span data-ttu-id="c8673-158">앞에서 설명한 것 처럼 위치 선택기를 통해 온-프레미스 사용자를 검색할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c8673-158">As previously explained, the locations picker will let you search for on-premises users.</span></span> 
    
5. <span data-ttu-id="c8673-159">검색을 저장 하 고 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="c8673-159">Save and run the search.</span></span> <span data-ttu-id="c8673-160">온-프레미스 사용자에 대 한 클라우드 기반 사서함의 모든 검색 결과를 다른 검색 결과와 같이 미리 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c8673-160">Any search results from the cloud-based mailboxes for on-premises users can be previewed like any other search results.</span></span> <span data-ttu-id="c8673-161">또한 팀 채팅 데이터를 포함 하 여 검색 결과를 PST 파일로 내보낼 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c8673-161">Additionally, you can you can export the search results (including any Teams chat data) to a PST file.</span></span> <span data-ttu-id="c8673-162">자세한 내용은 다음을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="c8673-162">For more information, see:</span></span> 
    
    - [<span data-ttu-id="c8673-163">새 검색 만들기</span><span class="sxs-lookup"><span data-stu-id="c8673-163">Create a new search</span></span>](content-search.md#create-a-new-search)
    
    - [<span data-ttu-id="c8673-164">검색 결과 미리 보기</span><span class="sxs-lookup"><span data-stu-id="c8673-164">Preview search results</span></span>](content-search.md#preview-search-results)
    
    - [<span data-ttu-id="c8673-165">콘텐츠 검색 결과 내보내기</span><span class="sxs-lookup"><span data-stu-id="c8673-165">Export Content Search results</span></span>](export-search-results.md)
    
## <a name="using-powershell-to-search-for-teams-chat-data-in-cloud-based-mailboxes-for-on-premises-users"></a><span data-ttu-id="c8673-166">PowerShell을 사용 하 여 온-프레미스 사용자의 클라우드 기반 사서함에서 팀 채팅 데이터 검색</span><span class="sxs-lookup"><span data-stu-id="c8673-166">Using PowerShell to search for Teams chat data in cloud-based mailboxes for on-premises users</span></span>

<span data-ttu-id="c8673-167">Security & 준수 센터 PowerShell에서 **ComplianceSearch** 및 **ComplianceSearch** cmdlet을 사용 하 여 온-프레미스 사용자의 클라우드 기반 사서함을 검색할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c8673-167">You can use the **New-ComplianceSearch** and **Set-ComplianceSearch** cmdlets in the Security & Compliance Center PowerShell to search the cloud-based mailbox for on-premises users.</span></span> <span data-ttu-id="c8673-168">앞에서 설명한 것 처럼 PowerShell을 사용 하 여 온-프레미스 사용자의 팀 채팅 데이터를 검색 하기 위해 지원 요청을 제출할 필요가 없습니다.</span><span class="sxs-lookup"><span data-stu-id="c8673-168">As previously explained, you don't have to submit a support request to use PowerShell to search for Teams chat data for on-premises users.</span></span> 
  
1. <span data-ttu-id="c8673-169">[Security & 준수 센터 PowerShell에 연결](https://docs.microsoft.com/powershell/exchange/office-365-scc/connect-to-scc-powershell/connect-to-scc-powershell)합니다.</span><span class="sxs-lookup"><span data-stu-id="c8673-169">[Connect to Security & Compliance Center PowerShell](https://docs.microsoft.com/powershell/exchange/office-365-scc/connect-to-scc-powershell/connect-to-scc-powershell).</span></span>
    
2. <span data-ttu-id="c8673-170">새 콘텐츠를 만들려면 다음 PowerShell 명령을 실행 하 여 온-프레미스 사용자의 클라우드 기반 사서함을 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="c8673-170">Run the following PowerShell command to create a new content searches the cloud-based mailboxes of on-premises users.</span></span>
    
    ```
    New-ComplianceSearch <name of new search> -ContentMatchQuery <search query> -ExchangeLocation <on-premises user> -IncludeUserAppContent $true -AllowNotFoundExchangeLocationsEnabled $true  
    ```
   
    <span data-ttu-id="c8673-171">*includeuserappcontent* 매개 변수는 *ExchangeLocation* 매개 변수에 지정 된 사용자 또는 사용자에 대 한 클라우드 기반 사서함을 지정 하는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c8673-171">The  *IncludeUserAppContent*  parameter is used to specify the cloud-based mailbox for the user or users who are specified by the  *ExchangeLocation*  parameter.</span></span> <span data-ttu-id="c8673-172">*AllowNotFoundExchangeLocationsEnabled* 에서는 온-프레미스 사용자에 대해 클라우드 기반 사서함을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c8673-172">The  *AllowNotFoundExchangeLocationsEnabled*  allows cloud-based mailboxes for on-premises users.</span></span> <span data-ttu-id="c8673-173">이 매개 변수의 `$true` 값을 사용 하는 경우 검색을 실행 하기 전에 사서함의 존재 여부를 확인 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c8673-173">When you use the `$true` value for this parameter, the search doesn't try to validate the existence of the mailbox before it runs.</span></span> <span data-ttu-id="c8673-174">이는 사서함 유형이 일반 사서함으로 확인 되지 않으므로 온-프레미스 사용자의 클라우드 기반 사서함을 검색 하는 데 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="c8673-174">This is required to search the cloud-based mailboxes for on-premises users because these types of mailboxes don't resolve as regular mailboxes.</span></span> 
    
    <span data-ttu-id="c8673-175">다음은 Contoso 조직의 온-프레미스 사용자 인 Sara Davis의 클라우드 기반 사서함에 "redstone" 키워드를 포함 하는 팀 대화방 (인스턴트 메시지)을 검색 하는 예제입니다.</span><span class="sxs-lookup"><span data-stu-id="c8673-175">The following example searches for Teams chats (which are instant messages) that contain keyword "redstone" in the cloud-based mailbox of Sara Davis, who is an on-premises user in the Contoso organization.</span></span>
  
    ```
    New-ComplianceSearch "Redstone_Search" -ContentMatchQuery "redstone AND kind:im" -ExchangeLocation sarad@contoso.com -IncludeUserAppContent $true -AllowNotFoundExchangeLocationsEnabled $true  
    ```

   <span data-ttu-id="c8673-176">새 검색을 만든 후에는 **ComplianceSearch** cmdlet을 사용 하 여 검색을 실행 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c8673-176">After you create a new search, be sure to use the **Start-ComplianceSearch** cmdlet to run the search.</span></span> 
  
<span data-ttu-id="c8673-177">이러한 cmdlet을 사용 하는 방법에 대 한 자세한 내용은 다음을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="c8673-177">For more information using these cmdlets, see:</span></span>
  
- [<span data-ttu-id="c8673-178">New-ComplianceSearch</span><span class="sxs-lookup"><span data-stu-id="c8673-178">New-ComplianceSearch</span></span>](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-content-search/new-compliancesearch)
    
- [<span data-ttu-id="c8673-179">Set-ComplianceSearch</span><span class="sxs-lookup"><span data-stu-id="c8673-179">Set-ComplianceSearch</span></span>](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-content-search/set-compliancesearch)
    
- [<span data-ttu-id="c8673-180">Start-ComplianceSearch</span><span class="sxs-lookup"><span data-stu-id="c8673-180">Start-ComplianceSearch</span></span>](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-content-search/start-compliancesearch)
    

## <a name="known-issues"></a><span data-ttu-id="c8673-181">알려진 문제</span><span class="sxs-lookup"><span data-stu-id="c8673-181">Known issues</span></span>

- <span data-ttu-id="c8673-182">현재 온-프레미스 사용자의 경우 클라우드 기반 사서함에서 콘텐츠를 검색, 미리 보기 및 내보낼 수만 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c8673-182">Currently, you can only search, preview, and export content in cloud-based mailboxes for on-premises users.</span></span> <span data-ttu-id="c8673-183">온-프레미스 사용자에 대해 클라우드 기반 사서함을 eDiscovery 사례와 관련 된 보류에 배치 하거나 Office 365 보존 정책에 할당 하는 것은 지원 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c8673-183">Placing a cloud-based mailbox for an on-premises user on a hold associated with an eDiscovery case or assigning it to an Office 365 retention policy is not supported.</span></span> 
    
- <span data-ttu-id="c8673-184">eDiscovery 보류에 대 한 콘텐츠 위치 선택에서는 온-프레미스 사용자를 표시 하 고이를 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c8673-184">The content location picker for eDiscovery holds displays on-premises users and will let you select them.</span></span> <span data-ttu-id="c8673-185">하지만 앞에서 설명한 보류가 온-프레미스 사용자에 게 적용 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c8673-185">However, as previously explained the hold will not be applied to the on-premises user.</span></span>
    
## <a name="frequently-asked-questions"></a><span data-ttu-id="c8673-186">자주하는 질문</span><span class="sxs-lookup"><span data-stu-id="c8673-186">Frequently asked questions</span></span>

 <span data-ttu-id="c8673-187">**온-프레미스 사용자에 대 한 클라우드 기반 사서함은 어디에 있나요?**</span><span class="sxs-lookup"><span data-stu-id="c8673-187">**Where are cloud-based mailboxes for on-premises users located?**</span></span>
  
<span data-ttu-id="c8673-188">클라우드 기반 사서함은 Office 365 조직과 동일한 데이터 센터에 만들어지고 저장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c8673-188">Cloud-based mailboxes are created and stored in the same datacenter as your Office 365 organization.</span></span> 
  
 <span data-ttu-id="c8673-189">**지원 요청을 제출 하는 것 외에 다른 요구 사항이 있습니까?**</span><span class="sxs-lookup"><span data-stu-id="c8673-189">**Are there any other requirements other than submitting a support request?**</span></span>
  
 <span data-ttu-id="c8673-190">앞에서 설명한 것 처럼, 프레미스 사서함을 사용 하는 사용자의 id는 Office 365에서 각 온-프레미스 사용자 계정에 대해 해당 메일 사용자 계정을 만들 수 있도록 클라우드 기반 조직과 동기화 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c8673-190">As previously explained, the identities of users with on-prem mailboxes must be synchronized to your cloud-based organization so that a corresponding mail user account is created for each on-premises user account in Office 365.</span></span> <span data-ttu-id="c8673-191">또한 조직에 office 365 enterprise E1, E3 또는 E5 구독과 같은 office 365 enterprise 구독이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c8673-191">Additionally, your organization must have an Office 365 enterprise subscription, such as an Office 365 Enterprise E1, E3, or E5 subscription.</span></span> 
  
 <span data-ttu-id="c8673-192">**사용자의 온-프레미스 사서함이 클라우드로 마이그레이션될 경우 팀 채팅 데이터가 손실 될 위험이 있습니까?**</span><span class="sxs-lookup"><span data-stu-id="c8673-192">**Is there a risk of losing the Teams chat data if the user's on-premises mailbox is migrated to the cloud?**</span></span>
  
<span data-ttu-id="c8673-193">아니요.</span><span class="sxs-lookup"><span data-stu-id="c8673-193">No.</span></span> <span data-ttu-id="c8673-194">온-프레미스 사용자의 기본 사서함을 클라우드로 마이그레이션하는 경우 해당 사용자에 대 한 팀 채팅 데이터가 새로운 클라우드 기반 기본 사서함으로 마이그레이션됩니다.</span><span class="sxs-lookup"><span data-stu-id="c8673-194">When you migrate the primary mailbox of an on-premises user to the cloud, the Teams chat data for that user will be migrated to their new cloud-based primary mailbox.</span></span>
  
 <span data-ttu-id="c8673-195">**온-프레미스 사용자에 게 eDiscovery 보류 또는 Office 365 보존 정책을 적용할 수 있나요?**</span><span class="sxs-lookup"><span data-stu-id="c8673-195">**Can I apply an eDiscovery hold or Office 365 retention policies to on-premises users?**</span></span>
  
<span data-ttu-id="c8673-196">아니요.</span><span class="sxs-lookup"><span data-stu-id="c8673-196">No.</span></span>
  
 <span data-ttu-id="c8673-197">**조직에서이 기능을 사용 하도록 요청을 제출한 시간 이전에 온-프레미스 사용자의 이전 팀 대화방을 찾을 수 있습니까?**</span><span class="sxs-lookup"><span data-stu-id="c8673-197">**Can Content Search find older Teams chats for on-premises users before the time my organization submitted the request to enable this feature?**</span></span>
  
<span data-ttu-id="c8673-198">Microsoft가 2018 년 1 월 31 일에 온-프레미스 사용자에 대 한 팀 채팅 데이터 저장을 시작 했습니다.</span><span class="sxs-lookup"><span data-stu-id="c8673-198">Microsoft started storing the Teams chat data for on-premises users on January 31, 2018.</span></span> <span data-ttu-id="c8673-199">따라서이 날짜 이후에 active directory 및 Azure active directory 간에 온-프레미스 팀 사용자의 id가 동기화 된 경우 팀 채팅 데이터가 클라우드 기반 사서함에 저장 되 고 콘텐츠 검색을 통해 검색 가능 하 게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c8673-199">So, if the identity of an on-premises Teams user has been synched between Active Directory and Azure Active Directory since this date, then their Teams chat data will be stored in a cloud-based mailbox and will be searchable using Content Search.</span></span> <span data-ttu-id="c8673-200">또한 Microsoft는 온-프레미스 사용자의 클라우드 기반 사서함에서 2018 년 1 월 31 일 이전에 팀 채팅 데이터를 저장 하는 작업을 수행 하 고 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c8673-200">Microsoft is also working on storing Teams chat data from prior to January 31, 2018 in the cloud-based mailboxes for on-premises users.</span></span> <span data-ttu-id="c8673-201">이에 대 한 자세한 내용은 곧 제공 될 예정입니다.</span><span class="sxs-lookup"><span data-stu-id="c8673-201">More information about this will be available soon.</span></span>
