---
title: 확인 되지 않은 보낸 사람
ms.author: tracyp
author: MSFTTracyP
manager: laurawi
ms.date: 04/25/2019
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.collection:
- M365-security-compliance
description: 피싱 메시지가 사서함에 도착 하지 않도록 하기 위해 웹에서 Outlook.com 및 Outlook은 보낸 사람이 누구 인지를 확인 하 고 의심 스러운 메시지를 정크 메일로 표시 합니다.
ms.openlocfilehash: 92458a93a4da3e449061e4d2a4ba312d635c42cc
ms.sourcegitcommit: 7f00f765e8fa674ce1c8c66f5b89b6bea45e13ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/22/2019
ms.locfileid: "34341626"
---
# <a name="unverified-sender"></a>확인 되지 않은 보낸 사람

피싱 메시지가 사서함에 도착 하지 않도록 하기 위해 웹에서 Outlook.com 및 Outlook은 보낸 사람이 누구 인지를 확인 하 고 의심 스러운 메시지를 정크 메일로 표시 합니다.

> [!IMPORTANT]
> 메시지가 피싱 사기로 표시 되 면 Outlook.com 및 웹용 Outlook의 페이지 맨 위에 경고가 표시 되지만 메시지의 모든 링크는 계속 열 수 있습니다.

## <a name="how-can-i-identify-a-suspicious-message-in-my-inbox"></a>받은 편지함에서 의심 스러운 메시지를 어떻게 확인할 수 있나요?

Outlook.com and Outlook에서 메시지를 보낸 사람이 식별 되지 않거나 id가 보낸 사람 주소에 표시 되는 내용과 다를 때 나타나는 지표를 표시 합니다.

## <a name="how-to-manage-which-messages-receive-the-unverified-sender-treatment"></a>확인 되지 않은 보낸 사람 처리를 수신 하는 메시지를 관리 하는 방법 

Office 365 고객 인 경우 Security & 준수 센터를 통해이 기능을 관리할 수 있습니다. 

- Office 365 Security & 준수 센터에서 테 넌 트 관리자는 피싱 정책 아래에 있는 스푸핑 방지 보호를 통해이 기능을 켜거나 끌 수 있습니다. 또한 ' AntiPhishPolicy ' cmdlet을 통해 관리할 수 있습니다. 자세한 내용은 Office 365 및 AntiPhishPolicy의 피싱 방지 보호를 참조 하세요.

    ![그래픽 인터페이스에서 인증 되지 않은 보낸 사람 편집](media/unverified-sender-article-editing-unauthenticated-senders.jpg)

- 관리자가 가양성을 식별 했 고 보낸 사람이 확인 되지 않은 보낸 사람 처리를 수신 하지 않아야 하는 경우 다음 작업 중 하나를 수행 하 여 위장 인텔리전스 스푸핑 허용 목록에 보낸 사람을 추가할 수 있습니다.
        
    - 스푸핑 인텔리전스 이해를 통해 도메인 쌍을 추가 합니다. 자세한 내용은 연습: 스푸핑 인텔리전스 이해를 참조 하세요.
                
    - Get-phishfilterpolicy cmdlet을 통해 도메인 쌍을 추가 합니다. 자세한 내용은 Office 365의 Get-phishfilterpolicy 및 스푸핑 방지 보호를 참조 하세요.

또한 ETRs (전자 메일 전송 규칙), 안전한 도메인 목록 (스팸 방지 정책), 수신 허용-보낸 사람 목록 또는 사용자가 해당 사용자를 "안전한 보낸 사람"으로 설정 하 여 관리자 허용 목록을 통해 받은 편지 함으로 배달 된 경우에는 확인 되지 않은 보낸 사람 처리가 적용 되지 않습니다. 받은 편지함.

### <a name="you-see-a--in-the-sender-image"></a>보낸 사람 이미지에 '? '가 표시 됩니다.

Outlook.com 및 웹용 Outlook에서 전자 메일 인증 기술을 사용 하 여 보낸 사람의 id를 확인할 수 없는 경우 보낸 사람 사진에 '? '가 표시 됩니다. 

![메시지가 확인 통과 되지 않음](media/message-did-not-pass-verification.jpg)

인증에 실패 한 모든 메시지는 악성이 아닙니다. 그러나 보낸 사람을 인식 하지 못하는 경우 인증을 받지 않는 메시지와 상호 작용할 때는 주의 해야 합니다. 또는 일반적으로 보낸 사람 이미지에 '? '가 포함 되지 않는 보낸 사람을 인식할 수 있지만이를 갑자기 보면 보낸 사람이 위장 중 이라고 표시 됩니다.

## <a name="frequently-asked-questions"></a>자주하는 질문

### <a name="what-criteria-does-outlookcom-and-outlook-on-the-web-use-to-add-the--and-the-via-properties"></a>Outlook.com 및 웹용 Outlook에서 '? ' 및 ' via ' 속성을 추가 하는 데 사용 하는 기준은 무엇입니까?

보낸 사람 이미지의 '? '에 대해: Outlook.com에서는 메시지가 SPF 또는 DKIM 인증을 통과 해야 합니다. 자세한 내용은 office 365에서 스푸핑 방지 및 dkim을 사용 하 여 사용자 지정 365 도메인에서 보낸 아웃 바운드 전자 메일의 유효성을 검사 하는 데 도움을 주는 방법에 SPF를 설정 합니다.

Via 태그의 경우: 보낸 사람 주소에 있는 도메인이 DKIM 서명 또는 SMTP 메일에서 보낸 도메인과 다른 경우 Outlook.com는 해당 두 필드 중 하나에 도메인을 표시 합니다 (DKIM 서명 우선).

### <a name="how-do-i-remove-the-"></a>'? '를 제거 하려면 어떻게 해야 합니까?

보낸 사람 이미지의 '? '에 대해 보낸 사람으로 서 SPF 또는 DKIM 중 하나를 사용 하 여 메시지를 인증 해야 합니다.

Via 태그: 보낸 사람으로 서, DKIM 서명 또는 SMTP 메일의 도메인은 From 주소에 있는 도메인과 같거나 그 하위 도메인 인지 확인 해야 합니다.

### <a name="does-outlookcom-and-outlook-on-the-web-show-this-for-every-message-that-doesnt-pass-authentication"></a>Outlook.com 및 웹용 Outlook에서 인증을 통과 하지 않는 모든 메시지를 표시 하나요?

꼭 필요 하지는 않습니다. Outlook.com 및 웹용 Outlook의 메시지에는 보낸 사람을 인증 하기 위한 다른 속성이 있을 수 있습니다.

## <a name="related-topics"></a>관련 항목

[Outlook.com 전자 메일 계정 보호](https://support.office.com/article/a4f20fc5-4307-4ece-8231-6d4d4bd8a9ba)

[Outlook.com에서 불건전, 피싱 또는 스푸핑 처리](https://support.office.com/article/0d882ea5-eedc-4bed-aebc-079ffa1105a3)

[웹용 Outlook에서 정크 메일 및 스팸 필터링](https://support.office.com/article/db786e79-54e2-40cc-904f-d89d57b7f41d)
