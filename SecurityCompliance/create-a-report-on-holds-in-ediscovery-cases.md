---
title: Office 365의 eDiscovery 사례에서 보류에서 보고서 만들기
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 9/11/2017
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid: MOE150
ms.assetid: cca08d26-6fbf-4b2c-b102-b226e4cd7381
description: 이 문서에서 스크립트를 사용 하 여 Office 365 보안에서 eDiscovery 사례와 연결 된 모든 보류 하는 방법에 대 한 정보가 포함 된 보고서를 생성 하려면 &amp; 준수 센터입니다.
ms.openlocfilehash: b6cef2824002d7e45e4f500bc6c1e9bc880cbd41
ms.sourcegitcommit: 7956955cd919f6e00b64e4506605a743c5872549
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/26/2018
ms.locfileid: "25038211"
---
# <a name="create-a-report-on-holds-in-ediscovery-cases-in-office-365"></a><span data-ttu-id="c4267-103">Office 365의 eDiscovery 사례에서 보류에서 보고서 만들기</span><span class="sxs-lookup"><span data-stu-id="c4267-103">Create a report on holds in eDiscovery cases in Office 365</span></span>
  
<span data-ttu-id="c4267-p101">이 문서의 스크립트 eDiscovery 관리자를 사용 하 고 Office 365 보안에서 eDiscovery 사례와 연결 된 모든 보류 하는 방법에 대 한 정보가 포함 된 보고서를 생성 하는 eDiscovery 관리자 &amp; 준수 센터입니다. 보고서는 경우 보류의 이름을 보류에 배치 되는 콘텐츠 위치와 연결 된 같은 및 쿼리 기반 인지 보류 정보를 포함 합니다. 모든 보류를 설치 하지 않은 경우 경우 스크립트에 보류 없이 사례의 목록을 사용 하 여 추가 보고서를이 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="c4267-p101">The script in this article lets eDiscovery administrators and eDiscovery managers generate a report that contains information about all holds that are associated with eDiscovery cases in the Office 365 Security &amp; Compliance Center. The report contains information such as the name of the case a hold is associated with, the content locations that are placed on hold, and whether the hold is query-based. If there are cases that don't have any holds, the script will create an additional report with a list of cases without holds.</span></span>

<span data-ttu-id="c4267-107">보고서에 포함 되는 정보에 대 한 자세한 설명에 대 한 [자세한 내용](#more-information) 은 섹션을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="c4267-107">See the [More information](#more-information) section for a detailed description of the information included in the report.</span></span> 
  
## <a name="before-you-begin"></a><span data-ttu-id="c4267-108">시작하기 전에</span><span class="sxs-lookup"><span data-stu-id="c4267-108">Before you begin</span></span>

- <span data-ttu-id="c4267-p102">조직에서 모든 eDiscovery 사례에 대 한 보고서를 생성 하려면 조직에서 eDiscovery 관리자를 지정 해야 합니다. EDiscovery 관리자 인 경우 보고서에 액세스할 수 있는 경우에 대 한 정보가 포함 됩니다. EDiscovery 사용 권한에 대 한 자세한 내용은 참조 [Office 365 보안에서 eDiscovery 사용 권한을 할당 &amp; 준수 센터](assign-ediscovery-permissions.md)합니다.</span><span class="sxs-lookup"><span data-stu-id="c4267-p102">To generate a report on all eDiscovery cases in your organization, you have to be an eDiscovery Administrator in your organization. If you are an eDiscovery Manager, the report will only include information about the cases that you can access. For more information about eDiscovery permissions, see [Assign eDiscovery permissions in the Office‍ 365 Security &amp; Compliance Center](assign-ediscovery-permissions.md).</span></span>
    
- <span data-ttu-id="c4267-p103">이 문서의 스크립트는 최소한의 오류 처리 합니다. 주요 목적은 신속 하 게 조직에서 eDiscovery 사례와 연결 된 보류에 대 한 보고서를 만드는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="c4267-p103">The script in this article has minimal error handling. The primary purpose is to quickly create report about the holds that are associated with the eDiscovery cases in your organization.</span></span>
    
- <span data-ttu-id="c4267-p104">이 항목에서 제공된 샘플 스크립트는 Microsoft 표준 지원 프로그램 또는 서비스에서는 지원되지 않습니다. 샘플 스크립트는 어떠한 보증도 없이 "있는 그대로" 제공됩니다. Microsoft는 묵시적인 모든 보증(상품성 또는 특정 목적에의 적합성에 대한 묵시적인 보증을 포함하되 이에 제한되지 않음)을 부인합니다. 샘플 스크립트 및 문서의 사용 또는 수행으로 인해 발생하는 모든 위험은 사용자의 책임입니다. 어떠한 경우에도 Microsoft, 스크립트 작성자 또는 스크립트의 작성, 생산 또는 제공과 관련된 사람은 누구나 샘플 스크립트 또는 문서의 사용 또는 사용 불가능으로 인해 발생하는 모든 손해(수익에 대한 손실, 비즈니스 중단, 비즈니스 정보 손실 또는 기타 금전상의 손실을 포함하되 이에 제한되지 않음)에 대해 책임지지 않습니다. 이는 Microsoft가 이러한 손해가 발생할 가능성에 대해 알고 있었더라고 마찬가지입니다.</span><span class="sxs-lookup"><span data-stu-id="c4267-p104">The sample scripts provided in this topic aren't supported under any Microsoft standard support program or service. The sample scripts are provided AS IS without warranty of any kind. Microsoft further disclaims all implied warranties including, without limitation, any implied warranties of merchantability or of fitness for a particular purpose. The entire risk arising out of the use or performance of the sample scripts and documentation remains with you. In no event shall Microsoft, its authors, or anyone else involved in the creation, production, or delivery of the scripts be liable for any damages whatsoever (including, without limitation, damages for loss of business profits, business interruption, loss of business information, or other pecuniary loss) arising out of the use of or inability to use the sample scripts or documentation, even if Microsoft has been advised of the possibility of such damages.</span></span>
    
## <a name="step-1-connect-to-the-security-amp-compliance-center-using-remote-powershell"></a><span data-ttu-id="c4267-119">1 단계: 보안 연결할 &amp; 원격 PowerShell을 사용 하 여 준수 센터</span><span class="sxs-lookup"><span data-stu-id="c4267-119">Step 1: Connect to the Security &amp; Compliance Center using Remote PowerShell</span></span>

<span data-ttu-id="c4267-120">보안에 Windows PowerShell을 연결 하는 첫번째 단계는 &amp; 조직에 대 한 준수 센터입니다.</span><span class="sxs-lookup"><span data-stu-id="c4267-120">The first step is to connect Windows PowerShell to the Security &amp; Compliance Center for your organization.</span></span>
  
1. <span data-ttu-id="c4267-121">.Ps1 파일 이름 접미사를 사용 하 여 Windows PowerShell 스크립트 파일에 다음 텍스트를 저장 예, `ConnectSCC.ps1`합니다.</span><span class="sxs-lookup"><span data-stu-id="c4267-121">Save the following text to a Windows PowerShell script file by using a filename suffix of .ps1; for example, `ConnectSCC.ps1`.</span></span> 
    
      ```
      # Get login credentials 
      $UserCredential = Get-Credential 
      $Session = New-PSSession -ConfigurationName Microsoft.Exchange -ConnectionUri https://ps.compliance.protection.outlook.com/powershell-liveid -Credential $UserCredential -Authentication Basic -AllowRedirection 
      Import-PSSession $Session -AllowClobber -DisableNameChecking 
      $Host.UI.RawUI.WindowTitle = $UserCredential.UserName + " (Office 365 Security &amp; Compliance Center)" 
    ```

2. <span data-ttu-id="c4267-122">로컬 컴퓨터에서 Windows PowerShell 열고 스크립트를 저장 한 폴더로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="c4267-122">On your local computer, open Windows PowerShell and go to the folder where you saved the script.</span></span> 
    
3. <span data-ttu-id="c4267-123">스크립트를 실행 합니다. 예를 들어:</span><span class="sxs-lookup"><span data-stu-id="c4267-123">Run the script; for example:</span></span>

    ```
    .\ConnectSCC.ps1
    ```
   
4. <span data-ttu-id="c4267-124">사용자의 자격 증명에 대 한 대화 상자가 나타나면 전자 메일 주소와 암호를 입력 한 다음 **확인**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="c4267-124">When prompted for your credentials, enter your email address and password, and then click **OK**.</span></span> 
  
## <a name="step-2-run-the-script-to-report-on-holds-associated-with-ediscovery-cases"></a><span data-ttu-id="c4267-125">2 단계:를 실행 하는 스크립트에 대해 보고를 포함 하 고 eDiscovery 사례와 연결</span><span class="sxs-lookup"><span data-stu-id="c4267-125">Step 2: Run the script to report on holds associated with eDiscovery cases</span></span>

<span data-ttu-id="c4267-126">보안에 연결한 후 &amp; 원격 PowerShell 사용한 준수 센터, 다음 단계에서는를 만들고 조직에서 eDiscovery 사례에 대 한 정보를 수집 하는 스크립트를 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="c4267-126">After you've connected to the Security &amp; Compliance Center with remote PowerShell, the next step is to create and run the script that collects information about the eDiscovery cases in your organization.</span></span> 
  
1. <span data-ttu-id="c4267-127">.Ps1 파일 이름 접미사를 사용 하 여 Windows PowerShell 스크립트 파일에 다음 텍스트를 저장 예: CaseHoldsReport.ps1 합니다.</span><span class="sxs-lookup"><span data-stu-id="c4267-127">Save the following text to a Windows PowerShell script file by using a filename suffix of .ps1; for example, CaseHoldsReport.ps1.</span></span> 
    
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

2. <span data-ttu-id="c4267-128">1 단계에서에서 연 Windows PowerShell 세션에서 스크립트를 저장 한 위치로 폴더로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="c4267-128">In the Windows PowerShell session that opened in Step 1, go to the folder where you saved the script.</span></span> 
    
3. <span data-ttu-id="c4267-129">스크립트를 실행 합니다. 예를 들어:</span><span class="sxs-lookup"><span data-stu-id="c4267-129">Run the script; for example:</span></span>

    ```
    .\CaseHoldsReport.ps1
    ```

    <span data-ttu-id="c4267-130">스크립트는 보고서를 저장 하려면 대상 폴더에 대 한 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="c4267-130">The script will prompt for a target folder to save the report to.</span></span> 
    
4. <span data-ttu-id="c4267-131">보고서를 저장할 폴더의 전체 경로 이름을 입력 하 고 **Enter**키를 누릅니다.</span><span class="sxs-lookup"><span data-stu-id="c4267-131">Type the full path name of the folder to save the report to, and then press **Enter**.</span></span>
    
    > [!TIP]
    > <span data-ttu-id="c4267-p105">스크립트에 있는 같은 폴더에 보고서를 저장 하려면 마침표 (".") 대상 폴더에 대 한 대화 상자가 나타나면 합니다. 스크립트가 있는 폴더에 있는 하위 폴더에서 보고서를 저장 하려면 하위 폴더의 이름을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="c4267-p105">To save the report in the same folder that the script is located in, type a period (".") when prompted for a target folder. To save the report in a subfolder in the folder where the script is located, just type the name of the subfolder.</span></span> 
  
    <span data-ttu-id="c4267-p106">조직에서 모든 eDiscovery 사례에 대 한 정보를 수집 하는 스크립트를 시작 합니다. 스크립트 실행 되는 동안 보고서 파일에 액세스 하지 마십시오. 스크립트가 완료 되 면 Windows PowerShell 세션에 확인 메시지가 표시 됩니다. 이 메시지가 표시 되 면 4 단계에서에서 지정한 폴더에서 보고서를 액세스할 수 있습니다. 다음은 보고서에 대 한 파일 이름은 `CaseHoldsReport<DateTimeStamp>.csv`합니다.</span><span class="sxs-lookup"><span data-stu-id="c4267-p106">The script starts to collect information about all the eDiscovery cases in your organization. Don't access the report file while the script is running. After the script is complete, a confirmation message is displayed in the Windows PowerShell session. After this message is displayed, you can access the report in the folder that you specified in Step 4. The file name for the report is `CaseHoldsReport<DateTimeStamp>.csv`.</span></span>

    <span data-ttu-id="c4267-p107">Addtionally, 스크립트는 또한 보고서의 모든 보류를 설치 하지 않은 경우 목록을 만듭니다. 이 보고서에 대 한 파일 이름은 `CaseswithNoHolds<DateTimeStamp>.csv`합니다.</span><span class="sxs-lookup"><span data-stu-id="c4267-p107">Addtionally, the script also creates a report with a list of cases that don't have any holds. The file name for this report is `CaseswithNoHolds<DateTimeStamp>.csv`.</span></span>
    
    <span data-ttu-id="c4267-141">다음은 CaseHoldsReport.ps1 스크립트를 실행 하는 예제입니다.</span><span class="sxs-lookup"><span data-stu-id="c4267-141">Here's an example of running the CaseHoldsReport.ps1 script.</span></span> 
    
    ![CaseHoldsReport.ps1 스크립트를 실행 한 후 출력](media/7d312ed5-505e-4ec5-8f06-3571e3524a1a.png)
  
## <a name="more-information"></a><span data-ttu-id="c4267-143">추가 정보</span><span class="sxs-lookup"><span data-stu-id="c4267-143">More information</span></span>

<span data-ttu-id="c4267-p108">대/소문자 각 대기 하는 방법에 대 한 다음 정보를 포함 하는이 문서에서 스크립트를 실행할 때 생성 되는 보고서를 포함 합니다. 앞에서 설명한 것 처럼 eDiscovery 관리자가 조직에서 모든 보류에 대 한 정보를 반환할 수 해야 합니다. 대/소문자에 대 한 자세한 내용은 보유 하 고 참조 [Office 365 보안에서 eDiscovery 사례 &amp; 준수 센터](ediscovery-cases.md)합니다.</span><span class="sxs-lookup"><span data-stu-id="c4267-p108">The case holds report that's created when you run the script in this article contains the following information about each hold. As previously explained, you have to be an eDiscovery Administrator to return information for all holds in your organization. For more information about case holds, see [eDiscovery cases in the Office 365 Security &amp; Compliance Center](ediscovery-cases.md).</span></span>
  
  - <span data-ttu-id="c4267-147">보류 및 eDiscovery 사례의 보류 연관 된 이름의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c4267-147">The name of the hold and the name of the eDiscovery case that the hold is associated with.</span></span>
    
  - <span data-ttu-id="c4267-148">EDiscovery 사례 인지 여부 활성화 또는 종료 합니다.</span><span class="sxs-lookup"><span data-stu-id="c4267-148">Whether or not the eDiscovery case is active or closed.</span></span>
    
  - <span data-ttu-id="c4267-149">여부 보류 사용 하거나 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c4267-149">Whether or not the hold is enabled or disabled.</span></span>
    
  - <span data-ttu-id="c4267-p109">보류 연관 된 eDiscovery 사례의 구성원입니다. 사례 구성원 보거나 할당 했을 때 eDiscovery 사용 권한에 따라 사례를 관리할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c4267-p109">The members of the eDiscovery case that the hold is associated with. Case members can view or manage a case, depending on the eDiscovery permissions they've been assigned.</span></span>
    
  - <span data-ttu-id="c4267-152">대/소문자를 만든 날짜와 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="c4267-152">The time and date the case was created.</span></span>
    
  - <span data-ttu-id="c4267-153">사례 닫혀 있으면 없으며 시간 닫히고 날짜 사람이 닫았습니다.</span><span class="sxs-lookup"><span data-stu-id="c4267-153">If a case is closed, the person who closed it and the time and date it was closed.</span></span>
    
  - <span data-ttu-id="c4267-154">Exchange 사서함 및 SharePoint 사이트 대기 수 있는 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="c4267-154">The Exchange mailboxes and SharePoint sites locations that are on hold.</span></span>
    
  - <span data-ttu-id="c4267-155">보류는 쿼리를 기반으로 하는 경우 쿼리 구문입니다.</span><span class="sxs-lookup"><span data-stu-id="c4267-155">If the hold is query-based, the query syntax.</span></span>
    
  - <span data-ttu-id="c4267-156">시간 및 보류를 만든 날짜 및 만든 사람입니다.</span><span class="sxs-lookup"><span data-stu-id="c4267-156">The time and date the hold was created and the person who created it.</span></span>
    
  - <span data-ttu-id="c4267-157">시간 및 보류를 마지막으로 변경한 날짜 및 사용자가 변경한 상태로입니다.</span><span class="sxs-lookup"><span data-stu-id="c4267-157">The time and date the hold was last changed and the person who changed it.</span></span>
