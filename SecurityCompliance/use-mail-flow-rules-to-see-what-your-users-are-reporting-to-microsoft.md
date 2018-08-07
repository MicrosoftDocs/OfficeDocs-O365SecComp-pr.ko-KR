---
title: 메일 흐름 규칙을 사용 하 여 Microsoft에 보고 하는 사용자에 게는 참조 하려면
ms.author: krowley
author: kccross
manager: laurawi
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
ms.assetid: 8401f520-8e7c-467b-9e06-4a9fdb2ba548
description: 사용자가 분석을 위해 Microsoft에 전자 메일 메시지를 보내지 못하도록 방지 하 고 고유한 보안 프로세스에서 사용 하는 Exchange 전송 규칙을 만들 수 있습니다.
ms.openlocfilehash: 6c6af23e6a5f345e26c7dc09c898f2978ea51a5f
ms.sourcegitcommit: df1e9590a9fa152fa776f16d9b25c180ba7198f3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/07/2018
ms.locfileid: "22122588"
---
# <a name="use-mail-flow-rules-to-see-what-your-users-are-reporting-to-microsoft"></a>메일 흐름 규칙을 사용 하 여 Microsoft에 보고 하는 사용자에 게는 참조 하려면

여러 가지 방법으로 분석을 위해 Microsoft에 false 양의 하 고 false 이면 음수 메시지를 보낼 수 있습니다. 관리자로 서 어떤 사용자에 게는 Microsoft에 보고를 피싱 메일, 스팸 및 스팸이 아닌와 참조를 메일 흐름 규칙을 사용할 수 있습니다. 자세한 내용은 [전송 스팸, 스팸이 아닌 및 분석을 위해 Microsoft에 피싱 사기 메시지를](submit-spam-non-spam-and-phishing-scam-messages-to-microsoft-for-analysis.md)참조 하십시오. 반면, 사용자가 분석을 위해 Microsoft에 전자 메일 메시지를 보내지 못하도록 방지 하 고 고유한 보안 프로세스에서 사용 하는 Exchange 전송 규칙을 만들 수 있습니다.
  
## <a name="what-do-you-need-to-know-before-you-begin"></a>시작하기 전에 알아야 할 내용

예상 완료 시간: 5분
  
이 절차를 수행 하기 전에 사용 권한을 할당 해야 합니다. 필요한 사용 권한을 확인 하려면 [메시징 정책 및 규정 준수 권한](http://technet.microsoft.com/library/ec4d3b9f-b85a-4cb9-95f5-6fc149c3899b.aspx) 항목의 "전송 규칙" 항목 및 [클라이언트 및 모바일 장치 사용 권한](http://technet.microsoft.com/library/57eca42a-5a7f-4c65-89f0-7a84f2dbea19.aspx) 항목의 "Outlook Web App 사서함 정책" 항목을 참조 하십시오. 
  
이 항목의 절차에 적용할 수 있는 바로 가기 키에 대한 자세한 내용은 **Exchange 관리 센터의 바로 가기 키**을 참조하세요.
  
## <a name="use-the-eac-to-create-a-mail-flow-rule-to-view-users-manual-junk-phishing-and-not-junk-reports"></a>EAC를 사용 하 여 사용자의 수동 정크, 피싱, 및 정크 메일 아님으로 보고서를 보려면 메일 흐름 규칙을 만들려면

1. EAC에서 **메일 흐름** \> **규칙**으로 이동합니다.
    
2. ![아이콘 추가](media/ITPro-EAC-AddIcon.png)를 클릭한 다음 **새 규칙 만들기**를 선택합니다.
    
3. 규칙 이름을 지정하고 **기타 옵션**을 클릭합니다.
    
4. **다음의 경우 이 규칙 적용**에서 **받는 사람**을 선택하고 **주소에 다음 단어 포함**을 선택합니다.
    
5. **단어 또는 구 지정** 상자에 다음을 입력합니다. 
    - 형식은 `abuse@messaging.microsoft.com` 다음을 클릭 하 고 ![아이콘 추가](media/ITPro-EAC-AddIcon.png), 다음을 입력 하 고 `junk@office365.microsoft.com` 다음을 클릭 하 고 ![아이콘 추가](media/ITPro-EAC-AddIcon.png)합니다. 이러한 전자 메일 주소는 Microsoft로 거짓 부정 메시지 전송 하는데 사용 됩니다.
    - 형식은 `phish@office365.microsoft.com` 다음을 클릭 하 고 ![아이콘 추가](media/ITPro-EAC-AddIcon.png)합니다. 이 전자 메일 주소는 Microsoft로 부재중된 피싱 메시지를 전송 하는데 사용 됩니다.
    - 형식은 `false_positive@messaging.microsoft.com` 다음을 클릭 하 고 ![아이콘 추가](media/ITPro-EAC-AddIcon.png), 다음을 입력 하 고 `not_junk@office365.microsoft.com` 다음을 클릭 하 고 ![아이콘 추가](media/ITPro-EAC-AddIcon.png)합니다. 이러한 전자 메일 주소는 Microsoft로 가양성 메시지 전송 하는데 사용 됩니다.
    - **확인**을 클릭합니다.
    
6. **다음을 수행**을 선택 **숨은 참조 메시지를...** 위치를 하려는 사서함의 메시지를 받을 다음 하 고 다음 선택 하 고 있습니다. 
    
7. 원하는 경우에 감사 규칙, 규칙을 테스트, 특정 기간 동안 규칙 활성화를 선택 하 고 다른 선택 항목을 만들 수 있습니다. 적용 하기 전에 기간에 대 한 규칙을 테스트 하는 것이 좋습니다. [메일 흐름 규칙에 대 한 절차](https://docs.microsoft.com/Exchange/policy-and-compliance/mail-flow-rules/mail-flow-rule-procedures)를 참조 하십시오. 
    
8. **저장** 단추를 클릭하여 규칙을 저장합니다. 규칙이 규칙 목록에 표시됩니다. 
    
만들 규칙을 적용 하 고 지정 된 전자 메일 주소를 조직에서 전송 되는 모든 메시지가 지정 된 사서함에 복사 됩니다.
  

