---
title: 관리자 도움말 대기-클라우드 기반 사서함의 복구 가능한 항목 폴더에서 항목 삭제
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 9/21/2017
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MOE150
- MET150
ms.assetid: a85e1c87-a48e-4715-bfa9-d5275cde67b0
description: '관리자를 위한: 해당 사서함이 법적 보유 중일 경우에 Exchange Online 사서함에 대 한 사용자의 복구 가능한 항목 폴더에서 항목을 삭제 합니다. 이것이 Office 365에 실수로 넘어가 되는 데이터를 삭제할 수 있는 효과적인 방법입니다.'
ms.openlocfilehash: c984bcaa35a9bc7bc30e11d68ba8f7f0ce75b64d
ms.sourcegitcommit: 31e0d94244c76a9f5118efee8bbc93395d080f91
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/01/2018
ms.locfileid: "23796884"
---
# <a name="delete-items-in-the-recoverable-items-folder-of-cloud-based-mailboxes-on-hold---admin-help"></a>관리자 도움말 대기-클라우드 기반 사서함의 복구 가능한 항목 폴더에서 항목 삭제

Exchange Online 사서함에 대 한 복구 가능한 항목 폴더에서 실수로 또는 악의적 삭제 보호 하기 위해 존재 합니다. 또한 유지 되 고, 검색 보류 및 eDiscovery와 같은 Office 365 규정 준수 기능에 액세스 하는 항목을 저장 하는데 사용 됩니다. 그러나 일부 상황에서 조직에는 실수로 삭제 해야 자신이 복구 가능한 항목 폴더에 보존 된 하는 데이터 있을 수 있습니다. 등 사용자 수 모른 보내기 또는 중요 한 정보 또는 심각한 비즈니스 영향을 미칠 수 있는 정보를 포함 하는 전자 메일 메시지를 전달 합니다. 메시지를 영구적으로 삭제 하는 경우에 것 수 보존할 무기한 법적 보유가 사서함에 배치 되어 있으므로 합니다. 이 시나리오는 Office 365에 데이터를 실수로 넘어가 된 되므로 데이터 액체 엎질렀는지 여부 라고 합니다. 이러한 상황에서 해당 사서함이 대기 상태에 놓일 Office 365의 다른 보류 기능 중 하나를 사용 하는 경우에 Exchange Online 사서함에 대 한 사용자의 복구 가능한 항목 폴더에서 항목을 삭제할 수 있습니다. 이러한 유형의 보류 소송 보존을 포함 하 고, 원본 위치 유지, eDiscovery 보류 및 Office 365 보안에서 만든 Office 365 보존 정책이 포함 &amp; 준수 센터입니다. 
  
 이 문서에서는 보류에 있는 클라우드 기반 사서함에 대 한 복구 가능한 항목 폴더에서 항목을 삭제 하는 방법에 설명 합니다. 이 절차는 사서함에 대 한 액세스를 사용 하지 않도록 설정 하 고는 관리 되는 폴더 도우미에서 사서함을 처리, 일시적으로 보류를 제거 하 고, 복구 가능한 항목 폴더에서 항목을 삭제 하 고 되돌리는 다음을 사용 하지 않도록 설정 하는 단일 항목 복구를 사용 하지 않도록 설정 사서함의 이전 구성입니다. 하는 프로세스는 다음과 같습니다. 
  
[1 단계: 사서함에 대 한 정보를 수집 합니다.](#step-1-collect-information-about-the-mailbox)

[2 단계: 사서함 준비](#step-2-prepare-the-mailbox)

[3 단계: 사서함에서 모든 보류를 제거 합니다.](#step-3-remove-all-holds-from-the-mailbox)

[복구 가능한 항목 폴더에서 항목을 삭제 하는 4 단계:](#step-4-delete-items-in-the-recoverable-items-folder)

[5 단계: 사서함을 이전 상태로 되돌리기](#step-5-revert-the-mailbox-to-its-previous-state)
  
> [!CAUTION]
> 이 문서에 설명 된 절차 될 되는 데이터 영구적으로 삭제 (비우기)에서 Exchange Online 사서함 수 있습니다. 즉, 메시지 복구 가능한 항목 폴더에서 삭제를 복구할 수 없는 및 법적 개시 또는 기타 준수 용도로 사용할 수 없습니다. 원본 위치 유지는 소송 보존의 일환으로 보류에 추가 되는 사서함에서 메시지를 삭제 하려는 경우 eDiscovery 보류 또는 Office 365 보안에서 Office 365 보존 정책을 만든 &amp; 준수 센터, 레코드 관리 또는 법률 확인 보류를 제거 하기 전에 부서 합니다. 조직에 사서함에 보존 여부를 정의 하는 정책을 사용할 수 있습니다 또는 데이터 액체 엎질렀는지 여부 문제가 발생 한 설정이 우선 합니다. 
  
## <a name="before-you-begin"></a>시작하기 전에

- 다음 관리 역할을 모두 Exchange Online에 할당할를 검색 하 고 4 단계에서에서 복구 가능한 항목 폴더에서 메시지를 삭제 해야 합니다.
    
  - **사서함 검색** -이 역할을 사용 하면 조직에서 사서함을 검색할 수 있습니다. Exchange 관리자가 기본적으로이 역할을 할당 되지 않습니다. 사용자가 직접이 역할을 할당 하려면 추가 자신 검색 관리 역할 그룹의 구성원으로 Exchange Online 합니다. 
    
  - **사서함 가져오기 내보내기** -이 역할을 통해 사용자의 사서함에서 메시지를 삭제할 수 있습니다. 기본적으로이 역할은 모든 역할 그룹에 할당 되지 않습니다. 사용자의 사서함에서 메시지를 삭제 하려면 추가할 수 있습니다는 사서함 가져오기 내보내기 역할 조직 관리 역할 그룹에 Exchange 온라인. 
    
- 이 문서에서 설명 하는 절차는 비활성 사서함에 대 한 지원 되지 않습니다. 있기 때문입니다 보류 (또는 Office 365 보존 정책)를 다시 적용할 수 없습니다 비활성 사서함을 제거 하면 됩니다. 비활성 사서함에서 보류를 제거할 때 기본 일시 삭제 된 사서함으로 변경 되 고 관리 하는 폴더 도우미에 의해 처리 된 후 조직에서 영구적으로 삭제 됩니다.
    
- 보존 잠금을 사용 하 여 잠긴 되는 Office 365 보존 정책에 할당 된 사서함에 대해이 절차를 수행할 수 없습니다. 보존 잠금을 제거 하거나는 관리 되는 폴더 도우미는 사서함에서 사용 하지 않도록 설정 및 Office 365 보존 정책에서 사서함을 제외 하면 때문입니다. 보존 정책 잠금에 대 한 자세한 내용은 [보존 정책 잠금](retention-policies.md#locking-a-retention-policy)을 참조 하십시오.
    
- 사서함 보류에 추가 되지 않습니다 (또는 단일 항목 복구를 사용할 수 없으면) 하는 경우에 복구 가능한 항목 폴더에서 항목을 간단히 삭제할 수 있습니다. 이 작업을 수행 하는 방법에 대 한 자세한 내용은 [메시지에 대 한 검색 및 삭제를 ](https://go.microsoft.com/fwlink/?linkid=852453)참조 하십시오.
  
## <a name="step-1-collect-information-about-the-mailbox"></a>1 단계: 사서함에 대 한 정보를 수집 합니다.

이 첫번째 단계가이 절차에 영향을 주는 대상 사서함에서 선택 된 속성을 수집 하는 것입니다. 이러한 설정을 기록해 또는 이러한 속성 중 일부를 변경 하 고 복구 가능한 항목 폴더에서 항목을 삭제 한 후 5 단계에서에서 원래 값으로 다시 만든 다음 되돌릴 수 있으므로 텍스트 파일에 저장 해야 합니다. 다음은 수집 해야하는 사서함 속성의 목록입니다.
  
-  *SingleItemRecoveryEnabled* 및 *RetainDeletedItemsFor* ; 필요한 경우 단일 복구를 사용 하지 않도록 설정 하 고 3 단계에서에서 삭제 된 항목 보존 기간을 늘립니다. 
    
-  *LitigationHoldEnabled* 및 *InPlaceHolds* ; 3 단계에서에서 일시적으로 제거할 수 있도록 사서함에 배치 하는 모든 보류를 식별 해야 합니다. 사서함에 배치 될 수 있는 형식 보류를 식별 하는 방법에 대 한 팁에 대 한 [자세한 내용](delete-items-in-the-recoverable-items-folder-of-mailboxes-on-hold.md#moreinfo) 은 섹션을 참조 하십시오. 
    
또한 있도록 가져옵니다. 사서함 클라이언트 액세스 설정을 해제할 수 있습니다 일시적으로 소유자 (또는 다른 사용자에 게) 하는 동안이 절차는 사서함에 액세스할 수 없습니다 있도록 필요 합니다. 마지막으로 복구 가능한 항목 폴더의 현재 크기 및 항목 수를 얻을 수 있습니다. 4 단계에서에서 복구 가능한 항목 폴더에서 항목을 삭제 한 후이 정보를 사용 하 여 실제로 제거 된 항목을 확인 하기 위해 표시 됩니다.
  
1. [Exchange Online PowerShell에 연결](https://go.microsoft.com/fwlink/?linkid=396554)합니다. Exchange Online에서 적절 한 관리 역할 할당 된 관리자 계정에 대 한 사용자 이름 및 암호를 사용 해야 합니다. 
    
2. 단일 항목 복구 하 고 삭제 된 항목 보존 기간에 대 한 정보를 가져오려면 다음 명령을 실행 합니다.

    ```
    Get-Mailbox <username> | FL SingleItemRecoveryEnabled,RetainDeletedItemsFor
    ```

   단일 항목 복구를 사용 하는 경우 2 단계에서에서 사용 하지 않도록 설정 해야 합니다. 하는 경우 삭제 된 항목 보존 기간을 30 일 동안 설정 되지 않습니다 (Exchange Online의 최대 값) 다음 2 단계에서에서 늘릴 수 있습니다. 
    
3. 사서함의 사서함에 대 한 액세스 설정 하려면 다음 명령을 실행 합니다. 
    
    ```
    Get-CASMailbox <username> | FL EwsEnabled,ActiveSyncEnabled,MAPIEnabled,OWAEnabled,ImapEnabled,PopEnabled
    ```

   2 단계에서에서 이러한 액세스 방법의 모든를 비활성화할 수 있습니다.
    
4. 보류 및 사서함에 적용 된 Office 365 보존 정책에 대 한 정보를 가져오려면 다음 명령을 실행 합니다.
    
    ```
    Get-Mailbox <username> | FL LitigationHoldEnabled,InPlaceHolds
    ```


   > [!TIP]
    > 실행할 수 *InPlaceHolds* 속성에 너무 많은 값이 모두 하지 표시 하는 경우는 `Get-Mailbox <username> | Select-Object -ExpandProperty InPlaceHolds` 별도 줄에 각 값을 표시 하는 명령입니다. 
  
5. 모든 조직 전체의 Office 365 보존 정책에 대 한 정보를 가져오려면 다음 명령을 실행 합니다. 

    ```
    Get-OrganizationConfig | FL InPlaceHolds
    ```
   조직에 있는 조직 수준의 Office 365 보존 정책, 3 단계에서에서 이러한 정책에서 사서함을 제외 하도록 해야 합니다.

   > [!TIP]
    > 실행할 수 *InPlaceHolds* 속성에 너무 많은 값이 모두 하지 표시 하는 경우는 `Get-OrganizationConfig | Select-Object -ExpandProperty InPlaceHolds` 별도 줄에 각 값을 표시 하는 명령입니다. 
  
6. 폴더와 사용자의 기본 사서함의 복구 가능한 항목 폴더에 하위 폴더에서 항목의 총 수와 현재 크기를 가져오려면 다음 명령을 실행 합니다. 

    ```
    Get-MailboxFolderStatistics <username> -FolderScope RecoverableItems | FL Name,FolderAndSubfolderSize,ItemsInFolderAndSubfolders
    ```

   폴더 및 보관 사서함의 복구 가능한 항목 폴더에 하위 폴더의 크기와 총 항목 수를 가져오려면 다음 명령을 실행 하는 사용자의 보관 사서함을 사용 하는 경우. 

    ```s
    Get-MailboxFolderStatistics <username> -FolderScope RecoverableItems -Archive | FL Name,FolderAndSubfolderSize,ItemsInFolderAndSubfolders
    ```

   4 단계에서에서 항목을 삭제 하는 경우에 삭제 또는 사용자의 기본 보관 사서함의 복구 가능한 항목 폴더에서 항목을 삭제 하지를 선택할 수 있습니다. 참고 보관 자동을 확장 하면 해당 사서함에 대해 활성화 된 경우 보조 보관 사서함에 있는 항목은 삭제할 수 없습니다.
  
## <a name="step-2-prepare-the-mailbox"></a>2 단계: 사서함 준비

수집 하 고 사서함에 대 한 정보를 저장 한 후 다음 단계는 다음과 같은 작업을 수행 하 여 사서함을 준비 하는 것: 
  
- **사서함에 대 한 클라이언트 액세스를 사용 하지 않도록 설정** 하 사서함 소유자 수는 없습니다 자신의 사서함에 액세스 하 고이 절차는 동안 사서함 데이터를 변경 합니다. 
    
- 30 일에 **삭제 된 항목 보존 기간을 늘립니다** (Exchange Online의 최대값) 4 단계에서에서 삭제 하기 전에 복구 가능한 항목 폴더에서 항목 삭제 되지 않도록 합니다. 
    
- 4 단계에서에서 복구 가능한 항목 폴더에서 삭제 하면 (삭제 된 항목 보존 기간을 기간)에 대 한 **단일 항목 복구를 사용 하지 않도록 설정** 하는 항목이 있으므로 유지 되지 않을 것입니다. 
    
- It 관리 사서함을 처리 하며 4 단계에서에서 삭제 된 항목을 유지 하지 않도록 **관리 되는 폴더 도우미를 사용 하지 않도록** 합니다. 
    
Exchange Online PowerShell에서 다음 단계를 수행 합니다.
  
1. 사서함에 대 한 모든 클라이언트 액세스를 사용 하지 않도록 설정 하려면 다음 명령을 실행 합니다. 명령 구문 사서함에서 모든 클라이언트 액세스 방법 활성화 되었는지 하는 것으로 가정 합니다.

    ```   
    Set-CASMailbox <username> -EwsEnabled $false -ActiveSyncEnabled $false -MAPIEnabled $false -OWAEnabled $false -ImapEnabled $false -PopEnabled $false
    ```
   
   > [!NOTE]
    > 사서함에 모든 클라이언트 액세스 방법을 사용 하지 않으려면 60 분까지 걸릴 수 있습니다. Note 이러한 액세스 메서드를 사용 하지 않도록 설정에서 로그인 현재 사서함 소유자 분리 하지 않습니다. 소유자 되지 로그인 하는 경우 이러한 액세스 방법을 사용할 수 없는 후 자신의 사서함에 액세스 못할 수 있습니다. 
  
2. 최대 30 일의 삭제 된 항목 보존 기간을 늘리려면 다음 명령을 실행 합니다. 이 현재 설정을 30 일 보다 작은 이라고 가정 합니다. 

    ```
    Set-Mailbox <username> -RetainDeletedItemsFor 30
    ```

3. 단일 항목 복구를 사용 하지 않도록 설정 하려면 다음 명령을 실행 합니다.
    
    ```
    Set-Mailbox <username> -SingleItemRecoveryEnabled $false
    ```

   > [!NOTE]
    > 단일 항목 복구를 사용 하지 않도록 설정 하려면 최대 60 분까지 걸릴 수 있습니다. 이 기간 경과할 때까지 복구 가능한 항목 폴더에서 항목을 삭제 하지 마십시오. 
  
4. 관리 되는 폴더 도우미에서 사서함을 처리 하지 않으려면 다음 명령을 실행 합니다. 앞에서 설명한 것 처럼 경우 비활성화할 수 있습니다는 관리 되는 폴더 도우미만 사서함에 보존 잠금에는 Office 365 보존 정책이 적용 되지 않습니다. 

    ```
    Set-Mailbox <username> -ElcProcessingDisabled $true
    ```

## <a name="step-3-remove-all-holds-from-the-mailbox"></a>3 단계: 사서함에서 모든 보류를 제거 합니다.

복구 가능한 항목 폴더에서 항목을 삭제 하기 전에 마지막 단계는 사서함에 배치 모든 (즉 1 단계에서에서 식별) 보류를 제거 하는 것입니다. 복구 가능한 항목 폴더에서 삭제 한 후 항목을 유지 되지 않을 것 되도록 모든 보류를 제거 해야 합니다. 다음 섹션에서는 다양 한 유형의 사서함에서 보류를 제거 하는 방법에 대 한 정보를 포함 합니다. 사서함에 배치 될 수 있는 형식 보류를 식별 하는 방법에 대 한 팁에 대 한 [자세한 내용](#more-information) 은 섹션을 참조 하십시오. 
  
> [!CAUTION]
> 앞서 설명한 것 처럼 사서함에서 보류를 제거 하기 전에 레코드 관리 또는 법률 부서를 확인 합니다. 
  
 ### <a name="litigation-hold"></a>소송 보존
  
다음 명령을 실행 Exchange Online 사서함에서 소송 보존을 제거 하는 PowerShell 합니다.

```
Set-Mailbox <username> -LitigationHoldEnabled $false
```

   
> [!NOTE]
> 클라이언트 액세스 방법 및 단일 항목 복구를 사용 하지 않도록 설정 하려면와 마찬가지로 걸릴 수 있습니다 소송 보존을 제거 하려면 최대 60 분입니다. 이 기간 경과할 때까지 복구 가능한 항목 폴더에서 항목을 삭제 하지 마십시오. 
  
 ### <a name="in-place-hold"></a>원본 위치 유지
  
다음 명령을 실행 Exchange Online 사서함에 배치 되는 원본 위치 유지를 식별 하는 PowerShell 합니다. 1 단계에서에서 식별 된 원본 위치 유지 하는 GUID를 사용 합니다. 

```
Get-MailboxSearch -InPlaceHoldIdentity <hold GUID> | FL Name
```
   
원본 위치 유지를 확인 한 후 보류에서 사서함을 제거 하려면 Exchange 관리 센터 (EAC) 또는 Exchange Online PowerShell을 사용할 수 있습니다. 자세한 내용은 [만들기 또는 제거 In-place Hold](https://go.microsoft.com/fwlink/?linkid=852668)를 참조 하십시오.
  
 ### <a name="office-365-retention-policies-applied-to-specific-mailboxes"></a>특정 사서함에 적용 하는 office 365 보존 정책
  
다음 명령을 실행 [Office 365 보안 &amp; 준수 센터 PowerShell](https://go.microsoft.com/fwlink/?linkid=627084) 사서함에 적용 되는 Office 365 보존 정책을 식별 합니다. GUID를 사용 하 여 (포함 하지는 `mbx` 또는 `skp` 접두사) 1 단계에서에서 식별 하는 보존 정책에 대 한 합니다. 

```
Get-RetentionCompliancePolicy <retention policy GUID without prefix> | FL Name
```
   
**날짜 관리 방식** 으로 이동 하는 보존 정책, 파악 한 후 \> 보안에서 **보존** 페이지 &amp; 준수 센터 이전 단계에서 식별 하는 보존 정책을 편집 하 고 목록에서 사서함을 제거 합니다. 보존 정책에 포함 된 받는 사람입니다. 
  
 ### <a name="organization-wide-office-365-retention-policies"></a>조직 전체의 Office 365 보존 정책
  
조직에서 모든 사서함에 조직 차원 및 Exchange 전체 Office 365 보존 정책이 적용 됩니다. 이러한 (사서함 수준이 아닌 함) 조직 수준에서 적용 되 고 1 단계에서에서 **Get-organizationconfig** cmdlet을 실행 하는 경우 반환 됩니다. 다음 명령을 실행 [보안 &amp; 준수 센터 PowerShell](https://go.microsoft.com/fwlink/?linkid=627084) 를 조직 전체의 Office 365 보존 정책을 식별 합니다. GUID를 사용 하 여 (포함 하지는 `mbx` 접두사) 1 단계에서에서 식별 하는 조직 전체의 보존 정책에 대 한 합니다. 

```
Get-RetentionCompliancePolicy <retention policy GUID without prefix> | FL Name
```

**날짜 관리 방식** 으로 이동 하는 조직 전체의 Office 365 보존 정책, 파악 한 후 \> 보안에서 **보존** 페이지 &amp; 준수 센터에서 식별 하는 각 조직 전체의 보존 정책 편집은 이전 단계를 실행 하 고 사서함 제외 된 받는 사람 목록에 추가 합니다. 이렇게 하면 사용자의 사서함 보존 정책에서 제거 됩니다. 
  
 ### <a name="ediscovery-case-holds"></a>eDiscovery 사례를 포함 하
  
다음 명령을 실행 [보안 &amp; 준수 센터 PowerShell](https://go.microsoft.com/fwlink/?linkid=627084) 사서함에 적용 되는 eDiscovery 사례와 관련 된 보류를 식별할 수 있습니다. GUID를 사용 하 여 (포함 하지는 `UniH` 접두사) eDiscovery에 대 한 1 단계에서에서 확인 된을 유지 합니다. 두번째 명령은 보류;와 연결 된 eDiscovery 사례의 이름을 표시 하는 note 세번째 명령은 보류의 이름을 표시합니다. 
  
```
$CaseHold = Get-CaseHoldPolicy <hold GUID without prefix>
```

```
Get-ComplianceCase $CaseHold.CaseId | FL Name
```

```
$CaseHold.Name
```

EDiscovery 사례와 보류의 이름을 결정 했다면, 한 후 이동은 **검색 &amp; 조사** \> 보안에서 **eDiscovery** 페이지 &amp; 준수 센터 대/소문자를 열고 보류에서 사서함을 제거 합니다. 자세한 내용은 참조 [Office 365 보안에서 eDiscovery 사례 관리 &amp; 준수 센터](manage-ediscovery-cases.md)합니다.
  
## <a name="step-4-delete-items-in-the-recoverable-items-folder"></a>복구 가능한 항목 폴더에서 항목을 삭제 하는 4 단계:

이제 준비가 실제로 사용 하 여 [검색 사서함](https://go.microsoft.com/fwlink/?linkid=852595) cmdlet은 Exchange Online PowerShell 복구 가능한 항목 폴더에서 항목을 삭제 합니다. **Search-mailbox** cmdlet을 실행 하는 경우 다음과 같은 세가지 옵션이 있습니다. 
  
- 삭제 하기 전에 필요한 경우 항목을 검토할 수 있습니다를 삭제 하기 전에 대상 사서함에 항목을 복사 합니다.
    
- 대상 사서함에 항목을 복사 하 고 같은 명령에서이 삭제 합니다.
    
- 대상 사서함으로 복사 하지 않고 항목을 삭제 합니다. 
    
사용자의 기본 보관 사서함의 복구 가능한 항목 폴더에서 항목을 참고 실행 하는 경우에 삭제 됩니다는 * * 검색 사서함 * * cmdlet입니다. 이 방지 하려면 *DoNotIncludeArchive* 스위치를 포함할 수 있습니다. 앞서 설명한 것 처럼 자동 확장 보관 하는 경우 사용할 수는 사서함에 대해는 * * 검색 사서함 * * cmdlet을 보조 보관 사서함의 항목을 삭제 하지 않습니다. 자동 확장 하는 방법에 대 한 자세한 내용은 보관, [Office 365 무제한 보관의 개요](unlimited-archiving.md)를 참조 하십시오.
  
> [!NOTE]
> ( *SearchQuery* 매개 변수를 사용 하 여) 하 여 검색 쿼리를 포함 하는 경우 **검색 사서함** cmdlet은 검색 결과에 최대 10, 000 항목을 반환 합니다. 따라서 검색 쿼리를 포함 하는 경우에 10, 000 개 이상의 항목을 삭제 하려면 **사서함 검색** 명령을 여러 번 실행 해야할 수 있습니다. 
  
다음 예제에서는 이러한 각 옵션에 대 한 명령 구문을 보여줍니다. 사용 하 여 이러한 예제는 `-SearchQuery size>0` 복구 가능한 항목 폴더의 모든 하위 폴더에서 모든 항목을 삭제 하는 매개 변수 값입니다. 특정 조건에 맞는 항목만 삭제할 해야하는 경우에 날짜 범위 나 메시지의 제목 등의 다른 조건을 지정 하려면 *SearchQuery* 매개 변수를 사용할 수 있습니다. [SearchQuery 매개 변수를 사용 하는 다른 예제](#other-examples-of-using-the-searchquery-parameter) 아래를 참조 하십시오. 
  
### <a name="example-1"></a>예 1

사용자의 복구 가능한 항목 폴더의 모든 항목 조직의 검색 사서함의 폴더에 복사 하는이 예제입니다. 이렇게 하면 영구적으로 삭제 하기 전에 항목을 검토 합니다.

```
Search-Mailbox <username> -SearchQuery size>0 -SearchDumpsterOnly -TargetMailbox "Discovery Search Mailbox" -TargetFolder "<foldername>"
```

이전 예제에서는 사서함 검색에 항목을 복사할 필요가 없습니다. 모든 대상 사서함에 메시지를 복사할 수 있습니다. 그러나 잠재적으로 중요 한 사서함 데이터에 대 한 액세스를 방지 하려면 메시지 권한이 부여 된 직원에 게 제한 된 액세스 권한이 있는 사서함에 복사 하는 것이 좋습니다. 기본적으로 기본 검색 사서함에 대 한 액세스 제한 된 검색 관리 역할 그룹의 구성원에 게 Exchange 온라인 합니다. 
  
### <a name="example-2"></a>예 2

이 예에서는 조직의 검색 사서함의 폴더를 사용자의 복구 가능한 항목 폴더의 모든 항목을 복사 하 고 사용자의 복구 가능한 항목 폴더에서 항목을 삭제 합니다.

```
Search-Mailbox <username> -SearchQuery size>0 -SearchDumpsterOnly -TargetMailbox "Discovery Search Mailbox" -TargetFolder "<foldername>" -DeleteContent
```
 
### <a name="example-3"></a>예 3

대상 사서함으로 복사 하지 않고 사용자의 복구 가능한 항목 폴더의 모든 항목을 삭제 하는이 예제입니다. 

```
Search-Mailbox <username> -SearchQuery size>0 -SearchDumpsterOnly -DeleteContent
```

### <a name="other-examples-of-using-the-searchquery-parameter"></a>SearchQuery 매개 변수를 사용 하는 다른 예제

*SearchQuery* 매개 변수를 사용 하 여 특정 메시지를 찾으려면의 몇가지 예는 다음과 같습니다. 특정 항목을 검색 하려면 *SearchQuery* 매개 변수를 사용 하는 경우에 검색 결과 검토 하 고 다음 쿼리 수정 필요한 경우 검색 결과 삭제 하기 전에 수 있도록 대상 사서함에 검색 결과 복사 하는 것이 좋습니다. 
  
제목 필드에서 특정 구를 포함 하는 메시지를 반환 하는이 예제입니다.
  
```
SearchQuery 'subject:"MAIL_BOX VALIDATION/UPGRADE!!!"' 
```

이 예제에서는 지정된 된 날짜 범위 내에서 보낸 메시지를 반환 합니다.
  
```
SearchQuery 'sent>=06/01/2016 AND sent<=09/01/2016'
```
 
이 예제에서는 지정 된 사람에 게 보낸 메시지를 반환 합니다.

```
SearchQuery 'to:garthf@alpinehouse.com'
```
   
### <a name="verify-that-items-were-deleted"></a>항목이 삭제 되 고 있는지 확인 합니다.

사서함의 복구 가능한 항목 폴더에서 항목을 성공적으로 삭제 했는지를 확인 하려면 cmdlet을 사용 **Get-mailboxfolderstatistics** Exchange 온라인 PowerShell 크기와 복구 가능한 항목 폴더의 항목 수를 확인 합니다. 1 단계에서에서 수집 된 내용으로 이러한 통계를 비교할 수 있습니다. 
  
폴더와 사용자의 기본 사서함의 복구 가능한 항목 폴더에 하위 폴더에서 항목의 총 수와 현재 크기를 가져오려면 다음 명령을 실행 합니다. 
  
```
Get-MailboxFolderStatistics <username> -FolderScope RecoverableItems | FL Name,FolderAndSubfolderSize,ItemsInFolderAndSubfolders
```
   
폴더 및 사용자의 보관 사서함의 복구 가능한 항목 폴더에 하위 폴더의 크기와 총 항목 수를 가져오려면 다음 명령을 실행 합니다. 

```
Get-MailboxFolderStatistics <username> -FolderScope RecoverableItems -Archive | FL Name,FolderAndSubfolderSize,ItemsInFolderAndSubfolders
```
  
## <a name="step-5-revert-the-mailbox-to-its-previous-state"></a>5 단계: 사서함을 이전 상태로 되돌리기

마지막 단계를 이전 구성으로 다시 사서함으로 돌아가려면입니다. 즉, 2 단계에서에서 변경 되는 속성을 다시 설정 하 고 3 단계에서에서 제거 된 보류를 다시 적용 합니다. 이는 다음이 포함 됩니다.
  
- 이전 값으로 다시 삭제 된 항목 보존 기간을 변경 합니다. 또는 남겨둘 수 있습니다 Exchange에서 30 일, 최대 값으로 설정이 온라인 합니다.
    
- 단일 항목 복구를 다시 사용 하도록 설정 합니다.
    
- 다시 소유자가 사서함에 액세스할 수 있도록 클라이언트 액세스 방법을 사용 하도록 설정 합니다.
    
- 보류 및 제거 하는 Office 365 보존 정책을 다시 적용 합니다.
    
- 다시 사용 하도록 설정의 관리 되는 폴더 도우미가 사서함 처리할 수 있습니다.
    
> [!IMPORTANT]
> 다시 보류 또는 Office 365를 적용 한 후 24 시간은 때까지 대기 하는 것이 좋습니다 보존 정책 (및 원본 위치에 있는지 확인 (영문))는 관리 되는 폴더 도우미는 사서함을 처리를 다시 활성화 하기 전에 합니다. 
  
Exchange Online PowerShell에서 (지정된 된 시퀀스)에서 다음 단계를 수행 합니다.
  
1. 원래 값 삭제 된 항목 보존 기간을 변경 하려면 다음 명령을 다시 실행 합니다. 이전 설정이 30 일 보다 작은; 것이 가정 예: 14 일입니다. 
    
    ```
    Set-Mailbox <username> -RetainDeletedItemsFor 14
    ```
   
2. 단일 항목 복구를 다시 사용 하도록 설정 하려면 다음 명령을 실행 합니다.
   
    ```
    Set-Mailbox <username> -SingleItemRecoveryEnabled $true
    ```

3. 다시 사서함에 모든 클라이언트 액세스 메서드를 사용 하도록 설정 하려면 다음 명령을 실행 합니다.
    
    ```
    Set-CASMailbox <username> -EwsEnabled $true -ActiveSyncEnabled $true -MAPIEnabled $true -OWAEnabled $true -ImapEnabled $true -PopEnabled $true
    ```
   
4. 3 단계에서에서 제거 된 보류를 다시 적용 합니다. 보류의 유형에 따라 다음 절차 중 하나를 사용 합니다.
    
    **소송 보존**
    
    사서함에 대 한 소송 보존을 다시 사용 하도록 설정 하려면 다음 명령을 실행 합니다.
    
    ```
    Set-Mailbox <username> -LitigationHoldEnabled $true
    ```

    **원본 위치 유지**
    
    사서함에 다시 추가 원본 위치 유지를 EAC (또는 Exchange Online PowerShell)를 사용 합니다. 
    
    **특정 사서함에 적용 하는 office 365 보존 정책**
    
    보안을 사용 하 여 &amp; 준수 센터 사서함 Office 365 보존 정책에 다시 추가 합니다. **날짜 관리 방식** 으로 이동 \> 보안에서 **보존** 페이지 &amp; 준수 센터 보존 정책을 편집 하 고 사서함 보존 정책에 적용 되는 받는 사람 목록에 다시 추가 합니다. 
    
    **조직 전체의 Office 365 보존 정책**
    
    정책에서 제외 하 여 한 조직 수준의 또는 Exchange 전체 보존 정책을 제거 하는 경우 다음 사용 하 여 보안 &amp; 준수 센터의 목록에서 사서함을 제거 하려면 사용자를 제외 합니다. **날짜 관리 방식** 으로 이동 \> 보안에서 **보존** 페이지 &amp; 준수 센터 조직 전체의 보존 정책을 편집 하 고 제외 된 받는 사람 목록에서 사서함을 제거 합니다. 이 수행 하는 사용자의 사서함에 보존 정책을 다시 적용 됩니다. 
    
    **eDiscovery 사례를 포함 하**
    
    보안을 사용 하 여 &amp; 사서함을 추가 하려면 준수 센터 eDiscovery 사례와 관련 된 보류를 백업 합니다. 이동 하는 **검색 &amp; 조사** \> 보안에서 **eDiscovery** 페이지 &amp; 준수 센터 대/소문자를 열고 사서함 보류에 다시 추가 합니다. 
    
5. 관리 되는 폴더 도우미는 사서함을 다시 처리할 수 있도록 하려면 다음 명령을 실행 합니다. 듯이 다시 보류 또는 Office 365를 적용 한 후 24 시간은 때까지 대기 하는 것이 좋습니다 보존 정책 (및 원본 위치에 있는지 확인 (영문)) 관리 되는 폴더 도우미를 다시 활성화 하기 전에 합니다. 

    ```
    Set-Mailbox <username> -ElcProcessingDisabled $false
    ```
   
6. 사서함을 이전 구성으로 다시 되돌렸습니다 있는지를 확인 하려면 다음 명령을 실행 수 있으며 다음 설정의 1 단계에서에서 수집 하는 것과 비교할 수 있습니다.

    ```
    Get-Mailbox <username> | FL ElcProcessingDisabled,InPlaceHolds,LitigationHoldEnabled,RetainDeletedItemsFor,SingleItemRecoveryEnabled
    ```

    ```
    Get-CASMailbox <username> | FL EwsEnabled,ActiveSyncEnabled,MAPIEnabled,OWAEnabled,ImapEnabled,PopEnabled
    ```
  
## <a name="more-information"></a>추가 정보

다음은 다양 한 유형의 **Get-mailbox** 또는 **Get-organizationconfig** cmdlet을 실행 하는 경우 *InPlaceHolds* 속성의 값에 따라 보류를 식별 하는 방법에 설명 하는 테이블입니다. 앞부분에 설명 하 고, 모든 보류를 제거 하려면 있고 하기 전에 사서함에서 Office 365 보존 정책이 성공적으로 복구 가능한 항목 폴더에서 항목을 삭제할 수 있습니다. 
  
|**종류를 유지 합니다.**|**예제 값**|**보류를 식별 하는 방법**|
|:-----|:-----|:-----|
|소송 보존  <br/> | `True` <br/> |*LitigationHoldEnabled* 속성이로 설정 된 `True`합니다.  <br/> |
|원본 위치 유지  <br/> | `c0ba3ce811b6432a8751430937152491` <br/> |*InPlaceHolds* 속성의 사서함에 배치 되는 원본 위치 유지의 GUID를 포함 합니다. 이 In-place Hold GUID를 접두사로 시작 되지 않으면 때문에 알 수 있습니다.<br/> 사용할 수는 ' Get-mailboxsearch InPlaceHoldIdentity<hold GUID> | FL' 사서함에서 원본 위치 유지 하는 방법에 대 한 정보를 얻을 수 있는 Exchange Online PowerShell에서 명령 합니다.  <br/> |
| 보안에서 office 365 보존 정책을 &amp; 준수 센터 특정 사서함에 적용  <br/> | `mbxcdbbb86ce60342489bff371876e7f224` <br/> 또는  <br/>  `skp127d7cf1076947929bf136b7a2a8c36f` <br/> |**Get-mailbox** cmdlet을 실행 하는 경우 *InPlaceHolds* 속성은 사서함에 적용 된 Office 365의 guid가 보존 정책도 포함 합니다. 으로 시작 하는 GUID 때문에 보존 정책을 식별할 수는 `mbx` 접두사입니다. 보존 정책의 GUID로 시작 하는 경우는 `skp` 비즈니스 대화에 대 한 보존 정책을 Skype에 적용 되는지 나타내는 접두사입니다.<br/> 사서함에 적용 되는 Office 365 identity 보존 정책, 보안에서 다음 명령을 실행 &amp; 준수 센터 PowerShell: <br/> <br/>' Get RetentionCompliancePolicy<retention policy GUID without prefix> | FL 이름`<br/><br/>Be sure to remove the  `mbx` or  `skp'이 명령을 실행 하면 접두사입니다.  <br/> |
|보안에서 조직 전체의 Office 365 보존 정책 &amp; 준수 센터  <br/> |값 없음  <br/> 또는  <br/>  `-mbxe9b52bf7ab3b46a286308ecb29624696`(사서함은 조직 수준의 정책에서 제외를 나타냄)  <br/> |*InPlaceHolds* 속성이 비어 있는 **Get-mailbox** cmdlet을 실행 하는 경우, 하는 경우에 여전히 있을 수 있습니다 하나 이상의 조직 전체의 Office 365 보존 정책 사서함에 적용 합니다.  <br/> 이 확인 하려면 실행할 수 있습니다는 ' Get-organizationconfig | FL InPlaceHolds` command in Exchange Online PowerShell to get a list of the GUIDs for organization-wide Office 365 retention policies. The GUID for organization-wide retention policies applied to Exchange mailboxes start with the  `mbx` prefix; for example  `mbxa3056bb15562480fadb46ce523ff7b02`.  <br/> To identity the organization-wide Office 365 retention policy that's applied to the mailbox, run the following command in Security &amp; Compliance Center PowerShell: <br/><br/> `Get RetentionCompliancePolicy<retention policy GUID without prefix> | FL 이름`<br/><br/>Note that if a mailbox is excluded from an organization-wide Office 365 retention policy, the GUID for the retention policy is displayed in the  *InPlaceHolds*  property of the user's mailbox when you run the **Get-Mailbox** cmdlet; it's identified by the prefix  `-mbx`; for example,  `-mbxe9b52bf7ab3b46a286308ecb29624696' <br/> |
|eDiscovery 사례 유지 (영문) 보안 &amp; 준수 센터  <br/> | `UniH7d895d48-7e23-4a8d-8346-533c3beac15d` <br/> |*InPlaceHolds* 속성은 또한 보안에서 eDiscovery 사례와 관련 된 모든 보류의 GUID가 포함 &amp; 준수 센터의 사서함에 배치 될 수입니다. 이런 현상이 발생 eDiscovery 사례 보류도 시작 하는 GUID를 알 수는 `UniH` 접두사입니다.<br/> 사용할 수 있습니다는 `Get-CaseHoldPolicy` 보안에서 cmdlet &amp; 준수 센터 PowerShell 보류의 사서함에 연결 된 eDiscovery 사례에 대 한 정보를 얻을 수 있습니다. 명령을 실행할 수 등 ' Get CaseHoldPolicy<hold GUID without prefix> | FL 이름` to display the name of the case hold that's on the mailbox. Be sure to remove the  `UniH` prefix when you run this command.  <br/><br/> To identity the eDiscovery case that the hold on the mailbox is associated with, run the following commands:<br/><br/>`$CaseHold Get CaseHoldPolicy = <hold GUID without prefix> `<br/><br/>`Get ComplianceCase $CaseHold.CaseId | FL 이름 '


