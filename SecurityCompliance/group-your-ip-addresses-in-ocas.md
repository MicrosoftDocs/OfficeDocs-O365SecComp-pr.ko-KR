---
title: IP를 그룹화하여 Office 365 Cloud App Security 관리를 단순화
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
ms.assetid: b5e1471c-1ad6-4bc5-9e75-ce791aee283c
description: 실제 office IP 주소와 같은 Office 365 Cloud App Security에서 사용 하는 ip 주소 집합을 쉽게 식별 하려면 IP 주소 범위의 그룹을 설정할 수 있습니다.
ms.openlocfilehash: b8f5c1dd46b2e3990d53a65881d12ca8f3961b16
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30220448"
---
# <a name="group-your-ip-addresses-to-simplify-management-in-office-365-cloud-app-security"></a>IP를 그룹화하여 Office 365 Cloud App Security 관리를 단순화
  
|계산 * *\>**|계획 * *\>**|배포 * *\>**|사용률 * * * *|
|:-----|:-----|:-----|:-----|
|[평가 시작](office-365-cas-overview.md) <br/> |[계획 시작](get-ready-for-office-365-cas.md) <br/> |사용자가 여기 있어!  <br/> [다음 단계](#next-steps) <br/> |[활용 시작](utilization-activities-for-ocas.md) <br/> |
   
실제 office IP 주소와 같은 Office 365 Cloud App Security에서 사용 하는 ip 주소 집합을 쉽게 식별 하려면 IP 주소 범위의 그룹을 설정할 수 있습니다. 이러한 범위를 정의 하면 태그를 지정 하 고 분류할 수 있으며 태그 및 범주를 사용 하 여 활동 로그 및 경고를 표시 하 고 조사 하는 방법을 사용자 지정할 수 있습니다.
  
각 ip 범위 그룹은 선택한 태그 이름으로 태그가 지정 될 수 있으며,이 태그는 기본 IP 범주 목록 (예: 회사, 관리, 위험 및 VPN)을 기반으로 분류할 수 있습니다. IPv4 및 IPv6 주소가 모두 지원 됩니다.
  
> [!NOTE]
> 이 문서의 절차를 수행 하려면 전역 관리자 또는 보안 관리자 여야 합니다. 자세한 내용은 [Office 365 보안 &amp; 및 준수 센터의 사용 권한](permissions-in-the-security-and-compliance-center.md)를 참조 하세요. 
  
## <a name="to-set-up-an-ip-address-range-in-office-365-cloud-app-security"></a>Office 365 Cloud App Security에서 IP 주소 범위를 설정 하려면

1. 전역 관리자 또는 보안 관리자로 이동 하 여 Cloud App security portal ([https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com))로 이동한 후 로그인 합니다.
    
2. 페이지 오른쪽 위에서 **설정** \> **IP 주소 범위**를 클릭 합니다.<br>![O365 Cloud App Security에서 시스템 및 데이터 설정에 액세스 하기 위한 설정을 선택 합니다.](media/f6c48ee3-39b4-4b5a-8252-b6493b7bcd3d.png)<br>
  
3. 더하기 기호 ( **+**)와 같은 새로 만들기 단추를 클릭 합니다.
    
4. **새 IP 주소 범위** 창에서 다음 값을 지정 합니다. 
    
|**필드 또는 목록**|**수행할 작업**|
|:-----|:-----|
|**이름** <br/> |이 필드를 사용 하 여 IP 주소 범위 및 설정을 관리 합니다. (이 값은 활동 로그에 표시 되지 않습니다.)  <br/> |
|**IP 주소 범위** <br/> |네트워크 접두사 표기법 (CIDR 표기법이 라고도 함)을 사용 하 여 범위를 지정 합니다. 예를 들어 192.168.1.0/27에는 192.168.1.31 (포함) 사이의 값 192.168.1.0이 포함 되어 있습니다.  <br/> |
|**위치** 및 **등록 된 ISP** <br/> |IP 주소 범위에 대 한 위치 및 ISP (인터넷 서비스 공급자)를 지정 합니다. 이는 주소에 대해 정의 된 공용 필드를 재정의 하며, IP 주소는 일반적으로 아일랜드에 있는 것으로 간주 되지만 실제로는 미국에 있는 경우에 유용 합니다.  <br/> |
|**태그** <br/> |태그를 사용 하 여 IP 주소 그룹의 이름을 합니다. 이름 필드와 달리 작업 로그에 태그가 표시 됩니다. 태그에 사용할 단어나 구를 입력 합니다. 각 IP 주소 범위에 대해 원하는 만큼 태그를 추가할 수 있습니다. 이미 태그를 설정 했으며이 IP 주소 범위를 추가 하려면 입력을 시작할 때 표시 되는 현재 태그 목록에서이를 선택 합니다.  <br/> |
|**범주** <br/> | 특정 IP 주소에서 제공 되는 활동을 보다 쉽게 인식할 수 있도록 태그에 범주를 할당 합니다. 다음 옵션 중에서 선택 합니다.<br/> **관리** 관리자의 모든 IP 주소입니다.  <br/> **클라우드 공급자** 클라우드의 프록시 IP 주소입니다.  <br/> **회사** 내부 네트워크의 모든 IP 주소, 지점 사무소 및 wi-fi 로밍 주소  <br/> **위험** 이전에 보았던 의심 스러운 ip 주소, 경쟁사의 네트워크에 있는 ip 주소 등 위험할 수 있다고 생각 되는 모든 ip 주소입니다. 기본적으로 위험한 범주에는 두 개의 IP 태그 ( **익명 프록시** 및 **** 받는 사람)가 포함 됩니다. <br/> **VPN** 원격 작업자 들이 사용 하는 모든 IP 주소  <br/> |
   
7. **Save(저장)** 를 선택합니다.
    
IP 주소 범위를 설정한 후에는 이러한 변경으로 인해 앞으로 발생 하는 이벤트만 영향을 받습니다.
  
## <a name="next-steps"></a>다음 단계

- [활동 정책 및 알림](activity-policies-and-alerts.md)
    
- [변칙 검색 정책](anomaly-detection-policies-in-ocas.md)
    
- [siem 서버 통합](integrate-your-siem-server-with-office-365-cas.md)
    
- [검토 하 고 필요한 작업을 Office 365 Cloud App Security 검토 및 알림 작업 수행](review-office-365-cas-alerts.md)
    

