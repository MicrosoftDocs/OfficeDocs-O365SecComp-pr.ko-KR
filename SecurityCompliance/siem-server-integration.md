---
title: Microsoft 365 SIEM 서버 통합
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.audience: ITPro
ms.topic: article
ms.date: 10/29/2018
ms.service: o365-solutions
localization_priority: Normal
ms.collection: Ent_O365
ms.custom:
- Ent_Solutions
- SIEM
- M365-security-compliance
description: '요약: Microsoft 365 SIEM 서버 통합을 대략적를이 문서를 읽어봅니다.'
ms.openlocfilehash: a6e139d14a7ea3625b2d2fffec5ad5d913ea9184
ms.sourcegitcommit: efccf5b4f22d34a9674bc55ebf3d88bc8bda2972
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/14/2019
ms.locfileid: "29995199"
---
# <a name="siem-server-integration-with-microsoft-365-services-and-applications"></a>Microsoft 365 서비스 및 응용 프로그램의 SIEM 서버 통합

## <a name="overview"></a>개요

조직에는 보안 정보 및 이벤트 관리 (SIEM) 서버를 사용 하는 서버를 파악 한 SIEM 곧를 계획 하는 경우 하는지에 대해 어떻게 Office 365 Enterprise를 포함 하 여 Microsoft 365, 통합 하는 경우. SIEM 서버의 필요 여부는 조직의 보안 요구 사항 등의 여러 요인에 따라 달라 집니다. Microsoft 365 다양 한 보안 기능입니다. 그러나 온-프레미스 및 클라우드 (예: 하이브리드 클라우드 배포의 경우)에서 조직에 콘텐츠 및 응용 프로그램을 하는 경우 추가 보호에 대 한 SIEM 서버 추가 (영문) 고려 될 수 있습니다. 또는 조직에 특히 엄격한 보안 요구 사항을 충족 해야, 경우 환경에 추가 하는 SIEM 서버를 고려할 수 있습니다.

## <a name="siem-server-integration-microsoft-365"></a>Microsoft 365 SIEM 서버 통합

SIEM 서버는 다양 한 Microsoft 365 서비스 및 응용 프로그램에서에서 데이터를 받을 수 있습니다. 다음 표에서 여러 Microsoft 365 서비스 및 응용 프로그램 SIEM 서버 입력 및 SIEM 서버 통합 하는 방법에 대 한 자세한 내용은 이동할 위치를 나열 합니다. 

| Microsoft 365 서비스 또는 응용 프로그램 | SIEM 서버 입력 | 자세한 내용은 리소스 |
| --- | --- | --- |
| [Office 365 Advanced Threat Protection 방지](office-365-atp.md) <br/>   또는   <br/>[Office 365 위협 인텔리전스](office-365-ti.md) | 감사 로그 | [Office 365 위협 인텔리전스 및 고급 위협 보호 SIEM 통합](siem-integration-with-office-365-ti.md) |
| [Microsoft Cloud App Security](https://docs.microsoft.com/cloud-app-security/what-is-cloud-app-security) | 로그의 통합 | [Microsoft 클라우드 앱 보안 SIEM 통합](https://docs.microsoft.com/cloud-app-security/siem) |
| [Office 365 Cloud App Security](office-365-cas-overview.md) | 로그의 통합 | [Office 365 Cloud App Security와 SIEM 서버 통합](integrate-your-siem-server-with-office-365-cas.md) |
| [Windows Defender Advanced Threat Protection](https://docs.microsoft.com/windows/security/threat-protection/) | 로그의 통합 | [SIEM 도구 끌어오기 알림](https://docs.microsoft.com/windows/security/threat-protection/windows-defender-atp/configure-siem-windows-defender-advanced-threat-protection) |
| [Azure 보안 센터](https://docs.microsoft.com/azure/security-center/security-center-intro) (위협 보호 및 위협 감지) | 알림 | [SIEM-파이프라인 구성-미리 보기를 azure 보안 데이터 내보내기](https://docs.microsoft.com/azure/security-center/security-center-export-data-to-siem) |
| [Azure Active Directory Id 보호](https://docs.microsoft.com/azure/active-directory/identity-protection/overview) | 감사 로그 | [Azure Active Directory 감사 로그를 통합 합니다.](https://docs.microsoft.com/azure/security/security-azure-log-integration-ad) |
| [Azure 고급 위협 분석](https://docs.microsoft.com/azure/security/azure-threat-detection) | 로그의 통합 | [ATA SIEM 로그 참조 (영문)](https://docs.microsoft.com/advanced-threat-analytics/cef-format-sa) |

## <a name="audit-logging-must-be-turned-on"></a>감사 로깅을 설정 해야

SIEM 서버 통합을 구성 하기 전에 감사 로깅이 설정 되어있는지 확인 합니다. 

- SharePoint online, 비즈니스 및 Azure Active Directory [보안 & 준수 센터의에서 감사 로깅이 설정](https://docs.microsoft.com/office365/securitycompliance/turn-audit-log-search-on-or-off)에 대 한 OneDrive 합니다.

- 에 대 한 Exchange Online, [Windows PowerShell을 사용한 감사 로깅이 켜져](https://docs.microsoft.com/office365/securitycompliance/enable-mailbox-auditing)있습니다.
 
## <a name="see-also"></a>참고 항목

[클라우드 채택 및 하이브리드 솔루션](https://docs.microsoft.com/office365/enterprise/cloud-adoption-and-hybrid-solutions)
  
[클라우드 도입 TLG(테스트 랩 가이드)](https://docs.microsoft.com/office365/enterprise/cloud-adoption-test-lab-guides-tlgs)


