---
title: 참조 정책, 사례 및 지침
ms.author: tracyp
author: MSFTTracyP
manager: laurawi
ms.date: 12/9/2016
ms.audience: ITPro
ms.topic: reference
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: ff3f140b-b005-445f-bfe0-7bc3f328aaf0
ms.collection:
- M365-security-compliance
description: Microsoft는 다양 한 정책과 절차를 개발 하 고 사용자가 악성 전자 메일, 원치 않는 이메일 또는 악의적으로 보호 하는 데 도움이 되는 몇 가지 업계 모범 사례를 채택 했습니다.
ms.openlocfilehash: a074bb1fbe6fedb9054b98d3723511607fed7304
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32261536"
---
# <a name="reference-policies-practices-and-guidelines"></a>참조: 정책, 사례 및 지침
  
Microsoft는 웹에서 가장 신뢰할 수 있는 사용자 환경을 제공 하기 위해 노력 하 고 있습니다. 따라서 Microsoft는 다양 한 정책 및 절차를 개발 하 고 사용자가 악성 메일, 원치 않음 또는 악의 있는 이메일을 방지 하는 데 도움이 되는 여러 업계 모범 사례를 채택 했습니다. 보낸 사람이 Office 365 사용자에 게 전자 메일을 보내려고 시도 하는 경우이 문서의 지침에 따라 이러한 작업을 수행 하 고 잠재적인 배달 문제를 방지 하는 데 도움이 됩니다.
  
이러한 정책 및 지침을 준수 하지 않는 경우 지원 팀이 도움을 드릴 수 없습니다. 이 문서에서 설명 하는 지침, 사례 및 정책에 따라 보내는 IP 주소를 기반으로 하는 배달 문제가 여전히 발생 하 고 있는 경우에는 단계에 따라 목록 이외의 요청을 제출 하십시오. 자세한 내용은 [목록 해제 포털을 사용 하 여 Office 365 수신 거부 목록에서 자신 제거](use-the-delist-portal-to-remove-yourself-from-the-office-365-blocked-senders-lis.md)를 참조 하세요.
  
## <a name="general-microsoft-policies"></a>일반 Microsoft 정책
<a name="GenMsftPolicies"> </a>

전자 메일 전송 office 365 사용자가 전자 메일 전송 및 office 365 사용을 관리 하는 모든 Microsoft 정책을 준수 해야 합니다.
  
- Office 365에 해당 하는 서비스 약관 특히, prohibition에서 서비스를 사용 하 여 스팸을 보내거나 맬웨어를 배포 하는 것을 방지 합니다.
    
- [Microsoft 서비스 계약](https://www.microsoft.com/servicesagreement/)
    
## <a name="governmental-regulations"></a>정부 규정
<a name="GovtRegulations"> </a>

전자 메일 전송 Office 365 사용자는 해당 하는 관할지의 전자 메일 통신을 규제 하는 모든 관련 법률 및 규정을 준수 해야 합니다.
  
- [CAN-스팸 Act: 비즈니스에 대 한 준수 가이드](https://www.ftc.gov/tips-advice/business-center/guidance/can-spam-act-compliance-guide-business)
    
- ["내 정보 제거" 응답 및 책임: 전자 메일 Marketers "구독 취소" 클레임을 준수 해야 함](https://www.lawpublish.com/ftc-emai-marketers-unsubscribe-claims.mdl)
    
## <a name="technical-guidelines"></a>기술 지침
<a name="TechGuidelines"> </a>

Office 365로 전송 되는 전자 메일은 아래 문서에 나열 된 적용 가능한 권장 사항을 준수 해야 합니다 (일부 링크는 영어로만 제공 됨).
  
- [RFC 2505: SMTP mta에 대 한 스팸 방지 권장 사항](https://www.ietf.org/rfc/rfc2505.txt)
    
- [RFC 2920: 명령 파이프라이닝에 대 한 SMTP 서비스 확장](https://www.ietf.org/rfc/rfc2920.txt)
    
또한 Office 365에 연결 하는 전자 메일 서버는 다음 요구 사항을 충족 해야 합니다.
  
- 보낸 사람은 인터넷 전자 메일의 전송에 대 한 모든 기술 표준과 rfc 5321, rfc 5322 등을 비롯 한 IETF (인터넷 엔지니어링 작업 강제 실행)를 통해 게시 되는 모든 기술적 표준을 준수 해야 합니다. 
    
- 500과 599 사이에 숫자 SMTP 오류 응답 코드가 지정 된 후 (영구 배달 응답이 나 NDR이 라고도 함) 보낸 사람은 해당 메시지를 해당 받는 사람에 게 다시 전송 하지 않아야 합니다.
    
- 배달 못 함 응답이 여러 개 있으면 보낸 사람은 해당 받는 사람에 게 전자 메일을 보내기 위한 추가 시도를 중단 해야 합니다.
    
- 보안 되지 않은 전자 메일 릴레이 또는 프록시 서버를 통해 메시지를 전송 해서는 안 됩니다.
    
- 구독 취소에 대 한 메커니즘은 개별 목록 또는 보낸 사람이 호스트 하는 모든 목록을 명확 하 게 문서화 하 고 받는 사람에 게 간편 하 게 찾아서 사용할 수 있도록 해야 합니다.
    
- 동적 IP 공간에서의 연결을 허용 하지 않을 수 있습니다.
    
- 전자 메일 서버에는 유효한 역방향 DNS 레코드가 있어야 합니다.
    
## <a name="reputation-management"></a>신뢰도 관리
<a name="RepManagement"> </a>

보낸 사람, ISP 및 기타 서비스 공급자는 아웃 바운드 IP 주소의 신뢰도를 적극적으로 관리 해야 합니다.
  
## <a name="office-365-limits"></a>Office 365 제한
<a name="sectionSection4"> </a>

보낸 사람은 [Exchange Online Protection 제한](https://technet.microsoft.com/library/exchange-online-protection-limits.aspx)에 나열 된 Office 365 제한을 준수 해야 합니다.
  
## <a name="email-delivery-resources-and-organizations"></a>전자 메일 배달 리소스 및 조직
<a name="sectionSection5"> </a>

Microsoft는 인터넷 및 전자 메일 에코 시스템을 개선 하기 위해 업계 바디 및 서비스 공급자와 활발 하 게 작동 합니다. 이러한 조직은 지 원하는 모범 사례 문서를 제공 했으며 보낸 사람이 준수 하는 것이 권장 됩니다. 이렇게 하면 전 세계 여러 전자 메일 서비스 공급자 간에 전자 메일을 배달 하는 기능이 향상 됩니다.
  
- [메시징 맬웨어 모바일 불건전 사용 작업 그룹](https://www.m3aawg.org/)
    
- [온라인 신뢰 동맹](https://www.otalliance.org/resources)
    
- [전자 메일 &amp; 보낸 사람 공급자 Coalition](http://www.espcoalition.org/)
    
## <a name="abuse-and-spam-reporting"></a>불건전 및 스팸 보고
<a name="AbuseSpamReports"> </a>

불법적, 악성 글, 원치 않는 전자 메일 등을 보고 하려면 [웹용 Outlook에서 정크 메일 및 피싱 사기를 신고 ](report-junk-email-and-phishing-scams-in-outlook-on-the-web-eop.md)하세요. 이러한 유형의 통신을 전송 하는 것은 Microsoft 정책 위반 및 확인 된 보고서에 대 한 적절 한 작업을 수행 하는 것입니다.
  
## <a name="law-enforcement"></a>법 집행
<a name="sectionSection7"> </a>

사법 기관 구성원 인 경우 Office 365에 대 한 법적 설명서를 제공 하거나 microsoft에 제출한 법적 설명서에 대 한 질문이 있는 경우에는 (1) (425) 722-1299을 (를) 호출 해 보세요.
  

