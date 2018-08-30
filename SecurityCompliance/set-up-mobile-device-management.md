---
title: 모바일 장치 관리 (MDM) Office 365의 설정
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 6/29/2018
ms.audience: Admin
ms.topic: get-started-article
f1_keywords:
- O365M_OverviewMDM
- 'O365E_OverviewMDM '
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MED150
- MBS150
- MET150
ms.assetid: dd892318-bc44-4eb1-af00-9db5430be3cd
description: Office 365에 대 한 기본 제공 되는 모바일 장치 관리를 사용 하면 보안을 유지 하 고 Iphone, Ipad, Androids, 같은 사용자의 모바일 장치를 관리 하 고 Windows 전화 합니다. 시작 하기를 활성화 하 고 Office 365에 대 한 모바일 장치 관리를 설정 하려면 다음이 단계를 수행 합니다.
ms.openlocfilehash: c92290170b2937067e7407787282eaaa368b25b7
ms.sourcegitcommit: c31424cafbf1953f2864d7e2ceb95b329a694edb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/29/2018
ms.locfileid: "23272363"
---
# <a name="set-up-mobile-device-management-mdm-in-office-365"></a><span data-ttu-id="9fc22-104">모바일 장치 관리 (MDM) Office 365의 설정</span><span class="sxs-lookup"><span data-stu-id="9fc22-104">Set up Mobile Device Management (MDM) in Office 365</span></span>

<span data-ttu-id="9fc22-p102">Office 365에 대 한 기본 제공 모바일 장치 관리 (MDM)는를 사용 하면 보안을 유지 하 고 Iphone, Ipad, Androids, 같은 사용자의 모바일 장치를 관리 하 고 Windows 전화 합니다. 수 및 장치 보안 정책 관리, 원격으로 장치 지우기 시도 만들고 자세한 장치 보고서를 볼 합니다.</span><span class="sxs-lookup"><span data-stu-id="9fc22-p102">The built-in Mobile Device Management (MDM) for Office 365 helps you secure and manage your users' mobile devices like iPhones, iPads, Androids, and Windows phones. You can create and manage device security policies, remotely wipe a device, and view detailed device reports.</span></span>
  
<span data-ttu-id="9fc22-p103">질문이 있습니까? [도움말 주소 관련 된 일반적인 질문에 대 한 FAQ](frequently-asked-questions-about-mdm.md)를 준비 했습니다. 사용할 수는 없습니다 주의 [파트너: 위임 된 관리 제공](https://support.office.com/article/26530dc0-ebba-415b-86b1-b55bc06b073e) Office 365에 대 한 모바일 장치 관리를 관리 하 합니다.</span><span class="sxs-lookup"><span data-stu-id="9fc22-p103">Have questions? We've put together [a FAQ to help address common questions](frequently-asked-questions-about-mdm.md). Be aware that you cannot use a [Partners: Offer delegated administration](https://support.office.com/article/26530dc0-ebba-415b-86b1-b55bc06b073e) to manage Mobile Device Management for Office 365.</span></span> 
  
<span data-ttu-id="9fc22-110">장치 관리는 보안의 일부 &amp; 준수 센터 MDM 설치를 시작 하려면 다음과 같은 이동 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="9fc22-110">Device management is part of the Security &amp; Compliance Center so you'll need to go there to kick off MDM setup.</span></span>
  
<span data-ttu-id="9fc22-111">Office 365에 대 한 모바일 장치 관리를 설정 하려면에 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="9fc22-111">To set up Mobile Device Management for Office 365 you'll need to:</span></span>
  
1. [<span data-ttu-id="9fc22-112">모바일 장치 관리 서비스를 활성화 합니다.</span><span class="sxs-lookup"><span data-stu-id="9fc22-112">Activate the Mobile Device Management service</span></span>](#activate-the-mobile-device-management-service)  
2. [<span data-ttu-id="9fc22-113">모바일 장치 관리 설정</span><span class="sxs-lookup"><span data-stu-id="9fc22-113">Set up Mobile Device Management</span></span>](#set-up-mobile-device-management)
3. [<span data-ttu-id="9fc22-114">사용자가 자신의 장치 등록 되었는지 확인</span><span class="sxs-lookup"><span data-stu-id="9fc22-114">Make sure users enroll their devices</span></span>](#step-4-recommended-manage-device-security-policies)
  
## <a name="activate-the-mobile-device-management-service"></a><span data-ttu-id="9fc22-115">모바일 장치 관리 서비스를 활성화 합니다.</span><span class="sxs-lookup"><span data-stu-id="9fc22-115">Activate the Mobile Device Management service</span></span>

1. <span data-ttu-id="9fc22-116">회사 또는 학교 계정을 사용하여 Office 365에 로그인합니다.</span><span class="sxs-lookup"><span data-stu-id="9fc22-116">Sign in to Office 365 with your work or school account.</span></span> 
    
2. <span data-ttu-id="9fc22-117">이동 [보안 &amp; 준수 센터](https://protection.office.com)합니다.</span><span class="sxs-lookup"><span data-stu-id="9fc22-117">Go to [Security &amp; Compliance Center](https://protection.office.com).</span></span>
    
3. <span data-ttu-id="9fc22-118">**데이터 손실 방지** 로 이동 \> **장치 관리** **아래의 단계를 시작** 하는 정품 인증 프로세스를 시작 하기를 클릭 하 고 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9fc22-118">Navigate to **Data loss prevention** \> **Device management** and click **Let's get started** to kick off the activation process.</span></span> 
    
    ![Office 365에 대 한 모바일 장치 관리 설정](media/368e1026-9aa5-431b-a722-8f7cf528f263.png)
  
4. <span data-ttu-id="9fc22-p104">시작 하는데 도움이 수에 대 한 기본 보안 정책을 만들었습니다. 이 페이지에는 보안 정책의 이름을 업데이트 하 고 **설치 프로그램을 시작**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="9fc22-p104">We created a default security policy for you to help you get started. Update the name of the security policy on this page, and then click **Start setup**.</span></span>
    
    ![모바일 장치 관리 보안 정책 설정](media/5619a2d1-f900-4268-9050-5d7eb57429a5.png)
  
5. <span data-ttu-id="9fc22-123">서비스를 설정에서 진행 상태를 표시 하는 설치 화면을 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9fc22-123">You'll see the setup screen that shows progress on setting up the service.</span></span>
    
    ![MDM 설치 진행률](media/db45d1bb-d247-4ac0-9deb-1b0c1ace9bfa.png)
  
> [!TIP]
> <span data-ttu-id="9fc22-p105">검색을 통해 **MDM 설치** 찾을 수 있습니다. Office 365 관리 센터에서 \> **홈** 페이지에서 **검색** 상자에 종류 모바일 장치 관리 합니다. > ![관리 센터에서 모바일 장치 관리에 대 한 검색](media/cd0ebf15-ef79-4eaa-ab5b-041ac0bd4e5b.png)</span><span class="sxs-lookup"><span data-stu-id="9fc22-p105">You can also locate **MDM Setup** through Search. In the Office 365 admin center \> **Home** page, type mobile device management in the **Search** box. > ![Search for mobile device management in the admin center](media/cd0ebf15-ef79-4eaa-ab5b-041ac0bd4e5b.png)</span></span>
  
<span data-ttu-id="9fc22-128">Office 365에 대 한 모바일 장치 관리를 활성화 하려면 시간이 다소 걸릴 수 하지만 적용 하려면 다음 단계를 설명 하는 전자 메일 받게 완료 되 면 합니다.</span><span class="sxs-lookup"><span data-stu-id="9fc22-128">It can take some time to activate Mobile Device Management for Office 365, but when it finishes, you'll receive an email that explains the next steps to take.</span></span>
  
## <a name="set-up-mobile-device-management"></a><span data-ttu-id="9fc22-129">모바일 장치 관리 설정</span><span class="sxs-lookup"><span data-stu-id="9fc22-129">Set up Mobile Device Management</span></span>

<span data-ttu-id="9fc22-p106">서비스를 수행할 준비가 되 면 설치를 완료 하는 다음 네가지 단계를 완료 합니다. **장치 관리** 페이지에서 보안 [설정 관리를](https://portal.office.com/EAdmin/Device/IntuneInventory.aspx) 클릭 해야 &amp; 준수 센터에서는 다음 설정을 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9fc22-p106">When the service is ready, complete the following four steps to finish setup. You may need to click [Manage settings](https://portal.office.com/EAdmin/Device/IntuneInventory.aspx) on the **Device management** page in the Security &amp; Compliance Center to see the following settings.</span></span> 
  
![권장 되는 단계 및 필요한 모바일 장치 관리 설정](media/d71e3c76-b6b9-4549-ade6-cbfab846d908.png)
  
### <a name="step-1-required-configure-domains-for-mdm"></a><span data-ttu-id="9fc22-133">MDM에 대 한 1 단계: (필수) 구성 도메인</span><span class="sxs-lookup"><span data-stu-id="9fc22-133">Step 1: (Required) Configure domains for MDM</span></span>

<span data-ttu-id="9fc22-p107">Office 365와 관련 된 사용자 지정 도메인 없는 또는 하지 Windows 장치를 관리 하는 경우에이 섹션을 건너뛸 수 있습니다. 그렇지 않은 경우 DNS 호스트에는 도메인에 대 한 DNS 레코드를 추가 하려면 필요 합니다. Office 365를 사용 하 여 도메인 설정의 일부로 이미, 레코드를 추가한 경우 모두 설정 합니다. 레코드를 추가한 후 사용자 지정 도메인을 사용 하는 전자 메일 주소와 해당 Windows 장치에 로그인 하면 조직에서 Office 365 사용자를 Office 365에 대 한 MDM에 등록할 리디렉션됩니다.</span><span class="sxs-lookup"><span data-stu-id="9fc22-p107">If you don't have a custom domain associated with Office 365 or if you're not managing Windows devices, you can skip this section. Otherwise, you'll need to add DNS records for the domain at your DNS host. If you've added the records already, as part of setting up your domain with Office 365, you're all set. After you add the records, Office 365 users in your organization who sign in on their Windows device with an email address that uses your custom domain are redirected to enroll in MDM for Office 365.</span></span>
  
<span data-ttu-id="9fc22-p108">레코드를 설정 하는 데 도움이 필요 하세요? [DNS 레코드를 관리 하는 경우 Office 365 용 DNS 레코드 만들기](https://support.office.com/article/b0f3fdca-8a80-4e8e-9ef3-61e8a2a9ab23) 에 제공 된 목록에서 도메인 등록자를 찾아 DNS 레코드 만들기 (영문)에 대 한 단계별 도움말으로 이동 하려면 등록자 이름을 선택 합니다. 이러한 지침을 사용 하 여 다음 두 레코드를 추가 하려면:</span><span class="sxs-lookup"><span data-stu-id="9fc22-p108">Need help setting up the records? Find your domain registrar in the list provided in [Create DNS records for Office 365 when you manage your DNS records](https://support.office.com/article/b0f3fdca-8a80-4e8e-9ef3-61e8a2a9ab23) and select the registrar name to go to step-by-step help for creating DNS records. Use those instructions to add the following two records:</span></span> 
  
|<span data-ttu-id="9fc22-141">**호스트 이름**</span><span class="sxs-lookup"><span data-stu-id="9fc22-141">**Host name**</span></span>|<span data-ttu-id="9fc22-142">**레코드 유형**</span><span class="sxs-lookup"><span data-stu-id="9fc22-142">**Record type**</span></span>|<span data-ttu-id="9fc22-143">**주소**</span><span class="sxs-lookup"><span data-stu-id="9fc22-143">**Address**</span></span>|<span data-ttu-id="9fc22-144">**TTL**</span><span class="sxs-lookup"><span data-stu-id="9fc22-144">**TTL**</span></span>|
|:-----|:-----|:-----|:-----|
|<span data-ttu-id="9fc22-145">EnterpriseEnrollment</span><span class="sxs-lookup"><span data-stu-id="9fc22-145">EnterpriseEnrollment</span></span>  <br/> |<span data-ttu-id="9fc22-146">CNAME</span><span class="sxs-lookup"><span data-stu-id="9fc22-146">CNAME</span></span>  <br/> |<span data-ttu-id="9fc22-147">EnterpriseEnrollment.manage.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="9fc22-147">EnterpriseEnrollment.manage.microsoft.com</span></span>  <br/> |<span data-ttu-id="9fc22-148">3600</span><span class="sxs-lookup"><span data-stu-id="9fc22-148">3600</span></span>  <br/> |
|<span data-ttu-id="9fc22-149">EnterpriseRegistration</span><span class="sxs-lookup"><span data-stu-id="9fc22-149">EnterpriseRegistration</span></span>  <br/> |<span data-ttu-id="9fc22-150">CNAME</span><span class="sxs-lookup"><span data-stu-id="9fc22-150">CNAME</span></span>  <br/> |<span data-ttu-id="9fc22-151">EnterpriseRegistration.windows.net</span><span class="sxs-lookup"><span data-stu-id="9fc22-151">EnterpriseRegistration.windows.net</span></span>  <br/> |<span data-ttu-id="9fc22-152">3600</span><span class="sxs-lookup"><span data-stu-id="9fc22-152">3600</span></span>  <br/> |
   
<span data-ttu-id="9fc22-153">두 레코드를 추가한 후 보안으로 다시 이동 &amp; 준수 센터 **장치 관리** 로 이동 하 고 \> 다음 단계를 완료 하려면 **관리 설정** 합니다.</span><span class="sxs-lookup"><span data-stu-id="9fc22-153">After you add the two records, go back to the Security &amp; Compliance Center and navigate to **Device management** \> **Manage settings** to complete the next step.</span></span> 
  
### <a name="step-2-required-configure-an-apns-certificate-for-ios-devices"></a><span data-ttu-id="9fc22-154">2 단계: (필수) 구성 iOS 장치에 대 한 한 apn을 사용할 인증서를</span><span class="sxs-lookup"><span data-stu-id="9fc22-154">Step 2: (Required) Configure an APNs Certificate for iOS devices</span></span>

<span data-ttu-id="9fc22-155">IPad / Iphone 같은 iOS 장치를 관리 하려면 한 apn을 사용할 인증서를 만들려면 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="9fc22-155">To manage iOS devices like iPad and iPhones, you need to create an APNs certificate.</span></span>
  
<span data-ttu-id="9fc22-156">이 위해 **설치 모바일 장치 관리 페이지**에서 **설정** 링크에서 단계를 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="9fc22-156">To do this, follow the steps from the **Set up** links on the **Setup mobile device management page**.</span></span>
  
1. <span data-ttu-id="9fc22-157">**IOS 장치에 대 한 한 apn을 사용할 인증서 구성**옆에 있는 **설정**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="9fc22-157">Next to **Configure a APNs Certificate for iOS devices**, select **Set up**.</span></span>
    
2. <span data-ttu-id="9fc22-158">**CSR 파일 다운로드** 를 선택 하 고 인증서 서명 요청을 곳에 저장 기억할 수 있는 컴퓨터에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9fc22-158">Select **Download your CSR file** and save the Certificate signing request to a somewhere on your computer that you'll remember.</span></span> 
    
    ![APN 인증서 대화 상자를 설치 합니다.](media/03aa8a24-e95c-4077-9b6b-ef76a86bafd7.png)
  
3. <span data-ttu-id="9fc22-160">**다음**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="9fc22-160">Select **Next**.</span></span>
    
4. <span data-ttu-id="9fc22-161">APN 인증서를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9fc22-161">Create an APN certificate.</span></span>
    
  - <span data-ttu-id="9fc22-162">**Apple 한 apn을 사용할 포털** Apple 푸시 인증서 포털을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="9fc22-162">Select **Apple APNS Portal** to open the Apple Push Certificates Portal.</span></span> 
    
    ![Apple 한 apn을 사용할 포털을 선택 된 APN 알림 인증서 대화 상자를 설치 합니다.](media/ce19f53c-f44a-470b-baf3-9278dfda2ba5.png)
  
  - <span data-ttu-id="9fc22-164">Apple ID를 사용 하 여 로그인</span><span class="sxs-lookup"><span data-stu-id="9fc22-164">Sign in with an Apple ID.</span></span>
    
    > [!IMPORTANT]
    > <span data-ttu-id="9fc22-p109">Apple ID 관리 하는 계정 사용자를 떠날 하는 경우에 사용자의 조직과 상태로 유지 되는 전자 메일 계정과 연결 된 회사를 사용 합니다. 인증서를 갱신 하는 경우 동일한 ID를 사용 하 여 수행 해야 하기 때문에이 ID를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="9fc22-p109">Use a company Apple ID associated with an email account that will remain with your organization even if the user who manages the account leaves. Save this ID because you'll need to use the same ID when it's time to renew the certificate.</span></span> 
  
  - <span data-ttu-id="9fc22-167">**인증서 만들기** 를 선택 하 고 **사용 약관에**동의 합니다.</span><span class="sxs-lookup"><span data-stu-id="9fc22-167">Select **Create a Certificate** and accept the **Terms of Use**.</span></span>
    
  - <span data-ttu-id="9fc22-168">Office 365 및 **업로드**선택에서 사용자 컴퓨터로 다운로드 한 인증서 서명 요청 **이동** 합니다.</span><span class="sxs-lookup"><span data-stu-id="9fc22-168">**Browse** to the Certificate signing request you downloaded to your computer from Office 365 and select **Upload**.</span></span>
    
  - <span data-ttu-id="9fc22-169">APN 인증서는 Apple 푸시 인증서 포털에서 사용자의 컴퓨터에 만든 **다운로드** 합니다.</span><span class="sxs-lookup"><span data-stu-id="9fc22-169">**Download** the APN certificate created by the Apple Push Certificate Portal to your computer.</span></span> 
    
    > [!TIP]
    > <span data-ttu-id="9fc22-170">인증서를 다운로드 하는데 문제가 경우 브라우저를 새로 고쳐 합니다.</span><span class="sxs-lookup"><span data-stu-id="9fc22-170">If you're having trouble downloading the certificate, refresh your browser.</span></span> 
  
5. <span data-ttu-id="9fc22-171">Office 365로 다시 이동 하 고 **다음** **한 apn을 업로드 하는 사용할 인증서** 페이지를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="9fc22-171">Go back to Office 365 and select **Next** to get to the **Upload APNS certificate** page.</span></span> 
    
6. <span data-ttu-id="9fc22-172">Apple 푸시 인증서 포털에서 다운로드 한 APN 인증서로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="9fc22-172">Browse to the APN certificate you downloaded from the Apple Push Certificates Portal.</span></span>
    
    ![Apple에서 다운로드 한 apn을 사용할 인증서를 선택 하려면 찾아보기 단추를 클릭 합니다.](media/afe2849d-af23-4c55-9009-d8f25edaf6c0.png)
  
7. <span data-ttu-id="9fc22-174">**완료 날짜**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="9fc22-174">Select **Finish**.</span></span>
    
<span data-ttu-id="9fc22-175">APN 인증서를 추가한 후 보안으로 다시 이동 &amp; 준수 센터 **장치 관리** 로 이동 하 고 \> 다음 단계를 완료 하려면 **관리 설정** 합니다.</span><span class="sxs-lookup"><span data-stu-id="9fc22-175">After you add APN Certificate, go back to the Security &amp; Compliance Center and navigate to **Device management** \> **Manage settings** to complete the next step.</span></span> 
  
### <a name="step-3-recommended-set-up-multi-factor-authentication"></a><span data-ttu-id="9fc22-176">3 단계: 다단계 인증 설정 (권장)</span><span class="sxs-lookup"><span data-stu-id="9fc22-176">Step 3: (Recommended) Set up multi-factor authentication</span></span>

<span data-ttu-id="9fc22-p110">다단계 인증 (MFA) **권장 단계**아래에 표시 되지 않으면, 하는 경우에이 섹션을 건너뛸 수 있습니다. 이 옵션은 표시 하는 경우에 Office 365 등록 프로세스에 대 한 모바일 장치 관리의 보안을 강화 하기 Azure AD 포털에서 MFA에 설정 하는 것이 좋습니다. 기본적으로 해제 되어 합니다.</span><span class="sxs-lookup"><span data-stu-id="9fc22-p110">If you don't see multi-factor authentication (MFA) under **Recommended steps**, you can skip this section. If this option is listed, we recommend you turn on MFA in the Azure AD portal to increase the security of the Mobile Device Management for Office 365 enrollment process. It is turned off by default.</span></span>
  
<span data-ttu-id="9fc22-p111">MFA 두번째 형태의 인증을 요구 하 여 모바일 장치 등록을 위한 Office 365에 로그인 secure 도움이 됩니다. 사용자가 전화 통화, 텍스트 메시지 또는 올바르게 자신의 작업 계정 암호를 입력 한 후가 모바일 장치에서 응용 프로그램 알림 승인 하는 데 필요 합니다. 인증의 두번째 폼이 완료 되 면 해당 장치만 등록할 수 있습니다. 사용자의 장치는 Office 365에 대 한 모바일 장치 관리에 등록 된, 사용자가 자신의 작업 계정에만 사용 하 여 Office 365 리소스 액세스할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9fc22-p111">MFA helps secure the sign in to Office 365 for mobile device enrollment by requiring a second form of authentication. Users are required to acknowledge a phone call, text message, or app notification on their mobile device after correctly entering their work account password. They can only enroll their device after this second form of authentication is completed. After users' devices are enrolled in Mobile Device Management for Office 365, users can access Office 365 resources with just their work account.</span></span>
  
<span data-ttu-id="9fc22-p112">**다단계 인증 설정**옆에 있는 **설정**을 선택 합니다. MFA Azure AD 포털에서 사용 하는 방법을 알아보려면 [다단계 인증 설정](https://go.microsoft.com/fwlink/p/?LinkId=519255)을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="9fc22-p112">Next to **Set up multi-factor authentication**, select **Set up**. To learn how to turn on MFA in the Azure AD portal, see [Set up multi-factor authentication](https://go.microsoft.com/fwlink/p/?LinkId=519255).</span></span>
  
<span data-ttu-id="9fc22-186">MFA를 설정한 후 보안으로 다시 이동 &amp; 준수 센터 **장치 관리** 로 이동 하 고 \> 다음 단계를 완료 하려면 **관리 설정** 합니다.</span><span class="sxs-lookup"><span data-stu-id="9fc22-186">After you set up MFA, go back to the Security &amp; Compliance Center and navigate to **Device management** \> **Manage settings** to complete the next step.</span></span> 
  
### <a name="step-4-recommended-manage-device-security-policies"></a><span data-ttu-id="9fc22-187">4 단계: (권장) 관리 장치 보안 정책</span><span class="sxs-lookup"><span data-stu-id="9fc22-187">Step 4: (Recommended) Manage device security policies</span></span>

<span data-ttu-id="9fc22-p113">다음 단계를 만들고 Office 365 조직의 데이터를 보호 하는 장치 보안 정책 배포 됩니다. 사용자가 비활성 5 분 후 잠금 장치에는 정책을 만들어 해당 장치를 잃어버린 경우 데이터 손실을 방지 하 고 장치가 도움이 되는 예 3-로그인 실패 한 후 데이터 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="9fc22-p113">The next step is to create and deploy device security policies to help protect your Office 365 organization's data. For example, you can help prevent data loss if a user loses their device by creating a policy to lock devices after 5 minutes of inactivity and have devices wiped after 3 sign-in failures.</span></span>
  
<span data-ttu-id="9fc22-190">**보안 &amp; 준수 센터** **보안 정책** 으로 이동, \> **장치 보안 정책** 장치 보안 정책을 만들고이 규칙에 액세스 합니다.</span><span class="sxs-lookup"><span data-stu-id="9fc22-190">In the **Security &amp; Compliance Center**, go to **Security policies** \> **Device security policies** to create device security policies and access rules.</span></span> 
  
![장치 보안 정책 추가](media/69a027f5-fbfb-482a-b850-9ccb280b8c62.png)
  
<span data-ttu-id="9fc22-192">새 정책을 만들려면 하는 방법에는 단계별 지침을 참조 하십시오. [만들기 및 장치 보안 정책 배포](create-device-security-policies.md)합니다.</span><span class="sxs-lookup"><span data-stu-id="9fc22-192">For step by step instructions on how to create a new policy, see [Create and deploy device security policies](create-device-security-policies.md).</span></span>
  
> [!TIP]
>  <span data-ttu-id="9fc22-p114">새 정책을 만들 때에 사용자의 장치 정책와 호환 되지 않습니다 액세스 및 보고서 정책 위반을 허용 하도록 정책을 설정 하는 것이 좋습니다. 이 얼마나 많은 모바일 장치에서 Office 365에 대 한 액세스를 차단 하지 않고 정책에 의해 영향을 받는 것을 볼 수 있습니다. > 새 정책을 모든 사람에 게 조직에 배포 하기 전에 사용자 수가 적은에서 사용 하는 장치에서 테스트 하는 것이 좋습니다. > 또한 정책을 배포 하기 전에 Office 365에 대 한 MDM에서 장치를 등록의 잠재적 영향을 알고 있는 조직 수 있도록 합니다. 정책 설정 방법에 따라 이러한 (비준수 장치)를 준수 하지 장치는 Office 365에 액세스 하지 못하도록 차단할 수 있습니다. 비 호환 장치 앱 설치, 사진 및 기타 개인 정보는 등록 된 장치에서 삭제 될 수 있습니다는 장치 데이터 삭제 하는 경우는 있을 수 있습니다. 추가 정보: [Office 365의 모바일 장치 지우기 시도](wipe-a-mobile-device.md)합니다.</span><span class="sxs-lookup"><span data-stu-id="9fc22-p114">When you create a new policy, you might want to set the policy to allow access and report policy violation where a user's device isn't compliant with the policy. This lets you see how many mobile devices would be impacted by the policy without blocking access to Office 365. >  Before you deploy a new policy to everyone in your organization, we recommend you test it on the devices used by a small number of users. >  Also, before you deploy policies, let your organization know the potential impacts of enrolling a device in MDM for Office 365. Depending on how you set up the policies, devices that don't comply with them (non-compliant devices) could be blocked from accessing Office 365. Non-compliant devices might also have apps installed, photos, and other personal information which, on an enrolled device, could be deleted if the device is wiped. More info: [Wipe a mobile device in Office 365](wipe-a-mobile-device.md).</span></span> 
  
## <a name="make-sure-users-enroll-their-devices"></a><span data-ttu-id="9fc22-200">사용자가 자신의 장치 등록 되었는지 확인</span><span class="sxs-lookup"><span data-stu-id="9fc22-200">Make sure users enroll their devices</span></span>

<span data-ttu-id="9fc22-p115">만들어 모바일 장치 관리 정책 배포 했을 때 후 장치 정책에 적용 되는 조직에서 사용이 허가 된 각 Office 365 사용자가 받습니다 등록 메시지 다음에 자신의 모바일 장치에서 Office 365에 로그인 합니다. Office 365 전자 메일 및 문서에 액세스할 수 있으려면 등록 및 정품 인증 단계를 완료 해야 있습니다. [작업 또는 학교에 대 한 모바일 장치 등록](enroll-your-mobile-device.md)을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="9fc22-p115">After you've created and deployed a mobile device management policy, each licensed Office 365 user in your organization that the device policy applies to will receive an enrollment message the next time they sign into Office 365 from their mobile device. They must complete the enrollment and activation steps before they can access Office 365 email and documents. See [Enroll your mobile device for work or school](enroll-your-mobile-device.md).</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="9fc22-p116">사용자의 기본 설정된 언어 등록 프로세스에 의해 지원 되지 않으면 사용자가 다른 언어로 등록 알림 및 작업 단계는 모바일 장치에서 받을 수 있습니다. Office 365에서 지원 되는 일부 언어는 모바일 장치에는 등록 프로세스에 대 한 현재 지원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9fc22-p116">If a user's preferred language isn't supported by the enrollment process, users may receive enrollment notification and steps on their mobile devices in another language. Not all languages supported in Office 365 are currently supported for the enrollment process on mobile devices.</span></span> 
  
<span data-ttu-id="9fc22-206">Android 또는 iOS 장치를 사용 하는 사용자는 등록 프로세스의 일부로 회사 포털 응용 프로그램을 설치 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="9fc22-206">Users with Android or iOS devices are required to install the Company Portal app as part of the enrollment process.</span></span>
  
## <a name="related-topics"></a><span data-ttu-id="9fc22-207">관련 항목</span><span class="sxs-lookup"><span data-stu-id="9fc22-207">Related Topics</span></span>

[<span data-ttu-id="9fc22-208">모바일 장치 관리의 기능</span><span class="sxs-lookup"><span data-stu-id="9fc22-208">Capabilities of Mobile Device Management</span></span>](capabilities-of-mobile-device-management.md)
  
[<span data-ttu-id="9fc22-209">장치 보안 정책 만들기 및 배포</span><span class="sxs-lookup"><span data-stu-id="9fc22-209">Create and deploy device security policies</span></span>](create-device-security-policies.md)
  

