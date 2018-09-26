---
title: 여러 콘텐츠 검색 만들기, 보고하기 및 삭제
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 6/26/2018
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- SPO160
- MOE150
ms.assetid: 1d463dda-a3b5-4675-95d4-83db19c9c4a3
description: 검색을 만들고 Office 365 보안의 PowerShell 스크립트를 통해 보고서를 실행 하는 등의 콘텐츠 검색 작업을 자동화 하는 방법에 알아봅니다 &amp; 준수 센터입니다.
ms.openlocfilehash: a32c003dfd9a27ea8c38b29b31001b612368bc4a
ms.sourcegitcommit: 7956955cd919f6e00b64e4506605a743c5872549
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/26/2018
ms.locfileid: "25038141"
---
# <a name="create-report-on-and-delete-multiple-content-searches"></a>여러 콘텐츠 검색 만들기, 보고하기 및 삭제

 신속 하 게 만들고 검색 검색 보고는 종종는 중요 한 단계 eDiscovery 및 조사 다양성의 기본 데이터 및 검색의 품질에 대해 자세히 알아보려면 때입니다. 이 작업을 수행 하는데 도움이 되는 보안 &amp; 준수 센터 시간이 오래 걸리는 콘텐츠 검색 작업을 자동화 하는 Windows PowerShell cmdlet의 집합을 제공 합니다. 이러한 스크립트는 다양 한 검색을 만들 수 있는 빠르고 간편한 방법을 제공 하 고 문제의 데이터의 양을 결정 하는 데 도움이 되는 예상된 검색 결과의 보고서를 실행 하십시오. 또한 각 하나를 생성 하 고 결과 비교 하는 검색의 서로 다른 버전을 만드는 스크립트를 사용할 수 있습니다. 이러한 스크립트에서 빠르고 효율적으로 식별 하 고 데이터를 cull 쉽게 메시지를 표시할 수 있습니다. 
  
## <a name="before-you-begin"></a>시작하기 전에

- 보안에서 eDiscovery 관리자 역할 그룹의 구성원 이어야 하는 &amp; 이 항목에서 설명 하는 스크립트를 실행 하려면 준수 센터입니다. 
    
- 1 단계에서에서 CSV 파일에 추가할 수 있는 조직에서 비즈니스 사이트에 대 한 OneDrive에 대 한 Url의 목록을 수집 하려면 [조직에서 모든 OneDrive 위치 목록을 만들기](https://support.office.com/article/Create-a-list-of-all-OneDrive-locations-in-your-organization-8e200cb2-c768-49cb-88ec-53493e8ad80a)를 참조 합니다. 
    
- 이 항목을 동일한 폴더에서 만든 모든 파일을 저장 해야 합니다. 하는 간편 하 게 스크립트를 실행 합니다.
    
- 스크립트는 최소한의 오류 처리를 포함 합니다. 주요 용도를 신속 하 게, 대 한 보고서를 만들고 여러 콘텐츠 검색을 delete 하는 합니다.
    
- 이 항목에서 제공된 샘플 스크립트는 Microsoft 표준 지원 프로그램 또는 서비스에서는 지원되지 않습니다. 샘플 스크립트는 어떠한 보증도 없이 "있는 그대로" 제공됩니다. Microsoft는 묵시적인 모든 보증(상품성 또는 특정 목적에의 적합성에 대한 묵시적인 보증을 포함하되 이에 제한되지 않음)을 부인합니다. 샘플 스크립트 및 문서의 사용 또는 수행으로 인해 발생하는 모든 위험은 사용자의 책임입니다. 어떠한 경우에도 Microsoft, 스크립트 작성자 또는 스크립트의 작성, 생산 또는 제공과 관련된 사람은 누구나 샘플 스크립트 또는 문서의 사용 또는 사용 불가능으로 인해 발생하는 모든 손해(수익에 대한 손실, 비즈니스 중단, 비즈니스 정보 손실 또는 기타 금전상의 손실을 포함하되 이에 제한되지 않음)에 대해 책임지지 않습니다. 이는 Microsoft가 이러한 손해가 발생할 가능성에 대해 알고 있었더라고 마찬가지입니다.
    
## <a name="step-1-create-a-csv-file-that-contains-information-about-the-searches-you-want-to-run"></a>1 단계:를 실행 하는 검색에 대 한 정보가 포함 된 CSV 파일 만들기

이 단계에서 만든 쉼표로 구분 된 값 (CSV) 파일을 검색 하려면 각 사용자에 대 한 행을 포함 합니다. 사용자의 Exchange Online 사서함 (포함 하는 보관 사서함에 설정 된 경우) 및 비즈니스 사이트에 대 한 자신의 OneDrive를 검색할 수 있습니다. 또는 사서함만 또는 비즈니스 사이트에 대 한 OneDrive를 검색할 수 있습니다. SharePoint Online 조직에서 모든 사이트를 검색할 수도 있습니다. 3 단계에서에서 실행 하는 스크립트에서는 CSV 파일에 각 행에 대 한 별도 검색을 만듭니다. 
  
1. 복사 하 고 메모장을 사용 하 여.txt 파일에 다음 텍스트를 붙여넣습니다. 로컬 컴퓨터의 폴더에는이 파일을 저장 합니다. 이 폴더로 다른 스크립트를 저장할 수 있습니다.
    
    ```
    ExchangeLocation,SharePointLocation,ContentMatchQuery,StartDate,EndDate
    sarad@contoso.onmicrosoft.com,https://contoso-my.sharepoint.com/personal/sarad_contoso_onmicrosoft_com,(lawsuit OR legal),1/1/2000,12/31/2005
    sarad@contoso.onmicrosoft.com,https://contoso-my.sharepoint.com/personal/sarad_contoso_onmicrosoft_com,(lawsuit OR legal),1/1/2006,12/31/2010
    sarad@contoso.onmicrosoft.com,https://contoso-my.sharepoint.com/personal/sarad_contoso_onmicrosoft_com,(lawsuit OR legal),1/1/2011,3/21/2016
    ,https://contoso.sharepoint.com/sites/contoso,,,3/21/2016
    ,https://contoso-my.sharepoint.com/personal/davidl_contoso_onmicrosoft_com,,1/1/2015,
    ,https://contoso-my.sharepoint.com/personal/janets_contoso_onmicrosoft_com,,1/1/2015,
    ```

    첫째 행 또는 파일의 머리글 행에 새 콘텐츠 검색을 만듭니다 (3 단계에서에서 스크립트)에서 **새로 만들기 ComplianceSearch** cmdlet에 의해 사용 되는 매개 변수를 나열 합니다. 각 매개 변수 이름은 쉼표로 구분 됩니다. 머리글 행에 공백을 남지 있는지 확인 하십시오. 각 행 머리글 행에서 각 검색에 대 한 매개 변수 값을 나타냅니다. 실제 데이터와 함께 CSV 파일의 개체 틀 데이터를 교체 해야 합니다. 
    
2. Excel에서.txt 파일을 열고 각 검색에 대 한 정보를 사용 하 여 파일을 편집 하려면 다음 표의 정보를 사용 합니다. 
    
    |**매개 변수**|**설명**|
    |:-----|:-----|
    | `ExchangeLocation` <br/> |사용자의 사서함의 SMTP 주소입니다.  <br/> |
    | `SharePointLocation` <br/> |비즈니스 사이트에 대 한 사용자의 OneDrive 또는 조직에서 모든 사이트에 대 한 URL에 대 한 URL입니다. 비즈니스 사이트에 대 한 OneDrive에 대 한 URL에 대 한이 형식 사용: ` https://<your organization>-my.sharepoint.com/personal/<user alias>_<your organization>_onmicrosoft_com `합니다. 예, `https://contoso-my.sharepoint.com/personal/sarad_contoso_onmicrosoft_com`합니다.<br/> |
    | `ContentMatchQuery` <br/> |검색에 대 한 검색 쿼리 합니다. 검색 쿼리 만들기 (영문) 하는 방법에 대 한 자세한 내용은 [키워드 쿼리 및 콘텐츠 검색에 대 한 검색 조건을](keyword-queries-and-search-conditions.md)참조 하십시오.<br/> |
    | `StartDate` <br/> |전자 메일에 대 한 날짜 또는 그 이후에 메시지를 받는 사람이 받거나 보낸 사람이 보낸 합니다. SharePoint 또는 OneDrive에 비즈니스 사이트에 대 한 문서에 대 한 날짜 또는 그 이후에 문서를 마지막으로 수정한 합니다.  <br/> |
    | `EndDate` <br/> |하 여 전송 된 날짜 또는 그 이전 메시지에 대 한 전자 메일, 사용자가 보낸 합니다. SharePoint 또는 OneDrive에 비즈니스 사이트에 대 한 문서에 대 한 날짜 또는 그 이전 문서에 마지막으로 수정한 합니다.  <br/> |
   
3. 로컬 컴퓨터의 폴더를 CSV 파일로 Excel 파일을 저장 합니다. 3 단계에서에서 만든 스크립트가 CSV 파일의 정보를 사용 하 여 검색을 만들 수 있습니다. 
  
## <a name="step-2-connect-to-security--compliance-center-powershell"></a>2 단계: 보안 및 규정 준수 센터 PowerShell에 연결

다음 단계는 보안을 Windows PowerShell에 연결 하는 &amp; 조직에 대 한 준수 센터입니다.
  
1. .Ps1 파일 이름 접미사를 사용 하 여 Windows PowerShell 스크립트 파일에 다음 텍스트를 저장 예, `ConnectSCC.ps1`합니다. 1 단계에서에서 CSV 파일을 저장 하는 동일한 폴더에 파일을 저장 합니다.
    
    ```
    # Get login credentials 
    $UserCredential = Get-Credential 
    $Session = New-PSSession -ConfigurationName Microsoft.Exchange -ConnectionUri https://ps.compliance.protection.outlook.com/powershell-liveid -Credential $UserCredential -Authentication Basic -AllowRedirection 
    Import-PSSession $Session -AllowClobber -DisableNameChecking 
    $Host.UI.RawUI.WindowTitle = $UserCredential.UserName + " (Office 365 Security &amp; Compliance Center)" 
    ```

2. 로컬 컴퓨터에서 Windows PowerShell, 이전 단계에서 만든 스크립트 위치한 폴더로 이동한 다음 열고 실행 스크립트입니다. 예를 들어:
    
    ```
    .\ConnectSCC.ps1
    ```
  
## <a name="step-3-run-the-script-to-create-and-start-the-searches"></a>3 단계:를 만들고 검색 시작 스크립트를 실행 합니다.

이 단계에서는 스크립트에서는 1 단계에서에서 만든 CSV 파일에 각 행에 대 한 별도 콘텐츠 검색을 만듭니다. 이 스크립트를 실행 하면 두 값에 대 한 묻는 메시지가 나타납니다.
  
- **검색 그룹 ID** -이 이름은 CSV 파일에서 만든 검색을 구성 하는 간편한 방법을 제공 합니다. 검색 그룹 ID를 사용 하 여 생성 된 각 검색 라는 하 고 검색 이름에 숫자를 추가 하는 다음 키를 누릅니다. 예, 검색 그룹 ID에 대 한 **ContosoCase** 를 입력 하는 경우 다음 검색은 명명 된 **ContosoCase_1**, **ContosoCase_2**, **ContosoCase_3**등에. 메모를 입력할 때 이름은 대/소문자 구분 합니다. 4 단계와 5 단계에서 검색 그룹 ID를 사용 하면 만들었을 때와 같이 동일한 대/소문자를 사용 해야 합니다. 
    
- **CSV 파일** -1 단계에서에서 만든 CSV 파일의 이름입니다. 사용할 전체 이름을 사용 하 여 포함,.csv 파일 확장명을 포함 해야 합니다. 예, `ContosoCase.csv`합니다.
    
스크립트를 실행하려면

1. .Ps1 파일 이름 접미사를 사용 하 여 Windows PowerShell 스크립트 파일에 다음 텍스트를 저장 예, `CreateSearches.ps1`합니다. 다른 파일을 저장 하는 동일한 폴더에 파일을 저장 합니다.
    
  ```
  # Get the Search Group ID and the location of the CSV input file
  $searchGroup = Read-Host 'Search Group ID'
  $csvFile = Read-Host 'Source CSV file'
    
  # Do a quick check to make sure our group name will not collide with other searches
  $searchCounter = 1
  import-csv $csvFile |
    ForEach-Object{
    
    $searchName = $searchGroup +'_' + $searchCounter
    $search = Get-ComplianceSearch $searchName -EA SilentlyContinue
    if ($search)
    {
        Write-Error "The Search Group ID conflicts with existing searches.  Please choose a search group name and restart the script."
        return
    }
    $searchCounter++
  }
    
  $searchCounter = 1
  import-csv $csvFile |
    ForEach-Object{
    
    # Create the query
    $query = $_.ContentMatchQuery
    if(($_.StartDate -or $_.EndDate))
    {
          # Add the appropriate date restrictions.  NOTE: Using the Date condition property here because it works across Exchange, SharePoint, and OneDrive for Business.
          # For Exchange, the Date condition property maps to the Sent and Received dates; for SharePoint and OneDrive for Business, it maps to Created and Modified dates.
          if($query)
          {
              $query += " AND"
          }
          $query += " ("
          if($_.StartDate)
          {
              $query += "Date >= " + $_.StartDate
          }
          if($_.EndDate)
          {
              if($_.StartDate)
              {
                  $query += " AND "
              }
              $query += "Date <= " + $_.EndDate
          }
          $query += ")"
    }
      
      # -ExchangeLocation can't be set to an empty string, set to null if there's no location.
      $exchangeLocation = $null
      if ( $_.ExchangeLocation)
      {
           $exchangeLocation = $_.ExchangeLocation
      }
    
    # Create and run the search        
    $searchName = $searchGroup +'_' + $searchCounter
    Write-Host "Creating and running search: " $searchName -NoNewline
    $search = New-ComplianceSearch -Name $searchName -ExchangeLocation $exchangeLocation -SharePointLocation $_.SharePointLocation -ContentMatchQuery $query
    
    # Start and wait for each search to complete
    Start-ComplianceSearch $search.Name
    while ((Get-ComplianceSearch $search.Name).Status -ne "Completed")
    {
        Write-Host " ." -NoNewline
        Start-Sleep -s 3
    }
    Write-Host ""
    
    $searchCounter++
  }
  ```

2. Windows PowerShell에서 이전 단계에서 스크립트를 저장 위치 폴더로 이동 하 고; 스크립트를 실행 하는 다음 예를 들어:
    
    ```
    .\CreateSearches.ps1
    ```

3. **검색 그룹 ID** 프롬프트 검색 그룹 이름을 입력 하 고 **Enter**키를 누릅니다. 예, `ContosoCase`합니다. 이후 단계에서 동일한 방식으로 입력 해야 하므로이 이름은 대/소문자를 구분 인지를 기억 합니다.
    
4. **원본 CSV 파일** 프롬프트.csv 파일 확장명;를 포함 하 여 CSV 파일의 이름을 입력합니다 예, `ContosoCase.csv`합니다.
    
5. 스크립트를 실행 하 여 계속 하려면 **Enter** 키를 누릅니다. 
    
    스크립트를 만들고 검색 실행 진행 상태가 표시 됩니다. 스크립트가 완료 되 면 프롬프트를 반환 합니다. 
    
    ![여러 규정 준수 검색을 만드는 스크립트를 실행한 경우의 샘플 출력](media/37d59b0d-5f89-4dbc-9e2d-0e88e2ed7b4c.png)
  
## <a name="step-4-run-the-script-to-report-the-search-estimates"></a>검색 보고를 스크립트 추정 실행 하는 4 단계:

검색을 만든 후 다음 단계 3 단계에서에서 만든 각 검색에 대 한 검색 방문 횟수의 간단한 보고서를 표시 하는 스크립트를 실행 하는 것입니다. 다음은 보고서에는 각 검색 및 방문 횟수의 총 수와 모든 검색의 총 크기에 대 한 결과의 크기를 포함 됩니다. 보고 스크립트를 실행 하면 메시지가 표시 됩니다 검색 그룹 ID 및 CSV 파일에 대 한 보고서를 CSV 파일로 저장 하려는 경우.
  
1. .Ps1 파일 이름 접미사를 사용 하 여 Windows PowerShell 스크립트 파일에 다음 텍스트를 저장 예, `SearchReport.ps1`합니다. 다른 파일을 저장 하는 동일한 폴더에 파일을 저장 합니다.
    
  ```
  $searchGroup = Read-Host 'Search Group ID'
  $outputFile = Read-Host 'Enter a file name or file path to save the report to a .csv file. Leave blank to only display the report'
  $searches = Get-ComplianceSearch | ?{$_.Name -clike $searchGroup + "_*"}
  $allSearchStats = @()
  foreach ($partialObj in $searches)
  {
      $search = Get-ComplianceSearch $partialObj.Name
      $sizeMB = [System.Math]::Round($search.Size / 1MB, 2)
      $searchStatus = $search.Status
      if($search.Errors)
      {
          $searchStatus = "Failed"
      }elseif($search.NumFailedSources -gt 0)
      {
          $searchStatus = "Failed Sources"
      }
      $searchStats = New-Object PSObject
      Add-Member -InputObject $searchStats -MemberType NoteProperty -Name Name -Value $search.Name
      Add-Member -InputObject $searchStats -MemberType NoteProperty -Name ContentMatchQuery -Value $search.ContentMatchQuery
      Add-Member -InputObject $searchStats -MemberType NoteProperty -Name Status -Value $searchStatus
      Add-Member -InputObject $searchStats -MemberType NoteProperty -Name Items -Value $search.Items
      Add-Member -InputObject $searchStats -MemberType NoteProperty -Name "Size" -Value $search.Size
      Add-Member -InputObject $searchStats -MemberType NoteProperty -Name "Size(MB)" -Value $sizeMB
      $allSearchStats += $searchStats
  }
  # Calculate the totals
  $allItems = ($allSearchStats | Measure-Object Items -Sum).Sum
  # Convert the total size to MB and round to the nearst 100th
  $allSize = ($allSearchStats | Measure-Object 'Size' -Sum).Sum
  $allSizeMB = [System.Math]::Round($allSize  / 1MB, 2)
  # Get the total successful searches and total of all searches
  $allSuccessCount = ($allSearchStats |?{$_.Status -eq "Completed"}).Count
  $allCount = $allSearchStats.Count
  $allStatus = [string]$allSuccessCount + " of " + [string]$allCount
  # Totals Row
  $totalSearchStats = New-Object PSObject
  Add-Member -InputObject $totalSearchStats -MemberType NoteProperty -Name Name -Value "Total"
  Add-Member -InputObject $totalSearchStats -MemberType NoteProperty -Name Status -Value $allStatus
  Add-Member -InputObject $totalSearchStats -MemberType NoteProperty -Name Items -Value $allItems
  Add-Member -InputObject $totalSearchStats -MemberType NoteProperty -Name "Size(MB)" -Value $allSizeMB
  $allSearchStats += $totalSearchStats
  # Just get the columns we're interested in showing
  $allSearchStatsPrime = $allSearchStats | Select-Object Name, Status, Items, "Size(MB)", ContentMatchQuery
  # Print the results to the screen
  $allSearchStatsPrime |ft -AutoSize -Wrap
  # Save the results to a CSV file
  if ($outputFile)
  {
      $allSearchStatsPrime | Export-Csv -Path $outputFile -NoTypeInformation
  }
  ```

2. Windows PowerShell에서 이전 단계에서 스크립트를 저장 위치 폴더로 이동 하 고; 스크립트를 실행 하는 다음 예를 들어:
    
    ```
    .\SearchReport.ps1
    ```

3. **검색 그룹 ID** 프롬프트 검색 그룹 이름을 입력 하 고 **Enter**키를 누릅니다. 예 `ContosoCase`합니다. 이 이름은 대/소문자 구분, 입력 해야 하므로 동일한 방식으로 수행한 것과 3 단계에서에서 스크립트를 실행 했을 때 기억 합니다.
    
4. **파일 경로 CSV 파일로 (방금 보고서가 표시 되도록 나가기 비어 있음) 보고서를 저장 하려면** 프롬프트에서 보고서를 CSV 파일로 저장 하려는 경우 전체 파일 이름 경로 (.csv 파일 확장명이 포함)의 파일 이름을 입력 합니다. .csv 파일 확장명을 포함 하 여 CSV 파일의 이름입니다. 입력할 수 등 `ContosoCaseReport.csv` 현재 디렉터리에 저장 하려면 입력 `C:\Users\admin\OneDrive for Business\ContosoCase\ContosoCaseReport.csv` 와 다른 폴더에 저장 해야 합니다. 보고서를 표시 하지만 파일에 저장 하지 빈 프롬프트를도 남길 수 있습니다. 
    
5. **입력**하는 키를 누릅니다.
    
    스크립트를 만들고 검색 실행 진행 상태가 표시 됩니다. 스크립트가 완료 되 면 보고서 표시 됩니다. 
    
    ![검색 보고서를 실행하여 검색 그룹에 대한 예상 결과 표시](media/3b5f2595-71d5-4a14-9214-fad156c981f8.png)
  
> [!NOTE]
> 같은 사서함 이나 사이트를 검색 그룹에서 둘 이상의 검색에서 콘텐츠 위치로 지정 하는 경우 (대 한 항목 수 및 총 크기) 보고서의 총 결과 예측 같은 항목에 대 한 결과 포함할 수 있습니다. 동일한 전자 메일 메시지 또는 문서를 계산 여러 번 검색 그룹에서 다른 검색 쿼리와 일치 하는 경우 때문입니다. 
  
## <a name="step-5-run-the-script-to-delete-the-searches"></a>5 단계: 스크립트를 실행 하는 검색 삭제

검색의 많은 작성할 수 있으므로이 마지막 스크립트 방금 쉽게을 신속 하 게 3 단계에서에서 만든 검색을 삭제 합니다. 다른 스크립트와 같은이 한도를 묻는 메시지 검색 그룹 id입니다. 이 스크립트를 실행 하는 경우 검색 이름에 검색 그룹 ID를 가진 모든 검색 삭제 됩니다. 
  
1. .Ps1 파일 이름 접미사를 사용 하 여 Windows PowerShell 스크립트 파일에 다음 텍스트를 저장 예, `DeleteSearches.ps1`합니다. 다른 파일을 저장 하는 동일한 폴더에 파일을 저장 합니다.
    
  ```
  # Delete all searches in a search group
  $searchGroup = Read-Host 'Search Group ID'
  Get-ComplianceSearch |
      ForEach-Object{
      # If the name matches the search group name pattern (case sensitive), delete the search
      if ($_.Name -cmatch $searchGroup + "_\d+")
      {
          Write-Host "Deleting search: " $_.Name
          Remove-ComplianceSearch $_.Name -Confirm:$false
      }
  }
  ```

2. Windows PowerShell에서 이전 단계에서 스크립트를 저장 위치 폴더로 이동 하 고; 스크립트를 실행 하는 다음 예를 들어:
    
    ```
    .\DeleteSearches.ps1
    ```

3. **검색 그룹 ID** 프롬프트에서 삭제 하려는 검색에 대 한 검색 그룹 이름을 입력 한 다음 **Enter**키를 누릅니다. 예, `ContosoCase`합니다. 이 이름은 대/소문자 구분, 입력 해야 하므로 동일한 방식으로 수행한 것과 3 단계에서에서 스크립트를 실행 했을 때 기억 합니다.
    
    삭제 되는 각 검색의 이름을 표시 하는 스크립트입니다.
    
    ![검색 그룹에서 검색을 삭제하기 위한 스크립트 실행](media/9d97b9d6-a539-4d9b-a4e4-e99989144ec7.png)
