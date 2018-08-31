---
title: IP를 그룹화하여 Office 365 Cloud App Security 관리를 단순화
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 2/22/2018
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: b5e1471c-1ad6-4bc5-9e75-ce791aee283c
description: 집합의 실제 사무실 IP 주소를 사용 하 여 같은 Office 365 클라우드 응용 프로그램 보안에 사용할 IP 주소를 쉽게 식별할 수 IP 주소 범위는 그룹을 설정할 수 있습니다.
ms.openlocfilehash: 76cb9625a46d1f5eceaab696de5dcbb72f4d2b47
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22532919"
---
# <a name="group-your-ip-addresses-to-simplify-management-in-office-365-cloud-app-security"></a>IP를 그룹화하여 Office 365 Cloud App Security 관리를 단순화
  
|평가 * *\>**|계획 * *\>**|배포 * *\>**|사용률 * * *|
|:-----|:-----|:-----|:-----|
|[평가 시작 합니다.](office-365-cas-overview.md) <br/> |[계획을 시작합니다](get-ready-for-office-365-cas.md) <br/> |여기는!  <br/> [다음 단계](#next-steps) <br/> |[활용 하 여 시작](utilization-activities-for-ocas.md) <br/> |
   
집합의 실제 사무실 IP 주소를 사용 하 여 같은 Office 365 클라우드 응용 프로그램 보안에 사용할 IP 주소를 쉽게 식별할 수 IP 주소 범위는 그룹을 설정할 수 있습니다. 정의 이러한 범위 수 있음 태그를 지정 하 고, 분류 하 고 태그를 사용할 수 있습니다 및 작업 로그 및 경고 방법을 사용자 지정 하는 범주를 표시 하 고 확인 합니다.
  
IP 범위를 가진 각 그룹을 선택 하 고 다음 태그 분류할 수 있습니다 (예: 회사, 관리, Risky, 및 VPN) IP 범주의 기본 목록을 기반으로 하는 태그 이름으로 태그가 지정 된 수 있습니다. IPv4 및 IPv6 주소를 모두 지원 됩니다.
  
> [!NOTE]
> 이 문서의 절차를 수행 하려면 전역 관리자 또는 보안 관리자 여야 합니다. 자세한 내용은 참조 [Office 365 보안에 대 한 사용 권한을 &amp; 준수 센터](permissions-in-the-security-and-compliance-center.md)합니다. 
  
## <a name="to-set-up-an-ip-address-range-in-office-365-cloud-app-security"></a>Office 365 클라우드 응용 프로그램 보안의 IP 주소 범위를 설정 하려면

1. 전역 관리자 또는 보안 관리자로 이동 [https://protection.office.com](https://protection.office.com) 작업이 나 교육용 계정을 사용 하 여 로그인 하 고 있습니다. (이렇게 하면 보안 &amp; 준수 센터.) 
    
2. 보안에서 &amp; 준수 센터 **알림** 선택 \> **관리 고급 알림**입니다.
    
3. **Office 365 클라우드 응용 프로그램 보안으로 이동**을 선택 합니다.
    
    ![보안에서 &amp; 준수 센터 Office 365 클라우드 앱 보안으로 이동 하려면 고급 알림 관리를 선택 합니다.](media/958632d4-03e3-4ade-8e22-d5509db6fca7.png)
  
4. 페이지의 오른쪽 위에서 **설정** 을 클릭 \> **IP 주소 범위**입니다.
    
    ![O 365 클라우드 응용 프로그램 보안에서 시스템 및 데이터 설정에 액세스 하는 설정을 선택합니다](media/f6c48ee3-39b4-4b5a-8252-b6493b7bcd3d.png)
  
5. 더하기 기호를 비슷한 새 단추를 클릭 ( **+**).
    
6. **새 IP 주소 범위** 창에서 다음 값을 지정 합니다. 
    
|**필드 또는 목록**|**수행할 작업**|
|:-----|:-----|
|**이름** <br/> |이 필드를 사용 하 여 IP 주소 범위 및 설정을 관리할 수 있습니다. (활동 로그에이 값을 표시 되지 않습니다.)  <br/> |
|**IP 주소 범위** <br/> |네트워크 접두사 표기법 (CIDR 표기법 라고도 함)를 사용 하 여 범위를 지정 합니다. 예, 192.168.1.0/27 192.168.1.31 (포함)을 통해 192.168.1.0 값의 범위를 포함합니다.  <br/> |
|**위치** 및 **ISP에 등록** <br/> |IP 주소 범위에 대 한 위치 및 인터넷 서비스 공급자 (ISP)를 지정 합니다. 와 같이 IP 주소는 공개적으로 아일랜드 될 것으로 간주 됩니다 이지만 실제로 미국에서의 경우에 대 한 유용한은 공용 필드의 주소에 대해 정의 된 재정의  <br/> |
|**태그** <br/> |태그를 사용 하 여 IP 주소 그룹의 이름을 지정 합니다. (이름 필드와는 달리 태그의에서 나타납니다 기록을.) 단어 또는 구를 태그를 사용 하려는 입력 합니다. 각 IP 주소 범위에 대해 원하는 만큼의 태그를 추가할 수 있습니다. 및 태그를 이미 설정 했을 때이 IP 주소 범위를 추가 하려는 경우 입력을 시작 하면 표시 되는 현재 태그의 목록에서 선택 합니다.  <br/> |
|**종류** <br/> | 특정 IP 주소에서 제공 하는 활동을 인식 하도록 쉽게 수행할 수 있도록 태그에 범주를 할당 합니다. 다음 옵션 중에서 선택 합니다.<br/> **관리** 모든 사용자 admins 그룹의 IP 주소입니다.  <br/> **클라우드 공급자** 클라우드에서 프록시의 IP 주소입니다.  <br/> **회사** 모든 IP 주소를 내부 네트워크, 지사에서 및 Wi-fi 로밍 주소.  <br/> **Risky를 찾습니다.** 하면 의심 스러운 IP 주소와 같은 위험한, 수를 고려 하는 모든 IP 주소 경쟁 업체의 네트워크의 IP 주소에 이전에 본 하 고 등입니다. 기본적으로 위험한 범주에 포함 되어 두 IP 태그: **익명 프록시** 및 **에** <br/> **VPN** 원격 작업 자가 사용 하는 모든 IP 주소입니다.  <br/> |
   
7. **저장**을 선택합니다.
    
IP 주소 범위를 설정 하면 염두에 향후 이벤트는 이러한 변경 내용에 영향을 합니다.
  
## <a name="next-steps"></a>다음 단계

- [활동 정책 및 알림](activity-policies-and-alerts.md)
    
- [예외 탐지 정책](anomaly-detection-policies-in-ocas.md)
    
- [SIEM 서버 통합](integrate-your-siem-server-with-office-365-cas.md)
    
- [검토 하 고 필요한 작업을 Office 365 Cloud App Security 검토 및 알림 작업 수행](review-office-365-cas-alerts.md)
    

