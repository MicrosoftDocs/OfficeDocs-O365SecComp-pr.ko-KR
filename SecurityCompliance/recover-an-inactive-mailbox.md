---
title: Office 365에서 비활성 사서함 복구
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 6/21/2018
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
ms.collection: M365-security-compliance
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: 35d0ecdb-7cb0-44be-ad5c-69df2f8f8b25
description: '이전 직원이 조직에 반환 되는 경우 또는 이거나 퇴직 한 직원의 직무에 따라 새 직원을 고용 하는 경우 Office 365에서 비활성 사서함의 콘텐츠를 복구할 수 있습니다. 비활성 사서함을 복구 하면 비활성 사서함의 내용이 포함 된 새 사서함으로 변환 됩니다. '
ms.openlocfilehash: c7f942c518dcc74a4bdb37d67e27e8a63879ab46
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32261546"
---
# <a name="recover-an-inactive-mailbox-in-office-365"></a>Office 365에서 비활성 사서함 복구

일시 삭제 된 사서함 유형의 비활성 사서함은 조직 내에서 이전 직원의 전자 메일을 보존 하는 데 사용 됩니다. 해당 직원이 조직에 반환 되는 경우 또는 이전 직원의 작업에 다른 직원이 참여 하는 경우 비활성 사서함의 내용을 사용자가 사용할 수 있도록 하는 방법에는 두 가지가 있습니다. 
  
- **비활성 사서함 복구** 이전 직원이 조직에 게 반환 되거나, 이전 직원의 작업을 담당 하는 새 직원이 고용 되 면 비활성 사서함의 내용을 복구할 수 있습니다. 이 메서드는 비활성 사서함을 비활성 사서함의 콘텐츠를 포함 하는 새 활성 사서함으로 변환 합니다. 복구한 후 비활성 사서함 존재 하지 않습니다. 이 항목의 절차에서는이 방법에 대해 설명 합니다. 
    
- **비활성 사서함 복원** 다른 직원이 이전 직원의 업무 책임을 취하고 있거나, 다른 사용자가 비활성 사서함의 콘텐츠에 액세스 해야 하는 경우 비활성 사서함의 내용을 기존 사서함으로 복원 하거나 병합할 수 있습니다. 비활성 사서함에서 보관 함을 복원할 수도 있습니다. 이 방법에 대 한 절차에 대 한 자세한 내용은 [Office 365에서 비활성 사서함 복원을](restore-an-inactive-mailbox.md)참조 하십시오.
    
비활성 사서함 복구 및 복원과 비활성 사서함을 복구할 때 수행 되는 작업에 대 한 자세한 [내용은 추가 정보](#more-information) 섹션을 참조 하십시오.
  
> [!NOTE]
> 사서함을 비활성 상태로 만들기 위해 새 원본 위치 유지를 만드는 마감 기한을 연기 했습니다. 하지만 나중에 Exchange Online에서는 새로운 원본 위치 유지를 만들 수 없습니다. 그때는 소송 보존과 Office 365 보존 정책만 사용하여 비활성화 사서함을 만들 수 있습니다. 그러나 원본 위치 유지에 있는 기존 비활성화 사서함은 계속 지원되며 비활성화 사서함에서 원본 위치 유지를 계속 관리할 수 있습니다. 관리 항목으로는 원본 위치 유지 기간 변경 및 원본 위치 유지를 삭제하여 비활성화 사서함을 영구 삭제하는 작업이 포함됩니다. 
  
## <a name="before-you-begin"></a>시작하기 전에

- 비활성 사서함을 복원 하려면 Exchange Online PowerShell을 사용 해야 합니다. EAC(Exchange 관리 센터)는 사용할 수 없습니다. 단계별 지침은 [Exchange Online PowerShell에 연결을](https://go.microsoft.com/fwlink/?linkid=396554)참조 하십시오.
    
- 다음 명령을 실행 하 여 조직의 비활성 사서함에 대 한 id 정보를 가져옵니다. 

    ```
    Get-Mailbox -InactiveMailboxOnly | FL Name,DistinguishedName,ExchangeGuid,PrimarySmtpAddress
    ```

    이 명령에서 반환 하는 정보를 사용 하 여 특정 비활성 사서함을 복구 합니다.
    
- 비활성 사서함에 대 한 자세한 내용은 [Office 365의 비활성 사서함](inactive-mailboxes-in-office-365.md)을 참조 하십시오.
    
## <a name="recover-an-inactive-mailbox"></a>비활성 사서함 복구

비활성 사서함을 복구 하려면 *inactivemailbox* 매개 변수와 함께 **새 사서함** cmdlet을 사용 합니다. 
  
1. 비활성 사서함의 속성을 포함 하는 변수를 만듭니다. 
    
    ```
    $InactiveMailbox = Get-Mailbox -InactiveMailboxOnly -Identity <identity of inactive mailbox>
    ```
   
    > [!IMPORTANT]
    > 이전 명령에서 **DistinguishedName** 또는 **ExchangeGUID** 속성 값을 사용 하 여 비활성 사서함을 식별 합니다. 이러한 속성은 조직의 각 사서함에 대해 고유 하지만 활성 및 비활성 사서함의 기본 SMTP 주소가 같을 수 있습니다. 
  
2. 이 예에서는 이전 명령에서 가져온 속성을 사용 하 고 비활성 사서함을 사용자 Ann Beebe의 활성 사서함에 복구 합니다. *Name* 및 *MicrosoftOnlineServicesID* 매개 변수에 지정 된 값은 조직 내에서 고유 해야 합니다. 

    ```
    New-Mailbox -InactiveMailbox $InactiveMailbox.DistinguishedName -Name annbeebe -FirstName Ann -LastName Beebe -DisplayName "Ann Beebe" -MicrosoftOnlineServicesID Ann.Beebe@contoso.com -Password (ConvertTo-SecureString -String 'P@ssw0rd' -AsPlainText -Force) -ResetPasswordOnNextLogon $true
    ```

    복구 된 비활성 사서함의 기본 SMTP 주소는 *MicrosoftOnlineServicesID* 매개 변수에 지정 된 것과 같은 값을 갖습니다. 
    
비활성 사서함을 복구한 후에는 새 Office 365 사용자 계정도 만들어집니다. 라이선스를 할당하여 이 사용자 계정을 활성화해야 합니다. Microsoft 365 관리 센터에서 라이선스를 할당하려면 [비즈니스용 Office 365 라이선스 할당 또는 할당 취소](https://go.microsoft.com/fwlink/p/?LinkId=276798)를 참조하세요.
  
## <a name="more-information"></a>추가 정보

- **비활성 사서함을 복구 하 고 복원 하는 경우의 주요 차이점은 무엇 인가요?** 비활성 사서함을 복구 하면 기본적으로 사서함이 새 사서함으로 변환 되며 비활성 사서함의 콘텐츠 및 폴더 구조가 보존 되 고 사서함이 새 사용자 계정에 연결 됩니다. 복구를 복구한 후에는 비활성 사서함이 더 이상 존재 하지 않으며, 새 사서함의 콘텐츠에 대 한 변경 내용은 원래 비활성 사서함에서 유지 되었던 콘텐츠에 영향을 줍니다. 반대로 비활성 사서함을 복원 하는 경우에는 콘텐츠가 다른 사서함으로 복사 되기만 합니다. 비활성 사서함은 유지 되 고 비활성 사서함은 유지 됩니다. 대상 사서함의 콘텐츠가 변경 되어도 비활성 사서함에 저장 된 원래 콘텐츠에는 영향을 주지 않습니다. 원본 위치 eDiscovery를 사용 하 여 비활성 사서함을 여전히 검색할 수 있으며, 해당 콘텐츠를 다른 사서함으로 복원 하거나 나중에 복구 하거나 삭제할 수 있습니다. 
    
- **비활성 사서함을 복구 하면 어떻게 되나요?** 비활성 사서함을 복구 하면 다음과 같은 상황이 발생 합니다. 
    
  - 소송 보존 (비활성 사서함에 대해 사용 하도록 설정 된 경우)이 제거 됩니다.
    
  - 원본 위치 유지는 제거 됩니다. 즉, 비활성 사서함은 원본 위치 유지 또는 현재 위치 eDiscovery 검색에서 소스 사서함으로 제거 됩니다. 
    
  - 비활성 사서함이 적용 된 Office 365 보존 정책에서 제거 됩니다.
    
  - **RetainDeletedItemsFor** mailbox 속성으로 정의 되는 단일 항목 복구 기간은 30 일로 설정 됩니다. 일반적으로 Exchange Online에서 새 사서함을 만들면이 보존 기간은 14 일로 설정 됩니다. 이 값을 최대 30 일로 설정 하면 비활성 사서함에서 영구적으로 삭제 (또는 제거 된) 데이터를 복구할 수 있는 시간이 더 많이 제공 됩니다. 단일 항목 복구를 사용 하지 않도록 설정 하거나 단일 항목 복구 기간을 기본값인 14 일로 다시 설정할 수도 있습니다. 자세한 내용은 [사서함에 대한 단일 항목을 사용하거나 사용하지 않도록 설정](https://go.microsoft.com/fwlink/?linkid=856769)을 참조하세요.
    
  - 보존 설정이 사용 하도록 설정 되어 있고 보존 기간이 30 일로 설정 됩니다. 즉, 기본 Exchange 보존 정책 및 새 사서함에 할당 된 조직 전체 또는 Exchange 전체 Office 365 보존 정책은 30 일 동안 처리 되지 않습니다. 이렇게 하면 반환 되는 직원 또는 복구 된 비활성 사서함 시간의 새 소유자가 이전 메시지를 관리할 수 있습니다. 그렇지 않으면 exchange 또는 office 365 보존 정책에서 exchange 또는 office 365 보존 정책에 대해 구성 된 설정을 기반으로 만료 된 이전 사서함 항목을 삭제 하거나 (사용 하도록 설정 된 경우 보관 사서함으로 항목을 이동할 수 있음) 30 일 후에 보존 기간이 만료 되 면 **RetentionHoldEnabled** mailbox 속성은 **False**로 설정 되 고 관리 되는 폴더 도우미는 사서함에 할당 된 정책을 처리 하기 시작 합니다. 이 추가 시간이 필요 하지 않으면 보존 유지를 제거 하면 됩니다. 또는, **설정 된 사서함-enddatefor소송** 명령을 사용 하 여 보존 기간을 늘릴 수 있습니다. 자세한 내용은 [사서함을 보존 상태로 두기](https://go.microsoft.com/fwlink/?linkid=856300)를 참조 하십시오.
    
- **비활성 사서함의 원래 상태를 보존 해야 하는 경우 복구 된 사서함을 유지 합니다.** 새 사서함 소유자 또는 보존 정책이 복구 된 비활성 사서함에서 메시지를 영구적으로 삭제 하지 못하게 하려면 사서함에 소송 보존을 설정할 수 있습니다. 자세한 내용은 [사서함을 소송 보존으로 설정](https://go.microsoft.com/fwlink/?linkid=856286)를 참조 하십시오.
    
- **비활성 사서함을 복구할 때 사용할 수 있는 사용자 ID는 무엇입니까?** 비활성 사서함을 복구 하는 경우 *MicrosoftOnlineServicesID* 매개 변수에 대해 지정 하는 값은 비활성 사서함과 연결 된 것과 다를 수 있습니다. 원래 사용자 ID를 사용할 수도 있습니다. 하지만 앞에서 설명한 것 처럼, 비활성 사서함을 복구 하는 경우 *Name* 및 *MicrosoftOnlineServicesID* 에 사용 되는 값이 조직 내에서 고유한 지 확인 합니다. 
    
- **비활성 사서함의 사서함 보존 기간이 만료 되지 않은 경우 어떻게 하나요?** 비활성 사서함이 30 일 보다 적게 일시 삭제 된 경우에는 **새 사서함 inactivemailbox** 명령을 사용 하 여 복구할 수 없습니다. 해당 하는 Office 365 사용자 계정을 복원 하 여 복구 해야 합니다. 자세한 내용은 [사용자 삭제 또는 복원을](https://go.microsoft.com/fwlink/p/?LinkId=279162)참조 하세요.
    
- **비활성 사서함의 일시 삭제 된 사서함 보존 기간이 만료 되었는지 어떻게 알 수 있나요?** 다음 명령을 실행합니다. 
    
    ```
    Get-Mailbox -InactiveMailboxOnly <identity of inactive mailbox> | FL ExternalDirectoryObjectId
  ```

    **externaldirectoryobjectid** 속성에 대 한 값이 없으면 사서함 보존 기간이 만료 된 것 이며, **새 사서함-inactivemailbox** 명령을 실행 하 여 비활성 사서함을 복구할 수 있습니다. **externaldirectoryobjectid** 속성에 대 한 값이 있는 경우 일시 삭제 된 사서함 보존 기간은 만료 되지 않으며 Office 365 사용자 계정을 복원 하 여 사서함을 복구 해야 합니다. [사용자 삭제 또는 복원을](https://go.microsoft.com/fwlink/p/?LinkId=279162) 참조 하세요.
    
- **비활성 사서함을 복구한 후 보관 사서함을 사용 하도록 설정 하는 것이 좋습니다.** 이렇게 하면 반환 되는 사용자 또는 새 직원은 이전 메시지를 보관 사서함으로 이동할 수 있습니다. 보존 기간이 만료 되 면 Exchange Online 사서함에 할당 된 기본 exchange 보존 정책의 일부인 보관 정책이 보관 사서함으로 2 년 이상 된 항목을 이동 합니다. 보관 사서함을 사용 하도록 설정 하지 않으면 2 년 보다 오래 된 항목이 사용자의 기본 사서함에 남아 있게 됩니다. 자세한 내용은 [Office 365 보안 &amp; 및 준수 센터에서 보관 사서함 사용](enable-archive-mailboxes.md)을 참조 하십시오.
 