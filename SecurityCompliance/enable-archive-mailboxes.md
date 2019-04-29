---
title: 보안 & 준수 센터에서 보관 사서함을 사용 하도록 설정
ms.author: markjjo
author: markjjo
manager: laurawi
ms.audience: Admin
ms.topic: article
f1_keywords:
- ms.o365.cc.ArchivingHelp
ms.service: O365-seccomp
localization_priority: Priority
ms.collection:
- Strat_O365_IP
- M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: 268a109e-7843-405b-bb3d-b9393b2342ce
description: Office 365의 Security & 준수 센터를 사용 하 여 조직의 메시지 보존, eDiscovery 및 보존 요구 사항을 지원 하기 위해 보관 사서함을 사용 하도록 설정할 수 있습니다.
ms.openlocfilehash: f4f02e5107526f2f45b0a46579e0676b791f0dd1
ms.sourcegitcommit: e23b84ef4eee9cccec7205826b71ddfe9aaac2f8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33402926"
---
# <a name="enable-archive-mailboxes-in-the-security--compliance-center"></a>보안 & 준수 센터에서 보관 사서함을 사용 하도록 설정
  
Office 365 (원본 위치 보관이 라고도 함)의 보관은 사용자에 게 사서함 저장소 공간을 추가로 제공 합니다. 보관 사서함을 켜면 사용자가 Microsoft outlook 및 웹용 outlook (이전의 outlook web App)을 사용 하 여 보관 사서함에 메시지를 액세스 하 고 저장할 수 있습니다. 사용자는 기본 사서함과 해당 보관 사서함 간에 메시지를 이동 하거나 복사할 수도 있습니다. 지운 편지함 복구 도구를 사용 하 여 보관 사서함의 복구 가능한 항목 폴더에서 삭제 된 항목을 복구할 수도 있습니다. 
  
> [!TIP]
> Office 365에서는 자동 확장 보관 기능과 무제한의 보관 저장소를 제공 합니다. 자동 확장 보관이 켜져 있는 경우 사용자의 보관 사서함에 있는 초기 저장소 할당량에 도달 하면 Office 365에서 자동으로 저장 공간을 추가 합니다. 즉, 사용자에 게 사서함 저장소 공간이 부족 하지 않으며, 처음에 보관 사서함을 사용 하도록 설정 하 고 조직에 대해 자동 확장 보관을 사용 하도록 설정한 후에는 별도로 관리할 필요가 없습니다. 자세한 내용은 [Office 365 무제한 보관의 개요](unlimited-archiving.md)를 참조하세요. 
  
## <a name="before-you-begin"></a>시작하기 전에

보관 사서함을 사용 하거나 사용 하지 않도록 설정 하려면 Exchange Online의 Mail Recipients 역할을 할당 받아야 합니다. 기본적으로이 역할은 Exchange 관리 센터의 **사용 권한** 페이지에 있는 받는 사람 관리 및 조직 관리 역할 그룹에 할당 됩니다. 보안 & 준수 센터에 **보관** 페이지가 표시 되지 않으면 관리자에 게 필요한 사용 권한을 할당 해 달라고 요청 합니다. 
  
## <a name="enable-an-archive-mailbox"></a>보관 사서함 사용
  
1. [https://protection.office.com](https://protection.office.com)으로 이동합니다.
    
2. 회사 또는 학교 계정을 사용하여 Office 365에 로그인합니다.
    
3. Security & 준수 센터의 왼쪽 창에서 **데이터 거 버 넌 스** \> **보관**함을 클릭 합니다.
    
    **보관** 페이지가 표시 됩니다. **보관 사서함** 열에는 각 사용자에 대해 보관 사서함이 사용 하도록 설정 되었는지 또는 사용 하지 않도록 설정 되어 있는지 여부가 표시 됩니다. 
    
4. 사서함 목록에서 보관 사서함을 사용 하도록 설정 하려는 사용자를 선택 합니다.
    
    ![선택한 사용자의 세부 정보 창에서 사용을 클릭 하 여 보관 사서함을 사용 하도록 설정 합니다.](media/8b53cdec-d5c9-4c28-af11-611f95c37b34.png)
  
5. 선택한 사용자에 대 한 세부 정보 창에서 **사용**을 클릭 합니다. 
    
    보관 사서함을 사용 하도록 설정 하면 사용자 사서함에서 사서함에 할당 된 보관 정책 보다 오래 된 항목이 새 보관 사서함으로 이동 됨을 알리는 경고가 표시 됩니다. Exchange Online 사서함에 할당 된 보존 정책의 일부인 기본 보관 정책은 항목이 사서함으로 배달 되거나 사용자가 만든 날짜 후 2 년 후에 항목을 보관 사서함으로 이동 합니다. 자세한 내용은이 문서의 **추가 정보** 섹션을 참조 하십시오. 
    
6. **예** 를 클릭 하 여 보관 사서함을 사용 하도록 설정 합니다. 
    
    보관 사서함을 만드는 데 몇 분 정도 걸릴 수 있습니다. 이 파일을 만들 때 **보관 사서함: enabled** 가 선택한 사용자에 대 한 세부 정보 창에 표시 됩니다. 세부 정보 창에서 정보를 업데이트 하려면](media/O365-MDM-Policy-RefreshIcon.gif) 새로 고침 아이콘 **새로 고침** ![을 클릭 해야 할 수 있습니다. 
    
> [!TIP]
> 또한 사용 하지 않도록 설정 된 보관 사서함을 사용 하 여 여러 사용자를 선택 하 여 보관 사서함을 대량으로 사용 하도록 설정할 수 있습니다 (Shift 또는 Ctrl 키 사용). 여러 사서함을 선택한 후 세부 정보 창에서 **사용** 을 클릭 합니다. 
  
## <a name="disable-an-archive-mailbox"></a>보관 사서함 사용 안 함
  
또한 Security & 준수 센터의 **보관** 페이지를 사용 하 여 사용자의 보관 사서함을 사용 하지 않도록 설정할 수 있습니다. 보관 사서함을 사용 하지 않도록 설정한 후에는 사용 하지 않도록 설정 하 고 30 일 이내에 사용자의 기본 사서함에 다시 연결할 수 있습니다. 이 경우 보관 사서함의 원래 내용이 복원됩니다. 30일이 지나면 원래 보관 사서함의 내용이 영구적으로 삭제되어 복구할 수 없습니다. 따라서 비활성화한 지 30일 넘게 지난 뒤 보관 사서함을 다시 사용하도록 설정하면 새 보관 사서함이 만들어집니다. 
  
사용자 사서함에 할당 된 기본 보관 정책이 항목을 배달 한 날짜 후 2 년 후에 항목을 보관 사서함으로 이동 합니다. 사용자의 보관 사서함을 사용 하지 않도록 설정 하면 사서함 항목에 대 한 아무 작업도 수행 되지 않으며 사용자의 기본 사서함에 남아 있게 됩니다.
  
보관 사서함을 사용 하지 않도록 설정 하려면
  
1. [https://protection.office.com](https://protection.office.com)으로 이동합니다.
    
2. 회사 또는 학교 계정을 사용하여 Office 365에 로그인합니다.
    
3. Security & 준수 센터의 왼쪽 창에서 **데이터 거 버 넌 스** \> **보관**함을 클릭 합니다.
    
    **보관** 페이지가 표시 됩니다. **보관 사서함** 열에는 각 사용자에 대해 보관 사서함이 사용 하도록 설정 되었는지 또는 사용 하지 않도록 설정 되어 있는지 여부가 표시 됩니다. 
    
4. 사서함 목록에서 보관 사서함을 사용 하지 않도록 설정 하려는 사용자를 선택 합니다.
    
5. 세부 정보 창에서 **사용 안 함을**클릭 합니다. 
    
    30 일 동안 보관 사서함을 다시 사용 하도록 설정 하 고 30 일 후에 보관 함의 모든 정보가 영구적으로 삭제 됨을 알리는 경고 메시지가 표시 됩니다. 
    
6. **예** 를 클릭 하 여 보관 사서함을 사용 하지 않도록 설정 합니다. 
    
    보관 사서함을 사용 하지 않도록 설정 하는 데 몇 분 정도 걸릴 수 있습니다. 사용 하지 않도록 설정 된 경우 **보관 사서함: 사용 안 함** 이 선택한 사용자의 세부 정보 창에 표시 됩니다. 세부 정보 창에서 정보를 업데이트 하려면](media/O365-MDM-Policy-RefreshIcon.gif) 새로 고침 아이콘 **새로 고침** ![을 클릭 해야 할 수 있습니다. 
    
> [!TIP]
> 보관 사서함을 사용 하도록 설정한 여러 사용자를 선택 하 여 보관 사서함을 대량으로 사용 하지 않도록 설정할 수도 있습니다 (Shift 또는 Ctrl 키 사용). 여러 사서함을 선택한 후 세부 정보 창에서 **사용 안 함을** 클릭 합니다. 
  
## <a name="use-exchange-online-powershell-to-enable-or-disable-archive-mailboxes"></a>Exchange Online PowerShell을 사용 하 여 보관 사서함을 사용 하거나 사용 하지 않도록 설정

또한 Exchange Online PowerShell을 사용 하 여 보관 사서함을 사용 하도록 설정할 수 있습니다. PowerShell을 사용 하는 주요 이유는 조직의 모든 사용자에 대해 보관 사서함을 빠르게 사용 하도록 설정할 수 있다는 것입니다.

첫 번째 단계는 Exchange Online PowerShell에 연결 하는 것입니다. 자세한 내용은 [Exchange Online PowerShell에 연결을](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell)참조 하십시오.

Exchange Online에 연결 하 고 나면 다음 섹션의 명령을 실행 하 여 보관 사서함을 사용 하거나 사용 하지 않도록 설정할 수 있습니다.

### <a name="enable-archive-mailboxes"></a>보관 사서함 사용

다음 명령을 실행 하 여 단일 사용자에 대해 보관 사서함을 사용 하도록 설정 합니다.
    
  ```
  Enable-Mailbox -Identity <username> -Archive
  ```

다음 명령을 실행 하 여 조직의 모든 사용자 (보관 사서함 현재 사용 하지 않도록 설정 되어 있지 않음)에서 보관 사서함을 사용 하도록 설정 합니다.
    
  ```
  Get-Mailbox -Filter {ArchiveStatus -Eq "None" -AND RecipientTypeDetails -eq "UserMailbox"} | Enable-Mailbox -Archive
  ```
  
### <a name="disable-archive-mailboxes"></a>보관 사서함 사용 안 함

다음 명령을 실행 하 여 단일 사용자에 대해 보관 사서함을 사용 하지 않도록 설정 합니다.
    
  ```
  Disable-Mailbox -Identity <username> -Archive
  ```

다음 명령을 실행 하 여 조직의 모든 사용자 (보관 사서함 현재 사용 가능)에 대 한 보관 사서함을 사용 하지 않도록 설정 합니다.
    
  ```
  Get-Mailbox -Filter {ArchiveStatus -Eq "Active" -AND RecipientTypeDetails -eq "UserMailbox"} | Disable-Mailbox -Archive
  ```

## <a name="more-information"></a>추가 정보
  
- 보관 사서함을 사용 하도록 설정 하면 사용자가 보관 사서함에 메시지를 저장할 수 있습니다. 사용자는 Microsoft outlook 및 웹용 Outlook을 사용 하 여 보관 사서함에 액세스할 수 있습니다. 이러한 클라이언트 응용 프로그램 중 하나를 사용 하면 사용자가 자신의 보관 사서함에서 메시지를 보고 기본 사서함과 해당 보관 사서함 간에 메시지를 이동 하거나 복사할 수 있습니다. 또한 사용자는 지운 편지함 복구 도구를 사용 하 여 보관 사서함의 복구 가능한 항목 폴더에서 삭제 된 항목을 복구할 수 있습니다.

   원본 위치 보관을 지 원하는 outlook 라이선스 목록은 [Exchange 기능에 대 한 outlook 라이선스 요구 사항을](https://support.office.com/article/outlook-license-requirements-for-exchange-features-46b6b7c5-c3ca-43e5-8424-1e2807917c99)참조 하세요.

- 보관 사서함을 통해 조직의 보존, eDiscovery 및 보존 요구 사항을 충족 하는 사용자를 지원할 수 있습니다. 예를 들어 조직의 Exchange 보존 정책을 사용 하 여 사서함 콘텐츠를 사용자의 보관 사서함으로 이동할 수 있습니다. 보안 & 준수 센터의 콘텐츠 검색 도구를 사용 하 여 사용자의 사서함에서 특정 콘텐츠를 검색 하는 경우 사용자의 보관 사서함도 검색 됩니다. 또한 소송 보존을 수행 하거나 사용자 사서함에 Office 365 유지 정책을 적용 하는 경우 보관 사서함의 항목도 보존 됩니다.
  
- 보관 사서함을 사용 하도록 설정한 후에는 조직에서 모든 사서함에 자동으로 할당 되는 기본 Exchange 보존 정책 (메시징 레코드 관리 또는 mrm 정책)을 활용할 수 있습니다. 보관 사서함을 사용 하도록 설정 하면 기본 Exchange 보존 정책이 자동으로 다음 작업을 수행 합니다. 
  
    - 사용자의 기본 사서함에서 보관 사서함으로 2년 이상 된 항목을 이동합니다. 
    
    - 사용자의 기본 사서함에 있는 복구 가능한 항목 폴더에서 보관 사서함의 복구 가능한 항목 폴더로 14일 이상 된 항목을 이동합니다.
    
- 보관 사서함 및 Exchange 보존 정책에 대 한 자세한 내용은 다음 항목을 참조 하십시오.
    
  - [보존 태그 및 보존 정책](https://go.microsoft.com/fwlink/?LinkId=404424)
    
  - [Exchange Online의 기본 보존 정책](https://go.microsoft.com/fwlink/?linkid=839418)
    
  - [Office 365 조 직의 사서함에 대 한 보관 및 삭제 정책 설정](set-up-an-archive-and-deletion-policy-for-mailboxes.md)
