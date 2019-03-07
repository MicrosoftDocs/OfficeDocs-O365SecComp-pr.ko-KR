---
title: 작업 집합에서 데이터 쿼리
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
ms.openlocfilehash: 2523072181307cce510f0f318834329b2c70b376
ms.sourcegitcommit: 6aa82374eef09d2c1921f93bda3eabeeb28aadeb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/06/2019
ms.locfileid: "30454990"
---
# <a name="query-the-data-in-a-working-set"></a>작업 집합에서 데이터 쿼리

대부분의 경우이 기능은 작업 집합에 있는 항목을 보다 자세히 살펴보고 보다 효율적으로 검토할 수 있도록 구성 하는 데 도움이 됩니다. 작업 집합 내의 쿼리를 사용 하면 사용자가 한 번에 정의한 기준을 충족 하는 문서 하위 집합에 집중할 수 있으므로이를 수행할 수 있습니다.

## <a name="creating-and-running-a-query-within-a-working-set"></a>작업 집합 내에서 쿼리 만들기 및 실행

작업 집합 내에서 쿼리를 만들고 실행 하려면 작업 집합에서 "새 쿼리"를 클릭 합니다. 쿼리 이름을 지정 하 고 조건을 정의한 후에는 "저장"을 클릭 하 여 쿼리를 실행 합니다. 이전에 저장 한 쿼리를 실행 하려면 저장 된 쿼리를 클릭 하면 됩니다. 검색할 수 있는 메타 데이터 목록은 [문서 메타 데이터 필드](document-metadata-fields.md) 를 참조 하십시오.

## <a name="building-your-query"></a>쿼리 작성

키워드 조건 카드에 조건 카드와 쿼리 언어를 함께 사용 하 여 쿼리를 작성할 수 있습니다.

### <a name="condition-card"></a>조건 카드

작업 집합의 모든 검색 가능 필드에는 쿼리를 작성 하는 데 사용할 수 있는 해당 하는 조건 카드가 있습니다.

여러 유형의 조건 카드를 사용할 수 있습니다.
- freetext: freetext 조건 카드는 subject와 같은 텍스트 필드에 사용 됩니다. 여러 검색 용어를 쉼표로 구분 하 여 나열할 수 있습니다.
- 날짜: 날짜 조건 카드는 마지막으로 수정한 날짜와 같은 날짜 필드에 사용 됩니다.
- 검색 옵션: 검색 옵션 조건 카드에는 작업 집합의 특정 필드에 사용할 수 있는 값의 목록이 제공 됩니다. 이 속성은 작업 집합에 가능한 값의 수가 한정 된 보낸 사람 등의 필드에 사용 됩니다.
- 키워드: 키워드 조건 카드는 용어를 검색 하거나에서 KQL와 같은 쿼리 언어를 사용 하는 데 사용할 수 있는 freetext 조건 카드의 특정 인스턴스입니다. 자세한 내용은 아래를 참조 하세요.

### <a name="query-language"></a>쿼리 언어

조건 카드 외에도 키워드 카드에서 KQL 같은 쿼리 언어를 사용 하 여 쿼리를 작성할 수 있습니다. 쿼리 언어는 and, OR, NOT 및 NEAR (n)과 같은 표준 KQL 구문을 지원 합니다. 또한 단일 문자 와일드 카드 (?) 및 여러 문자 와일드 카드 (*)를 지원 합니다.