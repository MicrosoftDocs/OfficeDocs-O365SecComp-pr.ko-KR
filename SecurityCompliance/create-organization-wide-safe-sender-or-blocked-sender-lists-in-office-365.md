---
title: Create organization-wide safe sender or blocked sender lists in Office 365
ms.author: stephow
author: stephow-msft
manager: laurawi
ms.date: 8/8/2015
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
ms.assetid: 9721b46d-cbea-4121-be51-542395e6fd21
description: 조정할 수 하 고 해당 메시지를 신뢰 하기 때문에 특정 한 보낸에서 메일을 받을 해야 하려는 경우에 Exchange 관리 센터에서 스팸 필터 정책에서 허용 목록.
ms.openlocfilehash: 1086a4a710432eb412ae9f08f204beda52aa5390
ms.sourcegitcommit: 22bca85c3c6d946083d3784f72e886c068d49f4a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/06/2018
ms.locfileid: "22027545"
---
# <a name="create-organization-wide-safe-sender-or-blocked-sender-lists-in-office-365"></a>Create organization-wide safe sender or blocked sender lists in Office 365
  
조정할 수 하 고 해당 메시지를 신뢰 하기 때문에 특정 한 보낸에서 메일을 받을 해야 하려는 경우 대화 **보호** 에 Exchange 관리 센터 (EAC)에서 스팸 필터 정책에서 허용 목록 \> **스팸 필터**입니다. [스팸 필터 정책 구성](configure-your-spam-filter-policies.md)에서이 대 한 자세한 내용을 알아봅니다. 다른 옵션 같은 도메인 또는 사용자 기반 works 허용 목록 스팸 필터에는 Exchange 전송 규칙을 만들 수 있습니다. 너무 비슷한 방법으로 특정 도메인 또는 사용자가 보낸 메시지를 차단할 수 있습니다.
  
전송 규칙에도 유용 하다이 이런 메시지 헤더 또는 첨부 파일의 이름을 확인 하는 등 복잡 한 조건을 지정 하기 위해 필터링 할 때 또는 메시지에는 고 지 사항을 추가 (영문) 또는 시간 간격을 적용 하는 등의 복잡 한 작업을 추가 하려는 경우에 rul e 활성 상태입니다. 그러나 특정 보낸 사람이 나 도메인에서 보내는 전자 메일 스팸 필터링 무시 되도록 것이 좋습니다 스팸 필터 정책에 추가 합니다. 시작 하기이 EAC에서 **보호** 를 이동 하 여 \> **스팸 필터**입니다. 자세한 내용은 [스팸 필터 정책 구성](configure-your-spam-filter-policies.md).
  
> [!TIP]
> 도메인 스푸핑 될 수 있으므로 도메인 기반 목록을 전송 규칙에는 IP 주소를 기준으로 목록으로 안전 하지 않습니다. 또한 보내는 IP 주소가 차단 목록에 있으면 해당 도메인에 대 한 필터링 하는 경우에에 여전히 차단 됩니다 또는 사용자가 무시 되 고 있습니다. 즉, 도메인 또는 사용자에 전송 규칙을 글로벌 IP 차단 목록 재정의 하지 않습니다. 대부분의 경우에서 IP 주소를 기준으로 목록을 사용 하는 것이 좋습니다. IP 주소를 기준으로 목록을 만들려면 IP 허용 목록 또는 IP 차단 목록 연결 필터에 사용할 수 있습니다. 콘텐츠 필터에 의해 이러한 IP 주소에서 보낸 모든 메시지가 확인 되지 않습니다. IP 허용 목록 또는 IP 차단 목록에 IP 주소를 추가 하 여 연결 필터 정책 구성 하는 방법에 대 한 자세한 내용은 [연결 필터 정책 구성](configure-the-connection-filter-policy.md)을 참조 하십시오. 
  
전송 규칙과 관련된 추가 관리 작업에 대한 자세한 내용은 [Transport Rules](http://technet.microsoft.com/library/743bd525-0ca2-426d-b76c-b4a052bc8886.aspx)을 참조하십시오.
  
## <a name="use-the-eac-to-customize-a-block-or-allow-list-to-prevent-or-receive-email-from-a-domain-or-user"></a>EAC를 사용 하 여 블록을 사용자 지정 하거나 목록에서 방지 하거나 도메인 또는 사용자가 전자 메일을 수신 허용
<a name="sectionSection0"> </a>

1. EAC에서 **보호** 로 이동 \> **스팸 필터**입니다. 
    
2. **일반** 페이지에서 다음 중 하나를 수행 합니다. 
    
  - 기본 정책 또는 기존 정책을 편집 하는 것을 시작 하기 위해 두번클릭 합니다.
    
  - 사용자, 그룹 및 조직에서 도메인에 적용할 수 있는 사용자 지정 스팸 필터 정책을 새로 만들려면 **새로 만들기** 를 클릭 합니다. 
    
3. **허용 목록** 페이지에서 항목을 보낸 사람이 나 도메인의 받은 편지 함으로 배달 될 항상 등을 지정할 수 있습니다. 이러한 항목에 대 한 전자 메일 스팸 필터에 의해 처리 되지 않습니다. 다음을 수행 합니다. 
    
  - 신뢰할 수 있는 보낸 사람이 보낸 사람에 게 허용 된 대화 상대를 추가 합니다. **추가**클릭 하 고 선택 대화 상자에서 허용 하려는 보낸사람 주소를 추가 합니다. 세미콜론으로 또는 새 줄을 사용 하 여 여러 항목을 구분할 수 있습니다. **허용 목록을** 페이지로 돌아가려면 확인을 클릭 합니다. 
    
  - 신뢰할 수 있는 도메인의 도메인을 허용 된 대화 상대를 추가 합니다. **추가**클릭 한 다음 선택 대화 상자에서 허용 하려는 도메인을 추가 합니다. 세미콜론으로 또는 새 줄을 사용 하 여 여러 항목을 구분할 수 있습니다. **허용 목록을** 페이지로 돌아가려면 확인을 클릭 합니다. 
    
    > [!CAUTION]
    > 최상위 도메인을 허용 하는 경우 될 하지 않으려고 전자 메일 하는 받은 편지 함으로 배달 됩니다. 
  
4. **차단 목록** 페이지에서 항상 스팸으로 표시될 항목(예: 보낸 사람 또는 도메인)을 지정할 수 있습니다. 서비스는 이러한 항목과 일치하는 전자 메일에 구성된 높은 정확도 스팸 작업을 적용합니다. 
    
  - 원하지 않는 보낸사람 보낸 사람이 차단 목록에 추가 합니다. **추가**클릭![아이콘 추가](media/ITPro-EAC-AddIcon.png), 하 고 선택 대화 상자에서 차단할 보낸사람 주소를 추가 합니다. 세미콜론으로 또는 새 줄을 사용 하 여 여러 항목을 구분할 수 있습니다. **확인** **차단 목록** 페이지로 돌아가려면를 클릭 합니다. 
    
  - 도메인 차단 목록에 원치 않는 도메인을 추가 합니다. **추가**클릭![아이콘 추가](media/ITPro-EAC-AddIcon.png), 하 고 선택 대화 상자에서 차단할 도메인을 추가 합니다. 세미콜론으로 또는 새 줄을 사용 하 여 여러 항목을 구분할 수 있습니다. **확인** **차단 목록** 페이지로 돌아가려면를 클릭 합니다. 
    
    > [!CAUTION]
    > 최상위 도메인을 차단 하는 경우에는 원하는 전자 메일 스팸으로 표시 되어야 하는 것 같습니다. 
  
## <a name="what-do-you-need-to-know-before-you-begin-creating-a-transport-rule"></a>전송 규칙 만들기 (영문)를 시작 하기 전에 필요한
<a name="sectionSection1"> </a>

- 예상 완료 시간: 15분
    
- 스팸 필터링 무시 또는 전자 메일 보낸 사람이 나 도메인에 대 한 스팸으로 표시 하는 전송 규칙을 만들 필요가 없습니다. 차단 또는 특정 보낸 사람이 나 도메인을 허용 하 고 연결 하지 않고는 추가 조건의 하는 경우이 전송 규칙 대신 스팸 정책에서 허용 목록 및 Exchange Online Protection 블록을 사용 합니다. [스팸 필터 정책 구성](configure-your-spam-filter-policies.md)에서이 대 한 자세한 내용을 알아봅니다.
    
- 이러한 절차를 수행하려면 먼저 사용 권한을 할당받아야 합니다. 필요한 사용 권한을 확인하려면 다음을 참조하세요. [Messaging policy and compliance permissions](http://technet.microsoft.com/library/ec4d3b9f-b85a-4cb9-95f5-6fc149c3899b.aspx)의 "전송 규칙" 항목 
    
- 이 항목의 절차에 적용할 수 있는 바로 가기 키에 대한 자세한 내용은 **Exchange 관리 센터의 바로 가기 키**을 참조하세요.
    
> [!TIP]
> 문제가 있습니까? Exchange 포럼에서 도움을 요청하세요. 포럼 주소는 다음과 같습니다.[Exchange Server](https://go.microsoft.com/fwlink/p/?linkId=60612),[Exchange Online](https://go.microsoft.com/fwlink/p/?linkId=267542), 또는 [Exchange Online Protection](https://go.microsoft.com/fwlink/p/?linkId=285351) 
  
## <a name="use-the-eac-to-create-a-transport-rule-to-bypass-spam-filtering-for-a-domain-or-user"></a>EAC를 사용 하 여 도메인 또는 사용자에 대해 스팸 필터링을 무시 하도록 전송 규칙을 만들려면
<a name="sectionSection2"> </a>

1. EAC에서 **메일 흐름** \> **규칙**으로 이동합니다. **추가**![아이콘 추가](media/ITPro-EAC-AddIcon.png)를 선택한 후 **스팸 필터링 무시**를 선택합니다.
    
2. 규칙에 이름을 지정합니다. **다음의 경우 이 규칙 적용**에서 **보낸 사람**을 선택하고 다음 조건 중 하나를 선택합니다. 
    
  - 도메인을 지정하려면 **도메인**을 선택합니다. **도메인 지정** 대화 상자에 수신 허용으로 지정할 보낸 사람의 도메인을 contoso.com과 같이 입력합니다. 해당 도메인을 구 목록으로 이동하려면 **추가**![아이콘 추가](media/ITPro-EAC-AddIcon.png)를 클릭합니다. 도메인을 더 추가하려면 이 단계를 반복하고 완료되면 **확인**을 클릭합니다. 
    
  - 사용자를 지정하려면 **이 사람**을 선택합니다. **구성원 선택** 대화 상자의 사용자 유형 목록에서 사용자를 추가하고 **이름 확인**을 클릭합니다. 사용자를 더 추가하려면 이 단계를 반복하고 완료되면 **확인**을 클릭합니다. 
    
3. 다른 규칙이 없는 바이패스 동작을 되돌릴 수 있는지 확인 하려면 **추가 규칙 처리 중지** 확인란을 선택 
    
4. **메시지에서 일치 하는 보낸사람 주소** 옵션에 대 한 **헤더 또는 봉투를**선택 합니다.
    
5. 원하는 경우에 감사 규칙, 규칙을 테스트, 특정 기간 동안 규칙 활성화를 선택 하 고 다른 선택 항목을 만들 수 있습니다. 조직에 적용 하기 전에 시간 기간에 대 한 규칙을 테스트 하는 것이 좋습니다. 이러한 선택 항목에 대 한 자세한 내용은 [전송 규칙 관리](http://technet.microsoft.com/library/e7a81372-b6d7-4d1f-bc9e-a845a7facac2.aspx)를 참조 하십시오.
    
6. **저장**을 선택하여 규칙을 저장합니다. 
    
규칙을 만들어 적용하고 나면 지정한 도메인 또는 사용자에 대해 스팸 필터링이 무시됩니다.
  
## <a name="use-the-eac-to-create-a-transport-rule-that-blocks-messages-sent-from-a-domain-or-user"></a>EAC를 사용 하 여 도메인 또는 사용자가 보낸 메시지를 차단 하는 전송 규칙을 만들려면
<a name="sectionSection3"> </a>

1. EAC에서 **메일 흐름** \> **규칙**으로 이동합니다. **추가**![아이콘 추가](media/ITPro-EAC-AddIcon.png)를 선택한 다음 **새 규칙 만들기**를 선택합니다.
    
2. 규칙 이름을 지정하고 **기타 옵션**을 클릭합니다. 
    
3. **다음의 경우 이 규칙 적용**에서 **보낸 사람**을 선택하고 다음 조건 중 하나를 선택합니다. 
    
  - 도메인을 지정하려면 **도메인**을 선택합니다. 도메인 지정 대화 상자에 메시지를 차단할 보낸 사람 도메인을 contoso.com과 같이 입력합니다. 구 목록으로 이 도메인을 이동하려면 **추가**![아이콘 추가](media/ITPro-EAC-AddIcon.png)를 클릭합니다. 도메인을 더 추가하려면 이 단계를 반복하고 완료되면 **확인**을 클릭합니다. 
    
  - 사용자를 지정하려면 **이 사람**을 선택합니다. **구성원 선택** 대화 상자의 사용자 유형 목록에서 사용자를 추가하고 **이름 확인**을 클릭합니다. 사용자를 더 추가하려면 이 단계를 반복하고 완료되면 **확인**을 클릭합니다. 
    
4. **다음 작업 실행**에서 **메시지 차단**을 선택한 다음 **아무에게도 알리지 않고 메시지 삭제**와 같은 다른 옵션 중 하나를 클릭합니다.
    
5. **기타 옵션**을 클릭 한 다음 **메시지에서 일치 하는 보낸사람 주소** 옵션에 대 한 **헤더 또는 봉투를**선택 합니다.
    
6. 원하는 경우에 감사 규칙, 규칙을 테스트, 특정 기간 동안 규칙 활성화를 선택 하 고 다른 선택 항목을 만들 수 있습니다. 조직에 적용 하기 전에 시간 기간에 대 한 규칙을 테스트 하는 것이 좋습니다. 이러한 선택 항목에 대 한 자세한 내용은 [전송 규칙 관리](http://technet.microsoft.com/library/e7a81372-b6d7-4d1f-bc9e-a845a7facac2.aspx)를 참조 하십시오.
    
7. **저장**을 선택하여 규칙을 저장합니다. 
    
규칙을 만들어 적용하고 나면 지정한 도메인 또는 사용자가 보내는 모든 메시지가 차단됩니다.
  
## <a name="see-also"></a>참고 항목
<a name="sectionSection3"> </a>

[스팸 필터 정책 구성](configure-your-spam-filter-policies.md)
  
[전송 규칙을 사용 하 여 대량 전자 메일 필터링을 구성 하려면](use-transport-rules-to-configure-bulk-email-filtering.md)

