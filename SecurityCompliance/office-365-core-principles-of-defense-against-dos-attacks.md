---
title: 서비스 거부 공격에 대 한 방어의 Office 365 핵심 원리
ms.author: robmazz
author: robmazz
manager: laurawi
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.collection:
- Strat_O365_IP
- M365-security-compliance
description: Microsoft가 DoS (서비스 거부) 공격에 대 한 방어에서 absorption, 검색 및 완화의 핵심 원칙을 활용 하는 방법
ms.openlocfilehash: bbfffeaeb66fc83e80c274be9550a95dc8bd3f0d
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32262930"
---
# <a name="core-principles-of-defense-against-denial-of-service-attacks"></a>서비스 거부 공격에 대한 보안 핵심 원칙

네트워크 기반 DoS 공격 으로부터 방어할 때의 세 가지 핵심 원리는 Absorption, 검색 및 완화입니다.
Absorption가 검색 전에 수행 되 고 완화 되기 전에 검색이 수행 됩니다. DoS 공격에 대 한 최선의 방어는 Absorption입니다. 공격을 검색할 수 없는 경우에는이를 완화할 수 없습니다. 그러나 가장 작은 DoS 공격을 수용할 수 없는 경우에도 서비스는 공격을 감지할 수 있을 정도로 오래 지속 되지 않습니다.

물론 대부분의 조직에서는 기술 및 기술 기술에 상당한 투자가 필요 하기 때문에, 일반적으로 대부분의 조직이 DoS 공격을 economically 하는 데 필요한 지나친 용량을 구입 하는 것은 아닙니다. 이는 Microsoft 클라우드 서비스를 사용 하는 경우의 보안 혜택 중 하나를 강조 표시 합니다. 서비스를 대규모로 사용 하면 클라우드 고객에 게 비용 효율적인 방식으로 강력한 네트워크 보호 기능을 제공할 수 있습니다. 그러나이 크기의 경우에도 absorption, 검색 및 완화 간의 균형이 유지 되어야 합니다. 이러한 균형을 확인 하기 위해 공격의 증가율을 조사 하 여 얼마나 많은 정보를 처리 해야 하는지 예측 합니다.

검색은 cat and 마우스 게임입니다. 사용자가 공격 하는 새로운 방법을 끊임없이 확인 하거나 시스템을 처치 해야 합니다. > 완화-> 검색-> 완화 등은 무한정 계속 되는 정품, 영구 상태입니다.

## <a name="defending-against-dos-attacks"></a>DoS 공격 으로부터 방어

DoS 공격을 성공적으로 방어 하려면 초기 검색이 필수적입니다. 시스템이 너무 defenders 전에 공격을 감지 하 여 응답 계획을 실행할 수 있습니다.

다음 공식은 DoS 공격의 영향에 대 한 시간을 예상 하는 데 도움이 됩니다.

   **최대 용량 (바이트/초)/증가율 (바이트/초) = 영향에 대 한 시간 (바이트/초)**

시간에 영향을 줄 수 있는 시간까지 검색을 수행 하는 경우 DoS 공격이 성공할 가능성이 높습니다. 시간에 영향을 미치는 시간을 검색할 때까지 발생 하는 서비스는 완화 전략을 사용 하는 경우 온라인 및 액세스 가능한 상태로 유지 해야 합니다. 따라서 DoS 공격 으로부터 보호 하기 위해 두 가지 작업을 수행할 수 있습니다.
- 용량을 늘려 최대 용량에 대 한 천장을 증대 시켜 공격을 감지 하는 데 더 많은 시간을 제공 합니다. 사용자나
- 검색 하는 데 걸리는 시간을 단축 합니다.

용량 증가는 회계에 직접적인 영향을 줍니다. 고객은 기본 absorption 용량을 개발 하 여 특정 수준의 DoS 공격을 계속 받을 수 있도록 하는 것이 좋습니다. 각 고객은 노출, 위험 및 재무 outlay에 대 한 자체 임계값을 가지 며 실제 absorption 용량은 고객 마다 다를 수 있습니다. 경제적 이유로 궁극적으로 시간을 절감 하는 방법으로 연구 및 시간을 투자 하는 것은 대개 비용 면에서 효과적으로 방어 하는 것입니다.
