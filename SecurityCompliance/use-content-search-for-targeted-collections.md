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
description: 보안 & 준수 센터에서 콘텐츠 검색을 사용 하 여 대상 지정 된 컬렉션을 수행 합니다. 대상 컬렉션은 사례 또는 권한이 부여 된 항목에 대 한 응답 항목이 특정 사서함 또는 사이트 폴더에 있는 것을 확신 함을 의미 합니다. 이 문서의 스크립트를 사용 하 여 검색 하려는 특정 사서함 또는 사이트 폴더의 폴더 ID 또는 경로를 가져옵니다.
ms.openlocfilehash: 3d9a82926a08b3f7f1f245146e70d79617e7a413
ms.sourcegitcommit: 6c9340e4eb221bf81472ff3f1ae25ae21aaf5297
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/11/2019
ms.locfileid: "31813999"
---
# <a name="use-content-search-in-office-365-for-targeted-collections"></a>대상 모음에 Office 365의 콘텐츠 검색 사용

Office 365 보안 &amp; 준수 센터의 콘텐츠 검색 기능은 Exchange 사서함 이나 SharePoint 및 비즈니스용 OneDrive 사이트의 특정 폴더를 검색 하는 UI에서 직접 방법을 제공 하지 않습니다. 그러나 실제 검색 쿼리 구문의 사이트에 대 한 전자 메일 또는 경로 (documentlink) 속성을 지정 하 여 특정 폴더 (대상 지정 된 *컬렉션*이라고 함)를 검색할 수 있습니다. 콘텐츠 검색을 사용 하 여 대상 모음을 수행 하는 것은 특정 사서함 이나 사이트 폴더에 있는 항목에 대 한 응답 항목이 있는 경우에 유용 합니다. 이 문서의 스크립트를 사용 하 여 SharePoint 및 비즈니스용 OneDrive 사이트의 폴더 ID 또는 사서함 폴더에 대 한 경로 (documentlink)를 가져올 수 있습니다. 그런 다음 검색 쿼리의 폴더 ID 또는 경로를 사용 하 여 폴더에 있는 항목을 반환할 수 있습니다.

> [!NOTE]
> SharePoint 또는 비즈니스용 OneDrive 사이트의 폴더에 있는 콘텐츠를 반환 하려면이 항목의 스크립트에서 Path 속성 대신 documentlink 관리 속성을 사용 합니다. documentlink 속성은 폴더의 모든 콘텐츠를 반환 하지만 path 속성은 일부 미디어 파일을 반환 하지 않기 때문에 경로 속성 보다 더 강력 합니다.

## <a name="before-you-begin"></a>시작하기 전에

- 1 단계에서 스크립트를 실행 하려면 보안 &amp; 및 준수 센터에서 eDiscovery 관리자 역할 그룹의 구성원 이어야 합니다. 자세한 내용은 [eDiscovery 사용 권한 할당](assign-ediscovery-permissions.md)을 참조 하십시오.
    
    또한 Exchange Online 조직에서 Mail Recipients 역할을 할당 받아야 합니다. 이는 1 단계의 스크립트에 포함 된 **get-mailboxfolderstatistics** cmdlet을 실행 하는 데 필요 합니다. 기본적으로 메일 받는 사람 역할은 Exchange Online의 조직 관리 및 받는 사람 관리 역할 그룹에 할당 됩니다. Exchange Online에서 사용 권한을 할당 하는 방법에 대 한 자세한 내용은 [Manage role group members](https://go.microsoft.com/fwlink/p/?linkid=692102)를 참조 하십시오. 사용자 지정 역할 그룹을 만들고 메일 받는 사람 역할을 할당 한 다음 1 단계에서 스크립트를 실행 해야 하는 구성원을 추가할 수도 있습니다. 자세한 내용은 [역할 그룹 관리](https://go.microsoft.com/fwlink/p/?linkid=730688) 항목을 참조하십시오.
    
- 1 단계에서 스크립트를 실행할 때마다 새 원격 PowerShell 세션이 만들어집니다. 따라서 사용할 수 있는 모든 원격 PowerShell 세션을 사용할 수 있습니다. 이러한 상황이 발생 하지 않도록 하려면 다음 명령을 실행 하 여 활성 원격 PowerShell 세션의 연결을 끊으십시오.
    
  ```
  Get-PSSession | Remove-PSSession
  ```

    자세한 내용은 [원격 PowerShell을 사용하여 Exchange Online에 연결](https://go.microsoft.com/fwlink/p/?linkid=396554)을 참조하세요.
    
- 스크립트에 최소 오류 처리가 포함 되어 있습니다. 이 스크립트의 기본 목적은 콘텐츠 검색의 검색 쿼리 구문에서 대상 모음을 수행 하는 데 사용할 수 있는 사서함 폴더 id 또는 사이트 경로 목록을 빠르게 표시 하는 것입니다.
    
- 이 항목에서 제공 하는 예제 스크립트는 Microsoft standard 지원 프로그램 또는 서비스에서 지원 되지 않습니다. 예제 스크립트는 어떤 종류의 보증도 없이 있는 그대로 제공 됩니다. Microsoft는 상품성 또는 특정 목적에 대 한 적합성에 대 한 묵시적 보증을 제한 없이 포함 하 여 모든 묵시적 보증을 배제 합니다. 샘플 스크립트 및 설명서의 사용 또는 성능으로 인해 발생 하는 전체 위험은 사용자에 게 남아 있습니다. Microsoft, 작성자 또는 스크립트를 작성, 프로덕션 또는 전달 하는 것과 관련 된 다른 모든 손해에 대 한 책임 (예를 들어, 비즈니스 이익 손실에 대 한 손해, 비즈니스 중단 Microsoft에서 이러한 손해에 대 한 권고를 받은 경우에도 예제 스크립트나 설명서를 사용 하거나 사용 하지 못하는 등의 비즈니스 정보 또는 기타 pecuniary 손실입니다.
  
## <a name="step-1-run-the-script-to-get-a-list-of-folders-for-a-mailbox-or-site"></a>1 단계: 스크립트를 실행 하 여 사서함 또는 사이트의 폴더 목록 가져오기

이 첫 단계에서 실행 하는 스크립트는 사서함 폴더 또는 SharePoint 및 비즈니스용 OneDrive 폴더 목록과 각 폴더의 해당 하는 폴더 ID 또는 경로를 반환 합니다. 이 스크립트를 실행 하면 다음 정보를 입력 하 라는 메시지가 표시 됩니다.
  
- **전자 메일 주소 또는 사이트 URL** Exchange 사서함 폴더 및 폴더 id 목록을 반환할 custodian의 전자 메일 주소를 입력 합니다. 또는 SharePoint 사이트의 URL 또는 비즈니스용 OneDrive 사이트를 입력 하 여 지정 된 사이트에 대 한 경로 목록을 반환 합니다. 그 예는 다음과 같습니다. 
    
  - **Exchange** -stacig@contoso.onmicrosoft.com 
    
  - **SharePoint** - https://contoso.sharepoint.com/sites/marketing 
    
  - **비즈니스용 OneDrive** - https://contoso-my.sharepoint.com/personal/stacig_contoso_onmicrosoft_com 
    
- **사용자 자격 증명** -스크립트는 자격 증명을 사용 하 여 Exchange Online 및 원격 PowerShell을 통해 보안 & 준수 센터에 연결 합니다. 앞에서 설명한 것 처럼이 스크립트를 성공적으로 실행 하려면 적절 한 사용 권한을 할당 받아야 합니다.
    
사서함 폴더 또는 사이트 documentlink (경로) 이름 목록을 표시 하려면 다음을 수행 합니다.
  
1. 파일 이름 접미사. p s 1을 사용 하 여 Windows PowerShell 스크립트 파일에 다음 텍스트를 저장 합니다. 예를 `GetFolderSearchParameters.ps1`들면입니다.
    
  ```
  #########################################################################################################
  # This PowerShell script will prompt you for:                             #
  #    * Admin credentials for a user who can run the Get-MailboxFolderStatistics cmdlet in Exchange    #
  #      Online and who is an eDiscovery Manager in the Security & Compliance Center.           #
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
  # Authenticate with Exchange Online and the Security & Compliance Center (Exchange Online Protection - EOP)
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
      # Authenticate with the Security & Compliance Center
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

2. 로컬 컴퓨터에서 Windows PowerShell을 열고 스크립트를 저장 한 폴더로 이동 합니다.
    
3. 스크립트를 실행 합니다. 예를 들어:
    
      ```
      .\GetFolderSearchParameters.ps1
      ```

4. 스크립트에서 묻는 메시지가 표시 되는 정보를 입력 합니다.
    
    이 스크립트는 지정 된 사용자에 대 한 사서함 폴더 또는 사이트 폴더의 목록을 표시 합니다. 폴더 ID 또는 documentlink 링크 이름을 복사 하 여 2 단계의 검색 쿼리에 붙여 넣을 수 있도록이 창을 열어 놓습니다.
    
    > [!TIP]
    > 컴퓨터 화면에 폴더 목록을 표시 하는 대신 스크립트의 출력을 텍스트 파일로 다시 보낼 수 있습니다. 이 파일은 스크립트가 있는 폴더에 저장 됩니다. 예를 들어 스크립트 출력을 텍스트 파일로 리디렉션하려면 3 단계: `.\GetFolderSearchParameters.ps1 > StacigFolderIds.txt` 에서 다음 명령을 실행 하 고 검색 쿼리에서 사용할 폴더 ID 또는 documentlink를 파일에서 복사 하면 됩니다.
  
### <a name="script-output-for-mailbox-folders"></a>사서함 폴더에 대 한 스크립트 출력

사서함 폴더 id를 가져오는 경우 스크립트는 원격 PowerShell을 사용 하 여 Exchange Online에 연결 하 고 **MailboxFolderStatisics** cmdlet을 실행 한 다음 지정 된 사서함의 폴더 목록을 표시 합니다. 사서함의 모든 폴더에 대해 스크립트는 **FolderPath** 열에 폴더 이름을 표시 하 고 **folderquery** 열에는 폴더 ID를 나타냅니다. 또한이 스크립트는 사서함 속성의 이름인 **folderId** 접두사를 폴더 ID에 추가 합니다. **folderid** 속성은 검색 가능한 속성 이므로 2 단계의 검색 쿼리를 `folderid:<folderid>` 사용 하 여 해당 폴더를 검색 합니다. 

> [!IMPORTANT]
> 이 문서의 스크립트에는 **get-mailboxfolderstatistics** 에서 반환 하는 64 문자 폴더 Id 값을 검색을 위해 인덱싱되는 동일한 48 문자로 변환 하는 인코딩 논리가 포함 되어 있습니다. 이 문서의 스크립트를 실행 하는 대신 PowerShell에서 **get-mailboxfolderstatistics** cmdlet을 실행 하 여 폴더 id를 가져오는 경우 해당 폴더 id 값을 사용 하는 검색 쿼리가 실패 합니다. 콘텐츠 검색에 사용할 수 있는 올바르게 포맷 된 폴더 id를 가져오려면 스크립트를 실행 해야 합니다.
  
다음은 사서함 폴더에 대 한 스크립트에서 반환 하는 출력의 예입니다.
  
![스크립트에서 반환 된 사서함 폴더 및 폴더 id 목록의 예](media/cd739207-eb84-4ebf-a03d-703f3d3a797d.png)
  
2 단계의 예제에서는 사용자의 복구 가능한 항목 폴더에서 제거 하위 폴더를 검색 하는 데 사용 되는 쿼리를 보여 줍니다.
  
### <a name="script-output-for-site-folders"></a>사이트 폴더의 스크립트 출력

SharePoint 또는 비즈니스용 OneDrive 사이트에서 **documentlink** 속성의 경로를 가져오는 경우 스크립트는 원격 PowerShell을 사용 하 여 보안 & 준수 센터에 연결 하 고 사이트에서 폴더를 검색 하는 새 콘텐츠 검색을 만듭니다. 지정한 다음 지정 된 사이트에 있는 폴더의 목록을 표시 합니다. 스크립트는 각 폴더의 이름을 표시 하 고 폴더 URL에 **documentlink** 의 접두사를 추가 합니다. **documentlink** 속성은 검색 가능한 속성 이므로 2 단계의 검색 쿼리에서 property `documentlink:<path>` : value 쌍을 사용 하 여 해당 폴더를 검색 합니다. 
  
다음은 사이트 폴더 스크립트에서 반환 하는 출력의 예입니다.
  
![스크립트에서 반환 하는 사이트 폴더의 documentlink 이름 목록 예제](media/519e8347-7365-4067-af78-96c465dc3d15.png)
  
## <a name="step-2-use-a-folder-id-or-documentlink-to-perform-a-targeted-collection"></a>2 단계: 폴더 ID 또는 documentlink를 사용 하 여 대상 모음을 수행 합니다.

스크립트를 실행 하 여 특정 사용자에 대 한 폴더 id 또는 documentlinks의 목록을 수집한 후에는 다음 단계를 수행 하 여 Security & 준수 센터로 이동한 다음 새 콘텐츠 검색을 만들어 특정 폴더를 검색 합니다. 콘텐츠 검색 키워드 상자 `folderid:<folderid>` 에서 `documentlink:<path>` 구성 하는 검색 쿼리에 값 쌍을 사용 하거나, **ComplianceSearch** cmdlet을 사용 하는 경우 *contentmatchquery* 매개 변수의 값으로 사용할 수 있습니다. `folderid` 또는 `documentlink` 속성을 다른 검색 매개 변수 또는 검색 조건과 결합할 수 있습니다. 쿼리에 `folderid` 또는 `documentlink` 속성만 포함 하면 지정한 폴더에 있는 모든 항목이 검색에 반환 됩니다. 
  
1. [https://protection.office.com](https://protection.office.com)으로 이동합니다.
    
2. 1 단계에서 스크립트를 실행 하는 데 사용한 계정 및 자격 증명을 사용 하 여 Office 365에 로그인 합니다.
    
3. 보안 & 준수 센터의 왼쪽 창에서 **콘텐츠 검색** **검색** \> 을 클릭 하 고 **새** ![추가 아이콘](media/O365-MDM-CreatePolicy-AddIcon.gif)을 클릭 합니다.
    
4. **새 검색** 페이지에서 콘텐츠 검색의 이름을 입력합니다. 이 이름은 조직 내에서 고유해야 합니다. 
    
5. 검색 여부에 따라 다음 중 하나를 수행 하 여 사서함 폴더를 검색할지, 사이트 폴더를 **찾습니다**.
    
    - **검색 하려는 특정 사서함 선택을** 클릭 한 다음 1 단계에서 스크립트를 실행할 때 지정한 것과 동일한 사서함을 추가 합니다. 
    
      또는
    
    - 검색 하려면 **특정 사이트 선택을** 클릭 한 다음 1 단계에서 스크립트를 실행할 때 지정한 것과 동일한 사이트 URL을 추가 합니다. 
    
6. **다음**을 클릭합니다.
    
7. 확인할 **작업** 페이지의 키워드 상자에서 1 단계에서 스크립트에 의해 반환 된 `folderid:<folderid>` `documentlink:<path>` 값을 붙여 넣습니다. 
    
    예를 들어 다음 스크린샷의 쿼리는 사용자의 복구할 수 있는 항목 폴더에 있는 제거 하위 폴더의 모든 항목을 검색 합니다 (제거 하위 폴더 `folderid` 의 속성 값은 1 단계의 스크린샷에 표시 됨).
    
    ![검색 쿼리의 키워드 상자에 folderid 또는 documentlink를 붙여 넣습니다.](media/84057516-b663-48a4-a78f-8032a8f8da80.png)
  
8. **검색** 을 클릭 하 여 대상 지정 된 모음 검색을 시작 합니다. 
  
### <a name="examples-of-search-queries-for-targeted-collections"></a>대상 지정 컬렉션에 대 한 검색 쿼리 예제

다음은 검색 쿼리의 `folderid` 및 `documentlink` 속성을 사용 하 여 대상 모음을 수행 하는 방법의 몇 가지 예입니다. 자리 표시자는 `folderid:<folderid>` 및 `documentlink:<path>` 공간을 절약 하는 데 사용 됩니다. 
  
- 이 예에서는 서로 다른 세 개의 사서함 폴더를 검색 합니다. 비슷한 쿼리 구문을 사용 하 여 사용자의 복구 가능한 항목 폴더에서 숨겨진 폴더를 검색할 수 있습니다.
    
  ```
  folderid:<folderid> OR folderid:<folderid> OR folderid:<folderid>
  ```

- 이 예에서는 사서함 폴더에서 정확한 구가 포함 된 항목을 검색 합니다.
    
  ```
  folderid:<folderid> AND "Contoso financial results"
  ```

- 이 예에서는 제목에 "NDA" 문자가 포함 된 문서의 사이트 폴더와 하위 폴더를 검색 합니다.
    
  ```
  documentlink:<path> AND filename:nda
  ```

- 다음은 날짜 범위 내에서 변경 된 문서의 사이트 폴더와 하위 폴더를 검색 하는 예제입니다.
    
  ```
  documentlink:<path> AND (lastmodifiedtime>=01/01/2017 AND lastmodifiedtime<=01/21/2017)
  ```
  
## <a name="more-information"></a>추가 정보

이 문서의 스크립트를 사용 하 여 대상 모음을 수행할 때는 다음 사항을 염두에 두어야 합니다.
  
- 스크립트는 결과에서 폴더를 제거 하지 않습니다. 따라서 결과에 나열 된 일부 폴더에는 시스템 생성 콘텐츠가 포함 되어 있기 때문에 검색 되지 않거나 0 개 항목이 반환 될 수 있습니다.
    
- 이 스크립트는 사용자의 기본 사서함에 대 한 폴더 정보만 반환 합니다. 사용자의 보관 사서함에 있는 폴더에 대 한 정보는 반환 되지 않습니다.
    
- 사서함 폴더를 검색할 때 지정 된 폴더 (해당 `folderid` 속성으로 식별 됨)만 검색 됩니다. 하위 폴더는 검색 되지 않습니다. 하위 폴더를 검색 하려면 검색 하려는 하위 폴더에 대 한 폴더 ID를 사용 해야 합니다. 
    
- 사이트 폴더를 검색 하면 해당 `documentlink` 속성으로 식별 된 폴더와 모든 하위 폴더가 검색 됩니다. 
    
- 검색 쿼리의 `folderid` 속성만 지정 하는 검색 결과를 내보낼 때 첫 번째 내보내기 옵션인 "모든 항목 (인식할 수 없는 형식을 포함 하거나 암호화 됨 또는 다른 이유로 인덱싱되지 않은 것은 제외)을 선택할 수 있습니다. 폴더 ID는 항상 인덱싱되어 있기 때문에 폴더의 모든 항목은 인덱싱 상태에 관계 없이 항상 내보내집니다.
