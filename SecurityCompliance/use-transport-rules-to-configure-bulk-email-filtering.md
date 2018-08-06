---
title: 전송 규칙을 사용 하 여 대량 전자 메일 필터링을 구성 하려면
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 12/20/2017
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
ms.assetid: 2889c82e-fab0-4e85-87b0-b001b2ccd4f7
description: 기본 스팸 콘텐츠 필터 정책을 사용 하 여 스팸 및 대량 전자 메일에 대 한 회사 전체의 콘텐츠 필터를 설정할 수 있습니다. 체크아웃 구성 스팸 필터 정책 및 Set-hostedcontentfilterpolicy 콘텐츠 필터 정책을 설정 하는 방법에 있습니다.
ms.openlocfilehash: f72fa5cc50ab6aa5447e3af9fabc365457c82973
ms.sourcegitcommit: 22bca85c3c6d946083d3784f72e886c068d49f4a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/06/2018
ms.locfileid: "22027685"
---
# <a name="use-transport-rules-to-configure-bulk-email-filtering"></a>전송 규칙을 사용 하 여 대량 전자 메일 필터링을 구성 하려면

기본 스팸 콘텐츠 필터 정책을 사용 하 여 스팸 및 대량 전자 메일에 대 한 회사 전체의 콘텐츠 필터를 설정할 수 있습니다. 콘텐츠 필터 정책을 설정 하는 방법에 [스팸 필터 정책 구성](configure-your-spam-filter-policies.md) 및 [Set-hostedcontentfilterpolicy](http://technet.microsoft.com/library/f597aa65-baa7-49d0-8832-2a300073f211.aspx) 체크아웃 합니다. 
  
대량으로 메시지를 필터링 하려면 기타 옵션을 하려는 경우에 텍스트 패턴이 나 대량 전자 메일에서 자주 발생 하는 구를 검색 하는 Exchange 전송 규칙을 만들 수 있습니다. 이러한 특성을 포함 하는 모든 메시지는 스팸으로 표시 됩니다. 이러한 규칙을 사용 하 여 조직에서 받을 원치 않는 대량 전자 메일의 양을 줄일 수 있습니다.
  
> [!NOTE]
> 이 항목을 문서화 전송 규칙 만들기 (영문), 전에 먼저 읽어보는 것이 좋습니다 [정크 메일과 대량 전자 메일의 차이점은 무엇입니까?](what-s-the-difference-between-junk-email-and-bulk-email.md) 및 [대량 불만 수준 값](bulk-complaint-level-values.md)입니다. 
  
> [!NOTE]
> 다음 절차 전체 조직에 대 한 스팸 메시지를 표시 합니다. 그러나 조직에서 특정 받는 사람에만 이러한 규칙을 적용할 다른 조건을 추가할 수 있습니다. 이와 같은 방식이으로 소수의 사용자에 게 매우를 사용 하 여 대상 지정 필터링 설정을 적용할 수 적극적으로 대량 전자 메일 사용자 (대개 에이전트는 로그인에 대 한 대량 전자 메일을 가져오기 위해)의 나머지 부분 하는 동안 되지 않은 영향을 받습니다. 
  
### <a name="create-an-exchange-transport-rule-to-filter-bulk-email-messages-based-on-text-patterns"></a>텍스트 패턴에 따라 대량 전자 메일 메시지를 필터링하는 Exchange 전송 규칙 만들기

1. EAC(Exchange 관리 센터)에서 **메일 흐름** \> **규칙**으로 이동합니다.
    
2. **추가**![아이콘 추가](media/ITPro-EAC-AddIcon.png)를 클릭한 다음 **새 규칙 만들기**를 선택합니다.
    
3. 규칙 이름을 지정합니다.
    
4. **기타 옵션**을 클릭 합니다. **하는 경우이 규칙 적용**에서 **제목이 나 본문** 선택 \> **제목이 나 본문에 다음 텍스트 패턴과 일치**합니다.
    
5. **단어 또는 구 지정** 대화 상자에 대량 전자 메일에서 일반적으로 발견되는 다음 정규식을 한 번에 하나씩 추가하고 작업을 마치면 **확인**을 클릭합니다. 
    
  - 이 전자 메일의 내용을 볼 수 없는 경우\,
    
  - \\>(safe )?구독 취소( here)?\\</a\\>
    
  - 이러한 메일을 더 이상 받지 않으려면\,
    
  - \\<img height\="?1"? width\="?1"? src\=.?http\://
    
  - 이러한 \s+전자 메일의 수신을 중지하려면\:http\://
    
  - 구독을 취소하려면 \w+ (e\-?letter|e?-?mail|newsletter)
    
  - 더 이상 (wish )?(to )?(be sent|receive) \w+ email
    
  - 이 전자 메일의 내용을 볼 수 없는 경우\, 여기를 클릭하십시오
    
  - (your daily deals|our e-?mails)의 수신을 확인하려면\,
    
  - 이러한 메일을 더 이상 받지 않으려면
    
  - (subscription preferences|preferences or unsubscribe)을(를) 변경하려면
    
  - 구독을 취소하려면 (here to|the)을(를) 클릭
    
    **참고:**
    
  - 위 목록에는 대량 전자 메일;에서 발견 되는 정규식의 광범위 한 집합 되지 않습니다. 더 추가 하거나 제거할 수 필요에 따라 합니다. 그러나 것이 좋은 시작점입니다.
    
  - 단어 또는 제목에 텍스트 패턴 또는 메시지에 다른 헤더 필드에 대 한 검색 한 *후* 메시지 인코딩 방법 ASCII 텍스트에서 SMTP 서버 간의 이진 메시지를 전송 하는데 사용 된 MIME 콘텐츠 전송에서 디코딩된 되었는지가 발생 합니다. 원시에 대 한 검색 조건 또는 예외를 사용할 수 없습니다 (일반적으로 Base64) 인코딩된 제목 또는 메시지에 다른 헤더 필드의 값입니다. 
    
6. **다음 작업 실행**에서 **메시지 속성 수정** \> **SCL(스팸 지수) 설정**을 선택합니다.
    
7. **SCL 지정** 대화 상자에서 SCL을 **5**, **6** 또는 **9**로 설정하고 **확인**을 클릭합니다.
    
    SCL를 5 또는 6 인치로 설정 **스팸** 동작을 설정 하는 동안 9 SCL **높은 정확도 스팸** 에서 작업을 수행, 콘텐츠 필터 정책에 구성 된 대로 합니다. 서비스는 콘텐츠 필터 정책에 설정 된 작업을 수행 합니다. 받는 사람의 정크 메일 폴더로 메시지를 제공 하기 위해 기본 작업 이지만 [스팸 필터 정책 구성](configure-your-spam-filter-policies.md)의 설명에 따라 다른 작업을 구성할 수 있습니다.
    
    > [!NOTE]
    > 전송 규칙과 일치를 사용 하 여 하며 대화할 수를 통해 또는 최종 사용자 스팸 격리에서으로 메시지 관리자가 격리로 전송 됩니다를 받는 사람의 정크 메일 폴더로 전송 하는 것이 아니라는 메시지를 격리 하 여 구성 된 작업의 경우 최종 사용자 스팸 알림입니다. 
  
    서비스의 SCL 값에 대한 자세한 내용은 [스팸 신뢰 수준](spam-confidence-levels.md)를 참조하세요.
    
8. 규칙을 저장합니다.
    
### <a name="create-an-exchange-transport-rule-to-filter-bulk-email-messages-based-on-phrases"></a>구에 따라 대량 전자 메일 메시지를 필터링하는 Exchange 전송 규칙 만들기

1. EAC에서 **메일 흐름** \> **규칙**으로 이동합니다.
    
2. **추가**![아이콘 추가](media/ITPro-EAC-AddIcon.png)를 클릭한 다음 **새 규칙 만들기**를 선택합니다.
    
3. 규칙 이름을 지정합니다.
    
4. **기타 옵션**을 클릭 합니다. **하는 경우이 규칙 적용**에서 **제목이 나 본문** 선택 \> **제목이 나 본문에 다음이 단어 중 하나라도 포함**합니다.
    
5. **단어 또는 구 지정** 대화 상자에 대량 전자 메일에서 일반적으로 발견되는 다음 구를 한 번에 하나씩 추가하고 작업을 마치면 **확인**을 클릭합니다. 
    
  - 기본 설정을 변경하거나 구독을 취소하려면
    
  - 전자 메일 기본 설정을 수정하거나 구독을 취소하려면
    
  - 이것은 홍보 메일입니다
    
  - 이것은 구독을 요청한 사용자에게 제공되는 메일입니다
    
  - 구독을 취소하려면 여기를 클릭
    
  - 이 전자 메일은 구독을 요청했기 때문에 제공된 것입니다
    
  - 전자 메일 뉴스레터를 더 이상 받지 않으려면
    
  - 이 뉴스레터에서 구독을 취소하려면
    
  - 이 전자 메일을 보는 데 문제가 있는 경우
    
  - 이것은 광고 메일입니다
    
  - 구독을 취소하거나
    
  - 이 전자 메일을 웹 페이지로 보려면
    
  - 구독한 경우에 제공되는 메일입니다
    
    **참고**: 다시이 목록 되어있지 대량 전자 메일;에서 발견 되는 구의 광범위 한 집합 더 추가 하거나 제거할 수 필요에 따라 합니다. 그러나 것이 좋은 시작점입니다.
    
6. **다음 작업 실행**에서 **메시지 속성 수정** \> **SCL(스팸 지수) 설정**을 선택합니다.
    
7. **SCL 지정** 대화 상자에서 SCL을 **5**, **6** 또는 **9**로 설정하고 **확인**을 클릭합니다.
    
    SCL를 5 또는 6 인치로 설정 **스팸** 동작을 설정 하는 동안 9 SCL **높은 정확도 스팸** 에서 작업을 수행, 콘텐츠 필터 정책에 구성 된 대로 합니다. 서비스는 콘텐츠 필터 정책에 설정 된 작업을 수행 합니다. 받는 사람의 정크 메일 폴더로 메시지를 제공 하기 위해 기본 작업 이지만 [스팸 필터 정책 구성](configure-your-spam-filter-policies.md)의 설명에 따라 다른 작업을 구성할 수 있습니다.
    
    > [!NOTE]
    > 전송 규칙과 일치를 사용 하 여 하며 대화할 수를 통해 또는 최종 사용자 스팸 격리에서으로 메시지 관리자가 격리로 전송 됩니다를 받는 사람의 정크 메일 폴더로 전송 하는 것이 아니라는 메시지를 격리 하 여 구성 된 작업의 경우 최종 사용자 스팸 알림입니다. 
  
    서비스의 SCL 값에 대한 자세한 내용은 [스팸 신뢰 수준](spam-confidence-levels.md)를 참조하세요.
    
8. 규칙을 저장합니다.
    
## <a name="for-more-information"></a>자세한 내용

[정크 메일과 대량 전자 메일의 차이점](what-s-the-difference-between-junk-email-and-bulk-email.md)
  
[대량 불만 수준 값](bulk-complaint-level-values.md)
  
[스팸 필터 정책 구성](configure-your-spam-filter-policies.md)
  
[고급 스팸 필터링 옵션](advanced-spam-filtering-asf-options.md)
  

