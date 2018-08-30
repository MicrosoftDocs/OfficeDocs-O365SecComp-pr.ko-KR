---
title: Office 365 보안에서 eDiscovery 사용 권한을 할당 &amp; 준수 센터
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 3/22/2018
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MOE150
- MET150
ms.assetid: 5b9a067b-9d2e-4aa5-bb33-99d8c0d0b5d7
description: 보안을 사용 하 여 eDiscovery 관련 작업을 수행 하는 데 필요한 사용 권한을 할당 &amp; 준수 센터입니다.
ms.openlocfilehash: 96434655dbb7bc9145406ccb6e2c70d36c448928
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22533388"
---
# <a name="assign-ediscovery-permissions-in-the-office-365-security-amp-compliance-center"></a>Office 365 보안에서 eDiscovery 사용 권한을 할당 &amp; 준수 센터

Office 365 보안의 eDiscovery 관련 도구 중 하나를 사용 하 여 사용자를 원하는 경우 &amp; 준수 센터에 적절 한 사용 권한을 할당 해야 합니다. 이 작업을 수행 하는 것이 가장 편리 방법은 Office 365 보안의 **사용 권한** 페이지에서 사용자는 적절 한 역할 그룹을 추가 하는 &amp; 준수 센터입니다. 이 항목에서는 보안을 사용 하 여 eDiscovery 관련 작업을 수행 하는 데 필요한 사용 권한을 설명 &amp; 준수 센터입니다. 
  
보안의 기본 eDiscovery와 관련 된 역할 그룹은 &amp; 준수 센터 **eDiscovery 관리자**라고 합니다. 이 역할 그룹 내에서 두 하위 그룹이 있습니다. 
  
- **eDiscovery 관리자** -eDiscovery 관리자 보안에서 콘텐츠 검색 도구를 사용할 수 &amp; 는 조직에서 콘텐츠 위치를 검색 하 고 미리 보기 등의 다양 한 검색 관련 작업을 수행 하 고 검색 내보내기에 준수 센터 결과입니다. 구성원 수도 및 eDiscovery 사례 관리, 추가 하 고 사례에 구성원을 제거, 사례 보류 만들기 만들고 사례와 연결 된 콘텐츠 검색을 실행 합니다. EDiscovery 관리자만 액세스할 수 있는 만들 사례 및 관리 합니다. 액세스 하거나 관리할 수는 없습니다의 경우 다른 eDiscovery 관리자 하 여 만듭니다. 
    
- **eDiscovery 관리자** -eDiscovery 관리자 eDiscovery 관리자 역할 그룹의 구성원 및 동일한 콘텐츠 검색 및 eDiscovery 관리자가 수행할 수 있는 사례 관리 관련 작업을 수행할 수 있습니다. 또한 eDiscovery 관리자가 다음과 같은 작업을 수행할 수 있습니다. 
    
  - 보안에서 **eDiscovery 사례** 페이지에 나열 된 모든 경우에 액세스 &amp; 준수 센터입니다. 
    
  - 본인을 사례의 구성원으로 추가한 후에 eDiscovery 사례를 관리합니다.
    
  - 사용자 설정의 경우 만들기 (영문), 데이터 가져오기 (영문) 등의 고급 eDiscovery의 관리 작업을 수행 합니다. 이런 현상이 발생 eDiscovery 관리자는 보안에 있는 사람이 &amp; 준수 센터의 고급 eDiscovery 관리자 권한으로 자동으로 추가 됩니다.
    
  > [!NOTE]
    > 고급 eDiscovery를 사용 하 여 사용자의 데이터를 분석 하려면 (데이터의 더불어) 사용자는 Office 365 E5 라이선스를 할당 합니다. 또는 Office 365 E1 또는 E3 라이선스를 사용 하는 사용자의 고급 eDiscovery 독립 실행형 라이선스를 할당할 수 있습니다. 관리자 및 규정 준수 관리자의 경우에 할당 된 및 고급 eDiscovery를 사용 하 여 데이터를 분석 하 게 e 5 라이선스가 필요는 없습니다. 
  
    이유가 있습니다 eDiscovery 관리자가 조직에서에 대 한 [자세한 내용](#more-information) 은 섹션을 참조 하십시오. 
    
## <a name="before-you-begin"></a>시작하기 전에

- 조직 관리 역할 그룹의 구성원 이어야 합니다 (또는 역할 관리 역할을 할당 받을) 해야하는 보안에서 eDiscovery 사용 권한을 할당할 &amp; 준수 센터입니다.
    
- [Add-rolegroupmember](https://technet.microsoft.com/en-us/library/dd638207%28v=exchg.160%29.aspx) cmdlet을 사용 하 여 보안에 수 &amp; eDiscovery 관리자 역할 그룹에서 eDiscovery 관리자 하위 그룹의 구성원으로 메일 사용이 가능한 보안 그룹을 추가 하려면 준수 센터 PowerShell 합니다. 그러나 eDiscovery 관리자 하위 그룹에는 메일 사용이 가능한 보안 그룹을 추가할 수 없습니다. 자세한 내용은 [자세한 정보](#more-information) 섹션을 참조 하십시오. 
    
## <a name="assign-ediscovery-permissions-in-the-security-amp-compliance-center"></a>보안에서 eDiscovery 사용 권한을 할당 &amp; 준수 센터

1. 이동 [https://protection.office.com](https://protection.office.com)합니다.
    
2. 작업이 나 교육용 계정을 사용 하 여 Office 365에 로그인 합니다.
    
3. 보안의 왼쪽된 창에서 &amp; 준수 센터 **사용 권한**, 클릭 한 다음 **eDiscovery 관리자**옆에 있는 확인란을 클릭 합니다.
    
4. **EDiscovery 관리자** 플라이 아웃 페이지에서 eDiscovery 사용 권한을 할당 하려는에 따라 다음 중 하나를 수행 합니다. 
    
  - **EDiscovery 관리자 사용자를 만들려면** **EDiscovery 관리자**옆에 있는 **편집**을 클릭 합니다. **선택한 eDiscovery 관리자**아래에서 **편집**을 클릭 하 고 다음을 클릭 ![아이콘 추가](media/ITPro-EAC-AddIcon.gif) **추가**합니다. 사용자 (또는 사용자)를 선택 eDiscovery 관리자로 추가 한 다음 **추가**클릭 합니다. 사용자 추가 (영문)이 끝나면 **완료**를 클릭 합니다. 그런 다음, **선택 편집 eDiscovery 관리자** 플라이 아웃 페이지에서 eDiscovery 관리자 구성원 자격의 변경 내용을 저장 하려면 **저장** 를 클릭 합니다. 
    
  - **EDiscovery 관리자가 사용자를 만들려면** **EDiscovery 관리자**옆에 있는 **편집**을 클릭 합니다. **선택한 eDiscovery 관리자**아래에서 **편집**을 클릭 하 고 다음을 클릭 ![아이콘 추가](media/ITPro-EAC-AddIcon.gif) **추가**합니다. 사용자 (또는 사용자)를 선택 하는 ediscovery 관리자를 추가 하 고 **추가**클릭 한 다음 원하는 합니다. 사용자 추가 (영문)이 끝나면 **완료**를 클릭 합니다. 그런 다음, **선택 편집 eDiscovery 관리자** 플라이 아웃 페이지에서 eDiscovery 관리자 구성원 자격의 변경 내용을 저장 하려면 **저장** 를 클릭 합니다. 
    
> [!NOTE]
> EDiscovery 관리자가 사용자를 만들려면 **추가 eDiscoveryCaseAdmin** cmdlet을 사용할 수도 있습니다. 그러나 사용자 역할을 할당 해야는 사례 관리 eDiscovery 관리자에이 cmdlet을 사용할 수 있습니다. 자세한 내용은 [추가 eDiscoveryCaseAdmin](https://go.microsoft.com/fwlink/p/?LinkID=798217)를 참조 하십시오. 
  
보안에서 **사용 권한** 페이지에서 &amp; 준수 센터를 할당할 수도 있습니다 사용자 권한을 eDiscovery 관련 규정 준수 관리자, 조직 관리 및 검토자 역할 그룹에 추가 하 여 합니다. 이러한 각 역할 그룹에 할당 된 eDiscovery와 관련 된 역할의 목록에 대 한 [자세한 내용](#more-information) 은 섹션을 참조 합니다. 
  
## <a name="more-information"></a>추가 정보

- **보안에서 eDiscovery 관련 된 역할은 무엇입니까 &amp; 준수 센터?** 다음 표에서 보안에서 eDiscovery 관련 된 역할에 설명 &amp; 준수 센터 기본적으로 각 역할에 할당 된 기본 제공 역할 그룹을 나타냅니다. 
    
|**역할**|**준수 관리자**|**eDiscovery 관리자 &amp; 관리자**|**조직 관리**|**Reviewer**|
|:-----|:-----|:-----|:-----|:-----|
|**사례 관리** <br/> 만들기, 편집, 삭제 및 보안에서 eDiscovery 사례에 대 한 액세스를 제어할 수 있도록 &amp; 준수 센터입니다. 자세한 내용은 참조 [Office 365 보안에서 eDiscovery 사례 관리 &amp; 준수 센터](manage-ediscovery-cases.md)합니다.<br/> 앞에서 설명한 것 처럼 사용자 할당 되어야 합니다 사례 관리 역할에 eDiscovery 관리자 **추가 eDiscoveryCaseAdmin** cmdlet을 사용할 수 있습니다.  <br/> |![확인 표시](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)           <br/> |![확인 표시](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)           <br/> |![확인 표시](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)           <br/> | <br/> |
|**규격 검색** <br/> 사용자가 보안에서 콘텐츠 검색 도구를 실행할 수 있도록 &amp; 준수 센터 사서함 및 공용 폴더, 비즈니스 사이트에 대 한 OneDrive, 비즈니스 대화, Office 365 그룹 및 팀이 Microsoft Skype SharePoint Online 사이트를 검색 합니다. 이 역할을 예상 검색 결과 가져오고 내보내기 보고서를 만들 사용자 수는 있지만 추가 역할 미리 보기, 내보내기, 또는 검색 결과 삭제 하는 등의 콘텐츠 검색 작업을 시작 하는데 사용 됩니다.<br/><br/>사용자 준수 검색 역할을 할당 이지만 미리 보기 역할 없는 미리 보기 동작이 미리 보기 역할에 할당 하는 사용자가 시작 된 하는 검색의 결과 미리볼 수 있습니다. 미리 보기 역할 없는 사용자 초기 미리 보기 작업 만들어진 후에 최대 2 주에 대 한 결과 미리볼 수 있습니다.<br/><br/> 마찬가지로 준수 검색 역할을 할당 하는 사용자 수 있지만 역할 내보내기 역할에 할당 하는 사용자가 내보내기 작업에 시작 하는 검색의 결과 다운로드할 수 있는 내보내기 필요는 없습니다. 내보내기 역할 없는 사용자의 초기 내보내기 작업을 만든 후 최대 2 주에 대 한 검색 결과 다운로드할 수 있습니다. 그 다음 내보내기 역할을 가진 사람이 내보내기를 다시 시작 하지 않는 한 결과 다운로드 하는 것이 수 없습니다.<br/><br/>자세한 내용은 [Office 365에서 콘텐츠 검색](content-search.md)을 참조 하십시오.  <br/> |![확인 표시](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)           <br/> |![확인 표시](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)           <br/> |![확인 표시](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)           <br/> | <br/> |
|**내보내기** <br/> 로컬 컴퓨터에 콘텐츠 검색의 결과 내보낼 수 있도록 합니다. 고급 eDiscovery에 대 한 분석을 위해 검색 결과 준비 하 수 있습니다.<br/> 검색 결과 내보내기 (영문) 하는 방법에 대 한 자세한 내용은 참조 [내보내기 검색 결과 Office 365 보안에서 &amp; 준수 센터](export-search-results.md)합니다.  <br/> | <br/> |![확인 표시](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)           <br/> | <br/> | <br/> |
|**보류** <br/>  사서함, 공용 폴더, 사이트, Skype 비즈니스 대화 및 보류에서 Office 365 그룹에 대 한 콘텐츠를 배치할 수 있도록 합니다. 보류에 콘텐츠가 있는 경우 콘텐츠 소유자는 여전히을 수정 하거나 원래 콘텐츠를 삭제할 수 있지만 콘텐츠 보존이 제거 하거나 보존 기간이 만료 될 때까지 유지 됩니다.<br/>  보류에 대 한 자세한 내용은 다음을 참조 합니다.  <br/> [Office 365 보안에서 eDiscovery 사례 관리 &amp; 준수 센터](manage-ediscovery-cases.md) <br/> [보존 정책 개요](retention-policies.md) <br/> |![확인 표시](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)           <br/> |![확인 표시](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)           <br/> |![확인 표시](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)           <br/> | <br/> |
|**미리 보기** <br/> 콘텐츠 검색에서 반환 된 항목의 목록을 볼 수 있도록 합니다. 이러한 수를 열고 해당 콘텐츠를 보려면 목록에서 각 항목을 봅니다.<br/> | <br/> |![확인 표시](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)           <br/> | <br/> | <br/> |
|**검토** <br/> 사용자가 참조 하 고 보안에서 eDiscovery 페이지 사례의 목록을 엽니다 수 있도록 &amp; 준수 센터의 멤버인입니다. 이러한 다른 사례 관리 작업을 수행할 수 없습니다.<br/> | <br/> |![확인 표시](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)           <br/> | <br/> |![확인 표시](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)           <br/> |
|**RMS 암호 해독** <br/> 고급 eDiscovery의 결과 나 분석을 위해 준비 검색 결과 검색 내보내기 (영문) 하는 경우 RMS 암호화 된 전자 메일 메시지를 해독할 수 있도록 합니다. 내보내는 동안 검색 결과 암호를 해독 하는 방법에 대 한 자세한 내용은 참조 [내보내기 검색 결과 Office 365 보안에서 &amp; 준수 센터](export-search-results.md)합니다.<br/> ||![확인 표시](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)           <br/> |||
|**검색 및 삭제** <br/> 콘텐츠 검색 조건과 일치 하는 데이터의 대량 제거를 수행할 수 있도록 합니다. 자세한 내용은 [Office 365 조직에서 전자 메일 메시지를 삭제 하 고 검색에 대 한](search-for-and-delete-messages-in-your-organization.md)를 참조 하십시오.<br/> | <br/> | <br/> |![확인 표시](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)           <br/> | <br/> |
   
- **이유 관리자가 eDiscovery 검색 만들기?** 앞부분에 설명에, eDiscovery 관리자가 확인 하 고 조직에서 모든 eDiscovery 사례에 액세스할 수 있는 eDiscovery 관리자 역할 그룹의 구성원 이어야 합니다. 모든 eDiscovery 사례에 액세스 하는이 기능은 두 중요 한 목적에 있습니다. 
    
  - 구성원 수 없기 때문에 해당 eDiscovery 사례 eDiscovery 사례의 유일한 구성원 인 사용자 조직에서 나가는 경우 액세스할 수 있습니다 (조직 관리 역할 그룹의 구성원 또는 eDiscovery 관리자 역할 그룹의 다른 구성원을 포함 하 여) 아무도 사례입니다. 이 이런 경우에 데이터에 액세스할 수 있는 방법이 없습니다 있을 것입니다. EDiscovery 관리자가 조직에서 모든 eDiscovery 사례에 액세스할 수 있으므로 보안에서 대/소문자를 볼 수 있도록 하지만 &amp; 준수 센터 대/소문자의 구성원으로 직접 또는 다른 eDiscovery 관리자를 추가 하 고 있습니다.
    
  - EDiscovery 관리자는 보고 하 고 모든 eDiscovery 사례에 액세스할 수, 때문에 감사 하 고 모든 경우 감독 수 및 관련 규정 준수를 검색 합니다. 그러면 모든 오용 준수 검색 또는 eDiscovery 사례를 방지 하기 위해 수 있습니다. 및 eDiscovery 관리자 준수 검색 결과에서 잠재적으로 중요 한 정보에 액세스할 수 있으므로 eDiscovery 관리자가 사용자의 수를 제한 해야 합니다.
    
    또한 eDiscovery 관리자 보안에서 &amp; 준수 센터 고급 eDiscovery의 관리자로 자동으로 추가 됩니다. 즉, 사용자는 eDiscovery 사용자 설정의 경우 만들기 (영문), 사례에에서 데이터 가져오기 (영문) 등의 고급 eDiscovery의 관리 작업을 수행 하려면 관리자 여야 합니다.
    
- **보안에서 eDiscovery 관리자 역할 그룹의 구성원으로 그룹을 추가할 수 &amp; 준수 센터?** 앞부분에 설명, 보안에서 **Add-rolegroupmember** cmdlet을 사용 하 여 eDiscovery 관리자 역할 그룹에서 eDiscovery 관리자 하위 그룹의 구성원으로 메일 사용이 가능한 보안 그룹을 추가할 수 있습니다 &amp; 준수 센터 PowerShell 합니다. 예, eDiscovery 관리자 역할 그룹에 메일 사용이 가능한 보안 그룹을 추가 하려면 다음 명령을 실행할 수 있습니다. 
    
  ```
  Add-RoleGroupMember "eDiscovery Manager" -Member <name of security group>
  ```

    Note는 Exchange 메일 그룹 또는 Office 365 그룹 지원 되지 않습니다. 사용 하 여 Exchange Online PowerShell에서 만들 수 있는 메일 사용이 가능한 보안 그룹을 사용 해야는 ` New-DistributionGroup -Type Security ` 명령 합니다. 또한 메일 사용이 가능한 보안 그룹을 만듭니다 (추가 하는 구성원) Office 365 관리 센터 또는 Exchange 관리 센터에 있습니다. Note eDiscovery 관리자 역할 그룹에 추가할 수는 새 메일 사용이 가능한 보안을 위해 만든 후 60 분까지 걸릴 수 있습니다. 
    
    또한 앞부분에 나와있는 eDiscovery 관리자 보안에서 **추가 eDiscoveryCaseAdmin** cmdlet을 사용 하 여 그룹을 메일 사용이 가능한 보안을 만들 수 없습니다 &amp; 준수 센터 PowerShell 합니다. 만 ediscovery 관리자가 개별 사용자를 추가할 수 있습니다. 
    
    참고도 추가할 수는 없습니다 메일 사용이 가능한 보안 그룹의 사례를 구성원으로 합니다.
