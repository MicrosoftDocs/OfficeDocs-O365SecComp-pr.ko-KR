---
title: Office 365 Advanced eDiscovery에 대 한 데이터 준비
ms.author: chrfox
author: chrfox
manager: laurawi
ms.date: 9/14/2017
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: 2fb94c23-1846-4a0e-994d-da6d02445f15
description: 'Microsoft 365 보안 &amp; 및 준수 센터를 사용 하 여 Office 365 Advanced eDiscovery로 Analysis for office 365 데이터를 준비 하는 방법을 알아봅니다. '
ms.openlocfilehash: be778acb3356071e9575ed708623a0b94e2b3c7a
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/17/2019
ms.locfileid: "34157460"
---
# <a name="prepare-data-for-office-365-advanced-ediscovery"></a>Office 365 Advanced eDiscovery에 대 한 데이터 준비

이 항목에서는 Advanced eDiscovery의 사례에 대 한 콘텐츠 검색 결과를 로드 하는 방법에 대해 설명 합니다. 
  
> [!NOTE]
> Advanced eDiscovery를 사용하려면 Office 365 E3의 고급 준수 추가 기능이나 조직을 위한 E5 구독이 필요합니다. 이 요금제가 없는 상태에서 Advanced eDiscovery를 사용하려는 경우에는 [Office 365 Enterprise E5 평가판을 등록](https://go.microsoft.com/fwlink/p/?LinkID=698279)할 수 있습니다. 
  
## <a name="step-1-prepare-office-365-data-for-advanced-ediscovery"></a>1 단계: 고급 eDiscovery 용 Office 365 데이터 준비

고급 eDiscovery를 사용 하 여 데이터를 분석 하기 위해 microsoft 365 보안 <b0></b0> <b2></b2> 및 준수 센터의 <b1>콘텐츠 검색</b1> 페이지에 나열 된 < 365 보안 준수 센터에서 실행 한 콘텐츠 검색의 결과를 사용할 수 있습니다. eDiscovery 사례에 연결 된 검색 (보안 <b4></b4> 및 준수 센터의 <b3>ediscovery</b3> 페이지에 나열 됨) 
  
고급 eDiscovery에서 분석에 대 한 검색 결과를 준비 하는 방법에 대 한 자세한 단계는 [Office 365 Advanced eDiscovery에 대 한 검색 결과 준비](prepare-search-results-for-advanced-ediscovery.md)를 참조 하세요.
  
> [!NOTE]
> Office 365 외부에 데이터가 있고이를 office 365로 가져와서 고급 eDiscovery에서이를 준비 하 고 분석할 수 있도록 하려면 office 365에서 PST 파일을 365 office로 가져오기 개요 및 타사 데이터 보관을 참조 하세요. 
  
## <a name="step-2-load-search-result-data-in-to-a-case-in-advanced-ediscovery"></a>2 단계: Advanced eDiscovery에서 사례에 검색 결과 데이터 로드

분석을 위해 보안 &amp; 및 준수 센터에서 검색 결과를 준비한 다음에는 Advanced eDiscovery의 사례에 검색 결과를 로드 합니다. 자세한 내용은 [Process 모듈 실행](run-the-process-module-in-advanced-ediscovery.md)을 참조 하십시오.
  
1. [https://protection.office.com](https://protection.office.com)으로 이동합니다.
    
2. 회사 또는 학교 계정을 사용하여 Office 365에 로그인합니다.
    
3. 보안 및 준수 센터에서 **검색 &amp; 조사** \> **eDiscovery**를 클릭하여 조직의 사례 목록을 표시합니다. 
    
4. 고급 eDiscovery에서 데이터를 로드 하려는 사례 옆에 있는 **열기** 를 클릭 합니다. 
    
5. 사례에 대한 **홈** 페이지에서 **Advanced eDiscovery**를 클릭합니다. 
    
    ![Advanced eDiscovery로 전환을 클릭 하 여 Advanced eDiscovery의 케이스 열기](media/8e34ba23-62e3-4e68-a530-b6ece39b54be.png)
  
    **고급 eDiscovery 진행률 표시줄에 연결 하** 는 중입니다. 고급 eDiscovery에 연결 되어 있는 경우 서비스 케이스의 설정 페이지에 컨테이너 목록이 표시 됩니다. 
    
    ![이 사례는 Advanced eDiscovery에 표시 됩니다.](media/8036e152-70dc-4bb7-9379-61c1ed8326b4.png)
  
     이러한 컨테이너는 1 단계에서 고급 eDiscovery를 분석 하기 위해 준비한 검색 결과를 나타냅니다. 컨테이너의 이름은 보안 &amp; 및 준수 센터의 사례에 있는 콘텐츠 검색과 이름이 같습니다. 이 목록에는 사용자가 준비한 컨테이너 들이 나열 됩니다. 다른 사용자가 고급 eDiscovery를 위해 준비 된 검색 결과를 사용 하는 경우 해당 컨테이너가 목록에 포함 되지 않습니다. 
    
6. 컨테이너의 검색 결과 데이터를 Advanced eDiscovery의 사례에 로드 하려면 컨테이너를 선택 하 고 **처리**를 클릭 합니다.
    
보안 &amp; 및 준수 센터의 검색 결과가 advanced ediscovery의 사례에 추가 되 면 다음 단계는 advanced ediscovery의 도구를 사용 하 여 사례와 관련 된 데이터를 분석 하 고 cull 합니다. 
  
## <a name="see-also"></a>참고 항목

[Office 365 Advanced eDiscovery](office-365-advanced-ediscovery.md)
  
[사용자 및 사례 설정](set-up-users-and-cases-in-advanced-ediscovery.md)
  
[사례 데이터 분석](analyze-case-data-with-advanced-ediscovery.md)
  
[관련성 설정 관리](manage-relevance-setup-in-advanced-ediscovery.md)
  
[관련성 모듈 사용](use-relevance-in-advanced-ediscovery.md)
  
[사례 데이터 내보내기](export-case-data-in-advanced-ediscovery.md)

