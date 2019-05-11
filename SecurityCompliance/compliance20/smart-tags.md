---
title: 고급 eDiscovery에서 변호사에 대 한 스마트 태그 설정-클라이언트 권한 검색
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
ROBOTS: NOINDEX, NOFOLLOW
description: ''
ms.openlocfilehash: 721426f23aec862bcefbd13b8e61415dac3aeb27
ms.sourcegitcommit: aa8ea45d5854f8906714e0a407937585ec7993ad
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/10/2019
ms.locfileid: "33951705"
---
# <a name="set-up-smart-tags-for-ml-assisted-review-in-advanced-ediscovery"></a>고급 eDiscovery에서 ML 지원 검토를 위한 스마트 태그 설정

Advanced eDiscovery의 기계 학습 기능은 문서에 대 한 의사 결정 프로세스를 보다 효율적으로 수행 하는 데 도움이 됩니다. 스마트 태그는 결정 내용이 기록 되는 위치 (태그 및 태그 그룹)로 컴퓨터 학습 기능을 가져오는 방법입니다. 스마트 태그 그룹을 만들 때 그룹에 매핑된 ML 모델에 대 한 결정 내용은 그룹의 태그와 함께 줄에 표시 되며,이를 통해 온라인으로 컨텍스트 되는 정보를 확인할 수 있습니다.

## <a name="how-to-set-up-a-smart-tag-group"></a>스마트 태그 그룹을 설정 하는 방법

1. 검토 집합에서 **검토 설정** -> 관리**태그**관리로 이동 합니다.

2. **태그 그룹 추가** 옆에 있는 드롭다운을 클릭 하 고 **스마트 태그 그룹 추가**를 선택 합니다.

3. 이 그룹에 매핑할 모델을 선택 합니다. 이렇게 하면 태그 구역과 N 개의 하위 태그가 생성 되며 여기에서 N은 모델의 가능한 출력 수입니다. 예를 들어, 변호사-클라이언트 권한 감지 모델에는 두 가지 가능한 출력이 있고 권한이 부여 되지 않음이 있습니다. 이 모델을 선택 하면 검토 집합에 두 개의 하위 태그가 생성 되며 각각 가능한 출력 중 하나에 해당 됩니다.

4. 표시 되는 대로 태그 그룹 및 태그의 이름을 바꿉니다.

## <a name="how-to-use-a-smart-tag-group"></a>스마트 태그 그룹을 사용 하는 방법

문서를 검토할 때 모델의 결과가 해당 태그 값 옆에 표시 됩니다. 예를 들어, 변호사-클라이언트 권한 검색을 위한 스마트 태그 그룹을 사용 하 고 모델이 결정 한 문서를 검토 하면 해당 태그 옆에 해당 하는 이유가 표시 됩니다. 이 태그는 자동으로 적용 되지 않습니다. 모든 목적에 따라 스마트 태그 그룹 내의 태그는 적절 한 경우 모델 결과를 표시 하는 것을 제외 하 고는 일반 태그와 동일 하 게 작동 합니다.