---
title: Microsoft 365 준수 센터의 새로운 기능
ms.author: brendonb
author: brendonb
manager: laurawi
ms.date: ''
audience: Admin
ms.topic: reference
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- SPO160
- MOE150
- MET150
ms.assetid: e3c6df61-8513-499d-ad8e-8a91770bff63
ms.collection:
- M365-security-compliance
description: Microsoft 365 준수 센터의 기능과 마찬가지로, 도움말 콘텐츠는 항상 발전 하 고 있습니다. Microsoft에서는 피드백에 따라 계속 새 문서를 만들고, 기존 기사를 업데이트 하 고, 변경 작업을 수행 하 고 있습니다. 이번 달의 새로운 기능과 업데이트 된 기능에 대해 알아보세요.
ms.openlocfilehash: e7600c2f84d0b591c6114c2a61c77d8e2c664056
ms.sourcegitcommit: 9fd606e8d912f4507fbcd9f1fcb9dfcfd20de08b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/13/2019
ms.locfileid: "36980804"
---
# <a name="recent-updates-to-microsoft-365-compliance-content"></a>Microsoft 365 준수 콘텐츠에 대 한 최신 업데이트

Microsoft 365 준수 센터의 기능과 마찬가지로, 도움말 콘텐츠는 항상 발전 하 고 있습니다. Microsoft에서는 피드백에 따라 계속 새 문서를 만들고, 기존 기사를 업데이트 하 고, 변경 작업을 수행 하 고 있습니다. 이번 달에 새로 추가 되 고 업데이트 된 내용을 확인 하려면 아래를 확인 하세요.

> [!TIP]
> Microsoft 365 준수 센터의 최신 기능 업데이트를 계속 해 서 확인 하려면 [microsoft 365 준수 센터에서 새롭게 소개](whats-new.md)되는 내용을 참조 하세요.

## <a name="august-2019"></a>8 월 2019

### <a name="auditing"></a>감사

[사서함 감사 관리](enable-mailbox-auditing.md#more-information) 고칠<br>E5 라이선스를 사용 하는 사용자나 관리자가 사서함 감사를 수동으로 설정 하는 사서함에 대 한 사서함 감사 로그 이벤트를 사용 하는 방법에 대 한 세부 정보가 추가 되었습니다. 또한 Exchange Online PowerShell에서 **search-mailboxauditlog** cmdlet을 사용 하 여 E5 라이선스 없이 사용자에 대 한 사서함 감사 로그를 검색 하는 방법에 대 한 새로운 지침이 제공 됩니다.

[일반적인 시나리오 문제를 해결 하기 위해 Office 365 감사 로그 검색](auditing-troubleshooting-scenarios.md#investigate-why-there-was-a-successful-login-by-a-user-outside-your-organization) 고칠<br>통과 인증을 사용 하 여 외부 사용자의 성공한 로그인을 조사 하는 방법에 대 한 새로운 섹션입니다.

### <a name="content-search--ediscovery"></a>콘텐츠 검색 & eDiscovery

[콘텐츠 검색에 대 한 권한 필터링 구성](permissions-filtering-for-content-search.md#using-a-filters-list-to-combine-filter-types) 고칠<br>단일 검색 권한 필터에 사서함 및 사이트 필터를 추가 하는 데 사용할 수 있는 필터 목록 사용에 대 한 세부 정보가 추가 되었습니다.

[Office 365의 콘텐츠 검색](content-search.md#searching-disconnected-or-de-licensed-mailboxes) 고칠<br>연결이 끊어지거나 사용이 허가 되지 않은 사서함 검색에 대 한 세부 정보가 추가 되었습니다.

[Office 365의 콘텐츠 검색](content-search.md#searching-for-content-in-a-sharepoint-multi-geo-environment) 고칠<br>
[Office 365에서 eDiscovery 조사에 대 한 준수 경계 설정](set-up-compliance-boundaries.md#searching-and-exporting-content-in-multi-geo-environments) 고칠<br>SharePoint 다중 지리적 환경에서 콘텐츠를 검색 하는 방법에 대 한 세부 정보를 두 문서에 모두 추가 했습니다.

### <a name="data-governance"></a>데이터 거버넌스

[Office 365의 무제한 보관 개요](unlimited-archiving.md#how-auto-expanding-archiving-works) 고칠<br>Office 365에서 총 1tb의 추가 저장소에 대해 최대 20 개의 보조 보관 파일을 추가 하는 방법에 대 한 세부 정보가 추가 되었습니다.

### <a name="data-investigations"></a>데이터 조사

[원래 위치에서 항목 삭제](datainvestigations/delete-items-from-original-locations.md) 새로운<br>이제 미리 보기에서 사용할 수 있으며, 증거 집합에서 항목을 선택한 다음 Exchange, SharePoint 및 OneDrive의 원래 위치에서이를 일시 삭제할 수 있습니다.

[Microsoft 365에서 데이터 유출 인시던트 관리](datainvestigations/manage-data-spillage-incidents.md#step-4-delete-the-spilled-data) 고칠<br>새 ' 원래 위치에서 항목 삭제 ' 기능을 사용 하 여 분산 된 데이터를 삭제 하는 방법에 대 한 세부 정보가 추가 되었습니다.

### <a name="permissions"></a>사용 권한

[Microsoft 365 준수 센터 및 microsoft 365 보안 센터의 사용 권한](permissions-microsoft-365-compliance-security.md) 새로운<br>새 Azure Active Directory 역할 그룹이 공개 미리 보기로 릴리스 되었습니다.

### <a name="records-management"></a>레코드 관리

[파일 계획 관리자 개요 (업데이트 됨)](file-plan-manager.md#export-all-existing-retention-labels-to-analyze-andor-perform-offline-reviews)<br>Excel 서식 파일에 사용할 유효한 값을 나열 하는 표가 추가 되었습니다.

### <a name="supervision"></a>감독

[Office 365의 감독 정책](supervision-policies.md) 고칠<br>Office 365 그룹과 메일 그룹 지원에 대해 설명 하 고 전자 메일 및 첨부 파일 둘 다에서 키워드 일치에 대 한 지침을 추가 했으며 팀 채널 내에서 Outlook을 지원 합니다.

### <a name="windows-information-protection"></a>Windows Information Protection

[WIP (Windows Information Protection)에 사용할 인식 된 Microsoft 앱 목록](https://docs.microsoft.com/windows/security/information-protection/windows-information-protection/enlightened-microsoft-apps-and-wip) 고칠 <br>Microsoft 3D 뷰어는 이제 인식 된 앱입니다.
