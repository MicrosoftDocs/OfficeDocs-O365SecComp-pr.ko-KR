---
title: Office 365의 eDiscovery 사례에 대 한 보고서를 작성 합니다.
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 9/11/2017
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid: MOE150
ms.assetid: cca08d26-6fbf-4b2c-b102-b226e4cd7381
description: 이 문서의 스크립트를 사용 하 여 Office 365 보안 &amp; 및 준수 센터의 eDiscovery 사례와 관련 된 모든 보존 정보를 포함 하는 보고서를 생성 합니다.
ms.openlocfilehash: cf547ff7c76ba6e16a3bde18465ae0aef9ab4075
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30217439"
---
# <a name="create-a-report-on-holds-in-ediscovery-cases-in-office-365"></a><span data-ttu-id="059ae-103">Office 365의 eDiscovery 사례에 대 한 보고서를 작성 합니다.</span><span class="sxs-lookup"><span data-stu-id="059ae-103">Create a report on holds in eDiscovery cases in Office 365</span></span>
  
<span data-ttu-id="059ae-p101">이 문서의 스크립트를 사용 하면 ediscovery 관리자 및 ediscovery 관리자가 Office 365 보안 &amp; 및 준수 센터의 ediscovery 사례와 관련 된 모든 보존 정보를 포함 하는 보고서를 생성할 수 있습니다. 이 보고서에는 보류가 연결 된 사례 이름, 보류 중인 콘텐츠 위치, 쿼리 기반 인지 여부 등의 정보가 포함 됩니다. 보류 된 상태가 없는 경우가 있으면 스크립트는 보류가 없는 사례 목록이 포함 된 추가 보고서를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="059ae-p101">The script in this article lets eDiscovery administrators and eDiscovery managers generate a report that contains information about all holds that are associated with eDiscovery cases in the Office 365 Security &amp; Compliance Center. The report contains information such as the name of the case a hold is associated with, the content locations that are placed on hold, and whether the hold is query-based. If there are cases that don't have any holds, the script will create an additional report with a list of cases without holds.</span></span>

<span data-ttu-id="059ae-107">보고서에 포함 된 정보에 대 한 자세한 [내용은 추가 정보](#more-information) 섹션을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="059ae-107">See the [More information](#more-information) section for a detailed description of the information included in the report.</span></span> 
  
## <a name="before-you-begin"></a><span data-ttu-id="059ae-108">시작하기 전에</span><span class="sxs-lookup"><span data-stu-id="059ae-108">Before you begin</span></span>

- <span data-ttu-id="059ae-p102">조직의 모든 ediscovery 사례에 대 한 보고서를 생성 하려면 조직의 ediscovery 관리자 여야 합니다. eDiscovery 관리자 인 경우 보고서에 액세스할 수 있는 사례에 대 한 정보만 포함 됩니다. ediscovery 권한에 대 한 자세한 내용은 [Office 365 보안 &amp; 및 준수 센터에서 ediscovery 사용 권한 할당](assign-ediscovery-permissions.md)을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="059ae-p102">To generate a report on all eDiscovery cases in your organization, you have to be an eDiscovery Administrator in your organization. If you are an eDiscovery Manager, the report will only include information about the cases that you can access. For more information about eDiscovery permissions, see [Assign eDiscovery permissions in the Office‍ 365 Security &amp; Compliance Center](assign-ediscovery-permissions.md).</span></span>
    
- <span data-ttu-id="059ae-p103">이 문서의 스크립트에는 최소한의 오류 처리가 있습니다. 기본 목적은 조직의 eDiscovery 사례와 연결 된 보류에 대 한 보고서를 빠르게 만드는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="059ae-p103">The script in this article has minimal error handling. The primary purpose is to quickly create report about the holds that are associated with the eDiscovery cases in your organization.</span></span>
    
- <span data-ttu-id="059ae-p104">이 항목에서 제공된 샘플 스크립트는 Microsoft 표준 지원 프로그램 또는 서비스에서는 지원되지 않습니다. 샘플 스크립트는 어떠한 보증도 없이 "있는 그대로" 제공됩니다. Microsoft는 묵시적인 모든 보증(상품성 또는 특정 목적에의 적합성에 대한 묵시적인 보증을 포함하되 이에 제한되지 않음)을 부인합니다. 샘플 스크립트 및 문서의 사용 또는 수행으로 인해 발생하는 모든 위험은 사용자의 책임입니다. 어떠한 경우에도 Microsoft, 스크립트 작성자 또는 스크립트의 작성, 생산 또는 제공과 관련된 사람은 누구나 샘플 스크립트 또는 문서의 사용 또는 사용 불가능으로 인해 발생하는 모든 손해(수익에 대한 손실, 비즈니스 중단, 비즈니스 정보 손실 또는 기타 금전상의 손실을 포함하되 이에 제한되지 않음)에 대해 책임지지 않습니다. 이는 Microsoft가 이러한 손해가 발생할 가능성에 대해 알고 있었더라고 마찬가지입니다.</span><span class="sxs-lookup"><span data-stu-id="059ae-p104">The sample scripts provided in this topic aren't supported under any Microsoft standard support program or service. The sample scripts are provided AS IS without warranty of any kind. Microsoft further disclaims all implied warranties including, without limitation, any implied warranties of merchantability or of fitness for a particular purpose. The entire risk arising out of the use or performance of the sample scripts and documentation remains with you. In no event shall Microsoft, its authors, or anyone else involved in the creation, production, or delivery of the scripts be liable for any damages whatsoever (including, without limitation, damages for loss of business profits, business interruption, loss of business information, or other pecuniary loss) arising out of the use of or inability to use the sample scripts or documentation, even if Microsoft has been advised of the possibility of such damages.</span></span>
    
## <a name="step-1-connect-to-the-security-amp-compliance-center-using-remote-powershell"></a><span data-ttu-id="059ae-119">1 단계: 원격 PowerShell을 사용 &amp; 하 여 보안 및 준수 센터에 연결</span><span class="sxs-lookup"><span data-stu-id="059ae-119">Step 1: Connect to the Security &amp; Compliance Center using Remote PowerShell</span></span>

<span data-ttu-id="059ae-120">첫 번째 단계는 Windows PowerShell을 조직의 보안 &amp; 및 준수 센터에 연결 하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="059ae-120">The first step is to connect Windows PowerShell to the Security &amp; Compliance Center for your organization.</span></span>
  
1. <span data-ttu-id="059ae-121">파일 이름 접미사. p s 1을 사용 하 여 Windows PowerShell 스크립트 파일에 다음 텍스트를 저장 합니다. 예를 `ConnectSCC.ps1`들면입니다.</span><span class="sxs-lookup"><span data-stu-id="059ae-121">Save the following text to a Windows PowerShell script file by using a filename suffix of .ps1; for example, `ConnectSCC.ps1`.</span></span> 
    
      ```
      # Get login credentials 
      $UserCredential = Get-Credential 
      $Session = New-PSSession -ConfigurationName Microsoft.Exchange -ConnectionUri https://ps.compliance.protection.outlook.com/powershell-liveid -Credential $UserCredential -Authentication Basic -AllowRedirection 
      Import-PSSession $Session -AllowClobber -DisableNameChecking 
      $Host.UI.RawUI.WindowTitle = $UserCredential.UserName + " (Office 365 Security &amp; Compliance Center)" 
    ```

2. <span data-ttu-id="059ae-122">로컬 컴퓨터에서 Windows PowerShell을 열고 스크립트를 저장 한 폴더로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="059ae-122">On your local computer, open Windows PowerShell and go to the folder where you saved the script.</span></span> 
    
3. <span data-ttu-id="059ae-123">스크립트를 실행 합니다. 예를 들어:</span><span class="sxs-lookup"><span data-stu-id="059ae-123">Run the script; for example:</span></span>

    ```
    .\ConnectSCC.ps1
    ```
   
4. <span data-ttu-id="059ae-124">자격 증명을 묻는 메시지가 표시 되 면 전자 메일 주소와 암호를 입력 하 고 **확인**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="059ae-124">When prompted for your credentials, enter your email address and password, and then click **OK**.</span></span> 
  
## <a name="step-2-run-the-script-to-report-on-holds-associated-with-ediscovery-cases"></a><span data-ttu-id="059ae-125">2 단계: 스크립트를 실행 하 여 eDiscovery 사례와 연결 된 보류에 대해 보고</span><span class="sxs-lookup"><span data-stu-id="059ae-125">Step 2: Run the script to report on holds associated with eDiscovery cases</span></span>

<span data-ttu-id="059ae-126">원격 PowerShell을 사용 하 여 보안 &amp; 및 준수 센터에 연결한 후에는 조직의 eDiscovery 사례에 대 한 정보를 수집 하는 스크립트를 만들고 실행 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="059ae-126">After you've connected to the Security &amp; Compliance Center with remote PowerShell, the next step is to create and run the script that collects information about the eDiscovery cases in your organization.</span></span> 
  
1. <span data-ttu-id="059ae-127">파일 이름 접미사. p s 1을 사용 하 여 Windows PowerShell 스크립트 파일에 다음 텍스트를 저장 합니다. 예: CaseHoldsReport.</span><span class="sxs-lookup"><span data-stu-id="059ae-127">Save the following text to a Windows PowerShell script file by using a filename suffix of .ps1; for example, CaseHoldsReport.ps1.</span></span> 
    
  ```
#script begin
" " 
write-host "***********************************************"
write-host "   Office 365 Security & Compliance Center   " -foregroundColor yellow -backgroundcolor darkgreen
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

2. <span data-ttu-id="059ae-128">1 단계에서 연 Windows PowerShell 세션에서 스크립트를 저장 한 폴더로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="059ae-128">In the Windows PowerShell session that opened in Step 1, go to the folder where you saved the script.</span></span> 
    
3. <span data-ttu-id="059ae-129">스크립트를 실행 합니다. 예를 들어:</span><span class="sxs-lookup"><span data-stu-id="059ae-129">Run the script; for example:</span></span>

    ```
    .\CaseHoldsReport.ps1
    ```

    <span data-ttu-id="059ae-130">스크립트는 보고서를 저장할 대상 폴더를 입력 하 라는 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="059ae-130">The script will prompt for a target folder to save the report to.</span></span> 
    
4. <span data-ttu-id="059ae-131">보고서를 저장할 폴더의 전체 경로 이름을 입력 한 다음 enter 키를 누릅니다. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="059ae-131">Type the full path name of the folder to save the report to, and then press **Enter**.</span></span>
    
    > [!TIP]
    > <span data-ttu-id="059ae-p105">스크립트가 있는 폴더에 보고서를 저장 하려면 대상 폴더를 묻는 메시지가 표시 되 면 마침표 (".")를 입력 합니다. 스크립트가 있는 폴더의 하위 폴더에 보고서를 저장 하려면 하위 폴더의 이름만 입력 하면 됩니다.</span><span class="sxs-lookup"><span data-stu-id="059ae-p105">To save the report in the same folder that the script is located in, type a period (".") when prompted for a target folder. To save the report in a subfolder in the folder where the script is located, just type the name of the subfolder.</span></span> 
  
    <span data-ttu-id="059ae-p106">스크립트에서 조직의 모든 eDiscovery 사례에 대 한 정보를 수집 하기 시작 합니다. 스크립트가 실행 되는 동안에는 보고서 파일에 액세스 하지 마세요. 스크립트가 완료 되 면 Windows PowerShell 세션에 확인 메시지가 표시 됩니다. 이 메시지가 표시 되 면 4 단계에서 지정한 폴더의 보고서에 액세스할 수 있습니다. 보고서의 파일 이름은 `CaseHoldsReport<DateTimeStamp>.csv`입니다.</span><span class="sxs-lookup"><span data-stu-id="059ae-p106">The script starts to collect information about all the eDiscovery cases in your organization. Don't access the report file while the script is running. After the script is complete, a confirmation message is displayed in the Windows PowerShell session. After this message is displayed, you can access the report in the folder that you specified in Step 4. The file name for the report is `CaseHoldsReport<DateTimeStamp>.csv`.</span></span>

    <span data-ttu-id="059ae-p107">addtionally을 사용 하는 경우 스크립트는 보류 된 것이 없는 사례 목록을 포함 하는 보고서도 만듭니다. 이 보고서의 파일 이름은 `CaseswithNoHolds<DateTimeStamp>.csv`입니다.</span><span class="sxs-lookup"><span data-stu-id="059ae-p107">Addtionally, the script also creates a report with a list of cases that don't have any holds. The file name for this report is `CaseswithNoHolds<DateTimeStamp>.csv`.</span></span>
    
    <span data-ttu-id="059ae-141">다음은 CaseHoldsReport 스크립트를 실행 하는 예제입니다.</span><span class="sxs-lookup"><span data-stu-id="059ae-141">Here's an example of running the CaseHoldsReport.ps1 script.</span></span> 
    
    ![CaseHoldsReport 스크립트를 실행 한 후의 출력](media/7d312ed5-505e-4ec5-8f06-3571e3524a1a.png)
  
## <a name="more-information"></a><span data-ttu-id="059ae-143">추가 정보</span><span class="sxs-lookup"><span data-stu-id="059ae-143">More information</span></span>

<span data-ttu-id="059ae-p108">이 문서의 스크립트를 실행할 때 생성 되는 보고서에는 각 보류에 대 한 다음과 같은 정보가 포함 되어 있습니다. 앞에서 설명한 것 처럼, 조직의 모든 보류에 대 한 정보를 반환 하려면 eDiscovery 관리자 여야 합니다. 사례 보존에 대 한 자세한 내용은 [Office 365 보안 &amp; 및 준수 센터에서 eDiscovery 사례](ediscovery-cases.md)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="059ae-p108">The case holds report that's created when you run the script in this article contains the following information about each hold. As previously explained, you have to be an eDiscovery Administrator to return information for all holds in your organization. For more information about case holds, see [eDiscovery cases in the Office 365 Security &amp; Compliance Center](ediscovery-cases.md).</span></span>
  
  - <span data-ttu-id="059ae-147">보류의 이름과 보류가 연결 된 eDiscovery 사례의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="059ae-147">The name of the hold and the name of the eDiscovery case that the hold is associated with.</span></span>
    
  - <span data-ttu-id="059ae-148">eDiscovery 사례가 활성 상태 인지 닫혀 있는지 여부</span><span class="sxs-lookup"><span data-stu-id="059ae-148">Whether or not the eDiscovery case is active or closed.</span></span>
    
  - <span data-ttu-id="059ae-149">보류를 사용 하거나 사용 하지 않도록 설정할지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="059ae-149">Whether or not the hold is enabled or disabled.</span></span>
    
  - <span data-ttu-id="059ae-p109">보류가 연결 된 eDiscovery 사례의 구성원입니다. 사례 구성원은 할당 된 eDiscovery 권한에 따라 사례를 보거나 관리할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="059ae-p109">The members of the eDiscovery case that the hold is associated with. Case members can view or manage a case, depending on the eDiscovery permissions they've been assigned.</span></span>
    
  - <span data-ttu-id="059ae-152">사례를 만든 날짜와 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="059ae-152">The time and date the case was created.</span></span>
    
  - <span data-ttu-id="059ae-153">사례가 닫히면 해당 사례를 닫은 사람 및 종료 된 시간 및 날짜입니다.</span><span class="sxs-lookup"><span data-stu-id="059ae-153">If a case is closed, the person who closed it and the time and date it was closed.</span></span>
    
  - <span data-ttu-id="059ae-154">보류 중인 Exchange 사서함 및 SharePoint 사이트 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="059ae-154">The Exchange mailboxes and SharePoint sites locations that are on hold.</span></span>
    
  - <span data-ttu-id="059ae-155">보류가 쿼리 기반 인 경우 쿼리 구문입니다.</span><span class="sxs-lookup"><span data-stu-id="059ae-155">If the hold is query-based, the query syntax.</span></span>
    
  - <span data-ttu-id="059ae-156">보류가 만들어진 날짜와 시간 및이를 만든 사람입니다.</span><span class="sxs-lookup"><span data-stu-id="059ae-156">The time and date the hold was created and the person who created it.</span></span>
    
  - <span data-ttu-id="059ae-157">보류를 마지막으로 변경한 날짜와 시간을 변경한 사람입니다.</span><span class="sxs-lookup"><span data-stu-id="059ae-157">The time and date the hold was last changed and the person who changed it.</span></span>
