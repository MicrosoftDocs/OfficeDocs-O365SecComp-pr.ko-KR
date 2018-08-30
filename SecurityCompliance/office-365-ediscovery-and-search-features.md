---
title: Office 365 eDiscovery 및 검색 기능 개요 (영문)
ms.author: robmazz
author: robmazz
manager: laurawi
ms.date: 8/21/2018
audience: ITPro
ms.topic: article
ms.service: Office 365 Administration
localization_priority: None
search.appverid:
- MET150
ms.collection: Strat_O365_Enterprise
description: EDiscovery 기능 및 투명도 및 감사 사용에 대 한 Office 365 내에서 다른 검색 기능 개요입니다.
ms.openlocfilehash: 2d5cc2533c195b51f685aebd8da4462518116905
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22533530"
---
# <a name="ediscovery-and-search-features"></a>eDiscovery 및 검색 기능 

## <a name="ediscovery"></a>eDiscovery
EDiscovery 기능 관리자, 규정 준수 관리자를 위한 단일 위치를 제공 하 고 권한이 있는 다른 사용자가 Office 365 사용자 작업에 포괄적인 조사를 수행할 수 있습니다. 전체 콘텐츠에 포함 하 고 적절 한 사용 권한 가진 보안 담당자 검색을 수행할 수 있습니다. 검색 결과는 동일한 결과 콘텐츠 검색에서 가져올 점을 제외 하 고에 적용 되는 모든 보류에 대해 eDiscovery 사례 만들어집니다. EDiscovery 검색의 결과 보안을 위해 암호화 하 고 [고급 eDiscovery](https://support.office.com/article/office-365-advanced-ediscovery-fd53438a-a760-45f6-9df4-861b50161ae4)를 사용 하 여 내보낸된 데이터를 분석할 수 있습니다.

## <a name="content-search"></a>콘텐츠 검색
[콘텐츠 검색](https://support.office.com/article/Run-a-Content-Search-in-the-Office-365-Security-Compliance-Center-61852fd9-fe8a-4880-a339-cb19ed3bff4a) 은 이전 eDiscovery 검색 도구를 통해 보안 및 향상 된 확장을 제공 하는 준수 센터와 성능 기능에서 새 eDiscovery 검색 도구. 비즈니스 위치에 대 한 사서함, 공용 폴더, SharePoint Online 사이트 및 OneDrive를 검색 하려면 콘텐츠 검색을 사용할 수 있습니다. 콘텐츠 검색은 매우 큰 검색 특별히 설계 되었습니다. 사서함 및 검색할 수 있는 사이트 수에 제한이 있습니다. 동시에 실행할 수 있는 검색 수에 제한이 있습니다. 후 검색, 콘텐츠 원본 수와 예상된 검색 결과 미리 보고 하거나 로컬 컴퓨터에 내보낼 수 있는 검색 페이지에서 세부 정보 창에 결과가 표시 되는 숫자를 실행 합니다. 조직에 Office 365 Enterprise E5 구독 있으면 수도 있습니다 [Office 365 고급 eDiscovery](http://go.microsoft.com/fwlink/p/?LinkID=620116)의 강력한 분석 기능을 사용 하 여 분석 [결과 준비](https://support.office.com/article/Run-a-Content-Search-in-the-Office-365-Security-Compliance-Center-61852fd9-fe8a-4880-a339-cb19ed3bff4a#prepare) 합니다.

## <a name="audit-log-search"></a>감사 로그 검색
Office 365 조직에 변경 내용을 추적 하는 것 외에도 고객은 감사 보고서를 볼 및 감사 로그 내보내기도 수 있습니다. Office 365 테 넌 트에 대 한 감사를 사용 하도록 설정, 사용자 및 해당 테 넌 트에 대 한 관리 활동 이벤트 로그에 기록 정의와 검색할 수 있습니다. 예, 사서함 감사 로깅을 사서함 소유자 이외의 사용자가 사서함에서 수행 하는 작업을 추적을 사용할 수 있습니다. 또한 규정 준수 관리자는 관리자가 사용자 관리 작업을 수행 하거나 지난 90 일 동안에서 테 넌 트 구성 변경 작업을 수행 하는 경우 또는 사용자가 보거나에서 특정 문서를 다운로드 하는 경우 참조를 검색 및 필터링 기능을 사용할 수 있습니다. 검색 결과는 사용자 또는 관리자가 수행 된 특정 활동에 대 한 중요 한 법적 정보 포함 될 수 있습니다. 사용자 및 Office 365에 로깅되는 관리 작업에 대 한 설명은 [Office 365의 Audited 활동](https://support.office.com/article/Search-the-audit-log-in-the-Office-365-Security-Compliance-Center-0d4d0f35-390b-4518-800e-0c7ec95e946c#auditlogevents) 을 참조 하십시오.

SharePoint Online 및 비즈니스용 OneDrive에서 발생 한 이벤트의 발생의 30 분 이내 로그에 표시 됩니다. Exchange Online에서 이벤트 발생의 24 시간 내에서 감사 로그에 표시 됩니다. Azure AD에서 로그인 이벤트는 발생의 시간 (분) 내에서 사용할 수 및 Azure AD에서 다른 디렉터리 이벤트는 발생의 24 시간 내에서 사용할 수 있습니다. 추가 분석을 위해 감사 로그 검색 결과의 이벤트를 내보낼 수도 있습니다. (50, 000 항목의 최대 단일 감사 로그 검색에서 내보낼 수 있습니다. 이 제한 하는 더 많은 항목을 내보내려면, 날짜 범위를 줄이거나 여러 감사 로그 검색을 실행 하십시오.)

다음 표에서 일부 활동 보고서에 표시 되는 정보를 자세히 설명 합니다. [Office 365에서 자세한 속성 감사 로그에](https://support.office.com/article/detailed-properties-in-the-office-365-audit-log-ce004100-9e7f-443e-942b-9b04098fcfc3
) 대 한 속성의 각 Office 365 작업으로 수집 하는 방법에 대 한 자세한 내용은 참조 하십시오.

| 속성 | 설명 |
|----------------|----------------------------------------------------------------------------------------------------------------------|
| 날짜 | 이벤트의 날짜 및 시간 |
| 사용자 | 작업을 수행한 사용자 |
| ClientIP | 작업 기록 되었는지 때 사용 된 장치의 IPv4 또는 IPv6 주소입니다. |
| CreationTime | 날짜 및 시간에서 UTC Coordinated Universal Time ()는 작업을 수행 하는 사용자입니다. |
| EventSource | 이벤트가 발생 했음을 나타냅니다. 가능한 값은 SharePoint 및 ObjectModel 합니다. |
| ID | 보고서 항목의 ID입니다. ID는 고유 하 게 보고서 항목을 식별합니다. |
| 작업 | 사용자 또는이 사용자 작업에 대 한 표시 결과에서 선택한 값에 해당 하는 작업의 이름입니다. |
| OrganizationId | 이벤트가 발생 하는 조직의 Office 365 서비스에 대 한 GUID입니다. |
| UserAgent | 브라우저에 의해 제공 된 사용자의 브라우저에 대 한 정보를 제공 합니다. |
| 사용자 Id | 기록 되는 레코드를 발생 시킨 (Operation 속성에 지정 된) 작업을 수행한 사용자입니다. |
| UserType | 작업을 수행한 사용자의 형식입니다. 다음 값에는 사용자 유형을 나타냅니다. |
|  | 0은 일반 사용자를 나타냅니다. |
|  | 2는 Office 365 조직에서 관리자를 나타냅니다. |
|  | 3에는 Microsoft 데이터 센터 관리자 또는 데이터 센터 시스템 계정을 나타냅니다. |
| 작업량 | Office 365 서비스 활동 발생 했습니다. 이 속성에 대 한 가능한 값은. |
|  | Exchange Online |
|  | SharePoint Online |
|  | 비즈니스용 OneDrive |
|  | Azure Active Directory 보고서 |


Office 365를 검색 하는 자세한 단계에 대 한 감사 로그는 [Office 365 보안 및 규정 준수 센터에서 검색 감사 로그를](https://support.office.com/article/Search-the-audit-log-in-the-Office-365-Security-Compliance-Center-0d4d0f35-390b-4518-800e-0c7ec95e946c)참조 하십시오.

## <a name="search-unified-audit-log"></a>통합 된 감사 로그를 검색 합니다.
보안 및 규정 준수 센터의 감사 로그 검색 기능 통합된 감사 로그 검색에 사용할 수 있습니다. 또한 office 365 원격 PowerShell을 사용 하 여이 로그를 검색 하는 기능을 제공 합니다. 특히, 비즈니스 및 Azure AD에 대 한 Exchange Online, SharePoint Online, OneDrive에서 사용자 작업에 관련 된 이벤트의 통합된 감사 로그를 검색 하려면 Exchange Online PowerShell에서 [검색 UnifiedAuditLog cmdlet](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-audit/Search-UnifiedAuditLog?view=exchange-ps) 를 사용할 수 있습니다. 모든 이벤트는 지정한 날짜 범위 내에서 검색할 수 또는 대상 개체 또는 작업을 수행한 사용자가 특정 작업을 등의 특정 조건을 기준으로 결과 필터링 할 수 있습니다. 관리자는 큰 날짜 범위 검색을 분할 하려면 Exchange Online PowerShell 세션을 동시에 실행 하는 3까지를 사용할 수 있습니다.
