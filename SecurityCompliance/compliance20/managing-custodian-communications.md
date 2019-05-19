---
title: Advanced eDiscovery에서 통신 사용
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: 고급 eDiscovery를 사용 하면 법적 조사에 custodians 알리는 법적 보존 알림 워크플로를 쉽게 관리할 수 있습니다.
ms.openlocfilehash: cf5c8f5e932993255bda2cb959657c2c6ded3163
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/17/2019
ms.locfileid: "34154910"
---
# <a name="work-with-communications-in-advanced-ediscovery"></a>Advanced eDiscovery에서 통신 사용

고급 eDiscovery를 사용 하면 법적 부서에서 법적 보존 알림을 추적 및 배포 하기 위한 프로세스를 단순화할 수 있습니다. Custodian communications tool을 사용 하면 법무 부서가 전체 법적 프로세스, 초기 알림, 미리 알림 및 에스컬레이션을 모두 한 곳에 관리 및 자동화할 수 있습니다.

## <a name="what-is-a-legal-hold-notification"></a>법적 보존 알림 이란?

법적 보존 ( *소송 보존*이 라고도 함)은 조직의 법률 부서에서 법적 조사와 관련이 있을 수 있는 직원, 불확정 직원 또는 custodians에 게 전송 되는 알림입니다. 이러한 알림은 활성 또는 임박한 법적 정보와 관련이 있을 수 있는 모든 콘텐츠 뿐만 아니라 전자적으로 저장 된 정보를 보존 하도록 custodians에 게 지시 합니다. 법률 팀에서는 각 custodian가 제공 된 지침을 준수 하 고, 읽고, 이해 하 고 동의한 것으로 확인 해야 합니다.

## <a name="the-legal-hold-notification-process"></a>법적 보존 알림 프로세스

조직은 임박한 소송 또는 규제 조사에 대해 학습 하는 경우 관련 정보를 보존 하는 업무를 담당 합니다. 조사에 대 한 보존 요구 사항을 준수 하기 위해 조직은 적절 한 정보를 보존 하기 위한 업무에 대 한 잠재적 custodians을 즉시 알려야 합니다.

고급 eDiscovery를 사용 하는 경우 법률 팀은 법적 보존 알림 워크플로를 만들고 사용자 지정할 수 있습니다. Custodian communications tool을 사용 하면 합법적인 팀이 다음과 같은 공지와 워크플로를 구성할 수 있습니다.

1. **발급 알림**: 법적 고 지 사항에 대 한 관련 정보를 확인할 수 있는 custodians에 법적 부서의 알림으로 법률 보존 알림을 발급 (또는 시작) 합니다. 이 알림 메시지는 검색에 필요한 모든 정보를 보존 하도록 custodians에 지시 합니다.
   
2.  **재발급 통지**: 예를 들어 custodians는 이전에 요청한 것 보다 더 많은 콘텐츠 (또는 더 적은 콘텐츠)를 보존 해야 할 수 있습니다. 이 시나리오에서는 기존 보존 통지를 업데이트 하 고 custodians에 다시 발행할 수 있습니다.

3.  **릴리스 알림**: 문제가 해결 되 고 custodian가 보존 요구 사항에 더 이상 적용 되지 않으면 사례에서 custodian를 해제할 수 있습니다. 또한 콘텐츠를 보존 하는 데 더 이상 필요 하지 않음을 custodian에 게 알릴 수 있으며, 데이터와 관련 하 여 일반적인 작업 활동을 다시 시작 하는 방법에 대 한 지침을 제공 합니다.

4. **미리 알림 및 에스컬레이션**: 일부 인스턴스에서는 알림을 발급 하는 것 만으로는 법적 검색 요구 사항을 충족 하기에 충분 하지 않습니다. 각 알림을 사용 하는 경우 법률 팀은 미리 알림 및 에스컬레이션 워크플로 집합에서 응답 하지 않는 custodians 자동으로 추가 작업을 예약할 수 있습니다.

    - **미리 알림**: 법적 보존 알림을 발급 하거나 custodians 집합으로 다시 발급 한 후 조직에서 응답 하지 않는 custodians 알림을 보내도록 미리 알림을 설정할 수 있습니다.

    - **에스컬레이션**: 일정 기간 동안 미리 알림 집합에도 불구 하 고 custodian 응답 하지 않는 경우 법률 팀은 응답성이 없는 워크플로를 설정 하 여 응답 하지 않는 custodians 및 관리자에 게 알릴 수 있습니다.

## <a name="role-groups-and-permissions"></a>역할 그룹 및 사용 권한 

법률 팀은 보안 & 준수 센터에서 eDiscovery 관련 역할 그룹 및 사용 권한을 사용 하 여 서비스 케이스 활동을 제어 하 고 분리할 수 있습니다. 

법적 보존 알림을 만들고 관리 하려면 사용자가 다음 역할 그룹에 속해 있어야 합니다.

- **Ediscovery 관리자** -이 역할 그룹의 구성원은 ediscovery 사례를 만들고 관리할 수 있습니다. 구성원을 추가 및 제거 하 고, custodians 및 콘텐츠 위치를 보류 하 고, 법률 보존 알림을 관리 하 고, 사례와 연결 된 콘텐츠 검색을 만들고 편집 하 고, 콘텐츠 검색 결과를 내보내고, 고급 분석을 위한 검색 결과를 준비할 수 있습니다. eDiscovery. 이 역할 그룹에 두 개의 하위 그룹이 있습니다. 이러한 하위 그룹 간의 차이는 범위를 기준으로 합니다.

  - **Ediscovery 관리자** -자신이 만들거나 구성원 인 ediscovery 사례를 보고 관리할 수 있습니다. 다른 eDiscovery 관리자가 사례를 만들었지만 두 번째 eDiscovery 관리자를 해당 사례 구성원으로 추가 하지 않는 경우 두 번째 eDiscovery 관리자가 Security & 준수 센터의 eDiscovery 페이지에서 사례를 보거나 열 수 없습니다. eDiscovery 관리자는 고급 eDiscovery의 사례에 액세스 하 여 분석 작업을 수행할 수도 있습니다.

  - **Ediscovery 관리자** -ediscovery 관리자가 수행할 수 있는 모든 사례 관리 작업을 수행할 수 있습니다. 또한 eDiscovery 관리자(Administrator)는 다음과 같은 작업을 수행할 수 있습니다.
    
    - eDiscovery 페이지에 나열된 모든 사례를 봅니다.
    - 조직의 대/소문자를 구성원으로 추가한 후 조직에서 모든 사례를 관리 합니다.
    - 조직의 모든 경우에 대 한 고급 eDiscovery의 사례 데이터 액세스

자세한 내용은 [Security _AMP_ 준수 센터에서 eDiscovery 사용 권한 할당](../assign-ediscovery-permissions.md)을 참조 하십시오.