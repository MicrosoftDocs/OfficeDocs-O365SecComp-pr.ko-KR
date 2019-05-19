---
title: 격리된 SharePoint Online 팀 사이트 배포
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
ms.date: 05/14/2018
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: Ent_O365
ms.custom: Ent_Solutions
ms.assetid: 3033614b-e23b-4f68-9701-f62525eafaab
description: '요약: 다음 단계별 지침을 사용 하 여 격리 된 SharePoint Online 팀 사이트를 새로 배포 합니다.'
ms.openlocfilehash: 488f834f568e65d35a7186b85cc393f5a66b2900
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/17/2019
ms.locfileid: "34153400"
---
# <a name="deploy-an-isolated-sharepoint-online-team-site"></a><span data-ttu-id="4e0c1-103">격리된 SharePoint Online 팀 사이트 배포</span><span class="sxs-lookup"><span data-stu-id="4e0c1-103">Deploy an isolated SharePoint Online team site</span></span>

 <span data-ttu-id="4e0c1-104">**요약:** 다음 단계별 지침을 사용 하 여 격리 된 SharePoint Online 팀 사이트를 새로 배포 합니다.</span><span class="sxs-lookup"><span data-stu-id="4e0c1-104">**Summary:** Deploy a new isolated SharePoint Online team site with these step-by-step instructions.</span></span>
  
<span data-ttu-id="4e0c1-105">이 문서는 Microsoft Office 365에서 격리 된 SharePoint Online 팀 사이트를 만들고 구성 하기 위한 단계별 배포 가이드입니다.</span><span class="sxs-lookup"><span data-stu-id="4e0c1-105">This article is a step-by-step deployment guide for creating and configuring an isolated SharePoint Online team site in Microsoft Office 365.</span></span> <span data-ttu-id="4e0c1-106">이러한 단계에서는 각 액세스 수준에 대해 단일 Azure Active Directory (AD) 기반 액세스 그룹을 사용 하 여 세 가지 기본 SharePoint 그룹 및 해당 사용 권한 수준을 사용할 것으로 가정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4e0c1-106">These steps assume the use of the three default SharePoint groups and corresponding permission levels, with a single Azure Active Directory (AD)-based access group for each level of access.</span></span>
  
## <a name="phase-1-create-and-populate-the-team-site-access-groups"></a><span data-ttu-id="4e0c1-107">1 단계: 팀 사이트 액세스 그룹 만들기 및 채우기</span><span class="sxs-lookup"><span data-stu-id="4e0c1-107">Phase 1: Create and populate the team site access groups</span></span>

<span data-ttu-id="4e0c1-108">이 단계에서는 세 가지 기본 SharePoint 그룹에 대 한 세 개의 Azure AD 기반 액세스 그룹을 만들고 적절 한 사용자 계정으로 채웁니다.</span><span class="sxs-lookup"><span data-stu-id="4e0c1-108">In this phase, you create the three Azure AD-based access groups for the three default SharePoint groups and populate them with the appropriate user accounts.</span></span>
  
> [!NOTE]
> <span data-ttu-id="4e0c1-109">다음 단계에서는 필요한 모든 사용자 계정이 이미 있고 해당 라이선스가 할당 된 것으로 가정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4e0c1-109">The following steps assume that all necessary user accounts already exist and are assigned the appropriate licenses.</span></span> <span data-ttu-id="4e0c1-110">그렇지 않은 경우 1 단계를 진행 하기 전에 추가 하 고 라이선스를 할당 하세요.</span><span class="sxs-lookup"><span data-stu-id="4e0c1-110">If not, please add them and assign licenses before proceeding to step 1.</span></span> 
  
### <a name="step-1-list-the-sharepoint-online-admins-for-the-site"></a><span data-ttu-id="4e0c1-111">1 단계: 사이트에 대 한 SharePoint Online 관리자 나열</span><span class="sxs-lookup"><span data-stu-id="4e0c1-111">Step 1: List the SharePoint Online admins for the site</span></span>

<span data-ttu-id="4e0c1-112">격리 된 팀 사이트에 대 한 SharePoint Online 관리자에 해당 하는 사용자 계정 집합을 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="4e0c1-112">Determine the set of user accounts corresponding to the SharePoint Online admins for the isolated team site.</span></span>
  
<span data-ttu-id="4e0c1-113">Office 365을 통해 사용자 계정 및 그룹을 관리 하는 경우 Windows PowerShell을 사용 하려면 upn (사용자 계정 이름) 목록 (예: belindan@contoso.com)을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="4e0c1-113">If you are managing user accounts and groups through Office 365 and want to use Windows PowerShell, make a list of their user principal names (UPNs) (example UPN: belindan@contoso.com).</span></span>
  
### <a name="step-2-list-the-members-for-the-site"></a><span data-ttu-id="4e0c1-114">2 단계: 사이트 구성원 나열</span><span class="sxs-lookup"><span data-stu-id="4e0c1-114">Step 2: List the members for the site</span></span>

<span data-ttu-id="4e0c1-115">사이트 내에 저장 된 리소스에 대해 공동으로 작업할 격리 된 팀 사이트의 구성원에 해당 하는 사용자 계정 집합을 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="4e0c1-115">Determine the set of user accounts corresponding to the members for the isolated team site, those who will be collaborating on resources stored within the site.</span></span>
  
<span data-ttu-id="4e0c1-116">Office 365을 통해 사용자 계정 및 그룹을 관리 하는 경우 PowerShell을 사용 하려면 Upn 목록을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="4e0c1-116">If you are managing user accounts and groups through Office 365 and want to use PowerShell, make a list of their UPNs.</span></span> <span data-ttu-id="4e0c1-117">사이트 구성원이 많은 경우에는 Upn 목록을 텍스트 파일에 저장 하 고 모두 단일 PowerShell 명령을 사용 하 여 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4e0c1-117">If there are a lot of site members, you can store the list of UPNs in a text file and add them all with a single PowerShell command.</span></span>
  
### <a name="step-3-list-the-viewers-for-the-site"></a><span data-ttu-id="4e0c1-118">3 단계: 사이트에 대 한 보는 사람 나열</span><span class="sxs-lookup"><span data-stu-id="4e0c1-118">Step 3: List the viewers for the site</span></span>

<span data-ttu-id="4e0c1-119">격리 된 팀 사이트의 보는 사람에 해당 하는 사용자 계정 집합 (사이트에 저장 된 리소스를 볼 수는 있지만 수정 하거나 콘텐츠를 직접 공동으로 작업 하지는 않는 경우)을 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4e0c1-119">Determine the set of user accounts corresponding to the viewers of the isolated team site, those who can view the resources stored in the site but not modify them or directly collaborate on their contents.</span></span>
  
<span data-ttu-id="4e0c1-120">Office 365을 통해 사용자 계정 및 그룹을 관리 하는 경우 PowerShell을 사용 하려면 Upn 목록을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="4e0c1-120">If you are managing user accounts and groups through Office 365 and want to use PowerShell, make a list of their UPNs.</span></span> <span data-ttu-id="4e0c1-121">사이트 구성원이 많은 경우에는 Upn 목록을 텍스트 파일에 저장 하 고 모두 단일 PowerShell 명령을 사용 하 여 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4e0c1-121">If there are a lot of site members, you can store the list of UPNs in a text file and add them all with a single PowerShell command.</span></span>
  
<span data-ttu-id="4e0c1-122">사이트 보기에는 임원 관리, 법률 자문 위원 또는 부서별 부서 간 이해 관계자가 포함 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4e0c1-122">Viewers for the site might include executive management, legal counsel, or inter-departmental stakeholders.</span></span>
  
### <a name="step-4-create-the-three-access-groups-for-the-site-in-azure-ad"></a><span data-ttu-id="4e0c1-123">4 단계: Azure AD에서 사이트에 대 한 세 개의 액세스 그룹 만들기</span><span class="sxs-lookup"><span data-stu-id="4e0c1-123">Step 4: Create the three access groups for the site in Azure AD</span></span>

<span data-ttu-id="4e0c1-124">Azure AD에서 다음 액세스 그룹을 만들어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="4e0c1-124">You need to create the following access groups in Azure AD:</span></span>
  
- <span data-ttu-id="4e0c1-125">사이트 관리자 (1 단계에서 목록이 포함 됨)</span><span class="sxs-lookup"><span data-stu-id="4e0c1-125">Site admins (which will contain the list from step 1)</span></span>
    
- <span data-ttu-id="4e0c1-126">사이트 구성원 (2 단계에서 목록이 포함 됨)</span><span class="sxs-lookup"><span data-stu-id="4e0c1-126">Site members (which will contain the list from step 2)</span></span>
    
- <span data-ttu-id="4e0c1-127">사이트 뷰어 (3 단계의 목록이 포함 됨)</span><span class="sxs-lookup"><span data-stu-id="4e0c1-127">Site viewers (which will contain the list from step 3)</span></span>
    
1. <span data-ttu-id="4e0c1-128">브라우저에서 Azure 포털로 이동한 [https://portal.azure.com](https://portal.azure.com) 후 사용자 관리 관리자 또는 회사 관리자 역할로 할당 된 계정의 자격 증명을 사용 하 여 로그인 합니다.</span><span class="sxs-lookup"><span data-stu-id="4e0c1-128">In your browser, go to the Azure portal at [https://portal.azure.com](https://portal.azure.com) and sign in with the credentials of an account that has been assigned with User Management Admin or Company Administrator role.</span></span>
    
2. <span data-ttu-id="4e0c1-129">Azure Portal에서 **Azure Active Directory > 그룹**을 차례로 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="4e0c1-129">In the Azure portal, click **Azure Active Directory > Groups**.</span></span>
    
3. <span data-ttu-id="4e0c1-130">**그룹 - 모든 그룹** 블레이드에서 **+ 새 그룹**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="4e0c1-130">On the **Groups - All groups** blade, click **+ New group**.</span></span>
    
4. <span data-ttu-id="4e0c1-131">**그룹** 블레이드에서:</span><span class="sxs-lookup"><span data-stu-id="4e0c1-131">On the **Group** blade:</span></span>
    
  - <span data-ttu-id="4e0c1-132">**그룹 유형**에서 **Office 365**를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="4e0c1-132">Select **Office 365** in **Group type**.</span></span>
    
  - <span data-ttu-id="4e0c1-133">**이름**에 그룹 이름을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="4e0c1-133">Type the group name in **Name**.</span></span>
    
  - <span data-ttu-id="4e0c1-134">그룹 **설명**에 그룹에 대 한 설명을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="4e0c1-134">Type a description of the group in **Group description**.</span></span>
    
  - <span data-ttu-id="4e0c1-135">**멤버 유형**에서 **할당됨**을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="4e0c1-135">Select **Assigned** in **Membership type**.</span></span>
    
5. <span data-ttu-id="4e0c1-136">**만들기**를 클릭한 다음 **그룹** 블레이드를 닫습니다.</span><span class="sxs-lookup"><span data-stu-id="4e0c1-136">Click **Create**, and then close the **Group** blade.</span></span>
    
6. <span data-ttu-id="4e0c1-137">추가 그룹에 대해 3-5 단계를 반복 합니다.</span><span class="sxs-lookup"><span data-stu-id="4e0c1-137">Repeat steps 3-5 for your additional groups.</span></span>
    
> [!NOTE]
> <span data-ttu-id="4e0c1-138">Office 기능을 사용 하도록 설정 하려면 Azure portal을 사용 하 여 그룹을 만들어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="4e0c1-138">You need to use the Azure portal to create the groups so that they have Office features enabled.</span></span> <span data-ttu-id="4e0c1-139">SharePoint Online 격리 된 사이트가 파일을 암호화 하 고 특정 그룹에 사용 권한을 할당 하기 위해 Azure Information Protection 레이블을 사용 하 여 고도로 기밀 사이트로 구성 된 경우에는 허용 되는 그룹이 Office 기능을 사용 하도록 설정 된 상태로 만들어져 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="4e0c1-139">If a SharePoint Online isolated site is later configured as a Highly Confidential site with an Azure Information Protection label to encrypt files and assign permission to specific groups, the permitted groups must have been created with Office features enabled.</span></span> <span data-ttu-id="4e0c1-140">Azure AD 그룹을 만든 후에는 Office 기능 설정을 변경할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="4e0c1-140">You cannot change the Office features setting of an Azure AD group after it has been created.</span></span> 
  
<span data-ttu-id="4e0c1-141">다음은 세 개의 사이트 액세스 그룹이 포함 된 결과 구성입니다.</span><span class="sxs-lookup"><span data-stu-id="4e0c1-141">Here is your resulting configuration with the three site access groups.</span></span>
  
![격리 된 SharePoint Online 사이트 배포에 대 한 세 가지 액세스 그룹](media/c2557f61-478b-4494-95e9-d79fe5909e8b.png)
  
### <a name="step-5-add-the-user-accounts-to-the-access-groups"></a><span data-ttu-id="4e0c1-143">5단계.</span><span class="sxs-lookup"><span data-stu-id="4e0c1-143">Step 5.</span></span> <span data-ttu-id="4e0c1-144">액세스 그룹에 사용자 계정 추가</span><span class="sxs-lookup"><span data-stu-id="4e0c1-144">Add the user accounts to the access groups</span></span>

<span data-ttu-id="4e0c1-145">이 단계에서는 다음을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="4e0c1-145">In this step, do the following:</span></span>
  
1. <span data-ttu-id="4e0c1-146">1 단계의 사용자 목록을 site admins 액세스 그룹에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="4e0c1-146">Add the list of users from step 1 to the site admins access group</span></span>
    
2. <span data-ttu-id="4e0c1-147">2 단계의 사용자 목록을 사이트 구성원 액세스 그룹에 추가</span><span class="sxs-lookup"><span data-stu-id="4e0c1-147">Add the list of users from step 2 to the site members access group</span></span>
    
3. <span data-ttu-id="4e0c1-148">3 단계의 사용자 목록을 사이트 뷰어 액세스 그룹에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="4e0c1-148">Add the list of users from step 3 to the site viewers access group</span></span>
    
<span data-ttu-id="4e0c1-149">Windows Server AD를 통해 사용자 계정 및 그룹을 관리 하는 경우에는 일반 Windows Server AD 사용자 및 그룹 관리 절차를 사용 하 여 적절 한 액세스 그룹에 사용자를 추가 하 고 Office 365 구독과의 동기화를 기다립니다.</span><span class="sxs-lookup"><span data-stu-id="4e0c1-149">If you are managing user accounts and groups through Windows Server AD, add users to the appropriate access groups using your normal Windows Server AD user and group management procedures and wait for synchronization with your Office 365 subscription.</span></span>
  
<span data-ttu-id="4e0c1-150">Office 365을 통해 사용자 계정 및 그룹을 관리 하는 경우 Office 관리 센터 또는 PowerShell을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4e0c1-150">If you are managing user accounts and groups through Office 365, you can use the Office Admin center or PowerShell.</span></span> <span data-ttu-id="4e0c1-151">액세스 그룹의 그룹 이름이 중복 된 경우 Office 관리 센터를 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="4e0c1-151">If you have duplicate group names for any of the access groups, you should use the Office Admin center.</span></span>
  
<span data-ttu-id="4e0c1-152">Office 관리 센터의 경우 사용자 계정 관리자 또는 회사 관리자 역할이 할당 된 사용자 계정으로 로그인 하 고 그룹을 사용 하 여 적절 한 액세스 그룹에 적절 한 사용자 계정 및 그룹을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="4e0c1-152">For the Office Admin center, sign in with a user account that has been assigned the User Account Administrator or Company Administrator role and use Groups to add the appropriate user accounts and groups to the appropriate access groups.</span></span>
  
<span data-ttu-id="4e0c1-153">PowerShell의 경우 먼저 [Graph 모듈에 대 한 Azure Active Directory PowerShell을 사용 하 여 연결](https://docs.microsoft.com/office365/enterprise/powershell/connect-to-office-365-powershell#connect-with-the-azure-active-directory-powershell-for-graph-module)합니다.</span><span class="sxs-lookup"><span data-stu-id="4e0c1-153">For PowerShell, first [Connect with the Azure Active Directory PowerShell for Graph module](https://docs.microsoft.com/office365/enterprise/powershell/connect-to-office-365-powershell#connect-with-the-azure-active-directory-powershell-for-graph-module).</span></span>
  
<span data-ttu-id="4e0c1-154">다음으로, 다음 명령 블록을 사용 하 여 액세스 그룹에 개별 사용자 계정을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="4e0c1-154">Next, use the following command block to add an individual user account to an access group:</span></span>
  
```
$userUPN="<UPN of the user account>"
$grpName="<display name of the access group>"
Add-AzureADGroupMember -RefObjectId (Get-AzureADUser | Where { $_.UserPrincipalName -eq $userUPN }).ObjectID -ObjectId (Get-AzureADGroup | Where { $_.DisplayName -eq $grpName }).ObjectID
```

> [!TIP]
> <span data-ttu-id="4e0c1-155">모든 PowerShell 명령 및 그룹 및 사용자 계정 이름에 따라 PowerShell 명령을 생성 하는 Excel 구성 워크시트가 포함 된 텍스트 파일의 경우 [격리 된 SharePoint Online 팀 사이트 배포 키트](https://gallery.technet.microsoft.com/Isolated-SharePoint-Online-0b364907)를 다운로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="4e0c1-155">For a text file that contains all the PowerShell commands and an Excel configuration worksheet that generates PowerShell commands based on your group and user account names, download the [Isolated SharePoint Online Team Site Deployment Kit](https://gallery.technet.microsoft.com/Isolated-SharePoint-Online-0b364907).</span></span> 
  
<span data-ttu-id="4e0c1-156">텍스트 파일의 액세스 그룹에 대 한 사용자 계정의 Upn을 저장 한 경우 다음 PowerShell 명령 블록을 사용 하 여 모든 항목을 한 번에 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4e0c1-156">If you stored the UPNs of user accounts for any of the access groups in a text file, you can use the following PowerShell command block to add them all at one time:</span></span>
  
```
$grpName="<display name of the access group>"
$fileName="<path and name of the file containing the list of account UPNs>"
$grpID=(Get-AzureADGroup | Where { $_.DisplayName -eq $grpName }).ObjectID
Get-Content $fileName | ForEach { $userUPN=$_; Add-AzureADGroupMember -RefObjectId (Get-AzureADUser | Where { $_.UserPrincipalName -eq $userUPN }).ObjectID -ObjectID $grpID }
```

<span data-ttu-id="4e0c1-157">PowerShell의 경우 다음 명령 블록을 사용 하 여 액세스 그룹에 개별 그룹을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="4e0c1-157">For PowerShell, use the following command block to add an individual group to an access group:</span></span>
  
```
$nestedGrpName="<display name of the group to add to the access group>"
$grpName="<display name of the access group>"
Add-AzureADGroupMember -RefObjectId (Get-AzureADGroup | Where { $_.DisplayName -eq $nestedGrpName }).ObjectID -ObjectID (Get-AzureADGroup | Where { $_.DisplayName -eq $grpName }).ObjectID

```

<span data-ttu-id="4e0c1-158">결과는 다음과 같아야 합니다.</span><span class="sxs-lookup"><span data-stu-id="4e0c1-158">The results should be the following:</span></span>
  
- <span data-ttu-id="4e0c1-159">Site admins Azure AD 그룹에는 사이트 관리자 사용자 계정 또는 그룹이 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4e0c1-159">The site admins Azure AD group contains the site admin user accounts or groups</span></span>
    
- <span data-ttu-id="4e0c1-160">사이트 구성원 Azure AD 그룹에는 사이트 구성원 사용자 계정 또는 그룹이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4e0c1-160">The site members Azure AD group contains the site member user accounts or groups</span></span>
    
- <span data-ttu-id="4e0c1-161">사이트 뷰어 Azure AD 그룹에는 사이트 콘텐츠만 볼 수 있는 사용자 계정 또는 그룹이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4e0c1-161">The site viewers Azure AD group contains the user accounts or groups that can only view the site contents</span></span>
    
<span data-ttu-id="4e0c1-162">Office 관리 센터를 사용 하거나 다음 PowerShell 명령 블록을 사용 하 여 각 액세스 그룹의 그룹 구성원 목록을 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="4e0c1-162">Validate the list of group members for each access group with the Office Admin center or with the following PowerShell command block:</span></span>
  
```
$grpName="<display name of the access group>"
Get-AzureADGroupMember -ObjectId (Get-AzureADGroup | Where { $_.DisplayName -eq $grpName }).ObjectID | Sort UserPrincipalName | Select UserPrincipalName,DisplayName,UserType
```

<span data-ttu-id="4e0c1-163">다음은 사용자 계정이 나 그룹으로 채워진 3 개의 사이트 액세스 그룹이 포함 된 결과 구성입니다.</span><span class="sxs-lookup"><span data-stu-id="4e0c1-163">Here is your resulting configuration with the three site access groups populated with user accounts or groups.</span></span>
  
![세 개의 액세스 그룹은 사용자 계정으로 채워집니다.](media/2320107c-dad6-4c8f-94e5-f6427c125e71.png)
  
## <a name="phase-2-create-and-configure-the-isolated-team-site"></a><span data-ttu-id="4e0c1-165">2 단계: 격리 된 팀 사이트 만들기 및 구성</span><span class="sxs-lookup"><span data-stu-id="4e0c1-165">Phase 2: Create and configure the isolated team site</span></span>

<span data-ttu-id="4e0c1-166">이 단계에서는 격리 된 SharePoint Online 사이트를 만들고 기본 SharePoint Online 권한 수준에 대 한 사용 권한을 구성 하 여 새 Azure AD 기반 액세스 그룹을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="4e0c1-166">In this phase, you create the isolated SharePoint Online site and configure the permissions for the default SharePoint Online permission levels to use your new Azure AD-based access groups.</span></span>
  
<span data-ttu-id="4e0c1-167">먼저 다음 단계를 사용 하 여 SharePoint Online 팀 사이트를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="4e0c1-167">First, create the SharePoint Online team site with these steps.</span></span>
  
1. <span data-ttu-id="4e0c1-168">SharePoint Online 팀 사이트(SharePoint Online 관리자)를 관리하는 데에도 사용할 계정으로 관리 센터에 로그인합니다.</span><span class="sxs-lookup"><span data-stu-id="4e0c1-168">Sign in to the admin center with an account that will also be used to administer the SharePoint Online team site (a SharePoint Online administrator).</span></span> <span data-ttu-id="4e0c1-169">도움을 받으려면 [Office 365에 로그인하는 위치](https://support.office.com/Article/Where-to-sign-in-to-Office-365-e9eb7d51-5430-4929-91ab-6157c5a050b4)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="4e0c1-169">For help, see [Where to sign in to Office 365](https://support.office.com/Article/Where-to-sign-in-to-Office-365-e9eb7d51-5430-4929-91ab-6157c5a050b4).</span></span>
    
2. <span data-ttu-id="4e0c1-170">타일 목록에서 **SharePoint**를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="4e0c1-170">In the list of tiles, click **SharePoint**.</span></span>
    
3. <span data-ttu-id="4e0c1-171">브라우저의 새 **SharePoint 탭**에서 + **사이트 만들기**를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="4e0c1-171">In the new **SharePoint** tab of your browser, click **+ Create site**.</span></span>
    
4. <span data-ttu-id="4e0c1-172">**사이트 만들기** 페이지에서 **팀 사이트**를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="4e0c1-172">On the **Create a site** page, click **Team site**.</span></span>
    
5. <span data-ttu-id="4e0c1-173">**사이트 이름**에 팀 사이트의 이름을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="4e0c1-173">In **Site name**, type a name for the team site.</span></span> 
    
6. <span data-ttu-id="4e0c1-174">**팀 사이트 설명** 에서 사이트의 용도에 대 한 설명을 입력 합니다 (선택 사항).</span><span class="sxs-lookup"><span data-stu-id="4e0c1-174">In **Team site description,** type an optional description of the purpose of the site.</span></span>
    
7. <span data-ttu-id="4e0c1-175">**개인 정보 설정**에서 **비공개 – 구성원만 이 사이트에 액세스할 수 있습니다.** 를 선택하고 **다음**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="4e0c1-175">In **Privacy settings**, select **Private - only members can access this site**, and then click **Next**.</span></span>
    
8. <span data-ttu-id="4e0c1-176">**어떤 사람을 추가하시겠습니까?** 창에서 **마침**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="4e0c1-176">On the **Who do you want to add?** pane, click **Finish**.</span></span>
    
<span data-ttu-id="4e0c1-177">다음으로, 새 SharePoint Online 팀 사이트에서 사용 권한을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="4e0c1-177">Next, from the new SharePoint Online team site, configure permissions.</span></span>
  
1. <span data-ttu-id="4e0c1-178">도구 모음에서 설정 아이콘을 클릭한 다음, **사이트 권한**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="4e0c1-178">In the tool bar, click the settings icon, and then click **Site permissions**.</span></span>
    
2. <span data-ttu-id="4e0c1-179">**사이트 권한** 창에서 **고급 권한 설정**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="4e0c1-179">In the **Site permissions** pane, click **Advanced permissions settings**.</span></span>
    
3. <span data-ttu-id="4e0c1-180">브라우저의 새 **권한** 탭에서 **액세스 요청 설정**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="4e0c1-180">On the new **Permissions** tab of your browser, click **Access Request Settings**.</span></span>
    
4. <span data-ttu-id="4e0c1-181">**액세스 요청 설정** 대화 상자에서 **구성원이 사이트 및 개별 파일 및 폴더를 공유 하도록 허용** 을 선택 취소 하 고 세 확인란이 모두 선택 취소 되도록 **액세스 요청을 허용한** 다음 **확인**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="4e0c1-181">In the **Access Requests Settings** dialog box, clear **Allow member to share the site and individual files and folders** and **Allow access requests** (so that all three check boxes are cleared), and then click **OK**.</span></span>
    
5. <span data-ttu-id="4e0c1-182">브라우저의 **사용 권한** 탭에 있는 목록에서 \*\* \<사이트 name> 구성원\*\* 을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="4e0c1-182">On the **Permissions** tab of your browser, click **\<site name> Members** in the list.</span></span>
    
6. <span data-ttu-id="4e0c1-183">**사용자 및 그룹**에서 **새로 만들기**를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="4e0c1-183">In **People and Groups**, click **New**.</span></span>
    
7. <span data-ttu-id="4e0c1-184">**공유** 대화 상자에서 사이트 구성원 액세스 그룹의 이름을 입력 하 고,이를 선택한 다음, **공유**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="4e0c1-184">In the **Share** dialog box, type the name of the site members access group, select it, and then click **Share**.</span></span>
    
8. <span data-ttu-id="4e0c1-185">브라우저에서 뒤로 단추를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="4e0c1-185">Click the back button on your browser.</span></span>
    
9. <span data-ttu-id="4e0c1-186">목록에서 \*\* \<사이트 name> 소유자\*\* 를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="4e0c1-186">Click **\<site name> Owners** in the list.</span></span>
    
10. <span data-ttu-id="4e0c1-187">**사용자 및 그룹**에서 **새로 만들기**를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="4e0c1-187">In **People and Groups**, click **New**.</span></span>
    
11. <span data-ttu-id="4e0c1-188">**공유** 대화 상자에서 site admins 액세스 그룹의 이름을 입력 하 고,이를 선택한 다음, **공유**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="4e0c1-188">In the **Share** dialog box, type the name of the site admins access group, select it, and then click **Share**.</span></span>
    
12. <span data-ttu-id="4e0c1-189">브라우저에서 뒤로 단추를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="4e0c1-189">Click the back button on your browser.</span></span>
    
13. <span data-ttu-id="4e0c1-190">목록에서 \*\* \<사이트 name> 방문자\*\* 를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="4e0c1-190">Click **\<site name> Visitors** in the list.</span></span>
    
14. <span data-ttu-id="4e0c1-191">**사용자 및 그룹**에서 **새로 만들기**를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="4e0c1-191">In **People and Groups**, click **New**.</span></span>
    
15. <span data-ttu-id="4e0c1-192">**공유** 대화 상자에서 사이트 뷰어 액세스 그룹의 이름을 입력 하 고,이를 선택한 다음, **공유**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="4e0c1-192">In the **Share** dialog box, type the name of the site viewers access group, select it, and then click **Share**.</span></span>
    
16. <span data-ttu-id="4e0c1-193">브라우저의 **권한** 탭을 닫습니다.</span><span class="sxs-lookup"><span data-stu-id="4e0c1-193">Close the **Permissions** tab of your browser.</span></span>
    
<span data-ttu-id="4e0c1-194">이러한 권한 설정의 결과는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="4e0c1-194">The results of these permission settings are:</span></span>
  
- <span data-ttu-id="4e0c1-195">Site name> owner SharePoint 그룹에는 모든 구성원이 모든 권한 수준을 갖는 사이트 관리자 액세스 그룹이 포함 되어 있습니다 \*\*\*\* . \*\* \<\*\*</span><span class="sxs-lookup"><span data-stu-id="4e0c1-195">The **\<site name> Owners** SharePoint group contains the site admins access group, in which all the members have the **Full control** permission level.</span></span>
    
- <span data-ttu-id="4e0c1-196">Site name> Members SharePoint 그룹에는 모든 구성원이 **편집** 권한 수준을 갖는 사이트 구성원 액세스 그룹이 포함 되어 있습니다. \*\* \<\*\*</span><span class="sxs-lookup"><span data-stu-id="4e0c1-196">The **\<site name> Members** SharePoint group contains the site members access group, in which all the members have the **Edit** permission level.</span></span>
    
- <span data-ttu-id="4e0c1-197">Site name> 방문자 SharePoint 그룹에는 모든 구성원이 **읽기** 권한 수준을 갖는 사이트 뷰어 액세스 그룹이 포함 되어 있습니다. \*\* \<\*\*</span><span class="sxs-lookup"><span data-stu-id="4e0c1-197">The **\<site name> Visitors** SharePoint group contains the site viewers access group, in which all the members have the **Read** permission level.</span></span>
    
- <span data-ttu-id="4e0c1-198">구성원이 다른 구성원을 초대 하거나 구성원이 아닌 사람에 게 액세스를 요청 하는 기능은 사용 하지 않도록 설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4e0c1-198">The ability for members to invite other members or for non-members to request access is disabled.</span></span>
    
<span data-ttu-id="4e0c1-199">다음은 사용자 계정 또는 Azure AD 그룹으로 채워지는 세 개의 액세스 그룹을 사용 하도록 구성 된 사이트에 대 한 세 가지 SharePoint 그룹의 구성 결과입니다.</span><span class="sxs-lookup"><span data-stu-id="4e0c1-199">Here is your resulting configuration with the three SharePoint groups for the site configured to use the three access groups, which are populated with user accounts or Azure AD groups.</span></span>
  
![액세스 그룹과 사용자 계정을 사용 하는 격리 된 SharePoint Online 사이트의 최종 구성](media/e7618971-06ab-447b-90ff-d8be3790fe63.png)
  
<span data-ttu-id="4e0c1-201">액세스 그룹 중 하나의 그룹 구성원 자격을 통해 사이트의 구성원은 이제 사이트의 리소스를 사용 하 여 공동 작업을 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4e0c1-201">You and the members of the site, through group membership in one of the access groups, can now collaborate using the resources of the site.</span></span>
  
## <a name="next-step"></a><span data-ttu-id="4e0c1-202">다음 단계</span><span class="sxs-lookup"><span data-stu-id="4e0c1-202">Next step</span></span>

<span data-ttu-id="4e0c1-203">사이트 액세스 그룹 구성원 자격을 변경 하거나 사용자 지정 사용 권한이 있는 문서 폴더를 만들려면 [격리 된 SharePoint Online 팀 사이트 관리](manage-an-isolated-sharepoint-online-team-site.md)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="4e0c1-203">When you need to change site access group membership or create a document folder with custom permissions, see [Manage an isolated SharePoint Online team site](manage-an-isolated-sharepoint-online-team-site.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="4e0c1-204">참고 항목</span><span class="sxs-lookup"><span data-stu-id="4e0c1-204">See Also</span></span>

[<span data-ttu-id="4e0c1-205">격리된 SharePoint Online 팀 사이트</span><span class="sxs-lookup"><span data-stu-id="4e0c1-205">Isolated SharePoint Online team sites</span></span>](isolated-sharepoint-online-team-sites.md)
  
[<span data-ttu-id="4e0c1-206">격리된 SharePoint Online 팀 사이트 디자인</span><span class="sxs-lookup"><span data-stu-id="4e0c1-206">Design an isolated SharePoint Online team site</span></span>](design-an-isolated-sharepoint-online-team-site.md)
  
[<span data-ttu-id="4e0c1-207">격리된 SharePoint Online 팀 사이트 관리</span><span class="sxs-lookup"><span data-stu-id="4e0c1-207">Manage an isolated SharePoint Online team site</span></span>](manage-an-isolated-sharepoint-online-team-site.md)
  



