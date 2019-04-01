---
title: Office 365에서 eDiscovery 조사에 대한 준수 경계 설정
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
ms.assetid: 1b45c82f-26c8-44fb-9f3b-b45436fe2271
description: 준수 경계를 사용 하 여 eDiscovery 관리자가 검색할 수 있는 사용자 콘텐츠 위치를 제어 하는 Office 365 조직 내에 논리적 경계를 만듭니다. 준수 경계는 검색 권한 필터링 (규정 준수 보안 필터 라고도 함)을 사용 하 여 특정 사용자가 검색할 수 있는 사서함, SharePoint 사이트 및 OneDrive 계정을 제어 합니다.
ms.openlocfilehash: b23c6d0c96874fb7e6205de6bf8a7f4eb00e4254
ms.sourcegitcommit: 691370682825a7601bd4b77d0a8c4b51ed15682f
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/31/2019
ms.locfileid: "31014027"
---
# <a name="set-up-compliance-boundaries-for-ediscovery-investigations-in-office-365"></a>Office 365에서 eDiscovery 조사에 대한 준수 경계 설정

준수 경계는 eDiscovery 관리자가 검색할 수 있는 사용자 콘텐츠 위치 (예: 사서함, SharePoint 사이트, OneDrive 계정)를 제어 하는 Office 365 조직 내에 논리적 경계를 만듭니다. 또한 규정 준수 경계는 법률, 인적 자원 또는 조직 내 다른 조사를 관리 하는 데 사용 되는 eDiscovery 사례에 액세스할 수 있는 사용자를 제어 합니다. 지리적 boarders 및 규정을 준수 해야 하는 국내 기업에는 종종 다양 한 기관으로 분류 되는 정부에 대 한 적합성 경계가 필요 합니다. Office 365에서 준수 경계는 콘텐츠 검색을 수행 하 고 eDiscovery 사례를 통해 조사를 관리할 때 이러한 요구 사항을 충족 하는 데 도움이 됩니다.
  
다음 그림의 예를 사용 하 여 준수 경계의 작동 방식을 알아봅니다.
  
![준수 경계는 eDisocovery 사례에 대 한 액세스를 제어 하는 기관 및 관리 역할 그룹에 대 한 액세스를 제어 하는 검색 권한 필터로 구성 됩니다.](media/5c206cc8-a6eb-4d6b-a3a5-21e158791f9a.png)
  
이 예에서 Contoso b 2는 두 개의 자회사, 커피 및 Coho Winery으로 구성 되는 Office 365 조직입니다. 비즈니스에서는 eDiscovery mangers 및 investigators가 해당 에이전시에서 Exchange 사서함, OneDrive 계정 및 SharePoint 사이트만 검색할 수 있어야 합니다. 또한 ediscovery 관리자 및 investigators는 자신의 에이전시에 있는 ediscovery 사례만 볼 수 있을 뿐 이며 구성원 인 경우에만 액세스할 수 있습니다. 준수 경계가 이러한 요구 사항을 충족 하는 방식은 다음과 같습니다.
  
- 콘텐츠 검색의 검색 권한 필터링 기능은 eDiscovery 관리자 및 investigators에서 검색할 수 있는 콘텐츠 위치를 제어 합니다. 즉, eDiscovery 관리자 및 네 번째 커피 기관에 있는 investigators는 네 번째 커피 자회사의 콘텐츠 위치만 검색할 수 있음을 의미 합니다. Coho Winery 자회사에도 동일한 제한이 적용 됩니다.
    
    역할 그룹은 보안 & 준수 센터에서 eDiscovery 사례를 볼 수 있는 사용자를 제어 합니다. 즉, ediscovery 관리자 및 investigators는 해당 에이전시에서 ediscovery 사례만 볼 수 있습니다.
    
- 또한 역할 그룹은 구성원을 eDiscovery 사례에 할당할 수 있는 사용자를 제어 합니다. 즉, eDiscovery 관리자 및 investigators는 자신이 자신을 구성원 인 사례에만 구성원을 할당할 수 있음을 의미 합니다.
    
준수 경계를 설정 하는 프로세스는 다음과 같습니다.
  
[1 단계: 사용자 특성을 식별 하 여 에이전시를 정의 합니다.](#step-1-identify-a-user-attribute-to-define-your-agencies)

[2 단계: Microsoft Support가 사용자 특성을 OneDrive 계정에 동기화 하는 요청을 파일에 포함](#step-2-file-a-request-with-microsoft-support-to-synchronize-the-user-attribute-to-onedrive-accounts)

[3 단계: 각 에이전시에 대 한 역할 그룹 만들기](#step-3-create-a-role-group-for-each-agency)

[4 단계: 검색 권한 필터를 만들어 준수 경계를 적용 합니다.](#step-4-create-a-search-permissions-filter-to-enforce-the-compliance-boundary)

[5 단계: 에이전시 내 조사에 대 한 eDiscovery 사례 만들기](#step-5-create-an-ediscovery-case-for-an-intra-agency-investigations)
  
## <a name="step-1-identify-a-user-attribute-to-define-your-agencies"></a>1 단계: 사용자 특성을 식별 하 여 에이전시를 정의 합니다.

첫 번째 단계는 기관을 정의 하는 데 사용할 Azure Active Directory 특성을 선택 하는 것입니다. 이 특성은 eDiscovery 관리자가이 특성에 대 한 특정 값이 할당 된 사용자의 콘텐츠 위치만 검색 하도록 제한 하는 검색 권한 필터를 만드는 데 사용 됩니다. 예를 들어 Contoso에서 **부서** 특성을 사용 하기로 결정 한다고 가정해 보겠습니다. Coho Winery 자회사의 사용자에 대 한이 특성의 값은 다음과 `FourthCoffee` 같습니다 `CohoWinery`. 4 단계에서는이 `attribute:value` 쌍 (예 *: FourthCoffee* )을 사용 하 여 eDiscovery 관리자가 검색할 수 있는 사용자 콘텐츠 위치를 제한 합니다. 
  
다음은 준수 경계에 사용할 수 있는 Azure Active Directory 사용자 특성 목록입니다.
  
- Company
    
- CustomAttribute1-CustomAttribute15
    
- 부서
    
- 사무실

- C (두 문자 국가 코드)
    
더 많은 사용자 특성을 사용할 수 있지만 (특히 Exchange 사서함의 경우) 위에 나열 된 특성도 현재 OneDrive에서 지원 됩니다.
  
## <a name="step-2-file-a-request-with-microsoft-support-to-synchronize-the-user-attribute-to-onedrive-accounts"></a>2 단계: Microsoft Support가 사용자 특성을 OneDrive 계정에 동기화 하는 요청을 파일에 포함

다음 단계에서는 1 단계에서 선택한 Azure Active Directory 특성을 조직의 모든 OneDrive 계정으로 동기화 하는 Microsoft 지원 서비스에 파일을 요청 합니다. 이 동기화가 수행 되 면 1 단계에서 선택한 특성 및 값이 SharePoint의 숨겨진 관리 속성에 매핑됩니다 `ComplianceAttribute`. 이 특성을 사용 하 여 4 단계에서 OneDrive에 대 한 검색 권한 필터를 만듭니다.
  
Microsoft 지원 서비스에 요청을 제출할 때 다음 정보를 포함 합니다.
  
- Office 365 조직의 기본 도메인 이름입니다.
    
- Azure Active Directory 특성의 이름 (1 단계)
    
- 다음은 지원 요청의 목적에 대 한 설명입니다. "비즈니스용 OneDrive에서 준수 보안 필터에 대 한 Azure Active Directory를 사용 하도록 설정 합니다." 이를 통해 요청을 구현할 Office 365 eDiscovery 엔지니어링 팀에 게 요청을 라우팅할 수 있습니다.
    
엔지니어링이 변경 되 고 특성이 OneDrive에 동기화 되 면 Microsoft Support에서 변경 된 빌드 번호와 예상 배포 날짜가 전송 됩니다. 배포 프로세스는 일반적으로 지원 요청을 제출한 후 4-6 주 정도 걸립니다.
  
 **중요:** 변경 내용이 배포 될 때까지 3 단계부터 5 단계까지 완료할 수 있습니다. 하지만 콘텐츠 검색을 실행 해도 변경 내용을 배포할 때까지 검색 권한 필터에 지정 된 OneDrive 사이트의 문서가 반환 되지 않습니다. 
  
## <a name="step-3-create-a-role-group-for-each-agency"></a>3 단계: 각 에이전시에 대 한 역할 그룹 만들기

다음 단계는 사용자의 조직과 부합 되는 보안 & 준수 센터에서 역할 그룹을 만드는 것입니다. 기본 제공 eDiscovery 관리자 그룹을 복사 하 고, 적절 한 구성원을 추가 하 고, 필요에 따라 적용 되지 않을 수 있는 역할을 제거 하 여 새 역할 그룹을 만드는 것이 좋습니다. ediscovery 관련 역할에 대 한 자세한 내용은 [Office 365 Security & 준수 센터에서 ediscovery 사용 권한 할당](assign-ediscovery-permissions.md)을 참조 하십시오.
  
역할 그룹을 만들려면 Security & 준수 센터의 **사용 권한** 페이지로 이동한 후 준수 경계 및 eDiscovery 사례를 사용 하 여 조사를 관리할 각 에이전시의 각 팀에 대해 역할 그룹을 만듭니다. 
  
Contoso 준수 경계 시나리오를 사용 하 여 네 개의 역할 그룹을 만들고 해당 구성원을 각각에 추가 해야 합니다.
  
- 커피 eDiscovery 관리자 4 대
    
- 네 번째 커피 Investigators
    
- Coho Winery eDiscovery 관리자
    
- Coho Winery Investigators
    

  
## <a name="step-4-create-a-search-permissions-filter-to-enforce-the-compliance-boundary"></a>4 단계: 검색 권한 필터를 만들어 준수 경계를 적용 합니다.

각 에이전시에 대해 역할 그룹을 만든 후에는 각 역할 그룹을 특정 에이전시에 연결 하는 검색 권한 필터를 만들고 준수 경계 자체를 정의 합니다. 각 에이전시에 대해 하나의 검색 권한 필터를 만들어야 합니다. 보안 권한 필터를 만드는 방법에 대 한 자세한 내용은 [콘텐츠 검색에 대 한 사용 권한 필터링 구성을](permissions-filtering-for-content-search.md)참조 하십시오.
  
준수 경계에 사용 되는 검색 권한 필터를 만드는 데 사용 되는 구문은 다음과 같습니다.

```
New-ComplianceSecurityFilter -FilterName <name of filter> -Users <role groups> -Filters "Mailbox_<Compliance attribute from Step 1>  -eq '<AttributeVale> '", "Site_ComplianceAttribute  -eq <AttributeValue>' -or Site_Path -like <SharePointURL> *'" -Action <Action >
```
  
다음은 명령의 각 매개 변수에 대 한 설명입니다.
  
-  `FilterName`-필터의 이름을 지정 합니다. 필터를 사용할 에이전시를 설명 하거나 식별 하는 이름을 사용 합니다. 
    
-  `Users`-이 필터가 수행 하는 콘텐츠 검색 작업에이 필터를 적용할 사용자 또는 그룹을 지정 합니다. 준수 경계의 경우이 매개 변수는 필터를 만드는 데 사용할 에이전시에서 3 단계에서 만든 역할 그룹을 지정 합니다. 참고 이것은 다중 값 매개 변수 이므로 쉼표로 구분 하 여 하나 이상의 역할 그룹을 포함할 수 있습니다. 
    
-  `Filters`-필터에 대 한 검색 조건을 지정 합니다. 준수 경계에는 다음 필터를 정의 합니다. 각 항목은 사용자 콘텐츠 위치에 적용 됩니다. 
    
  -  `Mailbox`- `Users` 매개 변수에 정의 된 역할 그룹이 검색할 수 있는 사서함을 지정 합니다. 준수 경계의 경우 *ComplianceAttribute* 는 1 단계에서 식별 한 특성 및 *AttributeValue* 에서 해당 에이전시를 지정 합니다. 이 필터는 역할 그룹의 구성원이 특정 에이전시의 사서함만 검색할 수 있도록 허용 합니다. 예를 `"Mailbox_Department -eq 'FourthCoffee'"` 들면입니다. 
    
  -  `Site`- `Users` 매개 변수에 정의 된 역할 그룹이 검색할 수 있는 OneDrive 계정을 지정 합니다. OneDrive 필터의 경우 실제 문자열 `ComplianceAttribute`을 사용 합니다. 이는 1 단계에서 확인 하 고 2 단계에서 제출한 지원 요청의 결과로 OneDrive 계정과 동기화 된 것과 동일한 특성에 매핑됩니다.  *AttributeValue* 는 에이전시를 지정 합니다. 이 필터는 역할 그룹의 구성원이 특정 에이전시의 OneDrive 계정만 검색할 수 있도록 허용 합니다. 예를 `"Site_ComplianceAttribute -eq 'FourthCoffee'"`들면입니다.
    
  -  `Site_Path`- `Users` 매개 변수에 정의 된 역할 그룹이 검색할 수 있는 SharePoint 사이트를 지정 합니다. *SharePointURL* 은 역할 그룹의 구성원이 검색할 수 있는 에이전시의 사이트를 지정 합니다. 예를 들어`"Site_Path -like 'https://contoso.sharepoint.com/sites/FourthCoffee*'"`
    
-  `Action`-필터가 적용 되는 준수 검색 작업의 유형을 지정 합니다. 예를 `-Action Search` 들어 `Users` 매개 변수에 정의 된 역할 그룹의 구성원이 콘텐츠 검색을 실행 하는 경우에만 필터를 적용 합니다. 이 경우 검색 결과를 내보낼 때 필터가 적용 되지 않습니다. 준수 경계의 경우 필터를 `-Action All` 모든 검색 작업에 적용 하도록 사용 합니다. 
    
    콘텐츠 검색 작업 목록은 [콘텐츠 검색에 대 한 권한 필터링 구성](permissions-filtering-for-content-search.md#new-compliancesecurityfilter)의 "new-compliancesecurityfilter" 섹션을 참조 하십시오.
    
다음은 Contoso 준수 경계 시나리오를 지원 하기 위해 만드는 두 가지 검색 권한 필터의 예입니다.
  
 **커피 4**

```
New-ComplianceSecurityFilter -FilterName "Fourth Coffee Security Filter" -Users "Fourth Coffee eDiscovery Managers", "Fourth Coffee Investigators" -Filters "Mailbox_Department -eq 'FourthCoffee'", "Site_ComplianceAttribute -eq 'FourthCoffee' -or Site_Path -like 'https://contoso.sharepoint.com/sites/FourthCoffee*'" -Action ALL
```
   
 **Coho Winery**

```
New-ComplianceSecurityFilter -FilterName "Coho Winery Security Filter" -Users "Coho Winery eDiscovery Managers", "Coho Winery Investigators" -Filters "Mailbox_Department -eq 'CohoWinery'", "Site_ComplianceAttribute -eq 'CohoWinery' -or Site_Path -like 'https://contoso.sharepoint.com/sites/CohoWinery*'" -Action ALL
```

## <a name="step-5-create-an-ediscovery-case-for-an-intra-agency-investigations"></a>5 단계: 에이전시 내 조사에 대 한 eDiscovery 사례 만들기

마지막 단계는 Security & 준수 센터에서 새 eDiscovery 사례를 만든 다음 3 단계에서 만든 역할 그룹을 사례 구성원으로 추가 하는 것입니다. 이로 인해 준수 경계를 사용 하는 경우의 두 가지 중요 한 특징이 있습니다.
  
- 사례에 추가 된 역할 그룹의 구성원만이 보안 & 준수 센터의 사례를 보고 액세스할 수 있습니다. 예를 들어, 네 번째 커피 Investigators 역할 그룹이 사례 유일한 구성원 인 경우에는 네 번째 커피 eDiscovery 관리자 역할 그룹의 구성원 또는 다른 역할 그룹의 구성원도 해당 사례를 보거나 액세스할 수 없습니다.
    
- 사례에 할당 된 역할 그룹의 구성원이 사례와 연결 된 검색을 실행 하는 경우, 해당 사용자는 해당 에이전시 (4 단계에서 만든 검색 권한 필터에 의해 정의 됨) 내의 콘텐츠 위치만 검색할 수 있습니다.


새 사례를 만들고 구성원을 할당 하려면 다음을 수행 합니다.
    
1. Security & 준수 센터의 **eDiscovery** 페이지로 이동 하 여 새 사례를 만듭니다. 
    
2. eDiscovery 사례 목록에서 방금 만든 사례 이름을 클릭 합니다.
    
3. **이 사례** 플라이 아웃 관리 페이지의 **역할 그룹**관리자에서 add 아이콘 ![](media/8ee52980-254b-440b-99a2-18d068de62d3.gif) **추가**를 클릭 합니다.
    
    ![eDiscovery 사례의 구성원으로 역할 그룹 추가](media/f8b4b557-01b9-4388-85be-b5b5ab7c5629.png)
  
4. 역할 그룹 목록에서 3 단계에서 만든 역할 그룹 중 하나를 선택 하 고 **추가**를 클릭 합니다.
    
5. **이 사례** 플라이 아웃 관리에서 **저장** 을 클릭 하 여 변경 내용을 저장 합니다. 

## <a name="compliance-boundary-limitations"></a>준수 경계 제한

eDiscovery 사례를 관리 하 고 준수 경계를 사용 하는 조사를 관리할 때는 다음과 같은 제한 사항을 염두에 두어야 합니다.
  
- 콘텐츠 검색을 만들고 실행 하는 경우에는 에이전시 외부에 있는 콘텐츠 위치를 선택할 수 있습니다. 그러나 검색 권한 필터 때문에 해당 위치의 콘텐츠가 검색 결과에 포함 되지 않습니다.
    
- 준수 경계는 eDiscovery 사례의 보류에 적용 되지 않습니다. 즉, 한 에이전시의 eDiscovery 관리자가 사용자를 보류 중인 다른 에이전시에 배치할 수 있습니다. 그러나 eDiscovery 관리자가 보류 되었던 사용자의 콘텐츠 위치를 검색 하는 경우 준수 경계가 적용 됩니다. 즉, eDiscovery 관리자는 사용자를 보류 상태로 설정할 수 있더라도 사용자의 콘텐츠 위치를 검색할 수 없습니다.
    
    또한 보유 통계는 에이전시의 콘텐츠 위치에만 적용 됩니다.
    
- 검색 사용 권한 필터는 Exchange 공용 폴더에 적용 되지 않습니다.

## <a name="searching-and-exporting-content-in-multi-geo-environments"></a>다중 지역 환경에서 콘텐츠 검색 및 내보내기

또한 검색 권한 필터를 사용 하 여 [SharePoint 다중 위치 환경](https://go.microsoft.com/fwlink/?linkid=860840)에서 콘텐츠를 검색 하는 데 사용할 수 있는 콘텐츠와 검색 되는 데이터 센터의 위치를 제어할 수 있습니다.
  
- **검색 결과 내보내기** -Exchange 사서함, SharePoint 사이트 및 OneDrive 계정에서 특정 데이터 센터의 검색 결과를 내보낼 수 있습니다. 즉, 검색 결과를 내보낼 데이터 센터 위치를 지정할 수 있습니다.

    **new-compliancesecurityfilter** 또는 **new-compliancesecurityfilter** cmdlet에 **Region** 매개 변수를 사용 하 여 내보내기가 라우팅되는 데이터 센터를 만들거나 변경 합니다.
  
    |**매개 변수 값**|**데이터 센터 위치**|
    |:-----|:-----|
    |NAM  <br/> |북미 (실제 데이터 센터는 미국)  <br/> |
    |EUR  <br/> |유럽  <br/> |
    |APC  <br/> |아시아 태평양  <br/> |
    |CAN <br/> |캐나다
    
- **콘텐츠 검색 라우팅** -SharePoint 사이트 및 OneDrive 계정의 콘텐츠 검색을 위성 데이터 센터로 라우팅할 수 있습니다. 즉, 검색을 실행할 데이터 센터 위치를 지정할 수 있습니다.
    
    SharePoint 사이트 및 OneDrive 위치를 검색할 때 콘텐츠 검색이 실행 되는 데이터 센터를 제어 하려면 **Region** 매개 변수 값으로 다음 값을 사용 합니다. 다음 표에는 라우팅되는 데이터 센터 내보내기도 나와 있습니다. 
  
    |**매개 변수 값**|**내보내기에 대 한 데이터 센터 라우팅 위치**|
    |:-----|:-----|
    |NAM  <br/> |US  <br/> |
    |EUR  <br/> |유럽  <br/> |
    |APC  <br/> |아시아 태평양  <br/> |
    |CAN  <br/> |US  <br/> |
    |AUS  <br/> |아시아 태평양  <br/> |
    |KOR  <br/> |조직의 기본 데이터 센터  <br/> |
    |GBR  <br/> |유럽  <br/> |
    |JPN  <br/> |아시아 태평양  <br/> |
    |IND  <br/> |아시아 태평양  <br/> |
    |LAM  <br/> |US  <br/> |
   
> [!NOTE]
> 검색 권한 필터에 **Region** 매개 변수를 지정 하지 않으면 조직 기본 SharePoint 지역이 검색 되 고 검색 결과가 가장 가까운 데이터 센터로 내보내집니다. 
  
다음은 준수 경계에 대 한 검색 권한 필터를 만들 때 **Region** 매개 변수를 사용 하는 예입니다. 이 경우에는 네 번째 커피 자회사를 북미에 있고 Coho Winery가 유럽에 있는 것으로 가정 합니다. 
  
```
New-ComplianceSecurityFilter -FilterName "Fourth Coffee Security Filter" -Users "Fourth Coffee eDiscovery Managers", "Fourth Coffee Investigators" -Filters "Mailbox_Department -eq 'FourthCoffee'", "Site_Department -eq 'FourthCoffee' -or Site_Path -like 'https://contoso.sharepoint.com/sites/FourthCoffee*'" -Action ALL -Region NAM
```

```
New-ComplianceSecurityFilter -FilterName "Coho Winery Security Filter" -Users "Coho Winery eDiscovery Managers", "Coho Winery Investigators" -Filters "Mailbox_Department -eq 'CohoWinery'", "Site_Department -eq 'CohoWinery' -or Site_Path -like 'https://contoso.sharepoint.com/sites/CohoWinery*'" -Action ALL -Region EUR
```
   
다중 지리적 환경에서 콘텐츠를 검색 하 고 내보낼 때는 다음 사항을 염두에 두어야 합니다.
  
- **Region** 매개 변수는 Exchange 사서함의 검색을 제어 하지 않습니다. 사서함을 검색할 때 모든 데이터 센터가 검색 됩니다. Exchange 사서함을 검색할 수 있는 범위를 제한 하려면 검색 권한 필터를 만들거나 변경할 때 **Filters** 매개 변수를 사용 합니다. 
    
- ediscovery 관리자가 여러 SharePoint 지역에서 검색 해야 하는 경우에는 검색 권한 필터에 사용할 수 있는 다른 사용자 계정을 해당 ediscovery 관리자에 게 만들어야 합니다. SharePoint 사이트 또는 OneDrive 계정이 있습니다.
    
- SharePoint 및 OneDrive에서 콘텐츠를 검색할 때 **Region** 매개 변수는 ediscovery 관리자가 ediscovery 조사를 수행 하는 기본 또는 위성 위치를 검색 하도록 지시 합니다. eDiscovery 관리자가 SharePoint 및 OneDrive 사이트 검색 사용 권한 필터에 지정 된 지역 외부를 검색 하는 경우 검색 결과가 반환 되지 않습니다. 
    
- 검색 결과를 내보낼 때 모든 콘텐츠 위치의 콘텐츠 (예를 들어 Exchange, 비즈니스용 Skype, SharePoint, OneDrive 및 기타 Office 365 서비스는 콘텐츠 검색 도구를 사용 하 여 검색할 수 있음)의 Azure 저장소 위치에 업로드 됩니다. **Region** 매개 변수에 의해 지정 된 데이터 센터입니다. 이렇게 하면 조직이 제어 테두리에 걸쳐 콘텐츠를 내보낼 수 없도록 하 여 규정 준수를 유지 하는 데 도움이 됩니다. 검색 권한 필터에 지역이 지정 되어 있지 않으면 콘텐츠가 조직의 기본 영역에 업로드 됩니다. 
    
- 다음 명령을 실행 하 여 기존 검색 권한 필터를 편집 하 여 지역을 추가 하거나 변경할 수 있습니다.

    ```
    Set-ComplianceSecurityFilter -FilterName <Filter name>  -Region <Region>
    ```
 
## <a name="frequently-asked-questions"></a>자주하는 질문

 **new-compliancesecurityfilter 및 new-compliancesecurityfilter cmdlet을 사용 하 여 검색 권한 필터를 만들고 관리할 수 있는 사람은 누구 인가요?**
  
검색 사용 권한 필터를 만들고 보고 수정 하려면 Security & 준수 센터에서 조직 관리 역할 그룹의 구성원 이어야 합니다.
  
 **여러 기관에 걸쳐 있는 둘 이상의 역할 그룹에 eDiscovery 관리자를 할당 하는 경우, 한 에이전시에서 콘텐츠를 검색 하려면 어떻게 해야 합니까?**
  
eDiscovery 관리자는 검색 쿼리에 특정 에이전시로 제한 되는 매개 변수를 추가할 수 있습니다. 예를 들어 조직에서 **CustomAttribute10** 속성을 지정 하 여 기관을 차별화 하는 경우 다음을 검색 쿼리에 추가 하 여 특정 에이전시에서 사서함 및 OneDrive 계정을 검색할 수 있습니다 `CustomAttribute10:<value> AND Site_ComplianceAttribute:<value>`.
  
 **검색 권한 필터에서 준수 특성으로 사용 되는 특성의 값이 변경 된 경우 어떻게 되나요?**
  
필터에 사용 된 특성의 값이 변경 되는 경우 검색 권한 필터에 대해 최대 3 일이 소요 됩니다. 예를 들어 Contoso 시나리오에서, 네 번째 커피 에이전시의 사용자가 Coho Winery 에이전시로 전송 된다는 것을 가정해 보겠습니다. 따라서 사용자 개체의 **부서** 특성 값은 *FourthCoffee* 에서 *CohoWinery* 로 변경 됩니다. 이 상황에서 네 번째 커피 eDiscovery 및 투자자는 해당 사용자에 대 한 검색 결과를 3 일 동안 (특성이 변경 된 후)로 가져옵니다. 마찬가지로, Coho Winery eDiscovery 관리자 및 investigators에서 사용자에 대 한 검색 결과를 가져올 때까지 최대 3 일이 걸립니다. 
  
 **eDiscovery 관리자가 두 개의 별도 준수 경계의 콘텐츠를 볼 수 있습니까?**
  
예. 이 작업은 두 기관에 모두 표시 되는 역할 그룹에 사용자를 추가 하 여 수행할 수 있습니다.
  
 **검색 사용 권한 필터가 eDiscovery 사례 보존, Office 365 보존 정책 또는 DLP에 대해 작동 하나요?**
  
아니요, 지금은 아님
  
 **콘텐츠를 내보내는 위치를 제어 하는 영역을 지정 했지만 해당 지역에 sharepoint 조직이 없는 경우에도 sharepoint를 검색할 수 있나요?**
  
검색 권한 필터에 지정 된 지역이 조직에 없는 경우에는 기본 지역이 검색 됩니다.
  
 **조직에서 만들 수 있는 검색 권한 필터의 최대 수는 얼마나 됩니까?**
  
조직에서 만들 수 있는 검색 권한 필터의 수에는 제한이 없습니다. 그러나 검색 권한 필터가 100 개 보다 많으면 검색 성능이 영향을 받습니다. 조직의 검색 권한 필터 수를 가능한 한 작게 유지 하려면 가능 하면 Exchange, SharePoint 및 OneDrive에 대 한 규칙을 단일 검색 권한 필터에 결합 하는 필터를 만듭니다.
