---
title: EOP에서 그룹 관리
ms.author: tracyp
author: MSFTTracyP
manager: dansimp
ms.date: 11/17/2014
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.assetid: 212e68ac-6330-47e9-a169-6cf5e2f21e13
description: EOP(Exchange Online Protection)를 사용하여 Exchange 조직에 메일 사용 가능 그룹을 만들 수 있습니다. 또한 구성원 자격, 전자 메일 주소 및 그룹의 기타 측면을 지정하는 그룹 속성을 정의하거나 업데이트할 수도 있습니다.
ms.openlocfilehash: 9ce501c5d51561a7be86963ae98b62046995e46f
ms.sourcegitcommit: 361aab46b1bb295ed2dcc1a417ac81f699b8ff78
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/30/2019
ms.locfileid: "36676738"
---
# <a name="manage-groups-in-eop"></a>EOP에서 그룹 관리

 EOP(Exchange Online Protection)를 사용하여 Exchange 조직에 메일 사용 가능 그룹을 만들 수 있습니다. 또한 구성원 자격, 전자 메일 주소 및 그룹의 기타 측면을 지정하는 그룹 속성을 정의하거나 업데이트할 수도 있습니다. 필요에 따라 메일 그룹 및 보안 그룹을 만들 수 있습니다. 이러한 그룹은 EAC(Exchange 관리 센터)를 사용하거나 원격 Windows PowerShell을 통해 만들 수 있습니다.
  
## <a name="types-of-mail-enabled-groups"></a>메일 사용 가능 그룹의 유형

Exchange 조직에 대해 다음과 같은 두 가지 유형의 그룹을 만들 수 있습니다.
  
- 메일 그룹은 일반적인 관심 영역과 관련 하 여 전자 메일을 받거나 보내야 하는 팀 또는 기타 특별 그룹 같은 전자 메일 사용자의 모음입니다. 메일 그룹은 전자 메일 메시지 배포 전용으로 사용됩니다. EOP에서 메일 그룹은 보안 컨텍스트 유무에 관계없이 모든 메일 사용 가능 그룹을 의미합니다.

- 보안 그룹은 관리자 역할에 대 한 액세스 권한이 필요한 전자 메일 사용자의 모음입니다. 예를 들어 특정 사용자 그룹에게 스팸 방지 및 맬웨어 방지 설정을 구성할 수 있도록 관리자 역할 권한을 제공할 수 있습니다.

    > [!NOTE]
    > 기본적으로 모든 새로운 메일 사용이 가능한 보안 그룹을 사용하려면 모든 보낸 사람에 대한 인증이 필요합니다. 따라서 외부 보낸 사람은 메일 사용이 가능한 보안 그룹에 메시지를 보낼 수 없습니다.
  
## <a name="before-you-begin"></a>시작하기 전에

- 이러한 절차를 수행하려면 먼저 사용 권한을 할당받아야 합니다. 필요한 사용 권한을 확인하려면 다음을 참조하세요. [EOP의 기능 사용 권한](feature-permissions-in-eop.md) 항목의 "메일 그룹 및 보안 그룹" 항목

- Exchange 관리 센터를 열려면 exchange [Online Protection의 exchange 관리 센터](../exchange-admin-center-in-exchange-online-protection-eop.md)를 참조 하세요.

- Exchange Online Protection PowerShell cmdlet을 사용 하 여 그룹을 만들고 관리할 때 제한이 발생할 수도 있습니다.

- 이 항목의 PowerShell 절차에서는 일괄 처리 방법을 사용 하 여 명령 결과가 표시 되기까지 몇 분 정도 전파 지연을 발생 시킵니다.

- Windows PowerShell을 사용 하 여 Exchange Online Protection에 연결 하는 방법에 대 한 자세한 내용은 [connect To Exchange Online Protection PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-eop/connect-to-exchange-online-protection-powershell?view=exchange-ps)을 참조 하십시오.

- 이 항목의 절차에 적용할 수 있는 바로 가기 키에 대 한 자세한 내용은 [Exchange Online에서 exchange 관리 센터에 대 한 바로 가기 키](https://docs.microsoft.com/Exchange/accessibility/keyboard-shortcuts-in-admin-center)를 참조 하십시오.

> [!TIP]
> 문제가 있습니까? [Exchange Online Protection](https://go.microsoft.com/fwlink/p/?linkId=285351) 포럼에서 도움을 요청 하세요. 
  
## <a name="create-a-group-in-the-eac"></a>EAC에서 그룹 만들기

1. EAC에서 **받는 사람** \> **그룹**으로 이동 합니다.

2. 필요 **** ![에 따라 새](../media/ITPro-EAC-AddIcon.gif)추가 아이콘을 클릭 한 다음 **메일 그룹** 또는 **보안 그룹**을 클릭 합니다.

3. **새 메일 그룹** 또는 **새 보안 그룹** 페이지에서 다음 설정을 구성 합니다.

   - **표시 이름**: 조직에서 고유 하며 EOP 사용자에 게 의미가 있는 표시 이름을 입력 합니다. 표시 이름은 필요 합니다.

   - **별칭**: 조직에서 고유한 그룹 별칭 (최대 64 자)을 입력 합니다. EOP 사용자가 전자 메일 메시지의 받는 사람: 줄에 입력하는 별칭은 그룹의 표시 이름으로 확인됩니다. 별칭을 변경하는 경우 그룹의 기본 SMTP 주소도 변경되며 새 별칭이 포함됩니다. 별칭은 필수 입력 필드입니다. 

   - **설명**: 사용자가 그룹의 용도를 파악할 수 있도록 그룹에 대 한 설명을 입력 합니다. 

   - **소유자**: 기본적으로 그룹을 만든 사람이 소유자입니다. 추가 아이콘](../media/ITPro-EAC-AddIcon.gif) **추가** ![를 선택 하 여 소유자를 추가할 수 있습니다. 모든 그룹에는 한 명 이상의 소유자가 있어야 합니다.

     > [!NOTE]
     > 소유자는 그룹의 구성원이 아니어도 됩니다.
  
   - **구성원**:이 섹션을 사용 하 여 그룹 구성원을 추가 하 고 사용자가 그룹에 가입 하거나 탈퇴 하는 데 승인이 필요한 지 여부를 지정 합니다. 그룹에 구성원을 추가 하려면 **** ![추가 아이콘](../media/ITPro-EAC-AddIcon.gif)추가를 클릭 합니다.

4. **확인**을 클릭하여 원래 페이지로 돌아갑니다.

5. 작업을 마치면 **저장**을 클릭하여 그룹을 만듭니다. 그러면 새 그룹이 그룹 목록에 표시됩니다.

## <a name="edit-or-remove-a-group-in-the-eac"></a>EAC에서 그룹 편집 또는 제거

1. EAC에서 **받는 사람** \> **그룹**으로 이동합니다.

2. 다음 단계 중 하나를 수행 합니다.

   - 그룹을 편집 하려면 그룹 목록에서 보거나 변경 하려는 그룹을 클릭 한 다음 편집 아이콘](../media/ITPro-EAC-EditIcon.gif) **편집** ![을 클릭 합니다. 일반 설정을 업데이트 하 고, 그룹 소유자를 추가 또는 제거 하 고, 필요에 따라 그룹 구성원을 추가 또는 제거할 수 있습니다.

   - 그룹을 제거 하려면 그룹을 선택 하 고 제거 **** ![아이콘](../media/ITPro-EAC-RemoveIcon.gif)제거를 클릭 합니다.

3. 변경을 마치면 **저장**을 클릭합니다.

## <a name="create-edit-or-remove-a-group-using-remote-windows-powershell"></a>원격 Windows PowerShell을 사용하여 그룹 만들기, 편집 또는 제거

이 섹션에서는 Exchange Online Protection PowerShell에서 그룹을 만들고 속성을 변경 하는 방법에 대 한 정보를 제공 합니다. 또한 기존 그룹을 제거하는 방법도 보여 줍니다.
  
### <a name="create-a-group-using-remote-windows-powershell"></a>원격 Windows PowerShell을 사용 하 여 그룹 만들기
  
이 예제에서는 [New-EOPDistributionGroup](https://docs.microsoft.com/powershell/module/exchange/users-and-groups/New-EOPDistributionGroup) cmdlet을 사용하여 별칭이 itadmin이고 이름이 IT Administrators인 메일 그룹을 만듭니다. 또한 사용자를 그룹의 구성원으로 추가합니다.
  
```Powershell
New-EOPDistributionGroup -Type Distribution -Name "IT Administrators" -Alias itadmin -Members @("Member1","Member2","Member3") -ManagedBy Member1
```

**참고**: 메일 그룹 대신 보안 그룹을 만들려면 `Security` *Type* 매개 변수의 값을 사용 합니다.
  
IT Administrators 그룹을 성공적으로 만들었는지 확인 하려면 다음 명령을 실행 하 여 새 그룹에 대 한 정보를 표시 합니다.
  
```Powershell
Get-Recipient "IT Administrators" | Format-List
```

구문과 매개 변수에 대 한 자세한 내용은 [Get-Recipient](https://docs.microsoft.com/powershell/module/exchange/users-and-groups/Get-Recipient)를 참조 하십시오.

그룹의 구성원 목록을 가져오려면 다음 명령을 실행 합니다.
  
```Powershell
Get-DistributionGroupMember "IT Administrators"
```

구문과 매개 변수에 대 한 자세한 내용은 [get-distributiongroupmember](https://docs.microsoft.com/powershell/module/exchange/users-and-groups/get-distributiongroupmember)를 참조 하십시오.

모든 그룹의 전체 목록을 보려면 다음 명령을 실행 합니다.
  
```Powershell
Get-Recipient -RecipientType "MailUniversalDistributionGroup" | Format-Table | more
```

### <a name="change-the-properties-of-a-group-using-remote-windows-powershell"></a>원격 Windows PowerShell을 사용 하 여 그룹의 속성 변경
  
EAC 대신 PowerShell을 사용 하는 경우의 이점은 여러 그룹의 속성을 변경할 수 있다는 것입니다.
  
다음은 Exchange Online Protection PowerShell을 사용 하 여 그룹 속성을 변경 하는 몇 가지 예입니다.
  
이 예에서는 시애틀 Employees 그룹에 대 한 기본 SMTP 주소 (회신 주소 라고도 함)가 sea.employees@contoso.com로 변경 됩니다.
  
```Powershell
Set-EOPDistributionGroup "Seattle Employees" -PrimarysmptAddress "sea.employees@contoso.com"
```

구문 및 매개 변수에 대 한 자세한 내용은 [set-eopdistributiongroup](https://docs.microsoft.com/powershell/module/exchange/users-and-groups/set-eopdistributiongroup)를 참조 하십시오.

그룹의 속성을 성공적으로 변경 했는지 확인 하려면 다음 명령을 실행 하 여 새 값을 확인 합니다.
  
```Powershell
Get-Recipient "Seattle Employees" | Format-List "PrimarySmtpAddress"
```

이 예에서는 시애틀 Employees 그룹의 모든 구성원을 업데이트 합니다. 모든 구성원은 쉼표로 구분합니다.
  
```Powershell
Update-EOPDistributionGroupMember -Identity "Seattle Employees" -Members @("Member1","Member2","Member3","Member4","Member5")
```

구문과 매개 변수에 대 한 자세한 내용은 [에서는 update-eopdistributiongroupmember](https://docs.microsoft.com/en-us/powershell/module/exchange/users-and-groups/update-eopdistributiongroupmember)를 참조 하십시오.

시애틀 직원 그룹의 모든 구성원 목록을 가져오려면 다음 명령을 실행 합니다. 
  
```Powershell
Get-DistributionGroupMember "Seattle Employees"
```

### <a name="remove-a-group-using-remote-windows-powershell"></a>원격 Windows PowerShell을 사용 하 여 그룹 제거
  
이 예에서는 IT Administrators 라는 메일 그룹을 제거 합니다.
  
```Powershell
Remove-EOPDistributionGroup -Identity "IT Administrators"
```

구문과 매개 변수에 대 한 자세한 내용은 [set-eopdistributiongroup](https://docs.microsoft.com/powershell/module/exchange/users-and-groups/remove-eopdistributiongroup)를 참조 하십시오.

그룹이 제거 되었는지 확인 하려면 다음 명령을 실행 하 여 그룹 (이 경우 "It Administrators")이 삭제 되었는지 확인 합니다.
  
```Powershell
Get-Recipient -RecipientType "MailUniversalDistributionGroup"
```
