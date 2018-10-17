---
title: 등록 되지 않은 도메인 전자 메일
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 10/17/2018
ms.audience: Admin
ms.topic: overview
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
description: 많은 양의 등록 되지 않은 도메인 전자 메일을 전송 하면 위험 시작 차단 되는 전자 메일을 실행 합니다. 자세한 내용은이 문서를 읽어보십시오.
ms.openlocfilehash: 30d7887be0429195380f2c4ae1a328904dffd69c
ms.sourcegitcommit: 6d72cdb882b93edf6dfddb5ff2e6d8a16e2fa0bc
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/17/2018
ms.locfileid: "25596731"
---
# <a name="unregistered-domain-email-what-you-need-to-know"></a>등록 되지 않은 도메인 전자 메일: 필요한 알고

Office 365 테 넌 트를 통해 Exchange Online Protection (EOP)는 일부 메시지를 릴레이 하도록 허용 합니다. 사용자가 Office 365 사서함 및 외부 사용자에 게 보냅니다 전자 메일 하지만 나가는 다시 외부 사용자의 사서함에 있도록 전자 메일 전달을 구성 하는 경우이 예로 지원 되는 것입니다. 여기서 학생 하려면 자신의 개인 전자 메일 인터페이스를 활용 하지만 여전히 학교와 관련 된 전자 메일을 가져올 교육 환경에서 가장 일반적으로입니다. 다른 예로 고객 하이브리드 시나리오에 있고 EOP 외부로 전자 메일을 전송 하는 온-프레미스 서버를 포함 하는 경우.

## <a name="problems-with-unregistered-domains"></a>등록 되지 않은 도메인으로 구성 된 문제

온-프레미스 서버 손상 된 및 EOP에서 스팸의 양이 릴레이를 종료 하는 경우이 문제가입니다. 거의 모든 경우에서 오른쪽 커넥터 설정 하지만 등록 되지 않은로 알려져 구성 되지 않은 도메인에서 전자 메일을 보낼 합니다. Office 365에서 적절 한 양의 등록 되지 않은 도메인에서 제공 하는 메일을 허용 하지만 부재중 보내는 방법에 계획 하는 각 도메인에 대 한 관리 센터에 있는 허용 도메인을 구성 해야 합니다.

손상 되 면 테 넌 트가 등록 되지 않은 도메인에 대 한 아웃 바운드 메일을 보내지 못하도록 차단 됩니다. 사용자는 배달 못함 보고서 (NDR) 없다는 표시 됩니다.

- 550 5.7.750 서비스를 사용할 수 없습니다. 클라이언트 등록 되지 않은 도메인에서 보내지 못하도록 차단

## <a name="unblocking-tenant-in-order-to-send-again"></a>다시 전송 하기 위해 테 넌 트를 차단 해제

여러 가지 방법으로 등록 되지 않은 도메인에서 보내는 차단 될 경우 수행 해야 합니다.

1. Office 365 관리 센터에서 도메인의 모든 등록 수 있는지 확인 하십시오. 자세한 정보를 찾을 수 [여기](https://docs.microsoft.com/en-us/exchange/mail-flow-best-practices/manage-accepted-domains/manage-accepted-domains)합니다.

2. 비정상 커넥터에 대 한 정보를 제공 합니다. 악의적인 작업자 스팸 메일을 보낼를 Office 365 테 넌 트에 새 인바운드 커넥터를 만들 자주 됩니다. 확인 하 여 커넥터에 자세한 정보를 찾을 수 [여기](https://docs.microsoft.com/en-us/powershell/module/exchange/mail-flow/get-inboundconnector?view=exchange-ps)합니다. 

3. 온-프레미스 서버를 잠급니다 하 고 손상 되지 않도록 합니다.

> [!TIP]
> 여러 가지 요인을 관련 된 여기에 제 3 자 서버는 하는 경우에 특히 합니다. 그럼에도 불구 하 고 있어야 할 모든 메일 서버에서 나가는 합법적인 되었는지 확인 합니다.

4. 작업이 완료 되 면 Microsoft 기술 지원 서비스를 호출 하 고 등록 되지 않은 도메인에서 배달을 다시 차단을 해제 하는 테 넌 트를 가져오려면 요청 해야 합니다.  유용 오류 코드를 제공 하지만 환경을 보호 하는 하 고는 스팸 보내지 않을 다시 평가 해야 합니다. 기술 지원 요청을 열면 자세한 정보를 찾을 수 [여기](https://support.office.com/en-us/article/Contact-support-for-business-products-Admin-Help-32a17ca7-6fa0-4870-8a8d-e25ba4ccfd4b#ID0EAADAAA=online)합니다.
  
## <a name="for-more-information"></a>자세한 내용

[Office 365 스팸 방지 보호](anti-spam-protection.md)

[Office 365에서 전자 메일 배달 못함 보고서](https://support.office.com/article/email-non-delivery-reports-in-office-365-51daa6b9-2e35-49c4-a0c9-df85bf8533c3)

[사서함에 대 한 전자 메일 전달 구성](https://docs.microsoft.com/en-us/exchange/recipients-in-exchange-online/manage-user-mailboxes/configure-email-forwarding)

[Office 365를 사용하여 전자 메일을 보내도록 다기능 장치 또는 응용 프로그램을 설정하는 방법](https://support.office.com/en-us/article/How-to-set-up-a-multifunction-device-or-application-to-send-email-using-Office-365-69f58e99-c550-4274-ad18-c805d654b4c4)

[관리 허용 도메인 Exchange 온라인](https://docs.microsoft.com/en-us/exchange/mail-flow-best-practices/manage-accepted-domains/manage-accepted-domains)합니다.
