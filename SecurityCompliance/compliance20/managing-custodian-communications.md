---
title: 고급 eDiscovery (미리 보기)의 통신 사용 (영문)
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection: ''
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: ''
ms.openlocfilehash: b27d6cca0382b18123cae4106f77ce0dcdf5e525
ms.sourcegitcommit: ee28ee2b2bdfd049333c2f495d7f7780d13af4a6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2019
ms.locfileid: "29608181"
---
# <a name="working-with-communications-in-advanced-ediscovery-preview"></a>고급 eDiscovery (미리 보기)의 통신 사용 (영문)

고급 eDiscovery (미리 보기) 추적 및 법적 보유 알림 배포를 중심으로 한 프로세스를 단순화 하기 위해 법률 부서 수 있습니다. 더불어 통신 기능을 사용 하면 법률 부서를 관리 하 고 알림, 미리 알림, 고 한곳에서 모든 에스컬레이션-에서 조직의 전체 법적 보유 프로세스-를 자동화 합니다.

## <a name="what-is-a-legal-hold-notification"></a>법적 보유 알림 이란?

법적 보유 (로 알려져는 *소송 보존*) 통지는 직원, 파견 직원 또는 기타 데이터 custodians 조직의 법률 부서에서 보내는 알림입니다. 이러한 알림을 활성 또는 임박한 법적 문제 관련 될 수 있는 모든 자료를 비롯 하 여 전자적으로 저장 된 정보 (ESI)으로 유지 하기 위해 custodians에 지시 합니다. 법적 팀은 각 더불어가 수신 하 고 이해 하 고을 읽고 동의 지정 된 지침을 준수 하 알고 있어야 합니다.

## <a name="the-legal-hold-notification-process"></a>법률 알림 프로세스를 유지

조직에는 임박한 소송 또는 규정 조사 하는 방법에 대 한 학습 하는 경우 관련 정보를 유지 하기 위해 의무 있습니다. 해당 보존 요구 사항을 준수를 위해 조직 즉시 알려야 잠재적인 custodians 관련 정보를 유지 하기 위해 업무에 대 한 합니다. 

고급 eDiscovery (미리 보기)와 팀이 법적 만들고 자신의 법적 보유 알림 워크플로 사용자 지정할 수 있습니다. 더불어 통신 기능을 사용 하는 다음과 같은 통지 및 워크플로 구성 하려면 법적 팀:

1. **발급 주의**: 법적 보유 통지는 발급 (또는 시작)은 법률 부서에서 사례 문제에 대 한 관련 정보를 가진 custodians에 대 한 알림을 합니다. 이 공지 검색을 위해 필요할 수 있는 모든 정보를 유지 하기 위해 해당 custodians에 지시 합니다. 
   
2.  **다시 발급 확인**: 추가 유지 하기 위해 필요한 수 custodians 사례를 하는 동안 또는 보다 작으면 정보를 이전에 지시 합니다. 이 시나리오에 대 한 기존 보류 통지를 업데이트할 수 있으며 다시 대화 custodians를 발급할 수 있습니다.

3.  **릴리스 알 수**: 정보는 더이상 그대로 유지 하는 경우가 필요 하지 않은 되도록 더불어를 해제 해야하는 문제를 해결 한 후 더불어 더이상 보존 의무에 따라 달라 집니다. 또한 대화 더불어 알림을 받게 됩니다 보존 의무 아래 및 해당 작업을 다시 시작 하는 방법에 뛰어난 지침과 함께 더 이상.

4. **미리 알림 및 에스컬레이션**: 일부 경우에 알림을 발행 충분 하지 않습니다 법적 개시 요구를 충족 합니다. 각 알림 법적 팀 응답 하지 않는 custodians 함께 자동으로 추가 작업을 미리 알림 및 에스컬레이션 워크플로 집합을 예약할 수 있습니다.

    - **미리 알림**: 법적 보유 통지 발급 되었거나 다시 custodians 집합에 대 한 후 조직 설정 했을 수 미리 응답 하지 않는 custodians 경고 하도록 합니다. 

    - **에스컬레이션**: 경우에 따라 프로그램 더불어 미리 알림, 집합을 한 후에 응답 하지 않는 유지 되도록 하는 경우 법률 팀을 설정할 수 있습니다는 에스컬레이션 워크플로를 더불어 및 님이 자신의 관리자에 게 알려야 합니다.

## <a name="role-groups-and-permissions"></a>역할 그룹 및 사용 권한 

법적 팀을 제어 하 고 보안 & 준수 센터의에서 eDiscovery 관련 된 역할 그룹 및 사용 권한을 사용 하 여 사례 작업과 세그먼트 수 있습니다. 

만들고 법적 보유 알림 관리 하려면 사용자 역할 그룹의 일부 이어야 합니다.

- **eDiscovery 관리자** -이 역할 그룹의 구성원 만들고 eDiscovery 사례를 관리할 수 있습니다. 추가 하 고 구성원을 제거, custodians를 배치할 수 및 콘텐츠 위치에 유지, 법적 보유 알림 관리, 사례와 연결 된 콘텐츠 검색, 콘텐츠 검색 결과 내보내기 하 고 편집할 고급에서 분석을 위해 검색 결과 준비 eDiscovery (미리 보기)입니다. 이 역할 그룹에 두 하위 그룹이 있습니다. 이러한 하위 그룹 간의 차이 범위를 기반으로 합니다.

  - **eDiscovery 관리자** -볼 수 있으며를 만들거나의 구성원 이어야 하는 eDiscovery 사례를 관리할 수 있습니다. 다른 eDiscovery 관리자 사례를 만듭니다. 하 고 해당 사례의 구성원으로 두번째 eDiscovery 관리자를 추가 하지는 않습니다를 두번째 eDiscovery 관리자를 보거나 보안 & 준수 센터의에서 eDiscovery 페이지에서 대/소문자를 열 수 없습니다. eDiscovery 관리자 고급 ediscovery (미리 보기) 분석 작업을 수행 하는 경우에 액세스할 수도 있습니다.

  - **eDiscovery 관리자** -eDiscovery 관리자 작업을 수행할 수 있는 모든 사례 관리 작업을 수행할 수 있습니다. 또한 eDiscovery 관리자가 다음과 같은 작업을 수행할 수 있습니다.
    
    - eDiscovery 페이지에 나열된 모든 사례를 봅니다.
    - 자신 대/소문자의 구성원으로 추가 후에 조직에서 모든 경우를 관리 합니다.
    - 조직에서 모든 사례에 대 한 고급 eDiscovery (Preview)의 경우 데이터를 액세스 합니다.

자세한 내용은 [Office 365 보안 & 준수 센터의에서 eDiscovery 사용 권한 할당](../assign-ediscovery-permissions.md)을 참조 하십시오.