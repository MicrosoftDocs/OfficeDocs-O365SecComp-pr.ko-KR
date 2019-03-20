---
title: 'Exchange Online Protection의 Exchange 관리 센터 '
ms.author: tracyp
author: MSFTTracyP
manager: laurawi
ms.date: 12/9/2016
ms.audience: ITPro
ms.topic: overview
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 97921f0e-832f-40c7-b56d-414faede5191
ms.collection:
- M365-security-compliance
description: EAC(Exchange 관리 센터)는 Microsoft EOP(Exchange Online Protection)의 웹 기반 관리 콘솔입니다.
ms.openlocfilehash: 983f6fe6b9f1592115e524315c9e52e08fed5101
ms.sourcegitcommit: 0f93b37c39d807dec91f118aa671a3430c47a9ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/20/2019
ms.locfileid: "30693447"
---
# <a name="exchange-admin-center-in-exchange-online-protection"></a>Exchange Online Protection의 Exchange 관리 센터 

EAC(Exchange 관리 센터)는 Microsoft EOP(Exchange Online Protection)의 웹 기반 관리 콘솔입니다. 
  
이 항목의 Exchange 2013 버전은 [Exchange admin center in Exchange 2013](http://technet.microsoft.com/library/a9aea11a-6ba3-4f4a-a76e-79072e7cfc7d.aspx)를 참조하세요.
  
이 항목의 Exchange Online 버전은 [Exchange admin center in Exchange Online](https://docs.microsoft.com/exchange/exchange-admin-center)를 참조하세요.
  
## <a name="accessing-the-eac"></a>EAC 액세스

대부분의 경우 EOP 고객은 Microsoft 365 관리 센터를 통해 EAC에 액세스 합니다. **내 소식** 타일 옆에 있는 **관리** 타일의 드롭다운 메뉴에 EOP에 대한 링크가 있습니다. **관리** 타일을 클릭하고 드롭다운 메뉴에서 **Exchange Online Protection**를 선택하여 EAC로 이동합니다. 
  
You can also access the EAC sign in page directly via the following URL: https://admin.protection.outlook.com/ecp/\<companydomain\>. For example, https://admin.protection.outlook.com/ecp/contoso.onmicrosoft.com. After specifying your user credentials you will be taken directly into the EAC.
  
## <a name="common-user-interface-elements-in-the-eac"></a>EAC의 공통 사용자 인터페이스 요소

이 섹션에서는 EMC에 있는 사용자 인터페이스 요소에 대해 설명합니다.
  
![EOP-admincenter](media/EOP-AdminCenter.png)
  
### <a name="feature-pane"></a>기능 창

이 창은 EAC에서 수행할 대부분의 작업에 대한 첫 번째 탐색 수준으로, 기능 영역별로 구성됩니다.
  
1. **받는 사람** 내부 사용자와 외부 연락처를 볼 수 있습니다. 
    
2. **사용 권한** 관리자 역할을 관리할 수 있습니다. 
    
3. **준수 관리** 관리자 역할 그룹 보고서와 같은 보고서, 감사 로그 등을 찾아볼 수 있습니다. 
    
4. **보호** 조직에 대해 맬웨어 방지 및 스팸 방지 보호 기능을 관리하고 격리된 메시지를 관리할 수 있습니다. 
    
5. **메일 흐름** 규칙, 허용 도메인 및 커넥터를 관리하고 메시지 추적을 수행할 수 있습니다. 
    
### <a name="tabs"></a>탭

탭은 두 번째 탐색 수준입니다. 각 기능 영역에는 각각의 기능을 나타내는 다양한 탭이 있습니다.
  
### <a name="toolbar"></a>도구 모음

대부분의 탭은 클릭하면 도구 모음이 표시됩니다. 도구 모음에는 특정 작업을 수행하는 아이콘이 있습니다. 다음 표에서는 아이콘과 그 작업에 대해 설명합니다.
  
|**아이콘**|**이름**|**작업**|
|:-----|:-----|:-----|
|![아이콘 추가](media/ITPro-EAC-AddIcon.gif)           <br/> |추가, 새로 만들기  <br/> |이 아이콘을 사용하면 새 개체를 만들 수 있습니다. 일부 아이콘에는 아래쪽 화살표가 있으며 이 화살표를 클릭하면 만들 수 있는 추가 개체가 표시됩니다.  <br/> |
|![편집 아이콘](media/ITPro-EAC-EditIcon.gif)           <br/> |편집  <br/> |이 아이콘을 사용하면 개체를 편집할 수 있습니다.  <br/> |
|![삭제 아이콘](media/ITPro-EAC-DeleteIcon.gif)           <br/> |삭제  <br/> |이 아이콘을 사용하면 개체를 삭제할 수 있습니다. 일부 삭제 아이콘에는 아래쪽 화살표가 있으며 이 화살표를 클릭하면 추가 옵션이 표시됩니다.  <br/> |
|![검색 아이콘](media/ITPro-EAC-.gif)           <br/> |검색  <br/> |이 아이콘을 사용하면 찾으려는 개체에 대한 검색어를 입력할 수 있는 검색 상자가 열립니다.  <br/> |
|![새로 고침 아이콘](media/ITPro-EAC-RefreshIcon.gif)           <br/> |새로 고침  <br/> |이 아이콘을 사용하면 목록 보기를 새로 고칠 수 있습니다.  <br/> |
|![기타 옵션 아이콘](media/ITPro-EAC-MoreOptionsIcon.gif)           <br/> |기타 옵션  <br/> |이 아이콘을 사용하면 해당 탭의 개체에 대해 수행할 수 있는 기타 작업을 볼 수 있습니다. 예를 들어 **받는 사람 \> 사용자**에서 이 아이콘을 클릭하면 **고급 검색**을 수행할 수 있는 옵션이 표시됩니다.  <br/> |
|![위쪽 화살표 아이콘](media/ITPro-EAC-UpArrowIcon.gif)![아래쪽 화살표 아이콘](media/ITPro-EAC-DownArrowIcon.gif)           <br/> |위쪽 화살표와 아래쪽 화살표  <br/> |이 아이콘을 사용하면 개체 우선 순위를 위나 아래로 이동할 수 있습니다.  <br/> |
|![아이콘 제거](media/ITPro-EAC-RemoveIcon.gif)           <br/> |제거  <br/> |이 아이콘을 사용하면 목록에서 개체를 제거할 수 있습니다.  <br/> |
   
### <a name="list-view"></a>목록 보기

탭을 선택하면 대부분의 경우 목록 보기가 표시됩니다. EAC 목록 보기 내에서 약 10,000개의 개체를 볼 수 있습니다. 또한 결과로 페이징할 수 있도록 페이징이 포함되어 있습니다.
  
### <a name="details-pane"></a>세부 정보 창

목록 보기에서 개체를 선택하면 해당 개체에 대한 정보가 세부 정보 창에 표시됩니다. 세부 정보 창에 관리 작업이 포함된 경우도 있습니다.
  
### <a name="me-tile-and-help"></a>내 소식 타일 및 도움말

**내 소식** 타일을 통해 EAC에서 로그아웃하고 다른 사용자로 로그인할 수 있습니다. **도움말**![도움말 아이콘](media/ITPro-EAC-HelpIcon.gif) 드롭다운 메뉴에서 다음 작업을 수행할 수 있습니다. 
  
1. **도움말** 온라인 도움말 내용을 보려면 ![도움말 아이콘](media/ITPro-EAC-HelpIcon.gif)을 클릭합니다. 
    
2. **풍선형 도움말 사용 안 함** 풍선형 도움말에는 개체를 만들거나 편집할 때 필드에 대한 상황에 맞는 도움말이 표시됩니다. 풍선형 도움말을 끌 수 있으며, 풍선형 도움말을 사용하지 않도록 설정한 경우에는 켤 수 있습니다. 
    
3. **저작권**Exchange Online Protection에 대한 저작권 표시를 보려면 이 링크를 클릭합니다. 
    
4. **개인 정보 보호 정책**Exchange Online Protection의 개인 정보 보호 정책을 보려면 클릭합니다. 
    
## <a name="supported-browsers"></a>지원되는 브라우저

최상의 EAC 사용 환경을 위해 항상 최신 브라우저, Office 클라이언트 및 앱을 사용하는 것이 좋습니다. 또한 소프트웨어 업데이트가 제공되면 이를 설치하는 것이 좋습니다. 서비스의 지원되는 브라우저 및 시스템 요구 사항에 대한 자세한 내용은 [Office 365 시스템 요구 사항](https://go.microsoft.com/fwlink/p/?LinkID=402699)을 참조하세요. 
  
## <a name="supported-languages-in-eop"></a>EOP에서 지원되는 언어

Exchange Online Protection에서 지원되고 사용할 수 있는 언어는 다음과 같습니다.
  
- 암하라어
    
- 아랍어
    
- 바스크어(바스크)
    
- 뱅골어(인도)
    
- 불가리아어
    
- 카탈로니아어
    
- 중국어(간체)
    
- 중국어(번체)
    
- 크로아티아어
    
- 체코어
    
- 덴마크어
    
- 네덜란드어
    
- 네덜란드어
    
- 영어
    
- 에스토니아어
    
- 필리핀어(필리핀)
    
- 핀란드어
    
- 프랑스어
    
- 갈리시아어
    
- 독일어
    
- 그리스어
    
- 구자라트어
    
- 히브리어
    
- 힌디어
    
- 헝가리어
    
- 아이슬란드어
    
- 인도네시아어
    
- 이탈리아어
    
- 일본어
    
- 칸나다어
    
- 카자흐어
    
- 스와힐리어
    
- 한국어
    
- 라트비아어
    
- 리투아니아어
    
- 말레이어(브루나이)
    
- 말레이어(말레이시아)
    
- 말라얄람어
    
- 마라티어
    
- 노르웨이어(복말)
    
- 노르웨이어(니노르스크)
    
- 오리야어
    
- 페르시아어
    
- 폴란드어
    
- 포르투갈어(브라질)
    
- 포르투갈어(포르투갈)
    
- 루마니아어
    
- 러시아어
    
- 세르비아어(키릴 자모, 세르비아)
    
- 세르비아어(라틴 문자)
    
- 슬로바키아어
    
- 슬로베니아어
    
- 스페인어
    
- 스웨덴어
    
- 타밀어
    
- 텔루구어
    
- 태국어
    
- 터키어
    
- 우크라이나어
    
- 우르두어
    
- 베트남어
    
- 웨일스어
    

