---
title: Office 365 액세스 제어 모니터링 및 감사
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
description: '요약: Office 365 내에서 사용할 수 있는 다양 한 모니터링 및 감사 액세스 제어에 대 한 요약입니다.'
ms.openlocfilehash: 91d78ba3de41554755a7c19799eb1f7b25933b05
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30217738"
---
# <a name="monitoring-and-auditing-access-controls-in-office-365"></a><span data-ttu-id="258ea-103">Office 365의 액세스 제어 모니터링 및 감사</span><span class="sxs-lookup"><span data-stu-id="258ea-103">Monitoring and Auditing Access Controls in Office 365</span></span>

<span data-ttu-id="258ea-p101">Microsoft는 모든 위임, 모든 권한 사용 및 Office 365 내에서 발생 하는 모든 작업에 대 한 광범위 한 모니터링 및 감사를 수행 합니다. Office 365 액세스 제어는 최소 권한 원칙에 따라 자동화 된 프로세스 이며, 데이터 액세스 제어 및 감사를 통합 합니다.</span><span class="sxs-lookup"><span data-stu-id="258ea-p101">Microsoft performs extensive monitoring and auditing of all delegation, all use of privileges, and all operations that occur within Office 365. Office 365 access control is an automated process built on the principle of least privilege and to incorporate data access controls and audits:</span></span>
- <span data-ttu-id="258ea-106">허용 되는 모든 액세스는 고유 사용자가 추적할 수 있으므로 관리자가 고객 콘텐츠를 처리 하는 데 책임이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="258ea-106">All permitted access is traceable to a unique user, making administrators accountable for their handling of customer content.</span></span>
- <span data-ttu-id="258ea-107">액세스 제어 요청, 승인 및 관리 작업 로그는 보안 정보 및 악성 이벤트 분석을 위해 캡처됩니다.</span><span class="sxs-lookup"><span data-stu-id="258ea-107">Access control requests, approvals, and administrative operations logs are captured for analysis of security insights and malicious events.</span></span>
- <span data-ttu-id="258ea-108">액세스 수준은 보안 그룹 구성원을 기반으로 하 여 거의 실시간으로 검토 되며, 권한이 부여 된 비즈니스 근거 및 자격 요건을 충족 하는 사용자만 시스템에 액세스할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="258ea-108">Access levels are reviewed in near real-time based on security group membership to ensure that only users who have authorized business justifications and meet the eligibility requirements have access to the systems.</span></span>
- <span data-ttu-id="258ea-109">Office 365, 해당 액세스 제어 및 지원 서비스 (Azure Active Directory 및 실제 데이터 센터 포함)는 독립 타사에서 [ISO/iec 27001](https://www.microsoft.com/en-us/TrustCenter/Compliance/iso-iec-27001), [iso/iec 27018](https://www.microsoft.com/en-us/TrustCenter/Compliance/iso-iec-27018), [SOC](https://www.microsoft.com/en-us/TrustCenter/Compliance/SOC)를 준수 하기 위해 정기적으로 감사 됩니다. [FedRAMP](https://www.microsoft.com/en-us/TrustCenter/Compliance/FedRAMP)및 기타 [표준](https://www.microsoft.com/en-us/TrustCenter/Compliance?service=Office#Icons)</span><span class="sxs-lookup"><span data-stu-id="258ea-109">Office 365, its access controls, and supporting services, including Azure Active Directory and our physical datacenters, are regularly audited by independent third-parties for compliance with [ISO/IEC 27001](https://www.microsoft.com/en-us/TrustCenter/Compliance/iso-iec-27001), [ISO/IEC 27018](https://www.microsoft.com/en-us/TrustCenter/Compliance/iso-iec-27018), [SOC](https://www.microsoft.com/en-us/TrustCenter/Compliance/SOC), [FedRAMP](https://www.microsoft.com/en-us/TrustCenter/Compliance/FedRAMP), and other [standards](https://www.microsoft.com/en-us/TrustCenter/Compliance?service=Office#Icons).</span></span>
- <span data-ttu-id="258ea-110">Office 365 엔지니어는 연간 보안 교육을 통해 높은 수준의 액세스 모범 사례 및 위험을 검토 하 고 Microsoft의 보안 및 개인 정보 취급 방침을 승인 하 여 서비스에 대 한 권리를 계속 유지 하는 데 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="258ea-110">Office 365 engineers are required to take yearly security training reviewing elevated access best practices and risks and acknowledge Microsoft's security and privacy policies to continue maintaining their entitlements to the service.</span></span>

<span data-ttu-id="258ea-p102">짧은 기간 내에 여러 번 실패 한 로그인과 같은 의심 스러운 작업이 감지 되 면 자동화 된 경고가 트리거됩니다. Office 365 보안 응답 팀은 기계 학습 및 대규모 데이터 분석을 사용 하 여 불규칙 한 액세스 패턴에 대 한 활동을 검토 및 분석 하 고 비정상 및 불법 활동에 사전 대응 합니다. 또한 Microsoft는 서비스에서 보안 및 액세스 제어 문제를 찾기 위해 주기적으로 위험 팀을 전담 하 고 팀이 정기적으로 팀을 관리 하 고 있습니다. 고객은 감사 보고서 및 Office 365에서 제공 하는 관리 활동 API를 사용 하 여 액세스 제어 시스템의 효율성을 확인할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="258ea-p102">Automated alerts are triggered when suspicious activity is detected, such as multiple failed logins within a short period. The Office 365 Security Response team uses machine learning and big data analysis to review and analyze activity for irregular access patterns and to proactively respond to anomalous and illicit activities. Microsoft also employs a dedicated team of penetration testers and engages in periodic red team and blue team exercises to find security and access control issues in the service. Customers may also verify the effectiveness of access control systems by using audit reports and the management activity API provided by Office 365.</span></span> 

<span data-ttu-id="258ea-115">자세한 내용은 office [365 관리 활동 API 참조](https://msdn.microsoft.com/en-us/library/office/mt227394.aspx) 및 [감사 및 보고](office-365-auditing-and-reporting-overview.md)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="258ea-115">For more information, see [Office 365 Management Activity API reference](https://msdn.microsoft.com/en-us/library/office/mt227394.aspx) and [Auditing and Reporting in Office 365](office-365-auditing-and-reporting-overview.md).</span></span>
