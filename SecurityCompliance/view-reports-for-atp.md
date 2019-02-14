---
title: Office 365 고급 위협 보호에 대 한 보고서 보기
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 02/13/2019
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: e47e838c-d99e-4c0b-b9aa-e66c4fae902f
ms.collection: M365-security-compliance
description: 찾기 및 보안에서 Office 365 고급 위협 보호에 대 한 보고서를 사용 하는 방법에 알아봅니다 &amp; 준수 센터입니다.
ms.openlocfilehash: a27fdf6c7d04a2526873047d4e2a33bb283878b3
ms.sourcegitcommit: efccf5b4f22d34a9674bc55ebf3d88bc8bda2972
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/14/2019
ms.locfileid: "29995229"
---
# <a name="view-reports-for-office-365-advanced-threat-protection"></a>Office 365 고급 위협 보호에 대 한 보고서 보기

조직에 [Office 365 고급 위협 보호](office-365-atp.md) (ATP) 하는 경우 [필요한 사용 권한](#what-permissions-are-needed-to-view-these-reports)을 가진 사용자는 보안에서 여러 ATP 보고서를 사용할 수 있습니다 &amp; 준수 센터입니다. ( **보고서** 로 이동 \> **대시보드**.)
  
![보안&amp; 규정 준수 센터 대시보드는 Advanced Threat Protection이 작업 중인 위치를 확인할 수 있도록 도와줍니다](media/6b213d34-adbb-44af-8549-be9a7e2db087.png)
  
ATP 보고서 [위협 보호 상태 보고서](#threat-protection-status-report), [ATP 파일 형식 보고서](#atp-file-types-report)및 [ATP 메시지 처리 보고서](#atp-message-disposition-report)를 포함 합니다. 이 문서 ATP 보고서에 설명 하 고 [보려는 추가 보고서](#additional-reports-to-view)에 대 한 링크를 포함 합니다.
  
## <a name="threat-protection-status-report"></a>위협 보호 상태 보고서

**위협 보호 상태** 보고서에는 함께 악의적인 콘텐츠 및 악의적인 전자 메일 감지 및 [Exchange Online Protection](eop/exchange-online-protection-overview.md) (EOP) 및 [Office 365 ATP](office-365-atp.md)에 의해 차단 하는 방법에 대 한 정보를 제공 하는 단일 보기입니다. 보고서에서 제공 하는 집계 된 횟수가 악의적인 콘텐츠가 포함 된 (파일 또는 웹사이트 주소 (Url)) 맬웨어 방지 엔진, [0-시간 자동 삭제 (ZAP)](zero-hour-auto-purge.md), 및 [ATP 안전한 링크](atp-safe-links.md), [ATP 안전 하 게 보호 등의 ATP 기능에 의해 차단 되는 고유한 전자 메일 메시지 첨부 파일](atp-safe-attachments.md), [ATP 피싱 방지 기능](atp-anti-phishing.md)을 합니다.

> [!NOTE]
> 위협 보호 상태 보고서는 고객에 게 [Office 365 ATP](office-365-atp.md) 또는 [Exchange Online Protection](eop/exchange-online-protection-eop.md) (EOP);가 사용할 수 있는 그러나 ATP 고객에 대 한 위협 보호 상태 보고서에 표시 되는 정보 나타날 EOP 고객 보다 다양 한 데이터를 가능성이 포함 됩니다. 예, ATP 고객에 대 한 위협 보호 상태 보고서에는 [SharePoint Online, OneDrive, 또는 Microsoft 팀의 악의적인 파일을 검색](atp-for-spo-odb-and-teams.md)하는 방법에 대 한 정보가 포함 됩니다. 이러한 정보 ATP, 특정 이므로 고객은 EOP 하지만 ATP 하지는 자신의 위협 보호 상태 보고서에서 해당 정보를 표시 되지 것입니다.
  
에 위협 보호 상태 보고서를 보려면는 [보안 &amp; 준수 센터](https://protection.office.com), **보고서** 로 이동 \> **대시보드** \> **위협 보호 상태**입니다.
  
![ATP 위협 보호 상태 보고서](media/6bdd41eb-62e0-423b-9fd4-d1d5baf0cbd5.png)
  
하루에 대 한 자세한 상태를 가져올, 그래프를 가리킵니다.
  
![하루에 대 한 ATP 위협 보호 상태 데이터](media/d5c2c6ad-c002-4985-a032-c866e46fdea8.png)
  
기본적으로 위협 보호 상태 보고서는 지난 7 일간에 대 한 데이터를 표시 합니다. 그러나 **필터** 를 선택 하 고 최대 90 일 동안 데이터를 보려는 날짜 범위를 변경할 수 있습니다. 
  
![ATP 위협 보호 상태 필터입니다.](media/4f703369-642b-402b-9758-b9c828283410.png)
  
또한 보고서에 표시 되는 정보를 변경 하 **여 데이터 보기** 메뉴를 사용할 수 있습니다. 
  
![ATP 위협 보호 상태 보고서에 대 한 표시 옵션](media/4959bf8c-d192-4542-b00b-184e101e7513.png)
  
## <a name="atp-file-types-report"></a>ATP 파일 형식 보고서

**ATP 파일 형식** 보고서 [ATP 안전한 첨부](atp-safe-attachments.md)하 여 악의적으로 감지 하는 파일의 종류를 표시 합니다.
  
이 보고서를 보려면는 [보안 &amp; 준수 센터](https://protection.office.com), **보고서** 로 이동 \> **대시보드** \> **ATP 파일 형식**입니다.
  
![ATP 파일 형식 보고서](media/6e3f5d33-79aa-4b2d-938c-6ef135d9e54c.png)
  
특정 일 위에 마우스를 가져가면 [ATP 안전한 첨부 파일](atp-safe-attachments.md) 에서 검색 된 악의적인 파일 형식 분석을 볼 수 있습니다 및 [스팸 방지 &amp; Office 365의 맬웨어 방지 보호 기능](anti-spam-and-anti-malware-protection.md)합니다.
  
![하루에 대 한 데이터를 보고 하는 ATP 파일 형식](media/10d18428-699a-41d2-a73e-be3a8214ada1.png)
  
## <a name="atp-message-disposition-report"></a>ATP 메시지 처리 보고서

**ATP 메시지 처리** 보고서가 악의적인 콘텐츠가 있는 것으로 검색 된 전자 메일 메시지에 대 한 수행 된는 작업을 표시 합니다. 
  
이 보고서를 보려면는 [보안 &amp; 준수 센터](https://protection.office.com), **보고서** 로 이동 \> **대시보드** \> **ATP 메시지 처리**합니다.
  
![ATP 메시지 처리 보고서](media/b0ff65c4-53d3-496d-bafa-8937a5eb69e5.png)
  
다음은 차트에서 막대 위에 마우스를 가져가면 해당 날짜에 대 한 검색 된 전자 메일에 대해 어떤 작업을 수행을 볼 수 있습니다.
  
![하루에 대 한 ATP 메시지 처리 보고서 데이터](media/68d2beb8-4b30-48c4-8ba6-5e8ab88ae456.png)
  
## <a name="additional-reports-to-view"></a>추가 보고서를 보려면

다음 표에 설명 된 대로이 문서에 설명 된 ATP 보고서 외에도 다른 여러 보고서를를 사용할 수 있습니다.

|보고서 유형  |자세한 정보  |
|---------|---------|
|**전자 메일 보안 보고서**와 같은, 위쪽 보낸사람 및 받는 사람에 게 보고서, 스푸핑 메일 보고서 및 스팸이 감지 된 보고서입니다. | [보안에서 전자 메일 보안 보고서를 보려면 &amp; 준수 센터](view-email-security-reports.md)        |
|**탐색기** (위협 탐색기 라고도 함,이에 포함 된 [Office 365 위협 인텔리전스](office-365-ti.md))     | [탐색기를 사용 하 여 보안에서 &amp; 준수 센터](use-explorer-in-security-and-compliance.md)        |
|**EOP 및 ATP 결과** (PowerShell을 사용 하 여 생성 하는 사용자 지정 보고서 임). 이 보고서에는 도메인, 날짜, 이벤트 유형, 방향, 동작 및 메시지 수와 같은 정보를 포함합니다.  | [Get MailTrafficATPReport cmdlet 참조 (영문)](https://docs.microsoft.com/powershell/module/exchange/advanced-threat-protection/get-mailtrafficatpreport?view=exchange-ps) |
|**EOP 및 ATP 감지** (PowerShell을 사용 하 여 생성 하는 사용자 지정 보고서 임). 이 보고서는 악의적인 파일 또는 Url, 피싱 시도, 가장, 및 전자 메일 또는 파일에 대 한 기타 잠재적 위협에 대 한 세부 정보를 포함합니다.   | [Get MailDetailATPReport cmdlet 참조 (영문)](https://docs.microsoft.com/powershell/module/exchange/advanced-threat-protection/get-maildetailatpreport?view=exchange-ps)        |

  
## <a name="what-permissions-are-needed-to-view-the-atp-reports"></a>사용 권한은 ATP 보고서를 보려면 필요 합니까?

이 문서에 설명 된 보고서 보기 및 사용 하기 위해 **모두 보안을 위해 할당 되는 적절 한 역할을 해야 &amp; 준수 센터 및 Exchange 관리 센터**합니다.

- 보안을 위해 &amp; 준수 센터 있어야 할당 된 다음 역할 중 하나:
    - 조직 관리
    - 보안 관리자 (Azure Active Directory 관리 센터에서이 할당할 수 있습니다 ([https://aad.portal.azure.com](https://aad.portal.azure.com))
    - 보안 읽기 권한자

- Exchange Online에 대 한 있어야 Exchange 관리 센터에 할당 된 다음 역할 중 하나 ([https://outlook.office365.com/ecp](https://outlook.office365.com/ecp)) 또는 PowerShell cmdlet (참조 [Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/exchange-online-powershell?view=exchange-ps))을 사용 합니다.
    - 조직 관리
    - 보기 전용 조직 관리
    - 보기 권한만 있는 받는 사람 역할
    - 준수 관리

자세한 내용은 다음 리소스를 참조 합니다.

- [Office 365 보안에 대 한 사용 권한을 &amp; 준수 센터](permissions-in-the-security-and-compliance-center.md)

- [Exchange Online의 기능 사용 권한](https://docs.microsoft.com/exchange/permissions-exo/feature-permissions)
   
## <a name="what-if-the-reports-arent-showing-data"></a>경우에 어떻게 보고서 데이터를 표시 하지?

ATP 보고서의 데이터를 나타나지 않는 경우 정책에 올바르게 설정 하는 다시 확인 하십시오. 조직 전체에 포함 되도록 [ATP 안전한 링크 정책](set-up-atp-safe-links-policies.md) 및 ATP 보호에 대 한 순서에 정의 된 [ATP 안전한 첨부 파일 정책](set-up-atp-safe-attachments-policies.md) 있어야 합니다. 또한 [Office 365의 스팸 방지 및 맬웨어 방지 보호 기능](anti-spam-and-anti-malware-protection.md)을 참조 하십시오.
  
## <a name="related-topics"></a>관련 항목

[보고서 및 Office 365 보안에 대 한 의견 &amp; 준수 센터](reports-and-insights-in-security-and-compliance.md)
  
[보안에서 보고서에 대 한 일정을 만들 &amp; 준수 센터](create-a-schedule-for-a-report.md)
  
[설정 및 보안에서 사용자 지정 보고서를 다운로드 &amp; 준수 센터](set-up-and-download-a-custom-report.md)
  

