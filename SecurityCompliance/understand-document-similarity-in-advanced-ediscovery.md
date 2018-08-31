---
title: Office 365 Advanced eDiscovery의 문서 유사성 이해
ms.author: chrfox
author: chrfox
manager: laurawi
ms.date: 9/14/2017
ms.audience: Admin
ms.topic: conceptual
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: 4d4cb381-4c9a-4165-a455-609d525c7a88
description: 'Office 365 고급 eDiscovery에서 문서 다음과 비슷한 값, 최소 수준의 중복 근처 것으로 간주 하는 두 파일에 대 한와 작동 하는 방법을 검토 합니다. '
ms.openlocfilehash: 39cd8c31204f0164f6b52c71fa707253cb22758a
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22533328"
---
# <a name="understand-document-similarity-in-office-365-advanced-ediscovery"></a>Office 365 Advanced eDiscovery의 문서 유사성 이해

> [!NOTE]
> 고급 eDiscovery 조직에 대 한 고급 준수 추가 기능 또는 e 5 구독은 Office 365 E3 필요합니다. 해당 요금제에 가입한 상태 고급 eDiscovery 시도 하려는 하지 경우에 [Office 365 Enterprise e 5의 평가판 등록](https://go.microsoft.com/fwlink/p/?LinkID=698279)할 수 있습니다. 
  
고급 eDiscovery 문서 다음과 비슷한에는 거의 중복 된 것으로 간주 하는 두 문서에 필요한와의 최소 수준입니다.
  
> [!TIP]
> 대부분의 비즈니스 응용 프로그램에 대 한 다음과 비슷한 값의 60%-75%를 사용 하는 것이 좋습니다. 매우 불량 품질 광학 문자 인식 (OCR) 자료에 대 한 더 낮은 다음과 비슷한 값을 적용할 수 있습니다. 
  
> [!NOTE]
> 것에 설정 하 여 지정 된 경우에 대 한 실행 후에 다음과 비슷한 값을 변경할 수 없습니다. 
  
Near 중복 된 (ND) 집합 내에서 다음과 비슷한 임계값 아래와 수준 사용 하는 문서 수 있습니다. ND 집합에 참가 하는 문서에 대 한 초과 하는 다음과 비슷한와 수준으로 설정 하는 ND에서 하나 이상의 문서 이어야 합니다. 
  
예는 다음과 비슷한 80%로 설정 됨, 문서 F1 유사한 85%의 수준에서 F2 문서 및 문서 F2 유사한 F3 90%의 수준에서 문서를 가정 합니다. 
  
그러나 문서 F1 임계값 아래에 있는 70%만의 수준에서 문서 F3 유사할 수 있습니다. 그럼에도 불구 하 고이 예제에서는 문서 F1, F2 및 f 3을 하나의 ND에 표시 하는 모든 설정 합니다. 마찬가지로, 다음과 비슷한 값이 80%를 사용 하는 만들었을 수 두 집합, EquiSet-1과 EquiSet 2. EquiSet 1 E1 및 E2 문서를 포함합니다. Equiset 2 F1, F2 및 F3 문서를 포함합니다. 
  
와의 수준은 다음과 같이 나와 있습니다.
  
![문서 유사성](media/3907ea7d-e28a-4027-8fc3-be090dd39144.gif)
  
다른 문서, X1, 이제 삽입 되는 것으로 가정 합니다. X1 및 E3 간의 87%입니다. 마찬가지로, X1 및 F1 간의 92%입니다. 결과적으로, EquiSet-1,-2 주, EquiSet 및 X1는 이제으로 결합 한 nd 등을 설정 합니다.
  
![문서 유사성](media/d140d347-33d5-475a-af04-594a0f2ab13d.gif)
  
> [!NOTE]
> 두 문서에는 집합은 병합 하는 경우 또는 하나의 ND 집합에 할당 된 동일한 ND 집합 함께 유지 됩니다, 추가 하는 경우에 문서 집합에 추가 됩니다 경우. 
  
집합 병합 된 후 새 문서 집합에 추가 되 면 피벗 문서 변경할 수 있습니다. 
  
## <a name="see-also"></a>참고 항목

[Office 365 Advanced eDiscovery](office-365-advanced-ediscovery.md)
  
[분석 옵션 설정](set-analyze-options-in-advanced-ediscovery.md)
  
[텍스트를 무시 하는 설정](set-ignore-text-in-advanced-ediscovery.md)
  
[고급 설정 설정 분석](set-analyze-advanced-settings-in-advanced-ediscovery.md)
  
[분석 결과 보기](view-analyze-results-in-advanced-ediscovery.md)

