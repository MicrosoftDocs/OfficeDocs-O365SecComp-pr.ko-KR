---
title: 사용자 및 장치 액세스 보호
ms.author: bcarter
author: brendacarter
manager: laurawi
ms.date: 4/17/2018
audience: Admin
ms.topic: hub-page
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: a6ef28a4-2447-4b43-aae2-f5af6d53c68e
description: O365 데이터 및 서비스에 대 한 액세스를 보호 하기 위한 랜딩 페이지
ms.openlocfilehash: 9fc1691e7e36f994b5d0b8a6a9735fe8ccd8735a
ms.sourcegitcommit: 4a2bde56178609e75c1ad7ecad2db5e049fc0c45
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/05/2019
ms.locfileid: "36761614"
---
# <a name="protect-user-and-device-access"></a><span data-ttu-id="081bf-103">사용자 및 장치 액세스 보호</span><span class="sxs-lookup"><span data-stu-id="081bf-103">Protect user and device access</span></span>

<span data-ttu-id="081bf-104">Office 365 데이터 및 서비스에 대 한 액세스를 보호 하는 것은 고 사이버 공격을 방어 하 고 데이터 손실 으로부터 보호 하는 데 매우 중요 합니다.</span><span class="sxs-lookup"><span data-stu-id="081bf-104">Protecting access to your Office 365 data and services is crucial to defending against cyberattacks and guarding against data loss.</span></span> <span data-ttu-id="081bf-105">해당 환경의 다른 SaaS 응용 프로그램 및 Azure Active Directory 응용 프로그램 프록시를 사용 하 여 게시 된 온-프레미스 응용 프로그램에도 동일한 보호를 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="081bf-105">The same protections can be applied to other SaaS applications in your environment and even to on-premises applications published with Azure Active Directory Application Proxy.</span></span>
  
## <a name="step-1-review-recommendations"></a><span data-ttu-id="081bf-106">1 단계: 권장 사항 검토</span><span class="sxs-lookup"><span data-stu-id="081bf-106">Step 1: Review recommendations</span></span>

<span data-ttu-id="081bf-107">Azure AD 애플리케이션 프록시를 사용하여 게시한 온-프레미스 응용 프로그램, Office 365 및 다른 SaaS 서비스에 액세스하는 ID 및 디바이스를 보호하기 위해 권장되는 기능입니다.</span><span class="sxs-lookup"><span data-stu-id="081bf-107">Recommended capabilities for protecting identities and devices that access Office 365, other SaaS services, and on-premises applications published with Azure AD Application Proxy.</span></span>
  
<span data-ttu-id="081bf-108">[PDF](https://go.microsoft.com/fwlink/p/?linkid=841656) | [Visio](https://go.microsoft.com/fwlink/p/?linkid=841657) | [더 많은 언어](https://www.microsoft.com/download/details.aspx?id=55032)</span><span class="sxs-lookup"><span data-stu-id="081bf-108">[PDF](https://go.microsoft.com/fwlink/p/?linkid=841656) | [Visio](https://go.microsoft.com/fwlink/p/?linkid=841657) | [More languages](https://www.microsoft.com/download/details.aspx?id=55032)</span></span>
  
## <a name="step-2-protect-administrator-accounts-and-access"></a><span data-ttu-id="081bf-109">2 단계: 관리자 계정 보호 및 액세스</span><span class="sxs-lookup"><span data-stu-id="081bf-109">Step 2: Protect administrator accounts and access</span></span>
<span data-ttu-id="081bf-110">Office 365 환경을 관리 하는 데 사용 하는 관리 계정에 상승 된 권한이 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="081bf-110">The administrative accounts you use to administer your Office 365 environment include elevated privileges.</span></span> <span data-ttu-id="081bf-111">다음은 해커 및 cyberattackers에 대 한 귀중 한 목표입니다.</span><span class="sxs-lookup"><span data-stu-id="081bf-111">These are valuable targets for hackers and cyberattackers.</span></span> 

<span data-ttu-id="081bf-112">먼저 관리용 관리자 계정만 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="081bf-112">Begin by using administrator accounts only for administration.</span></span> <span data-ttu-id="081bf-113">관리자에 게는 관리 작업과 관련 된 일반 사용을 위한 별도의 사용자 계정이 있어야 하며, 해당 작업 기능과 연결 되는 작업을 완료 하는 데 필요한 경우에만 해당 관리자 계정을 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="081bf-113">Admins should have a separate user account for regular, non-administrative use and only use their administrative account when necessary to complete a task associated with their job function.</span></span>

<span data-ttu-id="081bf-114">Multi-factor authentication 및 조건부 액세스를 사용 하 여 관리자 계정을 보호 합니다.</span><span class="sxs-lookup"><span data-stu-id="081bf-114">Protect your administrator accounts with multi-factor authentication and conditional access.</span></span> <span data-ttu-id="081bf-115">자세한 내용은 [관리자 계정 보호](https://docs.microsoft.com/microsoft-365/enterprise/identity-access-prerequisites#protecting-administrator-accounts)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="081bf-115">For more information, see [Protecting administrator accounts](https://docs.microsoft.com/microsoft-365/enterprise/identity-access-prerequisites#protecting-administrator-accounts).</span></span> 

<span data-ttu-id="081bf-116">다음으로, Office 365에서 권한이 부여 된 액세스 관리를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="081bf-116">Next, configure privileged access management in Office 365.</span></span> <span data-ttu-id="081bf-117">권한이 부여 된 액세스 관리를 통해 Office 365의 권한 있는 관리 작업을 세부적으로 제어할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="081bf-117">Privileged access management allows granular access control over privileged admin tasks in Office 365.</span></span> <span data-ttu-id="081bf-118">중요 한 데이터에 대 한 액세스 권한이 나 중요 한 구성 설정에 대 한 액세스 권한이 있는 기존 권한 관리 계정을 사용 하는 보안 침해 로부터 조직을 보호 하는 데 도움이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="081bf-118">It can help protect your organization from breaches that may use existing privileged admin accounts with standing access to sensitive data or access to critical configuration settings.</span></span>

- [<span data-ttu-id="081bf-119">권한 있는 액세스 관리 개요</span><span class="sxs-lookup"><span data-stu-id="081bf-119">Overview of privileged access management</span></span>](privileged-access-management-overview.md)
- [<span data-ttu-id="081bf-120">권한이 부여된 액세스 관리 구성</span><span class="sxs-lookup"><span data-stu-id="081bf-120">Configure privileged access management</span></span>](privileged-access-management-configuration.md)

<span data-ttu-id="081bf-121">또 다른 주요 권장 사항은 관리 작업을 위해 특별히 구성 된 워크스테이션을 사용 하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="081bf-121">Another top recommendation is to use workstations specifically configured for administrative work.</span></span> <span data-ttu-id="081bf-122">관리 작업에만 사용 되는 전용 장치입니다.</span><span class="sxs-lookup"><span data-stu-id="081bf-122">These are dedicated devices that are only used for administrative tasks.</span></span> <span data-ttu-id="081bf-123">[권한 있는 액세스 보호](https://docs.microsoft.com/windows-server/identity/securing-privileged-access/securing-privileged-access)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="081bf-123">See [Securing privileged access](https://docs.microsoft.com/windows-server/identity/securing-privileged-access/securing-privileged-access).</span></span>

<span data-ttu-id="081bf-124">마지막으로, 테 넌 트에서 두 개 이상의 응급 액세스 계정을 만들어 실수로 관리 액세스가 부족 하다는 영향을 완화할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="081bf-124">Finally, you can mitigate the impact of inadvertent lack of administrative access by creating two or more emergency access accounts in your tenant.</span></span> <span data-ttu-id="081bf-125">[AZURE AD에서 긴급 액세스 계정 관리를](https://docs.microsoft.com/azure/active-directory/users-groups-roles/directory-emergency-access)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="081bf-125">See [Manage emergency access accounts in Azure AD](https://docs.microsoft.com/azure/active-directory/users-groups-roles/directory-emergency-access).</span></span> 

## <a name="step-3-configure-recommended-identity-and-device-access-policies"></a><span data-ttu-id="081bf-126">3 단계: 권장 되는 id 및 장치 액세스 정책 구성</span><span class="sxs-lookup"><span data-stu-id="081bf-126">Step 3: Configure recommended identity and device access policies</span></span>
<span data-ttu-id="081bf-127">MFA (multi-factor authentication) 및 조건부 액세스 정책은 손상 된 계정 및 무단 액세스를 완화 하기 위한 강력한 도구입니다.</span><span class="sxs-lookup"><span data-stu-id="081bf-127">Multi-factor authentication (MFA) and conditional access policies are powerful tools for mitigating against compromised accounts and unauthorized access.</span></span> <span data-ttu-id="081bf-128">함께 테스트 된 정책 집합을 구현 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="081bf-128">We recommend implementing a set of policies that have been tested together.</span></span> <span data-ttu-id="081bf-129">배포 단계를 비롯 한 자세한 내용은 [id 및 장치 액세스 구성](https://docs.microsoft.com/microsoft-365/enterprise/microsoft-365-policies-configurations)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="081bf-129">For more information, including deployment steps, see [Identity and device access configurations](https://docs.microsoft.com/microsoft-365/enterprise/microsoft-365-policies-configurations).</span></span>

 <span data-ttu-id="081bf-130">이러한 정책은 다음과 같은 기능을 구현 합니다.</span><span class="sxs-lookup"><span data-stu-id="081bf-130">These policies implement the following capabilities:</span></span>
- <span data-ttu-id="081bf-131">여러 요소 인증</span><span class="sxs-lookup"><span data-stu-id="081bf-131">Mult-factor authentication</span></span>
- <span data-ttu-id="081bf-132">조건부 액세스</span><span class="sxs-lookup"><span data-stu-id="081bf-132">Conditional access</span></span>
- <span data-ttu-id="081bf-133">Intune 앱 보호 (장치용 앱 및 데이터 보호)</span><span class="sxs-lookup"><span data-stu-id="081bf-133">Intune app protection (app and data protection for devices)</span></span>
- <span data-ttu-id="081bf-134">Intune 장치 준수</span><span class="sxs-lookup"><span data-stu-id="081bf-134">Intune device compliance</span></span>
- <span data-ttu-id="081bf-135">Azure AD ID 보호</span><span class="sxs-lookup"><span data-stu-id="081bf-135">Azure AD Identity Protection</span></span>

<span data-ttu-id="081bf-136">Intune 장치 준수를 구현 하려면 장치 등록이 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="081bf-136">Implementing Intune device compliance requires device enrollment.</span></span> <span data-ttu-id="081bf-137">장치를 관리 하면 해당 환경의 리소스에 대 한 액세스를 허용 하기 전에 정상 및 호환이 가능 하도록 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="081bf-137">Managing devices allows you to ensure that they are healthy and compliant before allowing them access to resources in your environment.</span></span> <span data-ttu-id="081bf-138">[Intune에서 관리용 장치 등록](https://docs.microsoft.com/intune-classic/deploy-use/enroll-devices-in-microsoft-intune) 을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="081bf-138">See [Enroll devices for management in Intune](https://docs.microsoft.com/intune-classic/deploy-use/enroll-devices-in-microsoft-intune)</span></span>

## <a name="step-4-configure-sharepoint-device-access-policies"></a><span data-ttu-id="081bf-139">4 단계: SharePoint 장치 액세스 정책 구성</span><span class="sxs-lookup"><span data-stu-id="081bf-139">Step 4: Configure SharePoint device access policies</span></span>

<span data-ttu-id="081bf-140">Microsoft는 장치 액세스 제어를 통해 중요 하 고 규제 된 콘텐츠를 사용 하 여 SharePoint 사이트의 콘텐츠를 보호 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="081bf-140">Microsoft recommends you protect content in SharePoint sites with sensitive and highly-regulated content with device access controls.</span></span> <span data-ttu-id="081bf-141">자세한 내용은 [SharePoint 사이트 및 파일을 보호 하기 위한 정책 권장 사항을](https://docs.microsoft.com/microsoft-365/enterprise/sharepoint-file-access-policies)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="081bf-141">For more information, see [Policy recommendations for securing SharePoint sites and files](https://docs.microsoft.com/microsoft-365/enterprise/sharepoint-file-access-policies).</span></span>



    

