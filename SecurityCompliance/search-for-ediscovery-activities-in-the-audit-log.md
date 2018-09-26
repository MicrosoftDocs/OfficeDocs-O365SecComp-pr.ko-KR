---
title: Office 365 감사 로그에서 eDiscovery 활동에 대 한 검색
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 10/24/2017
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid: MOE150
ms.assetid: 67cc7f42-a53d-4751-b929-6005c80798f7
description: 규정 준수 관리자 보안에서 콘텐츠 검색 및 eDiscovery 사례 작업을 수행 하는 경우 로깅되는 이벤트를 위한 Office 365 감사 로그를 검색 하는 방법에 알아봅니다 &amp; 준수 센터입니다.
ms.openlocfilehash: a4cc3a6b5030a6412d739236e4c534f36948d57f
ms.sourcegitcommit: 7956955cd919f6e00b64e4506605a743c5872549
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/26/2018
ms.locfileid: "25038351"
---
# <a name="search-for-ediscovery-activities-in-the-office-365-audit-log"></a>Office 365 감사 로그에서 eDiscovery 활동에 대 한 검색

콘텐츠 검색 및 수행 하는 Office 365 보안의 eDiscovery 관련 작업을 &amp; 준수 센터 또는 해당 Windows PowerShell을 실행 하 여 cmdlet은 Office 365 감사 로그에 기록 됩니다. 관리자 또는 규정 준수 관리자 (또는 모든 사용자가 할당 된 eDiscovery 사용 권한) Office 365 보안에서 다음과 같은 콘텐츠 검색 및 eDiscovery 관련 작업 수행 이벤트 로그에 기록 됩니다 &amp; 준수 센터:
  
- 만들기 (영문) 및 eDiscovery 사례 관리
    
- 만들기 (영문), 시작 및 콘텐츠 검색을 편집 합니다.
    
- 내보내기 및 삭제의 검색 결과 미리 보기 등의 콘텐츠 검색 작업을 수행 합니다.
    
- 콘텐츠 검색에 대 한 필터링 하는 사용 권한 구성
    
- EDiscovery 관리자 역할 관리
    
> [!IMPORTANT]
> 이 문서에 설명 된 작업은 보안을 사용 하 여 수행 하는 eDiscovery 작업의 결과만 &amp; 준수 센터입니다. Exchange Online 또는 SharePoint Online에서 eDiscovery 센터의 원본 위치 eDiscovery 도구를 사용 하 여 수행 된 eDiscovery 작업에 포함 되지 않습니다. 
  
Office 365 감사 로그를 검색 하는 방법에 대 한 자세한 내용은 사용 권한 있는 필요한, 하 고 검색 결과 내보내기 (영문) 참조 [Office 365 보안에서 감사 로그를 검색 &amp; 준수 센터](search-the-audit-log-in-security-and-compliance.md)합니다.
  
## <a name="how-to-search-for-and-view-ediscovery-activities"></a>검색 하는 방법 및 eDiscovery 활동 보기

현재 Office 365 감사 로그에서 eDiscovery 활동을 볼 수는 몇 특정 작업을 수행 해야 합니다. 다음은 방법입니다.
  
1. [https://protection.office.com](https://protection.office.com)으로 이동합니다.
    
2. 작업이 나 교육용 계정을 사용 하 여 Office 365에 로그인 합니다.
    
3. 왼쪽된 창에서 클릭 **검색 &amp; 조사**, **감사 로그 검색**을 클릭 하 고 있습니다.
    
4. **활동** 드롭다운 목록에서 **eDiscovery 활동**하나 이상의 작업에 대 한 검색을 클릭 합니다. 또는 모든 eDiscovery 관련 활동에 대 한 검색을 **eDiscovery 활동** 클릭할 수 있습니다. 
    
    > [!NOTE]
    > 활동 드롭다운 목록에는 cmdlet 감사 로그에서 레코드를 반환 하는 **eDiscovery cmdlet 활동** 이라는 작업 그룹을 포함 됩니다. 
  
5.  해당 기간 내에 발생 하는 eDiscovery 이벤트를 표시 하는 날짜 및 시간 범위를 선택 합니다. 
    
6. **사용자** 상자에 대 한 검색 결과 표시 하려면 하나 이상의 사용자를 선택 합니다. 이 상자는 모든 사용자에 대 한 항목의 인덱스 번호를 비워 둡니다. 
    
7. 검색 조건을 사용 하 여 검색을 실행 하려면 **검색** 클릭 합니다. 
    
8. 검색 결과 표시 한 후에 **필터 결과** 필터링 하거나 결과 활동 레코드를 정렬 하려면 클릭 수 있습니다. 그러나 수는 없습니다 필터링을 사용 하면 특정 활동을 명시적으로 제외 하도록 합니다. 
    
9. 활동에 대 한 세부 정보를 보려면 검색 결과의 목록에서 활동 레코드를 클릭 합니다. 
    
    페이지에는 **세부 정보** 날아가기 이벤트 레코드에서 자세한 속성을 포함 하는 표시 됩니다. 추가 세부 정보를 표시 하기 위해 **추가 정보**를 클릭 합니다. 이러한 속성에 대 한 [eDiscovery 활동에 대 한 자세한 속성](#detailed-properties-for-ediscovery-activities) 섹션을 참조 합니다. 

  
## <a name="ediscovery-activities"></a>eDiscovery 활동

다음 표에서 콘텐츠 검색 및 관리자 또는 사용자가 보안을 사용 하 여 eDiscovery 관련 활동을 수행할 때 로깅되는 eDiscovery 관련 작업을 &amp; 준수 센터 또는 해당 cmdlet을 실행 하 여 조직의 보안에 연결 된 원격 PowerShell &amp; 준수 센터입니다. 
  
> [!NOTE]
> 이 섹션에 설명 된 eDiscovery 활동의 다음 섹션에 설명 된 eDiscovery cmdlet 활동에 비슷한 정보를 제공 합니다. 30 분 이내 감사 로그 검색 결과에 나타나지 않기 때문에이 섹션에 설명 된 eDiscovery 활동을 사용 하는 것이 좋습니다. 감사 로그 검색 결과에 표시 하는 cmdlet 활동 eDiscovery 24 시간까지 걸립니다. 
  
|**이름**|**Operation**|**해당 cmdlet**|**설명**|
|:-----|:-----|:-----|:-----|
|EDiscovery 사례에 추가 된 구성원  <br/> |CaseMemberAdded  <br/> |추가 ComplianceCaseMember  <br/> |사용자는 eDiscovery 사례의 구성원으로 추가 되었습니다. 사용자는 사례의 멤버로 필요한 사용 권한을 할당 되었는지 여부에 따라 다양 한 대/소문자와 관련 된 작업을 수행할 수 있습니다.  <br/> |
|변경 된 콘텐츠 검색  <br/> |SearchUpdated  <br/> |Set-ComplianceSearch  <br/> |기존 콘텐츠 검색 변경 되었습니다. 추가 (영문) 또는 콘텐츠 위치를 제거 하거나 검색 쿼리를 편집 변경 내용이 포함할 수 있습니다.  <br/> |
|변경 된 eDiscovery 관리자 구성원 자격  <br/> |CaseAdminUpdated  <br/> |업데이트 eDiscoveryCaseAdmin  <br/> |조직에서 eDiscovery 관리자의 목록 변경 되었습니다. 이 작업의 새 사용자 그룹과 eDiscovery 관리자의 목록 바꿀 때 기록 됩니다. 한 명의 사용자를 추가 하거나 제거 하는 경우에 CaseAdminAdded 작업 기록 됩니다.  <br/> |
|변경 된 eDiscovery 사례  <br/> |CaseUpdated  <br/> |집합 ComplianceCase  <br/> |EDiscovery 사례 변경 되었습니다. 변경 내용을 열려있는 사례를 닫는 또는 닫힌된 사례를 다시 열를 포함 합니다.  <br/> |
|변경 된 eDiscovery 사례 멤버 자격  <br/> |CaseMemberUpdated  <br/> |업데이트 ComplianceCaseMember  <br/> |EDiscovery 사례의 구성원 목록 변경 되었습니다. 모든 구성원은 새 사용자의 그룹으로 바뀌고이 활동 기록 됩니다. 단일 구성원을 추가 하거나 제거 하는 경우에 CaseMemberAdded 또는 CaseMemberRemoved 작업 기록 됩니다.  <br/> |
|검색 사용 권한 필터를 변경합니다.  <br/> |SearchPermissionUpdated  <br/> |집합 ComplianceSecurityFilter  <br/> |검색 사용 권한 필터 변경 되었습니다.  <br/> |
|EDiscovery 사례 보류에 대 한 변경 된 검색 쿼리  <br/> |HoldUpdated  <br/> |집합 CaseHoldRule  <br/> |EDiscovery 사례와 관련 된 쿼리 기반 보류 변경 되었습니다. 쿼리를 편집 가능한 값은 다음과 또는 쿼리 기반에 대 한 날짜 범위를 유지 합니다.  <br/> |
|콘텐츠 검색 미리 보기 항목을 다운로드  <br/> |PreviewItemDownloaded  <br/> |해당 없음  <br/> |사용자 항목을 다운로드 자신의 로컬 컴퓨터 ( **원본 항목을 다운로드** 링크를 클릭) 하 여 때 검색 결과 미리볼 합니다.  <br/> |
|콘텐츠 검색 미리 보기 항목 나열  <br/> |PreviewItemListed  <br/> |해당 없음  <br/> |사용자가 콘텐츠 검색 결과에서 최대 1000 개의 항목을 나열 하는 미리 보기 검색 결과 페이지를 표시 하려면 **검색 결과 미리 보기** 클릭 합니다.  <br/> |
|콘텐츠 검색 미리 보기 항목 표시  <br/> |PreviewItemRendered  <br/> |해당 없음  <br/> |EDiscovery 관리자는 검색 결과 미리볼 때 클릭 하 여 항목을 표시 합니다.  <br/> |
|만든된 콘텐츠 검색  <br/> |SearchCreated  <br/> |New-ComplianceSearch  <br/> |새로운 콘텐츠 검색을 만들었습니다.  <br/> |
|만든된 eDiscovery 관리자  <br/> |CaseAdminAdded  <br/> |추가 eDiscoveryCaseAdmin  <br/> |사용자는 조직에서 eDiscovery 관리자 권한으로 추가 되었습니다.  <br/> |
|만든된 eDiscovery 사례  <br/> |CaseAdded  <br/> |새 ComplianceCase  <br/> |EDiscovery 사례를 만들었습니다. 사례를 만들 때 이름을 지정 해야 합니다. 구성원 추가 (영문), 유지 만들기 (영문)에 기록 되는 추가 이벤트 사례 결과와 관련 된 콘텐츠 검색 만들기 (영문)와 같은 다른 사례와 관련 된 작업 합니다.  <br/> |
|검색 사용 권한 필터를 생성합니다.  <br/> |SearchPermissionCreated  <br/> |새 ComplianceSecurityFilter  <br/> |검색 사용 권한 필터를 만들었습니다.  <br/> |
|EDiscovery 사례 보류에 대 한 만든된 검색 쿼리  <br/> |HoldCreated  <br/> |새 CaseHoldRule  <br/> |EDiscovery 사례와 관련 된 쿼리 기반 보류를 만들었습니다.  <br/> |
|삭제 된 콘텐츠 검색  <br/> |SearchRemoved  <br/> |Remove-ComplianceSearch  <br/> |기존 콘텐츠 검색 삭제 되었습니다.  <br/> |
|삭제 된 eDiscovery 관리자  <br/> |CaseAdminRemoved  <br/> |EDiscoveryCaseAdmin 제거  <br/> |EDiscovery 관리자가 조직에서 삭제 되었습니다.  <br/> |
|삭제 된 eDiscovery 사례  <br/> |CaseRemoved  <br/> |ComplianceCase 제거  <br/> |EDiscovery 사례 삭제 되었습니다. 대/소문자와 관련 된 모든 보류에서 대/소문자를 삭제할 수 있습니다를 먼저 제거 하는 메모 합니다.  <br/> |
|삭제 된 검색 권한 필터  <br/> |SearchPermissionRemoved  <br/> |ComplianceSecurityFilter 제거  <br/> |검색 사용 권한 필터 삭제 되었습니다.  <br/> |
|EDiscovery 사례 보류에 대 한 삭제 된 검색 쿼리  <br/> |HoldRemoved  <br/> |CaseHoldRule 제거  <br/> |EDiscovery 사례와 관련 된 쿼리 기반 보류 삭제 되었습니다. 보류를 삭제 결과 자주은 보류에서 쿼리를 제거 합니다. 보류 또는 대기 쿼리를 삭제 하는 경우에 대기 했던 콘텐츠 위치는 해제 됩니다.  <br/> |
|콘텐츠 검색의 다운로드 한 내보내기  <br/> |SearchResultDownloaded  <br/> |해당 없음  <br/> |사용자가 자신의 로컬 컴퓨터에 콘텐츠 검색의 결과 다운로드 합니다. 검색 결과 다운로드할 수 있습니다 전에 시작 하려면 **시작 콘텐츠 검색의 내보내기** 활동 되어있는지 note 합니다.<br/> |
|콘텐츠 검색의 미리 보기 결과  <br/> |SearchPreviewed  <br/> |해당 없음  <br/> |사용자는 콘텐츠 검색의 결과를 미리봅니다.  <br/> |
|제거 된 콘텐츠 검색 결과  <br/> |SearchResultsPurged  <br/> |New-ComplianceSearchAction  <br/> |사용자를 실행 하 여 콘텐츠 검색의 결과 지울는 **새로 ComplianceSearchAction-항목 지우기** 명령 합니다.  <br/> |
|콘텐츠 검색의 제거 된 분석  <br/> |RemovedSearchResultsSentToZoom  <br/> |ComplianceSearchAction 제거  <br/> |콘텐츠 검색 준비 작업 (Office 365 고급 eDiscovery에 대 한 검색 결과 준비) 삭제 되었습니다. 준비 작업에는 2 주 했으므로, 고급 eDiscovery에 대해 준비 된 검색 결과 Microsoft Azure 저장소 영역에서 삭제 되었습니다. 준비 작업을 2 주 보다 오래 된 경우이 이벤트는 해당 준비 작업에만 삭제 되었음을 나타냅니다 다음 합니다.  <br/> |
|콘텐츠 검색의 제거 된 내보내기  <br/> |RemovedSearchExported  <br/> |ComplianceSearchAction 제거  <br/> |콘텐츠 검색 내보내기 작업을 삭제 되었습니다. 내보내기 작업 했으므로 2 주, Microsoft Azure 저장소 영역에 업로드 된 검색 결과 삭제 되었습니다. 내보내기 작업을 2 주 보다 오래 된 경우이 이벤트만 해당 되는 내보내기 작업 삭제 되었음을 나타냅니다 합니다.  <br/> |
|EDiscovery 사례에서 제거 된 구성원  <br/> |CaseMemberRemoved  <br/> |ComplianceCaseMember 제거  <br/> |사용자는 eDiscovery 사례의 구성원으로 제거 되었습니다.  <br/> |
|콘텐츠 검색의 결과 미리 보기를 제거합니다.  <br/> |RemovedSearchPreviewed  <br/> |ComplianceSearchAction 제거  <br/> |콘텐츠 검색 미리 보기 작업을 삭제 되었습니다.  <br/> |
|콘텐츠 검색에서 제거 된 삭제 작업을 수행  <br/> |RemovedSearchResultsPurged  <br/> |ComplianceSearchAction 제거  <br/> |콘텐츠 검색 삭제 작업을 삭제 되었습니다.  <br/> |
|검색 보고서를 제거합니다.  <br/> |SearchReportRemoved  <br/> |ComplianceSearchAction 제거  <br/> |콘텐츠 검색 작업 삭제 된 보고서를 내보냅니다.  <br/> |
|콘텐츠 검색의 시작된 분석  <br/> |SearchResultsSentToZoom  <br/> |New-ComplianceSearchAction  <br/> |콘텐츠 검색의 결과 고급 eDiscovery에 대 한 분석을 위해 준비 되었습니다.  <br/> |
|콘텐츠 검색 시작  <br/> |SearchStarted  <br/> |Start-ComplianceSearch  <br/> |콘텐츠 검색을 시작 했습니다. 만들 하거나 보안을 사용 하 여 콘텐츠 검색을 변경 하면 &amp; 준수 센터 GUI, 검색 자동으로 시작 됩니다. 만들거나 **새로 ComplianceSearch** 또는 **집합 ComplianceSearch** cmdlet을 사용 하 여 검색을 변경 하는 경우 검색을 시작 하려면 **시작 ComplianceSearch** cmdlet을 실행 해야 합니다.<br/> |
|콘텐츠 검색의 시작된 내보내기  <br/> |SearchExported  <br/> |New-ComplianceSearchAction  <br/> |사용자는 콘텐츠 검색의 결과 내보냅니다.  <br/> |
|시작된 내보내기 보고서  <br/> |SearchReport  <br/> |New-ComplianceSearchAction  <br/> |사용자는 콘텐츠 검색 보고서를 내보냅니다.  <br/> |
|콘텐츠 검색을 중지  <br/> |SearchStopped  <br/> |Stop-ComplianceSearch  <br/> |사용자가 콘텐츠 검색을 중지 합니다.  <br/> |
  
## <a name="ediscovery-cmdlet-activities"></a>eDiscovery cmdlet 활동

다음 표에서 관리자 또는 사용자가 보안을 사용 하 여 eDiscovery 관련 활동을 수행할 때 로깅되는 cmdlet 감사 로그 레코드 &amp; 준수 센터 또는 원격 PowerShell에서 해당 cmdlet을 실행 하 여의 조직의 보안에 연결 된 &amp; 준수 센터입니다. 감사 로그 레코드에 자세한 정보가이 표에 나열 된 cmdlet 작업과 이전 섹션에 설명 된 eDiscovery 활동에 대 한 서로 다른 지 note 합니다. 
  
앞서 설명한 것 처럼 걸리는 eDiscovery 24 시간까지 cmdlet 활동 감사 로그 검색 결과에 표시 합니다.
  
> [!TIP]
> 다음 표의 **작업** 열에서 cmdlet은 TechNet에서 해당 cmdlet 도움말 항목에 연결 됩니다. 각 cmdlet에 대 한 사용 가능한 매개 변수에 대 한 설명은 cmdlet 도움말 항목으로 이동 합니다. 매개 변수는 및 cmdlet을 함께 사용 된 매개 변수 값은 기록 된 각 eDiscovery cmdlet 활동에 대 한 감사 로그 항목에 포함 됩니다. 
  
|**이름**|**작업 (cmdlet)**|**설명**|
|:-----|:-----|:-----|
|EDiscovery 사례에서 만든된 보류  <br/> |[새 CaseHoldPolicy](https://go.microsoft.com/fwlink/p/?LinkId=823813) <br/> |EDiscovery 사례에 대 한 보류를 만들었습니다. 또는 콘텐츠 원본을 지정 하지 않고 보류를 만들 수 있습니다. 콘텐츠 원본을 지정 된 감사 로그 항목에 식별 됩니다.  <br/> |
|EDiscovery 사례에서 삭제 된 보류  <br/> |[CaseHoldPolicy 제거](https://go.microsoft.com/fwlink/p/?LinkId=823814) <br/> |EDiscovery 사례와 연결 된 보류 삭제 되었습니다. 삭제 보류의 모든 보류에서 콘텐츠 위치를 해제 합니다. 삭제 보류와 관련 된 경우 대기 규칙의 결과가 보류를도 삭제 ( **제거 CaseHoldRule** 아래 참조).<br/> |
|EDiscovery 사례에서 변경 된 보류  <br/> |[집합 CaseHoldPolicy](https://go.microsoft.com/fwlink/p/?LinkId=823815) <br/> |EDiscovery와 연결 된 보류 변경 되었습니다. 가능한 값은 다음과 추가 (영문) 또는 콘텐츠 위치를 제거 하거나 기능을 해제 (사용 안함) 보류 합니다.  <br/> |
|EDiscovery 사례 보류에 대 한 만든된 검색 쿼리  <br/> |[새 CaseHoldRule](https://go.microsoft.com/fwlink/p/?LinkId=823816) <br/> |EDiscovery 사례와 관련 된 쿼리 기반 보류를 만들었습니다.  <br/> |
|EDiscovery 사례 보류에 대 한 삭제 된 검색 쿼리  <br/> |[CaseHoldRule 제거](https://go.microsoft.com/fwlink/p/?LinkId=823820) <br/> |EDiscovery 사례와 관련 된 쿼리 기반 보류 삭제 되었습니다. 보류를 삭제 결과 자주은 보류에서 쿼리를 제거 합니다. 보류 또는 대기 쿼리를 삭제 하는 경우에 대기 했던 콘텐츠 위치는 해제 됩니다.  <br/> |
|EDiscovery 사례 보류에 대 한 변경 된 검색 쿼리  <br/> |[집합 CaseHoldRule](https://go.microsoft.com/fwlink/p/?LinkId=823819) <br/> |EDiscovery 사례와 관련 된 쿼리 기반 보류 변경 되었습니다. 쿼리를 편집 가능한 값은 다음과 또는 쿼리 기반에 대 한 날짜 범위를 유지 합니다.  <br/> |
|만든된 eDiscovery 사례  <br/> |[새 ComplianceCase](https://go.microsoft.com/fwlink/p/?LinkId=823842) <br/> |EDiscovery 사례를 만들었습니다. 사례를 만들 때 이름을 지정 해야 합니다. 구성원 추가 (영문), 유지 만들기 (영문)에 기록 되는 추가 이벤트 사례 결과와 관련 된 콘텐츠 검색 만들기 (영문)와 같은 다른 사례와 관련 된 작업 합니다.  <br/> |
|삭제 된 eDiscovery 사례  <br/> |[ComplianceCase 제거](https://go.microsoft.com/fwlink/p/?LinkId=823844) <br/> |EDiscovery 사례 삭제 되었습니다. 대/소문자와 관련 된 모든 보류에서 대/소문자를 삭제할 수 있습니다를 먼저 제거 하는 메모 합니다.  <br/> |
|변경 된 eDiscovery 사례  <br/> |[집합 ComplianceCase](https://go.microsoft.com/fwlink/p/?LinkId=823846) <br/> |EDiscovery 사례 변경 되었습니다. 변경 내용을 열려있는 사례를 닫는 또는 닫힌된 사례를 다시 열를 포함 합니다.  <br/> |
|EDiscovery 사례에 추가 된 구성원  <br/> |[추가 ComplianceCaseMember](https://go.microsoft.com/fwlink/p/?LinkId=823848) <br/> |사용자는 eDiscovery 사례의 구성원으로 추가 되었습니다. 사용자는 사례의 멤버로 필요한 사용 권한을 할당 되었는지 여부에 따라 다양 한 대/소문자와 관련 된 작업을 수행할 수 있습니다.  <br/> |
|EDiscovery 사례에서 제거 된 구성원  <br/> |[ComplianceCaseMember 제거](https://go.microsoft.com/fwlink/p/?LinkId=823849) <br/> |사용자는 eDiscovery 사례의 구성원으로 제거 되었습니다.  <br/> |
|변경 된 eDiscovery 사례 멤버 자격  <br/> |[업데이트 ComplianceCaseMember](https://go.microsoft.com/fwlink/p/?LinkId=823850) <br/> |EDiscovery 사례의 구성원 목록 변경 되었습니다. 모든 구성원은 새 사용자의 그룹으로 바뀌고이 활동 기록 됩니다. 단일 구성원을 추가 하거나 제거 하는 경우에 **ComplianceCaseMember 추가** 또는 **제거 ComplianceCaseMember** 작업 기록 됩니다.<br/> |
|만든된 콘텐츠 검색  <br/> |[New-ComplianceSearch](https://go.microsoft.com/fwlink/p/?LinkId=517935) <br/> |새로운 콘텐츠 검색을 만들었습니다.  <br/> |
|삭제 된 콘텐츠 검색  <br/> |[Remove-ComplianceSearch](https://go.microsoft.com/fwlink/p/?LinkId=517936) <br/> |기존 콘텐츠 검색 삭제 되었습니다.  <br/> |
|변경 된 콘텐츠 검색  <br/> |[Set-ComplianceSearch](https://go.microsoft.com/fwlink/p/?LinkId=517937) <br/> |기존 콘텐츠 검색 변경 되었습니다. 추가 또는 검색 되는 콘텐츠 위치를 제거 하 고, 검색 쿼리를 편집 변경 내용이 포함할 수 있습니다.  <br/> |
|콘텐츠 검색 시작  <br/> |[Start-ComplianceSearch](https://go.microsoft.com/fwlink/p/?LinkId=517938) <br/> |콘텐츠 검색을 시작 했습니다. 만들 하거나 보안을 사용 하 여 콘텐츠 검색을 변경 하면 &amp; 준수 센터 GUI, 검색 자동으로 시작 됩니다. 만들거나 **새로 ComplianceSearch** 또는 **집합 ComplianceSearch** cmdlet을 사용 하 여 검색을 변경 하는 경우 검색을 시작 하려면 **시작 ComplianceSearch** cmdlet을 실행 해야 합니다.<br/> |
|콘텐츠 검색을 중지  <br/> |[Stop-ComplianceSearch](https://go.microsoft.com/fwlink/p/?LinkId=517939) <br/> |실행 중이 던 콘텐츠 검색을 중지 되었습니다.  <br/> |
|콘텐츠 검색 작업을 만든  <br/> |[New-ComplianceSearchAction](https://go.microsoft.com/fwlink/p/?LinkId=527971) <br/> |콘텐츠 검색 작업을 만들었습니다. 콘텐츠 검색 작업 등이 검색 결과 미리 보거나, 검색 결과 내보내기 (영문), 검색 결과 준비 하 고 Office 365 고급 eDiscovery에 대 한 분석을 위해 콘텐츠 검색의 검색 조건과 일치 하는 항목을 영구적으로 삭제 합니다.  <br/> |
|삭제 된 콘텐츠 검색 작업  <br/> |[ComplianceSearchAction 제거](https://go.microsoft.com/fwlink/p/?LinkId=824027) <br/> |콘텐츠 검색 작업을 삭제 되었습니다.  <br/> |
|검색 사용 권한 필터를 생성합니다.  <br/> |[새 ComplianceSecurityFilter](https://go.microsoft.com/fwlink/p/?LinkId=617542) <br/> |검색 사용 권한 필터를 만들었습니다.  <br/> |
|삭제 된 검색 권한 필터  <br/> |[ComplianceSecurityFilter 제거](https://go.microsoft.com/fwlink/p/?LinkId=617543) <br/> |검색 사용 권한 필터 삭제 되었습니다.  <br/> |
|검색 사용 권한 필터를 변경합니다.  <br/> |[집합 ComplianceSecurityFilter](https://go.microsoft.com/fwlink/p/?LinkId=617544) <br/> |검색 사용 권한 필터 변경 되었습니다.  <br/> |
|만든된 eDiscovery 관리자  <br/> |[추가 eDiscoveryCaseAdmin](https://go.microsoft.com/fwlink/p/?LinkId=798217) <br/> |사용자는 조직에서 eDiscovery 관리자 권한으로 추가 되었습니다.  <br/> |
|삭제 된 eDiscovery 관리자  <br/> |[EDiscoveryCaseAdmin 제거](https://go.microsoft.com/fwlink/p/?LinkId=823945) <br/> |EDiscovery 관리자가 조직에서 삭제 되었습니다.  <br/> |
|변경 된 eDiscovery 관리자 구성원 자격  <br/> |[업데이트 eDiscoveryCaseAdmin](https://go.microsoft.com/fwlink/p/?LinkId=823946) <br/> |조직에서 eDiscovery 관리자의 목록 변경 되었습니다. 이 작업의 새 사용자 그룹과 eDiscovery 관리자의 목록 바꿀 때 기록 됩니다. 한 명의 사용자를 추가 하거나 제거 하는 경우에 **eDiscoveryCaseAdmin 추가** 또는 **제거 eDiscoveryCaseAdmin** 작업 기록 됩니다.<br/> |
   
## <a name="detailed-properties-for-ediscovery-activities"></a>EDiscovery 활동에 대 한 자세한 속성

다음 표에서 검색 결과에 나열 된 eDiscovery 활동에 대 한 **세부 정보** 페이지에서 **자세한 정보** 를 클릭 하면 포함 된 속성을 설명 합니다. 이러한 속성은 감사 로그 검색 결과 내보낼 때에 CSV 파일에 포함 됩니다. 참고 eDiscovery 활동에 대 한 감사 로그 레코드를 아래에 나열 된 모든 세부 속성을 포함 하지 않습니다. 
  
> [!TIP]
> 검색 결과 내보낼 때 CSV 파일 **세부 정보**, 다중값 속성에는 다음 표에 설명 된 세부 속성을 포함 하는 명명 된 열을 포함 합니다. Excel에서이 열을 여러 열으로 분할 하 각 속성에는 자체 열 가지게 됩니다 파워 쿼리 기능을 사용할 수 있습니다. 이렇게 하면 이러한 속성 중 하나 이상이에서 정렬 및 필터링 있습니다. 자세한 내용은 [Office 365 보안 및 규정 준수 센터에서 감사 로그 검색 ](search-the-audit-log-in-security-and-compliance.md#step-4-export-the-search-results-to-a-file)에 "파일을 검색 결과 내보내기" 섹션을 참조 하십시오. 
  
|**속성**|**설명**|
|:-----|:-----|
|사례  <br/> |작성, 변경 또는 삭제 된 하는 eDiscovery 사례의 id (GUID)입니다.  <br/> |
|ClientApplication  <br/> |eDiscovery cmdlet 활동 **EMC** 의이 속성 값이 포함 됩니다. 보안을 사용 하 여 작업을 수행한 나타냅니다 &amp; 준수 센터 GUI 또는 powershell에서 cmdlet을 실행 합니다.<br/> |
|ClientIP  <br/> |작업 기록 되었는지 때 사용 된 장치의 IP 주소입니다. IP 주소는 IPv4 또는 IPv6 주소 형식으로 표시 됩니다.  <br/> |
|ClientRequestId  <br/> | EDiscovery 활동에 대 한이 속성은 일반적으로 비어 있습니다.  <br/> |
|CmdletVersion  <br/> |버전의 보안에 대 한 빌드 번호 &amp; 준수 센터 조직에서 실행 합니다.  <br/> |
|CreationTime  <br/> |날짜 및 시간에서 UTC Coordinated Universal Time () eDiscovery 활동이 완료 되었을 때입니다.  <br/> |
|EffectiveOrganization  <br/> |이름의 Office 365 조직입니다.  <br/> |
|ExchangeLocations  <br/> |EDiscovery 사례에 콘텐츠 검색에 포함 되거나에 배치 되는 Exchange Online 사서함 보류 합니다.  <br/> |
|제외  <br/> |사서함 또는 사이트 위치에 콘텐츠 검색 또는 eDiscovery 사례에 보류에서 제외 됩니다.  <br/> |
|ExtendedProperties  <br/> |추가 속성을 콘텐츠에서 검색, 콘텐츠 검색 작업을 또는 유지 (영문) 개체 GUID와 같은 eDiscovery 사례, 해당 cmdlet 및 작업을 수행할 때 사용 된 cmdlet 매개 변수입니다.  <br/> |
|Id  <br/> |보고서 항목의 ID입니다. ID는 감사 로그 항목을 고유 하 게 식별 합니다.  <br/> |
|NonPIIParameters  <br/> |목록 작업 속성에서 확인 된 cmdlet과 함께 사용 된 모든 값) (없이 매개 변수입니다. 이 속성에 나열 된 매개 변수는 Parameters 속성에 나열 된 것과 동일 합니다.  <br/> |
|ObjectId  <br/> |작성, 변경 또는 작업 속성에 나열 된 활동에 의해 삭제 된 개체 (예: 콘텐츠 검색 또는 eDiscovery 사례)의 이름 또는 GUID입니다. 이 개체는 또한 감사 로그 검색 결과에서 항목 열에서 식별 됩니다.  <br/> |
|ObjectType  <br/> |사용자 작성, 삭제 또는 수정; eDiscovery 개체의 유형 예 (미리 보기, 내보내기 또는 지우기) 콘텐츠 검색 작업을, eDiscovery 사례, 또는 콘텐츠를 검색 합니다.  <br/> |
|작업  <br/> |수행 된 eDiscovery 활동에 해당 하는 작업의 이름입니다.  <br/> |
|OrganizationId  <br/> |Office 365 조직에 대 한 GUID입니다.  <br/> |
|매개 변수  <br/> |이름 및 해당 cmdlet과 함께 사용 된 매개 변수에 대 한 값입니다.  <br/> |
|PublicFolderLocations  <br/> |Exchange online 콘텐츠 검색에 포함 되거나에 배치 하는 공용 폴더 위치 eDiscovery 사례에서 대기 합니다.  <br/> |
|쿼리  <br/> |예: 콘텐츠 검색 또는 쿼리 기반 보존 작업과 관련 된 검색 쿼리 합니다.  <br/> |
|RecordType  <br/> |레코드에 지정 된 작업의 형식입니다. **18** 값 [eDiscovery cmdlet 활동](#ediscovery-cmdlet-activities) 섹션에 나열 된 활동에 관련 된 이벤트를 나타냅니다. **24** 의 값을 [검색 하는 방법 및 보기 eDiscovery 작업](#how-to-search-for-and-view-ediscovery-activities) 섹션에 나열 된 활동에 관련 된 이벤트를 나타냅니다.<br/> |
|ResultStatus  <br/> |(Operation 속성에 지정 된) 작업 성공 했는지 여부를 나타냅니다.  <br/> |
|SecurityComplianceCenterEventType  <br/> |활동을 보안 했음을 나타냅니다 &amp; 준수 센터 이벤트입니다. 모든 eDiscovery 활동을 **0** 이 속성의 값을 갖습니다.<br/> |
|SharepointLocations  <br/> |EDiscovery 사례에 콘텐츠 검색에 포함 되거나에 배치 하는 SharePoint Online 사이트를 보관 합니다.  <br/> |
|StartTime  <br/> |날짜 및 시간에서 UTC Coordinated Universal Time () eDiscovery 활동이 시작 된 경우입니다.  <br/> |
|사용자 Id  <br/> |기록 되는 레코드를 발생 시킨 (Operation 속성에 지정 된) 작업을 수행한 사용자. Note 레코드 시스템 계정 (예: NT 권한 \ 시스템)에 의해 수행 되는 eDiscovery 활동에 대 한 감사 로그에도 포함 됩니다.  <br/> |
|UserKey  <br/> |UserId 속성에서 식별 한 사용자에 대 한 대체 ID입니다. EDiscovery 활동에 대 한이 속성 값은 일반적으로 UserId 속성과 다릅니다.  <br/> |
|UserServicePlan  <br/> |조직에서 사용 하는 Office 365 구독 합니다. EDiscovery 활동에 대 한이 속성은 일반적으로 비어 있습니다.  <br/> |
|UserType  <br/> |작업을 수행한 사용자의 형식입니다. 다음 값에는 사용자 유형을 나타냅니다.  <br/> 0 A 일반 사용자입니다. 2 Office 365 조직에서는 관리자입니다. 3 Microsoft 데이터 센터 관리자 또는 데이터 센터 시스템 계정입니다. 4 시스템 계정입니다. 5는 응용 프로그램입니다. 6는 서비스 사용자. |
|Version  <br/> |기록 되는 활동 (작업 속성에 의해 식별 된)의 버전 번호를 나타냅니다.  <br/> |
|작업량  <br/> |Office 365 서비스 활동 발생 했습니다. EDiscovery 활동에 대 한 값은 **SecurityComplianceCenter**.<br/> |
