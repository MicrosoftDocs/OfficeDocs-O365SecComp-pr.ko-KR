---
title: Office 365 Advanced eDiscovery에 대한 데이터 준비
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
ms.assetid: 2fb94c23-1846-4a0e-994d-da6d02445f15
description: 'Office 365 보안을 사용 하는 방법에 알아봅니다 &amp; 준수 센터 Office 365 고급 eDiscovery 사용 하 여 분석을 위해 Office 365 데이터를 준비 합니다. '
ms.openlocfilehash: cf0c76b0c274121da435de7829c769abf5111cab
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22533892"
---
# <a name="prepare-data-for-office-365-advanced-ediscovery"></a>Office 365 Advanced eDiscovery에 대한 데이터 준비

이 항목에서는 고급 ediscovery에서 사례에 콘텐츠 검색의 결과 로드 하는 방법에 설명 합니다. 
  
> [!NOTE]
> 고급 eDiscovery 조직에 대 한 고급 준수 추가 기능 또는 e 5 구독은 Office 365 E3 필요합니다. 해당 요금제에 가입한 상태 고급 eDiscovery 시도 하려는 하지 경우에 [Office 365 Enterprise e 5의 평가판 등록](https://go.microsoft.com/fwlink/p/?LinkID=698279)할 수 있습니다. 
  
## <a name="step-1-prepare-office-365-data-for-advanced-ediscovery"></a>1 단계: 고급 eDiscovery에 대 한 Office 365 데이터 준비

고급 eDiscovery 사용 하 여 데이터를 분석 하려면 Office 365 보안에서 실행 하는 콘텐츠 검색의 결과 사용할 수 있습니다 &amp; 준수 센터 (Office 365 보안에서 **콘텐츠 검색** 페이지에 나열 된 &amp; 준수 센터) 또는 검색 eDiscovery 사례와 관련 된 (보안에서 **eDiscovery** 페이지에 나열 된 &amp; 준수 센터). 
  
고급 eDiscovery에 대 한 분석을 위해 검색 결과 준비 하는 중에 자세한 단계에 대 한 [Office 365 고급 eDiscovery에 대 한 검색 결과 준비를](prepare-search-results-for-advanced-ediscovery.md)참조 하십시오.
  
> [!NOTE]
> Office 365의 외부 데이터를 가지게 하 고 준비 하 고 고급 eDiscovery, 한 참조를에서 분석할 수 있도록 Office 365로 가져올 하는 경우 [Office 365에 PST 파일 가져오기 (영문)의 개요](https://support.office.com/article/ba688e0a-0fcb-4bd7-8e57-2b669564ea84) 및 [Office 365의 보관 제 3 자 데이터](https://go.microsoft.com/fwlink/p/?linkid=716918)입니다. 
  
## <a name="step-2-load-search-result-data-in-to-a-case-in-advanced-ediscovery"></a>2 단계: 검색 결과에서 데이터 로드 고급 ediscovery에서 사례에

보안에서 검색 결과 준비한 후 &amp; 고급 ediscovery에서 사례에에서 검색 결과 로드 하는 분석을 위해 준수 센터, 다음 단계에서는 것입니다. 자세한 내용은 [프로세스 모듈을 실행](run-the-process-module-in-advanced-ediscovery.md)을 참조 하십시오.
  
1. 이동 [https://protection.office.com](https://protection.office.com)합니다.
    
2. 작업이 나 교육용 계정을 사용 하 여 Office 365에 로그인 합니다.
    
3. 보안에서 &amp; 준수 센터 클릭 **검색 &amp; 조사** \> **eDiscovery** 를 조직에서 사례의 목록을 표시 합니다. 
    
4. 고급 ediscovery에서로 데이터 로드 하려는 경우 다음 **열기** 를 클릭 합니다. 
    
5. 대/소문자에 대 한 **홈** 페이지에서 **고급 eDiscovery**를 클릭 합니다. 
    
    ![고급 eDiscovery의 대/소문자를 열려면 고급 ediscovery 스위치를 클릭 합니다.](media/8e34ba23-62e3-4e68-a530-b6ece39b54be.png)
  
    **고급 ediscovery 연결** 진행률 표시줄이 표시 됩니다. 고급 eDiscovery에 연결 하는 경우 대/소문자에 대 한 설치 페이지에서 컨테이너의 목록이 표시 됩니다. 
    
    ![대/소문자 고급 eDiscovery에 표시 됩니다.](media/8036e152-70dc-4bb7-9379-61c1ed8326b4.png)
  
     이러한 컨테이너 고급 eDiscovery (영문) 1 단계에서에서 분석을 위해 준비 하는 검색 결과를 나타냅니다. 보안에서 대/소문자에 콘텐츠 검색와 이름이 같은 미치지 않습니다 컨테이너의 이름을 &amp; 준수 센터입니다. 목록에서 컨테이너는 준비한 메시지입니다. 다른 사용자, 고급 ediscovery 검색 결과 준비 하는 경우 해당 컨테이너 목록에 포함 되지 않습니다. 
    
6. 검색 결과 데이터를 컨테이너에서 고급 eDiscovery의 대/소문자를 로드 하려면 컨테이너를 선택 하 고 **프로세스**를 클릭 합니다.
    
검색 결과 보안에서 후 &amp; 준수 센터를 분석 하 고는 대/소문자와 관련이 있는 데이터를 cull 고급 eDiscovery의 도구를 사용 하 여 다음 단계는 고급 ediscovery에서 사례에 추가 됩니다. 
  
## <a name="see-also"></a>참고 항목

[Office 365 Advanced eDiscovery](office-365-advanced-ediscovery.md)
  
[사용자 및 사례 설정](set-up-users-and-cases-in-advanced-ediscovery.md)
  
[사례 데이터 분석](analyze-case-data-with-advanced-ediscovery.md)
  
[관련성 설정 관리](manage-relevance-setup-in-advanced-ediscovery.md)
  
[관련성 모듈을 사용 하 여](use-relevance-in-advanced-ediscovery.md)
  
[사례 데이터 내보내기 (영문)](export-case-data-in-advanced-ediscovery.md)

