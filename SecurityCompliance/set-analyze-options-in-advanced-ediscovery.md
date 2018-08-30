---
title: Office 365 Advanced eDiscovery 분석 옵션 설정
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
ms.assetid: f6cd6588-f6b6-424a-a9ab-3782b842faee
description: '중복 근처, 전자 메일 스레드 및 테마를 포함 하 여 Office 365 고급 ediscovery에서 분석 프로세스에 대 한 옵션을 설정 하는 단계를 검토 합니다.  '
ms.openlocfilehash: a0ebbadb180321a3094cb1056ed8e0e6500ee66a
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22533489"
---
# <a name="set-analyze-options-in-office-365-advanced-ediscovery"></a>Office 365 Advanced eDiscovery 분석 옵션 설정

> [!NOTE]
> 고급 eDiscovery 조직에 대 한 고급 준수 추가 기능 또는 e 5 구독은 Office 365 E3 필요합니다. 해당 요금제에 가입한 상태 고급 eDiscovery 시도 하려는 하지 경우에 [Office 365 Enterprise e 5의 평가판 등록](https://go.microsoft.com/fwlink/p/?LinkID=698279)할 수 있습니다. 
  
고급 eDiscovery에서 분석을 실행 하기 전에 분석 옵션을 설정 합니다.
  
## <a name="set-analyze-options"></a>분석 옵션 설정

Open **준비 \> 분석** \> **설치**합니다. 다음과 같은 창이 표시 됩니다.
  
![세트 옵션 분석](media/c3ec7a92-8484-4812-b98c-aa3eb740e5b7.png)
  
 **중복 근처 스레드를 전자 메일 및** 분석을 실행 하려는 경우이 확인란을 선택 합니다. 기본적으로 선택 됩니다. 
  
 **문서 다음과 비슷한** Near 중복 임계값을 입력 하거나 65%의 기본값을 적용 합니다. 
  
 **테마** 모든 파일을 처리 하 고 테마 자신에 게 할당 하려면이 확인란을 선택 합니다. 기본적으로이 확인란이 선택 되지 않습니다. 테마 처리를 수행 하려는 경우 다음 옵션을 입력 합니다.
  
- **테마의 최대 개수** 만들려는 테마의 수에 대 한 값을 선택 하거나 입력 합니다. 기본값은 200입니다. 
    
    > [!NOTE]
    > 테마의 수를 늘리면 성능이 될 일반화 하는 테마의 기능에 영향을 줍니다. 테마 수가 많을 수록, 보다 세부적인 됩니다. 예: 50 테마 집합이 "농구, 저비용과, Lakers 전 정가 위"; 테마를 포함 하는 경우 300 테마 별도 테마에 포함 될 수 있습니다. "저비용과", "전 정가 위", "Lakers"입니다. 테마를 인식 하지 "농구" 명의 ECA에 대 한이 기능을 사용 하는 경우 테마 특정인 "농구" 유용할 수 있습니다. 하지만 "농구" 라는 단어를 표시 하지 될 수는 처리 한 너무 많은 테마가 하는 경우 및는 저비용과 및 전 정가 위는 좋은 농구 테마를 검토 하는 대신에 포함할 항목 부팅 되 고 머리에 사용 되는 알 수 있습니다. 
  
- **추천 테마** 테마를 처리 하는 테마를 제어 하는 단어를 제안할 수 있습니다. 고급 eDiscovery 중점적으로 이러한 추천된 단어 및 "테마 수가 Max" 설정에 따라 하나 이상의 관련 된 테마를 만들려고 시도 합니다. 
    
    예, 추천된 단어를 "computer", "테마의 최대 개수"으로 "2"을 지정 하는 경우 고급 eDiscovery "computer" 라는 단어와 관련 된 두 테마를 생성 하려고 합니다. 예 두 테마: "컴퓨터 소프트웨어" 및 "컴퓨터 하드웨어" 있을 수 있습니다. 
    
    ![추천된 테마 추가](media/06e9ffd3-a76c-423b-b450-9e465eb9a02f.png)
  
1. 추가, 편집 또는 보기 제안 된 테마를 하려면 **수정**을 클릭 합니다.
    
2. **추천 테마** 패널에서 **추가**클릭![추가 아이콘](media/c2dd8b3a-5a22-412c-a7fa-143f5b2b5612.png) 아이콘 테마를 추가 합니다. **추가 제안된 테마** 패널에서 쉼표로 구분 하 여 단어를 추가 합니다. 
    
3. **테마의 수**,에서 고급 eDiscovery 합니다 (기본값인 1 테마) 다음이 단어에 대 한 생성 하려고 하는 테마의 수를 결정 하는 값을 선택 합니다.
    
4. **저장** 을 클릭 하 고는 대화 상자를 닫습니다. 
    
    > [!NOTE]
    > 제안 된 테마를 포함 하는 테마의 총 수입니다. 총 제시 테마 총 테마를 초과할 수 없습니다. 총 테마를 기준으로 제안 된 테마 수 없으면 대부분의 테마의 전용으로 사용 됩니다 테마 제안 하기 때문에 몇가지 "소설" 테마 시스템에 의해 검색 됩니다. 
  
- **모드** 드롭다운 목록에서 **테마** 옵션을 선택 합니다. 
    
  - **만들기 모델을 적용 하 고**: 파일의 세그먼트에서 모델을 통해 테마를 계산 하 고 다음 사항을 포함 하는 파일을 분산 합니다.
    
  - **모델 만들기**: 세그먼트의 파일에서 테마 모델을 계산 합니다. 파일을 나눈 적용 프로세스는 나중에 개별적으로 수행 됩니다.
    
  - **적용 모델**:이 옵션은 모델을 이전에 생성 되어 아직 적용 하는 경우에 표시 됩니다. 이 테마에 따라 파일 나눌 됩니다.
    
수도 있습니다 [집합 텍스트를 무시](set-ignore-text-in-advanced-ediscovery.md) 하 고 [고급 설정 분석 설정](set-analyze-advanced-settings-in-advanced-ediscovery.md) 분석에 대 한. 
  
이러한 옵션을 설정한 후에 **분석** 실행을 클릭 합니다. [보기를 분석 결과가](view-analyze-results-in-advanced-ediscovery.md) 표시 됩니다. 
  
## <a name="see-also"></a>참고 항목

[Office 365 Advanced eDiscovery](office-365-advanced-ediscovery.md)
  
[문서 다음과 비슷한 이해 (영문)](understand-document-similarity-in-advanced-ediscovery.md)
  
[무시 텍스트를 설정 합니다.](set-ignore-text-in-advanced-ediscovery.md)
  
[고급 설정 설정 분석](set-analyze-advanced-settings-in-advanced-ediscovery.md)
  
[분석 결과 보기](view-analyze-results-in-advanced-ediscovery.md)

