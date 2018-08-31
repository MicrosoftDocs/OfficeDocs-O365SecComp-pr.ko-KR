---
title: EDiscovery 검색 결과에서 중복 제거
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 12/21/2016
ms.audience: Admin
ms.topic: overview
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MOE150
- MET150
ms.assetid: 5af334b6-a15d-4f73-97f8-1423457d9f6b
description: 취소 동일한 메시지의 여러 인스턴스는 서로 다른 사서함에서 찾을 수 있습니다 하는 경우에 전자 메일 메시지의 복사본을 하나만 내보낼 수 있도록 내보내도록 eDiscovery 검색 결과 복제 하는 옵션이 있습니다.
ms.openlocfilehash: 02a4f9f6db0fb8831d5e5cc13adaffbd0c4dcecc
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22534040"
---
# <a name="de-duplication-in-ediscovery-search-results"></a>EDiscovery 검색 결과에서 중복 제거

이 문서에서는 eDiscovery 검색 결과의 중복 작동 하 고 중복 알고리즘의 제한 사항에 설명 하는 방법에 대해 설명 합니다.
  
Office 365 eDiscovery 도구를 사용 하 여 eDiscovery 검색의 결과 내보낼를 해제 내보내도록 결과 복제 하려면 옵션도 있습니다. 무슨 뜻 입니까? 중복을 사용 하면 (기본적으로 중복 되지 사용), 전자 메일 메시지의 복사본을 하나만 내보내는 경우에 동일한 메시지의 여러 인스턴스는 검색 된 사서함에서 찾을 수 있습니다. 중복을 사용 하면 검토 하 고 검색 결과 내보내도록 후 분석 해야 하는 항목 수가 감소 하 여 시간을 절약할 수 있습니다. 하지만 중복의 작동 방식을 이해 하 고 내보내기 프로세스 중에 중복 된 것으로 표시할지 고유 항목을 발생 시킬 수 있는 알고리즘에 제한이 있는지에 유의 해야 합니다.
  
## <a name="how-duplicate-messages-are-identified"></a>중복 된 메시지는 식별 하는 방법

Office 365 eDiscovery 도구 메시지 중복 되는지 여부를 확인 하려면 다음 전자 메일 속성 조합해 서 사용 합니다.
  
- **InternetMessageId** -이 속성은 특정 메시지의 특정 버전을 참조 하는 전역적으로 고유 식별자는 전자 메일 메시지의 인터넷 메시지 식별자를 지정 합니다. 이 ID는 보낸 사람의 전자 메일 클라이언트 프로그램 또는 메시지를 보내는 호스트 전자 메일 시스템에서 생성 됩니다. 사용자는 둘 이상의 받는 사람에 게 메시지를 보내, 메시지의 각 인스턴스에 대해 동일 인터넷 메시지 ID 됩니다. 원본 메시지의 이후 수정 하는 다양 한 메시지 식별자를 받게 됩니다. 
    
- **ConversationTopic** -가 속성 대화 스레드 메시지의 제목을 지정합니다. **ConversationTopic** 속성 값은 대화의 전체 항목에 설명 하는 문자열입니다. 보존 하는 초기 메시지 및 초기 메시지에 회신에 보낸 모든 메시지의로 구성 됩니다. 같은 대화 내에서 메시지 **ConversationTopic** 속성에 대 한 같은 값을가지고 있습니다. 이 속성의 값은 일반적으로 대화를 생성 하는 초기 메시지의 제목 줄입니다. 
    
- **BodyTagInfo** -내부 Exchange 저장소 속성입니다. 이 속성의 값은 메시지의 본문에 다양 한 특성을 확인 하 여 계산 됩니다. 이 속성은 메시지 본문의 차이 식별 하는데 사용 됩니다. 
    
EDiscovery 내보내기 프로세스 동안 이러한 세 속성은 검색 조건과 일치 하는 모든 메시지에 대 한 비교 됩니다. 이러한 속성은 두 (또는 그 이상) 메시지에 대 한 동일, 이러한 메시지 중복 된 것으로 확인 되 하 고 결과 중복을 사용 하도록 설정 하는 경우 메시지의 복사본을 하나만 내보낼 수는 있습니다. 내보내는 메시지 "원본 항목" 이라고 합니다. 중복 된 메시지에 대 한 정보는 내보낸된 검색 결과에 포함 된 **Results.csv** 및 **Manifest.xml** 보고서에 포함 됩니다. **Results.csv** 파일에서 중복 된 메시지의 **중복 항목을** 열에서 값을 사용 함으로써 식별 됩니다. 내보낸 메시지에 대 한 **항목 Id** 열 값과 일치 하는 값이이 열에 있습니다. 
  
다음 그래픽 표시 방법을 중복 된 메시지가 검색 결과 함께 내보내집니다 **Results.csv** 및 **Manifest.xml** 보고서에 표시 됩니다. 이러한 보고서는 앞에서 설명한 중복 알고리즘에 사용 되는 전자 메일 속성을 포함 하지 않습니다. 대신, 보고서는 Exchange 저장소에서 항목에 할당 된 **항목 Identity** 속성을 포함 합니다. 
  
 ### <a name="resultscsv-report-viewed-in-excel"></a>Results.csv 보고서 (Excel에 표시 됨)
  
![Results.csv 보고서에서 중복 된 항목에 대 한 정보 보기](media/e3d64004-3b91-4cba-b6f3-934b46cbdcdb.png)
  
 ### <a name="manifestxml-report-viewed-in-excel"></a>Manifest.xml 보고서 (Excel에 표시 됨)
  
![Manifest.xml 보고서에서 중복 된 항목에 대 한 정보 보기](media/69aa4786-9883-46ff-bcae-b35e0daf4a6d.png)
  
또한 중복 메시지에서 다른 속성 내보내기 보고서에 포함 됩니다. 메일 그룹에 메시지를 보낸 여부 및 참조 또는 다른 사용자에 게 된 숨은 참조 메시지 인지 여부 중복 된 메시지에 있는 사서함 포함 됩니다.
  
## <a name="limitations-of-the-de-duplication-algorithm"></a>중복 알고리즘의 제한 사항

중복 되는 값으로 표시 하기에 고유 항목을 초래할 수 있는 중복 알고리즘의 알려진된 제한 사항은 있습니다. 것은 선택적 중복 기능을 사용할 것인지 여부를 결정할 수 있도록 이러한 제한 사항 이해 하는 것이 중요 합니다.
  
여기에서 중복 기능 수 실수로 중복 된 것으로 메시지를 식별 하 고 내보내지 않으려면 (하지만 여전히 내보내기 보고서에서 중복 된 것으로 인용) 한 상황이 있습니다. 이들은 메시지에 사용자를 편집 하는 있지만 보낼 하지 않습니다. 예, 사용자 Outlook에서 메시지를 선택 하는, 메시지의 내용을 복사 하 고 새 메시지에 붙여 가정해보십시오. 다음 사용자 변경 된 복사본 중 하나 제거 또는 첨부 파일을 추가 하거나 제목줄 또는 자체 본문을 변경 하 여 합니다. 이러한 두 메시지가 eDiscovery 검색의 쿼리 일치 하는 경우 중복 검색 결과 내보낼 때 사용 하는 경우 메시지 중 하나에만 내보낼 수 있습니다. 따라서 원본 메시지 또는 복사 된 메시지 변경 된 경우에 모두 수정 된 메시지를 보낸 및 받지 **InternetMessageId**, **ConversationTopic** 및 **BodyTagInfo** 속성의 값을 업데이트 하는 따라서 합니다. 고유 하지만 앞에서 설명한 것 처럼 메시지를 모두 내보내기 보고서에 나열 됩니다. 
  
고유한 메시지 수도 수로 표시 하는 중복 항목을 원본 위치 유지 또는 소송 보존으로 설정 되는 사서함의 대/소문자와 같이 기록 중 복사 페이지 보호 기능을 사용 하는 경우 note 합니다. 기록 중 복사 기능 원본 메시지에 복사 (하 고 사용자의 복구 가능한 항목 폴더의 버전 폴더에 저장 하는) 원본 항목에 수정 버전을 저장 하기 전에 합니다. 이 경우 수정 된 복사 및 (복구 가능한 항목 폴더)에 있는 원본 메시지 중복 메시지도 간주 될 수 있습니다 하 고 그 중 하나에 내보낼 수는 있으므로 합니다.
  
> [!IMPORTANT]
> 중복 알고리즘의 제한 사항 검색 결과의 품질에 영향을 줄 수를 하는 경우 항목을 내보낼 때 중복을 사용 하지 말아야 합니다. 이 섹션에서 설명 하는 경우 검색 결과에서 한 요소가 될 가능성이 없는 경우 중복 된 것을 하고자 하는 항목 수를 줄일 중복을 사용 하도록 설정 고려해 야 합니다. 
  
## <a name="more-information"></a>추가 정보

- 이 문서의 정보는 최종 사용자가 다음 eDiscovery 도구 중 하나를 사용 하 여 검색 결과 내보낼 때 적용 됩니다.
    
  - Office 365 보안에서 콘텐츠 검색 &amp; 준수 센터
    
  - Exchange Online의 원본 위치 eDiscovery
    
  - SharePoint Onlin의 eDiscovery 센터
    
- 검색 결과 내보내기 (영문) 하는 방법에 대 한 자세한 내용은 다음을 참조 합니다.
    
  - [Office 365 보안에서 검색 결과 내보내기 &amp; 준수 센터](export-search-results.md)
    
  - [Office 365 보안에서 콘텐츠 검색 보고서 내보내기 &amp; 준수 센터](export-a-content-search-report.md)
    
  - [PST 파일로 내보낼 원본 위치 eDiscovery 검색 결과](https://go.microsoft.com/fwlink/p/?linkid=832671)
    
  - [eDiscovery 센터에서 콘텐츠 내보내기 및 보고서 만들기](https://support.office.com/article/7b2ea190-5f9b-4876-86e5-4440354c381a)
