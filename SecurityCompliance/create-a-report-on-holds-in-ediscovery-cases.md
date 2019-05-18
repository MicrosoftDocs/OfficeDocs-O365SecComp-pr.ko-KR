---
title: Office 365의 eDiscovery 사례에 대 한 보고서를 작성 합니다.
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 9/11/2017
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
search.appverid: MOE150
ms.assetid: cca08d26-6fbf-4b2c-b102-b226e4cd7381
description: 이 문서의 스크립트를 사용 하 여 Office 365 또는 Microsoft 365의 준수 센터에서 eDiscovery 사례와 관련 된 모든 보류에 대 한 정보를 포함 하는 보고서를 생성 합니다.
ms.openlocfilehash: 7118b62dcd42413309e33c45e80516c8822faeff
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/17/2019
ms.locfileid: "34151290"
---
# <a name="create-a-report-on-holds-in-ediscovery-cases-in-office-365"></a>Office 365의 eDiscovery 사례에 대 한 보고서를 작성 합니다.
  
이 문서의 스크립트를 통해 eDiscovery 관리자 및 eDiscovery 관리자는 Office 365 또는 Microsoft 365의 준수 센터에 있는 eDiscovery 사례와 관련 된 모든 보존 정보를 포함 하는 보고서를 생성할 수 있습니다. 이 보고서에는 보류가 연결 된 사례 이름, 보류 중인 콘텐츠 위치, 쿼리 기반 인지 여부 등의 정보가 포함 됩니다. 보류 된 상태가 없는 경우가 있으면 스크립트는 보류가 없는 사례 목록이 포함 된 추가 보고서를 만듭니다.

보고서에 포함 된 정보에 대 한 자세한 [내용은 추가 정보](#more-information) 섹션을 참조 하십시오. 
  
## <a name="before-you-begin"></a>시작하기 전에

- 조직의 모든 eDiscovery 사례에 대 한 보고서를 생성 하려면 조직의 eDiscovery 관리자 여야 합니다. EDiscovery 관리자 인 경우 보고서에 액세스할 수 있는 사례에 대 한 정보만 포함 됩니다. EDiscovery 권한에 대 한 자세한 내용은 [ediscovery 사용 권한 할당](assign-ediscovery-permissions.md)을 참조 하십시오.
    
- 이 문서의 스크립트에는 최소한의 오류 처리가 있습니다. 기본 목적은 조직의 eDiscovery 사례와 연결 된 보류에 대 한 보고서를 빠르게 만드는 것입니다.
    
- 이 항목에서 제공된 샘플 스크립트는 Microsoft 표준 지원 프로그램 또는 서비스에서는 지원되지 않습니다. 샘플 스크립트는 어떠한 보증도 없이 "있는 그대로" 제공됩니다. Microsoft는 묵시적인 모든 보증(상품성 또는 특정 목적에의 적합성에 대한 묵시적인 보증을 포함하되 이에 제한되지 않음)을 부인합니다. 샘플 스크립트 및 문서의 사용 또는 수행으로 인해 발생하는 모든 위험은 사용자의 책임입니다. 어떠한 경우에도 Microsoft, 스크립트 작성자 또는 스크립트의 작성, 생산 또는 제공과 관련된 사람은 누구나 샘플 스크립트 또는 문서의 사용 또는 사용 불가능으로 인해 발생하는 모든 손해(수익에 대한 손실, 비즈니스 중단, 비즈니스 정보 손실 또는 기타 금전상의 손실을 포함하되 이에 제한되지 않음)에 대해 책임지지 않습니다. 이는 Microsoft가 이러한 손해가 발생할 가능성에 대해 알고 있었더라고 마찬가지입니다.
    
## <a name="step-1-connect-to-the-security--compliance-center-powershell"></a>1 단계: Security & 준수 센터 PowerShell에 연결

첫 번째 단계는 조직의 Security & 준수 센터에 연결 하는 것입니다.
  
1. 파일 이름 접미사. p s 1을 사용 하 여 Windows PowerShell 스크립트 파일에 다음 텍스트를 저장 합니다. 예를 `ConnectSCC.ps1`들면입니다. 
    
      ```
      # Get login credentials 
      $UserCredential = Get-Credential 
      $Session = New-PSSession -ConfigurationName Microsoft.Exchange -ConnectionUri https://ps.compliance.protection.outlook.com/powershell-liveid -Credential $UserCredential -Authentication Basic -AllowRedirection 
      Import-PSSession $Session -AllowClobber -DisableNameChecking 
      $Host.UI.RawUI.WindowTitle = $UserCredential.UserName + " (Security & Compliance Center)" 
    ```

2. 로컬 컴퓨터에서 Windows PowerShell을 열고 스크립트를 저장 한 폴더로 이동 합니다. 
    
3. 스크립트를 실행 합니다. 예를 들어:

    ```
    .\ConnectSCC.ps1
    ```
   
4. 자격 증명을 묻는 메시지가 표시 되 면 전자 메일 주소와 암호를 입력 하 고 **확인**을 클릭 합니다. 
  
## <a name="step-2-run-the-script-to-report-on-holds-associated-with-ediscovery-cases"></a>2 단계: 스크립트를 실행 하 여 eDiscovery 사례와 연결 된 보류에 대해 보고

보안 & 준수 센터 PowerShell에 연결한 후에는 조직의 eDiscovery 사례에 대 한 정보를 수집 하는 스크립트를 만들고 실행 해야 합니다. 
  
1. 파일 이름 접미사. p s 1을 사용 하 여 Windows PowerShell 스크립트 파일에 다음 텍스트를 저장 합니다. 예: CaseHoldsReport. 
    
  ```
#script begin
" " 
write-host "***********************************************"
write-host "   Security & Compliance Center   " -foregroundColor yellow -backgroundcolor darkgreen
write-host "        eDiscovery cases - Holds report         " -foregroundColor yellow -backgroundcolor darkgreen 
write-host "***********************************************"
" " 
#prompt users to specify a path to store the output files
$time=get-date
$Path = Read-Host 'Enter a file path to save the report to a .csv file'
$outputpath=$Path+'\'+'CaseHoldsReport'+' '+$time.day+'-'+$time.month+'-'+$time.year+' '+$time.hour+'.'+$time.minute+'.csv'
$noholdsfilepath=$Path+'\'+'CaseswithNoHolds'+' '+$time.day+'-'+$time.month+'-'+$time.year+' '+$time.hour+'.'+$time.minute+'.csv'
#add case details to the csv file
function add-tocasereport{
Param([string]$casename,
[String]$casestatus,
[datetime]$casecreatedtime,
[string]$casemembers,
[datetime]$caseClosedDateTime,
[string]$caseclosedby,
[string]$holdname,
[String]$Holdenabled,
[string]$holdcreatedby,
[string]$holdlastmodifiedby,
[string]$ExchangeLocation,
[string]$sharePointlocation,
[string]$ContentMatchQuery,
[datetime]$holdcreatedtime,
[datetime]$holdchangedtime
)
$addRow = New-Object PSObject 
Add-Member -InputObject $addRow -MemberType NoteProperty -Name "Case name" -Value $casename
Add-Member -InputObject $addRow -MemberType NoteProperty -Name "Case status" -Value $casestatus
Add-Member -InputObject $addRow -MemberType NoteProperty -Name "Case members" -Value $casemembers
Add-Member -InputObject $addRow -MemberType NoteProperty -Name "Case created time" -Value $casecreatedtime
Add-Member -InputObject $addRow -MemberType NoteProperty -Name "Case closed time" -Value $caseClosedDateTime
Add-Member -InputObject $addRow -MemberType NoteProperty -Name "Case closed by" -Value $caseclosedby
Add-Member -InputObject $addRow -MemberType NoteProperty -Name "Hold name" -Value $holdname
Add-Member -InputObject $addRow -MemberType NoteProperty -Name "Hold enabled" -Value $Holdenabled
Add-Member -InputObject $addRow -MemberType NoteProperty -Name "Hold created by" -Value $holdcreatedby
Add-Member -InputObject $addRow -MemberType NoteProperty -Name "Hold last changed by" -Value $holdlastmodifiedby
Add-Member -InputObject $addRow -MemberType NoteProperty -Name "Exchange locations" -Value  $ExchangeLocation
Add-Member -InputObject $addRow -MemberType NoteProperty -Name "SharePoint locations" -Value $sharePointlocation
Add-Member -InputObject $addRow -MemberType NoteProperty -Name "Hold query" -Value $ContentMatchQuery
Add-Member -InputObject $addRow -MemberType NoteProperty -Name "Hold created time (UTC)" -Value $holdcreatedtime
Add-Member -InputObject $addRow -MemberType NoteProperty -Name "Hold changed time (UTC)" -Value $holdchangedtime
$allholdreport = $addRow | Select-Object "Case name","Case status","Hold name","Hold enabled","Case members", "Case created time","Case closed time","Case closed by","Exchange locations","SharePoint locations","Hold query","Hold created by","Hold created time (UTC)","Hold last changed by","Hold changed time (UTC)"
$allholdreport | export-csv -path $outputPath -notypeinfo -append -Encoding ascii 
}
#get information on the cases and pass values to the case report function
" "
write-host "Gathering a list of cases and holds..."
" "
$edc =Get-ComplianceCase -ErrorAction SilentlyContinue
foreach($cc in $edc)
{
write-host "Working on case :" $cc.name
if($cc.status -eq 'Closed')
{
$cmembers = ((Get-ComplianceCaseMember -Case $cc.name).windowsLiveID)-join ';'
add-tocasereport -casename $cc.name -casestatus $cc.Status -caseclosedby $cc.closedby -caseClosedDateTime $cc.ClosedDateTime -casemembers $cmembers 
}
else{
$cmembers = ((Get-ComplianceCaseMember -Case $cc.name).windowsLiveID)-join ';'
$policies = Get-CaseHoldPolicy -Case $cc.Name | %{ Get-CaseHoldPolicy $_.Name -Case $_.CaseId -DistributionDetail}
if ($policies -ne $NULL)
{
foreach ($policy in $policies)
{
$rule=Get-CaseHoldRule -Policy $policy.name
add-tocasereport -casename $cc.name -casemembers $cmembers -casestatus $cc.Status -casecreatedtime $cc.CreatedDateTime -holdname $policy.name -holdenabled $policy.enabled -holdcreatedby $policy.CreatedBy -holdlastmodifiedby $policy.LastModifiedBy -ExchangeLocation (($policy.exchangelocation.name)-join ';') -SharePointLocation (($policy.sharePointlocation.name)-join ';') -ContentMatchQuery $rule.ContentMatchQuery -holdcreatedtime $policy.WhenCreatedUTC -holdchangedtime $policy.WhenChangedUTC
}
}
else{
write-host "No hold policies found in case:" $cc.name -foregroundColor 'Yellow'
" "
[string]$cc.name | out-file -filepath $noholdsfilepath -append 
}
}
}

" "
Write-host "Script complete! Report files saved to this folder: '$Path'"
" "
#script end
  ```

2. 1 단계에서 연 Windows PowerShell 세션에서 스크립트를 저장 한 폴더로 이동 합니다. 
    
3. 스크립트를 실행 합니다. 예를 들어:

    ```
    .\CaseHoldsReport.ps1
    ```

    스크립트는 보고서를 저장할 대상 폴더를 입력 하 라는 메시지를 표시 합니다. 
    
4. 보고서를 저장할 폴더의 전체 경로 이름을 입력 한 다음 enter 키를 누릅니다. ****
    
    > [!TIP]
    > 스크립트가 있는 폴더에 보고서를 저장 하려면 대상 폴더를 묻는 메시지가 표시 되 면 마침표 (".")를 입력 합니다. 스크립트가 있는 폴더의 하위 폴더에 보고서를 저장 하려면 하위 폴더의 이름만 입력 하면 됩니다. 
  
    스크립트에서 조직의 모든 eDiscovery 사례에 대 한 정보를 수집 하기 시작 합니다. 스크립트가 실행 되는 동안에는 보고서 파일에 액세스 하지 마세요. 스크립트가 완료 되 면 Windows PowerShell 세션에 확인 메시지가 표시 됩니다. 이 메시지가 표시 되 면 4 단계에서 지정한 폴더의 보고서에 액세스할 수 있습니다. 보고서의 파일 이름은 `CaseHoldsReport<DateTimeStamp>.csv`입니다.

    Addtionally을 사용 하는 경우 스크립트는 보류 된 것이 없는 사례 목록을 포함 하는 보고서도 만듭니다. 이 보고서의 파일 이름은 `CaseswithNoHolds<DateTimeStamp>.csv`입니다.
    
    다음은 CaseHoldsReport 스크립트를 실행 하는 예제입니다. 
    
    ![CaseHoldsReport 스크립트를 실행 한 후의 출력](media/7d312ed5-505e-4ec5-8f06-3571e3524a1a.png)
  
## <a name="more-information"></a>추가 정보

이 문서의 스크립트를 실행할 때 생성 되는 보고서에는 각 보류에 대 한 다음과 같은 정보가 포함 되어 있습니다. 앞에서 설명한 것 처럼, 조직의 모든 보류에 대 한 정보를 반환 하려면 eDiscovery 관리자 여야 합니다. 사례 보류에 대 한 자세한 내용은 [eDiscovery 사례](ediscovery-cases.md)를 참조 하십시오.
  
  - 보류의 이름과 보류가 연결 된 eDiscovery 사례의 이름입니다.
    
  - EDiscovery 사례가 활성 상태 인지 닫혀 있는지 여부
    
  - 보류를 사용 하거나 사용 하지 않도록 설정할지 여부를 지정 합니다.
    
  - 보류가 연결 된 eDiscovery 사례의 구성원입니다. 사례 구성원은 할당 된 eDiscovery 권한에 따라 사례를 보거나 관리할 수 있습니다.
    
  - 사례를 만든 날짜와 시간입니다.
    
  - 사례가 닫히면 해당 사례를 닫은 사람 및 종료 된 시간 및 날짜입니다.
    
  - 보류 중인 Exchange 사서함 및 SharePoint 사이트 위치입니다.
    
  - 보류가 쿼리 기반 인 경우 쿼리 구문입니다.
    
  - 보류가 만들어진 날짜와 시간 및이를 만든 사람입니다.
    
  - 보류를 마지막으로 변경한 날짜와 시간을 변경한 사람입니다.
