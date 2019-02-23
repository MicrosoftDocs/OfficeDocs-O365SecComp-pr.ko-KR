---
title: Office 365 Advanced eDiscovery 프로세스 모듈 결과 보기
ms.author: chrfox
author: chrfox
manager: laurawi
ms.date: 9/14/2017
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: c6f016cb-409f-4ae9-911c-1395cf0c86ea
description: '작업 상태 및 프로세스 요약을 포함 하 여 Office 365 Advanced eDiscovery에서 실행 되는 프로세스 모듈의 결과를 찾는 방법에 대해 알아봅니다.  '
ms.openlocfilehash: 0393cde78e559036d92b9ac48245afafc974a8b2
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30218058"
---
# <a name="view-process-module-results-in-office-365-advanced-ediscovery"></a>Office 365 Advanced eDiscovery 프로세스 모듈 결과 보기

**준비** \> **프로세스가** 시작 되 면 진행률과 결과를 볼 수 있습니다. 
  
> [!NOTE]
> Advanced eDiscovery를 사용하려면 Office 365 E3의 고급 준수 추가 기능이나 조직을 위한 E5 구독이 필요합니다. 이 요금제가 없는 상태에서 Advanced eDiscovery를 사용하려는 경우에는 [Office 365 Enterprise E5 평가판을 등록](https://go.microsoft.com/fwlink/p/?LinkID=698279)할 수 있습니다. 
  
## <a name="process-task-status"></a>프로세스 작업 상태

**준비** \> **** 프로세스 \> **결과**에서 페이지에는 현재 상태가 (프로세스가 현재 실행 중인 경우) 또는 다음 예제와 같이 마지막 프로세스 상태 작업 상태가 표시 됩니다.
  
![프로세스 모듈 작업 상태](media/9430f9e7-a4dd-47c7-ac2e-2c6a60fc948b.png)
  
선택한 프로세스 옵션에 따라 표시 되는 작업이 다를 수 있습니다. 
  
- **인벤토리**: 고급 eDiscovery 프로세스를 위해 선택한 모든 파일을 반복 하 고 기본 데이터 수집을 수행 합니다.
    
- **서명 계산**: MD5 디지털 서명을 계산 합니다.
    
- **Compounds 추출**: 복합 파일 (예: PST, ZIP, MSG)에서 내부 또는 포함 된 파일을 재귀적으로 추출 합니다. 추출 된 파일은 사례의 사례 폴더에 저장 됩니다.
    
- **데이터베이스 동기화**: 내부 데이터베이스 프로세스
    
- **파일 복사**: 프로세스 파일을 복사 합니다. 이 작업은 파일 복사 고급 옵션을 선택한 경우에도 항상 표시 됩니다.
    
- **텍스트 추출**: 네이티브 파일이 있는 경우 Advanced eDiscovery는 dtsearch를 사용 하 여 이러한 파일에서 텍스트를 추출 합니다. 이러한 파일의 추출 된 텍스트는 case 폴더에 텍스트 파일로 저장 됩니다.
    
- **메타 데이터 업데이트**: 로드 된 메타 데이터를 처리 합니다. 
    
- **마무리**: 로드 된 사례 파일의 데이터를 종료 하는 내부 처리 (예를 들어 오류 및 성공 파일 식별)입니다. 
    
작업 상태: 작업 완료 후에 표시 됩니다. 작업이 실행 되는 동안 실행 기간이 표시 됩니다.
  
> [!NOTE]
> 완료 된 작업에는 처리를 완료 한 파일, 오류가 발생 한 파일에 대 한 요약도 포함 될 수 있습니다. 
  
> [!TIP]
> "취소"를 선택 하면 프로세스 실행을 중지 하 고 이전 데이터 채우기 또는 저장 처리 된 데이터로 롤백하는 롤백 옵션이 제공 됩니다. Rollback 처리 된 데이터를 모두 지웁니다. 처리 된 데이터를 손실 하지 않으려면 (예: 이러한 파일을 다시 로드 하려는 경우)이 창에서 "취소" 옵션을 선택 하 여 롤백하지 않도록 선택 합니다. 
  
## <a name="process-summary"></a>프로세스 요약

프로세스 \> \> 결과 \> 준비 프로세스 요약에서는 파일 처리 성공 및 오류 결과에 따라 로드 된 파일 결과를 분석 하 여 표시 합니다.
  
이 창은 다음과 같이 가져온 파일 통계를 그래픽으로 표시 합니다.
  
- **프로세스 요약**이 사례에 있는 모든 파일을 누적 합니다.
    
- **프로세스 요약 마지막**: 마지막 세션 또는 작업에서 로드 된 파일입니다. 
    
- **성 계열**: 사례 (있는 경우)의 패밀리 정보
    
- **시드** 파일을 추가 하면 파일에 대해 정의 된 문제 당 시드 파일 수가 나열 됩니다. 
    
    **시드** 파일을 표시 하지 못한 경우에도 해당 됩니다. 
    
- **사전 태그가 지정** 된 파일이 추가 되 면 파일에 대해 정의 된 문제 당 미리 태그가 지정 된 파일의 수가 나열 됩니다. 
    
    **미리 태그가 지정** 된 파일을 표시 하는 데 실패 한 경우에도 해당 됩니다. 
    
![프로세스 모듈 요약](media/2086a691-9e3d-4117-beb2-a5c3a9a4cc94.png)
  
## <a name="process-summary-accumulated-and-last-charts"></a>누적 프로세스 요약 및 마지막 차트

왼쪽 막대에는 원본 + 추출한 파일 (모든 파일)이 포함 되어 있습니다. 
  
처리 된 오른쪽 막대에는 다음이 포함 됩니다.
  
- 로드 오류가 발생 한 파일
    
- 파일을 성공적으로 로드 했으며, 다음을 포함할 수 있습니다. 
    
  - **기존**파일: 이전에 로드 되 고 다시 로드 되는 (중복 항목 포함).
    
  - **텍스트**: 텍스트를 포함 하는 고유한 파일입니다.
    
  - **텍스트가 아닌**경우: 빈 텍스트 파일, 빈 네이티브 텍스트 파일, 기본 텍스트가 아닌 파일 
    
  - **중복**s: 텍스트와 중복 된 파일을 사용 합니다.
    
## <a name="last-process-errors"></a>마지막 프로세스 오류

준비 \> 프로세스 \> 결과 \> 에서 마지막 프로세스 오류가 발생 하면 마지막 세션에 있는 오류 또는 수행 된 작업에 대 한 세부 정보가 표시 됩니다.
  
![프로세스 모듈 오류](media/4771d0f4-4217-445a-9ba4-8b6541c5ad09.png)
  
## <a name="see-also"></a>참고 항목

[Office 365 Advanced eDiscovery](office-365-advanced-ediscovery.md)
  
[프로세스 모듈 실행 및 데이터 로드](run-the-process-module-and-load-data-in-advanced-ediscovery.md)

