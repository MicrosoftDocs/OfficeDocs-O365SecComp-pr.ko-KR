---
title: Office 365 메시지 암호화 관리
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 6/13/2018
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 09f6737e-f03f-4bc8-8281-e46d24ee2a74
description: 설정을를 Office 365 메시지 암호화 OME ()을 완료 한 후 다양 한 방법으로에서 배포의 구성을 사용자 지정할 수 있습니다. 등을 1 회 암호가 하 고, 웹, 등의 Outlook에서 암호로 보호 단추를 표시 여부를 구성할 수 있습니다. 이 문서의 작업에 설명 방법입니다.
ms.openlocfilehash: ddc86bdf0d0ce5480587862a4ed438b6c138987f
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22533236"
---
# <a name="manage-office-365-message-encryption"></a><span data-ttu-id="bf1ad-105">Office 365 메시지 암호화 관리</span><span class="sxs-lookup"><span data-stu-id="bf1ad-105">Manage Office 365 Message Encryption</span></span>

<span data-ttu-id="bf1ad-p102">설정을를 Office 365 메시지 암호화 OME ()을 완료 한 후 다양 한 방법으로에서 배포의 구성을 사용자 지정할 수 있습니다. 등을 1 회 암호가 하 고, 웹, 등의 Outlook에서 **암호로 보호** 단추를 표시 여부를 구성할 수 있습니다. 이 문서의 작업에 설명 방법입니다.</span><span class="sxs-lookup"><span data-stu-id="bf1ad-p102">Once you've finished setting up Office 365 Message Encryption (OME), you can customize the configuration of your deployment in a number of ways. For example, you can configure whether to enable one-time pass codes, display the **Protect** button in Outlook on the web, and more. The tasks in this article describe how.</span></span> 
  
||
|:-----|
|<span data-ttu-id="bf1ad-p103">이 문서는 Office 365 메시지 암호화에 대 한 문서를 더 큰 시리즈의 일부입니다. 이 문서는 관리자 및 IT 전문가 위한 것입니다. 방금 경우 보내거나 암호화 된 메시지를 받는 방법에 대 한 정보에 대 한 자세한 내용은 [Office 365 메시지 암호화 OME ()](ome.md) 의 문서 목록을 참조 하 고 요구 사항에 가장 적합 한 문서를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="bf1ad-p103">This article is part of a larger series of articles about Office 365 Message Encryption. This article is intended for administrators and IT Pros. If you're just looking for information on sending or receiving an encrypted message, see the list of articles in [Office 365 Message Encryption (OME)](ome.md) and locate the article that best fits your needs.</span></span> |
   
## <a name="managing-whether-google-yahoo-and-microsoft-account-recipients-can-use-these-accounts-to-sign-in-to-the-office-365-message-encryption-portal"></a><span data-ttu-id="bf1ad-112">Google, yahoo 및 Microsoft 계정 받는 사람에 게 이러한 계정을 사용 하 여 Office 365 메시지 암호화 포털에 로그인 할 수 있는지 여부를 관리 합니다.</span><span class="sxs-lookup"><span data-stu-id="bf1ad-112">Managing whether Google, Yahoo, and Microsoft Account recipients can use these accounts to sign in to the Office 365 Message Encryption portal</span></span>
<span data-ttu-id="bf1ad-113"><a name="PermitSocialID"> </a></span><span class="sxs-lookup"><span data-stu-id="bf1ad-113"></span></span>

<span data-ttu-id="bf1ad-p104">기본적으로 새 Office 365 메시지 암호화 기능을 설정 하는 경우 조직의 사용자가 메시지를 보낼 수는 Office 365 조직 외부의 받는 사람에 게 있습니다. 받는 사람이 공유 ID를 사용 하 여 OME 포털에 로그인 할 수 받는 Google 계정, yahoo 계정 또는 Microsoft 계정 같은 *공유 ID* 를 사용 하는 경우 원할 경우 OME 포털에 로그인 하려면 공유 Id를 사용 하 여 받는 사람을 사용할 수 없도록 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bf1ad-p104">By default, when you set up the new Office 365 Message Encryption capabilities, users in your organization can send messages to recipients that are outside of your Office 365 organization. If the recipient uses a  *social ID*  such as a Google account, Yahoo account, or Microsoft account, the recipient can sign in to the OME portal using the social ID. If you want, you can choose not to allow recipients to use social IDs to sign in to the OME portal.</span></span> 
  
 <span data-ttu-id="bf1ad-117">**OME 포털에 로그인 하려면 공유 Id를 사용 하 여 받는 사람에 게 허용 여부를 관리 하려면**</span><span class="sxs-lookup"><span data-stu-id="bf1ad-117">**To manage whether or not to allow recipients to use social IDs to sign in to the OME portal**</span></span>
  
1. <span data-ttu-id="bf1ad-118">[원격 PowerShell을 사용 하 여 온라인 Exchange에 연결](http://technet.microsoft.com/library/jj984289%28v=exchg.150%29.aspx)합니다.</span><span class="sxs-lookup"><span data-stu-id="bf1ad-118">[Connect to Exchange Online Using Remote PowerShell](http://technet.microsoft.com/library/jj984289%28v=exchg.150%29.aspx).</span></span>
    
2. <span data-ttu-id="bf1ad-119">다음과 같이 SocialIdSignIn 매개 변수와 함께 Set-omeconfiguration cmdlet를 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="bf1ad-119">Run the Set-OMEConfiguration cmdlet with the SocialIdSignIn parameter as follows:</span></span>
    
  ```
  Set-OMEConfiguration -Identity <"OMEConfigurationIdParameter "> -SocialIdSignIn <$true |$false >
  ```

    <span data-ttu-id="bf1ad-120">예: 공유 Id를 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bf1ad-120">For example, to disable social IDs:</span></span>
    
  ```
  Set-OMEConfiguration -Identity "OME Configuration" -SocialIdSignIn $false
  ```

    <span data-ttu-id="bf1ad-121">공유 Id 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="bf1ad-121">To enable social IDs:</span></span>
    
  ```
  Set-OMEConfiguration -Identity "OME Configuration" -SocialIdSignIn $true
  ```

## <a name="managing-the-use-of-one-time-pass-codes-for-signing-in-to-the-office-365-message-encryption-portal"></a><span data-ttu-id="bf1ad-122">1 회 암호가 사용 하 여 Office 365 메시지 암호화 포털에 로그인 하는 것에 대 한 관리</span><span class="sxs-lookup"><span data-stu-id="bf1ad-122">Managing the use of one-time pass codes for signing in to the Office 365 Message Encryption portal</span></span>
<span data-ttu-id="bf1ad-123"><a name="GenerateOTPC"> </a></span><span class="sxs-lookup"><span data-stu-id="bf1ad-123"></span></span>

<span data-ttu-id="bf1ad-p105">기본적으로 OME 하 여 암호화 된 메시지의 받는 사람으로 받는 사람을 사용 하는 계정에 관계 없이 Outlook을 사용 하지 않는 경우 받는 메시지를 읽을 수 있도록 하는 제한 된 기간 동안 웹 보기 링크를 받습니다. 1 회 암호가 포함 됩니다. 관리자로 서 1 회 암호가 OME 포털에 로그인을 사용할 수 있는지 여부를 관리할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bf1ad-p105">By default, if the recipient of a message encrypted by OME doesn't use Outlook, regardless of the account used by the recipient, the recipient receives a limited-time web-view link that lets them read the message. This includes a one-time pass code. As an administrator, you can manage whether or not one-time pass codes can be used to sign-in to the OME portal.</span></span>
  
 <span data-ttu-id="bf1ad-127">**1 회 암호가 OME에 대해 생성 되는 여부를 관리 하려면**</span><span class="sxs-lookup"><span data-stu-id="bf1ad-127">**To manage whether or not one-time pass codes are generated for OME**</span></span>
  
1. <span data-ttu-id="bf1ad-128">[원격 PowerShell을 사용 하 여 온라인 Exchange에 연결](http://technet.microsoft.com/library/jj984289%28v=exchg.150%29.aspx)합니다.</span><span class="sxs-lookup"><span data-stu-id="bf1ad-128">[Connect to Exchange Online Using Remote PowerShell](http://technet.microsoft.com/library/jj984289%28v=exchg.150%29.aspx).</span></span>
    
2. <span data-ttu-id="bf1ad-129">다음과 같이 OTPEnabled 매개 변수와 함께 Set-omeconfiguration cmdlet를 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="bf1ad-129">Run the Set-OMEConfiguration cmdlet with the OTPEnabled parameter as follows:</span></span>
    
  ```
  Set-OMEConfiguration -Identity <"OMEConfigurationIdParameter "> -OTPEnabled <$true |$false >
  ```

    <span data-ttu-id="bf1ad-130">예: 일회용 암호 코드를 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bf1ad-130">For example, to disable one-time pass codes:</span></span>
    
  ```
  Set-OMEConfiguration -Identity "OME Configuration" -OTPEnabled $false
  ```

    <span data-ttu-id="bf1ad-131">1 회 암호가 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="bf1ad-131">To enable one-time pass codes:</span></span>
    
  ```
  Set-OMEConfiguration -Identity "OME Configuration" -OTPEnabled $true
  ```

## <a name="managing-the-display-of-the-protect-button-in-outlook-on-the-web"></a><span data-ttu-id="bf1ad-132">웹에 있는 Outlook에서 암호로 보호 단추를 표시 하는 관리</span><span class="sxs-lookup"><span data-stu-id="bf1ad-132">Managing the display of the Protect button in Outlook on the web</span></span>
<span data-ttu-id="bf1ad-133"><a name="DisplayProtectButton"> </a></span><span class="sxs-lookup"><span data-stu-id="bf1ad-133"></span></span>

<span data-ttu-id="bf1ad-p106">기본적으로 웹에 있는 Outlook에서 **암호로 보호** 단추는 사용할 수 없는 OME를 설정 하는 경우. 관리자로 서 최종 사용자에 게이 단추를 표시할 것인지 여부를 관리할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bf1ad-p106">By default, the **Protect** button in Outlook on the web is not enabled when you set up OME. As an administrator, you can manage whether or not to display this button to end users.</span></span> 
  
 <span data-ttu-id="bf1ad-136">**관리 여부는 Protect 단추 표시 하는 Outlook에서 웹에**</span><span class="sxs-lookup"><span data-stu-id="bf1ad-136">**To manage whether or not the Protect button appears in Outlook on the web**</span></span>
  
1. <span data-ttu-id="bf1ad-137">[원격 PowerShell을 사용 하 여 온라인 Exchange에 연결](http://technet.microsoft.com/library/jj984289%28v=exchg.150%29.aspx)합니다.</span><span class="sxs-lookup"><span data-stu-id="bf1ad-137">[Connect to Exchange Online Using Remote PowerShell](http://technet.microsoft.com/library/jj984289%28v=exchg.150%29.aspx).</span></span>
    
2. <span data-ttu-id="bf1ad-138">다음과 같이-SimplifiedClientAccessEnabled 매개 변수와 함께 Set-irmconfiguration cmdlet를 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="bf1ad-138">Run the Set-IRMConfiguration cmdlet with the -SimplifiedClientAccessEnabled parameter as follows:</span></span>
    
  ```
  Set-IRMConfiguration -SimplifiedClientAccessEnabled <$true |$false >
  ```

    <span data-ttu-id="bf1ad-139">예: **Protect** 단추를 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bf1ad-139">For example, to disable the **Protect** button:</span></span> 
    
  ```
  Set-IRMConfiguration -SimplifiedClientAccessEnabled $false
  ```

    <span data-ttu-id="bf1ad-140">단추를 사용 하도록 **암호로 보호** :</span><span class="sxs-lookup"><span data-stu-id="bf1ad-140">To enable the **Protect** button:</span></span> 
    
  ```
  Set-IRMConfiguration -SimplifiedClientAccessEnabled $true
  ```

## <a name="enable-service-side-decryption-of-email-messages-for-ios-mail-app-users"></a><span data-ttu-id="bf1ad-141">IOS 메일 앱 사용자에 대 한 전자 메일 메시지의 서비스 측 암호 해독을 사용 하도록 설정</span><span class="sxs-lookup"><span data-stu-id="bf1ad-141">Enable service-side decryption of email messages for iOS mail app users</span></span>
<span data-ttu-id="bf1ad-142"><a name="EnableServiceSideDecrypt"> </a></span><span class="sxs-lookup"><span data-stu-id="bf1ad-142"></span></span>

<span data-ttu-id="bf1ad-p107">IOS 메일 앱 Office 365 메시지 암호화로 보호 되는 메시지를 해독할 수 없습니다. Office 365 관리자로 iOS 메일 앱에 전달 된 메시지에 대 한 서비스 측 암호 해독을 적용할 수 있습니다. 이 작업을 수행 하려는 경우 서비스는 iOS 장치에 메시지의 암호가 해독 된 복사본을 보냅니다. 메시지는 클라이언트 장치에서 암호를 해독 저장 됩니다. 또한 메시지 iOS 메일 앱 클라이언트쪽 사용 권한을 사용자에 게는 적용 되지 않습니다 하는 경우에 사용 권한에 대 한 정보를 유지 합니다. 즉, 사용자가 복사 하거나 그렇게 권한을 원래가지고 있지 않은 경우에 메시지를 인쇄할 수 있습니다. 그러나 사용자가 Office 365 메일 서버는 메시지를 전달 하는 예: 필요한 작업을 완료 하려고 하는 경우 서버는 허용 하지 작업 사용자가 원래 그렇게 수 있는 사용 권한이 없는 경우. 그러나 최종 사용자를 해결할 수 제한 사항 전달 하지 않음 메일의 서비스 측 암호 해독을 설정 하는 여부에 관계 없이 자신의 iOS 메일 응용 프로그램의 다른 계정에서 메시지를 전달 하 여, 모든 첨부 파일을 암호화 및 권한 메일 보호 iOS 메일 응용 프로그램에서 볼 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="bf1ad-p107">The iOS mail app can't decrypt messages protected with Office 365 Message Encryption. As an Office 365 administrator, you can apply service-side decryption for messages delivered to the iOS mail app. When you choose to do this, the service sends a decrypted copy of the message to the iOS device. The message is stored decrypted on the client device. The message also retains information about usage rights even though the iOS mail app doesn't apply client-side usage rights to the user. This means that the user can copy or print the message even if they did not originally have the rights to do so. However, if the user attempts to complete an action that requires the Office 365 mail server, such as forwarding the message, the server will not permit the action if the user did not originally have the usage right to do so. However, end-users can work around Do Not Forward usage restriction by forwarding the message from a different account in their iOS mail app. Regardless of whether you set up service-side decryption of mail, any attachments to encrypted and rights protected mail cannot be viewed in the iOS mail app.</span></span>
  
<span data-ttu-id="bf1ad-p108">해독 된 메시지를 보낼 수를 허용 하지 않도록 선택 하는 경우 iOS 메일 앱 사용자, 사용자가 메시지를 볼 수 있는 권한이 없더라도 없다는 메시지를 수신 합니다. 기본적으로 전자 메일 메시지의 서비스 측 암호 해독을 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="bf1ad-p108">If you choose not to allow decrypted messages to be sent to iOS mail app users, users receive a message that states that they don't have the rights to view the message. By default, service-side decryption of email messages is not enabled.</span></span>
  
<span data-ttu-id="bf1ad-154">자세한 내용 및 클라이언트 환경에서의 보기에는 "[iPhone 또는 iPad에서 암호화 된 메시지를 보려면](https://support.office.com/article/4d631321-0d26-4bcc-a483-d294dd0b1caf#iOSEncryptedMail)" [iPhone 또는 iPad에서 암호화 된 메시지 보기](https://support.office.com/article/4d631321-0d26-4bcc-a483-d294dd0b1caf)에서 섹션을 참조 합니다.</span><span class="sxs-lookup"><span data-stu-id="bf1ad-154">For more information, and for a view of the client experience, see the section, "[View encrypted messages on your iPhone or iPad](https://support.office.com/article/4d631321-0d26-4bcc-a483-d294dd0b1caf#iOSEncryptedMail)" in [View encrypted messages on your iPhone or iPad](https://support.office.com/article/4d631321-0d26-4bcc-a483-d294dd0b1caf).</span></span>
  
 <span data-ttu-id="bf1ad-155">**IOS 메일 앱 사용자 여부를 관리 하려면 Office 365 메시지 암호화로 보호 된 메시지를 볼 수 있습니다.**</span><span class="sxs-lookup"><span data-stu-id="bf1ad-155">**To manage whether or not iOS mail app users can view messages protected by Office 365 Message Encryption**</span></span>
  
1. <span data-ttu-id="bf1ad-156">[원격 PowerShell을 사용 하 여 온라인 Exchange에 연결](http://technet.microsoft.com/library/jj984289%28v=exchg.150%29.aspx)합니다.</span><span class="sxs-lookup"><span data-stu-id="bf1ad-156">[Connect to Exchange Online Using Remote PowerShell](http://technet.microsoft.com/library/jj984289%28v=exchg.150%29.aspx).</span></span>
    
2. <span data-ttu-id="bf1ad-157">다음과 같이 AllowRMSSupportForUnenlightenedApps 매개 변수와 함께 집합 ActiveSyncOrganizations cmdlet를 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="bf1ad-157">Run the Set-ActiveSyncOrganizations cmdlet with the AllowRMSSupportForUnenlightenedApps parameter as follows:</span></span>
    
  ```
  Set-ActiveSyncOrganizationSettings -AllowRMSSupportForUnenlightenedApps <$true |$false >
  ```

    <span data-ttu-id="bf1ad-158">등 unenlightened 앱에 보낸 메시지의 암호 해독에 서비스를 구성 하려면 다음과 같이 iOS 메일 앱:</span><span class="sxs-lookup"><span data-stu-id="bf1ad-158">For example, to configure the service to decrypt messages before they are sent to unenlightened apps such as the iOS mail app:</span></span>
    
  ```
  Set-ActiveSyncOrganizationSettings -AllowRMSSupportForUnenlightenedApps $true
  ```

    <span data-ttu-id="bf1ad-159">예: unenlightened 응용 프로그램을 암호가 해독 된 메시지를 보내지 서비스를 구성 하려면:</span><span class="sxs-lookup"><span data-stu-id="bf1ad-159">For example, to configure the service not to send decrypted messages to unenlightened apps:</span></span>
    
  ```
  Set-ActiveSyncOrganizationSettings -AllowRMSSupportForUnenlightenedApps $false
  ```

## <a name="enable-service-side-decryption-of-email-attachments-for-web-browser-mail-clients"></a><span data-ttu-id="bf1ad-160">웹 브라우저 메일 클라이언트에 대 한 전자 메일 첨부 파일의 서비스 측 암호 해독을 사용 하도록 설정</span><span class="sxs-lookup"><span data-stu-id="bf1ad-160">Enable service-side decryption of email attachments for web browser mail clients</span></span>
<span data-ttu-id="bf1ad-161"><a name="EnableServiceSideDecrypt"> </a></span><span class="sxs-lookup"><span data-stu-id="bf1ad-161"></span></span>

<span data-ttu-id="bf1ad-p109">일반적으로 Office 365 메시지 암호화를 사용 하면 첨부 파일 자동으로 암호화 됩니다. Office 365 관리자 권한으로 사용자가 웹 브라우저에서 다운로드 하는 전자 메일 첨부 파일에 대 한 서비스 측 암호 해독을 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bf1ad-p109">Normally, when you use Office 365 message encryption, attachments are automatically encrypted. As an Office 365 administrator, you can apply service-side decryption for email attachments that users download from a web browser.</span></span> 
  
<span data-ttu-id="bf1ad-p110">이 작업을 수행 하려는 경우 서비스는 장치에 파일의 암호가 해독 된 복사본을 보냅니다. 메시지는 여전히 암호화 됩니다. 또한 전자 메일 첨부 파일 브라우저 클라이언트쪽 사용 권한을 사용자에 게는 적용 되지 않습니다 하는 경우에 사용 권한에 대 한 정보를 유지 합니다. 즉, 사용자가 복사 하거나 그렇게 권한을 원래가지고 있지 않은 경우에 전자 메일 첨부 파일을 인쇄할 수 있습니다. 그러나 사용자가 첨부 파일을 전달 하는 등의 Office 365 메일 서버를 필요로 하는 작업을 완료 하려고 하는 경우 서버는 허용 하지 작업 사용자가 원래 그렇게 수 있는 사용 권한이 없는 경우.</span><span class="sxs-lookup"><span data-stu-id="bf1ad-p110">When you choose to do this, the service sends a decrypted copy of the file to the device. The message is still encrypted. The email attachment also retains information about usage rights even though the browser does not apply client-side usage rights to the user. This means that the user can copy or print the email attachment even if they did not originally have the rights to do so. However, if the user attempts to complete an action that requires the Office 365 mail server, such as forwarding the attachment, the server will not permit the action if the user did not originally have the usage right to do so.</span></span>
  
<span data-ttu-id="bf1ad-169">첨부 파일의 서비스 측 암호 해독 설정 여부에 관계 없이 모든 첨부 파일을 암호화 하 고 iOS 메일 앱의 권한 제한 된 메일을 볼 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="bf1ad-169">Regardless of whether you set up service-side decryption of attachments, any attachments to encrypted and rights protected mail cannot be viewed in the iOS mail app.</span></span>
  
<span data-ttu-id="bf1ad-p111">기본 인 암호가 해독 된 전자 메일 첨부 파일을 허용 하지 않도록 선택 하는 경우 사용자가 첨부 파일을 볼 수 있는 권한이 없더라도 없다는 메시지를 수신 합니다. \* \* \* 그림을 삽입?</span><span class="sxs-lookup"><span data-stu-id="bf1ad-p111">If you choose not to allow decrypted email attachments, which is the default, users receive a message that states that they don't have the rights to view the attachment. \*\*\* insert picture?</span></span>
  
<span data-ttu-id="bf1ad-172">Office 365에서 전자 메일 및 전자 메일 첨부 파일 암호화 전용 옵션에 대 한 암호화를 구현 하는 방법에 대 한 자세한 내용은 참조 [전자 메일에 대 한 암호화 전용 옵션.](https://docs.microsoft.com/azure/information-protection/deploy-use/configure-usage-rights#encrypt-only-option-for-emails)</span><span class="sxs-lookup"><span data-stu-id="bf1ad-172">For more information about how Office 365 implements encryption for emails and email attachments with the Encrypt-Only option, see [Encrypt-Only option for emails.](https://docs.microsoft.com/azure/information-protection/deploy-use/configure-usage-rights#encrypt-only-option-for-emails)</span></span>
  
 <span data-ttu-id="bf1ad-173">**관리 여부 전자 메일 첨부 파일의 암호 해독에 웹 브라우저에서 다운로드**</span><span class="sxs-lookup"><span data-stu-id="bf1ad-173">**To manage whether or not email attachments are decrypted on download from a web browser**</span></span>
  
1. <span data-ttu-id="bf1ad-174">[원격 PowerShell을 사용 하 여 온라인 Exchange에 연결](http://technet.microsoft.com/library/jj984289%28v=exchg.150%29.aspx)합니다.</span><span class="sxs-lookup"><span data-stu-id="bf1ad-174">[Connect to Exchange Online Using Remote PowerShell](http://technet.microsoft.com/library/jj984289%28v=exchg.150%29.aspx).</span></span>
    
2. <span data-ttu-id="bf1ad-175">다음과 같이 DecryptAttachmentFromPortal 매개 변수와 함께 Set-irmconfiguration cmdlet를 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="bf1ad-175">Run the Set-IRMConfiguration cmdlet with the DecryptAttachmentFromPortal parameter as follows:</span></span>
    
  ```
  Set-IRMConfiguration -DecryptAttachmentFromPortal <$true |$false >
  ```

    <span data-ttu-id="bf1ad-176">예 때 사용자의 전자 메일 첨부 파일의 암호를 해독 하는 서비스를 구성 하려면을 다운로드 하는 웹 브라우저에서:</span><span class="sxs-lookup"><span data-stu-id="bf1ad-176">For example, to configure the service to decrypt email attachments when a user downloads them from a web browser:</span></span>
    
  ```
  Set-IRMConfiguration -DecryptAttachmentFromPortal $true
  ```

    <span data-ttu-id="bf1ad-177">서비스를 구성 하려면 다운로드 시로 암호화 된 전자 메일 첨부 파일을 유지 하도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="bf1ad-177">To configure the service to leave encrypted email attachments as they are upon download:</span></span>
    
  ```
  Set-IRMConfiguration -DecryptAttachmentFromPortal $false
  ```

## <a name="customizing-the-appearance-of-email-messages-and-the-ome-portal"></a><span data-ttu-id="bf1ad-178">전자 메일 메시지와 OME 포털의 모양을 사용자 지정</span><span class="sxs-lookup"><span data-stu-id="bf1ad-178">Customizing the appearance of email messages and the OME portal</span></span>
<span data-ttu-id="bf1ad-179"><a name="CustomizeAppearance"> </a></span><span class="sxs-lookup"><span data-stu-id="bf1ad-179"></span></span>

<span data-ttu-id="bf1ad-180">조직에 대 한 OME를 사용자 지정할 수는 방법에 대 한 자세한 내용은 [조직의 브랜드를 암호화 된 메시지에 추가](add-your-organization-brand-to-encrypted-messages.md)참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="bf1ad-180">For detailed information about how you can customize OME for your organization, see [Add your organization's brand to your encrypted messages](add-your-organization-brand-to-encrypted-messages.md).</span></span>
  
## <a name="disabling-the-new-capabilities-for-ome"></a><span data-ttu-id="bf1ad-181">OME에 대 한 새로운 기능을 사용 하지 않도록 설정</span><span class="sxs-lookup"><span data-stu-id="bf1ad-181">Disabling the new capabilities for OME</span></span>
<span data-ttu-id="bf1ad-182"><a name="CustomizeAppearance"> </a></span><span class="sxs-lookup"><span data-stu-id="bf1ad-182"></span></span>

<span data-ttu-id="bf1ad-p112">바랍니다 하는 경우 필요한, 작업은 매우 간단 OME에 대 한 새로운 기능을 사용 하지 않도록 설정 하지만,를 제공 하지 않습니다. 첫째, 규칙을 제거 하려면 모든 메일 흐름 만들었고 새 OME 기능을 사용 하는 필요 합니다. 메일 흐름 규칙을 제거 하는 방법에 대 한 정보, [메일 흐름 규칙 관리를](https://technet.microsoft.com/library/jj657505%28v=exchg.150%29.aspx)참조 하십시오. 그런 다음, 다음이 단계를 완료 Exchange 온라인 PowerShell 합니다.</span><span class="sxs-lookup"><span data-stu-id="bf1ad-p112">We hope it doesn't come to it, but if you need to, disabling the new capabilities for OME is very straightforward. First, you'll need to remove any mail flow rules you've created that use the new OME capabilities. For information about removing mail flow rules, see [Manage mail flow rules](https://technet.microsoft.com/library/jj657505%28v=exchg.150%29.aspx). Then, complete these steps in Exchange Online PowerShell.</span></span>
  
 <span data-ttu-id="bf1ad-187">**OME에 대 한 새로운 기능을 사용 하지 않도록 설정 하려면**</span><span class="sxs-lookup"><span data-stu-id="bf1ad-187">**To disable the new capabilities for OME**</span></span>
  
1. <span data-ttu-id="bf1ad-188">[원격 PowerShell을 사용 하 여 온라인 Exchange에 연결](https://technet.microsoft.com/library/jj984289%28v=exchg.160%29.aspx)합니다.</span><span class="sxs-lookup"><span data-stu-id="bf1ad-188">[Connect to Exchange Online Using Remote PowerShell](https://technet.microsoft.com/library/jj984289%28v=exchg.160%29.aspx).</span></span>
    
2. <span data-ttu-id="bf1ad-189">웹에 있는 Outlook에서 암호로 보호 단추를 사용 하도록 설정한 경우 다음과 같이 SimplifiedClientAccessEnabled 매개 변수와 함께 Set-irmconfiguration cmdlet을 실행 하 여 해제 합니다.</span><span class="sxs-lookup"><span data-stu-id="bf1ad-189">If you enabled the Protect button in Outlook on the web, disable it by running the Set-IRMConfiguration cmdlet with the SimplifiedClientAccessEnabled parameter as follows:</span></span>
    
  ```
  Set-IRMConfiguration -SimplifiedClientAccessEnabled $false
  ```

3. <span data-ttu-id="bf1ad-190">다음과 같이 AzureRMSLicensingEnabled 매개 변수와 함께 Set-irmconfiguration cmdlet를 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="bf1ad-190">Run the Set-IRMConfiguration cmdlet with the AzureRMSLicensingEnabled parameter as follows:</span></span>
    
  ```
  Set-IRMConfiguration -AzureRMSLicensingEnabled $false
  ```


