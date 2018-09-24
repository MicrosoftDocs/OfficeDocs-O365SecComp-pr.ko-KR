---
title: Office 365 위협 인텔리전스 및 고급 위협 보호 SIEM 통합
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.audience: ITPro
ms.topic: overview
ms.service: o365-administration
localization_priority: None
search.appverid:
- MET150
- MOE150
ms.assetid: eb56b69b-3170-4086-82cf-ba40a530fa1b
description: Office 365 위협 인텔리전스 및 Office 365 활동 관리 API를 사용 하 여 고급 위협 보호 조직의 SIEM 서버를 통합 합니다.
ms.openlocfilehash: 057d8ac101b96f37846ac751645934279d45dc88
ms.sourcegitcommit: 17c7e18d7d00135b1af40cbea117c9a817a41117
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/24/2018
ms.locfileid: "24972260"
---
# <a name="siem-integration-with-office-365-threat-intelligence-and-advanced-threat-protection"></a>Office 365 위협 인텔리전스 및 고급 위협 보호 SIEM 통합

조직 보안 사고 및 이벤트 (SIEM) 관리 서버를 사용 하는 경우 SIEM 서버와 Office 365 위협 인텔리전스 및 고급 위협 보호를 통합할 수 있습니다. SIEM 통합을 사용 하면 맬웨어 SIEM 서버 보고서에서 Office 365 고급 보호 및 위협 인텔리전스 하 여 검색 등의 정보를 볼 수 있습니다. SIEM 통합을 설정 하려면 [Office 365 활동 관리 API](https://docs.microsoft.com/office/office-365-management-api/office-365-management-activity-api-reference)를 사용 합니다. 

Office 365 활동 관리 API는 조직의 Office 365와 Azure Active Directory 활동 로그에서 사용자, 관리, 시스템 및 정책 작업 및 이벤트에 대 한 정보를 검색합니다. [Office 365 고급 위협 보호 및 위협 인텔리전스 스키마](https://docs.microsoft.com/office/office-365-management-api/office-365-management-activity-api-schema#office-365-advanced-threat-protection-and-threat-intelligence-schema) 함께 작동 위협 인텔리전스 및/또는 고급 위협 보호 되므로 조직에 고급 위협 보호 하지 위협 인텔리전스 하지만 (또는 그 반대의 경우도 마찬가지)을 하는 경우 다음을 수행할 수 있습니다. 여전히 해당 동일한 API를 사용 하 여 SIEM 서버 통합용 합니다. 

SIEM 서버 또는 기타 유사한 시스템 액세스 감지 이벤트 **audit.general** 작업 부하를 폴링해야 합니다. 자세한 내용은 [Office 365 관리 Api 시작](https://docs.microsoft.com/office/office-365-management-api/get-started-with-office-365-management-apis)합니다. 

> [!IMPORTANT]
> Office 365 전역 관리자 또는 보안 관리자 역할이 Office 365 위협 인텔리전스 및 고급 위협 보호 SIEM 통합을 설정 하는 보안 및 규정 준수 센터에 할당 해야 합니다.<br/>감사 로깅 Office 365 환경에 대 한 설정 해야 합니다. 를 대체 되는 도움말을 보려면 [Office 365 설정 또는 해제 로그 검색 감사](turn-audit-log-search-on-or-off.md)를 참조 합니다.

## <a name="related-topics"></a>관련 항목

[Office 365 위협 인텔리전스](office-365-ti.md)

[Office 365 Advanced Threat Protection](office-365-atp.md)

[보고서 및 Office 365 보안에 대 한 의견을 스마트 &amp; 준수 센터](reports-and-insights-in-security-and-compliance.md)
  
[Office 365 보안에 대 한 사용 권한을 &amp; 준수 센터](permissions-in-the-security-and-compliance-center.md)
  

