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
ms.openlocfilehash: 2763ca35456bb40b5b11e38eb2e7497934115d5f
ms.sourcegitcommit: 32ecff689ae32c59a39b7633ca0f36a304e7516e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/09/2019
ms.locfileid: "35599644"
---
# <a name="manage-groups-in-eop"></a>EOP에서 그룹 관리

 EOP(Exchange Online Protection)를 사용하여 Exchange 조직에 메일 사용 가능 그룹을 만들 수 있습니다. 또한 구성원 자격, 전자 메일 주소 및 그룹의 기타 측면을 지정하는 그룹 속성을 정의하거나 업데이트할 수도 있습니다. 필요에 따라 메일 그룹 및 보안 그룹을 만들 수 있습니다. 이러한 그룹은 EAC(Exchange 관리 센터)를 사용하거나 원격 Windows PowerShell을 통해 만들 수 있습니다. 
  
## <a name="types-of-mail-enabled-groups"></a>메일 사용 가능 그룹의 유형

Exchange 조직에 대해 다음과 같은 두 가지 유형의 그룹을 만들 수 있습니다.
  
- 메일 그룹이라고도 하는 [EAC에서 그룹 만들기](manage-groups-in-eop.md)은 특정 관심 영역과 관련하여 전자 메일을 보내거나 받아야 하는 팀 또는 임시 그룹과 같은 전자 메일 사용자 집합입니다. 메일 그룹은 전자 메일 메시지 배포 전용으로 사용됩니다. EOP에서 메일 그룹은 보안 컨텍스트 유무에 관계없이 모든 메일 사용 가능 그룹을 의미합니다.
    
- 보안 그룹이라고도 하는 [EAC에서 그룹 편집 또는 제거](manage-groups-in-eop.md)은 관리자 역할에 대한 액세스 권한이 있어야 하는 전자 메일 사용자 집합입니다. 예를 들어 특정 사용자 그룹에게 스팸 방지 및 맬웨어 방지 설정을 구성할 수 있도록 관리자 역할 권한을 제공할 수 있습니다.
    
    > [!NOTE]
    > 기본적으로 모든 새로운 메일 사용이 가능한 보안 그룹을 사용하려면 모든 보낸 사람에 대한 인증이 필요합니다. 따라서 외부 보낸 사람은 메일 사용이 가능한 보안 그룹에 메시지를 보낼 수 없습니다. 
  
## <a name="before-you-begin"></a>시작하기 전에

- 이러한 절차를 수행하려면 먼저 사용 권한을 할당받아야 합니다. 필요한 사용 권한을 확인하려면 다음을 참조하세요. [EOP의 기능 사용 권한](feature-permissions-in-eop.md) 항목의 "메일 그룹 및 보안 그룹" 항목 
    
- 원격 PowerShell cmdlet을 사용하여 그룹을 만들고 관리할 경우 제한에 도달할 수 있습니다.
    
- 이 cmdlet은 일괄 처리 방법을 사용하므로 cmdlet 결과가 보이기 몇 분 전에 전파 지연이 발생합니다.
    
- Windows PowerShell을 사용하여 Exchange Online Protection에 연결하는 방법에 대한 자세한 내용은 [원격 PowerShell을 사용하여 Exchange Online Protection에 연결](https://docs.microsoft.com/powershell/exchange/exchange-eop/connect-to-exchange-online-protection-powershell?view=exchange-ps)을 참조하세요.
    
- 이 항목의 절차에 적용할 수 있는 바로 가기 키에 대한 자세한 내용은 **Keyboard shortcuts in Exchange 2013**을 참조하세요.
    
> [!TIP]
> 문제가 있습니까? Exchange 포럼에서 도움을 요청하세요. 포럼 주소는 다음과 같습니다.[Exchange Server](https://go.microsoft.com/fwlink/p/?linkId=60612),[Exchange Online](https://go.microsoft.com/fwlink/p/?linkId=267542), 또는 [Exchange Online Protection](https://go.microsoft.com/fwlink/p/?linkId=285351) 
  
## <a name="create-a-group-in-the-eac"></a>EAC에서 그룹 만들기

1. EAC(Exchange 관리 센터)에서 **받는 사람** \> **그룹**으로 이동합니다.
    
2. **새로 만들기**![아이콘 추가](../media/ITPro-EAC-AddIcon.gif)를 클릭한 다음 필요에 따라 **메일 그룹** 또는 **보안 그룹**을 클릭합니다. 두 그룹의 차이점은 [메일 사용 가능 그룹의 유형](manage-groups-in-eop.md)을 참조하세요. 
    
3. **새 메일 그룹** 또는 **새 보안 그룹** 페이지에서 다음 필드에 값을 입력합니다. 
    
  - **표시 이름** 조직에서 고유하며 EOP 사용자에게 의미가 있는 표시 이름을 입력합니다. 표시 이름은 필수 입력 필드입니다. 
    
  - **별칭** 조직에서 고유한 그룹 별칭을 64자까지 입력합니다. EOP 사용자가 전자 메일 메시지의 받는 사람: 줄에 입력하는 별칭은 그룹의 표시 이름으로 확인됩니다. 별칭을 변경하는 경우 그룹의 기본 SMTP 주소도 변경되며 새 별칭이 포함됩니다. 별칭은 필수 입력 필드입니다. 
    
  - **설명** 다른 사람들이 그룹의 용도를 파악할 수 있도록 그룹 설명을 입력합니다. 
    
  - **소유자** 기본적으로 그룹을 만든 사람이 소유자입니다. **추가**![아이콘 추가](../media/ITPro-EAC-AddIcon.gif)를 선택하여 소유자를 추가할 수 있습니다. 모든 그룹에는 한 명 이상의 소유자가 있어야 합니다.
    
    > [!NOTE]
    > 소유자는 그룹의 구성원이 아니어도 됩니다. 
  
  - **구성원** 이 섹션을 사용하면 그룹 구성원을 추가하고 그룹에 구독하거나 그룹에서 탈퇴하려는 사용자에 대해 승인이 필요한지 여부를 지정할 수 있습니다. 그룹에 구성원을 추가하려면 **추가**![아이콘 추가](../media/ITPro-EAC-AddIcon.gif)를 클릭합니다.
    
4. **확인**을 클릭하여 원래 페이지로 돌아갑니다. 
    
5. 작업을 마치면 **저장**을 클릭하여 그룹을 만듭니다. 그러면 새 그룹이 그룹 목록에 표시됩니다. 
    
## <a name="edit-or-remove-a-group-in-the-eac"></a>EAC에서 그룹 편집 또는 제거

1. EAC에서 **받는 사람** \> **그룹**으로 이동합니다.
    
2. 다음 중 하나를 수행합니다.
    
  - 그룹을 편집 하려면 그룹 목록에서 보거나 변경할 배포 또는 보안 그룹을 클릭 한 다음 편집 아이콘](../media/ITPro-EAC-EditIcon.gif) **편집** ![을 클릭 합니다. 필요에 따라 일반 설정을 업데이트하고 그룹 소유자 및 그룹 구성원을 추가하거나 제거할 수 있습니다.
    
  - 그룹을 제거하려면 그룹을 선택하고 **제거**![아이콘 제거](../media/ITPro-EAC-RemoveIcon.gif)를 클릭합니다.
    
3. 변경을 마치면 **저장**을 클릭합니다.
    
## <a name="create-edit-or-remove-a-group-using-remote-windows-powershell"></a>원격 Windows PowerShell을 사용하여 그룹 만들기, 편집 또는 제거

이 섹션에서는 원격 Windows PowerShell을 사용하여 그룹을 만들고 속성을 변경하는 방법에 대한 정보가 제공됩니다. 또한 기존 그룹을 제거하는 방법도 보여 줍니다. 
  
 **원격 Windows PowerShell을 사용하여 그룹을 만들려면**
  
이 예제에서는 [New-EOPDistributionGroup](http://technet.microsoft.com/library/4610dfe5-fca8-4ba8-be3c-535d1753e0f4.aspx) cmdlet을 사용하여 별칭이 itadmin이고 이름이 IT Administrators인 메일 그룹을 만듭니다. 또한 사용자를 그룹의 구성원으로 추가합니다. 
  
```Powershell
New-EOPDistributionGroup -Type "Distribution" -Name "IT Administrators" -Alias itadmin -Members @("Member1","Member2","Member3") -ManagedBy "Member1"

```

메일 그룹 대신 보안 그룹을 만들려면  `-Type "Security"`를 대신 지정합니다. 
  
IT Administrators 그룹을 성공적으로 만들었는지 확인하려면 [Get-Recipient](http://technet.microsoft.com/library/2ce6250f-0ad3-4b29-870c-e1d6e1e154bc.aspx) cmdlet을 실행하여 새 그룹에 대한 정보를 표시합니다. 
  
```Powershell
Get-Recipient "IT Administrators" | Format-List

```

그룹의 구성원 목록을 표시하려면 다음과 같이 [Get-DistributionGroupMember](http://technet.microsoft.com/library/15c71bc5-4246-44ac-8b34-8ccd585294b5.aspx) cmdlet을 실행합니다. 
  
```Powershell
Get-DistributionGroupMember "IT Administrators"

```

모든 그룹의 전체 목록을 표시하려면 다음과 같이 [Get-Recipient](http://technet.microsoft.com/library/2ce6250f-0ad3-4b29-870c-e1d6e1e154bc.aspx) cmdlet을 실행합니다. 
  
```Powershell
Get-Recipient -RecipientType "MailUniversalDistributionGroup" | FT | more

```

 **원격 Windows PowerShell을 사용하여 그룹의 속성을 변경하려면**
  
[Get-Recipient](http://technet.microsoft.com/library/2ce6250f-0ad3-4b29-870c-e1d6e1e154bc.aspx) 및 [Set-EOPDistributionGroup](http://technet.microsoft.com/library/689a66c5-a524-4870-88f3-091fd6eae3b7.aspx) cmdlet을 사용하여 그룹의 속성을 보고 변경합니다. EAC 대신 원격 PowerShell을 사용할 때의 한 가지 이점은 여러 그룹의 속성을 변경할 수 있다는 것입니다. 
  
다음은 원격 Windows PowerShell을 사용하여 그룹 속성을 변경하는 방법의 몇 가지 예입니다.
  
이 예제에서는 [Set-EOPDistributionGroup](http://technet.microsoft.com/library/689a66c5-a524-4870-88f3-091fd6eae3b7.aspx) cmdlet을 사용하여 Seattle Employees 그룹의 기본 SMTP 주소(회신 주소라고도 함)를 sea.employees@contoso.com으로 변경합니다. 
  
```Powershell
Set-EOPDistributionGroup "Seattle Employees" -PrimarysmptAddress "sea.employees@contoso.com"

```

그룹의 속성을 성공적으로 변경했는지 확인하려면 [Get-Recipient](http://technet.microsoft.com/library/2ce6250f-0ad3-4b29-870c-e1d6e1e154bc.aspx) cmdlet을 사용하여 변경 내용을 검토합니다. 원격 PowerShell을 사용할 때 얻을 수 있는 한 가지 이점은 여러 그룹의 여러 속성을 볼 수 있다는 것입니다. 기본 SMTP 주소 그룹을 변경한 위의 예에서는 다음 명령을 실행하여 새 값을 확인합니다. 
  
```Powershell
Get-Recipient "Seattle Employees" | FL "PrimarySmtpAddress"

```

이 예제에서는 [Update-EOPDistributionGroupMember](http://technet.microsoft.com/library/a6d4f790-1b94-42f8-af6f-fa79c504d8ec.aspx) cmdlet을 사용하여 Seattle Employees 그룹의 모든 구성원을 업데이트합니다. 모든 구성원은 쉼표로 구분합니다. 
  
```Powershell
Update-EOPDistributionGroupMember -Identity "Seattle Employees" -Members @("Member1","Member2","Member3","Member4","Member5")

```

Seattle Employees 그룹의 모든 구성원 목록을 표시하려면 다음과 같이 [Get-DistributionGroupMember](http://technet.microsoft.com/library/15c71bc5-4246-44ac-8b34-8ccd585294b5.aspx) cmdlet을 사용합니다. 
  
```Powershell
Get-DistributionGroupMember "Seattle Employees"

```

 **원격 Windows PowerShell을 사용하여 그룹을 제거하려면**
  
이 예제에서는 [Remove-EOPDistributionGroup](http://technet.microsoft.com/library/a17b1307-3187-40b0-a438-c7b35a34c002.aspx) cmdlet을 사용하여 IT Administrators라는 메일 그룹을 제거합니다. 
  
```Powershell
Remove-EOPDistributionGroup -Identity "IT Administrators" 

```

그룹이 제거되었는지 확인하려면 다음과 같이 [Get-Recipient](http://technet.microsoft.com/library/2ce6250f-0ad3-4b29-870c-e1d6e1e154bc.aspx) cmdlet을 실행하고 그룹(이 경우 "It Administrators")이 삭제되었는지 확인합니다. 
  
```Powershell
Get-Recipient -RecipientType "MailUniversalDistributionGroup"

```


