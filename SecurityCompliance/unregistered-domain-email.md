---
title: 등록 되지 않은 도메인 전자 메일
ms.author: tracyp
author: MSFTTracyP
manager: laurawi
ms.date: 10/17/2018
audience: Admin
ms.topic: overview
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.collection:
- M365-security-compliance
description: 등록 되지 않은 도메인 전자 메일을 대량 전송 하는 경우 전자 메일 차단 위험이 실행 됩니다. 자세한 내용은이 문서를 참조 하세요.
ms.openlocfilehash: 207b71ab7e144af9709e7485d61c936e07271a11
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/17/2019
ms.locfileid: "34156300"
---
# <a name="unregistered-domain-email-what-you-need-to-know"></a>등록 되지 않은 도메인 전자 메일: 알아야 할 사항

Office 365을 사용 하면 테 넌 트에서 Exchange Online Protection (EOP)을 통해 일부 메시지를 릴레이할 수 있습니다. 이 예에서는 사용자가 Office 365 사서함을 사용 하 고 외부 사용자가 전자 메일을 보낼 때 전자 메일 전달이 구성 되는 경우를 예로 들 수 있습니다. 이는 학생 들이 자신의 개인 전자 메일 인터페이스를 활용 하지만 학교와 관련 된 전자 메일이 전송 되는 교육 환경에서 가장 자주 발생 합니다. 다른 예로는 고객이 하이브리드 시나리오에 있고 EOP에서 전자 메일을 보내는 온-프레미스 서버가 있는 경우를 들 수 있습니다.

## <a name="problems-with-unregistered-domains"></a>등록 되지 않은 도메인 문제

이 문제는 온-프레미스 서버가 손상 되 고 종료 되 면 많은 양의 스팸을 EOP에서 릴레이할 때 발생 합니다. 거의 모든 경우에 적절 한 커넥터를 설정 했지만 등록 되지 않은 도메인에서 전자 메일을 전송 하 고 있습니다. Office 365을 사용 하면 등록 되지 않은 도메인에서 합당 한 메일을 가져올 수 있지만, 허용 도메인은 외부에서 송신을 수행 하려는 각 도메인에 대해 관리 센터에서 구성 해야 합니다.

일단 손상 되 면 테 넌 트에서 등록 되지 않은 도메인에 대 한 아웃 바운드 메일을 보낼 수 없게 됩니다. 사용자에 게 다음과 같은 내용의 배달 못 함 보고서 (NDR)를 받게 됩니다.

- 550 5.7.750 서비스를 사용할 수 없습니다. 클라이언트가 등록 되지 않은 도메인에서 보내지 못하도록 차단 됨

## <a name="unblocking-tenant-in-order-to-send-again"></a>다시 보내기 위해 테 넌 트 차단 해제

등록 되지 않은 도메인에서 보내기를 차단 하면 몇 가지 작업을 수행 해야 합니다.

1. 모든 도메인을 Microsoft 365 관리 센터에 등록 해야 합니다. 자세한 내용은 [여기](https://docs.microsoft.com/en-us/exchange/mail-flow-best-practices/manage-accepted-domains/manage-accepted-domains)에서 확인할 수 있습니다.

2. 비정상적인 커넥터를 찾습니다. 악의적인 행위자는 종종 Office 365 테 넌 트에서 새 인바운드 커넥터를 만들어 스팸을 보냅니다. 커넥터를 확인 하는 방법에 대 한 자세한 내용은 [여기](https://docs.microsoft.com/en-us/powershell/module/exchange/mail-flow/get-inboundconnector?view=exchange-ps)에서 확인할 수 있습니다. 

3. 온-프레미스 서버를 잠그고 해당 서버가 손상 되지 않았는지 확인 합니다.

> [!TIP]
> 특히 타사 서버인 경우에는 여기에 포함 되는 여러 요소가 있습니다. 서버에서 나가는 모든 메일을 사용할 수 있는지 확인 해야 합니다.

4. 작업이 완료 되 면 Microsoft 지원 서비스에 문의 하 여 등록 되지 않은 도메인에서 다시 보내기 위해 테 넌 트의 차단 해제를 요청 해야 합니다.  오류 코드를 제공 하는 것이 도움이 되지만 환경이 보호 되 고 스팸이 다시 보내지지 않도록 해야 합니다. 지원 사례를 여는 방법에 대 한 자세한 내용은 [여기](https://support.office.com/en-us/article/Contact-support-for-business-products-Admin-Help-32a17ca7-6fa0-4870-8a8d-e25ba4ccfd4b#ID0EAADAAA=online)에서 확인할 수 있습니다.
  
## <a name="for-more-information"></a>자세한 내용

[Office 365 스팸 방지 보호](anti-spam-protection.md)

[Office 365의 전자 메일 배달 못 함 보고서(NDR)](https://support.office.com/article/email-non-delivery-reports-in-office-365-51daa6b9-2e35-49c4-a0c9-df85bf8533c3)

[사서함의 전자 메일 전달 구성](https://docs.microsoft.com/en-us/exchange/recipients-in-exchange-online/manage-user-mailboxes/configure-email-forwarding)

[Office 365를 사용하여 전자 메일을 보내도록 다기능 장치 또는 응용 프로그램을 설정하는 방법](https://support.office.com/en-us/article/How-to-set-up-a-multifunction-device-or-application-to-send-email-using-Office-365-69f58e99-c550-4274-ad18-c805d654b4c4)

[Exchange Online에서 허용 도메인을 관리](https://docs.microsoft.com/en-us/exchange/mail-flow-best-practices/manage-accepted-domains/manage-accepted-domains)합니다.
