---
title: 격리된 SharePoint Online 팀 사이트 개발/테스트 환경
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
ms.date: 12/15/2017
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: Ent_O365
ms.custom:
- TLG
- Ent_TLGs
ms.assetid: d1795031-beef-49ea-a6fc-5da5450d320d
description: '요약: Office 365 개발/테스트 환경에서 조직의 나머지 부분과 격리 된 SharePoint Online 팀 사이트를 구성 합니다.'
ms.openlocfilehash: a8a02c10f799b136b299801a3636820e4f64e087
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30217138"
---
# <a name="isolated-sharepoint-online-team-site-devtest-environment"></a><span data-ttu-id="9f3b3-103">격리된 SharePoint Online 팀 사이트 개발/테스트 환경</span><span class="sxs-lookup"><span data-stu-id="9f3b3-103">Isolated SharePoint Online team site dev/test environment</span></span>

 <span data-ttu-id="9f3b3-104">**요약:** Office 365 개발/테스트 환경에서 조직의 나머지 부분과 격리 된 SharePoint Online 팀 사이트를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="9f3b3-104">**Summary:** Configure a SharePoint Online team site that is isolated from the rest of the organization in your Office 365 dev/test environment.</span></span>
  
<span data-ttu-id="9f3b3-p101">Office 365의 SharePoint Online 팀 사이트는 공통 문서 라이브러리, OneNote 전자 필기장 및 기타 서비스를 사용 하는 공동 작업을 위한 위치입니다. 대부분의 경우 부서나 조직 간에 폭넓은 액세스 및 공동 작업을 수행할 수 있습니다. 그러나 경우에 따라 소규모 사용자 그룹 간에 공동 작업 하는 데 필요한 액세스 및 사용 권한을 강력 하 게 제어 하려는 경우도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9f3b3-p101">SharePoint Online team sites in Office 365 are locations for collaboration using a common document library, a OneNote notebook, and other services. In many cases, you want wide access and collaboration across departments or organizations. However, in some cases, you want to tightly control the access and permissions for collaboration among a small group of people.</span></span>
  
<span data-ttu-id="9f3b3-p102">sharepoint Online 팀 사이트에 대 한 액세스 및 사용자가 수행할 수 있는 작업은 sharepoint 그룹 및 사용 권한 수준에 의해 제어 됩니다. 기본적으로 SharePoint Online 사이트에는 다음과 같은 세 가지 수준의 액세스 권한이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9f3b3-p102">Access to SharePoint Online team sites and what users can do is controlled by SharePoint groups and permission levels. By default, SharePoint Online sites have three levels of access:</span></span>
  
- <span data-ttu-id="9f3b3-110">**구성원**: 사이트의 리소스를 보고, 만들고, 수정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9f3b3-110">**Members**, who can view, create, and modify resources on the site.</span></span>
    
- <span data-ttu-id="9f3b3-111">**소유자**: 권한 변경 기능을 비롯하여 사이트를 완전히 제어할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9f3b3-111">**Owners**, who have complete control of the site, including the ability to change permissions.</span></span>
    
- <span data-ttu-id="9f3b3-112">**방문자**: 사이트의 리소스를 볼 수만 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9f3b3-112">**Visitors**, who only can view resources on the site.</span></span>
    
<span data-ttu-id="9f3b3-p103">이 문서에서는 projectx 라는 기밀 조사 프로젝트에 대 한 격리 된 SharePoint Online 팀 사이트의 구성을 단계별로 안내 합니다. 액세스 요구 사항은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="9f3b3-p103">This article steps you through the configuration of an isolated SharePoint Online team site for a secret research project named ProjectX. The access requirements are:</span></span>
  
- <span data-ttu-id="9f3b3-115">프로젝트의 구성원만 사이트 및 해당 콘텐츠(문서, OneNote 전자 필기장, 페이지)에 액세스할 수 있고, SharePoint 편집 및 보기 권한 수준은 그룹 구성원 자격을 통해 제어됩니다.</span><span class="sxs-lookup"><span data-stu-id="9f3b3-115">Only members of the project can access the site and its contents (documents, OneNote Notebook, Pages), with edit and view SharePoint permission levels controlled through group membership.</span></span>
    
- <span data-ttu-id="9f3b3-116">사이트의 사이트 작성자 및 관리자 그룹의 구성원만 사이트 수준 권한 수정을 비롯한 사이트 관리 작업을 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9f3b3-116">Only the site creator and members of an Admins group for the site can perform site administration, which includes modifying site-level permissions.</span></span>
    
<span data-ttu-id="9f3b3-117">Office 365 개발/테스트 환경에서 격리 된 SharePoint Online 팀 사이트를 설정 하는 세 가지 단계는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="9f3b3-117">There are three phases to setting up an isolated SharePoint Online team site in your Office 365 dev/test environment:</span></span>
  
1. <span data-ttu-id="9f3b3-118">Office 365 개발/테스트 환경을 만듭니다.
</span><span class="sxs-lookup"><span data-stu-id="9f3b3-118">Create the Office 365 dev/test environment.</span></span>
    
2. <span data-ttu-id="9f3b3-119">ProjectX에 대한 사용자 및 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9f3b3-119">Create the users and groups for ProjectX.</span></span>
    
3. <span data-ttu-id="9f3b3-120">새 projectx SharePoint Online 팀 사이트를 만들고 격리 합니다.</span><span class="sxs-lookup"><span data-stu-id="9f3b3-120">Create a new ProjectX SharePoint Online team site and isolate it.</span></span>
    
> [!TIP]
> <span data-ttu-id="9f3b3-121">[여기](http://aka.ms/catlgstack)를 클릭하여 One Microsoft 클라우드 테스트 랩 가이드 스택의 모든 문서에 대한 가상 맵을 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9f3b3-121">Click [here](http://aka.ms/catlgstack) for a visual map to all the articles in the One Microsoft Cloud Test Lab Guide stack.</span></span>
  
## <a name="phase-1-build-out-your-lightweight-or-simulated-enterprise-office-365-devtest-environment"></a><span data-ttu-id="9f3b3-122">1단계: 경량 또는 시뮬레이트된 엔터프라이즈 Office 365 개발/테스트 환경을 구축합니다.</span><span class="sxs-lookup"><span data-stu-id="9f3b3-122">Phase 1: Build out your lightweight or simulated enterprise Office 365 dev/test environment</span></span>

<span data-ttu-id="9f3b3-123">최소 요구 사항과 함께 간단한 방식으로 격리 된 SharePoint Online 팀 사이트를 만들려는 경우에는 [Office 365 개발/테스트 환경의](https://docs.microsoft.com/office365/enterprise/office-365-dev-test-environment)2, 3 단계의 지침을 따릅니다.</span><span class="sxs-lookup"><span data-stu-id="9f3b3-123">If you just want to create an isolated SharePoint Online team site in a lightweight way with the minimum requirements, follow the instructions in phases 2 and 3 of [Office 365 dev/test environment](https://docs.microsoft.com/office365/enterprise/office-365-dev-test-environment).</span></span>
  
<span data-ttu-id="9f3b3-124">시뮬레이트된 엔터프라이즈 구성에서 격리 된 SharePoint Online 팀 사이트를 만들려면 [Office 365 개발/테스트 환경용 DirSync](https://docs.microsoft.com/office365/enterprise/dirsync-for-your-office-365-dev-test-environment)의 지침을 따릅니다.</span><span class="sxs-lookup"><span data-stu-id="9f3b3-124">If you want to create an isolated SharePoint Online team site in a simulated enterprise configuration, follow the instructions in [DirSync for your Office 365 dev/test environment](https://docs.microsoft.com/office365/enterprise/dirsync-for-your-office-365-dev-test-environment).</span></span>
  
> [!NOTE]
> <span data-ttu-id="9f3b3-p104">격리된 SharePoint Online 사이트를 만들기 위해 시뮬레이트된 엔터프라이즈 개발/테스트 환경이 필요하지 않습니다. 해당 환경에는 Windows Server AD 포리스트의 디렉터리 동기화 및 인터넷에 연결된 시뮬레이트된 인트라넷이 포함되어 있습니다. 여기서는 옵션으로 제공되므로 격리된 SharePoint Online 사이트를 테스트하고 일반적인 조직을 나타내는 환경에서 실험할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9f3b3-p104">Creating an isolated SharePoint Online site does not require the simulated enterprise dev/test environment, which includes a simulated intranet connected to the Internet and directory synchronization for a Windows Server AD forest. It is provided here as an option so that you can test an isolated SharePoint Online site and experiment with it in an environment that represents a typical organization.</span></span> 
  
## <a name="phase-2-create-user-accounts-and-access-groups"></a><span data-ttu-id="9f3b3-127">2 단계: 사용자 계정 및 액세스 그룹 만들기</span><span class="sxs-lookup"><span data-stu-id="9f3b3-127">Phase 2: Create user accounts and access groups</span></span>

<span data-ttu-id="9f3b3-128">[office 365 PowerShell에 연결](https://technet.microsoft.com/library/dn975125.aspx) 의 지침을 사용 하 여 다음 위치에서 전역 관리자 계정을 사용 하 여 office 365 트레일 구독에 연결 합니다.</span><span class="sxs-lookup"><span data-stu-id="9f3b3-128">Use the instructions in [Connect to Office 365 PowerShell](https://technet.microsoft.com/library/dn975125.aspx) to connect to your Office 365 trail subscription with your global administrator account from:</span></span>
  
- <span data-ttu-id="9f3b3-129">사용하는 컴퓨터(경량 Office 365 개발/테스트 환경)</span><span class="sxs-lookup"><span data-stu-id="9f3b3-129">Your computer (for the lightweight Office 365 dev/test environment).</span></span>
    
- <span data-ttu-id="9f3b3-130">CLIENT1 가상 컴퓨터(시뮬레이트된 엔터프라이즈 Office 365 개발/테스트 환경)</span><span class="sxs-lookup"><span data-stu-id="9f3b3-130">The CLIENT1 virtual machine (for the simulated enterprise Office 365 dev/test environment).</span></span>
    
<span data-ttu-id="9f3b3-131">projectx SharePoint Online 팀 사이트에 대 한 새 액세스 그룹을 만들려면 windows PowerShell 프롬프트에 대 한 windows Azure Active Directory 모듈에서 다음 명령을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="9f3b3-131">To create the new access groups for the ProjectX SharePoint Online team site, run these commands from the Windows Azure Active Directory Module for Windows PowerShell prompt:</span></span>
  
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
> <span data-ttu-id="9f3b3-132">이 문서의 PowerShell 명령을 모두 포함 하는 텍스트 파일을 보려면 [여기](https://gallery.technet.microsoft.com/PowerShell-commands-for-an-b2608df1) 를 클릭 하십시오.</span><span class="sxs-lookup"><span data-stu-id="9f3b3-132">Click [here](https://gallery.technet.microsoft.com/PowerShell-commands-for-an-b2608df1) for a text file that contains all of the PowerShell commands in this article.</span></span>
  
<span data-ttu-id="9f3b3-133">조직 이름(예: contosotoycompany), 위치에 대한 2자리 국가 코드를 입력한 후 Windows PowerShell 프롬프트에 대한 Microsoft Azure Active Directory 모듈에서 다음 명령을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="9f3b3-133">Fill in your organization name (example: contosotoycompany), the two-character country code for your location, and then run the following commands from the Windows Azure Active Directory Module for Windows PowerShell prompt:</span></span>
  
```
$orgName="<organization name>"
$loc="<two-character country code, such as US>"
$licAssignment= $orgName + ":ENTERPRISEPREMIUM"
$userName= "designer@" + $orgName + ".onmicrosoft.com"
New-MsolUser -DisplayName "Lead Designer" -FirstName Lead -LastName Designer -UserPrincipalName $userName -UsageLocation $loc -LicenseAssignment $licAssignment -ForceChangePassword $false
```

<span data-ttu-id="9f3b3-134">**New-MsolUser** 명령 표시에서 Lead Designer 계정에 대해 생성된 암호를 적어둔 후 안전한 위치에 보관합니다.</span><span class="sxs-lookup"><span data-stu-id="9f3b3-134">From the display of the **New-MsolUser** command, note the generated password for the Lead Designer account and record it in a safe location.</span></span>
  
<span data-ttu-id="9f3b3-135">Windows PowerShell 프롬프트에 대한 Microsoft Azure Active Directory 모듈에서 다음 명령을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="9f3b3-135">Run the following commands from the Windows Azure Active Directory Module for Windows PowerShell prompt:</span></span>
  
```
$userName= "researcher@" + $orgName + ".onmicrosoft.com"
New-MsolUser -DisplayName "Lead Researcher" -FirstName Lead -LastName Researcher -UserPrincipalName $userName -UsageLocation $loc -LicenseAssignment $licAssignment -ForceChangePassword $false
```

<span data-ttu-id="9f3b3-136">**New-MsolUser** 명령 표시에서 Lead Researcher 계정에 대해 생성된 암호를 적어둔 후 안전한 위치에 보관합니다.</span><span class="sxs-lookup"><span data-stu-id="9f3b3-136">From the display of the **New-MsolUser** command, note the generated password for the Lead Researcher account and record it in a safe location.</span></span>
  
<span data-ttu-id="9f3b3-137">Windows PowerShell 프롬프트에 대한 Microsoft Azure Active Directory 모듈에서 다음 명령을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="9f3b3-137">Run the following commands from the Windows Azure Active Directory Module for Windows PowerShell prompt:</span></span>
  
```
$userName= "devvp@" + $orgName + ".onmicrosoft.com"
New-MsolUser -DisplayName "Development VP" -FirstName Development -LastName VP -UserPrincipalName $userName -UsageLocation $loc -LicenseAssignment $licAssignment -ForceChangePassword $false
```

<span data-ttu-id="9f3b3-138">**New-MsolUser** 명령 표시에서 Development VP 계정에 대해 생성된 암호를 적어둔 후 안전한 위치에 보관합니다.</span><span class="sxs-lookup"><span data-stu-id="9f3b3-138">From the display of the **New-MsolUser** command, note the generated password for the Development VP account and record it in a safe location.</span></span>
  
<span data-ttu-id="9f3b3-139">다음으로 새 액세스 그룹에 새 계정을 추가 하려면 windows powershell 프롬프트에 대 한 windows Azure Active Directory 모듈에서 다음 PowerShell 명령을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="9f3b3-139">Next, to add the new accounts to the new access groups, run these PowerShell commands from the Windows Azure Active Directory Module for Windows PowerShell prompt:</span></span>
  
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

<span data-ttu-id="9f3b3-140">결과:</span><span class="sxs-lookup"><span data-stu-id="9f3b3-140">Results:</span></span>
  
- <span data-ttu-id="9f3b3-141">projectx 구성원 액세스 그룹에는 잠재 고객 디자이너 및 잠재 고객 리서치 도구 사용자 계정이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9f3b3-141">The ProjectX-Members access group contains the Lead Designer and Lead Researcher user accounts</span></span>
    
- <span data-ttu-id="9f3b3-142">projectx-Admins 액세스 그룹에는 평가판 구독에 대 한 전역 관리자 계정이 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9f3b3-142">The ProjectX-Admins access group contains the global administrator account for your trial subscription</span></span>
    
- <span data-ttu-id="9f3b3-143">projectx-뷰어 액세스 그룹에는 개발 VP 사용자 계정이 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9f3b3-143">The ProjectX-Viewers access group contains the Development VP user account</span></span>
    
<span data-ttu-id="9f3b3-144">그림 1에는 액세스 그룹 및 해당 구성원 자격이 나와 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9f3b3-144">Figure 1 shows the access groups and their membership.</span></span>
  
<span data-ttu-id="9f3b3-145">**그림 1**</span><span class="sxs-lookup"><span data-stu-id="9f3b3-145">**Figure 1**</span></span>

![Office 365 그룹 및 격리된 SharePoint Online 그룹 사이트에 대한 멤버 자격](media/5b7373b9-2a80-4880-afe5-63ffb17237e6.png)
  
## <a name="phase-3-create-a-new-projectx-sharepoint-online-team-site-and-isolate-it"></a><span data-ttu-id="9f3b3-147">3 단계: 새 projectx SharePoint Online 팀 사이트를 만들고 격리 합니다.</span><span class="sxs-lookup"><span data-stu-id="9f3b3-147">Phase 3: Create a new ProjectX SharePoint Online team site and isolate it</span></span>

<span data-ttu-id="9f3b3-148">projectx에 대 한 SharePoint Online 팀 사이트를 만들려면 다음을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="9f3b3-148">To create a SharePoint Online team site for ProjectX, do the following:</span></span>
  
1. <span data-ttu-id="9f3b3-149">로컬 컴퓨터 (경량 구성) 또는 CLIENT1 (시뮬레이트된 엔터프라이즈 구성)에서 브라우저를 사용 하 여 전역 관리자 계정을 사용 하 여 Office 365 포털 ([https://portal.office.com](https://portal.office.com))에 로그인 합니다.</span><span class="sxs-lookup"><span data-stu-id="9f3b3-149">Using a browser on either your local computer (lightweight configuration) or on CLIENT1 (simulated enterprise configuration), sign in to the Office 365 portal ([https://portal.office.com](https://portal.office.com)) using your global administrator account.</span></span>
    
2. <span data-ttu-id="9f3b3-150">타일 목록에서 **SharePoint**를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="9f3b3-150">In the list of tiles, click **SharePoint**.</span></span>
    
3. <span data-ttu-id="9f3b3-151">브라우저의 새 SharePoint 탭에서 **+ 사이트 만들기**를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="9f3b3-151">On the new SharePoint tab in your browser, click **+ Create site**.</span></span>
    
4. <span data-ttu-id="9f3b3-p105">**팀 사이트 이름**에서 **projectx**를 입력 합니다. **개인 정보 설정**에서 **비공개-구성원만이 사이트에 액세스할 수 있습니다**.를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="9f3b3-p105">In **Team site name**, type **ProjectX**. In **Privacy settings**, select **Private - only members can access this site**.</span></span>
    
5. <span data-ttu-id="9f3b3-154">**팀 사이트 설명**에서 **ProjectX에 대한 SharePoint 사이트**를 입력하고 **다음**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="9f3b3-154">In **Team site description**, type **SharePoint site for ProjectX**, and then click **Next**.</span></span>
    
6. <span data-ttu-id="9f3b3-155">**누가 추가**하 시겠습니까? 창에서 **마침을**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="9f3b3-155">On the **Who do you want to add**? pane, click **Finish**.</span></span>
    
7. <span data-ttu-id="9f3b3-156">브라우저의 새 **ProjectX-Home** 탭에 있는 도구 모음에서 설정 아이콘을 클릭한 다음 **사이트 권한**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="9f3b3-156">On the new **ProjectX-Home** tab in your browser, in the tool bar, click the settings icon, and then click **Site permissions**.</span></span>
    
8. <span data-ttu-id="9f3b3-157">**사이트 권한** 창에서 **고급 권한 설정**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="9f3b3-157">In the **Site permissions** pane, click **Advanced permissions settings**.</span></span>
    
9. <span data-ttu-id="9f3b3-158">브라우저의 새 **사용 권한: Project X** 탭에서 **액세스 요청 설정**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="9f3b3-158">In the new **Permissions: Project X** tab in your browser, click **Access Request Settings**.</span></span>
    
10. <span data-ttu-id="9f3b3-159">**액세스 요청 설정** 대화 상자에서 **구성원이 사이트와 개별 파일 및 폴더를 공유할 수 있도록 허용합니다.** 및 **액세스 요청 허용**(3개의 확인란이 모두 선택 취소됨)을 선택 취소하고 **확인**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="9f3b3-159">In the **Access Requests Settings** dialog box, clear **Allow members to share the site and individual files and folders** and **Allow access requests** (so that all three check boxes are cleared), and then click **OK**.</span></span>
    
11. <span data-ttu-id="9f3b3-160">목록에서 **ProjectX Members**를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="9f3b3-160">Click **ProjectX Members** in the list.</span></span>
    
12. <span data-ttu-id="9f3b3-161">**사용자 및 그룹** 페이지에서 **새로 만들기**를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="9f3b3-161">On the **People and Groups** page, click **New**.</span></span>
    
13. <span data-ttu-id="9f3b3-162">**공유** 대화 상자에 **ProjectX-Members**를 입력하고 **공유**를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="9f3b3-162">In the **Share** dialog box, type **ProjectX-Members**, select it, and then click **Share**.</span></span>
    
14. <span data-ttu-id="9f3b3-163">브라우저에서 뒤로 단추를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="9f3b3-163">Click the back button on your browser.</span></span>
    
15. <span data-ttu-id="9f3b3-164">목록에서 **ProjectX Owners**를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="9f3b3-164">Click **ProjectX Owners** in the list.</span></span>
    
16. <span data-ttu-id="9f3b3-165">**사용자 및 그룹** 페이지에서 **새로 만들기**를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="9f3b3-165">On the **People and Groups** page, click **New**.</span></span>
    
17. <span data-ttu-id="9f3b3-166">**공유** 대화 상자에 **ProjectX-Admins**를 입력하고 **공유**를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="9f3b3-166">In the **Share** dialog box, type **ProjectX-Admins**, select it, and then click **Share**.</span></span>
    
18. <span data-ttu-id="9f3b3-167">브라우저에서 뒤로 단추를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="9f3b3-167">Click the back button on your browser.</span></span>
    
19. <span data-ttu-id="9f3b3-168">목록에서 **ProjectX Visitors**를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="9f3b3-168">Click **ProjectX Visitors** in the list.</span></span>
    
20. <span data-ttu-id="9f3b3-169">**사용자 및 그룹** 페이지에서 **새로 만들기**를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="9f3b3-169">On the **People and Groups** page, click **New**.</span></span>
    
21. <span data-ttu-id="9f3b3-170">**공유** 대화 상자에 **ProjectX-Viewers**를 입력하고 **공유**를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="9f3b3-170">In the **Share** dialog box, type **ProjectX-Viewers**, select it, and then click **Share**.</span></span>
    
22. <span data-ttu-id="9f3b3-171">브라우저에서 **사용자 및 그룹** 탭을 닫고 브라우저에서 **ProjectX-Home**을 클릭한 다음 **사이트 권한** 창을 닫습니다.
</span><span class="sxs-lookup"><span data-stu-id="9f3b3-171">Close the **People and Groups** tab in your browser, click the **ProjectX-Home** tab in your browser, and then close the **Site permissions** pane.</span></span>
    
<span data-ttu-id="9f3b3-172">권한 구성의 결과는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="9f3b3-172">Here are the results of configuring permissions:</span></span>
  
- <span data-ttu-id="9f3b3-173">projectx members SharePoint 그룹에는 projectx-Members 액세스 그룹 (잠재 고객 디자이너 및 잠재 고객 연구원 사용자 계정만 포함)과 projectx 그룹 (전역 관리자 사용자 계정만 포함)만 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9f3b3-173">The ProjectX Members SharePoint group contains only the ProjectX-Members access group (which contains only the Lead Designer and Lead Researcher user accounts) and the ProjectX group (which contains only the global administrator user account).</span></span>
    
- <span data-ttu-id="9f3b3-174">projectx 소유자 SharePoint 그룹에는 projectx-Admins 액세스 그룹 (전역 관리자 사용자 계정만 포함)만 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9f3b3-174">The ProjectX Owners SharePoint group contains only the ProjectX-Admins access group (which contains only the global administrator user account).</span></span>
    
- <span data-ttu-id="9f3b3-175">projectx 방문자 SharePoint 그룹에는 projectx-뷰어 액세스 그룹 (개발 VP 사용자 계정만 포함)만 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9f3b3-175">The ProjectX Visitors SharePoint group contains only the ProjectX-Viewers access group (which contains only the Development VP user account).</span></span>
    
- <span data-ttu-id="9f3b3-176">구성원은 사이트 수준 권한을 수정할 수 없습니다(이 작업은 ProjectX-Admins 그룹의 구성원만 수행할 수 있음).</span><span class="sxs-lookup"><span data-stu-id="9f3b3-176">Members cannot modify site-level permissions (this can only be done by members of the ProjectX-Admins group).</span></span>
    
- <span data-ttu-id="9f3b3-177">다른 사용자 계정은 사이트나 해당 리소스에 액세스할 수 없고 사이트에 대한 액세스를 요청할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="9f3b3-177">Other user accounts cannot access the site or its resources or request access to the site.</span></span>
    
<span data-ttu-id="9f3b3-178">그림 2는 SharePoint 그룹 및 해당 그룹 구성원을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="9f3b3-178">Figure 2 shows the SharePoint groups and their membership.</span></span>
  
<span data-ttu-id="9f3b3-179">**그림 2**</span><span class="sxs-lookup"><span data-stu-id="9f3b3-179">**Figure 2**</span></span>

![SharePoint Online 그룹 및 격리된 SharePoint Online 그룹 사이트에 대한 멤버 자격](media/595abff4-64f9-49de-a37a-c70c6856936b.png)
  
<span data-ttu-id="9f3b3-181">이제 수석 디자이너 사용자 계정을 사용 하 여 액세스 방법을 살펴보겠습니다.</span><span class="sxs-lookup"><span data-stu-id="9f3b3-181">Now let's demonstrate access using the Lead Designer user account:</span></span>
  
1. <span data-ttu-id="9f3b3-182">브라우저에서 **ProjectX-Home** 탭을 닫은 후 브라우저에서 **Microsoft Office 홈** 탭을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="9f3b3-182">Close the **ProjectX-Home** tab in your browser, and then click the **Microsoft Office Home** tab in your browser.</span></span>
    
2. <span data-ttu-id="9f3b3-183">전역 관리자의 이름을 클릭한 다음 **로그아웃**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="9f3b3-183">Click the name of your global administrator, and then click **Sign out**.</span></span>
    
3. <span data-ttu-id="9f3b3-184">잠재 고객 디자이너 계정 이름 및 암호를[https://portal.office.com](https://portal.office.com)사용 하 여 Office 365 portal ()에 로그인 합니다.</span><span class="sxs-lookup"><span data-stu-id="9f3b3-184">Sign in to the Office 365 portal ([https://portal.office.com](https://portal.office.com)) using the Lead Designer account name and its password.</span></span>
    
4. <span data-ttu-id="9f3b3-185">타일 목록에서 **SharePoint**를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="9f3b3-185">In the list of tiles, click **SharePoint**.</span></span>
    
5. <span data-ttu-id="9f3b3-p106">브라우저의 새 **SharePoint** 탭에 있는 검색 상자에 **projectx** 를 입력 하 고 검색을 활성화 한 다음 **projectx** 팀 사이트를 클릭 합니다. projectx 팀 사이트에 대 한 브라우저에 새 탭이 표시 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="9f3b3-p106">On the new **SharePoint** tab in your browser, type **ProjectX** in the search box, activate the search, and then click the **ProjectX** team site. You should see a new tab in your browser for the ProjectX team site.</span></span>
    
6. <span data-ttu-id="9f3b3-p107">설정 아이콘을 선택합니다. **사이트 권한**에 대한 옵션은 없습니다. 즉, ProjectX-Admins 그룹의 구성원만 사이트에서 사용 권한을 수정할 수 있기 때문입니다.</span><span class="sxs-lookup"><span data-stu-id="9f3b3-p107">Click the settings icon. Notice that there is no option for **Site Permissions**. This is correct because only the members of the ProjectX-Admins group can modify permissions on the site</span></span>
    
7. <span data-ttu-id="9f3b3-191">메모장 또는 원하는 텍스트 편집기를 엽니다.</span><span class="sxs-lookup"><span data-stu-id="9f3b3-191">Open Notepad or a text editor of your choice.</span></span>
    
8. <span data-ttu-id="9f3b3-192">projectx 팀 사이트의 URL을 복사 하 여 메모장 이나 텍스트 편집기에서 새 줄에 붙여 넣습니다.</span><span class="sxs-lookup"><span data-stu-id="9f3b3-192">Copy the URL of the ProjectX team site and paste it on a new line in Notepad or your text editor.</span></span>
    
9. <span data-ttu-id="9f3b3-193">브라우저의 새 **ProjectX-Home** 탭에서 **문서**를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="9f3b3-193">On the new **ProjectX-Home** tab in your browser, click **Documents**.</span></span>
    
10. <span data-ttu-id="9f3b3-194">ProjectX 문서 폴더 URL을 복사한 후 메모장이나 텍스트 편집기에서 새 줄에 붙여 넣습니다.</span><span class="sxs-lookup"><span data-stu-id="9f3b3-194">Copy the URL of the ProjectX documents folder and paste it on a new line in Notepad or your text editor.</span></span>
    
11. <span data-ttu-id="9f3b3-195">브라우저의 새 **ProjectX-Documents** 탭에서 **새로 만들기 > Word 문서**를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="9f3b3-195">On the new **ProjectX-Documents** tab in your browser, click **New > Word document**.</span></span>
    
12. <span data-ttu-id="9f3b3-p108">**Word Online** 페이지에서 일부 텍스트를 입력하고, 상태가 **저장됨**이 될 때까지 기다린 후 브라우저에서 뒤로 단추를 클릭하고 페이지를 새로 고칩니다. **문서** 폴더에는 새 **Document.docx**가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="9f3b3-p108">Type some text in the **Word Online** page, wait for the status to indicate **Saved**, click the back button on your browser, and then refresh the page. You should see a new **Document.docx** in the **Documents** folder.</span></span>
    
13. <span data-ttu-id="9f3b3-198">**Document.docx** 문서에 대해 줄임표를 클릭하고 **링크 가져오기**를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="9f3b3-198">Click the ellipsis for the **Document.docx** document, and then click **Get a link**.</span></span>
    
14. <span data-ttu-id="9f3b3-199">**공유의 ' 문서 .docx '** 대화 상자에 URL을 복사 하 여 메모장 이나 텍스트 편집기에서 새 줄에 붙여 넣은 다음 **공유 ' 문서 .docx '** 대화 상자를 닫습니다.</span><span class="sxs-lookup"><span data-stu-id="9f3b3-199">Copy the URL in the **Share 'Document.docx'** dialog box and paste it on a new line in Notepad or your text editor, and then close the **Share 'Document.docx'** dialog box.</span></span>
    
15. <span data-ttu-id="9f3b3-200">브라우저에서 **ProjectX-Documents** 및 **SharePoint** 탭을 닫은 후 **Microsoft Office 홈** 탭을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="9f3b3-200">Close the **ProjectX-Documents** and **SharePoint** tabs in your browser, and then click the **Microsoft Office Home** tab.</span></span>
    
16. <span data-ttu-id="9f3b3-201">**Lead Designer** 이름을 클릭하고 **로그아웃**을 클릭합니다.
</span><span class="sxs-lookup"><span data-stu-id="9f3b3-201">Click the **Lead Designer** name, and then click **Sign out**.</span></span>
    
<span data-ttu-id="9f3b3-202">이제 개발 VP 사용자 계정을 사용 하 여 액세스 방법을 살펴보겠습니다.</span><span class="sxs-lookup"><span data-stu-id="9f3b3-202">Now let's demonstrate access using the Development VP user account:</span></span>
  
1. <span data-ttu-id="9f3b3-203">개발 VP 계정 이름 및 암호를 사용[https://portal.office.com](https://portal.office.com)하 여 Office 365 portal ()에 로그인 합니다.</span><span class="sxs-lookup"><span data-stu-id="9f3b3-203">Sign in to the Office 365 portal ([https://portal.office.com](https://portal.office.com)) using the Development VP account name and its password.</span></span>
    
2. <span data-ttu-id="9f3b3-204">타일 목록에서 **SharePoint**를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="9f3b3-204">In the list of tiles, click **SharePoint**.</span></span>
    
3. <span data-ttu-id="9f3b3-p109">브라우저의 새 **SharePoint** 탭에 있는 검색 상자에 **projectx** 를 입력 하 고 검색을 활성화 한 다음 **projectx** 팀 사이트를 클릭 합니다. projectx 팀 사이트에 대 한 브라우저에 새 탭이 표시 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="9f3b3-p109">On the new **SharePoint** tab in your browser, type **ProjectX** in the search box, activate the search, and then click the **ProjectX** team site. You should see a new tab in your browser for the ProjectX team site.</span></span>
    
4. <span data-ttu-id="9f3b3-207">**문서**를 클릭하고 **Document.docx** 파일을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="9f3b3-207">Click **Documents**, and then click the **Document.docx** file.</span></span>
    
5. <span data-ttu-id="9f3b3-p110">브라우저의 **Document.docx** 탭에서 텍스트를 수정해 봅니다. **이 문서는 읽기 전용입니다.** 라는 메시지가 표시됩니다. Development VP 사용자 계정에는 사이트에 대한 보기 권한만 있기 때문입니다.</span><span class="sxs-lookup"><span data-stu-id="9f3b3-p110">In the **Document.docx** tab in your browser, try to modify the text. You should see a message stating **This document is read-only.** This is expected because the Development VP user account only has view permissions for the site.</span></span>
    
6. <span data-ttu-id="9f3b3-211">브라우저에서 **Document.docx**, **ProjectX-Documents** 및 **SharePoint** 탭을 닫습니다.</span><span class="sxs-lookup"><span data-stu-id="9f3b3-211">Close the **Document.docx**, **ProjectX-Documents**, and **SharePoint** tabs in your browser.</span></span>
    
7. <span data-ttu-id="9f3b3-212">**Microsoft Office 홈** 탭을 클릭하고 **Development VP** 이름을 클릭한 후 **로그아웃**을 클릭합니다.
</span><span class="sxs-lookup"><span data-stu-id="9f3b3-212">Click the **Microsoft Office Home** tab, click the **Development VP** name, and then click **Sign out**.</span></span>
    
<span data-ttu-id="9f3b3-213">이제 사용 권한이 없는 사용자 계정을 사용 하 여 액세스 하는 방법을 알아보겠습니다.</span><span class="sxs-lookup"><span data-stu-id="9f3b3-213">Now let's demonstrate access with a user account that has no permissions:</span></span>
  
1. <span data-ttu-id="9f3b3-214">사용자 3 계정 이름 및 암호를 사용[https://portal.office.com](https://portal.office.com)하 여 Office 365 portal ()에 로그인 합니다.</span><span class="sxs-lookup"><span data-stu-id="9f3b3-214">Sign in to the Office 365 portal ([https://portal.office.com](https://portal.office.com)) using the User 3 account name and its password.</span></span>
    
2. <span data-ttu-id="9f3b3-215">타일 목록에서 **SharePoint**를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="9f3b3-215">In the list of tiles, click **SharePoint**.</span></span>
    
3. <span data-ttu-id="9f3b3-p111">	브라우저의 새 *\*SharePoint** 탭에서 검색 상자에 *\*ProjectX*\*를 입력하고 검색을 활성화합니다. *\*여기에는 검색에 일치하는 항목이 없습니다.** 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="9f3b3-p111">On the new **SharePoint** tab in your browser, type **ProjectX** in the search box and then activate the search. You should see the message **Nothing here matches your search.**</span></span>
    
4. <span data-ttu-id="9f3b3-p112">열려 있는 메모장 또는 텍스트 편집기 인스턴스에서 ProjectX 사이트의 URL을 브라우저의 주소 표시줄에 복사하고 **Enter** 키를 누릅니다. **액세스가 거부되었습니다.** 페이지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="9f3b3-p112">From the open instance of Notepad or your text editor, copy the URL for the ProjectX site into the address bar of your browser and press **Enter**. You should see an **Access Denied** page.</span></span>
    
5. <span data-ttu-id="9f3b3-p113">메모장 또는 텍스트 편집기에서 ProjectX Documents 폴더의 URL을 브라우저의 주소 표시줄에 복사하고 **Enter** 키를 누릅니다. **액세스가 거부되었습니다.** 페이지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="9f3b3-p113">From Notepad or your text editor, copy the URL for the ProjectX Documents folder into the address bar of your browser and press **Enter**. You should see an **Access Denied** page.</span></span>
    
6. <span data-ttu-id="9f3b3-p114">메모장 또는 텍스트 편집기에서 Documents.docx 파일의 URL을 브라우저의 주소 표시줄에 복사하고 **Enter** 키를 누릅니다. **액세스가 거부되었습니다.** 페이지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="9f3b3-p114">From Notepad or your text editor, copy the URL for the Documents.docx file into the address bar of your browser and press **Enter**. You should see an **Access Denied** page.</span></span>
    
7. <span data-ttu-id="9f3b3-224">브라우저에서 **SharePoint** 탭을 닫고 **Microsoft Office 홈** 탭을 클릭한 후 **사용자 3** 이름을 클릭하고 **로그아웃**을 클릭합니다.
</span><span class="sxs-lookup"><span data-stu-id="9f3b3-224">Close the **SharePoint** tab in your browser, click the **Microsoft Office Home** tab, click the **User 3** name, and then click **Sign out**.</span></span>
    
<span data-ttu-id="9f3b3-225">이제 격리 된 SharePoint Online 사이트에 대 한 추가 실험 준비가 완료 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="9f3b3-225">Your isolated SharePoint Online site is now ready for your additional experimentation.</span></span>
  
## <a name="next-step"></a><span data-ttu-id="9f3b3-226">다음 단계</span><span class="sxs-lookup"><span data-stu-id="9f3b3-226">Next Step</span></span>

<span data-ttu-id="9f3b3-227">프로덕션 환경에 격리된 SharePoint Online 팀 사이트를 배포할 준비가 되면 [격리된 SharePoint Online 팀 사이트 디자인](design-an-isolated-sharepoint-online-team-site.md)에서 단계별 디자인 고려 사항을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="9f3b3-227">When you are ready to deploy an isolated SharePoint Online team site in production, see the step-by-step design considerations in [Design an isolated SharePoint Online team site](design-an-isolated-sharepoint-online-team-site.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="9f3b3-228">참고 항목</span><span class="sxs-lookup"><span data-stu-id="9f3b3-228">See Also</span></span>

[<span data-ttu-id="9f3b3-229">격리된 SharePoint Online 팀 사이트</span><span class="sxs-lookup"><span data-stu-id="9f3b3-229">Isolated SharePoint Online team sites</span></span>](isolated-sharepoint-online-team-sites.md)
  
[<span data-ttu-id="9f3b3-230">클라우드 도입 TLG(테스트 랩 가이드)</span><span class="sxs-lookup"><span data-stu-id="9f3b3-230">Cloud adoption Test Lab Guides (TLGs)</span></span>](https://docs.microsoft.com/office365/enterprise/cloud-adoption-test-lab-guides-tlgs)
  
[<span data-ttu-id="9f3b3-231">기본 구성 개발/테스트 환경</span><span class="sxs-lookup"><span data-stu-id="9f3b3-231">Base Configuration dev/test environment</span></span>](https://docs.microsoft.com/office365/enterprise/base-configuration-dev-test-environment)
  
[<span data-ttu-id="9f3b3-232">Office 365 개발/테스트 환경</span><span class="sxs-lookup"><span data-stu-id="9f3b3-232">Office 365 dev/test environment</span></span>](https://docs.microsoft.com/office365/enterprise/office-365-dev-test-environment)
  
[<span data-ttu-id="9f3b3-233">클라우드 도입 및 하이브리드 솔루션</span><span class="sxs-lookup"><span data-stu-id="9f3b3-233">Cloud adoption and hybrid solutions</span></span>](https://docs.microsoft.com/office365/enterprise/cloud-adoption-and-hybrid-solutions)




