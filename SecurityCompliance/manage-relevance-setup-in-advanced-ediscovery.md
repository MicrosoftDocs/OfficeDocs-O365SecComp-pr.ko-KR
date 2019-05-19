---
title: Office 365 Advanced eDiscovery에서 관련성 설정 관리
ms.author: chrfox
author: chrfox
manager: laurawi
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Priority
search.appverid:
- MOE150
- MET150
ms.assetid: fd6be6d3-2e8d-449d-9851-03ab7546e6aa
description: 관련성별로 파일 점수를 매기고 분석 결과를 생성하도록 Office 365 Advanced eDiscovery의 관련성 학습을 설정하기 위한 권장 사항을 읽어봅니다.
ms.openlocfilehash: 5efcaca0d62cec6ccf61f20eea72ed9c538e436e
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/17/2019
ms.locfileid: "34155690"
---
# <a name="manage-relevance-setup-in-office-365-advanced-ediscovery"></a>Office 365 Advanced eDiscovery에서 관련성 설정 관리

> [!NOTE]
> Advanced eDiscovery를 사용하려면 Office 365 E3의 고급 준수 추가 기능이나 조직을 위한 E5 구독이 필요합니다. 이 요금제가 없는 상태에서 Advanced eDiscovery를 사용하려는 경우에는 [Office 365 Enterprise E5 평가판을 등록](https://go.microsoft.com/fwlink/p/?LinkID=698279)할 수 있습니다. 
  
 Advanced eDiscovery 관련성 기술은 관련성에 따라 파일에 점수를 매기기 위해 전문가 지원 소프트웨어를 사용합니다. Advanced eDiscovery 관련성은 ECA(초기 사례 평가), 선별 및 파일 샘플 검토에 사용할 수 있습니다. 
  
 Advanced eDiscovery에는 사례와 관련된 파일에 대한 관련성 학습 및 태그 지정을 위한 구성 요소가 포함되어 있습니다. Advanced eDiscovery는 관련 및 비관련 파일의 학습된 샘플에서 학습하여 각 파일에 대해 관련성 점수를 제공하고, 파일 검토 프로세스 도중 및 이후에 사용할 수 있는 분석 결과를 제공합니다. 
  
## <a name="guidelines-for-setting-up-relevance-training"></a>관련성 학습 설정 지침

 Advanced eDiscovery의 **사례** 창에서 사례를 선택하고 **사례로 이동**을 클릭합니다. **관련성** \> **관련성 설정**을 클릭합니다. 권장 지침에 따라 관련성을 설정합니다. 
  
- **태그 지정**: 반복적인 관련성 학습 프로세스의 효과는 정확도 및 일관성을 유지하면서 파일 샘플에 태그를 지정하는 전문가의 능력에 달려 있습니다.
    
- **사례 문제**: 
    
  - 각 문제에 있어서, 관련성 학습 프로세스 전체에 걸쳐 동일한 전문가를 사용합니다. 여러 명의 전문가가 동시에 같은 문제에 대해 태그를 지정하는 것은 허용되지 않습니다.
    
  - 각 파일 그룹이 특정 문제와만 관련이 있는지를 확인합니다. 
    
  - 문제가 너무 일반적으로 정의되면 Advanced eDiscovery는 실제로 관련성이 없는 너무 많은 파일을 표시할 수 있습니다. 문제가 너무 구체적으로 정의되면 관련성 학습 프로세스에 더 많은 시간이 걸릴 수 있습니다. 
    
  - 각 관련성 학습 주기 동안, Advanced eDiscovery는 단일 활성 문제에 초점을 맞추며, 그에 따라 임시 샘플 결과가 표시됩니다.
    
  - 여러 문제 시나리오에서는 샘플링 모드를 사용하여 처리에 포함할 문제를 선택할 수 있습니다. “해제”로 정의된 문제는 샘플링 모드가 변경될 때까지 처리되지 않습니다. 문제는 한 명의 전문가에 대해 “유휴” 또는 “설정”일 수 있습니다.
    
  -  Advanced eDiscovery를 사용하여 후보 권한 파일을 생성할 수 있습니다. 권한에 대해서는 별도 문제를 설정합니다. 가능한 경우 관련성을 먼저 학습 및 선별한 다음, 선별된 집합에 대해서만 권한을 학습합니다(선별된 집합을 별도 사례로 다시 로드). 
    
  - 배치 계산은 열린 샘플이 없을 때만 수행할 수 있습니다(배치 계산을 클릭하면 열린 샘플이 있는 사용자의 목록이 표시됨). 다른 사용자의 샘플을 “닫으려는 경우”(이러한 사용자가 이러한 샘플에 태그를 지정하지 않은 경우에만 가능) 관리자가 “관련성 수정” 유틸리티에서 “모든 사용자 샘플” 옵션을 사용할 수 있습니다.
    
- **메타데이터**: Advanced eDiscovery는 콘텐츠에 주안점을 줍니다. 따라서 관련성 조건의 일부로 메타데이터를 고려하지 않습니다. 
    
- **풍부성**: 문제의 풍부성이 평가 후에 3% 미만이 되면 알려진 관련 및 비관련 파일을 사용한 관련성 학습을 시드하는 것이 좋습니다.
    
- **파일 크기**: 큰 파일(추출된 텍스트가 5,242,880자 이상인 경우)은 관련성에서 무시됩니다. 이러한 파일은 관련성 학습 프로세스에 참여하지 않으며, 배치 계산 후에 관련성 점수를 받지 않습니다. 5MB보다 큰 파일은 평가 집합에 포함될 수 없습니다.
    
## <a name="setting-up-case-issues"></a>사례 문제 설정

이 섹션에 설명된 매개 변수는 Advanced eDiscovery **관련성** \> **관련성 설정**에서 사용할 수 있습니다. 
  
- 문제는 파일을 학습하는 사용자에게 할당되어야 합니다.
    
- 그런 후에 중요한 파일은 처리될 로드에 추가됩니다.
    
- 문제는 관련성 학습 결과에 영향을 미칠 수 있으므로 신중하게 정의하고 구성합니다.
    
매개 변수가 설정되면 검토자/전문가는 **관련성** 탭에서 파일 학습을 시작할 수 있습니다. 
  
## <a name="see-also"></a>참고 항목

[Office 365 Advanced eDiscovery](office-365-advanced-ediscovery.md)
  
[문제 정의 및 사용자 할당](define-issues-and-assign-users.md)
  
[가져온 파일을 추가하도록 로드 설정](set-up-loads-to-add-imported-files.md)
  
[강조 표시된 키워드 및 고급 옵션 정의](define-highlighted-keywords-and-advanced-options.md)

