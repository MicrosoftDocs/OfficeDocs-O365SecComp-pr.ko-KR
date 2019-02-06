---
title: 서비스 거부 공격에 대 한 방어의 주요 원칙을 office 365
ms.author: robmazz
author: robmazz
manager: laurawi
audience: ITPro
ms.topic: article
ms.service: Office 365 Administration
localization_priority: None
search.appverid:
- MET150
ms.collection: Strat_O365_Enterprise
description: 어떻게 Microsoft 통해, 검색 및 서비스 거부 (DoS) 공격에 대 한 해당 방어에 완화의 핵심 원칙을 활용 합니다.
ms.openlocfilehash: e313d5514e9bc493db78bebffca24a0fae4cbca7
ms.sourcegitcommit: a64af0ebd0b03e4a5e60a33e9108c44c7d74f356
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/05/2019
ms.locfileid: "29741101"
---
# <a name="core-principles-of-defense-against-denial-of-service-attacks"></a>서비스 거부 공격에 대한 보안 핵심 원칙

세 개 코어 통해, 검색 및 완화 방법 모두 네트워크 기반 DoS 공격을 방어 원칙입니다. 통해 검색, 이전에 발생 하 고 완화 하기 전에 수행 되는 검색 합니다. 통해는 DoS 공격에 대 한 최상의 방어입니다. 공격을 감지할 수 없는 완화할 수 없습니다. 하지만 DoS 공격 가장 작은 값을 전달 수 없음, 서비스 감지 되지 않을 공격에 대 한 충분 한 시간 살아남기가 이동 되지 않습니다.

물론 않은 일반적으로 대부분의 조직에서는이 기술 및 기술에 상당한 투자의 요구에 따라 DoS 공격을 처리 하는 데 필요한 여분의 용량을 구입 하는 것이 불가능 합니다. 이 강조 표시 하는 Microsoft 클라우드 서비스를 사용 하는 보안 이점 중 하나 서비스에 대 한 그 규모 비용 효율적인 방식으로 강력한 네트워크 보호 클라우드 고객에 게 제공할 수 있습니다. 하지만 수직 확장의도 하지만 여전히 있어야 통해, 검색 및 완화 방법 간의 균형 합니다. 해당 간의 균형을 찾으려고 있어 병합할 해야 얼마나 예측 하는 공격 증가율을 검토 합니다.

검색은 cat-and-mouse 게임입니다. 새로운 방법으로 사용자는 하면 공격 또는 시스템 물리 하려고를 지속적으로 유사 해야 합니다. 검색-gt_ 완화-gt_ 검색-gt_ Mitigate 등 무기한 계속 하는 영구, 영구 상태가 됩니다.

## <a name="defending-against-dos-attacks"></a>DoS 공격에 대 한 방어

DoS 공격을 성공적으로 방어를 초기 검색 반드시 필요 합니다. 시스템에 병목 현상이 발생 하기 전에 공격을 감지, 하 여 방어 대응 계획을 실행할 수 있습니다.

다음 수식을 DoS 공격에 영향을 줄에 시간에 근접 한 여러 하는데 도움이 됩니다.

   **최대 용량 (바이트/초)에 바이트/초) (에서 등급을 성장 / 바이트/초) (에 영향을 시간 =**

것일 수 검색 시간에 영향을 시간 후 발생 하는 경우에 DoS 공격 성공적으로 수행 됩니다. 검색 시간에 영향을 시간 전에 발생 하는 경우 온라인 및 완화 전략을 사용 하는 경우에 액세스할 공격 서비스 유지 되어야 합니다. 따라서 다음과 같은 사항을 두 DoS 공격을 방어을 수행할 수 있습니다.
- 거듭제곱할 (차례 대로 제공 하는 공격을 감지 하는 시간이 더) 최대 용량;의 최대 용량 증가 또는
- 검색 하는 시간을 줄입니다.

용량을 늘리는 가장 영향이 직접 회계 합니다. 고객 최소한의 기본 통해를 개발 하는 것이 좋습니다 용량 일부 수준의 DoS 공격을 살아남기 수 있는지 확인 합니다. 각 고객에 게 노출, 위험 및 재무 들이지에 대 한 자신의 임계값으로 실제 통해 용량에서 고객을 고객을 달라 집니다. 궁극적으로, 경제적인 이유로 연구 (영문) 및 시간을 검색 하려면 시간을 줄이는 방법에 대 한 투자는 일반적으로 가장 경제적인 방어 합니다.
