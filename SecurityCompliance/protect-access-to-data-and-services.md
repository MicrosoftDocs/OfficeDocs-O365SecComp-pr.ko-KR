---
title: Office 365에서 데이터 및 서비스에 대한 액세스 보호
ms.author: chrfox
author: chrfox
manager: laurawi
ms.date: 4/17/2018
ms.audience: Admin
ms.topic: hub-page
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: a6ef28a4-2447-4b43-aae2-f5af6d53c68e
description: O365 데이터 및 서비스에 대 한 액세스를 보호 하기 위해 페이지를 방문 합니다.
ms.openlocfilehash: e6e2d8d3ba6482d4b80593bd9e09d49d6120af80
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22533758"
---
# <a name="protect-access-to-data-and-services-in-office-365"></a><span data-ttu-id="858e4-103">Office 365에서 데이터 및 서비스에 대한 액세스 보호</span><span class="sxs-lookup"><span data-stu-id="858e4-103">Protect access to data and services in Office 365</span></span>

<span data-ttu-id="858e4-p101">Office 365 데이터 및 서비스에 대 한 액세스를 보호 하는 것은 인터넷 공격을 방어 하 고 데이터 손실을 예방 중요 합니다. 환경의 다른 SaaS 응용 프로그램에 동일한 보호를 적용할 수 및 Azure Active Directory 응용 프로그램 프록시를 사용 하 여 온-프레미스 응용 프로그램에도 게시 합니다.</span><span class="sxs-lookup"><span data-stu-id="858e4-p101">Protecting access to your Office 365 data and services is crucial to defending against cyber-attacks and guarding against data loss. The same protections can be applied to other SaaS applications in your environment and even to on-premises applications published with Azure Active Directory Application Proxy.</span></span>
  
## <a name="step-1-review-recommendations"></a><span data-ttu-id="858e4-106">1 단계: 검토 권장 사항</span><span class="sxs-lookup"><span data-stu-id="858e4-106">Step 1: Review recommendations</span></span>

<span data-ttu-id="858e4-107">Azure AD 응용프로그램 프록시를 사용하여 게시한 온-프레미스 응용 프로그램, Office 365 및 다른 SaaS 서비스에 액세스하는 ID 및 장치를 보호하기 위해 권장되는 기능입니다.</span><span class="sxs-lookup"><span data-stu-id="858e4-107">Recommended capabilities for protecting identities and devices that access Office 365, other SaaS services, and on-premises applications published with Azure AD Application Proxy.</span></span>
  
<span data-ttu-id="858e4-108">[PDF](https://go.microsoft.com/fwlink/p/?linkid=841656) | [Visio](https://go.microsoft.com/fwlink/p/?linkid=841657) | [더 많은 언어](https://www.microsoft.com/download/details.aspx?id=55032)</span><span class="sxs-lookup"><span data-stu-id="858e4-108">[PDF](https://go.microsoft.com/fwlink/p/?linkid=841656) | [Visio](https://go.microsoft.com/fwlink/p/?linkid=841657) | [More languages](https://www.microsoft.com/download/details.aspx?id=55032)</span></span>
  
## <a name="step-2-configure-mfa"></a><span data-ttu-id="858e4-109">2 단계: MFA 구성</span><span class="sxs-lookup"><span data-stu-id="858e4-109">Step 2: Configure MFA</span></span>

<span data-ttu-id="858e4-110">이러한 리소스를 사용 하 여 MFA를 지정 하는 사용자가 직접 버전은 적합 한, 결정을 하 고 계획 하 고 MFA 사용자의 환경에 배포 합니다.</span><span class="sxs-lookup"><span data-stu-id="858e4-110">Use these resources to orient yourself to MFA, decide which version is right for you, and then plan and deploy MFA for your environment.</span></span>
  
- [<span data-ttu-id="858e4-111">Azure 다단계 인증 이란?</span><span class="sxs-lookup"><span data-stu-id="858e4-111">What is Azure multi-factor authentication?</span></span>](https://docs.microsoft.com/azure/multi-factor-authentication/multi-factor-authentication)
    
- [<span data-ttu-id="858e4-112">Azure 다단계 인증 솔루션 선택</span><span class="sxs-lookup"><span data-stu-id="858e4-112">Choose the Azure multi-factor authentication solution for you</span></span>](https://docs.microsoft.com/azure/multi-factor-authentication/multi-factor-authentication-get-started)
    
- [<span data-ttu-id="858e4-113">Azure 다단계 인증을 얻는 방법</span><span class="sxs-lookup"><span data-stu-id="858e4-113">How to get Azure multi-factor authentication</span></span>](https://docs.microsoft.com/azure/multi-factor-authentication/multi-factor-authentication-versions-plans)
    
- [<span data-ttu-id="858e4-114">Office 365 배포에 대 한 다중 요소 인증에 대 한 계획</span><span class="sxs-lookup"><span data-stu-id="858e4-114">Plan for multi-factor authentication for Office 365 deployments</span></span>](https://support.office.com/article/043807b2-21db-4d5c-b430-c8a6dee0e6ba)
    
- [<span data-ttu-id="858e4-115">Office 365 사용자에 게 다단계 인증 설정</span><span class="sxs-lookup"><span data-stu-id="858e4-115">Set up multi-factor authentication for Office 365 users</span></span>](https://support.office.com/article/8f0454b2-f51a-4d9c-bcde-2c48e41621c6)
    
- [<span data-ttu-id="858e4-116">MFA, 클라우드 또는 온-프레미스 배포 위치 계획</span><span class="sxs-lookup"><span data-stu-id="858e4-116">Plan where to deploy MFA, Cloud or on-premises</span></span>](https://docs.microsoft.com/azure/multi-factor-authentication/multi-factor-authentication-get-started)
    
- [<span data-ttu-id="858e4-117">Azure 다단계 인증 설정 구성</span><span class="sxs-lookup"><span data-stu-id="858e4-117">Configure Azure multi-factor authentication settings</span></span>](https://docs.microsoft.com/azure/multi-factor-authentication/multi-factor-authentication-whats-next)
    
## <a name="step-3-enforce-mfa-with-azure-ad-conditional-access-rules"></a><span data-ttu-id="858e4-118">3 단계: Azure AD 조건부 액세스 규칙으로 MFA 적용</span><span class="sxs-lookup"><span data-stu-id="858e4-118">Step 3: Enforce MFA with Azure AD conditional access rules</span></span>

<span data-ttu-id="858e4-119">Azure AD MFA를 사용 하는 경우 Office 365 및 환경에서 다른 SaaS 응용 프로그램에 대 한 액세스에 대 한 MFA를 요청 하는 조건부 액세스 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="858e4-119">If you are using Azure AD MFA, create a conditional access rule to require MFA for access to Office 365 and other SaaS apps in your environment.</span></span>
  
- [<span data-ttu-id="858e4-120">Azure Active Directory에 대 한 조건부 액세스</span><span class="sxs-lookup"><span data-stu-id="858e4-120">Conditional access in Azure Active Directory</span></span>](https://docs.microsoft.com/azure/active-directory/active-directory-conditional-access-azure-portal)
    
## <a name="step-4-configure-sharepoint-device-access-policies"></a><span data-ttu-id="858e4-121">4 단계: SharePoint 장치 액세스 정책 구성</span><span class="sxs-lookup"><span data-stu-id="858e4-121">Step 4: Configure SharePoint device access policies</span></span>

<span data-ttu-id="858e4-p102">중요 한, 분류, 및 규제 데이터를 보호 하는 것에 대 한 SharePoint Online 및 비즈니스용 OneDrive에 대 한 장치 액세스 정책을 사용 하는 것이 좋습니다. 장치 액세스 정책을 개별 팀 사이트에 적용할 수 있는 기능을는 곧 제공 될 예정입니다.</span><span class="sxs-lookup"><span data-stu-id="858e4-p102">Device access policies for SharePoint Online and OneDrive for Business are recommended for protecting sensitive, classified, and regulated data. Coming soon is the ability to apply device access policies to individual team sites.</span></span>
  
- [<span data-ttu-id="858e4-124">관리되지 않는 장치에서 액세스 제어</span><span class="sxs-lookup"><span data-stu-id="858e4-124">Control access from unmanaged devices</span></span>](https://support.office.com/article/Control-access-from-unmanaged-devices-5ae550c4-bd20-4257-847b-5c20fb053622?ui=en-US&amp;rs=en-US&amp;ad=US)
    
## <a name="step-5-configure-app-and-data-protection-for-devices"></a><span data-ttu-id="858e4-125">5 단계: 장치에 대 한 응용 프로그램 및 데이터 보호를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="858e4-125">Step 5: Configure app and data protection for devices</span></span>

<span data-ttu-id="858e4-p103">모바일 장치 관리에 대 한 장치는 등록 되었는지 여부에 관계 없이 모바일 장치에서 응용 프로그램을 관리할 수 있습니다. 이 실수로 유출 메일 및 파일을 포함 하 여 Office 365의 데이터를 보호 합니다.</span><span class="sxs-lookup"><span data-stu-id="858e4-p103">You can manage applications on mobile devices regardless of whether the devices are enrolled for mobile device management. This protects against accidental leakage of data in Office 365, including mail and files.</span></span>
  
- <span data-ttu-id="858e4-128">IOS 및 Android: [Microsoft Intune를 사용한 응용 프로그램 보호 정책을 사용 하 여 응용 프로그램 데이터를 보호](https://docs.microsoft.com/intune-classic/deploy-use/protect-app-data-using-mobile-app-management-policies-with-microsoft-intune)</span><span class="sxs-lookup"><span data-stu-id="858e4-128">For iOS and Android: [Protect app data using app protection policies with Microsoft Intune](https://docs.microsoft.com/intune-classic/deploy-use/protect-app-data-using-mobile-app-management-policies-with-microsoft-intune)</span></span>
    
<span data-ttu-id="858e4-129">Windows 10에 대 한 Windows 정보 보호 (진행 중) 실수로 데이터 누출 방지 하기 위해를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="858e4-129">For Windows 10, configure Windows Information Protection (WIP) to prevent accidental data leaks.</span></span>
  
- <span data-ttu-id="858e4-130">관리 되는 장치에 대 한: [Microsoft Intune를 위한 Azure 포털을 사용 하 여 등록 정책 사용 하 여 Windows 정보 보호 (WIP) 만들기](https://docs.microsoft.com/windows/threat-protection/windows-information-protection/create-wip-policy-using-intune-azure)</span><span class="sxs-lookup"><span data-stu-id="858e4-130">For managed devices: [Create a Windows Information Protection (WIP) with enrollment policy using the Azure portal for Microsoft Intune](https://docs.microsoft.com/windows/threat-protection/windows-information-protection/create-wip-policy-using-intune-azure)</span></span>
    
- <span data-ttu-id="858e4-131">되지 않은 관리 되는 장치에 대 한: [만들기 진행 (Windows 정보 보호 중) 응용 프로그램 보호 정책을 Intune 사용한 배포 및](https://docs.microsoft.com/intune/windows-information-protection-policy-create)</span><span class="sxs-lookup"><span data-stu-id="858e4-131">For un-managed devices: [Create and deploy Windows Information Protection (WIP) app protection policy with Intune](https://docs.microsoft.com/intune/windows-information-protection-policy-create)</span></span>
    
## <a name="step-6-manage-devices-with-intune"></a><span data-ttu-id="858e4-132">6 단계: Intune 사용 하 여 장치를 관리 합니다.</span><span class="sxs-lookup"><span data-stu-id="858e4-132">Step 6: Manage devices with Intune</span></span>

<span data-ttu-id="858e4-p104">장치 관리를 사용 하면 사용자 환경에서 리소스에 대 한 액세스를 허용 하기 전에 정상 상태이 고 호환 되는지 확인 합니다. 장치 기반 규칙을 보장 공격자가 액세스할 수 없으므로 자원에 비관리 장치에서 조건부 액세스 합니다.</span><span class="sxs-lookup"><span data-stu-id="858e4-p104">Managing devices allows you to ensure that they are healthy and compliant before allowing them access to resources in your environment. Device based conditional access rules help ensure attackers can't gain access to your resources from unmanaged devices.</span></span>
  
- [<span data-ttu-id="858e4-135">Intune의 관리 기능에 대 한 장치를 등록 합니다.</span><span class="sxs-lookup"><span data-stu-id="858e4-135">Enroll devices for management in Intune</span></span>](https://docs.microsoft.com/intune-classic/deploy-use/enroll-devices-in-microsoft-intune)
    
## <a name="step-7-configure-additional-intune-policies-and-conditional-access-rules-for-your-environment"></a><span data-ttu-id="858e4-136">7 단계: 추가 Intune 정책 및 사용자 환경에 대 한 조건부 액세스 규칙 구성</span><span class="sxs-lookup"><span data-stu-id="858e4-136">Step 7: Configure additional Intune policies and conditional access rules for your environment</span></span>

<span data-ttu-id="858e4-137">엔터프라이즈 규모 또는 복잡 한 access 보안 시나리오에 대 한 시작 지점으로 권장 되는 구성에 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="858e4-137">Use these recommended configurations as a starting point for enterprise scale or sophisticated access security scenarios.</span></span>
  
- [<span data-ttu-id="858e4-138">전자 메일 보안 정책 및 구성</span><span class="sxs-lookup"><span data-stu-id="858e4-138">Secure email policies and configurations</span></span>](https://docs.microsoft.com/azure/active-directory/secure-email-introduction)
    

