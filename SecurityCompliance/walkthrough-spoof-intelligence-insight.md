---
title: 연습에서 인텔리전스 통찰력을 스푸핑
ms.author: krowley
author: kccross
ms.date: 7/30/2018
ms.audience: ITPro
ms.topic: overview
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 59a3ecaf-15ed-483b-b824-d98961d88bdd
description: 새 스푸핑 인텔리전스 통찰력은 어떻게 작동 하는지 확인 하세요.
ms.openlocfilehash: 83fa1580a0e7c4717581cc5f23b8f525d6b918e0
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30220328"
---
# <a name="walkthrough-spoof-intelligence-insight"></a>연습: 지능 통찰력 스푸핑

스푸핑 인텔리전스 통찰력을 사용 하 여 인증 되지 않은 전자 메일을 합법적으로 전송 하는 보낸 사람을 빠르게 확인할 수 있습니다. 그들에 게 스푸핑된 메시지를 보낼 수 있도록 허용 하면 가양성이 사용자에 게 노출 되는 위험을 줄이는 데 도움이 됩니다.
  
또한 스푸핑 인텔리전스 모니터를 사용 하 고 허용 된 도메인 쌍을 관리 하 여 추가 보안 계층을 제공 하 고 안전 하지 않은 메시지가 조직에 도착 하지 못하게 할 수도 있습니다.
  
회사 또는 학교 계정에 Office 365 전역 관리자, &amp; 보안 관리자 또는 보안 독자 권한이 부여 된 경우 보안 및 준수 센터에서 스푸핑 인텔리전스 정보를 사용할 수 있습니다. 자세한 내용은 [Office 365 보안 &amp; 및 준수 센터의 사용 권한을](permissions-in-the-security-and-compliance-center.md)참조 하세요.
  
[Office 365 보안 &amp; 및 준수 센터에서 보고서 및 통찰력](reports-and-insights-in-security-and-compliance.md)을 처음 사용할 경우 대시보드를 통해 통찰력 및 권장 작업으로 쉽게 이동할 수 있는 방법을 확인 하는 데 도움이 될 수 있습니다.
  
보안 &amp; 및 준수 센터에서 둘 이상의 대시보드에서 스푸핑 인텔리전스 정보를 볼 수 있습니다. 현재 보고 있는 대시보드에 상관 없이, 통찰력은 동일한 세부 정보를 제공 하며 동일한 작업을 빠르게 수행할 수 있도록 합니다.
  
다음은 보안 &amp; 및 준수 센터에 대 한 몇 가지 연습 중 하나입니다. 보고서 및 insights를 탐색 하는 방법에 대 한 자세한 내용은 관련 항목 섹션의 연습을 참조 하십시오.
  
## <a name="getting-to-the-spoof-intelligence-insight-in-the-security-amp-compliance-center"></a>보안 &amp; 및 준수 센터에서 스푸핑 인텔리전스 통찰력 얻기

1. 시작 하려면 [보안 &amp; 및 준수 센터로 이동](go-to-the-securitycompliance-center.md)해야 합니다.
    
2. 보안 &amp; 및 준수 센터에서 **위협 관리** \> **대시보드로 이동 합니다.**
    
3. **Insights** 행에서 스푸핑 인텔리전스 통찰력을 찾습니다. 스푸핑 인텔리전스를 사용 하도록 설정한 경우에는 **최근 30 일의 인증에 실패 한 스푸핑된 도메인**이라는 통찰력을 갖게 됩니다. 스푸핑 방지를 사용 하도록 설정 하지 않은 경우 타이틀 **스푸핑 방지 보호**사용을 통해 확인 메시지가 표시 됩니다. 
    
## <a name="about-the-insight-on-the-dashboard"></a>대시보드의 통찰력 정보

대시보드에 대 한 통찰력에는 다음과 같은 정보가 나와 있습니다.
  
![스푸핑 인텔리전스 통찰력 스크린샷](media/28aeabac-c1a1-4d16-9fbe-14996f742a9a.png)
  
이 통찰력에는 두 가지 모드가 있습니다.
  
 **통찰력 모드**입니다. 스푸핑 정책이 사용 하도록 설정 된 경우에는 지난 30 일 동안 스푸핑 인텔리전스 기능으로 영향을 받은 메일의 수를 확인할 수 있습니다. 
  
 **if 모드** 스푸핑 정책이 사용 하도록 설정 되어 있지 않은 경우에는 지난 30 일 동안 스푸핑 인텔리전스 기능 ** 으로 영향을 받은 메일의 수를 확인할 수 있습니다. 
  
어느 방법을 통해 파악에 표시 되는 스푸핑된 도메인은 두 범주로 구분 됩니다. 의심 스러운 도메인 쌍 및 의심 스러운 도메인 쌍 이러한 범주는 검토할 세 가지 다른 버킷으로 세분화 됩니다. 
  
*도메인 쌍* 은 "보낸 사람:" 주소와 보내는 인프라를 조합한 것입니다. 
  
- "보낸 사람" 주소는 메일 응용 프로그램에서 보낸 사람 주소로 표시 되는 주소입니다. 이 주소는 전자 메일의 작성자를 식별 합니다. 즉, 메시지 작성을 담당 하는 사람이 나 시스템의 사서함입니다. 이를 5322.from 주소의 주소 라고도 합니다.
    
- 보내는 인프라 또는 보낸 사람은 보내는 IP 주소의 PTR 레코드에 대 한 조직 도메인입니다. 보내는 ip 주소에 PTR 레코드가 없으면 보낸 사람은 255.255.255.0 서브넷 마스크가 CIDR 표기법 (/24) 인 보내는 ip로 식별 됩니다. 예를 들어 IP 주소가 192.168.100.100 이면 보낸 사람의 전체 IP 주소는 192.168.100.100/24가 됩니다.
    
 **의심 스러운 도메인 쌍** 은 다음과 같습니다. 
  
- **신뢰도가 높은 스푸핑** Office 365는 도메인의 신뢰도 점수 및 전송 패턴을 기반으로 이러한 도메인이 의심 스 럽 거는 강력한 신호를 수신 했습니다. Office 365은 도메인이 스푸핑 대상이 고 이러한 도메인에서 전송 된 메시지가 합법적 일 가능성이 낮은 지를 확실 하 게 확신 합니다. 
    
- **보통 신임 스푸핑** Office 365는 도메인의 신뢰도 점수 및 기록 전송 패턴을 기반으로 이러한 도메인이 의심 스 럽 거는 일반 신호를 수신 했습니다. Office 365에서는 도메인이 스푸핑 되 고 이러한 도메인에서 전송 된 메시지가 합법적 인지 확실 하 게 확신 합니다. 이 버킷에는 신뢰도가 높은 위장 버킷 보다 더 많은 FPs가 포함 될 가능성이 높습니다. 
    
 **의심 스 럽 지 않은 도메인 쌍** 에는 자동 **복구 스푸핑이**포함 됩니다. 자동 복구 스푸핑은 명시적 인증 검사 ( [SPF](https://docs.microsoft.com/office365/SecurityCompliance/how-office-365-uses-spf-to-prevent-spoofing), [dkim](https://docs.microsoft.com/office365/SecurityCompliance/use-dkim-to-validate-outbound-email), [DMARC](https://docs.microsoft.com/office365/SecurityCompliance/use-dmarc-to-validate-email))에 실패 했지만 연장 인증 검사를 통과 한 도메인입니다. 따라서 Office 365은 사용자 대신 메일을 자동으로 복구 하며 메일에 대해 스푸핑 방지 작업을 수행 하지 않았습니다. 
  
## <a name="view-detailed-information-about-suspicious-domain-pairs-from-the-spoof-intelligence-insight"></a>스푸핑 인텔리전스 통찰력에서 의심 스러운 도메인 쌍에 대 한 세부 정보 보기

1. 스푸핑 인텔리전스 이해에서 도메인 쌍 (높음, 중간 또는 자동 복구)을 클릭 합니다.
  
승인 되지 않은 메일을 조직으로 보내는 보낸 사람 목록을 보여 주는 **스푸핑 인텔리전스 이해** 페이지가 표시 됩니다. 이 페이지의 정보는 스푸핑된 메시지에 대 한 인증 여부를 결정 하는 데 도움이 되거나 추가 작업을 수행 해야 하는 경우에 유용 합니다. 메시지 수, 스푸핑이 마지막으로 검색 된 날짜 등을 기준으로 정보를 정렬할 수 있습니다. (예를 들어 **메시지 수** 또는 **마지막으로 본**것과 같은 열 머리글을 클릭 합니다.) 
    
2. 테이블에서 항목을 선택 하 여 도메인 쌍에 대 한 다양 한 정보가 포함 된 세부 정보 창 (이 예에서는 사용자가 수행 해야 하는 작업, 보낸 사람에 대 한 WhoIs 데이터 및 같은 보낸 사람에 대 한 테 넌 트에 표시 되는 유사한 전자 메일)을 제공 합니다. 여기에서 **allowedtospoof** 수신 허용-보낸 사람 목록에서 도메인 쌍을 추가 하거나 제거 하도록 선택할 수도 있습니다. 
  
![스푸핑 인텔리전스 통찰력 세부 정보 창에 있는 도메인 스크린샷](media/03ad3e6e-2010-4e8e-b92e-accc8bbebb79.png)
  
## <a name="add-or-remove-a-domain-from-the-allowedtospoof-safe-sender-list"></a>allowedtospoof 수신 허용-보낸 사람 목록에서 도메인 추가 또는 제거

스푸핑 인텔리전스 이해의 세부 정보 창에서 도메인 쌍을 검토 하는 동시에 allowedtospoof 수신 허용-보낸 사람 목록에서 도메인을 추가 하거나 제거 합니다. 이에 따라 토글을 설정 하기만 하면 됩니다.
  
이렇게 하면 스푸핑된 도메인 및 보내는 인프라의 고유한 도메인 쌍 조합이 수정 되며, 격리 된 전체 스푸핑된 도메인 또는 보내는 인프라에 대 한 검사는 제공 되지 않습니다. 예를 들어 다음 도메인 쌍을 ' allowedtospoof ' 보낸 사람 목록: *스푸핑된 도메인* "gmail.com"에 추가 하 고 *인프라* " *tms"를* 보내는 경우 해당 도메인 쌍의 메일만 스푸핑 될 수 있습니다. 다른 보낸 사람이 "gmail.com"로 위장 하려고 하 고 "tms.mx.com" 스푸핑이 시도 하는 다른 도메인은 스푸핑 인텔리전스로 계속 보호 됩니다. 
  
## <a name="related-topics"></a>관련 항목

[스푸핑 인텔리전스에 대해 자세히 알아보기](learn-about-spoof-intelligence.md)
  
[Office 365의 스푸핑 방지 보호 기능](anti-spoofing-protection.md)
  
[연습 - 대시보드에서 통찰력에 이르기까지](from-a-dashboard-to-an-insight.md)
  
[연습 - 자세한 보고서에서 통찰력에 이르기까지](from-a-detailed-report-to-an-insight.md)
  
[연습 - 통찰력에서 자세한 보고서](from-an-insight-to-a-detailed-report.md)
  

