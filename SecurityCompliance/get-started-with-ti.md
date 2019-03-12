---
title: Office 365 위협 조사 및 응답을 시작 합니다.
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 03/10/2019
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 38e9b67f-d188-490f-bc91-a1ae4b270441
ms.collection:
- M365-security-compliance
description: Office 365 위협 조사 및 응답 및 시작 하는 방법에 대해 알아봅니다.
ms.openlocfilehash: 3e77e79a38da10ed80a611d93dbd55ab9cfc0fda
ms.sourcegitcommit: 6e8e2b43a4bea31c1e835c5b050824651c6a0094
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/11/2019
ms.locfileid: "30537625"
---
# <a name="get-started-with-threat-investigation-and-response"></a>위협 조사 및 응답 시작 

조직의 보안 팀에 속해 있는 경우 Office 365 위협 조사 및 응답 기능을 사용 하 여 공격 으로부터 사용자를 보호할 수 있습니다. office 365 Advanced threat Protection 계획 2 (이전의 office 365 위협 인텔리전스)에서는 보안 분석가와 관리자가 사용자에 게 정보를 버블링 하 고 Office 365 환경에서 발생 하는 작업을 식별 하는 방법을 제공 하는 방법을 제공 합니다. 이러한 정보는 위협 인텔리전스 데이터 및 시스템에 대 한 포괄적인 리포지토리를 기반으로 공격 동작과 의심 스러운 활동에 해당 하는 패턴을 강조 하는 데 사용 됩니다.
  
이 문서를 읽으면 위협 인텔리전스 및 시작 방법에 대해 자세히 알아볼 수 있습니다.
  
## <a name="what-are-the-threat-investigation-and-response-capabilities-included-in-office-365"></a>Office 365에 포함 된 위협 조사 및 응답 기능은 무엇 인가요?

위협 조사 및 응답은 위협 및 관련 응답 작업에 대 한 정보를 파악 하 고 Office 365 보안 &amp; 및 준수 센터에서 사용할 수 있는 도구 모음을 제공 합니다. 이러한 통찰력은 조직의 보안 팀이 전자 메일 또는 파일 기반 공격 으로부터 Office 365 사용자를 보호 하는 데 도움이 될 수 있습니다. 이 기능은 신호를 모니터링 하 고 사용자 활동, 인증, 전자 메일, 손상 된 pc 및 보안 인시던트와 같은 여러 원본의 데이터를 수집 하는 데 도움이 됩니다. 비즈니스 의사 결정권자 및 Office 365 전역 관리자, 보안 관리자 및 보안 분석가는이 정보를 사용 하 여 Office 365 사용자에 대 한 위협을 파악 하 고 대응 하 고 지적 재산을 보호할 수 있습니다.

> [!IMPORTANT]
> office 365 위협 인텔리전스는 이제 추가 위협 방지 기능을 사용 하 여 office 365 Advanced Threat protection 계획 2를 제공 합니다. 자세한 내용은 [office 365 advanced threat protection 요금제 및 가격](https://products.office.com/exchange/advance-threat-protection) 및 [office 365 advanced threat protection 서비스 설명을](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description)참조 하세요.
  
## <a name="get-acquainted-with-the-threat-dashboard-explorer-and-incidents"></a>위협 대시보드, 탐색기 및 인시던트 숙지

[위협 대시보드](get-started-with-ti.md#dashboard), [위협 탐색기](get-started-with-ti.md#explorer), [인시던트](get-started-with-ti.md#incidents), 공격 등 &amp; 을 비롯 한 도구 및 응답 워크플로 집합으로, 보안 및 준수 센터의 위협 조사 및 응답 capabiltiies surface [ 시뮬레이터](attack-simulator.md)및 자동화 된 조사 & 응답
  
### <a name="threat-dashboard"></a>위협 대시보드

위협 대시보드 ( [보안 대시보드](security-dashboard.md)라고도 함)를 사용 하 여 해결 된 위협을 빠르게 확인 하 고, Office 365 서비스가 비즈니스를 보호 하는 방법을 비즈니스 의사 결정권자에 게 보고 하는 방법을 설명 합니다.
  
![위협 대시보드](media/ce013a31-3f80-4d09-bb95-bfb7623b8bc4.png)
  
이 대시보드 &amp; 를 보고 사용 하려면 보안 및 준수 센터에서 **위협 관리** \> **대시보드로**이동 합니다.
  
### <a name="threat-explorer"></a>위협 탐색기

위협 탐색기 (이 라고도 함)를 사용 하 여 위협을 분석 하 고, 시간에 따른 공격 량을 확인 하 고, 위협 계열, 침입자 인프라 등을 기준으로 데이터를 분석 합니다. 위협 탐색기는 모든 보안 분석가의 조사 워크플로에서 시작 되는 위치입니다.
  
![위협 탐색기](media/7a7cecee-17f0-4134-bcb8-7cee3f3c3890.png)
  
이 보고서 &amp; 를 보고 사용 하려면 보안 및 준수 센터에서 **위협 관리** \> **탐색기**로 이동 합니다.
  
 ### <a name="incidents"></a>인시던트

문제 목록 (조사가 라고도 함)을 사용 하 여 비행 보안 인시던트 목록을 확인 합니다. 인시던트는 의심 스러운 전자 메일 메시지와 같은 위협을 추적 하 고 추가 조사 및 수정을 수행 하는 데 사용 됩니다.
  
![Office 365의 현재 위협 인시던트 목록](media/acadd4c7-d2de-4146-aeb8-90cfad805a9c.png)
  
조직의 현재 인시던트 &amp; 목록을 보려면 보안 및 준수 센터에서 **위협 관리** \> **검토** \> **인시던트**로 이동 합니다.
  
![보안 &amp; 및 준수 센터에서 위협 관리 \> 검토를 선택 합니다.](media/e0f46454-fa38-40f0-a120-b595614d1d22.png)
  
## <a name="learn-more-about-malware-amp-threats"></a>맬웨어 &amp; 위협에 대 한 자세한 정보

보안 분석가는 Office 365 Advanced Threat Protection 계획 2 제공의 일부로 알려진 위협에 대 한 세부 정보를 검토할 수 있습니다. 이 기능은 사용자가 안전 하 게 유지 하기 위해 수행할 수 있는 추가 예방 조치/단계가 있는지 여부를 확인 하는 데 유용 합니다.
  
![최근 위협에 대 한 정보를 보여 주는 보안 경향](media/11e7d40d-139b-4c56-8d52-c091c8654151.png) 
  
## <a name="how-do-we-get-these-threat-investigation-and-response-capabilities"></a>이러한 위협 조사 및 응답 기능은 어떻게 얻을 수 있나요?

office 365 위협 Invesigation 및 응답 기능은 Office 365 Advanced Threat Protection 계획 2 및 Enterprise E5에 포함 되어 있습니다. 

> [!TIP]
> 조직의 office 365 구독에 이러한 위협 조사 및 응답 기능이 포함 되어 있지 않은 경우 office 365 Advanced threat Protection과 함께 추가 기능으로 구매할 수 있습니다. 계획 옵션에 대 한 자세한 내용은 office [365 플랫폼 서비스 설명: office 365 보안 &amp; 및 준수 센터](https://docs.microsoft.com/office365/servicedescriptions/office-365-platform-service-description/office-365-securitycompliance-center) 및 [비즈니스용 office 365 용 추가 기능 구입 또는 편집](https://docs.microsoft.com/office365/admin/subscriptions-and-billing/buy-or-edit-an-add-on)을 참조 하세요.
  
1. office 365 전역 관리자 인 경우로 이동 [https://portal.office.com](https://portal.office.com) 하 여 office 365에 대 한 회사 또는 학교 계정을 사용 하 여 로그인 합니다. 
    
2. **관리자 ** \> ** 청구**을 선택하여 현재 구독에 포함된 내용을 확인합니다. 
    - **office 365 Enterprise E5**가 표시 되 면 조직에 office 365 위협 인텔리전스가 있는 것입니다. 
    - **office 365 enterprise E3** 또는 **office 365 enterprise E1**과 같은 다른 구독을 볼 수 있는 경우 위협 인텔리전스를 추가 하는 것이 좋습니다. 이 작업을 수행 하려면 **+ 구독 추가**를 선택 합니다.
    
3. Office 365 관리 센터에서 **사용자** \> **활성 사용자**를 선택합니다.
    
5. 모든 활성 사용자에 게 Office 365 위협 인텔리전스 라이선스를 할당 합니다. (위협 인텔리전스에 대 한 라이선스가 있는 사용자만 보고서 (예: Explorer)에 표시 됩니다.)
    
6. Office 365 Advanced Threat Protection으로 작업할 조직의 사용자에 게 역할을 할당 합니다. [사용자에 게 Office 365 보안 &amp; 및 준수 센터에 대 한 액세스 권한을 부여](grant-access-to-the-security-and-compliance-center.md)하 고 다음 표를 참조 하세요.<br/>

  |**이 작업을 수행 하려면 ...** <br/> |**다음 역할 중 하나가 있어야 합니다.** <br/> |  
  |:-----|:-----|
  |위협 대시보드 (또는 새 [보안 대시보드](security-dashboard.md)) 사용<br/> 최근 또는 현재 위협에 대 한 정보 보기  <br/> |Office 365 전역 관리자  <br/> 보안 관리자 (보안 &amp; 및 준수 센터에서 할당 됨)  <br/> 보안 독자 (보안 &amp; 및 준수 센터에서 할당 됨)  <br/> |
  |위협 탐색기 (탐색기 라고도 함) 사용  <br/> 위협 분석  <br/> |Office 365 전역 관리자  <br/> 보안 관리자 (보안 &amp; 및 준수 센터에서 할당 됨)  <br/> 보안 독자 (보안 &amp; 및 준수 센터에서 할당 됨)  <br/> |
  |인시던트 보기 (조사가 라고도 함) <br/> 인시던트에 전자 메일 메시지 추가  <br/> |Office 365 전역 관리자  <br/> 보안 관리자 (보안 &amp; 및 준수 센터에서 할당 됨)  <br/> 보안 독자 (보안 &amp; 및 준수 센터에서 할당 됨)  <br/> |
  |인시던트에서 전자 메일 작업 트리거  <br/> 의심 스러운 전자 메일 메시지 찾기 및 삭제  <br/> |Office 365 전역 관리자 또는 보안 관리자  <br/> 위 역할과 검색 및 제거 (보안 &amp; 및 준수 센터에서 할당 됨) 중 하나  <br/> |
  |Windows Defender Advanced threat Protection과 Office 365 위협 인텔리전스 통합  <br/> siem 서버에 Office 365 위협 인텔리전스 통합  <br/> |Office 365 전역 관리자  <br/> 보안 관리자 (보안 &amp; 및 준수 센터에서 할당 됨)  <br/> 추가 응용 프로그램에서 할당 되는 적절 한 역할 (예: Windows Defender Advanced Threat Protection portal 또는 siem server)  <br/> |
   
역할, 역할 그룹 및 권한에 대 한 자세한 내용은 [Office 365 보안 &amp; 및 준수 센터의 사용 권한을](permissions-in-the-security-and-compliance-center.md)참조 하세요.
    
## <a name="next-steps"></a>다음 단계

- [위협 추적기에 대해 알아보기-신규 및 중요](threat-trackers.md)
    
- [배달 된 악성 전자 메일 찾기 및 조사 (Office 365 위협 조사 및 응답)](investigate-malicious-email-that-was-delivered.md)
    
- [Windows Defender Advanced Threat Protection을 사용 하 여 Office 365 위협 조사 및 응답 통합](integrate-office-365-ti-with-wdatp.md)
    
- [공격 시뮬레이터에 대 한 자세한 정보](attack-simulator.md)
  

