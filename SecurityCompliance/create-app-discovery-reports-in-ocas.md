---
title: Office 365 Cloud App Security을 사용하여 앱 검색 보고서 만들기
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
ms.assetid: 3e68e691-1fc4-4d3e-a2c0-d3134eb64055
description: Office 365 및 다른 응용 프로그램 사용자 조직에서 사용 하는 방법을 이해할 수 있도록 하는 Office 365 클라우드 앱 보안이 포함 된 보고서를 만듭니다.
ms.openlocfilehash: 6842912f42072e21608955bde5250f0774c7bba4
ms.sourcegitcommit: 9034809b6f308bedc3b8ddcca8242586b5c30f94
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/15/2019
ms.locfileid: "28014871"
---
# <a name="create-app-discovery-reports-using-office-365-cloud-app-security"></a>Office 365 Cloud App Security을 사용하여 앱 검색 보고서 만들기

Office 365 고급 보안 관리 Office 365 클라우드 응용 프로그램 보안 되었습니다.
  
|평가 * *\>**|계획 * *\>**|배포 * *\>**|사용률 * * *|
|:-----|:-----|:-----|:-----|
|[평가 시작 합니다.](office-365-cas-overview.md) <br/> |[계획을 시작합니다](get-ready-for-office-365-cas.md) <br/> |[배포를 시작 합니다.](turn-on-office-365-cas.md) <br/> |여기는!  <br/> [다음 단계](#next-steps) <br/> |
   
Office 365 클라우드 앱 보안 전역 관리자, 보안 관리자 및 보안 독자 사용자가 조직에서 사용 하는 클라우드 서비스에 대 한 정보를 얻을 수 있습니다. 예 및 데이터의 양을 앱 또는 Office 365 외부에 있는 서비스에 업로드 되는 사용자를 저장 하 고 문서에서 공동 작업을 볼 수 있습니다.
  
앱 검색 보고서를 생성 하려면 수동으로 웹 트래픽 로그 파일에서 방화벽 및 프록시를가 업로드 하 고 Office 365 클라우드 앱 보안 구문 분석 하 고 보고서에 대 한 해당 파일을 분석 하 여 다음 합니다.
  
> [!NOTE]
> 이 문서에서 설명 하는 작업을 수행 하려면 전역 관리자, 보안 관리자 또는 보안 판독기 이어야 합니다. 자세한 내용은 참조 [Office 365 보안에 대 한 사용 권한을 &amp; 준수 센터](permissions-in-the-security-and-compliance-center.md)합니다. 
  
## <a name="create-a-report-with-app-discovery"></a>응용 프로그램 검색을 사용 하 여 보고서 만들기

응용 프로그램 검색 보고서를 만들려면를 분석 로그 파일을 선택한 다음 보고서를 요청 하려는 로그 파일에 대 한 공급 업체 데이터 소스를 식별 합니다.
  
> [!NOTE]
> 조직에서 사용 현황의 최상의 표현을 가져올 최대 트래픽을 기간을 포함 하는 웹 트래픽 로그 파일을 사용 합니다. 
  
1. 사용자 [웹 트래픽 로그 및 Office 365 클라우드 응용 프로그램 보안에 대 한 데이터 원본을](web-traffic-logs-and-data-sources-for-ocas.md)수집 합니다.
    
2. 이동 [https://protection.office.com](https://protection.office.com) 작업이 나 교육용 계정을 사용 하 여 로그인 하 고 있습니다. 
    
3. 보안에서 &amp; 준수 센터 **알림** 선택 \> **관리 고급 알림**입니다.
    
4. **Office 365 클라우드 응용 프로그램 보안으로 이동**을 선택 합니다.
    
5. **검색** 을 선택 \> **새 보고서 만들기**.
    
    ![Office 365 CAS 포털에서 검색을 선택](media/73b5299f-94b5-49dd-a00f-154d188eb2c5.png)
  
6. 이름 및 사용자 보고서에 대 한 설명을 지정 하 고 **데이터 원본** 목록에서 웹 트래픽 로그에 대 한 데이터 원본을 선택 합니다. 
    
    ![O365 CA에서 검색을 선택 \> 새 보고서 만들기](media/22e660f0-5eb2-49fa-9fea-f88a5809a07b.png)
  
    > [!NOTE]
    > 사용 하 여 원하는 데이터 원본 목록에 없는 경우 추가 될 요청할 수 있습니다. **데이터 원본**대 한 **기타** 를 선택 하 고 업로드 하려는 데이터 원본의 이름을 입력 합니다. 로그를 검토 하 고 사용 하는 것을 생성 하는 데이터 원본에 대 한 지원을 추가 하는 경우 알 수 하는 합니다. 
  
7. 수집한 로그 파일의 위치를 찾아 해당 파일을 선택 합니다. 로그 파일은 보고서에 대해 선택한 데이터 원본에 의해 생성 합니다.
    
8. 보고서 만들기 프로세스를 시작 하려면 **만들기** 클릭 합니다. 
    
9. 다음은 보고서의 상태를 보려면 **Manage 스냅숏 보고서**를 클릭 합니다. 보고서 준비 되 면 **보고서 보기** 옵션을 표시 됩니다. 
    
## <a name="next-steps"></a>다음 단계

- [검토 및 알림 작업을 수행 합니다.](review-office-365-cas-alerts.md)
    
- [Office 365 Cloud App Security을 사용하여 앱 검색 결과 검토](review-app-discovery-findings-in-ocas.md)
    
- [Office 365 클라우드 응용 프로그램 보안에 대 한 사용률 활동](utilization-activities-for-ocas.md) 을 검토 합니다.
    

