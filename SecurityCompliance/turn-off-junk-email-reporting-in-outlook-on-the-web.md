---
title: 웹용 Outlook에서 정크 메일 보고 해제
ms.author: krowley
author: kccross
manager: laurawi
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
ms.assetid: 8d57fe9e-57b8-4884-9317-80b380804b4a
description: Office 365 관리자는 사용자가 전자 메일을 정크 메일로 보고 하는 기능을 해제할 수 있습니다.
ms.openlocfilehash: efe898f57fdf322ce49edd9e2577daab46dd8d8f
ms.sourcegitcommit: a80bd8626720fabdf592b84e4424cd3a83d08280
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30223827"
---
# <a name="turn-off-junk-email-reporting-in-outlook-on-the-web"></a>웹용 Outlook에서 정크 메일 보고 해제

웹용 outlook [의 정크 메일 및 피싱 사기 보고 ](report-junk-email-and-phishing-scams-in-outlook-on-the-web-eop.md)에 설명 된 대로, 웹용 outlook (이전의 outlook web App이 라고도 함) 정크 메일 보고 옵션을 사용 하 여 정크, 피싱 및 정크 메시지를 분석을 위해 Microsoft에 보낼 수 있습니다. 이러한 옵션을 사용 하지 않으려는 경우 관리자는 [set-owamailboxpolicy](http://technet.microsoft.com/library/530166f7-ab42-4609-ba73-9b5a39b567be.aspx) cmdlet을 통해이를 해제할 수 있습니다. 
  
## <a name="what-do-you-need-to-know-before-you-begin"></a>시작하기 전에 알아야 할 내용
<a name="sectionSection0"> </a>

- 예상 완료 시간: 5분
    
- 이 절차를 수행 하려면 먼저 사용 권한을 할당 받아야 합니다. 필요한 사용 권한을 확인 하려면 [웹 사용 권한](http://technet.microsoft.com/library/57eca42a-5a7f-4c65-89f0-7a84f2dbea19.aspx#OutlookWebApp) 항목의 outlook에서 "웹 사서함 정책의 outlook" 항목을 참조 하십시오. 

- exchange online powershell에 연결 하려면 [exchange online powershell에 연결](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell)을 참조 하세요.

## <a name="turn-off-junk-phishing-and-not-junk-reporting-to-microsoft"></a>Microsoft에 대 한 정크 메일, 피싱 및 정크 메일 아님 보고 해제
<a name="sectionSection1"> </a>

먼저 다음 명령을 실행 하 여 웹 사서함 정책에서 사용 가능한 Outlook 이름을 가져옵니다.
  
```
Get-OwaMailboxPolicy | Format-Table Name
```

다음 구문을 사용 하 여 웹용 Outlook에서 정크 및 정크 메일 아님 보고를 사용 하거나 사용 하지 않도록 설정 합니다.
  
```
Set-OwaMailboxPolicy -Identity "<OWAMailboxPolicyName>" -ReportJunkEmailEnabled <$true | $false>
```

다음은 기본 Outlook web app 사서함 정책에서 보고 기능을 해제 하는 예제입니다.
  
```
Set-OwaMailboxPolicy -Identity "OwaMailboxPolicy-Default" -ReportJunkEmailEnabled $false
```

구문과 매개 변수에 대 한 자세한 내용은 [set-owamailboxpolicy](http://technet.microsoft.com/library/bdd580d3-8812-4b4a-93e8-c6401b0d2f0f.aspx) 및 [set-owamailboxpolicy](http://technet.microsoft.com/library/530166f7-ab42-4609-ba73-9b5a39b567be.aspx)를 참조 하십시오.

## <a name="how-do-you-know-this-worked"></a>작동 여부는 어떻게 확인합니까?
<a name="sectionSection2"> </a>

**set-owamailboxpolicy** 를 실행 하 여 매개 변수 값을 확인 한 다음 웹에서 outlook을 열어 해당 사용자에 게 적용 되는 웹 사서함 정책을 사용 하는 outlook을 연 다음 정크, 피싱 및 정크 메일을 보고 하는 옵션을 사용할 수 없는지 확인 합니다. 메시지를 정크 메일 이나 피싱이 아닌 메시지로 표시할 수는 있지만 보고할 수는 없습니다. 
