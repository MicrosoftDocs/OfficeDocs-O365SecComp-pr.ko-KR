---
title: 메일을 빨간색으로 플래그 지정 했을 때 정책 및 보호 기능 결합 방법
description: 전자 메일이 맬웨어, 스팸, 높은 신뢰도 스팸, 피싱, EOP 및/또는 ATP에 의해 대량으로 표시 될 때 적용 되는 정책 및 수행 해야 하는 작업을 설명 합니다.
keywords: 보안, 맬웨어, Microsoft 365, M365, 보안 센터, ATP, Windows Defender atp, Office 365 atp, Azure ATP
ms.author: tracyp
author: MSFTTracyp
manager: laurawi
ms.date: 03/26/2019
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- M365-security-compliance
ms.openlocfilehash: 7aa0f89eed379273cb069cd65c083749a9552e91
ms.sourcegitcommit: a79eb9907759d4cd849c3f948695a9ff890b19bf
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/26/2019
ms.locfileid: "30926473"
---
# <a name="what-policy-applies-when-multiple-protection-methods-and-detection-scans-run-on-your-email"></a>전자 메일에 대해 여러 보호 방법 및 검색 검사가 실행 될 때 적용 되는 정책

받는 메일에는 여러 형태의 보호 (예: EOP *및* ATP)가 플래그 지정 되어 있을 수 있으며, 스팸 *및* 피싱 등의 여러 검색 검사를 수행할 수 있습니다. atp 고객에 게는 atp 피싱 방지 정책, EOP 고객을 위한 EOP 피싱 방지 정책 등이 있기 때문에 이러한 일이 가능 합니다. 또한이는 메시지가 맬웨어, 피싱 및 사용자 가장을 위해 여러 검색 검색을 탐색할 수도 있음을 의미 합니다. 이 모든 활동이 제공 되 면 어떤 정책이 적용 되는지 약간의 혼동이 있을 수 있습니다.

일반적으로 메시지에 적용 되는 정책은 **CAT (Category)** 속성의 **스팸 방지-Report** 헤더에서 식별 됩니다. 피싱 방지 정책이 여러 개 있는 경우 우선 순위가 가장 높은 정책 중 하나가 적용 됩니다.

아래 정책은 _모든 조직_에 적용 됩니다.

|우선 순위 |정책  |범주  |관리 되는 위치 |
|---------|---------|---------|---------|
|개     | 맬웨어      | MALW      | 맬웨어 정책   |
|2     | 피싱     | PHSH     | 스팸 필터 정책 구성     |
|3(sp3)     | 높은 정확도 스팸      | HSPM        | 스팸 필터 정책 구성        |
|1-4     | 스푸핑        | 스푸핑        | 피싱 방지 정책, 스푸핑 인텔리전스        |
|2-5     | 스팸         | SPM         | 스팸 필터 정책 구성         |
|번     | 대량         | 대량        | 스팸 필터 정책 구성         |

또한 이러한 정책은 _ATP가 있는 조직_에 적용 됩니다.

|우선 순위 |정책  |범주  |관리 되는 위치 |
|---------|---------|---------|---------|
|연중     | 도메인 가장         | DIMP         | Office 365 ATP 피싱 방지 및 피싱 방지 정책 설정        |
|8     | 사용자 가장        | UIMP         | Office 365 ATP 피싱 방지 및 피싱 방지 정책 설정         |

예를 들어 두 개의 정책이 있는 경우 다음을 수행 합니다.

|정책  |우선 순위  |사용자/도메인 가장  |스푸핑 방지  |
|---------|---------|---------|---------|
|A     | 개        | 켜짐        |해제         |
|B     | 2        | 해제        | 켜짐        |

메시지가 _사용자 가장_ 및 _스푸핑_ (위의 표에 나오는 스푸핑 방지 참조)으로 식별 되 고 정책 a로 범위가 지정 된 동일한 사용자 집합에 정책 B가 적용 되 면 해당 메시지의 플래그를 설정 하 고 _위장_로 취급 하지만이는 그렇지 않습니다. 스푸핑 방지 기능이 해제 되어 있고 **스푸핑이 보다 높은 우선 순위 (8)에서 실행**되므로 작업이 적용 됩니다.

다른 유형의 피싱 정책이 적용 되도록 하려면 다양 한 정책이 적용 되는 사용자의 설정을 조정 해야 합니다.



