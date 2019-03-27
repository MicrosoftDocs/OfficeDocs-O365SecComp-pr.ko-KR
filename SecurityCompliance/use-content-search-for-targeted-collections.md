---
title: 대상 모음에 Office 365의 콘텐츠 검색 사용
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
ms.collection: M365-security-compliance
localization_priority: Normal
search.appverid: MOE150
ms.assetid: e3cbc79c-5e97-43d3-8371-9fbc398cd92e
description: Office 365 보안 &amp; 및 준수 센터의 콘텐츠 검색을 사용 하 여 대상 지정 된 컬렉션을 수행 합니다. 대상 컬렉션은 사례 또는 권한이 부여 된 항목에 대 한 응답 항목이 특정 사서함 또는 사이트 폴더에 있는 것을 확신 함을 의미 합니다. 이 문서의 스크립트를 사용 하 여 검색 하려는 특정 사서함 또는 사이트 폴더의 폴더 ID 또는 경로를 가져옵니다.
ms.openlocfilehash: 4cfdb95ef65f94bc46b79265f986ed8d9ada04da
ms.sourcegitcommit: c0d4fe3e43e22353f30034567ade28330266bcf7
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/27/2019
ms.locfileid: "30899998"
---
# <a name="use-content-search-in-office-365-for-targeted-collections"></a><span data-ttu-id="4cc3c-105">대상 모음에 Office 365의 콘텐츠 검색 사용</span><span class="sxs-lookup"><span data-stu-id="4cc3c-105">Use Content Search in Office 365 for targeted collections</span></span>

<span data-ttu-id="4cc3c-106">Office 365 보안 &amp; 준수 센터의 콘텐츠 검색 기능은 Exchange 사서함 이나 SharePoint 및 비즈니스용 OneDrive 사이트의 특정 폴더를 검색 하는 UI에서 직접 방법을 제공 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4cc3c-106">The Content Search feature in the Office 365 Security &amp; Compliance Center doesn't provide a direct way in the UI to search specific folders in Exchange mailboxes or SharePoint and OneDrive for Business sites.</span></span> <span data-ttu-id="4cc3c-107">그러나 실제 검색 쿼리 구문의 사이트에 대 한 전자 메일 또는 경로 (documentlink) 속성을 지정 하 여 특정 폴더 (대상 지정 된 *컬렉션*이라고 함)를 검색할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4cc3c-107">However, it's possible to search specific folders (called a *targeted collection*) by specifying the folder ID property for email or path (DocumentLink) property for sites in the actual search query syntax.</span></span> <span data-ttu-id="4cc3c-108">콘텐츠 검색을 사용 하 여 대상 모음을 수행 하는 것은 특정 사서함 이나 사이트 폴더에 있는 항목에 대 한 응답 항목이 있는 경우에 유용 합니다.</span><span class="sxs-lookup"><span data-stu-id="4cc3c-108">Using Content Search to perform a targeted collection is useful when you're confident that items responsive to a case or privileged items are located in a specific mailbox or site folder.</span></span> <span data-ttu-id="4cc3c-109">이 문서의 스크립트를 사용 하 여 SharePoint 및 비즈니스용 OneDrive 사이트의 폴더 ID 또는 사서함 폴더에 대 한 경로 (documentlink)를 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4cc3c-109">You can use the script in this article to obtain the folder ID for mailbox folders or the path (DocumentLink) for folders on a SharePoint and OneDrive for Business site.</span></span> <span data-ttu-id="4cc3c-110">그런 다음 검색 쿼리의 폴더 ID 또는 경로를 사용 하 여 폴더에 있는 항목을 반환할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4cc3c-110">Then you can use the folder ID or path in a search query to return items located in the folder.</span></span>

> [!NOTE]
> <span data-ttu-id="4cc3c-111">SharePoint 또는 비즈니스용 OneDrive 사이트의 폴더에 있는 콘텐츠를 반환 하려면이 항목의 스크립트에서 Path 속성 대신 documentlink 관리 속성을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="4cc3c-111">To return content located in a folder in a SharePoint or OneDrive for Business site, the script in this topic uses the DocumentLink managed property instead of the Path property.</span></span> <span data-ttu-id="4cc3c-112">documentlink 속성은 폴더의 모든 콘텐츠를 반환 하지만 path 속성은 일부 미디어 파일을 반환 하지 않기 때문에 경로 속성 보다 더 강력 합니다.</span><span class="sxs-lookup"><span data-stu-id="4cc3c-112">The DocumentLink property is more robust than the Path property because it will return all content in a folder, whereas the Path property won't return some media files.</span></span>

## <a name="before-you-begin"></a><span data-ttu-id="4cc3c-113">시작하기 전에</span><span class="sxs-lookup"><span data-stu-id="4cc3c-113">Before you begin</span></span>

- <span data-ttu-id="4cc3c-114">1 단계에서 스크립트를 실행 하려면 보안 &amp; 및 준수 센터에서 eDiscovery 관리자 역할 그룹의 구성원 이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="4cc3c-114">You have to be a member of the eDiscovery Manager role group in the Security &amp; Compliance Center to run the script in Step 1.</span></span> <span data-ttu-id="4cc3c-115">자세한 내용은 [eDiscovery 사용 권한 할당](assign-ediscovery-permissions.md)을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="4cc3c-115">For more information, see [Assign eDiscovery permissions](assign-ediscovery-permissions.md).</span></span>
    
    <span data-ttu-id="4cc3c-116">또한 Exchange Online 조직에서 Mail Recipients 역할을 할당 받아야 합니다.</span><span class="sxs-lookup"><span data-stu-id="4cc3c-116">Additionally, you have to be assigned the Mail Recipients role in your Exchange Online organization.</span></span> <span data-ttu-id="4cc3c-117">이는 1 단계의 스크립트에 포함 된 **get-mailboxfolderstatistics** cmdlet을 실행 하는 데 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="4cc3c-117">This is required to run the **Get-MailboxFolderStatistics** cmdlet, which is included in the script in Step 1.</span></span> <span data-ttu-id="4cc3c-118">기본적으로 메일 받는 사람 역할은 Exchange Online의 조직 관리 및 받는 사람 관리 역할 그룹에 할당 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4cc3c-118">By default, the Mail Recipients role is assigned to the Organization Management and Recipient Management role groups in Exchange Online.</span></span> <span data-ttu-id="4cc3c-119">Exchange Online에서 사용 권한을 할당 하는 방법에 대 한 자세한 내용은 [Manage role group members](https://go.microsoft.com/fwlink/p/?linkid=692102)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="4cc3c-119">For more information about assigning permissions in Exchange Online, see [Manage role group members](https://go.microsoft.com/fwlink/p/?linkid=692102).</span></span> <span data-ttu-id="4cc3c-120">사용자 지정 역할 그룹을 만들고 메일 받는 사람 역할을 할당 한 다음 1 단계에서 스크립트를 실행 해야 하는 구성원을 추가할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4cc3c-120">You could also create a custom role group, assign the Mail Recipients role to it, and then add the members who need to run the script in Step 1.</span></span> <span data-ttu-id="4cc3c-121">자세한 내용은 [역할 그룹 관리](https://go.microsoft.com/fwlink/p/?linkid=730688) 항목을 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="4cc3c-121">For more information, see [Manage role groups](https://go.microsoft.com/fwlink/p/?linkid=730688).</span></span>
    
- <span data-ttu-id="4cc3c-122">1 단계에서 스크립트를 실행할 때마다 새 원격 PowerShell 세션이 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="4cc3c-122">Each time you run the script in Step 1, a new remote PowerShell session is created.</span></span> <span data-ttu-id="4cc3c-123">따라서 사용할 수 있는 모든 원격 PowerShell 세션을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4cc3c-123">So you could use up all the remote PowerShell sessions available to you.</span></span> <span data-ttu-id="4cc3c-124">이러한 상황이 발생 하지 않도록 하려면 다음 명령을 실행 하 여 활성 원격 PowerShell 세션의 연결을 끊으십시오.</span><span class="sxs-lookup"><span data-stu-id="4cc3c-124">To prevent this from happening, you can run the following command to disconnect your active remote PowerShell sessions.</span></span>
    
  ```
  Get-PSSession | Remove-PSSession
  ```

    <span data-ttu-id="4cc3c-125">자세한 내용은 [원격 PowerShell을 사용하여 Exchange Online에 연결](https://go.microsoft.com/fwlink/p/?linkid=396554)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="4cc3c-125">For more information, see [Connect to Exchange Online PowerShell](https://go.microsoft.com/fwlink/p/?linkid=396554).</span></span>
    
- <span data-ttu-id="4cc3c-126">스크립트에 최소 오류 처리가 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4cc3c-126">The script includes minimal error handling.</span></span> <span data-ttu-id="4cc3c-127">이 스크립트의 기본 목적은 콘텐츠 검색의 검색 쿼리 구문에서 대상 모음을 수행 하는 데 사용할 수 있는 사서함 폴더 id 또는 사이트 경로 목록을 빠르게 표시 하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="4cc3c-127">The primary purpose of the script is to quickly display a list of mailbox folder IDs or site paths that can be used in the search query syntax of a Content Search to perform a targeted collection.</span></span>
    
- <span data-ttu-id="4cc3c-128">이 항목에서 제공 하는 예제 스크립트는 Microsoft standard 지원 프로그램 또는 서비스에서 지원 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4cc3c-128">The sample script provided in this topic isn't supported under any Microsoft standard support program or service.</span></span> <span data-ttu-id="4cc3c-129">예제 스크립트는 어떤 종류의 보증도 없이 있는 그대로 제공 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4cc3c-129">The sample script is provided AS IS without warranty of any kind.</span></span> <span data-ttu-id="4cc3c-130">Microsoft는 상품성 또는 특정 목적에 대 한 적합성에 대 한 묵시적 보증을 제한 없이 포함 하 여 모든 묵시적 보증을 배제 합니다.</span><span class="sxs-lookup"><span data-stu-id="4cc3c-130">Microsoft further disclaims all implied warranties including, without limitation, any implied warranties of merchantability or of fitness for a particular purpose.</span></span> <span data-ttu-id="4cc3c-131">샘플 스크립트 및 설명서의 사용 또는 성능으로 인해 발생 하는 전체 위험은 사용자에 게 남아 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4cc3c-131">The entire risk arising out of the use or performance of the sample script and documentation remains with you.</span></span> <span data-ttu-id="4cc3c-132">Microsoft, 작성자 또는 스크립트를 작성, 프로덕션 또는 전달 하는 것과 관련 된 다른 모든 손해에 대 한 책임 (예를 들어, 비즈니스 이익 손실에 대 한 손해, 비즈니스 중단 Microsoft에서 이러한 손해에 대 한 권고를 받은 경우에도 예제 스크립트나 설명서를 사용 하거나 사용 하지 못하는 등의 비즈니스 정보 또는 기타 pecuniary 손실입니다.</span><span class="sxs-lookup"><span data-stu-id="4cc3c-132">In no event shall Microsoft, its authors, or anyone else involved in the creation, production, or delivery of the scripts be liable for any damages whatsoever (including, without limitation, damages for loss of business profits, business interruption, loss of business information, or other pecuniary loss) arising out of the use of or inability to use the sample scripts or documentation, even if Microsoft has been advised of the possibility of such damages.</span></span>
  
## <a name="step-1-run-the-script-to-get-a-list-of-folders-for-a-mailbox-or-site"></a><span data-ttu-id="4cc3c-133">1 단계: 스크립트를 실행 하 여 사서함 또는 사이트의 폴더 목록 가져오기</span><span class="sxs-lookup"><span data-stu-id="4cc3c-133">Step 1: Run the script to get a list of folders for a mailbox or site</span></span>

<span data-ttu-id="4cc3c-134">이 첫 단계에서 실행 하는 스크립트는 사서함 폴더 또는 SharePoint 및 비즈니스용 OneDrive 폴더 목록과 각 폴더의 해당 하는 폴더 ID 또는 경로를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="4cc3c-134">The script that you run in this first step will return a list of mailbox folders or SharePoint and OneDrive for Business folders, and the corresponding folder ID or path for each folder.</span></span> <span data-ttu-id="4cc3c-135">이 스크립트를 실행 하면 다음 정보를 입력 하 라는 메시지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4cc3c-135">When you run this script, it will prompt you for the following information.</span></span>
  
- <span data-ttu-id="4cc3c-136">**전자 메일 주소 또는 사이트 URL** Exchange 사서함 폴더 및 폴더 id 목록을 반환할 custodian의 전자 메일 주소를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="4cc3c-136">**Email address or site URL** Type an email address of the custodian to return a list of Exchange mailbox folders and folder IDs.</span></span> <span data-ttu-id="4cc3c-137">또는 SharePoint 사이트의 URL 또는 비즈니스용 OneDrive 사이트를 입력 하 여 지정 된 사이트에 대 한 경로 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="4cc3c-137">Or type the URL for a SharePoint site or a OneDrive for Business site to return a list of paths for the specified site.</span></span> <span data-ttu-id="4cc3c-138">그 예는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="4cc3c-138">Here are some examples:</span></span> 
    
  - <span data-ttu-id="4cc3c-139">**Exchange** -stacig@contoso.onmicrosoft.com</span><span class="sxs-lookup"><span data-stu-id="4cc3c-139">**Exchange** - stacig@contoso.onmicrosoft.com</span></span> 
    
  - <span data-ttu-id="4cc3c-140">**SharePoint** - https://contoso.sharepoint.com/sites/marketing</span><span class="sxs-lookup"><span data-stu-id="4cc3c-140">**SharePoint** - https://contoso.sharepoint.com/sites/marketing</span></span> 
    
  - <span data-ttu-id="4cc3c-141">**비즈니스용 OneDrive** - https://contoso-my.sharepoint.com/personal/stacig_contoso_onmicrosoft_com</span><span class="sxs-lookup"><span data-stu-id="4cc3c-141">**OneDrive for Business** - https://contoso-my.sharepoint.com/personal/stacig_contoso_onmicrosoft_com</span></span> 
    
- <span data-ttu-id="4cc3c-142">**사용자 자격 증명** -스크립트는 자격 증명을 사용 하 여 Exchange Online 및 원격 PowerShell을 &amp; 통해 보안 준수 센터에 연결 합니다.</span><span class="sxs-lookup"><span data-stu-id="4cc3c-142">**Your user credentials** - The script will use your credentials to connect to Exchange Online and the Security &amp; Compliance Center with remote PowerShell.</span></span> <span data-ttu-id="4cc3c-143">앞에서 설명한 것 처럼이 스크립트를 성공적으로 실행 하려면 적절 한 사용 권한을 할당 받아야 합니다.</span><span class="sxs-lookup"><span data-stu-id="4cc3c-143">As previously explained, you have to assigned the appropriate permissions to successfully run this script.</span></span>
    
<span data-ttu-id="4cc3c-144">사서함 폴더 또는 사이트 documentlink (경로) 이름 목록을 표시 하려면 다음을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="4cc3c-144">To display a list of mailbox folders or site documentlink (path) names:</span></span>
  
1. <span data-ttu-id="4cc3c-145">파일 이름 접미사. p s 1을 사용 하 여 Windows PowerShell 스크립트 파일에 다음 텍스트를 저장 합니다. 예를 `GetFolderSearchParameters.ps1`들면입니다.</span><span class="sxs-lookup"><span data-stu-id="4cc3c-145">Save the following text to a Windows PowerShell script file by using a filename suffix of .ps1; for example, `GetFolderSearchParameters.ps1`.</span></span>
    
  ```
  #########################################################################################################
  # This PowerShell script will prompt you for:                             #
  #    * Admin credentials for a user who can run the Get-MailboxFolderStatistics cmdlet in Exchange    #
  #      Online and who is an eDiscovery Manager in the Security &amp; Compliance Center.           #
  # The script will then:                                           #
  #    * If an email address is supplied: list the folders for the target mailbox.          #
  #    * If a SharePoint or OneDrive for Business site is supplied: list the documentlinks (folder paths) #
  #    * for the site.                                                                                  #
  #    * In both cases, the script supplies the correct search properties (folderid: or documentlink:)  #
  #      appended to the folder ID or documentlink to use in a Content Search.              #
  # Notes:                                              #
  #    * For SharePoint and OneDrive for Business, the paths are searched recursively; this means the   #
  #      the current folder and all sub-folders are searched.                       #
  #    * For Exchange, only the specified folder will be searched; this means sub-folders in the folder #
  #      will not be searched.  To search sub-folders, you need to use the specify the folder ID for    #
  #      each sub-folder that you want to search.                               #
  #    * For Exchange, only folders in the user's primary mailbox will be returned by the script.       #
  #########################################################################################################
  # Collect the target email address or SharePoint Url
  $addressOrSite = Read-Host "Enter an email address or a URL for a SharePoint or OneDrive for Business site"
  # Authenticate with Exchange Online and the Security &amp; Compliance Center (Exchange Online Protection - EOP)
  if (!$credentials)
  {
      $credentials = Get-Credential
  }
  if ($addressOrSite.IndexOf("@") -ige 0)
  {
      # List the folder Ids for the target mailbox
      $emailAddress = $addressOrSite
      # Authenticate with Exchange Online
      if (!$ExoSession)
      {
          $ExoSession = New-PSSession -ConfigurationName Microsoft.Exchange -ConnectionUri https://ps.outlook.com/powershell-liveid/ -Credential $credentials -Authentication Basic -AllowRedirection
          Import-PSSession $ExoSession -AllowClobber -DisableNameChecking
      }
      $folderQueries = @()
      $folderStatistics = Get-MailboxFolderStatistics $emailAddress
      foreach ($folderStatistic in $folderStatistics)
      {
          $folderId = $folderStatistic.FolderId;
          $folderPath = $folderStatistic.FolderPath;
          $encoding= [System.Text.Encoding]::GetEncoding("us-ascii")
          $nibbler= $encoding.GetBytes("0123456789ABCDEF");
          $folderIdBytes = [Convert]::FromBase64String($folderId);
          $indexIdBytes = New-Object byte[] 48;
          $indexIdIdx=0;
          $folderIdBytes | select -skip 23 -First 24 | %{$indexIdBytes[$indexIdIdx++]=$nibbler[$_ -shr 4];$indexIdBytes[$indexIdIdx++]=$nibbler[$_ -band 0xF]}
          $folderQuery = "folderid:$($encoding.GetString($indexIdBytes))";
          $folderStat = New-Object PSObject
          Add-Member -InputObject $folderStat -MemberType NoteProperty -Name FolderPath -Value $folderPath
          Add-Member -InputObject $folderStat -MemberType NoteProperty -Name FolderQuery -Value $folderQuery
          $folderQueries += $folderStat
      }
      Write-Host "-----Exchange Folders-----"
      $folderQueries |ft
  }
  elseif ($addressOrSite.IndexOf("http") -ige 0)
  {
      $searchName = "SPFoldersSearch"
      $searchActionName = "SPFoldersSearch_Preview"
      # List the folders for the SharePoint or OneDrive for Business Site
      $siteUrl = $addressOrSite
      # Authenticate with the Security &amp; Compliance Center
      if (!$SccSession)
      {
          $SccSession = New-PSSession -ConfigurationName Microsoft.Exchange -ConnectionUri https://ps.compliance.protection.outlook.com/powershell-liveid -Credential $credentials -Authentication Basic -AllowRedirection
          Import-PSSession $SccSession -AllowClobber -DisableNameChecking
      }
      # Clean-up, if the script was aborted, the search we created might not have been deleted.  Try to do so now.
      Remove-ComplianceSearch $searchName -Confirm:$false -ErrorAction 'SilentlyContinue'
      # Create a Content Search against the SharePoint Site or OneDrive for Business site and only search for folders; wait for the search to complete
      $complianceSearch = New-ComplianceSearch -Name $searchName -ContentMatchQuery "contenttype:folder" -SharePointLocation $siteUrl
      Start-ComplianceSearch $searchName
      do{
          Write-host "Waiting for search to complete..."
          Start-Sleep -s 5
          $complianceSearch = Get-ComplianceSearch $searchName
      }while ($complianceSearch.Status -ne 'Completed')
      if ($complianceSearch.Items -gt 0)
      {
          # Create a Compliance Search Action and wait for it to complete. The folders will be listed in the .Results parameter
          $complianceSearchAction = New-ComplianceSearchAction -SearchName $searchName -Preview
          do
          {
              Write-host "Waiting for search action to complete..."
              Start-Sleep -s 5
              $complianceSearchAction = Get-ComplianceSearchAction $searchActionName
          }while ($complianceSearchAction.Status -ne 'Completed')
          # Get the results and print out the folders
          $results = $complianceSearchAction.Results
          $matches = Select-String "Data Link:.+[,}]" -Input $results -AllMatches
          foreach ($match in $matches.Matches)
          {
              $rawUrl = $match.Value
              $rawUrl = $rawUrl -replace "Data Link: " -replace "," -replace "}"
              Write-Host "DocumentLink:""$rawUrl"""
          }
      }
      else
      {
          Write-Host "No folders were found for $siteUrl"
      }
      Remove-ComplianceSearch $searchName -Confirm:$false -ErrorAction 'SilentlyContinue'
  }
  else
  {
      Write-Error "Couldn't recognize $addressOrSite as an email address or a site URL"
  }
  ```

2. <span data-ttu-id="4cc3c-146">로컬 컴퓨터에서 Windows PowerShell을 열고 스크립트를 저장 한 폴더로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="4cc3c-146">On your local computer, open Windows PowerShell and go to the folder where you saved the script.</span></span>
    
3. <span data-ttu-id="4cc3c-147">스크립트를 실행 합니다. 예를 들어:</span><span class="sxs-lookup"><span data-stu-id="4cc3c-147">Run the script; for example:</span></span>
    
      ```
      .\GetFolderSearchParameters.ps1
      ```

4. <span data-ttu-id="4cc3c-148">스크립트에서 묻는 메시지가 표시 되는 정보를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="4cc3c-148">Enter the information that the script prompts you for.</span></span>
    
    <span data-ttu-id="4cc3c-149">이 스크립트는 지정 된 사용자에 대 한 사서함 폴더 또는 사이트 폴더의 목록을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="4cc3c-149">The script displays a list of mailbox folders or site folders for the specified user.</span></span> <span data-ttu-id="4cc3c-150">폴더 ID 또는 documentlink 링크 이름을 복사 하 여 2 단계의 검색 쿼리에 붙여 넣을 수 있도록이 창을 열어 놓습니다.</span><span class="sxs-lookup"><span data-stu-id="4cc3c-150">Let this window open so that you can copy a folder ID or documentlink name and paste it in to a search query in Step 2.</span></span>
    
    > [!TIP]
    > <span data-ttu-id="4cc3c-151">컴퓨터 화면에 폴더 목록을 표시 하는 대신 스크립트의 출력을 텍스트 파일로 다시 보낼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4cc3c-151">Instead of displaying a list of folders on the computer screen, you can re-direct the output of the script to a text file.</span></span> <span data-ttu-id="4cc3c-152">이 파일은 스크립트가 있는 폴더에 저장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4cc3c-152">This file will be saved to the folder where the script is located.</span></span> <span data-ttu-id="4cc3c-153">예를 들어 스크립트 출력을 텍스트 파일로 리디렉션하려면 3 단계: `.\GetFolderSearchParameters.ps1 > StacigFolderIds.txt` 에서 다음 명령을 실행 하 고 검색 쿼리에서 사용할 폴더 ID 또는 documentlink를 파일에서 복사 하면 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4cc3c-153">For example, to redirect the script output to a text file, run the following command in Step 3:  `.\GetFolderSearchParameters.ps1 > StacigFolderIds.txt` Then you can copy a folder ID or documentlink from the file to use in a search query.</span></span>
  
### <a name="script-output-for-mailbox-folders"></a><span data-ttu-id="4cc3c-154">사서함 폴더에 대 한 스크립트 출력</span><span class="sxs-lookup"><span data-stu-id="4cc3c-154">Script output for mailbox folders</span></span>

<span data-ttu-id="4cc3c-155">사서함 폴더 id를 가져오는 경우 스크립트는 원격 PowerShell을 사용 하 여 Exchange Online에 연결 하 고 **MailboxFolderStatisics** cmdlet을 실행 한 다음 지정 된 사서함의 폴더 목록을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="4cc3c-155">If you're getting mailbox folder IDs, the script connects to Exchange Online by using remote PowerShell, runs the **Get-MailboxFolderStatisics** cmdlet, and then displays the list of the folders from the specified mailbox.</span></span> <span data-ttu-id="4cc3c-156">사서함의 모든 폴더에 대해 스크립트는 **FolderPath** 열에 폴더 이름을 표시 하 고 **folderquery** 열에는 폴더 ID를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="4cc3c-156">For every folder in the mailbox, the script displays the name of the folder in the **FolderPath** column and the folder ID in the **FolderQuery** column.</span></span> <span data-ttu-id="4cc3c-157">또한이 스크립트는 사서함 속성의 이름인 **folderId** 접두사를 폴더 ID에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="4cc3c-157">Additionally, the script adds the prefix of **folderId** (which is the name of the mailbox property) to the folder ID.</span></span> <span data-ttu-id="4cc3c-158">**folderid** 속성은 검색 가능한 속성 이므로 2 단계의 검색 쿼리를 `folderid:<folderid>` 사용 하 여 해당 폴더를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="4cc3c-158">Because the **folderid** property is a searchable property, you'll use  `folderid:<folderid>` in a search query in Step 2 to search that folder.</span></span> 

> [!IMPORTANT]
> <span data-ttu-id="4cc3c-159">이 문서의 스크립트에는 **get-mailboxfolderstatistics** 에서 반환 하는 64 문자 폴더 Id 값을 검색을 위해 인덱싱되는 동일한 48 문자로 변환 하는 인코딩 논리가 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4cc3c-159">The script in this article includes encoding logic that converts the 64-character folder Id values that are returned by **Get-MailboxFolderStatistics** to the same 48-character format that is indexed for search.</span></span> <span data-ttu-id="4cc3c-160">이 문서의 스크립트를 실행 하는 대신 PowerShell에서 **get-mailboxfolderstatistics** cmdlet을 실행 하 여 폴더 id를 가져오는 경우 해당 폴더 id 값을 사용 하는 검색 쿼리가 실패 합니다.</span><span class="sxs-lookup"><span data-stu-id="4cc3c-160">If you just run the **Get-MailboxFolderStatistics** cmdlet in PowerShell to obtain a folder Id (instead of running the script in this article), a search query that uses that folder Id value will fail.</span></span> <span data-ttu-id="4cc3c-161">콘텐츠 검색에 사용할 수 있는 올바르게 포맷 된 폴더 id를 가져오려면 스크립트를 실행 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="4cc3c-161">You have to run the script to get the correctly-formatted folder Ids that can be used in a Content Search.</span></span>
  
<span data-ttu-id="4cc3c-162">다음은 사서함 폴더에 대 한 스크립트에서 반환 하는 출력의 예입니다.</span><span class="sxs-lookup"><span data-stu-id="4cc3c-162">Here's an example of the output returned by the script for mailbox folders.</span></span>
  
![스크립트에서 반환 된 사서함 폴더 및 폴더 id 목록의 예](media/cd739207-eb84-4ebf-a03d-703f3d3a797d.png)
  
<span data-ttu-id="4cc3c-164">2 단계의 예제에서는 사용자의 복구 가능한 항목 폴더에서 제거 하위 폴더를 검색 하는 데 사용 되는 쿼리를 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="4cc3c-164">The example in Step 2 shows the query used to search the Purges subfolder in the user's Recoverable Items folder.</span></span>
  
### <a name="script-output-for-site-folders"></a><span data-ttu-id="4cc3c-165">사이트 폴더의 스크립트 출력</span><span class="sxs-lookup"><span data-stu-id="4cc3c-165">Script output for site folders</span></span>

<span data-ttu-id="4cc3c-166">SharePoint 또는 비즈니스용 OneDrive 사이트에서 **documentlink** 속성의 경로를 가져오는 경우 스크립트는 원격 PowerShell을 사용 하 여 보안 & 준수 센터에 연결 하 고 사이트에서 폴더를 검색 하는 새 콘텐츠 검색을 만듭니다. 지정한 다음 지정 된 사이트에 있는 폴더의 목록을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="4cc3c-166">If you're getting the path of the **documentlink** property from SharePoint or OneDrive for Business sites, the script connects to the Security & Compliance Center using remote PowerShell, creates a new Content Search that searches the site for folders, and then displays a list of the folders located in the specified site.</span></span> <span data-ttu-id="4cc3c-167">스크립트는 각 폴더의 이름을 표시 하 고 폴더 URL에 **documentlink** 의 접두사를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="4cc3c-167">The script displays the name of each folder and adds the prefix of **documentlink** to the folder URL.</span></span> <span data-ttu-id="4cc3c-168">**documentlink** 속성은 검색 가능한 속성 이므로 2 단계의 검색 쿼리에서 property `documentlink:<path>` : value 쌍을 사용 하 여 해당 폴더를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="4cc3c-168">Because the **documentlink** property is a searchable property, you'll use `documentlink:<path>` property:value pair in a search query in Step 2 to search that folder.</span></span> 
  
<span data-ttu-id="4cc3c-169">다음은 사이트 폴더 스크립트에서 반환 하는 출력의 예입니다.</span><span class="sxs-lookup"><span data-stu-id="4cc3c-169">Here's an example of the output returned by the script for site folders.</span></span>
  
![스크립트에서 반환 하는 사이트 폴더의 documentlink 이름 목록 예제](media/519e8347-7365-4067-af78-96c465dc3d15.png)
  
## <a name="step-2-use-a-folder-id-or-documentlink-to-perform-a-targeted-collection"></a><span data-ttu-id="4cc3c-171">2 단계: 폴더 ID 또는 documentlink를 사용 하 여 대상 모음을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="4cc3c-171">Step 2: Use a folder ID or documentlink to perform a targeted collection</span></span>

<span data-ttu-id="4cc3c-172">스크립트를 실행 하 여 특정 사용자에 대 한 폴더 id 또는 documentlinks의 목록을 수집한 후에는 다음 단계를 수행 하 여 Security & 준수 센터로 이동한 다음 새 콘텐츠 검색을 만들어 특정 폴더를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="4cc3c-172">After you've run the script to collect a list of folder IDs or documentlinks for a specific user, the next step to go to the Security & Compliance Center and create a new Content Search to search a specific folder.</span></span> <span data-ttu-id="4cc3c-173">콘텐츠 검색 키워드 상자 `folderid:<folderid>` 에서 `documentlink:<path>` 구성 하는 검색 쿼리에 값 쌍을 사용 하거나, **ComplianceSearch** cmdlet을 사용 하는 경우 *contentmatchquery* 매개 변수의 값으로 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4cc3c-173">You'll use the  `folderid:<folderid>` or  `documentlink:<path>` property:value pair in the search query that you configure in the Content Search keyword box (or as the value for the  *ContentMatchQuery*  parameter if you use the **New-ComplianceSearch** cmdlet).</span></span> <span data-ttu-id="4cc3c-174">`folderid` 또는 `documentlink` 속성을 다른 검색 매개 변수 또는 검색 조건과 결합할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4cc3c-174">You can combine the  `folderid` or  `documentlink` property with other search parameters or search conditions.</span></span> <span data-ttu-id="4cc3c-175">쿼리에 `folderid` 또는 `documentlink` 속성만 포함 하면 지정한 폴더에 있는 모든 항목이 검색에 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4cc3c-175">If you only include the  `folderid` or  `documentlink` property in the query, the search will return all items located in the specified folder.</span></span> 
  
1. <span data-ttu-id="4cc3c-176">[https://compliance.microsoft.com](https://compliance.microsoft.com)으로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="4cc3c-176">Go to [https://compliance.microsoft.com](https://compliance.microsoft.com).</span></span>
    
2. <span data-ttu-id="4cc3c-177">1 단계에서 스크립트를 실행 하는 데 사용한 계정 및 자격 증명을 사용 하 여 Office 365에 로그인 합니다.</span><span class="sxs-lookup"><span data-stu-id="4cc3c-177">Sign in to Office 365 using the account and credentials that you used to run the script in Step 1.</span></span>
    
3. <span data-ttu-id="4cc3c-178">보안 & 준수 센터의 왼쪽 창에서 **콘텐츠 검색** **검색** \> 을 클릭 하 고 **새** ![추가 아이콘](media/O365-MDM-CreatePolicy-AddIcon.gif)을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="4cc3c-178">In the left pane of the Security & Compliance Center, click **Search** \> **Content search**, and then click **New** ![Add icon](media/O365-MDM-CreatePolicy-AddIcon.gif).</span></span>
    
4. <span data-ttu-id="4cc3c-179">**새 검색** 페이지에서 콘텐츠 검색의 이름을 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="4cc3c-179">On the **New search** page, type a name for the Content Search.</span></span> <span data-ttu-id="4cc3c-180">이 이름은 조직 내에서 고유해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="4cc3c-180">This name has to be unique in your organization.</span></span> 
    
5. <span data-ttu-id="4cc3c-181">검색 여부에 따라 다음 중 하나를 수행 하 여 사서함 폴더를 검색할지, 사이트 폴더를 **찾습니다**.</span><span class="sxs-lookup"><span data-stu-id="4cc3c-181">Under **Where do you want us to look**, do one of the following, based on whether you're searching a mailbox folder or a site folder:</span></span>
    
    - <span data-ttu-id="4cc3c-182">**검색 하려는 특정 사서함 선택을** 클릭 한 다음 1 단계에서 스크립트를 실행할 때 지정한 것과 동일한 사서함을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="4cc3c-182">Click **Choose specific mailboxes to search** and then add the same mailbox that you specified when you ran the script in Step 1.</span></span> 
    
      <span data-ttu-id="4cc3c-183">또는</span><span class="sxs-lookup"><span data-stu-id="4cc3c-183">Or</span></span>
    
    - <span data-ttu-id="4cc3c-184">검색 하려면 **특정 사이트 선택을** 클릭 한 다음 1 단계에서 스크립트를 실행할 때 지정한 것과 동일한 사이트 URL을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="4cc3c-184">Click **Choose specific sites to search** to search and then add the same site URL that you specified when you ran the script in Step 1.</span></span> 
    
6. <span data-ttu-id="4cc3c-185">**다음**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="4cc3c-185">Click **Next**.</span></span>
    
7. <span data-ttu-id="4cc3c-186">확인할 **작업** 페이지의 키워드 상자에서 1 단계에서 스크립트에 의해 반환 된 `folderid:<folderid>` `documentlink:<path>` 값을 붙여 넣습니다.</span><span class="sxs-lookup"><span data-stu-id="4cc3c-186">In the keyword box on the **What do you want us to look for** page, paste the  `folderid:<folderid>` or  `documentlink:<path>` value that was returned by the script in Step 1.</span></span> 
    
    <span data-ttu-id="4cc3c-187">예를 들어 다음 스크린샷의 쿼리는 사용자의 복구할 수 있는 항목 폴더에 있는 제거 하위 폴더의 모든 항목을 검색 합니다 (제거 하위 폴더 `folderid` 의 속성 값은 1 단계의 스크린샷에 표시 됨).</span><span class="sxs-lookup"><span data-stu-id="4cc3c-187">For example, the query in the following screenshot will search for any item in the Purges subfolder in the user's Recoverable Items folder (the value of the `folderid` property for the Purges subfolder is shown in the screenshot in Step 1):</span></span>
    
    ![검색 쿼리의 키워드 상자에 folderid 또는 documentlink를 붙여 넣습니다.](media/84057516-b663-48a4-a78f-8032a8f8da80.png)
  
8. <span data-ttu-id="4cc3c-189">**검색** 을 클릭 하 여 대상 지정 된 모음 검색을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="4cc3c-189">Click **Search** to start the targeted collection search.</span></span> 
  
### <a name="examples-of-search-queries-for-targeted-collections"></a><span data-ttu-id="4cc3c-190">대상 지정 컬렉션에 대 한 검색 쿼리 예제</span><span class="sxs-lookup"><span data-stu-id="4cc3c-190">Examples of search queries for targeted collections</span></span>

<span data-ttu-id="4cc3c-191">다음은 검색 쿼리의 `folderid` 및 `documentlink` 속성을 사용 하 여 대상 모음을 수행 하는 방법의 몇 가지 예입니다.</span><span class="sxs-lookup"><span data-stu-id="4cc3c-191">Here are some examples of using the  `folderid` and  `documentlink` properties in a search query to perform a targeted collection.</span></span> <span data-ttu-id="4cc3c-192">자리 표시자는 `folderid:<folderid>` 및 `documentlink:<path>` 공간을 절약 하는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4cc3c-192">Note that placeholders are used for  `folderid:<folderid>` and  `documentlink:<path>` to save space.</span></span> 
  
- <span data-ttu-id="4cc3c-193">이 예에서는 서로 다른 세 개의 사서함 폴더를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="4cc3c-193">This example searches three different mailbox folders.</span></span> <span data-ttu-id="4cc3c-194">비슷한 쿼리 구문을 사용 하 여 사용자의 복구 가능한 항목 폴더에서 숨겨진 폴더를 검색할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4cc3c-194">You could use similar query syntax to search the hidden folders in a user's Recoverable Items folder.</span></span>
    
  ```
  folderid:<folderid> OR folderid:<folderid> OR folderid:<folderid>
  ```

- <span data-ttu-id="4cc3c-195">이 예에서는 사서함 폴더에서 정확한 구가 포함 된 항목을 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="4cc3c-195">This example searches a mailbox folder for items that contain an exact phrase.</span></span>
    
  ```
  folderid:<folderid> AND "Contoso financial results"
  ```

- <span data-ttu-id="4cc3c-196">이 예에서는 제목에 "NDA" 문자가 포함 된 문서의 사이트 폴더와 하위 폴더를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="4cc3c-196">This example searches a site folder (and any subfolders) for documents that contain the letters "NDA" in the title.</span></span>
    
  ```
  documentlink:<path> AND filename:nda
  ```

- <span data-ttu-id="4cc3c-197">다음은 날짜 범위 내에서 변경 된 문서의 사이트 폴더와 하위 폴더를 검색 하는 예제입니다.</span><span class="sxs-lookup"><span data-stu-id="4cc3c-197">This example searches a site folder (and any subfolder) for documents there were changed within a date range.</span></span>
    
  ```
  documentlink:<path> AND (lastmodifiedtime>=01/01/2017 AND lastmodifiedtime<=01/21/2017)
  ```
  
## <a name="more-information"></a><span data-ttu-id="4cc3c-198">추가 정보</span><span class="sxs-lookup"><span data-stu-id="4cc3c-198">More information</span></span>

<span data-ttu-id="4cc3c-199">이 문서의 스크립트를 사용 하 여 대상 모음을 수행할 때는 다음 사항을 염두에 두어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="4cc3c-199">Keep the following things in mind when using the script in this article to perform targeted collections.</span></span>
  
- <span data-ttu-id="4cc3c-200">스크립트는 결과에서 폴더를 제거 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4cc3c-200">The script doesn't remove any folders from the results.</span></span> <span data-ttu-id="4cc3c-201">따라서 결과에 나열 된 일부 폴더에는 시스템 생성 콘텐츠가 포함 되어 있기 때문에 검색 되지 않거나 0 개 항목이 반환 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4cc3c-201">So some folders listed in the results might be unsearchable (or return zero items) because they contain system-generated content.</span></span>
    
- <span data-ttu-id="4cc3c-202">이 스크립트는 사용자의 기본 사서함에 대 한 폴더 정보만 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="4cc3c-202">This script only returns folder information for the user's primary mailbox.</span></span> <span data-ttu-id="4cc3c-203">사용자의 보관 사서함에 있는 폴더에 대 한 정보는 반환 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4cc3c-203">It doesn't return information about folders in the user's archive mailbox.</span></span>
    
- <span data-ttu-id="4cc3c-204">사서함 폴더를 검색할 때 지정 된 폴더 (해당 `folderid` 속성으로 식별 됨)만 검색 됩니다. 하위 폴더는 검색 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4cc3c-204">When searching mailbox folders, only the specified folder (identified by its  `folderid` property) will be searched; subfolders won't be searched.</span></span> <span data-ttu-id="4cc3c-205">하위 폴더를 검색 하려면 검색 하려는 하위 폴더에 대 한 폴더 ID를 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="4cc3c-205">To search sub-folders, you need to use the  folder ID for the sub-folder that you want to search.</span></span> 
    
- <span data-ttu-id="4cc3c-206">사이트 폴더를 검색 하면 해당 `documentlink` 속성으로 식별 된 폴더와 모든 하위 폴더가 검색 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4cc3c-206">When searching site folders, the folder (identified by its  `documentlink` property) and all sub-folders will be searched.</span></span> 
    
- <span data-ttu-id="4cc3c-207">검색 쿼리의 `folderid` 속성만 지정 하는 검색 결과를 내보낼 때 첫 번째 내보내기 옵션인 "모든 항목 (인식할 수 없는 형식을 포함 하거나 암호화 됨 또는 다른 이유로 인덱싱되지 않은 것은 제외)을 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4cc3c-207">When exporting the results of a search in which you only specified the `folderid` property in the search query, you can choose the first export option, "All items, excluding ones that have an unrecognized format, are encrypted, or weren't indexed for other reasons."</span></span> <span data-ttu-id="4cc3c-208">폴더 ID는 항상 인덱싱되어 있기 때문에 폴더의 모든 항목은 인덱싱 상태에 관계 없이 항상 내보내집니다.</span><span class="sxs-lookup"><span data-stu-id="4cc3c-208">All items in the folder will always be exported regardless of their indexing status because the folder ID is always indexed.</span></span>
