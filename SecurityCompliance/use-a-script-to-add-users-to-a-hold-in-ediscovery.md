---
title: 스크립트를 사용 하 여 Office 365 보안 &amp; 및 준수 센터에서 eDiscovery 사례의 보류에 사용자 추가
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 1/23/2017
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MOE150
- MED150
- MBS150
ms.assetid: bad352ff-d5d2-45d8-ac2a-6cb832f10e73
description: 스크립트를 실행 하 여 Office 365 보안 &amp; 및 준수 센터에서 eDiscovery 사례와 연결 된 새 보류에 사서함 및 비즈니스용 OneDrive 사이트를 빠르게 추가 합니다.
ms.openlocfilehash: b9d34f4576299dccf0f751c7f204639b5a770b32
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30214288"
---
# <a name="use-a-script-to-add-users-to-a-hold-in-an-ediscovery-case-in-the-office-365-security-amp-compliance-center"></a>스크립트를 사용 하 여 Office 365 보안 &amp; 및 준수 센터에서 eDiscovery 사례의 보류에 사용자 추가

Office 365 보안 &amp; 및 준수 센터는 eDiscovery 사례를 만들고 관리 하는 데 관련 된 시간이 오래 걸리는 작업을 자동화할 수 있는 다양 한 Windows PowerShell cmdlet을 제공 합니다. 현재는 보안 &amp; 및 준수 센터의 eDiscovery 사례 도구를 사용 하 여 많은 수의 custodian 콘텐츠 위치를 유지 하는 데 시간이 오래 걸리고 준비를 진행 하 고 있습니다. 예를 들어 보류를 만들기 전에 보류 하려는 각 비즈니스용 OneDrive 사이트의 URL을 수집 해야 합니다. 그런 다음 보류 하려는 각 사용자에 대해 해당 사서함 및 비즈니스용 OneDrive 사이트를 보류에 추가 해야 합니다. 향후 릴리스된 보안 &amp; 및 준수 센터에서이 작업을 수행 하는 것이 더 쉽습니다. 그때까지이 문서의 스크립트를 사용 하 여이 프로세스를 자동화할 수 있습니다.
  
스크립트는 URL https://contoso-my.sharepoint.com)의 **contoso** , 기존 eDiscovery 사례 이름, 사례와 연결 된 새 보류의 이름, 원하는 사용자의 전자 메일 주소 목록 등을 묻는 메시지를 표시 하는 것입니다. 유지 하 고 쿼리 기반 보존을 만들려는 경우 사용할 검색 쿼리를 선택 합니다. 그런 다음 스크립트는 목록에 있는 각 사용자의 비즈니스용 onedrive 사이트에 대 한 URL을 가져오고, 새로 보존을 만든 다음 목록에 있는 각 사용자에 대 한 비즈니스용 onedrive 사이트를 보류에 추가 합니다. 또한이 스크립트는 새로 보존에 대 한 정보가 포함 된 로그 파일을 생성 합니다. 
  
이 작업을 수행 하는 단계는 다음과 같습니다.
  
[1단계: SharePoint Online 관리 셸 설치](use-a-script-to-add-users-to-a-hold-in-ediscovery.md#step1)
  
[2 단계: 사용자 목록 생성](use-a-script-to-add-users-to-a-hold-in-ediscovery.md#step2)
  
[3 단계: 스크립트를 실행 하 여 보류 만들기 및 사용자 추가](use-a-script-to-add-users-to-a-hold-in-ediscovery.md#step3)
  
## <a name="before-you-begin"></a>시작하기 전에

- 3 단계에서 스크립트를 실행 하려면 보안 &amp; 및 준수 센터에서 eDiscovery 관리자 역할 그룹의 구성원 이어야 하 고 SharePoint Online 전역 관리자에 게 문의 해야 합니다. 자세한 내용은 [Office 365 보안 &amp; 및 준수 센터에서 eDiscovery 사용 권한 할당](assign-ediscovery-permissions.md)을 참조 하세요.
    
- 최대 1000 개의 사서함과 100 사이트를 보안 &amp; 및 준수 센터에서 eDiscovery 사례와 연결 된 보류에 추가할 수 있습니다. 보존 하려는 모든 사용자에 게 비즈니스용 OneDrive 사이트가 있는 경우이 문서의 스크립트를 사용 하 여 최대 100 명의 사용자를 보류에 추가할 수 있습니다. 
    
- 2 단계에서 만든 사용자 목록과 3 단계의 스크립트를 같은 폴더에 저장 해야 합니다. 이를 통해 스크립트를 보다 쉽게 실행할 수 있습니다.
    
- 이 스크립트는 기존 사례와 연결 된 새 보류에 사용자 목록을 추가 합니다. 스크립트를 실행 하기 전에 보류를 연결 하려는 대/소문자를 만들어야 합니다.
    
- 스크립트에 최소 오류 처리가 포함 되어 있습니다. 이 기본 목적은 사서함과 각 사용자의 비즈니스용 OneDrive 사이트를 보류 하 고 쉽게 사용할 수 있도록 하는 것입니다.
    
- 이 항목에서 제공된 샘플 스크립트는 Microsoft 표준 지원 프로그램 또는 서비스에서는 지원되지 않습니다. 샘플 스크립트는 어떠한 보증도 없이 "있는 그대로" 제공됩니다. Microsoft는 묵시적인 모든 보증(상품성 또는 특정 목적에의 적합성에 대한 묵시적인 보증을 포함하되 이에 제한되지 않음)을 부인합니다. 샘플 스크립트 및 문서의 사용 또는 수행으로 인해 발생하는 모든 위험은 사용자의 책임입니다. 어떠한 경우에도 Microsoft, 스크립트 작성자 또는 스크립트의 작성, 생산 또는 제공과 관련된 사람은 누구나 샘플 스크립트 또는 문서의 사용 또는 사용 불가능으로 인해 발생하는 모든 손해(수익에 대한 손실, 비즈니스 중단, 비즈니스 정보 손실 또는 기타 금전상의 손실을 포함하되 이에 제한되지 않음)에 대해 책임지지 않습니다. 이는 Microsoft가 이러한 손해가 발생할 가능성에 대해 알고 있었더라고 마찬가지입니다.

## <a name="step-1-install-the-sharepoint-online-management-shell"></a>1단계: SharePoint Online 관리 셸 설치

첫 번째 단계는 SharePoint Online 관리 셸을 로컬 컴퓨터에 아직 설치 하지 않은 경우 설치 하는 것입니다. 이 절차에서 셸을 사용할 필요는 없지만 3 단계에서 실행 하는 스크립트에 필요한 필수 구성 요소를 포함 하기 때문에 설치 해야 합니다. 이러한 필수 구성 요소를 통해 스크립트가 SharePoint Online과 통신 하 여 비즈니스용 OneDrive 사이트용 url을 가져올 수 있습니다.
  
[sharepoint online 관리 셸 Windows PowerShell 환경 설정](https://go.microsoft.com/fwlink/p/?LinkID=286318) 으로 이동 하 여 1 단계와 2 단계를 수행 하 여 로컬 컴퓨터에 SharePoint online 관리 셸을 설치 합니다. 

## <a name="step-2-generate-a-list-of-users"></a>2 단계: 사용자 목록 생성
<a name="step2"> </a>

3 단계의 스크립트에서는 eDiscovery 사례와 연결 된 보류를 만들고 사용자 목록의 사서함 및 비즈니스용 OneDrive 사이트를 보류에 추가 합니다. 텍스트 파일에 전자 메일 주소를 입력 하거나, Windows PowerShell에서 명령을 실행 하 여 전자 메일 주소 목록을 가져오고이를 파일 (3 단계에서 스크립트를 저장할 동일한 폴더에 있음)에 저장할 수 있습니다.
  
다음은 Exchange Online 조직에 연결 된 원격 powershell을 사용 하 여 실행 하는 PowerShell 명령으로, 조직의 모든 사용자에 대 한 전자 메일 주소 목록을 가져오고이를 HoldUsers 이라는 텍스트 파일에 저장 하는 것입니다.
  
```
Get-Mailbox -ResultSize unlimited -Filter { RecipientTypeDetails -eq 'UserMailbox'} | Select-Object PrimarySmtpAddress > HoldUsers.txt
```

이 명령을 실행 한 후에는 텍스트 파일을 열고 속성 이름이 포함 된 헤더를 제거 `PrimarySmtpAddress`합니다. 그런 다음 3 단계에서 만들 보류에 추가할 사용자에 대 한 전자 메일 주소를 제외 하 고 모두 제거 합니다. 전자 메일 주소 목록 앞 이나 뒤에 빈 행이 없는지 확인 합니다.
  

  
## <a name="step-3-run-the-script-to-create-a-hold-and-add-users"></a>3 단계: 스크립트를 실행 하 여 보류 만들기 및 사용자 추가
<a name="step3"> </a>

이 단계에서 스크립트를 실행 하면 다음 정보를 입력 하 라는 메시지가 표시 됩니다. 스크립트를 실행 하기 전에이 정보를 준비 해야 합니다.
  
- **사용자 자격 증명** -스크립트는 자격 증명을 사용 하 여 원격 PowerShell을 &amp; 통해 보안 준수 센터에 연결 합니다. 또한 이러한 자격 증명을 사용 하 여 SharePoint Online에 액세스 하 여 사용자 목록에 대 한 비즈니스용 OneDrive url을 가져옵니다.
    
- **내 사이트 도메인 이름** -내 사이트 도메인은 조직 내 모든 비즈니스용 OneDrive 사이트가 포함 된 도메인입니다. 예를 들어 내 사이트 도메인의 URL이 인 **https://contoso-my.sharepoint.com**경우 스크립트에서 내 사이트 도메인 `contoso` 이름을 묻는 메시지를 표시 하는 경우를 입력 합니다. 
    
- **대/소문자 이름** -기존 사례 이름입니다. 스크립트는이 사례와 연결 된 새 보류를 만듭니다.
    
- **보류의 이름** -스크립트를 만들어 지정 된 사례와 연결할 보류의 이름입니다.
    
- **쿼리 기반 보존에 대 한 검색 쿼리** -지정 된 검색 조건을 충족 하는 콘텐츠만 보존 되도록 쿼리 기반 보존을 만들 수 있습니다. 모든 콘텐츠를 보류 상태로 설정 하려면 검색 쿼리를 **입력** 하 라는 메시지가 표시 되 면 enter 키를 누르기만 하면 됩니다. 
    
- **보류를 설정 하지 않을 지 여부를 지정 하** 는 경우에는 스크립트를 만든 후에이를 설정할 수 있으며, 스크립트를 사용 하지 않고 보류를 만들 수 있습니다. 스크립트에서 보류를 설정 하지 않은 경우 나중에 보안 &amp; 및 준수 센터에서 설정 하거나 다음 PowerShell 명령을 실행 하 여 설정할 수 있습니다. 
    
  ```
  Set-CaseHoldPolicy -Identity <name of the hold> -Enabled $true
  ```

  ```
  Set-CaseHoldRule -Identity <name of the hold> -Disabled $false
  ```

- **사용자 목록이 포함 된 텍스트 파일의 이름** -2 단계의 텍스트 파일 이름으로, 보류에 추가할 사용자의 목록이 들어 있습니다. 이 파일이 스크립트와 같은 폴더에 있는 경우 파일의 이름 (예: HoldUsers)을 입력 하면 됩니다. 텍스트 파일이 다른 폴더에 있으면 파일의 전체 경로 이름을 입력 합니다.
    
스크립트에서 입력 해야 하는 정보를 수집한 후 마지막 단계는 스크립트를 실행 하 여 새 보류를 만들고 사용자를 추가 하는 것입니다.
  
1. 파일 이름 접미사. p s 1을 사용 하 여 Windows PowerShell 스크립트 파일에 다음 텍스트를 저장 합니다. 예를 `AddUsersToHold.ps1`들면입니다.
    
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

2. 로컬 컴퓨터에서 Windows PowerShell을 열고 스크립트를 저장 한 폴더로 이동 합니다.
    
3. 스크립트를 실행 합니다. 예를 들어:
    
      ```
    .\AddUsersToHold.ps1
      ```

4. 스크립트에서 묻는 메시지가 표시 되는 정보를 입력 합니다.
    
    이 스크립트는 Security & 준수 센터 PowerShell에 연결한 다음 eDiscovery 사례에 새로 보존을 만들고 사서함 및 비즈니스용 OneDrive를 목록의 사용자에 게 추가 합니다. 보안 &amp; 및 준수 센터의 **eDiscovery** 페이지에서 사례로 이동 하 여 새 보류를 볼 수 있습니다. 
    
스크립트 실행이 완료 되 면 다음 로그 파일이 만들어지고 스크립트가 있는 폴더에 저장 됩니다.
  
- **LocationsOnHold** -스크립트가 성공적으로 보류 된 사서함 및 비즈니스용 OneDrive 사이트의 목록을 포함 합니다.
    
- **LocationsNotOnHold** -스크립트가 보류 되지 않은 사서함 및 비즈니스용 OneDrive 사이트의 목록이 포함 되어 있습니다. 사용자에 게 사서함이 있지만 비즈니스용 onedrive 사이트가 아닌 경우에는 보류 되지 않은 비즈니스용 onedrive 사이트 목록에 사용자가 포함 됩니다.
    
- **GetCaseHoldPolicy** -새 보류를 만든 후 스크립트가 실행 된 새 보류에 대 한 **new-caseholdpolicy** cmdlet의 출력을 포함 합니다. 이 cmdlet이 반환 하는 정보에는 사서함과 비즈니스용 OneDrive 사이트를 보류 하는 사용자 목록과 보류를 사용 하거나 사용 하지 않도록 설정 되어 있습니다. 
    
- **GetCaseHoldRule** -새 보류를 만든 후 스크립트가 실행 된 새 보류에 대 한 **new-caseholdrule** cmdlet의 출력을 포함 합니다. 이 cmdlet이 반환 하는 정보에는 스크립트를 사용 하 여 쿼리 기반 보존을 만든 경우 검색 쿼리가 포함 됩니다. 
