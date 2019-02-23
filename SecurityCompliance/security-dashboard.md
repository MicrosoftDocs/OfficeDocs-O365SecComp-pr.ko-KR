---
title: 보안 대시보드 개요
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 02/07/2019
ms.audience: ITPro
ms.topic: overview
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: fe0b9b8f-faa9-44ff-8095-4d1b2f507b74
ms.collection: M365-security-compliance
description: 새 보안 대시보드를 사용 하 여 Office 365 위협 방지 상태를 검토 하 고 보안 경고를 보고 작동 합니다.
ms.openlocfilehash: 7fcf570887e5ed720e2e62d627b442597b824e84
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30215178"
---
# <a name="security-dashboard"></a>보안 대시보드

## <a name="overview"></a>개요

[ &amp; 보안 준수 센터](go-to-the-securitycompliance-center.md) 를 통해 조직에서 데이터 보호 및 규정 준수를 관리할 수 있습니다. 필요한 사용 권한이 있는 경우 보안 대시보드를 사용 하 여 위협 방지 상태를 검토 하 고 보안 경고에 대 한 작업을 수행할 수 있습니다. 
  
비디오를 시청 하 여 개요를 확인 한 다음이 문서를 참조 하 여 자세한 내용을 확인 하세요.
  
> [!VIDEO https://www.microsoft.com/videoplayer/embed/3540b1f8-62d2-47fa-a07d-d7ad76f55b0f?autoplay=false]
  
조직의 Office 365 구독에 포함 된 내용에 따라 보안 대시보드에는 위협 관리 요약, 위협 방지 상태, 전역 주간 위협 감지, 맬웨어 등의 여러 widget이 포함 되어 있습니다. 다음과 같은 섹션이 있습니다.
  
보안 대시보드를 보려면 [Office 365 보안 &amp; 및 준수 센터](go-to-the-securitycompliance-center.md)에서 **위협 관리** \> **대시보드로**이동 합니다.
  
> [!NOTE]
> 보안 대시보드를 보려면 Office 365 전역 관리자, 보안 관리자 또는 보안 독자 여야 합니다. 일부 위젯을 보려면 추가 권한이 필요 합니다. 자세한 내용은 [Office 365 보안 &amp; 및 준수 센터의 사용 권한](permissions-in-the-security-and-compliance-center.md)를 참조 하세요. 
  
## <a name="threat-management-summary"></a>위협 관리 요약

위협 관리 요약 위젯은 지난 7 일 동안 위협 으로부터 조직이 보호 된 방식을 한눈에 보여 줍니다.

![보안 대시보드-위협 관리 요약 위젯](media/SecDash-ThreatMgmtSummary.png)

위협 관리 요약에 표시 되는 정보는 구독에 포함 된 항목에 따라 달라 집니다. 다음 표에서는 office 365 enterprise E3 및 office 365 enterprise E5에 포함 된 정보를 설명 합니다.


|Office 365 Enterprise E3  |Office 365 Enterprise E5  |
|---------|---------|
|차단 된 맬웨어 메시지<br/>차단 된 피싱 메시지<br>사용자가 보고 한 메시지<br><br><br><br> |차단 된 맬웨어 메시지<br>차단 된 피싱 메시지<br>사용자가 보고 한 메시지<br>제로 일 맬웨어 차단<br>검색 된 고급 피싱 메시지<br>차단 된 악의적인 url |

위협 관리 요약 위젯을 보거나 액세스 하려면 Advanced Threat Protection 보고서를 볼 수 있는 권한이 있어야 합니다. 자세한 내용은 [ATP 보고서를 확인 하는 데 필요한 사용 권한](view-reports-for-atp.md#what-permissions-are-needed-to-view-the-atp-reports)를 참조 하십시오. 

## <a name="threat-protection-status"></a>위협 방지 상태

위협 방지 상태 위젯은 피싱 및 맬웨어 추이에 대 한 경향 및 상세 보기로 위협 보호 효과를 표시 합니다. 

![위협 방지 상태 위젯](media/tpswidget.png)

세부 정보는 office 365 구독에 [office 365 ATP (Advanced Threat protection](office-365-atp.md) )가 있는 EOP ( [Exchange Online Protection](eop/exchange-online-protection-eop.md) )가 포함 되어 있는지 여부에 따라 달라 집니다.


|구독에 다음이 포함 된 경우 ... |다음 정보가 표시 됩니다. |
|---------|---------|
|EOP는 아니지만 Office 365 ATP     |EOP에서 검색 및 차단 된 악의적인 전자 메일<br> [위협 방지 상태 보고서 (EOP)](view-email-security-reports.md#threat-protection-status-report)를 참조 하세요.| |
|Office 365 ATP |EOP 및 Office 365 ATP가 검색 하 고 차단한 악성 콘텐츠 및 악성 전자 메일<br>맬웨어 방지 엔진, [자동 삭제](zero-hour-auto-purge.md)및 atp 기능 ( [안전한 링크](atp-safe-links.md), [안전한 첨부 파일](atp-safe-attachments.md)및 [atp 피싱 방지](atp-anti-phishing.md))에 의해 차단 되는 악성 콘텐츠가 포함 된 고유한 전자 메일 메시지의 집계 개수입니다.<br>[ATP (Threat Protection 상태 보고서)](view-reports-for-atp.md#threat-protection-status-report)를 참조 하세요. | 

위협 방지 상태 위젯을 보거나 액세스 하려면 Advanced Threat Protection 보고서를 볼 수 있는 권한이 있어야 합니다. 자세한 내용은 [ATP 보고서를 확인 하는 데 필요한 사용 권한](view-reports-for-atp.md#what-permissions-are-needed-to-view-the-atp-reports)를 참조 하십시오. 

## <a name="global-weekly-threat-detections"></a>전역 주간 위협 감지
 
전체 주간 위협 감지 위젯은 지난 7 일 동안 전자 메일 메시지에서 검색 된 위협의 수를 보여 줍니다.

![전역 주간 위협 감지 위젯](media/globalweeklythreatdetections.png)

메트릭은 다음 표에 설명 된 대로 계산 됩니다.

|메트릭  |계산 방법  |
|---------|---------|
|검색 된 메시지 |검색 된 전자 메일 메시지의 수를 받는 사람 수에 곱하여 함 |
|위협이 중지 됨  |맬웨어를 포함 하는 것으로 식별 되는 전자 메일 메시지 수 (받는 사람 수) |
|[ATP](office-365-atp.md) 에 의해 차단 됨 |ATP에 의해 차단 되는 전자 메일 메시지 수와 받는 사람 수를 곱합니다. |
|배달 후 제거 됨 |[자동 삭제](zero-hour-auto-purge.md) 를 통해 제거 되는 메시지 수를 받는 사람 수 곱하여 |

## <a name="malware"></a>Malware

맬웨어 위젯은 지난 7 일 동안의 맬웨어 추세 및 맬웨어 패밀리 유형에 대 한 세부 정보를 표시 합니다.

![맬웨어 추세 및 패밀리 유형](media/malwarewidgetatpe5.png)
 
## <a name="insights"></a>인사이트

자세한 내용은 검토 해야 하는 주요 문제 뿐 아니라 권장 사항과 고려할 작업도 포함 되어 있습니다. 

![고급 통찰력](media/smartinsights.png)

예를 들어 일부 사용자가 정크 메일 옵션을 사용 하지 않도록 설정 했으므로 피싱 전자 메일 메시지가 배달 되는 것을 볼 수 있습니다. insights 작동 방식에 대 한 자세한 내용은 [Office 365 보안 &amp; 및 준수 센터의 Reports and insights](reports-and-insights-in-security-and-compliance.md)를 참조 하세요.
  
## <a name="threat-intelligence"></a>위협 인텔리전스

조직의 구독에 [위협 인텔리전스 기능이](office-365-ti.md)포함 되어 있는 경우 보안 대시보드에 고급 도구를 포함 하는 **위협 인텔리전스** 섹션이 있습니다. 조직의 보안 팀은이 섹션의 정보를 사용 하 여 최신 캠페인을 이해 하 고 위협을 조사 하 고 인시던트를 관리할 수 있습니다. 
  
![위협 인텔리전스를 통해 조직에서 대상이 되는 공격을 이해 하는 데 도움이 됩니다.](media/threatintelwidget.png)
  
  
## <a name="trends"></a>추세

보안 대시보드 아래쪽에는 조직에 대 한 전자 메일 흐름 추세를 요약 하는 **추세** 섹션을 소개 합니다. 보고서는 스팸으로 분류 된 전자 메일, 맬웨어, 피싱 시도 및 좋은 전자 메일에 대 한 정보를 제공 합니다. 타일을 클릭 하 여 보고서에서 자세한 정보를 볼 수 있습니다. 
  
![조직에 대 한 전자 메일 흐름 추세를 요약 하는 추세 섹션](media/trends.png)
  
또한 조직의 Office 365 구독에 [위협 인텔리전스 기능이](office-365-ti.md)포함 되어 있는 경우 보안 팀이이 섹션에서 **최신 위협 관리 경고** 보고서를 사용 하 여 해당 정보를 확인 하 고 작업을 수행할 수 있습니다. 우선 순위가 높은 보안 알림 

보내고 받은 전자 메일 위젯을 보거나 액세스 하려면 Advanced Threat Protection 보고서를 볼 수 있는 권한이 있어야 합니다. 자세한 내용은 [ATP 보고서를 확인 하는 데 필요한 사용 권한](view-reports-for-atp.md#what-permissions-are-needed-to-view-the-atp-reports)를 참조 하십시오. 

최신 위협 관리 알림 위젯을 보거나 액세스 하려면 알림을 볼 수 있는 권한이 있어야 합니다. 자세한 내용은 [경고를 보는 데 필요한 RBAC 사용 권한을](alert-policies.md#rbac-permissions-required-to-view-alerts)참조 하세요.
  
## <a name="related-topics"></a>관련 항목

[보안 &amp; 및 준수 센터의 전자 메일 보안 보고서 보기](view-email-security-reports.md)
  
[Office 365 Advanced Threat Protection에 대 한 보고서 보기](view-reports-for-atp.md)
  
[Office 365 Advanced Threat Protection 방지](office-365-atp.md)
  
[Office 365 위협 인텔리전스](office-365-ti.md)
  

