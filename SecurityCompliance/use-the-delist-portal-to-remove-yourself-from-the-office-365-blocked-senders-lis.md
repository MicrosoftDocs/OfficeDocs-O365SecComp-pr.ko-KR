---
title: 목록 해제 포털을 사용하여 Office 365 수신 거부 목록에서 본인 제거
ms.author: tracyp
author: MSFTTracyP
manager: laurawi
ms.date: 4/18/2016
audience: ITPro
ms.topic: troubleshooting
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 0bcecdd4-3343-4cc0-9e58-e19d4de515e8
ms.collection:
- M365-security-compliance
description: 해당 전자 메일 주소가 Office 365에 포함되는 받는 사람에게 전자 메일을 보내려고 할 때 오류 메시지가 발생하나요? 오류 메시지가 표시되지 않아야 한다고 생각될 경우 목록 해제 포털을 사용하여 Office 365 수신 거부 목록에서 본인을 제거할 수 있습니다.
ms.openlocfilehash: d63d8ffcd72789d8b8a7b7b825248ee8d0cc64a7
ms.sourcegitcommit: 5a93c2f3df35d06a59a7fbaff5c91f7afde11781
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/11/2019
ms.locfileid: "34857638"
---
# <a name="use-the-delist-portal-to-remove-yourself-from-the-office-365-blocked-senders-list"></a>목록 해제 포털을 사용하여 Office 365 수신 거부 목록에서 본인 제거

해당 전자 메일 주소가 Office 365에 포함되는 받는 사람에게 전자 메일을 보내려고 할 때 오류 메시지가 발생하나요? 오류 메시지가 표시되지 않아야 한다고 생각될 경우 목록 해제 포털을 사용하여 Office 365 수신 거부 목록에서 본인을 제거할 수 있습니다.
  
## <a name="what-is-the-office-365-blocked-senders-list"></a>Office 365 수신 거부 목록은 무엇인가요?

Microsoft는 수신 거부 목록을 사용하여 스팸, 스푸핑 및 피싱 공격으로부터 고객을 보호합니다. 메일 서버의 IP 주소, 즉 메일 서버가 인터넷에서 자신을 식별하는 데 사용하는 주소는 다양한 이유 중 하나로 Office 365의 잠재적 위협으로 태그가 지정되었습니다. Office 365에서 이 목록에 IP 주소를 추가하면 Microsoft 데이터 센터를 통한 해당 IP 주소와 고객의 간의 추가 통신이 금지됩니다.
  
다음과 같은 오류가 포함된 메일 메시지에 대한 응답이 수신되면 이 목록에 본인이 추가된 것입니다.
  
> 550 5.7.606-649 액세스 거부, 금지 된 보낸 IP [_ip 주소_]; 이 목록에서 제거를 요청 하려면을 https://sender.office.com/ 방문 하 여 지침을 따르세요. 자세한 내용은 [Office 365의 전자 메일 배달 못 함 보고서](http://go.microsoft.com/fwlink/?LinkID=526653)를 참조 하세요.
  
여기서  _IP address_는 메일 서버가 실행되는 컴퓨터의 IP 주소입니다. 
  
### <a name="to-use-the-office-365-delist-portal-to-remove-yourself-from-the-blocked-senders-list"></a>Office 365 목록 해제 포털을 사용하여 수신 거부 목록에서 본인을 제거하려면

1. 웹 브라우저에서 [https://sender.office.com](https://sender.office.com)으로 이동합니다.
    
2. 페이지의 지시를 따릅니다. 오류 메시지가 전송된 전자 메일 주소와 오류 메시지에 지정된 IP 주소를 사용하고 있는지 확인합니다. 방문할 때마다 하나의 전자 메일 주소 및 하나의 IP 주소만 입력할 수 있습니다.
    
3. **전송**을 클릭합니다.
    
    포털에서는 사용자가 제공한 전자 메일 주소로 전자 메일을 보냅니다. 전자 메일은 다음과 같이 표시 됩니다. ![목록 해제 포털을 통해 요청을 제출할 때 받는 전자 메일의 스크린샷](media/bf13e4f7-f68c-4e46-baa7-b6ab4cfc13f3.png)
  
4. 목록 해제 포털을 사용하여 사용자에게 전송된 전자 메일의 확인 링크를 클릭합니다.
    
    그러면 목록 해제 포털로 돌아갑니다.
    
5. 목록 해제 포털에서 **IP 목록 해제**를 클릭합니다.
    
    수신 거부 목록에서 IP 주소가 제거되면 해당 IP 주소에서 보낸 전자 메일 메시지가 Office 365를 사용하는 받는 사람에게 배달됩니다. 따라서 해당 IP 주소에서 보낸 전자 메일에 부적절하거나 악의적인 내용이 없는지 확인해야 합니다. 이러한 내용이 있으면 해당 IP 주소가 다시 차단될 수 있습니다.
    
    > [!NOTE]
    > 제한이 제거 되기 전에 최대 24 시간이 걸릴 수도 있고 결과가 크게 다를 수 있습니다.
    
[실제 전자 메일이 office 365에서 스팸으로 표시 되는](prevent-email-from-being-marked-as-spam.md ) 것을 방지 하 고, [office 365에서 아웃 바운드 스팸을 제어](outbound-spam-controls.md) 하 여 IP가 Blacklisted 되지 않도록 하는 방법에 대해 알아봅니다.
