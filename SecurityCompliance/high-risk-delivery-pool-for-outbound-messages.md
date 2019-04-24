---
title: 아웃 바운드 메시지에 대 한 위험성이 높은 배달 풀
ms.author: tracyp
author: MSFTTracyP
manager: laurawi
ms.date: 8/24/2016
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: ac11edd9-2da3-462d-8ea3-bbf9dbc6f948
ms.collection:
- M365-security-compliance
description: 고객의 전자 메일 시스템이 맬웨어 또는 악성 스팸 공격에 의해 손상 되 고 호스팅된 필터링 서비스를 통해 아웃 바운드 스팸 메일을 보내는 경우이로 인해 타사 블록에 나열 되는 Office 365 데이터 센터 서버의 IP 주소가 생성 될 수 있습니다. 주고.
ms.openlocfilehash: b3c0aecd45dd01d407712af2e3945e1cff521710
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32253946"
---
# <a name="high-risk-delivery-pool-for-outbound-messages"></a>아웃 바운드 메시지에 대 한 위험성이 높은 배달 풀

고객의 전자 메일 시스템이 맬웨어 또는 악성 스팸 공격에 의해 손상 되 고 호스팅된 필터링 서비스를 통해 아웃 바운드 스팸 메일을 보내는 경우이로 인해 타사 블록에 나열 되는 Office 365 데이터 센터 서버의 IP 주소가 생성 될 수 있습니다. 주고. 호스트 필터링 서비스를 사용 하지 않지만 이러한 차단 목록을 사용 하 여 해당 목록에 추가 된 호스트 필터링 IP 주소에서 보낸 모든 전자 메일은 거부 하는 대상 서버입니다. 이를 방지 하기 위해 스팸 임계값을 초과 하는 모든 아웃 바운드 메시지는 위험성이 높은 배달 풀을 통해 전송 됩니다. 이 보조 아웃 바운드 전자 메일 풀은 저품질 일 수 있는 메시지를 보내는 데만 사용 됩니다. 이렇게 하면 네트워크의 나머지 부분에서 보내는 IP 주소가 차단 될 가능성이 높은 메시지가 전송 되지 않도록 할 수 있습니다.
  
전용 위험성이 높은 배달 풀을 사용 하면 일반 아웃 바운드 풀이 높은 품질로 알려진 메시지만 보낼 수 있습니다. 이 보조 IP 풀을 사용 하면 일반 아웃 바운드 IP 풀이 차단 된 목록에 추가 될 가능성을 줄일 수 있습니다. 위험성이 높은 배달 풀이 차단 된 목록에 포함 될 가능성은 여전히 위험에 노출 됩니다. 이는 설계에 따른 것입니다.
  
보내는 도메인에 도메인의 IP 주소를 제공 하는 주소 레코드 (A 레코드) 및 DNS의 특정 도메인에 대 한 메일을 받아야 하는 서버로 메일을 보낼 수 있도록 하는 MX 레코드가 없는 메시지는 항상 스팸 처리에 관계 없이 위험성이 높은 배달 풀
  
## <a name="understanding-delivery-status-notification-dsn-messages"></a>DSN (배달 상태 알림) 메시지 이해

아웃 바운드 높은 위험 배달 풀은 모든 "반송" 또는 "실패" (DSN) 메시지의 배달을 관리 합니다.
  
DSN 메시지가 갑자기 증가하는 경우의 가능한 원인은 다음과 같습니다.
  
- 서비스 사용 고객 중 한 명에게 영향을 주는 스푸핑 캠페인
    
- 디렉터리 수집 공격
    
- 스팸 공격
    
- Rogue SMTP 서버
    
이러한 모든 문제로 인해 서비스에서 처리하는 DSN 메시지의 수가 급증할 수 있습니다. 대부분의 경우 이러한 DSN 메시지는 다른 전자 메일 서버 및 서비스에 스팸으로 표시 됩니다.
  
## <a name="for-more-information"></a>자세한 내용

[아웃바운드 스팸 정책 구성](configure-the-outbound-spam-policy.md)
  
[스팸 방지 보호 기능 FAQ](anti-spam-protection-faq.md)
  

