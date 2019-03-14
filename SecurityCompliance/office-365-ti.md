---
title: Office 365 위협 조사 및 응답
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 03/09/2019
ms.audience: Admin
ms.topic: overview
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 32405da5-bee1-4a4b-82e5-8399df94c512
ms.collection:
- M365-security-compliance
description: office 365 Advanced threat Protection의 위협 인텔리전스 기능을 통해 조직에 대 한 위협을 파악 하 고, 맬웨어, 피싱 및 기타 공격에 대처 하 고 사용자를 대신 하 여 Office 365에서 검색 한 기타 공격과 위협을 검색할 수 있는 방법을 알아봅니다. 슬라이더.
ms.openlocfilehash: e3696306b5188858e6ca72e265c4f1aa24574f79
ms.sourcegitcommit: f25a667e4c7d11c43c87604d576f1e6d6155b14f
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/11/2019
ms.locfileid: "30536188"
---
# <a name="office-365-threat-investigation-and-response"></a>Office 365 위협 조사 및 응답

위협 조사 및 Office 365 Advanced threat Protection의 응답 기능은 보안 분석가와 관리자가 조직의 Office 365 사용자를 보호 하는 데 도움이 됩니다.
  
1. 공격을 쉽게 식별 하 고 모니터링 하 고 이해할 수 있도록 설정
    
2. Exchange online, SharePoint online, 비즈니스용 OneDrive 및 Microsoft 팀의 위협에 빠르게 문제를 해결 하는 데 도움을 줍니다.
    
3. 조직에서 공격을 방지 하는 데 도움이 되는 정보를 제공 합니다.

4. 중요 전자 메일 기반 위협에 대 한 자동화 된 조사 및 응답
    
> [!IMPORTANT]
> **office 365 advanced threat protection 및 위협 조사 및 응답 (이전에 office 365 위협 인텔리전스)은 이제 특정 구독에 포함 된 office 365 advanced threat protection 2의 일부입니다** [. microsoft 365 enterprise](https://www.microsoft.com/microsoft-365/enterprise/home), [microsoft 365 Business](https://www.microsoft.com/microsoft-365/business), office 365 Enterprise E5, office 365 교육용 A5 등입니다. 조직에서 Office 365 ATP를 포함 하지 않는 구독을 사용 하는 경우 ATP를 추가 기능으로 구입할 수 있습니다. 자세한 내용은 [office 365 advanced threat protection 요금제 및 가격](https://products.office.com/exchange/advance-threat-protection) 및 [office 365 advanced threat protection 서비스 설명을](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description#whats-new-in-office-365-advanced-threat-protection-atp)참조 하세요. 
  
## <a name="whats-changing"></a>변경 된 기능

이전의 office 365 위협 조사 및 응답 기능은 office 365 Enterprise E5와 같은 구독에 포함 되었습니다. 여전히 이러한 기능을 사용할 수 있으며, 이제 이러한 기능은 office 365 Advanced Threat Protection 계획 2에 포함 되어 있으며,이는 office 365 Enterprise E5에 들어 있습니다. 

또한 office 365 위협 조사 및 응답 capbailities는 이전에 office 365 for business 고객을 위한 추가 기능으로 구매할 수 있었습니다. 이제 이러한 기능은 office 365 advanced threat protection 계획 2 (office 365 advanced threat protection plan 1 포함)에 포함 되어 있습니다. 자세한 내용은 [Office 365 Advanced Threat Protection 요금제 및 가격 책정](https://products.office.com/exchange/advance-threat-protection)를 참조 하세요.

이 모든 것을 의미 하는 것은 다음과 같습니다.

- **조직에 이미 Office 365 Enterprise E5가 있는 경우**Advanced threat Protection 계획 2가 이미 있고, 위협 조사 및 대응 기능도 포함 되어 있습니다.

- **조직에서 이전에 office 365 위협 인텔리전스 (office 365 Advanced threat Protection 제외)** 가 다른 office 365 구독에 대 한 추가 기능으로 사용 되는 경우 office 365 Advanced threat protection 계획 2가 됩니다. 여기에는 Office 365 Advanced Threat Protection 계획 1 및 위협 조사 및 응답 기능이 포함 됩니다. 

- **조직에서 이전에 office 365 advanced threat protection (office 365 위협 인텔리전스)** 을 다른 office 365 구독에 추가 기능으로 사용 하는 경우 office 365 Advanced threat protection 계획 1이 됩니다. 여기에는 Office 365 Advanced threat Protection (위협 조사 및 응답 기능 제외)이 포함 됩니다.

자세한 내용은 [office 365 advanced threat protection 요금제 및 가격](https://products.office.com/exchange/advance-threat-protection) 및 [office 365 advanced threat protection 서비스 설명](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description#whats-new-in-office-365-advanced-threat-protection-atp) 를 참조 하세요.

## <a name="get-started-with-threat-investigaiton-and-response-capabilities"></a>위협 investigaiton 및 응답 기능 시작

다음 리소스를 사용 하 여 Office 365의 위협 조사 및 응답 기능에 대해 자세히 알아보고 조직의 사용자를 보다 안전 하 게 유지 하는 방법을 알아보세요.
  
- [위협 조사 및 응답 시작](get-started-with-ti.md) (필수 역할에 대 한 정보가 포함 됩니다.) 
    
- [위협 추적기에 대해 알아보기-신규 및 중요](threat-trackers.md)
    
- [배달 된 악성 전자 메일 찾기 및 조사](investigate-malicious-email-that-was-delivered.md)
    
- [공격 시뮬레이터 사용](attack-simulator.md)
    
- [Windows Defender Advanced Threat Protection을 통한 위협 조사 및 대응 통합](integrate-office-365-ti-with-wdatp.md)
    
## <a name="related-topics"></a>관련 항목

[Office 365에서 위협 으로부터 보호](protect-against-threats.md)
  
[Office 365 Advanced Threat Protection](office-365-atp.md)
  
[Permissions in the Office 365 Security &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md)
 
