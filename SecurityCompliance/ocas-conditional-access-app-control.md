---
title: Office 365 Cloud App Security 조건부 액세스 앱 컨트롤을 사용하여 앱 보호
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.reviewer: alesibov
ms.audience: Admin
ms.topic: reference
ms.date: 02/27/2019
ms.service: O365-seccomp
localization_priority: Normal
description: Office 365 Cloud app Security 조건부 Access 앱 컨트롤을 사용 하 여 실시간으로 위반 및 누출을 중단 합니다.
ms.openlocfilehash: d8370b1e02866db8f92ab7f6a46b06ddc3ed1055
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32262990"
---
# <a name="protect-apps-with-office-365-cloud-app-security-conditional-access-app-control"></a><span data-ttu-id="285c6-103">Office 365 Cloud App Security 조건부 액세스 앱 컨트롤을 사용하여 앱 보호</span><span class="sxs-lookup"><span data-stu-id="285c6-103">Protect apps with Office 365 Cloud App Security Conditional Access App Control</span></span>

|<span data-ttu-id="285c6-104">계산 \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="285c6-104">\*\*\*\*Evaluation\*\* \>\*\*</span></span>|<span data-ttu-id="285c6-105">계획 \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="285c6-105">\*\*\*\*Planning\*\* \>\*\*</span></span>|<span data-ttu-id="285c6-106">배포 \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="285c6-106">\*\*\*\*Deployment\*\* \>\*\*</span></span>|<span data-ttu-id="285c6-107">사용률 \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="285c6-107">\*\*\*\*Utilization\*\*\*\*</span></span>|
|:-----|:-----|:-----|:-----|
|[<span data-ttu-id="285c6-108">평가 시작</span><span class="sxs-lookup"><span data-stu-id="285c6-108">Start evaluating</span></span>](office-365-cas-overview.md) <br/> |[<span data-ttu-id="285c6-109">계획 시작</span><span class="sxs-lookup"><span data-stu-id="285c6-109">Start planning</span></span>](get-ready-for-office-365-cas.md) <br/> |<span data-ttu-id="285c6-110">사용자가 여기 있어!</span><span class="sxs-lookup"><span data-stu-id="285c6-110">You are here!</span></span>  <br/> [<span data-ttu-id="285c6-111">다음 단계</span><span class="sxs-lookup"><span data-stu-id="285c6-111">Next step</span></span>](ocas-deploy-conditional-access-app-control.md) <br/> |[<span data-ttu-id="285c6-112">활용 시작</span><span class="sxs-lookup"><span data-stu-id="285c6-112">Start utilizing</span></span>](utilization-activities-for-ocas.md) <br/> |

<span data-ttu-id="285c6-113">요즘에는 클라우드 환경에서 발생 하는 작업을 파악 하는 데 충분 하지 않은 경우가 많습니다.</span><span class="sxs-lookup"><span data-stu-id="285c6-113">In today’s workplace, it’s often not enough to know what’s happening in your cloud environment after the fact.</span></span> <span data-ttu-id="285c6-114">직원 들이 고의적으로 또는 실수로 데이터와 조직을 위험에 노출 하기 전까지 실시간으로 침해 및 누출을 중단 하려는 경우</span><span class="sxs-lookup"><span data-stu-id="285c6-114">You want to stop breaches and leaks in real time, before employees intentionally or inadvertently put your data and your organization at risk.</span></span> <span data-ttu-id="285c6-115">조직의 사용자가 클라우드 앱에서 사용 가능한 서비스와 도구를 대부분 사용할 수 있도록 설정 하 고 자체 장치를 사용 하도록 허용 하는 것이 중요 합니다.</span><span class="sxs-lookup"><span data-stu-id="285c6-115">It's important to enable users in your organization to make the most of the services and tools available to them in cloud apps, and let them bring their own devices to work.</span></span> <span data-ttu-id="285c6-116">동시에 조직에서 데이터 누출 및 데이터 절도를 실시간으로 보호 하는 데 도움이 되는 도구가 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="285c6-116">At the same time, you need tools to help protect your organization from data leaks, and data theft, in real time.</span></span> <span data-ttu-id="285c6-117">Azure Active Directory와 함께 Office 365 Cloud App Security에서는 조건부 액세스 앱 컨트롤을 사용 하 여 전체적이 고 통합 된 환경에서 이러한 기능을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="285c6-117">Together with Azure Active Directory, Office 365 Cloud App Security delivers these capabilities in a holistic and integrated experience with Conditional Access App Control.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="285c6-118">Cloud app Security 조건부 Access 앱 컨트롤을 사용 하려면 [Azure active Directory P1 라이선스](https://azure.microsoft.com/pricing/details/active-directory/) 및 활성 [Office 365 Cloud App Security](office-365-cas-overview.md) 구독이 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="285c6-118">To use Cloud App Security Conditional Access App Control, you need an [Azure Active Directory P1 license](https://azure.microsoft.com/pricing/details/active-directory/) and an active [Office 365 Cloud App Security](office-365-cas-overview.md) subscription.</span></span>

## <a name="how-it-works"></a><span data-ttu-id="285c6-119">작업 방법</span><span class="sxs-lookup"><span data-stu-id="285c6-119">How it works</span></span>

<span data-ttu-id="285c6-120">조건부 액세스 앱 컨트롤은 역방향 프록시 아키텍처를 사용 하며 Azure AD 조건부 액세스와 고유 하 게 통합 됩니다.</span><span class="sxs-lookup"><span data-stu-id="285c6-120">Conditional Access App Control uses a reverse proxy architecture and is uniquely integrated with Azure AD conditional access.</span></span> <span data-ttu-id="285c6-121">Azure AD 조건부 액세스를 사용 하면 특정 조건에 따라 조직의 앱에 대 한 액세스 제어를 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="285c6-121">Azure AD conditional access allows you to enforce access controls on your organization’s apps based on certain conditions.</span></span> <span data-ttu-id="285c6-122">조건은 사용자 또는 ** 사용자 그룹을 정의 하 고, *어떤* 클라우드 앱 ** 을 지정 하 고, 조건부 액세스 정책을 적용할 위치와 네트워크를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="285c6-122">The conditions define *who* (user or group of users) and *what* (which cloud apps) and *where* (which locations and networks) a conditional access policy is applied to.</span></span> <span data-ttu-id="285c6-123">조건을 확인 한 후 access 및 세션 제어를 적용 하 여 조건부 Access 앱 컨트롤을 사용 하 여 데이터를 보호할 수 있는 Office 365 Cloud App Security로 사용자를 라우팅할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="285c6-123">After you’ve determined the conditions, you can route users to Office 365 Cloud App Security where you can protect data with Conditional Access App Control by applying access and session controls.</span></span>

<span data-ttu-id="285c6-124">조건부 액세스 앱 컨트롤을 사용 하면 access 및 세션 정책에 따라 실시간으로 사용자 앱 액세스와 세션을 모니터링 하 고 제어할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="285c6-124">Conditional Access App Control enables user app access and sessions to be monitored and controlled in real time based on access and session policies.</span></span> <span data-ttu-id="285c6-125">액세스 및 세션 정책은 Cloud App Security 포털에서 사용 되어 필터를 보다 구체화 하 고 사용자에 대해 수행할 작업을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="285c6-125">Access and session policies are used within the Cloud App Security portal to further refine filters and set actions to be taken on a user.</span></span> <span data-ttu-id="285c6-126">액세스 및 세션 정책을 사용 하 여 다음을 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="285c6-126">With the access and session policies, you can:</span></span>

- <span data-ttu-id="285c6-127">**다운로드 차단**: 중요 한 문서의 다운로드를 차단할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="285c6-127">**Block on download**: You can block the download of sensitive documents.</span></span> <span data-ttu-id="285c6-128">예를 들어 관리 되지 않는 장치</span><span class="sxs-lookup"><span data-stu-id="285c6-128">For example, on unmanaged devices.</span></span>

- <span data-ttu-id="285c6-129">**다운로드 시 보호**: 중요 한 문서 다운로드를 차단 하는 대신 다운로드 시 암호화를 통해 문서를 보호 해야 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="285c6-129">**Protect on download**: Instead of blocking the download of sensitive documents, you can require documents to be protected via encryption on download.</span></span> <span data-ttu-id="285c6-130">이 암호화를 사용 하면 데이터가 신뢰할 수 없는 장치로 다운로드 되는 경우 문서가 보호 되 고 사용자 액세스가 인증 됩니다.</span><span class="sxs-lookup"><span data-stu-id="285c6-130">This encryption makes sure the document is protected and user access is authenticated if the data is downloaded to an untrusted device.</span></span>

- <span data-ttu-id="285c6-131">**낮은 신뢰 사용자 세션 모니터링**: 위험한 사용자가 앱에 로그인 할 때 모니터링 되 고 해당 작업이 세션 내에서 로그에 기록 되는 경우</span><span class="sxs-lookup"><span data-stu-id="285c6-131">**Monitor low-trust user sessions**: Risky users are monitored when they sign into apps and their actions are logged from within the session.</span></span> <span data-ttu-id="285c6-132">나중에 세션 정책을 적용 해야 하는 위치를 이해 하기 위해 사용자 동작을 조사 하 고 분석할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="285c6-132">You can investigate and analyze user behavior to understand where, and under what conditions, session policies should be applied in the future.</span></span>

- <span data-ttu-id="285c6-133">**차단 액세스**: 관리 되지 않는 장치 또는 회사 이외의 네트워크에서 들어오는 사용자에 대 한 특정 앱에 대 한 액세스를 완전히 차단할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="285c6-133">**Block access**: You can completely block access to specific apps for users coming from unmanaged devices or from non-corporate networks.</span></span>

- <span data-ttu-id="285c6-134">**읽기 전용 모드 만들기**: 사용자 지정 앱 내 활동을 모니터링 하 고 차단 하면 특정 사용자에 대 한 특정 앱에 대 한 읽기 전용 모드를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="285c6-134">**Create read-only mode**: By monitoring and blocking custom in-app activities, you can create a read-only mode to specific apps for specific users.</span></span>

- <span data-ttu-id="285c6-135">**비 회사 네트워크에서 사용자 세션 제한**: 회사 네트워크에 포함 되지 않은 위치에서 보호 된 앱에 액세스 하는 사용자는 제한 된 액세스를 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="285c6-135">**Restrict user sessions from non-corporate networks**: Users accessing a protected app from a location that isn't part of your corporate network are allowed restricted access.</span></span> <span data-ttu-id="285c6-136">중요 한 자료의 다운로드는 차단 되거나 보호 됩니다.</span><span class="sxs-lookup"><span data-stu-id="285c6-136">The download of sensitive materials is blocked or protected.</span></span>

### <a name="how-session-control-works"></a><span data-ttu-id="285c6-137">세션 제어 작동 방식</span><span class="sxs-lookup"><span data-stu-id="285c6-137">How session control works</span></span>

<span data-ttu-id="285c6-138">조건부 액세스 앱 컨트롤을 사용 하 여 세션 정책을 만들면 앱에 직접 연결 하는 대신 역방향 프록시를 통해 사용자 세션을 제어할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="285c6-138">Creating a session policy with Conditional Access App Control enables you to control user sessions by redirecting the user through a reverse proxy instead of directly to the app.</span></span> <span data-ttu-id="285c6-139">그런 다음, 사용자 요청 및 응답은 앱에 직접 실행 되는 것이 아니라 Office 365 Cloud App Security를 통해 진행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="285c6-139">From then on, user requests and responses go through Office 365 Cloud App Security rather than directly to the app.</span></span>

<span data-ttu-id="285c6-140">사용자를 세션 내에 유지 하기 위해 앱 세션 내의 모든 관련 url, Java 스크립트 및 쿠키가 Office 365 Cloud app Security url로 대체 됩니다.</span><span class="sxs-lookup"><span data-stu-id="285c6-140">To keep the user within the session, all the relevant URLs, Java scripts, and cookies within the app session are replaced with Office 365 Cloud App Security URLs.</span></span> <span data-ttu-id="285c6-141">예를 들어 앱이 myapp.com로 끝나는 링크가 있는 페이지를 반환 하는 경우 링크가 다음과 같이 끝나는 도메인으로 대체 됩니다.</span><span class="sxs-lookup"><span data-stu-id="285c6-141">For example, if the app returns a page with links whose domains end with myapp.com, the link is replaced with domains ending with something like: myapp.com.us.cas.ms</span></span>

<span data-ttu-id="285c6-142">이 방법에서는 장치에 아무것도 설치할 필요가 없습니다.</span><span class="sxs-lookup"><span data-stu-id="285c6-142">This method doesn't require you to install anything on the device.</span></span> <span data-ttu-id="285c6-143">이 메서드는 관리 되지 않는 장치에서 세션을 모니터할 때 이상적입니다.</span><span class="sxs-lookup"><span data-stu-id="285c6-143">This method is ideal when monitoring sessions from unmanaged devices.</span></span>

<span data-ttu-id="285c6-144">Office 365 Cloud App Security를 통해 세션이 전송 된 후에는 다음 작업을 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="285c6-144">After a session is directed through Office 365 Cloud App Security, the following actions can be done:</span></span>

1. <span data-ttu-id="285c6-145">사용자 작업에 대 한 트래픽 조사</span><span class="sxs-lookup"><span data-stu-id="285c6-145">Inspect the traffic for user activities</span></span>

2. <span data-ttu-id="285c6-146">Office 365 Cloud App Security Activity log에서 식별 된 활동 표시</span><span class="sxs-lookup"><span data-stu-id="285c6-146">Display the identified activities in the Office 365 Cloud App Security Activity log</span></span>

3. <span data-ttu-id="285c6-147">트래픽 로그 저장 및 분석</span><span class="sxs-lookup"><span data-stu-id="285c6-147">Save the traffic logs and analyze them</span></span>

4. <span data-ttu-id="285c6-148">관리자가 트래픽 로그를 내보내도록 설정</span><span class="sxs-lookup"><span data-stu-id="285c6-148">Enable the admin to export the traffic logs</span></span>

5. <span data-ttu-id="285c6-149">세션에 대 한 정책 적용</span><span class="sxs-lookup"><span data-stu-id="285c6-149">Enforce policies on the session</span></span>

## <a name="managed-device-identification"></a><span data-ttu-id="285c6-150">관리 되는 장치 식별</span><span class="sxs-lookup"><span data-stu-id="285c6-150">Managed device identification</span></span>

<span data-ttu-id="285c6-151">조건부 액세스 앱 컨트롤을 사용 하면 장치 관리 여부를 고려 하는 정책을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="285c6-151">Conditional Access App Control enables you to create policies that take into account whether a device is managed or not.</span></span> <span data-ttu-id="285c6-152">장치가 관리 되는지 여부를 확인 하려면 다음 기능을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="285c6-152">To identify whether a device is managed or not, the feature uses:</span></span>

- <span data-ttu-id="285c6-153">호환 되는 장치</span><span class="sxs-lookup"><span data-stu-id="285c6-153">Compliant devices</span></span>

- <span data-ttu-id="285c6-154">도메인에 가입 된 장치</span><span class="sxs-lookup"><span data-stu-id="285c6-154">Domain-joined devices</span></span>

- <span data-ttu-id="285c6-155">클라이언트 인증서 배포</span><span class="sxs-lookup"><span data-stu-id="285c6-155">Client certificates deployment</span></span>

### <a name="compliant-and-domain-joined-devices"></a><span data-ttu-id="285c6-156">규격 및 도메인에 가입 된 장치</span><span class="sxs-lookup"><span data-stu-id="285c6-156">Compliant and domain-joined devices</span></span>

<span data-ttu-id="285c6-157">Azure AD 조건부 액세스를 사용 하면 호환 및 도메인에 가입 된 장치 정보를 Office 365 Cloud App Security로 직접 전달할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="285c6-157">Azure AD conditional access enables compliant and domain-joined device information to be passed directly to Office 365 Cloud App Security.</span></span> <span data-ttu-id="285c6-158">여기서는 장치 상태를 필터로 사용 하는 액세스 정책 또는 세션 정책을 개발할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="285c6-158">From there, an access policy or a session policy can be developed that uses device state as a filter.</span></span> <span data-ttu-id="285c6-159">자세한 내용은 [Azure Active Directory의 장치 관리 소개](https://docs.microsoft.com/azure/active-directory/device-management-introduction)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="285c6-159">For more information, see the [Introduction to device management in Azure Active Directory](https://docs.microsoft.com/azure/active-directory/device-management-introduction).</span></span>

### <a name="client-certificate-authenticated-devices"></a><span data-ttu-id="285c6-160">클라이언트 인증서 인증 장치</span><span class="sxs-lookup"><span data-stu-id="285c6-160">Client-certificate authenticated devices</span></span>

<span data-ttu-id="285c6-161">장치 식별 메커니즘은 클라이언트 인증서를 사용 하 여 관련 디바이스에서 인증을 요청할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="285c6-161">The device identification mechanism can request authentication from relevant devices using client certificates.</span></span> <span data-ttu-id="285c6-162">조직에 이미 배포 된 기존 클라이언트 인증서를 사용 하거나 관리 되는 장치에 새 클라이언트 인증서를 롤아웃할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="285c6-162">You can either use existing client certificates already deployed in your organization or roll out new client certificates to managed devices.</span></span> <span data-ttu-id="285c6-163">그런 다음 이러한 인증서가 있는지 여부를 사용 하 여 액세스 및 세션 정책을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="285c6-163">You then use the presence of those certificates to set access and session policies.</span></span> <span data-ttu-id="285c6-164">클라이언트 인증서를 배포 하는 방법에 대 한 자세한 내용은 [deploy 조건부 Access App Control for Office 365 apps](ocas-deploy-conditional-access-app-control.md)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="285c6-164">For information on how to deploy client certificates see [Deploy Conditional Access App Control for Office 365 apps](ocas-deploy-conditional-access-app-control.md).</span></span>

## <a name="supported-apps-and-clients"></a><span data-ttu-id="285c6-165">지원 되는 앱 및 클라이언트</span><span class="sxs-lookup"><span data-stu-id="285c6-165">Supported apps and clients</span></span>

<span data-ttu-id="285c6-166">Office 365에 대 한 조건부 Access 앱 컨트롤은 다음과 같은 추천 앱을 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="285c6-166">Conditional Access App Control for Office 365 supports the following featured apps:</span></span>

- <span data-ttu-id="285c6-167">Exchange Online (미리 보기)</span><span class="sxs-lookup"><span data-stu-id="285c6-167">Exchange Online (preview)</span></span>

- <span data-ttu-id="285c6-168">비즈니스용 OneDrive (미리 보기)</span><span class="sxs-lookup"><span data-stu-id="285c6-168">OneDrive for Business (preview)</span></span>

- <span data-ttu-id="285c6-169">Power BI (미리 보기)</span><span class="sxs-lookup"><span data-stu-id="285c6-169">Power BI (preview)</span></span>

- <span data-ttu-id="285c6-170">SharePoint Online (미리 보기)</span><span class="sxs-lookup"><span data-stu-id="285c6-170">SharePoint Online (preview)</span></span>

- <span data-ttu-id="285c6-171">Microsoft 팀 (미리 보기)</span><span class="sxs-lookup"><span data-stu-id="285c6-171">Microsoft Teams (preview)</span></span>

- <span data-ttu-id="285c6-172">Yammer (미리 보기)</span><span class="sxs-lookup"><span data-stu-id="285c6-172">Yammer (preview)</span></span>

<span data-ttu-id="285c6-173">추가 앱이 계속 해 서 세션 제어에 boarded.</span><span class="sxs-lookup"><span data-stu-id="285c6-173">Additional apps are being continuously on-boarded to session control.</span></span>

## <a name="next-steps"></a><span data-ttu-id="285c6-174">다음 단계</span><span class="sxs-lookup"><span data-stu-id="285c6-174">Next steps</span></span>

- [<span data-ttu-id="285c6-175">Office 365 앱용 조건부 액세스 앱 컨트롤 배포</span><span class="sxs-lookup"><span data-stu-id="285c6-175">Deploy Conditional Access App Control for Office 365 apps</span></span>](ocas-deploy-conditional-access-app-control.md)

- [<span data-ttu-id="285c6-176">Office 365 Cloud App Security의 세션 정책에 대해 자세히 알아보기</span><span class="sxs-lookup"><span data-stu-id="285c6-176">Learn about session policies in Office 365 Cloud App Security</span></span>](ocas-session-policies.md)

- [<span data-ttu-id="285c6-177">Office 365 Cloud App Security의 액세스 정책에 대해 자세히 알아보기</span><span class="sxs-lookup"><span data-stu-id="285c6-177">Learn about access policies in Office 365 Cloud App Security</span></span>](ocas-access-policies.md) 