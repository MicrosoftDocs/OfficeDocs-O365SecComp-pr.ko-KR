---
title: Office 365 검색에서 office 365 테 넌 트 격리
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
description: '요약: Office 365 검색에서 테 넌 트 격리의 설명 합니다.'
ms.openlocfilehash: cc73f3c157ffd20b3891a6b7c58e7d0b2adf4e55
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22532896"
---
# <a name="tenant-isolation-in-office-365-search"></a>Office 365 검색에서 테넌트 격리
SharePoint Online 검색은 테 넌 트 간에 누수 되는 정보에 대 한 보호를 사용 하 여 공유 데이터 구조의 효율성을 균형 있게 조정 하는 테 넌 트 분리 모델을 사용 합니다. 이 모델을 사용 하는 검색 기능에서 설정을 변경할는 합니다.
- 다른 테 넌 트에서 문서를 포함 하는 쿼리 결과 반환 합니다.
- 숙련 된 사용자가 다른 테 넌 트에 대 한 정보를 유추 수 쿼리 결과에 충분 한 정보 표시 (영문)
- 다른 테 넌 트에서 스키마 또는 설정 표시
- 혼합 분석 테 넌 트 또는 잘못 된 테 넌 트에 저장소 결과 사이 정보를 처리 하는 기능
- 다른 테 넌 트에서 사전 항목을 사용 하 여

각 유형의 테 넌 트 데이터에 대 한 사용 보호의 하나 이상의 레이어에 코드에서 정보의 실수로 누출 방지 하기 위해 합니다. 가장 중요 한 데이터에는 대부분 보호 계층을 단일 결함 실제 또는 체감 정보 유출 발생 하지는 있는지 확인 합니다.

## <a name="tenant-separation-for-the-search-index"></a>검색 인덱스에 대 한 테 넌 트 분리
검색 인덱스는 인덱스 구성 요소를 호스팅하는 서버에서 디스크에 저장 하 고는 테 넌 트에 있는 인덱스 파일을 공유 합니다. 테 넌 트의 인덱싱된 문서 해당 테 넌 트에 대 한 쿼리가 대해서만 표시 됩니다. 세 독립적인 메커니즘 정보 누출 방지:
- 테 넌 트 ID 필터링
- 테 넌 트 ID 용어 앞에 추가
- ACL 검사

모든 세 메커니즘은 잘못 된 테 넌 트에 문서를 반환 하는 검색에 대 한 실패 해야 합니다.

## <a name="tenant-id-filtering-and-tenant-id-term-prefixing"></a>테 넌 트 ID 필터링 및 테 넌 트 ID 용어 앞에 추가
검색 접두사 테 넌 트 ID 사용 하 여 전체 텍스트 인덱스에서 인덱싱되는 모든 용어 예, "*foo*" 이라는 용어는 ID가 "*123*" 인 테 넌 트에 대 한 인덱스 되 면 때 전체 텍스트 인덱스의 항목은 "*123foo.*"

모든 쿼리는 테 넌 트 ID 필터링 이라는 프로세스를 사용 하 여 테 넌 트 ID를 포함 하도록 변환 됩니다. "<*Guid*>"*foo*"쿼리를 변환 하는 예. *foo* 및 *테*: <*guid*> ", 여기서 <*guid*> 쿼리를 수행 하는 테 넌 트를 나타냅니다. 이 쿼리 변환 각 인덱스 노드 내에서 발생 하 고 쿼리도 아니고 콘텐츠 처리를 미칠 수 있습니다. 모든 쿼리에 테 넌 트 ID를 추가 하기 때문에 최고 일치 하는 하나의 테 넌 트에 순위를 검토 하 여 다른 테 넌 트의 용어 빈도 없으며 그렇게 유추 수는 없습니다.

테 넌 트 ID 용어 접두사로 전체 텍스트 인덱스에만 발생합니다. "*제목: foo*"와 같은 한 검색 용어 테 넌 트 id입니다. 없는 접두사로 가상 검색 인덱스를 이동 대신, 검색 한 필드 이름 붙습니다. 쿼리 "*제목: foo*" 변환할 등 "*fields.title:foo AND fields.tenantID*: <*guid*>." 용어 빈도 가상 검색 인덱스에서 방문 횟수의 순위에 영향을 주지 않습니다, 때문에 용어 앞에 추가 하 여 서로 분리 된 테 넌 트 않아도가 됩니다. "*제목: foo*"와 같은 fielded 검색용 테 넌 트 콘텐츠 분리 테 넌 트 ID 쿼리 변환에 의해 필터링에 따라 다릅니다.

## <a name="document-access-control-list-checks"></a>문서 액세스 제어 목록 확인
검색 인덱스에 저장 된 Acl 통해 문서에 액세스를 제어 하는 검색 합니다. 모든 항목은 특별 한 ACL 필드에서 용어 집합으로 인덱싱됩니다. ACL 필드 그룹 또는 문서를 볼 수 있는 사용자 당 하나의 용어를 포함 합니다. 모든 쿼리 인증 된 사용자가 속해 있는 각 그룹에 대 한 액세스 제어 항목 (ACE) 용어 목록이 포함 되어있습니다.

예: "<*guid*>와 같은 쿼리. *foo AND 테*: <*guid*> "즉시:" <*guid*>. *foo AND 테*: <*guid*> *AND* (*docACL:*<*ace1*> *OR docACL*: <*ace2*> *OR docACL*: <*ace3*> *... *)"

때문에 사용자 및 그룹 식별자 및 그래서 Ace는 고유, 추가 수준의 일부 사용자에 게 표시 되는 문서에 대 한 테 넌 트 사이 보안을 제공 합니다. 특별 한 "를 제외한 모든 외부 사용자에 게"에 대 한 경우에는 해당 동일한 테 넌 트의 일반 사용자에 대 한 액세스 권한을 부여 하는 ACE 합니다. 하지만 공용 문서에 대 한 테 넌 트 분리 테 넌 트 ID 필터링에 따라 달라 집니다는 이후 "모두"에 대 한 Ace는 모든 테 넌 트에 대해 동일 합니다. 거부 Ace도 지원 됩니다. 거부 ACE와 일치 하는 경우 결과에서 문서를 제거 하는 절을 추가 하는 쿼리 확대 합니다.

Exchange Online 검색 인덱스는 SharePoint Online에서 같이 테 넌 트 ID (구독 ID) 하는 대신 개별 사용자의 사서함에 대 한 사서함 ID에서 분할 됩니다. 파티션 메커니즘을 SharePoint Online와 동일 이지만 없는 ACL 필터링 합니다.
