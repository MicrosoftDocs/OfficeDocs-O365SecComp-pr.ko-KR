---
title: Office 365 Yammer Enterprise 액세스 제어
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
description: '요약: 간략 한 설명 Yammer Enterprise 액세스 제어 하는 방법에 대 한 프로덕션 환경에서 합니다.'
ms.openlocfilehash: 3f51e63c16022353e743b57d8e977f2ea2e6a835
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22534019"
---
# <a name="yammer-enterprise-access-controls"></a>Yammer Enterprise 액세스 제어 

Yammer 프로덕션 환경에 대 한 물리적 / 논리적 액세스 사용자 (인프라 및 작업)의 매우 작은 집합으로 제한 됩니다. 다른 Office 365 엔지니어와 마찬가지로 Yammer 엔지니어에 액세스할 수 없는 순위 고객 데이터입니다. Lockbox, 비슷합니다 승인 기반 적시에 대 한 액세스 제어 시스템을 사용 하 여 액세스를 요청 해야 않으며 승인자의 제한 된 수 있습니다. 승인자가 요청을 확인 합니다 (예: 자신이 기반 필요, 비즈니스 사례, 시간 등으로 요청은 합법적인 여부)을 확인 하 고 다음을 승인 하거나 요청을 거부 합니다. 요청 승인 되 면 자동으로 만료 되는 정의 되 고 제한 된 시간에 대 한 JIT 액세스가 부여 됩니다. 

다른 Office 365 서비스와 마찬가지로 Yammer 프로덕션 환경에 대 한 모든 액세스 다단계 인증을 활용 합니다. 모든 액세스 하 고 명령 기록의 사용자에 게 특성을 사용 하 고 기록 되 고 Yammer 보안 팀에서 정기적으로 검토 있습니다.

Yammer 관리 및 관리 하는 방법에 대 한 자세한 내용은 [Yammer 관리자 도움말](https://support.office.com/article/yammer-–-admin-help-e1464355-1f97-49ac-b2aa-dd320b179dbe?ui=en-US&rs=en-US&ad=US)을 참조 하십시오.