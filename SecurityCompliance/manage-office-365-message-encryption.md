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
# <a name="manage-office-365-message-encryption"></a>Office 365 메시지 암호화 관리

Office 365 메시지 암호화 (OME) 설정을 완료 한 후에는 여러 가지 방법으로 배포 구성을 사용자 지정할 수 있습니다. 예를 들어, 웹의 Outlook에서 1 회 통과, **암호화** 단추를 표시할 것인지 여부를 구성할 수 있습니다. 이 문서의 작업에서는 이러한 방법을 설명 합니다.

## <a name="manage-whether-google-yahoo-and-microsoft-account-recipients-can-use-these-accounts-to-sign-in-to-the-office-365-message-encryption-portal"></a>Google, Yahoo 및 Microsoft 계정 받는 사람이 이러한 계정을 사용 하 여 Office 365 메시지 암호화 포털에 로그인 할 수 있는지 여부를 관리 합니다.

새 Office 365 메시지 암호화 기능을 설정 하면 조직의 사용자가 Office 365 조직 외부에 있는 받는 사람에 게 메시지를 보낼 수 있습니다. 받는 사람이 Google 계정, Yahoo account 또는 Microsoft 계정과 같은 *공유 id* 를 사용 하는 경우 받는 사람은 공유 ID로 OME 포털에 로그인 할 수 있습니다. 원하는 경우 받는 사람이 공유 Id를 사용 하 여 OME 포털에 로그인 하는 것을 허용 하지 않도록 선택할 수 있습니다.
  
### <a name="to-manage-whether-recipients-can-use-social-ids-to-sign-in-to-the-ome-portal"></a>받는 사람이 공유 Id를 사용 하 여 OME 포털에 로그인 할 수 있는지 여부를 관리 하려면
  
1. [원격 PowerShell을 사용 하 여 Exchange Online에 연결](http://technet.microsoft.com/library/jj984289%28v=exchg.150%29.aspx)합니다.

2. 다음과 같이, Set-omeconfiguration cmdlet을 사회 Alidsignin 매개 변수를 사용 하 여 실행 합니다.

   ```powershell
   Set-OMEConfiguration -Identity <"OMEConfigurationIdParameter"> -SocialIdSignIn <$true|$false>
   ```

   예를 들어, 공유 Id를 사용 하지 않도록 설정 하려면

   ```powershell
   Set-OMEConfiguration -Identity "OME Configuration" -SocialIdSignIn $false
   ```

   공유 Id를 사용 하도록 설정 하려면:

   ```powershell
   Set-OMEConfiguration -Identity "OME Configuration" -SocialIdSignIn $true
   ```

## <a name="manage-the-use-of-one-time-pass-codes-for-the-office-365-message-encryption-portal"></a>Office 365 메시지 암호화 포털에 대해 1 회 통과 코드 사용 관리

받는 사람이 사용 하는 계정에 관계 없이 OME에서 암호화 된 메시지를 받는 사람이 Outlook을 사용 하지 않는 경우에는 받는 사람에 게 메시지를 읽을 수 있는 제한 된 웹 보기 링크가 수신 됩니다. 이 링크에는 1 회 통과 코드가 포함 되어 있습니다. 관리자는 받는 사람이 1 회 통과 코드를 사용 하 여 OME 포털에 로그인 할 수 있는지 결정할 수 있습니다.
  
### <a name="to-manage-whether-ome-generates-one-time-pass-codes"></a>OME에서 1 회 통과 코드를 생성할지 여부를 관리 하려면
  
1. Office 365 조직에서 전역 관리자 권한이 있는 회사 또는 학교 계정을 사용 하 고, Windows PowerShell 세션을 시작 하 고, Exchange Online에 연결 합니다. 자세한 내용은 [Exchange Online PowerShell에 연결을](https://aka.ms/exopowershell)참조 하십시오.

2. OTPEnabled 매개 변수를 사용 하 여 Set-omeconfiguration cmdlet을 실행 합니다.

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

## <a name="manage-the-display-of-the-encrypt-button-in-outlook-on-the-web"></a>웹용 Outlook에서 암호화 단추 표시 관리

관리자는이 단추를 최종 사용자에 게 표시할지 여부를 관리할 수 있습니다.
  
### <a name="to-manage-whether-the-encrypt-button-appears-in-outlook-on-the-web"></a>웹에서 Outlook에 암호화 단추를 표시할지 여부를 관리 하려면
  
1. Office 365 조직에서 전역 관리자 권한이 있는 회사 또는 학교 계정을 사용 하 고, Windows PowerShell 세션을 시작 하 고, Exchange Online에 연결 합니다. 자세한 내용은 [Exchange Online PowerShell에 연결을](https://aka.ms/exopowershell)참조 하십시오.

2. -SimplifiedClientAccessEnabled 매개 변수를 사용 하 여 IRMConfiguration cmdlet을 실행 합니다.

   ```powershell
   Set-IRMConfiguration -SimplifiedClientAccessEnabled <$true|$false>
   ```

   예를 들어 **암호화** 단추를 사용 하지 않도록 설정 하려면 다음을 수행 합니다.

   ```powershell
   Set-IRMConfiguration -SimplifiedClientAccessEnabled $false
   ```

   **암호화** 단추를 사용 하도록 설정 하려면:

   ```powershell
   Set-IRMConfiguration -SimplifiedClientAccessEnabled $true
   ```

## <a name="enable-service-side-decryption-of-email-messages-for-ios-mail-app-users"></a>IOS 메일 앱 사용자에 대 한 전자 메일 메시지의 서비스 쪽 암호 해독을 사용 하도록 설정

IOS 메일 앱은 Office 365 메시지 암호화로 보호 된 메시지의 암호를 해독할 수 없습니다. Office 365 관리자는 iOS 메일 앱으로 배달 되는 메시지에 대해 서비스 쪽 암호 해독을 적용할 수 있습니다. 서비스 쪽 암호 해독을 사용 하도록 선택 하면 서비스에서 암호 해독 된 메시지 복사본을 iOS 장치로 보냅니다. 클라이언트 장치는 암호 해독 된 메시지의 복사본을 저장 합니다. 또한 iOS 메일 앱이 사용자에 게 클라이언트 쪽 사용 권한을 적용 하지 않더라도 사용 권한에 대 한 정보도 유지 됩니다. 사용자는 원래 해당 권한이 없는 경우에도 메시지를 복사 하거나 인쇄할 수 있습니다. 그러나 사용자가 메시지 전달 등의 Office 365 메일 서버가 필요한 작업을 완료 하려고 하면 사용자가 원래 사용 권한을 갖고 있지 않은 경우 서버에서 해당 작업을 허용 하지 않습니다. 그러나 최종 사용자는 iOS 메일 응용 프로그램 내에서 다른 계정 으로부터 메시지를 전달 하 여 "전달 금지" 사용 제한을 해결할 수 있습니다. 메일에 대 한 서비스 쪽 암호 해독을 설정 하는지 여부에 관계 없이 암호화 및 권한으로 보호 되는 전자 메일의 첨부 파일은 iOS 메일 앱에서 볼 수 없습니다.
  
암호 해독 된 메시지를 iOS 메일 앱 사용자에 게 보내도록 허용 하지 않도록 선택 하면 사용자에 게 메시지를 볼 수 있는 권한이 없다는 메시지가 표시 됩니다. 기본적으로 전자 메일 메시지의 서비스 쪽 암호 해독이 사용 되도록 설정 되지 않습니다.
  
자세한 내용과 클라이언트 환경의 보기에 대 한 자세한 내용은 [iPhone 또는 iPad에서 암호화 된 메시지 보기](https://support.office.com/article/4d631321-0d26-4bcc-a483-d294dd0b1caf)를 참조 하세요.
  
### <a name="to-manage-whether-ios-mail-app-users-can-view-messages-protected-by-office-365-message-encryption"></a>IOS 메일 앱 사용자가 Office 365 메시지 암호화로 보호 된 메시지를 볼 수 있는지 여부를 관리 하려면
  
1. Office 365 조직에서 전역 관리자 권한이 있는 회사 또는 학교 계정을 사용 하 고, Windows PowerShell 세션을 시작 하 고, Exchange Online에 연결 합니다. 자세한 내용은 [Exchange Online PowerShell에 연결을](https://aka.ms/exopowershell)참조 하십시오.

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
  
서비스 쪽 암호 해독을 사용 하면 서비스에서 암호 해독 된 파일 복사본을 장치로 보냅니다. 메시지가 계속 암호화 됩니다. 또한 브라우저가 클라이언트 쪽 사용 권한을 사용자에 게 적용 하지 않더라도 전자 메일 첨부 파일은 사용 권한에 대 한 정보를 유지 합니다. 사용자는 원래 사용 권한을 갖고 있지 않은 경우에도 전자 메일 첨부 파일을 복사 하거나 인쇄할 수 있습니다. 그러나 사용자가 Office 365 메일 서버가 필요한 작업 (예: 첨부 파일 전달)을 완료 하려고 하면 사용자가 원래 사용 권한을 갖고 있지 않은 경우 서버에서 해당 작업을 허용 하지 않습니다.
  
사용자가 첨부 파일에 대해 서비스 쪽 암호 해독을 설정 하는지 여부에 관계 없이 iOS 메일 응용 프로그램에서 암호화 및 권한으로 보호 된 메일의 첨부 파일을 볼 수 없습니다.
  
해독 된 전자 메일 첨부 파일 (기본값)을 허용 하지 않도록 선택 하면 사용자에 게 첨부 파일을 볼 수 있는 권한이 없다는 메시지가 표시 됩니다.
  
Office 365에서 암호화 전용 옵션을 사용 하 여 전자 메일 첨부 파일에 대 한 암호화를 구현 하는 방법에 대 한 자세한 내용은 [전자 메일에 대 한 암호화 전용 옵션](https://docs.microsoft.com/azure/information-protection/deploy-use/configure-usage-rights#encrypt-only-option-for-emails) 을 참조 하십시오.
  
### <a name="to-manage-whether-email-attachments-are-decrypted-on-download-from-a-web-browser"></a>웹 브라우저에서 전자 메일 첨부 파일을 다운로드 하 여 암호를 해독 하는지 여부를 관리 하려면
  
1. Office 365 조직에서 전역 관리자 권한이 있는 회사 또는 학교 계정을 사용 하 고, Windows PowerShell 세션을 시작 하 고, Exchange Online에 연결 합니다. 자세한 내용은 [Exchange Online PowerShell에 연결을](https://aka.ms/exopowershell)참조 하십시오.

2. DecryptAttachmentFromPortal 매개 변수를 사용 하 여 Set-IRMConfiguration cmdlet을 실행 합니다.

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

## <a name="ensure-all-external-recipients-use-the-ome-portal-to-read-encrypted-mail--office-365-advanced-message-encryption-only"></a>모든 외부 받는 사람이 OME 포털을 사용 하 여 암호화 된 메일을 읽도록 확인-Office 365 Advanced Message Encryption만 해당

Office 365 고급 메시지 암호화가 있는 경우 사용자 지정 브랜딩 템플릿을 사용 하 여 받는 사람이 웹에서 Outlook 또는 Outlook을 사용 하는 대신 OME 포털에서 암호화 된 전자 메일을 읽도록 지시 하는 래퍼 메일을 받을 수 있습니다. 받는 사람이 받은 메일을 사용 하는 방법을 보다 강력 하 게 제어 하려는 경우에이 작업을 수행 하는 것이 좋습니다. 예를 들어 외부 받는 사람이 웹 포털에서 전자 메일을 볼 경우 전자 메일의 만료 날짜를 설정할 수 있으며 전자 메일을 해지할 수 있습니다. 이러한 기능은 OME 포털을 통해서만 지원 됩니다. 메일 흐름 규칙을 만들 때 암호화 옵션 및 전달 금지 옵션을 사용할 수 있습니다.

### <a name="create-a-custom-template-to-force-all-external-recipients-to-use-the-ome-portal-and-for-encrypted-email-to-be-revocable-and-expire-in-7-days"></a>모든 외부 받는 사람이 OME 포털을 사용 하 고 암호화 된 전자 메일이 7 일 후에 revocable 및 만료 되도록 하려면 사용자 지정 서식 파일을 만듭니다.

1. Office 365 조직에서 전역 관리자 권한이 있는 회사 또는 학교 계정을 사용 하 고, Windows PowerShell 세션을 시작 하 고, Exchange Online에 연결 합니다. 자세한 내용은 [Exchange Online PowerShell에 연결을](https://aka.ms/exopowershell)참조 하십시오.

2. Set-omeconfiguration cmdlet을 실행 합니다.

   ```powershell
   New-OMEConfiguration -Identity "<template name>" -ExternalMailExpiryInDays 7
   ```

   여기서 `template name` 는 Office 365 메시지 암호화 사용자 지정 브랜딩 서식 파일에 사용 하려는 이름입니다. For example,

   ```powershell
   New-OMEConfiguration -Identity "<One week expiration>" -ExternalMailExpiryInDays 7
   ```

3. New-transportrule cmdlet을 실행 합니다.

   ```powershell
   New-TransportRule -name "<mail flow rule name>" -FromScope "InOrganization" -ApplyRightsProtectionTemplate "<option name>" -ApplyRightsProtectionCustomizationTemplate "<template name>"
   ```

    여기서 각 부분이 나타내는 의미는 다음과 같습니다.

   - `mail flow rule name`은 새 메일 흐름 규칙에 사용할 이름입니다.

   - `option name`은 `Encrypt` 또는 `Do Not Forward`입니다.

   - `template name`은 사용자 지정 브랜딩 서식 파일에 지정한 이름입니다 예: `One week expiration`

   모든 외부 전자 메일을 "한 주 만료" 서식 파일로 암호화 하 고 암호화 전용 옵션을 적용 하려면 다음을 수행 합니다.

   ```powershell
   New-TransportRule -name "<All outgoing mail>" -FromScope "InOrganization" -ApplyRightsProtectionTemplate "Encrypt" -ApplyRightsProtectionCustomizationTemplate "<One week expiration>"
   ```

   모든 외부 전자 메일을 "한 주 만료" 서식 파일로 암호화 하 고 전달 금지 옵션을 적용 하려면 다음을 수행 합니다.

   ```powershell
   New-TransportRule -name "<All outgoing mail>" -FromScope "InOrganization" -ApplyRightsProtectionTemplate "Do Not Forward" -ApplyRightsProtectionCustomizationTemplate "<One week expiration>"
   ```

## <a name="customize-the-appearance-of-email-messages-and-the-ome-portal"></a>전자 메일 메시지 및 OME 포털의 모양 사용자 지정

조직에 대해 OME를 사용자 지정 하는 방법에 대 한 자세한 내용은 [암호화 된 메시지에 조직의 브랜드 추가](add-your-organization-brand-to-encrypted-messages.md)를 참조 하세요.
  
## <a name="disable-the-new-capabilities-for-ome"></a>OME의 새 기능을 사용 하지 않도록 설정

OME에 대 한 새로운 기능을 사용 하지 않도록 설정 하는 것은 쉽지 않은 일입니다. 먼저 새 OME 기능을 사용 하 여 만든 메일 흐름 규칙을 제거 해야 합니다. 메일 흐름 규칙을 제거 하는 방법에 대 한 자세한 내용은 [메일 흐름 규칙 관리](https://technet.microsoft.com/library/jj657505%28v=exchg.150%29.aspx)를 참조 하십시오. 그런 다음 Exchange Online PowerShell에서 다음 단계를 완료 합니다.
  
### <a name="to-disable-the-new-capabilities-for-ome"></a>OME에 대 한 새 기능을 사용 하지 않도록 설정 하려면
  
1. Office 365 조직에서 전역 관리자 권한이 있는 회사 또는 학교 계정을 사용 하는 경우 Windows PowerShell 세션을 시작 하 고 Exchange Online에 연결 합니다. 자세한 내용은 [Exchange Online PowerShell에 연결을](https://aka.ms/exopowershell)참조 하십시오.

2. 웹용 Outlook에서 **암호화** 단추를 사용 하도록 설정한 경우에는 SimplifiedClientAccessEnabled 매개 변수를 사용 하 여 Set-IRMConfiguration cmdlet을 실행 하 여 사용 하지 않도록 설정 합니다. 그렇지 않으면이 단계를 건너뜁니다.

   ```powershell
   Set-IRMConfiguration -SimplifiedClientAccessEnabled $false
   ```

3. AzureRMSLicensingEnabled 매개 변수를 false로 설정 하 고 OME의 새 기능을 사용 하지 않도록 설정 합니다.

   ```powershell
   Set-IRMConfiguration -AzureRMSLicensingEnabled $false
   ```
