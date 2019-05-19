---
title: Office 365 메시지 암호화 레거시 정보
ms.author: tracyp
author: MSFTTracyP
manager: laurawi
ms.date: 1/4/2018
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: None
search.appverid:
- MET150
ms.assetid: 5986b9e1-c824-4f8f-9b7d-a2b0ae2a7fe9
ms.collection:
- M365-security-compliance
description: 아직 Office 365 조 직을 새 OME 기능으로 이동 하지 않았지만 이미 OME을 배포한 경우이 문서의 정보가 조직에 적용 됩니다. 조직에 적합 한 시기에 새 OME 기능으로 바로 이동 하는 계획을 수립 하는 것이 좋습니다. 자세한 내용은 Azure Information Protection 기반으로 구축 된 새 Office 365 메시지 암호화 기능 설치를 참조 하세요. 새 기능이 먼저 작동 하는 방식에 대해 자세히 알아보려면 Office 365 메시지 암호화를 참조 하세요. 이 문서의 나머지 부분에서는 새 OME 기능이 출시 되기 전에 발생 하는 OME 동작을 나타냅니다.
ms.openlocfilehash: aaba63364cf469f66a213ba791fc48ba29a69384
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/17/2019
ms.locfileid: "34155920"
---
# <a name="legacy-information-for-office-365-message-encryption"></a>Office 365 메시지 암호화 레거시 정보

아직 Office 365 조 직을 새 OME 기능으로 이동 하지 않았지만 이미 OME을 배포한 경우이 문서의 정보가 조직에 적용 됩니다. 조직에 적합 한 시기에 새 OME 기능으로 바로 이동 하는 계획을 수립 하는 것이 좋습니다. 자세한 내용은 [Azure Information Protection 기반으로 구축 된 새 Office 365 메시지 암호화 기능 설치](set-up-new-message-encryption-capabilities.md)를 참조 하세요. 새 기능이 먼저 작동 하는 방식에 대해 자세히 알아보려면 [Office 365 메시지 암호화](ome.md)를 참조 하세요. 이 문서의 나머지 부분에서는 새 OME 기능이 출시 되기 전에 발생 하는 OME 동작을 나타냅니다.
  
Office 365 메시지 암호화를 사용 하면 조직에서 조직 내부 및 외부의 사용자 간에 암호화 된 전자 메일 메시지를 보내고 받을 수 있습니다. Office 365 메시지 암호화는 Outlook.com, Yahoo, Gmail 및 기타 전자 메일 서비스와 함께 작동 합니다. 전자 메일 메시지 암호화는 의도 된 받는 사람만 메시지 콘텐츠를 볼 수 있도록 합니다.
  
그 예는 다음과 같습니다.
  
- 은행 직원이 고객에 게 신용 카드 명세서를 보냄
    
- 보험 회사 담당자가 고객에 게 정책 세부 정보를 제공 합니다.
    
- 담보 대출 브로커가 대출 응용 프로그램에 대 한 고객의 재무 정보를 요청 합니다.
    
- 의료 보험 공급자가 환자의에 게 의료 정보를 보냅니다.
    
- 변호사가 고객이 나 다른 변호사에 게 기밀 정보를 보내는 경우
    
## <a name="how-office-365-message-encryption-works-without-the-new-capabilities"></a>새로운 기능 없이 Office 365 메시지 암호화가 작동 하는 방식

Office 365 메시지 암호화는 Microsoft Azure 권한 관리 (Azure RMS)를 기반으로 작성 된 온라인 서비스입니다. Azure RMS를 사용 하는 경우 관리자는 메일 흐름 규칙을 정의 하 여 암호화 조건을 결정할 수 있습니다. 예를 들어 규칙에 따라 특정 받는 사람에 게 보내는 모든 메시지의 암호화가 필요할 수 있습니다.
  
이 짧은 비디오를 시청 하면 새로운 기능 없이 Office 365 메시지 암호화가 작동 하는 방식을 확인할 수 있습니다.
  
> [!VIDEO https://www.microsoft.com/videoplayer/embed/c55540e7-f7f0-42f5-b254-4b2d2fbb1d63?autoplay=false]
  
사용자가 Exchange Online에서 암호화 규칙과 일치 하는 전자 메일 메시지를 보내면 해당 메시지는 HTML 첨부 파일과 함께 전송 됩니다. 받는 사람이 HTML 첨부 파일을 열고 지침에 따라 Office 365 메시지 암호화 포털에서 암호화 된 메시지를 확인 합니다. 받는 사람은 Microsoft 계정 또는 Office 365와 연결 된 회사 또는 학교에 로그인 하거나 일회성 암호 코드를 사용 하 여 메시지를 볼 수 있습니다. 두 옵션을 사용하면 해당 받는 사람만 암호화된 메시지를 볼 수 있도록 보장할 수 있습니다. 이 프로세스는 새로운 OME 기능에서 매우 다릅니다.
  
다음 다이어그램은 암호화 및 암호 해독 프로세스를 통한 전자 메일 메시지의 흐름이 요약되어 있습니다.
  
![암호화된 전자 메일의 경로를 보여 주는 다이어그램](media/O365-Office365MessageEncryption-Concept.png)
  
자세한 내용은 [새 OME 기능을 출시 하기 전에 레거시 Office 365 메시지 암호화에 대 한 서비스 정보](legacy-information-for-message-encryption.md#LegacyServiceInfo)를 참조 하세요.
  
## <a name="defining-mail-flow-rules-for-office-365-message-encryption-that-dont-use-the-new-ome-capabilities"></a>새 OME 기능을 사용 하지 않는 Office 365 메시지 암호화에 대 한 메일 흐름 규칙 정의

새 기능 없이 Office 365 메시지 암호화를 사용 하도록 설정 하기 위해 Exchange Online 및 Exchange Online Protection 관리자는 Exchange 메일 흐름 규칙을 정의 합니다. 이러한 규칙은 전자 메일 메시지를 암호화 해야 하는 조건 및 메시지 암호화를 제거 하는 조건에 따라 결정 됩니다. 규칙에 대해 암호화 동작을 설정 하면 규칙 조건과 일치 하는 모든 메시지가 전송 되기 전에 암호화 됩니다.
  
메일 흐름 규칙은 융통성이 있으므로 단일 규칙에서 특정 보안 요구 사항을 충족할 수 있도록 조건을 조합할 수도 있습니다. 예를 들어 지정 된 키워드를 포함 하 고 외부 받는 사람에 게 보내는 모든 메시지를 암호화 하는 규칙을 만들 수 있습니다. Office 365 메시지 암호화도 암호화 된 전자 메일의 받는 사람 으로부터 회신을 암호화 하 고, 전자 메일 사용자의 편의를 위해 이러한 회신을 해독 하는 규칙을 만들 수 있습니다. 이렇게 하면 조직의 사용자가 암호화 포털에 로그인 하 여 회신을 볼 필요가 없습니다.
  
Exchange 메일 흐름 규칙을 만드는 방법에 대 한 자세한 내용은 [Define rules For Office 365 Message Encryption](define-mail-flow-rules-to-encrypt-email.md)을 참조 하십시오.
  
## <a name="sending-viewing-and-replying-to-encrypted-email-messages"></a>암호화된 전자 메일 메시지 보내기, 보기 및 회신

Office 365 메시지 암호화를 사용 하면 전자 메일 메시지가 관리자 정의 규칙에 따라 자동으로 암호화 됩니다. 암호화 된 메시지가 있는 전자 메일은 받는 사람의 받은 편지함에 첨부 된 HTML 파일로 도착 합니다.
  
받는 사람은 메시지의 지침에 따라 Microsoft 계정 또는 Office 365와 연관 된 회사 또는 학교를 사용 하 여 인증을 받고 해당 첨부 파일을 엽니다. 받는 사람이 이러한 계정 중 하나를 사용 하지 않는 경우에는 암호화 된 메시지를 볼 수 있는 로그인을 허용 하는 Microsoft 계정을 만들도록 지시 됩니다. 또는 받는 사람이 메시지를 보기 위해 일회성 통과 코드를 받을 수 있습니다. 한 번에 로그인 하거나 일회성 암호를 사용 하 여 받는 사람은 암호가 해독 된 메시지를 보고 암호화 된 회신을 보낼 수 있습니다.
  
## <a name="customize-encrypted-messages-with-office-365-message-encryption"></a>Office 365 메시지 암호화를 사용 하 여 암호화 된 메시지 사용자 지정

Exchange Online 및 Exchange Online Protection 관리자는 암호화 된 메시지를 사용자 지정할 수 있습니다. 예를 들어 회사의 브랜드 및 로고를 추가 하 고, 소개를 지정 하 고, 받는 사람이 암호화 된 메시지를 볼 수 있는 포털에 설명, 텍스트를 추가 하는 등의 고 지 사항을 추가할 수도 있습니다. Windows PowerShell cmdlet을 사용하면 암호화된 전자 메일 메시지 받는 사람의 보기 환경에서 다음과 같은 요소를 사용자 지정할 수 있습니다.
  
- 암호화된 메시지를 포함하는 전자 메일의 소개 텍스트
    
- 암호화된 메시지를 포함하는 전자 메일의 고지 사항 텍스트
    
- 메시지 보기 포털에 표시되는 포털 텍스트
    
- 전자 메일 메시지와 보기 포털에 표시되는 로고
    
언제든지 기본 모양과 느낌으로 되돌릴 수 있습니다.
  
다음 예에서는 전자 메일 첨부 파일에 포함된 ContosoPharma의 사용자 지정 로고를 보여 줍니다.
  
![암호화된 메시지 보기 페이지 예제](media/TA-OME-3attachment2.jpg)
  
 **조직의 브랜드를 사용 하 여 암호화 전자 메일 메시지와 암호화 포털을 사용자 지정 하려면**
  
1. [원격 powershell을 사용 하 여 Exchange online에 연결](https://docs.microsoft.com/office365/enterprise/powershell/connect-to-exchange-online-tenants-with-remote-windows-powershell-for-delegated)하는 방법에 설명 된 대로 원격 powershell을 사용 하 여 exchange online에 연결 합니다.
    
2. 여기에 설명 된 대로 Set-omeconfiguration cmdlet을 사용 하 여 Set-omeconfiguration를 참조 하거나 다음 표를 사용 하 여 지침을 [제공](http://technet.microsoft.com/en-us/3ef0aec0-ce28-411d-abe8-7236f082af1b) 합니다. 
    
   **암호화 사용자 지정 옵션**

|**암호화 환경에서 사용자 지정하려는 기능**|**사용할 Windows PowerShell 명령**|
|:-----|:-----|
|암호화된 전자 메일 메시지에 포함되는 기본 텍스트  <br/> 암호화된 메시지를 보기 위한 지침 위에 표시되는 기본 텍스트  <br/> | `Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> -EmailText "<string of up to 1024 characters>"` <br/> **예제:** `Set-OMEConfiguration -Identity "OME Configuration" -EmailText "Encrypted message from ContosoPharma secure messaging system"` <br/> |
|암호화된 메시지를 포함하는 전자 메일의 고지 사항 설명문  <br/> | `Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> DisclaimerText "<your disclaimer statement, string of up to 1024 characters>"` <br/> **예제:** `Set-OMEConfiguration -Identity "OME Configuration" -DisclaimerText "This message is confidential for the use of the addressee only"` <br/> |
|암호화된 메일 보기 포털 위쪽에 표시되는 텍스트  <br/> | `Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> -PortalText "<text for your portal, string of up to 128 characters>"` <br/> **예제:** `Set-OMEConfiguration -Identity "OME Configuration" -PortalText "ContosoPharma secure email portal"` <br/> |
|회사  <br/> | `Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> -Image <Byte[]>` <br/> **예제:** `Set-OMEConfiguration -Identity "OME configuration" -Image (Get-Content "C:\Temp\contosologo.png" -Encoding byte)` <br/> 지원되는 파일 형식: .png, .jpg, .bmp 또는 .tiff  <br/> 로고 파일의 최적 크기: 40KB 미만  <br/> 최적 로그 이미지 크기: 170x70 픽셀  <br/> |
   
 **암호화 된 전자 메일 메시지와 암호화 포털에서 브랜드 사용자 지정을 제거 하려면**
  
1. [원격 powershell을 사용 하 여 Exchange online에 연결](http://technet.microsoft.com/en-us/library/jj984289%28v=exchg.150%29.aspx)하는 방법에 설명 된 대로 원격 powershell을 사용 하 여 exchange online에 연결 합니다.
    
2. 여기에 설명 된 대로 Set-omeconfiguration cmdlet을 사용 하 여 [set-omeconfiguration를 설정](http://technet.microsoft.com/3ef0aec0-ce28-411d-abe8-7236f082af1b)합니다. DisclaimerText, EmailText 및 PortalText 값에서 조직의 브랜드 사용자 지정을 제거 하려면이 값을 빈 문자열 ( `""`)로 설정 합니다. 로고 등의 모든 이미지 값에 대해 값을로 `"$null"`설정 합니다.
    
   **암호화 사용자 지정 옵션**

|**암호화 환경의 이 기능을 기본 텍스트 및 이미지로 되돌리려면**|**사용할 Windows PowerShell 명령**|
|:-----|:-----|
|암호화된 전자 메일 메시지에 포함되는 기본 텍스트  <br/> 암호화된 메시지를 보기 위한 지침 위에 표시되는 기본 텍스트  <br/> | `Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> -EmailText "<empty string>"` <br/> **예제:** `Set-OMEConfiguration -Identity "OME Configuration" -EmailText ""` <br/> |
|암호화된 메시지를 포함하는 전자 메일의 고지 사항 설명문  <br/> | `Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> DisclaimerText "<empty string>"` <br/> **예제:** `Set-OMEConfiguration -Identity "OME Configuration" -DisclaimerText ""` <br/> |
|암호화된 메일 보기 포털 위쪽에 표시되는 텍스트  <br/> | `Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> -PortalText "<empty string>"` <br/> **다음은 기본값으로 되돌리는 예제입니다.**`Set-OMEConfiguration -Identity "OME Configuration" -PortalText ""` <br/> |
|회사  <br/> | `Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> -Image <"$null">` <br/> **다음은 기본값으로 되돌리는 예제입니다.**`Set-OMEConfiguration -Identity "OME configuration" -Image $null` <br/> |
   
## <a name="service-information-for-legacy-office-365-message-encryption-prior-to-the-release-of-the-new-ome-capabilities"></a>새 OME 기능 출시 이전의 레거시 Office 365 메시지 암호화에 대 한 서비스 정보
<a name="LegacyServiceInfo"> </a>

다음 표에는 새로운 OME 기능을 출시 하기 전에 Office 365 메시지 암호화 서비스에 대 한 기술 정보가 나와 있습니다.
  
|**서비스 정보**|**설명**|
|:-----|:-----|
|클라이언트 장치 요구 사항  <br/> |양식 게시를 지원하는 최신 브라우저에서 HTML 첨부 파일을 열 수 있으면 모든 클라이언트 장치에서 암호화된 메시지를 확인할 수 있습니다.  <br/> |
|암호화 알고리즘 및 FIPS(Federal Information Processing Standard) 규정 준수  <br/> |Office 365 메시지 암호화에서는 Windows Azure IRM(정보 권한 관리)과 같은 암호화 키를 사용하며 암호화 모드 2(RSA용 2K 키 및 SHA-1 시스템용 256비트 키)가 지원됩니다. 기본 IRM 암호화 모드에 대 한 자세한 내용은 [AD RMS 암호화 모드](http://technet.microsoft.com/library/hh867439%28WS.10%29.aspx)를 참조 하십시오.  <br/> |
|지원되는 메시지 유형  <br/> |Office 365 메시지 암호화는 메시지 클래스 ID가 **IPM.Note**인 항목에 대해서만 지원됩니다. 자세한 내용은 [항목 형식 및 메시지 클래스](https://msdn.microsoft.com/library/office/ff861573.aspx)를 참조 하십시오.  <br/> |
|메시지 크기 제한  <br/> |Office 365 메시지 암호화는 최대 25MB의 메시지를 암호화할 수 있습니다. 메시지 크기 제한에 대 한 자세한 내용은 [Exchange Online 제한을](http://technet.microsoft.com/library/exchange-online-limits.aspx)참조 하세요.  <br/> |
|Exchange Online 전자 메일 보존 정책  <br/> |Exchange Online에서는 암호화 된 메시지를 저장 하지 않습니다.  <br/> |
|Office 365 메시지 암호화에 대한 언어 지원  <br/> | Office 365 메시지 암호화는 Office 365 언어를 다음과 같이 지원합니다.  <br/>  받는 전자 메일 메시지와 첨부 된 HTML 파일은 보낸 사람의 언어 설정에 따라 지역화 됩니다.  <br/>  보기 포털은 받는 사람의 브라우저 설정에 따라 지역화됩니다.  <br/>  암호화된 메시지의 본문(내용)은 지역화되지 않습니다.  <br/> |
|OME 포털 및 OME 뷰어 앱에 대한 개인 정보 취급 방침 정보  <br/> |[Office 365 Messaging Encryption Portal privacy statement](protected-message-viewer-portal-privacy-statement.md)은 Microsoft가 귀하의 개인 정보로 수행하는 작업과 수행하지 않는 작업에 대한 자세한 정보를 제공합니다.  <br/> |
   
## <a name="frequently-asked-questions-about-legacy-ome"></a>레거시 OME에 대 한 질문과 대답
<a name="LegacyServiceInfo"> </a>

Office 365 메시지 암호화에 대 한 질문이 있나요? 몇 가지 답은 다음과 같습니다. 필요한 정보를 찾을 수 없으면 office [365 커뮤니티](http://community.office365.com/en-us/forums/default.aspx)의 office 365 커뮤니티 포럼을 확인 하세요.
  
 **Q. 사용자가 조직 외부의 받는 사람에 게 암호화 된 전자 메일 메시지를 보냅니다. Office 365 메시지 암호화로 암호화 된 전자 메일 메시지를 읽고 회신 하기 위해 외부 받는 사람이 수행 해야 하는 작업이 있습니까?**
  
조직 외부에서 Office 365 암호화 메시지를 받는 사람은 다음 두 가지 방법 중 하나로 메시지를 볼 수 있습니다.
  
- Microsoft 계정 또는 Office 365와 연결 된 회사 또는 학교 계정으로 로그인 하는 방법
    
- 1 회 통과 코드 사용
    
 **Q. Office 365 암호화된 메시지는 클라우드 또는 Microsoft 서버에 저장되나요?**
  
아니요, 암호화 된 메시지는 받는 사람의 전자 메일 시스템에 보관 되며 받는 사람이 메시지를 열면 Office 365 서버에서 보기 위해 일시적으로 게시 됩니다. 메시지는 저장 되지 않습니다.
  
 **Q. 암호화된 전자 메일 메시지를 원하는 브랜드로 사용자 지정할 수 있나요?**
  
예. Windows PowerShell cmdlet을 사용하여 암호화된 전자 메일 메시지 위쪽에 표시되는 기본 텍스트, 고지 사항 텍스트, 그리고 전자 메일 메시지와 암호화 포털에 사용할 로고를 사용자 지정할 수 있습니다. 자세한 내용은 [Add branding to encrypted messages](add-your-organization-brand-to-encrypted-messages.md)를 참조하세요.
  
 **Q. 서비스를 사용하려면 조직의 모든 사용자에게 라이선스가 필요하나요?**
  
암호화된 전자 메일을 보내는 조직의 모든 사용자에게는 라이선스가 있어야 합니다.
  
 **Q. 외부 받는 사람도 서비스를 구독해야 하나요?**
  
아니요. 외부 받는 사람은 서비스를 구독하지 않아도 암호화된 메시지를 읽거나 회신을 보낼 수 있습니다. 
  
 **Q. Office 365 메시지 암호화는 RMS (권한 관리 서비스)와는 어떤 차이가 있나요?**
  
RMS는 기본 제공 서식 파일 (예: 전달 및 회사 기밀)을 제공 하 여 조직의 내부 전자 메일에 대 한 정보 권한 보호 기능을 제공 합니다. Office 365 메시지 암호화에서는 내부 받는 사람과 외부 받는 사람에게 보내는 메시지에 대해 전자 메일 메시지 암호화가 지원됩니다.
  
 **Q. Office 365 메시지 암호화는 S/MIME과는 다른 것은 무엇입니까?**
  
S/MIME은 기본적으로 클라이언트 쪽 암호화 기술이며, 사용하려면 복잡한 인증서 관리 및 게시 인프라가 필요합니다. Office 365 메시지 암호화는 메일 흐름 규칙 (전송 규칙이 라고도 함)을 사용 하며, 인증서 게시에 의존 하지 않습니다.
  
 **Q. 모바일 장치에서 암호화된 메시지를 읽을 수 있나요?**
  
예, [Google Play 스토어](http://go.microsoft.com/fwlink/?LinkID=525995&amp;clcid=0x409) 및 [Apple 앱 스토어](http://go.microsoft.com/fwlink/?LinkID=525996&amp;clcid=0x409)에서 OME Viewer 앱을 다운로드 하 여 Android 및 iOS에서 메시지를 볼 수 있습니다. OME 뷰어 앱에서 HTML 첨부 파일을 연 다음 지시에 따라 암호화된 메시지를 엽니다. 모바일 장치에서는 메일 클라이언트에서 폼 게시를 지원하는 경우 HTML 첨부 파일을 열 수 있습니다.
  
 **Q. 회신과 전달된 메시지도 암호화되나요?**
  
예. 스레드가 진행되는 동안에는 응답도 계속 암호화됩니다.
  
 **Q. Office 365 메시지 암호화는 지역화를 제공 하나요?**
  
받는 전자 메일 및 HTML 콘텐츠는 보낸 사람의 전자 메일 설정에 따라 지역화됩니다. 보기 포털은 받는 사람의 브라우저 설정에 따라 지역화됩니다. 그러나 암호화된 메시지의 실제 본문(내용)은 지역화되지 않습니다.
  
 **Q. Office 365 메시지 암호화에 사용 되는 암호화 방법은 무엇입니까?**
  
Office 365 메시지 암호화는 RMS (권한 관리 서비스)를 암호화 인프라로 사용 합니다. 사용되는 암호화 방식은 메시지 암호화 및 암호 해독에 사용되는 RMS 키를 얻은 위치에 따라 다릅니다.
  
- Microsoft Azure RMS를 사용 하 여 키를 가져오는 경우 암호화 모드 2가 사용 됩니다. 암호화 모드 2는 업데이트 및 향상 된 AD RMS 암호화 구현입니다. 서명 및 암호화를 위해 RSA 2048를 지원 하 고 서명을 위해 SHA-256를 지원 합니다.
    
- AD(Active Directory) RMS를 사용하여 키를 얻은 경우 암호화 모드 1 또는 암호화 모드 2가 사용됩니다. 사용되는 방법은 온-프레미스 AD RMS 배포에 따라 다릅니다. 암호화 모드 1은 원래 AD RMS 암호화 구현으로, 서명 및 암호화에 RSA 1024을 지원하고 서명에 SHA-1을 지원합니다. 이 모드는 RMS의 모든 현재 버전에서 계속 지원됩니다.
    
자세한 내용은 [AD RMS 암호화 모드](http://go.microsoft.com/fwlink/p/?LinkId=398616)를 참조 하세요.
  
 **Q. 일부 암호화된 메시지에 Office365@messaging.microsoft.com에서 전송되었다고 표시되는 이유**
  
암호화된 회신 암호화 포털에서 또는 OME 뷰어 앱을 통해 전송되는 경우 암호화된 메시지는 Microsoft 끝점을 통해 전송되므로 보내는 전자 메일 주소는 Office365@messaging.microsoft.com으로 설정됩니다. 이를 통해 암호화된 메시지가 스팸으로 표시되지 않도록 합니다. 암호화 포털 안의 주소 및 전자 메일에 표시되는 이름은 이 레이블을 지정으로 인해 변경되지 않습니다. 또한 다른 전자 메일 클라이언트를 통해서가 아니라 해당 포털을 통해 보낸 메시지에만 이 레이블 지정을 적용합니다.
  
 **Q. EHE (Exchange Hosted Encryption) 구독자 Office 365 메시지 암호화로의 업그레이드에 대 한 자세한 내용은 어디에서 확인할 수 있나요?**
  
모든 EHE 고객은 Office 365 메시지 암호화로 업그레이드되었습니다. 자세한 내용은 [Exchange Hosted Encryption Upgrade Center](http://go.microsoft.com/fwlink/p/?LinkID=511077)를 참조 하십시오.
  
 **Q. Office 365 메시지 암호화를 지원 하기 위해 조직의 방화벽에 있는 Url, IP 주소 또는 포트를 열어야 하나요?**
  
예. Office 365 메시지 암호화로 암호화 된 메시지에 대 한 인증을 사용 하도록 설정 하려면 Exchange Online에 대 한 Url을 조직의 허용 목록에 추가 해야 합니다. Exchange Online URL 목록은 [Office 365 URLs and IP Address Ranges](https://support.office.com/article/f57e35b7-0a45-42f0-855e-11aa5e7f13fd.aspx)를 참조하세요.
  
 **Q. Office 365 암호화 메시지를 한 번에 몇 명에게 보낼 수 있습니까?**
  
암호화 된 메시지의 받는 사람 제한은 메시지 **대상** 필드의 문자 수에 따라 달라 집니다. 메일 그룹 확장 후에 **받는 사람** 필드에 포함된 받는 사람 주소를 모두 합쳤을 때 문자 수가 11,980자를 초과할 수 없습니다. 전자 메일 주소는 문자 길이에 따라 다를 수 있기 때문에 암호화 된 단일 메시지에 대 한 표준 받는 사람 제한은 없습니다. 
  
 **Q. 특정 받는 사람에게 보낸 메시지를 취소할 수 있습니까?**
  
아니요. 특정인이 보낸 후에는 해당 사용자에 게 메시지를 해지할 수 없습니다.
  
 **Q. 받아서 읽은 암호화된 메시지에 대한 보고서를 볼 수 있습니까?**
  
암호화 된 메시지를 본 적이 있는지를 보여 주는 보고서는 없지만, 예를 들어, 특정 메일 흐름 규칙 (전송 규칙이 라고도 함)과 일치 하는 메시지 수를 확인 하기 위해 사용할 수 있는 Office 365 보고서가 있습니다.
  
 **Q. Microsoft는 OME 포털 및 OME 뷰어 앱을 통해 제공한 정보로 어떤 작업을 수행하나요?**
  
[Office 365 메시징 암호화 포털 개인 정보 취급 방침](protected-message-viewer-portal-privacy-statement.md) 은 Microsoft가 어떤 작업을 수행 하 고 있는지에 대 한 자세한 정보를 제공 합니다. 
  

