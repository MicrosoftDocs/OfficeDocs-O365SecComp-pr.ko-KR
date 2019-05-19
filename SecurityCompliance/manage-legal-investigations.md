---
title: Office 365에서 법적 조사 관리
ms.author: markjjo
author: markjjo
manager: laurawi
audience: Admin
ms.topic: conceptual
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: 2e5fbe9f-ee4d-4178-8ff8-4356bc1b168e
description: 조직의 법적 조사를 관리 하려면 Office 365의 Security & 준수 센터에서 eDiscovery 사례를 사용 합니다. E5 구독이 있는 경우에는 고급 eDiscovery의 텍스트 분석, 기계 학습 및 예측 코딩 기능을 사용 하 여 사례 데이터를 보다 자세히 분석할 수 있습니다.
ms.openlocfilehash: 6f5b7bc7b1c8d672efe60629b1ccf1315c8b74dd
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/17/2019
ms.locfileid: "34155730"
---
# <a name="manage-legal-investigations-in-office-365"></a>Office 365에서 법적 조사 관리

조직에는 조직의 특정 임원 또는 다른 직원과 관련 된 법적 사례에 대응 해야 하는 여러 가지 이유가 있습니다. 이 작업을 수행 하는 동안에는 해당 일상 업무 작업에 사람들이 사용 하는 전자 메일, 문서, 인스턴트 메시징 대화 및 기타 콘텐츠 위치에서 특정 정보를 빠르게 찾고 보존 하는 작업이 포함 될 수 있습니다. 보안 & 준수 센터의 eDiscovery 사례 도구를 사용 하 여 이러한 작업과 비슷한 여러 가지 작업을 수행할 수 있습니다.
  
[EDiscovery 사례를 사용 하 여 법적 조사 관리](#manage-legal-investigations-with-ediscovery-cases)
  
[Office 365 Advanced eDiscovery를 사용 하 여 사례 데이터 분석](#analyze-case-data-using-office-365-advanced-ediscovery)
  
**Microsoft에서 eDiscovery 조사를 관리 하는 방법을 알고 싶으십니까?** 이 문서에서는 내부 eDiscovery 워크플로를 관리 하기 위해 동일한 Office 365 검색 및 조사 도구를 사용 하는 방법에 대해 설명 하는 [기술 백서](https://go.microsoft.com/fwlink/?linkid=852161) 를 다운로드할 수 있습니다.
   
## <a name="manage-legal-investigations-with-ediscovery-cases"></a>EDiscovery 사례를 사용 하 여 법적 조사 관리

eDiscovery 사례를 사용 하면 조직에서 eDiscovery 사례를 만들고, 액세스 하 고, 관리할 수 있는 사용자를 제어할 수도 있습니다. 사례를 사용 하 여 구성원을 추가 하 고 수행할 수 있는 작업 유형을 제어 하 고, 법적 사례와 관련 된 콘텐츠 위치를 유지 하 고, 콘텐츠 검색 도구를 사용 하 여 해당 사례에 응답할 수 있는 콘텐츠에 대해 보류 중인 위치를 검색 합니다. 그런 다음 외부 검토자의 추가 조사를 위해 해당 결과를 내보내고 다운로드할 수도 있습니다. Office 365 조직에 E5 구독이 있는 경우 고급 eDiscovery에서 분석에 대 한 검색 결과를 준비할 수도 있습니다.
  
- 조직이 수행 해야 하는 모든 법률 조사에 대해 eDiscovery 사례를 만들고 사용 하 여 [ediscovery 워크플로를 관리 합니다](ediscovery-cases.md) . 
    
- 조직에서 eDiscovery 사례를 만들고 관리할 수 있는 사용자를 제어 하기 위해 [ediscovery 권한 할당](assign-ediscovery-permissions.md) 
    
- EDiscovery 관리자가 검색할 수 있는 사용자 콘텐츠 위치를 제어 하는 [준수 경계를 설정](set-up-compliance-boundaries.md) 합니다. 
    
- 조직의 [콘텐츠 검색](search-for-content.md) 
    
- Advanced [ediscovery에 대 한 사례 콘텐츠 준비](prepare-search-results-for-advanced-ediscovery.md) 고급 ediscovery의 강력한 분석 도구 (예: 광학 인식, 전자 메일 스레딩 및 예측 코딩)를 사용 하 여 분석을 수행할 수 있도록 합니다. 
    
### <a name="use-scripts-for-advanced-scenarios"></a>고급 시나리오에 스크립트 사용

콘텐츠 검색 시나리오에 대 한 스크립트를 나열 하는 이전 섹션에서와 마찬가지로 eDiscovery 사례를 관리 하는 데 도움이 되는 몇 가지 보안 & 준수 센터 PowerShell 스크립트도 만들었습니다.
  
- 조직의 eDiscovery 사례와 관련 된 모든 보류에 대 한 정보가 포함 된 [eDiscovery 보류 보고서를 만듭니다](create-a-report-on-holds-in-ediscovery-cases.md) . 
    
- EDiscovery 보류에 사용자 목록에 대 한 [사서함 및 OneDrive 위치 추가](use-a-script-to-add-users-to-a-hold-in-ediscovery.md) 
  
## <a name="analyze-case-data-using-office-365-advanced-ediscovery"></a>Office 365 Advanced eDiscovery를 사용 하 여 사례 데이터 분석

Office 365 Advanced eDiscovery는 이전 섹션에서 설명한 콘텐츠 검색 및 eDiscovery 기능을 기반으로 합니다. EDiscovery 사례를 만들고 custodian 위치를 보류 한 후 사례에 응답할 수 있는 데이터를 수집 하 고 나면 텍스트 분석, 기계 학습 및 고급의 예측 코딩 기능을 사용 하 여 데이터를 상세히 분석할 수 있습니다. eDiscovery. 이를 통해 조직에서 수천 개의 전자 메일 메시지, 문서 및 기타 종류의 데이터를 빠르게 처리 하 여 특정 사례와 관련성이 가장 높은 항목을 찾을 수 있습니다. 또한 보안 & 준수 센터에서 동일한 대/소문자를 완벽 하 게 관리할 수 있도록 통합 사례 관리 및 고급 eDiscovery가 제공 됩니다.
  
> [!NOTE]
> 고급 eDiscovery를 사용 하 여 사용자 데이터를 분석 하려면 데이터의 custodian 사용자에 게 Office 365 E5 라이선스를 할당 해야 합니다. 또는 Office 365 E1 또는 E3 라이선스를 사용 하는 사용자에 게 고급 eDiscovery 독립 실행형 라이선스를 할당할 수 있습니다. 서비스 케이스에 할당 되 고 고급 eDiscovery를 사용 하 여 데이터를 분석 하는 관리자 및 규정 준수 직원은 E5 라이선스가 필요 하지 않습니다. 
  
### <a name="get-started"></a>시작

고급 eDiscovery를 시작 하는 가장 빠른 방법은 사례를 만들고 보안 & 준수 센터에서 검색 결과를 준비한 후 Advanced eDiscovery에서 결과를 로드 한 다음, 빠른 분석을 실행 하 여 사례 데이터를 분석 하 고 결과를 내보내는 것입니다. 외부 리뷰에 해당 합니다.
  
- 고급 eDiscovery 워크플로에 대 한 [간략 한 개요 보기](quick-setup-for-advanced-ediscovery.md) 
    
- 보안 & 준수 센터를 사용 하 여 사례를 만들고, eDiscovery 권한을 할당 하 고, 사례 구성원을 추가 하 여 고급 eDiscovery에 대 한 [사용자 및 사례를 설정](set-up-users-and-cases-in-advanced-ediscovery.md) 합니다. 
    
- Advanced eDiscovery에서 사례에 대 한 [검색 데이터 준비 및 로드](prepare-data-for-advanced-ediscovery.md) 
    
- 고급 eDiscovery에서 분석을 위해 [비 Office 365 데이터](import-non-office-365-data-into-advanced-ediscovery.md) 를 사례에 로드 
    
- [빠른 분석을 사용](use-express-analysis-in-advanced-ediscovery.md) 하 여 사례에서 데이터를 빠르게 분석 한 다음 결과를 쉽게 내보내기 
    
### <a name="analyze-data"></a>데이터 분석

고급 eDiscovery의 사례에 검색 데이터를 로드 한 후에는 Analyze 모듈을 사용 하 여 분석을 시작 합니다. 분석 프로세스의 첫 번째 부분은 파일을 고유한 파일 그룹, 중복 항목 및 거의 모든 이름 (문서 유사성으로 인식)으로 구성 하는 것입니다. 그런 다음 데이터를 계층적으로 구성 된 전자 메일 스레드 및 테마 그룹으로 구성 하 고 필요에 따라 ignore 텍스트 필터를 설정 하 여 특정 텍스트를 분석에서 제외 합니다. 그런 다음 분석을 실행 하 고 결과를 확인 합니다.
  
- 고급 eDiscovery에서 데이터를 분석 하기 위한 준비를 위해 [문서 유사성에 대해 자세히 알아봅니다](understand-document-similarity-in-advanced-ediscovery.md) . 
    
- 유사 복제, 테마 및 전자 메일 스레딩에 대 한 [옵션을 설정](set-analyze-options-in-advanced-ediscovery.md) 하 고 Analyze 모듈을 실행 합니다. 
    
- [무시 텍스트 필터를 설정](set-ignore-text-in-advanced-ediscovery.md) 하 여 텍스트 및 텍스트 문자열이 분석 되지 않도록 합니다. 관련성 분석을 실행 하면 이러한 필터도 텍스트를 무시 합니다. 
    
- 분석 프로세스 [결과 보기](view-analyze-results-in-advanced-ediscovery.md) 
    
- 분석 프로세스에 대 한 [고급 설정 구성](set-analyze-advanced-settings-in-advanced-ediscovery.md) 
    
### <a name="set-up-relevance-training"></a>관련성 교육 설정

고급 eDiscovery에서 예측 코딩 (관련성 이라고 함)은 소수의 문서 집합에 대 한 결정을 내릴 수 있도록 하 여 원하는 내용을 시스템에 교육 합니다.
  
- 관련성 교육 설정, 사례와 관련 된 파일 태그 지정 및 사례 문제 정의 [에 대해 자세히 알아보기](manage-relevance-setup-in-advanced-ediscovery.md) 
    
- [사례 문제를 정의](define-issues-and-assign-users.md) 하 고 파일을 교육할 사용자에 게 각 문제를 할당 합니다. 
    
- [가져온 파일을 관련성 교육에 추가할 현재 또는 새 부하에 추가](set-up-loads-to-add-imported-files.md) 합니다. 부하는 사례에 추가 된 다음 관련성 성향 습득에 사용 되는 새로운 파일 배치입니다. 
    
- 관련성 교육에 추가할 수 있는 [강조 표시 된 키워드를 정의](define-highlighted-keywords-and-advanced-options.md) 합니다. 이를 통해 사례와 관련 된 파일을 보다 효율적으로 식별할 수 있습니다. 
    
### <a name="run-the-relevance-module"></a>관련성 모듈 실행

교육을 설정 하 고 나면 관련성 모듈을 실행 하 고 교육 설정의 효과를 평가할 수 있습니다 .이로 인해 추가 교육을 수행 해야 할지 아니면 파일 태그 지정을 시작할 준비가 되었는지 여부를 결정 하는 데 도움이 되는 관련성 순위가 지정 됩니다. 사용자 사례와 관련이 있습니다.
  
- 샘플 파일 집합을 기반으로 하는 관련성 프로세스 및 평가, 태그 지정, 추적 및 다시 교육 프로세스 [에 대해 알아봅니다](use-relevance-in-advanced-ediscovery.md) . 
    
- 사례에 익숙한 전문가가 사례 파일 집합을 검토 하 고 관련성 교육의 효율성을 확인 하는 [평가에 대해 알아봅니다](assessment-in-relevance-in-advanced-ediscovery.md) . 
    
- [사례 파일을 평가](tagging-and-assessment-in-advanced-ediscovery.md) 하 여 교육 설정의 효율성 ( *다양성* )을 계산 하 고 해당 사례와 관련성이 있거나 관련이 없는 파일에 태그를 적용 합니다. 이렇게 하면 현재 교육이 충분 한지 또는 교육 설정을 조정 해야 하는지 쉽게 확인할 수 있습니다. 
    
- 평가가 완료 된 후 [관련성 교육을 수행한](tagging-and-relevance-training-in-advanced-ediscovery.md) 다음, 사례에 대해 정의한 문제와 관련이 있거나 관련성이 없는 파일을 다시 태그 지정 합니다. 
    
- 관련성 분석 프로세스를 추적 하 여 관련성 교육이 평가 대상 ( *안정적인 교육 상태* 라고 함)을 달성 했는지, 더 많은 교육이 필요한 지를 확인 [합니다](track-relevance-analysis-in-advanced-ediscovery.md) . 또한 각 사례 문제에 대 한 관련성 결과를 볼 수 있습니다. 
    
- 검토를 위해 내보낼 수 있는 사례 파일의 결과 집합 크기를 결정 하기 위한 [관련성 분석에 따라 결정](decision-based-on-the-results-in-advanced-ediscovery.md) 을 내립니다. 
    
- 관련성 [분석의 품질을 테스트](test-relevance-analysis-in-advanced-ediscovery.md) 하 여 관련성 프로세스 중에 수행 된 culling 결정 사항 유효성 검사 
    
### <a name="export-results"></a>결과 내보내기

Advanced eDiscovery에서 사례 데이터를 분석 하는 마지막 단계는 외부 검토에 대 한 분석 결과를 내보내는 것입니다.
  
- [사례 데이터 내보내기에 대 한 자세한 정보](export-case-data-in-advanced-ediscovery.md)
    
- [사례 데이터 내보내기](export-results-in-advanced-ediscovery.md)
    
- [일괄 처리 기록 보기 및 이전 결과 내보내기](view-batch-history-and-export-past-results.md)
    
- [보고서 필드 내보내기](export-report-fields-in-advanced-ediscovery.md)
    
### <a name="other-advanced-ediscovery-tools"></a>기타 고급 eDiscovery 도구

고급 eDiscovery에서는 사례 데이터, 관련성 분석 및 데이터 내보내기에 대 한 추가 도구 및 기능을 제공 합니다.
  
- [고급 eDiscovery 보고서 실행](run-reports-in-advanced-ediscovery.md)
    
- [사례 및 테 넌 트 설정 정의](define-case-and-tenant-settings-in-advanced-ediscovery.md)
    
- [고급 eDiscovery 유틸리티](use-advanced-ediscovery-utilities.md)
