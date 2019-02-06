---
title: In-place Hold 일시 삭제 된 사서함에 Exchange 온라인 상태로
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
search.appverid: ''
ms.assetid: 421f72bd-dd43-4be1-82f5-0ae9ac43bd00
description: 원본 위치 유지 일시 삭제 된 사서함에 대 한 비활성 확인 하 고 해당 내용을 보존을 만드는 방법에 알아봅니다. 그런 다음 비활성 사서함을 검색 하려면 Microsoft eDiscovery 도구를 사용할 수 있습니다.
ms.openlocfilehash: e666ac608ec224bf97caa947be2cb42b742c6fa9
ms.sourcegitcommit: ca97beff215d154b6ab006ce1222056434fde1a9
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/05/2019
ms.locfileid: "29740800"
---
# <a name="put-an-in-place-hold-on-a-soft-deleted-mailbox-in-exchange-online"></a>In-place Hold 일시 삭제 된 사서함에 Exchange 온라인 상태로

원본 위치 유지 일시 삭제 된 사서함에 대 한 비활성 확인 하 고 해당 내용을 보존을 만드는 방법에 알아봅니다. 그런 다음 비활성 사서함을 검색 하려면 Microsoft eDiscovery 도구를 사용할 수 있습니다.
  
> [!NOTE]
> 새로 만들기 위한 원본 위치 유지 Exchange Online에서 Office 365 및 Exchange Online 독립 실행형 계획) (에 마감을 연기 했을 때 했습니다. 하지만 올해 또는 초기 다음 연도 새로 만들기 원본 위치 유지 Exchange 온라인 수 없습니다. 원본 위치 유지를 사용 하는 대신, 또는 사용할 수 있습니다 [eDiscovery 사례](https://go.microsoft.com/fwlink/?linkid=780738) [보존 정책](https://go.microsoft.com/fwlink/?linkid=827811) 에서 Office 365 보안 &amp; 준수 센터입니다. 원본 위치 유지는 새로운 해제, 후에 여전히 기존 전체가 보유 하 고 수정할 수 있습니다 하 고 새로 만들기 전체를 포함 하 고 Exchange Server 2013 및 Exchange 하이브리드 배포는 여전히 지원 됩니다. 및 여전히 소송 보존으로 설정에서 사서함을 배치할 수 있습니다. 
  
여기서 사용자 조직, 왼쪽 및가 해당 사용자 계정 및 사서함 삭제 된 상황이 있을 수 있습니다. 나중에, 유지 하는 사서함에 대 한 정보는 실현 합니다. 어떻게 해야 합니까? 삭제 된 사서함 보존 기간이 만료 되지 않았으면 하는 경우 (일시 삭제 된 사서함 라고 함)는 삭제 된 사서함에 In-place Hold를 입력 하 고 비활성 사서함을 만들 수 있습니다. *비활성 사서함* 이 있는 자신이 조직을 떠난 후 이전 직원의 전자 메일을 유지 하기 위해 사용 됩니다. 비활성 이었습니다 때 일시 삭제 된 사서함에 있던 원본 위치 유지 기간이 배치에 대 한 비활성 사서함의 내용은 유지 됩니다. Office 365 보안에서 콘텐츠 검색 Exchange online에서는 원본 위치 eDiscovery를 사용 하 여 사서함을 검색할 수 사서함 비활성 이루어진 후 &amp; 준수 센터 또는 SharePoint Online에서 eDiscovery 센터입니다. 
  
> [!NOTE]
> Exchange Online에서 일시 삭제 된 사서함: 특정 보존 기간 내에서 복구할 수 있지만 삭제 된 사서함 Exchange Online에서 일시 삭제 된 사서함 보존 기간 30 일입니다. 즉, 사서함 수 있음을 복구할 (또는 비활성 사서함 내용을) 삭제 되 고 30 일 이내입니다. 30 일 후 일시 삭제 된 사서함은 영구적으로 삭제를 위해 표시 하 고 복구 하거나 수 비활성 합니다. 
  
## <a name="before-you-begin"></a>시작하기 전에

- Windows PowerShell에서 **New-mailboxsearch** cmdlet을 사용 하면 일시 삭제 된 사서함에는 원본 위치 유지를 배치 해야 합니다. Exchange 관리 센터 (EAC) 또는 SharePoint Online에서 eDiscovery 센터를 사용할 수 없습니다. 
    
- Windows PowerShell을 사용하여 Exchange Online에 연결하는 방법에 대한 자세한 내용은 [Connect to Exchange Online Using Remote PowerShell](https://go.microsoft.com/fwlink/p/?linkid=396554)을 참조하세요.
    
- 조직에서 일시 삭제 된 사서함에 대 한 id 정보를 가져오려면 다음 명령을 실행 합니다. 
    
  ```
  Get-Mailbox -SoftDeletedMailbox | FL Name,WhenSoftDeleted,DistinguishedName,ExchangeGuid,PrimarySmtpAddress
  ```

- 비활성 사서함에 대 한 자세한 내용은 [Office 365에서 비활성 사서함의 개요](inactive-mailboxes-in-office-365.md)를 참조 하십시오.
    
## <a name="put-an-in-place-hold-on-a-soft-deleted-mailbox-to-make-it-an-inactive-mailbox"></a>비활성 사서함 하도록 일시 삭제 된 사서함에는 원본 위치 유지를 배치 합니다.

일시 삭제 된 사서함을 비활성 사서함 만들기 **New-mailboxsearch** cmdlet을 사용 합니다. 자세한 내용은 [New-mailboxsearch](http://technet.microsoft.com/library/74303b47-bb49-407c-a43b-590356eae35c.aspx)를 참조 하십시오.
  
1. 일시 삭제 된 사서함의 속성을 포함 하는 변수를 만듭니다. 
    
   ```
   $SoftDeletedMailbox = Get-Mailbox -SoftDeletedMailbox -Identity <identity of soft-deleted mailbox>
   ```

    > [!IMPORTANT]
    > 이전 명령에서 일시 삭제 된 사서함을 식별할 **DistinguishedName** 또는 **ExchangeGuid** 속성 값을 사용 합니다. 이러한 속성은는 활성 사서함과 일시 삭제 된 사서함 수는 동일한 기본 SMTP 주소 수도 있지만 조직 전체에서 각 사서함에 대 한 고유 합니다. 
  
2. 원본 위치 유지를 만들고 일시 삭제 된 사서함에 배치 합니다. 이 예제에서는 대기 기간이 지정 됩니다. 즉, 무기한 보류 비활성 사서함에서 제거 될 때까지 또는 항목에 보관 됩니다.
    
   ```
   New-MailboxSearch -Name "InactiveMailboxHold" -SourceMailboxes $SoftDeletedMailbox.DistinguishedName -InPlaceHoldEnabled $true
    ```
   원본 위치 유지를 만들 때 보류 기간을 지정할 수도 있습니다. 이 예제에서는 약 7 년에 대 한 비활성 사서함에 있는 항목을 보유 합니다.
    
   ```
   New-MailboxSearch -Name "InactiveMailboxHold" -SourceMailboxes $SoftDeletedMailbox.DistinguishedName -InPlaceHoldEnabled $true -ItemHoldPeriod 2777
   ```

3. 잠시 후 일시 삭제 된 사서함 비활성 사서함 인지를 확인 하려면 다음 명령 중 하나를 실행 합니다.
    
   ```
   Get-Mailbox -InactiveMailboxOnly
   ```

    또는
    
   ```
   Get-Mailbox -InactiveMailboxOnly -Identity $SoftDeletedMailbox.DistinguishedName  | FL IsInactiveMailbox
   ```

## <a name="more-information"></a>추가 정보

비활성 사서함 일시 삭제 된 사서함을 변경한 후 다양 한 방법으로 사서함을 관리할 수 있습니다. 자세한 내용은 다음을 참조 합니다.
  
- [비활성 사서함의 유지 보존 기간 변경](change-the-hold-duration-for-an-inactive-mailbox.md)
    
- [비활성 사서함 복구](recover-an-inactive-mailbox.md)
    
- [비활성 사서함 복원](restore-an-inactive-mailbox.md)
    
- [비활성 사서함 삭제](delete-an-inactive-mailbox.md) 보류를 제거 하는) (여
