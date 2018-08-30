---
title: Office 365 Advanced eDiscovery에서 분석에 대한 텍스트 무시 옵션 설정
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
ms.assetid: 44055727-56e8-42d7-9dc3-fb942f3901cc
description: 'Office 365 고급 eDiscovery의 분석 및 프로세스 모듈을 사용 하는 경우 특정 텍스트를 무시 하도록 규칙을 정의 하는 방법에 알아봅니다.  '
ms.openlocfilehash: eb7e7052979087b7dba98aac3b0c9ab75ec0d02a
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22533541"
---
# <a name="set-ignore-text-option-for-analyze-in-office-365-advanced-ediscovery"></a>Office 365 Advanced eDiscovery에서 분석에 대한 텍스트 무시 옵션 설정

> [!NOTE]
> 고급 eDiscovery 조직에 대 한 고급 준수 추가 기능 또는 e 5 구독은 Office 365 E3 필요합니다. 해당 요금제에 가입한 상태 고급 eDiscovery 시도 하려는 하지 경우에 [Office 365 Enterprise e 5의 평가판 등록](https://go.microsoft.com/fwlink/p/?LinkID=698279)할 수 있습니다. 
  
다음과 같은 고급 eDiscovery 모듈 중 하나 또는 모두에 텍스트를 무시 기능을 적용할 수 있습니다: (근처-중복 되는 값, 전자 메일 스레드 테마)를 분석 하 고 관련성 합니다. 무시 텍스트 관련성을에 표시 되는 파일에 표시 되지 않으며 분석/계산 무시 텍스트를 삭제 합니다.
  
텍스트를 무시 기능이 이미 실행 되는 모듈에 대 한 이전에 정의 된 경우 텍스트를 무시 설정은 수정 되지 이제 보호 됩니다. 그러나 관련성 모듈에 대 한 텍스트를 무시 기능 언제 든 지 여전히 변경할 수 있습니다.
  
## <a name="how-ignore-text-filters-are-applied"></a>텍스트를 무시 필터가 적용 되는 방법

여러 무시 텍스트 필터는 입력 된 순서로 적용 됩니다. 적용 되는 순서를 변경 하려면 자신이 해야 삭제 되어 원하는 순서로 다시 입력 합니다.
  
예: 텍스트 콘텐츠가 경우: "DAVE BOB ALICE CAROL EVE"는 다음과 같은 항목 텍스트를 무시 하 고 결과의 샘플:
  
||||
|:-----|:-----|:-----|
|**텍스트 항목을 무시 합니다.** <br/> |**==\>** <br/> |**결과** <br/> |
|"ALICE", "CAROL BOB"  <br/> |==\>  <br/> |"DAVE EVE"  <br/> |
|"ALICE", "ALICE BOB CAROL"  <br/> |==\>  <br/> |"DAVE BOB CAROL EVE"  <br/> |
   
두번째 무시 텍스트 항목에는 첫번째 무시 텍스트가 적용 된 후에 문자열이 이와 같이 발견 되지 않으면 때문에 구현 되지 않았습니다.
  
## <a name="use-regular-expressions-when-defining-ignore-text"></a>텍스트를 무시를 정의할 때 정규식을 사용 하 여

정규식 무시 텍스트를 정의할 때 사용할 수 있도록 지원 합니다. 다음은 정규식 구문 및 사용법의 예입니다.
  
- 제거 하려면 (무시) 텍스트 줄의 끝까지 시작에서:
    
     `Begin(.*)$`
    
    여기서 "Begin"는 줄에서이 문자열의 초기 항목입니다.
    
    예: 다음 텍스트:
    
    **"이 고 첫 문장 첫 줄**
    
    **이 두번째 문장 및 둘째 줄 "**
    
    정규식 first(.\*) $ 발생 합니다.
    
    **"This is**
    
    **이 두번째 문장 및 둘째 줄 "**
    
- 법적 고 지 사항 및 전자 메일 스레드의 끝에 자동으로 삽입 된 법률 정보를 제거 하는 방법
    
     `Begin(.|\s)*End`
    
    여기서 "시작" 및 "종료"는 겹쳐진된 텍스트 단락의 시작과 끝에 고유한 문자열입니다. 
    
    예 다음 정규식 법적 고 지 사항 및 전자 메일 스레드 Begin 및 End 문자열 사이에서 있던 법률 정보 제거 됩니다.
    
    **기밀 정보를 포함 하는이 메시지 (. | \s)\*확인이 필요 하면 하드 카피 버전을 요청 하십시오**
    
- 제거 하려면 (특수 문자를 포함 하 여) 하는 고 지 사항: 
    
    예 (x 하 여 여기에 표시 되 고 지 사항)와 다음 텍스트: 
    
    **/\*\ \이 메시지는 기밀 정보를 포함합니다. 이며 이며**
    
    **이며 이며 이며 이며 이며 이며 이며**
    
    **이며 이며 확인이 필요한 경우에 하드 카피 버전을 요청 하십시오. /\*\**
    
    위의 고 지 사항은 제거 하는 정규식 해야 합니다. 
    
    **\/\\*\\기밀 정보를 포함 하는이 메시지\.(. | \s)\* 확인이 필요 하면 하드 카피 버전을 요청 하십시오\.\/\\*\\**
    
- 정규식 규칙:
    
  - 공간, "_"를 제외 하 고 알파벳의 일부가 아닌 모든 문자 및 "-" 앞에 나와야 "\"합니다.
    
  - 일반 eExpression 필드 길이 제한 없음을된 수 있습니다.
    
> [!TIP]
> 설명과 정규식의 자세한 구문에 대 한 참조: [일반 표현 언어-빠른 참조](https://msdn.microsoft.com/en-us/library/az24scfc%28v=vs.110%29.aspx)합니다. 
  
## <a name="define-ignore-text-rule"></a>텍스트를 무시 규칙 정의

1. **관리 \> 분석 \> 옵션 분석** **무시 텍스트** 섹션에서 탭을 클릭 하는 **+** 규칙을 추가 하는 아이콘 합니다. 
    
2. **이름** 필드에서 **무시 텍스트 추가** 대화 상자에서 텍스트를 무시 규칙에 대 한 이름을 입력 합니다. 
    
    ![무시 하는 텍스트 추가](media/98e5129b-2667-4692-86fa-2d0117187a7f.png)
  
3. **텍스트** 상자에서 무시 되도록 텍스트를 입력 합니다. 텍스트 필드에는 무제한 개수의 문자 수 있습니다. 
    
    > [!TIP]
    > 위쪽 창에 표시 된 것과 같이 무시 텍스트 규칙에 대 한 일반적인 구문을 지침을 보려면 **전구** 클릭 합니다. 
  
4. 원하는 경우 **대/소문자 구분** 확인란을 선택 합니다. 
    
5. **적용 대상** 목록에서 프로그램 정의 적용 하는 고급 eDiscovery 모듈을 선택 합니다. 
    
6. 예제 텍스트에서 실행 하는 테스트를 **입력** 텍스트 상자에 예제 텍스트를 입력 하 고 **테스트**를 클릭 합니다. 결과 **출력** 텍스트 상자에 표시 됩니다. 
    
7. 텍스트를 무시 규칙을 저장 하려면 **확인** 클릭 합니다. 정의 된 텍스트를 무시 규칙이 표시 됩니다. 
    
    ![무시 설정 텍스트 이름](media/3a788ac3-4a1c-46c9-89bd-7ff32d68ce23.png)
  
## <a name="see-also"></a>참고 항목

[Office 365 Advanced eDiscovery](office-365-advanced-ediscovery.md)
  
[문서 다음과 비슷한 이해 (영문)](understand-document-similarity-in-advanced-ediscovery.md)
  
[분석 옵션 설정](set-analyze-options-in-advanced-ediscovery.md)
  
[고급 설정 설정 분석](set-analyze-advanced-settings-in-advanced-ediscovery.md)
  
[분석 결과 보기](view-analyze-results-in-advanced-ediscovery.md)

