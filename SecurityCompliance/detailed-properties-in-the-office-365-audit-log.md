---
title: Office 365 감사 로그의 자세한 속성
ms.author: markjjo
author: markjjo
manager: laurawi
ms.audience: Admin
ms.topic: reference
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MOE150
- BCS160
- MET150
ms.assetid: ce004100-9e7f-443e-942b-9b04098fcfc3
description: Office 365 감사 로그 레코드에 포함 된 추가 속성에 대 한 설명입니다.
ms.openlocfilehash: 0219ed1fe29dc3ae1f940cd6991781368ae2d519
ms.sourcegitcommit: a80bd8626720fabdf592b84e4424cd3a83d08280
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30223477"
---
# <a name="detailed-properties-in-the-office-365-audit-log"></a>Office 365 감사 로그의 자세한 속성

Office 365 보안 &amp; 및 준수 센터에서 감사 로그 검색 결과를 내보낼 때 검색 조건을 충족 하는 모든 결과를 다운로드할 수 있는 옵션이 있습니다. 보안 &amp; 및 준수 센터의 **** \> **감사 로그 검색** 페이지에서 **모든 결과 다운로드** 를 선택 하 여이 작업을 수행 합니다. 자세한 내용은 [Office 365 보안 &amp; 및 준수 센터에서 감사 로그 검색](search-the-audit-log-in-security-and-compliance.md)을 참조 하세요.
  
 감사 로그 검색에 대 한 모든 결과를 내보낼 때 Office 365 통합 감사 로그의 원시 데이터는 로컬 컴퓨터로 다운로드 되는 CSV (쉼표로 구분 된 값) 파일로 복사 됩니다. 이 파일에는 감사 로그 항목에서 **Detail**이라는 열에 대 한 추가 정보가 포함 되어 있습니다. 이 열에는 감사 로그 레코드의 여러 속성에 대 한 다중 값 속성이 포함 되어 있습니다. 이 다중 값 속성의 각 **속성: 값** 쌍은 쉼표로 구분 됩니다. 
  
다음 표에서는 여러 속성 **정보** 열에서 이벤트가 발생 하는 Office 365 서비스에 따라 포함 되는 속성에 대해 설명 합니다. 이 속성 열이 있는 **Office 365 서비스** 는 해당 속성을 포함 하는 서비스 및 작업 유형 (사용자 또는 관리자)을 나타냅니다. 이러한 속성에 대 한 자세한 내용 또는이 항목에 나열 되지 않을 수 있는 속성에 대 한 자세한 내용은 [Office 365 Management Activity API Schema](https://go.microsoft.com/fwlink/p/?LinkId=717993)를 참조 하십시오.
  
> [!TIP]
> Excel에서 파워 쿼리를 사용 하 여이 열을 여러 열로 분할 하 여 각 속성에 자체 열을 표시할 수 있습니다. 이렇게 하면 이러한 속성 중 하나 이상을 정렬 및 필터링 할 수 있습니다. 이 작업을 수행 하는 방법에 대 한 자세한 내용은 [split a text 열 (Power Query)](https://support.office.com/article/5282d425-6dd0-46ca-95bf-8e0da9539662)에서 "구분 기호로 열 분할" 섹션을 참조 하십시오. 
  
|**속성**|**설명**|**이 속성을 가진 Office 365 서비스**|
|:-----|:-----|:-----|
|터  <br/> |작업을 수행한 사용자 또는 서비스 계정입니다. |Azure Active Directory  <br/> |
|AddOnName  <br/> |팀에서 추가, 제거 또는 업데이트 된 추가 기능의 이름입니다. Microsoft 팀의 추가 기능 유형은 bot, 커넥터 또는 탭입니다.  <br/> |Microsoft Teams  <br/> |
|AddOnType  <br/> |팀에서 추가, 제거 또는 업데이트 된 추가 기능의 유형입니다. 다음 값은 추가 기능의 형식을 나타냅니다.<br/> **1** -bot을 나타냅니다.<br/> **2** -커넥터를 나타냅니다.<br/> **3** -탭을 나타냅니다. |Microsoft Teams  <br/> |
|AzureActiveDirectoryEventType  <br/> |Azure Active Directory 이벤트의 유형입니다. 이벤트 유형을 나타내는 값은 다음과 같습니다.<br/> **0** -계정 로그인 이벤트를 나타냅니다.<br/> **1** -Azure 응용 프로그램 보안 이벤트를 나타냅니다. |Azure Active Directory  <br/> |
|channelguid  <br/> |Microsoft 팀 채널의 ID입니다. 채널이 있는 팀이 **teamname** 및 **teamname** 속성으로 식별 됩니다.<br/> |Microsoft Teams  <br/> |
|channelname  <br/> |Microsoft 팀 채널의 이름입니다. 채널이 있는 팀이 **teamname** 및 **teamname** 속성으로 식별 됩니다.<br/> |Microsoft Teams  <br/> |
|Client  <br/> |클라이언트 장치, 장치 OS 및 login 이벤트에 사용 되는 장치 브라우저 (예: Nokia Lumia 920;) Windows Phone 8; IE Mobile 11).  <br/> |Azure Active Directory  <br/> |
|clientinfostring  <br/> |브라우저 버전, Outlook 버전 및 모바일 장치 정보와 같이 작업을 수행 하는 데 사용한 전자 메일 클라이언트에 대 한 정보  <br/> |Exchange (사서함 활동)  <br/> |
|ClientIP  <br/> |활동을 로그할 때 사용 된 장치의 IP 주소입니다. IP 주소는 IPv4 또는 IPv6 주소 형식으로 표시 됩니다.  <br/> |Exchange 및 Azure Active Directory  <br/> |
|ClientIPAddress  <br/> |ClientIP과 동일 합니다.  <br/> |SharePoint  <br/> |
|CreationTime  <br/> |사용자가 활동을 수행 했을 때 utc (협정 세계시)로 표시 되는 날짜와 시간입니다.  <br/> |모두  <br/> |
|destinationfileextension  <br/> |복사 하거나 이동할 파일의 파일 확장명입니다. 이 속성은 FileCopied 및 FileMoved 사용자 작업에만 표시 됩니다.  <br/> |SharePoint  <br/> |
|DestinationFileName  <br/> |파일 이름이 복사 되거나 이동 됩니다. 이 속성은 FileCopied 및 FileMoved 작업에만 표시 됩니다.  <br/> |SharePoint  <br/> |
|DestinationRelativeUrl  <br/> |파일을 복사 하거나 이동할 대상 폴더의 URL입니다. **SiteURL**, **DestinationRelativeURL**및 **destinationfilename** 속성의 값을 조합 하면 **ObjectID** 속성의 값 (복사 된 파일의 전체 경로 이름)과 같습니다. 이 속성은 FileCopied 및 FileMoved 사용자 작업에만 표시 됩니다.<br/> |SharePoint  <br/> |
|EventSource  <br/> |SharePoint에서 이벤트가 발생 한 것을 식별 합니다. 사용할 수 있는 값은 **SharePoint** 및 **objectmodel**입니다.<br/> |SharePoint  <br/> |
|externalaccess  <br/> |Exchange 관리 활동의 경우, cmdlet이 조직의 사용자에 의해 실행 되었는지, Microsoft 데이터 센터 담당자나 데이터 센터 서비스 계정 또는 위임 된 관리자가 실행할지를 지정 합니다. 값이 **False** 이면 조직의 다른 사용자가 cmdlet을 실행 한 것입니다. **True** 값은 데이터 센터 직원, 데이터 센터 서비스 계정 또는 위임 된 관리자에 의해 cmdlet이 실행 되었음을 나타냅니다.<br/> Exchange 사서함 활동의 경우 조직 외부의 사용자가 사서함에 액세스 했는지 여부를 지정 합니다.  <br/> |Exchange  <br/> |
|ExtendedProperties  <br/> |Azure Active Directory 이벤트에 대 한 확장 된 속성입니다.  <br/> |Azure Active Directory  <br/> |
|ID  <br/> |보고서 항목의 ID입니다. ID는 보고서 항목을 고유 하 게 식별 합니다.  <br/> |모두  <br/> |
|internallogontype  <br/> |내부용으로 예약 되어 있습니다.  <br/> |Exchange (사서함 활동)  <br/> |
|ItemType  <br/> |액세스 하거나 수정한 개체의 유형입니다. 사용할 수 있는 값에는 **파일**, **폴더**, **웹**, **사이트**, **테 넌 트**및 **documentlibrary**가 있습니다.<br/> |SharePoint  <br/> |
|LoginStatus  <br/> |발생 했을 수 있는 로그인 실패를 확인 합니다.  <br/> |Azure Active Directory  <br/> |
|logontype  <br/> |사서함 액세스 유형입니다. 다음 값은 사서함에 액세스 한 사용자의 유형을 나타냅니다.<br/><br/> **0** -사서함 소유자를 나타냅니다.<br/> **1** -관리자를 나타냅니다.<br/> **2** -대리인을 나타냅니다. <br/>**3** -Microsoft 데이터 센터의 전송 서비스를 나타냅니다.<br/> **4** -Microsoft 데이터 센터의 서비스 계정을 나타냅니다. <br/>**6** -위임 된 관리자를 나타냅니다. |Exchange (사서함 활동)  <br/> |
|MailboxGuid  <br/> |액세스 한 사서함의 Exchange GUID입니다.  <br/> |Exchange (사서함 활동)  <br/> |
|MailboxOwnerUPN  <br/> |액세스 한 사서함을 소유한 사용자의 전자 메일 주소입니다.  <br/> |Exchange (사서함 활동)  <br/> |
|구성원  <br/> |팀에서 추가 되거나 제거 된 사용자를 나열 합니다. 다음 값은 사용자에 게 할당 된 역할 형식을 나타냅니다.<br/><br/> **1** -소유자 역할을 나타냅니다.<br/> **2** -구성원 역할을 나타냅니다.<br/> **3** -게스트 역할을 나타냅니다. <br/><br/>Members 속성에도 조직의 이름과 구성원의 전자 메일 주소가 포함 됩니다.  <br/> |Microsoft Teams  <br/> |
|ModifiedProperties (Name, NewValue, OldValue)  <br/> |이 속성은 사이트 또는 사이트 모음 관리 그룹의 구성원으로 사용자를 추가 하는 등의 관리 이벤트에 포함 됩니다. 이 속성에는 수정 된 속성의 이름 (예: 사이트 관리자 그룹)과 수정한 속성의 새 값 (사이트 관리자로 추가한 사용자 및 수정한 개체의 이전 값)이 포함 됩니다.  <br/> |모두 (관리 활동)  <br/> |
|id  <br/> |Exchange 관리자 감사 로깅을 위해 cmdlet에 의해 수정 된 개체의 이름입니다.  <br/> SharePoint 작업의 경우 사용자가 액세스 하는 파일 또는 폴더의 전체 URL 경로 이름입니다.  <br/> Azure AD 활동의 경우 수정 된 사용자 계정의 이름입니다.  <br/> |모두  <br/> |
|작업  <br/> |사용자 또는 관리자 활동의 이름입니다. 이 속성의 값은 **활동** 드롭다운 목록에서 선택한 값에 해당 합니다. **모든 작업에 대해 결과 표시** 를 선택 하면 보고서에 모든 서비스에 대 한 모든 사용자 및 관리 활동에 대 한 항목이 포함 됩니다. office 365 감사 로그에 기록 된 작업/작업에 대 한 설명은 [office 365 보안 &amp; 및 준수 센터에서 감사 로그 검색](search-the-audit-log-in-security-and-compliance.md)의 **감사 된 작업** 탭을 참조 하십시오.<br/> Exchange 관리 활동의 경우이 속성은 실행 된 cmdlet의 이름을 식별 합니다.  <br/> |모두  <br/> |
|조직 id  <br/> |Office 365 조 직의 GUID입니다.  <br/> |모두  <br/> |
|경로  <br/> |액세스 한 메시지가 있는 사서함 폴더의 이름입니다. 이 속성은 또한 메시지가 만들어지거나 복사/이동 되는 폴더를 식별 합니다.  <br/> |Exchange (사서함 활동)  <br/> |
|매개 변수  <br/> |Exchange 관리 활동의 경우 Operation 속성에서 식별 된 cmdlet에 사용 된 모든 매개 변수의 이름과 값입니다.  <br/> |Exchange (관리 활동)  <br/> |
|RecordType  <br/> |record에서 지정한 작업의 유형입니다. 다음 값은 레코드 종류를 나타냅니다.<br/><br/> **1** -Exchange 관리자 감사 로그의 레코드를 나타냅니다. <br/>**2** -singled 사서함 항목에 대해 수행 된 작업에 대 한 Exchange 사서함 감사 로그의 레코드를 나타냅니다. <br/>**3** -Exchange 사서함 감사 로그 에서도 레코드를 나타냅니다. 이 레코드 종류는 원본 사서함에서 여러 항목을 지운 편지함 폴더로 이동 하거나 여러 항목을 영구적으로 삭제 하는 등의 여러 항목에 대해 작업이 수행 되었음을 나타냅니다.<br/>**4** -사이트에 대 한 권한 할당 관리자 또는 사용자와 같은 SharePoint의 사이트 관리 작업을 나타냅니다. <br/>**6** -사용자가 파일을 보거나 수정 하는 등 SharePoint의 파일 또는 폴더 관련 작업을 나타냅니다. <br/>**8** -Azure Active Directory에서 수행 된 관리 작업을 나타냅니다. <br/>**9** -OrgId 로그인 이벤트를 Azure Active Directory에 표시 합니다. 이 레코드 종류는 더 이상 사용 되지 않습니다.<br/>**10** -데이터 센터에서 Microsoft 담당자가 수행한 보안 cmdlet 이벤트를 나타냅니다. <br/>**11** -SharePoint의 DLP (데이터 손실 방지) 이벤트를 나타냅니다.<br/> **12** -Sway 이벤트를 나타냅니다. <br/>**13** -통합 dlp 정책으로 구성 된 경우 Exchange의 DLP 이벤트를 나타냅니다. Exchange 전송 규칙을 기반으로 하는 DLP 이벤트는 지원 되지 않습니다.<br>**14** -SharePoint의 공유 이벤트를 나타냅니다.<br/> **15** -Azure Active Directory의 STS (보안 토큰 서비스) 로그온 이벤트를 나타냅니다. <br/>**18** -보안 &amp; 준수 센터 이벤트를 나타냅니다. <br/>**20** -Power BI 이벤트를 나타냅니다. <br/>**21**-Dynamics 365 이벤트를 나타냅니다.<br/>**22** -Yammer 이벤트를 나타냅니다. <br/>**23** -비즈니스용 Skype 이벤트를 나타냅니다. <br/>**24** -eDiscovery 이벤트를 나타냅니다. 이 레코드 종류는 보안 &amp; 및 준수 센터에서 콘텐츠 검색을 실행 하 고 eDiscovery 사례를 관리 하 여 수행한 작업을 나타냅니다. 자세한 내용은 Office 365 감사 로그에서 eDiscovery 활동 검색을 참조 하세요.<br/>**25, 26 또는 27** -Microsoft 팀 이벤트를 나타냅니다. <br/>**28** -Exchange Online Protection 및 Office 365 Advanced Threat protection 이벤트의 피싱 및 맬웨어 이벤트를 나타냅니다.<br/> **30** -Microsoft Flow 이벤트를 나타냅니다.<br/> **32** -지정 된 Microsoft Stream 이벤트<br/> **35** -Microsoft Project 이벤트를 나타냅니다. <br/> **36** -SharePoint 목록 이벤트를 나타냅니다.<br/> **40** -보안 및 준수 알림 신호의 결과로 생성 되는 이벤트를 나타냅니다.<br/> **41** -안전 링크 차단 시간 및 Office 365 Advanced Threat Protection의 무시 이벤트 차단 이벤트가 표시 됩니다.<br/>**44** -작업에 대 한 분석 이벤트를 나타냅니다. <br/>**47** -SharePoint, OneDrive 및 Microsoft 팀의 파일에 대 한 Office 365 Advanced Threat Protection의 피싱 및 맬웨어 이벤트를 나타냅니다. |모두  <br/> |
|resultstatus  <br/> |**작업** 속성에 지정 된 작업이 성공 했는지 여부를 나타냅니다.  <br/> Exchange 관리 활동의 경우이 값은 **True** (성공) 또는 **False** (failed) 중 하나입니다.  <br/> |모두  <br/>|
|SecurityComplianceCenterEventType  <br/> |작업이 보안 &amp; 및 준수 센터 이벤트 임을 나타냅니다. 이 속성 &amp; 에 대 한 모든 보안 준수 센터 작업의 값은 **0** 입니다.<br/> |Office 365 보안 및 준수 센터  <br/> |
|SharingType  <br/> |리소스를 공유 하는 사용자에 게 할당 된 공유 권한 유형입니다. 이 사용자는 **usersharedwith** 속성에서 식별 됩니다.<br/> |SharePoint  <br/> |
|사이트  <br/> |사용자가 액세스 한 파일 또는 폴더가 있는 사이트의 GUID입니다.  <br/> |SharePoint  <br/> |
|SiteUrl  <br/> |사용자가 액세스 한 파일 또는 폴더가 있는 사이트의 URL입니다.  <br/> |SharePoint  <br/> |
|sourcefileextension  <br/> |사용자가 액세스 한 파일의 파일 확장명입니다. 액세스 한 개체가 폴더인 경우이 속성은 비어 있습니다.  <br/> |SharePoint  <br/> |
|sourcefilename  <br/> |사용자가 액세스 하는 파일 또는 폴더의 이름입니다.  <br/> |SharePoint  <br/> |
|SourceRelativeUrl  <br/> |사용자가 액세스 한 파일이 들어 있는 폴더의 URL입니다. **SiteURL**, **SourceRelativeURL**및 **sourcefilename** 속성의 값 조합은 사용자가 액세스 하는 파일의 전체 경로 이름인 **ObjectID** 속성의 값과 같습니다.<br/> |SharePoint  <br/> |
|Subject  <br/> |액세스 한 메시지의 제목 줄입니다.  <br/> |Exchange (사서함 활동)  <br/> |
|tabtype  <br/> | 팀에서 추가, 제거 또는 업데이트 된 탭의 유형입니다. 이 속성에 사용할 수 있는 값은 다음과 같습니다.<br/><br/> **** excel 탭  <br/> **내선** -모든 자사 및 타사 앱 (예: Planner, VSTS 및 양식)  <br/> **Notes** -OneNote 탭  <br/> **Pdfpin** -PDF 탭  <br/> **powerbi** -Powerbi 탭  <br/> **Powerpointpin** -PowerPoint 탭  <br/> **Sharepointfiles** -SharePoint 탭  <br/> **웹 페이지** -고정 된 웹 사이트 탭  <br/> **위 키-탭** -위 키 탭  <br/> **wordpin** -Word 탭입니다.  <br/> |Microsoft Teams  <br/> |
|대상  <br/> |작업 ( **Operation** ) 속성에서 식별 된 작업을 수행 하는 사용자입니다. 예를 들어 게스트 사용자가 SharePoint 또는 Microsoft 팀에 추가 된 경우에는 해당 사용자가이 속성에 나열 됩니다.<br/> |Azure Active Directory  <br/> |
|teamguid  <br/> |Microsoft 팀의 팀 ID입니다.  <br/> |Microsoft Teams  <br/> |
|teamname  <br/> |Microsoft 팀의 팀 이름입니다.  <br/> |Microsoft Teams  <br/> |
|UserAgent  <br/> |사용자 브라우저에 대 한 정보입니다. 이 정보는 브라우저에서 제공 됩니다.  <br/> |SharePoint  <br/> |
|userdomain  <br/> |작업을 수행한 사용자 (작업자)의 테 넌 트 조직에 대 한 id 정보입니다.  <br/> |Azure Active Directory  <br/> |
|UserID  <br/> |**작업** 속성에 지정 된 작업을 수행 하 여 레코드가 기록 되는 사용자입니다. 시스템 계정 (예: SHAREPOINT\system 또는 NT 권한 \ 컴퓨터)에서 수행 하는 작업에 대 한 레코드가 감사 로그에도 포함 되어 있습니다.<br/> |모두  <br/> |
|userkey  <br/> |**UserID** 속성에서 식별 된 사용자의 대체 ID입니다. 예를 들어이 속성은 SharePoint의 사용자가 수행한 이벤트에 대 한 passport 고유 ID (PUID)로 채워집니다. 또한이 속성은 다른 서비스에서 발생 하는 이벤트에 대 한 **UserID** 속성과 동일한 값과 시스템 계정에서 수행 하는 이벤트를 지정할 수 있습니다.<br/> |모두  <br/> |
|usersharedwith  <br/> |리소스를 공유한 사용자입니다. 이 속성은 **Operation** 속성의 값이 **SharingSet**인 경우에 포함 됩니다. 이 사용자는 보고서의 **공유** 됨 열에도 표시 됩니다.<br/> |SharePoint  <br/> |
|UserType  <br/> |작업을 수행한 사용자의 유형입니다. 다음 값은 사용자 형식을 나타냅니다.<br/> <br/> **0** -일반 사용자입니다. <br/>**2** -Office 365 조직의 관리자입니다. <br/>**3** -Microsoft 데이터 센터 관리자 또는 데이터 센터 시스템 계정입니다. <br/>**4** -시스템 계정입니다. <br/>**5** -응용 프로그램 <br/>**6** -서비스 사용자입니다.<br/>**7** -사용자 지정 정책<br/>**8** -시스템 정책. |모두  <br/> |
|Version  <br/> |기록 된 작업의 버전 번호 ( **Operation** 속성으로 식별 됨)를 나타냅니다.  <br/> |모두  <br/> |
|작업량  <br/> |활동이 발생 한 Office 365 서비스입니다. 이 속성에 사용할 수 있는 값은 다음과 같습니다.<br/> <br/>**SharePoint<br/>OneDrive<br/>Exchange<br/>AzureActiveDirectory<br/>datac, 보안<br/>준수<br/>Sway<br/>비즈니스용 Skype<br/>SecurityComplianceCenter<br/>PowerBI CRM<br/><br/>Yammer<br/>MicrosoftTeams<br/>ThreatIntelligence<br/>MicrosoftFlow<br/>MicrosoftStream<br/>DlpSharePointClassificationData<br/>Project<br/>PowerApps<br/>작업 공간 분석**|모두  <br/> |
||||
   
특정 이벤트에 대 한 세부 정보를 볼 때 **자세한 정보** 를 클릭 하면 위에서 설명한 속성도 표시 됩니다. 
  
![감사 로그 이벤트 레코드의 자세한 속성을 보려면 추가 정보를 클릭 합니다.](media/6df582ae-d339-4735-b1a6-80914fb77a08.png)
  

