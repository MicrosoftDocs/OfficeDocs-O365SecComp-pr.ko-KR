---
title: Office 365 감사 로그에서 eDiscovery 활동 검색
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 10/24/2017
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
ms.collection: M365-security-compliance
localization_priority: Normal
search.appverid: MOE150
ms.assetid: 67cc7f42-a53d-4751-b929-6005c80798f7
description: 준수 관리자가 보안 &amp; 및 준수 센터에서 콘텐츠 검색 및 eDiscovery 사례 작업을 수행할 때 기록 되는 이벤트에 대 한 Office 365 감사 로그를 검색 하는 방법을 알아봅니다.
ms.openlocfilehash: f4778fd2aab48d58b3104dd2466875ba53e2c0a0
ms.sourcegitcommit: baf23be44f1ed5abbf84f140b5ffa64fce605478
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/26/2019
ms.locfileid: "30296761"
---
# <a name="search-for-ediscovery-activities-in-the-office-365-audit-log"></a>Office 365 감사 로그에서 eDiscovery 활동 검색

office 365 보안 &amp; 준수 센터에서 또는 해당 Windows PowerShell cmdlet을 실행 하 여 수행 되는 콘텐츠 검색 및 eDiscovery 관련 작업은 office 365 감사 로그에 기록 됩니다. 이벤트는 관리자 또는 준수 관리자 (또는 eDiscovery 권한이 할당 된 사용자)가 Office 365 보안 &amp; 및 준수 센터에서 다음과 같은 콘텐츠 검색 및 eDiscovery 관련 작업을 수행할 때 기록 됩니다.
  
- eDiscovery 사례 만들기 및 관리
    
- 콘텐츠 검색 만들기, 시작 및 편집
    
- 검색 결과 미리 보기, 내보내기, 삭제 등의 콘텐츠 검색 작업 수행
    
- 콘텐츠 검색에 대 한 사용 권한 필터링 구성
    
- eDiscovery 관리자 역할 관리
    
> [!IMPORTANT]
> 이 문서에서 설명 하는 작업은 보안 &amp; 및 준수 센터를 사용 하 여 수행한 eDiscovery 작업의 결과만 발생 합니다. Exchange online의 원본 위치 eDiscovery 도구 또는 SharePoint online의 eDiscovery Center를 사용 하 여 수행한 ediscovery 작업은 포함 되지 않습니다. 
  
office 365 감사 로그 검색, 필요한 사용 권한, 검색 결과 내보내기에 대 한 자세한 내용은 [office 365 보안 &amp; 및 준수 센터에서 감사 로그 검색](search-the-audit-log-in-security-and-compliance.md)을 참조 하십시오.
  
## <a name="how-to-search-for-and-view-ediscovery-activities"></a>eDiscovery 작업을 검색 하 고 확인 하는 방법

현재는 Office 365 감사 로그에서 eDiscovery 활동을 보기 위해 몇 가지 특정 작업을 수행 해야 합니다. 방법은 다음과 같습니다.
  
1. [https://protection.office.com](https://protection.office.com)으로 이동합니다.
    
2. 회사 또는 학교 계정을 사용하여 Office 365에 로그인합니다.
    
3. 왼쪽 창에서 **검색 &amp; 조사**를 클릭 하 고 **감사 로그 검색**을 클릭 합니다.
    
4. **작업** 드롭다운 목록의 **eDiscovery 활동**에서 검색할 하나 이상의 활동을 클릭 합니다. 또는 **ediscovery 활동** 을 클릭 하 여 모든 ediscovery 관련 활동을 검색할 수 있습니다. 
    
    > [!NOTE]
    > 또한 작업 드롭다운 목록에는 cmdlet 감사 로그의 레코드를 반환 하는 **eDiscovery cmdlet 작업** 이라는 작업 그룹이 포함 되어 있습니다. 
  
5.  날짜 및 시간 범위를 선택 하 여 해당 기간 내에 발생 한 eDiscovery 이벤트를 표시 합니다. 
    
6. **사용자** 상자에서 검색 결과를 표시할 사용자를 한 명 이상 선택 합니다. 모든 사용자에 대 한 항목을 반환 하려면이 상자를 비워 둡니다. 
    
7. 검색 **** 을 클릭 하 여 검색 조건을 사용 하 여 검색을 실행 합니다. 
    
8. 검색 결과가 표시 된 후 **결과 필터링** 을 클릭 하 여 결과 활동 레코드를 필터링 하거나 정렬할 수 있습니다. 아쉽게도 필터링을 사용 하 여 특정 활동을 명시적으로 제외할 수는 없습니다. 
    
9. 활동에 대 한 세부 정보를 보려면 검색 결과 목록에서 활동 레코드를 클릭 합니다. 
    
    이벤트 레코드의 자세한 속성을 포함 하는 **세부 정보가** 플라이 아웃 페이지에 표시 됩니다. 자세한 내용을 표시 하려면 **추가 정보**를 클릭 합니다. 이러한 속성에 대 한 [자세한 내용은 eDiscovery 작업에 대 한 자세한 속성](#detailed-properties-for-ediscovery-activities) 섹션을 참조 하십시오. 

  
## <a name="ediscovery-activities"></a>eDiscovery 활동

다음 표에서는 관리자 또는 사용자가 보안 &amp; 및 준수 센터를 사용 하거나 해당 cmdlet을 실행 하 여 ediscovery 관련 활동을 수행할 때 기록 되는 콘텐츠 검색 및 ediscovery 관련 작업에 대해 설명 합니다. 조직의 보안 &amp; 및 준수 센터에 연결 된 원격 PowerShell 
  
> [!NOTE]
> 이 섹션에서 설명 하는 ediscovery 작업은 다음 섹션에서 설명 하는 ediscovery cmdlet 작업에 대 한 유사한 정보를 제공 합니다. 이 섹션에서 설명 하는 eDiscovery 작업은 감사 로그 검색 결과에서 30 분 이내에 표시 되므로 사용 하는 것이 좋습니다. eDiscovery cmdlet 작업이 감사 로그 검색 결과에 표시 되는 데 최대 24 시간이 걸릴 수 있습니다. 
  
|**이름**|**Operation**|**해당 cmdlet**|**설명**|
|:-----|:-----|:-----|:-----|
|eDiscovery 사례에 구성원이 추가 됨  <br/> |CaseMemberAdded  <br/> |get-compliancecasemember 추가  <br/> |사용자가 eDiscovery 사례의 구성원으로 추가 되었습니다. 사례 구성원으로 서, 사용자는 필요한 권한이 할당 되었는지 여부에 따라 다양 한 사례 관련 작업을 수행할 수 있습니다.  <br/> |
|변경 된 콘텐츠 검색  <br/> |searchupdated  <br/> |Set-ComplianceSearch  <br/> |기존 콘텐츠 검색이 변경 되었습니다. 변경 사항에는 콘텐츠 위치 추가 또는 제거 또는 검색 쿼리 편집이 포함 될 수 있습니다.  <br/> |
|eDiscovery 관리자 멤버 자격 변경  <br/> |CaseAdminUpdated  <br/> |업데이트-eDiscoveryCaseAdmin  <br/> |조직의 eDiscovery 관리자 목록이 변경 되었습니다. 이 작업은 eDiscovery 관리자 목록이 새 사용자의 그룹으로 바뀔 때 기록 됩니다. 단일 사용자를 추가 하거나 제거 하면 CaseAdminAdded 작업이 기록 됩니다.  <br/> |
|eDiscovery 사례 변경  <br/> |CaseUpdated  <br/> |remove-compliancecase  <br/> |eDiscovery 사례가 변경 되었습니다. 변경 내용에는 미해결 사례 닫기 또는 닫힌 사례 다시 열기가 포함 됩니다.  <br/> |
|eDiscovery 사례 구성원 자격이 변경 됨  <br/> |CaseMemberUpdated  <br/> |업데이트-get-compliancecasemember  <br/> |eDiscovery 사례의 구성원 목록이 변경 되었습니다. 이 작업은 모든 구성원이 새 사용자의 그룹으로 바뀔 때 기록 됩니다. 단일 구성원을 추가 하거나 제거 하는 경우 CaseMemberAdded 또는 CaseMemberRemoved 작업이 기록 됩니다.  <br/> |
|변경 된 검색 권한 필터  <br/> |search추가 업데이트  <br/> |new-compliancesecurityfilter  <br/> |검색 권한 필터가 변경 되었습니다.  <br/> |
|eDiscovery 사례 보류에 대 한 검색 쿼리 변경  <br/> |HoldUpdated  <br/> |new-caseholdrule  <br/> |eDiscovery 사례와 관련 된 쿼리 기반 보류가 변경 되었습니다. 가능한 변경 사항에는 쿼리 기반 보존에 대 한 쿼리 또는 날짜 범위 편집이 포함 됩니다.  <br/> |
|콘텐츠 검색 미리 보기 항목 다운로드 됨  <br/> |PreviewItemDownloaded  <br/> |해당 없음  <br/> |사용자가 검색 결과를 미리 볼 때 **원래 항목 다운로드** 링크를 클릭 하 여 항목을 로컬 컴퓨터에 다운로드 한 경우  <br/> |
|나열 된 콘텐츠 검색 미리 보기 항목  <br/> |PreviewItemListed  <br/> |해당 없음  <br/> |사용자가 **검색 결과 미리 보기** 를 클릭 하 여 콘텐츠 검색 결과에서 최대 1000 개의 항목을 나열 하는 검색 결과 미리 보기 페이지를 표시 합니다.  <br/> |
|콘텐츠 검색 미리 보기 항목 표시  <br/> |PreviewItemRendered  <br/> |해당 없음  <br/> |eDiscovery 관리자가 검색 결과를 미리 볼 때 해당 항목을 클릭 하 여 확인 했습니다.  <br/> |
|만든 콘텐츠 검색  <br/> |searchcreated  <br/> |New-ComplianceSearch  <br/> |새 콘텐츠 검색을 만들었습니다.  <br/> |
|eDiscovery 관리자를 만들었습니다.  <br/> |CaseAdminAdded  <br/> |eDiscoveryCaseAdmin 추가  <br/> |사용자가 조직에서 eDiscovery 관리자로 추가 되었습니다.  <br/> |
|eDiscovery 사례를 만들었습니다.  <br/> |CaseAdded  <br/> |remove-compliancecase  <br/> |eDiscovery 사례를 만들었습니다. 사례를 만들 때 이름을 지정 하기만 하면 됩니다. 멤버 추가, 보류 만들기, 사례와 연결 된 콘텐츠 검색 만들기 등의 기타 사례 관련 작업은 추가 이벤트가 기록 됩니다.  <br/> |
|만든 검색 권한 필터  <br/> |searchpermissioncreated  <br/> |new-compliancesecurityfilter  <br/> |검색 권한 필터를 만들었습니다.  <br/> |
|eDiscovery 사례 보류에 대 한 검색 쿼리를 만들었습니다.  <br/> |HoldCreated  <br/> |new-caseholdrule  <br/> |eDiscovery 사례와 관련 된 쿼리 기반 보류를 만들었습니다.  <br/> |
|삭제 된 콘텐츠 검색  <br/> |searchremoved 됨  <br/> |Remove-ComplianceSearch  <br/> |기존 콘텐츠 검색이 삭제 되었습니다.  <br/> |
|삭제 된 eDiscovery 관리자  <br/> |CaseAdminRemoved  <br/> |eDiscoveryCaseAdmin을 제거 합니다.  <br/> |eDiscovery 관리자가 조직에서 삭제 되었습니다.  <br/> |
|삭제 된 eDiscovery 사례  <br/> |CaseRemoved  <br/> |remove-compliancecase을 제거 합니다.  <br/> |eDiscovery 사례가 삭제 되었습니다. 사례를 삭제 하려면 먼저 케이스와 연결 된 보류를 제거 해야 합니다.  <br/> |
|삭제 된 검색 권한 필터  <br/> |search에이 제거 됨  <br/> |new-compliancesecurityfilter을 제거 합니다.  <br/> |검색 권한 필터가 삭제 되었습니다.  <br/> |
|eDiscovery 사례 보류에 대해 삭제 된 검색 쿼리  <br/> |HoldRemoved  <br/> |new-caseholdrule을 제거 합니다.  <br/> |eDiscovery 사례와 관련 된 쿼리 기반 보류가 삭제 되었습니다. 보류 삭제의 결과는 보류에서 쿼리를 제거 하는 경우가 많습니다. 보류 또는 보류 쿼리를 삭제 하면 보류 되었던 콘텐츠 위치가 릴리스됩니다.  <br/> |
|다운로드 된 콘텐츠 검색 내보내기  <br/> |searchexportdownloaded  <br/> |해당 없음  <br/> |사용자가 콘텐츠 검색 결과를 로컬 컴퓨터에 다운로드 했습니다. 검색 결과를 다운로드 하려면 먼저 **콘텐츠 검색 작업의 내보내기를** 시작 해야 합니다.<br/> |
|미리 본 콘텐츠 검색 결과  <br/> |searchpreviewed 보기  <br/> |해당 없음  <br/> |콘텐츠 검색 결과를 미리 본 사용자입니다.  <br/> |
|제거 된 콘텐츠 검색 결과  <br/> |SearchResultsPurged  <br/> |New-ComplianceSearchAction  <br/> |사용자가 **new-compliancesearchaction** 명령을 실행 하 여 콘텐츠 검색의 결과를 제거 했습니다.  <br/> |
|콘텐츠 검색 분석이 제거 됨  <br/> |RemovedSearchResultsSentToZoom  <br/> |new-compliancesearchaction을 제거 합니다.  <br/> |Office 365 Advanced eDiscovery에 대 한 검색 결과를 준비 하기 위한 콘텐츠 검색 준비 작업을 삭제 했습니다. 준비 작업이 2 주 이내 였으 면 고급 eDiscovery 용으로 준비 된 검색 결과가 Microsoft Azure storage 영역에서 삭제 되었습니다. 준비 작업이 2 주 이상 경과 된 경우이 이벤트는 해당 준비 동작만 삭제 되었음을 나타냅니다.  <br/> |
|콘텐츠 검색 내보내기 제거 됨  <br/> |RemovedSearchExported  <br/> |new-compliancesearchaction을 제거 합니다.  <br/> |콘텐츠 검색 내보내기 작업이 삭제 되었습니다. 내보내기 작업이 2 주 이내 였던 경우 Microsoft Azure 저장소 영역에 업로드 된 검색 결과가 삭제 되었습니다. 내보내기 작업이 2 주 보다 오래 된 경우이 이벤트는 해당 내보내기 동작만 삭제 되었음을 나타냅니다.  <br/> |
|eDiscovery 사례에서 구성원 제거 됨  <br/> |CaseMemberRemoved  <br/> |get-compliancecasemember을 제거 합니다.  <br/> |사용자가 eDiscovery 사례의 구성원으로 제거 되었습니다.  <br/> |
|콘텐츠 검색 결과 미리 보기 제거 됨  <br/> |RemovedSearchPreviewed  <br/> |new-compliancesearchaction을 제거 합니다.  <br/> |콘텐츠 검색 미리 보기 작업이 삭제 되었습니다.  <br/> |
|콘텐츠 검색에 대해 수행 된 삭제 된 제거 작업  <br/> |RemovedSearchResultsPurged  <br/> |new-compliancesearchaction을 제거 합니다.  <br/> |콘텐츠 검색 제거 작업이 삭제 되었습니다.  <br/> |
|제거 된 검색 보고서  <br/> |searchreportremoved 됨  <br/> |new-compliancesearchaction을 제거 합니다.  <br/> |콘텐츠 검색 내보내기 보고서 작업이 삭제 되었습니다.  <br/> |
|콘텐츠 검색 분석이 시작 됨  <br/> |SearchResultsSentToZoom  <br/> |New-ComplianceSearchAction  <br/> |콘텐츠 검색 결과는 고급 eDiscovery에서 분석을 위해 준비 되었습니다.  <br/> |
|시작 콘텐츠 검색  <br/> |searchstarted  <br/> |Start-ComplianceSearch  <br/> |콘텐츠 검색을 시작 했습니다. 보안 &amp; 및 준수 센터 GUI를 사용 하 여 콘텐츠 검색을 만들거나 변경 하면 검색이 자동으로 시작 됩니다. **ComplianceSearch** 또는 **ComplianceSearch** cmdlet을 사용 하 여 검색을 만들거나 변경 하는 경우 **ComplianceSearch** cmdlet을 실행 하 여 검색을 시작 해야 합니다.<br/> |
|콘텐츠 검색 내보내기 시작  <br/> |내보낸 search  <br/> |New-ComplianceSearchAction  <br/> |사용자가 콘텐츠 검색 결과를 내보냈습니다.  <br/> |
|보고서 내보내기 시작  <br/> |searchreport  <br/> |New-ComplianceSearchAction  <br/> |사용자가 콘텐츠 검색 보고서를 내보냈습니다.  <br/> |
|콘텐츠 검색 중지 됨  <br/> |searchstopped 됨  <br/> |Stop-ComplianceSearch  <br/> |사용자가 콘텐츠 검색을 중지 했습니다.  <br/> |
  
## <a name="ediscovery-cmdlet-activities"></a>eDiscovery cmdlet 작업

다음 표에는 관리자 또는 사용자가 보안 &amp; 및 준수 센터를 사용 하거나 원격 PowerShell에서 해당 cmdlet을 실행 하 여 eDiscovery 관련 작업을 수행 하는 경우 기록 되는 cmdlet 감사 로그 레코드가 나와 있습니다. 조직의 보안 &amp; 및 준수 센터에 연결 됩니다. 이 표에 나와 있는 cmdlet 작업 및 이전 섹션에 설명 된 eDiscovery 작업에 대 한 감사 로그 레코드의 자세한 정보는 서로 다릅니다. 
  
앞에서 설명한 것 처럼 감사 로그 검색 결과에 eDiscovery cmdlet 작업을 표시 하는 데 최대 24 시간이 걸릴 수 있습니다.
  
> [!TIP]
> 다음 표의 **작업** 열에 있는 cmdlet은 TechNet의 해당 cmdlet 도움말 항목에 연결 됩니다. 각 cmdlet에 대해 사용 가능한 매개 변수에 대 한 설명을 보려면 cmdlet 도움말 항목으로 이동 합니다. cmdlet에 사용 된 매개 변수 및 매개 변수 값은 로깅된 각 eDiscovery cmdlet 작업에 대 한 감사 로그 항목에 포함 됩니다. 
  
|**이름**|**작업 (cmdlet)**|**설명**|
|:-----|:-----|:-----|
|eDiscovery 사례에서 생성 되는 보류  <br/> |[new-caseholdpolicy](https://go.microsoft.com/fwlink/p/?LinkId=823813) <br/> |eDiscovery 사례에 대 한 보류를 만들었습니다. 콘텐츠 원본을 지정 하지 않고 또는을 사용 하 여 보류를 만들 수 있습니다. 콘텐츠 원본이 지정 된 경우 감사 로그 항목에서 식별 됩니다.  <br/> |
|eDiscovery 사례에서 보류 삭제  <br/> |[new-caseholdpolicy을 제거 합니다.](https://go.microsoft.com/fwlink/p/?LinkId=823814) <br/> |eDiscovery 사례와 연결 된 보류가 삭제 되었습니다. 보류를 삭제 하면 보류의 모든 콘텐츠 위치가 해제 됩니다. 보류를 삭제 하면 보류와 연결 된 케이스 보류 규칙도 삭제 됩니다 (아래 **new-caseholdrule** 참조).<br/> |
|eDiscovery 사례의 변경 된 보류  <br/> |[new-caseholdpolicy](https://go.microsoft.com/fwlink/p/?LinkId=823815) <br/> |eDiscovery와 연결 된 보류가 변경 되었습니다. 가능한 변경 사항으로는 콘텐츠 위치를 추가 또는 제거 하거나 보류를 해제 (사용 하지 않도록 설정)가 포함 됩니다.  <br/> |
|eDiscovery 사례 보류에 대 한 검색 쿼리를 만들었습니다.  <br/> |[new-caseholdrule](https://go.microsoft.com/fwlink/p/?LinkId=823816) <br/> |eDiscovery 사례와 관련 된 쿼리 기반 보류를 만들었습니다.  <br/> |
|eDiscovery 사례 보류에 대해 삭제 된 검색 쿼리  <br/> |[new-caseholdrule을 제거 합니다.](https://go.microsoft.com/fwlink/p/?LinkId=823820) <br/> |eDiscovery 사례와 관련 된 쿼리 기반 보류가 삭제 되었습니다. 보류 삭제의 결과는 보류에서 쿼리를 제거 하는 경우가 많습니다. 보류 또는 보류 쿼리를 삭제 하면 보류 되었던 콘텐츠 위치가 릴리스됩니다.  <br/> |
|eDiscovery 사례 보류에 대 한 검색 쿼리 변경  <br/> |[new-caseholdrule](https://go.microsoft.com/fwlink/p/?LinkId=823819) <br/> |eDiscovery 사례와 관련 된 쿼리 기반 보류가 변경 되었습니다. 가능한 변경 사항에는 쿼리 기반 보존에 대 한 쿼리 또는 날짜 범위 편집이 포함 됩니다.  <br/> |
|eDiscovery 사례를 만들었습니다.  <br/> |[remove-compliancecase](https://go.microsoft.com/fwlink/p/?LinkId=823842) <br/> |eDiscovery 사례를 만들었습니다. 사례를 만들 때 이름을 지정 하기만 하면 됩니다. 멤버 추가, 보류 만들기, 사례와 연결 된 콘텐츠 검색 만들기 등의 기타 사례 관련 작업은 추가 이벤트가 기록 됩니다.  <br/> |
|삭제 된 eDiscovery 사례  <br/> |[remove-compliancecase을 제거 합니다.](https://go.microsoft.com/fwlink/p/?LinkId=823844) <br/> |eDiscovery 사례가 삭제 되었습니다. 사례를 삭제 하려면 먼저 케이스와 연결 된 보류를 제거 해야 합니다.  <br/> |
|eDiscovery 사례 변경  <br/> |[remove-compliancecase](https://go.microsoft.com/fwlink/p/?LinkId=823846) <br/> |eDiscovery 사례가 변경 되었습니다. 변경 내용에는 미해결 사례 닫기 또는 닫힌 사례 다시 열기가 포함 됩니다.  <br/> |
|eDiscovery 사례에 구성원이 추가 됨  <br/> |[get-compliancecasemember 추가](https://go.microsoft.com/fwlink/p/?LinkId=823848) <br/> |사용자가 eDiscovery 사례의 구성원으로 추가 되었습니다. 사례 구성원으로 서, 사용자는 필요한 권한이 할당 되었는지 여부에 따라 다양 한 사례 관련 작업을 수행할 수 있습니다.  <br/> |
|eDiscovery 사례에서 구성원 제거 됨  <br/> |[get-compliancecasemember을 제거 합니다.](https://go.microsoft.com/fwlink/p/?LinkId=823849) <br/> |사용자가 eDiscovery 사례의 구성원으로 제거 되었습니다.  <br/> |
|eDiscovery 사례 구성원 자격이 변경 됨  <br/> |[업데이트-get-compliancecasemember](https://go.microsoft.com/fwlink/p/?LinkId=823850) <br/> |eDiscovery 사례의 구성원 목록이 변경 되었습니다. 이 작업은 모든 구성원이 새 사용자의 그룹으로 바뀔 때 기록 됩니다. 단일 구성원을 추가 하거나 제거 하는 경우 **get-compliancecasemember** 또는 **get-compliancecasemember** 작업이 기록 됩니다.<br/> |
|만든 콘텐츠 검색  <br/> |[New-ComplianceSearch](https://go.microsoft.com/fwlink/p/?LinkId=517935) <br/> |새 콘텐츠 검색을 만들었습니다.  <br/> |
|삭제 된 콘텐츠 검색  <br/> |[Remove-ComplianceSearch](https://go.microsoft.com/fwlink/p/?LinkId=517936) <br/> |기존 콘텐츠 검색이 삭제 되었습니다.  <br/> |
|변경 된 콘텐츠 검색  <br/> |[Set-ComplianceSearch](https://go.microsoft.com/fwlink/p/?LinkId=517937) <br/> |기존 콘텐츠 검색이 변경 되었습니다. 이러한 변경 사항에는 검색 쿼리를 편집 하거나 편집할 콘텐츠 위치를 추가 하거나 제거 하는 것이 포함 될 수 있습니다.  <br/> |
|시작 콘텐츠 검색  <br/> |[Start-ComplianceSearch](https://go.microsoft.com/fwlink/p/?LinkId=517938) <br/> |콘텐츠 검색을 시작 했습니다. 보안 &amp; 및 준수 센터 GUI를 사용 하 여 콘텐츠 검색을 만들거나 변경 하면 검색이 자동으로 시작 됩니다. **ComplianceSearch** 또는 **ComplianceSearch** cmdlet을 사용 하 여 검색을 만들거나 변경 하는 경우 **ComplianceSearch** cmdlet을 실행 하 여 검색을 시작 해야 합니다.<br/> |
|콘텐츠 검색 중지 됨  <br/> |[Stop-ComplianceSearch](https://go.microsoft.com/fwlink/p/?LinkId=517939) <br/> |실행 중 이었던 콘텐츠 검색을 중지 했습니다.  <br/> |
|만든 콘텐츠 검색 작업  <br/> |[New-ComplianceSearchAction](https://go.microsoft.com/fwlink/p/?LinkId=527971) <br/> |콘텐츠 검색 작업을 만들었습니다. 콘텐츠 검색 작업에는 검색 결과 미리 보기, 검색 결과 내보내기, Office 365 Advanced eDiscovery에서 분석에 대 한 검색 결과 준비, 콘텐츠 검색의 검색 조건과 일치 하는 항목 영구 삭제 등이 포함 됩니다.  <br/> |
|삭제 된 콘텐츠 검색 작업  <br/> |[new-compliancesearchaction을 제거 합니다.](https://go.microsoft.com/fwlink/p/?LinkId=824027) <br/> |콘텐츠 검색 작업이 삭제 되었습니다.  <br/> |
|만든 검색 권한 필터  <br/> |[new-compliancesecurityfilter](https://go.microsoft.com/fwlink/p/?LinkId=617542) <br/> |검색 권한 필터를 만들었습니다.  <br/> |
|삭제 된 검색 권한 필터  <br/> |[new-compliancesecurityfilter을 제거 합니다.](https://go.microsoft.com/fwlink/p/?LinkId=617543) <br/> |검색 권한 필터가 삭제 되었습니다.  <br/> |
|변경 된 검색 권한 필터  <br/> |[new-compliancesecurityfilter](https://go.microsoft.com/fwlink/p/?LinkId=617544) <br/> |검색 권한 필터가 변경 되었습니다.  <br/> |
|eDiscovery 관리자를 만들었습니다.  <br/> |[eDiscoveryCaseAdmin 추가](https://go.microsoft.com/fwlink/p/?LinkId=798217) <br/> |사용자가 조직에서 eDiscovery 관리자로 추가 되었습니다.  <br/> |
|삭제 된 eDiscovery 관리자  <br/> |[eDiscoveryCaseAdmin을 제거 합니다.](https://go.microsoft.com/fwlink/p/?LinkId=823945) <br/> |eDiscovery 관리자가 조직에서 삭제 되었습니다.  <br/> |
|eDiscovery 관리자 멤버 자격 변경  <br/> |[업데이트-eDiscoveryCaseAdmin](https://go.microsoft.com/fwlink/p/?LinkId=823946) <br/> |조직의 eDiscovery 관리자 목록이 변경 되었습니다. 이 작업은 eDiscovery 관리자 목록이 새 사용자의 그룹으로 바뀔 때 기록 됩니다. 단일 사용자를 추가 하거나 제거 하는 경우 **eDiscoveryCaseAdmin** 또는 **eDiscoveryCaseAdmin 제거** 작업이 기록 됩니다.<br/> |
   
## <a name="detailed-properties-for-ediscovery-activities"></a>eDiscovery 작업에 대 한 자세한 속성

다음 표에는 검색 결과에 나열 된 eDiscovery 활동에 대 한 **세부** 정보 페이지에서 **자세한 내용을** 클릭 하면 포함 되는 속성에 대 한 설명이 나와 있습니다. 이러한 속성은 감사 로그 검색 결과를 내보낼 때 CSV 파일에도 포함 됩니다. eDiscovery 활동에 대 한 감사 로그 레코드에는 아래 나열 된 모든 세부 속성이 포함 되지 않습니다. 
  
> [!TIP]
> 검색 결과를 내보낼 때 CSV 파일에는 여러 값 속성의 다음 표에 설명 된 자세한 속성을 포함 하는 **Detail**이라는 열이 포함 되어 있습니다. Excel에서 파워 쿼리 기능을 사용 하 여이 열을 여러 열로 분할 하 여 각 속성에 자체 열을 표시할 수 있습니다. 이렇게 하면 이러한 속성 중 하나 이상을 정렬 및 필터링 할 수 있습니다. 자세한 내용은 [search the audit log in the Office 365 Security & 준수 센터 ](search-the-audit-log-in-security-and-compliance.md#step-4-export-the-search-results-to-a-file)의 "파일로 검색 결과 내보내기" 섹션을 참조 하십시오. 
  
|**속성**|**설명**|
|:-----|:-----|
|사례  <br/> |생성, 변경 또는 삭제 된 eDiscovery 사례의 id (GUID)입니다.  <br/> |
|clientapplication  <br/> |eDiscovery cmdlet 활동에는이 속성에 대 한 값이 **EMC** 로 포함 됩니다. 이는 보안 &amp; 및 준수 센터 GUI를 사용 하 여 작업을 수행한 것을 나타내며 PowerShell에서 cmdlet을 실행 하는 것을 나타냅니다.<br/> |
|ClientIP  <br/> |활동을 로그할 때 사용 된 장치의 IP 주소입니다. IP 주소는 IPv4 또는 IPv6 주소 형식으로 표시 됩니다.  <br/> |
|ClientRequestId  <br/> | eDiscovery 작업의 경우이 속성은 일반적으로 비어 있습니다.  <br/> |
|cmdletversion  <br/> |조직에서 실행 되는 보안 &amp; 준수 센터 버전의 빌드 번호입니다.  <br/> |
|CreationTime  <br/> |eDiscovery 활동이 완료 된 utc (협정 세계시)로 된 날짜와 시간입니다.  <br/> |
|EffectiveOrganization  <br/> |Office 365 조직의 이름입니다.  <br/> |
|ExchangeLocations  <br/> |콘텐츠 검색에 포함 되거나 eDiscovery 사례에서 보류 된 Exchange Online 사서함입니다.  <br/> |
|제외 항목  <br/> |eDiscovery 사례의 콘텐츠 검색 또는 보류에서 제외 되는 사서함 또는 사이트 위치입니다.  <br/> |
|ExtendedProperties  <br/> |콘텐츠 검색의 추가 속성, 콘텐츠 검색 작업 또는 eDiscovery 사례 (예: 개체 GUID, 작업을 수행할 때 사용 된 cmdlet 매개 변수 등)  <br/> |
|Id  <br/> |보고서 항목의 ID입니다. ID는 감사 로그 항목을 고유 하 게 식별 합니다.  <br/> |
|nonpiiparameters  <br/> |Operation 속성에서 식별 한 cmdlet에 사용 된 매개 변수 (값 제외)의 목록입니다. 이 속성에 나열 된 매개 변수는 parameters 속성에 나와 있는 것과 동일 합니다.  <br/> |
|id  <br/> |작업 속성에 나열 된 작업에 의해 만들어지거나, 변경 되거나, 삭제 되는 개체의 GUID 또는 이름 (예: 콘텐츠 검색 또는 eDiscovery 사례)입니다. 이 개체는 감사 로그 검색 결과의 항목 열에도 식별 됩니다.  <br/> |
|ObjectType  <br/> |사용자가 만들거나 삭제 하거나 수정한 eDiscovery 개체의 유형입니다. 예를 들어 콘텐츠 검색 작업 (미리 보기, 내보내기 또는 삭제), eDiscovery 사례 또는 콘텐츠 검색 등이 있습니다.  <br/> |
|작업  <br/> |수행한 eDiscovery 활동에 해당 하는 작업의 이름입니다.  <br/> |
|조직 id  <br/> |Office 365 조 직의 GUID입니다.  <br/> |
|매개 변수  <br/> |해당 cmdlet에 사용 된 매개 변수의 이름 및 값입니다.  <br/> |
|publicfolderlocations  <br/> |콘텐츠 검색에 포함 되거나 eDiscovery 사례에 유지 되는 Exchange Online의 공용 폴더 위치입니다.  <br/> |
|쿼리  <br/> |활동에 연결 된 검색 쿼리 (예: 콘텐츠 검색 또는 쿼리 기반 유지)  <br/> |
|RecordType  <br/> |record에서 지정한 작업의 유형입니다. **18** 값은 [eDiscovery cmdlet 작업](#ediscovery-cmdlet-activities) 섹션에 나열 된 작업과 관련 된 이벤트를 나타냅니다. 값이 **24** 이면 [eDiscovery 활동 검색 및 보기](#how-to-search-for-and-view-ediscovery-activities) 섹션에 나열 된 작업과 관련 된 이벤트를 나타냅니다.<br/> |
|resultstatus  <br/> |작업 속성에 지정 된 작업이 성공 했는지 여부를 나타냅니다.  <br/> |
|SecurityComplianceCenterEventType  <br/> |작업이 보안 &amp; 및 준수 센터 이벤트 임을 나타냅니다. 이 속성의 경우 모든 eDiscovery 활동 값은 **0** 입니다.<br/> |
|SharepointLocations  <br/> |콘텐츠 검색에 포함 되거나 eDiscovery 사례에서 보류 되는 SharePoint Online 사이트입니다.  <br/> |
|StartTime  <br/> |eDiscovery 활동이 시작 된 시간을 utc (협정 세계시)로 된 날짜와 시간입니다.  <br/> |
|UserId  <br/> |작업 속성에 지정 된 활동을 수행한 사용자가 레코드를 기록 합니다. 시스템 계정 (예: NT 권한 \ 컴퓨터)에서 수행한 eDiscovery 작업에 대 한 레코드는 감사 로그에도 포함 되어 있습니다.  <br/> |
|userkey  <br/> |UserId 속성에서 식별 된 사용자의 대체 ID입니다. eDiscovery 작업의 경우이 속성 값은 일반적으로 UserId 속성과 동일 합니다.  <br/> |
|userserviceplan  <br/> |조직에서 사용 하는 Office 365 구독 eDiscovery 작업의 경우이 속성은 일반적으로 비어 있습니다.  <br/> |
|UserType  <br/> |작업을 수행한 사용자의 유형입니다. 다음 값은 사용자 형식을 나타냅니다.  <br/> 0 일반 사용자입니다. 2 Office 365 조직의 관리자입니다. 3 A Microsoft 데이터 센터 관리자 또는 데이터 센터 시스템 계정입니다. 4 시스템 계정입니다. 5 응용 프로그램 6 서비스 사용자 |
|Version  <br/> |기록 된 작업의 버전 번호 (Operation 속성으로 식별 됨)를 나타냅니다.  <br/> |
|작업량  <br/> |활동이 발생 한 Office 365 서비스입니다. eDiscovery 활동의 경우이 값은 **SecurityComplianceCenter**입니다.<br/> |
