---
title: 메시지-관리자 도움말에 대 한 검색 및 삭제
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 12/20/2017
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
ms.assetid: 8c36bb03-e716-4fdd-9958-4aa7a2a1db42
description: 관리자는 검색 사서함 cmdlet를 사용 하 여 사용자 사서함을 검색 하 고 다음 사서함에서 메시지를 삭제 수 있습니다.
ms.openlocfilehash: ed110c4a3e36a93970af99e9548aa293d94307fd
ms.sourcegitcommit: 22bca85c3c6d946083d3784f72e886c068d49f4a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/06/2018
ms.locfileid: "22026585"
---
# <a name="search-for-and-delete-messages---admin-help"></a>메시지-관리자 도움말에 대 한 검색 및 삭제
  
관리자는 **검색 사서함** cmdlet를 사용 하 여 사용자 사서함을 검색 하 고 다음 사서함에서 메시지를 삭제 수 있습니다. 
  
한 번에 메시지를 검색하여 삭제하려면  **DeleteContent** 스위치와 함께 _Search-Mailbox_ cmdlet을 실행합니다. 하지만, 이 경우 검색 결과를 미리 보거나 검색에 의해 반환되는 메시지 로그를 생성할 수 없으며, 삭제하면 안 되는 메시지를 실수로 삭제할 수 있습니다. 메시지를 삭제하기 전에 검색되는 메시지에 대한 로그를 미리 보려면  **LogOnly** 스위치와 함께 _Search-Mailbox_ cmdlet을 실행합니다. 
  
추가적인 안전 장치로서,  _TargetMailbox_ 및  _TargetFolder_ 매개 변수를 사용하여 먼저 메시지를 다른 사서함에 복사할 수 있습니다. 이렇게 하면 삭제되는 메시지의 복사본을 보관하여 필요할 때 다시 액세스할 수 있습니다. 
  
## <a name="what-do-i-need-to-know-before-i-begin"></a>시작하기 전에 알아야 할 사항은 무엇입니까?
<a name="sectionSection0"> </a>

- 예상 완료 시간: 10분 실제 시간은 사서함 및 검색 쿼리의 크기에 따라 다를 수 있습니다.
    
- 이 절차를 수행하는 데 EAC(Exchange 관리 센터)를 사용할 수 없습니다. 셸을 사용해야 합니다.
    
- 모두 검색 하 여 사용자의 사서함에서 메시지를 삭제 하려면 다음 관리 역할을 할당 해야 합니다.
    
  - **사서함 검색** 이 역할을 사용 하면 조직에서 여러 사서함 간에 메시지를 검색할 수 있습니다. 관리자는 기본적으로이 역할을 할당 되지 않습니다. 사용자가 직접이 역할을 할당 사서함을 검색할 수 있도록, 검색 관리 역할 그룹의 구성원으로 자신을 추가 합니다. [검색 관리 역할 그룹에 사용자 추가](http://technet.microsoft.com/library/729e09d8-614b-431f-ae04-ae41fb4c628e.aspx)참조 하십시오.
    
  - **사서함 가져오기 내보내기** 이 역할을 사용 하면 사용자의 사서함에서 메시지를 삭제할 수 있습니다. 기본적으로이 역할은 모든 역할 그룹에 할당 되지 않습니다. 사용자의 사서함에서 메시지를 삭제 하려면 조직 관리 역할 그룹에는 사서함 가져오기 내보내기 역할을 추가할 수 있습니다. 자세한 내용은 [관리 역할 그룹](http://technet.microsoft.com/library/ab9b7a3b-bf67-4ba1-bde5-8e6ac174b82c.aspx) 의 "역할을 역할 그룹에 게 추가" 섹션을 참조 하십시오. 
    
- 메시지를 삭제 하려는 사서함 단일 항목 복구를 사용할 수 있으면 먼저 기능을 비활성화 해야 합니다. 자세한 내용은 [사서함에 대 한 단일 항목 복구를 사용 하지 않도록 설정 하거나 사용](http://technet.microsoft.com/library/2e7f1bcd-8395-45ad-86ce-22868bd46af0.aspx)을 참조 하십시오.
    
- 메시지를 삭제 하려는 사서함은 보류 상태로 변경 하는 경우에 레코드 관리 또는 보류를 제거 하 고 사서함 콘텐츠를 삭제 하기 전에 법률 부서를 확인 하는 것이 좋습니다. 승인을 얻으려면 항목 [정리 Up the 복구 가능한 항목 폴더](http://technet.microsoft.com/library/82c310f8-de2f-46f2-8e1a-edb6055d6e69.aspx)에 나열 된 단계를 수행 합니다.
    
- 최대 10, 000 사서함 **검색 사서함** cmdlet을 사용 하 여 검색할 수 있습니다. Exchange Online 조직 이며 10, 000 개 이상의 사서함이 있습니까, 경우 무제한 사서함을 검색 하려면 준수 검색 기능 (또는 해당 **새로 ComplianceSearch** cmdlet)를 사용할 수 있습니다. 다음 규정 준수 검색을 통해 반환 되는 메시지를 삭제 하려면 **새로 만들기 ComplianceSearchAction** cmdlet을 사용할 수 있습니다. 자세한 내용은 [Office 365 조직에서 전자 메일 메시지를 삭제 하 고 검색에 대 한](https://go.microsoft.com/fwlink/p/?LinkId=786856)를 참조 하십시오.
    
- ( *SearchQuery* 매개 변수를 사용 하 여) 하 여 검색 쿼리를 포함 하는 경우 **검색 사서함** cmdlet은 검색 결과에 최대 10, 000 항목을 반환 합니다. 따라서 검색 쿼리를 포함 하는 경우에 10, 000 개 이상의 항목을 삭제 하려면 **사서함 검색** 명령을 여러 번 실행 해야할 수 있습니다. 
    
- **Search-mailbox** cmdlet을 실행 하는 경우에 사용자의 보관 사서함을 검색 합니다. 마찬가지로, _DeleteContent_ 스위치와 함께 **Search-mailbox** cmdlet을 사용 하는 경우 기본 보관 사서함에 항목이 삭제 됩니다. 이 방지 하려면 *DoNotIncludeArchive* 스위치를 포함할 수 있습니다. 또한는 사용 하지 않는 _DeleteContent_ 스위치를 사용 하는 Exchange에서 메시지를 삭제 하려면 온라인 예기치 않은 데이터 손실이 발생할 수 있으므로 사용 보관 자동 확장 된 사서함 하는 것이 좋습니다. 
    
## <a name="search-messages-and-log-the-search-results"></a>메시지 검색 및 검색 결과 기록
<a name="sectionSection1"> </a>

이 예에서는 April Stewart의 사서함에서 제목에 "Your bank statement" 구가 포함된 메시지를 검색하고 관리자 사서함의 SearchAndDeleteLog 폴더에 검색 결과를 기록합니다. 메시지는 대상 사서함에 복사되거나 대상 사서함에서 삭제되지 않습니다.
  
```
Search-Mailbox -Identity "April Stewart" -SearchQuery 'Subject:"Your bank statement"' -TargetMailbox administrator -TargetFolder "SearchAndDeleteLog" -LogOnly -LogLevel Full
```

이 예제에서는 모든 유형의 파일 이름에 "트로이" 단어를 포함 하 고 관리자의 사서함에 로그 메시지를 전송 하는 첨부 파일이 있는 메시지에 대 한 조직에서 모든 사서함을 검색 합니다.
  
```
Get-Mailbox -ResultSize unlimited | Search-Mailbox -SearchQuery attachment:trojan* -TargetMailbox administrator -TargetFolder "SearchAndDeleteLog" -LogOnly -LogLevel Full
```

구문과 매개 변수에 대한 자세한 내용은 [Search-Mailbox](http://technet.microsoft.com/library/9ee3b02c-d343-4816-a583-a90b1fad4b26.aspx)를 참조하십시오.
  
[Return to top](search-for-and-delete-messagesadmin-help.md#top)
  
## <a name="search-and-delete-messages"></a>메시지 검색 및 삭제
<a name="sectionSection2"> </a>

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

이 예제에서는 "이이 파일 다운로드" 제목줄이 있는 메시지에 대 한 조직에서 모든 사서함을 검색 한 다음 영구적으로 삭제 합니다. 
  
```
Get-Mailbox -ResultSize unlimited | Search-Mailbox -SearchQuery 'Subject:"Download this file"' -DeleteContent
```

구문과 매개 변수에 대한 자세한 내용은 [Search-Mailbox](http://technet.microsoft.com/library/9ee3b02c-d343-4816-a583-a90b1fad4b26.aspx)를 참조하십시오.
  
[Return to top](search-for-and-delete-messagesadmin-help.md#top)
  
## <a name="using-the--loglevel-full-parameter"></a>-LogLevel 전체 매개 변수를 사용 하 여
<a name="sectionSection3"> </a>

앞의 예제를 _LogLevel_ 매개 변수 중 일부에서 함께 `Full` 값 **사서함 검색** cmdlet에 의해 반환 된 결과 대 한 자세한 정보를 기록 하는데 사용 됩니다. 이 매개 변수를 포함 하는 경우 전자 메일 메시지를 만들고 _TargetMailbox_ 매개 변수에 의해 지정 된 사서함에 전송 합니다. (즉, 검색 Results.csv 라는 CSV 형식의 파일) 로그 파일이 전자 메일 메시지에 첨부 되 고 _TargetFolder_ 매개 변수에 의해 지정 된 폴더에 배치 됩니다. 로그 파일 **Search-mailbox** cmdlet을 실행 하면 검색 결과에 포함 된 각 메시지에 대 한 행을 포함 합니다. 
  

