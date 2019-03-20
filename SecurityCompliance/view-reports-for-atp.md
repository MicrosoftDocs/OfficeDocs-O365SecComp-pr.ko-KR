---
title: Office 365 Advanced Threat Protection에 대 한 보고서 보기
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 03/19/2019
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: e47e838c-d99e-4c0b-b9aa-e66c4fae902f
ms.collection:
- M365-security-compliance
description: 보안 &amp; 및 준수 센터에서 Office 365 Advanced Threat Protection에 대 한 보고서를 찾아서 사용 하는 방법에 대해 알아봅니다.
ms.openlocfilehash: 3a128103d16ed03edb18becde96a5d20ee6eca9b
ms.sourcegitcommit: 0f93b37c39d807dec91f118aa671a3430c47a9ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/20/2019
ms.locfileid: "30692407"
---
# <a name="view-reports-for-office-365-advanced-threat-protection"></a>Office 365 Advanced Threat Protection에 대 한 보고서 보기

조직에 [Office 365 ATP (Advanced Threat Protection](office-365-atp.md) )가 있고 [필요한 사용 권한이](#what-permissions-are-needed-to-view-these-reports)있는 경우 보안 &amp; 및 준수 센터에서 여러 ATP 보고서를 사용할 수 있습니다. ( **보고서** \> **대시보드로**이동 합니다.)
  
![보안&amp; 규정 준수 센터 대시보드는 Advanced Threat Protection이 작업 중인 위치를 확인할 수 있도록 도와줍니다](media/6b213d34-adbb-44af-8549-be9a7e2db087.png)
  
atp 보고서에는 [위협 보호 상태 보고서](#threat-protection-status-report), [atp 파일 형식 보고서](#atp-file-types-report)및 [ATP 메시지 처리 보고서](#atp-message-disposition-report)가 포함 됩니다. 이 문서에서는 ATP 보고서에 대해 설명 하 고 [확인할 추가 보고서](#additional-reports-to-view)에 대 한 링크를 제공 합니다.
  
## <a name="threat-protection-status-report"></a>위협 방지 상태 보고서

**위협 방지 상태** 보고서는 EOP ( [Exchange Online Protection](eop/exchange-online-protection-overview.md) ) 및 [Office 365 ATP](office-365-atp.md)에 의해 감지 되어 차단 된 악의적인 콘텐츠와 악성 전자 메일에 대 한 정보를 함께 가져오는 단일 보기입니다. 이 보고서는 맬웨어 방지 엔진, [0 시간 자동 제거 (ZAP)](zero-hour-auto-purge.md)및 atp (전송 안전한 [링크](atp-safe-links.md), [atp 안전)에 의해 차단 되는 악의적인 콘텐츠 (파일 또는 웹 사이트 주소 (url))의 집계 된 고유 전자 메일 메시지 수를 제공 합니다. 첨부 파일](atp-safe-attachments.md)및 [ATP 피싱 방지 기능](atp-anti-phishing.md)

> [!NOTE]
> [Office 365 ATP](office-365-atp.md) 또는 [Exchange Online Protection](eop/exchange-online-protection-eop.md) (EOP)이 있는 고객은 위협 보호 상태 보고서를 사용할 수 있습니다. 그러나 ATP 고객에 대 한 위협 방지 상태 보고서에 표시 되는 정보에는 고객에 게 표시 될 수 있는 것과 다른 데이터가 포함 될 가능성이 EOP. 예를 들어 ATP 고객에 대 한 위협 방지 상태 보고서에는 [SharePoint Online, OneDrive 또는 Microsoft 팀에서 검색 된 악성 파일](atp-for-spo-odb-and-teams.md)에 대 한 정보가 포함 됩니다. 이러한 정보는 atp와 관련 된 것 이므로, EOP가 아닌 고객은 위협 보호 상태 보고서에 해당 세부 정보를 볼 수 없습니다.
  
위협 방지 상태 보고서를 보려면 [보안 &amp; 및 준수 센터](https://protection.office.com)에서 **보고서** \> **대시보드** \> **위협 보호 상태로**이동 합니다.
  
![ATP 위협 방지 상태 보고서](media/6bdd41eb-62e0-423b-9fd4-d1d5baf0cbd5.png)
  
하루 동안 자세한 상태를 보려면 그래프를 가리킵니다.
  
![ATP 위협 방지 상태 데이터 (일)](media/d5c2c6ad-c002-4985-a032-c866e46fdea8.png)
  
기본적으로 위협 방지 상태 보고서에는 최근 7 일간의 데이터가 표시 됩니다. 그러나 **필터** 를 선택 하 고 날짜 범위를 변경 하 여 데이터를 최대 90 일까 지 확인할 수 있습니다. 
  
![ATP 위협 방지 상태 필터](media/4f703369-642b-402b-9758-b9c828283410.png)
  
**데이터 보기 기준** 메뉴를 사용 하 여 보고서에 표시 되는 정보를 변경할 수도 있습니다. 
  
![ATP 위협 방지 상태 보고서에 대 한 옵션 보기](media/4959bf8c-d192-4542-b00b-184e101e7513.png)
  
## <a name="atp-file-types-report"></a>ATP 파일 형식 보고서

**atp 파일 형식** 보고서에는 [atp 안전한 첨부 파일](atp-safe-attachments.md)에 의해 악의적으로 검색 된 파일 유형이 표시 됩니다.
  
이 보고서를 보려면 [보안 &amp; 및 준수 센터](https://protection.office.com)에서 **보고서** \> **대시보드** \> **ATP 파일 형식**으로 이동 합니다.
  
![ATP 파일 형식 보고서](media/6e3f5d33-79aa-4b2d-938c-6ef135d9e54c.png)
  
특정 날짜를 마우스로 가리키면 [ATP 수신 허용 첨부 파일](atp-safe-attachments.md) 및 [Office 365의 스팸 &amp; 방지 바이러스 백신 보호 기능](anti-spam-and-anti-malware-protection.md)에서 검색 된 악의적인 파일의 유형을 확인할 수 있습니다.
  
![ATP 파일 형식 하루에 대 한 보고서 데이터](media/10d18428-699a-41d2-a73e-be3a8214ada1.png)
  
## <a name="atp-message-disposition-report"></a>ATP 메시지 처리 보고서

**ATP 메시지 처리** 보고서에는 악성 콘텐츠가 있는 것으로 검색 된 전자 메일 메시지에 대해 수행 된 작업이 표시 됩니다. 
  
이 보고서를 보려면 [보안 &amp; 및 준수 센터](https://protection.office.com)에서 **보고서** \> **대시보드** \> **ATP 메시지 처리**로 이동 합니다.
  
![ATP 메시지 처리 보고서](media/b0ff65c4-53d3-496d-bafa-8937a5eb69e5.png)
  
차트의 막대 위에 마우스를 올리면 해당 요일의 검색 된 전자 메일에 대해 수행한 작업을 확인할 수 있습니다.
  
![ATP 메시지 처리 보고서 데이터 (일)](media/68d2beb8-4b30-48c4-8ba6-5e8ab88ae456.png)
  
## <a name="additional-reports-to-view"></a>볼 수 있는 추가 보고서

이 문서에서 설명 하는 ATP 보고서 외에도 다음 표에 설명 된 것 처럼 다른 몇 가지 보고서를 사용할 수 있습니다.

|보고서 유형  |자세한 정보  |
|---------|---------|
|상위 보낸 사람 및 받는 사람 보고서, 스푸핑 메일 보고서, 스팸 감지 보고서 등의 **전자 메일 보안 보고서** | [보안 &amp; 및 준수 센터의 전자 메일 보안 보고서 보기](view-email-security-reports.md)        |
|**탐색기** (위협 탐색기 라고도 하며,이는 [Office 365 Advanced Threat Protection 계획 2](office-365-ti.md)에 포함 되어 있습니다.)     | [보안 &amp; 및 준수 센터에서 탐색기 사용](use-explorer-in-security-and-compliance.md)        |
|**EOP 및 ATP 결과** (PowerShell을 사용 하 여 생성 하는 사용자 지정 보고서입니다.) 이 보고서에는 도메인, 날짜, 이벤트 유형, 방향, 동작 및 메시지 수와 같은 정보가 포함 됩니다.  | [MailTrafficATPReport cmdlet 참조](https://docs.microsoft.com/powershell/module/exchange/advanced-threat-protection/get-mailtrafficatpreport?view=exchange-ps) |
|**EOP 및 ATP** 검색 (PowerShell을 사용 하 여 생성 하는 사용자 지정 보고서입니다.) 이 보고서에는 악성 파일 또는 url, 피싱 시도, 가장 및 기타 잠재적 위협 (전자 메일 또는 파일)에 대 한 자세한 정보가 포함 되어 있습니다.   | [MailDetailATPReport cmdlet 참조](https://docs.microsoft.com/powershell/module/exchange/advanced-threat-protection/get-maildetailatpreport?view=exchange-ps)        |

  
## <a name="what-permissions-are-needed-to-view-the-atp-reports"></a>ATP 보고서를 표시 하는 데 필요한 사용 권한은 무엇입니까?

이 문서에서 설명 하는 보고서를 보고 사용 하려면 **보안 &amp; 및 준수 센터와 Exchange 관리 센터 둘 다에 대해 적절 한 역할이 할당 되어 있어야 합니다**.

- 보안 &amp; 및 준수 센터에는 다음 역할 중 하나가 할당 되어 있어야 합니다.
    - 조직 관리
    - 보안 관리자 (Azure Active Directory 관리 센터[https://aad.portal.azure.com](https://aad.portal.azure.com)에서 할당할 수 있음)
    - 보안 독자

- exchange online의 경우 exchange 관리 센터 ([https://outlook.office365.com/ecp](https://outlook.office365.com/ecp)) 또는 PowerShell cmdlet ( [exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/exchange-online-powershell?view=exchange-ps)참조)에서 다음 역할 중 하나를 할당 받아야 합니다.
    - 조직 관리
    - 보기 전용 조직 관리
    - 보기 권한만 있는 받는 사람 역할
    - 준수 관리

자세한 내용은 다음 리소스를 참조 하십시오.

- [Permissions in the Office 365 Security &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md)

- [Exchange Online의 기능 사용 권한](https://docs.microsoft.com/exchange/permissions-exo/feature-permissions)
   
## <a name="what-if-the-reports-arent-showing-data"></a>보고서에 데이터가 표시 되지 않으면 어떻게 하나요?

ATP 보고서에 데이터가 표시 되지 않는 경우 정책이 올바르게 설정 되어 있는지 다시 확인 합니다. 조직에 atp 보호 기능을 적용 하려면 atp [안전한 링크 정책](set-up-atp-safe-links-policies.md) 및 [atp 안전 첨부 파일 정책이](set-up-atp-safe-attachments-policies.md) 정의 되어 있어야 합니다. 또한 [Office 365에서 스팸 방지 및 맬웨어 방지 보호 기능을](anti-spam-and-anti-malware-protection.md)참조 하세요.
  
## <a name="related-topics"></a>관련 항목

[Office 365 보안 &amp; 및 준수 센터의 보고서 및 정보](reports-and-insights-in-security-and-compliance.md)
  
[보안 &amp; 및 준수 센터에서 보고서 일정 만들기](create-a-schedule-for-a-report.md)
  
[보안 &amp; 및 준수 센터에서 사용자 지정 보고서 설정 및 다운로드](set-up-and-download-a-custom-report.md)
  

