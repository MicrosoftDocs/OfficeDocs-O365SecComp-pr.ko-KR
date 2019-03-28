---
title: Office 365에서 가양성을 발생을 방지하는 방법
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 6/7/2018
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
ms.collection:
- M365-security-compliance
localization_priority: Priority
search.appverid:
- MOE150
- MET150
description: 가양성을 방지하고 Office 365에서 실제 전자 메일을 쓸모없는 상태로 유지하는 방법에 대해 알아보십시오.
ms.openlocfilehash: ecce497269030945457344122a9a218105369be2
ms.sourcegitcommit: 8a65a29aa3bfe5dcad0ff152a7cd795e02877dd9
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/28/2019
ms.locfileid: "30936708"
---
# <a name="how-to-prevent-real-email-from-being-marked-as-spam-in-office-365"></a>Office 365에서 실제 전자 메일이 스팸으로 표시되는 일을 방지하는 방법

 **실제 전자 메일이 Office 365에서 스팸으로 표시되나요? 그렇다면 다음을 수행하세요.**
  
거짓 부정이 있는 경우 [보고서 메시지 추가 기능 사용](https://support.office.com/article/b5caa9f1-cdf3-4443-af8c-ff724ea719d2)을 사용하여 Microsoft에 메시지를 보고해야 합니다. 또한 메시지 *을 첨부 파일*로 not_junk@office365.microsoft.com으로 전달할 수 있습니다.

**중요** 메시지를 첨부 파일로 전달하지 않는 경우 헤더가 누락되며 Office 365에서 스팸 메일 필터링을 개선할 수 없습니다.
    
## <a name="determine-the-reason-why-the-message-was-marked-as-spam"></a>메시지가 스팸으로 표시되는 이유 확인

Office 365의 스팸 문제는 [전자 메일 메시지 머리글 보기](https://support.office.com/article/cd039382-dc6e-4264-ac74-c048563d212c)를 통해 해결할 수 있으며 잘못된 내용을 파악할 수 있습니다. X-Forefront-Antispam-Report라는 헤더를 찾아야합니다. [스팸 방지 메시지 헤더에 대해 자세히 알아](https://technet.microsoft.com/library/dn205071%28v=exchg.150%29.aspx)볼 수 있습니다.
  
헤더에서 다음 머리글 및 값을 찾습니다.
  
### <a name="x-forefront-antispam-report"></a>X-Forefront-Antispam-Report

- **SFV:SPM** EOP 스팸 필터도 인해 메시지가 스팸으로 표시되지 않았음을 나타냅니다. 

- **SFV:BLK** 보내는 주소가 받는 사람의 수신 거부 보낸 사람 목록에 있기 때문에 메시지가 스팸으로 표시되었음을 나타냅니다. 
    
- **SFV:SKS** 메시지가 콘텐츠 필터 전에 스팸으로 표시되었음을 나타냅니다. 여기에는 메시지를 스팸으로 표시하는 메일 흐름 규칙(전송 규칙이라고도 함)이 포함될 수 있습니다. 메시지 추적을 실행하여 SCL(스팸 지수)이 높게 설정되었을 수 있는 메일 흐름 규칙이 트리거되었는지 알아봅니다. 
    
- **SFV:SKB** 스팸 필터 정책의 차단 목록과 일치하므로 메시지가 스팸으로 표시되었음을 나타냅니다. 
    
- **SFV:BULK** x-microsoft-antispam 헤더에 있는 BCL(대량 불만 수준) 값이 콘텐츠 필터에 대해 설정된 대량 임계값보다 높음을 나타냅니다. 대량 전자 메일은 사용자가 등록했을 수 있지만 여전히 원치 않을 수 있는 전자 메일입니다. 메시지 헤더에서 X-Microsoft-Antispam 헤더의 BCL(대량 불만 수준) 속성을 찾으세요. BCL 값이 스팸 필터에 설정된 임계값보다 낮으면 이러한 유형의 대량 메시지를 스팸으로 대신 표시하도록 임계값을 조정할 수 있습니다. 사용자마다 [대량 전자 메일을 처리하는 방법](https://docs.microsoft.com/ko-KR/office365/SecurityCompliance/bulk-complaint-level-values)에 대해 다른 임계값 및 기본 설정을 사용할 수 있습니다. 사용자 기본 설정마다 다른 정책 또는 규칙을 만들 수 있습니다.
    
- **CAT:SPOOF** 또는 **CAT: PHISH** 메시지가 스푸핑된 것을 나타냅니다. 즉, 메시지 원본이 유효한지 검사할 수 없으며 의심스러운 경우를 의미합니다. 유효한 경우 보낸 사람은 SPF 및 DKIM 구성이 올바른지 확인해야 합니다. 자세한 내용은 Authentication-Results 헤더를 확인합니다. 모든 보낸 사람이 적절한 전자 메일 인증 방법을 사용하도록 하는 것은 쉽지 않을 수 있지만 이러한 검사를 우회하는 것은 매우 위험할 수 있으며 보안 위반의 가장 큰 원인이 됩니다. 
    
### <a name="x-customspam"></a>x-customspam

- 이 헤더가 있으면 스팸 필터에서 [고급 스팸 옵션 중 하나가 사용되도록 설정](https://technet.microsoft.com/library/jj200750%28v=exchg.150%29.aspx)되어 있기 때문에 메시지가 스팸으로 표시되었음을 나타냅니다. 이러한 기능이 필요하지 않으면 기본 설정을 사용하는 것이 좋습니다. 
    
## <a name="solutions-to-additional-causes-of-too-much-spam"></a>너무 많은 스팸을 유발하는 추가 원인에 대한 해결 방법

효과적인 작동을 위해 EOP(Exchange Online Protection)는 관리자가 몇 가지 작업을 완료하도록 요구합니다. Office 365 테넌트의 관리자가 아니며 스팸이 너무 많이 발생하는 경우 관리자와 함께 이러한 문제를 해결할 수 있습니다. 그렇지 않은 경우 사용자 작업으로 건너뛸 수 있습니다.
  
### <a name="for-admins"></a>관리자

- **Office 365를 가리키도록 DNS 레코드 지정** EOP를 통해 보호를 제공하려면 모든 도메인의 MX(메일 교환기)가 Office 365만 가리켜야 합니다. MX가 Office 365를 가리키지 않는 경우, EOP는 사용자를 위해 스팸 필터링를 제공하지 않습니다. 다른 서비스 또는 어플라이언스를 사용하여 도메인에 대한 스팸 필터링을 제공하려는 경우 EOP에서 스팸 보호 기능을 사용하지 않도록 설정하는 것이 좋습니다. SCL 값을 -1로 설 하는 메일 흐름 규칙을 만들어 이렇게 할 수 있습니다. 나중에 EOP를 사용하기로 결정하면 이 메일 흐름 규칙을 제거해야 합니다. 
    
- **사용자에 대한 보고서 메시지 추가 기능 켜기** [사용자가 보고서 메시지 추가 기능을 사용할 수 있도록 설정](enable-the-report-message-add-in.md)하는 것이 좋습니다. 관리자는 사용자가 보내는 의견을 보고, 패턴을 사용하여 문제를 유발할 수 있는 설정을 조정할 수 있습니다.

- [여기](https://docs.microsoft.com/ko-KR/office365/servicedescriptions/exchange-online-service-description/exchange-online-limits)에 표시된 대로 **사용자가 전자 메일을 송수신하기 위한 허용 한계 내에 있는지 확인하십시오**.

 - [여기](bulk-complaint-level-values.md)에 명시된 대로 **대량 레벨을 다시 확인하십시오**
    
### <a name="for-users"></a>사용자
    
- **안전한 발신자 목록 만들기** 사용자는 신뢰할 수 있는 발신인의 주소를 [Outlook](https://go.microsoft.com/fwlink/p/?LinkId=270065) 또는 [웹상의 Outlook](https://go.microsoft.com/fwlink/p/?LinkId=294862)에 안전한 발신자 목록에 추가할 수 있습니다. 웹에서 Outlook을 시작하려면 **설정**![을 선택합니다. ](media/24bd5467-c8d2-4936-9c37-a179bd0e21ec.png) \> ** 옵션 ** \> **차단 또는 허용**합니다. 다음 다이어그램은 안전한 발신자 목록에 무언가를 추가하는 예를 보여줍니다.
  
![웹용 Outlook에 안전한 발신자 추가](media/8de6b24e-429e-4e8f-8ce8-53ba659cbfcb.png)
  
EOP는 사용자의 수신 허용 - 보낸 사람 및 받는 사람을 존중하지만 Safe Domains는 사용하지 않습니다. 이는 도메인이 웹에서 Outlook을 통해 추가되거나 Outlook에서 추가되고 Directory Sync를 사용하여 동기화되는지 여부에 관계없이 적용됩니다.

- **Outlook에서 SmartScreen 사용 안 함** 이전 Outlook 데스크톱 클라이언트를 사용하는 경우 지원이 중단된 SmartScreen 필터링 기능을 사용하지 않도록 설정해야 합니다. 이 기능을 사용하도록 설정하면 가양성이 발생할 수 있습니다. 업데이트된 데스크톱 Outlook 클라이언트를 실행하는 경우에는 이 작업이 필요하지 않습니다.

## <a name="troubleshooting-a-message-ends-up-in-the-junk-folder-even-though-eop-marked-the-message-as-non-spam"></a>문제 해결 : EOP가 메시지를 스팸이 아닌 것으로 표시했더라도 메시지는 정크 폴더에 놓입니다.


사용자가 Outlook에서 "수신 허용 목록만 허용 : 수신 허용 - 보낸 사람 목록 또는 수신 허용 - 받는 사람 목록의 사람 또는 도메인에게서 온 메일만 받은 편지함으로 배달됩니다" 옵션을 사용하는 경우 모든 전자 메일은 보낸 사람의 정크 메일 폴더로 이동합니다. 보낸 사람이 받는 사람의 수신 허용 목록에 있지 않은 경우 이것은 EOP가 메시지를 스팸이 아닌 것으로 표시했는지 여부와 관계없이 또는 EOP에서 메시지를 스팸이 아닌 것으로 표시하도록 설정한 경우에도 발생합니다.
  
[ Outlook : 정크 메일 UI를 비활성화하는 정책 설정 및 필터링 메커니즘](https://support.microsoft.com/ko-KR/kb/2180568)의 지침에 따라 Outlook 사용자의 수신 허용 목록 전용 옵션을 비활성화할 수 있습니다.
  
웹용 Outlook에서 메시지를 보면 보낸 사람이 수신자의 보낸 사람 목록에 없기 때문에 메시지가 정크 폴더에 있음을 나타내는 노란색 안전 팁이 표시됩니다.
  
메시지의 헤더를 보면 스탬프 SFV: SKN(IP 허용 또는 ETR 허용) 또는 SFV: NSPM(스팸 아님) 스탬프가 포함될 수 있지만 메시지는 여전히 사용자의 정크 폴더에 있습니다. 사용자가 "수신 허용 목록"만 사용하도록 설정한 메시지 헤더에는 아무 것도 없습니다. 이는 Outlook의 사용자가 설정한 "안전 목록 전용" 옵션이 EOP 설정을 무시하기 때문에 발생합니다. 
  
 **수신 허용 목록의 메시지가 메시지 헤더에 스팸이 아닌 것으로 표시되지만 여전히 사용자의 정크 폴더로 분류되는 이유를 확인하려면 **
  
1. Exchange Online PowerShell로 연결하는 방법을 알아보려면 [Exchange Online PowerShell에 연결](https://go.microsoft.com/fwlink/p/?LinkId=396554)을 참조하세요. 
    
2. 다음 명령을 실행하여 사용자의 정크 메일 구성 설정을 봅니다.
    
  ```Powershell
  Get-MailboxJunkEmailConfiguration example@contoso.com | fl TrustedListsOnly,ContactsTrusted,TrustedSendersAndDomains
  ```

- TrustedListsOnly가 True로 설정되면 이 설정이 사용 가능하다는 의미입니다.
- ContactsTrusted가 True로 설정되면 사용자가 연락처와 수신 허용 - 보낸 사람 모두를 신뢰함을 의미합니다.
- TrustedSendersAndDomains는 사용자의 수신 허용 - 보낸 사람 목록의 내용을 나열합니다.


## <a name="eop-only-customers-use-directory-synchronization"></a> EOP 전용 고객: 디렉터리 동기화를 사용

EOP 전용 고객의 경우, 즉 온 - 프레미스(Exchange) 전자 메일 서버와 함께 사용하기 위해 EOP 서비스에 가입한 경우 디렉터리 동기화를 사용하여 사용자 설정을 서비스와 동기화해야 합니다. 이렇게 하면 수신 허용 - 보낸 사람 목록이 EOP에 의해 존중되도록 할 수 있습니다. 자세한 내용은 [EOP](https://go.microsoft.com/fwlink/?LinkId=534098)의 메일 사용자 관리에서 "디렉터리 동기화를 사용하여 메일 사용자 관리"를 참조하십시오.
