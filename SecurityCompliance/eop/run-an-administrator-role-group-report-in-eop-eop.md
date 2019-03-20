---
title: 'EOP에서 관리자 역할 그룹 보고서 실행 '
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 11/17/2014
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.assetid: 23b47b57-0eec-46a3-a03b-366ea014ab31
description: 관리자가 구성원을 관리자 역할 그룹에 추가하거나 그룹에서 제거하면 Microsoft EOP(Exchange Online Protection)에서 각 작업을 기록합니다.
ms.openlocfilehash: 752def771d95fcfbb3f7cbe0bc86a33b3967716d
ms.sourcegitcommit: 0f93b37c39d807dec91f118aa671a3430c47a9ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/20/2019
ms.locfileid: "30692717"
---
# <a name="run-an-administrator-role-group-report-in-eop"></a>EOP에서 관리자 역할 그룹 보고서 실행 

 관리자가 구성원을 관리자 역할 그룹에 추가하거나 그룹에서 제거하면 Microsoft EOP(Exchange Online Protection)에서 각 작업을 기록합니다. Exchange 관리 센터에서 관리자 역할 그룹 보고서를 실행하면 항목은 검색 결과로 표시되며 해당하는 역할 그룹, 역할 그룹 구성원을 변경한 사람과 시간, 그리고 구성원 업데이트 내용이 포함됩니다. 이 보고서를 사용하여 조직의 사용자에게 할당된 관리 권한의 변경을 모니터링할 수 있습니다.
  
## <a name="what-do-you-need-to-know-before-you-begin"></a>시작하기 전에 알아야 할 내용

- 예상 완료 시간: 2분
    
- 이러한 절차를 수행하려면 먼저 사용 권한을 할당받아야 합니다. 필요한 사용 권한을 확인하려면 다음을 참조하세요. [EOP의 기능 사용 권한](feature-permissions-in-eop.md)의 "보고서" 섹션 
    
- 이 항목의 절차에 적용할 수 있는 바로 가기 키에 대한 자세한 내용은 **Keyboard shortcuts in Exchange 2013**을 참조하세요.
    
> [!TIP]
> 문제가 있습니까? Exchange 포럼에서 도움을 요청하세요. 포럼 주소는 다음과 같습니다.[Exchange Server](https://go.microsoft.com/fwlink/p/?linkId=60612),[Exchange Online](https://go.microsoft.com/fwlink/p/?linkId=267542), 또는 [Exchange Online Protection](https://go.microsoft.com/fwlink/p/?linkId=285351) 
  
## <a name="use-the-eac-to-run-an-administrator-role-group-report"></a>EAC를 사용하여 관리자 역할 그룹 보고서 실행

관리자 역할 그룹 보고서를 실행하여 특정 시간대 내 조직의 관리 역할 그룹 변경 내용을 찾을 수 있습니다.
  
1. EAC에서 **준수 관리** \> **감사**로 이동한 후 **관리자 역할 그룹 보고서 실행**을 선택합니다.
    
2. **시작 날짜**와 **끝 날짜**를 선택합니다. 기본적으로 보고서는 지난 2주 동안의 관리자 역할 그룹 변경 내용을 검색합니다.
    
3. 특정 역할 그룹에 대한 변경 내용을 보려면 **역할 그룹 선택**을 클릭합니다. 그러면 표시되는 대화 상자에서 역할 그룹을 하나 이상 선택하고 **확인**을 클릭합니다. 변경된 모든 역할 그룹을 찾으려는 경우에는 해당 필드를 비워 두면 됩니다.
    
4. **검색**을 클릭합니다.
    
지정한 조건을 사용하여 찾은 변경 내용은 결과 창에 표시됩니다. 검색 결과에서 역할 그룹을 클릭하여 세부 정보 창에서 변경 내용을 확인합니다.
  
## <a name="how-do-you-know-this-worked"></a>작동 여부는 어떻게 확인하나요?

관리자 역할 그룹 보고서를 성공적으로 실행한 경우 날짜 범위 내에서 변경된 역할 그룹은 검색 결과 창에 표시됩니다. 결과가 표시되지 않으면 지정된 날짜 범위 내에서 역할 그룹이 변경되지 않은 것입니다. 표시할 결과가 있다고 생각되면 날짜 범위를 변경한 다음 보고서를 다시 실행하십시오.
  
## <a name="monitor-changes-to-role-group-membership"></a>역할 그룹 구성원의 변경 모니터링

구성원이 역할 그룹에서 추가되거나 제거되면 세부 정보 창에 표시되는 검색 결과에서 역할 그룹 구성원이 업데이트되었음이 표시되고 현재 구성원이 표시됩니다. 이 결과에서는 추가되거나 제거된 사용자가 명시적으로 나타나지 않습니다.
  
사용자가 추가되었거나 제거되었는지 확인하려면 보고서에서 두 가지 항목을 비교해야 합니다. 예를 들어 **HelpDesk** 역할 그룹에 대한 다음 로그 항목을 살펴보겠습니다. 
  
 **2013/1/27 오후 4:43**
  
 **관리자**
  
 **업데이트된 구성원: Administrator;annb,florencef;pilarp**
  
 **2013/2/06 오전 10:09**
  
 **관리자**
  
 **업데이트된 구성원: Administrator;annb;florencef;pilarp;tonip**
  
 **2013/2/19 오후 2:12**
  
 **관리자**
  
 **업데이트된 구성원: Administrator;annb;florencef;tonip**
  
이 예에서는 관리자 사용자 계정이 다음과 같은 변경을 수행했습니다.
  
- 2013년 2월 6일에 사용자 tonip을 추가했습니다.
    
- 2013년 2월 19일에 사용자 pilarp를 제거했습니다.
    

