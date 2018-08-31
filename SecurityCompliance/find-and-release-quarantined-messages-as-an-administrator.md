---
title: 관리자로 격리된 메시지 찾기 및 릴리스
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 6/16/2017
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: ab95bf17-bb09-4dd1-9990-ddd02ddecf05
description: 이 항목 방법에 대해 설명 Exchange Online 및 Exchange Online Protection (EOP) 관리자 수, 릴리스, Exchange 관리 센터 (EAC)에서 격리 된 메시지를 보고 합니다.
ms.openlocfilehash: a8c450471d2fe627346b5bea8db50b91d67ffd3f
ms.sourcegitcommit: e9dca2d6a7838f98bb7eca127fdda2372cda402c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/21/2018
ms.locfileid: "23003277"
---
# <a name="find-and-release-quarantined-messages-as-an-administrator"></a>관리자로 격리된 메시지 찾기 및 릴리스

이 항목 방법에 대해 설명 Exchange Online 및 Exchange Online Protection (EOP) 관리자 수, 릴리스, Exchange 관리 센터 (EAC)에서 격리 된 메시지를 보고 합니다. Office 365 중 하나를 격리로 메시지를 전달 스팸으로 식별 된 대로 또는 일치 하는 전송 규칙 때문입니다. 
  
보안을 사용 하 여 &amp; EAC 보기 뿐 아니라 이러한 작업 중 하나를 완료 하 고 맬웨어를 포함 하기 때문에 격리로 전송 된 메시지와 함께 작동 하는 대신 준수 센터입니다. 자세한 내용은 [Office 365에서 전자 메일 메시지를 격리를](https://support.office.com/article/Quarantine-email-messages-in-Office-365-4c234874-015e-4768-8495-98fcccfc639b)참조 하십시오.
  
격리 된 메시지는 EAC에서 **격리** 페이지에 나열 됩니다. 기본적으로 메시지를 **받은 날짜** 에서 가장 오래 된 최신 필드에서 정렬 됩니다. 각 메시지에 대 한 **보낸사람**, **주제**및 **만료 날짜** 값도 표시 됩니다. 이러한 필드 중 하나에 해당 머리글을 클릭 하 여 정렬할 수 있습니다. 두번째 시간, 열 머리글을 클릭 하는 경우 정렬 순서를 반대로 바꿉니다. **격리** 페이지에는 최대 500 메시지를 표시 합니다. 
  
모든 격리 된 메시지의 목록을 볼 수 또는 필터 조건을 지정 하 여 특정 메시지를 검색할 수 있습니다 (필터링 수도 줄일 수 사용자의 결과 집합 500 개가 넘는 메시지가 있는 경우). 에 대 한 검색 하 고 격리 된 특정 메시지를 찾은 후 메시지에 대 한 세부 정보를 볼 수 있습니다. 또한 다음을 수행할 수 있습니다.
  
- 하나 이상의 받는 사람에 게 메시지를 해제 하 고 필요에 따라 평가 하 고 메시지를 분석 Microsoft 스팸 분석 팀에 false 가양성 (정크 아님) 메시지로 보고할 합니다. 분석의 결과 따라 서비스 수준 스팸 콘텐츠 필터 규칙을 통해 메시지를 허용 하도록 조정 될 수 있습니다.
    
- 메시지를 해제 하 고 해당 보낸에서 이후의 모든 메시지를 허용 합니다.
    
## <a name="what-do-you-need-to-know-before-you-begin"></a>시작하기 전에 알아야 할 내용
<a name="sectionSection0"> </a>

- 이 절차를 수행 하기 전에 사용 권한을 할당 해야 합니다. 필요한 사용 권한을 [Exchange Online의 기능 사용 권한](http://technet.microsoft.com/library/15073ce1-0917-403b-8839-02a2ebc96e16.aspx) 항목의 "격리" 항목을 참조 하십시오. 
    
- 릴리스 수도 있고 **격리** 페이지에서 한번에 여러 메시지를 보고할 수 있습니다. 또는이 작업을 수행 하기 위해 원격 Windows PowerShell 스크립트를 만들 수 있습니다. 메시지를 검색 하려면 [Get-quarantinemessage](http://technet.microsoft.com/library/88026da1-8dbc-49e7-80e8-112a32773c34.aspx) cmdlet 및 해제 하는 [릴리스 QuarantineMessage](http://technet.microsoft.com/library/4a3aa05c-238f-46f2-b8dd-b0e3c38eab3e.aspx) cmdlet을 사용 합니다. 
    
- 이 항목의 절차에 적용할 수 있는 바로 가기 키에 대한 자세한 내용은 **Exchange 관리 센터의 바로 가기 키**을 참조하세요.
    
> [!TIP]
> 문제가 있습니까? Exchange 포럼에서 도움을 요청하세요. 포럼 주소는 다음과 같습니다.[Exchange Server](https://go.microsoft.com/fwlink/p/?linkId=60612),[Exchange Online](https://go.microsoft.com/fwlink/p/?linkId=267542), 또는 [Exchange Online Protection](https://go.microsoft.com/fwlink/p/?linkId=285351) 
  
## <a name="use-advanced-search-to-filter-and-locate-quarantined-messages"></a>고급 검색을 사용하여 격리된 메시지 필터링 및 찾기
<a name="BKMK_UseAdvancedSearchtoFilterMessages"> </a>

EAC(Exchange 관리 센터)에서 고급 검색을 사용하여 여러 조건에 따라 격리된 항목을 필터링할 수 있습니다. 이러한 조건은 따로 사용할 수도 있고 조합하여 사용할 수도 있습니다. 검색에서는 모든 필터 조건을 충족하는 메시지 목록이 제공됩니다.
  
1. EAC에서 **보호** 로 이동 \> **격리**, **고급 검색**을 클릭 하 고 있습니다.
    
2. **고급 검색** 창에서 다음 조건 중 임의의 조합 하 여 선택 합니다. 각 조건을 사용 하도록 설정 하려면 연결된 확인란을 선택 합니다. 와일드 카드가 지원 되지 않습니다. 
    
1. **메시지 ID** 특정 메시지에 대 한 대상으로 지정 된 검색을 수행 하려면이 매개 변수를 사용할 수 있습니다. 예, 하 여 특정 메시지를 보내거나 이용 하 여 조직에서 사용자 하 고 해당 대상에 도달 하면 하지를 하는 경우 메시지 추적 기능을 사용 하 여 메시지에 대 한 검색할 수 있습니다. 세부 정보를 [실행 하는 메시지 추적 및 결과 보기를](http://technet.microsoft.com/library/74a9fc59-7e0e-4832-baf9-2a86418b0079.aspx)참조 하십시오. 사용자를 격리에 보낸 메시지를 발견 한 경우 아마도 규칙과 일치 하거나, 스팸으로 확인 되었습니다 때문에 다음 쉽게 찾을 수이 메시지를 격리에 id. 해당 메시지를 지정 하 여 전체 메시지 ID 문자열을 포함 해야 합니다. 여기에 꺾쇠 괄호 포함 될 수 있습니다 (\<\>). 
    
2. **보낸 사람 전자 메일 주소** 메시지를 보낸 사람의 전자 메일 주소를 지정합니다. 
    
3. **받는 사람 전자 메일 주소** 메시지를 받는 사람의 전자 메일 주소를 지정합니다. 
    
4. **제목** 메시지의 제목 줄 텍스트를 지정합니다. 
    
5. **수신** 지난 24 시간 내 ( **오늘**), 지난 주 ( **지난 7 일**) 내에 속하는 지난 48 시간 ( **마지막 2 일**) 내에서 격리 하 여 받은 메시지를 선택 하거나 메시지를 하는 동안 사용자가 지정한 시간 간격을 선택할 수 있습니다. 사용자를 격리 하 여 수신 합니다. 
    
6. **만료** 다음 24 시간 내 ( **오늘**), 다음 주 ( **다음 7 일**) 내에서 다음 48 시간 ( **다음 2 일**) 내에서 메시지가 격리에서 삭제 또는 하는 동안 사용자가 지정한 시간 간격을 선택할 수 있습니다를 선택할 수 있습니다는 메시지 격리에서 삭제 됩니다.
    
    > [!IMPORTANT]
    > 기본적으로 스팸 격리 메시지를 전송 규칙과 일치 하는 격리 된 메시지는 7 일이에 대 한 사용자를 격리에 보관 되는 동안 15 일 동안 격리에 보관 됩니다. Office 365이이 기간 후 메시지를 삭제 하 고 검색할 수 없습니다. 전송 규칙과 일치 하는 격리 된 메시지에 대 한 보존 기간을 구성할 수는 없습니다. 그러나 콘텐츠 필터 정책에서 **보관 스팸 (일)에 대 한** 설정을 통해 스팸 격리 된 메시지에 대 한 보존 기간을 낮출 수 있습니다. 자세한 내용은 [스팸 필터 정책 구성](configure-your-spam-filter-policies.md)을 참조 하십시오. 
  
7. **유형** **스팸**으로 식별되어 격리된 메시지를 검색할지 아니면 **전송 규칙**과 일치한 메시지를 검색할지를 지정할 수 있습니다.
    
3. **확인**을 클릭하여 고급 검색 실행을 시작합니다. 
    
    > [!NOTE]
    > 검색 조건을 지우고 격리의 모든 메시지를 보려면 **고급 검색** 창에서 모든 확인란의 선택을 취소하고 **확인**을 클릭합니다. 
  
메시지를 검색하고 나면 지정한 조건과 일치하는 결과가 사용자 인터페이스에 표시됩니다. EAC에서는 메시지를 500개까지 표시할 수 있습니다. 
  
## <a name="view-details-about-a-specific-quarantined-message"></a>격리된 특정 메시지에 대한 세부 정보 보기
<a name="BKMK_ViewDetailsAboutaSpecificQuarantinedMessage"> </a>

**격리** 페이지에서 특정 격리 된 메시지를 찾은 후에 대 한 세부 정보를 볼 수 있습니다. 
  
1. **격리** 페이지에서 특정 메시지를 선택 하 고 해당 메시지의 속성 요약이 화면 오른쪽의 세부 정보 창에 표시 합니다. 
    
    **메시지 상태** 값은 다음과 같습니다. 
    
  - **유형** 메시지가 **스팸**으로 식별되었는지 아니면 **전송 규칙**과 일치했는지를 나타냅니다.
    
  - **만료 날짜** 메시지가 격리에서 삭제되는 날짜입니다. 
    
    **메시지 정보** 값은 다음과 같습니다. 
    
  - **보낸 사람** 메시지를 보낸 사람의 전자 메일 주소입니다. 
    
  - **제목** 메시지의 제목 줄 텍스트입니다. 
    
  - **받은 날짜** 격리에서 메시지를 받은 날짜입니다. 
    
  - **크기** 메시지의 크기입니다. 단위는 KB 또는 MB(메시지 크기가 999KB를 초과하는 경우)입니다. 
    
  - **메시지 헤더 보기** 메시지 헤더 텍스트를 확인할 수 있는 **메시지 헤더** 대화 상자를 열려면 이 링크를 클릭합니다. 메시지 헤더 텍스트를 클립보드에 복사한 다음 [메시지 헤더 분석기](https://testconnectivity.microsoft.com/?tabid=mha)에 붙여 넣을 수도 있습니다. 메시지 헤더 분석기 도구가 표시되면 **헤더 분석**을 클릭하여 헤더에 대한 정보를 검색합니다. 
    
    > [!TIP]
    > 서비스에서 삽입하는 특정 스팸 방지 메시지 헤더 필드에 대한 자세한 내용은 [스팸 방지 메시지 헤더](anti-spam-message-headers.md)를 참조하세요. 
  
  - **전자 메일 메시지 미리 보기** 메시지의 텍스트를 검토 하려면이 링크를 클릭 합니다. 
    
2. 격리된 메시지를 두 번 클릭하면 **격리된 메시지** 창이 열리고 다음 정보가 표시됩니다. 
    
  - **릴리스됨** 메시지가 릴리스된 사용자(있는 경우)의 모든 전자 메일 주소가 포함된 목록입니다. 
    
  - **아직 릴리스되지 않음** 메시지가 아직 릴리스되지 않은 사용자(있는 경우)의 모든 전자 메일 주소가 포함된 목록입니다. **릴리스됨** 링크를 클릭하면 메시지를 릴리스할 수 있습니다. 메시지 릴리스에 대한 자세한 내용은 다음 섹션을 참조하세요. 
    
  - **메시지 ID** 메시지 헤더에 있는 인터넷 메시지 ID(클라이언트 ID라고도 함)입니다. 
    
    **닫기**를 클릭하여 기본 격리 창으로 돌아갑니다. 
    
## <a name="release-messages-from-quarantine"></a>격리에서 릴리스 메시지
<a name="sectionSection3"> </a>

받는 사람에 게 메시지를 해제 하려면 사용자 옵션은 같습니다.
  
- [격리 된 메시지 릴리스 및 이후 메시지를 보낸 사람에 게 허용](find-and-release-quarantined-messages-as-an-administrator.md#Releasequarantinedmessageallowfuturemessagesfromsender)
    
- [특정 받는 사람에 게 격리 된 메시지를 가양성으로 보고 하지 않고 릴리스](find-and-release-quarantined-messages-as-an-administrator.md#Releasequarantinedmessagetospecificrecipientswithoutreportingasfalsepositive)
    
- [모든 받는 사람에 게 하나 이상의 격리 된 메시지 릴리스](find-and-release-quarantined-messages-as-an-administrator.md#Releaseoneormorequarantinedmessagestoallrecipients)
    
- [모든 받는 사람 및 보고서 가양성을 하나 이상의 격리 된 메시지 릴리스](find-and-release-quarantined-messages-as-an-administrator.md#Releaseoneormorequarantinedmessagestoallrecipientsandreportfalsepositives)
    
### <a name="release-a-quarantined-message-and-allow-future-messages-from-the-sender"></a>격리 된 메시지 릴리스 및 이후 메시지를 보낸 사람에 게 허용
<a name="Releasequarantinedmessageallowfuturemessagesfromsender"> </a>

1. EAC에서 **보호** 로 이동 \> **격리**합니다.
    
2. 메시지를 선택한 다음 화면에 표시 된 대로 **메시지 릴리스** 아이콘을 클릭 합니다를 클릭 합니다. 
  
![강조 표시된 메시지 릴리스 아이콘 및 표시된 릴리스 옵션이 포함된 격리 페이지를 보여줍니다.](media/36ee081f-3e30-40c9-8ce3-240cee1970cc.png)
  
드롭다운 목록에서 **선택한 메시지를 릴리스하고 보낸사람 허용** 을 클릭 합니다. 
    
3. **메시지 릴리스 및 보낸사람 허용** 대화 상자가 열립니다. 필요에 따라 **해제 하 고 허용**을 클릭 한 다음 메시지를 Microsoft에 보고를 선택할 수 있습니다. 메시지를 발표 될 예정에 게 배달 되 모든 받는 사람에 게 하 고이 보낸 이후의 모든 메시지를 허용 됩니다. 그러나이 메시지는 전송 규칙으로 인해 격리 된 보낸 사람이 차단 되는 경우를 앞으로 메시지를 차단 하도록 보낸사람 계속 됩니다. 
    
### <a name="release-a-quarantined-message-to-specific-recipients-without-reporting-it-as-a-false-positive"></a>특정 받는 사람에 게 격리 된 메시지를 가양성으로 보고 하지 않고 릴리스
<a name="Releasequarantinedmessagetospecificrecipientswithoutreportingasfalsepositive"> </a>

1. EAC에서 **보호** 로 이동 \> **격리**합니다.
    
2. 메시지를 선택 하 고 **메시지 릴리스** 아이콘을 클릭 한 다음 드롭다운 목록에서 **특정 받는 사람에 게 메시지 릴리스를** 클릭 합니다. 
    
3. **메시지 릴리스** 대화 상자에서 다음 옵션 중 하나를 선택합니다. 
    
  - **모든 받는 사람에게 메시지 릴리스** 이 옵션을 선택하면 메시지를 동일한 받는 사람에게 두 번 이상 릴리스할 수 없습니다. 받는 사람이 이 메시지를 이전에 수신한 경우 메시지가 해당 받는 사람에게 다시 릴리스되지 않습니다. 
    
  - **지정 된 받는 사람에 게 메시지 릴리스** 누구에 게 메시지를 해제할 수 있는 받는 사람을 선택 합니다. 하므로 메시지 각 받는 사람에 게 적용할에 해제 될 수 받는 사람에만이 목록에 표시 한 후에 해제할 수 있습니다. 다중 선택이 지원 됩니다. 받는 사람 선택 항목에 확인 한 후 **추가**클릭 합니다.
    
4. **릴리스**를 클릭합니다. 
    
**새로고침**단추를 누르면![새로고침 아이콘](media/ITPro-EAC-RefreshIcon.gif) 데이터를 새로 고치고, 메시지를 두번클릭 한 다음 아이콘 것 릴리스된 의도 한 받는 사람에 게 표시 됩니다. 
  
### <a name="release-one-or-more-quarantined-messages-to-all-recipients"></a>모든 받는 사람에 게 하나 이상의 격리 된 메시지 릴리스
<a name="Releaseoneormorequarantinedmessagestoallrecipients"> </a>

1. EAC에서 **보호** 로 이동 \> **격리**합니다.
    
2. 선택 하거나 여러 메시지를 선택 하려면 shift 키를 사용 하 여 메시지를 클릭 합니다. **메시지 릴리스** 아이콘을 클릭 합니다. 
    
3. 드롭다운 목록에서 **모든 받는 사람에 게 선택 된 메시지 릴리스를** 클릭 합니다. 
    
4. 경고 대화 상자가 열립니다. 이 경고를 읽고 진행 하려는 경우 **예** 를 선택 합니다. 이 옵션을 선택 하는 경우 유의 동일한 받는 사람에 게 메시지를 여러 번 해제할 수 없습니다. 받는 사람이 메시지를 받은 이전에 하는 경우 하지 발표 될 예정 다시 해당 받는 사람에 게 있습니다. 
    
### <a name="release-one-or-more-quarantined-messages-to-all-recipients-and-report-false-positives"></a>모든 받는 사람 및 보고서 가양성을 하나 이상의 격리 된 메시지 릴리스
<a name="Releaseoneormorequarantinedmessagestoallrecipientsandreportfalsepositives"> </a>

1. EAC에서 **보호** 로 이동 \> **격리**합니다.
    
2. 선택 하거나 여러 메시지를 선택 하려면 shift 키를 사용 하 여 메시지를 클릭 합니다. **메시지 릴리스** 아이콘을 클릭 합니다. 
    
3. 드롭다운 목록에서 **릴리스 선택한 메시지와 가양성으로 보고서를** 클릭 합니다. 
    
4. 경고 대화 상자가 열립니다. 이 경고를 읽고 진행 하려는 경우 **예** 를 선택 합니다. 이 옵션을 선택 하는 경우 유의 동일한 받는 사람에 게 메시지를 여러 번 해제할 수 없습니다. 받는 사람이 메시지를 받은 이전에 하는 경우 하지 발표 될 예정 다시 해당 받는 사람에 게 있습니다. 
    
     이 옵션을 선택 하는 경우 모든 받는 사람에 게 아직 수신 되지 않은 메시지 발표 될 예정입니다. 스팸 격리 된 메시지를 평가 하 고 메시지를 분석 Microsoft 스팸 분석 팀에도 보고 됩니다. 분석의 결과 따라 서비스 수준 스팸 콘텐츠 필터 규칙을 통해 메시지를 허용 하도록 조정 될 수 있습니다. 
    
> [!TIP]
> 보장 [메시지가 스팸으로 표시 되지 않음 되었는지 보장 하는 방법](how-to-help-ensure-that-a-message-isn-t-marked-as-spam.md)의 단계를 수행 하 여 메시지가 스팸으로 표시 되지 않습니다. 
  
**새로고침**단추를 누르면![새로고침 아이콘](media/ITPro-EAC-RefreshIcon.gif) 데이터를 새로 고치고, 메시지를 두번클릭 한 다음 아이콘 것 릴리스된 의도 한 받는 사람에 게 표시 됩니다. 
  
## <a name="for-more-information"></a>자세한 내용
<a name="sectionSection4"> </a>

[격리 FAQ](quarantine-faq.md)
  

