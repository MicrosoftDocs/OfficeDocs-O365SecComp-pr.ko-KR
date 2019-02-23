---
title: Office 365 보안 &amp; 및 준수 센터에서 eDiscovery 권한 할당
ms.author: markjjo
author: markjjo
manager: laurawi
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MOE150
- MET150
ms.assetid: 5b9a067b-9d2e-4aa5-bb33-99d8c0d0b5d7
description: 보안 &amp; 및 준수 센터를 사용 하 여 eDiscovery 관련 작업을 수행 하는 데 필요한 사용 권한을 할당 합니다.
ms.openlocfilehash: c4dcbf51282aa2887fd7d5032eb8587b5e9d56d7
ms.sourcegitcommit: a80bd8626720fabdf592b84e4424cd3a83d08280
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30223277"
---
# <a name="assign-ediscovery-permissions-in-the-office-365-security-amp-compliance-center"></a>Office 365 보안 &amp; 및 준수 센터에서 eDiscovery 권한 할당

사용자가 Office 365 보안 &amp; 및 준수 센터에서 eDiscovery 관련 도구 중 하나를 사용 하 게 하려면 적절 한 사용 권한을 할당 해야 합니다. 이 작업을 수행 하는 가장 쉬운 방법은 Office 365 보안 &amp; 및 준수 센터의 **사용 권한** 페이지에서 해당 역할 그룹에 해당 하는 사람을 추가 하는 것입니다. 이 항목에서는 보안 &amp; 및 준수 센터를 사용 하 여 eDiscovery 관련 작업을 수행 하는 데 필요한 사용 권한에 대해 설명 합니다. 
  
보안 &amp; 및 준수 센터의 기본 ediscovery 관련 역할 그룹을 **eDiscovery 관리자**라고 합니다. 이 역할 그룹에는 두 개의 하위 그룹이 있습니다. 
  
- **ediscovery** 관리자-ediscovery Manager가 보안 &amp; 준수 센터의 콘텐츠 검색 도구를 사용 하 여 조직의 콘텐츠 위치를 검색 하 고 미리 보기 및 내보내기 검색과 같은 다양 한 검색 관련 작업을 수행할 수 있습니다. 검색. 또한 구성원은 eDiscovery 사례를 만들고 관리 하 고, 사례에 구성원을 추가 및 제거 하 고, 사례 보류를 만들고, 사례와 연결 된 콘텐츠 검색을 실행 하 고, Office 365 Advanced eDiscovery에서 사례 데이터에 액세스할 수 있습니다.  eDiscovery 관리자는 자신이 만드는 사례에 액세스 하 고 관리만 할 수 있습니다. 다른 eDiscovery 관리자가 만든 사례에 액세스 하거나 관리할 수 없습니다. 
    
- **ediscovery** 관리자-ediscovery 관리자는 ediscovery 관리자 역할 그룹의 구성원이 며, ediscovery 관리자가 수행할 수 있는 동일한 콘텐츠 검색 및 사례 관리 관련 작업을 수행할 수 있습니다. 또한 eDiscovery 관리자는 다음 작업을 수행할 수 있습니다. 
    
  - 보안 &amp; 및 준수 센터의 **eDiscovery 사례** 페이지에 나열 된 모든 경우에 액세스 합니다. 

  - 조직의 모든 경우에 대 한 고급 eDiscovery의 사례 데이터 액세스
    
  - 본인을 사례의 구성원으로 추가한 후에 eDiscovery 사례를 관리합니다.
  
  조직에서 eDiscovery 관리자가 필요한 이유는 [추가 정보](#more-information) 섹션을 참조 하십시오. 

> [!NOTE]
> 고급 eDiscovery를 사용 하 여 사용자 데이터를 분석 하려면 데이터의 custodian 사용자에 게 Office 365 E5 라이선스를 할당 해야 합니다. 또는 Office 365 E1 또는 E3 라이선스를 사용 하는 사용자에 게 고급 eDiscovery 독립 실행형 라이선스를 할당할 수 있습니다. 서비스 케이스에 할당 되 고 고급 eDiscovery를 사용 하 여 데이터를 분석 하는 관리자 및 규정 준수 직원은 E5 라이선스가 필요 하지 않습니다.  
  
## <a name="before-you-begin"></a>시작하기 전에

- 보안 &amp; 및 준수 센터에서 eDiscovery 권한을 할당 하려면 조직 관리 역할 그룹의 구성원 이거나 역할 관리 역할을 할당 받아야 합니다.
    
- 보안 &amp; 및 준수 센터 PowerShell의 [추가-rolegroupmember](https://technet.microsoft.com/en-us/library/dd638207%28v=exchg.160%29.aspx) cmdlet을 사용 하 여 메일 사용이 가능한 보안 그룹을 ediscovery 관리자 역할 그룹의 ediscovery 관리자 그룹 구성원으로 추가할 수 있습니다. 그러나 메일 사용이 가능한 보안 그룹은 eDiscovery Administrators 그룹에 추가할 수 없습니다. 자세한 [내용은 추가 정보](#more-information) 섹션을 참조 하세요. 
    
## <a name="assign-ediscovery-permissions-in-the-security-amp-compliance-center"></a>보안 &amp; 및 준수 센터에서 eDiscovery 권한 할당

1. [https://protection.office.com](https://protection.office.com)으로 이동합니다.
    
2. 회사 또는 학교 계정을 사용하여 Office 365에 로그인합니다.
    
3. 보안 &amp; 및 준수 센터의 왼쪽 창에서 **사용 권한을**클릭 하 고 **eDiscovery Manager**옆에 있는 확인란을 클릭 합니다.
    
4. **ediscovery 관리자** 플라이 아웃 페이지에서 할당 하려는 eDiscovery 권한에 따라 다음 중 하나를 수행 합니다. 
    
  - **사용자를 eDiscovery 관리자로 설정 하려면** **eDiscovery 관리자**옆에 있는 **편집**을 클릭 합니다. **선택한 eDiscovery 관리자**에서 **편집**, 아이콘 ![](media/ITPro-EAC-AddIcon.gif) **** 추가 추가를 차례로 클릭 합니다. eDiscovery 관리자로 추가할 사용자 (또는 사용자)를 선택한 다음 **추가**를 클릭 합니다. 사용자 추가가 완료 되 면 **완료**를 클릭 합니다. 그런 다음 **ediscovery 관리자** 플라이 아웃 선택 페이지에서 **저장** 을 클릭 하 여 ediscovery 관리자 멤버 자격에 대 한 변경 내용을 저장 합니다. 
    
  - **사용자를 eDiscovery 관리자로 설정 하려면** **eDiscovery 관리자**옆에 있는 **편집**을 클릭 합니다. **선택한 eDiscovery 관리자**에서 **편집**, 아이콘 ![](media/ITPro-EAC-AddIcon.gif) **** 추가 추가를 차례로 클릭 합니다. eDiscovery 관리자로 추가할 사용자 (또는 사용자)를 선택한 다음 **추가**를 클릭 합니다. 사용자 추가가 완료 되 면 **완료**를 클릭 합니다. 그런 다음 **ediscovery 관리자** 플라이 아웃 선택 페이지에서 **저장** 을 클릭 하 여 ediscovery 관리자 멤버 자격에 대 한 변경 내용을 저장 합니다. 
    
> [!NOTE]
> **eDiscoveryCaseAdmin** cmdlet을 사용 하 여 사용자를 eDiscovery 관리자로 설정할 수도 있습니다. 그러나이 cmdlet을 eDiscovery 관리자로 설정 하려면 사용자에 게 사례 관리 역할을 할당 받아야 합니다. 자세한 내용은 [Add-eDiscoveryCaseAdmin](https://go.microsoft.com/fwlink/p/?LinkID=798217)를 참조 하세요. 
  
보안 &amp; 및 준수 센터의 **사용 권한** 페이지에서는 사용자 eDiscovery 관련 사용 권한을 규정 준수 관리자, 조직 관리 및 검토자 역할 그룹에 추가 하 여 할당할 수도 있습니다. 이러한 각 역할 그룹에 할당 된 eDiscovery 관련 rbac 역할에 대 한 자세한 내용은 [eDiscovery와 관련 된 rbac 역할](#rbac-roles-related-to-ediscovery) 섹션을 참조 하십시오. 

## <a name="rbac-roles-related-to-ediscovery"></a>eDiscovery와 관련 된 RBAC 역할

다음 표에서는 보안 & 준수 센터의 eDiscovery 관련 RBAC 역할을 나열 하 고 각 역할이 기본적으로 할당 되는 기본 제공 역할 그룹을 나타냅니다. 
    
|**역할**|**준수 관리자**|**eDiscovery 관리자 & 관리자**|**조직 관리**|**Reviewer**|
|:-----|:-----:|:-----:|:-----:|:-----:|
|사례 관리 <br/> |![확인 표시](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png) <br/> |![확인 표시](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png) <br/> |![확인 표시](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png) <br/> | <br/> |
|규격 검색 <br/> |![확인 표시](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png) <br/> |![확인 표시](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png) <br/> |![확인 표시](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png) <br/> | <br/> |
|내보내기 <br/> | <br/> |![확인 표시](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png) <br/> | <br/> | <br/> |
|보류 <br/>  |![확인 표시](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png) <br/> |![확인 표시](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png) <br/> |![확인 표시](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png) <br/> | <br/> |
|미리 보기 <br/>  | <br/> |![확인 표시](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png) <br/> | <br/> | <br/> |
|검토  <br/>  | <br/> |![확인 표시](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png) <br/> | <br/> |![확인 표시](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png) <br/> |
|RMS 암호 해독 <br/>  ||![확인 표시](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png) <br/> |||
|검색 및 제거 <br/> | <br/> | <br/> |![확인 표시](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)           <br/> | <br/> | 
||||
  
다음 섹션에서는 위의 표에 나열 된 각 eDiscovery 관련 RBAC 역할에 대해 설명 합니다.

### <a name="case-management"></a>사례 관리

이 역할을 사용 하면 사용자가 보안 & 준수 센터에서 eDiscovery 사례에 대 한 액세스를 만들고, 편집 하 고, 삭제 하 고 제어할 수 있습니다. 자세한 내용은 [Office 365 보안 &amp; 및 준수 센터에서 eDiscovery 사례 관리](manage-ediscovery-cases.md)를 참조 하세요. 앞에서 설명한 것 처럼, 사용자는 **eDiscoveryCaseAdmin** cmdlet을 사용 하 여 eDiscovery 관리자로 설정할 수 있도록 사례 관리 역할을 할당 받아야 합니다. 

### <a name="compliance-search"></a>규격 검색

이 역할을 사용 하면 사용자가 보안 & 준수 센터에서 콘텐츠 검색 도구를 실행 하 여 사서함 및 공용 폴더, SharePoint Online 사이트, 비즈니스용 OneDrive 사이트, 비즈니스용 Skype 대화, Office 365 그룹 및 Microsoft 팀을 검색할 수 있습니다. 이 역할을 사용 하면 사용자가 예상 검색 결과를 가져오고 내보내기 보고서를 만들 수 있지만 검색 결과를 미리 보거나 내보내거나 삭제 하는 등의 콘텐츠 검색 작업을 시작 하려면 추가 역할이 필요 합니다.

준수 검색 역할을 할당 했지만 미리 보기 역할을 지정 하지 않은 사용자는 미리 보기 역할이 할당 된 사용자가 미리 보기 작업을 시작한 검색 결과를 미리 볼 수 있습니다. 미리 보기 역할이 없는 사용자는 초기 미리 보기 작업을 만든 후 최대 2 주 동안 결과를 미리 볼 수 있습니다.

마찬가지로, 규정 준수 검색 역할을 할당 했지만 내보내기 역할이 할당 되지 않은 사용자가 내보내기 작업이 시작 된 검색 결과를 내보낼 수는 없습니다. 내보내기 역할이 없는 사용자는 초기 내보내기 작업을 만든 후 최대 2 주까지 검색 결과를 다운로드할 수 있습니다. 이 이후에는 내보내기 역할을 가진 사용자가 내보내기를 다시 시작 하지 않으면 결과를 다운로드할 수 없습니다.

자세한 내용은 [Office 365의 콘텐츠 검색](content-search.md)을 참조 하세요. 

### <a name="export"></a>내보내기

사용자는 역할을 사용 하 여 콘텐츠 검색의 결과를 로컬 컴퓨터로 내보낼 수 있습니다. 또한 고급 eDiscovery에서 분석에 대 한 검색 결과를 준비할 수 있습니다. 

검색 결과를 내보내는 방법에 대 한 자세한 내용은 [Export search results from the Office 365 Security & 준수 센터](export-search-results.md)를 참조 하세요.

### <a name="hold"></a>보류

사용자는이 역할을 사용 하 여 사서함, 공용 폴더, 사이트, 비즈니스용 Skype 대화 및 Office 365 그룹에 콘텐츠를 저장할 수 있습니다. 콘텐츠가 보존 되는 동안에는 콘텐츠 소유자가 원본 콘텐츠를 수정 하거나 삭제할 수는 있지만 보류를 제거 하거나 보존 기간이 만료 될 때까지 콘텐츠가 보존 됩니다. 

보류에 대 한 자세한 내용은 다음 항목을 참조 하십시오.

- [Office 365 보안 & 준수 센터의 eDiscovery 사례](ediscovery-cases.md) 
- [보존 정책 개요](retention-policies.md)

### <a name="preview"></a>미리 보기

이 역할을 통해 사용자는 콘텐츠 검색에서 반환 된 항목의 목록을 볼 수 있습니다. 또한 목록의 각 항목을 열고 콘텐츠를 볼 수 있습니다.

### <a name="review"></a>검토 

이 역할을 사용 하면 사용자가 Office 365 Advanced eDiscovery에서 사례 데이터에 액세스할 수 있습니다. 이 역할의 기본 목적은 사용자에 게 고급 eDiscovery에 대 한 액세스 권한을 부여 하는 것입니다. 이 역할이 할당 된 사용자는 보안 & 준수 센터에서 구성원 인 eDiscovery 페이지의 사례 목록을 보고 열 수 있습니다. 사용자가 Security & 준수 센터의 사례에 액세스 한 후 advanced **ediscovery로 전환을** 클릭 하 여 advanced ediscovery에서 사례 데이터에 액세스 하 고 분석할 수 있습니다. 이 역할은 사용자가 사례와 연결 된 콘텐츠 검색의 결과를 미리 보거나 기타 콘텐츠 검색 또는 사례 관리 작업을 수행 하는 것을 허용 하지 않습니다.

### <a name="rms-decrypt"></a>RMS 암호 해독

이 역할을 사용 하면 사용자가 검색 결과를 내보내거나 고급 eDiscovery에서 분석에 대 한 검색 결과를 준비할 때 RMS 암호화 전자 메일 메시지의 암호를 해독할 수 있습니다. 내보내기 중 검색 결과의 암호를 해독 하는 방법에 대 한 자세한 내용은 [export search results from the Office 365 Security & 준수 센터](export-search-results.md)를 참조 하세요.

### <a name="search-and-purge"></a>검색 및 제거

이 역할을 사용 하면 사용자가 콘텐츠 검색 조건과 일치 하는 데이터를 일괄적으로 제거할 수 있습니다. 자세한 내용은 [Office 365 조 직에서 전자 메일 메시지 검색 및 삭제](search-for-and-delete-messages-in-your-organization.md)를 참조 하세요. 


## <a name="more-information"></a>추가 정보

- **eDiscovery 관리자를 만드는 이유는 무엇 인가요?** 앞에서 설명한 것 처럼 ediscovery 관리자는 조직의 모든 ediscovery 사례를 보고 액세스할 수 있는 ediscovery 관리자 역할 그룹의 구성원 이어야 합니다. 모든 eDiscovery 사례에 액세스할 수 있는 이러한 기능에는 다음과 같은 두 가지 중요 한 용도가 있습니다. 
    
  - ediscovery 사례의 유일한 구성원 인 사용자가 조직을 벗어나면 조직 관리 역할 그룹의 구성원이 나 ediscovery 관리자 역할 그룹의 구성원을 포함 하는 아무도 구성원이 아니므로 ediscovery 사례에 액세스할 수 없습니다. 사례입니다. 이 경우에는 대/소문자에서 데이터에 액세스할 수 있는 방법이 없습니다. 그러나 ediscovery 관리자가 조직의 모든 eDiscovery 사례에 액세스할 수 있으므로 해당 사용자는 보안 &amp; 및 준수 센터에서 사례를 보고 케이스의 구성원으로 자신 또는 다른 eDiscovery 관리자를 추가할 수 있습니다.
    
  - ediscovery 관리자는 모든 ediscovery 사례를 보고 액세스할 수 있으므로 모든 사례 및 관련 준수 검색을 감사 하 고 감독 할 수 있습니다. 이를 통해 준수 검색 또는 eDiscovery 사례의 오용을 방지할 수 있습니다. 또한 ediscovery 관리자는 준수 검색 결과에서 잠재적으로 중요 한 정보에 액세스할 수 있으므로 ediscovery 관리자 인 사용자 수를 제한 해야 합니다.
    
    또한 보안 &amp; 및 준수 센터의 eDiscovery 관리자는 고급 eDiscovery의 관리자에 게 자동으로 추가 됩니다. 즉, 사용자를 설정 하 고 사례를 만들고 사례에 데이터를 가져오는 등 고급 eDiscovery에서 관리 작업을 수행 하려면 ediscovery 관리자 여야 합니다.
    
- **보안 &amp; 및 준수 센터에서 eDiscovery 관리자 역할 그룹의 구성원으로 그룹을 추가할 수 있나요?** 앞에서 설명한 것 처럼, 보안 &amp; 준수 센터 PowerShell의 **추가 기능 그룹 구성원** cmdlet을 사용 하 여 ediscovery 관리자 역할 그룹에서 메일 사용이 가능한 보안 그룹의 구성원으로이를 추가할 수 있습니다. 예를 들어 다음 명령을 실행 하 여 eDiscovery 관리자 역할 그룹에 메일 사용이 가능한 보안 그룹을 추가할 수 있습니다. 
    
  ```
  Add-RoleGroupMember "eDiscovery Manager" -Member <name of security group>
  ```

    Exchange 메일 그룹 또는 Office 365 그룹은 지원 되지 않습니다. ` New-DistributionGroup -Type Security ` 명령을 사용 하 여 Exchange Online PowerShell에서 만들 수 있는 메일 사용이 가능한 보안 그룹을 사용 해야 합니다. 또한 Exchange 관리 센터 또는 Office 365 관리 센터에서 메일 사용이 가능한 보안 그룹 (및 구성원 추가)을 만들 수 있습니다. 새 메일 사용이 가능한 보안을 eDiscovery 관리자 역할 그룹에 추가할 수 있도록 만든 후 최대 60 분이 걸릴 수 있습니다. 
    
    또한 앞에서 설명한 것 처럼, 보안 &amp; 및 준수 센터 PowerShell에서 **eDiscoveryCaseAdmin** cmdlet을 사용 하 여 메일 사용이 가능한 보안 그룹을 eDiscovery 관리자로 설정할 수 없습니다. 개별 사용자만 eDiscovery 관리자로 추가할 수 있습니다. 
    
    또한 메일 사용이 가능한 보안 그룹은 사례 구성원으로 추가할 수 없습니다.
