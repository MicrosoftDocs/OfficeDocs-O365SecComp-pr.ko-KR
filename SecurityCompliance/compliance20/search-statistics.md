---
title: 검색 통계
ms.author: markjjo
author: esclee
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
ms.openlocfilehash: c5b7caff3550d42d84408d6b4e966655b8341123
ms.sourcegitcommit: ee28ee2b2bdfd049333c2f495d7f7780d13af4a6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2019
ms.locfileid: "29608158"
---
# <a name="search-statistics"></a>검색 통계
검색 결과 유효성을 검사 하는 한 가지 방법은 한 기대 눈금에 맞춰집니다 있는지 확인 하도록 결과 주위 통계를 확인 하는 것입니다. 검색 완료 되 면 높은 수준의 통계 검색 세부 정보 플라이 아웃에 나와 있습니다.
- 번호 및 검색에서 검색 되는 항목의 볼륨
- 번호와 볼륨의 부분적으로 인덱싱된/인덱싱되지 않은 검색 위치에서 발견 된 항목
- 수의 사서함과 위치를 검색 합니다. 자세한 통계를 보려면 검색 세부 정보 플라이 아웃에서 "통계"에서 클릭 합니다.

## <a name="summary"></a>요약
요약 보기의 위치 (예: Exchange) 형식으로 분류 된 검색 결과 볼 수 있습니다. 각 위치 유형에 대 한 다음을 확인할 수 있습니다.
- 검색 조건에 일치 하는 항목을 했던 위치 개수
- 검색 조건에 일치 하는 이러한 위치에서 항목 수
- 검색 조건과 일치 하는 항목의 총 볼륨입니다.

## <a name="top-locations"></a>위쪽 위치
위쪽 위치 보기의 개별 위치에서 가장 일치 하는 결과를 볼 수 있습니다. 각 위치에 대해 다음을 확인할 수 있습니다.
- 위치 이름 (예: SharePoint URL)
- 위치 종류
- 검색 조건에 일치 하는 항목 수
- 검색 조건과 일치 하는 항목의 총 볼륨입니다.

## <a name="queries"></a>쿼리
쿼리에서 (c:s) 키워드 또는 키워드 행을 사용 하는 경우 위치 유형 마다 쿼리 보기에서 쿼리를 분석을 볼 수 있습니다. 각 위치 유형에 대 한 표시 됩니다.
- 부: 단어 "기본" 또는 "키워드"이이 열에 지정할 하거나 됩니다. "기본"을 의미 하는 행 전체 쿼리 통계를 제공 "키워드" 쿼리 구성 요소 중 하나를 의미 하는 반면 합니다.
- 쿼리:는 실제 쿼리 구성 요소는 행을 참조 합니다. "기본" 부분을 사용 하는 경우이 속성은 전체 쿼리에 존재 합니다. 파트 "키워드" 했으므로, 다음 쿼리 구성 요소 중 하나 나타납니다.
  - 실제 쿼리는 (모든 키워드를 지정 하지 않으면) 하 여 모든 contentin 사서함을 검색 하는 경우 (크기 gt_ = 0) 항목을 모두 반환 되도록
  - 비즈니스 사이트에 대 한 SharePoint Online 및 OneDrive를 검색 하는 경우에 다음 구성 요소 2가 추가 됩니다.
    - 하지 IsExternalContent:1-온-프레미스 SharePoint 조직에서 모든 콘텐츠를 제외 합니다.
    - 하지 isOneNotePage: 1-있기 때문에 이러한 중복 항목을 검색 쿼리와 일치 하는 모든 문서의 모든 OneNote 파일을 제외 합니다.
- 검색 조건에 일치 하는 항목을 했던 위치 개수
- 검색 조건에 일치 하는 이러한 위치에서 항목 수
- 검색 조건과 일치 하는 항목의 총 볼륨입니다.

## <a name="refiners"></a>구체화
Exchange 사서함에 대 한 구체화 보기에서는 ItemClass, 보낸사람 및 받는 사람으로 추가 붕괴로. 각 위치 및 구체화 값에 대 한 검색에서 반환 된 문서 수를 확인할 수 있습니다.