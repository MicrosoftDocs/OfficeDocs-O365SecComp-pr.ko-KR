---
title: Office 365 격리 컨트롤
ms.author: robmazz
author: robmazz
manager: laurawi
ms.date: 8/21/2018
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: None
search.appverid:
- MET150
ms.collection:
- Strat_O365_IP
- M365-security-compliance
description: '요약: Office 365 내의 격리 컨트롤에 대 한 설명입니다.'
ms.openlocfilehash: a6ff2b11ea02334a6c47317cbb77b8d47207b552
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30217318"
---
# <a name="office-365-isolation-controls"></a>Office 365 격리 컨트롤 

Microsoft는 Office 365의 다중 테 넌 트 아키텍처에서 엔터프라이즈 수준의 보안, 기밀성, 개인 정보, 무결성 및 가용성 [표준을](https://www.microsoft.com/TrustCenter/Compliance?service=Office#Icons)지원 하 고 지역 및 국제 표준을 지 원하는 방식으로 계속 작동 합니다. Microsoft에서 제공 하는 서비스의 확장 및 범위를 감안 하면 상당한 인간 상호 작용이 필요한 경우 Office 365을 관리 하기가 어렵고 경제적이 지 않습니다. Office 365 서비스는 여러 전역 분산 데이터 센터를 통해 자동으로 제공 되며, 대부분의 데이터 센터 작업에는 사용자의 터치가 필요 하며, 더 적은 작업은 고객 콘텐츠에 대 한 액세스 권한이 필요 합니다. 이러한 서비스와 데이터 센터는 자동화 된 도구 및 높은 보안 수준의 원격 액세스를 통해 지원 됩니다. 대규모 서비스가 office 365에서 운영 되는 방식에 대 한 자세한 내용은 [배후에서 IT 전문가를 위한 Office 365의 모습](https://channel9.msdn.com/Events/SharePoint-Conference/2014/SPC202)을 참조 하십시오.

office 365은 중요 한 비즈니스 기능을 제공 하 고 전체 Office 365 환경에 기여 하는 여러 서비스로 구성 됩니다. 이러한 각 서비스는 독립적 이며 서로 통합 되도록 설계 되었습니다. Office 365는 잘 정의 된 비즈니스 기능을 제공 하는 상호 운용 가능한 서비스 형태의 소프트웨어 디자인 및 개발으로 정의 되는 [서비스 지향 아키텍처](https://msdn.microsoft.com/library/aa480021.aspx)원칙을 사용 하 여 설계 되었으며 [운영 보안 ](http://www.microsoft.com/download/details.aspx?id=40872)microsoft [보안 개발 수명 주기](https://www.microsoft.com/sdl/default.aspx), [microsoft 보안 대응 센터](https://technet.microsoft.com/library/dn440717.aspx)및 깊이를 포함 하 여 microsoft에 고유 하 게 제공 되는 다양 한 기능을 통해 얻은 지식을 통합 하는 프레임 워크 (보증) cybersecurity 위협 가로 인식

Office 365 서비스는 서로 상호 운용이 가능 하지만, 서로 독립적으로 배포 및 운영 되는 자치 서비스로 배포할 수 있도록 설계 및 구현 됩니다. Microsoft segregates 의무 및 책임 영역으로, 무단으로 수정 되거나 조직의 자산의 오용에 대 한 영업 기회를 줄이기 위한 Office 365 Office 365 팀은 포괄적인 역할 기반 액세스 제어 메커니즘의 일부로 역할을 정의 합니다.

## <a name="customer-content-isolation"></a>고객 콘텐츠 격리
테 넌 트에 속한 모든 고객 콘텐츠는 다른 테 넌 트에서 격리 되며, Office 365 관리에서 사용 되는 운영 및 시스템 데이터와는 다릅니다. office 365 서비스 또는 응용 프로그램의 손상 위험을 최소화 하기 위해 또는 테 넌 트 또는 office 365 시스템 자체의 정보에 무단으로 액세스 하려는 경우 여러 가지 유형의 보호를 office 365에서 구현 했습니다. Microsoft가 office 365 내의 테 넌 트 데이터의 논리적 격리를 구현 하는 방법에 대 한 자세한 내용은 [office 365에서 테 넌 트 격리](office-365-tenant-isolation-overview.md)를 참조 하세요
