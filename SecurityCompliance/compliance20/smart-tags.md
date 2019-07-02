---
title: 고급 eDiscovery에서 스마트 태그 설정
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
ROBOTS: NOINDEX, NOFOLLOW
description: 스마트 태그를 사용 하면 고급 eDiscovery 사례에서 콘텐츠를 검토할 때 기계 학습 기능을 적용할 수 있습니다. 스마트 태그 그룹을 사용 하 여 변호사-클라이언트 권한 모델과 같은 기계 학습 검색 모델의 결과를 표시 합니다.
ms.openlocfilehash: 68b558cc2282cc388387f8d61825b9ee569ff32a
ms.sourcegitcommit: e323610df2df71c84f536e8a38650d33d8069e41
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/04/2019
ms.locfileid: "34703831"
---
# <a name="set-up-smart-tags-in-advanced-ediscovery"></a>고급 eDiscovery에서 스마트 태그 설정

고급 eDiscovery의 ML (기계 학습) 기능은 검토 집합에서 사례 문서를 검토할 때 보다 효율적으로 결정 프로세스를 만드는 데 도움이 될 수 있습니다. 스마트 태그는 검토 중에 문서에 태그를 지정할 때 결정 내용이 기록 되는 위치에 대 한 ML 기능을 가져오는 방법입니다. 스마트 태그 그룹을 만들 때 스마트 태그 그룹과 연결 된 ML 모델의 결과가 태그 그룹의 태그와 함께 줄에 표시 되는 결정 사항을 결정할 수 있습니다. 이렇게 하면 특정 문서를 검토할 때 행에서 ML 결과 정보를 볼 수 있습니다.

## <a name="how-to-set-up-a-smart-tag-group"></a>스마트 태그 그룹을 설정 하는 방법

1. 검토 집합에서 **검토 설정 관리** 를 클릭 한 다음 **태그 관리**를 클릭 합니다.

2. **태그 그룹 추가** 를 클릭 한 다음 **스마트 태그 그룹 추가**를 선택 합니다.

3. 태그 그룹에 연결 하려는 ML 모델을 선택 합니다.
    
   이렇게 하면 태그 그룹 및 *n* 개의 하위 태그가 생성 되며 여기에서 *n* 은 모델의 가능한 출력 수입니다. 예를 들어, [변호사-클라이언트 권한 검색 모델](attorney-privilege-detection.md) 에는 다음과 같은 두 가지 가능한 출력이 있습니다. 

   - **긍정** -변호사 클라이언트의 권한 있는 콘텐츠가 포함 된 문서에 태그를 추가할 때 사용 합니다.
   
   - **음수** -변호사 클라이언트의 권한 있는 콘텐츠가 포함 되지 않은 문서에 태그를 표시 하는 데 사용 됩니다.
    
    이 모델을 선택 하면 검토 집합에 대해 하위 태그가 두 개 있는 태그 그룹 ( **양수** 와 이름이 각각 **음수**라는 하위 태그)이 만들어집니다. 이 예에서 각 하위 태그는 변호사 클라이언트 권한 검색 모델의 가능한 출력 중 하나에 해당 합니다.

4. 원하는 경우 태그 그룹 및 자식 태그의 이름을 바꿀 수 있습니다. 예를 들어 **양수** 태그의 이름을 **특권** 으로 바꾸고 **음수** 태그를 **권한이 없는**이름으로 바꿀 수 있습니다.

## <a name="how-to-use-smart-tags"></a>스마트 태그 사용 방법

문서를 검토 하면 해당 자식 태그 옆에 모델의 결과가 표시 됩니다. 예를 들어 변호사-클라이언트 권한 검색을 위한 스마트 태그 그룹이 있고 잠재적으로 권한이 부여 된 문서를 검토 하는 경우 해당 결론에 대 한 이유가 해당 태그 옆에 표시 됩니다. 태그가 문서에 자동으로 적용 되지 않는다는 점에 유의 해야 합니다. 검토자가 문서에 태그를 설정 하는 방법을 결정 합니다.