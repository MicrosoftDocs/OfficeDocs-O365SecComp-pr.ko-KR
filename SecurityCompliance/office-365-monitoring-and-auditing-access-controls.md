---
title: Office 365 모니터링 및 감사 액세스 제어
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
description: '요약: 다양 한 모니터링 및 감사 액세스 컨트롤의 Office 365에서 사용할 수 있는 요약 합니다.'
ms.openlocfilehash: 7ef25d62ce3c4fa320dd0b164183c6f67be7d76d
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22534018"
---
# <a name="monitoring-and-auditing-access-controls-in-office-365"></a>모니터링 및 감사 Office 365의에서 액세스 제어

Microsoft는 광범위 한 모니터링 및 모든 위임, 모든 권한, 사용 및 Office 365 내에서 발생 하는 모든 작업에 대해 감사를 수행 합니다. Office 365 액세스 제어는 최소한의 권한 및 데이터 액세스 제어 및 감사를 통합 하는 원칙을 기반으로 작성 된 자동화 된 프로세스:
- 허용 되는 모든 액세스를 관리자가 자신의 고객 콘텐츠 처리에 대 한 책임이 있는 요청을 고유 사용자에 게 추적할 수 있습니다.
- 액세스 제어 요청, 승인 및 관리 작업 로그의 보안 정보 및 악의적인 이벤트 분석을 위해 캡처됩니다.
- 액세스 수준은 실시간에 따라 보안 그룹 구성원만 사용자에 게 권한이 부여 된 비즈니스 근거 하 고 자격 요구 사항을 충족는 시스템에 액세스할 수 있는지 확인 하려면 근처에서 검토 해야 합니다.
- Office 365, 액세스 제어 및 지원 서비스, Azure Active Directory와 실제 데이터 센터를 포함 하 여을 정기적으로 [ISO/IEC 27001](https://www.microsoft.com/en-us/TrustCenter/Compliance/iso-iec-27001), [ISO/IEC 27018](https://www.microsoft.com/en-us/TrustCenter/Compliance/iso-iec-27018), [SOC](https://www.microsoft.com/en-us/TrustCenter/Compliance/SOC), 준수를 위한 독립 제 3 자가 감사 [FedRAMP](https://www.microsoft.com/en-us/TrustCenter/Compliance/FedRAMP)및 기타 [표준](https://www.microsoft.com/en-us/TrustCenter/Compliance?service=Office#Icons)입니다.
- Office 365 엔지니어는 상승 된 액세스에 대 한 유용한 정보를 검토 하는 위험 연간 보안 교육을 수행 하 고 Microsoft의 보안 및 개인정보 보호 정책을 유지 관리 하는 서비스에 해당 권리를 계속 하려면 승인 해야 합니다.

자동화 된 경고는 의심 스러운 활동이 감지 되 면 짧은 기간 내의 여러 실패 한 로그인 등 때 트리거됩니다. Office 365 보안 대응 팀을 사용 하 여 컴퓨터 학습 및 큰 데이터 분석 검토 하 고 불규칙적인 액세스 패턴에 대 한 작업을 분석 하 고 사전 비정상적인 및 불법 활동에 응답할 수 있습니다. 또한 Microsoft 통과 테스터의 전용된 팀에서 사용 하는 하 게 되 고 연습을 보안 찾기 및 액세스 제어 문제가 발생 한 서비스에서를 정기적으로 빨간색 팀과 파란색 팀에서 시작 합니다. 고객 감사 보고서 및 관리 활동 Office 365에서 제공 하는 API 사용 하 여 액세스 제어 시스템의 효과 확인할 수도 있습니다. 

자세한 내용은 [Office 365 관리 활동 API 참조](https://msdn.microsoft.com/en-us/library/office/mt227394.aspx) 및 [감사 및 Office 365의 보고 기능](office-365-auditing-and-reporting-overview.md)을 참조 하십시오.
