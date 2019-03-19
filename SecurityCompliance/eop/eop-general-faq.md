---
title: EOP 관련 일반 FAQ(질문과 대답)
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 1/2/2018
ms.audience: ITPro
ms.topic: reference
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
ms.assetid: 9dbff00a-474e-4452-aeb5-5be9a6b8c6d5
description: 다음은 Microsoft EOP(Exchange Online Protection) 클라우드 호스팅 전자 메일 필터링 서비스에 대한 가장 일반적인 질문과 그에 대한 대답입니다. 그 이외의 FAQ(질문과 대답) 항목은 다음 링크를 참조하십시오.
ms.openlocfilehash: 888cf338a3f1767ddd6ba01a2f0f60f2f8794e3e
ms.sourcegitcommit: b688d67935edb036658bb5aa1671328498d5ddd3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/19/2019
ms.locfileid: "30670453"
---
# <a name="eop-general-faq"></a>EOP 관련 일반 FAQ(질문과 대답)

다음은 Microsoft EOP(Exchange Online Protection) 클라우드 호스팅 전자 메일 필터링 서비스에 대한 가장 일반적인 질문과 그에 대한 대답입니다. 그 이외의 FAQ(질문과 대답) 항목은 다음 링크를 참조하십시오.
  
- [EOP 대기, 지연 및 반송 메시지 FAQ](eop-queued-deferred-and-bounced-messages-faq.md)
    
- [위임된 관리 FAQ](delegated-administration-faq.md)
    
- [스팸 방지 보호 기능 FAQ](../anti-spam-protection-faq.md)
    
- [Exchange Online의 수신 허용-보낸 사람 및 수신 거부 목록](../safe-sender-and-blocked-sender-lists-faq.md)
    
- [Quarantine FAQ](../quarantine-faq.md)
    
- [맬웨어 방지 보호 FAQ](../anti-malware-protection-faq-eop.md)
    
- [Message Trace FAQ](http://technet.microsoft.com/library/aa49e3f9-a5b1-4410-aac2-ddbbf3f5bfb2.aspx)
    
- [FOPE to EOP Transition FAQ](http://technet.microsoft.com/library/e0e76b89-b0d3-4c0a-bfc8-137b579e983b.aspx)
    
 **질문. EOP란 무엇입니까?**
  
대답. EOP는 스팸 및 맬웨어로부터 고객을 보호하고 사용자 지정 정책 규칙을 구현하도록 구축된 클라우스 호스트 전자 메일 필터링 서비스입니다.
  
 **질문. EOP 평가판을 등록하거나 EOP를 구입할 수 있는 방법은 어떻게 됩니까?**
  
대답. [Exchange Online Protection 홈 페이지](https://go.microsoft.com/fwlink/p/?LinkId=279912)에서 EOP 평가판을 등록하거나 EOP를 구입할 수 있습니다. 구입한 평가판의 기능은 유료 구독과 동일하지만, [Exchange Online Protection 서비스 설명](https://go.microsoft.com/fwlink/p/?LinkId=320619)에서 설명하는 Exchange Enterprise CAL with Services 구독 계획에서 제공되는 추가 기능도 포함됩니다. 
  
 **질문. EOP 가격은 어떻게 책정됩니까?**
  
대답. EOP는 사용자별로 라이선스가 부여됩니다. 최신 가격 정보는 [Exchange Online Protection 홈 페이지](https://go.microsoft.com/fwlink/p/?LinkId=279912)를 참조하십시오.
  
 **질문. EOP를 프로덕션에 배치하는 데 얼마나 소요됩니까?**
  
대답. MX 레코드를 변경할 경우 [EOP 서비스 설정](set-up-your-eop-service.md) 및 EOP를 통한 메일 흐름에 설명된 단계에 따라 필터링이 즉시 시작됩니다. MX 레코드가 DNS를 통해 전파되려면 24~48시간 정도 소요될 수 있습니다. 이 프로세스 동안 언제든지 EAC(Exchange 관리 센터)에서 보호 설정을 세부적으로 조정할 수 있습니다.
  
 **질문. EOP를 사용하려면 Microsoft Office 365의 모든 기능을 사용해야 합니까? EOP 보호만 사용해도 됩니까?**
  
대답. Office 365의 다른 기능은 사용하지 않고 EOP를 사용하여 온-프레미스 사서함을 보호할 수 있습니다. 이를 독립 실행형 구독이라고 합니다. EOP 기능 목록은 [Exchange Online Protection 서비스 설명](https://go.microsoft.com/fwlink/p/?LinkId=320619)에서 찾을 수 있습니다.
  
 **질문. EOP를 통해 전자 메일 필터링에 등록할 때 Office 365 테넌트가 필요한 이유는 무엇입니까?**
  
대답. Office 365는 Office 365 테넌트를 통해 액세스할 수 있는 제품과 서비스 모음에 지정된 이름입니다. Office 365 테넌트는 전자 메일 필터링용 라이선스를 추가할 수 있는 시작점으로 생각하면 됩니다.
  
 **Q. EOP에도 알려진 문제와 필요한 해결 방법에 대한 정보를 찾을 수 있는 통신 포털이 있습니까? 새로운 기능에 대한 정보는 어떻게 확인할 수 있습니까?**
  
A. Microsoft 365 관리 센터에는 이러한 정보 중 일부가 포함 되어 있습니다. 서비스 수준 이벤트의 영향을 받는 경우 Microsoft 365 관리 센터에 로그인 한 후 통신 경고 (일반적으로 종 아이콘이 함께)가 표시 됩니다. 모든 항목을 읽고 적절한 조치를 취하는 것이 좋습니다.
  
새 EOP 기능과 관련해서 [비즈니스용 Office 365 로드맵](https://office.microsoft.com/en-us/products/office-365-roadmap-FX104343353.aspx)은 향후 출시될 새 기능에 대한 정보를 찾는 데 유용한 리소스입니다. 또한 새로운 기능에 대한 블로그 기사를 [Office 블로그](https://go.microsoft.com/fwlink/p/?LinkId=392724) 웹 사이트에 게시할 예정입니다. 
  
 **질문. Exchange Server 2010 등의 레거시 Exchange 버전 및 Exchange 이외의 환경에서도 서비스가 작동합니까?**
  
대답. 예, 서비스는 서버에 상관없이 사용 가능하며 모든 SMTP 메일 전송 에이전트에서 사용할 수 있습니다.
  
 **질문. 어떤 규모의 조직에서 서비스를 사용할 수 있습니까?**
  
대답. 모든 규모의 조직에서 서비스를 사용할 수 있습니다. EOP 네트워크는 조직의 확장을 수용할 수 있는 충분한 용량을 갖추고 있으므로 조직이 급속하게 확장되더라도 전혀 문제가 되지 않습니다.
  
 **EOP를 설정하려면 어떤 사용 권한이 필요합니까?**
  
EOP를 구성하려면 Office 365 전역 관리자 또는 Exchange 회사 관리자(조직 관리 역할 그룹)여야 합니다.
  
 **질문. 내 데이터와 개인 정보가 안전한지 어떻게 알 수 있습니까?**
  
대답. SLA(서비스 수준 계약)에 대한 정보를 비롯하여 데이터 및 개인 정보의 안전을 확보하기 위해 Microsoft에서 수행한 단계에 대한 자세한 내용을 보려면 [Office 365 보안 센터](https://go.microsoft.com/fwlink/p/?LinkId=285405)를 참조하십시오.
  
 **질문. 메시지 크기 제한 등 주의해야 하는 제한 사항이 있습니까?**
  
A. 예. EOP의 제한에 대한 자세한 내용은 [Exchange Online Protection 제한](https://go.microsoft.com/fwlink/p/?LinkId=402617)을 참조하세요. 
  
 **Q. EOP에서 원격 Windows PowerShell이 지원됩니까?**
  
A. 예, 전체 EOP 기능을 원격 Windows PowerShell을 통해 사용할 수 있습니다. 자세한 내용은 [PowerShell in Exchange Online Protection](http://technet.microsoft.com/library/f7918a88-774a-405e-945b-bc2f5ee9f748.aspx)을 참조하세요.
  

