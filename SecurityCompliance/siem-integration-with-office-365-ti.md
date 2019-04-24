---
title: siem과 Office 365 Advanced Threat Protection의 통합
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.audience: ITPro
ms.topic: overview
ms.service: O365-seccomp
localization_priority: None
search.appverid:
- MET150
- MOE150
ms.assetid: eb56b69b-3170-4086-82cf-ba40a530fa1b
ms.date: 03/11/2019
ms.collection:
- M365-security-compliance
description: office 365 활동 관리 API에서 조직의 siem server를 office 365 Advanced Threat Protection 및 관련 위협 이벤트와 통합 합니다.
ms.openlocfilehash: fa9dcda0556684b748068cbe5ee848ba443d7667
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32260686"
---
# <a name="siem-integration-with-office-365-advanced-threat-protection"></a>siem과 Office 365 Advanced Threat Protection의 통합

조직에서 siem (보안 인시던트 및 이벤트 관리) 서버를 사용 하는 경우 Office 365 Advanced Threat Protection을 siem 서버와 통합할 수 있습니다. siem 통합을 사용 하면 siem server reports에서 Office 365 고급 보호를 통해 검색 된 맬웨어 또는 피싱 같은 정보를 볼 수 있습니다. siem 통합을 설정 하려면 [Office 365 활동 관리 API](https://docs.microsoft.com/office/office-365-management-api/office-365-management-activity-api-reference)를 사용 합니다. 

office 365 활동 관리 API는 조직의 Office 365 및 Azure Active Directory 활동 로그에서 사용자, 관리자, 시스템 및 정책 작업과 이벤트에 대 한 정보를 검색 합니다. [office 365 advanced threat protection 스키마](https://docs.microsoft.com/office/office-365-management-api/office-365-management-activity-api-schema#office-365-advanced-threat-protection-and-threat-intelligence-schema) 는 advanced threat protection과 함께 작동 하므로 조직에 Office 365 Advanced Threat protection 계획 1 또는 계획 2 또는 Office 365 E5가 있는 경우에도이 API를 사용 하 여 siem 서버 통합에 사용할 수 있습니다. 

siem 서버 또는 기타 유사한 시스템에서 **감사의 일반적인** 작업을 폴링하여 검색 이벤트에 액세스 해야 합니다. 자세한 내용은 [Office 365 관리 api 시작](https://docs.microsoft.com/office/office-365-management-api/get-started-with-office-365-management-apis)을 참조 하세요. 또한 다음 **AuditLogRecordType** 값은 Office 365 ATP 이벤트와 관련이 있습니다.

### <a name="enum-auditlogrecordtype---type-edmint32"></a>Enum: AuditLogRecordType: Edm. i a i. Int32

#### <a name="auditlogrecordtype"></a>AuditLogRecordType

|값|멤버 이름|설명|
|:-----|:-----|:-----|
|28@@|ThreatIntelligence|Exchange Online Protection 및 Office 365 Advanced Threat protection의 피싱 및 맬웨어 이벤트|
|41|ThreatIntelligenceUrl|ATP Safe 링크는 Office 365 Advanced Threat Protection에서 차단 및 차단 이벤트 차단을 방지 하 고 무시 합니다.|
|47|ThreatIntelligenceAtpContent|SharePoint Online, 비즈니스용 OneDrive 및 Office 365 Advanced Threat Protection의 파일에 대 한 피싱 및 맬웨어 이벤트입니다.|

> [!IMPORTANT]
> office 365 Advanced Threat Protection과 함께 siem 통합을 설정 하려면 office 365 전역 관리자 이거나 보안 & 준수 센터에 대해 보안 관리자 역할이 할당 되어 있어야 합니다.<br/>Office 365 환경에 대해 감사 로깅을 켜야 합니다. 이에 대 한 도움말을 보려면 [Turn Office 365 감사 로그 검색 설정 또는 해제](turn-audit-log-search-on-or-off.md)를 참조 하세요.

## <a name="related-topics"></a>관련 항목

[Office 365 위협 조사 및 응답](office-365-ti.md)

[Office 365 Advanced Threat Protection](office-365-atp.md)

[Office 365 보안 &amp; 및 준수 센터의 Smart reports 및 정보](reports-and-insights-in-security-and-compliance.md)
  
[Permissions in the Office 365 Security &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md)
  
