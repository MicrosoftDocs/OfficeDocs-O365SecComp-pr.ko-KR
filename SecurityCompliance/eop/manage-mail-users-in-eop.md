---
title: EOP에서 메일 사용자 관리
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 12/9/2016
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
ms.assetid: 4bfaf2ab-e633-4227-8bde-effefb41a3db
description: 메일 사용자 정의는 EOP(Exchange Online Protection) 서비스 관리의 중요한 부분입니다.
ms.openlocfilehash: b0093c64a0fcb5997b474e7bd491c0915164b77e
ms.sourcegitcommit: 48fa456981b5c52ab8aeace173c8366b9f36723b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/28/2019
ms.locfileid: "30341029"
---
# <a name="manage-mail-users-in-eop"></a>EOP에서 메일 사용자 관리

메일 사용자 정의는 EOP(Exchange Online Protection) 서비스 관리의 중요한 부분입니다. EOP에서는 여러 가지 방식으로 사용자를 관리할 수 있습니다.
  
- 디렉터리 동기화를 사용 하 여 메일 사용자 관리: 회사의 온-프레미스 Active directory 환경에 기존 사용자 계정이 있는 경우 해당 계정을 Azure AD (active directory)와 동기화 하 여 계정 복사본을 클라우드에 저장할 수 있습니다. 기존 사용자 계정을 Azure Active Directory에 동기화 할 때 EAC (Exchange 관리 센터)의 **받는 사람** 창에서 해당 사용자를 볼 수 있습니다. 디렉터리 동기화를 사용 하는 것이 좋습니다. 
    
- EAC를 사용하여 메일 사용자 관리: EAC에서 메일 사용자를 직접 추가하고 관리합니다. 이 방법이 메일 사용자를 추가하는 가장 쉬운 방법이며 한 번에 한 명의 사용자를 추가하는 데 유용합니다.
    
- 원격 Windows PowerShell을 사용하여 메일 사용자 관리: 원격 Windows PowerShell을 실행하여 메일 사용자를 추가하고 관리합니다. 이 방법은 여러 레코드를 추가하고 스크립트를 만드는 데 유용합니다.
    
> [!NOTE]
> Office 365 관리 센터에서 사용자를 추가할 수 있지만 이러한 사용자는 메일 받는 사람으로 사용할 수 없습니다. 
  
## <a name="before-you-begin"></a>시작하기 전에

- 이 항목의 절차는 특정 사용 권한이 필요합니다. 사용 권한 정보에 대한 각 절차를 참조하세요.
    
- 이 항목의 절차에 적용할 수 있는 바로 가기 키에 대한 자세한 내용은 **Exchange 관리 센터의 바로 가기 키**을 참조하세요.
    
> [!TIP]
> 문제가 있습니까? Exchange 포럼에서 도움을 요청하세요. 포럼 주소는 다음과 같습니다.[Exchange Server](https://go.microsoft.com/fwlink/p/?linkId=60612),[Exchange Online](https://go.microsoft.com/fwlink/p/?linkId=267542), 또는 [Exchange Online Protection](https://go.microsoft.com/fwlink/p/?linkId=285351) 
  
## <a name="use-directory-synchronization-to-manage-mail-users"></a>디렉터리 동기화를 사용하여 메일 사용자 관리

이 섹션에서는 디렉터리 동기화를 사용하여 전자 메일 사용자를 관리하는 방법에 대해 설명합니다.
  
> [!IMPORTANT]
> 디렉터리 동기화를 사용하여 받는 사람을 관리하는 경우 Office 365 관리 센터에서 계속해서 사용자를 추가하고 관리할 수 있습니다. 하지만 이러한 받는 사람은 온-프레미스 Active Directory와 동기화되지는 않습니다. 디렉터리 동기화는 온-프레미스 Active Directory의 받는 사람만 클라우드로 동기화하기 때문입니다. 
  
> [!TIP]
>  > **Outlook 수신 허용-보낸 사람 및 수신 거부 목록** -서비스와 동기화 된 경우이 목록에는 서비스의 스팸 필터링 보다 우선 순위가 더 높은 디렉터리 동기화 기능을 사용 하는 것이 좋습니다. 이를 통해 사용자는 사용자별 또는 도메인 별로 수신 허용-보낸 사람 및 수신 거부 목록을 관리할 수 있습니다. **dbeb (> Directory 기반 edge 차단)** -dbeb에 대 한 자세한 내용은 [Use Directory Based edge 차단은 잘못 된 받는 사람에 게 보낸 메시지를 거부](http://technet.microsoft.com/library/ca7b7416-92ed-40ad-abdb-695be46ea2e4.aspx)합니다 .를 참조 하세요. > 최종 사용자 스팸 **격리** -최종 사용자 스팸 격리에 액세스 하기 위해 최종 사용자에 게 유효한 Office 365 사용자 ID 및 암호가 있어야 합니다. 온-프레미스 사서함을 보호 하는 EOP 고객은 유효한 전자 메일 사용자 여야 합니다. > **메일 흐름 규칙** -디렉터리 동기화를 사용 하는 경우 기존 Active directory 사용자 및 그룹이 클라우드로 자동 업로드 되 고 특정 사용자를 대상으로 하는 메일 흐름 규칙 (전송 규칙이 라고도 함)을 만들 수 있습니다. 아니면 EAC 또는 Exchange Online Protection PowerShell을 통해 그룹을 수동으로 추가 하지 않아도 됩니다. [동적 메일 그룹](https://go.microsoft.com/fwlink/?LinkId=507569) 은 디렉터리 동기화를 통해 동기화 할 수 없습니다. 
  
 **시작하기 전에**
  
[디렉터리 동기화 준비](https://go.microsoft.com/fwlink/p/?LinkId=308908)의 설명에 따라 필요한 사용 권한을 얻고 디렉터리 동기화를 준비합니다.
  
### <a name="to-synchronize-user-directories"></a>사용자 디렉터리를 동기화하려면

1. [디렉터리 동기화 활성화](https://go.microsoft.com/fwlink/p/?LinkId=308909)의 설명에 따라 디렉터리 동기화를 활성화합니다.
    
2. [디렉터리 동기화 컴퓨터 설정](http://go.microsoft.com/fwlink/p/?LinkId=308911)의 설명에 따라 디렉터리 동기화 컴퓨터를 설정합니다.
    
3. [구성 마법사를 사용하여 디렉터리 동기화](http://go.microsoft.com/fwlink/?LinkId=308912)의 설명에 따라 디렉터리를 동기화합니다.
    
    > [!IMPORTANT]
    > Azure Active Directory 동기화 도구 구성 마법사를 완료하면 Active Directory 포리스트에 **MSOL_AD_SYNC** 계정이 만들어집니다. 이 계정을 사용하여 온-프레미스 Active Directory 정보를 읽고 동기화합니다. 디렉터리 동기화가 정상적으로 작동하도록 하려면 로컬 디렉터리 동기화 서버의 TCP 443이 열려 있는지 확인합니다. 
  
4. [동기화된 사용자 활성화](http://go.microsoft.com/fwlink/p/?LinkId=308913)의 설명에 따라 동기화된 사용자를 활성화합니다.
    
5. [디렉터리 동기화 관리](http://go.microsoft.com/fwlink/p/?LinkId=308915)의 설명에 따라 디렉터리 동기화를 관리합니다.
    
6. EOP가 올바르게 동기화되는지 확인합니다. 이렇게 하려면 EAC에서 **받는 사람** \> **연락처**로 이동한 다음 온-프레미스 환경에서 사용자 목록이 올바르게 동기화되었는지 확인합니다. 
    
## <a name="use-the-eac-to-manage-mail-users"></a>EAC를 사용하여 메일 사용자 관리

이 섹션에서는 전자 메일 사용자를 EAC에서 직접 추가 및 관리하는 방법에 대해 설명합니다.
  
 **시작하기 전에**
  
이러한 절차를 수행하려면 먼저 사용 권한을 할당받아야 합니다. 필요한 사용 권한을 확인하려면 다음을 참조하세요. [EOP의 기능 사용 권한](feature-permissions-in-eop.md)의 "사용자, 연락처 및 역할 그룹" 항목
  
### <a name="to-add-a-mail-user-in-the-eac"></a>EAC에서 메일 사용자를 추가하려면

1. EAC에서 **받는 사람** \> **연락처**로 이동한 다음 **새로 만들기 +** 를 클릭하여 전자 메일 사용자를 만듭니다.
    
2. **새 메일 사용자** 페이지에서 다음을 비롯한 사용자의 정보를 입력합니다. 
    
   ****

|**메일 사용자 속성**|**설명**|
|:-----|:-----|
|**이름**, **이니셜**, **성** <br/> |해당 상자에 사용자의 전체 이름을 입력합니다.  <br/> |
|**표시 이름** <br/> |이름을 64자까지 입력합니다. 기본적으로 이 상자에는 **이름**, **이니셜** 및 **성** 상자의 이름(있는 경우)이 표시됩니다. 표시 이름은 필수 입력 필드입니다.  <br/> |
|**별칭** <br/> |사용자의 고유한 별칭을 64자까지 입력합니다. 별칭은 필수 입력 필드입니다.  <br/> |
|**외부 전자 메일 주소** <br/> |사용자의 외부 전자 메일 주소를 입력합니다.  <br/> |
|**사용자 ID** <br/> |사용자가 서비스에 로그인하는 데 사용할 이름을 입력합니다. 사용자 로그인 이름은 @ 기호 왼쪽의 사용자 이름과 오른쪽의 접미사로 구성됩니다. 일반적으로 접미사는 사용자 계정이 있는 도메인 이름입니다.  <br/> |
|**새 암호** <br/> |사용자가 서비스에 로그인하는 데 사용할 암호를 입력합니다. 제공하는 암호는 사용자 계정을 만들 도메인의 암호 길이, 복잡성 및 내역 요구 사항을 준수해야 합니다.  <br/> |
|**암호 확인** <br/> |암호를 다시 입력하여 확인합니다.  <br/> |
   
3. **저장**을 클릭하여 새 전자 메일 사용자를 만듭니다. 그러면 새 사용자가 사용자 목록에 표시됩니다. 
    
### <a name="to-edit-or-remove-a-mail-user-in-the-eac"></a>EAC에서 메일 사용자를 편집하거나 제거하려면

- EAC에서 **받는 사람** \> **연락처로**이동 합니다. 사용자 목록에서 보거나 변경 하려는 사용자를 클릭 한 다음 편집 아이콘](../media/ITPro-EAC-EditIcon.gif) **편집** ![을 선택 하 여 사용자 설정을 필요에 따라 업데이트 합니다. 사용자의 이름, 별칭 또는 연락처 정보를 변경할 수 있으며 조직에서 사용자의 역할에 대 한 자세한 정보를 기록할 수 있습니다. 사용자를 선택한 다음 제거 아이콘](../media/ITPro-EAC-RemoveIcon.gif) **제거**![를 선택 하 여 삭제를 삭제할 수도 있습니다. 
    
## <a name="use-remote-windows-powershell-to-manage-mail-users"></a>원격 Windows PowerShell을 사용하여 메일 사용자 관리

이 섹션에서는 원격 Windows PowerShell을 사용하여 메일 사용자를 추가하고 관리하는 방법에 대한 정보가 제공됩니다.
  
 **시작하기 전에**
  
- 이러한 절차를 수행하려면 먼저 사용 권한을 할당받아야 합니다. 필요한 사용 권한을 확인하려면 다음을 참조하세요. [EOP의 기능 사용 권한](feature-permissions-in-eop.md)의 "사용자, 연락처 및 역할 그룹" 항목
    
- 원격 PowerShell cmdlet을 사용하여 메일 사용자를 만들 때는 제한에 도달할 수 있습니다.
    
- 이 cmdlet은 일괄 처리 방법을 사용하므로 cmdlet 결과가 보이기 몇 분 전에 전파 지연이 발생합니다.
    
- Windows PowerShell을 사용하여 Exchange Online Protection에 연결하는 방법에 대한 자세한 내용은 [원격 PowerShell을 사용하여 Exchange Online Protection에 연결](http://technet.microsoft.com/library/054e0fd7-d465-4572-93f8-a00a9136e4d1.aspx)을 참조하세요.
    
 **원격 PowerShell을 사용하여 메일 사용자를 추가하려면**
  
이 예제에서는 다음 세부 정보를 사용하여 [New-EOPMailUser](http://technet.microsoft.com/library/0520cf33-4ad0-44e4-99a3-1b485739fc05.aspx) cmdlet을 통해 EOP에서 Jeffrey Zeng에 대한 메일 사용이 가능한 사용자 계정을 만듭니다. 
  
- 이름은 Jeffrey고 성은 Zeng입니다.
    
- 이름은 Jeffrey이고 표시 이름은 Jeffrey Zeng입니다.
    
- 별칭은 jeffreyz입니다.
    
- 외부 전자 메일 주소는 jzeng@tailspintoys.com입니다.
    
- Office 365 로그인 이름은 jeffreyz@contoso.onmicrosoft.com입니다.
    
- 암호는 Pa$$word1입니다.
    
```
New-EOPMailUser -LastName Zeng -FirstName Jeffrey -DisplayName "Jeffrey Zeng" -Name Jeffrey -Alias jeffreyz -MicrosoftOnlineServicesID jeffreyz@contoso.onmicrosoft.com -ExternalEmailAddress jeffreyz@tailspintoys.com -Password (ConvertTo-SecureString -String 'Pa$$word1' -AsPlainText -Force)
```

 **결과에 문제가 없는지 확인하려면**
  
다음과 같이 [Get-User](http://technet.microsoft.com/library/2a33c9e6-33da-438c-912d-28ce3f4c9afb.aspx) cmdlet을 실행하여 새 메일 사용자 Jeffrey Zeng에 대한 정보를 표시합니다. 
  
```
Get-User "Jeffrey Zeng"

```

 **원격 PowerShell을 사용하여 메일 사용자의 속성을 편집하려면**
  
[Get-Recipient](http://technet.microsoft.com/library/2ce6250f-0ad3-4b29-870c-e1d6e1e154bc.aspx) 및 [Set-EOPMailUser](http://technet.microsoft.com/library/834c3de6-1485-4d50-bb96-262a2c0c8619.aspx) cmdlet을 사용하여 메일 사용자의 속성을 보거나 변경할 수 있습니다. 
  
다음 예에서는 Pilar Pinilla의 외부 전자 메일 주소를 설정합니다.
  
```
Set-EOPMailUser -Identity "Pilar Pinilla" -EmailAddresses pilarp@tailspintoys.com
```

다음 예에서는 모든 메일 사용자의 Company 속성을 Contoso로 설정합니다.
  
```
$Recip = Get-Recipient -ResultSize unlimited -Filter {(RecipientTypeDetails -eq 'mailuser')}
$Recip | foreach {Set-EOPUser -Identity $_.Alias -Company Contoso}

```

 **결과에 문제가 없는지 확인하려면**
  
메일 사용자 Pilar Pinella의 속성을 변경한 이전 예제에서 [Get-Recipient](http://technet.microsoft.com/library/2ce6250f-0ad3-4b29-870c-e1d6e1e154bc.aspx) cmdlet을 사용하여 변경 내용을 확인합니다. 여러 메일 연락처의 여러 속성을 확인할 수 있습니다. 
  
```
Get-Recipient -Identity "Pilar Pinilla" | Format-List 

```

모든 메일 사용자에 대한 Company 속성이 Contoso로 설정된 이전 예제에서 변경 사항을 확인하려면 다음 명령을 실행합니다.
  
```
Get-Recipient -ResultSize unlimited -Filter {(RecipientTypeDetails -eq 'mailuser')} | Format-List Name,Company
```

> [!IMPORTANT]
> 이 cmdlet은 일괄 처리 방법을 사용하므로 cmdlet 결과가 보이기 몇 분 전에 전파 지연이 발생합니다. 
  
 **원격 PowerShell을 사용하여 메일 사용자를 제거하려면**
  
이 예제에서는 [Remove-EOPMailUser](http://technet.microsoft.com/library/cb91dc26-ed22-4d3c-9f64-df9df1754edb.aspx) cmdlet을 사용하여 사용자 Jeffrey Zeng을 삭제합니다. 
  
```
Remove-EOPMailUser -Identity Jeffrey
```

 **결과에 문제가 없는지 확인하려면**
  
다음과 같이 [Get-Recipient](http://technet.microsoft.com/library/2ce6250f-0ad3-4b29-870c-e1d6e1e154bc.aspx) cmdlet을 실행합니다. 해당 사용자가 더 이상 존재하지 않으므로 오류 메시지가 표시됩니다. 
  
```
Get-Recipient Jeffrey | fl
```


