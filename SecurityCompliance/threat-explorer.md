---
title: 위협 탐색기 (및 실시간 검색)
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 06/20/2019
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 82ac9922-939c-41be-9c8a-7c75b0a4e27d
ms.collection:
- M365-security-compliance
description: 보안 &amp; 및 준수 센터의 Explorer (및 실시간 검색)에 대해 알아봅니다.
ms.openlocfilehash: 3d2eab30b97655b692ed1bfe089b6a79834fd110
ms.sourcegitcommit: 011bfa60cafdf47900aadf96a17eb275efa877c4
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/29/2019
ms.locfileid: "35394353"
---
# <a name="threat-explorer-and-real-time-detections"></a>위협 탐색기 (및 실시간 검색)

조직에 [office 365 Advanced Threat Protection](office-365-atp.md) (OFFICE 365 ATP)이 있고 [필요한 사용 권한이](#required-licenses-and-permissions)있는 경우에는 **Explorer** 또는 **실시간** 검색 (이전에는 *실시간 보고서* )을 통해 다음을 [참조 하십시오. 새로운 기능](#new-features-in-real-time-detections)! 보안 & 준수 센터에서 **위협 관리**로 이동한 다음 **Explorer** 또는 **실시간**검색을 선택 합니다. 

|ATP 계획 2를 사용 하는 경우 다음을 확인할 수 있습니다.  |ATP 계획 1을 사용 하는 경우 다음을 확인할 수 있습니다.  |
|---------|---------|
|![위협 탐색기](media/threatmgmt-explorer.png)      |![실시간 검색](media/threatmgmt-realtimedetections.png)         |

Explorer (또는 실시간 검색)를 사용 하는 경우 보안 운영 팀이 효과적이 고 효율적으로 위협을 조사 하 고 대응 하는 데 사용할 수 있는 강력한 보고서가 있으며 다음과 같은 이미지와 비슷합니다. 

![위협 관리 \> 탐색기로 이동](media/cab32fa2-66f1-4ad5-bc1d-2bac4dbeb48c.png)

이 보고서를 사용 하 여 다음을 수행할 수 있습니다.
- [Office 365 보안 기능으로 검색 된 맬웨어를 참조 하세요.](#see-malware-detected-in-email-by-technology)
- [피싱 Url에 대 한 데이터를 확인 하 고 결과를 클릭 합니다.](#view-data-about-phishing-urls-and-click-verdict)
- [탐색기의 보기에서 자동화 된 조사 및 응답 프로세스 시작](#start-automated-investigation-and-response) (ATP 요금제 2에만 해당)
- ... [악성 전자 메일을 조사 하 고 더 많은 방법을 확인해](#more-ways-to-use-explorer-or-real-time-detections)보세요.

## <a name="new-features-in-real-time-detections"></a>실시간 검색의 새로운 기능

Explorer/실시간 검색에서는 전자 메일이 있는 위치를 보다 완전 하 게 보여 주도록 디자인 된 새 필드를 새로 추가 합니다. 이러한 변경 목표의 일환으로는 보안 Ops 사용자에 게 더 쉽게 사냥을 사용할 수 있지만,이는 네트워크 결과에서 문제 전자 메일의 위치를 한눈에 파악 하는 것입니다.

어떤 작업을 수행 하나요? 배달 상태는 이제 다음과 같은 두 개의 열로 나뉩니다.

- 배달 작업-이 전자 메일의 상태는 무엇입니까?
- 배달 위치-이 전자 메일의 경로가 어떻게 설정 되었습니까?

배달 작업은 기존 정책 또는 검색으로 인해 전자 메일에 대해 수행 되는 작업입니다. 다음은 전자 메일에 사용할 수 있는 작업입니다.

|배달  |Junked  |수준  |바뀌면  |
|---------|---------|---------|---------|
|전자 메일이 사용자의 받은 편지함 또는 폴더에 배달 되었으며 사용자가 직접 액세스할 수 있습니다.    | 사용자의 정크 폴더 또는 삭제 된 폴더에 전자 메일이 전송 되 고 해당 폴더의 전자 메일에 대 한 액세스 권한이 사용자에 게 있습니다.       | 격리 되거나, 실패 했거나, 삭제 된 전자 메일입니다. 사용자가이를 완전히 액세스할 수 없습니다.     | 첨부 파일이 악성 인 .txt 파일로 악의적 첨부 파일이 교체 되는 모든 전자 메일     |

다음은 사용자가 볼 수 있는 것과 그렇지 않은 항목입니다.

|최종 사용자가 액세스할 수 있음  |최종 사용자가 액세스할 수 없음  |
|---------|---------|
|배달     | 수준        |
|Junked     | 바뀌면        |

배달 위치는 배달 후 실행 되는 정책 및 검색의 결과를 표시 합니다. 배달 작업에 연결 됩니다. 이 필드는 문제 메일을 찾은 경우 수행 되는 작업에 대 한 통찰력을 제공 하기 위해 추가 되었습니다. 다음은 배달 위치의 possilbe 값입니다.

1. 받은 편지함 또는 폴더-전자 메일이 받은 편지함 또는 폴더 (전자 메일 규칙에 따라 다름)에 있습니다.
2. 온-프레미스 또는 external-사서함이 클라우드에는 없지만 온-프레미스에 있는 경우
3. 정크 폴더-사용자의 정크 폴더에 있는 전자 메일입니다.
4. 지운 편지함 폴더-사용자의 지운 편지함 폴더에 있는 전자 메일입니다.
5. 격리-전자 메일을 격리 하 고 사용자의 사서함에 있지 않습니다.
6. Failed – 전자 메일이 사서함에 연결 하지 못했습니다.
7. 삭제 됨-전자 메일이 메일 흐름의 어딘가에 손실 됩니다.

## <a name="see-malware-detected-in-email-by-technology"></a>기술 별로 전자 메일에서 발견 된 맬웨어를 참조 하세요.

Office 365 기술을 통해 전자 메일로 검색 된 맬웨어를 확인 하려는 경우를 가정해 보겠습니다. 이 작업을 수행 하려면 [전자 메일 > 맬웨어](threat-explorer-views.md#email--malware) 보기 Explorer (또는 실시간 검색)를 사용 합니다.

1. 보안 &[https://protection.office.com](https://protection.office.com)준수 센터 ()에서 **Threat management** > **Explorer** (또는 **실시간**검색)를 선택 합니다. (이 예제에서는 탐색기를 사용 합니다.)

2. **보기** 메뉴에서 **전자 메일** > **맬웨어**를 선택 합니다.<br/>![탐색기에 대 한 보기 메뉴](media/ExplorerViewEmailMalwareMenu.png)<br/>

3. **보낸 사람**을 클릭 한 다음 **기본** > **검색 기술을**선택 합니다.<br/>이제 검색 기술을 보고서에 대 한 필터로 사용할 수 있습니다.<br/>![맬웨어 검색 기술](media/ExplorerEmailMalwareDetectionTech.png)<br/> 

4. 옵션을 선택한 다음 **새로 고침** 단추를 클릭 하 여 해당 필터를 적용 합니다.<br/>![선택한 검색 기술](media/ExplorerEmailMalwareDetectionTechATP.png)<br/> 

선택한 기술 옵션을 사용 하 여 전자 메일로 검색 된 결과 맬웨어가 표시 되도록 보고서가 새로 고쳐집니다. 여기서는 추가 분석을 수행할 수 있습니다.

## <a name="view-data-about-phishing-urls-and-click-verdict"></a>피싱 Url에 대 한 데이터를 확인 하 고 결과를 클릭 합니다.

허용, 차단 및 재정의 된 Url 목록을 비롯 하 여 전자 메일의 Url을 통한 피싱 시도를 확인 하려는 경우를 가정해 봅니다. 클릭 한 Url을 식별 하려면 [ATP 안전한 링크](atp-safe-links.md) 를 구성 해야 합니다. 클릭 verdicts 보호 및 로깅에 대 한 [Atp Safe links 정책이](set-up-atp-safe-links-policies.md) 설정 되었는지 확인 합니다. Atp safe 링크를 클릭 합니다. 

메시지에서 피싱 Url을 검토 하 고 피싱 메시지의 Url을 클릭 하려면 [전자 메일 > 피싱](threat-explorer-views.md#email--phish) Explorer 보기 (실시간 검색)를 사용 합니다.

1. 보안 &[https://protection.office.com](https://protection.office.com)준수 센터 ()에서 **Threat management** > **Explorer** (또는 **실시간**검색)를 선택 합니다. (이 예제에서는 탐색기를 사용 합니다.)

2. **보기** 메뉴에서 **전자 메일** > **피싱**을 선택 합니다.<br/>![탐색기에 대 한 보기 메뉴](media/ExplorerViewEmailPhishMenu.png)<br/>

3. **보낸 사람**을 클릭 한 다음 **url** > 을 선택 합니다**결과를 클릭**합니다.

4. **차단** 됨 및 **무시 된 블록과**같은 옵션을 하나 이상 선택 하 고 해당 필터를 적용 하는 옵션과 같은 줄에 있는 **새로 고침** 단추를 클릭 합니다. (브라우저 창을 새로 고치지 않습니다.)<br/>![Url을 선택 하 고 verdicts을 클릭 합니다.](media/ThreatExplorerEmailPhishClickVerdictOptions.png)<br/>

    보고서를 새로 고치면 보고서 아래의 URL 탭에 서로 다른 두 개의 URL 테이블이 표시 됩니다.

   1. **상위 url** 은 필터링 된 메시지에 포함 된 url 및 각 URL에 대 한 전자 메일 배달 작업 수입니다. 피싱 전자 메일 보기에서 일반적으로이 목록에는 합법적인 Url이 포함 됩니다. 공격자는 메시지에 효과적이 고 잘못 된 Url을 함께 사용 하 여 배달 하려고 할 수 있지만, 사용자가 클릭 하는 데 더 흥미로운 악성 링크를 만들 수 있습니다. Url의 테이블은 총 전자 메일 수를 기준으로 정렬 됩니다 (참고:이 열은 보기를 단순하게 하기 위해 표시 되지 않음).

   2. **위쪽** 클릭은 클릭 한 안전한 링크 래핑된 url이 총 클릭 횟수에 따라 정렬 되며 보기를 단순화 하기 위해이 열도 표시 되지 않습니다. 총 개수 열에서 안전한 링크를 나타냅니다. 클릭 한 각 URL에 대해 결과 count를 클릭 합니다. 피싱 email (전자 메일 보기)에서 이러한 메시지는 일반적으로 의심 되거나 악성 Url 이지만 피싱 메시지가 있는 깨끗 한 Url을 포함할 수 있습니다. 래핑 해제 한 링크의 URL 클릭은 여기에 표시 되지 않습니다.
   
   두 개의 Url 테이블에는 배달 작업 및 위치로 피싱 전자 메일의 상위 Url이 표시 되며, 사용자가 잘못 된 링크를 받아 사용자가 상호 작용 한 잠재적 문제를 파악할 수 있는 URL 클릭이 표시 됩니다 (또는 경고와 상관 없이 방문 됨). 여기서는 추가 분석을 수행할 수 있습니다. 예를 들어 차트 아래에서 조직의 환경에서 차단 된 전자 메일의 상위 Url을 볼 수 있습니다.
   
   ![차단 된 탐색기 Url](media/ExplorerPhishClickVerdictURLs.png)
   
   자세한 정보를 보려면 URL을 선택 합니다. URL 플라이 아웃 대화 상자에서 전자 메일에 대 한 필터링이 제거 되어 사용자 환경에 표시 되는 URL의 전체 보기를 보여 줍니다. 이를 통해 탐색기의 전자 메일을 관심 있는 항목으로 필터링 하 고, 잠재적인 위협이 되는 특정 Url을 찾은 다음, url 정보 대화 상자를 통해 해당 환경의 URL 노출에 대 한 이해를 확장 하 여 url 필터를 탐색기 보기 자체

## <a name="review-email-messages-reported-by-users"></a>사용자가 보고 한 전자 메일 메시지 검토

조직의 사용자가 [outlook 및 웹용 outlook에 대 한 보고서 메시지 추가 기능](enable-the-report-message-add-in.md)을 사용 하 여 정크 메일 또는 피싱이 아닌 메시지를 보고 한다고 가정 합니다. 이 작업을 수행 하려면 [전자 메일 > 사용자가 보고](threat-explorer-views.md#email--user-reported) 한 탐색기 보기 (실시간 검색)를 사용 합니다.

1. 보안 &[https://protection.office.com](https://protection.office.com)준수 센터 ()에서 **Threat management** > **Explorer** (또는 **실시간**검색)를 선택 합니다. (이 예제에서는 탐색기를 사용 합니다.)

2. **보기** 메뉴에서**사용자가 보고 한** **전자 메일** > 을 선택 합니다.<br/>![탐색기에 대 한 보기 메뉴](media/ExplorerViewMenuEmailUserReported.png)<br/>

3. **보낸 사람**을 클릭 한 다음 **기본** > **보고서 유형을**선택 합니다.

4. **피싱**등의 옵션을 선택 하 고 **새로 고침** 단추를 클릭 합니다. <br/>![사용자가 보고 한 피싱](media/EmailUserReportedReportType.png)<br/> 

보고서가 새로 고쳐지고 조직의 사용자가 피싱 시도로 보고 한 전자 메일 메시지에 대 한 데이터가 표시 됩니다. 이 정보를 사용 하 여 추가 분석을 수행 하 고, 필요한 경우 [ATP 피싱 방지 정책을](set-up-anti-phishing-policies.md)조정할 수 있습니다.

## <a name="start-automated-investigation-and-response"></a>자동 조사 및 응답 시작

> [!NOTE]
> 자동화 된 조사 및 응답 기능은 **office 365 ATP 계획 2** 및 **Office 365 E5**에서 사용할 수 있습니다.

(새로운 방법!) [자동화 된 조사 및 응답](automated-investigation-response-office.md) 은 사이버 공격을 조사 하 고 완화 하는 과정에서 보안 운영 팀을 훨씬 더 많은 시간과 노력으로 절감할 수 있습니다. 보안 playbook 트리거될 수 있는 알림을 구성 하는 것 외에도 탐색기의 보기에서 자동화 된 조사 및 응답 프로세스를 시작할 수 있습니다. 

이에 대 한 자세한 내용은 [예제: 보안 관리자가 탐색기에서 조사를 트리거하는 예](automated-investigation-response-office.md#example-a-security-administrator-triggers-an-investigation-from-threat-explorer)를 참조 하십시오.

## <a name="more-ways-to-use-explorer-or-real-time-detections"></a>Explorer (또는 실시간 검색)를 사용 하는 여러 방법

이 문서에서 설명 하는 시나리오 외에도 Explorer (또는 실시간 검색)에서 사용할 수 있는 보고 옵션이 더 많이 있습니다. 
- [배달된 악성 전자 메일 찾기 및 조사](investigate-malicious-email-that-was-delivered.md)
- [SharePoint Online, OneDrive 및 Microsoft 팀에서 검색 된 악의적인 파일 보기](malicious-files-detected-in-spo-odb-or-teams.md)
- [위협 탐색기 및 실시간 검색의 보기에 대 한 개요 보기](threat-explorer-views.md)

## <a name="required-licenses-and-permissions"></a>필요한 라이선스 및 사용 권한

Explorer 또는 실시간 검색을 하려면 [Office 365 ATP](office-365-atp.md) 가 있어야 합니다.
- Explorer는 Office 365 ATP 계획 2에 포함 되어 있습니다. 
- 실시간 검색 보고서는 Office 365 ATP 계획 1에 포함 되어 있습니다.
- ATP가 보호 해야 하는 모든 사용자에 대해 라이선스를 할당 하도록 계획 합니다. (Explorer 또는 실시간 검색은 사용이 허가 된 사용자에 대 한 검사 데이터를 표시 합니다.)

탐색기 또는 실시간 검색을 보고 사용 하려면 보안 관리자 또는 보안 판독기에 부여 된 것과 같은 적절 한 사용 권한이 있어야 합니다. 

- 보안 &amp; 및 준수 센터에는 다음 역할 중 하나가 할당 되어 있어야 합니다.
    - 조직 관리
    - 보안 관리자 (Azure Active Directory 관리 센터[https://aad.portal.azure.com](https://aad.portal.azure.com)에서 할당할 수 있음)
    - 보안 독자

- Exchange Online의 경우 Exchange 관리 센터 ([https://outlook.office365.com/ecp](https://outlook.office365.com/ecp)) 또는 PowerShell Cmdlet ( [Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/exchange-online-powershell?view=exchange-ps)참조)에서 다음 역할 중 하나를 할당 받아야 합니다.
    - 조직 관리
    - 보기 전용 조직 관리
    - 보기 권한만 있는 받는 사람 역할
    - 준수 관리

역할 및 사용 권한에 대 한 자세한 내용은 다음 리소스를 참조 하십시오.

- [Permissions in the Office 365 Security &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md)
- [Exchange Online의 기능 사용 권한](https://docs.microsoft.com/exchange/permissions-exo/feature-permissions)
  
