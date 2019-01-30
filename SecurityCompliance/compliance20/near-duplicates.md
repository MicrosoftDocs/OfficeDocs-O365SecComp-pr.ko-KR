---
title: 중복 검색 근처
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection: ''
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: ''
ms.openlocfilehash: a3f5945ee4ba0a1bc78ab6c8ccc9af934d392232
ms.sourcegitcommit: ee28ee2b2bdfd049333c2f495d7f7780d13af4a6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2019
ms.locfileid: "29608122"
---
# <a name="near-duplicate-detection"></a>중복 검색 근처

문서를 검토 하는 하위 집합 동일한 템플릿을 기반으로 쉽고 대개 같은 상용구 언어, 몇가지 차이가 있으므로 여기에 집합을 고려해 야 합니다. 검토자가 하위이 집합을 식별 하 고 철저 하 게, 그 중 하나를 검토 하 고 나머지 부분에 대 한 차이 검토 하 수, 자신이 것 하지 하지 않았을 모든 고유한 정보 빠르게 시간을 라인 걸리므로 표지를 표지 문서를 모두 읽을 수 하는 동안. 거의 중복 검색 함수와 비슷한 문서 보다 효율적으로 검토 프로세스 수를 함께 그룹화 합니다.

## <a name="how-does-it-work"></a>작동 방식

중복 검색 근처를 실행 하는 경우 시스템에 텍스트가 있는 모든 문서 구문 분석 합니다. 그런 다음, 해당 다음과 비슷한 집합 임계값 보다 크면 되는지 확인 하기 위해 각 장치에 대 한 모든 문서를 비교 합니다. 인 경우에 문서 함께 그룹화 됩니다. 모든 문서 비교 및 그룹화 된, 각 그룹에서이 문서는 "피벗";으로 표시 됩니다. 문서를 검토, 피벗을 먼저 검토 수 있으며 피벗 및 검토에 있는 문서 간의 차이에 초점을 맞추고 중복 집합 근처 같은 다른 문서를 검토 수 있습니다.