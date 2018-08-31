---
title: Office 365 Advanced eDiscovery에서 관련성 평가 이해
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
ms.assetid: 1d33d4fb-91ed-41c0-b72e-5a26eca3a2a7
description: '평가 단계 및 Office 365 고급 eDiscovery의 관련성 교육 하는 동안 다양 한 문제를 결정할 때 해당 역할에 대 한 개요를 가져옵니다.  '
ms.openlocfilehash: a54a4134609b16568586f3cb6b60ebdeba860bac
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22533508"
---
# <a name="understand-assessment-in-relevance-in-office-365-advanced-ediscovery"></a>Office 365 Advanced eDiscovery에서 관련성 평가 이해

> [!NOTE]
> 고급 eDiscovery 조직에 대 한 고급 준수 추가 기능 또는 e 5 구독은 Office 365 E3 필요합니다. 해당 요금제에 가입한 상태 고급 eDiscovery 시도 하려는 하지 경우에 [Office 365 Enterprise e 5의 평가판 등록](https://go.microsoft.com/fwlink/p/?LinkID=698279)할 수 있습니다. 
  
고급 eDiscovery에 따라 정의 된 문제 및 사례에 대해 가져온 데이터에 대 한 초기 평가 사용 하는 예입니다. 고급 eDiscovery 전문가 관련 된 채택된 되는 방법을 결정 하 고 문서 검토 프로젝트에 적용할 수 있습니다.
  
## <a name="understanding-assessment"></a>이해 평가

평가, 전문가 다양 한 문제를 확인 하 고 교육 결과 반영 하는 통계를 생성 하는데 사용 되는 최소한 500 파일의 임의 집합을 검토 합니다. 평가 고급 eDiscovery 관련성 정확 하 게 통계를 제공 하 고 효과적으로 교육 프로세스에서 안정화 포인트를 결정 하는 데 도움이 되는 통계 수준에 도달 하기 위해 충분 한 관련 된 파일이 발견 되 면 실행 되었습니다. 
  
많을 수록 더 정확한 평가 집합에서 관련 수가 파일을 통계 및 안정성 알고리즘의 효과입니다. 평가 파일 내에서 관련 파일의 수는 다양 한 문제에 따라 달라 집니다. 다양성이 문제에 관련 된 집합의 관련 파일의 예상된 %입니다. 이보다 더 풍부한 기능 관련 문제가 더 낮은 다양성와 관련 파일 수가 많을 수록 문제 보다 빠르게 도달 합니다. 매우 낮은 풍부한 기능 관련 문제 (예: 2% 이하의) 관련 파일의 수가 많은 도달로 설정 하는 매우 큰 평가 수행 해야 합니다.
  
다른 검토 집합에 대 한 회수의 추정치를 포함 하는 통계를 교육 하는 동안 및 일괄 처리 계산 후 추적 및 판단 탭에 표시 됩니다. 통계를 추정: 표본을 기반으로 하는 설정 (이 경우 평가 파일)에 오류의 여백 및 해당 오류 여백 신뢰도 포함 합니다. 예, 80%의 예상된 회수 오차 여백으로 더하기의 또는 5%-95%의 신뢰도가 있을 수 있습니다. 즉, 예상된 회수는 실제로 75%-85% 하 고이 예상이 95% 신뢰 합니다. 평가 집합 클수록 오류의 여백 더 작은 되며 통계가 보다 정확 하 게 합니다. 
  
전문가 초기 평가 집합이 500 파일을 검토, 한 후 관련성은 현재 여백의 회수 값의 오류를 확인할 수 있습니다. 관련성 평가 집합을 최적화 하기 위해 도달 하기 위해 권장 되는 오류의 기본 여백을 설정도 됩니다. 다음은 몇가지 예입니다.
  
- 이미 설정 평가 검색어 오류 더하기의 또는 10% 보다 작은 값의 여백, 교육 (없음 추가 평가 검토 필요)로 이동 하려면 관련성은 것이 좋습니다. 
    
- 평가 집합 더하기의 또는 13% 빼기 오류의 여백 검색어를 하는 경우 관련성 다른 집합이 더 작은 여백에 도달 하기 위해 평가 파일의 검토를 것이 좋습니다 될 수 있습니다. 
    
- 다양성 매우 낮은 경우 관련성 오류의 여백 (요청 통계 비실용적) 큰 경우에 평가 중지 하는 것이 좋습니다 될 수 있습니다, 그리고 오류의 유용한 여백에 도달 하는 데 필요한 평가 설정 때문에 너무 큽니다.
    
각 문제 자체 다양성, 오류의 현재 여백을 있으며 따라서 추가 평가 파일의 수를 예상 합니다. 다음 평가 집합 (최대 1, 000 개 단일 집합에서) 파일의 최대 수에 따라 만들어집니다.
  
관련성 권장 사항을 따르는 또는 사용자의 요구에 따라 현재 여백의 오류를 조정할 수 있습니다. 오류의 기본 현재 여백 회수 equal 이상 75%에 따라 결정 됩니다.
  
> [!NOTE]
> 평가 단계를 무시할 수 있습니다에서 **관련성 \> 추적** 문제 당 한 "모든 문제"에 대 한 다음 **평가** 확인란 선택을 취소 하 여는 문제에 대 한 확장 된 보기의 탭입니다. 그러나 결과적으로, 됩니다이 문제에 대 한 통계 없습니다. > **평가** 확인란의 선택을 취소만 가능 평가 수행 하기 전에 합니다. 각 문제에 대 한 확인란의 선택을 취소 하는 경우에 평가 사용 하지 않을 경우에 여러 문제가 존재 하는 경우 
  
## <a name="see-also"></a>참고 항목

[Office 365 Advanced eDiscovery](office-365-advanced-ediscovery.md)
  
[태그 지정 및 평가](tagging-and-assessment-in-advanced-ediscovery.md)
  
[태그 지정 및 관련성 교육](tagging-and-relevance-training-in-advanced-ediscovery.md)
  
[관련성 분석 추적](track-relevance-analysis-in-advanced-ediscovery.md)
  
[결과에 따라 결정](decision-based-on-the-results-in-advanced-ediscovery.md)
  
[관련성 분석 테스트](test-relevance-analysis-in-advanced-ediscovery.md)

