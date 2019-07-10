---
title: 위협 탐색기 및 실시간 검색의 보기
ms.author: deniseb
author: denisebmsft
manager: dansimp
ms.date: 03/18/2019
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid: ''
ms.collection:
- M365-security-compliance
description: 위협 탐색기 및 실시간 검색에서 사용할 수 있는 다양 한 종류의 보기에 대해 알아봅니다.
ms.openlocfilehash: 71ec20daae45bee8385f24091850ea6223399eae
ms.sourcegitcommit: 32ecff689ae32c59a39b7633ca0f36a304e7516e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/09/2019
ms.locfileid: "35600821"
---
# <a name="views-in-threat-explorer-and-real-time-detections"></a>위협 탐색기 및 실시간 검색의 보기

![위협 탐색기](media/ThreatExplorerFirstOpened.png)

[위협 탐색기](use-explorer-in-security-and-compliance.md) 실시간 검색 보고서는 보안 운영 팀에서 보안 &amp; 및 준수 센터의 위협에 대해 조사 하 고 대응 하는 데 도움이 되는 강력 하 고도 비슷한 실시간 도구입니다. Explorer (and 실시간 검색 보고서)에는 조직에 대 한 기타 보안 위협 및 위험 뿐 아니라 전자 메일 및 Office 365의 파일에 있는 의심 스러운 맬웨어 및 피싱에 대 한 정보가 표시 됩니다. 

- [Office 365 ATP (Advanced Threat Protection](office-365-atp.md) ) 계획 2가 있는 경우 Explorer를 사용할 수 있습니다.
- Office 365 ATP 계획 1을 사용 하는 경우에는 실시간 검색이 가능 합니다.

Explorer (또는 실시간 검색 보고서)를 처음으로 열면 기본 보기에는 최근 7 일간의 전자 메일 맬웨어 검색이 표시 됩니다. [안전한 링크](atp-safe-links.md)에서 검색 되는 악성 Url, [안전한 첨부 파일](atp-safe-attachments.md)에서 검색 된 악의적인 파일 등의 ATP 검색이이 보고서에 표시 될 수도 있습니다. 평가판 구독을 사용 하는 경우가 아니면이 보고서를 수정 하 여 최근 30 일간의 데이터를 표시할 수 있습니다. 평가판 구독에는 최근 7 일간의 데이터만 포함 됩니다.

표시 되는 정보를 변경 하려면 **보기** 메뉴를 사용 합니다. 도구 설명은 사용할 보기를 결정 하는 데 도움이 됩니다.
  
![위협 탐색기 보기 메뉴](media/ThreatExplorerViewMenu.png)

보기를 선택한 후에는 필터를 적용 하 고 추가 분석을 수행 하도록 쿼리를 설정할 수 있습니다. 다음 섹션에서는 Explorer (또는 실시간 검색)에서 사용할 수 있는 다양 한 보기에 대 한 간략 한 개요를 제공 합니다.  

## <a name="email--malware"></a>전자 메일 > 맬웨어

이 보고서를 보려면 Explorer (또는 실시간 검색)에서**전자 메일** > **맬웨어** **보기** > 를 선택 합니다. 이 보기에는 맬웨어를 포함 하는 것으로 확인 된 전자 메일 메시지에 대 한 정보가 표시 됩니다.  

![맬웨어로 식별 된 전자 메일에 대 한 데이터 보기](media/ExplorerEmailMalwareMenu.png) 

**보낸 사람** 을 클릭 하 여 보기 옵션 목록을 엽니다. 이 목록을 사용 하 여 보낸 사람, 받는 사람, 보낸 사람 도메인, 제목, 검색 기술, 보호 상태 등의 데이터를 볼 수 있습니다. 

예를 들어 검색 된 전자 메일 메시지에서 어떤 작업이 수행 되었는지 확인 하려면 목록에서 **보호 상태** 를 선택 합니다. 옵션을 선택한 다음 새로 고침 단추를 클릭 하 여 보고서에 해당 필터를 적용 합니다.

![위협 탐색기에 대 한 위협 보호 상태 옵션](media/ThreatExplorerProtectionStatusOptions.png)

차트 아래에서 특정 메시지에 대 한 세부 정보를 확인 합니다. 목록에서 항목을 선택 하면 선택한 항목에 대 한 자세한 정보를 볼 수 있는 플라이 아웃 창이 열립니다. 

![플라이 아웃이 열린 위협 탐색기](media/ThreatExplorerMalwareItemSelectedFlyout.png)

## <a name="email--phish"></a>전자 메일 > 피싱

이 보고서를 보려면 Explorer (또는 실시간 검색)에서**전자 메일** > **피싱** **보기** > 를 선택 합니다. 이 보기에는 피싱 시도로 식별 된 전자 메일 메시지가 표시 됩니다.  

![피싱 시도로 식별 된 전자 메일에 대 한 데이터 보기](media/ThreatExplorerEmailPhish.png) 

**보낸 사람** 을 클릭 하 여 보기 옵션 목록을 엽니다. 이 목록을 사용 하 여 보낸 사람, 받는 사람, 보낸 사람 도메인, 보낸 사람 IP, URL 도메인 별로 데이터를 확인 하 고 결과 등을 클릭 합니다. 

예를 들어 사용자가 피싱 시도로 식별 된 Url을 클릭 했을 때 수행한 작업을 확인 하려면 목록에서 **결과 클릭** 을 선택 하 고 옵션을 하나 이상 선택 하 고 새로 고침 단추를 클릭 합니다.

![피싱 보고서에 대 한 결과 옵션을 클릭 합니다.](media/ThreatExplorerEmailPhishClickVerdictOptions.png)

차트 아래에서 특정 메시지, URL 클릭, Url 및 전자 메일 원본에 대 한 세부 정보를 확인 합니다. 

![전자 메일 메시지에서 피싱으로 검색 된 Url](media/ThreatExplorerEmailPhishURLs.png)

검색 된 URL과 같은 목록에서 항목을 선택 하는 경우 선택한 항목에 대 한 자세한 내용을 확인할 수 있는 플라이 아웃 창이 열립니다. 

![검색 된 URL에 대 한 세부 정보](media/ThreatExplorerEmailPhishURLDetails.png)

## <a name="email--user-reported"></a>전자 메일 > 사용자가 보고 됨

이 보고서를 보려면 Explorer (또는 실시간 검색)에서**사용자가 보고**한**전자 메일** >  **보기** > 를 선택 합니다. 이 보기에는 사용자가 정크 메일로 보고 되거나, 정크 메일, 피싱 전자 메일이 표시 됩니다. 

![사용자가 보고 한 전자 메일 메시지](media/ThreatExplorerEmailUserReportedViewOptions.png) 

**보낸 사람** 을 클릭 하 여 보기 옵션 목록을 엽니다. 이 목록을 사용 하 여 보낸 사람, 받는 사람, 보고서 유형 (사용자가 정크 메일 인지, 정크 메일이 아님, 피싱 인지를 결정) 등의 정보를 볼 수 있습니다. 

예를 들어 피싱 시도로 보고 된 전자 메일 메시지에 대 한 정보를 보려면 **Sender** > **Report type**을 클릭 하 고 **피싱**를 선택한 다음 새로 고침 단추를 클릭 합니다.

![보고서 유형 필터를 위해 선택한 피싱](media/ThreatExplorerEmailUserReportedPhishSelected.png)

차트 아래에 있는 특정 전자 메일 메시지에 대 한 세부 정보 (예: 제목 줄, 보낸 사람의 IP 주소, 메시지를 정크로 보고 한 사용자, 정크 메일, 피싱 등)를 자세히 확인 합니다. 

![피싱 시도로 보고 된 메시지](media/ThreatExplorerEmailPhishUserReportedPhishDetails.png)

목록에서 항목을 선택 하 여 추가 세부 정보를 확인 합니다.

## <a name="email--all-email"></a>모든 전자 메일 > 전자 메일

이 보고서를 보려면 탐색기에서**전자** > 메일**모든 메일** **보기** > 를 선택 합니다. 이 보기에는 모든 비 악성 메일 (일반 전자 메일, 스팸 및 대량 메일)과 마찬가지로 피싱 또는 맬웨어로 인 한 악성 전자 메일을 비롯 한 전자 메일 활동의 모든 보기가 표시 됩니다. 

> [!NOTE]
> **너무 많은 데이터를 표시 하는 데**오류가 발생 하는 경우 필터를 추가 하 고 필요한 경우 보고 있는 날짜 범위를 좁힐 수 있습니다. 

필터를 적용 하려면 **보낸 사람**을 선택 하 고 목록에서 항목을 선택한 다음 새로 고침 단추를 클릭 합니다. 이 예제에서는 **검색 기술을** 필터로 사용 했으며 몇 가지 옵션을 사용할 수 있습니다. 보낸 사람, 보낸 사람의 도메인, 받는 사람, 제목, 첨부 파일 이름, 맬웨어 제품군, 보호 상태 (Office 365의 위협 보호 기능 및 정책에 따라 수행 된 작업), 검색 기술 (맬웨어 감지 방법) 및 자세한. 

![검색 기술을 통해 검색 된 전자 메일에 대 한 데이터 보기](media/0c032eb3-6021-4174-9f06-ff8f30c245ca.png) 

차트 아래에 제목 줄, 받는 사람, 보낸 사람, 상태 등의 특정 전자 메일 메시지에 대 한 세부 정보를 확인 합니다. 

## <a name="content--malware"></a>맬웨어 > 콘텐츠

이 보고서를 보려면 Explorer (또는 실시간 검색)에서**콘텐츠** > **맬웨어** **보기** > 를 선택 합니다. 이 보기는 [SharePoint Online, 비즈니스용 OneDrive 및 Microsoft 팀의 Office 365 Advanced Threat Protection에서](atp-for-spo-odb-and-teams.md)악의적으로 식별 된 파일을 보여 줍니다.

맬웨어 제품군, 검색 기술 (맬웨어가 감지 된 방법) 및 작업 (OneDrive, SharePoint 또는 팀)을 통해 정보를 확인 합니다. 

![검색 된 맬웨어에 대 한 데이터 보기](media/d11dc568-b091-4159-b261-df13d76b520b.png)  

차트 아래에서 첨부 파일 이름, 작업, 파일 크기, 파일을 마지막으로 수정한 사용자 등 특정 파일에 대 한 세부 정보를 확인 합니다. 
  
## <a name="click-to-filter-capabilities"></a>간편 필터 기능

탐색기 (및 실시간 검색)를 사용 하 여 클릭 한 번으로 필터를 적용할 수 있습니다. 범례에서 항목을 클릭 하면 해당 항목이 보고서에 대 한 필터가 됩니다. 예를 들어 Explorer에서 맬웨어 보기를 보고 있다고 가정 합니다.
  
![위협 관리 \> 탐색기로 이동](media/cab32fa2-66f1-4ad5-bc1d-2bac4dbeb48c.png)
  
이 차트에서 **ATP 샌드 박싱** 를 클릭 하면 다음과 같은 보기가 만들어집니다. 
  
![ATP 샌드 박싱 결과만 표시 하도록 필터링 된 탐색기](media/7241d7dd-27bc-467d-9db8-6e806c49df14.png)
  
이 보기에서는 [Office 365 ATP 안전한 첨부](atp-safe-attachments.md)파일에서 열 된 파일에 대 한 데이터를 살펴봅니다. 이 차트 아래에서 ATP 안전한 첨부 파일에 의해 검색 된 첨부 파일이 있는 특정 전자 메일 메시지에 대 한 세부 정보를 확인할 수 있습니다.
  
![검색 된 첨부 파일이 있는 전자 메일 메시지에 대 한 구체적인 세부 정보](media/c91fb05c-d1d4-4085-acc6-f7008a415c2a.png)
  
항목을 하나 이상 선택 하면 선택한 항목에 대해 선택할 수 있는 여러 선택 항목이 제공 되는 **작업** 메뉴가 활성화 됩니다. 
  
![항목을 선택 하면 작업 메뉴가 활성화 됩니다.](media/95f127a4-1b2a-4a76-88b9-096e3ba27d1b.png)
  
클릭 하 고 특정 세부 정보로 탐색 하는 기능을 통해 위협을 조사 하는 데 많은 시간을 절약할 수 있습니다.

## <a name="queries-and-filters"></a>쿼리 및 필터

Explorer (및 실시간 검색 보고서)에는 상위 대상 사용자, 최고 맬웨어 제품군, 검색 기술 등의 세부 정보를 확인할 수 있는 몇 가지 강력한 필터 및 쿼리 기능이 있습니다. 각 보고서 종류에서는 다양 한 방식으로 데이터를 보고 탐색할 수 있습니다.

> [!IMPORTANT]
> 검색에 대 한 쿼리 표시줄 (또는 실시간 검색)에 별표 (*) 또는 물음표 (?)와 같은 와일드 카드 문자를 사용 하지 마십시오. 전자 메일 메시지의 제목 필드를 검색 하면 Explorer (또는 실시간 검색)에서 부분 일치를 수행 하 고 와일드 카드 검색과 비슷한 결과를 반환 합니다.
