---
title: Office 365 Advanced eDiscovery의 문서 유사성 이해
ms.author: chrfox
author: chrfox
manager: laurawi
ms.date: 9/14/2017
ms.audience: Admin
ms.topic: conceptual
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: 4d4cb381-4c9a-4165-a455-609d525c7a88
description: '문서 유사성 값을 검토 하 고 거의 중복으로 간주 되는 두 파일의 최소 resemblance 수준이 Office 365 Advanced eDiscovery에서 작동 합니다. '
ms.openlocfilehash: eb8f07ceedb10bd0152693dd1e82a28797d86a5a
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32264156"
---
# <a name="understand-document-similarity-in-office-365-advanced-ediscovery"></a>Office 365 Advanced eDiscovery의 문서 유사성 이해

> [!NOTE]
> Advanced eDiscovery를 사용하려면 Office 365 E3의 고급 준수 추가 기능이나 조직을 위한 E5 구독이 필요합니다. 이 요금제가 없는 상태에서 Advanced eDiscovery를 사용하려는 경우에는 [Office 365 Enterprise E5 평가판을 등록](https://go.microsoft.com/fwlink/p/?LinkID=698279)할 수 있습니다. 
  
Advanced eDiscovery에서 문서 유사성은 두 문서를 중복 항목으로 간주 하는 데 필요한 최소 resemblance 수준입니다.
  
> [!TIP]
> 대부분의 비즈니스 응용 프로그램에서는 유사도 값 60%-75%를 사용 하는 것이 좋습니다. 아주 불량 OCR (광학 인식) 재질의 경우 낮은 유사도 값을 적용할 수 있습니다. 
  
> [!NOTE]
> 지정한 사례를 설정 하 고 실행 한 후에는 유사성 값을 변경할 수 없습니다. 
  
유사 중복 (ND) 집합 내에서 유사성 임계값 아래에 resemblance 수준이 있는 문서가 있을 수 있습니다. 문서에서 nd 집합에 가입 하려면 resemblance 수준이 유사도를 초과 하는 nd 집합에 하나 이상의 문서가 있어야 합니다. 
  
예를 들어 유사도가 80%로 설정 되어 있고 문서 F1이 85%에 있는 문서와 유사 하 게, 문서 f2는 문서 F3과 같은 수준의 90%로 되어 있다고 가정 합니다. 
  
그러나 document F1은 문서 F3와 비슷한 수준으로, 임계값 보다 낮은 70%만 사용할 수 있습니다. 그러나이 예에서 문서 F1, F2 및 F3 모두 하나의 ND 집합에 표시 됩니다. 마찬가지로, 유사도 값을 80%로 설정 하면-1과 EquiSet-2 EquiSet 두 개의 집합을 만들 수 있습니다. EquiSet-1에는 E1 및 E2 문서가 포함 되어 있습니다. Equiset-2에는 문서 (f1, F2 및 F3가 포함 됩니다. 
  
resemblance의 수준은 다음과 같이 표시 됩니다.
  
![문서 유사성](media/3907ea7d-e28a-4027-8fc3-be090dd39144.gif)
  
이제 다른 문서인 X1이 삽입 되었다고 가정 합니다. X1과 E3 사이의 resemblance은 87%입니다. 마찬가지로 X1과 F1 사이의 resemblance은 92%입니다. 따라서 이제 EquiSet-1, EquiSet-2 및 X1이 하나의 ND 집합으로 결합 됩니다.
  
![문서 유사성](media/d140d347-33d5-475a-af04-594a0f2ab13d.gif)
  
> [!NOTE]
> 한 nd 집합에 두 문서가 할당 되 면 해당 집합에 추가 문서가 추가 되거나 집합이 병합 되는 경우에도 동일한 nd 집합에 함께 유지 됩니다. 
  
집합이 병합 된 후에는 새 문서가 집합에 추가 될 때 피벗 문서가 변경 될 수 있습니다. 
  
## <a name="see-also"></a>참고 항목

[Office 365 Advanced eDiscovery](office-365-advanced-ediscovery.md)
  
[분석 옵션 설정](set-analyze-options-in-advanced-ediscovery.md)
  
[무시 텍스트 설정](set-ignore-text-in-advanced-ediscovery.md)
  
[고급 설정 분석 설정](set-analyze-advanced-settings-in-advanced-ediscovery.md)
  
[분석 결과 보기](view-analyze-results-in-advanced-ediscovery.md)

