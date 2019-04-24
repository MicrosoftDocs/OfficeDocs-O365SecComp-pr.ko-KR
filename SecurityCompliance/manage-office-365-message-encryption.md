---
title: Office 365 메시지 암호화 관리
ms.author: tracyp
author: MSFTTracyP
manager: laurawi
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 09f6737e-f03f-4bc8-8281-e46d24ee2a74
ms.collection:
- M365-security-compliance
description: Office 365 메시지 암호화 (OME) 설정을 완료 한 후에는 여러 가지 방법으로 배포 구성을 사용자 지정할 수 있습니다. 예를 들어, 웹의 Outlook에서 1 회 통과, 보호 단추를 표시할 것인지 여부를 구성할 수 있습니다. 이 문서의 작업에서는 이러한 방법을 설명 합니다.
ms.openlocfilehash: 7b5297ae42d3efa071408540863c6ff7dbdee407
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32259816"
---
# <a name="manage-office-365-message-encryption"></a><span data-ttu-id="8fdd8-105">Office 365 메시지 암호화 관리</span><span class="sxs-lookup"><span data-stu-id="8fdd8-105">Manage Office 365 Message Encryption</span></span>

<span data-ttu-id="8fdd8-106">Office 365 메시지 암호화 (OME) 설정을 완료 한 후에는 여러 가지 방법으로 배포 구성을 사용자 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8fdd8-106">Once you've finished setting up Office 365 Message Encryption (OME), you can customize the configuration of your deployment in a number of ways.</span></span> <span data-ttu-id="8fdd8-107">예를 들어, 웹의 Outlook에서 1 회 통과, **보호** 단추를 표시할 것인지 여부를 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8fdd8-107">For example, you can configure whether to enable one-time pass codes, display the **Protect** button in Outlook on the web, and more.</span></span> <span data-ttu-id="8fdd8-108">이 문서의 작업에서는 이러한 방법을 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="8fdd8-108">The tasks in this article describe how.</span></span>
  
||
|:-----|
|<span data-ttu-id="8fdd8-109">이 문서는 Office 365 메시지 암호화에 대 한 보다 광범위 한 문서에 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8fdd8-109">This article is part of a larger series of articles about Office 365 Message Encryption.</span></span> <span data-ttu-id="8fdd8-110">이 문서는 관리자와 itpros 전문가를 위한 것입니다.</span><span class="sxs-lookup"><span data-stu-id="8fdd8-110">This article is intended for administrators and ITPros.</span></span> <span data-ttu-id="8fdd8-111">암호화 된 메시지를 보내거나 받는 방법에 대 한 정보를 찾으려는 경우에는 [Office 365 메시지 암호화 (OME)](ome.md) 의 문서 목록을 참조 하 여 요구 사항에 가장 적합 한 문서를 검색 하세요.</span><span class="sxs-lookup"><span data-stu-id="8fdd8-111">If you're just looking for information on sending or receiving an encrypted message, see the list of articles in [Office 365 Message Encryption (OME)](ome.md) and locate the article that best fits your needs.</span></span> |
||

## <a name="managing-whether-google-yahoo-and-microsoft-account-recipients-can-use-these-accounts-to-sign-in-to-the-office-365-message-encryption-portal"></a><span data-ttu-id="8fdd8-112">Google, Yahoo 및 Microsoft 계정 받는 사람이 이러한 계정을 사용 하 여 Office 365 메시지 암호화 포털에 로그인 할 수 있는지 여부를 관리 합니다.</span><span class="sxs-lookup"><span data-stu-id="8fdd8-112">Managing whether Google, Yahoo, and Microsoft Account recipients can use these accounts to sign in to the Office 365 Message Encryption portal</span></span>

<span data-ttu-id="8fdd8-113">기본적으로 새 Office 365 메시지 암호화 기능을 설정 하면 조직의 사용자가 Office 365 조 직 외부에 있는 받는 사람에 게 메시지를 보낼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8fdd8-113">By default, when you set up the new Office 365 Message Encryption capabilities, users in your organization can send messages to recipients that are outside of your Office 365 organization.</span></span> <span data-ttu-id="8fdd8-114">받는 사람이 Google 계정, Yahoo account 또는 Microsoft 계정과 같은 *공유 id* 를 사용 하는 경우 받는 사람은 공유 id를 사용 하 여 OME 포털에 로그인 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8fdd8-114">If the recipient uses a *social ID* such as a Google account, Yahoo account, or Microsoft account, the recipient can sign in to the OME portal using the social ID.</span></span> <span data-ttu-id="8fdd8-115">원하는 경우 받는 사람이 공유 id를 사용 하 여 OME 포털에 로그인 하는 것을 허용 하지 않도록 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8fdd8-115">If you want, you can choose not to allow recipients to use social IDs to sign in to the OME portal.</span></span>
  
### <a name="to-manage-whether-or-not-to-allow-recipients-to-use-social-ids-to-sign-in-to-the-ome-portal"></a><span data-ttu-id="8fdd8-116">받는 사람이 공유 id를 사용 하 여 OME 포털에 로그인 하도록 허용할지 여부를 관리 하려면</span><span class="sxs-lookup"><span data-stu-id="8fdd8-116">To manage whether or not to allow recipients to use social IDs to sign in to the OME portal</span></span>
  
1. <span data-ttu-id="8fdd8-117">[원격 PowerShell을 사용 하 여 Exchange Online에 연결](http://technet.microsoft.com/library/jj984289%28v=exchg.150%29.aspx)합니다.</span><span class="sxs-lookup"><span data-stu-id="8fdd8-117">[Connect to Exchange Online Using Remote PowerShell](http://technet.microsoft.com/library/jj984289%28v=exchg.150%29.aspx).</span></span>

2. <span data-ttu-id="8fdd8-118">다음과 같이, set-omeconfiguration cmdlet을 사회 alidsignin 매개 변수를 사용 하 여 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="8fdd8-118">Run the Set-OMEConfiguration cmdlet with the SocialIdSignIn parameter as follows:</span></span>

   ```powershell
   Set-OMEConfiguration -Identity <"OMEConfigurationIdParameter "> -SocialIdSignIn <$true | $false>
   ```

   <span data-ttu-id="8fdd8-119">예를 들어, 공유 id를 사용 하지 않도록 설정 하려면</span><span class="sxs-lookup"><span data-stu-id="8fdd8-119">For example, to disable social IDs:</span></span>

   ```powershell
   Set-OMEConfiguration -Identity "OME Configuration" -SocialIdSignIn $false
   ```

   <span data-ttu-id="8fdd8-120">공유 id를 사용 하도록 설정 하려면:</span><span class="sxs-lookup"><span data-stu-id="8fdd8-120">To enable social IDs:</span></span>

   ```powershell
   Set-OMEConfiguration -Identity "OME Configuration" -SocialIdSignIn $true
   ```

## <a name="managing-the-use-of-one-time-pass-codes-for-signing-in-to-the-office-365-message-encryption-portal"></a><span data-ttu-id="8fdd8-121">Office 365 메시지 암호화 포털에 로그인 하기 위한 1 회 통과 코드 사용 관리</span><span class="sxs-lookup"><span data-stu-id="8fdd8-121">Managing the use of one-time pass codes for signing in to the Office 365 Message Encryption portal</span></span>

<span data-ttu-id="8fdd8-122">기본적으로 OME에서 암호화 된 메시지를 받는 사람이 Outlook을 사용 하지 않는 경우에는 받는 사람이 사용 하는 계정에 관계 없이 받는 사람에 게 메시지를 읽을 수 있는 제한 된 웹 보기 링크가 수신 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8fdd8-122">By default, if the recipient of a message encrypted by OME doesn't use Outlook, regardless of the account used by the recipient, the recipient receives a limited-time web-view link that lets them read the message.</span></span> <span data-ttu-id="8fdd8-123">여기에는 1 회 통과 코드가 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8fdd8-123">This includes a one-time pass code.</span></span> <span data-ttu-id="8fdd8-124">관리자는 OME 포털에 로그인 하는 데 일회성 통과 코드를 사용할 수 있는지 여부를 관리할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8fdd8-124">As an administrator, you can manage whether or not one-time pass codes can be used to sign-in to the OME portal.</span></span>
  
### <a name="to-manage-whether-or-not-one-time-pass-codes-are-generated-for-ome"></a><span data-ttu-id="8fdd8-125">OME에 대해 1 회 가공 패스 코드가 생성 되는지 여부를 관리 하려면</span><span class="sxs-lookup"><span data-stu-id="8fdd8-125">To manage whether or not one-time pass codes are generated for OME</span></span>
  
1. <span data-ttu-id="8fdd8-126">Office 365 조직에서 전역 관리자 권한이 있는 회사 또는 학교 계정을 사용 하는 경우 Windows PowerShell 세션을 시작 하 고 Exchange Online에 연결 합니다.</span><span class="sxs-lookup"><span data-stu-id="8fdd8-126">Using a work or school account that has global administrator permissions in your Office 365 organization, start a Windows PowerShell session and connect to Exchange Online.</span></span> <span data-ttu-id="8fdd8-127">자세한 내용은 [Exchange Online PowerShell에 연결을](https://aka.ms/exopowershell)참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="8fdd8-127">For instructions, see [Connect to Exchange Online PowerShell](https://aka.ms/exopowershell).</span></span>

2. <span data-ttu-id="8fdd8-128">OTPEnabled 매개 변수를 사용 하 여 set-omeconfiguration cmdlet을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="8fdd8-128">Run the Set-OMEConfiguration cmdlet with the OTPEnabled parameter:</span></span>

   ```powershell
   Set-OMEConfiguration -Identity <"OMEConfigurationIdParameter "> -OTPEnabled <$true|$false>
   ```

   <span data-ttu-id="8fdd8-129">예를 들어, 1 회 통과 코드를 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8fdd8-129">For example, to disable one-time pass codes:</span></span>

   ```powershell
   Set-OMEConfiguration -Identity "OME Configuration" -OTPEnabled $false
   ```

   <span data-ttu-id="8fdd8-130">1 회 통과 코드를 사용 하도록 설정 하려면:</span><span class="sxs-lookup"><span data-stu-id="8fdd8-130">To enable one-time pass codes:</span></span>

   ```powershell
   Set-OMEConfiguration -Identity "OME Configuration" -OTPEnabled $true
   ```

## <a name="managing-the-display-of-the-protect-button-in-outlook-on-the-web"></a><span data-ttu-id="8fdd8-131">웹용 Outlook에서 보호 단추 표시 관리</span><span class="sxs-lookup"><span data-stu-id="8fdd8-131">Managing the display of the Protect button in Outlook on the web</span></span>

<span data-ttu-id="8fdd8-132">기본적으로 OME를 설정 해도 웹용 Outlook의 **보호** 단추는 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="8fdd8-132">By default, the **Protect** button in Outlook on the web is not enabled when you set up OME.</span></span> <span data-ttu-id="8fdd8-133">관리자는이 단추를 최종 사용자에 게 표시할지 여부를 관리할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8fdd8-133">As an administrator, you can manage whether or not to display this button to end users.</span></span>
  
### <a name="to-manage-whether-or-not-the-protect-button-appears-in-outlook-on-the-web"></a><span data-ttu-id="8fdd8-134">웹에서 Outlook에 보호 단추가 표시 되는지 여부를 관리 하려면</span><span class="sxs-lookup"><span data-stu-id="8fdd8-134">To manage whether or not the Protect button appears in Outlook on the web</span></span>
  
1. <span data-ttu-id="8fdd8-135">Office 365 조직에서 전역 관리자 권한이 있는 회사 또는 학교 계정을 사용 하는 경우 Windows PowerShell 세션을 시작 하 고 Exchange Online에 연결 합니다.</span><span class="sxs-lookup"><span data-stu-id="8fdd8-135">Using a work or school account that has global administrator permissions in your Office 365 organization, start a Windows PowerShell session and connect to Exchange Online.</span></span> <span data-ttu-id="8fdd8-136">자세한 내용은 [Exchange Online PowerShell에 연결을](https://aka.ms/exopowershell)참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="8fdd8-136">For instructions, see [Connect to Exchange Online PowerShell](https://aka.ms/exopowershell).</span></span>

2. <span data-ttu-id="8fdd8-137">-SimplifiedClientAccessEnabled 매개 변수를 사용 하 여 irmconfiguration cmdlet을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="8fdd8-137">Run the Set-IRMConfiguration cmdlet with the -SimplifiedClientAccessEnabled parameter:</span></span>

   ```powershell
   Set-IRMConfiguration -SimplifiedClientAccessEnabled <$true|$false>
   ```

   <span data-ttu-id="8fdd8-138">예를 들어 **보호** 단추를 사용 하지 않으려면 다음을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="8fdd8-138">For example, to disable the **Protect** button:</span></span>

   ```powershell
   Set-IRMConfiguration -SimplifiedClientAccessEnabled $false
   ```

   <span data-ttu-id="8fdd8-139">**보호** 단추를 사용 하도록 설정 하려면:</span><span class="sxs-lookup"><span data-stu-id="8fdd8-139">To enable the **Protect** button:</span></span>

   ```powershell
   Set-IRMConfiguration -SimplifiedClientAccessEnabled $true
   ```

## <a name="enable-service-side-decryption-of-email-messages-for-ios-mail-app-users"></a><span data-ttu-id="8fdd8-140">iOS 메일 앱 사용자에 대 한 전자 메일 메시지의 서비스 쪽 암호 해독을 사용 하도록 설정</span><span class="sxs-lookup"><span data-stu-id="8fdd8-140">Enable service-side decryption of email messages for iOS mail app users</span></span>

<span data-ttu-id="8fdd8-141">iOS 메일 앱은 Office 365 메시지 암호화로 보호 된 메시지의 암호를 해독할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="8fdd8-141">The iOS mail app can't decrypt messages protected with Office 365 Message Encryption.</span></span> <span data-ttu-id="8fdd8-142">Office 365 관리자는 iOS 메일 앱으로 배달 되는 메시지에 대해 서비스 쪽 암호 해독을 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8fdd8-142">As an Office 365 administrator, you can apply service-side decryption for messages delivered to the iOS mail app.</span></span> <span data-ttu-id="8fdd8-143">이 작업을 수행 하도록 선택 하면 서비스에서 암호 해독 된 메시지 복사본을 iOS 장치로 보냅니다.</span><span class="sxs-lookup"><span data-stu-id="8fdd8-143">When you choose to do this, the service sends a decrypted copy of the message to the iOS device.</span></span> <span data-ttu-id="8fdd8-144">메시지가 클라이언트 장치에 해독 되어 저장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8fdd8-144">The message is stored decrypted on the client device.</span></span> <span data-ttu-id="8fdd8-145">또한 iOS 메일 앱이 사용자에 게 클라이언트 쪽 사용 권한을 적용 하지 않더라도 사용 권한에 대 한 정보도 유지 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8fdd8-145">The message also retains information about usage rights even though the iOS mail app doesn't apply client-side usage rights to the user.</span></span> <span data-ttu-id="8fdd8-146">즉, 사용자가 원래 사용 권한을 갖고 있지 않은 경우에도 메시지를 복사 하거나 인쇄할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8fdd8-146">This means that the user can copy or print the message even if they did not originally have the rights to do so.</span></span> <span data-ttu-id="8fdd8-147">그러나 사용자가 Office 365 메일 서버가 필요한 작업 (예: 메시지 전달)을 완료 하려고 하면 사용자가 원래 사용 권한을 갖고 있지 않은 경우 서버에서 해당 작업을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8fdd8-147">However, if the user attempts to complete an action that requires the Office 365 mail server, such as forwarding the message, the server will not permit the action if the user did not originally have the usage right to do so.</span></span> <span data-ttu-id="8fdd8-148">그러나 최종 사용자는 iOS 메일 응용 프로그램의 다른 계정에서 메시지를 전달 하 여 사용 제한을 전달 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8fdd8-148">However, end-users can work around Do Not Forward usage restriction by forwarding the message from a different account in their iOS mail app.</span></span> <span data-ttu-id="8fdd8-149">메일의 서비스 쪽 암호 해독이 설정 되어 있는지 여부에 관계 없이 암호화 및 권한으로 보호 된 메일에 대 한 모든 첨부 파일을 iOS 메일 앱에서 볼 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="8fdd8-149">Regardless of whether you set up service-side decryption of mail, any attachments to encrypted and rights protected mail cannot be viewed in the iOS mail app.</span></span>
  
<span data-ttu-id="8fdd8-150">암호 해독 된 메시지를 iOS 메일 앱 사용자에 게 보내도록 허용 하지 않도록 선택 하면 사용자에 게 메시지를 볼 수 있는 권한이 없다는 메시지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8fdd8-150">If you choose not to allow decrypted messages to be sent to iOS mail app users, users receive a message that states that they don't have the rights to view the message.</span></span> <span data-ttu-id="8fdd8-151">기본적으로 전자 메일 메시지의 서비스 쪽 암호 해독이 사용 되도록 설정 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8fdd8-151">By default, service-side decryption of email messages is not enabled.</span></span>
  
<span data-ttu-id="8fdd8-152">자세한 내용과 클라이언트 환경의 보기에 대 한 자세한 내용은 [iPhone 또는 iPad에서 암호화 된 메시지 보기](https://support.office.com/article/4d631321-0d26-4bcc-a483-d294dd0b1caf)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="8fdd8-152">For more information, and for a view of the client experience, see [View encrypted messages on your iPhone or iPad](https://support.office.com/article/4d631321-0d26-4bcc-a483-d294dd0b1caf).</span></span>
  
### <a name="to-manage-whether-or-not-ios-mail-app-users-can-view-messages-protected-by-office-365-message-encryption"></a><span data-ttu-id="8fdd8-153">iOS 메일 앱 사용자가 Office 365 메시지 암호화로 보호 된 메시지를 볼 수 있는지 여부를 관리 하려면</span><span class="sxs-lookup"><span data-stu-id="8fdd8-153">To manage whether or not iOS mail app users can view messages protected by Office 365 Message Encryption</span></span>
  
1. <span data-ttu-id="8fdd8-154">Office 365 조직에서 전역 관리자 권한이 있는 회사 또는 학교 계정을 사용 하는 경우 Windows PowerShell 세션을 시작 하 고 Exchange Online에 연결 합니다.</span><span class="sxs-lookup"><span data-stu-id="8fdd8-154">Using a work or school account that has global administrator permissions in your Office 365 organization, start a Windows PowerShell session and connect to Exchange Online.</span></span> <span data-ttu-id="8fdd8-155">자세한 내용은 [Exchange Online PowerShell에 연결을](https://aka.ms/exopowershell)참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="8fdd8-155">For instructions, see [Connect to Exchange Online PowerShell](https://aka.ms/exopowershell).</span></span>

2. <span data-ttu-id="8fdd8-156">AllowRMSSupportForUnenlightenedApps 매개 변수를 사용 하 여 ActiveSyncOrganizations cmdlet을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="8fdd8-156">Run the Set-ActiveSyncOrganizations cmdlet with the AllowRMSSupportForUnenlightenedApps parameter:</span></span>

   ```powershell
   Set-ActiveSyncOrganizationSettings -AllowRMSSupportForUnenlightenedApps <$true|$false>
   ```

   <span data-ttu-id="8fdd8-157">예를 들어 메시지가 iOS 메일 응용 프로그램과 같은 unenlightened 앱으로 전송 되기 전에 암호를 해독 하도록 서비스를 구성 하려면 다음을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="8fdd8-157">For example, to configure the service to decrypt messages before they are sent to unenlightened apps such as the iOS mail app:</span></span>

   ```powershell
   Set-ActiveSyncOrganizationSettings -AllowRMSSupportForUnenlightenedApps $true
   ```

   <span data-ttu-id="8fdd8-158">또는 암호화 되지 않은 메시지를 unenlightened 앱으로 보내지 않도록 서비스를 구성 하려면 다음을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="8fdd8-158">Or, to configure the service not to send decrypted messages to unenlightened apps:</span></span>

   ```powershell
   Set-ActiveSyncOrganizationSettings -AllowRMSSupportForUnenlightenedApps $false
   ```

## <a name="enable-service-side-decryption-of-email-attachments-for-web-browser-mail-clients"></a><span data-ttu-id="8fdd8-159">웹 브라우저 메일 클라이언트에 대 한 전자 메일 첨부 파일의 서비스 쪽 암호 해독을 사용 하도록 설정</span><span class="sxs-lookup"><span data-stu-id="8fdd8-159">Enable service-side decryption of email attachments for web browser mail clients</span></span>

<span data-ttu-id="8fdd8-160">일반적으로 Office 365 메시지 암호화를 사용 하면 첨부 파일이 자동으로 암호화 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8fdd8-160">Normally, when you use Office 365 message encryption, attachments are automatically encrypted.</span></span> <span data-ttu-id="8fdd8-161">Office 365 관리자는 사용자가 웹 브라우저에서 다운로드 하는 전자 메일 첨부 파일에 대해 서비스 쪽 암호 해독을 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8fdd8-161">As an Office 365 administrator, you can apply service-side decryption for email attachments that users download from a web browser.</span></span>
  
<span data-ttu-id="8fdd8-162">이 작업을 선택 하면 서비스에서 암호 해독 된 파일 복사본을 장치로 보냅니다.</span><span class="sxs-lookup"><span data-stu-id="8fdd8-162">When you choose to do this, the service sends a decrypted copy of the file to the device.</span></span> <span data-ttu-id="8fdd8-163">메시지가 계속 암호화 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8fdd8-163">The message is still encrypted.</span></span> <span data-ttu-id="8fdd8-164">또한 전자 메일 첨부 파일은 브라우저가 클라이언트 쪽 사용 권한을 사용자에 게 적용 하지 않더라도 사용 권한에 대 한 정보를 유지 합니다.</span><span class="sxs-lookup"><span data-stu-id="8fdd8-164">The email attachment also retains information about usage rights even though the browser does not apply client-side usage rights to the user.</span></span> <span data-ttu-id="8fdd8-165">즉, 사용자가 원래 사용 권한을 갖고 있지 않은 경우에도 전자 메일 첨부 파일을 복사 하거나 인쇄할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8fdd8-165">This means that the user can copy or print the email attachment even if they did not originally have the rights to do so.</span></span> <span data-ttu-id="8fdd8-166">그러나 사용자가 Office 365 메일 서버가 필요한 작업 (예: 첨부 파일 전달)을 완료 하려고 하면 사용자가 원래 사용 권한을 갖고 있지 않은 경우 서버에서 해당 작업을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8fdd8-166">However, if the user attempts to complete an action that requires the Office 365 mail server, such as forwarding the attachment, the server will not permit the action if the user did not originally have the usage right to do so.</span></span>
  
<span data-ttu-id="8fdd8-167">첨부 파일에 대 한 서비스 쪽 암호 해독을 설정 하는지 여부에 관계 없이 암호화 및 권한으로 보호 되는 메일에 대 한 모든 첨부 파일을 iOS 메일 앱에서 볼 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="8fdd8-167">Regardless of whether you set up service-side decryption of attachments, any attachments to encrypted and rights protected mail cannot be viewed in the iOS mail app.</span></span>
  
<span data-ttu-id="8fdd8-168">해독 된 전자 메일 첨부 파일 (기본값)을 허용 하지 않도록 선택 하면 사용자에 게 첨부 파일을 볼 수 있는 권한이 없다는 메시지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8fdd8-168">If you choose not to allow decrypted email attachments, which is the default, users receive a message that states that they don't have the rights to view the attachment.</span></span>
  
<span data-ttu-id="8fdd8-169">Office 365에서 암호화 전용 옵션을 사용 하 여 전자 메일 첨부 파일에 대 한 암호화를 구현 하는 방법에 대 한 자세한 내용은 [전자 메일에 대 한 암호화 전용 옵션](https://docs.microsoft.com/azure/information-protection/deploy-use/configure-usage-rights#encrypt-only-option-for-emails) 을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="8fdd8-169">For more information about how Office 365 implements encryption for emails and email attachments with the Encrypt-Only option, see [Encrypt-Only option for emails.](https://docs.microsoft.com/azure/information-protection/deploy-use/configure-usage-rights#encrypt-only-option-for-emails)</span></span>
  
### <a name="to-manage-whether-or-not-email-attachments-are-decrypted-on-download-from-a-web-browser"></a><span data-ttu-id="8fdd8-170">웹 브라우저에서 전자 메일 첨부 파일을 다운로드 하 여 암호를 해독 하는지 여부를 관리 하려면</span><span class="sxs-lookup"><span data-stu-id="8fdd8-170">To manage whether or not email attachments are decrypted on download from a web browser</span></span>
  
1. <span data-ttu-id="8fdd8-171">Office 365 조직에서 전역 관리자 권한이 있는 회사 또는 학교 계정을 사용 하는 경우 Windows PowerShell 세션을 시작 하 고 Exchange Online에 연결 합니다.</span><span class="sxs-lookup"><span data-stu-id="8fdd8-171">Using a work or school account that has global administrator permissions in your Office 365 organization, start a Windows PowerShell session and connect to Exchange Online.</span></span> <span data-ttu-id="8fdd8-172">자세한 내용은 [Exchange Online PowerShell에 연결을](https://aka.ms/exopowershell)참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="8fdd8-172">For instructions, see [Connect to Exchange Online PowerShell](https://aka.ms/exopowershell).</span></span>

2. <span data-ttu-id="8fdd8-173">DecryptAttachmentFromPortal 매개 변수를 사용 하 여 Set-irmconfiguration cmdlet을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="8fdd8-173">Run the Set-IRMConfiguration cmdlet with the DecryptAttachmentFromPortal parameter:</span></span>

   ```powershell
   Set-IRMConfiguration -DecryptAttachmentFromPortal <$true|$false>
   ```

   <span data-ttu-id="8fdd8-174">예를 들어 사용자가 웹 브라우저에서 전자 메일 첨부 파일을 다운로드할 때 암호를 해독 하도록 서비스를 구성 하려면 다음을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="8fdd8-174">For example, to configure the service to decrypt email attachments when a user downloads them from a web browser:</span></span>

   ```powershell
   Set-IRMConfiguration -DecryptAttachmentFromPortal $true
   ```

   <span data-ttu-id="8fdd8-175">암호화 된 전자 메일 첨부 파일을 다운로드 하는 동안 남길 수 있도록 서비스를 구성 하려면 다음을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="8fdd8-175">To configure the service to leave encrypted email attachments as they are upon download:</span></span>

   ```powershell
   Set-IRMConfiguration -DecryptAttachmentFromPortal $false
   ```

## <a name="customizing-the-appearance-of-email-messages-and-the-ome-portal"></a><span data-ttu-id="8fdd8-176">전자 메일 메시지 및 OME 포털의 모양 사용자 지정</span><span class="sxs-lookup"><span data-stu-id="8fdd8-176">Customizing the appearance of email messages and the OME portal</span></span>

<span data-ttu-id="8fdd8-177">조직에 대해 OME를 사용자 지정 하는 방법에 대 한 자세한 내용은 [암호화 된 메시지에 조직의 브랜드 추가](add-your-organization-brand-to-encrypted-messages.md)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="8fdd8-177">For detailed information about how you can customize OME for your organization, see [Add your organization's brand to your encrypted messages](add-your-organization-brand-to-encrypted-messages.md).</span></span>
  
## <a name="disabling-the-new-capabilities-for-ome"></a><span data-ttu-id="8fdd8-178">OME의 새 기능을 사용 하지 않도록 설정</span><span class="sxs-lookup"><span data-stu-id="8fdd8-178">Disabling the new capabilities for OME</span></span>

<span data-ttu-id="8fdd8-179">OME에 대 한 새로운 기능을 사용 하지 않도록 설정 하는 것은 쉽지 않은 일입니다.</span><span class="sxs-lookup"><span data-stu-id="8fdd8-179">We hope it doesn't come to it, but if you need to, disabling the new capabilities for OME is very straightforward.</span></span> <span data-ttu-id="8fdd8-180">먼저 새 OME 기능을 사용 하 여 만든 메일 흐름 규칙을 제거 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="8fdd8-180">First, you'll need to remove any mail flow rules you've created that use the new OME capabilities.</span></span> <span data-ttu-id="8fdd8-181">메일 흐름 규칙을 제거 하는 방법에 대 한 자세한 내용은 [메일 흐름 규칙 관리](https://technet.microsoft.com/library/jj657505%28v=exchg.150%29.aspx)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="8fdd8-181">For information about removing mail flow rules, see [Manage mail flow rules](https://technet.microsoft.com/library/jj657505%28v=exchg.150%29.aspx).</span></span> <span data-ttu-id="8fdd8-182">그런 다음 Exchange Online PowerShell에서 다음 단계를 완료 합니다.</span><span class="sxs-lookup"><span data-stu-id="8fdd8-182">Then, complete these steps in Exchange Online PowerShell.</span></span>
  
### <a name="to-disable-the-new-capabilities-for-ome"></a><span data-ttu-id="8fdd8-183">OME에 대 한 새 기능을 사용 하지 않도록 설정 하려면</span><span class="sxs-lookup"><span data-stu-id="8fdd8-183">To disable the new capabilities for OME</span></span>
  
1. <span data-ttu-id="8fdd8-184">Office 365 조직에서 전역 관리자 권한이 있는 회사 또는 학교 계정을 사용 하는 경우 Windows PowerShell 세션을 시작 하 고 Exchange Online에 연결 합니다.</span><span class="sxs-lookup"><span data-stu-id="8fdd8-184">Using a work or school account that has global administrator permissions in your Office 365 organization, start a Windows PowerShell session and connect to Exchange Online.</span></span> <span data-ttu-id="8fdd8-185">자세한 내용은 [Exchange Online PowerShell에 연결을](https://aka.ms/exopowershell)참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="8fdd8-185">For instructions, see [Connect to Exchange Online PowerShell](https://aka.ms/exopowershell).</span></span>

2. <span data-ttu-id="8fdd8-186">웹용 Outlook에서 **보호** 단추를 사용 하도록 설정한 경우 SimplifiedClientAccessEnabled 매개 변수를 사용 하 여 Set-irmconfiguration cmdlet을 실행 하 여 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8fdd8-186">If you enabled the **Protect** button in Outlook on the web, disable it by running the Set-IRMConfiguration cmdlet with the SimplifiedClientAccessEnabled parameter.</span></span> <span data-ttu-id="8fdd8-187">그렇지 않으면이 단계를 건너뜁니다.</span><span class="sxs-lookup"><span data-stu-id="8fdd8-187">Otherwise, skip this step.</span></span>

   ```powershell
   Set-IRMConfiguration -SimplifiedClientAccessEnabled $false
   ```

3. <span data-ttu-id="8fdd8-188">AzureRMSLicensingEnabled 매개 변수를 false로 설정 하 고 OME의 새 기능을 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8fdd8-188">Disable the new capabilities for OME by running the Set-IRMConfiguration cmdlet with the AzureRMSLicensingEnabled parameter set to false:</span></span>

   ```powershell
   Set-IRMConfiguration -AzureRMSLicensingEnabled $false
   ```
