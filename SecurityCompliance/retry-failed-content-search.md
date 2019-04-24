---
title: 콘텐츠 검색을 다시 시도 하 여 콘텐츠 위치 오류 해결
ms.author: markjjo
author: markjjo
manager: laurawi
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: ''
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: 다시 시도 단추를 사용 하 여 콘텐츠 위치 오류가 있는 콘텐츠 검색 문제를 해결 합니다.
ms.openlocfilehash: 8334ec053e86e48f99955af2d56e511a2df5c25a
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32261504"
---
# <a name="retry-a-content-search-to-resolve-a-content-location-error"></a>콘텐츠 검색을 다시 시도 하 여 콘텐츠 위치 오류 해결

보안 및 준수 센터에서 콘텐츠 검색을 사용 하 여 많은 수의 사서함을 검색 하는 경우 (예: 단일 콘텐츠 검색에서 10만 사서함을 검색 하는 경우) 다음과 비슷한 검색 오류를 가져올 수 있습니다.

```
Error

The search on the following locations failed:

User1@contoso.com: Problem in processing the request. Please try again later. If you keep getting this error, contact your admin. (CS008-009)

User2@contoso.com: Application error occurred. Please try again later. (CS012-002)
```

이러한 오류 (CS008와 CS012-009의 오류 코드 포함)는 콘텐츠 검색에서 특정 콘텐츠 위치를 검색 하지 못했음을 나타냅니다. 이 예에서는 두 사서함이 검색 되지 않습니다. 이러한 오류는 콘텐츠 검색의 상태 세부 정보 플라이 아웃 페이지에 표시 됩니다.

## <a name="cause-of-content-location-errors"></a>콘텐츠 위치 오류 원인

많은 수의 사서함을 검색할 때 검색은 Microsoft 데이터 센터의 수많은 서버에 분산 됩니다. 특정 서버는 언제 든 지 다시 부팅 상태가 되거나 중복 복사본에 장애 조치 (failover) 될 수 있습니다. 이러한 경우에는 콘텐츠 검색 요청이 데이터를 검색 하는 데 시간이 초과 됩니다. 이전 예제에서 실패 한 사서함에 대 한 오류는 검색 시간 초과로 인해 발생 했습니다.

## <a name="resolving-content-location-errors"></a>콘텐츠 위치 오류 해결

검색을 다시 시작 하면 여러 서버에서 유사한 오류가 발생 하는 경우가 많습니다. 검색을 다시 시작 하는 대신 검색 결과 페이지 위쪽에 표시 되는 **다시 시도** 단추를 클릭 합니다.

![다시 시도 단추를 클릭 하 여 콘텐츠 위치 오류 해결](media/retrycontentsearch3.png)

이렇게 하면 오류가 발생 한 사서함에 대해서만 검색이 다시 시도 됩니다. 검색을 다시 시도 하면 성공적으로 반환 된 다른 결과가 보존 됩니다.

## <a name="tips-to-avoid-content-location-errors"></a>콘텐츠 위치 오류를 방지 하기 위한 팁

다음은 콘텐츠 위치 오류의 몇 가지 추가 원인과 많은 수의 사서함을 검색할 때 방지 하는 데 도움이 되는 몇 가지 팁입니다.

- 사용자 작업으로 인해 검색 중인 사서함이 사용 중일 수 있습니다. 이 경우 검색 서비스는 사서함을 사용할 수 없게 되는 것을 방지할 수 있습니다. 이를 방지 하려면 업무 외 시간에 검색을 실행 해 봅니다.

- 검색 쿼리가 사서함에서 너무 많은 콘텐츠를 검색 하 고 있을 수 있습니다. 가능한 경우 키워드, 날짜 범위 및 검색 조건을 사용 하 여 검색 범위를 좁힙니다.

- [키워드 목록을](view-keyword-statistics-for-content-search.md#get-keyword-statistics-for-content-searches)사용 하 여 검색 쿼리를 만들 때 키워드나 키워드 구문이 너무 많습니다. 키워드 목록을 사용 하는 검색 쿼리를 실행 하면 기본적으로 키워드 목록에 있는 각 행에 대해 별도의 검색을 실행 하 여 통계가 생성 될 수 있도록 합니다. 검색 쿼리에서 키워드 목록을 사용 하는 경우에는 키워드 목록에서 행 수를 최소화 하거나, 숫자 키워드를 작은 목록으로 나누고, 각 키워드 목록에 대해 다른 검색을 만듭니다.

  > [!NOTE]
  > 큰 키워드 목록으로 인해 발생 하는 문제를 줄이기 위해 이제는 검색 쿼리의 키워드 목록에서 최대 20 개의 행으로 제한 됩니다.

- 동시에 같은 사서함에서 너무 많은 검색을 수행 하 고 있습니다. 가능한 경우 한 사서함에서 한 번에 하나씩 검색을 실행 해 봅니다.

- 단일 검색에서 너무 많은 사서함을 검색 하는 경우 매우 많은 수의 사서함을 검색할 때 콘텐츠 위치 오류의 발생 가능성이 증가 합니다. 가능한 경우 각 검색에 조직에 있는 사서함의 하위 집합이 포함 되도록 여러 검색을 실행 해 봅니다.

- 사서함에서 필요한 유지 관리 작업을 수행 하 고 있습니다. 이 문제가 가끔 발생 하는 것은 아니지만 콘텐츠 위치 오류를 받은 후에 잠시 기다린 후에 검색을 다시 시도 하세요.
