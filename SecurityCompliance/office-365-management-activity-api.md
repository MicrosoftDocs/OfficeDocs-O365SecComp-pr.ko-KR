---
title: Office 365 관리 작업 API
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
ms.collection:
- Strat_O365_IP
- M365-analytics
description: Office 365 관리 활동 API에 대 한 간략 한 요약입니다.
ms.openlocfilehash: ca5517d3049830cd7be912b2e2e47a34a866aca0
ms.sourcegitcommit: c94cb88a9ce5bcc2d3c558f0fcc648519cc264a2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/20/2019
ms.locfileid: "30090561"
---
# <a name="office-365-management-activity-api"></a><span data-ttu-id="82faa-103">Office 365 관리 작업 API</span><span class="sxs-lookup"><span data-stu-id="82faa-103">Office 365 Management Activity API</span></span>
<span data-ttu-id="82faa-p101">Microsoft는 관리자가 Office 365 테 넌 트에 대 한 집계 된 트랜잭션 정보를 가져올 수 있도록 하는 보고 서비스를 제공 합니다. [Office 365 관리 활동 API](https://docs.microsoft.com/office/office-365-management-api/office-365-management-apis-overview) 는 인증을 위해 업계 표준 RESTful 디자인 및 OAuth v2를 사용 하므로 데이터 검색 및 시각화 도구 및 응용 프로그램으로 ingesting을 쉽게 시험해 볼 수 있습니다. 이 API는 Office 365의 사용자, 관리자, 작업 및 보안 작업에 대 한 정보를 포함 하는 데이터 피드를 제공 합니다. 데이터는 규정 목적에 따라 유지 되거나, 온-프레미스 인프라 또는 기타 원본에서 확보 한 로그 데이터와 함께 기업 전체의 운영, 보안 및 규정 준수를 위한 모니터링 솔루션을 구축 하는 데 사용 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="82faa-p101">Microsoft provides reporting services that enable administrators to obtain aggregated transactional information about their Office 365 tenant. The [Office 365 Management Activity API](https://docs.microsoft.com/office/office-365-management-api/office-365-management-apis-overview) uses an industry-standard RESTful design and OAuth v2 for authentication, which makes it easy to start experimenting with retrieving data and ingesting it into visualization tools and applications. The API provides a data feed that includes information about user, administrator, operations, and security activity in Office 365. The data can be kept for regulatory purposes, or combined with log data procured from an on-premises infrastructure or other sources to build a monitoring solution for operations, security, and compliance across the enterprise.</span></span>

<span data-ttu-id="82faa-p102">office 365 관리 활동 API는 office 365 및 Azure Active Directory 활동 로그에서 다양 한 사용자, 관리자, 시스템 및 정책 작업과 이벤트에 대 한 정보를 제공 합니다. 이 API는 모든 서비스에서 공통적으로 사용 되는 필드가 10 개를 넘는 일관성 있는 감사 스키마를 제공 합니다. 이를 통해 조직은 이벤트 간의 쉬운 연결을 가능 하 게 하 고 데이터에 대 한 이유를 새로 만들 수 있습니다. 수십 개의 독립 소프트웨어 공급 업체 (isv)는 API를 기반으로 하는 Microsoft 및 구축 된 솔루션과 제휴 합니다. 일부 솔루션은 Office 365 데이터에만 초점을 맞춘 반면, 일부는 여러 클라우드 공급자 및 온-프레미스 시스템에서 데이터를 수집 하 여 모든 작업, 보안 및 준수 관련 작업에 대 한 통합 된 보기를 만들 수 있는 기능을 제공 합니다. 자세한 내용은 [Office 365 관리 활동 API 참조](https://docs.microsoft.com/office/office-365-management-api/office-365-management-activity-api-reference)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="82faa-p102">The Office 365 Management Activity API provides information about various user, admin, system, and policy actions and events from Office 365 and Azure Active Directory activity logs. The API provides a consistent audit schema with over 10 fields that are in common across all the services. This allows organizations to make easy connections between events, and it enables new ways to reason over the data. Dozens of Independent Software Vendors (ISVs) have partnered with Microsoft and built solutions based on the API. Some solutions are focused solely on Office 365 data, while others provide the ability to ingest data from multiple cloud providers and on-premises systems to create a unified view of all operations, security, and compliance-related activity. For more information, see the [Office 365 Management Activity API reference](https://docs.microsoft.com/office/office-365-management-api/office-365-management-activity-api-reference).</span></span>
