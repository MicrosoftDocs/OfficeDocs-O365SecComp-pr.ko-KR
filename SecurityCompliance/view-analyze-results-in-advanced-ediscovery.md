---
title: Office 365 Advanced eDiscovery 분석 결과 보기
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
ms.assetid: 5974f3c2-89fe-4c5f-ac7b-57f214437f7e
description: '표시 된 작업 옵션의 정의를 포함 하 여 Office 365 Advanced eDiscovery에서 분석 프로세스의 결과를 볼 수 있는 위치를 파악 합니다.  '
ms.openlocfilehash: 990bcbb3c6626521d40f7ce057c764200d5047b5
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30218828"
---
# <a name="view-analyze-results-in-office-365-advanced-ediscovery"></a>Office 365 Advanced eDiscovery 분석 결과 보기

> [!NOTE]
> Advanced eDiscovery를 사용하려면 Office 365 E3의 고급 준수 추가 기능이나 조직을 위한 E5 구독이 필요합니다. 이 요금제가 없는 상태에서 Advanced eDiscovery를 사용하려는 경우에는 [Office 365 Enterprise E5 평가판을 등록](https://go.microsoft.com/fwlink/p/?LinkID=698279)할 수 있습니다. 
  
Advanced eDiscovery에서는 아래에 설명 된 것 처럼 다양 한 표시에서 분석 프로세스의 진행률과 결과를 볼 수 있습니다.
  
## <a name="view-analyze-task-status"></a>작업 상태 분석 보기

문제 ** \> 분석 \> \> 결과 작업 상태**에서 분석 프로세스 실행 중 및 이후 상태가 표시 됩니다. 
  
![작업 상태를 분석 합니다.](media/d0372978-ce08-4f4e-a1fc-aa918ae44364.png)
  
표시 되는 작업은 선택한 옵션에 따라 다를 수 있습니다. 
  
- **ND/ET: setup**: 실행을 위한 준비 예를 들면 run 및 case 매개 변수를 설정 합니다.
    
- **nd/ET: nd 계산**: 거의 중복 된 파일 분석을 처리 합니다.
    
- **ND/ET: et 계산**: 전체 전자 메일 집합에 대해 전자 메일 스레드 분석을 수행 합니다.
    
- **ND/ET:** 피벗 및 유사성: pivot과 파일 유사성 처리를 수행 합니다.
    
- **ND/ET: 메타 데이터 업데이트**: 데이터베이스의 파일에 대해 수집 된 새 데이터를 마무리 합니다.
    
- **테마: 테마 계산**: 테마 분석을 실행 합니다. (선택 된 경우에만 표시 됨)
    
- **작업 상태**:이 줄은 작업 완료 후에 표시 됩니다. 작업이 실행 되는 동안 실행 기간이 표시 됩니다.
    
> [!NOTE]
> 유사 중복 항목 및 전자 메일 스레드 (ND 및 ED)의 분석 결과는 처리할 문서 수에 적용 됩니다. 정확 하 게 중복 되는 파일은 포함 하지 않습니다. 
  
## <a name="view-near-duplicates-and-email-threads-status"></a>유사 복제 및 전자 메일 스레드 상태 보기

**대상** 인구 결과에는 대상 모집단의 문서, 전자 메일, 첨부 파일 및 오류 수가 표시 됩니다. 
  
**문서** 결과에는 피벗, 고유 중복 항목 및 정확한 중복 파일 수가 표시 됩니다. 
  
전자 **** 메일 결과에는 포함, 포함 마이너스, 고유 포함 복사본, 그리고 나머지 이메일 메시지의 수가 표시 됩니다. 다양 한 유형의 전자 메일 결과는 다음과 같습니다. 
  
- **포괄**사항: 포함 전자 메일은 전자 메일 스레드의 종료 노드이며 해당 스레드의 이전 기록이 모두 포함 됩니다. 따라서 검토자가 포함 된 전자 메일에 안전 하 게 집중할 수 있으며 스레드의 이전 메시지를 읽지 않아도 됩니다. 
    
- **포괄 빼기**: 포함 메시지의 부모와 연결 된 다른 첨부 파일이 하나 이상 있는 경우 포함 전자 메일은 포괄 값으로 지정 됩니다. 이 컨텍스트에서 상위 용어는 해당 특정 포함 전자 메일에 포함 된 전자 메일 스레드나 대화에서 위쪽에 있는 메시지에 사용 됩니다. 검토자가 포함 된 전자 메일 부모의 콘텐츠를 검토 하는 데에는 필요 하지 않지만 포함 경로 부모와 연결 된 첨부 파일을 검토 하는 것이 유용할 수 있는 신호로 서 수 빼기 표시를 사용할 수도 있습니다. 
    
- **포함 복사본**: 포함 전자 메일이 포함 또는 포함으로 표시 된 다른 메시지의 복사본 인 경우 포괄 복사본으로 지정 됩니다. 즉,이 메시지는 다른 포괄 메시지와 같은 제목 및 본문을 가지 며 같은 노드에 동시에 상주 합니다. 포함 복사본 메시지에는 동일한 콘텐츠가 포함 되므로 일반적으로 검토 프로세스에서이를 생략할 수 있습니다. 
    
- **rest**: 고유한 콘텐츠가 포함 되지 않은 전자 메일을 나타내며, 따라서 이전의 세 범주에 속하지 않습니다. 이러한 전자 메일 메시지는 검토할 필요가 없습니다. 나중에 포함 되는 전자 메일에 없는 첨부 파일이 메시지에 포함 되어 있는 경우에는 첨부 파일을 검토 해야 할 수 있습니다. 이는 스레드 내에 포함 마이너스 전자 메일이 있다는 것을 나타냅니다.
    
**첨부 파일** 결과에는 고유 하거나 중복 된 형식에 따라 첨부 파일 수가 표시 됩니다. 
  
![전자 메일 스레드 및 중복 근처](media/54491303-0ee3-4739-b42e-d1ee486842fd.png)
  
## <a name="see-also"></a>참고 항목

[Office 365 Advanced eDiscovery](office-365-advanced-ediscovery.md)
  
[문서 유사성 이해](understand-document-similarity-in-advanced-ediscovery.md)
  
[분석 옵션 설정](set-analyze-options-in-advanced-ediscovery.md)
  
[무시 텍스트 설정](set-ignore-text-in-advanced-ediscovery.md)
  
[고급 설정 분석 설정](view-analyze-results-in-advanced-ediscovery.md)

