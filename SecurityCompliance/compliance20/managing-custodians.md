---
title: Advanced eDiscovery에서 custodians을 사용 하 여 작업
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
description: 고급 eDiscovery의 custodian 관리 도구를 사용 하면 법적 사례에 관심이 있는 사용자와 연결 된 데이터를 식별, 보존 및 수집 하는 방법에 대 한 워크플로를 관리할 수 있습니다.
ms.openlocfilehash: 6e365f0b7f80a0a5caa050b2e0b08c94dbed4746
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/17/2019
ms.locfileid: "34151600"
---
# <a name="work-with-custodians-in-advanced-ediscovery"></a>Advanced eDiscovery에서 custodians을 사용 하 여 작업

조직이 법적 조사에 응답 하는 경우 관련 된 콘텐츠를 식별, 보존 및 수집 하는 워크플로는 관련 데이터를 custodians 조직의 구성원을 기반으로 합니다. EDiscovery에서는 이러한 개인을 *data custodians* (또는 *custodians*) 라고 하며 "문서 또는 전자 파일의 관리 권한을 가진 사람"으로 정의 됩니다. 예를 들어 전자 메일 메시지의 custodian는 관련 메시지를 포함 하는 사서함의 소유자가 될 수 있습니다.  

조사가 시작 되 면 eDiscovery 팀은 사례와 관련 된 모든 관련 custodians 및 데이터 원본을 빠르게 식별 해야 합니다. 시간이 지남에 따라 custodians 및 해당 데이터 원본 목록이 늘어나거나 decreasse 될 수 있습니다. 따라서 조직은 사례 수명 주기 동안 custodial 콘텐츠를 식별, 보존 및 수집 하는 제어 된 프로세스를 유지 관리 해야 합니다.

고급 eDiscovery 사례에서는 법률 팀이 조직의 개인을 custodians으로 추가 하 고 Exchange 사서함, OneDrive 계정, SharePoint 및 팀 사이트 등의 custodial 데이터 원본을 자동으로 식별 하 고 보존할 수 있습니다. 고급 eDiscovery의 기본 제공 custodian 관리 도구를 사용 하면 조직에서 실수로 또는 고의로 삭제 된 정보를 전자적으로 저장 하 여 보호할 수 있습니다. 이를 통해 적절 한 보존 프로세스를 수동으로 수행 해야 하는 시간이 걸리고 오류가 발생 하기 쉬운 프로세스를 제거할 수 있습니다. 

Custodians 사용에 대 한 자세한 내용은 다음 항목을 참조 하십시오. 

- [보유자를 사례에 추가](add-custodians-to-case.md)

- [사례에서 custodians 관리](manage-new-custodians.md)

- [보유자 활동 보기](view-custodian-activity.md)

## <a name="advanced-ediscovery-permissions"></a>고급 eDiscovery 권한

고급 eDiscovery에서 기본 제공 eDiscovery 관리자 역할 그룹을 사용 하 여 올바른 investigators에 필요한 사용 권한을 할당할 수 있으므로 고급 eDiscovery에서 종단 간 워크플로를 관리할 수 있습니다. 또는 고급 eDiscovery에서 특정 작업을 수행 하는 데 필요한 역할의 하위 집합을 사용 하 여 사용자 지정 역할 그룹을 만들 수 있습니다. EDiscovery 관련 역할에 대 한 자세한 내용은 [Security _AMP_ 준수 센터에서 ediscovery 사용 권한 할당](../assign-ediscovery-permissions.md)을 참조 하십시오.
