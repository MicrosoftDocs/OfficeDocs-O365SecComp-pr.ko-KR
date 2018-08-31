---
title: 아웃 바운드 메시지 용 위험성이 높은 배달 풀
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 8/24/2016
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: ac11edd9-2da3-462d-8ea3-bbf9dbc6f948
description: 맬웨어 또는 악의적인 스팸 공격을 여는 고객의 전자 메일 시스템 암호가 손상 된 호스팅된 필터링 서비스를 통해 아웃 바운드 스팸 발송 하는 경우이 될 수 있습니다 제 3 자 블록에 나열 되는 Office 365 데이터 센터 서버의 IP 주소 나열합니다.
ms.openlocfilehash: 69548488f70944a319a449bfc4ac1cb1bffd7b1c
ms.sourcegitcommit: e9dca2d6a7838f98bb7eca127fdda2372cda402c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/21/2018
ms.locfileid: "23003137"
---
# <a name="high-risk-delivery-pool-for-outbound-messages"></a>아웃 바운드 메시지 용 위험성이 높은 배달 풀

맬웨어 또는 악의적인 스팸 공격을 여는 고객의 전자 메일 시스템 암호가 손상 된 호스팅된 필터링 서비스를 통해 아웃 바운드 스팸 발송 하는 경우이 될 수 있습니다 제 3 자 블록에 나열 되는 Office 365 데이터 센터 서버의 IP 주소 나열합니다. 수행 하는 대상 서버 하지 호스팅된 필터링 서비스를 사용 하지만 수행 이러한 차단 목록을 사용 하 여, 모든 해당 목록에 추가 된 호스팅된 필터링 IP 주소에서 보낸 모든 전자 메일을 거부 합니다. 이 방지 하려면 위험성이 높은 배달 풀을 통해 스팸 임계값을 초과 하는 모든 아웃 바운드 메시지 전송 됩니다. 이 보조 아웃 바운드 전자 메일 풀 저품질 유용할 수 있는 메시지를 보낼 수만 사용 됩니다. 이 네트워크의 나머지 부분을 차단 하 고 보내는 IP 주소에서 발생 하는 메시지를 보내지 못하도록 보호할 수 있습니다.
  
기본 아웃 바운드 풀 높은 품질의 것으로 알려진 된 메시지를 보내지만 전용된 위험성이 높은 배달 풀을 사용 하면. 이 보조 IP 풀을 사용 하 여 차단된 목록에 추가 되는 기본 아웃 바운드 IP 풀의 확률을 줄일 수 있습니다. 차단된 목록에 배치 되 고 위험성이 높은 배달 풀의 가능성을 사전에는 위험 유지 됩니다. 의도적인 것입니다.
  
보내는 도메인의 도메인의 IP 주소를 제공 하는 없는 주소 record (레코드) 및 DNS에서 특정 도메인에 대 한 메일을 수신 해야 하는 서버에 직접 메일을 사용 하면, MX 레코드가 없습니다 사람이 없는 메시지를 통해 항상 라우팅되는 스팸 대비한에 관계 없이 위험성이 높은 배달 풀입니다.
  
## <a name="understanding-delivery-status-notification-dsn-messages"></a>배달 상태 알림 (DSN) 메시지 이해 (영문)

아웃 바운드 위험성이 높은 배달 풀은 모든 "반송 됨" 또는 "실패" (DSN) 메시지 배달을 관리합니다.
  
DSN 메시지가 갑자기 증가하는 경우의 가능한 원인은 다음과 같습니다.
  
- 서비스 사용 고객 중 한 명에게 영향을 주는 스푸핑 캠페인
    
- 디렉터리 수집 공격
    
- 스팸 공격
    
- Rogue SMTP 서버
    
이러한 문제는 모든 서비스에 의해 처리 중인 DSN 메시지의 수에 갑자기 증가 하는 될 수 있습니다. 여러 번 반복, 이러한 DSN 메시지는 다른 전자 메일 서버 및 서비스에 대 한 스팸 것 같습니다.
  
## <a name="for-more-information"></a>자세한 내용

[아웃바운드 스팸 정책 구성](configure-the-outbound-spam-policy.md)
  
[스팸 방지 보호 FAQ](anti-spam-protection-faq.md)
  

