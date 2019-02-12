---
title: Office 365 감사 로그의 자세한 속성
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: reference
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MOE150
- BCS160
- MET150
ms.assetid: ce004100-9e7f-443e-942b-9b04098fcfc3
description: Office 365에 포함 되는 추가 속성에 대 한 설명이 로그 레코드를 감사 합니다.
ms.openlocfilehash: e2450f8d4f9a613d6b21e373d2a2de841cfc7ca0
ms.sourcegitcommit: d6b1632a44e40522a4a16e7cb05ba5189214baeb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/11/2019
ms.locfileid: "29890049"
---
# <a name="detailed-properties-in-the-office-365-audit-log"></a>Office 365 감사 로그의 자세한 속성

Office 365 보안에서 감사 로그 검색의 결과 내보낼 때 &amp; 준수 센터 해야 검색 조건을 만족 하는 모든 결과 다운로드 하는 옵션입니다. **결과 내보내기** 를 선택 하 여이 작업을 수행 \> 보안에서 **감사 로그 검색** 페이지의 **모든 결과 다운로드** 를 &amp; 준수 센터입니다. 자세한 내용은 참조 [Office 365 보안에서 감사 로그를 검색 &amp; 준수 센터](search-the-audit-log-in-security-and-compliance.md)합니다.
  
 모든 내보내기는 감사 로그 검색에 대 한 결과 하는 경우에 쉼표를 통합된 감사 로그를 복사 하는 Office 365에서 원시 데이터 값 (CSV) 파일을 로컬 컴퓨터에 다운로드는이 구분 합니다. 이 파일 **세부 정보**를 명명 된 열에서 감사 로그 항목에서 추가 정보를 포함 합니다. 이 열에는 감사 로그 레코드에서 여러 속성에 대 한 다중값 속성을 포함 합니다. 이 다중값 속성의 **속성: 값** 쌍의 각 쉼표로 구분 됩니다. 
  
포함 된 속성을 설명 하는 다음 표에-Office 365에 따라 이벤트가 발생 하는의 서비스-다중 속성의 **세부 정보** 열에 있습니다. **이 속성이 설치 된 Office 365 서비스** 열에는 서비스 및 속성이 포함 된 활동 (사용자 또는 관리자)의 유형을 나타냅니다. 이러한 속성에 대 한 또는이 항목에 나열 될 수 있는 속성에 대 한 자세한 내용은 [Office 365 관리 활동 API 스키마](https://go.microsoft.com/fwlink/p/?LinkId=717993)를 참조 하십시오.
  
> [!TIP]
> Excel에서이 열을 여러 열으로 분할 하 각 속성에는 자체 열 갖습니다 파워 쿼리를 사용할 수 있습니다. 이렇게 하면 이러한 속성 중 하나 이상이에서 정렬 및 필터링 있습니다. 이 작업을 수행 하는 방법을 알아보려면 [분할 (전원 쿼리) 텍스트의 열에서](https://support.office.com/article/5282d425-6dd0-46ca-95bf-8e0da9539662)에서 "구분 기호로 사용 하 여 열을 분할" 섹션을 참조 하십시오. 
  
|**속성**|**설명**|**이 속성에는 office 365 서비스**|
|:-----|:-----|:-----|
|작업자  <br/> |작업을 수행 하는 사용자 또는 서비스 계정입니다. |Azure Active Directory  <br/> |
|AddOnName  <br/> |추가 기능을 추가, 제거 또는 팀에서 업데이트 된의 이름입니다. 추가 기능에서 Microsoft 팀의 유형은 bot, 연결선, 또는 탭 합니다.  <br/> |Microsoft Teams  <br/> |
|AddOnType  <br/> |종류 추가, 제거 되었거나 팀에서 업데이트 하는 추가 기능입니다. 다음 값에는 추가 기능 유형을 나타냅니다.<br/> **1** -bot을 나타냅니다.<br/> **2** -커넥터를 나타냅니다.<br/> **3** -탭을 나타냅니다. |Microsoft Teams  <br/> |
|AzureActiveDirectoryEventType  <br/> |Azure Active Directory 이벤트의 형식입니다. 다음 값은 이벤트의 종류를 나타냅니다.<br/> **0** -계정 로그인 이벤트를 나타냅니다.<br/> **1** -Azure 응용 프로그램 보안 이벤트를 나타냅니다. |Azure Active Directory  <br/> |
|ChannelGuid  <br/> |Microsoft 팀의 채널의 ID입니다. 채널에 있는 팀 **TeamName** 및 **TeamGuid** 속성에 의해 식별 됩니다.<br/> |Microsoft Teams  <br/> |
|ChannelName  <br/> |Microsoft 팀의 채널의 이름입니다. 채널에 있는 팀 **TeamName** 및 **TeamGuid** 속성에 의해 식별 됩니다.<br/> |Microsoft Teams  <br/> |
|Client  <br/> |클라이언트 장치, 운영 체제, 장치 및 로그인 이벤트 (예: Nokia Lumia 920;에 사용 되는 장치 브라우저 Windows Phone 8; IE 모바일 11)입니다.  <br/> |Azure Active Directory  <br/> |
|ClientInfoString  <br/> |브라우저 버전, Outlook 버전 및 모바일 장치 정보 등의 작업을 수행 하는데 사용 된 전자 메일 클라이언트에 대 한 정보  <br/> |Exchange (사서함 활동)  <br/> |
|ClientIP  <br/> |작업 기록 되었는지 때 사용 된 장치의 IP 주소입니다. IP 주소는 IPv4 또는 IPv6 주소 형식으로 표시 됩니다.  <br/> |Exchange와 Azure Active Directory  <br/> |
|ClientIPAddress  <br/> |ClientIP와 동일 합니다.  <br/> |SharePoint  <br/> |
|CreationTime  <br/> |날짜 및 시간에서 UTC Coordinated Universal Time ()는 작업을 수행 하는 사용자입니다.  <br/> |모두  <br/> |
|DestinationFileExtension  <br/> |복사 또는 이동 된 파일의 파일 확장명입니다. 이 속성은 FileCopied 및 FileMoved 사용자 작업에 대해서만 표시 됩니다.  <br/> |SharePoint  <br/> |
|DestinationFileName  <br/> |파일의 이름을 복사 하거나 이동 합니다. 이 속성은 FileCopied 및 FileMoved 작업에 대해서만 표시 됩니다.  <br/> |SharePoint  <br/> |
|DestinationRelativeUrl  <br/> |파일을 복사 하거나 이동 대상 폴더의 URL입니다. **SiteURL**, **DestinationRelativeURL**, 및 **DestinationFileName** 속성에 대 한 값의 조합이 복사한 파일에 대 한 전체 경로 이름을 **ObjectID** 속성에 대 한 값과 같습니다. 이 속성은 FileCopied 및 FileMoved 사용자 작업에 대해서만 표시 됩니다.<br/> |SharePoint  <br/> |
|EventSource  <br/> |SharePoint에서 이벤트가 발생 했음을 나타냅니다. 가능한 값은 **SharePoint** 및 **ObjectModel**합니다.<br/> |SharePoint  <br/> |
|ExternalAccess  <br/> |Exchange 관리 작업에 대 한 데이터 센터 서비스 계정이 나 Microsoft 데이터 센터 담당자가 조직에서 사용자가 또는 위임 된 관리자가 cmdlet을 실행 하는지 여부를 지정 합니다. **False** 값 cmdlet은 조직에서 사용자에 의해 실행 된 하는 것을 나타냅니다. 데이터 센터 담당자, 데이터 센터 서비스 계정 또는 위임 된 관리자를 통해 cmdlet을 실행 하는 값은 **True** 를 나타냅니다.<br/> Exchange 사서함 활동에 대 한 조직 외부 사용자가 사서함 액세스 하는지 여부를 지정 합니다.  <br/> |Exchange  <br/> |
|ExtendedProperties  <br/> |확장 된 속성에 대 한는 Azure Active Directory 이벤트입니다.  <br/> |Azure Active Directory  <br/> |
|ID  <br/> |보고서 항목의 ID입니다. ID는 고유 하 게 보고서 항목을 식별합니다.  <br/> |모두  <br/> |
|InternalLogonType  <br/> |내부용으로 예약 합니다.  <br/> |Exchange (사서함 활동)  <br/> |
|ItemType  <br/> |액세스 또는 수정 된 개체의 형식입니다. 가능한 값에는 **파일**, **폴더**, **웹**, **사이트**, **테 넌 트**및 **DocumentLibrary**포함 됩니다.<br/> |SharePoint  <br/> |
|LoginStatus  <br/> |발생 했을 수 있는 로그인 오류를 식별 합니다.  <br/> |Azure Active Directory  <br/> |
|LogonType  <br/> |사서함 액세스의 형식입니다. 다음 값은 사서함에 액세스 한 사용자의 종류를 나타냅니다.<br/><br/> **0** -사서함 소유자를 나타냅니다.<br/> **1** -관리자를 나타냅니다.<br/> **2** -대리자를 나타냅니다. <br/>**3** -Microsoft 데이터 센터에서 전송 서비스를 나타냅니다.<br/> **4** -Microsoft 데이터 센터에서 서비스 계정을 나타냅니다. <br/>**6** -위임 된 관리자를 나타냅니다. |Exchange (사서함 활동)  <br/> |
|MailboxGuid  <br/> |사서함에 액세스 하는 Exchange GUID입니다.  <br/> |Exchange (사서함 활동)  <br/> |
|MailboxOwnerUPN  <br/> |액세스 된 사서함을 소유한 사용자의 전자 메일 주소입니다.  <br/> |Exchange (사서함 활동)  <br/> |
|구성원  <br/> |추가 되거나 팀에서 제거 된 사용자를 나열 합니다. 다음 값은 사용자에 게 할당 된 역할 종류를 나타냅니다.<br/><br/> **1** -소유자 역할을 나타냅니다.<br/> **2** -구성원 역할을 나타냅니다.<br/> **3** -게스트 역할을 나타냅니다. <br/><br/>Members 속성에는 구성원의 전자 메일 주소 및 사용자 조직의 이름이 포함 됩니다.  <br/> |Microsoft Teams  <br/> |
|ModifiedProperties (이름, NewValue, OldValue)  <br/> |속성에 대 한 사이트 또는 사이트 모음 관리자 그룹의 구성원으로 사용자를 추가 하는 등의 관리 이벤트가 포함 됩니다. 속성 (예: 사이트 관리자 그룹)에 수정 된 속성의 이름이 포함 된 새 속성 값은 수정 된 (예: 사용자의 사이트 관리자 및 수정 된 개체의 이전 값으로 추가 되었습니다.  <br/> |모든 (관리 활동)  <br/> |
|ObjectID  <br/> |Exchange 관리자 감사 로깅, cmdlet에 의해 수정 된 개체의 이름입니다.  <br/> 개발자를 위한 SharePoint 작업, 파일 또는 사용자가 액세스 하는 폴더의 전체 URL 경로 이름입니다.  <br/> Azure AD 작업용으로 수정한 사용자 계정의 이름입니다.  <br/> |모두  <br/> |
|작업  <br/> |사용자 또는 관리자 작업의 이름입니다. 이 속성의 값 값에 해당 하는 **활동** 에 선택 된 드롭다운 목록입니다. 선택 된 **모든 작업에 대 한 결과 표시** 하는 경우 보고서 모든 서비스에 대 한 모든 사용자 및 관리자 작업에 대 한 항목이 포함 됩니다. Office 365 감사 로그에 기록 되는 작업 활동에 대 한 참조 **Audited 활동** 탭에서 [Office 365 보안에서 감사 로그를 검색 &amp; 준수 센터](search-the-audit-log-in-security-and-compliance.md)합니다.<br/> Exchange 관리 작업에 대 한이 속성은 실행 된 cmdlet의 이름을 식별 합니다.  <br/> |모두  <br/> |
|OrganizationID  <br/> |Office 365 조직에 대 한 GUID입니다.  <br/> |모두  <br/> |
|경로  <br/> |메시지에 액세스 하는 위치한 사서함 폴더의 이름입니다. 이 속성은 또한 where a 폴더 식별에 메시지를 만들거나 복사/이동 합니다.  <br/> |Exchange (사서함 활동)  <br/> |
|매개 변수  <br/> |Exchange 관리 작업, 이름 및 작업 속성에서 식별 되는 cmdlet과 함께 사용 된 모든 매개 변수에 대 한 값입니다.  <br/> |Exchange (관리 활동)  <br/> |
|RecordType  <br/> |레코드에 지정 된 작업의 형식입니다. 다음 값은 레코드 종류를 나타냅니다.<br/><br/> **1** -Exchange 관리자 감사 로그에서 레코드를 나타냅니다. <br/>**2** -선별 사서함 항목에서 수행 되는 작업에 대 한 Exchange 사서함 감사 로그에서 레코드를 나타냅니다. <br/>또한 **3** -Exchange 사서함 감사 로그에서 레코드를 나타냅니다. 이 레코드 종류 (예: 여러 항목을 지운 편지함 폴더로 이동 또는 여러 항목을 영구적으로 삭제) 원본 사서함에서 여러 항목에 대해 작업을 수행 하는 것을 나타냅니다.<br/>**4** -관리자 또는 사이트에 사용 권한을 할당 하는 사용자가 예: sharepoint에서 사이트 관리 작업을 나타냅니다. <br/>**6** -파일 또는 폴더와 관련 된 작업 보기 또는 파일을 수정 하는 사용자와 같은 sharepoint에서 나타냅니다. <br/>**8** -Azure Active Directory에서 수행 되는 관리 작업을 나타냅니다. <br/>**9** -Azure Active Directory에서 로그온 이벤트 OrgId를 나타냅니다. 이 레코드 종류는 사용 되지 않습니다.<br/>**10** -데이터 센터에서 Microsoft 담당자가 수행한 보안 cmdlet 이벤트를 나타냅니다. <br/>**11** -SharePoint에서 손실 방지 (DLP) 이벤트 데이터를 나타냅니다.<br/> **12** -이벤트 라를 나타냅니다. <br/>**13** -Exchange, DLP 정책 통합을 구성 하는 경우의 이벤트를 DLP를 나타냅니다. Exchange 전송 규칙을 기반으로 DLP 이벤트 지원 되지 않습니다.<br>**14** -SharePoint에서 공유 이벤트를 나타냅니다.<br/> **15** -Azure Active Directory에서 로그온 이벤트 나타냅니다 보안 토큰 서비스 (STS). <br/>**18** -나타냅니다 보안 &amp; 준수 센터 이벤트입니다. <br/>**20** -이벤트 Power BI를 나타냅니다. <br/>**21**-이벤트 Dynamics 365 나타냅니다.<br/>**22** -이벤트 Yammer를 나타냅니다. <br/>**23** -비즈니스 이벤트에 대 한 Skype를 나타냅니다. <br/>**24** -eDiscovery 이벤트를 나타냅니다. 이 레코드 종류 나타냅니다 콘텐츠 검색을 실행 하 고 보안에서 eDiscovery 사례를 관리 하 여 수행 된 활동 &amp; 준수 센터입니다. 자세한 내용은 감사 로그는 Office 365의 eDiscovery 활동에 대 한 검색을 참조 하십시오.<br/>**25, 26, 또는 27** -이벤트 Microsoft 팀의를 나타냅니다. <br/>**28** -피싱 및 맬웨어 이벤트에서 Exchange Online Protection 및 Office 365 고급 위협 보호 이벤트를 나타냅니다.<br/> **30** -이벤트 Microsoft 흐름을 나타냅니다.<br/> **32** -Microsoft 스트림 지정 된 이벤트입니다.<br/> **35** -이벤트 Microsoft Project를 나타냅니다. <br/> **36** -목록 이벤트 SharePoint를 나타냅니다.<br/> **40** -나타냅니다 보안 및 규정 준수 경고 신호에서 발생 하는 이벤트입니다.<br/> **41** -Office 365 고급 위협 보호의 안전한 링크 블록의 시간 및 블록 재정의 이벤트를 나타냅니다.<br/>**44** -이벤트 직장 분석을 나타냅니다. <br/>**47** -SharePoint, OneDrive 및 Microsoft 팀의 파일에 대 한 Office 365 고급 위협 보호에서 피싱 및 맬웨어 이벤트를 나타냅니다. |모두  <br/> |
|ResultStatus  <br/> |( **Operation** 속성에 지정 된) 작업 성공 했는지 여부를 나타냅니다.  <br/> Exchange 관리 작업에 대 한 값은 **True** (성공) 또는 **False** (실패).  <br/> |모두  <br/>|
|SecurityComplianceCenterEventType  <br/> |활동을 보안 했음을 나타냅니다 &amp; 준수 센터 이벤트입니다. 모든 보안 &amp; 준수 센터 활동 **0** 이 속성의 값이 포함 됩니다.<br/> |Office 365 보안 및 준수 센터  <br/> |
|SharingType  <br/> |자원으로 공유 하는 사용자에 게 할당 된 사용 권한을 공유의 형식입니다. 이 사용자는 **UserSharedWith** 속성에서 식별 됩니다.<br/> |SharePoint  <br/> |
|사이트  <br/> |파일 또는 사용자가 액세스 폴더가 있는 사이트의 GUID입니다.  <br/> |SharePoint  <br/> |
|SiteUrl  <br/> |파일 또는 사용자가 액세스 폴더가 있는 사이트의 URL입니다.  <br/> |SharePoint  <br/> |
|SourceFileExtension  <br/> |사용자가 액세스 하는 파일의 파일 확장명입니다. 이 속성에 액세스 하는 개체 폴더인 경우 비어 있습니다.  <br/> |SharePoint  <br/> |
|SourceFileName  <br/> |파일 또는 사용자가 액세스 하는 폴더의 이름입니다.  <br/> |SharePoint  <br/> |
|SourceRelativeUrl  <br/> |사용자가 액세스 하는 파일이 들어 있는 폴더의 URL입니다. **SiteURL**, **SourceRelativeURL**, 및 **SourceFileName** 속성에 대 한 값의 조합이 사용자가 액세스 하 여 파일에 대 한 전체 경로 이름을 **ObjectID** 속성에 대 한 값과 같습니다.<br/> |SharePoint  <br/> |
|Subject  <br/> |에 액세스 하는 메시지의 제목 줄.  <br/> |Exchange (사서함 활동)  <br/> |
|유형 매니저 탭  <br/> | 탭의 종류를 추가, 제거 또는 팀에서 업데이트 합니다. 이 속성에 대 한 사용 가능한 값은:<br/><br/> **Excelpin** -Excel 탭 합니다.  <br/> **확장** -모든 자사 및 타사 앱입니다. 예: 플래너, VSTS, 및 양식입니다.  <br/> **메모** -OneNote 탭 합니다.  <br/> **Pdfpin** -A PDF 탭 합니다.  <br/> **Powerbi** -A PowerBI 탭 합니다.  <br/> **Powerpointpin** -A PowerPoint 탭 합니다.  <br/> **Sharepointfiles** -A SharePoint 탭 합니다.  <br/> **웹 페이지** -고정 된 웹사이트 탭 합니다.  <br/> **위 키 탭** -wiki 탭 합니다.  <br/> **Wordpin** -A Word 탭 합니다.  <br/> |Microsoft Teams  <br/> |
|대상  <br/> |( **Operation** 속성에서 확인 된) 작업에서 수행한 사용자입니다. 예, 게스트 사용자는 SharePoint 또는 Microsoft 팀에 추가 되 면 해당 사용자가이 속성에 나열 됩니다.<br/> |Azure Active Directory  <br/> |
|TeamGuid  <br/> |Microsoft 팀에 팀의 ID입니다.  <br/> |Microsoft Teams  <br/> |
|TeamName  <br/> |Microsoft 팀에 팀의 이름입니다.  <br/> |Microsoft Teams  <br/> |
|UserAgent  <br/> |사용자의 브라우저에 대 한 정보를 제공 합니다. 이 정보는 브라우저에서 제공 됩니다.  <br/> |SharePoint  <br/> |
|UserDomain  <br/> |Id 정보 (작업자) 하는 사용자의 테 넌 트 조직에 대 한 작업을 수행한 사용자입니다.  <br/> |Azure Active Directory  <br/> |
|사용자 Id  <br/> |기록 되는 레코드를 발생 시킨 ( **Operation** 속성에 지정 된) 작업을 수행한 사용자입니다. Note 레코드 시스템 계정 (예: SHAREPOINT\system 또는 NT 권한 \ 시스템)에 의해 수행 되는 활동에 대 한 감사 로그에도 포함 됩니다.<br/> |모두  <br/> |
|UserKey  <br/> |**UserID** 속성에서 식별 한 사용자에 대 한 대체 ID입니다. 예,이 속성은 SharePoint의 사용자에 의해 수행 되는 이벤트에 대 한 passport 고유 ID (PUID) 채워집니다. 또한이 속성 다른 서비스 및 시스템 계정에 의해 수행 되는 이벤트의 발생 하는 이벤트에 대 한 **UserID** 속성으로 같은 값을 지정 될 수 있습니다.<br/> |모두  <br/> |
|UserSharedWith  <br/> |사용자를 자원으로 공유입니다. 이 속성은 **Operation** 속성의 값은 **SharingSet**하는 경우에 포함 합니다. 이 사용자가 보고서에 있는 **공유 대상** 열에도 표시 됩니다.<br/> |SharePoint  <br/> |
|UserType  <br/> |작업을 수행한 사용자의 형식입니다. 다음 값에는 사용자 유형을 나타냅니다.<br/> <br/> **0** -일반 사용자입니다. <br/>**2** -Office 365 조직에서 관리자입니다. <br/>**3** -A Microsoft 데이터 센터 관리자 또는 데이터 센터 시스템 계정입니다. <br/>**4** -시스템 계정입니다. <br/>**5** -응용 프로그램입니다. <br/>**6** -서비스 사용자입니다.<br/>**7** -사용자 지정 정책입니다.<br/>**8** -시스템 정책입니다. |모두  <br/> |
|Version  <br/> |기록 되는 활동 ( **작업** 속성에 의해 식별 된)의 버전 번호를 나타냅니다.  <br/> |모두  <br/> |
|작업량  <br/> |Office 365 서비스 활동 발생 했습니다. 이 속성에 대 한 사용 가능한 값은:<br/> <br/>**SharePoint<br/>OneDrive<br/>Exchange<br/>AzureActiveDirectory<br/>DataCenterSecurity<br/>준수<br/>라<br/>비즈니스를 위한 Skype<br/>SecurityComplianceCenter<br/>PowerBI<br/>CRM<br/>Yammer<br/>MicrosoftTeams<br/>ThreatIntelligence<br/>MicrosoftFlow<br/>MicrosoftStream<br/>DlpSharePointClassificationData<br/>프로젝트<br/>PowerApps<br/>직장 분석**|모두  <br/> |
||||
   
특정 이벤트의 세부 정보를 볼 때 **추가 정보** 를 클릭 하는 경우에 속성 위에서 설명한 하는 내용의 정보가 표시 됩니다. 
  
![감사 로그 이벤트 레코드의 자세한 속성을 보려면 자세한 정보를 클릭 합니다.](media/6df582ae-d339-4735-b1a6-80914fb77a08.png)
  

