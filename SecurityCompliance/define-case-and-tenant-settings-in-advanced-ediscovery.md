---
title: Office 365 Advanced eDiscovery에서 사례 및 테 넌 트 설정 정의
ms.author: chrfox
author: chrfox
manager: laurawi
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: 383809de-7f5e-4a1d-9098-c525f67b7a9a
description: 'Office 365 Advanced eDiscovery의 사례 수준에서 정의할 수 있는 레이블, 모듈 간 및 테 넌 트 설정에 대해 알아봅니다.  '
ms.openlocfilehash: 69e6e824a7c6a5698e9dc25095d4fab49e369490
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/17/2019
ms.locfileid: "34150600"
---
# <a name="define-case-and-tenant-settings-in-office-365-advanced-ediscovery"></a>Office 365 Advanced eDiscovery에서 사례 및 테 넌 트 설정 정의

> [!NOTE]
> Advanced eDiscovery를 사용하려면 Office 365 E3의 고급 준수 추가 기능이나 조직을 위한 E5 구독이 필요합니다. 이 요금제가 없는 상태에서 Advanced eDiscovery를 사용하려는 경우에는 [Office 365 Enterprise E5 평가판을 등록](https://go.microsoft.com/fwlink/p/?LinkID=698279)할 수 있습니다. 
  
고급 eDiscovery 사례 및 테 넌 트 설정은이 항목에 설명 되어 있습니다.
  
## <a name="case-settings"></a>사례 설정

이 섹션에서는 사례 수준에서 정의할 수 있는 설정에 대해 설명 합니다.
  
> [!NOTE]
> 고급 eDiscovery에서 현재 선택 된 케이스가 없으면 **사례 설정** 탭이 비활성화 됩니다. 
  
### <a name="cross-module"></a>크로스 모듈

다음 크로스 모듈 설정은 고급 eDiscovery 모듈에 적용 되는 대/소문자 옵션입니다.
  
- 로그인 후 기본 페이지 고급 eDiscovery를 시작할 때 기본 페이지가 표시 되도록 설정 합니다.
    
- 파일 표시 이름: 파일 제목/경로 또는 전자 메일 제목의 고급 eDiscovery 표시 이름 대신 파일을 식별 하기 위해 고급 eDiscovery 전체에서 표시 되는 파일 식별자입니다.
    
1. **Cogwheel** 아이콘을 클릭 하 여 **설정 및 유틸리티** 를 엽니다. **설정 및 유틸리티 \> 사례 설정 탭** \> 을 **모듈 간에**엽니다. 
    
2. **로그인 옵션 후 기본 페이지** 에서를 선택 합니다. 
    
  - **이전 로그인의 마지막 페이지**
    
  - **사례 페이지**
    
3. **저장**을 클릭합니다.
    
## <a name="tenant-settings"></a>테 넌 트 설정

이 섹션에서는 고급 eDiscovery 테 넌 트 설정에 대해 설명 합니다.
  
### <a name="user-administration"></a>관리

사용자 관리 옵션은 [사용자 및 사례 설정](set-up-users-and-cases-in-advanced-ediscovery.md)에 설명 되어 있습니다.
  
### <a name="event-log"></a>이벤트 로그

이벤트 로그는 Advanced eDiscovery 작업 중에 언제 든 지 Advanced eDiscovery 처리와 관련 된 메타 데이터를 제공 합니다. 예를 들어 기본 고급 eDiscovery 프로세스 (가져오기, 분석, 관련성 및 내보내기)의 시작 시간 뿐만 아니라 종료 시간 및 상태를 포함 합니다. 이 로그는 데이터 처리 작업을 추적 하 고 문제를 해결 하 고 오류 및 경고를 해결 하는 데 사용할 수 있습니다.
  
1. **Cogwheel** 아이콘을 클릭 하 여 **설정 및 유틸리티** 를 엽니다. 
    
2. **설정 및 유틸리티 \> 테 넌 트 설정** 탭에서 **이벤트 로그**를 선택 합니다. 이벤트 로그 데이터가 표시 됩니다.
    
  - 로그 출력을 사례 별로 필터링 하려면 **사례** 목록에서 사례를 선택 합니다. 
    
  - 열을 기준으로 로그를 정렬 하려면 열 머리글을 클릭 합니다. 
    
  - 열 순서를 수정 하려면 열 머리글을 클릭 하 고 끕니다.
    
  - 로그 페이지 간 이동 하려면 및 **\>** **\<** 아이콘을 클릭 합니다. 
    
### <a name="system-information"></a>시스템 정보

Advanced eDiscovery 버전 시스템 정보 및 활성 작업이 테 넌 트 설정 탭에 표시 됩니다.
  
1. **Cogwheel** 아이콘을 클릭 하 여 **설정 및 유틸리티** 를 엽니다. 
    
2. **설정 및 유틸리티 \> 테 넌 트 설정** 탭에서 **시스템 정보**를 선택 합니다. 버전 정보가 표시 됩니다.
    
테 넌 트 정보 아래의 **새로 고침** 아이콘을 클릭 하 여 표시를 업데이트할 수 있습니다. 
  
## <a name="see-also"></a>참고 항목

[Office 365 Advanced eDiscovery](office-365-advanced-ediscovery.md)
  
[유틸리티 사용](use-advanced-ediscovery-utilities.md)

