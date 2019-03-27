---
title: EOP 구성을 위한 모범 사례
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 12/9/2016
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.assetid: faf1efd1-3b0c-411a-804d-17f37292eac0
description: 일반적인 구성 오류를 방지하고 구성 설정에 성공하려면 Exchange Online Protection EOP 모범 사례 권장 사항을 따르세요.
ms.openlocfilehash: 3b8cf41be41e199017dcff7fd3762711402d8ca2
ms.sourcegitcommit: c0d4fe3e43e22353f30034567ade28330266bcf7
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/27/2019
ms.locfileid: "30900187"
---
# <a name="best-practices-for-configuring-eop"></a>EOP 구성을 위한 모범 사례
  
일반적인 구성 오류를 방지하고 구성 설정에 성공하려면 Exchange Online Protection EOP 모범 사례 권장 사항을 따르세요. 일반적으로는 기본 구성 설정을 사용하는 것이 좋습니다. 이 항목에서는 설정 프로세스를 이미 완료했다고 가정합니다. EOP 설정을 완료하지 않은 경우 [EOP 서비스 설정](set-up-your-eop-service.md)을 참조하세요.
  
## <a name="use-a-test-domain"></a>테스트 도메인 사용

볼륨이 큰 프로덕션 도메인에서 구현하기 전에 테스트 도메인, 하위 도메인 또는 볼륨이 작은 도메인을 사용하여 서비스 기능을 시험적으로 사용해 보는 것이 좋습니다.
  
## <a name="synchronize-recipients"></a>받는 사람 동기화

조직의 온-프레미스 Active Directory 환경에 기존 사용자 계정이 있는 경우 클라우드의 Azure Active Directory에 해당 계정을 동기화할 수 있습니다. 디렉터리 동기화를 사용하는 것이 좋습니다. 디렉터리 동기화를 사용할 경우의 이점 및 이를 설정하기 위해 수행해야 하는 단계에 대한 자세한 내용은 [EOP에서 메일 사용자 관리](manage-mail-users-in-eop.md)를 참조하세요.
  
## <a name="spf-record-customization-to-help-prevent-spoofing"></a>스푸핑을 방지하기 위한 SPF 레코드 사용자 지정

EOP를 설정할 때 EOP용 SPF(보낸 사람 정책 프레임워크) 레코드를 DNS 레코드에 추가했을 것입니다. SPF 레코드는 스푸핑을 방지하는 데 도움이 됩니다. spf 레코드에서 스푸핑을 방지 하는 방법과 온-프레미스 IP 주소를 SPF 레코드에 추가 하는 방법에 대 한 자세한 내용은 [스푸핑 방지를 위해 Office 365에서 spf를 설정](../set-up-spf-in-office-365-to-help-prevent-spoofing.md)합니다 .를 참조 하세요. 
  
## <a name="set-anti-spam-options"></a>스팸 방지 옵션 설정

IP 허용 및 IP 차단 목록에 IP 주소를 추가하고 **수신 허용 목록 사용** 옵션을 선택하여 연결 필터 설정을 관리하면 수신되는 가양성(스팸으로 분류된 정상 메일) 수가 줄어듭니다. 자세한 내용은 [Configure the connection filter policy](../configure-the-connection-filter-policy.md)을 참고 하십시오. [전체 조직에 적용되는 추가 스팸 설정은 메시지가 스팸으로 표시되지 않는지 확인하는 방법](https://go.microsoft.com/fwlink/p/?LinkId=534224) 또는 [Office 365 스팸 필터로 전자 메일 스팸을 차단하여 거짓 부정 문제 방지](https://go.microsoft.com/fwlink/p/?LinkId=534225)를 참조하세요. 사용자가 관리자 수준 제어를 가지고 있고 가양성이나 거짓 부정을 방지하려고 할 때 유용합니다.
  
기본 설정을 검토 하 고 필요에 따라 변경 하 여 콘텐츠 필터를 관리 합니다. 예를 들어, 스팸 검색 메시지에 미치는 작업을 변경할 수 있습니다. 스팸 필터링에 대 한 적극적인 접근 방법을 사용 하려면 고급 스팸 필터링 옵션을 구성 하면 됩니다. 프로덕션 환경에서 이러한 옵션을 구현 하기 전에 먼저 테스트를 수행 하는 것이 좋으며, 이렇게 설정 하는 것이 피싱에 관심이 있는 조직이 **SPF 레코드: hard fail** 옵션을 사용 하는 것이 좋습니다. 자세한 내용은 [스팸 필터 정책 구성](../configure-your-spam-filter-policies.md) 및 [고급 스팸 필터링 옵션](../advanced-spam-filtering-asf-options.md)을 참고 하세요.
  
> [!IMPORTANT]
> 기본 콘텐츠 필터 동작을 사용 하는 경우 **메시지를 정크 메일 폴더로 이동**하 여이 작업이 온-프레미스 사서함과 함께 작동 하도록 하려면 온-프레미스에서 Exchange 메일 흐름 규칙 (전송 규칙이 라고도 함)을 구성 해야 합니다. EOP에서 추가한 스팸 헤더를 검색 하기 위한 서버 자세한 내용은 [스팸이 각 사용자의 정크 메일 폴더로 라우팅되는지 확인](../ensure-that-spam-is-routed-to-each-user-s-junk-email-folder.md)을 참조하십시오. 
  
아웃 바운드 메일이 배달 되도록 하는 데 도움이 되는 아웃 바운드 메일 모범 사례를 포함 하 여 [스팸 방지 보호 관련 FAQ](../anti-spam-protection-faq.md)를 검토 하는 것이 좋습니다.
  
여러 가지 방법을 통해 거짓 부정(스팸) 및 가양성(스팸 아님) 항목을 Microsoft에 분석용으로 제출할 수 있습니다. 자세한 내용은 분석을 [위해 Microsoft에 스팸, 스팸이 아닌 정보 및 피싱 사기 메시지 제출을](../submit-spam-non-spam-and-phishing-scam-messages-to-microsoft-for-analysis.md)참조 하세요.
  
## <a name="set-anti-malware-options"></a>맬웨어 방지 옵션 설정

EAC(Exchange 관리 센터)에서 맬웨어 필터 설정을 검토하고 세부 조정합니다. 자세한 내용은 [맬웨어 방지 정책 구성](../configure-anti-malware-policies.md)를 참고 하십시오. [맬웨어 방지 보호 관련 FAQ ](../anti-malware-protection-faq-eop.md)에서 맬웨어 방지 보호 기능에 대 한 질문과 대답을 읽어 보는 것도 좋습니다.
  
맬웨어가 포함된 실행 파일이 우려되는 경우 실행 파일이 있는 모든 전자 메일 첨부 파일을 차단하는 Exchange 메일 흐름 규칙을 만들 수 있습니다. exchange online Protection에서 [첨부 파일 차단을](https://support.microsoft.com/kb/2959596) 사용 하 여 exchange online의 [메시지 첨부 파일을 검사 하](https://docs.microsoft.com/exchange/security-and-compliance/mail-flow-rules/inspect-message-attachments#supported-file-types-for-mail-flow-rule-content-inspection)는 방법에 나열 되지 않도록 차단 하기 위해이 문서의 단계를 수행 합니다.
  
EAC의 일반 첨부 파일 유형 필터를 사용할 수 있습니다. **보호** \> **맬웨어 필터**를 선택하세요. 실행 가능한 콘텐츠가 포함 된 모든 전자 메일 첨부 파일을 차단 하는 메일 흐름 규칙을 만들 수 있습니다. 
  
또한 보호 수준을 높이려면 메일 흐름 규칙을 사용하여 ade, adp, ani, bas, bat, chm, cmd, com, cpl, crt, hlp, ht, hta, inf, ins, isp, job, js, jse, lnk, mda, mdb, mde, mdz, msc, msi, msp, mst, pcd, reg, scr, sct, shs, url, vb, vbe, vbs, wsc, wsf, wsh 확장명을 일부 또는 전부를 차단하는 것이 좋습니다. **모든 첨부 파일 확장명에 다음 단어 포함** 조건을 사용하면 됩니다. 
  
관리자와 최종 사용자는 분석을 위해 Microsoft로 보내 필터를 통과하게 만든 맬웨어를 제출하거나 맬웨어로 잘못 식별된 파일을 제출하여 Microsoft로 보내 분석하도록 할 수 있습니다. 자세한 내용은 [Submitting malware and non-malware to Microsoft for analysis](../submitting-malware-and-non-malware-to-microsoft-for-analysis.md)을 참조하세요.
  
## <a name="create-mail-flow-rules"></a>메일 흐름 규칙 만들기

비즈니스 요구를 충족 하기 위해 메일 흐름 규칙 (전송 규칙이 라고도 함) 또는 사용자 지정 필터를 만듭니다.
  
새 규칙을 프로덕션 환경으로 배포할 때는 먼저 테스트 모드 중 하나를 선택하여 규칙의 효과를 확인합니다. 규칙이 원하는 방식으로 작동하면 규칙 모드를 **적용**으로 변경합니다.
  
새 규칙을 배포할 때는 적용된 규칙을 모니터링하기 위해 **문제 보고서 생성** 동작을 추가할 수 있습니다. 
  
조직의 일부는 온-프레미스에 있고 나머지는 Office 365에 있는 하이브리드 배포 구성에서는 전체 조직에 적용되는 규칙을 만들 수 있습니다. 이렇게 하려면 온-프레미스와 Office 365에서 모두 사용 가능한 조건을 사용합니다. 대부분의 조건은 두 배포에서 모두 사용할 수 있지만, 일부 항목은 특정 배포 시나리오에서만 사용 가능합니다. 자세한 내용은 [메일 흐름 규칙 (전송 규칙)에서 Exchange Online을](http://technet.microsoft.com/library/743bd525-0ca2-426d-b76c-b4a052bc8886.aspx)확인 하세요.
  
조직 내에서 전송되는 메시지의 전자 메일 첨부 파일을 조사하려는 경우 메일 흐름 규칙을 설정하면 됩니다. 그런 후 해당 첨부 파일의 내용이나 특성에 따라 조사한 메시지에 대해 작업을 수행할 수 있습니다. 자세한 내용은 [Use mail flow rules to inspect message attachments](http://technet.microsoft.com/library/874d1c78-a8ec-4938-b388-d3208c2fa971.aspx)를 참조하세요.
  
### <a name="phishing-and-spoofing-prevention"></a>피싱 및 스푸핑 방지

개인 정보가 조직을 벗어날 때 전자 메일을 검색하여 피싱 방지 보호를 향상시킬 수 있습니다. 예를 들어 메일 흐름 규칙에서 다음 정규식을 사용하면 개인 재무 데이터 또는 개인 정보를 노출할 수 있는 정보의 전송을 감지할 수 있습니다.
  
- \d\d\d\d\s\d\d\d\d\s\d\d\d\d\s\d\d\d\d(MasterCard/Visa)
    
- \d\d\d\d\s\d\d\d\d\d\d\s\d\d\d\d\d (American Express)
    
- \d\d\d\d\d\d\d\d\d\d\d\d\d\d\d\d(임의의 16자리 숫자)
    
- \d\d\d\-\d\d\-\d\d\d\d(주민 등록 번호)
    
자체 도메인에서 보낸 것으로 표시되는 악의적인 인바운드 전자 메일을 차단하여 스팸 및 피싱을 줄일 수도 있습니다. 예를 들어 회사 도메인에서 동일한 회사 도메인으로 보내는 메시지를 거부하는 메일 흐름 규칙을 만들어 이러한 유형의 보낸 사람 위조를 방지할 수 있습니다.
  
> [!CAUTION]
> 도메인의 적법한 전자 메일을 인터넷에서 메일 서버로 보내는 경우가 전혀 없는 경우에만 이 거부 규칙을 만드는 것이 좋습니다. 이는 조직의 사용자가 외부 받는 사람에게 보낸 메시지가 조직 내의 다른 받는 사람에게 전달되는 경우에는 발생할 수 있습니다. 
  
### <a name="extension-blocking"></a>확장명 차단

맬웨어가 포함된 실행 파일이 우려되는 경우 실행 파일이 있는 모든 전자 메일 첨부 파일을 차단하도록 맬웨어 방지 정책을 구성할 수 있습니다. [맬웨어 방지 정책 구성](../configure-anti-malware-policies.md)의 단계를 따릅니다.
  
보호 수준을 높이려면 ade, adp, ani, bas, bat, chm, cmd, com, cpl, crt, hlp, ht, hta, inf, ins, isp, job, js, jse, lnk, mda, mdb, mde, mdz, msc, msi, msp, mst, pcd, reg, scr, sct, shs, url, vb, vbe, vbs, wsc, wsf, wsh 확장명도 일부 또는 모두 차단하는 것이 좋습니다.
  
## <a name="reporting-and-troubleshooting"></a>보고 및 문제 해결

관리 센터의 보고서를 사용 하 여 일반적인 문제 및 추세 문제를 해결 합니다. 메시지 추적 도구를 사용하면 메시지에 대한 단일 지점 관련 데이터를 찾을 수 있습니다. 보고에 대한 자세한 내용은 [Exchange Online Protection의 보고 및 메시지 추적](reporting-and-message-trace-in-exchange-online-protection.md)을 참조하세요. 메시지 추적 도구에 대한 자세한 내용은 [Trace an Email Message](http://technet.microsoft.com/library/0c83cde6-5b09-4106-8587-c200cdc59094.aspx)을 참조하세요.
  
## <a name="for-more-information"></a>자세한 내용

[EOP 관련 일반 FAQ(질문과 대답)](eop-general-faq.md)
  
[EOP에 대한 도움말 및 지원](help-and-support-for-eop.md)
  
[메시지가 스팸으로 표시되지 않는지 확인하는 방법](https://go.microsoft.com/fwlink/p/?LinkId=534224)
  
[Office 365 스팸 필터로 전자 메일 스팸을 차단하여 거짓 부정 문제 방지](https://go.microsoft.com/fwlink/p/?LinkId=534225)
  

