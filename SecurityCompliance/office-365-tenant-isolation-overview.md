---
title: Office 365 테 넌 트 격리
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
description: Microsoft Office 365에 대 한 테 넌 트 격리를 적용 하는 방법을 간략하게 설명 합니다.
ms.openlocfilehash: fcf66ee65c2a4cfdf73ae0eac77f54bd555d059d
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22533561"
---
# <a name="tenant-isolation-in-office-365"></a>Office 365 테 넌 트 격리

클라우드 컴퓨팅 공유, 공통 인프라의 개념을 동시에 여러 다양 한 고객은, 규모의 경제 향하는의 주요 이점 중 하나입니다. 이 개념을 *다중 테 넌 트*라고 합니다. Microsoft은 클라우드 서비스에 대 한 다중 테 넌 트 아키텍처 엔터프라이즈 수준의 보안, 기밀성, 개인정보 보호, 무결성 및 가용성 표준을 지원 하는지 확인 하려면 계속 작동 합니다.

중요 한 투자 및 [신뢰할 수 있는 컴퓨팅](https://www.microsoft.com/en-us/twc/default.aspx) 및 [보안 개발 수명 주기](http://www.microsoft.com/security/sdl/default.aspx)에서 수집 된 환경에 따라, Microsoft 클라우드 서비스는 모든 잠재적으로 유해한 모든 테 넌 트 되었는지 가정 대상으로 설계 다른 테 넌 트 되 고, 보안 또는 다른 테 넌 트의 서비스에 영향을 주지 또는 다른 테 넌 트의 콘텐츠 액세스 (영문)에서 하나의 테 넌 트의 동작을 방지 하기 위해 보안 조치를 구현 했습니다.

다중 테 넌 트 환경에서 테 넌 트 격리를 유지 관리의 두 기본 목표는:
1.  테 넌 트; 별 고객 내용에도 유출 되지 않도록, 또는 무단으로 액세스 방지 및
2.  다른 테 넌 트에 대 한 서비스에 부정적인 영향을 하나의 테 넌 트의 동작을 방지

여러 양식은 보호 하는 고객을 그대로 유지 하는 Office 365 서비스 또는 응용 프로그램이 나 다른 테 넌 트 또는 포함 하 여 Office 365 시스템 자체에 정보에 무단으로 액세스 하지 못하도록 방지 하기 위해 Office 365 전체에서 구현 된:
- Office 365 서비스에 대 한 각 테 넌 트 내의 고객 콘텐츠의 논리적 격리 Azure Active Directory 권한 부여 및 역할 기반 액세스 제어를 통해 이루어집니다.
- SharePoint Online에서는 저장소 수준에서 데이터 격리 메커니즘을 제공 합니다.
- Microsoft 엄격한 물리적 보안, 배경 차단 및 다중 계층된 암호화 전략을 사용 하 여 기밀성 및 고객 콘텐츠의 무결성을 보호 합니다. 모든 Office 365 데이터 센터는 실제에 액세스 하는 가장 필요한 팜 인쇄와의 생체 인식 컨트롤이 있습니다. 또한 모든 미국 기반 Microsoft 직원 채용 과정의 일부로 표준 배경 검사를 완료 해야 합니다. Office 365에 대 한 관리 액세스에 사용 되는 컨트롤에 대 한 자세한 내용은 [Office 365 관리 액세스 제어](office-365-administrative-access-controls-overview.md)를 참조 하십시오.
- Office 365에서 BitLocker, 파일 당 암호화를 포함 하 여 전송 하 고 나머지 부분에서 고객 콘텐츠를 암호화 하는 서비스 측 기술을 사용 하 여 전송 계층 보안 (TLS) 및 인터넷 프로토콜 보안 (IPsec). Office 365의 암호화에 대 한 구체적인 정보에 대 한 [데이터 암호화 기술 Office 365에](office-365-encryption-in-the-microsoft-cloud-overview.md)을 참조 하십시오.

함께 위에 나열 된 보호 기능이 위협 보호 및 완화 방법 만으로는 물리적으로 격리 하 여 제공 하는 것에 해당 하는 강력한 논리 격리 컨트롤을 제공 합니다.

## <a name="related-links"></a>관련된 링크
- [Azure Active Directory에서 격리 및 액세스 제어](office-365-isolation-in-azure-active-directory.md)
- [Office Graph 및 Delve에서 테넌트 격리](office-365-isolation-in-graph-and-delve.md)
- [Office 365 검색에서 테넌트 격리](office-365-isolation-in-office-365-search.md)
- [Office 365 비디오에서 테넌트 격리](office-365-isolation-in-office-365-video.md)
- [리소스 제한 사항](office-365-resource-limits.md)
- [테넌트 경계 모니터링 및 테스트](office-365-monitoring-and-testing.md)
- [Office 365에서 격리 및 액세스 제어](office-365-isolation-in-office-365.md)