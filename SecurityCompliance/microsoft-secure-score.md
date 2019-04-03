---
title: Microsoft Secure Score
description: Microsoft 365 보안 점수, 세부 정보를 계산 하는 방법 및 보안 관리자가이를 사용 하는 것으로 예상할 수 있는 사항을 설명 합니다.
keywords: 보안, 맬웨어, Microsoft 365, M365, 보안 점수, 보안 센터, 개선 작업
ms.prod: w10
ms.mktglfcycl: deploy
ms.localizationpriority: medium
ms.author: ellevin
author: levinec
manager: dansimp
audience: ITPro
ms.collection: M365-security-compliance
ms.topic: article
search.appverid: met150
ms.openlocfilehash: fa76e2edd3f66595a47fb511881f15c07b441c77
ms.sourcegitcommit: 8213c353954b92f5c3979bee4aa049da0fd28a18
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/03/2019
ms.locfileid: "31043249"
---
# <a name="microsoft-secure-score"></a>Microsoft Secure Score

microsoft 365 보안 센터에서 microsoft 보안 점수를 사용 하 여 조직의 보안 상태에 대 한 가시성과 제어를 향상 시킬 수 있습니다. 중앙 집중식 대시보드에서 Microsoft 365 id, 데이터, 앱, 장치 및 인프라에 대 한 보안을 모니터링 하 고 향상 시킬 수 있습니다.

Microsoft 보안 점수는 강력한 시각화, 다른 Microsoft 제품과의 통합, 다른 회사와의 점수 비교, 범주별 필터링 등을 제공 합니다. 이 도구를 사용 하 여 조직 내에서 보안 개선 작업을 완료 하 고 점수 기록을 추적할 수 있습니다. 또한이 점수는 타사 솔루션에서 권장 되는 개선 작업을 해결 한 경우에도 반영 될 수 있습니다.  

## <a name="how-it-works"></a>작업 방법

권장 되는 보안 기능을 구성 하 고, 보고서 보기와 같은 보안 관련 작업을 수행 하거나, 타사 응용 프로그램 또는 소프트웨어를 사용 하 여 개선 작업을 처리 하기 위한 사항이 제공 됩니다. 일부 작업은 사용자에 게 MFA (multi-factor authentication)를 사용 하도록 설정 하는 것과 같은 부분 완성에 대해 점수가 지정 됩니다. 보안은 항상 유용성과 균형을 유지 해야 하며 환경에 적합 한 모든 권장 사항은 아닙니다.

## <a name="required-permissions"></a>필요한 사용 권한

현재, Microsoft 보안 점수를 보려면 Azure Active Directory에서 다음 역할 중 하나를 할당 받아야 합니다.

* 전역 관리자
* 보안 관리자
* 보안 독자

## <a name="rich-experiences--additional-security-recommendations"></a>추가 보안 권장 사항을 & 하는 다양 한 환경

Microsoft 보안 점수가 azure AD, Intune 및 Cloud App Security에서 권장 사항이 추가 되었으며 azure 보안 센터 및 Windows Defender ATP의 권장 사항이 제공 됩니다. 또한 Office 365 보안 권장 사항도 추가 되었습니다. 보다 광범위 한 Microsoft 제품 및 서비스 집합에 대 한 추가 통찰력과 가시성을 통해 조직의 보안 상태에 대 한 관리를 확실 하 게 보고할 수 있습니다. [Microsoft Graph API](https://docs.microsoft.com/graph/api/resources/securescores?view=graph-rest-beta)를 사용 하 여 점수를 얻을 수도 있습니다.

필요한 정보를 보다 신속 하 게 지원 하기 위해 Microsoft 추천은 그룹으로 구성 됩니다.

* id (Azure AD 계정 및 역할의 보호 상태)
* 데이터 (Office 365 문서의 보호 상태)
* 장치 (장치의 보호 상태) 곧 출시 될 Windows Defender ATP 향상 작업
* 앱 (전자 메일 및 클라우드 앱의 보호 상태)
* 인프라 (Azure 리소스의 보호 상태, 출시 예정)

Microsoft 보안 점수 개요 페이지에서 이러한 그룹 간의 점수가 분할 되는 방식과 사용할 수 있는 지점을 볼 수 있습니다. 개요 페이지는 또한 전체 점수에 대 한 모든 보기, 벤치 마크 비교를 사용한 보안 점수의 역사적 추세 및 점수를 높이기 위해 수행할 수 있는 향상 작업의 우선 순위를 지정 하는 위치를 제공 합니다. 이 데이터를 사용 하 여 보안 환경을 작동 하 고 큰 차이를 내릴 수 있습니다.  

![M365 홈](./media/secure-score/homepage-original.png)
페이지*그림 1: Microsoft 보안 점수 개요 페이지*

## <a name="take-action-to-improve-your-score"></a>점수를 개선 하기 위한 조치 수행

개선 작업 탭에는 해당 테 넌 트에 적용할 수 있는 모든 보안 권장 사항 (완료 됨, 완료 되지 않음, 타사를 통해 확인 및 무시 됨)이 함께 표시 됩니다. 모든 컨트롤을 검색, 필터링 및 그룹화 할 수 있습니다.  순위는 두 가지 보안 가치를 평가 하 고 완료 하기 위한 노력을 기반으로 합니다.

Microsoft 보안 점수에 의해 [점수 없음] 레이블이 지정 된 작업은 추적 되지 않습니다. 계속 해 서 작업을 수행할 수는 있지만 작업이 완료 되 면 점수에 영향을 주지 않습니다. 향후 Microsoft 보안 점수에 따라 작업이 추적 되 고 이미 완료 된 경우 보안 점수가 자동으로 변경 됩니다.

향상 작업을 클릭 하면 플라이 아웃이 나타납니다. 이 작업을 완료 하려면 몇 가지 옵션을 사용할 수 있습니다.

1. **설정 보기** 를 선택 하 여 구성 화면으로 이동 하 고 변경을 수행 합니다. 그런 다음 바로 위로 이동 하 여 표시 되는 작업에 대 한 점수를 얻게 됩니다. 점수를 업데이트 하는 데 최대 24 시간이 걸릴 수 있습니다.

2. 타사 응용 프로그램 또는 소프트웨어에서 향상 된 기능을 이미 해결 했기 때문에 타사 **에서 문제 해결** 을 선택 합니다. 작업을 수행 하는 것이 가장 좋은 점수를 얻을 수 있으므로 보안 점수가 전체적인 보안 상태를 보다 잘 반영 합니다. 제 3 자가 더 이상 해당 컨트롤을 커버 하지 않으면 개선 작업을 완료 되지 않은 것으로 표시할 수 있습니다. 개선 작업을 제 3 자까지 해결 된 것으로 표시 한 경우 Microsoft는 점수 요구 사항이 충족 되었는지 여부를 볼 수 없습니다.

3. 위험을 수락 하 고 개선 작업을 규정 하지 않기로 결정 했으므로 **무시** 를 선택 합니다. 개선 작업을 무시 하면 최대 보안 점수 점수가 감소 합니다. 언제 든 지 기록에서이 작업을 보거나 실행 취소할 수 있습니다.

4. 향상 작업을 수행 하려면 환경의 일부를 정기적으로 검토 하 여 점수를 얻고 유지 해야 하므로 **검토** 를 선택 합니다. 예를 들어 사서함 전달 규칙을 매주 검토 하 여 데이터가 네트워크에서 노출 되었습니다 되 고 있지 않은지 확인 해야 합니다. 변경할 필요는 없지만 작업을 수행 해야 합니다. 정기적으로 규칙을 검토 하면 점수를 받게 됩니다. 그렇지 않으면 점수가 줄어들게 됩니다.

![M365 홈페이지](./media/secure-score/secure-score1x450.png) ![M365 홈페이지](./media/secure-score/secure-score2x450.png)

*그림 2 & 3: 개선 조치 flyouts*

## <a name="monitor-improvements-over-time"></a>시간에 따른 모니터 향상

**기록** 탭에서 시간에 따른 조직의 점수 그래프를 볼 수 있습니다. 이 보기에는 선택한 시간 범위 동안 수행 된 모든 작업과 함께 전역 average, 산업 average 및 이와 유사한 좌석 수가 포함 됩니다. 날짜 범위를 사용자 지정 하 고 범주별로 필터링 할 수도 있습니다.

점수는 하루에 한 번 계산 됩니다 (1:00 AM PST 기준). 측정 된 작업을 변경 하면 점수가 다음 날에 자동으로 업데이트 됩니다. 또한 일부 다른 포털에는 Microsoft 보안 점수 (예: Windows Defender 보안 센터)의 일부가 표시 된다는 점에 유의 해야 합니다. 개선 작업을 완료 하 고 해당 포털에서 점수가 증가 하는 경우 업데이트 된 점수가 Microsoft 365 보안 센터에 표시 되는 데 최대 24 시간이 걸릴 수 있습니다.  

## <a name="risk-awareness"></a>위험 인식

Microsoft 보안 점수는 시스템 구성, 사용자 동작 및 기타 보안 관련 측정값을 기반으로 한 보안 환경을 나타내는 수치 요약입니다. 시스템 또는 데이터를 얼마나 많이 침해 해야 하는지 절대 측정 한 것은 아닙니다. 대신 Microsoft 환경에서 보안 제어를 채택 하는 범위를 나타내므로 위반 위험을 상쇄 하는 데 도움이 될 수 있습니다. 보안 침해에의 한 온라인 서비스에는 전혀 문제가 되지 않으며 보안 점수가 보안상 침해에 대 한 보장으로 해석 되어서는 안 됩니다.

## <a name="we-want-to-hear-from-you"></a>사용자의 의견을 듣고 싶습니다.

문제가 있는 경우 [Security, 개인정보 보호 정책 & 준수](https://techcommunity.microsoft.com/t5/Security-Privacy-Compliance/bd-p/security_privacy) 커뮤니티에 게시를 통해 의견을 보내 주시기 바랍니다. 당사는 커뮤니티를 모니터링 하 고 도움이 될 것입니다.
