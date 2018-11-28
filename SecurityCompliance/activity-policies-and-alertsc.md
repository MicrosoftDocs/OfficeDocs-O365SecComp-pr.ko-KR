---
title: Office 365 Cloud App Security 활동 정책 및 알림
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 2/26/2018
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 367f25d3-10a0-4a91-bdae-70ebb7a79c98
description: Office 365 클라우드 응용 프로그램을 설정 하려면 보안 경고를 특정 활동을 발생 하거나 너무 자주 발생 하는 경우를 트리거할 수를 사용 하 여 작업 정책을 정의 합니다. 경고를 트리거하도록 정책을 설정 하 여에 대 한 알림을 받을 수 및 특정 활동을 모니터링 합니다.
ms.openlocfilehash: ff1f0acd3c622f20bff26f6a77cc686193cf76fc
ms.sourcegitcommit: 2cf7f5bb282c971d33e00f65d9982a3f14aec74e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/27/2018
ms.locfileid: "26706472"
---
# <a name="activity-policies-and-alerts-in-office-365-cloud-app-security"></a>Office 365 Cloud App Security 활동 정책 및 알림

Office 365 고급 보안 관리 Office 365 클라우드 응용 프로그램 보안 되었습니다.
  
|평가 * *\>**|계획 * *\>**|배포 * *\>**|사용률 * * *|
|:-----|:-----|:-----|:-----|
|[평가 시작 합니다.](office-365-cas-overview.md) <br/> |[계획을 시작합니다](get-ready-for-office-365-cas.md) <br/> |여기는!  <br/> [다음 단계](anomaly-detection-policies-in-ocas.md) <br/> |[활용 하 여 시작](utilization-activities-for-ocas.md) <br/> |
   
Office 365 클라우드 응용 프로그램 보안 고급 클라우드 관리 정책 발생 하거나 너무 자주 발생 하는 특정 작업에 대 한 경고를 트리거합니다. 등 사용자 Office 365에 로그인 하 려 하 고 1 분에 70 번 실패 경우를 가정해 보겠습니다. 다른 사용자 7, 000iops 파일을 다운로드 또는 로그인, 캐나다에서 해당 사용자가 다른 위치에 있어야 할 때 나타나는 경우를 가정해 보겠습니다. 또는 심각한 문제 다른 사용자의 계정 암호가 손상 된 하 고 공격자는 해당 계정을 사용 하 여 조직의 클라우드 앱 및 중요 한 데이터에 액세스 하는 경우를 가정해 보겠습니다.
  
[전역 관리자 또는 보안 관리자](permissions-in-the-security-and-compliance-center.md)인 경우 활동 알림을 이러한와 같은 이벤트 될 때 발생 합니다. 셰이프시트에서 변경 된 조사할 수 있을 때까지 사용자 계정을 일시 중단 하는 등의 특정 작업을 할 수 있습니다.
  
> [!NOTE]
> Office 365 클라우드 응용 프로그램 보안 정책에서 서로 다릅니다 [Office 365 보안에서 정책 경고 &amp; 준수 센터](alert-policies.md)합니다. 이 문서에서 설명 하는 정책 Office 365 클라우드 응용 프로그램 보안 포털에 정의 되어 있고 수 높이 데 도움이 활동 조직의 클라우드 환경을 관리 합니다. 
  
## <a name="before-you-begin"></a>시작하기 전에

다음 사항을 확인합니다.
  
- 조직에 [Office 365 클라우드 응용 프로그램 보안](office-365-cas-overview.md)및 서비스를 [설정](turn-on-office-365-cas.md)합니다.
    
- Office 365 환경에 대 한 [감사 로깅](turn-audit-log-search-on-or-off.md) 기능이 켜 집니다. 
    
- 전역 관리자 또는 Office 365에 대 한 보안 관리자는 합니다.
    
## <a name="create-a-new-activity-policy"></a>새 작업 정책 만들기

1. 전역 관리자 또는 보안 관리자로 이동 [https://security.microsoft.com](https://security.microsoft.com) 작업이 나 교육용 계정을 사용 하 여 로그인 하 고 있습니다. 
    
2. 보안에서 &amp; 준수 센터 **알림** 선택 \> **관리 고급 알림**입니다.
    
3. **Office 365 클라우드 응용 프로그램 보안으로 이동**을 선택 합니다.
    
    이 Office 365 클라우드 앱 보안 정책 페이지로 이동 합니다.
    
    ![정책 페이지로 시작 하 여 Office 365 클라우드 응용 프로그램 보안 포털에 이동할 때](media/5cb8833c-4e08-438c-bab3-91b5106f6f3f.png)
  
4. **정책 만들기**클릭 하 고 **작업 정책**을 선택 합니다.
    
    ![O365 CA에서 정책을 만들면 활동 정책과 이상 탐지 정책을 선택할 수 있습니다.](media/79f34535-ddf9-4a5b-a0a3-8766bf9c174c.png)
  
5. **활동 정책 만들기** 페이지에서 **정책 이름** 및 **설명**을 지정 합니다. 정책에 따라 기본 서식 파일의 기반을 **정책 서식 파일** 목록에서 하나를 선택 하거나 서식 파일을 사용 하지 않고 직접 정책을 만듭니다. 
    
    ![Office 365 클라우드 앱 보안이 포함 된 활동 정책을 만들 수 있습니다.](media/4083a76f-7074-4d6a-8200-6d76d49259d7.png)
  
6. **정책 심각도** (낮음, 보통, 또는 높음) 얼마나 심각 하는 것이 경우이 정책에는 경고를 표시할 경우을 측정 하는 선택 합니다. 이렇게 하면 나중에 검토 하는 경우 경고를 필터링 합니다. 
    
7. 이 정책에 대 한 **범주** 를 선택 합니다. 이렇게 하면 필터 및 정렬, 트리거된 알림 또는 변경 하 게 검토 하는 경우 그룹 정책의 합니다. 
    
8. 다른 작업 또는이 정책에 따라 경고를 발생 시키는 메트릭을 설정 하려면 **활동 필터** 를 선택 합니다. 
    
9. **활동 매개 변수와 일치**에서 지정한 수의 반복 해 서 활동 경고 트리거 하기 전에 필요한 경우 또는 단일 활동을 필터에 일치 하는 경우 정책 위반 트리거되는지 여부를 지정 합니다.
    
    **반복 작업**을 선택 하는 경우 활동을 시간 프레임 수를 지정 및 모든 app와 같은 사용자 또는 특정 응용 프로그램 내에서 사용자에 대 한 위반 count가 있는지 여부.
    
10. 필요에 따라 **만들기 경고** 전자 메일, 텍스트 메시지 또는 둘 모두) (통해이 정책에서 알림을 받도록 추가 알림을 만들 수를 선택할 수 있습니다. 
    
    > [!IMPORTANT]
    > 전자 메일 공급자 no-reply@cloudappsecurity.com에서 보낸 전자 메일을 차단 하지 있는지 확인 하십시오. 
  
11. 사용자를 일시 중단 하거나 사용자가 Office 365 응용 프로그램을 다시 로그인 해야 경고가 표시 될 때 취해야 하는 **작업** 을 선택 합니다. 
    
12. 사용자 정책 만들기를 종료 하려면 **만들기** 선택 합니다. 
    
## <a name="next-steps"></a>다음 단계
<a name="nextsteps"> </a>

- [예외 탐지 정책](anomaly-detection-policies-in-ocas.md)
    
- [SIEM 서버 통합](integrate-your-siem-server-with-office-365-cas.md)
    
- [검토 및 알림 작업을 수행 합니다.](review-office-365-cas-alerts.md)
    
- [관리를 단순화 하 여 IP 주소를 그룹화](group-your-ip-addresses-in-ocas.md)
    

