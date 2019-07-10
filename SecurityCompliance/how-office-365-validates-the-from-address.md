---
title: Office 365에서 보낸 사람 주소의 유효성을 검사 하 여 피싱을 방지 하는 방법
ms.author: tracyp
author: MSFTTracyp
manager: dansimp
ms.date: 10/11/2017
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- OWC150
- MET150
ms.assetid: eef8408b-54d3-4d7d-9cf7-ad2af10b2e0e
ms.collection:
- M365-security-compliance
description: '피싱 방지를 위해 Office 365 및 Outlook.com에는 이제 From: 주소에 대 한 RFC 준수가 필요 합니다.'
ms.openlocfilehash: 39c9898a31c715487f3bc934ad0986e9a7b3679d
ms.sourcegitcommit: 32ecff689ae32c59a39b7633ca0f36a304e7516e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/09/2019
ms.locfileid: "35599134"
---
# <a name="how-office-365-validates-the-from-address-to-prevent-phishing"></a>Office 365에서 보낸 사람 주소의 유효성을 검사 하 여 피싱을 방지 하는 방법

Office 365 및 Outlook.com 전자 메일 계정에는 많은 수의 피싱 공격이 수신 됩니다. Phishers을 사용 하는 한 가지 방법은 [RFC 5322](https://tools.ietf.org/html/rfc5322)을 준수 하지 않는 보낸 사람: 주소에 대 한 값이 포함 된 메시지를 보내는 것입니다. 보낸 사람: 주소는 5322.from 주소의 주소 라고도 합니다. 이러한 유형의 피싱를 방지 하기 위해 Office 365 및 Outlook.com에서는이 문서에 설명 된 대로 서비스에서 받은 메시지에 RFC 호환 From: address를 포함 해야 합니다.
  
> [!NOTE]
> 이 문서의 정보를 사용 하려면 전자 메일 주소의 일반적인 형식을 기본적으로 이해 해야 합니다. 자세한 내용은 [rfc 5322](https://tools.ietf.org/html/rfc5322) (특히 3.2.3, 3.4 및 3.4.1), [Rfc 5321](https://tools.ietf.org/html/rfc5321)및 [rfc 3696](https://tools.ietf.org/html/rfc3696)을 참조 하십시오. 이 문서에서는 5322.from 주소의 주소에 대 한 정책 적용 정보를 소개 합니다. 이 문서는 5321 보낸 사람 주소에는 해당 되지 않습니다. 
  
아쉽게도 인터넷에는 여전히 일부 레거시 전자 메일 서버가 있는데,이는 주소가 누락 되었거나 형식이 잘못 된 "합법적인" 전자 메일 메시지를 계속 전송 합니다. 이러한 레거시 시스템을 사용 하는 조직에서 정기적으로 전자 메일을 수신 하는 경우 해당 조직이 최신 보안 표준을 준수 하도록 메일 서버를 업데이트 하도록 권장 합니다.
  
Microsoft는 2017 년 11 월 9 일에이 문서에서 설명 하는 정책의 적용을 롤아웃 하기 시작 합니다.
  
## <a name="how-office-365-enforces-the-use-of-a-valid-from-address-to-prevent-phishing-attacks"></a>Office 365에서 유효한 보낸 사람 주소 사용을 적용 하 여 피싱 공격을 방지 하는 방법

Office 365은 피싱 공격 으로부터 사용자를 보호 하기 위해 받은 메시지에 보낸 사람: 주소를 사용 하도록 강제 적용 하는 방식을 변경 하는 것입니다. 이 문서의 내용
  
- [모든 메시지에는 다음의 유효한 보낸 사람: 주소가 포함 되어야 합니다.](how-office-365-validates-the-from-address.md#MustIncludeFromAddress)
    
- [보낸 사람: 주소에 표시 이름을 포함 하지 않는 경우의 형식](how-office-365-validates-the-from-address.md#FormatNoDisplayName)
    
- [보낸 사람: 주소에 표시 이름을 포함 하는 경우의 형식](how-office-365-validates-the-from-address.md#FormatDisplayName)
    
- [유효한 및 잘못 된 보낸 사람에 대 한 추가 예: 주소](how-office-365-validates-the-from-address.md#Examples)
    
- [의 출처를 끊지 않고 사용자 지정 도메인에 대 한 자동 회신을 표시 하지 않습니다.](how-office-365-validates-the-from-address.md#SuppressAutoReply)
    
- [Office 365 From: address 강요 policy 재정의](how-office-365-validates-the-from-address.md#Override)
    
- [Office 365에서 cybercrimes을 방지 하 고 보호 하는 기타 방법](how-office-365-validates-the-from-address.md#OtherProtection)
    
다른 사용자 대신 보내기는이 변경 내용에 영향을 주지 않습니다. 자세한 내용은 Terry Zink의 블로그 "[전자 메일의 ' 보낸 사람 '을 참조 하는 경우 무슨 의미 입니까?](https://blogs.msdn.microsoft.com/tzink/2017/06/22/what-do-we-mean-when-we-refer-to-the-sender-of-an-email/)"를 읽습니다.
  
### <a name="all-messages-must-include-a-valid-from-address"></a>모든 메시지에는 다음의 유효한 보낸 사람: 주소가 포함 되어야 합니다.
<a name="MustIncludeFromAddress"> </a>

일부 자동화 된 메시지는 보낸 경우에 보낸 사람: 주소를 포함 하지 않습니다. 이전의 경우 Office 365 또는 Outlook.com가 보낸 사람: 주소를 제외 하 고 메시지를 받은 경우 서비스는 다음과 같은 기본값을 메시지에 주소에 추가 하 여 it를 인도품으로 만듭니다.
  
```
From: <>
```

2017 년 11 월 9 일부터 Office 365은 데이터 센터 및 메일 서버에 대 한 변경 내용을 롤아웃하기 때문에 보낸 사람: 주소 없이 메시지가 Office 365 또는 Outlook.com에서 더 이상 수락 되지 않습니다. 대신, Office 365에서 수신 되는 모든 메시지에는 올바른 보낸 사람: 주소가 포함 되어 있어야 합니다. 그렇지 않으면 메시지가 Outlook.com 및 Office 365의 정크 메일 또는 지운 편지함 폴더에 전송 됩니다. 
  
### <a name="syntax-overview-valid-format-for-the-from-address-for-office-365"></a>구문 개요: From: address for Office 365의 유효한 형식
<a name="SyntaxOverviewFromAddress"> </a>

From: 주소 값의 형식은 여러 Rfc에서 세부 정보로 정의 됩니다. 주소 지정에는 많은 변화가 있으며 유효한 지 또는 잘못 된 것으로 간주 될 수 있습니다. 이를 단순하게 유지 하기 위해 다음 형식과 정의를 사용 하는 것이 좋습니다.
  
```
From: "displayname " <emailaddress >
```

여기서 각 부분이 나타내는 의미는 다음과 같습니다.
  
- 반드시  *displayname* 은 전자 메일 주소의 소유자를 설명 하는 구입니다. 예를 들어 사서함 이름 보다 사용자에 게 친숙 한 이름을 사용 하 여 보낸 사람을 설명할 수 있습니다. 표시 이름을 사용 하는 것은 선택 사항입니다. 그러나 표시 이름을 사용 하도록 선택 하는 경우에는 다음과 같이 항상 따옴표로 묶어야 합니다. 
    
- 않아도  *emailaddress* 는 다음으로 구성 됩니다. 
    
  ```
  local-part @domain
  ```

    여기서 각 부분이 나타내는 의미는 다음과 같습니다.
    
  - 않아도  *로컬 부분-* 주소와 연결 된 사서함을 식별 하는 문자열입니다. 이는 도메인 내에서 고유 합니다. 일반적으로 사서함 소유자의 사용자 이름 또는 GUID는 로컬 부분에 대 한 값으로 사용 됩니다. 
    
  - 않아도  *domain* 은 전자 메일 주소의 로컬 부분으로 식별 되는 사서함을 호스트 하는 메일 서버의 FQDN (정규화 된 도메인 이름)입니다. 
    
### <a name="format-of-the-from-address-if-you-dont-include-a-display-name"></a>보낸 사람: 주소에 표시 이름을 포함 하지 않는 경우의 형식
<a name="FormatNoDisplayName"> </a>

표시 이름이 포함 되지 않은 적절 한 형식의 주소에는 단일 전자 메일 주소만 포함 되거나 꺾쇠 괄호를 사용 하지 않습니다. 꺾쇠 괄호와 공백을 구분 하지 않는 것이 좋습니다. 또한 전자 메일 주소 다음에는 아무런 내용도 포함 하지 마세요.
  
다음 예제를 사용할 수 있습니다.
  
```
From: sender@contoso.com
```

```
From: <sender@contoso.com>
```

다음은 유효 하지만 꺾쇠 괄호와 전자 메일 주소 사이에 공백이 포함 되므로 권장 되지 않습니다.
  
```
From: < sender@contoso.com >
```

다음 예는 전자 메일 주소 다음에 텍스트가 포함 되어 있기 때문에 유효 하지 않습니다.
  
```
From: "Office 365" <sender@contoso.com> (Sent by a process)
```

### <a name="format-of-the-from-address-if-you-include-a-display-name"></a>보낸 사람: 주소에 표시 이름을 포함 하는 경우의 형식
<a name="FormatDisplayName"> </a>

보낸 사람: 표시 이름에 대 한 값을 포함 하는 주소에는 다음 규칙이 적용 됩니다.
  
- 보낸 사람 주소에 표시 이름이 포함 되어 있고 표시 이름에 쉼표가 포함 되어 있으면 표시 이름을 따옴표 안에 넣어야 합니다. 예를 들면 다음과 같습니다.
    
    다음 예를 사용할 수 있습니다.
    
  ```
  From: "Sender, Example" <sender.example@contoso.com>
  ```

    다음 예는 유효 하지 않습니다.
    
  ```
  From: Sender, Example <sender.example@contoso.com>
  ```

    RFC 5322에 따라 표시 이름이 쉼표를 포함 하는 경우 표시 이름을 따옴표로 묶지 않습니다.
    
    표시 이름에 쉼표가 있는지 여부에 관계 없이 표시 이름 앞뒤에 따옴표를 입력 하는 것이 좋습니다.
    
- 보낸 사람 주소에 표시 이름이 포함 된 경우 전자 메일 주소를 꺾쇠 괄호 안에 넣어야 합니다.
    
    최상의 방법으로 표시 이름과 전자 메일 주소 사이에 공백을 삽입 하는 것이 좋습니다.
    
### <a name="additional-examples-of-valid-and-invalid-from-addresses"></a>유효한 및 잘못 된 보낸 사람에 대 한 추가 예: 주소
<a name="Examples"> </a>

- 잘못
    
  ```
  From: "Office 365" <sender@contoso.com>
  ```

- 올바르지 않음. 전자 메일 주소를 꺽쇠 괄호로 묶지 않습니다.
    
  ```
  From: Office 365 sender@contoso.com
  ```

- 유효 하지만 권장 되지 않습니다. 표시 이름이 따옴표가 아닌 경우 가장 좋은 방법은 항상 표시 이름을 따옴표 앞에 추가 하는 것입니다.
    
  ```
  From: Office 365 <sender@contoso.com>
  ```

- 올바르지 않음. 표시 이름만이 아니라 인용 부호로 묶여 있는 항목은 다음과 같습니다.
    
  ```
  From: "Office 365 <sender@contoso.com>"
  ```

- 올바르지 않음. 전자 메일 주소 주변에는 꺽쇠 괄호가 없습니다.
    
  ```
  From: "Office 365 <sender@contoso.com>" sender@contoso.com
  ```

- 올바르지 않음. 표시 이름과 왼쪽 꺽쇠 괄호 사이에는 공백이 없습니다.
    
  ```
  From: Office 365<sender@contoso.com>
  ```

- 올바르지 않음. 표시 이름과 왼쪽 꺽쇠 괄호 사이에는 닫는 따옴표 사이에 공백이 없어야 합니다.
    
  ```
  From: "Office 365"<sender@contoso.com>
  ```

### <a name="suppress-auto-replies-to-your-custom-domain-without-breaking-the-from-policy"></a>의 출처를 끊지 않고 사용자 지정 도메인에 대 한 자동 회신을 표시 하지 않습니다.
<a name="SuppressAutoReply"> </a>

새로운 from: 정책 적용을 사용 하 여 다음 \< \> 위치에서 더 이상 자동 회신을 사용 하지 않을 수 있습니다. 대신 사용자 지정 도메인에 대해 null MX 레코드를 설정 해야 합니다.
  
MX (메일 교환기) 레코드는 도메인에 대 한 메일을 수신 하는 메일 서버를 식별 하는 DNS의 리소스 레코드입니다. 응답 서버가 메시지를 보낼 수 있는 게시 된 주소가 없기 때문에 자동 회신 (및 모든 응답)은 자연스럽 게 표시 되지 않습니다.
  
사용자 지정 도메인에 대해 null MX 레코드를 설정 하는 경우 다음을 수행 합니다.
  
- 전자 메일을 수락 (수신) 하지 않는 메시지를 보낼 도메인을 선택 합니다. 예를 들어 주 도메인이 contoso.com 인 경우 noreply.contoso.com을 선택할 수 있습니다.
    
- 도메인에 대해 null MX 레코드를 설정 합니다. Null MX 레코드는 다음과 같은 단일 점으로 구성 됩니다.
    
  ```
  noreply.contoso.com IN MX .
  ```

Null MX를 게시 하는 방법에 대 한 자세한 내용은 [RFC 7505](https://tools.ietf.org/html/rfc7505)을 참조 하십시오.
  
### <a name="overriding-the-office-365-from-address-enforcement-policy"></a>Office 365 From: address 강요 policy 재정의
<a name="Override"> </a>

새 정책을 완료 한 후에는 다음 방법 중 하나를 사용 하 여 Office 365에서 받은 인바운드 메일용으로이 정책만 무시할 수 있습니다. 
  
- IP 허용 목록
    
- Exchange Online 메일 흐름 규칙
    
에서의 적용을 무시 하는 것이 좋습니다. 이 정책을 재정의 하면 스팸, 피싱 및 기타 cybercrimes에 대 한 조직의 노출 위험을 높일 수 있습니다.
  
Office 365에서 보내는 아웃 바운드 메일에 대해서는이 정책을 재정의할 수 없습니다. 또한 Outlook.com에서는 지원을 통해 모든 종류의 재정의를 허용 하지 않습니다. 
  
### <a name="other-ways-to-prevent-and-protect-against-cybercrimes-in-office-365"></a>Office 365에서 cybercrimes을 방지 하 고 보호 하는 기타 방법
<a name="OtherProtection"> </a>

피싱, spamming, 데이터 위반 및 기타 위협과 같은 cybercrimes 로부터 조직을 강화 하는 방법에 대 한 자세한 내용은 [Office 365의 보안 모범 사례](https://support.office.com/article/9295e396-e53d-49b9-ae9b-0b5828cdedc3)를 참조 하세요.
  
## <a name="related-topics"></a>관련 주제

[후방 분산 메시지 및 EOP](https://technet.microsoft.com/en-us/library/dn499795%28v=exchg.150%29.aspx)
  

