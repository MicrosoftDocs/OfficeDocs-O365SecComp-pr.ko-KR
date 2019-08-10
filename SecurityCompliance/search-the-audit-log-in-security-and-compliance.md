---
title: 보안 및 준수 센터에서 감사 로그 검색
ms.author: markjjo
author: markjjo
manager: laurawi
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Priority
ms.collection:
- Strat_O365_IP
- M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: 0d4d0f35-390b-4518-800e-0c7ec95e946c
description: '보안 및 준수 센터를 사용하여 통합 감사 로그를 검색해 Office 365 조직의 사용자 및 관리자 활동을 확인합니다. '
ms.openlocfilehash: 79309a2145db53f38d5d3c3c29777571d56910ae
ms.sourcegitcommit: 6122eb026c558a5126c40845e656fbb0c40cb32a
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/06/2019
ms.locfileid: "36165694"
---
# <a name="search-the-audit-log-in-the-security--compliance-center"></a>보안 및 준수 센터에서 감사 로그 검색

## <a name="introduction"></a>소개

사용자가 특정 문서를 보았는지 또는 사서함에서 항목을 제거했는지 확인해야 하나요? 이 경우 Office 365 보안 &amp; 준수 센터를 사용하여 통합 감사 로그를 검색해 Office 365 조직의 사용자 및 관리자 활동을 확인합니다. 통합된 감사 로그를 사용하는 이유는 무엇일까요? Office 365에서 다음과 같은 유형의 사용자 및 관리자 활동을 검색할 수 있기 때문입니다.
  
- SharePoint Online 및 비즈니스용 OneDrive의 사용자 활동
    
- Exchange Online(Exchange 사서함 감사 로깅)의 사용자 활동
  
- SharePoint Online의 관리 활동
    
- Azure Active Directory(Office 365용 디렉터리 서비스)의 관리자 활동
    
- Exchange Online(Exchange 관리자 감사 로깅)의 관리자 활동
    
- Sway의 사용자 및 관리자 활동
    
- 보안 및 준수 센터에서 eDiscovery 활동
    
- Power BI의 사용자 및 관리자 활동
    
- Microsoft Teams의 사용자 및 관리자 활동

- Dynamics 365의 사용자 및 관리자 활동
    
- Yammer의 사용자 및 관리자 활동
 
- Microsoft Flow의 사용자 및 관리자 활동
    
- Microsoft Stream의 사용자 및 관리자 활동

- Microsoft Workplace Analytics의 분석가 및 관리자 활동

- Microsoft PowerApps의 사용자 및 관리자 활동
    
   
## <a name="before-you-begin"></a>시작하기 전에

Office 365 감사 로그의 검색을 시작하기 전에 반드시 아래 내용을 읽어 보시기 바랍니다.
  
- 먼저 관리자(또는 또 다른 관리자)가 감사 로깅을 켜야 Office 365 감사 로그를 검색할 수 있습니다. 감사 로깅을 켜려면 보안 및 준수 센터의 **감사 로그 검색** 페이지에서 **사용자 및 관리자 활동 기록 시작**을 클릭하기만 하면 됩니다. (이 링크가 표시되지 않으면 조직에 대해 감사가 이미 켜져 있는 것입니다.) 감사 로깅을 켜면 감사 로그를 준비 중이며 준비가 완료된 후 두 시간 내에 검색을 실행할 수 있다는 메시지가 표시됩니다. 이 작업은 한 번만 수행하면 됩니다. 
    
    > [!NOTE]
    > 현재 기본적으로 감사가 켜지도록 구현 중입니다. 해당 기능이 구현될 때까지 앞에서 설명한 단계에 따라 직접 켜시기 바랍니다. 
  
- Office 365 감사 로그를 검색하려면 Exchange Online에서 보기 전용 감사 로그 또는 감사 로그 역할이 할당되어야 합니다. 기본적으로 이러한 역할은 Exchange 관리 센터의 **사용 권한** 페이지에서 규정 준수 관리 및 조직 관리 역할 그룹에 할당됩니다. 참고 Office 365 및 Microsoft 365의 전역 관리자는 자동으로 Exchange Online 서비스에서 조직 관리 역할 그룹의 구성원이 됩니다. 최소 권한 수준을 사용하여 Office 365 감사 로그를 검색할 수 있는 권한을 사용자에게 제공하려면 Exchange Online에서 사용자 지정 역할 그룹을 만들고 보기 전용 감사 로그 또는 감사 로그 역할을 추가한 다음 새 역할 그룹의 구성원으로 사용자를 추가할 수 있습니다. 자세한 내용은 [Exchange Online에서 역할 그룹 관리](https://go.microsoft.com/fwlink/p/?LinkID=730688)를 참조하세요.
    
    > [!IMPORTANT]
    > 보안 및 준수 센터의 **사용 권한** 페이지에서 사용자에게 보기 전용 감사 로그 또는 감사 로그 역할을 할당하는 경우 Office 365 감사 로그를 검색할 수 없습니다. Exchange Online에서 사용 권한을 할당해야 합니다. 감사 로그를 검색하는 데 사용되는 기본 cmdlet이 Exchange Online cmdlet이기 때문입니다. 
  
- 사용자 또는 관리자가 감사되는 활동을 수행하면 감사 레코드가 생성되어 조직의 Office 365 감사 로그에 저장됩니다. 감사 기록이 보존되고 감사 로그에서 검색 가능한 시간은 Office 365 구독, 특히 특정 사용자에게 할당된 라이선스 유형에 따라 다릅니다.

     - **Office 365 E3:** 감사 레코드는 90일간 보존됩니다. 즉, 감사 로그에서 최근 90일 내에 수행된 활동을 검색할 수 있습니다.  

     - **Office 365 E5:** 감사 레코드는 90일간 보존됩니다. 결국에는 E5 사용자, E3 라이선스, Office 365 Advanced Compliance 애드온 라이선스를 보유한 사용자는 1년 동안 감사 레코드를 보유할 수 있을 것입니다.

        > [!NOTE]
        > E5 조직(또는 Advanced Compliance 애드온 라이선스가 있는 E3 조직의 사용자)에 대한 감사 레코드의 1년 보존 기간에 대한 개인 미리보기 프로그램은 새 등록이 마감되었습니다. 이 문서는 1년 보존 기간이 공개 미리보기로 제공되거나 일반용으로 출시될 때 업데이트됩니다.

- 조직에서 Office 365 감사 로그 검색을 해제하려면 Exchange Online 조직에 연결된 원격 PowerShell에서 다음과 같은 명령을 실행하세요.
    
  ```
  Set-AdminAuditLogConfig -UnifiedAuditLogIngestionEnabled $false
  ```

    감사 검색을 다시 설정하기 위해 Exchange Online PowerShell에서 다음 명령을 실행할 수 있습니다.
    
  ```
  Set-AdminAuditLogConfig -UnifiedAuditLogIngestionEnabled $true
  ```

    자세한 내용은 [Office 365의 감사 로그 검색 해제](turn-audit-log-search-on-or-off.md)를 참조하세요.
    
- 이전에 설명한 것처럼, 감사 로그를 검색하는 데 사용되는 기본 cmdlet은 **Search-UnifiedAuditLog**인 Exchange Online cmdlet입니다. 즉 보안 및 준수 센터의 **감사 로그 검색** 페이지를 사용하는 대신 이 cmdlet을 사용하여 Office 365 감사 로그를 검색할 수 있습니다. Exchange Online 조직에 연결된 원격 PowerShell에서 이 cmdlet을 실행해야 합니다. 자세한 내용은 [Search-UnifiedAuditLog](https://go.microsoft.com/fwlink/p/?linkid=834776)를 참조하세요. 

    **Search-UnifiedAuditLog** cmdlet에서 반환되는 검색 결과를 CSV 파일로 내보내는 방법에 대한 자세한 내용은 [감사 로그 레코드 내보내기, 구성 및 보기](export-view-audit-log-records.md#tips-for-exporting-and-viewing-the-audit-log)의 "감사 로그 내보내기 및 보기 팁" 섹션을 참조하세요.  

- Office 365 감사 로그에서 프로그래밍 방식으로 데이터를 다운로드하려면 PowerShell 스크립트를 사용하는 대신 Office 365 관리 작업 API를 사용하는 것이 좋습니다. Office 365 관리 작업 API는 조직의 작업, 보안 및 규정 준수 모니터링 솔루션을 개발하는 데 사용할 수 있는 REST 웹 서비스입니다. 자세한 내용은 [Office 365 관리 작업 API 참조](https://docs.microsoft.com/office/office-365-management-api/office-365-management-activity-api-reference)를 참조하세요.
    
- 검색 결과에 해당 감사 로그 항목이 표시되려면 이벤트 발생 시점으로부터 30분에서 24시간 정도 걸릴 수 있습니다. 다음 표에는 Office 365의 여러 서비스가 표시되는 데 걸리는 시간이 나와 있습니다.
    
    |**Office 365 서비스**|**30분**|**24시간**|
    |:-----|:-----|:-----|
    |고급 위협 방지 및 위협 인텔리전스  <br/> |![확인 표시](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)| |
    |Azure Active Directory(사용자 로그인 이벤트)  <br/> ||![확인 표시](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)           <br/> |
    |Azure Active Directory(관리 이벤트)  <br/> ||![확인 표시](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png) |
    |데이터 손실 방지  <br/> |![확인 표시](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)       <br/>| |
    |Dynamics 365 CRM <br/> |![확인 표시](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)           <br/>| |
    |eDiscovery  <br/> |![확인 표시](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)           <br/>| |
    |Exchange Online  <br/> |![확인 표시](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)           <br/> ||
    |Microsoft Flow  <br/> |![확인 표시](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)           <br/>| |
    |Microsoft Project  <br/> |![확인 표시](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)           <br/>| |
    |Microsoft Stream  <br/> |![확인 표시](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)           <br/>| |
    |Microsoft Teams  <br/> |![확인 표시](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)           <br/> ||
    |Power BI  <br/> |![확인 표시](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)           <br/>| |
    |보안 및 준수 센터  <br/> |![확인 표시](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)           <br/> ||
    |SharePoint Online 및 비즈니스용 OneDrive  <br/> |![확인 표시](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)           <br/> ||
    |Sway  <br/> ||![확인 표시](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)           <br/> |
    |Workplace Analytics<br/> |![확인 표시](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)           <br/> || 
    |Yammer  <br/> ||![확인 표시](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)           <br/> |
   
- Azure A (azure Active Directory)는 Office 365의 디렉터리 서비스입니다. 통합 감사 로그에는 Microsoft 365 관리 센터 또는 Azure 관리 포털에서 수행된 사용자, 그룹, 응용 프로그램, 도메인 및 디렉터리 활동이 포함됩니다. Azure AD 이벤트의 전체 목록은 [Azure Active Directory 감사 보고서 이벤트](https://go.microsoft.com/fwlink/p/?LinkID=616549)를 참조하세요.
    
- Power BI에 대 한 감사 로깅은 기본적으로 사용하지 않도록 설정되어 있습니다. Office 365 감사 로그에서 Power BI 작업을 검색하려면 Power BI 관리 포털에서 감사를 사용하도록 설정해야 합니다. 자세한 내용은 [Power BI 관리 포털](https://docs.microsoft.com/power-bi/service-admin-portal#audit-logs)의 "감사 로그" 섹션을 참조 하세요.
    
    
## <a name="search-the-audit-log"></a>감사 로그 검색

Office 365에서 감사 로그를 검색하는 과정은 다음과 같습니다. 
  
[1단계: 감사 로그 검색 실행](#step-1-run-an-audit-log-search)
  
[2단계: 검색 결과 보기](#step-2-view-the-search-results)

[3단계: 검색 결과 필터링](#step-3-filter-the-search-results)

[4단계: 검색 결과를 파일로 내보내기](#step-4-export-the-search-results-to-a-file)



  
### <a name="step-1-run-an-audit-log-search"></a>1단계: 감사 로그 검색 실행

1. [https://protection.office.com](https://protection.office.com)으로 이동합니다.
    
    > [!TIP]
    > 비공개 브라우징 세션(일반 세션이 아님)을 사용하여 보안 및 준수 센터에 액세스하면 현재 로그온한 자격 증명을 사용할 수 없으므로 비공개 브라우징 세션을 사용하세요. Internet Explorer 또는 Microsoft Edge에서 InPrivate 브라우징 세션을 열려면 CTRL+SHIFT+P를 누릅니다. Google Chrome에서 비공개 브라우징 세션을 열려면(incognito 창이라고 함) CTRL+SHIFT+N을 누릅니다. 
  
2. 회사 또는 학교 계정을 사용하여 Office 365에 로그인합니다.
    
3. 보안 및 준수 센터의 왼쪽 창에서 **검색**을 클릭한 다음 **감사 로그 검색**을 클릭합니다.
    
    **감사 로그 검색** 페이지가 표시됩니다. 
    
    ![조건을 구성한 다음 검색을 클릭하여 보고서를 실행합니다.](media/8639d09c-2843-44e4-8b4b-9f45974ff7f1.png)
  
    > [!NOTE]
    > 먼저 감사 로깅을 켜야 감사 로그 검색을 실행할 수 있습니다. **사용자 및 관리자 활동 기록 시작** 링크가 표시되면 클릭하여 감사를 켭니다. 이 링크가 표시되지 않으면 조직에 대해 감사가 이미 켜져 있는 것입니다. 
  
4. 다음과 같은 검색 조건을 구성합니다. 
    
    a. **활동** 드롭다운 목록을 클릭하여 검색할 수 있는 활동을 표시합니다. 사용자 및 관리자 활동은 관련 활동 그룹으로 구성되어 있습니다. 특정 활동을 선택하거나, 활동 그룹 이름을 클릭하여 그룹의 모든 활동을 선택할 수 있습니다. 선택한 활동을 클릭하여 선택을 취소할 수도 있습니다. 검색을 실행하면 선택한 활동에 대한 감사 로그 항목만 표시됩니다. **모든 활동에 대한 결과 표시**를 선택하면 선택한 사용자 또는 사용자 그룹이 수행한 모든 활동에 대한 결과가 표시됩니다. 
    
    100개가 넘는 사용자 및 관리자 활동이 Office 365 감사 로그에 기록됩니다. 여러 Office 365 서비스의 각 활동에 대한 설명을 보려면 이 문서의 항목에서 **감사되는 활동** 탭을 클릭합니다. 
    
    b. **시작 날짜** 및 ** 날짜** 기본적으로 최근 7일이 선택됩니다. 날짜 및 시간 범위를 선택하여 해당 기간 내에 발생한 이벤트를 표시합니다. 날짜 및 시간은 UTC(협정 세계시) 형식으로 표시됩니다. 지정할 수 있는 최대 날짜 범위는 90일입니다. 선택한 날짜 범위가 90일보다 크면 오류가 표시됩니다. 
    
    > [!TIP]
    > 최대 날짜 범위인 90일을 사용하는 경우 **시작 날짜**에 대해 현재 시간을 선택합니다. 그러지 않으면 시작 날짜가 종료 날짜보다 이전이라는 오류가 표시됩니다. 최근 90일 내에 감사를 켠 경우 최대 날짜 범위가 감사를 켠 날짜 이전에 시작할 수 없습니다. 
  
    c. **사용자** 이 상자 안을 클릭하고 검색 결과를 표시할 사용자를 하나 이상 선택합니다. 이 상자에서 선택한 사용자가 수행한 선택한 활동에 대한 감사 로그 항목이 결과 목록에 표시됩니다. 조직의 모든 사용자(및 서비스 계정)에 대한 항목을 반환하려면 이 상자를 비워 둡니다. 
    
    d. **파일, 폴더 또는 사이트** 파일이나 폴더 이름의 일부 또는 전체를 입력하여 지정한 키워드를 포함하는 파일이나 폴더와 관련된 활동을 검색합니다. 파일 또는 폴더의 URL을 지정할 수도 있습니다. URL을 사용하는 경우 전체 URL 경로를 입력하거나 URL의 일부만 입력하는 경우 특수 문자나 공백을 포함하지 마세요. 
    
    조직의 모든 파일 및 폴더에 대한 항목을 반환하려면 이 상자를 비워 둡니다.
    
   **TIPS**

   - **사이트**와 관련된 모든 활동을 찾으려면 URL 뒤에 와일드 카드 기호 (\*)를 추가하여 해당 사이트의 모든 항목을 반환합니다. 예를 들어 **"https://contoso-my.sharepoint.com/personal/*"** 가 있습니다.

   - **파일**과 관련된 모든 활동을 찾으려면 파일 이름 앞에 와일드 카드 기호 (\*)를 추가하여 해당 파일의 모든 항목을 반환하십시오. 예를 들어 **"*Customer_Profitability_Sample.csv"** 가 있습니다.
    

    
5. **검색**을 클릭하여 검색 조건을 사용한 검색을 실행합니다.  
    
    검색 결과가 로드되고, 잠시 후에 **결과**에 표시됩니다. 검색이 완료되면 찾은 결과 수가 표시됩니다. **결과** 창에 최대 5000 개의 이벤트가 150 이벤트 단위로 표시 됩니다. 5000개 이상의 이벤트에서 검색 조건을 충족하는 경우에는 최근 5000 이벤트가 표시됩니다. 
    
    ![검색을 완료한 후 결과 수가 표시됩니다.](media/986216f1-ca2f-4747-9480-e232b5bf094c.png)
  
  
#### <a name="tips-for-searching-the-audit-log"></a>감사 로그 검색을 위한 팁

- 활동 이름을 클릭하여 검색할 특정 활동을 선택할 수 있습니다. 또는 그룹 이름을 클릭하여 그룹의 모든 활동(예: **파일 및 폴더 활동**)을 검색할 수도 있습니다. 활동이 선택된 경우 클릭하면 선택을 취소할 수 있습니다. 검색 상자를 사용하여 입력한 키워드를 포함하는 활동을 표시할 수도 있습니다.
    
    ![활동 그룹 이름을 클릭하여 모든 활동을 선택합니다.](media/3cde97cb-6f35-47c0-8612-ecd9c6ac36a3.png)
  
- Exchange 관리자 감사 로그의 항목을 표시하려면 **활동** 목록에서 **모든 활동에 대한 결과 표시**를 선택해야 합니다. 이 감사 로그의 이벤트는 결과의 **활동** 열에 cmdlet 이름(예: **Set-Mailbox**)을 표시합니다. 자세한 내용을 보려면 이 항목에서 **감사되는 활동** 탭을 클릭한 다음 **Exchange 관리 활동** 클릭합니다.
    
    마찬가지로 **활동** 목록에 해당하는 항목이 없는 일부 감사 활동이 있습니다. 이러한 활동에 대한 작업 이름을 알고 있는 경우 모든 활동을 검색한 다음 **활동** 열의 상자에 작업 이름을 입력하여 결과를 필터링할 수 있습니다. 결과 필터링에 대한 자세한 내용은 [3단계: 검색 결과 필터링](#step-3-filter-the-search-results)을 참조하세요. 
    
- **지우기**를 클릭하여 현재 검색 조건을 지웁니다. 날짜 범위가 기본값인 최근 7일로 돌아갑니다. **모든 활동에 대한 결과를 표시하도록 모두 지우기**를 클릭하여 선택한 모든 작업을 취소할 수도 있습니다. 
    
- 5,000개의 결과가 발견되면 검색 조건에 맞는 이벤트가 5,000개 이상 있다고 가정할 수 있습니다. 검색 조건을 구체화한 다음 검색을 다시 실행하여 더 적은 결과를 반환하거나, **결과 내보내기** \> **모든 결과 다운로드**를 선택하여 모든 검색 결과를 내보낼 수 있습니다.

  
### <a name="step-2-view-the-search-results"></a>2단계: 검색 결과 보기

감사 로그 검색 결과는 **감사 로그 검색** 페이지의 **결과**에 표시됩니다. 앞에서 언급한 것처럼 150개 이벤트 단위로 최대 5,000개(최신)의 이벤트가 표시됩니다. 이벤트를 더 표시하려면 **결과** 창에서 스크롤 막대를 사용하거나, **Shift+End**를 눌러 다음 150개의 이벤트를 표시할 수 있습니다. 
  
결과에는 검색에서 반환되는 각 이벤트에 대한 다음 정보가 포함됩니다.
  
- **날짜** 이벤트가 발생한 날짜 및 시간(UTC 형식)입니다. 
    
- **IP 주소** 활동을 기록할 때 사용된 장치의 IP 주소입니다. IP 주소는 IPv4 또는 IPv6 주소 형식으로 표시됩니다. 
    
- **사용자** 이벤트를 트리거한 작업을 수행한 사용자(또는 서비스 계정)입니다. 
    
- **활동** 사용자가 수행한 활동입니다. 이 값은 **활동** 드롭다운 목록에서 선택한 활동에 해당합니다. Exchange 관리자 감사 로그의 이벤트에 대한 이 열의 값은 Exchange cmdlet입니다. 
    
- **항목** 해당 활동의 결과로 생성 또는 수정된 개체입니다. 예를 들어 보거나 수정된 파일 또는 업데이트된 사용자 계정입니다. 일부 활동은 이 열에 값이 없습니다. 
    
- **세부 정보** 활동에 대한 추가 정보입니다. 마찬가지로, 일부 활동에는 값이 없습니다. 
    
> [!TIP]
> **결과** 아래의 열 머리글을 클릭하여 결과를 정렬합니다. 결과를 오름차순 또는 내림차순으로 정렬할 수 있습니다. 결과를 가장 오래된 항목에서 최신 항목 순이나 최신 항목에서 가장 오래된 항목 순으로 정렬하려면 **날짜** 머리글을 클릭합니다. 
  
#### <a name="view-the-details-for-a-specific-event"></a>특정 이벤트에 대한 세부 정보 보기

검색 결과 목록에서 이벤트 레코드를 클릭하여 이벤트에 대한 세부 정보를 볼 수 있습니다. 이벤트 레코드의 자세한 속성이 포함된 **세부 정보**페이지가 표시됩니다. 표시되는 속성은 이벤트가 발생한 Office 365 서비스에 따라 다릅니다. 추가 세부 정보를 표시하려면 **추가 정보**를 클릭합니다. 설명은 [Office 365 감사 로그의 자세한 속성](detailed-properties-in-the-office-365-audit-log.md)을 참조하세요.
  
![감사 로그 이벤트 레코드의 자세한 속성을 보려면 추가 정보를 클릭합니다.](media/6df582ae-d339-4735-b1a6-80914fb77a08.png)

  
### <a name="step-3-filter-the-search-results"></a>3단계: 검색 결과 필터링

정렬 외에도 감사 로그 검색 결과를 필터링할 수 있습니다. 특정 사용자 또는 활동에 대한 결과를 빠르게 필터링하는 데 도움이 되는 유용한 기능입니다. 처음에 광범위한 검색을 만든 후 결과를 빠르게 필터링하여 특정 이벤트를 확인할 수 있습니다. 그런 다음 검색 조건 범위를 좁혀서 검색을 다시 실행하여 더 작고 간결한 결과 집합을 반환할 수 있습니다.
  
결과를 필터링하려면
  
1. 감사 로그 검색을 실행합니다.
    
2. 결과가 표시되면 **결과 필터링**을 클릭합니다.
    
    각 열 머리글 아래에 키워드 상자가 표시됩니다.
    
3. 열 머리글 아래에 있는 상자 중 하나를 클릭하고 필터링할 열에 따라 단어 또는 구를 입력합니다. 결과가 동적으로 다시 조정되어 필터와 일치하는 이벤트를 표시합니다.
    
    ![필터와 일치하는 이벤트를 표시하려면 필터에 단어를 입력합니다.](media/542dc323-a997-402c-934b-cc5e218e50bc.png)
  
4. 필터를 지우려면 필터 상자에서 **X**를 클릭하거나 **필터링 숨기기**를 클릭합니다.
    
> [!TIP]
> Exchange 관리자 감사 로그의 이벤트를 표시하려면 **활동** 필터 상자에 **-**(대시)를 입력합니다. Exchange 관리자 이벤트에 대한 **활동** 열에 표시되는 cmdlet 이름이 나타납니다. 그런 다음 cmdlet 이름을 사전순으로 정렬할 수 있습니다. 

### <a name="step-4-export-the-search-results-to-a-file"></a>4단계: 검색 결과를 파일로 내보내기

감사 로그 검색 결과를 로컬 컴퓨터의 CSV(쉼표로 구분된 값) 파일로 내보낼 수 있습니다. Microsoft Excel에서 이 파일을 열고 검색, 정렬, 필터링, 단일 열(여러 속성 포함)을 여러 개의 열로 분할 등의 기능을 사용할 수 있습니다.
  
1. 감사 로그 검색을 실행한 다음 원하는 결과를 얻을 때까지 검색 조건을 수정합니다.
    
2. **결과 내보내기**를 클릭하고 다음 옵션 중 하나를 선택합니다. 
    
     - **로드된 결과 저장** **감사 로그 검색** 페이지의 **결과** 아래에 표시되는 항목만 내보내려면 이 옵션을 선택합니다. 다운로드한 CSV 파일에는 페이지에 표시되는 것과 동일한 열(날짜, 사용자, 활동, 항목 및 세부 정보) 및 데이터가 포함되어 있습니다. CSV 파일에 감사 로그 항목의 추가 정보가 들어 있는 추가 열(**자세히**)이 포함됩니다. **감사 로그 검색** 페이지에 로드되어 표시되는 것과 동일한 결과를 내보내기 때문에 최대 5,000개의 항목이 내보내집니다. 
    
     - **모든 결과 다운로드** Office 365 감사 로그에서 검색 조건에 맞는 항목을 모두 내보내려면 이 옵션을 선택합니다. 검색 결과 집합이 큰 경우 이 옵션을 선택하여 **감사 로그 검색** 페이지에 표시되는 5,000개의 감사 레코드뿐 아니라 감사 로그의 모든 항목을 다운로드합니다. 이 옵션은 감사 로그의 원시 데이터를 CSV 파일로 다운로드하며 감사 로그 항목의 추가 정보를 **AuditData** 열에 포함합니다. 파일이 다른 옵션을 선택할 경우 다운로드되는 파일보다 훨씬 더 클 수 있기 때문에 이 내보내기 옵션을 선택할 경우 파일을 다운로드하는 데 오래 걸릴 수 있습니다.
    
       > [!IMPORTANT]
       > 단일 감사 로그 검색에서 최대 50,000의 항목을 CSV 파일로 다운로드할 수 있습니다. 50,000개의 항목이 CSV 파일로 다운로드되면 검색 조건에 맞는 이벤트가 50,000개 이상 있다고 가정할 수 있습니다. 이 제한보다 많은 항목을 내보내려면 날짜 범위를 사용하여 감사 로그 항목 수를 줄이세요. 50,000개 이상의 항목을 내보내기 위해 더 작은 날짜 범위로 여러 번 검색을 실행해야 할 수 있습니다. 
  
3. 내보내기 옵션을 선택하면 CSV 파일을 열지, 다운로드 폴더에 저장할지 또는 특정 폴더에 저장할지를 묻는 메시지가 창의 맨 아래에 표시됩니다.
 
#### <a name="more-information-about-exporting-and-viewing-audit-log-search-results"></a>감사 로그 검색 결과 내보내기 및 보기에 대한 추가 정보

- 모든 검색 결과를 다운로드하는 경우 CSV 파일에 각 이벤트에 대한 추가 정보가 들어 있는 **AuditData** 열이 포함됩니다. 이 열의 데이터는 감사 로그 레코드의 여러 속성을 포함하는 JSON 개체로 구성됩니다. JSON 각 *개체 속성: 값* 쌍은 쉼표로 구분됩니다. Excel의 파워 쿼리 편집기에서 JSON transform 도구를 사용하여 **AuditData** 열을 여러 개의 열로 분할하여 JSON 개체의 각 속성에 고유한 열을 지정할 수 있습니다. 이렇게 하면 하나 이상의 속성을 기준으로 정렬 및 필터링할 수 있습니다. 파워 쿼리 편집기를 사용하여 JSON 개체를 변환한 단계별 지침을 보려면 [감사 로그 레코드 내보내기, 구성 및 보기](export-view-audit-log-records.md)를 참조하세요.
    
    **AuditData** 열을 분할한 후 **작업** 열을 기준으로 필터링하여 특정 유형의 활동에 대한 자세한 속성을 표시할 수 있습니다. 
    
- **모든 결과 다운로드** 옵션은 Office 365 감사 로그의 원시 데이터를 CSV 파일로 다운로드합니다. 이 파일에는 **로드된 결과 저장** 옵션을 선택할 경우 다운로드되는 파일과 다른 열 이름(CreationDate, UserIds, Operation, AuditData)이 포함됩니다. 동일한 활동에 대한 두 개의 다른 CSV 파일에 있는 값도 서로 다를 수 있습니다. 예를 들어 CSV 파일의 **작업** 열에 있는 활동은 **감사 로그 검색** 페이지의 **활동** 열에 표시되는 "사용자에게 친숙한" 버전과 다른 값을 가질 수 있습니다. (예: MailboxLogin 및 사서함에 로그인한 사용자)

- 다양한 Office 365 서비스의 이벤트를 포함하는 검색 쿼리의 모든 결과를 다운로드하는 경우 CSV 파일의 **AuditData** 열에 작업을 수행한 서비스에 따라 서로 다른 속성이 포함됩니다. 예를 들어 Exchange 및 Azure AD 감사 로그의 항목에는 작업 성공 여부를 나타내는 **ResultStatus** 속성이 포함됩니다. SharePoint의 이벤트에 대해서는 이 속성이 포함되지 않습니다. 마찬가지로, SharePoint 이벤트에는 파일 및 폴더 관련 활동의 사이트 URL을 식별하는 속성이 있습니다. 이 동작을 완화하려면 다른 검색을 사용하여 단일 서비스의 활동에 대한 결과를 내보내는 것이 좋습니다. 
    
    모든 결과를 다운로드할 때 CSV 파일의 **AuditData** 열에 나열되는 여러 속성에 대한 설명은 [Office 365 감사 로그의 자세한 속성](detailed-properties-in-the-office-365-audit-log.md)을 참조하세요.

## <a name="audited-activities"></a>감사되는 활동

이 섹션의 표에서는 Office 365에서 감사되는 활동에 대해 설명합니다. 보안 및 준수 센터에서 감사 로그를 검색하여 이러한 이벤트를 검색할 수 있습니다.
  
표에는 관련 활동 또는 특정 Office 365 서비스의 활동이 그룹화되어 표시됩니다. 표에는 **활동** 드롭다운 목록에 표시되는 이름과 감사 레코드의 상세 정보에 표시되는 해당 작업의 이름과 검색 결과를 내보낼 때 CSV 파일에 표시되는 이름이 포함되어 있습니다. 자세한 정보에 대한 설명은 [Office 365 감사 로그의 자세한 속성](detailed-properties-in-the-office-365-audit-log.md)을 참조하세요.
  
특정 표로 이동하려면 아래 링크 중 하나를 클릭합니다.
  
||||
|:-----|:-----|:-----|
|[파일 및 페이지 활동](#file-and-page-activities)<br/> |[폴더 활동](#folder-activities)<br/> |[SharePoint 목록 활동](#sharepoint-list-activities)<br/>|
|[공유 및 액세스 요청 활동](#sharing-and-access-request-activities)<br/> |[동기화 활동](#synchronization-activities)<br/> |[사이트 사용 권한 활동](#site-permissions-activities)<br/> |
|[사이트 관리 활동](#site-administration-activities)<br/> |[Exchange 사서함 활동](#exchange-mailbox-activities)<br/> |[Sway 활동](#sway-activities) <br/> |
|[사용자 관리 활동](#user-administration-activities) <br/> |[Azure AD 그룹 관리 활동](#azure-ad-group-administration-activities) <br/> |[응용 프로그램 관리 활동](#application-administration-activities) <br/> |
|[역할 관리 활동](#role-administration-activities) <br/> |[디렉터리 관리 활동](#directory-administration-activities) <br/>|[eDiscovery 활동](#ediscovery-activities) <br/> |
|[고급 eDiscovery 활동](#advanced-ediscovery-activities)<br/> |[Power BI 활동](#power-bi-activities) <br/> |[Microsoft Workplace Analytics](#microsoft-workplace-analytics-activities)<br/>|
|[Microsoft Teams 활동](#microsoft-teams-activities) <br/> |[Yammer 활동](#yammer-activities) <br/> |[Microsoft Flow 활동](#microsoft-flow-activities) <br/>|
|[Microsoft PowerApps 활동](#microsoft-powerapps)<br/>|[Microsoft Stream 활동](#microsoft-stream-activities) <br/>|[Exchange 관리자 활동](#exchange-admin-audit-log)<br/>|
||||
  
### <a name="file-and-page-activities"></a>파일 및 페이지 활동
  
다음 표에서는 SharePoint Online 및 비즈니스용 OneDrive의 파일 및 페이지 활동에 대해 설명합니다.
  
|**친숙한 이름**|**작업**|**설명**|
|:-----|:-----|:-----|
|파일에 액세스함  <br/> |FileAccessed  <br/> |사용자 또는 시스템 계정이 파일에 액세스합니다.  <br/> |
|(없음)  <br/> |FileAccessedExtended  <br/> |“파일에 액세스함"(FileAccessed) 활동과 관련이 있습니다. FileAccessedExtended 이벤트는 동일한 사용자가 장시간(최대 3시간) 지속적으로 파일에 액세스할 때 기록됩니다. FileAccessedExtened 이벤트 로깅의 목적은 파일에 지속적으로 액세스할 때 기록되는 FileAccessed 이벤트의 수를 줄이는 것입니다. 이렇게 하면 기본적으로 무엇이 동일한 사용자 활동인지에 대한 여러 FileAccessed 레코드의 노이즈를 줄일 수 있으며 초기( 및 중요한) FileAccessed 이벤트에 집중할 수 있습니다.  <br/> |
|준수 정책 레이블 변경됨<br/> |ComplianceSettingChanged<br/> |보존 레이블이 문서에 적용되거나 문서에서 제거되었습니다. 이 이벤트는 보존 레이블이 수동으로 또는 메시지에 자동으로 적용될 때 트리거됩니다.<br/> |
|레코드 상태를 잠김으로 변경함<br/> |LockRecord<br/> |문서를 레코드로 분류하는 보존 레이블의 레코드 상태가 잠겼습니다. 즉, 문서를 수정하거나 삭제할 수 없습니다. 사이트에 대한 최소한 참가자 권한이 할당된 사용자만 문서의 레코드 상태를 변경할 수 있습니다.<br/> |
|레코드 상태를 잠김 해제로 변경함<br/> |UnlockRecord<br/> |문서를 레코드로 분류하는 보존 레이블의 레코드 상태의 잠금이 해제되었습니다. 즉, 문서를 수정하거나 삭제할 수 있습니다. 사이트에 대한 최소한 참가자 권한이 할당된 사용자만 문서의 레코드 상태를 변경할 수 있습니다.<br/><br/> |
|파일 체크 인됨  <br/> |FileCheckedIn  <br/> |사용자가 문서 라이브러리에서 체크 아웃한 문서를 체크 인합니다.  <br/> |
|파일 체크 아웃됨  <br/> |FileCheckedOut  <br/> |사용자가 문서 라이브러리에 있는 문서를 체크 아웃합니다. 사용자는 공유된 문서를 체크 아웃한 후 변경할 수 있습니다.  <br/> |
|파일 복사됨  <br/> |FileCopied  <br/> |사용자가 사이트에서 문서를 복사합니다. 복사한 파일을 사이트의 다른 폴더에 저장할 수 있습니다.  <br/> |
|파일 삭제됨  <br/> |FileDeleted  <br/> |사용자가 사이트에서 문서를 삭제합니다.  <br/> |
|휴지통에서 파일 삭제됨  <br/> |FileDeletedFirstStageRecycleBin  <br/> |사용자가 사이트의 휴지통에서 파일을 삭제합니다.  <br/> |
|2단계 휴지통에서 파일 삭제됨  <br/> |FileDeletedSecondStageRecycleBin  <br/> |사용자가 사이트의 2단계 휴지통에서 파일을 삭제합니다.  <br/> |
|준수 정책 레이블 삭제됨<br/> |ComplianceRecordDelete<br/> |레코드로 분류된 문서가 삭제되었습니다. 문서에 콘텐츠를 레코드로 분류하는 보존 레이블이 적용된 경우 문서는 레코드로 간주됩니다. <br/> |
|발견된 문서 민감도 불일치 <br/>|DocumentSensitivityMismatchDetected<br/>|사용자가 문서를 업로드하는 사이트에 적용되는 민감도 레이블보다 중요도가 높은 문서를 업로드합니다. 이 이벤트는 사이트에 적용된 민감도 레이블이 사이트에 업로드된 문서에 적용된 민감도 레이블보다 우선 순위가 높은 경우 트리거되지 않습니다. 민감도 레이블 우선 순위에 대 한 자세한 내용은 [민감도 레이블 개요](sensitivity-labels.md#label-priority-order-matters)의 "레이블 우선 순위" 섹션을 참조하세요.<br/>|
|파일에서 맬웨어 검색됨  <br/> |FileMalwareDetected  <br/> |SharePoint 바이러스 백신 엔진이 파일에서 맬웨어를 검색합니다.  <br/> |
|파일 체크 아웃 취소됨  <br/> |FileCheckOutDiscarded  <br/> |사용자가 체크 아웃한 파일을 취소(또는 명령 취소)합니다. 즉, 체크 아웃되었을 때 파일에서 변경한 내용이 취소되고 문서 라이브러리의 문서 버전에 저장되지 않습니다.  <br/> |
|다운로드한 파일  <br/> |FileDownloaded  <br/> |사용자가 사이트에서 문서를 다운로드합니다.  <br/> |
|파일 수정됨  <br/> |FileModified  <br/> |사용자 또는 시스템 계정이 사이트에 있는 문서의 콘텐츠 또는 속석을 수정합니다.  <br/> |
|(없음)  <br/> |FileModifiedExtended  <br/> |“파일 수정됨"(FileModified) 활동과 관련이 있습니다. FileModifiedExtended 이벤트는 동일한 사용자가 장시간(최대 3시간) 지속적으로 파일을 수정할 때 기록됩니다. FileModifiedExtended 이벤트 로깅의 목적은 파일이 지속적으로 수정될 때 기록되는 FileModified 이벤트의 수를 줄이는 것입니다. 이렇게 하면 기본적으로 무엇이 동일한 사용자 활동인지에 대한 여러 FileModified 레코드의 노이즈를 줄일 수 있으며 초기( 및 중요한) FileModified 이벤트에 집중할 수 있습니다.  <br/> |
|파일 이동됨  <br/> |FileMoved  <br/> |사용자가 사이트의 현재 위치에서 새 위치로 문서를 이동합니다.  <br/> |
|(없음)  <br/> |FilePreviewed  <br/> |사용자가 SharePoint 또는 비즈니스용 OneDrive 사이트에서 파일을 미리 봅니다. 이러한 이벤트는 일반적으로 이미지 갤러리 보기와 같이 단일 활동을 기반으로 대량으로 발생합니다.  <br/> |
|파일의 모든 부 버전이 재생됨  <br/> |FileVersionsAllMinorsRecycled  <br/> |사용자가 파일의 버전 기록에서 모든 부 버전을 삭제합니다. 삭제된 버전은 사이트의 휴지통으로 이동됩니다.  <br/> |
|파일의 모든 버전이 재생됨  <br/> |FileVersionsAllRecycled  <br/> |사용자가 파일의 버전 기록에서 모든 버전을 삭제합니다. 삭제된 버전은 사이트의 휴지통으로 이동됩니다.  <br/> |
|파일의 버전이 재생됨  <br/> |FileVersionRecycled  <br/> |사용자가 파일의 버전 기록에서 버전을 삭제합니다. 삭제된 버전은 사이트의 휴지통으로 이동됩니다.  <br/> |
|파일 이름 바뀜  <br/> |FileRenamed  <br/> |사용자가 사이트의 문서 이름을 바꿉니다.  <br/> |
|파일 복원됨  <br/> |FileRestored  <br/> |사용자가 사이트의 휴지통에서 문서를 복원합니다.  <br/> |
|파일 업로드됨  <br/> |FileUploaded  <br/> |사용자가 사이트의 폴더에 문서를 업로드합니다.  <br/> |
|페이지 확인함  <br/> |PageViewed  <br/> |사용자가 사이트에서 페이지를 확인합니다. 웹 브라우저를 사용하여 문서 라이브러리에 있는 파일을 확인하는 작업은 포함되지 않습니다.  <br/> |
|(없음)  <br/> |PageViewedExtended  <br/> |“페이지 확인함”(PageViewed) 활동과 관련이 있습니다. PageViewedExtended 이벤트는 동일한 사용자가 장시간(최대 3시간) 지속적으로 웹 페이지를 확인할 때 기록됩니다. PageViewedExtended 이벤트 로깅의 목적은 페이지가 지속적으로 조회될 때 기록되는 PageViewed 이벤트 수를 줄이는 것입니다. 이렇게 하면 기본적으로 무엇이 동일한 사용자 활동인지에 대한 여러 PageViewed 레코드의 노이즈를 줄일 수 있으며 초기( 및 중요한) PageViewed 이벤트에 집중할 수 있습니다.  <br/> |
|클라이언트가 신호를 보낸 보기 <br/>|ClientViewSignaled<br/>|사용자의 클라이언트(예 : 웹 사이트 또는 모바일 앱)가 표시된 페이지를 사용자가 본다는 신호를 보냈습니다. 이 활동은 페이지에 대한 PagePrefetched 이벤트를 통해 기록되는 경우가 많습니다. <br/><br/>**참고** : ClientViewSignaled 이벤트는 서버가 아닌 클라이언트가 신호하므로 이벤트가 서버에 의해 기록되지 않아 감사 로그에 표시되지 않을 수 있습니다. 감사 레코드의 정보가 신뢰되지 않을 수도 있습니다. 그러나 사용자의 ID는 신호를 만드는 데 사용되는 토큰에 의해 유효성이 검사되므로 해당 감사 레코드에 나열된 사용자 ID가 정확합니다. |
|(없음) <br/>|PagePrefetched<br/>|사용자의 클라이언트(예 : 웹 사이트 또는 모바일 앱)가 사용자가 웹 페이지를 탐색할 때 성능을 개선할 수 있도록 표시된 페이지를 요청했습니다. 이 이벤트는 페이지 콘텐츠가 사용자의 클라이언트에게 제공되었음을 나타내기 위해 기록됩니다. 이 이벤트는 사용자가 페이지를 탐색했다는 명확한 표시가 아닙니다. 클라이언트가 페이지 콘텐츠를 렌더링하면(사용자 요청에 따라) ClientViewSignaled 이벤트가 생성되어야 합니다. 모든 클라이언트가 사전 페치 표시하도록 지원하지 않으므로 일부 사전 페치된 활동이 PageViewed 이벤트로 대신 기록될 수 있습니다.<br/>|
||||
  
### <a name="folder-activities"></a>폴더 활동
  
다음 표에서는 SharePoint Online 및 비즈니스용 OneDrive의 폴더 활동에 대해 설명합니다.
  
|**친숙한 이름**|**작업**|**설명**|
|:-----|:-----|:-----|
|폴더 복사됨  <br/> |FolderCopied  <br/> |사용자가 사이트의 폴더를 SharePoint 또는 비즈니스용 OneDrive의 다른 위치에 복사합니다.  <br/> |
|폴더 생성됨  <br/> |FolderCreated  <br/> |사용자가 사이트에 폴더를 생성합니다.  <br/> |
|폴더 삭제됨  <br/> |FolderDeleted  <br/> |사용자가 사이트에서 폴더를 삭제합니다.  <br/> |
|휴지통에서 폴더 삭제됨  <br/> |FolderDeletedFirstStageRecycleBin  <br/> |사용자가 사이트의 휴지통에서 폴더를 삭제합니다.  <br/> |
|2단계 휴지통에서 폴더 삭제됨  <br/> |FolderDeletedSecondStageRecycleBin  <br/> |사용자가 사이트의 2단계 휴지통에서 폴더를 삭제합니다.  <br/> |
|폴더 수정됨  <br/> |FolderModified  <br/> |사용자가 사이트에서 폴더를 수정합니다. 태그 및 속성 변경과 같은 폴더 메타데이터 변경이 포함됩니다.  <br/> |
|폴더 이동됨  <br/> |FolderMoved  <br/> |사용자가 폴더를 사이트의 다른 위치로 이동합니다.  <br/> |
|폴더 이름 변경됨  <br/> |FolderRenamed  <br/> |사용자가 사이트에서 폴더 이름을 변경합니다.  <br/> |
|폴더 복원됨  <br/> |FolderRestored  <br/> |사용자가 사이트의 휴지통에서 삭제된 폴더를 복원합니다.  <br/> |
||||
  
### <a name="sharepoint-list-activities"></a>SharePoint 목록 활동
  
다음 표에서는 사용자가 SharePoint Online에서 목록과 목록 항목과 상호 작용하는 경우와 관련된 활동에 대해 설명합니다.

|**친숙한 이름**|**작업**|**설명**|
|:-----|:-----|:-----|
| 목록이 만들어짐              | ListCreated              | 사용자가 SharePoint 목록을 만들었습니다.|
| 목록 열이 만들어짐       | ListColumnCreated        | 사용자가 SharePoint 목록 열을 만들었습니다. 목록 열은 하나 이상의 SharePoint 목록에 첨부되는 열입니다. |
| 목록 콘텐츠 유형이 만들어짐 | ListContentTypeCreated   | 사용자가 목록 콘텐츠 유형을 만들었습니다. 목록 콘텐츠 유형은 하나 이상의 SharePoint 목록에 첨부된 콘텐츠 유형입니다.|
| 목록 항목이 만들어짐         | ListItemCreated          | 사용자가 기존 SharePoint 목록에서 항목을 만들었습니다.|
| 사이트 열 만들기       | SiteColumnCreated        | 사용자가 SharePoint 사이트 열을 만들었습니다. 사이트 열은 목록에 첨부되지 않은 열입니다. 사이트 열은 지정된 웹의 모든 목록에서 사용할 수 있는 메타 데이터 구조이기도 합니다.|
| 사이트 콘텐츠 유형이 만들어짐 | 사이트 ContentType이 만들어짐 | 사용자가 사이트 콘텐츠 유형을 만들었습니다. 사이트 콘텐츠 유형은 상위 사이트에 첨부된 콘텐츠 유형입니다.|
| 목록이 삭제됨              | ListDeleted              | 사용자가 SharePoint 목록을 삭제했습니다.|
| 목록 열이 삭제됨       | 목록 열이 삭제됨      | 사용자가 SharePoint 목록 열을 삭제했습니다.|
| 목록 콘텐츠 유형이 삭제됨 | ListContentTypeDeleted   | 사용자가 목록 콘텐츠 유형을 삭제했습니다. |
| 목록 항목이 삭제됨         | 목록 항목이 삭제됨        | 사용자가 SharePoint 목록 항목을 삭제했습니다.|
| 사이트 열이 삭제됨       | SiteColumnDeleted        | 사용자가 SharePoint 사이트 열을 삭제했습니다. |
| 사이트 콘텐츠 유형이 삭제됨 | SiteContentTypeDeleted   | 사용자가 사이트 콘텐츠 유형을 삭제했습니다.|
| 목록 항목 휴지통으로 이동        | ListItemRecycled         | 사용자가 SharePoint 목록 항목을 휴지통으로 이동했습니다.|
| 목록 복원됨             | ListRestored             | 사용자가 SharePoint 목록을 휴지통에서 복원했습니다.|
| 목록 항목 복원됨        | ListItemRestored         | 사용자가 SharePoint 목록 항목을 휴지통에서 복원했습니다.|
| 목록 업데이트됨              | ListUpdated              | 사용자가 하나 이상의 속성을 수정하여 SharePoint 목록을 업데이트했습니다.|
| 목록 열이 업데이트됨       | ListColumnUpdated        | 사용자가 하나 이상의 속성을 수정하여 SharePoint 목록 열을 업데이트했습니다.|
| 목록 콘텐츠 유형이 업데이트됨 | ListContentTypeUpdated   | 사용자가 하나 이상의 속성을 수정하여 SharePoint 목록 콘텐츠 유형을 업데이트했습니다.|
| 목록 항목 업데이트됨         | ListItemUpdated          | 사용자가 하나 이상의 속성을 수정하여 SharePoint 목록 항목을 업데이트했습니다.|  
| 사이트 열 업데이트됨       | SiteColumnUpdated        | 사용자가 하나 이상의 속성을 수정하여 SharePoint 사이트 열을 업데이트했습니다.|
| 사이트 콘텐츠 유형이 업데이트됨 | SiteContentTypeUpdated   | 사용자가 하나 이상의 속성을 수정하여 SharePoint 사이트 콘텐츠 유형을 업데이트했습니다.|
||||

### <a name="sharing-and-access-request-activities"></a>공유 및 액세스 요청 활동
  
다음 표에서는 SharePoint Online 및 비즈니스용 OneDrive의 사용자 공유 및 액세스 요청 활동에 대해 설명합니다. 공유 이벤트의 경우 **결과** 아래의 **세부 정보** 열에서 항목이 공유된 사용자 또는 그룹의 이름과 해당 사용자 또는 그룹이 조직의 구성원인지, 게스트인지를 식별합니다. 자세한 내용은 [Office 365 감사 로그에서 공유 감사 사용](use-sharing-auditing.md)을 참조하세요.
  
> [!NOTE]
> 사용자는 사용자 개체의 UserType 속성에 따라 *구성원* 또는 *게스트*일 수 있습니다. 구성원은 일반적으로 직원이고, 게스트는 일반적으로 조직 외부의 공동 작업자입니다. 조직에 속하지 않은 사용자가 공유 초대를 수락하면 조직의 디렉터리에 해당 게스트 계정이 만들어집니다. 게스트 사용자의 계정이 디렉터리에 있으면 초대장 없이 해당 사용자와 직접 리소스를 공유할 수 있습니다. 
  
|**친숙한 이름**|**작업**|**설명**|
|:-----|:-----|:-----|
|사이트 모음에 사용 권한 수준 추가됨  <br/> |PermissionLevelAdded  <br/> |사이트 모음에 사용 권한 수준이 추가되었습니다.  <br/> |
|액세스 요청 수락됨  <br/> |AccessRequestAccepted  <br/> |사이트, 폴더 또는 문서에 대한 액세스 요청이 수락되었으며 요청하는 사용자에게 액세스 권한이 부여되었습니다.  <br/> |
|공유 초대 수락됨  <br/> |SharingInvitationAccepted  <br/> |사용자(구성원 또는 게스트)가 공유 초대를 수락했으며 리소스에 대한 액세스 권한이 부여되었습니다. 이 이벤트에는 초대를 받은 사용자 및 초대를 수락하는 데 사용된 전자 메일 주소에 대한 정보가 포함됩니다(다를 수 있음). 이 활동에는 대체로 사용자에게 리소스에 대한 액세스 권한이 어떻게 부여되었는지를 설명(예: 리소스에 대한 액세스 권한이 있는 그룹에 사용자 추가)하는 두 번째 이벤트가 수반됩니다.  <br/> |
|공유 초대 차단됨  <br/> |SharingInvitationBlocked  <br/> | 조직의 사용자가 보낸 공유 초대가 대상 사용자의 도메인을 기반으로 외부 공유를 허용하거나 거부하는 외부 공유 정책으로 인해 차단되었습니다. 이 경우 공유 초대는 다음과 같은 이유로 차단되었습니다.  <br/>  대상 사용자의 도메인이 허용된 도메인 목록에 포함되어 있지 않습니다.  <br/>  또는  <br/>  대상 사용자의 도메인이 차단된 도메인 목록에 포함되어 있습니다.  <br/>  도메인을 기반으로 한 외부 공유 허용 또는 차단에 대한 자세한 내용은 [SharePoint Online 및 비즈니스용 OneDrive의 제한된 도메인 공유](https://support.office.com/article/5d7589cd-0997-4a00-a2ba-2320ec49c4e9)를 참조하세요.  <br/> |
|액세스 요청 생성됨  <br/> |AccessRequestCreated  <br/> |사용자가 액세스 권한이 없는 사이트, 폴더 또는 문서에 대한 액세스를 요청합니다.  <br/> |
|회사에서 공유할 수 있는 링크 생성됨   <br/> |CompanyLinkCreated  <br/> |사용자가 리소스에 대한 회사 전체 링크를 생성했습니다. 회사 전체 링크는 조직의 구성원만 사용할 수 있습니다. 게스트는 사용할 수 없습니다.  <br/> |
|익명 링크 생성됨  <br/> |AnonymousLinkCreated  <br/> |사용자가 리소스에 대한 익명 링크를 만들었습니다. 이 링크만 있으면 누구든지 인증 필요 없이 리소스에 액세스할 수 있습니다.  <br/> |
|보안 링크 생성됨  <br/> |SecureLinkCreated  <br/> |이 항목에 대한 보안 공유 링크가 생성되었습니다.  <br/> |
|공유 초대 생성됨  <br/> |SharingInvitationCreated  <br/> |사용자가 SharePoint Online 또는 비즈니스용 OneDrive에서 조직의 디렉터리에 없는 사용자와 리소스를 공유했습니다.  <br/> |
|보안 링크 삭제됨  <br/> |SecureLinkDeleted  <br/> |보안 공유 링크가 삭제되었습니다.  <br/> |
|액세스 요청 거부됨   <br/> |AccessRequestDenied  <br/> |사이트, 폴더 또는 문서에 대한 액세스 요청을 거부했습니다.  <br/> |
|회사에서 공유할 수 있는 링크 제거됨  <br/> |CompanyLinkRemoved  <br/> |사용자가 리소스에 대한 회사 차원의 링크를 제거했습니다. 더 이상 링크를 사용하여 리소스에 액세스할 수 없습니다.  <br/> |
|익명 링크 제거됨  <br/> |AnonymousLinkRemoved  <br/> |사용자가 리소스에 대한 익명 링크를 제거했습니다. 더 이상 링크를 사용하여 리소스에 액세스할 수 없습니다.  <br/> |
|공유 파일, 폴더 또는 사이트  <br/> |SharingSet  <br/> |사용자(구성원 또는 게스트)가 SharePoint Online 또는 비즈니스용 OneDrive에서 조직의 디렉터리에 있는 사용자와 파일, 폴더 또는 사이트를 공유했습니다. 이 활동에 대한 **세부 정보** 열의 값은 리소스가 공유된 사용자의 이름과 이 사용자가 구성원인지, 게스트인지를 식별합니다. 이 활동에는 대체로 사용자에게 리소스에 대한 액세스 권한이 어떻게 부여되었는지를 설명하는 두 번째 이벤트가 수반됩니다. 예를 들어, 리소스에 대한 액세스 권한이 있는 그룹에 사용자를 추가합니다.  <br/> |
|액세스 요청 업데이트됨  <br/> |AccessRequestUpdated  <br/> |항목에 대한 액세스 요청이 업데이트되었습니다.  <br/> |
|익명 링크 업데이트됨   <br/> |AnonymousLinkUpdated  <br/> |사용자가 리소스에 대한 익명 링크를 업데이트했습니다. 업데이트된 필드는 검색 결과를 내보낼 때 EventData 속성에 포함됩니다.  <br/> |
|공유 초대 업데이트됨  <br/> |SharingInvitationUpdated  <br/> |외부 공유 초대가 업데이트되었습니다.  <br/> |
|익명 링크 사용됨  <br/> |AnonymousLinkUsed  <br/> |익명 사용자가 익명 링크를 사용하여 리소스에 액세스했습니다. 사용자 ID는 모르지만 사용자 IP 주소와 같은 다른 세부 정보를 얻을 수 있습니다.  <br/> |
|파일, 폴더 또는 사이트 공유 해제됨  <br/> |SharingRevoked  <br/> |사용자(구성원 또는 게스트)가 이전에 다른 사용자와 공유된 파일, 폴더 또는 사이트 공유를 해제했습니다.  <br/> |
|회사에서 공유할 수 있는 링크 사용됨  <br/> |CompanyLinkUsed  <br/> |사용자가 회사 차원의 링크를 사용하여 리소스에 액세스했습니다.  <br/> |
|보안 링크 사용됨  <br/> |SecureLinkUsed  <br/> |사용자가 보안 링크를 사용했습니다.  <br/> |
|보안 링크에 사용자 추가됨  <br/> |AddedToSecureLink  <br/> |보안 공유 링크를 사용할 수 있는 엔터티 목록에 사용자가 추가되었습니다.  <br/> |
|보안 링크에서 사용자 제거됨  <br/> |RemovedFromSecureLink  <br/> |보안 공유 링크를 사용할 수 있는 엔터티 목록에 사용자가 제거되었습니다.  <br/> |
|공유 초대 제거됨  <br/> |SharingInvitationRevoked  <br/> |사용자가 리소스에 대한 공유 초대를 제거했습니다.   <br/> |
||||
  
### <a name="synchronization-activities"></a>동기화 활동
  
다음 표에서는 SharePoint Online 및 비즈니스용 OneDrive의 파일 동기화 활동에 대해 나열합니다.
  
|**친숙한 이름**|**작업**|**설명**|
|:-----|:-----|:-----|
|컴퓨터에서 파일을 동기화할 수 있도록 허용됨  <br/> |ManagedSyncClientAllowed  <br/> |사용자가 사이트와 동기화 관계를 설정합니다. 사용자 컴퓨터가 조직의 문서 라이브러리에 액세스할 수 있는 도메인 목록(*수신 허용-받는 사람 목록*)에 추가된 도메인의 구성원이므로 동기화 관계는 성공적으로 설정됩니다.  <br/> 이 기능에 대한 자세한 내용은 [Windows PowerShell cmdlet을 통해 수신 허용 - 받는 사람 목록에 있는 도메인에 대해 OneDrive 동기화를 사용하도록 설정](https://go.microsoft.com/fwlink/p/?LinkID=534609)을 참조하세요.  <br/> |
|컴퓨터에서 파일을 동기화할 수 없도록 차단됨  <br/> |UnmanagedSyncClientBlocked  <br/> |사용자가 조직의 도메인 구성원이 아니거나 조직의 문서 라이브러리에 액세스할 수 있는 도메인 목록(*수신 허용 - 받는 사람 목록)* 에 추가되지 않은 도메인의 구성원인 컴퓨터에서 사이트와 동기화 관계를 설정하려고 합니다. 동기화 관계는 허용되지 않고 사용자의 컴퓨터에서 문서 라이브러리의 파일에 대한 동기화, 다운로드 또는 업로드가 차단됩니다.  <br/> 이 기능에 대한 자세한 내용은 [Windows PowerShell cmdlet을 통해 수신 허용 - 받는 사람 목록에 있는 도메인에 대해 OneDrive 동기화를 사용하도록 설정](https://go.microsoft.com/fwlink/p/?LinkID=534609)을 참조하세요.  <br/> |
|컴퓨터에 파일 다운로드됨  <br/> |FileSyncDownloadedFull  <br/> |사용자가 동기화 관계를 설정하고 처음으로 문서 라이브러리에서 해당 컴퓨터로 파일을 다운로드합니다.  <br/> |
|컴퓨터에 파일 변경 내용 다운로드됨  <br/> |FileSyncDownloadedPartial  <br/> |사용자가 문서 라이브러리의 파일에 대한 변경 내용을 다운로드합니다. 이 활동은 문서 라이브러리의 파일에 대한 변경 내용이 사용자 컴퓨터로 모두 다운로드되었음을 나타냅니다. **컴퓨터에 파일 다운로드됨** 활동에 표시된 것처럼 사용자가 이전에 문서 라이브러리를 다운로드했기 때문에 변경 내용만 다운로드되었습니다.  <br/> |
|문서 라이브러리에 파일 업로드됨  <br/> |FileSyncUploadedFull  <br/> |사용자가 동기화 관계를 설정하고 처음으로 해당 컴퓨터에서 문서 라이브러리로 파일을 업로드합니다.  <br/> |
|문서 라이브러리에 파일 변경 내용 업로드됨  <br/> |FileSyncUploadedPartial  <br/> |사용자가 문서 라이브러리의 파일에 대한 변경 내용을 업로드합니다. 이 이벤트는 문서 라이브러리의 로컬 파일 버전에 대한 변경 내용이 문서 라이브러리로 업로드되었음을 나타냅니다. **문서 라이브러리에 파일 업로드됨** 활동에 표시된 것처럼 사용자가 이전에 해당 파일을 업로드했기 때문에 변경 내용만 업로드되었습니다.  <br/> |
||||

### <a name="site-permissions-activities"></a>사이트 사용 권한 활동

다음 표에서는 SharePoint에서 사용 권한을 할당하고 그룹을 사용하 여 사이트에 대한 액세스를 제공하고 철회하는 데 관련된 이벤트를 보여 줍니다.

|**친숙한 이름**|**작업**|**설명**|
|:-----|:-----|:-----|
|사이트 모음 관리자 추가됨  <br/> |SiteCollectionAdminAdded  <br/> |사이트 모음 관리자 또는 소유자가 사이트에 대한 사이트 모음 관리자로 사용자를 추가합니다. 사이트 모음 관리자는 사이트 모음 및 모든 하위 사이트에 대한 모든 권한을 갖습니다. 이 활동은 또한 관리자가 사용자의 OneDrive 계정에 액세스할 수 있는 경우(SharePoint 관리 센터에서 사용자 프로필을 편집하거나 [Microsoft 365 관리 센터를 사용하는 경우](https://docs.microsoft.com/office365/admin/add-users/get-access-to-and-back-up-a-former-user-s-data#part-1---get-access-to-the-former-employees-onedrive-for-business-documents))에도 기록됩니다. <br/> |
|SharePoint 그룹에 사용자 또는 그룹 추가됨  <br/> |AddedToGroup  <br/> |사용자가 SharePoint 그룹에 구성원 또는 게스트를 추가했습니다. 이는 의도된 작업이거나 공유 이벤트와 같은 다른 활동의 결과일 수 있습니다.  <br/> |
|사용 권한 수준 상속 해제  <br/> |PermissionLevelsInheritanceBroken  <br/> |항목이 더 이상 부모에서 사용 권한을 상속하지 않도록 변경되었습니다.  <br/> |
|상속 공유 해제  <br/> |SharingInheritanceBroken  <br/> |항목이 더 이상 부모에서 공유 권한을 상속하지 않도록 변경되었습니다.  <br/> |
|그룹 생성됨  <br/> |GroupAdded  <br/> |사이트 관리자 또는 소유자가 사이트에 대한 그룹을 만들거나 그룹이 생성되게 하는 작업을 수행합니다. 예를 들어 처음으로 사용자가 파일 공유에 대한 링크를 만들면 사용자의 skydrive_pro 사이트에 시스템 그룹이 추가됩니다. 이 이벤트는 공유 파일에 대한 편집 권한이 있는 사용자가 링크를 만들 때 발생하는 결과일 수도 있습니다.  <br/> |
|그룹 삭제됨  <br/> |GroupRemoved  <br/> |사용자가 사이트에서 그룹을 삭제합니다.  <br/> |
|액세스 요청 설정 수정됨  <br/> |WebRequestAccessModified  <br/> |액세스 요청 설정이 사이트에서 수정되었습니다.  <br/> |
|'구성원이 공유할 수 있음’ 설정 수정됨  <br/> |WebMembersCanShareModified  <br/> |**구성원이 공유할 수 있음** 설정이 수정되었습니다.  <br/> |
|사이트 모음에서 사용 권한 수준 수정됨  <br/> |PermissionLevelModified  <br/> |사이트 모음에서 사용 권한 수준이 변경되었습니다.  <br/> |
|사이트 사용 권한 수정됨  <br/> |SitePermissionsModified  <br/> |사이트 관리자 또는 소유자(또는 시스템 계정)가 사이트에 대한 그룹에 할당된 사용 권한 수준을 변경합니다. 그룹에서 모든 사용 권한이 제거된 경우에도 이 활동이 기록됩니다.  <br/><br/> **참고**:이 작업은 SharePoint Online에서 더 이상 사용되지 않습니다. 관련 이벤트를 찾으려면 **사이트 모음 관리자 추가됨**, **SharePoint 그룹에 사용자 또는 그룹을 추가함**, **사용자가 그룹을 만들 수 있도록 허용됨**, **그룹 생성됨**, **그룹 삭제됨** 같은 기타 권한 관련 활동을 검색할 수 있습니다.|
|사이트 모음에서 사용 권한 수준 제거됨  <br/> |PermissionLevelRemoved  <br/> |사이트 모음에서 사용 권한 수준이 제거되었습니다.  <br/> |
|사이트 모음 관리자 제거됨  <br/> |SiteCollectionAdminRemoved <br/> |사이트 모음 관리자 또는 소유자가 사이트에 대한 사이트 모음 관리자로 사용자를 제거합니다. 이 활동은 또한 관리자가 사용자의 OneDrive 계정의 사이트 모음 관리자 목록에서 자신을 제거할 경우(SharePoint 관리 센터에서 사용자 프로필을 편집하여)에도 기록됩니다.  감사 로그 검색 결과에서 이 활동을 반환하려면 모든 활동을 검색해야 합니다. <br/> |
|SharePoint 그룹에 사용자 또는 그룹 제거됨  <br/> |RemovedFromGroup  <br/> |사용자가 SharePoint 그룹에서 구성원 또는 게스트를 제거했습니다. 이는 의도된 작업이거나 공유 해제 이벤트와 같은 다른 활동의 결과일 수 있습니다.  <br/> |
|사이트 관리자 권한 요청됨  <br/> |SiteAdminChangeRequest  <br/> |사용자가 사이트 모음의 사이트 모음 관리자로 추가되도록 요청합니다. 사이트 모음 관리자는 사이트 모음 및 모든 하위 사이트에 대한 모든 권한을 갖습니다.  <br/> |
|상속 공유 복원됨  <br/> |SharingInheritanceReset  <br/> |항목이 상위 항목에서 공유 권한을 상속하도록 변경되었습니다.  <br/> |
|그룹 업데이트됨  <br/> |GroupUpdated  <br/> |사이트 관리자 또는 소유자가 사이트에 대한 그룹 설정을 변경합니다. 여기에는 그룹 이름 변경, 그룹 구성원을 보거나 편집할 수 있는 사람, 구성원 자격 요청의 처리 방법이 포함될 수 있습니다.  <br/> |
||||

  
### <a name="site-administration-activities"></a>사이트 관리 활동
  
다음 표에는 사용자가 SharePoint Online에서 사이트 관리 작업이 수행될 때 발생하는 이벤트가 나와 있습니다.
  
|**친숙한 이름**|**작업**|**설명**|
|:-----|:-----|:-----|
|허용된 데이터 위치 추가됨<br/>|AllowedDataLocationAdded|SharePoint 또는 전역 관리자가 여러 지리적 환경에서 허용되는 데이터 위치를 추가했습니다. <br/>|
|예외 사용자 에이전트 추가됨  <br/> |ExemptUserAgentSet  <br/> |SharePoint 또는 전역 관리자가 SharePoint 관리 센터에서 예외 사용자 에이전트 목록에 사용자 에이전트를 추가했습니다.  <br/> |
|지리적 위치 관리자 추가됨<br/>|GeoAdminAdded<br/>|SharePoint 또는 전역 관리자가 위치에 대한 지리적 관리자로 사용자를 추가했습니다. <br/>|
|사용자가 그룹을 만들 수 있도록 허용됨  <br/> |AllowGroupCreationSet  <br/> |사이트 관리자 또는 소유자가 해당 권한이 할당된 사용자가 사이트에 대한 그룹을 만들 수 있도록 허용하는 사용 권한 수준을 사이트에 추가합니다.  <br/> |
|사이트 지리적 이동 취소됨  <br/> |SiteGeoMoveCancelled  <br/> |SharePoint 또는 전역 관리자가 SharePoint 또는 OneDrive 사이트 지리적 이동을 성공적으로 취소했습니다. Multi-Geo Capabilities를 사용하면 Office 365 조직이 geos라는 여러 Office 365 데이터센터 지역에 걸쳐 있을 수 있습니다. 자세한 내용은 [Office 365의 OneDrive 및 SharePoint Online의 여러 지리 기능](https://go.microsoft.com/fwlink/?linkid=860840)을 참조하세요.  <br/> |
|공유 정책 변경됨  <br/> |SharingPolicyChanged  <br/> |SharePoint 또는 전역 관리자가 Office 365 관리 포털, SharePoint 관리자 포털 또는 SharePoint Online 관리 셸을 사용하여 SharePoint 공유 정책을 변경했습니다. 조직의 공유 정책 설정에 대한 변경 내용이 모두 기록됩니다. 변경 된 정책은 이벤트 레코드의 자세한 속성에서 **ModifiedProperties** 필드에서 식별됩니다.  <br/> |
|장치 액세스 정책 변경됨  <br/> |DeviceAccessPolicyChanged  <br/> |SharePoint 또는 전역 관리자가 조직의 관리되지 않는 장치 정책을 변경했습니다. 이 정책은 조직에 가입되지 않은 장치에서의 SharePoint, OneDrive, Office 365에 대한 액세스를 제어합니다. 이 정책을 구성하려면 Enterprise Mobility + Security 구독이 필요합니다. 자세한 내용은 [관리되지 않는 장치에서의 액세스 제어](https://support.office.com/article/5ae550c4-bd20-4257-847b-5c20fb053622)를 참조하세요.  <br/> |
|예외 사용자 에이전트 변경됨  <br/> |CustomizeExemptUsers  <br/> |SharePoint 또는 전역 관리자가 SharePoint 관리 센터에서 예외 사용자 에이전트 목록을 사용자 지정했습니다. 인덱스에 전체 웹 페이지를 받을 수 없도록 제외할 사용자 에이전트를 지정할 수 있습니다. 즉, 예외로 지정한 사용자 에이전트가 InfoPath 양식을 만나면 해당 양식은 전체 웹 페이지가 아닌 XML 파일로 반환됩니다. 이렇게 하면 InfoPath 양식을 더 빠르게 인덱싱할 수 있습니다.  <br/> |
|네트워크 액세스 정책 변경됨  <br/> |NetworkAccessPolicyChanged  <br/> |SharePoint 또는 전역 관리자가 SharePoint 관리 센터에서 또는 SharePoint PowerShell을 사용하여 위치 기반 액세스 정책(신뢰할 수 있는 네트워크 경계라고도 함)을 변경했습니다. 이 정책 유형은 지정한 권한 있는 IP 주소 범위를 기반으로 조직의 SharePoint 및 OneDrive 리소스에 액세스할 수 있는 사용자를 제어합니다. 자세한 내용은 [네트워크 위치를 기반으로 SharePoint Online 및 OneDrive 데이터에 대한 액세스 제어](https://support.office.com/article/b5a5f1f1-1174-4c6b-91d0-9273a6b6971f)를 참조하세요.  <br/> |
|사이트 지리적 이동 완료됨  <br/> |SiteGeoMoveCompleted  <br/> |조직의 전역 관리자가 예약한 사이트 지리적 이동이 완료되었습니다. Multi-Geo Capabilities를 사용하면 Office 365 조직이 geos라는 여러 Office 365 데이터센터 지역에 걸쳐 있을 수 있습니다. 자세한 내용은 [Office 365의 OneDrive 및 SharePoint Online의 여러 지리 기능](https://go.microsoft.com/fwlink/?linkid=860840)을 참조하세요.  <br/> |
|받는 사람 연결 생성됨  <br/> |SendToConnectionAdded  <br/> |SharePoint 또는 전역 관리자가 SharePoint 관리 센터의 레코드 관리 페이지에서 새 보내기 연결을 만듭니다. 받는 사람 연결은 문서 리포지토리 또는 레코드 센터에 대한 설정을 지정합니다. 받는 사람 연결을 만들면 콘텐츠 구성 도우미가 문서를 지정된 위치에 제출할 수 있습니다.  <br/> |
|사이트 모음 생성됨  <br/> |SiteCollectionCreated  <br/> |Sharepoint 또는 전역 관리자가 SharePoint Online 조직에서 사이트 모음을 만들거나 사용자가 비즈니스용 OneDrive 사이트를 프로비전합니다.  <br/> |
|분리된 허브 사이트 삭제됨<br/>|HubSiteOrphanHubDeleted<br/>|SharePoint 또는 전역 관리자가 연결된 사이트가 없는 허브 사이트인 분리된 허브 사이트를 삭제합니다. 분리된 허브는 원본 허브 사이트를 삭제하여 발생하는 문제일 수 있습니다. <br/>|
|받는 사람 연결 삭제됨  <br/> |SendToConnectionRemoved  <br/> |SharePoint 또는 전역 관리자가 SharePoint 관리 센터의 레코드 관리 페이지에서 보내기 연결을 삭제합니다.  <br/> |
|사이트 삭제됨  <br/> |SiteDeleted  <br/> |사이트 관리자가 사이트를 삭제합니다.  <br/> |
|문서 미리 보기가 사용하도록 설정됨  <br/> |PreviewModeEnabledSet  <br/> |사이트 관리자가 사이트에 대해 문서 미리 보기를 사용하도록 설정합니다.  <br/> |
|레거시 워크플로가 사용하도록 설정됨  <br/> |LegacyWorkflowEnabledSet  <br/> |사이트 관리자 또는 소유자가 SharePoint 2013 워크플로 작업 콘텐츠 형식을 사이트에 추가합니다. 전역 관리자는 SharePoint 관리 센터에서 전체 조직에 대해 워크플로를 사용하도록 설정할 수도 있습니다.  <br/> |
|Office on Demand가 사용하도록 설정됨  <br/> |OfficeOnDemandSet  <br/> |사이트 관리자가 최신 버전의 Office 데스크톱 응용 프로그램에 액세스할 수 있도록 하는 Office on Demand를 사용하도록 설정합니다. Office on Demand는 SharePoint 관리 센터에서 사용되도록 설정되며 설치된 전체 Office 응용 프로그램을 포함하는 Office 365 구독이 있어야 사용할 수 있습니다.  <br/> |
|사용자 검색 결과 원본이 사용하도록 설정됨<br/>|PeopleResultsScopeSet<br/>|사이트 관리자가 사이트에 대한 사용자 검색 결과 원본을 만듭니다.<br/>|
|RSS 피드가 사용하도록 설정됨  <br/> |NewsFeedEnabledSet  <br/> |사이트 관리자 또는 소유자가 사이트에 대해 RSS 피드를 사용하도록 설정합니다. 전역 관리자는 SharePoint 관리 센터에서 전체 조직에 대해 RSS 피드를 사용하도록 설정할 수 있습니다.  <br/> |
|사이트가 허브 사이트에 연결됨<br/>|HubSiteJoined<br/>|사이트 소유자가 사이트를 허브 사이트에 연결합니다.<br/>|
|허브 사이트 등록됨<br/>|HubSiteRegistered<br/>|SharePoint 또는 전역 관리자가 허브 사이트를 만듭니다. 그 결과 사이트는 허브 사이트에 등록됩니다. <br/>|
|허용된 데이터 위치 제거됨<br/>|AllowedDataLocationDeleted<br/>|SharePoint 또는 전역 관리자가 여러 지리적 환경에서 허용되는 데이터 위치를 제거했습니다.<br/>|
|지리적 위치 관리자 제거됨<br/>|GeoAdminDeleted<br/>|SharePoint 또는 전역 관리자가 위치에 대한 지리적 관리자로 사용자를 제거했습니다.<br/>|
|사이트 이름 바뀜  <br/> |SiteRenamed  <br/> |사이트 관리자 또는 소유자가 사이트 이름을 바꿉니다.  <br/> |
|예약된 사이트 지리적 이동  <br/> |SiteGeoMoveScheduled  <br/> |SharePoint 또는 전역 관리자가 SharePoint 또는 OneDrive 사이트 지리적 이동을 예약합니다. Multi-Geo Capabilities를 사용하면 Office 365 조직이 geos라는 여러 Office 365 데이터센터 지역에 걸쳐 있을 수 있습니다. 자세한 내용은 [Office 365의 OneDrive 및 SharePoint Online의 여러 지리 기능](https://go.microsoft.com/fwlink/?linkid=860840)을 참조하세요.  <br/> |
|호스트 사이트 설정됨  <br/> |HostSiteSet  <br/> |SharePoint 또는 전역 관리자가 개인 또는 비즈니스용 OneDrive 사이트를 호스트하도록 지정된 사이트를 변경합니다.  <br/> |
|지리적 위치에 대한 저장소 할당량 설정됨  <br/> |GeoQuotaAllocated<br/> |SharePoint 또는 전역 관리자가 다중 지리적 환경에서 지리적 위치에 대한 저장소 할당량을 구성했습니다.<br/> |
|허브 사이트의 사이트 연결이 끊김<br/>|HubSiteUnjoined<br/>|사이트 소유자가 사이트를 허브 사이트에서 연결을 끊습니다.<br/>|
|허브 사이트 등록이 취소됨<br/>|HubSiteUnregistered<br/>|SharePoint 또는 전역 관리자가 허브 사이트로 등록을 취소합니다. 허브 사이트의 등록이 취소되면 더 이상 허브 사이트 역할을 하지 않습니다. <br/>|
||||
  
### <a name="exchange-mailbox-activities"></a>Exchange 사서함 활동
  
다음 표에서는 사서함 감사 로깅에서 기록할 수 있는 활동을 보여 줍니다. 사서함 소유자, 위임된 사용자 또는 관리자가 수행한 사서함 활동은 최대 90일 동안 Office 365 감사 로그에 자동으로 기록됩니다. 관리자는 조직의 모든 사용자에 대한 사서함 감사 로깅을 해제할 수 있습니다. 이 경우 어떤 사용자에 대한 사서함 작업도 기록되지 않습니다. 자세한 내용은 [사서함 감사 관리](enable-mailbox-auditing.md)를 참조하세요.

 Exchange Online PowerShell에서 [Search-MailboxAuditLog](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-audit/search-mailboxauditlog) cmdlet을 사용하여 사서함 활동을 검색할 수도 있습니다. 
  
|**친숙한 이름**|**작업**|**설명**|
|:-----|:-----|:-----|
|대리인 사서함 사용 권한 추가됨  <br/> |AddMailboxPermissions  <br/> |관리자가 다른 사람의 사서함에 사용자(대리인)에 대한 FullAcess 사서함 사용 권한을 부여했습니다. FullAccess 사용 권한이 부여된 대리인은 다른 사람의 사서함을 열고 사서함의 콘텐츠를 읽거나 관리할 수 있습니다.  <br/> |
|일정 폴더에 대한 대리인 액세스 권한이 있는 사용자 추가 또는 제거 됨<br/> |UpdateCalendarDelegation<br/> |사용자가 다른 사용자의 사서함 일정에 대리인으로 추가 또는 제거되었습니다. 일정 위임 기능을 사용하여 같은 조직의 다른 사용자가 사서함 소유자의 일정을 관리할 수 있습니다. <br/> |
|폴더에 사용 권한 추가됨<br/> |AddFolderPermissions<br/> |폴더 사용 권한이 추가되었습니다. 폴더 사용 권한은 사서함의 폴더와 해당 폴더에 있는 메시지에 액세스할 수 있는 조직의 사용자를 제어합니다.<br/> |
|메시지가 다른 폴더에 복사됨  <br/> |복사  <br/> |메시지가 다른 폴더에 복사되었습니다.  <br/> |
|생성된 사서함 항목  <br/> |만들기  <br/> |항목이 사서함의 일정, 연락처, 메모 또는 작업 폴더에 만들어집니다. 예를 들면 새 모임 요청이 만들어집니다. 메시지 작성, 보내기 또는 받기는 감사되지 않습니다. 사서함 폴더 만들기도 감사되지 않습니다.  <br/> |
|Outlook 웹앱에서 새 편지함 규칙 만들어짐  <br/> |NewInboxRule<br/> |사서함에 액세스할 수 있는 사서함 소유자 또는 다른 사용자가 Outlook 웹앱에서 받은 편지함 규칙을 만들었습니다.<br/> |
|지운 편지함 폴더에서 메시지 삭제됨  <br/> |SoftDelete  <br/> |지운 편지함 폴더에서 메시지가 영구적으로 삭제 또는 삭제되었습니다. 이러한 항목은 복구 가능한 항목 폴더로 이동됩니다. 사용자가 메시지를 선택하고 **Shift+Delete**를 누르는 경우에도 복구 가능한 항목 폴더로 이동됩니다.  <br/> |
|메시지가 레코드로 지정됨  <br/> |ApplyRecordLabel<br/> |메시지가 레코드로 분류되었습니다. 이는 콘텐츠를 레코드로 분류하는 보존 레이블이 수동으로 또는 메시지에 자동으로 적용되는 경우 발생합니다.<br/> |
|메시지가 다른 폴더로 이동됨  <br/> |이동  <br/> |메시지가 다른 폴더로 이동되었습니다.  <br/> |
|메시지가 지운 편지함 폴더로 이동됨  <br/> |MoveToDeletedItems  <br/> |메시지가 삭제되어 지운 편지함 폴더로 이동되었습니다.  <br/> |
|폴더 권한이 수정됨  <br/> |UpdateFolderPermissions  <br/> |폴더 권한이 변경되었습니다. 폴더 권한은 사서함 폴더와 폴더의 메시지에 액세스할 수 있는 조직의 사용자를 제어합니다.  <br/> |
|Outlook 웹앱에서 받은 편지함 규칙이 수정됨<br/> |SetInboxRule<br/> |사서함에 액세스할 수 있는 사서함 소유자 또는 다른 사용자가 Outlook 웹앱을 사용하여 받은 편지함 규칙을 수정했습니다.<br/> |
|사서함에서 메시지 제거됨  <br/> |HardDelete  <br/> |메시지가 복구 가능한 항목 폴더에서 제거되었습니다(사서함에서 영구적으로 삭제됨).  <br/> |
|대리인 사서함 사용 권한 제거됨  <br/> |Remove-MailboxPermission  <br/> |관리자가 다른 사람의 사서함에서 (대리인에게 부여되었던) FullAccess 사용 권한을 제거했습니다. FullAccess 사용 권한이 제거되면 대리인이 더 이상 다른 사람의 사서함을 열거나 사서함의 콘텐츠에 액세스할 수 없습니다.  <br/> |
|폴더에서 사용 권한이 제거됨<br/> |RemoveFolderPermissions<br/> |폴더 사용 권한이 제거되었습니다. 폴더 사용 권한은 사서함의 폴더와 해당 폴더에 있는 메시지에 액세스할 수 있는 조직의 사용자를 제어합니다.<br/> |
|다른 사람 이름으로 보내기 권한을 사용하여 메시지 전송됨  <br/> |SendAs  <br/> |SendAs 권한을 사용하여 메시지가 전송되었습니다. 즉 사서함 소유자가 보낸 것처럼 보이도록 하여 다른 사용자가 메시지를 보냈습니다.  <br/> |
|대신 보내기 권한을 사용하여 메시지 전송됨  <br/> |SendOnBehalf  <br/> |SendOnBehalf 권한을 사용하여 메시지가 전송되었습니다. 즉 다른 사용자가 사서함 소유자 대신에 메시지를 보낸 것입니다. 이 메시지는 메시지가 대신 전송된 사람과 실제로 메시지를 보낸 사람을 받는 사람에게 알립니다.  <br/> |
|Outlook 클라이언트로부터 편지함 규칙 업데이트됨<br/> |UpdateInboxRules<br/> |사서함에 액세스할 수 있는 사서함 소유자 또는 다른 사용자가 Outlook 클라이언트에서 받은 편지함 규칙을 수정했습니다.<br/> |
|메시지 업데이트됨  <br/> |업데이트  <br/> |메시지 또는 해당 속성이 변경되었습니다.  <br/> |
|사용자가 사서함에 로그인함  <br/> |MailboxLogin  <br/> |사용자가 자신의 사서함에 로그인했습니다.  <br/> |
||||

### <a name="sway-activities"></a>Sway 활동
  
다음 표에서는 Sway의 사용자와 관리자 활동을 보여 줍니다. Sway는 사용자가 대화형 웹 기반 캔버스에서 아이디어, 스토리 및 프레젠테이션을 수집하고 서식을 지정한 다음 공유하는 데 도움이 되는 Office 365 앱입니다. 자세한 내용은 [Sway에 대한 질문과 대답 – 관리자 도움말](https://support.office.com/article/446380fa-25bf-47b2-996c-e12cb2f9d075)을 참조하세요.
  
|**친숙한 이름**|**작업**|**설명**|
|:-----|:-----|:-----|
|Sway 공유 수준 변경됨  <br/> |SwayChangeShareLevel  <br/> |사용자가 Sway의 공유 수준을 변경합니다. 이 이벤트는 사용자가 Sway와 연결된 공유 범위(예: 공개 및 조직 내부)를 변경하는 작업을 캡처합니다.  <br/> |
|Sway 만들어짐  <br/> |SwayCreate  <br/> |사용자가 Sway를 만듭니다.  <br/> |
|Sway 삭제됨  <br/> |SwayDelete  <br/> |사용자가 Sway를 삭제합니다.  <br/> |
|Sway 복제가 사용하지 않도록 설정됨  <br/> |SwayDisableDuplication  <br/> |사용자가 Sway 복제를 사용하지 않도록 설정합니다.  <br/> |
|Sway 복제됨  <br/> |SwayDuplicate  <br/> |사용자가 Sway를 복제합니다.  <br/> |
|Sway 편집됨  <br/> |SwayEdit  <br/> |사용자가 Sway를 편집합니다.  <br/> |
|Sway 복제가 사용하도록 설정됨  <br/> |EnableDuplication  <br/> |사용자가 Sway 복제를 사용도록 설정합니다. 사용자가 기본적으로 Sway 복제를 사용하도록 설정할 수 있습니다.  <br/> |
|Sway 공유 취소  <br/> |SwayRevokeShare  <br/> |사용자가 액세스 권한을 취소하여 Sway 공유를 중지합니다. 액세스 권한을 취소하면 Sway와 연결된 링크가 변경됩니다.  <br/> |
|Sway 공유됨  <br/> |SwayShare  <br/> |사용자가 Sway를 공유하려고 합니다. 이 이벤트는 Sway 공유 메뉴 내에서 특정 공유 대상을 클릭하는 사용자 작업을 캡처합니다. 이벤트에서 사용자가 공유 작업을 완료했는지 여부는 표시하지 않습니다.  <br/> |
|Sway 외부 공유 꺼짐  <br/> |SwayExternalSharingOff  <br/> |관리자가 Microsoft 365 관리 센터를 사용하여 전체 조직에 대해 외부 Sway 공유를 사용하지 않도록 설정합니다.  <br/> |
|Sway 외부 공유 켜짐  <br/> |SwayExternalSharingOn  <br/> |관리자가 Microsoft 365 관리 센터를 사용하여 전체 조직에 대해 외부 Sway 공유를 사용하도록 설정합니다.  <br/> |
|Sway 서비스 꺼짐  <br/> |SwayServiceOff  <br/> |관리자가 Microsoft 365 관리 센터를 사용하여 전체 조직에 대해 Sway를 사용하지 않도록 설정합니다.  <br/> |
|Sway 서비스 켜짐  <br/> |SwayServiceOn  <br/> |관리자가 Microsoft 365 관리 센터를 사용하여 전체 조직에 대해 Sway를 사용하도록 설정합니다(Sway 서비스는 기본적으로 사용됨).  <br/> |
|Sway 조회됨  <br/> |SwayView  <br/> |사용자가 Sway를 조회했습니다.  <br/> |
||||

  
### <a name="user-administration-activities"></a>사용자 관리 활동
  
다음 표에서는 365 관리 센터 또는 Azure 관리 포털을 사용하여 관리자가 사용자 계정을 추가하거나 변경할 때 기록되는 사용자 관리 활동을 보여 줍니다.
  
|**활동**|**작업**|**설명**|
|:-----|:-----|:-----|
|사용자 추가됨  <br/> |사용자 추가  <br/> |Office 365 사용자 계정이 생성되었습니다.  <br/> |
|사용자 라이선스 변경됨  <br/> |사용자 라이선스 변경  <br/> |사용자에게 할당된 라이선스가 변경되었습니다. 변경된 라이선스를 확인하려면 해당 **사용자 업데이트됨** 활동을 참조하세요.  <br/> |
|사용자 암호 변경됨  <br/> |사용자 암호 변경  <br/> |관리자가 사용자 암호를 변경했습니다.  <br/> |
|사용자 삭제됨  <br/> |사용자 삭제  <br/> |Office 365 사용자 계정이 삭제되었습니다.  <br/> |
|사용자 암호 재설정  <br/> |사용자 암호 재설정  <br/> |관리자가 사용자 암호를 재설정했습니다.  <br/> |
|강제로 사용자 암호를 변경하게 하는 속성 설정  <br/> |사용자 암호 강제 변경 설정  <br/> |관리자가 다음에 Office 365에 로그인할 때 강제로 사용자 암호를 변경하게 하는 속성을 설정했습니다.  <br/> |
|라이선스 속성 설정  <br/> |라이선스 속성 설정  <br/> |관리자가 사용자에게 할당된 라이선스의 속성을 수정했습니다.  <br/> |
|사용자 업데이트됨  <br/> |사용자 업데이트  <br/> |관리자가 사용자 계정의 속성을 하나 이상 변경합니다. 업데이트할 수 있는 사용자 속성 목록은 [Azure Active Directory 감사 보고서 이벤트](https://go.microsoft.com/fwlink/p/?LinkID=616549)에서 "사용자 속성 업데이트" 섹션을 참조하세요.  <br/> |
||||
  
### <a name="azure-ad-group-administration-activities"></a>Azure AD 그룹 관리 활동
  
다음 표에서는 관리자 또는 사용자가 Office 365 그룹을 만들거나 변경할 때 또는 관리자가 Microsoft 365 관리 센터 또는 Azure 관리 포털을 사용하여 보안 그룹을 만들 때 기록되는 그룹 관리 활동을 보여 줍니다. Office 365의 그룹에 대한 자세한 내용은 [Microsoft 365 관리 센터에서 그룹 보기, 만들기, 삭제](https://support.office.com/article/a6360120-2fc4-46af-b105-6a04dc5461c7)를 참조하세요.
  
|**친숙한 이름**|**작업**|**설명**|
|:-----|:-----|:-----|
|그룹 추가됨  <br/> |그룹 추가  <br/> |그룹이 생성되었습니다.  <br/> |
|그룹에 구성원 추가됨  <br/> |그룹에 구성원 추가  <br/> |그룹에 구성원이 추가되었습니다.  <br/> |
|그룹 삭제됨  <br/> |그룹 삭제  <br/> |그룹이 삭제되었습니다.  <br/> |
|그룹에서 구성원 제거됨  <br/> |그룹에서 구성원 제거  <br/> |그룹에서 구성원이 제거되었습니다.  <br/> |
|그룹 업데이트됨  <br/> |그룹 업데이트  <br/> |그룹의 속성이 변경되었습니다.  <br/> |
||||
   
### <a name="application-administration-activities"></a>응용 프로그램 관리 활동
  
다음 표에서는 관리자가 Azure AD에 등록된 응용 프로그램을 추가하거나 변경할 때 기록되는 응용 프로그램 관리 활동을 보여 줍니다. Azure AD를 인증에 사용하는 응용 프로그램은 모두 디렉터리에 등록되어야 합니다.
  
|**친숙한 이름**|**작업**|**설명**|
|:-----|:-----|:-----|
|위임 항목 추가됨  <br/> |위임 항목 추가  <br/> |Azure AD에서 인증 권한이 생성/응용 프로그램에 부여되었습니다.  <br/> |
|서비스 사용자 추가됨  <br/> |서비스 사용자 추가  <br/> |응용 프로그램이 Azure AD에 등록되었습니다. 응용 프로그램은 디렉터리에서 서비스 사용자로 표시됩니다.  <br/> |
|서비스 사용자에 자격 증명 추가됨   <br/> |서비스 사용자 자격 증명 추가  <br/> |Azure AD의 서비스 사용자에 자격 증명이 추가되었습니다. 서비스 사용자는 디렉터리의 응용 프로그램을 나타냅니다.  <br/> |
|위임 항목 제거됨  <br/> |위임 항목 제거  <br/> |Azure AD의 응용 프로그램에서 인증 권한이 제거되었습니다.  <br/> |
|디렉터리에서 서비스 사용자 제거됨  <br/> |서비스 사용자 제거  <br/> |응용 프로그램이 Azure AD에서 삭제/등록 취소되었습니다. 응용 프로그램은 디렉터리에서 서비스 사용자로 표시됩니다.  <br/> |
|서비스 사용자에서 자격 증명 제거됨   <br/> |서비스 사용자 자격 증명 제거  <br/> |Azure AD의 서비스 사용자에서 자격 증명이 제거되었습니다. 서비스 사용자는 디렉터리의 응용 프로그램을 나타냅니다.  <br/> |
|위임 항목 설정  <br/> |위임 항목 설정  <br/> |Azure AD의 응용 프로그램에 대해 인증 권한을 업데이트했습니다.  <br/> |
||||

### <a name="role-administration-activities"></a>역할 관리 활동
  
다음 표에서는 Microsoft 365 관리 센터 또는 Azure 관리 포털에서 관리자가 관리자 역할을 관리할 때 기록되는 Azure AD 관리 활동을 보여줍니다.
  
|**친숙한 이름**|**작업**|**설명**|
|:-----|:-----|:-----|
|역할에 구성원 추가  <br/> |역할에 역할 구성원 추가  <br/> |Office 365의 관리자 역할에 사용자를 추가했습니다.  <br/> |
|디렉터리 역할에서 사용자 제거됨  <br/> |역할에서 역할 구성원 제거  <br/> |Office 365의 관리자 역할에서 사용자를 제거했습니다.  <br/> |
|회사 연락처 정보 설정  <br/> |회사 연락처 정보 설정  <br/> |Office 365 조직에 대한 회사 차원의 연락처 기본 설정을 업데이트했습니다. 여기에는 Office 365에서 보내는 구독 관련 전자 메일의 전자 메일 주소와 Office 365 서비스에 대한 기술 알림이 포함됩니다.  <br/> |
||||
   
### <a name="directory-administration-activities"></a>디렉터리 관리 활동
  
다음 표에서는 Microsoft 365 관리 센터 또는 Azure 관리 포털에서 관리자가 해당 Office 365 조직을 관리할 때 기록되는 Azure AD 디렉터리 및 도메인 관련 활동을 보여줍니다.
  
|**친숙한 이름**|**작업**|**설명**|
|:-----|:-----|:-----|
|회사에 도메인 추가됨  <br/> |회사에 도메인 추가  <br/> |Office 365 조직에 도메인을 추가합니다.  <br/> |
|디렉터리에 파트너 추가됨  <br/> |회사에 파트너 추가  <br/> |Office 365 조직에 파트너(위임된 관리자)를 추가했습니다.  <br/> |
|회사에서 도메인 제거됨  <br/> |회사에서 도메인 제거  <br/> |Office 365 조직에서 도메인을 제거했습니다.  <br/> |
|디렉터리에서 파트너 제거됨  <br/> |회사에서 파트너 제거  <br/> |Office 365 조직에서 파트너(위임된 관리자)를 제거했습니다.  <br/> |
|회사 정보 설정  <br/> |회사 정보 설정  <br/> |Office 365 조직에 대한 회사 정보를 업데이트했습니다. 여기에는 Office 365에서 보내는 구독 관련 전자 메일의 전자 메일 주소와 Office 365 서비스에 대한 기술 알림이 포함됩니다.  <br/> |
|도메인 인증 설정  <br/> |도메인 인증 설정  <br/> |Office 365 조직에 대한 도메인 인증 설정을 변경했습니다.  <br/> |
|도메인에 대한 페더레이션 설정 업데이트됨  <br/> |도메인에 대한 페더레이션 설정 지정  <br/> |Office 365 조직에 대한 페더레이션(외부 공유) 설정을 변경했습니다.  <br/> |
|암호 정책 설정  <br/> |암호 정책 설정  <br/> |Office 365 조직의 사용자 암호에 대한 길이 및 문자 제약 조건을 변경했습니다.  <br/> |
|Azure AD 동기화 설정됨  <br/> |회사에 대해 DirSyncEnabled 플래그 설정  <br/> |Azure AD 동기화에 대해 디렉터리를 사용하도록 설정하는 속성을 설정합니다.  <br/> |
|도메인 업데이트됨  <br/> |도메인 업데이트  <br/> |Office 365 조직의 도메인 설정을 업데이트했습니다.  <br/> |
|도메인 확인됨  <br/> |도메인 확인  <br/> |조직이 도메인의 소유자임을 확인했습니다.  <br/> |
|전자 메일 확인 도메인 확인됨  <br/> |전자 메일 확인 도메인 확인  <br/> |전자 메일 확인을 사용하여 조직이 도메인의 소유자임을 확인했습니다.  <br/> |
||||
   
### <a name="ediscovery-activities"></a>eDiscovery 활동
  
보안 및 준수 센터에서 또는 해당 PowerShell cmdlet을 실행하여 수행한 콘텐츠 검색 및 eDiscovery 관련 활동은 감사 로그에 기록됩니다. 여기에는 다음과 같은 활동이 포함됩니다.
  
- eDiscovery 사례 만들기 및 관리
    
- 콘텐츠 검색 만들기, 시작 및 편집
    
- 검색 결과 미리 보기, 내보내기, 삭제 등 콘텐츠 검색 작업 수행
    
- 콘텐츠 검색에 대한 사용 권한 필터링 구성
    
- eDiscovery 관리자 역할 관리
    
기록되는 eDiscovery 활동의 목록과 자세한 설명을 보려면 [Office 365 감사 로그에서 eDiscovery 활동 검색](search-for-ediscovery-activities-in-the-audit-log.md)을 참조하세요.
  
> [!NOTE]
> **활동** 드롭다운 목록의 **eDiscovery 활동** 아래에 나열된 활동에서 발생한 이벤트가 검색 결과에 표시될 때까지 최대 30분이 걸립니다. 반대로, eDiscovery cmdlet 활동의 해당 이벤트가 검색 결과에 나타날 때까지는 최대 24시간이 걸립니다. 
  
### <a name="advanced-ediscovery-activities"></a>고급 eDiscovery 활동

다음 표에는 Microsoft 365의 고급 eDiscovery에 대한 작업을 수행하는 IT 및 법인 전문가의 활동 목록이 나와 있습니다. 자세한 내용은 M[icrosoft 365의 고급 eDiscovery 솔루션 개요](compliance20/overview-ediscovery-20.md)를 참조하세요.

|**친숙한 이름**|**작업**|**설명**|
|:-----|:-----|:-----|
| 다른 검토 집합에 데이터 추가됨<br/>         | AddWorkingSetQueryToWorkingSet<br/>  |  사용자가 한 검토 집합에서 다른 검토 집합으로 문서를 추가했습니다.<br/>|
| 검토 집합에 데이터 추가됨 <br/>                | AddQueryToWorkingSet<br/>            |  사용자가 고급 eDiscovery 사례와 연결된 콘텐츠 검색에서 검토 집합에 검색 결과를 추가했습니다.<br/>|
| 검토 집합에 비 Office 365 데이터 추가<br/>  | AddNonOffice365DataToWorkingSet<br/> |  사용자가 검토 집합에 비 Office 365 데이터를 추가했습니다.<br/>|
| 수정된 문서가 검토 집합에 추가됨<br/> | AddRemediatedData<br/>               |  사용자가 검토 집합으로 수정된 색인 작성 오류가 있는 문서를 업로드합니다.<br/>|
| 검토 집합의 데이터가 분석됨 <br/>             | RunAlgo<br/>                         |  사용자가 검토 집합의 문서에 대한 분석을 실행했습니다. <br/>|
| 검토 집합의 문서에 주석이 달림 <br/>        | AnnotateDocument<br/>                |  사용자가 검토 집합의 문서에 주석을 달았습니다. 주석에는 문서의 내용을 편집하는 것이 포함되어 있습니다.  <br/>|
| 부하 집합 비교됨 <br/>                      | LoadComparisonJob<br/>               |사용자가 검토 집합에서 서로 다른 두 개의 부하 집합을 비교했습니다. 부하 집합은 사례와 연결된 콘텐츠 검색 데이터가 검토 집합에 추가되는 경우입니다.  <br/>|
| 편집된 문서가 PDF로 변환됨<br/>      | BurnJob<br/>                         |사용자가 검토의 모든 편집된 문서를 PDF 파일로 변환했습니다.<br/>|
| 검토 집합 생성됨<br/>                       | CreateWorkingSet<br/>                |사용자가 검토 집합을 만들었습니다.<br/>|
| 검토 집합 검색 생성됨<br/>                | CreateWorkingSetSearch<br/>          |사용자가 검토 집합에서 문서를 검색하는 검색 쿼리를 만들었습니다. <br/>|
| 태그 생성됨<br/>                              | 태그 생성<br/>                       |사용자가 검토 집합에 태그 그룹을 만들었습니다. 태그 그룹에는 하나 이상의 하위 태그가 포함될 수 있습니다. 그런 다음 이 태그를 사용하여 검토 집합의 문서에 태그를 지정합니다.<br/>|
| 검토 집합 검색 삭제됨 <br/>               | DeleteWorkingSetSearch<br/>          |사용자가 검토 집합에서 검색 쿼리를 삭제했습니다.<br/>|
| 태그 삭제됨<br/>                              | DeleteTag<br/>                       |사용자가 검토 집합의 태그 그룹을 삭제었습니다.<br/>|
| 문서 다운로드됨<br/>                      | DownloadDocument<br/>                |사용자가 검토 집합에서 문서를 다운로드했습니다.<br/>|
| 태그 편집됨 <br/>                              | DownloadDocument<br/>                |사용자가 검토 집합에서 태그를 변경했습니다.<br/>|
| 검토 집합에서 문서 내보냄 <br/>      | ExportJob<br/>                       |사용자가 검토 집합에서 문서를 내보냈습니다.<br/>|
| 사례 설정 수정됨 <br/>                   | UpdateCaseSettings<br/>              | 사용자가 사례에 대한 설정을 수정했습니다. 사례 설정에는 사례 정보, 액세스 권한 및 검색 및 분석 동작을 제어하는 설정이 포함됩니다.<br/>|
| 검토 집합 검색 수정됨<br/>               | UpdateWorkingSetSearch<br/>          |  사용자가 검토 집합에서 검색 쿼리를 편집했습니다.<br/>|
| 검토 집합 검색 미리 보기됨 <br/>             | PreviewWorkingSetSearch<br/>         |  사용자가 검토 집합에 검색 쿼리의 결과를 미리 보았습니다.<br/>|
| 오류 문서 수정됨 <br/>              | ErrorRemediationJob<br/>             |  사용자가 인덱싱 오류가 있는 파일을 수정합니다. <br/>|
| 문서에 태그가 지정됨<br/>                          | TagFiles<br/>                        |  사용자가 검토 집합의 문서에 태그를 지정합니다.<br/>|
| 쿼리의 결과가 태그됨<br/>                | TagJob<br/>                          |  사용자는 검토 집합의 검색 쿼리 조건과 일치하는 모든 문서를 태그합니다.<br/>|
| 검토 집합의 문서 조회됨<br/>            | ViewDocument<br/>                    |  사용자가 검토 집합의 문서를 조회했습니다.<br/>|
|||

### <a name="power-bi-activities"></a>Power BI 활동
  
Power BI에서 활동에 대한 감사 로그를 검색할 수 있습니다. Power BI 활동에 대한 자세한 내용은 [조직 내에서 감사 사용](https://docs.microsoft.com/power-bi/service-admin-auditing#activities-audited-by-power-bi)의 "Power BI가 감사한 활동" 섹션을 참조하세요.
  
Power BI에 대 한 감사 로깅은 기본적으로 사용하지 않도록 설정되어 있습니다. Office 365 감사 로그에서 Power BI 작업을 검색하려면 Power BI 관리 포털에서 감사를 사용하도록 설정해야 합니다. 자세한 내용은 [Power BI 관리 포털](https://docs.microsoft.com/power-bi/service-admin-portal#audit-logs)의 "감사 로그" 섹션을 참조 하세요.
  
### <a name="microsoft-workplace-analytics-activities"></a>Microsoft Workplace Analytics 활동

Workplace Analytics는 Office 365 조직에서 그룹이 공동으로 작업하는 방법에 대한 정보를 줍니다. 다음 표는 Workplace Analytics에서 관리자 역할 또는 분석가 역할이 할당된 사용자가 수행한 활동을 나열합니다. 분석 역할이 할당된 사용자는 모든 서비스 기능에 대한 전체 액세스 권한을 가지며 제품을 사용하여 분석을 수행합니다. 관리자 역할이 할당된 사용자는 개인 정보 설정 및 시스템 기본값을 구성하고 Workplace Analytics에서 조직 데이터를 준비, 업로드 및 확인할 수 있습니다. 자세한 내용은 [Workplace Analytics](https://docs.microsoft.com/ko-KR/workplace-analytics/index-orig)를 참조하세요.

|**친숙한 이름**|**작업**|**설명**|
|:-----|:-----|:-----|
|OData 링크 액세스됨 <br/> |AccessedOdataLink <br/> |분석가가 쿼리에 대해 OData 링크에 액세스했습니다.|
|쿼리 취소됨 <br/> |CanceledQuery <br/> |분석가가 실행 중인 쿼리를 취소했습니다.|
|모임 제외 만들어짐 <br/> |MeetingExclusionCreated <br/> |분석가가 모임 제외 규칙을 만들었습니다.|
|결과 삭제됨 <br/> |DeletedResult <br/> |분석가가 쿼리 결과를 삭제했습니다.|
|보고서 다운로드됨 <br/> |DownloadedReport <br/> |분석가가 쿼리 결과 파일을 다운로드했습니다.|
|쿼리 실행됨 <br/> |ExecutedQuery <br/> |분석가가 쿼리를 실행했습니다.|
|데이터 액세스 설정 업데이트됨 <br/> |UpdatedDataAccessSetting <br/> |관리자가 데이터 액세스 설정을 업데이트했습니다.|
|개인 정보 설정 업데이트됨 <br/> |UpdatedPrivacySetting <br/> |관리자가 개인 정보 설정을 업데이트했습니다.(예: 최소 그룹 크기)|
|조직 데이터가 업로드됨 <br/> |UploadedOrgData <br/> |관리자가 조직 데이터 파일을 업로드했습니다.|
|탐색 보기 <br/> |ViewedExplore <br/> |분석가가 하나 이상의 탐색 페이지 탭에서 시각화를 봤습니다.|
||||

### <a name="microsoft-teams-activities"></a>Microsoft Teams 활동
  
다음 표에서는 Microsoft Teams에서 Office 365 감사 로그에 기록되는 사용자 및 관리자 활동을 보여 줍니다. Microsoft 팀은 Office 365에서 채팅 중심의 작업 영역입니다. Microsoft Teams를 사용하면 팀의 대화, 모임, 파일 및 메모를 모두 한곳에서 관리할 수 있습니다. 자세한 내용과 도움말 항목에 대한 링크는 다음을 참조하세요.
  
- [Microsoft Teams에 대한 질문과 대답 – 관리 도움말](https://support.office.com/article/05cbe533-2181-4e95-a4b0-52cd7695fafc)
    
- [Microsoft Teams 도움말](https://support.office.com/article/23156c0c-2c6e-49dd-8b7b-7c564b76508c)
    
|**친숙한 이름**|**작업**|**설명**|
|:-----|:-----|:-----|
|팀에 봇이 추가됨  <br/> |BotAddedToTeam  <br/> |사용자가 팀에 봇을 추가합니다.  <br/> |
|채널 추가됨  <br/> |ChannelAdded  <br/> |사용자가 팀에 채널을 추가합니다.  <br/> |
|커넥터 추가됨  <br/> |ConnectorAdded  <br/> |사용자가 채널에 커넥터를 추가합니다.  <br/> |
|팀에 구성원이 추가됨  <br/> |MemberAdded  <br/> |팀 소유자가 팀에 구성원을 추가합니다.  <br/> |
|탭 추가됨  <br/> |TabAdded  <br/> |사용자가 채널에 탭을 추가합니다.  <br/> |
|채널 설정 변경함  <br/> |ChannelSettingChanged  <br/> | ChannelSettingChanged 작업은 팀 구성원이 다음 활동을 수행하는 경우 로깅됩니다. 각 활동에 대해 감사 로그 검색 결과의 **항목** 열에 변경된 설정에 대한 설명(아래에서 괄호 안에 표시된 내용)이 표시됩니다.  <br/> <br/>- 팀 채널의 이름을 변경합니다(**채널 이름**).  <br/>  <br/>- 팀 채널의 설명을 변경합니다(**채널 설명**).  <br/> |
|조직 설정 변경함  <br/> |TeamsTenantSettingChanged  <br/> | TeamsTenantSettingChanged 작업은 Microsoft 365 관리 센터를 사용하여 전역 관리자가 다음 활동을 수행할 때 기록됩니다. 이러한 활동은 조직 전체의 Microsoft Teams 설정에 영향을 미칩니다. 자세한 내용은 [Microsoft Teams의 관리자 설정](https://support.office.com/article/3966a3f5-7e0f-4ea9-a402-41888f455ba2)을 참조하세요.  <br/>  각 활동에 대해 감사 로그 검색 결과의 **항목** 열에 변경된 설정에 대한 설명(아래에서 괄호 안에 표시된 내용)이 표시됩니다.  <br/><br/>- 조직에서 Microsoft Teams를 사용하거나 사용하지 않도록 설정합니다(**Microsoft Teams**).  <br/><br/>- 조직에서 Microsoft Teams과 비즈니스용 skype 사이의 상호 운용성을 활성화하거나 비활성화합니다(**비즈니스용 skype 상호 운용성**).<br/><br/>-Microsoft Teams 클라이언트에서 조직도 보기를 사용하거나 사용하지 않습니다(조직도 보기 **).  <br/><br/>- 팀 구성원이 비공개 모임을 예약할 수 있는 기능을사용하거나 사용하지 않도록 설정합니다(** 비공개 모임 예약 **).  <br/><br/>- 팀 구성원이 채널 모임을 예약하는 기능을 사용하거나 사용하지 않도록 설정합니다(채널 모임 예약**).  <br/><br/>- 팀 회의에서 비디오 통화를 사용하거나 사용하지 않도록 설정합니다(Skype 모임용 비디오 **).  <br/><br/>- 조직의 Microsoft Teams 모임에서 화면 공유를 사용하거나 사용하지 않도록 설정합니다(** Skype 모임의 화면 공유 **).  <br/><br/>- 팀 대화(애니메이션 이미지**)에 애니메이션 이미지(Giphys라고 함)를 추가하는 기능을 사용하거나 사용하지 않도록 설정합니다.  <br/><br/>- 조직의 콘텐츠 등급 설정을 변경합니다(**콘텐츠 등급**). 콘텐츠 등급으로 인해 대화에 표시될 수 있는 애니메이션 이미지의 유형이 제한됩니다.  <br/><br/>- 팀 구성원이 사용자 지정할 수 있는 이미지(사용자 지정 memes라고 함)를 인터넷에서 팀 대화에 추가할 수 있도록 허용하거나 허용하지 않습니다(인터넷에서 사용자 지정할 수 있는 이미지 **).  <br/><br/>- 팀 구성원이 편집할 수 있는 이미지(스티커)를 팀 대화에 추가할 수 있도록 허용하거나 허용하지 않습니다(** 편집할 수 있는 이미지 **).  <br/><br/>- 팀원들이 Microsoft Teams에서 봇을 사용할 수 있도록 허용하거나 허용하지 않습니다(조직 전체 봇**).<br/><br/>- Microsoft Teams의 전용 봇을 활성화합니다. 조직에서 봇이 활성화된 경우 사용할 수 있는 Teams 도움말 봇인 T-Bot은 여기에 포함되지 않습니다(**개별 봇**).  <br/><br/>- 팀 구성원이 확장자 또는 탭을 추가할 수 있도록 허용하거나 허용하지 않습니다(**확장자 또는 탭**).  <br/><br/>Microsoft Teams용 독점 봇의 테스트용 로드 기능을 활성화하거나 비활성화합니다(**봇의 테스트용 로드**).  <br/><br/>사용자가 Microsoft Teams 채널로 전자 메일 메시지를 보낼 수 있도록 허용하거나 허용하지 않습니다(**채널 전자 메일**).  <br/> |
|팀의 구성원 역할이 변경됨  <br/> |MemberRoleChanged  <br/> |팀 소유자가 팀의 구성원 역할을 변경합니다. 다음 값은 사용자에게 할당된 역할 유형을 나타냅니다.  <br/><br/><br/> **1** - 소유자 역할을 나타냅니다.<br/>**2** - 구성원 역할을 나타냅니다. <br/>**3** - 게스트 역할을 나타냅니다. <br/>구성원 속성에는 조직의 이름 및 구성원의 전자 메일 주소도 포함됩니다.  <br/> |
|팀 설정 변경함  <br/> |TeamSettingChanged  <br/> | TeamSettingChanged 작업은 팀 소유자가 다음 활동을 수행하는 경우 로깅됩니다. 각 활동에 대해 감사 로그 검색 결과의 **항목** 열에 변경된 설정에 대한 설명(아래에서 괄호 안에 표시된 내용)이 표시됩니다.  <br/><br/>- 팀의 액세스 유형을 변경합니다. 팀은 비공개 또는 공개로 설정될 수 있습니다(**팀 액세스 유형**). 비공개 팀(기본값)은 초대받은 사용자만 액세스할 수 있습니다. 공개 팀은 누구나 검색할 수 있습니다.  <br/><br/>- 팀의 정보 분류를 변경합니다(**팀 분류**).  <br/>  예를 들어, 팀 데이터는 높은 비즈니스 영향, 중간 비즈니스 영향 또는 낮은 비즈니스 영향으로 분류될 수 있습니다.<br/><br/>- 팀의 이름을 변경합니다(**팀 이름**).  <br/><br/>- 팀 설명을 변경합니다(팀 설명**). <br/><br/>- 팀 설정에 대한 변경 사항입니다. 팀 소유자는 팀을 마우스 오른쪽 단추로 클릭하고 **팀 관리**를 클릭한 다음 **설정** 탭을 클릭하여 Teams 클라이언트에서 이러한 설정에 액세스할 수 있습니다. 이러한 활동에 대해 변경된 설정의 이름이 감사 로그 검색 결과의 **항목** 열에 표시됩니다.  <br/> |
|팀 생성됨  <br/> |TeamCreated  <br/> |사용자가 팀을 만듭니다.  <br/> |
|채널 삭제됨  <br/> |ChannelDeleted  <br/> |사용자는 팀에서 채널을 삭제합니다.  <br/> |
|팀 삭제됨  <br/> |TeamDeleted  <br/> |팀 소유자가 팀을 삭제합니다.  <br/> |
|팀에서 봇이 제거됨  <br/> |BotRemovedFromTeam  <br/> |사용자가 팀에서 봇을 제거합니다.  <br/> |
|커넥터 제거됨  <br/> |ConnectorRemoved  <br/> |사용자가 채널에 커넥터를 제거합니다.  <br/> |
|팀에서 구성원이 제거됨  <br/> |MemberRemoved  <br/> |팀 소유자가 팀에서 구성원을 제거합니다.  <br/> |
|탭 제거됨  <br/> |TabRemoved  <br/> |사용자는 채널에서 탭을 제거합니다.  <br/> |
|커넥터가 업데이트됨  <br/> |ConnectorUpdated  <br/> |사용자가 채널의 커넥터를 수정했습니다.  <br/> |
|탭이 업데이트됨  <br/> |TabUpdated  <br/> |사용자가 채널의 탭을 수정했습니다.  <br/> |
|사용자가 Teams에 로그인함  <br/> |TeamsSessionStarted  <br/> |사용자가 Microsoft Teams 클라이언트에 로그인합니다.  <br/> |
||||

### <a name="yammer-activities"></a>Yammer 활동
  
다음 표에서는 Yammer에서 Office 365 감사 로그에 기록되는 사용자 및 관리자 활동을 보여 줍니다. Office 365 감사 로그에서 Yammer 관련 활동을 반환하려면 **활동** 목록에서 **모든 활동에 대한 결과 표시**를 선택해야 합니다. 날짜 범위 상자와 **사용자** 목록을 사용하여 결과를 좁힙니다. 
  
|**친숙한 이름**|**작업**|**설명**|
|:-----|:-----|:-----|
|데이터 보존 정책이 변경됨  <br/> |SoftDeleteSettingsUpdated  <br/> |확인된 관리자가 네트워크 데이터 보존 정책의 설정을 영구 삭제 또는 일시 삭제로 업데이트했습니다. 이 작업은 확인된 관리자만 수행할 수 있습니다.  <br/> |
|네트워크 구성이 변경됨  <br/> |NetworkConfigurationUpdated  <br/> |네트워크 관리자 또는 확인된 관리자가 Yammer 네트워크의 구성을 변경했습니다. 여기에는 데이터 내보내기 간격 및 채팅 활성화 설정이 포함됩니다.  <br/> |
|네트워크 프로필 설정이 변경됨  <br/> |ProcessProfileFields  <br/> |네트워크 관리자 또는 확인된 관리자가 네트워크 사용자 네트워크의 회원 프로필에 표시되는 정보를 변경합니다.  <br/> |
|비공개 콘텐츠 모드가 변경됨  <br/> |SupervisorAdminToggled  <br/> |확인된 관리자가 *비공개 콘텐츠 모드*를 끄거나 켭니다. 이 모드를 통해 관리자는 비공개 그룹의 게시물을 보고 개별 사용자(또는 사용자 그룹) 간 비공개 메시지를 볼 수 있습니다. 이 작업은 확인된 관리자만 수행할 수 있습니다.  <br/> |
|보안 구성이 변경됨  <br/> |NetworkSecurityConfigurationUpdated  <br/> |확인된 관리자가 Yammer 네트워크의 보안 구성을 업데이트했습니다. 여기에는 암호 만료 정책 및 IP 주소 제한 설정이 포함됩니다. 이 작업은 확인된 관리자만 수행할 수 있습니다.  <br/> |
|파일이 생성됨  <br/> |FileCreated  <br/> |사용자가 파일을 업로드했습니다.  <br/> |
|그룹 생성됨  <br/> |GroupCreation  <br/> |사용자가 그룹을 만듭니다.  <br/> |
|그룹 삭제됨  <br/> |GroupDeletion  <br/> |Yammer에서 그룹이 삭제되었습니다.  <br/> |
|메시지가 삭제됨  <br/> |MessageDeleted  <br/> |사용자가 메시지를 삭제했습니다.  <br/> |
|다운로드한 파일  <br/> |FileDownloaded  <br/> |사용자가 파일을 다운로드했습니다.  <br/> |
|데이터를 내보냄  <br/> |DataExport  <br/> |확인된 관리자가 Yammer 네트워크 데이터를 내보냈습니다. 이 작업은 확인된 관리자만 수행할 수 있습니다.  <br/> |
|파일이 공유됨  <br/> |FileShared  <br/> |사용자가 다른 사용자와 파일을 공유했습니다.  <br/> |
|네트워크 사용자가 일시 중단됨  <br/> |NetworkUserSuspended  <br/> |네트워크 관리자 또는 확인된 관리자가 Yammer에서 사용자를 일시 중단(비활성화)했습니다.  <br/> |
|사용자가 일시 중단됨  <br/> |UserSuspension  <br/> |사용자 계정이 일시 중단(비활성화)되었습니다.  <br/> |
|파일 설명이 업데이트됨  <br/> |FileUpdateDescription  <br/> |사용자가 파일의 설명을 변경했습니다.  <br/> |
|파일 이름이 업데이트됨  <br/> |FileUpdateName  <br/> |사용자가 파일의 이름을 변경했습니다.  <br/> |
|파일이 조회됨  <br/> |FileVisited  <br/> |사용자가 파일을 조회했습니다.  <br/> |
||||
   
### <a name="microsoft-flow-activities"></a>Microsoft Flow 활동

Microsoft Flow에서 활동에 대한 감사 로그를 검색할 수 있습니다. 이러한 활동에는 흐름 만들기, 편집, 삭제 및 흐름 사용 권한 변경이 포함됩니다. Flow 활동을 감사하는 방법에 대한 자세한 내용은 [현재 보안 및 준수 센터에서 사용할 수 있는 Microsoft Flow 감사 이벤트](https://flow.microsoft.com/blog/security-and-compliance-center)를 블로그에서 참조하세요.

### <a name="microsoft-powerapps"></a>Microsoft PowerApps

PowerApps에서 활동에 대한 감사 로그를 검색할 수 있습니다. 이러한 활동에는 앱을 만들고, 시작하고, 게시하는 작업이 포함됩니다. 앱에 대한 사용 권한을 할당하는 방법도 감사할 수 있습니다. 모든 PowerApps 활동에 대한 설명은 [PowerApps에 대한 활동 로깅](https://docs.microsoft.com/ko-KR/power-platform/admin/logging-powerapps#what-events-are-audited)을 참조하세요.

### <a name="microsoft-stream-activities"></a>Microsoft Stream 활동
  
Microsoft Stream에서 활동에 대한 감사 로그를 검색할 수 있습니다. 이러한 활동에는 사용자가 수행한 비디오 활동, 그룹 채널 활동 및 관리자 활동(예: 사용자 관리, 조직 설정 관리, 보고서 내보내기 등)이 포함됩니다. 이러한 활동에 대 한 설명은 [Microsoft Stream의 감사 로그](https://docs.microsoft.com/stream/audit-logs)에서 "Microsoft Stream에 기록된 활동" 섹션을 참조하세요.

### <a name="exchange-admin-audit-log"></a>Exchange 관리자 감사 로그
  
관리자(또는 관리 권한이 할당 된 사용자)가 Exchange Online 조직에서 변경 작업을 수행할 때 Exchange 관리자 감사 로깅(Office 365에서 기본적으로 사용하도록 설정됨)은 Office 365 감사 로그에 이벤트를 기록합니다. Exchange 관리 센터를 사용하거나 Exchange Online PowerShel에서 cmdlet을 실행하여 수행한 변경 내용은 Exchange 관리 감사 로그에 기록 됩니다. **Get-**, **Search-** 또는 **Test-** 동사로 시작하는 cmdlet은 Office 365 감사 로그에 기록되지 않습니다. Exchange의 관리자 감사 로깅에 대한 자세한 내용은 [관리자 감사 로깅](https://go.microsoft.com/fwlink/p/?LinkID=619225)을 참조하세요.

> [!IMPORTANT]
> Exchange 관리자 감사 로그(또는 Office 365 감사 로그)에 기록되지 않는 일부 Exchange Online cmdlet도 있습니다. 이러한 cmdlet 중 다수는 Exchange Online 서비스 유지 관리와 관련이 있으며 Microsoft 데이터 센터 직원 또는 서비스 계정에 의해 실행됩니다. 이 cmdlet은 많은 양의 "소음이 발생 하는" 감사 이벤트를 생성하므로 기록되지 않습니다. 감사되지 않는 Exchange Online cmdlet이 있으면 [Office 365 보안 및 규정 준수 사용자 음성 포럼](https://office365.uservoice.com/forums/289138-office-365-security-compliance)에 제안 사항을 제출하고 감사를 사용할 수 있도록 요청하세요. DCR(디자인 변경 요청)를 Microsoft 지원에 제출할 수도 있습니다.
  
다음은 Office 365 감사 로그를 검색하는 경우 Exchange 관리 활동을 검색하기 위한 몇 가지 팁입니다.
  
- Exchange 관리자 감사 로그의 항목을 반환하려면 **활동** 목록에서 **모든 활동에 대한 결과 표시**를 선택해야 합니다. 날짜 범위 상자와 **사용자** 목록을 사용하여 특정 Exchange 관리자가 특정 날짜 범위 내에 실행한 cmdlet에 대한 검색 결과로 범위를 좁힙니다. 
    
- Exchange 관리자 감사 로그의 이벤트를 표시하려면 검색 결과를 필터링하고 **활동** 필터 상자에 **-**(대시)를 입력합니다. Exchange 관리자 이벤트에 대한 **활동** 열에 표시되는 cmdlet 이름이 나타납니다. 그런 다음 cmdlet 이름을 사전순으로 정렬할 수 있습니다. 
    
    ![Exchange 관리 이벤트를 필터링하려면 작업 상자에 대시를 입력합니다.](media/7628e7aa-6263-474a-a28b-2dcf5694bb27.png)
  
- 실행된 cmdlet, 사용된 매개 변수 및 매개 변수 값, 영향을 받은 개체에 대한 정보를 가져오려면 **모든 결과 다운로드** 옵션을 선택하여 검색 결과를 내보낼 수 있습니다. 자세한 내용은 [감사 로그 레코드 내보내기, 구성 및 보기](export-view-audit-log-records.md)를 참조하세요. 

- Exchange Online PowerShell에서 `Search-UnifiedAuditLog -RecordType ExchangeAdmin` 명령을 사용하여 Exchange 관리자 감사 로그의 감사 레코드만 반환할 수도 있습니다. Exchange cmdlet가 실행된 후 해당 감사 로그 항목이 검색 결과에 반환되려면 최대 30분이 걸릴 수 있습니다. 자세한 내용은 [Search-UnifiedAuditLog](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-audit/search-unifiedauditlog)를 참조하세요. **Search-UnifiedAuditLog** cmdlet에서 반환되는 검색 결과를 CSV 파일로 내보내는 방법에 대한 자세한 내용은 [감사 로그 레코드 내보내기, 구성 및 보기](export-view-audit-log-records.md#tips-for-exporting-and-viewing-the-audit-log)의 "감사 로그 내보내기 및 보기 팁" 섹션을 참조하세요.

- Exchange 관리 센터를 사용하거나 Exchange Online PowerShell에서 **Search-AdminAuditLog**를 실행하여 Exchange 관리자 감사 로그에서 이벤트를 볼 수도 있습니다. 이 방법은 Exchange Online 관리자가 수행하는 활동을 구체적으로 검색하는 좋은 방법입니다. 해당 지침은 다음 항목을 참조하세요.
   
   - [관리자 감사 로그 보기](https://technet.microsoft.com/library/dn342832%28v=exchg.150%29.aspx) 
   
   -  [Search-AdminAuditLog](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-audit/search-adminauditlog)
   
   동일한 Exchange 관리 활동은 Exchange 관리자 감사 로그 및 Office 365 감사 로그에 모두 기록됩니다.
  
## <a name="frequently-asked-questions"></a>자주하는 질문

**Office 365의 감사 서비스에서 제공하는 기능에 대한 자세한 내용은 어디에서 찾을 수 있나요?**

Office 365에서 사용할 수 있는 감사 및 보고 기능에 대한 자세한 내용은 [Office 365에서 감사 및 보고](office-365-auditing-and-reporting-overview.md)를 참조하세요. 

**현재 감사되는 다른 Office 365 서비스는 무엇인가요?**

Exchange Online, SharePoint Online, 비즈니스용 OneDrive, Azure Active Directory, Microsoft Teams, Dynamics 365, Advanced Threat Protection 및 Power BI와 같이 가장 많이 사용되는 Office 365 서비스가 감사됩니다. 감사되는 서비스 목록은 [이 문서의 시작 부분](search-the-audit-log-in-security-and-compliance.md)을 참조하세요.

**Office 365의 감사 서비스에서 어떤 활동을 감사하나요?**

Office 365에서 감사되는 활동의 목록과 설명을 보려면 이 문서의 [감사되는 활동](#audited-activities) 섹션을 참조하세요.

**이벤트가 발생한 후 감사 레코드를 사용하는 데 시간이 얼마나 걸리나요?**

대부분의 감사 데이터는 30분 이내에 사용 가능하지만 이벤트가 발생한 후 해당 감사 로그 항목이 검색 결과에 표시되기까지 최대 24시간이 걸릴 수 있습니다. 이 문서의 [시작하기 전](#before-you-begin)에 섹션에서 다른 Office 365 서비스의 이벤트를 사용하는 데 걸리는 시간을 보여 주는 표를 참조하세요.

**감사 레코드는 얼마나 오래 보존되나요?**

앞서 설명한 것처럼 감사 레코드의 보존 기간은 조직의 Office 365 구독에 따라 다릅니다.  

- **Office 365 E3:** 감사 레코드는 90일간 보존됩니다.

- **Office 365 E5:** 감사 레코드는 90일간 보존됩니다. 결국에는 E5 사용자, E3 라이선스, Office 365 Advanced Compliance 애드온 라이선스를 보유한 사용자는 1년 동안 감사 레코드를 보유할 수 있을 것입니다.

     > [!NOTE]
     > 앞서 설명한 것처럼 E5 조직(또는 Advanced Compliance 애드온 라이선스가 있는 E3 조직)에 대한 감사 레코드의 1년 보존 기간에 대한 개인 미리보기 프로그램은 새 등록이 마감되었습니다. 이 문서는 1년 보존 기간이 공개 미리보기로 제공되거나 일반용으로 출시될 때 업데이트됩니다.

또한 감사 레코드의 보존 기간은 사용자 단위 라이선스를 기반으로 합니다. 예를 들어 조직의 사용자에게 Office 365 E3 또는 E5 라이선스가 할당된 경우 해당 사용자가 수행한 활동에 대한 감사 레코드는 90일 동안 유지됩니다.

**프로그래밍 방식으로 감사 데이터에 액세스할 수 있나요?**

예. Office 365 관리 활동 API는 프로그래밍 방식으로 감사 로그를 가져오는 데 사용됩니다.  시작하려면 [Office 365 관리 API 시작](https://docs.microsoft.com/office/office-365-management-api/get-started-with-office-365-management-apis)을 참조하세요.

**보안 및 준수 센터 또는 Office 365 관리 활동 API를 사용하는 것 외에도 다른 방법을 사용하여 감사 로그를 얻을 수 있나요?**

아니요. 이 두 가지가 Office 365 감사 서비스에서 데이터를 가져오는 유일한 방법입니다. 

**감사 로그를 캡처하려는 각 서비스에서 개별적으로 감사를 사용하도록 설정해야 하나요?**

대부분의 Office 365 서비스에서(이 문서의 [시작하기 전에](#before-you-begin) 섹션에 설명된 대로) Office 365 조직에 대한 감사를 처음 켜면 기본적으로 감사가 사용되도록 설정되어 있습니다.

**Office 365 감사 서비스에서 레코드 중복 제거를 지원하나요?**

아니요. 감사 서비스 파이프라인은 거의 실시간이므로 중복 제거를 지원할 수 없습니다.
 
**Office 365에서 지리적으로 데이터 흐름을 감사하나요?**

아니요. 현재 NA(북아메리카), EMEA(유럽, 중동, 아프리카) 및 APAC(아시아 태평양) 지역에 감사 파이프라인 배포가 있습니다. 그러나 이러한 지역에 로드 밸런싱을 위해 라이브 사이트 문제 중에만 데이터가 전달됩니다. 이러한 활동을 수행하면 전송 중인 데이터가 암호화됩니다.   
 
**감사 데이터는 암호화되어 있나요?**

감사 데이터는 감사 파이프라인이 배포된 동일한 지역의 Exchange 사서함(휴지 상태인 데이터)에 저장됩니다. 이 데이터는 암호화되지 않습니다. 그러나 전송 중인 데이터는 언제나 암호화됩니다. 
