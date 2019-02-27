---
title: 검색 통계
ms.author: markjjo
author: esclee
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
ms.openlocfilehash: a2234d0a0e94e3fbb15f8fac8f6e49cc7b26cfb2
ms.sourcegitcommit: baf23be44f1ed5abbf84f140b5ffa64fce605478
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/26/2019
ms.locfileid: "30295661"
---
# <a name="search-statistics"></a>검색 통계

검색 결과의 유효성을 검사할 수 있는 한 가지 방법은 결과를 기준으로 통계를 확인 하 여 예상과 일치 하는지 확인 하는 것입니다. 검색이 완료 되 면 검색 세부 정보 플라이 아웃에 높은 수준의 통계가 표시 됩니다.
- 검색을 통해 검색 되는 항목의 수 및 볼륨
- 검색 위치에서 찾은 부분 인덱싱된/인덱싱되지 않은 항목의 수 및 볼륨
- 검색 된 사서함 및 위치 수입니다. 자세한 통계를 보려면 검색 세부 정보 플라이 아웃에서 "통계"를 클릭 합니다.

## <a name="summary"></a>요약

요약 보기에서는 위치 유형 (예: Exchange)으로 분류 된 검색 결과를 볼 수 있습니다. 각 위치 유형에 대해 다음을 확인할 수 있습니다.
- 검색 조건과 일치 하는 항목이 있는 위치 수
- 이 위치에서 검색 조건과 일치 하는 항목의 수
- 검색 조건과 일치 하는 항목의 총 크기입니다.

## <a name="top-locations"></a>상위 위치

상위 위치 보기에는 가장 일치 하는 개별 위치가 표시 됩니다. 각 위치에 대해 다음이 표시 됩니다.
- 위치 이름 (예: SharePoint URL)
- 위치 종류
- 검색 조건과 일치 하는 항목 수
- 검색 조건과 일치 하는 항목의 총 크기입니다.

## <a name="queries"></a>쿼리하도록

쿼리에 사용 된 (c:s) 키워드나 키워드 행이 있는 경우 쿼리 결과를 위치 유형별 쿼리 보기로 볼 수 있습니다. 각 위치 유형에 대해 다음이 표시 됩니다.

- 파트:이 열에는 "Primary" 또는 "Keyword" 라는 단어가 포함 됩니다. "기본"은 행에 전체 쿼리에 대 한 통계가 표시 되는 반면 "Keyword"는 쿼리 구성 요소 중 하나를 의미 합니다.

- 쿼리: 행이 참조 하는 실제 쿼리 구성 요소입니다. Part가 "Primary" 이면 전체 쿼리가 됩니다. Part가 "Keyword" 이면 여기에 쿼리 구성 요소 중 하나가 표시 됩니다.
  
  - 모든 contentin 사서함을 검색 하는 경우 (키워드를 지정 하지 않음) 실제 쿼리는 (size > = 0)로, 모든 항목이 반환 됩니다.
  
  - SharePoint Online 및 비즈니스용 OneDrive 사이트를 검색 하면 다음과 같은 두 가지 구성 요소가 추가 됩니다.
    
    - NOT IsExternalContent: 1-온-프레미스 SharePoint 조직에서 모든 콘텐츠를 제외 합니다.
    
    - NOT isOneNotePage: 1-모든 OneNote 파일은 검색 쿼리와 일치 하는 모든 문서와 중복 되므로 제외 합니다.

- 검색 조건과 일치 하는 항목이 있는 위치 수입니다.

- 검색 조건과 일치 하는 이러한 위치에 있는 항목의 수입니다.

- 검색 조건과 일치 하는 항목의 총 크기입니다.