---
title: 비즈니스용 OneDrive 사이트에 eDiscovery 사용 권한 할당
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 6/27/2018
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- SPO160
- MOE150
- MET150
ms.assetid: 422858ff-917b-46d4-9e5b-3397f60eee4d
description: 특정 키워드, 중요 한 정보 및 기타 검색 조건에 대 한 조직에서 비즈니스 사이트에 대 한 모든 OneDrive를 검색 하려면 SharePoint Online에서 eDiscovery 센터를 사용할 수 있습니다. 조직에서 각 사용자가 자신의 OneDrive 이름이 지정 된 사이트 모음에 있는 비즈니스 사이트의 소유자 https://domain-my.sharepoint.com합니다. 기본적으로 Office 365 전역 관리자 또는 규정 준수 관리자는 비즈니스 사이트에 대 한 모든 OneDrive를 검색 하려면 SharePoint Online에서 eDiscovery 센터를 사용할 수 없습니다. 비즈니스 사이트, 관리자 또는 규정 준수 관리자에 대 한 OneDrive를 검색 하려면 해당 onedrive 비즈니스 사이트에 대 한 사이트 모음 관리자 여야 합니다.
ms.openlocfilehash: 48f84dfe21f0f99913ba2c27123d6c0e1f8bc03f
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22533520"
---
# <a name="assign-ediscovery-permissions-to-onedrive-for-business-sites"></a>비즈니스용 OneDrive 사이트에 eDiscovery 사용 권한 할당

특정 키워드, 중요 한 정보 및 기타 검색 조건에 대 한 조직에서 비즈니스 사이트에 대 한 모든 OneDrive를 검색 하려면 SharePoint Online에서 eDiscovery 센터를 사용할 수 있습니다. 조직에서 각 사용자가 자신의 OneDrive 이름이 지정 된 사이트 모음에 있는 비즈니스 사이트의 소유자 https://domain-my.sharepoint.com합니다. 기본적으로 Office 365 전역 관리자 또는 규정 준수 관리자는 비즈니스 사이트에 대 한 모든 OneDrive를 검색 하려면 SharePoint Online에서 eDiscovery 센터를 사용할 수 없습니다. 비즈니스 사이트, 관리자 또는 규정 준수 관리자에 대 한 OneDrive를 검색 하려면 해당 onedrive 비즈니스 사이트에 대 한 사이트 모음 관리자 여야 합니다. 
  
이 문서에서는 조직에서 관리자 또는 규정 준수 관리자 비즈니스 사이트에 대 한 모든 OneDrive에 대 한 사이트 모음 관리자를 확인 하는 단계를 안내 합니다. 
  
이 문서에서는 비즈니스 사이트에 대 한 사이트 모음 관리자로 OneDrive에서 사용자를 제거 하려면 3 단계에서에서 스크립트를 수정 하는 포함 하 여 스크립트를 사용 하는 방법에 대 한 팁에 대 한 [자세한 내용](#more-information) 은 섹션을 참조 하십시오. 
  
## <a name="before-you-begin"></a>시작하기 전에

- SharePoint Online 관리 셸을 설치 합니다. 내용은 [SharePoint Online 관리 셸 Windows PowerShell 환경 설정](https://go.microsoft.com/fwlink/p/?LinkID=286318)을 참조 하십시오.
    
- 조직에서 비즈니스 사이트에 대 한 모든 OneDrive에 사이트 모음 관리자 권한으로 사용자를 할당 하려는 때마다 3 단계에서에서 스크립트를 실행 합니다. 
    
    > [!IMPORTANT]
    > 관리자 또는 규정 준수 관리자에 게 OneDrive에 대 한 사이트 모음 관리자는 비즈니스 사이트 수 있는 비즈니스 문서 라이브러리에 대 한 사용자의 OneDrive 열고 소유자와 동일한 작업을 수행 하기 위한 합니다. 제어 하 고 사용자가 할당 된 사용 권한을 eDiscovery OneDrive 조직에서 비즈니스 사이트에 대 한 모니터링을 고려해 야 합니다. 
  
- 이 문서에서 제공 되는 샘플 스크립트는 Microsoft 표준 지원 프로그램이 나 서비스에서 지원 되지 않습니다. 샘플 스크립트는 어떠한 보증도 없이 있는 그대로 제공 됩니다. Microsoft 추가로 포함 하 여, 제한 되지 않고 하는 모든 묵시적된 보증을 부인 묵시적 보증 상품성 또는 특정 목적에의 적합성입니다. 사용 또는 성능 샘플 스크립트 및 설명서에 발생 하는 위험은 있습니다. 어떠한 이벤트에 Microsoft, 해당 작성자 또는 다른 만들기, 제작, 또는 스크립트의 배달에 참여 하는 모든 책임을 지지 모든 손해에 대해 (포함 하 되, 제한 되지 않고 비즈니스 이익, 영업 중단, 손실 손실에 대 한 손해 비즈니스 정보 또는 기타 금전적 손실을) Microsoft가 그와 같은 손해의 가능성을 사전에 알고 있었던 경우에 사용 또는 설명서를 확인 하는 샘플 스크립트를 사용 하 여 원인으로 발생 합니다.
    
## <a name="step-1-collect-a-list-of-all-onedrive-for-business-sites"></a>1 단계: 비즈니스 사이트에 대 한 모든 OneDrive 목록이 수집 합니다.

먼저 조직에서 비즈니스 사이트에 대 한 모든 OneDrive의 목록을 만드는 것입니다. 자세한 내용은 [조직에서 모든 OneDrive 위치 목록을 만들기](https://support.office.com/article/8e200cb2-c768-49cb-88ec-53493e8ad80a)를 참조 합니다. 이 문서에서이 스크립트는 모든 OneDrive 사이트의 목록을 포함 하는 텍스트 파일을 만듭니다. 3 단계에서에서 실행 하는 스크립트는이 단계에서 만든 텍스트 파일에 나열 된 비즈니스 사이트에 대 한 각 OneDrive에 사이트 모음 관리자로 지정 된 사용자를 할당 합니다. 다음 텍스트에는이 파일에는 사이트의 목록 서식 지정 방법의 예가 나와 있습니다. 필요한 경우이 파일에서 사이트를 제거할 수 있습니다.

```
/personal/annb_contoso_onmicrosoft_com/
/personal/carolt_contoso_onmicrosoft_com/
/personal/esterv_contoso_onmicrosoft_com/
/personal/hollyh_contoso_onmicrosoft_com/
/personal/jeffl_contoso_onmicrosoft_com/
/personal/joeh_contoso_onmicrosoft_com/
/personal/kaia_contoso_onmicrosoft_com/
```

## <a name="step-2-connect-sharepoint-online-management-shell-to-your-organization"></a>2 단계: SharePoint Online 관리 셸을 조직에 연결

1. 로컬 컴퓨터에서 SharePoint Online 관리 셸을 열고 다음 명령을 실행합니다.

    ```
    $credentials = Get-Credential
    ```

2. **Windows PowerShell 자격 증명 요청** 대화 상자에서 Office 365 전역 관리자 계정의 사용자 이름 및 암호를 입력한 다음 **확인**을 클릭합니다.
    
3. 다음 명령을 실행하여 SharePoint Online 조직에 셸을 연결합니다.
    
    ```
    Connect-SPOService -Url https://<your organization name>-admin.sharepoint.com -credential $credentials
    ```
   
4. SharePoint Online 조직에 연결되었는지 확인하려면 다음 명령을 실행하여 조직의 모든 사이트 목록을 가져옵니다.
    
    ```
    Get-SPOSite
    ```

## <a name="step-3-assign-a-user-as-a-site-collection-administrator-to-onedrive-for-business-sites"></a>3단계: 사용자를 비즈니스용 OneDrive 사이트에 사이트 모음 관리자로 할당

다음 단계에서는 조직에서 비즈니스 사이트에 대 한 모든 OneDrive에서 사이트 모음 관리자로 지정 된 사용자를 할당 하는 스크립트를 실행 하는 것입니다. 이 스크립트는 1 단계에서에서 만든 비즈니스 사이트에 대 한 OneDrive 목록이 사용 합니다. 앞서 설명한 것 처럼 비즈니스 사이트에 대 한 사용자를 사이트 모음 관리자로 OneDrive 할당 하려는 때마다가이 스크립트를 실행 해야 합니다.
  
1. 다음 텍스트를 텍스트 파일로 저장합니다. 예를 들어 OD4BAssignSCA.txt 파일로 저장할 수 있습니다.

    ```
    # Start logging, so if this script fails, you can look at the last successful change,
    # remove any OneDrive for Business paths that worked it from the input file, and then rerun the script.

    Start-Transcript

    # URL for your organization's SPO admin service

    $AdminURI = "https://<your organization name>-admin.sharepoint.com"

    # User account for an Office 365 global admin in your organization

    $AdminAccount = "<global admin account>"

    # Compliance manager to be made site collection admin on each MySite

    $eDiscoveryUser = "<eDiscovery user account>"

    # URL for your tenant's MySite domain

    $MySitePrefix = "https://<your organization name>-my.sharepoint.com"

    # Where should we read the list of MySites?
    # This file should contain partial MySite paths formatted as follows, one per line; for example
    # /personal/junminh_contoso_onmicrosoft_com/

    $MySiteListFile = 'C:\Users\<youralias>\Desktop\ListOfMysites.txt'

    # Begin by connecting to the service
    Connect-SPOService -Url $AdminURI -Credential $AdminAccount

    # Make a reader for our list of MySites

    $reader = [System.IO.File]::OpenText($MySiteListFile)

    try {
      for(;;) {

    # Read a line
          $line = $reader.ReadLine()
    # Stop if it doesn't exist
          if ($line -eq $null) { break }

    # Turn the line into a complete SharePoint site path by merging $MySitePrefix
    # Formatted like this: "https://contoso-my.sharepoint.com"
    # ...with each partial MySite path in the file, formatted like this:
    # "/personal/junminh_contoso_onmicrosoft_com/"

          $fullsitepath = "$MySitePrefix$line"

    Write-Host "Operating on $fullsitepath "

    # We need to remove the last "/" to work around an issue.
    # "/personal/junminh_contoso_onmicrosoft_com/"
    # becomes "/personal/junminh_contoso_onmicrosoft_com"

    $fullsitepath = $fullsitepath.trimend("/")

    # Make the specified eDiscovery user a site collection admin on the OneDrive for Business site
    Write-Host "Making $eDiscoveryUser a Site Collection Admin"
    Set-SPOUser -Site $fullsitepath -LoginName $eDiscoveryUser -IsSiteCollectionAdmin $true
      }
    }
    finally {
      $reader.Close()
    }
    Write-Host "Done!"
    Stop-Transcript
    Write-Host "Log written."
    ```

2. 스크립트 파일의 시작 부분에서 다음 변수를 편집 하 고 조직에 관련 된 정보를 사용 합니다. 다음 예제에서는 조직의 도메인 이름을 contoso.onmicrosoft.com 형식으로 가정 합니다. 주위에 큰따옴표를 사용 하 여 변수에 대 한 값을 확인 ("").
    
    - **$AdminURI** -이 URI를 지정 하면 SharePoint Online 관리 서비스에 대 한 예 `"https://contoso-admin.sharepoint.com"`합니다.
    
    - **$AdminAccount** -이 전역 관리자 계정을 지정 Office 365 조직에서 예, `"admin@contoso.onmicrosoft.com"`합니다.
    
    - 관리자의 사용자 계정을 지정 **$eDiscoveryUser** -또는 규정 준수 관리자 등 조직 전체에서 비즈니스 사이트에 대 한 모든 OneDrive에 대 한 사이트 모음 관리자로 할당 받을 `"annb@contoso.onmicrosoft.com"`합니다.
    
      > [!NOTE]
      > **$EDiscoveryUser** 변수에 지정 된 사용자 계정을 변경 하 고 다시 **$MySiteListFile** 변수에서 지정 된 비즈니스 사이트에 대 한 OneDrive에 사이트 모음 관리자 권한으로 다른 사용자를 할당 하려면 스크립트를 실행 합니다. 
  
    - **$MySitePrefix** 이 경우 조직의 내 사이트 도메인에 대 한 URL을 지정 합니다. 이것은 등 조직 전체에서 비즈니스 사이트에 대 한 모든 OneDrive를 포함 하는 도메인 `"https://contoso-my.sharepoint.com"`합니다.
    
    - **$MySiteListFile** 1 단계에서에서 만든 텍스트 파일의 전체 경로 지정 합니다. 이 파일의 목록이 표시 OneDrive 조직 전체에서 비즈니스 사이트에 대 한 예 `'C:\Users\<youralias>\Desktop\ListOfMysites.txt'`합니다. 단일 따옴표로이 변수에 대 한 값을 묶지 확인 (' '). Note 1 단계에서에서 텍스트 파일을 저장 하는 위치를 지정 해야 합니다.
    
3. 파일 이름 접미사를 .ps1로 변경하여 텍스트 파일을 PowerShell 스크립트 파일로 저장합니다. 예를 들어 OD4BAssignSCA.txt 파일을 OD4BAssignSCA.ps1로 저장합니다.
    
4. SharePoint Online 관리 셸에서 이전 단계에서 만든 PowerShell 스크립트가 포함된 폴더로 이동한 다음 스크립트를 실행합니다. 예:
    
    ```
    .\OD4BAssignSCA.ps1
    ```

    스크립트에 지정 된 관리자 계정의 암호를 입력 하 라는 메시지가 표시 됩니다. 스크립트를 메시지 성공적으로 실행 하는 경우 `"Making  _\<user specified by $eDiscoveryUser\>_ a Site Collection Admin"` **$MySiteListFile**하 여 지정한 입력된 파일에 나열 된 비즈니스 사이트에 대 한 각 onedrive 표시 됩니다.

## <a name="more-information"></a>추가 정보

- 3 단계에서에서 실행 되는 스크립트 **Set-spouser** cmdlet를 사용 하 여 **$MySiteListFile** 변수에 지정 된 파일에 나열 된 비즈니스에 대 한 모든 OneDrive에 사이트 모음 관리자로 지정된 된 사용자를 할당 합니다. 다양 한 사용자에 게 매우 큰 조직을 설정한 경우에 할당 eDiscovery 사용 권한 관리를 쉽게 수행할 수 있도록 다음을 수행 하는 것이 좋습니다. 
    
  - 사용자가 현재 법적 경우에서 관여에 대 한 사이트에만 포함 되도록 비즈니스 사이트에 대 한 OneDrive 목록이 포함 된 1 단계에서에서 만든 파일을 편집 합니다.
    
  - 2, 500 개 이하의 OneDrive 하루 비즈니스 사이트에 대 한 권한을 할당 합니다. 예, 비즈니스 사이트에 대 한 10, 000 OneDrive 조직에 있는 가정해 보겠습니다. 모든 사이트를 수집 하려면 1 단계에서에서 목록을 만들 수 있습니다. 다음 해당 파일을 사용 하 여 2, 500 사용자를 포함 하는 4 개의 파일을 만들 수 있습니다. 첫번째 날에 처음 2, 500 OneDrive 비즈니스 사이트에 대 한 사용 권한을 할당 하려면 3 단계에서에서 스크립트를 실행 합니다. 두 번째 날에 비즈니스 사이트에 대 한 다음 2, 500 onedrive 스크립트를 실행 하는 등입니다.
    
- EDiscovery 사용 권한 및 사이트 모음 관리자로 할당 된 사용자에 할당 된 비즈니스 사이트에 대 한 OneDrive의 레코드를 유지 합니다. 예, 사용 권한을 할당한 후 비즈니스 사이트에 대 한 OneDrive 목록이 포함 된 텍스트 파일을 저장 하 고 하 여 사이트 모음 관리자로 할당 된 사용자를 식별 하는 줄을 추가 수 있습니다.
    
- 사용자는 자신의 onedrive 비즈니스 사이트에 대 한 사이트 모음 administators 목록이 볼 수 있습니다. 사용자가 자신의 onedrive 비즈니스 사이트에 대 한 사이트 모음 관리자는 이기 때문에 사이트 모음 관리자를 제거할 수 있습니다. EDiscovery 권한을 비즈니스 사이트에 대 한의 OneDrive에 할당 된 사용자를 제거 하는 사용자의 가능성을 완화 하기 위해 다음을 수행 하는 것이 좋습니다.
    
  - eDiscovery 및 규정 준수 목적을 위해 규정 준수 관리자가 할당 된 사이트 모음 관리자로 OneDrive 조직에서 비즈니스 사이트에 대 한 사용자에 게 알려야 합니다.
    
  - 사이트 모음 관리자로 OneDrive에 대 한 비즈니스 사이트에 대 한 사용자를 다시 할당 하려면 필요한 경우 3 단계에서에서 스크립트를 다시 실행 합니다.
    
- 3 단계에서에서 실행 되는 스크립트를 사용할 수도 있습니다 비즈니스 사이트에 대 한 사이트 모음 관리자로 OneDrive에서 사용자를 제거 해야 합니다. 사이트 모음 관리자 권한으로 사용자를 제거 하려면 (의 끝부분 스크립트)에 다음 명령을에서 변경 해야 합니다. 

    ```
    Set-SPOUser -Site $fullsitepath -LoginName $eDiscoveryUser -IsSiteCollectionAdmin $true
    ```

    다음으로 변경합니다.
    
    ```
    Set-SPOUser -Site $fullsitepath -LoginName $eDiscoveryUser -IsSiteCollectionAdmin $false
    ```

    스크립트의 다음 행을

    ```
    "Making $eDiscoveryUser a Site Collection Admin"
    ```

    다음으로 변경합니다.
    
    ```
    "Removing $eDiscoveryUser as a Site Collection Admin"
    ```

    이러한 변경을 수행한 후 OD4BRemoveSCA.ps1, 등의 다른 이름으로 스크립트를 저장 하 고를 사용 하 여 사이트 모음 관리자로 비즈니스 사이트에 대 한 OneDrive의 그룹에서 사용자를 제거 합니다.
