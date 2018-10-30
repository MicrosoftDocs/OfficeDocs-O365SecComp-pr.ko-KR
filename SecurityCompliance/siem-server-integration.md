---
title: Microsoft 365 SIEM 서버 통합
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.audience: ITPro
ms.topic: article
ms.date: 10/29/2018
ms.service: o365-solutions
localization_priority: Normal
ms.collection: Ent_O365
ms.custom:
- Ent_Solutions
- SIEM
description: '요약: Microsoft 365 SIEM 서버 통합을 대략적를이 문서를 읽어봅니다.'
ms.openlocfilehash: bd512ca6d75928712e3444581a78610a0869123d
ms.sourcegitcommit: 63ed467fc3e1ab1ab9ee122df97c64737169834e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/30/2018
ms.locfileid: "25842687"
---
# <a name="siem-server-integration-with-microsoft-365-services-and-applications"></a><span data-ttu-id="d6232-103">Microsoft 365 서비스 및 응용 프로그램의 SIEM 서버 통합</span><span class="sxs-lookup"><span data-stu-id="d6232-103">SIEM server integration with Microsoft 365 services and applications</span></span>

## <a name="overview"></a><span data-ttu-id="d6232-104">개요</span><span class="sxs-lookup"><span data-stu-id="d6232-104">Overview</span></span>

<span data-ttu-id="d6232-p101">조직에는 보안 정보 및 이벤트 관리 (SIEM) 서버를 사용 하는 서버를 파악 한 SIEM 곧를 계획 하는 경우 하는지에 대해 어떻게 Office 365 Enterprise를 포함 하 여 Microsoft 365, 통합 하는 경우. SIEM 서버의 필요 여부는 조직의 보안 요구 사항 등의 여러 요인에 따라 달라 집니다. Microsoft 365 다양 한 보안 기능입니다. 그러나 온-프레미스 및 클라우드 (예: 하이브리드 클라우드 배포의 경우)에서 조직에 콘텐츠 및 응용 프로그램을 하는 경우 추가 보호에 대 한 SIEM 서버 추가 (영문) 고려 될 수 있습니다. 또는 조직에 특히 엄격한 보안 요구 사항을 충족 해야, 경우 환경에 추가 하는 SIEM 서버를 고려할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d6232-p101">If your organization is using a Security Information and Event Management (SIEM) server, or if you are planning to get a SIEM server soon, you might be wondering how that'll integrate with your Microsoft 365, including Office 365 Enterprise. Whether you need a SIEM server depends on many factors, such as your organization's security requirements. Microsoft 365 offers a variety of security features; however, if your organization has content and applications on premises and in the cloud (as in the case of a hybrid cloud deployment), you might consider adding a SIEM server for extra protection. Or, if your organization has particularly stringent security requirements you must meet, you might consider adding a SIEM server to your environment.</span></span>

## <a name="siem-server-integration-microsoft-365"></a><span data-ttu-id="d6232-109">Microsoft 365 SIEM 서버 통합</span><span class="sxs-lookup"><span data-stu-id="d6232-109">SIEM server integration Microsoft 365</span></span>

<span data-ttu-id="d6232-p102">SIEM 서버는 다양 한 Microsoft 365 서비스 및 응용 프로그램에서에서 데이터를 받을 수 있습니다. 다음 표에서 여러 Microsoft 365 서비스 및 응용 프로그램 SIEM 서버 입력 및 SIEM 서버 통합 하는 방법에 대 한 자세한 내용은 이동할 위치를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6232-p102">A SIEM server can receive data from a wide variety of Microsoft 365 services and applications. The following table lists several Microsoft 365 services and applications along with SIEM server inputs and where to go to learn more about SIEM server integration.</span></span> 

| <span data-ttu-id="d6232-112">Microsoft 365 서비스 또는 응용 프로그램</span><span class="sxs-lookup"><span data-stu-id="d6232-112">Microsoft 365 Service or Application</span></span> | <span data-ttu-id="d6232-113">SIEM 서버 입력</span><span class="sxs-lookup"><span data-stu-id="d6232-113">SIEM server inputs</span></span> | <span data-ttu-id="d6232-114">자세한 내용은 리소스</span><span class="sxs-lookup"><span data-stu-id="d6232-114">Resources to learn more</span></span> |
| --- | --- | --- |
| [<span data-ttu-id="d6232-115">Office 365 Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="d6232-115">Office 365 Advanced Threat Protection</span></span>](office-365-atp.md) <br/>   <span data-ttu-id="d6232-116">또는</span><span class="sxs-lookup"><span data-stu-id="d6232-116">or</span></span>   <br/>[<span data-ttu-id="d6232-117">Office 365 위협 인텔리전스</span><span class="sxs-lookup"><span data-stu-id="d6232-117">Office 365 Threat Intelligence</span></span>](office-365-ti.md) | <span data-ttu-id="d6232-118">감사 로그</span><span class="sxs-lookup"><span data-stu-id="d6232-118">Audit logs</span></span> | [<span data-ttu-id="d6232-119">Office 365 위협 인텔리전스 및 고급 위협 보호 SIEM 통합</span><span class="sxs-lookup"><span data-stu-id="d6232-119">SIEM integration with Office 365 Threat Intelligence and Advanced Threat Protection</span></span>](siem-integration-with-office-365-ti.md) |
| [<span data-ttu-id="d6232-120">Microsoft Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="d6232-120">Microsoft Cloud App Security</span></span>](https://docs.microsoft.com/cloud-app-security/what-is-cloud-app-security) | <span data-ttu-id="d6232-121">로그의 통합</span><span class="sxs-lookup"><span data-stu-id="d6232-121">Log integration</span></span> | [<span data-ttu-id="d6232-122">Microsoft 클라우드 앱 보안 SIEM 통합</span><span class="sxs-lookup"><span data-stu-id="d6232-122">SIEM integration with Microsoft Cloud App Security</span></span>](https://docs.microsoft.com/cloud-app-security/siem) |
| [<span data-ttu-id="d6232-123">Office 365 Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="d6232-123">Office 365 Cloud App Security</span></span>](office-365-cas-overview.md) | <span data-ttu-id="d6232-124">로그의 통합</span><span class="sxs-lookup"><span data-stu-id="d6232-124">Log integration</span></span> | [<span data-ttu-id="d6232-125">Office 365 Cloud App Security와 SIEM 서버 통합</span><span class="sxs-lookup"><span data-stu-id="d6232-125">Integrate your SIEM server with Office 365 Cloud App Security</span></span>](integrate-your-siem-server-with-office-365-cas.md) |
| [<span data-ttu-id="d6232-126">Windows Defender Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="d6232-126">Windows Defender Advanced Threat Protection</span></span>](https://docs.microsoft.com/windows/security/threat-protection/) | <span data-ttu-id="d6232-127">로그의 통합</span><span class="sxs-lookup"><span data-stu-id="d6232-127">Log integration</span></span> | [<span data-ttu-id="d6232-128">SIEM 도구 끌어오기 알림</span><span class="sxs-lookup"><span data-stu-id="d6232-128">Pull alerts to your SIEM tools</span></span>](https://docs.microsoft.com/windows/security/threat-protection/windows-defender-atp/configure-siem-windows-defender-advanced-threat-protection) |
| <span data-ttu-id="d6232-129">[Azure 보안 센터](https://docs.microsoft.com/azure/security-center/security-center-intro) (위협 보호 및 위협 감지)</span><span class="sxs-lookup"><span data-stu-id="d6232-129">[Azure Security Center](https://docs.microsoft.com/azure/security-center/security-center-intro) (Threat Protection and Threat Detection)</span></span> | <span data-ttu-id="d6232-130">알림</span><span class="sxs-lookup"><span data-stu-id="d6232-130">Alerts</span></span> | [<span data-ttu-id="d6232-131">SIEM-파이프라인 구성-미리 보기를 azure 보안 데이터 내보내기</span><span class="sxs-lookup"><span data-stu-id="d6232-131">Azure Security data export to SIEM - Pipeline Configuration - Preview</span></span>](https://docs.microsoft.com/azure/security-center/security-center-export-data-to-siem) |
| [<span data-ttu-id="d6232-132">Azure Active Directory Id 보호</span><span class="sxs-lookup"><span data-stu-id="d6232-132">Azure Active Directory Identity Protection</span></span>](https://docs.microsoft.com/azure/active-directory/identity-protection/overview) | <span data-ttu-id="d6232-133">감사 로그</span><span class="sxs-lookup"><span data-stu-id="d6232-133">Audit logs</span></span> | [<span data-ttu-id="d6232-134">Azure Active Directory 감사 로그를 통합 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6232-134">Integrate Azure Active Directory audit logs</span></span>](https://docs.microsoft.com/azure/security/security-azure-log-integration-ad) |
| [<span data-ttu-id="d6232-135">Azure 고급 위협 분석</span><span class="sxs-lookup"><span data-stu-id="d6232-135">Azure Advanced Threat Analytics</span></span>](https://docs.microsoft.com/azure/security/azure-threat-detection) | <span data-ttu-id="d6232-136">로그의 통합</span><span class="sxs-lookup"><span data-stu-id="d6232-136">Log integration</span></span> | [<span data-ttu-id="d6232-137">ATA SIEM 로그 참조 (영문)</span><span class="sxs-lookup"><span data-stu-id="d6232-137">ATA SIEM log reference</span></span>](https://docs.microsoft.com/advanced-threat-analytics/cef-format-sa) |

## <a name="audit-logging-must-be-turned-on"></a><span data-ttu-id="d6232-138">감사 로깅을 설정 해야</span><span class="sxs-lookup"><span data-stu-id="d6232-138">Audit logging must be turned on</span></span>

<span data-ttu-id="d6232-139">SIEM 서버 통합을 구성 하기 전에 감사 로깅이 설정 되어있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6232-139">Make sure audit logging is turned on before you configure SIEM server integration.</span></span> 

- <span data-ttu-id="d6232-140">SharePoint online, 비즈니스 및 Azure Active Directory [의 보안 및 규정 준수 센터의 감사 로깅이 설정](https://docs.microsoft.com/office365/securitycompliance/turn-audit-log-search-on-or-off)에 대 한 OneDrive 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6232-140">For SharePoint Online, OneDrive for Business, and Azure Active Directory, [audit logging is turned on in the Security & Compliance Center](https://docs.microsoft.com/office365/securitycompliance/turn-audit-log-search-on-or-off).</span></span>

- <span data-ttu-id="d6232-141">에 대 한 Exchange Online, [Windows PowerShell을 사용한 감사 로깅이 켜져](https://docs.microsoft.com/office365/securitycompliance/enable-mailbox-auditing)있습니다.</span><span class="sxs-lookup"><span data-stu-id="d6232-141">For Exchange Online, [audit logging is turned on with Windows PowerShell](https://docs.microsoft.com/office365/securitycompliance/enable-mailbox-auditing).</span></span>
 
## <a name="see-also"></a><span data-ttu-id="d6232-142">참고 항목</span><span class="sxs-lookup"><span data-stu-id="d6232-142">See Also</span></span>

[<span data-ttu-id="d6232-143">클라우드 채택 및 하이브리드 솔루션</span><span class="sxs-lookup"><span data-stu-id="d6232-143">Cloud adoption and hybrid solutions</span></span>](https://docs.microsoft.com/office365/enterprise/cloud-adoption-and-hybrid-solutions)
  
[<span data-ttu-id="d6232-144">클라우드 도입 TLG(테스트 랩 가이드)</span><span class="sxs-lookup"><span data-stu-id="d6232-144">Cloud adoption Test Lab Guides (TLGs)</span></span>](https://docs.microsoft.com/office365/enterprise/cloud-adoption-test-lab-guides-tlgs)


