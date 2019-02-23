---
title: Exchange Online에서 일시 삭제 된 사서함에 원본 위치 유지
ms.author: markjjo
author: markjjo
manager: laurawi
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
search.appverid: ''
ms.assetid: 421f72bd-dd43-4be1-82f5-0ae9ac43bd00
description: 일시 삭제 된 사서함의 원본 위치 유지를 사용 하 여 비활성 상태로 만들고 해당 콘텐츠를 보존 하는 방법을 알아봅니다. 그런 다음 Microsoft eDiscovery 도구를 사용 하 여 비활성 사서함을 검색할 수 있습니다.
ms.openlocfilehash: 70feb265e95741406dbf170c6be70bd83b2ec081
ms.sourcegitcommit: a80bd8626720fabdf592b84e4424cd3a83d08280
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30223527"
---
# <a name="put-an-in-place-hold-on-a-soft-deleted-mailbox-in-exchange-online"></a>Exchange Online에서 일시 삭제 된 사서함에 원본 위치 유지

일시 삭제 된 사서함의 원본 위치 유지를 사용 하 여 비활성 상태로 만들고 해당 콘텐츠를 보존 하는 방법을 알아봅니다. 그런 다음 Microsoft eDiscovery 도구를 사용 하 여 비활성 사서함을 검색할 수 있습니다.
  
> [!NOTE]
> exchange online (Office 365 및 Exchange Online 독립 실행형 계획)에서 새로운 원본 위치 유지를 만드는 마감 기한을 연기 했습니다. 그러나 올해에는 Exchange Online에서 새로운 현재 위치 유지를 만들 수 없습니다. 원본 위치 유지를 사용 하는 대신 Office 365 보안 &amp; 및 준수 센터에서 [eDiscovery 사례](https://go.microsoft.com/fwlink/?linkid=780738) 또는 [보존 정책을](https://go.microsoft.com/fwlink/?linkid=827811) 사용할 수 있습니다. 새로운 원본 위치 유지 기능을 해제 한 후에도 여전히 기존 원본 위치 유지를 수정할 수 있으며, exchange Server 2013 및 exchange 하이브리드 배포에서 새로운 원본 위치 유지를 만드는 것은 여전히 지원 됩니다. 또한 사서함을 소송 보존에도 배치할 수 있습니다. 
  
사용자가 조직을 떠난 경우와 해당 사용자 계정 및 사서함이 삭제 된 상황이 있을 수 있습니다. 나중에 사서함에 보존 해야 하는 정보가 있음을 알게 됩니다. 어떤 작업을 수행 해야 하나요? 삭제 된 사서함 보존 기간이 만료 되지 않은 경우에는 삭제 된 사서함 (일시 삭제 된 사서함 이라고 함)에 원본 위치 유지를 설정 하 고 비활성 사서함으로 설정할 수 있습니다. *비활성 사서함* 은 조직에서 이전 직원의 전자 메일을 보존 하는 데 사용 됩니다. 비활성 사서함의 콘텐츠는 비활성 상태로 설정 되었을 때 일시 삭제 된 사서함에 있던 원본 위치 유지 기간 동안 보존 됩니다. 사서함을 비활성화 한 후에는 Exchange online의 원본 위치 eDiscovery, Office 365 보안 &amp; 및 준수 센터의 콘텐츠 검색 또는 SharePoint Online의 eDiscovery Center를 사용 하 여 사서함을 검색할 수 있습니다. 
  
> [!NOTE]
> Exchange Online에서 일시 삭제 된 사서함은 삭제 되었지만 특정 보존 기간 내에 복구할 수 있는 사서함입니다. Exchange Online의 일시 삭제 된 사서함 보존 기간은 30 일입니다. 즉, 삭제 된 30 일 이내에 사서함을 복구 하거나 비활성 사서함을 만들 수 있습니다. 30 일이 지나면 일시 삭제 된 사서함은 영구적으로 삭제 되도록 표시 되며 복구 하거나 비활성 상태로 설정할 수 없습니다. 
  
## <a name="before-you-begin"></a>시작하기 전에

- Windows PowerShell에서 **new-mailboxsearch** cmdlet을 사용 하 여 일시 삭제 된 사서함을 원본 위치 유지 상태로 설정 해야 합니다. SharePoint Online의 EAC (Exchange 관리 센터) 또는 eDiscovery 센터를 사용할 수 없습니다. 
    
- Windows PowerShell을 사용하여 Exchange Online에 연결하는 방법에 대한 자세한 내용은 [Connect to Exchange Online Using Remote PowerShell](https://go.microsoft.com/fwlink/p/?linkid=396554)을 참조하세요.
    
- 다음 명령을 실행 하 여 조직의 일시 삭제 된 사서함에 대 한 id 정보를 가져옵니다. 
    
  ```
  Get-Mailbox -SoftDeletedMailbox | FL Name,WhenSoftDeleted,DistinguishedName,ExchangeGuid,PrimarySmtpAddress
  ```

- 비활성 사서함에 대 한 자세한 내용은 [Overview in Office 365의 비활성 사서함 개요](inactive-mailboxes-in-office-365.md)를 참조 하세요.
    
## <a name="put-an-in-place-hold-on-a-soft-deleted-mailbox-to-make-it-an-inactive-mailbox"></a>일시 삭제 된 사서함에 원본 위치 유지를 적용 하 여 비활성 사서함으로 설정

**new-mailboxsearch** cmdlet을 사용 하 여 일시 삭제 된 사서함을 비활성 사서함으로 만들 수 있습니다. 자세한 내용은 [new-mailboxsearch](http://technet.microsoft.com/library/74303b47-bb49-407c-a43b-590356eae35c.aspx)를 참조 하십시오.
  
1. 일시 삭제 된 사서함의 속성이 포함 된 변수를 만듭니다. 
    
   ```
   $SoftDeletedMailbox = Get-Mailbox -SoftDeletedMailbox -Identity <identity of soft-deleted mailbox>
   ```

    > [!IMPORTANT]
    > 이전 명령에서 **DistinguishedName** 또는 **ExchangeGuid** 속성 값을 사용 하 여 일시 삭제 된 사서함을 식별 합니다. 이러한 속성은 조직의 각 사서함에 대해 고유 하지만 활성 사서함과 일시 삭제 된 사서함의 기본 SMTP 주소가 같을 수 있습니다. 
  
2. 원본 위치 유지를 만들고 일시 삭제 된 사서함에 배치 합니다. 이 예에서는 보존 기간을 지정 하지 않습니다. 즉, 항목이 무기한으로 또는 비활성 사서함에서 제거 될 때까지 유지 됩니다.
    
   ```
   New-MailboxSearch -Name "InactiveMailboxHold" -SourceMailboxes $SoftDeletedMailbox.DistinguishedName -InPlaceHoldEnabled $true
    ```
   원본 위치 유지를 만들 때 보존 기간을 지정할 수도 있습니다. 이 예에서는 약 7 년 동안 비활성 사서함의 항목을 포함 합니다.
    
   ```
   New-MailboxSearch -Name "InactiveMailboxHold" -SourceMailboxes $SoftDeletedMailbox.DistinguishedName -InPlaceHoldEnabled $true -ItemHoldPeriod 2777
   ```

3. 잠시 후에 다음 명령 중 하나를 실행 하 여 일시 삭제 된 사서함이 비활성 사서함 인지 확인 합니다.
    
   ```
   Get-Mailbox -InactiveMailboxOnly
   ```

    또는
    
   ```
   Get-Mailbox -InactiveMailboxOnly -Identity $SoftDeletedMailbox.DistinguishedName  | FL IsInactiveMailbox
   ```

## <a name="more-information"></a>추가 정보

일시 삭제 된 사서함을 비활성 사서함으로 설정한 후 사서함을 관리 하는 방법에는 여러 가지가 있습니다. 자세한 내용은 다음 항목을 참조 하십시오.
  
- [비활성 사서함의 유지 보존 기간 변경](change-the-hold-duration-for-an-inactive-mailbox.md)
    
- [비활성 사서함 복구](recover-an-inactive-mailbox.md)
    
- [비활성 사서함 복원](restore-an-inactive-mailbox.md)
    
- [비활성 사서함 삭제](delete-an-inactive-mailbox.md) (보류 제거)
