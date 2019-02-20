---
title: Office 365 Cloud App Security을 사용하여 앱 검색 결과 검토
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
ms.assetid: aac65513-e75e-4c82-a668-9a6604dd9f9d
description: Office online의 앱 검색 보고서 검토 365 cloud app Security에서는 조직의 사용자가 클라우드 앱을 사용 하는 방법에 대해 자세히 알아볼 수 있습니다. 방화벽 및 프록시의 로그 파일을 사용 하 여 앱 검색 보고서를 만든 후에는 앱 검색 대시보드의 결과를 검토 하세요.
ms.openlocfilehash: fa5ab7c6cd734feb26878cf1a97f7ce708aa1478
ms.sourcegitcommit: 8679937354c1d8870ecd41519a59d2d7468c23c4
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/19/2019
ms.locfileid: "30087337"
---
# <a name="review-app-discovery-findings-in-office-365-cloud-app-security"></a>Office 365 Cloud App Security을 사용하여 앱 검색 결과 검토
  
|계산 * *\>**|계획 * *\>**|배포 * *\>**|사용률 * * * *|
|:-----|:-----|:-----|:-----|
|[평가 시작](office-365-cas-overview.md) <br/> |[계획 시작](get-ready-for-office-365-cas.md) <br/> |[배포 시작](turn-on-office-365-cas.md) <br/> |사용자가 여기 있어!  <br/> [다음 단계](#next-steps) <br/> |
   
클라우드 검색 대시보드는 조직의 웹 트래픽 로그와 함께 작동 하 여 클라우드 앱 사용에 대 한 자세한 정보를 제공 합니다. 전역 관리자, 보안 관리자 또는 보안 판독기이 고 조직에서 [Office 365 Cloud app security의 앱 검색 보고서를 만든](create-app-discovery-reports-in-ocas.md)경우 클라우드 검색 대시보드를 사용 하 여 사용자가 조직에서 Office 365 및 기타 클라우드 앱을 사용 하 고 있습니다. 클라우드 검색 대시보드는 생산성 앱 검색으로도 알려져 있습니다.
  
 클라우드 검색 대시보드를 사용 하 여 조직의 사용자가 Office 365 및 기타 앱을 사용 하는 방법에 대 한 자세한 정보를 볼 수 있습니다. 
  
![클라우드 검색 대시보드가 업데이트 되었습니다.](media/12712681-c0b3-4cb3-b7fd-2cf2ad4e825f.png)
     
## <a name="go-to-the-cloud-discovery-dashboard"></a>클라우드 검색 대시보드로 이동

1. Cloud App Security portal ([https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com))로 이동 하 여 로그인 합니다.
    
2. **클라우드 검색 대시보드** **검색** \> 으로 이동 합니다.
    
## <a name="see-your-top-users-ip-addresses-apps-and-risk-levels"></a>상위 사용자, IP 주소, 앱 및 위험 수준 보기

클라우드 검색 대시보드를 통해 조직의 Office 365, 열린 경고, 상위 사용자 및 위험 수준에 사용 되는 앱을 한눈에 파악할 수 있습니다.
  
![클라우드 검색 이점](media/06696946-fbdf-4781-b5b8-2ac074fcb2a1.png)
  
1. **대시보드** 탭의 화면 위쪽에 있는 개요 섹션에서 조직에 사용 되는 전체 클라우드 앱을 확인 합니다. 
    
2. 조직에서 사용 되는 앱에 대해서는 **Office 365 범주** 를 참조 하세요. 
    
3. 이 보기에서 Office 365 및 기타 앱을 사용 하는 방법을 확인 하려면 **검색 된 앱** 위젯을 확인 하세요. 
    
4. **상위 사용자** 및 **상위 IP 주소** 위젯을 사용 하 여 조직에서 Office 365 및 클라우드 앱을 가장 많이 사용해 서 확인 합니다. 
    
5. **앱 본사 위치** 맵을 사용 하 여 사용자가 사용 중인 앱이 지리적 위치를 볼 수 있습니다. 
    
6. 지도 영역 위에 표시 되는 **위험 수준** 개요에서 검색 된 앱의 위험 점수를 확인 합니다. **검색 된 앱** 영역에서 사용한 것과 동일한 그룹 및 범주를 사용 하 여 위험을 확인할 수 있습니다. 예를 들어, 상위, 중간 또는 낮은 위험 앱을 기준으로 각 그룹화의 트래픽 양을 확인할 수 있습니다. 
    
## <a name="dive-deeper-into-the-information"></a>정보에 대해 자세히 알아보기

클라우드 검색을 사용 하 여 앱, 하위 도메인, IP 주소 및 사용자에 대 한 자세한 내용을 확인할 수 있습니다.
  
1. 클라우드 검색 대시보드에서 **검색 된 앱** 탭을 선택 합니다. 
    
2. 필터 섹션을 사용 하 여 이름, 범주, 사용 현황 수준 또는 마지막으로 본 날짜를 기준으로 앱을 볼 수 있습니다.
    
3. 결과 목록에서 응용 프로그램 이름을 가리켜 **하위 도메인 보기** 링크를 표시 합니다.<br/> ![하위 도메인 세부 정보를 볼 수 있는 링크를 나타내기 위해 앱 옆에 가리키기](media/4a212215-8a2c-46fd-9ef9-89e4064658a6.png)<br/>선택한 앱에 대 한 자세한 정보가 표시 됩니다.
    
4. ip 주소에 대 한 세부 정보를 보려면 **ip 주소** 탭을 선택 합니다.<br/>![클라우드 검색에서 IP 주소에 대 한 자세한 정보를 표시 합니다.](media/0c742bf6-da9e-4d22-8656-a27a5007d5d5.png)<br/>결과 목록에서 개별 IP 주소를 선택 하 여 더 자세한 정보를 확인 합니다.
    
5. 조직 내 Office 365 사용자에 대 한 세부 정보를 보려면 **사용자** 탭을 선택 합니다.<br/>![클라우드 검색-사용자 정보](media/2d9c2d85-01e6-4057-8020-d9a68f26bbac.png)
  
## <a name="exclude-entities"></a>엔터티 제외

특정 시스템 사용자 또는 IP 주소를 제외 하 여 보다 구체적인 정보를 중점적으로 확인할 수 있습니다.
  
1. **설정** \> **클라우드 검색 설정을**선택 합니다.
    
2. **엔터티 제외**를 선택 합니다.
    
3. 제외 된 **사용자** 또는 **제외 된 IP 주소**를 선택 합니다.
    
4. 사용자 또는 ip 주소를 지정 하 고 **설명** 상자에 해당 사용자 또는 ip 주소를 제외 하는 이유에 대 한 정보를 입력 합니다. 
    
5. **Add(추가)** 를 선택합니다.
    
## <a name="next-steps"></a>다음 단계

- [경고 검토 및 알림 작업 수행](review-office-365-cas-alerts.md)
    
- [앱 검색 보고서 만들기](create-app-discovery-reports-in-ocas.md)
    
- [Office 365 Cloud App Security에 대 한 사용률 작업](utilization-activities-for-ocas.md) 검토
    

