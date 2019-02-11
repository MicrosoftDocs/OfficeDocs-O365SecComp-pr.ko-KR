---
title: 고급 eDiscovery (미리 보기)에서 작업 집합의 데이터를 분석 합니다.
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
ms.openlocfilehash: 68a8b7586700a9bffe78f2b3a4ff419a1f85ba8a
ms.sourcegitcommit: 7e2a0185cadea7f3a6afc5ddc445eac2e1ce22eb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/11/2019
ms.locfileid: "29695144"
---
# <a name="analyze-data-in-a-working-set-in-advanced-ediscovery-preview"></a>고급 eDiscovery (미리 보기)에서 작업 집합의 데이터를 분석 합니다.

수집 된 문서 수 클 경우 모두 검토 하는 것이 어려울 수 있습니다. 고급 eDiscovery (미리 보기)는 다양 한 문서 정보를 손실 없이 검토 하 고 일관 된 방식으로 문서를 구성 하는데 도움이 되는 문서의 양을 줄일를 분석 하는 도구를 제공 합니다. 이러한 기능에 대 한 자세한 내용은 참조 합니다.

- [중복에 가까운 검색](near-duplicates.md)
- [전자 메일 스레드](email-threading.md)
- [테마](themes.md)

작업 집합의 데이터를 분석 합니다.

1. 사례 분석 설정을 구성 합니다. 자세한 내용은 [검색 및 분석 설정 구성을](configure-search-analytics-settings.md)참조 하십시오.
2. 분석 하려는 작업 집합을 엽니다.
3. "관리 작업 집합"로 이동 합니다.
4. "분석"을 클릭 합니다.

사용자의 경우에서 작업 탭에는 분석의 진행률을 확인할 수 있습니다.

 분석 완료 되 면 분석 보고서를 볼 수 있습니다, 사용자 작업 내에서 실행된 된 쿼리 (대 한 자세한 내용은 참조 하십시오 [설정 하면 작업 내에서 쿼리](working-set-search.md)) 분석의 출력에 설정 하 고 (자세한 내용은 참조 [에 대 한 특정 문서의 관련된 문서를 참조 하십시오. 작업 집합의 데이터를 검토](reviewing-data-in-working-set.md)).

## <a name="analytics-report"></a>분석 보고서

작업 집합에 대 한 분석 보고서를 보려면

1. 작업 집합을 엽니다.
2. "관리 작업 집합"로 이동 합니다.
3. "보고서"를 클릭 합니다.

보고서에는 4 개의 구성 요소가 분석에서:

- **분석 하 여** -얼마나 많은 전자 메일, 첨부 파일 및 문서를 느슨한 작업 집합에서 발견 되었습니다.

- **문서 (첨부 파일은 제외)** -얼마나 많은 느슨한 문서 위치별, 피벗의 중복 되는 값 이나 다른 문서를 정확 하 게 복제 근처에 고유한 했습니다.

- **전자 메일** -inclusives, 복사본 (포함), (포함) minuses 또는 위의 사항 얼마나 많은 전자 메일이 했습니다.

- **첨부 파일** -얼마나 많은 전자 메일 첨부 된 고유 또는 작업 집합 내에서 서로 다른 전자 메일 첨부 파일의 복제 합니다.