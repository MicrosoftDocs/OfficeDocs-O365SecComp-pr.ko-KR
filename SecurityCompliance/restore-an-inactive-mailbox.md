---
title: Office 365에서 비활성 사서함 복원
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 8/28/2017
audience: Admin
ms.topic: article
ms.service: O365-seccomp
ms.collection: M365-security-compliance
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: 97e06a7a-ef9a-4ce8-baea-18b9e20449a3
description: 새 직원 또는 다른 사용자가 Office 365에서 비활성 사서함의 콘텐츠에 액세스 해야 하는 경우 비활성 사서함의 내용을 기존 사서함으로 복원 하거나 병합할 수 있습니다.
ms.openlocfilehash: 6bd147296e4324c5f75ff808768f8899cf9b59fd
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/17/2019
ms.locfileid: "34157310"
---
# <a name="restore-an-inactive-mailbox-in-office-365"></a>Office 365에서 비활성 사서함 복원

일시 삭제 된 사서함 유형의 비활성 사서함은 조직 내에서 이전 직원의 전자 메일을 유지 하는 데 사용 됩니다. 다른 직원이 이거나 퇴직 한 직원의 작업을 수행 하거나 해당 직원이 조직에 게 제공 되는 경우, 비활성 사서함의 내용을 사용자가 사용할 수 있도록 하는 방법에는 두 가지가 있습니다. 
  
- **비활성 사서함 복원** 다른 직원이 이거나 퇴직 한 직원의 작업 책임을 취하고 있거나, 다른 사용자가 비활성 사서함의 콘텐츠에 액세스 해야 하는 경우 비활성 사서함의 내용을 기존 사서함으로 복원 하거나 병합할 수 있습니다. 비활성 사서함에서 보관 함을 복원할 수도 있습니다. 복원 후 비활성 사서함은 보존 되며 비활성 사서함으로 보존 됩니다. 이 항목에서는 비활성 사서함을 복원 하는 절차에 대해 설명 합니다. 
    
- **비활성 사서함 복구** 이거나 퇴직 한 직원이 조직으로 반환 되거나, 새 직원이 이거나 퇴직 한 직원의 직무를 담당 하는 경우 비활성 사서함의 내용을 복구할 수 있습니다. 이 메서드는 비활성 사서함을 비활성 사서함의 내용이 포함 된 새 사서함으로 변환 합니다. 복구한 후 비활성 사서함 존재 하지 않습니다. 단계별 절차에 대 한 자세한 내용은 [Office 365에서 비활성 사서함 복구](recover-an-inactive-mailbox.md)를 참조 하십시오.
    
비활성 사서함 복원 및 복구 간의 차이점에 대 한 자세한 내용은이 문서의 **추가 정보** 섹션을 참조 하십시오. 
  
## <a name="before-you-begin"></a>시작하기 전에

- 비활성 사서함을 복원 하려면 Exchange Online PowerShell을 사용 해야 합니다. EAC(Exchange 관리 센터)는 사용할 수 없습니다. 단계별 지침은 [Exchange Online PowerShell에 연결을](https://go.microsoft.com/fwlink/?linkid=396554)참조 하십시오.
    
- Exchange Online PowerShell에서 다음 명령을 실행 하 여 조직의 비활성 사서함에 대 한 id 정보를 가져옵니다. 
    
    ```
    Get-Mailbox -InactiveMailboxOnly | FL Name,DistinguishedName,ExchangeGuid,PrimarySmtpAddress
    ```

     이 명령에서 반환 하는 정보를 사용 하 여 특정 비활성 사서함을 복원 합니다.
    
- 비활성 사서함에 대 한 자세한 내용은 [Office 365의 비활성 사서함](inactive-mailboxes-in-office-365.md)을 참조 하십시오.
    
## <a name="restore-an-inactive-mailbox"></a>비활성 사서함 복원

**Get-mailboxrestorerequest** Cmdlet을 _sourcemailbox_ 및 _targetmailbox_ 매개 변수와 함께 사용 하 여 비활성 사서함의 내용을 기존 사서함으로 복원할 수 있습니다. 이 cmdlet을 사용 하는 방법에 대 한 자세한 내용은 [get-mailboxrestorerequest](https://go.microsoft.com/fwlink/?linkid=856298)를 참조 하십시오.
  
1. 비활성 사서함의 속성을 포함 하는 변수를 만듭니다. 
    
    ```
    $InactiveMailbox = Get-Mailbox -InactiveMailboxOnly -Identity <identity of inactive mailbox>
    ```

    > [!IMPORTANT]
    > 이전 명령에서 **DistinguishedName** 또는 **ExchangeGUID** 속성 값을 사용 하 여 비활성 사서함을 식별 합니다. 이러한 속성은 조직의 각 사서함에 대해 고유 하지만 활성 및 비활성 사서함의 기본 SMTP 주소가 같을 수 있습니다. 
  
2. 비활성 사서함의 내용을 기존 사서함으로 복원 합니다. 비활성 사서함의 콘텐츠 (원본 사서함)가 기존 사서함의 해당 폴더 (대상 사서함)에 병합 됩니다.
    
    ```
    New-MailboxRestoreRequest -SourceMailbox $InactiveMailbox.DistinguishedName -TargetMailbox newemployee@contoso.com -AllowLegacyDNMismatch
    ```
   
   또는 비활성 사서함의 콘텐츠를 복원할 최상위 폴더를 대상 사서함에서 지정할 수 있습니다. 지정 된 대상 폴더 또는 대상 폴더 구조가 대상 사서함에 없는 경우 복원 프로세스 중에 만들어집니다. 
    
    이 예에서는 비활성 사서함의 사서함 항목 및 하위 폴더를 대상 사서함의 최상위 폴더 구조에 있는 "비활성 사서함" 이라는 폴더로 복사 합니다.
    
   ```
   New-MailboxRestoreRequest -SourceMailbox $InactiveMailbox.DistinguishedName -TargetMailbox newemployee@contoso.com -TargetRootFolder "Inactive Mailbox" -AllowLegacyDNMismatch
   ```
  
## <a name="restore-the-archive-from-an-inactive-mailbox"></a>비활성 사서함에서 보관 파일 복원

비활성 사서함에 보관 사서함이 있는 경우 기존 사서함의 보관 사서함으로 복원할 수도 있습니다. 비활성 사서함에서 보관 함을 복원 하려면 비활성 사서함을 복원 하는 데 사용 되는 명령에 _Sourceisarchive_ 및 _TargetIsAchive_ 스위치를 추가 해야 합니다. 
  
1. 비활성 사서함의 속성을 포함 하는 변수를 만듭니다. 
    
    ```
    $InactiveMailbox = Get-Mailbox -InactiveMailboxOnly -Identity <identity of inactive mailbox>
    ```

    > [!IMPORTANT]
    > 이전 명령에서 **DistinguishedName** 또는 **ExchangeGUID** 속성 값을 사용 하 여 비활성 사서함을 식별 합니다. 이러한 속성은 조직의 각 사서함에 대해 고유 하지만 활성 및 비활성 사서함의 기본 SMTP 주소가 같을 수 있습니다. 
  
2. 비활성 사서함 (원본 보관 함)의 보관 함 콘텐츠를 기존 사서함 (대상 보관 파일)의 보관 함으로 복원 합니다. 이 예에서는 원본 보관 함의 콘텐츠가 대상 사서함의 보관 함에 있는 "비활성 사서함 보관" 폴더에 복사 됩니다.

    ```
    New-MailboxRestoreRequest -SourceMailbox $InactiveMailbox.DistinguishedName -SourceIsArchive -TargetMailbox newemployee@contoso.com -TargetIsArchive -TargetRootFolder "Inactive Mailbox Archive" -AllowLegacyDNMismatch
    ```

  
## <a name="more-information"></a>추가 정보

- **비활성 사서함을 복구 하 고 복원 하는 경우의 주요 차이점은 무엇 인가요?** 비활성 사서함을 복구 하면 기본적으로 사서함이 새 사서함으로 변환 되며 비활성 사서함의 콘텐츠 및 폴더 구조가 보존 되 고 사서함이 새 사용자 계정에 연결 됩니다. 복구를 복구한 후에는 비활성 사서함이 더 이상 존재 하지 않으며, 새 사서함의 콘텐츠에 대 한 변경 내용은 원래 비활성 사서함에서 유지 되었던 콘텐츠에 영향을 줍니다. 반대로 비활성 사서함을 복원 하는 경우에는 콘텐츠가 다른 사서함으로 복사 되기만 합니다. 비활성 사서함은 유지 되 고 비활성 사서함은 유지 됩니다. 대상 사서함의 콘텐츠가 변경 되어도 비활성 사서함에 저장 된 원래 콘텐츠에는 영향을 주지 않습니다. 보안 & 준수 센터의 [콘텐츠 검색 도구](run-a-content-search-in-the-security-and-compliance-center.md) 를 사용 하 여 비활성 사서함을 계속 검색할 수 있으며, 해당 콘텐츠를 다른 사서함으로 복원 하거나 나중에 복구 하거나 삭제할 수 있습니다. 
    
- **비활성 사서함은 어떻게 찾을 수 있나요?** 조직의 비활성 사서함 목록을 가져오고 비활성 사서함을 복원 하는 데 유용한 정보를 표시 하려면이 명령을 실행 하면 됩니다. 

  ```
  Get-Mailbox -InactiveMailboxOnly | FL Name,PrimarySMTPAddress,DistinguishedName,ExchangeGUID,LegacyExchangeDN,ArchiveStatus
  ```

- **소송 보존 또는 Office 365 보존 정책을 사용 하 여 비활성 사서함 콘텐츠를 유지 합니다.** 비활성 사서함을 복원한 후 상태를 유지 하려면 비활성 사서함을 복원 하기 전에 대상 사서함을 [소송](https://go.microsoft.com/fwlink/?linkid=856286) 보존으로 설정 하거나 [Office 365 보관 정책을](retention-policies.md) 적용할 수 있습니다. 이렇게 하면 대상 사서함으로 복원 된 후 비활성 사서함의 항목이 영구적으로 삭제 되는 것을 방지할 수 있습니다. 
    
- **비활성 사서함을 복원 하기 전에 대상 사서함에 대해 보존을 사용 하도록 설정 합니다.** 비활성 사서함의 사서함 항목은 오래 되었을 수 있으므로 비활성 사서함을 복원 하기 전에 대상 사서함에 대해 보존을 사용 하도록 설정할 수 있습니다. 사서함을 보존 상태로 전환할 때 할당 된 보존 정책은 보존 상태가 제거 될 때까지 또는 보존 기간이 만료 될 때까지 처리 되지 않습니다. 이렇게 하면 대상 사서함 시간 소유자가 비활성 사서함에서 오래 된 메시지를 관리할 수 있습니다. 그렇지 않으면 보존 정책이 대상 사서함에 대해 구성 된 보존 설정에 따라 오래 된 항목을 삭제 하거나 (사용 하도록 설정 된 경우 보관 사서함으로 항목을 이동) 할 수 있습니다. 자세한 내용은 [Exchange Online에서 사서함을 보존 상태로 유지](https://go.microsoft.com/fwlink/?linkid=856300)를 참조 하세요.
    
- **AllowLegacyDNMismatch 스위치는 어떤 작업을 수행 하나요?** 이전 예제에서 비활성 사서함을 복원 하는 경우 **AllowLegacyDNMismatch** 스위치를 사용 하 여 비활성 사서함을 다른 대상 사서함으로 복원할 수 있습니다. 일반적인 복원 시나리오에서는 원본 및 대상 사서함이 같은 사서함 인 콘텐츠를 복원 하는 것이 목표입니다. 따라서 기본적으로 **get-mailboxrestorerequest** cmdlet은 원본 및 대상 사서함에서 **LegacyExchangeDN** 속성 값이 동일한 지 확인 합니다. 따라서 실수로 원본 사서함을 잘못 된 대상 사서함으로 복원 하는 것을 방지할 수 있습니다. **AllowLegacyDNMismatch** 스위치를 사용 하지 않고 비활성 사서함을 복원 하려고 하면 원본 및 대상 사서함의 **LegacyExchangeDN** 속성 값이 서로 다른 경우 명령이 실패할 수 있습니다. 
    
- **Get-mailboxrestorerequest cmdlet의 다른 매개 변수를 사용 하 여 비활성 사서함에 대해 서로 다른 복원 시나리오를 구현할 수 있습니다.** 예를 들어이 명령을 실행 하 여 비활성 사서함의 보관 함을 대상 사서함의 기본 사서함으로 복원할 수 있습니다. 
    
  ```
  New-MailboxRestoreRequest -SourceMailbox <inactive mailbox> -SourceIsArchive -TargetMailbox <target mailbox> -TargetRootFolder "Inactive Mailbox Archive" -AllowLegacyDNMismatch
  ```

  또한이 명령을 실행 하 여 비활성 기본 사서함을 대상 사서함의 보관 함으로 복원할 수 있습니다.

  ```
  New-MailboxRestoreRequest -SourceMailbox <inactive mailbox> -TargetMailbox <target mailbox> -TargetIsArchive -TargetRootFolder "Inactive Mailbox" -AllowLegacyDNMismatch
  ```

- **TargetRootFolder 매개 변수는 어떤 역할을 합니까?** 앞에서 설명한 것 처럼 **Targetrootfolder** 매개 변수를 사용 하 여 비활성 사서함의 콘텐츠를 복원할 대상 사서함에서 폴더 구조 (루트 라고도 함)의 맨 위에 폴더를 지정할 수 있습니다. 이 매개 변수를 사용 하지 않으면 비활성 사서함의 사서함 항목이 대상 사서함의 해당 하는 기본 폴더에 병합 되 고 사용자 지정 폴더가 대상 사서함의 루트에 다시 만들어집니다. 다음 그림에서는 **Targetrootfolder** 매개 변수를 사용 하는 것과 사용할 때의 차이점을 강조 표시 합니다. 
    
    **TargetRootFolder 매개 변수가 사용 되지 않는 경우 대상 사서함의 폴더 계층 구조**
    
    ![TargetRootFolder 매개 변수가 사용되지 않는 경우의 스크린샷](media/76a759af-f483-4d1c-8cc7-243435b5562e.png)
  
    **TargetRootFolder 매개 변수를 사용 하는 경우 대상 사서함의 폴더 계층 구조**
    
    ![TargetRootFolder 매개 변수가 사용된 경우의 스크린샷](media/300da592-7323-48db-b8a4-07012259d113.png)

  

