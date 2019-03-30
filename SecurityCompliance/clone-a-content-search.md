---
title: 콘텐츠 검색 복제
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 4/26/2017
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MOE150
- MED150
ms.assetid: 7b40eeaa-544c-4534-b89b-9f79998e374c
description: 이 문서의 Windows PowerShell 스크립트를 사용 하 여 Office 365 또는 Microsoft 365의 준수 센터에서 기존 콘텐츠 검색을 빠르게 복제 합니다. 검색을 복제 하면 원래 검색과 같은 속성을 포함 하는 새 검색 (새 이름 포함)이 만들어집니다. 그런 다음 키워드 쿼리 또는 날짜 범위를 변경 하 여 새 검색을 편집한 다음 실행할 수 있습니다.
ms.openlocfilehash: b08ccb6fbaf2dc9d92e0814fe9f92ea77c731147
ms.sourcegitcommit: e7a776a04ef6ed5e287a33cfdc36aa2d72862b55
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/29/2019
ms.locfileid: "31001201"
---
# <a name="clone-a-content-search"></a>콘텐츠 검색 복제

Office 365 또는 Microsoft 365의 준수 센터에서 콘텐츠 검색을 만들면 많은 사서함 또는 SharePoint 및 비즈니스용 OneDrive 사이트를 검색 하는 데 시간이 오래 걸릴 수 있습니다. URL을 잘못 입력 한 경우 검색할 사이트를 지정 하면 오류가 발생할 수도 있습니다. 이러한 문제가 발생 하지 않도록 하려면이 문서의 Windows PowerShell 스크립트를 사용 하 여 기존 콘텐츠 검색을 빠르게 복제할 수 있습니다. 검색을 복제 하면 원본 검색과 동일한 속성 (예: 콘텐츠 위치 및 검색 쿼리)이 포함 된 새 검색 (다른 이름 포함)이 만들어집니다. 그런 다음 키워드 쿼리 또는 날짜 범위를 변경 하 여 새 검색을 편집 하 고 실행할 수 있습니다.
  
콘텐츠 검색을 복제 하는 이유
  
- 서로 다른 키워드 검색 쿼리 결과를 비교 하려면 동일한 콘텐츠 위치에서 실행 합니다.
    
- 새 검색을 만들 때 많은 수의 콘텐츠 위치를 다시 입력 해야 하는 것을 줄일 수 있습니다.
    
- 검색 결과의 크기를 줄이려면 예를 들어 검색 결과로 너무 많은 결과를 반환 하는 경우 검색을 복제 한 다음 날짜 범위에 따라 검색 조건을 추가 하 여 검색 결과의 수를 줄일 수 있습니다.
  
## <a name="before-you-begin"></a>시작하기 전에

- 이 항목에서 설명 하는 스크립트를 실행 하려면 Security & 준수 센터에서 eDiscovery 관리자 역할 그룹의 구성원 이어야 합니다.
    
- 스크립트에 최소 오류 처리가 포함 되어 있습니다. 이 스크립트의 기본 목적은 콘텐츠 검색을 빠르게 복제 하는 것입니다.
    
- 스크립트에서 새 콘텐츠 검색을 만들지만이를 시작 하지는 않습니다.
    
- 이 스크립트는 복제 중인 콘텐츠 검색이 eDiscovery 사례와 연결 되어 있는지 여부를 고려 합니다. 검색이 사례와 연결 된 경우 새 검색도 동일한 사례에 연결 됩니다. 기존 검색이 사례와 연결 되어 있지 않으면 새 검색이 준수 센터의 **콘텐츠 검색** 페이지에 나열 됩니다. 
    
- 이 항목에서 제공 하는 예제 스크립트는 Microsoft standard 지원 프로그램 또는 서비스에서 지원 되지 않습니다. 예제 스크립트는 어떤 종류의 보증도 없이 있는 그대로 제공 됩니다. Microsoft는 상품성 또는 특정 목적에 대 한 적합성에 대 한 묵시적 보증을 제한 없이 포함 하 여 모든 묵시적 보증을 배제 합니다. 샘플 스크립트 및 설명서의 사용 또는 성능으로 인해 발생 하는 전체 위험은 사용자에 게 남아 있습니다. Microsoft, 작성자 또는 스크립트를 작성, 프로덕션 또는 전달 하는 것과 관련 된 다른 모든 손해에 대 한 책임 (예를 들어, 비즈니스 이익 손실에 대 한 손해, 비즈니스 중단 Microsoft에서 이러한 손해에 대 한 권고를 받은 경우에도 예제 스크립트나 설명서를 사용 하거나 사용 하지 못하는 등의 비즈니스 정보 또는 기타 pecuniary 손실입니다.
  
## <a name="step-1-run-the-script-to-clone-a-search"></a>1 단계: 스크립트를 실행 하 여 검색 복제

이 단계의 스크립트는 기존 콘텐츠 검색을 복제 하 여 새로 만듭니다. 이 스크립트를 실행 하면 다음 정보를 입력 하 라는 메시지가 표시 됩니다.
  
- **사용자 자격 증명** -이 스크립트는 자격 증명을 사용 하 여 Windows PowerShell을 사용 하는 Office 365 조 직에 대 한 보안 & 준수 센터에 연결 합니다. 앞에서 설명한 것 처럼 스크립트를 실행 하려면 Security & compcompliance 센터에서 eDiscovery 관리자 역할 그룹의 구성원 이어야 합니다. 
    
- **기존 검색의 이름** 으로, 복제할 콘텐츠 검색입니다. 
    
- **새로 만들 검색의 이름** -이 값을 비워 두면 스크립트에서 복제 중인 검색의 이름을 기반으로 하는 새 검색의 이름을 만듭니다. 
    
검색을 복제 하려면 다음을 수행 합니다.
  
1. 파일 이름 접미사. p s 1을 사용 하 여 Windows PowerShell 스크립트 파일에 다음 텍스트를 저장 합니다. 예를 `CloneSearch.ps1`들면입니다.
    
  ```
  # This PowerShell script clones an existing Content Search in the Office 365 security and compliance center.
  # Get login credentials from the user
  if(!$UserCredential)
  {
      $UserCredential = Get-Credential
      $Session = New-PSSession -ConfigurationName Microsoft.Exchange -ConnectionUri https://ps.compliance.protection.outlook.com/powershell-liveid -Credential $UserCredential -Authentication Basic -AllowRedirection
      if (!$Session)
      {
          Write-Error "Couldn't create a remote PowerShell session."
          return
      }
      Import-PSSession $Session -AllowClobber -DisableNameChecking
      $Host.UI.RawUI.WindowTitle = $UserCredential.UserName + " (Security & Compliance Center)"
  }
  # Ask for the name of the search you want to clone
  $searchName = Read-Host 'Enter the name of the search that you want to clone'
  # Ask for the name of the new search
  $newSearchName = Read-Host 'Enter a name for the new search [leave blank to automatically generate a name]'
  $originalSearch = Get-ComplianceSearch $searchName -EA SilentlyContinue
  # Make sure we have a valid search before continuing
  if(!$originalSearch)
  {
      Write-Error "Couldn't find search: $searchName"
      return
  }
  $searchNameCounter = 1
  # Find a suitable name for the new search
  while(!$newSearchName)
  {
      $newSearchName = $originalSearch.Name + "_" + $searchNameCounter
      $tempSearch = Get-ComplianceSearch $newSearchName -EA SilentlyContinue
      if ($tempSearch)
      {
          $newSearchName = $null
          $searchNameCounter++
      }
  }
  $caseName
  # Determine if the search is part of a case; if so get the case name
  if ($originalSearch.CaseId)
  {
      $searchCase = Get-ComplianceCase $originalSearch.CaseId
      $caseName = $searchCase.Name
  }
  # Need to cast this value as a Boolean the old fashion way
  $allowNotFoundExchangeLocationsEnabled = $false
  if ($originalSearch.AllowNotFoundExchangeLocationsEnabled)
  {
      $allowNotFoundExchangeLocationsEnabled = $true
  }
  $newSearch = New-ComplianceSearch -Name $newSearchName -AllowNotFoundExchangeLocationsEnabled $allowNotFoundExchangeLocationsEnabled -Case $caseName -ContentMatchQuery $originalSearch.ContentMatchQuery -Description $originalSearch.Description -ExchangeLocation $originalSearch.ExchangeLocation -ExchangeLocationExclusion $originalSearch.ExchangeLocationExclusion -Language $originalSearch.Language -SharePointLocation $originalSearch.SharePointLocation -SharePointLocationExclusion $originalSearch.SharePointLocationExclusion -PublicFolderLocation $originalSearch.PublicFolderLocation
  if ($newSearch)
  {
      Write-Host $newSearch.Name "was successfully created" -ForegroundColor Yellow
  }
  ```

2. Windows PowerShell을 열고 스크립트를 저장 한 폴더로 이동 합니다.
    
3. 스크립트를 실행 합니다. 예를 들어:
    
    ```
    .\CloneSearch.ps1
    ```

4. 자격 증명을 묻는 메시지가 표시 되 면 전자 메일 주소와 암호를 입력 하 고 **확인**을 클릭 합니다.
    
5. 스크립트에서 메시지가 표시 되 면 다음 정보를 입력 합니다. 각 정보를 입력 한 다음 enter 키 **** 를 누릅니다.
    
    - 기존 검색의 이름입니다.
    
    - 새 검색의 이름입니다.
    
    스크립트에서 새 콘텐츠 검색을 만들지만이를 시작 하지는 않습니다. 이렇게 하면 다음 단계에서 검색을 편집 하 고 실행할 수 있습니다. **ComplianceSearch** cmdlet을 실행 하거나 새 검색이 사례와 연결 되어 있는지 여부에 따라 준수 센터의 **콘텐츠 검색** 또는 **eDiscovery** 페이지로 이동 하 여 새 검색의 속성을 볼 수 있습니다. 
  
## <a name="step-2-edit-and-run-the-cloned-search-in-the-compliance-center"></a>2 단계: 준수 센터에서 복제 된 검색 편집 및 실행

스크립트를 실행 하 여 기존 콘텐츠 검색을 복제 한 후에는 준수 센터로 이동 하 여 새 검색을 편집 하 고 실행 합니다. 앞에서 설명한 것 처럼 키워드 검색 쿼리를 변경 하 고 검색 조건을 추가 하거나 제거 하 여 검색을 편집할 수 있습니다. 자세한 내용은 다음을 참조하세요.
  
- [Office 365의 콘텐츠 검색](content-search.md)
    
- [콘텐츠 검색에 대한 키워드 쿼리 및 검색 조건](keyword-queries-and-search-conditions.md)
    
- [eDiscovery 사례](ediscovery-cases.md)
