---
title: 사용자에게 Office 365 보안 및 준수 센터에 대한 액세스 권한 부여
ms.author: chrisda
author: chrisda
manager: dansimp
ms.date: ''
audience: Admin
ms.topic: article
f1_keywords:
- ms.o365.cc.PermissionsHelp
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MOE150
- MET150
ms.assetid: 2cfce2c8-20c5-47f9-afc4-24b059c1bd76
description: 사용자는 보안 또는 규정 준수 기능을 관리 하기 전에 Office 365 보안 & 준수 센터에서 사용 권한을 할당 받아야 합니다.
ms.openlocfilehash: f11114ede37269f9b89c4d2b34c69f2d6db8a3f7
ms.sourcegitcommit: 044003455eb36071806c9f008ac631d54c64dde6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/24/2019
ms.locfileid: "35199743"
---
# <a name="give-users-access-to-the-office-365-security--compliance-center"></a>사용자에게 Office 365 보안 및 준수 센터에 대한 액세스 권한 부여

사용자는 보안 또는 규정 준수 기능을 관리 하기 전에 Office 365 보안 & 준수 센터에서 사용 권한을 할당 받아야 합니다. 보안 & 준수 센터에서 Office 365 전역 관리자 또는 OrganizationManagement 역할 그룹의 구성원으로 사용자에 게 이러한 사용 권한을 부여할 수 있습니다. 사용자는 액세스 권한을 부여 받은 보안 또는 규정 준수 기능만 관리할 수 있습니다. 
  
보안 & 준수 센터에서 사용자에 게 부여할 수 있는 다양 한 사용 권한에 대 한 자세한 내용은 [Office 365 보안 & 준수 센터의 사용 권한](permissions-in-the-security-and-compliance-center.md)를 참조 하세요.
  
## <a name="what-do-you-need-to-know-before-you-begin"></a>시작하기 전에 알아야 할 내용

- 이 문서의 단계를 완료 하려면 Office 365 전역 관리자 이거나 보안 & 준수 센터에서 OrganizationManagement 역할 그룹의 구성원 이어야 합니다.

- 보안 & 준수 센터의 역할 그룹은 Exchange Online의 역할 그룹과 유사한 이름을 사용할 수 있지만 동일 하지는 않습니다.

- 역할 그룹 구성원 자격은 Exchange Online과 보안 & 준수 센터 간에 공유 되지 않습니다.

- (AOBO) 권한이 있는 DAP (위임 된 액세스 권한) 사용 권한을 사용 하는 경우에는 보안 & 준수 센터에 액세스할 수 없습니다.

## <a name="use-the-office-365-admin-center-to-give-another-user-access-to-the-security--compliance-center"></a>Office 365 관리 센터를 사용 하 여 다른 사용자에 게 보안 & 준수 센터에 대 한 액세스 권한 부여

1. [Office 365에 로그인 하 고 관리 센터로 이동](https://go.microsoft.com/fwlink/p/?LinkId=525275)합니다.

2. Office 365 관리 센터에서 **관리 센터** 를 열고 **보안 & 준수**를 클릭 합니다.

3. 보안 & 준수 센터에서 **사용 권한**으로 이동 합니다.

4. 목록에서 사용자를 추가 하려는 역할 그룹을 선택 하 고 편집 아이콘](media/O365-MDM-CreatePolicy-EditIcon.gif) **편집** ![을 클릭 합니다.

5. 역할 그룹의 속성 페이지 **구성원**아래에 있는 추가 아이콘 ****![](media/ITPro-EAC-AddIcon.gif) 추가를 클릭 하 고 추가 하려는 사용자의 이름을 선택 합니다.

6. 역할 그룹에 추가 하려는 모든 사용자를 선택 했으면 **추가\> ** 를 클릭 한 다음 **확인**을 클릭 합니다.

7. **저장**을 클릭하여 역할 그룹에 대한 변경 내용을 저장합니다.

### <a name="how-do-you-know-this-worked"></a>작동 여부는 어떻게 확인합니까?

1. 보안 & 준수 센터에서 **사용 권한**으로 이동 합니다.

2. 목록에서 구성원을 볼 역할 그룹을 선택 합니다.

3. 역할 그룹 세부 정보의 오른쪽에서 역할 그룹의 구성원을 볼 수 있습니다.

## <a name="use-powershell-to-give-another-user-access-to-the-security--compliance-center"></a>PowerShell을 사용 하 여 다른 사용자에 게 보안 & 준수 센터에 대 한 액세스 권한 부여

1. [Office 365 보안 & 준수 센터 PowerShell에 연결](https://docs.microsoft.com/en-us/powershell/exchange/office-365-scc/connect-to-scc-powershell/connect-to-scc-powershell?view=exchange-ps)합니다.

2. 다음 예와 같이 **Add-RoleGroupMember** 명령을 사용하여 사용자를 조직 관리 역할에 추가합니다.

   ```
   Add-RoleGroupMember -Identity "OrganizationManagement" -Member MatildaS
   ```

   **매개 변수**:
  
   - _Identity_ 는 구성원을 추가할 역할 그룹입니다.

   - _구성원_ 은 역할 그룹에 추가할 사서함, USG (유니버설 보안 그룹) 또는 컴퓨터입니다. 구성원은 한 번에 하나만 지정할 수 있습니다.

구문 및 매개 변수에 대 한 자세한 내용은 [추가-RoleGroupMember](https://go.microsoft.com/fwlink/p/?LinkId=510859)를 참조 하십시오.
  
### <a name="how-do-you-know-this-worked"></a>작동 여부는 어떻게 확인하나요?

사용자에 게 보안 & 준수 센터에 대 한 액세스 권한이 있는지 확인 하려면 다음 예제와 같이 **Get-RoleGroupMember** cmdlet을 사용 하 여 조직 관리 역할 그룹의 구성원을 확인 합니다.
  
```
Get-RoleGroupMember -Identity "OrganizationManagement"
```

구문 및 매개 변수에 대 한 자세한 내용은 [Get-RoleGroupMember](https://go.microsoft.com/fwlink/p/?LinkId=510860)를 참조 하십시오.
