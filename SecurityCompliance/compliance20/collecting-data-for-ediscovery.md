---
title: Advanced eDiscovery에서 사례에 대 한 데이터 수집
ms.author: esclee
author: markjjo
manager: laurawi
ms.date: ''
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: ''
ms.openlocfilehash: 8e67c3c8a693e627bade9e581f0f1e246bf6802a
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/17/2019
ms.locfileid: "34151890"
---
# <a name="collect-data-for-a-case-in-advanced-ediscovery"></a>Advanced eDiscovery에서 사례에 대 한 데이터 수집

해당 사례에 관심이 있는 custodians 및 데이터 원본을 파악 한 후에는 delve에 사용할 문서 집합을 식별 해야 합니다. 고급 eDiscovery의 검색 도구를 사용 하 여 Office 365에서 custodial 및 비 custodial 위치를 확인할 수 있습니다.

검색을 실행 한 후 검색 쿼리와 일치 하는 항목이 가장 많은 위치와 같은 검색 된 항목에 대 한 통계를 볼 수 있습니다. 또한 결과의 하위 집합을 미리 볼 수도 있습니다. 추가로 확인할 문서 집합을 식별 한 경우 수집 및 처리할 검토 집합에 검색 결과를 추가할 수 있습니다.

## <a name="create-a-search"></a>Create a search

검색 탭에서 **새 검색** 을 클릭 하면 검색을 만드는 과정을 안내 하는 마법사가 시작 됩니다. **** 검색을 만드는 방법에 대 한 자세한 내용은 [create a search를 검색 하 여 데이터 수집](create-search-to-collect-data.md)을 참조 하십시오.

검색을 만든 후에는 세부 정보가 포함 된 플라이 아웃 페이지가 표시 됩니다. 검색이 아직 완료 되지 않았으므로 **통계** 및 **미리 보기** 단추가 초기에 회색으로 표시 됩니다. 검색의 진행 상태를 추적할 수 있습니다 (검색 탭) **** .

## <a name="view-search-results-and-statistics"></a>검색 결과 및 통계 보기
콘텐츠 검색에는 통계 (예측) 및 미리 보기의 두 가지 구성 요소가 있습니다. 이러한 각 구성 요소가 완료 되 면 **검색** 탭의 해당 열에 **제출** 됨에서 **진행 중** 에서 **완료**됨으로 변경 된 상태가 표시 됩니다.

검색 예측이 완료 되 면 검색을 클릭 하 여 플라이 아웃 페이지를 표시 하 고 검색 결과에 대 한 일부 높은 수준의 통계를 표시 합니다. 이 시점에서 **통계** 단추가 활성화 됩니다. 이 도구를 클릭 하 여 다음과 같은 검색 통계를 볼 수 있습니다.

- 요약
- 상위 위치
- 쿼리하도록

검색 통계에 대 한 자세한 내용은 [검색 통계](search-statistics.md)를 참조 하세요.

미리 보기가 완료 되 면 **미리 보기** 단추가 활성화 됩니다. 이 도구를 클릭 하 여 결과의 샘플링할 하위 집합을 미리 봅니다.

## <a name="adding-search-results-to-a-review-set"></a>검토 집합에 검색 결과 추가

검색의 전체 결과를 수집 하 고 처리할 준비가 되 면 검토 집합에 추가 하 여 검색할 수 있습니다. 자세한 내용은 [검토 집합에 데이터 추가](add-data-to-review-set.md)를 참조 하십시오. 