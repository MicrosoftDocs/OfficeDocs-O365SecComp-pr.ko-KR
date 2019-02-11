---
title: 검토 하 고 필요한 작업을 Office 365 Cloud App Security 검토 및 알림 작업 수행
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 97e9c3d9-df89-458e-924b-369becee5532
description: Office 365 클라우드 응용 프로그램 보안에서 경고 페이지를 사용 하 여를 잠재적 문제를 보고 하 여 작업도 하지 않습니다. 해제 하 고 또는 경고를 확인 하 고, 필요한 경우에 사용자 계정이 일시 중단 수 있습니다.
ms.openlocfilehash: ff20b913553414d796f9653108ac9b8a3d84cb74
ms.sourcegitcommit: 7e2a0185cadea7f3a6afc5ddc445eac2e1ce22eb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/11/2019
ms.locfileid: "29603679"
---
# <a name="review-and-take-action-on-alerts-in-office-365-cloud-app-security"></a>검토 하 고 필요한 작업을 Office 365 Cloud App Security 검토 및 알림 작업 수행
  
|평가 * *\>**|계획 * *\>**|배포 * *\>**|사용률 * * *|
|:-----|:-----|:-----|:-----|
|[평가 시작 합니다.](office-365-cas-overview.md) <br/> |[계획을 시작합니다](get-ready-for-office-365-cas.md) <br/> |[배포를 시작 합니다.](turn-on-office-365-cas.md) <br/> |여기는!  <br/> [다음 단계](#next-steps) <br/> |
   
잠재적인 문제를 확인 하 고 필요한 경우 작업을 수행 하려면 Office 365 클라우드 앱 보안에서 경고 페이지를 사용할 수 있습니다.
  
> [!NOTE]
> 이 문서에서 작업을 수행 하는 전역 관리자 또는 보안 관리자 여야 합니다. 참조 [Office 365 보안에 대 한 사용 권한을 &amp; 준수 센터](permissions-in-the-security-and-compliance-center.md)합니다. 
  
## <a name="how-to-get-to-the-alerts-page"></a>알림 페이지로 이동 하는 방법

1. 클라우드 응용 프로그램 보안 포털에 이동 ([https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com))에 로그인 하 고 있습니다.
  
2. 화면 위쪽 탐색 모음에서 **경고**를 선택 합니다.<br/>![경고 페이지에서 경고를 트리거한 된 및 수행 하는 모든 작업을 볼 수 있습니다.](media/3b53d4c9-4b13-435d-8547-8c0f9ae6b914.png)
  
## <a name="review-and-handle-alerts"></a>검토 및 핸들 알림

알림 추가로 조사를 수행 해야할 수 있는 Office 365 클라우드 환경에서 작업을 파악 하는데 도움이 됩니다. 새 정책 만들기 또는 표시 경고에 따라 기존 정책을 편집 하려면 결정할 수 있습니다. 예, 이상한 위치에서 로그온 하는 관리자의 이름을 표시 하는 경우에 관리자가 특정 위치에서 Office 365에 로그인 하지 못하게 하는 정책을 설정 할 수 있습니다.
  
> [!TIP]
> 먼저 가장 중요 한 항목을 관리할 수 있도록 **범주별** 로 또는 **심각도** 경고를 필터링 할 수 있습니다. 
  
각 경고에 대해 수행할 동작을 결정할 수 있도록 어떤 인해으로 찾습니다. 경고에 대 한 자세한 내용을 보려면 및 경고를 해결 하거나 일시 중단 하는 사용자 계정 등의 작업을 수행할 세부 정보 페이지를 열려면 경고를 선택 합니다. 세부 정보 페이지에서 활동 로그, 계정 및 경고와 관련 된 사용자를 검토 하 고 다음과 같은 작업을 수행할 수 있습니다.
  
- **해제** 경고 가양성 했으므로,이 해제 합니다. 필요에 따라 해제할 이유를 설명 하는 메모를 추가할 수 있습니다. 
    
- **경고를 해결 합니다.** 알고 있는 활동에 대 한 위협 요소 되지 않습니다 하 여 경고가 발생 하는 경우,이 해결 합니다. 필요에 따라 해결 한 이유를 설명 하는 메모를 추가할 수 있습니다. 
    
- **일시 중단** 허가 되지 않은 기호 기능 등 해당 사용자를 알고 있는 경우 다른 국가에서 로그인 사용자 계정에는 로컬 사무실에서 물리적으로, 의심 되 [는 계정을 일시 중단](suspend-or-restore-an-account-in-ocas.md) 상황을 조사 하는 동안 할 수 있습니다. 
    
## <a name="next-steps"></a>다음 단계

- [활동 조사](investigate-an-activity-in-office-365-cas.md)
    
- [일시 중단 또는 사용자 계정 복원](suspend-or-restore-an-account-in-ocas.md)
    
- 지원 되는 [웹 트래픽 로그 및 데이터 원본](web-traffic-logs-and-data-sources-for-ocas.md) 목록 보기
    
- [Office 365 클라우드 응용 프로그램 보안에 대 한 사용률 활동](utilization-activities-for-ocas.md) 을 검토 합니다.
    

