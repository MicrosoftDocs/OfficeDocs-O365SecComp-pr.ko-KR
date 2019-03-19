---
title: Office 365에서 무제한 보관을 사용 하도록 설정-관리자 도움말
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 6/29/2018
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- Strat_O365_IP
- M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: e2a789f2-9962-4960-9fd4-a00aa063559e
description: '관리자: 사용자에 게 Exchange Online 사서함에 대 한 무제한 저장소를 제공 하는 Office 365에서 자동 확장 보관을 사용 하도록 설정 하는 방법을 알아봅니다. 전체 조직 또는 특정 사용자만 자동 확장 보관을 사용 하도록 설정할 수 있습니다.'
ms.openlocfilehash: 634807a687a8ccbb764a54300f338263f876b604
ms.sourcegitcommit: b688d67935edb036658bb5aa1671328498d5ddd3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/19/2019
ms.locfileid: "30670623"
---
# <a name="enable-unlimited-archiving-in-office-365---admin-help"></a>Office 365에서 무제한 보관을 사용 하도록 설정-관리자 도움말

Office 365에서 Exchange Online 자동 확장 보관 기능을 사용 하 여 보관 사서함에 대해 무제한 저장 공간을 사용 하도록 설정할 수 있습니다. 자동 확장 보관이 켜져 있는 경우 저장소 제한에 도달 하면 추가 저장소 공간이 사용자의 보관 사서함에 자동으로 추가 됩니다. 따라서 사서함 저장소 용량 제한이 없습니다. 조직의 모든 사용자 또는 특정 사용자에 대해서만 자동 확장 보관을 설정할 수 있습니다. 자동 확장 보관에 대 한 자세한 내용은 [Office 365의 무제한 보관 개요](unlimited-archiving.md)를 참조 하세요.

## <a name="before-you-begin"></a>시작하기 전에

- 전체 조직 또는 특정 사용자에 대해 자동 확장 보관을 사용 하도록 설정 하려면 Office 365 조직의 전역 관리자 이거나 Exchange Online 조직에서 조직 관리 역할 그룹의 구성원 이어야 합니다. 또는 특정 사용자에 대 한 자동 확장 보관을 사용 하도록 설정 하려면 Mail Recipients 역할이 할당 된 역할 그룹의 구성원 이어야 합니다.
    
- 자동 확장 보관을 사용 하도록 설정 하려면 먼저 사용자의 보관 사서함을 사용 하도록 설정 해야 합니다. 보관 사서함을 사용 하도록 설정 하려면 사용자에 게 Exchange Online 계획 2 라이선스를 할당 받아야 합니다. 사용자에 게 exchange online 계획 1 라이선스가 할당 된 경우 해당 보관 사서함을 사용 하도록 설정 하기 위해 별도의 exchange online 보관 라이선스를 할당 해야 합니다. [Office 365 보안 &amp; 및 준수 센터에서 보관 사서함 사용](enable-archive-mailboxes.md)을 참조 하세요.
    
- 또한 PowerShell을 사용 하 여 보관 사서함을 사용 하도록 설정할 수 있습니다. 조직의 모든 사용자에 대해 보관 사서함을 사용 하도록 설정 하는 데 사용할 수 있는 PowerShell 명령의 예는 [추가 정보](#more-information) 섹션을 참조 하십시오. 
    
- 자동 확장 보관 기능은 공유 사서함도 지원합니다. 공유 사서함에 대 한 보관 함을 사용 하도록 설정 하려면 exchange online 계획 2 라이선스 또는 교환 라이선스가 있는 exchange online 계획 1 라이선스가 필요 합니다.
    
- Exchange 관리 센터 또는 보안 &amp; 및 준수 센터를 사용 하 여 자동 확장 보관을 사용 하도록 설정할 수는 없습니다. Exchange Online PowerShell을 사용 해야 합니다. 원격 PowerShell을 사용 하 여 exchange online 조직에 연결 하려면 [exchange online PowerShell에 연결](https://go.microsoft.com/fwlink/p/?linkid=396554)을 참조 하세요.
    
  
## <a name="enable-auto-expanding-archiving-for-your-entire-organization"></a>전체 조직에 대해 자동 확장 보관을 사용 하도록 설정

전체 조직에 대해 자동 확장 보관을 사용 하도록 설정할 수 있습니다. 이 기능을 켜면 기존 사용자 사서함과 새로 만든 사용자 사서함에 대해 자동 확장 보관이 사용 하도록 설정 됩니다. 새 사용자 사서함을 만들 때는 사용자의 기본 보관 사서함을 사용 하도록 설정 하 여 새 사용자 사서함에 대해 자동 확장 보관 기능을 사용할 수 있도록 해야 합니다.
  
1. [원격 PowerShell을 사용하여 Exchange Online에 연결](https://go.microsoft.com/fwlink/p/?linkid=396554)
    
2. Exchange Online PowerShell에서 다음 명령을 실행 하 여 전체 조직에 대해 자동 확장 보관을 사용 하도록 설정 합니다.

    ```
    Set-OrganizationConfig -AutoExpandingArchive
    ```
  
## <a name="enable-auto-expanding-archiving-for-specific-users"></a>특정 사용자에 대해 자동 확장 보관을 사용 하도록 설정

조직의 모든 사용자에 대해 자동 확장 보관을 사용 하도록 설정 하는 대신 특정 사용자 에게만 사용 하도록 설정할 수 있습니다. 이 작업을 수행 하는 경우에는 일부 사용자 에게만 대용량 보관 저장소를 사용할 필요가 있을 수 있습니다.
  
특정 사용자에 대해 자동 확장 보관을 사용 하도록 설정 하 고 보류 중이거나 Office 365 보존 정책에 할당 된 사용자의 사서함에 대해 다음 두 가지 구성 변경이 수행 됩니다.
  
- 사용자의 기본 보관 사서함에 대 한 저장소 할당량을 10gb로 증가 시킵니다 (100에서 110 g b까지). 보관 경고 할당량은 10gb (90에서 100 gb까지)로 증가 합니다.
    
- 사용자의 기본 사서함에 있는 복구 가능한 항목 폴더의 저장소 할당량은 10gb로 증가 합니다 (100에서 110 g b까지). 복구 가능한 항목 경고 할당량은 10gb (90에서 100 gb까지)로 증가 합니다. 이러한 변경 내용은 사서함이 보류 되거나 Office 365 보존 정책에 할당 된 경우에만 적용 됩니다.
    
이 추가 공간은 자동 확장 보관이 구축 되기 전에 발생할 수 있는 저장 문제를 방지 하기 위해 추가 됩니다. 이전 섹션에 설명 된 대로 전체 조직에 대해 자동 확장 보관을 사용 하도록 설정 하면 추가 저장 공간이 추가 *되지 않습니다* . 
  
1. [원격 PowerShell을 사용하여 Exchange Online에 연결](https://go.microsoft.com/fwlink/p/?linkid=396554)
    
2. Exchange Online PowerShell에서 다음 명령을 실행 하 여 특정 사용자에 대해 자동 확장 보관을 사용 하도록 설정 합니다. 앞에서 설명한 것 처럼 사용자의 보관 사서함 (기본 보관 함)을 사용 하도록 설정 해야 해당 사용자에 대해 자동 확장 보관을 설정할 수 있습니다.
    
    ```
    Enable-Mailbox <user mailbox> -AutoExpandingArchive
    ```


> [!IMPORTANT]
> Exchange 하이브리드 배포에서는 기본 사서함이 온-프레미스이 고 보관 사서함이 클라우드 기반 인 특정 사용자에 대해 자동 확장 보관을 사용 하도록 설정 하기 위해 **AutoExpandingArchive** 명령을 사용할 수 없습니다. exchange 하이브리드 배포에서 클라우드 기반 보관 사서함에 대해 자동 확장 보관을 사용 하도록 설정 하려면 exchange Online PowerShell에서 **set-organizationconfig-AutoExpandingArchive** 명령을 실행 하 여 자동 확장 보관을 사용 하도록 설정 해야 합니다. 전체 조직 사용자의 기본 및 보관 사서함이 둘 다 클라우드 기반 인 경우에는 **AutoExpandingArchive** 명령을 사용 하 여 해당 특정 사용자에 대 한 자동 확장 보관을 사용 하도록 설정할 수 있습니다. 
  
## <a name="verify-that-auto-expanding-archiving-is-enabled"></a>자동 확장 보관이 사용 되도록 설정 되어 있는지 확인

조직에 대해 자동 확장 보관을 사용 하도록 설정 되어 있는지 확인 하려면 Exchange Online PowerShell에서 다음 명령을 실행 합니다.

```
Get-OrganizationConfig | FL AutoExpandingArchiveEnabled
```

값은 조직 `True` 에 대해 자동 확장 보관을 사용 하도록 설정 됨을 나타냅니다. 
  
특정 사용자가 자동 확장 보관을 사용 하도록 설정 되어 있는지 확인 하려면 Exchange Online PowerShell에서 다음 명령을 실행 합니다.
  
```
Get-Mailbox <user mailbox> | FL AutoExpandingArchiveEnabled
```
값은 사용자 `True` 에 대해 자동 확장 보관을 사용 하도록 설정 됨을 나타냅니다. 
  
자동 확장 보관을 사용 하도록 설정한 후에는 다음 사항을 염두에 두어야 합니다.
  
- **set-organizationconfig-AutoExpandingArchive** 명령을 실행 하 여 조직에 대해 자동 확장 보관을 사용 하도록 설정 하는 경우에는 개별 사서함에서 **enable-AutoExpandingArchive** 를 실행할 필요가 없습니다. **set-organizationconfig** cmdlet을 실행 하 여 조직에 대해 자동 확장 보관을 사용 하도록 설정 해도 사용자 사서함의 *AutoExpandingArchiveEnabled* 속성은로 `True`변경 되지 않습니다.
    
- 마찬가지로 자동 확장 보관을 사용 하도록 설정 하면 *ArchiveQuota* 및 *ArchiveWarningQuota* 사서함 속성의 값이 변경 되지 않습니다. 실제로 사용자 사서함에 대해 자동 확장 보관을 사용 하도록 설정 하 고 *AutoExpandingArchiveEnabled* `True`속성을로 설정 하면 *ArchiveQuota* 및 *ArchiveWarningQuota* 속성이 무시 됩니다. 다음은 사용자 사서함에 대해 자동 확장 보관을 사용 하도록 설정한 후 이러한 사서함 속성의 예입니다. 
    
    ![자동 확장 보관을 사용 하도록 설정한 후에는 ArchiveQuota 및 ArchiveWarningQuota 속성이 무시 됩니다.](media/6a1c1b69-5c4c-4267-aac8-53577667f03e.png)

  
## <a name="more-information"></a>추가 정보

- 또한 PowerShell을 사용 하 여 보관 사서함을 사용 하도록 설정할 수 있습니다. 예를 들어 Exchange Online PowerShell에서 다음 명령을 실행 하 여 보관 사서함이 아직 사용 하도록 설정 되지 않은 모든 사용자에 대해 보관 사서함을 사용 하도록 설정할 수 있습니다.

    ```
    Get-Mailbox -Filter {ArchiveStatus -Eq "None" -AND RecipientTypeDetails -eq "UserMailbox"} | Enable-Mailbox -Archive
    ```

- 조직 또는 특정 사용자에 대해 자동 확장 보관을 설정 하면 보관 사서함 (복구 가능한 항목 폴더 포함)이 90 GB에 도달할 때 보관 사서함이 자동 확장 아카이브로 변환 됩니다. 추가 저장 공간을 프로 비전 하는 데 최대 30 일이 걸릴 수 있습니다.
    
- 자동 확장 보관을 설정한 후에는 끌 수 없습니다.
    
- 온-프레미스 기본 사서함이 있는 사용자의 경우 Exchange 하이브리드 배포에서 클라우드 기반 보관 사서함에 대해 자동 확장 보관이 지원 됩니다. 그러나 클라우드 기반 보관 사서함에 대해 자동 확장 보관을 사용 하도록 설정한 후에는 온-프레미스 Exchange 조직으로 사서함을 다시 보관 하는 보드를 끌 수 없습니다. Exchange Server 2010의 온-프레미스 사서함에 대해서는 자동 확장 보관이 지원 되지 않습니다.
    
- 사용자가 보관 사서함의 추가 저장소 영역에 있는 항목에 액세스 하는 데 사용할 수 있는 outlook 클라이언트 목록은 [Office 365의 무제한 보관](unlimited-archiving.md#outlook-requirements-for-accessing-items-in-an-auto-expanded-archive) 에 대 한 개요의 "자동 확장 된 보관 함 항목에 액세스 하기 위한 Outlook 요구 사항" 섹션을 참조 하세요. .
    
- 앞에서 설명한 것 처럼, **AutoExpandingArchive** 명령을 실행할 때 사용자의 기본 보관 사서함 및 사서함이 대기 중인 경우 복구 가능한 항목 폴더의 저장소 할당량에 10gb가 추가 됩니다. 이렇게 하면 자동 확장 된 저장소 공간이 프로 비전 될 때까지 (최대 30 일이 걸릴 수 있음) 추가 저장소가 제공 됩니다. **set-organizationconfig-AutoExpandingArchive** 을 실행 하 여 조직의 모든 사서함에 대해 자동 확장 보관을 사용 하도록 설정 하면이 추가 저장소 공간이 추가 되지 않습니다. 전체 조직에 대해 자동 확장 보관을 사용 하도록 설정 했지만 특정 사용자에 게 10gb의 추가 저장 공간을 추가 해야 하는 경우 해당 사서함에서 **AutoExpandingArchive** 명령을 실행할 수 있습니다. 자동 확장 보관이 이미 사용 하도록 설정 되었지만 추가 저장 공간이 사서함에 추가 된다는 오류 메시지가 표시 됩니다. 

- 관리자가 저장소 할당량을 조정할 수 없습니다.

> [!IMPORTANT]
> 자동 확장 보관은 일별 크기가 1gb를 넘지 않는 개별 사용자 또는 공유 사서함에 사용 되는 사서함에 대해서만 지원 됩니다. 보관을 목적으로 저널링, 전송 규칙 또는 자동 전달 규칙을 사용 하 여 보관 사서함에 메시지를 복사할 수는 없습니다. 사용자의 보관 사서함은 해당 사용자만을 위한 것입니다. Microsoft는 사용자의 보관 사서함이 다른 사용자의 보관 데이터를 저장하는데 사용되는 경우 인스턴스의 무제한 보관을 거부할 권리를 가지고 있습니다.
