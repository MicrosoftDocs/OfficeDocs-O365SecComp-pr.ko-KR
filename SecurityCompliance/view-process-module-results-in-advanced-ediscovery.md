---
title: Office 365 Advanced eDiscovery 프로세스 모듈 결과 보기
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
ms.assetid: c6f016cb-409f-4ae9-911c-1395cf0c86ea
description: '작업 상태 및 요약 프로세스를 포함 하 여 Office 365 고급 eDiscovery에서 실행 하는 프로세스 모듈의 결과 확인 하는 방법에 알아봅니다.  '
ms.openlocfilehash: 01093b0230aaf78ab7ccf1235f0874a0b69aa1bd
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22532913"
---
# <a name="view-process-module-results-in-office-365-advanced-ediscovery"></a>Office 365 Advanced eDiscovery 프로세스 모듈 결과 보기

**Prepare** 후 \> **프로세스** 를 시작, 진행 및 결과 볼 수 있습니다. 
  
> [!NOTE]
> 고급 eDiscovery 조직에 대 한 고급 준수 추가 기능 또는 e 5 구독은 Office 365 E3 필요합니다. 해당 요금제에 가입한 상태 고급 eDiscovery 시도 하려는 하지 경우에 [Office 365 Enterprise e 5의 평가판 등록](https://go.microsoft.com/fwlink/p/?LinkID=698279)할 수 있습니다. 
  
## <a name="process-task-status"></a>프로세스 작업 상태

**Prepare** 에 \> **프로세스** \> **결과**얻으려면이 페이지에 표시 현재 상태 (프로세스는 현재 실행 중인 경우) 또는 마지막 프로세스 상태 작업 상태는 다음 예제와 같이 합니다.
  
![프로세스 모듈 작업 상태](media/9430f9e7-a4dd-47c7-ac2e-2c6a60fc948b.png)
  
표시 되는 작업은 선택한 프로세스 옵션에 따라 달라질 수 있습니다. 
  
- **재고**: 고급 eDiscovery 프로세스에 대해 선택 된 모든 파일을 반복 하 고 기본 데이터 수집을 수행 합니다.
    
- **Calculate 서명**: MD5 디지털 서명을 계산 합니다.
    
- **복합어 추출**: 복합 파일 (예: PST, ZIP, MSG)에서 재귀적으로 파일을 추출한 내부 또는 포함 합니다. 추출 된 파일은 대/소문자의 경우 폴더에 저장 됩니다.
    
- **동기화 데이터베이스**: 내부 데이터베이스 프로세스입니다.
    
- **파일 복사**: 파일 복사본 처리 합니다. 이 작업은 고급 복사본 파일 옵션을 선택 하는 경우에 항상 표시 됩니다.
    
- **텍스트 추출**: 네이티브 파일이 있을 때 고급 eDiscovery DTSearch를 사용 하 여 이러한 파일에서 텍스트를 추출 합니다. 이러한 파일의 압축 푼된 텍스트 사례 폴더에 있는 텍스트 파일로 저장 됩니다.
    
- **메타 데이터를 업데이트**: 로드 된 메타 데이터를 처리 합니다. 
    
- **Finalizing**: 데이터의 작업을 완료 하는 내부 처리 로드 사례 파일 (오류 및 성공 파일을 식별 등). 
    
작업 상태: 작업 완료 후 표시 합니다. 작업을 실행 하는 동안 실행된 지속 시간 표시 됩니다.
  
> [!NOTE]
> 완료 된 작업 처리를 완료 하는 파일 또는 오류와 함께 파일에 대 한 합계를 포함할 수도 있습니다. 
  
> [!TIP]
> "취소" 프로세스 실행을 중지 하 고 롤백할 이전 데이터 생성기를 롤백 옵션을 제공 하거나 처리 된 데이터를 저장 합니다. 롤백 처리 된 모든 데이터를 지웁니다. 처리 된 데이터를 롤백할 하지 않도록 선택 하려면이 창에서 선택 된 "취소" 옵션 (예: 이러한 파일을 다시 로드 하려는) 손실 될 경우 하는 경우 
  
## <a name="process-summary"></a>프로세스 요약

Prepare에 \> 프로세스 \> 결과 \> 프로세스 요약, 로드 된 파일 결과 분석 하 여 성공적인 파일 처리 및 오류 결과 따라 표시 됩니다.
  
하는 창을 다음과 같이 가져온된 파일 통계를 그래픽으로 표시를 제공 합니다.
  
- **프로세스 요약 누적**d: 모든 경우에 파일입니다.
    
- **마지막 요약 처리**: 파일 마지막 세션 또는 동작에서 로드 됩니다. 
    
- **제품군 마지막**: (해당 되는 경우)의 경우에서 제품군 정보입니다.
    
- **시드** 파일 추가 된 경우 파일에 대해 정의 된 문제 당 시드 파일 수가 나와 있습니다. 
    
    **시드** 파일의 표시에 실패 한 경우는 또한 기록 됩니다. 
    
- **미리 태그가 지정 된** 파일 추가 된 경우 사전 태그가 지정 된 파일의 수는 파일에 대해 정의 된 문제 당 나열 됩니다. 
    
    **미리 태그가 지정 된** 파일의 표시에 실패 한 경우는 또한 기록 됩니다. 
    
![프로세스 모듈 요약](media/2086a691-9e3d-4117-beb2-a5c3a9a4cc94.png)
  
## <a name="process-summary-accumulated-and-last-charts"></a>프로세스 요약 누적 성과 차트

왼쪽된 표시줄 포함 원본 + 압축 푼된 파일: 모든 파일은 찾을 수 있습니다. 
  
오른쪽 가로 막대형, 처리를 포함 합니다.
  
- 파일 로드 오류
    
- 성공적으로 로드 하는 파일을 포함 될 수 있습니다. 
    
  - **기존**: 파일 전에 로드 된 하 고 지금 다시 (포함 하 여 중복) 로드 됩니다.
    
  - **텍스트**: 텍스트와 고유한 파일입니다.
    
  - **비 텍스트**: 텍스트 파일, 빈 기본 텍스트 파일, 네이티브 비 텍스트 파일을 비웁니다. 
    
  - **중복**s: 중복 파일을 텍스트입니다.
    
## <a name="last-process-errors"></a>마지막 프로세스 오류

Prepare에 \> 프로세스 \> 결과 \> 마지막 프로세스 오류, 작업을 수행 하는 마지막 세션에서 오류에 대 한 세부 정보 표시 됩니다.
  
![프로세스 모듈 오류](media/4771d0f4-4217-445a-9ba4-8b6541c5ad09.png)
  
## <a name="see-also"></a>참고 항목

[Office 365 Advanced eDiscovery](office-365-advanced-ediscovery.md)
  
[프로세스 모듈을 실행 하 고 데이터 로드](run-the-process-module-and-load-data-in-advanced-ediscovery.md)

