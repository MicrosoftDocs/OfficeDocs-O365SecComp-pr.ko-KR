---
title: Office 365 보안에서 eDiscovery 사례에 보류에 사용자를 추가 하는 스크립트를 사용 하 여 &amp; 준수 센터
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 1/23/2017
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MED150
- MBS150
- MET150
ms.assetid: bad352ff-d5d2-45d8-ac2a-6cb832f10e73
description: 신속 하 게 사서함을 추가 하는 스크립트를 실행 하 고 비즈니스용 Office 365 보안에서 eDiscovery 사례와 관련 된 새로운 보류에 사이트 &amp; 준수 센터입니다.
ms.openlocfilehash: eb53f01b4f1b7245e1411ac470db629115eb1ef5
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22533417"
---
# <a name="use-a-script-to-add-users-to-a-hold-in-an-ediscovery-case-in-the-office-365-security-amp-compliance-center"></a>Office 365 보안에서 eDiscovery 사례에 보류에 사용자를 추가 하는 스크립트를 사용 하 여 &amp; 준수 센터

Office 365 보안 &amp; 준수 센터에서 제공 하는 많은 수 있도록 하는 Windows PowerShell cmdlet 만들기 (영문) 및 eDiscovery 사례 관리와 관련 된 하는 시간이 오래 걸리는 작업을 자동화 합니다. 현재, eDiscovery 사례 도구를 사용 하 여 보안에서 &amp; 많은 더불어 콘텐츠 위치를 대기 시키려면 준수 센터 소요 시간과 준비 합니다. 예, 보류를 만들기 전에를 대기 시키려면 원하는 비즈니스 사이트에 대 한 각 OneDrive에 대 한 URL을 수집 해야 합니다. 다음을 보류 하려는 각 사용자에 대해 해야 자신의 사서함 및 해당 OneDrive 비즈니스 사이트에 대 한 보류에 추가 합니다. 보안의 향후 릴리스에서 &amp; 준수 센터가를 편리 하 게 작업을 수행 하기 위해. 그 때까지이 프로세스를 자동화 하려면이 문서에서 스크립트를 사용할 수 있습니다.
  
스크립트 조직의 내 사이트 도메인의 이름에 대 한 묻는 메시지를 표시 합니다 (예: **contoso** URL에서 https://contoso-my.sharepoint.com), 대/소문자와 연결 하는 기존 eDiscovery 사례의 이름, 새 보류의 이름을, 원하는 사용자의 전자 메일 주소 목록 보류 및 쿼리 기반 보존을 만들려고 할 경우를 사용 하 여 검색 쿼리에 배치 합니다. 스크립트 다음 목록에서 각 사용자에 대 한 비즈니스 사이트에 대 한 OneDrive에 대 한 URL을 가져옵니다 새 보류를 만들고을 추가 하는 사서함 및 OneDrive 목록에서 각 사용자에 대 한 비즈니스 사이트에 대 한 보류 합니다. 이 스크립트는 또한 새 대기 하는 방법에 대 한 정보가 들어 있는 로그 파일을 생성 합니다. 
  
이렇게 하는 단계는 다음과 같습니다.
  
[1단계: SharePoint Online 관리 셸 설치](use-a-script-to-add-users-to-a-hold-in-ediscovery.md#step1)
  
[2 단계: 사용자의 목록 생성](use-a-script-to-add-users-to-a-hold-in-ediscovery.md#step2)
  
[보류를 만들고 사용자를 추가 하는 스크립트를 실행 하는 3 단계:](use-a-script-to-add-users-to-a-hold-in-ediscovery.md#step3)
  
## <a name="before-you-begin"></a>시작하기 전에

- 보안에서 eDiscovery 관리자 역할 그룹의 구성원 이어야 하는 &amp; 준수 센터 및 3 단계에서에서 스크립트를 실행 하려면 SharePoint Online 전역 관리자입니다. 자세한 내용은 참조 [Office 365 보안에서 eDiscovery 사용 권한을 할당 &amp; 준수 센터](assign-ediscovery-permissions.md)합니다.
    
- 보안에서 eDiscovery 사례와 관련 된 보류에 추가할 수 최대 1000 개의 사서함과 사이트 수가 100 &amp; 준수 센터입니다. 보류에 배치 하려는 모든 사용자가 비즈니스 사이트에 대 한 OneDrive, 이라고 가정할이 문서에서 스크립트를 사용 하 여 보류에 최대 100 명의 사용자를 추가할 수 있습니다. 
    
- 2 단계와 3 단계에서에서 동일한 폴더에 스크립트에서 만든 사용자의 목록에 저장 해야 합니다. 하는 간편 하 게 스크립트를 실행 합니다.
    
- 사용자의 목록 기존 사례와 연결 된 새 보류에 추가 하는 스크립트입니다. 스크립트를 실행 하기 전에 함께 보류에 연결 하려는 경우 만들어지는 확인 해야 합니다.
    
- 이 스크립트는 최소한의 오류 처리를 포함합니다. 서비스의 주요 목적은 시키려면 빠르고 쉽게 사서함 이며 비즈니스 사이트에 대 한 각 사용자의 비즈니스용 OneDrive 유지 합니다.
    
- 이 항목에서 제공 하는 샘플 스크립트는 Microsoft 표준 지원 프로그램이 나 서비스에서 지원 되지 않습니다. 샘플 스크립트는 어떠한 보증도 없이 있는 그대로 제공 됩니다. Microsoft 추가로 포함 하 여, 제한 되지 않고 하는 모든 묵시적된 보증을 부인 묵시적 보증 상품성 또는 특정 목적에의 적합성입니다. 사용 또는 성능 샘플 스크립트 및 설명서에 발생 하는 위험은 있습니다. 어떠한 이벤트에 Microsoft, 해당 작성자 또는 다른 만들기, 제작, 또는 스크립트의 배달에 참여 하는 모든 책임을 지지 모든 손해에 대해 (포함 하 되, 제한 되지 않고 비즈니스 이익, 영업 중단, 손실 손실에 대 한 손해 비즈니스 정보 또는 기타 금전적 손실을) Microsoft가 그와 같은 손해의 가능성을 사전에 알고 있었던 경우에 사용 또는 설명서를 확인 하는 샘플 스크립트를 사용 하 여 원인으로 발생 합니다.

## <a name="step-1-install-the-sharepoint-online-management-shell"></a>1단계: SharePoint Online 관리 셸 설치

첫번째 단계에서는 로컬 컴퓨터에 설치 된 하지 않은 경우 SharePoint Online 관리 셸을 설치 하는 것입니다. 셸을 사용 하 여이 절차에서는 필요는 없지만 필수 구성 요소가 3 단계에서에서 실행 하는 스크립트에 필요한 포함 하기 때문에 설치 해야 합니다. 이러한 필수 구성이 요소는 비즈니스 사이트에 대 한 OneDrive에 대 한 Url을 가져올 SharePoint Online과 통신 하는 스크립트를 허용 합니다.
  
[SharePoint Online 관리 셸 Windows PowerShell 환경 설정](https://go.microsoft.com/fwlink/p/?LinkID=286318) 를 이동 하 고 로컬 컴퓨터에 SharePoint Online 관리 셸을 설치 하려면 1 단계 및 2 단계를 수행 합니다. 

## <a name="step-2-generate-a-list-of-users"></a>2 단계: 사용자의 목록 생성
<a name="step2"> </a>

3 단계에서에서 스크립트와 관련 된 추가 및 eDiscovery 사례, 사서함 및 OneDrive 보류에 대 한 사용자 목록의 비즈니스 사이트에 대 한 보류를 만들어집니다. 만 텍스트 파일에 대 한 전자 메일 주소를 입력 하거나 전자 메일 주소 목록을 가져오고 (3 단계에서에서 스크립트를를 저장할 수 있는 동일한 폴더에 있음) 파일에 저장 하는 Windows PowerShell에서 명령을 실행할 수 있습니다.
  
다음 PowerShell 명령을 (실행 하는 Exchange Online 조직에 연결 된 원격 PowerShell을 사용 하 여)은 조직에서 모든 사용자에 대 한 전자 메일 주소 목록을 가져오고 텍스트 파일에 저장 하 라는 HoldUsers.txt 합니다.
  
```
Get-Mailbox -ResultSize unlimited -Filter { RecipientTypeDetails -eq 'UserMailbox'} | Select-Object PrimarySmtpAddress > HoldUsers.txt
```

이 명령을 실행 하 고 텍스트 파일을 열 속성 이름을 포함 하는 헤더 제거 후 `PrimarySmtpAddress`합니다. 3 단계에서에서 만들 수 있는 보류에 추가 하려는 사용자에 대 한 확인란을 제외한 모든 전자 메일 주소를 제거 합니다. 빈 행이 없는 앞 또는 뒤에 전자 메일 주소 목록에 있는지 확인 합니다.
  

  
## <a name="step-3-run-the-script-to-create-a-hold-and-add-users"></a>보류를 만들고 사용자를 추가 하는 스크립트를 실행 하는 3 단계:
<a name="step3"> </a>

이 단계에서 스크립트를 실행 하는 경우 다음 정보에 대 한 묻는 됩니다 것입니다. 스크립트를 실행 하기 전에이 정보를 준비를 해야 합니다.
  
- **사용자 자격 증명** -스크립트 자격 증명을 사용 하 여 보안에 연결할 &amp; 준수 센터 원격 PowerShell 사용 합니다. 또한 이러한 자격 증명 SharePoint 온라인 OneDrive 비즈니스 Url에 대 한 사용자의 목록에 대 한 액세스를 사용 합니다.
    
- **내 사이트 도메인의 이름** -내 사이트는 도메인은 조직에서 비즈니스 사이트에 대 한 모든 OneDrive를 포함 하는 도메인입니다. 예: 내 사이트 도메인에 대 한 URL이 경우 **https://contoso-my.sharepoint.com**을 입력 한 다음 `contoso` 때 스크립트를 묻는 MySite 도메인의 이름입니다. 
    
- **대/소문자의 이름** -기존 사례의 이름입니다. 이 스크립트에서는이 경우와 연결 된 새 보류를 만듭니다.
    
- **보류의 이름** 을-스크립트 보류의 이름을 만들고 지정된 된 사례와 연결 됩니다.
    
- **쿼리 기반에 대 한 검색 쿼리 대기** -지정 된 검색 조건에 맞는 콘텐츠만 대기 상태에 놓일 수 있도록 쿼리 기반 보존을 만들 수 있습니다. **모든 콘텐츠를 대기 시키려면 그냥 enter 키를 검색 쿼리에 대 한 메시지가 나타나면 합니다.** 
    
- **보류를 설정 하 여부** -만들어질 또는 것을 사용 하지 않고 보류를 만드는 스크립트를 포함할 수 후 보류를 설정 하는 스크립트를 가질 수 있습니다. 보류를 설정 하는 스크립트를 설치 하지 않은 경우 수 설정 하는 보안 뒷부분에 나오는 &amp; 준수 센터 또는 다음 PowerShell 명령을 실행 하 여: 
    
  ```
  Set-CaseHoldPolicy -Identity <name of the hold> -Enabled $true
  ```

  ```
  Set-CaseHoldRule -Identity <name of the hold> -Disabled $false
  ```

- **사용자의 목록을 사용 하 여 텍스트 파일의 이름** -보류에 추가할 사용자의 목록을 포함 하는 2 단계에서에서 텍스트 파일의 이름입니다. 이 파일, 스크립트와 같은 폴더에 있는 경우 (예: HoldUsers.txt) 파일의 이름을 입력 합니다. 텍스트 파일을 다른 폴더에 복사한 경우에 파일의 전체 경로 이름을 입력 합니다.
    
스크립트를 묻는 메시지에 대 한 정보를 수집한 했을 때 후 마지막 단계는 새 보류를 만들고 사용자를 추가 하는 스크립트를 실행 합니다.
  
1. .Ps1 파일 이름 접미사를 사용 하 여 Windows PowerShell 스크립트 파일에 다음 텍스트를 저장 예, `AddUsersToHold.ps1`합니다.
    
  ```
  #script begin
  " " 
  write-host "***********************************************"
  write-host "   Office 365 Security &amp; Compliance Center   " -foregroundColor yellow -backgroundcolor darkgreen
  write-host "   eDiscovery cases - Add users to a hold   " -foregroundColor yellow -backgroundcolor darkgreen 
  write-host "***********************************************"
  " " 
  # Get user credentials &amp; Connect to Office 365 SCC, SPO
  $credentials = Get-Credential -Message "Specify your credentials to connect to the Office 365 Security &amp; Compliance Center and SharePoint Online"
  $s = New-PSSession -ConfigurationName Microsoft.Exchange -ConnectionUri "https://ps.compliance.protection.outlook.com/powershell-liveid" -Credential $credentials -Authentication Basic -AllowRedirection -SessionOption (New-PSSessionOption -SkipCACheck -SkipCNCheck -SkipRevocationCheck)
  $a = Import-PSSession $s -AllowClobber
      if (!$s)
      {
          Write-Error "Couldn't create PowerShell session."
          return;
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
          Write-Error "The SharePoint Online Management Shell isn't installed. Please install it from: http://go.microsoft.com/fwlink/p/?LinkId=255251 and then re-run this script."
          return;
      }
  }
  if (!$spCreds)
  {
      $spCreds = New-Object Microsoft.SharePoint.Client.SharePointOnlineCredentials($credentials.UserName, $credentials.Password)
  }
  # Get the user's MySite domain name. We use this to create the admin URL and root URL for OneDrive for Business
  ""
  $mySiteDomain = Read-Host "Enter the name of your organization's MySite domain. For example, 'contoso' for 'https://contoso-my.sharepoint.com'"
  ""
  # Get other required information
  do{
  $casename = Read-Host "Enter the name of the case"
  $caseexists = (get-compliancecase -identity "$casename" -erroraction SilentlyContinue).isvalid
  if($caseexists -ne 'True')
  {""
  write-host "A case named '$casename' doesn't exist. Please specify the name of an existing case, or create a new case and then re-run the script." -foregroundColor Yellow
  ""}
  }While($caseexists -ne 'True')
  ""
  do{
  $holdName = Read-Host "Enter the name of the new hold"
  $holdexists=(get-caseholdpolicy -identity "$holdname" -case "$casename" -erroraction SilentlyContinue).isvalid
  if($holdexists -eq 'True')
  {""
  write-host "A hold named '$holdname' already exists. Please specify a new hold name." -foregroundColor Yellow
  ""}
  }While($holdexists -eq 'True')
  ""
  $holdQuery = Read-Host "Enter a search query to create a query-based hold, or press Enter to hold all content"
  ""
  $holdstatus = read-host "Do you want the hold enabled after it's created? (Yes/No)"
  do{
  ""
  $inputfile = read-host "Enter the name of the text file that contains the email addresses of the users to add to the hold"
  ""
  $fileexists = test-path -path $inputfile
  if($fileexists -ne 'True'){write-host "$inputfile doesn't exist. Please enter a valid file name." -foregroundcolor Yellow}
  }while($fileexists -ne 'True')
  #Import the list of addresses from the txt file.  Trim any excess spaces and make sure all addresses 
      #in the list are unique.
    [array]$emailAddresses = Get-Content $inputfile -ErrorAction SilentlyContinue | where {$_.trim() -ne ""}  | foreach{ $_.Trim() }
    [int]$dupl = $emailAddresses.count
    [array]$emailAddresses = $emailAddresses | select-object -unique
    $dupl -= $emailAddresses.count
  #Validate email addresses so the hold creation does not run in to an error.
  if($emailaddresses.count -gt 0){
  write-host ($emailAddresses).count "addresses were found in the text file. There were $dupl duplicate entries in the file." -foregroundColor Yellow
  ""
  Write-host "Validating the email addresses. Please wait..." -foregroundColor Yellow
  ""
  $finallist =@()
  foreach($emailAddress in $emailAddresses)
  {
  if((get-recipient $emailaddress -erroraction SilentlyContinue).isvalid -eq 'True')
  {$finallist += $emailaddress}
  else {"Unable to find the user $emailaddress"
  [array]$excludedlist += $emailaddress}
  }
  ""
  #find user's OneDrive Site URL using email address
  Write-Host "Getting the URL for each user's OneDrive for Business site." -foregroundColor Yellow
  ""
  $AdminUrl = "https://$mySiteDomain-admin.sharepoint.com"
  $mySiteUrlRoot = "https://$mySiteDomain-my.sharepoint.com"
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
  $urls = @()
  foreach($emailAddress in $emailAddresses)
  {
        try{
          $prop = $UserProfileService.GetUserProfileByName("i:0#.f|membership|$emailAddress") | Where-Object { $_.Name -eq "PersonalSpace" }
          $url = $prop.values[0].value
        if($url -ne $null){
          $furl = $mySiteUrlRoot + $url
          $urls += $furl
          Write-Host "- $emailAddress => $furl"
        [array]$ODadded += $furl}
    else{    
          Write-Warning "Couldn't locate OneDrive for $emailAddress"
        [array]$ODExluded += $emailAddress
      }}
    catch { 
    Write-Warning "Could not locate OneDrive for $emailAddress"
    [array]$ODExluded += $emailAddress
    Continue }
  }
  if(($finallist.count -gt 0) -or ($urls.count -gt 0)){
  ""
  Write-Host "Creating the hold named $holdname. Please wait..." -foregroundColor Yellow
  if(($holdstatus -eq "Y") -or ($holdstatus -eq  "y") -or ($holdstatus -eq "yes") -or ($holdstatus -eq "YES")){
  New-CaseHoldPolicy -Name "$holdName" -Case "$casename" -ExchangeLocation $finallist -SharePointLocation $urls -Enabled $True | out-null
  New-CaseHoldRule -Name "$holdName" -Policy "$holdname" -ContentMatchQuery $holdQuery | out-null
  }
  else{
  New-CaseHoldPolicy -Name "$holdName" -Case "$casename" -ExchangeLocation $finallist -SharePointLocation $urls -Enabled $false | out-null
  New-CaseHoldRule -Name "$holdName" -Policy "$holdname" -ContentMatchQuery $holdQuery -disabled $true | out-null
  }
  ""
  }
  else {"No valid locations were identified. Therefore, the hold wasn't created."}
  #write log files (if needed)
  $newhold=Get-CaseHoldPolicy -Identity "$holdname" -Case "$casename" -erroraction SilentlyContinue
  $newholdrule=Get-CaseHoldRule -Identity "$holdName" -erroraction SilentlyContinue
  if(($ODAdded.count -gt 0) -or ($ODExluded.count -gt 0) -or ($finallist.count -gt 0) -or ($excludedlist.count -gt 0) -or ($newhold.isvalid -eq 'True') -or ($newholdrule.isvalid -eq 'True'))
  {
  Write-Host "Generating output files..." -foregroundColor Yellow
  if($ODAdded.count -gt 0){
  "OneDrive Locations" | add-content .\LocationsOnHold.txt
  "==================" | add-content .\LocationsOnHold.txt 
  $newhold.SharePointLocation.name | add-content .\LocationsOnHold.txt}
  if($ODExluded.count -gt 0){ 
  "Users without OneDrive locations" | add-content .\LocationsNotOnHold.txt
  "================================" | add-content .\LocationsNotOnHold.txt
  $ODExluded | add-content .\LocationsNotOnHold.txt}
  if($finallist.count -gt 0){
  " " | add-content .\LocationsOnHold.txt
  "Exchange Locations" | add-content .\LocationsOnHold.txt
  "==================" | add-content .\LocationsOnHold.txt 
  $newhold.ExchangeLocation.name | add-content .\LocationsOnHold.txt}
  if($excludedlist.count -gt 0){
  " "| add-content .\LocationsNotOnHold.txt
  "Mailboxes not added to the hold" | add-content .\LocationsNotOnHold.txt
  "===============================" | add-content .\LocationsNotOnHold.txt
  $excludedlist | add-content .\LocationsNotOnHold.txt}
  $FormatEnumerationLimit=-1
  if($newhold.isvalid -eq 'True'){$newhold|fl >.\GetCaseHoldPolicy.txt}
  if($newholdrule.isvalid -eq 'True'){$newholdrule|Fl >.\GetCaseHoldRule.txt}
  }
  }
  else {"The hold wasn't created because no valid entries were found in the text file."}
  ""
  Write-host "Script complete!" -foregroundColor Yellow
  ""
  #script end
  ```

2. 로컬 컴퓨터에서 Windows PowerShell 열고 스크립트를 저장 한 폴더로 이동 합니다.
    
3. 스크립트를 실행 합니다. 예를 들어:
    
      ```
    .\AddUsersToHold.ps1
      ```

4. 이 스크립트는 메시지가 표시 되는 정보를 입력 합니다.
    
    스크립트 하 고 보안 및 규정 준수 센터 PowerShell 연결 하 고 새 보류 eDiscovery 사례에 만들고 목록에서 사용자에 대 한 사서함과 비즈니스용 OneDrive를 추가 합니다. 보안에서 **eDiscovery** 페이지에서 대/소문자도 이동할 수 &amp; 준수 센터 새 보류를 볼 수 있습니다. 
    
스크립트가 완료 되 면 다음 로그 파일을 만듭니다 및 스크립트 위치한 폴더에 저장을 실행 합니다.
  
- **LocationsOnHold.txt** -에 성공적으로 배치 스크립트 보유 하는 비즈니스 사이트에 대 한 사서함 및 OneDrive의 목록을 포함 합니다.
    
- **LocationsNotOnHold.txt** -대기 스크립트를 배치 하지 않고 비즈니스 사이트에 대 한 사서함 및 OneDrive의 목록을 포함 합니다. 사용자 사서함을 하지만 비즈니스 사이트에 대 한 OneDrive 하지 있으면 사용자 보류에 추가 되지 않은 비즈니스 사이트에 대 한 OneDrive의 목록에 포함 됩니다.
    
- **GetCaseHoldPolicy.txt** -새 보류를 만든 후 스크립트를 실행 하는 새 보류에 대 한 **Get CaseHoldPolicy** cmdlet의 출력을 포함 합니다. 이 cmdlet에 의해 반환 되는 정보에는 사용자의 사서함과 비즈니스 사이트에 대 한 OneDrive 대기 하 고 보류의 사용 여부에 배치 된 목록을 포함 됩니다. 
    
- **GetCaseHoldRule.txt** -새 보류를 만든 후 스크립트를 실행 하는 새 보류에 대 한 **Get CaseHoldRule** cmdlet의 출력을 포함 합니다. 쿼리 기반 보류를 만드는 스크립트를 사용 하는 경우이 cmdlet에 의해 반환 되는 정보는 검색 쿼리를 포함 합니다. 
