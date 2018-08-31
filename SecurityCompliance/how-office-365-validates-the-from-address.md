---
title: Office 365 피싱 방지 하기 위해 보낸사람 주소를 확인 하는 방법
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 10/11/2017
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- OWC150
- MET150
ms.assetid: eef8408b-54d3-4d7d-9cf7-ad2af10b2e0e
description: '피싱을 방지 하려면 Office 365 및 Outlook.com 이제 필요에 대 한 RFC 준수에서: 주소입니다.'
ms.openlocfilehash: 562e08aa54cb6544beccb6f0e8760735f67b834b
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22532938"
---
# <a name="how-office-365-validates-the-from-address-to-prevent-phishing"></a>Office 365 피싱 방지 하기 위해 보낸사람 주소를 확인 하는 방법

Office 365와 Outlook.com 전자 메일 계정을 피싱 공격 수가 점점 많은 받습니다. From에 대 한 값이 있는 메시지를 보낼 피셔를 사용 하는 방법 중 하나는: [RFC 5322](https://tools.ietf.org/html/rfc5322)와 호환 되지 않은 주소입니다. From: 주소는 5322.From 주소를 라고도 합니다. Office 365 및 Outlook.com 필요 서비스에서 받은 메시지에 게는 RFC 규격를 포함 하도록이 유형의 피싱을 방지 하려면에서:이 문서에서 설명한 것 처럼 처리 합니다.
  
> [!NOTE]
> 이 문서의 정보는 일반 형식의 전자 메일 주소를 기본적으로 이해 해야 합니다. 자세한 내용은 [RFC 5322](https://tools.ietf.org/html/rfc5322) (특히 3.2.3, 3.4, 및 섹션 3.4.1), [RFC 5321](https://tools.ietf.org/html/rfc5321) [RFC 3696](https://tools.ietf.org/html/rfc3696)을 참조 하십시오. 이 문서는 5322.From 주소에 대 한 정책 적용 하는 방법에 대 한 합니다. 이 문서는 5321.MailFrom 주소에 대 한 없습니다. 
  
그러나 중인 있으면 인터넷에서 계속 해 서 "합법적인" 전자 메일 메시지는 누락 된 있는 보내기 일부 레거시 전자 메일 서버에서 잘못 된 또는: 주소입니다. 정기적으로 이러한 레거시 시스템을 사용 하는 조직에서 전자 메일을 수신, 현대 보안 표준을 준수 하는 메일 서버를 업데이트 하려면 이러한 조직의 것을 권장 합니다.
  
Microsoft는 2017 년 11 월 9에서이 문서에 설명 된 정책 적용 롤아웃 시작 됩니다.
  
## <a name="how-office-365-enforces-the-use-of-a-valid-from-address-to-prevent-phishing-attacks"></a>Office 365에서 유효한의 사용을 적용 하는 방법: 피싱 공격을 방지 하기 위해 주소

Office 365가 변경 From의 사용을 적용 하는 방식에 작업을 수행: 향상 하기 위해 받는 메시지에 주소 피싱 공격 으로부터 사용자를 보호 합니다. 이 문서의 내용
  
- [모든 메시지에서 유효한 포함 해야: 주소](how-office-365-validates-the-from-address.md#MustIncludeFromAddress)
    
- [모든 메시지에서 유효한 포함 해야: 주소](how-office-365-validates-the-from-address.md#MustIncludeFromAddress)
    
- [From의 형식: 표시 이름을 포함 하지 않으면 주소](how-office-365-validates-the-from-address.md#FormatNoDisplayName)
    
- [From의 형식: 주소 표시 이름을 포함 하는 경우](how-office-365-validates-the-from-address.md#FormatDisplayName)
    
- [유효 하지 않은의 추가 예: 주소](how-office-365-validates-the-from-address.md#Examples)
    
- [From을 위반 하지 않고 자동 회신 메시지를 사용자 지정 도메인을 표시 안함: 정책](how-office-365-validates-the-from-address.md#SuppressAutoReply)
    
- [Office 365에서 재정의: 적용 정책 처리](how-office-365-validates-the-from-address.md#Override)
    
- [방지 하 고 Office 365의 cybercrimes 보호 하는 다른 방법](how-office-365-validates-the-from-address.md#OtherProtection)
    
Terry Zink 블로그 읽기에 대 한 자세한 내용은 이러한 변경에 의해 영향을 받지 않습니다 다른 사용자 대신 보내기 "[수행의 의미는 전자 메일의 '보낸'를 언급할 때?](https://blogs.msdn.microsoft.com/tzink/2017/06/22/what-do-we-mean-when-we-refer-to-the-sender-of-an-email/)"입니다.
  
### <a name="all-messages-must-include-a-valid-from-address"></a>모든 메시지에서 유효한 포함 해야: 주소
<a name="MustIncludeFromAddress"> </a>

일부 자동화 된 메시지를 보낸을 포함 하지 않습니다: 전송 하는 경우를 처리 합니다. Office 365 또는 Outlook.com From 없이 메시지를 받을 때 이전에: 주소, 서비스에서 다음과 같은 기본 추가: 결과물 확인 하기 위해 메시지에 주소:
  
```
From: <>
```

2017 년 11 월 9, 시작 Office 365가 될 롤아웃 변경 내용을 새 규칙을 적용 하는 해당 데이터 센터 및 메일 서버에 있는 From 없이 메시지: 주소는 Office 365 또는 Outlook.com에서 더이상 허용 됩니다. 대신 Office 365에서 받은 모든 메시지 이미 포함 되어 있어야에서 유효한: 주소입니다. 그렇지 않은 경우 Outlook.com 및 Office 365의 정크 메일 또는 지운 편지함 폴더에 메시지를 전송 됩니다. 
  
### <a name="syntax-overview-valid-format-for-the-from-address-for-office-365"></a>구문 개요: From에 대 한 유효한 형식: Office 365에 대 한 주소
<a name="SyntaxOverviewFromAddress"> </a>

From 값에 대 한 형식: 주소 여러 Rfc 별 자세히 정의 됩니다. 주소 지정 하 고 유효한 지 여부에 간주할 수에 다음과 같은 여러 가지가 있습니다. 단순하게 유지 하는 다음과 같은 형식 및 정의 사용 하는 것이 좋습니다.
  
```
From: "displayname " <emailaddress >
```

여기서 각 부분이 나타내는 의미는 다음과 같습니다.
  
- (선택 사항)  *displayname* 은 전자 메일 주소의 소유자를 설명 하는 구문입니다. 예,이 기능이 필요할 수는 사서함의 이름 보다 보낸사람을 설명 하기 위해 보다 친숙 한 이름입니다. 표시 이름을 사용 하는 것은 선택 사항입니다. 그러나 표시 이름을 사용 하려는 하면 항상 묶어야 따옴표와 같이 것이 좋습니다. 
    
- (필수)  *emailaddress* 으로 이루어집니다. 
    
  ```
  local-part @domain
  ```

    여기서 각 부분이 나타내는 의미는 다음과 같습니다.
    
  - (필수)  *로컬-* 부분은 주소와 연결 된 사서함을 식별 하는 문자열입니다. 이 도메인 내에서 고유 합니다. 자주, 사서함 소유자의 사용자 이름 또는 GUID를 값으로 사용 로컬 부분에 대 한 합니다. 
    
  - (필수)  *도메인* 의 전자 메일 주소 중 로컬 부분으로 식별 된 사서함을 호스트 하는 메일 서버의 정규화 된 도메인 이름 (FQDN)은. 
    
### <a name="format-of-the-from-address-if-you-dont-include-a-display-name"></a>From의 형식: 표시 이름을 포함 하지 않으면 주소
<a name="FormatNoDisplayName"> </a>

A에서 올바르게 포맷: 주소는 표시 이름이 포함 되지 않은 단일 전자 메일 주소를 함께 또는 따로 꺾쇠 괄호를 포함 합니다. 공백으로 꺾쇠 괄호를 구분 하지 않는 것이 좋습니다. 또한 하지 뒤에 포함 아무것도 전자 메일 주소입니다.
  
다음 예는 유효 합니다.
  
```
From: sender@contoso.com
```

```
From: <sender@contoso.com>
```

다음 예제에서는 유효 하지만 꺾쇠 괄호와 전자 메일 주소 사이 공백이 포함 되어 있으므로 권장 되지:
  
```
From: < sender@contoso.com >
```

다음 예제에서는 전자 메일 주소 다음 텍스트를 포함 하기 때문에 유효 하지 않습니다.
  
```
From: "Office 365" <sender@contoso.com> (Sent by a process)
```

### <a name="format-of-the-from-address-if-you-include-a-display-name"></a>From의 형식: 주소 표시 이름을 포함 하는 경우
<a name="FormatDisplayName"> </a>

에 대 한에서: 표시 이름에 대 한 값이 포함 된 주소, 다음 규칙이 적용 됩니다.
  
- 보낸사람 주소 표시 이름을 포함 하는 경우 표시 이름에 쉼표가 포함 표시 이름은 따옴표로 묶을 수 해야 합니다. 예를 들어:
    
    다음 예제에서는 유효 합니다.
    
  ```
  From: "Sender, Example" <sender.example@contoso.com>
  ```

    다음 예제에서는 유효 하지 않습니다.
    
  ```
  From: Sender, Example <sender.example@contoso.com>
  ```

    해당 표시 이름에 쉼표를 포함 하는 경우 표시 이름을 따옴표로 하지 구분 RFC 5322에 따라 올바르지 않습니다.
    
    최상의 방법으로 put 인용 부호에 관계 없이 표시 이름 주위 있는지 여부는 표시 이름 내에 쉼표를 합니다.
    
- 표시 이름을 포함 하는 보낸사람 주소, 전자 메일 주소 꺾쇠 괄호 안에 묶을 수 있어야 합니다.
    
    최상의 방법으로 Microsoft 표시 이름 및 전자 메일 주소 사이 공백을 삽입 하는 강력 하 게 권장 합니다.
    
### <a name="additional-examples-of-valid-and-invalid-from-addresses"></a>유효 하지 않은의 추가 예: 주소
<a name="Examples"> </a>

- 유효 합니다.
    
  ```
  From: "Office 365" <sender@contoso.com>
  ```

- 올바르지 않음. 전자 메일 주소는 꺾쇠 괄호와 묶지 않았습니다.
    
  ```
  From: Office 365 sender@contoso.com
  ```

- 유효 하지만 권장 하지는 않습니다. 표시 이름에 따옴표 않습니다. 표시 이름 주위에 따옴표를 항상 배치 것이 가장 좋습니다.
    
  ```
  From: Office 365 <sender@contoso.com>
  ```

- 올바르지 않음. 모든 작업은 사이 포함 된 따옴표, 표시 이름 뿐아니라:
    
  ```
  From: "Office 365 <sender@contoso.com>"
  ```

- 올바르지 않음. 전자 메일 주소 주위 없는 꺾쇠 괄호 가지가 있습니다.
    
  ```
  From: "Office 365 <sender@contoso.com>" sender@contoso.com
  ```

- 올바르지 않음. 표시 이름 및 왼쪽된 꺾쇠 괄호 사이의 공간이 없습니다.
    
  ```
  From: Office 365<sender@contoso.com>
  ```

- 올바르지 않음. 표시 이름 주위 열린 닫는 인용 부호가 왼쪽된 꺾쇠 괄호 사이의 공간이 없습니다.
    
  ```
  From: "Office 365"<sender@contoso.com>
  ```

### <a name="suppress-auto-replies-to-your-custom-domain-without-breaking-the-from-policy"></a>From을 위반 하지 않고 자동 회신 메시지를 사용자 지정 도메인을 표시 안함: 정책
<a name="SuppressAutoReply"> </a>

새로 만들기와: 정책 적용 더 이상에서 사용할 수 없습니다: \< \> 자동 회신을 표시 하지 않으려면 합니다. 대신, 사용자 지정 도메인에 대 한 null MX 레코드를 설정 해야 합니다.
  
메일 교환기 (MX) 레코드를 도메인에 대 한 메일을 받는 메일 서버를 식별 하는 DNS에 리소스 레코드를입니다. 자동 회신 (및 모든 회신) 응답 하는 서버가 메시지를 보낼 수 있는 게시 된 주소가 되지 않으므로 억제 원활 하 게 됩니다.
  
설정할 때 null MX 레코드를 사용자 지정 도메인에 대 한:
  
- 도메인 선택에 맞지 않는 메시지를 보내며를 () 전자 메일을 받게 됩니다. 예: contoso.com에서 기본 도메인을 사용 하는 경우 noreply.contoso.com를 선택할 수 있습니다.
    
- 도메인에 대 한 null MX 레코드를 설정 합니다. Null MX 레코드는 단일 점을 사용 하 고 프로그램의 같이 구성 됩니다.
    
  ```
  noreply.contoso.com IN MX .
  ```

Null MX를 게시 하는 방법에 대 한 자세한 내용은 [RFC 7505](https://tools.ietf.org/html/rfc7505)을 참조 하십시오.
  
### <a name="overriding-the-office-365-from-address-enforcement-policy"></a>Office 365에서 재정의: 적용 정책 처리
<a name="Override"> </a>

새 정책은 roll 완료 되 면 다음 방법 중 하나를 사용 하 여 Office 365에서 수신 되는 인바운드 메일에 대 한이 정책을 건너뛸 수 있습니다. 
  
- IP 허용 목록
    
- Exchange Online 메일 흐름 규칙
    
From의 적용을 재정의 하는 것에 대 한 Microsoft 권장: 정책입니다. 이 정책을 재정의 스팸에 대 한 노출, 피싱, 및 기타 cybercrimes 조직의 위험을 높일 수 있습니다.
  
Office 365에서 보내는 아웃 바운드 메일에 대 한이 정책을 재정의할 수 없습니다. 또한 Outlook.com 지원 통한 경우에 어떤 종류의 재정의 허용 하지 않습니다. 
  
### <a name="other-ways-to-prevent-and-protect-against-cybercrimes-in-office-365"></a>방지 하 고 Office 365의 cybercrimes 보호 하는 다른 방법
<a name="OtherProtection"> </a>

피싱 같은 cybercrimes에 대 한 조직을 강화할 수는 방법에 대 한 자세한 내용은 스팸, 데이터 침해 및 기타 위협 요소는 [Office 365에 대 한 보안 모범 사례](https://support.office.com/article/9295e396-e53d-49b9-ae9b-0b5828cdedc3)를 참조 합니다.
  
## <a name="related-topics"></a>관련 항목

[후방 분산 메시지 및 EOP](https://technet.microsoft.com/en-us/library/dn499795%28v=exchg.150%29.aspx)
  

