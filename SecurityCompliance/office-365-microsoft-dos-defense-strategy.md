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
# <a name="microsofts-denial-of-service-defense-strategy"></a><span data-ttu-id="ef39d-103">Microsoft의 서비스 거부 방어 전략</span><span class="sxs-lookup"><span data-stu-id="ef39d-103">Microsoft's Denial-of-Service Defense Strategy</span></span>

<span data-ttu-id="ef39d-p101">네트워크 기반 서비스 거부 (DoS) 공격을 방어에 대 한 Microsoft의 전략은 사용해 눈금과 글로벌 공간으로 인해 다소 고유 합니다. 이 배율 (공급자 또는 고객 조직) 몇 조직에 일치 시킬 수 있는 기법 및 전략을 활용 하는 Microsoft 수 있습니다. DoS 전략의 토대 사용해 전역 현재 상태를 활용 하 여 합니다. Microsoft는 귀하 (하는이 작성 하는 시점 18 개월 마다 주위 두배로 설정 하는) 중요 한 인터넷 현재 상태를 부여 세계의 기업 인터넷 공급자, (공용 및 전용) 피어 링 공급자 및 개인 예약 합니다. 매우 큰 노출 영역을 통해 공격을 처리 하는 Microsoft를 사용 하면 큰 현재 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="ef39d-p101">Microsoft's strategy for defending against network-based denial-of-service (DoS) attacks is somewhat unique due to our scale and global footprint. This scale allows Microsoft to utilize strategies and techniques that few organizations (providers or customer organizations) can match. The cornerstone of our DoS strategy is leveraging our global presence. Microsoft engages with Internet providers, peering providers (public and private), and private corporations all over the world, giving us a significant Internet presence (which as of this writing, doubles around every 18 months). Having such a large presence enables Microsoft to absorb attacks across a very large surface area.</span></span>

<span data-ttu-id="ef39d-p102">대규모 기업에서 사용 되는 다른 검색 및 완화 프로세스를 사용 하 여 Microsoft 고유 하므로를 제공 합니다. 이 전략은 사용해 여러 모서리를 통해 전역적으로 분산 된 완화는 물론 검색 및 완화 방법, 구분을 기반으로 합니다. 대부분의 기업은 검색 하 고 가장자리 공격을 방지 하는 타사 솔루션을 사용 합니다. 이 지 용량 증가으로 개인 또는 특정 가장자리에 대 한 모든 공격의 중요성 매우 낮은 했음을 지우기 되었습니다. 이 고유한 구성으로 인해 우리가 구분 하 여 검색 및 완화 구성 요소입니다. 전역 완화 가장자리를 유지 관리 하는 동안 자신의 채도 포인트에 더 가깝게에 공격을 검색할 수 있게 하는 다중 계층 감지를 배포 했습니다. 이 전략 여러 동시 공격을 처리할 수 있는 것을 보장 합니다.</span><span class="sxs-lookup"><span data-stu-id="ef39d-p102">Given our unique nature, Microsoft uses detection and mitigation processes that differ from those used by large enterprises. Our strategy is based on a separation of detection and mitigation, as well as global, distributed mitigation through our many edges. Many enterprises use third-party solutions which detect and mitigate attacks at the edge. As our edge capacity grew, it became clear that the significance of any attack against individual or particular edges was very low. Because of our unique configuration, we have separated the detection and mitigation components. We have deployed multi-tiered detection that enables us to detect attacks closer to their saturation points while maintaining global mitigation at the edge. This strategy ensures we can handle multiple simultaneous attacks.</span></span>

<span data-ttu-id="ef39d-p103">이 공격 영역을 줄이는데 DoS 공격에 대 한 Microsoft에서 사용 되는 가장 효과적이 고 저렴 한 비용 방어 중 하나입니다. 이렇게 원치 않는 트래픽을 분석 처리 하 고 데이터 인라인 스크러빙 것과 반대로 가장자리에 놓을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ef39d-p103">One of the most effective and low-cost defenses employed by Microsoft against DoS attacks is to reduce our attack surface. Doing so enables us to drop unwanted traffic at the edge, as opposed to analyzing, processing and scrubbing the data inline.</span></span>

<span data-ttu-id="ef39d-p104">공용 네트워크 인터페이스에 Microsoft에서 방화벽, 네트워크 주소 변환 및 IP 필터링 함수에 대 한 특수 용도의 보안 장치를 사용 합니다. 또한 전역 equal 비용 다중 경로 (ECMP) 라우팅을 사용 하 여 합니다. 전역 ECMP 라우팅은 서비스 연결에 대 한 여러 글로벌 경로 통해 하는 네트워크 프레임 워크입니다. 이러한 여러 경로 통해 서비스에 대 한 공격 신청을 공격 거-최종 사용자는 해당 지역에서 서비스에 연결할 다른 경로 사용 하는 다른 지역 해야이 공격에 의해 영향을 받지 않습니다 지역에 제한 해야 합니다. 또한 흐름 데이터, 성능 메트릭 및 기타 정보를 사용 하는 자체 내부 DoS 상관 및 검색 시스템을 개발 했습니다. Microsoft 네트워크에서 다양 한 지점에서 수집한 데이터를 분석 하는 Microsoft Azure 내에서 실행 되는 hyperscale 클라우드 서비스 및 서비스입니다. 크로스-작업량 DoS 사고 대응 팀 팀, 에스컬레이션을 위한 조건 및 다양 한 팀에 연락 하는 것에 대 한 및 문제 처리에 대 한 프로토콜에 걸쳐 역할 및 책임을 식별 합니다. 이러한 솔루션 DoS 공격에 대 한 네트워크 기반 보호를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="ef39d-p104">At the interface with the public network, Microsoft uses special-purpose security devices for firewall, network address translation, and IP filtering functions. We also use global equal-cost multi-path (ECMP) routing. Global ECMP routing is a network framework that ensures there are multiple global paths to reach a service. Thanks to these multiple paths, an attack against the service should be limited to the region from which the attack originates – other regions should be unaffected by this attack, as end users would use other paths to reach the service in those regions. We have also developed our own internal DoS correlation and detection system that uses flow data, performance metrics and other information. This is a hyperscale cloud service running within Microsoft Azure which analyzes data collected from various points on Microsoft networks and services. A cross-workload DoS incident response team identifies the roles and responsibilities across teams, the criteria for escalations, and the protocols for engaging various teams and for incident handling. These solutions provide network-based protection against DoS attacks.</span></span>

<span data-ttu-id="ef39d-126">마지막으로, 해당 프로토콜을 기반으로 최적화 된 임계값을 사용 하 여 클라우드 기반 작업 구성 및 대역폭 사용량 작업 부하를 고유 하 게 보호 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ef39d-126">Finally, cloud-based workloads are configured with optimized thresholds based on their protocol and bandwidth usage needs to uniquely protect that workload.</span></span>
