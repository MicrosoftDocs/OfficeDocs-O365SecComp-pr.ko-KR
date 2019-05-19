---
title: 격리된 SharePoint Online 팀 사이트 개발/테스트 환경
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
ms.date: 12/15/2017
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: Ent_O365
ms.custom:
- TLG
- Ent_TLGs
ms.assetid: d1795031-beef-49ea-a6fc-5da5450d320d
description: '요약: Office 365 개발/테스트 환경에서 조직의 나머지 부분과 격리 된 SharePoint Online 팀 사이트를 구성 합니다.'
ms.openlocfilehash: 23b734e55e8c68cdc42f41b4e61bdfe152fb01e0
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/17/2019
ms.locfileid: "34152590"
---
# <a name="isolated-sharepoint-online-team-site-devtest-environment"></a><span data-ttu-id="c0289-103">격리된 SharePoint Online 팀 사이트 개발/테스트 환경</span><span class="sxs-lookup"><span data-stu-id="c0289-103">Isolated SharePoint Online team site dev/test environment</span></span>

 <span data-ttu-id="c0289-104">**요약:** Office 365 개발/테스트 환경에서 조직의 나머지 부분과 격리 된 SharePoint Online 팀 사이트를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="c0289-104">**Summary:** Configure a SharePoint Online team site that is isolated from the rest of the organization in your Office 365 dev/test environment.</span></span>
  
<span data-ttu-id="c0289-105">Office 365의 SharePoint Online 팀 사이트는 공통 문서 라이브러리, OneNote 전자 필기장 및 기타 서비스를 사용 하는 공동 작업을 위한 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="c0289-105">SharePoint Online team sites in Office 365 are locations for collaboration using a common document library, a OneNote notebook, and other services.</span></span> <span data-ttu-id="c0289-106">대부분의 경우 부서나 조직 간에 폭넓은 액세스 및 공동 작업을 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c0289-106">In many cases, you want wide access and collaboration across departments or organizations.</span></span> <span data-ttu-id="c0289-107">그러나 경우에 따라 소규모 사용자 그룹 간에 공동 작업 하는 데 필요한 액세스 및 사용 권한을 강력 하 게 제어 하려는 경우도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c0289-107">However, in some cases, you want to tightly control the access and permissions for collaboration among a small group of people.</span></span>
  
<span data-ttu-id="c0289-108">Sharepoint Online 팀 사이트에 대 한 액세스 및 사용자가 수행할 수 있는 작업은 SharePoint 그룹 및 사용 권한 수준에 의해 제어 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c0289-108">Access to SharePoint Online team sites and what users can do is controlled by SharePoint groups and permission levels.</span></span> <span data-ttu-id="c0289-109">기본적으로 SharePoint Online 사이트에는 다음과 같은 세 가지 수준의 액세스 권한이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c0289-109">By default, SharePoint Online sites have three levels of access:</span></span>
  
- <span data-ttu-id="c0289-110">**구성원**-사이트의 리소스를 보고, 만들고, 수정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c0289-110">**Members**, who can view, create, and modify resources on the site.</span></span>
    
- <span data-ttu-id="c0289-111">**소유자**-사용 권한 변경 기능을 비롯 하 여 사이트에 대 한 모든 권한이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c0289-111">**Owners**, who have complete control of the site, including the ability to change permissions.</span></span>
    
- <span data-ttu-id="c0289-112">**방문자**-사이트의 리소스만 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c0289-112">**Visitors**, who only can view resources on the site.</span></span>
    
<span data-ttu-id="c0289-113">이 문서에서는 ProjectX 라는 기밀 조사 프로젝트에 대 한 격리 된 SharePoint Online 팀 사이트의 구성을 단계별로 안내 합니다.</span><span class="sxs-lookup"><span data-stu-id="c0289-113">This article steps you through the configuration of an isolated SharePoint Online team site for a secret research project named ProjectX.</span></span> <span data-ttu-id="c0289-114">액세스 요구 사항은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="c0289-114">The access requirements are:</span></span>
  
- <span data-ttu-id="c0289-115">프로젝트의 구성원만 사이트 및 해당 콘텐츠 (문서, OneNote 전자 필기장, 페이지)에 액세스할 수 있으며, 그룹 구성원을 통해 제어 되는 SharePoint 사용 권한 수준이 편집 및 보기입니다.</span><span class="sxs-lookup"><span data-stu-id="c0289-115">Only members of the project can access the site and its contents (documents, OneNote Notebook, Pages), with edit and view SharePoint permission levels controlled through group membership.</span></span>
    
- <span data-ttu-id="c0289-116">사이트 작성자 및 사이트에 대 한 관리자 그룹의 구성원만 사이트 수준 사용 권한 수정을 포함 하는 사이트 관리를 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c0289-116">Only the site creator and members of an Admins group for the site can perform site administration, which includes modifying site-level permissions.</span></span>
    
<span data-ttu-id="c0289-117">Office 365 개발/테스트 환경에서 격리 된 SharePoint Online 팀 사이트를 설정 하는 세 가지 단계는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="c0289-117">There are three phases to setting up an isolated SharePoint Online team site in your Office 365 dev/test environment:</span></span>
  
1. <span data-ttu-id="c0289-118">Office 365 개발/테스트 환경을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c0289-118">Create the Office 365 dev/test environment.</span></span>
    
2. <span data-ttu-id="c0289-119">ProjectX에 대 한 사용자 및 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c0289-119">Create the users and groups for ProjectX.</span></span>
    
3. <span data-ttu-id="c0289-120">새 ProjectX SharePoint Online 팀 사이트를 만들고 격리 합니다.</span><span class="sxs-lookup"><span data-stu-id="c0289-120">Create a new ProjectX SharePoint Online team site and isolate it.</span></span>
    
> [!TIP]
> <span data-ttu-id="c0289-121">[여기](http://aka.ms/catlgstack)를 클릭하여 One Microsoft 클라우드 테스트 랩 가이드 스택의 모든 문서에 대한 가상 맵을 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c0289-121">Click [here](http://aka.ms/catlgstack) for a visual map to all the articles in the One Microsoft Cloud Test Lab Guide stack.</span></span>
  
## <a name="phase-1-build-out-your-lightweight-or-simulated-enterprise-office-365-devtest-environment"></a><span data-ttu-id="c0289-122">1단계: 경량 또는 시뮬레이트된 엔터프라이즈 Office 365 개발/테스트 환경을 구축합니다.</span><span class="sxs-lookup"><span data-stu-id="c0289-122">Phase 1: Build out your lightweight or simulated enterprise Office 365 dev/test environment</span></span>

<span data-ttu-id="c0289-123">최소 요구 사항과 함께 간단한 방식으로 격리 된 SharePoint Online 팀 사이트를 만들려는 경우에는 [Office 365 개발/테스트 환경의](https://docs.microsoft.com/office365/enterprise/office-365-dev-test-environment)2, 3 단계의 지침을 따릅니다.</span><span class="sxs-lookup"><span data-stu-id="c0289-123">If you just want to create an isolated SharePoint Online team site in a lightweight way with the minimum requirements, follow the instructions in phases 2 and 3 of [Office 365 dev/test environment](https://docs.microsoft.com/office365/enterprise/office-365-dev-test-environment).</span></span>
  
<span data-ttu-id="c0289-124">시뮬레이트된 엔터프라이즈 구성에서 격리 된 SharePoint Online 팀 사이트를 만들려면 [Office 365 개발/테스트 환경용 DirSync](https://docs.microsoft.com/office365/enterprise/dirsync-for-your-office-365-dev-test-environment)의 지침을 따릅니다.</span><span class="sxs-lookup"><span data-stu-id="c0289-124">If you want to create an isolated SharePoint Online team site in a simulated enterprise configuration, follow the instructions in [DirSync for your Office 365 dev/test environment](https://docs.microsoft.com/office365/enterprise/dirsync-for-your-office-365-dev-test-environment).</span></span>
  
> [!NOTE]
> <span data-ttu-id="c0289-125">격리 된 SharePoint Online 사이트를 만드는 경우에는 Windows Server AD 포리스트의 인터넷 및 디렉터리 동기화에 연결 된 시뮬레이트된 인트라넷을 포함 하는 시뮬레이트된 엔터프라이즈 개발/테스트 환경이 필요 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c0289-125">Creating an isolated SharePoint Online site does not require the simulated enterprise dev/test environment, which includes a simulated intranet connected to the Internet and directory synchronization for a Windows Server AD forest.</span></span> <span data-ttu-id="c0289-126">격리 된 SharePoint Online 사이트를 테스트 하 고 일반적인 조직을 나타내는 환경에서 테스트해 볼 수 있도록 여기에서 옵션으로 제공 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c0289-126">It is provided here as an option so that you can test an isolated SharePoint Online site and experiment with it in an environment that represents a typical organization.</span></span> 
  
## <a name="phase-2-create-user-accounts-and-access-groups"></a><span data-ttu-id="c0289-127">2 단계: 사용자 계정 및 액세스 그룹 만들기</span><span class="sxs-lookup"><span data-stu-id="c0289-127">Phase 2: Create user accounts and access groups</span></span>

<span data-ttu-id="c0289-128">[Office 365 PowerShell에 연결](https://technet.microsoft.com/library/dn975125.aspx) 의 지침을 사용 하 여 다음 위치에서 전역 관리자 계정을 사용 하 여 office 365 트레일 구독에 연결 합니다.</span><span class="sxs-lookup"><span data-stu-id="c0289-128">Use the instructions in [Connect to Office 365 PowerShell](https://technet.microsoft.com/library/dn975125.aspx) to connect to your Office 365 trail subscription with your global administrator account from:</span></span>
  
- <span data-ttu-id="c0289-129">사용하는 컴퓨터(경량 Office 365 개발/테스트 환경)</span><span class="sxs-lookup"><span data-stu-id="c0289-129">Your computer (for the lightweight Office 365 dev/test environment).</span></span>
    
- <span data-ttu-id="c0289-130">CLIENT1 가상 컴퓨터(시뮬레이트된 엔터프라이즈 Office 365 개발/테스트 환경)</span><span class="sxs-lookup"><span data-stu-id="c0289-130">The CLIENT1 virtual machine (for the simulated enterprise Office 365 dev/test environment).</span></span>
    
<span data-ttu-id="c0289-131">ProjectX SharePoint Online 팀 사이트에 대 한 새 액세스 그룹을 만들려면 Windows PowerShell 프롬프트에 대 한 Windows Azure Active Directory 모듈에서 다음 명령을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="c0289-131">To create the new access groups for the ProjectX SharePoint Online team site, run these commands from the Windows Azure Active Directory Module for Windows PowerShell prompt:</span></span>
  
```
$groupName="ProjectX-Members"
$groupDesc="People allowed to collaborate for ProjectX."
New-MsolGroup -DisplayName $groupName -Description $groupDesc
$groupName="ProjectX-Admins"
$groupDesc="People allowed to administer SharePoint for ProjectX."
New-MsolGroup -DisplayName $groupName -Description $groupDesc
$groupName="ProjectX-Viewers"
$groupDesc="People allowed to view the SharePoint resources for ProjectX."
New-MsolGroup -DisplayName $groupName -Description $groupDesc
```

> [!TIP]
> <span data-ttu-id="c0289-132">이 문서의 PowerShell 명령을 모두 포함 하는 텍스트 파일을 보려면 [여기](https://gallery.technet.microsoft.com/PowerShell-commands-for-an-b2608df1) 를 클릭 하십시오.</span><span class="sxs-lookup"><span data-stu-id="c0289-132">Click [here](https://gallery.technet.microsoft.com/PowerShell-commands-for-an-b2608df1) for a text file that contains all of the PowerShell commands in this article.</span></span>
  
<span data-ttu-id="c0289-133">조직 이름(예: contosotoycompany), 위치에 대한 2자리 국가 코드를 입력한 후 Windows PowerShell 프롬프트에 대한 Microsoft Azure Active Directory 모듈에서 다음 명령을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="c0289-133">Fill in your organization name (example: contosotoycompany), the two-character country code for your location, and then run the following commands from the Windows Azure Active Directory Module for Windows PowerShell prompt:</span></span>
  
```
$orgName="<organization name>"
$loc="<two-character country code, such as US>"
$licAssignment= $orgName + ":ENTERPRISEPREMIUM"
$userName= "designer@" + $orgName + ".onmicrosoft.com"
New-MsolUser -DisplayName "Lead Designer" -FirstName Lead -LastName Designer -UserPrincipalName $userName -UsageLocation $loc -LicenseAssignment $licAssignment -ForceChangePassword $false
```

<span data-ttu-id="c0289-134">**Get-msoluser** 명령을 표시 하 고 나면 잠재 고객 디자이너 계정에 대해 생성 된 암호를 확인 하 여 안전한 위치에 기록 합니다.</span><span class="sxs-lookup"><span data-stu-id="c0289-134">From the display of the **New-MsolUser** command, note the generated password for the Lead Designer account and record it in a safe location.</span></span>
  
<span data-ttu-id="c0289-135">Windows PowerShell 프롬프트에 대한 Microsoft Azure Active Directory 모듈에서 다음 명령을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="c0289-135">Run the following commands from the Windows Azure Active Directory Module for Windows PowerShell prompt:</span></span>
  
```
$userName= "researcher@" + $orgName + ".onmicrosoft.com"
New-MsolUser -DisplayName "Lead Researcher" -FirstName Lead -LastName Researcher -UserPrincipalName $userName -UsageLocation $loc -LicenseAssignment $licAssignment -ForceChangePassword $false
```

<span data-ttu-id="c0289-136">**Get-msoluser** 명령을 표시할 때 잠재 고객 리서치 도구 계정에 대해 생성 된 암호를 확인 하 고 안전한 위치에 기록 합니다.</span><span class="sxs-lookup"><span data-stu-id="c0289-136">From the display of the **New-MsolUser** command, note the generated password for the Lead Researcher account and record it in a safe location.</span></span>
  
<span data-ttu-id="c0289-137">Windows PowerShell 프롬프트에 대한 Microsoft Azure Active Directory 모듈에서 다음 명령을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="c0289-137">Run the following commands from the Windows Azure Active Directory Module for Windows PowerShell prompt:</span></span>
  
```
$userName= "devvp@" + $orgName + ".onmicrosoft.com"
New-MsolUser -DisplayName "Development VP" -FirstName Development -LastName VP -UserPrincipalName $userName -UsageLocation $loc -LicenseAssignment $licAssignment -ForceChangePassword $false
```

<span data-ttu-id="c0289-138">**Get-msoluser** 명령을 표시할 때 개발 VP 계정에 대해 생성 된 암호를 확인 하 고 안전한 위치에 기록 합니다.</span><span class="sxs-lookup"><span data-stu-id="c0289-138">From the display of the **New-MsolUser** command, note the generated password for the Development VP account and record it in a safe location.</span></span>
  
<span data-ttu-id="c0289-139">다음으로 새 액세스 그룹에 새 계정을 추가 하려면 Windows PowerShell 프롬프트에 대 한 Windows Azure Active Directory 모듈에서 다음 PowerShell 명령을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="c0289-139">Next, to add the new accounts to the new access groups, run these PowerShell commands from the Windows Azure Active Directory Module for Windows PowerShell prompt:</span></span>
  
```
$grpName="ProjectX-Members"
$userUPN="designer@" + $orgName + ".onmicrosoft.com"
Add-MsolGroupMember -GroupObjectId (Get-MsolGroup | Where { $_.DisplayName -eq $grpName }).ObjectID -GroupMemberObjectId (Get-MsolUser | Where { $_.UserPrincipalName -eq $userUPN }).ObjectID -GroupMemberType "User"
$userUPN="researcher@" + $orgName + ".onmicrosoft.com"
Add-MsolGroupMember -GroupObjectId (Get-MsolGroup | Where { $_.DisplayName -eq $grpName }).ObjectID -GroupMemberObjectId (Get-MsolUser | Where { $_.UserPrincipalName -eq $userUPN }).ObjectID -GroupMemberType "User"
$grpName="ProjectX-Admins"
Add-MsolGroupMember -GroupObjectId (Get-MsolGroup | Where { $_.DisplayName -eq $grpName }).ObjectID -GroupMemberObjectId (Get-MsolUser | Where { $_.UserPrincipalName -eq $userCredential.UserName }).ObjectID -GroupMemberType "User"
$grpName="ProjectX-Viewers"
$userUPN="devvp@" + $orgName + ".onmicrosoft.com"
Add-MsolGroupMember -GroupObjectId (Get-MsolGroup | Where { $_.DisplayName -eq $grpName }).ObjectID -GroupMemberObjectId (Get-MsolUser | Where { $_.UserPrincipalName -eq $userUPN }).ObjectID -GroupMemberType "User"
```

<span data-ttu-id="c0289-140">검색</span><span class="sxs-lookup"><span data-stu-id="c0289-140">Results:</span></span>
  
- <span data-ttu-id="c0289-141">ProjectX 구성원 액세스 그룹에는 잠재 고객 디자이너 및 잠재 고객 리서치 도구 사용자 계정이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c0289-141">The ProjectX-Members access group contains the Lead Designer and Lead Researcher user accounts</span></span>
    
- <span data-ttu-id="c0289-142">ProjectX-Admins 액세스 그룹에는 평가판 구독에 대 한 전역 관리자 계정이 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c0289-142">The ProjectX-Admins access group contains the global administrator account for your trial subscription</span></span>
    
- <span data-ttu-id="c0289-143">ProjectX-뷰어 액세스 그룹에는 개발 VP 사용자 계정이 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c0289-143">The ProjectX-Viewers access group contains the Development VP user account</span></span>
    
<span data-ttu-id="c0289-144">그림 1에는 액세스 그룹 및 해당 구성원 자격이 나와 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c0289-144">Figure 1 shows the access groups and their membership.</span></span>
  
<span data-ttu-id="c0289-145">**그림 1**</span><span class="sxs-lookup"><span data-stu-id="c0289-145">**Figure 1**</span></span>

![격리 된 SharePoint Online 그룹 사이트에 대 한 Office 365 그룹 및 해당 구성원 자격](media/5b7373b9-2a80-4880-afe5-63ffb17237e6.png)
  
## <a name="phase-3-create-a-new-projectx-sharepoint-online-team-site-and-isolate-it"></a><span data-ttu-id="c0289-147">3 단계: 새 ProjectX SharePoint Online 팀 사이트를 만들고 격리 합니다.</span><span class="sxs-lookup"><span data-stu-id="c0289-147">Phase 3: Create a new ProjectX SharePoint Online team site and isolate it</span></span>

<span data-ttu-id="c0289-148">ProjectX에 대 한 SharePoint Online 팀 사이트를 만들려면 다음을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="c0289-148">To create a SharePoint Online team site for ProjectX, do the following:</span></span>
  
1. <span data-ttu-id="c0289-149">로컬 컴퓨터 (경량 구성) 또는 CLIENT1 (시뮬레이트된 엔터프라이즈 구성)에서 브라우저를 사용 하 여 전역 관리자 계정을 사용 하 여 Office 365 포털 ([https://admin.microsoft.com](https://admin.microsoft.com))에 로그인 합니다.</span><span class="sxs-lookup"><span data-stu-id="c0289-149">Using a browser on either your local computer (lightweight configuration) or on CLIENT1 (simulated enterprise configuration), sign in to the Office 365 portal ([https://admin.microsoft.com](https://admin.microsoft.com)) using your global administrator account.</span></span>
    
2. <span data-ttu-id="c0289-150">타일 목록에서 **SharePoint**를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="c0289-150">In the list of tiles, click **SharePoint**.</span></span>
    
3. <span data-ttu-id="c0289-151">브라우저의 새 SharePoint 탭에서 **+ 사이트 만들기**를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="c0289-151">On the new SharePoint tab in your browser, click **+ Create site**.</span></span>
    
4. <span data-ttu-id="c0289-152">**팀 사이트 이름**에서 **projectx**를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="c0289-152">In **Team site name**, type **ProjectX**.</span></span> <span data-ttu-id="c0289-153">**개인 정보 설정**에서 **비공개-구성원만이 사이트에 액세스할 수 있습니다**.를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="c0289-153">In **Privacy settings**, select **Private - only members can access this site**.</span></span>
    
5. <span data-ttu-id="c0289-154">**팀 사이트 설명**에서 **projectx에 대 한 SharePoint 사이트**를 입력 하 고 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="c0289-154">In **Team site description**, type **SharePoint site for ProjectX**, and then click **Next**.</span></span>
    
6. <span data-ttu-id="c0289-155">**누가 추가**하 시겠습니까? 창에서 **마침을**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="c0289-155">On the **Who do you want to add**? pane, click **Finish**.</span></span>
    
7. <span data-ttu-id="c0289-156">브라우저의 새 **projectx** 에 있는 도구 모음에서 설정 아이콘을 클릭 한 다음 **사이트 사용 권한을**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="c0289-156">On the new **ProjectX-Home** tab in your browser, in the tool bar, click the settings icon, and then click **Site permissions**.</span></span>
    
8. <span data-ttu-id="c0289-157">**사이트 권한** 창에서 **고급 권한 설정**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="c0289-157">In the **Site permissions** pane, click **Advanced permissions settings**.</span></span>
    
9. <span data-ttu-id="c0289-158">브라우저의 새 **사용 권한: 프로젝트 X** 탭에서 **액세스 요청 설정을**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="c0289-158">In the new **Permissions: Project X** tab in your browser, click **Access Request Settings**.</span></span>
    
10. <span data-ttu-id="c0289-159">**액세스 요청 설정** 대화 상자에서 **구성원이 사이트 및 개별 파일 및 폴더 공유를 허용** 하 고 **액세스 요청 허용** (3 개의 확인란이 모두 선택 취소 됨) 하 고 **확인**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="c0289-159">In the **Access Requests Settings** dialog box, clear **Allow members to share the site and individual files and folders** and **Allow access requests** (so that all three check boxes are cleared), and then click **OK**.</span></span>
    
11. <span data-ttu-id="c0289-160">목록에서 **Projectx Members** 를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="c0289-160">Click **ProjectX Members** in the list.</span></span>
    
12. <span data-ttu-id="c0289-161">**사용자 및 그룹** 페이지에서 **새로 만들기**를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="c0289-161">On the **People and Groups** page, click **New**.</span></span>
    
13. <span data-ttu-id="c0289-162">**공유** 대화 상자에서 **Projectx-Members**를 입력 하 고, 해당 구성원을 선택한 다음, **공유**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="c0289-162">In the **Share** dialog box, type **ProjectX-Members**, select it, and then click **Share**.</span></span>
    
14. <span data-ttu-id="c0289-163">브라우저에서 뒤로 단추를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="c0289-163">Click the back button on your browser.</span></span>
    
15. <span data-ttu-id="c0289-164">목록에서 **Projectx 소유자** 를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="c0289-164">Click **ProjectX Owners** in the list.</span></span>
    
16. <span data-ttu-id="c0289-165">**사용자 및 그룹** 페이지에서 **새로 만들기**를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="c0289-165">On the **People and Groups** page, click **New**.</span></span>
    
17. <span data-ttu-id="c0289-166">**공유** 대화 상자에서 **Projectx-Admins**를 입력 하 고, 해당 파일을 선택한 다음, **공유**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="c0289-166">In the **Share** dialog box, type **ProjectX-Admins**, select it, and then click **Share**.</span></span>
    
18. <span data-ttu-id="c0289-167">브라우저에서 뒤로 단추를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="c0289-167">Click the back button on your browser.</span></span>
    
19. <span data-ttu-id="c0289-168">목록에서 **Projectx 방문자** 를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="c0289-168">Click **ProjectX Visitors** in the list.</span></span>
    
20. <span data-ttu-id="c0289-169">**사용자 및 그룹** 페이지에서 **새로 만들기**를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="c0289-169">On the **People and Groups** page, click **New**.</span></span>
    
21. <span data-ttu-id="c0289-170">**공유** 대화 상자에서 **Projectx-뷰어**를 입력 하 고 선택 하 고 **공유**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="c0289-170">In the **Share** dialog box, type **ProjectX-Viewers**, select it, and then click **Share**.</span></span>
    
22. <span data-ttu-id="c0289-171">브라우저에서 **사용자 및 그룹** 탭을 닫고 브라우저에서 **Projectx-Home** 탭을 클릭 한 다음, **사이트 권한** 창을 닫습니다.</span><span class="sxs-lookup"><span data-stu-id="c0289-171">Close the **People and Groups** tab in your browser, click the **ProjectX-Home** tab in your browser, and then close the **Site permissions** pane.</span></span>
    
<span data-ttu-id="c0289-172">권한 구성의 결과는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="c0289-172">Here are the results of configuring permissions:</span></span>
  
- <span data-ttu-id="c0289-173">ProjectX Members SharePoint 그룹에는 ProjectX-Members 액세스 그룹 (잠재 고객 디자이너 및 잠재 고객 연구원 사용자 계정만 포함)과 ProjectX 그룹 (전역 관리자 사용자 계정만 포함)만 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c0289-173">The ProjectX Members SharePoint group contains only the ProjectX-Members access group (which contains only the Lead Designer and Lead Researcher user accounts) and the ProjectX group (which contains only the global administrator user account).</span></span>
    
- <span data-ttu-id="c0289-174">ProjectX 소유자 SharePoint 그룹에는 ProjectX-Admins 액세스 그룹 (전역 관리자 사용자 계정만 포함)만 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c0289-174">The ProjectX Owners SharePoint group contains only the ProjectX-Admins access group (which contains only the global administrator user account).</span></span>
    
- <span data-ttu-id="c0289-175">ProjectX 방문자 SharePoint 그룹에는 ProjectX-뷰어 액세스 그룹 (개발 VP 사용자 계정만 포함)만 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c0289-175">The ProjectX Visitors SharePoint group contains only the ProjectX-Viewers access group (which contains only the Development VP user account).</span></span>
    
- <span data-ttu-id="c0289-176">구성원은 사이트 수준 권한을 수정할 수 없습니다 (이 작업은 Projectx-Admins 그룹의 구성원만 수행할 수 있음).</span><span class="sxs-lookup"><span data-stu-id="c0289-176">Members cannot modify site-level permissions (this can only be done by members of the ProjectX-Admins group).</span></span>
    
- <span data-ttu-id="c0289-177">다른 사용자 계정은 사이트 또는 해당 리소스에 액세스하거나 사이트에 대한 액세스를 요청할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="c0289-177">Other user accounts cannot access the site or its resources or request access to the site.</span></span>
    
<span data-ttu-id="c0289-178">그림 2는 SharePoint 그룹 및 해당 구성원 자격을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="c0289-178">Figure 2 shows the SharePoint groups and their membership.</span></span>
  
<span data-ttu-id="c0289-179">**그림 2**</span><span class="sxs-lookup"><span data-stu-id="c0289-179">**Figure 2**</span></span>

![SharePoint Online 그룹 및 격리 된 SharePoint Online 그룹 사이트에 대 한 구성원 자격](media/595abff4-64f9-49de-a37a-c70c6856936b.png)
  
<span data-ttu-id="c0289-181">이제 수석 디자이너 사용자 계정을 사용 하 여 액세스 방법을 살펴보겠습니다.</span><span class="sxs-lookup"><span data-stu-id="c0289-181">Now let's demonstrate access using the Lead Designer user account:</span></span>
  
1. <span data-ttu-id="c0289-182">브라우저에서 **Projectx-home** 탭을 닫고 브라우저에서 **Microsoft Office Home** 탭을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="c0289-182">Close the **ProjectX-Home** tab in your browser, and then click the **Microsoft Office Home** tab in your browser.</span></span>
    
2. <span data-ttu-id="c0289-183">전역 관리자의 이름을 클릭 하 고 **로그 아웃**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="c0289-183">Click the name of your global administrator, and then click **Sign out**.</span></span>
    
3. <span data-ttu-id="c0289-184">잠재 고객 디자이너 계정 이름 및 암호를[https://admin.microsoft.com](https://admin.microsoft.com)사용 하 여 Office 365 portal ()에 로그인 합니다.</span><span class="sxs-lookup"><span data-stu-id="c0289-184">Sign in to the Office 365 portal ([https://admin.microsoft.com](https://admin.microsoft.com)) using the Lead Designer account name and its password.</span></span>
    
4. <span data-ttu-id="c0289-185">타일 목록에서 **SharePoint**를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="c0289-185">In the list of tiles, click **SharePoint**.</span></span>
    
5. <span data-ttu-id="c0289-186">브라우저의 새 **SharePoint** 탭에 있는 검색 상자에 **projectx** 를 입력 하 고 검색을 활성화 한 다음 **projectx** 팀 사이트를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="c0289-186">On the new **SharePoint** tab in your browser, type **ProjectX** in the search box, activate the search, and then click the **ProjectX** team site.</span></span> <span data-ttu-id="c0289-187">ProjectX 팀 사이트에 대 한 브라우저에 새 탭이 표시 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c0289-187">You should see a new tab in your browser for the ProjectX team site.</span></span>
    
6. <span data-ttu-id="c0289-188">설정 아이콘을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="c0289-188">Click the settings icon.</span></span> <span data-ttu-id="c0289-189">**사이트 사용 권한에**대 한 옵션이 없는 것을 알 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c0289-189">Notice that there is no option for **Site Permissions**.</span></span> <span data-ttu-id="c0289-190">Projectxadmins 그룹의 구성원만이 사이트에 대 한 사용 권한을 수정할 수 있기 때문에 이것은 올바릅니다.</span><span class="sxs-lookup"><span data-stu-id="c0289-190">This is correct because only the members of the ProjectX-Admins group can modify permissions on the site</span></span>
    
7. <span data-ttu-id="c0289-191">메모장 또는 원하는 텍스트 편집기를 엽니다.</span><span class="sxs-lookup"><span data-stu-id="c0289-191">Open Notepad or a text editor of your choice.</span></span>
    
8. <span data-ttu-id="c0289-192">ProjectX 팀 사이트의 URL을 복사 하 여 메모장 이나 텍스트 편집기에서 새 줄에 붙여 넣습니다.</span><span class="sxs-lookup"><span data-stu-id="c0289-192">Copy the URL of the ProjectX team site and paste it on a new line in Notepad or your text editor.</span></span>
    
9. <span data-ttu-id="c0289-193">브라우저의 새 **Projectx-홈** 탭에서 **문서**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="c0289-193">On the new **ProjectX-Home** tab in your browser, click **Documents**.</span></span>
    
10. <span data-ttu-id="c0289-194">ProjectX documents 폴더의 URL을 복사 하 여 메모장 이나 텍스트 편집기에서 새 줄에 붙여 넣습니다.</span><span class="sxs-lookup"><span data-stu-id="c0289-194">Copy the URL of the ProjectX documents folder and paste it on a new line in Notepad or your text editor.</span></span>
    
11. <span data-ttu-id="c0289-195">브라우저의 새 **Projectx-문서** 탭에서 **새 > Word 문서**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="c0289-195">On the new **ProjectX-Documents** tab in your browser, click **New > Word document**.</span></span>
    
12. <span data-ttu-id="c0289-196">**Word Online** 페이지에서 텍스트를 입력 하 고 상태를 **저장할**때까지 기다렸다가 브라우저에서 뒤로 단추를 클릭 한 다음 페이지를 새로 고칩니다.</span><span class="sxs-lookup"><span data-stu-id="c0289-196">Type some text in the **Word Online** page, wait for the status to indicate **Saved**, click the back button on your browser, and then refresh the page.</span></span> <span data-ttu-id="c0289-197">**문서** 폴더에 새 **문서 .docx** 가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c0289-197">You should see a new **Document.docx** in the **Documents** folder.</span></span>
    
13. <span data-ttu-id="c0289-198">**문서 .docx** 문서의 줄임표를 클릭 한 다음 **링크 가져오기를**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="c0289-198">Click the ellipsis for the **Document.docx** document, and then click **Get a link**.</span></span>
    
14. <span data-ttu-id="c0289-199">**공유의 ' 문서 .docx '** 대화 상자에 URL을 복사 하 여 메모장 이나 텍스트 편집기에서 새 줄에 붙여 넣은 다음 **공유 ' 문서 .docx '** 대화 상자를 닫습니다.</span><span class="sxs-lookup"><span data-stu-id="c0289-199">Copy the URL in the **Share 'Document.docx'** dialog box and paste it on a new line in Notepad or your text editor, and then close the **Share 'Document.docx'** dialog box.</span></span>
    
15. <span data-ttu-id="c0289-200">브라우저에서 **Projectx-문서** 및 **SharePoint** 탭을 닫고 **Microsoft Office 홈** 탭을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="c0289-200">Close the **ProjectX-Documents** and **SharePoint** tabs in your browser, and then click the **Microsoft Office Home** tab.</span></span>
    
16. <span data-ttu-id="c0289-201">**잠재 고객 디자이너** 이름을 클릭 하 고 **로그 아웃**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="c0289-201">Click the **Lead Designer** name, and then click **Sign out**.</span></span>
    
<span data-ttu-id="c0289-202">이제 개발 VP 사용자 계정을 사용 하 여 액세스 방법을 살펴보겠습니다.</span><span class="sxs-lookup"><span data-stu-id="c0289-202">Now let's demonstrate access using the Development VP user account:</span></span>
  
1. <span data-ttu-id="c0289-203">개발 VP 계정 이름 및 암호를 사용[https://admin.microsoft.com](https://admin.microsoft.com)하 여 Office 365 portal ()에 로그인 합니다.</span><span class="sxs-lookup"><span data-stu-id="c0289-203">Sign in to the Office 365 portal ([https://admin.microsoft.com](https://admin.microsoft.com)) using the Development VP account name and its password.</span></span>
    
2. <span data-ttu-id="c0289-204">타일 목록에서 **SharePoint**를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="c0289-204">In the list of tiles, click **SharePoint**.</span></span>
    
3. <span data-ttu-id="c0289-205">브라우저의 새 **SharePoint** 탭에 있는 검색 상자에 **projectx** 를 입력 하 고 검색을 활성화 한 다음 **projectx** 팀 사이트를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="c0289-205">On the new **SharePoint** tab in your browser, type **ProjectX** in the search box, activate the search, and then click the **ProjectX** team site.</span></span> <span data-ttu-id="c0289-206">ProjectX 팀 사이트에 대 한 브라우저에 새 탭이 표시 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c0289-206">You should see a new tab in your browser for the ProjectX team site.</span></span>
    
4. <span data-ttu-id="c0289-207">**문서**를 클릭 한 다음 **문서 .docx** 파일을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="c0289-207">Click **Documents**, and then click the **Document.docx** file.</span></span>
    
5. <span data-ttu-id="c0289-208">브라우저의 **.docx** 탭에서 텍스트를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c0289-208">In the **Document.docx** tab in your browser, try to modify the text.</span></span> <span data-ttu-id="c0289-209">**이 문서는 읽기 전용** 이라는 메시지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c0289-209">You should see a message stating **This document is read-only.**</span></span> <span data-ttu-id="c0289-210">이는 개발 VP 사용자 계정에 사이트에 대 한 보기 권한만 있다는 이유로 예상 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c0289-210">This is expected because the Development VP user account only has view permissions for the site.</span></span>
    
6. <span data-ttu-id="c0289-211">브라우저에서 **문서 .docx**, **projectx-문서**및 **SharePoint** 탭을 닫습니다.</span><span class="sxs-lookup"><span data-stu-id="c0289-211">Close the **Document.docx**, **ProjectX-Documents**, and **SharePoint** tabs in your browser.</span></span>
    
7. <span data-ttu-id="c0289-212">**Microsoft Office 홈** 탭을 클릭 하 고 **개발 VP** 이름을 클릭 한 다음 **로그 아웃**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="c0289-212">Click the **Microsoft Office Home** tab, click the **Development VP** name, and then click **Sign out**.</span></span>
    
<span data-ttu-id="c0289-213">이제 사용 권한이 없는 사용자 계정을 사용 하 여 액세스 하는 방법을 알아보겠습니다.</span><span class="sxs-lookup"><span data-stu-id="c0289-213">Now let's demonstrate access with a user account that has no permissions:</span></span>
  
1. <span data-ttu-id="c0289-214">사용자 3 계정 이름 및 암호를 사용[https://admin.microsoft.com](https://admin.microsoft.com)하 여 Office 365 portal ()에 로그인 합니다.</span><span class="sxs-lookup"><span data-stu-id="c0289-214">Sign in to the Office 365 portal ([https://admin.microsoft.com](https://admin.microsoft.com)) using the User 3 account name and its password.</span></span>
    
2. <span data-ttu-id="c0289-215">타일 목록에서 **SharePoint**를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="c0289-215">In the list of tiles, click **SharePoint**.</span></span>
    
3. <span data-ttu-id="c0289-216">브라우저의 새 **SharePoint** 탭에 있는 검색 상자에 **projectx** 를 입력 한 다음 검색을 활성화 합니다.</span><span class="sxs-lookup"><span data-stu-id="c0289-216">On the new **SharePoint** tab in your browser, type **ProjectX** in the search box and then activate the search.</span></span> <span data-ttu-id="c0289-217">**검색 조건과 일치** 하는 메시지가 없는 것을 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c0289-217">You should see the message **Nothing here matches your search.**</span></span>
    
4. <span data-ttu-id="c0289-218">메모장의 열린 인스턴스나 텍스트 편집기에서 ProjectX 사이트의 URL을 브라우저의 주소 표시줄에 복사한 다음 enter 키를 누릅니다. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="c0289-218">From the open instance of Notepad or your text editor, copy the URL for the ProjectX site into the address bar of your browser and press **Enter**.</span></span> <span data-ttu-id="c0289-219">**액세스 거부** 페이지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c0289-219">You should see an **Access Denied** page.</span></span>
    
5. <span data-ttu-id="c0289-220">메모장 이나 텍스트 편집기에서 ProjectX Documents 폴더의 URL을 브라우저의 주소 표시줄에 복사 하 고 enter 키를 누릅니다. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="c0289-220">From Notepad or your text editor, copy the URL for the ProjectX Documents folder into the address bar of your browser and press **Enter**.</span></span> <span data-ttu-id="c0289-221">**액세스 거부** 페이지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c0289-221">You should see an **Access Denied** page.</span></span>
    
6. <span data-ttu-id="c0289-222">메모장 이나 텍스트 편집기에서 문서 .docx 파일의 URL을 브라우저의 주소 표시줄에 복사한 다음 enter 키를 누릅니다. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="c0289-222">From Notepad or your text editor, copy the URL for the Documents.docx file into the address bar of your browser and press **Enter**.</span></span> <span data-ttu-id="c0289-223">**액세스 거부** 페이지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c0289-223">You should see an **Access Denied** page.</span></span>
    
7. <span data-ttu-id="c0289-224">브라우저에서 **SharePoint** 탭을 닫고 **Microsoft Office 홈** 탭을 클릭 한 다음 **사용자 3** 이름을 클릭 하 고 **로그 아웃**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="c0289-224">Close the **SharePoint** tab in your browser, click the **Microsoft Office Home** tab, click the **User 3** name, and then click **Sign out**.</span></span>
    
<span data-ttu-id="c0289-225">이제 격리 된 SharePoint Online 사이트에 대 한 추가 실험 준비가 완료 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c0289-225">Your isolated SharePoint Online site is now ready for your additional experimentation.</span></span>
  
## <a name="next-step"></a><span data-ttu-id="c0289-226">다음 단계</span><span class="sxs-lookup"><span data-stu-id="c0289-226">Next Step</span></span>

<span data-ttu-id="c0289-227">프로덕션 환경에 격리된 SharePoint Online 팀 사이트를 배포할 준비가 되면 [격리된 SharePoint Online 팀 사이트 디자인](design-an-isolated-sharepoint-online-team-site.md)에서 단계별 디자인 고려 사항을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="c0289-227">When you are ready to deploy an isolated SharePoint Online team site in production, see the step-by-step design considerations in [Design an isolated SharePoint Online team site](design-an-isolated-sharepoint-online-team-site.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="c0289-228">참고 항목</span><span class="sxs-lookup"><span data-stu-id="c0289-228">See Also</span></span>

[<span data-ttu-id="c0289-229">격리된 SharePoint Online 팀 사이트</span><span class="sxs-lookup"><span data-stu-id="c0289-229">Isolated SharePoint Online team sites</span></span>](isolated-sharepoint-online-team-sites.md)
  
[<span data-ttu-id="c0289-230">클라우드 도입 TLG(테스트 랩 가이드)</span><span class="sxs-lookup"><span data-stu-id="c0289-230">Cloud adoption Test Lab Guides (TLGs)</span></span>](https://docs.microsoft.com/office365/enterprise/cloud-adoption-test-lab-guides-tlgs)
  
[<span data-ttu-id="c0289-231">기본 구성 개발/테스트 환경</span><span class="sxs-lookup"><span data-stu-id="c0289-231">Base Configuration dev/test environment</span></span>](https://docs.microsoft.com/office365/enterprise/base-configuration-dev-test-environment)
  
[<span data-ttu-id="c0289-232">Office 365 개발/테스트 환경</span><span class="sxs-lookup"><span data-stu-id="c0289-232">Office 365 dev/test environment</span></span>](https://docs.microsoft.com/office365/enterprise/office-365-dev-test-environment)
  
[<span data-ttu-id="c0289-233">클라우드 도입 및 하이브리드 솔루션</span><span class="sxs-lookup"><span data-stu-id="c0289-233">Cloud adoption and hybrid solutions</span></span>](https://docs.microsoft.com/office365/enterprise/cloud-adoption-and-hybrid-solutions)




