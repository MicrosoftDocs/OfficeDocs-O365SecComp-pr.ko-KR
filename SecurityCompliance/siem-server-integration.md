---
title: Microsoft 365과의 SIEM 서버 통합
ms.author: deniseb
author: denisebmsft
manager: laurawi
audience: ITPro
ms.topic: article
ms.date: 10/29/2018
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- M365-security-compliance
ms.custom:
- Ent_Solutions
- SIEM
description: 요약:이 문서를 읽으면 Microsoft 365과의 SIEM server 통합에 대 한 개요를 확인할 수 있습니다.
ms.openlocfilehash: f1911aabaccb7a6c2a56bbd5ff37e396730db72a
ms.sourcegitcommit: 0d5a863f48914eeaaf29f7d2a2022618de186247
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/15/2019
ms.locfileid: "34077524"
---
# <a name="siem-server-integration-with-microsoft-365-services-and-applications"></a><span data-ttu-id="b648f-103">Microsoft 365 서비스 및 응용 프로그램과의 SIEM 서버 통합</span><span class="sxs-lookup"><span data-stu-id="b648f-103">SIEM server integration with Microsoft 365 services and applications</span></span>

## <a name="overview"></a><span data-ttu-id="b648f-104">개요</span><span class="sxs-lookup"><span data-stu-id="b648f-104">Overview</span></span>

<span data-ttu-id="b648f-105">조직에서 SIEM (보안 정보 및 이벤트 관리) 서버를 사용 하는 경우 또는 SIEM 서버를 곧 가져올 계획인 경우 Office 365 Enterprise를 포함 하 여 Microsoft 365와 통합 되는 방법을 궁금할 것입니다.</span><span class="sxs-lookup"><span data-stu-id="b648f-105">If your organization is using a Security Information and Event Management (SIEM) server, or if you are planning to get a SIEM server soon, you might be wondering how that'll integrate with your Microsoft 365, including Office 365 Enterprise.</span></span> <span data-ttu-id="b648f-106">SIEM 서버가 필요한 지 여부는 조직의 보안 요구 사항 등의 많은 요인에 따라 달라 집니다.</span><span class="sxs-lookup"><span data-stu-id="b648f-106">Whether you need a SIEM server depends on many factors, such as your organization's security requirements.</span></span> <span data-ttu-id="b648f-107">Microsoft 365에서는 다양 한 보안 기능을 제공 합니다. 그러나 조직에서 온-프레미스와 클라우드에서 콘텐츠 및 응용 프로그램이 있는 경우 (하이브리드 클라우드 배포의 경우), 추가 보호를 위해 SIEM 서버를 추가 하는 것을 고려할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b648f-107">Microsoft 365 offers a variety of security features; however, if your organization has content and applications on premises and in the cloud (as in the case of a hybrid cloud deployment), you might consider adding a SIEM server for extra protection.</span></span> <span data-ttu-id="b648f-108">또는 조직이 특히 엄격한 보안 요구 사항을 충족 하는 경우에는 환경에 SIEM server를 추가 하는 것을 고려할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b648f-108">Or, if your organization has particularly stringent security requirements you must meet, you might consider adding a SIEM server to your environment.</span></span>

## <a name="siem-server-integration-microsoft-365"></a><span data-ttu-id="b648f-109">SIEM 서버 통합 Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="b648f-109">SIEM server integration Microsoft 365</span></span>

<span data-ttu-id="b648f-110">SIEM 서버는 다양 한 Microsoft 365 서비스 및 응용 프로그램에서 데이터를 받을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b648f-110">A SIEM server can receive data from a wide variety of Microsoft 365 services and applications.</span></span> <span data-ttu-id="b648f-111">다음 표에는 몇 가지 Microsoft 365 서비스와 응용 프로그램과 SIEM server의 입력과 함께, SIEM 서버 통합에 대해 자세히 알아볼 수 있는 위치가 나와 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b648f-111">The following table lists several Microsoft 365 services and applications along with SIEM server inputs and where to go to learn more about SIEM server integration.</span></span> 

| <span data-ttu-id="b648f-112">Microsoft 365 서비스 또는 응용 프로그램</span><span class="sxs-lookup"><span data-stu-id="b648f-112">Microsoft 365 Service or Application</span></span> | <span data-ttu-id="b648f-113">SIEM 서버 입력</span><span class="sxs-lookup"><span data-stu-id="b648f-113">SIEM server inputs</span></span> | <span data-ttu-id="b648f-114">자세한 정보를 볼 수 있는 리소스</span><span class="sxs-lookup"><span data-stu-id="b648f-114">Resources to learn more</span></span> |
| --- | --- | --- |
| [<span data-ttu-id="b648f-115">Office 365 Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="b648f-115">Office 365 Advanced Threat Protection</span></span>](office-365-atp.md) <br/>   <span data-ttu-id="b648f-116">또는</span><span class="sxs-lookup"><span data-stu-id="b648f-116">or</span></span>   <br/>[<span data-ttu-id="b648f-117">Office 365 Threat Intelligence</span><span class="sxs-lookup"><span data-stu-id="b648f-117">Office 365 Threat Intelligence</span></span>](office-365-ti.md) | <span data-ttu-id="b648f-118">감사 로그</span><span class="sxs-lookup"><span data-stu-id="b648f-118">Audit logs</span></span> | [<span data-ttu-id="b648f-119">SIEM과 Office 365 Advanced Threat Protection의 통합</span><span class="sxs-lookup"><span data-stu-id="b648f-119">SIEM integration with Office 365 Advanced Threat Protection</span></span>](siem-integration-with-office-365-ti.md) |
| [<span data-ttu-id="b648f-120">Microsoft Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="b648f-120">Microsoft Cloud App Security</span></span>](https://docs.microsoft.com/cloud-app-security/what-is-cloud-app-security) | <span data-ttu-id="b648f-121">로그 통합</span><span class="sxs-lookup"><span data-stu-id="b648f-121">Log integration</span></span> | [<span data-ttu-id="b648f-122">Microsoft Cloud App Security와의 SIEM 통합</span><span class="sxs-lookup"><span data-stu-id="b648f-122">SIEM integration with Microsoft Cloud App Security</span></span>](https://docs.microsoft.com/cloud-app-security/siem) |
| [<span data-ttu-id="b648f-123">Office 365 Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="b648f-123">Office 365 Cloud App Security</span></span>](https://docs.microsoft.com/cloud-app-security/what-is-cloud-app-security) | <span data-ttu-id="b648f-124">로그 통합</span><span class="sxs-lookup"><span data-stu-id="b648f-124">Log integration</span></span> | [<span data-ttu-id="b648f-125">SIEM server를 Cloud App Security와 통합</span><span class="sxs-lookup"><span data-stu-id="b648f-125">Integrate your SIEM server with Cloud App Security</span></span>](https://docs.microsoft.com/cloud-app-security/siem) |
| [<span data-ttu-id="b648f-126">Windows Defender Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="b648f-126">Windows Defender Advanced Threat Protection</span></span>](https://docs.microsoft.com/windows/security/threat-protection/) | <span data-ttu-id="b648f-127">로그 통합</span><span class="sxs-lookup"><span data-stu-id="b648f-127">Log integration</span></span> | [<span data-ttu-id="b648f-128">SIEM 도구에 대 한 알림 가져오기</span><span class="sxs-lookup"><span data-stu-id="b648f-128">Pull alerts to your SIEM tools</span></span>](https://docs.microsoft.com/windows/security/threat-protection/windows-defender-atp/configure-siem-windows-defender-advanced-threat-protection) |
| <span data-ttu-id="b648f-129">[Azure 보안 센터](https://docs.microsoft.com/azure/security-center/security-center-intro) (위협 방지 및 위협 검색)</span><span class="sxs-lookup"><span data-stu-id="b648f-129">[Azure Security Center](https://docs.microsoft.com/azure/security-center/security-center-intro) (Threat Protection and Threat Detection)</span></span> | <span data-ttu-id="b648f-130">경고</span><span class="sxs-lookup"><span data-stu-id="b648f-130">Alerts</span></span> | [<span data-ttu-id="b648f-131">Azure 보안 데이터를 SIEM 파이프라인 구성으로 내보내기-미리 보기</span><span class="sxs-lookup"><span data-stu-id="b648f-131">Azure Security data export to SIEM - Pipeline Configuration - Preview</span></span>](https://docs.microsoft.com/azure/security-center/security-center-export-data-to-siem) |
| [<span data-ttu-id="b648f-132">Azure Active Directory Id 보호</span><span class="sxs-lookup"><span data-stu-id="b648f-132">Azure Active Directory Identity Protection</span></span>](https://docs.microsoft.com/azure/active-directory/identity-protection/overview) | <span data-ttu-id="b648f-133">감사 로그</span><span class="sxs-lookup"><span data-stu-id="b648f-133">Audit logs</span></span> | [<span data-ttu-id="b648f-134">Azure Active Directory 감사 로그 통합</span><span class="sxs-lookup"><span data-stu-id="b648f-134">Integrate Azure Active Directory audit logs</span></span>](https://docs.microsoft.com/azure/security/security-azure-log-integration-ad) |
| [<span data-ttu-id="b648f-135">Azure Advanced Threat Analytics</span><span class="sxs-lookup"><span data-stu-id="b648f-135">Azure Advanced Threat Analytics</span></span>](https://docs.microsoft.com/azure/security/azure-threat-detection) | <span data-ttu-id="b648f-136">로그 통합</span><span class="sxs-lookup"><span data-stu-id="b648f-136">Log integration</span></span> | [<span data-ttu-id="b648f-137">ATA SIEM 로그 참조</span><span class="sxs-lookup"><span data-stu-id="b648f-137">ATA SIEM log reference</span></span>](https://docs.microsoft.com/advanced-threat-analytics/cef-format-sa) |

## <a name="audit-logging-must-be-turned-on"></a><span data-ttu-id="b648f-138">감사 로깅을 설정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b648f-138">Audit logging must be turned on</span></span>

<span data-ttu-id="b648f-139">SIEM 서버 통합을 구성 하기 전에 감사 로깅이 설정 되어 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="b648f-139">Make sure audit logging is turned on before you configure SIEM server integration.</span></span> 

- <span data-ttu-id="b648f-140">SharePoint Online, 비즈니스용 OneDrive 및 Azure Active Directory의 경우 [보안 _AMP_ 준수 센터에서 감사 로깅이 설정 됩니다](https://docs.microsoft.com/office365/securitycompliance/turn-audit-log-search-on-or-off).</span><span class="sxs-lookup"><span data-stu-id="b648f-140">For SharePoint Online, OneDrive for Business, and Azure Active Directory, [audit logging is turned on in the Security & Compliance Center](https://docs.microsoft.com/office365/securitycompliance/turn-audit-log-search-on-or-off).</span></span>

- <span data-ttu-id="b648f-141">Exchange Online의 경우 [감사 로깅은 Windows PowerShell을 사용 하 여 설정 됩니다](https://docs.microsoft.com/office365/securitycompliance/enable-mailbox-auditing).</span><span class="sxs-lookup"><span data-stu-id="b648f-141">For Exchange Online, [audit logging is turned on with Windows PowerShell](https://docs.microsoft.com/office365/securitycompliance/enable-mailbox-auditing).</span></span>
 
## <a name="see-also"></a><span data-ttu-id="b648f-142">참고 항목</span><span class="sxs-lookup"><span data-stu-id="b648f-142">See Also</span></span>

[<span data-ttu-id="b648f-143">클라우드 채택 및 하이브리드 솔루션</span><span class="sxs-lookup"><span data-stu-id="b648f-143">Cloud adoption and hybrid solutions</span></span>](https://docs.microsoft.com/office365/enterprise/cloud-adoption-and-hybrid-solutions)
  
[<span data-ttu-id="b648f-144">클라우드 도입 TLG(테스트 랩 가이드)</span><span class="sxs-lookup"><span data-stu-id="b648f-144">Cloud adoption Test Lab Guides (TLGs)</span></span>](https://docs.microsoft.com/office365/enterprise/cloud-adoption-test-lab-guides-tlgs)


