---
title: 보안 &amp; 및 준수 센터에서 위협 탐색기 사용
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 03/31/2019
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
ms.openlocfilehash: c782e5962164b7d35947befe526c20f7dc0943d5
ms.sourcegitcommit: 691370682825a7601bd4b77d0a8c4b51ed15682f
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/31/2019
ms.locfileid: "31014017"
---
# <a name="use-threat-explorer-in-the-security-amp-compliance-center"></a>보안 &amp; 및 준수 센터에서 위협 탐색기 사용

조직에 [Office 365 Advanced threat Protection 계획 2](office-365-ti.md) (ATP)가 있고 필요한 사용 권한이 있는 경우 위협 탐색기 (탐색기 라고도 함)를 사용 하 여 위협을 식별 하 고 분석할 수 있습니다. &amp; (Explorer를 사용 하려면 보안 및 준수 센터에서 **위협 관리** \> **탐색기**로 이동 합니다.)

![위협 관리 \> 탐색기로 이동](media/cab32fa2-66f1-4ad5-bc1d-2bac4dbeb48c.png)

Explorer는 보안 운영 팀에서 보안 &amp; 및 준수 센터의 위협에 대해 조사 하 고 대응 하는 데 도움을 주는 강력 하 고도 비슷한 실시간 도구입니다. 수행할 수 있는 작업은 다음과 같습니다.
- [Office 365 보안 기능에서 검색 된 맬웨어를 참조 하세요.](#see-malware-detected-in-email-by-technology)
- [피싱 url에 대 한 데이터를 확인 하 고 결과를 클릭 합니다.](#view-data-about-phishing-urls-and-click-verdict)
- [탐색기의 보기에서 자동화 된 조사 및 응답 프로세스 시작](#start-automated-investigation-and-response)
- ... [더 많은 내용을](#more-ways-to-use-explorer)확인해 보세요.

## <a name="see-malware-detected-in-email-by-technology"></a>기술 별로 전자 메일에서 발견 된 맬웨어를 참조 하세요.

전자 메일에서 검색 된 맬웨어 및 Office 365의 기술에 대해 확인 하려는 경우를 가정해 보겠습니다. 이 작업을 수행 하려면 [전자 메일 > 맬웨어](threat-explorer-views.md#email--malware) 보기 탐색기를 사용 합니다.

1. [https://protection.office.com](https://protection.office.com)Security & 준수 센터 ()에서 **Threat management** > **Explorer**를 선택 합니다.
2. **보기** 메뉴에서 **전자 메일** > **맬웨어**를 선택 합니다.<br/>![탐색기에 대 한 보기 메뉴](media/ExplorerViewEmailMalwareMenu.png)<br/>
3. **보낸 사람**을 클릭 한 다음 **기본** > **검색 기술을**선택 합니다.<br/>이제 검색 기술을 보고서에 대 한 필터로 사용할 수 있습니다.<br/>![맬웨어 검색 기술](media/ExplorerEmailMalwareDetectionTech.png)<br/> 
4. 옵션을 선택한 다음 새로 고침 단추를 클릭 하 여 해당 필터를 적용 합니다.<br/>![선택한 검색 기술](media/ExplorerEmailMalwareDetectionTechATP.png)<br/> 

선택한 기술 옵션을 사용 하 여 전자 메일로 검색 된 결과 맬웨어가 표시 되도록 보고서가 새로 고쳐집니다. 여기서는 추가 분석을 수행할 수 있습니다.

## <a name="view-data-about-phishing-urls-and-click-verdict"></a>피싱 url에 대 한 데이터를 확인 하 고 결과를 클릭 합니다.

허용, 차단 및 재정의 된 url 목록을 비롯 하 여 전자 메일의 url을 통한 피싱 시도를 확인 하려는 경우를 가정해 보겠습니다.  클릭 한 url을 식별 하려면 [ATP Safe 링크가](atp-safe-links.md)필요 합니다. (atp 안전한 링크를 클릭 하 여 verdicts에 대 한 클릭 시 보호 및 로깅을 위해 사용자에 게 [atp 안전한 링크 정책을](set-up-atp-safe-links-policies.md) 설정 하 고 적용 했는지 확인 합니다.) 메시지에서 피싱 url을 검토 하 고 피싱 메시지의 url을 클릭 하려면 Explorer의 [전자 메일 > 피싱](threat-explorer-views.md#email--phish) 보기를 사용 합니다.

1. [https://protection.office.com](https://protection.office.com)Security & 준수 센터 ()에서 **Threat management** > **Explorer**를 선택 합니다.
2. **보기** 메뉴에서 **전자 메일** > **피싱**을 선택 합니다.<br/>![탐색기에 대 한 보기 메뉴](media/ExplorerViewEmailPhishMenu.png)<br/>
3. **보낸 사람**을 클릭 한 다음 **url** > 을 선택 합니다**결과를 클릭**합니다.
4. **차단** 됨 및 **무시 된 블록과**같은 옵션을 하나 이상 선택 하 고 **새로 고침** 단추를 클릭 하 여 해당 필터를 적용 합니다.<br/>![url을 선택 하 고 verdicts을 클릭 합니다.](media/ThreatExplorerEmailPhishClickVerdictOptions.png)<br/>

보고서가 새로 고쳐지고 아래 url 탭에 서로 다른 두 개의 URL 테이블이 표시 됩니다.
1. **상위 url** 은 필터링 된 메시지에 포함 된 url 및 각 URL에 대 한 전자 메일 배달 작업 수입니다. 피싱 전자 메일 보기에서 일반적으로이 목록에는 합법적인 url이 포함 됩니다. 공격자는 메시지에 효과적이 고 잘못 된 url을 함께 사용 하 여 배달 하려고 할 수 있지만, 사용자가 클릭 하는 데 더 흥미로운 악성 링크를 만들 수 있습니다. url의 테이블은 총 전자 메일 수를 기준으로 정렬 됩니다 (참고:이 열은 보기를 단순하게 하기 위해 표시 되지 않음).
2. **위쪽** 클릭은 클릭 한 안전한 링크 래핑된 url이 총 클릭 횟수에 따라 정렬 되며 보기를 단순화 하기 위해이 열도 표시 되지 않습니다. 총 개수 열에서 안전한 링크를 나타냅니다. 클릭 한 각 URL에 대해 결과 count를 클릭 합니다. 피싱 전자 메일 보기에서는 이러한 연결이 의심 스 럽 거 나 악성 링크 이지만 피싱 메시지에 있는 깨끗 한 url을 포함할 수 있습니다. 래핑 해제 한 링크의 URL 클릭은 여기에 표시 되지 않습니다.

두 개의 url 테이블에는 배달 상태별 피싱 전자 메일의 상위 url이 표시 되 고, 사용자가 잘못 된 링크를 받아 사용자가 상호 작용 한 잠재적 링크가 무엇 인지 이해할 수 있도록 차단 된 (또는 경고에 따라 방문) url 클릭이 표시 됩니다. 여기서는 추가 분석을 수행할 수 있습니다. 예를 들어 차트 아래에서 조직의 환경에서 차단 된 전자 메일의 상위 url을 볼 수 있습니다. 

![차단 된 탐색기 url](media/ExplorerPhishClickVerdictURLs.png) 

자세한 정보를 보려면 URL을 선택 합니다. url 플라이 아웃 대화 상자에서 사용자 환경에 표시 되는 url의 전체 보기를 보여 주기 위해 전자 메일에 대 한 필터링이 제거 됩니다. 이를 통해 탐색기의 전자 메일을 관심 있는 항목으로 필터링 하 고, 잠재적인 위협이 되는 특정 url을 찾은 다음, url 정보 대화 상자를 통해 해당 환경의 url 노출에 대 한 이해를 확장 하 여 url 필터를 탐색기 보기 자체

## <a name="review-email-messages-reported-by-users"></a>사용자가 보고 한 전자 메일 메시지 검토

조직의 사용자가 [outlook 및 웹용 outlook에 대 한 보고서 메시지 추가 기능](enable-the-report-message-add-in.md)을 사용 하 여 정크 메일 또는 피싱이 아닌 메시지를 보고 했다고 가정 합니다. 이 작업을 수행 하려면 [전자 메일 > 사용자가 보고](threat-explorer-views.md#email--user-reported) 한 탐색기 보기를 사용 합니다.

1. [https://protection.office.com](https://protection.office.com)Security & 준수 센터 ()에서 **Threat management** > **Explorer**를 선택 합니다.
2. **보기** 메뉴에서**사용자가 보고 한** **전자 메일** > 을 선택 합니다.<br/>![탐색기에 대 한 보기 메뉴](media/ExplorerViewMenuEmailUserReported.png)<br/>
3. **보낸 사람**을 클릭 한 다음 **기본** > **보고서 유형을**선택 합니다.
4. **피싱**등의 옵션을 선택 하 고 **새로 고침** 단추를 클릭 합니다. <br/>![사용자가 보고 한 피싱](media/EmailUserReportedReportType.png)<br/> 

보고서가 새로 고쳐지고 조직의 사용자가 피싱 시도로 보고 한 전자 메일 메시지에 대 한 데이터가 표시 됩니다. 이 정보를 사용 하 여 추가 분석을 수행 하 고, 필요한 경우 [ATP 피싱 방지 정책을](set-up-anti-phishing-policies.md)조정할 수 있습니다.

## <a name="start-automated-investigation-and-response"></a>자동 조사 및 응답 시작

(새로운 방법!) 최근 ATP 계획 2에 추가 된 [자동화 된 조사 및 응답](automated-investigation-response-office.md)은 사이버 공격을 조사 하 고 완화 하는 데 많은 시간과 노력을 기울여야 합니다. 보안 playbook 트리거될 수 있는 알림을 구성 하는 것 외에도 탐색기의 보기에서 자동화 된 조사 및 응답 프로세스를 시작할 수 있습니다. 

이에 대 한 자세한 내용은 [예제: 보안 관리자가 위협 탐색기에서 조사를 트리거하](automated-investigation-response-office.md#example-a-security-administrator-triggers-an-investigation-from-threat-explorer)는 방법을 참조 하세요.

## <a name="more-ways-to-use-explorer"></a>탐색기를 사용 하는 다른 방법

이 문서에서 설명 하는 시나리오 외에도 탐색기에서 사용할 수 있는 보고 옵션이 더 많이 있습니다. 
- [배달된 악성 전자 메일 찾기 및 조사](investigate-malicious-email-that-was-delivered.md)
- [SharePoint Online, OneDrive 및 Microsoft 팀에서 검색 된 악의적인 파일 보기](malicious-files-detected-in-spo-odb-or-teams.md)
- [위협 탐색기의 보기에 대 한 개요 가져오기](threat-explorer-views.md)

## <a name="required-licenses-and-permissions"></a>필요한 라이선스 및 사용 권한

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

역할 및 사용 권한에 대 한 자세한 내용은 다음 리소스를 참조 하십시오.

- [Permissions in the Office 365 Security &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md)

- [Exchange Online의 기능 사용 권한](https://docs.microsoft.com/exchange/permissions-exo/feature-permissions)
  
