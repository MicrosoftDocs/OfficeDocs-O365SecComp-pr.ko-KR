---
title: 메일 흐름 규칙을 사용하여 사용자가 Microsoft에 보고한 내용 확인
ms.author: krowley
author: kccross
manager: laurawi
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 8401f520-8e7c-467b-9e06-4a9fdb2ba548
description: 사용자가 분석을 위해 Microsoft에 전자 메일 메시지를 보내지 못하도록 하 고 자체 보안 프로세스에서 사용 하는 것을 방지 하는 Exchange 전송 규칙을 만들 수 있습니다.
ms.openlocfilehash: 7ee8fb2bca1071ccd4080379485c1670a5e66a73
ms.sourcegitcommit: 06d6e63225f912d0f3c6bb836c61eb11c1dbe97a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/22/2019
ms.locfileid: "30206411"
---
# <a name="use-mail-flow-rules-to-see-what-your-users-are-reporting-to-microsoft"></a>메일 흐름 규칙을 사용하여 사용자가 Microsoft에 보고한 내용 확인

분석을 위해 가양성 및 거짓 네거티브 메시지를 Microsoft에 보낼 수 있는 방법은 여러 가지가 있습니다. 관리자는 메일 흐름 규칙을 사용 하 여 사용자가 Microsoft에 스팸, 비 스팸 및 피싱 사기를 보고 하는 항목을 확인할 수 있습니다. 자세한 내용은 [분석을 위해 Microsoft에 스팸 및 스팸이 아닌 메시지 제출을](submit-spam-non-spam-and-phishing-scam-messages-to-microsoft-for-analysis.md)참조 하세요. 반대로, 사용자가 분석을 위해 Microsoft에 전자 메일 메시지를 보내지 못하도록 하 고 자체 보안 프로세스에서 사용 하는 것을 방지 하는 Exchange 전송 규칙을 만들 수 있습니다.
  
## <a name="what-do-you-need-to-know-before-you-begin"></a>시작하기 전에 알아야 할 내용

예상 완료 시간: 5분
  
이 절차를 수행 하려면 먼저 사용 권한을 할당 받아야 합니다. 필요한 사용 권한을 확인 하려면 [메시징 정책 및 준수 권한](http://technet.microsoft.com/library/ec4d3b9f-b85a-4cb9-95f5-6fc149c3899b.aspx) 항목의 "전송 규칙" 항목 및 [클라이언트 및 모바일 장치 사용 권한](http://technet.microsoft.com/library/57eca42a-5a7f-4c65-89f0-7a84f2dbea19.aspx) 항목의 "웹 사서함 정책에서 Outlook" 항목을 참조 하십시오. 
  
이 항목의 절차에 적용할 수 있는 바로 가기 키에 대한 자세한 내용은 **Exchange 관리 센터의 바로 가기 키**을 참조하세요.
  
## <a name="use-the-eac-to-create-a-mail-flow-rule-to-view-users-manual-junk-phishing-and-not-junk-reports"></a>EAC를 사용 하 여 메일 흐름 규칙을 만들어 사용자의 수동 정크, 피싱 및 정크가 아닌 보고서를 볼 수 있습니다.

1. EAC에서 **메일 흐름** \> **규칙**으로 이동합니다.
    
2. ![아이콘 추가](media/ITPro-EAC-AddIcon.gif)를 클릭한 다음 **새 규칙 만들기**를 선택합니다.
    
3. 규칙 이름을 지정하고 **기타 옵션**을 클릭합니다.
    
4. **다음의 경우 이 규칙 적용**에서 **받는 사람**을 선택하고 **주소에 다음 단어 포함**을 선택합니다.
    
5. **단어 또는 구 지정** 상자에 다음을 입력합니다. 
    - 를 `abuse@messaging.microsoft.com` 입력 하 고 ![아이콘](media/ITPro-EAC-AddIcon.gif)추가를 클릭 한 다음 `junk@office365.microsoft.com` 아이콘](media/ITPro-EAC-AddIcon.gif)추가를 ![클릭 합니다. 이러한 전자 메일 주소는 Microsoft에 거짓 부정 메시지를 전송 하는 데 사용 됩니다.
    - 를 `phish@office365.microsoft.com` 입력 하 고 ![아이콘](media/ITPro-EAC-AddIcon.gif)추가를 클릭 합니다. 이 전자 메일 주소는 부재 중 피싱 메시지를 Microsoft에 제출 하는 데 사용 됩니다.
    - 를 `false_positive@messaging.microsoft.com` 입력 하 고 ![아이콘](media/ITPro-EAC-AddIcon.gif)추가를 클릭 한 다음 `not_junk@office365.microsoft.com` 아이콘](media/ITPro-EAC-AddIcon.gif)추가를 ![클릭 합니다. 이러한 전자 메일 주소는 Microsoft에 허위 긍정 메시지를 전송 하는 데 사용 됩니다.
    - **확인**을 클릭합니다.
    
6. **다음 작업 실행**에서 **메시지를 받는 사람** ...을 선택한 후 메시지를 받을 사서함을 선택 합니다. 
    
7. 원하는 경우 규칙을 감사 하 고 규칙을 테스트 하며 특정 기간 동안 규칙을 활성화 하 고 기타 선택 항목을 만들 수 있습니다. 규칙을 적용 하기 전에 테스트 하는 것이 좋습니다. [메일 흐름 규칙에 대 한 절차를](https://docs.microsoft.com/Exchange/policy-and-compliance/mail-flow-rules/mail-flow-rule-procedures)참조 하세요. 
    
8. **저장** 단추를 클릭하여 규칙을 저장합니다. 규칙이 규칙 목록에 표시됩니다. 
    
규칙을 만들어 적용 하 고 나면 조직에서 지정 된 전자 메일 주소로 보내는 모든 메시지가 지정 된 사서함에 복사 됩니다.
  

