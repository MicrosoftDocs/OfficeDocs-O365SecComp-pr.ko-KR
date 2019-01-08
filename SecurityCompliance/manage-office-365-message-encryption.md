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
ms.openlocfilehash: 460ac0bba4d10fe8bef896a23a20f74527f031b2
ms.sourcegitcommit: bd1762ccf63c7d2ad8b49a936115171c72fb2c0f
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/08/2019
ms.locfileid: "27750057"
---
# <a name="manage-office-365-message-encryption"></a>Office 365 메시지 암호화 관리

설정을를 Office 365 메시지 암호화 OME ()을 완료 한 후 다양 한 방법으로에서 배포의 구성을 사용자 지정할 수 있습니다. 등을 1 회 암호가 하 고, 웹, 등의 Outlook에서 **암호로 보호** 단추를 표시 여부를 구성할 수 있습니다. 이 문서의 작업에 설명 방법입니다. 
  
||
|:-----|
|이 문서는 Office 365 메시지 암호화에 대 한 문서를 더 큰 시리즈의 일부입니다. 이 문서는 관리자 및 IT 전문가 위한 것입니다. 방금 경우 보내거나 암호화 된 메시지를 받는 방법에 대 한 정보에 대 한 자세한 내용은 [Office 365 메시지 암호화 OME ()](ome.md) 의 문서 목록을 참조 하 고 요구 사항에 가장 적합 한 문서를 찾습니다. |

## <a name="managing-whether-google-yahoo-and-microsoft-account-recipients-can-use-these-accounts-to-sign-in-to-the-office-365-message-encryption-portal"></a>Google, yahoo 및 Microsoft 계정 받는 사람에 게 이러한 계정을 사용 하 여 Office 365 메시지 암호화 포털에 로그인 할 수 있는지 여부를 관리 합니다.

기본적으로 새 Office 365 메시지 암호화 기능을 설정 하는 경우 조직의 사용자가 메시지를 보낼 수는 Office 365 조직 외부의 받는 사람에 게 있습니다. 받는 사람이 공유 ID를 사용 하 여 OME 포털에 로그인 할 수 받는 Google 계정, yahoo 계정 또는 Microsoft 계정 같은 *공유 ID* 를 사용 하는 경우 원할 경우 OME 포털에 로그인 하려면 공유 Id를 사용 하 여 받는 사람을 사용할 수 없도록 선택할 수 있습니다. 
  
### <a name="to-manage-whether-or-not-to-allow-recipients-to-use-social-ids-to-sign-in-to-the-ome-portal"></a>OME 포털에 로그인 하려면 공유 Id를 사용 하 여 받는 사람에 게 허용 여부를 관리 하려면
  
1. [원격 PowerShell을 사용 하 여 온라인 Exchange에 연결](http://technet.microsoft.com/library/jj984289%28v=exchg.150%29.aspx)합니다.

2. 다음과 같이 SocialIdSignIn 매개 변수와 함께 Set-omeconfiguration cmdlet를 실행 합니다.

  ```
  Set-OMEConfiguration -Identity <"OMEConfigurationIdParameter "> -SocialIdSignIn <$true | $false>
  ```

  예: 공유 Id를 사용 하지 않도록 설정 합니다.
  
  ```
  Set-OMEConfiguration -Identity "OME Configuration" -SocialIdSignIn $false
  ```

  공유 Id 수 있도록 합니다.

  ```
  Set-OMEConfiguration -Identity "OME Configuration" -SocialIdSignIn $true
  ```

## <a name="managing-the-use-of-one-time-pass-codes-for-signing-in-to-the-office-365-message-encryption-portal"></a>1 회 암호가 사용 하 여 Office 365 메시지 암호화 포털에 로그인 하는 것에 대 한 관리

기본적으로 OME 하 여 암호화 된 메시지의 받는 사람으로 받는 사람을 사용 하는 계정에 관계 없이 Outlook을 사용 하지 않는 경우 받는 메시지를 읽을 수 있도록 하는 제한 된 기간 동안 웹 보기 링크를 받습니다. 1 회 암호가 포함 됩니다. 관리자로 서 1 회 암호가 OME 포털에 로그인을 사용할 수 있는지 여부를 관리할 수 있습니다.
  
### <a name="to-manage-whether-or-not-one-time-pass-codes-are-generated-for-ome"></a>1 회 암호가 OME에 대해 생성 되는 여부를 관리 하려면
  
1. Office 365 조직에 대 한 전역 관리자 권한이 있는 작업이 나 교육용 계정을 사용 하는 Windows PowerShell 세션을 시작 하 고 Exchange Online에 연결 합니다. 자세한 내용은 [Connect to Exchange Online PowerShell를](https://aka.ms/exopowershell)참조 하십시오.

2. OTPEnabled 매개 변수와 함께 Set-omeconfiguration cmdlet을 실행 합니다.

   ```Set-OMEConfiguration -Identity <"OMEConfigurationIdParameter "> -OTPEnabled <$true|$false>```

   예: 일회용 암호 코드를 사용 하지 않도록 설정 합니다.

   ```Set-OMEConfiguration -Identity "OME Configuration" -OTPEnabled $false```

   1 회 암호가 수 있도록 합니다.

   ```Set-OMEConfiguration -Identity "OME Configuration" -OTPEnabled $true```

## <a name="managing-the-display-of-the-protect-button-in-outlook-on-the-web"></a>웹에 있는 Outlook에서 암호로 보호 단추를 표시 하는 관리

기본적으로 웹에 있는 Outlook에서 **암호로 보호** 단추는 사용할 수 없는 OME를 설정 하는 경우. 관리자로 서 최종 사용자에 게이 단추를 표시할 것인지 여부를 관리할 수 있습니다. 
  
### <a name="to-manage-whether-or-not-the-protect-button-appears-in-outlook-on-the-web"></a>관리 여부는 Protect 단추 표시 하는 Outlook에서 웹에
  
1. Office 365 조직에 대 한 전역 관리자 권한이 있는 작업이 나 교육용 계정을 사용 하는 Windows PowerShell 세션을 시작 하 고 Exchange Online에 연결 합니다. 자세한 내용은 [Connect to Exchange Online PowerShell를](https://aka.ms/exopowershell)참조 하십시오.

2. -SimplifiedClientAccessEnabled 매개 변수와 함께 Set-irmconfiguration cmdlet을 실행 합니다.

   ```Set-IRMConfiguration -SimplifiedClientAccessEnabled <$true|$false>```

   예: **Protect** 단추를 사용 하지 않도록 설정 합니다.

   ```Set-IRMConfiguration -SimplifiedClientAccessEnabled $false```

   단추를 사용 하도록 **암호로 보호** :

   ```Set-IRMConfiguration -SimplifiedClientAccessEnabled $true```

## <a name="enable-service-side-decryption-of-email-messages-for-ios-mail-app-users"></a>IOS 메일 앱 사용자에 대 한 전자 메일 메시지의 서비스 측 암호 해독을 사용 하도록 설정

IOS 메일 앱 Office 365 메시지 암호화로 보호 되는 메시지를 해독할 수 없습니다. Office 365 관리자로 iOS 메일 앱에 전달 된 메시지에 대 한 서비스 측 암호 해독을 적용할 수 있습니다. 이 작업을 수행 하려는 경우 서비스는 iOS 장치에 메시지의 암호가 해독 된 복사본을 보냅니다. 메시지는 클라이언트 장치에서 암호를 해독 저장 됩니다. 또한 메시지 iOS 메일 앱 클라이언트쪽 사용 권한을 사용자에 게는 적용 되지 않습니다 하는 경우에 사용 권한에 대 한 정보를 유지 합니다. 즉, 사용자가 복사 하거나 그렇게 권한을 원래가지고 있지 않은 경우에 메시지를 인쇄할 수 있습니다. 그러나 사용자가 Office 365 메일 서버는 메시지를 전달 하는 예: 필요한 작업을 완료 하려고 하는 경우 서버는 허용 하지 작업 사용자가 원래 그렇게 수 있는 사용 권한이 없는 경우. 그러나 최종 사용자를 해결할 수 제한 사항 전달 하지 않음 메일의 서비스 측 암호 해독을 설정 하는 여부에 관계 없이 자신의 iOS 메일 응용 프로그램의 다른 계정에서 메시지를 전달 하 여, 모든 첨부 파일을 암호화 및 권한 메일 보호 iOS 메일 응용 프로그램에서 볼 수 없습니다.
  
해독 된 메시지를 보낼 수를 허용 하지 않도록 선택 하는 경우 iOS 메일 앱 사용자, 사용자가 메시지를 볼 수 있는 권한이 없더라도 없다는 메시지를 수신 합니다. 기본적으로 전자 메일 메시지의 서비스 측 암호 해독을 사용할 수 없습니다.
  
자세한 내용 및 클라이언트 환경에서의 보기에는 "[iPhone 또는 iPad에서 암호화 된 메시지를 보려면](https://support.office.com/article/4d631321-0d26-4bcc-a483-d294dd0b1caf#iOSEncryptedMail)" [iPhone 또는 iPad에서 암호화 된 메시지 보기](https://support.office.com/article/4d631321-0d26-4bcc-a483-d294dd0b1caf)에서 섹션을 참조 합니다.
  
### <a name="to-manage-whether-or-not-ios-mail-app-users-can-view-messages-protected-by-office-365-message-encryption"></a>IOS 메일 앱 사용자 여부를 관리 하려면 Office 365 메시지 암호화로 보호 된 메시지를 볼 수 있습니다.
  
1. Office 365 조직에 대 한 전역 관리자 권한이 있는 작업이 나 교육용 계정을 사용 하는 Windows PowerShell 세션을 시작 하 고 Exchange Online에 연결 합니다. 자세한 내용은 [Connect to Exchange Online PowerShell를](https://aka.ms/exopowershell)참조 하십시오.

2. AllowRMSSupportForUnenlightenedApps 매개 변수와 함께 집합 ActiveSyncOrganizations cmdlet을 실행 합니다.

   ```Set-ActiveSyncOrganizationSettings -AllowRMSSupportForUnenlightenedApps <$true|$false>```

   등 unenlightened 앱에 보낸 메시지의 암호 해독에 서비스를 구성 하려면 다음과 같이 iOS 메일 앱:

   ```Set-ActiveSyncOrganizationSettings -AllowRMSSupportForUnenlightenedApps $true```

   또는 unenlightened 응용 프로그램을 암호가 해독 된 메시지를 보내지 서비스를 구성 하려면:

   ```Set-ActiveSyncOrganizationSettings -AllowRMSSupportForUnenlightenedApps $false```

## <a name="enable-service-side-decryption-of-email-attachments-for-web-browser-mail-clients"></a>웹 브라우저 메일 클라이언트에 대 한 전자 메일 첨부 파일의 서비스 측 암호 해독을 사용 하도록 설정

일반적으로 Office 365 메시지 암호화를 사용 하면 첨부 파일 자동으로 암호화 됩니다. Office 365 관리자 권한으로 사용자가 웹 브라우저에서 다운로드 하는 전자 메일 첨부 파일에 대 한 서비스 측 암호 해독을 적용할 수 있습니다. 
  
이 작업을 수행 하려는 경우 서비스는 장치에 파일의 암호가 해독 된 복사본을 보냅니다. 메시지는 여전히 암호화 됩니다. 또한 전자 메일 첨부 파일 브라우저 클라이언트쪽 사용 권한을 사용자에 게는 적용 되지 않습니다 하는 경우에 사용 권한에 대 한 정보를 유지 합니다. 즉, 사용자가 복사 하거나 그렇게 권한을 원래가지고 있지 않은 경우에 전자 메일 첨부 파일을 인쇄할 수 있습니다. 그러나 사용자가 첨부 파일을 전달 하는 등의 Office 365 메일 서버를 필요로 하는 작업을 완료 하려고 하는 경우 서버는 허용 하지 작업 사용자가 원래 그렇게 수 있는 사용 권한이 없는 경우.
  
첨부 파일의 서비스 측 암호 해독 설정 여부에 관계 없이 모든 첨부 파일을 암호화 하 고 iOS 메일 앱의 권한 제한 된 메일을 볼 수 없습니다.
  
기본 인 암호가 해독 된 전자 메일 첨부 파일을 허용 하지 않도록 선택 하는 경우 사용자가 첨부 파일을 볼 수 있는 권한이 없더라도 없다는 메시지를 수신 합니다.
  
Office 365에서 전자 메일 및 전자 메일 첨부 파일 암호화 전용 옵션에 대 한 암호화를 구현 하는 방법에 대 한 자세한 내용은 참조 [전자 메일에 대 한 암호화 전용 옵션.](https://docs.microsoft.com/azure/information-protection/deploy-use/configure-usage-rights#encrypt-only-option-for-emails)
  
### <a name="to-manage-whether-or-not-email-attachments-are-decrypted-on-download-from-a-web-browser"></a>관리 여부 전자 메일 첨부 파일의 암호 해독에 웹 브라우저에서 다운로드
  
1. Office 365 조직에 대 한 전역 관리자 권한이 있는 작업이 나 교육용 계정을 사용 하는 Windows PowerShell 세션을 시작 하 고 Exchange Online에 연결 합니다. 자세한 내용은 [Connect to Exchange Online PowerShell를](https://aka.ms/exopowershell)참조 하십시오.

2. DecryptAttachmentFromPortal 매개 변수와 함께 Set-irmconfiguration cmdlet을 실행 합니다.

   ```Set-IRMConfiguration -DecryptAttachmentFromPortal <$true|$false>```

   예 때 사용자의 전자 메일 첨부 파일의 암호를 해독 하는 서비스를 구성 하려면을 다운로드 하는 웹 브라우저에서:

   ```Set-IRMConfiguration -DecryptAttachmentFromPortal $true```

   서비스를 구성 하려면 다운로드 시로 암호화 된 전자 메일 첨부 파일을 유지 하도록 합니다.

   ```Set-IRMConfiguration -DecryptAttachmentFromPortal $false```

## <a name="customizing-the-appearance-of-email-messages-and-the-ome-portal"></a>전자 메일 메시지와 OME 포털의 모양을 사용자 지정

조직에 대 한 OME를 사용자 지정할 수는 방법에 대 한 자세한 내용은 [조직의 브랜드를 암호화 된 메시지에 추가](add-your-organization-brand-to-encrypted-messages.md)참조 하십시오.
  
## <a name="disabling-the-new-capabilities-for-ome"></a>OME에 대 한 새로운 기능을 사용 하지 않도록 설정

바랍니다 하는 경우 필요한, 작업은 매우 간단 OME에 대 한 새로운 기능을 사용 하지 않도록 설정 하지만,를 제공 하지 않습니다. 첫째, 규칙을 제거 하려면 모든 메일 흐름 만들었고 새 OME 기능을 사용 하는 필요 합니다. 메일 흐름 규칙을 제거 하는 방법에 대 한 정보, [메일 흐름 규칙 관리를](https://technet.microsoft.com/library/jj657505%28v=exchg.150%29.aspx)참조 하십시오. 그런 다음, 다음이 단계를 완료 Exchange 온라인 PowerShell 합니다.
  
### <a name="to-disable-the-new-capabilities-for-ome"></a>OME에 대 한 새로운 기능을 사용 하지 않도록 설정 하려면
  
1. Office 365 조직에 대 한 전역 관리자 권한이 있는 작업이 나 교육용 계정을 사용 하는 Windows PowerShell 세션을 시작 하 고 Exchange Online에 연결 합니다. 자세한 내용은 [Connect to Exchange Online PowerShell를](https://aka.ms/exopowershell)참조 하십시오.

2. 웹에 있는 Outlook에서 **암호로 보호** 단추를 사용 하도록 설정한 경우 SimplifiedClientAccessEnabled 매개 변수와 함께 Set-irmconfiguration cmdlet을 실행 하 여 비활성화 합니다. 그렇지 않은 경우이 단계를 건너뜁니다.

   ```Set-IRMConfiguration -SimplifiedClientAccessEnabled $false```

3. OME에 대 한 새로운 기능을 사용 하지 않도록 설정 false로 설정 하는 AzureRMSLicensingEnabled 매개 변수와 함께 Set-irmconfiguration cmdlet을 실행 하 여:

   ```Set-IRMConfiguration -AzureRMSLicensingEnabled $false```
