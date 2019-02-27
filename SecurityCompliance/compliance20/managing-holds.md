---
title: Advanced eDiscovery에서 보류 관리 (미리 보기)
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: ''
ms.openlocfilehash: fe6ab3a1e1108e9ab2e4fc201357b72a77453d38
ms.sourcegitcommit: baf23be44f1ed5abbf84f140b5ffa64fce605478
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/26/2019
ms.locfileid: "30295721"
---
# <a name="manage-holds-in-advanced-ediscovery-preview"></a>Advanced eDiscovery에서 보류 관리 (미리 보기)

고급 eDiscovery (미리 보기) 사례를 사용 하 여 해당 사례와 관련이 있을 수 있는 콘텐츠를 보존 하는 보류를 만들 수 있습니다. 고급 eDiscovery (미리 보기) 유지 기능을 사용 하 여 custodians 및 해당 데이터 원본에 보류를 배치할 수 있습니다. 또한 사서함과 비즈니스용 OneDrive 사이트에 custodial이 없는 보류를 배치할 수 있습니다. 또한 Office 365 그룹의 그룹 사서함, SharePoint 사이트 및 비즈니스용 OneDrive 사이트에 보류할 수 있습니다. 마찬가지로 Microsoft 팀과 연결 된 사서함 및 사이트를 유지할 수 있습니다. 콘텐츠 위치를 유지 하는 경우에는 custodian를 해제 하거나, 특정 데이터 위치를 제거 하거나, 보존 정책을 완전히 삭제할 때까지 콘텐츠가 보관 됩니다.

## <a name="manage-custodian-based-holds"></a>custodian 유지 관리

경우에 따라 식별 하 고 choosen 보존을 위해 custodians 데이터 집합을 가질 수 있습니다. 고급 eDiscovery (미리 보기)에서 이러한 custodians를 보류 하면 사용자 및 선택한 데이터 원본이 custodian 보류 정책에 자동으로 추가 됩니다. 

custodian 보류 정책을 보려면 다음을 수행 합니다.

1. **보안 & 준수 센터**에서 **eDiscovery > Advanced eDiscovery (미리 보기)** 를 클릭 하 여 조직의 사례 목록을 표시 합니다.
   
2. **Custodians** 탭으로 이동 하 여 사례 내의 Custodians을 추가 합니다. 고급 ediscovery (미리 보기) 사례 내에서 보류 중인 custodians을 추가 하 고 배치 하는 방법에 대 한 자세한 내용은 [add custodians to a advanced ediscovery (preview) case](add-custodians-to-case.md)을 참조 하십시오. custodians를 이미 추가 했 고 대기 상태로 둔 경우 3 단계로 이동 합니다.
   
3. **보류** 탭으로 이동 하 여 ' Custodian Policy '를 선택 합니다.
   
4. 플라이 아웃 페이지에서는 정책에 대 한 보류 통계를 볼 수 있습니다. custodian 기반 유지에 쿼리를 적용 하는 등의 작업을 수행할 수도 있습니다. 보류 쿼리를 만들고 조건을 사용 하는 방법에 대 한 자세한 내용은 [키워드 쿼리 및 검색 조건을](../keyword-queries-and-search-conditions.md)참조 하십시오.
 
## <a name="manage-non-custodial-holds"></a>비 custodial 보류 관리

보류를 만들 때 지정 된 콘텐츠 위치에 보관 되는 콘텐츠의 범위를 지정할 수 있는 옵션은 다음과 같습니다.

  - 모든 콘텐츠가 보류 되는 영구 보존을 만듭니다. 또는 검색 쿼리와 일치 하는 콘텐츠만 보존 되는 쿼리 기반 보류를 만들 수 있습니다.
  - 해당 날짜 범위 내에서 전송, 수신 또는 만든 콘텐츠만 저장 하는 날짜 범위를 지정할 수 있습니다. 또는 보내기, 수신 또는 만든 시기에 관계 없이 모든 콘텐츠를 저장할 수 있습니다.

고급 eDiscovery (미리 보기)에 대 한 보존을 만들려면 다음을 수행 합니다.

1. **보안 & 준수 센터**에서 **eDiscovery > Advanced eDiscovery (미리 보기)** 를 클릭 하 여 조직의 사례 목록을 표시 합니다.
  
2. 보류를 만들려는 사례 옆에 있는 **열기** 를 클릭 합니다.
  
3. 사례에 대 한 홈 페이지에서 **보류** 탭을 클릭 합니다.
  
4. **보류** 탭에서 **만들기**를 클릭 합니다.
  
5. **보존 이름** 페이지에서 보류 이름을 지정 합니다. 보류의 이름은 조직 내에서 고유 해야 합니다.
 
6. 반드시 **설명** 상자에 보류에 대 한 설명을 추가 합니다.
  
7. **다음**을 클릭합니다.
  
8. 보류 상태로 설정할 콘텐츠 위치를 선택 합니다. 사서함, 사이트 및 공용 폴더를 보류에 배치할 수 있습니다.

   **전자 메일 교환** - **사용자, 그룹 또는 팀 선택을** 클릭 하 고 **사용자, 그룹 또는 팀 선택을** 차례로 클릭 하 여 보류할 사서함을 지정 합니다. 검색 상자를 사용 하 여 사용자 사서함과 메일 그룹 (그룹 구성원의 사서함을 보류)을 보류 상태로 설정 합니다. Office 365 그룹 또는 Microsoft 팀에 대 한 연결 된 사서함을 보류할 수도 있습니다. 사용자, 그룹, 팀 확인란을 선택 하 고 **선택을**클릭 한 후 **완료**를 클릭 합니다.
 
    > [!NOTE]
    > **사용자, 그룹 또는 팀 선택을** 클릭 하 여 보류 중인 사서함을 지정 하는 경우 표시 되는 사서함 선택은 비어 있습니다. 이는 성능 향상을 위해 설계 된 것입니다. 이 목록에 사용자를 추가 하려면 검색 상자에 이름 (최소 3 자)을 입력 합니다.

    b. **sharepoint 사이트** - **사이트 선택을** 클릭 한 다음 **사이트 선택을** 다시 클릭 하 여 SharePoint 및 비즈니스용 OneDrive 사이트를 보류로 지정 합니다. 보류 하도록 설정할 각 사이트의 URL을 입력 합니다. 또한 Office 365 그룹 또는 Microsoft 팀에 대 한 SharePoint 사이트의 URL을 추가할 수 있습니다. **선택을**클릭 하 고 **완료**를 클릭 합니다.
    
     Office 365 그룹 및 Microsoft 팀을 보류 하는 방법에 대 한 팁은 **FAQ** 섹션을 참조 하십시오.

    > [!NOTE]
    > 드문 경우 이지만 사용자의 upn (사용자 계정 이름)이 변경 된 경우에는 해당 OneDrive 계정에 대 한 URL도 새 UPN을 통합 하도록 변경 됩니다. 이 경우에는 사용자의 새 OneDrive URL을 추가 하 고 이전 항목을 제거 하 여 보류를 수정 해야 합니다.

     c. **exchange 공용 폴더** -설정/해제 스위치를 all 위치로 이동 하 여 Exchange Online 조직의 모든 공용 폴더를 보류 상태로 전환 합니다. 특정 공용 폴더를 선택 하 여 보류 상태로 설정할 수는 없습니다. 공용 폴더를 보존 하지 않으려면 toggle 스위치를 **"없음"** 으로 설정 된 상태로 둡니다.

9. 보류에 콘텐츠 위치를 모두 추가한 후에 **다음**을 클릭 합니다.
  
10. 조건을 사용 하 여 쿼리 기반 보존을 만들려면 다음을 완료 합니다. 그렇지 않으면 **다음**을 클릭 합니다.
    
    - **키워드**아래의 상자에 검색 조건을 충족 하는 콘텐츠만 저장 되도록 상자에 검색 쿼리를 입력 합니다. 키워드, 메시지 속성 또는 문서 속성 (예: 파일 이름)을 지정할 수 있습니다. AND, OR, NOT 등의 부울 연산자를 사용 하 여 보다 복잡 한 쿼리를 사용할 수도 있습니다. 키워드 상자를 비워 두면 지정 된 콘텐츠 위치에 있는 모든 콘텐츠가 보류 상태가 됩니다.

    - 조건 **추가** 를 클릭 하 여 보류에 대 한 검색 쿼리 범위를 좁히는 조건을 하나 이상 추가 합니다. 각 조건은 보류를 만들 때 만들어지고 실행 되는 KQL 검색 쿼리에 절을 추가 합니다. 예를 들어 날짜 범위를 지정 하 여 원거리 시간 내에 만들어진 전자 메일 또는 사이트 문서를 보류할 수 있습니다. 조건은 AND 연산자에 의해 키워드 상자에 지정 된 키워드 쿼리에 논리적으로 연결 됩니다. 즉, 항목이 유지 되도록 키워드 쿼리와 조건을 모두 충족 해야 합니다.

     검색 쿼리를 만들고 조건을 사용 하는 방법에 대 한 자세한 내용은 [키워드 쿼리 및 검색 조건을](https://docs.microsoft.com/en-us/office365/SecurityCompliance/keyword-queries-and-search-conditions)참조 하십시오.

12. 쿼리 기반 보존을 구성한 후 **다음**을 클릭 합니다.
 
13. 설정을 검토 하 고 **이 보류 만들기**를 클릭 합니다.


## <a name="view-hold-statistics"></a>보류 통계 보기

잠시 후에 새 보류에 대 한 정보가 선택한 보류에 대 한 **보류** 탭의 세부 정보 창에 표시 됩니다. 이 정보에는 보류 중인 사서함 및 사이트의 수와 보류 중인 항목의 총 수와 크기, 보류 통계가 계산 된 마지막 시간 등이 포함 됩니다. 이러한 보존 통계를 통해 eDiscovery 사례와 관련 된 콘텐츠의 양에 대 한 정보를 확인할 수 있습니다.

보류 통계에 대해서는 다음 사항을 염두에 두어야 합니다.

- 보류 중인 총 항목 수는 보류 된 모든 콘텐츠 원본의 항목 수를 나타냅니다. 쿼리 기반 보존을 만든 경우이 통계는 쿼리와 일치 하는 항목의 수를 나타냅니다.
  
- 보류 중인 항목 수에는 콘텐츠 위치에 있는 인덱싱되지 않은 항목도 포함 됩니다. 쿼리 기반 보존을 만드는 경우에는 콘텐츠 위치에 있는 모든 인덱싱되지 않은 항목이 보류에 저장 됩니다. 여기에는 날짜 범위 조건 외부에 있을 수 있는 쿼리 기반 보류 및 인덱싱되지 않은 항목의 검색 조건과 일치 하지 않는 인덱싱되지 않은 항목이 포함 됩니다. 이는 검색 쿼리와 일치 하지 않거나 날짜 범위에서 제외 된 인덱싱되지 않은 항목이 검색 결과에 포함 되지 않는 콘텐츠 검색을 실행할 때 일어나는 것과는 다릅니다. 인덱싱되지 않은 항목에 대 한 자세한 내용은 [Office 365의 콘텐츠 검색에서 부분적으로 인덱싱된 항목](../partially-indexed-items-in-content-search.md)을 참조 하세요. 

- 통계 업데이트를 클릭 하 여 보류 중인 항목 수를 계산 하는 검색 예측을 다시 실행 하 여 최신 보존 통계를 가져올 수 있습니다.

- 필요한 경우 도구 모음에서 새로 고침을 클릭 하 여 세부 정보 창에서 보류 통계를 업데이트 합니다.

- 사서함 이나 사이트가 보류 중인 사용자가 새 전자 메일 메시지를 보내거나 받고 새 SharePoint 및 비즈니스용 OneDrive 문서를 만드는 경우에는 보존 되는 항목의 수가 시간에 따라 증가 합니다.

- SharePoint 사이트 또는 OneDrive 계정을 다중 지리적 환경에서 다른 지역으로 이동 하는 경우 해당 사이트에 대 한 통계가 보존 통계에 포함 되지 않습니다. 하지만 사이트의 콘텐츠는 계속 유지 됩니다. 또한 사이트가 다른 지역으로 이동 되는 경우 보류에 표시 되는 URL은 업데이트 되지 않습니다. 보류를 편집 하 고 URL을 업데이트 해야 합니다.

## <a name="frequently-asked-questions"></a>자주하는 질문

- **추가 Office 365 그룹 또는 Microsoft 팀 사이트를 custodian에 매핑하는 방법은 무엇 인가요? Office 365 그룹 및 Microsoft 팀에 Custodial 되지 않는 보류를 배치 하는 방법은 무엇 인가요?** Microsoft 팀은 Office 365 그룹을 기반으로 작성 됩니다. 따라서 eDiscovery 사례에서 보류를 설정 하는 것은 매우 유사 합니다. Office 365 그룹과 Microsoft 팀을 보류할 때 다음과 같은 사항을 염두에 두어야 합니다.
  - 보류 중인 Office 365 그룹 및 Microsoft 팀에 있는 콘텐츠를 배치 하려면 그룹 또는 팀과 연결 된 사서함 및 SharePoint 사이트를 지정 해야 합니다.
  
  - Exchange Online에서 **remove-unifiedgroup** cmdlet을 실행 하 여 Office 365 그룹 또는 Microsoft Team의 속성을 볼 수 있습니다. 이를 통해 Office 365 그룹 또는 Microsoft 팀에 연결 된 사이트의 URL을 가져올 수 있습니다. 예를 들어 다음 명령은 선임 리더십 팀 이라는 Office 365 그룹에 대해 선택 된 속성을 표시 합니다.


    ```
    Get-UnifiedGroup "Senior Leadership Team" | FL DisplayName,Alias,PrimarySmtpAddress,SharePointSiteUrl
    DisplayName            : Senior Leadership Team
    Alias                  : seniorleadershipteam
    PrimarySmtpAddress     : seniorleadershipteam@contoso.onmicrosoft.com
    SharePointSiteUrl      : https://contoso.sharepoint.com/sites/seniorleadershipteam
    ```

    > [!NOTE]
    > remove-unifiedgroup cmdlet을 실행 하려면 Exchange Online에서 보기 전용 받는 사람 역할을 할당 받거나 보기 전용 받는 사람 역할이 할당 된 역할 그룹의 구성원 이어야 합니다.

 - 사용자의 사서함이 검색 되 면 사용자가 구성원으로 속해 있는 모든 Office 365 그룹 또는 Microsoft 팀이 검색 되지 않습니다. 마찬가지로, Office 365 그룹 또는 Microsoft 팀을 유지 하면 그룹 사서함과 그룹 사이트만 보존 됩니다. 그룹 구성원의 사서함 및 비즈니스용 OneDrive 사이트는 명시적으로 custodians로 추가 하거나 데이터 원본을 유지 하는 경우가 아니면 보류 되지 않습니다. 따라서 특정 custodian으로 Office 365 그룹 또는 Microsoft Team을 보류할 필요가 있는 경우 그룹 사이트 및 그룹 사서함을 custodian에 매핑합니다 (Advanced eDiscovery (Preview)에서 Custodians 관리 참조). Office 365 그룹 또는 Microsoft 팀이 단일 custodian으로 인 한 경우에는 custodial 되지 않은 보류에 원본을 추가 하는 것이 좋습니다. 
 
 - office 365 그룹 또는 Microsoft Team의 구성원 목록을 보려면 office 365 관리 센터의 Home > Groups 페이지에서 해당 속성을 볼 수 있습니다. 또는 Exchange Online PowerShell에서 다음 명령을 실행할 수도 있습니다.

   ``` 
   Get-UnifiedGroupLinks <group or team name> -LinkType Members | FL DisplayName,PrimarySmtpAddress
   ```

    > [!NOTE]
    > **add-unifiedgrouplinks** cmdlet을 실행 하려면 Exchange Online에서 보기 전용 받는 사람 역할을 할당 받거나 보기 전용 받는 사람 역할이 할당 된 역할 그룹의 구성원 이어야 합니다.

- Microsoft 팀 채널의 일부인 채널 대화는 팀과 연결 된 사서함에 저장 됩니다. 마찬가지로 팀 구성원이 채널에서 공유 하는 파일은 팀의 SharePoint 사이트에 저장 됩니다. 따라서 대화 및 파일을 채널에 유지 하려면 Microsoft 팀 사서함 및 SharePoint 사이트를 보류 상태로 설정 해야 합니다.
  
- 또는 Microsoft 팀의 채팅 목록에 포함 된 대화는 채팅에 참가 하는 사용자의 사서함에 저장 됩니다.  사용자가 채팅 대화에서 공유 하는 파일은 해당 파일을 공유 하는 사용자의 비즈니스용 OneDrive 사이트에 저장 됩니다. 따라서 채팅 목록에 있는 대화 및 파일을 유지 하려면 개별 사용자 사서함과 비즈니스용 OneDrive 사이트를 보존 해야 합니다. 
  
- 모든 Microsoft 팀 또는 팀 채널에는 노트 기록 및 공동 작업을 위한 Wiki가 포함 되어 있습니다. Wiki 콘텐츠가 .mht 형식의 파일에 자동으로 저장 됩니다. 이 파일은 팀의 SharePoint 사이트에 있는 팀 위 키 데이터 문서 라이브러리에 저장 됩니다. 팀의 SharePoint 사이트를 보류 하 여 해당 콘텐츠를 Wiki에 배치할 수 있습니다.

  > [!NOTE]
  > Microsoft 팀 또는 팀 채널에 대 한 Wiki 콘텐츠를 보존 하는 기능 (팀의 SharePoint 사이트를 보류할 때)은 6 월 22 일에 릴리스 되었습니다. 팀 사이트를 보류 중인 경우에는 해당 날짜에 대해 Wiki 콘텐츠가 유지 됩니다. 그러나 팀 사이트가 유지 되 고 wiki 콘텐츠가 6 월 22 일 이전에 삭제 된 경우에는 wiki 콘텐츠가 보존 되지 않습니다.
