---
title: 한 검토 집합의 데이터를 다른 검토 집합에 추가
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
ms.openlocfilehash: 9dc75717ac0a57c8ccb38b1e01ec2fcb9c5737ab
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/17/2019
ms.locfileid: "34151970"
---
# <a name="add-data-to-a-review-set-from-another-review-set"></a>다른 검토 집합의 검토 집합에 데이터 추가

어떤 경우에는 한 검토 집합에서 문서 일부를 carve 다른 검토 집합에서 개별적으로 사용 해야 할 수도 있습니다.  이 기능은 검토 집합에 콘텐츠를 culled 데이터 하위 집합에 대 한 분석을 실행 하려는 경우 특히 유용 합니다.

이 문서에서 설명 하는 워크플로를 따라 검토 집합 간에 콘텐츠를 추가 합니다.

## <a name="before-you-begin"></a>시작하기 전에

시작 하기 전에 데이터를 추가할 새 검토 집합을 만들어야 합니다.  사례에 대 한 **검토 집합** 탭에 새 검토 집합을 추가할 수 있습니다. 자세한 내용은 [Create a review set](managing-review-sets.md#create-a-review-set)을 참조 하십시오.

## <a name="step-1-identify-content-to-add-to-another-review-set"></a>1 단계: 다른 검토 집합에 추가할 콘텐츠 식별

원본 검토 집합에서 특정 문서를 선택 하거나 b seleting 모든 항목을 검토 설정 쿼리로 지정 하 여 한 검토 집합의 콘텐츠를 다른 검토할 수 있습니다.  선택한 항목을 추가 하는 경우 항목을 선택 하 고 **동작**을 클릭 한 다음 **다른 검토 집합에 추가를**클릭 합니다.

![다른 검토 집합에 추가](../media/64f2a4d4-eba3-4ab3-a3ba-d519feea3142.png)

## <a name="step-2-specify-options-for-adding-to-another-review-set"></a>2 단계: 다른 검토 집합에 추가 하기 위한 옵션 지정

**다른 검토 설정 옵션** 의 플라이 아웃 추가 페이지에서 항목을 추가할 검토 집합을 선택 합니다. **모든 검색 결과** 또는 **선택한 항목**을 추가할지 여부를 선택 합니다.  추가 정보에서는 새 검토 집합에 문서를 추가할 때 항목의 모든 메타 데이터 및 원본 검토 집합에서 태그 ( **레이블** 확인란 선택)를 포함 하는 옵션을 제공 합니다.  

![다른 검토 집합에 추가](../media/6440ee44-68fd-44d7-b43a-3a477345525c.png)

**확인**을 클릭 하면 다른 검토 집합에 콘텐츠를 추가 하기 위해 새 작업 (즉, **다른 검토 집합에 데이터 추가**)이 만들어집니다.  **작업** 탭으로 이동 하 여이 작업의 진행 상태를 모니터링할 수 있습니다. 자세한 내용은 [작업 관리](managing-jobs-ediscovery20.md)를 참조 하세요.
