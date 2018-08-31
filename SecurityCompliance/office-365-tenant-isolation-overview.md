---
title: Office 365 테 넌 트 격리
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
description: Microsoft Office 365에 대 한 테 넌 트 격리를 적용 하는 방법을 간략하게 설명 합니다.
ms.openlocfilehash: fcf66ee65c2a4cfdf73ae0eac77f54bd555d059d
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22533561"
---
# <a name="tenant-isolation-in-office-365"></a><span data-ttu-id="c0a98-103">Office 365 테 넌 트 격리</span><span class="sxs-lookup"><span data-stu-id="c0a98-103">Tenant Isolation in Office 365</span></span>

<span data-ttu-id="c0a98-p101">클라우드 컴퓨팅 공유, 공통 인프라의 개념을 동시에 여러 다양 한 고객은, 규모의 경제 향하는의 주요 이점 중 하나입니다. 이 개념을 *다중 테 넌 트*라고 합니다. Microsoft은 클라우드 서비스에 대 한 다중 테 넌 트 아키텍처 엔터프라이즈 수준의 보안, 기밀성, 개인정보 보호, 무결성 및 가용성 표준을 지원 하는지 확인 하려면 계속 작동 합니다.</span><span class="sxs-lookup"><span data-stu-id="c0a98-p101">One of the primary benefits of cloud computing is concept of a shared, common infrastructure across numerous customers simultaneously, leading to economies of scale. This concept is called *multi-tenancy*. Microsoft works continuously to ensure that the multi-tenant architectures of our cloud services support enterprise-level security, confidentiality, privacy, integrity, and availability standards.</span></span>

<span data-ttu-id="c0a98-107">중요 한 투자 및 [신뢰할 수 있는 컴퓨팅](https://www.microsoft.com/en-us/twc/default.aspx) 및 [보안 개발 수명 주기](http://www.microsoft.com/security/sdl/default.aspx)에서 수집 된 환경에 따라, Microsoft 클라우드 서비스는 모든 잠재적으로 유해한 모든 테 넌 트 되었는지 가정 대상으로 설계 다른 테 넌 트 되 고, 보안 또는 다른 테 넌 트의 서비스에 영향을 주지 또는 다른 테 넌 트의 콘텐츠 액세스 (영문)에서 하나의 테 넌 트의 동작을 방지 하기 위해 보안 조치를 구현 했습니다.</span><span class="sxs-lookup"><span data-stu-id="c0a98-107">Based upon the significant investments and experience gathered from [Trustworthy Computing](https://www.microsoft.com/en-us/twc/default.aspx) and the [Security Development Lifecycle](http://www.microsoft.com/security/sdl/default.aspx), Microsoft cloud services were designed with the assumption that all tenants are potentially hostile to all other tenants, and we have implemented security measures to prevent the actions of one tenant from affecting the security or service of another tenant, or accessing the content of another tenant.</span></span>

<span data-ttu-id="c0a98-108">다중 테 넌 트 환경에서 테 넌 트 격리를 유지 관리의 두 기본 목표는:</span><span class="sxs-lookup"><span data-stu-id="c0a98-108">The two primary goals of maintaining tenant isolation in a multi-tenant environment are:</span></span>
1.  <span data-ttu-id="c0a98-109">테 넌 트; 별 고객 내용에도 유출 되지 않도록, 또는 무단으로 액세스 방지 및</span><span class="sxs-lookup"><span data-stu-id="c0a98-109">Preventing leakage of, or unauthorized access to, customer content across tenants; and</span></span>
2.  <span data-ttu-id="c0a98-110">다른 테 넌 트에 대 한 서비스에 부정적인 영향을 하나의 테 넌 트의 동작을 방지</span><span class="sxs-lookup"><span data-stu-id="c0a98-110">Preventing the actions of one tenant from adversely affecting the service for another tenant</span></span>

<span data-ttu-id="c0a98-111">여러 양식은 보호 하는 고객을 그대로 유지 하는 Office 365 서비스 또는 응용 프로그램이 나 다른 테 넌 트 또는 포함 하 여 Office 365 시스템 자체에 정보에 무단으로 액세스 하지 못하도록 방지 하기 위해 Office 365 전체에서 구현 된:</span><span class="sxs-lookup"><span data-stu-id="c0a98-111">Multiple forms of protection have been implemented throughout Office 365 to prevent customers from compromising Office 365 services or applications or gaining unauthorized access to the information of other tenants or the Office 365 system itself, including:</span></span>
- <span data-ttu-id="c0a98-112">Office 365 서비스에 대 한 각 테 넌 트 내의 고객 콘텐츠의 논리적 격리 Azure Active Directory 권한 부여 및 역할 기반 액세스 제어를 통해 이루어집니다.</span><span class="sxs-lookup"><span data-stu-id="c0a98-112">Logical isolation of customer content within each tenant for Office 365 services is achieved through Azure Active Directory authorization and role-based access control.</span></span>
- <span data-ttu-id="c0a98-113">SharePoint Online에서는 저장소 수준에서 데이터 격리 메커니즘을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="c0a98-113">SharePoint Online provides data isolation mechanisms at the storage level.</span></span>
- <span data-ttu-id="c0a98-p102">Microsoft 엄격한 물리적 보안, 배경 차단 및 다중 계층된 암호화 전략을 사용 하 여 기밀성 및 고객 콘텐츠의 무결성을 보호 합니다. 모든 Office 365 데이터 센터는 실제에 액세스 하는 가장 필요한 팜 인쇄와의 생체 인식 컨트롤이 있습니다. 또한 모든 미국 기반 Microsoft 직원 채용 과정의 일부로 표준 배경 검사를 완료 해야 합니다. Office 365에 대 한 관리 액세스에 사용 되는 컨트롤에 대 한 자세한 내용은 [Office 365 관리 액세스 제어](office-365-administrative-access-controls-overview.md)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="c0a98-p102">Microsoft uses rigorous physical security, background screening, and a multi-layered encryption strategy to protect the confidentiality and integrity of customer content. All Office 365 datacenters have biometric access controls, with most requiring palm prints to gain physical access. In addition, all U.S.-based Microsoft employees are required to successfully complete a standard background check as part of the hiring process. For more information on the controls used for administrative access in Office 365, see [Office 365 Administrative Access Controls](office-365-administrative-access-controls-overview.md).</span></span>
- <span data-ttu-id="c0a98-p103">Office 365에서 BitLocker, 파일 당 암호화를 포함 하 여 전송 하 고 나머지 부분에서 고객 콘텐츠를 암호화 하는 서비스 측 기술을 사용 하 여 전송 계층 보안 (TLS) 및 인터넷 프로토콜 보안 (IPsec). Office 365의 암호화에 대 한 구체적인 정보에 대 한 [데이터 암호화 기술 Office 365에](office-365-encryption-in-the-microsoft-cloud-overview.md)을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="c0a98-p103">Office 365 uses service-side technologies that encrypt customer content at rest and in transit, including BitLocker, per-file encryption, Transport Layer Security (TLS) and Internet Protocol Security (IPsec). For specific details about encryption in Office 365, see [Data Encryption Technologies in Office 365](office-365-encryption-in-the-microsoft-cloud-overview.md).</span></span>

<span data-ttu-id="c0a98-120">함께 위에 나열 된 보호 기능이 위협 보호 및 완화 방법 만으로는 물리적으로 격리 하 여 제공 하는 것에 해당 하는 강력한 논리 격리 컨트롤을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="c0a98-120">Together, the above-listed protections provide robust logical isolation controls that provide threat protection and mitigation equivalent to that provided by physical isolation alone.</span></span>

## <a name="related-links"></a><span data-ttu-id="c0a98-121">관련된 링크</span><span class="sxs-lookup"><span data-stu-id="c0a98-121">Related Links</span></span>
- [<span data-ttu-id="c0a98-122">Azure Active Directory에서 격리 및 액세스 제어</span><span class="sxs-lookup"><span data-stu-id="c0a98-122">Isolation and Access Control in Azure Active Directory</span></span>](office-365-isolation-in-azure-active-directory.md)
- [<span data-ttu-id="c0a98-123">Office Graph 및 Delve에서 테넌트 격리</span><span class="sxs-lookup"><span data-stu-id="c0a98-123">Tenant Isolation in the Office Graph and Delve</span></span>](office-365-isolation-in-graph-and-delve.md)
- [<span data-ttu-id="c0a98-124">Office 365 검색에서 테넌트 격리</span><span class="sxs-lookup"><span data-stu-id="c0a98-124">Tenant Isolation in Office 365 Search</span></span>](office-365-isolation-in-office-365-search.md)
- [<span data-ttu-id="c0a98-125">Office 365 비디오에서 테넌트 격리</span><span class="sxs-lookup"><span data-stu-id="c0a98-125">Tenant Isolation in Office 365 Video</span></span>](office-365-isolation-in-office-365-video.md)
- [<span data-ttu-id="c0a98-126">리소스 제한 사항</span><span class="sxs-lookup"><span data-stu-id="c0a98-126">Resource Limits</span></span>](office-365-resource-limits.md)
- [<span data-ttu-id="c0a98-127">테넌트 경계 모니터링 및 테스트</span><span class="sxs-lookup"><span data-stu-id="c0a98-127">Monitoring and Testing Tenant Boundaries</span></span>](office-365-monitoring-and-testing.md)
- [<span data-ttu-id="c0a98-128">Office 365에서 격리 및 액세스 제어</span><span class="sxs-lookup"><span data-stu-id="c0a98-128">Isolation and Access Control in Office 365</span></span>](office-365-isolation-in-office-365.md)