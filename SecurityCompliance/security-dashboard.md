---
title: 보안 대시보드 개요 (영문)
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 02/07/2019
ms.audience: ITPro
ms.topic: overview
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: fe0b9b8f-faa9-44ff-8095-4d1b2f507b74
ms.collection: M365-security-compliance
description: 새 보안 대시보드를 사용 하 여 Office 365 위협 보호 상태를 검토 하 고를 보고 하 보안 경고 작업을 수행 합니다.
ms.openlocfilehash: 403c47ed09e9652a66abeafb93be02589c9b1702
ms.sourcegitcommit: efccf5b4f22d34a9674bc55ebf3d88bc8bda2972
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/14/2019
ms.locfileid: "29995129"
---
# <a name="security-dashboard"></a>보안 대시보드

## <a name="overview"></a>개요

[보안 &amp; 준수 센터](go-to-the-securitycompliance-center.md) 조직 데이터 보호 및 규정 준수를 관리할 수 있도록 합니다. 보안 대시보드를 필요한 사용 권한이 가정 하 고, 위협 보호 상태를 검토 및 보기 뿐 보안 경고에 작업을 수행할 수 있습니다. 
  
한 개요를 가져올 비디오 하 한 다음 자세한 내용을 보려면이 문서를 읽습니다.
  
> [!VIDEO https://www.microsoft.com/videoplayer/embed/3540b1f8-62d2-47fa-a07d-d7ad76f55b0f?autoplay=false]
  
조직의 Office 365 구독을 포함 되는 기능에 따라 보안 대시보드 포함 위협 관리 요약, 위협 보호 상태, 전역 주간 위협 감지, 맬웨어, 등과 같은,의 설명에 따라 여러 위젯은 다음 섹션입니다.
  
보안 대시보드를 볼 수는 [Office 365 보안 &amp; 준수 센터](go-to-the-securitycompliance-center.md), **위협 관리** 로 이동 \> **대시보드**합니다.
  
> [!NOTE]
> Office 365 전역 관리자, 보안 관리자 또는 보안 판독기 보안 대시보드를 보려면 이어야 합니다. 일부 위젯 볼 수 있는 추가 권한이 필요 합니다. 자세한 내용은 참조 [Office 365 보안에 대 한 사용 권한을 &amp; 준수 센터](permissions-in-the-security-and-compliance-center.md)합니다. 
  
## <a name="threat-management-summary"></a>위협 관리 요약

위협 관리를 위한 요약 위젯 지시를 한눈 어떻게 조직 지난 7 (7) 일 동안의 위협 으로부터 보호 되었습니다.

![보안 대시보드-위협 관리를 위한 요약 위젯](media/SecDash-ThreatMgmtSummary.png)

위협 관리 요약에 표시 됩니다 정보 구독 하면 포함 된 항목에 따라 다릅니다. 다음 표에서 Office 365 엔터프라이즈 E3 및 Office 365 Enterprise e 5에 대 한 포함 되는 정보를 설명 합니다.


|Office 365 Enterprise E3  |Office 365 Enterprise E5  |
|---------|---------|
|맬웨어 메시지 차단<br/>피싱 메시지 차단<br>사용자가 보고 하는 메시지<br><br><br><br> |맬웨어 메시지 차단<br>피싱 메시지 차단<br>사용자가 보고 하는 메시지<br>제로 데가 맬웨어 차단<br>고급 피싱 메시지 검색<br>악성 Url 차단 |

보거나 위협 관리를 위한 요약 위젯에 액세스 하려면 고급 위협 보호 보고서를 볼 수 있는 권한이 있어야 합니다. 자세한 내용은 참조 [ATP 보고서를 보려면 어떤 사용 권한이 필요한?](view-reports-for-atp.md#what-permissions-are-needed-to-view-the-atp-reports)합니다. 

## <a name="threat-protection-status"></a>위협 보호 상태

위협 보호 상태 위젯 phish 및 맬웨어 추세 및 상세 보기와 위협 보호 효과를 보여줍니다. 

![위협 보호 상태 위젯](media/tpswidget.png)

세부 정보 또는 [Office 365 고급 위협 보호](office-365-atp.md) (ATP) 없이 Office 365 구독 [Exchange Online Protection](eop/exchange-online-protection-eop.md) (EOP)을 포함 하는 여부에 따라 달라 집니다.


|구독에 포함 된 경우... |이러한 세부 정보를 볼 수 있습니다. |
|---------|---------|
|EOP 하지만 Office 365 ATP 하지     |검색 및 EOP에 의해 차단 된 악의적인 전자 메일<br> [위협 보호 상태 보고서 (EOP)를](view-email-security-reports.md#threat-protection-status-report)참조 하십시오.| |
|Office 365 ATP |악의적인 콘텐츠 및 악의적인 전자 메일 감지 및 EOP 및 Office 365 ATP에 의해 차단<br>맬웨어 방지 엔진, [0-시간 자동 삭제](zero-hour-auto-purge.md), 및 ATP 기능 ( [안전한 링크](atp-safe-links.md), [안전한 첨부 파일](atp-safe-attachments.md)및 [ATP 피싱 방지](atp-anti-phishing.md)포함)에 의해 차단 되는 악의적인 콘텐츠가 포함 된 고유 전자 메일 메시지의 집계 수입니다.<br>[위협 보호 상태 보고서 ATP ()를](view-reports-for-atp.md#threat-protection-status-report)참조 하십시오. | 

보거나 위협 보호 상태 위젯에 액세스 하려면 고급 위협 보호 보고서를 볼 수 있는 권한이 있어야 합니다. 자세한 내용은 참조 [ATP 보고서를 보려면 어떤 사용 권한이 필요한?](view-reports-for-atp.md#what-permissions-are-needed-to-view-the-atp-reports)합니다. 

## <a name="global-weekly-threat-detections"></a>글로벌 주간 위협 감지
 
전역 주간 위협 감지 위젯 얼마나 많은 위협 지난 7 (7) 일간 전자 메일 메시지에서 검색 된 것을 보여줍니다.

![글로벌 주간 위협 감지 위젯](media/globalweeklythreatdetections.png)

다음 표에 설명 된 대로 메트릭을 계산 됩니다.

|메트릭  |계산 방법  |
|---------|---------|
|검색 된 메시지 |검색 된 전자 메일 메시지의 받는 사람 수를 곱한 수 |
|중지 위협  |받는 사람 수를 곱한 맬웨어를 포함 하는로 식별 된 전자 메일 메시지의 수 |
|[ATP](office-365-atp.md) 에 의해 차단 |받는 사람 수를 곱한 ATP에 의해 차단 되는 전자 메일 메시지의 수 |
|배달 후에 제거 |받는 사람 수를 곱한으로 [0 시간 자동 삭제](zero-hour-auto-purge.md) 하 여 제거 하는 메시지의 수 |

## <a name="malware"></a>Malware

지난 7 (7) 일 동안의 맬웨어 추세 및 맬웨어 가족 형식에 대 한 자세한 정보를 표시 하는 맬웨어 위젯.

![맬웨어 추세 및 가족 유형](media/malwarewidgetatpe5.png)
 
## <a name="insights"></a>인사이트

인 사이트에만 아니라 주요 문제를 검토 해야 표면, 권장 사항 및 작업을 고려 하도 포함 합니다. 

![스마트 insights (영문)](media/smartinsights.png)

예, 일부 사용자가 자신의 정크 메일 옵션을 비활성화 하기 때문에 피싱 전자 메일 메시지를 전달 되는 볼 수 있습니다. 인 사이트 작동 하는 방법에 대 한 자세한 내용은 참조 하십시오. [보고서 및 Office 365 보안에 대 한 의견 &amp; 준수 센터](reports-and-insights-in-security-and-compliance.md)합니다.
  
## <a name="threat-intelligence"></a>위협 인텔리전스

조직의 구독 [위협 인텔리전스 기능](office-365-ti.md)를 포함 하는 경우 보안 대시보드에 고급 도구를 포함 하는 **위협 인텔리전스** 섹션을 있습니다. 조직의 보안 팀이이 섹션의 정보를 사용 하 여 새로운 캠페인 이해, 위협 조사 및 사고를 관리 하 수 있습니다. 
  
![위협 인텔리전스를 사용 하면 사용자가 조직에 대상으로 하는 공격을 이해](media/threatintelwidget.png)
  
  
## <a name="trends"></a>추세

보안 대시보드의 아래쪽에 있는 조직에 대 한 전자 메일 흐름 추세를 요약 하는 **추세** 섹션은입니다. 보고서 전자 메일을 스팸, 맬웨어, 피싱 시도 하 고 효율적인 전자 메일으로 분류 하는 방법에 대 한 정보를 제공 합니다. 보고서에서 자세한 정보를 보려면 타일을 클릭 합니다. 
  
![추세 섹션에는 조직에 대 한 전자 메일 흐름 추세를 요약 되어있습니다.](media/trends.png)
  
및 **최근 위협 관리 알림** 보고서 보안 팀을 보고 조치를 취할 수 있도록 하는이 섹션에도 설치는 조직의 Office 365 구독 [위협 인텔리전스 기능](office-365-ti.md)를 포함 하는 경우 우선순위가 높은 보안 경고 합니다. 

보거나 송신 및 수신 전자 메일 위젯에 액세스 하려면 고급 위협 보호 보고서를 볼 수 있는 권한이 있어야 합니다. 자세한 내용은 참조 [ATP 보고서를 보려면 어떤 사용 권한이 필요한?](view-reports-for-atp.md#what-permissions-are-needed-to-view-the-atp-reports)합니다. 

보거나 최근 위협 관리 알림 위젯에 액세스 하려면 경고를 볼 수 있는 권한이 있어야 합니다. 자세한 내용은, [RBAC 권한이 필요한 알림을 보려면](alert-policies.md#rbac-permissions-required-to-view-alerts)를 참조 합니다.
  
## <a name="related-topics"></a>관련 항목

[보안에서 전자 메일 보안 보고서를 보려면 &amp; 준수 센터](view-email-security-reports.md)
  
[Office 365 고급 위협 보호에 대 한 보고서 보기](view-reports-for-atp.md)
  
[Office 365 Advanced Threat Protection 방지](office-365-atp.md)
  
[Office 365 위협 인텔리전스](office-365-ti.md)
  

