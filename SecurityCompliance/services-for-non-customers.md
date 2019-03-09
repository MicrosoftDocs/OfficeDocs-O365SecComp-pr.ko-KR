---
title: 비 고객을 위한 Office 365 메일을 보내는 서비스
ms.author: tracyp
author: MSFTTracyP
manager: laurawi
ms.date: 5/2/2016
ms.audience: ITPro
ms.topic: overview
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 19fd3e0f-8dbf-4049-a810-2c8ee6cefd48
ms.collection:
- M365-security-compliance
description: 전자 메일을 사용할 때 사용자의 신뢰를 유지 하기 위해 Microsoft는 사용자를 보호 하기 위한 다양 한 정책 및 기술을 배치 했습니다.
ms.openlocfilehash: 868f5491ae9433e115090567b40abcd39ef2ebf8
ms.sourcegitcommit: 5eb664b6ecef94aef4018a75684ee4ae66c486bb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/08/2019
ms.locfileid: "30492797"
---
# <a name="services-for-non-customers-sending-mail-to-office-365"></a>비 고객을 위한 Office 365 메일을 보내는 서비스
  
전자 메일 남용, 정크 메일 및 사기성 전자 메일 (피싱)은 전체 전자 메일 에코에 부담을 주지 않습니다. 전자 메일을 사용할 때 사용자의 신뢰를 유지 하기 위해 Microsoft는 사용자를 보호 하기 위한 다양 한 정책 및 기술을 배치 했습니다. 그러나 Microsoft는 합법적인 전자 메일이 부정적인 영향을 받지 않도록 인식 하 고 있습니다. 따라서 전송 신뢰도를 사전에 관리 하 여 발신자가 Office 365 사용자에 게 전자 메일을 배달 하는 기능을 개선 하는 데 도움이 되는 서비스 제품군을 설정 했습니다.
  
이 개요에서는 Office 365 고객이 아닌 경우에도 조직에 제공 하는 혜택에 대 한 정보를 제공 합니다.
  
## <a name="sender-solutions"></a>보낸 사람 솔루션
<a name="sectionSection0"> </a>

|**서비스**|**이점**|
|:-----|:-----|
|온라인 도움말 콘텐츠  <br/> | 단계별로  <br/>  EOP 사용자에 게 통신을 제공 하는 것과 관련 된 질문에 대 한 시작점  <br/>  여기에는 정책 및 요구 사항이 포함 된 간단한 온라인 가이드가 포함 되어 있습니다.  <br/>  Microsoft에서 사용한 정크 메일 필터 및 인증 기술에 대 한 개요  <br/> |
|[Microsoft 지원](services-for-non-customers.md#AboutSupport) <br/> |배달 문제에 대 한 자가 진단 및 에스컬레이션 지원을 제공 합니다.  <br/> |
|[Office 365 스팸 방지 IP 목록 포털](services-for-non-customers.md#DelistPortal) <br/> |IP 목록 요청을 제출 하는 도구입니다. 이 요청을 제출 하기 전에 해당 IP가 보낸 모든 메일이 악의적이 든 악의적인 지 확인 해야 합니다.  <br/> |
|[Exchange Online에서 보내는 정크 메일에 대 한 불건전 및 스팸 보고](services-for-non-customers.md#ReportOurJunk) <br/> |스팸 및 기타 원치 않는 메일이 Exchange Online에서 전송 되 고 인터넷 및 메일 시스템을 복잡 하 게 유지 합니다.  <br/> |
   
## <a name="microsoft-support"></a>Microsoft 지원
<a name="AboutSupport"> </a>

Microsoft에서는 Office 365 받은 편지함에 메일을 보내는 데 문제가 있는 사용자를 위해 몇 가지 지원 옵션을 제공 합니다. 따라서 다음 작업이 권장됩니다.
  
- 수신 하는 배달 못 함 보고서 (들)의 지침을 따릅니다.
    
- [Office 365로 전송 되는 메일 문제 해결](troubleshooting-mail-sent-to-office-365.md)에서 고객이 직면 하 게 되는 가장 일반적인 문제를 확인 합니다.
    
- [Office 365 목록 해제 포털](https://sender.office.com) 을 사용 하 여 수신 거부 목록에서 IP를 제거 하는 요청을 제출 합니다. 
    
- [Microsoft 커뮤니티 포럼](https://community.office365.com/en-us/f/)을 읽습니다.
    
- 다른 방법을 사용 하 여 전자 메일을 보내려고 하는 Office 365 고객에 게 문의 하 여 사용자에 게 Microsoft 지원에 문의 하 여 지원 티켓을 열도록 요청 합니다. 법적 이유가 있는 경우 Microsoft Support는 차단 되는 IP 공간을 소유한 보낸 사람과 직접 통신 해야 합니다. 그러나 일반적으로 고객은 지원 티켓을 열 수 없습니다.
    
     Office 365에 대 한 Microsoft 기술 지원에 대 한 자세한 내용은 [지원](https://technet.microsoft.com/library/office-365-support.aspx)항목을 참조 하십시오.
    
## <a name="office-365-anti-spam-ip-delist-portal"></a>Office 365 스팸 방지 IP 목록 포털
<a name="DelistPortal"> </a>

이는 Office 365 수신 거부 목록에서 자신을 제거 하는 데 사용할 수 있는 셀프 서비스 포털입니다. 전자 메일 주소가 Office 365에 있는 받는 사람에 게 전자 메일을 보내려고 할 때 오류 메시지가 표시 되는 경우에는이 포털을 사용 하십시오. 자세한 내용은 [목록 해제 포털을 사용하여 Office 365 수신 거부 목록에서 자신 제거](use-the-delist-portal-to-remove-yourself-from-the-office-365-blocked-senders-lis.md)를 참조하세요.
  
## <a name="abuse-and-spam-reporting-for-junk-email-originating-from-exchange-online"></a>Exchange Online에서 보내는 정크 메일에 대 한 불건전 및 스팸 보고
<a name="ReportOurJunk"> </a>

타사에서 Office 365을 사용 하 여 정크 메일을 보내는 경우에는 사용 약관 및 정책을 위반 하 게 됩니다. Office 365에서 정크 메일을 받은 경우 이러한 메시지를 [junk@office365.microsoft.com](mailto:junk@office365.microsoft.com)에 보고할 수 있습니다. RFC 5322 또는 arf 형식으로 전체 메시지 헤더를 포함 하 여 잘못 된 메시지를 첨부 하세요. 웹 사용자의 Outlook은 기본 제공 도구를 사용 하 여 정크 메일을 보고할 수 있습니다. 자세한 내용은 [웹용 Outlook에서 정크 메일 및 피싱 사기 보고 ](report-junk-email-and-phishing-scams-in-outlook-on-the-web-eop.md)를 참조 하세요.
  

