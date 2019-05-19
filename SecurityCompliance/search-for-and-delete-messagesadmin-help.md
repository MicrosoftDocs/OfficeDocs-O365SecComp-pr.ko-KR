---
title: 메시지 검색 및 삭제 - 관리자 도움말
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 12/20/2017
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.collection: M365-security-compliance
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 8c36bb03-e716-4fdd-9958-4aa7a2a1db42
description: 관리자는 검색 사서함 cmdlet을 사용 하 여 사용자 사서함을 검색 한 다음 사서함에서 메시지를 삭제할 수 있습니다.
ms.openlocfilehash: a097b39aa179ed18c3d5426eeeacff204d48ee9b
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/17/2019
ms.locfileid: "34158490"
---
# <a name="search-for-and-delete-messages---admin-help"></a>메시지 검색 및 삭제 - 관리자 도움말
  
관리자는 **검색 사서함** cmdlet을 사용 하 여 사용자 사서함을 검색 한 다음 사서함에서 메시지를 삭제할 수 있습니다. 
  
한 번에 메시지를 검색하여 삭제하려면  **DeleteContent** 스위치와 함께 _Search-Mailbox_ cmdlet을 실행합니다. 하지만, 이 경우 검색 결과를 미리 보거나 검색에 의해 반환되는 메시지 로그를 생성할 수 없으며, 삭제하면 안 되는 메시지를 실수로 삭제할 수 있습니다. 메시지를 삭제하기 전에 검색되는 메시지에 대한 로그를 미리 보려면  **LogOnly** 스위치와 함께 _Search-Mailbox_ cmdlet을 실행합니다. 
  
추가적인 안전 장치로서,  _TargetMailbox_ 및  _TargetFolder_ 매개 변수를 사용하여 먼저 메시지를 다른 사서함에 복사할 수 있습니다. 이렇게 하면 삭제되는 메시지의 복사본을 보관하여 필요할 때 다시 액세스할 수 있습니다. 
  
## <a name="before-you-begin"></a>시작하기 전에

- 예상 완료 시간: 10분. 실제 시간은 사서함 및 검색 쿼리의 크기에 따라 다를 수 있습니다.
    
- 이 절차를 수행하는 데 EAC(Exchange 관리 센터)를 사용할 수 없습니다. 셸을 사용해야 합니다.
    
- 사용자 사서함에서 메시지를 검색 및 삭제 하려면 다음 관리 역할을 둘 다 할당 받아야 합니다.
    
  - **사서함 검색**-이 역할을 사용 하면 조직의 여러 사서함에서 메시지를 검색할 수 있습니다. 관리자에게는 기본적으로 이 역할이 할당되지 않습니다. 사서함을 검색할 수 있도록 이 역할을 자신에게 할당하려면 자신을 검색 관리 역할 그룹의 구성원으로 추가합니다. [Add a User to the Discovery Management Role Group](http://technet.microsoft.com/library/729e09d8-614b-431f-ae04-ae41fb4c628e.aspx)를 참조하세요.
    
  - **사서함 가져오기 내보내기** -이 역할을 사용 하면 사용자 사서함에서 메시지를 삭제할 수 있습니다. 기본적으로 이 역할은 역할 그룹에 할당되지 않습니다. 사용자 사서함에서 메시지를 삭제하려면 조직 관리 역할 그룹에 사서함 가져오기 내보내기 역할을 추가하면 됩니다. 자세한 내용은 [역할 그룹 관리](http://technet.microsoft.com/library/ab9b7a3b-bf67-4ba1-bde5-8e6ac174b82c.aspx) 의 "역할 그룹에 역할 추가" 섹션을 참조 하십시오. 
    
- 메시지를 삭제하려는 사서함에서 단일 항목 복구를 사용하는 경우 먼저 이 기능을 사용하지 않도록 설정해야 합니다. 자세한 내용은 [사서함에 대한 단일 항목을 사용하거나 사용하지 않도록 설정](http://technet.microsoft.com/library/2e7f1bcd-8395-45ad-86ce-22868bd46af0.aspx)을 참조하세요.
    
- 메시지를 삭제 하려는 사서함이 보존 상태에 있는 경우 보존을 제거 하 고 사서함 콘텐츠를 삭제 하기 전에 레코드 관리 또는 법률 부서를 확인 하는 것이 좋습니다. 승인을 받은 후에 [는 복구 가능한 항목 폴더 정리](http://technet.microsoft.com/library/82c310f8-de2f-46f2-8e1a-edb6055d6e69.aspx)항목에 나와 있는 단계를 수행 합니다.
    
- **검색 사서함** cmdlet을 사용 하 여 최대 1만 개의 사서함을 검색할 수 있습니다. Exchange Online 조직이 고 사서함이 1만 개 보다 많은 경우 준수 검색 기능 (또는 해당 **ComplianceSearch** cmdlet)을 사용 하 여 사서함 수를 무제한으로 검색할 수 있습니다. 그런 다음 **new-compliancesearchaction** cmdlet을 사용 하 여 준수 검색에서 반환 된 메시지를 삭제할 수 있습니다. 자세한 내용은 [Office 365 조 직에서 전자 메일 메시지 검색 및 삭제](https://go.microsoft.com/fwlink/p/?LinkId=786856)를 참조 하세요.
    
- *Searchquery* 매개 변수를 사용 하 여 검색 쿼리를 포함 하는 경우 검색 **사서함** cmdlet은 최대 1만 개의 항목을 검색 결과에 반환 합니다. 따라서 검색 쿼리를 포함 하는 경우 1만 개 보다 많은 항목을 삭제 하려면 **검색 사서함** 명령을 여러 번 실행 해야 할 수 있습니다. 
    
- 또한 **검색 사서함** cmdlet을 실행 하면 사용자의 보관 사서함도 검색 됩니다. 마찬가지로, _DeleteContent_ 스위치와 함께 **검색 사서함** cmdlet을 사용 하면 기본 보관 사서함의 항목이 삭제 됩니다. 이를 방지 하기 위해 *만드는 경우 donotincludearchive* 스위치를 포함할 수 있습니다. 또한 예기치 않은 데이터 손실이 발생할 수 있으므로 _DeleteContent_ 스위치를 사용 하 여 자동 확장 기능을 사용 하는 Exchange Online 사서함의 메시지를 삭제 하지 않는 것이 좋습니다. 
    
## <a name="search-messages-and-log-the-search-results"></a>메시지 검색 및 검색 결과 기록

이 예에서는 April Stewart의 사서함에서 제목에 "Your bank statement" 구가 포함된 메시지를 검색하고 관리자 사서함의 SearchAndDeleteLog 폴더에 검색 결과를 기록합니다. 메시지는 대상 사서함에 복사되거나 대상 사서함에서 삭제되지 않습니다.
  
```
Search-Mailbox -Identity "April Stewart" -SearchQuery 'Subject:"Your bank statement"' -TargetMailbox administrator -TargetFolder "SearchAndDeleteLog" -LogOnly -LogLevel Full
```

이 예에서는 조직의 모든 사서함에서 파일 이름에 "트로이" 라는 단어가 포함 된 모든 유형의 첨부 파일이 있는 메시지를 검색 하 고 관리자의 사서함에 로그 메시지를 보냅니다.
  
```
Get-Mailbox -ResultSize unlimited | Search-Mailbox -SearchQuery attachment:trojan* -TargetMailbox administrator -TargetFolder "SearchAndDeleteLog" -LogOnly -LogLevel Full
```

구문과 매개 변수에 대한 자세한 내용은 [Search-Mailbox](http://technet.microsoft.com/library/9ee3b02c-d343-4816-a583-a90b1fad4b26.aspx)를 참조하십시오.
  
 
## <a name="search-and-delete-messages"></a>메시지 검색 및 삭제

이 예에서는 April Stewart의 사서함에서 제목 필드에 "Your bank statement" 구가 포함된 메시지를 검색하고 검색 결과를 다른 폴더에 복사하지 않고 원본 사서함에서 메시지를 삭제합니다. 앞에서 설명한 것처럼 사용자 사서함에서 메시지를 삭제하려면 사서함 가져오기 내보내기 관리 역할이 할당되어 있어야 합니다.
  
> [!IMPORTANT]
> **DeleteContent** 스위치와 함께 _Search-Mailbox_ cmdlet을 사용할 경우 메시지는 원본 사서함에서 영구 삭제됩니다. 영구히 메시지를 삭제하기 전에  _LogOnly_ 스위치를 사용하여 검색으로 찾은 메시지에 대해 로그를 생성한 후 삭제하거나 해당 메시지를 다른 사서함에 복사한 후 원본 사서함에서 삭제하는 것이 좋습니다. 
  
```
Search-Mailbox -Identity "April Stewart" -SearchQuery 'Subject:"Your bank statement"' -DeleteContent
```

이 예에서는 April Stewart의 사서함에서 제목 필드에 "Your bank statement" 구가 포함된 메시지를 검색하고 BackupMailbox 사서함의 AprilStewart-DeletedMessages 폴더에 검색 결과를 복사한 후 April 사서함에서 메시지를 삭제합니다.
  
```
Search-Mailbox -Identity "April Stewart" -SearchQuery 'Subject:"Your bank statement"' -TargetMailbox "BackupMailbox" -TargetFolder "AprilStewart-DeletedMessages" -LogLevel Full -DeleteContent
```

이 예에서는 조직의 모든 사서함에서 제목이 "이 파일을 다운로드 합니다." 라는 메시지를 검색 한 다음이를 영구적으로 삭제 합니다. 
  
```
Get-Mailbox -ResultSize unlimited | Search-Mailbox -SearchQuery 'Subject:"Download this file"' -DeleteContent
```

구문과 매개 변수에 대한 자세한 내용은 [Search-Mailbox](http://technet.microsoft.com/library/9ee3b02c-d343-4816-a583-a90b1fad4b26.aspx)를 참조하십시오.

## <a name="using-the--loglevel-full-parameter"></a>-LogLevel Full 매개 변수 사용

위 예제 중 일부는이 `Full` 값을 포함 하는 _LogLevel_ 매개 변수를 사용 하 여 **검색 사서함** cmdlet에서 반환 되는 결과에 대 한 자세한 정보를 기록 합니다. 이 매개 변수를 포함 하면 전자 메일 메시지가 만들어지고 _targetmailbox_ 매개 변수로 지정 된 사서함으로 전송 됩니다. 이 전자 메일 메시지에는 로그 파일 (검색 결과인 .csv 이라는 CSV 파일)이 첨부 되며 _Targetfolder_ 매개 변수에 지정 된 폴더에 배치 됩니다. 로그 파일에는 **검색 사서함** cmdlet을 실행할 때 검색 결과에 포함 된 각 메시지에 대 한 행이 포함 됩니다. 
