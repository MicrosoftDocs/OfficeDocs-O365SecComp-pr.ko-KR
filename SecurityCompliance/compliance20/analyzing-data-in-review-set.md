---
title: 고급 eDiscovery에서 검토 집합의 데이터 분석
ms.author: markjjo
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
ms.openlocfilehash: cfed07d473f2af367de4cb2e9fe924a29e4123cd
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/17/2019
ms.locfileid: "34155210"
---
# <a name="analyze-data-in-a-review-set-in-advanced-ediscovery"></a>고급 eDiscovery에서 검토 집합의 데이터 분석

수집 된 문서 수가 크면 검토 하는 것이 상당히 어려울 수 있습니다. 고급 eDiscovery에서는 문서를 분석 하 여 정보 손실 없이 검토할 문서 크기를 줄이고 일관 된 방식으로 문서를 구성 하는 데 도움이 되는 다양 한 도구를 제공 합니다. 이러한 기능에 대 한 자세한 내용은 다음 항목을 참조 하십시오.

- [중복에 가까운 검색](near-duplicates.md)

- [전자 메일 스레드](email-threading.md)

- [테마](themes.md)

검토 집합에서 데이터를 분석 하려면 다음을 수행 합니다.

1. 사례에 대 한 분석 설정을 구성 합니다. 자세한 내용은 [Configure search and analytics settings](configure-search-analytics-settings.md)을 참조 하십시오.

2. 분석 하려는 검토 집합을 엽니다.

3. **검토 설정 관리**를 클릭 합니다.

4. **분석**을 클릭 합니다.

사례에 대 한 **작업** 탭에서 분석 진행률을 확인할 수 있습니다.

 분석이 완료 되 면 분석 보고서를 보고, 분석 출력에 대 한 검토 집합 내에서 쿼리를 실행 하 고 ( [검토 집합 내의 쿼리](review-set-search.md)참조), 지정 된 문서의 관련 문서를 볼 수 있습니다 ( [검토 집합의 데이터 검토](reviewing-data-in-review-set.md)참조).

## <a name="analytics-report"></a>분석 보고서

검토 집합에 대 한 분석 보고서를 보려면:

1. 검토 집합을 엽니다.

2. **검토 설정 관리**를 클릭 합니다.

3. **보고서**를 클릭 합니다.

보고서에는 분석을 통해 다음과 같은 4 가지 구성 요소가 포함 됩니다.

- **분석 결과** -검토 집합에서 찾은 전자 메일 메시지, 첨부 파일 및 느슨한 문서 수입니다.

- **문서 (첨부 파일 제외)** -피벗, 중복 되는 항목에 대 한 고유 하지 않은 문서 또는 다른 문서와 정확히 일치 하는 복사본의 수입니다.

- **전자 메일** -inclusives, 포함 복사본, 포함 minuses 또는이 중 어느 것도 사용 되지 않은 전자 메일 메시지의 수입니다.

- **첨부 파일** -검토 집합에 있는 다른 전자 메일 첨부 파일의 고유 복사본 또는 중복 된 전자 메일 첨부 파일의 수입니다.