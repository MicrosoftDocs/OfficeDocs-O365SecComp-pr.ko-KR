---
title: 관리자로 격리된 메시지 찾기 및 릴리스
ms.author: tracyp
author: MSFTTracyP
manager: laurawi
ms.date: 6/16/2017
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: ab95bf17-bb09-4dd1-9990-ddd02ddecf05
ms.collection:
- M365-security-compliance
description: 이 항목에서는 Exchange Online 및 exchange Online Protection (EOP) 관리자가 EAC (exchange 관리 센터)에서 격리 된 메시지를 찾아서 해제 하 고 보고 하는 방법에 대해 설명 합니다.
ms.openlocfilehash: 7ac65ae5b4225e56861dacacdd61bf5a237f7ca8
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/17/2019
ms.locfileid: "34154570"
---
# <a name="find-and-release-quarantined-messages-as-an-administrator"></a>관리자로 격리된 메시지 찾기 및 릴리스

이 항목에서는 Exchange Online 및 exchange Online Protection (EOP) 관리자가 EAC (exchange 관리 센터)에서 격리 된 메시지를 찾아서 해제 하 고 보고 하는 방법에 대해 설명 합니다. Office 365에서는 메시지가 스팸으로 식별 되었거나 메일 흐름 규칙 (전송 규칙이 라고도 함)과 일치 하기 때문에 메시지를 격리로 보냅니다. 
  
EAC 대신 보안 &amp; 및 준수 센터를 사용 하 여 이러한 작업을 완료 하 고, 맬웨어가 포함 되어 있어 격리로 전송 된 메시지를 보고 작업 합니다. 자세한 내용은 [Office 365에서 전자 메일 메시지 격리](https://support.office.com/article/Quarantine-email-messages-in-Office-365-4c234874-015e-4768-8495-98fcccfc639b)를 참조 하세요.
  
격리 된 메시지는 EAC의 **격리** 페이지에 나열 됩니다. 기본적으로 메시지는 **받은 날짜** 필드에서 가장 오래 된 항목 순으로 정렬 됩니다. 각 메시지에 대해 **보낸 사람**, **제목** 및 **만료 날짜** 값도 표시됩니다. 이러한 필드의 머리글을 클릭하여 각 필드를 정렬할 수 있습니다. 열 머리글을 두 번 클릭 하면 정렬 순서가 반전 됩니다. **격리** 페이지에 최대 500 개의 메시지가 표시 됩니다. 
  
격리 된 모든 메시지의 목록을 보거나, 필터 조건을 지정 하 여 특정 메시지를 검색할 수 있습니다 (필터링은 메시지 수가 500 개를 초과 하는 경우에도 결과 집합을 줄이는 데 도움이 됩니다). 격리된 특정 메시지를 검색하여 찾은 후에는 메시지에 대한 세부 정보를 확인할 수 있습니다. 다음 작업도 수행할 수 있습니다.
  
- 메시지를 한 명 이상의 받는 사람에 게 놓은 다음, 필요에 따라 메시지를 평가 하 고 분석할 Microsoft 스팸 분석 팀에 가양성 (정크 메일 아님) 메시지로 보고 합니다. 분석 결과에 따라 메시지 통과를 허용하도록 서비스 전체적으로 스팸 콘텐츠 필터 규칙이 조정될 수 있습니다.
    
- 메시지를 해제 하 고 앞으로 해당 하는 해당 보낸 사람의 메시지를 모두 허용 합니다.
    
## <a name="what-do-you-need-to-know-before-you-begin"></a>시작하기 전에 알아야 할 내용
<a name="sectionSection0"> </a>

- 이러한 절차를 수행하려면 먼저 사용 권한을 할당받아야 합니다. 필요한 사용 권한을 확인 하려면 [Feature permissions In Exchange Online](http://technet.microsoft.com/library/15073ce1-0917-403b-8839-02a2ebc96e16.aspx) 항목의 "격리" 항목을 참조 하십시오. 
    
- **격리** 페이지에서 한 번에 여러 메시지를 릴리스 하거나 보고할 수 있습니다. 또는이 작업을 수행 하는 원격 Windows PowerShell 스크립트를 만들 수 있습니다. [Get-QuarantineMessage](http://technet.microsoft.com/library/88026da1-8dbc-49e7-80e8-112a32773c34.aspx) cmdlet을 사용하여 메시지를 검색하고 [Release-QuarantineMessage](http://technet.microsoft.com/library/4a3aa05c-238f-46f2-b8dd-b0e3c38eab3e.aspx) cmdlet을 사용하여 메시지를 해제할 수 있습니다. 
    
- 이 항목의 절차에 적용할 수 있는 바로 가기 키에 대한 자세한 내용은 **Exchange 관리 센터의 바로 가기 키**을 참조하세요.
    
> [!TIP]
> 문제가 있습니까? Exchange 포럼에서 도움을 요청하세요. 포럼 주소는 다음과 같습니다.[Exchange Server](https://go.microsoft.com/fwlink/p/?linkId=60612),[Exchange Online](https://go.microsoft.com/fwlink/p/?linkId=267542), 또는 [Exchange Online Protection](https://go.microsoft.com/fwlink/p/?linkId=285351) 
  
## <a name="use-advanced-search-to-filter-and-locate-quarantined-messages"></a>고급 검색을 사용하여 격리된 메시지 필터링 및 찾기
<a name="BKMK_UseAdvancedSearchtoFilterMessages"> </a>

EAC(Exchange 관리 센터)에서 고급 검색을 사용하여 여러 조건에 따라 격리된 항목을 필터링할 수 있습니다. 이러한 조건은 따로 사용할 수도 있고 조합하여 사용할 수도 있습니다. 검색에서는 모든 필터 조건을 충족하는 메시지 목록이 제공됩니다.
  
1. EAC에서 **보호** \> **격리**로 이동한 다음 **고급 검색**을 클릭 합니다.
    
2. **고급 검색** 창에서 다음 조건의 조합을 선택합니다. 연결 된 확인란을 선택 하 여 각 조건을 사용 하도록 설정 합니다. 와일드카드는 지원되지 않습니다. 
    
1. **메시지 ID** 이 매개 변수를 사용하여 특정 메시지를 대상으로 하는 검색을 수행할 수 있습니다. 예를 들어 메시지 추적 기능을 사용하면 조직의 특정 사용자가 보냈거나 받아야 하는데 대상에 도착하지 않은 메시지를 검색할 수 있습니다. 자세한 내용은 [메시지 추적 실행 및 결과 보기](http://technet.microsoft.com/library/74a9fc59-7e0e-4832-baf9-2a86418b0079.aspx)를 참조하세요. 규칙과 일치하거나 스팸으로 확인되어 격리로 전송된 메시지가 있으면 해당 메시지 ID를 지정하여 격리에서 메시지를 쉽게 찾을 수 있습니다. 이때 전체 메시지 ID 문자열을 포함해야 합니다. 여기에는 꺾쇠 괄호 (\<\>)가 포함 될 수 있습니다. 
    
2. **보낸 사람 전자 메일 주소** 메시지를 보낸 사람의 전자 메일 주소를 지정합니다. 
    
3. **받는 사람 전자 메일 주소** 메시지를 받는 사람의 전자 메일 주소를 지정합니다. 
    
4. **제목** 메시지의 제목 줄 텍스트를 지정합니다. 
    
5. **받은 날짜** 지난 24 시간 이내 ( **오늘**), 지난 48 시간 ( **지난 2 일**), 지난 주 ( **지난 7 일**) 내에 격리를 통해 메시지가 수신 되었음을 선택 하거나, 메시지를 표시할 사용자 지정 시간 간격을 선택할 수 있습니다. 격리에 의해 수신 됩니다. 
    
6. **만료** 다음 24 시간 이내 ( **오늘**), 다음 48 시간 ( **다음 2 일**), 다음 주 (다음 **7 일**) 이내에 메시지가 격리에서 삭제 되는 것을 선택 하거나 메시지를 표시할 사용자 지정 시간 간격을 선택할 수 있습니다. 격리에서 삭제 됩니다.
    
    > [!IMPORTANT]
    > 기본적으로 스팸 격리 메시지는 15 일 동안 격리 된 상태로 유지 되 고, 메일 흐름 규칙과 일치 하는 격리 된 메시지는 7 일 동안 격리 됩니다. 이 기간 후에 Office 365에서 메시지를 삭제 하며 이러한 시간을 검색할 수 없습니다. 메일 흐름 규칙과 일치 하는 격리 된 메시지의 보존 기간은 구성할 수 없습니다. 그렇지만 스팸 격리 메시지의 보존 기간은 콘텐츠 필터 정책의 **스팸 보존 기간(일)** 설정을 통해 줄일 수 있습니다. 자세한 내용은 [스팸 필터 정책 구성을](configure-your-spam-filter-policies.md)참조 하세요. 
  
7. **입력** **스팸으로**확인 된 격리 된 메시지를 검색할지 아니면 메일 흐름 규칙 (**전송 규칙**)과 일치 하는 메시지를 검색할지를 지정할 수 있습니다.
    
3. **확인**을 클릭하여 고급 검색 실행을 시작합니다. 
    
    > [!NOTE]
    > 검색 조건을 지우고 격리의 모든 메시지를 보려면 **고급 검색** 창에서 모든 확인란의 선택을 취소하고 **확인**을 클릭합니다. 
  
메시지를 검색하고 나면 지정한 조건과 일치하는 결과가 사용자 인터페이스에 표시됩니다. EAC에서는 메시지를 500개까지 표시할 수 있습니다. 
  
## <a name="view-details-about-a-specific-quarantined-message"></a>격리된 특정 메시지에 대한 세부 정보 보기
<a name="BKMK_ViewDetailsAboutaSpecificQuarantinedMessage"> </a>

격리 페이지에서 격리 된 특정 메시지를 **** 찾은 후에는이에 대 한 세부 정보를 볼 수 있습니다. 
  
1. **격리** 페이지에서 특정 메시지를 선택 하 고 화면 오른쪽의 세부 정보 창에 해당 메시지의 속성에 대 한 요약을 표시 합니다. 
    
    **메시지 상태** 값은 다음과 같습니다. 
    
  - **입력** 메시지가 **스팸으로** 식별 되었는지 아니면 메일 흐름 규칙 (**전송 규칙**)과 일치 했는지를 나타냅니다.
    
  - **만료 날짜** 메시지가 격리에서 삭제되는 날짜입니다. 
    
    **메시지 정보** 값은 다음과 같습니다. 
    
  - **보낸 사람** 메시지를 보낸 사람의 전자 메일 주소입니다. 
    
  - **제목** 메시지의 제목 줄 텍스트입니다. 
    
  - **받은 날짜** 격리에서 메시지를 받은 날짜입니다. 
    
  - **크기** 메시지의 크기입니다. 단위는 KB 또는 MB(메시지 크기가 999KB를 초과하는 경우)입니다. 
    
  - **메시지 헤더 보기** 메시지 헤더 텍스트를 확인할 수 있는 **메시지 헤더** 대화 상자를 열려면 이 링크를 클릭합니다. 메시지 헤더 텍스트를 클립보드에 복사한 다음 [메시지 헤더 분석기](https://testconnectivity.microsoft.com/?tabid=mha)에 붙여 넣을 수도 있습니다. 메시지 헤더 분석기 도구가 표시되면 **헤더 분석**을 클릭하여 헤더에 대한 정보를 검색합니다. 
    
    > [!TIP]
    > 서비스에서 삽입하는 특정 스팸 방지 메시지 헤더 필드에 대한 자세한 내용은 [스팸 방지 메시지 헤더](anti-spam-message-headers.md)를 참조하세요. 
  
  - **전자 메일 메시지 미리 보기** 메시지 텍스트를 검토 하려면이 링크를 클릭 합니다. 
    
2. 격리된 메시지를 두 번 클릭하면 **격리된 메시지** 창이 열리고 다음 정보가 표시됩니다. 
    
  - **릴리스됨** 메시지가 릴리스된 사용자(있는 경우)의 모든 전자 메일 주소가 포함된 목록입니다. 
    
  - **아직 릴리스되지 않음** 메시지가 아직 릴리스되지 않은 사용자(있는 경우)의 모든 전자 메일 주소가 포함된 목록입니다. **릴리스됨** 링크를 클릭하면 메시지를 릴리스할 수 있습니다. 메시지 릴리스에 대한 자세한 내용은 다음 섹션을 참조하세요. 
    
  - **메시지 ID** 메시지 헤더에 있는 인터넷 메시지 ID(클라이언트 ID라고도 함)입니다. 
    
    **닫기**를 클릭하여 기본 격리 창으로 돌아갑니다. 
    
## <a name="release-messages-from-quarantine"></a>격리에서 메시지 릴리스
<a name="sectionSection3"> </a>

받는 사람에 게 메시지를 릴리스하기 위해 다음 옵션을 사용할 수 있습니다.
  
- [격리 된 메시지 릴리스 및 보낸 사람의 향후 메시지 허용](find-and-release-quarantined-messages-as-an-administrator.md#Releasequarantinedmessageallowfuturemessagesfromsender)
    
- [격리 된 메시지를 가양성으로 보고 하지 않고 특정 받는 사람에 게 릴리스](find-and-release-quarantined-messages-as-an-administrator.md#Releasequarantinedmessagetospecificrecipientswithoutreportingasfalsepositive)
    
- [모든 받는 사람에 게 격리 된 메시지를 하나 이상 릴리스](find-and-release-quarantined-messages-as-an-administrator.md#Releaseoneormorequarantinedmessagestoallrecipients)
    
- [하나 이상의 격리 된 메시지를 모든 받는 사람에 게 릴리스하고 가양성 보고](find-and-release-quarantined-messages-as-an-administrator.md#Releaseoneormorequarantinedmessagestoallrecipientsandreportfalsepositives)
    
### <a name="release-a-quarantined-message-and-allow-future-messages-from-the-sender"></a>격리 된 메시지 릴리스 및 보낸 사람의 향후 메시지 허용
<a name="Releasequarantinedmessageallowfuturemessagesfromsender"> </a>

1. EAC에서 **보호** \> **격리**로 이동 합니다.
    
2. 메시지를 클릭 하 여 선택 하 고 다음 스크린샷과 같이 **메시지 릴리스** 아이콘을 클릭 합니다. 
  
![강조 표시된 메시지 릴리스 아이콘 및 표시된 릴리스 옵션이 포함된 격리 페이지를 보여줍니다.](media/36ee081f-3e30-40c9-8ce3-240cee1970cc.png)
  
드롭다운 목록에서 **선택한 메시지 릴리스 및 보낸 사람 허용** 을 클릭 합니다. 
    
3. **메시지 릴리스 및 보낸 사람 허용** 대화 상자가 열립니다. 필요한 경우 Microsoft에 메시지를 보고할지 선택한 다음 **릴리스 및 허용**을 클릭할 수 있습니다. 메시지가 주소가 지정 된 모든 받는 사람에 게 전달 되 고 앞으로이 보낸 사람에 게 보내는 모든 메시지가 허용 됩니다. 그러나 메일 흐름 규칙 또는 수신 거부로 인해이 메시지가 격리 된 경우에는 이후 메시지에 대 한 보낸 사람을 계속 차단 합니다. 
    
### <a name="release-a-quarantined-message-to-specific-recipients-without-reporting-it-as-a-false-positive"></a>격리 된 메시지를 가양성으로 보고 하지 않고 특정 받는 사람에 게 릴리스
<a name="Releasequarantinedmessagetospecificrecipientswithoutreportingasfalsepositive"> </a>

1. EAC에서 **보호** \> **격리**로 이동 합니다.
    
2. 메시지를 선택 하 고 **메시지 릴리스** 아이콘을 클릭 한 다음 드롭다운 목록에서 **메시지를 특정 받는 사람에 게 릴리스를** 클릭 합니다. 
    
3. **메시지 릴리스** 대화 상자에서 다음 옵션 중 하나를 선택합니다. 
    
  - **모든 받는 사람에게 메시지 릴리스** 이 옵션을 선택하면 메시지를 동일한 받는 사람에게 두 번 이상 릴리스할 수 없습니다. 받는 사람이 이 메시지를 이전에 수신한 경우 메시지가 해당 받는 사람에게 다시 릴리스되지 않습니다. 
    
  - **지정한 받는 사람에 게 메시지 릴리스** 메시지를 해제할 수 있는 받는 사람을 선택 합니다. 메시지는 받는 사람 모두에 게 한 번만 릴리스될 수 있으므로이 목록에는 해당 받는 사람을 해제할 수 있는 사용자만 표시 됩니다. 여러 항목을 선택할 수 있습니다. 받는 사람을 선택한 후 **추가**를 클릭 합니다.
    
4. **릴리스**를 클릭합니다. 
    
새로 고침 아이콘](media/ITPro-EAC-RefreshIcon.gif) **새로**![고침 아이콘을 클릭 하 여 데이터를 새로 고친 다음 해당 메시지를 두 번 클릭 하면 해당 받는 사람에 게 해당 메시지가 해제 된 것을 확인할 수 있습니다. 
  
### <a name="release-one-or-more-quarantined-messages-to-all-recipients"></a>모든 받는 사람에 게 격리 된 메시지를 하나 이상 릴리스
<a name="Releaseoneormorequarantinedmessagestoallrecipients"> </a>

1. EAC에서 **보호** \> **격리**로 이동 합니다.
    
2. 메시지를 클릭 하 여 선택 하거나 shift 키를 사용 하 여 여러 메시지를 선택 합니다. 그런 다음 **메시지 릴리스** 아이콘을 클릭 합니다. 
    
3. 드롭다운 목록에서 **모든 받는 사람에 대해 선택한 메시지 릴리스를** 클릭 합니다. 
    
4. 경고 대화 상자가 열립니다. 경고를 읽고 계속 진행 하려면 **예** 를 선택 합니다. 이 옵션을 선택 하면 메시지를 동일한 받는 사람에 게 두 번 이상 릴리스할 수 없습니다. 받는 사람이 이 메시지를 이전에 수신한 경우 메시지가 해당 받는 사람에게 다시 릴리스되지 않습니다. 
    
### <a name="release-one-or-more-quarantined-messages-to-all-recipients-and-report-false-positives"></a>하나 이상의 격리 된 메시지를 모든 받는 사람에 게 릴리스하고 가양성 보고
<a name="Releaseoneormorequarantinedmessagestoallrecipientsandreportfalsepositives"> </a>

1. EAC에서 **보호** \> **격리**로 이동 합니다.
    
2. 메시지를 클릭 하 여 선택 하거나 shift 키를 사용 하 여 여러 메시지를 선택 합니다. 그런 다음 **메시지 릴리스** 아이콘을 클릭 합니다. 
    
3. **선택한 메시지 릴리스를 클릭 하 고 드롭다운 목록에서 가양성으로 보고** 합니다. 
    
4. 경고 대화 상자가 열립니다. 경고를 읽고 계속 진행 하려면 **예** 를 선택 합니다. 이 옵션을 선택 하면 메시지를 동일한 받는 사람에 게 두 번 이상 릴리스할 수 없습니다. 받는 사람이 이 메시지를 이전에 수신한 경우 메시지가 해당 받는 사람에게 다시 릴리스되지 않습니다. 
    
     스팸으로 격리된 메시지는 Microsoft 스팸 분석 팀에도 보고됩니다. 스팸 격리 된 메시지는 메시지를 평가 및 분석 하는 Microsoft 스팸 분석 팀에도 보고 됩니다. 분석 결과에 따라 메시지 통과를 허용하도록 서비스 전체적으로 스팸 콘텐츠 필터 규칙이 조정될 수 있습니다. 
    
> [!TIP]
> [메시지가 스팸으로 표시 되지](how-to-help-ensure-that-a-message-isn-t-marked-as-spam.md)않도록 하는 방법의 단계에 따라 메시지가 스팸으로 표시 되지 않도록 할 수 있습니다. 
  
새로 고침 아이콘](media/ITPro-EAC-RefreshIcon.gif) **새로**![고침 아이콘을 클릭 하 여 데이터를 새로 고친 다음 해당 메시지를 두 번 클릭 하면 해당 받는 사람에 게 해당 메시지가 해제 된 것을 확인할 수 있습니다. 
  
## <a name="for-more-information"></a>자세한 내용
<a name="sectionSection4"> </a>

[격리 FAQ](quarantine-faq.md)
  

