---
title: 콘텐츠 검색에 대한 권한 필터링 구성
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
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
ms.assetid: 1adffc35-38e5-4f7d-8495-8e0e8721f377
description: 콘텐츠 검색 권한 필터링을 사용 하 여 eDiscovery 관리자가 Office 365 조직에서 사서함 및 사이트의 하위 집합만 검색 하도록 합니다.
ms.openlocfilehash: 0c0f94827576fc1a022b2a9e2735f667295b624e
ms.sourcegitcommit: a5a7e43822336ed18d8f5879167766686cf6b2a3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2019
ms.locfileid: "36478167"
---
# <a name="configure-permissions-filtering-for-content-search"></a>콘텐츠 검색에 대한 권한 필터링 구성

검색 권한 필터링을 사용 하 여 eDiscovery 관리자가 Office 365 조직에서 사서함과 사이트의 하위 집합만 검색 하도록 할 수 있습니다. 또한 권한 필터링을 사용하여 동일한 eDiscovery 관리자가 특정 검색 조건을 충족하는 사서함 또는 사이트 콘텐츠만 검색하도록 할 수도 있습니다. 예를 들어 검색 관리자가 특정 위치나 부서의 사용자 사서함만 검색하도록 할 수 있습니다. 지원 되는 받는 사람 필터를 사용 하 여 특정 사용자 또는 사용자 그룹이 검색할 수 있는 사서함을 제한 하는 필터를 만들어이 작업을 수행 합니다. 검색할 수 있는 사서함 콘텐츠를 지정하는 필터를 만들 수도 있습니다. 이 작업은 검색 가능한 메시지 속성을 사용하는 필터를 만들어 수행합니다. 마찬가지로, eDiscovery 관리자가 조직의 특정 SharePoint 사이트만 검색 하도록 할 수 있습니다. 이 작업은 검색할 수 있는 사이트를 제한하는 필터를 만들어 수행합니다. 검색할 수 있는 사이트 콘텐츠를 지정하는 필터를 만들 수도 있습니다. 이 작업은 검색 가능한 사이트 속성을 사용하는 필터를 만들어 수행합니다.

또한 검색 권한 필터링을 사용 하 여 사서함, SharePoint 사이트, OneDrive 계정 등의 사용자 콘텐츠 위치를 제어 하는 Office 365 조직 내에서 *준수 경계*라고 하는 논리적 경계를 만들 수 있습니다. 특정 eDiscovery 관리자가 검색할 수 있습니다. 자세한 내용은 [Office 365에서 eDiscovery 조사에 대 한 준수 경계 설정을](set-up-compliance-boundaries.md)참조 하세요.
  
검색 권한 필터링은 보안 & 준수 센터의 콘텐츠 검색 기능을 통해 지원 됩니다. 다음 4 개의 cmdlet을 사용 하 여 검색 권한 필터를 구성 하 고 관리할 수 있습니다.
  
[New-compliancesecurityfilter](#new-compliancesecurityfilter)

[New-compliancesecurityfilter](#get-compliancesecurityfilter)

[New-compliancesecurityfilter](#set-compliancesecurityfilter)

[New-compliancesecurityfilter을 제거 합니다.](#remove-compliancesecurityfilter)

## <a name="before-you-begin"></a>시작하기 전에

- 준수 보안 필터 cmdlet을 실행 하려면 보안 & 준수 센터에서 조직 관리 역할 그룹의 구성원 이어야 합니다. 자세한 내용은 [Security & 준수 센터의 사용 권한을](permissions-in-the-security-and-compliance-center.md)참조 하세요.
    
- 준수 보안 필터 cmdlet을 사용 하려면 보안 & 준수 센터와 Exchange Online 조직 둘 다에 Windows PowerShell을 연결 해야 합니다. 이러한 cmdlet은 사서함 속성에 액세스 해야 하므로 Exchange Online에 연결 해야 하는 경우에 필요 합니다. 다음 섹션의 단계를 참조하세요. 
    
- 검색 권한 필터에 대한 자세한 내용은 [More information](#more-information) 섹션을 참조하세요. 
    
- 검색 사용 권한 필터링은 비활성 사서함에 적용할 수 있으며,이는 사서함 및 사서함 콘텐츠 필터링을 사용 하 여 비활성 사서함을 검색할 수 있는 사용자를 제한 하는 것을 의미 합니다. 사용 권한 필터링 및 비활성 사서함에 대 한 자세한 내용은 추가 [정보](#more-information) 섹션을 참조 하십시오. 
    
-  검색 사용 권한 필터링은 Exchange에서 공용 폴더를 검색할 수 있는 사용자를 제한 하는 데 사용할 수 없습니다. 
    
- 조직에서 만들 수 있는 검색 권한 필터의 수에는 제한이 없습니다. 하지만 검색 사용 권한 필터가 100 개 보다 많은 경우에는 search 성능이 영향을 받습니다. 조직의 검색 권한 필터 수를 가능한 한 작게 유지 하려면 가능 하면 단일 필터에서 Exchange, SharePoint 및 OneDrive에 대해 규칙을 결합 하는 필터를 만듭니다.
    
## <a name="connect-to-the-security--compliance-center-and-exchange-online-in-a-single-remote-powershell-session"></a>단일 원격 PowerShell 세션에서 보안 & 준수 센터 및 Exchange Online에 연결

1. 파일 이름 접미사. p s e c 1을 사용 하 여 Windows PowerShell 스크립트 파일에 다음 텍스트를 저장 **합니다.** 예를 들어 **ConnectEXO-CC**이라는 파일에 저장할 수 있습니다.
    
    ```
    $UserCredential = Get-Credential
    $Session = New-PSSession -ConfigurationName Microsoft.Exchange -ConnectionUri https://ps.outlook.com/powershell-liveid -Credential $UserCredential -Authentication Basic -AllowRedirection
    Import-PSSession $Session -DisableNameChecking
    $Session = New-PSSession -ConfigurationName Microsoft.Exchange -ConnectionUri https://ps.compliance.protection.outlook.com/powershell-liveid -Credential $UserCredential -Authentication Basic -AllowRedirection
    Import-PSSession $Session -AllowClobber -DisableNameChecking
    $Host.UI.RawUI.WindowTitle = $UserCredential.UserName + " (Exchange Online + Compliance Center)"
    ```

2. 로컬 컴퓨터에서 Windows PowerShell을 열고, 이전 단계에서 만든 스크립트가 있는 폴더로 이동한 다음 스크립트를 실행 합니다. 예를 들어:
    
    ```
    .\ConnectEXO-CC.ps1
    ```
 
작동 여부는 어떻게 확인하나요? 스크립트를 실행 한 후에는 보안 & 준수 센터 및 Exchange Online의 cmdlet을 로컬 Windows PowerShell 세션으로 가져옵니다. 오류가 발생하지 않으면 정상적으로 연결된 것입니다. 빠른 테스트는 보안 & 준수 센터 cmdlet 및 Exchange Online cmdlet을 실행 하는 것입니다. 예를 들어 **UnifiedCompliancePrerequisite** 및 **Get-Mailbox**를 실행할 수 있습니다. 
  
오류가 발생하면 다음 요구 사항을 확인합니다.
  
- 가장 흔한 문제는 암호를 잘못 입력한 경우입니다. 두 가지 단계를 다시 실행하고 1단계에서 사용자 이름과 암호를 입력할 때 신중하게 확인합니다.
    
- 계정에 보안 & 준수 센터에 대 한 액세스 권한이 있는지 확인 합니다. 자세한 내용은 [사용자에 게 보안 & 준수 센터에 대 한 액세스 권한을 부여](grant-access-to-the-security-and-compliance-center.md)를 참조 하십시오.
    
- DoS (서비스 거부) 공격을 방지 하려면 보안 & 준수 센터에 세 개의 개방형 원격 PowerShell 연결만을 사용 해야 합니다.
    
- 스크립트를 실행 하려면 Windows PowerShell을 구성 해야 합니다. 이 작업은 연결할 때마다 발생 하지 않고 한 번만 수행 하면 됩니다. Windows PowerShell이 서명된 스크립트를 실행하도록 설정하려면 관리자 권한 Windows PowerShell 창(**관리자 권한으로 실행**을 선택하면 열리는 Windows PowerShell 창)에서 다음 명령을 실행합니다.

    ```
    Set-ExecutionPolicy RemoteSigned
    ```
- 로컬 컴퓨터와 Office 365 간에 TCP 포트 80 트래픽을 열어야 합니다. 이 포트는 이미 열려 있을 수도 있지만 조직에서 제한적인 인터넷 액세스 정책을 사용하는 경우에는 열려 있는지를 고려해야 합니다.

  
## <a name="new-compliancesecurityfilter"></a>New-compliancesecurityfilter

**New-compliancesecurityfilter** 는 검색 권한 필터를 만드는 데 사용 됩니다. 다음 표에서는이 cmdlet의 매개 변수를 설명 합니다. 준수 보안 필터를 만들려면 모든 매개 변수가 필요합니다. 
  
|**매개 변수**|**설명**|
|:-----|:-----|
| _Action_ <br/> | _Action_ 매개 변수는 필터가 적용 되는 검색 작업 유형을 지정 합니다. 가능한 콘텐츠 검색 작업은 다음과 같습니다.  <br/><br/> **내보내기:** 검색 결과를 내보낼 때 필터가 적용 됩니다.  <br/> **미리 보기:** 검색 결과를 미리 볼 때 필터가 적용 됩니다.  <br/> **제거:** 검색 결과를 삭제할 때 필터가 적용 됩니다.  <br/> **검색:** 필터는 검색을 실행할 때 적용 됩니다.  <br/> **All:** 모든 검색 작업에 필터가 적용 됩니다.  <br/> |
| _FilterName_ <br/> |_FilterName_ 매개 변수는 권한 필터의 이름을 지정 합니다. 이 이름은 **Get-ComplianceSecurityFilter**, **Set-ComplianceSecurityFilter** 및 **Remove-ComplianceSecurityFilter** cmdlet을 사용할 때 필터를 식별하는 데 사용됩니다.  <br/> |
| _필터_ <br/> | _Filters_ 매개 변수는 준수 보안 필터에 대 한 검색 조건을 지정 합니다. 다음과 같은 세 가지 유형의 필터를 만들 수 있습니다.  <br/><br/> **사서함 필터링:** 이 필터 유형은 지정 된 사용자 ( _users_ 매개 변수에서 지정)가 검색할 수 있는 사서함을 지정 합니다. 이 필터 유형의 구문은 검색할 수 있는 사서함의 범위를 지정 __ 하는 데 사용 되는 사서함 속성을 **Mailbox_** _MailboxPropertyName_입니다. 예를 들어 사서함 필터 `"Mailbox_CustomAttribute10 -eq 'OttawaUsers'"` 를 사용 하면이 필터를 할당 받은 사용자가 CustomAttribute10 속성에 "OttawaUsers" 값을 갖는 사서함만 검색할 수 있습니다.  <br/>  _MailboxPropertyName_ 속성에는 지원 되는 모든 필터링 가능한 받는 사람 속성을 사용할 수 있습니다. 지원 되는 속성 목록을 보려면 [-RecipientFilter 매개 변수의 필터링 할 수 있는 속성](https://go.microsoft.com/fwlink/p/?LinkId=784903)을 참조 하십시오.  <br/><br/> **사서함 콘텐츠 필터링:** 이 유형의 필터는 검색할 수 있는 콘텐츠에 적용 됩니다. 할당 된 사용자가 검색할 수 있는 사서함 콘텐츠를 지정 합니다. 이러한 유형의 필터에 대 한 구문은 **MailboxContent_** _searchablepropertyname: Value_이며, _Searchablepropertyname_ 은 콘텐츠 검색에 지정할 수 있는 KQL (Keyword Query Language) 속성을 지정 합니다. 예를 들어 사서함 콘텐츠 필터 `MailboxContent_recipients:contoso.com` 를 사용 하 여이 필터를 할당 받은 사용자는 contoso.com 도메인의 받는 사람에 게 전송 된 메시지만 검색할 수 있습니다.  <br/>  검색 가능한 메시지 속성 목록은 [Keyword queries and search 조건문 For Content search](keyword-queries-and-search-conditions.md)을 참조 하십시오. <br/> <br/> **중요:**  단일 검색 필터에는 사서함 필터와 사서함 콘텐츠 필터가 포함 될 수 없습니다. 이 둘을 단일 필터에서 결합 하려면 [필터 목록을](#using-a-filters-list-to-combine-filter-types)사용 해야 합니다.  그러나 필터에는 동일한 유형의 보다 복잡 한 쿼리를 포함할 수 있습니다. 예를 들어`"Mailbox_CustomAttribute10 -eq 'FTE' -and Mailbox_MemberOfGroup -eq '$($DG.DistinguishedName)'"`  <br/><br/> **사이트 및 사이트 콘텐츠 필터링:** 할당 된 사용자가 검색할 수 있는 사이트 또는 사이트 콘텐츠를 지정 하는 데 사용할 수 있는 두 가지 SharePoint 및 비즈니스용 OneDrive 사이트 관련 필터가 있습니다.  <br/><br/> - **Site_** _SearchableSiteProperty_ <br/> - **SiteContent_** _SearchableSiteProperty_ <br/><br/>  이러한 두 필터는 서로 바꿔 사용할 수 있습니다. 예를 `"Site_Path -like 'https://contoso.sharepoint.com/sites/doctors*'"` 들어와 `"SiteContent_Path -like 'https://contoso.sharepoint.com/sites/doctors*'"` 같은 결과를 반환 합니다. 그러나 필터에서 수행 하는 작업을 식별 하는 데 도움이 `Site_` 되도록 사이트 관련 속성 (예: site URL)을 지정 하 고 `SiteContent_` 콘텐츠 관련 속성 (예: 문서 유형)을 지정 하는 데 사용할 수 있습니다. 예를 들어 필터 `"Site_Path -like 'https://contoso.sharepoint.com/sites/doctors*'"` 를 사용 하 여이 필터를 할당 받은 사용자가 https://contoso.sharepoint.com/sites/doctors 사이트 모음의 콘텐츠만 검색할 수 있도록 허용 합니다. 필터 `"SiteContent_FileExtension -eq 'docx'"` 를 사용 하면이 필터를 할당 한 사용자가 word 문서 (word 2007 이상)만 검색할 수 있습니다.  <br/><br/>  검색 가능한 사이트 속성 목록은 [SharePoint의 크롤링 및 관리 속성 개요](https://go.microsoft.com/fwlink/p/?LinkId=331599)를 참조 하세요. **쿼리** 가능 열에서 **예** 로 표시 된 속성을 사용 하 여 사이트 또는 사이트 콘텐츠 필터를 만들 수 있습니다.  <br/><br/> **중요:** 사용자가 특정 Office 365 서비스에서 콘텐츠 위치를 검색 하지 못하도록 명시적으로 허용 하려면 검색 권한 필터를 만들어야 합니다 (예: Exchange 사서함 또는 SharePoint 사이트를 검색 하지 못하게 함). 즉, 사용자가 조직의 모든 SharePoint 사이트를 검색할 수 있도록 하는 검색 권한 필터를 만들면 해당 사용자가 사서함을 검색할 수 없습니다. 예를 들어 SharePoint 관리자가 SharePoint 사이트만 검색 하도록 허용 하려면 사서함을 검색 하지 못하도록 필터를 만들어야 합니다. 마찬가지로 Exchange 관리자만 검색 사서함을 허용 하려면 사이트 검색을 차단 하는 필터를 만들어야 합니다.           |
| _사용자_ <br/> |_Users_ 매개 변수는이 필터가 콘텐츠 검색에 적용 되는 사용자를 지정 합니다. 별칭 또는 기본 SMTP 주소로 사용자를 식별합니다. 여러 값을 쉼표로 구분하여 지정하거나 **All** 값을 사용하여 모든 사용자에게 필터를 할당할 수 있습니다.  <br/> _Users_ 매개 변수를 사용 하 여 보안 & 준수 센터 역할 그룹을 지정할 수도 있습니다. 이렇게 하면 사용자 지정 역할 그룹을 만든 다음 해당 역할 그룹에 검색 권한 필터를 할당할 수 있습니다. 예를 들어 국내 회사의 미국 자회사에 대해 eDiscovery 관리자에 대 한 사용자 지정 역할 그룹을 사용 한다고 가정해 보겠습니다. _Users_ 매개 변수를 사용 하 여 역할 그룹의 Name 속성을 사용 하 여이 역할 그룹을 지정 하 고 _Filter_ 매개 변수를 사용 하 여 미국에 있는 사서함만 검색할 수 있습니다.  <br/> 이 매개 변수로 메일 그룹을 지정할 수는 없습니다.  <br/> |
   
### <a name="using-a-filters-list-to-combine-filter-types"></a>필터 목록을 사용 하 여 필터 유형 결합

*필터 목록은* 사서함 필터와 쉼표로 구분 된 사이트 필터를 포함 하는 필터입니다. 필터 목록을 사용 하는 것은 서로 다른 유형의 필터를 결합 하는 유일한 방법입니다. 다음 예제에서는 **사서함** 과 **사이트** 필터를 쉼표로 구분 합니다.

```
-Filters "Mailbox_CustomAttribute10 -eq 'OttawaUsers'", "Site_Path -like 'https://contoso.sharepoint.com/sites/doctors*'"
```

콘텐츠 검색을 실행 하는 동안 필터 목록을 포함 하는 필터를 처리 하면 필터 목록 (쉼표로 구분 된 각 필터에 하나씩)의 검색 권한 필터 두 개가 만들어집니다. 따라서 앞의 예제에서 사서함 검색 권한 필터와 사이트 검색 권한 필터 하나를 만듭니다. 

필터 목록을 사용 하는 대신 두 개의 개별 검색 권한 필터를 만들 수 있습니다. 따라서 앞의 예제에서는 사서함 특성에 대 한 필터와 사이트 특성에 대 한 하나의 필터를 만듭니다. 두 경우 모두 결과는 같습니다. 필터 목록을 사용 하거나 별도의 검색 권한 만들기 필터를 만드는 것은 기본 설정의 중요 한 사항입니다.

필터 목록 사용에 대해서는 다음 사항에 유의 하세요.

- **사서함** 필터와 **MailboxContent** 필터를 포함 하는 필터를 만들려면 필터 목록을 사용 해야 합니다. 

- 앞에서 설명한 것 처럼 단일 검색 권한 필터에 **사이트** 및 **SiteContent** 필터를 포함 하기 위해 필터 목록을 사용 하지 않아도 됩니다. 예를 들어, **-or** 연산자를 사용 하 여 **사이트** 와 **SiteContent** 필터를 결합할 수 있습니다.

   ```
   -Filters "Site_ComplianceAttribute -eq 'FourthCoffee' -or Site_Path -like 'https://contoso.sharepoint.com/sites/FourthCoffee*'"
   ```

- 필터 목록의 각 구성 요소에는 복잡 한 필터 구문이 포함 될 수 있습니다. 예를 들어 사서함과 사이트 필터에는 **or** 연산자로 구분 된 여러 필터가 포함 될 수 있습니다.

   ```
   -Filters "Mailbox_Department -eq 'CohoWinery' -or Mailbox_CustomAttribute10 -eq 'CohoUsers'", "Site_ComplianceAttribute -eq 'CohoWinery' -or Site_Path -like 'https://contoso.sharepoint.com/sites/CohoWinery*'"
   ```

## <a name="examples-of-creating-search-permissions-filters"></a>검색 권한 필터를 만드는 예

다음은 **New-ComplianceSecurityFilter** cmdlet을 사용하여 검색 권한 필터를 만드는 예입니다. 
  
이 예에서는 사용자 annb@contoso.com가 캐나다의 사서함에 대해서만 모든 콘텐츠 검색 작업을 수행할 수 있도록 허용 합니다. 이 필터에는 ISO 3166-1의 3자리 캐나다 국가 코드가 포함되어 있습니다.

```
New-ComplianceSecurityFilter -FilterName CountryFilter  -Users annb@contoso.com -Filters "Mailbox_CountryCode  -eq '124'" -Action All
```

이 예에서는 사용자의 donh 및 suzanf가에서 CustomAttribute1 mailbox 속성에 ' Marketing ' 값이 있는 사서함만 검색할 수 있도록 허용 합니다.

```
New-ComplianceSecurityFilter -FilterName MarketingFilter  -Users donh,suzanf -Filters "Mailbox_CustomAttribute1  -eq 'Marketing'" -Action Search
```
   
이 예에서는 "미국 검색 관리자" 역할 그룹의 구성원이 미국에 있는 사서함에 대해서만 모든 콘텐츠 검색 작업을 수행할 수 있도록 합니다. 이 필터에는 ISO 3166-1의 3자리 미국 국가 코드가 포함되어 있습니다.
  
```
New-ComplianceSecurityFilter -FilterName USDiscoveryManagers  -Users "US Discovery Managers" -Filters "Mailbox_CountryCode  -eq '840'" -Action All
```

이 예에서는 eDiscovery 관리자 역할 그룹의 구성원이 Ottawa 사용자 메일 그룹 구성원의 사서함만 검색할 수 있도록 허용 합니다. 
  
```
$DG = Get-DistributionGroup "Ottawa Users"
```

```
New-ComplianceSecurityFilter -FilterName DGFilter  -Users eDiscoveryManager -Filters "Mailbox_MemberOfGroup -eq '$($DG.DistinguishedName)'" -Action Search
```
이 예에서는 누구도 Executive Team 메일 그룹 구성원의 사서함에서 콘텐츠를 삭제하지 못하게 합니다.

```
$DG = Get-DistributionGroup "Executive Team"
```

```
New-ComplianceSecurityFilter -FilterName NoExecutivesPreview  -Users All -Filters "Mailbox_MemberOfGroup -ne '$($DG.DistinguishedName)'" -Action Purge
```
   
이 예에서는 OneDrive eDiscovery 관리자 사용자 지정 역할 그룹의 구성원이 조직의 비즈니스용 OneDrive 위치에 있는 콘텐츠만 검색할 수 있도록 허용 합니다.

```
New-ComplianceSecurityFilter -FilterName OneDriveOnly  -Users "OneDrive eDiscovery Managers" -Filters "Site_Path -like 'https://contoso-my.sharepoint.com/personal*'" -Action Search
```
   
> [!NOTE]
> 사용자가 특정 사이트를 검색 하도록 제한 하려면 이전 예제 `Site_Path`와 같이 필터를 사용 합니다. 사용 `Site_Site` 은 작동 하지 않습니다. 
  
이 예에서는 2015년 동안 보낸 전자 메일 메시지에 대해서만 모든 콘텐츠 검색 작업을 수행하도록 제한합니다.

```
New-ComplianceSecurityFilter -FilterName EmailDateRestrictionFilter -Users donh@contoso.com -Filters "MailboxContent_Received -ge '01-01-2015' -and MailboxContent_Received -le '12-31-2015'" -Action All
```
   
앞의 예와 마찬가지로 이 예에서는 2015년에 마지막으로 변경된 문서에 대해서만 모든 콘텐츠 검색 작업을 수행하도록 제한합니다.

```
New-ComplianceSecurityFilter -FilterName DocumentDateRestrictionFilter -Users donh@contoso.com -Filters "SiteContent_LastModifiedTime -ge '01-01-2015' -and SiteContent_LastModifiedTime -le '12-31-2015'" -Action All
```
   
이 예에서는 "OneDrive 검색 관리자" 역할 그룹의 구성원이 조직의 모든 사서함에 대해 콘텐츠 검색 작업을 수행 하지 못하도록 차단 합니다. 

```
New-ComplianceSecurityFilter -FilterName NoEXO -Users "OneDrive Discovery Managers" -Filters "Mailbox_Alias -notlike '*'"  -Action All
```

이 예에서는 조직의 모든 사용자가 janets 또는 sarad에서 보내거나 받은 전자 메일 메시지를 검색할 수 없도록 합니다.

```
New-ComplianceSecurityFilter -FilterName NoSaraJanet -Users All -Filters "MailboxContent_Participants -notlike 'janets@contoso.onmicrosoft.com' -and MailboxContent_Participants -notlike 'sarad@contoso.onmicrosoft.com'" -Action Search
```

이 예에서는 필터 목록을 사용 하 여 사서함 및 사이트 필터를 결합 합니다.

```
New-ComplianceSecurityFilter -FilterName "Coho Winery Security Filter" -Users "Coho Winery eDiscovery Managers", "Coho Winery Investigators" -Filters "Mailbox_Department -eq 'CohoWinery'", "Site_ComplianceAttribute -eq 'CohoWinery' -or Site_Path -like 'https://contoso.sharepoint.com/sites/CohoWinery*'" -Action ALL
```

## <a name="get-compliancesecurityfilter"></a>New-compliancesecurityfilter

**New-compliancesecurityfilter** 는 검색 권한 필터 목록을 반환 하는 데 사용 됩니다. 특정 검색 필터에 대 한 정보를 반환 하려면 _FilterName_ 매개 변수를 사용 합니다. 
  
## <a name="set-compliancesecurityfilter"></a>New-compliancesecurityfilter

**New-compliancesecurityfilter** 는 기존 검색 권한 필터를 수정 하는 데 사용 됩니다. 필수 매개 변수는 _FilterName_뿐입니다. 
  
|**매개 변수**|**설명**|
|:-----|:-----|
| _Action_| _Action_ 매개 변수는 필터가 적용 되는 검색 작업 유형을 지정 합니다. 가능한 콘텐츠 검색 작업은 다음과 같습니다. <br/><br/> **내보내기:** 검색 결과를 내보낼 때 필터가 적용 됩니다.  <br/> **미리 보기:** 검색 결과를 미리 볼 때 필터가 적용 됩니다.  <br/> **제거:** 검색 결과를 삭제할 때 필터가 적용 됩니다.  <br/> **검색:** 필터는 검색을 실행할 때 적용 됩니다.  <br/> **All:** 모든 검색 작업에 필터가 적용 됩니다.  <br/> |
| _FilterName_|_FilterName_ 매개 변수는 권한 필터의 이름을 지정 합니다. |
| _필터_| _Filters_ 매개 변수는 준수 보안 필터에 대 한 검색 조건을 지정 합니다. 다음과 같은 두 가지 유형의 필터를 만들 수 있습니다. <br/><br/>**사서함 필터링:** 이 필터 유형은 지정 된 사용자 ( _users_ 매개 변수에서 지정)가 검색할 수 있는 사서함을 지정 합니다. 이 필터 유형의 구문은 검색할 수 있는 사서함의 범위를 지정 __ 하는 데 사용 되는 사서함 속성을 **Mailbox_** _MailboxPropertyName_입니다. 예를 들어 사서함 필터 `"Mailbox_CustomAttribute10 -eq 'OttawaUsers'"` 를 사용 하면이 필터를 할당 받은 사용자가 CustomAttribute10 속성에 "OttawaUsers" 값을 갖는 사서함만 검색할 수 있습니다.  _MailboxPropertyName_ 속성에는 지원 되는 모든 필터링 가능한 받는 사람 속성을 사용할 수 있습니다. 지원 되는 속성 목록을 보려면 [-RecipientFilter 매개 변수의 필터링 할 수 있는 속성](https://go.microsoft.com/fwlink/p/?LinkId=784903)을 참조 하십시오. <br/><br/>**사서함 콘텐츠 필터링:** 이 유형의 필터는 검색할 수 있는 콘텐츠에 적용 됩니다. 할당 된 사용자가 검색할 수 있는 사서함 콘텐츠를 지정 합니다. 이러한 유형의 필터에 대 한 구문은 **MailboxContent_** _searchablepropertyname: Value_이며, _Searchablepropertyname_ 은 콘텐츠 검색에 지정할 수 있는 KQL (Keyword Query Language) 속성을 지정 합니다. 예를 들어 사서함 콘텐츠 필터 `MailboxContent_recipients:contoso.com` 를 사용 하 여이 필터를 할당 받은 사용자는 contoso.com 도메인의 받는 사람에 게 전송 된 메시지만 검색할 수 있습니다.  검색 가능한 메시지 속성 목록은 [Keyword queries For Content Search](keyword-queries-and-search-conditions.md)을 참조 하십시오. <br/><br/>**사이트 및 사이트 콘텐츠 필터링:** 할당 된 사용자가 검색할 수 있는 사이트 또는 사이트 콘텐츠를 지정 하는 데 사용할 수 있는 두 가지 SharePoint 및 비즈니스용 OneDrive 사이트 관련 필터가 있습니다. <br/><br/>- **Site_** *SearchableSiteProperty* <br/>- **SiteContent**_*SearchableSiteProperty*<br/><br/>이러한 두 필터는 서로 바꿔 사용할 수 있습니다. 예를 `"Site_Path -like 'https://contoso.spoppe.com/sites/doctors*'"` 들어와 `"SiteContent_Path -like 'https://contoso.spoppe.com/sites/doctors*'"` 같은 결과를 반환 합니다. 그러나 필터에서 수행 하는 작업을 식별 하는 데 도움이 `Site_` 되도록 사이트 관련 속성 (예: site URL)을 지정 하 고 `SiteContent_` 콘텐츠 관련 속성 (예: 문서 유형)을 지정 하는 데 사용할 수 있습니다. 예를 들어 필터 `"Site_Path -like 'https://contoso.spoppe.com/sites/doctors*'"` 를 사용 하 여이 필터를 할당 받은 사용자가 https://contoso.spoppe.com/sites/doctors 사이트 모음의 콘텐츠만 검색할 수 있도록 허용 합니다. 필터 `"SiteContent_FileExtension -eq 'docx'"` 를 사용 하면이 필터를 할당 한 사용자가 word 문서 (word 2007 이상)만 검색할 수 있습니다.  <br/><br/>검색 가능한 사이트 속성 목록은 [SharePoint의 크롤링 및 관리 속성 개요](https://go.microsoft.com/fwlink/p/?LinkId=331599)를 참조 하세요. **쿼리** 가능 열에서 **예** 로 표시 된 속성을 사용 하 여 사이트 또는 사이트 콘텐츠 필터를 만들 수 있습니다. <br/><br/>          |
| _사용자_|_Users_ 매개 변수는이 필터가 콘텐츠 검색에 적용 되는 사용자를 지정 합니다. 다중 값 속성 이므로이 매개 변수를 사용 하 여 사용자 또는 사용자 그룹을 지정 하면 기존 사용자 목록을 덮어쓰게 됩니다. 선택한 사용자를 추가 및 제거 하는 구문에 대해서는 다음 예제를 참조 하세요. <br/><br/>_Users_ 매개 변수를 사용 하 여 보안 & 준수 센터 역할 그룹을 지정할 수도 있습니다. 이렇게 하면 사용자 지정 역할 그룹을 만든 다음 해당 역할 그룹에 검색 권한 필터를 할당할 수 있습니다. 예를 들어 국내 회사의 미국 자회사에 대해 eDiscovery 관리자에 대 한 사용자 지정 역할 그룹을 사용 한다고 가정해 보겠습니다. _Users_ 매개 변수를 사용 하 여 역할 그룹의 Name 속성을 사용 하 여이 역할 그룹을 지정 하 고 _Filter_ 매개 변수를 사용 하 여 미국에 있는 사서함만 검색할 수 있습니다. <br/><br/>이 매개 변수로 메일 그룹을 지정할 수는 없습니다. |

## <a name="examples-of-changing-search-permissions-filters"></a>검색 권한 필터 변경의 예

다음은 **new-compliancesecurityfilter** 및 **new-compliancesecurityfilter** cmdlet을 사용 하 여 필터가 할당 된 사용자의 기존 목록에 사용자를 추가 하거나 제거 하는 방법을 보여 주는 예제입니다. 필터에서 사용자를 추가 또는 제거할 때는 SMTP 주소를 사용하여 사용자를 지정합니다. 
  
이 예에서는 필터에 사용자를 추가합니다.

```
$filterusers = Get-ComplianceSecurityFilter -FilterName OttawaUsersFilter
```
```
$filterusers.users.add("pilarp@contoso.com")
```

```
Set-ComplianceSecurityFilter -FilterName OttawaUsersFilter -Users $filterusers.users
```
   
이 예에서는 필터에서 사용자를 제거합니다.

```
$filterusers = Get-ComplianceSecurityFilter -FilterName OttawaUsersFilter
```

```
$filterusers.users.remove("annb@contoso.com")
```

```
Set-ComplianceSecurityFilter -FilterName OttawaUsersFilter -Users $filterusers.users
```
  
## <a name="remove-compliancesecurityfilter"></a>New-compliancesecurityfilter을 제거 합니다.

**New-compliancesecurityfilter** 는 검색 필터를 삭제 하는 데 사용 됩니다. 삭제할 필터를 지정 하려면 _FilterName_ 매개 변수를 사용 합니다. 
  
## <a name="more-information"></a>추가 정보

- **검색 권한 필터링이 작동 하는 방식** 콘텐츠 검색을 실행할 때 검색 쿼리에 사용 권한 필터가 추가 됩니다. 사용 권한 필터는 **AND** Boolean 연산자에 의해 검색 쿼리에 조인 됩니다. 예를 들어 Bob이 작업자 메일 그룹 구성원의 사서함에 대 한 모든 검색 작업을 수행할 수 있도록 하는 사용 권한 필터가 있습니다. 그러면 Bob이 검색 쿼리 `sender:jerry@adatum.com`를 사용 하 여 조직의 모든 사서함에 대해 콘텐츠 검색을 실행 합니다. 사용 권한 필터와 검색 쿼리는 **and** 연산자에 의해 논리적으로 결합 되므로, 검색 기능은 jerry@adatum.com에서 보낸 모든 메시지를 작업자 메일 그룹의 구성원으로 반환 합니다. 
    
- **여러 검색 권한 필터가 있는 경우 발생하는 결과** 콘텐츠 검색 쿼리에서 여러 권한 필터는 **OR** 부울 연산자로 결합됩니다. 따라서 필터 중 하나가 참이면 결과가 반환됩니다. 콘텐츠 검색에서 모든 필터(**OR** 연산자로 결합)는 **AND** 연산자를 사용하여 검색 쿼리와 결합됩니다. 검색 필터를 통해 Bob이 작업자 메일 그룹 구성원의 사서함만 검색할 수 있도록 하는 위의 예를 살펴보겠습니다. 그런 후에 이제 Bob이 Phil의 사서함("Mailbox_Alias -ne 'Phil'")을 검색하지 못하도록 하는 다른 필터를 만듭니다. 이번에는 Phil을 작업자 그룹의 구성원으로 가정합니다. Bob이 조직의 모든 사서함에 대 한 콘텐츠 검색 (이전 예에서)을 실행 하면 Bob이 Phil의 사서함을 검색 하지 못하도록 필터를 적용 했더라도 Phil의 사서함에 대 한 검색 결과가 반환 됩니다. 이것은 Bob이 작업자 그룹을 검색할 수 있도록 하는 첫 번째 필터가 올바르기 때문입니다. Phil이 작업자 그룹의 구성원이더라도 Bob은 Phil의 사서함을 검색할 수 있습니다. 
    
- **검색 권한 필터링이 비활성 사서함에 대해 작동 하나요?** 예, 사서함 및 사서함 콘텐츠 필터를 사용 하 여 조직에서 비활성 사서함을 검색할 수 있는 사용자를 제한할 수 있습니다. 일반 사서함 처럼 사용 권한 필터를 만드는 데 사용 되는 받는 사람 속성을 사용 하 여 비활성 사서함을 구성 해야 합니다. 필요한 경우 **Mailbox-InactiveMailboxOnly** 명령을 사용 하 여 비활성 사서함의 속성을 표시할 수 있습니다. 자세한 내용은 [Office 365에서 비활성 사서함 만들기 및 관리](create-and-manage-inactive-mailboxes.md)를 참조 하세요.
    
- **검색 권한 필터링이 공용 폴더에 대해 작동 하나요?** 아니요. 앞에서 설명한 것 처럼 검색 권한 필터링은 Exchange에서 공용 폴더를 검색할 수 있는 사용자를 제한 하는 데 사용할 수 없습니다. 예를 들어 공용 폴더 위치에 있는 항목은 사용 권한 필터로 검색 결과에서 제외할 수 없습니다. 
    
- **사용자가 특정 서비스의 모든 콘텐츠 위치를 검색 하도록 허용 하 여 다른 서비스의 콘텐츠 위치를 검색 하지 못하게 할 수도 있습니까?** 아니요. 앞에서 설명한 대로 검색 권한 필터를 만들어 사용자가 특정 Office 365 서비스에서 콘텐츠 위치를 검색 하지 못하도록 명시적으로 설정 해야 합니다 (예: Exchange 사서함 또는 SharePoint 사이트를 검색 하지 못하게 함). 즉, 사용자가 조직의 모든 SharePoint 사이트를 검색할 수 있도록 하는 검색 권한 필터를 만들면 해당 사용자가 사서함을 검색할 수 없습니다. 예를 들어 SharePoint 관리자가 SharePoint 사이트만 검색 하도록 허용 하려면 사서함을 검색 하지 못하도록 필터를 만들어야 합니다. 마찬가지로 Exchange 관리자만 검색 사서함을 허용 하려면 사이트 검색을 차단 하는 필터를 만들어야 합니다.
