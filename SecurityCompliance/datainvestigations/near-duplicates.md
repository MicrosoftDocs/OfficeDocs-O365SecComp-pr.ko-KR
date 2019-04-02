---
title: 중복에 가까운 검색
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: ''
ms.openlocfilehash: 941809193a3342d8c7b9de991370848aee4af070
ms.sourcegitcommit: 2c5834235c32b2616e1813ce24eeb3419a09629f
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/02/2019
ms.locfileid: "31030377"
---
# <a name="near-duplicate-detection"></a>중복에 가까운 검색

하위 집합이 같은 서식 파일을 기반으로 하며, 여기에 몇 가지 차이가 있는 같은 상용구 언어를 사용 하는 검토할 문서 집합을 가정해 봅니다. 검토자가이 하위 집합을 식별 하 고, 그 중 하나를 철저히 검토 하 고, 나머지에 대 한 차이를 검토 하 고, 모든 문서를 읽을 수 있는 시간만 차지 하는 동안에는 고유한 정보를 놓치지 않을 수 있습니다. 유사 중복 검색 그룹은 검토 프로세스의 효율성을 높이기 위해 비슷한 문서를 함께 설명 합니다.

## <a name="how-does-it-work"></a>작동 방식

근접 중복 검색이 실행 되 면 시스템은 텍스트를 사용 하 여 모든 문서를 구문 분석 합니다. 그런 다음 모든 문서를 서로 비교 하 여 유사도가 설정 된 임계값 보다 큰지 여부를 확인 합니다. 이 경우 문서가 함께 그룹화 됩니다. 모든 문서를 비교 하 고 그룹화 한 후에는 각 그룹의 문서가 "피벗"으로 표시 됩니다. 문서를 검토할 때 검토 중인 피벗 및 문서 간의 차이에 초점을 맞추어, 먼저 피벗을 검토 하 고 동일한 근거리 복제 세트로 다른 문서를 검토할 수 있습니다.