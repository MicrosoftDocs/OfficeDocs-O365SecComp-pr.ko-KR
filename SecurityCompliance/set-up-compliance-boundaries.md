---
title: Office 365에서 eDiscovery 조사에 대한 준수 경계 설정
ms.author: markjjo
author: markjjo
manager: laurawi
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- Strat_O365_IP
- M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: 1b45c82f-26c8-44fb-9f3b-b45436fe2271
description: 준수 경계를 사용 하 여 eDiscovery 관리자가 검색할 수 있는 사용자 콘텐츠 위치를 제어 하는 Office 365 조직 내에 논리적 경계를 만듭니다. 준수 경계는 검색 권한 필터링 (규정 준수 보안 필터 라고도 함)을 사용 하 여 특정 사용자가 검색할 수 있는 사서함, SharePoint 사이트 및 OneDrive 계정을 제어 합니다.
ms.openlocfilehash: ab9fae4dcae04bc79c94f5a5138dfd56cc551414
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/17/2019
ms.locfileid: "34156580"
---
# <a name="set-up-compliance-boundaries-for-ediscovery-investigations-in-office-365"></a><span data-ttu-id="c9dd9-104">Office 365에서 eDiscovery 조사에 대한 준수 경계 설정</span><span class="sxs-lookup"><span data-stu-id="c9dd9-104">Set up compliance boundaries for eDiscovery investigations in Office 365</span></span>

<span data-ttu-id="c9dd9-105">준수 경계는 eDiscovery 관리자가 검색할 수 있는 사용자 콘텐츠 위치 (예: 사서함, SharePoint 사이트, OneDrive 계정)를 제어 하는 Office 365 조직 내에 논리적 경계를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c9dd9-105">Compliance boundaries create logical boundaries within an Office 365 organization that control the user content locations (such as mailboxes, SharePoint sites, and OneDrive accounts) that eDiscovery managers can search.</span></span> <span data-ttu-id="c9dd9-106">또한 규정 준수 경계는 법률, 인적 자원 또는 조직 내 다른 조사를 관리 하는 데 사용 되는 eDiscovery 사례에 액세스할 수 있는 사용자를 제어 합니다.</span><span class="sxs-lookup"><span data-stu-id="c9dd9-106">Additionally, compliance boundaries control who can access eDiscovery cases used to manage the legal, human resources, or other investigations within your organization.</span></span> <span data-ttu-id="c9dd9-107">지리적 boarders 및 규정을 준수 해야 하는 국내 기업에는 종종 다양 한 기관으로 분류 되는 정부에 대 한 적합성 경계가 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="c9dd9-107">The need for compliance boundaries is often necessary for multi-nations corporations that have to respect geographical boarders and regulations, and for governments, which are often divided into different agencies.</span></span> <span data-ttu-id="c9dd9-108">Office 365에서 준수 경계는 콘텐츠 검색을 수행 하 고 eDiscovery 사례를 통해 조사를 관리할 때 이러한 요구 사항을 충족 하는 데 도움이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c9dd9-108">In Office 365, compliance boundaries help you meet these requirements when performing content searches and managing investigations with eDiscovery cases.</span></span>
  
<span data-ttu-id="c9dd9-109">다음 그림의 예를 사용 하 여 준수 경계의 작동 방식을 알아봅니다.</span><span class="sxs-lookup"><span data-stu-id="c9dd9-109">We'll use the example in the following illustration to explain how compliance boundaries work.</span></span>
  
![준수 경계는 eDisocovery 사례에 대 한 액세스를 제어 하는 기관 및 관리 역할 그룹에 대 한 액세스를 제어 하는 검색 권한 필터로 구성 됩니다.](media/5c206cc8-a6eb-4d6b-a3a5-21e158791f9a.png)
  
<span data-ttu-id="c9dd9-111">이 예에서 Contoso b 2는 두 개의 자회사, 커피 및 Coho Winery으로 구성 되는 Office 365 조직입니다.</span><span class="sxs-lookup"><span data-stu-id="c9dd9-111">In this example, Contoso LTD is an Office 365 organization that consists of two subsidiaries, Fourth Coffee and Coho Winery.</span></span> <span data-ttu-id="c9dd9-112">비즈니스에서는 eDiscovery mangers 및 investigators가 해당 에이전시에서 Exchange 사서함, OneDrive 계정 및 SharePoint 사이트만 검색할 수 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c9dd9-112">The business requires that eDiscovery mangers and investigators can only search the Exchange mailboxes, OneDrive accounts, and SharePoint sites in their agency.</span></span> <span data-ttu-id="c9dd9-113">또한 eDiscovery 관리자 및 investigators는 자신의 에이전시에 있는 eDiscovery 사례만 볼 수 있을 뿐 이며 구성원 인 경우에만 액세스할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c9dd9-113">Additionally, eDiscovery managers and investigators can only see eDiscovery cases in the in their agency, and they can only access the cases that they're a member of.</span></span> <span data-ttu-id="c9dd9-114">준수 경계가 이러한 요구 사항을 충족 하는 방식은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="c9dd9-114">Here's how compliance boundaries meet these requirements.</span></span>
  
- <span data-ttu-id="c9dd9-115">콘텐츠 검색의 검색 권한 필터링 기능은 eDiscovery 관리자 및 investigators에서 검색할 수 있는 콘텐츠 위치를 제어 합니다.</span><span class="sxs-lookup"><span data-stu-id="c9dd9-115">The search permissions filtering functionality in Content Search controls the content locations that eDiscovery managers and investigators can search.</span></span> <span data-ttu-id="c9dd9-116">즉, eDiscovery 관리자 및 네 번째 커피 기관에 있는 investigators는 네 번째 커피 자회사의 콘텐츠 위치만 검색할 수 있음을 의미 합니다.</span><span class="sxs-lookup"><span data-stu-id="c9dd9-116">This means eDiscovery managers and investigators in the Fourth Coffee agency can only search content locations in the Fourth Coffee subsidiary.</span></span> <span data-ttu-id="c9dd9-117">Coho Winery 자회사에도 동일한 제한이 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c9dd9-117">The same restriction applies to the Coho Winery subsidiary.</span></span>
    
    <span data-ttu-id="c9dd9-118">역할 그룹은 보안 & 준수 센터에서 eDiscovery 사례를 볼 수 있는 사용자를 제어 합니다.</span><span class="sxs-lookup"><span data-stu-id="c9dd9-118">Role groups control who can see the eDiscovery cases in the Security & Compliance Center.</span></span> <span data-ttu-id="c9dd9-119">즉, eDiscovery 관리자 및 investigators는 해당 에이전시에서 eDiscovery 사례만 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c9dd9-119">This means that eDiscovery managers and investigators can only see the eDiscovery cases in their agency.</span></span>
    
- <span data-ttu-id="c9dd9-120">또한 역할 그룹은 구성원을 eDiscovery 사례에 할당할 수 있는 사용자를 제어 합니다.</span><span class="sxs-lookup"><span data-stu-id="c9dd9-120">Role groups also control who can assign members to an eDiscovery case.</span></span> <span data-ttu-id="c9dd9-121">즉, eDiscovery 관리자 및 investigators는 자신이 자신을 구성원 인 사례에만 구성원을 할당할 수 있음을 의미 합니다.</span><span class="sxs-lookup"><span data-stu-id="c9dd9-121">This means eDiscovery managers and investigators can only assign members to cases that they themselves are a member of.</span></span>
    
<span data-ttu-id="c9dd9-122">준수 경계를 설정 하는 프로세스는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="c9dd9-122">Here's the process for setting up compliance boundaries:</span></span>
  
[<span data-ttu-id="c9dd9-123">1 단계: 사용자 특성을 식별 하 여 에이전시를 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="c9dd9-123">Step 1: Identify a user attribute to define your agencies</span></span>](#step-1-identify-a-user-attribute-to-define-your-agencies)

[<span data-ttu-id="c9dd9-124">2 단계: Microsoft Support가 사용자 특성을 OneDrive 계정에 동기화 하는 요청을 파일에 포함</span><span class="sxs-lookup"><span data-stu-id="c9dd9-124">Step 2: File a request with Microsoft Support to synchronize the user attribute to OneDrive accounts</span></span>](#step-2-file-a-request-with-microsoft-support-to-synchronize-the-user-attribute-to-onedrive-accounts)

[<span data-ttu-id="c9dd9-125">3 단계: 각 에이전시에 대 한 역할 그룹 만들기</span><span class="sxs-lookup"><span data-stu-id="c9dd9-125">Step 3: Create a role group for each agency</span></span>](#step-3-create-a-role-group-for-each-agency)

[<span data-ttu-id="c9dd9-126">4 단계: 검색 권한 필터를 만들어 준수 경계를 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="c9dd9-126">Step 4: Create a search permissions filter to enforce the compliance boundary</span></span>](#step-4-create-a-search-permissions-filter-to-enforce-the-compliance-boundary)

[<span data-ttu-id="c9dd9-127">5 단계: 에이전시 내 조사에 대 한 eDiscovery 사례 만들기</span><span class="sxs-lookup"><span data-stu-id="c9dd9-127">Step 5: Create an eDiscovery case for an intra-agency investigations</span></span>](#step-5-create-an-ediscovery-case-for-an-intra-agency-investigations)
  
## <a name="step-1-identify-a-user-attribute-to-define-your-agencies"></a><span data-ttu-id="c9dd9-128">1 단계: 사용자 특성을 식별 하 여 에이전시를 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="c9dd9-128">Step 1: Identify a user attribute to define your agencies</span></span>

<span data-ttu-id="c9dd9-129">첫 번째 단계는 기관을 정의 하는 데 사용할 Azure Active Directory 특성을 선택 하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="c9dd9-129">The first step is to choose an Azure Active Directory attribute to use that will define your agencies.</span></span> <span data-ttu-id="c9dd9-130">이 특성은 eDiscovery 관리자가이 특성에 대 한 특정 값이 할당 된 사용자의 콘텐츠 위치만 검색 하도록 제한 하는 검색 권한 필터를 만드는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c9dd9-130">This attribute will be used to create the search permissions filter that limits an eDiscovery manager to search only the content locations of users who are assigned a specific value for this attribute.</span></span> <span data-ttu-id="c9dd9-131">예를 들어 Contoso에서 **부서** 특성을 사용 하기로 결정 한다고 가정해 보겠습니다.</span><span class="sxs-lookup"><span data-stu-id="c9dd9-131">For example, let's say Contoso decides to use the **Department** attribute.</span></span> <span data-ttu-id="c9dd9-132">Coho Winery 자회사의 사용자에 대 한이 특성의 값은 다음과 `FourthCoffee` 같습니다 `CohoWinery`.</span><span class="sxs-lookup"><span data-stu-id="c9dd9-132">The value for this attribute for users in the Fourth Coffee subsidiary would be  `FourthCoffee`  and the value for users in Coho Winery subsidiary would be `CohoWinery`.</span></span> <span data-ttu-id="c9dd9-133">4 단계에서는이 `attribute:value` 쌍 (예 *: FourthCoffee* )을 사용 하 여 eDiscovery 관리자가 검색할 수 있는 사용자 콘텐츠 위치를 제한 합니다.</span><span class="sxs-lookup"><span data-stu-id="c9dd9-133">In Step 4, you'll use this  `attribute:value`  pair (for example,  *Department:FourthCoffee*  ) to limit the user content locations that eDiscovery managers can search.</span></span> 
  
<span data-ttu-id="c9dd9-134">다음은 준수 경계에 사용할 수 있는 Azure Active Directory 사용자 특성 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="c9dd9-134">Here's a list of Azure Active Directory user attributes that you can use for compliance boundaries:</span></span>
  
- <span data-ttu-id="c9dd9-135">Company</span><span class="sxs-lookup"><span data-stu-id="c9dd9-135">Company</span></span>
    
- <span data-ttu-id="c9dd9-136">CustomAttribute1-CustomAttribute15</span><span class="sxs-lookup"><span data-stu-id="c9dd9-136">CustomAttribute1 - CustomAttribute15</span></span>
    
- <span data-ttu-id="c9dd9-137">부서</span><span class="sxs-lookup"><span data-stu-id="c9dd9-137">Department</span></span>
    
- <span data-ttu-id="c9dd9-138">사무실</span><span class="sxs-lookup"><span data-stu-id="c9dd9-138">Office</span></span>

- <span data-ttu-id="c9dd9-139">C (두 문자 국가 코드)</span><span class="sxs-lookup"><span data-stu-id="c9dd9-139">C (Two letter Country Code)</span></span>
    
<span data-ttu-id="c9dd9-140">더 많은 사용자 특성을 사용할 수 있지만 (특히 Exchange 사서함의 경우) 위에 나열 된 특성도 현재 OneDrive에서 지원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c9dd9-140">Although more user attributes are available, particularly for Exchange mailboxes, the attributes listed above are the only ones currently supported by OneDrive.</span></span>
  
## <a name="step-2-file-a-request-with-microsoft-support-to-synchronize-the-user-attribute-to-onedrive-accounts"></a><span data-ttu-id="c9dd9-141">2 단계: Microsoft Support가 사용자 특성을 OneDrive 계정에 동기화 하는 요청을 파일에 포함</span><span class="sxs-lookup"><span data-stu-id="c9dd9-141">Step 2: File a request with Microsoft Support to synchronize the user attribute to OneDrive accounts</span></span>

<span data-ttu-id="c9dd9-142">다음 단계에서는 1 단계에서 선택한 Azure Active Directory 특성을 조직의 모든 OneDrive 계정으로 동기화 하는 Microsoft 지원 서비스에 파일을 요청 합니다.</span><span class="sxs-lookup"><span data-stu-id="c9dd9-142">The next step is to file a request with Microsoft Support to synchronize the Azure Active Directory attribute that you chose in Step 1 to all OneDrive accounts in your organization.</span></span> <span data-ttu-id="c9dd9-143">이 동기화가 수행 되 면 1 단계에서 선택한 특성 및 값이 SharePoint의 숨겨진 관리 속성에 매핑됩니다 `ComplianceAttribute`.</span><span class="sxs-lookup"><span data-stu-id="c9dd9-143">After this synchronization occurs, the attribute (and its value) that you chose in Step 1 will be mapped to a hidden managed property in SharePoint named  `ComplianceAttribute`.</span></span> <span data-ttu-id="c9dd9-144">이 특성을 사용 하 여 4 단계에서 OneDrive에 대 한 검색 권한 필터를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c9dd9-144">You'll use this attribute to create the search permissions filter for OneDrive in Step 4.</span></span>
  
<span data-ttu-id="c9dd9-145">Microsoft 지원 서비스에 요청을 제출할 때 다음 정보를 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="c9dd9-145">Include the following information when you submit the request to Microsoft support:</span></span>
  
- <span data-ttu-id="c9dd9-146">Office 365 조직의 기본 도메인 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c9dd9-146">The default domain name of your Office 365 organization</span></span>
    
- <span data-ttu-id="c9dd9-147">Azure Active Directory 특성의 이름 (1 단계)</span><span class="sxs-lookup"><span data-stu-id="c9dd9-147">The name of the Azure Active Directory attribute (from Step 1)</span></span>
    
- <span data-ttu-id="c9dd9-148">다음은 지원 요청의 목적에 대 한 설명입니다. "비즈니스용 OneDrive에서 준수 보안 필터에 대 한 Azure Active Directory를 사용 하도록 설정 합니다."</span><span class="sxs-lookup"><span data-stu-id="c9dd9-148">The following title or description of the purpose of the support request: "Enable OneDrive for Business Synchronization with Azure Active Directory for Compliance Security Filters".</span></span> <span data-ttu-id="c9dd9-149">이를 통해 요청을 구현할 Office 365 eDiscovery 엔지니어링 팀에 게 요청을 라우팅할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c9dd9-149">This will help route the request to the Office 365 eDiscovery engineering team who will implement the request.</span></span>
    
<span data-ttu-id="c9dd9-150">엔지니어링이 변경 되 고 특성이 OneDrive에 동기화 되 면 Microsoft Support에서 변경 된 빌드 번호와 예상 배포 날짜가 전송 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c9dd9-150">After the engineering change is made and the attribute is synchronized to OneDrive, Microsoft Support will send you the build number that the change was made in and an estimated deployment date.</span></span> <span data-ttu-id="c9dd9-151">배포 프로세스는 일반적으로 지원 요청을 제출한 후 4-6 주 정도 걸립니다.</span><span class="sxs-lookup"><span data-stu-id="c9dd9-151">Note that the deployment process usually takes 4-6 weeks after you submit the support request.</span></span>
  
 <span data-ttu-id="c9dd9-152">**중요:** 변경 내용이 배포 될 때까지 3 단계부터 5 단계까지 완료할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c9dd9-152">**Important:** You can complete Step 3 through Step 5 before the change is deployed.</span></span> <span data-ttu-id="c9dd9-153">하지만 콘텐츠 검색을 실행 해도 변경 내용을 배포할 때까지 검색 권한 필터에 지정 된 OneDrive 사이트의 문서가 반환 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c9dd9-153">But running content searches won't return documents from OneDrive sites specified in the search permissions filter until after the change is deployed.</span></span> 
  
## <a name="step-3-create-a-role-group-for-each-agency"></a><span data-ttu-id="c9dd9-154">3 단계: 각 에이전시에 대 한 역할 그룹 만들기</span><span class="sxs-lookup"><span data-stu-id="c9dd9-154">Step 3: Create a role group for each agency</span></span>

<span data-ttu-id="c9dd9-155">다음 단계는 사용자의 조직과 부합 되는 보안 & 준수 센터에서 역할 그룹을 만드는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="c9dd9-155">The next step is to create the role groups in the Security & Compliance Center that will align with your agencies.</span></span> <span data-ttu-id="c9dd9-156">기본 제공 eDiscovery 관리자 그룹을 복사 하 고, 적절 한 구성원을 추가 하 고, 필요에 따라 적용 되지 않을 수 있는 역할을 제거 하 여 새 역할 그룹을 만드는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="c9dd9-156">We recommend that you create a new role group by copying the built-in eDiscovery Managers group, adding the appropriate members, and removing roles that may not be applicable to your needs.</span></span> <span data-ttu-id="c9dd9-157">EDiscovery 관련 역할에 대 한 자세한 내용은 [Office 365 Security _AMP_ 준수 센터에서 ediscovery 사용 권한 할당](assign-ediscovery-permissions.md)을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="c9dd9-157">For more information about eDiscovery-related roles, see [Assign eDiscovery permissions in the Office‍ 365 Security & Compliance Center](assign-ediscovery-permissions.md).</span></span>
  
<span data-ttu-id="c9dd9-158">역할 그룹을 만들려면 Security & 준수 센터의 **사용 권한** 페이지로 이동한 후 준수 경계 및 eDiscovery 사례를 사용 하 여 조사를 관리할 각 에이전시의 각 팀에 대해 역할 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c9dd9-158">To create the role groups, go to the **Permissions** page in the Security & Compliance Center and create a role group for each team in each agency that will use compliance boundaries and eDiscovery cases to manage investigations.</span></span> 
  
<span data-ttu-id="c9dd9-159">Contoso 준수 경계 시나리오를 사용 하 여 네 개의 역할 그룹을 만들고 해당 구성원을 각각에 추가 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c9dd9-159">Using the Contoso compliance boundaries scenario, four role groups need to be created and the appropriate members added to each one.</span></span>
  
- <span data-ttu-id="c9dd9-160">커피 eDiscovery 관리자 4 대</span><span class="sxs-lookup"><span data-stu-id="c9dd9-160">Fourth Coffee eDiscovery Managers</span></span>
    
- <span data-ttu-id="c9dd9-161">네 번째 커피 Investigators</span><span class="sxs-lookup"><span data-stu-id="c9dd9-161">Fourth Coffee Investigators</span></span>
    
- <span data-ttu-id="c9dd9-162">Coho Winery eDiscovery 관리자</span><span class="sxs-lookup"><span data-stu-id="c9dd9-162">Coho Winery eDiscovery Managers</span></span>
    
- <span data-ttu-id="c9dd9-163">Coho Winery Investigators</span><span class="sxs-lookup"><span data-stu-id="c9dd9-163">Coho Winery Investigators</span></span>
    

  
## <a name="step-4-create-a-search-permissions-filter-to-enforce-the-compliance-boundary"></a><span data-ttu-id="c9dd9-164">4 단계: 검색 권한 필터를 만들어 준수 경계를 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="c9dd9-164">Step 4: Create a search permissions filter to enforce the compliance boundary</span></span>

<span data-ttu-id="c9dd9-165">각 에이전시에 대해 역할 그룹을 만든 후에는 각 역할 그룹을 특정 에이전시에 연결 하는 검색 권한 필터를 만들고 준수 경계 자체를 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="c9dd9-165">After you've created role groups for each agency, the next step is to create the search permissions filters that associate each role group to its specific agency and defines the compliance boundary itself.</span></span> <span data-ttu-id="c9dd9-166">각 에이전시에 대해 하나의 검색 권한 필터를 만들어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c9dd9-166">You need to create one search permissions filter for each agency.</span></span> <span data-ttu-id="c9dd9-167">보안 권한 필터를 만드는 방법에 대 한 자세한 내용은 [콘텐츠 검색에 대 한 사용 권한 필터링 구성을](permissions-filtering-for-content-search.md)참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="c9dd9-167">For more information about creating security permissions filters, see [Configure permissions filtering for Content Search](permissions-filtering-for-content-search.md).</span></span>
  
<span data-ttu-id="c9dd9-168">준수 경계에 사용 되는 검색 권한 필터를 만드는 데 사용 되는 구문은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="c9dd9-168">Here's the syntax that's used to create a search permissions filter used for compliance boundaries.</span></span>

```
New-ComplianceSecurityFilter -FilterName <name of filter> -Users <role groups> -Filters "Mailbox_<Compliance attribute from Step 1>  -eq '<AttributeVale> '", "Site_ComplianceAttribute  -eq <AttributeValue>' -or Site_Path -like <SharePointURL> *'" -Action <Action >
```
  
<span data-ttu-id="c9dd9-169">다음은 명령의 각 매개 변수에 대 한 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="c9dd9-169">Here's a description of each parameter in the command:</span></span>
  
-  <span data-ttu-id="c9dd9-170">`FilterName`-필터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c9dd9-170">`FilterName` - Specifies the name of the filter.</span></span> <span data-ttu-id="c9dd9-171">필터를 사용할 에이전시를 설명 하거나 식별 하는 이름을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="c9dd9-171">Use a name that describes or identifies the agency that filter will be used in.</span></span> 
    
-  <span data-ttu-id="c9dd9-172">`Users`-이 필터가 수행 하는 콘텐츠 검색 작업에이 필터를 적용할 사용자 또는 그룹을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c9dd9-172">`Users` - Specifies the users or groups who get this filter applied to the Content Search actions they perform.</span></span> <span data-ttu-id="c9dd9-173">준수 경계의 경우이 매개 변수는 필터를 만드는 데 사용할 에이전시에서 3 단계에서 만든 역할 그룹을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c9dd9-173">For compliance boundaries, this parameter specifies the role groups (that you created in Step 3) in the agency that you're creating the filter for.</span></span> <span data-ttu-id="c9dd9-174">참고 이것은 다중 값 매개 변수 이므로 쉼표로 구분 하 여 하나 이상의 역할 그룹을 포함할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c9dd9-174">Note this is a multi-value parameter so you can include one or more role groups, separated by commas.</span></span> 
    
-  <span data-ttu-id="c9dd9-175">`Filters`-필터에 대 한 검색 조건을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c9dd9-175">`Filters` - Specifies the search criteria for the filter.</span></span> <span data-ttu-id="c9dd9-176">준수 경계에는 다음 필터를 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="c9dd9-176">For the compliance boundaries, you will define the following filters.</span></span> <span data-ttu-id="c9dd9-177">각 항목은 사용자 콘텐츠 위치에 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c9dd9-177">Each one applies to a user content location.</span></span> 
    
  -  <span data-ttu-id="c9dd9-178">`Mailbox`- `Users` 매개 변수에 정의 된 역할 그룹이 검색할 수 있는 사서함을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c9dd9-178">`Mailbox` - Specifies the mailboxes that the role groups defined in the  `Users` parameter can search.</span></span> <span data-ttu-id="c9dd9-179">준수 경계의 경우 *ComplianceAttribute* 는 1 단계에서 식별 한 특성 및 *AttributeValue* 에서 해당 에이전시를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c9dd9-179">For compliance boundaries,  *ComplianceAttribute*  is the same attribute that you identified in Step 1 and  *AttributeValue*  specifies the agency.</span></span> <span data-ttu-id="c9dd9-180">이 필터는 역할 그룹의 구성원이 특정 에이전시의 사서함만 검색할 수 있도록 허용 합니다. 예를 `"Mailbox_Department -eq 'FourthCoffee'"` 들면입니다.</span><span class="sxs-lookup"><span data-stu-id="c9dd9-180">This filter allow members of the role group to only search the mailboxes in a specific agency; for example,  `"Mailbox_Department -eq 'FourthCoffee'"` .</span></span> 
    
  -  <span data-ttu-id="c9dd9-181">`Site`- `Users` 매개 변수에 정의 된 역할 그룹이 검색할 수 있는 OneDrive 계정을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c9dd9-181">`Site` - Specifies the OneDrive accounts that the role groups defined in the  `Users` parameter can search.</span></span> <span data-ttu-id="c9dd9-182">OneDrive 필터의 경우 실제 문자열 `ComplianceAttribute`을 사용 합니다. 이는 1 단계에서 확인 하 고 2 단계에서 제출한 지원 요청의 결과로 OneDrive 계정과 동기화 된 것과 동일한 특성에 매핑됩니다.  *AttributeValue* 는 에이전시를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c9dd9-182">For the OneDrive filter, use the actual string  `ComplianceAttribute`; this will map to the same attribute that you identified in Step 1 and that's synchronized to OneDrive accounts as a result of the support request that you submitted in Step 2;  *AttributeValue*  specifies the agency.</span></span> <span data-ttu-id="c9dd9-183">이 필터는 역할 그룹의 구성원이 특정 에이전시의 OneDrive 계정만 검색할 수 있도록 허용 합니다. 예를 `"Site_ComplianceAttribute -eq 'FourthCoffee'"`들면입니다.</span><span class="sxs-lookup"><span data-stu-id="c9dd9-183">This filter allow members of the role group to only search the OneDrive accounts in a specific agency; for example,  `"Site_ComplianceAttribute -eq 'FourthCoffee'"`.</span></span>
    
  -  <span data-ttu-id="c9dd9-184">`Site_Path`- `Users` 매개 변수에 정의 된 역할 그룹이 검색할 수 있는 SharePoint 사이트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c9dd9-184">`Site_Path` - Specifies the SharePoint sites that the role groups defined in the  `Users` parameter can search.</span></span> <span data-ttu-id="c9dd9-185">*SharePointURL* 은 역할 그룹의 구성원이 검색할 수 있는 에이전시의 사이트를 지정 합니다. 예를 들어`"Site_Path -like 'https://contoso.sharepoint.com/sites/FourthCoffee*'"`</span><span class="sxs-lookup"><span data-stu-id="c9dd9-185">The  *SharePointURL*  specifies the sites in the agency that members of the role group can search; for example,  `"Site_Path -like 'https://contoso.sharepoint.com/sites/FourthCoffee*'"`</span></span>
    
-  <span data-ttu-id="c9dd9-186">`Action`-필터가 적용 되는 준수 검색 작업의 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c9dd9-186">`Action` - Specifies the type of Compliance Search action that the filter is applied to.</span></span> <span data-ttu-id="c9dd9-187">예를 `-Action Search` 들어 `Users` 매개 변수에 정의 된 역할 그룹의 구성원이 콘텐츠 검색을 실행 하는 경우에만 필터를 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="c9dd9-187">For example,  `-Action Search` would only apply the filter when members of the role groups defined in the  `Users` parameter runs a content search.</span></span> <span data-ttu-id="c9dd9-188">이 경우 검색 결과를 내보낼 때 필터가 적용 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c9dd9-188">In this case, the filter wouldn't be applied when exporting search results.</span></span> <span data-ttu-id="c9dd9-189">준수 경계의 경우 필터를 `-Action All` 모든 검색 작업에 적용 하도록 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="c9dd9-189">For compliance boundaries, use  `-Action All` so the filter applies to all search actions.</span></span> 
    
    <span data-ttu-id="c9dd9-190">콘텐츠 검색 작업 목록은 [콘텐츠 검색에 대 한 권한 필터링 구성](permissions-filtering-for-content-search.md#new-compliancesecurityfilter)의 "new-compliancesecurityfilter" 섹션을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="c9dd9-190">For a list of the Content Search actions, see the "New-ComplianceSecurityFilter" section in [Configure permissions filtering for Content Search](permissions-filtering-for-content-search.md#new-compliancesecurityfilter).</span></span>
    
<span data-ttu-id="c9dd9-191">다음은 Contoso 준수 경계 시나리오를 지원 하기 위해 만드는 두 가지 검색 권한 필터의 예입니다.</span><span class="sxs-lookup"><span data-stu-id="c9dd9-191">Here are examples of the two search permissions filters that would be created to support the Contoso compliance boundaries scenario.</span></span>
  
 <span data-ttu-id="c9dd9-192">**커피 4**</span><span class="sxs-lookup"><span data-stu-id="c9dd9-192">**Fourth Coffee**</span></span>

```
New-ComplianceSecurityFilter -FilterName "Fourth Coffee Security Filter" -Users "Fourth Coffee eDiscovery Managers", "Fourth Coffee Investigators" -Filters "Mailbox_Department -eq 'FourthCoffee'", "Site_ComplianceAttribute -eq 'FourthCoffee' -or Site_Path -like 'https://contoso.sharepoint.com/sites/FourthCoffee*'" -Action ALL
```
   
 <span data-ttu-id="c9dd9-193">**Coho Winery**</span><span class="sxs-lookup"><span data-stu-id="c9dd9-193">**Coho Winery**</span></span>

```
New-ComplianceSecurityFilter -FilterName "Coho Winery Security Filter" -Users "Coho Winery eDiscovery Managers", "Coho Winery Investigators" -Filters "Mailbox_Department -eq 'CohoWinery'", "Site_ComplianceAttribute -eq 'CohoWinery' -or Site_Path -like 'https://contoso.sharepoint.com/sites/CohoWinery*'" -Action ALL
```

## <a name="step-5-create-an-ediscovery-case-for-an-intra-agency-investigations"></a><span data-ttu-id="c9dd9-194">5 단계: 에이전시 내 조사에 대 한 eDiscovery 사례 만들기</span><span class="sxs-lookup"><span data-stu-id="c9dd9-194">Step 5: Create an eDiscovery case for an intra-agency investigations</span></span>

<span data-ttu-id="c9dd9-195">마지막 단계는 Security & 준수 센터에서 새 eDiscovery 사례를 만든 다음 3 단계에서 만든 역할 그룹을 사례 구성원으로 추가 하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="c9dd9-195">The final step is to create a new eDiscovery case in the Security & Compliance Center and then add the role group—that you created in Step 3—as a member of the case.</span></span> <span data-ttu-id="c9dd9-196">이로 인해 준수 경계를 사용 하는 경우의 두 가지 중요 한 특징이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c9dd9-196">This results in two important characteristics of using compliance boundaries:</span></span>
  
- <span data-ttu-id="c9dd9-197">사례에 추가 된 역할 그룹의 구성원만이 보안 & 준수 센터의 사례를 보고 액세스할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c9dd9-197">Only members of the role group added to the case will be able to see and access the case in the Security & Compliance Center.</span></span> <span data-ttu-id="c9dd9-198">예를 들어, 네 번째 커피 Investigators 역할 그룹이 사례 유일한 구성원 인 경우에는 네 번째 커피 eDiscovery 관리자 역할 그룹의 구성원 또는 다른 역할 그룹의 구성원도 해당 사례를 보거나 액세스할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="c9dd9-198">For example, if the Fourth Coffee Investigators role group is the only member of a case, then members of the Fourth Coffee eDiscovery Managers role group (or members of any other role group) won't be able to see or access the case.</span></span>
    
- <span data-ttu-id="c9dd9-199">사례에 할당 된 역할 그룹의 구성원이 사례와 연결 된 검색을 실행 하는 경우, 해당 사용자는 해당 에이전시 (4 단계에서 만든 검색 권한 필터에 의해 정의 됨) 내의 콘텐츠 위치만 검색할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c9dd9-199">When a member of the role group assigned to a case runs a search associated with the case, they will only be able to search the content locations within their agency (which is defined by the search permissions filter that you created in Step 4.)</span></span>


<span data-ttu-id="c9dd9-200">새 사례를 만들고 구성원을 할당 하려면 다음을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="c9dd9-200">To create a new case and assign members:</span></span>
    
1. <span data-ttu-id="c9dd9-201">Security & 준수 센터의 **eDiscovery** 페이지로 이동 하 여 새 사례를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c9dd9-201">Go to the **eDiscovery** page in the Security & Compliance Center and create a new case.</span></span> 
    
2. <span data-ttu-id="c9dd9-202">EDiscovery 사례 목록에서 방금 만든 사례 이름을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="c9dd9-202">In the list of eDiscovery cases, click the name of the case you just created.</span></span>
    
3. <span data-ttu-id="c9dd9-203">**이 사례** 플라이 아웃 관리 페이지의 **역할 그룹**관리자에서 add 아이콘 ![](media/8ee52980-254b-440b-99a2-18d068de62d3.gif) **추가**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="c9dd9-203">In the **Manage this case** flyout page, under **Mange role groups**, click ![Add icon](media/8ee52980-254b-440b-99a2-18d068de62d3.gif) **Add**.</span></span>
    
    ![EDiscovery 사례의 구성원으로 역할 그룹 추가](media/f8b4b557-01b9-4388-85be-b5b5ab7c5629.png)
  
4. <span data-ttu-id="c9dd9-205">역할 그룹 목록에서 3 단계에서 만든 역할 그룹 중 하나를 선택 하 고 **추가**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="c9dd9-205">In the list of role groups, select one of the role groups that you created in Step 3, and click **Add**.</span></span>
    
5. <span data-ttu-id="c9dd9-206">**이 사례** 플라이 아웃 관리에서 **저장** 을 클릭 하 여 변경 내용을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="c9dd9-206">Click **Save** on the **Manage this case** flyout to save the change.</span></span> 

## <a name="compliance-boundary-limitations"></a><span data-ttu-id="c9dd9-207">준수 경계 제한</span><span class="sxs-lookup"><span data-stu-id="c9dd9-207">Compliance boundary limitations</span></span>

<span data-ttu-id="c9dd9-208">EDiscovery 사례를 관리 하 고 준수 경계를 사용 하는 조사를 관리할 때는 다음과 같은 제한 사항을 염두에 두어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c9dd9-208">Keep the following limitations in mind when managing eDiscovery cases and investigations that use of compliance boundaries.</span></span>
  
- <span data-ttu-id="c9dd9-209">콘텐츠 검색을 만들고 실행 하는 경우에는 에이전시 외부에 있는 콘텐츠 위치를 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c9dd9-209">When creating and running a Content Search, you can select content locations that are outside of your agency.</span></span> <span data-ttu-id="c9dd9-210">그러나 검색 권한 필터 때문에 해당 위치의 콘텐츠가 검색 결과에 포함 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c9dd9-210">However, because of the search permissions filter, content from those locations won't be included in the search results.</span></span>
    
- <span data-ttu-id="c9dd9-211">준수 경계는 eDiscovery 사례의 보류에 적용 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c9dd9-211">Compliance boundaries don't apply to holds in eDiscovery cases.</span></span> <span data-ttu-id="c9dd9-212">즉, 한 에이전시의 eDiscovery 관리자가 사용자를 보류 중인 다른 에이전시에 배치할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c9dd9-212">That means an eDiscovery manager in one agency can place a user in a different agency on hold.</span></span> <span data-ttu-id="c9dd9-213">그러나 eDiscovery 관리자가 보류 되었던 사용자의 콘텐츠 위치를 검색 하는 경우 준수 경계가 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c9dd9-213">However, the compliance boundary will be enforced if the eDiscovery manager searches the content locations of the user who was placed on hold.</span></span> <span data-ttu-id="c9dd9-214">즉, eDiscovery 관리자는 사용자를 보류 상태로 설정할 수 있더라도 사용자의 콘텐츠 위치를 검색할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="c9dd9-214">That means the eDiscovery manager won't be able search the user's content locations, even though they were able to place the user on hold.</span></span>
    
    <span data-ttu-id="c9dd9-215">또한 보유 통계는 에이전시의 콘텐츠 위치에만 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c9dd9-215">Additionally, hold statistics will only apply to content locations in the agency.</span></span>
    
- <span data-ttu-id="c9dd9-216">검색 사용 권한 필터는 Exchange 공용 폴더에 적용 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c9dd9-216">Search permissions filters aren't applied to Exchange public folders.</span></span>

## <a name="searching-and-exporting-content-in-multi-geo-environments"></a><span data-ttu-id="c9dd9-217">다중 지역 환경에서 콘텐츠 검색 및 내보내기</span><span class="sxs-lookup"><span data-stu-id="c9dd9-217">Searching and exporting content in Multi-Geo environments</span></span>

<span data-ttu-id="c9dd9-218">또한 검색 권한 필터를 사용 하 여 [SharePoint 다중 위치 환경](https://go.microsoft.com/fwlink/?linkid=860840)에서 콘텐츠를 검색 하는 데 사용할 수 있는 콘텐츠와 검색 되는 데이터 센터의 위치를 제어할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c9dd9-218">Search permissions filters also let you control where content is routed for export and which datacenter can be searched when searching content locations in a [SharePoint Multi-Geo environment](https://go.microsoft.com/fwlink/?linkid=860840).</span></span>
  
- <span data-ttu-id="c9dd9-219">**검색 결과 내보내기** -Exchange 사서함, SharePoint 사이트 및 OneDrive 계정에서 특정 데이터 센터의 검색 결과를 내보낼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c9dd9-219">**Export search results** - You can export the search results from Exchange mailboxes, SharePoint sites, and OneDrive accounts from a specific datacenter.</span></span> <span data-ttu-id="c9dd9-220">즉, 검색 결과를 내보낼 데이터 센터 위치를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c9dd9-220">This means that you can specify the datacenter location that search results will be exported from.</span></span>

    <span data-ttu-id="c9dd9-221">**New-compliancesecurityfilter** 또는 **New-compliancesecurityfilter** cmdlet에 **Region** 매개 변수를 사용 하 여 내보내기가 라우팅되는 데이터 센터를 만들거나 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="c9dd9-221">Use the **Region** parameter for **New-ComplianceSecurityFilter** or **Set-ComplianceSecurityFilter** cmdlets to create or change which datacenter the export will be routed through.</span></span>
  
    |<span data-ttu-id="c9dd9-222">**매개 변수 값**</span><span class="sxs-lookup"><span data-stu-id="c9dd9-222">**Parameter value**</span></span>|<span data-ttu-id="c9dd9-223">**데이터 센터 위치**</span><span class="sxs-lookup"><span data-stu-id="c9dd9-223">**Datacenter location**</span></span>|
    |:-----|:-----|
    |<span data-ttu-id="c9dd9-224">NAM</span><span class="sxs-lookup"><span data-stu-id="c9dd9-224">NAM</span></span>  <br/> |<span data-ttu-id="c9dd9-225">북미 (실제 데이터 센터는 미국)</span><span class="sxs-lookup"><span data-stu-id="c9dd9-225">North American (actual datacenters are in the US)</span></span>  <br/> |
    |<span data-ttu-id="c9dd9-226">EUR</span><span class="sxs-lookup"><span data-stu-id="c9dd9-226">EUR</span></span>  <br/> |<span data-ttu-id="c9dd9-227">유럽</span><span class="sxs-lookup"><span data-stu-id="c9dd9-227">Europe</span></span>  <br/> |
    |<span data-ttu-id="c9dd9-228">APC</span><span class="sxs-lookup"><span data-stu-id="c9dd9-228">APC</span></span>  <br/> |<span data-ttu-id="c9dd9-229">아시아 태평양</span><span class="sxs-lookup"><span data-stu-id="c9dd9-229">Asia Pacific</span></span>  <br/> |
    |<span data-ttu-id="c9dd9-230">CAN</span><span class="sxs-lookup"><span data-stu-id="c9dd9-230">CAN</span></span> <br/> |<span data-ttu-id="c9dd9-231">캐나다</span><span class="sxs-lookup"><span data-stu-id="c9dd9-231">Canada</span></span>
    
- <span data-ttu-id="c9dd9-232">**콘텐츠 검색 라우팅** -SharePoint 사이트 및 OneDrive 계정의 콘텐츠 검색을 위성 데이터 센터로 라우팅할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c9dd9-232">**Route content searches** - You can route the content searches of SharePoint sites and OneDrive accounts to a satellite data center.</span></span> <span data-ttu-id="c9dd9-233">즉, 검색을 실행할 데이터 센터 위치를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c9dd9-233">This means you can specify the datacenter location where searches will be run.</span></span>
    
    <span data-ttu-id="c9dd9-234">SharePoint 사이트 및 OneDrive 위치를 검색할 때 콘텐츠 검색이 실행 되는 데이터 센터를 제어 하려면 **Region** 매개 변수 값으로 다음 값을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="c9dd9-234">Use the following values for the **Region** parameter values to control which datacenter that Content Searches will run in when searching SharePoint sites and OneDrive locations.</span></span> <span data-ttu-id="c9dd9-235">다음 표에는 라우팅되는 데이터 센터 내보내기도 나와 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c9dd9-235">Note that the following table also shows which datacenter exports will be routed through.</span></span> 
  
    |<span data-ttu-id="c9dd9-236">**매개 변수 값**</span><span class="sxs-lookup"><span data-stu-id="c9dd9-236">**Parameter value**</span></span>|<span data-ttu-id="c9dd9-237">**내보내기에 대 한 데이터 센터 라우팅 위치**</span><span class="sxs-lookup"><span data-stu-id="c9dd9-237">**Datacenter routing locations for export**</span></span>|
    |:-----|:-----|
    |<span data-ttu-id="c9dd9-238">NAM</span><span class="sxs-lookup"><span data-stu-id="c9dd9-238">NAM</span></span>  <br/> |<span data-ttu-id="c9dd9-239">US</span><span class="sxs-lookup"><span data-stu-id="c9dd9-239">US</span></span>  <br/> |
    |<span data-ttu-id="c9dd9-240">EUR</span><span class="sxs-lookup"><span data-stu-id="c9dd9-240">EUR</span></span>  <br/> |<span data-ttu-id="c9dd9-241">유럽</span><span class="sxs-lookup"><span data-stu-id="c9dd9-241">Europe</span></span>  <br/> |
    |<span data-ttu-id="c9dd9-242">APC</span><span class="sxs-lookup"><span data-stu-id="c9dd9-242">APC</span></span>  <br/> |<span data-ttu-id="c9dd9-243">아시아 태평양</span><span class="sxs-lookup"><span data-stu-id="c9dd9-243">Asia Pacific</span></span>  <br/> |
    |<span data-ttu-id="c9dd9-244">CAN</span><span class="sxs-lookup"><span data-stu-id="c9dd9-244">CAN</span></span>  <br/> |<span data-ttu-id="c9dd9-245">US</span><span class="sxs-lookup"><span data-stu-id="c9dd9-245">US</span></span>  <br/> |
    |<span data-ttu-id="c9dd9-246">AUS</span><span class="sxs-lookup"><span data-stu-id="c9dd9-246">AUS</span></span>  <br/> |<span data-ttu-id="c9dd9-247">아시아 태평양</span><span class="sxs-lookup"><span data-stu-id="c9dd9-247">Asia Pacific</span></span>  <br/> |
    |<span data-ttu-id="c9dd9-248">KOR</span><span class="sxs-lookup"><span data-stu-id="c9dd9-248">KOR</span></span>  <br/> |<span data-ttu-id="c9dd9-249">조직의 기본 데이터 센터</span><span class="sxs-lookup"><span data-stu-id="c9dd9-249">The organization's default data center</span></span>  <br/> |
    |<span data-ttu-id="c9dd9-250">GBR</span><span class="sxs-lookup"><span data-stu-id="c9dd9-250">GBR</span></span>  <br/> |<span data-ttu-id="c9dd9-251">유럽</span><span class="sxs-lookup"><span data-stu-id="c9dd9-251">Europe</span></span>  <br/> |
    |<span data-ttu-id="c9dd9-252">JPN</span><span class="sxs-lookup"><span data-stu-id="c9dd9-252">JPN</span></span>  <br/> |<span data-ttu-id="c9dd9-253">아시아 태평양</span><span class="sxs-lookup"><span data-stu-id="c9dd9-253">Asia Pacific</span></span>  <br/> |
    |<span data-ttu-id="c9dd9-254">IND</span><span class="sxs-lookup"><span data-stu-id="c9dd9-254">IND</span></span>  <br/> |<span data-ttu-id="c9dd9-255">아시아 태평양</span><span class="sxs-lookup"><span data-stu-id="c9dd9-255">Asia Pacific</span></span>  <br/> |
    |<span data-ttu-id="c9dd9-256">LAM</span><span class="sxs-lookup"><span data-stu-id="c9dd9-256">LAM</span></span>  <br/> |<span data-ttu-id="c9dd9-257">US</span><span class="sxs-lookup"><span data-stu-id="c9dd9-257">US</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="c9dd9-258">검색 권한 필터에 **Region** 매개 변수를 지정 하지 않으면 조직 기본 SharePoint 지역이 검색 되 고 검색 결과가 가장 가까운 데이터 센터로 내보내집니다.</span><span class="sxs-lookup"><span data-stu-id="c9dd9-258">If you don't specify the **Region** parameter for a search permissions filter, the organizations default SharePoint region will be searched, then search results are exported to the closest datacenter.</span></span> 
  
<span data-ttu-id="c9dd9-259">다음은 준수 경계에 대 한 검색 권한 필터를 만들 때 **Region** 매개 변수를 사용 하는 예입니다.</span><span class="sxs-lookup"><span data-stu-id="c9dd9-259">Here are examples of using the **Region** parameter when creating search permission filters for compliance boundaries.</span></span> <span data-ttu-id="c9dd9-260">이 경우에는 네 번째 커피 자회사를 북미에 있고 Coho Winery가 유럽에 있는 것으로 가정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c9dd9-260">This assumes that the Fourth Coffee subsidiary is located in North America and that Coho Winery is in Europe.</span></span> 
  
```
New-ComplianceSecurityFilter -FilterName "Fourth Coffee Security Filter" -Users "Fourth Coffee eDiscovery Managers", "Fourth Coffee Investigators" -Filters "Mailbox_Department -eq 'FourthCoffee'", "Site_Department -eq 'FourthCoffee' -or Site_Path -like 'https://contoso.sharepoint.com/sites/FourthCoffee*'" -Action ALL -Region NAM
```

```
New-ComplianceSecurityFilter -FilterName "Coho Winery Security Filter" -Users "Coho Winery eDiscovery Managers", "Coho Winery Investigators" -Filters "Mailbox_Department -eq 'CohoWinery'", "Site_Department -eq 'CohoWinery' -or Site_Path -like 'https://contoso.sharepoint.com/sites/CohoWinery*'" -Action ALL -Region EUR
```
   
<span data-ttu-id="c9dd9-261">다중 지리적 환경에서 콘텐츠를 검색 하 고 내보낼 때는 다음 사항을 염두에 두어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c9dd9-261">Keep the following things in mind when searching and exporting content in multi-geo environments.</span></span>
  
- <span data-ttu-id="c9dd9-262">**Region** 매개 변수는 Exchange 사서함의 검색을 제어 하지 않습니다. 사서함을 검색할 때 모든 데이터 센터가 검색 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c9dd9-262">The **Region** parameter doesn't control searches of Exchange mailboxes; all data centers will be searched when you search mailboxes.</span></span> <span data-ttu-id="c9dd9-263">Exchange 사서함을 검색할 수 있는 범위를 제한 하려면 검색 권한 필터를 만들거나 변경할 때 **Filters** 매개 변수를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="c9dd9-263">To limit the scope of which Exchange mailboxes can be searched, use the **Filters** parameter when creating or changing a search permissions filter.</span></span> 
    
- <span data-ttu-id="c9dd9-264">EDiscovery 관리자가 여러 SharePoint 지역에서 검색 해야 하는 경우에는 검색 권한 필터에 사용할 수 있는 다른 사용자 계정을 해당 eDiscovery 관리자에 게 만들어야 합니다. SharePoint 사이트 또는 OneDrive 계정이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c9dd9-264">If it's necessary for an eDiscovery Manager to search across multiple SharePoint regions, you'll need to create a different user account for that eDiscovery manager that can be used in the search permissions filter to specify the alternate region where the SharePoint sites or OneDrive accounts are located.</span></span>
    
- <span data-ttu-id="c9dd9-265">SharePoint 및 OneDrive에서 콘텐츠를 검색할 때 **Region** 매개 변수는 ediscovery 관리자가 ediscovery 조사를 수행 하는 기본 또는 위성 위치를 검색 하도록 지시 합니다.</span><span class="sxs-lookup"><span data-stu-id="c9dd9-265">When searching for content in SharePoint and OneDrive, the **Region** parameter directs searches to either the main or satellite location where the eDiscovery manager will conduct eDiscovery investigations.</span></span> <span data-ttu-id="c9dd9-266">EDiscovery 관리자가 SharePoint 및 OneDrive 사이트 검색 사용 권한 필터에 지정 된 지역 외부를 검색 하는 경우 검색 결과가 반환 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c9dd9-266">If an eDiscovery manager searches SharePoint and OneDrive sites outside of the region that's specified in the search permissions filter, no search results will be returned.</span></span> 
    
- <span data-ttu-id="c9dd9-267">검색 결과를 내보낼 때 모든 콘텐츠 위치의 콘텐츠 (예를 들어 Exchange, 비즈니스용 Skype, SharePoint, OneDrive 및 기타 Office 365 서비스는 콘텐츠 검색 도구를 사용 하 여 검색할 수 있음)의 Azure 저장소 위치에 업로드 됩니다. **Region** 매개 변수에 의해 지정 된 데이터 센터입니다.</span><span class="sxs-lookup"><span data-stu-id="c9dd9-267">When exporting search results, content from all content locations (including Exchange, Skype for Business, SharePoint, OneDrive and other Office 365 services that you can search by using the Content Search tool) will be uploaded to the Azure storage location in the data center that's specified by the **Region** parameter.</span></span> <span data-ttu-id="c9dd9-268">이렇게 하면 조직이 제어 테두리에 걸쳐 콘텐츠를 내보낼 수 없도록 하 여 규정 준수를 유지 하는 데 도움이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c9dd9-268">This helps organizations stay within compliance by not allowing content to be exported across controlled borders.</span></span> <span data-ttu-id="c9dd9-269">검색 권한 필터에 지역이 지정 되어 있지 않으면 콘텐츠가 조직의 기본 영역에 업로드 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c9dd9-269">If no region is specified in the search permissions filter, content is uploaded to the organization's default region.</span></span> 
    
- <span data-ttu-id="c9dd9-270">다음 명령을 실행 하 여 기존 검색 권한 필터를 편집 하 여 지역을 추가 하거나 변경할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c9dd9-270">You can edit an existing search permissions filter to add or change the region by running the following command:</span></span>

    ```
    Set-ComplianceSecurityFilter -FilterName <Filter name>  -Region <Region>
    ```
 
## <a name="frequently-asked-questions"></a><span data-ttu-id="c9dd9-271">자주하는 질문</span><span class="sxs-lookup"><span data-stu-id="c9dd9-271">Frequently asked questions</span></span>

 <span data-ttu-id="c9dd9-272">**New-compliancesecurityfilter 및 New-compliancesecurityfilter cmdlet을 사용 하 여 검색 권한 필터를 만들고 관리할 수 있는 사람은 누구 인가요?**</span><span class="sxs-lookup"><span data-stu-id="c9dd9-272">**Who can create and manage search permissions filters (using New-ComplianceSecurityFilter and Set-ComplianceSecurityFilter cmdlets )?**</span></span>
  
<span data-ttu-id="c9dd9-273">검색 사용 권한 필터를 만들고 보고 수정 하려면 Security & 준수 센터에서 조직 관리 역할 그룹의 구성원 이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c9dd9-273">To create, view and modify search permissions filters, you have to be a member of the Organization Management role group in the Security & Compliance Center.</span></span>
  
 <span data-ttu-id="c9dd9-274">**여러 기관에 걸쳐 있는 둘 이상의 역할 그룹에 eDiscovery 관리자를 할당 하는 경우, 한 에이전시에서 콘텐츠를 검색 하려면 어떻게 해야 합니까?**</span><span class="sxs-lookup"><span data-stu-id="c9dd9-274">**If an eDiscovery manager is assigned to more than one role group that spans multiple agencies, how do they search for content in one agency or the other?**</span></span>
  
<span data-ttu-id="c9dd9-275">EDiscovery 관리자는 검색 쿼리에 특정 에이전시로 제한 되는 매개 변수를 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c9dd9-275">The eDiscovery manager can add parameters to their search query that will restrict the search to a specific agency.</span></span> <span data-ttu-id="c9dd9-276">예를 들어 조직에서 **CustomAttribute10** 속성을 지정 하 여 기관을 차별화 하는 경우 다음을 검색 쿼리에 추가 하 여 특정 에이전시에서 사서함 및 OneDrive 계정을 검색할 수 있습니다 `CustomAttribute10:<value> AND Site_ComplianceAttribute:<value>`.</span><span class="sxs-lookup"><span data-stu-id="c9dd9-276">For example, if an organization has specified the **CustomAttribute10** property to differentiate agencies, they can append the following to their search query to search mailboxes and OneDrive accounts in a specific agency:  `CustomAttribute10:<value> AND Site_ComplianceAttribute:<value>`.</span></span>
  
 <span data-ttu-id="c9dd9-277">**검색 권한 필터에서 준수 특성으로 사용 되는 특성의 값이 변경 된 경우 어떻게 되나요?**</span><span class="sxs-lookup"><span data-stu-id="c9dd9-277">**What happens if the value of the attribute that's used as the compliance attribute in a search permissions filter is changed?**</span></span>
  
<span data-ttu-id="c9dd9-278">필터에 사용 된 특성의 값이 변경 되는 경우 검색 권한 필터에 대해 최대 3 일이 소요 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c9dd9-278">It takes up to 3 days for a search permissions filter to enforce the compliance boundary if the value of the attribute that's used in the filter is changed.</span></span> <span data-ttu-id="c9dd9-279">예를 들어 Contoso 시나리오에서, 네 번째 커피 에이전시의 사용자가 Coho Winery 에이전시로 전송 된다는 것을 가정해 보겠습니다.</span><span class="sxs-lookup"><span data-stu-id="c9dd9-279">For example, in the Contoso scenario let's say that a user in the Fourth Coffee agency is transferred to the Coho Winery agency.</span></span> <span data-ttu-id="c9dd9-280">따라서 사용자 개체의 **부서** 특성 값은 *FourthCoffee* 에서 *CohoWinery* 로 변경 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c9dd9-280">As a result, the value of the **Department** attribute on the user object is changed from  *FourthCoffee*  to  *CohoWinery*  .</span></span> <span data-ttu-id="c9dd9-281">이 상황에서 네 번째 커피 eDiscovery 및 투자자는 해당 사용자에 대 한 검색 결과를 3 일 동안 (특성이 변경 된 후)로 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c9dd9-281">In this situation, Fourth Coffee eDiscovery and investors will get search results for that user for up 3 days after the attribute is changed.</span></span> <span data-ttu-id="c9dd9-282">마찬가지로, Coho Winery eDiscovery 관리자 및 investigators에서 사용자에 대 한 검색 결과를 가져올 때까지 최대 3 일이 걸립니다.</span><span class="sxs-lookup"><span data-stu-id="c9dd9-282">Similarly, it will take up to 3 days before Coho Winery eDiscovery managers and investigators will get search results for the user.</span></span> 
  
 <span data-ttu-id="c9dd9-283">**EDiscovery 관리자가 두 개의 별도 준수 경계의 콘텐츠를 볼 수 있습니까?**</span><span class="sxs-lookup"><span data-stu-id="c9dd9-283">**Can an eDiscovery manager see content from two separate compliance boundaries?**</span></span>
  
<span data-ttu-id="c9dd9-284">예.</span><span class="sxs-lookup"><span data-stu-id="c9dd9-284">Yes.</span></span> <span data-ttu-id="c9dd9-285">이 작업은 두 기관에 모두 표시 되는 역할 그룹에 사용자를 추가 하 여 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c9dd9-285">This can be done by adding the user to role groups that have visibility to both agencies.</span></span>
  
 <span data-ttu-id="c9dd9-286">**검색 사용 권한 필터가 eDiscovery 사례 보존, Office 365 보존 정책 또는 DLP에 대해 작동 하나요?**</span><span class="sxs-lookup"><span data-stu-id="c9dd9-286">**Do search permissions filters work for eDiscovery case holds, Office 365 retention policies, or DLP?**</span></span>
  
<span data-ttu-id="c9dd9-287">아니요, 지금은 아님</span><span class="sxs-lookup"><span data-stu-id="c9dd9-287">No, not at this time</span></span>
  
 <span data-ttu-id="c9dd9-288">**콘텐츠를 내보내는 위치를 제어 하는 영역을 지정 했지만 해당 지역에 SharePoint 조직이 없는 경우에도 SharePoint를 검색할 수 있나요?**</span><span class="sxs-lookup"><span data-stu-id="c9dd9-288">**If I specify a region to control where content is exported, but I don't have a SharePoint organization in that region, can I still search SharePoint?**</span></span>
  
<span data-ttu-id="c9dd9-289">검색 권한 필터에 지정 된 지역이 조직에 없는 경우에는 기본 지역이 검색 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c9dd9-289">If the region specified in the search permissions filter doesn't exist in your organization, the default region will be searched.</span></span>
  
 <span data-ttu-id="c9dd9-290">**조직에서 만들 수 있는 검색 권한 필터의 최대 수는 얼마나 됩니까?**</span><span class="sxs-lookup"><span data-stu-id="c9dd9-290">**What is the maximum number of search permissions filters that can be created in an organization?**</span></span>
  
<span data-ttu-id="c9dd9-291">조직에서 만들 수 있는 검색 권한 필터의 수에는 제한이 없습니다.</span><span class="sxs-lookup"><span data-stu-id="c9dd9-291">There is no limit to the number of search permissions filters that can be created in an organization.</span></span> <span data-ttu-id="c9dd9-292">그러나 검색 권한 필터가 100 개 보다 많으면 검색 성능이 영향을 받습니다.</span><span class="sxs-lookup"><span data-stu-id="c9dd9-292">However, search performance will be impacted when there are more than 100 search permissions filters.</span></span> <span data-ttu-id="c9dd9-293">조직의 검색 권한 필터 수를 가능한 한 작게 유지 하려면 가능 하면 Exchange, SharePoint 및 OneDrive에 대 한 규칙을 단일 검색 권한 필터에 결합 하는 필터를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c9dd9-293">To keep the number of search permissions filters in your organization as small as possible, create filters that combine rules for Exchange, SharePoint, and OneDrive into a single search permissions filter whenever possible.</span></span>
