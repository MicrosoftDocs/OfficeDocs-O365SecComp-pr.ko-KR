---
title: Exchange Online Protection의 메일 흐름 규칙(전송 규칙)
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 4/29/2017
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
ms.assetid: 9c2cf227-eff7-48ef-87fb-487186e47363
description: 전송 규칙이라고도 알려진 메일 흐름 규칙을 사용하여 Office 365 조직을 통과하는 메시지를 식별하고 작업을 수행할 수 있습니다.
ms.openlocfilehash: b6bd5f0510c8a9e5f5cc4679dce669b6da50f5e8
ms.sourcegitcommit: b0b0b716718c22779c7c04775b8010d65cd6656b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28723245"
---
# <a name="mail-flow-rules-transport-rules-in-exchange-online-protection"></a>Exchange Online Protection의 메일 흐름 규칙(전송 규칙)

전송 규칙이라고도 알려진 메일 흐름 규칙을 사용하여 Office 365 조직을 통과하는 메시지를 식별하고 작업을 수행할 수 있습니다. 메일 흐름 규칙은 Outlook 및 웹에서 Outlook에서 사용할 수 있는 받은 편지함 규칙과 유사합니다. 주요 차이점은 메일 흐름 규칙이 메시지가 배달된 후가 아니라 메시지가 전송 중일 때 작업을 수행한다는 것입니다. 메일 흐름 규칙에는 여러 유형의 메시징 정책을 유연하게 구현하는 데 사용할 수 있는 다양한 조건, 예외 및 작업 집합이 포함되어 있습니다.
  
이 문서에서는 메일 흐름 규칙의 구성 요소와 작동 방식을 설명합니다.
  
을 만드는 단계에 대 한 복사 하 고 메일 흐름 규칙 관리 **메일 흐름 규칙 관리를**참조 하십시오. 각 규칙에 대 한 것 적용 (영문), 테스트, 또는으로 테스트 하 고 보낸사람에 게 알리지 해야 합니다. 테스트 옵션에 대 한 자세한 내용은, **메일 흐름 규칙을 테스트** 및 **정책 팁**을 참조 하십시오.
  
메일 흐름 규칙과 일치하는 메시지에 대한 요약 및 세부 보고서를 보려면 **Use mail protection reports in Office 365 to view data about malware, spam, and rule detections**을 참조하세요.
  
메일 흐름 규칙을 사용해서 특정 메시징 정책을 실행하려면 다음 항목을 참조하세요.
  
- [Use mail flow rules to inspect message attachments in Office 365](http://technet.microsoft.com/library/874d1c78-a8ec-4938-b388-d3208c2fa971.aspx)
    
- [Office 365 Enterprise의 암호화 설정](https://support.office.com/article/e86fc991-0161-4f01-9c1c-d25e87733d06)
    
- [Organization-wide message disclaimers, signatures, footers, or headers in Office 365](http://technet.microsoft.com/library/29ac61c2-77f1-4071-b14e-8cc64e3e76ba.aspx)
    
- [Use mail flow rules to set the spam confidence level (SCL) in messages](../use-mail-flow-rules-to-set-the-spam-confidence-level-scl-in-messages.md)
    
- [Create organization-wide safe sender or blocked sender lists in Office 365](../create-organization-wide-safe-sender-or-blocked-sender-lists-in-office-365.md)
    
- [Exchange 온라인 보호의 첨부 파일 차단을 통한 맬웨어 위협 감소](reducing-malware-threats-through-file-attachment-blocking-in-exchange-online-pro.md)
    
- [전자 메일 메시지를 암호화하거나 암호를 해독하는 규칙 정의](https://go.microsoft.com/fwlink/p/?Linkid=402846)
    
다음 비디오는 Exchange Online Protection의 흐름 규칙 메일 설정의 데모를 제공합니다.
  
> [!VIDEO https://www.microsoft.com/videoplayer/embed/7cdcd2cb-9382-4065-98e1-81257b32a189?autoplay=false]
  
## <a name="mail-flow-rule-components"></a>메일 흐름 규칙 구성 요소

메일 흐름 규칙은 조건, 예외, 작업 및 속성의 이루어집니다.
  
- **조건** 수행할 작업에 적용할 메시지를 식별합니다. 일부 조건은 받는 사람, 보낸 사람, 참조 필드 등의 메시지 헤더 필드를 검사하며 다른 조건은 메시지 제목, 본문, 첨부 파일, 메시지 크기, 메시지 분류 등의 메시지 속성을 검사합니다. 대부분의 조건에는 같음, 같지 않음 또는 포함 등의 비교 연산자 및 일치시킬 값을 지정해야 합니다. 조건이나 예외가 없는 경우 규칙이 모든 메시지에 적용됩니다. 
    
    Exchange Online Protection의 메일 흐름 규칙 조건에 대 한 자세한 내용은 참조 [Exchange Online의 메일 흐름 규칙 조건 및 예외 (조건자).](https://docs.microsoft.com/en-us/exchange/security-and-compliance/mail-flow-rules/conditions-and-exceptions)합니다.
    
- **예외** 선택적으로 해당 작업이 적용되면 안 되는 메시지를 식별합니다. 조건에서 사용할 수 있는 동일한 메시지 식별자를 예외에서도 사용할 수 있습니다. 예외는 조건을 재정의하며, 메시지가 구성된 모든 조건과 일치하더라도 규칙 작업이 메시지에 적용되지 않도록 합니다. 
    
- **작업** 규칙의 조건과 일치하고 예외와는 일치하지 않는 메시지에 수행할 작업을 지정합니다. 메시지를 거부, 삭제 또는 리디렉션하거나, 받는 사람을 추가하거나, 메시지 제목에 접두사를 추가하거나, 메시지 본문에 고지 사항을 삽입하는 등 다양한 작업을 수행할 수 있습니다. 
    
    에 대 한 자세한 내용은 메일 흐름 규칙 동작 사용할 수 있는 Exchange Online Protection [메일 흐름 규칙 동작 Exchange Online Protection을](http://technet.microsoft.com/library/f8621ecb-a177-4025-9011-a6569999746a.aspx)참조 하십시오.
    
- **속성** 조건, 예외 또는 작업 되지 않은 다른 규칙 설정을 지정 합니다. 예 때 규칙을 적용할을 적용할지 또는 규칙 및 규칙 활성화 되어 기간을 테스트 합니다. 
    
     자세한 내용은이 항목의 [메일 흐름 규칙 속성](mail-flow-rules-transport-rules-0.md#Properties) 섹션을 참조 하십시오. 
    
### <a name="multiple-conditions-exceptions-and-actions"></a>여러 조건, 예외 및 작업

다음 표에는 규칙에서 여러 조건, 조건 값, 예외 및 작업이 처리되는 방식이 나와 있습니다.
  
|**구성 요소**|**논리**|**Comments**|
|:-----|:-----|:-----|
|여러 조건  <br/> |AND  <br/> |메시지는 규칙의 모든 조건과 일치해야 합니다. 하나의 조건 또는 다른 조건과 일치해야 하는 경우 각 조건에 대해 별도의 규칙을 사용합니다. 예를 들어 특정 텍스트를 포함하는 메시지 및 첨부 파일이 있는 메시지에 동일한 고지 사항을 추가하려면 각 조건에 대해 하나의 규칙을 만듭니다. EAC에서는 규칙을 쉽게 복사할 수 있습니다.  <br/> |
|값이 여러 개인 조건  <br/> |OR  <br/> |일부 조건을 사용 하면 둘 이상의 값을 지정할 수 있습니다. 메시지 (모두는 아님) 중 하나는 지정 된 값을 일치 해야 합니다. 예, 전자 메일 메시지에 제목 주식 가격 정보 하 여 **제목 단어가 포함 된 다음이 단어의** 조건은 Contoso 단어 또는 재고 항목과 일치 하도록 구성 된 경우 조건을 만족 하는 제목 중 하나 이상이 포함 하기 때문에 지정 된 값입니다.<br/> |
|여러 예외  <br/> |OR  <br/> |예외 중 하나라도 메시지와 일치하면 작업은 메시지에 적용되지 않습니다. 메시지가 모든 예외와 일치할 필요는 없습니다.  <br/> |
|여러 작업  <br/> |AND  <br/> |규칙 조건에 일치하는 메시지에는 규칙에 지정된 모든 작업이 적용됩니다. 예를 들어, **메시지 제목 앞에 다음 추가** 및 **숨은 참조란에 받는 사람 추가** 작업을 선택하면 두 작업 모두 메시지에 적용됩니다.<br/> **아무에게도 알리지 않고 메시지 삭제** 등의 일부 작업을 적용할 경우 후속 규칙이 메시지에 적용되지 않습니다. **메시지 전달** 등의 다른 작업은 추가 작업을 허용하지 않습니다.<br/> 해당 규칙이 적용될 때 후속 규칙은 메시지에 적용되지 않도록 규칙에 대해 작업을 설정할 수도 있습니다.  <br/> |
   
### <a name="mail-flow-rule-properties"></a>메일 흐름 규칙 속성
<a name="Properties"> </a>

다음 표에서 메일 흐름 규칙에서 사용할 수 있는 규칙 속성을 설명합니다.
  
|**EAC의 속성 이름**|**PowerShell에서 매개 변수 이름**|**설명**|
|:-----|:-----|:-----|
|**우선 순위** <br/> | _우선 순위_ <br/> |메시지에 규칙이 적용되는 순서를 나타냅니다. 기본 우선 순위는 규칙을 만들 때를 기준으로 합니다(이전 규칙은 새로운 규칙보다 우선 순위가 높고, 우선 순위가 높은 규칙은 우선 순위가 낮은 규칙보다 먼저 처리됨).  <br/> 규칙을 규칙 목록에서 위나 아래로 이동 하 여 EAC의 규칙 우선순위를 변경 합니다. 우선순위 수를 설정 하면 PowerShell에서 (0 가장 높은 우선순위를은).  <br/> 예를 들어 신용 카드 번호가 포함된 메시지는 거부하는 규칙과 승인을 요구하는 또 다른 규칙이 있을 때 거부 규칙이 먼저 적용되도록 한 다음 다른 규칙이 적용되지 않도록 할 수 있습니다.  |
|**Mode** <br/> | _Mode_ <br/> |규칙이 메시지 처리를 즉시 시작하도록 할지 여부 또는 메시지의 배달에 영향을 주지 않고 규칙을 테스트할지 여부를 지정할 수 있습니다(데이터 손실 방지 또는 DLP 정책 팁 사용 또는 사용 안 함).  <br/> 정책 팁 Outlook 또는 Outlook 메시지를 작성 하는 사람에 게 가능한 정책 위반 하는 방법에 대 한 정보를 제공 하는 웹에 대 한 간략 한 메모를 제공 합니다. 자세한 내용은 **정책 팁**을 참조 하십시오.<br/> 모드에 대한 자세한 내용은 **Test a mail flow rule**를 참조하세요.  <br/> |
|**다음 날짜에 이 규칙 활성화** <br/> **다음 날짜에 이 규칙 비활성화** <br/> | _ActivationDate_ <br/>  _ExpiryDate_ <br/> | 규칙이 활성화되는 날짜 범위를 지정합니다.  <br/> |
|**설정** 확인란 선택 또는 선택 취소  <br/> |새 규칙: **New-transportrule** cmdlet에서 매개 변수를 _사용_ 합니다.  <br/> 기존 규칙: **Enable-TransportRule** 또는 **Disable-TransportRule** cmdlet을 사용합니다.  <br/> 해당 값은 규칙의 **State** 속성에 표시됩니다.  <br/> |사용되지 않도록 설정된 규칙을 만들고 테스트할 준비가 되면 사용하도록 설정할 수 있습니다. 또는 규칙을 삭제하지 않고 사용하지 않도록 설정하여 설정을 유지할 수 있습니다.  <br/> |
|**규칙 처리가 완료되지 않으면 메시지 연기** <br/> | _RuleErrorAction_ <br/> |규칙 처리를 완료할 수 없는 경우 메시지를 처리할 방법을 지정할 수 있습니다. 기본적으로 규칙은 무시되지만 처리를 위해 메시지를 다시 전송하도록 선택할 수 있습니다.  <br/> |
|**메시지의 보낸 사람 주소 일치** <br/> | _SenderAddressLocation_ <br/> |규칙이 보낸 사람의 전자 메일 주소를 검사하는 조건 또는 예외를 사용하는 경우 메시지 머리글이나 메시지 봉투 또는 둘 다에 있는 값을 찾을 수 있습니다.  <br/> |
|**추가 규칙 처리 중지** <br/> | _SenderAddressLocation_ <br/> |규칙에 대한 작업이지만 EAC의 속성과 같습니다. 규칙이 메시지를 처리하면 메시지에 추가 규칙을 적용하지 않도록 선택할 수 있습니다.  <br/> |
|**Comments** <br/> | _Comments_ <br/> |  규칙에 대한 설명을 입력할 수 있습니다.  <br/> |
   
## <a name="how-mail-flow-rules-are-applied-to-messages"></a>메일 흐름 규칙은 메시지에 적용 하는 방법

조직을 통해 주고받는 모든 메시지를 조직에서 사용 가능한 메일 흐름 규칙에 대해 평가 됩니다. **메일 흐름** 에 나열 된 순서 대로 규칙은 처리 \> **규칙** EAC, 페이지 또는 PowerShell에서 해당 _Priority_ 매개 변수 값을 기반으로 합니다. 
  
또한 각 규칙은 일치할 경우 추가 규칙의 처리를 중지하는 옵션도 제공됩니다. 이 설정은 여러 메일 흐름 규칙의 조건과 일치하는 메시지에 중요합니다(메시지에 어떤 규칙을 적용할까요? 모두? 하나만?).
  
### <a name="differences-in-processing-based-on-message-type"></a>메시지 유형에 따른 처리 방식의 차이

조직을 통과하는 메시지 유형에는 몇 가지가 있습니다. 다음 표에는 메일 흐름 규칙으로 처리될 수 있는 메시지 유형이 나와 있습니다.
  
****

|**메시지 유형**|**규칙을 적용할 수 있는지 여부**|
|:-----|:-----|
|**일반 메시지** 단일 RTF(서식 있는 텍스트), HTML 또는 일반 텍스트 메시지 본문 또는 여러 부분으로 된 메시지 본문 집합이나 대체 메시지 본문 집합이 포함된 메시지입니다.  <br/> |예  <br/> |
|**Office 365 메시지 암호화 ** Office 365에서 Office 365 메시지 암호화에 의해 암호화된 메시지입니다. 자세한 내용은 [Office 365 메시지 암호화](https://go.microsoft.com/fwlink/p/?LinkId=392525)를 참조하세요.  <br/> |규칙은 항상 봉투 헤더에 액세스하여 해당 헤더를 검사하는 조건을 바탕으로 메시지를 처리할 수 있습니다.  <br/> 암호화된 메시지의 내용을 검사하거나 수정하는 규칙의 경우, 전송 암호 해독이 사용되도록 설정되어 있는지 확인해야 합니다(필수 또는 옵션. 기본값은 옵션임). 자세한 내용은 [전송 암호 해독 사용 또는 사용 안 함](https://go.microsoft.com/fwlink/p/?linkid=848060)을 참조하세요.  <br/> 암호화된 메시지의 암호를 자동으로 해독하는 규칙을 만들 수도 있습니다. 자세한 내용은 [전자 메일 메시지를 암호화하거나 암호를 해독하는 규칙 정의](https://go.microsoft.com/fwlink/p/?Linkid=402846)를 참조하세요.  <br/> |
|**S/MIME 암호화 메시지** <br/> |규칙은 봉투 헤더에 액세스하여 해당 헤더를 검사하는 조건을 바탕으로 메시지를 처리할 수만 있습니다.  <br/> 메시지 내용을 검사해야 하는 조건이 포함된 규칙이나 메시지의 내용을 수정하는 작업은 처리할 수 없습니다.  <br/> |
|**RMS 보호 메시지** Active Directory Rights Management Services(AD RMS) 또는 RMS(Azure 권한 관리) 정책이 적용된 메시지입니다.  <br/> |규칙은 항상 봉투 헤더에 액세스하여 해당 헤더를 검사하는 조건을 바탕으로 메시지를 처리할 수 있습니다.  <br/> RMS 보호 메시지의 내용을 검사하거나 수정하는 규칙의 경우, 전송 암호 해독이 사용되도록 설정되어 있는지 확인해야 합니다(필수 또는 옵션. 기본값은 옵션임). 자세한 내용은 [전송 암호 해독 사용 또는 사용 안 함](https://go.microsoft.com/fwlink/p/?linkid=848060)을 참조하세요.  <br/> |
|**일반 텍스트 서명된 메시지** 서명되었지만 암호화되지는 않은 메시지입니다.  <br/> |예  <br/> |
|**UM 메시지** 음성 사서함, 팩스, 부재 중 전화 알림, Microsoft Outlook Voice Access를 사용하여 만들었거나 전달된 메시지 등 통합 메시징 서비스에서 생성하거나 처리한 메시지입니다.  <br/> |예  <br/> |
|**익명 메시지** 익명 보낸 사람이 보낸 메시지입니다.  <br/> |예  <br/> |
|**읽기 보고서** 받는 사람이 읽기 확인을 요청한 경우에 생성되는 보고서입니다. 읽기 보고서에는  `IPM.Note*.MdnRead` 또는  `IPM.Note*.MdnNotRead`라는 메시지 클래스가 표시됩니다.  <br/> |예  <br/> |
   
## <a name="what-else-should-i-know"></a>더 알아야 할 것은 무엇입니까?

- Exchange Online Protection의 중요 한 규칙에 대 한 **버전** 또는 **RuleVersion** 속성 값 하지 않습니다. 
    
- 만들거나 메일 흐름 규칙을 수정 후 메시지에 적용할 신규 또는 업데이트 된 규칙에 대 한 최대 30 분까지 걸릴 수 있습니다.
    
## <a name="for-more-information"></a>자세한 내용

[전송 규칙 관리](http://technet.microsoft.com/library/e7a81372-b6d7-4d1f-bc9e-a845a7facac2.aspx)
  
[전송 규칙 조건자](http://technet.microsoft.com/library/04edeaba-afd4-4207-b2cb-51bcc44e483c.aspx)
  
[전송 규칙 작업](http://technet.microsoft.com/library/f8621ecb-a177-4025-9011-a6569999746a.aspx)
  
[Using transport rules to inspect message attachments](http://technet.microsoft.com/library/874d1c78-a8ec-4938-b388-d3208c2fa971.aspx)
  
[Office 365의 전자 메일 암호화](https://support.office.com/article/c0d87cbe-6d65-4c03-88ad-5216ea5564e8)
  
[전송 규칙 절차](http://technet.microsoft.com/library/bc682071-eb68-4cd9-a306-e5de0e1e79cc.aspx)
  
[전송 및 받은 편지함 규칙 제한](https://go.microsoft.com/fwlink/p/?LinkId=324584)
  

