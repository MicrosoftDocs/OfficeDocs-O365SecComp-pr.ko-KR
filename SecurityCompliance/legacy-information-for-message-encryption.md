---
title: Office 365 메시지 암호화 레거시 정보
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 1/4/2018
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: None
search.appverid:
- MET150
ms.assetid: 5986b9e1-c824-4f8f-9b7d-a2b0ae2a7fe9
description: 새로운 OME 기능을 Office 365 조직을 아직 이동 하지 않은 OME를 이미 배포한 경우이 문서의 정보는 조직에 적용 됩니다. 것이 조직에 대 한 적당 하 게 하는 즉시 새 OME 기능으로 이동 하는 계획을 확인 하는 것이 좋습니다. 자세한 내용은 세트를 참조 하십시오. Azure 정보 보호 위쪽에 구축 된 새로운 Office 365 메시지 암호화 기능을 합니다. 새로운 기능 먼저 작동 하는 방법에 대 한 자세한 정보를 계속 확인 하려는 경우 Office 365 메시지 암호화를 참조 하십시오. 이 문서의 나머지 부분 릴리스 이전에 새 OME 기능 OME 동작을 가리킵니다.
ms.openlocfilehash: d5b21cbe0004ca7bda38085bd5d8ef5f2a22b04e
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22533584"
---
# <a name="legacy-information-for-office-365-message-encryption"></a>Office 365 메시지 암호화 레거시 정보

새로운 OME 기능을 Office 365 조직을 아직 이동 하지 않은 OME를 이미 배포한 경우이 문서의 정보는 조직에 적용 됩니다. 것이 조직에 대 한 적당 하 게 하는 즉시 새 OME 기능으로 이동 하는 계획을 확인 하는 것이 좋습니다. 자세한 내용은 [Azure 정보 보호 위쪽에 구축 된 새로운 Office 365 메시지 암호화 기능을 설정](set-up-new-message-encryption-capabilities.md)합니다. 새로운 기능 먼저 작동 하는 방법에 대 한 자세한 정보를 계속 확인 하려는 경우 [Office 365 메시지 암호화](ome.md)를 참조 하십시오. 이 문서의 나머지 부분 릴리스 이전에 새 OME 기능 OME 동작을 가리킵니다.
  
Office 365 메시지 암호화를 사용 하면 조직 보내고 사용자 조직 내부 및 외부 사용자 간의 암호화 된 전자 메일 메시지를 받을 수 있습니다. Office 365 메시지 암호화 Outlook.com, yahoo!, Gmail, 및 다른 전자 메일 서비스에서 작동합니다. 전자 메일 메시지 암호화를 통해 확인만 받는 사람에 게 대상으로 하는 메시지 콘텐츠를 볼 수 있습니다.
  
아래에 몇 가지 예가 나와 있습니다.
  
- 은행 직원이 고객에 게 신용 카드 청구서를 보내는
    
- 고객에 게 정책 세부 정보를 제공 하는 보험 회사 담당자
    
- 모기지 브로커가 대출 응용 프로그램에 대 한 고객에서 재무 정보를 요청합니다.
    
- 의료 서비스 공급자는 환자 의료 정보를 보냅니다.
    
- 변호사는 고객이 나 다른 변호사에 기밀 정보를 보내는
    
## <a name="how-office-365-message-encryption-works-without-the-new-capabilities"></a>새로운 기능 없이 Office 365 메시지 암호화의 작동 방식

Office 365 메시지 암호화는 Microsoft Azure 권한 관리 (Azure RMS)에서 작성 되는 온라인 서비스입니다. 관리자는 Azure RMS 암호화에 대 한 조건을 확인 하려면 메일 흐름 규칙을 정의할 수 있습니다. 예, 규칙을 특정 받는 사람에 게 보내는 모든 메시지의 암호화가 필요 수 있습니다.
  
Office 365 메시지 암호화의 새로운 기능 없이 작동 하는 방법을 보려면이 짧은 비디오를 시청 합니다.
  
> [!VIDEO https://www.microsoft.com/videoplayer/embed/c55540e7-f7f0-42f5-b254-4b2d2fbb1d63?autoplay=false]
  
다른 사용자가 보낼 때 전자 메일 메시지를 Exchange 온라인와 일치 하는 암호화 규칙, HTML 파일을 첨부 한 메시지 전송 됩니다. 받는 사람이 HTML 첨부 파일 및 Office 365 메시지 암호화 포털에서 암호화 된 메시지를 볼 수 있는 지침을 따릅니다. 받는 사람이 Microsoft 계정 또는 작업 또는 Office 365와 관련 된 학교를 사용 하 여 서명 또는 일회용 암호를 사용 하 여 메시지를 볼 수도 있습니다. 두 옵션을 보장 의도 한 받는 사람이 암호화 된 메시지를 볼 수 있습니다. 이 프로세스는 새로운 OME 기능에 대 한 매우 다릅니다.
  
다음 다이어그램은 암호화 및 암호 해독 프로세스를 통한 전자 메일 메시지의 흐름이 요약되어 있습니다.
  
![암호화된 전자 메일의 경로를 보여 주는 다이어그램](media/O365-Office365MessageEncryption-Concept.png)
  
자세한 내용은 [새 OME 기능 출시 하기 전에 레거시 Office 365 메시지 암호화에 대 한 서비스 정보](legacy-information-for-message-encryption.md#LegacyServiceInfo)를 참조 하십시오.
  
## <a name="defining-mail-flow-rules-for-office-365-message-encryption-that-dont-use-the-new-ome-capabilities"></a>새 OME 기능을 사용 하지 않는 Office 365 메시지 암호화에 대 한 메일 흐름 규칙 정의

Office 365 메시지 암호화 없이 새로운 기능을 사용 하려면 Exchange Online 및 Exchange Online Protection 관리자는 Exchange 메일 흐름 규칙을 정의 합니다. 이러한 규칙에서 어떤 조건 전자 메일 메시지를 암호화 해야, 메시지 암호화를 제거 하기 위한 조건, 결정 합니다. 암호화 작업 규칙에 대해 설정 된 경우이 로그는 전송 하기 전에 규칙 조건에 맞는 모든 메시지는 암호화 됩니다.
  
메일 흐름 규칙은 유연한 두면 조건을 결합 하는 단일 규칙에서 특정 보안 요구 사항을 충족할 수 있습니다. 예를 포함 하는 지정 된 키워드 외부 받는 사람에 게 보내는 모든 메시지를 암호화 하는 규칙을 만들 수 있습니다. Office 365 메시지 암호화도 암호화 된 전자 메일의 받는 사람에 대 한 회신을 암호화 하 고 전자 메일 사용자를 위한 사용자 편의 위해서 이러한 회신의 암호를 해독 하는 규칙을 만들 수 있습니다. 이러한 방법으로 조직의 사용자가 회신을 볼 암호화 포털에 로그인 할 필요가 있습니다.
  
Exchange 메일 흐름 규칙을 만드는 방법에 대 한 자세한 내용은 [Office 365 메시지 암호화에 대 한 규칙 정의](define-mail-flow-rules-to-encrypt-email.md)참조 하십시오.
  
## <a name="sending-viewing-and-replying-to-encrypted-email-messages"></a>암호화된 전자 메일 메시지 보내기, 보기 및 회신

Office 365 메시지 암호화 된 전자 메일 메시지는 암호화 자동으로 관리자 정의 규칙을 기반으로 합니다. 암호화 된 메시지에는 전자 메일 첨부 된 HTML 파일에 있는 받는 사람의 받은 편지함에 도착 합니다.
  
받는 사람에 게 첨부 파일을 열고 Microsoft 계정 또는 작업 또는 Office 365와 관련 된 학교를 사용 하 여 인증 하는 메시지의에서 지침에 따릅니다. 받는 사람에 게 계정 중 하나를 설치 하지 않은 경우 암호화 된 메시지를 볼 수는 수 있도록 하는 계정 로그인 Microsoft 만들 향하는 중입니다. 또는 받는 사람에 게 메시지를 보려면 1 회 암호를 가져올 선택할 수 있습니다. 로그인 또는 일회용 암호를 사용 하 여, 후 받는 사람에 게 암호가 해독 된 메시지를 보고 하 고 암호화 된 회신을 보낼 수 있습니다.
  
## <a name="customize-encrypted-messages-with-office-365-message-encryption"></a>Office 365 메시지 암호화와 암호화 된 메시지를 사용자 지정

Exchange Online 및 Exchange Online Protection 관리자 권한으로 암호화 된 메시지를 사용자 지정할 수 있습니다. 예, 회사 브랜드 및 로고, 소개를 지정 하 고 받는 사람에 게 암호화 된 메시지를 볼 있는 포털 및 암호화 된 메시지에 고 지 사항 텍스트를 추가 추가할 수 있습니다. Windows PowerShell cmdlet을 사용 하 여 암호화 된 전자 메일 메시지의 받는 사람에 대 한 보기 환경에서 다음과 같은 측면을 사용자 지정할 수 있습니다.
  
- 암호화된 메시지를 포함하는 전자 메일의 소개 텍스트
    
- 암호화된 메시지를 포함하는 전자 메일의 고지 사항 텍스트
    
- 메시지 보기 포털에 표시되는 포털 텍스트
    
- 전자 메일 메시지와 보기 포털에 표시되는 로고
    
언제든지 기본 모양과 느낌으로 되돌릴 수 있습니다.
  
다음 예에서는 전자 메일 첨부 파일에 포함된 ContosoPharma의 사용자 지정 로고를 보여 줍니다.
  
![암호화된 메시지 보기 페이지 예제](media/TA-OME-3attachment2.jpg)
  
 **암호화 전자 메일 메시지와 암호화 포털 조직의 브랜드로 사용자 지정 하려면**
  
1. [Exchange Online를 사용 하 여 원격 PowerShell 연결](https://docs.microsoft.com/office365/enterprise/powershell/connect-to-exchange-online-tenants-with-remote-windows-powershell-for-delegated)의 설명에 따라 원격 PowerShell을 사용 하는 Exchange Online에 연결 합니다.
    
2. Cmdlet을 사용 하면 Set-omeconfiguration 설명에 따라 여기: [Set-omeconfiguration](http://technet.microsoft.com/en-us/3ef0aec0-ce28-411d-abe8-7236f082af1b) 또는 지침에 대 한 다음 표를 사용 합니다. 
    
   **암호화 사용자 지정 옵션**

|**암호화 환경에서 사용자 지정하려는 기능**|**사용할 Windows PowerShell 명령**|
|:-----|:-----|
|암호화된 전자 메일 메시지에 포함되는 기본 텍스트  <br/> 암호화된 메시지를 보기 위한 지침 위에 표시되는 기본 텍스트  <br/> | `Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> -EmailText "<string of up to 1024 characters>"` <br/> **예제:**`Set-OMEConfiguration -Identity "OME Configuration" -EmailText "Encrypted message from ContosoPharma secure messaging system"` <br/> |
|암호화된 메시지를 포함하는 전자 메일의 고지 사항 설명문  <br/> | `Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> DisclaimerText "<your disclaimer statement, string of up to 1024 characters>"` <br/> **예제:**`Set-OMEConfiguration -Identity "OME Configuration" -DisclaimerText "This message is confidential for the use of the addressee only"` <br/> |
|암호화된 메일 보기 포털 위쪽에 표시되는 텍스트  <br/> | `Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> -PortalText "<text for your portal, string of up to 128 characters>"` <br/> **예제:**`Set-OMEConfiguration -Identity "OME Configuration" -PortalText "ContosoPharma secure email portal"` <br/> |
|로고  <br/> | `Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> -Image <Byte[]>` <br/> **예제:**`Set-OMEConfiguration -Identity "OME configuration" -Image (Get-Content "C:\Temp\contosologo.png" -Encoding byte)` <br/> 지원되는 파일 형식: .png, .jpg, .bmp 또는 .tiff  <br/> 로고 파일의 최적 크기: 40KB 미만  <br/> 최적 로그 이미지 크기: 170x70 픽셀  <br/> |
   
 **암호화 전자 메일 메시지와 암호화 포털에서 사용자 지정 브랜드를 제거 하려면**
  
1. [Exchange Online를 사용 하 여 원격 PowerShell 연결](http://technet.microsoft.com/en-us/library/jj984289%28v=exchg.150%29.aspx)의 설명에 따라 원격 PowerShell을 사용 하는 Exchange Online에 연결 합니다.
    
2. Cmdlet을 사용 하면 Set-omeconfiguration 설명에 따라 여기: [Set-omeconfiguration](http://technet.microsoft.com/3ef0aec0-ce28-411d-abe8-7236f082af1b)합니다. PortalText 값을 빈 문자열 값을 설정 하 고 조직을 제거 하려면 DisclaimerText, EmailText에서 사용자 지정 브랜드의 `""`합니다. 모든 이미지 로고, 등의 값에 대 한 값을 설정 `"$null"`합니다.
    
   **암호화 사용자 지정 옵션**

|**암호화 환경의 이 기능을 기본 텍스트 및 이미지로 되돌리려면**|**사용할 Windows PowerShell 명령**|
|:-----|:-----|
|암호화된 전자 메일 메시지에 포함되는 기본 텍스트  <br/> 암호화된 메시지를 보기 위한 지침 위에 표시되는 기본 텍스트  <br/> | `Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> -EmailText "<empty string>"` <br/> **예제:**`Set-OMEConfiguration -Identity "OME Configuration" -EmailText ""` <br/> |
|암호화된 메시지를 포함하는 전자 메일의 고지 사항 설명문  <br/> | `Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> DisclaimerText "<empty string>"` <br/> **예제:**`Set-OMEConfiguration -Identity "OME Configuration" -DisclaimerText ""` <br/> |
|암호화된 메일 보기 포털 위쪽에 표시되는 텍스트  <br/> | `Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> -PortalText "<empty string>"` <br/> **다시 기본값으로 되돌리는 예제:**`Set-OMEConfiguration -Identity "OME Configuration" -PortalText ""` <br/> |
|로고  <br/> | `Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> -Image <"$null">` <br/> **다시 기본값으로 되돌리는 예제:**`Set-OMEConfiguration -Identity "OME configuration" -Image $null` <br/> |
   
## <a name="service-information-for-legacy-office-365-message-encryption-prior-to-the-release-of-the-new-ome-capabilities"></a>새 OME 기능을 릴리스하기 전에 레거시 Office 365 메시지 암호화에 대 한 서비스 정보
<a name="LegacyServiceInfo"> </a>

다음 표에서 새 OME 기능 출시 하기 전에 Office 365 메시지 암호화 서비스에 대 한 기술 세부 정보를 제공합니다.
  
|**서비스 정보**|**설명**|
|:-----|:-----|
|클라이언트 장치 요구 사항  <br/> |양식 게시를 지원하는 최신 브라우저에서 HTML 첨부 파일을 열 수 있으면 모든 클라이언트 장치에서 암호화된 메시지를 확인할 수 있습니다.  <br/> |
|암호화 알고리즘 및 FIPS(Federal Information Processing Standard) 규정 준수  <br/> |Office 365 메시지 암호화로 Windows Azure 권한 관리 IRM (정보)는 동일한 암호화 키를 사용 하 여 및 sha-1 시스템에 대 한 암호화 모드 2 (2k RSA) 및 256 비트 키를 지원 합니다. 원본으로 사용 되는 IRM 암호화 모드에 대 한 자세한 내용은 [AD RMS 암호화 모드](http://technet.microsoft.com/library/hh867439%28WS.10%29.aspx)를 참조 하십시오.<br/> |
|지원되는 메시지 유형  <br/> |Office 365 메시지 암호화는 **IPM의 메시지 클래스 ID가 있는 항목에 대해서만 지원 됩니다. 참고**합니다. 자세한 내용은 [항목 형식 및 메시지 클래스를](https://msdn.microsoft.com/library/office/ff861573.aspx)참조 하십시오.<br/> |
|메시지 크기 제한  <br/> |Office 365 메시지 암호화는 최대 25 메가바이트의 메시지를 암호화할 수 있습니다. 메시지 크기 제한에 대 한 자세한 내용은 [Exchange Online 제한](http://technet.microsoft.com/library/exchange-online-limits.aspx)을 참조 하십시오.<br/> |
|Exchange Online 전자 메일 보존 정책  <br/> |Exchange Online는 암호화 된 메시지를 저장 하지 않습니다.  <br/> |
|Office 365 메시지 암호화에 대한 언어 지원  <br/> | Office 365 메시지 암호화는 Office 365 언어를 다음과 같이 지원합니다.  <br/>  받는 전자 메일 메시지와 첨부 된 HTML 파일은 보낸 사람의 언어 설정에 따라 지역화 됩니다.  <br/>  보기 포털은 받는 사람의 브라우저 설정에 따라 지역화됩니다.  <br/>  암호화된 메시지의 본문(내용)은 지역화되지 않습니다.  <br/> |
|OME 포털 및 OME 뷰어 앱에 대한 개인 정보 취급 방침 정보  <br/> |[Office 365 Messaging Encryption Portal privacy statement](protected-message-viewer-portal-privacy-statement.md)은 Microsoft가 귀하의 개인 정보로 수행하는 작업과 수행하지 않는 작업에 대한 자세한 정보를 제공합니다.  <br/> |
   
## <a name="frequently-asked-questions-about-legacy-ome"></a>질문과 대답 레거시 OME 하는 방법에 대 한
<a name="LegacyServiceInfo"> </a>

Office 365 메시지 암호화에 대 한 질문이 있습니까? 다음은 일부 대답 합니다. 필요한 정보를 찾을 수 없는 경우에 [Office 365 커뮤니티](http://community.office365.com/en-us/forums/default.aspx)에서 Office 365 커뮤니티 포럼 확인 합니다.
  
 **Q: 내 사용자가 조직 외부의 받는 사람에 게 암호화 된 전자 메일 메시지를 보내야 합니다. 이 외부 받는 사람을 읽고 Office 365 메시지 암호화와 암호화 된 전자 메일 메시지에 회신 하기 위해 수행 해야할 아무것도 있습니까?**
  
조직 외부에서 Office 365 암호화 메시지를 받는 사람은 다음 두 가지 방법 중 하나로 메시지를 볼 수 있습니다.
  
- Microsoft 계정 또는 Office 365와 관련 된 작업이 나 교육용 계정을 사용 하 여 서명 합니다.
    
- 일회성를 사용 하 여 코드를 전달 합니다.
    
 **Q. Office 365 암호화된 메시지는 클라우드 또는 Microsoft 서버에 저장되나요?**
  
아니요, 암호화 된 메시지 받는 사람의 전자 메일 시스템에 보관 되며 받는 사람이 메시지를 열 때 일시적으로 Office 365 서버에서 볼 수 있도록 게시 됩니다. 메시지는 다음과 같은 저장 되지 않습니다.
  
 **Q. 암호화된 전자 메일 메시지를 원하는 브랜드로 사용자 지정할 수 있나요?**
  
예. Windows PowerShell cmdlet을 사용하여 암호화된 전자 메일 메시지 위쪽에 표시되는 기본 텍스트, 고지 사항 텍스트, 그리고 전자 메일 메시지와 암호화 포털에 사용할 로고를 사용자 지정할 수 있습니다. 자세한 내용은 [Add branding to encrypted messages](add-your-organization-brand-to-encrypted-messages.md)를 참조하세요.
  
 **Q. 서비스를 사용하려면 조직의 모든 사용자에게 라이선스가 필요하나요?**
  
암호화된 전자 메일을 보내는 조직의 모든 사용자에게는 라이선스가 있어야 합니다.
  
 **Q. 외부 받는 사람도 서비스를 구독해야 하나요?**
  
아니요. 외부 받는 사람은 서비스를 구독하지 않아도 암호화된 메시지를 읽거나 회신을 보낼 수 있습니다. 
  
 **Q: 방법에서 서비스 RMS (권한 관리) 다른 Office 365 메시지 암호화 인지 확인**
  
RMS와 같은 기본 제공 서식 파일을 제공 하 여 조직의 내부 전자 메일에 대 한 정보 권한 보호 기능을 제공: 회사 기밀을 전달 하지 않습니다. Office 365 메시지 암호화에서 지 원하는 전자 메일 메시지 암호화도 외부 받는 사람에 게 내부 받는 사람에 게 전송 되는 메시지에 대 한 합니다.
  
 **Q: 방법 Office 365 메시지 암호화 S/MIME 다르게 인지 확인**
  
S/MIME은 기본적으로 클라이언트 쪽 암호화 기술이며, 사용하려면 복잡한 인증서 관리 및 게시 인프라가 필요합니다. 반면 Office 365 메시지 암호화에서는 인증서 게시가 아닌 전송 규칙이 사용됩니다.
  
 **Q. 모바일 장치에서 암호화된 메시지를 읽을 수 있나요?**
  
예, [Google 재생을 저장](http://go.microsoft.com/fwlink/?LinkID=525995&amp;clcid=0x409) 하 고 [Apple App 저장소](http://go.microsoft.com/fwlink/?LinkID=525996&amp;clcid=0x409)에서 OME 뷰어 앱을 다운로드 하 여 Android 및 iOS 메시지를 볼 수 있습니다. OME 뷰어 응용 프로그램에서 HTML 첨부 파일을 연 다음에 암호화 된 메시지를 열고 지침을 따릅니다. 기타 모바일 장치에 대 한 전자 메일 클라이언트 양식 게시를 지 원하는 HTML 첨부 파일을 열 수 있습니다.
  
 **Q. 회신과 전달된 메시지도 암호화되나요?**
  
예. 스레드가 진행되는 동안에는 응답도 계속 암호화됩니다.
  
 **Q. 지역화된 Office 365 메시지 암호화가 제공되나요?**
  
받는 전자 메일 및 HTML 콘텐츠는 보낸 사람의 전자 메일 설정에 따라 지역화됩니다. 보기 포털은 받는 사람의 브라우저 설정에 따라 지역화됩니다. 그러나 암호화된 메시지의 실제 본문(내용)은 지역화되지 않습니다.
  
 **Q. Office 365 메시지 암호화에서는 어떤 암호화 방식이 사용되나요?**
  
Office 365 메시지 암호화에서는 RMS(Rights Management Services)를 암호화 인프라로 사용합니다. 사용되는 암호화 방식은 메시지 암호화 및 암호 해독에 사용되는 RMS 키를 얻은 위치에 따라 다릅니다.
  
- Microsoft Azure RMS 키 받기를 사용 하 여 암호화 모드 2 사용 됩니다. 암호화 모드 2는 업데이트 및 향상 된 AD RMS 암호화 구현 합니다. RSA 2048 서명 및 암호화를 지원 하 고 서명에 대 한 s h A-256을 지원 합니다.
    
- AD(Active Directory) RMS를 사용하여 키를 얻은 경우 암호화 모드 1 또는 암호화 모드 2가 사용됩니다. 사용되는 방법은 온-프레미스 AD RMS 배포에 따라 다릅니다. 암호화 모드 1은 원래 AD RMS 암호화 구현으로, 서명 및 암호화에 RSA 1024을 지원하고 서명에 SHA-1을 지원합니다. 이 모드는 RMS의 모든 현재 버전에서 계속 지원됩니다.
    
자세한 내용은 [AD RMS 암호화 모드](http://go.microsoft.com/fwlink/p/?LinkId=398616)를 참조 하십시오.
  
 **Q. 일부 암호화된 메시지에 Office365@messaging.microsoft.com에서 전송되었다고 표시되는 이유**
  
암호화된 회신 암호화 포털에서 또는 OME 뷰어 앱을 통해 전송되는 경우 암호화된 메시지는 Microsoft 끝점을 통해 전송되므로 보내는 전자 메일 주소는 Office365@messaging.microsoft.com으로 설정됩니다. 이를 통해 암호화된 메시지가 스팸으로 표시되지 않도록 합니다. 암호화 포털 안의 주소 및 전자 메일에 표시되는 이름은 이 레이블을 지정으로 인해 변경되지 않습니다. 또한 다른 전자 메일 클라이언트를 통해서가 아니라 해당 포털을 통해 보낸 메시지에만 이 레이블 지정을 적용합니다.
  
 **Q: 호스팅된 암호화 EHE (Exchange) 구독자 결정 합니다. 여기서 자세한 내용은 Office 365 메시지 암호화로 업그레이드 하는 방법에 대 한 확인할 수 있습니까?**
  
모든 EHE 고객이 Office 365 메시지 암호화로 업그레이드 되었습니다. 자세한 내용은 [Exchange 호스트 된 암호화 업그레이드 센터](http://go.microsoft.com/fwlink/p/?LinkID=511077)를 방문 합니다.
  
 **Q: 해야하는 모든 Url, IP 주소, 열기 또는 내 조직 방화벽에서 포트를 Office 365 메시지 암호화를 지원 합니까?**
  
예. Office 365 메시지 암호화로 암호화된 메시지를 인증할 수 있도록 Exchange Online의 URL을 조직의 허용 목록에 추가해야 합니다. Exchange Online URL 목록은 [Office 365 URLs and IP Address Ranges](https://support.office.com/article/f57e35b7-0a45-42f0-855e-11aa5e7f13fd.aspx)를 참조하세요.
  
 **Q. Office 365 암호화 메시지를 한 번에 몇 명에게 보낼 수 있습니까?**
  
암호화 된 메시지에 대 한 받는 사람 제한 메시지의 **받는** 사람 필드에 있는 문자의 수를 기반으로 합니다. 메일 그룹 확장) (이후이 결합 하는 경우 **받는** 사람 필드에 받는 사람 주소에는 11,980 자를 초과 하지 않아야 합니다. 문자 길이에서 전자 메일 주소 다를 수 있으므로 단일 암호화 된 메시지에 대 한 표준 받는 사람 제한은 없습니다. 
  
 **Q. 특정 받는 사람에게 보낸 메시지를 취소할 수 있습니까?**
  
아니요. 특정 사람에 게 메시지를 보낸 후 취소할 수 없습니다.
  
 **Q. 받아서 읽은 암호화된 메시지에 대한 보고서를 볼 수 있습니까?**
  
다음과 같은 경우 암호화 된 메시지에 본적, 하지만 대 한 특정 전송 규칙을 일치 하는 메시지의 수를 확인 하려면 활용할 수를 사용할 수 있는 Office 365 보고서를 표시 하는 보고서를 하지 않습니다.
  
 **Q. Microsoft는 OME 포털 및 OME 뷰어 앱을 통해 제공한 정보로 어떤 작업을 수행하나요?**
  
[Office 365 메시징 암호화 포털 개인정보취급방침](protected-message-viewer-portal-privacy-statement.md) Microsoft에서는 및 개인 사용자 정보로 수행 하지 하는 방법에 대 한 자세한 정보를 제공 합니다. 
  

