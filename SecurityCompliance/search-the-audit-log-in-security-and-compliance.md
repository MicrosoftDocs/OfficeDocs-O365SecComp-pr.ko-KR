---
title: Office 365 보안 및 준수 센터에서 감사 로그 검색
ms.author: markjjo
author: markjjo
manager: laurawi
ms.audience: Admin
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
description: 'office 365 Security & 준수 센터를 사용 하 여 office 365 조직의 사용자 및 관리자 활동을 볼 수 있는 통합 된 감사 로그를 검색할 수 있습니다. '
ms.openlocfilehash: d9a0b009a47a00b3d7242b54b14286609ece6886
ms.sourcegitcommit: ed822a776d3419853453583e882f3c61ca26d4b2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/05/2019
ms.locfileid: "30411023"
---
# <a name="search-the-audit-log-in-the-office-365-security--compliance-center"></a>Office 365 Security & 준수 센터에서 감사 로그 검색

사용자가 특정 문서를 보거나 사서함에서 항목을 삭제 한 경우를 확인 해야 하나요? 이 경우 office 365 보안 &amp; 및 준수 센터를 사용 하 여 office 365 조직의 사용자 및 관리자 활동을 볼 수 있는 통합 된 감사 로그를 검색 하면 됩니다. 통합 감사 로그가 왜 있나요? Office 365에서 다음과 같은 유형의 사용자 및 관리자 활동을 검색할 수 있습니다.
  
- SharePoint Online 및 비즈니스용 OneDrive의 사용자 활동
    
- exchange Online의 사용자 활동 (exchange 사서함 감사 로깅)
    
    > [!IMPORTANT]
    > Exchange Online의 사용자 작업이 기록 되기 전에 각 사용자 사서함에 대해 사서함 감사 로깅을 설정 해야 합니다. 자세한 내용은 [Office 365에서 사서함 감사 사용](enable-mailbox-auditing.md)을 참조 하십시오.
  
- SharePoint Online의 관리 활동
    
- Azure Active Directory의 관리 활동 (Office 365의 디렉터리 서비스)
    
- exchange Online의 관리 활동 (exchange 관리자 감사 로깅)
    
- Sway의 사용자 및 관리자 활동
    
- Office 365 보안 & 준수 센터의 eDiscovery 활동
    
- Power BI의 사용자 및 관리 활동
    
- Microsoft 팀의 사용자 및 관리자 활동

- Dynamics 365의 사용자 및 관리자 활동
    
- Yammer의 사용자 및 관리자 활동
 
- Microsoft Flow의 사용자 및 관리자 활동
    
- Microsoft Stream의 사용자 및 관리 활동

- Microsoft 작업 공간 분석의 분석가 및 관리 활동

- PowerApps의 사용자 및 관리 활동
    
   
## <a name="before-you-begin"></a>시작하기 전에

Office 365 감사 로그 검색을 시작 하기 전에 다음 항목을 읽어 보아야 합니다.
  
- Office 365 감사 로그 검색을 시작 하기 전에 사용자 또는 다른 관리자가 먼저 감사 로깅을 켜야 합니다. 이 기능을 설정 하려면 보안 &amp; 및 준수 센터의 **감사 로그 검색** 페이지에서 **사용자 및 관리자 활동 기록을** 클릭 하면 됩니다. (이 링크가 표시 되지 않는 경우 조직에 대 한 감사가 이미 설정 된 경우) 이 기능을 켜면 감사 로그가 준비 중 이며 준비 완료 후 몇 시간 내에 검색을 실행할 수 있음을 알리는 메시지가 표시 됩니다. 이 작업은 한 번만 수행 하면 됩니다. 
    
    > [!NOTE]
    > 여기서는 기본적으로 감사를 설정 하는 프로세스를 진행 하 고 있습니다. 그때 까지는 이전에 설명한 것 처럼 켤 수 있습니다. 
  
- Office 365 감사 로그를 검색 하려면 Exchange Online에서 보기 전용 감사 로그 또는 감사 로그 역할을 할당 받아야 합니다. 기본적으로 이러한 역할은 Exchange 관리 센터의 **사용 권한** 페이지에 있는 준수 관리 및 조직 관리 역할 그룹에 할당 됩니다. 사용자에 게 최소 수준의 권한으로 Office 365 감사 로그를 검색할 수 있는 기능을 제공 하기 위해 Exchange Online에서 사용자 지정 역할 그룹을 만들고 보기 전용 감사 로그 또는 감사 로그 역할을 추가한 다음 사용자를 새 역할 그룹의 구성원으로 추가할 수 있습니다. 자세한 내용은 [Exchange Online에서 역할 그룹 관리](https://go.microsoft.com/fwlink/p/?LinkID=730688)를 참조 하세요.
    
    > [!IMPORTANT]
    > 보안 &amp; 및 준수 센터의 **사용 권한** 페이지에서 사용자에 게 보기 전용 감사 로그 또는 감사 로그 역할을 할당 하면 Office 365 감사 로그를 검색할 수 없습니다. Exchange Online에서 사용 권한을 할당 해야 합니다. 이는 감사 로그를 검색 하는 데 사용 되는 기본 cmdlet이 Exchange Online cmdlet 이기 때문입니다. 
  
- 사용자 또는 관리자가 감사 된 활동을 수행 하는 경우 감사 레코드가 생성 되 고 조직의 Office 365 감사 로그에 저장 됩니다. 감사 레코드가 보존 되는 시간 (및 감사 로그에서 검색 가능)은 Office 365 구독에 따라 다르며, 특히 특정 사용자에 게 할당 된 라이선스의 유형입니다.

     - **Office 365 E3** -감사 레코드는 90 일 동안 보존 됩니다. 즉, 최근 90 일 이내에 수행 된 작업에 대 한 감사 로그를 검색할 수 있습니다.

     - **Office 365 E5** -감사 레코드는 365 일 (1 년) 동안 보존 됩니다. 즉, 지난 해에 수행 된 활동에 대 한 감사 로그를 검색할 수 있습니다. 1 년 동안 감사 기록 보존은 E3/Exchange Online 계획 1 라이선스가 할당 되 고 Office 365 Advanced 준수 추가 기능 라이선스가 있는 사용자 에게도 제공 됩니다.

        > [!NOTE]
        > E5 조 직 (또는 고급 준수 추가 기능 라이선스가 있는 E3 조직)에 대 한 감사 레코드의 1 년 보존 기간은 현재 전용 미리 보기 프로그램의 일부로만 사용할 수 있습니다. 이 미리 보기 프로그램에 등록 하려면 [Microsoft 지원 서비스](https://docs.microsoft.com/en-us/office365/admin/contact-support-for-business-products?redirectSourcePath=%252fen-us%252farticle%252fcontact-support-for-business-products-admin-help-32a17ca7-6fa0-4870-8a8d-e25ba4ccfd4b&view=o365-worldwide&tabs=online) 에 대 한 요청을 실행 하 여 도움이 필요한 항목에 대 한 설명을 "장기적인 Office 365 audit log 비공개 preview"로 포함 하십시오.

- 조직에 대해 Office 365에서 감사 로그 검색을 해제 하려는 경우 Exchange Online 조직에 연결 된 원격 PowerShell에서 다음 명령을 실행할 수 있습니다.
    
  ```
  Set-AdminAuditLogConfig -UnifiedAuditLogIngestionEnabled $false
  ```

    감사 검색을 다시 설정 하려면 Exchange Online PowerShell에서 다음 명령을 실행 하면 됩니다.
    
  ```
  Set-AdminAuditLogConfig -UnifiedAuditLogIngestionEnabled $true
  ```

    자세한 내용은 [Office 365에서 감사 로그 검색](turn-audit-log-search-on-or-off.md)해제를 참조 하세요.
    
- 앞에서 설명한 것 처럼, 감사 로그를 검색 하는 데 사용 되는 기본 cmdlet은 Exchange Online cmdlet ( **search-unifiedauditlog)** 입니다. 즉, 보안 &amp; 및 준수 센터에서 **감사 로그 검색** 페이지를 사용 하는 대신이 cmdlet을 사용 하 여 Office 365 감사 로그를 검색할 수 있습니다. 이 cmdlet은 Exchange Online 조직에 연결 된 원격 PowerShell에서 실행 해야 합니다. 자세한 내용은 [검색-search-unifiedauditlog](https://go.microsoft.com/fwlink/p/?linkid=834776)를 참조 하세요.
    
- office 365 감사 로그에서 프로그래밍 방식으로 데이터를 다운로드 하려는 경우 PowerShell 스크립트를 사용 하는 대신 office 365 관리 작업 API를 사용 하는 것이 좋습니다. Office 365 관리 활동 API는 조직에 대 한 운영, 보안 및 규정 준수 모니터링 솔루션을 개발 하는 데 사용할 수 있는 REST 웹 서비스입니다. 자세한 내용은 [Office 365 관리 활동 API 참조](https://go.microsoft.com/fwlink/?linkid=852309)를 참조 하세요.
    
- 해당 감사 로그 항목이 검색 결과에 표시 될 때까지 이벤트가 발생 한 후 최대 30 분 이나 최대 24 시간이 걸릴 수 있습니다. 다음 표에서는 Office 365의 서로 다른 서비스에 소요 되는 시간을 보여 줍니다.
    
    |**Office 365 서비스**|**30분**|**24시간**|
    |:-----|:-----|:-----|
    |Advanced threat Protection 및 위협 인텔리전스  <br/> |![확인 표시](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)| |
    |Azure Active Directory (사용자 로그인 이벤트)  <br/> ||![확인 표시](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)           <br/> |
    |Azure Active Directory (관리 이벤트)  <br/> ||![확인 표시](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png) |
    |데이터 손실 방지  <br/> |![확인 표시](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)       <br/>| |
    |Dynamics 365 CRM <br/> |![확인 표시](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)           <br/>| |
    |eDiscovery  <br/> |![확인 표시](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)           <br/>| |
    |Exchange Online  <br/> |![확인 표시](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)           <br/> ||
    |Microsoft Flow  <br/> |![확인 표시](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)           <br/>| |
    |Microsoft Forms  <br/> |![확인 표시](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)           <br/>| |
    |Microsoft Project  <br/> |![확인 표시](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)           <br/>| |
    |Microsoft Stream  <br/> |![확인 표시](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)           <br/>| |
    |Microsoft 팀  <br/> |![확인 표시](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)           <br/> ||
    |Power BI  <br/> |![확인 표시](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)           <br/>| |
    |Security &amp; Compliance Center  <br/> |![확인 표시](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)           <br/> ||
    |SharePoint Online 및 비즈니스용 OneDrive  <br/> |![확인 표시](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)           <br/> ||
    |Sway  <br/> ||![확인 표시](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)           <br/> |
    |Workplace Analytics<br/> |![확인 표시](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)           <br/> || 
    |Yammer  <br/> ||![확인 표시](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)           <br/> |
   
- azure Active directory (azure AD)는 Office 365의 디렉터리 서비스입니다. 통합 된 감사 로그에는 Office 365 관리 센터 또는 Azure 관리 포털에서 수행 되는 사용자, 그룹, 응용 프로그램, 도메인 및 디렉터리 작업이 포함 되어 있습니다. azure AD 이벤트의 전체 목록은 [azure Active Directory 감사 보고서 이벤트](https://go.microsoft.com/fwlink/p/?LinkID=616549)를 참조 하세요.
    
- exchange Online 감사 로그는 exchange 관리 이벤트 (관리자가 수행한 작업)와 사서함 이벤트 (사서함 사용자가 수행한 작업)의 두 가지 이벤트 유형으로 구성 됩니다. 사서함 감사는 기본적으로 사용 하지 않도록 설정 되어 있습니다. Office 365 감사 로그에서 사서함 이벤트를 검색 하려면 각 사용자 사서함에 대해이 기능을 사용 하도록 설정 해야 합니다. 기록 되는 사서함 감사 및 사서함 감사 작업에 대 한 자세한 내용은 [Office 365에서 사서함 감사 사용](enable-mailbox-auditing.md)을 참조 하십시오.
    
- Power BI에 대 한 감사 로깅은 기본적으로 사용 하지 않도록 설정 되어 있습니다. Office 365 감사 로그에서 power bi 활동을 검색 하려면 power bi 관리 포털에서 감사를 사용 하도록 설정 해야 합니다. 자세한 내용은 [Power BI 관리 포털](https://docs.microsoft.com/power-bi/service-admin-portal#audit-logs)의 "감사 로그" 섹션을 참조 하십시오.
    
    
## <a name="search-the-audit-log"></a>감사 로그 검색

Office 365에서 감사 로그를 검색 하는 프로세스는 다음과 같습니다.
  
[1 단계: 감사 로그 검색 실행](#step-1-run-an-audit-log-search)
  
[2 단계: 검색 결과 보기](#step-2-view-the-search-results)

[3 단계: 검색 결과 필터링](#step-3-filter-the-search-results)

[4 단계: 검색 결과를 파일로 내보내기](#step-4-export-the-search-results-to-a-file)
  
### <a name="step-1-run-an-audit-log-search"></a>1 단계: 감사 로그 검색 실행

1. [https://protection.office.com](https://protection.office.com)으로 이동합니다.
    
    > [!TIP]
    > Office 365 보안 &amp; 및 준수 센터에 액세스 하려면 개인 검색 세션 (일반 세션이 아님)을 사용 하 여 현재 로그온 한 자격 증명이 사용 되지 않도록 합니다. Internet Explorer 또는 Microsoft Edge에서 InPrivate 브라우징 세션을 열려면 CTRL + SHIFT + P를 누르기만 하면 됩니다. Google Chrome (incognito 창 이라고 함)에서 개인 검색 세션을 열려면 CTRL + SHIFT + N을 누릅니다. 
  
2. 회사 또는 학교 계정을 사용하여 Office 365에 로그인합니다.
    
3. 보안 &amp; 및 준수 센터의 왼쪽 창에서 **검색 &amp; 조사**를 클릭 하 고 **감사 로그 검색**을 클릭 합니다.
    
    **감사 로그 검색** 페이지가 표시 됩니다. 
    
    ![조건을 구성 하 고 검색을 클릭 하 여 보고서를 실행 합니다.](media/8639d09c-2843-44e4-8b4b-9f45974ff7f1.png)
  
    > [!NOTE]
    > 감사 로그 검색을 실행 하려면 먼저 감사 로깅을 켜야 합니다. **사용자 및 관리 활동 기록 시작** 링크가 표시 되 면 해당 링크를 클릭 하 여 감사를 설정 합니다. 이 링크가 표시 되지 않으면 조직에서 감사가 이미 설정 된 것입니다. 
  
4. 다음 검색 조건을 구성 합니다.
    
    위한. **활동** 드롭다운 목록을 클릭 하 여 검색할 수 있는 활동을 표시 합니다. 사용자 및 관리 활동은 관련 활동 그룹으로 구성 됩니다. 특정 활동을 선택 하거나 활동 그룹 이름을 클릭 하 여 그룹의 모든 활동을 선택할 수 있습니다. 선택한 활동을 클릭 하 여 선택을 취소할 수도 있습니다. 검색을 실행 한 후에는 선택한 작업에 대 한 감사 로그 항목만 표시 됩니다. **모든 작업에 대해 결과 표시** 를 선택 하면 선택한 사용자 또는 사용자 그룹에 의해 수행 된 모든 작업에 대 한 결과가 표시 됩니다. 
    
    100 Over 사용자 및 관리 활동이 Office 365 감사 로그에 기록 됩니다. 이 문서의 항목에서 **감사 된 작업** 탭을 클릭 하면 각 Office 365 서비스의 모든 활동에 대 한 설명을 볼 수 있습니다. 
    
    b. **시작 날짜** 및 **끝 날짜** 지난 7 일간이 기본적으로 선택 됩니다. 날짜 및 시간 범위를 선택 하 여 해당 기간 내에 발생 한 이벤트를 표시 합니다. 날짜와 시간은 utc (협정 세계시) 형식으로 표시 됩니다. 지정할 수 있는 최대 날짜 범위는 90 일입니다. 선택한 날짜 범위가 90 일 보다 크면 오류가 표시 됩니다. 
    
    > [!TIP]
    > 최대 날짜 범위 90 일을 사용 하는 경우 **시작 날짜**의 현재 시간을 선택 합니다. 그렇지 않으면 시작 날짜가 종료 날짜 보다 이전 이라는 오류가 표시 됩니다. 최근 90 일 이내에 감사를 설정한 경우에는 감사가 설정 된 날짜 이전에 최대 날짜 범위를 시작할 수 없습니다. 
  
    &. **사용자** 이 상자를 클릭 하 고 검색 결과를 표시할 사용자를 한 명 이상 선택 합니다. 이 상자에서 선택한 사용자가 수행한 선택한 작업에 대 한 감사 로그 항목이 결과 목록에 표시 됩니다. 조직의 모든 사용자 및 서비스 계정에 대 한 항목을 반환 하려면이 상자를 비워 둡니다. 
    
    &. **파일, 폴더 또는 사이트** 지정한 키워드를 포함 하는 폴더의 파일에 관련 된 작업을 검색 하려면 파일 또는 폴더 이름을 일부 또는 모두 입력 합니다. 파일 또는 폴더의 URL을 지정할 수도 있습니다. url을 사용 하는 경우에는 전체 url 경로를 입력 하거나 url의 일부만 입력 해야 하며 특수 문자나 공백은 포함 하지 않습니다. 
    
    조직의 모든 파일 및 폴더에 대 한 항목을 반환 하려면이 상자를 비워 둡니다.
    
    > [!TIP]
    > **사이트**와 관련 된 모든 활동을 찾으려는 경우 URL 뒤에 와일드 카드 기호 (\*)를 추가 하 여 해당 사이트에 대 한 모든 항목을 반환 합니다. 예를 들면 **"https://contoso-my.sharepoint.com/personal/*"** 입니다.
    
5. 검색 **** 을 클릭 하 여 검색 조건을 사용 하 여 검색을 실행 합니다. 
    
    검색 결과가 로드 되 고 몇 분 후에 **결과**아래에 표시 됩니다. 검색이 완료 되 면 검색 된 결과 수가 표시 됩니다. 최대 5000 개의 이벤트가 **결과** 창에 150 이벤트로 증가 하 여 표시 됩니다. 5000 개 보다 많은 이벤트가 검색 조건을 충족 하는 경우 가장 최근 5000 이벤트가 표시 됩니다. 
    
    ![검색이 완료 된 후 결과 수가 표시 됩니다.](media/986216f1-ca2f-4747-9480-e232b5bf094c.png)
  
  
#### <a name="tips-for-searching-the-audit-log"></a>감사 로그 검색 팁

- 활동 이름을 클릭 하 여 검색할 특정 활동을 선택할 수 있습니다. 또는 그룹 이름을 클릭 하 여 그룹의 모든 활동 (예: **파일 및 폴더 활동**)을 검색할 수 있습니다. 활동을 선택한 경우이를 클릭 하 여 선택 내용을 취소할 수 있습니다. 또한 검색 상자를 사용 하 여 입력 하는 키워드가 포함 된 활동을 표시할 수도 있습니다.
    
    ![활동 그룹 이름을 클릭 하 여 모든 활동을 선택 합니다.](media/3cde97cb-6f35-47c0-8612-ecd9c6ac36a3.png)
  
- Exchange 관리자 감사 로그의 이벤트를 표시 하려면 **작업** 목록에서 **모든 작업에 대 한 결과 표시** 를 선택 해야 합니다. 이 감사 로그의 이벤트는 결과의 **활동** 열에 cmdlet 이름 (예: **설정 사서함** )을 표시 합니다. 자세한 내용을 보려면이 항목에서 **감사 된 작업** 탭을 클릭 한 다음 **Exchange 관리 활동**을 클릭 합니다.
    
    마찬가지로, **활동** 목록에 해당 항목이 없는 몇 가지 감사 작업도 있습니다. 이러한 활동에 대 한 작업의 이름을 알고 있는 경우에는 모든 활동을 검색 한 다음 **활동** 열에 대 한 상자에 작업 이름을 입력 하 여 결과를 필터링 할 수 있습니다. 결과를 필터링 하는 방법에 대 한 자세한 내용은 [3 단계: 검색 결과 필터링](#step-3-filter-the-search-results) 을 참조 하십시오. 
    
- **지우기를** 클릭 하 여 현재 검색 조건을 지웁니다. 날짜 범위가 지난 7 일간의 기본값으로 돌아옵니다. 모두 지우기를 클릭 하 여 **모든 활동에 대 한 결과를 표시** 하 여 선택한 모든 활동을 취소할 수도 있습니다. 
    
- 5000 결과가 발견 되 면 검색 조건을 충족 하는 이벤트가 5000 개 보다 많은 것으로 간주할 수 있습니다. 검색 조건을 구체화 하 고 검색을 다시 실행 하 여 더 많은 결과를 반환 하거나, **** \> **모든 결과 다운로드**를 선택 하 여 모든 검색 결과를 내보낼 수 있습니다.

  
### <a name="step-2-view-the-search-results"></a>2 단계: 검색 결과 보기

감사 로그 검색 페이지의 **결과** 아래 표시 됩니다. **** 앞에서 설명한 것 처럼 최대 5000 (최신) 이벤트는 150 이벤트 단위로 표시 됩니다. 더 많은 이벤트를 표시 하려면 **결과** 창에서 스크롤 막대를 사용 하거나 **Shift + End** 를 눌러 다음 150 이벤트를 표시할 수 있습니다. 
  
결과에는 검색에서 반환 된 각 이벤트에 대 한 다음과 같은 정보가 포함 됩니다.
  
- **날짜:** 이벤트가 발생 한 날짜 및 시간 (UTC 형식)입니다. 
    
- **IP 주소:** 활동을 로그할 때 사용 된 장치의 IP 주소입니다. IP 주소는 IPv4 또는 IPv6 주소 형식으로 표시 됩니다. 
    
- **사용자:** 이벤트를 트리거한 작업을 수행한 사용자 또는 서비스 계정입니다. 
    
- **활동:** 사용자가 수행 하는 작업입니다. 이 값은 **활동** 드롭다운 목록에서 선택한 활동에 해당 합니다. exchange 관리자 감사 로그의 이벤트에 대해이 열의 값은 exchange cmdlet입니다. 
    
- **항목:** 해당 활동의 결과로 만들어지거나 수정 된 개체입니다. 예를 들어, 보거나 수정한 파일 또는 업데이트 된 사용자 계정입니다. 모든 활동에이 열에 대 한 값이 있는 것은 아닙니다. 
    
- **자세한 정보:** 활동에 대 한 추가 정보입니다. 다시 말하지만 모든 작업에는 값이 포함 되지 않습니다. 
    
> [!TIP]
> 결과를 정렬 하려면 **results** 에서 열 머리글을 클릭 합니다. 결과를 a에서 z 또는 z에서 a로 정렬할 수 있습니다. **날짜** 머리글을 클릭 하 여 결과를 오름차순에서 최신으로 또는 가장 오래 된 항목 순으로 정렬 합니다. 
  
#### <a name="view-the-details-for-a-specific-event"></a>특정 이벤트에 대 한 세부 정보 보기

검색 결과 목록에서 이벤트 레코드를 클릭 하 여 이벤트에 대 한 자세한 정보를 볼 수 있습니다. 이벤트 레코드의 자세한 속성을 포함 하는 **세부 정보** 페이지가 표시 됩니다. 표시 되는 속성은 이벤트가 발생 하는 Office 365 서비스에 따라 달라 집니다. 이러한 세부 정보를 표시 하려면 **추가 정보**를 클릭 합니다. [자세한 내용은 Office 365 감사 로그의 자세한 속성](detailed-properties-in-the-office-365-audit-log.md)을 참조 하십시오.
  
![감사 로그 이벤트 레코드의 자세한 속성을 보려면 추가 정보를 클릭 합니다.](media/6df582ae-d339-4735-b1a6-80914fb77a08.png)

  
### <a name="step-3-filter-the-search-results"></a>3 단계: 검색 결과 필터링

정렬 외에도 감사 로그 검색의 결과를 필터링 할 수도 있습니다. 이 기능은 특정 사용자 또는 활동에 대 한 결과를 빠르게 필터링 하는 데 도움이 되는 유용한 기능입니다. 처음에는 다양 한 검색을 만든 다음 결과를 빠르게 필터링 하 여 특정 이벤트를 볼 수 있습니다. 그런 다음 검색 조건을 좁혀 검색을 다시 실행 하 여 더 작은 보다 간단한 결과 집합을 반환할 수 있습니다.
  
결과를 필터링 하려면
  
1. 감사 로그 검색을 실행 합니다.
    
2. 결과가 표시 되 면 **필터 결과**를 클릭 합니다.
    
    각 열 머리글 아래에 키워드 상자가 표시 됩니다.
    
3. 필터링 하는 열에 따라 열 머리글 아래의 상자 중 하나를 클릭 하 고 단어 또는 구를 입력 합니다. 결과가 동적으로 readjust 필터와 일치 하는 이벤트가 표시 됩니다.
    
    ![필터에 단어를 입력 하 여 필터와 일치 하는 이벤트 표시](media/542dc323-a997-402c-934b-cc5e218e50bc.png)
  
4. 필터를 지우려면 필터 상자에서 **X** 를 클릭 하거나 **필터링 숨기기**를 클릭 하면 됩니다.
    
> [!TIP]
> Exchange 관리자 감사 로그의 이벤트를 표시 하려면 **활동** 필터 상자 **-** 에 대시 (-)를 입력 합니다. 이렇게 하면 Exchange 관리 이벤트에 대 한 **활동** 열에 표시 되는 cmdlet 이름이 표시 됩니다. 그런 다음 cmdlet 이름을 알파벳 순으로 정렬할 수 있습니다. 

### <a name="step-4-export-the-search-results-to-a-file"></a>4 단계: 검색 결과를 파일로 내보내기

감사 로그 검색 결과를 로컬 컴퓨터의 CSV (쉼표로 구분 된 값) 파일로 내보낼 수 있습니다. Microsoft Excel에서이 파일을 열고, 검색, 정렬, 필터링, 다중 값 셀이 포함 된 단일 열을 여러 열로 분할 등의 기능을 사용할 수 있습니다.
  
1. 감사 로그 검색을 실행 한 다음 원하는 결과가 나올 때까지 검색 조건을 수정 합니다.
    
2. **결과 내보내기를** 클릭 하 고 다음 옵션 중 하나를 선택 합니다. 
    
  - **로드 된 결과 저장** * * 감사 로그 검색 * * 페이지의 **결과** 에 표시 되는 항목만 내보내려면이 옵션을 선택 합니다. 다운로드 되는 CSV 파일에는 페이지 (날짜, 사용자, 작업, 항목 및 세부 정보)에 표시 되는 것과 동일한 열 (및 데이터)이 포함 되어 있습니다. 감사 로그 항목에서 더 **** 많은 정보를 포함 하는 추가 열 (추가)이 CSV 파일에 포함 됩니다. **감사 로그 검색** 페이지에서 로드 되 고 볼 수 있는 것과 동일한 결과를 내보내기 때문에 최대 5000 개의 항목을 내보냅니다. 
    
  - **모든 결과 다운로드** 검색 조건을 충족 하는 Office 365 감사 로그의 모든 항목을 내보내려면이 옵션을 선택 합니다. 다양 한 검색 결과 집합의 경우 감사 로그 **검색** 페이지에 표시할 수 있는 5000 결과 외에도 모든 항목을 audit log에서 다운로드 하려면이 옵션을 선택 합니다. 이 옵션은 감사 로그의 원시 데이터를 CSV 파일로 다운로드 하 고 감사 로그 항목에서 **auditdata**라는 열에 대 한 추가 정보를 포함 합니다. 다른 옵션을 선택 하는 경우이 내보내기 옵션을 선택 하면 다운로드 한 파일 보다 훨씬 커질 수 있으므로 파일을 다운로드 하는 데 시간이 오래 걸릴 수도 있습니다.
    
    > [!IMPORTANT]
    > 단일 감사 로그 검색에서 최대 5만 개의 항목을 CSV 파일에 다운로드할 수 있습니다. 5만 항목이 CSV 파일에 다운로드 되는 경우 검색 조건을 충족 하는 이벤트가 5만 개 보다 많은 것으로 간주할 수 있습니다. 이 제한 보다 많은 시간을 내보내려면 날짜 범위를 사용 하 여 감사 로그 항목 수를 줄이십시오. 5만 개 보다 많은 항목을 내보내려면 날짜 범위가 더 작은 검색을 여러 개 실행 해야 할 수 있습니다. 
  
3. 내보내기 옵션을 선택한 후에는 CSV 파일을 열도록 요청 하는 메시지가 창 아래쪽에 표시 되며 다운로드 폴더에 저장 하거나 특정 폴더에 저장 합니다.

  
#### <a name="more-information-about-exporting-audit-log-search-results"></a>감사 로그 검색 결과 내보내기에 대 한 자세한 정보

- **모든 결과 다운로드** 옵션은 Office 365 감사 로그의 원시 데이터를 CSV 파일로 다운로드 합니다. 이 파일에는 **로드 된 결과 저장** 옵션을 선택한 경우에 다운로드 되는 파일의 열 이름 (CreationDate, UserIds, 작업, auditdata)이 서로 다릅니다. 동일한 활동에 대해 서로 다른 두 개의 CSV 파일 값이 다를 수도 있습니다. 예를 들어 CSV 파일의 **작업** 열에 있는 작업 및 **감사 로그 검색** 페이지의 **활동** 열에 표시 되는 "사용자에 게 친숙 한" 버전과는 다른 값을 사용할 수 있습니다. 예를 들어 사서함에 로그인 한 MailboxLogin 및 사용자입니다.
    
- 모든 결과를 다운로드 하는 경우 CSV 파일에는 각 이벤트에 대 한 추가 정보를 포함 하는 **auditdata**라는 열이 포함 됩니다. 앞에서 설명한 것 처럼이 열에는 감사 로그 레코드의 여러 속성에 대 한 다중 값 속성이 포함 되어 있습니다. 이 다중 값 속성의 각 **속성: 값** 쌍은 쉼표로 구분 됩니다. Excel에서 파워 쿼리를 사용 하 여이 열을 여러 열로 분할 하 여 각 속성에 자체 열을 표시할 수 있습니다. 이렇게 하면 이러한 속성 중 하나 이상을 정렬 및 필터링 할 수 있습니다. 이 작업을 수행 하는 방법에 대 한 자세한 내용은 [split a text 열 (Power Query)](https://support.office.com/article/5282d425-6dd0-46ca-95bf-8e0da9539662)에서 "구분 기호로 열 분할" 섹션을 참조 하십시오.
    
    **auditdata** 열을 분할 한 후에는 **작업** 열에서 필터링 하 여 특정 활동 유형의 세부 속성을 표시할 수 있습니다. 
    
- 감사 레코드의 **auditdata** 필드에 표시 되는 데이터에 대 한 3060 자 제한이 있습니다. 3060 문자 제한이 초과 되는 경우이 필드의 데이터는 잘립니다. 
    
- 다른 Office 365 서비스의 이벤트가 포함 된 검색 쿼리의 결과를 모두 다운로드 하면 CSV 파일의 **auditdata** 열에는 작업을 수행 하는 서비스에 따라 다양 한 속성이 포함 됩니다. 예를 들어 Exchange 및 Azure AD 감사 로그의 항목에는 action이 정상적으로 작동 했는지 여부를 나타내는 **resultstatus** 라는 속성이 포함 되어 있습니다. 이 속성은 SharePoint의 이벤트에는 포함 되지 않습니다. 마찬가지로 SharePoint 이벤트에는 파일 및 폴더 관련 작업의 사이트 URL을 식별 하는 속성이 있습니다. 이 동작을 완화 하려면 다른 검색을 사용 하 여 단일 서비스에서 활동에 대 한 결과를 내보냅니다. 
    
    모든 결과를 다운로드할 때 CSV 파일의 **auditdata** 열에 나열 되는 속성에 대 한 설명과 각 항목에 적용 되는 서비스에 대 한 [자세한 내용은 Office 365 감사 로그의 자세한 속성](detailed-properties-in-the-office-365-audit-log.md)을 참조 하십시오.

## <a name="audited-activities"></a>감사 작업

이 섹션의 표에서는 Office 365에서 감사 되는 작업에 대해 설명 합니다. 보안 & 준수 센터에서 감사 로그를 검색 하 여 이러한 이벤트를 검색할 수 있습니다.
  
이러한 표에는 특정 Office 365 서비스의 관련 활동 또는 활동이 그룹화 되어 있습니다. 이 테이블에는 **작업** 드롭다운 목록에 표시 되는 이름과 검색 결과를 내보낼 때 감사 레코드 및 CSV 파일의 자세한 정보에 표시 되는 해당 작업의 이름이 포함 되어 있습니다. 자세한 정보에 대 한 설명은 [Office 365 감사 로그의 자세한 속성](detailed-properties-in-the-office-365-audit-log.md)을 참조 하십시오.
  
다음 링크 중 하나를 클릭 하 여 특정 테이블로 이동 합니다.
  
||||
|:-----|:-----|:-----|
|[파일 및 페이지 활동](#file-and-page-activities)<br/> |[폴더 활동](#folder-activities)<br/> |[공유 및 액세스 요청 활동](#sharing-and-access-request-activities)<br/> |
|[동기화 작업](#synchronization-activities)<br/> |[사이트 관리 작업](#site-administration-activities)<br/> |[Exchange 사서함 활동](#exchange-mailbox-activities)<br/> |
|[보존 정책 및 레이블 활동](#retention-policy-and-label-activities) <br/>|[Sway 활동](#sway-activities) <br/> |[사용자 관리 활동](#user-administration-activities) <br/> 
|[Azure AD 그룹 관리 작업](#azure-ad-group-administration-activities) <br/> |[응용 프로그램 관리 작업](#application-administration-activities) <br/> |[역할 관리 작업](#role-administration-activities) <br/> |
|[디렉터리 관리 작업](#directory-administration-activities) <br/> |[eDiscovery 활동](#ediscovery-activities) <br/> |[Power BI 활동](#power-bi-activities) <br/> |
|[Microsoft 작업 공간 분석](#microsoft-workplace-analytics-activities)<br/>|[Microsoft 팀원 활동](#microsoft-teams-activities) <br/> |[Yammer 활동](#yammer-activities) <br/> |
[Microsoft Flow](#microsoft-flow) <br/> |[Microsoft PowerApps](#microsoft-powerapps)<br/>|[Microsoft Stream](#microsoft-stream) <br/>|
|[Exchange 관리 활동](#exchange-admin-audit-log)<br/>
||||
   
  
### <a name="file-and-page-activities"></a>파일 및 페이지 활동
  
다음 표에서는 SharePoint Online 및 비즈니스용 OneDrive의 파일 및 페이지 활동에 대해 설명 합니다.
  
|**식별 이름**|**Operation**|**설명**|
|:-----|:-----|:-----|
|액세스 한 파일  <br/> |액세스 한 파일  <br/> |사용자 또는 시스템 계정이 파일에 액세스합니다.  <br/> |
|none  <br/> |FileAccessedExtended  <br/> |이는 "액세스 한 파일" (fileaccessed) 작업과 관련이 있습니다. FileAccessedExtended 이벤트는 동일한 사용자가 계속 해 서 오랜 시간 동안 파일에 액세스할 때 기록 됩니다 (최대 3 시간). FileAccessedExtended 이벤트를 로깅하는 목적은 파일에 계속 액세스 하는 경우 기록 되는 fileaccessed 한 이벤트의 수를 줄이기 위한 것입니다. 이렇게 하면 기본적으로 동일한 사용자 작업에 대 한 여러 fileaccessed 한 레코드의 노이즈를 줄일 수 있으며, 초기 (및 보다 중요 한)에 액세스 한 이벤트에 초점을 둘 있습니다.  <br/> |
|체크 인 된 파일  <br/> |FileCheckedIn  <br/> |사용자가 문서 라이브러리에서 체크 아웃 한 문서를 체크 인 합니다.  <br/> |
|체크 아웃 된 파일  <br/> |FileCheckedOut  <br/> |사용자가 문서 라이브러리에 있는 문서를 체크 아웃 합니다. 사용자는 공유 된 문서를 체크 아웃 하 고 변경할 수 있습니다.  <br/> |
|복사 되는 파일  <br/> |FileCopied  <br/> |사용자가 사이트에서 문서를 복사 합니다. 복사된 파일은 사이트의 다른 폴더에 저장할 수 있습니다.  <br/> |
|삭제 된 파일  <br/> |filedeleted  <br/> |사용자가 사이트에서 문서를 삭제 합니다.  <br/> |
|휴지통에서 삭제 된 파일  <br/> |FileDeletedFirstStageRecycleBin  <br/> |사용자가 사이트의 휴지통에서 파일을 삭제 합니다.  <br/> |
|2 단계 휴지통에서 삭제 된 파일  <br/> |FileDeletedSecondStageRecycleBin  <br/> |사용자가 사이트의 2 단계 휴지통에서 파일을 삭제 합니다.  <br/> |
|파일에서 맬웨어가 검색 되었습니다.  <br/> |FileMalwareDetected  <br/> |SharePoint 바이러스 백신 엔진이 파일에서 맬웨어를 감지 합니다.  <br/> |
|삭제 한 파일 체크 아웃  <br/> |FileCheckOutDiscarded  <br/> |사용자가 체크 아웃된 파일을 삭제(또는 실행 취소)합니다. 즉, 체크 아웃한 파일의 변경 내용은 취소되고, 문서 라이브러리에 있는 문서 버전에 저장되지 않습니다.  <br/> |
|다운로드 한 파일  <br/> |파일 다운로드 됨  <br/> |사용자가 사이트에서 문서를 다운로드 합니다.  <br/> |
|수정 된 파일  <br/> |FileModified  <br/> |사용자 또는 시스템 계정이 사이트에 있는 문서의 내용이 나 속성을 수정 합니다.  <br/> |
|none  <br/> |FileModifiedExtended  <br/> |이는 "수정 된 파일" (FileModified) 작업과 관련이 있습니다. FileModifiedExtended 이벤트는 동일한 사용자가 계속 해 서 오랜 시간 동안 파일을 수정할 때 기록 됩니다 (최대 3 시간). FileModifiedExtended 이벤트를 로깅하는 목적은 파일을 계속 수정할 때 기록 되는 FileModified 이벤트의 수를 줄이는 것입니다. 이렇게 하면 기본적으로 동일한 사용자 활동에 대 한 여러 FileModified 레코드의 노이즈가 줄어들지만 초기 (및 더 중요 한) FileModified 이벤트에 집중할 수 있습니다.  <br/> |
|이동 된 파일  <br/> |FileMoved  <br/> |사용자가 사이트의 현재 위치에서 새 위치로 문서를 이동 합니다.  <br/> |
|파일의 모든 부 버전 재생  <br/> |FileVersionsAllMinorsRecycled  <br/> |사용자가 파일의 버전 기록에서 모든 부 버전을 삭제 합니다. 삭제 된 버전은 사이트의 휴지통으로 이동 됩니다.  <br/> |
|모든 파일 버전 재생  <br/> |FileVersionsAllRecycled  <br/> |사용자가 파일의 버전 기록에서 모든 버전을 삭제 합니다. 삭제 된 버전은 사이트의 휴지통으로 이동 됩니다.  <br/> |
|파일의 재활용 버전  <br/> |fileversionrecycled  <br/> |사용자가 파일의 버전 기록에서 버전을 삭제 합니다. 삭제 된 버전은 사이트의 휴지통으로 이동 됩니다.  <br/> |
|이름이 바뀐 파일  <br/> |FileRenamed  <br/> |사용자가 사이트에서 문서의 이름을 바꿉니다.  <br/> |
|복원 된 파일  <br/> |FileRestored  <br/> |사용자가 사이트의 휴지통에서 문서를 복원 합니다.  <br/> |
|업로드 된 파일  <br/> |fileuploaded 됨  <br/> |사용자가 사이트의 폴더에 문서를 업로드 합니다.  <br/> |
|본 페이지  <br/> |pageviewed  <br/> |사용자가 사이트의 페이지를 볼 수 있습니다. 여기에는 웹 브라우저를 사용 하 여 문서 라이브러리에 있는 파일을 보는 것이 포함 되지 않습니다.  <br/> |
|none  <br/> |PageViewedExtended  <br/> |이 작업은 "본 페이지" (pageviewed) 작업과 관련이 있습니다. PageViewedExtended 이벤트는 같은 사용자가 계속 해 서 오랜 시간 동안 웹 페이지를 볼 때 기록 됩니다 (최대 3 시간). PageViewedExtended 이벤트를 로깅하는 목적은 페이지를 계속 볼 때 기록 되는 페이지로 표시 되는 이벤트의 수를 줄이기 위한 것입니다. 이렇게 하면 기본적으로 동일한 사용자 활동에 대 한 여러 pageviewed 레코드의 노이즈를 줄일 수 있으며, 초기 (및 더 중요 한) pageviewed 이벤트에 집중할 수 있습니다.  <br/> |
||||
  
### <a name="folder-activities"></a>폴더 활동
  
다음 표에는 SharePoint Online의 폴더 활동 및 비즈니스용 OneDrive에 대 한 설명이 나와 있습니다.
  
|**식별 이름**|**Operation**|**설명**|
|:-----|:-----|:-----|
|복사 되는 폴더  <br/> |foldercopied  <br/> |사용자가 사이트에서 SharePoint 또는 비즈니스용 OneDrive의 다른 위치로 폴더를 복사 합니다.  <br/> |
|만든 폴더  <br/> |foldercreated  <br/> |사용자가 사이트에 폴더를 만듭니다.  <br/> |
|삭제 된 폴더  <br/> |folderdeleted  <br/> |사용자가 사이트에서 폴더를 삭제 합니다.  <br/> |
|휴지통에서 삭제 된 폴더  <br/> |FolderDeletedFirstStageRecycleBin  <br/> |사용자가 사이트의 휴지통에서 폴더를 삭제 합니다.  <br/> |
|2 단계 휴지통에서 삭제 된 폴더  <br/> |FolderDeletedSecondStageRecycleBin  <br/> |사용자가 사이트의 2 단계 휴지통에서 폴더를 삭제 합니다.  <br/> |
|수정 된 폴더  <br/> |foldermodified  <br/> |사용자가 사이트의 폴더를 수정 합니다. 여기에는 태그 및 속성 변경과 같은 폴더 메타 데이터 변경이 포함 됩니다.  <br/> |
|이동한 폴더  <br/> |foldermoved  <br/> |사용자가 사이트의 다른 위치로 폴더를 이동 합니다.  <br/> |
|이름이 바뀐 폴더  <br/> |FolderRenamed  <br/> |사용자가 사이트에서 폴더 이름을 바꿉니다.  <br/> |
|복원 된 폴더  <br/> |folderrestored  <br/> |사용자가 사이트의 휴지통에서 삭제 된 폴더를 복원 합니다.  <br/> |
||||
  
### <a name="sharing-and-access-request-activities"></a>공유 및 액세스 요청 활동
  
다음 표에서는 SharePoint Online 및 비즈니스용 OneDrive의 사용자 공유 및 액세스 요청 작업에 대해 설명 합니다. 공유 이벤트의 경우 **결과** 아래의 **세부 정보** 열에는 해당 항목이 공유 된 사용자 또는 그룹의 이름과 해당 사용자 또는 그룹이 조직의 구성원 또는 게스트 인지 여부가 식별 됩니다. 자세한 내용은 [Office 365 감사 로그에서 공유 감사 사용](use-sharing-auditing.md)을 참조 하십시오.
  
> [!NOTE]
> 사용자 개체의 UserType 속성을 기반으로 하는 *구성원이* 나 *게스트가* 될 수 있습니다. 구성원은 일반적으로 직원 이며, 게스트는 대개 조직 외부의 협력자입니다. 사용자가 공유 초대를 수락 하 고 (아직 조직의 일부가 아닌 경우) 조직의 디렉터리에서 게스트 계정을 만듭니다. 게스트 사용자의 디렉터리에 계정이 있으면 리소스를 초대 없이 직접 공유할 수 있습니다. 
  
|**식별 이름**|**Operation**|**설명**|
|:-----|:-----|:-----|
|수락 된 액세스 요청  <br/> |accessrequestaccepted 됨  <br/> |사이트, 폴더 또는 문서에 대 한 액세스 요청이 수락 되었으며 요청 하는 사용자에 게 액세스 권한이 부여 되었습니다.  <br/> |
|수락 된 공유 초대  <br/> |SharingInvitationAccepted  <br/> |사용자 (구성원 또는 게스트)가 공유 초대를 수락 했으며 리소스에 대 한 액세스 권한을 부여 받았습니다. 이 이벤트에는 초대 된 사용자에 대 한 정보와 초대를 수락 하는 데 사용 된 전자 메일 주소가 포함 됩니다 (다른 것은 해당 됨). 이 작업은 대개 사용자에 게 리소스에 대 한 액세스 권한을 부여 받은 방법, 즉 리소스에 액세스할 수 있는 그룹에 사용자를 추가 하는 방법을 설명 하는 두 번째 이벤트가 수반 됩니다.  <br/> |
|사이트 모음에 대 한 권한 수준을 추가 했습니다.  <br/> |강화 level추가 됨  <br/> |사용 권한 수준이 사이트 모음에 추가 되었습니다.  <br/> |
|보안 링크에 사용자 추가  <br/> |ad이상 tosecurelink  <br/> |이 보안 공유 링크를 사용할 수 있는 엔터티 목록에 사용자가 추가 되었습니다.  <br/> |
|차단 된 공유 초대  <br/> |SharingInvitationBlocked  <br/> | 조직의 사용자가 보낸 공유 초대는 대상 사용자의 도메인에 따라 외부 공유를 허용 하거나 거부 하는 외부 공유 정책으로 인해 차단 됩니다. 이 경우에는 다음과 같은 이유로 공유 초대가 차단 되었습니다.  <br/>  대상 사용자의 도메인은 허용 된 도메인 목록에 포함 되지 않습니다.  <br/>  또는  <br/>  대상 사용자의 도메인이 차단 된 도메인 목록에 포함 됩니다.  <br/>  도메인을 기반으로 외부 공유를 허용 하거나 차단 하는 방법에 대 한 자세한 내용은 [SharePoint Online의 제한 된 도메인 공유 및 비즈니스용 OneDrive](https://support.office.com/article/5d7589cd-0997-4a00-a2ba-2320ec49c4e9)를 참조 하세요.  <br/> |
|중단 권한 수준 상속  <br/> |PermissionLevelsInheritanceBroken  <br/> |부모 로부터 더 이상 사용 권한 수준을 상속 하지 않도록 항목을 변경 했습니다.  <br/> |
|공유 상속 중단  <br/> |SharingInheritanceBroken  <br/> |상위 항목에서 더 이상 공유 사용 권한을 상속 하지 않도록 항목이 변경 되었습니다.  <br/> |
|회사 공유 가능 링크를 만들었습니다.  <br/> |CompanyLinkCreated  <br/> |사용자가 자원에 대 한 회사 차원 링크를 만들었습니다. 회사 전체의 링크는 조직의 구성원만 사용할 수 있습니다. 게스트에는 사용할 수 없습니다.  <br/> |
|만든 액세스 요청  <br/> |accessrequestcreated  <br/> |사용자가 액세스할 수 있는 권한이 없는 사이트, 폴더 또는 문서에 대 한 액세스를 요청 합니다.  <br/> |
|익명 링크를 만들었습니다.  <br/> |AnonymousLinkCreated  <br/> |사용자가 리소스에 대 한 익명 링크를 만들었습니다. 이 링크를 사용 하는 모든 사용자는 인증 없이 리소스에 액세스할 수 있습니다.  <br/> |
|만든 보안 링크  <br/> |securelinkcreated  <br/> |이 항목에 대 한 보안 공유 링크를 만들었습니다.  <br/> |
|만든 공유 초대  <br/> |SharingInvitationCreated  <br/> |사용자가 조직의 디렉터리에 없는 사용자를 사용 하 여 SharePoint Online 또는 비즈니스용 OneDrive의 리소스를 공유 했습니다.  <br/> |
|삭제 된 보안 링크  <br/> |securelinkdeleted  <br/> |보안 공유 링크가 삭제 되었습니다.  <br/> |
|거부 된 액세스 요청  <br/> |accessrequestdenied 됨  <br/> |사이트, 폴더 또는 문서에 대 한 액세스 요청이 거부 되었습니다.  <br/> |
|사이트 모음에 대 한 수정 된 사용 권한 수준  <br/> |권한 levelmodified  <br/> |사이트 모음에서 사용 권한 수준이 변경 되었습니다.  <br/> |
|회사 공유 가능 링크가 제거 됨  <br/> |CompanyLinkRemoved  <br/> |사용자가 자원에 대 한 회사 차원 링크를 제거 했습니다. 링크를 더 이상 사용 하 여 리소스에 액세스할 수 없습니다.  <br/> |
|익명 링크 제거  <br/> |AnonymousLinkRemoved  <br/> |사용자가 리소스에 대 한 익명 링크를 제거 했습니다. 링크를 더 이상 사용 하 여 리소스에 액세스할 수 없습니다.  <br/> |
|사이트 모음에서 사용 권한 수준을 제거 했습니다.  <br/> |권한 level제거 됨  <br/> |사이트 모음에서 사용 권한 수준이 제거 되었습니다.  <br/> |
|복원 된 공유 상속  <br/> |SharingInheritanceReset  <br/> |항목이 상위 항목에서 공유 사용 권한을 상속 하도록 변경 내용이 적용 되었습니다.  <br/> |
|공유 파일, 폴더 또는 사이트  <br/> |SharingSet  <br/> |사용자 (구성원 또는 게스트) SharePoint 또는 비즈니스용 OneDrive의 파일, 폴더 또는 사이트를 조직의 디렉터리에 있는 사용자와 공유 합니다. 이 활동에 대 한 **세부 정보** 열의 값은 리소스가 공유 된 사용자의 이름과이 사용자가 구성원 또는 게스트 인지를 식별 합니다. 이 작업은 대개 사용자에 게 리소스에 대 한 액세스 권한을 부여 하는 방법을 설명 하는 두 번째 이벤트가 수반 됩니다. 예를 들어, 리소스에 대 한 액세스 권한이 있는 그룹에 사용자를 추가 합니다.  <br/> |
|업데이트 된 액세스 요청  <br/> |accessrequestupdated 됨  <br/> |항목에 대 한 액세스 요청이 업데이트 되었습니다.  <br/> |
|익명 링크가 업데이트 되었습니다.  <br/> |AnonymousLinkUpdated  <br/> |사용자가 리소스에 대 한 익명 링크를 업데이트 했습니다. 업데이트 된 필드는 검색 결과를 내보낼 때 EventData 속성에 포함 됩니다.  <br/> |
|업데이트 된 공유 초대  <br/> |SharingInvitationUpdated  <br/> |외부 공유 초대를 업데이트 했습니다.  <br/> |
|익명 링크를 사용 했습니다.  <br/> |AnonymousLinkUsed  <br/> |익명 사용자가 익명 링크를 사용 하 여 리소스에 액세스 했습니다. 사용자의 id를 알 수는 없지만 사용자의 IP 주소와 같은 기타 세부 정보를 얻을 수 있습니다.  <br/> |
|공유 되지 않는 파일, 폴더 또는 사이트  <br/> |SharingRevoked  <br/> |사용자 (구성원 또는 게스트)가 다른 사용자와 이전에 공유 된 파일, 폴더 또는 사이트를 공유 하지 않습니다.  <br/> |
|회사의 공유 가능한 링크를 사용 합니다.  <br/> |CompanyLinkUsed  <br/> |사용자가 회사 차원 링크를 사용 하 여 리소스에 액세스 했습니다.  <br/> |
|사용 되는 보안 링크  <br/> |securelinkused  <br/> |사용자가 안전한 링크를 사용 했습니다.  <br/> |
|보안 링크에 사용자 추가  <br/> |ad이상 tosecurelink  <br/> |보안 공유 링크를 사용할 수 있는 엔터티 목록에 사용자가 추가 되었습니다.  <br/> |
|보안 링크에서 사용자 제거  <br/> |RemovedFromSecureLink  <br/> |보안 공유 링크를 사용할 수 있는 엔터티 목록에서 사용자를 제거 했습니다.  <br/> |
|Withdrew 공유 초대  <br/> |SharingInvitationRevoked  <br/> |사용자가 리소스에 대 한 공유 초대를 withdrew 합니다.  <br/> |
||||
  
### <a name="synchronization-activities"></a>동기화 작업
  
다음 표에는 SharePoint Online 및 비즈니스용 OneDrive의 파일 동기화 작업이 나와 있습니다.
  
|**식별 이름**|**Operation**|**설명**|
|:-----|:-----|:-----|
|파일을 동기화 할 수 있는 컴퓨터  <br/> |managedsyncclientallowed  <br/> |사용자가 사이트와 동기화 관계를 설정 했습니다. 사용자의 컴퓨터가 조직의 문서 라이브러리에 액세스할 수 있는 도메인 ( *수신 허용-받는 사람 목록* 이라고 함)의 목록에 추가 된 domain의 구성원 인 경우 동기화 관계가 성공적입니다.  <br/> 이 기능에 대 한 자세한 내용은 [수신 허용-받는 사람 목록에 있는 도메인에 대해 OneDrive 동기화를 사용 하도록 설정 하려면 Windows PowerShell cmdlet 사용](https://go.microsoft.com/fwlink/p/?LinkID=534609)을 참조 하십시오.  <br/> |
|파일이 동기화 되지 않도록 차단 된 컴퓨터  <br/> |UnmanagedSyncClientBlocked  <br/> |사용자가 조직의 도메인 구성원이 아니거나 문서에 액세스할 수 있는 도메인 ( *수신 허용-받는 사람 목록)* 에 추가 되지 않은 도메인의 구성원 인 컴퓨터의 사이트와 동기화 관계를 설정 하려고 합니다. 조직의 라이브러리 동기화 관계는 허용 되지 않으며, 사용자 컴퓨터는 문서 라이브러리의 파일 동기화, 다운로드 또는 업로드를 차단 합니다.  <br/> 이 기능에 대 한 자세한 내용은 [수신 허용-받는 사람 목록에 있는 도메인에 대해 OneDrive 동기화를 사용 하도록 설정 하려면 Windows PowerShell cmdlet 사용](https://go.microsoft.com/fwlink/p/?LinkID=534609)을 참조 하십시오.  <br/> |
|컴퓨터에 다운로드 한 파일  <br/> |FileSyncDownloadedFull  <br/> |사용자가 동기화 관계를 설정 하 고 파일을 처음으로 문서 라이브러리에서 컴퓨터로 다운로드 합니다.  <br/> |
|컴퓨터에 다운로드 한 파일 변경 내용  <br/> |FileSyncDownloadedPartial  <br/> |사용자가 문서 라이브러리의 파일에 대 한 변경 내용을 성공적으로 다운로드 합니다. 이 작업은 문서 라이브러리의 파일에 대 한 변경 내용이 사용자 컴퓨터로 다운로드 되었음을 나타냅니다. 사용자가 문서 라이브러리를 이전에 다운로드 했기 때문에 ( **다운로드 한 파일에서 컴퓨터** 작업으로 표시) 변경 내용만 다운로드 되었습니다.  <br/> |
|문서 라이브러리에 업로드 된 파일  <br/> |FileSyncUploadedFull  <br/> |사용자가 자신의 컴퓨터에서 문서 라이브러리로 처음으로 동기화 관계를 설정 하 고 파일을 성공적으로 업로드 합니다.  <br/> |
|문서 라이브러리에 업로드 된 파일 변경 내용  <br/> |FileSyncUploadedPartial  <br/> |사용자가 문서 라이브러리의 파일에 대 한 변경 내용을 업로드 했습니다. 이 이벤트는 문서 라이브러리의 파일 로컬 버전에 대해 변경한 내용이 문서 라이브러리에 성공적으로 업로드되었음을 나타냅니다. 변경 내용은 이전에 사용자가 업로드 한 것 이며 (* * 파일을 문서 라이브러리에 업로드 한 파일로 표시 됨) 해당 파일이 언로드된 작업입니다.  <br/> |
||||
  
### <a name="site-administration-activities"></a>사이트 관리 작업
  
다음 표에는 SharePoint Online의 사이트 관리 작업에서 발생 하는 이벤트가 나와 있습니다.
  
|**식별 이름**|**Operation**|**설명**|
|:-----|:-----|:-----|
|예외 사용자 에이전트 추가  <br/> |ExemptUserAgentSet  <br/> |sharepoint 또는 전역 관리자가 sharepoint 관리 센터에서 예외 사용자 에이전트 목록에 사용자 에이전트를 추가 합니다.  <br/> |
|사이트 모음 관리자 추가  <br/> |SiteCollectionAdminAdded  <br/> |사이트 모음 관리자 또는 소유자가 사이트의 사이트 모음 관리자로 사용자를 추가 합니다. 사이트 모음 관리자는 사이트 모음 및 모든 하위 사이트에 대해 모든 권한을 갖습니다. 또한 관리자가 SharePoint 관리 센터에서 사용자 프로필을 편집 하거나 [Office 365 관리 센터를 사용](https://docs.microsoft.com/office365/admin/add-users/get-access-to-and-back-up-a-former-user-s-data#part-1---get-access-to-the-former-employees-onedrive-for-business-documents)하 여 사용자의 OneDrive 계정에 대 한 액세스를 제공 하는 경우에도이 작업이 기록 됩니다. <br/> |
|none  <br/> |SiteCollectionAdminRemoved <br/> |사이트 모음 관리자 또는 소유자가 사이트의 사이트 모음 관리자로 사용자를 제거 합니다. 이 작업은 또한 관리자가 SharePoint 관리 센터에서 사용자 프로필을 편집 하 여 사용자의 OneDrive 계정에 대 한 사이트 모음 관리자 목록에서 자신을 제거할 때에도 기록 됩니다.  감사 로그 검색 결과에서이 활동을 반환 하려면 모든 작업을 검색 해야 합니다. <br/> |
|SharePoint 그룹에 사용자 또는 그룹을 추가 했습니다.  <br/> |addedtogroup  <br/> |사용자가 SharePoint 그룹에 구성원 또는 게스트를 추가 했습니다. 의도적인 동작이 나 공유 이벤트와 같은 다른 작업의 결과가 있을 수 있습니다.  <br/> |
|그룹을 만들 수 있는 사용자  <br/> |AllowGroupCreationSet  <br/> |사이트 관리자 또는 소유자는 해당 권한이 할당 된 사용자가 해당 사이트에 대 한 그룹을 만들 수 있도록 허용 하는 사용 권한 수준을 사이트에 추가 합니다.  <br/> |
|사이트 지리적 이동 취소  <br/> |SiteGeoMoveCancelled  <br/> |sharepoint 또는 전역 관리자가 sharepoint 또는 OneDrive 사이트 지리적 이동을 성공적으로 취소 합니다. 다중 위치 기능을 사용 하면 office 365 조직에서 여러 office 365 데이터 센터 지역 (예를 들어, geos)을 사용할 수 있습니다. 자세한 내용은 [OneDrive 및 Office 365에서 SharePoint Online의 다중 지리적 기능](https://go.microsoft.com/fwlink/?linkid=860840)을 참조 하세요.  <br/> |
|공유 정책 변경  <br/> |SharingPolicyChanged  <br/> |sharepoint 또는 전역 관리자가 Office 365 관리 포털, sharepoint 관리 포털 또는 SharePoint Online 관리 셸을 사용 하 여 sharepoint 공유 정책을 변경 했습니다. 조직의 공유 정책 설정에 대 한 모든 변경 내용이 기록 됩니다. 변경 된 정책은 이벤트 레코드의 자세한 속성에 있는 **ModifiedProperties** 필드에서 식별 됩니다.  <br/> |
|변경 된 장치 액세스 정책  <br/> |DeviceAccessPolicyChanged  <br/> |SharePoint 또는 전역 관리자가 조직에 대해 관리 되지 않는 장치 정책을 변경 했습니다. 이 정책은 조직에 가입 되지 않은 장치에서 SharePoint, OneDrive 및 Office 365에 대 한 액세스를 제어 합니다. 이 정책을 구성 하려면 엔터프라이즈 이동성 + 보안 구독이 필요 합니다. 자세한 내용은 [관리 되지 않는 장치에서의 액세스 제어](https://support.office.com/article/5ae550c4-bd20-4257-847b-5c20fb053622)를 참조 하세요.  <br/> |
|변경 된 예외 사용자 에이전트  <br/> |CustomizeExemptUsers  <br/> |sharepoint 또는 전역 관리자가 sharepoint 관리 센터에서 예외 사용자 에이전트 목록을 사용자 지정 했습니다. 인덱싱할 전체 웹 페이지를 받지 못하도록 제외되는 사용자 에이전트를 지정할 수 있습니다. 즉, 제외로 지정한 사용자 에이전트가 InfoPath 양식을 만나면 전체 웹 페이지가 아닌 XML 파일로 반환 됩니다 (해당 양식이 있는 경우). 따라서 InfoPath 양식 인덱싱 속도가 빨라집니다.  <br/> |
|네트워크 액세스 정책 변경  <br/> |NetworkAccessPolicyChanged  <br/> |sharepoint 또는 전역 관리자가 sharepoint 관리 센터에서 또는 sharepoint Online PowerShell을 사용 하 여 위치 기반 액세스 정책 (신뢰할 수 있는 네트워크 경계 라고도 함)을 변경 했습니다. 이 정책 유형은 사용자가 지정한 승인 된 IP 주소 범위에 따라 조직의 SharePoint 및 OneDrive 리소스에 액세스할 수 있는 사람을 제어 합니다. 자세한 내용은 [네트워크 위치를 기반으로 SharePoint Online 및 OneDrive 데이터에 대 한 제어 액세스](https://support.office.com/article/b5a5f1f1-1174-4c6b-91d0-9273a6b6971f)를 참조 하세요.  <br/> |
|완료 된 사이트 지리적 이동  <br/> |SiteGeoMoveCompleted  <br/> |조직의 전역 관리자가 예약한 사이트 지리적 이동이 성공적으로 완료 되었습니다. 다중 위치 기능을 사용 하면 office 365 조직에서 여러 office 365 데이터 센터 지역 (예를 들어, geos)을 사용할 수 있습니다. 자세한 내용은 [OneDrive 및 Office 365에서 SharePoint Online의 다중 지리적 기능](https://go.microsoft.com/fwlink/?linkid=860840)을 참조 하세요.  <br/> |
|만든 그룹  <br/> |groupadded 됨  <br/> |사이트 관리자 또는 소유자가 사이트에 대 한 그룹을 만들거나 그룹을 만드는 작업을 수행 합니다. 예를 들어 사용자가 파일을 공유 하기 위한 링크를 처음 만들 때 사용자의 비즈니스용 OneDrive 사이트에 시스템 그룹이 추가 됩니다. 사용자가 공유 파일에 대한 편집 권한이 있는 링크를 만들어도 이 이벤트가 발생할 수 있습니다.  <br/> |
|만든 사람에 게 연결 되었습니다.  <br/> |sendtoconnectionadded 됨  <br/> |sharepoint 또는 전역 관리자가 sharepoint 관리 센터의 레코드 관리 페이지에서 새 보내기 연결을 만듭니다. 보내기 연결은 문서 리포지토리 또는 레코드 센터에 대한 설정을 지정합니다. 보내기 연결을 만들면 콘텐츠 구성 도우미가 지정된 위치로 문서를 전송할 수 있습니다.  <br/> |
|만든 사이트 모음  <br/> |SiteCollectionCreated  <br/> |sharepoint 또는 전역 관리자가 sharepoint Online 조직에 새 사이트 모음을 만들거나 사용자가 비즈니스용 OneDrive 사이트를 프로 비전 합니다.  <br/> |
|삭제 된 그룹  <br/> |그룹 제거 됨  <br/> |사용자가 사이트에서 그룹을 삭제 합니다.  <br/> |
|삭제 된 메시지를 연결로 보냄  <br/> |sendtoconnectionremoved 됨  <br/> |sharepoint 또는 전역 관리자가 sharepoint 관리 센터의 레코드 관리 페이지에서 보내기 연결을 삭제 합니다.  <br/> |
|삭제 된 사이트  <br/> |sitedeleted 됨  <br/> |사이트 관리자가 사이트를 삭제 합니다.  <br/> |
|문서 미리 보기 사용  <br/> |PreviewModeEnabledSet  <br/> |사이트 관리자가 사이트에 대해 문서 미리 보기를 사용 하도록 설정 합니다.  <br/> |
|레거시 워크플로 사용  <br/> |LegacyWorkflowEnabledSet  <br/> |사이트 관리자 또는 소유자가 사이트에 SharePoint 2013 워크플로 작업 콘텐츠 형식을 추가합니다. 또한 전역 관리자는 SharePoint 관리 센터에서 전체 조직에 대한 워크플로를 사용하도록 설정할 수 있습니다.  <br/> |
|Office on Demand 설정  <br/> |OfficeOnDemandSet  <br/> |사이트 관리자가 최신 버전의 Office 데스크톱 응용 프로그램에 액세스할 수 있도록 하는 Office on Demand를 사용하도록 설정합니다. office on Demand는 SharePoint 관리 센터에서 사용 하도록 설정 되며, 설치 된 모든 office 응용 프로그램을 포함 하는 office 365 구독이 필요 합니다.  <br/> |
|RSS 피드 사용  <br/> |NewsFeedEnabledSet  <br/> |사이트 관리자 또는 소유자는 사이트에 대해 RSS 피드를 사용 하도록 설정 합니다. 전역 관리자는 SharePoint 관리 센터에서 전체 조직에 대한 RSS 피드를 사용하도록 설정할 수 있습니다.  <br/> |
|수정 된 액세스 요청 설정  <br/> |webrequestaccessmodified  <br/> |사이트에서 액세스 요청 설정이 수정 되었습니다.  <br/> |
|수정 된 구성원의 공유 가능 설정  <br/> |WebMembersCanShareModified  <br/> |**구성원 공유 가능** 설정이 사이트에서 수정 되었습니다.  <br/> |
|수정 된 사이트 사용 권한  <br/> |SitePermissionsModified  <br/> |사이트 관리자나 소유자 (또는 시스템 계정)는 사이트의 그룹에 할당 된 사용 권한 수준을 변경 합니다. 이 작업은 모든 사용 권한이 그룹에서 제거 된 경우에도 기록 됩니다.  <br/> > [!NOTE]>이 작업은 SharePoint Online에서 더 이상 사용 되지 않습니다. 관련 이벤트를 찾으려면 **추가 된 사이트 모음 관리자**, **사용자 또는 그룹을 SharePoint 그룹에 추가 하거나** **그룹을 만들고** **만든 그룹**및 삭제할 수 있는 다른 사용 권한 관련 작업을 검색 하면 됩니다. ** 그룹입니다.**         |
|SharePoint 그룹에서 사용자 또는 그룹 제거  <br/> |RemovedFromGroup  <br/> |사용자가 SharePoint 그룹에서 구성원 또는 게스트를 제거 했습니다. 이 작업은 의도적인 동작이 나 다른 작업의 결과 (예: 공유가 해제 이벤트) 일 수 있습니다.  <br/> |
|이름이 바뀐 사이트  <br/> |SiteRenamed  <br/> |사이트 관리자 또는 소유자가 사이트의 이름을 바꿉니다.  <br/> |
|요청 된 사이트 관리자 권한  <br/> |siteadminchangerequest  <br/> |사용자 요청을 사이트 모음에 대 한 사이트 모음 관리자로 추가 합니다. 사이트 모음 관리자는 사이트 모음 및 모든 하위 사이트에 대해 모든 권한을 갖습니다.  <br/> |
|예약 된 사이트 지리적 이동  <br/> |SiteGeoMoveScheduled  <br/> |sharepoint 또는 전역 관리자가 sharepoint 또는 OneDrive 사이트 지리적 이동을 성공적으로 예약 합니다. 다중 위치 기능을 사용 하면 office 365 조직에서 여러 office 365 데이터 센터 지역 (예를 들어, geos)을 사용할 수 있습니다. 자세한 내용은 [OneDrive 및 Office 365에서 SharePoint Online의 다중 지리적 기능](https://go.microsoft.com/fwlink/?linkid=860840)을 참조 하세요.  <br/> |
|호스트 사이트 설정  <br/> |hostsiteset  <br/> |SharePoint 또는 전역 관리자가 개인 또는 비즈니스용 OneDrive 사이트를 호스팅하도록 지정 된 사이트를 변경 합니다.  <br/> |
|업데이트 된 그룹  <br/> |groupupdated  <br/> |사이트 관리자 또는 소유자가 사이트에 대 한 그룹의 설정을 변경 합니다. 여기에는 그룹의 이름, 그룹 구성원 자격을 보거나 편집할 수 있는 사람 및 구성원 요청이 처리되는 방법을 변경하는 경우가 포함될 수 있습니다.  <br/> |
||||
  
### <a name="exchange-mailbox-activities"></a>Exchange 사서함 활동
  
다음 표에는 사서함 감사 로깅에서 로깅할 수 있는 작업이 나와 있습니다. 사서함 소유자, 위임 된 사용자 또는 관리자가 수행한 사서함 활동을 기록 합니다. 기본적으로 Office 365의 사서함 감사는 설정 되어 있지 않습니다. 사서함 작업을 기록 하기 전에 각 사서함에 대해 사서함 감사 로깅을 켜야 합니다. 자세한 내용은 [Office 365에서 사서함 감사 사용](https://go.microsoft.com/fwlink/p/?LinkID=626109)을 참조 하십시오.
  
|**식별 이름**|**Operation**|**설명**|
|:-----|:-----|:-----|
|대리인 사서함 사용 권한 추가  <br/> |add-mailboxpermission 추가  <br/> |관리자가 다른 사람의 사서함에 대 한 사용자 (대리인)에 게 FullAccess 사서함 권한을 할당 했습니다. FullAccess 사용 권한을 사용 하면 대리인이 다른 사용자의 사서함을 열고 사서함의 내용을 읽고 관리할 수 있습니다.  <br/> |
|레코드로 분류 된 메시지  <br/> |applyrecordlabel<br/> |메시지가 레코드로 분류 되었습니다. 콘텐츠를 레코드로 분류 하는 보존 레이블이 수동으로 또는 메시지에 자동으로 적용 되는 경우이 이벤트가 발생 합니다.<br/> |
|다른 폴더로 복사한 메시지  <br/> |복사  <br/> |메시지가 다른 폴더에 복사되었습니다.  <br/> |
|만든 사서함 항목  <br/> |만들기  <br/> |사서함의 일정, 연락처, 메모 또는 작업 폴더에 항목이 만들어집니다. 예를 들어 새 모임 요청이 만들어집니다. 메시지 만들기, 보내기 또는 받기는 감사 되지 않습니다. 또한 사서함 폴더를 만드는 것은 감사 되지 않습니다.  <br/> |
|Outlook web app에서 새 받은 편지함 규칙을 만들었습니다.  <br/> |NewInboxRule<br/> |<br/> |
|지운 편지함 폴더에서 삭제 된 메시지  <br/> |SoftDelete  <br/> |메시지가 지운 편지함 폴더에서 삭제되어가 영구적으로 삭제되었습니다. 이러한 항목은 복구 가능한 항목 폴더로 이동 됩니다. 또한 메시지는 사용자가 선택 하 고 **Shift + Delete**를 누를 때 복구 가능한 항목 폴더로 이동 됩니다.  <br/> |
|메시지를 다른 폴더로 이동  <br/> |이동  <br/> |메시지가 다른 폴더로 이동했습니다.  <br/> |
|지운 편지함 폴더로 메시지 이동  <br/> |MoveToDeletedItems  <br/> |메시지가 삭제되어 지운 편지함 폴더로 이동되었습니다.  <br/> |
|수정 된 폴더 권한  <br/> |updatefolderpermissions 작업이 로깅됩니다  <br/> |폴더 사용 권한이 변경 되었습니다. 폴더 사용 권한은 조직에서 사서함 폴더 및 폴더의 메시지에 액세스할 수 있는 사용자를 제어 합니다.  <br/> |
|사서함에서 메시지 제거  <br/> |HardDelete  <br/> |메시지가 복구 가능한 항목 폴더 (사서함에서 영구적으로 삭제 됨)에서 제거 되었습니다.  <br/> |
|대리인 사서함 사용 권한 제거  <br/> |add-mailboxpermission을 제거 합니다.  <br/> |관리자가 사용자의 사서함에서 대리인에 게 할당 된 FullAccess 사용 권한을 제거 했습니다. FullAccess 사용 권한이 제거 되 면 대리인은 다른 사람의 사서함을 열거나 해당 사용자의 모든 콘텐츠에 액세스할 수 없습니다.  <br/> |
|메시지를 다른 사람 이름으로 보내기 권한을 사용 하 여 보냄  <br/> |SendAs  <br/> |메시지가 SendAs 권한을 사용하여 전송되었습니다. 즉 사서함 소유자가 보낸 것처럼 보이도록 하여 다른 사용자가 메시지를 보냈습니다.  <br/> |
|"대신 보내기" 권한을 사용 하 여 보낸 메시지  <br/> |SendOnBehalf  <br/> |메시지가 SendOnBehalf 권한을 사용하여 전송되었습니다. 즉 다른 사용자가 사서함 소유자 대신에 메시지를 보냈습니다. 받는 사람은 메시지를 대신 보낸 사용자와 해당 메시지를 실제로 보낸 사용자를 메시지에서 확인할 수 있습니다.  <br/> |
|일정 폴더에 대 한 대리인 액세스 업데이트  <br/> |UpdateCalendarDelegation  <br/> |일정 위임이 사서함에 할당 되었습니다. 일정 위임 같은 조직에서 사서함 소유자의 일정을 관리 하는 다른 사람에 게 제공 합니다.  <br/> |
|업데이트 된 메시지  <br/> |업데이트  <br/> |메시지 또는 해당 속성이 변경되었습니다.  <br/> |
|사용자가 사서함에 로그인 되어 있음  <br/> |MailboxLogin  <br/> |사용자가 자신의 사서함에 로그인했습니다.  <br/> |
|none  <br/> |UpdateInboxRules  <br/> |받은 편지함 규칙이 추가, 제거 또는 변경 된 경우 받은 편지함 규칙은 지정 된 조건에 따라 사용자의 받은 편지함에서 메시지를 처리 하 고, 메시지를 지정 된 폴더로 이동 하거나 메시지를 삭제 하는 것과 같이 규칙의 조건이 충족 될 때 작업을 수행 하는 데 사용 됩니다.  <br/> 받은 편지함 규칙 활동의 항목을 반환 하려면 **활동** 목록에서 **모든 활동에 대 한 결과 표시** 를 선택 해야 합니다. 날짜 범위 상자와 **사용자** 목록을 사용 하 여 검색 결과의 범위를 좁힐 수 있습니다.  <br/> |
||||
  
### <a name="retention-policy-and-label-activities"></a>보존 정책 및 레이블 활동

다음 표에서는 보안 & 준수 센터의 보존 정책 및 보존 레이블과 관련 된 작업에 대해 설명 합니다. 자세한 내용은 다음을 참조하세요.

- [보존 정책 개요](retention-policies.md)
- [보존 레이블 개요](labels.md)
<br/>

|**작업**|**Operation**|**설명**|
|:-----|:-----|:-----|
| 보존 정책에 대 한 보존 구성을 만들었습니다.<br/> |NewRetentionComplianceRule<br/> |관리자가 새 보존 정책에 대 한 보존 설정을 구성 합니다. 보존 설정에는 항목이 보존 되는 기간, 보존 기간이 만료 되 면 항목 삭제, 항목 보존 또는 삭제와 같은 항목이 수행 되는 시간이 포함 됩니다. 이 활동은 [new-retentioncompliancerule](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-retention/new-retentioncompliancerule) cmdlet을 실행 하는 경우에도 해당 됩니다.<br/>|
| 만든 보존 레이블 <br/> |NewComplianceTag<br/>  |관리자가 새 보존 레이블을 만듭니다.<br/> |
| 만들어진 보존 정책<br/> |NewRetentionCompliancePolicy<br/> |관리자가 새 보존 정책을 만듭니다.<br/>  |
| 보존 정책에 대 한 삭제 된 보존 구성<br/> | RemoveRetentionComplianceRule<br/>| 관리자가 보존 정책의 구성 설정을 삭제 합니다. 이 작업은 관리자가 보존 정책을 삭제 하거나 **new-retentioncompliancerule** cmdlet을 실행 하는 경우에 기록 될 수 있습니다.<br/> |
| 삭제 된 보존 레이블 <br/> |removecompliancetag<br/>  | 관리자가 보존 레이블을 삭제 합니다.<br/>|
| 삭제 된 보존 정책<br/> |RemoveRetentionCompliancePolicy<br/> |관리자가 보존 정책을 삭제 합니다. <br/>  |
| 규정 준수 기능 사용<br/> |SetRestrictiveRetentionUI<br/> |관리자는 RegulatoryComplianceUI cmdlet을 실행 하 여 규정 준수 기능을 사용 하도록 **설정** 합니다. 이 cmdlet을 실행 하 고 나면 관리자가 보안 & 준수 센터 UI를 사용 하 여 보존 정책을 잠그고 보존 레이블을 규정 레코드로 지정할 수 있습니다. 조직에서 **RegulatoryComplianceUI** cmdlet을 사용 하 여 이러한 기능을 사용 하도록 설정 하기 전 까지는 보존 정책을 잠그고 규정 보존 레이블을 만드는 작업을 PowerShell을 통해서만 수행할 수 있습니다. <br/>|
| 보존 정책에 대 한 업데이트 된 보존 구성<br/> | SetRetentionComplianceRule<br/>| 관리자가 기존 보존 정책에 대 한 보존 설정을 변경 합니다. 보존 설정에는 항목이 보존 되는 기간, 보존 기간이 만료 되 면 항목 삭제, 항목 보존 또는 삭제와 같은 항목이 수행 되는 시간이 포함 됩니다. 이 활동은 [new-retentioncompliancerule](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-retention/set-retentioncompliancerule) cmdlet을 실행 하는 경우에도 해당 됩니다. <br/>|
| 업데이트 된 보존 레이블 <br/> |SetComplianceTag<br/>  | 관리자가 기존 보존 레이블을 업데이트 합니다.<br/>|
| 업데이트 된 보존 정책<br/> |SetRetentionCompliancePolicy <br/>|관리자가 기존 보존 정책을 업데이트 합니다. 이 이벤트를 트리거하는 업데이트에는 보존 정책이 적용 되는 콘텐츠 위치 추가 또는 제외가 포함 됩니다.<br/>|
||||

### <a name="sway-activities"></a>Sway 활동
  
다음 표에는 Sway의 사용자 및 관리 활동이 나와 있습니다. Sway는 대화형 웹 기반 캔버스에서 아이디어, 스토리 및 프레젠테이션을 수집 하 고 서식을 지정 하 고 공유 하는 데 도움이 되는 Office 365 앱입니다. 자세한 내용은 [Sway-Admin 도움말에 대 한 질문과 대답](https://support.office.com/article/446380fa-25bf-47b2-996c-e12cb2f9d075)을 참조 하십시오.
  
|**식별 이름**|**Operation**|**설명**|
|:-----|:-----|:-----|
|변경 된 Sway 공유 수준  <br/> |SwayChangeShareLevel  <br/> |사용자가 Sway의 공유 수준을 변경 했습니다. 이 이벤트는 Sway와 연결 된 공유 범위를 변경 하는 사용자를 캡처합니다. 예를 들면 public과 조직 내부입니다.  <br/> |
|만든 Sway  <br/> |SwayCreate  <br/> |사용자가 Sway를 만듭니다.  <br/> |
|삭제 된 Sway  <br/> |SwayDelete  <br/> |사용자가 Sway를 삭제 합니다.  <br/> |
|사용 하지 않도록 설정 된 Sway 복제  <br/> |SwayDisableDuplication  <br/> |사용자가 Sway 중복을 사용 하지 않도록 설정 합니다.  <br/> |
|중복 된 Sway  <br/> |SwayDuplicate  <br/> |사용자가 Sway를 복제 합니다.  <br/> |
|편집 된 Sway  <br/> |SwayEdit  <br/> |사용자가 Sway를 편집 합니다.  <br/> |
|사용 하도록 설정 된 Sway 복제  <br/> |enableduplication  <br/> |사용자가 Sway를 복제할 수 있습니다. 사용자가 Sway의 중복을 사용 하도록 설정 하는 기능은 기본적으로 사용 하도록 설정 됩니다.  <br/> |
|취소 된 Sway 공유  <br/> |SwayRevokeShare  <br/> |사용자가 액세스를 취소 하 여 Sway 공유를 중지 합니다. 액세스를 취소 하면 Sway와 연결 된 연결이 변경 됩니다.  <br/> |
|공유 Sway  <br/> |SwayShare  <br/> |사용자가 Sway를 공유 하려고 합니다. 이 이벤트는 Sway 공유 메뉴에서 특정 공유 대상을 클릭 했을 때의 사용자 작업을 캡처합니다. 이 이벤트는 사용자가 공유 작업을 완료 했는지 여부를 나타내지 않습니다.  <br/> |
|Sway 외부 공유 해제  <br/> |SwayExternalSharingOff  <br/> |관리자는 Office 365 관리 센터를 사용 하 여 전체 조직에 대해 외부 Sway 공유를 사용할 수 없도록 설정 합니다.  <br/> |
|Sway 외부 공유 설정  <br/> |SwayExternalSharingOn  <br/> |관리자는 Office 365 관리 센터를 사용 하 여 전체 조직에 대 한 외부 Sway 공유를 사용 하도록 설정 합니다.  <br/> |
|Sway 서비스 해제  <br/> |SwayServiceOff  <br/> |관리자는 Office 365 관리 센터를 사용 하 여 전체 조직에 대해 Sway를 사용 하지 않도록 설정 합니다.  <br/> |
|Sway 서비스 설정  <br/> |SwayServiceOn  <br/> |관리자는 Office 365 관리 센터를 사용 하 여 전체 조직에 sway를 사용 하도록 설정 합니다 (sway service는 기본적으로 사용 하도록 설정 됨).  <br/> |
|Sway 보기  <br/> |SwayView  <br/> |사용자가 Sway를 볼 수 있습니다.  <br/> |
||||

  
### <a name="user-administration-activities"></a>사용자 관리 활동
  
다음 표에는 관리자가 Office 365 관리 센터 또는 Azure 관리 포털을 사용 하 여 사용자 계정을 추가 하거나 변경할 때 기록 되는 사용자 관리 작업이 나와 있습니다.
  
|**작업**|**Operation**|**설명**|
|:-----|:-----|:-----|
|추가 된 사용자  <br/> |사용자를 추가 합니다.  <br/> |Office 365 사용자 계정을 만들었습니다.  <br/> |
|변경 된 사용자 라이선스  <br/> |사용자 라이선스 변경  <br/> |변경 된 사용자에 게 할당 된 라이선스 변경 된 라이선스를 확인 하려면 해당 **업데이트 된 사용자** 활동을 참조 하십시오.  <br/> |
|변경 된 사용자 암호  <br/> |사용자 암호 변경  <br/> |관리자가 사용자 암호 암호를 변경 했습니다.  <br/> |
|삭제 된 사용자  <br/> |Delete user  <br/> |Office 365 사용자 계정이 삭제 되었습니다.  <br/> |
|사용자 암호 다시 설정  <br/> |사용자 암호 다시 설정  <br/> |관리자가 사용자의 암호를 다시 설정 합니다.  <br/> |
|사용자가 암호를 변경 하도록 강제 적용 하는 속성 설정  <br/> |강제 변경 사용자 암호 설정  <br/> |관리자는 사용자가 다음에 Office 365에 로그인 할 때 사용자에 게 암호를 변경 하도록 강제 하는 속성을 설정 합니다.  <br/> |
|라이선스 속성 설정  <br/> |라이선스 속성 설정  <br/> |관리자가 사용자에 게 할당 된 라이선스의 속성을 수정 합니다.  <br/> |
|업데이트 된 사용자  <br/> |사용자 업데이트  <br/> |관리자가 사용자 계정의 속성을 하나 이상 변경 합니다. 업데이트할 수 있는 사용자 속성 목록은 [Azure Active Directory Audit Report 이벤트](https://go.microsoft.com/fwlink/p/?LinkID=616549)의 "사용자 특성 업데이트" 섹션을 참조 하십시오.  <br/> |
||||
  
### <a name="azure-ad-group-administration-activities"></a>Azure AD 그룹 관리 작업
  
다음 표에는 관리자 또는 사용자가 office 365 그룹을 만들거나 변경할 때 또는 관리자가 office 365 관리 센터 또는 Azure 관리 포털을 사용 하 여 보안 그룹을 만들 때 기록 되는 그룹 관리 작업이 나와 있습니다. office 365의 그룹에 대 한 자세한 내용은 [office 365 관리 센터에서 그룹 보기, 만들기 및 삭제](https://support.office.com/article/a6360120-2fc4-46af-b105-6a04dc5461c7)를 참조 하세요.
  
|**식별 이름**|**Operation**|**설명**|
|:-----|:-----|:-----|
|추가 된 그룹  <br/> |그룹 추가  <br/> |그룹을 만들었습니다.  <br/> |
|그룹에 구성원 추가 됨  <br/> |그룹에 구성원 추가  <br/> |구성원이 그룹에 추가 되었습니다.  <br/> |
|삭제 된 그룹  <br/> |그룹 삭제  <br/> |그룹이 삭제 되었습니다.  <br/> |
|그룹에서 구성원 제거 됨  <br/> |그룹에서 구성원 제거  <br/> |구성원이 그룹에서 제거 되었습니다.  <br/> |
|업데이트 된 그룹  <br/> |그룹 업데이트  <br/> |그룹의 속성이 변경 되었습니다.  <br/> |
||||
   
### <a name="application-administration-activities"></a>응용 프로그램 관리 작업
  
다음 표에는 관리자가 Azure AD에 등록 된 응용 프로그램을 추가 하거나 변경할 때 기록 되는 응용 프로그램 관리 작업이 나와 있습니다. 인증에 Azure AD를 사용 하는 모든 응용 프로그램은 디렉터리에 등록 되어 있어야 합니다.
  
|**식별 이름**|**Operation**|**설명**|
|:-----|:-----|:-----|
|위임 항목 추가 됨  <br/> |위임 항목 추가  <br/> |Azure AD에서 응용 프로그램에 대 한 인증 권한이 생성/부여 되었습니다.  <br/> |
|서비스 사용자 추가 됨  <br/> |서비스 사용자 추가  <br/> |응용 프로그램이 Azure AD에 등록 되었습니다. 응용 프로그램은 디렉터리에서 서비스 사용자에 게 표시 됩니다.  <br/> |
|서비스 사용자에 게 자격 증명 추가  <br/> |서비스 사용자 자격 증명 추가  <br/> |Azure AD의 서비스 사용자에 게 자격 증명이 추가 되었습니다. 서비스 원칙은 디렉터리에 있는 응용 프로그램을 나타냅니다.  <br/> |
|제거 된 위임 항목  <br/> |위임 항목 제거  <br/> |Azure AD의 응용 프로그램에서 인증 권한이 제거 되었습니다.  <br/> |
|디렉터리에서 서비스 사용자 제거  <br/> |서비스 사용자 제거  <br/> |Azure AD에서 응용 프로그램이 삭제/등록 취소 되었습니다. 응용 프로그램은 디렉터리에서 서비스 사용자에 게 표시 됩니다.  <br/> |
|서비스 사용자가 자격 증명을 제거 했습니다.  <br/> |서비스 사용자 자격 증명 제거  <br/> |Azure AD의 서비스 사용자 로부터 자격 증명이 제거 되었습니다. 서비스 원칙은 디렉터리에 있는 응용 프로그램을 나타냅니다.  <br/> |
|위임 항목 설정  <br/> |위임 항목 설정  <br/> |Azure AD의 응용 프로그램에 대 한 인증 권한이 업데이트 되었습니다.  <br/> |
||||

### <a name="role-administration-activities"></a>역할 관리 작업
  
다음 표에는 관리자가 Office 365 관리 센터 또는 Azure 관리 포털에서 관리자 역할을 관리 하는 경우 기록 되는 Azure AD 역할 관리 작업이 나와 있습니다.
  
|**식별 이름**|**Operation**|**설명**|
|:-----|:-----|:-----|
|역할에 구성원 추가  <br/> |역할에 역할 구성원 추가  <br/> |Office 365에서 관리자 역할에 사용자를 추가 했습니다.  <br/> |
|디렉터리 역할에서 사용자 제거  <br/> |역할에서 역할 구성원 제거  <br/> |Office 365의 관리자 역할에서 사용자를 제거 했습니다.  <br/> |
|회사 연락처 정보 설정  <br/> |회사 연락처 정보 설정  <br/> |Office 365 조 직에 대 한 회사 수준의 연락처 기본 설정이 업데이트 되었습니다. 여기에는 office 365 서비스에 대 한 기술 알림과 함께 office 365에서 보내는 구독 관련 전자 메일의 전자 메일 주소가 포함 됩니다.  <br/> |
||||
   
### <a name="directory-administration-activities"></a>디렉터리 관리 작업
  
다음 표에는 관리자가 office 365 관리 센터 또는 Azure 관리 포털에서 office 365 조직을 관리 하는 경우 기록 되는 Azure AD 디렉터리 및 도메인 관련 작업이 나와 있습니다.
  
|**식별 이름**|**Operation**|**설명**|
|:-----|:-----|:-----|
|회사에 도메인 추가  <br/> |회사에 도메인 추가  <br/> |Office 365 조직에 도메인을 추가 했습니다.  <br/> |
|디렉터리에 파트너가 추가 됨  <br/> |회사에 파트너 추가  <br/> |Office 365 조직에 파트너 (위임 된 관리자)가 추가 되었습니다.  <br/> |
|회사에서 도메인 제거 됨  <br/> |회사에서 도메인 제거  <br/> |Office 365 조직에서 도메인을 제거 했습니다.  <br/> |
|디렉터리에서 파트너를 제거 했습니다.  <br/> |회사에서 파트너 제거  <br/> |Office 365 조직에서 파트너 (위임 된 관리자)를 제거 했습니다.  <br/> |
|회사 정보 설정  <br/> |회사 정보 설정  <br/> |Office 365 조 직에 대 한 회사 정보가 업데이트 되었습니다. 여기에는 office 365 서비스에 대 한 기술 알림과 함께 office 365에서 보내는 구독 관련 전자 메일의 전자 메일 주소가 포함 됩니다.  <br/> |
|도메인 인증 설정  <br/> |도메인 인증 설정  <br/> |Office 365 조 직에 대 한 도메인 인증 설정이 변경 되었습니다.  <br/> |
|도메인에 대 한 페더레이션 설정이 업데이트 됨  <br/> |도메인의 페더레이션 설정 설정  <br/> |Office 365 조 직에 대 한 페더레이션 (외부 공유) 설정이 변경 되었습니다.  <br/> |
|암호 정책 설정  <br/> |암호 정책 설정  <br/> |Office 365 조 직의 사용자 암호에 대 한 길이 및 문자 제약 조건이 변경 되었습니다.  <br/> |
|Azure AD sync 설정  <br/> |회사에서 고 여부 플래그 설정  <br/> |Azure AD 동기화를 위해 디렉터리를 사용할 수 있도록 하는 속성을 설정 합니다.  <br/> |
|업데이트 된 도메인  <br/> |도메인 업데이트  <br/> |Office 365 조직에서 도메인의 설정이 업데이트 되었습니다.  <br/> |
|확인 된 도메인  <br/> |도메인 확인  <br/> |조직이 도메인의 소유자 인지 확인 했습니다.  <br/> |
|확인 된 전자 메일 확인 도메인  <br/> |전자 메일 확인 도메인 확인  <br/> |전자 메일 확인을 사용 하 여 조직이 도메인의 소유자 인지 확인 합니다.  <br/> |
||||
   
### <a name="ediscovery-activities"></a>eDiscovery 활동
  
office 365 보안 & 준수 센터에서 또는 해당 Windows PowerShell cmdlet을 실행 하 여 수행 되는 콘텐츠 검색 및 eDiscovery 관련 작업은 office 365 감사 로그에 기록 됩니다. 여기에는 다음과 같은 작업이 포함 됩니다.
  
- eDiscovery 사례 만들기 및 관리
    
- 콘텐츠 검색 만들기, 시작 및 편집
    
- 검색 결과 미리 보기, 내보내기, 삭제 등의 콘텐츠 검색 작업 수행
    
- 콘텐츠 검색에 대 한 사용 권한 필터링 구성
    
- eDiscovery 관리자 역할 관리
    
기록 되는 ediscovery 활동에 대 한 자세한 내용 및 설명은 [Office 365 감사 로그에서 ediscovery 활동 검색](search-for-ediscovery-activities-in-the-audit-log.md)을 참조 하세요.
  
> [!NOTE]
> **활동** 드롭다운 목록의 **eDiscovery 활동** 에 나열 된 작업에서 검색 결과에 표시 되는 이벤트가 발생 하는 데 최대 30 분이 걸릴 수 있습니다. 반대로 eDiscovery cmdlet 작업의 해당 이벤트가 검색 결과에 표시 되는 데 최대 24 시간이 걸립니다. 
  
### <a name="power-bi-activities"></a>Power BI 활동
  
Power BI에서 활동에 대 한 감사 로그를 검색할 수 있습니다. power BI 활동에 대 한 자세한 내용은 [조직 내에서 감사 사용](https://docs.microsoft.com/power-bi/service-admin-auditing#activities-audited-by-power-bi)의 "power power bi로 감사 된 작업" 섹션을 참조 하십시오.
  
Power BI에 대 한 감사 로깅은 기본적으로 사용 하지 않도록 설정 되어 있습니다. Office 365 감사 로그에서 power bi 활동을 검색 하려면 power bi 관리 포털에서 감사를 사용 하도록 설정 해야 합니다. 자세한 내용은 [Power BI 관리 포털](https://docs.microsoft.com/power-bi/service-admin-portal#audit-logs)의 "감사 로그" 섹션을 참조 하십시오.
  
### <a name="microsoft-workplace-analytics-activities"></a>Microsoft 작업 공간 분석 활동

회사 분석에서는 Office 365 조직에서 그룹이 공동 작업을 수행 하는 방법에 대 한 통찰력을 제공 합니다. 다음 표에는 작업 공간 분석에서 관리자 역할이 나 분석가 역할이 할당 된 사용자가 수행한 작업이 나와 있습니다. 분석가 역할이 할당 된 사용자는 모든 서비스 기능에 대 한 모든 권한을 가지 며이 제품을 사용 하 여 분석을 수행 합니다. 관리자 역할이 할당 된 사용자는 개인 정보 설정 및 시스템 기본값을 구성할 수 있으며, 작업 공간 분석에서 조직 데이터를 준비, 업로드 및 확인할 수 있습니다. 자세한 내용은 [작업 공간 분석](https://docs.microsoft.com/en-us/workplace-analytics/index-orig)을 참조 하세요.

|**식별 이름**|**Operation**|**설명**|
|:-----|:-----|:-----|
|액세스 한 OData 링크 <br/> |AccessedOdataLink <br/> |분석가가 쿼리에 대 한 OData 링크에 액세스 했습니다.|
|취소 쿼리 <br/> |canceledquery <br/> |분석가가 실행 중인 쿼리를 취소 했습니다.|
|만든 모임 제외 <br/> |MeetingExclusionCreated <br/> |분석가가 새 모임 제외 규칙을 만들었습니다.|
|삭제 된 결과 <br/> |DeletedResult <br/> |분석가가 쿼리 결과를 삭제 했습니다.|
|다운로드 한 보고서 <br/> |DownloadedReport <br/> |분석가가 쿼리 결과 파일을 다운로드 했습니다.|
|실행 쿼리 <br/> |executedquery <br/> |분석가가 쿼리를 실행 했습니다.|
|업데이트 된 데이터 액세스 설정 <br/> |UpdatedDataAccessSetting <br/> |관리자가 데이터 액세스 설정을 업데이트 했습니다.|
|개인 정보 설정 업데이트 <br/> |UpdatedPrivacySetting <br/> |관리자가 업데이트 한 개인 정보 설정 예를 들면 최소 그룹 크기입니다.|
|업로드 된 조직 데이터 <br/> |UploadedOrgData <br/> |관리자가 조직 데이터 파일을 업로드 했습니다.|
|탐색 보기 <br/> |ViewedExplore <br/> |분석가가 하나 이상의 탐색 페이지 탭에서 시각화를 확인 했습니다.|
||||

### <a name="microsoft-teams-activities"></a>Microsoft 팀원 활동
  
다음 표에는 Office 365 감사 로그에 기록 되는 Microsoft 팀의 사용자 및 관리 활동이 나와 있습니다. Microsoft 팀은 Office 365에서 채팅을 중심으로 하는 작업 영역입니다. 팀의 대화, 모임, 파일 및 메모를 한 곳에 모아 둡니다. 도움말 항목에 대 한 자세한 내용 및 링크는 다음 항목을 참조 하십시오.
  
- [Microsoft 팀에 대 한 질문과 대답-관리자 도움말](https://support.office.com/article/05cbe533-2181-4e95-a4b0-52cd7695fafc)
    
- [Microsoft 팀 도움말](https://support.office.com/article/23156c0c-2c6e-49dd-8b7b-7c564b76508c)
    
|**식별 이름**|**Operation**|**설명**|
|:-----|:-----|:-----|
|팀에 추가 된 인공 지능  <br/> |BotAddedToTeam  <br/> |사용자가 팀에 bot을 추가 합니다.  <br/> |
|추가 된 채널  <br/> |channeladded 됨  <br/> |사용자가 팀에 채널을 추가 합니다.  <br/> |
|추가 된 커넥터  <br/> |커넥터 추가 됨  <br/> |사용자가 채널에 커넥터를 추가 합니다.  <br/> |
|팀에 구성원 추가  <br/> |memberadded 됨  <br/> |팀 소유자가 팀에 구성원을 추가 합니다.  <br/> |
|탭 추가 됨  <br/> |tabadded 됨  <br/> |사용자가 채널에 탭을 추가 합니다.  <br/> |
|변경 된 채널 설정  <br/> |channelsettingchanged  <br/> | 다음 활동이 팀 구성원에 의해 수행 되는 경우 channelsettingchanged 작업이 기록 됩니다. 이러한 각 활동에 대해 감사 로그 검색 결과의 **항목** 열에 변경 된 설정 (아래 괄호에 표시 됨)에 대 한 설명이 표시 됩니다.  <br/> <br/>-팀 채널의 이름 ( **채널 이름**)을 변경 합니다.  <br/>  <br/>-팀 채널에 대 한 설명을 변경 합니다 ( **채널 설명**).  <br/> |
|변경 된 조직 설정  <br/> |teamsten앤틸리스 변경  <br/> | 전역 관리자가 Office 365 관리 센터를 사용 하 여 다음 작업을 수행 하면 teamsten앤틸리스 settingchanged 작업이 기록 됩니다. 이러한 활동은 조직 전체의 Microsoft 팀 설정에 영향을 줍니다. 자세한 내용은 [Microsoft 팀의 관리자 설정](https://support.office.com/article/3966a3f5-7e0f-4ea9-a402-41888f455ba2)를 참조 하세요.  <br/>  이러한 각 활동에 대해 감사 로그 검색 결과의 **항목** 열에 변경 된 설정 (아래 괄호에 표시 됨)에 대 한 설명이 표시 됩니다.  <br/><br/>-조직 ( **microsoft 팀**)에 대해 Microsoft 팀을 사용 하거나 사용 하지 않도록 설정 합니다.  <br/><br/>-Microsoft 팀과 비즈니스용 skype 간의 상호 운용성을 사용 하거나 사용 하지 않도록 설정 (비즈니스용 **skype 상호 운용성**)<br/><br/>-Microsoft 팀 클라이언트 ( **조직도 보기**)에서 조직도 보기를 사용 하거나 사용 하지 않도록 설정 합니다.  <br/><br/>-팀 구성원이 개인적인 회의를 예약 하는 기능을 사용 하거나 사용 하지 않도록 설정 합니다 ( **개인 모임 예약**).  <br/><br/>-팀 구성원이 채널 회의를 예약 하는 기능을 사용 하거나 사용 하지 않도록 설정 합니다 ( **채널 회의 일정**).  <br/><br/>-팀 회의에 화상 통화를 사용 하거나 사용 하지 않도록 설정 합니다 ( **Skype 모임을 위한 비디오**).  <br/><br/>-Microsoft 팀 meetups ( **Skype 모임에 대 한 화면 공유**)에서 화면 공유를 사용 하거나 사용 하지 않도록 설정 합니다.  <br/><br/>-팀 대화 ( **애니메이션 이미지**)에 애니메이션 이미지 (Giphys 라고 함)를 추가 하는 기능을 사용 하거나 사용 하지 않도록 설정 합니다.  <br/><br/>-조직에 대 한 콘텐츠 등급 설정 ( **콘텐츠 등급**)을 변경 합니다. 콘텐츠 등급은 대화에 표시할 수 있는 애니메이션 이미지의 형식을 제한 합니다.  <br/><br/>-팀 구성원이 사용자 지정 가능한 이미지를 인터넷에서 팀 대화에 추가 하는 기능을 사용 하거나 사용 하지 않도록 설정 합니다 ( **인터넷에서 맞춤형 이미지**).  <br/><br/>-팀 구성원이 편집 가능한 이미지 (스티커)를 팀 대화 ( **편집 가능한 이미지**)에 추가 하는 기능을 사용 하거나 사용 하지 않도록 설정 합니다.<br/><br/>-팀 구성원이 Microsoft 팀 채팅 및 채널에서 bot을 사용할 수 있는 기능을 사용 하거나 사용 하지 않도록 설정 ( **조직 차원의 인공 지능**)<br/><br/>-Microsoft 팀에 대해 특정 인공 지능을 사용 하도록 설정 합니다. 여기에는 조직이 인공 지능 ( **개별 bot**)을 사용할 때 사용할 수 있는 팀에 해당 하는 t-bot이 포함 되지 않습니다.  <br/><br/>-팀 구성원이 내선 번호 또는 탭 ( **확장명 또는 탭**)을 추가 하는 기능을 사용 하거나 사용 하지 않도록 설정 합니다.  <br/><br/>-Microsoft 팀에 대 한 소유 인공 지능 로드를 사용 하거나 사용 하지 않도록 설정 합니다 ( **인공 지능 로드**).  <br/><br/>-사용자가 Microsoft 팀 채널 ( **채널 전자 메일**)에 전자 메일 메시지를 보내는 기능을 사용 하거나 사용 하지 않도록 설정 합니다.  <br/> |
|팀 구성원의 변경 된 역할  <br/> |MemberRoleChanged  <br/> |팀 소유자가 팀 구성원의 역할을 변경 합니다. 다음 값은 사용자에 게 할당 된 역할 형식을 나타냅니다.  <br/><br/><br/> **1** -소유자 역할을 나타냅니다.<br/>**2** -구성원 역할을 나타냅니다. <br/>**3** -게스트 역할을 나타냅니다. <br/>Members 속성에도 조직의 이름과 구성원의 전자 메일 주소가 포함 됩니다.  <br/> |
|변경 된 팀 설정  <br/> |teamsettingchanged  <br/> | 팀 소유자가 다음 작업을 수행 하면 teamsettingchanged 작업이 기록 됩니다. 이러한 각 활동에 대해 감사 로그 검색 결과의 **항목** 열에 변경 된 설정 (아래 괄호에 표시 됨)에 대 한 설명이 표시 됩니다.  <br/><br/>-팀에 대 한 액세스 유형을 변경 합니다. 팀을 개인 또는 공용으로 설정할 수 있습니다 ( **팀 액세스 유형**). 팀이 비공개 인 경우 (기본 설정) 사용자는 초대를 통해서만 팀에 액세스할 수 있습니다. 공용 상태인 팀은 누구나 검색할 수 있습니다.  <br/><br/>-팀의 정보 분류 ( **팀 분류**)를 변경 합니다.  <br/>  예를 들어 팀 데이터는 높은 비즈니스 영향, 중간 규모 비즈니스 영향 또는 낮은 비즈니스 영향으로 분류 될 수 있습니다.<br/><br/>-팀 이름 ( **팀 이름**)을 변경 합니다.  <br/><br/>-팀 설명 ( **팀 설명**)을 변경 합니다. <br/><br/>-팀 설정에 대 한 변경 내용 팀 소유자는 팀을 마우스 오른쪽 단추로 클릭 하 고 **팀 관리**를 클릭 한 다음 **설정** 탭을 클릭 하 여 팀 클라이언트에서 이러한 설정에 액세스할 수 있습니다. 이러한 작업의 경우 변경 된 설정의 이름은 감사 로그 검색 결과의 **항목** 열에 표시 됩니다.  <br/> |
|만든 팀  <br/> |teamcreated  <br/> |사용자가 새 팀을 만듭니다.  <br/> |
|삭제 된 채널  <br/> |channeldeleted  <br/> |사용자가 팀에서 채널을 삭제 합니다.  <br/> |
|삭제 된 팀  <br/> |teamdeleted  <br/> |팀 소유자가 팀을 삭제 합니다.  <br/> |
|팀에서 제거 된 인공 지능  <br/> |BotRemovedFromTeam  <br/> |사용자가 팀에서 bot을 제거 합니다.  <br/> |
|제거 된 커넥터  <br/> |커넥터 제거 됨  <br/> |사용자가 채널에서 커넥터를 제거 합니다.  <br/> |
|팀에서 구성원을 제거 했습니다.  <br/> |memberremoved 됨  <br/> |팀 소유자가 팀에서 구성원을 제거 합니다.  <br/> |
|제거 된 탭  <br/> |tabremoved 됨  <br/> |사용자가 채널에서 탭을 제거 합니다.  <br/> |
|업데이트 된 커넥터  <br/> |커넥터 업데이트  <br/> |사용자가 채널에서 커넥터를 수정 했습니다.  <br/> |
|업데이트 된 탭  <br/> |tabupdated  <br/> |사용자가 채널에서 탭을 수정 했습니다.  <br/> |
|팀에 로그인 한 사용자  <br/> |teamssessionstarted  <br/> |사용자가 Microsoft 팀 클라이언트에 로그인 합니다.  <br/> |
||||

### <a name="yammer-activities"></a>Yammer 활동
  
다음 표에는 Office 365 감사 로그에 기록 된 Yammer의 사용자 및 관리 활동이 나와 있습니다. Office 365 감사 로그에서 Yammer 관련 활동을 반환 하려면 **활동** 목록에서 **모든 활동에 대 한 결과 표시** 를 선택 해야 합니다. 날짜 범위 상자와 **사용자** 목록을 사용 하 여 검색 결과의 범위를 좁힐 수 있습니다. 
  
|**식별 이름**|**Operation**|**설명**|
|:-----|:-----|:-----|
|변경 된 데이터 보존 정책  <br/> |소프트 deletesetting날짜  <br/> |관리자가 네트워크 데이터 보존 정책에 대 한 설정을 하드 삭제 또는 일시 삭제 중 하나로 업데이트 하는지 확인 했습니다. 확인 된 관리자만이 작업을 수행할 수 있습니다.  <br/> |
|변경 된 네트워크 구성  <br/> |networkconfigurationupdated 됨  <br/> |네트워크 또는 확인 된 관리자가 Yammer 네트워크의 구성을 변경 합니다. 여기에는 데이터를 내보내고 채팅을 사용 하기 위한 간격 설정이 포함 됩니다.  <br/> |
|네트워크 프로필 설정 변경  <br/> |processprofilefields  <br/> |네트워크 또는 확인 된 관리자 변경 네트워크 사용자 네트워크의 구성원 프로필에 표시 되는 정보입니다.  <br/> |
|변경 된 개인 콘텐츠 모드  <br/> |SupervisorAdminToggled  <br/> |관리자가 *비공개 콘텐츠 모드* 를 설정 또는 해제 하는지 확인 했습니다. 이 모드를 사용 하면 관리 보기가 개인 그룹에 게시 되 고 개별 사용자 또는 사용자 그룹 간의 개인 메시지를 볼 수 있습니다. 확인 된 관리자만이 작업을 수행할 수 있습니다.  <br/> |
|보안 구성 변경  <br/> |networksecurityconfigurationupdated 됨  <br/> |관리자가 Yammer 네트워크의 보안 구성을 확인 했습니다. 여기에는 IP 주소에 대 한 암호 만료 정책 및 제한 설정이 포함 됩니다. 확인 된 관리자만이 작업을 수행할 수 있습니다.  <br/> |
|만든 파일  <br/> |FileCreated  <br/> |사용자가 파일을 업로드 합니다.  <br/> |
|만든 그룹  <br/> |groupcreation  <br/> |사용자가 새 그룹을 만듭니다.  <br/> |
|삭제 된 그룹  <br/> |groupdeletion  <br/> |Yammer에서 그룹이 삭제 됩니다.  <br/> |
|삭제 된 메시지  <br/> |messagedeleted  <br/> |사용자가 메시지를 삭제 합니다.  <br/> |
|다운로드 한 파일  <br/> |파일 다운로드 됨  <br/> |사용자가 파일을 다운로드 합니다.  <br/> |
|내보낸 데이터  <br/> |dataexport  <br/> |관리자가 Yammer 네트워크 데이터를 내보내도록 확인 합니다. 확인 된 관리자만이 작업을 수행할 수 있습니다.  <br/> |
|공유 파일  <br/> |FileShared  <br/> |사용자가 다른 사용자와 파일을 공유 합니다.  <br/> |
|일시 중단 된 네트워크 사용자  <br/> |networkusersuspended  <br/> |네트워크 또는 관리자가 Yammer에서 사용자를 일시 중단 (비활성화) 합니다.  <br/> |
|일시 중단 된 사용자  <br/> |usersuspension 중단  <br/> |사용자 계정이 일시 중단 (비활성화 됨) 됩니다.  <br/> |
|업데이트 된 파일 설명  <br/> |fileupdatedescription  <br/> |사용자가 파일에 대 한 설명을 변경 합니다.  <br/> |
|업데이트 된 파일 이름  <br/> |fileupdatename  <br/> |사용자가 파일의 이름을 변경 합니다.  <br/> |
|표시 한 파일  <br/> |열어 본 파일  <br/> |사용자가 파일을 볼 수 있습니다.  <br/> |
||||
   
### <a name="microsoft-flow-activities"></a>Microsoft Flow 활동

Microsoft Flow에서 활동에 대 한 감사 로그를 검색할 수 있습니다. 이러한 작업에는 흐름 만들기, 편집 및 삭제, 흐름 권한 변경 등이 있습니다. 유동 활동을 감사 하는 방법에 대 한 자세한 내용은 [현재 Office 365 Security & 준수 센터에서 사용할 수 있는 블로그 Microsoft Flow 감사 이벤트](https://flow.microsoft.com/blog/security-and-compliance-center)를 참조 하십시오.

### <a name="microsoft-powerapps"></a>Microsoft PowerApps

PowerApps에서 앱 관련 작업에 대 한 감사 로그를 검색할 수 있습니다. 이러한 활동에는 앱 만들기, 시작 및 게시가 포함 됩니다. 앱에 사용 권한을 할당 하는 것도 감사 됩니다. 모든 powerapps 활동에 대 한 설명은 [powerapps에 대 한 활동 로깅을](https://docs.microsoft.com/en-us/power-platform/admin/logging-powerapps#what-events-are-audited)참조 하십시오.

### <a name="microsoft-stream-activities"></a>Microsoft Stream 작업
  
Microsoft Stream에서 작업에 대 한 감사 로그를 검색할 수 있습니다. 이러한 작업에는 사용자 관리, 그룹 채널 작업 및 관리 작업 (예: 사용자 관리자, 조직 설정 관리, 보고서 내보내기 등)에 의해 수행 되는 비디오 작업이 포함 됩니다. 이러한 작업에 대 한 자세한 내용은 [microsoft stream의 감사 로그](https://docs.microsoft.com/stream/audit-logs)에서 "microsoft stream에 기록 된 활동" 섹션을 참조 하십시오.

### <a name="exchange-admin-audit-log"></a>Exchange 관리자 감사 로그
  
office 365에서 기본적으로 사용 되는 Exchange 관리자 감사 로깅은 관리자 또는 관리 권한이 할당 된 사용자가 exchange Online 조직을 변경할 때 office 365 감사 로그에 이벤트를 기록 합니다. exchange 관리 센터를 사용 하거나 Windows PowerShell에서 cmdlet을 실행 하 여 변경한 내용은 exchange 관리자 감사 로그에 기록 됩니다. Exchange의 관리자 감사 로깅에 대 한 자세한 내용은 [관리자 감사 로깅을](https://go.microsoft.com/fwlink/p/?LinkID=619225)참조 하십시오.
  
다음은 Exchange 관리자 감사 로그에서 활동을 검색 하는 데 도움이 되는 몇 가지 팁입니다.
  
- Exchange 관리자 감사 로그의 항목을 반환 하려면 **활동** 목록에서 **모든 활동에 대 한 결과 표시** 를 선택 해야 합니다. 날짜 범위 상자와 **사용자** 목록을 사용 하 여 특정 날짜 범위 내에서 특정 Exchange 관리자가 실행 한 cmdlet에 대 한 검색 결과의 범위를 좁힐 수 있습니다. 
    
- Exchange 관리자 감사 로그의 이벤트를 표시 하려면 검색 결과를 필터링 하 고 **활동** 필터 **-** 상자에 대시 (-)를 입력 합니다. 이렇게 하면 Exchange 관리 이벤트에 대 한 **활동** 열에 표시 되는 cmdlet 이름이 표시 됩니다. 그런 다음 cmdlet 이름을 알파벳 순으로 정렬할 수 있습니다. 
    
    ![작업 상자에 대시를 입력 하 여 Exchange 관리 이벤트를 필터링 합니다.](media/7628e7aa-6263-474a-a28b-2dcf5694bb27.png)
  
- 실행 된 cmdlet, 사용 된 매개 변수 및 매개 변수 값, 영향을 받은 개체에 대 한 정보를 얻으려면 검색 결과를 내보내고 **모든 결과 다운로드** 옵션을 선택 해야 합니다. 
    
- exchange 관리 센터를 사용 하 여 exchange 관리자 감사 로그에서 이벤트를 볼 수도 있습니다. 자세한 내용은 [관리자 감사 로그 보기](https://technet.microsoft.com/library/dn342832%28v=exchg.150%29.aspx)를 참조 하십시오.
  
## <a name="frequently-asked-questions"></a>자주하는 질문

**Office 365에서 감사 서비스가 제공 하는 기능에 대 한 자세한 내용은 어디에서 찾을 수 있나요?**

office 365에서 사용할 수 있는 감사 및 보고 기능에 대 한 자세한 내용은 [office 365에서 감사 및 보고](office-365-auditing-and-reporting-overview.md)를 참조 하세요. 

**현재 감사 되는 다른 Office 365 서비스는 무엇 인가요?**

Exchange Online, SharePoint, OneDrive, Azure Active Directory, Microsoft 팀, CRM, Advanced Threat Protection 및 데이터 손실 방지와 같은 가장 많이 사용 되는 Office 365 서비스를 감사 합니다. 전체 목록은이 문서의 [소개](#search-the-audit-log-in-the-office-365-security-amp-compliance-center) 섹션을 참조 하십시오.

**Office 365의 감사 서비스에서 감사 하는 활동은 무엇입니까?**

Office 365에서 감사 되는 작업에 대 한 설명은이 문서의 [감사 된 작업](#audited-activities) 섹션을 참조 하십시오.

**이벤트가 발생 한 후에 감사 레코드를 사용할 수 있도록 하는 데 소요 되는 시간**

대부분의 감사 데이터는 30 분 내에 사용할 수 있지만 해당 감사 로그 항목이 검색 결과에 표시 될 때까지 이벤트가 발생 한 후 최대 24 시간이 걸릴 수 있습니다. 이 문서의 [시작 하기 전에](#before-you-begin) 섹션에 나와 있는 표를 참조 하 여 다양 한 Office 365 서비스의 이벤트에 소요 되는 시간을 보여 줍니다.

**감사 레코드가 보존 되는 기간**

앞에서 설명한 것 처럼 감사 레코드의 보존 기간은 조직의 Office 365 구독에 따라 달라 집니다.  

- **Office 365 E3** -감사 레코드는 90 일 동안 보존 됩니다.

- **Office 365 E5** -감사 레코드는 365 일 (1 년) 동안 보존 됩니다. 1 년 동안 감사 레코드 보존은 E3 구독 및 Office 365 고급 준수 추가 기능 구독이 있는 조직 에서도 사용할 수 있습니다.

     > [!NOTE]
     > 앞에서 설명한 것 처럼, E5 조직 (또는 고급 준수 추가 기능 라이선스가 있는 E3 조직)에 대 한 감사 기록의 1 년 보존 기간은 현재 전용 미리 보기 프로그램의 일부로만 사용할 수 있습니다. 이 미리 보기 프로그램에 등록 하려면 [Microsoft 지원 서비스](https://docs.microsoft.com/en-us/office365/admin/contact-support-for-business-products?redirectSourcePath=%252fen-us%252farticle%252fcontact-support-for-business-products-admin-help-32a17ca7-6fa0-4870-8a8d-e25ba4ccfd4b&view=o365-worldwide&tabs=online) 에 대 한 요청을 실행 하 여 도움이 필요한 항목에 대 한 설명을 "장기적인 Office 365 audit log 비공개 preview"로 포함 하십시오.

또한 감사 레코드의 보존 기간 기간은 사용자별 라이선스를 기반으로 합니다. 예를 들어 조직의 사용자에 게 Office 365 E3 라이선스를 할당 한 경우 해당 사용자가 수행한 활동에 대 한 감사 레코드는 90 일 동안 보존 됩니다. 다른 사용자에 게 Office 365 E5 라이선스가 할당 되 면 1 년 동안 감사 레코드가 보존 됩니다. 

**감사 데이터에 프로그래밍 방식으로 액세스할 수 있습니까?**

예. Office 365 관리 활동 API는 감사 로그를 프로그래밍 방식으로 페치하는 데 사용 됩니다.  시작 하려면 [Office 365 관리 api 시작](https://docs.microsoft.com/office/office-365-management-api/get-started-with-office-365-management-apis)을 참조 하세요.

**office 365 Security & 준수 센터 또는 office 365 관리 활동 API를 사용할 때를 제외 하 고 감사 로그를 가져오는 다른 방법이 있나요?**

아니요. 다음 두 가지 방법으로 Office 365 감사 서비스에서 데이터를 가져올 수 있습니다. 

**감사 로그를 캡처할 각 서비스에서 개별적으로 감사를 사용 하도록 설정 해야 하나요?**

대부분의 office 365 서비스에서는이 문서의 [시작 하기 전에](#before-you-begin) 섹션에 설명 된 대로 office 365 조 직에 대 한 감사를 처음 설정한 후에 기본적으로 감사가 사용 되도록 설정 됩니다. 그러나 감사 하려는 각 사서함에 대해 Exchange Online에서 사서함 감사를 사용 하도록 설정 해야 합니다.   Office 365 조직의 모든 사서함에 대해 기본적으로 사서함 감사를 사용 하도록 설정 하는 작업을 수행 하 고 있습니다. 자세한 내용은 [Microsoft 보안, 개인 정보 보호 및 준수 블로그에서](https://techcommunity.microsoft.com/t5/Security-Privacy-and-Compliance/Exchange-Mailbox-Auditing-will-be-enabled-by-default/ba-p/215171)"기본적으로 Exchange 사서함 감사를 사용 하도록 설정 합니다."를 참조 하세요.

**Office 365 감사 서비스가 레코드의 중복 제거를 지원 합니까?**

아니요. 감사 서비스 파이프라인은 실시간에 거의 도달 하므로 중복 제거를 지원할 수 없습니다.
 
**Office 365에서 여러 지역 간의 데이터 흐름을 감사 하나요?**

아니요. 현재는 NA (북미), EMEA (유럽, 중동 및 아프리카) 및 apac (아시아 태평양) 지역에서 감사 파이프라인 배포가 진행 되 고 있습니다. 그러나 microsoft는 이러한 지역에서 부하 분산을 위해 그리고 live 사이트 문제 중에만 데이터를 전달할 수 있습니다. 이러한 활동을 수행 하면 전송 중인 데이터가 암호화 됩니다.   
 
**암호화 데이터를 감사 합니까?**

감사 데이터는 감사 파이프라인이 배포 된 동일한 지역에서 Exchange 사서함 (휴지 위치에 있는 데이터)에 저장 됩니다. 이 데이터는 암호화 되지 않습니다. 그러나 전송 중인 데이터는 항상 암호화 됩니다. 












