---
title: Office 365 Advanced Threat Protection
ms.author: deniseb
author: denisebmsft
manager: dansimp
ms.date: 03/28/2019
audience: Admin
ms.topic: hub-page
ms.service: O365-seccomp
localization_priority: Priority
search.appverid:
- MET150
- MOE150
ms.assetid: e100fe7c-f2a1-4b7d-9e08-622330b83653
ms.collection:
- M365-security-compliance
description: Office 365 Advanced Threat Protection에는 안전한 첨부 파일, 안전한 링크, 고급 피싱 도구, 보고 도구 및 위협 인텔리전스 기능이 포함 되어 있습니다.
ms.openlocfilehash: 96e79a8aabe0788388473da9fcd514b9285e1c00
ms.sourcegitcommit: 33c8e9c16143650ca443d73e91631f9180a9268e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/25/2019
ms.locfileid: "35854782"
---
# <a name="office-365-advanced-threat-protection"></a>Office 365 Advanced Threat Protection

> [!IMPORTANT]
> 이 문서는 [Office 365 Advanced Threat Protection](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description)을 사용 하는 비즈니스 고객을 위한 것입니다. Outlook.com, Office 365 Home 또는 Office 365 Personal을 사용 하는 경우 Outlook의 안전한 링크에 대 한 정보를 찾으려면 [Advanced Outlook.com security](https://support.office.com/article/advanced-outlook-com-security-for-office-365-subscribers-882d2243-eab9-4545-a58a-b36fee4a46e2)를 참조 하세요.

## <a name="overview"></a>개요

Office 365 ATP (Advanced Threat Protection)는 전자 메일 메시지, 링크 (Url) 및 공동 작업 도구로 인해 야기 되는 악의적인 위협 으로부터 조직을 보호 합니다. ATP에는 다음이 포함 됩니다.

- [위협 보호 정책](#configure-atp-policies): 위협 방지 정책을 정의 하 여 조직에 적합 한 보호 수준을 설정 합니다. 

- [보고서](#view-atp-reports): 실시간 보고서를 확인 하 여 조직의 ATP 성능을 모니터링 합니다. 

- [위협 조사 및 응답 기능](#use-threat-investigation-and-response-capabilities): 주요에 지 도구를 사용 하 여 위협을 조사, 이해, 시뮬레이트 및 방지 합니다. 

- [자동화 된 조사 및 응답 기능](#save-time-with-automated-investigation-and-response): 시간과 노력을 절감 하 고 위협을 완화 합니다.

## <a name="office-365-atp-plan-1-and-plan-2"></a>Office 365 ATP 계획 1 및 계획 2

ATP는 Office 365 E5에 포함 되어 있습니다. 그러나 ATP 요금제 및 ATP 계획 2는 각각 특정 구독의 추가 기능으로 사용할 수 있습니다. 자세한 내용은 [ATP 계획에서의 기능 가용성](https://docs.microsoft.com/en-us/office365/servicedescriptions/office-365-advanced-threat-protection-service-description#feature-availability-across-advanced-threat-protection-atp-plans)을 참조 하십시오.

## <a name="configure-atp-policies"></a>ATP 정책 구성

Office 365 ATP는 조직에 적합 한 보호 수준을 설정 하기 위한 다양 한 도구를 제공 합니다. 

조직의 보안 팀은 Office 365 보안 & 준수 센터에서 각 ATP 도구에 대 한 정책을 정의 해야 합니다. **위협 관리** > **정책** 으로 이동 하 여 정책 옵션에 액세스 합니다. 이에 대 한 도움말을 보려면 [Quick Start Guide: Set Up Office 365 Advanced Threat Protection](checklist-atp-setup.md)를 참조 하세요.

조직에 대해 정의 된 정책에 따라 미리 정의 된 위협에 대 한 동작 및 보호 수준이 결정 됩니다. 정책 옵션은 매우 유연 합니다. 예를 들어 조직의 보안 팀은 사용자, 조직, 받는 사람 및 도메인 수준에서 세분화 된 위협 보호를 설정할 수 있습니다. 매일 새로운 위협과 과제가 발생 하기 때문에 정책을 정기적으로 검토 하는 것이 중요 합니다.  

- [ATP 안전한 첨부 파일](atp-safe-attachments.md): 악성 콘텐츠에 대 한 전자 메일 첨부 파일을 확인 하 여 메시징 시스템을 보호 하는 제로 일 보호를 제공 합니다. 바이러스/맬웨어 서명이 없는 모든 메시지와 첨부 파일을 특수 한 환경으로 라우팅합니다. 그런 다음 컴퓨터 학습 및 분석 기법을 사용 하 여 악의적인 의도를 검색 합니다. 의심 스러운 활동이 발견 되지 않으면 메시지가 사서함으로 전달 됩니다. 자세한 내용은 [Office 365 ATP 안전 첨부 파일 정책 설정을](set-up-atp-safe-attachments-policies.md)참조 하십시오.

- [ATP 안전한 링크](atp-safe-links.md): 전자 메일 메시지 및 Office 파일 등의 url을 클릭 하는 데 걸리는 시간을 확인 합니다. 보호는 진행 중 이며 메시징 및 Office 환경 전체에 적용 됩니다. 각 클릭에 대해 링크가 검색 됩니다. 안전한 링크는 계속 액세스할 수 있으며 악성 링크는 동적으로 차단 됩니다. 자세한 내용은 [Office 365 ATP 안전한 링크 정책 설정을](https://docs.microsoft.com/en-us/office365/securitycompliance/set-up-atp-safe-links-policies)참조 하십시오. 

- [SharePoint, OneDrive 및 Microsoft 팀에 대 한 ATP](atp-for-spo-odb-and-teams.md): 사용자가 팀 사이트 및 문서 라이브러리에서 악의적인 파일을 식별 하 고 차단 하 여 파일을 공동 작업 하 고 공유할 때 조직을 보호 합니다. 자세한 내용은 [SharePoint, OneDrive 및 Microsoft Teams에 대한 Office 365 ATP 실행](turn-on-atp-for-spo-odb-and-teams.md)을 참조하세요. 

- [ATP 피싱 방지 보호](atp-anti-phishing.md): 사용자 및 사용자 지정 도메인 가장을 검색 하려는 시도를 감지 합니다. Avert 피싱 공격에 기계 학습 모델 및 고급 가장 검색 알고리즘을 적용 합니다. 자세한 내용은 [Office 365 ATP 피싱 방지 및 피싱 방지 정책을](set-up-anti-phishing-policies.md)참조 하세요.

## <a name="view-atp-reports"></a>ATP 보고서 보기

Office 365 ATP에는 ATP 성능을 모니터링 하기 위한 고급 [보고 대시보드가](view-reports-for-atp.md) 포함 되어 있습니다. 보안 & 준수 센터의 **보고서 > 대시보드에서** 액세스할 수 있습니다. 

최신 정보를 제공 하는 실시간으로 업데이트를 보고 합니다. 이러한 보고서는 권장 사항을 제공 하 고 곧 위협을 임박한 것을 알립니다. 미리 정의 된 보고서에는 다음이 포함 됩니다. 

- [위협 탐색기 (또는 실시간 검색)](threat-explorer.md)

- [위협 방지 상태 보고서](view-reports-for-atp.md#threat-protection-status-report)

- [ATP 파일 형식 보고서](view-reports-for-atp.md#atp-file-types-report)

- [ATP 메시지 처리 보고서](view-reports-for-atp.md#atp-message-disposition-report)

- ... 등이 있습니다. 

## <a name="use-threat-investigation-and-response-capabilities"></a>위협 조사 및 응답 기능 사용

Office 365 ATP 계획 2에는 조직의 보안 팀이 악의적인 공격을 예측, 이해 및 방지할 수 있도록 하는 최상의 [위협 조사 및 응답 도구가](office-365-ti.md) 포함 되어 있습니다. 

- [위협 추적기](threat-trackers.md) 는 prevailing cybersecurity 문제에 대 한 최신 인텔리전스를 제공 합니다. 예를 들어 최신 맬웨어에 대 한 정보를 보고, 조직에 대 한 실제 위협이 되기 전에 대책을 취할 수 있습니다. 사용 가능한 추적기에는 [중요 한 추적기](threat-trackers.md#noteworthy-trackers), [추세 분석](threat-trackers.md#trending-trackers), 추적 [된](threat-trackers.md#saved-queries) [쿼리](threat-trackers.md#tracked-queries)및 저장 되는 쿼리가 포함 됩니다.

- [위협 탐색기 (또는 실시간 검색)](threat-explorer.md) (탐색기 라고도 함)은 최근 위협을 식별 하 고 분석 하는 데 사용할 수 있는 실시간 보고서입니다. 사용자 지정 기간에 대 한 데이터를 표시 하도록 탐색기를 구성할 수 있습니다.

- [공격 시뮬레이터](attack-simulator.md) 를 사용 하면 조직에서 현실적인 공격 시나리오를 실행 하 여 vulnerabilites를 식별할 수 있습니다. [표시 이름 스피어 피싱 공격](attack-simulator.md#display-name-spear-phishing-attack), [암호 분무 공격](attack-simulator.md#password-spray-attack), [무작위 암호 공격](attack-simulator.md#brute-force-password-attack)등을 비롯 한 현재 유형의 공격에 대 한 시뮬레이션을 사용할 수 있습니다.
    
## <a name="save-time-with-automated-investigation-and-response"></a>자동화 된 조사 및 응답으로 시간 절약

(**새로운 방법!**) 잠재적인 사이버 공격을 조사 하는 경우 시간이 본질적으로 시간입니다. 위협을 식별 하 고 완화할 수 있을 수록 조직의 성능이 향상 됩니다. Office 365 ATP 계획 2에는 이제 [자동 조사 및 응답 (AIR)](automated-investigation-response-office.md) 기능이 포함 되어 있습니다. (이러한 기능이 아직 없는 경우 ATP 계획 2를 사용 하 여 곧 제공 될 예정입니다.)

AIR에는 경고가 트리거될 때 또는 탐색기의 보기와 같이 수동으로 시작할 수 있는 보안 playbook 집합이 포함 되어 있습니다. AIR에서는 위협, 효과적이 고 효율적으로 위협을 완화 하기 위해 보안 작업 팀의 시간과 노력을 절감할 수 있습니다. 자세한 내용은 [Office 365의 자동화 된 조사 및 응답 (AIR)](automated-investigation-response-office.md)을 참조 하세요.

## <a name="permissions-required-to-use-atp-features"></a>ATP 기능을 사용 하는 데 필요한 사용 권한

보안 & 준수 센터에서 ATP 기능에 액세스 하려면 적절 한 역할을 할당 받아야 합니다. 다음 표에는 몇 가지 예가 나와 있습니다.

|역할 또는 역할 그룹  |자세한 정보를 볼 수 있는 리소스  |
|---------|---------|
|Office 365 전역 관리자 |[Office 365 관리자 역할 정보](https://docs.microsoft.com/office365/admin/add-users/about-admin-roles)|
|보안 관리자 |[Azure Active Directory의 관리자 역할 권한](https://docs.microsoft.com/en-us/azure/active-directory/users-groups-roles/directory-assign-admin-roles)|
|Exchange Online 조직 관리 |[Exchange Online의 사용 권한](https://docs.microsoft.com/en-us/exchange/permissions-exo/permissions-exo) <br>한<br> [Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/exchange-online-powershell?view=exchange-ps)|

자세한 내용은 다음을 참조하세요.

- [보안 및 준수 센터의 사용 권한](permissions-in-the-security-and-compliance-center.md) 

- [사용자에게 보안 및 준수 센터에 대한 액세스 권한 부여](grant-access-to-the-security-and-compliance-center.md)

## <a name="get-office-365-atp"></a>Office 365 ATP 받기

Office 365 ATP 계획 2는 Office 365 Enterprise E5, Office 365 교육 A5 및 Microsoft 365 Business에 포함 되어 있습니다. 구독에 Office 365 ATP가 포함 되어 있지 않은 경우 ATP 계획 1 또는 ATP 계획 2를 특정 구독에 대 한 추가 기능으로 구입할 수 있습니다. 자세한 내용은 다음 리소스를 참조 하십시오.

- ATP 계획을 포함 하는 구독 목록은 [Office 365 atp (Advanced Threat Protection) 사용 가능 여부](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description#office-365-advanced-threat-protection-atp-availability) 를 참조 하세요.

- 계획 1 및 2에 포함 된 기능 목록은 [ATP (Advanced Threat Protection) 계획에서 기능 가용성](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description#feature-availability-across-advanced-threat-protection-atp-plans) 을 참조 하십시오.

- 요금제를 비교 하 고 Office 365 ATP를 구매 하려면 [적절 한 Office 365 Advanced Threat Protection](https://products.office.com/exchange/advance-threat-protection#pmg-allup-content) 을 참조 하세요.

## <a name="new-features-in-office-365-atp"></a>Office 365 ATP의 새로운 기능

Office 365 ATP에 새로운 기능이 지속적으로 추가 됩니다. 자세한 내용은 다음 리소스를 참조 하십시오.

- [Microsoft 365 로드맵](https://www.microsoft.com/microsoft-365/roadmap?filters=&searchterms=advanced%2Cthreat%2Cprotection) 에서는 개발 및 롤아웃의 새로운 기능 목록을 제공 합니다.

- [Office 365 Advanced Threat Protection 서비스 설명](https://docs.microsoft.com/en-us/office365/servicedescriptions/office-365-advanced-threat-protection-service-description#whats-new-in-office-365-advanced-threat-protection-atp) 에서는 ATP 계획 별 기능 및 가용성에 대해 설명 합니다.
