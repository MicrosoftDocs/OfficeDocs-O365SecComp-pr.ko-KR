---
title: Office 365에서 콘텐츠 검색을 사용 하 여 대상된 컬렉션에 대 한
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 10/12/2018
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid: MOE150
ms.assetid: e3cbc79c-5e97-43d3-8371-9fbc398cd92e
description: 콘텐츠 검색을 사용 하 여 Office 365 보안에서 &amp; 준수 센터를 대상으로 지정 된 모음을 수행 합니다. 대상된 컬렉션 사례에 응답 하는 항목 또는 권한 있는 항목은 한 특정 사서함 이나 사이트 폴더에 있는 판단 하 것을 의미 합니다. 이 문서에서 스크립트를 사용 하 여 폴더 ID 또는 검색 하려면 특정 사이트 또는 사서함 폴더에 대 한 경로 가져옵니다.
ms.openlocfilehash: f4bb63a193a11e7467b3b296b2bdfa50657ae65a
ms.sourcegitcommit: 448c5897e44448adfc82e3eaffb774c770c04815
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/12/2018
ms.locfileid: "25522289"
---
# <a name="use-content-search-in-office-365-for-targeted-collections"></a><span data-ttu-id="ec11b-105">Office 365에서 콘텐츠 검색을 사용 하 여 대상된 컬렉션에 대 한</span><span class="sxs-lookup"><span data-stu-id="ec11b-105">Use Content Search in Office 365 for targeted collections</span></span>

<span data-ttu-id="ec11b-p102">Office 365 보안에서 콘텐츠 검색 기능 &amp; 준수 센터에는 비즈니스 사이트에 대 한 Exchange 사서함 또는 SharePoint 및 OneDrive에서 특정 폴더를 검색 하 고 UI에서 직접 방법을 제공 하지 않습니다. 그러나 실제 검색 쿼리 구문을 폴더 ID 또는 경로 지정 하 여 특정 폴더 (대상된 컬렉션 라고 함)를 검색 하는 것이 같습니다. 콘텐츠 검색을 사용 하 여 대상된 컬렉션을 수행 하는 사례에 응답 하는 항목 또는 권한 있는 항목은 한 특정 사서함 이나 사이트 폴더에 있는 판단 하 고 있는 경우에 유용 합니다. 사서함 폴더에 대 한 폴더 ID 또는 비즈니스 사이트에 대 한 SharePoint 및 OneDrive 폴더에 대 한 경로 얻으려면이 문서에서 스크립트를 사용할 수 있습니다. 다음 검색 쿼리에서 폴더 ID 또는 경로 사용 하 여 폴더에 있는 항목을 반환 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ec11b-p102">The Content Search feature in the Office 365 Security &amp; Compliance Center doesn't provide a direct way in the UI to search specific folders in Exchange mailboxes or SharePoint and OneDrive for Business sites. However, it is possible to search specific folders (called a targeted collection) by specifying the folder ID or path in the actual search query syntax. Using Content Search to perform a targeted collection is useful when you're confident that items responsive to a case or privileged items are located in a specific mailbox or site folder. You can use the script in this article to obtain the folder ID for mailbox folders or the path for folders on a SharePoint and OneDrive for Business site. Then you can use the folder ID or path in a search query to return items located in the folder.</span></span>
  
## <a name="before-you-begin"></a><span data-ttu-id="ec11b-111">시작하기 전에</span><span class="sxs-lookup"><span data-stu-id="ec11b-111">Before you begin</span></span>

- <span data-ttu-id="ec11b-p103">보안에서 eDiscovery 관리자 역할 그룹의 구성원 이어야 하는 &amp; 1 단계에서에서 스크립트를 실행 하려면 준수 센터입니다. 자세한 내용은 참조 [Office 365 보안에서 eDiscovery 사용 권한을 할당 &amp; 준수 센터](assign-ediscovery-permissions.md)합니다.</span><span class="sxs-lookup"><span data-stu-id="ec11b-p103">You have to be a member of the eDiscovery Manager role group in the Security &amp; Compliance Center to run the script in Step 1. For more information, see [Assign eDiscovery permissions in the Office‍ 365 Security &amp; Compliance Center](assign-ediscovery-permissions.md).</span></span>
    
    <span data-ttu-id="ec11b-p104">또한 Exchange Online 조직에서 편지 병합 받는 사람 역할을 할당 해야 합니다. 1 단계에서에서 스크립트에 포함 된 **Get-mailboxfolderstatistics** cmdlet을 실행 하는데 필요 합니다. 기본적으로 메일 받는 사람에 게 역할 할당 된 조직 관리 및 받는 사람 관리 역할 그룹에 Exchange Online 합니다. Exchange Online에서 사용 권한을 할당 하는 방법에 대 한 자세한 내용은 [관리 역할 그룹 구성원](https://go.microsoft.com/fwlink/p/?linkid=692102)을 참조 하십시오. 사용자 지정 역할 그룹을 만들 수도 하 고,를 편지 병합 받는 사람 역할을 할당 하 고, 다음 1 단계에서에서 스크립트를 실행 하는 구성원을 추가 수 있습니다. 자세한 내용은 [관리 역할 그룹](https://go.microsoft.com/fwlink/p/?linkid=730688)을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="ec11b-p104">Additionally, you have to be assigned the Mail Recipients role in your Exchange Online organization. This is required to run the **Get-MailboxFolderStatistics** cmdlet, which is included in the script in Step 1. By default, the Mail Recipients role is assigned to the Organization Management and Recipient Management role groups in Exchange Online. For more information about assigning permissions in Exchange Online, see [Manage role group members](https://go.microsoft.com/fwlink/p/?linkid=692102). You could also create a custom role group, assign the Mail Recipients role to it, and then add the members who need to run the script in Step 1. For more information, see [Manage role groups](https://go.microsoft.com/fwlink/p/?linkid=730688).</span></span>
    
- <span data-ttu-id="ec11b-p105">1 단계에서에서 스크립트를 실행할 때마다 새 원격 PowerShell 세션이 만들어집니다. 따라서 모든 원격 PowerShell 세션을 사용할 수 있습니다를 사용할 수 있습니다. 이러한 문제가 발생 하지 못하도록이, 원격 PowerShell 세션을 현재 연결을 해제 하려면 다음 명령을 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ec11b-p105">Each time you run the script in Step 1, a new remote PowerShell session is created. So you could use up all the remote PowerShell sessions available to you. To prevent this from happening, you can run the following command to disconnect your active remote PowerShell sessions.</span></span>
    
  ```
  Get-PSSession | Remove-PSSession
  ```

    <span data-ttu-id="ec11b-123">자세한 내용은 [원격 PowerShell을 사용하여 Exchange Online에 연결](https://go.microsoft.com/fwlink/p/?linkid=396554)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="ec11b-123">For more information, see [Connect to Exchange Online PowerShell](https://go.microsoft.com/fwlink/p/?linkid=396554).</span></span>
    
- <span data-ttu-id="ec11b-p106">이 스크립트는 최소한의 오류 처리를 포함합니다. 스크립트의 주요 목적은 신속 하 게 사서함 폴더 Id의 목록 표시 또는 대상된 컬렉션을 수행 하는 콘텐츠 검색의 검색 쿼리 구문에서 사용할 수 있는 경로 사이트 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ec11b-p106">The script includes minimal error handling. The primary purpose of the script is to quickly display a list of mailbox folder IDs or site paths that can be used in the search query syntax of a Content Search to perform a targeted collection.</span></span>
    
- <span data-ttu-id="ec11b-p107">이 항목에 제공 된 샘플 스크립트는 Microsoft 표준 지원 프로그램이 나 서비스에서 지원 되지 않습니다. 샘플 스크립트는 어떠한 보증도 없이 있는 그대로 제공 됩니다. Microsoft 추가로 포함 하 여, 제한 되지 않고 하는 모든 묵시적된 보증을 부인 묵시적 보증 상품성 또는 특정 목적에의 적합성입니다. 사용 또는 성능 샘플 스크립트 및 설명서에 발생 하는 위험은 있습니다. 어떠한 이벤트에 Microsoft, 해당 작성자 또는 다른 만들기, 제작, 또는 스크립트의 배달에 참여 하는 모든 책임을 지지 모든 손해에 대해 (포함 하 되, 제한 되지 않고 비즈니스 이익, 영업 중단, 손실 손실에 대 한 손해 비즈니스 정보 또는 기타 금전적 손실을) Microsoft가 그와 같은 손해의 가능성을 사전에 알고 있었던 경우에 사용 또는 설명서를 확인 하는 샘플 스크립트를 사용 하 여 원인으로 발생 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec11b-p107">The sample script provided in this topic isn't supported under any Microsoft standard support program or service. The sample script is provided AS IS without warranty of any kind. Microsoft further disclaims all implied warranties including, without limitation, any implied warranties of merchantability or of fitness for a particular purpose. The entire risk arising out of the use or performance of the sample script and documentation remains with you. In no event shall Microsoft, its authors, or anyone else involved in the creation, production, or delivery of the scripts be liable for any damages whatsoever (including, without limitation, damages for loss of business profits, business interruption, loss of business information, or other pecuniary loss) arising out of the use of or inability to use the sample scripts or documentation, even if Microsoft has been advised of the possibility of such damages.</span></span>
  
## <a name="step-1-run-the-script-to-get-a-list-of-folders-for-a-mailbox-or-site"></a><span data-ttu-id="ec11b-131">1 단계: 사서함 또는 사이트에 대 한 폴더의 목록을 표시 하려면 스크립트를 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec11b-131">Step 1: Run the script to get a list of folders for a mailbox or site</span></span>

<span data-ttu-id="ec11b-p108">이 첫번째 단계에서 실행 하는 스크립트 사서함 폴더의 목록을 또는 SharePoint 또는 비즈니스 폴더에 대 한 OneDrive 및 해당 폴더 ID 또는 각 폴더에 대 한 경로 반환 됩니다. 이 스크립트를 실행 하는 경우 다음 정보에 대 한 묻는 됩니다 것입니다.</span><span class="sxs-lookup"><span data-stu-id="ec11b-p108">The script that you run in this first step will return a list of mailbox folders or SharePoint or OneDrive for Business folders, and the corresponding folder ID or path for each folder. When you run this script, it will prompt you for the following information.</span></span>
  
- <span data-ttu-id="ec11b-p109">**주소 또는 사이트 URL을 전자 메일로 보내기** Exchange 사서함 폴더의 목록을 반환 하 고 Id 커튼 콜를 더불어의 전자 메일 주소를 입력 합니다. 또는 SharePoint 사이트에 대 한 URL 또는 비즈니스 사이트에 대 한 OneDrive의 지정된 된 사이트에 대 한 경로 목록을 반환할 수를 입력 합니다. 다음은 몇가지 예입니다.</span><span class="sxs-lookup"><span data-stu-id="ec11b-p109">**Email address or site URL** Type an email address of the custodian to return a list of Exchange mailbox folders and fold IDs. Or type the URL for a SharePoint site or a OneDrive for Business site to return a list of paths for the specified site. Here are some examples:</span></span> 
    
  - <span data-ttu-id="ec11b-137">**Exchange** -stacig@contoso.onmicrosoft.com</span><span class="sxs-lookup"><span data-stu-id="ec11b-137">**Exchange** - stacig@contoso.onmicrosoft.com</span></span> 
    
  - <span data-ttu-id="ec11b-138">**SharePoint** - https://contoso.sharepoint.com/sites/marketing</span><span class="sxs-lookup"><span data-stu-id="ec11b-138">**SharePoint** - https://contoso.sharepoint.com/sites/marketing</span></span> 
    
  - <span data-ttu-id="ec11b-139">**비즈니스용 OneDrive** - https://contoso-my.sharepoint.com/personal/stacig_contoso_onmicrosoft_com</span><span class="sxs-lookup"><span data-stu-id="ec11b-139">**OneDrive for Business** - https://contoso-my.sharepoint.com/personal/stacig_contoso_onmicrosoft_com</span></span> 
    
- <span data-ttu-id="ec11b-p110">**사용자 자격 증명** -스크립트 자격 증명을 사용 하 여 Exchange Online 및 보안에 연결할 &amp; 준수 센터 원격 PowerShell 사용 합니다. 앞에서 설명한 것 처럼 성공적으로이 스크립트를 실행 하려면 적절 한 사용 권한을 할당 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec11b-p110">**Your user credentials** - The script will use your credentials to connect to Exchange Online and the Security &amp; Compliance Center with remote PowerShell. As previously explained, you have to assigned the appropriate permissions to successfully run this script.</span></span>
    
<span data-ttu-id="ec11b-142">사서함 폴더의 목록을 표시 하거나 경로 이름 사이트:</span><span class="sxs-lookup"><span data-stu-id="ec11b-142">To display a list of mailbox folders or site path names:</span></span>
  
1. <span data-ttu-id="ec11b-143">.Ps1 파일 이름 접미사를 사용 하 여 Windows PowerShell 스크립트 파일에 다음 텍스트를 저장 예, `GetFolderSearchParameters.ps1`합니다.</span><span class="sxs-lookup"><span data-stu-id="ec11b-143">Save the following text to a Windows PowerShell script file by using a filename suffix of .ps1; for example, `GetFolderSearchParameters.ps1`.</span></span>
    
  ```
  #########################################################################################################
  # This PowerShell script will prompt you for:                             #
  #    * Admin credentials for a user who can run the Get-MailboxFolderStatistics cmdlet in Exchange    #
  #      Online and who is an eDiscovery Manager in the Security &amp; Compliance Center.           #
  # The script will then:                                           #
  #    * If an email address is supplied: list the folders for the target mailbox.          #
  #    * If a SharePoint or OneDrive for Business site is supplied: list the folder paths for the site. #
  #    * In both cases, the script supplies the correct search properties (folderid: or path:)      #
  #      appended to the folder ID or path ID to use in a Content Search.               #
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
          # Create a Complinace Search Action and wait for it to complete. The folders will be listed in the .Results parameter
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
              Write-Host "path:""$rawUrl"""
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

2. <span data-ttu-id="ec11b-144">로컬 컴퓨터에서 Windows PowerShell 열고 스크립트를 저장 한 폴더로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec11b-144">On your local computer, open Windows PowerShell and go to the folder where you saved the script.</span></span>
    
3. <span data-ttu-id="ec11b-145">스크립트를 실행 합니다. 예를 들어:</span><span class="sxs-lookup"><span data-stu-id="ec11b-145">Run the script; for example:</span></span>
    
      ```
      .\GetFolderSearchParameters.ps1
      ```

4. <span data-ttu-id="ec11b-146">이 스크립트는 메시지가 표시 되는 정보를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec11b-146">Enter the information that the script prompts you for.</span></span>
    
    <span data-ttu-id="ec11b-p111">사서함 폴더 또는 지정된 된 사용자에 대 한 사이트 폴더의 목록을 표시 하는 스크립트입니다. 이 창을 통해 폴더 ID 또는 경로 이름에 복사 하 고 2 단계에서에서 검색 쿼리를 붙여넣을 수 있도록 엽니다.</span><span class="sxs-lookup"><span data-stu-id="ec11b-p111">The script displays a list of mailbox folders or site folder for the specified user. Let this window open so that you can copy a folder ID or path name and paste it in to a search query in Step 2.</span></span>
    
    > [!TIP]
    > <span data-ttu-id="ec11b-p112">컴퓨터 화면에 폴더의 목록을 표시를 하는 대신 텍스트 파일에 스크립트의 출력을 다시 보낼 수 있습니다. 이 파일은 스크립트 위치한 폴더에 저장 됩니다. 예, 텍스트 파일에 출력 하는 스크립트를 착신 전환 하려면 3 단계에서에서 다음 명령을 실행: `.\GetFolderSearchParameters.ps1 > StacigFolderIds.txt` 후에 검색 쿼리를 사용 하 여 파일에서 폴더 ID 또는 경로 복사할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ec11b-p112">Instead of displaying a list of folders on the computer screen, you can re-direct the output of the script to a text file. This file will be saved to the folder where the script is located. For example, to redirect the script output to a text file, run the following command in Step 3:  `.\GetFolderSearchParameters.ps1 > StacigFolderIds.txt` Then you can copy a folder ID or path from the file to use in a search query.</span></span>
  
### <a name="script-output-for-mailbox-folders"></a><span data-ttu-id="ec11b-152">사서함 폴더에 대 한 스크립트 출력</span><span class="sxs-lookup"><span data-stu-id="ec11b-152">Script output for mailbox folders</span></span>

<span data-ttu-id="ec11b-p113">사서함 폴더 Id, 들리지 경우 스크립트 원격 PowerShell을 사용 하 여 Exchange Online에 연결, **Get-MailboxFolderStatisics** cmdlet을 실행 하 고 지정 된 사서함에서 폴더의 목록을 표시 합니다. 모든 폴더의 사서함에 대 한 스크립트를 표시 하는 폴더의 이름을 **FolderPath** 열 및 **FolderQuery** 열에 있는 폴더 ID입니다. 스크립트 폴더 id (즉, 사서함 속성의 이름) **폴더 Id** 의 접두사를 추가 하는 또한 **폴더 id** 속성은 검색 가능한 속성 이기 때문에 사용할 `folderid:<folderid>` 에서 해당 폴더를 검색 하려면 2 단계에서에서 검색 쿼리 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec11b-p113">If you're getting mailbox folder IDs, the script connects to Exchange Online by using remote PowerShell, runs the **Get-MailboxFolderStatisics** cmdlet, and then displays the list of the folders from the specified mailbox. For every folder in the mailbox, the script displays the name of the folder in the **FolderPath** column and the folder ID in the **FolderQuery** column. Additionally, the script adds the prefix of **folderId** (which is the name of the mailbox property) to the folder ID. Because the **folderid** property is a searchable property, you'll use  `folderid:<folderid>` in a search query in Step 2 to search that folder.</span></span> 
  
<span data-ttu-id="ec11b-157">사서함 폴더에 대 한 스크립트에 의해 반환 되는 출력의 예는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="ec11b-157">Here's an example of the output returned by the script for mailbox folders.</span></span>
  
![사서함 폴더 및 폴더의 스크립트에 의해 반환 된 Id의 목록 예제](media/cd739207-eb84-4ebf-a03d-703f3d3a797d.png)
  
<span data-ttu-id="ec11b-159">2 단계에서에서이 예제는 사용자의 복구 가능한 항목 폴더에서 제거 하위 폴더를 검색 하는 데 사용 하는 쿼리를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec11b-159">The example in Step 2 shows the query used to search the Purges subfolder in the user's Recoverable Items folder.</span></span>
  
### <a name="script-output-for-site-folders"></a><span data-ttu-id="ec11b-160">사이트 폴더에 대 한 스크립트 출력</span><span class="sxs-lookup"><span data-stu-id="ec11b-160">Script output for site folders</span></span>

<span data-ttu-id="ec11b-p114">이 스크립트는 보안 연결할 비즈니스 사이트에 대 한 SharePoint 또는 OneDrive에서 경로 들리지, 경우 &amp; 원격 PowerShell을 사용 하 여 준수 센터 만듭니다 폴더에 대 한 사이트를 검색 하 고 다음 폴더의 목록을 표시 하는 새로운 콘텐츠 검색 지정된 된 사이트에 있습니다. 각 폴더의 이름을 표시 하는 폴더 url **경로** (즉, site 속성의 이름)의 접두사를 추가 하는 스크립트입니다. **Path** 속성을 검색 가능한 속성 이기 때문에 사용할 `path:<path>` 에서 해당 폴더를 검색 하려면 2 단계에서에서 검색 쿼리 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec11b-p114">If you're getting paths from SharePoint or OneDrive for Business sites, the script connects to the Security &amp; Compliance Center using remote PowerShell, creates a new Content Search that searches the site for folders, and then displays a list of the folders located in the specified site. The script displays the name of each folder and adds the prefix of **path** (which is the name of the site property) to the folder URL. Because the **path** property is a searchable property, you'll use  `path:<path>` in a search query in Step 2 to search that folder.</span></span> 
  
<span data-ttu-id="ec11b-164">사이트 폴더에 대 한 스크립트에 의해 반환 되는 출력의 예는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="ec11b-164">Here's an example of the output returned by the script for site folders.</span></span>
  
![스크립트에 의해 반환 되는 사이트 폴더에 대 한 경로 이름의 목록 예제](media/519e8347-7365-4067-af78-96c465dc3d15.png)
  
## <a name="step-2-use-a-folder-id-or-path-to-perform-a-targeted-collection"></a><span data-ttu-id="ec11b-166">2 단계: 폴더 ID 또는 경로 사용 하 여 대상된 컬렉션을 수행 하려면</span><span class="sxs-lookup"><span data-stu-id="ec11b-166">Step 2: Use a folder ID or path to perform a targeted collection</span></span>

<span data-ttu-id="ec11b-p115">보안으로 이동 하려면 다음 단계 폴더 Id 또는 특정 사용자에 대 한 경로 목록을 수집 하려면 스크립트를 실행 했을 때 후 &amp; 준수 센터 특정 폴더를 검색 하려면 새 콘텐츠 검색을 만듭니다. 사용 하는 `folderid:<folderid>` 또는 `path:<path>` 콘텐츠 검색 키워드 상자에 (또는 *ContentMatchQuery* 매개 변수는 **새 ComplianceSearch** cmdlet을 사용 하는 경우에 대 한 값으로)를 구성 하는 검색 쿼리에 속성입니다. 결합할 수는 `folderid` 또는 `path` 속성을 다른 매개 변수를 검색 하거나 검색 조건입니다. 만 포함 하는 경우는 `folderid` 또는 `path` 쿼리에 속성을 검색에 지정된 된 폴더에 있는 모든 항목이 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ec11b-p115">After you've run the script to collect a list of folder IDs or paths for a specific user, the next step to go to the Security &amp; Compliance Center and create a new Content Search to search a specific folder. You'll use the  `folderid:<folderid>` or  `path:<path>` property in the search query that you configure in the Content Search keyword box (or as the value for the  *ContentMatchQuery*  parameter if you use the **New-ComplianceSearch** cmdlet). You can combine the  `folderid` or  `path` property with other search parameters or search conditions. If you only include the  `folderid` or  `path` property in the query, the search will return all items located in the specified folder.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="ec11b-171">사용 하 여 `path` 속성 OneDrive 위치를 검색 하려면 검색 결과에서.png,.tiff, 또는.wav 파일을 등의 미디어 파일을 반환 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ec11b-171">Using the  `path` property to search OneDrive locations won't return media files, such as .png, .tiff, or .wav files, in the search results.</span></span> 
  
1. <span data-ttu-id="ec11b-172">[https://protection.office.com](https://protection.office.com)으로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="ec11b-172">Go to [https://protection.office.com](https://protection.office.com).</span></span>
    
2. <span data-ttu-id="ec11b-173">계정 및 1 단계에서에서 스크립트를 실행 하는데 사용 되는 자격 증명을 사용 하 여 Office 365에 로그인 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec11b-173">Sign in to Office 365 using the account and credentials that you used to run the script in Step 1.</span></span>
    
3. <span data-ttu-id="ec11b-174">보안의 왼쪽된 창에서 &amp; 준수 센터 클릭 **검색 &amp; 조사** \> **콘텐츠 검색**한 다음 **새로 만들기** 를 클릭 하 고 ![추가 아이콘](media/O365-MDM-CreatePolicy-AddIcon.gif)합니다.</span><span class="sxs-lookup"><span data-stu-id="ec11b-174">In the left pane of the Security &amp; Compliance Center, click **Search &amp; investigation** \> **Content search**, and then click **New** ![Add icon](media/O365-MDM-CreatePolicy-AddIcon.gif).</span></span>
    
4. <span data-ttu-id="ec11b-p116">**새 검색** 페이지에서 콘텐츠 검색의 이름을 입력합니다. 이 이름은 조직 내에서 고유해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec11b-p116">On the **New search** page, type a name for the Content Search. This name has to be unique in your organization.</span></span> 
    
5. <span data-ttu-id="ec11b-177">**수행 하려는 찾을 우리**는 다음 중 하나를 수행 하는 아래에서 여부에 따라 사서함 폴더 또는 사이트 폴더를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec11b-177">Under **Where do you want us to look**, do one of the following, based on whether your searching a mailbox folder or a site folder:</span></span>
    
    - <span data-ttu-id="ec11b-178">**Choose 특정 사서함 검색을** 클릭 하 고 1 단계에서에서 스크립트를 실행 했을 때 지정한 동일한 사서함을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec11b-178">Click **Choose specific mailboxes to search** and then add the same mailbox that you specified when you ran the script in Step 1.</span></span> 
    
      <span data-ttu-id="ec11b-179">또는</span><span class="sxs-lookup"><span data-stu-id="ec11b-179">Or</span></span>
    
    - <span data-ttu-id="ec11b-180">검색 한 다음 1 단계에서에서 스크립트를 실행 했을 때 지정한 동일한 사이트 URL을 추가 하려면 **검색 선택 특정 사이트** 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec11b-180">Click **Choose specific sites to search** to search and then add the same site URL that you specified when you ran the script in Step 1.</span></span> 
    
6. <span data-ttu-id="ec11b-181">**다음**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="ec11b-181">Click **Next**.</span></span>
    
7. <span data-ttu-id="ec11b-182">**실행할 찾을 우리** 페이지에서 키워드 상자에 붙여넣습니다는 `folderid:<folderid>` 또는 `path:<path>` 1 단계에서에서 스크립트에 의해 반환 된 값입니다.</span><span class="sxs-lookup"><span data-stu-id="ec11b-182">In the keyword box on the **What do you want us to look for** page, paste the  `folderid:<folderid>` or  `path:<path>` value that was returned by the script in Step 1.</span></span> 
    
    <span data-ttu-id="ec11b-183">사용자의 복구 가능한 항목 폴더에서 제거 하위 폴더에 있는 모든 항목에 대 한 다음 스크린샷에 쿼리를 검색 하는 예 (의 값은 `folderid` 제거 하위 폴더에 대 한 속성은 1 단계에서에서 스크린샷에 표시 된):</span><span class="sxs-lookup"><span data-stu-id="ec11b-183">For example, the query in the following screenshot will search for any item in the Purges subfolder in the user's Recoverable Items folder (the value of the `folderid` property for the Purges subfolder is shown in the screenshot in Step 1):</span></span>
    
    ![폴더 id 또는 검색 쿼리 키워드 상자에 경로 붙여넣기](media/84057516-b663-48a4-a78f-8032a8f8da80.png)
  
8. <span data-ttu-id="ec11b-185">**검색** 대상된 컬렉션 검색 시작을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec11b-185">Click **Search** to start the targeted collection search.</span></span> 
  
### <a name="examples-of-search-queries-for-targeted-collections"></a><span data-ttu-id="ec11b-186">대상된 컬렉션에 대 한 검색 쿼리의 예제</span><span class="sxs-lookup"><span data-stu-id="ec11b-186">Examples of search queries for targeted collections</span></span>

<span data-ttu-id="ec11b-p117">다음은 몇가지 예를 사용 하는 `folderid` 및 `path` 대상된 컬렉션을 수행 하는 검색 쿼리에 속성입니다. 개체 틀에 사용 되는 참고 `folderid:<folderid>` 및 `path:<path>` 공간을 절약 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec11b-p117">Here are some examples of using the  `folderid` and  `path` properties in a search query to perform a targeted collection. Note that placeholders are used for  `folderid:<folderid>` and  `path:<path>` to save space.</span></span> 
  
- <span data-ttu-id="ec11b-p118">세개의 서로 다른 사서함 폴더를 검색 하는이 예제입니다. 사용자의 복구 가능한 항목 폴더의 숨겨진된 폴더를 검색 하려면 다음과 비슷한 쿼리 구문을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ec11b-p118">This example searches three different mailbox folders. You could use similar query syntax to search the hidden folders in a user's Recoverable Items folder.</span></span>
    
  ```
  folderid:<folderid> OR folderid:<folderid> OR folderid:<folderid>
  ```

- <span data-ttu-id="ec11b-191">정확한 구를 포함 하는 항목에 대 한 사서함 폴더를 검색 하는이 예제입니다.</span><span class="sxs-lookup"><span data-stu-id="ec11b-191">This example searches a mailbox folder for items that contain an exact phrase.</span></span>
    
  ```
  folderid:<folderid> AND "Contoso financial results"
  ```

- <span data-ttu-id="ec11b-192">제목에 "NDA" 문자를 포함 하는 문서에 대 한 사이트 폴더 (및 모든 하위 폴더)를 검색 하는이 예제입니다.</span><span class="sxs-lookup"><span data-stu-id="ec11b-192">This example searches a site folder (and any subfolders) for documents that contain the letters "NDA" in the title.</span></span>
    
  ```
  path:<path> AND filename:nda
  ```

- <span data-ttu-id="ec11b-193">이 예제에서는 날짜 범위 내에서 변경 된 문서에 대 한 사이트 폴더 (및 모든 하위 폴더)를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec11b-193">This example searches a site folder (and any subfolder) for documents there were changed within a date range.</span></span>
    
  ```
  path:<path> AND (lastmodifiedtime>=01/01/2017 AND lastmodifiedtime<=01/21/2017)
  ```
  
## <a name="more-information"></a><span data-ttu-id="ec11b-194">추가 정보</span><span class="sxs-lookup"><span data-stu-id="ec11b-194">More information</span></span>

<span data-ttu-id="ec11b-195">이 문서에서 스크립트를 사용 하는 경우 다음 사항에 주의 유지 하 고 모음을 대상으로 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec11b-195">Keep the following things in mind when using the script in this article and performing targeted collections.</span></span>
  
- <span data-ttu-id="ec11b-p119">스크립트 결과에서 폴더가 제거 되지 않습니다. 일부 폴더에 나열 결과 수 검색할 수 (또는 0 항목을 반환) 시스템에서 생성 된 콘텐츠를 포함 하기 때문입니다.</span><span class="sxs-lookup"><span data-stu-id="ec11b-p119">The script doesn't remove any folders from the results. So some folders listed in the results might be unsearchable (or return zero items) because they contain system-generated content.</span></span>
    
- <span data-ttu-id="ec11b-p120">이 스크립트는만 사용자의 기본 사서함에 대 한 폴더 정보를 반환 합니다. 사용자의 보관 사서함의 폴더에 대 한 정보를 반환 하지 않습니다 것입니다.</span><span class="sxs-lookup"><span data-stu-id="ec11b-p120">This script only returns folder information for the user's primary mailbox. It doesn't return information about folders in the user's archive mailbox.</span></span>
    
- <span data-ttu-id="ec11b-p121">사서함 폴더를 지정된 된 폴더를 검색 하는 경우 (로 식별 되는 `folderid` 속성)을 검색 합니다. 하위 폴더를 검색할 수 없습니다. 하위 폴더를 검색 하려면 사용 하 여 필요한는 `folderid` 를 검색 하려면 하위 폴더에 대 한 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec11b-p121">When searching mailbox folders, only the specified folder (identified by its  `folderid` property) will be searched. Subfolders won't be searched. To search sub-folders, you need to use the  `folderid` for the sub-folder that you want to search.</span></span> 
    
- <span data-ttu-id="ec11b-203">사이트 폴더, 폴더를 검색 하는 경우 (로 식별 되는 `path` 속성) 및 모든 하위 폴더를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec11b-203">When searching site folders, the folder (identified by its  `path` property) and all sub-folders will be searched.</span></span> 
    
- <span data-ttu-id="ec11b-p122">앞서 설명한 것 처럼 사용할 수 없습니다 `path` OneDrive 위치에 있는 속성을.png,.tiff,.wav 파일 등의 미디어 파일을 검색 합니다. OneDrive 폴더의 미디어 파일을 검색 하려면 다른 [사이트 속성](keyword-queries-and-search-conditions.md#searchable-site-properties) 을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec11b-p122">As previously stated, you can't use  `path` property to search for media files, such as .png, .tiff, or .wav files, located in OneDrive locations. Use a different [site property](keyword-queries-and-search-conditions.md#searchable-site-properties) to search for media files in OneDrive folders.</span></span> 
