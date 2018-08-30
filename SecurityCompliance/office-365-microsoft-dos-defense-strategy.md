---
title: Office 365 Microsoft DoS 방어 전략
ms.author: robmazz
author: robmazz
manager: laurawi
ms.date: 8/21/2018
audience: ITPro
ms.topic: article
ms.service: Office 365 Administration
localization_priority: None
search.appverid:
- MET150
ms.collection: Strat_O365_Enterprise
description: 서비스 거부 (DoS) 공격 처리 하기 위한 Microsoft의 방어 전략의 개요입니다.
ms.openlocfilehash: f172db5080ef73402c7e9bc61720eb0f87e844ac
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22532901"
---
# <a name="microsofts-denial-of-service-defense-strategy"></a>Microsoft의 서비스 거부 방어 전략

네트워크 기반 서비스 거부 (DoS) 공격을 방어에 대 한 Microsoft의 전략은 사용해 눈금과 글로벌 공간으로 인해 다소 고유 합니다. 이 배율 (공급자 또는 고객 조직) 몇 조직에 일치 시킬 수 있는 기법 및 전략을 활용 하는 Microsoft 수 있습니다. DoS 전략의 토대 사용해 전역 현재 상태를 활용 하 여 합니다. Microsoft는 귀하 (하는이 작성 하는 시점 18 개월 마다 주위 두배로 설정 하는) 중요 한 인터넷 현재 상태를 부여 세계의 기업 인터넷 공급자, (공용 및 전용) 피어 링 공급자 및 개인 예약 합니다. 매우 큰 노출 영역을 통해 공격을 처리 하는 Microsoft를 사용 하면 큰 현재 필요 합니다.

대규모 기업에서 사용 되는 다른 검색 및 완화 프로세스를 사용 하 여 Microsoft 고유 하므로를 제공 합니다. 이 전략은 사용해 여러 모서리를 통해 전역적으로 분산 된 완화는 물론 검색 및 완화 방법, 구분을 기반으로 합니다. 대부분의 기업은 검색 하 고 가장자리 공격을 방지 하는 타사 솔루션을 사용 합니다. 이 지 용량 증가으로 개인 또는 특정 가장자리에 대 한 모든 공격의 중요성 매우 낮은 했음을 지우기 되었습니다. 이 고유한 구성으로 인해 우리가 구분 하 여 검색 및 완화 구성 요소입니다. 전역 완화 가장자리를 유지 관리 하는 동안 자신의 채도 포인트에 더 가깝게에 공격을 검색할 수 있게 하는 다중 계층 감지를 배포 했습니다. 이 전략 여러 동시 공격을 처리할 수 있는 것을 보장 합니다.

이 공격 영역을 줄이는데 DoS 공격에 대 한 Microsoft에서 사용 되는 가장 효과적이 고 저렴 한 비용 방어 중 하나입니다. 이렇게 원치 않는 트래픽을 분석 처리 하 고 데이터 인라인 스크러빙 것과 반대로 가장자리에 놓을 수 있습니다.

공용 네트워크 인터페이스에 Microsoft에서 방화벽, 네트워크 주소 변환 및 IP 필터링 함수에 대 한 특수 용도의 보안 장치를 사용 합니다. 또한 전역 equal 비용 다중 경로 (ECMP) 라우팅을 사용 하 여 합니다. 전역 ECMP 라우팅은 서비스 연결에 대 한 여러 글로벌 경로 통해 하는 네트워크 프레임 워크입니다. 이러한 여러 경로 통해 서비스에 대 한 공격 신청을 공격 거-최종 사용자는 해당 지역에서 서비스에 연결할 다른 경로 사용 하는 다른 지역 해야이 공격에 의해 영향을 받지 않습니다 지역에 제한 해야 합니다. 또한 흐름 데이터, 성능 메트릭 및 기타 정보를 사용 하는 자체 내부 DoS 상관 및 검색 시스템을 개발 했습니다. Microsoft 네트워크에서 다양 한 지점에서 수집한 데이터를 분석 하는 Microsoft Azure 내에서 실행 되는 hyperscale 클라우드 서비스 및 서비스입니다. 크로스-작업량 DoS 사고 대응 팀 팀, 에스컬레이션을 위한 조건 및 다양 한 팀에 연락 하는 것에 대 한 및 문제 처리에 대 한 프로토콜에 걸쳐 역할 및 책임을 식별 합니다. 이러한 솔루션 DoS 공격에 대 한 네트워크 기반 보호를 제공 합니다.

마지막으로, 해당 프로토콜을 기반으로 최적화 된 임계값을 사용 하 여 클라우드 기반 작업 구성 및 대역폭 사용량 작업 부하를 고유 하 게 보호 해야 합니다.
