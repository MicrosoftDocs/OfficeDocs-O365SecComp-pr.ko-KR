---
title: Office 365 Cloud App Security 적용한 후 사용률 활동
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 2/26/2018
ms.audience: ITPro
ms.topic: conceptual
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 86f414ad-81de-4703-b40a-c6615bbe9108
description: 설정 하면 Office 365 클라우드 응용 프로그램 보안 롤아웃 후 구성은 올바른 하의 정기적 검토 준비 하는 특정 작업을 수행 합니다.
ms.openlocfilehash: bc8cfad8eb9d9444066c3193ec2978e9ffd9f56a
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22533267"
---
# <a name="utilization-activities-after-rolling-out-office-365-cloud-app-security"></a>Office 365 Cloud App Security 적용한 후 사용률 활동
  
|평가 * *\>**|계획 * *\>**|배포 * *\>**|사용률 * * *|
|:-----|:-----|:-----|:-----|
|[평가 시작 합니다.](office-365-cas-overview.md) <br/> |[계획을 시작합니다](get-ready-for-office-365-cas.md) <br/> |[배포를 시작 합니다.](turn-on-office-365-cas.md) <br/> |여기는!  <br/> [다음 단계](review-office-365-cas-alerts.md) <br/> |
   
> [!NOTE]
> Office 365 클라우드 App 보안은 Office 365 Enterprise e 5에 사용할 수 있습니다. 조직의 다른 Office 365 Enterprise 등록을 사용 하는 경우 Office 365 클라우드 앱 보안 추가 기능으로 구입할 수 있습니다. (전역 관리자는 Office 365 관리 센터에서 선택 **대금 청구** \> **추가 구독**.) 자세한 내용은 참조 [Office 365 플랫폼 서비스 설명: Office 365 보안 &amp; 준수 센터](https://technet.microsoft.com/en-us/library/dn933793.aspx) [구입 또는 비즈니스를 위한 Office 365에 대 한 추가 기능을 편집](https://support.office.com/article/4e7b57d6-b93b-457d-aecd-0ea58bff07a6)하 고 있습니다. 
  
설정 및 Office 365 클라우드 응용 프로그램 보안 구성 되어 있다고을 한 후 Office 365 전역 관리자 또는 조직에 대 한 보안 관리자 권한으로 특정 사용률 작업을 수행 합니다. 

이러한 작업을 수행 하 여는 Office 365 클라우드 App 보안은 올바르게 구성, 정책에는 최신 상태로 및 조직의 Office 365에서 값을 실현를 보장할 수 수 있습니다. 지침으로이 문서를 사용 하 여 이러한 작업에 대 한 계획을 세우는 데 도움이 됩니다.
  
> [!NOTE]
> 이 문서에서 설명 하는 작업을 수행 하려면 전역 관리자 또는 보안 관리자 여야 합니다. 자세한 내용은 참조 [Office 365 보안에 대 한 사용 권한을 &amp; 준수 센터](permissions-in-the-security-and-compliance-center.md)합니다. 
    
## <a name="activities-after-the-initial-configuration-and-rollout-of-office-365-cloud-app-security"></a>초기 구성 데이터베이스 및 Office 365 클라우드 응용 프로그램 보안을 배포 후 작업

Office 365 클라우드 응용 프로그램 보안을 구성 하 고 전역 관리자 또는 보안 관리자, 롤아웃 후 해야 몇가지 사항을 고려해 야 합니다.
  
- 작업 해야하는 IT 부서 일정에 추가할 수 있습니까?
    
- Office 365 클라우드 앱 보안 시간에 따른 정책의 오른쪽 집합을 사용 하도록 구성 된 하려면 어떻게 해야 합니까?
    
- IT 관리 체인을 어떤 종류의 요약 정보를 보낼 해야 합니까?
    
다음 표에서 진행 중인 작업을 수행 하려는 및 IT 부서의 일정에 추가 하는 것이 좋습니다 정기적으로 작업을 간략하게 요약 한 합니다.
  
|**진행 중인 작업**|**정기적으로 작업**|
|:-----|:-----|
| 경고 메시지를 보내는 전자 메일 계정을 모니터링합니다  <br/>  새로운 인터넷 공격에 대 한 최신 정보에 대 한 업계 cybersecurity 뉴스 피드를 모니터링 합니다.  <br/>  보안 경고를 식별 하 고 보안 문제 및 위험을 해결 작업을 수행합니다  <br/>  각 보안 문제 및 해결 방법 중앙 로그에 요약  <br/> | Office 365 클라우드 응용 프로그램 보안 알림 별색 비정상 상태를 월별 또는 분기별로 검토를 수행 하 고 추세 분석  <br/>  Office 365 클라우드 응용 프로그램 보안 및 주소 새 cyberattacks 및 cybersecurity의 흐름에서 향상 된 기능을 포함 하 여 기존 Office 365 클라우드 응용 프로그램 보안 정책의 월별 또는 분기별로 검토를 수행 합니다.  <br/> |
   
조직의 크기와 모니터링 및 유지 관리 하는 보안 스 태 쳐에 관심을 따라를 포함 하 여 IT 관리 체인에 대 한 월별 요약을 컴파일할 수 있습니다.
  
- 다양 한 유형의 Office 365 클라우드 앱 보안 있는 것으로 식별 하는 보안 문제
    
- 보안 문제를 발견 하는 문제 발생 횟수 등의 로그를 중앙에서 요약 정보
    
- 경고 추세 및 주소가 지정 방법
    
- 최신 cybersecurity 추세
    
- Office 365 클라우드 응용 프로그램 보안 정책 변경 사항 및 최종 사용자에 대 한 영향에 대 한 권장 사항
    
## <a name="activities-after-time-has-passed-since-rolling-out-office-365-cloud-app-security"></a>Office 365 클라우드 앱 보안 롤아웃 이후 시간이 경과한 후 활동

조직의 보안 목표와 현재 기능을 반영 하는 구성으로 다시 이동 하려면 다음 단계를 수행와 시간의 처음 구성 또는 Office 365 클라우드 응용 프로그램 보안 정책을 유지 관리 이후을 통과 하는 경우 Office 365 클라우드 응용 프로그램 보안:
  
1. Office 365 클라우드 응용 프로그램 보안에 대 한 마지막 구성 변경의 날짜를 결정 합니다.
    
2. 현재 Office 365 클라우드 응용 프로그램 보안 구성을 이해 하 고 필요에 따라 해당 정책이 조정 합니다. 예, 알림 전자 메일을 통해 전송 되 고 위치를 알고 있는 확인 합니다.
    
3. Office 365 클라우드 응용 프로그램 보안을 마지막으로 구성한 이후 제품 변경 사항에 대 한 [Office 365 클라우드 응용 프로그램 보안의 새로운 기능](new-in-office-365-cas.md) 을 참조 하십시오. 
    
4. Office 365 클라우드 응용 프로그램 보안 경고 및 로그 별색 비정상 상태에 대 한 분석을 수행 하 고 추세를 분석 합니다.
    
5. 최신 보안 위협 요소를 인식 되도록 업계 cybersecurity 추세를 확인 합니다.
    
6. Office 365 클라우드 응용 프로그램 보안 정책의 현재 집합을 수 있도록 하는 변경 내용에 대 한 분석을 수행 합니다. Office 365 클라우드 응용 프로그램 보안 기능 변경 사항, 현재 비정상 상태 및 cybersecurity 추세를 통합 합니다. 새 정책 만들기 또는 기존 정책 변경 내용을 권장 합니다.
    
7. 정책 변경 내용을 구현에 대 한 계획을 확인 합니다. 통신 (인사 및 대화)가 필요에 따라 최종 사용자와 제안 된 변경 내용 같은 결과가 발생 합니다.
    
8. Office 365 클라우드 응용 프로그램 보안 정책 변경 내용을 구현 합니다.
    
9. 최종 사용자에 게 피드백 및 Office 365 클라우드 응용 프로그램 보안 경고를 모니터링 하 고 시간에 따른 정책을 조정 합니다.
    
## <a name="next-steps"></a>다음 단계

- [활동 조사](investigate-an-activity-in-office-365-cas.md)
    
- [일시 중단 또는 사용자 계정 복원](suspend-or-restore-an-account-in-ocas.md)
    
- [앱 사용 권한 관리](manage-app-permissions-in-ocas.md)
    
- [Office 365 Cloud App Security을 사용하여 앱 검색 결과 검토](review-app-discovery-findings-in-ocas.md)
    
- 지원 되는 [웹 트래픽 로그 및 데이터 원본](web-traffic-logs-and-data-sources-for-ocas.md) 목록 보기
    

