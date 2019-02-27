---
title: Office 365 감사 로그 검색 켜기 또는 끄기
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 10/18/2017
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- Strat_O365_IP
- M365-security-compliance
search.appverid:
- MOE150
- MED150
- MET150
ms.assetid: e893b19a-660c-41f2-9074-d3631c95a014
description: Office 365 보안 &amp; 및 준수 센터에서 감사 로그 검색 기능을 설정할 수 있습니다. 생각이 변경 되 면 언제 든 지 설정을 해제할 수 있습니다. 감사 로그 검색이 해제 되 면 관리자가 조직의 사용자 및 관리자 활동에 대 한 Office 365 감사 로그를 검색할 수 없습니다.
ms.openlocfilehash: 17b98cce26054d073006fa78c55fe418b5f327d8
ms.sourcegitcommit: baf23be44f1ed5abbf84f140b5ffa64fce605478
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/26/2019
ms.locfileid: "30295461"
---
# <a name="turn-office-365-audit-log-search-on-or-off"></a>Office 365 감사 로그 검색 켜기 또는 끄기

사용자 (또는 다른 관리자)가 감사 로깅을 켜야 Office 365 감사 로그 검색을 시작할 수 있습니다. Office 365 보안 &amp; 및 준수 센터에서 감사 로그 검색이 설정 된 경우 조직의 사용자 및 관리자 활동이 감사 로그에 기록 되 고 90 일 동안 보존 됩니다. 그러나 조직에서 감사 로그 데이터를 기록 하 고 보존 하지 않을 수도 있습니다. 또는 타사의 siem (보안 정보 및 이벤트 관리) 응용 프로그램을 사용 하 여 감사 데이터에 액세스할 수 있습니다. 이러한 경우 전역 관리자가 Office 365에서 감사 로그 검색을 해제할 수 있습니다.
  
## <a name="before-you-begin"></a>시작하기 전에

- Office 365 조직에서 감사 로그 검색을 설정 하거나 해제 하려면 Exchange Online에서 감사 로그 역할을 할당 받아야 합니다. 기본적으로이 역할은 Exchange 관리 센터의 **사용 권한** 페이지에 있는 준수 관리 및 조직 관리 역할 그룹에 할당 됩니다. Office 365의 전역 관리자는 Exchange Online의 조직 관리 역할 그룹의 구성원입니다. 
    
    > [!IMPORTANT]
    > 감사 로그 검색을 설정 또는 해제 하려면 사용자에 게 Exchange Online의 사용 권한을 할당 해야 합니다. 보안 &amp; 및 준수 센터의 **사용 권한** 페이지에서 사용자에 게 감사 로그 역할을 할당 하면 감사 로그 검색을 설정 하거나 해제할 수 없습니다. 이는 기본 cmdlet이 Exchange Online cmdlet 이기 때문입니다. 
  
- office 365에서 감사 로그 검색을 해제 해도 office 365 관리 작업 API를 사용 하 여 조직의 감사 데이터에 액세스할 수 있습니다. 이 문서에서 설명 하는 단계에 따라 감사 로그 검색을 해제 하면 보안 &amp; 및 준수 센터를 사용 하 여 감사 로그를 검색 하거나 Exchange Online에서 **search-unifiedauditlog** cmdlet을 실행할 때 결과가 반환 되지 않습니다. 슬래시. 그러나 Office 365 관리 활동 API를 통해 조직의 감사 데이터에 액세스 하도록 모든 응용 프로그램에 권한을 부여한 경우 해당 응용 프로그램은 계속 작동 합니다. 
    
- office 365 감사 로그를 검색 하는 방법에 대 한 단계별 지침은 [office 365 보안 &amp; 및 준수 센터에서 감사 로그 검색](search-the-audit-log-in-security-and-compliance.md)을 참조 하십시오.
    
## <a name="turn-on-audit-log-search"></a>감사 로그 검색 켜기

보안 &amp; 및 준수 센터 또는 PowerShell을 사용 하 여 Office 365에서 감사 로그 검색을 설정할 수 있습니다. 감사 로그 검색을 설정한 후에는 여러 시간이 걸릴 수 있습니다. 감사 로그 검색을 설정 하려면 Exchange Online에서 감사 로그 역할을 할당 받아야 합니다.
  
### <a name="use-the-security-amp-compliance-center-to-turn-on-audit-log-search"></a>보안 &amp; 및 준수 센터를 사용 하 여 감사 로그 검색 설정

1. 보안 &amp; 및 준수 센터에서 **검색 &amp; 조사** \> **감사 로그 검색**으로 이동 합니다.
    
2. **사용자 및 관리 활동 기록을 시작**합니다 .를 클릭 합니다.
    
    ![기록 시작 사용자 및 관리자 활동을 클릭하여 감사 기능을 설정](media/39a9d35f-88d0-4bbe-a962-0be2f838e2bf.png)
  
    조직의 사용자 및 관리자 활동이 Office 365 감사 로그에 기록 되 고 보고서에서 볼 수 있음을 알리는 대화 상자가 표시 됩니다. 
    
3. **켜기** 를 클릭합니다.
    
    감사 로그를 준비 중 이며 준비 완료 후 몇 시간 내에 검색을 실행할 수 있음을 알리는 메시지가 표시 됩니다.
    
### <a name="use-powershell-to-turn-on-audit-log-search"></a>PowerShell을 사용 하 여 감사 로그 검색 설정

1. [원격 PowerShell을 사용하여 Exchange Online에 연결](https://go.microsoft.com/fwlink/p/?LinkID=396554)
    
2. 다음 PowerShell 명령을 실행 하 여 Office 365에서 감사 로그 검색을 사용 하도록 설정 합니다.
    
    ```
    Set-AdminAuditLogConfig -UnifiedAuditLogIngestionEnabled $true
    ```

    변경 내용이 적용 되는 데 최대 60 분이 걸릴 수 있다는 메시지가 표시 됩니다.
  
## <a name="turn-off-audit-log-search"></a>감사 로그 검색 해제

감사 로그 검색을 해제 하려면 Exchange Online 조직에 연결 된 원격 PowerShell을 사용 해야 합니다. 감사 로그 검색을 설정 하는 것과 마찬가지로 감사 로그 검색을 해제 하려면 Exchange Online에서 감사 로그 역할을 할당 받아야 합니다.
  
1. [원격 PowerShell을 사용하여 Exchange Online에 연결](https://go.microsoft.com/fwlink/p/?LinkID=396554)
    
2. 다음 PowerShell 명령을 실행 하 여 Office 365에서 감사 로그 검색을 해제 합니다.
    
    ```
    Set-AdminAuditLogConfig -UnifiedAuditLogIngestionEnabled $false
    ```

3. 잠시 후에 감사 로그 검색이 해제 되어 있는지 확인 합니다 (사용 하지 않도록 설정 됨). 이 작업을 수행 하는 방법에는 두 가지가 있습니다.
    
    - PowerShell에서 다음 명령을 실행 합니다.

        ```
        Get-AdminAuditLogConfig | FL UnifiedAuditLogIngestionEnabled
        ```

        UnifiedAuditLogIngestionEnabled 속성의 `False` 값은 __ 감사 로그 검색이 해제 됨을 나타냅니다. 
    
    - 보안 &amp; 및 준수 센터에서 ** &amp; 검색 조사** \> **감사 로그 검색**으로 이동한 다음 **검색**을 클릭 합니다.
    
      감사 로그 검색이 설정 되지 않았다는 메시지가 표시 됩니다. 
    
      ![감사가 해제 된 경우 메시지가 dispayed](media/dca53da6-1cbe-4fa3-9860-f0d674de9538.png)
