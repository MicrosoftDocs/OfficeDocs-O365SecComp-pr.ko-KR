---
title: 콘텐츠 검색을 사용하여 사용자 목록에 대 한 사서함 및 비즈니스용 OneDrive 검색
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 1/3/2017
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: 5f4f8206-2d6a-4cb2-bbc6-7a0698703cc0
description: 이 문서에 콘텐츠 검색 및 스크립트를 사용 하 여 사용자 그룹에 대 한 비즈니스 사이트에 대 한 사서함과 OneDrive를 검색 합니다.
ms.openlocfilehash: cc88f8e81a9883b8d392965db14994691878748d
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22533355"
---
# <a name="use-content-search-to-search-the-mailbox-and-onedrive-for-business-site-for-a-list-of-users"></a>콘텐츠 검색을 사용하여 사용자 목록에 대 한 사서함 및 비즈니스용 OneDrive 검색

Office 365 보안 &amp; 준수 센터 시간이 오래 걸리는 eDiscovery 관련 작업을 자동화할 수 있도록 하는 Windows PowerShell cmdlet의 번호를 제공 합니다. 현재 보안에서 콘텐츠 검색을 만드는 &amp; 많은 더불어 콘텐츠 위치를 검색 하려면 준수 센터 소요 시간과 준비 합니다. 검색을 만들기 전에 비즈니스 사이트에 대 한 각 OneDrive에 대 한 URL을 수집 하 고 다음 검색 각 사서함 및 비즈니스 사이트에 대 한 O neDrive를 추가 해야 합니다. 향후 릴리스에서,이 속성은 쉽게 보안에서 작업을 수행할 수 &amp; 준수 센터입니다. 그 때까지이 프로세스를 자동화 하려면이 문서에서 스크립트를 사용할 수 있습니다. 이 스크립트 조직의 내 사이트 도메인의 이름에 대 한 묻는 메시지를 표시 합니다 (예: **contoso** URL에서 https://contoso-my.sharepoint.com), 주소는 사용자 전자 메일의 목록, 새로운 콘텐츠 검색 및 검색 쿼리 사용 하 여의 이름입니다. 스크립트는 OneDrive 비즈니스 URL에 대 한 목록에서 각 사용자에 대 한를 가져오고 만듭니다 하 고 목록에서 제공 하는 검색 쿼리를 사용 하 여 각 사용자에 대 한 비즈니스 사이트에 대 한 사서함을 검색 하는 콘텐츠 검색 및 OneDrive를 시작 합니다. 
  
## <a name="before-you-begin"></a>시작하기 전에

- 보안에서 eDiscovery 관리자 역할 그룹의 구성원 이어야 하는 &amp; 준수 센터 및 3 단계에서에서 스크립트를 실행 하려면 SharePoint Online 전역 관리자입니다.
    
- 2 단계와 3 단계에서에서 동일한 폴더에 스크립트에서 만든 사용자의 목록에 저장 해야 합니다. 하는 간편 하 게 스크립트를 실행 합니다.
    
- 이 스크립트는 최소한의 오류 처리를 포함합니다. 주요 목적은 빠르고 쉽게 검색 각 사용자의 비즈니스 사이트에 대 한 사서함 및 OneDrive입니다.
    
- 이 항목에서 제공 하는 샘플 스크립트는 Microsoft 표준 지원 프로그램이 나 서비스에서 지원 되지 않습니다. 샘플 스크립트는 어떠한 보증도 없이 있는 그대로 제공 됩니다. 또한 Microsoft 모든 보증을 부인 i[https://go.microsoft.com/fwlink/p/?LinkId=517283](https://go.microsoft.com/fwlink/p/?LinkId=517283)mplied 보증을 포함 하 되이 제한 되지 않음 모든 묵시적 보증 상품성 또는 특정 목적에의 적합성의 합니다. 사용 또는 성능 샘플 스크립트 및 설명서에 발생 하는 위험은 있습니다. 어떠한 이벤트에 Microsoft, 해당 작성자 또는 다른 만들기, 제작, 또는 스크립트의 배달에 참여 하는 모든 책임을 지지 모든 손해에 대해 (포함 하 되, 제한 되지 않고 비즈니스 이익, 영업 중단, 손실 손실에 대 한 손해 비즈니스 정보 또는 기타 금전적 손실을) Microsoft가 그와 같은 손해의 가능성을 사전에 알고 있었던 경우에 사용 또는 설명서를 확인 하는 샘플 스크립트를 사용 하 여 원인으로 발생 합니다.
    
## <a name="step-1-install-the-sharepoint-online-management-shell"></a>1단계: SharePoint Online 관리 셸 설치
<a name="step1"> </a>

첫 단계 SharePoint Online 관리 셸을 설치 하는 것입니다. 셸을 사용 하 여이 절차에서는 필요는 없지만 필수 구성 요소가 3 단계에서에서 실행 하는 스크립트에 필요한 포함 하기 때문에 설치 해야 합니다. 이러한 필수 구성이 요소는 비즈니스 사이트에 대 한 OneDrive에 대 한 Url을 가져올 SharePoint Online과 통신 하는 스크립트를 허용 합니다.
  
[SharePoint Online 관리 셸 Windows PowerShell 환경 설정](https://go.microsoft.com/fwlink/p/?LinkID=286318) 를 이동 하 고 SharePoint Online 관리 셸을 설치 하는 단계 1 및 2 단계를 수행 합니다.
  
## <a name="step-2-generate-a-list-of-users"></a>2 단계: 사용자의 목록 생성
<a name="step2"> </a>

3 단계에서에서 스크립트를 검색 사서함 및 사용자의 목록에 대 한 OneDrive 계정에 대 한 콘텐츠 검색을 만듭니다. 만 텍스트 파일에 대 한 전자 메일 주소를 입력 하거나 전자 메일 주소 목록을 가져오고 (3 단계에서에서 스크립트를를 저장할 수 있는 동일한 폴더에 있음) 파일에 저장 하는 Windows PowerShell에서 명령을 실행할 수 있습니다.
  
여기에 조직에서 모든 사용자에 대 한 전자 메일 주소 목록을 가져오고 라는 텍스트 파일에 저장 하는 아니다 수 있는 [Exchange Online PowerShell](https://go.microsoft.com/fwlink/p/?LinkId=517283) 명령 `Users.txt`합니다. 
  
```
Get-Mailbox -ResultSize unlimited -Filter { RecipientTypeDetails -eq 'UserMailbox'} | Select-Object PrimarySmtpAddress > Users.txt
```

이 명령을 실행 하면 파일을 열고 헤더 속성 이름을 포함 하 고 제거를 확인 해야 `PrimarySmtpAddress`합니다. 텍스트 파일의 전자 메일 주소 목록 및 다른 nothing에 포함 되어야 합니다. 빈 행이 없는 앞 또는 뒤에 전자 메일 주소 목록에 있는지 확인 합니다.
  
## <a name="step-3-run-the-script-to-create-and-start-the-search"></a>3 단계:를 만들고 검색을 시작 스크립트를 실행 합니다.

이 단계에서 스크립트를 실행 하는 경우 다음 정보에 대 한 묻는 됩니다 것입니다. 스크립트를 실행 하기 전에이 정보를 준비를 해야 합니다.
  
- **사용자 자격 증명** -스크립트를 사용 하 여 사용자의 자격 증명 SharePoint Online 비즈니스 Url에 대 한 OneDrive 가져올 및 보안에 연결할 액세스 &amp; 준수 센터 원격 PowerShell 사용 합니다. 
    
- **내 사이트 도메인의 이름** -내 사이트는 도메인은 조직에서 비즈니스 사이트에 대 한 모든 OneDrive를 포함 하는 도메인입니다. 예: 내 사이트 도메인에 대 한 URL이 경우 **https://contoso-my.sharepoint.com**을 입력 한 다음 `contoso` 때 스크립트를 묻는 MySite 도메인의 이름입니다. 
    
- **2 단계에서에서 텍스트 파일의 경로 이름** -2 단계에서에서 만든 텍스트 파일의 경로 이름입니다. 텍스트 파일 및 스크립트를 같은 폴더에 있는 경우에 텍스트 파일의 이름을 입력 합니다. 그렇지 않은 경우 텍스트 파일에 대 한 전체 경로 입력 합니다. 
    
- **콘텐츠 검색의 이름** -스크립트에 의해 생성 될 콘텐츠 검색의 이름입니다. 
    
- **검색 쿼리** -콘텐츠 검색 사용 되는 검색 쿼리 만들어져 실행 됩니다. 검색 쿼리 하는 방법에 대 한 자세한 내용은 [키워드 쿼리 및 콘텐츠 검색에 대 한 검색 조건을](keyword-queries-and-search-conditions.md)참조 하십시오.


**스크립트를 실행하려면**
    
1. .Ps1 파일 이름 접미사를 사용 하 여 Windows PowerShell 스크립트 파일에 다음 텍스트를 저장 예, `SearchEXOOD4B.ps1`합니다. 2 단계에서에서 사용자 목록의 저장 하는 동일한 폴더에 파일을 저장 합니다.
    
  ```
  # This PowerShell script will prompt you for the following information:
  #    * Your user credentials 
  #    * The name of your organization's MySite domain                                              
  #    * The pathname for the text file that contains a list of user email addresses
  #    * The name of the Content Search that will be created
  #    * The search query string
  # The script will then:
  #    * Find the OneDrive for Business site for each user in the text file
  #    * Create and start a Content Search using the above information
  # Get user credentials
  if (!$credentials)
  {
      $credentials = Get-Credential
  }
  # Get the user's MySite domain name.  We use this to create the admin URL and root URL for OneDrive for Business
  $mySiteDomain = Read-Host "What is your organization's MySite domain?  For example,  'contoso' for 'https://contoso-my.sharepoint.com'"
  $AdminUrl = "https://$mySiteDomain-admin.sharepoint.com"
  $mySiteUrlRoot = "https://$mySiteDomain-my.sharepoint.com"
  # Get other required information
  $inputfile = read-host "Enter the file name of the text file that contains the email addresses for the users you want to search"
  $searchName = Read-Host "Enter the name for the new search"
  $searchQuery = Read-Host "Enter the search query you want to use"
  $emailAddresses = Get-Content $inputfile | where {$_ -ne ""}  | foreach{ $_.Trim() }
  # Connect to Office 365
  if (!$s -or !$a)
  {
      $s = New-PSSession -ConfigurationName Microsoft.Exchange -ConnectionUri "https://ps.compliance.protection.outlook.com/powershell-liveid" -Credential $credentials -Authentication Basic -AllowRedirection -SessionOption (New-PSSessionOption -SkipCACheck -SkipCNCheck -SkipRevocationCheck)
      $a = Import-PSSession $s -AllowClobber
      if (!$s)
      {
          Write-Error "Could not create PowerShell session."
          return;
      }
  }
  # Load the SharePoint assemblies from the SharePoint Online Management Shell
  # To install, go to http://go.microsoft.com/fwlink/p/?LinkId=255251
  if (!$SharePointClient -or !$SPRuntime -or !$SPUserProfile)
  {
      $SharePointClient = [System.Reflection.Assembly]::LoadWithPartialName("Microsoft.SharePoint.Client")
      $SPRuntime = [System.Reflection.Assembly]::LoadWithPartialName("Microsoft.SharePoint.Client.Runtime")
      $SPUserProfile = [System.Reflection.Assembly]::LoadWithPartialName("Microsoft.SharePoint.Client.UserProfiles")
      if (!$SharePointClient)
      {
          Write-Error "SharePoint Online Management Shell isn't installed, please install from: http://go.microsoft.com/fwlink/p/?LinkId=255251 and then run this script again"
          return;
      }
  }
  if (!$spCreds)
  {
      $spCreds = New-Object Microsoft.SharePoint.Client.SharePointOnlineCredentials($credentials.UserName, $credentials.Password)
  }
  # Add the path of the User Profile Service to the SPO admin URL, then create a new webservice proxy to access it
  $proxyaddr = "$AdminUrl/_vti_bin/UserProfileService.asmx?wsdl"
  $UserProfileService= New-WebServiceProxy -Uri $proxyaddr -UseDefaultCredential False
  $UserProfileService.Credentials = $credentials
  # Take care of auth cookies
  $strAuthCookie = $spCreds.GetAuthenticationCookie($AdminUrl)
  $uri = New-Object System.Uri($AdminUrl)
  $container = New-Object System.Net.CookieContainer
  $container.SetCookies($uri, $strAuthCookie)
  $UserProfileService.CookieContainer = $container
  Write-Host "Getting each user's OneDrive for Business URL"
  $urls = @()
  foreach($emailAddress in $emailAddresses)
  {
      try
      {
          $prop = $UserProfileService.GetUserProfileByName("i:0#.f|membership|$emailAddress") | Where-Object { $_.Name -eq "PersonalSpace" } 
          $url = $prop.values[0].value
          $furl = $mySiteUrlRoot + $url
          $urls += $furl
          Write-Host "-$emailAddress => $furl"
      }
      catch
      {
          Write-Warning "Could not locate OneDrive for $emailAddress"
      }
  }
  Write-Host "Creating and starting the search"
  $search = New-ComplianceSearch -Name $searchName -ExchangeLocation $emailAddresses -SharePointLocation $urls -ContentMatchQuery $searchQuery
  # Finally, start the search and then display the status
  if($search)
  {
      Start-ComplianceSearch $search.Name
      Get-ComplianceSearch $search.Name
  }
  
  ```

2. Windows PowerShell을 열고 2 단계에서에서 스크립트와 사용자의 목록을 저장 되는 위치 폴더로 이동 합니다.
    
3. 시작 스크립트입니다. 예를 들어:
    
    ```
    .\SearchEXOOD4B.ps1
    ```

4. 사용자의 자격 증명에 대 한 대화 상자가 나타나면 전자 메일 주소와 암호를 입력 한 다음 **확인**을 클릭 합니다. 
    
5. 정보는 스크립트에 의해 대화 상자가 나타나면 다음을 입력 합니다. 각 부분의 정보를 입력 하 고 **Enter**키를 누릅니다.
    
    - 내 사이트 도메인의 이름입니다. 
    
    - 사용자의 목록을 포함 하는 텍스트 파일의 경로 이름입니다.
    
    - 콘텐츠 검색에 대 한 이름입니다.
    
    - 검색 쿼리 (비워가 콘텐츠 위치에 있는 모든 항목을 반환 하려면).
    
    스크립트는 비즈니스 사이트에 대 한 각 OneDrive에 대 한 Url을 가져옵니다 하 고 만들고 검색을 시작 합니다. 검색 통계와 결과 표시 하는 보안 및 규정 준수 센터 PowerShell에서 **Get ComplianceSearch** cmdlet을 실행 하거나 확인 하거나 보안에서 **콘텐츠 검색** 페이지로 이동할 수 &amp; 를 보기 위해 준수 센터 검색에 대 한 정보를 제공 합니다. 
