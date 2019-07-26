---
title: Office 365 조직의 전자 메일 메시지 검색 및 삭제 - 관리자 도움말
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
ms.assetid: 3526fd06-b45f-445b-aed4-5ebd37b3762a
description: Office365 보안 및 준수 센터의 검색 및 지우기 기능을 사용하여 조직의 모든 사서함에서 전자 메일 메시지를 검색하고 삭제할 수 있습니다.
ms.openlocfilehash: 318a7deeedb6bd4875a7a2ca0f5e33b764bdbac3
ms.sourcegitcommit: 33c8e9c16143650ca443d73e91631f9180a9268e
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/25/2019
ms.locfileid: "35854632"
---
# <a name="search-for-and-delete-email-messages-in-your-office-365-organization---admin-help"></a>Office 365 조직의 전자 메일 메시지 검색 및 삭제 - 관리자 도움말

**이 문서는 관리자를 위해 작성되었습니다. 사서함에서 삭제할 항목을 찾으려고 하나요? [빠른 검색을 사용하여 메시지 또는 항목 찾기](https://support.office.com/article/69748862-5976-47b9-98e8-ed179f1b9e4d)**|을 참조하세요.
   
Office365의 콘텐츠 검색 기능을 사용하여 조직의 모든 사서함에서 전자 메일 메시지를 검색하고 삭제할 수 있습니다. 이렇게 하면 잠재적으로 유해하거나 위험성이 높은 전자 메일을 찾아서 제거하는 데 도움이 됩니다.
  
- 위험한 첨부 파일 또는 바이러스를 포함하는 메시지
    
- 피싱 메시지
    
- 중요한 데이터가 포함된 메시지
    
> [!CAUTION]
> 검색 및 삭제는 필요한 권한이 할당된 누구든지 조직의 사서함에서 전자 메일 메시지를 삭제할 수 있도록 하는 강력한 기능입니다. 
  
## <a name="before-you-begin"></a>시작하기 전에

- 콘텐츠 검색을 만들고 실행하려면 **eDiscovery 관리자** 역할 그룹의 구성원이거나 **준수 검색** 관리 역할을 할당 받아야 합니다. 메시지를 삭제하려면 **조직 관리** 역할 그룹의 구성원이거나 **검색 및 삭제** 관리 역할을 할당 받아야 합니다. 역할 그룹에 사용자를 추가하는 방법에 대한 자세한 내용은 [사용자에게 보안 및 준수 센터에 대한 액세스 권한 부여](grant-access-to-the-security-and-compliance-center.md)를 참조하세요.
    
- 메시지를 삭제하려면 보안 및 준수 센터 PowerShell을 사용해야 합니다. 연결하는 방법에 대한 자세한 내용은 [2단계](#step-2-connect-to-security--compliance-center-powershell)를 참조하세요.
    
- 사서함마다 한 번에 최대 10개의 항목을 제거할 수 있습니다. 메시지를 검색하고 제거하는 기능은 인시던트 응답 도구로 고안되었으므로 이러한 제한은 사서함에서 메시지가 빠르게 제거되도록 합니다. 이 기능은 사용자 사서함을 정리하기 위한 것이 아닙니다. 10개를 초과하는 항목을 삭제하려면 Exchange Online PowerShell에서 **Search-Mailbox -DeleteContent** 명령을 사용할 수 있습니다. [메시지 검색 및 삭제 - 관리자 도움말](search-for-and-delete-messagesadmin-help.md)를 참조하세요.
    
- 콘텐츠 검색에서 검색 및 삭제 작업을 수행하여 항목을 삭제할 수 있는 최대 사서함 수는 50,000개입니다. [1단계](#step-1-create-a-content-search-to-find-the-message-to-delete)에서 만든 콘텐츠 검색에 50,000개를 초과하는 원본 사서함이 있는 경우 3단계에서 만드는 삭제 작업이 실패합니다. 50,000개 이상의 사서함에 대해 검색 및 삭제 작업을 수행하는 방법에 대한 자세한 내용은 [추가 정보](#more-information) 섹션을 참조하세요. 
    
- 이 문서의 절차는 Exchange Online 사서함 및 공용 폴더에서 항목을 삭제하는 데에만 사용할 수 있습니다. SharePoint 또는 비즈니스용 OneDrive 사이트에서 콘텐츠를 삭제하는 데에는 사용할 수 없습니다.
    
## <a name="step-1-create-a-content-search-to-find-the-message-to-delete"></a>1단계: 삭제할 메시지를 찾는 콘텐츠 검색 만들기

첫 번째 단계는 조직의 사서함에서 제거하려는 메시지를 찾는 콘텐츠 검색을 만들어 실행하는 것입니다. 보안 및 준수 센터를 사용하거나 **New-ComplianceSearch** 및 **Start-ComplianceSearch** cmdlet을 실행하여 검색을 만들 수 있습니다. 이 검색의 쿼리와 일치하는 메시지는 [3단계](#step-3-delete-the-message)에서 **New-ComplianceSearchAction -Purge** 명령을 실행하여 삭제합니다. 콘텐츠 검색을 만들고 검색 쿼리를 구성하는 방법에 대한 자세한 내용은 다음 항목을 참조하세요. 
  
- [Office 365의 콘텐츠 검색](content-search.md)
    
- [콘텐츠 검색에 대한 키워드 쿼리](keyword-queries-and-search-conditions.md)
    
- [New-ComplianceSearch](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-content-search/New-ComplianceSearch)
    
- [Start-ComplianceSearch](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-content-search/Start-ComplianceSearch)
    
> [!NOTE]
> 이 단계에서 만드는 콘텐츠 검색에서 검색되는 콘텐츠 위치에는 SharePoint 또는 비즈니스용 OneDrive 사이트가 포함될 수 없습니다. 전자 메일 메시지에 사용되는 콘텐츠 검색에는 사서함 및 공용 폴더만 포함될 수 있습니다. 콘텐츠 검색에 사이트가 포함되는 경우 **New-ComplianceSearchAction** cmdlet을 실행할 때 3단계에서 오류가 발생합니다. 
  
### <a name="tips-for-finding-messages-to-remove"></a>제거할 메시지를 찾기 위한 팁

검색 쿼리의 목적은 검색의 결과 범위를 제거할 메시지로만 좁히는 것입니다. 다음 팁을 참조하세요.
  
- 메시지의 제목 줄에 사용된 정확한 텍스트나 구를 알고 있으면 검색 쿼리에 **Subject** 속성을 사용합니다. 
    
- 메시지의 정확한 날짜(또는 날짜 범위)를 알고 있으면 검색 쿼리에 **Received** 속성을 포함합니다. 
    
- 메시지를 보낸 사람을 알고 있으면 검색 쿼리에 **From** 속성을 포함합니다. 
    
- 검색 결과를 미리 확인하여 콘텐츠 검색이 삭제하려는 메시지만 반환하는지 검토합니다.
    
- 검색 예상 통계(보안 및 준수 센터의 검색 세부 정보 창에 표시되거나 [Get-ComplianceSearch](https://go.microsoft.com/fwlink/p/?LinkId=517934) cmdlet을 사용할 경우에 표시)를 사용하여 결과의 총 개수를 가져올 수 있습니다. 
    
다음은 의심스러운 전자 메일 메시지를 찾는 쿼리의 두 가지 예입니다.
  
- 이 쿼리는 2016년 4월 13일과 2016년 4월 14일 사이에 사용자가 받은 메시지 중에서 제목 줄에 "action" 및 "required"가 포함된 메시지를 반환합니다.
    
    ```
    (Received:4/13/2016..4/14/2016) AND (Subject:'Action required')
    ```
   
- 이 쿼리는 chatsuwloginsset12345@outlook.com에서 보낸 메시지 중에서 제목 줄에 "Update your account information"이 포함된 메시지를 반환합니다.
    
    ```
    (From:chatsuwloginsset12345@outlook.com) AND (Subject:"Update your account information")
    ```

## <a name="step-2-connect-to-security--compliance-center-powershell"></a>2단계: 보안 및 준수 센터 PowerShell에 연결

다음 단계에서는 조직의 보안 및 준수 센터 PowerShell에 연결합니다. 단계별 지침은 [보안 및 준수 센터 PowerShell에 연결하기](https://docs.microsoft.com/powershell/exchange/office-365-scc/connect-to-scc-powershell/connect-to-scc-powershell)를 참조하세요.
  
Office 365 계정에서 MFA(다단계 인증) 또는 페더레이션된 인증을 사용하는 경우 이전 항목의 지침에 따라 보안 및 준수 센터 PowerShell에 연결할 수 없습니다. 대신 [다단계 인증을 사용하여 보안 및 준수 센터 PowerShell에 연결](https://docs.microsoft.com/powershell/exchange/office-365-scc/connect-to-scc-powershell/mfa-connect-to-scc-powershell) 항목의 지침을 참조하세요.
  
## <a name="step-3-delete-the-message"></a>3단계: 메시지 삭제

제거하려면 메시지를 반환하는 콘텐츠 검색을 만들고 구체화한 다음 보안 및 준수 센터 PowerShell에 연결되면 마지막으로 **New-ComplianceSearchAction** cmdlet을 실행하여 메시지를 삭제합니다. 메시지를 일시 또는 영구 삭제할 수 있습니다. 일시 삭제된 메시지는 사용자의 복구 가능한 항목 폴더로 이동하고 삭제된 항목 보존 기간이 만료될 때까지 보존됩니다. 영구 삭제된 메시지는 사서함에서 영구 제거 표시되고 관리되는 폴더 도우미에서 다음에 사서함을 처리할 때 영구적으로 제거됩니다. 사서함에 대해 단일 항목 복구를 사용하는 경우 삭제된 항목 보존 기간이 만료되면 영구 삭제된 항목은 영구히 제거됩니다. 사서함이 보류 중인 경우 항목에 대한 보존 기간이 만료되거나 사서함에서 보류가 제거될 때까지 삭제된 메시지가 보존됩니다.
  
다음 예에서 명령은 “피싱 메시지 제거”라는 콘텐츠 검색에 의해 반환된 검색 결과를 일시 삭제합니다. 

```
New-ComplianceSearchAction -SearchName "Remove Phishing Message" -Purge -PurgeType SoftDelete
```

"피싱 메시지 제거" 콘텐츠 검색에서 반환되는 항목을 영구 삭제하려면 다음 명령을 실행합니다.

```
New-ComplianceSearchAction -SearchName "Remove Phishing Message" -Purge -PurgeType HardDelete
```

이전 명령을 실행하여 메시지를 일시 삭제하거나 영구 삭제하는 경우 *SearchName* 매개 변수에 지정된 검색은 1단계에서 만든 콘텐츠 검색입니다. 
  
자세한 내용은 [New-ComplianceSearchAction](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-content-search/New-ComplianceSearchAction)을 참조하세요.

## <a name="more-information"></a>추가 정보

- **검색 및 삭제 작업에 대한 상태를 어떻게 가져오나요?**

    삭제 작업에 대한 상태를 가져오려면 **Get-ComplianceSearchAction**을 실행합니다. **New-ComplianceSearchAction** cmdlet을 실행할 때 생성되는 개체의 이름은 다음 형식을 사용하여 지정됩니다. `<name of Content Search>_Purge`. 
    
- **메시지를 삭제하면 어떻게 되나요?**

   `New-ComplianceSearchAction -Purge -PurgeType HardDelete` 명령을 사용하여 삭제한 메시지는 제거 폴더로 이동되고 사용자가 액세스할 수 없습니다. 사서함에서 단일 항목 복구를 사용하는 경우 메시지는 제거 폴더로 이동된 후 삭제된 항목 보존 기간 동안 보존됩니다. Office 365에서는 새 사서함을 만들 때 단일 항목 복구가 기본적으로 사용됩니다. 삭제된 항목 보존 기간이 만료되면 메시지는 영구 삭제로 표시되고 관리되는 폴더 도우미에서 사서함을 다음에 처리할 때 Office 365에서 제거됩니다. 

   `New-ComplianceSearchAction -Purge -PurgeType SoftDelete` 명령을 사용하는 경우 사용자의 복구 가능한 항목 폴더에서 삭제 폴더로 메시지가 이동합니다. 메시지는 Office 365에서 바로 제거되지 않습니다. 사용자는 사서함에 구성된 삭제된 항목 보존 기간에 따라 일정 기간 동안 삭제된 항목 폴더에서 메시지를 복구할 수 있습니다. 이 보존 기간이 만료되거나 만료되기 전에 사용자가 메시지를 제거하면 메시지는 제거 폴더로 이동되고 더 이상 액세스할 수 없습니다. 사서함에서 단일 항목 복구를 사용하는 경우 제거 폴더의 메시지는 사서함에 대해 구성된 삭제된 항목 보존 기간에 따라 일정 기간 동안 보존됩니다. Office 365에서는 새 사서함을 만들 때 단일 항목 복구가 기본적으로 사용됩니다. 삭제된 항목 보존 기간이 만료되면 메시지는 영구 삭제로 표시되고 관리되는 폴더 도우미에서 사서함을 다음에 처리할 때 Office 365에서 제거됩니다. 
    
- **50,000개를 초과하는 사서함에서 메시지를 삭제해야 하는 경우 어떻게 되나요?**

    앞서 설명한 대로 최대 50,000개의 사서함에서 검색 및 삭제 작업을 수행할 수 있습니다. 50,000개를 초과하는 사서함에서 검색 및 삭제 작업을 수행해야 하는 경우 검색되는 사서함 수를 50,000개 이하로 줄여주는 임시 검색 권한 필터를 만들어 보세요. 예를 들어 여러 부서, 주 또는 국가에 조직의 사서함이 포함되어 있는 경우 이러한 사서함 속성 중 하나를 기반으로 사서함 검색 권한 필터를 만들어 조직의 사서함 하위 집합을 검색할 수 있습니다. 검색 사용 권한 필터를 만든 후 1단계에서 설명한 대로 검색을 만든 후 3단계에서 설명한 대로 메시지를 삭제합니다. 그런 다음 필터를 편집하여 다른 사서함 집합에서 메시지를 검색한 후 삭제할 수 있습니다. 검색 권한 필터를 만드는 방법에 대한 자세한 내용은 [콘텐츠 검색에 대한 권한 필터링 구성](permissions-filtering-for-content-search.md)을 참조하세요.
    
- **검색 결과에 포함된 인덱싱되지 않은 항목이 삭제되나요?**

    아니요. `New-ComplianceSearchAction -Purge 명령은 인덱싱되지 않은 항목을 삭제하지 않습니다. 
    
- **원본 위치 유지 또는 소송 보존에 포함되거나 Office 365 보존 정책에 할당된 사서함에서 메시지를 삭제하면 어떻게 되나요?**

    메시지가 삭제되고 제거 폴더로 이동된 후 보존 기간이 만료될 때까지 보존됩니다. 보존 기간에 제한이 없는 경우 보류를 제거하거나 보존 기간을 변경할 때까지 항목이 보존됩니다.
    
- **다양한 보안 및 준수 센터 역할 그룹 간에 검색 및 제거 워크플로가 분리되어 있는 이유**

    앞서 설명한 것처럼 사서함을 검색하려면 eDiscovery 관리자 역할 그룹의 구성원이거나 준수 검색 관리 역할이 할당되어야 합니다. 메시지를 삭제하려면 조직 관리 역할 그룹의 구성원이거나 검색 및 제거 관리 역할을 할당 받아야 합니다. 이렇게 하면 조직에서 사서함을 검색할 수 있는 사람과 메시지를 삭제할 수 있는 사람을 제어할 수 있습니다. 
