---
title: Office 365 Advanced eDiscovery에서 분석 옵션 설정
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
ms.assetid: f6cd6588-f6b6-424a-a9ab-3782b842faee
description: '유사 복제, 전자 메일 스레드 및 테마를 포함 하 여 Office 365 Advanced eDiscovery의 분석 프로세스에 대 한 옵션을 설정 하는 단계를 검토 합니다.  '
ms.openlocfilehash: 4689638f5cebe2ef17fcea5a13ff06edc29e5930
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32260902"
---
# <a name="set-analyze-options-in-office-365-advanced-ediscovery"></a>Office 365 Advanced eDiscovery에서 분석 옵션 설정

> [!NOTE]
> Advanced eDiscovery를 사용하려면 Office 365 E3의 고급 준수 추가 기능이나 조직을 위한 E5 구독이 필요합니다. 이 요금제가 없는 상태에서 Advanced eDiscovery를 사용하려는 경우에는 [Office 365 Enterprise E5 평가판을 등록](https://go.microsoft.com/fwlink/p/?LinkID=698279)할 수 있습니다. 
  
고급 eDiscovery에서 분석을 실행 하기 전에 분석 옵션을 설정 합니다.
  
## <a name="set-analyze-options"></a>분석 옵션 설정

** \> 준비 분석** \> **설정을**엽니다. 다음 창이 표시 됩니다.
  
![세트 옵션 분석](media/c3ec7a92-8484-4812-b98c-aa3eb740e5b7.png)
  
 **유사-중복 및 전자 메일 스레드** 분석을 실행 하려면이 확인란을 선택 합니다. 이 옵션은 기본적으로 선택되어 있습니다. 
  
 **문서 유사성** 거의 모든 부분 복제 임계값을 입력 하거나 기본값인 65%를 그대로 사용 합니다. 
  
 **테마** 모든 파일을 처리 하 고 테마를 할당 하려면이 확인란을 선택 합니다. 이 확인란은 기본적으로 선택 되어 있지 않습니다. 테마 처리를 수행 하려면 다음 옵션을 입력 합니다.
  
- **최대 테마 수** 만들 테마 수 값을 입력 하거나 선택 합니다. 기본값은 200입니다. 
    
    > [!NOTE]
    > 테마 수를 늘리면 성능에 영향을 미치며 테마를 일반화할 수 있습니다. 테마 수가 높을수록 더 세밀 하 게 표시 됩니다. 예를 들어 50 테마 집합에 "농구, Spurs, Clippers, Lakers"와 같은 테마가 포함 된 경우 300 테마에는 별도의 테마 ("Spurs", "Clippers", "Lakers")가 포함 될 수 있습니다. "농구" 테마에 대 한 인식이 없고 ECA에 대해이 기능을 사용 하는 경우 "농구" 라는 테마를 표시 하는 것이 유용할 수 있습니다. 그러나 처리에 너무 많은 테마가 포함 되어 있는 경우에는 "농구" 라는 단어가 표시 되지 않으며 Spurs 및 Clippers는 시작 하는 데 사용 되는 항목을 나타내는 것이 아니라 더 나은 농구 테마 인지 알 수 없습니다. 
  
- **추천 테마** 테마 처리를 제어 하는 theme 단어를 제안할 수 있습니다. 고급 eDiscovery는 이러한 추천 단어에 집중 하 고 "최대 테마 수" 설정에 따라 하나 이상의 관련 테마를 만들려고 시도 합니다. 
    
    예를 들어 추천 단어가 "computer"이 고 "2"를 "최대 테마 수"로 지정한 경우 Advanced eDiscovery에서는 "computer" 라는 단어와 관련 된 두 테마를 생성 합니다. "컴퓨터 소프트웨어" 및 "컴퓨터 하드웨어"와 같은 두 가지 테마를 사용할 수 있습니다. 
    
    ![추천된 테마 추가](media/06e9ffd3-a76c-423b-b450-9e465eb9a02f.png)
  
1. 제안 된 테마를 보거나 추가 하거나 편집 하려면 **수정을**클릭 합니다.
    
2. 제안 된 **테마** 패널에서 추가 아이콘 **** ![](media/c2dd8b3a-5a22-412c-a7fa-143f5b2b5612.png) 추가 아이콘를 클릭 하 여 테마를 추가 합니다. **제안 테마 추가** 패널에서 단어를 쉼표로 구분 하 여 추가 합니다. 
    
3. **테마 수**에 따라 고급 eDiscovery에서 해당 단어에 대해 생성을 시도할 테마 수를 결정 하는 값 (기본값은 1 테마)을 선택 합니다.
    
4. **저장** 을 클릭 하 고 대화 상자를 닫습니다. 
    
    > [!NOTE]
    > 테마의 총 수에 추천 테마가 포함 되어 있습니다. 제안 된 총 테마는 총 테마를 초과할 수 없습니다. 전체 테마에 대 한 추천 테마가 여러 개 있는 경우 대부분의 테마가 추천 테마에 전용으로 제공 되므로 일부 "novel" 테마만 시스템에서 검색 됩니다. 
  
- **모드** 드롭다운 목록에서 **테마** 옵션을 선택 합니다. 
    
  - **모델 만들기 및 적용**: 파일 세그먼트에서 모델 별로 테마를 계산 하 여 파일 간에 배포 합니다.
    
  - **모델 만들기**: 파일의 세그먼트에서 테마 모델을 계산 합니다. 파일을 나눌 때의 적용 프로세스는 별도로 수행 됩니다.
    
  - **모델 적용**:이 옵션은 모델을 이전에 만들었지만 아직 적용 하지 않은 경우에만 표시 됩니다. 이렇게 하면 테마에 따라 파일이 구분 됩니다.
    
또한 [ignore 텍스트를 설정](set-ignore-text-in-advanced-ediscovery.md) 하 고 분석할 [고급 설정 분석](set-analyze-advanced-settings-in-advanced-ediscovery.md) 을 설정할 수 있습니다. 
  
이러한 옵션을 설정한 후에는 **분석** 을 클릭 하 여 실행 합니다. [보기 분석 결과](view-analyze-results-in-advanced-ediscovery.md) 를 표시 합니다. 
  
## <a name="see-also"></a>참고 항목

[Office 365 Advanced eDiscovery](office-365-advanced-ediscovery.md)
  
[문서 유사성 이해](understand-document-similarity-in-advanced-ediscovery.md)
  
[무시 텍스트 설정](set-ignore-text-in-advanced-ediscovery.md)
  
[고급 설정 설정 분석](set-analyze-advanced-settings-in-advanced-ediscovery.md)
  
[결과 분석 보기](view-analyze-results-in-advanced-ediscovery.md)

