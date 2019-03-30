---
title: EDiscovery 검색 결과에서 중복 제거
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 12/21/2016
ms.audience: Admin
ms.topic: overview
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- Strat_O365_IP
- M365-security-compliance
search.appverid: MOE150
ms.assetid: 5af334b6-a15d-4f73-97f8-1423457d9f6b
description: 동일한 메시지의 여러 인스턴스가 서로 다른 사서함에서 발견 된 경우에도 전자 메일 메시지의 복사본 하나만 내보내도록 내보내기 위해 내보낸 eDiscovery 검색 결과를 복제 해제 하는 옵션을 사용할 수 있습니다.
ms.openlocfilehash: b3810e3568bd2c7aa1628bcfcebbad5a87468ff8
ms.sourcegitcommit: e7a776a04ef6ed5e287a33cfdc36aa2d72862b55
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/29/2019
ms.locfileid: "30999301"
---
# <a name="de-duplication-in-ediscovery-search-results"></a>EDiscovery 검색 결과에서 중복 제거

이 문서에서는 eDiscovery 검색 결과의 중복 제거 방법에 대해 설명 하 고 중복 제거 알고리즘의 제한에 대해 설명 합니다.
  
Office 365 ediscovery 도구를 사용 하 여 ediscovery 검색의 결과를 내보낼 때 내보내는 결과를 복제 하지 않도록 선택할 수 있습니다. 시나리오 중복 제거를 사용 하도록 설정 하는 경우 (기본적으로 중복 제거를 사용 하지 않도록 설정), 검색 된 사서함에서 같은 메시지의 여러 인스턴스를 발견 한 경우에도 전자 메일 메시지의 복사본을 하나만 내보낼 수 있습니다. 비 복제는 검색 결과를 내보낸 후 검토 하 고 분석 해야 하는 항목 수를 줄임으로써 시간을 절약 하는 데 도움이 됩니다. 그러나 중복 연결이 해제 되는 방식을 이해 하는 것이 중요 하며, 내보내기 프로세스 중에 고유한 항목을 중복으로 표시할 수 있는 알고리즘에 제한이 있다는 점에 유의 해야 합니다.
  
## <a name="how-duplicate-messages-are-identified"></a>중복 메시지를 식별 하는 방법

Office 365 eDiscovery 도구 다음 전자 메일 속성의 조합을 사용 하 여 메시지가 중복 되었는지 여부를 확인할 수 있습니다.
  
- **internetmessageid** -이 속성은 특정 메시지의 특정 버전을 나타내는 전역 고유 식별자 인 전자 메일 메시지의 인터넷 메시지 id를 지정 합니다. 이 ID는 보낸 사람의 전자 메일 클라이언트 프로그램 또는 메시지를 보내는 호스트 전자 메일 시스템을 통해 생성 됩니다. 사용자가 메시지를 두 명 이상의 받는 사람에 게 보내는 경우 인터넷 메시지 ID는 메시지의 각 인스턴스에 대해 동일 합니다. 원본 메시지에 대 한 후속 변경 내용에는 다른 메시지 식별자가 표시 됩니다. 
    
- **conversationtopic 속성과** -해당 속성 메시지의 대화 스레드 제목을 지정 합니다. **conversationtopic 속성과** 속성 값은 대화의 전체 주제를 설명 하는 문자열입니다. 보존 이란 초기 메시지에 대 한 회신으로 전송 된 모든 메시지와 초기 메시지를 구성 합니다. 같은 대화 내의 메시지는 **conversationtopic 속성과** 속성의 값과 동일 합니다. 이 속성의 값은 일반적으로 대화를 생성 한 초기 메시지의 제목 줄입니다. 
    
- **BodyTagInfo** -내부 Exchange 저장소 속성입니다. 이 속성의 값은 메시지 본문에서 다양 한 특성을 확인 하 여 계산 됩니다. 이 속성은 메시지 본문의 차이점을 식별 하는 데 사용 됩니다. 
    
eDiscovery 내보내기 프로세스 중에 검색 조건과 일치 하는 모든 메시지에 대해 이러한 세 가지 속성을 비교 합니다. 두 개 이상의 메시지에 대해 이러한 속성을 동일 하 게 설정 하는 경우 이러한 메시지는 중복 되는 것으로 확인 되며 중복 해제 된 경우에는 메시지의 복사본 하나만 내보내집니다. 내보낸 메시지를 "원본 항목" 이라고 합니다. 중복 메시지에 대 한 정보는 내보낸 검색 결과에 포함 된 **.csv** 및 **manifest.xml** 보고서에 포함 됩니다. **결과 .csv** 파일에서 중복 **항목** 열에 값을 표시 하 여 복제 된 메시지를 식별 합니다. 이 열의 값은 내보낸 메시지의 **항목 id** 열에 있는 값과 일치 합니다. 
  
다음 그래픽에서는 검색 결과와 함께 내보낸 **.csv** 및 **manifest.xml** 보고서에 중복 메시지를 표시 하는 방법을 보여 줍니다. 이 보고서에는 이전에 설명한 중복 제거 알고리즘에서 사용 되는 전자 메일 속성이 포함 되어 있지 않습니다. 대신 Exchange 저장소에서 항목에 할당 한 **항목 Identity** 속성이 보고서에 포함 됩니다. 
  
 ### <a name="resultscsv-report-viewed-in-excel"></a>결과 .csv 보고서 (Excel에서 표시)
  
![결과 .csv 보고서의 중복 된 항목에 대 한 정보 보기](media/e3d64004-3b91-4cba-b6f3-934b46cbdcdb.png)
  
 ### <a name="manifestxml-report-viewed-in-excel"></a>manifest.xml 보고서 (Excel에서 표시)
  
![manifest.xml 보고서의 중복 항목에 대 한 정보 보기](media/69aa4786-9883-46ff-bcae-b35e0daf4a6d.png)
  
또한 중복 메시지의 다른 속성도 내보내기 보고서에 포함 됩니다. 여기에는 중복 메시지가 있는 사서함이 포함 되 고, 메시지가 메일 그룹으로 전송 되었는지, 메시지가 다른 사용자에 게 참조 아웃 또는 숨은 참조 인지 여부입니다.
  
## <a name="limitations-of-the-de-duplication-algorithm"></a>중복 제거 알고리즘의 제한 사항

중복 되지 않은 알고리즘의 몇 가지 알려진 제한 사항에 따라 고유 항목이 중복 항목으로 표시 될 수도 있습니다. 이러한 제한 사항을 이해 하는 것이 중요 하므로, 선택적 복제 기능을 사용할지 여부를 결정할 수 있습니다.
  
중복 제거 기능으로 인해 실수로 메시지를 중복 된 것으로 식별 하 고 내보낼 수는 없지만 내보내기에서는 여전히 중복 된 것으로 나타납니다. 사용자가 편집 하지만 보내지 않는 메시지입니다. 예를 들어 사용자가 Outlook에서 메시지를 선택 하 고 메시지 내용을 복사한 다음 새 메시지에 붙여 넣는 것을 가정해 보겠습니다. 사용자가 첨부 파일을 제거 또는 추가 하거나 제목 줄 또는 본문을 변경 하 여 복사본 중 하나를 변경 합니다. 이러한 두 메시지가 eDiscovery 검색 쿼리와 일치 하는 경우 검색 결과를 내보낼 때 중복 해제가 사용 되도록 설정 된 경우 메시지 중 하나만 내보내집니다. 따라서 원본 메시지 또는 복사 된 메시지가 변경 되었지만 수정 된 메시지는 전송 되지 않으며, 따라서 **internetmessageid**의 값은 **conversationtopic 속성과** 및 **BodyTagInfo** 속성이 업데이트 되지 않습니다. 앞에서 설명한 것 처럼 두 메시지가 모두 내보내기 보고서에 나열 됩니다. 
  
사서함을 소송 보존 또는 원본 위치 유지 상태로 설정 하는 경우와 마찬가지로, 쓰기 페이지 보호 기능을 사용 하는 경우에는 고유 메시지를 중복으로 표시할 수도 있습니다. 쓰기 복사 기능을 사용 하면 원본 메시지가 저장 되기 전에 원본 메시지를 복사 하 여 사용자의 복구 가능한 항목 폴더의 버전 폴더에 저장 합니다. 이 경우 수정 된 복사본 및 원본 메시지 (복구 가능한 항목 폴더)가 중복 메시지로 간주 되어 그 중 하나만 내보내집니다.
  
> [!IMPORTANT]
> 중복 제거 알고리즘의 한계가 검색 결과의 품질에 영향을 줄 수 있는 경우 항목을 내보낼 때 중복 제거를 사용 하도록 설정 하지 않아야 합니다. 이 섹션에서 설명 하는 상황이 검색 결과의 요인이 되지 않을 것 이며, 중복 되는 항목 수를 줄이기 위해서는 중복 제거를 사용 하도록 설정 하는 것이 좋습니다. 
  
## <a name="more-information"></a>추가 정보

- 이 문서의 정보는 다음 eDiscovery 도구 중 하나를 사용 하 여 검색 결과를 내보낼 때 적용할 수 있습니다.
    
  - Office 365의 준수 센터에서 콘텐츠 검색
    
  - Exchange Online의 원본 위치 eDiscovery
    
  - SharePoint Onlin의 eDiscovery 센터
    
- 검색 결과를 내보내는 방법에 대 한 자세한 내용은 다음을 참조 하십시오.
    
  - [콘텐츠 검색 내보내기](export-search-results.md)
    
  - [콘텐츠 검색 보고서 내보내기](export-a-content-search-report.md)
    
  - [PST 파일로 원본 위치 eDiscovery 검색 결과 내보내기](https://go.microsoft.com/fwlink/p/?linkid=832671)
    
  - [eDiscovery 센터에서 콘텐츠 내보내기 및 보고서 만들기](https://support.office.com/article/7b2ea190-5f9b-4876-86e5-4440354c381a)
