---
title: Office 365에 대 한 모바일 장치 관리 (MDM) 하 여 관리 되는 장치에 대 한 정보를 봅니다.
ms.author: brendonb
author: brendonb
manager: laurawi
ms.date: 6/12/2018
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MBS150
- MET150
ms.assetid: 5602963c-a1f2-4c21-afb9-f66cd7dca1f0
description: 이 문서에서는 조직에서 Office 365에 대 한 모바일 장치 관리에 대 한 설정 하는 장치에 대 한 세부 정보를 가져오는데 Windows PowerShell을 사용 하는 방법을 보여줍니다.
ms.openlocfilehash: 2e406d3583e7892531b7c74bef0db374672956c7
ms.sourcegitcommit: c31424cafbf1953f2864d7e2ceb95b329a694edb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/29/2018
ms.locfileid: "23272533"
---
# <a name="get-details-about-devices-managed-by-mobile-device-management-mdm-for-office-365"></a><span data-ttu-id="cdab0-103">Office 365에 대 한 모바일 장치 관리 (MDM) 하 여 관리 되는 장치에 대 한 정보를 봅니다.</span><span class="sxs-lookup"><span data-stu-id="cdab0-103">Get details about devices managed by Mobile Device Management (MDM) for Office 365</span></span>

<span data-ttu-id="cdab0-104">이 문서에서는 조직에서 Office 365에 대 한 모바일 장치 관리에 대 한 설정 하는 장치에 대 한 세부 정보를 가져오는데 Windows PowerShell을 사용 하는 방법을 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="cdab0-104">This article shows you how to use Windows PowerShell to get details about the devices in your organization that you set up for Mobile Device Management for Office 365.</span></span> 
  
## <a name="what-device-details-can-i-get"></a><span data-ttu-id="cdab0-105">어떤 장치 세부 정보를 얻을 수 있습니까?</span><span class="sxs-lookup"><span data-stu-id="cdab0-105">What device details can I get?</span></span>

<span data-ttu-id="cdab0-106">분석 하는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="cdab0-106">Here's a breakdown.</span></span>
  
|<span data-ttu-id="cdab0-107">**세부 정보**</span><span class="sxs-lookup"><span data-stu-id="cdab0-107">**Detail**</span></span>|<span data-ttu-id="cdab0-108">**PowerShell에서 찾을 대상을**</span><span class="sxs-lookup"><span data-stu-id="cdab0-108">**What to look for in PowerShell**</span></span>|
|:-----|:-----|
|<span data-ttu-id="cdab0-109">장치는 [Office 365에 대 한 MDM에 등록](enroll-your-mobile-device.md)</span><span class="sxs-lookup"><span data-stu-id="cdab0-109">Device is [enrolled in MDM for Office 365](enroll-your-mobile-device.md)</span></span> <br/> |<span data-ttu-id="cdab0-110">*IsManaged* 매개 변수의 값이입니다.</span><span class="sxs-lookup"><span data-stu-id="cdab0-110">The value of the  *isManaged*  parameter is:</span></span>  <br/> <span data-ttu-id="cdab0-111">**True 이면** = 장치 등록 됩니다.</span><span class="sxs-lookup"><span data-stu-id="cdab0-111">**True** = device is enrolled.</span></span>  <br/> <span data-ttu-id="cdab0-112">**False 이면** = 장치는 등록 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="cdab0-112">**False** = device is not enrolled.</span></span>  <br/> |
|<span data-ttu-id="cdab0-113">장치 [장치 보안 정책](https://go.microsoft.com/fwlink/?linkid=615144) 준수 하는</span><span class="sxs-lookup"><span data-stu-id="cdab0-113">Device is compliant with your [device security policies](https://go.microsoft.com/fwlink/?linkid=615144)</span></span> <br/> |<span data-ttu-id="cdab0-114">*IsCompliant* 매개 변수의 값이입니다.</span><span class="sxs-lookup"><span data-stu-id="cdab0-114">The value of the  *isCompliant*  parameter is:</span></span>  <br/> <span data-ttu-id="cdab0-115">**True 이면** = 장치는 정책을 준수 합니다.</span><span class="sxs-lookup"><span data-stu-id="cdab0-115">**True** = device is compliant with policies.</span></span>  <br/> <span data-ttu-id="cdab0-116">**False 이면** = 장치 정책에 맞지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="cdab0-116">**False** = device is not compliant with policies.</span></span>  <br/> |
   
![장치는 등록 여부 및 불만 사항에 대 한 AAD 셸 매개 변수 값을 표시 하는 흐름](media/647b70f4-f886-41ef-8bff-04773a1da278.png)
  
> [!NOTE]
> <span data-ttu-id="cdab0-118">명령 및이 문서에 있는 스크립트에는 [Microsoft Intune](https://www.microsoft.com/en-us/cloud-platform/microsoft-intune)하 여 관리 되는 모든 장치에 대 한 세부 정보를 반환도 됩니다.</span><span class="sxs-lookup"><span data-stu-id="cdab0-118">The commands and scripts in this article will also return details about any devices that are managed by [Microsoft Intune](https://www.microsoft.com/en-us/cloud-platform/microsoft-intune).</span></span> 
  
## <a name="before-you-begin"></a><span data-ttu-id="cdab0-119">시작하기 전에</span><span class="sxs-lookup"><span data-stu-id="cdab0-119">Before you begin</span></span>

<span data-ttu-id="cdab0-120">몇 가지 방법으로 수행 해야 하도록 설정 하려면이 문서의 명령 및 설명 하는 스크립트를 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="cdab0-120">There are a few things you'll need to set up to run the commands and scripts described in this article.</span></span>
  
### <a name="step-1-download-and-install-the-azure-active-directory-module-for-windows-powershell"></a><span data-ttu-id="cdab0-121">1 단계: 다운로드 하 고 Azure Active Directory 모듈에 대 한 Windows PowerShell을 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="cdab0-121">Step 1: Download and install the Azure Active Directory Module for Windows PowerShell</span></span>

<span data-ttu-id="cdab0-122">다음이 단계에서 자세한 정보를 [Office 365 PowerShell 연결](https://docs.microsoft.com/Office365/enterprise/powershell/connect-to-office-365-powershell)을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="cdab0-122">For more info on these steps, see [Connect to Office 365 PowerShell](https://docs.microsoft.com/Office365/enterprise/powershell/connect-to-office-365-powershell).</span></span>
  
1. <span data-ttu-id="cdab0-123">[Microsoft Online Services 로그인 도우미에 대 한 IT 전문가 RTWl를](https://www.microsoft.com/en-us/download/details.aspx?id=41950) 이동 하 고 Microsoft Online Services 로그인 도우미에 대 한 **다운로드** 를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="cdab0-123">Go to [Microsoft Online Services Sign-In Assistant for IT Professionals RTWl](https://www.microsoft.com/en-us/download/details.aspx?id=41950) and click **Download** for Microsoft Online Services Sign-in Assistant.</span></span> 
    
2. <span data-ttu-id="cdab0-124">다음 단계에 따라 Windows PowerShell용 Microsoft Azure Active Directory 모듈을 설치합니다.</span><span class="sxs-lookup"><span data-stu-id="cdab0-124">Install the Microsoft Azure Active Directory Module for Windows PowerShell with these steps:</span></span>
    
    1. <span data-ttu-id="cdab0-125">관리자 수준 PowerShell 명령 프롬프트를 엽니다.</span><span class="sxs-lookup"><span data-stu-id="cdab0-125">Open an administrator-level PowerShell command prompt.</span></span>
        
    2. <span data-ttu-id="cdab0-126">실행 하는 `Install-Module MSOnline` 명령 합니다.</span><span class="sxs-lookup"><span data-stu-id="cdab0-126">Run the `Install-Module MSOnline` command.</span></span>
        
    3. <span data-ttu-id="cdab0-127">NuGet 공급자를 설치 하 라는 메시지를 표시 하는 경우 입력 `Y` ENTER 키를 누릅니다.</span><span class="sxs-lookup"><span data-stu-id="cdab0-127">If prompted to install the NuGet provider, type `Y` and press ENTER.</span></span>
        
    4. <span data-ttu-id="cdab0-128">PSGallery에서 모듈을 설치 하 라는 메시지를 표시 하는 경우 입력 `Y` ENTER 키를 누릅니다.</span><span class="sxs-lookup"><span data-stu-id="cdab0-128">If prompted to install the module from PSGallery, type `Y` and press ENTER.</span></span>
        
    5. <span data-ttu-id="cdab0-129">설치 후 PowerShell 명령 창을 닫습니다.</span><span class="sxs-lookup"><span data-stu-id="cdab0-129">After installation, close the PowerShell command window.</span></span>
    
### <a name="step-2-connect-to-your-office-365-subscription"></a><span data-ttu-id="cdab0-130">2단계: Office 365 구독에 연결</span><span class="sxs-lookup"><span data-stu-id="cdab0-130">Step 2: Connect to your Office 365 subscription</span></span>

1. <span data-ttu-id="cdab0-131">Windows Azure Active Directory 모듈에 대 한 Windows PowerShell을에서 다음 명령을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="cdab0-131">In the Windows Azure Active Directory Module for Windows PowerShell, run the following command.</span></span></br>  
  `$UserCredential = Get-Credential`

2. <span data-ttu-id="cdab0-132">**Windows PowerShell 자격 증명 요청** 대화 상자에서 사용자 이름 및 Office 365 전역 관리자 계정에 대 한 암호를 입력 한 다음 **확인**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="cdab0-132">In the **Windows PowerShell Credential Request** dialog box, type the user name and password for your Office 365 global admin account, and then click **OK**.</span></span>
    
3. <span data-ttu-id="cdab0-133">다음 명령을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="cdab0-133">Run the following command.</span></span></br>
    `
  Connect-MsolService -Credential $UserCredential
  `

### <a name="step-3-make-sure-youre-able-to-run-powershell-scripts"></a><span data-ttu-id="cdab0-134">3 단계: PowerShell 스크립트를 실행할 수 있는지 확인</span><span class="sxs-lookup"><span data-stu-id="cdab0-134">Step 3: Make sure you're able to run PowerShell scripts</span></span>

> [!NOTE]
> <span data-ttu-id="cdab0-135">이미 설정한 PowerShell 스크립트를 실행 하는 경우이 단계를 건너뛸 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cdab0-135">You can skip this step if you're already set up to run PowerShell scripts.</span></span> 
  
<span data-ttu-id="cdab0-136">**Get MsolUserDeviceComplianceStatus.ps1** 스크립트를 실행 하려면 PowerShell 스크립트를 실행 하는 사용 하도록 설정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="cdab0-136">To run the **Get-MsolUserDeviceComplianceStatus.ps1** script, you need to enable the running of PowerShell scripts.</span></span> 
  
1. <span data-ttu-id="cdab0-p101">Windows 바탕 화면에서 **시작**을 클릭 하 고 Windows PowerShell를 입력 합니다. **Windows PowerShell**을 마우스 오른쪽 단추로 클릭 한 다음 **관리자 권한으로 실행**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="cdab0-p101">From your Windows Desktop, click **Start**, and then type Windows PowerShell. Right click **Windows PowerShell**, and then click **Run as administrator**.</span></span>
    
2. <span data-ttu-id="cdab0-139">다음 명령을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="cdab0-139">Run the following command.</span></span></br>
  `Set-ExecutionPolicy RemoteSigned`

3. <span data-ttu-id="cdab0-140">대화 상자가 나타나면 입력 `Y` 한 다음 Enter 키를 누릅니다.</span><span class="sxs-lookup"><span data-stu-id="cdab0-140">When prompted, type `Y` and then press Enter.</span></span> 
    
## <a name="run-the-get-msoldevice-cmdlet-to-display-details-for-all-devices-in-your-organization"></a><span data-ttu-id="cdab0-141">조직에서 모든 장치에 대 한 세부 정보를 표시 하면 MsolDevice cmdlet을 실행</span><span class="sxs-lookup"><span data-stu-id="cdab0-141">Run the Get-MsolDevice cmdlet to display details for all devices in your organization</span></span>

1. <span data-ttu-id="cdab0-142">Windows PowerShell용 Microsoft Azure Active Directory 모듈을 엽니다.</span><span class="sxs-lookup"><span data-stu-id="cdab0-142">Open the Microsoft Azure Active Directory Module for Windows PowerShell.</span></span>
    
2. <span data-ttu-id="cdab0-143">다음 명령을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="cdab0-143">Run the following command.</span></span></br>
  ```
  Get-MsolDevice -All -ReturnRegisteredOwners | Where-Object {$_.RegisteredOwners.Count -gt 0}
  ```

<span data-ttu-id="cdab0-144">추가 예제 [Get MsolDevice](https://go.microsoft.com/fwlink/?linkid=841721)을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="cdab0-144">For more examples, see [Get-MsolDevice](https://go.microsoft.com/fwlink/?linkid=841721).</span></span>
  
## <a name="run-a-script-to-get-device-details"></a><span data-ttu-id="cdab0-145">장치 세부 정보를 가져오는데 스크립트 실행</span><span class="sxs-lookup"><span data-stu-id="cdab0-145">Run a script to get device details</span></span>

### <a name="first-save-the-script-to-your-computer"></a><span data-ttu-id="cdab0-146">먼저, 스크립트를 컴퓨터에 저장</span><span class="sxs-lookup"><span data-stu-id="cdab0-146">First, save the script to your computer</span></span>

1. <span data-ttu-id="cdab0-147">복사 하 고 메모장에 다음 텍스트를 붙여넣습니다.</span><span class="sxs-lookup"><span data-stu-id="cdab0-147">Copy and paste the following text into Notepad.</span></span></br> 
  ```
  param (
      [PSObject[]]$users = @(),
      [Switch]$export,
      [String]$exportFileName = "UserDeviceComplianceStatus_" + (Get-Date -Format "yyMMdd_HHMMss") + ".csv",
      [String]$exportPath = [Environment]::GetFolderPath("Desktop")
   )
  [System.Collections.IDictionary]$script:schema = @{
      
      DeviceId = ''
      DeviceOSType = ''
      DeviceOSVersion = ''
      DeviceTrustLevel = ''
      DisplayName = ''
      IsCompliant = ''
      IsManaged = ''
      ApproximateLastLogonTimestamp = ''
      DeviceObjectId = ''    
      RegisteredOwnerUpn = ''
      RegisteredOwnerObjectId = ''
      RegisteredOwnerDisplayName = ''
  }
  function createResultObject
  {
      [PSObject]$resultObject = New-Object -TypeName PSObject -Property $script:schema
      return $resultObject
  }
  If ($users.Count -eq 0)
  {
      $users = Get-MsolUser
  }
  [PSObject[]]$result = foreach ($u in $users)
  {
      
      [PSObject]$devices = get-msoldevice -RegisteredOwnerUpn $u.UserPrincipalName
      foreach ($d in $devices)
      {
          [PSObject]$deviceResult = createResultObject
          $deviceResult.DeviceId = $d.DeviceId 
          $deviceResult.DeviceOSType = $d.DeviceOSType 
          $deviceResult.DeviceOSVersion = $d.DeviceOSVersion 
          $deviceResult.DeviceTrustLevel = $d.DeviceTrustLevel
          $deviceResult.DisplayName = $d.DisplayName
          $deviceResult.IsCompliant = $d.GraphDeviceObject.IsCompliant
          $deviceResult.IsManaged = $d.GraphDeviceObject.IsManaged
          $deviceResult.DeviceObjectId = $d.ObjectId
          $deviceResult.RegisteredOwnerUpn = $u.UserPrincipalName
          $deviceResult.RegisteredOwnerObjectId = $u.ObjectId
          $deviceResult.RegisteredOwnerDisplayName = $u.DisplayName
          $deviceResult.ApproximateLastLogonTimestamp = $d.ApproximateLastLogonTimestamp
          $deviceResult
      }
  }
  If ($export)
  {
      $result | Export-Csv -path ($exportPath + "\" + $exportFileName) -NoTypeInformation
  }
  Else
  {
      $result
  }
  
  ```

2. <span data-ttu-id="cdab0-148">파일 확장명 **. p s 1**을 사용 하 여 Windows PowerShell 스크립트 파일로 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="cdab0-148">Save it as a Windows PowerShell script file by using the file extension **.ps1**.</span></span> </br><span data-ttu-id="cdab0-149">예제:</span><span class="sxs-lookup"><span data-stu-id="cdab0-149">Example:</span></span></br> <span data-ttu-id="cdab0-150">`Get-MsolUserDeviceComplianceStatus.ps1`.</span><span class="sxs-lookup"><span data-stu-id="cdab0-150"></span></span>
    
### <a name="run-the-script-to-get-device-information-for-a-single-user-account"></a><span data-ttu-id="cdab0-151">단일 사용자 계정에 대 한 장치 정보를 가져오려면 스크립트 실행</span><span class="sxs-lookup"><span data-stu-id="cdab0-151">Run the script to get device information for a single user account</span></span>

1. <span data-ttu-id="cdab0-152">Windows PowerShell용 Microsoft Azure Active Directory 모듈을 엽니다.</span><span class="sxs-lookup"><span data-stu-id="cdab0-152">Open the Microsoft Azure Active Directory Module for Windows PowerShell.</span></span>
    
2. <span data-ttu-id="cdab0-p102">스크립트를 저장 한 폴더로 이동 합니다. 등 C:\PS-Scripts에 저장 한 경우 다음 명령을 실행이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cdab0-p102">Navigate to the folder where you saved the script. For example, if you saved it to C:\PS-Scripts, you'd run the following command.</span></span></br>
    `cd C:\PS-Scripts`

3. <span data-ttu-id="cdab0-p103">에 대 한 장치 세부 정보를 가져오는데 사용할 사용자를 식별 하려면 다음 명령을 실행 합니다. 이 예제에서는 bar@example.com에 대 한 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="cdab0-p103">Run the following command to identify the user you want to get device details for. This example gets details for bar@example.com.</span></span></br>
  ```
  $u = Get-MsolUser -UserPrincipalName bar@example.com
  ```

4. <span data-ttu-id="cdab0-157">스크립트를 시작 하려면 다음 명령을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="cdab0-157">Run the following command to initiate the script.</span></span></br>
  ```
  .\Get-MsolUserDeviceComplianceStatus.ps1 -User $u -Export
  ```

<span data-ttu-id="cdab0-p104">정보는 Windows 바탕 화면에 CSV 파일로 내보내집니다. CSV의 경로 파일 이름을 지정 하려면 추가 매개 변수를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cdab0-p104">The information is exported to your Windows Desktop as a CSV file. You can use additional parameters to specify the file name and path of the CSV.</span></span>
  
### <a name="run-the-script-to-get-device-information-for-a-group-of-users"></a><span data-ttu-id="cdab0-160">사용자 그룹에 대 한 장치 정보를 가져올 스크립트 실행</span><span class="sxs-lookup"><span data-stu-id="cdab0-160">Run the script to get device information for a group of users</span></span>

1. <span data-ttu-id="cdab0-161">Windows PowerShell용 Microsoft Azure Active Directory 모듈을 엽니다.</span><span class="sxs-lookup"><span data-stu-id="cdab0-161">Open the Microsoft Azure Active Directory Module for Windows PowerShell.</span></span>
    
2. <span data-ttu-id="cdab0-p105">스크립트를 저장 한 폴더로 이동 합니다. 등 C:\PS-Scripts에 저장 한 경우 다음 명령을 실행이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cdab0-p105">Navigate to the folder where you saved the script. For example, if you saved it to C:\PS-Scripts, you'd run the following command.</span></span></br>
  `cd C:\PS-Scripts`

3. <span data-ttu-id="cdab0-p106">장치 세부 정보를 가져올 하려는 그룹을 식별 하려면 다음 명령을 실행 합니다. 이 예제에서는 FinanceStaff 그룹에서 사용자에 대 한 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="cdab0-p106">Run the following command to identify the group you want to get device details for. This example gets details for users in the FinanceStaff group.</span></span></br>
  ```
  $u = Get-MsolGroupMember -SearchString "FinanceStaff" | % { Get-MsolUser -ObjectId $_.ObjectId }
  ```

4. <span data-ttu-id="cdab0-166">스크립트를 시작 하려면 다음 명령을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="cdab0-166">Run the following command to initiate the script.</span></span></br>
  ```
  .\Get-MsolUserDeviceComplianceStatus.ps1 -User $u -Export
  ```

<span data-ttu-id="cdab0-p107">정보는 Windows 바탕 화면에 CSV 파일로 내보내집니다. CSV의 경로 파일 이름을 지정 하려면 추가 매개 변수를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cdab0-p107">The information is exported to your Windows Desktop as a CSV file. You can use additional parameters to specify the file name and path of the CSV.</span></span>
  
## <a name="more-info"></a><span data-ttu-id="cdab0-169">추가 정보</span><span class="sxs-lookup"><span data-stu-id="cdab0-169">More info</span></span>

[<span data-ttu-id="cdab0-170">Office 365에 대 한 MDM 개요</span><span class="sxs-lookup"><span data-stu-id="cdab0-170">Overview of MDM for Office 365</span></span>](overview-of-mdm.md)
  
[<span data-ttu-id="cdab0-171">Get-MsolDevice</span><span class="sxs-lookup"><span data-stu-id="cdab0-171">Get-MsolDevice</span></span>](https://go.microsoft.com/fwlink/?linkid=841721)
  

