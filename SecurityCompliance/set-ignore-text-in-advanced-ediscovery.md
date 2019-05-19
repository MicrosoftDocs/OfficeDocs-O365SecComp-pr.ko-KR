---
title: Office 365 Advanced eDiscovery에서 분석에 대 한 텍스트 무시 옵션 설정
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
ms.assetid: 44055727-56e8-42d7-9dc3-fb942f3901cc
description: 'Office 365 Advanced eDiscovery에서 Analyze 및 Process 모듈을 사용할 때 특정 텍스트를 무시 하는 규칙을 정의 하는 방법을 알아봅니다.  '
ms.openlocfilehash: 70d9879f1cb6b3def06ff978fc2f7fa8f20a92f0
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/17/2019
ms.locfileid: "34156680"
---
# <a name="set-ignore-text-option-for-analyze-in-office-365-advanced-ediscovery"></a>Office 365 Advanced eDiscovery에서 분석에 대 한 텍스트 무시 옵션 설정

> [!NOTE]
> Advanced eDiscovery를 사용하려면 Office 365 E3의 고급 준수 추가 기능이나 조직을 위한 E5 구독이 필요합니다. 이 요금제가 없는 상태에서 Advanced eDiscovery를 사용하려는 경우에는 [Office 365 Enterprise E5 평가판을 등록](https://go.microsoft.com/fwlink/p/?LinkID=698279)할 수 있습니다. 
  
텍스트 무시 기능은 분석 (거의 중복, 전자 메일 스레드, 테마) 및 관련성에 따라 다음과 같은 고급 eDiscovery 모듈 전체 또는 일부에 적용할 수 있습니다. 무시 된 텍스트는 관련성이 있는 파일에 표시 되지 않으며, 분석/계산은 무시 되는 텍스트를 무시 합니다.
  
이미 실행 했던 모듈에 대해 무시 텍스트 기능이 이전에 정의 된 경우에는 텍스트 무시 설정이 이제 수정 되지 않도록 보호 됩니다. 그러나 관련성 모듈에 대 한 텍스트 무시 기능은 언제 든 지 변경 될 수 있습니다.
  
## <a name="how-ignore-text-filters-are-applied"></a>무시 텍스트 필터를 적용 하는 방법

여러 Ignore 텍스트 필터는 입력 한 순서 대로 적용 됩니다. 적용 되는 순서를 변경 하려면 삭제 하 고 원하는 순서 대로 다시 입력 해야 합니다.
  
예를 들어 텍스트 콘텐츠가 "DAVE BOB ALICE 고 전날" 인 경우 다음은 무시 텍스트 항목과 결과의 예입니다.
  
||||
|:-----|:-----|:-----|
|**텍스트 항목 무시** <br/> |**==\>** <br/> |**결과** <br/> |
|"ALICE", "BOB의가을"  <br/> |==\>  <br/> |"DAVE 전날"  <br/> |
|"ALICE", "BOB ALICE 고 대"  <br/> |==\>  <br/> |"DAVE BOB 고 전날"  <br/> |
   
첫 번째 무시 텍스트가 적용 된 후에 문자열이 검색 되지 않으므로 두 번째 Ignore 텍스트 항목은 구현 되지 않습니다.
  
## <a name="use-regular-expressions-when-defining-ignore-text"></a>텍스트 무시를 정의할 때 정규식 사용

정규식은 무시 텍스트를 정의할 때 사용할 수 있습니다. 다음은 정규식 구문과 사용 방법의 예입니다.
  
- 시작 부분에서 줄 끝까지 텍스트를 제거 하려면 다음을 수행 합니다.
    
     `Begin(.*)$`
    
    여기에서 "Begin"은 줄에서이 문자열의 초기 항목입니다.
    
    예를 들어 다음과 같은 텍스트를 예로 들 있습니다.
    
    **"이 문장이 나 첫 번째 줄입니다.**
    
    **두 번째 문장이 며 두 번째 줄이 됩니다. "**
    
    정규식 first (.\*) $의 결과는 다음과 같습니다.
    
    **"이는**
    
    **두 번째 문장이 며 두 번째 줄이 됩니다. "**
    
- 전자 메일 스레드 끝에 자동으로 삽입 되는 고 지 사항 및 법률 문서를 제거 하려면:
    
     `Begin(.|\s)*End`
    
    여기서 "Begin" 및 "End"는 줄 바꿈된 텍스트 단락의 시작과 끝에 있는 고유한 문자열입니다. 
    
    예를 들어 다음 정규식은 Begin 및 End 문자열 사이에 있는 전자 메일 스레드에 있는 고 지 사항 및 법률 자문을 제거 합니다.
    
    **이 메시지에는 기밀 정보 (. | \s)\*확인이 필요한 경우 하드 카피 버전을 요청 하세요.**
    
- 고 지 사항 (특수 문자 포함)을 제거 하려면 
    
    예를 들어 다음 텍스트 (고 지 사항이 x로 표시 됨)에 대해 다음을 수행 합니다. 
    
    **/\*\이 메시지에는 기밀 정보가 포함 되어 있습니다. xxxx xxxx**
    
    **xxxx xxxx xxxx xxxx xxxx xxxx xxxx**
    
    **xxxx xxxx 확인이 필요한 경우에는 하드 카피 버전을 요청 하세요. /\*\**
    
    위의 부인 내용을 제거 하는 정규식은 다음과 같습니다. 
    
    **\/\\*\\이 메시지에는 기밀\.정보 (. | \s)\* 확인이 필요한 경우 하드 카피 버전\. 을 요청 하세요.\/\\*\\**
    
- 정규식 규칙:
    
  - 공백을 제외 하 고 알파벳의 일부가 아닌 모든 문자, "_" 및 "-"은 앞에 "가와 야 합니다\".
    
  - 일반 eExpression 필드의 길이에는 제한이 없습니다.
    
> [!TIP]
> 정규식의 자세한 설명과 자세한 내용은 [정규식 언어-빠른 참조](https://msdn.microsoft.com/en-us/library/az24scfc%28v=vs.110%29.aspx)를 참조 하십시오. 
  
## <a name="define-ignore-text-rule"></a>무시 텍스트 규칙 정의

1. 분석 ** \> 분석 옵션 \> 관리** 탭의 **텍스트 무시** 섹션에서 **+** 아이콘을 클릭 하 여 규칙을 추가 합니다. 
    
2. **Ignore 텍스트 추가** 대화 상자의 **이름** 필드에 무시 텍스트 규칙의 이름을 입력 합니다. 
    
    ![무시 하는 텍스트 추가](media/98e5129b-2667-4692-86fa-2d0117187a7f.png)
  
3. **텍스트** 상자에 무시할 텍스트를 입력 합니다. 텍스트 필드에 무제한의 문자를 사용할 수 있습니다. 
    
    > [!TIP]
    > 위의 창에 표시 된 것 처럼 전구 **** 를 클릭 하 여 Ignore 텍스트 규칙에 대 한 일반적인 구문 지침을 확인 합니다. 
  
4. 필요한 경우 **대/소문자 구분** 확인란을 선택 합니다. 
    
5. **적용 대상** 목록에서 정의를 적용할 고급 eDiscovery 모듈을 선택 합니다. 
    
6. 예제 텍스트에 대 한 테스트를 실행 하려면 **입력** 텍스트 상자에 예제 텍스트를 입력 하 고 **테스트**를 클릭 합니다. 결과가 **출력** 텍스트 상자에 표시 됩니다. 
    
7. **확인** 을 클릭 하 여 무시 텍스트 규칙을 저장 합니다. 정의 된 Ignore 텍스트 규칙이 표시 됩니다. 
    
    ![무시 설정 텍스트 이름](media/3a788ac3-4a1c-46c9-89bd-7ff32d68ce23.png)
  
## <a name="see-also"></a>참고 항목

[Office 365 Advanced eDiscovery](office-365-advanced-ediscovery.md)
  
[문서 유사성 이해](understand-document-similarity-in-advanced-ediscovery.md)
  
[분석 옵션 설정](set-analyze-options-in-advanced-ediscovery.md)
  
[고급 설정 분석 설정](set-analyze-advanced-settings-in-advanced-ediscovery.md)
  
[분석 결과 보기](view-analyze-results-in-advanced-ediscovery.md)

