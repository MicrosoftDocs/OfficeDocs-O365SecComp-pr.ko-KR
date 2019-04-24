---
title: Advanced eDiscovery (미리 보기)에 대 한 릴리스 정보
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
description: 이 문서에서는 Advanced eDiscovery (미리 보기)에 대 한 릴리스 정보를 포함 합니다.
ms.openlocfilehash: 32a02c16fd30e740fcc6e1c99b46775b97590a28
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32240943"
---
# <a name="release-notes-for-advanced-ediscovery-preview"></a>Advanced eDiscovery (미리 보기)에 대 한 릴리스 정보

고급 eDiscovery에 대 한 공용 미리 보기 프로그램은 예정 된 기능과 업데이트에 빠르게 액세스할 수 있는 방법입니다. 최신 기능에 빨리 액세스 하려면 Office 365 Security & 준수 센터에서 고급 eDiscovery (미리 보기) 사례를 만들고 사용 합니다. [새 사례 만들기를](create-new-ediscovery-case.md)참조 하세요.

## <a name="known-issues"></a>알려진 문제

**Microsoft Forms**

- custodian 사서함을 검색 하기 위해 고급 eDiscovery (미리 보기)에서 검색 도구를 사용 하 여 1 월 31 일 이전에 만든 폼에 해당 하는 데이터를 검색할 수는 없습니다. 이 날짜 이후에 만든 양식은 검색에 사용할 수 있습니다.

- 사용자가 만든 양식은 양식을 만든 사용자가 삭제 된 후에도 응답을 계속 받을 수 있습니다. 그러나 고급 eDiscovery (미리 보기)에서 검색 도구를 사용 하 여 custodian 사서함을 검색 하는 경우 custodian 사서함이 삭제 된 후에 발생 한 해당 응답에 대 한 해당 데이터를 검색할 수 없습니다.
 
**Microsoft Sway**

- 사용자가 해당 sway 소유자의 사용자 계정을 삭제 하기 바로 전에 sway를 편집 하는 경우에는 Advanced eDiscovery (Preview)의 검색 도구를 사용 하 여 custodian 사서함을 검색할 때 이러한 변경 내용을 검색 하지 못할 수 있습니다. sway는 계정이 삭제 되었다는 신호를 받으면 즉시 sway에 대 한 변경 내용을 차단 합니다. 그러나이 신호가 수신 되기 전에는 sway를 편집할 수 있는 작은 기회가 있습니다.

## <a name="issues-fixed-in-this-release"></a>이번 릴리스에서 해결 된 문제

- DCR: 인덱싱되지 않은 항목 및 분리 된 항목에 대 한 예외 처리
- DCR: 보류 알림
- DCR: eDiscovery의 Custodians

## <a name="whats-new"></a>새로운 기능

- **보안 & 준수 센터** -Advanced eDiscovery (Preview)에서 새롭게 디자인 된 탐색은 새로운 모양과 느낌을 갖습니다. 고급 eDiscovery (미리 보기)를 사용 하 여 사례 워크플로를 더 많이 관리 합니다.

- **사례 관리** -새로운 사례 유형에 대 한 추가 지원이 있습니다. 최신 및 즐겨 찾는 사례를 선택 하 고 저장할 수도 있습니다. 새 대시보드를 사용 하는 경우 및 사례 간에 활동을 추적 하 고 모니터링 합니다.

- **Custodian management** -사례 내에서 사용자를 데이터 custodians로 추가 및 제거 합니다.

- **Exchange, OneDrive 및 팀 통합** -사용자의 현재 사서함, 비즈니스용 OneDrive 계정 및 Microsoft 팀 사이트를 사례에 자동으로 추가 합니다. 

- **Custodian communications** -조직을 대신 하 여 법적 보존 알림을 보내고 관리 합니다.

- **Custodian portal** -custodians의 새 포털을 사용 하 여 활성 보류 상태에 액세스할 수 있습니다.

- **딥 인덱싱** -요청 시 부분적으로 인덱싱된 항목을 다시 크롤링합니다.

- **오류** 해결 방법-처리 오류를 수정 하거나 다운로드 합니다. 여기에는 큰 파일 형식, 암호로 보호 된 파일 등에 대 한 재구성 지원이 포함 됩니다. 

- **향상 된 검색 기능** -custodians 및/또는 위치를 식별 하 여 검색을 만듭니다.

- **작업 집합** -문서 정적 집합을 관리, 추적 및 감사 합니다.

- **검토** – 작업 집합에 추가 된 문서를 검토 하려면 native, text 및 near 기본 보기를 사용 합니다.

- 문서를 검토할 때 텍스트 교정 **, 태그 지정 및 주석 달기** /태그 적용 및 주석 만들기
  
- **분석 기반 검토**-eDiscovery 분석을 활용 하 여 작업 집합 내에서 결과를 찾고, 검색 하 고, cull 합니다.

- **작업** -장기 실행 프로세스의 상태를 추적 합니다.

- **새 감사 작업** -고급 eDiscovery에 대 한 새 감사 활동을 추적 및 확인 합니다.
