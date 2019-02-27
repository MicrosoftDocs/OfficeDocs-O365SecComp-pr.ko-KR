---
title: Advanced eDiscovery (미리 보기)에서 통신에 대 한 작업
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: ''
ms.openlocfilehash: 916691e1f2470ef9e9e54d9dfe06c5277a92ba53
ms.sourcegitcommit: baf23be44f1ed5abbf84f140b5ffa64fce605478
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/26/2019
ms.locfileid: "30296091"
---
# <a name="work-with-communications-in-advanced-ediscovery-preview"></a>Advanced eDiscovery (미리 보기)에서 통신에 대 한 작업

고급 eDiscovery (미리 보기)를 통해 법적 부서에서 법적 보존 알림을 추적 및 배포 하는 프로세스를 단순화할 수 있습니다. custodian communications 기능을 사용 하면 합법적 부서가 알림, 미리 알림 및 에스컬레이션--모두를 한 곳에서 관리 및 자동화할 수 있습니다.

## <a name="what-is-a-legal-hold-notification"></a>법적 보존 알림 이란?

법적 보존 ( *소송 보존*이 라고도 함)은 조직의 법률 부서에서 직원, 불확정 직원 또는 기타 데이터 custodians 전송 하는 알림입니다. 이러한 알림은 활성 또는 임박한 법적 정보와 관련이 있을 수 있는 모든 자료 뿐 아니라 전자 저장 된 정보 (ESI)를 보존 하도록 custodians에 지시 합니다. 법률 팀에서는 각 custodian가 해당 지침을 받고, 읽고, 이해 하 고 동의한 것으로 인식 해야 합니다.

## <a name="the-legal-hold-notification-process"></a>법적 보존 알림 프로세스

조직은 임박한 소송 또는 규제 조사에 대해 학습 하는 경우 관련 정보를 보존 하는 업무를 담당 합니다. 보존 요구 사항을 준수 하기 위해 조직은 관련 정보를 보존 하기 위해 잠재적 custodians에 대해 즉시 알려야 합니다. 

고급 eDiscovery (미리 보기)를 사용 하는 경우 법률 팀은 법적 보존 알림 워크플로를 만들고 사용자 지정할 수 있습니다. Custodian Communications 기능을 사용 하면 법적 팀이 다음과 같은 공지와 워크플로를 구성할 수 있습니다.

1. **발급 알림**: 법적 고 지 사항에 대 한 관련 정보가 있을 수 있는 custodians에 법적 부서의 알림으로 법률 보존 알림을 발급 (또는 시작) 합니다. 이 내용은 검색에 필요한 모든 정보를 보존 하기 위해 이러한 custodians에 게 지시 합니다. 
   
2.  **다시 발급 통지**: 경우에 따라 이전에 지시 된 것 보다 더 많은 정보를 보존 해야 할 수도 있습니다. 이 시나리오에서는 기존 보존 통지를 업데이트 하 고 custodians에 다시 발행할 수 있습니다.

3.  **릴리스 알림**: 문제가 해결 되 고 custodian가 보존 작업에 더 이상 적용 되지 않는 경우에는 필요 하지 않은 경우 정보가 더 이상 보존 되지 않도록 custodian을 해제할 수 있습니다. 또한 custodian에는 더 이상 보존 업무에 미치지 않으며 활동을 다시 시작 하는 방법에 대 한 자세한 지침을 제공 합니다.

4. **미리 알림 및 에스컬레이션**: 일부 인스턴스에서는 알림을 발급 하는 것 만으로는 법적 검색 요구 사항을 충족 하지 못할 수 있습니다. 각 알림을 사용 하는 경우 법률 팀은 미리 알림 및 에스컬레이션 워크플로 집합에서 응답 하지 않는 custodians 자동으로 추가 작업을 예약할 수 있습니다.

    - **미리 알림**: 법적 보존 알림을 발급 하거나 custodians 집합으로 다시 발급 한 후 조직에서 응답 하지 않는 custodians 알림을 보내도록 미리 알림을 설정할 수 있습니다. 

    - **에스컬레이션**: custodian 미리 알림 집합 에서도 여전히 응답 하지 않는 경우 법적 팀은 custodian 및 해당 관리자에 게 알릴 단계적 워크플로를 설정할 수 있습니다.

## <a name="role-groups-and-permissions"></a>역할 그룹 및 사용 권한 

법률 팀은 보안 & 준수 센터에서 eDiscovery 관련 역할 그룹 및 사용 권한을 사용 하 여 사례 활동을 제어 하 고 분리할 수 있습니다. 

법적 보존 알림을 만들고 관리 하려면 사용자가 다음 역할 그룹에 속해 있어야 합니다.

- **ediscovery 관리자** -이 역할 그룹의 구성원은 ediscovery 사례를 만들고 관리할 수 있습니다. 구성원을 추가 및 제거 하 고, custodians 및 콘텐츠 위치를 보류 하 고, 법률 보존 알림을 관리 하 고, 사례와 연결 된 콘텐츠 검색을 만들고 편집 하 고, 콘텐츠 검색 결과를 내보내고, 고급 분석을 위한 검색 결과를 준비할 수 있습니다. eDiscovery (미리 보기) 이 역할 그룹에는 두 개의 하위 그룹이 있습니다. 이러한 하위 그룹의 차이점은 범위를 기반으로 합니다.

  - **ediscovery 관리자** -자신이 만들거나 구성원 인 ediscovery 사례를 보고 관리할 수 있습니다. 다른 ediscovery 관리자가 사례를 만들었지만 두 번째 ediscovery 관리자를 해당 사례 구성원으로 추가 하지 않는 경우 두 번째 ediscovery 관리자가 Security & 준수 센터의 ediscovery 페이지에서 사례를 보거나 열 수 없습니다. eDiscovery 관리자는 고급 eDiscovery (미리 보기)에서 해당 사례에 액세스 하 여 분석 작업을 수행할 수도 있습니다.

  - **ediscovery 관리자** -ediscovery 관리자가 수행할 수 있는 모든 사례 관리 작업을 수행할 수 있습니다. 또한 eDiscovery 관리자는 다음 작업을 수행할 수 있습니다.
    
    - eDiscovery 페이지에 나열된 모든 사례를 봅니다.
    - 조직의 대/소문자를 구성원으로 추가한 후 조직에서 모든 사례를 관리 합니다.
    - 조직의 모든 경우에 대해 Advanced eDiscovery (Preview)의 사례 데이터에 액세스 합니다.

자세한 내용은 [Office 365 Security & 준수 센터에서 eDiscovery 사용 권한 할당](../assign-ediscovery-permissions.md)을 참조 하십시오.