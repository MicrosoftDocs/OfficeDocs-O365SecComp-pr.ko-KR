---
title: 스팸 필터 규칙 및 스팸 필터 정책에 잘못 된 문자 방지
ms.author: tracyp
author: MSFTTracyP
manager: laurawi
ms.date: 9/24/2018
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.collection:
- M365-security-compliance
description: 스팸 방지 구성에 잘못 된 문자가 있는 관리자가 보안 &amp; 및 준수 센터를 사용 하려고 할 때 문제를 해결 하는 데 도움이 되는 정보를 제공 합니다.
ms.openlocfilehash: 0e7dcb40d8e54045caa55083e2cbf0585a80869d
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/17/2019
ms.locfileid: "34154167"
---
# <a name="avoid-invalid-characters-in-your-spam-filter-rules-and-spam-filter-policy"></a>스팸 필터 규칙 및 스팸 필터 정책에 잘못 된 문자 방지 

이전에 Office 365 관리자는 EAC (Exchange 관리 센터)를 사용 하 여 스팸 필터 규칙 및 스팸 필터 정책을 설정 하 고 구성 합니다. 이제 보안 &amp; 및 준수 센터를 사용 하 여 스팸 방지 구성을 관리 합니다. 다음 문자는 EAC에서 지원 되지만 보안 &amp; 및 준수 센터에서 사용할 수 없습니다.  

**잘못 된 문자:**
  
```\ % & * + / = ? { } | < > ( ) ; : , [ ] "```

스팸 필터 규칙 또는 스팸 필터 정책에 잘못 된 문자가 포함 된 경우 다음과 같은 문제가 발생할 수 있습니다.
- 보안 &amp; 및 준수 센터에서 정책이 나 규칙을 찾지 못할 수 있습니다.
- Windows PowerShell을 사용 하 여 규칙 또는 정책을 가져오려고 하면 오류가 나타날 수 있습니다.
- 정책이 나 설정이 제대로 실행 되지 않거나 예상 대로 수행 되지 않을 수 있습니다.

## <a name="remove-the-invalid-characters-from-the-spam-filter-policy-and-rules"></a>스팸 필터 정책 및 규칙에서 잘못 된 문자 제거

잘못 된 문자를 포함 하는 정책 및 규칙을 식별 한 후에는 Windows PowerShell cmdlet을 사용 하 여 이름을 변경할 수 있습니다. 

1. [원격 PowerShell을 사용 하 여 Exchange Online에 연결](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell?view=exchange-ps)합니다.
    
2. 스팸 필터 정책의 이름을 변경 하려면 다음과 같이 Get-hostedcontentfilterpolicy cmdlet을 실행 합니다.
    
    ```
    Set-HostedContentFilterPolicy -Identity "Old policy name" -Name "New policy name"
    ```  

3. 스팸 필터 규칙의 이름을 변경 하려면 다음과 같이 Disable-hostedcontentfilterrule cmdlet을 실행 합니다.
    
    ```
    Set-HostedContentFilterRule -Identity "Old rule name" -Name "New rule name"
    ```  

  
 ## <a name="for-more-information"></a>자세한 내용

[보안 &amp; 및 준수 센터의 위협 관리](threat-management.md)
  
[Get-hostedcontentfilterpolicy](https://docs.microsoft.com/powershell/module/exchange/antispam-antimalware/set-hostedcontentfilterpolicy?view=exchange-ps)

[Disable-hostedcontentfilterrule](https://docs.microsoft.com/powershell/module/exchange/antispam-antimalware/set-hostedcontentfilterrule?view=exchange-ps)
