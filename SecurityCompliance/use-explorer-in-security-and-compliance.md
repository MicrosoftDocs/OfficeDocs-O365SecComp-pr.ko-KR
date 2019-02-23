---
title: 보안 &amp; 및 준수 센터에서 탐색기 사용
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 02/13/2019
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 82ac9922-939c-41be-9c8a-7c75b0a4e27d
ms.collection: M365-security-compliance
description: 보안 &amp; 및 준수 센터의 Explorer (위협 탐색기 라고도 함)에 대해 알아봅니다.
ms.openlocfilehash: 439a7d53e185e12ddd5d2e19b9d88bd8c9b47dad
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30218988"
---
# <a name="use-explorer-in-the-security-amp-compliance-center"></a>보안 &amp; 및 준수 센터에서 탐색기 사용

조직에 [Office 365 위협 인텔리전스](office-365-ti.md)가 있고 필요한 권한이 있는 경우 Explorer를 사용 하 여 위협을 식별 하 고 분석할 수 있습니다. 예를 들어 배달 된 악성 전자 메일을 식별 하 고 삭제할 수 있으며, Office 365 보안 기능으로 인해 발견 된 맬웨어를 볼 수도 있습니다. Explorer (위협 탐색기 라고도 함)는 보안 &amp; 및 준수 센터에서 매우 근접 한 실시간 보고서입니다.
  
![위협 관리 \> 탐색기로 이동](media/cab32fa2-66f1-4ad5-bc1d-2bac4dbeb48c.png)
  
Explorer를 &amp; 사용 하려면 보안 및 준수 센터에서 **위협 관리** \> **탐색기**로 이동 합니다.

> [!IMPORTANT]
> 2019 년 2 월에 시작 해 서 향후 몇 개월 동안 롤아웃 되는 office 365 위협 인텔리전스는 추가 위협 방지 기능을 사용 하 여 office 365 Advanced threat protection 계획 2가 됩니다. 자세한 내용은 [office 365 advanced threat protection 요금제 및 가격](https://products.office.com/exchange/advance-threat-protection) 및 [office 365 advanced threat protection 서비스 설명을](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description)참조 하세요.
      
## <a name="explorer-overview"></a>탐색기 개요

Explorer에는 조직에 대 한 기타 보안 위협 및 위험 뿐 아니라 전자 메일 및 Office 365의 파일에 있는 의심 스러운 악성 프로그램에 대 한 정보가 표시 됩니다. Explorer를 처음 열면 기본 보기의 최근 7 일 동안 바이러스 백신에서 맬웨어가 탐지 된 것을 보여 줍니다. 또한 Explorer는 [안전한 링크](atp-safe-links.md) 및 [안전한 첨부 파일](atp-safe-attachments.md) 을 포함 하 여 Office 365의 보안 보호 기능을 표시할 수 있으며, 이전의 30 일간의 데이터를 표시 하도록 수정할 수 있습니다.
  
![Explorer에는 가장 많이 사용한 맬웨어 및 대상 사용자에 대 한 정보가 표시 됩니다.](media/8e8c1582-d6f4-4521-8591-686a1cb01f7e.png)
  
표시 되는 정보를 변경 하려면 보기 메뉴를 사용 합니다.
  
![탐색기에 대 한 보기 메뉴](media/2bb34f58-555f-4967-ba55-740334ef1f8e.png)
  
Explorer에는 상위 대상 사용자, 최고 맬웨어 제품군 등의 세부 정보를 확인할 수 있는 다양 한 필터링 및 쿼리 기능이 있습니다. 각 보고서 종류에서는 다양 한 방식으로 데이터를 보고 탐색할 수 있습니다.

> [!IMPORTANT]
> 별표 (*) 또는 물음표 (?)와 같은 와일드 카드 문자는 탐색기에서 사용 하지 마십시오. 전자 메일 메시지의 제목 필드를 검색 하면 Explorer는 부분 일치를 수행 하 고 와일드 카드 검색과 비슷한 결과를 반환 합니다.

## <a name="email--malware"></a>전자 \> 메일 맬웨어

이 보기에는 맬웨어를 포함 하는 것으로 확인 된 전자 메일 메시지가 표시 됩니다.  

맬웨어 제품군, 보낸 사람 도메인, 보낸 사람 IP, 보호 상태 (Office 365의 위협 보호 기능 및 정책에 의해 수행 된 작업) 및 검색 기술 (맬웨어 검색 방법)에 따라 차트의 정보를 확인 합니다.  

![검색 된 맬웨어에 대 한 데이터 보기](media/d11dc568-b091-4159-b261-df13d76b520b.png)         

차트 아래에서 주요 맬웨어 패밀리, 상위 대상 사용자 및 특정 메시지에 대 한 세부 정보를 확인할 수 있습니다. 

## <a name="email--phish"></a>전자 \> 메일 피싱

이 보기에는 피싱 시도로 식별 된 전자 메일 메시지가 표시 됩니다.  

보낸 사람 도메인, 보낸 사람 IP 및 보호 상태 (Office 365의 위협 보호 기능 및 정책에 의해 수행 된 작업) 별로 정보를 확인 합니다. 

![피싱 시도로 식별 된 전자 메일에 대 한 데이터 보기](media/2e3f97fa-2b99-47f9-afd6-216d10633c50.png) 

차트 아래에서 특정 메시지에 대 한 세부 정보를 확인 합니다. 

## <a name="email--user-reported"></a>전자 \> 메일 사용자가 보고 됨

이 보기에는 사용자가 정크 메일로 보고 되거나, 정크 메일, 피싱 전자 메일이 표시 됩니다.  

정보 보기 (사용자가 전자 메일을 정크 메일로, 정크 메일이 아님, 또는 피싱를 결정 함), 배달 사유 (스팸 필터 정책, 메일 흐름 규칙, 수신 거부 목록, 수신 허용-보낸 사람 목록 등을 사용 하 여 전자 메일을 특정 위치로 이동 해야 하는 이유) 등)  

![정크 메일로 보고 된 전자 메일 사용자에 대 한 데이터 보기, 정크 메일 또는 피싱 사기](media/255acd04-0d07-4b29-82af-5060a60c20ab.png)  

차트 아래에 있는 특정 전자 메일 메시지에 대 한 세부 정보 (예: 제목 줄, 보낸 사람의 IP 주소, 메시지를 정크로 보고 한 사용자, 정크 메일, 피싱 등)를 자세히 확인 합니다. 

## <a name="email--all-mail"></a>전자 \> 메일 모든 메일

이 보기에는 모든 비 악성 메일 (일반 전자 메일, 스팸 및 대량 메일)과 마찬가지로 피싱 또는 맬웨어로 인 한 악성 전자 메일을 비롯 한 전자 메일 활동의 모든 보기가 표시 됩니다. 

> [!NOTE]
> **너무 많은 데이터를 표시 하는 데**오류가 발생 하는 경우 필터를 추가 하 고 필요한 경우 보고 있는 날짜 범위를 좁힐 수 있습니다. 

필터를 적용 하려면 **보낸 사람**을 선택 하 고 목록에서 항목을 선택한 다음 새로 고침 단추를 클릭 합니다. 이 예제에서는 **검색 기술을** 필터로 사용 했으며 몇 가지 옵션을 사용할 수 있습니다. 보낸 사람, 보낸 사람의 도메인, 받는 사람, 제목, 첨부 파일 이름, 맬웨어 제품군, 보호 상태 (Office 365의 위협 보호 기능 및 정책에 따라 수행 된 작업), 검색 기술 (맬웨어 감지 방법) 및 자세한. 

![검색 기술을 통해 검색 된 전자 메일에 대 한 데이터 보기](media/0c032eb3-6021-4174-9f06-ff8f30c245ca.png) 

차트 아래에 제목 줄, 받는 사람, 보낸 사람, 상태 등의 특정 전자 메일 메시지에 대 한 세부 정보를 확인 합니다. 

## <a name="content--malware"></a>콘텐츠 \> 맬웨어

SharePoint Online, 비즈니스용 OneDrive 및 Microsoft 팀에서 악성으로 식별 된 파일을 보여 주는 보기입니다.

맬웨어 제품군, 검색 기술 (맬웨어가 감지 된 방법) 및 작업 (OneDrive, SharePoint 또는 팀)을 통해 정보를 확인 합니다. 

![검색 된 맬웨어에 대 한 데이터 보기](media/d11dc568-b091-4159-b261-df13d76b520b.png)  

차트 아래에서 첨부 파일 이름, 작업, 파일 크기, 파일을 마지막으로 수정한 사용자 등 특정 파일에 대 한 세부 정보를 확인 합니다. 
  
## <a name="new-click-to-filter-capabilities"></a>(새로운 방법!) 간편 필터 기능

새로 만들기 Explorer를 클릭 하 여 필터링 할 수 있습니다. 늦은 5 월 말부터 범례에서 항목을 클릭 하면 해당 항목이 보고서에 대 한 필터가 됩니다. 예를 들어 Explorer에서 맬웨어 보기를 보고 있다고 가정 합니다.
  
![위협 관리 \> 탐색기로 이동](media/cab32fa2-66f1-4ad5-bc1d-2bac4dbeb48c.png)
  
이 차트에서 **ATP 샌드 박싱** 를 클릭 하면 다음과 같은 보기가 만들어집니다. 
  
![탐색기가 필터링 되어 ATO 샌드 박싱 결과만 표시 합니다.](media/7241d7dd-27bc-467d-9db8-6e806c49df14.png)
  
이 보기에서는 [Office 365 ATP 안전한 첨부](atp-safe-attachments.md)파일에서 열 된 파일에 대 한 데이터를 살펴봅니다. 이 차트 아래에서 ATP 안전한 첨부 파일에 의해 검색 된 첨부 파일이 있는 특정 전자 메일 메시지에 대 한 세부 정보를 확인할 수 있습니다.
  
![검색 된 첨부 파일이 있는 전자 메일 메시지에 대 한 구체적인 세부 정보](media/c91fb05c-d1d4-4085-acc6-f7008a415c2a.png)
  
항목을 하나 이상 선택 하면 선택한 항목에 대해 선택할 수 있는 여러 선택 항목이 제공 되는 **작업** 메뉴가 활성화 됩니다. 
  
![항목을 선택 하면 작업 메뉴가 활성화 됩니다.](media/95f127a4-1b2a-4a76-88b9-096e3ba27d1b.png)
  
클릭 하 고 특정 세부 정보로 탐색 하는 기능을 통해 위협을 조사 하는 데 많은 시간을 절약할 수 있습니다.
  
## <a name="how-do-i-get-explorer"></a>탐색기를 가져오려면 어떻게 해야 합니까?

Explorer는 [Office 365 위협 인텔리전스](office-365-ti.md)에 포함 되어 있습니다. 

Explorer를 보고 사용 하려면 보안 관리자 또는 보안 판독기에 부여 된 것과 같은 적절 한 사용 권한이 있어야 합니다. 자세한 내용은 [Office 365 보안 &amp; 및 준수 센터의 사용 권한](permissions-in-the-security-and-compliance-center.md)를 참조 하세요.
  
## <a name="related-topics"></a>관련 항목

[Office 365 보안 &amp; 및 준수 센터의 보고서 및 정보](reports-and-insights-in-security-and-compliance.md)
  
[배달 된 악성 전자 메일 찾기 및 조사 (Office 365 위협 인텔리전스)](investigate-malicious-email-that-was-delivered.md)
  
[Office 365의 스팸 방지 및 맬웨어 방지 보호](anti-spam-and-anti-malware-protection.md)
  

