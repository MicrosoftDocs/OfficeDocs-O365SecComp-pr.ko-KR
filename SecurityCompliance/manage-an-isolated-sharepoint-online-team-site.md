---
title: 격리된 SharePoint Online 팀 사이트 관리
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
ms.date: 12/15/2017
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: Ent_O365
ms.custom: Ent_Solutions
ms.assetid: 79a61003-4905-4ba8-9e8a-16def7add37c
description: '요약: 이러한 절차를 사용 하 여 격리 된 SharePoint Online 팀 사이트를 관리 합니다.'
ms.openlocfilehash: 81a6fcd80bb3e4950eb7b783d1ad964b9bc67cc5
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30214488"
---
# <a name="manage-an-isolated-sharepoint-online-team-site"></a><span data-ttu-id="49c96-103">격리된 SharePoint Online 팀 사이트 관리</span><span class="sxs-lookup"><span data-stu-id="49c96-103">Manage an isolated SharePoint Online team site</span></span>

 <span data-ttu-id="49c96-104">**요약:** 이러한 절차를 사용 하 여 격리 된 SharePoint Online 팀 사이트를 관리 합니다.</span><span class="sxs-lookup"><span data-stu-id="49c96-104">**Summary:** Manage your isolated SharePoint Online team site with these procedures.</span></span>
  
<span data-ttu-id="49c96-105">이 문서에서는 격리 된 SharePoint Online 팀 사이트의 일반적인 관리 작업에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="49c96-105">This article describes common management operations for an isolated SharePoint Online team site.</span></span>
  
## <a name="add-a-new-user"></a><span data-ttu-id="49c96-106">새 사용자 추가</span><span class="sxs-lookup"><span data-stu-id="49c96-106">Add a new user</span></span>

<span data-ttu-id="49c96-107">다른 사용자가 사이트에 참가 하는 경우 사이트 참여 수준을 결정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="49c96-107">When someone new joins the site, you must decide their level of participation in the site:</span></span>
  
- <span data-ttu-id="49c96-108">관리: 새 사용자 계정을 site admins 액세스 그룹에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="49c96-108">Administration: Add the new user account to the site admins access group</span></span>
    
- <span data-ttu-id="49c96-109">활성 공동 작업: 사이트 구성원 액세스 그룹에 사용자 계정 추가</span><span class="sxs-lookup"><span data-stu-id="49c96-109">Active collaboration: Add the user account to the site members access group</span></span>
    
- <span data-ttu-id="49c96-110">보기: 사이트 뷰어 액세스 그룹에 사용자 계정 추가</span><span class="sxs-lookup"><span data-stu-id="49c96-110">Viewing: Add the user account to the site viewers access group</span></span>
    
<span data-ttu-id="49c96-111">Windows server ad (Active Directory)를 통해 사용자 계정 및 그룹을 관리 하는 경우 일반 Windows server AD 사용자 및 그룹 관리 절차를 사용 하 여 적절 한 사용자를 해당 액세스 그룹에 추가 하 고 사용자와의 동기화를 기다립니다. Office 365 구독</span><span class="sxs-lookup"><span data-stu-id="49c96-111">If you are managing user accounts and groups through Windows Server Active Directory (AD), add the appropriate users to the appropriate access groups using your normal Windows Server AD user and group management procedures and wait for synchronization with your Office 365 subscription.</span></span>
  
<span data-ttu-id="49c96-112">office 365을 통해 사용자 계정 및 그룹을 관리 하는 경우 office 관리 센터 또는 Microsoft PowerShell을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="49c96-112">If you are managing user accounts and groups through Office 365, you can use the Office Admin center or Microsoft PowerShell:</span></span>
  
- <span data-ttu-id="49c96-113">Office 관리 센터의 경우 사용자 계정 관리자 또는 회사 관리자 역할이 할당 된 사용자 계정으로 로그인 하 고 그룹을 사용 하 여 해당 하는 액세스 그룹에 적절 한 사용자를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="49c96-113">For the Office Admin center, sign in with a user account that has been assigned the User Account Administrator or Company Administrator role and use Groups to add the appropriate users to the appropriate access groups.</span></span>
    
- <span data-ttu-id="49c96-p101">PowerShell의 경우 먼저 [Azure Active Directory V2 PowerShell 모듈을 사용 하 여 연결](https://go.microsoft.com/fwlink/?linkid=842218)합니다. UPN (사용자 계정 이름)을 사용 하 여 액세스 그룹에 사용자 계정을 추가 하려면 다음 PowerShell 명령 블록을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="49c96-p101">For PowerShell, first [Connect with the Azure Active Directory V2 PowerShell module](https://go.microsoft.com/fwlink/?linkid=842218). To add a user account to an access group with its user principal name (UPN), use the following PowerShell command block:</span></span>
    
```
$userUPN="<UPN of the user account>"
$grpName="<display name of the group>"
Add-AzureADGroupMember -RefObjectId (Get-AzureADUser | Where { $_.UserPrincipalName -eq $userUPN }).ObjectID -ObjectID (Get-AzureADGroup | Where { $_.DisplayName -eq $grpName }).ObjectID
```

> [!TIP]
> <span data-ttu-id="49c96-116">모든 powershell 명령 및 그룹 및 사용자 계정 이름에 따라 powershell 명령을 생성 하는 Excel 구성 워크시트가 포함 된 텍스트 파일의 경우 [격리 된 SharePoint Online 팀 사이트 배포 키트](https://gallery.technet.microsoft.com/Isolated-SharePoint-Online-0b364907)를 다운로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="49c96-116">For a text file that contains all the PowerShell commands and an Excel configuration worksheet that generates PowerShell commands based on your group and user account names, download the [Isolated SharePoint Online Team Site Deployment Kit](https://gallery.technet.microsoft.com/Isolated-SharePoint-Online-0b364907).</span></span> 

<span data-ttu-id="49c96-117">표시 이름이 있는 access 그룹에 사용자 계정을 추가 하려면 다음 PowerShell 명령 블록을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="49c96-117">To add a user account to an access group with its display name, use the following PowerShell command block:</span></span>

```
$userDisplayName="<display name of the user account>"
$grpName="<display name of the group>"
Add-AzureADGroupMember -RefObjectId (Get-AzureADUser | Where { $_.DisplayName -eq $userDisplayName }).ObjectID -ObjectID (Get-AzureADGroup | Where { $_.DisplayName -eq $grpName }).ObjectID
```

## <a name="add-a-new-group"></a><span data-ttu-id="49c96-118">새 그룹 추가</span><span class="sxs-lookup"><span data-stu-id="49c96-118">Add a new group</span></span>

<span data-ttu-id="49c96-119">전체 그룹에 대 한 액세스 권한을 추가 하려면 사이트에서 그룹의 모든 구성원에 대 한 참여 수준을 결정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="49c96-119">To add access to an entire group, you must decide the level of participation of all the members of the group in the site:</span></span>
  
- <span data-ttu-id="49c96-120">관리: 사이트 관리자 액세스 그룹에 그룹 추가</span><span class="sxs-lookup"><span data-stu-id="49c96-120">Administration: Add the group to the site admins access group</span></span>
    
- <span data-ttu-id="49c96-121">활성 공동 작업: 사이트 구성원 액세스 그룹에 그룹 추가</span><span class="sxs-lookup"><span data-stu-id="49c96-121">Active collaboration: Add the group to the site members access group</span></span>
    
- <span data-ttu-id="49c96-122">보기: 사이트 뷰어 액세스 그룹에 그룹 추가</span><span class="sxs-lookup"><span data-stu-id="49c96-122">Viewing: Add the group to the site viewers access group</span></span>
    
<span data-ttu-id="49c96-123">Windows server ad를 통해 사용자 계정 및 그룹을 관리 하는 경우 일반 Windows server ad 사용자 및 그룹 관리 절차를 사용 하 여 적절 한 그룹을 적절 한 그룹에 추가 하 고 Office 365 구독과의 동기화를 기다립니다.</span><span class="sxs-lookup"><span data-stu-id="49c96-123">If you are managing user accounts and groups through Windows Server AD, add the appropriate groups to the appropriate groups using your normal Windows Server AD user and group management procedures and wait for synchronization with your Office 365 subscription.</span></span>
  
<span data-ttu-id="49c96-124">office 365을 통해 사용자 계정 및 그룹을 관리 하는 경우 office 관리 센터 또는 PowerShell을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="49c96-124">If you are managing user accounts and groups through Office 365, you can use the Office Admin center or PowerShell:</span></span>
  
- <span data-ttu-id="49c96-125">Office 관리 센터의 경우 사용자 계정 관리자 또는 회사 관리자 역할이 할당 된 사용자 계정으로 로그인 하 고 그룹을 사용 하 여 적절 한 액세스 그룹에 적절 한 그룹을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="49c96-125">For the Office Admin center, sign in with a user account that has been assigned the User Account Administrator or Company Administrator role and use Groups to add the appropriate groups to the appropriate access groups.</span></span>
    
- <span data-ttu-id="49c96-p102">PowerShell의 경우 먼저 [Azure Active Directory V2 PowerShell 모듈을 사용 하 여 연결](https://go.microsoft.com/fwlink/?linkid=842218)합니다. 그런 후 다음 PowerShell 명령을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="49c96-p102">For PowerShell, first [Connect with the Azure Active Directory V2 PowerShell module](https://go.microsoft.com/fwlink/?linkid=842218). Then, use the following PowerShell commands:</span></span>
 
```
$newGroupName="<display name of the new group to add>"
$siteGrpName="<display name of the access group>"
Add-AzureADGroupMember -RefObjectId (Get-AzureADGroup | Where { $_.DisplayName -eq $newGroupName }).ObjectID -ObjectID (Get-AzureADGroup | Where { $_.DisplayName -eq $siteGrpName }).ObjectID
```

## <a name="remove-a-user"></a><span data-ttu-id="49c96-128">사용자 제거</span><span class="sxs-lookup"><span data-stu-id="49c96-128">Remove a user</span></span>

<span data-ttu-id="49c96-129">사이트에서 다른 사용자의 액세스 권한을 제거 해야 하는 경우 해당 사이트의 참가를 기반으로 하는 현재 구성원 인 액세스 그룹에서 해당 항목을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="49c96-129">When someone's access must be removed from the site, you remove them from the access group for which they are currently a member based on their participation in the site:</span></span>
  
- <span data-ttu-id="49c96-130">관리: site admins 액세스 그룹에서 사용자 계정 제거</span><span class="sxs-lookup"><span data-stu-id="49c96-130">Administration: Remove the user account from the site admins access group</span></span>
    
- <span data-ttu-id="49c96-131">활성 공동 작업: 사이트 구성원 액세스 그룹에서 사용자 계정을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="49c96-131">Active collaboration: Remove the user account from the site members access group</span></span>
    
- <span data-ttu-id="49c96-132">보기: 사이트 뷰어 액세스 그룹에서 사용자 계정 제거</span><span class="sxs-lookup"><span data-stu-id="49c96-132">Viewing: Remove the user account from the site viewers access group</span></span>
    
<span data-ttu-id="49c96-133">Windows Server ad를 통해 사용자 계정 및 그룹을 관리 하는 경우에는 일반적인 Windows server ad 사용자 및 그룹 관리 절차를 사용 하 여 적절 한 액세스 그룹에서 해당 사용자를 제거 하 고 Office 365와의 동기화를 기다립니다. 구독은.</span><span class="sxs-lookup"><span data-stu-id="49c96-133">If you are managing user accounts and groups through Windows Server AD, remove the appropriate users from the appropriate access groups using your normal Windows Server AD user and group management procedures and wait for synchronization with your Office 365 subscription.</span></span>
  
<span data-ttu-id="49c96-134">office 365을 통해 사용자 계정 및 그룹을 관리 하는 경우 office 관리 센터 또는 PowerShell을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="49c96-134">If you are managing user accounts and groups through Office 365, you can use the Office Admin center or PowerShell:</span></span>
  
- <span data-ttu-id="49c96-135">Office 관리 센터의 경우 사용자 계정 관리자 또는 회사 관리자 역할이 할당 된 사용자 계정으로 로그인 하 고 그룹을 사용 하 여 해당 하는 액세스 그룹에서 해당 사용자를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="49c96-135">For the Office Admin center, sign in with a user account that has been assigned the User Account Administrator or Company Administrator role and use Groups to remove the appropriate users from the appropriate access groups.</span></span>
    
- <span data-ttu-id="49c96-p103">PowerShell의 경우 먼저 [Azure Active Directory V2 PowerShell 모듈을 사용 하 여 연결](https://go.microsoft.com/fwlink/?linkid=842218)합니다. UPN을 사용 하 여 액세스 그룹에서 사용자 계정을 제거 하려면 다음 PowerShell 명령 블록을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="49c96-p103">For PowerShell, first [Connect with the Azure Active Directory V2 PowerShell module](https://go.microsoft.com/fwlink/?linkid=842218). To remove a user account from an access group with its UPN, use the following PowerShell command block:</span></span>
    
```
$userUPN="<UPN of the user account>"
$grpName="<display name of the access group>"
Remove-AzureADGroupMember -MemberId (Get-AzureADUser | Where { $_.UserPrincipalName -eq $userUPN }).ObjectID -ObjectID (Get-AzureADGroup | Where { $_.DisplayName -eq $grpName }).ObjectID
```

<span data-ttu-id="49c96-138">표시 이름이 있는 액세스 그룹에서 사용자 계정을 제거 하려면 다음 PowerShell 명령 블록을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="49c96-138">To remove a user account from an access group with its display name, use the following PowerShell command block:</span></span>
    
```
$userDisplayName="<display name of the user account>"
$grpName="<display name of the access group>"
Remove-AzureADGroupMember -MemberId (Get-AzureADUser | Where { $_.DisplayName -eq $userDisplayName }).ObjectID -ObjectID (Get-AzureADGroup | Where { $_.DisplayName -eq $grpName }).ObjectID
```

## <a name="remove-a-group"></a><span data-ttu-id="49c96-139">그룹 제거</span><span class="sxs-lookup"><span data-stu-id="49c96-139">Remove a group</span></span>

<span data-ttu-id="49c96-140">전체 그룹에 대 한 액세스 권한을 제거 하려면 사이트에서 해당 사용자의 참여에 따라 현재 구성원 인 그룹을 액세스 그룹에서 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="49c96-140">To remove access for an entire group, you remove the group from the access group for which they are currently a member based on their participation in the site:</span></span>
  
- <span data-ttu-id="49c96-141">관리: site admins 액세스 그룹에서 그룹을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="49c96-141">Administration: Remove the group from the site admins access group</span></span>
    
- <span data-ttu-id="49c96-142">활성 공동 작업: 사이트 구성원 액세스 그룹에서 그룹을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="49c96-142">Active collaboration: Remove the group from the site members access group</span></span>
    
- <span data-ttu-id="49c96-143">보기: 사이트 뷰어 액세스 그룹에서 그룹 제거</span><span class="sxs-lookup"><span data-stu-id="49c96-143">Viewing: Remove the group from the site viewers access group</span></span>
    
<span data-ttu-id="49c96-144">Windows server Active Directory를 통해 사용자 계정 및 그룹을 관리 하는 경우 일반 Windows server AD 사용자 및 그룹 관리 절차를 사용 하 여 적절 한 액세스 그룹에서 적절 한 그룹을 제거 하 고 사용자와의 동기화를 기다립니다. Office 365 구독</span><span class="sxs-lookup"><span data-stu-id="49c96-144">If you are managing user accounts and groups through Windows Server Active Directory, remove the appropriate groups from the appropriate access groups using your normal Windows Server AD user and group management procedures and wait for synchronization with your Office 365 subscription.</span></span>
  
<span data-ttu-id="49c96-145">office 365을 통해 사용자 계정 및 그룹을 관리 하는 경우 office 관리 센터 또는 PowerShell을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="49c96-145">If you are managing user accounts and groups through Office 365, you can use the Office Admin center or PowerShell:</span></span>
  
- <span data-ttu-id="49c96-146">Office 관리 센터의 경우 사용자 계정 관리자 또는 회사 관리자 역할이 할당 된 사용자 계정으로 로그인 하 고 그룹을 사용 하 여 해당 하는 액세스 그룹에서 적절 한 그룹을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="49c96-146">For the Office Admin center, sign in with a user account that has been assigned the User Account Administrator or Company Administrator role and use Groups to remove the appropriate groups from the appropriate access groups.</span></span>
    
- <span data-ttu-id="49c96-147">PowerShell의 경우 먼저 [Azure Active Directory V2 PowerShell 모듈을 사용 하 여 연결](https://go.microsoft.com/fwlink/?linkid=842218)합니다.</span><span class="sxs-lookup"><span data-stu-id="49c96-147">For PowerShell, first [Connect with the Azure Active Directory V2 PowerShell module](https://go.microsoft.com/fwlink/?linkid=842218).</span></span>    
<span data-ttu-id="49c96-148">표시 이름을 사용 하 여 액세스 그룹에서 그룹을 제거 하려면 다음 PowerShell 명령 블록을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="49c96-148">To remove a group from an access group using their display names, use the following PowerShell command block:</span></span>
    
```
$groupMemberName="<display name of the group to remove>"
$grpName="<display name of the access group>"
Remove-AzureADGroupMember -MemberId (Get-AzureADGroup | Where { $_.DisplayName -eq $groupMemberName }).ObjectID -ObjectID (Get-AzureADGroup | Where { $_.DisplayName -eq $grpName }).ObjectID
```

## <a name="create-a-documents-subfolder-with-custom-permissions"></a><span data-ttu-id="49c96-149">사용자 지정 권한으로 문서 하위 폴더 만들기</span><span class="sxs-lookup"><span data-stu-id="49c96-149">Create a documents subfolder with custom permissions</span></span>

<span data-ttu-id="49c96-p104">일부 경우에는 격리 된 사이트 내에서 작업 하는 사용자의 하위 집합에 보다 개인적인 공동 작업을 수행 해야 하는 경우가 있습니다. SharePoint Online 사이트의 경우 사이트의 문서 폴더에 하위 폴더를 만들고 사용자 지정 사용 권한을 할당할 수 있습니다. 사용 권한이 없는 권한은 하위 폴더가 표시 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="49c96-p104">In some cases, a subset of the people working within the isolated site need a more private place to collaborate. For SharePoint Online sites, you can create a subfolder in the Documents folder of the site and assign custom permissions. Those without permissions will not see the subfolder.</span></span>
  
<span data-ttu-id="49c96-153">사용자 지정 사용 권한을 사용 하 여 문서 하위 폴더를 만들려면 다음을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="49c96-153">To create a documents subfolder with custom permissions, do the following:</span></span>
  
1. <span data-ttu-id="49c96-p105">사이트에 대 한 관리자 액세스 그룹의 구성원 인 계정을 사용 하 여 Office 365에 로그인 합니다. 도움말을 보려면 [Office 365에 로그인 하는 위치](https://support.office.com/Article/Where-to-sign-in-to-Office-365-e9eb7d51-5430-4929-91ab-6157c5a050b4)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="49c96-p105">Sign in to Office 365 with an account that is a member of the admins access group for the site. For help, see [Where to sign in to Office 365](https://support.office.com/Article/Where-to-sign-in-to-Office-365-e9eb7d51-5430-4929-91ab-6157c5a050b4).</span></span>
    
2. <span data-ttu-id="49c96-156">격리 된 팀 사이트로 이동 하 여 **문서**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="49c96-156">Go to the isolated team site and click **Documents**.</span></span>
    
3. <span data-ttu-id="49c96-157">사용자 지정 사용 권한이 있는 하위 폴더가 포함 될 문서 폴더의 폴더로 이동 하 여 해당 폴더를 만든 다음 엽니다.</span><span class="sxs-lookup"><span data-stu-id="49c96-157">Browse to the folder in the documents folder that will contain the subfolder with custom permissions, create the folder, and then open it.</span></span>
    
4. <span data-ttu-id="49c96-158">**공유**를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="49c96-158">Click **Share**.</span></span>
    
5. <span data-ttu-id="49c96-159">**> 고급을 사용 하 여 공유를**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="49c96-159">Click **Shared with > Advanced**.</span></span>
    
6. <span data-ttu-id="49c96-160">**사용 권한 상속 중지**를 클릭 하 고 **확인**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="49c96-160">Click **Stop inheriting permissions**, and then click **OK**.</span></span>
    
7. <span data-ttu-id="49c96-161">**공유**를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="49c96-161">Click **Share**.</span></span>
    
8. <span data-ttu-id="49c96-162">**> 고급을 사용 하 여 공유를**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="49c96-162">Click **Shared with > Advanced**.</span></span>
    
9. <span data-ttu-id="49c96-163">**> Advanced와 공유 > 사용 권한 부여를**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="49c96-163">Click **Grant Permissions > Shared with > Advanced**.</span></span>
    
10. <span data-ttu-id="49c96-164">사용 권한 페이지의 \*\* \<목록에서 사이트 name> 구성원\*\*을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="49c96-164">On the permissions page, click **\<site name> Members in the list**.</span></span>
    
11. <span data-ttu-id="49c96-165">사이트 name> 구성원 페이지에서 사이트 구성원 액세스 그룹 옆에 있는 확인 표시를 선택 하 고 **작업**을 클릭 한 다음 **그룹에서 사용자 제거**를 클릭 하 고 **확인**을 클릭 합니다. \*\* \<\*\*</span><span class="sxs-lookup"><span data-stu-id="49c96-165">On the **\<site name> Members** page, select the checkmark next to the site members access group, click **Actions**, click **Remove users from group**, and then click **OK**.</span></span>
    
12. <span data-ttu-id="49c96-166">이 하위 폴더에 특정 구성원을 추가 하려면 **새로 만들기 > 사용자 추가**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="49c96-166">To add specific members to this subfolder, click **New > Add users**.</span></span>
    
13. <span data-ttu-id="49c96-167">**공유** 대화 상자에서 하위 폴더의 파일에 대해 공동 작업할 수 있는 사용자 계정의 이름을 입력 하 고 **공유**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="49c96-167">In the **Share** dialog box, type the names of the user accounts that can collaborate on files in the subfolder, and then click **Share**.</span></span>
    
14. <span data-ttu-id="49c96-168">웹 페이지를 새로 고쳐 새 결과를 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="49c96-168">Refresh the web page to see the new results.</span></span>
    
15. <span data-ttu-id="49c96-169">왼쪽 탐색 창의 **그룹** 에서 \*\* \<site name> 방문자\*\* 그룹을 클릭 하 고, 11-14 단계를 사용 하 여 하위 폴더의 파일을 볼 수 있는 사용자 계정 집합 (필요한 경우)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="49c96-169">Under **Groups** in the left navigation, click the **\<site name> Visitors** group and use steps 11-14 to specify the set of user accounts that can view the files in the subfolder (as needed).</span></span>
    
16. <span data-ttu-id="49c96-170">왼쪽 탐색 창의 **그룹** 에서 \*\* \<site name>\*\* owner 그룹을 클릭 하 고 11-14 단계를 사용 하 여 하위 폴더의 사용 권한을 관리할 수 있는 사용자 계정 집합 (필요한 경우)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="49c96-170">Under **Groups** in the left navigation, click the **\<site name> Owners** group and use steps 11-14 to specify the set of user accounts that can administer the permissions in the subfolder (as needed).</span></span>
    
17. <span data-ttu-id="49c96-171">브라우저에서 **사용자 및 그룹** 탭을 닫습니다.</span><span class="sxs-lookup"><span data-stu-id="49c96-171">Close the **People and Groups** tab in your browser.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="49c96-172">참고 항목</span><span class="sxs-lookup"><span data-stu-id="49c96-172">See Also</span></span>

[<span data-ttu-id="49c96-173">격리된 SharePoint Online 팀 사이트</span><span class="sxs-lookup"><span data-stu-id="49c96-173">Isolated SharePoint Online team sites</span></span>](isolated-sharepoint-online-team-sites.md)
  
[<span data-ttu-id="49c96-174">격리된 SharePoint Online 팀 사이트 디자인</span><span class="sxs-lookup"><span data-stu-id="49c96-174">Design an isolated SharePoint Online team site</span></span>](design-an-isolated-sharepoint-online-team-site.md)

[<span data-ttu-id="49c96-175">격리된 SharePoint Online 팀 사이트 배포</span><span class="sxs-lookup"><span data-stu-id="49c96-175">Deploy an isolated SharePoint Online team site</span></span>](deploy-an-isolated-sharepoint-online-team-site.md)



