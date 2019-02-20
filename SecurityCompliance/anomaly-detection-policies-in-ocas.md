---
title: Office 365 Cloud App Security 변칙 검색 정책
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 02/15/2019
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 88935b4e-dcb1-47f1-8aca-1bf8fb069db6
description: '변칙 검색 정책 Office 365 Cloud App Security에서는 잠재적 문제를 파악 하는 데 도움이 되는 기본 제공 알고리즘을 사용 합니다. 필터를 사용 하 여 튜닝할 수 있는 변칙 검색 정책이 하나 이상 있어야 합니다. '
ms.openlocfilehash: a3c7fb16ab10b0bcfaca444093e4e1f52468f0c8
ms.sourcegitcommit: 8679937354c1d8870ecd41519a59d2d7468c23c4
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/19/2019
ms.locfileid: "30087367"
---
# <a name="anomaly-detection-policies-in-office-365-cloud-app-security"></a>Office 365 Cloud App Security 변칙 검색 정책

|계산 * *\>**|계획 * *\>**|배포 * *\>**|사용률 * * * *|
|:-----|:-----|:-----|:-----|
|[평가 시작](office-365-cas-overview.md) <br/> |[계획 시작](get-ready-for-office-365-cas.md) <br/> |사용자가 여기 있어!  <br/> [다음 단계](ocas-conditional-access-app-control.md) <br/> |[활용 시작](utilization-activities-for-ocas.md) <br/> |
   
[Microsoft Cloud app security release 116](new-in-office-365-cas-2018.md#office-365-cloud-app-security-release-116)부터는 Office 365 Cloud app security에서는 사용자 및 ueba (항목 분석) 및 ML (엔터티 동작 분석과)을 포함 하는 미리 정의 된 변칙 검색 정책 ("상자에서 벗어나")이 포함 되어 있습니다.
  
![변칙 검색 정책을 보려면 제어 \> 정책을 선택 합니다.](media/9663baa5-98bf-45e0-9458-6e572b43ec72.png)
  
이러한 변칙 검색 정책은 사용자 및 네트워크에 연결 된 컴퓨터와 장치에 대 한 다양 한 동작을 대상으로 하는 즉각적인 감지를 제공 하 여 즉각적인 결과를 제공 합니다. 또한 새 정책은 클라우드 앱 보안 검색 엔진에서 더 많은 데이터를 제공 하 여 조사 프로세스를 가속화 하 고 진행 중인 위협을 포함 하는 데 도움이 됩니다.
  
office 365 전역 관리자 또는 보안 관리자는 office 365 Cloud App security에서 사용할 수 있는 기본 정책을 검토 하 고 필요한 경우 수정할 수 있습니다.
  
 > [!IMPORTANT]
> 초기 학습 기간은 7 일 이며이 기간 동안 비정상적인 동작 경고가 트리거되지 않습니다. 변칙 검색 알고리즘은 가양성 경고 수를 줄이기 위해 최적화 됩니다. 
  
## <a name="before-you-begin"></a>시작하기 전에

다음 사항을 확인합니다.
  
- 조직에 [Office 365 Cloud App Security](office-365-cas-overview.md)가 있고 서비스를 사용 [하도록 설정](turn-on-office-365-cas.md)되어 있습니다.
    
- Office 365 환경에 대 한 [감사 로깅이](turn-audit-log-search-on-or-off.md) 설정 되어 있어야 합니다. 
    
- Office 365에 대 한 전역 관리자 또는 보안 관리자 여야 합니다.
    
## <a name="view-your-anomaly-detection-policies"></a>변칙 검색 정책 보기

1. 전역 관리자 또는 보안 관리자로 이동 하 여 Cloud App security portal ([https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com))로 이동한 후 로그인 합니다.<br>이렇게 하면 Office 365 Cloud App Security 정책 페이지로 이동 합니다.
    
2. **유형** 목록에서 **변칙 검색 정책을**선택 합니다.<br>조직의 기본 (또는 기존) 변칙 검색 정책이 표시 됩니다.<br>![Office 365 Cloud App Security 변칙 검색 정책](media/2e0ee770-787a-4d4a-bea8-389dc765d4c6.png)
  
3. 설정을 검토 하거나 편집할 정책을 선택 합니다.
    
4. **업데이트**를 선택하여 변경 내용을 저장합니다. 
    
## <a name="learn-more-about-anomaly-detection-policies"></a>변칙 검색 정책에 대해 자세히 알아보기

변칙 검색 정책은 자동으로 사용 하도록 설정 됩니다. 그러나 Office 365 Cloud App Security에는 일부 변칙 검색 알림이 발생 하지 않는 7 일 동안의 초기 학습 기간이 있습니다. 그 후에는 각 세션을 활동, 즉 사용자가 활성 상태 이면, IP 주소, 장치 등이 이러한 활동의 위험 점수와 비교 됩니다. 이러한 검색은 사용자 환경을 프로 파일링 하 고 조직의 활동에서 배운 기준에 따라 알림을 트리거하는 추론 변칙 감지 엔진의 일부분입니다. 이러한 검색은 또한 사용자와 로그인 패턴을 프로 파일링 하기 위해 설계 된 기계 학습 알고리즘을 활용 하 여 가양성을 줄입니다.
  
사용자 작업을 검사 하 여 예외를 감지 합니다. 위험 이란 서로 다른 위험 요소로 그룹화 된 30 가지 이상의 위험 표시기를 확인 하 여 위험한 IP 주소, 로그인 오류, 관리 활동, 비활성 계정, 위치, 불가능 한 여행, 장치 및 사용자 에이전트, 작업 속도 등의 여러 위기 요인에 따라 평가 됩니다.
  
정책 결과에 따라 보안 경고가 트리거됩니다. office 365 Cloud App Security에서는 office 365의 모든 사용자 세션을 살펴보고 조직의 초기 계획과 사용자의 일반 활동에서 발생 하는 상황에 따라 사용자에 게 경고를 표시 합니다.
  
다음 표에서는 기본 변칙 검색 정책, 사용자가 수행 하는 작업 및 작동 방식에 대해 설명 합니다.
  
|**변칙 검색 정책 이름**|**작업 방법**|
|:-----|:-----|
|불가능 한 여행  <br/> |사용자가 첫 번째 위치에서 두 번째 위치로 이동 하는 데 걸리는 시간 보다 짧은 기간 동안 지리적으로 서로 떨어져 있는 위치에서 두 개의 사용자 작업 (하나 또는 여러 개의 세션)을 식별 합니다. 사용자가 동일한 자격 증명을 사용 하 고 있습니다. 이 검색에서는 조직의 다른 사용자가 정기적으로 사용 하는 vpn 및 위치와 같은 불가능 한 이동 조건에 기여 하는 명백 하 게 "가양성"을 무시 하는 컴퓨터 학습 알고리즘을 활용 합니다. 이 검색에는 새 사용자의 활동 패턴을 학습 하는 7 일 동안의 초기 학습 기간이 있습니다.  <br/> |
|자주 발생 하지 않는 국가의 활동  <br/> |이전의 활동 위치를 고려 하 여 새로 및 자주 발생 하지 않는 위치를 결정 합니다. 변칙 검색 엔진은 조직의 사용자가 사용 하는 이전 위치에 대 한 정보를 저장 합니다. 사용자가 최근 또는 조직 내 사용자가 방문 하지 않은 위치에서 활동이 발생 하는 경우 경고가 트리거됩니다.  <br/> |
|익명 IP 주소의 활동  <br/> |사용자가 익명 프록시 IP 주소로 식별 된 IP 주소에서 활성 상태 인지 확인 합니다. 이러한 프록시는 장치의 IP 주소를 숨기려는 사용자가 사용 하며 악의적인 의도에 사용 될 수 있습니다. 이 검색 기능은 조직의 사용자가 널리 사용 하는 잘못 된 태그가 지정 된 IP 주소와 같은 "가양성"을 줄이는 기계 학습 알고리즘을 활용 합니다.  <br/> |
|의심 스러운 IP 주소의 활동  <br/> |사용자가 Microsoft Threat Intelligence에서 위험한 것으로 확인 된 IP 주소에서 활성 상태 인지 확인 합니다. 이러한 IP 주소는 Botnet c&amp;c와 같은 악성 작업과 관련 되어 있으며, 계정이 손상 되었음을 나타낼 수 있습니다. 이 검색 기능은 조직의 사용자가 널리 사용 하는 잘못 된 태그가 지정 된 IP 주소와 같은 "가양성"을 줄이는 기계 학습 알고리즘을 활용 합니다.  <br/> |
|비정상적인 활동 (사용자 별)  <br/> | 다음과 같은 비정상적인 활동을 수행 하는 사용자를 식별 합니다.  <br/>  --여러 파일 다운로드  <br/>  --파일 공유 작업  <br/>  --파일 삭제 활동  <br/>  --가장 작업  <br/>  --관리 활동  <br/>  이러한 정책은 위반 시도에 따라 배운 기준을 고려 하 여 단일 세션 내의 활동을 찾습니다. 이러한 검색은 사용자에 게 로그온 패턴을 프로 파일링 하 고 가양성을 줄이는 기계 학습 알고리즘을 활용 합니다. 이러한 검색은 사용자 환경을 프로 파일링 하 고 조직의 활동에서 배운 기준에 따라 알림을 트리거하는 추론 변칙 감지 엔진의 일부분입니다.  <br/> |
|여러 번 실패 한 로그인 시도  <br/> |위반 시도에 표시할 수 있는 기준에 따라 단일 세션에서 여러 로그인 시도가 실패 한 사용자를 식별 합니다.  <br/> |
   
## <a name="triage-anomaly-detection-alerts"></a>변칙 검색 알림 문제 분류

알림이 발생 하면 이러한 알림을 신속 하 게 심사 하 여 먼저 처리할 항목을 결정할 수 있습니다. 알림을 위해 컨텍스트를 사용 하면 더 큰 그림을 확인 하 고 악의적이 실제로 발생 하는지 여부를 확인할 수 있습니다. 다음 절차에 따라 알림 탐색을 시작 합니다.
  
1. 전역 관리자 또는 보안 관리자로 이동 하 여 Cloud App security portal ([https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com))로 이동한 후 로그인 합니다. 
    
2. 알림을 **** 선택 하 여 경고를 확인 합니다. 
    
3. 경고에 대 한 컨텍스트를 가져오려면 다음 단계를 수행 합니다.
    
4. **작업 로그** **조사** \> 를 선택 합니다.
    
5. 사용자 또는 IP 주소와 같은 항목을 선택 합니다. 그러면 관련 insights 서랍이 열립니다.<br>![활동 로그에서 IP 주소를 조사할 수 있습니다.](media/32a727c5-e406-4fe2-9443-c1a7fb6628fc.png)
  
6. 관련 insights 서랍에서 **유사 항목 보기** 섹션의 아이콘과 같은 사용 가능한 명령을 클릭 합니다.<br> ![선택한 활동의 48 시간 내에 수행 된 작업을 보려면 시계 아이콘을 클릭 합니다.](media/c6c96aa0-98e5-4205-8873-45f8d6fd0843.png)
  
7. 계속 해 서 해당 항목에 대 한 세부 정보를 탐색 하 여 선택한 항목에 대 한 통찰력을 얻습니다.
    
여러 번 실패 한 로그인에 대 한 경고는 실제로 의심 스 럽 고 잠재적 무작위 공격을 나타낼 수 있습니다. 그러나 이러한 경고는 응용 프로그램의 구성이 될 수도 있으므로 경고가 심각 하지 않은 긍정적이 됩니다. 의심 스러운 활동이 추가로 발생 하는 다중-로그인 경고가 표시 되는 경우에는 계정이 손상 되는 확률이 더 높습니다. 예를 들어 여러 번 실패 한 로그인 경고 다음에는 고정 IP 주소의 활동이 발생 하 고,이에 대 한 강력한 두 가지 손상 표시가 모두 있습니다. 동일한 사용자가 대량 다운로드 활동을 수행한 것을 확인할 수도 있는데,이는 종종 공격자가 데이터를 exfiltration 하는 것을 나타내는 지표입니다. Office 365 Cloud App Security에서 탐색 하 여 알림을 보고 심사 하 고 필요한 경우 조치를 취할 수 있는 것과 같습니다.
  
## <a name="next-steps"></a>다음 단계

- [Office 365 앱에 대 한 조건부 액세스 앱 컨트롤 배포](ocas-deploy-conditional-access-app-control.md)

- [관리를 간소화 하는 IP 주소 그룹화](group-your-ip-addresses-in-ocas.md)

- [siem 서버 통합](integrate-your-siem-server-with-office-365-cas.md)
    
- [경고 검토 및 알림 작업 수행](review-office-365-cas-alerts.md)
    
    

