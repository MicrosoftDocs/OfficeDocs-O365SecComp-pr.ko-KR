---
title: Office 365의 감사 및 보고
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
description: 감사 및 보고 기능으로 Office 365 서비스 보증 내에서 개요입니다.
ms.openlocfilehash: 055a24523260bf14220d5436dcdd010f31f5d8cd
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22533776"
---
# <a name="auditing-and-reporting-in-office-365"></a>Office 365의 감사 및 보고

## <a name="introduction"></a>소개
Microsoft 클라우드 서비스를 여러 감사 및 보고 고객 사용자 및 Exchange Online 및 SharePoint Online 테 넌 트 구성 설정에 대 한 변경 내용 등 자신의 테 넌 트 내의 관리 작업을 추적 하는데 사용할 수 있는 기능 포함 문서 및 기타 항목에 사용자가 변경한 하 고 있습니다. 고객은 감사 정보 및 클라우드 서비스에서 사용할 수 있는 보고서를 사용 하 여 보다 효율적으로 사용자 환경에서 관리, 위험을 완화 및 규정 준수 의무를 충족 수 있습니다.

## <a name="office-365-security--compliance-center"></a>Office 365 보안 및 준수 센터
[Office 365 보안 및 규정 준수 센터](https://support.office.com/article/Go-to-the-Office-365-Security-Compliance-Center-7e696a40-b86b-4a20-afcc-559218b7b1b8) Office 365의 데이터를 보호 하는 것에 대 한 통합 포털 이며 다양 한 감사 및 보고 기능을 포함 합니다. Office 365 준수 센터의 발전 것입니다. 보안 및 규정 준수 센터 데이터를 사용 하는 조직에서는 위해 특별히 고안 된 보호 또는 규정 준수 요구 사항 또는 하는 사용자 및 관리자가 작업을 감사를 선택 합니다. 조직의 Office 365 데이터를 모두에 대 한 규정 준수를 관리 하는 보안 및 규정 준수 센터를 사용할 수 있습니다. 보안 및 규정 준수 센터에 액세스할 수 [http://protection.office.com](http://protection.office.com/) 프로그램 Office 365 관리자 계정을 사용 하 여 합니다.

보안 및 규정 준수 센터에는 여러 기능에 대 한 액세스를 제공 하는 탐색 창이 포함 됩니다.
- **알림** -를 사용 하면 알림 관리, 보안 관련 경고를 볼 및 [고급 보안 관리](https://support.office.com/article/overview-of-office-365-cloud-app-security-81f0ee9a-9645-45ab-ba56-de9cbccab475)를 사용 하 여 고급 알림을 관리할 수 있습니다. 
- **사용 권한** -사용 하면 조직에서 사람에 게 규정 준수 관리자, 관리자, eDiscovery 및 다른 사용자와 같은 [사용 권한 할당](https://support.office.com/article/Give-users-access-to-the-Office-365-Security-Compliance-Center-2cfce2c8-20c5-47f9-afc4-24b059c1bd76) 을 보안 및 규정 준수 센터에 작업을 수행할 수 있도록 합니다. 보안 및 규정 준수 센터의 대부분의 기능에 대 한 사용 권한을 할당할 수 있지만 Exchange 관리 센터 및 SharePoint 관리 센터를 사용 하 여 다른 사용 권한을 구성 해야 합니다.
- **위협 관리** -를 사용 하면 만들고 [Office 365 모바일 장치 관리](https://support.office.com/article/Overview-of-Mobile-Device-Management-for-Office-365-faa7d8e5-645d-4d59-839c-c8d4c1869e4a)사용 하 여 전자 메일 필터링을 구성 하 여 조직에 대 한 [데이터 손실 방지](https://support.office.com/article/Overview-of-data-loss-prevention-policies-1966b2a7-d1e2-4d92-ab61-42efbb137f5e) (DLP) 정책 설정 하는 장치 관리 정책을 적용할 수 있습니다. 맬웨어 방지, DomainKeys 식별 된 메일 (DKIM), 안전한 첨부 파일, 안전 링크 및 앱 사용 권한입니다.
- **데이터 관리 방식** - [전자 메일 또는 Office 365에 다른 시스템에서 SharePoint 데이터를 가져올](https://support.office.com/article/Import-PST-files-or-SharePoint-data-to-Office-365-ba688e0a-0fcb-4bd7-8e57-2b669564ea84) [구성 보관 사서함](https://support.office.com/article/Enable-archive-mailboxes-in-the-Office-365-Security-Compliance-Center-268a109e-7843-405b-bb3d-b9393b2342ce)을 사용 하면 및 전자 메일 및 기타 콘텐츠 조직 내에 대 한 [보존 정책](https://support.office.com/article/Retention-in-the-Office-365-Security-Compliance-Center-2a0fc432-f18c-45aa-a539-30ab035c608c) 을 설정 합니다.
- **검색 및 조사** -Exchange Online 사서함, 그룹 및 공용 폴더, SharePoint에 걸쳐 활동으로 드릴 신속 하 게 하는 [콘텐츠 검색](https://support.office.com/article/Run-a-Content-Search-in-the-Office-365-Security-Compliance-Center-61852fd9-fe8a-4880-a339-cb19ed3bff4a), [감사 로그](https://support.office.com/article/Search-the-audit-log-in-the-Office-365-Security-Compliance-Center-0d4d0f35-390b-4518-800e-0c7ec95e946c), 격리 및 [eDiscovery 사례 관리](https://support.office.com/article/Manage-eDiscovery-cases-in-the-Office-365-Security-Compliance-Center-edea80d6-20a7-40fb-b8c4-5e8c8395f6da) 도구를 제공 합니다. 온라인으로 비즈니스용 OneDrive 하 고 있습니다.
- **보고서** -를 사용 하면 신속 하 게 비즈니스, Exchange Online 및 Azure AD에 대 한 개발자를 위한 SharePoint Online, OneDrive [보고서](https://support.office.com/article/Reports-in-the-Office-365-Security-Compliance-Center-7acd33ce-1ec8-49fb-b625-43bac7b58c5a) 에 액세스할 수 있습니다.
- **서비스 보증** -Microsoft 보안, 개인 정보 및 Office 365, Azure, Microsoft Dynamics CRM Online, Microsoft Intune 하 고 다른 클라우드 서비스에 대 한 글로벌 표준 준수를 유지 관리 하는 방법에 대 한 정보를 제공 합니다. 또한 타사 ISO, SOC, 및 기타 감사 보고서를 뿐아니라 테스트 및 Office 365의 타사 감사자에 의해 검증 된 다양 한 컨트롤에 대 한 세부 정보를 제공 하는 감사 컨트롤에 대 한 액세스를 포함 합니다.

## <a name="service-assurance"></a>서비스 보증
대부분의 고객의 규제 업계는 광범위 한 규정 준수 요구 사항에 따라 달라 집니다. 고객 자신의 위험 평가 수행 하려면 Office 365 보안 및 개인정보 자신의 데이터를 유지 관리 하는 방법에 대 한 자세한 정보가 필요한 경우가 많습니다. Microsoft 보안 및 해당 클라우드 서비스에서 고객 데이터의 개인정보 보호 하 고 해당 작업과 독립 준수 보고서 및 평가에 쉽게 액세스할 수의 투명 한 보기를 제공 하 여 고객 신뢰를 획득 커밋됩니다.

서비스 보증 투명도 작업과 Microsoft 보안, 개인 정보 및 Office 365에서 고객 데이터의 규정 준수를 유지 관리 하는 방법에 대 한 정보를 제공 합니다. 데이터 암호화, 데이터 복구, 보안 사고 관리 등 Office 365 항목에서 백서, Faq 및 기타 자료 (영문)의 라이브러리와 함께 제 3 자 감사 보고서를 포함 되어있습니다. 고객 자체 규정 위험 평가 수행 하려면이 정보를 사용할 수 있습니다. 규정 준수 관리자 사용자에 액세스할 수 있도록 서비스 보증 "서비스 보증 사용자" 역할을 할당할 수 있습니다. 테 넌 트 관리자는 [Microsoft 클라우드 서비스를 신뢰 포털](http://aka.ms/STP) (STP)을 통해 서비스 보증 대시보드에서 정보에 액세스할 수 있는 독립 감사자와 같은 외부 사용자를 제공할 수도 있습니다. STP에 액세스 하는 방법에 대 한 자세한 내용은 방문 하 여 [시작 서비스를 신뢰 포털 Office 365에 대 한 비즈니스, Azure, 및 Dynamics CRM Online 구독](http://aka.ms/STPHelp)합니다.

## <a name="onedrive-for-business-admin-center"></a>비즈니스 관리 센터에 대 한 OneDrive
새 Microsoft OneDrive 관리 센터를 사용 하면 신속 하 게 하 고 한곳에서 비즈니스 설정에 대 한 조직의 OneDrive 쉽게 관리할 수입니다. OneDrive 관리 센터를 사용 하려면 onedrive.com에 대 한 액세스를 허용 해야 합니다. 또한 조직에 대 한 전역 관리자 또는 SharePoint 관리자 역할을 가진 사용자 지정 관리 이어야 합니다. 비즈니스 관리 센터에 미리 보기에 비즈니스용 OneDrive에 액세스 [https://admin.onedrive.com](https://admin.onedrive.com/)합니다.

감사 로그를 검색, DLP, 보존, eDiscovery, 작업 및 경고와 같은 주요 시나리오에 대 한 Office 365 보안 및 규정 준수 센터에 대 한 링크가 있는 관리자를 제공 하는 준수 영역을 포함 하는 주요 기능입니다.

## <a name="related-links"></a>관련된 링크
- [eDiscovery 및 검색 기능](office-365-ediscovery-and-search-features.md)
- [Office 365 보고 기능](office-365-reporting-features.md)
- [Office 365 관리 작업 API](office-365-management-activity-api.md)
- [Office 365 사서함 마이그레이션](office-365-mailbox-migrations.md)
- [Office 365 엔지니어링에 대한 내부 로깅](office-365-internal-logging.md)