---
title: 분석을 실행 하 여 더 빠른 조사
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
ms.openlocfilehash: 9516035fb6c758fdff1852249fff2815f19af559
ms.sourcegitcommit: 2c5834235c32b2616e1813ce24eeb3419a09629f
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/02/2019
ms.locfileid: "31030347"
---
# <a name="run-analytics-to-investigate-faster"></a>분석을 실행 하 여 더 빠른 조사

증거 수집이 크면 검토 하기가 어려울 수 있습니다. 증명 정보 집합에 동일 하거나 유사한 전자 메일 메시지 또는 문서의 복사본이 여러 개 포함 되는 경우가 많습니다. 데이터 조사 (미리 보기)는 정보 손실 없이 검토 해야 하는 문서 크기를 줄이는 데 도움이 되는 다양 한 분석 도구를 제공 합니다. 이러한 기능에 대 한 자세한 내용은 다음 항목을 참조 하십시오.

- [중복에 가까운 검색](near-duplicates.md)

- [전자 메일 스레드](email-threading.md)

- [테마](themes.md)

증거 집합에서 데이터를 분석 하려면 다음을 수행 합니다.

1. 조사에 대 한 분석 설정을 구성 합니다. 자세한 내용은 [Configure search and analytics settings](configure-search-analytics-settings.md)을 참조 하십시오.

2. 증거 집합을 엽니다.

3. **증거 관리**를 클릭 합니다.

4. **분석**에서 **분석**을 클릭 합니다.

조사에서 **작업** 탭의 분석 진행률을 확인할 수 있습니다. 트리거된 작업 유형은 **analytics를 실행**하는 이름입니다.

 분석이 완료 되 면 오른쪽 패널에 있는 검토 중인 문서와 정확히 일치 하는 중복 항목 또는 거의 중복 항목 목록을 볼 수 있습니다. 보고 있는 문서의 모든 중복 항목을 선택 하려면이 패널을 사용 하 여 작업을 쉽게 수행할 수 있습니다. 이 패널의 다른 기능에 대 한 자세한 내용은 [Review data in 증거](review-data-in-evidence.md)를 참조 하십시오. 

테마와 같은 분석 출력을 사용 하 여 증명 정보 내에서 추가 쿼리를 실행할 수도 있습니다. 자세한 내용은 [데이터를 증거에 쿼리](evidence-query.md)를 참조 하십시오.

## <a name="analytics-report"></a>분석 보고서

증명 정보에 대 한 분석 보고서를 보려면:

1. 증거 집합을 엽니다.

2. **증거 관리**를 클릭 합니다.

3. **분석**에서 **보고서 보기**를 클릭 합니다.

보고서에는 분석을 통해 다음과 같은 4 가지 구성 요소가 포함 됩니다.

- **분석 결과** -증명 정보 집합에 있는 원시 전자 메일, 첨부 파일 및 문서 수입니다.

- **전자 메일** -inclusives, 포괄 minuses, 포괄 복사본 또는 위의 값이 없는 eamil 메시지의 수입니다.
   - Inclusives: 이전 기록을 모두 포함 하며 검토가 필요한 전자 메일 스레드의 마지막 메시지입니다.
   - 포함 minuses: 스레드가 검토 해야 하는 다른 첨부 파일이 하나 이상 포함 된 메시지입니다.
   - 포함 복사본: 다른 포함 또는 포함 마이너스 메시지 (제목 및 본문)의 복사본 인 메시지입니다.

- **첨부 파일** -동일한 증거 내에 있는 다른 전자 메일 첨부 파일의 고유 또는 중복 되는 전자 메일 첨부 파일의 수입니다.

- **문서 (전자 메일 첨부 파일 제외)** -검토 해야 하는 고유 문서 수 (예: 거의 중복 된 집합의 가장 대표적인 문서 또는 다른 문서의 정확한 중복)입니다.