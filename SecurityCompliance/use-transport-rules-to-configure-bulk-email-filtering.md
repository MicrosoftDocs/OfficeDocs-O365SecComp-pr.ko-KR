---
title: 메일 흐름 규칙을 사용 하 여 Exchange Online Protection에서 대량 전자 메일 필터링 구성
ms.author: tracyp
author: MSFTTracyP
manager: laurawi
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 2889c82e-fab0-4e85-87b0-b001b2ccd4f7
ms.collection:
- M365-security-compliance
description: 관리자는 대량 전자 메일 필터링에 대해 Exchange Online Protection의 메일 흐름 규칙을 사용 하는 방법에 대해 알아봅니다.
ms.openlocfilehash: 43f0af6fe41bc7f8f4a62d0d87dbd825fb868f7b
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32267015"
---
# <a name="use-mail-flow-rules-to-configure-bulk-email-filtering-in-exchange-online-protection"></a>메일 흐름 규칙을 사용 하 여 Exchange Online Protection에서 대량 전자 메일 필터링 구성

기본 스팸 콘텐츠 필터 정책을 사용 하 여 스팸 및 대량 전자 메일에 대 한 회사 전체의 콘텐츠 필터를 설정할 수 있습니다. 이 문서에서는 [스팸 필터 정책 구성](configure-your-spam-filter-policies.md) 및 [get-hostedcontentfilterpolicy](https://docs.microsoft.com/powershell/module/exchange/antispam-antimalware/Set-HostedContentFilterPolicy?view=exchange-ps) 에서 콘텐츠 필터 정책을 설정 하는 방법에 대 한 설정을 확인 합니다. 
  
대량 메시지를 필터링 하는 더 많은 옵션을 원하는 경우 메일 흐름 규칙 (전송 규칙이 라고도 함)을 만들어 대량 전자 메일에서 자주 발견 되는 텍스트 패턴이 나 구를 검색할 수 있습니다. 이러한 특성을 포함 하는 모든 메시지는 스팸으로 표시 됩니다. 이러한 규칙을 사용하면 조직에 수신되는 원치 않는 대량 전자 메일을 줄일 수 있습니다.

> [!IMPORTANT]
> 이 항목에서 설명 하는 메일 흐름 규칙을 만들기 전에 먼저 [정크 메일과 대량 전자 메일의 차이점](what-s-the-difference-between-junk-email-and-bulk-email.md) 을 읽고, [대량 불만 수준 값](bulk-complaint-level-values.md)을 확인 하는 것이 좋습니다.<br> 다음 절차에서는 메시지를 전체 조직에 대한 스팸으로 표시합니다. 그러나 다른 조건을 추가하여 조직의 특정 받는 사람에게만 이러한 규칙을 적용할 수 있습니다. 이러한 방식으로 대상이 높은 대규모 전자 메일 필터링 설정은 소수의 사용자에 게 적용할 수 있지만, 사용자의 나머지 (대부분의 경우 대량 전자 메일을 가장 많이 받는 사람)에는 영향을 주지 않습니다. 
  
## <a name="create-a-mail-flow-rule-to-filter-bulk-email-messages-based-on-text-patterns"></a>텍스트 패턴에 따라 대량 전자 메일 메시지를 필터링 하는 메일 흐름 규칙 만들기

1. EAC(Exchange 관리 센터)에서 **메일 흐름** \> **규칙**으로 이동합니다.
    
2. 추가 아이콘](media/ITPro-EAC-AddIcon.gif) 추가를 클릭 한 다음 **새 규칙 만들기**를 선택 합니다. **** ![
    
3. 규칙 이름을 지정합니다.
    
4. **기타 옵션**을 클릭합니다. 다음의 **경우이 규칙 적용**에서 **제목 또는 본문** \> **제목 또는 본문이 다음 텍스트 패턴과 일치 하는 항목**을 선택 합니다.
    
5. **단어 또는 구 지정** 대화 상자에 대량 전자 메일에서 일반적으로 발견되는 다음 정규식을 한 번에 하나씩 추가하고 작업을 마치면 **확인**을 클릭합니다. 
    
   - `If you are unable to view the content of this email\, please`
    
   - `\>(safe )?unsubscribe( here)?\</a\>`
    
   - `If you do not wish to receive further communications like this\, please`
    
   - `\<img height\="?1"? width\="?1"? sr\c=.?http\://`
    
   - `To stop receiving these+emails\:http\://`
    
   - `To unsubscribe from \w+ (e\-?letter|e?-?mail|newsletter)`
    
   - `no longer (wish )?(to )?(be sent|receive) w+ email`
    
   - `If you are unable to view the content of this email\, please click here`
    
   - `To ensure you receive (your daily deals|our e-?mails)\, add`
    
   - `If you no longer wish to receive these emails`
    
   - `to change your (subscription preferences|preferences or unsubscribe)`
    
   - `click (here to|the) unsubscribe`
    
   위의 목록은 대량 전자 메일에서 발견 되는 일반 정규식 집합입니다. 필요에 따라 추가 하거나 제거할 수 있습니다. 그러나 이 목록에서 시작하는 것이 좋습니다.<br>ASCII 텍스트의 SMTP 서버 간에 이진 메시지를 전송 하는 데 사용 된 MIME 콘텐츠 전송 인코딩 방법 으로부터 메시지를 디코딩 *한 후* 메시지의 제목 또는 기타 헤더 필드에 대 한 단어 또는 텍스트 패턴 검색을 수행 합니다. 조건이나 예외를 사용하여 메시지의 제목이나 다른 머리글 필드에 있는 원시(일반적으로, Base64) 인코딩된 값을 검색할 수 없습니다. 
    
6. **다음 작업 실행**에서 **메시지 속성 수정** \> **SCL(스팸 지수) 설정**을 선택합니다.
    
7. **SCL 지정** 대화 상자에서 SCL을 **5**, **6** 또는 **9**로 설정하고 **확인**을 클릭합니다.
    
   SCL을 5 또는 6으로 설정하면 **스팸** 동작이 수행되지만 SCL을 9로 설정하면 콘텐츠 필터 정책에 구성된 대로 **높은 정확도 스팸** 작업이 수행됩니다. 서비스는 콘텐츠 필터 정책에 설정된 작업을 수행합니다. 기본 작업은 받는 사람의 정크 메일 폴더로 메시지를 배달 하는 것 이지만, [스팸 필터 정책 구성](configure-your-spam-filter-policies.md)에 설명 된 대로 다른 작업을 구성할 수도 있습니다.
    
   메시지를 받는 사람의 정크 메일 폴더로 보내지 않고 격리 하는 작업을 수행 하는 경우 메시지는 메일 흐름 규칙 일치로 관리자 격리로 보내지며 최종 사용자 스팸 격리 또는 최종 사용자에 게는 제공 되지 않습니다. 스팸 알림 
  
   서비스의 SCL 값에 대한 자세한 내용은 [스팸 신뢰 수준](spam-confidence-levels.md)를 참조하세요.
    
8. 규칙을 저장합니다.
    
## <a name="create-a-mail-flow-rule-to-filter-bulk-email-messages-based-on-phrases"></a>구에 따라 대량 전자 메일 메시지를 필터링 하는 메일 흐름 규칙 만들기

1. EAC에서 **메일 흐름** \> **규칙**으로 이동합니다.
    
2. 추가 아이콘](media/ITPro-EAC-AddIcon.gif) 추가를 클릭 한 다음 **새 규칙 만들기**를 선택 합니다. **** ![
    
3. 규칙 이름을 지정합니다.
    
4. **기타 옵션**을 클릭합니다. 다음의 **경우이 규칙 적용**에서 **제목 또는 본문** \> 에 **다음 단어 포함 또는 본문**을 선택 합니다.
    
5. **단어 또는 구 지정** 대화 상자에 대량 전자 메일에서 일반적으로 발견되는 다음 구를 한 번에 하나씩 추가하고 작업을 마치면 **확인**을 클릭합니다. 
    
   - `to change your preferences or unsubscribe`
    
   - `Modify email preferences or unsubscribe`
    
   - `This is a promotional email`
    
   - `You are receiving this email because you requested a subscription`
    
   - `click here to unsubscribe`
    
   - `You have received this email because you are subscribed`
    
   - `If you no longer wish to receive our email newsletter`
    
   - `to unsubscribe from this newsletter`
    
   - `If you have trouble viewing this email`
    
   - `This is an advertisement`
    
   - `you would like to unsubscribe or change your`
    
   - `view this email as a webpage`
    
   - `You are receiving this email because you are subscribed`
    
   이 목록은 대량 전자 메일에서 발견 되는 포괄적인 구 집합이 아닙니다. 필요에 따라 추가 하거나 제거할 수 있습니다. 그러나 이 목록에서 시작하는 것이 좋습니다.
    
6. **다음 작업 실행**에서 **메시지 속성 수정** \> **SCL(스팸 지수) 설정**을 선택합니다.
    
7. **SCL 지정** 대화 상자에서 SCL을 **5**, **6** 또는 **9**로 설정하고 **확인**을 클릭합니다.
    
   SCL을 5 또는 6으로 설정하면 **스팸** 동작이 수행되지만 SCL을 9로 설정하면 콘텐츠 필터 정책에 구성된 대로 **높은 정확도 스팸** 작업이 수행됩니다. 서비스는 콘텐츠 필터 정책에 설정된 작업을 수행합니다. 기본 작업은 받는 사람의 정크 메일 폴더로 메시지를 배달 하는 것 이지만, [스팸 필터 정책 구성](configure-your-spam-filter-policies.md)에 설명 된 대로 다른 작업을 구성할 수도 있습니다.
    
   메시지를 받는 사람의 정크 메일 폴더로 보내지 않고 격리 하는 작업을 수행 하는 경우 메시지는 메일 흐름 규칙 일치로 관리자 격리로 보내지며 최종 사용자 스팸 격리 또는 최종 사용자에 게는 제공 되지 않습니다. 스팸 알림 
  
   서비스의 SCL 값에 대한 자세한 내용은 [스팸 신뢰 수준](spam-confidence-levels.md)를 참조하세요.

8. 규칙을 저장합니다.

## <a name="for-more-information"></a>자세한 내용

[정크 메일과 대량 전자 메일의 차이점](what-s-the-difference-between-junk-email-and-bulk-email.md)

[대량 불만 수준 값](bulk-complaint-level-values.md)

[스팸 필터 정책 구성](configure-your-spam-filter-policies.md)

[고급 스팸 필터링 옵션](advanced-spam-filtering-asf-options.md)
