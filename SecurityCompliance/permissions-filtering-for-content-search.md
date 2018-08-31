---
title: 콘텐츠 검색에 대한 권한 필터링 구성
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 5/14/2018
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MOE150
- MET150
ms.assetid: 1adffc35-38e5-4f7d-8495-8e0e8721f377
description: Office 365 조직에서 사서함 및 사이트의 하위 집합을 검색 하는 eDiscovery 관리자 하도록 하려면이 옵션을 필터링 하는 콘텐츠 검색 사용 권한을 사용 합니다.
ms.openlocfilehash: 2b6968a097e7abe5943a84b9ceb9b6d126057cc2
ms.sourcegitcommit: c166964fe14eec69139a2d3d9c10d2c40ab33f91
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/28/2018
ms.locfileid: "23258626"
---
# <a name="configure-permissions-filtering-for-content-search"></a>콘텐츠 검색에 대한 권한 필터링 구성

Office 365 조직에서 사서함 및 사이트의 하위 집합을 검색 하는 eDiscovery 관리자 하도록 하려면이 옵션을 필터링 하는 검색 사용 권한을 사용할 수 있습니다. 또한 해당 동일한 eDiscovery 관리자만 특정 검색 조건을 충족 하는 사서함 또는 사이트 콘텐츠를 검색 하도록 하려면이 옵션을 필터링 하는 사용 권한을 사용할 수 있습니다. 예, 특정 위치 또는 부서에만 사용자의 사서함을 검색 하는 eDiscovery 관리자를 할당할 수도 있습니다. 지원 되는 받는 사람 필터를 사용 하 여 검색할 수 있는 사서함 수를 제한 하는 필터를 만들어이 작업을 수행 합니다. 사서함 콘텐츠를 검색할 수를 지정 하는 필터를 만들 수도 있습니다. 검색 가능한 메시지 속성을 사용 하는 필터를 만들어이 작업은 수행 합니다. 마찬가지로,만 조직에서 특정 SharePoint 사이트를 검색 하는 eDiscovery 관리자를 할당할 수도 있습니다. 사이트를 검색할 수를 제한 하는 필터를 만들어이 작업을 수행 합니다. 사이트 콘텐츠를 검색할 수를 지정 하는 필터를 만들 수도 있습니다. 검색 가능한 사이트 속성을 사용 하는 필터를 만들어이 작업은 수행 합니다.

검색 권한을 만들려면 논리적 경계 ( *준수 경계*라고 함)는 Office 365 조직 내에 있음 (예: 사서함, SharePoint 사이트 및 OneDrive 계정) 사용자 콘텐츠 위치를 제어 하는 필터링을 사용할 수 있습니다는 특정 eDiscovery 관리자를 검색할 수 있습니다. 자세한 내용은 [Office 365의 eDiscovery 조사에 대 한 준수 경계 설정](set-up-compliance-boundaries.md)을 참조 하십시오.
  
Office 365 보안에서 콘텐츠 검색 기능을 통해 필터링 하는 검색 사용 권한을 사용할 수 &amp; 준수 센터입니다. 이러한 4 개의 cmdlet을 사용 하 여 구성 하 고 검색 permisisons 필터를 관리할 수 있습니다.
  
[새 ComplianceSecurityFilter](#new-compliancesecurityfilter)

[Get-ComplianceSecurityFilter](#get-compliancesecurityfilter)

[집합 ComplianceSecurityFilter](#set-compliancesecurityfilter)

[ComplianceSecurityFilter 제거](#remove-compliancesecurityfilter)

## <a name="before-you-begin"></a>시작하기 전에

- 규정 준수 보안 필터 cmdlet를 실행 하려면 보안에서 조직 관리 역할 그룹의 구성원 이어야 필요가 &amp; 준수 센터입니다. 자세한 내용은 참조 [Office 365 보안에 대 한 사용 권한을 &amp; 준수 센터](permissions-in-the-security-and-compliance-center.md)합니다.
    
- 두 보안을 Windows PowerShell에 연결 해야 &amp; 준수 센터 및 규정 준수 보안 필터 cmdlet을 사용 하 여 Exchange Online 조직에 있습니다. 이러한 cmdlet는 Exchange Online에 연결 해야 하는 이유는 사서함 속성에 액세스할 수 있어야 하기 때문에 필요한입니다. 다음 섹션의 단계를 참조 하십시오. 
    
- 검색 권한 필터에 대한 자세한 내용은 [More information](#more-information) 섹션을 참조하세요. 
    
- 검색 권한을 필터링 사서함 및 사서함 콘텐츠 비활성 사서함을 검색할 수 있는 사람을 제한에는 필터링을 사용할 수 있는 비활성 사서함에 적용 됩니다. 필터링 하는 사용 권한 및 비활성 사서함에 대 한 추가 정보에 대 한 [자세한 내용](#more-information) 은 섹션을 참조 하십시오. 
    
-  Exchange 공용 폴더를 검색할 수 있는 제한 검색 권한은 필터링을 사용할 수 없습니다. 
    
- 조직 내에서 만들 수 있는 검색 권한 필터의 수에 제한이 없습니다. 그러나 검색 성능 영향을 미칩니다 100 개가 넘는 검색 권한 필터 했으면 합니다. 조직에서 검색 권한 필터의 수를 가능한 한 작게 유지 하려면 가능 하면 항상 단일 필터에 Exchange, SharePoint 및 OneDrive에 대 한 규칙을 결합 하는 필터를 만듭니다.
    
## <a name="connect-to-the-security-amp-compliance-center-and-exchange-online-in-a-single-remote-powershell-session"></a>보안을 연결할 &amp; 준수 센터 및 단일 원격 PowerShell 세션에서 Exchange Online

1. .Ps1 파일 이름 접미사를 사용 하 여 Windows PowerShell 스크립트 파일에 다음 텍스트를 저장 합니다. 예, ConnectEXO CC.ps1 라는 파일을 저장할 수 있습니다.
    
    ```
    $UserCredential = Get-Credential
    $Session = New-PSSession -ConfigurationName Microsoft.Exchange -ConnectionUri https://ps.outlook.com/powershell-liveid -Credential $UserCredential -Authentication Basic -AllowRedirection
    Import-PSSession $Session -DisableNameChecking
    $Session = New-PSSession -ConfigurationName Microsoft.Exchange -ConnectionUri https://ps.compliance.protection.outlook.com/powershell-liveid -Credential $UserCredential -Authentication Basic -AllowRedirection
    Import-PSSession $Session -AllowClobber -DisableNameChecking
    $Host.UI.RawUI.WindowTitle = $UserCredential.UserName + " (Exchange Online + Compliance Center)"
    ```

2. 로컬 컴퓨터에서 Windows PowerShell, 이전 단계에서 만든 스크립트 위치한 폴더로 이동한 다음 열고 실행 스크립트입니다. 예를 들어:
    
    ```
    .\ConnectEXO-CC.ps1
    ```
 
이 작동 하는 경우 어떻게 알 수 있습니까? Cmdlet은 보안에서 스크립트를 실행 하 고 나면 &amp; 준수 센터 및 Exchange Online 로컬 Windows PowerShell 세션으로 가져옵니다. 모든 오류가 하지 않으면 하는 경우 성공적으로 연결한 합니다. 빠른 테스트를 실행 하는 유가 증권를 &amp; 준수 센터 cmdlet- **설치 UnifiedCompliancePrerequisite** 예-및 **Get-mailbox**등의 Exchange Online cmdlet을 합니다. 
  
오류가 발생하면 다음 요구 사항을 확인합니다.
  
- 가장 흔한 문제는 암호를 잘못 입력한 경우입니다. 두 가지 단계를 다시 실행하고 1단계에서 사용자 이름과 암호를 입력할 때 신중하게 확인합니다.
    
- 사용자 계정에는 보안에 액세스할 수 있는 권한이 있는지 확인 &amp; 준수 센터입니다. 자세한 내용은 참조 [보안에 사용자가 액세스할 수 있도록 &amp; 준수 센터](grant-access-to-the-security-and-compliance-center.md)합니다.
    
- 세개의 개방형 원격 PowerShell에 대 한 연결 보안에는 서비스 거부 (DoS) 공격을 방지 하려면 &amp; 준수 센터입니다.
    
- Windows PowerShell은 스크립트를 실행하도록 구성해야 합니다. 이 설정은 연결할 때마다 구성하는 것이 아니라 컴퓨터에서 한 번만 구성하면 됩니다. Windows PowerShell이 서명된 스크립트를 실행하도록 하려면 상승된 Windows PowerShell 창( **관리자 권한으로 실행**을 선택하여 열린 Windows PowerShell 창)에서 다음 명령을 실행합니다.

    ```
    Set-ExecutionPolicy RemoteSigned
    ```
- TCP 포트 80 트래픽에 로컬 컴퓨터 및 Office 365 사이 열려 있어야 합니다. 아마도 열려 있지만 조직에는 제한적인 인터넷 액세스 정책이 하는 경우를 고려 하는 것이.
    

  
## <a name="new-compliancesecurityfilter"></a>새 ComplianceSecurityFilter
<a name="New"> </a>

새 검색 권한 필터를 만들려면 **새로 만들기 ComplianceSecurityFilter** 사용 됩니다. 다음 표에서이 cmdlet에 대 한 매개 변수를 설명 합니다. 규정 준수 보안 필터를 만드는 모든 매개 변수가 필요 합니다. 
  
|**매개 변수**|**설명**|
|:-----|:-----|
| _다중값 속성에서 하나 이상의 값 제거_ <br/> | _Action_ 매개 변수는 해당 필터에 적용 되는 검색 작업 유형을 지정 합니다. 가능한 콘텐츠 검색 동작은 다음과 같습니다.<br/><br/> **내보내기** -필터 검색 결과 내보낼 때 적용 됩니다.  <br/> 검색 결과 미리볼 때 **미리 보기** -필터가 적용 됩니다.  <br/> 검색 결과 삭제 하는 경우 **항목 지우기** -filter가 적용 됩니다.  <br/> **검색** -필터 검색을 실행할 때 적용 됩니다.  <br/> **모든** -필터 검색 한 모든 작업이 적용 됩니다.  <br/> |
| _FilterName_ <br/> |_FilterName_ 매개 변수는 사용 권한 필터의 이름을 지정합니다. 이 이름은 사용 되는 id에 필터를 **Get ComplianceSecurityFilter**, **집합-ComplianceSecurityFilter** 및 **제거 ComplianceSecurityFilter** cmdlet을 사용 하는 경우.<br/> |
| _필터_ <br/> | _필터_ 매개 변수는 준수 보안 필터에 대 한 검색 조건을 지정합니다. 세가지 다른 종류의 필터를 만들 수 있습니다.<br/><br/> **사서함 필터링** -이 유형의 필터 사서함을 검색할 수 있습니다 ( _사용자가_ 매개 변수에 의해 지정 된) 할당 된 사용자를 지정 합니다. 이 유형의 필터에 대 한 구문은 **Mailbox_** _MailboxPropertyName_, _MailboxPropertyName_ 범위를 검색할 수 있는 사서함에 사용 되는 사서함 속성을 지정 합니다. 사서함 필터 등 `"Mailbox_CustomAttribute10 -eq 'OttawaUsers'"` CustomAttribute10 속성에 사용자 할당이 필터 값이 포함 된 사서함을 검색 하는를 "OttawaUsers"를 허용 합니다.<br/>  지원 되는 모든 필터링 할 수 있는 받는 사람 속성 _MailboxPropertyName_ 속성에 대해 사용할 수 있습니다. 지원 되는 속성의 목록 [-RecipientFilter 매개 변수에 대 한 필터링 할 수 있는 속성](https://go.microsoft.com/fwlink/p/?LinkId=784903)을 참조 하십시오.<br/><br/> **사서함 콘텐츠 필터링** -이 유형의 필터는 검색할 수 있는 콘텐츠에 적용 됩니다. 할당 된 사용자를 검색할 수 있는 사서함 콘텐츠를 지정 합니다. 이 유형의 필터에 대 한 구문은 **MailboxContent_** _SearchablePropertyName:value_, _SearchablePropertyName_ 콘텐츠 검색에 지정할 수 있는 키워드 쿼리 언어 (KQL) 속성을 지정 합니다. 사서함 콘텐츠 필터 등 `MailboxContent_recipients:contoso.com` contoso.com 도메인의 받는 사람에 게 보내는 메시지에 대 한 검색만이 필터는 사용자에 게 할당을 사용 하면 됩니다.<br/>  검색 가능한 메시지 속성의 목록이 [키워드 쿼리 및 콘텐츠 검색에 대 한 검색 조건을](keyword-queries-and-search-conditions.md)참조 하십시오.  <br/><br/> **사이트 및 사이트 콘텐츠 필터링** -두 SharePoint와 OneDrive 할당 된 사용자가 어떤 사이트 또는 사이트 콘텐츠를 검색할 수를 지정 하는데 사용할 수 있는 비즈니스 사이트와 관련 된 필터에 대 한 있습니다.  <br/><br/> - **사이트 _** _SearchableSiteProperty_ <br/> - **SiteContent_** _SearchableSiteProperty_ <br/><br/>  이러한 두 필터는 서로 바꿔서 사용할 수 있습니다. 예 `"Site_Path -like 'https://contoso.sharepoint.com/sites/doctors*'"` 및 `"SiteContent_Path -like 'https://contoso.sharepoint.com/sites/doctors*'"` 동일한 결과 반환 합니다. 사용할 수 있는 필터를 수행 하는 작업을 식별할 수 있도록, 하지만 `Site_` 사이트와 관련 된 속성 (예: 사이트 URL)을 지정 하려면 및 `SiteContent_` (예: 문서 형식 콘텐츠 관련 속성을 지정 하려면. 필터 등 `"Site_Path -like 'https://contoso.sharepoint.com/sites/doctors*'"` 만의 콘텐츠를 검색 하려면이 필터는 사용자에 게 할당을 사용 하면는 https://contoso.sharepoint.com/sites/doctors 사이트 모음입니다. 필터 `"SiteContent_FileExtension -eq 'docx'"` Word 문서 (Word 2007 이상)에 대 한 검색만이 필터는 사용자에 게 할당을 사용 하면 됩니다.<br/><br/>  검색 가능한 사이트 속성의 목록에 대 한 [크롤링 속성 및 관리 SharePoint에서 속성의 개요를](https://go.microsoft.com/fwlink/p/?LinkId=331599)참조 합니다. **예** 의 표시 된 속성은 * * 쿼리 가능 * * 열을 사용 하 여 사이트 또는 사이트 콘텐츠 필터를 만들 수 있습니다.<br/> <br/> **중요:**  단일 검색 필터는 한 가지 유형의 필터;를 하나만 사용할 수 있습니다. 사서함 필터와 사이트 필터; 포함할 수 없습니다. 마찬가지로, 사서함 필터 및 사서함 콘텐츠 필터를 포함할 수 없습니다. 그러나 필터 같은 종류의 보다 복잡 한 쿼리를 포함할 수 있습니다. 예를 들어`"Mailbox_CustomAttribute10 -eq 'FTE' -and Mailbox_MemberOfGroup -eq '$($DG.DistinguishedName)'"` <br/><br/> **중요:** 명시적으로 (예: 모든 Exchange 사서함 또는 모든 SharePoint 사이트를 검색에서 사용자를 방지) 특정 Office 365 서비스에서 콘텐츠 위치를 검색에서 사용자를 방지 하기 위해 검색 권한 필터를 만들 해야 합니다. 즉, 조직에서 모든 SharePoint 사이트를 검색 하는 사용자 수 있게 하는 검색 사용 권한 필터를 만드는 사서함 검색에서 해당 사용자를 방지 하지 않습니다. 예, SharePoint 관리자가 SharePoint 사이트를 검색 하는 수 있도록 해야 사서함 검색을 금지 하는 필터를 만든 다음 만든. 마찬가지로, Exchange 관리자만 사서함을 검색할 수 있도록 해야 만들려면 사이트 검색을 금지 하는 필터를 만들 수 있습니다.           |
| _사용자_ <br/> |_사용자가_ 매개 변수는 해당 되는 콘텐츠 검색에 적용 된이 필터를 가져올 사용자를 지정 합니다. 사용자가 자신의 별칭 또는 기본 SMTP 주소를 식별 합니다. 쉼표로 구분 하 여 여러 값을 지정할 수 또는 **모든**값을 사용 하 여 필터를 모든 사용자에 게 할당할 수 있습니다.<br/> 보안을 지정 하려면 _사용자가_ 매개 변수를 사용할 수도 있습니다 &amp; 준수 센터 역할 그룹입니다. 검색 사용 권한 필터를 그룹화 하는이 사용자 지정 역할 그룹을 만들고 다음 해당 역할을 할당을이 사용 합니다. 등의 여러 국가 corporation 미국 자회사 eDiscovery 관리자에 대 한 사용자 지정 역할 그룹을 해야 가정해 보겠습니다. (사용 하 여 역할 그룹의 Name 속성)이 역할 그룹을 지정 하 고 다음 _Filter_ 매개 변수를 사용 하 여 검색할 미국에서 사서함만 허용 하려면 _사용자가_ 매개 변수를 사용할 수 있습니다.<br/> 이 매개 변수로 메일 그룹을 지정할 수는 없습니다.  <br/> |
   

## <a name="examples-of-creating-search-permissions-filters"></a>검색 사용 권한 필터 만들기 (영문)의 예

다음은 **New-ComplianceSecurityFilter** cmdlet을 사용하여 검색 권한 필터를 만드는 예입니다. 
  
이 예제에서는 사용자 annb@contoso.com을 캐나다의 사서함에 대해서만 모든 콘텐츠 검색 작업을 수행할 수 있습니다. 이 필터는 캐나다 ISO 3166-1에서에서 3 자리 숫자 국가 코드를 포함합니다.

```
New-ComplianceSecurityFilter -FilterName CountryFilter  -Users annb@contoso.com -Filters "Mailbox_CountryCode  -eq '124'" -Action All
```

이 예에서는 사용자 donh 및 suzanf가 CustomAttribute1 사서함 속성 값이 'Marketing'인 사서함만 검색할 수 있도록 합니다.

```
New-ComplianceSecurityFilter -FilterName MarketingFilter  -Users donh,suzanf -Filters "Mailbox_CustomAttribute1  -eq 'Marketing'" -Action Search
```
   
이 예에서는 "미국 검색 관리자" 역할 그룹의 구성원이 미국에 있는 사서함에 대해서만 모든 콘텐츠 검색 작업을 수행할 수 있도록 합니다. 이 필터에는 ISO 3166-1의 3자리 미국 국가 코드가 포함되어 있습니다.
  
```
New-ComplianceSecurityFilter -FilterName USDiscoveryManagers  -Users "US Discovery Managers" -Filters "Mailbox_CountryCode  -eq '840'" -Action All
```

이 예에서는 eDiscovery 관리자 역할 그룹의 구성원이 Ottawa 사용자 메일 그룹 구성원의 사서함만 검색할 수 있도록 합니다. 
  
```
$DG = Get-DistributionGroup "Ottawa Users"
```

```
New-ComplianceSecurityFilter -FilterName DGFilter  -Users eDiscoveryManager -Filters "Mailbox_MemberOfGroup -eq '$($DG.DistinguishedName)'" -Action Search
```
이 예에서는 어떤 사용자도 실무 팀 메일 그룹 구성원의 사서함에서 콘텐츠를 삭제할 수 없도록 합니다.

```
$DG = Get-DistributionGroup "Executive Team"
```

```
New-ComplianceSecurityFilter -FilterName NoExecutivesPreview  -Users all -Filters "Mailbox_MemberOfGroup -ne '$($DG.DistinguishedName)'" -Action Purge
```
   
이 예에서는 조직에서 비즈니스 위치에 대 한 OneDrive의 콘텐츠에 대 한 검색만 OneDrive eDiscovery 관리자 사용자 지정 역할 그룹의 구성원을 허용 합니다.

```
New-ComplianceSecurityFilter -FilterName OneDriveOnly  -Users "OneDrive eDiscovery Managers" -Filters "Site_Path -like 'https://contoso-my.sharepoint.com/personal*'" -Action Search
```
   
> [!NOTE]
> 사용자를 특정 사이트 검색를 제한 하는 필터를 사용 하 여 `Site_Path`앞의 예제와 같이, 합니다. 사용 하 여 `Site_Site` 작동 하지 것입니다. 
  
이 예에서는 2015년 동안 보낸 전자 메일 메시지에 대해서만 모든 콘텐츠 검색 작업을 수행하도록 제한합니다.

```
New-ComplianceSecurityFilter -FilterName EmailDateRestrictionFilter -Users donh@contoso.com -Filters "MailboxContent_Received -ge '01-01-2015' -and MailboxContent_Received -le '12-31-2015'" -Action All
```
   
앞의 예와 마찬가지로 이 예에서는 2015년에 마지막으로 변경된 문서에 대해서만 모든 콘텐츠 검색 작업을 수행하도록 제한합니다.

```
New-ComplianceSecurityFilter -FilterName DocumentDateRestrictionFilter -Users donh@contoso.com -Filters "SiteContent_LastModifiedTime -ge '01-01-2015' -and SiteContent_LastModifiedTime -le '12-31-2015'" -Action All
```
   
이 예에서는 조직의 모든 사서함에 콘텐츠 검색 작업을 수행 하는에서 "OneDrive 검색 관리자" 역할 그룹의 구성원 수 없습니다. 

```
New-ComplianceSecurityFilter -FilterName NoEXO -Users "OneDrive Discovery Managers" -Filters "Mailbox_Alias -notlike '*'"  -Action All
```
  
## <a name="get-compliancesecurityfilter"></a>Get-ComplianceSecurityFilter

**Get ComplianceSecurityFilter** 검색 권한 필터의 목록을 반환 하는 데 사용 됩니다. _FilterName_ 매개 변수를 사용 하 여 특정 검색 필터에 대 한 정보를 반환 합니다. 
  
## <a name="set-compliancesecurityfilter"></a>집합 ComplianceSecurityFilter

**집합 ComplianceSecurityFilter** 은 기존 검색 권한 필터를 수정 하는데 사용 됩니다. 유일한 필수 매개 변수는 _FilterName_합니다. 
  
|**매개 변수**|**설명**|
|:-----|:-----|
| _다중값 속성에서 하나 이상의 값 제거_| _Action_ 매개 변수는 해당 필터에 적용 되는 검색 작업 유형을 지정 합니다. 가능한 콘텐츠 검색 동작은 다음과 같습니다.<br/><br/> **내보내기** -필터 검색 결과 내보낼 때 적용 됩니다.  <br/> 검색 결과 미리볼 때 **미리 보기** -필터가 적용 됩니다.  <br/> 검색 결과 삭제 하는 경우 **항목 지우기** -filter가 적용 됩니다.  <br/> **검색** -필터 검색을 실행할 때 적용 됩니다.  <br/> **모든** -필터 검색 한 모든 작업이 적용 됩니다.  <br/> |
| _FilterName_|_FilterName_ 매개 변수는 사용 권한 필터의 이름을 지정합니다. |
| _필터_| _필터_ 매개 변수는 준수 보안 필터에 대 한 검색 조건을 지정합니다. 서로 다른 두 유형의 필터를 만들 수 있습니다.<br/><br/>**사서함 필터링** -이 유형의 필터 사서함을 검색할 수 있습니다 ( _사용자가_ 매개 변수에 의해 지정 된) 할당 된 사용자를 지정 합니다. 이 유형의 필터에 대 한 구문은 **Mailbox_** _MailboxPropertyName_, _MailboxPropertyName_ 범위를 검색할 수 있는 사서함에 사용 되는 사서함 속성을 지정 합니다. 사서함 필터 등 `"Mailbox_CustomAttribute10 -eq 'OttawaUsers'"` CustomAttribute10 속성에 사용자 할당이 필터 값이 포함 된 사서함을 검색 하는를 "OttawaUsers"를 허용 합니다.  지원 되는 모든 필터링 할 수 있는 받는 사람 속성 _MailboxPropertyName_ 속성에 대해 사용할 수 있습니다. 지원 되는 속성의 목록 [-RecipientFilter 매개 변수에 대 한 필터링 할 수 있는 속성](https://go.microsoft.com/fwlink/p/?LinkId=784903)을 참조 하십시오.<br/><br/>**사서함 콘텐츠 필터링**-이 유형의 필터는 검색할 수 있는 콘텐츠에 적용 됩니다. 할당 된 사용자를 검색할 수 있는 사서함 콘텐츠를 지정 합니다. 이 유형의 필터에 대 한 구문은 **MailboxContent_** _SearchablePropertyName:value_, _SearchablePropertyName_ 콘텐츠 검색에 지정할 수 있는 키워드 쿼리 언어 (KQL) 속성을 지정 합니다. 사서함 콘텐츠 필터 등 `MailboxContent_recipients:contoso.com` contoso.com 도메인의 받는 사람에 게 보내는 메시지에 대 한 검색만이 필터는 사용자에 게 할당을 사용 하면 됩니다.  검색 가능한 메시지 속성의 목록에 대 한 [콘텐츠 검색에 대 한 키워드 쿼리](keyword-queries-and-search-conditions.md)를 참조 하십시오.<br/><br/>**사이트 및 사이트 콘텐츠 필터링** 두 SharePoint와 OneDrive 할당 된 사용자가 어떤 사이트 또는 사이트 콘텐츠를 검색할 수를 지정 하는데 사용할 수 있는 비즈니스 사이트와 관련 된 필터에 대 한 <br/><br/>- **사이트 _** *SearchableSiteProperty* <br/>- **SiteContent**_*SearchableSiteProperty*<br/><br/>이러한 두 필터는 서로 바꿔서 사용할 수 있습니다. 예 `"Site_Path -like 'https://contoso.spoppe.com/sites/doctors*'"` 및 `"SiteContent_Path -like 'https://contoso.spoppe.com/sites/doctors*'"` 동일한 결과 반환 합니다. 사용할 수 있는 필터를 수행 하는 작업을 식별할 수 있도록, 하지만 `Site_` 사이트와 관련 된 속성 (예: 사이트 URL)을 지정 하려면 및 `SiteContent_` (예: 문서 형식 콘텐츠 관련 속성을 지정 하려면. 필터 등 `"Site_Path -like 'https://contoso.spoppe.com/sites/doctors*'"` 만의 콘텐츠를 검색 하려면이 필터는 사용자에 게 할당을 사용 하면는 https://contoso.spoppe.com/sites/doctors 사이트 모음입니다. 필터 `"SiteContent_FileExtension -eq 'docx'"` Word 문서 (Word 2007 이상)에 대 한 검색만이 필터는 사용자에 게 할당을 사용 하면 됩니다.<br/><br/>검색 가능한 사이트 속성의 목록에 대 한 [크롤링 속성 및 관리 SharePoint에서 속성의 개요를](https://go.microsoft.com/fwlink/p/?LinkId=331599)참조 합니다. 사이트 또는 사이트 콘텐츠 필터를 만들려면 **예** **쿼리 가능** 열에 표시 하는 속성을 사용할 수 있습니다.<br/><br/> **중요:** 단일 검색 필터는 한 가지 유형의 필터;를 하나만 사용할 수 있습니다. 사서함 필터와 사이트 필터; 포함할 수 없습니다. 마찬가지로, 사서함 필터 및 사서함 콘텐츠 필터를 포함할 수 없습니다. 그러나 필터 같은 종류의 보다 복잡 한 쿼리를 포함할 수 있습니다. 예를 들어`"Mailbox_CustomAttribute10 -eq 'FTE' -and Mailbox_MemberOfGroup -eq '$($DG.DistinguishedName)'"`          |
| _사용자_|_사용자가_ 매개 변수는 해당 되는 콘텐츠 검색에 적용 된이 필터를 가져올 사용자를 지정 합니다. 다중값 속성 이기 때문에이 매개 변수와 함께 사용자 또는 사용자 그룹을 지정 하는 기존 사용자 목록이 덮어쓰게 됩니다. 선택한 사용자 추가 및 제거에 대 한 구문에 대 한 다음 예를 참조 하십시오.<br/><br/>보안을 지정 하려면 _사용자가_ 매개 변수를 사용할 수도 있습니다 &amp; 준수 센터 역할 그룹입니다. 검색 사용 권한 필터를 그룹화 하는이 사용자 지정 역할 그룹을 만들고 다음 해당 역할을 할당을이 사용 합니다. 등의 여러 국가 corporation 미국 자회사 eDiscovery 관리자에 대 한 사용자 지정 역할 그룹을 해야 가정해 보겠습니다. (사용 하 여 역할 그룹의 Name 속성)이 역할 그룹을 지정 하 고 다음 _Filter_ 매개 변수를 사용 하 여 검색할 미국에서 사서함만 허용 하려면 _사용자가_ 매개 변수를 사용할 수 있습니다.<br/><br/>이 매개 변수로 메일 그룹을 지정할 수는 없습니다. |

## <a name="examples-of-changing-search-permissions-filters"></a>검색 사용 권한 필터를 변경의 예

이러한 예를 추가 하 여 필터에 할당 된 사용자의 기존 목록에 사용자를 제거 **하면 ComplianceSecurityFilter** 및 **집합 ComplianceSecurityFilter** cmdlet을 사용 하는 방법을 보여줍니다. 를 추가 하거나 필터에서 사용자를 제거할 때 해당 SMTP 주소를 사용 하 여 사용자를 지정 합니다. 
  
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
  
## <a name="remove-compliancesecurityfilter"></a>ComplianceSecurityFilter 제거

**제거 ComplianceSecurityFilter** 검색 필터를 삭제 하는 데 사용 됩니다. _FilterName_ 매개 변수를 사용 하 여 삭제할 필터를 지정 합니다. 
  
## <a name="more-information"></a>추가 정보

- **어떻게 작업을 필터링 하는 사용 권한에서 검색?** 사용 권한 필터는 콘텐츠 검색을 실행 하는 경우 검색 쿼리에 추가 됩니다. 사용 권한 필터는 기본적으로 **AND** 부울 연산자가 검색 쿼리를 연결 됩니다. 예, 근로자가 메일 그룹의 구성원의 사서함에서 모든 검색 작업을 수행 하는 Bob 수 있게 하는 사용 권한 필터가 있는 라고 표시 합니다. 검색 쿼리를 사용 하 여 조직에서 모든 사서함에 대 한 콘텐츠 검색을 실행 하는 Bob 다음 `sender:jerry@adatum.com`합니다. 사용 권한 필터 및 검색 쿼리는 **AND** 연산자가 논리적으로 결합 되 면 때문에 검색 jerry@adatum.com 근로자가 메일 그룹의 모든 구성원에 게 보낸 모든 메시지가 반환 됩니다. 
    
- **여러 검색 권한 필터를 설정한 경우 어떻게 됩니까?** 콘텐츠 검색 쿼리에서 여러 사용 권한 필터 **또는** 부울 연산자와 변수와 됩니다. 따라서 필터 중 하나에 해당 하는 경우 결과 반환 됩니다. 콘텐츠 검색에서 ( **또는** 연산자로 결합) 필터를 모두 검색 쿼리와 **AND** 연산자에 의해 결합 다음 됩니다. 알아보겠습니다 앞의 예제에서는 검색 필터에서 Bob만 근로자가 메일 그룹의 구성원의 사서함을 검색할 수를 사용 하는 위치입니다. 그런 다음 Bob 필의 사서함 ("Mailbox_Alias-ne 'Phil'")를 검색 하는 것을 금지 하는 다른 필터를 만듭니다. 또한 여러분이 Phil 작업자 그룹의 구성원 인지 하 고 있습니다. Bob을 실행 하면 콘텐츠 검색 (앞의 예제)에서 조직의 모든 사서함에서 검색 결과 필의 사서함 검색에서 Bob을 방지 하기 위해 필터를 적용 하는 경우에 필의 사서함에 대 한 반환 됩니다. 작업자 그룹을 검색 하려면 Bob을 허용 하는 첫번째 필터 참이 때문입니다. 및 Bob 필의 사서함을 검색할 수 Phil 작업자 그룹의 구성원은 이기 때문에. 
    
- **에서 비활성 사서함에 대 한 작업을 필터링 하는 사용 권한을 검색?** 예, 조직에서 비활성 사서함을 검색할 수 있는 제한 하려면 사서함 및 사서함 콘텐츠 필터를 사용할 수 있습니다. 일반 사서함 처럼 비활성 사서함 사용 권한 필터를 만드는 사용 되는 받는 사람 속성을 사용 하 여 구성 하는 합니다. 필요한 경우 비활성 사서함의 속성을 표시 하려면 **Get-mailbox InactiveMailboxOnly** 명령을 사용할 수 있습니다. 자세한 내용은 참조 [만들기 및 Office 365에서 비활성 사서함 관리](create-and-manage-inactive-mailboxes.md)합니다.
    
- **공용 폴더에 대 한 작업을 필터링 하는 사용 권한에서 검색?** 아니요. Exchange 공용 폴더를 검색할 수 있는 필터링 하는 사용 권한을 제한 하는데 사용할 수 없습니다 앞에서 설명한 것을 검색 합니다. 예, 사용 권한 필터에 의해 공용 폴더 위치에 있는 항목을 검색 결과에서 제외할 수 없습니다. 
    
- **특정 서비스의 모든 콘텐츠 위치를 검색 하는 사용자 수 있도록 설정도 사용할 수 없게 하는 서로 다른 서비스의 콘텐츠 위치를 검색에서?** 아니요. 앞에서 설명한 것 처럼 명시적으로 (예: 모든 Exchange 사서함 또는 모든 SharePoint 사이트를 검색에서 사용자를 방지) 특정 Office 365 서비스에서 콘텐츠 위치를 검색에서 사용자를 방지 하기 위해 검색 권한 필터를 만드는 해야 합니다. 즉, 조직에서 모든 SharePoint 사이트를 검색 하는 사용자 수 있게 하는 검색 사용 권한 필터를 만드는 사서함 검색에서 해당 사용자를 방지 하지 않습니다. 예, SharePoint 관리자가 SharePoint 사이트를 검색 하는 수 있도록 해야 사서함 검색을 금지 하는 필터를 만든 다음 만든. 마찬가지로, Exchange 관리자만 사서함을 검색할 수 있도록 해야 만들려면 사이트 검색을 금지 하는 필터를 만들 수 있습니다.
