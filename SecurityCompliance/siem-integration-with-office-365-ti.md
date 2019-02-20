---
title: Office 365 위협 인텔리전스 및 Advanced Threat Protection과의 siem 통합
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
description: office 365 활동 관리 API를 사용 하 여 조직의 siem 서버를 office 365 위협 인텔리전스 및 Advanced Threat Protection과 통합 합니다.
ms.openlocfilehash: 854f763b72dfac1a5dc1442b1d9d123ed5439257
ms.sourcegitcommit: 8679937354c1d8870ecd41519a59d2d7468c23c4
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/19/2019
ms.locfileid: "30087247"
---
# <a name="siem-integration-with-office-365-threat-intelligence-and-advanced-threat-protection"></a>Office 365 위협 인텔리전스 및 Advanced Threat Protection과의 siem 통합

조직에서 siem (보안 인시던트 및 이벤트 관리) 서버를 사용 하는 경우 Office 365 위협 인텔리전스 및 Advanced Threat Protection을 siem 서버와 통합할 수 있습니다. siem 통합을 사용 하면 siem server reports에서 Office 365 Advanced Protection 및 위협 인텔리전스를 통해 검색 된 맬웨어 같은 정보를 볼 수 있습니다. siem 통합을 설정 하려면 [Office 365 활동 관리 API](https://docs.microsoft.com/office/office-365-management-api/office-365-management-activity-api-reference)를 사용 합니다. 

office 365 활동 관리 API는 조직의 Office 365 및 Azure Active Directory 활동 로그에서 사용자, 관리자, 시스템 및 정책 작업과 이벤트에 대 한 정보를 검색 합니다. [Office 365 advanced threat protection 및 위협 인텔리전스 스키마](https://docs.microsoft.com/office/office-365-management-api/office-365-management-activity-api-schema#office-365-advanced-threat-protection-and-threat-intelligence-schema) 는 위협 인텔리전스 및/또는 advanced threat protection에서 작동 하므로 조직에서 Advanced threat protection을 사용 하는 경우에는 위협 인텔리전스 또는 그 반대의 경우도 가능 합니다. siem 서버 통합에도 동일한 API를 사용 합니다. 

siem 서버 또는 기타 유사한 시스템에서 **감사의 일반적인** 작업을 폴링하여 검색 이벤트에 액세스 해야 합니다. 자세한 내용은 [Office 365 관리 api 시작](https://docs.microsoft.com/office/office-365-management-api/get-started-with-office-365-management-apis)을 참조 하세요. 

> [!IMPORTANT]
> office 365 Advanced Threat Protection과 함께 siem 통합을 설정 하려면 office 365 전역 관리자 이거나 보안 & 준수 센터에 대해 보안 관리자 역할이 할당 되어 있어야 합니다.<br/>Office 365 환경에 대해 감사 로깅을 켜야 합니다. 이에 대 한 도움말을 보려면 [Turn Office 365 감사 로그 검색 설정 또는 해제](turn-audit-log-search-on-or-off.md)를 참조 하세요.

## <a name="related-topics"></a>관련 항목

[Office 365 위협 인텔리전스](office-365-ti.md)

[Office 365 Advanced Threat Protection 방지](office-365-atp.md)

[Office 365 보안 &amp; 및 준수 센터의 Smart reports 및 정보](reports-and-insights-in-security-and-compliance.md)
  
[Office 365 보안 &amp; 및 준수 센터의 사용 권한](permissions-in-the-security-and-compliance-center.md)
  

