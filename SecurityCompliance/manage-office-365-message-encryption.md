---
title: Office 365 메시지 암호화 관리
ms.author: krowley
author: kccross
manager: laurawi
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 09f6737e-f03f-4bc8-8281-e46d24ee2a74
description: Office 365 메시지 암호화 (OME) 설정을 완료 한 후에는 여러 가지 방법으로 배포 구성을 사용자 지정할 수 있습니다. 예를 들어, 웹의 Outlook에서 1 회 통과, 보호 단추를 표시할 것인지 여부를 구성할 수 있습니다. 이 문서의 작업에서는 이러한 방법을 설명 합니다.
ms.openlocfilehash: 8b044898efb1ef86790773cd3f8e8061523b0ec0
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30213758"
---
# <a name="manage-office-365-message-encryption"></a>Office 365 메시지 암호화 관리

Office 365 메시지 암호화 (OME) 설정을 완료 한 후에는 여러 가지 방법으로 배포 구성을 사용자 지정할 수 있습니다. 예를 들어, 웹의 Outlook에서 1 회 통과, **보호** 단추를 표시할 것인지 여부를 구성할 수 있습니다. 이 문서의 작업에서는 이러한 방법을 설명 합니다.
  
||
|:-----|
|이 문서는 Office 365 메시지 암호화에 대 한 보다 광범위 한 문서에 포함 되어 있습니다. 이 문서는 관리자와 itpros 전문가를 위한 것입니다. 암호화 된 메시지를 보내거나 받는 방법에 대 한 정보를 찾으려는 경우에는 [Office 365 메시지 암호화 (OME)](ome.md) 의 문서 목록을 참조 하 여 요구 사항에 가장 적합 한 문서를 검색 하세요. |
||

## <a name="managing-whether-google-yahoo-and-microsoft-account-recipients-can-use-these-accounts-to-sign-in-to-the-office-365-message-encryption-portal"></a>Google, Yahoo 및 Microsoft 계정 받는 사람이 이러한 계정을 사용 하 여 Office 365 메시지 암호화 포털에 로그인 할 수 있는지 여부를 관리 합니다.

기본적으로 새 Office 365 메시지 암호화 기능을 설정 하면 조직의 사용자가 Office 365 조 직 외부에 있는 받는 사람에 게 메시지를 보낼 수 있습니다. 받는 사람이 Google 계정, Yahoo account 또는 Microsoft 계정과 같은 *공유 id* 를 사용 하는 경우 받는 사람은 공유 id를 사용 하 여 OME 포털에 로그인 할 수 있습니다. 원하는 경우 받는 사람이 공유 id를 사용 하 여 OME 포털에 로그인 하는 것을 허용 하지 않도록 선택할 수 있습니다.
  
### <a name="to-manage-whether-or-not-to-allow-recipients-to-use-social-ids-to-sign-in-to-the-ome-portal"></a>받는 사람이 공유 id를 사용 하 여 OME 포털에 로그인 하도록 허용할지 여부를 관리 하려면
  
1. [원격 PowerShell을 사용 하 여 Exchange Online에 연결](http://technet.microsoft.com/library/jj984289%28v=exchg.150%29.aspx)합니다.

2. 다음과 같이, set-omeconfiguration cmdlet을 사회 alidsignin 매개 변수를 사용 하 여 실행 합니다.

   ```powershell
   Set-OMEConfiguration -Identity <"OMEConfigurationIdParameter "> -SocialIdSignIn <$true | $false>
   ```

   예를 들어, 공유 id를 사용 하지 않도록 설정 하려면

   ```powershell
   Set-OMEConfiguration -Identity "OME Configuration" -SocialIdSignIn $false
   ```

   공유 id를 사용 하도록 설정 하려면:

   ```powershell
   Set-OMEConfiguration -Identity "OME Configuration" -SocialIdSignIn $true
   ```

## <a name="managing-the-use-of-one-time-pass-codes-for-signing-in-to-the-office-365-message-encryption-portal"></a>Office 365 메시지 암호화 포털에 로그인 하기 위한 1 회 통과 코드 사용 관리

기본적으로 OME에서 암호화 된 메시지를 받는 사람이 Outlook을 사용 하지 않는 경우에는 받는 사람이 사용 하는 계정에 관계 없이 받는 사람에 게 메시지를 읽을 수 있는 제한 된 웹 보기 링크가 수신 됩니다. 여기에는 1 회 통과 코드가 포함 됩니다. 관리자는 OME 포털에 로그인 하는 데 일회성 통과 코드를 사용할 수 있는지 여부를 관리할 수 있습니다.
  
### <a name="to-manage-whether-or-not-one-time-pass-codes-are-generated-for-ome"></a>OME에 대해 1 회 가공 패스 코드가 생성 되는지 여부를 관리 하려면
  
1. Office 365 조직에서 전역 관리자 권한이 있는 회사 또는 학교 계정을 사용 하는 경우 Windows PowerShell 세션을 시작 하 고 Exchange Online에 연결 합니다. 자세한 내용은 [Exchange Online PowerShell에 연결을](https://aka.ms/exopowershell)참조 하십시오.

2. OTPEnabled 매개 변수를 사용 하 여 set-omeconfiguration cmdlet을 실행 합니다.

   ```powershell
   Set-OMEConfiguration -Identity <"OMEConfigurationIdParameter "> -OTPEnabled <$true|$false>
   ```

   예를 들어, 1 회 통과 코드를 사용 하지 않도록 설정 합니다.

   ```powershell
   Set-OMEConfiguration -Identity "OME Configuration" -OTPEnabled $false
   ```

   1 회 통과 코드를 사용 하도록 설정 하려면:

   ```powershell
   Set-OMEConfiguration -Identity "OME Configuration" -OTPEnabled $true
   ```

## <a name="managing-the-display-of-the-protect-button-in-outlook-on-the-web"></a>웹용 Outlook에서 보호 단추 표시 관리

기본적으로 OME를 설정 해도 웹용 Outlook의 **보호** 단추는 사용할 수 없습니다. 관리자는이 단추를 최종 사용자에 게 표시할지 여부를 관리할 수 있습니다.
  
### <a name="to-manage-whether-or-not-the-protect-button-appears-in-outlook-on-the-web"></a>웹에서 Outlook에 보호 단추가 표시 되는지 여부를 관리 하려면
  
1. Office 365 조직에서 전역 관리자 권한이 있는 회사 또는 학교 계정을 사용 하는 경우 Windows PowerShell 세션을 시작 하 고 Exchange Online에 연결 합니다. 자세한 내용은 [Exchange Online PowerShell에 연결을](https://aka.ms/exopowershell)참조 하십시오.

2. -SimplifiedClientAccessEnabled 매개 변수를 사용 하 여 irmconfiguration cmdlet을 실행 합니다.

   ```powershell
   Set-IRMConfiguration -SimplifiedClientAccessEnabled <$true|$false>
   ```

   예를 들어 **보호** 단추를 사용 하지 않으려면 다음을 수행 합니다.

   ```powershell
   Set-IRMConfiguration -SimplifiedClientAccessEnabled $false
   ```

   **보호** 단추를 사용 하도록 설정 하려면:

   ```powershell
   Set-IRMConfiguration -SimplifiedClientAccessEnabled $true
   ```

## <a name="enable-service-side-decryption-of-email-messages-for-ios-mail-app-users"></a>iOS 메일 앱 사용자에 대 한 전자 메일 메시지의 서비스 쪽 암호 해독을 사용 하도록 설정

iOS 메일 앱은 Office 365 메시지 암호화로 보호 된 메시지의 암호를 해독할 수 없습니다. Office 365 관리자는 iOS 메일 앱으로 배달 되는 메시지에 대해 서비스 쪽 암호 해독을 적용할 수 있습니다. 이 작업을 수행 하도록 선택 하면 서비스에서 암호 해독 된 메시지 복사본을 iOS 장치로 보냅니다. 메시지가 클라이언트 장치에 해독 되어 저장 됩니다. 또한 iOS 메일 앱이 사용자에 게 클라이언트 쪽 사용 권한을 적용 하지 않더라도 사용 권한에 대 한 정보도 유지 됩니다. 즉, 사용자가 원래 사용 권한을 갖고 있지 않은 경우에도 메시지를 복사 하거나 인쇄할 수 있습니다. 그러나 사용자가 Office 365 메일 서버가 필요한 작업 (예: 메시지 전달)을 완료 하려고 하면 사용자가 원래 사용 권한을 갖고 있지 않은 경우 서버에서 해당 작업을 허용 하지 않습니다. 그러나 최종 사용자는 iOS 메일 응용 프로그램의 다른 계정에서 메시지를 전달 하 여 사용 제한을 전달 하지 않을 수 있습니다. 메일에 대 한 서비스 쪽 암호 해독을 설정 하는지 여부에 관계 없이 암호화 및 권한으로 보호 되는 메일에 대 한 모든 첨부 파일 iOS 메일 앱에서 볼 수 없습니다.
  
암호 해독 된 메시지를 iOS 메일 앱 사용자에 게 보내도록 허용 하지 않도록 선택 하면 사용자에 게 메시지를 볼 수 있는 권한이 없다는 메시지가 표시 됩니다. 기본적으로 전자 메일 메시지의 서비스 쪽 암호 해독이 사용 되도록 설정 되지 않습니다.
  
자세한 내용과 클라이언트 환경의 보기에 대 한 자세한 내용은 [iPhone 또는 iPad에서 암호화 된 메시지 보기](https://support.office.com/article/4d631321-0d26-4bcc-a483-d294dd0b1caf)를 참조 하세요.
  
### <a name="to-manage-whether-or-not-ios-mail-app-users-can-view-messages-protected-by-office-365-message-encryption"></a>iOS 메일 앱 사용자가 Office 365 메시지 암호화로 보호 된 메시지를 볼 수 있는지 여부를 관리 하려면
  
1. Office 365 조직에서 전역 관리자 권한이 있는 회사 또는 학교 계정을 사용 하는 경우 Windows PowerShell 세션을 시작 하 고 Exchange Online에 연결 합니다. 자세한 내용은 [Exchange Online PowerShell에 연결을](https://aka.ms/exopowershell)참조 하십시오.

2. AllowRMSSupportForUnenlightenedApps 매개 변수를 사용 하 여 ActiveSyncOrganizations cmdlet을 실행 합니다.

   ```powershell
   Set-ActiveSyncOrganizationSettings -AllowRMSSupportForUnenlightenedApps <$true|$false>
   ```

   예를 들어 메시지가 iOS 메일 응용 프로그램과 같은 unenlightened 앱으로 전송 되기 전에 암호를 해독 하도록 서비스를 구성 하려면 다음을 수행 합니다.

   ```powershell
   Set-ActiveSyncOrganizationSettings -AllowRMSSupportForUnenlightenedApps $true
   ```

   또는 암호화 되지 않은 메시지를 unenlightened 앱으로 보내지 않도록 서비스를 구성 하려면 다음을 수행 합니다.

   ```powershell
   Set-ActiveSyncOrganizationSettings -AllowRMSSupportForUnenlightenedApps $false
   ```

## <a name="enable-service-side-decryption-of-email-attachments-for-web-browser-mail-clients"></a>웹 브라우저 메일 클라이언트에 대 한 전자 메일 첨부 파일의 서비스 쪽 암호 해독을 사용 하도록 설정

일반적으로 Office 365 메시지 암호화를 사용 하면 첨부 파일이 자동으로 암호화 됩니다. Office 365 관리자는 사용자가 웹 브라우저에서 다운로드 하는 전자 메일 첨부 파일에 대해 서비스 쪽 암호 해독을 적용할 수 있습니다.
  
이 작업을 선택 하면 서비스에서 암호 해독 된 파일 복사본을 장치로 보냅니다. 메시지가 계속 암호화 됩니다. 또한 전자 메일 첨부 파일은 브라우저가 클라이언트 쪽 사용 권한을 사용자에 게 적용 하지 않더라도 사용 권한에 대 한 정보를 유지 합니다. 즉, 사용자가 원래 사용 권한을 갖고 있지 않은 경우에도 전자 메일 첨부 파일을 복사 하거나 인쇄할 수 있습니다. 그러나 사용자가 Office 365 메일 서버가 필요한 작업 (예: 첨부 파일 전달)을 완료 하려고 하면 사용자가 원래 사용 권한을 갖고 있지 않은 경우 서버에서 해당 작업을 허용 하지 않습니다.
  
첨부 파일에 대 한 서비스 쪽 암호 해독을 설정 하는지 여부에 관계 없이 암호화 및 권한으로 보호 되는 메일에 대 한 모든 첨부 파일을 iOS 메일 앱에서 볼 수 없습니다.
  
해독 된 전자 메일 첨부 파일 (기본값)을 허용 하지 않도록 선택 하면 사용자에 게 첨부 파일을 볼 수 있는 권한이 없다는 메시지가 표시 됩니다.
  
Office 365에서 암호화 전용 옵션을 사용 하 여 전자 메일 첨부 파일에 대 한 암호화를 구현 하는 방법에 대 한 자세한 내용은 [전자 메일에 대 한 암호화 전용 옵션](https://docs.microsoft.com/azure/information-protection/deploy-use/configure-usage-rights#encrypt-only-option-for-emails) 을 참조 하십시오.
  
### <a name="to-manage-whether-or-not-email-attachments-are-decrypted-on-download-from-a-web-browser"></a>웹 브라우저에서 전자 메일 첨부 파일을 다운로드 하 여 암호를 해독 하는지 여부를 관리 하려면
  
1. Office 365 조직에서 전역 관리자 권한이 있는 회사 또는 학교 계정을 사용 하는 경우 Windows PowerShell 세션을 시작 하 고 Exchange Online에 연결 합니다. 자세한 내용은 [Exchange Online PowerShell에 연결을](https://aka.ms/exopowershell)참조 하십시오.

2. DecryptAttachmentFromPortal 매개 변수를 사용 하 여 Set-irmconfiguration cmdlet을 실행 합니다.

   ```powershell
   Set-IRMConfiguration -DecryptAttachmentFromPortal <$true|$false>
   ```

   예를 들어 사용자가 웹 브라우저에서 전자 메일 첨부 파일을 다운로드할 때 암호를 해독 하도록 서비스를 구성 하려면 다음을 수행 합니다.

   ```powershell
   Set-IRMConfiguration -DecryptAttachmentFromPortal $true
   ```

   암호화 된 전자 메일 첨부 파일을 다운로드 하는 동안 남길 수 있도록 서비스를 구성 하려면 다음을 수행 합니다.

   ```powershell
   Set-IRMConfiguration -DecryptAttachmentFromPortal $false
   ```

## <a name="customizing-the-appearance-of-email-messages-and-the-ome-portal"></a>전자 메일 메시지 및 OME 포털의 모양 사용자 지정

조직에 대해 OME를 사용자 지정 하는 방법에 대 한 자세한 내용은 [암호화 된 메시지에 조직의 브랜드 추가](add-your-organization-brand-to-encrypted-messages.md)를 참조 하세요.
  
## <a name="disabling-the-new-capabilities-for-ome"></a>OME의 새 기능을 사용 하지 않도록 설정

OME에 대 한 새로운 기능을 사용 하지 않도록 설정 하는 것은 쉽지 않은 일입니다. 먼저 새 OME 기능을 사용 하 여 만든 메일 흐름 규칙을 제거 해야 합니다. 메일 흐름 규칙을 제거 하는 방법에 대 한 자세한 내용은 [메일 흐름 규칙 관리](https://technet.microsoft.com/library/jj657505%28v=exchg.150%29.aspx)를 참조 하십시오. 그런 다음 Exchange Online PowerShell에서 다음 단계를 완료 합니다.
  
### <a name="to-disable-the-new-capabilities-for-ome"></a>OME에 대 한 새 기능을 사용 하지 않도록 설정 하려면
  
1. Office 365 조직에서 전역 관리자 권한이 있는 회사 또는 학교 계정을 사용 하는 경우 Windows PowerShell 세션을 시작 하 고 Exchange Online에 연결 합니다. 자세한 내용은 [Exchange Online PowerShell에 연결을](https://aka.ms/exopowershell)참조 하십시오.

2. 웹용 Outlook에서 **보호** 단추를 사용 하도록 설정한 경우 SimplifiedClientAccessEnabled 매개 변수를 사용 하 여 Set-irmconfiguration cmdlet을 실행 하 여 사용 하지 않도록 설정 합니다. 그렇지 않으면이 단계를 건너뜁니다.

   ```powershell
   Set-IRMConfiguration -SimplifiedClientAccessEnabled $false
   ```

3. AzureRMSLicensingEnabled 매개 변수를 false로 설정 하 고 OME의 새 기능을 사용 하지 않도록 설정 합니다.

   ```powershell
   Set-IRMConfiguration -AzureRMSLicensingEnabled $false
   ```
