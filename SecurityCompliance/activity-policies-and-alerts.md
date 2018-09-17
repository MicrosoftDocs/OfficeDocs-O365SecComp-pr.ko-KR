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
ms.openlocfilehash: 6f5039d09dea98de970ab4bd28e95a6cfad73db4
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22533512"
---
# <a name="activity-policies-and-alerts-in-office-365-cloud-app-security"></a>Office 365 Cloud App Security 활동 정책 및 알림

Office 365 고급 보안 관리 Office 365 클라우드 응용 프로그램 보안 되었습니다.
  
|평가 * *\>**|계획 * *\>**|배포 * *\>**|사용률 * * *|
|:-----|:-----|:-----|:-----|
|[평가 시작 합니다.](office-365-cas-overview.md) <br/> |[계획을 시작합니다](get-ready-for-office-365-cas.md) <br/> |여기는!  <br/> [다음 단계](anomaly-detection-policies-in-ocas.md) <br/> |[활용 하 여 시작](utilization-activities-for-ocas.md) <br/> |
   

Office 365 클라우드 앱 시큐리티를 이용하면 특정 활동을 일으키거나 너무 자주 발생하는 활동에 대하여 고급 클라우드 관리 정책이 경고를 발생시킵니다. 예를 들어 사용자의 Office 365에 대한 로그인 시도가 1분에 70번 실패한 경우를 가정해 보겠습니다. 또한, 다른 사용자가 7000개의 파일을 다운로드한다거나 다른 위치에 있어야 할 사용자가 캐나다에 있는 것 처럼 나타나는 경우를 생각해 보겠습니다. 더 나아가, 최악의 상황으로 누군가의 계정이 탈취당하여 공격자가 당신의 조직의 클라우드 앱과 중요한 데이터에 접근하려 한다고 가정해 봅시다.

  
만약 당신이 [전역 관리자 또는 보안 관리자](permissions-in-the-security-and-compliance-center.md)인 경우 이러한 상황일 경우 활동알림이 발생합니다. 당신은 해당 사건에 대하여 조사할 수 있을 때 까지 특정 사용자 계정을 일시적으로 비활성화 하는 등의 작업을 할 수 있습니다.
  
> [!NOTE]
> Office 365 클라우드 앱 시큐리티 정책은 [Office 365 보안 및 규정 준수 센터의 알림 정책](alert-policies.md)과는 다릅니다. 이 문서에서 설명 하는 정책은 Office 365 클라우드 앱 시큐리티 포털에 정의 되어 있고, 조직의 클라우드 환경 관리에 더 나은 도움을 줄 수 있습니다.
  
## <a name="before-you-begin"></a>시작하기 전에

다음 사항을 확인합니다.
  
- 조직에 [Office 365 클라우드 앱 시큐리티](office-365-cas-overview.md)를 소유하고 있으며 이 서비스를 [활성화](turn-on-office-365-cas.md)합니다.
    
- Office 365 환경에 대한 [감사 로그](turn-audit-log-search-on-or-off.md) 기능을 활성화합니다. 
    
- 전역 관리자 또는 Office 365의 보안 관리자 권한.
    
## <a name="create-a-new-activity-policy"></a>새 작업 정책 만들기

1. 전역 관리자 또는 보안 관리자 권한으로 [https://protection.office.com](https://protection.office.com)로 이동하여 조직이나 학교 계정을 이용하여 로그인합니다.
    
2. 보안 및 규정 준수센터에서, **알림** \> **고급 알림 관리**를 선택합니다.
    
3. **Office 365 클라우드 앱 시큐리티로 이동**을 선택 합니다.
    
     Office 365 클라우드 앱 보안 정책 페이지로 이동하게 됩니다.
    
    ![정책 페이지에서 Office 365 클라우드 앱 시큐리티 포털로 이동할 때](media/5cb8833c-4e08-438c-bab3-91b5106f6f3f.png)
  
4. **정책 만들기**를 클릭 하고 **작업 정책**을 선택 합니다.
    
    ![O365 CA에서 정책을 만들면 활동 정책과 이상 탐지 정책을 선택할 수 있습니다.](media/79f34535-ddf9-4a5b-a0a3-8766bf9c174c.png)
  
5. **활동 정책 만들기** 페이지에서 **정책 이름** 및 **설명**을 지정 합니다. 기본 탬플릿 파일의 정책에 기반하여 **정책 탬플릿 파일** 목록에서 하나를 선택 하거나 탬플릿 파일을 사용 하지 않고 직접 정책을 만듭니다. 
    
    ![Office 365 클라우드 앱 보안이 포함 된 활동 정책을 만들 수 있습니다.](media/4083a76f-7074-4d6a-8200-6d76d49259d7.png)
  
6. 이 정책이 보내는 경고의 중요도를 나타내는 **정책 중요도** (낮음, 보통, 또는 높음)를 선택합니다. 이렇게 하면 나중에 정책을 검토 하는 경우 필터링 하는데 도움이 될 것입니다.
    
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

- [예외 탐지 정책](anomaly-detection-policies-in-ocas.md)
    
- [SIEM 서버 통합](integrate-your-siem-server-with-office-365-cas.md)
    
- [검토 및 알림 작업을 수행 합니다.](review-office-365-cas-alerts.md)
    
- [관리를 단순화 하 여 IP 주소를 그룹화](group-your-ip-addresses-in-ocas.md)
    

