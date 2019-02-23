---
title: 키워드 사전 만들기
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 6/29/2018
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Priority
ms.collection: Strat_O365_IP
search.appverid:
- MOE150
- MET150
ms.assetid: c8a95d1b-c3b6-4613-98ab-0331d1872cf3
description: '경우에 따라 중요한 정보를 식별하기 위해 키워드를 검색해야 할 수 있습니다. 이러한 작업은 일반 콘텐츠(예: 의료 관련 커뮤니케이션) 또는 부적절하거나 명시적인 언어를 식별할 때 특히 필요합니다. 중요한 정보 유형에 키워드 목록을 만들 수 있지만 키워드 목록은 크기가 제한되며 생성하거나 편집하기 위해 XML을 수정해야 합니다. 키워드 사전은 키워드를 보다 간편하게 관리할 수 있도록 하며 사전당 최대 100,000개 용어를 지원합니다.'
ms.openlocfilehash: 5dd41223cd3ce5ac45614abcc3926bf5e49fbb5a
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30217378"
---
# <a name="create-a-keyword-dictionary"></a>키워드 사전 만들기

Office 365의 DLP(데이터 손실 방지)는 중요한 정보를 식별, 모니터링 및 보호할 수 있습니다. 경우에 따라 중요한 정보를 식별하기 위해 키워드를 검색해야 할 수 있습니다. 이러한 작업은 일반 콘텐츠(예: 의료 관련 커뮤니케이션) 또는 부적절하거나 명시적인 언어를 식별할 때 특히 필요합니다. 중요한 정보 유형에 키워드 목록을 만들 수 있지만 키워드 목록은 크기가 제한되며 생성하거나 편집하기 위해 XML을 수정해야 합니다. 키워드 사전은 키워드를 보다 간편하게 관리할 수 있도록 하며 사전당 최대 100,000개 용어를 지원합니다.
  
## <a name="basic-steps-to-creating-a-keyword-dictionary"></a>키워드 사전을 만드는 기본 단계

사전의 키워드는 다양한 원본, 파일(예:.csv 또는 .txt 목록)(대부분의 경우), cmdlet에 사용자가 직접 입력한 목록 또는 기존 사전에서 가져올 수 있습니다. 키워드 사전을 만들 때 다음과 같은 동일한 핵심 단계를 따르세요.
  
1. **보안 및 &amp;준수 센터 PowerShell에 연결** - [이 항목](https://docs.microsoft.com/ko-KR/powershell/exchange/office-365-scc/connect-to-scc-powershell/connect-to-scc-powershell)을 참조하세요.
    
2. **의도한 원본의 키워드 정의 또는 로드** - 키워드 사전을 만드는 cmdlet은 쉼표로 구분된 키워드 목록을 수락하므로, 이 단계는 키워드를 가져오는 원본에 따라 약간 다릅니다. 
    
3. **키워드 인코딩** - 일단 로드되고 나면 가져오기 전에 바이트 배열로 변환됩니다. 
    
4. **사용자 사전 만들기** - 이름과 설명을 선택하고 사전을 만듭니다. 
    
## <a name="create-a-keyword-dictionary-from-a-file"></a>파일에서 키워드 사전 만들기

종종 대용량 사전 만들어야 할 경우 다른 원본에서 가져온 파일이나 목록의 키워드를 사용할 수 있습니다. 이 경우 외부 전자 메일에서 걸러내야 할 부적절한 언어 목록이 포함된 키워드 사전을 만듭니다. 먼저 [Office 365 보안 &amp; 및 준수 센터 PowerShell에 연결](https://docs.microsoft.com/ko-KR/powershell/exchange/office-365-scc/connect-to-scc-powershell/connect-to-scc-powershell)해야 합니다.
  
1. 키워드를 텍스트 파일에 복사합니다. 이때 각 키워드를 별도 줄에 복사해야 합니다.
    
2. 텍스트 파일을 유니코드 인코딩으로 저장합니다. 메모장에서 \> **다른 이름으로 저장** \> **인코딩으로** \> **유니코드**를 선택합니다.
    
3. 다음 cmdlet을 실행하여 파일을 변수로 읽습니다.
    
  ```
  $fileData = Get-Content <filename> -Encoding Byte -ReadCount 0
  ```

4. 다음 cmdlet을 실행하여 사전을 만듭니다.
    
  ```
  New-DlpKeywordDictionary -Name <name> -Description <description> -FileData $fileData
  ```

## <a name="modifying-an-existing-keyword-dictionary"></a>기존 키워드 사전 수정

키워드 사전 중 하나에서 키워드를 수정하거나, 기본 제공된 사전 중 하나에서 키워드를 수정해야 할 수 있습니다. 이 예제에서는 PowerShell에서 일부 용어를 수정하고, 편집기에서 수정할 수 있도록 로컬로 저장한 후 이전 용어를 업데이트합니다. 먼저 다음과 같이 사전 개체를 검색합니다.
  
```
$dict = Get-DlpKeywordDictionary -Name "Diseases"
```

`$dict`를 출력하면 다양한 변수가 표시됩니다. 키워드 자체는 백 엔드의 개체에 저장되지만 `$dict.KeywordDictionary`에는 사전을 수정하는 데 사용하게 되는 문자열 표현이 포함됩니다. 사전을 수정하기 전에 `.split(',')` 메서드를 사용하여 용어 문자열을 다시 배열로 전환해야 합니다. 그런 후 `.trim()` 메서드를 사용하여 키워드 사이의 원치 않는 공백을 지우고 사용할 키워드만 남겨둡니다. 
  
```
$terms = $dict.KeywordDictionary.split(',').trim()
```

이제 사전에서 몇 가지 용어를 제거해봅니다. 예제 사전에는 키워드가 몇 개만 포함되어 있으므로 사전을 내보내고 메모장에서 편집하는 과정으로 쉽게 건너뛸 수 있습니다. 그렇지만 사전에는 많은 용어가 들어 있는 것이 일반적이므로 먼저 이 방법을 배워 PowerShell에서 쉽게 편집할 수 있도록 합니다.
  
마지막 단계에서는 키워드를 배열로 저장했습니다. [배열에서 항목을 제거](https://go.microsoft.com/fwlink/p/?linkid=852620)하는 방법에는 여러 가지가 있지만 사전에서 제거하려는 용어의 배열을 만든 후 용어 목록에 없는 사전 용어만 복사하여 제거할 수 있습니다.
  
명령 `$terms`를 실행하여 현재 용어 목록을 표시합니다. 명령 출력은 다음과 같습니다. 
  
```
aarskog's syndrome
abandonment
abasia
abderhalden-kaufmann-lignac
abdominalgia
abduction contracture
abetalipoproteinemia
abiotrophy
ablatio
ablation
ablepharia
abocclusion
abolition
aborter
abortion
abortus
aboulomania
abrami's disease
```

다음 명령을 실행하여 제거하려는 용어를 지정합니다.
  
```
$termsToRemove = @('abandonment', 'ablatio')
```

목록에서 용어를 실제로 제거하려면 다음 명령을 실행합니다.
  
```
$updatedTerms = $terms | Where-Object{ $_ -notin $termsToRemove }
```

명령 `$updatedTerms`를 실행하여 업데이트된 용어 목록을 표시합니다. 명령 출력은 다음과 같습니다(지정된 용어가 제거됨). 
  
```
aarskog's syndrome
abasia
abderhalden-kaufmann-lignac
abdominalgia
abduction contracture
abetalipo proteinemia
abiotrophy
ablation
ablepharia
abocclusion
abolition
aborter
abortion
abortus
aboulomania
abrami's disease
```

이제 사전을 로컬로 저장하고 몇 개의 항목을 추가합니다. PowerShell에서 바로 용어를 추가할 수 있지만 파일이 유니코드 인코딩으로 저장되었는지와 BOM을 포함하는지 확인하려면 파일을 로컬로 내보내야 합니다.
  
다음을 실행하여 사전을 로컬로 저장합니다.
  
```
Set-Content $updatedTerms -Path "C:\myPath\terms.txt"
```

이제 파일을 열고 영어를 더 추가한 후 유니코드 인코딩(UTF-16)으로 저장하면 됩니다. 업데이트된 용어를 업로드하고 사전을 업데이트합니다.
  
```
PS> Set-DlpKeywordDictionary -Identity "Diseases" -FileData (Get-Content -Path "C:myPath\terms.txt" -Encoding Byte -ReadCount 0)
```

이제 사전이 제대로 업데이트되었습니다. `Identity` 필드 에는 사전의 이름이 표시됩니다. `set-` cmdlet을 사용하여 사전 이름도 변경하려면 위 명령에서 새 사전 이름과 함께 `-Name` 매개 변수만 추가하면 됩니다. 
  
## <a name="using-keyword-dictionaries-in-custom-sensitive-information-types-and-dlp-policies"></a>사용자 지정 중요한 정보 유형과 DLP 정책에서 키워드 사전 사용

키워드 사전은 사용자 지정 중요한 정보 유형에 대한 일치 요구 사항의 일부로 또는 중요한 정보 유형 자체로 사용할 수 있습니다. 두 경우 모두 [Office 365 보안 및 준수 센터 PowerShell에서 사용자 지정 중요한 정보 유형을 만들어야](create-a-custom-sensitive-information-type-in-scc-powershell.md) 합니다. 링크 문서의 지침에 따라 중요한 정보 유형을 만듭니다. XML이 있으면 사전에 대한 GUID 식별자가 있어야 사용할 수 있습니다.
  
```
<Entity id="9e5382d0-1b6a-42fd-820e-44e0d3b15b6e" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef=". . ."/>
    </Pattern>
</Entity>
```

사전의 ID를 확인하려면 다음 명령을 실행하고 **Identity** 속성 값을 복사합니다. 
  
```
Get-DlpKeywordDictionary -Name "Diseases"
```

이 명령의 출력은 다음과 같습니다.
  
```
RunspaceId        : 138e55e7-ea1e-4f7a-b824-79f2c4252255
Identity          : 8d2d44b0-91f4-41f2-94e0-21c1c5b5fc9f
Name              : Diseases
Description       : Names of diseases and injuries from ICD-10-CM lexicon
KeywordDictionary : aarskog's syndrome, abandonment, abasia, abderhalden-kaufmann-lignac, abdominalgia, abduction contracture, abetalipo
                    proteinemia, abiotrophy, ablatio, ablation, ablepharia, abocclusion, abolition, aborter, abortion, abortus, aboulomania,
                    abrami's disease, abramo
IsValid           : True
ObjectState       : Unchanged
```

사용자 지정 중요한 정보 유형의 XML에 ID를 붙여넣은 후 업로드합니다. 이제 사전이 중요한 정보 유형 목록에 표시되므로 일치시킬 키워드 수를 지정하여 정책에서 바로 사용할 수 있습니다.
  
```
<Entity id="d333c6c2-5f4c-4131-9433-db3ef72a89e8" patternsProximity="300" recommendedConfidence="85">
      <Pattern confidenceLevel="85">
        <IdMatch idRef="8d2d44b0-91f4-41f2-94e0-21c1c5b5fc9f" />
      </Pattern>
    </Entity>
    <LocalizedStrings>
      <Resource idRef="d333c6c2-5f4c-4131-9433-db3ef72a89e8">
        <Name default="true" langcode="en-us">Diseases</Name>
        <Description default="true" langcode="en-us">Detects various diseases</Description>
      </Resource>
    </LocalizedStrings>
```


