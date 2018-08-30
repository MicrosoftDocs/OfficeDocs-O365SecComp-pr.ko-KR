---
title: Office 365 엔지니어링을 위한 office 365 내부 로깅
ms.author: robmazz
author: robmazz
manager: laurawi
ms.date: 8/18/2018
audience: ITPro
ms.topic: article
ms.service: Office 365 Administration
localization_priority: None
search.appverid:
- MET150
ms.collection: Strat_O365_Enterprise
description: Office 365 엔지니어링에 대 한 내부 어떻게 로깅에 대 한 설명을 팀 작동 합니다.
ms.openlocfilehash: 1a613584b6b815524435acb20db7a8022d95e3bc
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22533206"
---
# <a name="internal-logging-for-office-365-engineering"></a>Office 365 엔지니어링에 대한 내부 로깅
이벤트와 고객을 위해 사용할 수 있는 로그 데이터 외에도 Office 365 엔지니어에 게 사용할 수 있는 내부 로그 데이터 수집 시스템도 됩니다. 다양 한 유형의 로그 데이터는 컴퓨팅 Cosmos 라는 서비스 지정 하 고 내부 큰 데이터를 Office 365 서버에서 업로드 됩니다. 각 서비스 팀 집계 및 분석을 위해 Cosmos 데이터베이스에는 해당 서버에서 감사 로그를 업로드합니다. 이 데이터 전송에 구체적으로 승인 된 포트 및 프로토콜 Office 데이터 로더 (ODL) 라는 독점 자동화 도구를 사용 하 여 FIPS 140-2-유효성을 검사 TLS 연결을 통해 발생 합니다.

서비스 팀에 중앙화 된 리포지토리로 Cosmos를 사용 하 여 응용 프로그램 사용, 시스템 및 운영 성능 측정 하 고 비정상적인 및 문제 또는 보안 문제를 나타낼 수 있는 패턴을 찾고 대 한 분석을 수행 합니다. 각 서비스 팀에 Cosmos, 분석를 검색 하는 기능에 따라 포함 된 로그 종종의 기준선을 업로드 합니다.
- 이벤트 로그
- AppLocker 로그
- 성능 데이터
- System Center 데이터
- 통화 정보 기록
- 체감 품질 데이터
- IIS 웹 서버 로그
- SQL Server 로그
- Syslog 데이터
- 보안 감사 로그

Cosmos에 데이터를 업로드 하기 전에 ODL 응용 프로그램 스크러빙 서비스를 사용 하 여 테 넌 트 정보 및 최종 사용자 식별 정보 등의 고객 데이터를 포함 하는 모든 필드를 난독 처리 및 이러한 필드는 해시 값을 바꿉니다. Anonymized 및 해시 된 로그 다시 작성 되며 다음 Cosmos로 업로드 됩니다. 팀이 서비스는 상관, 경고 및 보고에 대 한 Cosmos에서 자신의 데이터에 대해 범위가 지정 된 쿼리를 실행 합니다. Cosmos에서 감사 로그 데이터 보존 기간 서비스 팀;에 의해 결정 됩니다. 보안 문제 조사를 지원 하 고 규정 보존 요구를 충족 하기 위해 대부분의 감사 로그 데이터는 90 일 동안 또는 그 이상 유지 됩니다.

Cosmos에 저장 된 데이터를 Office 365에 대 한 액세스 권한이 부여 된 직원에 게 제한 됩니다. Microsoft 감사 기능을 담당 하는 서비스 팀 구성원의 제한 된 하위 집합을 관리 감사 기능을 제한 합니다. 이러한 팀 구성원을 수정 하거나 Cosmos에서 데이터를 삭제 하는 기능을 사용 하지 않은 및 Cosmos에 대 한 로깅 메커니즘에 모든 변경 내용을 기록 되 고 감사를 수행 합니다.

특정 분석을 수행 하려면 특정 응용 프로그램의 권한을 부여 하 여 분석을 위해 해당 로그 데이터를 액세스 하는 각 서비스 팀입니다. 등 Office 365 보안 팀은 독점적인 이벤트 로그 파서를 통해 Cosmos에서 데이터를 사용 하 여 관계를 지정, 경고, 및 Office 365 프로덕션 환경에서 가능한 의심 스러운 활동에 대 한 조치 가능한 보고서를 생성 합니다. 이 데이터에서 보고서, 보안 문제를 해결 하 고 서비스의 전반적인 성능이 개선 하기 위해 사용 됩니다. 특정 알림 또는 보고서를 조사 해야 추가 하는 경우 서비스 담당자는 Office 365 서비스에 다시 데이터를 가져올 수를 요청할 수 있습니다. 특정 로그 이후 Cosmos에서 가져올에 암호화 및 서비스 직원 암호 해독 키에 액세스할 수 없는, 대상 로그 권한이 부여 된 서비스 직원에 게 범위가 지정 된 결과 반환 하는 암호 해독 서비스를 통해 프로그래밍 방식으로 전달 됩니다. 이 연습에서 발견 된 모든 취약점 보고 되 고 Microsoft의 표준 보안 사고 관리 채널을 사용 하 여 에스컬레이션 합니다.
