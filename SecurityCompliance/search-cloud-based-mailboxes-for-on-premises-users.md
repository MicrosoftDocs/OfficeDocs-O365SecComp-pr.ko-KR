---
title: Office 365의 온-프레미스 사용자를 위한 클라우드 기반 사서함 검색
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 6/4/2018
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MST160
- MET150
ms.assetid: 3f7dde1a-a8ea-4366-86da-8ee6777f357c
description: 콘텐츠 검색 도구를 사용 하 여 Office 365 보안에서 &amp; 준수 센터를 검색 하 고 Exchange 하이브리드 배포에서 온-프레미스 사용자를 위한 (1xN 채팅 라고 함) MicrosoftTeams 채팅 데이터를 내보냅니다.
ms.openlocfilehash: a504dfcf4c82bec036137b90312c01a0b2326ccc
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22533307"
---
# <a name="searching-cloud-based-mailboxes-for-on-premises-users-in-office-365"></a>Office 365의 온-프레미스 사용자를 위한 클라우드 기반 사서함 검색

조직에 Exchange 하이브리드 배포 팀이 Microsoft 사용 하도록 설정한 경우 사용자가 인스턴트 메시징에 대 한 팀 채팅 응용 프로그램을 사용할 수 있습니다. 클라우드 기반 사용자에 대 한 팀 채팅 데이터 (1xN 채팅 라고도 함)가 기본 클라우드 기반 사서함에 저장 됩니다. 온-프레미스 사용자를 팀 채팅 응용 프로그램을 사용 하는 경우 기본 사서함이 있는 온-프레미스 합니다. 이 제한을 해결 하려면 Microsoft 온-프레미스 사용자에 대 한 팀 채팅 데이터를 저장 하는 클라우드 기반 저장소 영역 (온-프레미스 사용자를 위한 클라우드 기반 사서함 라고 함) 만들어진 새 기능을 출시 했습니다. 이렇게 하면 콘텐츠 검색 도구를 사용 하 여 Office 365 보안에서 &amp; 팀은 온-프레미스 사용자에 대 한 채팅 데이터를 검색 하 고 내보내기 준수 센터입니다. 
  
요구 사항 및를 설정 하 고 설정 및 온-프레미스 사용자를 위한 클라우드 기반 사서함을 검색에 대 한 제한은 다음과 같습니다.
  
- 사용자 계정 (예: Active Directory)에서 온-프레미스 디렉터리 서비스에서 Azure Active Directory를 Office 365의 디렉터리 서비스와 동기화 되어야 합니다. 즉, 메일 사용자 계정을 Office 365에서 만든 및 온-프레미스 조직에서 기본 사서함이 있는 사용자와 연결 됩니다.
    
- 온-프레미스 사용자를 위한 클라우드 기반 사서함만 저장소를 사용 하는 팀이 채팅 데이터를입니다. 온-프레미스 사용자는 클라우드 기반 사서함에 로그인 하거나 어떤 식으로도 액세스할 수 없습니다. 전자 메일 메시지를 주고받을를 사용할 수 없습니다. 
    
- 조직에서 온-프레미스 사용자를 위한 클라우드 기반 사서함 채팅 데이터를 팀에 대 한 검색을 사용 하도록 설정 하려면 Microsoft 기술 지원 서비스에 요청을 제출 해야 합니다. 참조 [보안에서이 기능을 사용 하려면 Microsoft 기술 지원 서비스 요청을 채우고 &amp; 준수 센터](#filing-a-request-with-microsoft-support-to-enable-this-feature-in-the-security-amp-compliance-center) 이 문서의 합니다. 
    
 **참고:** 팀이 채널 대화는 항상 팀과 관련 된 클라우드 기반 사서함에 저장 됩니다. 즉, 대화 하지 않고 지원 요청을 파일에 있는 검색 채널에 콘텐츠 검색을 사용할 수 있습니다. 팀을 검색 하는 방법에 대 한 자세한 내용은 채널 대화 하 고 [Microsoft 팀의 검색 및 Office 365 그룹을](content-search.md#searching-microsoft-teams-and-office-365-groups)참조 하십시오.
  
## <a name="how-it-works"></a>작업 방법

Microsoft 팀이 사용이 가능한 사용자가 온-프레미스 사서함이 있는 경우 해당 사용자 계정 id를 클라우드로 동기화 된가 Microsoft 1xN 팀 채팅 데이터를 저장 하는 클라우드 기반 사서함을 만듭니다. 팀이 채팅 데이터는 클라우드 기반 사서함에 저장 된, 후 검색을 위해 인덱싱되는 합니다. 이렇게 하면 사용 하 여 콘텐츠 검색 (및 eDiscovery 사례와 연결 된 검색)를 검색 하려면 미리 보기, 및 온-프레미스 사용자에 대 한 팀 채팅 데이터를 내보냅니다. 사용할 수도 있습니다 ** \*ComplianceSearch** cmdlet에서 Office 365 보안 &amp; 준수 센터 PowerShell 팀에 대 한 온-프레미스 사용자에 대 한 채팅 데이터를 검색 합니다. 
  
다음 그림에서는 팀에서 온-프레미스 사용자에 대 한 데이터를 채팅 하는 방법의 워크플로가 검색 미리 보기, 가져오기 및 내보내기를 사용할 수 있는 보여줍니다.
  
![Microsoft 팀의 온-프레미스 사용자를 위한 클라우드 기반 저장소](media/895845f8-2ceb-47ed-96c9-5ab7f1aea916.png)
  
이 새로운 기능 외에도 계속 사용할 수 있습니다 콘텐츠 검색 검색 미리 보기, 가져오기 및 내보내기, 팀이 채팅 데이터에 대 한 Exchange Online 사서함에 있는 각 Microsoft 팀 및 팀이 1xN와 관련 된 클라우드 기반 SharePoint 사이트와 Exchange 사서함의 콘텐츠를 클라우드 기반 사용자입니다.

## <a name="filing-a-request-with-microsoft-support-to-enable-this-feature-in-the-security-amp-compliance-center"></a>보안에서이 기능을 사용 하려면 Microsoft 기술 지원 서비스 요청을 채우고 &amp; 준수 센터

보안에서 그래픽 사용자 인터페이스를 사용 하 여 조직에 사용 하도록 설정 하려면 Microsoft 기술 지원 서비스 요청을 파일 해야 &amp; 준수 센터 온-프레미스 사용자를 위한 클라우드 기반 사서함에서 채팅 데이터를 팀에 대 한 검색 합니다. 이 기능은 Office 365 보안에서 사용할 수는 &amp; 준수 센터 PowerShell 합니다. 온-프레미스 사용자에 대 한 팀 채팅 데이터를 검색 하려면 PowerShell을 사용 하 여 지원 요청을 제출 필요가 없습니다. 
  
Microsoft 기술 지원 서비스에 요청을 제출 하는 경우 다음 정보를 포함 합니다.
  
- Office 365 조직의 기본 도메인 이름입니다.
    
- 테 넌 트 이름과 하 여 Office 365 조직의 테 넌 트 ID입니다. Azure Active Directory 포털에 따라이 찾을 수 있습니다 ( **관리** 에서 \> **속성**). [사용자의 Office 365 테 넌 트 ID를 찾을](https://support.office.com/article/6891b561-a52d-4ade-9f39-b492285e2c9b)참조 하십시오.
    
- 다음 제목 또는 지원 요청의 용도 설명: "온-프레미스 사용자에 대 한 콘텐츠 검색 응용 프로그램"를 사용 하도록 설정 합니다. 이렇게 하면 요청을 구현 하 게 수행 하는 Office 365 eDiscovery 엔지니어링 팀에 요청을 라우팅할 하는 데 도움이 됩니다. 
    
문서를 엔지니어링 변경 후 예상된 배포 날짜 Microsoft 기술 지원 서비스에 전송 됩니다. 참고 배포 프로세스에 일반적으로 지원 요청을 제출한 후 2-3 주 걸립니다. 
  
### <a name="what-happens-after-this-feature-is-enabled"></a>이 기능을 활성화 한 후 어떻게 해야 할까요?

다음과 같이 변경 콘텐츠 검색에서 적용 되 면 및 연관 된 eDiscovery 검색에는 보안의 경우이 기능이 Office 365 조직에 배포 된 후 &amp; 준수 센터:
  
- 콘텐츠 검색의 **위치** 에서 **온-프레미스 사용자에 대 한 추가 Office 응용 프로그램 콘텐츠** 확인란 추가 됩니다. 
    
    !["온-프레미스 사용자를 위한 Office 응용 프로그램 콘텐츠 추가" 확인란 콘텐츠 검색 UI에 추가 됩니다.](media/599e751e-17bd-408d-a18c-127538de6e85.png)
  
- 온-프레미스 사용자를 검색 하려면 사용자 사서함을 선택 하는데 사용 하 여 콘텐츠 위치 선택에 표시 됩니다. 
    

  
## <a name="searching-for-teams-chat-content-in-cloud-based-mailboxes-for-on-premises-users"></a>온-프레미스 사용자를 위한 클라우드 기반 사서함의 콘텐츠 팀 채팅에 대 한 검색

기능이 활성화 된 후 보안에서 콘텐츠 검색을 사용할 수 있습니다 &amp; 준수 센터 온-프레미스 사용자를 위한 클라우드 기반 사서함에서 채팅 데이터를 팀에 대 한 검색 합니다. 
  
1. 보안에서 &amp; 준수 센터, 이동 **검색 &amp; 조사** \> **콘텐츠 검색**
    
2. **검색** 페이지를 클릭 ![추가 아이콘](media/8ee52980-254b-440b-99a2-18d068de62d3.gif) **새 검색**합니다.
    
    앞에서 설명한 것 처럼 **온-프레미스 사용자에 대 한 추가 Office 응용 프로그램 콘텐츠** checkbox **위치**아래 표시 됩니다. 참고 기본적으로 선택 합니다.
    
3. 키워드 쿼리를 작성 하 고 필요한 경우 검색 쿼리를 조건을 추가 합니다. 팀에 대 한 검색만 채팅 데이터, **키워드** 상자에 다음 쿼리를 추가할 수 있습니다. 
    
    ```
    kind:im
    ``` 

4. 이 시점 **위치**에서 다음 옵션 중 하나를 선택할 수 있습니다.
    
    - **모든 위치** -조직에서 모든 사용자의 사서함을 검색 하려면이 옵션을 선택 합니다. 확인란을 선택 하는 경우에 온-프레미스 사용자에 대 한 모든 클라우드 기반 사서함 검색 됩니다. 
    
    - **특정 위치** -이 옵션을 선택 하 고 한 다음 **수정** 을 클릭 \> 사용자, 그룹 또는 팀이 특정 사서함을 검색할 수를 선택 합니다. 앞에서 설명한 것 처럼 위치 선택 하면 온-프레미스 사용자를 검색 합니다. 
    
5. 저장 하 고 검색을 실행 합니다. 온-프레미스 사용자를 위한 클라우드 기반 사서함에서 검색 결과가 다른 검색 결과 같은 미리볼 수 있습니다. 또한 수 있습니다 (모든 팀 채팅 데이터를 포함 하 여) 검색 결과 PST 파일로 내보낼 수 있습니다. 자세한 내용은 다음을 참조 합니다. 
    
    - [새 검색 만들기](content-search.md#create-a-new-search)
    
    - [검색 결과 미리 보기](content-search.md#preview-search-results)
    
    - [Office 365 보안에서 콘텐츠 검색 결과 내보낼 &amp; 준수 센터](export-search-results.md)
    
## <a name="using-powershell-to-search-for-teams-chat-data-in-cloud-based-mailboxes-for-on-premises-users"></a>PowerShell을 사용 하 여 온-프레미스 사용자를 위한 클라우드 기반 사서함에서 채팅 데이터를 팀에 대 한 검색

Office 365 보안에서 **새로 만들기 ComplianceSearch** 및 **집합 ComplianceSearch** cmdlet을 사용 하면 &amp; 준수 센터 PowerShell 온-프레미스 사용자를 위한 클라우드 기반 사서함을 검색 합니다. 앞에서 설명한 것 처럼 온-프레미스 사용자에 대 한 팀 채팅 데이터를 검색 하려면 PowerShell을 사용 하 여 지원 요청을 제출 필요가 없습니다. 
  
1. [Office 365 보안 연결할 &amp; 준수 센터 PowerShell](https://docs.microsoft.com/powershell/exchange/office-365-scc/connect-to-scc-powershell/connect-to-scc-powershell)합니다.
    
2. 새 콘텐츠를 만들기 위해 명령을 다음 PowerShell 실행 온-프레미스 사용자의 클라우드 기반 사서함을 검색 합니다.
    
    ```
    New-ComplianceSearch <name of new search> -ContentMatchQuery <search query> -ExchangeLocation <on-premises user> -IncludeUserAppContent $true -AllowNotFoundExchangeLocationsEnabled $true  
    ```
   
    *IncludeUserAppContent* 매개 변수는 사용자 또는 *ExchangeLocation* 매개 변수에 의해 지정 된 사용자에 대 한 클라우드 기반 사서함을 지정 하는데 사용 됩니다. *AllowNotFoundExchangeLocationsEnabled* 온-프레미스 사용자를 위한 클라우드 기반 사서함을 허용합니다. 사용 하는 경우는 `$true` 값이 매개이 변수는 검색에 대 한 사서함의 존재 여부를 실행 하기 전에 유효성을 검사 하려고 하지 않습니다. 이러한 유형의 사서함 일반 사서함으로 해결 되지 않으면 하기 때문에 온-프레미스 사용자를 위한 클라우드 기반 사서함을 검색 하는 데 필요한입니다. 
    
    다음 예제에서는 팀에 대 한 키워드 "redstone" 클라우드 기반 사서함에 Contoso 조직에서 온-프레미스 사용자가이 Sara Davis의 포함 된 (인스턴트 메시지 인) 채팅을 검색 합니다.
  
    ```
    New-ComplianceSearch "Redstone_Search" -ContentMatchQuery "redstone AND kind:im" -ExchangeLocation sarad@contoso.com -IncludeUserAppContent $true -AllowNotFoundExchangeLocationsEnabled $true  
    ```

   새 검색을 만든 후에 **시작 ComplianceSearch** cmdlet을 사용 하 여 검색을 실행 해야 합니다. 
  
이러한 cmdlet을 사용 하 여 자세한 정보를 참조 하십시오.
  
- [New-ComplianceSearch](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-content-search/new-compliancesearch)
    
- [Set-ComplianceSearch](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-content-search/set-compliancesearch)
    
- [Start-ComplianceSearch](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-content-search/start-compliancesearch)
    

## <a name="known-issues"></a>알려진 문제

- 현재, 검색, 미리 보기 및 클라우드 기반 사서함에 대 한 콘텐츠 내보내기 온-프레미스 사용자만 수 있습니다. EDiscovery와 관련 된 보류의 온-프레미스 사용자에 대 한 클라우드 기반 사서함을 배치 케이스 또는 Office 365 보존 정책에 할당 하는 방법 지원 되지 않습니다. 
    
- Ediscovery 콘텐츠 위치 선택 표시 온-프레미스 사용자를 보유 하 고을 선택할 수 있습니다. 그러나 앞부분에 설명 된 보류 온-프레미스 사용자에 게 적용 되지 않습니다.
    
## <a name="frequently-asked-questions"></a>질문과 대답

 **온-프레미스 사용자를 위한 클라우드 기반 사서함은 어디에 있습니까?**
  
클라우드 기반 사서함 만들고 Office 365 조직 동일한 데이터 센터에 저장 됩니다. 
  
 **지원 요청을 제출 이외의 다른 요구 사항이 있습니까?**
  
 Office 365의 각 온-프레미스 사용자 계정에 대 한 해당 메일 사용자 계정이 만들어질 수 있도록 prem에 사서함이 있는 사용자의 id 앞에서 설명한 것 처럼 클라우드 기반 조직에 동기화 해야 합니다. 또한 조직에 Office 365 Enterprise E1, E3 또는 e 5 구독 등 Office 365 enterprise 구독에 있어야 합니다. 
  
 **이 사용자의 온-프레미스 사서함을 클라우드로 마이그레이션한 경우 팀 채팅 데이터 손실 될 위험이 있습니까?**
  
아니요. 온-프레미스 사용자의 기본 사서함 클라우드로 마이그레이션할 때 새 클라우드 기반 기본 사서함에 해당 사용자에 대 한 팀 채팅 데이터를 마이그레이션합니다.
  
 **EDiscovery 보류 또는 Office 365 보존 정책을 온-프레미스 사용자에 게 적용할 수 있습니까?**
  
아니요.
  
 **오래 된 팀 채팅 온-프레미스 사용자에 대 한 시간 전에 내 조직 콘텐츠 검색 찾기가이 기능을 사용 하도록 요청 제출 된 수 있습니까?**
  
Microsoft은 2018 년 1 월 31에서 온-프레미스 사용자에 대 한 팀 채팅 데이터를 저장 하기 시작 합니다. 따라서이 날짜 이후 Active Directory와 Azure Active Directory 간의 온-프레미스 팀이 사용자의 id를 동기화 된가, 하는 경우 다음 자신의 팀이 채팅 데이터 클라우드 기반 사서함에 저장 됩니다 및 콘텐츠 검색을 사용 하 여 검색할 수 있습니다. Microsoft는 또한 온-프레미스 사용자를 위한 클라우드 기반 사서함에서 2018 년 1 월 31, 하기 전에 팀 채팅 데이터를 저장 (영문). 이 대 한 자세한 내용은 곧 제공 됩니다.
