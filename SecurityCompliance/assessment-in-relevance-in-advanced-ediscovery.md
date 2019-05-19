---
title: Office 365 Advanced eDiscovery에서 관련성 평가 이해
ms.author: chrfox
author: chrfox
manager: laurawi
ms.date: 9/14/2017
audience: Admin
ms.topic: conceptual
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: 1d33d4fb-91ed-41c0-b72e-5a26eca3a2a7
description: Office 365 Advanced eDiscovery의 관련성 교육 중에 다양 한 문제를 파악 하기 위한 평가 단계 및 해당 역할에 대 한 개요를 확인할 수 있습니다.
ms.openlocfilehash: 229df3f51c6a71ddb644fcd45a6de0e30f9775b9
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/17/2019
ms.locfileid: "34155540"
---
# <a name="understand-assessment-in-relevance-in-office-365-advanced-ediscovery"></a>Office 365 Advanced eDiscovery에서 관련성 평가 이해

> [!NOTE]
> Advanced eDiscovery를 사용하려면 Office 365 E3의 고급 준수 추가 기능이나 조직을 위한 E5 구독이 필요합니다. 이 요금제가 없는 상태에서 Advanced eDiscovery를 사용하려는 경우에는 [Office 365 Enterprise E5 평가판을 등록](https://go.microsoft.com/fwlink/p/?LinkID=698279)할 수 있습니다. 
  
고급 eDiscovery에서는 정의 된 문제와 사례에 대해 가져온 데이터에 대 한 초기 평가를 수행할 수 있습니다. 고급 eDiscovery를 사용 하면 전문가가 채택 된 방법과 관련 하 여 의사 결정을 내리고 문서 검토 프로젝트에 적용할 수 있습니다.
  
## <a name="understanding-assessment"></a>평가 이해

평가에서는 전문가가 문제를 확인 하 고 교육 결과를 반영 하는 통계를 생성 하는 데 사용 되는 최소 500 파일 중에서 임의의 집합을 검토 합니다. 평가는 성공적인 통계를 제공 하 고 교육 프로세스에서 안정화 된 지점을 효과적으로 결정 하는 데 도움이 되는 자세한 eDiscovery 관련성을 유지 하는 통계 수준에 도달 하기 위해 충분 한 관련 파일이 발견 되는 경우 성공 합니다. 
  
평가 집합에서 관련 파일의 수가 많을 수록 통계와 안정성 알고리즘의 효율성이 더욱 정확해 집니다. 평가 파일 내의 관련 파일 수는 다양 한 문제에 따라 달라 집니다. 다양성은 문제와 관련 된 집합에서 관련 파일의 예상 비율입니다. 더 많은 다양성을 가진 문제는 보다 자세한 문제 보다 더 많은 관련 파일에 빠르게 도달 하 게 됩니다. 아주 낮은 다양성 (예: 2% 이하인 경우) 문제에는 많은 수의 관련 파일에 도달 하기 위해 매우 큰 평가 집합이 필요 합니다.
  
성향 습득 중 및 일괄 처리를 수행 하는 동안 Track 및 결정 탭에 표시 되는 통계는 서로 다른 검토 집합에 대 한 회수의 추정치를 포함 합니다. 통계에서 예제 집합을 기반으로 하는 추정치 (이 경우 평가 파일)에는 오류의 여백과 해당 오류 여백에 대 한 신뢰 수준이 포함 됩니다. 예를 들어, 80%의 예상 회수는 신뢰도가 95% 인 + 또는-5%의 오차를 포함할 수 있습니다. 즉, 예상 회수는 실제로 75%-85%이 고이 예상은 95%의 신뢰도를 나타냅니다. 평가 설정이 클수록 오류 여백이 작아지고 통계가 더 정확 합니다. 
  
전문가가 500 파일의 초기 평가 집합을 검토 한 후에는 관련성을 통해 회수 값의 현재 오류 여백을 확인할 수 있습니다. 또한 평가 집합을 최적화 하기 위해 권장 되는 기본 오류 여백도 함께 설정 됩니다. 몇 가지 예는 다음과 같습니다.
  
- 평가 집합에서 + 또는-10%의 오류 여백이 이미 발생 한 경우 교육을 진행 하는 것이 좋습니다 (추가 평가 검토가 필요 하지 않음). 
    
- 평가 집합에 플러스 또는-13%의 오류 여백이 발생 한 경우 관련성이 더 작은 부분에 도달 하도록 다른 평가 파일 집합을 검토 하는 것이 좋습니다. 
    
- 유용한 오류 여백에 도달 하는 데 필요한 평가 집합이 너무 커서 오류가 발생 한 경우에도 다양성은 매우 낮은 수준의 평가를 중지 하는 것이 좋습니다.
    
각 문제에는 고유한 다양성, 현재까지 오류가 발생 한 여백이 있으며, 따라서 예측 된 추가 평가 파일 수가 표시 됩니다. 다음 평가 집합은 최대 파일 수에 따라 생성 됩니다 (단일 집합에서 최대 1000).
  
관련성 권장 사항을 그대로 사용 하거나 필요에 따라 현재 오류 여백을 조정할 수 있습니다. 기본값 현재 오류 여백이 75% 이상 인지 여부에 따라 결정 됩니다.
  
> [!NOTE]
> 평가 단계를 무시할 수 있으며, 문제에 대 한 확장 된 보기의 ** \> 관련성 트랙** 탭에서 문제 마다 **평가** 확인란을 선택 취소 하 고 "모든 문제"에 대해 확인 합니다. 그러나 따라서이 문제에 대 한 통계가 제공 되지 않습니다. **평가** 를 수행 하기 전에 > 확인 확인란을 선택 해야 합니다. 사례에 여러 문제가 있는 경우 각 문제에 대해 확인란이 선택 취소 되어 있는 경우에만 평가를 무시 합니다. 
  
## <a name="see-also"></a>참고 항목

[Office 365 Advanced eDiscovery](office-365-advanced-ediscovery.md)
  
[태그 지정 및 평가](tagging-and-assessment-in-advanced-ediscovery.md)
  
[태그 지정 및 관련성 교육](tagging-and-relevance-training-in-advanced-ediscovery.md)
  
[관련성 분석 추적](track-relevance-analysis-in-advanced-ediscovery.md)
  
[결과를 기준으로 결정](decision-based-on-the-results-in-advanced-ediscovery.md)
  
[관련성 분석 테스트](test-relevance-analysis-in-advanced-ediscovery.md)

