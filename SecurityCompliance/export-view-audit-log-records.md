---
title: 감사 로그 기록 내보내기, 구성 및 보기
ms.author: markjjo
author: markjjo
manager: laurawi
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- Strat_O365_IP
- M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: 0d4d0f35-390b-4518-800e-0c7ec95e946c
description: Office 365 감사 로그 검색 결과를 CSV 파일로 내보내고 다운로드 한 후 Excel의 파워 쿼리 편집기에서 JSON 변환 기능을 사용 하 여 AuditData 열에 있는 JSON 개체의 각 속성을 자체 열로 분할할 수 있습니다. 이를 통해 원하는 특정 감사 데이터를 빠르게 찾을 수 있습니다.
ms.openlocfilehash: 7dac373e8f25ead38dddbe2663e521b35b3153ef
ms.sourcegitcommit: b262d40f6daf06be26e7586f37b736e09f8a4511
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/02/2019
ms.locfileid: "35462939"
---
# <a name="export-configure-and-view-audit-log-records"></a>감사 로그 기록 내보내기, 구성 및 보기

Office 365 감사 로그를 검색 하 고 검색 결과를 CSV 파일로 다운로드 한 후 해당 파일에는 각 이벤트에 대 한 추가 정보를 포함 하는 **Auditdata**라는 열이 포함 되어 있습니다. 이 열의 데이터는 JSON 개체로 형식이 지정 되며,이 개체는 쉼표로 구분 된 *값* 쌍으로 구성 된 여러 속성을 포함 합니다. Excel의 파워 쿼리 편집기에서 JSON 변환 기능을 사용 하 여 각 속성에 자체 열이 포함 되도록 **Auditdata** 열에 있는 json 개체의 각 속성을 여러 열로 분할할 수 있습니다. 이를 통해 이러한 속성 중 하나 이상을 정렬 및 필터링 하 여 원하는 특정 감사 데이터를 빠르게 찾을 수 있습니다.

## <a name="step-1-export-audit-log-search-results"></a>1 단계: 감사 로그 검색 결과 내보내기

첫 번째 단계는 감사 로그를 검색 한 다음 CSV (쉼표로 구분 된 값) 파일의 결과를 로컬 컴퓨터로 내보내는 것입니다.
  
1. [감사 로그 검색](search-the-audit-log-in-security-and-compliance.md#search-the-audit-log) 을 실행 하 고 필요한 경우 원하는 결과를 얻을 때까지 검색 조건을 수정 합니다.
    
2. **결과 내보내기를** 클릭 하 고 **모든 결과 다운로드**를 선택 합니다. 
    
   ![모든 결과 다운로드를 클릭 합니다.](media/ExportAuditSearchResults.png)

   이 옵션을 선택 하면 1 단계에서 실행 한 감사 로그 검색의 모든 감사 레코드를 내보내고, 감사 로그의 원시 데이터를 CSV 파일로 다운로드 합니다. 

   CSV 파일을 열거나 저장 하 라는 메시지가 창 맨 아래에 표시 됩니다. 

3. **저장 > 다른 이름으로 저장** 을 클릭 하 여 로컬 컴퓨터에 CSV 파일을 저장 합니다. 많은 검색 결과를 다운로드 하는 데 시간이 오래 걸립니다. 이는 일반적으로 모든 작업을 검색 하는 경우 또는 광범위 한 날짜 범위에 해당 합니다. CSV 파일의 다운로드가 완료 되 면 windows 아래쪽에 메시지가 표시 됩니다.
 
   ![CSV 파일 다운로드가 완료 되 면 표시 되는 메시지](media/ExportAuditSearchResultsFinish.png)

> [!NOTE]
  > 단일 감사 로그 검색에서 최대 5만 개의 항목을 CSV 파일에 다운로드할 수 있습니다. 5만 항목이 CSV 파일에 다운로드 되는 경우 검색 조건을 충족 하는 이벤트가 5만 개 보다 많은 것으로 간주할 수 있습니다. 이 제한 보다 많은 시간을 내보내려면 날짜 범위를 사용 하 여 감사 로그 레코드 수를 줄이십시오. 5만 개 보다 많은 항목을 내보내려면 날짜 범위가 더 작은 검색을 여러 개 실행 해야 할 수 있습니다.

## <a name="step-2-format-the-exported-audit-log-using-the-power-query-editor"></a>2 단계: 파워 쿼리 편집기를 사용 하 여 내보낸 감사 로그 서식 지정

다음 단계에서는 Excel의 파워 쿼리 편집기에서 JSON 변환 기능을 사용 하 여 **Auditdata** 열에 있는 json 개체의 각 속성을 자체 열로 분할 합니다. 그런 다음 특정 속성의 값을 기반으로 레코드를 볼 수 있도록 열을 필터링 합니다. 이를 통해 원하는 특정 감사 데이터를 빠르게 찾을 수 있습니다.

1. Excel에서 Office 365, Excel 2019 또는 Excel 2016의 빈 통합 문서를 엽니다.
    
2.  **데이터** 탭의 **& 변환 데이터 가져오기** 리본 그룹에서 **텍스트/CSV를**클릭 합니다.

    ![데이터 탭에서 Text/CSV를 클릭 합니다.](media/JSONTransformOpenCSVFile.png)

3. 1 단계에서 다운로드 한 CSV 파일을 엽니다.
    
4. 표시 된 창에서 **데이터 변환을**클릭 합니다.

   ![데이터 변환 클릭](media/JSONOpenPowerQuery.png)

CSV 파일이 **쿼리 편집기**에서 열립니다. **CreationDate**, **UserIds**, **Operations**및 **auditdata**의 네 가지 열이 있습니다. **Auditdata** 열은 여러 속성을 포함 하는 JSON 개체입니다. 다음 단계에서는 JSON 개체의 각 속성에 대 한 열을 만듭니다.
    
5. **Auditdata** 열에서 제목을 마우스 오른쪽 단추로 클릭 하 고 **변환**, **JSON**을 차례로 클릭 합니다. 
 
   ![AuditData 열을 마우스 오른쪽 단추로 클릭 하 고 변환, JSON을 차례로 선택 합니다.](media/JSONTransform.png)

6. **Auditdata** 열의 오른쪽 위 모서리에서 확장 아이콘을 클릭 합니다.
    
   ![AuditData 열에서 확장 아이콘](media/JSONTransformExpandIcon.png)

   **Auditdata** 열에 있는 JSON 개체의 속성 중 일부 목록이 표시 됩니다.

7. 모두 **로드** 를 클릭 하 여 **AUDITDATA** 열에 JSON 개체의 모든 속성을 표시 합니다.

   ![JSON 개체에 모든 속성을 표시 하려면 추가를 클릭 합니다.](media/JSONTransformLoadJSONProperties.png)

   포함 하지 않을 속성 옆의 확인란을 선택 취소할 수 있습니다. 조사에 도움이 되지 않는 열을 제거 하는 것은 감사 로그에 표시 되는 데이터의 양을 줄이는 좋은 방법입니다. 

   > [!NOTE]
   > 이전 스크린샷에 표시 된 JSON 속성 ( **더 이상 로드**를 클릭 한 후)은 CSV 파일의 첫 번째 1000 행에서 **auditdata** 열에 있는 속성을 기반으로 합니다. 첫 번째 1000 행 다음의 레코드에 다른 JSON 속성이 있는 경우에는 **Auditdata** 열이 여러 열로 분할 될 때 이러한 속성 및 해당 열이 포함 되지 않습니다. 이를 방지 하기 위해 감사 로그 검색을 다시 실행 하 고 검색 조건을 좁혀 더 작은 레코드가 반환 되도록 하는 것이 좋습니다. 또 다른 해결 방법은 **Auditdata** 열에서 JSON 개체를 변환 하기 전에 **작업** 열에서 항목을 필터링 하 여 행 수 (위의 5 단계를 수행 하기 전)를 줄이기 위한 것입니다.

8. 다음 중 하나를 수행 하 여 선택 된 각 JSON 속성에 추가 되는 열의 제목에 서식을 지정 합니다.

    - JSON 속성 이름을 열 이름으로 사용 하려면 **원래 열 이름을 접두사로 사용** 확인란의 선택을 취소 합니다. 예를 들어 **RecordType** 또는 **sourcefilename**을 사용할 때
    
   - 열 이름에 AuditData 접두사를 추가 하려면 **원래 열 이름을 접두사로 사용** 확인란을 선택 된 상태로 유지 합니다. 예를 들어, **Auditdata** 또는 **Auditdata. sourcefilename**을 사용할 때

9. **확인**을 클릭합니다.
    
    **Auditdata** 열은 여러 열로 분할 됩니다. 각각의 새 열은 AuditData JSON 개체의 속성에 해당 합니다. 열의 각 행에는 속성의 값이 들어 있습니다. 속성에 값이 포함 되어 있지 않으면 *null* 값이 표시 됩니다. Excel에서 null 값이 있는 셀은 비어 있습니다.
  
10. **홈** 탭에서 **& 로드 닫기를** 클릭 하 여 파워 쿼리 편집기를 닫고 Excel 통합 문서에서 변환 된 CSV 파일을 엽니다. 

## <a name="tips-for-exporting-and-viewing-the-audit-log"></a>감사 로그 내보내기 및 보기에 대 한 팁

다음은 JSON 변환 기능을 사용 하 여 **Auditdata** 열을 여러 열로 분할 하기 전과 수행한 후의 감사 로그 내보내기 및 보기에 대 한 몇 가지 팁과 예입니다.

- **RecordType** 열을 필터링 하 여 특정 Office 365 서비스 또는 기능 영역의 레코드만 표시 합니다. 예를 들어 SharePoint 공유와 관련 된 이벤트를 표시 하려면 **14** (SharePoint 공유 활동에서 트리거된 레코드의 enum 값)를 선택 합니다. **RecordType** 열에 표시 된 열거형 값에 해당 하는 office 365 서비스의 목록은 [office 365 감사 로그의 자세한 속성](detailed-properties-in-the-office-365-audit-log.md)을 참조 하십시오.

- **작업** 열을 필터링 하 여 특정 활동에 대 한 레코드를 표시 합니다. 보안 & 준수 센터의 감사 로그 검색 도구에서 검색 가능한 활동에 해당 하는 대부분의 작업 목록을 보려면 [보안 & 준수 센터에서 감사 로그 검색](search-the-audit-log-in-security-and-compliance.md#audited-activities)의 "감사 된 작업" 섹션을 참조 하십시오.

- 보안 & 준수 센터에서 감사 로그 검색 도구를 사용 하는 대신 Exchange Online Powershell의 [search-unifiedauditlog](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-audit/search-unifiedauditlog) cmdlet을 사용 하 여 Office 365 감사 로그 검색의 결과를 CSV 파일로 내보낼 수 있습니다. 그런 다음 2 단계에서 설명한 것과 같은 절차에 따라 파워 쿼리 편집기를 사용 하 여 감사 로그를 포맷할 수 있습니다. PowerShell cmdlet을 사용 하는 경우의 한 가지 이점은 *RecordType* 매개 변수를 사용 하 여 특정 Office 365 서비스에서 이벤트를 검색할 수 있다는 것입니다. 다음은 PowerShell을 사용 하 여 감사 레코드를 CSV 파일로 내보낸 다음, 파워 쿼리 편집기를 사용 하 여 **Auditdata** 열에 있는 JSON 개체를 2 단계에 설명 된 대로 변환할 수 있는 몇 가지 예입니다.

   이 예제에서는 다음 명령을 실행 하 여 SharePoint 공유 작업과 관련 된 모든 레코드를 반환 합니다. 
   
   ```
   $auditlog = Search-UnifiedAuditLog -StartDate 06/01/2019 -EndDate 06/30/2019 -RecordType SharePointSharingOperation
   ```

   ```
   $auditlog | Select-Object -Property CreationDate,UserIds,RecordType,AuditData | Export-Csv -Path c:\AuditLogs\PowerShellAuditlog.csv -NoTypeInformation
   ```

   - 검색 결과는 CreationDate, UserIds, RecordType, AuditData와 같은 네 개의 열이 포함 된 *PowerShellAuditlog* 라는 CSV 파일로 내보내집니다.

   - 레코드 종류의 이름 또는 열거형 값을 *RecordType* 매개 변수의 값으로 사용할 수 있습니다. 레코드 유형 이름 및 해당 열거형 값의 목록은 *AuditLogRecordType* Table in [Office 365 Management Activity API schema](https://docs.microsoft.com/office/office-365-management-api/office-365-management-activity-api-schema#enum-auditlogrecordtype---type-edmint32)를 참조 하십시오.
   
   - 이 매개 변수에는 단일 값만 포함할 수 있습니다. 다른 레코드 종류에 대 한 감사 레코드를 검색 하려면 이전 두 명령을 다시 실행 하 여 다른 레코드 종류를 지정 하 고 해당 결과를 원래의 CSV 파일에 추가 해야 합니다. 예를 들어 다음 두 명령을 실행 하 여 동일한 날짜 범위의 SharePoint 파일 활동을 PowerShellAuditlog 파일에 추가 합니다.

       ```
      $auditlog = Search-UnifiedAuditLog -StartDate 06/01/2019 -EndDate 06/30/2019 -RecordType SharePointFileOperation
      ```

      ```
      $auditlog | Select-Object -Property CreationDate,UserIds,RecordType,AuditData | Export-Csv -Append -Path c:\AuditLogs\PowerShellAuditlog.csv -NoTypeInformation
      ```
