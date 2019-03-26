---
title: 보안 &amp; 및 준수 센터에서 위협 탐색기 사용
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 03/21/2019
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 82ac9922-939c-41be-9c8a-7c75b0a4e27d
ms.collection:
- M365-security-compliance
description: 보안 &amp; 및 준수 센터의 Explorer (위협 탐색기 라고도 함)에 대해 알아봅니다.
ms.openlocfilehash: 202898873bb9611c747aed335d295c749c7cd0fa
ms.sourcegitcommit: a56128c7be5d59e976851c27301031e19fa1997d
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/21/2019
ms.locfileid: "30732261"
---
# <a name="use-threat-explorer-in-the-security-amp-compliance-center"></a>보안 &amp; 및 준수 센터에서 위협 탐색기 사용

조직에 [Office 365 Advanced Threat Protection 계획 2](office-365-ti.md)가 있고 필요한 사용 권한이 있는 경우 위협 탐색기를 사용 하 여 위협을 식별 하 고 분석할 수 있습니다. 예를 들어 배달 된 악성 전자 메일을 식별 하 고 삭제할 수 있으며, Office 365 보안 기능으로 인해 발견 된 맬웨어를 볼 수도 있습니다. 위협 탐색기 (탐색기 라고도 함)는 보안 운영 팀에서 보안 &amp; 및 준수 센터의 위협에 대해 조사 하 고 대응 하는 데 도움이 되는 강력한 거의 실시간 도구입니다.
  
![위협 관리 \> 탐색기로 이동](media/cab32fa2-66f1-4ad5-bc1d-2bac4dbeb48c.png)
  
Explorer를 &amp; 사용 하려면 보안 및 준수 센터에서 **위협 관리** \> **탐색기**로 이동 합니다.

> [!IMPORTANT]
> office 365 위협 인텔리전스는 이제 추가 위협 방지 기능과 함께 office 365 Advanced Threat protection 계획 2를 제공 합니다. 자세한 내용은 [office 365 advanced threat protection 요금제 및 가격](https://products.office.com/exchange/advance-threat-protection) 및 [office 365 advanced threat protection 서비스 설명을](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description)참조 하세요.
      
## <a name="explorer-overview"></a>탐색기 개요

조직에 [Office 365 위협 조사 및 응답 기능이](office-365-ti.md) 있고 (ATP 계획 2에 포함 되어 있음) 필요한 권한이 있는 경우 위협 탐색기 (탐색기 라고도 함)를 사용 하 여 위협을 식별 하 고 분석할 수 있습니다. 보안 &amp; 및 준수 센터에서 **위협 관리** \> **탐색기**로 이동 합니다.

![위협 관리 \> 탐색기로 이동](media/cab32fa2-66f1-4ad5-bc1d-2bac4dbeb48c.png)

이 문서에서는 Explorer를 사용 하 여 수행할 수 있는 몇 가지 방법에 대해 설명 합니다 (더 많은 가능성이 있음).

- [전자 메일에서 검색 된 맬웨어 종류](#see-malware-detected-in-email-by-technology)및 위협 보호 기술 (맬웨어 방지 보호, ATP 안전한 첨부 파일 등)을 확인 합니다.

- [피싱 링크 (url)에 대 한 데이터를 보고](#view-data-about-phishing-urls-and-click-verdict), 클릭 verdicts의 용도 (경고 발생 시에는 url 차단, 허용 또는 방문 함)에 대 한 정보

- 정크 메일로 [보고 되거나, 정크 메일 이나 피싱이 아닌](#review-email-messages-reported-by-users)모든 경향을 식별 하 고, 모든 추세 (예: 피싱로 보고 되는 일반적인 메시지 수를 초과 하는 경우)를 확인 합니다. 

## <a name="see-malware-detected-in-email-by-technology"></a>기술 별로 전자 메일에서 발견 된 맬웨어를 참조 하세요.

전자 메일에서 검색 된 맬웨어 및 Office 365의 기술에 대해 확인 하려는 경우를 가정해 보겠습니다. 이 작업을 수행 하려면 [전자 메일 > 맬웨어](threat-explorer-views.md#email--malware) 보기 탐색기를 사용 합니다.

1. [https://protection.office.com](https://protection.office.com)Office 365 Security & 준수 센터 ()에서 **Threat management** > **Explorer**를 선택 합니다.
2. **보기** 메뉴에서 **전자 메일** > **맬웨어**를 선택 합니다.<br/>![탐색기에 대 한 보기 메뉴](media/ExplorerViewEmailMalwareMenu.png)<br/>
3. **보낸 사람**을 클릭 한 다음 **기본** > **검색 기술을**선택 합니다.<br/>이제 검색 기술을 보고서에 대 한 필터로 사용할 수 있습니다.<br/>![맬웨어 검색 기술](media/ExplorerEmailMalwareDetectionTech.png)<br/> 
4. 옵션을 선택한 다음 새로 고침 단추를 클릭 하 여 해당 필터를 적용 합니다.<br/>![선택한 검색 기술](media/ExplorerEmailMalwareDetectionTechATP.png)<br/> 

선택한 기술 옵션을 사용 하 여 전자 메일로 검색 된 결과 맬웨어가 표시 되도록 보고서가 새로 고쳐집니다. 여기서는 추가 분석을 수행할 수 있습니다.

## <a name="view-data-about-phishing-urls-and-click-verdict"></a>피싱 url에 대 한 데이터를 확인 하 고 결과를 클릭 합니다.

허용, 차단 및 재정의 된 url 목록을 비롯 하 여 전자 메일의 url을 통한 피싱 시도를 확인 하려는 경우를 가정해 보겠습니다. 이 작업을 수행 하려면 [전자 메일 > 피싱](threat-explorer-views.md#email--phish) Explorer 보기를 사용 합니다.

1. [https://protection.office.com](https://protection.office.com)Office 365 Security & 준수 센터 ()에서 **Threat management** > **Explorer**를 선택 합니다.
2. **보기** 메뉴에서 **전자 메일** > **피싱**을 선택 합니다.<br/>![탐색기에 대 한 보기 메뉴](media/ExplorerViewEmailPhishMenu.png)<br/>
3. **보낸 사람**을 클릭 한 다음 **url** > 을 선택 합니다**결과를 클릭**합니다.
4. **차단** 됨 및 **무시 된 블록과**같은 옵션을 하나 이상 선택 하 고 **새로 고침** 단추를 클릭 하 여 해당 필터를 적용 합니다.<br/>![url을 선택 하 고 verdicts을 클릭 합니다.](media/ThreatExplorerEmailPhishClickVerdictOptions.png)<br/>

보고서가 새로 고쳐지고 전자 메일 배달 상태와 함께 차단 (또는 경고가 발생 하더라도 방문) 된 전자 메일에 검색 된 피싱 url이 표시 됩니다. 여기서는 추가 분석을 수행할 수 있습니다. 예를 들어 차트 아래에서 조직의 전자 메일에서 차단 된 최상위 url을 볼 수 있습니다. 

![차단 된 탐색기 url](media/ExplorerPhishClickVerdictURLs.png) 

자세한 정보를 보려면 URL을 선택 합니다.

## <a name="review-email-messages-reported-by-users"></a>사용자가 보고 한 전자 메일 메시지 검토

조직의 사용자가 [outlook 및 웹용 outlook에 대 한 보고서 메시지 추가 기능](enable-the-report-message-add-in.md)을 사용 하 여 정크 메일 또는 피싱이 아닌 메시지를 보고 했다고 가정 합니다. 이 작업을 수행 하려면 [전자 메일 > 사용자가 보고](threat-explorer-views.md#email--user-reported) 한 탐색기 보기를 사용 합니다.

1. [https://protection.office.com](https://protection.office.com)Office 365 Security & 준수 센터 ()에서 **Threat management** > **Explorer**를 선택 합니다.
2. **보기** 메뉴에서**사용자가 보고 한** **전자 메일** > 을 선택 합니다.<br/>![탐색기에 대 한 보기 메뉴](media/ExplorerViewMenuEmailUserReported.png)<br/>
3. **보낸 사람**을 클릭 한 다음 **기본** > **보고서 유형을**선택 합니다.
4. **피싱**등의 옵션을 선택 하 고 **새로 고침** 단추를 클릭 합니다. <br/>![사용자가 보고 한 피싱](media/EmailUserReportedReportType.png)<br/> 

보고서가 새로 고쳐지고 조직의 사용자가 피싱 시도로 보고 한 전자 메일 메시지에 대 한 데이터가 표시 됩니다. 이 정보를 사용 하 여 추가 분석을 수행 하 고, 필요한 경우 [ATP 피싱 방지 정책을](set-up-anti-phishing-policies.md)조정할 수 있습니다.

## <a name="theres-more"></a>거기 더 있어!

이 문서에서 설명 하는 세 가지 시나리오 외에도 Explorer에서 사용할 수 있는 보고 시나리오가 많이 있습니다. 몇 가지 추가 예는 다음과 같습니다.

- [배달된 악성 전자 메일 찾기 및 조사](investigate-malicious-email-that-was-delivered.md)

- [SharePoint Online, OneDrive 및 Microsoft 팀에서 검색 된 악의적인 파일 보기](malicious-files-detected-in-spo-odb-or-teams.md)

- [위협 탐색기의 보기에 대 한 개요 가져오기](threat-explorer-views.md)

## <a name="how-to-get-explorer"></a>탐색기를 가져오는 방법

Explorer는 [Office 365 Advanced Threat Protection 계획 2](office-365-ti.md)에 포함 되어 있습니다. 

탐색기를 보고 사용 하려면 보안 관리자 또는 보안 판독기에 부여 된 것과 같은 적절 한 사용 권한이 있어야 합니다. 

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
  
## <a name="related-topics"></a>관련 항목

- [자동 조사 및 대응 (AIR)](automated-investigation-response-office.md)

- [위협 탐색기 보기](threat-explorer-views.md)

- [Office 365 Advanced Threat Protection에 대 한 보고서 보기](view-reports-for-atp.md)
