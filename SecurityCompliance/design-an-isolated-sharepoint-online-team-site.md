---
title: 격리된 SharePoint Online 팀 사이트 디자인
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
ms.date: 12/15/2017
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.collection: Ent_O365
ms.custom: Ent_Solutions
ms.assetid: 775a4e9e-3135-4a48-b32f-bbdd9f2bd0aa
description: '요약: 격리 된 SharePoint Online 팀 사이트에 대 한 디자인 프로세스를 단계별로 안내 합니다.'
ms.openlocfilehash: 04634052354de47a09aa3b13e2c82d97be22f4d2
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/17/2019
ms.locfileid: "34150320"
---
# <a name="design-an-isolated-sharepoint-online-team-site"></a><span data-ttu-id="6b656-103">격리된 SharePoint Online 팀 사이트 디자인</span><span class="sxs-lookup"><span data-stu-id="6b656-103">Design an isolated SharePoint Online team site</span></span>

 <span data-ttu-id="6b656-104">**요약:** 격리 된 SharePoint Online 팀 사이트에 대 한 디자인 프로세스를 단계별로 안내 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b656-104">**Summary:** Step through the design process for isolated SharePoint Online team sites.</span></span>
  
<span data-ttu-id="6b656-105">이 문서에서는 격리 된 SharePoint Online 팀 사이트를 만들기 전에 수행 해야 하는 주요 디자인 결정 사항에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b656-105">This article takes you through the key design decisions you must make before creating an isolated SharePoint Online team site.</span></span>
  
## <a name="phase-1-determine-your-sharepoint-groups-and-permission-levels"></a><span data-ttu-id="6b656-106">1 단계: SharePoint 그룹 및 권한 수준 결정</span><span class="sxs-lookup"><span data-stu-id="6b656-106">Phase 1: Determine your SharePoint groups and permission levels</span></span>

<span data-ttu-id="6b656-107">모든 SharePoint Online 팀 사이트는 기본적으로 다음과 같은 SharePoint 그룹을 사용 하 여 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="6b656-107">Every SharePoint Online team site by default is created with the following SharePoint groups:</span></span>
  
- <span data-ttu-id="6b656-108">\<사이트 name> 구성원</span><span class="sxs-lookup"><span data-stu-id="6b656-108">\<site name> Members</span></span>
    
- <span data-ttu-id="6b656-109">\<사이트 name> 방문자</span><span class="sxs-lookup"><span data-stu-id="6b656-109">\<site name> Visitors</span></span>
    
- <span data-ttu-id="6b656-110">\<사이트 name> 소유자</span><span class="sxs-lookup"><span data-stu-id="6b656-110">\<site name> Owners</span></span>
    
<span data-ttu-id="6b656-111">이러한 그룹은 Office 365 및 Azure Active Directory (AD) 그룹과는 별개 이며 사이트의 리소스에 대 한 사용 권한을 할당 하기 위한 기본이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6b656-111">These groups are separate from Office 365 and Azure Active Directory (AD) groups and are the basis for assigning permissions for the resources of the site.</span></span>
  
<span data-ttu-id="6b656-112">SharePoint 그룹의 구성원이 사이트에서 수행할 수 있는 작업을 결정 하는 특정 사용 권한 집합은 사용 권한 수준입니다.</span><span class="sxs-lookup"><span data-stu-id="6b656-112">The set of specific permissions that determines what a member of a SharePoint group can do in a site is a permission level.</span></span> <span data-ttu-id="6b656-113">SharePoint Online 팀 사이트에 대 한 세 가지 사용 권한 수준에는 기본적으로 편집, 읽기 및 모든 권한이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6b656-113">There are three permission levels by default for a SharePoint Online team site: Edit, Read, and Full control.</span></span> <span data-ttu-id="6b656-114">다음 표에서는 SharePoint 그룹 및 할당 된 사용 권한 수준에 대 한 기본 상관 관계를 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="6b656-114">The following table shows the default correlation of SharePoint groups and assigned permission levels:</span></span>
  
|<span data-ttu-id="6b656-115">**SharePoint 그룹**</span><span class="sxs-lookup"><span data-stu-id="6b656-115">**SharePoint group**</span></span>|<span data-ttu-id="6b656-116">**권한 수준**</span><span class="sxs-lookup"><span data-stu-id="6b656-116">**Permission level**</span></span>|
|:-----|:-----|
|<span data-ttu-id="6b656-117">\<사이트 name> 구성원</span><span class="sxs-lookup"><span data-stu-id="6b656-117">\<site name> Members</span></span>  <br/> |<span data-ttu-id="6b656-118">편집</span><span class="sxs-lookup"><span data-stu-id="6b656-118">Edit</span></span>  <br/> |
|<span data-ttu-id="6b656-119">\<사이트 name> 방문자</span><span class="sxs-lookup"><span data-stu-id="6b656-119">\<site name> Visitors</span></span>  <br/> |<span data-ttu-id="6b656-120">읽기</span><span class="sxs-lookup"><span data-stu-id="6b656-120">Read</span></span>  <br/> |
|<span data-ttu-id="6b656-121">\<사이트 name> 소유자</span><span class="sxs-lookup"><span data-stu-id="6b656-121">\<site name> Owners</span></span>  <br/> |<span data-ttu-id="6b656-122">모든 권한</span><span class="sxs-lookup"><span data-stu-id="6b656-122">Full control</span></span>  <br/> |
   
 <span data-ttu-id="6b656-123">**모범 사례:** 추가 SharePoint 그룹 및 권한 수준을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6b656-123">**Best practice:** You can create additional SharePoint groups and permission levels.</span></span> <span data-ttu-id="6b656-124">그러나 격리 된 SharePoint Online 사이트에 대 한 기본 SharePoint 그룹 및 사용 권한 수준을 사용 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="6b656-124">However, we recommend using the default SharePoint groups and permission levels for your isolated SharePoint Online site.</span></span>
  
<span data-ttu-id="6b656-125">다음은 기본 SharePoint 그룹 및 사용 권한 수준입니다.</span><span class="sxs-lookup"><span data-stu-id="6b656-125">Here are the default SharePoint groups and permission levels.</span></span>
  
![SharePoint Online 사이트에 대 한 기본 SharePoint 그룹 및 사용 권한 수준입니다.](media/3f892ab4-6479-42f0-a505-1ba0ef94b9c6.png)
  
## <a name="phase-2-assign-permissions-to-users-with-access-groups"></a><span data-ttu-id="6b656-127">2 단계: 액세스 그룹을 사용 하 여 사용자에 게 사용 권한 할당</span><span class="sxs-lookup"><span data-stu-id="6b656-127">Phase 2: Assign permissions to users with access groups</span></span>

<span data-ttu-id="6b656-128">사용자 계정이 구성원으로 속해 있는 Office 365 또는 Azure AD 그룹을 SharePoint 그룹에 추가 하는 방식으로 사용자에 게 사용 권한을 할당할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6b656-128">You can assign permissions to users by adding their user account, or an Office 365 or Azure AD group of which the user account is a member, to the SharePoint groups.</span></span> <span data-ttu-id="6b656-129">Office 365 또는 Azure AD 그룹의 멤버 자격을 통해 직접 또는 간접적으로 Office 365 사용자 계정을 추가한 후에는 SharePoint 그룹과 연결 된 사용 권한 수준에 할당 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6b656-129">Once added, the Office 365 user accounts, either directly or indirectly via membership in an Office 365 or Azure AD group, are assigned the permission level associated with the SharePoint group.</span></span>
  
<span data-ttu-id="6b656-130">기본 SharePoint 그룹을 예로 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b656-130">Using the default SharePoint groups as an example:</span></span>
  
- <span data-ttu-id="6b656-131">사용자 계정 및 그룹을 모두 포함할 수 있는 \*\* \<site name> members\*\* SharePoint 그룹의 구성원에 게는 **편집** 권한 수준이 할당 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6b656-131">Members of the **\<site name> Members** SharePoint group, which can include both user accounts and groups, are assigned the **Edit** permission level</span></span>
    
- <span data-ttu-id="6b656-132">사용자 계정 및 그룹을 모두 포함할 수 있는 \*\* \<사이트 name> 방문자\*\* SharePoint 그룹의 구성원에 게는 **읽기** 권한 수준이 할당 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6b656-132">Members of the **\<site name> Visitors** SharePoint group, which can include both user accounts and groups, are assigned the **Read** permission level</span></span>
    
- <span data-ttu-id="6b656-133">사용자 계정 및 그룹을 모두 포함할 수 있는 \*\* \<site name>\*\* owner SharePoint 그룹의 구성원에 게는 **모든** 권한 수준이 할당 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6b656-133">Members of the **\<site name> Owners** SharePoint group, which can include both user accounts and groups, are assigned the **Full control** permission level</span></span>
    
 <span data-ttu-id="6b656-134">**모범 사례:** 개별 사용자 계정을 통해 사용 권한을 관리할 수는 있지만 대신 액세스 그룹 이라고 하는 단일 Azure AD 그룹을 사용 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="6b656-134">**Best practice:** Although you can manage permissions through individual user accounts, we recommend that you use a single Azure AD group, known as an access group, instead.</span></span> <span data-ttu-id="6b656-135">이를 통해 각 SharePoint 그룹의 사용자 계정 목록을 관리 하는 것이 아니라 액세스 그룹의 구성원을 통해 사용 권한을 쉽게 관리할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6b656-135">This simplifies the management of permissions through membership in the access group, rather than managing the list of user accounts for each SharePoint group.</span></span>
  
<span data-ttu-id="6b656-136">Office 365의 Azure AD 그룹은 Office 365 그룹과는 다릅니다.</span><span class="sxs-lookup"><span data-stu-id="6b656-136">Azure AD groups for Office 365 are different than Office 365 groups.</span></span> <span data-ttu-id="6b656-137">Azure AD 그룹은 해당 **유형이** **보안** 으로 설정 되 고 전자 메일 주소가 없는 Office 관리 센터에 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6b656-137">Azure AD groups appear in the Office Admin center with their **Type** set to **Security** and do not have an email address.</span></span> <span data-ttu-id="6b656-138">Azure AD 그룹은 다음 내에서 관리할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6b656-138">Azure AD groups can be managed within:</span></span>
  
- <span data-ttu-id="6b656-139">Windows Server Active Directory (AD)</span><span class="sxs-lookup"><span data-stu-id="6b656-139">Windows Server Active Directory (AD)</span></span>
    
    <span data-ttu-id="6b656-140">온-프레미스 Windows Server AD 인프라에 만들어져 Office 365 구독과 동기화 된 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="6b656-140">These are groups that have been created in your on-premises Windows Server AD infrastructure and synchronized to your Office 365 subscription.</span></span> <span data-ttu-id="6b656-141">Office 관리 센터에서 이러한 그룹의 **상태** 는 **Active directory와 동기화**되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6b656-141">In the Office Admin center, these groups have a **Status** of **Synched with active directory**.</span></span>
    
- <span data-ttu-id="6b656-142">Office 365</span><span class="sxs-lookup"><span data-stu-id="6b656-142">Office 365</span></span>
    
    <span data-ttu-id="6b656-143">Office 관리 센터, Azure portal 또는 Microsoft PowerShell 중 하나를 사용 하 여 만든 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="6b656-143">These are groups that have been created using either the Office Admin center, the Azure portal, or Microsoft PowerShell.</span></span> <span data-ttu-id="6b656-144">Office 관리 센터에서 이러한 그룹의 **상태** 는 **Cloud**입니다.</span><span class="sxs-lookup"><span data-stu-id="6b656-144">In the Office Admin center, these groups have a **Status** of **Cloud**.</span></span>
    
 <span data-ttu-id="6b656-145">**모범 사례:** Windows Server AD 온-프레미스를 사용 중이 고 Office 365 구독과 동기화 하는 경우 Windows Server AD에서 사용자 및 그룹 관리를 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b656-145">**Best practice:** If you are using Windows Server AD on-premises and synchronizing with your Office 365 subscription, perform your user and group management with Windows Server AD.</span></span>
  
<span data-ttu-id="6b656-146">격리 된 SharePoint Online 팀 사이트의 경우 권장 되는 그룹 구조는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="6b656-146">For isolated SharePoint Online team sites, the recommended group structure looks like this:</span></span>
  
|<span data-ttu-id="6b656-147">**SharePoint 그룹**</span><span class="sxs-lookup"><span data-stu-id="6b656-147">**SharePoint group**</span></span>|<span data-ttu-id="6b656-148">**Azure AD 기반 액세스 그룹**</span><span class="sxs-lookup"><span data-stu-id="6b656-148">**Azure AD-based access group**</span></span>|<span data-ttu-id="6b656-149">**권한 수준**</span><span class="sxs-lookup"><span data-stu-id="6b656-149">**Permission level**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="6b656-150">\<사이트 name> 구성원</span><span class="sxs-lookup"><span data-stu-id="6b656-150">\<site name> Members</span></span>  <br/> |<span data-ttu-id="6b656-151">\<사이트 name> 구성원</span><span class="sxs-lookup"><span data-stu-id="6b656-151">\<site name> Members</span></span>  <br/> |<span data-ttu-id="6b656-152">편집</span><span class="sxs-lookup"><span data-stu-id="6b656-152">Edit</span></span>  <br/> |
|<span data-ttu-id="6b656-153">\<사이트 name> 방문자</span><span class="sxs-lookup"><span data-stu-id="6b656-153">\<site name> Visitors</span></span>  <br/> |<span data-ttu-id="6b656-154">\<사이트 name> 뷰어</span><span class="sxs-lookup"><span data-stu-id="6b656-154">\<site name> Viewers</span></span>  <br/> |<span data-ttu-id="6b656-155">읽기</span><span class="sxs-lookup"><span data-stu-id="6b656-155">Read</span></span>  <br/> |
|<span data-ttu-id="6b656-156">\<사이트 name> 소유자</span><span class="sxs-lookup"><span data-stu-id="6b656-156">\<site name> Owners</span></span>  <br/> |<span data-ttu-id="6b656-157">\<사이트 name> 관리자</span><span class="sxs-lookup"><span data-stu-id="6b656-157">\<site name> Admins</span></span>  <br/> |<span data-ttu-id="6b656-158">모든 권한</span><span class="sxs-lookup"><span data-stu-id="6b656-158">Full control</span></span>  <br/> |
   
 <span data-ttu-id="6b656-159">**모범 사례:** Office 365 또는 Azure AD 그룹을 SharePoint 그룹의 구성원으로 사용할 수는 있지만 Azure AD 그룹을 사용 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="6b656-159">**Best practice:** Although you can use either Office 365 or Azure AD groups as members of SharePoint groups, we recommend that you use Azure AD groups.</span></span> <span data-ttu-id="6b656-160">Windows Server AD 또는 Office 365를 통해 관리 되는 Azure AD 그룹은 중첩 된 그룹을 보다 유연 하 게 사용 하 여 사용 권한을 할당할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6b656-160">Azure AD groups, managed either through Windows Server AD or Office 365, give you more flexibility to use nested groups to assign permissions.</span></span>
  
<span data-ttu-id="6b656-161">Azure AD 기반 액세스 그룹을 사용 하도록 구성 된 기본 SharePoint 그룹은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="6b656-161">Here are the default SharePoint groups configured to use Azure AD-based access groups.</span></span>
  
![Access 그룹을 기본 SharePoint Online 사이트 그룹의 구성원으로 사용 합니다.](media/50a76328-ae69-483e-9029-ac4e7357b5ef.png)
  
<span data-ttu-id="6b656-163">세 개의 액세스 그룹을 디자인할 때는 다음 사항을 염두에 두어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b656-163">When designing the three access groups, keep the following in mind:</span></span>
  
- <span data-ttu-id="6b656-164">팀 사이트를 관리 하는 소수의 SharePoint Online 관리자에 게 해당 하는 \*\* \<사이트 name> Admins\*\* 액세스 그룹의 구성원은 몇 명만 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b656-164">There should be only a few members in the **\<site name> Admins** access group, corresponding to a small number of SharePoint Online administrators who are managing the team site.</span></span>
    
- <span data-ttu-id="6b656-165">대부분의 사이트 구성원은 \*\* \<사이트 name> members\*\* 또는 \*\* \<site name> viewer\*\* 액세스 그룹에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6b656-165">Most of your site members are in the **\<site name> Members** or **\<site name> Viewers** access groups.</span></span> <span data-ttu-id="6b656-166">Site \*\* \<name> members\*\* 액세스 그룹의 사이트 구성원은 사이트의 리소스를 삭제 하거나 수정할 수 있기 때문에 멤버 자격을 신중 하 게 고려해 야 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b656-166">Because site members in the **\<site name> Members** access group have the ability to delete or modify resources in the site, carefully consider its membership.</span></span> <span data-ttu-id="6b656-167">확실 하지 않은 경우 사이트 구성원을 \*\* \<사이트 name> viewer\*\* 액세스 그룹에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b656-167">When in doubt, add the site member to the **\<site name> Viewers** access group.</span></span>
    
<span data-ttu-id="6b656-168">다음은 ProjectX 라는 격리 된 사이트에 대 한 SharePoint 그룹 및 액세스 그룹의 예입니다.</span><span class="sxs-lookup"><span data-stu-id="6b656-168">Here is an example of the SharePoint groups and access groups for an isolated site named ProjectX.</span></span>
  
![ProjectX 라는 SharePoint Online 사이트에 대 한 액세스 그룹을 사용 하는 방법의 예입니다.](media/13afe542-9ffd-4671-9f48-210a0e2a502a.png)
  
## <a name="phase-3-use-nested-azure-ad-groups"></a><span data-ttu-id="6b656-170">3 단계: 중첩 된 Azure AD 그룹 사용</span><span class="sxs-lookup"><span data-stu-id="6b656-170">Phase 3: Use nested Azure AD groups</span></span>

<span data-ttu-id="6b656-171">소수의 사용자로 한정 된 프로젝트의 경우 사이트의 SharePoint 그룹에 추가 되는 단일 수준의 Azure AD 기반 액세스 그룹이 대부분의 시나리오에 적합 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b656-171">For a project confined to a small number of people, a single level of Azure AD-based access groups added to the SharePoint groups of the site will fit most scenarios.</span></span> <span data-ttu-id="6b656-172">그러나 사용자 수가 많고 해당 사용자가 이미 설정 된 Azure AD 그룹의 구성원 인 경우에는 중첩 그룹 또는 다른 그룹을 구성원으로 포함 하는 그룹을 사용 하 여 SharePoint 권한을 보다 쉽게 할당할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6b656-172">However, if you have a large number of people and those people are already members of established Azure AD groups, you can more easily assign SharePoint permissions by using nested groups, or groups that contain other groups as members.</span></span>
  
<span data-ttu-id="6b656-173">예를 들어 영업, 마케팅, 엔지니어링, 법률 및 지원 부서의 임원 및 해당 부서에서 임원 사용자 계정을 사용 하는 자체 그룹을 공동 작업용으로 사용할 수 있도록 격리 된 SharePoint online 팀 사이트를 만들려고 합니다. 멤버 자격.</span><span class="sxs-lookup"><span data-stu-id="6b656-173">For example, you want to create an isolated SharePoint online team site for collaboration among the executives of the sales, marketing, engineering, legal, and support departments and those departments already their own groups with executive user account membership.</span></span> <span data-ttu-id="6b656-174">새 사이트 구성원에 대해 새 그룹을 만들고 모든 개별 executive 사용자 계정을 배치 하는 것이 아니라 새 그룹의 각 부서에 대 한 기존 임원 그룹을 배치 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b656-174">Rather than creating a new group for the new site members and placing all the individual executive user accounts in it, put the existing executive groups for each department in the new group.</span></span>
  
 <span data-ttu-id="6b656-175">여러 조직 간에 Office 365 구독을 공유 하는 경우 사용자 계정 수가 많기 때문에 조직에 대해 격리 된 사이트에 대 한 단일 그룹 구성원 자격이 관리 하기가 어려울 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6b656-175">If you are sharing an Office 365 subscription between multiple organizations, a single level of group membership for an isolated site for an organization might become difficult to manage due to the sheer number of user accounts.</span></span> <span data-ttu-id="6b656-176">이 경우 조직 내에서 그룹을 포함 하는 각 조직에 대해 중첩 된 Azure AD 그룹을 사용 하 여 사용 권한을 관리할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6b656-176">In this case, you can use nested Azure AD groups for each organization that contain the groups within their organizations to manage the permissions.</span></span>
  
<span data-ttu-id="6b656-177">중첩 된 Azure AD 그룹을 사용 하려면:</span><span class="sxs-lookup"><span data-stu-id="6b656-177">To use nested Azure AD groups:</span></span>
  
1. <span data-ttu-id="6b656-178">사용자 계정을 포함 하는 Azure AD 그룹을 식별 하거나 만들고 해당 사용자 계정을 구성원으로 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b656-178">Identify or create the Azure AD groups that will contain user accounts and add the appropriate user accounts as members.</span></span>
    
2. <span data-ttu-id="6b656-179">다른 Azure AD 그룹을 포함 하는 컨테이너 Azure AD 기반 액세스 그룹을 만들고 해당 그룹을 구성원으로 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b656-179">Create the container Azure AD-based access group that will contain the other Azure AD groups and add those groups as members.</span></span>
    
3.  <span data-ttu-id="6b656-180">컨테이너 액세스 그룹에 대 한 적절 한 액세스 수준에 대해 SharePoint 그룹 및 해당 권한 수준을 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b656-180">For the appropriate level of access for the container access group, identify the SharePoint group and corresponding permission level.</span></span>
    
> [!NOTE]
> <span data-ttu-id="6b656-181">중첩 된 Office 365 그룹은 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="6b656-181">You cannot use nested Office 365 groups.</span></span> 
  
<span data-ttu-id="6b656-182">다음은 ProjectX 구성원 액세스 그룹에 대 한 중첩 된 Azure AD 그룹의 예입니다.</span><span class="sxs-lookup"><span data-stu-id="6b656-182">Here is an example of nested Azure AD groups for the ProjectX member access group.</span></span>
  
![ProjectX 사이트의 구성원 액세스 그룹에 대해 중첩 된 액세스 그룹을 사용 하는 방법의 예입니다.](media/2abca710-bf9e-4ce8-9bcd-a8e128264fb1.png)
  
<span data-ttu-id="6b656-184">연구, 엔지니어링 및 프로젝트 리더 팀의 모든 사용자 계정이 사이트 구성원 이므로 Azure AD 그룹을 ProjectX Members access 그룹에 추가 하는 것이 더 쉽습니다.</span><span class="sxs-lookup"><span data-stu-id="6b656-184">Because all of the user accounts in the Research, Engineering, and Project leads teams are intended to be site members, it is easier to add their Azure AD groups to the ProjectX Members access group.</span></span>
  
## <a name="next-step"></a><span data-ttu-id="6b656-185">다음 단계</span><span class="sxs-lookup"><span data-stu-id="6b656-185">Next step</span></span>

<span data-ttu-id="6b656-186">격리 된 사이트를 만들고 프로덕션 환경에 구성할 준비가 되 면 [격리 SharePoint Online 팀 사이트 배포](deploy-an-isolated-sharepoint-online-team-site.md)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="6b656-186">When you are ready to create and configure an isolated site in production, see [Deploy an isolated SharePoint Online team site](deploy-an-isolated-sharepoint-online-team-site.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="6b656-187">참고 항목</span><span class="sxs-lookup"><span data-stu-id="6b656-187">See Also</span></span>

[<span data-ttu-id="6b656-188">격리된 SharePoint Online 팀 사이트</span><span class="sxs-lookup"><span data-stu-id="6b656-188">Isolated SharePoint Online team sites</span></span>](isolated-sharepoint-online-team-sites.md)
  
[<span data-ttu-id="6b656-189">격리된 SharePoint Online 팀 사이트 관리</span><span class="sxs-lookup"><span data-stu-id="6b656-189">Manage an isolated SharePoint Online team site</span></span>](manage-an-isolated-sharepoint-online-team-site.md)

[<span data-ttu-id="6b656-190">격리된 SharePoint Online 팀 사이트 배포</span><span class="sxs-lookup"><span data-stu-id="6b656-190">Deploy an isolated SharePoint Online team site</span></span>](deploy-an-isolated-sharepoint-online-team-site.md)



