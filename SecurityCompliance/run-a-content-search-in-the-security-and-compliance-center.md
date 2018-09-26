---
title: 콘텐츠 검색을 실행 하는 Office 365 보안에서 &amp; 준수 센터
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 6/26/2018
ms.audience: Admin
ms.topic: article
f1_keywords:
- ms.o365.cc.ComplianceSearch
ms.service: o365-administration
localization_priority: Normal
ms.assetid: 61852fd9-fe8a-4880-a339-cb19ed3bff4a
description: '콘텐츠 검색을 사용 하 여 Office 365 보안에서 &amp; 준수 센터 비즈니스 위치에 대 한 사서함, SharePoint Online 사이트 및 OneDrive를 검색 합니다. '
ms.openlocfilehash: d480579db1c39d51d4fa8b0931106f135c5339d2
ms.sourcegitcommit: 7956955cd919f6e00b64e4506605a743c5872549
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/26/2018
ms.locfileid: "25038321"
---
# <a name="run-a-content-search-in-the-office-365-security-amp-compliance-center"></a>콘텐츠 검색을 실행 하는 Office 365 보안에서 &amp; 준수 센터

Office 365 보안에서 콘텐츠 검색 eDiscovery 도구를 사용할 수 있는 &amp; 준수 센터 전자 메일, 문서 및 인스턴트 메시징 대화 Office 365 조직에서 등의 항목을 찾으려고 합니다. 이 도구를 사용 하 여 이러한 Office 365 서비스에 있는 항목을 찾으려고 합니다.
  
- Exchange Online 사서함과 공용 폴더
    
- SharePoint Online 및 비즈니스 사이트에 대 한 OneDrive
    
- 비즈니스 대화에 대 한 Skype
    
- Microsoft Teams 
    
- Office 365 그룹
    
콘텐츠 검색은 새롭고 향상 된 성능과 확장성 기능을 사용 하는 새 eDiscovery 검색 도구입니다. 콘텐츠 검색을 사용 하 여 매우 큰 eDiscovery 검색을 실행 합니다. 비즈니스 계정 단일 콘텐츠 검색에 대 한 모든 사서함, 모든 Exchange 공용 폴더 및 모든 SharePoint Online 사이트와 OneDrive를 검색할 수 있습니다. 검색할 수 있는 콘텐츠 위치 수에 제한이 있습니다. 동시에 실행할 수 있는 검색 수에 제한이 있습니다. 콘텐츠 검색, 콘텐츠 위치 개수를 실행 하 고 검색 결과 예상된 수 **콘텐츠 검색** 페이지에서 세부 정보 창에 표시 됩니다. 검색을 실행 하 고 나면 결과 미리 보고, 하나에 대 한 키워드 통계를 가져올 수 또는 더 많은 검색 콘텐츠 검색을 대량으로 편집 하 고 로컬 컴퓨터에 결과 내보냅니다. 
  
 **목차**
  
[검색 만들기](run-a-content-search-in-the-security-and-compliance-center.md#create)
  
[검색 결과 내보내기](run-a-content-search-in-the-security-and-compliance-center.md#export)
  
[검색 결과 미리 보기](run-a-content-search-in-the-security-and-compliance-center.md#preview)
  
[검색 결과 업데이트](run-a-content-search-in-the-security-and-compliance-center.md#restart)
  
[검색 편집](run-a-content-search-in-the-security-and-compliance-center.md#edit)
  
[검색 다시 시도](run-a-content-search-in-the-security-and-compliance-center.md#retry)
  

  
## <a name="before-you-begin"></a>시작하기 전에

- 검색 쿼리 및 [키워드 쿼리 및 콘텐츠 검색에 대 한 검색 조건을](keyword-queries-and-search-conditions.md)참조 부울 검색 연산자를 사용 하 여 정보 및 구축 하는 방법에 대 한 지침에 대 한 합니다. 이 문서에는 중요 한 정보 유형을 검색 하 고 내부 테두리와 조직 외부의 사용자와 공유 되는 콘텐츠를 검색 하는 방법에 대 한 정보가 들어 있습니다.
    
- **콘텐츠 검색** 페이지를 검색 하 고 미리 보기를 수행 하 고 검색 결과 내보내기에 대 한 액세스를 관리자, 규정 준수 관리자 또는 eDiscovery 관리자 여야 보안에서 eDiscovery 관리자 역할 그룹의 구성원 &amp; 규정 준수 가운데 비즈니스 사이트에 대 한 추가 검색 권한 Exchange Online, SharePoint Online에서 또는 onedrive 할당 필요가 없습니다. 자세한 내용은 참조 [Office 365 보안에서 eDiscovery 사용 권한을 할당 &amp; 준수 센터](assign-ediscovery-permissions.md)합니다.
    
- 상태 및 Office 365 조직에 제공 하는 서비스의 품질을 유지 하기 위해 콘텐츠 검색에 적용 되는 제한이 있습니다. 대부분의 경우에서 이러한 제한을 수정할 수 없습니다 하지만 계획, 실행 및 검색 문제를 해결 하는 경우 고려 이러한 제한은 사용할 수 있도록 그 중 알고 있어야 합니다. 자세한 내용은 참조 [검색 Office 365 보안에 대 한 제한 &amp; 준수 센터](limits-for-content-search.md)합니다.
    
- 단일 콘텐츠 검색에서 검색 되는 사서함 수에 따라 예상된 검색 시간에 대 한 섹션을 참조 하십시오. 
    
- 앞서 설명한 것 처럼 Office 365 그룹 및 Microsoft 팀의 콘텐츠를 검색 하려면 콘텐츠 검색을 사용할 수 있습니다. 즉, 그룹 사서함, 공유 일정 및 Office 365 그룹과 팀이 Microsoft와 연결 된 SharePoint 사이트를 검색할 수 있습니다. 또한 Microsoft 팀에서 채널 대화를 검색할 수 있습니다. Office 365 그룹 및 Microsoft 팀의 하는 방법에 대 한 정보를 참조 하십시오.
    
  - [Office 365 그룹에 대 한 설명](https://support.office.com/article/b565caa1-5c40-40ef-9915-60fdb2d97fa2)
    
  - [팀이 Microsoft 도움말](https://support.office.com/article/23156c0c-2c6e-49dd-8b7b-7c564b76508c)
    
    Office 365 그룹 및 Microsoft 팀의 콘텐츠를 검색에 대 한 팁 섹션을 참조 하십시오. 
    
[Return to top](run-a-content-search-in-the-security-and-compliance-center.md#top)
  
## <a name="create-a-search"></a>검색 만들기
<a name="create"> </a>

1. [https://protection.office.com](https://protection.office.com)으로 이동합니다.
    
2. 작업이 나 교육용 계정을 사용 하 여 Office 365에 로그인 합니다.
    
3. 보안 및 준수 센터의 왼쪽 창에서 **검색 및 조사** \> **콘텐츠 검색**을 클릭합니다.
    
4. **새로 만들기**![추가 아이콘](media/O365-MDM-CreatePolicy-AddIcon.gif)을 클릭합니다.
    
5. **새 검색** 페이지에서 콘텐츠 검색의 이름을 입력합니다. 이 이름은 조직 내에서 고유해야 합니다. 
    
6. 검색 하려는 콘텐츠 위치를 선택 합니다. 동일한 검색에서 사서함, 사이트 및 공용 폴더를 검색할 수 있습니다.
    
    ![검색 하려는 콘텐츠 위치를 선택 합니다.](media/da32e3f9-6cd6-4a26-8217-e97a5a7071e4.png)
  
1. **모든 위치에서 검색** 조직에서 모든 콘텐츠 위치를 검색 하려면이 옵션을 선택 합니다. 이 옵션을 선택 하는 경우 (모든 Office 365 그룹 및 팀이 Microsoft에 대 한 비활성 사서함 및 사서함을 포함 한), 모든 사서함을 검색 하도록 선택할 수 있습니다 모든 SharePoint와 비즈니스 사이트에 대 한 OneDrive (Office 365 그룹의 모든 사이트를 포함 하 고 Microsoft 팀의 경우) 및 모든 공용 폴더입니다.
    
    ![검색을 모든 곳에서 모든 콘텐츠 위치를 검색 하는 옵션을 클릭](media/86f132f1-0a2a-4048-900c-9f219d909ef2.png)
  
2. **사용자 지정 위치 선택** 사서함 및 사이트를 검색 하려면를 선택 하려면이 옵션을 선택 합니다. 이 옵션을 선택 하는 경우 (예: 모든 Exchange 사서함을 검색) 특정 서비스에 대 한 모든 콘텐츠 위치를 검색할 수 있는 유연성을 해야 하거나 Office 365 서비스에 대 한 특정 콘텐츠 위치를 검색할 수 있습니다.
    
    검색할 콘텐츠 위치를 추가 하는 경우 다음을 염두에 두십시오.
    
    **사서함**
    
  - **추가**클릭 하면![아이콘 추가](media/ITPro-EAC-AddIcon.gif) 검색할 사서함을 지정 하려면 표시 되는 사서함 선택 비어 있습니다. 성능 향상을 위해 디자인입니다. 이 목록에 받는 사람을 추가 하려면 검색 상자에 이름 (최소 3 자)를 입력 하 고 **검색**을 클릭![검색 아이콘](media/5f6f9463-50e9-460b-8738-b67e759c2efc.gif)합니다.
    
  - 비활성 사서함 및 메일 그룹을 검색 하는 사서함의 목록에 추가할 수 있습니다. 메일 그룹에 대 한 그룹 구성원의 사서함 검색 됩니다. Note 동적 메일 그룹 지원 되지 않습니다.
    
  - 명령을 실행 하면 조직에서 비활성 사서함의 목록을 가져오려면, `Get-Mailbox -InactiveMailboxOnly` Exchange Online PowerShell에서 합니다. 또는 **데이터 관리 방식** 으로 이동할 수 있습니다 \> 보안에서 **보존** &amp; 준수 센터 다음 **자세히**를 클릭 하 고![탐색 모음 타원](media/9723029d-e5cd-4740-b5b1-2806e4f28208.gif) \> **비활성 사서함**입니다.
    
  - 또한는 Office 365 그룹 또는 팀이 Microsoft와 관련 된 사서함을 추가할 수 있습니다. 이 경우에 그룹 또는 팀 사서함 검색은 되지 않습니다. 그룹 또는 팀 구성원의 사서함 검색 되지 않습니다. 를 검색 하려면 구체적으로 검색에 추가할 필요가 있습니다.
    
  - 모든 사서함 검색을 포함 하도록 않으려면 **선택 특정 사서함 검색을**선택 하지만 사서함 목록에 추가 하지 마십시오.
    
    **사이트**
    
  - **추가**클릭![아이콘 추가](media/ITPro-EAC-AddIcon.gif) 검색 사이트를 추가 합니다. 검색 하려는 각 사이트에 대 한 URL을 입력 합니다. 콘텐츠 검색 도구는 URL의 유효성을 검사 하 고을 검색 하는 사이트의 목록에 추가 됩니다. 
    
  - Office 365 그룹 또는 팀이 Microsoft와 관련 된 SharePoint를 추가할 수 있습니다. 그룹 또는 팀에 대 한 URL을 확인 하는 방법에 대 한 지침 섹션을 참조 하십시오. 
    
  - 검색에서 모든 사이트를 포함 하도록 않으려면 **선택 검색 하려면 특정 사이트**선택 하지만 사이트 목록에 추가 하지 마십시오.
    
    **공용 폴더**
    
    공용 폴더에 대 한 Exchange Online 조직에서 모든 공용 폴더를 검색 하거나 모든 공용 폴더를 검색 하지를 선택할 수 있습니다.
    
7. **다음**을 클릭합니다.
    
8. **새 검색** 페이지에서 키워드 및 조건을 추가하여 검색 쿼리를 만들 수 있습니다. 
    
    ![키워드와 같은 검색 쿼리 만들기](media/1b7cf7b5-f1e1-471a-ad5c-48aad8435b00.png)
  
1. 아래에 있는 상자에서 **수행할를 찾도록 우리?**, 상자에 검색 쿼리를 입력 합니다. 키워드, 메시지 전송 및 받은 날짜 또는 파일 이름 등의 문서 속성 또는 문서를 마지막으로 변경한 날짜와 같은 속성을 지정할 수 있습니다. 예: **AND**, **또는**, **하지**, **NEAR**또는 **ONEAR**부울 연산자를 사용 하는 보다 복잡 한 쿼리를 사용할 수 있습니다. 문서 또는 외부에서 공유 된 문서에 대 한 검색에서 중요 한 정보 (예: 주민등록 번호)을 검색할 수도 있습니다. 키워드 상자에 빈을 지정 하지 않으면 검색 결과에 지정 된 콘텐츠 위치에 있는 모든 콘텐츠를 포함 합니다. 
    
2. 각 행에 키워드 형식과 **키워드 목록을 표시** 확인란을 클릭할 수 있습니다. 이렇게 하면 각 행에 키워드 만들어지는 검색 쿼리에 **또는** 연산자로 연결 됩니다. 
    
    ![키워드 목록에 있는 행의 키워드 또는 키워드 단계를 입력할 수 있습니다.](media/aea1a361-639d-4a82-8c3c-48645ef3fc05.png)
  
    키워드 목록을 사용 하는 이유 각 키워드를 일치 하는 얼마나 많은 항목이 표시 하는 통계를 얻을 수 있습니다. 이 키워드는는 가장 (및 최소) 효과적인를 빠르게 식별할 수 있습니다. 행에서 (괄호로 묶입니다) 키워드 구의 사용할 수도 있습니다. 검색 통계에 대 한 자세한 내용은 [콘텐츠 검색 결과 대 한 키워드 통계 보기를](view-keyword-statistics-for-content-search.md)참조 하십시오.
    
    키워드 목록을 사용 하 여에 대 한 지침 섹션을 참조 하십시오. 
    
3. 대문자로 표시 될 수 있는 부울 연산자 및 지원 되지않는 문자에 대 한 쿼리를 확인 하려면 **오타에 대 한 쿼리 확인** 을 클릭 합니다. 지원 되지않는 문자는 종종 및 일반적으로 검색 오류를 발생 숨겨지거나 원하지 않는 결과 반환 합니다. 지원 되지않는 문자를 되는지 여부를 확인 하는 방법에 대 한 자세한 내용은 [오류에 대 한 콘텐츠 검색 쿼리와 확인](check-your-content-search-query-for-errors.md)을 참조 하십시오.
    
4. **조건**조건을 검색 범위를 좁힐 보다 정교한 결과 집합이 반환 하는 검색 쿼리를 추가 합니다. KQL 검색 쿼리를 만들고 실행 하 여 검색을 시작 하는 경우에 절을 추가 하는 각 조건입니다. 조건 **및** 연산자에 의해 (키워드 상자에 지정 된) 키워드 쿼리를 논리적으로 연결 됩니다. 항목 키워드 쿼리 및 결과에 포함 되어야 하는 조건을 모두 충족 해야 함을 의미 합니다. 결과 범위를 좁히려면 조건 도움이 되는 방식입니다. 
    
||
|:-----|
|검색 쿼리 만들기 (영문) 및 조건을 사용 하는 방법에 대 한 자세한 내용은 [키워드 쿼리 및 콘텐츠 검색에 대 한 검색 조건을 ](keyword-queries-and-search-conditions.md)참조 하십시오. |
   
9. **검색**을 클릭하여 검색 설정을 저장하고 검색을 시작합니다. 
    
    검색 시작 됩니다. 검색이 완료 되 면 세부 정보 창에 다음과 같은 정보가 표시 됩니다.
    
    ![검색 통계 선택한 콘텐츠 검색의 세부 정보 창에 표시 되며](media/2046bb5e-f4cb-4ba7-b7fc-8e5e53dae567.png)
  
1. 날짜 및 검색 마지막으로 실행 된 시간입니다.
    
2. 수 (및 총 크기) 항목의는 발견 된 검색 쿼리를 일치 시킵니다. 항목 종류의 예로 전자 메일 메시지, 일정 항목 및 문서를 들 수 있습니다. 항목에 대 한 검색 되는 키워드의 여러 인스턴스를 포함 하는 경우 총 항목 수에 한번 계산만 됩니다. 예, "stock" 단어를 검색 하려면 또는 "tip" 및 전자 메일 메시지로 "stock" 라는 단어의 세 인스턴스를 포함 하는 경우만 계산 됩니다 한번 **항목** 필드에 합니다. 
    
3. 검색 된 콘텐츠 위치에 있는 크고 인덱싱되지 않은 항목의 총 크기와 수 있습니다. 세부 정보 창에 표시 되는 검색 통계에 검색 조건을 충족 하지 않는 인덱싱되지 않은 항목 수가 포함 됩니다. 인덱싱되지 않은 항목 일치 하는 항목 검색 (하기 때문에 검색 조건을 충족 하는 다른 메시지 또는 문서 속성)를 쿼리 하는 경우 예상된 인덱싱되지 않은 항목 수에 포함 되지 않습니다. 그러나 인덱싱되지 않은 항목이 검색 조건에 의해를 제외 하는 경우 인덱싱되지 않은 항목의 예상에 포함 되지 않습니다.
    
4. 각 유형의 검색 된 콘텐츠 위치 번호입니다. 사서함에 대 한 보관 사서함 검색 된 사서함의 총 수에 포함 되는 note 합니다. 이전 예제에서 4 개의 사용자 사서함에서 검색 된 하 고 각이 사용자에 대 한 보관 사서함 사용 하도록 설정 합니다. 이 때문 8 개의 사서함 검색 통계에 나와 있습니다.
    
5. 검색 미리 보기에 대 한 링크가 결과 또는 검색 검색 통계 업데이트를 다시 실행 합니다.
    
    필요한 경우 **새로 고칠**을 클릭![새로고침 아이콘](media/O365-MDM-Policy-RefreshIcon.gif) 선택한 검색에 대 한 세부 정보 창에 대 한 정보를 업데이트 합니다. 
    
[Return to top](run-a-content-search-in-the-security-and-compliance-center.md#top)
  
## <a name="export-search-results"></a>검색 결과 내보내기
<a name="export"> </a>

검색을 성공적으로 실행 한 후에 로컬 컴퓨터에 검색 결과 내보낼 수 있습니다. 전자 메일 결과 내보낼 때 사진을 다운로드 한 사용자의 컴퓨터에 PST 파일로 합니다. SharePoint와 OneDrive에서 비즈니스 사이트에 대 한 콘텐츠를 내보낼 때 네이티브 Office 문서의 복사본을 내보냅니다. 추가 문서와 내보낸된 검색 결과에 포함 된 보고서 됩니다. 자세한 내용은 참조 [내보내기 검색 결과 Office 365 보안에서 &amp; 준수 센터](export-search-results.md)합니다.
  
## <a name="preview-search-results"></a>검색 결과 미리 보기
<a name="preview"> </a>

검색을 성공적으로 완료 된 후에 검색 결과 미리볼 수 있습니다. 제한와 관련 된 콘텐츠 검색 결과 미리볼 수가 있습니다. 자세한 내용은 참조 [검색 Office 365 보안에 대 한 제한 &amp; 준수 센터](limits-for-content-search.md)합니다. 인덱싱되지 않은 항목 미리 보기에서 사용할 수 없습니다는 note 합니다.
  
1. **콘텐츠 검색** 페이지에서 검색을 선택 합니다. 
    
2. 세부 정보 창에서 **결과** 아래의 **검색 결과 미리 보기**를 클릭합니다. **검색 결과 미리 보기** 페이지가 열리고 검색 결과 항목 목록이 표시됩니다. 
    
    제목, 형식, 보낸사람, 또는 항목의 원본 사서함에서 받은 날짜를 기준으로 결과 정렬 하려면 열 머리글을 클릭 수 있습니다.
    
3. 항목을 미리 보기를 클릭 합니다.
    
    항목 미리 보기 창에서 열립니다.
    
4. 문서의 복사본을 다운로드 하려면 또는 미리 보기에 대 한 파일 형식을 지원 되지 않으면 로컬 컴퓨터에 다운로드 하려면 **원본 파일을 다운로드** 를 클릭 수 있습니다. 경우에 페이지에 액세스할 수 있는 권한이 없습니다 웹 페이지.aspx에 대 한 페이지에 대 한 URL을 포함 됩니다. 
    
> [!NOTE]
> 마지막 7 일이 경과으로 실행 된 검색에 대 한 검색 결과 미리 보고 하는 경우에 검색 결과 업데이트 하 라는 메시지가 표시 됩니다. 검색 되는 검색 쿼리를 충족 하는 최신 결과 얻으려면 다시 실행 합니다. 
  
### <a name="file-types-that-can-be-previewed"></a>미리 보기를 할 수 있는 파일 형식

미리 보기 창에서 지원 되는 파일 형식 미리볼 수 있습니다. 파일 형식을 지원 되지 않으면 보기에서 로컬 컴퓨터로 파일 복사본을 다운로드 해야 합니다. 다음과 같은 파일 형식 지원 되며 **검색 결과 미리 보기** 페이지에서 미리볼 수 있습니다. 
  
- .txt,.html,.mhtml
    
- .eml
    
- .doc,.docx,.docm
    
- .pptm,.pptx
    
- .pdf
    
또한 다음과 같은 파일 컨테이너 형식 지원 됩니다. 미리 보기 창에서 컨테이너에 있는 파일 목록을 볼 수 있습니다.
  
- .zip
    
- .gzip
    
[Return to top](run-a-content-search-in-the-security-and-compliance-center.md#top)
  
## <a name="update-search-results"></a>검색 결과 업데이트
<a name="restart"> </a>

기존 콘텐츠 검색의 결과 업데이트할 때 지정 된 모든 콘텐츠 위치에 검색 쿼리는 다시 실행 됩니다. 검색 결과 업데이트 하는 분명 한 이유 최신 데이터를 얻는 것입니다.
  
1. **콘텐츠 검색** 페이지에서 결과를 업데이트할 검색을 선택합니다. 
    
2. 세부 정보 창에서 **결과** 아래의 **검색 결과 업데이트**를 클릭합니다.
    
    상태 메시지는 결과 가져올 없다는 표시 됩니다. 검색이 완료 되 면 업데이트 된 정보는 세부 정보 창에서 **결과** 아래에서 표시 됩니다. Note 세부 정보 창에서 **에서 검색** 필드에 날짜 현재 날짜와 시간으로 업데이트 되도록 합니다. 콘텐츠 검색 목록에서 정보를 새로 고칠 **새로고침**을 클릭![새로고침 아이콘](media/O365-MDM-Policy-RefreshIcon.gif)합니다.
    
[Return to top](run-a-content-search-in-the-security-and-compliance-center.md#top)
  
## <a name="edit-a-search"></a>검색 편집
<a name="edit"> </a>

기존 콘텐츠 검색에 대 한 원본 사서함 및 검색 쿼리를 변경할 수 있습니다.
  
1. **콘텐츠 검색** 페이지에서 검색을 선택 합니다. 
    
2. 세부 정보 창에서 **쿼리** 아래의 **검색 편집**을 클릭합니다.
    
3. **위치** 페이지에 있는 사서함, 그룹, SharePoint 사이트 또는 비즈니스 사이트에 대 한 검색 하려면 OneDrive를 변경할 수 있습니다. 선택할 수 있습니다 (또는 선택 되지 않은) Exchange의 모든 공용 폴더를 검색 합니다. 
    
4. **쿼리** 페이지에서 검색 쿼리를 편집할 수 있습니다. 
    
5. 수정 된 검색을 시작 하는 **원본** 또는 **위치** 페이지에서 **검색** 을 클릭 합니다. 
    
    수정된 검색이 시작됩니다. 검색이 완료되면 수정된 검색에 대한 예상 결과가 세부 정보 창에 표시됩니다.
    
## <a name="retry-a-search"></a>검색 다시 시도
<a name="retry"> </a>

검색을 모든 오류를 반환 하는 경우에 다시의 모든 콘텐츠 위치를 검색 필요가 없습니다. 콘텐츠 위치에 실패 한 검색을 다시가 되도록 검색을 다시 실행할 수 있습니다. 모든 콘텐츠 위치를 다시 검색 하려면 검색 결과 업데이트할 수 있습니다.
  
1. **콘텐츠 검색** 페이지에서 다시 검색 하려는 콘텐츠 위치를 포함 하는 검색을 선택 합니다. 
    
2. 세부 정보 창에서 **오류** 아래의 **검색 다시 시도**를 클릭합니다.
    
    상태 메시지는 결과 가져올 없다는 표시 됩니다. 검색 완료 되 면 업데이트 된 정보는 세부 정보 창에서 **결과** 아래에서 표시 됩니다. Note 세부 정보 창에서 **에서 검색** 필드에 날짜 현재 날짜와 시간으로 업데이트 되도록 합니다. 검색의 목록에서 정보를 새로 고칠 **새로고침**을 클릭![새로고침 아이콘](media/O365-MDM-Policy-RefreshIcon.gif)합니다.
    
[Return to top](run-a-content-search-in-the-security-and-compliance-center.md#top)
  
## <a name="more-information"></a>추가 정보
<a name="moreinfo"> </a>

콘텐츠를 검색 하는 방법에 대 한 자세한 내용은 다음과 같습니다.
  
[제한 및 성능](run-a-content-search-in-the-security-and-compliance-center.md#limits)
  
[인덱싱되지 않은 항목](run-a-content-search-in-the-security-and-compliance-center.md#unindexeditems)
  
[팀이 Microsoft 및 Office 365 그룹](run-a-content-search-in-the-security-and-compliance-center.md#teams)
  
[비즈니스용 OneDrive](run-a-content-search-in-the-security-and-compliance-center.md#onedrive)
  
[검색 쿼리](run-a-content-search-in-the-security-and-compliance-center.md#queries)
  
[비활성 사서함 검색](run-a-content-search-in-the-security-and-compliance-center.md#inactivemailboxes)
  
[기타](run-a-content-search-in-the-security-and-compliance-center.md#misc)
  
[(맨위로 돌아가기)](run-a-content-search-in-the-security-and-compliance-center.md#top)
  
 **제한 및 성능**
  
- 콘텐츠 검색 기능에 적용 되는 제한에 대 한 참조 [검색 Office 365 보안에 대 한 제한 &amp; 준수 센터](limits-for-content-search.md)합니다.
    
- Microsoft는 모든 Office 365 조직에 의해 실행 되는 콘텐츠 검색에 대 한 성능 정보를 수집 합니다. 복잡 한 검색 쿼리 검색 시간에 영향을 줄 수를 하는 동안 기간 검색 라인은 사서함의 수에 영향을 주는 가장 큰 요인 해야 검색 됩니다. Microsoft 검색 시간에 대 한 서비스 수준 계약을 제공 하지, 하지만 다음 표에서 검색에 포함 된 사서함 수에 따라 콘텐츠 검색에 대 한 평균 검색 시간을 보여줍니다.
    
|**사서함 수**|**평균 검색 시간**|
|:-----|:-----|
|100  <br/> |30초  <br/> |
|1,000  <br/> |45 초  <br/> |
|10,000  <br/> |4분  <br/> |
|25000  <br/> |10분  <br/> |
|50000  <br/> |20분  <br/> |
|100,000  <br/> |25분  <br/> |
   

  
 **인덱싱되지 않은 항목**
  
- 검색 되는 콘텐츠 위치에 앞에서 설명한 것, 인덱싱되지 않은 항목으로 예상된 검색 결과에 포함 됩니다. 인덱싱되지 않은 항목 일치 하는 항목 검색 (하기 때문에 검색 조건을 충족 하는 다른 메시지 또는 문서 속성)를 쿼리 하는 경우 예상된 인덱싱되지 않은 항목 수에 포함 되지 않습니다. 인덱싱되지 않은 항목이 검색 조건에 의해를 제외 하는 경우 것도에 포함 되지 않습니다 예상된 인덱싱되지 않은 항목 수입니다. 자세한 내용은 [콘텐츠 검색의 인덱싱되지 않은 항목](https://go.microsoft.com/fwlink/p/?LinkId=780739)을 참조 하십시오.
    

  
 **팀이 Microsoft 및 Office 365 그룹**
  
- 팀이 Microsoft Office 365 그룹 기반으로 구축 됩니다. 따라서 검색 하는 매우 유사 합니다. 팀이 Microsoft 및 Office 365 그룹의 콘텐츠를 검색할 때 다음 사항에 주의 유지 합니다.
    
  - 팀이 Microsoft 및 Office 365 그룹에 있는 콘텐츠를 검색 하려면 사서함 및 팀 또는 그룹에 연결할 수 있는 SharePoint 사이트를 지정 해야 합니다.
    
  - Microsoft 팀 또는 Office 365 그룹에 대 한 속성을 보려면 Exchange Online에서 **Get UnifiedGroup** cmdlet을 실행 합니다. 이것은 팀 또는 그룹에 연결 된 사이트의 URL을 얻으려면 좋은 방법입니다. 예, 다음 수석 지도 팀 이라는 하는 Office 365 그룹에 대 한 하는 선택 된 속성을 표시 하는 다음 명령을: 
    
  ```
  Get-UnifiedGroup "Senior Leadership Team" | FL DisplayName,Alias,PrimarySmtpAddress,SharePointSiteUrl
  DisplayName            : Senior Leadership Team
  Alias                  : seniorleadershipteam
  PrimarySmtpAddress     : seniorleadershipteam@contoso.onmicrosoft.com
  SharePointSiteUrl      : https://contoso.sharepoint.com/sites/seniorleadershipteam
  
  ```

    > [!NOTE]
    > **Get UnifiedGroup** cmdlet를 실행 하려면 역할을 할당 보기 권한만 있는 받는 사람에 게 Exchange 온라인 해야 하거나 역할 그룹의 구성원 이어야 하는 할당 보기 권한만 있는 받는 사람에 게 역할입니다. 
  
  - 사용자의 사서함을 검색 하는 경우 모든 Microsoft 팀 또는 Office 365 그룹의 구성원 인 사용자를 검색할 수 없습니다. 마찬가지로, 검색 하는 경우 Microsoft 팀 이나 그룹 사서함 및만 그룹 사이트 수를 지정 하는 Office 365 그룹 검색은 되지 않습니다. 사서함 및 그룹 구성원의 비즈니스 계정에 대 한 OneDrive 검색에 명시적으로 추가 하지 않으면 검색 되지 않습니다.
    
  - Microsoft 팀 또는 Office 365 그룹의 구성원 목록을 가져오려면,에서 속성을 볼 수 있습니다는 **홈 \> 그룹** Office 365 관리 센터의 페이지입니다. 또는 Exchange Online PowerShell에서 다음 명령을 실행할 수 있습니다. 
    
  ```
  Get-UnifiedGroupLinks <group or team name> -LinkType Members | FL DisplayName,PrimarySmtpAddress 
  ```

    > [!NOTE]
    > **Get UnifiedGroupLinks** cmdlet를 실행 하려면 역할을 할당 보기 권한만 있는 받는 사람에 게 Exchange 온라인 해야 하거나 역할 그룹의 구성원 이어야 하는 할당 보기 권한만 있는 받는 사람에 게 역할입니다. 
  
  - Microsoft 팀의 채널의 일부인 대화에 연결 된 Microsoft 팀의 사서함에 저장 됩니다. 마찬가지로, 채널에서 팀 구성원을 공유 하는 파일은 팀의 SharePoint 사이트에 저장 됩니다. 따라서 채널의 대화 및 파일을 검색 하는 콘텐츠 위치의 Microsoft 팀 사서함 및 SharePoint 사이트를 추가 해야 합니다.
    
  - 
    
    또는 Microsoft 팀의 채팅 목록에 포함 된 대화 대화방에 참가 한 사용자의 Exchange Online 사서함에 저장 됩니다. 및 채팅 대화에 사용자를 공유 하는 파일의 파일 공유는 사용자의 비즈니스 계정에 대 한 OneDrive에 저장 됩니다. 따라서 채팅 목록에서 대화 하 고 파일을 검색 하려면 콘텐츠 위치로 비즈니스 계정에 대 한 개별 사용자 사서함 및 OneDrive를 추가 해야 합니다.
    
    > [!NOTE]
    > Microsoft 팀의 채팅 목록에 포함 된 대화에 참가 한 사용자 채팅 대화를 검색 하는 순서에는 Exchange Online (클라우드 기반) 사서함이 있어야 합니다. 채팅 목록에 포함 된 대화 채팅 참가자의 클라우드 기반 사서함에 저장 된 때문입니다. 채팅 참가자가 없는 경우 Exchange Online 사서함, 채팅 대화를 검색할 수 없습니다. 예, Exchange 하이브리드 배포에서 온-프레미스 사서함이 있는 사용자 Microsoft 팀의 채팅 목록에 포함 된 대화에 참가할 수 있도록 수 있습니다. 그러나이 경우이 대화의 콘텐츠를 없는 검색 가능한 사용자 클라우드 기반 사서함이 없기 때문에 있습니다. 
  
  - 모든 Microsoft 팀 또는 팀 채널 노트 작성 및 공동 작업에 대 한 Wiki를 포함합니다. Wiki 콘텐츠.mht 서식 사용 하 여 파일을 자동으로 저장 됩니다. 이 파일은 팀의 SharePoint 사이트에 팀이 위 키 데이터 문서 라이브러리에 저장 됩니다. 검색할 콘텐츠 위치로 팀의 SharePoint 사이트를 지정 하 여 Wiki를 검색 하는 콘텐츠 검색 도구를 사용할 수 있습니다. 
    
    > [!NOTE]
    > (팀의 SharePoint 사이트를 검색) 하는 경우 Microsoft 팀 또는 채널에 대 한 Wiki를 검색 하는 기능은 2017 년 6 월 22에 릴리스 되었습니다. 위 키 페이지를 저장 되거나에서 업데이트 된 날짜 또는 후에 검색할 사용할 수 있는 합니다. 위 키 페이지 마지막으로 저장 하거나 해당 날짜 이전에 업데이트 검색에 사용할 수 없습니다. 
  

  
 **비즈니스용 OneDrive **
  
- Url의 목록을 조직에서 비즈니스 사이트에 대 한 onedrive를 수집 하려면 [조직에서 모든 OneDrive 위치의 목록 만들기](https://support.office.com/article/8e200cb2-c768-49cb-88ec-53493e8ad80a)를 참조 합니다. 이 문서의 스크립트 비즈니스 사이트에 대 한 모든 OneDrive 목록이 포함 된 텍스트 파일을 만듭니다. 이 스크립트를 실행 하려면 설치 하 고 SharePoint Online 관리 셸을 사용 해야 합니다. 검색 하려는 비즈니스 사이트에 대 한 각 OneDrive에 조직의 내 사이트 도메인에 대 한 URL을 추가 해야 합니다. 비즈니스;에 대 한 모든 OneDrive를 포함 하는 도메인입니다. 예, `https://contoso-my.sharepoint.com`합니다. 다음은 비즈니스 사이트에 대 한 사용자의 OneDrive에 대 한 URL의 한 예: `https://contoso-my.sharepoint.com/personal/sarad_contoso_onmicrosoft.com`합니다.
    

  
 **검색 쿼리**
  
- 키워드 목록을 사용 하 여 검색 쿼리를 만들 때 다음 사항에 주의 유지 합니다.
    
  - 해야 **키워드 목록을 표시** 확인란을 선택 하 고 검색 쿼리를 만드는 별도 행에 각 키워드를 입력 한 다음 각 행의 키워드 (또는 키워드 구) **OR** 연산자로 연결 됩니다. 키워드 상자에 키워드 목록을 붙여 방금 또는 키워드를 입력 한 후 **Enter** 키를 눌러, 하는 경우 **또는** 연산자로 연결 되지 않습니다. 키워드 목록을 추가 하는 잘못 된 및 올바른 예는 다음과 같습니다. 
    
    **잘못 된**
    
    ![(키워드 상자에 목록을 붙여넣어) 하 여 키워드 목록 서식을 지정 하는 잘못 된 방법](media/fb54e3df-232a-439a-b3d7-27a60ec76a4c.png)
  
    **맞는**
    
    ![(확인란을 차례로 선택 붙여넣기 목록) 하 여 키워드 목록 서식을 지정 하는 올바른 방법](media/5d511a7b-c1f9-499c-bffe-e075bfc9adec.png)
  
  - 또한 키워드 또는 키워드 구를 Excel 파일 또는 일반 텍스트 파일을 목록을 준비 하 고 하 고 복사 하 고, 키워드 목록에 목록에 붙여 수 있습니다. 이 작업을 수행 하려면 **키워드 목록을 표시** 확인란을 선택 해야 합니다. 그런 다음, 키워드 목록에 있는 첫번째 행을 클릭 하 고 목록에 붙여넣습니다. 키워드 목록에서 행을 구분 하는 Excel 또는 텍스트 파일에서 각 줄에 붙여넣어집니다. 
    
  - (선택 된 검색의 세부 정보 창)에서 검색 쿼리 구문을 확인 하는 것이 좋습니다를은 키워드 목록을 사용 하 여 쿼리를 만든 후 검색 쿼리는 의도 합니다. **쿼리** 아래에서 세부 정보 창에 표시 되는 검색 쿼리 키워드는 쉼표로 구분 하 여 텍스트 **(c:s)**. 키워드 **OR** 연산자로 연결 되어 있음을 나타냅니다. 마찬가지로, 검색 쿼리 조건을 포함 하는 경우 조건과 키워드는 구분 하 여 텍스트 **(c:c)**. 키워드 **및** 연산자에 의해 조건에 연결 되어 있음을 나타냅니다. 키워드 목록 및 조건을 사용 하는 경우 발생 하는 검색 쿼리 (세부 정보 창에 표시 됨)의 예는 다음과 같습니다. 
    
    ![쿼리 키워드 목록 및 조건을 사용할 때 만들어지는의 예](media/b463750c-57fa-4602-9fed-0d5a420db3ad.png)
  
  - 영어가 아닌 문자 (예: 중국어 문자)에 대 한 키워드를 포함 하는 검색 쿼리를 사용 하는 경우 콘텐츠 검색에 대 한 언어 속성을 구성 하는 **집합 ComplianceSearch** cmdlet을 사용 해야할 수 있습니다. GUI를 사용 하 여 보안에서 콘텐츠 검색을 만들 때 &amp; 준수 센터의 기본 언어 중립 됩니다. 
    
    콘텐츠 검색에 대 한 언어 설정을 변경할 필요가 어떻게 알 수 있습니까? 인 경우 콘텐츠 위치를 검색 하는 영어가 아닌 문자를 포함 하지만 검색에서 반환 하는 결과가 없으면 특정 언어 설정이 원인일 수 있습니다.
    
    기존 콘텐츠 검색에 대 한 언어 설정을 변경 하려면 다음 명령을 실행 보안 &amp; 준수 센터 PowerShell:
    
  ```
  Set-ComplianceSearch <name of content search> -Language <culture code value>
  ```

    예, 하려면 언어 설정을 중국어로 변경, 사용 `zh-CN` 문화권 코드 값에 대 한 합니다. 언어 설정, 변경 된 후 검색을 다시 실행 해야 합니다. 가능한 문화권 코드 값의 목록에 대 한 [CultureInfo 클래스](https://go.microsoft.com/fwlink/p/?LinkID=184859)를 참조 하십시오. 두 부분으로 구성 문화권 코드를 사용 하 여 언어 설정;의 값에 대 한 좋습니다 콘텐츠 검색 예, `ja-JP` 및 not `ja`합니다.
    

  
 **비활성 사서함 검색**
  
앞서 설명한 것 처럼 콘텐츠 검색에서 비활성 사서함을 검색할 수 있습니다. 다음은 비활성 사서함을 검색할 때 주의 해야할 사항입니다.
  
- 콘텐츠 검색 사용자 사서함을 포함 하는 경우 해당 사서함 그런 다음 비활성 이루어집니다 비활성 하 게 되 면 검색을 다시 실행 하는 경우 비활성 사서함을 검색 하는 콘텐츠 검색을 계속 됩니다.
    
- 일부 경우에는 사용자는 활성 사서함과 동일한 SMTP 주소를가지고 있는 비활성 사서함 있을 수 있습니다. 이 경우 콘텐츠 검색에 대 한 위치도를 선택 하면 특정 사서함만 검색 됩니다. 즉, 검색 하는 사용자의 사서함을 추가 하는 경우 가정할 수 없습니다는 자신의 활성 및 비활성 사서함 검색 됩니다 되지 않습니다. 검색에 명시적으로 추가 하는 사서함을 검색 합니다.
    
- 활성 사서함과 동일한 SMTP 주소를 사용 하 여 비활성 사서함 필요 하지 못하도록 하는 것이 좋습니다. 비활성 사서함을 복구 하거나 활성 사서함이 있는 (또는 활성 사서함의 보관) 비활성 사서함의 내용을 복원 하는 다음 삭제를 권장 비활성 사서함에 현재 할당 된 SMTP 주소를 다시 사용 해야하는 경우는 비활성 사서함입니다. 자세한 내용은 다음 항목 중 하나를 참조 하십시오.
    
  - [Office 365에서 비활성 사서함 복구](recover-an-inactive-mailbox.md)
    
  - [Office 365에서 비활성 사서함 복원](restore-an-inactive-mailbox.md)
    
  - [Office 365에서 비활성 사서함 삭제](delete-an-inactive-mailbox.md)
    

  
 **기타**
  
- **콘텐츠 검색** 페이지의 보안에서 작성 한 검색 콘텐츠 &amp; 준수 센터에 표시 되지 않습니다는 **원본 위치 eDiscovery &amp; 유지** Exchange 관리 센터의 페이지입니다. 콘텐츠 검색 아키텍처 및 검색 개체의 보안에서 만든 하기 때문에이 &amp; 준수 센터는 Exchange Online의 원본 위치 eDiscovery 기능 보다 완전히 다릅니다. 
    
    같은 이유 때문에 **콘텐츠 검색** 페이지에서 작성 한 검색 보안에서 eDiscovery 사례의 **검색** 페이지에 표시 되지 않으면 &amp; 준수 센터입니다. 
    
- 다시 시작 하 고 검색을 다시 시도 하는 간의 차이 무엇입니까? 검색을 다시 시작 하면 새 미리 보기 검색에서 검색에 지정 된 모든 콘텐츠 위치 다시 검색 됩니다. 그러나 검색을 다시 시도 하는 경우 콘텐츠 위치는 검색을 마지막으로 실행 하는 경우에 실패 한 다시 검색 됩니다.
   

