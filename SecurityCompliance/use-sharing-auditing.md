---
title: 외부 사용자와 공유된 리소스를 찾기 위한 감사 공유
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- SPO160
- MOE150
- BCS160
- MET150
ms.assetid: 50bbf89f-7870-4c2a-ae14-42635e0cfc01
description: '공유는 SharePoint Online 및 비즈니스용 OneDrive의 주요 활동입니다. 이제 관리자는 Office 365 감사 로그의 공유 감사를 사용 하 여 조직 외부의 사용자와 공유 되는 리소스를 식별할 수 있습니다. '
ms.openlocfilehash: 8996d404e2dbeaba01952c33a8699ca2f151ad5d
ms.sourcegitcommit: a8049055a48375bee7e6ed81fafcb27a7b2fcdff
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/26/2019
ms.locfileid: "35911778"
---
# <a name="use-sharing-auditing-in-the-office-365-audit-log"></a>외부 사용자와 공유된 리소스를 찾기 위한 감사 공유

공유는 SharePoint Online 및 비즈니스용 OneDrive의 주요 활동 이며, Office 365 조직에서 널리 사용 되 고 있습니다. 관리자는 Office 365 감사 로그의 공유 감사를 사용 하 여 조직에서 공유를 사용 하는 방법을 확인할 수 있습니다. 
  
## <a name="the-sharepoint-sharing-schema"></a>SharePoint 공유 스키마

공유 정책 및 공유 링크와 관련 된 이벤트를 제외 하 고 발생 하는 관리 이벤트는 파일 및 폴더 관련 이벤트와는 다른 사용자에 게 영향을 주는 작업을 수행 하는 기본적인 방법 중 하나입니다. 예를 들어 자원 사용자 A가 사용자 B에 게 파일에 대 한 액세스 권한을 부여 하는 경우 이 예에서는 사용자 A가 작업 중인 *사용자* 이 고 사용자 B가 *대상 사용자*입니다. SharePoint 파일 스키마에서 작동 중인 사용자의 작업은 파일 자체에만 영향을 줍니다. 사용자 A가 파일을 여는 경우, **Fileaccessed** 한 이벤트에서 필요한 정보는 작업 중인 사용자입니다. 이러한 차이를 해결 하기 위해 *SharePoint 공유 스키마*라고 하는 별도의 스키마를 통해 공유 이벤트에 대 한 추가 정보를 캡처할 수 있습니다. 이를 통해 관리자는 리소스를 공유 하는 사용자와 리소스를 공유 하는 사람을 볼 수 있습니다. 
  
공유 스키마는 공유 이벤트와 관련 된 감사 레코드에 두 개의 필드를 추가로 제공 합니다. 
  
- **TargetUserOrGroupType:** 대상 사용자 또는 그룹이 Member, Guest, SharePointGroup, SecurityGroup 또는 Partner 인지를 식별 합니다.

- **Targetuserorgroupname:** 리소스를 공유 하는 대상 사용자 또는 그룹의 UPN 이나 이름을 저장 합니다 (이전 예제에서는 User B). 

이러한 두 필드는 사용자, 작업 및 날짜와 같은 Office 365 감사 로그 스키마의 다른 속성 외에, *누가 누구* 에 게 *어떤* 리소스를 공유 ** 하는지를 알려 줄 수 있습니다. ** 
  
공유 스토리에 중요 한 또 다른 스키마 속성이 있습니다. 감사 로그 검색 결과를 내보낼 때 내보낸 CSV 파일의 **Auditdata** 열에는 공유 이벤트에 대 한 정보가 저장 됩니다. 예를 들어 사용자가 다른 사용자와 사이트를 공유 하는 경우이 작업을 수행 하려면 SharePoint 그룹에 대상 사용자를 추가 합니다. **Auditdata** 열은 관리자에 게 컨텍스트를 제공 하기 위해이 정보를 캡처합니다. **Auditdata** 열에서 정보를 구문 분석 하는 방법에 대 한 지침은 [2 단계](#step-2-use-the-powerquery-editor-to-format-the-exported-audit-log) 를 참조 하십시오.

## <a name="sharepoint-sharing-events"></a>SharePoint 공유 이벤트

공유는 사용자 (작업 중인 사용자)가 ** 다른 사용자 ( *대상* 사용자)와 리소스를 공유 하려고 할 때 정의 됩니다. 외부 사용자 (조직 외부에 있고 조직의 Azure Active Directory에 게스트 계정이 없는 사용자)를 사용 하 여 리소스를 공유 하는 것과 관련 된 감사 레코드는 다음 이벤트 (Office 365에 기록 됨)로 식별 됩니다. 감사 로그:

- **SharingInvitationCreated:** 조직의 사용자가 외부 사용자와 리소스 (아마도 사이트)를 공유 하려고 했습니다. 이로 인해 외부 공유 초대가 대상 사용자에 게 전송 됩니다. 이때 리소스에 대 한 액세스 권한이 부여 되지 않습니다.

- **SharingInvitationAccepted:** 외부 사용자가 작동 중인 사용자가 보낸 공유 초대를 수락 했으며 이제 해당 리소스에 액세스할 수 있습니다.

- **AnonymousLinkCreated:** 리소스에 대 한 익명 링크 ("모든 사용자" 링크 라고도 함)가 만들어집니다. 익명 링크를 만들고 복사할 수 있으므로 익명 링크가 포함 된 모든 문서가 대상 사용자와 공유 된 것으로 가정 하는 것이 합리적입니다.

- **AnonymousLinkUsed:** 이름에서 알 수 있듯이이 이벤트는 익명 링크를 사용 하 여 리소스에 액세스할 때 기록 됩니다. 

- **Securelinkcreated:** 사용자가 특정 사람과 리소스를 공유 하기 위한 "특정 사용자 링크"를 만든 경우 이 대상 사용자는 조직 외부에 있는 사람도 될 수 있습니다.

- **Ad이상 Tosecurelink:** 사용자가 특정 사람 링크에 추가 되었습니다. 이 대상 사용자는 조직 외부에 있는 사람도 될 수 있습니다.

## <a name="sharing-auditing-work-flow"></a>감사 작업 흐름 공유
  
사용자 (작업 중인 사용자)가 다른 사용자 (대상 사용자)와 리소스를 공유 하려는 경우 먼저 SharePoint (또는 비즈니스용 OneDrive)가 대상 사용자의 전자 메일 주소가 조직의 디렉터리에 있는 사용자 계정과 이미 연결 되어 있는지 확인 합니다. 대상 사용자가 디렉터리에 있고 해당 게스트 사용자 계정이 있는 경우 SharePoint에서는 다음과 같은 작업을 수행 합니다.
  
-  는 대상 사용자를 적절 한 SharePoint 그룹에 추가 하 여 리소스에 액세스할 수 있는 권한을 즉시 할당 하 고 Ad연결 된 **Togroup** 이벤트를 기록 합니다. 
    
- 대상 사용자의 전자 메일 주소로 공유 알림을 보냅니다.
    
- **SharingSet** 이벤트를 기록 합니다. 이 이벤트에는 감사 로그 검색 도구의 활동 선택기에서 **공유 및 액세스 요청 작업** 의 "공유 파일, 폴더 또는 사이트" 라는 이름이 표시 됩니다. [1 단계](#step-1-search-for-sharing-events-and-export-the-results-to-a-csv-file)에 있는 스크린샷를 참조 하세요. 
    
대상 사용자에 대 한 사용자 계정이 디렉터리에 없는 경우 SharePoint는 다음을 수행 합니다. 
    
   - 리소스를 공유 하는 방법에 따라 다음 이벤트 중 하나를 기록 합니다.
   
      - **AnonymousLinkCreated**
   
      - **SecureLinkCreated**
   
      - **Ad이상 Tosecurelink** 

      - **SharingInvitationCreated** (이 이벤트는 공유 리소스가 사이트인 경우에만 기록 됨)
    
   - 대상 사용자가 초대의 링크를 클릭 하 여 전송 된 공유 초대를 수락 하면 SharePoint에서 **SharingInvitationAccepted** 이벤트를 기록 하 고 리소스에 액세스 하기 위한 대상 사용자 권한을 할당 합니다. 대상 사용자에 게 익명 링크가 전송 되는 경우 대상 사용자가 링크를 사용 하 여 해당 리소스에 액세스 한 후 **AnonymousLinkUsed** 이벤트가 기록 됩니다. 보안 링크의 경우에 **** 는 외부 사용자가 링크를 사용 하 여 리소스에 액세스할 때 파일에 액세스 한 이벤트가 기록 됩니다.

초대 하는 사용자의 id 및 초대를 실제로 수락 하는 사용자와 같은 대상 사용자에 대 한 추가 정보도 로깅됩니다. 경우에 따라 이러한 사용자 또는 전자 메일 주소는 다를 수 있습니다. 

## <a name="how-to-identify-resources-shared-with-external-users"></a>외부 사용자와 공유 된 리소스를 확인 하는 방법

관리자에 대 한 일반적인 요구 사항에는 조직 외부의 사용자와 공유 된 모든 리소스의 목록이 작성 됩니다. 관리자는 Office 365의 공유 감사를 사용 하 여이 목록을 생성할 수 있습니다. 이 작업을 수행하는 방법은 다음과 같습니다.
  
### <a name="step-1-search-for-sharing-events-and-export-the-results-to-a-csv-file"></a>1 단계: 공유 이벤트 검색 및 결과를 CSV 파일로 내보내기

첫 번째 단계는 공유 이벤트에 대 한 Office 365 감사 로그를 검색 하는 것입니다. 감사 로그 검색에 대 한 자세한 내용 (필요한 권한 포함)은 [Security & 준수 센터에서 감사 로그 검색](search-the-audit-log-in-security-and-compliance.md)을 참조 하십시오.
  
1. [https://protection.office.com](https://protection.office.com)으로 이동합니다.
    
2. 회사 또는 학교 계정을 사용하여 Office 365에 로그인합니다.
    
3. 보안 & 준수 센터의 왼쪽 창에서 **검색**  > **감사 로그 검색**을 클릭 합니다.
    
    **감사 로그 검색** 페이지가 표시 됩니다. 
    
4. **활동**아래에서 **공유 및 액세스 요청 활동** 을 클릭 하 여 공유 관련 이벤트를 검색 합니다. 
    
    ![활동 아래에서 공유 및 액세스 요청 작업을 선택 합니다.](media/46bb25b7-1eb2-4adf-903a-cc9ab58639f9.png)
  
5.  날짜 및 시간 범위를 선택 하 여 해당 기간 내에 발생 한 공유 이벤트를 찾습니다. 
    
6. 검색 **** 을 클릭 하 여 검색을 실행 합니다. 
    
7. 검색 실행이 완료 되 고 결과가 표시 되 면 결과 **내보내기** \> **모든 결과 다운로드**를 클릭 합니다.
    
    내보내기 옵션을 선택한 후에는 CSV 파일을 열거나 저장 하 라는 메시지가 창 맨 아래에 표시 됩니다.
    
8. 다른 **** \> **이름으로 저장** 저장을 클릭 하 고 로컬 컴퓨터의 폴더에 CSV 파일을 저장 합니다. 

### <a name="step-2-use-the-powerquery-editor-to-format-the-exported-audit-log"></a>2 단계: PowerQuery Editor를 사용 하 여 내보낸 감사 로그의 서식 지정

다음 단계에서는 Excel의 파워 쿼리 편집기에서 JSON 변환 기능을 사용 하 여 **Auditdata** 열의 각 속성 (다중 속성 JSON 개체로 구성)을 자체 열로 분할 합니다. 이렇게 하면 열을 필터링 하 여 공유와 관련 된 레코드를 볼 수 있습니다.

단계별 지침은 [Export, configure 및 view audit log records](export-view-audit-log-records.md#step-2-format-the-exported-audit-log-using-the-power-query-editor)에서 "2 단계: 검색 된 감사 로그를 Power Query Editor를 사용 하 여 서식 지정"을 참조 하십시오.

### <a name="step-3-filter-the-csv-file-for-resources-shared-with-external-users"></a>3 단계: 외부 사용자와 공유 되는 리소스에 대 한 CSV 파일 필터링

다음 단계에서는 이전에 [SharePoint 공유 이벤트](#sharepoint-sharing-events) 섹션에서 설명한 서로 다른 공유 관련 이벤트에 대 한 CSV를 필터링 합니다. 또는 **TargetUserOrGroupType** 열을 필터링 하 여이 속성의 값이 **Guest**인 모든 레코드를 표시할 수 있습니다. 

이전 단계의 지침에 따라 PowerQuery editor를 사용 하 여 CSV 파일을 준비한 후에 다음을 수행 합니다.
    
1. 2 단계에서 만든 Excel 파일을 엽니다. 

2. **홈** 탭에서 **정렬 & 필터**를 클릭 하 고 **필터**를 클릭 합니다.
    
3. **작업** 열의 **정렬 & 필터** 드롭다운 목록에서 모든 선택을 취소 하 고 다음 공유 관련 이벤트를 하나 이상 선택 하 고 **확인**을 클릭 합니다.
 
   - **SharingInvitationCreated**
   
   - **AnonymousLinkCreated**
   
   - **SecureLinkCreated**
   
   - **Ad이상 Tosecurelink** 
    
    선택한 이벤트에 대 한 행이 표시 됩니다.
    
4. **TargetUserOrGroupType** 라는 열로 이동 하 여 선택 합니다. 
    
5. **정렬 & 필터** 드롭다운 목록에서 모든 선택을 취소 하 고 **TargetUserOrGroupType: Guest**를 선택한 다음 **확인**을 클릭 합니다.
    
    이제 외부 사용자는 **TargetUserOrGroupType: Guest**값으로 식별 되므로 공유 이벤트 및 대상 사용자가 조직 외부에 있는 위치에 대 한 행이 표시 됩니다. 
  
> [!TIP]
> 표시 되는 감사 레코드의 경우 **ObjectId** 열은 대상 사용자와 공유 된 리소스를 식별 합니다. 예를 `ObjectId:https:\/\/contoso-my.sharepoint.com\/personal\/sarad_contoso_com\/Documents\/Southwater Proposal.docx`들어
