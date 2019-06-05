---
title: 검토 집합에 대 한 검색 용어 보고서 생성
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
ROBOTS: NOINDEX, NOFOLLOW
description: ''
ms.openlocfilehash: 877c0017359ab9193c4cae81cbef4240909053a8
ms.sourcegitcommit: e323610df2df71c84f536e8a38650d33d8069e41
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/04/2019
ms.locfileid: "34714997"
---
# <a name="generate-search-term-report-for-a-review-set"></a>검토 집합에 대 한 검색 용어 보고서 생성

EDiscovery에서는 문서를 쿼리 하는 데 가장 자주 사용 되는 조건 중 하나는 키워드 검색 용어를 사용 하는 것입니다. 사례에 중요 한 특정 키워드 ( *용어*라고도 함)를 포함 하는 문서를 식별 하 여 검토자가 해당 사용자가 직면 하 고 있는 항목에 대 한 높은 수준의 이해를 시작할 수 있습니다. Microsoft 365의 고급 eDiscovery에서는 검토 집합 내의 저장 된 쿼리에 검색 용어 보고서를 생성 하 여이 작업을 정확히 수행할 수 있습니다.

## <a name="step-1-create-a-saved-query-in-the-review-set"></a>1 단계: 검토 집합에 저장 된 쿼리 만들기

의미 있는 검색 용어 보고서를 생성 하려면 검토 집합에서 검색 용어 보고서를 생성 하려는 문서 집합을 정의 하는 저장 된 쿼리를 만듭니다. 예를 들어 키워드 조건 카드를 사용 하 여 날짜 범위 또는 실제 검색 용어 집합을 사용 하 여 쿼리를 만들 수 있습니다. 집합 쿼리 검토에 대해 자세히 알아보려면 [검토 집합에서 데이터 쿼리](review-set-search.md)를 참조 하십시오.

## <a name="step-2-generate-a-search-term-report"></a>2 단계: 검색 용어 보고서 생성

1 단계에서 만든 저장 된 쿼리의 상황에 맞는 메뉴를 통해 또는 검색 용어 보고서 관리 콘솔을 통해 검색 용어 보고서를 생성 하는 두 가지 방법이 있습니다.

- 상황에 맞는 메뉴를 사용 하려면 1 단계에서 만든 저장 된 쿼리의 상황에 맞는 메뉴를 열고 **검색 용어 보고서 생성**을 클릭 합니다.

- 관리 콘솔을 사용 하려면 **검토 설정 관리 > 검색 용어 보고서 보기로**이동 하 여 **새로 만들기**를 클릭 한 다음 1 단계에서 만든 저장 된 쿼리를 선택 합니다.

그런 다음 보고할 용어를 각각의 줄 바꿈으로 구분 하 여 입력 합니다. 1 단계에서 만든 저장 된 쿼리가 키워드 조건 카드를 사용 하는 경우, 플라이 아웃 페이지는 저장 된 쿼리에 사용 되는 첫 번째 키워드 조건 카드의 용어로 미리 채워집니다.

그런 다음 보고 대상으로 최대 3 개의 피벗을 선택 하 고 **생성**을 클릭 하 여 검색 용어 보고서 생성 작업을 시작 합니다.

### <a name="what-is-a-pivot"></a>피벗 이란?

피벗 보고서가 구성 되는 방식입니다. 다음 예를 살펴보겠습니다.

- 저장 된 쿼리는 10 개의 문서: 즉, doc1 ~ doc10을 검색 합니다.

- doc1, doc2, doc3, doc4, doc5, doc6 및 doc7는 "eDiscovery" 라는 용어를 포함 합니다.

- doc6, doc7, doc8, doc9 및 doc10에는 "조사" 라는 용어가 포함 되어 있습니다.

- doc1, doc3, doc5, doc7, doc9은 custodian A에서 시작 합니다.

- doc2, doc4, doc6, doc8, doc10은 custodian B입니다.

이 경우 custodians의 "eDiscovery" 및 "조사" 라는 용어에 대해 검색 용어 보고서를 생성 하 고 검색 용어 보고서는 다음과 같이 구성 됩니다.

- "eDiscovery"-custodian A: 4 문서

- "eDiscovery"-custodian B: 3 문서

- "조사"-custodian A: 2 개 문서

- "조사"-custodian B: 3 문서

## <a name="step-3-download-report"></a>3 단계: 보고서 다운로드

검색 용어 관리 콘솔에서 이전에 만든 검색 용어 보고서 작업의 상태를 추적할 수 있습니다. 작업이 완료 되 면 검색 용어 보고서에 대 한 행을 클릭 하 고 "다운로드"를 클릭 하면 검색 용어 보고서가 CSV 형식으로 다운로드 됩니다. (검색 용어, 피벗) 튜플에는 하나의 행이 있으며 각 행에는 다음 정보가 포함 됩니다.

- 검색 된 문서 수

- 문서 전체에서 검색 용어를 찾은 횟수는 몇 회 입니까?

- 검색 된 문서의 총 량은 얼마 입니까?

- 검색 된 패밀리가 몇 개입니까?

- 검색 용어가 없는 문서를 포함 하 여 해당 패밀리의 총 문서 수는 얼마나 됩니까?

- 위의 전체 볼륨은 무엇입니까?