---
title: Office 365에서 비활성 사서함 복구
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 6/21/2018
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: 35d0ecdb-7cb0-44be-ad5c-69df2f8f8b25
description: '이전 직원이 조직에 반환 하는 경우 또는 이전된 직원의 직무에 적용할 새 직원 고용 하는 경우에 Office 365에서 비활성 사서함의 콘텐츠를 복구할 수 있습니다. 비활성 사서함을 복구 하는 경우 비활성 사서함의 내용이 포함 된 새 사서함으로 변환 됩니다. '
ms.openlocfilehash: dcc84e44454a75f8b4dac953599632d632f340b9
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22534056"
---
# <a name="recover-an-inactive-mailbox-in-office-365"></a>Office 365에서 비활성 사서함 복구

비활성 사서함 (즉, 일시 삭제 된 사서함의 형식)가 자신이 조직을 떠난 후 이전 직원의 전자 메일을 유지 하기 위해 사용 됩니다. 해당 직원이 조직에 반환 하는 경우 또는 다른 직원 이전 직원의 직무에 수행 하는 경우에 경우 사용할 수 있는 비활성 사서함의 내용을 사용자에 게 두 가지가 있습니다. 
  
- **비활성 사서함 복구** 이전 직원이 조직에 반환 하는 경우 또는 이전 직원의 직무에 적용할 새 직원 고용 하는 경우 비활성 사서함의 내용을 복구할 수 있습니다. 이 메서드는 비활성 사서함의 내용이 포함 된 새, 활성 사서함을 비활성 사서함을 변환 합니다. 복구한 후 비활성 사서함 존재 하지 않습니다. 이 항목의 절차에서는이 메서드를 설명합니다. 
    
- **비활성 사서함 복원** 이전 직원의 직무에 가져와 다른 직원 또는 비활성 사서함의 내용에 대 한 액세스를 필요로 하는 다른 사용자 있습니다 수 복원 (또는 병합) 기존 사서함을 비활성 사서함의 내용을 합니다. 비활성 사서함에서 보관 사서함에 복원할 수도 있습니다. 이 메서드에 대 한 절차, [Office 365에서 비활성 사서함 복원](restore-an-inactive-mailbox.md)을 참조 하십시오.
    
비활성 사서함, 복원 및 복구 간의 차이점에 대 한 자세한 내용은 및 비활성 사서함을 복구할 때 수행 하는 작업에 대 한 설명을 대 한 [자세한 내용](recover-an-inactive-mailbox.md#moreinfo) 은 섹션을 참조 합니다.
  
> [!NOTE]
> 전체 사서함을 비활성화 하려면을 포함 하 고 새로 만들기에 대 한 마감을 연기 했을 때 했습니다. 하지만 일부 지점에서 나중에 수 없을 것 새로 만들려면 원본 위치 유지 Exchange 온라인 합니다. 그 당시 소송 보존을 포함 하 고 및 Office 365의 보존 정책에 대 한 비활성 사서함 만들기를 사용할 수 있습니다. 그러나 원본 위치 유지에 있는 기존 비활성 사서함은 여전히 지원 됩니다 및 비활성 사서함에서 원본 위치 유지 관리를 계속 받을 수 있습니다. In-place Hold의 지속 시간을 변경 하 고 원본 위치 유지를 제거 하 여 비활성 사서함을 영구적으로 삭제이 포함 됩니다. 
  
## <a name="before-you-begin"></a>시작하기 전에

- 비활성 사서함을 복원 하려면 Exchange Online PowerShell을 사용 해야 합니다. Exchange 관리 센터 (EAC)를 사용할 수 없습니다. 단계별 지침은 [Connect to Exchange Online PowerShell를](https://go.microsoft.com/fwlink/?linkid=396554)참조 하십시오.
    
- 조직에서 비활성 사서함에 대 한 id 정보를 가져오려면 다음 명령을 실행 합니다. 

    ```
    Get-Mailbox -InactiveMailboxOnly | FL Name,DistinguishedName,ExchangeGuid,PrimarySmtpAddress
    ```

    이 명령에서 반환 되는 정보를 사용 하 여 특정 비활성 사서함을 복구 합니다.
    
- 비활성 사서함에 대 한 자세한 내용은 [Office 365에서 비활성 사서함](inactive-mailboxes-in-office-365.md)을 참조 하십시오.
    
## <a name="recover-an-inactive-mailbox"></a>비활성 사서함 복구

비활성 사서함을 복구 하는 *InactiveMailbox* 매개 변수와 함께 **새 사서함** cmdlet을 사용 합니다. 
  
1. 비활성 사서함의 속성을 포함 하는 변수를 만듭니다. 
    
    ```
    $InactiveMailbox = Get-Mailbox -InactiveMailboxOnly -Identity <identity of inactive mailbox>
    ```
   
    > [!IMPORTANT]
    > 이전 명령에서 비활성 사서함을 식별할 **DistinguishedName** 또는 **ExchangeGUID** 속성 값을 사용 합니다. 이러한 속성은 활성 및 비활성 사서함을 들 수 동일한 기본 SMTP 주소 수도 있지만 조직 전체에서 각 사서함에 대 한 고유 합니다. 
  
2. 이 예제에서는 이전 명령에서 가져온 속성을 사용 하 여 및 Ann Beebe 사용자에 대 한 현재 사서함을 비활성 사서함 복구 됩니다. *이름* 및 *MicrosoftOnlineServicesID* 매개 변수에 대해 지정 된 값을 조직 내에서 고유한 지 확인 해야 합니다. 

    ```
    New-Mailbox -InactiveMailbox $InactiveMailbox.DistinguishedName -Name annbeebe -FirstName Ann -LastName Beebe -DisplayName "Ann Beebe" -MicrosoftOnlineServicesID Ann.Beebe@contoso.com -Password (ConvertTo-SecureString -String 'P@ssw0rd' -AsPlainText -Force) -ResetPasswordOnNextLogon $true
    ```

    복구 된 비활성 사서함에 대 한 기본 SMTP 주소 *MicrosoftOnlineServicesID* 매개 변수에 의해 지정 된 것과 동일한 값을 갖게 됩니다. 
    
비활성 사서함을 복구 후 새 Office 365 사용자 계정이 만들어집니다. 라이선스를 할당 하 여이 사용자 계정을 활성화 해야 합니다. Office 365 관리 센터에서 라이선스를 할당 하려면 [할당 또는 비즈니스를 위한 Office 365에 대 한 라이선스를 할당 취소 하려면](https://go.microsoft.com/fwlink/p/?LinkId=276798)을 참조 하십시오.
  
## <a name="more-information"></a>추가 정보

- **비활성 사서함 복원 및 복구 간의 주요 차이점은 무엇입니까?** 비활성 사서함을 복구 하는 경우 사서함은 기본적으로 새 사서함으로 변환 됩니다 내용과 비활성 사서함의 폴더 구조 유지 되므로 및 사서함을 새 사용자 계정에 연결 됩니다. 복구 되 비활성 사서함 더이상 존재 하 고 새 사서함의 콘텐츠를 변경한 내용을에 원래 있던 콘텐츠에 영향을 주는 후 비활성 사서함에서 대기 합니다. 이와 반대로 비활성 사서함을 복원 하는 경우 내용은 단순히 다른 사서함에 복사 됩니다. 비활성 사서함 보존 되 고 비활성 사서함 유지 됩니다. 대상 사서함의 콘텐츠를 변경한 내용을 비활성 사서함에 보관 원본 콘텐츠에 적용 되지 않습니다. 비활성 사서함 여전히 검색 가능한 원본 위치 eDiscovery를 사용 하 여, 다른 사서함의 내용을 복원할 수 또는 복구 되거나 나중에 삭제 될 수 있습니다. 
    
- **비활성 사서함을 복구 하는 경우 어떻게 됩니까?** 비활성 사서함을 복구 하는 경우 다음과 같은 동작이 수행 됩니다. 
    
  - 소송 보존 (비활성 사서함에 대해 활성화 된) 하는 경우 제거 됩니다.
    
  - 원본 위치 유지 제거 됩니다. 즉,는 비활성 사서함 원본 위치 유지 또는 원본 위치 eDiscovery 검색에서 원본 사서함에서 제거 됩니다. 
    
  - 비활성 사서함 모든 Office 365 보존 정책에서 제거 되는 위치에 적용 된 합니다.
    
  - ( **RetainDeletedItemsFor** 사서함 속성에 의해 정의 된)는 단일 항목 복구 기간을 30 일로 설정 됩니다. 일반적으로 새 사서함이 Exchange Online를 만들면이 보존 기간을 14 일로 설정 됩니다. 이 값 30 일의 최대값을 설정 하면 영구적으로 삭제 되었는지 (또는 제거) 하는 모든 데이터를 복구 하려면 더 많은 시간이 비활성 사서함에서 있습니다. 단일 항목 복구를 사용 하지 않도록 설정 하거나 단일 항목 복구를 설정할 수도 기본값인 14 일에 다시 기간입니다. 자세한 내용은 [사서함에 대 한 단일 항목 복구를 사용 하지 않도록 설정 하거나 사용](https://go.microsoft.com/fwlink/?linkid=856769)을 참조 하십시오.
    
  - 보존 대기 사용 하도록 설정 하 고 보존 대기 기간이 30 일로 설정 됩니다. 즉, 기본 Exchange 보존 정책 및 보존 정책에는 새 사서함에 할당 된 30 일 동안 처리 되지 않습니다 모든 조직 전체 또는 Exchange 전체 Office 365 합니다. 이렇게 하면 반환 직원 또는 복구 된 비활성 사서함 시간의 새 소유자 오래 된 메시지를 관리할 수 있습니다. 그렇지 않은 경우 Exchange 또는 Office 365 보존 정책 수 오래 된 사서함 항목을 삭제 (항목 이동 또는 보관 사서함에 설정 된 경우) Exchange 또는 Office 365 보존 정책에 대해 구성 된 설정에 따라 만료 됩니다. 30 일 후 보존 대기 만료, **RetentionHoldEnabled** 사서함 속성을 **False**로설정하면 설정 하 고 관리 되는 폴더 도우미가 시작 하는 사서함에 할당 된 정책 처리 합니다. 이 추가 시간이 필요 하지 않으면, 보존 대기만 제거할 수 있습니다. 또는 **Set-mailbox EndDateForRetentionHold** 명령을 사용 하 여 보존 대기의 기간을 늘릴 수 있습니다. 자세한 내용은 [사서함 보존에 원본 위치 유지](https://go.microsoft.com/fwlink/?linkid=856300)를 참조 하십시오.
    
- **보류 비활성 사서함의 원래 상태로 유지 하기 위해 필요한 경우 복구 된 사서함.** 보존 정책을 확인 하는 새 사서함 소유자가 비활성 복구 된 사서함에서 모든 메시지를 영구적으로 삭제를 방지 하려면 [전체 사서함에 소송 보존으로 설정](https://go.microsoft.com/fwlink/?linkid=856286)을 참조 하십시오 자세한 내용은 소송 보존에 대 한에서 사서함을 배치할 수 있습니다.
    
- **어떤 사용자 ID를 사용할 수 있는 비활성 사서함을 복구 하는 경우?** 비활성 사서함을 복구 하는 경우에 *MicrosoftOnlineServicesID* 매개 변수에 대해 지정 하는 값을 비활성 사서함에 연결 되었던 원래 각각 다른 수 있습니다. 원래 사용자 ID를 사용할 수도 있습니다. 하지만 앞서 설명한 것 처럼 비활성 사서함을 복구 하는 경우 *이름* 및 *MicrosoftOnlineServicesID* 에 사용 되는 값은 조직 내에서 고유 있는지 확인 합니다. 
    
- **비활성 사서함에 대 한 사서함 보존 기간 만료 하지 않은 경우에 어떻게?** 비활성 사서함 했으므로 일시 삭제 된 30 일 보다 작은, **New-mailbox InactiveMailbox** 명령을 복구를 사용할 수 없습니다. 해당 하는 Office 365 사용자 계정의 복원 하 여 복구 해야 합니다. 자세한 내용은 [사용자를 복원 또는 삭제](https://go.microsoft.com/fwlink/p/?LinkId=279162)를 참조 하십시오.
    
- **어떻게 알 수 있을까요 비활성 사서함에 대 한 일시 삭제 된 사서함 보존 기간이 만료 하는 경우?** 다음 명령을 실행 합니다. 
    
    ```
    Get-Mailbox -InactiveMailboxOnly <identity of inactive mailbox> | FL ExternalDirectoryObjectId
  ```

    **ExternalDirectoryObjectId** 속성에 대 한 값이 없으면 사서함 보존 기간이 만료 되었습니다 하 고 **새로 만들기 사서함 InactiveMailbox** 명령을 실행 하 여 비활성 사서함을 복구할 수 있습니다. **ExternalDirectoryObjectId** 속성에 대 한 값이 있는 경우 일시 삭제 된 사서함 보존 기간이 만료 되지 않았으면 하 고 복원 하는 Office 365 사용자 계정 하 여 사서함을 복구 해야 합니다. [사용자를 복원 또는 삭제](https://go.microsoft.com/fwlink/p/?LinkId=279162) 를 참조 하십시오.
    
- **비활성 사서함을 복구 후 보관 사서함을 사용 하도록 설정 하는 고려 해야할.** 이렇게 하면 반환 하는 사용자 또는 새 직원 오래 된 메시지 보관 사서함으로 이동 합니다. 및 보존 대기 만료 되 면 보관 정책을의 일부인 기본 Exchange 보존 정책을 Exchange Online 사서함 이동 하는 2 년에 속하는 항목에 할당 된 또는 보관 사서함으로 이전 합니다. 보관 사서함을 사용 하도록 설정 하지 하는 경우 사용자의 기본 사서함 2 년 보다 오래 된 항목 유지 됩니다. 자세한 내용은 참조 [Office 365 보안에서 보관 사서함 사용 &amp; 준수 센터](enable-archive-mailboxes.md)합니다.
 