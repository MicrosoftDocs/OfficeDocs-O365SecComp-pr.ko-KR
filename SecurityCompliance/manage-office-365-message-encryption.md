---
title: Office 365 메시지 암호화 관리
ms.author: krowley
author: kccross
manager: laurawi
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.date: 5/8/2019
search.appverid:
- MET150
ms.assetid: 09f6737e-f03f-4bc8-8281-e46d24ee2a74
ms.collection:
- Strat_O365_IP
- M365-security-compliance
description: Office 365 메시지 암호화 (OME) 설정을 완료 한 후에는 여러 가지 방법으로 배포 구성을 사용자 지정할 수 있습니다. 예를 들어, 웹의 Outlook에서 1 회 통과, 보호 단추를 표시할 것인지 여부를 구성할 수 있습니다. 이 문서의 작업에서는 이러한 방법을 설명 합니다.
ms.openlocfilehash: f19556f88783eed86bd33a7fdcbd1efae18c3ef3
ms.sourcegitcommit: b9d8a43cb3afcdc8820bc9470c5707eff8fc6616
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/11/2019
ms.locfileid: "34852532"
---
# <a name="manage-office-365-message-encryption"></a><span data-ttu-id="49869-105">Office 365 메시지 암호화 관리</span><span class="sxs-lookup"><span data-stu-id="49869-105">Manage Office 365 Message Encryption</span></span>

<span data-ttu-id="49869-106">Office 365 메시지 암호화 (OME) 설정을 완료 한 후에는 여러 가지 방법으로 배포 구성을 사용자 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="49869-106">Once you've finished setting up Office 365 Message Encryption (OME), you can customize the configuration of your deployment in several ways.</span></span> <span data-ttu-id="49869-107">예를 들어, 웹의 Outlook에서 1 회 통과, **암호화** 단추를 표시할 것인지 여부를 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="49869-107">For example, you can configure whether to enable one-time pass codes, display the **Encrypt** button in Outlook on the web, and more.</span></span> <span data-ttu-id="49869-108">이 문서의 작업에서는 이러한 방법을 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="49869-108">The tasks in this article describe how.</span></span>

## <a name="manage-whether-google-yahoo-and-microsoft-account-recipients-can-use-these-accounts-to-sign-in-to-the-office-365-message-encryption-portal"></a><span data-ttu-id="49869-109">Google, Yahoo 및 Microsoft 계정 받는 사람이 이러한 계정을 사용 하 여 Office 365 메시지 암호화 포털에 로그인 할 수 있는지 여부를 관리 합니다.</span><span class="sxs-lookup"><span data-stu-id="49869-109">Manage whether Google, Yahoo, and Microsoft Account recipients can use these accounts to sign in to the Office 365 Message Encryption portal</span></span>

<span data-ttu-id="49869-110">새 Office 365 메시지 암호화 기능을 설정 하면 조직의 사용자가 Office 365 조직 외부에 있는 받는 사람에 게 메시지를 보낼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="49869-110">When you set up the new Office 365 Message Encryption capabilities, users in your organization can send messages to recipients that are outside of your Office 365 organization.</span></span> <span data-ttu-id="49869-111">받는 사람이 Google 계정, Yahoo account 또는 Microsoft 계정과 같은 *공유 id* 를 사용 하는 경우 받는 사람은 공유 ID로 OME 포털에 로그인 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="49869-111">If the recipient uses a *social ID* such as a Google account, Yahoo account, or Microsoft account, the recipient can sign in to the OME portal with a social ID.</span></span> <span data-ttu-id="49869-112">원하는 경우 받는 사람이 공유 Id를 사용 하 여 OME 포털에 로그인 하는 것을 허용 하지 않도록 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="49869-112">If you want, you can choose not to allow recipients to use social IDs to sign in to the OME portal.</span></span>
  
### <a name="to-manage-whether-recipients-can-use-social-ids-to-sign-in-to-the-ome-portal"></a><span data-ttu-id="49869-113">받는 사람이 공유 Id를 사용 하 여 OME 포털에 로그인 할 수 있는지 여부를 관리 하려면</span><span class="sxs-lookup"><span data-stu-id="49869-113">To manage whether recipients can use social IDs to sign in to the OME portal</span></span>
  
1. <span data-ttu-id="49869-114">[원격 PowerShell을 사용 하 여 Exchange Online에 연결](http://technet.microsoft.com/library/jj984289%28v=exchg.150%29.aspx)합니다.</span><span class="sxs-lookup"><span data-stu-id="49869-114">[Connect to Exchange Online Using Remote PowerShell](http://technet.microsoft.com/library/jj984289%28v=exchg.150%29.aspx).</span></span>

2. <span data-ttu-id="49869-115">다음과 같이, Set-omeconfiguration cmdlet을 사회 Alidsignin 매개 변수를 사용 하 여 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="49869-115">Run the Set-OMEConfiguration cmdlet with the SocialIdSignIn parameter as follows:</span></span>

   ```powershell
   Set-OMEConfiguration -Identity <"OMEConfigurationIdParameter"> -SocialIdSignIn <$true|$false>
   ```

   <span data-ttu-id="49869-116">예를 들어, 공유 Id를 사용 하지 않도록 설정 하려면</span><span class="sxs-lookup"><span data-stu-id="49869-116">For example, to disable social IDs:</span></span>

   ```powershell
   Set-OMEConfiguration -Identity "OME Configuration" -SocialIdSignIn $false
   ```

   <span data-ttu-id="49869-117">공유 Id를 사용 하도록 설정 하려면:</span><span class="sxs-lookup"><span data-stu-id="49869-117">To enable social IDs:</span></span>

   ```powershell
   Set-OMEConfiguration -Identity "OME Configuration" -SocialIdSignIn $true
   ```

## <a name="manage-the-use-of-one-time-pass-codes-for-the-office-365-message-encryption-portal"></a><span data-ttu-id="49869-118">Office 365 메시지 암호화 포털에 대해 1 회 통과 코드 사용 관리</span><span class="sxs-lookup"><span data-stu-id="49869-118">Manage the use of one-time pass codes for the Office 365 Message Encryption portal</span></span>

<span data-ttu-id="49869-119">받는 사람이 사용 하는 계정에 관계 없이 OME에서 암호화 된 메시지를 받는 사람이 Outlook을 사용 하지 않는 경우에는 받는 사람에 게 메시지를 읽을 수 있는 제한 된 웹 보기 링크가 수신 됩니다.</span><span class="sxs-lookup"><span data-stu-id="49869-119">If the recipient of a message encrypted by OME doesn't use Outlook, regardless of the account used by the recipient, the recipient receives a limited-time web-view link that lets them read the message.</span></span> <span data-ttu-id="49869-120">이 링크에는 1 회 통과 코드가 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="49869-120">This link includes a one-time pass code.</span></span> <span data-ttu-id="49869-121">관리자는 받는 사람이 1 회 통과 코드를 사용 하 여 OME 포털에 로그인 할 수 있는지 결정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="49869-121">As an administrator, you can decide if recipients can use one-time pass codes to sign in to the OME portal.</span></span>
  
### <a name="to-manage-whether-ome-generates-one-time-pass-codes"></a><span data-ttu-id="49869-122">OME에서 1 회 통과 코드를 생성할지 여부를 관리 하려면</span><span class="sxs-lookup"><span data-stu-id="49869-122">To manage whether OME generates one-time pass codes</span></span>
  
1. <span data-ttu-id="49869-123">Office 365 조직에서 전역 관리자 권한이 있는 회사 또는 학교 계정을 사용 하 고, Windows PowerShell 세션을 시작 하 고, Exchange Online에 연결 합니다.</span><span class="sxs-lookup"><span data-stu-id="49869-123">Use a work or school account that has global administrator permissions in your Office 365 organization and start a Windows PowerShell session and connect to Exchange Online.</span></span> <span data-ttu-id="49869-124">자세한 내용은 [Exchange Online PowerShell에 연결을](https://aka.ms/exopowershell)참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="49869-124">For instructions, see [Connect to Exchange Online PowerShell](https://aka.ms/exopowershell).</span></span>

2. <span data-ttu-id="49869-125">OTPEnabled 매개 변수를 사용 하 여 Set-omeconfiguration cmdlet을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="49869-125">Run the Set-OMEConfiguration cmdlet with the OTPEnabled parameter:</span></span>

   ```powershell
   Set-OMEConfiguration -Identity <"OMEConfigurationIdParameter "> -OTPEnabled <$true|$false>
   ```

   <span data-ttu-id="49869-126">예를 들어, 1 회 통과 코드를 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="49869-126">For example, to disable one-time pass codes:</span></span>

   ```powershell
   Set-OMEConfiguration -Identity "OME Configuration" -OTPEnabled $false
   ```

   <span data-ttu-id="49869-127">1 회 통과 코드를 사용 하도록 설정 하려면:</span><span class="sxs-lookup"><span data-stu-id="49869-127">To enable one-time pass codes:</span></span>

   ```powershell
   Set-OMEConfiguration -Identity "OME Configuration" -OTPEnabled $true
   ```

## <a name="manage-the-display-of-the-encrypt-button-in-outlook-on-the-web"></a><span data-ttu-id="49869-128">웹용 Outlook에서 암호화 단추 표시 관리</span><span class="sxs-lookup"><span data-stu-id="49869-128">Manage the display of the Encrypt button in Outlook on the web</span></span>

<span data-ttu-id="49869-129">관리자는이 단추를 최종 사용자에 게 표시할지 여부를 관리할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="49869-129">As an administrator, you can manage whether to display this button to end users.</span></span>
  
### <a name="to-manage-whether-the-encrypt-button-appears-in-outlook-on-the-web"></a><span data-ttu-id="49869-130">웹에서 Outlook에 암호화 단추를 표시할지 여부를 관리 하려면</span><span class="sxs-lookup"><span data-stu-id="49869-130">To manage whether the Encrypt button appears in Outlook on the web</span></span>
  
1. <span data-ttu-id="49869-131">Office 365 조직에서 전역 관리자 권한이 있는 회사 또는 학교 계정을 사용 하 고, Windows PowerShell 세션을 시작 하 고, Exchange Online에 연결 합니다.</span><span class="sxs-lookup"><span data-stu-id="49869-131">Use a work or school account that has global administrator permissions in your Office 365 organization and start a Windows PowerShell session and connect to Exchange Online.</span></span> <span data-ttu-id="49869-132">자세한 내용은 [Exchange Online PowerShell에 연결을](https://aka.ms/exopowershell)참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="49869-132">For instructions, see [Connect to Exchange Online PowerShell](https://aka.ms/exopowershell).</span></span>

2. <span data-ttu-id="49869-133">-SimplifiedClientAccessEnabled 매개 변수를 사용 하 여 IRMConfiguration cmdlet을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="49869-133">Run the Set-IRMConfiguration cmdlet with the -SimplifiedClientAccessEnabled parameter:</span></span>

   ```powershell
   Set-IRMConfiguration -SimplifiedClientAccessEnabled <$true|$false>
   ```

   <span data-ttu-id="49869-134">예를 들어 **암호화** 단추를 사용 하지 않도록 설정 하려면 다음을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="49869-134">For example, to disable the **Encrypt** button:</span></span>

   ```powershell
   Set-IRMConfiguration -SimplifiedClientAccessEnabled $false
   ```

   <span data-ttu-id="49869-135">**암호화** 단추를 사용 하도록 설정 하려면:</span><span class="sxs-lookup"><span data-stu-id="49869-135">To enable the **Encrypt** button:</span></span>

   ```powershell
   Set-IRMConfiguration -SimplifiedClientAccessEnabled $true
   ```

## <a name="enable-service-side-decryption-of-email-messages-for-ios-mail-app-users"></a><span data-ttu-id="49869-136">IOS 메일 앱 사용자에 대 한 전자 메일 메시지의 서비스 쪽 암호 해독을 사용 하도록 설정</span><span class="sxs-lookup"><span data-stu-id="49869-136">Enable service-side decryption of email messages for iOS mail app users</span></span>

<span data-ttu-id="49869-137">IOS 메일 앱은 Office 365 메시지 암호화로 보호 된 메시지의 암호를 해독할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="49869-137">The iOS mail app can't decrypt messages protected with Office 365 Message Encryption.</span></span> <span data-ttu-id="49869-138">Office 365 관리자는 iOS 메일 앱으로 배달 되는 메시지에 대해 서비스 쪽 암호 해독을 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="49869-138">As an Office 365 administrator, you can apply service-side decryption for messages delivered to the iOS mail app.</span></span> <span data-ttu-id="49869-139">서비스 쪽 암호 해독을 사용 하도록 선택 하면 서비스에서 암호 해독 된 메시지 복사본을 iOS 장치로 보냅니다.</span><span class="sxs-lookup"><span data-stu-id="49869-139">When you choose to do use service-side decryption, the service sends a decrypted copy of the message to the iOS device.</span></span> <span data-ttu-id="49869-140">클라이언트 장치는 암호 해독 된 메시지의 복사본을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="49869-140">The client device stores a decrypted copy of the message.</span></span> <span data-ttu-id="49869-141">또한 iOS 메일 앱이 사용자에 게 클라이언트 쪽 사용 권한을 적용 하지 않더라도 사용 권한에 대 한 정보도 유지 됩니다.</span><span class="sxs-lookup"><span data-stu-id="49869-141">The message also retains information about usage rights even though the iOS mail app doesn't apply client-side usage rights to the user.</span></span> <span data-ttu-id="49869-142">사용자는 원래 해당 권한이 없는 경우에도 메시지를 복사 하거나 인쇄할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="49869-142">The user can copy or print the message even if they didn't originally have the rights to do so.</span></span> <span data-ttu-id="49869-143">그러나 사용자가 메시지 전달 등의 Office 365 메일 서버가 필요한 작업을 완료 하려고 하면 사용자가 원래 사용 권한을 갖고 있지 않은 경우 서버에서 해당 작업을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="49869-143">However, if the user attempts to complete an action that requires the Office 365 mail server, such as forwarding the message, the server won't permit the action if the user didn't originally have the usage right to do so.</span></span> <span data-ttu-id="49869-144">그러나 최종 사용자는 iOS 메일 응용 프로그램 내에서 다른 계정 으로부터 메시지를 전달 하 여 "전달 금지" 사용 제한을 해결할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="49869-144">However, end users can work around "Do Not Forward" usage restriction by forwarding the message from a different account within the iOS mail app.</span></span> <span data-ttu-id="49869-145">메일에 대 한 서비스 쪽 암호 해독을 설정 하는지 여부에 관계 없이 암호화 및 권한으로 보호 되는 전자 메일의 첨부 파일은 iOS 메일 앱에서 볼 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="49869-145">Regardless of whether you set up service-side decryption of mail, attachments to encrypted and rights protected mail can't be viewed in the iOS mail app.</span></span>
  
<span data-ttu-id="49869-146">암호 해독 된 메시지를 iOS 메일 앱 사용자에 게 보내도록 허용 하지 않도록 선택 하면 사용자에 게 메시지를 볼 수 있는 권한이 없다는 메시지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="49869-146">If you choose not to allow decrypted messages to be sent to iOS mail app users, users receive a message that states that they don't have the rights to view the message.</span></span> <span data-ttu-id="49869-147">기본적으로 전자 메일 메시지의 서비스 쪽 암호 해독이 사용 되도록 설정 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="49869-147">By default, service-side decryption of email messages is not enabled.</span></span>
  
<span data-ttu-id="49869-148">자세한 내용과 클라이언트 환경의 보기에 대 한 자세한 내용은 [iPhone 또는 iPad에서 암호화 된 메시지 보기](https://support.office.com/article/4d631321-0d26-4bcc-a483-d294dd0b1caf)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="49869-148">For more information, and for a view of the client experience, see [View encrypted messages on your iPhone or iPad](https://support.office.com/article/4d631321-0d26-4bcc-a483-d294dd0b1caf).</span></span>
  
### <a name="to-manage-whether-ios-mail-app-users-can-view-messages-protected-by-office-365-message-encryption"></a><span data-ttu-id="49869-149">IOS 메일 앱 사용자가 Office 365 메시지 암호화로 보호 된 메시지를 볼 수 있는지 여부를 관리 하려면</span><span class="sxs-lookup"><span data-stu-id="49869-149">To manage whether iOS mail app users can view messages protected by Office 365 Message Encryption</span></span>
  
1. <span data-ttu-id="49869-150">Office 365 조직에서 전역 관리자 권한이 있는 회사 또는 학교 계정을 사용 하 고, Windows PowerShell 세션을 시작 하 고, Exchange Online에 연결 합니다.</span><span class="sxs-lookup"><span data-stu-id="49869-150">Use a work or school account that has global administrator permissions in your Office 365 organization and start a Windows PowerShell session and connect to Exchange Online.</span></span> <span data-ttu-id="49869-151">자세한 내용은 [Exchange Online PowerShell에 연결을](https://aka.ms/exopowershell)참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="49869-151">For instructions, see [Connect to Exchange Online PowerShell](https://aka.ms/exopowershell).</span></span>

2. <span data-ttu-id="49869-152">AllowRMSSupportForUnenlightenedApps 매개 변수를 사용 하 여 ActiveSyncOrganizations cmdlet을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="49869-152">Run the Set-ActiveSyncOrganizations cmdlet with the AllowRMSSupportForUnenlightenedApps parameter:</span></span>

   ```powershell
   Set-ActiveSyncOrganizationSettings -AllowRMSSupportForUnenlightenedApps <$true|$false>
   ```

   <span data-ttu-id="49869-153">예를 들어 메시지가 iOS 메일 응용 프로그램과 같은 unenlightened 앱으로 전송 되기 전에 암호를 해독 하도록 서비스를 구성 하려면 다음을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="49869-153">For example, to configure the service to decrypt messages before they're sent to unenlightened apps like the iOS mail app:</span></span>

   ```powershell
   Set-ActiveSyncOrganizationSettings -AllowRMSSupportForUnenlightenedApps $true
   ```

   <span data-ttu-id="49869-154">또는 암호화 되지 않은 메시지를 unenlightened 앱으로 보내지 않도록 서비스를 구성 하려면 다음을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="49869-154">Or, to configure the service not to send decrypted messages to unenlightened apps:</span></span>

   ```powershell
   Set-ActiveSyncOrganizationSettings -AllowRMSSupportForUnenlightenedApps $false
   ```

## <a name="enable-service-side-decryption-of-email-attachments-for-web-browser-mail-clients"></a><span data-ttu-id="49869-155">웹 브라우저 메일 클라이언트에 대 한 전자 메일 첨부 파일의 서비스 쪽 암호 해독을 사용 하도록 설정</span><span class="sxs-lookup"><span data-stu-id="49869-155">Enable service-side decryption of email attachments for web browser mail clients</span></span>

<span data-ttu-id="49869-156">일반적으로 Office 365 메시지 암호화를 사용 하면 첨부 파일이 자동으로 암호화 됩니다.</span><span class="sxs-lookup"><span data-stu-id="49869-156">Normally, when you use Office 365 message encryption, attachments are automatically encrypted.</span></span> <span data-ttu-id="49869-157">Office 365 관리자는 사용자가 웹 브라우저에서 다운로드 하는 전자 메일 첨부 파일에 대해 서비스 쪽 암호 해독을 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="49869-157">As an Office 365 administrator, you can apply service-side decryption for email attachments that users download from a web browser.</span></span>
  
<span data-ttu-id="49869-158">서비스 쪽 암호 해독을 사용 하면 서비스에서 암호 해독 된 파일 복사본을 장치로 보냅니다.</span><span class="sxs-lookup"><span data-stu-id="49869-158">When you use service-side decryption, the service sends a decrypted copy of the file to the device.</span></span> <span data-ttu-id="49869-159">메시지가 계속 암호화 됩니다.</span><span class="sxs-lookup"><span data-stu-id="49869-159">The message is still encrypted.</span></span> <span data-ttu-id="49869-160">또한 브라우저가 클라이언트 쪽 사용 권한을 사용자에 게 적용 하지 않더라도 전자 메일 첨부 파일은 사용 권한에 대 한 정보를 유지 합니다.</span><span class="sxs-lookup"><span data-stu-id="49869-160">The email attachment also keeps information about usage rights even though the browser doesn't apply client-side usage rights to the user.</span></span> <span data-ttu-id="49869-161">사용자는 원래 사용 권한을 갖고 있지 않은 경우에도 전자 메일 첨부 파일을 복사 하거나 인쇄할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="49869-161">The user can copy or print the email attachment even if they didn't originally have the rights to do so.</span></span> <span data-ttu-id="49869-162">그러나 사용자가 Office 365 메일 서버가 필요한 작업 (예: 첨부 파일 전달)을 완료 하려고 하면 사용자가 원래 사용 권한을 갖고 있지 않은 경우 서버에서 해당 작업을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="49869-162">However, if the user tries to complete an action that requires the Office 365 mail server, such as forwarding the attachment, the server won't permit the action if the user didn't originally have the usage right to do so.</span></span>
  
<span data-ttu-id="49869-163">사용자가 첨부 파일에 대해 서비스 쪽 암호 해독을 설정 하는지 여부에 관계 없이 iOS 메일 응용 프로그램에서 암호화 및 권한으로 보호 된 메일의 첨부 파일을 볼 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="49869-163">Regardless of whether you set up service-side decryption of attachments, users can't view any attachments to encrypted and rights protected mail in the iOS mail app.</span></span>
  
<span data-ttu-id="49869-164">해독 된 전자 메일 첨부 파일 (기본값)을 허용 하지 않도록 선택 하면 사용자에 게 첨부 파일을 볼 수 있는 권한이 없다는 메시지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="49869-164">If you choose not to allow decrypted email attachments, which is the default, users receive a message that states that they don't have the rights to view the attachment.</span></span>
  
<span data-ttu-id="49869-165">Office 365에서 암호화 전용 옵션을 사용 하 여 전자 메일 첨부 파일에 대 한 암호화를 구현 하는 방법에 대 한 자세한 내용은 [전자 메일에 대 한 암호화 전용 옵션](https://docs.microsoft.com/azure/information-protection/deploy-use/configure-usage-rights#encrypt-only-option-for-emails) 을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="49869-165">For more information about how Office 365 implements encryption for emails and email attachments with the Encrypt-Only option, see [Encrypt-Only option for emails.](https://docs.microsoft.com/azure/information-protection/deploy-use/configure-usage-rights#encrypt-only-option-for-emails)</span></span>
  
### <a name="to-manage-whether-email-attachments-are-decrypted-on-download-from-a-web-browser"></a><span data-ttu-id="49869-166">웹 브라우저에서 전자 메일 첨부 파일을 다운로드 하 여 암호를 해독 하는지 여부를 관리 하려면</span><span class="sxs-lookup"><span data-stu-id="49869-166">To manage whether email attachments are decrypted on download from a web browser</span></span>
  
1. <span data-ttu-id="49869-167">Office 365 조직에서 전역 관리자 권한이 있는 회사 또는 학교 계정을 사용 하 고, Windows PowerShell 세션을 시작 하 고, Exchange Online에 연결 합니다.</span><span class="sxs-lookup"><span data-stu-id="49869-167">Use a work or school account that has global administrator permissions in your Office 365 organization and start a Windows PowerShell session and connect to Exchange Online.</span></span> <span data-ttu-id="49869-168">자세한 내용은 [Exchange Online PowerShell에 연결을](https://aka.ms/exopowershell)참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="49869-168">For instructions, see [Connect to Exchange Online PowerShell](https://aka.ms/exopowershell).</span></span>

2. <span data-ttu-id="49869-169">DecryptAttachmentFromPortal 매개 변수를 사용 하 여 Set-IRMConfiguration cmdlet을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="49869-169">Run the Set-IRMConfiguration cmdlet with the DecryptAttachmentFromPortal parameter:</span></span>

   ```powershell
   Set-IRMConfiguration -DecryptAttachmentFromPortal <$true|$false>
   ```

   <span data-ttu-id="49869-170">예를 들어 사용자가 웹 브라우저에서 전자 메일 첨부 파일을 다운로드할 때 암호를 해독 하도록 서비스를 구성 하려면 다음을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="49869-170">For example, to configure the service to decrypt email attachments when a user downloads them from a web browser:</span></span>

   ```powershell
   Set-IRMConfiguration -DecryptAttachmentFromPortal $true
   ```

   <span data-ttu-id="49869-171">암호화 된 전자 메일 첨부 파일을 다운로드 하는 동안 남길 수 있도록 서비스를 구성 하려면 다음을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="49869-171">To configure the service to leave encrypted email attachments as they are upon download:</span></span>

   ```powershell
   Set-IRMConfiguration -DecryptAttachmentFromPortal $false
   ```

## <a name="ensure-all-external-recipients-use-the-ome-portal-to-read-encrypted-mail--office-365-advanced-message-encryption-only"></a><span data-ttu-id="49869-172">모든 외부 받는 사람이 OME 포털을 사용 하 여 암호화 된 메일을 읽도록 확인-Office 365 Advanced Message Encryption만 해당</span><span class="sxs-lookup"><span data-stu-id="49869-172">Ensure all external recipients use the OME Portal to read encrypted mail — Office 365 Advanced Message Encryption only</span></span>

<span data-ttu-id="49869-173">Office 365 고급 메시지 암호화가 있는 경우 사용자 지정 브랜딩 템플릿을 사용 하 여 받는 사람이 웹에서 Outlook 또는 Outlook을 사용 하는 대신 OME 포털에서 암호화 된 전자 메일을 읽도록 지시 하는 래퍼 메일을 받을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="49869-173">If you have Office 365 Advanced Message Encryption, you can use custom branding templates to force recipients to receive a wrapper mail that directs them to read encrypted email in the OME Portal instead of using Outlook or Outlook on the web.</span></span> <span data-ttu-id="49869-174">받는 사람이 받은 메일을 사용 하는 방법을 보다 강력 하 게 제어 하려는 경우에이 작업을 수행 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="49869-174">You might want to do this if you use want greater control over how recipients use the mail they receive.</span></span> <span data-ttu-id="49869-175">예를 들어 외부 받는 사람이 웹 포털에서 전자 메일을 볼 경우 전자 메일의 만료 날짜를 설정할 수 있으며 전자 메일을 해지할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="49869-175">For example, if external recipients view email in the web portal, you can set an expiration date for the email, and you can revoke the email.</span></span> <span data-ttu-id="49869-176">이러한 기능은 OME 포털을 통해서만 지원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="49869-176">These features are only supported through the OME Portal.</span></span> <span data-ttu-id="49869-177">메일 흐름 규칙을 만들 때 암호화 옵션 및 전달 금지 옵션을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="49869-177">You can use the Encrypt option and the Do Not Forward option when creating the mail flow rules.</span></span>

### <a name="create-a-custom-template-to-force-all-external-recipients-to-use-the-ome-portal-and-for-encrypted-email-to-be-revocable-and-expire-in-7-days"></a><span data-ttu-id="49869-178">모든 외부 받는 사람이 OME 포털을 사용 하 고 암호화 된 전자 메일이 7 일 후에 revocable 및 만료 되도록 하려면 사용자 지정 서식 파일을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="49869-178">Create a custom template to force all external recipients to use the OME Portal and for encrypted email to be revocable and expire in 7 days</span></span>

1. <span data-ttu-id="49869-179">Office 365 조직에서 전역 관리자 권한이 있는 회사 또는 학교 계정을 사용 하 고, Windows PowerShell 세션을 시작 하 고, Exchange Online에 연결 합니다.</span><span class="sxs-lookup"><span data-stu-id="49869-179">Use a work or school account that has global administrator permissions in your Office 365 organization and start a Windows PowerShell session and connect to Exchange Online.</span></span> <span data-ttu-id="49869-180">자세한 내용은 [Exchange Online PowerShell에 연결을](https://aka.ms/exopowershell)참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="49869-180">For instructions, see [Connect to Exchange Online PowerShell](https://aka.ms/exopowershell).</span></span>

2. <span data-ttu-id="49869-181">Set-omeconfiguration cmdlet을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="49869-181">Run the New-OMEConfiguration cmdlet:</span></span>

   ```powershell
   New-OMEConfiguration -Identity "<template name>" -ExternalMailExpiryInDays 7
   ```

   <span data-ttu-id="49869-182">여기서 `template name` 는 Office 365 메시지 암호화 사용자 지정 브랜딩 서식 파일에 사용 하려는 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="49869-182">where `template name` is the name you want to use for the Office 365 Message Encryption custom branding template.</span></span> <span data-ttu-id="49869-183">For example,</span><span class="sxs-lookup"><span data-stu-id="49869-183">For example,</span></span>

   ```powershell
   New-OMEConfiguration -Identity "<One week expiration>" -ExternalMailExpiryInDays 7
   ```

3. <span data-ttu-id="49869-184">New-transportrule cmdlet을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="49869-184">Run the New-TransportRule cmdlet:</span></span>

   ```powershell
   New-TransportRule -name "<mail flow rule name>" -FromScope "InOrganization" -ApplyRightsProtectionTemplate "<option name>" -ApplyRightsProtectionCustomizationTemplate "<template name>"
   ```

    <span data-ttu-id="49869-185">여기서 각 부분이 나타내는 의미는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="49869-185">where:</span></span>

   - <span data-ttu-id="49869-186">`mail flow rule name`은 새 메일 흐름 규칙에 사용할 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="49869-186">`mail flow rule name` is the name you want to use for the new mail flow rule.</span></span>

   - <span data-ttu-id="49869-187">`option name`은 `Encrypt` 또는 `Do Not Forward`입니다.</span><span class="sxs-lookup"><span data-stu-id="49869-187">`option name` is either `Encrypt` or `Do Not Forward`.</span></span>

   - <span data-ttu-id="49869-188">`template name`은 사용자 지정 브랜딩 서식 파일에 지정한 이름입니다 예: `One week expiration`</span><span class="sxs-lookup"><span data-stu-id="49869-188">`template name` is the name you gave the custom branding template, for example `One week expiration`.</span></span>

   <span data-ttu-id="49869-189">모든 외부 전자 메일을 "한 주 만료" 서식 파일로 암호화 하 고 암호화 전용 옵션을 적용 하려면 다음을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="49869-189">To encrypt all external email with the "One week expiration" template and apply the Encrypt-Only option:</span></span>

   ```powershell
   New-TransportRule -name "<All outgoing mail>" -FromScope "InOrganization" -ApplyRightsProtectionTemplate "Encrypt" -ApplyRightsProtectionCustomizationTemplate "<One week expiration>"
   ```

   <span data-ttu-id="49869-190">모든 외부 전자 메일을 "한 주 만료" 서식 파일로 암호화 하 고 전달 금지 옵션을 적용 하려면 다음을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="49869-190">To encrypt all external email with the "One week expiration" template and apply the Do Not Forward option:</span></span>

   ```powershell
   New-TransportRule -name "<All outgoing mail>" -FromScope "InOrganization" -ApplyRightsProtectionTemplate "Do Not Forward" -ApplyRightsProtectionCustomizationTemplate "<One week expiration>"
   ```

## <a name="customize-the-appearance-of-email-messages-and-the-ome-portal"></a><span data-ttu-id="49869-191">전자 메일 메시지 및 OME 포털의 모양 사용자 지정</span><span class="sxs-lookup"><span data-stu-id="49869-191">Customize the appearance of email messages and the OME portal</span></span>

<span data-ttu-id="49869-192">조직에 대해 OME를 사용자 지정 하는 방법에 대 한 자세한 내용은 [암호화 된 메시지에 조직의 브랜드 추가](add-your-organization-brand-to-encrypted-messages.md)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="49869-192">For detailed information about how you can customize OME for your organization, see [Add your organization's brand to your encrypted messages](add-your-organization-brand-to-encrypted-messages.md).</span></span>
  
## <a name="disable-the-new-capabilities-for-ome"></a><span data-ttu-id="49869-193">OME의 새 기능을 사용 하지 않도록 설정</span><span class="sxs-lookup"><span data-stu-id="49869-193">Disable the new capabilities for OME</span></span>

<span data-ttu-id="49869-194">OME에 대 한 새로운 기능을 사용 하지 않도록 설정 하는 것은 쉽지 않은 일입니다.</span><span class="sxs-lookup"><span data-stu-id="49869-194">We hope it doesn't come to it, but if you need to, disabling the new capabilities for OME is very straightforward.</span></span> <span data-ttu-id="49869-195">먼저 새 OME 기능을 사용 하 여 만든 메일 흐름 규칙을 제거 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="49869-195">First, you'll need to remove any mail flow rules you've created that use the new OME capabilities.</span></span> <span data-ttu-id="49869-196">메일 흐름 규칙을 제거 하는 방법에 대 한 자세한 내용은 [메일 흐름 규칙 관리](https://technet.microsoft.com/library/jj657505%28v=exchg.150%29.aspx)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="49869-196">For information about removing mail flow rules, see [Manage mail flow rules](https://technet.microsoft.com/library/jj657505%28v=exchg.150%29.aspx).</span></span> <span data-ttu-id="49869-197">그런 다음 Exchange Online PowerShell에서 다음 단계를 완료 합니다.</span><span class="sxs-lookup"><span data-stu-id="49869-197">Then, complete these steps in Exchange Online PowerShell.</span></span>
  
### <a name="to-disable-the-new-capabilities-for-ome"></a><span data-ttu-id="49869-198">OME에 대 한 새 기능을 사용 하지 않도록 설정 하려면</span><span class="sxs-lookup"><span data-stu-id="49869-198">To disable the new capabilities for OME</span></span>
  
1. <span data-ttu-id="49869-199">Office 365 조직에서 전역 관리자 권한이 있는 회사 또는 학교 계정을 사용 하는 경우 Windows PowerShell 세션을 시작 하 고 Exchange Online에 연결 합니다.</span><span class="sxs-lookup"><span data-stu-id="49869-199">Using a work or school account that has global administrator permissions in your Office 365 organization, start a Windows PowerShell session and connect to Exchange Online.</span></span> <span data-ttu-id="49869-200">자세한 내용은 [Exchange Online PowerShell에 연결을](https://aka.ms/exopowershell)참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="49869-200">For instructions, see [Connect to Exchange Online PowerShell](https://aka.ms/exopowershell).</span></span>

2. <span data-ttu-id="49869-201">웹용 Outlook에서 **암호화** 단추를 사용 하도록 설정한 경우에는 SimplifiedClientAccessEnabled 매개 변수를 사용 하 여 Set-IRMConfiguration cmdlet을 실행 하 여 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="49869-201">If you enabled the **Encrypt** button in Outlook on the web, disable it by running the Set-IRMConfiguration cmdlet with the SimplifiedClientAccessEnabled parameter.</span></span> <span data-ttu-id="49869-202">그렇지 않으면이 단계를 건너뜁니다.</span><span class="sxs-lookup"><span data-stu-id="49869-202">Otherwise, skip this step.</span></span>

   ```powershell
   Set-IRMConfiguration -SimplifiedClientAccessEnabled $false
   ```

3. <span data-ttu-id="49869-203">AzureRMSLicensingEnabled 매개 변수를 false로 설정 하 고 OME의 새 기능을 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="49869-203">Disable the new capabilities for OME by running the Set-IRMConfiguration cmdlet with the AzureRMSLicensingEnabled parameter set to false:</span></span>

   ```powershell
   Set-IRMConfiguration -AzureRMSLicensingEnabled $false
   ```
