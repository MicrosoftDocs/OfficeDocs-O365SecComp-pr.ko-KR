---
title: Office 365 Advanced eDiscovery 프로세스 모듈 결과에 기반한 의사 결정
ms.author: chrfox
author: chrfox
manager: laurawi
ms.date: 9/14/2017
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: aed65bcd-0a4f-43e9-b5e5-b98cc376bdf8
description: 'Office 365 고급 ediscovery에서 판단 탭을 제공 하는데 도움이 되는 데이터 검토 일련의 경우 파일의 올바른 크기를 계산 하는 방법을 설명 합니다. '
ms.openlocfilehash: 58a181e00ad5843ccbbde4dcb47050eccf199225
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22533213"
---
# <a name="decision-based-on-the-results-in-office-365-advanced-ediscovery"></a>Office 365 Advanced eDiscovery 프로세스 모듈 결과에 기반한 의사 결정

> [!NOTE]
> 고급 eDiscovery 조직에 대 한 고급 준수 추가 기능 또는 e 5 구독은 Office 365 E3 필요합니다. 해당 요금제에 가입한 상태 고급 eDiscovery 시도 하려는 하지 경우에 [Office 365 Enterprise e 5의 평가판 등록](https://go.microsoft.com/fwlink/p/?LinkID=698279)할 수 있습니다. 
  
 고급 eDiscovery 판단 탭의 보기 및 사례 파일의 검토 집합의 크기를 결정 하기 위한 의사 결정 지원 통계를 사용 하는 것에 대 한 추가 정보를 제공 합니다. 
  
## <a name="using-the-decide-tab"></a>판단 탭을 사용 하 여

![관련성을 결정](media/f32fed89-f3b5-404a-90c7-ea25d2eb58a9.png)
  
이 탭에는 다음이 포함 됩니다.
  
- **문제**: 여기에서 관심 목록에서 문제를 선택할 수 있습니다. 
    
- **검토 회수 비율**: 관련성 점수에 따라 eDiscovery 검토 고급 비교 합니다. 다음은 차트에서 구분 지점 관련성 점수에 매핑된 파일을 검토의 비율을 나타냅니다. 컬링을 대 한 관련성 테스트 단계에서와 내보내기 임계값으로 사용 됩니다. 검토 파일의 수에 대 한 기본 구분 지점을 회수 및 정밀도 간의 균형 최적의 지점에서 됩니다. 실제 구분 지점은 목표 및 비용 장단점이 (% 검토) 및 위험 요소 (% 회수)에 따라 사용자에 의해 결정 됩니다. 슬라이더를 사용 하 여 구분 점을 조정할을 하 고 유효성을 검사 하는 결정 하기 전에 관련 파일을 검색할 수의 비율을 조정할 때 그래프와 매개 변수를에 미치는 영향을 볼 수 있습니다.
    
- **매개 변수**: 검토, 다음 관련 및 총 비용 매개 변수는 전체 대/소문자에 대 한 컬렉션에 relation에서 설정 검토와 관련 된 누적 계산 된 통계를 회수 합니다. 이러한 매개 변수에 대 한 정의 다음과 같습니다.
    
    **검토**:이 실시간 구분에 검토 하려면 파일의 백분율을 기준으로 합니다. 
    
    **회수**: 검토 집합의 관련 파일의 비율입니다. 
    
    **다음 관련**: 검토 하 고 설정 되지 않은 현재 검토에서 하는 추가 관련 파일을 식별 하는 비용입니다. 
    
    **총 비용**:이 비율의 경우 파일을 검토 하는 것에 대 한 비용입니다. 비용된 매개 변수 설정의 경우 관리자가 설정할 수 있습니다.
    
- **관련성 점수 하 여 배포**: 마감 점수 미만 왼쪽에 진한 회색 디스플레이 있는 파일입니다. 총 파일 관계에서 설정 검토 파일 관련성 점수 및 파일의 관련된 백분율을 표시 하는 도구 설명입니다.
    
추가 세부 정보를 표시 하는 확장 된 세부 정보 창입니다. 파일 컬렉션 그림 목차에 비어 있거나 모호한 파일을 포함 하지 마십시오. 가족 파일 그림 로드 되는 관련성을 아직 제품군의 일부로 계속 계산에 포함 되지 되는 파일을 나타냅니다.
  
## <a name="see-also"></a>참고 항목

[Office 365 Advanced eDiscovery](office-365-advanced-ediscovery.md)
  
[관련성에 이해 평가](assessment-in-relevance-in-advanced-ediscovery.md)
  
[태그 지정 및 평가](tagging-and-relevance-training-in-advanced-ediscovery.md)
  
[관련성 교육을 수행합니다.](tagging-and-assessment-in-advanced-ediscovery.md)
  
[관련성 분석 추적](track-relevance-analysis-in-advanced-ediscovery.md)
  
[관련성 분석 테스트](test-relevance-analysis-in-advanced-ediscovery.md)

