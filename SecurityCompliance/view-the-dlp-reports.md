---
title: 데이터 손실 방지에 대한 보고서 보기
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 6/7/2018
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
ms.collection:
- M365-security-compliance
localization_priority: Normal
search.appverid:
- MOE150
- MET150
description: Office 365의 dlp 보고서를 사용 하 여 dlp 정책 일치, 재정의 또는 가양성의 수를 빠르게 확인할 수 있습니다. 시간이 경과 함에 따라 작업 시간을 초과 하 고 있는지 여부를 확인할 수 있습니다. 다양 한 방법으로 보고서를 필터링 합니다. 그래프의 선에서 점을 선택 하 여 추가 세부 정보를 확인 합니다.
ms.openlocfilehash: 447245f945bd777f56cca71320a72a9d9dd8720e
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32267305"
---
# <a name="view-the-reports-for-data-loss-prevention"></a>데이터 손실 방지에 대한 보고서 보기

DLP (데이터 손실 방지) 정책을 만든 후에는 해당 정책이 의도 한 대로 작동 하 고 준수 상태를 유지 하는 데 도움을 주려는 것을 확인할 수 있습니다. Office 365 보안 &amp; 및 준수 센터의 DLP 보고서를 사용 하 여 다음을 빠르게 확인할 수 있습니다.
  
- **DLP 정책 일치 항목** 이 보고서는 시간에 따른 DLP 정책 일치 항목의 수를 표시 합니다. 날짜, 위치, 정책 또는 작업을 기준으로 보고서를 필터링 할 수 있습니다. 이 보고서를 사용 하 여 다음을 수행할 수 있습니다. 
    
  - 테스트 모드에서 실행 하면서 DLP 정책을 조정 하거나 구체화 합니다. 콘텐츠와 일치 하는 특정 규칙을 볼 수 있습니다.
    
  - 특정 기간에 초점을 맞추고 스파이크 및 추세의 이유를 이해합니다.
    
  - 조직의 DLP 정책을 위반 하는 비즈니스 프로세스를 검색 합니다.
    
  - 콘텐츠에 적용 되는 작업을 확인 하 여 DLP 정책의 모든 업무상 영향을 이해 합니다.
    
  - 해당 정책에 대한 일치 항목을 표시하여 특정 DLP 정책에 대한 준수를 확인합니다.
    
  - 상위 사용자 목록을 확인 하 고 조직의 사건에 기여 하는 사용자를 반복 합니다.
    
  - 조직에서 가장 중요 한 정보 유형 목록을 확인 합니다.
    
- **DLP 인시던트** 이 보고서에는 정책 일치 보고서와 같은 시간에 따른 정책 일치도 표시 됩니다. 그러나 정책이 규칙 수준에서 일치 하는 항목을 표시 하는 것은 아닙니다. 예를 들어 전자 메일이 세 가지 다른 규칙과 일치 하는 경우 정책 일치 보고서에는 세 가지 다른 줄 항목이 표시 됩니다. 반면 문제 보고서에는 항목 수준에서 일치 하는 항목이 표시 됩니다. 예를 들어 전자 메일이 세 가지 다른 규칙과 일치 하는 경우 문제 보고서에는 해당 콘텐츠에 대 한 단일 행 항목이 표시 됩니다. 
    
  보고서 개수가 서로 다르게 집계 되므로 정책 일치 보고서는 특정 규칙과 일치 하는 항목을 식별 하 고 DLP 정책을 세부적으로 조정 하는 데 도움이 됩니다. 문제 보고서는 DLP 정책에 문제가 있는 특정 콘텐츠를 식별 하는 데 도움이 됩니다.
    
- **DLP 가양성 및 재정의** DLP 정책을 사용 하 여 사용자가이를 재정의 하거나 가양성을 보고할 수 있는 경우이 보고서에는 시간에 따른 이러한 인스턴스의 개수가 표시 됩니다. 날짜, 위치 또는 정책을 기준으로 보고서를 필터링 할 수 있습니다. 이 보고서를 사용 하 여 다음을 수행할 수 있습니다. 
    
  - 가양성을 많이 발생 하는 정책을 확인 하 여 DLP 정책을 조정 하거나 구체화 합니다.
    
  - 사용자가 정책을 재정의 하 여 정책 팁을 확인할 때 제출한 근거를 봅니다.
    
  - 많은 수의 사용자 재정의를 발생 시켜 서 DLP 정책이 유효한 비즈니스 프로세스와 충돌 하는 위치를 파악 합니다.
    
모든 DLP 보고서는 최근 4 개월 동안의 데이터를 표시할 수 있습니다. 가장 최근 데이터가 보고서에 표시 되는 데 최대 24 시간이 걸릴 수 있습니다.
  
보안 &amp; 및 준수 센터 \> **보고서** \> **대시보드에서**이러한 보고서를 찾을 수 있습니다.
  
![DLP 정책 일치 보고서](media/117d20c9-d379-403f-ad68-1f5cd6c4e5cf.png)
  
## <a name="view-the-justification-submitted-by-a-user-for-an-override"></a>재정의를 위해 사용자가 전송한 사유 보기

사용자가 DLP 정책에서이를 재정의할 수 있도록 허용 하는 경우 false 긍정 및 override 보고서를 사용 하 여 정책 설명에서 사용자가 전송한 텍스트를 볼 수 있습니다.
  
![DLP 거짓 긍정 및 재정의 보고서의 세부 정보에 있는 사유 필드](media/e11e3126-026d-4e77-a16d-74a0686d1fa3.png)
  
## <a name="take-action-on-insights-and-recommendations"></a>정보 제공 및 권장 사항에 대 한 조치 수행

보고서는 위험 경고 아이콘을 클릭 하 여 잠재적 문제에 대 한 세부 정보를 확인 하 고 해결 가능한 조치를 취할 수 있는 정보를 표시 합니다.
  
![수행할 세부 정보 및 작업을 확인 하는 insights 아이콘 클릭](media/51782036-7299-4960-8175-75c2b1637159.png)
  
## <a name="permissions-for-dlp-reports"></a>DLP 보고서에 대 한 사용 권한

Security & 준수 센터에서 DLP 보고서를 보려면 다음을 할당 해야 합니다.

- Exchange 관리 센터의 **보안 독자** 역할입니다. 기본적으로이 역할은 Exchange 관리 센터의 조직 관리 및 보안 독자 역할 그룹에 할당 됩니다.

- 보안 & 준수 센터의 **보기 전용 DLP 준수 관리** 역할입니다. 기본적으로이 역할은 보안 & 준수 센터의 준수 관리자, 조직 관리, 보안 관리자 및 보안 독자 역할 그룹에 할당 됩니다.

- Exchange 관리 센터에서 **보기 전용 받는 사람** 역할입니다. 기본적으로이 역할은 Exchange 관리 센터의 준수 관리, 조직 관리 및 보기 전용 조직 관리 역할 그룹에 할당 됩니다.

## <a name="find-the-cmdlets-for-the-dlp-reports"></a>DLP 보고서용 cmdlet 찾기

보안 &amp; 및 준수 센터에 대 한 cmdlet을 대부분 사용 하려면 다음 작업을 수행 해야 합니다.
  
1. [원격 PowerShell을 사용하여 Office 365 보안 및 준수 센터에 연결](http://go.microsoft.com/fwlink/?LinkID=799771&amp;clcid=0x409)
    
2. 다음 [Office 365 보안 &amp; 및 준수 센터 cmdlet](http://go.microsoft.com/fwlink/?LinkID=799772&amp;clcid=0x409) 사용
    
그러나 DLP 보고서는 Exchange Online을 포함 하 여 Office 365 간에 데이터를 가져올 필요가 있습니다. 이러한 이유로 DLP 보고서용 cmdlet은 보안 &amp; 및 준수 센터 powershell이 아닌 Exchange Online Powershell에서 사용할 수 있습니다. 따라서 DLP 보고서에 대해 cmdlet을 사용 하려면 다음을 수행 해야 합니다.
  
1. [Connect to Exchange Online using remote PowerShell](http://go.microsoft.com/fwlink/?LinkID=799773&amp;clcid=0x409)(원격 PowerShell을 사용하여 Exchange Online에 연결)
    
2. DLP 보고서에 대해 다음 cmdlet 중 하나를 사용 합니다.
    
      - [get-dlpdetectionsreport](http://go.microsoft.com/fwlink/?LinkID=799774&amp;clcid=0x409)
    
      - [get-dlpdetailreport](http://go.microsoft.com/fwlink/?LinkID=799775&amp;clcid=0x409)
    

