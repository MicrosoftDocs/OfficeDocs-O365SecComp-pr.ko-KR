---
title: 정책, 사례 및 지침을 참조 합니다.
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 12/9/2016
ms.audience: ITPro
ms.topic: reference
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
ms.assetid: ff3f140b-b005-445f-bfe0-7bc3f328aaf0
description: Microsoft가 다양 한 정책, 절차를 개발 하 고 악성, 악의적인 또는 원치 않는, 전자 메일에서 사용자에 게 보호를 위해 여러 업계 모범 사례를 적용 합니다.
ms.openlocfilehash: 436f564f20d579c56197563c7bfac3ef903be750
ms.sourcegitcommit: 22bca85c3c6d946083d3784f72e886c068d49f4a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/06/2018
ms.locfileid: "22026275"
---
# <a name="reference-policies-practices-and-guidelines"></a>참조: 정책, 사례 및 지침
  
Microsoft 전용 내리도록 지원 웹에서 가장 신뢰할 수 있는 사용자 경험을 제공 합니다. Microsoft 다양 한 정책, 절차, 개발 및 사용자에 게 악성, 악의적인 또는 원치 않는, 전자 메일에서 보호를 위해 여러 업계 모범 사례를 채택 했습니다. Office 365 사용자에 게 전자 메일을 보낼 하려고 하는 보낸 사람은 자신이 완벽 하 게 이해 하 고이 작업에 도움이 되 고 잠재적 배달 문제를 방지 하려면이 문서의 지침 팔 로우 확인 해야 합니다.
  
이러한 정책 및 지침을 준수 하지 경우 도움을 주고 또는 지원팀에 대 한 가능한 되지 않을 수 있습니다. 지침, 사례 및이 문서에서 설명 하는 정책을 준수 하 고 여전히에 보내는 IP 주소를 기반으로 배달 문제 발생 하는 경우에 delisting 요청을 제출 하는 단계를 수행 하십시오. 자세한 내용은 [Office 365 수신된 거부 목록에서 자신을 제거 하려면 delist 포털을 사용 하 여](use-the-delist-portal-to-remove-yourself-from-the-office-365-blocked-senders-lis.md)참조 하십시오.
  
## <a name="general-microsoft-policies"></a>일반 Microsoft 정책
<a name="GenMsftPolicies"> </a>

Office 365 사용자에 게 보내는 전자 메일 전자 메일 전송 및 Office 365의 사용을 관리 하는 모든 Microsoft 정책 준수 해야 합니다.
  
- Office 365;에 적용할 수 있는 서비스 약관 특히, 서비스를 사용 하 여 스팸 또는 맬웨어를 배포에 대해 금지
    
- [Microsoft 서비스 계약](https://www.microsoft.com/servicesagreement/)
    
## <a name="governmental-regulations"></a>정부 규제
<a name="GovtRegulations"> </a>

Office 365 사용자에 게 보내는 전자 메일은 모든 관련 법률과 및 해당 관할지의 전자 메일 알림 관리 규정을 준수 해야 합니다.
  
- [스팸 Act: 비즈니스에 대 한 규정 준수 안내선](https://www.ftc.gov/tips-advice/business-center/guidance/can-spam-act-compliance-guide-business)
    
- ["나에 게 제거" 응답 및 책임: 전자 메일 마케팅 담당자 "구독을 취소 하려면" 클레임을 준수 해야 합니다](https://www.lawpublish.com/ftc-emai-marketers-unsubscribe-claims.mdl)
    
## <a name="technical-guidelines"></a>기술 지침
<a name="TechGuidelines"> </a>

Office 365로 전송 하는 전자 메일 (일부 링크는 영어로) 아래 문서에 나열 된 해당 권장 준수 해야 합니다.
  
- [SMTP Mta에 대 한 RFC 2505: 스팸 방지 권장 사항](https://www.ietf.org/rfc/rfc2505.txt)
    
- [명령 파이프라인에 대 한 RFC 2920: SMTP 서비스 확장](https://www.ietf.org/rfc/rfc2920.txt)
    
또한 Office 365에 연결 하는 전자 메일 서버는 다음 요구 사항을 준수 해야 합니다.
  
- 보낸 사람이 게시 하 여 The 인터넷 사회 Internet Engineering Task Force (IETF), RFC 5321, RFC 5322 및 다른 사용자를 포함 하 여 인터넷 전자 메일 전송에 대 한 모든 기술 표준을 준수 예정입니다. 
    
- 500 599 (로 알려져 영구 배달 못함 응답 또는 NDR) 사이의 숫자 SMTP 오류 응답 코드, 제공 된 후 해당 받는 사람에 게 해당 메시지를 재전송 하면 보낸 사람이 해야 시도 하지 않습니다.
    
- 여러 배달 못함 응답 한 후 보낸 해야 작동이 중단 추가 하려고 하면 해당 받는 사람에 게 전자 메일을 보냅니다.
    
- 안전 하지 않은 전자 메일 릴레이 또는 프록시 서버를 통해 메시지를 전송 되어야 합니다.
    
- 개별 목록 또는 보낸 사람이 호스트 하는 모든 목록에서 구독 취소 메커니즘 명확 하 게 문서화 하 고를 찾아 사용 하 여 받는 사람에 게 쉽게 이어야 합니다.
    
- 동적 IP 공간에서 연결을 사용할 수 없습니다.
    
- 전자 메일 서버에는 유효한 역방향 DNS 레코드가 있어야 합니다.
    
## <a name="reputation-management"></a>신뢰도 관리
<a name="RepManagement"> </a>

보낸사람, ISP에 및 다른 인터넷 서비스 공급자에 아웃 바운드 IP 주소의 신뢰도 관리 적극적으로 해야 합니다.
  
## <a name="office-365-limits"></a>Office 365 제한
<a name="sectionSection4"> </a>

[Exchange Online Protection 제한](https://technet.microsoft.com/library/exchange-online-protection-limits.aspx)에 나열 된 Office 365 제한 보낸사람 준수 해야 합니다.
  
## <a name="email-delivery-resources-and-organizations"></a>전자 메일 배달 리소스 및 조직
<a name="sectionSection5"> </a>

Microsoft는 적극적으로 인터넷 및 전자 메일 에코 시스템을 개선 하기 위해 업계 본문 및 서비스 공급자와 함께 작동 합니다. 이러한 조직은 모범 사례 문서를 지원 하 고 보낸 사람이를 따르는 것이 좋습니다.를 게시 합니다. 이 전세계 여러 전자 메일 서비스 공급자 간의 전자 메일을 제공 하는 사용자 능력을 향상 시킵니다.
  
- [메시징 맬웨어 모바일 방지 오용 작업 그룹](https://www.m3aawg.org/)
    
- [온라인 신뢰 제휴](https://www.otalliance.org/resources)
    
- [보낸 전자 메일을 &amp; 공급자 연합](http://www.espcoalition.org/)
    
## <a name="abuse-and-spam-reporting"></a>오용 및 스팸 보고
<a name="AbuseSpamReports"> </a>

불법적인, 악성, 악의적인 또는 원치 않는 전자 메일을 보고, [웹에 있는 Outlook에서 전자 메일 및 피싱 사기 정크 보고서 ](report-junk-email-and-phishing-scams-in-outlook-on-the-web-eop.md)하십시오. 이러한 유형의 통신을 보내는 Microsoft 정책 위반 하는 것 및 확인 된 보고서에서 적절 한 작업을 수행 합니다.
  
## <a name="law-enforcement"></a>법 집행
<a name="sectionSection7"> </a>

법 집행의 구성원 이어야 하 고 Microsoft Corporation Office 365에 대 한 법적 설명서와 함께 작동 하도록 시키려는 하거나 Microsoft에 제출 했는지 법적 설명서에 대 한 질문이 있는 경우, (1) (425) 722-1299를 호출 하십시오.
  

