---
title: Office 365 Cloud App Security에서 사용자 계정 일시 중단 또는 복원
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 12/03/2018
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 5f02d20f-b9aa-4b2f-ad2d-506a4a3c4540
description: 'Office 365 클라우드 응용 프로그램 보안을 위해 수행할 수 있는 관리 작업은 일시 중단 또는 사용자 계정을 일시 수 있습니다. '
ms.openlocfilehash: 09d6ae870aa1a6b0a619ccf20f8cc19b392e23a8
ms.sourcegitcommit: 9034809b6f308bedc3b8ddcca8242586b5c30f94
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/15/2019
ms.locfileid: "28014850"
---
# <a name="suspend-or-restore-a-user-account-in-office-365-cloud-app-security"></a>Office 365 Cloud App Security에서 사용자 계정 일시 중단 또는 복원

Office 365 고급 보안 관리 Office 365 클라우드 응용 프로그램 보안 되었습니다.
  
|평가 * *\>**|계획 * *\>**|배포 * *\>**|사용률 * * *|
|:-----|:-----|:-----|:-----|
|[평가 시작 합니다.](office-365-cas-overview.md) <br/> |[계획을 시작합니다](get-ready-for-office-365-cas.md) <br/> |[배포를 시작 합니다.](turn-on-office-365-cas.md) <br/> |여기는!  <br/> [다음 단계](suspend-or-restore-an-account-in-ocas.md#nextsteps) <br/> |
   
손상 된 Office 365에 대 한 조직의 사용자 계정 중 하나는 알림을 수신 하는 경우를 가정해 보겠습니다. 또는 사용자 계정을 사용 하 여 잘못 된 것을 알려주는 알림을 받은 경우를 가정해 보겠습니다. Office 365 클라우드 응용 프로그램 보안 사용자 계정을 일시 중단 하 고 나중에 받으면 알림을 확인 한 후 복원할 수 있습니다.
  
> [!NOTE]
> Office 365 클라우드 App 보안은 Office 365 Enterprise e 5에 사용할 수 있습니다. 조직의 다른 Office 365 Enterprise 등록을 사용 하는 경우 Office 365 클라우드 앱 보안 추가 기능으로 구입할 수 있습니다. (전역 관리자는 Office 365 관리 센터에서 선택 **대금 청구** \> **추가 구독**.) 자세한 내용은 참조 [Office 365 플랫폼 서비스 설명: Office 365 보안 &amp; 준수 센터](https://technet.microsoft.com/en-us/library/dn933793.aspx) [구입 또는 비즈니스를 위한 Office 365에 대 한 추가 기능을 편집](https://support.office.com/article/4e7b57d6-b93b-457d-aecd-0ea58bff07a6)하 고 있습니다. 
  
## <a name="to-suspend-a-user-account-in-office-365-cloud-app-security"></a>Office 365 클라우드 응용 프로그램 보안에 사용자 계정을 일시 중단

사용자 계정, 일시 중단 사용자 다시 로그인 되지 않도록 합니다. 해당 사용자 계정에 **로그인 차단 되는**로그인 상태를 설정 하려면 Office 365에서 직접 편집와 동일 합니다.
  
> [!NOTE]
> 해당 일시 중단 하 여 또는 로그인 상태를 편집 하 여 Office 365에 로그인 한 사용자를 차단 하는 경우 모든 사용자의 장치 및 클라이언트 ([편집 또는 Office 365에서 사용자를 변경](https://support.office.com/article/42BB3F17-8F9D-4182-B434-5F1C8024E614#SingleUserPreview))에 영향을 1 시간 정도 걸릴 수 있다는 유의 합니다. 사용자가 Office 365에 로그인 하는 경우 차단은 Office 365에 필요한 다시 로그인 할 때마다 적용이 됩니다. 
  
1. [전역 관리자 또는 보안 관리자](permissions-in-the-security-and-compliance-center.md)로 이동 [https://protection.office.com](https://protection.office.com) 작업이 나 교육용 계정을 사용 하 여 로그인 하 고 있습니다. (이렇게 하면 보안 &amp; 준수 센터.) 
    
2. 보안에서 &amp; 준수 센터 **알림** 선택 \> **관리 고급 알림**입니다.
    
3. **Office 365 클라우드 응용 프로그램 보안으로 이동**을 선택 합니다.<br>![보안에서 &amp; 준수 센터 Office 365 클라우드 앱 보안으로 이동 하려면 고급 알림 관리를 선택 합니다.](media/958632d4-03e3-4ade-8e22-d5509db6fca7.png)<br>
  
4. 화면 위쪽 탐색 모음에서 **경고**를 선택 합니다.
    
5. **경고** 열에는 특정 사용자 계정에 관련 경고를 두번클릭 합니다. 
    
6. **계정**아래에서 **상태** 열에서 설정을 선택 ![설정 아이콘](media/e01b75cc-b28f-4b83-8f86-b1b13dc27ab2.png) \> **일시 중단 사용자**입니다.
    
## <a name="to-restore-a-user-account"></a>사용자 계정을 복원 하려면

[Office 365에서 사용자를 복원 합니다.](https://support.office.com/article/2c261e42-5dd1-48b0-845f-2a016d29cfc1) 를 참조 하십시오.
  
## <a name="next-steps"></a>다음 단계

- [검토 하 고 필요한 작업을 Office 365 Cloud App Security 검토 및 알림 작업 수행](review-office-365-cas-alerts.md)
    
- [Office 365 Cloud App Security를 사용하여 OAuth 앱 관리](manage-app-permissions-in-ocas.md)
    
- [Office 365 클라우드 응용 프로그램 보안에 대 한 사용률 활동](utilization-activities-for-ocas.md) 을 검토 합니다.
    

