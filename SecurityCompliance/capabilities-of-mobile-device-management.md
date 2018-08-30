---
title: Office 365의 기본 제공 모바일 장치 관리 기능
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 6/11/2018
ms.audience: Admin
ms.topic: article
f1_keywords:
- ms.o365.cc.DevicePolicySupportedDevice
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MED150
- MBS150
- MET150
ms.assetid: a1da44e5-7475-4992-be91-9ccec25905b0
description: Office 365에 대 한 모바일 장치 관리 보안을 유지 하 고 Iphone, Ipad, Androids, 조직에서 사용 되는 Windows Phone와 같은 모바일 장치를 관리할 수 있습니다. 조직의 Office 365 전자 메일 및 지원 되는 모바일 장치 및 앱에 대 한 문서에 액세스 하 고를 도난당 한 장치를 원격으로 초기화 하면 컨트롤에 도움이 되는 설정을 사용 하 여 모바일 장치 관리 정책을 만듭니다.
ms.openlocfilehash: b7200eee3b50c2fc6d3e0ea0920236d71837a88b
ms.sourcegitcommit: c31424cafbf1953f2864d7e2ceb95b329a694edb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/29/2018
ms.locfileid: "23272603"
---
# <a name="capabilities-of-built-in-mobile-device-management-for-office-365"></a>Office 365의 기본 제공 모바일 장치 관리 기능

Office 365에 대 한 모바일 장치 관리 보안을 유지 하 고 Iphone, Ipad, Androids, 조직에서 사용이 허가 된 Office 365 사용자가 사용 하는 Windows Phone와 같은 모바일 장치를 관리할 수 있습니다. 조직의 Office 365 전자 메일 및 지원 되는 모바일 장치 및 앱에 대 한 문서에 대 한 액세스 제어는 데 도움이 되는 설정을 사용 하 여 모바일 장치 관리 정책을 만들 수 있습니다. 장치를 분실 하거나 도난당, 하는 경우 조직의 중요 한 정보를 제거 하려면 장치를 원격으로 완전히 제거할 수 있습니다.
    
Office 365에 대 한 MDM에 포함 된 것 보다 더 많은 기능을 필요 합니까? Microsoft Intune에 필요한 정보를 참조: [Office 365 및 Microsoft Intune MDM 간에 선택](choose-between-mdm-and-intune.md)합니다.
  
## <a name="supported-devices"></a>지원되는 장치

MDM Office 365에 대 한를 사용 하 여 보호 하 고 다음과 같은 유형의 장치를 관리할 수 있습니다.
  
- Windows Phone 8.1 +
    
- iOS 7.1 이상 버전
    
- iPad 4 이상 버전
    
- Windows 8.1\*
    
- Windows 8.1 RT\*
    
- Windows 10\*\*
    
- Windows 10 Mobile\*\*
    
\*Windows 8.1 및 Windows 8.1 RT 장치에 대 한 액세스 제어 Exchange ActiveSync 개로 제한 됩니다.
  
\*\*Azure Active Directory에 가입 하 여 조직의 모바일 장치 관리 서비스에 등록 하는 장치가 필요 합니다.
  
조직의 사용자에 게 Office 365에 대 한 모바일 장치 관리에서 지원 하지 않는 모바일 장치를 사용 하는 경우에 조직의 데이터를 보다 안전 하 게 하려면 해당 장치에 대 한 Office 365 전자 메일에 대 한 Exchange ActiveSync 응용 프로그램 액세스를 차단 하는 것이 좋습니다. Exchange ActiveSync를 차단 하기 위한 단계: [장치 액세스 설정 관리를](manage-device-access-settings.md)참조 하십시오.
  
## <a name="access-control-for-office-365-email-and-documents"></a>Office 365 전자 메일 및 문서에 대한 액세스 제어

다양 한 유형의 다음 표에 모바일 장치에 대 한 지원 되는 앱에는 사용자가 있는 사용자의 장치에 적용 되는 새로운 모바일 장치 관리 정책을 있고 사용자는 장치를 이전에 등록 하지 않은 Office 365에 대 한 MDM에 등록 하 라는 메시지가 나타납니다. 사용자의 장치 정책에 부합 하지 않는 경우 이러한 응용 프로그램에서 Office 365 리소스에 액세스 하지 못하도록 차단 되었을 사용자 설정에 따라 어떻게 하면 정책 또는 액세스할 수 있는 있지만 Office 365 정책 위반을 보고 합니다.
  
||**Windows Phone 8.1 +**|**iOS 7.1+**|**Android 4+**|
|:-----|:-----|:-----|:-----|
|**Exchange** <br/> Exchange ActiveSync에는 기본 제공 전자 메일 및 Exchange ActiveSync 버전 14.1 이상 사용 하는 TouchDown, 같은 제 3 자 앱 포함 됩니다.  <br/> |![Exchange ActiveSync 아이콘](media/b36e36ba-88a5-4b2e-bd1d-7432b751a60c.png)Exchange ActiveSync  <br/> ![Exchange 메일 모바일 아이콘](media/5b5312b4-3bfb-4fc7-84ff-d7ab21227c10.png)Exchange 메일  <br/> |![Exchange ActiveSync 아이콘](media/b36e36ba-88a5-4b2e-bd1d-7432b751a60c.png)Exchange ActiveSync  <br/> ![iPhone 메일 모바일 아이콘](media/888bdc7a-8354-4013-a0b2-0d4432a9a92e.png)메일  <br/> |![Exchange ActiveSync 아이콘](media/b36e36ba-88a5-4b2e-bd1d-7432b751a60c.png)Exchange ActiveSync  <br/> ![Android 전자 메일 아이콘](media/20b48492-4adc-40ce-99cf-1b47bd2b389d.png)전자 메일  <br/> |
|**Office** 및 **비즈니스용 OneDrive** <br/> |지원되는 앱 없음  <br/> |![iPhone Outlook 모바일 아이콘](media/6c63112d-c10c-4040-85cc-feeccc3dd424.png)Outlook  <br/> ![iPhone OneDrive 모바일 아이콘](media/560ec187-82d9-4793-b72f-7ba595972bdc.png)OneDrive  <br/> ![iPhone Word 모바일 아이콘](media/63a3a749-1f98-402f-b211-e46b9224b655.png)Word  <br/> ![iPhone Excel 모바일 아이콘](media/5b8f62c0-96aa-4602-9ed8-f837bbf5fa9e.png)Excel  <br/> ![iPhone PowerPoint 모바일 아이콘](media/17c02dca-f60a-4d13-a610-00d576a40943.png)PowerPoint  <br/> |**휴대폰 및 태블릿:** <br/> ![Android 전화 및 태블릿 Outlook 모바일 아이콘](media/ed2a813d-f481-46e0-acc9-6422f0d16072.png)Outlook  <br/> ![Android 휴대폰 OneDrive 모바일 아이콘](media/64855d02-1684-4795-b4c5-863860f18722.png)OneDrive  <br/> ![Android Word 모바일 아이콘](media/f618fe83-b163-4680-b924-fcedc06ab4ba.png)Word  <br/> ![Android Excel 모바일 아이콘](media/659c7a5f-5797-4b47-a776-4a0c8f784c89.png)Excel  <br/> ![Android PowerPoint 모바일 아이콘](media/35b98bce-d7cb-40ce-87e3-07b9764207b1.png)PowerPoint  <br/> **휴대폰만 해당:** <br/> ![Office 모바일 모바일 아이콘](media/1aa9e978-6eb2-40aa-82da-62fb79cee313.png)Office Mobile  <br/> |
   
> [!NOTE]
>  IOS 7.1 및 그 이후 버전에 대 한 지원 iPhone 및 iPad 장치를 포함합니다. > BlackBerry 장치 관리는 Office 365에 대 한 모바일 장치 관리를 통해 지원 되지 않습니다. BlackBerry Business Cloud Services (BBCS)에서 BlackBerry 사용 하 여 BlackBerry 장치를 관리할 수 있습니다. > 사용자를 등록 하 고 없습니다 차단 또는 Office 365 SharePoint 사이트, Office Online의 문서 또는 Outlook Web App에서 전자 메일에 액세스 하는 모바일 브라우저를 사용 하는 경우 정책 위반에 대 한 보고 하 라는 메시지가 표시 되지 않습니다. 
  
다음 다이어그램은 새 장치를 가진 사용자가 Office 365에 대 한 MDM 함께 컨트롤의 액세스는 지원 되는 응용 프로그램에 로그인 할 때 수행 하는 작업을 표시 합니다. 사용자가 장치를 등록할 때까지 응용 프로그램에서 Office 365 리소스에 액세스 하지 못하도록 차단 됩니다.
  
![새 장치에 대한 등록 프로세스를 보여 줍니다.](media/O365-MDM-Capabilities-EnrollmentExample.png)
  
> [!NOTE]
> 정책 및 액세스 규칙을 Office 365에 대 한 MDM에서 만든 Exchange ActiveSync 모바일 장치 사서함 정책 및 Exchange 관리 센터에서 만든 장치 액세스 규칙을 재정의 합니다. 장치는 Office 365에 대 한 MDM에 등록 되, 후 Exchange ActiveSync 모바일 장치 사서함 정책 또는 장치 액세스 규칙을 모두 장치에 적용 되는 무시 됩니다. Exchange ActiveSync에 대 한 자세한 내용은, [Exchange Online의 Exchange ActiveSync](https://go.microsoft.com/fwlink/p/?LinkId=524380)를 참조 하십시오. 
  
## <a name="policy-settings-for-mobile-devices"></a>모바일 장치에 대한 정책 설정

켜져 특정 설정을 사용 하 여 액세스를 차단 하기 위한 정책을 만드는 경우 사용자가 [Office 365 전자 메일 및 문서에 대 한 액세스 제어](#access-control-for-office-365-email-and-documents)에 나열 된 지원 되는 응용 프로그램을 사용 하는 경우 Office 365 리소스에 액세스 하지 못하도록 차단 됩니다. 이러한 섹션에 사용자가 Office 365 리소스에 액세스 하지 못하도록 차단할 수 있는 설정은 다음과 같습니다.
  
- 보안
    
- 암호화
    
- 암호 해독
    
- 관리되는 전자 메일 프로필
    
예, 다음 다이어그램은 등록 된 장치와 사용자가 장치에 적용 되는 모바일 장치 관리 정책에서 보안 설정을 준수 사용 하지 않을 때 수행 되는 작업을 표시 합니다. 사용자가 Office 365에 대 한 MDM 함께 컨트롤의 액세스는 지원 되는 응용 프로그램에 로그인 합니다. 해당 장치 보안 설정을 준수 때까지 응용 프로그램에서 Office 365 리소스에 액세스 하지 못하도록 차단 합니다.
  
![장치가 호환되지 않는 경우 사용자가 차단됨을 보여 줍니다.](media/O365-MDM-Capabilities-ComplianceExample.png)
  
다음 섹션에는 안전 하 게 보호 하 고 조직의 Office 365 리소스에 연결 하는 모바일 장치를 관리 하는데 사용할 수 정책 설정을 나열 합니다. 
  
### <a name="security-settings"></a>보안 설정

|**설정 이름**|**Windows Phone 8.1 +**|**iOS 7.1+**|**Android 4+**|**삼성 Knox**|
|:-----|:-----|:-----|:-----|:-----|
|암호 요구  <br/> |✔  <br/> |✔  <br/> |✔  <br/> |✔  <br/> |
|단순 암호 방지  <br/> |✔  <br/> |✔  <br/> |✖  <br/> |✖  <br/> |
|영숫자 암호 필요  <br/> |✔  <br/> |✔  <br/> |✖  <br/> |✖  <br/> |
|최소 암호 길이  <br/> |✔  <br/> |✔  <br/> |✔  <br/> |✔  <br/> |
|장치 데이터가 지워지기 전 로그인 오류 횟수  <br/> |✔  <br/> |✔  <br/> |✔  <br/> |✔  <br/> |
|장치가 잠기기 전 비활성화 시간(분)  <br/> |✔  <br/> |✔  <br/> |✔  <br/> |✔  <br/> |
|암호 만료(일)  <br/> |✔  <br/> |✔  <br/> |✔  <br/> |✔  <br/> |
|암호 기록 저장 및 재사용 금지  <br/> |✔  <br/> |✔  <br/> |✔  <br/> |✔  <br/> |
   
### <a name="encryption-settings"></a>암호화 설정

|**설정 이름**|**Windows Phone 8.1 +**|**iOS 7.1+**|**Android 4+**|**삼성 Knox**|
|:-----|:-----|:-----|:-----|:-----|
|장치에 데이터 암호화 필요  <br/> |Windows Phone 8.1은 이미 암호화되어 있으므로 암호화를 해제할 수 없습니다.  <br/> |✖  <br/> |✔  <br/> |✔\*  <br/> |
   
\*삼성 Knox와 저장소 카드에서 암호화를 요청할 수 있습니다.
  
### <a name="jail-broken-setting"></a>암호 해독 설정

|**설정 이름**|**Windows Phone 8.1 +**|**iOS 7.1+**|**Android 4+**|**삼성 Knox**|
|:-----|:-----|:-----|:-----|:-----|
|장치 암호를 해독하거나 루팅할 수 없음  <br/> |✖  <br/> |✔  <br/> |✔  <br/> |✔  <br/> |
   
### <a name="managed-email-profile-option"></a>관리되는 전자 메일 프로필 옵션

다음 옵션은 사용자가 수동으로 만든된 전자 메일 프로필을 사용 하 여 하는 경우 Office 365 전자 메일에 액세스 하지 못하도록 차단할 수 있습니다. 전자 메일에 액세스할 수 있으려면 iOS 장치에서 사용자 프로필을 수동으로 만든된 전자 메일을 삭제 해야 합니다. 프로필을 삭제 하 한 후 새 프로필을 장치에 자동으로 만들어집니다.
  
|**설정 이름**|**Windows Phone 8.1 +**|**iOS 7.1+**|**Android 4+**|**삼성 Knox**|
|:-----|:-----|:-----|:-----|:-----|
|전자 메일 프로필이 관리됨  <br/> |✖  <br/> |✔  <br/> |✖  <br/> |✖  <br/> |
   
### <a name="cloud-settings"></a>클라우드 설정

|**설정 이름**|**Windows Phone 8.1 +**|**iOS 7.1+**|**Android 4+**|**삼성 Knox**|
|:-----|:-----|:-----|:-----|:-----|
|암호화된 백업 필요  <br/> |✖  <br/> |✔  <br/> |✖  <br/> |✖  <br/> |
|클라우드 백업 차단  <br/> |✖  <br/> |✔  <br/> |✖  <br/> |✖  <br/> |
|문서 동기화 차단  <br/> |✖  <br/> |✔  <br/> |✖  <br/> |✖  <br/> |
|사진 동기화 차단  <br/> |✖  <br/> |✔  <br/> |✖  <br/> |✖  <br/> |
|Google 백업 허용  <br/> |해당 없음  <br/> |해당 없음  <br/> |✖  <br/> |✔  <br/> |
|Google 계정 자동 동기화를 허용 합니다.  <br/> |해당 없음  <br/> |해당 없음  <br/> |✖  <br/> |✔  <br/> |
   
### <a name="system-settings"></a>시스템 설정

|**설정 이름**|**Windows Phone 8.1 +**|**iOS 7.1+**|**Android 4+**|**삼성 Knox**|
|:-----|:-----|:-----|:-----|:-----|
|화면 캡처 차단  <br/> |✔  <br/> |✔  <br/> |✖  <br/> |✔  <br/> |
|장치에서 진단 데이터 전송 차단  <br/> |✔  <br/> |✔  <br/> |✖  <br/> |✔  <br/> |
   
### <a name="application-settings"></a>응용 프로그램 설정

|**설정 이름**|**Windows Phone 8.1 +**|**iOS 7.1+**|**Android 4+**|**삼성 Knox**|
|:-----|:-----|:-----|:-----|:-----|
|장치에서 비디오 회의 차단  <br/> |✖  <br/> |✔  <br/> |✖  <br/> |✖  <br/> |
|응용 프로그램 저장소에 대한 액세스 차단  <br/> |✔  <br/> |✔  <br/> |✖  <br/> |✔  <br/> |
|응용 프로그램 저장소에 액세스할 때 암호 필요  <br/> |✖  <br/> |✔  <br/> |✖  <br/> |✖  <br/> |
   
### <a name="device-capabilities-settings"></a>장치 기능 설정

|**설정 이름**|**Windows Phone 8.1 +**|**iOS 7.1+**|**Android 4+**|**삼성 Knox**|
|:-----|:-----|:-----|:-----|:-----|
|이동식 저장소와 연결 차단  <br/> |✔  <br/> |✖  <br/> |✖  <br/> |✔  <br/> |
|Bluetooth 연결 차단  <br/> |✔  <br/> |✖  <br/> |✖  <br/> |✔  <br/> |
   
### <a name="additional-settings"></a>추가 설정

PowerShell cmdlet을 사용 하 여 다음과 같은 추가 정책 설정을 설정할 수 있습니다. 자세한 내용은 참조 [Office 365 보안 &amp; 준수 센터 cmdlet](https://go.microsoft.com/fwlink/p/?LinkId=827804)합니다.
  
|**설정 이름**|**Windows Phone 8.1 +**|**iOS 7.1+**|**Android 4 + (삼성 Knox 포함)**|
|:-----|:-----|:-----|:-----|
|CameraEnabled  <br/> |✔  <br/> |✔  <br/> |✔  <br/> |
|RegionRatings  <br/> |✖  <br/> |✔  <br/> |✖  <br/> |
|MoviesRatings  <br/> |✖  <br/> |✔  <br/> |✖  <br/> |
|TVShowsRating  <br/> |✖  <br/> |✔  <br/> |✖  <br/> |
|AppsRatings  <br/> |✖  <br/> |✔  <br/> |✖  <br/> |
|AllowVoiceDialing  <br/> |✖  <br/> |✔  <br/> |✖  <br/> |
|AllowVoiceAssistant  <br/> |✖  <br/> |✔  <br/> |✖  <br/> |
|AllowAssistantWhileLocked  <br/> |✖  <br/> |✔  <br/> |✖  <br/> |
|AllowPassbookWhileLocked  <br/> |✖  <br/> |✔  <br/> |✖  <br/> |
|MaxPasswordGracePeriod  <br/> |✖  <br/> |✔  <br/> |✖  <br/> |
|PasswordQuality  <br/> |✖  <br/> |✖  <br/> |✔  <br/> |
|SystemSecurityTLS  <br/> |✖  <br/> |✔  <br/> |✖  <br/> |
|WLANEnabled  <br/> |✔  <br/> |✖  <br/> |✖  <br/> |
   
### <a name="settings-supported-by-windows"></a>Windows에서 지원 되는 설정

모바일 장치도이 등록 하 여 Windows 8.1 및 Windows 10 장치를 관리할 수 있습니다. 해당 정책을 배포한 후 Windows 8.1 RT 및 Windows 10 RT 장치와 사용자가 처음 Office 365 전자 메일에 액세스 하는 기본 제공 전자 메일 응용 프로그램을 사용할 때 Office 365에 대 한 MDM에 등록 하 필요 합니다. 
  
다음 설정으로 모바일 장치 등록 된 Windows 8.1 및 Windows 10 장치에 대 한 지원 됩니다. 사용자가 Office 365 리소스에 액세스 하지 못하도록 차단 되지 않음이 설정은 합니다.
  
 **보안 설정**
  
- 영숫자 암호 필요
    
- 최소 암호 길이
    
- 장치 데이터가 지워지기 전 로그인 오류 횟수
    
- 장치가 잠기기 전 비활성화 시간(분)
    
- 암호 만료(일)
    
- 암호 기록 저장 및 재사용 금지
    
 **시스템 설정**
  
장치에서 진단 데이터 전송 차단
  
 **추가 설정**
  
PowerShell cmdlet을 사용하여 다음의 추가 정책 설정을 지정할 수 있습니다.
  
- AllowConvenienceLogon
    
- UserAccountControlStatus
    
- FirewallStatus
    
- AutoUpdateStatus
    
- AntiVirusStatus
    
- AntiVirusSignatureStatus
    
- SmartScreenEnabled
    
- WorkFoldersSyncUrl
    
## <a name="remotely-wipe-a-mobile-device"></a>원격으로 모바일 장치의 데이터 지우기

 중요 한 조직 데이터를 제거 하 고 **보안에서에서 있는 지우기 기능을 수행 하 여 조직의 Office 365 리소스에 대 한 액세스를 방지할 수 있는 장치를 분실 하거나 도난당, 하는 경우 &amp; 준수 센터\>데이터 손실 방지\>장치 관리**합니다. 만 조직 구성 데이터를 제거 하려면 선택적 지우기 또는 장치에서 모든 정보를 삭제 하 고 공장 설정으로 복원할 수 있는 전체 지우기 기능을 수행할 수 있습니다.
  
자세한 내용은 [Office 365의 모바일 장치 지우기 시도](https://go.microsoft.com/fwlink/p/?LinkId=518157)참조 하십시오.
  
## <a name="see-also"></a>참고 항목

[Office 365의 모바일 장치 관리 개요](overview-of-mdm.md)
  
[장치 보안 정책 만들기 및 배포](create-device-security-policies.md)

