---
title: Office 365 Advanced eDiscovery 분석 결과 보기
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
ms.assetid: 5974f3c2-89fe-4c5f-ac7b-57f214437f7e
description: '표시 된 작업 옵션의 정의 포함 하 여 Office 365 고급 ediscovery에서 분석 프로세스의 결과 볼 수 있는 위치를 이해 합니다.  '
ms.openlocfilehash: 8f1de53e5548c8721f8fbfdb83374edb18379114
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22533884"
---
# <a name="view-analyze-results-in-office-365-advanced-ediscovery"></a>Office 365 Advanced eDiscovery 분석 결과 보기

> [!NOTE]
> 고급 eDiscovery 조직에 대 한 고급 준수 추가 기능 또는 e 5 구독은 Office 365 E3 필요합니다. 해당 요금제에 가입한 상태 고급 eDiscovery 시도 하려는 하지 경우에 [Office 365 Enterprise e 5의 평가판 등록](https://go.microsoft.com/fwlink/p/?LinkID=698279)할 수 있습니다. 
  
고급 eDiscovery의 진행 상황 및 분석 프로세스에 대 한 결과에서 볼 수 있습니다 다양 한 표시 아래에서 설명 합니다.
  
## <a name="view-analyze-task-status"></a>분석 작업 상태 보기

**준비 \> 분석 \> 결과 \> 상태 작업**, 하는 동안 및 분석 프로세스 실행 된 후에 상태가 표시 됩니다. 
  
![작업 상태를 분석 합니다.](media/d0372978-ce08-4f4e-a1fc-aa918ae44364.png)
  
표시 되는 작업은 선택한 옵션에 따라 달라질 수 있습니다. 
  
- **ND/ET: 설치**: 예 실행을 위한 준비, 실행 및 사례 매개 변수를 설정 합니다.
    
- **ND/ET: ND 계산**: 파일의 프로세스 거의 중복 된 분석 합니다.
    
- **ND/ET: ET 계산**: 전체 전자 메일 설정에 대 한 분석 전자 메일 스레드를 수행 합니다.
    
- **ND/ET: 위치별 및 유사점**: 피벗 및 파일 다음과 비슷한 처리를 수행 합니다.
    
- **ND/ET: 메타 데이터 업데이트**: 데이터베이스의 파일에 대해 수집 된 새 데이터 작업을 완료 합니다.
    
- **테마: 테마 계산**: 테마 분석을 실행 합니다. (선택 하는 경우에 표시 됩니다.)
    
- **작업 상태**: 작업 완료 후이 줄이 표시 됩니다. 작업을 실행 하는 동안 실행된 지속 시간 표시 됩니다.
    
> [!NOTE]
> 중복 근처 및 전자 메일 스레드 (ND 및 ED) 분석 결과 처리할 수에 문서 수에 적용 됩니다. 정확 하 게 중복 파일을 포함 하지는 않습니다. 
  
## <a name="view-near-duplicates-and-email-threads-status"></a>중복 근처 및 전자 메일 스레드 상태 보기

**대상** 모집단 결과 대상 모집단의 문서, 전자 메일, 첨부 파일 및 오류 수를 표시 합니다. 
  
**문서** 결과 위치별, 고유 근처-중복 되는 값을 정확 하 게 중복 된 파일의 수를 표시 합니다. 
  
**전자 메일** 결과 (포함), 고유 (포함) 복사본을 뺀 값 사이의 수 및 전자 메일 메시지의 나머지 부분을 표시합니다. 전자 메일 결과의 다른 유형은 다음과 같습니다. 
  
- **포괄 시간**: (포함) 전자 메일에서 전자 메일 스레드 종료 노드 및 해당 스레드의 모든 이전 기록을 포함 합니다. 따라서 검토자 스레드에서 이전 메시지를 읽을 필요 없이 (포함) 전자 메일에 안전 하 게 집중할 수 있습니다. 
    
- **빼기 포괄 시간**: 하나 이상의 다른 첨부 파일 포함 메시지의 상위와 관련 된 경우 (포함) 전자 메일 (포함) 빼기도 지정 됩니다. 이 상황에 맞는, 부모 위쪽으로 전자 메일 스레드 또는 대화에 있는 메시지에 사용 되는 용어는 특정 (포함) 전자 메일에 포함 합니다. 검토자는 (포함) 전자 메일 학부모의 내용을 검토 하는 데 필요한 수, 있지만 유용할 수 있습니다 (포함) 경로 부모와 연결 된 첨부 파일을 검토 하려면 상태가 표시 한 신호로 뺀 값 사이의 사용할 수 있습니다. 
    
- **복사본 (포함)**: (포함) 전자 메일 (포함) 복사본 다른 메시지의 복사본 경우 표시 (포함) 또는 빼기 (포함)으로 지정 됩니다. 즉,이 메시지에 동일한 제목 및 본문 포함 하는 다른 메시지로 하 여 이와 같이 동일한 노드에 있는 공동 합니다. 동일한 콘텐츠를 포함 하는 (포함) 복사본 메시지, 때문에 자신이 일반적으로 건너뛸 수 있습니다는 검토 과정에서. 
    
- **나머지**:이 모든 고유한 콘텐츠를 포함 하지 않습니다 하 고 이전 세 범주 중 하나에 속합니다 하지는 전자 메일을 나타냅니다. 이러한 전자 메일 메시지를 검토 필요가 없습니다. 나중에 포함 되는 메일에 첨부 파일을 포함 하는 메시지를 첨부 파일을 검토 하 필요할 수 있습니다. 이 전자 메일 스레드 내에서 뺀 값 사이의의 있는지 여부에 의해 표시 됩니다.
    
**첨부 파일** 결과 등으로 고유 유형 및 중복 되는 값에 따라 첨부 파일의 수를 표시 합니다. 
  
![전자 메일 스레드 및 중복 근처](media/54491303-0ee3-4739-b42e-d1ee486842fd.png)
  
## <a name="see-also"></a>참고 항목

[Office 365 Advanced eDiscovery](office-365-advanced-ediscovery.md)
  
[문서 다음과 비슷한 이해 (영문)](understand-document-similarity-in-advanced-ediscovery.md)
  
[분석 옵션 설정](set-analyze-options-in-advanced-ediscovery.md)
  
[텍스트를 무시 하는 설정](set-ignore-text-in-advanced-ediscovery.md)
  
[고급 설정 설정 분석](view-analyze-results-in-advanced-ediscovery.md)

