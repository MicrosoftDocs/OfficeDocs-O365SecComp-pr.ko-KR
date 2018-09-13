---
title: PowerShell을 사용하여 레이블 대량 생성 및 게시
ms.author: stephow
author: stephow-msft
ms.date: 1/17/2018
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Priority
search.appverid:
- MOE150
- MET150
ms.assetid: 8986701b-ffa1-46ec-8fd0-8f7e81d5b25f
description: Office 365에서 레이블을 사용하여 조직의 보존 일정을 구현할 수 있습니다. 레코드 관리자 또는 준수 담당자는 수백 개의 레이블을 만들고 게시해야 할 수 있습니다. 보안 및 준수 센터에서 UI를 통해 이 작업을 수행할 수 있지만, 한 번에 하나씩 레이블을 만드는 경우 시간이 오래 걸리고 비효율적입니다. 아래에 제공된 스크립트와 .csv 파일을 사용하면 레이블 및 레이블 정책을 대량으로 만들고 게시할 수 있습니다. 먼저 Excel에서 레이블 목록과 레이블 정책 목록을 만든 다음, PowerShell을 사용하여 해당 목록에 레이블과 레이블 정책을 대량으로 만듭니다. 이렇게 하면 보존 일정에 필요한 모든 레이블을 한 번에 더 쉽게 만들고 게시할 수 있습니다.
ms.openlocfilehash: 43e521d937a9589b522c608aca2e75fcfc2bf569
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22532997"
---
# <a name="bulk-create-and-publish-labels-by-using-powershell"></a><span data-ttu-id="0383a-108">PowerShell을 사용하여 레이블 대량 생성 및 게시</span><span class="sxs-lookup"><span data-stu-id="0383a-108">Bulk create and publish labels by using PowerShell</span></span>

<span data-ttu-id="0383a-p102">Office 365에서 레이블을 사용하여 조직의 보존 일정을 구현할 수 있습니다. 레코드 관리자 또는 준수 담당자는 수백 개의 레이블을 만들고 게시해야 할 수 있습니다. 보안 및 준수 센터에서 UI를 통해 이 작업을 수행할 수 있지만, 한 번에 하나씩 레이블을 만드는 경우 시간이 오래 걸리고 비효율적입니다.</span><span class="sxs-lookup"><span data-stu-id="0383a-p102">In Office 365, you can use labels to implement a retention schedule for your organization. As a record manager or compliance officer, you might have hundreds of labels to create and publish. You can do this through the UI in the Security &amp; Compliance Center, but creating labels one at a time is time-consuming and inefficient.</span></span>
  
<span data-ttu-id="0383a-p103">아래에 제공된 스크립트와 .csv 파일을 사용하면 레이블 및 레이블 정책을 대량으로 만들고 게시할 수 있습니다. 먼저 Excel에서 레이블 목록과 레이블 정책 목록을 만든 다음, PowerShell을 사용하여 해당 목록에 레이블과 레이블 정책을 대량으로 만듭니다. 이렇게 하면 보존 일정에 필요한 모든 레이블을 한 번에 더 쉽게 만들고 게시할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0383a-p103">By using the script and .csv files provided below, you can bulk create and publish labels and label policies. First you create a list of the labels and a list of the label policies in Excel, and then you bulk create the labels and label policies in those lists by using PowerShell. This makes it easier to create and publish at one time all of the labels that your retention schedule requires.</span></span>
  
<span data-ttu-id="0383a-115">레이블에 대한 자세한 내용은 [레이블 개요](labels.md)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="0383a-115">For more information about labels, see [Overview of labels in Office 365](labels.md).</span></span>
  
## <a name="disclaimer"></a><span data-ttu-id="0383a-116">고지 사항</span><span class="sxs-lookup"><span data-stu-id="0383a-116">Disclaimer</span></span>

<span data-ttu-id="0383a-p104">이 항목에서 제공된 샘플 스크립트는 Microsoft 표준 지원 프로그램 또는 서비스에서는 지원되지 않습니다. 샘플 스크립트는 어떠한 보증도 없이 "있는 그대로" 제공됩니다. Microsoft는 묵시적인 모든 보증(상품성 또는 특정 목적에의 적합성에 대한 묵시적인 보증을 포함하되 이에 제한되지 않음)을 부인합니다. 샘플 스크립트 및 문서의 사용 또는 수행으로 인해 발생하는 모든 위험은 사용자의 책임입니다. 어떠한 경우에도 Microsoft, 스크립트 작성자 또는 스크립트의 작성, 생산 또는 제공과 관련된 사람은 누구나 샘플 스크립트 또는 문서의 사용 또는 사용 불가능으로 인해 발생하는 모든 손해(수익에 대한 손실, 비즈니스 중단, 비즈니스 정보 손실 또는 기타 금전상의 손실을 포함하되 이에 제한되지 않음)에 대해 책임지지 않습니다. 이는 Microsoft가 이러한 손해가 발생할 가능성에 대해 알고 있었더라고 마찬가지입니다.</span><span class="sxs-lookup"><span data-stu-id="0383a-p104">The sample scripts provided in this topic aren’t supported under any Microsoft standard support program or service. The sample scripts are provided AS IS without warranty of any kind. Microsoft further disclaims all implied warranties including, without limitation, any implied warranties of merchantability or of fitness for a particular purpose. The entire risk arising out of the use or performance of the sample scripts and documentation remains with you. In no event shall Microsoft, its authors, or anyone else involved in the creation, production, or delivery of the scripts be liable for any damages whatsoever (including, without limitation, damages for loss of business profits, business interruption, loss of business information, or other pecuniary loss) arising out of the use of or inability to use the sample scripts or documentation, even if Microsoft has been advised of the possibility of such damages.</span></span>
  
## <a name="step-1-create-a-csv-file-for-creating-the-labels"></a><span data-ttu-id="0383a-122">1단계: 레이블을 만들기 위한 .csv 파일 만들기</span><span class="sxs-lookup"><span data-stu-id="0383a-122">Step 1: Create a .csv file for creating the labels</span></span>

<span data-ttu-id="0383a-p105">먼저 레이블 목록과 해당 보존 설정이 포함된 .csv 파일을 만듭니다. 아래 샘플을 Excel에 복사하고 텍스트를 열로 변환(Excel \> **데이터** 탭 \> **텍스트 나누기** \> **구분** \> **쉼표** \> **일반**)한 다음 워크시트를 찾기 쉬운 위치에 .csv 파일로 저장하면 이 샘플을 서식 파일로 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0383a-p105">First you create a .csv file that contains a list of your labels with their retention settings. You can use the sample below as a template by copying it into Excel, converting the text to columns (in Excel \> **Data** tab \> **Text to Columns** \> **Delimited** \> **Comma** \> **General**), and then saving the worksheet as a .csv file in a location that's easy to find.</span></span>
  
<span data-ttu-id="0383a-125">이 cmdlet의 매개 변수 값에 대한 자세한 내용은 [New-ComplianceTag](https://go.microsoft.com/fwlink/?linkid=866511)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="0383a-125">For more information about the parameter values for this cmdlet, see [New-ComplianceTag](https://go.microsoft.com/fwlink/?linkid=866511).</span></span>
  
<span data-ttu-id="0383a-126">참고:</span><span class="sxs-lookup"><span data-stu-id="0383a-126">Notes:</span></span>
  
- <span data-ttu-id="0383a-127">레이블을 만들기 위한 원본 파일을 제공하지 않으면 스크립트가 그대로 진행하여 레이블을 게시하기 위한 원본 파일을 묻는 메시지를 표시하고(다음 섹션 참조) 기존 레이블만 게시합니다.</span><span class="sxs-lookup"><span data-stu-id="0383a-127">If you don't provide a source file for creating labels, the script moves on and prompts you for the source file for publishing labels (see the next section), and the script will publish only existing labels.</span></span>
    
- <span data-ttu-id="0383a-p106">이미 존재하는 레이블과 동일한 이름을 가진 레이블이 .csv 파일에 있을 경우 스크립트에서 해당 레이블 생성을 건너뜁니다. 중복 레이블은 생성되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0383a-p106">If the .csv file contains a label with the same name as one that already exists, the script skips creating that label. No duplicate labels are created.</span></span>
    
- <span data-ttu-id="0383a-p107">열 머리글을 변경하거나 이름을 바꾸면 스크립트가 실패합니다. 여기에 제공된 형식의 .csv 파일이 스크립트에 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="0383a-p107">If you change or rename the column headers, the script will fail. The script requires a .csv file in the format provided here.</span></span>
    
### <a name="sample-csv-file"></a><span data-ttu-id="0383a-132">샘플 .csv 파일</span><span class="sxs-lookup"><span data-stu-id="0383a-132">Sample .csv file</span></span>

```
Name (Required),Comment (Optional),IsRecordLabel (Required),RetentionAction (Optional),RetentionDuration (Optional),RetentionType (Optional),ReviewerEmail (Optional)
LabelName_t_1,Record - keep and delete - 2 years,$true,KeepAndDelete,730,CreationAgeInDays,
LabelName_t_2,Keep and delete tag - 7 years,$false,KeepAndDelete,2555,ModificationAgeInDays,
LabelName_t_3,5 year delete,$false,Delete,1825,TaggedAgeInDays,
LabelName_t_4,Record label tag - financial,$true,Keep,730,CreationAgeInDays,
```

## <a name="step-2-create-a-csv-file-for-publishing-the-labels"></a><span data-ttu-id="0383a-133">레이블을 게시하기 위한 .csv 파일 만들기</span><span class="sxs-lookup"><span data-stu-id="0383a-133">Step 2: Create a .csv file for publishing the labels</span></span>

<span data-ttu-id="0383a-p108">레이블 정책 목록과 해당 위치 및 기타 설정이 포함된 .csv 파일을 만듭니다. 아래 샘플을 Excel에 복사하고 텍스트를 열로 변환(Excel \> **데이터** 탭 \> **텍스트 나누기** \> **구분** \> **쉼표** \> **일반**)한 다음 워크시트를 찾기 쉬운 위치에 .csv 파일로 저장하면 이 샘플을 서식 파일로 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0383a-p108">Next you create a .csv file that contains a list of label policies with their locations and other settings. You can use the sample below as a template by copying it into Excel, converting the text to columns (in Excel \> **Data** tab \> **Text to Columns** \> **Delimited** \> **Comma** \> **General**), and then saving the worksheet as a .csv file in a location that's easy to find.</span></span>
  
<span data-ttu-id="0383a-136">이 cmdlet의 매개 변수 값에 대한 자세한 내용은 [New-RetentionCompliancePolicy](https://go.microsoft.com/fwlink/?linkid=866512)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="0383a-136">For more information about the parameter values for this cmdlet, see [New-RetentionCompliancePolicy](https://go.microsoft.com/fwlink/?linkid=866512).</span></span>
  
<span data-ttu-id="0383a-137">참고:</span><span class="sxs-lookup"><span data-stu-id="0383a-137">Notes:</span></span>
  
- <span data-ttu-id="0383a-138">레이블을 게시하기 위한 원본 파일을 제공하지 않으면 스크립트에서 레이블을 만들지만(이전 섹션 참조) 게시하지는 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0383a-138">If you don't provide a source file for publishing labels, the script creates labels (see the previous section) but does not publish them.</span></span>
    
- <span data-ttu-id="0383a-p109">이미 존재하는 레이블 정책과 동일한 이름을 가진 레이블 정책이 .csv 파일에 있을 경우 스크립트에서 해당 레이블 정책 생성을 건너뜁니다. 중복 레이블 정책은 생성되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0383a-p109">If the .csv file contains a label policy with the same name as one that already exists, the script skips creating that label policy. No duplicate label policies are created.</span></span>
    
- <span data-ttu-id="0383a-p110">스크립트는 수동으로 콘텐츠에 적용된 레이블만 게시합니다. 이 스크립트는 콘텐츠에 자동 적용된 레이블을 지원하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0383a-p110">The script publishes only labels that are applied manually to content. This script does not support labels that are auto-applied to content.</span></span>
    
- <span data-ttu-id="0383a-p111">열 머리글을 변경하거나 이름을 바꾸면 스크립트가 실패합니다. 여기에 제공된 형식의 .csv 파일이 스크립트에 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="0383a-p111">If you change or rename the column headers, the script will fail. The script requires a .csv file in the format provided here.</span></span>
    
### <a name="sample-csv-file"></a><span data-ttu-id="0383a-145">샘플 .csv 파일</span><span class="sxs-lookup"><span data-stu-id="0383a-145">Sample .csv file</span></span>

```
Policy Name (Required),PublishComplianceTag (Required),Comment (Optional),Enabled (Required),ExchangeLocation (Optional),ExchangeLocationException (Optional),ModernGroupLocation (Optional),ModernGroupLocationException (Optional),OneDriveLocation (Optional),OneDriveLocationException (Optional),PublicFolderLocation (Optional),SharePointLocation (Optional),SharePointLocationException (Optional),SkypeLocation (Optional),SkypeLocationException (Optional)
Publishing Policy Red1,"LabelName_t_1, LabelName_t_2, LabelName_t_3, LabelName_t_4",N/A,$true,All,,All,,All,,,All,,,
Publishing Policy Orange1,"LabelName_t_1, LabelName_t_2",N/A,$true,All,,,,,,,,,,
Publishing Policy Yellow1,"LabelName_t_3, LabelName_t_4",N/A,$false,,,,,,,,,,,
```

## <a name="step-3-create-the-powershell-script"></a><span data-ttu-id="0383a-146">3단계: PowerShell 스크립트 만들기</span><span class="sxs-lookup"><span data-stu-id="0383a-146">Step 3: Create the PowerShell script</span></span>

<span data-ttu-id="0383a-p112">아래 PowerShell 스크립트를 복사하여 메모장에 붙여넣습니다. 파일 이름 접미사 .ps1을 사용하여 찾기 쉬운 위치에 파일을 저장합니다(예: \<경로\>CreateRetentionSchedule.ps1).</span><span class="sxs-lookup"><span data-stu-id="0383a-p112">Copy and paste the below PowerShell script into Notepad. Save the file by using a filename suffix of .ps1 in a location that's easy to find -- for example, \<path\>CreateRetentionSchedule.ps1.</span></span>
  
### <a name="powershell-script"></a><span data-ttu-id="0383a-149">PowerShell 스크립트</span><span class="sxs-lookup"><span data-stu-id="0383a-149">Windows PowerShell script helper</span></span>

```
<#
. Steps: Import and Publish Compliance Tag
    ○ Load compliance tag csv file 
    ○ Validate csv file input
    ○ Create compliance tag
    ○ Create compliance policy
    ○ Publish compliance tag for the policy
    ○ Generate the log for tags creation
    ○ Generate the csv result for the tags created and published
. Syntax
    .\Publish-ComplianceTag.ps1 [-LabelListCSV <string>] [-PolicyListCSV <string>] 
. Detailed Description
    1) [-LabelListCSV <string>]
    -LabelListCSV ".\SampleInputFile_LabelList.csv"
    Load compliance tag for creation.
    2) [-PolicyListCSV <string>]
    -PolicyListCSV ".\SampleInputFile_PolicyList.csv"
    Load compliance tag for creation.
#>
param (
    [Parameter(Mandatory = $true)]
    [string]$LabelListCSV = "",
    [Parameter(Mandatory = $true)]
    [string]$PolicyListCSV = "",
    [Switch]$ResultCSV
)
# -------------------
# File operation
# -------------------
Function FileExist
{
    Param(
        # File path needed to check
        [Parameter(Mandatory = $true)]
        [String]$FilePath,
        [Switch]$Warning
    )
    $inputFileExist = Test-Path $FilePath
    if (!$inputFileExist)
    {
        if ($Warning -eq $false) 
        { 
            WriteToLog -Type "Failed" -Message "[File: $FilePath] The file doesn't exist"
            throw 
        }
        else 
        { 
            WriteToLog -Type "Warning" -Message "[File: $FilePath] The file doesn't exist"
        }
    }
    else
    {
        WriteToLog -Type "Succeed" -Message "[File: $FilePath] The file is found"
    }
}
# -------------------
# Log operation
# -------------------
Function WriteToLog
{
    Param(
        # Message want to write to log file
        [Parameter(Mandatory = $true)]
        [String]$Message,
        # "Succeed" or "Faild"
        [String]$Type = "Message"
    )
    $date = Get-Date -Format 'HH:mm:ss'
    $logInfo = $date + " - [$Type] " + $Message
    $logInfo | Out-File -FilePath $logfilePath -Append
    if ($Type -eq "Succeed") { Write-Host $logInfo -ForegroundColor Green }
    elseif ($Type -eq "Failed") { Write-Host $logInfo -ForegroundColor Red }
    elseif ($Type -eq "Warning") { Write-Host $logInfo -ForegroundColor Yellow }
    elseif ($Type -eq "Start") { Write-Host $logInfo -ForegroundColor Cyan }
    else { Write-Verbose $logInfo }
}
Function Create-Log
{
    Param(
        # Log folder Root
        [Parameter(Mandatory = $true)]
        [String]$LogFolderRoot,
        # The function Log file for
        [Parameter(Mandatory = $true)]
        [String]$LogFunction
    )
    $logFolderPath = "$LogFolderRoot\logfiles"
    $folderExist = Test-Path "$logFolderPath"
    if (!$folderExist)
    {
        $folder = New-Item "$logFolderPath" -type directory
    }
    $date = Get-Date -Format 'MMddyyyy_HHmmss'
    $logfilePath = "$logFolderPath\Log_{0}_{1}.txt" -f $LogFunction, $date
    Write-Verbose "Log file is writen to: $logfilePath"
    $logfile = New-Item $logfilePath  -type file
    return $logfilePath
}
Function Create-ResultCSV
{
    Param(
        # Result folder Root
        [Parameter(Mandatory = $true)]
        [String]$ResultFolderRoot,
        # The function Result file for
        [Parameter(Mandatory = $true)]
        [String]$ResultFunction
    )
    $retFolderPath = "$ResultFolderRoot\logfiles"
    $folderExist = Test-Path "$retFolderPath"
    if (!$folderExist)
    {
        $folder = New-Item "$retFolderPath" -type directory
    }
    $date = Get-Date -Format 'MMddyyyy_HHmmss'
    $retfilePath = "$retFolderPath\Result_{0}_{1}.csv" -f $ResultFunction, $date
    Write-Verbose "Result file is writen to: $retfilePath"
    $retfile = New-Item $retfilePath  -type file
    return $retfilePath
}
# -------------------
# Prepare Log File
# -------------------
$scriptPath = '.\'
$logfilePath = Create-Log -LogFolderRoot $scriptPath -LogFunction "Publish_Compliance_Tag"
if ($ResultCSV)
{
    $tagRetFile = Create-ResultCSV -ResultFolderRoot $scriptPath -ResultFunction "Tag_Creation"
    $tagPubRetFile = Create-ResultCSV -ResultFolderRoot $scriptPath -ResultFunction "Tag_Publish"
}
# -------------------
# Invoke Powershell cmdlet
# -------------------
Function InvokePowerShellCmdlet
{
    Param(
        [Parameter(Mandatory = $true)]
        [String]$CmdLet
    )
    try
    {
        WriteToLog -Type "Start" -Message "Execute Cmdlet : '$CmdLet'" 
        return Invoke-Expression $CmdLet -ErrorAction SilentlyContinue
    }
    catch
    {
        WriteToLog -Type "Failed" "Failed to execute cmdlet!"
        WriteToLog -Type "Failed" $error[0]
        return $null
    }
}
# -------------------
# Create Compliance Tag
# -------------------
Function CreateComplianceTag
{
    Param(
        # File path needed to check
        [Parameter(Mandatory = $true)]
        [String]$FilePath
    )
    
    WriteToLog -Type "Start" "Start to create Compliance Tag"
    FileExist $FilePath
    
    # TODO Validate CSV file for the Header
    try
    {
        # Import csv
        $labels = Import-Csv $FilePath
        # Retrieve existing compliance tags
        $tags = InvokePowerShellCmdlet "Get-ComplianceTag"
        foreach($lab in $labels)
        {
            # Cmdlet parameters
            $para = [String]::Empty;
            $name = [String]::Empty;
            $cmdlet = 'New-ComplianceTag'
            if ([String]::IsNullOrEmpty($lab.'Name (Required)'))
            {
                WriteToLog -Type "Failed" -Message "Could not acquire table for writing."
                throw;
            }
            else
            {
                $name = $lab.'Name (Required)'
                $cmdlet += " -Name '" + $name + "'"
            }
            if (![String]::IsNullOrEmpty($lab.'Comment (Optional)'))
            {
                $para = $lab.'Comment (Optional)'
                $cmdlet += " -Comment '" + $para + "'"
            }
            if (![String]::IsNullOrEmpty($lab.'IsRecordLabel (Required)'))
            {
                $para = $lab.'IsRecordLabel (Required)'
                $cmdlet += " -IsRecordLabel " + $para
            }
            if (![String]::IsNullOrEmpty($lab.'RetentionAction (Optional)'))
            {
                $para = $lab.'RetentionAction (Optional)'
                $cmdlet += " -RetentionAction " + $para 
            }
            if (![String]::IsNullOrEmpty($lab.'RetentionDuration (Optional)'))
            {
                $para = $lab.'RetentionDuration (Optional)'
                $cmdlet += " -RetentionDuration " + $para
            }
            if (![String]::IsNullOrEmpty($lab.'RetentionType (Optional)'))
            {
                $para = $lab.'RetentionType (Optional)'
                $cmdlet += " -RetentionType " + $para
            }
            if (![String]::IsNullOrEmpty($lab.'ReviewerEmail (Optional)'))
            {
                $emails = $lab.'ReviewerEmail (Optional)'.Split(",") | ForEach-Object { $_.Trim() }
                if (($emails -ne $null) -and ($emails.Count -ne 0))
                {
                    $eml = '@('
                    foreach($email in $emails)
                    {
                        $eml += "'{0}'," -f $email
                    }
                    $eml = $eml.Substring(0, $eml.Length - 1) + ')'
                    
                    $cmdlet += " -ReviewerEmail " + $eml
                }
            }
            # If the tag already exists, skip for creation
            if (($tags -eq $null) -or ($tags | ? { $_.Name.ToLower() -eq $name.ToLower() }) -eq $null)
            {
                # Create compliance tag
                $msg = "Execute Cmdlet : {0}" -f $cmdlet
                
                $ret = InvokePowerShellCmdlet $cmdlet
            
                if ($ret -eq $null)
                {
                    WriteToLog -Type "Failed" $error[0]
                    break;
                }
            }
            else
            {
                WriteToLog -Type "Warning" -Message "The tag '$name' already exists! Skip for creation!"
            }
        }
    }
    catch
    {
        WriteToLog -Type "Failed" "Error in input"
    }
}
# -------------------
# Create Retention Compliance Policy
# -------------------
Function CreateRetentionCompliancePolicy
{
    Param(
        # File path needed to check
        [Parameter(Mandatory = $true)]
        [String]$FilePath
    )
    
    WriteToLog -Type "Start" "Start to Create Retention Policy"
    FileExist $FilePath
    try
    {
        # Import csv
        $list = Import-Csv -Path $FilePath
        # Retrieve existing retention compliance policy
        $policies = InvokePowerShellCmdlet "Get-RetentionCompliancePolicy"
        foreach($rp in $list)
        {
            # Cmdlet parameters
            $para = [String]::Empty;
            $name = [String]::Empty;
            $rpid = [String]::Empty;
            $cmdlet = 'New-RetentionCompliancePolicy'
            if ([String]::IsNullOrEmpty($rp.'Policy Name (Required)'))
            {
                WriteToLog -Type "Failed" -Message "Could not acquire table for writing."
                throw;
            }
            else
            {
               $name = $rp.'Policy Name (Required)'
               $cmdlet += " -Name '" + $name + "'"
            }
            if ([String]::IsNullOrEmpty($rp.'Enabled (Required)'))
            {
                WriteToLog -Type "Failed" -Message "Could not acquire table for writing."
                throw;
            }
            else
            {
                $enabled = $rp.'Enabled (Required)'
                $cmdlet += " -Enabled " + $enabled
            }
            if (![String]::IsNullOrEmpty($rp.'ExchangeLocation (Optional)'))
            {
                $para = $rp.'ExchangeLocation (Optional)'
                $cmdlet += " -ExchangeLocation " + $para
            }
         
            if (![String]::IsNullOrEmpty($rp.'ExchangeLocationException (Optional)'))
            {
                $para = $rp.'ExchangeLocationException (Optional)'
                $cmdlet += " -ExchangeLocationException " + $para
            }
            if (![String]::IsNullOrEmpty($rp.'ModernGroupLocation (Optional)'))
            {
                $para = $rp.'ModernGroupLocation (Optional)'
                $cmdlet += " -ModernGroupLocation " + $para
            }
            if (![String]::IsNullOrEmpty($rp.'ModernGroupLocationException (Optional)'))
            {
                $para = $rp.'ModernGroupLocationException (Optional)'
                $cmdlet += " -ModernGroupLocationException " + $para
            }
            if (![String]::IsNullOrEmpty($rp.'OneDriveLocation (Optional)'))
            {
                $para = $rp.'OneDriveLocation (Optional)'
                $cmdlet += " -OneDriveLocation " + $para
            }
            if (![String]::IsNullOrEmpty($rp.'OneDriveLocationException (Optional)'))
            {
                $para = $rp.'OneDriveLocationException (Optional)'
                $cmdlet += " -OneDriveLocationException " + $para
            }
            if (![String]::IsNullOrEmpty($rp.'SharePointLocation (Optional)'))
            {
                $para = $rp.'SharePointLocation (Optional)'
                $cmdlet += " -SharePointLocation " + $para
            }
            if (![String]::IsNullOrEmpty($rp.'SharePointLocationException (Optional)'))
            {
                $para = $rp.'SharePointLocationException (Optional)'
                $cmdlet += " -SharePointLocationException " + $para
            }
            if (![String]::IsNullOrEmpty($rp.'PublicFolderLocation (Optional)'))
            {
                $para = $rp.'PublicFolderLocation (Optional)'
                $cmdlet += " -PublicFolderLocation " + $para
            }
            if (![String]::IsNullOrEmpty($rp.'SkypeLocation (Optional)'))
            {
                $para = $rp.'SkypeLocation (Optional)'
                $cmdlet += " -SkypeLocation " + $para
            }
            if (![String]::IsNullOrEmpty($rp.'SkypeLocationException (Optional)'))
            {
                $para = $rp.'SkypeLocationException (Optional)'
                $cmdlet += " -SkypeLocationException " + $para
            }
            # If the policy already exists, skip for creation
            if (($policies -eq $null) -or ($policies | ? { $_.Name.ToLower() -eq $name.ToLower() }) -eq $null)
            {
                # Create retention compliance policy
                $msg = "Execute Cmdlet : {0}" -f $cmdlet
            
                $ret = invokepowershellcmdlet $cmdlet
            
                if ($ret -eq $null)
                {
                    WriteToLog -Type "Failed" $error[0]
                    break;
                }
                $rpid = $ret.Guid
            }
            else
            {
                WriteToLog -Type "Warning" -Message "The policy '$name' already exists! Skip for creation!"
                $rpid = ($policies | ? { $_.Name.ToLower() -eq $name.ToLower() }).Guid
            }
                        
            # Retrieve tag name for publishing
            $ts = $rp.'PublishComplianceTag (Required)'
            $tagList = $ts.Split(",") | ForEach-Object { $_.Trim() }
            
            WriteToLog -Type "Message" -Message "Publish Tags : '$ts'" 
            
            PublishComplianceTag -PolicyGuid $rpid -TagName $tagList
        }
    }
    catch
    {
        WriteToLog -Type "Failed" "Error in input"
    }
}
# -------------------
# Publish Compliance Tag
# -------------------
Function PublishComplianceTag
{
    Param(
        [Parameter(Mandatory = $true)]
        [String]$PolicyGuid,
        [Parameter(Mandatory = $true)]
        [String[]]$TagNames
    )
    
    WriteToLog -Type "Start" "Start to Publish Compliance Tag"
    try
    {
        # Retrieve existing rule related to the given compliance policy
        $rule = InvokePowerShellCmdlet ("Get-RetentionComplianceRule -Policy {0}" -f $PolicyGuid)
        $tagGuids = New-Object System.Collections.ArrayList
        
        foreach ($tn in $TagNames)
        {
            $t = InvokePowerShellCmdlet ("Get-ComplianceTag {0}" -f $tn)
            $tagGuids.Add($t.Guid) | Out-Null
        }
        if ($rule -ne $null)
        {
            foreach ($r in $rule)
            {
                if ([String]::IsNullOrEmpty($r.PublishComplianceTag))
                {
                    continue;
                }
                else
                {
                    $tl = $r.PublishComplianceTag.Split(",")
                    if ($tagGuids.Contains([GUID]$tl[0]))
                    {
                        $tagGuids.Remove([GUID]$tl[0]);
                    }
                }
            }
        }
        
        foreach($t in $tagGuids)
        {
            # Publish compliance tag
            $cmdlet = "New-RetentionComplianceRule -Policy {0} -PublishComplianceTag {1}" -f $PolicyGuid, $t
            $ret = InvokePowerShellCmdlet $cmdlet
            
            if ($ret -eq $null)
            {
                WriteToLog -Type "Failed" $error[0]
                break;
            }
        }
    }
    catch
    {
        WriteToLog -Type "Failed" "Error in input"
    }
}
# -------------------
# Export All Labels Created in The Process
# -------------------
Function ExportCreatedComplianceTag
{
    Param(
        [Parameter(Mandatory = $true)]
        [String]$LabelFilePath
    )
    
    WriteToLog -Type "Start" "Start to Export Compliance Tag Created"
    try
    {
        # Import input csv
        $labels = Import-Csv $LabelFilePath
        # Create result table
        $tabName = "ResultTable"
        $table = New-Object system.Data.DataTable "$tabName"
        $col1 = New-Object system.Data.DataColumn Name,([string])
        $col2 = New-Object system.Data.DataColumn Comment,([string])
        $col3 = New-Object system.Data.DataColumn IsRecordLabel,([string])
        $col4 = New-Object system.Data.DataColumn RetentionAction,([string])
        $col5 = New-Object system.Data.DataColumn RetentionDuration,([string])
        $col6 = New-Object system.Data.DataColumn RetentionType,([string])
        $col7 = New-Object system.Data.DataColumn ReviewerEmail,([string])
        
        # Add the Columns
        $table.columns.add($col1)
        $table.columns.add($col2)
        $table.columns.add($col3)
        $table.columns.add($col4)
        $table.columns.add($col5)
        $table.columns.add($col6)
        $table.columns.add($col7)
        foreach($lab in $labels)
        {
            $t = InvokePowerShellCmdlet ("Get-ComplianceTag '{0}' " -f $lab.'Name (Required)')
            
            # Create a result row
            $row = $table.NewRow()
            $row['Name'] = $t.Name
            $row['Comment'] = $t.Comment
            $row['IsRecordLabel'] = $t.IsRecordLabel
            $row['RetentionAction'] = $t.RetentionAction
            $row['RetentionDuration'] = $t.RetentionDuration
            $row['RetentionType'] = $t.RetentionType
            $row['ReviewerEmail'] = $t.ReviewerEmail
            
            # Add the row to the table
            $table.Rows.Add($row)
        }
        $table | Export-Csv $tagRetFile -NoTypeInformation
    }
    catch
    {
        WriteToLog -Type "Failed" "Error in exporting results."
    }
}
# -------------------
# Export All Published Labels and Policies in The Process
# -------------------
Function ExportPublishedComplianceTagAndPolicy
{
    Param(
        [Parameter(Mandatory = $true)]
        [String[]]$PolicyFilePath
    )
    
    WriteToLog -Type "Start" "Start to Export Published Compliance Tag and Policy"
    try
    {
        # Import input csv
        $policies = Import-Csv $PolicyFilePath
        # Create result table
        $tabName = "ResultTable"
        $table = New-Object system.Data.DataTable "$tabName"
        $col1 = New-Object system.Data.DataColumn 'Policy Name',([string])
        $col2 = New-Object system.Data.DataColumn PublishComplianceTag,([string])
        $col3 = New-Object system.Data.DataColumn Comment,([string])
        $col4 = New-Object system.Data.DataColumn Enabled,([string])
        $col5 = New-Object system.Data.DataColumn ExchangeLocation,([string])
        $col6 = New-Object system.Data.DataColumn ExchangeLocationException,([string])
        $col7 = New-Object system.Data.DataColumn ModernGroupLocation,([string])
        $col8 = New-Object system.Data.DataColumn ModernGroupLocationException,([string])
        $col9 = New-Object system.Data.DataColumn OneDriveLocation,([string])
        $col10 = New-Object system.Data.DataColumn OneDriveLocationException,([string])
        $col11 = New-Object system.Data.DataColumn PublicFolderLocation,([string])
        $col12 = New-Object system.Data.DataColumn SharePointLocation,([string])
        $col13 = New-Object system.Data.DataColumn SharePointLocationException,([string])
        $col14 = New-Object system.Data.DataColumn SkypeLocation,([string])
        $col15 = New-Object system.Data.DataColumn SkypeLocationException,([string])
        
        # Add the Columns
        $table.columns.add($col1)
        $table.columns.add($col2)
        $table.columns.add($col3)
        $table.columns.add($col4)
        $table.columns.add($col5)
        $table.columns.add($col6)
        $table.columns.add($col7)
        $table.columns.add($col8)
        $table.columns.add($col9)
        $table.columns.add($col10)
        $table.columns.add($col11)
        $table.columns.add($col12)
        $table.columns.add($col13)
        $table.columns.add($col14)
        $table.columns.add($col15)
        foreach($policy in $policies)
        {
            $t = InvokePowerShellCmdlet ("Get-RetentionCompliancePolicy '{0}' -DistributionDetail" -f $policy.'Policy Name (Required)')
            
            # Create a result row
            $row = $table.NewRow()
            $row['Policy Name'] = $t.Name
            
            $rules = InvokePowerShellCmdlet ("Get-RetentionComplianceRule -Policy {0}" -f $t.Guid)
            $tagList = [String]::Empty
            foreach($rule in $rules)
            {
                if ([String]::IsNullOrEmpty($rule.PublishComplianceTag) -eq $False)
                {
                    $tName = $rule.PublishComplianceTag.Split(',')[1]
                    $tagList = [String]::Concat($tagList, $tName, ",")
                }
            }
            if (![String]::IsNullOrEmpty($tagList))
            {
                $tagList = $tagList.Substring(0, $tagList.LastIndexOf(','))
            }
            $row['PublishComplianceTag'] = $tagList
            $row['Comment'] = $t.Comment
            $row['Enabled'] = $t.Enabled
            $row['ExchangeLocation'] = $t.ExchangeLocation
            $row['ExchangeLocationException'] = $t.ExchangeLocationException
            $row['ModernGroupLocation'] = $t.ModernGroupLocation
            $row['ModernGroupLocationException'] = $t.ModernGroupLocationException
            $row['OneDriveLocation'] = $t.OneDriveLocation
            $row['OneDriveLocationException'] = $t.OneDriveLocationException
            $row['PublicFolderLocation'] = $t.PublicFolderLocation
            $row['SharePointLocation'] = $t.SharePointLocation
            $row['SharePointLocationException'] = $t.SharePointLocationException
            $row['SkypeLocation'] = $t.SkypeLocation
            $row['SkypeLocationException'] = $t.SkypeLocationException
            
            # Add the row to the table
            $table.Rows.Add($row)
        }
        $table | Export-Csv $tagPubRetFile -NoTypeInformation
    }
    catch
    {
        WriteToLog -Type "Failed" "Error in exporting results."
    }
}
# Create compliance tag
CreateComplianceTag -FilePath $LabelListCSV
# Create retention policy and publish compliance tag with the policy
CreateRetentionCompliancePolicy -FilePath $PolicyListCSV
# Export to result csv
if ($ResultCSV)
{
    ExportCreatedComplianceTag -LabelFilePath $LabelListCSV
    ExportPublishedComplianceTagAndPolicy -PolicyFilePath $PolicyListCSV 
}

```

## <a name="step-4-connect-to-security-amp-compliance-center-powershell"></a><span data-ttu-id="0383a-150">4단계: 보안 및 준수 센터 PowerShell에 연결</span><span class="sxs-lookup"><span data-stu-id="0383a-150">Step 4: Connect to Security &amp; Compliance Center PowerShell</span></span>

<span data-ttu-id="0383a-151">아래 단계를 따릅니다.</span><span class="sxs-lookup"><span data-stu-id="0383a-151">Follow the steps here:</span></span>
  
- <span data-ttu-id="0383a-152">[Office 365 보안 및 준수 센터 PowerShell에 연결](https://go.microsoft.com/fwlink/?linkid=799771)</span><span class="sxs-lookup"><span data-stu-id="0383a-152">Connect to Office 365 Security  Compliance Center</span></span>
    
## <a name="step-5-run-the-powershell-script-to-create-and-publish-the-labels"></a><span data-ttu-id="0383a-153">5단계: PowerShell 스크립트를 실행하여 레이블 만들기 및 게시</span><span class="sxs-lookup"><span data-stu-id="0383a-153">Step 5: Run the PowerShell script to create and publish the labels</span></span>

<span data-ttu-id="0383a-154">보안 및 준수 센터 PowerShell에 연결한 후 레이블을 만들고 게시하는 스크립트를 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="0383a-154">After you've connected to Security &amp; Compliance Center PowerShell, next you run the script that creates and publishes the labels.</span></span>
  
1. <span data-ttu-id="0383a-155">보안 및 준수 센터 PowerShell 세션에서 경로 뒤에 .\ 문자와 스크립트의 파일 이름을 입력한 다음 Enter 키를 눌러 스크립트를 실행합니다. 예를 들면 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="0383a-155">In the Security &amp; Compliance PowerShell session, enter the path, followed by the characters .\ and file name of the script, and then press ENTER to run the script - for example:</span></span>
    
  ```
  <path>.\CreateRetentionSchedule.ps1
  ```

    <span data-ttu-id="0383a-156">위에서 만든 .csv 파일의 위치를 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="0383a-156">The script will prompt you for the locations of the .csv files that you created above.</span></span>
    
2. <span data-ttu-id="0383a-157">경로 뒤에 .\ 문자와 .csv 파일의 파일 이름을 입력한 다음 Enter 키를 누릅니다. 예를 들면 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="0383a-157">Enter the path, followed by the characters .\ and file name of the .csv file, and then press ENTER - for example:</span></span>
    
  ```
  <path>.\LabelsToCreate.csv
  ```

## <a name="step-6-view-the-log-file-with-the-results"></a><span data-ttu-id="0383a-158">6단계: 결과가 포함된 로그 파일 보기</span><span class="sxs-lookup"><span data-stu-id="0383a-158">Step 6: View the log file with the results</span></span>

<span data-ttu-id="0383a-p113">스크립트를 실행하면 수행된 각 작업과 작업 성공 또는 실패 여부를 기록하는 로그 파일이 생성됩니다. 로그 파일에는 생성된 레이블과 게시된 레이블에 대한 모든 메타데이터가 포함됩니다. 이 위치에서 로그 파일을 찾을 수 있습니다. 파일 이름의 숫자는 각기 다릅니다.</span><span class="sxs-lookup"><span data-stu-id="0383a-p113">When you run the script, it generates a log file that records each action it took and whether the action succeeded or failed. The log file includes all metadata about what labels were created and what labels were published. You can find the log file at this location -- note that the digits in the file name vary.</span></span>
  
```
<path>.\Log_Publish_Compliance_Tag_01112018_151239.txt
```


