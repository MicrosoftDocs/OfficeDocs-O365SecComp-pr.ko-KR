---
title: Microsoft Outlook용 정크 메일 보고 추가 기능 설치
ms.author: MSFTTracyP
author: tracyp
manager: laurawi
ms.date: 12/9/2016
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.assetid: 8dcc752f-e22e-44ce-a104-4cc4d7e439f3
ms.collection:
- M365-security-compliance
description: 이 articleSupported LanguagesInstall에서 정크 메일 보고 추가 기능에 대 한 자세한 내용은 정크 메일 보고 추가를 제거 합니다.
ms.openlocfilehash: c9211cd71fd82af2b9fc0533435ff27a82cd47be
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/17/2019
ms.locfileid: "34152560"
---
# <a name="install-the-junk-email-reporting-add-in-for-microsoft-outlook"></a>Microsoft Outlook용 정크 메일 보고 추가 기능 설치
  
이 항목에서는 조직의 클라이언트 컴퓨터에 Outlook용 Microsoft 정크 메일 보고 추가 기능을 설치하는 방법에 대해 설명합니다. 현재 버전의 추가 기능(2016년 1월)에 Outlook 2007, Outlook 2010, Outlook 2013, Outlook 2016에 대한 지원이 포함됩니다. 
  
지원되는 모든 언어에 대한 추가 기능을 사용하면 Outlook 리본에서 정크 메일을 직접 보고할 수 있습니다. 영어 버전의 추가 기능에는 리본에서 직접 Microsoft에 전자 메일 문제를 보고하는 추가 옵션이 포함됩니다.
  
-  받은 피싱 메일 보고 
    
- 정크 메일로 잘못 식별된 전자 메일을 보고합니다.
    
## <a name="supported-languages"></a>지원되는 언어
<a name="sectionSection0"> </a>

정크 메일 보고 추가 기능에서 지원되는 언어는 다음과 같습니다. 
  
- 중국어 간체
    
- 중국어 번체
    
- 네덜란드어
    
- 영어
    
- 프랑스어
    
- 독일어
    
- 이탈리아어
    
- 일본어
    
- 한국어
    
- 포르투갈어
    
- 포르투갈어(브라질)
    
- 스페인어
    
## <a name="install-the-junk-email-reporting-add-in"></a>정크 메일 보고 추가 기능 설치
<a name="sectionSection1"> </a>

다음과 같이 정크 메일 보고 추가 기능을 설치할 수 있습니다.
  
- 여타 .msi 파일과 마찬가지로 Windows Installer 패키지를 실행하여 설치합니다. 추가 기능을 설치할 경우 설치 화면을 안내하는 GUI 인터페이스가 열립니다. 자세한 내용은 [설치 마법사를 사용하여 정크 메일 보고 추가 기능 설치](install-the-junk-email-reporting-add-in-for-microsoft-outlook.md#BKMK_InstalltheJunkEmailReportingAdd-InUsingtheSetupWizard)를 참조하세요.
    
- 사용자 인터페이스를 표시하지 않는 자동 설치를 실행하여 설치합니다. 대신 설치 스크립트를 실행하는 명령줄 옵션을 지정합니다. 추가 기능을 설치할 경우 GUI 인터페이스를 통해 제공되지 않는 추가 구성 옵션이 표시됩니다. 자세한 내용은 [자동 모드를 사용하여 정크 메일 보고 추가 기능 설치](install-the-junk-email-reporting-add-in-for-microsoft-outlook.md#BKMK_InstalltheJunkEmailReportingAdd-IninSilentMode)를 참조하세요.
    
### <a name="what-do-you-need-to-know-before-you-begin"></a>시작하기 전에 알아야 할 내용

Microsoft Outlook용 Microsoft 정크 메일 보고 추가 기능을 설치하려면 다음을 충족해야 합니다.
  
- 다음 운영 체제 중 하나가 필요합니다. Windows 10, Windows 8.1, Windows 8, Windows 7 서비스팩 1, Windows 10 Server, Windows Server 2012 R2, Windows Server 2012 또는 Windows Server 2008 R2
    
- Outlook 2016, Outlook 2013, Outlook 2010 또는 Outlook 2007(서비스팩 2 이상)
    
- Microsoft Office PIA(기본 Interop 어셈블리): 
    
  - Microsoft Office 2010 이상용 PIA(기본 Interop 어셈블리)를 다운로드하려면 [Microsoft 다운로드 센터](https://go.microsoft.com/fwlink/?LinkID=166026)로 이동합니다.
    
  - Microsoft Office 2007용 PIA(기본 Interop 어셈블리)를 다운로드하려면 [Microsoft 다운로드 센터](https://go.microsoft.com/fwlink/?LinkId=72637)로 이동합니다.
    
- Microsoft .NET Framework [버전 2.0](https://go.microsoft.com/fwlink/?LinkID=208706)이 있어야 합니다.
    
> [!NOTE]
> 추가 기능을 설치할 컴퓨터에 대해 관리자 권한이 있어야 합니다. 
  
### <a name="install-the-junk-email-reporting-add-in-using-the-setup-wizard"></a>설치 마법사를 사용하여 정크 메일 보고 추가 기능 설치
<a name="BKMK_InstalltheJunkEmailReportingAdd-InUsingtheSetupWizard"> </a>

1. 컴퓨터에서 Outlook을 종료합니다.
    
2. Microsoft Outlook용 Microsoft 정크 메일 보고 추가 기능을 다운로드할 수 있는 Microsoft 다운로드 센터([https://go.microsoft.com/fwlink/?LinkID=147248](https://go.microsoft.com/fwlink/?LinkID=147248))로 이동한 후 .msi 파일을 다운로드합니다. 
    
3. .msi 파일을 두 번 클릭합니다. 
    
4. **Microsoft 정크 메일 보고 추가 기능 설치 시작** 페이지에서 **다음**을 클릭합니다. 
    
5. 사용권 계약을 읽어보고 설치 약관에 동의하면 **동의함**을 클릭합니다(계속해서 설치하려면 "동의함"을 클릭해야 함). **다음**을 클릭하여 계속합니다. 
    
6. 마법사가 완료되면 **마침**을 클릭합니다. 
    
7. Outlook을 시작합니다.
    
8. Outlook 리본에서 **정크** 단추를 찾습니다. 이제 받은 편지함에서 정크 메일 메시지를 선택하고 **정크 메일 보고** 단추를 클릭하여 Microsoft로 정크 메일 메시지를 보고할 수 있습니다. 
    
9. Microsoft에 피싱 메일을 보고하려는 경우 **피싱 메일로 보고**와 같은 기타 옵션을 보려면 **정크** 옆에 있는 아래쪽 화살표를 선택합니다. 전자 메일이 정크 메일로 잘못 식별된 경우 정크 메일 폴더에서 **정크 메일 아님으로 보고**를 선택할 수도 있습니다. 
    
### <a name="install-the-junk-email-reporting-add-in-using-silent-mode"></a>자동 모드를 사용하여 정크 메일 보고 추가 기능 설치
<a name="BKMK_InstalltheJunkEmailReportingAdd-IninSilentMode"> </a>

1. 컴퓨터에서 Outlook을 종료합니다.
    
2. 명령 프롬프트를 엽니다.
    
3. 선택적 매개 변수 없이 추가 기능을 바로 설치하려면 다음을 지정합니다.
    
  - x86 Outlook을 실행하는 컴퓨터:  `msiexec /qn /i JunkReportingAdd-in.x86-en.msi`
    
  - x64 Outlook을 실행하는 컴퓨터:  `msiexec /qn /i JunkReportingAdd-in.x64-en.msi`
    
    선택적 매개 변수 MaxMessageSelection 및 BccEmailAddress를 지정할 수도 있습니다.
    
  - MaxMessageSelection 관리자가 한 번의 클릭으로 전송을 위해 사용자가 선택할 수 있는 최대 메시지 수를 정의할 수 있습니다. 메시지 개수 범위는 1~50이며 기본값은 10개입니다.
    
    Example: If you want to set the maximum number of messages that can be selected by users for submission in a single click to 16, use the following option as part of the installation command:  `MaxMessageSelection=16`
    
  - BccEmailAddress 관리자가 숨은 참조 전자 메일 주소를 설정하여 모든 사용자 전송의 복사본을 수신하도록 사서함을 설정할 수 있습니다. 사서함이 설정되면 전송된 모든 전자 메일 복사본이 BccEmailAddress로 전송됩니다. 그렇지 않으면 기본 설정이 "숨은 참조 전자 메일 주소 없음"입니다.
    
    Example: If you want to use junkReports@contoso.com as the Bcc email address for all submissions, use the following command:  `BccEmailAddress="junkReports@contoso.com"`
    
    > [!NOTE]
    > 세미콜론 구분자를 입력하여 여러 숨은 참조 전자 메일 주소를 설정할 수 있습니다. 예:  `BccEmailAddress="junkReports@contoso.com; hollyd@treyresearch.net"`
  
    위의 예를 바탕으로 이 선택적 매개 변수를 모두 추가하려면 x86 Outlook을 실행하는 컴퓨터에 대해 다음을 지정합니다. 
    
  ```
  msiexec /qn /i JunkReportingAdd-in.x86-en.msi. MaxMessageSelection=16 BccEmailAddress="junkReports@contoso.com; hollyd@treyresearch.net"
  ```

4. 설치가 완료되면 Outlook을 시작합니다.
    
5. Outlook 리본에서 **정크** 단추를 찾습니다. 이제 받은 편지함에서 정크 메일 메시지를 선택하고 **정크 메일 보고** 단추를 클릭하여 Microsoft로 정크 메일 메시지를 보고할 수 있습니다. 
    
6. Microsoft에 피싱 메일을 보고하려는 경우 **피싱 메일로 보고**와 같은 기타 옵션을 보려면 **정크** 옆에 있는 아래쪽 화살표를 선택합니다. 전자 메일이 정크 메일로 잘못 식별된 경우 정크 메일 폴더에서 **정크 메일 아님으로 보고**를 선택할 수도 있습니다. 
    
## <a name="uninstall-the-junk-email-reporting-add-in"></a>정크 메일 보고 추가 기능 제거
<a name="sectionSection2"> </a>

다음과 같은 옵션 중 하나를 사용하여 정크 메일 보고 추가 기능을 제거할 수 있습니다.
  
- Windows 제어판에서 추가 기능을 제거합니다. 자세한 내용은 [제어판에서 정크 메일 보고 추가 기능 제거](install-the-junk-email-reporting-add-in-for-microsoft-outlook.md#BKMK_UninstalltheJunkEmailReportingAdd-infromControlPanel)를 참조하세요.
    
- Windows Installer 패키지를 실행하고 제거 옵션을 선택합니다. 자세한 내용은 [Windows Installer 패키지를 실행하여 정크 메일 보고 추가 기능 제거](install-the-junk-email-reporting-add-in-for-microsoft-outlook.md#BKMK_UninstalltheJunkEmailReportingAddinbyRunningtheWindowsInstallerPackage)를 참조하세요.
    
- 제거 옵션을 사용하여 자동 설치를 실행합니다. 자세한 내용은 [자동 모드로 정크 메일 보고 추가 기능 제거](install-the-junk-email-reporting-add-in-for-microsoft-outlook.md#MK_UninstalltheJunkEmailReportingAdd-ininSilentMode)를 참조하세요.
    
> [!NOTE]
> 추가 기능을 제거할 컴퓨터에 대해 관리자 권한이 있어야 합니다. 
  
### <a name="uninstall-the-junk-email-reporting-add-in-from-control-panel"></a>제어판에서 정크 메일 보고 추가 기능 제거
<a name="BKMK_UninstalltheJunkEmailReportingAdd-infromControlPanel"> </a>

1. 컴퓨터에서 Outlook을 종료합니다.
    
2. 컴퓨터의 시작 메뉴에서 **제어판**을 선택합니다.
    
3. **프로그램 및 기능**을 선택합니다.
    
4. **Microsoft Office Outlook용 Microsoft 정크 메일 보고 추가 기능**을 선택합니다.
    
5. **제거**를 선택합니다.
    
6. Outlook을 다시 시작하여 Outlook 리본에 추가 기능이 더 이상 표시되지 않는지 확인합니다.
    
### <a name="uninstall-the-junk-email-reporting-add-in-by-running-the-windows-installer-package"></a>Windows Installer 패키지를 실행하여 정크 메일 보고 추가 기능 제거
<a name="BKMK_UninstalltheJunkEmailReportingAddinbyRunningtheWindowsInstallerPackage"> </a>

1. 컴퓨터에서 Outlook을 종료합니다.
    
    > [!NOTE]
    > 제거 프로세스 동안 Outlook이 실행 중이면 Outlook을 다시 시작해야 추가 기능이 완벽하게 제거됩니다. 
  
2. 이전에 추가 기능을 설치할 때 실행한 .msi 파일을 다시 실행합니다. 
    
    Microsoft Outlook용 Microsoft 정크 메일 보고 추가 기능을 다운로드할 수 있는 Microsoft 다운로드 센터([https://go.microsoft.com/fwlink/?LinkId=147248](https://go.microsoft.com/fwlink/?LinkId=147248))로 이동하고 .msi 파일을 다운로드한 후 이 파일을 두 번 클릭합니다. 
    
3. 표시되는 지시에 따라 추가 기능을 제거합니다.
    
4. Outlook을 다시 시작하여 Outlook 리본에 추가 기능이 더 이상 표시되지 않는지 확인합니다.
    
### <a name="uninstall-the-junk-email-reporting-add-in-in-silent-mode"></a>자동 모드로 정크 메일 보고 추가 기능 제거
<a name="MK_UninstalltheJunkEmailReportingAdd-ininSilentMode"> </a>

1. 컴퓨터에서 Outlook을 종료합니다.
    
    > [!NOTE]
    > 제거 프로세스 동안 Outlook이 실행 중이면 Outlook을 다시 시작해야 추가 기능이 완벽하게 제거됩니다. 
  
2. 명령 프롬프트를 엽니다.
    
3. 다음 명령줄 매개 변수를 지정합니다.
    
    x86 Outlook을 실행하는 컴퓨터:  `msiexec /x JunkReportingAdd-in.x86-en.msi /qn MSIRESTARTMANAGERCONTROL="DisableShutdown"`
    
    x64 Outlook을 실행하는 컴퓨터:  `msiexec /x JunkReportingAdd-in.x64-en.msi /qn MSIRESTARTMANAGERCONTROL="DisableShutdown"`
    
4. Outlook을 다시 시작하여 Outlook 리본에 추가 기능이 더 이상 표시되지 않는지 확인합니다.
    
## <a name="for-more-information"></a>자세한 내용
<a name="sectionSection3"> </a>

[Microsoft에 정크 메일 메시지 보고](report-junk-email-messages-to-microsoft.md)
  
[문제 해결 및 지원 정보](troubleshooting-and-support-information.md)
  

