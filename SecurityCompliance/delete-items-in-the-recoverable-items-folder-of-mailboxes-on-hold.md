---
title: 보류에서 클라우드 기반 사서함의 복구 가능한 항목 폴더에 있는 항목 삭제-관리자 도움말
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
ms.assetid: a85e1c87-a48e-4715-bfa9-d5275cde67b0
description: '관리자: 해당 사서함이 법적 보존 상태로 설정 된 경우에도 Exchange Online 사서함에 대 한 사용자의 복구 가능한 항목 폴더에서 항목을 삭제 합니다. 이 방법은 실수로 Office 365에 분산 된 데이터를 삭제 하는 효율적인 방법입니다.'
ms.openlocfilehash: f3518dc1009b4e95472473f76e6cd41011bc6b3e
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30216958"
---
# <a name="delete-items-in-the-recoverable-items-folder-of-cloud-based-mailboxes-on-hold---admin-help"></a>보류에서 클라우드 기반 사서함의 복구 가능한 항목 폴더에 있는 항목 삭제-관리자 도움말

Exchange Online 사서함에 대 한 복구 가능한 항목 폴더는 실수로 또는 악의적으로 삭제 되는 것을 방지 하기 위해 존재 합니다. 또한 보류 및 eDiscovery 검색과 같은 Office 365 준수 기능에서 유지 하 고 액세스 하는 항목을 저장 하는 데도 사용 됩니다. 그러나 조직에서 삭제 해야 하는 복구 가능한 항목 폴더에 실수로 보존 된 데이터가 있을 수 있습니다. 예를 들어 사용자가 중요 한 정보를 포함 하는 전자 메일 메시지를 실수로 보내거나 전달할 수 있으며 비즈니스에 심각한 영향을 줄 수도 있습니다. 메시지가 영구적으로 삭제 된 경우에도 사서함에 법적 보존이 설정 되어 있기 때문에 무기한 유지 될 수 있습니다. 이 시나리오는 데이터가 실수로 Office 365에 분산 되어 있기 때문에 데이터 유출 합니다. 이러한 상황에서는 사용자의 복구 가능한 항목 폴더에서 Exchange Online 사서함에 대 한 항목을 삭제할 수 있으며 해당 사서함이 Office 365의 다른 보존 기능 중 하 나와 함께 유지 되는 경우에도 마찬가지입니다. 이러한 유형의 보류에는 소송 보존, 원본 위치 유지, eDiscovery 보류 및 office 365 보안 &amp; 및 준수 센터에서 만든 Office 365 보관 정책이 포함 됩니다. 
  
 이 문서에서는 보류 중인 클라우드 기반 사서함에 대 한 복구 가능한 항목 폴더에서 항목을 삭제 하는 방법에 대해 설명 합니다. 이 절차에서는 사서함에 대 한 액세스를 사용 하지 않도록 설정 하 고 단일 항목 복구를 사용 하지 않도록 설정 하 고 관리 되는 폴더 도우미가 사서함을 처리 하지 않도록 설정한 다음 일시적으로 보류를 제거 하 고 복구 가능한 항목 폴더에서 항목을 삭제 이전 구성으로 사서함을 이동할 수 있습니다. 프로세스는 다음과 같습니다. 
  
[1 단계: 사서함에 대 한 정보 수집](#step-1-collect-information-about-the-mailbox)

[2 단계: 사서함 준비](#step-2-prepare-the-mailbox)

[3 단계: 사서함에서 모든 보류 제거](#step-3-remove-all-holds-from-the-mailbox)

[4 단계: 사서함에서 지연 된 보류 제거](#step-4-remove-the-delay-hold-from-the-mailbox)

[5 단계: 복구 가능한 항목 폴더에서 항목 삭제](#step-5-delete-items-in-the-recoverable-items-folder)

[6 단계: 사서함을 이전 상태로 되돌리기](#step-6-revert-the-mailbox-to-its-previous-state)
  
> [!CAUTION]
> 이 문서에서 설명 하는 절차에 따라 Exchange Online 사서함에서 데이터가 영구적으로 삭제 (제거) 됩니다. 즉, 복구 가능한 항목 폴더에서 삭제 한 메시지는 복구할 수 없으며, 법적 검색 이나 다른 규정 준수 용도로는 사용할 수 없습니다. Office 365 보안 &amp; 및 준수 센터에서 만든 소송 보존, 원본 위치 유지, eDiscovery 보존 또는 office 365 보관 정책의 일부로 보류 중인 사서함의 메시지를 삭제 하려면 레코드 관리 또는 법적 법률을 확인 합니다. 보존을 제거 하기 전 부서 조직에 보류 중인 사서함 또는 데이터 유출 인시던트가 우선적으로 적용 되는지 여부를 정의 하는 정책이 있을 수 있습니다. 
  
## <a name="before-you-begin"></a>시작하기 전에

- 5 단계에서 복구 가능한 항목 폴더에서 메시지를 검색 하 고 삭제 하려면 Exchange Online의 다음 관리 역할을 둘 다 할당 해야 합니다.
    
  - **사서함 검색** -이 역할을 사용 하 여 조직의 사서함을 검색할 수 있습니다. Exchange 관리자에 게는 기본적으로이 역할이 할당 되지 않습니다. 자신을이 역할에 할당 하려면 자신을 Exchange Online의 검색 관리 역할 그룹의 구성원으로 추가 합니다. 
    
  - **사서함 가져오기 내보내기** -이 역할을 사용 하면 사용자 사서함에서 메시지를 삭제할 수 있습니다. 기본적으로이 역할은 역할 그룹에 할당 되지 않습니다. 사용자 사서함에서 메시지를 삭제 하려면 Exchange Online의 조직 관리 역할 그룹에 사서함 가져오기 내보내기 역할을 추가 하면 됩니다. 
    
- 이 문서에서 설명 하는 절차는 비활성 사서함에서는 지원 되지 않습니다. 이는 제거 후 보류 (또는 Office 365 보존 정책)를 비활성 사서함에 다시 적용할 수 없기 때문입니다. 비활성 사서함에서 보류를 제거 하면 일시 삭제 된 일반 사서함으로 변경 되 고 관리 되는 폴더 도우미에 의해 처리 된 후 조직에서 영구적으로 삭제 됩니다.
    
- 보존 잠금으로 잠긴 Office 365 보존 정책에 할당 된 사서함에 대해서는이 절차를 수행할 수 없습니다. 이는 보존 잠금 때문에 Office 365 보존 정책에서 사서함을 제거 하거나 제외 하 고 사서함에서 관리 되는 폴더 도우미를 사용 하지 않도록 설정할 수 없기 때문입니다. 보존 정책 잠금에 대 한 자세한 내용은 [잠금 a 보존 정책](retention-policies.md#locking-a-retention-policy)를 참조 하십시오.
    
- 사서함이 보류 되지 않거나 단일 항목 복구를 사용 하도록 설정 되지 않은 경우 복구 가능한 항목 폴더에서 항목을 삭제 하기만 하면 됩니다. 이 작업을 수행 하는 방법에 대 한 자세한 내용은 [메시지 검색 및 삭제 ](https://go.microsoft.com/fwlink/?linkid=852453)를 참조 하세요.
  
## <a name="step-1-collect-information-about-the-mailbox"></a>1 단계: 사서함에 대 한 정보 수집

첫 번째 단계는이 절차에 영향을 주는 대상 사서함에서 선택한 속성을 수집 하는 것입니다. 복구 가능한 항목 폴더에서 항목을 삭제 한 후 이러한 속성 중 일부를 변경 하 고 6 단계에서 원래 값으로 되돌리는 것 이므로 이러한 설정을 기록 하거나 텍스트 파일에 저장 해야 합니다. 여기에는 수집 해야 하는 사서함 속성의 목록이 나와 있습니다.
  
-  *singleitemrecoveryenabled* 및 *RetainDeletedItemsFor* ; 필요한 경우 한 번 복구를 사용 하지 않도록 설정 하 고 3 단계에서 삭제 된 항목 보존 기간을 늘립니다. 
    
-  *LitigationHoldEnabled* 및 *InPlaceHolds* 3 단계에서 일시적으로 제거할 수 있도록 사서함에 설정 된 모든 보류를 식별 해야 합니다. 사서함에 저장 될 수 있는 유형 보존을 식별 하는 방법에 대 한 팁을 보려면 [추가 정보](delete-items-in-the-recoverable-items-folder-of-mailboxes-on-hold.md#moreinfo) 섹션을 참조 하십시오. 
    
또한 사서함 클라이언트 액세스 설정을 일시적으로 사용 하지 않도록 설정 하 여 소유자 (또는 다른 사용자)가이 절차 중에 사서함에 액세스할 수 없도록 해야 합니다. 마지막으로 복구 가능한 항목 폴더의 현재 크기 및 항목 수를 가져올 수 있습니다. 5 단계에서 복구 가능한 항목 폴더의 항목을 삭제 한 후에는이 정보를 사용 하 여 항목이 실제로 제거 되었는지 확인 합니다.
  
1. [Exchange Online PowerShell에 연결](https://go.microsoft.com/fwlink/?linkid=396554)합니다. Exchange Online에서 적절 한 관리 역할이 할당 된 관리자 계정에 대해 사용자 이름과 암호를 사용 해야 합니다. 
    
2. 다음 명령을 실행 하 여 단일 항목 복구 및 삭제 된 항목 보존 기간에 대 한 정보를 가져옵니다.

    ```
    Get-Mailbox <username> | FL SingleItemRecoveryEnabled,RetainDeletedItemsFor
    ```

   단일 항목 복구를 사용 하도록 설정 하면 2 단계에서이를 사용 하지 않도록 설정 해야 합니다. 삭제 된 항목 보존 기간이 30 일 (Exchange Online의 최대값)으로 설정 되지 않은 경우 2 단계에서이를 늘릴 수 있습니다. 
    
3. 다음 명령을 실행 하 여 사서함에 대 한 사서함 액세스 설정을 가져옵니다. 
    
    ```
    Get-CASMailbox <username> | FL EwsEnabled,ActiveSyncEnabled,MAPIEnabled,OWAEnabled,ImapEnabled,PopEnabled
    ```

   2 단계에서 이러한 모든 access 메서드를 사용 하지 않도록 설정 합니다.
    
4. 다음 명령을 실행 하 여 사서함에 적용 된 보류 및 Office 365 보존 정책에 대 한 정보를 가져옵니다.
    
    ```
    Get-Mailbox <username> | FL LitigationHoldEnabled,InPlaceHolds
    ```


   > [!TIP]
    > *InPlaceHolds* 속성에 값이 너무 많고 이러한 속성이 모두 표시 되지 않는 경우에는 `Get-Mailbox <username> | Select-Object -ExpandProperty InPlaceHolds` 명령을 실행 하 여 각 값을 별도의 줄에 표시할 수 있습니다. 
  
5. 다음 명령을 실행 하 여 조직 전체 Office 365 보존 정책에 대 한 정보를 가져옵니다. 

    ```
    Get-OrganizationConfig | FL InPlaceHolds
    ```
   조직에서 조직 차원의 Office 365 보존 정책을 사용 하는 경우에는 3 단계에서 이러한 정책 으로부터 사서함을 제외 해야 합니다.

   > [!TIP]
    > *InPlaceHolds* 속성에 값이 너무 많고 이러한 속성이 모두 표시 되지 않는 경우에는 `Get-OrganizationConfig | Select-Object -ExpandProperty InPlaceHolds` 명령을 실행 하 여 각 값을 별도의 줄에 표시할 수 있습니다. 
  
6. 다음 명령을 실행 하 여 사용자의 기본 사서함에 있는 복구할 수 있는 항목 폴더에서 폴더 및 하위 폴더의 현재 크기와 총 항목 수를 가져옵니다. 

    ```
    Get-MailboxFolderStatistics <username> -FolderScope RecoverableItems | FL Name,FolderAndSubfolderSize,ItemsInFolderAndSubfolders
    ```

   사용자의 보관 사서함을 사용할 수 있는 경우 다음 명령을 실행 하 여 보관 사서함에서 복구 가능한 항목 폴더의 폴더 및 하위 폴더에 있는 항목의 크기 및 총 수를 가져옵니다. 

    ```s
    Get-MailboxFolderStatistics <username> -FolderScope RecoverableItems -Archive | FL Name,FolderAndSubfolderSize,ItemsInFolderAndSubfolders
    ```

   5 단계에서 항목을 삭제 하는 경우 사용자의 기본 보관 사서함에서 복구 가능한 항목 폴더의 항목을 삭제 하거나 삭제 하도록 선택할 수 있습니다. 사서함에 대해 자동 확장 보관을 사용 하도록 설정 된 경우 보조 보관 사서함의 항목은 삭제 되지 않습니다.
  
## <a name="step-2-prepare-the-mailbox"></a>2 단계: 사서함 준비

사서함에 대 한 정보를 수집 하 고 저장 한 다음에는 다음 작업을 수행 하 여 사서함을 준비 합니다. 
  
- 사서함 소유자가 사서함에 액세스할 수 없도록 사서함에 대 한 **클라이언트 액세스를 사용 하지 않도록 설정** 하 고이 절차 중에 사서함 데이터를 변경 합니다. 
    
- **삭제 된 항목 보존 기간** 을 5 단계에서 삭제 하기 전에 복구 가능한 항목 폴더에서 항목을 제거 하지 않도록 최대 30 일 (Exchange Online의 최대값)으로 늘립니다. 
    
- 5 단계에서 복구 가능한 항목 폴더에서 항목을 삭제 한 후 항목이 보존 되지 않도록 하려면 **단일 항목 복구를 사용 하지 않도록 설정** 합니다. 
    
- 사서함을 처리 하지 않고 5 단계에서 삭제 한 항목을 유지 하도록 **관리 되는 폴더 도우미를 사용 하지 않도록 설정 합니다** . 
    
Exchange Online PowerShell에서 다음 단계를 수행 합니다.
  
1. 다음 명령을 실행 하 여 사서함에 대 한 모든 클라이언트 액세스를 사용 하지 않도록 설정 합니다. 명령 구문에서는 사서함에서 모든 클라이언트 액세스 방법을 사용 하도록 설정 했다고 가정 합니다.

    ```   
    Set-CASMailbox <username> -EwsEnabled $false -ActiveSyncEnabled $false -MAPIEnabled $false -OWAEnabled $false -ImapEnabled $false -PopEnabled $false
    ```
   
   > [!NOTE]
    > 사서함에 대 한 모든 클라이언트 액세스 방법을 사용 하지 않도록 설정 하는 데 최대 60 분이 걸릴 수 있습니다. 이러한 access 메서드를 사용 하지 않도록 설정 해도 현재 로그인 되어 있는 사서함 소유자와의 연결이 끊어집니다. 소유자가 로그인 되어 있지 않으면 이러한 액세스 방법을 사용 하지 않도록 설정한 후에 사서함에 액세스할 수 없게 됩니다. 
  
2. 다음 명령을 실행 하 여 삭제 된 항목 보존 기간을 최대 30 일로 늘립니다. 이 경우 현재 설정이 30 일 미만인 것으로 가정 합니다. 

    ```
    Set-Mailbox <username> -RetainDeletedItemsFor 30
    ```

3. 다음 명령을 실행 하 여 단일 항목 복구를 사용 하지 않도록 설정 합니다.
    
    ```
    Set-Mailbox <username> -SingleItemRecoveryEnabled $false
    ```

   > [!NOTE]
    > 단일 항목 복구를 사용 하지 않도록 설정 하는 데 최대 60 분이 걸릴 수 있습니다. 이 기간이 경과할 때까지 복구 가능한 항목 폴더의 항목을 삭제 하지 마십시오. 
  
4. 다음 명령을 실행 하 여 관리 되는 폴더 도우미가 사서함을 처리 하지 못하게 합니다. 앞에서 설명한 것 처럼 보존 잠금이 있는 Office 365 보존 정책이 사서함에 적용 되지 않는 경우에만 관리 되는 폴더 도우미를 사용 하지 않도록 설정할 수 있습니다. 

    ```
    Set-Mailbox <username> -ElcProcessingDisabled $true
    ```

## <a name="step-3-remove-all-holds-from-the-mailbox"></a>3 단계: 사서함에서 모든 보류 제거

복구 가능한 항목 폴더에서 항목을 삭제 하는 마지막 단계는 사서함에 대해 1 단계에서 확인 한 모든 보류를 제거 하는 것입니다. 복구 가능한 항목 폴더에서 항목을 삭제 한 후에 항목이 보존 되지 않도록 하려면 모든 보존을 제거 해야 합니다. 다음 섹션에는 사서함에서 서로 다른 유형의 보류를 제거 하는 방법에 대 한 정보가 포함 되어 있습니다. 사서함에 저장 될 수 있는 유형 보존을 식별 하는 방법에 대 한 팁을 보려면 [추가 정보](#more-information) 섹션을 참조 하십시오. 자세한 내용은 [Exchange Online 사서함에 대해 설정 된 보류 유형을 식별](identify-a-hold-on-an-exchange-online-mailbox.md)하는 방법을 참조 하세요.
  
> [!CAUTION]
> 앞에서 설명한 것 처럼 사서함에서 보류를 제거 하기 전에 레코드 관리 또는 법률 부서에 문의 하세요. 
  
 ### <a name="litigation-hold"></a>소송 보존
  
Exchange Online PowerShell에서 다음 명령을 실행 하 여 사서함에서 소송 보존을 제거 합니다.

```
Set-Mailbox <username> -LitigationHoldEnabled $false
```

   
> [!NOTE]
> 클라이언트 액세스 방법 및 단일 항목 복구를 사용 하지 않도록 설정 하는 것과 마찬가지로 소송 보존을 제거 하는 데 최대 60 분이 걸릴 수 있습니다. 이 기간이 경과할 때까지 복구 가능한 항목 폴더에서 항목을 삭제 하지 마십시오. 
  
 ### <a name="in-place-hold"></a>원본 위치 유지
  
Exchange Online PowerShell에서 다음 명령을 실행 하 여 사서함에 배치 된 원본 위치 유지를 식별 합니다. 1 단계에서 확인 한 원본 위치 유지에 대해 GUID를 사용 합니다. 

```
Get-MailboxSearch -InPlaceHoldIdentity <hold GUID> | FL Name
```
   
원본 위치 유지를 확인 한 후 EAC (exchange 관리 센터) 또는 exchange Online PowerShell을 사용 하 여 보류에서 사서함을 제거할 수 있습니다. 자세한 내용은 원본 [위치 유지 만들기 또는 제거](https://go.microsoft.com/fwlink/?linkid=852668)를 참조 하세요.
  
 ### <a name="office-365-retention-policies-applied-to-specific-mailboxes"></a>특정 사서함에 적용 되는 Office 365 보존 정책
  
[office 365 보안 &amp; 준수 센터 PowerShell](https://go.microsoft.com/fwlink/?linkid=627084) 에서 다음 명령을 실행 하 여 사서함에 적용 되는 office 365 보존 정책을 식별 합니다. 1 단계에서 확인 한 보존 정책 `mbx` 에 `skp` 대해 또는 접두사를 제외 하 고 GUID를 사용 합니다. 

```
Get-RetentionCompliancePolicy <retention policy GUID without prefix> | FL Name
```
   
보존 정책을 파악 한 후에는 &amp; 보안 및 준수 센터의 **날짜 관리** \> **보존** 페이지로 이동 하 여 이전 단계에서 식별 한 보존 정책을 편집한 다음 목록에서 사서함을 제거 합니다. 보존 정책에 포함 된 받는 사람입니다. 
  
 ### <a name="organization-wide-office-365-retention-policies"></a>조직 전체 Office 365 보존 정책
  
조직 전체 및 Exchange 전체 Office 365 보존 정책은 조직의 모든 사서함에 적용 됩니다. 이러한 사용자는 조직 수준 (사서함 수준이 아님)에서 적용 되며 1 단계에서 **set-organizationconfig** cmdlet을 실행 하면 반환 됩니다. [보안 &amp; 준수 센터 PowerShell](https://go.microsoft.com/fwlink/?linkid=627084) 에서 다음 명령을 실행 하 여 조직 전반의 Office 365 보존 정책을 식별 합니다. 1 단계에서 확인 한 조직 차원의 `mbx` 보존 정책에 대해 접두사를 제외한 GUID를 사용 합니다. 

```
Get-RetentionCompliancePolicy <retention policy GUID without prefix> | FL Name
```

&amp; 조직 전반의 Office 365 보존 정책을 파악 한 후에는 보안 및 준수 센터의 **날짜 거 버 넌 스** \> **보존** 페이지로 이동 하 고, 이전 단계를 진행 하 고 제외 된 받는 사람 목록에 사서함을 추가 합니다. 이렇게 하면 보존 정책에서 사용자의 사서함이 제거 됩니다. 

### <a name="office-365-retention-labels"></a>Office 365 보존 레이블

사용자가 콘텐츠를 보존 하도록 구성 된 레이블을 적용할 때마다 해당 사서함의 폴더 또는 항목에 대 한 콘텐츠를 보존 하 고 삭제 하려면 *ComplianceTagHoldApplied* mailbox 속성을 **True**로 설정 합니다. 이 문제가 발생 하는 경우 사서함은 소송 보존에 적용 된 것으로 간주 되거나 Office 365 보관 정책에 할당 되는 것 처럼 유지 됩니다.

*ComplianceTagHoldApplied* 속성의 값을 확인 하려면 Exchange Online PowerShell에서 다음 명령을 실행 합니다.

```
Get-Mailbox <username> |FL ComplianceTagHoldApplied
```

폴더 또는 항목에 보존 레이블이 적용 되므로 사서함이 보류 중인 것을 확인 한 후에는 Security & 준수 센터의 콘텐츠 검색 도구를 사용 하 여 new-compliancetag 검색 조건을 사용 하 여 레이블이 지정 된 항목을 검색할 수 있습니다. 자세한 내용은 [키워드 쿼리 및 검색 조건에서 콘텐츠 검색에 대 한](keyword-queries-and-search-conditions.md#conditions-for-common-properties)"검색 조건" 섹션을 참조 하십시오.

레이블에 대 한 자세한 내용은 Overview in [Office 365 labels](labels.md)를 참조 하십시오.

 ### <a name="ediscovery-case-holds"></a>eDiscovery 사례 보류
  
[보안 &amp; 준수 센터 PowerShell](https://go.microsoft.com/fwlink/?linkid=627084) 에서 다음 명령을 실행 하 여 사서함에 적용 된 eDiscovery 사례와 관련 된 보류를 확인 합니다. 1 단계에서 확인 한 eDiscovery 보존 `UniH` 에 대 한 GUID (접두사를 포함 하지 않음)를 사용 합니다. 두 번째 명령은 보류가 연결 된 eDiscovery 사례의 이름을 표시 합니다. 세 번째 명령은 보류의 이름을 표시 합니다. 
  
```
$CaseHold = Get-CaseHoldPolicy <hold GUID without prefix>
```

```
Get-ComplianceCase $CaseHold.CaseId | FL Name
```

```
$CaseHold.Name
```

eDiscovery 사례 및 보류의 이름을 식별 한 후에는 &amp; 보안 및 준수 센터의 **검색 &amp; 조사** **** \> eDiscovery 페이지로 이동한 후 사례를 열고 해당 사서함을 보류에서 제거 합니다. 자세한 내용은 [Office 365 보안 &amp; 및 준수 센터에서 eDiscovery 사례 관리](manage-ediscovery-cases.md)를 참조 하세요.
  
## <a name="step-4-remove-the-delay-hold-from-the-mailbox"></a>4 단계: 사서함에서 지연 된 보류 제거

사서함에서 모든 유형의 보류가 제거 된 후에는 *DelayHoldApplied* mailbox 속성의 값이 **True**로 설정 됩니다. 다음 번에 관리 되는 폴더 도우미가 사서함을 처리 하 고 보류가 제거 되었음을 감지할 때 이러한 상황이 발생 합니다. 이를 *지연 보존* 이라고 하며, 데이터가 사서함에서 영구적으로 삭제 되는 것을 방지 하기 위해 보류의 실제 제거가 30 일 동안 지연 되는 것을 의미 합니다. 지연 보존의 목적은 관리자가 보류를 제거한 후 삭제 될 사서함 항목을 검색 하거나 복구할 수 있도록 하는 것입니다.  사서함에 연기 대기를 설정 하면 사서함이 소송 보존 상태에 있는 것 처럼 여전히 무제한 기간 동안 유지 되는 것으로 간주 됩니다. 30 일 후에 지연 보류가 만료 되 고 Office 365에서 자동으로 지연 대기 ( *DelayHoldApplied* 속성을 **False**로 설정)을 제거 하 여 보류를 실제로 제거 하려고 합니다. 

5 단계에서 항목을 삭제 하려면 먼저 사서함에서 지연 유지를 제거 해야 합니다. 먼저 Exchange Online PowerShell에서 다음 명령을 실행 하 여 지연 보류가 사서함에 적용 되는지 확인 합니다.

```
Get-Mailbox <username> | FL DelayHoldApplied
```

*DelayHoldApplied* 속성 값을 **False**로 설정 하면 대기 시간이 사서함에 저장 되지 않은 것입니다. 5 단계까지 이동 하 여 복구 가능한 항목 폴더의 항목을 삭제할 수 있습니다.

*DelayHoldApplied* 속성 값이 **True**로 설정 된 경우 다음 명령을 실행 하 여 지연 보존을 제거 합니다.

```
Set-Mailbox <username> -RemoveDelayHoldApplied
```
*RemoveDelayHoldApplied* 매개 변수를 사용 하려면 Exchange Online의 법적 보존 역할을 할당 받아야 합니다.

## <a name="step-5-delete-items-in-the-recoverable-items-folder"></a>5 단계: 복구 가능한 항목 폴더에서 항목 삭제

이제 Exchange Online PowerShell의 [검색 사서함](https://go.microsoft.com/fwlink/?linkid=852595) cmdlet을 사용 하 여 복구 가능한 항목 폴더의 항목을 실제로 삭제할 준비가 되었습니다. **검색 사서함** cmdlet을 실행할 때는 다음과 같은 세 가지 옵션을 사용할 수 있습니다. 
  
- 삭제 하기 전에 대상 사서함에 항목을 복사 하 여 필요한 경우 항목을 검토 한 다음 삭제할 수 있도록 합니다.
    
- 항목을 대상 사서함으로 복사 하 고 같은 명령에서 삭제 합니다.
    
- 항목을 대상 사서함에 복사 하지 않고 삭제 합니다. 
    
**검색 사서함** cmdlet을 실행 하면 사용자의 기본 보관 사서함에 있는 복구 가능한 항목 폴더의 항목도 삭제 됩니다. 이를 방지 하기 위해 *만드는 경우 donotincludearchive* 스위치를 포함할 수 있습니다. 앞에서 설명한 것 처럼 사서함에 대해 자동 확장 보관을 사용 하도록 설정 된 경우 * * 검색 사서함 * * cmdlet은 보조 보관 사서함의 항목을 삭제 하지 않습니다. 자동 확장 보관에 대 한 자세한 내용은 [Office 365의 무제한 보관 개요](unlimited-archiving.md)를 참조 하세요.
  
> [!NOTE]
> *searchquery* 매개 변수를 사용 하 여 검색 쿼리를 포함 하는 경우 검색 **사서함** cmdlet은 최대 1만 개의 항목을 검색 결과에 반환 합니다. 따라서 검색 쿼리를 포함 하는 경우 1만 개 보다 많은 항목을 삭제 하려면 **검색 사서함** 명령을 여러 번 실행 해야 할 수 있습니다. 
  
다음 예제에는 이러한 각 옵션에 대 한 명령 구문이 나와 있습니다. 다음은 `-SearchQuery size>0` 복구 가능한 항목 폴더의 모든 하위 폴더에서 모든 항목을 삭제 하는 매개 변수 값을 사용 하는 예제입니다. 특정 조건과 일치 하는 항목만 삭제 해야 하는 경우에는 *searchquery* 매개 변수를 사용 하 여 메시지 제목 또는 날짜 범위와 같은 다른 조건을 지정할 수도 있습니다. 아래에서 [searchquery 매개 변수를 사용 하는 다른 예](#other-examples-of-using-the-searchquery-parameter) 를 참조 하십시오. 
  
### <a name="example-1"></a>예 1

이 예에서는 사용자의 복구할 수 있는 항목 폴더에 있는 모든 항목을 조직의 검색 사서함에 있는 폴더로 복사 합니다. 이렇게 하면 항목을 영구적으로 삭제 하기 전에 검토할 수 있습니다.

```
Search-Mailbox <username> -SearchQuery size>0 -SearchDumpsterOnly -TargetMailbox "Discovery Search Mailbox" -TargetFolder "<foldername>"
```

이전 예제에서는 항목을 검색 검색 사서함에 복사할 필요가 없습니다. 모든 대상 사서함에 메시지를 복사할 수 있습니다. 그러나 중요 한 사서함 데이터에 대 한 액세스를 방지 하려면 액세스 권한이 있는 개인만 액세스할 수 있는 사서함으로 메시지를 복사 하는 것이 좋습니다. 기본적으로 Exchange Online의 검색 관리 역할 그룹 구성원에 게는 기본 검색 사서함에 대 한 액세스가 제한 됩니다. 
  
### <a name="example-2"></a>예 2

이 예에서는 복구 가능한 항목 폴더의 모든 항목을 조직의 검색 사서함에 있는 폴더로 복사한 다음 사용자의 복구 가능한 항목 폴더에서 해당 항목을 삭제 합니다.

```
Search-Mailbox <username> -SearchQuery size>0 -SearchDumpsterOnly -TargetMailbox "Discovery Search Mailbox" -TargetFolder "<foldername>" -DeleteContent
```
 
### <a name="example-3"></a>예 3

이 예에서는 사용자의 복구 가능한 항목 폴더에서 대상 사서함으로 복사 하지 않고 모든 항목을 삭제 합니다. 

```
Search-Mailbox <username> -SearchQuery size>0 -SearchDumpsterOnly -DeleteContent
```

### <a name="other-examples-of-using-the-searchquery-parameter"></a>searchquery 매개 변수를 사용 하는 다른 예

다음은 *searchquery* 매개 변수를 사용 하 여 특정 메시지를 찾는 몇 가지 예입니다. *searchquery* 매개 변수를 사용 하 여 특정 항목을 검색 하는 경우 검색 결과를 검토 한 다음 검색 결과를 삭제 하기 전에 필요한 경우 쿼리를 수정할 수 있도록 결과를 대상 사서함으로 복사 하는 것이 좋습니다. 
  
다음은 제목 필드에 특정 구를 포함 하는 메시지를 반환 하는 예제입니다.
  
```
SearchQuery 'subject:"MAIL_BOX VALIDATION/UPGRADE!!!"' 
```

이 예에서는 지정 된 날짜 범위 내에 전송 된 메시지를 반환 합니다.
  
```
SearchQuery 'sent>=06/01/2016 AND sent<=09/01/2016'
```
 
이 예제에서는 지정 된 사람에 게 전송 된 메시지를 반환 합니다.

```
SearchQuery 'to:garthf@alpinehouse.com'
```
   
### <a name="verify-that-items-were-deleted"></a>항목이 삭제 되었는지 확인

사서함의 복구할 수 있는 항목 폴더에서 항목이 삭제 되었는지 확인 하려면 Exchange Online PowerShell에서 **get-mailboxfolderstatistics** cmdlet을 사용 하 여 복구 가능한 항목 폴더의 항목 크기 및 수를 확인 합니다. 이러한 통계를 1 단계에서 수집한 것과 비교할 수 있습니다. 
  
에서 다음 명령을 실행 하 여 사용자의 기본 사서함에 있는 복구할 수 있는 항목 폴더에서 폴더 및 하위 폴더의 현재 크기와 총 항목 수를 가져옵니다. 
  
```
Get-MailboxFolderStatistics <username> -FolderScope RecoverableItems | FL Name,FolderAndSubfolderSize,ItemsInFolderAndSubfolders
```
   
다음 명령을 실행 하 여 사용자의 보관 사서함에 있는 복구 가능한 항목 폴더의 폴더 및 하위 폴더에 있는 항목의 크기 및 총 수를 가져옵니다. 

```
Get-MailboxFolderStatistics <username> -FolderScope RecoverableItems -Archive | FL Name,FolderAndSubfolderSize,ItemsInFolderAndSubfolders
```
  
## <a name="step-6-revert-the-mailbox-to-its-previous-state"></a>6 단계: 사서함을 이전 상태로 되돌리기

마지막 단계는 사서함을 다시 이전 구성으로 되돌리는 것입니다. 즉, 2 단계에서 변경한 속성을 다시 설정 하 고 3 단계에서 제거한 보존을 다시 적용 합니다. 여기에는 다음이 포함 됩니다.
  
- 삭제 된 항목 보존 기간을 이전 값으로 변경 또는 Exchange Online에서이 설정을 최대 30 일로 그대로 두면 됩니다.
    
- 단일 항목 복구를 다시 사용 하도록 설정 합니다.
    
- 소유자가 자신의 사서함에 액세스할 수 있도록 클라이언트 액세스 방법을 다시 사용 하도록 설정 합니다.
    
- 제거한 보류 및 Office 365 보존 정책을 다시 적용 합니다.
    
- 관리 되는 폴더 도우미가 사서함을 처리할 수 있도록 다시 설정 합니다.
    
> [!IMPORTANT]
> 관리 되는 폴더 도우미가 사서함을 처리 하도록 다시 설정 하기 전에 보류 또는 Office 365 보존 정책을 다시 적용 하 고 현재 위치에 있는지 확인 한 후 24 시간을 기다리는 것이 좋습니다. 
  
Exchange Online PowerShell에서 지정 된 순서 대로 다음 단계를 수행 합니다.
  
1. 다음 명령을 실행 하 여 삭제 된 항목 보존 기간을 원래 값으로 변경 합니다. 이는 이전 설정이 30 일 보다 작은 것으로 가정 합니다. 예: 14 일 
    
    ```
    Set-Mailbox <username> -RetainDeletedItemsFor 14
    ```
   
2. 다음 명령을 실행 하 여 단일 항목 복구를 다시 사용 하도록 설정 합니다.
   
    ```
    Set-Mailbox <username> -SingleItemRecoveryEnabled $true
    ```

3. 다음 명령을 실행 하 여 사서함에 대 한 모든 클라이언트 액세스 방법을 다시 사용 하도록 설정 합니다.
    
    ```
    Set-CASMailbox <username> -EwsEnabled $true -ActiveSyncEnabled $true -MAPIEnabled $true -OWAEnabled $true -ImapEnabled $true -PopEnabled $true
    ```
   
4. 3 단계에서 제거한 보존을 다시 적용 합니다. 보존 유형에 따라 다음 절차 중 하나를 사용 합니다.
    
    **소송 보존**
    
    다음 명령을 실행 하 여 사서함에 대 한 소송 보존을 다시 사용 하도록 설정 합니다.
    
    ```
    Set-Mailbox <username> -LitigationHoldEnabled $true
    ```

    **원본 위치 유지**
    
    EAC (또는 Exchange Online PowerShell)를 사용 하 여 사서함을 원본 위치 유지 상태로 다시 추가 합니다. 
    
    **특정 사서함에 적용 되는 Office 365 보존 정책**
    
    보안 &amp; 및 준수 센터를 사용 하 여 사서함을 다시 Office 365 보존 정책에 추가 합니다. 보안 &amp; 및 준수 센터의 **날짜 거 버 넌 스** \> **보존** 페이지로 이동 하 여 보존 정책을 편집한 다음 보존 정책이 적용 되는 받는 사람 목록에 사서함을 다시 추가 합니다. 
    
    **조직 전체 Office 365 보존 정책**
    
    정책에서 조직 전체 또는 Exchange 전체 보존 정책을 제거한 경우에는 보안 &amp; 및 준수 센터를 사용 하 여 제외 된 사용자 목록에서 해당 사서함을 제거 합니다. 보안 &amp; 및 준수 센터의 **날짜 거 버 넌 스** \> **보존** 페이지로 이동 하 여 조직 차원의 보존 정책을 편집 하 고 제외 된 받는 사람 목록에서 해당 사서함을 제거 합니다. 이렇게 하면 보존 정책이 사용자 사서함에 다시 적용 됩니다. 
    
    **eDiscovery 사례 보류**
    
    보안 &amp; 및 준수 센터를 사용 하 여 eDiscovery 사례와 연결 된 보류를 다시 사서함에 추가 합니다. 보안 &amp; 및 준수 센터의 ** &amp; 검색 조사** \> **eDiscovery** 페이지로 이동 하 여 사례를 열고 사서함을 보류에 다시 추가 합니다. 
    
5. 다음 명령을 실행 하 여 관리 되는 폴더 도우미가 사서함을 다시 처리할 수 있도록 합니다. 앞에서 설명한 것 처럼 관리 되는 폴더 도우미를 다시 사용 하도록 설정 하기 전에 보류 또는 Office 365 보존 정책을 다시 적용 하 고 현재 위치에 있는지 확인 한 후 24 시간을 기다리는 것이 좋습니다. 

    ```
    Set-Mailbox <username> -ElcProcessingDisabled $false
    ```
   
6. 사서함이 이전 구성으로 되돌아간 것을 확인 하려면 다음 명령을 실행 하 여 1 단계에서 수집한 설정과 비교 합니다.

    ```
    Get-Mailbox <username> | FL ElcProcessingDisabled,InPlaceHolds,LitigationHoldEnabled,RetainDeletedItemsFor,SingleItemRecoveryEnabled
    ```

    ```
    Get-CASMailbox <username> | FL EwsEnabled,ActiveSyncEnabled,MAPIEnabled,OWAEnabled,ImapEnabled,PopEnabled
    ```
  
## <a name="more-information"></a>추가 정보

다음은 *InPlaceHolds* 속성의 값에 따라 **get-Mailbox** 또는 **set-organizationconfig** cmdlet을 실행할 때 서로 다른 유형의 보류를 식별 하는 방법을 설명 하는 표입니다. 자세한 내용은 [Exchange Online 사서함에 대해 설정 된 보류 유형을 식별](identify-a-hold-on-an-exchange-online-mailbox.md)하는 방법을 참조 하세요.

앞에서 설명한 것 처럼 복구 가능한 항목 폴더의 항목을 성공적으로 삭제 하려면 먼저 사서함에서 모든 보류 및 Office 365 보존 정책을 제거 해야 합니다. 
  
|**보류 유형**|**예제 값**|**보류를 확인 하는 방법**|
|:-----|:-----|:-----|
|소송 보존  <br/> | `True` <br/> |*LitigationHoldEnabled* 속성은로 `True`설정 됩니다.  <br/> |
|원본 위치 유지  <br/> | `c0ba3ce811b6432a8751430937152491` <br/> |*InPlaceHolds* 속성은 사서함에 배치 된 원본 위치 유지의 GUID를 포함 합니다. GUID가 접두사로 시작 되지 않으므로 현재 위치 유지로 설정할 수 있습니다.<br/> Exchange Online PowerShell의 `Get-MailboxSearch -InPlaceHoldIdentity <hold GUID> | FL` 명령을 사용 하 여 사서함의 원본 위치 유지에 대 한 정보를 가져올 수 있습니다.  <br/> |
| 특정 사서함에 적용 되는 보안 &amp; 준수 센터의 Office 365 보존 정책  <br/> | `mbxcdbbb86ce60342489bff371876e7f224` <br/> 또는  <br/>  `skp127d7cf1076947929bf136b7a2a8c36f` <br/> |**사서함** 관리 cmdlet을 실행 하는 경우 *InPlaceHolds* 속성에는 사서함에 적용 되는 Office 365 보존 정책의 guid도 포함 되어 있습니다. GUID는 `mbx` 접두사로 시작 되므로 보존 정책을 식별할 수 있습니다. 보존 정책의 GUID가 `skp` 접두사로 시작 되 면 보존 정책이 비즈니스용 Skype 대화에 적용 됨을 나타내는 것을 볼 수 있습니다.<br/> 사서함에 적용 되는 Office 365 보존 정책을 식별 하려면 보안 &amp; 준수 센터 PowerShell에서 다음 명령을 실행 합니다. <br/> <br/>`Get-RetentionCompliancePolicy <retention policy GUID without prefix> | FL Name`<br/><br/>이 명령을 실행할 때 `mbx` or `skp` 접두사를 제거 해야 합니다.  <br/> |
|보안 &amp; 및 준수 센터의 조직 전체 Office 365 보존 정책  <br/> |No 값  <br/> 또는  <br/>  `-mbxe9b52bf7ab3b46a286308ecb29624696`(사서함이 조직 차원 정책에서 제외 됨을 나타냄)  <br/> |*InPlaceHolds* 속성이 비어 있는 경우에도 사서함 cmdlet을 실행할 **** 때 하나 이상의 조직 수준 Office 365 보존 정책이 사서함에 적용 될 수 있습니다.  <br/> 이를 확인 하려면 Exchange Online PowerShell에서 `Get-OrganizationConfig | FL InPlaceHolds` 명령을 실행 하 여 조직 전반의 Office 365 보존 정책의 guid 목록을 가져올 수 있습니다. Exchange 사서함에 적용 되는 조직 수준 보존 정책의 GUID는 `mbx` 접두사로 시작 합니다. 예를 `mbxa3056bb15562480fadb46ce523ff7b02`들어<br/> 사서함에 적용 되는 조직 차원의 Office 365 보존 정책을 식별 하려면 보안 &amp; 준수 센터 PowerShell에서 다음 명령을 실행 합니다. <br/><br/> `Get-RetentionCompliancePolicy <retention policy GUID without prefix> | FL Name`<br/><br/>사서함이 조직 차원의 Office 365 보존 정책에서 제외 되는 경우 **사서함** cmdlet을 실행 하면 보존 정책의 GUID가 사용자 사서함의 *InPlaceHolds* 속성에 표시 됩니다. 이 접두사는 접두사로 `-mbx`식별 됩니다. 예를 들어`-mbxe9b52bf7ab3b46a286308ecb29624696` <br/> |
|보안 &amp; 및 준수 센터에서 eDiscovery 사례 보류  <br/> | `UniH7d895d48-7e23-4a8d-8346-533c3beac15d` <br/> |*InPlaceHolds* 속성에는 사서함에 배치 될 수 있는 보안 &amp; 및 준수 센터에서 eDiscovery 사례와 관련 된 보류의 GUID도 포함 됩니다. GUID는 `UniH` 접두사로 시작 되므로 eDiscovery 사례 보류 임을 확인할 수 있습니다.<br/> 보안 &amp; 및 준수 센터 `Get-CaseHoldPolicy` PowerShell에서 cmdlet을 사용 하 여 사서함의 보류가 연결 된 eDiscovery 사례에 대 한 정보를 확인할 수 있습니다. 예를 들어 명령을 `Get-CaseHoldPolicy <hold GUID without prefix> | FL Name` 실행 하 여 사서함에 대 한 케이스 보류의 이름을 표시할 수 있습니다. 이 명령을 실행할 때 `UniH` 접두사를 제거 해야 합니다.<br/><br/> 사서함의 보류가 연결 된 eDiscovery 사례를 식별 하려면 다음 명령을 실행 합니다.<br/><br/>`$CaseHold = Get-CaseHoldPolicy <hold GUID without prefix>`<br/><br/>`Get-ComplianceCase $CaseHold.CaseId | FL Name`


