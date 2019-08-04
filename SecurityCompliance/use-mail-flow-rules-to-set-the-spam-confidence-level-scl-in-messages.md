---
title: 메일 흐름 규칙을 사용하여 메시지의 스팸 신뢰 수준(SCL) 설정
ms.author: tracyp
author: MSFTTracyP
manager: dansimp
ms.date: 11/17/2014
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 4ccab17a-6d49-4786-aa28-92fb28893e99
ms.collection:
- M365-security-compliance
description: 관리자는 Exchange Online Protection에서 메시지의 SCL을 설정 하는 방법을 확인할 수 있습니다.
ms.openlocfilehash: 5ec92573a9ebd1789683d6fdd596747a0e082df0
ms.sourcegitcommit: 32ecff689ae32c59a39b7633ca0f36a304e7516e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/09/2019
ms.locfileid: "35601415"
---
# <a name="use-mail-flow-rules-to-set-the-spam-confidence-level-scl-in-messages"></a>메일 흐름 규칙을 사용하여 메시지의 스팸 신뢰 수준(SCL) 설정

전자 메일 메시지의 SCL (스팸 지 수)을 설정 하는 메일 흐름 규칙 (전송 규칙이 라고도 함)을 만들 수 있습니다. SCL은 메시지의 스팸 가능성을 측정 한 것입니다. 스팸은 요청되지 않은(일반적으로 원치 않는) 전자 메일 메시지입니다. 서비스는 SCL 등급에 따라 메시지에서 다른 작업을 수행 합니다. 예를 들어 동료 로부터 내부에 보낸 메시지가 스팸이 아닌 것을 신뢰 하기 때문에 조직 내부의 사용자가 보낸 메시지에 대해서는 스팸 콘텐츠 필터링을 무시 하는 것이 좋습니다. 메일 흐름 규칙을 사용 하 여 메시지의 SCL 값을 설정 하면 스팸을 보다 쉽게 제어할 수 있습니다. 
  
 **시작하기 전에 알아야 할 내용**
  
- 이 절차의 예상 완료 시간: 10 분.
    
- 이러한 절차를 수행하려면 먼저 사용 권한을 할당받아야 합니다. 필요한 사용 권한을 확인 하려면 [Feature permissions In Exchange Online](http://technet.microsoft.com/library/15073ce1-0917-403b-8839-02a2ebc96e16.aspx) 또는 [FEATURE permissions in EOP에서](eop/feature-permissions-in-eop.md)"메일 흐름 규칙" 항목을 참조 하세요. 
    
- 이 항목의 절차에 적용할 수 있는 바로 가기 키에 대한 자세한 내용은 **Exchange 관리 센터의 바로 가기 키**을 참조하세요.
    
### <a name="to-create-a-mail-flow-rule-that-sets-the-scl-of-a-message"></a>메시지의 SCL을 설정 하는 메일 흐름 규칙을 만들려면

1. EAC (Exchange 관리 센터)에서 **메일 흐름** \> **규칙**을 선택 합니다.
    
2. **새로**![만들기 아이콘](media/ITPro-EAC-AddIcon.gif)을 선택한 다음 **새 규칙 만들기**를 선택 합니다.
    
3. 규칙 이름을 지정합니다.
    
4. **기타 옵션**을 선택한 다음 다음의 **경우이 규칙 적용**에서이 규칙에 대해 설정할 작업을 트리거할 조건을 지정 합니다 (SCL 값 설정).
    
    예를 들어 **보낸 사람이** \> **내부/외부 인지**설정할 수 있으며, **보낸 사람 위치 선택** 대화 상자에서 **조직 내부**를 선택 하 고 **확인**을 선택 합니다.<br/>
    ![보낸 사람 위치 선택](media/EOP-ETR-SetSCL-1.jpg)
  
5. **다음 작업 실행**에서 **메시지 속성 수정** \> **SCL(스팸 지수) 설정**을 선택합니다.
  
6. **SCL 지정** 대화 상자에서 다음 값 중 하나를 선택 하 고 **확인**을 선택 합니다.
    
  - **스팸 필터링 무시** -SCL을-1로 설정 하므로 콘텐츠 필터링이 수행 되지 않습니다. 
    
  - **0-4** -SCL을 이러한 값 중 하나로 설정 하면 메시지가 추가 처리를 위해 콘텐츠 필터와 함께 전달 됩니다. 
    
  - **5, 6** -SCL을 이러한 값 중 하나로 설정 하면 해당 콘텐츠 필터 정책의 **스팸** 에 대해 지정 된 작업이 적용 됩니다. 기본적으로 받는 사람의 정크 메일 폴더로 메시지를 전송 하는 작업이 수행 됩니다. 
    
  - **7-9** -SCL을 이러한 값 중 하나로 설정 하면 해당 콘텐츠 필터 정책의 **신뢰도가 높은 스팸** 에 대해 지정 된 작업이 적용 됩니다. 기본적으로 받는 사람의 정크 메일 폴더로 메시지를 전송 하는 작업이 수행 됩니다. 
    
    콘텐츠 필터 정책 구성에 대 한 자세한 내용은 [스팸 필터 정책 구성을](configure-your-spam-filter-policies.md)참조 하세요. 서비스의 SCL 값에 대한 자세한 내용은 [스팸 신뢰 수준](spam-confidence-levels.md)를 참조하세요.
    
7. 규칙에 대 한 추가 속성을 지정 하 고 **저장**을 선택 합니다.
    
    > [!TIP]
    > 이 규칙에 대해 선택 하거나 지정할 수 있는 추가 속성에 대 한 자세한 내용은 [EAC를 사용 하 여 메일 흐름 규칙 만들기](https://docs.microsoft.com/Exchange/policy-and-compliance/mail-flow-rules/mail-flow-rule-procedures#use-the-eac-to-create-mail-flow-rules)를 참조 하십시오. 
  
## <a name="how-do-you-know-this-worked"></a>작동 여부는 어떻게 확인하나요?

이 프로시저가 제대로 작동 하는지 확인 하려면 조직 내부의 사람에 게 전자 메일 메시지를 보내고 메시지에 대해 수행 된 작업이 예상 대로 진행 되는지 확인 합니다. 예를 들어 **SCL (스팸** 지 수)이 **스팸 필터링을 무시**하도록 설정 하는 경우 메시지를 지정 된 받는 사람의 받은 편지 함으로 보내야 합니다. 그러나 **SCL (스팸** 지 수)을 **9**로 설정 하 고 해당 콘텐츠 필터 정책에 대 한 **신뢰도가 높은 스팸** 작업을 정크 메일 폴더로 이동 하는 경우에는 지정 된 사용자에 게 메시지를 전송 해야 합니다. 받는 사람의 정크 메일 폴더입니다. 
  

