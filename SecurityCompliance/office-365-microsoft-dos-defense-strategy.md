---
title: Office 365 Microsoft의 DoS 방어 전략
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
ms.collection:
- Strat_O365_IP
- M365-security-compliance
description: DoS (서비스 거부) 공격을 처리 하기 위한 Microsoft의 방어 전략에 대 한 개요입니다.
ms.openlocfilehash: 0b0cf20e6282c85ede05edda3979ae5a7295ac78
ms.sourcegitcommit: c94cb88a9ce5bcc2d3c558f0fcc648519cc264a2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/20/2019
ms.locfileid: "30090820"
---
# <a name="microsofts-denial-of-service-defense-strategy"></a>Microsoft의 서비스 거부 방어 전략

네트워크 기반 DoS (서비스 거부) 공격을 방어 하기 위한 Microsoft의 전략은 규모와 전역 공간에 따라 다릅니다. 이 확장을 통해 Microsoft는 조직 (공급자 또는 고객 조직)이 일치 시킬 수 있는 전략과 기법을 활용 합니다. DoS 전략의 세밀는 글로벌 현재 상태를 활용 하 고 있습니다. Microsoft는 인터넷 공급자, 피어 링 공급자 (공개 및 개인) 및 사설 회사 모두를 대상으로 하며,이에 대 한 인터넷 현재 상태 (이 경우에는 약 18 개월 마다 double)가 제공 됩니다. 이러한 대규모 현재 상태를 유지 하는 경우 Microsoft에서 매우 큰 영역에 대 한 공격을 통과할 수 있습니다.

고유 특성이 제공 됨에 따라 Microsoft는 대규모 기업에서 사용 하는 것과는 다른 검색 및 완화 프로세스를 사용 합니다. 이 전략은 검색 및 완화의 분리, 그리고 다양 한 가장자리를 통한 분산 완화가 전체적으로 결정 됩니다. 대부분의 기업에서는 타사 솔루션을 사용 하 여 edge에서 공격을 감지 하 고 완화 합니다. edge 용량이 증가 함에 따라 개별 또는 특정 모서리에 대 한 공격의 중요성은 매우 낮음을 알게 되었습니다. 고유한 구성으로 인해 검색 및 완화 구성 요소를 분리 했습니다. 우리는 멀티 계층 검색을 배포한 후에는에 지에 대 한 전체 완화를 유지 하면서 해당 포화 지점에 가까운 공격을 검색할 수 있도록 합니다. 이 전략을 사용 하면 여러 동시 공격을 처리할 수 있습니다.

DoS 공격에 대해 Microsoft가 사용 하는 가장 효과적이 고 경제적인 방어 중 하나는 공격 허점을 줄이기 위한 것입니다. 이렇게 하면 데이터를 분석, 처리 및 삭제 하는 것과 반대로,에 지에 원치 않는 트래픽을 삭제할 수 있습니다.

공용 네트워크와의 인터페이스에서 Microsoft는 방화벽, 네트워크 주소 변환 및 IP 필터링 기능에 특수 용도의 보안 장치를 사용 합니다. 또한 글로벌 동일한 ecmp (다중 경로) 라우팅을 사용 합니다. 전역 ecmp 라우팅은 서비스에 연결할 수 있는 여러 전역 경로가 있는지를 확인 하는 네트워크 프레임 워크입니다. 이러한 여러 경로에서 서비스에 대 한 공격은 공격을 시작 하는 지역으로 제한 되어야 함-최종 사용자는 다른 경로를 사용 하 여 해당 지역의 서비스에 연결할 수 있습니다. 또한 흐름 데이터, 성능 메트릭 및 기타 정보를 사용 하는 내부 DoS 상관 관계 및 검색 시스템을 개발 했습니다. 이는 microsoft Azure 내에서 실행 되는 스케일 클라우드 서비스 이며,이는 마이크로소프트 네트워크 및 서비스의 여러 지점에서 수집한 데이터를 분석 하는 데 유용 합니다. 작업 부하를 수행 하는 DoS 인시던트 대응 팀은 팀 전체의 역할과 책임, 에스컬레이션 기준 및 다양 한 팀을 사용 하 고 인시던트를 처리 하기 위한 프로토콜을 식별 합니다. 이러한 솔루션은 DoS 공격 으로부터 네트워크 기반 보호를 제공 합니다.

마지막으로 클라우드 기반 워크 로드는 해당 프로토콜에 따라 최적화 된 임계값을 사용 하 여 구성 되며 해당 작업을 고유 하 게 보호 하기 위해 대역폭 사용량이 필요 합니다.
