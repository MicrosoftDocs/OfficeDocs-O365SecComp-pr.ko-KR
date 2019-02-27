---
title: Office 365 eDiscovery에서 부분적으로 인덱싱된 항목 조사
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 1/26/2018
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
search.appverid: MOE150
ms.assetid: 4e8ff113-6361-41e2-915a-6338a7e2a1ed
description: 부분적으로 인덱싱된 항목 (또한 인덱싱되지 않은 항목)은 Exchange 사서함 항목 및 몇 가지 이유로 인해 콘텐츠 검색을 위해 완전히 인덱싱되지 않은 SharePoint 및 OneDrive 사이트의 문서입니다. 이 문서에서는 검색을 위해 항목을 인덱싱할 수 없으며 부분적으로 인덱싱된 항목으로 반환 되며, 부분적으로 인덱싱된 항목에 대 한 검색 오류를 식별 하 고, PowerShell 스크립트를 사용 하 여 부분적으로 인덱싱된 전자 메일에 대 한 조직의 노출을 확인 하는 이유를 알 수 있습니다. 항목.
ms.openlocfilehash: d8fec240964ad84b811221754060af3e342af01f
ms.sourcegitcommit: baf23be44f1ed5abbf84f140b5ffa64fce605478
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/26/2019
ms.locfileid: "30295631"
---
# <a name="investigating-partially-indexed-items-in-office-365-ediscovery"></a>Office 365 eDiscovery에서 부분적으로 인덱싱된 항목 조사

Office 365 보안 &amp; 및 준수 센터에서 실행 하는 콘텐츠 검색에서는 검색을 실행할 때 예상 되는 검색 결과에 부분적으로 인덱싱된 항목이 자동으로 포함 됩니다. 부분적으로 인덱싱된 항목은 Exchange 사서함 항목 및 SharePoint의 문서와 몇 가지 이유로 검색을 위해 완전히 인덱싱되지 않은 비즈니스용 OneDrive 사이트입니다. 대부분의 전자 메일 메시지와 사이트 문서는 [전자 메일 메시지에 대 한 인덱싱 제한](limits-for-content-search.md#indexing-limits-for-email-messages)범위 내에 있으므로 성공적으로 인덱싱됩니다. 그러나 일부 항목은 이러한 인덱싱 제한을 초과할 수 있으며 부분적으로 인덱싱됩니다. 검색을 위해 항목을 인덱싱할 수 없으며 콘텐츠 검색을 실행할 때 부분적으로 인덱싱된 항목으로 반환 되는 기타 이유는 다음과 같습니다.
  
- 전자 메일 메시지에는 인덱싱할 수 없는 파일 형식의 첨부 파일이 있습니다. 대부분의 경우 파일 형식을 [인덱싱할 수 없거나 해당 형식이 지원 되지](partially-indexed-items-in-content-search.md#file-types-not-indexed-for-search) 않습니다.
    
- 전자 메일 메시지에는 이미지 파일과 같은 유효한 처리기가 없는 첨부 파일이 있습니다. 부분적으로 인덱싱된 전자 메일 항목의 가장 일반적인 원인은 다음과 같습니다.
    
- 전자 메일 메시지에 첨부 된 파일이 너무 많음
    
- 전자 메일 메시지에 첨부 된 파일이 너무 큽니다.
    
- 파일 형식이 인덱싱에 대해 지원 되지만 특정 파일에 대해 인덱싱 오류가 발생 했습니다.
    
대부분의 Office 365 조직 고객은 볼륨 별로 콘텐츠가 1% 미만이 고 부분적으로 인덱싱되는 크기의 콘텐츠 중 12% 미만 이어야 합니다. 볼륨과 크기 간의 차이점은 큰 파일의 경우 완전히 인덱싱할 수 없는 콘텐츠가 포함 될 가능성이 높기 때문입니다.
  
## <a name="why-does-the-partially-indexed-item-count-change-for-a-search"></a>검색에서 부분적으로 인덱싱된 항목 수가 변경 되는 이유는 무엇 인가요?

Office 365 보안 &amp; 및 준수 센터에서 콘텐츠 검색을 실행 한 후 검색 된 위치에 있는 부분적으로 인덱싱된 항목의 총 수와 크기는 다음에 대 한 자세한 통계에 표시 되는 검색 결과 통계에 나열 됩니다. 검색입니다. 참고 이러한 항목은 검색 통계에서 *인덱싱되지 않은 항목이* 라고도 합니다. 검색 결과에서 반환 되는 부분적으로 인덱싱된 항목의 수에 영향을 주는 몇 가지 사항은 다음과 같습니다. 
  
- 항목이 부분적으로 인덱싱되 고 검색 쿼리와 일치 하는 경우 검색 결과 항목 및 부분적으로 인덱싱된 항목의 개수와 크기 모두에 포함 됩니다. 그러나 같은 검색의 결과를 내보내면 항목은 검색 결과 집합에만 포함 됩니다. 부분적으로 인덱싱된 항목은 포함 되지 않습니다.
    
- 키워드 쿼리 또는 조건을 사용 하 여 검색 쿼리의 날짜 범위를 지정 하는 경우 날짜 범위와 일치 하지 않는 부분적으로 인덱싱된 항목이 부분적으로 인덱싱된 항목의 수에 포함 되지 않습니다. 날짜 범위 내에 속하는 부분적으로 인덱싱된 항목만 부분 인덱싱된 항목의 수에 포함 됩니다.
    
 **참고:** SharePoint 및 OneDrive 사이트에 있는 부분적으로 인덱싱된 항목은 검색에 대 한 자세한 통계에 표시 되는 부분적으로 인덱싱된 항목의 예상 기간에 포함 *되지 않습니다* . 그러나 콘텐츠 검색 결과를 내보낼 때 부분적으로 인덱싱된 항목을 내보낼 수 있습니다. 예를 들어 콘텐츠 검색 에서만 사이트를 검색 하는 경우 예상 되는 숫자의 부분 인덱싱된 항목은 0입니다. 
  
## <a name="calculating-the-ratio-of-partially-indexed-items-in-your-organization"></a>조직에서 부분적으로 인덱싱된 항목의 비율 계산

부분적으로 인덱싱된 항목에 대 한 조직의 노출을 이해 하려면 빈 키워드 쿼리를 사용 하 여 모든 사서함의 모든 콘텐츠에 대해 검색을 실행할 수 있습니다. 아래 아래의 예제에는 56208 (4830 mb) 완전히 인덱싱된 항목 및 470 (5mb) 부분 인덱싱된 항목이 있습니다.
  
![부분적으로 인덱싱된 항목을 보여 주는 검색 통계 예제](media/0f6a5cf7-4c98-44a0-a0dd-5aed67124641.png)
  
다음 계산을 사용 하 여 부분적으로 인덱싱된 항목의 백분율을 확인할 수 있습니다.
  
 **조직에서 부분적으로 인덱싱된 항목의 비율을 계산 하려면 다음을 수행 합니다.**

`(Total number of partially indexed items/Total number of items) x 100`


`(470/56,208) x 100 = 0.84%`
 
이전 예제의 검색 결과를 사용 하 여. 모든 사서함의 84% 항목이 부분적으로 인덱싱됩니다.
  
 **조직에서 부분적으로 인덱싱된 항목의 크기 비율을 계산 하려면 다음을 수행 합니다.**

`(Size of all partially indexed items/Size of all items) x 100`

`(316 MB/4830 MB) x 100 = 6.54%`

따라서 위 예에서 전체 사서함 항목 크기의 6.54%는 부분적으로 인덱싱된 항목에 해당 합니다. 앞에서 설명한 것 처럼 대부분의 Office 365 조직 고객은 볼륨 별로 콘텐츠가 1% 미만이 고 부분적으로 인덱싱되는 크기의 콘텐츠 중 12% 미만 이어야 합니다.

## <a name="working-with-partially-indexed-items"></a>부분적으로 인덱싱된 항목 사용

일부 항목을 검사 하 여 관련 정보가 포함 되어 있지 않은지 확인 해야 하는 경우에는 부분적으로 인덱싱된 항목에 대 한 정보가 포함 된 [콘텐츠 검색 보고서를 내보낼](export-a-content-search-report.md) 수 있습니다. 콘텐츠 검색 보고서를 내보낼 때는 부분적으로 인덱싱된 항목이 포함 된 내보내기 옵션 중 하나를 선택 해야 합니다. 
  
![두 번째 또는 세 번째 옵션을 선택 하 여 부분적으로 인덱싱된 항목 내보내기](media/624a62b4-78f7-4329-ab5d-e62e3b369885.png)
  
이러한 옵션 중 하나를 사용 하 여 콘텐츠 검색 결과 나 콘텐츠 검색 보고서를 내보낼 때 내보내기에는 인덱싱되지 않은 항목 .csv 이라는 보고서가 포함 됩니다. 이 보고서에는 ResultsLog 파일의 정보 대부분과 동일한 정보가 포함 되어 있습니다. 그러나 인덱싱되지 않은 항목 .csv 파일에는 부분 인덱싱된 항목과 관련 된 두 개의 필드인 **오류 태그** 및 **오류 속성이**포함 되어 있습니다. 이러한 필드에는 부분적으로 인덱싱된 각 항목의 인덱싱 오류에 대 한 정보가 포함 됩니다. 이러한 두 필드의 정보를 사용 하 여 특정 사항에 대 한 인덱싱 오류가 조사에 영향을 미치는지 여부를 결정할 수 있습니다. 이 경우 대상 콘텐츠 검색을 수행 하 고 특정 전자 메일 메시지와 SharePoint 또는 OneDrive 문서를 검색 하 고 내보내서 조사와 관련이 있는지 확인 하는 데 사용할 수 있습니다. 단계별 지침은 [Office 365에서 대상 콘텐츠 검색을 위한 CSV 파일 준비](csv-file-for-an-id-list-content-search.md)를 참조 하세요.
  
 **참고:** 또한 인덱싱되지 않은 항목 .csv 파일에는 **오류 유형** 및 **오류 메시지**라는 필드도 포함 되어 있습니다. 이러한 필드는 **오류 태그** 및 **오류 속성** 필드의 정보와 유사 하지만 자세한 정보를 포함 하는 레거시 필드가 됩니다. 이러한 레거시 필드는 무시 해도 됩니다. 
  
## <a name="errors-related-to-partially-indexed-items"></a>부분적으로 인덱싱된 항목과 관련 된 오류

error 태그는 두 가지 정보, 오류 및 파일 형식으로 구성 됩니다. 예를 들어 다음 오류/filetype 쌍에서 다음을 수행 합니다.

```
 parseroutputsize_xls
```

   
 `parseroutputsize`은 오류이 고 `xls` 오류가 발생 한 파일의 파일 형식입니다. 파일 형식이 인식 되지 않았거나 파일 형식이 오류에 적용 되지 않는 경우에는 파일 형식 대신 값 `noformat` 이 표시 됩니다. 
  
다음은 인덱싱 오류 목록과 오류의 가능한 원인에 대 한 설명입니다.
  
|**Error 태그**|**설명**|
|:-----|:-----|
| `attachmentcount` <br/> |전자 메일 메시지의 첨부 파일이 너무 많고 이러한 첨부 파일 중 일부가 처리 되지 않았습니다.  <br/> |
| `attachmentdepth` <br/> |콘텐츠 검색기 및 문서 파서가 다른 첨부 파일 내에 중첩 된 첨부 파일의 수준을 너무 많이 검색 했습니다. 이러한 첨부 파일 중 일부가 처리 되지 않았습니다.  <br/> |
| `attachmentrms` <br/> |첨부 파일이 RMS 보호 되었기 때문에 디코딩에 실패 했습니다.  <br/> |
| `attachmentsize` <br/> |전자 메일 메시지에 첨부 된 파일이 너무 커서 처리할 수 없습니다.  <br/> |
| `indexingtruncated` <br/> |처리 된 전자 메일 메시지를 인덱스에 쓸 때 인덱싱 가능한 속성 중 하나가 너무 커서 잘렸습니다. 잘린 속성은 오류 속성 필드에 나열 됩니다.  <br/> |
| `invalidunicode` <br/> |유효한 유니코드로 처리할 수 없는 텍스트가 포함 된 전자 메일 메시지 이 항목에 대 한 인덱싱이 불완전할 수 있습니다.  <br/> |
| `parserencrypted` <br/> |첨부 파일 또는 전자 메일 메시지의 내용이 암호화 되 고 Office 365에서 콘텐츠를 디코딩할 수 없습니다.  <br/> |
| `parsererror` <br/> |구문 분석 중 알 수 없는 오류가 발생 했습니다. 이는 일반적으로 소프트웨어 버그나 서비스 중단으로 인해 발생 합니다.  <br/> |
| `parserinputsize` <br/> |파서가 처리할 수 없는 첨부 파일이 너무 커서 해당 첨부 파일의 구문 분석이 발생 하지 않았거나 완료 되지 않았습니다.  <br/> |
| `parsermalformed` <br/> |첨부 파일이 잘못 되었거나 파서에서 처리할 수 없습니다. 이 결과는 이전 파일 형식, 호환 되지 않는 소프트웨어에서 만든 파일 또는 요청 되지 않은 것으로 가장 된 바이러스로 인해 발생 합니다.  <br/> |
| `parseroutputsize` <br/> |첨부 파일의 구문 분석 출력이 너무 커서 잘렸습니다.  <br/> |
| `parserunknowntype` <br/> |Office 365에서 검색할 수 없는 파일 형식을 첨부 한 경우  <br/> |
| `parserunsupportedtype` <br/> |Office 365에서 검색할 수 있는 파일 형식이 첨부 되었지만 해당 파일 형식이 지원 되지 않는 구문 분석  <br/> |
| `propertytoobig` <br/> |Exchange 스토어의 전자 메일 속성 값이 너무 커서 검색할 수 없으며 메시지를 처리할 수 없습니다. 일반적으로 전자 메일 메시지의 body 속성에만 발생 합니다.  <br/> |
| `retrieverrms` <br/> |콘텐츠 검색기에서 RMS 보호 메시지를 디코딩하지 못했습니다.  <br/> |
| `wordbreakertruncated` <br/> |색인 중에 너무 많은 단어가 문서에 식별 되었습니다. 제한에 도달 하면 속성 처리가 중지 되 고 속성이 잘립니다.  <br/> |
   
오류 필드에는 오류 태그 필드에 나열 된 처리 오류의 영향을 받는 필드에 대 한 설명이 나와 있습니다. 또는 `subject` `participants`와 같은 속성을 검색 하는 경우 메시지 본문의 오류는 검색 결과에 영향을 주지 않습니다. 이는 추가로 조사 해야 하는 부분적으로 인덱싱된 항목을 정확히 결정할 때 유용할 수 있습니다.
  
## <a name="using-a-powershell-script-to-determine-your-organizations-exposure-to-partially-indexed-email-items"></a>PowerShell 스크립트를 사용 하 여 부분적으로 인덱싱된 전자 메일 항목에 대 한 조직의 노출을 확인

다음 단계에서는 모든 Exchange 사서함의 모든 항목을 검색 하는 PowerShell 스크립트를 실행 한 다음 조직에서 부분적으로 인덱싱된 전자 메일 항목 (개수 및 크기)에 대 한 보고서를 생성 하 고 항목 수를 표시 하는 방법을 보여 줍니다 (및 각 인덱싱 오류가 발생 하는 파일 형식) 이전 섹션의 오류 태그 설명을 사용 하 여 인덱싱 오류를 식별 합니다.
  
1. 파일 이름 접미사. p s 1을 사용 하 여 Windows PowerShell 스크립트 파일에 다음 텍스트를 저장 합니다. 예를 `PartiallyIndexedItems.ps1`들면입니다.

```
  write-host "**************************************************"
  write-host "     Office 365 Security &amp; Compliance Center      " -foregroundColor yellow -backgroundcolor darkgreen
  write-host "   eDiscovery Partially Indexed Item Statistics   " -foregroundColor yellow -backgroundcolor darkgreen
  write-host "**************************************************"
  " " 
  # Create a search with Error Tags Refinders enabled
  Remove-ComplianceSearch "RefinerTest" -Confirm:$false -ErrorAction 'SilentlyContinue'
  New-ComplianceSearch -Name "RefinerTest" -ContentMatchQuery "size>0" -RefinerNames ErrorTags -ExchangeLocation ALL
  Start-ComplianceSearch "RefinerTest"
  # Loop while search is in progress
  do{
      Write-host "Waiting for search to complete..."
      Start-Sleep -s 5
      $complianceSearch = Get-ComplianceSearch "RefinerTest"
  }while ($complianceSearch.Status -ne 'Completed')
  $refiners = $complianceSearch.Refiners | ConvertFrom-Json
  $errorTagProperties = $refiners.Entries | Get-Member -MemberType NoteProperty
  $partiallyIndexedRatio = $complianceSearch.UnindexedItems / $complianceSearch.Items
  $partiallyIndexedSizeRatio = $complianceSearch.UnindexedSize / $complianceSearch.Size
  " "
  "===== Partially indexed items ====="
  "         Total          Ratio"
  "Count    {0:N0}{1:P2}" -f $complianceSearch.Items.ToString("N0").PadRight(15, " "), $partiallyIndexedRatio
  "Size(GB) {0:N2}{1:P2}" -f ($complianceSearch.Size / 1GB).ToString("N2").PadRight(15, " "), $partiallyIndexedSizeRatio
  " "
  Write-Host ===== Reasons for partially indexed items =====
  foreach($errorTagProperty in $errorTagProperties)
  {
      $name = $refiners.Entries.($errorTagProperty.Name).Name
      $count = $refiners.Entries.($errorTagProperty.Name).TotalCount
      $frag = $name.Split("{_}")
      $errorTag = $frag[0]
      $fileType = $frag[1]
      if ($errorTag -ne $lastErrorTag)
      {
          $errorTag
      }
      "    " + $fileType + " => " + $count
      $lastErrorTag = $errorTag
  }
  
```
   
2. [Office 365 보안 &amp; 및 준수 센터 PowerShell에 연결](https://go.microsoft.com/fwlink/p/?linkid=627084)합니다.
    
3. 보안 &amp; 및 준수 센터 PowerShell에서 1 단계에서 스크립트를 저장 한 폴더로 이동한 후 스크립트를 실행 합니다. 예를 들어:

    ```
    .\PartiallyIndexedItems.ps1
    ```
   
스크립트에서 반환 하는 출력의 예는 다음과 같습니다.
  
![조직에서 부분적으로 인덱싱된 전자 메일 항목에 대 한 보고서를 생성 하는 스크립트의 출력 예](media/aeab5943-c15d-431a-bdb2-82f135abc2f3.png)
  
다음에 유의하세요.
  
1. 전자 메일 항목의 총 수와 크기 및 조직의 부분적으로 인덱싱된 전자 메일 항목의 비율 (개수 및 크기)
    
2. 오류 태그와 오류가 발생 한 해당 파일 형식을 나열 합니다.
  
## <a name="see-also"></a>참고 항목

[Office 365의 콘텐츠 검색에서 부분적으로 인덱싱된 항목](partially-indexed-items-in-content-search.md)
