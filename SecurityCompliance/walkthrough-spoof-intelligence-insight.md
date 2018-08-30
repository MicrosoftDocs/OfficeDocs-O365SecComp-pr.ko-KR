---
title: 연습 스푸핑 인텔리전스 정보
ms.author: krowley
author: kccross
ms.date: 7/30/2018
ms.audience: ITPro
ms.topic: overview
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 59a3ecaf-15ed-483b-b824-d98961d88bdd
description: 새 스푸핑 인텔리전스 통찰력 작동 하는 방법을 참조 하십시오.
ms.openlocfilehash: ca9c4ae6f2d65ef2700a2e02acd5b4f1dfbfe903
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22596097"
---
# <a name="walkthrough-spoof-intelligence-insight"></a>연습: 스푸핑 인텔리전스 정보

스푸핑 인텔리전스 필요한 정보를 사용 하 여 어떤 보낸사람 합법적인 전자 메일을 인증 되지 않은 보내는 신속 하 게 확인할 수 있습니다. 위장 된 메시지를 보낼 수 있도록을 허용 하 여 사용자에 게 들어갈 모든 가양성의 위험을 줄일 수 있습니다.
  
또한 있습니다도 스푸핑 인텔리전스 모니터를 사용 하 고 관리할 수는 추가적인 보안을 제공 하 고 안전 하지 않은 메시지 조직에 도착 하는 것을 방지 하려면 허용 된 도메인 쌍입니다.
  
보안에서 스푸핑 인텔리전스 필요한 정보를 사용할 수 &amp; 준수 센터 Office 365 전역 관리자, 보안 관리자 또는 보안 독자 권한이 부여 된 작업이 나 교육용 계정 하는 경우. 자세한 내용은 참조 [Office 365 보안에 대 한 사용 권한을 &amp; 준수 센터](permissions-in-the-security-and-compliance-center.md)합니다.
  
처음 사용 하는 경우 [보고서 및 Office 365 보안에 대 한 의견 &amp; 준수 센터](reports-and-insights-in-security-and-compliance.md), 권장 되는 작업 없으며 방법을 쉽게 탐색할 수 대시보드에서 정보를 확인 하는 데 도움이 될 수 있습니다.
  
보안에서 둘 이상의 대시보드에서 스푸핑 인텔리전스 필요한 정보를 볼 수 &amp; 준수 센터입니다. 보고 하는 대시보드에 관계 없이 파악 같은 세부 정보를 제공 하 고 신속 하 게 동일한 작업을 수행할 수 있습니다.
  
보안에 대 한 여러 연습 중 하나가 &amp; 준수 센터입니다. 보고서 및 인 사이트를 탐색 하는 방법에 대 한 관련된 항목 섹션에서 연습을 확인 합니다.
  
## <a name="getting-to-the-spoof-intelligence-insight-in-the-security-amp-compliance-center"></a>보안에 스푸핑 인텔리전스 필요한 정보를 &amp; 준수 센터

1. 시작 하려면 수행 해야 [보안으로 이동 &amp; 준수 센터](go-to-the-securitycompliance-center.md)합니다.
    
2. 보안에서 &amp; 준수 센터, **위협 관리** 로 이동 \> **대시보드.**
    
3. **정보** 행에서 스푸핑 인텔리전스 견해를 찾습니다. 스푸핑 인텔리전스 사용 하도록 설정한 경우는 통찰력은 자격이 있는 **지난 30 일간의 인증에 실패 하는 Spoofed 도메인**입니다. 스푸핑 보호 기능을 활성화 하지 않은 경우 다음의 통찰력 하 라는 메시지가 나타납니다 제목 **스푸핑 방지 사용**을 사용 하 여 그렇게 합니다. 
    
## <a name="about-the-insight-on-the-dashboard"></a>대시보드에서 정보에 대 한

대시보드에서 견해는 다음과 같은 정보를 표시 합니다.
  
![필요한 정보를 스푸핑할 인텔리전스 스크린샷](media/28aeabac-c1a1-4d16-9fbe-14996f742a9a.png)
  
이 정보는 다음과 같은 두가지 모드가 있습니다.
  
 **필요한 정보를 모드**입니다. 모든 스푸핑 정책을 사용 하는 경우 다음의 정보를 보면 얼마나 많은 메일 영향을 받는 스푸핑 인텔리전스 기능 지난 30 일 동안의 있습니다. 
  
 **경우에 어떻게 모드**합니다. 사용 하도록 설정 하는 모든 스푸핑 정책이 없는 경우 다음의 정보를 보면 *는* 얼마나 많은 메일 된 어떤 영향을 사용해 스푸핑 인텔리전스 기능에 따라 지난 30 일 동안의 있습니다. 
  
두 방법 모두 위장 된 도메인의 정보에 표시 되는 구분 하 여 두 범주로; 의심 스러운 도메인 쌍 및 비 의심 스러운 도메인 쌍입니다. 이러한 범주 검토할 수에 대 한 서로 다른 세 그룹에 다시 나뉩니다. 
  
*도메인 쌍* 은의 조합 된 "에서:" 주소와 보내는 인프라입니다. 
  
- "From" 주소는 전자 메일 응용 프로그램으로 From 주소로 표시 되는 주소입니다. 이 주소는 전자 메일의 작성자를 식별 합니다. 즉, 사용자 또는 메시지를 작성 하는 일을 담당 하는 시스템의 사서함입니다. 이 방법을 5322.From 주소를 라고도 합니다.
    
- 보내는 인프라, 또는 보낸사람은 보내는 IP 주소의 PTR 레코드의 조직 도메인입니다. 보내는 IP 주소에 PTR 레코드가 없는 경우 발신자는 식별 하 여 보내는 IP는 255.255.255.0 서브넷 마스크 CIDR 표기법에서 (/ 24). 예, IP 주소는 192.168.100.100 하는 경우 보낸의 완전 한 IP 주소는 192.168.100.100/24 합니다.
    
 **의심 스러운 도메인 쌍** 은 다음과 같습니다. 
  
- **높은 정확도 스푸핑**합니다. Office 365 강력한 신호 기록 보내는 패턴 및 도메인의 신뢰도 점수가에 따라 이러한 도메인은 의심 스러운을 받았습니다. Office 365 도메인 스푸핑는 하 고는 이러한 도메인에서 보낸 메시지는 경우가 별로 합법적인 고도로 판단 됩니다. 
    
- **보통 신뢰 스푸핑**합니다. Office 365 보통 신호 기록 보내는 패턴 및 도메인의 신뢰도 점수가에 따라 이러한 도메인은 의심 스러운을 받았습니다. Office 365 도메인 스푸핑는 하 고 이러한 도메인에서 보낸 메시지는 합법적인는 보통 수준의 판단 됩니다. 이 버킷이 가양성 (Fp) 보다 높은 정확도 스푸핑 버킷 포함 된 가능성이 높아집니다. 
    
 **비 의심 스러운 도메인 쌍** **스푸핑 구출한**포함 합니다. 자동 복구 스푸핑은 명시적 인증 검사 ( [SPF](https://docs.microsoft.com/office365/SecurityCompliance/how-office-365-uses-spf-to-prevent-spoofing), [DKIM](https://docs.microsoft.com/office365/SecurityCompliance/use-dkim-to-validate-outbound-email) [DMARC](https://docs.microsoft.com/office365/SecurityCompliance/use-dmarc-to-validate-email)) 실패 했지만 확장 된 인증 검사를 통과 하는 도메인입니다. 이 결과 Office 365의 메일 사용자를 대신 하 여 구출한 및 스푸핑 방지 작업 없음의 메일에서 제거 되었습니다. 
  
## <a name="view-detailed-information-about-suspicious-domain-pairs-from-the-spoof-intelligence-insight"></a>스푸핑 인텔리전스 견해에서 의심 스러운 도메인 쌍에 대 한 자세한 정보를 보려면

1. 스푸핑 인텔리전스 통찰력에서 도메인 쌍 (높음, 보통, 또는 자동 복구) 중 하나를 클릭 합니다.
  
**스푸핑 인텔리전스 정보** 페이지는 보낸사람 목록에 전송 하는 인증 되지 않은 메일 조직으로를 보여주는 나타납니다. 이 페이지의 정보는 그렇지 않은지 위장 된 메시지는 권한이 있는지 여부 또는 다른 조치를 취할 필요가 결정 하는데 도움이 됩니다. 메시지 수에 따라 정보는 스푸핑 검색 되었지만 마지막 날짜 등을 정렬할 수 있습니다. (예: 클릭 **메시지를 계산** 하거나 **마지막으로 본**등의 열 머리글.) 
    
2. 도메인 쌍에 대 한 다양 한 정보를 포함 하는 세부 정보 창을 열려면 테이블에서 항목을 선택, 이유는이 발견을 포함 하 여 필요한를 수행 하기 위해 도메인 요약, 보낸사람, 및 동일한 보낸 테 넌 트에 살펴본 유사한 전자 메일에 대 한 WhoIs 데이터입니다. 이 탭에서 추가 또는 **AllowedToSpoof** 수신 허용 목록에서 도메인 쌍을 제거 하려면 선택할 수 있습니다. 
  
![스푸핑 인텔리전스 통찰력 세부 정보 창에서 도메인의 스크린샷](media/03ad3e6e-2010-4e8e-b92e-accc8bbebb79.png)
  
## <a name="add-or-remove-a-domain-from-the-allowedtospoof-safe-sender-list"></a>추가 또는 AllowedToSpoof 수신 허용 목록에서 도메인을 제거 합니다.

추가 또는 스푸핑 인텔리전스 통찰력의 세부 정보 창에서 도메인 쌍을 검토 하는 동안 AllowedToSpoof 수신 허용 목록에서 도메인을 제거 합니다. 단순히의 표시/숨기기를 적절 하 게 설정 합니다.
  
위장 된 도메인 및 송신 인프라의 고유한 도메인 쌍 조합을 수정 하 고 전체 위장 된 도메인 이나 격리 된 상태에서 보내는 인프라에 대 한 범위를 제공 하지 않습니다. 'AllowedToSpoof' 보낸 사람에 게 다음과 같은 도메인 쌍을 추가 하는 경우 허용 목록에 예: *도메인 스푸핑* "gmail.com" 및 *인프라를 보내는* "tms *. mx.com",* 해당 도메인 쌍의 메일만 할 수 있는 스푸핑한 다음 합니다. "Gmail.com" 및 다른 도메인으로 위장 하려고 하면 다른 보낸사람 스푸핑할을 "tms.mx.com" 시도 하 계속 스푸핑 인텔리전스에 의해 보호 됩니다. 
  
## <a name="related-topics"></a>관련 항목

[스푸핑 인텔리전스에 대해 자세히 알아보기](learn-about-spoof-intelligence.md)
  
[Office 365의 스푸핑 방지 보호 기능](anti-spoofing-protection.md)
  
[연습 - 대시보드에서 통찰력에 이르기까지](from-a-dashboard-to-an-insight.md)
  
[연습 - 자세한 보고서에서 통찰력에 이르기까지](from-a-detailed-report-to-an-insight.md)
  
[연습 - 통찰력에서 자세한 보고서](from-an-insight-to-a-detailed-report.md)
  

