---
title: Office 365 보안에서 보관 사서함 사용 &amp; 준수 센터
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: article
f1_keywords:
- ms.o365.cc.ArchivingHelp
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MOE150
- MET150
ms.assetid: 268a109e-7843-405b-bb3d-b9393b2342ce
description: Office 365 보안을 사용 하 여 &amp; 준수 센터 조직의 메시지 보존, eDiscovery, 지원 및 유지 요구 사항에 대 한 보관 사서함을 사용 하도록 설정 합니다.
ms.openlocfilehash: 1c290cf19b396221dac702efd1395911e8a51631
ms.sourcegitcommit: 7e2a0185cadea7f3a6afc5ddc445eac2e1ce22eb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/11/2019
ms.locfileid: "28327100"
---
# <a name="enable-archive-mailboxes-in-the-office-365-security-amp-compliance-center"></a>Office 365 보안에서 보관 사서함 사용 &amp; 준수 센터
  
(내부 보관이 라고도 함)는 Office 365의 보관 추가 사서함 저장 공간을 사용 하는 사용자를 제공 합니다. 보관 사서함에 대 한 정보를 설정한 후 사용자가 액세스 하 고 Microsoft Outlook을 사용 하 여 보관 사서함에 메시지를 저장할 수 및 Outlook Web app. 사용자를 이동 하거나 기본 사서함 및 보관 사서함 간 메시지 복사 수도 있습니다. 또한 지운 편지함 복구 도구를 사용 하 여 보관 사서함의 복구 가능한 항목 폴더에서 삭제 된 항목을 복구할 수 있습니다. 
  
> [!TIP]
> Office 365의 보관 저장소 자동 확장 보관 기능 무제한 금액을 제공합니다. 설정 보관 자동 확장 하 고 사용자의 보관 사서함의 초기 저장소 할당량에 도달 하면 다음을 Office 365 추가 저장 공간을 자동으로 추가 합니다. 사용자가 사서함 저장 공간 부족 실행 되지 않음 및 아무것도 하 고 나면 처음 관리 할 필요가 있는지 여부를이 나타내는 보관 사서함을 사용 하도록 설정 하 고 자동 확장 하면 조직에 대 한 보관 설정 합니다. 자세한 내용은 [Office 365 무제한 보관의 개요](unlimited-archiving.md)를 참조 하십시오. 
  
## <a name="before-you-begin"></a>시작하기 전에

역할을 할당 편지 병합 받는 사람 Exchange Online을 사용 하도록 설정 하거나 보관 사서함을 사용 하지 않도록 설정 해야 합니다. 기본적으로이 역할은 Exchange 관리 센터에서 **사용 권한** 페이지에서 받는 사람 관리 및 조직 관리 역할 그룹에 할당 됩니다. 보안에서 **보관** 페이지를 보이지 않으면 하는 경우 &amp; 준수 센터 필요한 사용 권한을 할당 하려면 관리자에 게 문의 합니다. 
  
## <a name="enable-an-archive-mailbox"></a>보관 사서함 사용
  
1. [https://protection.office.com](https://protection.office.com)으로 이동합니다.
    
2. 회사 또는 학교 계정을 사용하여 Office 365에 로그인합니다.
    
3. 보안의 왼쪽된 창에서 &amp; 준수 센터 **데이터 거 버 넌 스** 를 클릭 \> **보관**합니다.
    
    **보관** 페이지가 표시됩니다. **보관 사서함** 열은 각 사용자의 보관 사서함이 사용하도록 설정되었는지 여부를 나타냅니다. 
    
4. 사서함 목록에서 보관 사서함을 사용하도록 설정할 사용자를 선택합니다.
    
    ![보관 사서함을 사용 하도록 설정 하려면 선택한 사용자의 세부 정보 창에서 사용을 클릭 합니다.](media/8b53cdec-d5c9-4c28-af11-611f95c37b34.png)
  
5. 선택한 사용자에 대 한 세부 정보 창에서 **사용**을 클릭 합니다. 
    
    경고 메시지가 보관 사서함을 사용 하도록 설정 하는 경우 사용자의 사서함에서 사서함에 할당 된 보관 정책 보다 오래 된 항목은 새 보관 사서함으로 이동할 수 없다는 표시 됩니다. Exchange Online 사서함에 할당 된 보존 정책의 일부인 기본 보관 정책을 이동 하는 항목 보관 사서함에는 항목이 사서함으로 배달 되거나 사용자가 만든 날짜 로부터 2 년입니다. 자세한 내용은이 문서의 **추가 정보** 섹션을 참조 하십시오. 
    
6. **예**를 클릭하여 보관 사서함을 사용하도록 설정합니다. 
    
    보관 사서함을 만들 수는 몇 시간이 걸릴 수 있습니다. 만들 때 **보관 사서함: 활성화** 선택한 사용자에 대 한 세부 정보 창에 표시 됩니다. **새로 고침** 을 클릭 해야할 ![새로고침 아이콘](media/O365-MDM-Policy-RefreshIcon.gif) 세부 정보 창에 대 한 정보를 업데이트 합니다. 
    
> [!TIP]
> Shift 또는 Ctrl 키를 사용해 여러 사서함을 선택하여 보관함을 대량으로 사용하도록 설정할 수도 있습니다. 여러 사서함을 선택한 후 세부 정보 창에서 기타 옵션을 클릭합니다. 그런 후에 보관함에서 **사용**을 클릭합니다.  
  
## <a name="disable-an-archive-mailbox"></a>보관 사서함 사용 안 함
  
보안에서 **보관** 페이지를 사용할 수도 있습니다 &amp; 준수 센터 사용자의 보관 사서함을 사용 하지 않도록 설정 합니다. 보관 사서함을 해제 한 후 다시 연결할 수 있습니다 해당 사용자의 기본 사서함에 사용 하지 못하도록 30 일 이내입니다. 이 경우 보관 사서함의 원래 내용은 복원 됩니다. 30 일 후 원래 보관 사서함의 내용을 영구적으로 삭제 하 고 복구할 수 없습니다. 따라서 보관 30 일 보다 것을 비활성화 한 후 다시 사용, 하는 경우 새 보관 사서함이 만들어집니다. 
  
메모는 기본 보관 정책에 할당 된 사용자의 사서함 보관 사서함으로 이동 항목 날짜 후 2 년 항목이 배달 됩니다. 사용자의 보관 사서함 사용 하지 않는 경우 사서함 항목에 대해 아무 작업도 수행 되지 것입니다 하 고 사용자의 기본 사서함에 유지 됩니다.
  
보관 사서함을 사용 하지 않도록 설정 합니다.
  
1. [https://protection.office.com](https://protection.office.com)으로 이동합니다.
    
2. 회사 또는 학교 계정을 사용하여 Office 365에 로그인합니다.
    
3. 보안의 왼쪽된 창에서 &amp; 준수 센터 **데이터 거 버 넌 스** 를 클릭 \> **보관**합니다.
    
    **보관** 페이지가 표시됩니다. **보관 사서함** 열은 각 사용자의 보관 사서함이 사용하도록 설정되었는지 여부를 나타냅니다. 
    
4. 사서함 목록에서 보관 사서함을 사용하지 않도록 설정할 사용자를 선택합니다.
    
5. 세부 정보 창에서 **사용 안 함**을 클릭합니다.  
    
    경고 메시지가 없다는 30 일 보관 사서함을 다시 사용 하도록 설정 해야 하 고 30 일 후 보관 사서함에 정보를 모두 삭제 됨을 영구적으로 표시 됩니다. 
    
6. **예**를 클릭하여 보관 사서함을 사용하지 않도록 설정합니다. 
    
    보관 사서함 사용 하지 않으려면 잠시 걸릴 수 있습니다. 비활성화 되 면 **보관 사서함: 비활성화** 선택한 사용자에 대 한 세부 정보 창에 표시 됩니다. **새로 고침** 을 클릭 해야할 ![새로고침 아이콘](media/O365-MDM-Policy-RefreshIcon.gif) 세부 정보 창에 대 한 정보를 업데이트 합니다. 
    
> [!TIP]
> Shift 또는 Ctrl 키를 사용해 보관 사서함이 사용하도록 설정된 여러 사용자를 선택하여 보관 사서함을 사용하지 않도록 일괄 설정할 수도 있습니다. 여러 사서함을 선택한 후 세부 정보 창에서 **사용 안 함**을 클릭합니다.  
  
## <a name="use-exchange-online-powershell-to-enable-or-disable-archive-mailboxes"></a>Exchange Online PowerShell을 사용 하 여 보관 사서함을 사용 하지 않도록 설정 하거나 사용

보관 사서함을 사용 하도록 설정 하려면 Exchange Online PowerShell를 사용할 수도 있습니다. PowerShell을 사용 하는 주된 이유는 조직에서 모든 사용자에 대 한 보관 사서함을 빠르게 설정할 수 있습니다.

첫번째 단계에서는 Exchange Online PowerShell에 연결 하는 것입니다. 자세한 내용은 [Connect to Exchange Online PowerShell를](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell)참조 하십시오.

Exchange Online에 연결 된 후 사용 하도록 설정 하거나 보관 사서함을 사용 하지 않도록 설정 하려면 다음 섹션에서 명령을 실행할 수 있습니다.

### <a name="enable-archive-mailboxes"></a>보관 사서함 사용

단일 사용자에 대 한 보관 사서함을 사용 하도록 설정 하려면 다음 명령을 실행 합니다.
    
  ```
  Enable-Mailbox -Identity <username> -Archive
  ```

(보관 사서함을 현재 사용할 수 없습니다) 조직에서 모든 사용자에 대 한 보관 사서함을 사용 하도록 설정 하려면 다음 명령을 실행 합니다.
    
  ```
  Get-Mailbox -Filter {ArchiveStatus -Eq "None" -AND RecipientTypeDetails -eq "UserMailbox"} | Enable-Mailbox -Archive
  ```
  
### <a name="disable-archive-mailboxes"></a>보관 사서함을 사용하지 않도록 설정

단일 사용자에 대 한 보관 사서함을 사용 하지 않도록 설정 하려면 다음 명령을 실행 합니다.
    
  ```
  Disable-Mailbox -Identity <username> -Archive
  ```

(보관 사서함 사용 중인) 조직에서 모든 사용자에 대 한 보관 사서함을 사용 하지 않도록 설정 하려면 다음 명령을 실행 합니다.
    
  ```
  Get-Mailbox -Filter {ArchiveStatus -Eq "Active" -AND RecipientTypeDetails -eq "UserMailbox"} | Disable-Mailbox -Archive
  ```

## <a name="more-information"></a>추가 정보
  
- 보관 사서함 사용자와 함께 조직의 보존, eDiscovery를 충족 하기 위해 도움말과 요구를 유지 합니다. 예, 사용자의 보관 사서함으로 사서함 콘텐츠를 이동 하려면 조직의 Exchange 보존 정책을 사용할 수 있습니다. 보안에서 콘텐츠 검색 도구를 사용 하면 &amp; 특정 콘텐츠를 사용자의 보관 사서함에 대 한 사용자의 사서함을 검색 하려면 준수 센터는 검색할 수도 있습니다. 및 보관 사서함에 있는 항목의 보존도 소송 보존를 배치 하거나 사용자의 사서함에 Office 365 보존 정책을 적용 합니다.
  
- 보관 사서함 사용 하는 경우 사용자가 자신의 보관 사서함에 메시지를 저장할 수 있습니다. 사용자가 사서함에 액세스할 수 보관 Microsoft Outlook 및 Outlook Web app.를 사용 하 여 사용 하 여 이러한 클라이언트 응용 프로그램 중 하나, 사용자가 자신의 보관 사서함의 메시지를 보려면 및 이동 하거나, 기본 사서함 및 보관 사서함 간의 메시지를 복사할 수 있습니다. 사용자가 자신의 보관 사서함의 복구 가능한 항목 폴더에서 삭제 된 항목 지운 편지함 복구 도구를 사용 하 여 복구도 수 있습니다. 
  
- 보관 사서함 사용 하도록 설정 된 후 조직 활용할 수 기본 Exchange 보존 정책 (메시징 레코드 관리 또는 MRM 정책 라고도 함)에 자동으로 모든 사서함에 할당 됩니다. 보관 사서함 사용 하는 경우 기본 Exchange 보존 정책은 자동으로 다음를 수행 합니다. 
  
    - 사용자의 기본 사서함에서 보관 사서함으로 2년 이상 된 항목을 이동합니다. 
    
    - 사용자의 기본 사서함에 있는 복구 가능한 항목 폴더에서 보관 사서함의 복구 가능한 항목 폴더로 14일 이상 된 항목을 이동합니다.
    
- 보관 사서함 및 Exchange 보존 정책에 대 한 자세한 내용은 다음을 참조 합니다.
  
    
  - [보존 태그 및 보존 정책](https://go.microsoft.com/fwlink/?LinkId=404424)
    
  - [기본 보존 정책 in Exchange Online](https://go.microsoft.com/fwlink/?linkid=839418)
    
  - [Office 365 조직 내의 사서함에에서는 보관 및 삭제 정책 설정](set-up-an-archive-and-deletion-policy-for-mailboxes.md)
