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
description: 고급 보안 관리에서 응용 프로그램 검색 보고서를 검토 하면 조직에서 사람들이 클라우드 앱을 사용 하는 방법에 대 한 자세한 내용은 할 수 있습니다. 로그 파일에서 방화벽 및 프록시를 사용 하 여 응용 프로그램 검색 보고서를 만든 후 app 검색 대시보드에서 결과 검토 합니다.
ms.openlocfilehash: ddf3826f5aac9d3c837cf66f1b97b4650df70f32
ms.sourcegitcommit: 2cf7f5bb282c971d33e00f65d9982a3f14aec74e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/27/2018
ms.locfileid: "26706262"
---
# <a name="review-app-discovery-findings-in-office-365-cloud-app-security"></a>Office 365 Cloud App Security을 사용하여 앱 검색 결과 검토
  
|평가 * *\>**|계획 * *\>**|배포 * *\>**|사용률 * * *|
|:-----|:-----|:-----|:-----|
|[평가 시작 합니다.](office-365-cas-overview.md) <br/> |[계획을 시작합니다](get-ready-for-office-365-cas.md) <br/> |[배포를 시작 합니다.](turn-on-office-365-cas.md) <br/> |여기는!  <br/> [다음 단계](#next-steps) <br/> |
   
클라우드 검색 대시보드 클라우드 앱 사용 현황에 대 한 자세한 정보를 제공 하려면 조직의 웹 트래픽 로그 작동 합니다. 전역 관리자, 보안 관리자 또는 보안 판독기 자신이 하 고 조직에 [Office 365 클라우드 응용 프로그램 보안에서 app 검색 보고서를 만든](create-app-discovery-reports-in-ocas.md), 클라우드 검색 대시보드를 사용 하에 대 한 정보를 얻을 수 하는 경우 어떻게 구성원 들이 프로그램 조직에는 Office 365 및 기타 클라우드 앱 사용 하는 합니다. (클라우드 검색 대시보드는로 알려져 생산성 응용 프로그램 검색 합니다.)
  
 **클라우드 검색 대시보드 년 3 월 2018를 기준으로 새로운 기능이 추가 되었습니다** 보다 쉽게 Office 365 및 다른 응용 프로그램 사용자 조직에서 사용 하는 방법에 대 한 자세한 정보를 볼 수 있도록 합니다. 
  
![클라우드 검색 대시보드는 업데이트 된](media/12712681-c0b3-4cb3-b7fd-2cf2ad4e825f.png)
     
## <a name="go-to-the-cloud-discovery-dashboard"></a>클라우드 검색 대시보드로 이동

1. 이동 [https://protection.office.com](https://protection.office.com) 및 Office 365에 대 한 작업이 나 교육용 계정을 사용 하 여 로그인 합니다. (이렇게 하면 보안 &amp; 준수 센터.) 
    
2. 보안에서 &amp; 준수 센터 **알림** 선택 \> **관리 고급 알림**입니다.<br/>(하는 경우 Office 365 클라우드 앱 보안 아직 활성화 되지 않으면 및 [Office 365 클라우드 응용 프로그램 보안 설정](turn-on-office-365-cas.md)전역 관리자 여야 합니다.)
    
3. **Office 365 클라우드 응용 프로그램 보안으로 이동**을 선택 합니다.
    
4. **검색** 으로 이동 \> **클라우드 검색 대시보드**합니다.
    
## <a name="see-your-top-users-ip-addresses-apps-and-risk-levels"></a>상위 사용자, IP 주소, 앱 및 위험 수준을 참조 하십시오.

클라우드 검색 대시보드 조직, open 알림, 상위 사용자 및 위험 수준에서 Office 365와 함께 사용 되는 응용 프로그램에서 한 눈 개요를 제공 합니다.
  
![클라우드 검색 dashboaard](media/06696946-fbdf-4781-b5b8-2ac074fcb2a1.png)
  
1. **대시보드** 탭에서 전체 화면의 위쪽에서 개요 섹션에 조직에서 전체 클라우드 응용 프로그램 사용에서 찾습니다. 
    
2. 조직에서 사용 되는 응용 프로그램에 대 한 **Office 365 범주** 를 참조 하십시오. 
    
3. Office 365 및이 보기에 다른 응용 프로그램의 사용을 참조 하려면 **Discovered 앱** 위젯을 살펴봅니다. 
    
4. Office 365를 사용 하 여 사서함과 클라우드 조직에 가장 앱 사용자에 게 식별 하는 **상위 사용자** 및 **위쪽 IP 주소** 위젯을 살펴봅니다. 
    
5. **앱 본사 위치** 맵을 사용 하 여 지리적 위치에 따라 사용자를 사용 하는 앱이 참조 하십시오. 
    
6. 지도 영역 위에 **위험 수준** 개요에 포함 된 검색 된 앱의 위험 점수를 살펴보겠습니다. 동일한 그룹 및 범주 **Discovered 앱** 영역에서 사용 하 여 위험 볼 수 있습니다. 예, 높음, 중간 규모 또는 낮은 위험 앱에서 각 그룹화에서 트래픽 양과 볼 수 있습니다. 
    
## <a name="dive-deeper-into-the-information"></a>정보 자세히 알아보기

앱, 하위 도메인, IP 주소 및 사용자에 대 한 상세한 정보를 적용 하려면 클라우드 검색을 사용할 수 있습니다.
  
1. 클라우드 검색 대시보드에서 **Discovered 앱** 탭을 선택 합니다. 
    
2. 필터 섹션을 사용 하 여 앱 이름, 범주, 사용 현황 수준 또는 마지막으로 발생된 한 날짜를 볼 수 있습니다.
    
3. 결과 목록에서 **하위 도메인 보기** 링크를 표시 하는 응용 프로그램 이름으로 가져갑니다.<br/> ![하위 도메인 세부 정보를 보려면 링크를 표시 하는 응용 프로그램 옆에 있는 가리키기](media/4a212215-8a2c-46fd-9ef9-89e4064658a6.png)<br/>선택한 응용 프로그램에 대 한 자세한 정보 표시 됩니다.
    
4. IP 주소에 대 한 세부 정보를 보려면 **IP 주소** 탭을 선택 합니다.<br/>![IP 주소에 대 한 자세한 정보를 표시 하는 클라우드 검색](media/0c742bf6-da9e-4d22-8656-a27a5007d5d5.png)<br/>결과 목록에서 자세한 정보를 보려면 개별 IP 주소를 선택 합니다.
    
5. 조직 내에서 Office 365 사용자에 대 한 세부 정보를 보려면 **사용자** 탭을 선택 합니다.<br/>![클라우드 검색-사용자가 정보](media/2d9c2d85-01e6-4057-8020-d9a68f26bbac.png)
  
## <a name="exclude-entities"></a>엔터티를 제외 합니다.

보다 구체적인 정보를 중점적으로 하기 위해 특정 사용자가 시스템 또는 IP 주소를 제외할 수 있습니다.
  
1. **설정** 을 선택 \> **클라우드 검색 설정**합니다.
    
2. **엔터티를 제외**를 선택 합니다.
    
3. **제외 된 사용자** 또는 **제외 된 IP 주소**중 하나를 선택 합니다.
    
4. 사용자 또는 IP 주소를 지정 하 고 **설명** 상자에 해당 사용자 또는 IP 주소를 제외한는 이유에 대 한 정보를 입력 합니다. 
    
5. **Add(추가)** 를 선택합니다.
    
## <a name="next-steps"></a>다음 단계

- [검토 및 알림 작업을 수행 합니다.](review-office-365-cas-alerts.md)
    
- [응용 프로그램 검색 보고서 만들기](create-app-discovery-reports-in-ocas.md)
    
- [Office 365 클라우드 응용 프로그램 보안에 대 한 사용률 활동](utilization-activities-for-ocas.md) 을 검토 합니다.
    

