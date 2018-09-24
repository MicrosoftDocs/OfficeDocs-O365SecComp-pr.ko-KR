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
ms.openlocfilehash: 90ee59c5afed1cd260e13134299a7cb4f17dc5bc
ms.sourcegitcommit: 17c7e18d7d00135b1af40cbea117c9a817a41117
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/24/2018
ms.locfileid: "24972320"
---
# <a name="get-details-about-devices-managed-by-mobile-device-management-mdm-for-office-365"></a>Office 365에 대 한 모바일 장치 관리 (MDM) 하 여 관리 되는 장치에 대 한 정보를 봅니다.

이 문서에서는 조직에서 Office 365에 대 한 모바일 장치 관리에 대 한 설정 하는 장치에 대 한 세부 정보를 가져오는데 Windows PowerShell을 사용 하는 방법을 보여줍니다. 
  
## <a name="what-device-details-can-i-get"></a>어떤 장치 세부 정보를 얻을 수 있습니까?

분석 하는 다음과 같습니다.
  
|**세부 정보**|**PowerShell에서 찾을 대상을**|
|:-----|:-----|
|장치는 [Office 365에 대 한 MDM에 등록](enroll-your-mobile-device.md) <br/> |*IsManaged* 매개 변수의 값이입니다.  <br/> **True 이면** = 장치 등록 됩니다.  <br/> **False 이면** = 장치는 등록 되지 않습니다.  <br/> |
|장치 [장치 보안 정책](https://go.microsoft.com/fwlink/?linkid=615144) 준수 하는 <br/> |*IsCompliant* 매개 변수의 값이입니다.  <br/> **True 이면** = 장치는 정책을 준수 합니다.  <br/> **False 이면** = 장치 정책에 맞지 않습니다.  <br/> |
   
![장치는 등록 여부 및 불만 사항에 대 한 AAD 셸 매개 변수 값을 표시 하는 흐름](media/647b70f4-f886-41ef-8bff-04773a1da278.png)
  
> [!NOTE]
> 명령 및이 문서에 있는 스크립트에는 [Microsoft Intune](https://www.microsoft.com/en-us/cloud-platform/microsoft-intune)하 여 관리 되는 모든 장치에 대 한 세부 정보를 반환도 됩니다. 
  
## <a name="before-you-begin"></a>시작하기 전에

몇 가지 방법으로 수행 해야 하도록 설정 하려면이 문서의 명령 및 설명 하는 스크립트를 실행 합니다.
  
### <a name="step-1-download-and-install-the-azure-active-directory-module-for-windows-powershell"></a>1 단계: 다운로드 하 고 Azure Active Directory 모듈에 대 한 Windows PowerShell을 설치 합니다.

다음이 단계에서 자세한 정보를 [Office 365 PowerShell 연결](https://docs.microsoft.com/Office365/enterprise/powershell/connect-to-office-365-powershell)을 참조 하십시오.
  
1. [Microsoft Online Services 로그인 도우미에 대 한 IT 전문가 RTWl를](https://www.microsoft.com/en-us/download/details.aspx?id=41950) 이동 하 고 Microsoft Online Services 로그인 도우미에 대 한 **다운로드** 를 클릭 합니다. 
    
2. 다음 단계에 따라 Windows PowerShell용 Microsoft Azure Active Directory 모듈을 설치합니다.
    
    1. 관리자 수준 PowerShell 명령 프롬프트를 엽니다.
        
    2. 실행 하는 `Install-Module MSOnline` 명령 합니다.
        
    3. NuGet 공급자를 설치 하 라는 메시지를 표시 하는 경우 입력 `Y` ENTER 키를 누릅니다.
        
    4. PSGallery에서 모듈을 설치 하 라는 메시지를 표시 하는 경우 입력 `Y` ENTER 키를 누릅니다.
        
    5. 설치 후 PowerShell 명령 창을 닫습니다.
    
### <a name="step-2-connect-to-your-office-365-subscription"></a>2단계: Office 365 구독에 연결

1. Windows Azure Active Directory 모듈에 대 한 Windows PowerShell을에서 다음 명령을 실행 합니다.<br/>  
  `$UserCredential = Get-Credential`

2. **Windows PowerShell 자격 증명 요청** 대화 상자에서 사용자 이름 및 Office 365 전역 관리자 계정에 대 한 암호를 입력 한 다음 **확인**을 클릭 합니다.
    
3. 다음 명령을 실행합니다.<br/>
    `
  Connect-MsolService -Credential $UserCredential
  `

### <a name="step-3-make-sure-youre-able-to-run-powershell-scripts"></a>3 단계: PowerShell 스크립트를 실행할 수 있는지 확인

> [!NOTE]
> 이미 설정한 PowerShell 스크립트를 실행 하는 경우이 단계를 건너뛸 수 있습니다. 
  
**Get MsolUserDeviceComplianceStatus.ps1** 스크립트를 실행 하려면 PowerShell 스크립트를 실행 하는 사용 하도록 설정 해야 합니다. 
  
1. Windows 바탕 화면에서 **시작**을 클릭 하 고 Windows PowerShell를 입력 합니다. **Windows PowerShell**을 마우스 오른쪽 단추로 클릭 한 다음 **관리자 권한으로 실행**을 클릭 합니다.
    
2. 다음 명령을 실행합니다.<br/>
  `Set-ExecutionPolicy RemoteSigned`

3. 대화 상자가 나타나면 입력 `Y` 한 다음 Enter 키를 누릅니다. 
    
## <a name="run-the-get-msoldevice-cmdlet-to-display-details-for-all-devices-in-your-organization"></a>조직에서 모든 장치에 대 한 세부 정보를 표시 하면 MsolDevice cmdlet을 실행

1. Windows PowerShell용 Microsoft Azure Active Directory 모듈을 엽니다.
    
2. 다음 명령을 실행합니다.<br/>
  ```
  Get-MsolDevice -All -ReturnRegisteredOwners | Where-Object {$_.RegisteredOwners.Count -gt 0}
  ```

추가 예제 [Get MsolDevice](https://go.microsoft.com/fwlink/?linkid=841721)을 참조 하십시오.
  
## <a name="run-a-script-to-get-device-details"></a>장치 세부 정보를 가져오는데 스크립트 실행

### <a name="first-save-the-script-to-your-computer"></a>먼저, 스크립트를 컴퓨터에 저장

1. 복사 하 고 메모장에 다음 텍스트를 붙여넣습니다.<br/> 
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

2. 파일 확장명 **. p s 1**을 사용 하 여 Windows PowerShell 스크립트 파일로 저장 합니다. <br/>예제:<br/> `Get-MsolUserDeviceComplianceStatus.ps1`.
    
### <a name="run-the-script-to-get-device-information-for-a-single-user-account"></a>단일 사용자 계정에 대 한 장치 정보를 가져오려면 스크립트 실행

1. Windows PowerShell용 Microsoft Azure Active Directory 모듈을 엽니다.
    
2. 스크립트를 저장 한 폴더로 이동 합니다. 등 C:\PS-Scripts에 저장 한 경우 다음 명령을 실행이 있습니다.<br/>
    `cd C:\PS-Scripts`

3. 에 대 한 장치 세부 정보를 가져오는데 사용할 사용자를 식별 하려면 다음 명령을 실행 합니다. 이 예제에서는 bar@example.com에 대 한 세부 정보를 가져옵니다.<br/>
  ```
  $u = Get-MsolUser -UserPrincipalName bar@example.com
  ```

4. 스크립트를 시작 하려면 다음 명령을 실행 합니다.<br/>
  ```
  .\Get-MsolUserDeviceComplianceStatus.ps1 -User $u -Export
  ```

정보는 Windows 바탕 화면에 CSV 파일로 내보내집니다. CSV의 경로 파일 이름을 지정 하려면 추가 매개 변수를 사용할 수 있습니다.
  
### <a name="run-the-script-to-get-device-information-for-a-group-of-users"></a>사용자 그룹에 대 한 장치 정보를 가져올 스크립트 실행

1. Windows PowerShell용 Microsoft Azure Active Directory 모듈을 엽니다.
    
2. 스크립트를 저장 한 폴더로 이동 합니다. 등 C:\PS-Scripts에 저장 한 경우 다음 명령을 실행이 있습니다.<br/>
  `cd C:\PS-Scripts`

3. 장치 세부 정보를 가져올 하려는 그룹을 식별 하려면 다음 명령을 실행 합니다. 이 예제에서는 FinanceStaff 그룹에서 사용자에 대 한 세부 정보를 가져옵니다.<br/>
  ```
  $u = Get-MsolGroupMember -SearchString "FinanceStaff" | % { Get-MsolUser -ObjectId $_.ObjectId }
  ```

4. 스크립트를 시작 하려면 다음 명령을 실행 합니다.<br/>
  ```
  .\Get-MsolUserDeviceComplianceStatus.ps1 -User $u -Export
  ```

정보는 Windows 바탕 화면에 CSV 파일로 내보내집니다. CSV의 경로 파일 이름을 지정 하려면 추가 매개 변수를 사용할 수 있습니다.
  
## <a name="more-info"></a>추가 정보

[Office 365에 대 한 MDM 개요](overview-of-mdm.md)
  
[Get-MsolDevice](https://go.microsoft.com/fwlink/?linkid=841721)
  

