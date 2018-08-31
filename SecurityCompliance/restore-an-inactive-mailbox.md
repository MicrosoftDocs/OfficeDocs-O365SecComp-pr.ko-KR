---
title: Office 365에서 비활성 사서함 복원
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 8/28/2017
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: 97e06a7a-ef9a-4ce8-baea-18b9e20449a3
description: 새 직원 또는 다른 사용자가 Office 365에서 비활성 사서함의 내용에 대 한 액세스를 필요한 경우 있습니다 수 복원 (또는 병합) 기존 사서함을 비활성 사서함의 내용을 합니다.
ms.openlocfilehash: e0add2b63a48edc27795143324c83153b15dcf8c
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22532973"
---
# <a name="restore-an-inactive-mailbox-in-office-365"></a>Office 365에서 비활성 사서함 복원

비활성 사서함 (즉, 일시 삭제 된 사서함의 형식)가 자신이 조직을 떠난 후 이전 직원의 전자 메일을 유지 하는 데 사용 됩니다. 이전된 직원의 직무에 가져와 다른 직원 또는 해당 직원이 조직에 반환 하는 경우에 경우 사용할 수 있는 비활성 사서함의 내용을 사용자에 게 두 가지가 있습니다. 
  
- **비활성 사서함 복원** 이전된 직원의 직무에 가져와 다른 직원 또는 비활성 사서함의 내용에 대 한 액세스를 필요로 하는 다른 사용자 있습니다 수 복원 (또는 병합) 기존 사서함을 비활성 사서함의 내용입니다. 비활성 사서함에서 보관 사서함에 복원할 수도 있습니다. 복원 된 후에 비활성 사서함 보존 되 고 비활성 사서함으로 유지 됩니다. 이 항목에서는 비활성 사서함을 복원 하기 위한 절차에 설명 합니다. 
    
- **비활성 사서함 복구** 이전된 직원 조직에 반환 하는 경우 또는 이전된 직원의 직무에 적용할 새 직원 고용 하는 경우에 비활성 사서함의 콘텐츠를 복구할 수 있습니다. 이 메서드는 비활성 사서함의 내용이 포함 된 새 사서함을 비활성 사서함으로 변환 합니다. 복구한 후 비활성 사서함 존재 하지 않습니다. 단계별 절차에 대 한 [Office 365에서 비활성 사서함 복구](recover-an-inactive-mailbox.md)를 참조 합니다.
    
비활성 사서함을 복구 하 고 복원 간의 차이점에 대 한 자세한 내용은이 문서에서 **자세한 정보** 섹션을 참조 하십시오. 
  
## <a name="before-you-begin"></a>시작하기 전에

- 비활성 사서함을 복원 하려면 Exchange Online PowerShell을 사용 해야 합니다. Exchange 관리 센터 (EAC)를 사용할 수 없습니다. 단계별 지침은 [Connect to Exchange Online PowerShell를](https://go.microsoft.com/fwlink/?linkid=396554)참조 하십시오.
    
- 다음 명령을 실행 Exchange Online 조직에서 비활성 사서함에 대 한 id 정보를 가져올 PowerShell 합니다. 
    
    ```
    Get-Mailbox -InactiveMailboxOnly | FL Name,DistinguishedName,ExchangeGuid,PrimarySmtpAddress
    ```

     이 명령에서 반환 되는 정보를 사용 하 여 특정 비활성 사서함을 복원 합니다.
    
- 비활성 사서함에 대 한 자세한 내용은 [Office 365에서 비활성 사서함](inactive-mailboxes-in-office-365.md)을 참조 하십시오.
    
## <a name="restore-an-inactive-mailbox"></a>비활성 사서함 복원

_SourceMailbox_ 및 _TargetMailbox_ 매개 변수와 함께 **New-mailboxrestorerequest** cmdlet을 사용 하 여 기존 사서함을 비활성 사서함의 콘텐츠를 복원 합니다. 이 cmdlet을 사용 하는 방법에 대 한 자세한 내용은 [New-mailboxrestorerequest](https://go.microsoft.com/fwlink/?linkid=856298)을 참조 하십시오.
  
1. 비활성 사서함의 속성을 포함 하는 변수를 만듭니다. 
    
    ```
    $InactiveMailbox = Get-Mailbox -InactiveMailboxOnly -Identity <identity of inactive mailbox>
    ```

    > [!IMPORTANT]
    > 이전 명령에서 비활성 사서함을 식별할 **DistinguishedName** 또는 **ExchangeGUID** 속성 값을 사용 합니다. 이러한 속성은 활성 및 비활성 사서함을 들 수 동일한 기본 SMTP 주소 수도 있지만 조직 전체에서 각 사서함에 대 한 고유 합니다. 
  
2. 기존 사서함을 비활성 사서함의 콘텐츠를 복원 합니다. 비활성 사서함 (원본 사서함)의 내용은 기존 사서함 (대상 사서함)에서 해당 폴더에 병합 됩니다.
    
    ```
    New-MailboxRestoreRequest -SourceMailbox $InactiveMailbox.DistinguishedName -TargetMailbox newemployee@contoso.com -AllowLegacyDNMismatch
    ```
   
   또는 비활성 사서함에서 내용을 복원 하는 대상 사서함에서 최상위 폴더를 지정할 수 있습니다. 지정 된 대상 폴더 또는 대상 폴더 구조 존재 하지 않으면 대상 사서함에 복원 하는 동안 만들어집니다. 
    
    대상 사서함의 최상위 폴더 구조에서 사서함 항목 및 비활성 사서함에서 "비활성 사서함" 라는 폴더에 하위 폴더를 복사 하는이 예제입니다.
    
   ```
   New-MailboxRestoreRequest -SourceMailbox $InactiveMailbox.DistinguishedName -TargetMailbox newemployee@contoso.com -TargetRootFolder "Inactive Mailbox" -AllowLegacyDNMismatch
   ```
  
## <a name="restore-the-archive-from-an-inactive-mailbox"></a>비활성 사서함에서 보관 사서함 복원

비활성 사서함 보관 사서함이 있는 경우 기존 사서함의 보관 사서함에 복원할 수도 있습니다. 비활성 사서함에서 보관 사서함을 복원 하려면 비활성 사서함을 복원 하는 데 사용 하는 명령에 _SourceIsArchive_ 및 _TargetIsAchive_ 스위치를 추가 해야 합니다. 
  
1. 비활성 사서함의 속성을 포함 하는 변수를 만듭니다. 
    
    ```
    $InactiveMailbox = Get-Mailbox -InactiveMailboxOnly -Identity <identity of inactive mailbox>
    ```

    > [!IMPORTANT]
    > 이전 명령에서 비활성 사서함을 식별할 **DistinguishedName** 또는 **ExchangeGUID** 속성 값을 사용 합니다. 이러한 속성은 활성 및 비활성 사서함을 들 수 동일한 기본 SMTP 주소 수도 있지만 조직 전체에서 각 사서함에 대 한 고유 합니다. 
  
2. 비활성 사서함 (원본 보관)에서 기존 사서함 (대상 보관)의 보관 사서함으로 보관 사서함의 내용을 복원 합니다. 이 예제에서는 원본 보관 함의 내용이 대상 사서함의 보관 사서함에 "비활성 사서함 보관" 라는 폴더에 복사 됩니다.

    ```
    New-MailboxRestoreRequest -SourceMailbox $InactiveMailbox.DistinguishedName -SourceIsArchive -TargetMailbox newemployee@contoso.com -TargetIsArchive -TargetRootFolder "Inactive Mailbox Archive" -AllowLegacyDNMismatch
    ```

  
## <a name="more-information"></a>추가 정보

- **비활성 사서함 복원 및 복구 간의 주요 차이점은 무엇입니까?** 비활성 사서함을 복구 하는 경우 사서함은 기본적으로 새 사서함으로 변환 됩니다 내용과 비활성 사서함의 폴더 구조 유지 되므로 및 사서함을 새 사용자 계정에 연결 됩니다. 복구 되 비활성 사서함 더이상 존재 하 고 새 사서함의 콘텐츠를 변경한 내용을에 원래 있던 콘텐츠에 영향을 주는 후 비활성 사서함에서 대기 합니다. 이와 반대로 비활성 사서함을 복원 하는 경우 내용은 단순히 다른 사서함에 복사 됩니다. 비활성 사서함 보존 되 고 비활성 사서함 유지 됩니다. 대상 사서함의 콘텐츠를 변경한 내용을 비활성 사서함에 보관 원본 콘텐츠에 적용 되지 않습니다. 비활성 사서함 여전히 검색 가능한 Office 365 보안에서 [콘텐츠 검색 도구](run-a-content-search-in-the-security-and-compliance-center.md) 를 사용 하 여 &amp; 준수 센터의 내용을 다른 사서함으로 복원할 수 또는 복구 되거나 나중에 삭제 될 수 있습니다. 
    
- **는 어떻게 찾나요 비활성 사서함?** 조직에서 비활성 사서함 목록을 가져오고 비활성 사서함 복원에 대 한 유용한 정보를 표시,이 명령을 실행할 수 있습니다. 

  ```
  Get-Mailbox -InactiveMailboxOnly | FL Name,PrimarySMTPAddress,DistinguishedName,ExchangeGUID,LegacyExchangeDN,ArchiveStatus
  ```

- **비활성 사서함 콘텐츠를 유지 하려면 소송 보존으로 설정 또는 Office 365 보존 정책을 사용 하 여.** 복원 된 후 비활성 사서함의 상태를 유지 하려는 경우에 [소송 보존](https://go.microsoft.com/fwlink/?linkid=856286) 에 배치 하는 대상 사서함 수도 있고 비활성 사서함을 복원 하기 전에는 [Office 365 보존 정책](retention-policies.md) 을 적용할 수 있습니다. 이렇게 하면 대상 사서함 복원 중인 후 비활성 사서함에서 모든 항목은 영구적으로 삭제가 되지 것입니다. 
    
- **사용 보존 대상 사서함에서 비활성 사서함을 복원 하기 전에.** 비활성 사서함에서 사서함 항목을 이전 될 수 있으므로 비활성 사서함을 복원 하기 전에 대상 사서함에 보존 대기를 사용 하도록 설정 하는 것이 좋습니다. 배치에 할당 된 보존 정책 보존 보존이 제거 되거나는 보존 대기 될 때까지 기간이 만료 될 때까지 처리 되지 않습니다의 사서함에 보존 대기 합니다. 비활성 사서함에서 오래 된 메시지를 관리 하는 대상 사서함 시간의 소유자를 제공 합니다. 그렇지 않은 경우 보존 정책 수 오래 된 항목 삭제 (항목 이동 또는 보관 사서함에 설정 된 경우) 대상 사서함에 대해 구성 된 보존 설정에 따라 만료 됩니다. 자세한 내용은 [전체 사서함에 보존 대기 Exchange Online을](https://go.microsoft.com/fwlink/?linkid=856300)참조 하십시오.
    
- **AllowLegacyDNMismatch 스위치를 사용 하는 기능은 무엇입니까?** 비활성 사서함을 복원 하려면 앞의 예제를 **AllowLegacyDNMismatch** 스위치는 사용 하 여 서로 다른 대상 사서함을 비활성 사서함 복원 수 있도록 합니다. 일반적인 복원 시나리오에서는 목표는 어디에 원본 및 대상 사서함 같은 사서함 콘텐츠를 복원 하려면입니다. 따라서 기본적으로 **New-mailboxrestorerequest** cmdlet 확인 하는 원본 및 대상 사서함에서 **LegacyExchangeDN** 속성 값은 동일 인지 확인 합니다. 이 사용이 하면 실수로 잘못 된 대상 사서함에 원본 사서함을 복원할 수 없습니다. **AllowLegacyDNMismatch** 스위치를 사용 하지 않고 비활성 사서함을 복원 하는 경우 원본 및 대상 사서함 **LegacyExchangeDN** 속성에 대 한 서로 다른 값이 있는 경우 명령은 실패할 수 있습니다. 
    
- **비활성 사서함에 대 한 다른 복원 시나리오를 구현 하는 New-mailboxrestorerequest cmdlet을 통해 다른 매개 변수를 사용할 수 있습니다.** 예, 대상 사서함의 기본 사서함으로 비활성 사서함에서 보관 사서함을 복원 하려면이 명령을 실행할 수 있습니다. 
    
  ```
  New-MailboxRestoreRequest -SourceMailbox <inactive mailbox> -SourceIsArchive -TargetMailbox <target mailbox> -TargetRootFolder "Inactive Mailbox Archive" -AllowLegacyDNMismatch
  ```

  이 명령을 실행 하 여 대상 사서함의 보관 사서함으로 비활성 기본 사서함을 복원할 수 있습니다.

  ```
  New-MailboxRestoreRequest -SourceMailbox <inactive mailbox> -TargetMailbox <target mailbox> -TargetIsArchive -TargetRootFolder "Inactive Mailbox" -AllowLegacyDNMismatch
  ```

- **매개 변수를 수행 하는 TargetRootFolder를 수행 하는 작업?** 앞에서 설명한 것 처럼 비활성 사서함의 내용을 복원 하는 대상 사서함에 폴더 구조 (루트 라고도 함)의 위쪽에 폴더를 지정 하려면 **TargetRootFolder** 매개 변수를 사용할 수 있습니다. 이 매개 변수를 사용 하지 않으면 비활성 사서함에서 사서함 항목은 대상 사서함의 해당 기본 폴더에 병합 하 고 사용자 지정 폴더는 대상 사서함의 루트에 다시 만들어집니다. 다음 그림은 이러한 차이 사용 하 여 메시지를 **TargetRootFolder** 매개 변수를 사용 하지 않고 강조 표시 합니다. 
    
    **폴더 계층 구조를 대상 사서함 때 TargetRootFolder 매개 변수는 사용 되지 않습니다**
    
    ![TargetRootFolder 매개 변수가 사용되지 않는 경우의 스크린샷](media/76a759af-f483-4d1c-8cc7-243435b5562e.png)
  
    **TargetRootFolder 매개 변수를 사용 하는 경우 대상 사서함에 폴더 계층 구조**
    
    ![TargetRootFolder 매개 변수가 사용된 경우의 스크린샷](media/300da592-7323-48db-b8a4-07012259d113.png)

  

