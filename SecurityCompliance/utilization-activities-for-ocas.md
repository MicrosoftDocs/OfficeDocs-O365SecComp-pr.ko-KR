---
title: Office 365 Cloud App Security 적용한 후 사용률 활동
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 01/28/2019
ms.audience: ITPro
ms.topic: conceptual
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 86f414ad-81de-4703-b40a-c6615bbe9108
description: Office 365 Cloud App Security을 설정 하 고 롤아웃 한 후에는 특정 작업을 수행 하 여 구성이 올바르고 일반적인 검토를 위해 준비 되었는지 확인 해야 합니다.
ms.openlocfilehash: 232de4df1d1eb4debdddcee2c1d8672d1aeb4b21
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32242546"
---
# <a name="utilization-activities-after-rolling-out-office-365-cloud-app-security"></a>Office 365 Cloud App Security 적용한 후 사용률 활동
  
|계산 * *\>**|계획 * *\>**|배포 * *\>**|사용률 * * * *|
|:-----|:-----|:-----|:-----|
|[평가 시작](office-365-cas-overview.md) <br/> |[계획 시작](get-ready-for-office-365-cas.md) <br/> |[배포 시작](turn-on-office-365-cas.md) <br/> |사용자가 여기 있어!  <br/> [다음 단계](review-office-365-cas-alerts.md) <br/> |
   
> [!NOTE]
> office 365 Cloud App Security는 office 365 Enterprise E5에서 사용할 수 있습니다. 조직에서 다른 office 365 Enterprise 구독을 사용 하는 경우 office 365 Cloud App Security를 추가 기능으로 구입할 수 있습니다. (전역 관리자 인 경우 Microsoft 365 관리 센터에서 **청구** \> **구독 추가**를 선택 합니다.) 자세한 내용은 [office 365 플랫폼 서비스 설명: office 365 보안 &amp; 및 준수 센터](https://docs.microsoft.com/office365/servicedescriptions/office-365-platform-service-description/office-365-securitycompliance-center) 및 [비즈니스용 office 365 용 추가 기능 구입 또는 편집](https://support.office.com/article/4e7b57d6-b93b-457d-aecd-0ea58bff07a6)을 참조 하세요. 
  
office 365 Cloud App Security를 설정 하 고 구성한 후에는 특정 사용률 작업을 조직의 Office 365 전역 관리자 또는 보안 관리자로 수행 하는 것이 좋습니다. 

이러한 작업을 수행 하 여 office 365 Cloud App Security가 올바르게 구성 되어 있고, 정책이 최신 상태 이며, 조직에서 office 365의 가치를 인식 하도록 하는 데 도움이 됩니다. 이 문서를 참조 하 여 이러한 작업을 계획 하는 데 도움을 받을 수 있습니다.
  
> [!NOTE]
> 이 문서에서 설명 하는 작업을 수행 하려면 전역 관리자 또는 보안 관리자 여야 합니다. 자세한 내용은 [Office 365 보안 &amp; 및 준수 센터의 사용 권한](permissions-in-the-security-and-compliance-center.md)를 참조 하세요. 
    
## <a name="activities-after-the-initial-configuration-and-rollout-of-office-365-cloud-app-security"></a>Office 365 Cloud App Security의 초기 구성 및 롤아웃 후의 작업

Office 365 Cloud App security는 전역 관리자 또는 보안 관리자로 구성 및 롤아웃 된 후 다음과 같은 몇 가지 사항을 고려해 야 합니다.
  
- IT 부서 일정에 추가 해야 하는 작업
    
- Office 365 Cloud App Security가 시간에 따라 올바른 정책 집합을 사용 하도록 구성 되었는지 확인 하려면 어떻게 해야 하나요?
    
- IT 관리 체인을 전송 해야 하는 요약 정보 종류는 무엇입니까?
    
다음 표에서는 수행 하려는 진행 중인 작업 및 IT 부서의 일정에 추가 하는 데 필요한 정기적인 작업을 간략하게 요약 하 여 설명 합니다.
  
|**진행 중인 작업**|**정기 작업**|
|:-----|:-----|
| 알림 메시지를 보낼 전자 메일 계정 모니터링  <br/>  새 사이버 공격에 대 한 최신 정보에 대 한 업계 cybersecurity 뉴스 피드 모니터링  <br/>  보안 사고 및 위험을 식별 하 고 해결 하기 위한 보안 경고 동작  <br/>  중앙 로그의 각 보안 인시던트 및 해결 방법 요약  <br/> | Office 365 Cloud App 보안 경고의 월간 또는 분기별 검토를 수행 하 여 예외를 발견 하 고 추세를 분석 합니다.  <br/>  office 365 cloud app security의 향상 된 기능을 포함 하기 위해 기존 Office 365 cloud app security 정책을 매월 또는 분기별로 검토를 수행 하 고 cybersecurity의 새 고 사이버 공격 및 추세를 해결 합니다.  <br/> |
   
조직의 규모 및 모니터링 및 유지 관리에 대 한 관심 사항에 따라 다음을 포함 하는 IT 관리 체인에 대 한 월별 요약을 컴파일할 수 있습니다.
  
- Office 365 Cloud App security로 식별 되는 다양 한 보안 인시던트 유형
    
- 검색 된 인시던트 수와 같은 보안 사고의 중앙 로그의 요약 정보
    
- 알림 경향 및 처리 방법
    
- 최신 cybersecurity 추세
    
- Office 365 Cloud App Security policy 변경 및 최종 사용자에 게 미치는 영향에 대 한 권장 사항
    
## <a name="activities-after-time-has-passed-since-rolling-out-office-365-cloud-app-security"></a>Office 365 Cloud App Security 이후 시간이 지난 후 활동

처음에 Office 365 Cloud App Security 정책을 구성 하거나 유지 관리 한 후에 protracted 시간이 경과 된 경우 다음 단계를 수행 하 여 조직의 보안 목표 및 현재 기능을 반영 하는 구성으로 다시 이동 합니다. Office 365 Cloud App Security의 경우:
  
1. Office 365 Cloud App Security에 대 한 마지막 구성 변경 날짜를 확인 합니다.
    
2. 현재 Office 365 Cloud App Security configuration을 이해 하 고 필요에 따라 해당 정책을 조정 합니다. 예를 들어 전자 메일을 통해 알림을 보내는 위치를 알고 있어야 합니다.
    
3. office 365 cloud app security를 마지막으로 구성한 이후의 제품 변경 사항에 대해서는 [office 365 cloud app security의 새로운 기능](new-in-office-365-cas.md) 을 참조 하세요. 
    
4. Office 365 Cloud App 보안 경고 및 로그 분석을 수행 하 여 예외를 강조 하 고 추세를 분석 합니다.
    
5. 업계 cybersecurity 경향을 확인 하 여 최신 보안 위협을 파악 합니다.
    
6. 현재 Office 365 Cloud App Security 정책 집합에 적용 해야 하는 변경 사항에 대 한 분석을 수행 합니다. Office 365 Cloud App Security 기능 변경 사항, 현재 상황 및 cybersecurity 추세를 통합 합니다. 기존 정책 변경 또는 새 정책 만들기 권장
    
7. 정책 변경 사항 구현 계획을 수립 합니다. 의견 교환 (socialize) 필요에 따라 최종 사용자에 게 제안 된 변경의 결과를 포함 합니다.
    
8. Office 365 Cloud App 보안 정책 변경 사항을 구현 합니다.
    
9. 최종 사용자 의견 및 Office 365 Cloud App Security alerts를 모니터링 하 고 시간에 따라 정책을 조정 합니다.
    
## <a name="next-steps"></a>다음 단계

- [활동 조사](investigate-an-activity-in-office-365-cas.md)
    
- [사용자 계정 일시 중단 또는 복원](suspend-or-restore-an-account-in-ocas.md)
    
- [OAuth 앱 관리](manage-app-permissions-in-ocas.md)
    
- [Office 365 Cloud App Security을 사용하여 앱 검색 결과 검토](review-app-discovery-findings-in-ocas.md)
    
- 지원 되는 [웹 트래픽 로그 및 데이터 원본](web-traffic-logs-and-data-sources-for-ocas.md) 목록 보기
    

