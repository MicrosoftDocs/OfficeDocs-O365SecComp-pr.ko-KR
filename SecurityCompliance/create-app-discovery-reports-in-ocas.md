---
title: Office 365 Cloud App Security을 사용하여 앱 검색 보고서 만들기
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 1/28/2019
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 3e68e691-1fc4-4d3e-a2c0-d3134eb64055
description: office 365 Cloud App Security를 사용 하 여 보고서를 만들면 조직의 사용자가 office 365 및 기타 앱을 사용 하는 방법을 이해할 수 있습니다.
ms.openlocfilehash: 23165a52a09e5bcde46ee3ab2110dc17d0faf7f4
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32259644"
---
# <a name="create-app-discovery-reports-using-office-365-cloud-app-security"></a>Office 365 Cloud App Security을 사용하여 앱 검색 보고서 만들기

|계산 * *\>**|계획 * *\>**|배포 * *\>**|사용률 * * * *|
|:-----|:-----|:-----|:-----|
|[평가 시작](office-365-cas-overview.md) <br/> |[계획 시작](get-ready-for-office-365-cas.md) <br/> |[배포 시작](turn-on-office-365-cas.md) <br/> |사용자가 여기 있어!  <br/> [다음 단계](#next-steps) <br/> |
   
Office 365 cloud App security는 전역 관리자, 보안 관리자 및 보안 독자에 게 조직에서 사용 중인 클라우드 서비스에 대 한 통찰력을 제공 합니다. 예를 들어 사용자가 문서를 저장 하 고 공동으로 작업 하는 위치와 Office 365 외부에 있는 앱 또는 서비스에 업로드 되는 데이터의 양을 볼 수 있습니다.
  
앱 검색 보고서를 생성 하려면 방화벽과 프록시에서 웹 트래픽 로그 파일을 수동으로 업로드 한 다음 Office 365 Cloud app Security에서 해당 파일을 구문 분석 하 고 분석 하 여 보고서를 작성 합니다.
  
> [!NOTE]
> 이 문서에서 설명 하는 작업을 수행 하려면 전역 관리자, 보안 관리자 또는 보안 독자 여야 합니다. 자세한 내용은 [Office 365 보안 &amp; 및 준수 센터의 사용 권한](permissions-in-the-security-and-compliance-center.md)를 참조 하세요. 
  
## <a name="create-a-report-with-app-discovery"></a>앱 검색을 사용 하 여 보고서 만들기

앱 검색 보고서를 만들려면 분석 하려는 로그 파일의 공급 업체 데이터 원본을 식별 하 고, 로그 파일을 선택한 다음, 보고서를 요청 합니다.
  
> [!NOTE]
> 최대 트래픽 기간을 포함 하는 웹 트래픽 로그 파일을 사용 하 여 조직에서 사용을 최상의 방법으로 표시 합니다. 
  
1. [Office 365 Cloud App Security에 대 한 웹 트래픽 로그 및 데이터 원본을](web-traffic-logs-and-data-sources-for-ocas.md)수집 합니다.
    
2. Cloud App Security portal ([https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com))로 이동 하 여 로그인 합니다. 
       
3. **새 보고서 만들기** **검색** \> 을 선택 합니다. <br>![Office 365 CAS 포털에서 검색을 선택 합니다.](media/73b5299f-94b5-49dd-a00f-154d188eb2c5.png)<br>
  
4. 보고서의 이름과 설명을 지정한 다음 **데이터 원본** 목록에서 웹 트래픽 로그의 데이터 원본을 선택 합니다. <br>![O365 CAS에서 새 보고서 만들기 \> 검색을 선택 합니다.](media/22e660f0-5eb2-49fa-9fea-f88a5809a07b.png)<br>사용 하려는 데이터 원본이 나열 되지 않으면 추가 되도록 요청할 수 있습니다. **데이터 원본**에 대해 **기타** 를 선택한 다음 업로드 하려는 데이터 원본의 이름을 입력 합니다. 로그를 검토 하 고이를 생성 한 데이터 원본에 대 한 지원을 추가할 것인지를 알려 드리겠습니다. 
  
5. 수집한 로그 파일의 위치로 이동 하 여 해당 파일을 선택 합니다. 보고서에 대해 선택한 데이터 원본에서 로그 파일을 생성 해야 합니다.
    
6. **만들기** 를 클릭 하 여 보고서 생성 프로세스를 시작 합니다. 
    
7. 보고서의 상태를 보려면 **스냅숏 보고서 관리**를 클릭 합니다. 보고서가 준비 되 면 **보고서 보기** 옵션이 표시 됩니다. 
    
## <a name="next-steps"></a>다음 단계

- [경고 검토 및 알림 작업 수행](review-office-365-cas-alerts.md)
    
- [Office 365 Cloud App Security을 사용하여 앱 검색 결과 검토](review-app-discovery-findings-in-ocas.md)
    
- [Office 365 Cloud App Security에 대 한 사용률 작업](utilization-activities-for-ocas.md) 검토
    

