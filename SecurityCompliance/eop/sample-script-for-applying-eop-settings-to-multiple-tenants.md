---
title: 여러 테넌트에 EOP 설정을 적용하기 위한 샘플 스크립트
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 11/17/2014
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.assetid: e87e84e1-7be0-44bf-a414-d91d60ed8817
description: 다음 샘플 스크립트를 사용하여 여러 테넌트(회사)를 관리하는 Microsoft EOP(Exchange Online Protection) 관리자는 Windows PowerShell을 사용하여 해당 테넌트에 구성 설정을 적용할 수 있습니다.
ms.openlocfilehash: f064a44722d165711543e5a15ec6a19d70af4b25
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/17/2019
ms.locfileid: "34154560"
---
# <a name="sample-script-for-applying-eop-settings-to-multiple-tenants"></a><span data-ttu-id="f41bf-103">여러 테넌트에 EOP 설정을 적용하기 위한 샘플 스크립트</span><span class="sxs-lookup"><span data-stu-id="f41bf-103">Sample script for applying EOP settings to multiple tenants</span></span>

<span data-ttu-id="f41bf-104">다음 샘플 스크립트를 사용하여 여러 테넌트(회사)를 관리하는 Microsoft EOP(Exchange Online Protection) 관리자는 Windows PowerShell을 사용하여 해당 테넌트에 구성 설정을 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f41bf-104">The following sample script lets Microsoft Exchange Online Protection (EOP) admins who manage multiple tenants (companies) use Windows PowerShell to apply configuration settings to their tenants.</span></span>
  
### <a name="to-run-a-script-or-cmdlet-on-multiple-tenants"></a><span data-ttu-id="f41bf-105">여러 테넌트에 대해 스크립트 또는 cmdlet을 실행하려면</span><span class="sxs-lookup"><span data-stu-id="f41bf-105">To run a script or cmdlet on multiple tenants</span></span>

1. <span data-ttu-id="f41bf-106">Excel과 같은 응용 프로그램을 사용하여 .csv 파일(예: c:\scripts\inputfile.csv)을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f41bf-106">Using an application such as Excel, create a .csv file (for example, c:\scripts\inputfile.csv):</span></span>
    
1. <span data-ttu-id="f41bf-107">.csv 파일에서 두 개의 열 이름 UserName 및 Cmdlet을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f41bf-107">In the .csv file, specify two column names: UserName and Cmdlet.</span></span>
    
2. <span data-ttu-id="f41bf-p101">.csv 파일의 각 행에서 UserName 열에는 테넌트의 관리자 이름을 추가하고 cmdlet 열에는 해당 테넌트에 대해 실행할 cmdlet을 추가합니다. 예를 들어 admin@contoso.com 및 Get-AcceptedDomain을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="f41bf-p101">For each row in the .csv file, add the tenant's admin name in the UserName column and the cmdlet to run for that tenant in the Cmdlet column. For example, use admin@contoso.com and Get-AcceptedDomain.</span></span>
    
2. <span data-ttu-id="f41bf-110">[RunCmdletOnMultipleTenants.ps1](sample-script-for-applying-eop-settings-to-multiple-tenants.md#RunCmdletOnMultipleTenants.ps1) 스크립트를 메모장과 같은 편집기에 복사하고 .ps1 파일을 쉽게 찾을 수 있는 위치(예: c:\scripts)에 파일을 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="f41bf-110">Copy the [RunCmdletOnMultipleTenants.ps1](sample-script-for-applying-eop-settings-to-multiple-tenants.md#RunCmdletOnMultipleTenants.ps1) script to an editor like Notepad, and then save the file to a location (like c:\scripts) that makes .ps1 files easy to find.</span></span> 
    
3. <span data-ttu-id="f41bf-111">다음 구문을 사용하여 스크립트를 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="f41bf-111">Run the script by using the following syntax:</span></span>
    ```Powershell
     & "<file path>\RunCmdletOnMultipleTenants.ps1" "<file path>\inputfile.csv"
    ```
    
    <span data-ttu-id="f41bf-112">다음은 예입니다.</span><span class="sxs-lookup"><span data-stu-id="f41bf-112">Here's an example.</span></span> 
    
    ```Powershell
    & "c:\scripts\RunCmdletOnMultipleTenanats.ps1" "c:\scripts\inputfile.csv"
    ```

4. <span data-ttu-id="f41bf-113">각 테넌트에 로그온되며 해당 cmdlet이 실행됩니다.</span><span class="sxs-lookup"><span data-stu-id="f41bf-113">Each tenant will be logged on to, and the cmdlet will be run.</span></span>
    
## <a name="runcmdletonmultipletenantsps1"></a><span data-ttu-id="f41bf-114">Runcmdletonmultipletenants.ps1. ps1</span><span class="sxs-lookup"><span data-stu-id="f41bf-114">RunCmdletOnMultipleTenants.ps1</span></span>
<span data-ttu-id="f41bf-115"><a name="RunCmdletOnMultipleTenants.ps1"> </a></span><span class="sxs-lookup"><span data-stu-id="f41bf-115"></span></span>

```Powershell
# This script runs Windows PowerShell cmdlets on multiple tenants.
# Usage: RunCmdletOnMultipleTenants.ps1 inputfile.csv
#  
# .csv input file sample: 
# UserName,Cmdlet
# admin@contoso.com,Get-AcceptedDomain | ft Name
# URI for connecting to remote Windows PowerShell
$URI = "https://ps.protection.outlook.com/powershell-liveid/"
# Get the .csv file name as an argument to this script.
$FilePath = $args[0]
# Import the UserName and Cmdlet values from the .csv file.
$CompanyList = Import-CSV $FilePath
# Loop through each entry from the .csv file.
ForEach ($Company in $CompanyList) {
# Get the current entry's UserName.
$UserName = $Company.UserName
# Get the current entry's Cmdlet.
$Cmdlet = $Company.Cmdlet
# Create a PowerShell credential object by using the current entry's UserName. Prompt for the password.
$UserCredential = Get-Credential -username $UserName
# Log on to a new Windows PowerShell session.
$Session = New-PSSession -ConfigurationName Microsoft.Exchange -ConnectionUri $URI -Credential $UserCredential -Authentication Basic -AllowRedirection
Import-PSSession $Session
# Here's where the script to be run on the tenant goes.
# In this example, the cmdlet in the .csv file runs.
Invoke-Expression $Cmdlet
# End the current PowerShell session.
remove-pssession -session $Session
}

```


