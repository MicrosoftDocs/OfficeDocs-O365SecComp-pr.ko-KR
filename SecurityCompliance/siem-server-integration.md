---
title: Microsoft 365과의 siem 서버 통합
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.audience: ITPro
ms.topic: article
ms.date: 10/29/2018
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- M365-security-compliance
ms.custom:
- Ent_Solutions
- SIEM
description: 요약:이 문서를 읽으면 Microsoft 365과의 siem server 통합에 대 한 개요를 확인할 수 있습니다.
ms.openlocfilehash: 905f6fc9b6fd62748e25c27d6e5cdbedacc0f806
ms.sourcegitcommit: 0f93b37c39d807dec91f118aa671a3430c47a9ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/20/2019
ms.locfileid: "30693647"
---
# <a name="siem-server-integration-with-microsoft-365-services-and-applications"></a>Microsoft 365 서비스 및 응용 프로그램과의 siem 서버 통합

## <a name="overview"></a>개요

조직에서 siem (보안 정보 및 이벤트 관리) 서버를 사용 하는 경우 또는 siem 서버를 곧 가져올 계획인 경우 Office 365 Enterprise를 포함 하 여 Microsoft 365와 통합 되는 방법을 궁금할 것입니다. siem 서버가 필요한 지 여부는 조직의 보안 요구 사항 등의 많은 요인에 따라 달라 집니다. Microsoft 365에서는 다양 한 보안 기능을 제공 합니다. 그러나 조직에서 온-프레미스와 클라우드에서 콘텐츠 및 응용 프로그램이 있는 경우 (하이브리드 클라우드 배포의 경우), 추가 보호를 위해 siem 서버를 추가 하는 것을 고려할 수 있습니다. 또는 조직이 특히 엄격한 보안 요구 사항을 충족 하는 경우에는 환경에 siem server를 추가 하는 것을 고려할 수 있습니다.

## <a name="siem-server-integration-microsoft-365"></a>siem 서버 통합 Microsoft 365

siem 서버는 다양 한 Microsoft 365 서비스 및 응용 프로그램에서 데이터를 받을 수 있습니다. 다음 표에는 몇 가지 Microsoft 365 서비스와 응용 프로그램과 siem server의 입력과 함께, siem 서버 통합에 대해 자세히 알아볼 수 있는 위치가 나와 있습니다. 

| Microsoft 365 서비스 또는 응용 프로그램 | siem 서버 입력 | 자세한 정보를 볼 수 있는 리소스 |
| --- | --- | --- |
| [Office 365 Advanced Threat Protection](office-365-atp.md) <br/>   또는   <br/>[Office 365 Threat Intelligence](office-365-ti.md) | 감사 로그 | [siem과 Office 365 Advanced Threat Protection의 통합](siem-integration-with-office-365-ti.md) |
| [Microsoft Cloud App Security](https://docs.microsoft.com/cloud-app-security/what-is-cloud-app-security) | 로그 통합 | [Microsoft Cloud App Security와의 siem 통합](https://docs.microsoft.com/cloud-app-security/siem) |
| [Office 365 Cloud App Security](office-365-cas-overview.md) | 로그 통합 | [Office 365 Cloud App Security와 SIEM 서버 통합](integrate-your-siem-server-with-office-365-cas.md) |
| [Windows Defender Advanced Threat Protection](https://docs.microsoft.com/windows/security/threat-protection/) | 로그 통합 | [siem 도구에 대 한 알림 가져오기](https://docs.microsoft.com/windows/security/threat-protection/windows-defender-atp/configure-siem-windows-defender-advanced-threat-protection) |
| [Azure 보안 센터](https://docs.microsoft.com/azure/security-center/security-center-intro) (위협 방지 및 위협 검색) | 경고 | [Azure 보안 데이터를 siem 파이프라인 구성으로 내보내기-미리 보기](https://docs.microsoft.com/azure/security-center/security-center-export-data-to-siem) |
| [Azure Active Directory id 보호](https://docs.microsoft.com/azure/active-directory/identity-protection/overview) | 감사 로그 | [Azure Active Directory 감사 로그 통합](https://docs.microsoft.com/azure/security/security-azure-log-integration-ad) |
| [Azure Advanced Threat Analytics](https://docs.microsoft.com/azure/security/azure-threat-detection) | 로그 통합 | [ATA siem 로그 참조](https://docs.microsoft.com/advanced-threat-analytics/cef-format-sa) |

## <a name="audit-logging-must-be-turned-on"></a>감사 로깅을 설정 해야 합니다.

siem 서버 통합을 구성 하기 전에 감사 로깅이 설정 되어 있는지 확인 합니다. 

- SharePoint Online, 비즈니스용 OneDrive 및 Azure Active Directory의 경우 [보안 & 준수 센터에서 감사 로깅이 설정 됩니다](https://docs.microsoft.com/office365/securitycompliance/turn-audit-log-search-on-or-off).

- Exchange Online의 경우 [감사 로깅은 Windows PowerShell을 사용 하 여 설정 됩니다](https://docs.microsoft.com/office365/securitycompliance/enable-mailbox-auditing).
 
## <a name="see-also"></a>참고 항목

[클라우드 채택 및 하이브리드 솔루션](https://docs.microsoft.com/office365/enterprise/cloud-adoption-and-hybrid-solutions)
  
[클라우드 도입 TLG(테스트 랩 가이드)](https://docs.microsoft.com/office365/enterprise/cloud-adoption-test-lab-guides-tlgs)


