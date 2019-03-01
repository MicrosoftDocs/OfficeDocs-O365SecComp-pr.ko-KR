---
title: 보안 &amp; 및 준수 센터의 전자 메일 보안 보고서 보기
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 02/21/2019
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 3a137e28-1174-42d5-99af-f18868b43e86
ms.collection:
- M365-security-compliance
description: Office 365 Enterprise를 사용 하 여 조직에 대 한 전자 메일 보안 보고서를 찾아서 사용 하는 방법에 대해 알아봅니다. 보안 &amp; 및 준수 센터에서 전자 메일 보안 보고서를 사용할 수 있습니다.
ms.openlocfilehash: 833cb4e0b90375179a4ce2097cb986926a9856d0
ms.sourcegitcommit: 48fa456981b5c52ab8aeace173c8366b9f36723b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/28/2019
ms.locfileid: "30341449"
---
# <a name="view-email-security-reports-in-the-security-amp-compliance-center"></a>보안 &amp; 및 준수 센터의 전자 메일 보안 보고서 보기

[ &amp; 보안 및 준수 센터](https://protection.office.com) 에서 다양 한 보고서를 사용할 수 있으므로 Office 365의 스팸 방지, 맬웨어 방지 및 암호화 기능과 같은 전자 메일 보안 기능에서 조직을 보호 하는 방법을 확인할 수 있습니다. [필요한 권한이](#what-permissions-are-needed-to-view-these-reports) &amp; 있는 경우 **보고서** \> **대시보드로**이동 하 여 보안 및 준수 센터에서 이러한 보고서를 볼 수 있습니다.
  
![Advanced Threat Protection이 작동 하는 방식을 보는 대시보드](media/6b213d34-adbb-44af-8549-be9a7e2db087.png)
  
전자 메일 보안 보고서에는 다음이 포함 됩니다.

- [암호화 보고서](#encryption-report) (새로운 방법!)
  
- [위협 방지 상태 보고서](view-email-security-reports.md#tps) 
    
- [맬웨어 감지 보고서](view-email-security-reports.md#maldet)
    
- [주요 맬웨어 보고서](#top-malware-report)
    
- [상위 보낸 사람 및 받는 사람 보고서](view-email-security-reports.md#topsenders)
    
- [스푸핑 메일 보고서](#spoof-mail-report)
    
- [스팸 감지 보고서](#spam-detections-report)
    
- [보내고 받은 전자 메일 보고서](view-email-security-reports.md#sentreceivedemail)

- [사용자가 보고 한 메시지 보고서](view-email-security-reports.md#userreported)
    
## <a name="encryption-report"></a>암호화 보고서

(**새로운 방법!**) **암호화 보고서** 에는 정책 또는 최종 사용자 컨트롤을 통해 암호화 된 전자 메일 메시지에 대 한 정보가 표시 됩니다. 조직의 보안 팀은이 정보를 사용 하 여 패턴을 식별 하 고 중요 한 전자 메일 메시지에 대 한 정책을 사전에 적용 하거나 조정할 수 있습니다.

이 보고서를 보려면 보안 & 준수 센터에서 **보고서** \> **대시보드** \> **암호화 보고서**로 이동 합니다.

![암호화 보고서](media/encryptionreport-defaultview.png) 

보고서를 처음 열면 전자 메일 메시지에 사용 되는 암호화 방법에 대 한 데이터가 이전의 7 일 (7)로 표시 됩니다. 화면의 오른쪽 위 모서리에 있는 필터를 클릭 하 여 보고서의 날짜 범위와 세부 정보를 변경할 수 있습니다.

![암호화 보고서 필터](media/encryptionreport-filters.png)   

또한 아래로 나누기 메뉴를 사용 하 여 암호화 서식 파일 (또는 방법)을 통해 데이터를 볼 수도 있습니다.

![암호화 방법 또는 서식 파일](media/encryptionreport-breakdownby.png)

또한 데이터 보기 기준 메뉴를 사용 하 여 상위 5 개 받는 사람 도메인에 대 한 암호화 된 메시지 수를 확인 하기 위해 보기를 변경할 수 있습니다.

![암호화 보고서 데이터 보기 별 메뉴](media/encryptionreport-viewdataby.png)

새 암호화 보고서를 유연 하 게 사용 하 여 추세를 확인 하 고 적절 한 조치를 취할 수 있습니다. 예를 들어 사용자가 암호화 한 전자 메일 메시지가 많은 경우 특정 사용 사례에 대 한 암호화를 자동화 하는 암호화 정책을 추가할 수 있습니다. 또한 사용할 수 있는 암호화 서식 파일의 수가 여러 개 있지만 아무도 사용 하지 않는 경우에는 사용자가 해당 기능에 대 한 교육을 받아야 하는지 여부를 탐색할 수 있습니다. 

이 보고서를 사용 하면 조직의 보안 및 규정 준수 팀이 메시지 암호화를 사용 하는 방법과 추가 작업이 필요한 지 여부를 모니터링할 수 있습니다.

## <a name="threat-protection-status-report"></a>위협 방지 상태 보고서

**위협 방지 상태** 보고서는 Exchange Online Protection에서 검색 하 여 차단한 악성 전자 메일을 보여 주는 스마트 보고서입니다. 이 보고서에는 맬웨어가 나 피싱 시도로 식별 된 전자 메일에 대 한 정보가 표시 됩니다. 

> [!NOTE]
> [Office 365 ATP](office-365-atp.md) 또는 [Exchange Online Protection](eop/exchange-online-protection-eop.md) (EOP)이 있는 고객은 위협 보호 상태 보고서를 사용할 수 있습니다. 그러나 ATP 고객에 대 한 위협 방지 상태 보고서에 표시 되는 정보에는 고객에 게 표시 될 수 있는 것과 다른 데이터가 포함 될 가능성이 EOP. 예를 들어 EOP 고객은 전자 메일로 검색 된 맬웨어에 대 한 정보를 볼 수 있지만, [SharePoint Online, OneDrive 또는 Microsoft 팀에서 검색 된 악성 파일](atp-for-spo-odb-and-teams.md)에 대 한 정보는 ATP 관련 기능입니다. [ATP 보고서에 대해 자세히 알아보세요](view-reports-for-atp.md).
  
이 보고서를 보려면 [보안 &amp; 및 준수 센터](https://protection.office.com)에서 **보고서** \> **대시보드** \> **위협 보호 상태로**이동 합니다.
  
![위협 방지 상태 보고서](media/0ff86e12-c2b2-4d89-92a5-cefb054dc070.png)
  
위협 방지 상태 보고서를 처음 열면 보고서에는 기본적으로 이전의 7 일간의 데이터가 표시 됩니다. 그러나 **필터** 를 클릭 하 고 날짜 범위를 최대 90 일 정도 변경할 수 있습니다. 이 보고서는 조직의 Exchange Online 보호 기능과 장기적인 추세에 대 한 영향을 확인 하는 데 유용 합니다. 
  
![위협 보호 상태 보고서 필터](media/ab6b6b8d-e97a-4c3a-8fb1-c4940dcb7a07.png)
  
또한 해로운 것으로 확인 된 전자 메일, 피싱 시도로 식별 되는 전자 메일 또는 맬웨어로 식별 된 전자 메일에 대 한 데이터를 볼 수도 있습니다.
  
![위협 보호 상태 보고서 보기 옵션](media/d429ecd7-cb7a-4c99-8d27-79a2832cf467.png)
  
## <a name="malware-detections-report"></a>맬웨어 감지 보고서

**맬웨어 감지** 보고서에는 조직에 대 한 맬웨어를 포함 하는 것으로 검색 된 수신 및 발신 메시지의 수가 표시 됩니다. 
  
이 보고서를 보려면 [보안 &amp; 및 준수 센터](https://protection.office.com)에서 **보고서** \> **대시보드** \> **맬웨어 감지**로 이동 합니다.
  
![맬웨어 감지 보고서 예](media/a1ba61a3-565a-46d6-b0d5-6a6cff6b31d7.png)
  
위협 방지 상태 보고서와 같은 다른 보고서와 마찬가지로 보고서에는 최근 7 일간의 데이터가 기본적으로 표시 됩니다. 그러나 **필터** 를 선택 하 여 날짜 범위를 변경할 수는 있습니다. 
  
## <a name="top-malware-report"></a>주요 맬웨어 보고서

**주요 맬웨어** 보고서에는 Exchange Online에서 검색 된 다양 한 유형의 맬웨어가 표시 됩니다. 
  
이 보고서를 보려면 [보안 &amp; 및 준수 센터](https://protection.office.com)에서 **보고서** \> **대시보드** \> **최상위 맬웨어로**이동 합니다.
  
![SCC-EOP 최상위 맬웨어](media/763330b3-f56e-4ba4-b0bb-051500ae950a.png)
  
원형 차트의 쐐기형 위에 마우스를 가져가면 맬웨어 종류와 해당 맬웨어가 있는 것으로 검색 된 메시지의 수를 볼 수 있습니다.
  
보고서를 클릭 하거나 탭 하 여 새 브라우저 창에서 보고서를 열 수 있습니다.
  
![이 보고서에는 조직에 대해 검색 된 최상위 맬웨어가 표시 됩니다.](media/3fded224-fb31-4713-86f2-8afce5ce2991.png)
  
이 차트 아래에는 검색 된 맬웨어 목록과 해당 맬웨어가 있는 것으로 검색 한 메시지 수가 표시 됩니다.
  
## <a name="top-senders-and-recipients-report"></a>상위 보낸 사람 및 받는 사람 보고서

**상위 보낸 사람 및 받는 사람** 보고서는 상위 전자 메일 보낸 사람을 표시 하는 원형 차트입니다. 
  
이 보고서를 보려면 [보안 &amp; 및 준수 센터](https://protection.office.com)에서 **보고서** \> **대시보드의** \> **가장 큰 보낸 사람 및 받는 사람**으로 이동 합니다.
  
![이 보고서를 보려면 보안 &amp; 및 준수 센터에서 보고서 \> 대시보드 \> 최상위 보낸 사람 및 받는 사람으로 이동 합니다.](media/b5506b5c-2420-4a5a-9ea3-d654294ac838.png)
  
원형 차트의 쐐기형 위에 마우스를 올리면 보내거나 받은 메시지 수가 표시 됩니다.
  
보고서를 클릭 하거나 탭 하 여 새 브라우저 창에서 보고서를 열 수 있습니다.
  
**데이터 표시** 순서 목록을 사용 하 여 상위 보낸 사람, 받는 사람, 스팸 및 맬웨어 받는 사람에 대 한 데이터를 볼 지 여부를 선택 합니다. Advanced Threat Protection에서 검색 된 맬웨어를 받은 사용자도 볼 수 있습니다. 
  
![데이터 표시 목록을 사용 하 여 특정 정보 보기](media/bd91449f-7d42-4749-8666-7b44044049b8.png)
  
차트 아래에는 지정 된 기간 동안 보내거나 받은 메시지 수와 함께 맨 위에 있는 전자 메일 보낸 사람 또는 받는 사람이 표시 되는 사람을 볼 수 있습니다.
  
## <a name="spoof-detections-report"></a>스푸핑 감지 보고서

**스푸핑** 감지 보고서에는 얼마나 많은 스푸핑 메일 메시지가 검색 되었는지, 즉 합법적인 비즈니스 이유로 인해 스푸핑 메일을 "양호" 한 것으로 간주 되는 메시지 들이 표시 됩니다. 
  
이 보고서를 보려면 [보안 &amp; 및 준수 센터](https://protection.office.com)에서 **보고서** \> **대시보드** \> **스푸핑 메일로**이동 합니다.
  
![보안 &amp; 및 준수 센터에서 보고서 \> 대시보드 \> 위장 메일로 이동 합니다.](media/0427e85c-9e40-4225-a0f0-e21a4e8b0e44.png)
  
차트에서 특정 날짜를 마우스로 가리키면 위장 메일 메시지의 수를 확인할 수 있습니다.
  
보고서를 클릭 하거나 탭 하 여 새 브라우저 창에서 보고서를 열 수 있습니다.
  
## <a name="spam-detections-report"></a>스팸 감지 보고서

**스팸 감지** 보고서에는 Exchange Online에서 차단 된 모든 스팸 콘텐츠가 표시 됩니다. 
  
이 보고서를 보려면 [보안 &amp; 및 준수 센터](https://protection.office.com)에서 **보고서** \> **대시보드** \> **스팸 감지**로 이동 합니다.
  
![이 보고서를 보려면 보안 &amp; 및 준수 센터에서 보고서 \> 대시보드 \> EOP 스팸 감지로 이동 합니다.](media/028cff3c-79ce-4ec0-8f0f-ec32ac28243a.png)
  
차트에서 특정 날짜를 가리키면 해당 항목을 분류 한 방법 뿐 아니라 해당 요일이 차단 된 항목의 개수를 확인할 수 있습니다. 예를 들어 필터링 된 스팸 메시지 수와 IP (인터넷 프로토콜) 주소에서 가져온 항목 수를 확인할 수 있습니다.
  
보고서를 클릭 하거나 탭 하 여 새 브라우저 창에서 보고서를 열 수 있습니다.
  
![스팸 감지 보고서는 차단 되거나 필터링 된 스팸 메시지의 수를 알려 줍니다.](media/370ec67d-eb30-4863-bfcf-68a41be02295.png)
  
차트 아래에 검색 된 스팸 항목 목록이 표시 됩니다. 항목을 선택 하 여 스팸 항목이 인바운드 인지, 아웃 바운드 인지, 메시지 ID 및 받는 사람과 같은 추가 정보를 확인 합니다.
  
## <a name="sent-and-received-email-report"></a>보내고 받은 전자 메일 보고서

**Sent and received email** 보고서는 스팸 감지, 맬웨어 및 "양호"로 식별 된 전자 메일을 포함 하 여 수신 및 발신 전자 메일에 대 한 정보를 표시 하는 스마트 보고서입니다. 
  
이 보고서를 보려면 [ &amp; 보안 준수 센터](https://protection.office.com)에서 **보고서** \> **대시보드** \> **보내기 및 받기 전자 메일로**이동 합니다.
  
![이 보고서를 보려면 보안 &amp; 준수 센터에서 보고서 \> 대시보드 \> 보냄/받은 전자 메일로 이동 합니다.](media/0e710ed0-1b0e-4dac-8796-94a01a710f3a.png)
  
차트에서 특정 날짜를 가리키면 메시지 수와 해당 메시지가 분류 되는 방식을 볼 수 있습니다. 예를 들어 맬웨어가 있는 것으로 검색 된 메시지의 수와 스팸으로 식별 된 횟수를 확인할 수 있습니다.
  
보고서를 클릭 하거나 탭 하 여 새 브라우저 창에서 보고서를 열 수 있습니다.
  
**아래로 나누기** 목록을 사용 하 여 유형별로 정보를 보거나 방향 (수신 및 송신)을 기준으로 볼 수 있습니다. 
  
![문자 또는 방향에 따라 정보를 보려면 아래로 나누기 목록을 사용 합니다.](media/a5b30c94-d75f-4bfc-851a-cb155685b177.png)
  
차트 아래에는 **GoodMail**, **spamcontentfiltered**등의 전자 메일 범주 목록이 표시 됩니다. 맬웨어에 대해 수행 된 작업과 같은 추가 정보와 전자 메일이 들어오거나 나가는 지를 보려면 범주를 선택 합니다.
  
![이 보고서는 맬웨어 방지, 스팸 방지 및 기타 메시지 감지에 대해 알려줍니다.](media/9ea4b606-f27a-46ee-97a7-be018e2b839c.png)
  
## <a name="user-reported-messages-report"></a>사용자가 보고 한 메시지 보고서

**사용자가 보고 한 메시지** 보고서에는 사용자가 [보고서 메시지 추가 기능](enable-the-report-message-add-in.md)을 사용 하 여 정크 메일, 피싱 시도 또는 좋은 메일로 보고 한 전자 메일 메시지에 대 한 정보가 표시 됩니다.
  
각 메시지에 대 한 자세한 내용은 스팸 정책 예외 또는 조직에 대해 구성 된 메일 흐름 규칙과 같은 배달 이유를 포함 합니다. 세부 정보를 보려면 사용자-보고서 목록에서 항목을 선택한 다음 **요약** 및 **세부 정보** 탭에서 해당 정보를 확인 합니다. 
  
![사용자가 보고 한 메시지 보고서에는 사용자가 정크로 레이블이 지정 된 메시지, 정크 메일, 피싱 시도 등이 표시 됩니다.](media/ad5e9a3d-b833-419c-bcc9-3425d9604ead.png)
  
이 보고서를 보려면 [ &amp; 보안 및 준수 센터](https://protection.office.com)에서 다음 중 하나를 수행 합니다.
  
- **위협 관리** \> **대시보드** \> **사용자가 보고 한 메시지로**이동 합니다.
    
- **위협 관리** \> 로 이동 하 여 **사용자가 보고 한 메시지**를 **검토** \> 합니다.
    
![보안 &amp; 및 준수 센터에서 위협 관리 \> 검토 \> 사용자가 보고 한 메시지를 선택 합니다.](media/e372c57c-1414-4616-957b-bc933b8c8711.png)
  
> [!IMPORTANT]
> 사용자가 보고 한 메시지 보고서가 제대로 작동 하도록 하려면 Office 365 환경에 대해 **감사 로깅을 켜야 합니다** . 이 작업은 일반적으로 Exchange Online에서 감사 로그 역할이 할당 된 사용자가 수행 합니다. 자세한 내용은 [Turn Office 365 감사 로그 검색 켜기 또는 끄기를](turn-audit-log-search-on-or-off.md)참조 하세요. 
  
## <a name="what-permissions-are-needed-to-view-these-reports"></a>이러한 보고서를 표시 하는 데 필요한 사용 권한은 무엇입니까?

이 문서에서 설명 하는 보고서를 보고 사용 하려면 **보안 &amp; 및 준수 센터와 Exchange 관리 센터 둘 다에 대해 적절 한 역할이 할당 되어 있어야 합니다**.

- 보안 &amp; 및 준수 센터에는 다음 역할 중 하나가 할당 되어 있어야 합니다.
    - 조직 관리
    - 보안 관리자 (Azure Active Directory 관리 센터에서 할당할 수 있음[https://aad.portal.azure.com](https://aad.portal.azure.com))
    - 보안 독자

- exchange online의 경우 exchange 관리 센터 ([https://outlook.office365.com/ecp](https://outlook.office365.com/ecp)) 또는 PowerShell cmdlet ( [exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/exchange-online-powershell?view=exchange-ps)참조)에서 다음 역할 중 하나를 할당 받아야 합니다.
    - 조직 관리
    - 보기 전용 조직 관리
    - 보기 권한만 있는 받는 사람 역할
    - 준수 관리

자세한 내용은 다음 리소스를 참조 하십시오.

- [Office 365 보안 &amp; 및 준수 센터의 사용 권한](permissions-in-the-security-and-compliance-center.md)

- [Exchange Online의 기능 사용 권한](https://docs.microsoft.com/exchange/permissions-exo/feature-permissions)
   
   
## <a name="what-if-the-reports-arent-showing-data"></a>보고서에 데이터가 표시 되지 않으면 어떻게 하나요?

보고서에 데이터가 표시 되지 않는 경우 정책이 올바르게 설정 되어 있는지 다시 확인 합니다. 자세한 내용은 [Office 365의 스팸 방지 및 맬웨어 방지 보호](anti-spam-and-anti-malware-protection.md)를 참조 하세요.
  
## <a name="related-topics"></a>관련 항목

[Office 365 이메일 스팸 방지 보호](anti-spam-protection.md)
  
[Office 365 보안 &amp; 및 준수 센터의 보고서 및 정보](reports-and-insights-in-security-and-compliance.md)
  
[보안 &amp; 및 준수 센터에서 보고서 일정 만들기](create-a-schedule-for-a-report.md)
  
[보안 &amp; 및 준수 센터에서 사용자 지정 보고서 설정 및 다운로드](set-up-and-download-a-custom-report.md)
  

