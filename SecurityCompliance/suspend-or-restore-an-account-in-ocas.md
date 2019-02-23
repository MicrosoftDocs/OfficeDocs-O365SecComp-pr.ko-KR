---
title: Office 365 Cloud App Security에서 사용자 계정 일시 중단 또는 복원
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 12/03/2018
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 5f02d20f-b9aa-4b2f-ad2d-506a4a3c4540
description: 'Office 365 Cloud App Security를 사용 하는 경우 사용자 계정을 일시 중단 하거나 대기 취소 하는 거 버 넌 스 작업을 수행할 수 있습니다. '
ms.openlocfilehash: 3650a5304af0440dc537610994c4bd827f599989
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30215098"
---
# <a name="suspend-or-restore-a-user-account-in-office-365-cloud-app-security"></a>Office 365 Cloud App Security에서 사용자 계정 일시 중단 또는 복원

|계산 * *\>**|계획 * *\>**|배포 * *\>**|사용률 * * * *|
|:-----|:-----|:-----|:-----|
|[평가 시작](office-365-cas-overview.md) <br/> |[계획 시작](get-ready-for-office-365-cas.md) <br/> |[배포 시작](turn-on-office-365-cas.md) <br/> |사용자가 여기 있어!  <br/> [다음 단계](suspend-or-restore-an-account-in-ocas.md#nextsteps) <br/> |
   
조직의 Office 365에 대 한 사용자 계정 중 하나가 손상 되었음을 알리는 경고가 표시 되는 경우를 가정해 봅니다. 또는 사용자 계정에 문제가 있음을 나타내는 경고를 받았다고 가정해 보겠습니다. Office 365 Cloud App Security를 사용 하 여 사용자 계정을 일시 중단 하 고 나중에 수신한 알림을 조사한 후에 복원할 수 있습니다.
  
> [!NOTE]
> office 365 Cloud App Security는 office 365 Enterprise E5에서 사용할 수 있습니다. 조직에서 다른 office 365 Enterprise 구독을 사용 하는 경우 office 365 Cloud App Security를 추가 기능으로 구입할 수 있습니다. (전역 관리자 인 경우 Office 365 관리 센터에서 **청구** \> **구독 추가**를 선택 합니다.) 자세한 내용은 [office 365 플랫폼 서비스 설명: office 365 보안 &amp; 및 준수 센터](https://technet.microsoft.com/en-us/library/dn933793.aspx) 및 [비즈니스용 office 365 용 추가 기능 구입 또는 편집](https://support.office.com/article/4e7b57d6-b93b-457d-aecd-0ea58bff07a6)을 참조 하세요. 
  
## <a name="to-suspend-a-user-account-in-office-365-cloud-app-security"></a>Office 365 Cloud App Security에서 사용자 계정을 일시 중단 하려면

사용자 계정을 일시 중단 하면 사용자가 다시 로그인 할 수 없습니다. Office 365에서 직접 사용자 계정을 편집 하 여 로그인 상태를 **로그인 차단**으로 설정 하는 것과 동일 합니다.
  
> [!NOTE]
> 사용자가 Office 365에 로그인 하지 못하도록 차단 하거나 (또는 로그인 상태를 편집 하 여), 사용자의 모든 장치 및 클라이언트에 적용 되도록 ([office 365에서 사용자 편집 또는 변경](https://support.office.com/article/42BB3F17-8F9D-4182-B434-5F1C8024E614#SingleUserPreview)), 한 시간 정도 소요 될 수 있습니다. 사용자가 office 365에 로그인 되어 있으면 office 365에서 다시 로그인 해야 할 때마다 차단이 적용 됩니다. 
  
1. [전역 관리자 또는 보안 관리자로](permissions-in-the-security-and-compliance-center.md)이동 [https://protection.office.com](https://protection.office.com) 하 여 회사 또는 학교 계정을 사용 하 여 로그인 합니다. (보안 &amp; 및 준수 센터로 이동 합니다.) 
    
2. 보안 &amp; 및 준수 센터에서 **경고** \> **고급 알림 관리**를 선택 합니다.
    
3. **Office 365 Cloud App Security로 이동을**선택 합니다.<br>![보안 &amp; 및 준수 센터에서 Office 365 Cloud App Security로 이동 하려면 고급 알림 관리를 선택 합니다.](media/958632d4-03e3-4ade-8e22-d5509db6fca7.png)<br>
  
4. 화면 위쪽의 탐색 모음에서 **경고**를 선택 합니다.
    
5. **알림** 열에서 특정 사용자 계정과 관련 된 알림을 두 번 클릭 합니다. 
    
6. **계정**아래의 **상태** 열 ![에서](media/e01b75cc-b28f-4b83-8f86-b1b13dc27ab2.png) \> **사용자 일시 중단**설정 아이콘을 선택 합니다.
    
## <a name="to-restore-a-user-account"></a>사용자 계정을 복원 하려면

[Office 365에서 사용자 복원](https://support.office.com/article/2c261e42-5dd1-48b0-845f-2a016d29cfc1) 참조
  
## <a name="next-steps"></a>다음 단계

- [검토 하 고 필요한 작업을 Office 365 Cloud App Security 검토 및 알림 작업 수행](review-office-365-cas-alerts.md)
    
- [Office 365 Cloud App Security를 사용하여 OAuth 앱 관리](manage-app-permissions-in-ocas.md)
    
- [Office 365 Cloud App Security에 대 한 사용률 작업](utilization-activities-for-ocas.md) 검토
    

