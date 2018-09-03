---
title: Office 365-관리자 도움말 무제한 보관을 사용 하도록 설정
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 6/29/2018
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MOE150
- MET150
ms.assetid: e2a789f2-9962-4960-9fd4-a00aa063559e
description: '관리자를 위한: Exchange Online 사서함에 대 한 무제한으로 저장 된 사용자에 게 제공 하는 Office 365의 보관 자동 확장을 사용 하는 방법을 설명 합니다. 특정 사용자만 또는 전체 조직에 대 한 보관 자동 확장을 사용 하도록 설정할 수 있습니다.'
ms.openlocfilehash: ede3e75a021d750160268ccf06ac4fe1637d219a
ms.sourcegitcommit: 81c2fd5cd940c51bc43ac7858c7bdfa207ce401a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/03/2018
ms.locfileid: "23809703"
---
# <a name="enable-unlimited-archiving-in-office-365---admin-help"></a>Office 365-관리자 도움말 무제한 보관을 사용 하도록 설정

보관 사서함에 대 한 제한 없는 저장 공간을 사용 하도록 설정 하려면 Office 365의 Exchange Online 자동 확장 보관 기능을 사용할 수 있습니다. 보관 자동 확장 기능이 켜져은 추가 저장 공간 저장 용량 제한에 도달 하는 경우 사용자의 보관 사서함에 자동으로 추가 됩니다. 저장 용량 제한 없는 사서함이 반환이 됩니다. 자동 확장 하면 조직에서 모든 사용자에 대 한 이나 특정 사용자만 보관 설정할 수 있습니다. 자동 확장 하는 방법에 대 한 자세한 내용은 [Office 365 무제한 보관의 개요](unlimited-archiving.md)를 참조 보관 하십시오.

## <a name="before-you-begin"></a>시작하기 전에

- Office 365 조직 또는 조직 전체 또는 특정 사용자에 대해 보관 자동 확장을 사용 하 여 Exchange Online 조직에서 조직 관리 역할 그룹의 구성원에 전역 관리자 여야 해야 합니다. 또는 특정 사용자에 대 한 보관 자동 확장을 사용 하 여 편지 병합 받는 사람 역할에 할당 된 역할 그룹의 구성원 이어야 해야 합니다.
    
- 사용자의 보관 사서함에 보관 자동 확장을 설정 하기 전에 사용할 수 있습니다. 사용자의 보관 사서함을 사용 하도록 설정 하려면 Exchange Online 계획 2 라이선스를 할당 해야 합니다. Exchange Online 계획 1 라이선스를 할당 하면 사용자는 자신의 보관 사서함을 사용 하도록 설정 하는 별도 Exchange Online 보관 라이선스가 할당 해야 합니다. 참조 [Office 365 보안에서 보관 사서함 사용 &amp; 준수 센터](enable-archive-mailboxes.md)합니다.
    
- PowerShell을 사용 하 여 보관 사서함을 사용 하도록 설정 하려면 수도 있습니다. 조직에서 모든 사용자에 대 한 보관 사서함을 사용 하도록 설정 하는 데 사용할 수 있는 PowerShell 명령의 예에 대 한 [자세한 내용](#more-information) 은 섹션을 참조 하십시오. 
    
- 또한 보관 자동 확장 공유 사서함을 지원 합니다. 공유 사서함에 대 한 보관을 사용 하려면 Exchange Online 계획 2 라이선스 또는 Exchange Online 보관 라이선스를 사용 하 여 Exchange Online 계획 1 라이선스가 필요 합니다.
    
- Exchange 관리 센터 또는 보안을 사용할 수 없습니다 &amp; 준수 센터 보관 자동 확장을 사용 하도록 설정 합니다. Exchange Online PowerShell을 사용 해야 합니다. 원격 PowerShell을 사용 하 여 Exchange Online 조직에 연결할 [Connect to Exchange Online PowerShell를](https://go.microsoft.com/fwlink/p/?linkid=396554)참조 하십시오.
    
  
## <a name="enable-auto-expanding-archiving-for-your-entire-organization"></a>전체 조직에 대 한 보관 자동 확장을 사용 하도록 설정

전체 조직에 대 한 보관 자동 확장을 사용 하도록 설정할 수 있습니다. 설정한 후 보관 자동을 확장 하면 사용할 수 있고 기존 사용자 사서함에 대 한 및 만들어지는 새 사용자 사서함에 대 한. 새 사용자 사서함을 만들 때에 새 사용자 사서함에 대 한 자동 확장 하는 보관 기능이 작동할 되므로 사용자의 기본 보관 사서함을 사용 하도록 설정 해야 합니다.
  
1. [원격 PowerShell을 사용하여 Exchange Online에 연결](https://go.microsoft.com/fwlink/p/?linkid=396554)
    
2. 전체 조직에 대 한 보관 자동 확장을 사용 하는 Exchange Online PowerShell에서 다음 명령을 실행 합니다.

    ```
    Set-OrganizationConfig -AutoExpandingArchive
    ```
  
## <a name="enable-auto-expanding-archiving-for-specific-users"></a>특정 사용자에 대 한 보관 자동 확장을 사용 하도록 설정

조직에서 모든 사용자에 대 한 보관 자동 확장을 사용 하는 대신 특정 사용자에 대 한 것만 설정할 수 있습니다. 일부 사용자만 매우 큰 보관 저장소에 대 한 요구가 있을 수 있으므로이 수행할 수 있습니다.
  
때 특정 사용자에 대 한 보관 자동 확장을 사용 하 고에 대 한 사용자의 사서함에 유지 또는 Office 365 보존 정책에 할당 하는 다음 두 구성 변경 됩니다.
  
- 사용자의 기본 보관 사서함에 대 한 저장소 할당량은 (110 g B에 100GB)에서 10 g B 씩 증가 합니다. 보관 경고 할당량은도 (100GB로 90 GB)에서 10 g B 씩 증가 합니다.
    
- 사용자의 기본 사서함의 복구 가능한 항목 폴더에 대 한 저장소 할당량은 (도 110 g B에 100GB)에서 10 g B 씩 증가 합니다. 복구 가능한 항목 경고 보내기 할당량은도 (100GB로 90 GB)에서 10GB으로 증가 합니다. 이러한 변경의 사서함에 보존 또는 Office 365 보존 정책에 할당 하는 경우에 적용 됩니다.
    
이 추가 공간 자동 확장 보관 구축 하기 전에 발생할 수 있는 저장소 문제를 방지 하기 위해 추가 됩니다. Note 해당 추가 저장 공간이 *없는* 이전 섹션에서 설명한 것 처럼 전체 조직에 대 한 보관 자동 확장을 사용 하는 경우 추가 합니다. 
  
1. [원격 PowerShell을 사용하여 Exchange Online에 연결](https://go.microsoft.com/fwlink/p/?linkid=396554)
    
2. 특정 사용자에 대 한 보관 자동 확장을 사용 하는 Exchange Online PowerShell에서 다음 명령을 실행 합니다. 앞에서 설명한 것 처럼 사용자의 보관 사서함 (기본 보관 함)를 사용 하려면 먼저 자동-을 확장 하면 해당 사용자에 대 한 보관 활성화 되어야 합니다.
    
    ```
    Enable-Mailbox <user mailbox> -AutoExpandingArchive
    ```


> [!IMPORTANT]
> Exchange 하이브리드 배포에서 자동 확장 기본 사서함이 있는 온-프레미스 사용자를 특정에 대 한 보관을 사용 하도록 설정 하려면 **Enable-mailbox AutoExpandingArchive** 명령을 사용할 수 없습니다 및 클라우드 기반 보관 사서함은 합니다. 명령을 실행 하 여 **Set-organizationconfig AutoExpandingArchive** Exchange Online에 대 한 보관 자동 확장을 사용 하는 PowerShell 해야하는 Exchange 하이브리드 배포에서 클라우드 기반 보관 사서함에 대 한 보관 자동 확장을 사용 하려면 전체 조직입니다. 사용자의 기본 보관 사서함이 클라우드 기반 모두 하는 경우 해당 특정 사용자에 대 한 보관 자동 확장을 사용 하도록 **Enable-mailbox AutoExpandingArchive** 명령을 사용할 수 있습니다. 
  
## <a name="verify-that-auto-expanding-archiving-is-enabled"></a>보관 자동 확장을 사용할 수 있는지 확인 합니다.

조직에 대 한 보관 자동을 확장 하면가 사용 하도록 설정 되어있는지를 확인 하려면 Exchange Online PowerShell에서 다음 명령을 실행 합니다.

```
Get-OrganizationConfig | FL AutoExpandingArchiveEnabled
```

값이 `True` 는 조직에 대 한 보관 자동 확장을 사용할지를 나타냅니다. 
  
보관 자동을 확장 하면 특정 사용자에 대 한 사용 인지를 확인 하려면 Exchange Online PowerShell에서 다음 명령을 실행 합니다.
  
```
Get-Mailbox <user mailbox> | FL AutoExpandingArchiveEnabled
```
값이 `True` 사용자에 대 한 보관 자동 확장을 사용할지를 나타냅니다. 
  
자동 확장 보관을 활성화 한 후 다음 사항에 주의 유지 합니다.
  
- 조직에 대 한 보관 자동 확장을 사용 하도록 설정 하려면 **Set-organizationconfig AutoExpandingArchive** 명령을 실행 하는 경우에 개별 사서함에서 **Enable-mailbox AutoExpandingArchive** 를 실행할 필요가 없습니다. 해당 조직에 사용자 사서함에서 *AutoExpandingArchiveEnabled* 속성은 바뀌지 않습니다에 대 한 보관 자동 확장을 사용 하도록 설정 하려면 **Set-organizationconfig** cmdlet을 실행 하는 참고 `True`합니다.
    
- 마찬가지로, 보관 자동 확장을 사용 하는 경우 *ArchiveQuota* 및 *ArchiveWarningQuota* 사서함 속성에 대 한 값이 변경 되지 않습니다. 실제로 때 사용자 사서함에 대 한 보관 자동 확장을 사용 하 고 *AutoExpandingArchiveEnabled* 속성이로 설정 된 `True`, 방금 *ArchiveQuota* 및 *ArchiveWarningQuota* 속성은 무시 됩니다. 사용자의 사서함에 대 한 자동 확장 보관이 설정 된 후 이러한 사서함 속성의 예로 다음과 같습니다. 
    
    ![자동 확장 보관을 활성화 한 후 ArchiveQuota 및 ArchiveWarningQuota 속성은 무시 합니다.](media/6a1c1b69-5c4c-4267-aac8-53577667f03e.png)

  
## <a name="more-information"></a>추가 정보

- PowerShell을 사용 하 여 보관 사서함을 사용 하도록 설정 하려면 수도 있습니다. 예 있습니다 명령을 실행할 수는 다음 Exchange 온라인 보관 사서함 이미 설정 되지 않은 모든 사용자에 대 한 보관 사서함을 사용 하도록 설정 하는 PowerShell 합니다.

    ```
    Get-Mailbox -Filter {ArchiveStatus -Eq "None" -AND RecipientTypeDetails -eq "UserMailbox"} | Enable-Mailbox -Archive
    ```

- 자동 확장 특정 사용자 또는 조직에 대 한 보관을 설정한 후 (복구 가능한 항목 폴더 포함)의 보관 사서함에 90 g B에 도달 하면가 자동 확장 보관 보관 사서함 변환 됩니다. 프로 비전 할 추가 저장 공간에 대 한 최대 30 일 걸릴 수 있습니다.
    
- 자동 확장 보관을 설정한 후 해당 해제할 수 없습니다.
    
- 온-프레미스 기본 사서함을 가진 사용자에 대 한 Exchange 하이브리드 배포에서 클라우드 기반 보관 사서함에 대 한 보관 자동 확장 지원 됩니다. 그러나 보관 자동 확장 클라우드 기반 보관 사서함에 대해 설정 된 후 하면 수는 없습니다 오프-보드 온-프레미스 Exchange 조직에 다시 보관 사서함에 해당 합니다.
    
- 사용자가 자신의 보관 사서함에 추가 저장소 영역에 있는 항목에 액세스 하는데 사용할 수 있는 Outlook 클라이언트의 목록, [Office 365의 보관 무제한의 개요 (영문)](unlimited-archiving.md#outlook-requirements-for-accessing-items-in-an-auto-expanded-archive) 에서 "자동 확장 보관 위치에 있는 항목에 액세스할 수 있도록 Outlook의 요구 사항" 섹션을 참조 하십시오. .
    
- 이전에 설명, 사용자의 기본 보관 사서함의 저장소 할당량을 10GB 추가 됩니다 (하 고 복구 가능한 항목 폴더에는 사서함이 하는 경우 대기)으로 **Enable-mailbox AutoExpandingArchive** 명령을 실행 하면 됩니다. 이 자동 확장 된 저장 공간 (에 30 일 분까지 걸릴 수) 구축 될 때까지 추가 저장소를 제공 합니다. 조직에서 모든 사서함에 대 한 보관 자동 확장을 사용 하도록 설정 하려면 **Set-organizationconfig AutoExpandingArchive** 를 실행 하는 경우이 추가 저장 공간 추가 되지 않습니다. 전체 조직에 대 한 보관 자동 확장을 설정 하 고 특정 사용자에 대 한 저장 공간이 10GB 추가 추가 해야하는 해당 사서함에 **Enable-mailbox AutoExpandingArchive** 명령을 실행할 수 있습니다. 자동 확장 보관이 이미 설정 되었는지, 하지만 사서함에 추가할 추가 저장 공간 이라는 오류가 나타나면 note 합니다. 
