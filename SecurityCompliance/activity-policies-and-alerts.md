---
title: Office 365 Cloud App Security 활동 정책 및 알림
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 01/28/2019
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 367f25d3-10a0-4a91-bdae-70ebb7a79c98
description: Office 365 Cloud App Security를 사용 하 여 활동 정책을 정의 하 여 특정 활동이 발생 하거나 너무 자주 발생 하는 경우 트리거에 경고를 설정 합니다. 정책을 설정 하 여 알림을 트리거하도록 하면 특정 작업에 대 한 알림을 받을 수 있습니다.
ms.openlocfilehash: cfa58182ea35551ca3a3807c23e09c9f87c7be82
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30219768"
---
# <a name="activity-policies-and-alerts-in-office-365-cloud-app-security"></a>Office 365 Cloud App Security 활동 정책 및 알림

|계산 * *\>**|계획 * *\>**|배포 * *\>**|사용률 * * * *|
|:-----|:-----|:-----|:-----|
|[평가 시작](office-365-cas-overview.md) <br/> |[계획 시작](get-ready-for-office-365-cas.md) <br/> |사용자가 여기 있어!  <br/> [다음 단계](anomaly-detection-policies-in-ocas.md) <br/> |[활용 시작](utilization-activities-for-ocas.md) <br/> |
   
Office 365 Cloud App Security를 사용 하 여 고급 클라우드 관리 정책은 발생 하거나 자주 발생 하는 특정 작업에 대 한 경고를 트리거합니다. 예를 들어 사용자가 Office 365에 로그인 하려고 하면 1 분 안에 70 시간이 실패 한다고 가정 합니다. 다른 사용자가 다른 위치에 있는 경우 7000 파일을 다운로드 하거나, 사용자가 캐나다에서 로그인 한 것 처럼 보이는 경우를 가정해 보겠습니다. 다른 사람의 계정이 손상 되 고 공격자가 해당 계정을 사용 하 여 조직의 클라우드 앱 및 중요 한 데이터에 액세스 하는 경우를 가정해 보겠습니다.
  
[전역 관리자 또는 보안 관리자](permissions-in-the-security-and-compliance-center.md)인 경우 활동 경고는 이러한 이벤트가 발생 하는 경우 사용자에 게 알립니다. 그런 다음 사용자 계정을 일시 중단 하는 등의 특정 작업을 수행 하 여 어떤 일이 발생 했는지 조사할 수 있습니다.
  
> [!NOTE]
> office 365 Cloud App security 정책은 [office 365 보안 &amp; 및 준수 센터의 경고 정책과](alert-policies.md)다릅니다. 이 문서에서 설명 하는 활동 정책은 Office 365 Cloud App Security portal에서 정의 되며 조직의 클라우드 환경을 보다 효율적으로 관리 하는 데 도움이 될 수 있습니다. 
  
## <a name="before-you-begin"></a>시작하기 전에

다음 사항을 확인합니다.
  
- 조직에 [Office 365 Cloud App Security](office-365-cas-overview.md)가 있고 서비스를 사용 [하도록 설정](turn-on-office-365-cas.md)되어 있습니다.
    
- Office 365 환경에 대 한 [감사 로깅이](turn-audit-log-search-on-or-off.md) 설정 되어 있어야 합니다. 
    
- Office 365에 대 한 전역 관리자 또는 보안 관리자 여야 합니다.
    
## <a name="create-a-new-activity-policy"></a>새 활동 정책 만들기

1. 전역 관리자 또는 보안 관리자로 이동 하 여 Cloud App security portal ([https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com))로 이동한 후 로그인 합니다. <br>이렇게 하면 Office 365 Cloud App Security 정책 페이지로 이동 합니다.<br>![Office 365 Cloud App Security 포털로 이동 하면 정책 페이지부터 시작 합니다.](media/5cb8833c-4e08-438c-bab3-91b5106f6f3f.png)
  
2. **정책 만들기**를 클릭 한 다음 **활동 정책을**선택 합니다.<br>![O365 CAS에서 정책을 만들 때 활동 정책 및 변칙 검색 정책 중에서 선택할 수 있습니다.](media/79f34535-ddf9-4a5b-a0a3-8766bf9c174c.png)
  
3. **활동 정책 만들기** 페이지에서 **정책 이름** 및 **설명을**지정 합니다. 기본 서식 파일을 기반으로 정책을 만들려면 **정책 서식 파일** 목록에서 하나를 선택 하거나 서식 파일을 사용 하지 않고 고유한 정책을 만듭니다.<br>![Office 365 Cloud App Security를 사용 하 여 작업 정책을 만들 수 있습니다.](media/4083a76f-7074-4d6a-8200-6d76d49259d7.png)
  
4. 이 정책이 경고를 표시할 경우 얼마나 심각한 지를 측정 하는 **정책 심각도** (낮음, 중간 또는 높음)를 선택 합니다. 이렇게 하면 나중에 검토할 때 알림을 필터링 하는 데 도움이 됩니다. 
    
5. 이 정책의 **범주** 를 선택 합니다. 이렇게 하면 트리거된 알림을 필터링 하 고 정렬 하는 데 도움이 되며, 변경 작업을 수행할 때이를 검토할 때 그룹 정책이 적용 됩니다. 
    
6. 이 정책에 따라 알림을 트리거하는 다른 작업 또는 메트릭을 설정 하려면 **활동 필터** 를 선택 합니다. 
    
7. **작업 일치 매개 변수**에서 단일 활동이 필터와 일치 하는 경우 정책 위반이 트리거되는지, 아니면 경고가 트리거 되기 전에 지정 된 수의 반복 작업이 필요한 지 여부를 지정 합니다.<br>반복 되는 **활동**을 선택 하는 경우 활동 수, 기간 및 위반을 특정 앱 내의 사용자에 대해 허용할지, 아니면 다른 앱을 사용 하는 동일한 사용자에 대해 실행할지를 지정 합니다.
    
8. 필요에 따라 알림 **만들기** 를 선택 하 여 전자 메일, 문자 메시지 또는 둘 다를 통해이 정책에서 알림을 수신 하는 추가 알림을 만들 수 있습니다.<br>**전자 메일 공급자가 보낸 `no-reply@cloudappsecurity.com`전자 메일을 차단 하지 않는지 확인 **합니다. 
  
9. 사용자를 일시 중단 하거나 사용자가 Office 365 앱에 다시 로그인 하도록 요구 하는 경고가 트리거될 때 수행 해야 하는 **작업** 을 선택 합니다. 
    
10. **만들기** 를 선택 하 여 정책 만들기를 마칩니다. 
    
## <a name="next-steps"></a>다음 단계

- [변칙 검색 정책](anomaly-detection-policies-in-ocas.md)
    
- [siem 서버 통합](integrate-your-siem-server-with-office-365-cas.md)
    
- [경고 검토 및 알림 작업 수행](review-office-365-cas-alerts.md)
    
- [관리를 간소화 하는 IP 주소 그룹화](group-your-ip-addresses-in-ocas.md)
    

