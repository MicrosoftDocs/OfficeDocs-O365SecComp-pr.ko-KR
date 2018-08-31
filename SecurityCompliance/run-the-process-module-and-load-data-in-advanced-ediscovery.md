---
title: Office 365 Advanced eDiscovery 프로세스 모듈 실행 및 데이터 로드
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
ms.assetid: c87bb0e5-301c-4d1d-958e-aabeb7990f44
description: 'Office 365 보안을 사용 하는 방법에 알아봅니다 &amp; 준수 센터 Office 365 고급 eDiscovery를 액세스 하는 경우에 대 한 프로세스 모듈을 실행 합니다.  '
ms.openlocfilehash: 32052bccc37d20c8707a1efb0592f7c93daf3590
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22533509"
---
# <a name="run-the-process-module-and-load-data-in-office-365-advanced-ediscovery"></a>Office 365 Advanced eDiscovery 프로세스 모듈 실행 및 데이터 로드

> [!NOTE]
> 고급 eDiscovery 조직에 대 한 고급 준수 추가 기능 또는 e 5 구독은 Office 365 E3 필요합니다. 해당 요금제에 가입한 상태 고급 eDiscovery 시도 하려는 하지 경우에 [Office 365 Enterprise e 5의 평가판 등록](https://go.microsoft.com/fwlink/p/?LinkID=698279)할 수 있습니다. 
  
이 섹션에서는 고급 eDiscovery 프로세스 모듈의 기능에 설명 합니다. 
  
파일 데이터 외에도 각 사례에 대 한 저장 및 eDiscovery 고급에 파일 형식, 확장, 위치 또는 경로, 만든 날짜 및 시간, 작성자, 더불어, 및 제목, 등의 메타 데이터를 로드 수 있습니다. 기본 파일을 로드 하는지 일부 메타 데이터가 등 고급 eDiscovery 하 여 계산 됩니다. 
  
고급 eDiscovery 시스템 거의 중복 된 그룹화 또는 관련성 점수와 같은 메타 데이터 값을 제공합니다. 관리자가 파일 주석 등의 다른 메타 데이터를 추가할 수 있습니다. 
  
## <a name="running-process"></a>실행 중인 프로세스

> [!NOTE]
> 일괄 처리 번호는 파일의 추적할 수 있도록 프로세스 중 파일에 할당 됩니다. 일괄 처리 수에는 재처리 옵션에 대 한 프로세스 일괄 처리를 식별할 수 있습니다. 일괄 처리 번호와 세션으로 필터링에 대 한 추가 필터를 수 있습니다. 
  
프로세스를 실행 하려면 다음 단계를 수행 합니다.
  
1. [Office 365 보안 열고 &amp; 준수 센터](go-to-the-securitycompliance-center.md) 합니다. 
    
2. 이동 **검색 &amp; 조사** \> **eDiscovery** 를 누른 다음 **고급 eDiscovery로 이동**합니다.
    
3. 고급 eDiscovery에 표시 된 **경우** 페이지에서 적절 한 대/소문자를 선택 하 고 **대/소문자로 이동**을 클릭 합니다.
    
4. **Prepare** 에 \> **프로세스** \> **설치 프로그램**을 사용할 수 있는 컨테이너의 목록에서 컨테이너를 선택 합니다.
    
    ![대/소문자를 검색 결과 추가 하는 프로세스를 클릭 합니다.](media/50bdc55c-d378-4881-b302-31ef785fa359.png)
  
5. 시드 파일 또는 미리 태그가 지정 된 파일로 컨테이너를 추가 하려는 경우에 **고급 설정...** 을 클릭 합니다. 
    
    시드 파일을 사용 하 여 낮은 다양성와 문제에 대 한 교육을 신속 하 (일반적으로 2% 이하의). 시드 파일에 대 한 것이 좋습니다 다양 한 명확 하 게 관련 파일을 선택 하 고 처리에 대 한 문제 (너무 많은 시드 파일 관련성 결과 skew 수) 당 20 ~ 50 시드 합니다. 동일한 통화를 사용자가 문제를 교육 할지 시드 파일을 검토 해야 합니다.
    
    관련성 교육을 자동화 하려면 미리 태그가 지정 된 파일을 사용 합니다. 최소한 1, 500 파일 태그를 지정 하 고 관련성에 추가 된 모음과 동일 하 게 관련 아닌 파일에 관련 된 비율을 유지 해야 합니다. 이러한 파일을 수동으로 태그를 지정, 하 고 태그의 품질에 판단 해야 합니다.
    
    ![배치 파일을 처리 하기 위한 스크린샷의 고급 설정 페이지](media/3c25cb78-4484-41e5-bd34-3753c7ab6cf2.jpg)
  
  - **시드** 섹션: 
    
    **시드 파일로 표시** 시드 파일로 컨테이너를 표시할지를 선택 합니다. **문제에 대 한** 드롭다운 목록에서 문제 당 할당 하도록 선택할 필요는 있습니다. **태그** 드롭다운 메뉴에서 **다음과 관련 됨** 또는 **관련이 없는** 중 하나를 선택 합니다. 
    
    > [!NOTE]
    > **시드**으로 파일을 설정한 후 **태그가 지정 된 사전**으로 표시할 수 없습니다. 
  
  - 섹션에서 다음 **미리 태그가 지정 된 파일** . 
    
    **미리 태그가 지정 된 파일로 표시** 미리 태그가 지정 된 파일로 컨테이너를 표시할지를 선택 합니다. **문제에 대 한** 드롭다운 목록에서 문제 당 할당 해야하는 합니다. **태그** 드롭다운 메뉴에서 **다음과 관련 됨** 또는 **관련이 없는** 중 하나를 선택 합니다. 
    
    > [!NOTE]
    > **태그가 지정 된 사전**으로 파일을 설정한 후 **시드**으로 표시할 수 없습니다. 
  
  - **전자 메일에 태그 지정** 섹션입니다. 시드 또는 태그가 지정 된 사전으로 표시할지는 처리 된 전자 메일의 부분 집합입니다. 
    
6. 먼저, **프로세스**를 클릭 합니다. 완료 되 면 프로세스 결과가 표시 됩니다.
    
7. (선택 사항) 추가 하 고 **Custodians** 에 더불어 이름을 편집할 수 특정 더불어를 데이터 원본에 할당 해야하는 경우 \> **Custodians** 에서 **관리** 하 고 할당 custodians \> **할당**합니다. 
    
대/소문자를 추가 하는 경우을 처리할 수 있습니다 다시 합니다.
  
## <a name="see-also"></a>참고 항목

[Office 365 Advanced eDiscovery](office-365-advanced-ediscovery.md)
  
[프로세스 모듈 결과 보기](view-process-module-results-in-advanced-ediscovery.md)

