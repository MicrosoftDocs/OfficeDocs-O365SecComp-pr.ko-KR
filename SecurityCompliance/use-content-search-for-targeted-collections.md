---
title: Office 365에서 콘텐츠 검색을 사용 하 여 대상된 컬렉션에 대 한
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 12/19/2017
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: e3cbc79c-5e97-43d3-8371-9fbc398cd92e
description: 콘텐츠 검색을 사용 하 여 Office 365 보안에서 &amp; 준수 센터를 대상으로 지정 된 모음을 수행 합니다. 대상된 컬렉션 사례에 응답 하는 항목 또는 권한 있는 항목은 한 특정 사서함 이나 사이트 폴더에 있는 판단 하 것을 의미 합니다. 이 문서에서 스크립트를 사용 하 여 폴더 ID 또는 검색 하려면 특정 사이트 또는 사서함 폴더에 대 한 경로 가져옵니다.
ms.openlocfilehash: 3ff0ca00915bce53e9e932316c5ab47884f346b2
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22533021"
---
# <a name="use-content-search-in-office-365-for-targeted-collections"></a>Office 365에서 콘텐츠 검색을 사용 하 여 대상된 컬렉션에 대 한

Office 365 보안에서 콘텐츠 검색 기능 &amp; 준수 센터에는 비즈니스 사이트에 대 한 Exchange 사서함 또는 SharePoint 및 OneDrive에서 특정 폴더를 검색 하 고 UI에서 직접 방법을 제공 하지 않습니다. 그러나 실제 검색 쿼리 구문을 폴더 ID 또는 경로 지정 하 여 특정 폴더 (대상된 컬렉션 라고 함)를 검색 하는 것이 같습니다. 콘텐츠 검색을 사용 하 여 대상된 컬렉션을 수행 하는 사례에 응답 하는 항목 또는 권한 있는 항목은 한 특정 사서함 이나 사이트 폴더에 있는 판단 하 고 있는 경우에 유용 합니다. 사서함 폴더에 대 한 폴더 ID 또는 비즈니스 사이트에 대 한 SharePoint 및 OneDrive 폴더에 대 한 경로 얻으려면이 문서에서 스크립트를 사용할 수 있습니다. 다음 검색 쿼리에서 폴더 ID 또는 경로 사용 하 여 폴더에 있는 항목을 반환 수 있습니다.
  
## <a name="before-you-begin"></a>시작하기 전에

- 보안에서 eDiscovery 관리자 역할 그룹의 구성원 이어야 하는 &amp; 1 단계에서에서 스크립트를 실행 하려면 준수 센터입니다. 자세한 내용은 참조 [Office 365 보안에서 eDiscovery 사용 권한을 할당 &amp; 준수 센터](assign-ediscovery-permissions.md)합니다.
    
    또한 Exchange Online 조직에서 편지 병합 받는 사람 역할을 할당 해야 합니다. 1 단계에서에서 스크립트에 포함 된 **Get-mailboxfolderstatistics** cmdlet을 실행 하는데 필요 합니다. 기본적으로 메일 받는 사람에 게 역할 할당 된 조직 관리 및 받는 사람 관리 역할 그룹에 Exchange Online 합니다. Exchange Online에서 사용 권한을 할당 하는 방법에 대 한 자세한 내용은 [관리 역할 그룹 구성원](https://go.microsoft.com/fwlink/p/?linkid=692102)을 참조 하십시오. 사용자 지정 역할 그룹을 만들 수도 하 고,를 편지 병합 받는 사람 역할을 할당 하 고, 다음 1 단계에서에서 스크립트를 실행 하는 구성원을 추가 수 있습니다. 자세한 내용은 [관리 역할 그룹](https://go.microsoft.com/fwlink/p/?linkid=730688)을 참조 하십시오.
    
- 1 단계에서에서 스크립트를 실행할 때마다 새 원격 PowerShell 세션이 만들어집니다. 따라서 모든 원격 PowerShell 세션을 사용할 수 있습니다를 사용할 수 있습니다. 이러한 문제가 발생 하지 못하도록이, 원격 PowerShell 세션을 현재 연결을 해제 하려면 다음 명령을 실행할 수 있습니다.
    
  ```
  Get-PSSession | Remove-PSSession
  ```

    자세한 내용은 [원격 PowerShell을 사용하여 Exchange Online에 연결](https://go.microsoft.com/fwlink/p/?linkid=396554)을 참조하세요.
    
- 이 스크립트는 최소한의 오류 처리를 포함합니다. 스크립트의 주요 목적은 신속 하 게 사서함 폴더 Id의 목록 표시 또는 대상된 컬렉션을 수행 하는 콘텐츠 검색의 검색 쿼리 구문에서 사용할 수 있는 경로 사이트 됩니다.
    
- 이 항목에 제공 된 샘플 스크립트는 Microsoft 표준 지원 프로그램이 나 서비스에서 지원 되지 않습니다. 샘플 스크립트는 어떠한 보증도 없이 있는 그대로 제공 됩니다. Microsoft 추가로 포함 하 여, 제한 되지 않고 하는 모든 묵시적된 보증을 부인 묵시적 보증 상품성 또는 특정 목적에의 적합성입니다. 사용 또는 성능 샘플 스크립트 및 설명서에 발생 하는 위험은 있습니다. 어떠한 이벤트에 Microsoft, 해당 작성자 또는 다른 만들기, 제작, 또는 스크립트의 배달에 참여 하는 모든 책임을 지지 모든 손해에 대해 (포함 하 되, 제한 되지 않고 비즈니스 이익, 영업 중단, 손실 손실에 대 한 손해 비즈니스 정보 또는 기타 금전적 손실을) Microsoft가 그와 같은 손해의 가능성을 사전에 알고 있었던 경우에 사용 또는 설명서를 확인 하는 샘플 스크립트를 사용 하 여 원인으로 발생 합니다.
  
## <a name="step-1-run-the-script-to-get-a-list-of-folders-for-a-mailbox-or-site"></a>1 단계: 사서함 또는 사이트에 대 한 폴더의 목록을 표시 하려면 스크립트를 실행 합니다.

이 첫번째 단계에서 실행 하는 스크립트 사서함 폴더의 목록을 또는 SharePoint 또는 비즈니스 폴더에 대 한 OneDrive 및 해당 폴더 ID 또는 각 폴더에 대 한 경로 반환 됩니다. 이 스크립트를 실행 하는 경우 다음 정보에 대 한 묻는 됩니다 것입니다.
  
- **주소 또는 사이트 URL을 전자 메일로 보내기** Exchange 사서함 폴더의 목록을 반환 하 고 Id 커튼 콜를 더불어의 전자 메일 주소를 입력 합니다. 또는 SharePoint 사이트에 대 한 URL 또는 비즈니스 사이트에 대 한 OneDrive의 지정된 된 사이트에 대 한 경로 목록을 반환할 수를 입력 합니다. 다음은 몇가지 예입니다. 
    
  - **Exchange** -stacig@contoso.onmicrosoft.com 
    
  - **SharePoint** - https://contoso.sharepoint.com/sites/marketing 
    
  - **비즈니스용 OneDrive** - https://contoso-my.sharepoint.com/personal/stacig_contoso_onmicrosoft_com 
    
- **사용자 자격 증명** -스크립트 자격 증명을 사용 하 여 Exchange Online 및 보안에 연결할 &amp; 준수 센터 원격 PowerShell 사용 합니다. 앞에서 설명한 것 처럼 성공적으로이 스크립트를 실행 하려면 적절 한 사용 권한을 할당 해야 합니다.
    
사서함 폴더의 목록을 표시 하거나 경로 이름 사이트:
  
1. .Ps1 파일 이름 접미사를 사용 하 여 Windows PowerShell 스크립트 파일에 다음 텍스트를 저장 예, `GetFolderSearchParameters.ps1`합니다.
    
  ```
  #########################################################################################################
  # This PowerShell script will prompt you for:                             #
  #    * Admin credentials for a user who can run the Get-MailboxFolderStatistics cmdlet in Exchange    #
  #      Online and who is an eDiscovery Manager in the Security &amp; Compliance Center.           #
  # The script will then:                                           #
  #    * If an email address is supplied: list the folders for the target mailbox.          #
  #    * If a SharePoint or OneDrive for Business site is supplied: list the folder paths for the site. #
  #    * In both cases, the script supplies the correct search properties (folderid: or path:)      #
  #      appeneded to the folder ID or path ID to use in a Content Search.              #
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
  # Authenticate with Exchange Online and the Security &amp; Complaince Center (Exchange Online Protection - EOP)
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
      # Authenticate with the Security &amp; Complaince Center
      if (!$SccSession)
      {
          $SccSession = New-PSSession -ConfigurationName Microsoft.Exchange -ConnectionUri https://ps.compliance.protection.outlook.com/powershell-liveid -Credential $credentials -Authentication Basic -AllowRedirection
          Import-PSSession $SccSession -AllowClobber -DisableNameChecking
      }
      # Clean-up, if the the script was aborted, the search we created might not have been deleted.  Try to do so now.
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

2. 로컬 컴퓨터에서 Windows PowerShell 열고 스크립트를 저장 한 폴더로 이동 합니다.
    
3. 스크립트를 실행 합니다. 예를 들어:
    
      ```
      .\GetFolderSearchParameters.ps1
      ```

4. 이 스크립트는 메시지가 표시 되는 정보를 입력 합니다.
    
    사서함 폴더 또는 지정된 된 사용자에 대 한 사이트 폴더의 목록을 표시 하는 스크립트입니다. 이 창을 통해 폴더 ID 또는 경로 이름에 복사 하 고 2 단계에서에서 검색 쿼리를 붙여넣을 수 있도록 엽니다.
    
    > [!TIP]
    > 컴퓨터 화면에 폴더의 목록을 표시를 하는 대신 텍스트 파일에 스크립트의 출력을 다시 보낼 수 있습니다. 이 파일은 스크립트 위치한 폴더에 저장 됩니다. 예, 텍스트 파일에 출력 하는 스크립트를 착신 전환 하려면 3 단계에서에서 다음 명령을 실행: `.\GetFolderSearchParameters.ps1 > StacigFolderIds.txt` 후에 검색 쿼리를 사용 하 여 파일에서 폴더 ID 또는 경로 복사할 수 있습니다.
  
### <a name="script-output-for-mailbox-folders"></a>사서함 폴더에 대 한 스크립트 출력

사서함 폴더 Id, 들리지 경우 스크립트 원격 PowerShell을 사용 하 여 Exchange Online에 연결, **Get-MailboxFolderStatisics** cmdlet을 실행 하 고 지정 된 사서함에서 폴더의 목록을 표시 합니다. 모든 폴더의 사서함에 대 한 스크립트를 표시 하는 폴더의 이름을 **FolderPath** 열 및 **FolderQuery** 열에 있는 폴더 ID입니다. 스크립트 폴더 id (즉, 사서함 속성의 이름) **폴더 Id** 의 접두사를 추가 하는 또한 **폴더 id** 속성은 검색 가능한 속성 이기 때문에 사용할 `folderid:<folderid>` 에서 해당 폴더를 검색 하려면 2 단계에서에서 검색 쿼리 합니다. 
  
사서함 폴더에 대 한 스크립트에 의해 반환 되는 출력의 예는 다음과 같습니다.
  
![사서함 폴더 및 폴더의 스크립트에 의해 반환 된 Id의 목록 예제](media/cd739207-eb84-4ebf-a03d-703f3d3a797d.png)
  
2 단계에서에서이 예제는 사용자의 복구 가능한 항목 폴더에서 제거 하위 폴더를 검색 하는 데 사용 하는 쿼리를 표시 합니다.
  
### <a name="script-output-for-site-folders"></a>사이트 폴더에 대 한 스크립트 출력

이 스크립트는 보안 연결할 비즈니스 사이트에 대 한 SharePoint 또는 OneDrive에서 경로 들리지, 경우 &amp; 원격 PowerShell을 사용 하 여 준수 센터 만듭니다 폴더에 대 한 사이트를 검색 하 고 다음 폴더의 목록을 표시 하는 새로운 콘텐츠 검색 지정된 된 사이트에 있습니다. 각 폴더의 이름을 표시 하는 폴더 url **경로** (즉, site 속성의 이름)의 접두사를 추가 하는 스크립트입니다. **Path** 속성을 검색 가능한 속성 이기 때문에 사용할 `path:<path>` 에서 해당 폴더를 검색 하려면 2 단계에서에서 검색 쿼리 합니다. 
  
사이트 폴더에 대 한 스크립트에 의해 반환 되는 출력의 예는 다음과 같습니다.
  
![스크립트에 의해 반환 되는 사이트 폴더에 대 한 경로 이름의 목록 예제](media/519e8347-7365-4067-af78-96c465dc3d15.png)
  
## <a name="step-2-use-a-folder-id-or-path-to-perform-a-targeted-collection"></a>2 단계: 폴더 ID 또는 경로 사용 하 여 대상된 컬렉션을 수행 하려면

보안으로 이동 하려면 다음 단계 폴더 Id 또는 특정 사용자에 대 한 경로 목록을 수집 하려면 스크립트를 실행 했을 때 후 &amp; 준수 센터 특정 폴더를 검색 하려면 새 콘텐츠 검색을 만듭니다. 사용 하는 `folderid:<folderid>` 또는 `path:<path>` 콘텐츠 검색 키워드 상자에 (또는 *ContentMatchQuery* 매개 변수는 **새 ComplianceSearch** cmdlet을 사용 하는 경우에 대 한 값으로)를 구성 하는 검색 쿼리에 속성입니다. 결합할 수는 `folderid` 또는 `path` 속성을 다른 매개 변수를 검색 하거나 검색 조건입니다. 만 포함 하는 경우는 `folderid` 또는 `path` 쿼리에 속성을 검색에 지정된 된 폴더에 있는 모든 항목이 반환 됩니다. 
  
> [!NOTE]
> 사용 하 여 `path` 속성 OneDrive 위치를 검색 하려면 검색 결과에서.png,.tiff, 또는.wav 파일을 등의 미디어 파일을 반환 하지 않습니다. 
  
1. 이동 [https://protection.office.com](https://protection.office.com)합니다.
    
2. 계정 및 1 단계에서에서 스크립트를 실행 하는데 사용 되는 자격 증명을 사용 하 여 Office 365에 로그인 합니다.
    
3. 보안의 왼쪽된 창에서 &amp; 준수 센터 클릭 **검색 &amp; 조사** \> **콘텐츠 검색**한 다음 **새로 만들기** 를 클릭 하 고 ![추가 아이콘](media/O365-MDM-CreatePolicy-AddIcon.gif)합니다.
    
4. **새 검색** 페이지에서 콘텐츠 검색의 이름을 입력합니다. 이 이름은 조직 내에서 고유해야 합니다. 
    
5. **수행 하려는 찾을 우리**는 다음 중 하나를 수행 하는 아래에서 여부에 따라 사서함 폴더 또는 사이트 폴더를 검색 합니다.
    
    - **Choose 특정 사서함 검색을** 클릭 하 고 1 단계에서에서 스크립트를 실행 했을 때 지정한 동일한 사서함을 추가 합니다. 
    
      또는
    
    - 검색 한 다음 1 단계에서에서 스크립트를 실행 했을 때 지정한 동일한 사이트 URL을 추가 하려면 **검색 선택 특정 사이트** 클릭 합니다. 
    
6. **다음**을 클릭합니다.
    
7. **실행할 찾을 우리** 페이지에서 키워드 상자에 붙여넣습니다는 `folderid:<folderid>` 또는 `path:<path>` 1 단계에서에서 스크립트에 의해 반환 된 값입니다. 
    
    사용자의 복구 가능한 항목 폴더에서 제거 하위 폴더에 있는 모든 항목에 대 한 다음 스크린샷에 쿼리를 검색 하는 예 (의 값은 `folderid` 제거 하위 폴더에 대 한 속성은 1 단계에서에서 스크린샷에 표시 된):
    
    ![폴더 id 또는 검색 쿼리 키워드 상자에 경로 붙여넣기](media/84057516-b663-48a4-a78f-8032a8f8da80.png)
  
8. **검색** 대상된 컬렉션 검색 시작을 클릭 합니다. 
  
### <a name="examples-of-search-queries-for-targeted-collections"></a>대상된 컬렉션에 대 한 검색 쿼리의 예제

다음은 몇가지 예를 사용 하는 `folderid` 및 `path` 대상된 컬렉션을 수행 하는 검색 쿼리에 속성입니다. 개체 틀에 사용 되는 참고 `folderid:<folderid>` 및 `path:<path>` 공간을 절약 합니다. 
  
- 세개의 서로 다른 사서함 폴더를 검색 하는이 예제입니다. 사용자의 복구 가능한 항목 폴더의 숨겨진된 폴더를 검색 하려면 다음과 비슷한 쿼리 구문을 사용할 수 있습니다.
    
  ```
  folderid:<folderid> OR folderid:<folderid> OR folderid:<folderid>
  ```

- 정확한 구를 포함 하는 항목에 대 한 사서함 폴더를 검색 하는이 예제입니다.
    
  ```
  folderid:<folderid> AND "Contoso financial results"
  ```

- 제목에 "NDA" 문자를 포함 하는 문서에 대 한 사이트 폴더 (및 모든 하위 폴더)를 검색 하는이 예제입니다.
    
  ```
  path:<path> AND filename:nda
  ```

- 이 예제에서는 날짜 범위 내에서 변경 된 문서에 대 한 사이트 폴더 (및 모든 하위 폴더)를 검색 합니다.
    
  ```
  path:<path> AND (lastmodifiedtime>=01/01/2017 AND lastmodifiedtime<=01/21/2017)
  ```
  
## <a name="more-information"></a>추가 정보

이 문서에서 스크립트를 사용 하는 경우 다음 사항에 주의 유지 하 고 모음을 대상으로 수행 합니다.
  
- 스크립트 결과에서 폴더가 제거 되지 않습니다. 일부 폴더에 나열 결과 수 검색할 수 (또는 0 항목을 반환) 시스템에서 생성 된 콘텐츠를 포함 하기 때문입니다.
    
- 이 스크립트는만 사용자의 기본 사서함에 대 한 폴더 정보를 반환 합니다. 사용자의 보관 사서함의 폴더에 대 한 정보를 반환 하지 않습니다 것입니다.
    
- 사서함 폴더를 지정된 된 폴더를 검색 하는 경우 (로 식별 되는 `folderid` 속성)을 검색 합니다. 하위 폴더를 검색할 수 없습니다. 하위 폴더를 검색 하려면 사용 하 여 필요한는 `folderid` 를 검색 하려면 하위 폴더에 대 한 합니다. 
    
- 사이트 폴더, 폴더를 검색 하는 경우 (로 식별 되는 `path` 속성) 및 모든 하위 폴더를 검색 합니다. 
    
- 앞서 설명한 것 처럼 사용할 수 없습니다 `path` OneDrive 위치에 있는 속성을.png,.tiff,.wav 파일 등의 미디어 파일을 검색 합니다. OneDrive 폴더의 미디어 파일을 검색 하려면 다른 [사이트 속성](keyword-queries-and-search-conditions.md#searchable-site-properties) 을 사용 합니다. 
