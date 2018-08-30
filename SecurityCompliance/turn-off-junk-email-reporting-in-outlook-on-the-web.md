---
title: 정크 메일 웹에 있는 Outlook에서 보고 해제
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 10/9/2015
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
ms.custom: TN2DMC
localization_priority: Normal
ms.assetid: 8d57fe9e-57b8-4884-9317-80b380804b4a
description: Office 365 관리자를 해제할 수 있습니다 기능 보고서 전자 메일을 사용자에 대 한 정크 메일로 합니다.
ms.openlocfilehash: 8ee5ff87408b80c443e4cf950ce49f624096becb
ms.sourcegitcommit: c31424cafbf1953f2864d7e2ceb95b329a694edb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/29/2018
ms.locfileid: "23272043"
---
# <a name="turn-off-junk-email-reporting-in-outlook-on-the-web"></a>정크 메일 웹에 있는 Outlook에서 보고 해제

[보고서 정크 메일 및 피싱 메일 웹에 있는 outlook에서 ](report-junk-email-and-phishing-scams-in-outlook-on-the-web-eop.md)에서 설명한 대로 웹 정크 메일 옵션을 보고에 Outlook을 사용 하 여 분석을 위해 Microsoft에 정크, 피싱, 및 정크 메일이 아닌 메시지를 보낼 수 있습니다. 이러한 옵션을 사용 하 여 않으려면 관리자가 해제할 수 하 [Set-owamailboxpolicy](http://technet.microsoft.com/library/530166f7-ab42-4609-ba73-9b5a39b567be.aspx) cmdlet을 통해. 
  
## <a name="what-do-you-need-to-know-before-you-begin"></a>시작하기 전에 알아야 할 내용
<a name="sectionSection0"> </a>

- 예상 완료 시간: 5분
    
- 이 절차를 수행 하기 전에 사용 권한을 할당 해야 합니다. 필요한 사용 권한을 [Outlook Web App 사용 권한](http://technet.microsoft.com/library/57eca42a-5a7f-4c65-89f0-7a84f2dbea19.aspx#OutlookWebApp) 항목의 "Outlook Web App 사서함 정책" 항목을 참조 하십시오. 
    
- 정크 메일 보고를 해제 하는 데 필요한 cmdlet를 실행 하기 전에 [Get-owamailboxpolicy](http://technet.microsoft.com/library/bdd580d3-8812-4b4a-93e8-c6401b0d2f0f.aspx) 및 [Set-owamailboxpolicy](http://technet.microsoft.com/library/530166f7-ab42-4609-ba73-9b5a39b567be.aspx) 항목에 대 한 참조 정보를 검토 하려면 유용할 수 있습니다. 
    
## <a name="turn-off-junk-phishing-and-not-junk-reporting-to-microsoft"></a>정크, 피싱 끄고 Microsoft에 보고를 정크 메일 아님
<a name="sectionSection1"> </a>

먼저, 다음 cmdlet을 실행하여 보고를 해제할 가상 디렉터리를 가져옵니다.
  
```
Get-OwaMailboxPolicy -Identity <parameter>
```

다음 cmdlet을 실행하여 Microsoft에 대한 정크 및 정크 아님 보고를 해제합니다.
  
```
Set-OwaMailboxPolicy -Identity <parameter> -ReportJunkEmailEnabled $false
```

예를 들어 다음 cmdlet은 가상 디렉터리 Contoso\owa에 대한 보고를 해제합니다.
  
```
Set-OwaMailboxPolicy -Identity Default -ReportJunkEmailEnabled $false
```

## <a name="how-do-you-know-this-worked"></a>작동 여부는 어떻게 확인합니까?
<a name="sectionSection2"> </a>

Get-owamailboxpolicy 매개 변수 값을 확인 하 고 웹에서 Outlook에 액세스 한 다음을 실행 하 고 정크, 피싱, 보고 및 정크 메일 아님 하는 옵션을 사용할 수 있는지 확인 합니다. 정크, 피싱으로 메시지를 표시할 수 및 정크 메일 아님으로 여전히 수 있지만 보고할 수는 없습니다. 
  

