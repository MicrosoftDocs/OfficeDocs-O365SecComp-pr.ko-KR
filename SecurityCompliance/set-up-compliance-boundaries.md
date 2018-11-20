---
title: Office 365에서 eDiscovery 조사에 대한 준수 경계 설정
ms.author: markjjo
author: markjjo
manager: laurawi
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MOE150
- MET150
ms.assetid: 1b45c82f-26c8-44fb-9f3b-b45436fe2271
description: 규정 준수 경계를 사용 하 여 eDiscovery 관리자를 검색할 수 있는 사용자 콘텐츠 위치를 제어 하는 Office 365 조직 내에서 논리적 경계를 만들 수 있습니다. 준수 경계 어떤 사서함, SharePoint 사이트를 제어 하 (도 요건 보안 필터)을 필터링 하는 검색 사용 권한을 사용 하 고 OneDrive 계정을 특정 사용자가 검색할 수 있습니다.
ms.openlocfilehash: 2bebd29fa7701ba07aae7170142263aeaec5569e
ms.sourcegitcommit: c7264f3a6a97f1ff544544e2c722e7825e265fa1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/14/2018
ms.locfileid: "26299242"
---
# <a name="set-up-compliance-boundaries-for-ediscovery-investigations-in-office-365"></a><span data-ttu-id="7bb92-104">Office 365에서 eDiscovery 조사에 대한 준수 경계 설정</span><span class="sxs-lookup"><span data-stu-id="7bb92-104">Set up compliance boundaries for eDiscovery investigations in Office 365</span></span>

<span data-ttu-id="7bb92-p102">규정 준수 경계 사용자 콘텐츠 위치 (예: 사서함, SharePoint 사이트 및 OneDrive 계정)는 eDiscovery 관리자를 검색할 수를 제어 하는 Office 365 조직 내에서 논리적 경계를 만듭니다. 또한 준수 경계 사용자 제어는 법률, 인사, 또는 조직 내의 다른 조사를 관리 하는 데 사용 되는 eDiscovery 사례에 액세스할 수 있습니다. 규정 준수 경계에 대 한 요구는 필요한 지리적 현재 사용 하 고 규정을 준수 해야 하는 다중 국가 기업 및 정부 기관에서 다른 종종 나뉘며 하는 경우가 많습니다. Office 365 만족 하는 준수 경계 도움말에서에서 수행 하는 경우 이러한 요구 사항 콘텐츠 검색 및 eDiscovery 사례와 관리 조사 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bb92-p102">Compliance boundaries create logical boundaries within an Office 365 organization that control the user content locations (such as mailboxes, SharePoint sites, and OneDrive accounts) that eDiscovery managers can search. Additionally, compliance boundaries control who can access eDiscovery cases used to manage the legal, human resources, or other investigations within your organization. The need for compliance boundaries is often necessary for multi-nations corporations that have to respect geographical boarders and regulations, and for governments, which are often divided into different agencies. In Office 365, compliance boundaries help you meet these requirements when performing content searches and managing investigations with eDiscovery cases.</span></span>
  
<span data-ttu-id="7bb92-109">다음 그림에서 준수 경계 작동 하는 방법에 대해 설명 하는 예제를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bb92-109">We'll use the example in the following illustration to explain how compliance boundaries work.</span></span>
  
![관리 역할 및 기관에 대 한 액세스 제어 eDisocovery의 경우에는 권한을 그룹화 하는 검색 권한 필터의 규정 준수 경계도 구성](media/5c206cc8-a6eb-4d6b-a3a5-21e158791f9a.png)
  
<span data-ttu-id="7bb92-p103">이 예제에서는 Contoso LTD는 Fourth Coffee 및 Coho Winery 두 자회사의 구성 되는 Office 365 조직입니다. 비즈니스는 eDiscovery 관리자 및 수 사관 수만 Exchange 사서함, OneDrive 계정 및 SharePoint 사이트를 자신의 기관에서 검색을 해야 합니다. 또한 eDiscovery 관리자와 수 사관을 보려면 eDiscovery 사례에는 해당 기관에서 및의 멤버는 하는 경우에만 액세스할 수 있습니다. 규정 준수 경계 이러한 요구 사항을 충족 하는 방법을 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="7bb92-p103">In this example, Contoso LTD is an Office 365 organization that consists of two subsidiaries, Fourth Coffee and Coho Winery. The business requires that eDiscovery mangers and investigators can only search the Exchange mailboxes, OneDrive accounts, and SharePoint sites in their agency. Additionally, eDiscovery managers and investigators can only see eDiscovery cases in the in their agency, and they can only access the cases that they're a member of. Here's how compliance boundaries meet these requirements.</span></span>
  
- <span data-ttu-id="7bb92-p104">검색 사용 권한을 eDiscovery 관리자와 수 사관을 검색할 수 있는 콘텐츠 위치 콘텐츠 검색 컨트롤의 기능을 필터링 합니다. 즉, eDiscovery 관리자와 Fourth Coffee 기관에서 수 사관은 Fourth Coffee 자회사에서 콘텐츠 위치를만 검색할 수 있습니다. Coho Winery 자회사에 동일한 제한이 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7bb92-p104">The search permissions filtering functionality in Content Search controls the content locations that eDiscovery managers and investigators can search. This means eDiscovery managers and investigators in the Fourth Coffee agency can only search content locations in the Fourth Coffee subsidiary. The same restriction applies to the Coho Winery subsidiary.</span></span>
    
    <span data-ttu-id="7bb92-p105">Office 365 보안에서 eDiscovery 사례를 볼 수 있는 사용자 제어를 그룹화 하는 역할 &amp; 준수 센터입니다. 즉, eDiscovery 관리자와 수 사관 자신의 기관에서 eDiscovery 사례 볼만 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7bb92-p105">Role groups control who can see the eDiscovery cases in the Office 365 Security &amp; Compliance Center. This means that eDiscovery managers and investigators can only see the eDiscovery cases in their agency.</span></span>
    
- <span data-ttu-id="7bb92-p106">역할 그룹 eDiscovery 사례에 구성원을 할당할 수 있는 사람 제어할 수도 있습니다. 즉, eDiscovery 관리자와 수 사관은 자신이 구성원 인지 확인 하는 경우에 멤버를만 할당할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7bb92-p106">Role groups also control who can assign members to an eDiscovery case. This means eDiscovery managers and investigators can only assign members to cases that they themselves are a member of.</span></span>
    
<span data-ttu-id="7bb92-122">규정 준수 경계를 설정 하는 프로세스는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="7bb92-122">Here's the process for setting up compliance boundaries:</span></span>
  
[<span data-ttu-id="7bb92-123">1 단계: 기관에서 사용자를 정의 하는 사용자 특성을 식별</span><span class="sxs-lookup"><span data-stu-id="7bb92-123">Step 1: Identify a user attribute to define your agencies</span></span>](#step-1-identify-a-user-attribute-to-define-your-agencies)

[<span data-ttu-id="7bb92-124">2 단계: OneDrive 계정에 사용자 특성을 동기화 하려면 Microsoft 기술 지원 서비스 요청 파일</span><span class="sxs-lookup"><span data-stu-id="7bb92-124">Step 2: File a request with Microsoft Support to synchronize the user attribute to OneDrive accounts</span></span>](#step-2-file-a-request-with-microsoft-support-to-synchronize-the-user-attribute-to-onedrive-accounts)

[<span data-ttu-id="7bb92-125">3 단계: 각 기관에 대 한 역할 그룹 만들기</span><span class="sxs-lookup"><span data-stu-id="7bb92-125">Step 3: Create a role group for each agency</span></span>](#step-3-create-a-role-group-for-each-agency)

[<span data-ttu-id="7bb92-126">단계 4: 준수 경계를 사용 하 여 적용 하려면 검색 권한 필터 만들기</span><span class="sxs-lookup"><span data-stu-id="7bb92-126">Step 4: Create a search permissions filter to enforce the compliance boundary</span></span>](#step-4-create-a-search-permissions-filter-to-enforce-the-compliance-boundary)

[<span data-ttu-id="7bb92-127">5 단계: 내 기관 조사에 대 한 eDiscovery 사례 만들기</span><span class="sxs-lookup"><span data-stu-id="7bb92-127">Step 5: Create an eDiscovery case for an intra-agency investigations</span></span>](#step-5-create-an-ediscovery-case-for-an-intra-agency-investigations)
  
## <a name="step-1-identify-a-user-attribute-to-define-your-agencies"></a><span data-ttu-id="7bb92-128">1 단계: 기관에서 사용자를 정의 하는 사용자 특성을 식별</span><span class="sxs-lookup"><span data-stu-id="7bb92-128">Step 1: Identify a user attribute to define your agencies</span></span>

<span data-ttu-id="7bb92-p107">첫번째 단계는 도구를 사용 하는 Azure Active Directory 특성을 선택 하 여 기관에서 정의 합니다. 이 특성을 사용 하 여이 특성에 대 한 특정 값을 할당 된 사용자의 콘텐츠 위치에만 검색 하려면 관리자 eDiscovery를 제한 하는 검색 사용 권한 필터를 만들 수 됩니다. 예, **부서** 특성을 사용 하기로 결정 Contoso 가정해 보겠습니다. 번호 Fourth Coffee 자회사에서 사용자에 대해이 특성에 대 한 값은 `FourthCoffee` 번호 Coho Winery 자회사에서 사용자에 대 한 값은 및 `CohoWinery`합니다. 4 단계에서에서 사용할이 `attribute:value` 쌍 (예: *부서: FourthCoffee* ) 사용자를 제한 하려면 콘텐츠 eDiscovery 관리자를 검색할 수 있는 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="7bb92-p107">The first step is to choose an Azure Active Directory attribute to use that will define your agencies. This attribute will be used to create the search permissions filter that limits an eDiscovery manager to search only the content locations of users who are assigned a specific value for this attribute. For example, let's say Contoso decides to use the **Department** attribute. The value for this attribute for users in the Fourth Coffee subsidiary would be  `FourthCoffee`  and the value for users in Coho Winery subsidiary would be `CohoWinery`. In Step 4, you'll use this  `attribute:value`  pair (for example,  *Department:FourthCoffee*  ) to limit the user content locations that eDiscovery managers can search.</span></span> 
  
<span data-ttu-id="7bb92-134">규정 준수 경계에 사용할 수 있는 Azure Active Directory 사용자 특성의 목록은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="7bb92-134">Here's a list of Azure Active Directory user attributes that you can use for compliance boundaries:</span></span>
  
- <span data-ttu-id="7bb92-135">회사</span><span class="sxs-lookup"><span data-stu-id="7bb92-135">Company</span></span>
    
- <span data-ttu-id="7bb92-136">CountryCode</span><span class="sxs-lookup"><span data-stu-id="7bb92-136">CountryCode</span></span>
    
- <span data-ttu-id="7bb92-137">CustomAttribute1-CustomAttribute15</span><span class="sxs-lookup"><span data-stu-id="7bb92-137">CustomAttribute1 - CustomAttribute15</span></span>
    
- <span data-ttu-id="7bb92-138">부서</span><span class="sxs-lookup"><span data-stu-id="7bb92-138">Department</span></span>
    
- <span data-ttu-id="7bb92-139">사무실</span><span class="sxs-lookup"><span data-stu-id="7bb92-139">Office</span></span>
    
<span data-ttu-id="7bb92-140">더 많은 사용자 특성이 특히 Exchange 사서함을 사용할 수 있지만 위에 나열 된 특성 하는 사람은 OneDrive 하 여 현재 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bb92-140">Although more user attributes are available, particularly for Exchange mailboxes, the attributes listed above are the only ones currently supported by OneDrive.</span></span>
  
## <a name="step-2-file-a-request-with-microsoft-support-to-synchronize-the-user-attribute-to-onedrive-accounts"></a><span data-ttu-id="7bb92-141">2 단계: OneDrive 계정에 사용자 특성을 동기화 하려면 Microsoft 기술 지원 서비스 요청 파일</span><span class="sxs-lookup"><span data-stu-id="7bb92-141">Step 2: File a request with Microsoft Support to synchronize the user attribute to OneDrive accounts</span></span>

<span data-ttu-id="7bb92-p108">다음 단계를 선택한 1 단계에서에서 모든 OneDrive 계정에 조직에서 Azure Active Directory 특성을 동기화 하려면 Microsoft 기술 지원 서비스 요청 파일입니다. 특성 (및 그 값)이이 동기화 발생 한 후 SharePoint 라는에서 숨겨진된 관리 속성에 매핑할 수는 1 단계에서에서 선택한 `ComplianceAttribute`합니다. 이 특성을 사용 하 여 4 단계에서에서 onedrive 검색 권한 필터를 만드는 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7bb92-p108">The next step is to file a request with Microsoft Support to synchronize the Azure Active Directory attribute that you chose in Step 1 to all OneDrive accounts in your organization. After this synchronization occurs, the attribute (and its value) that you chose in Step 1 will be mapped to a hidden managed property in SharePoint named  `ComplianceAttribute`. You'll use this attribute to create the search permissions filter for OneDrive in Step 4.</span></span>
  
<span data-ttu-id="7bb92-145">Microsoft 기술 지원 서비스에 요청을 제출 하는 경우 다음 정보를 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bb92-145">Include the following information when you submit the request to Microsoft support:</span></span>
  
- <span data-ttu-id="7bb92-146">Office 365 조직의 기본 도메인 이름</span><span class="sxs-lookup"><span data-stu-id="7bb92-146">The default domain name of your Office 365 organization</span></span>
    
- <span data-ttu-id="7bb92-147">단계 1) (에서 Azure Active Directory 특성의 이름</span><span class="sxs-lookup"><span data-stu-id="7bb92-147">The name of the Azure Active Directory attribute (from Step 1)</span></span>
    
- <span data-ttu-id="7bb92-p109">다음 제목 또는 지원 요청의 용도 설명: "OneDrive에 대 한 비즈니스 동기화와 Azure Active Directory에 대 한 준수 보안 필터 사용" 합니다. 이렇게 하면 요청을 구현 하 게 수행 하는 Office 365 eDiscovery 엔지니어링 팀에 요청을 라우팅할 하는 데 도움이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7bb92-p109">The following title or description of the purpose of the support request: "Enable OneDrive for Business Synchronization with Azure Active Directory for Compliance Security Filters". This will help route the request to the Office 365 eDiscovery engineering team who will implement the request.</span></span>
    
<span data-ttu-id="7bb92-p110">엔지니어링 변경 되는 특성 OneDrive를 동기화 후 Microsoft 기술 지원 서비스 사용자에 게 변경 된 빌드 번호 및 예상된 배포 날짜입니다. 4-6 주 지원 요청을 제출한 후에 배포 프로세스는 일반적으로 시간이 메모 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bb92-p110">After the engineering change is made and the attribute is synchronized to OneDrive, Microsoft Support will send you the build number that the change was made in and an estimated deployment date. Note that the deployment process usually takes 4-6 weeks after you submit the support request.</span></span>
  
 <span data-ttu-id="7bb92-p111">**중요:** 변경을 배포 하기 전에 단계 3-5 단계를 완료할 수 있습니다. 하지만 콘텐츠 검색을 실행 변경을 배포한 후까지 검색 권한 필터에 지정 된 OneDrive 사이트에서 문서를 반환 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7bb92-p111">**Important:** You can complete Step 3 through Step 5 before the change is deployed. But running content searches won't return documents from OneDrive sites specified in the search permissions filter until after the change is deployed.</span></span> 
  
## <a name="step-3-create-a-role-group-for-each-agency"></a><span data-ttu-id="7bb92-154">3 단계: 각 기관에 대 한 역할 그룹 만들기</span><span class="sxs-lookup"><span data-stu-id="7bb92-154">Step 3: Create a role group for each agency</span></span>

<span data-ttu-id="7bb92-p112">Office 365 보안에서 역할 그룹을 만들려면 다음 단계는 &amp; 준수 센터에 기관 맞춰집니다입니다. 기본 제공 eDiscovery 관리자 그룹은 복사 적절 한 구성원을 추가 하 고 사용자의 요구에 적용할 수 있는 역할을 제거 하 여 새 역할 그룹을 만드는 것이 좋습니다. EDiscovery 관련 된 역할에 대 한 자세한 내용은 참조 [Office 365 보안에서 eDiscovery 사용 권한을 할당 &amp; 준수 센터](assign-ediscovery-permissions.md)합니다.</span><span class="sxs-lookup"><span data-stu-id="7bb92-p112">The next step is to create the role groups in the Office 365 Security &amp; Compliance Center that will align with your agencies. We recommend that you create a new role group by copying the built-in eDiscovery Managers group, adding the appropriate members, and removing roles that may not be applicable to your needs. For more information about eDiscovery-related roles, see [Assign eDiscovery permissions in the Office‍ 365 Security &amp; Compliance Center](assign-ediscovery-permissions.md).</span></span>
  
<span data-ttu-id="7bb92-158">역할 그룹을 만들려면 보안에서 **사용 권한** 페이지로 이동 &amp; 준수 센터를 사용 하 여 준수 경계 및 eDiscovery 사례 조사를 관리 하는 각 기관에서 각 팀에 대 한 역할 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="7bb92-158">To create the role groups, go to the **Permissions** page in the Security &amp; Compliance Center and create a role group for each team in each agency that will use compliance boundaries and eDiscovery cases to manage investigations.</span></span> 
  
<span data-ttu-id="7bb92-159">Contoso 준수 경계 시나리오를 사용 하 여 4 개의 역할 그룹 만들 필요 하 고 적절 한 구성원 각 명령에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bb92-159">Using the Contoso compliance boundaries scenario, four role groups need to be created and the appropriate members added to each one.</span></span>
  
- <span data-ttu-id="7bb92-160">Fourth Coffee eDiscovery 관리자</span><span class="sxs-lookup"><span data-stu-id="7bb92-160">Fourth Coffee eDiscovery Managers</span></span>
    
- <span data-ttu-id="7bb92-161">Fourth Coffee 수 사관</span><span class="sxs-lookup"><span data-stu-id="7bb92-161">Fourth Coffee Investigators</span></span>
    
- <span data-ttu-id="7bb92-162">Coho Winery eDiscovery 관리자</span><span class="sxs-lookup"><span data-stu-id="7bb92-162">Coho Winery eDiscovery Managers</span></span>
    
- <span data-ttu-id="7bb92-163">Coho Winery 수 사관</span><span class="sxs-lookup"><span data-stu-id="7bb92-163">Coho Winery Investigators</span></span>
    

  
## <a name="step-4-create-a-search-permissions-filter-to-enforce-the-compliance-boundary"></a><span data-ttu-id="7bb92-164">단계 4: 준수 경계를 사용 하 여 적용 하려면 검색 권한 필터 만들기</span><span class="sxs-lookup"><span data-stu-id="7bb92-164">Step 4: Create a search permissions filter to enforce the compliance boundary</span></span>
<span data-ttu-id="7bb92-165"><a name="step4"> </a></span><span class="sxs-lookup"><span data-stu-id="7bb92-165"></span></span>

<span data-ttu-id="7bb92-p113">각 기관에 대 한 역할 그룹을 만든 후 다음 단계를 해당 특정 기관에 각 역할 그룹에 연결 하는 검색 사용 권한 필터를 만드는 것 하 고 자체 규정 준수 경계를 정의 합니다. 각 기관에 대 한 하나의 검색 권한 필터를 만들 해야 합니다. 보안 권한 필터를 만드는 방법에 대 한 자세한 내용은 [콘텐츠 검색에 대 한 필터링 Configure permissions](permissions-filtering-for-content-search.md)을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="7bb92-p113">After you've created role groups for each agency, the next step is to create the search permissions filters that associate each role group to its specific agency and defines the compliance boundary itself. You need to create one search permissions filter for each agency. For more information about creating security permissions filters, see [Configure permissions filtering for Content Search](permissions-filtering-for-content-search.md).</span></span>
  
<span data-ttu-id="7bb92-169">규정 준수 경계에 사용 되는 검색 권한 필터를 만드는 사용 되는 구문은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="7bb92-169">Here's the syntax that's used to create a search permissions filter used for compliance boundaries.</span></span>

```
New-ComplianceSecurityFilter -FilterName <name of filter> -Users <role groups> -Filters "Mailbox_<Compliance attribute from Step 1>  -eq '<AttributeVale> '", "Site_ComplianceAttribute  -eq <AttributeValue>' -or Site_Path -like <SharePointURL> *'" -Action <Action >
```
  
<span data-ttu-id="7bb92-170">각 매개 변수는 명령에서에 대 한 설명을 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="7bb92-170">Here's a description of each parameter in the command:</span></span>
  
-  <span data-ttu-id="7bb92-p114">`FilterName`-필터의 이름을 지정 합니다. 설명 또는 필터링 하는 배출량 감소를 식별 하는 이름을 사용 하 여에서 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7bb92-p114">`FilterName` - Specifies the name of the filter. Use a name that describes or identifies the agency that filter will be used in.</span></span> 
    
-  <span data-ttu-id="7bb92-p115">`Users`-사용자 또는 수행 하는 콘텐츠 검색 작업에 적용 된이 필터를 가져올 그룹을 지정 합니다. 규정 준수 경계에 대 한이 매개 변수는에 대 한 필터를 만들려는 기관에서 역할 그룹 (3 단계에서에서 만든)을 지정 합니다. 이 다중값 매개 변수를 쉼표로 구분 하 여 하나 이상의 역할 그룹에 사용할 수 있도록 note 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bb92-p115">`Users` - Specifies the users or groups who get this filter applied to the Content Search actions they perform. For compliance boundaries, this parameter specifies the role groups (that you created in Step 3) in the agency that you're creating the filter for. Note this is a multi-value parameter so you can include one or more role groups, separated by commas.</span></span> 
    
-  <span data-ttu-id="7bb92-p116">`Filters`-필터에 대 한 검색 조건을 지정합니다. 규정 준수 경계에 대 한 다음 필터를 정의 합니다. 각 사용자 콘텐츠 위치에 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7bb92-p116">`Filters` - Specifies the search criteria for the filter. For the compliance boundaries, you will define the following filters. Each one applies to a user content location.</span></span> 
    
  -  <span data-ttu-id="7bb92-p117">`Mailbox`--사서함에 정의 된 역할 그룹을 지정 하는 중의 `Users` 매개 변수를 검색할 수 있습니다. 규정 준수 경계 *ComplianceAttribute* 1 단계에서에서 식별 되는 동일한 특성 이며 *특성 값* 배출량 감소를 지정 합니다. 이 필터에만 특정 기관;에서 사서함을 검색 하는 역할 그룹의 구성원 수 있도록 허용 예, `"Mailbox_Department -eq 'FourthCoffee'"` 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bb92-p117">`Mailbox` - Specifies the mailboxes that the role groups defined in the  `Users` parameter can search. For compliance boundaries,  *ComplianceAttribute*  is the same attribute that you identified in Step 1 and  *AttributeValue*  specifies the agency. This filter allow members of the role group to only search the mailboxes in a specific agency; for example,  `"Mailbox_Department -eq 'FourthCoffee'"` .</span></span> 
    
  -  <span data-ttu-id="7bb92-p118">`Site`-OneDrive 계정에 정의 된 역할 그룹에 지정 된 `Users` 매개 변수를 검색할 수 있습니다. OneDrive 필터에 대 한 실제 문자열을 사용 하 여 `ComplianceAttribute`; 1 단계에서에서 확인 되는 2 단계;에서 제출 된 지원 요청으로 인해 OneDrive 계정에 동기화 되는 동일한 특성에 매핑할 것이  *특성 값* 배출량 감소를 지정합니다. 이 필터에만 특정 기관;의 OneDrive 계정을 검색 하려면 역할 그룹의 구성원 수 있도록 허용 예, `"Site_ComplianceAttribute -eq 'FourthCoffee'"`합니다.</span><span class="sxs-lookup"><span data-stu-id="7bb92-p118">`Site` - Specifies the OneDrive accounts that the role groups defined in the  `Users` parameter can search. For the OneDrive filter, use the actual string  `ComplianceAttribute`; this will map to the same attribute that you identified in Step 1 and that's synchronized to OneDrive accounts as a result of the support request that you submitted in Step 2;  *AttributeValue*  specifies the agency. This filter allow members of the role group to only search the OneDrive accounts in a specific agency; for example,  `"Site_ComplianceAttribute -eq 'FourthCoffee'"`.</span></span>
    
  -  <span data-ttu-id="7bb92-p119">`Site_Path`--역할 그룹에 정의 하는 SharePoint 사이트를 지정 하는 중의 `Users` 매개 변수를 검색할 수 있습니다. *SharePointURL* 역할 그룹의 멤버를 검색할 수 있는 기관에서 사이트를 지정 합니다. 예를 들어`Site_Path -like 'https://contoso.sharepoint.com/sites/FourthCoffee*'"`</span><span class="sxs-lookup"><span data-stu-id="7bb92-p119">`Site_Path` - Specifies the SharePoint sites that the role groups defined in the  `Users` parameter can search. The  *SharePointURL*  specifies the sites in the agency that members of the role group can search; for example,  `Site_Path -like 'https://contoso.sharepoint.com/sites/FourthCoffee*'"`</span></span>
    
-  <span data-ttu-id="7bb92-p120">`Action`-필터에 적용 되는 규정 준수 검색 동작의 유형을 지정 합니다. 예 `-Action Search` 역할 그룹의 구성원에 정의 된 경우에 필터를 적용 것은 `Users` 매개 변수는 콘텐츠 검색을 실행 합니다. 이 경우 검색 결과 내보낼 때에 필터가 적용 하지 않습니다. 규정 준수 경계를 사용 하 여 `-Action All` 하므로 모든 검색 작업에 필터가 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7bb92-p120">`Action` - Specifies the type of Compliance Search action that the filter is applied to. For example,  `-Action Search` would only apply the filter when members of the role groups defined in the  `Users` parameter runs a content search. In this case, the filter wouldn't be applied when exporting search results. For compliance boundaries, use  `-Action All` so the filter applies to all search actions.</span></span> 
    
    <span data-ttu-id="7bb92-191">콘텐츠 검색 작업의 목록에 대 한 [권한을 콘텐츠 검색에 대 한 필터링 구성에](permissions-filtering-for-content-search.md#new-compliancesecurityfilter)"New-ComplianceSecurityFilter" 섹션을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="7bb92-191">For a list of the Content Search actions, see the "New-ComplianceSecurityFilter" section in [Configure permissions filtering for Content Search](permissions-filtering-for-content-search.md#new-compliancesecurityfilter).</span></span>
    
<span data-ttu-id="7bb92-192">Contoso 준수 경계 시나리오를 지원 하기 위해 만든 두 검색 권한 필터의 예는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="7bb92-192">Here are examples of the two search permissions filters that would be created to support the Contoso compliance boundaries scenario.</span></span>
  
 <span data-ttu-id="7bb92-193">**Fourth Coffee**</span><span class="sxs-lookup"><span data-stu-id="7bb92-193">**Fourth Coffee**</span></span>

```
New-ComplianceSecurityFilter -FilterName "Fourth Coffee Security Filter" -Users "Fourth Coffee eDiscovery Managers", "Fourth Coffee Investigators" -Filters "Mailbox_Department -eq 'FourthCoffee'", "Site_ComplianceAttribute -eq 'FourthCoffee' -or Site_Path -like 'https://contoso.sharepoint.com/sites/FourthCoffee*'" -Action ALL
```
   
 <span data-ttu-id="7bb92-194">**Coho Winery**</span><span class="sxs-lookup"><span data-stu-id="7bb92-194">**Coho Winery**</span></span>

```
New-ComplianceSecurityFilter -FilterName "Coho Winery Security Filter" -Users "Coho Winery eDiscovery Managers", "Coho Winery Investigators" -Filters "Mailbox_Department -eq 'CohoWinery'", "Site_ComplianceAttribute -eq 'CohoWinery' -or Site_Path -like 'https://contoso.sharepoint.com/sites/CohoWinery*'" -Action ALL
```

## <a name="step-5-create-an-ediscovery-case-for-an-intra-agency-investigations"></a><span data-ttu-id="7bb92-195">5 단계: 내 기관 조사에 대 한 eDiscovery 사례 만들기</span><span class="sxs-lookup"><span data-stu-id="7bb92-195">Step 5: Create an eDiscovery case for an intra-agency investigations</span></span>

<span data-ttu-id="7bb92-p121">마지막 단계는 보안에서 새 eDiscovery 사례를 만들려면 &amp; 준수 센터 다음 역할 그룹을 추가 하 고-3 단계에서에서 만든-대/소문자의 구성원으로 합니다. 그 결과 준수 경계를 사용 하 여 중요 한 특징은 두 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7bb92-p121">The final step is to create a new eDiscovery case in the Security &amp; Compliance Center and then add the role group—that you created in Step 3—as a member of the case. This results in two important characteristics of using compliance boundaries:</span></span>
  
- <span data-ttu-id="7bb92-p122">대/소문자에 추가 하는 역할 그룹의 구성원을 참조 하 고 보안에서 대/소문자에 액세스할 수 있게 됩니다만 &amp; 준수 센터입니다. 예는 경우의 유일한 구성원 Fourth Coffee 수 사관 역할 그룹을 사용 하는 경우 다음 Fourth Coffee eDiscovery 관리자 역할 그룹 (또는 다른 역할 그룹의 구성원)의 구성원 수 없습니다를 표시 하거나 대/소문자에 액세스 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bb92-p122">Only members of the role group added to the case will be able to see and access the case in the Security &amp; Compliance Center. For example, if the Fourth Coffee Investigators role group is the only member of a case, then members of the Fourth Coffee eDiscovery Managers role group (or members of any other role group) won't be able to see or access the case.</span></span>
    
- <span data-ttu-id="7bb92-200">대/소문자와 연결 된 검색을 실행 하는 경우에 할당 된 역할 그룹의 구성원만 수 있습니다 (정의 된 4 단계에서에서 만든 검색 권한 필터에 의해.)가 기관 내에서 콘텐츠 위치를 검색할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7bb92-200">When a member of the role group assigned to a case runs a search associated with the case, they will only be able to search the content locations within their agency (which is defined by the search permissions filter that you created in Step 4.)</span></span>


<span data-ttu-id="7bb92-201">새 사례를 만들고 구성원을 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bb92-201">To create a new case and assign members:</span></span>
    
1. <span data-ttu-id="7bb92-202">보안에서 **eDiscovery** 페이지로 이동 &amp; 준수 센터 새 사례를 작성 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bb92-202">Go to the **eDiscovery** page in the Security &amp; Compliance Center and create a new case.</span></span> 
    
2. <span data-ttu-id="7bb92-203">EDiscovery 사례 목록에서 방금 만든 하는 경우의 이름을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bb92-203">In the list of eDiscovery cases, click the name of the case you just created.</span></span>
    
3. <span data-ttu-id="7bb92-204">**이 경우 관리** 플라이 아웃 페이지에서 **관리 역할 그룹**를 클릭 ![추가 아이콘](media/8ee52980-254b-440b-99a2-18d068de62d3.gif) **추가**합니다.</span><span class="sxs-lookup"><span data-stu-id="7bb92-204">In the **Manage this case** flyout page, under **Mange role groups**, click ![Add icon](media/8ee52980-254b-440b-99a2-18d068de62d3.gif) **Add**.</span></span>
    
    ![EDiscovery 사례의 구성원으로 역할 그룹을 추가 합니다.](media/f8b4b557-01b9-4388-85be-b5b5ab7c5629.png)
  
4. <span data-ttu-id="7bb92-206">역할 그룹 목록에서 3 단계에서에서 만든 역할 그룹 중 하나를 선택 하 고 **추가**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bb92-206">In the list of role groups, select one of the role groups that you created in Step 3, and click **Add**.</span></span>
    
5. <span data-ttu-id="7bb92-207">변경 내용을 저장 하려면 **이 경우 관리** 플라이 아웃에서 **저장** 을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bb92-207">Click **Save** on the **Manage this case** flyout to save the change.</span></span> 

## <a name="compliance-boundary-limitations"></a><span data-ttu-id="7bb92-208">규정 준수 경계 제한 사항</span><span class="sxs-lookup"><span data-stu-id="7bb92-208">Compliance boundary limitations</span></span>

<span data-ttu-id="7bb92-209">EDiscovery 사례 및 규정 준수 경계에 대 한 조사를 사용 하는 관리 하는 경우 다음과 같은 제한 사항이 염두에 두십시오.</span><span class="sxs-lookup"><span data-stu-id="7bb92-209">Keep the following limitations in mind when managing eDiscovery cases and investigations that use of compliance boundaries.</span></span>
  
- <span data-ttu-id="7bb92-p123">만들고 콘텐츠 검색을 실행 하는 경우에 사용자 기관 외부에 있는 콘텐츠 위치를 선택할 수 있습니다. 그러나 검색 권한 필터로 인해 해당 위치의 콘텐츠를에서 검색 결과에 포함 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7bb92-p123">When creating and running a Content Search, you can select content locations that are outside of your agency. However, because of the search permissions filter, content from those locations won't be included in the search results.</span></span>
    
- <span data-ttu-id="7bb92-p124">규정 준수 경계 eDiscovery 사례에서 보류에 적용 되지 않습니다. 즉, 하나의 기관에서 eDiscovery 관리자는 대기 다른 기관에서 사용자를 배치할 수 있습니다. 그러나 eDiscovery 관리자 보류에 추가 된 사용자의 콘텐츠 위치를 검색 하는 경우 준수 경계를 사용 하 여 적용 됩니다. EDiscovery 관리자는 의미 없습니다 수 검색 콘텐츠 위치는 사용자의 수에서 사용자를 배치할 수 있었던 경우에 유지 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bb92-p124">Compliance boundaries don't apply to holds in eDiscovery cases. That means an eDiscovery manager in one agency can place a user in a different agency on hold. However, the compliance boundary will be enforced if the eDiscovery manager searches the content locations of the user who was placed on hold. That means the eDiscovery manager won't be able search the user's content locations, even though they were able to place the user on hold.</span></span>
    
    <span data-ttu-id="7bb92-216">또한 통계 기관에서 콘텐츠 위치에만 적용 됩니다를 보관 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bb92-216">Additionally, hold statistics will only apply to content locations in the agency.</span></span>
    
- <span data-ttu-id="7bb92-217">검색 사용 권한 필터는 Exchange 공용 폴더에 적용 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7bb92-217">Search permissions filters aren't applied to Exchange public folders.</span></span>

## <a name="searching-and-exporting-content-in-multi-geo-environments"></a><span data-ttu-id="7bb92-218">다중-지리적으로 분산 환경에서 콘텐츠 검색 및 내보내기</span><span class="sxs-lookup"><span data-stu-id="7bb92-218">Searching and exporting content in Multi-Geo environments</span></span>

<span data-ttu-id="7bb92-219">검색 사용 권한 필터를 사용 하 내보내기에 대 한 콘텐츠 라우팅되 및 [SharePoint 다중-지리적으로 분산 환경](https://go.microsoft.com/fwlink/?linkid=860840)에서 SharePoint 사이트 및 OneDrive 계정을 검색할 때 검색할 수 있는 데이터 센터를 제어할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7bb92-219">Search permissions filters also let you control where content is routed for export and which datacenter can be searched when searching SharePoint sites and OneDrive accounts in a [SharePoint Multi-Geo environment](https://go.microsoft.com/fwlink/?linkid=860840):</span></span>
  
- <span data-ttu-id="7bb92-p125">특정 데이터 센터에서 검색 결과 내보냅니다. 즉, 하는 데이터 센터 위치에서 결과 내보낼 수는 검색을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7bb92-p125">Export search results from a specific data center. This means that you can specify the data center location that search results will be exported from.</span></span>
    
- <span data-ttu-id="7bb92-p126">SharePoint 사이트 및 위성 데이터 센터로 OneDrive 계정을의 경로 검색 합니다. 즉, 검색을 실행 하는 데이터 센터 위치를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7bb92-p126">Route searches of SharePoint sites and OneDrive accounts to a satellite data center. This means you can specify the data center location where searches will be run.</span></span>
    
<span data-ttu-id="7bb92-224">**새로 만들기 ComplianceSecurityFilter** 또는 **집합 ComplianceSecurityFilter** cmdlet에 대 한 **Region** 매개 변수를 사용 하 여 만들거나 내보내기 라우팅될 수 있는 데이터 센터를 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bb92-224">Use the **Region** parameter for **New-ComplianceSecurityFilter** or **Set-ComplianceSecurityFilter** cmdlets to create or change which datacenter the export will be routed through.</span></span>
  
|<span data-ttu-id="7bb92-225">**매개 변수 값**</span><span class="sxs-lookup"><span data-stu-id="7bb92-225">**Parameter value**</span></span>|<span data-ttu-id="7bb92-226">**데이터 센터 위치**</span><span class="sxs-lookup"><span data-stu-id="7bb92-226">**Data center location**</span></span>|
|:-----|:-----|
|<span data-ttu-id="7bb92-227">NAM</span><span class="sxs-lookup"><span data-stu-id="7bb92-227">NAM</span></span>  <br/> |<span data-ttu-id="7bb92-228">북미 (실제 데이터 센터는 미국)</span><span class="sxs-lookup"><span data-stu-id="7bb92-228">North American (actual data centers are in the US)</span></span>  <br/> |
|<span data-ttu-id="7bb92-229">EUR</span><span class="sxs-lookup"><span data-stu-id="7bb92-229">EUR</span></span>  <br/> |<span data-ttu-id="7bb92-230">유럽</span><span class="sxs-lookup"><span data-stu-id="7bb92-230">Europe</span></span>  <br/> |
|<span data-ttu-id="7bb92-231">APC</span><span class="sxs-lookup"><span data-stu-id="7bb92-231">APC</span></span>  <br/> |<span data-ttu-id="7bb92-232">아시아 태평양</span><span class="sxs-lookup"><span data-stu-id="7bb92-232">Asia Pacific</span></span>  <br/> |
|<span data-ttu-id="7bb92-233">CAN</span><span class="sxs-lookup"><span data-stu-id="7bb92-233">CAN</span></span> <br/> |<span data-ttu-id="7bb92-234">캐나다</span><span class="sxs-lookup"><span data-stu-id="7bb92-234">Canada</span></span>
   
<span data-ttu-id="7bb92-p127">마찬가지로, SharePoint 및 OneDrive 위치를 검색 하는 경우 콘텐츠 검색에서 실행 되는 데이터 센터를 제어 하는 **지역** 매개 변수 값에 대 한 다음 값을 사용할 수 있습니다. 다음 표에서 내보내기 라우팅될 수 있는 데이터 센터를 표시 하는 note 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bb92-p127">Similarly, you can use the following values for the **Region** parameter values to control which data center that Content Searches will run in when searching SharePoint and OneDrive locations. Note that the following table also shows which data center exports will be routed through.</span></span> 
  
|<span data-ttu-id="7bb92-237">**매개 변수 값**</span><span class="sxs-lookup"><span data-stu-id="7bb92-237">**Parameter value**</span></span>|<span data-ttu-id="7bb92-238">**데이터 센터 내보내기에 대 한 라우팅 위치**</span><span class="sxs-lookup"><span data-stu-id="7bb92-238">**Data center routing locations for export**</span></span>|
|:-----|:-----|
|<span data-ttu-id="7bb92-239">NAM</span><span class="sxs-lookup"><span data-stu-id="7bb92-239">NAM</span></span>  <br/> |<span data-ttu-id="7bb92-240">US</span><span class="sxs-lookup"><span data-stu-id="7bb92-240">US</span></span>  <br/> |
|<span data-ttu-id="7bb92-241">EUR</span><span class="sxs-lookup"><span data-stu-id="7bb92-241">EUR</span></span>  <br/> |<span data-ttu-id="7bb92-242">유럽</span><span class="sxs-lookup"><span data-stu-id="7bb92-242">Europe</span></span>  <br/> |
|<span data-ttu-id="7bb92-243">APC</span><span class="sxs-lookup"><span data-stu-id="7bb92-243">APC</span></span>  <br/> |<span data-ttu-id="7bb92-244">아시아 태평양</span><span class="sxs-lookup"><span data-stu-id="7bb92-244">Asia Pacific</span></span>  <br/> |
|<span data-ttu-id="7bb92-245">CAN</span><span class="sxs-lookup"><span data-stu-id="7bb92-245">CAN</span></span>  <br/> |<span data-ttu-id="7bb92-246">US</span><span class="sxs-lookup"><span data-stu-id="7bb92-246">US</span></span>  <br/> |
|<span data-ttu-id="7bb92-247">AUS</span><span class="sxs-lookup"><span data-stu-id="7bb92-247">AUS</span></span>  <br/> |<span data-ttu-id="7bb92-248">아시아 태평양</span><span class="sxs-lookup"><span data-stu-id="7bb92-248">Asia Pacific</span></span>  <br/> |
|<span data-ttu-id="7bb92-249">KOR</span><span class="sxs-lookup"><span data-stu-id="7bb92-249">KOR</span></span>  <br/> |<span data-ttu-id="7bb92-250">조직의 기본 데이터 센터</span><span class="sxs-lookup"><span data-stu-id="7bb92-250">The organization's default data center</span></span>  <br/> |
|<span data-ttu-id="7bb92-251">GBR</span><span class="sxs-lookup"><span data-stu-id="7bb92-251">GBR</span></span>  <br/> |<span data-ttu-id="7bb92-252">유럽</span><span class="sxs-lookup"><span data-stu-id="7bb92-252">Europe</span></span>  <br/> |
|<span data-ttu-id="7bb92-253">JPN</span><span class="sxs-lookup"><span data-stu-id="7bb92-253">JPN</span></span>  <br/> |<span data-ttu-id="7bb92-254">아시아 태평양</span><span class="sxs-lookup"><span data-stu-id="7bb92-254">Asia Pacific</span></span>  <br/> |
|<span data-ttu-id="7bb92-255">찾기</span><span class="sxs-lookup"><span data-stu-id="7bb92-255">IND</span></span>  <br/> |<span data-ttu-id="7bb92-256">아시아 태평양</span><span class="sxs-lookup"><span data-stu-id="7bb92-256">Asia Pacific</span></span>  <br/> |
|<span data-ttu-id="7bb92-257">LAM</span><span class="sxs-lookup"><span data-stu-id="7bb92-257">LAM</span></span>  <br/> |<span data-ttu-id="7bb92-258">US</span><span class="sxs-lookup"><span data-stu-id="7bb92-258">US</span></span>  <br/> |
   
 <span data-ttu-id="7bb92-259">**참고:** 검색 사용 권한 필터에 대 한 Region 매개 변수를 지정 하지 않으면 조직 기본 SharePoint 지역은 검색할 한 다음 검색 결과 가장 가까운 데이터 센터에 내보내집니다.</span><span class="sxs-lookup"><span data-stu-id="7bb92-259">**Note:** If you don't specify the Region parameter for a search permissions filter, the organizations default SharePoint region will be searched, then search results are exported to the closest data center.</span></span> 
  
<span data-ttu-id="7bb92-p128">다음은 예를 사용 하는 **-지역** 준수 경계에 대 한 검색 권한 필터를 만들 때 매개 변수입니다. 이 Fourth Coffee 자회사 북미에 있고 Coho Winery 유럽의 인지 가정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bb92-p128">Here are examples of using the **-Region** parameter when creating search permission filters for compliance boundaries. This assumes that the Fourth Coffee subsidiary is located in North America and that Coho Winery is in Europe.</span></span> 
  
```
New-ComplianceSecurityFilter -FilterName "Fourth Coffee Security Filter" -Users "Fourth Coffee eDiscovery Managers", "Fourth Coffee Investigators" -Filters "Mailbox_Department -eq 'FourthCoffee'", "Site_Department -eq 'FourthCoffee' -or Site_Path -like 'https://contoso.sharepoint.com/sites/FourthCoffee*'" -Action ALL -Region NAM
```

```
New-ComplianceSecurityFilter -FilterName "Coho Winery Security Filter" -Users "Coho Winery eDiscovery Managers", "Coho Winery Investigators" -Filters "Mailbox_Department -eq 'CohoWinery'", "Site_Department -eq 'CohoWinery' -or Site_Path -like 'https://contoso.sharepoint.com/sites/CohoWinery*'" -Action ALL -Region EUR
```
   
<span data-ttu-id="7bb92-262">다중-지리적으로 분산 환경에서 콘텐츠를 검색할 때 유의 및 내보내기 (영문)에서 다음 작업을 유지 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bb92-262">Keep the following things in mind when searching and exporting content in multi-geo environments.</span></span>
  
- <span data-ttu-id="7bb92-p129">**Region** 매개 변수는 Exchange 사서함, 검색을 제어 하지 않습니다. 사서함을 검색 하는 경우 모든 데이터 센터를 검색 합니다. exchange 사서함을 검색할 수 범위를 제한 하는, 만들기 (영문) 또는 사용 권한 필요한 검색 필터를 변경 하는 경우 **필터** 매개 변수를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bb92-p129">The **Region** parameter doesn't control searches of Exchange mailboxes; all data centers will be searched when you search mailboxes. To limit the scope of which Exchange mailboxes can be searched, use the **Filters** parameter when creating or changing a search permissions filter.</span></span> 
    
- <span data-ttu-id="7bb92-265">대체 영역을 지정 하는 검색 권한 필터에서 해당 eDiscovery에 대 한 다른 사용자 계정을 사용할 수 있는 관리자를 만드는 해야 eDiscovery 여러 SharePoint 지역에서 검색 하는 관리자에 대 한 필요한 경우 위치는 SharePoint 사이트 또는 OneDrive 계정은 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7bb92-265">If it's necessary for an eDiscovery Manager to search across multiple SharePoint regions, you'll need to create a different user account for that eDiscovery manager that can be used in the search permissions filter to specify the alternate region where the SharePoint sites or OneDrive accounts are located.</span></span>
    
- <span data-ttu-id="7bb92-p130">**Region** 매개 변수 중 하나를 주 검색에 지시 SharePoint와 OneDrive의 콘텐츠를 검색할 때 또는 위성 eDiscovery 관리자는 eDiscovery 조사를 수행 하는 위치입니다. EDiscovery 관리자 검색 권한 필터에 지정 된 영역 외부의 OneDrive 및 SharePoint 사이트를 검색 하는 경우 검색 결과가 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7bb92-p130">When searching for content in SharePoint and OneDrive, the **Region** parameter directs searches to either the main or satellite location where the eDiscovery manager will conduct eDiscovery investigations. If an eDiscovery manager searches SharePoint and OneDrive sites outside of the region that's specified in the search permissions filter, no search results will be returned.</span></span> 
    
- <span data-ttu-id="7bb92-p131">Azure 저장소 위치에 (Exchange, Skype 비즈니스, SharePoint, onedrive 및 콘텐츠 검색 도구를 사용 하 여 검색할 수 있는 다른 Office 365 서비스 포함) 하는 모든 콘텐츠 위치에서 콘텐츠를 업로드 한가 검색 결과 내보낼 때의 **지역** 매개 변수에 의해 지정 된 데이터 센터입니다. 이렇게 하면 조직이 제어 테두리 간에 내보낼 콘텐츠를 허용 하지 않도록 규정 준수를 벗어나지 있습니다. 없는 지역 검색 권한 필터에 지정 하 고 하는 경우 조직의 기본 영역에 콘텐츠 업로드 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7bb92-p131">When exporting search results, content from all content locations (including Exchange, Skype for Business, SharePoint, OneDrive and other Office 365 services that you can search by using the Content Search tool) will be uploaded to the Azure storage location in the data center that's specified by the **Region** parameter. This helps organizations stay within compliance by not allowing content to be exported across controlled borders. If no region is specified in the search permissions filter, content is uploaded to the organization's default region.</span></span> 
    
- <span data-ttu-id="7bb92-271">추가 또는 다음 명령을 실행 하 여 영역을 변경 하 여 기존 검색 권한 필터를 편집할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7bb92-271">You can edit an existing search permissions filter to add or change the region by running the following command:</span></span>

    ```
    Set-ComplianceSecurityFilter -FilterName <Filter name>  -Region <Region>
    ```
 
## <a name="frequently-asked-questions"></a><span data-ttu-id="7bb92-272">자주 묻는 질문</span><span class="sxs-lookup"><span data-stu-id="7bb92-272">Frequently asked questions</span></span>

 <span data-ttu-id="7bb92-273">**사용자 만들고 관리할 수 있습니다 (New ComplianceSecurityFilter 및 집합 ComplianceSecurityFilter cmdlet을 사용 하 여) 검색 권한 필터?**</span><span class="sxs-lookup"><span data-stu-id="7bb92-273">**Who can create and manage search permissions filters (using New-ComplianceSecurityFilter and Set-ComplianceSecurityFilter cmdlets )?**</span></span>
  
<span data-ttu-id="7bb92-274">만들 보기 및 검색 권한 필터를 수정, 보안에서 조직 관리 역할 그룹의 구성원 이어야 하는 &amp; 준수 센터입니다.</span><span class="sxs-lookup"><span data-stu-id="7bb92-274">To create, view and modify search permissions filters, you have to be a member of the Organization Management role group in the Security &amp; Compliance Center.</span></span>
  
 <span data-ttu-id="7bb92-275">**EDiscovery 관리자는 여러 기관에 걸쳐 있는 둘 이상의 역할 그룹에 할당 되 면 검색 하려면 어떻게은 하나의 기관에서 콘텐츠 또는 다른?**</span><span class="sxs-lookup"><span data-stu-id="7bb92-275">**If an eDiscovery manager is assigned to more than one role group that spans multiple agencies, how do they search for content in one agency or the other?**</span></span>
  
<span data-ttu-id="7bb92-p132">EDiscovery 관리자는 특정 기관에는 검색을 제한 하는 해당 검색 쿼리를 매개 변수를 추가할 수 있습니다. 예, **CustomAttribute10** 속성 기관을 구분할 수를 지정 하는 조직 자신이에 추가할 수 다음 특정 기관에서 사서함 및 OneDrive 계정을 검색 하는 검색 쿼리: `CustomAttribute10:<value> AND Site_ComplianceAttribute:<value>`합니다.</span><span class="sxs-lookup"><span data-stu-id="7bb92-p132">The eDiscovery manager can add parameters to their search query that will restrict the search to a specific agency. For example, if an organization has specified the **CustomAttribute10** property to differentiate agencies, they can append the following to their search query to search mailboxes and OneDrive accounts in a specific agency:  `CustomAttribute10:<value> AND Site_ComplianceAttribute:<value>`.</span></span>
  
 <span data-ttu-id="7bb92-278">**검색 사용 권한 필터에 준수 특성으로 사용 되는 특성의 값이 변경 하면 어떻게 됩니까?**</span><span class="sxs-lookup"><span data-stu-id="7bb92-278">**What happens if the value of the attribute that's used as the compliance attribute in a search permissions filter is changed?**</span></span>
  
<span data-ttu-id="7bb92-p133">필터에 사용 되는 특성의 값이 변경 되는 경우 준수 경계를 적용 하는 검색 사용 권한 필터에 대 한 최대 3 일 걸립니다. 예, Contoso 시나리오에서 가정해 보겠습니다 Fourth Coffee 기관에서 사용자는 Coho Winery 기관 전송 됩니다. 따라서 *FourthCoffee* 에서 사용자 개체의 **부서** 특성의 값은 *CohoWinery* 로 변경 됩니다. 이 상황에서는 Fourth Coffee eDiscovery 및 투자자 특성이 변경 된 후에 3 일을에 대 한 해당 사용자에 대 한 검색 결과 얻을 수 있습니다. 마찬가지로, Coho Winery eDiscovery 관리자 하기 전에 최대 3 일 하는 것과 수 사관 사용자에 대 한 검색 결과 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7bb92-p133">It takes up to 3 days for a search permissions filter to enforce the compliance boundary if the value of the attribute that's used in the filter is changed. For example, in the Contoso scenario let's say that a user in the Fourth Coffee agency is transferred to the Coho Winery agency. As a result, the value of the **Department** attribute on the user object is changed from  *FourthCoffee*  to  *CohoWinery*  . In this situation, Fourth Coffee eDiscovery and investors will get search results for that user for up 3 days after the attribute is changed. Similarly, it will take up to 3 days before Coho Winery eDiscovery managers and investigators will get search results for the user.</span></span> 
  
 <span data-ttu-id="7bb92-284">**EDiscovery 관리자 두 별도 준수 경계에서 콘텐츠를 볼 수 있습니까?**</span><span class="sxs-lookup"><span data-stu-id="7bb92-284">**Can an eDiscovery manager see content from two separate compliance boundaries?**</span></span>
  
<span data-ttu-id="7bb92-p134">예입니다. 이 두 기관에 대 한 가시성을 포함 하는 역할 그룹에 사용자를 추가 하 여 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7bb92-p134">Yes. This can be done by adding the user to role groups that have visibility to both agencies.</span></span>
  
 <span data-ttu-id="7bb92-287">**EDiscovery 사례 보류, Office 365 보존 정책 또는 DLP에 대 한 사용 권한 필터 작업을 검색 하려면?**</span><span class="sxs-lookup"><span data-stu-id="7bb92-287">**Do search permissions filters work for eDiscovery case holds, Office 365 retention policies, or DLP?**</span></span>
  
<span data-ttu-id="7bb92-288">이 이번에는 아니오</span><span class="sxs-lookup"><span data-stu-id="7bb92-288">No, not at this time</span></span>
  
 <span data-ttu-id="7bb92-289">**콘텐츠를 내보낸 하지만 해당 영역에 SharePoint 조직 없는 위치를 제어 하는 영역을 지정 하는 경우 여전히 검색 합니까 SharePoint?**</span><span class="sxs-lookup"><span data-stu-id="7bb92-289">**If I specify a region to control where content is exported, but I don't have a SharePoint organization in that region, can I still search SharePoint?**</span></span>
  
<span data-ttu-id="7bb92-290">조직에서 검색 권한 필터에 지정 된 지역 없으면 기본 영역을 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bb92-290">If the region specified in the search permissions filter doesn't exist in your organization, the default region will be searched.</span></span>
  
 <span data-ttu-id="7bb92-291">**조직 내에서 만들 수 있는 검색 권한 필터의 최대 수는 무엇입니까?**</span><span class="sxs-lookup"><span data-stu-id="7bb92-291">**What is the maximum number of search permissions filters that can be created in an organization?**</span></span>
  
<span data-ttu-id="7bb92-p135">조직 내에서 만들 수 있는 검색 권한 필터의 수에 제한이 없습니다. 그러나 검색 성능 영향을 미칩니다 100 개가 넘는 검색 권한 필터 했으면 합니다. 조직에서 검색 권한 필터의 수를 가능한 한 작게 유지 하려면 Exchange, SharePoint 및 OneDrive에 대 한 규칙 가능 하면 항상 하나의 검색 권한 필터를 결합 하는 필터를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="7bb92-p135">There is no limit to the number of search permissions filters that can be created in an organization. However, search performance will be impacted when there are more than 100 search permissions filters. To keep the number of search permissions filters in your organization as small as possible, create filters that combine rules for Exchange, SharePoint, and OneDrive into a single search permissions filter whenever possible.</span></span>
