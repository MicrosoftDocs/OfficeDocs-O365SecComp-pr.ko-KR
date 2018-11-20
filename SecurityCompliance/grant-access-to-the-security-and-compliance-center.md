---
title: 사용자가 Office 365 보안에 액세스할 &amp; 준수 센터
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 8/18/2017
ms.audience: Admin
ms.topic: article
f1_keywords:
- ms.o365.cc.PermissionsHelp
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MOE150
- MET150
ms.assetid: 2cfce2c8-20c5-47f9-afc4-24b059c1bd76
description: 사용자가 Office 365 보안에 대 한 사용 권한을 할당할 필요가 &amp; 준수 센터 전에 해당 보안 또는 규정 준수 기능 중 하나를 관리할 수 있습니다.
ms.openlocfilehash: 976c4e21351e352672f3075d0f713e63a634ce42
ms.sourcegitcommit: da4aa7335b577148ecd61e09bbb11039b817b287
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/15/2018
ms.locfileid: "26539110"
---
# <a name="give-users-access-to-the-office-365-security-amp-compliance-center"></a>사용자가 Office 365 보안에 액세스할 &amp; 준수 센터

사용자가 Office 365 보안에 대 한 사용 권한을 할당할 필요가 &amp; 준수 센터 전에 해당 보안 또는 규정 준수 기능 중 하나를 관리할 수 있습니다. Office 365 전역 관리자 또는 보안에서 OrganizationManagement 역할 그룹의 구성원으로 &amp; 준수 센터 이러한 권한을 사용자에 게 부여할 수도 있습니다. 사용자에 대 한 액세스를 제공 하는 보안 또는 규정 준수 기능을 관리할 수만 있습니다. 
  
서로 다른 사용 권한에 대 한 자세한 내용은 보안에서 사용자에 게 부여 &amp; 준수 센터, 체크아웃 [Office 365 보안에 대 한 사용 권한을 &amp; 준수 센터](permissions-in-the-security-and-compliance-center.md)합니다.
  
## <a name="what-do-you-need-to-know-before-you-begin"></a>시작하기 전에 알아야 할 내용

- Office 365 전역 관리자 또는 보안에서 OrganizationManagement 역할 그룹의 구성원 일 필요가 &amp; 준수 센터가 문서의 단계를 완료 합니다.
    
- 보안에 대 한 역할 그룹 &amp; 준수 센터의 Exchange Online 역할 그룹에 대 한 유사한 이름이 가질 수 있지만 동일 하지는 합니다. 
    
- 역할 그룹 구성원 자격 Exchange Online 및 보안 간에 공유 되지 않은 &amp; 준수 센터입니다.
    
## <a name="use-the-office-365-admin-center-to-give-another-user-access-to-the-security-amp-compliance-center"></a>Office 365 관리 센터를 사용 하 여 보안에 대 한 다른 사용자 액세스를 부여할 &amp; 준수 센터

1. [Office 365 및 관리 센터로 이동에 로그인](https://go.microsoft.com/fwlink/p/?LinkId=525275)합니다.
    
2. Office 365 관리 센터에서 **관리 센터** 를 열고 하 고 다음을 클릭 **보안 &amp; 준수**합니다. 
    
3. 보안에서 &amp; 준수 센터, **사용 권한 관리**로 이동 하십시오.
    
4. 목록에서 사용자를 추가 하 고 **편집** 을 클릭 하려는 역할 그룹을 선택 ![편집 아이콘](media/O365_MDM_CreatePolicy_EditIcon.gif)합니다.
    
5. **구성원**에서 역할 그룹의 속성 페이지에서 **추가**클릭![아이콘 추가](media/ITPro-EAC-AddIcon.gif) 이름을 선택 하 고 추가 하려는 사용자 (또는 사용자)입니다. 
    
6. 모든 클릭, 역할 그룹에 추가 하려는 사용자를 선택 했을 때 때 **추가-\> ** 하 고 다음 **확인**합니다.
    
7. **저장**을 클릭하여 역할 그룹에 대한 변경 내용을 저장합니다. 
    
### <a name="how-do-you-know-this-worked"></a>작동 여부는 어떻게 확인하나요?

1. 보안에서 &amp; 준수 센터, **사용 권한 관리**로 이동 하십시오.
    
2. 목록에서 구성원을 보려면 역할 그룹을 선택 합니다.
    
3. 오른쪽, 역할 그룹 세부 정보는 역할 그룹의 구성원을 볼 수 있습니다.
    
## <a name="use-powershell-to-give-another-user-access-to-the-security-amp-compliance-center"></a>보안에 대 한 다른 사용자 액세스를 제공 하려면 PowerShell을 사용 하 여 &amp; 준수 센터

1. [Office 365 보안 및 규정 준수 센터 PowerShell에 연결](https://docs.microsoft.com/en-us/powershell/exchange/office-365-scc/connect-to-scc-powershell/connect-to-scc-powershell?view=exchange-ps)합니다.
    
2. 다음 예와 같이 **Add-RoleGroupMember** 명령을 사용하여 사용자를 조직 관리 역할에 추가합니다. 
    
  ```
  Add-RoleGroupMember -Identity "OrganizationManagement" -Member MatildaS
  
  ```

 **매개 변수**
  
-  _-Identity_는 구성원을 추가할 역할 그룹입니다. 
    
- - _구성원_ 은 사서함, 유니버설 보안 그룹 (USG) 또는 컴퓨터 역할 그룹에 추가 합니다. 한번에 하나만 구성원을 지정할 수 있습니다. 
    
구문과 매개 변수에 대 한 자세한 정보를 [Add-rolegroupmember](https://go.microsoft.com/fwlink/p/?LinkId=510859)을 참조 하십시오.
  
### <a name="how-do-you-know-this-worked"></a>작동 여부는 어떻게 확인하나요?

사용자가 액세스에 제공한 보안을 확인 하려면 &amp; 준수 센터 다음 예제와 같이 조직 관리 역할 그룹의 구성원을 볼 수 **Get-rolegroupmember** cmdlet을 사용 합니다. 
  
```
Get-RoleGroupMember -Identity "OrganizationManagement"

```

구문과 매개 변수에 대 한 자세한 정보를 [Get-rolegroupmember](https://go.microsoft.com/fwlink/p/?LinkId=510860)을 참조 하십시오.
  

