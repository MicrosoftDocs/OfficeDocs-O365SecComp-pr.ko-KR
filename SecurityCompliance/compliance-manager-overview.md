---
title: Microsoft 준수 관리자 개요
ms.author: chvukosw
author: chvukosw
manager: laurawi
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
description: Microsoft 준수 관리자는 Microsoft Service Trust Portal의 무료 워크플로 기반 위험 평가 도구입니다. 준수 관리자를 사용 하면 Microsoft 클라우드 서비스와 관련 된 규정 준수 활동을 추적, 할당 및 확인할 수 있습니다.
ms.openlocfilehash: fe9b5ed704259a09e9663420b18e741d829a6b2d
ms.sourcegitcommit: 1947ad3c0dde9163ba9b6834d8b38bd04b4264a5
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/27/2019
ms.locfileid: "36643250"
---
# <a name="microsoft-compliance-manager-preview"></a>Microsoft 준수 관리자 (미리 보기)

> [!IMPORTANT]
> 준수 관리자는 21Vianet, Office 365 Germany, Office 365 미국 GCC(Government Community High) 또는 Office 365 미국방부에서 운영하는 Office 365에서 사용할 수 없습니다.

[Microsoft 준수 관리자 (미리 보기)](https://servicetrust.microsoft.com/ComplianceManager) 는 microsoft 클라우드 서비스와 관련 된 규정 준수 활동을 추적, 할당 및 확인 하는 데 사용할 수 있는 무료 워크플로 기반 위험 평가 도구입니다. 365 365 Microsoft 클라우드 서비스에 대 한 공유 책임 모델 내에서 규정 준수를 관리 하는 데 도움이 관리자를 제공 합니다. 준수 관리자는 Microsoft 서비스 평가에 대 한 표준, 규정 및 제어 구현 세부 정보 및 테스트 결과를 보기 위한 중앙 집중식 대시보드를 제공 합니다. 또한 조직과 관련 된 사용자 지정 컨트롤 구현 및 규정 준수 추적을 관리할 수 있는 도구도 포함 되어 있습니다.

준수 관리자를 사용 하는 경우 조직에서 다음을 수행할 수 있습니다.
  
- 조직에 적합 한 표준 및 규정에 대 한 준수 자가 평가를 통해 클라우드 서비스에 대 한 감사자 및 조정기에 제공 되는 자세한 준수 정보를 통합 합니다. 여기에는 ISO (국제 표준화 기구), NIST (표준 및 기술 협회), 건강 보험 이식성 및 책임 Act (HIPAA), 일반 데이터 GDPR (보호 규정) 및 기타 다양 한 기능
- 규정 준수 및 평가 관련 활동을 할당, 추적 및 기록 하 여 조직에서 팀 장벽에 따라 규정 준수 목표를 달성할 수 있도록 도와줍니다.
- 규정 준수 점수를 제공 하 여 진행 상황을 추적 하 고 조직의 위험에 대 한 노출을 줄이는 데 도움이 되는 감사 컨트롤의 우선 순위를 지정 합니다.
- 준수 활동과 관련 된 증거 및 기타 아티팩트를 업로드 하 고 관리 하기 위한 보안 리포지토리를 제공 합니다.
- 감사자, 조정기 및 기타 규정 준수 검토자를 위해 Microsoft 및 조직이 수행한 규정 준수 활동을 문서화 하는 상세한 Microsoft Excel 보고서를 작성 합니다.

> [!NOTE]
> 준수 관리자에 제공 되는 고객 작업은 권장 사항입니다. 구현 하기 전에 해당 규정 환경에서 이러한 권장 사항의 효과를 평가 하는 것이 조직에 게 있습니다. 준수 관리자에 게 제공 되는 권장 사항은 준수 보장으로 해석 되어서는 안 됩니다.

## <a name="compliance-manager-relationships"></a>준수 관리자 관계

준수 관리자는 준수 관리 활동에 도움이 되는 여러 구성 요소를 사용 합니다. 이러한 구성 요소는 함께 작동 하 여 감사자에 대 한 완전 한 관리 작업 흐름과 필요 없는 준수 보고서를 제공 합니다.

다음 다이어그램은 준수 관리자의 기본 구성 요소 간의 관계를 보여 줍니다.

![준수 관리자 버전 3의 관계](media/compliance-manager-relationships.png)

## <a name="groups"></a>그룹

[그룹](https://docs.microsoft.com/office365/securitycompliance/working-with-compliance-manager#groups) 은 평가를 구성 하 고, 동일한 또는 관련 고객 관리 컨트롤이 있는 평가 간에 일반 정보 및 워크플로 작업을 공유 하는 데 사용할 수 있는 컨테이너입니다. 같은 그룹의 서로 다른 두 평가에서 고객 관리 되는 컨트롤을 공유 하는 경우 컨트롤의 구현 세부 정보, 테스트 및 상태가 그룹의 다른 평가에서 같은 컨트롤과 자동으로 동기화 됩니다. 이렇게 하면 그룹 전체에서 각 컨트롤에 대해 할당 된 작업 항목이 통합 되 고 복제 작업이 줄어듭니다. 그룹을 사용 하 여 구성 하는 방법도 선택할 수 있습니다. 규정 준수 작업을 구성 하는 데 도움이 되는 연도, 영역, 준수 표준 또는 기타 그룹화 별 평가.

## <a name="assessments"></a>평가가

[평가](https://docs.microsoft.com/office365/securitycompliance/working-with-compliance-manager#assessments) 는 클라우드 서비스 보안 및 규정 준수 위험을 평가 하기 위해 Microsoft와 조직 간에 공유 되는 책임을 기반으로 컨트롤을 구성 하는 데 사용할 수 있는 컨테이너입니다. 평가는 준수 표준 및 적용 가능한 데이터 보호 표준, 규정 또는 법으로 지정 되는 데이터 보호 보호를 구현 하는 데 도움이 됩니다. 선택한 Microsoft 클라우드 서비스에 대해 선택한 산업 표준에 대 한 데이터 보호 및 준수 상태를 파악 하는 데 도움이 됩니다. 평가는 인증 표준에 매핑되는 평가에 포함 된 컨트롤 구현에 의해 완료 됩니다.

기본적으로 준수 관리자는 조직에 대해 다음과 같은 평가를 만듭니다.

- Office 365 ISO 27001
- Office 365 NIST 800-53
- Office 365 GDPR

평가에는 다음과 같은 몇 가지 구성 요소가 포함 됩니다.
  
- **범위 내 서비스**: 각 평가는 특정 Microsoft 서비스 집합에 적용 됩니다.
- **Microsoft 관리 컨트롤**: 각 클라우드 서비스에 대해 microsoft는 적용 가능한 표준과 규정에 대 한 준수 제어 집합을 구현 하 고 관리 합니다.
- **고객 관리 컨트롤**: 각 컨트롤에 대해 작업을 수행할 때 조직에서 구현 하는 컨트롤의 컬렉션입니다.
- **평가 점수**: 평가에서 고객 관리 컨트롤에 대 한 가능한 총 점수 비율입니다. 이를 통해 각 컨트롤에 할당 된 작업의 구현을 추적할 수 있습니다.

## <a name="controls"></a>컨트롤

[컨트롤](https://docs.microsoft.com/office365/securitycompliance/working-with-compliance-manager#controls-and-actions) 은 준수 작업을 관리 하는 방법을 정의 하는 준수 관리자의 규정 준수 프로세스 컨테이너입니다. 이러한 컨트롤은 해당 인증 또는 규정에 대 한 평가 구조와 부합 되는 제어 모음으로 구성 됩니다.

- **컨트롤 ID**: 해당 하는 인증 또는 규정에서 선택한 컨트롤의 이름입니다.
- **컨트롤 제목**: 해당 하는 인증 또는 규정의 컨트롤 ID 제목입니다.
- **문서 ID**:이 필드는 gdpr 평가에만 사용할 수 있으며 해당 gdpr 문서 번호를 지정 합니다.
- **설명**: 해당 하는 인증 또는 규정의 컨트롤 텍스트입니다. 저작권 제한으로 인해 ISO 표준에 대 한 관련 정보에 대 한 링크가 나열 됩니다.

![준수 관리자 버전 3의 컨트롤](media/compliance-manager-controls.png)

준수 관리자, **Microsoft 관리 되는 컨트롤**, **고객 관리 되는 컨트롤**및 **공유 관리 컨트롤** 의 세 가지 유형의 컨트롤이 있습니다.

### <a name="microsoft-managed-controls"></a>Microsoft 관리 컨트롤

각 클라우드 서비스에 대해 Microsoft는 다양 한 표준 및 규정을 준수 하는 Microsoft의 기능으로 컨트롤 집합을 구현 하 고 관리 합니다. 각 컨트롤은 Microsoft 및/또는 독립 타사 감사자에 의해 제어가 어떻게 구현 되 고 해당 구현이 어떻게 테스트 되 고 유효성이 검사 되었는지에 대 한 세부 정보를 제공 합니다.

### <a name="customer-managed-controls"></a>고객 관리 컨트롤

조직에서 관리 하는 컨트롤의 컬렉션입니다. 조직은 지정 된 표준 또는 규정에 대 한 준수 프로세스의 일환으로 고객 관리 제어 구현을 담당 합니다. 고객 관리 컨트롤은 해당 하는 인증 또는 규제에 대 한 제어 패밀리로 구성 됩니다. 고객 관리 컨트롤을 사용 하 여 규정 준수 작업의 일환으로 Microsoft에서 제안한 권장 조치를 구현할 수 있습니다. 조직에서는 각 고객 관리 컨트롤의 규범적 지침 및 권장 되는 고객 작업을 사용 하 여 해당 컨트롤에 대 한 구현 및 평가 프로세스를 관리할 수 있습니다.

또한 평가의 고객 관리 컨트롤에는 평가 완료에 대 한 진행률을 관리 하 고 추적 하는 데 사용할 수 있는 기본 제공 워크플로 관리 기능도 있습니다. 이 워크플로 기능을 사용 하 여 다음을 수행할 수 있습니다.

- 각 컨트롤에 대해 작업 항목 할당
- 할당 된 작업 항목 추적
- 컨트롤 구현의 증거 업로드
- 컨트롤의 테스트 및 유효성 검사 문서화
- 작업 항목을 구현 및 테스트 된 것으로 표시

예를 들어 조직의 규정 준수 관리자는 IT 관리자에 게 권장 작업을 수행 하는 데 필요한 책임 및 권한이 있는 작업 항목을 할당 합니다. IT 관리자는 구현 작업의 증거 (구성 또는 정책 설정 스크린샷)를 업로드 하 고 완료 되 면 해당 작업 항목을 준수 관리자에 게 다시 할당 합니다. 규정 준수 책임자는 수집 된 증거를 평가 하 고, 컨트롤 구현을 테스트 하며, 준수 관리자에 게 구현 날짜 및 테스트 결과를 기록 합니다.

### <a name="shared-management-controls"></a>공유 관리 컨트롤

공유 컨트롤은 Microsoft와 고객이 모두 구현 하기 위해 책임을 공유 하는 모든 컨트롤을 참조 합니다. 예를 들어 직원 차단, 계정 및 암호 관리 및 암호화와 관련 된 컨트롤은 Microsoft와 고객 모두에 게 작업을 수행 해야 합니다.

## <a name="action-items"></a>작업 항목

[작업 항목](https://docs.microsoft.com/office365/securitycompliance/working-with-compliance-manager#controls-and-actions) 은 평가 완료 진행률을 관리 하 고 추적 하는 데 사용할 수 있는 기본 제공 워크플로 관리 기능의 일부로 서 고객 관리 되는 컨트롤에 포함 됩니다.

조직의 구성원은 준수 관리자를 사용 하 여 해당 사용자가 할당 된 모든 평가에서 고객 관리 되는 컨트롤을 검토할 수 있습니다. 사용자가 준수 관리자에 로그인 하 고 **작업 항목** 대시보드를 열면 할당 된 작업 항목 목록이 표시 됩니다. 사용자에 게 할당 된 준수 관리자 역할에 따라 구현 또는 테스트 세부 정보를 제공 하거나 상태를 업데이트 하거나 작업 항목을 할당할 수 있습니다.

인증 컨트롤은 일반적으로 한 사람에 의해 구현 되며 다른 사용자가 테스트 합니다. 예를 들어 초기에 한 사람에 게 할당 된 작업 항목이 완료 된 후에는 다음 사용자에 게 증거를 테스트 및 업로드 하기 위한 작업 항목이 할당 됩니다. 컨트롤 할당에 대 한 충분 한 사용 권한이 있는 모든 사용자는 작업 항목을 할당 하 고 다시 할당할 수 있습니다. 이를 통해 제어 할당을 중앙 집중식으로 관리 하 고 implementors 및 테스터 간에 작업 항목을 분산 하 여 라우팅할 수 있습니다.

## <a name="permissions"></a>사용 권한

준수 관리자가 역할 기반 액세스 제어 [권한 모델](https://docs.microsoft.com/office365/securitycompliance/working-with-compliance-manager#permissions)을 사용 합니다. 기본적으로 Azure Active Directory (Azure AD) 계정을 사용 하는 조직의 모든 사용자에 게는 모든 권한이 있으며 준수 관리자에서 모든 작업을 수행할 수 있습니다. 조직에서 역할 기반 액세스 제어를 구현한 후에는 정의 된 준수 관리자 역할에 할당 되지 않은 모든 사용자에 게 게스트 액세스 권한을 할당 합니다. Microsoft 서비스 담당자는 입력 하거나 업로드 하는 모든 데이터에 대 한 액세스 권한이 없습니다.

기본 사용 권한을 변경 하 고 전체 역할 기반 액세스 제어 모델을 구현 하려면 각 준수 관리자 역할에 하나 이상의 사용자를 추가 해야 합니다. 사용자가 역할에 추가 되 면 해당 역할에 할당 된 작업을 수행 하는 권한이 모든 사용자가 사용할 수 있는 기본 사용 권한 집합에서 제거 됩니다. 이 역할을 사용 하 여 프로 비전 된 사용자만 준수 관리자에 액세스 하 고 해당 역할에서 허용 하는 작업을 수행할 수 있습니다.

평가를 관리 하기 위해 역할에 사용자를 추가 하는 경우 해당 역할의 구성원만 평가를 관리할 수 있습니다. 사용자가 평가에서 데이터를 읽을 수 있도록 하는 사용자를 역할에 추가 하지 않으면 조직의 모든 사용자가 규정 준수 관리자에 액세스 하 고 모든 평가에서 데이터를 읽을 수 있습니다.
  
## <a name="manage-evidence"></a>증거 관리

준수 관리자는 고객 관리 컨트롤의 테스트 및 유효성 검사를 수행 하기 위한 구현 작업의 증거를 저장할 수 있습니다. 증거에는 문서, 스프레드시트, 스크린샷, 이미지, 스크립트, 스크립트 출력 파일 및 기타 파일이 포함 되어 있습니다. 또한 준수 관리자는 원격 분석을 자동으로 수신 하 고 보안 점수와 통합 된 작업 항목에 대 한 증거 레코드를 만듭니다. 준수 관리자에 증거로 업로드 된 모든 데이터는 Microsoft 클라우드 저장소 사이트의 미국에 저장 됩니다. 이 데이터는 동남 아시아 및 서유럽에 있는 Azure 지역 간에 복제 됩니다.

## <a name="templates"></a>템플릿

준수 관리자는 미리 구성 된 [서식 파일](https://docs.microsoft.com/office365/securitycompliance/working-with-compliance-manager#templates) 을 평가에 제공 하며, 규정 준수 요구 사항에 맞게 고객 관리 컨트롤에 대 한 사용자 지정 서식 파일을 만들 수 있습니다. 새 템플릿은 Excel 파일에서 컨트롤 정보를 가져오거나, 기존 서식 파일의 복사본에서 서식 파일을 만들 수 있습니다.

준수 관리자에 포함 된 미리 구성 된 서식 파일은 다음과 같습니다.
 
- [ISO 27001:2013](https://www.iso.org/obp/ui/#iso:std:iso-iec:27001:ed-2:v1:en)
- [ISO 27018:2019](https://www.iso.org/obp/ui/#iso:std:iso-iec:27018:ed-2:v1:en)
- [NIST 800-53](https://csrc.nist.gov/publications/detail/sp/800-53/rev-4/final)
- [NIST 800-171](https://csrc.nist.gov/publications/detail/sp/800-171/rev-1/final)
- [NIST Cybersecurity Framework (CSF)](https://www.nist.gov/cyberframework)
- [CSA (cloud Security 제휴) 3.0.1 (CCM)](https://cloudsecurityalliance.org/working-groups/cloud-controls-matrix/#_overview)
- [연방 금융 기관 검사 Council (FFIEC) 정보 보안 소책자](https://ithandbook.ffiec.gov/it-booklets/information-security.aspx) 
- [HIPAA](https://www.hhs.gov/hipaa/for-professionals/index.html) / [HITECH](https://www.hhs.gov/hipaa/for-professionals/special-topics/hitech-act-enforcement-interim-final-rule/index.html)
- [FedRAMP 보통](https://www.fedramp.gov/documents/)
- [유럽 연합 GDPR](https://eur-lex.europa.eu/legal-content/EN/TXT/HTML/?uri=CELEX:32016R0679&from=EN)

## <a name="compliance-score"></a>준수 점수

[준수 점수](compliance-score-methodology.md) 는 조직에서 규정 준수를 이해 하 고 관리 하는 데 도움이 되는 준수 관리자의 핵심 구성 요소입니다. [Microsoft 보안 점수](microsoft-secure-score.md)와 마찬가지로 준수 점수는 조직의 데이터 보호, 개인 정보 및 보안과 관련 된 활동에 대 한 동작 기반 점수 매기기 시스템입니다. 평가에 대 한 준수 점수는 지정 된 표준 또는 규정을 준수 하는 식입니다. 수치 점수가 높을수록 평가에 대 한 준수도가 향상 됩니다. 규정 준수 성과를 이해 하는 것은 필요한 고객 관리 제어 작업의 우선 순위를 지정 하는 데 중요 합니다.
  
> [!IMPORTANT]
> 준수 점수는 특정 표준 및 규정에 대해 조직 차원의 규정 준수에 대한 절대 측정 결과를 나타내지 않습니다. 개인 데이터 및 개별 개인 정보 보호에 대한 위험을 줄일 수 있는 컨트롤 채택 수준을 나타냅니다. 사용자의 표준 또는 규정 준수를 보장하는 서비스는 없으며, 준수 점수는 어떤 경우든 준수 보장으로 해셕되면 안 됩니다.

## <a name="secure-score-integration"></a>보안 점수 통합

준수 관리자는 동기화 된 작업 항목에 대 한 준수 점수에 보안 점수 학점을 자동으로 적용 하기 위해 [Microsoft 보안 점수](microsoft-secure-score.md) 와 통합 되어 있습니다. 개별 작업 항목에 대해 구성할 수 있으며 항목 간의 지속적인 업데이트를 제공 합니다.

예를 들어 조직에서 준수 관련 작업 항목에도 적용 되는 Azure 권한 관리를 활성화 하는 데 필요한 보안 관련 요구 사항이 있습니다. Azure 권한 관리가 정품 인증 되 고 보안 점수에 의해 처리 되 면 준수 관리자는 업데이트 알림을 받으며, 작업 항목의 점수가 완료 크레딧을 통해 자동으로 업데이트 됩니다.

## <a name="ready-to-get-started"></a>시작할 준비가 되셨습니까?

[준수 관리자를 사용](working-with-compliance-manager.md) 하 여 조직에 대 한 규정 준수 활동을 관리 하기 시작 합니다.

## <a name="resources"></a>리소스

- [대화형 가이드: 준수 관리자를 사용 하 여 데이터 보호 컨트롤 평가 및 개선](https://content.cloudguides.com/guides/Compliance%20Manager)
- [Microsoft 보안, 개인 정보 보호 및 준수 기술 커뮤니티](https://techcommunity.microsoft.com/t5/Security-Privacy-Compliance/ct-p/SecurityPrivacyCompliance)
