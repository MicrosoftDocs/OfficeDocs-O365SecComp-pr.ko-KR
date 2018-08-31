---
title: Office 365 격리 컨트롤
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
description: '요약: Office 365 내에서 격리 컨트롤의 설명 합니다.'
ms.openlocfilehash: 3a5c06d0675a4503d9f5e5edd58535688fb9180a
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22534158"
---
# <a name="office-365-isolation-controls"></a>Office 365 격리 컨트롤 

Microsoft은 Office 365의 다중 테 넌 트 아키텍처 엔터프라이즈 수준의 보안, 기밀성, 개인정보 보호, 무결성 및 가용성 [표준](https://www.microsoft.com/TrustCenter/Compliance?service=Office#Icons)으로 지역 및 국제 표준 사항을 지원 하도록 지속적으로 작동 합니다. 소수 자릿수 및 Microsoft에서 제공 하는 서비스의 범위를 지정 하는, 상태인 것 어렵고 중요 한 사용자 상호 작용 된 필요한 경우 Office 365를 관리 하려면 경제적인 합니다. Office 365 서비스는 여러 전체적으로 배포 된 데이터 센터를 매우 자동화 된 방식 이며, 여기서 매우 적은 데이터 센터 작업에는 휴먼 터치가 필요 하 고 더 적은 작업 필요 고객 콘텐츠에 대 한 액세스를 통해 제공 됩니다. 이러한 서비스 및 자동화 된 도구를 사용 하 여 데이터 센터를 지원 하 고 매우 원격 액세스를 보호 하는 직원 합니다. 방법에 대 한 자세한 내용은 중 일부에 대 한 대규모 서비스는 Office 365를 참조 [된 숨은 기능 IT 전문가 위한 Office 365를 살펴보는 숨김](https://channel9.msdn.com/Events/SharePoint-Conference/2014/SPC202)작동 합니다.

Office 365 중요 한 비즈니스 기능을 제공 하 고 전체 Office 365 환경에 참가 하는 여러 서비스 구성 됩니다. 이러한 각 서비스는 자동으로 포함 되어야 하 고 서로와 통합 되도록 설계 되었습니다. Office 365 [서비스 지향 아키텍처](https://msdn.microsoft.com/library/aa480021.aspx)를 디자인 하 고 잘 정의 된 비즈니스 기능 및 [운영 보안을 제공 하는 상호 운용할 수 있는 서비스의 형태로 소프트웨어 개발 (영문)으로 정의 하는 원칙에 따라 디자인 보증](http://www.microsoft.com/download/details.aspx?id=40872), 다양 한 Microsoft [보안 개발 수명 주기](https://www.microsoft.com/sdl/default.aspx), [Microsoft 보안 대응 센터](https://technet.microsoft.com/library/dn440717.aspx)및 자세히를 포함 하 여 Microsoft에 고유한 기능을 통해 얻은 정보를 통합 하는 프레임 워크 cybersecurity 위협 상황의 인식 합니다.

Office 365 서비스 서로 상호 운용 설계 하 고 배포 되 고 자치 서비스를 서로 독립적으로 작동할 수 있도록 구현 됩니다. Microsoft는 의무 및 Office 365 무단 또는 의도 하지 않은 수정에 대 한 기회를 줄일 수에 대 한 책임의 영역 또는 조직의 자산 오용 분리 합니다. Office 365 팀이 광범위 한 역할 기반 액세스 제어 메커니즘의 일부로 역할을 정의 합니다.

## <a name="customer-content-isolation"></a>콘텐츠 격리 고객
테 넌 트에 속한 모든 고객 콘텐츠 다른 테 넌 트 및 Office 365의 관리에 사용 되는 작업 및 시스템 데이터에서 격리 됩니다. 모든 Office 365 서비스 또는 응용 프로그램 또는 테 넌 트 또는 Office 365 시스템 자체의 정보에 무단으로 액세스 하지 못하도록 모든의 손상 위험을 최소화 하기 위해 Office 365 전체에서 여러 형태의 보호 구현 되었습니다. Microsoft Office 365 내에서 테 넌 트 데이터의 논리적 격리를 구현 하는 방법에 대 한 정보를 [Office 365에서 테 넌 트 격리](office-365-tenant-isolation-overview.md)를 참조 하십시오.
