---
title: Office에서 office 365 테 넌 트 격리 그래프 및 굴
ms.author: robmazz
author: robmazz
manager: laurawi
ms.date: 8/21/2018
audience: ITPro
ms.topic: article
ms.service: Office 365 Administration
localization_priority: None
search.appverid:
- MET150
ms.collection: Strat_O365_Enterprise
description: '요약: 테 넌 트 격리 Delve 및 Office 그래프에는 설명 합니다.'
ms.openlocfilehash: bdc0f34d558f25ec139861c9a91261a72418f18a
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22533336"
---
# <a name="tenant-isolation-in-the-office-graph-and-delve"></a>Office Graph 및 Delve에서 테넌트 격리

## <a name="tenant-isolation-in-the-office-graph"></a>Office 그래프에서 테 넌 트 격리
Office 365 서비스를 비롯 하 여 Exchange Online, SharePoint Online, Yammer Skype 등에 대 한 비즈니스, Azure Active Directory, 및 기타 Microsoft 서비스 또는 타사 서비스 등의 외부 서비스에서 [Office 그래프](https://dev.office.com/officegraph) 모델 활동입니다. Office 그래프 구성 요소는 Office 365 전체에서 사용 됩니다. Office 그래프 콘텐츠 및 활동 및 전체 Office 제품군 전체에 걸쳐 발생 하는 이들 간의 관계의 컬렉션을 나타냅니다. 기술을 이해 하는 복잡 한 컴퓨터를 사용 하 여 관련 콘텐츠, 대화 및 사람들을 자기 주위에 사용자를 연결 합니다. 예, SharePoint Online에서 테 넌 트 인덱스에는 인덱스가 Office 그래프 Delve 쿼리를 처리 하는데 사용 되는, SharePoint Online에서 분석 처리 엔진 신호를 저장 하 고 의견을 계산 하는데 사용 됩니다 및 Exchange Online 계산 하는 각 사용자의 테 넌 트 분석에 대 한 입력으로 받는 사람 캐시 합니다.

Office 그래프에는 사용자 및 문서와 관계 및 이러한 개체 간의 상호작용 하는 등의 enterprise 개체에 대 한 정보가 들어 있습니다. 관계 및 상호작용 *가장자리*으로 표현 됩니다. 에 지에 동일한 테 넌 시의 *노드* 간에 있을 수 있도록 Office 그래프 테 넌 트 세그먼트화 됩니다. *노드* 는 엔터티를 식별자 URI (Uniform Resource), 노드 유형, 액세스 제어 목록 및 *메타 데이터* 및에 지에 포함 된 패싯 집합입니다. 메타 데이터 및 가장자리, 공통 된 기술 모델에서와 같이 *측면* 으로 정렬 하 여 각 노드에 연결 합니다. *메타 데이터* 검색, 필터링, 또는 office 그래프 내에서 분석에 사용할 수 있는 노드에 저장 된 속성 이름이 지정 됩니다. *과제* 는 메타 데이터 및 노드에서 가장자리의 논리적 컬렉션입니다. 각 과제는 노드의 한 측면을 설명 합니다. 

Office 그래프 단일 리포지토리로 모든 데이터를 가져오지 않습니다. 대신, 메타 데이터 및 곳에 있는 데이터에 대 한 관계 저장 합니다. 여러 데이터 저장소 및 처리 구성 요소는 Office 그래프 구성 됩니다.
- 테 넌 트 그래프 저장소 효율적인 분석에 최적화 된 대량 저장소를 제공 합니다.
- 현재 콘텐츠 캐시 활성 노드에 대 한 빠른 임의 액세스 및 가장자리 드라이브 사용자 경험을 제공합니다.
- 입력된 라우터 내부 및 외부 테 넌 트 그래프에 대 한 변경 하는 구성 요소를 알립니다.

각 작업 내에서 분석 테 넌 트 수준 계산에 관련 된 정보를 추론 하 고 테 넌 트 그래프에 푸시입니다. 테 넌 트 분석 하는 이유는 테 넌 시의 모든 작업을 통해 패턴 동작에 대 한 통찰력을 생성 합니다. 예, Exchange Online 효율적으로 각 사용자의 사서함을 통해 이유는 분석 된 각 사용자에 대 한 받는 사람 캐시를 계산 합니다. 이러한 사용자 당 분석 테 넌 트 그래프를 차례 대로 푸시됩니다 하는 각 사용자에 *RecipientCache 가장자리* 의 집합을 생성 합니다. 이렇게 하면 as 범위를 최대한 원본 데이터에 근접 분석 처리 합니다.

## <a name="tenant-isolation-in-delve"></a>테 넌 트 격리에서 굴
앞서 언급 했 듯이 Office 그래프를 검색 하 고는 엔터프라이즈에서 현재 작업에 공동 작업을 수행할 수 있도록 도와주는 경험 전원을 작업 간에 콘텐츠 및 작업을 통해 이유를 분석에 대 한 엔터티 중심 플랫폼을 제공 하 고 Office 365 이상. 굴에서 첫째 이러한 환경을 Office 그래프에서 전원을 공급 합니다. 굴 Office 그래프를 통해 Office 365 사용자에 게 Office 365와 Yammer Enterprise에서 콘텐츠 표면 하는 Office 365 웹 환경 됩니다. 웹 환경 *내 주위 인기* 또는 *내가 수정한 문서*와 같은 특정 항목을 각각 다른 게시판으로 데이터를 표시합니다. 각 보드 요약 텍스트와 문서에서 그림을 표시 하는 여러 문서 카드로 이루어져 있습니다. 카드는 문서를 열거나 문서에 대 한 Yammer 페이지와 동일 하 게 작업을 수행할 수 있도록 합니다. 이 사용자에 대 한 가장 관련이 있는 문서를 표시 하는 Office 365 테 넌 트 및 해당 대화 상대와 상호작용 하기 위한 Exchange Online 또는 비즈니스를 위한 Skype를 호출할 수 있는 아이콘의 각 사용자에 대 한 페이지 방법이 있습니다. Delve Office 그래프 API를 기반으로 하므로 해당 API의 테 넌 트 기반 분리 하 여 바인딩됩니다.