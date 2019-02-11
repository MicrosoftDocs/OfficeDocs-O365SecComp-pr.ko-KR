---
title: 조직 브랜드를 암호화 된 메시지에 추가
ms.author: krowley
author: kccross
manager: laurawi
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 7a29260d-2959-42aa-8916-feceff6ee51d
description: Exchange 관리자 권한으로 조직의 브랜딩 조직의 암호화 된 전자 메일 메시지와 암호화 포털의 내용에 적용할 수 있습니다.
ms.openlocfilehash: 4b22b72a8b77c2978a7cf25166978759119c272c
ms.sourcegitcommit: 7e2a0185cadea7f3a6afc5ddc445eac2e1ce22eb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/11/2019
ms.locfileid: "29696222"
---
# <a name="add-your-organizations-brand-to-your-encrypted-messages"></a>암호화된 메시지에 조직의 브랜드 추가

관리자는 Exchange Online 또는 Exchange Online 보호 조직의 Office 365 메시지 암호화 전자 메일 메시지의 모양 및 암호화 포털의 내용을 사용자 지정 브랜딩 회사를 적용할 수 있습니다. Get-omeconfiguration 및 Set-omeconfiguration Windows PowerShell cmdlet을 사용 하 여 암호화 된 전자 메일 메시지의 받는 사람에 대 한 보기 환경에서 다음과 같은 측면을 사용자 지정할 수 있습니다.
  
- 암호화된 메시지를 포함하는 전자 메일의 소개 텍스트
- 암호화된 메시지를 포함하는 전자 메일의 고지 사항 텍스트
- OME 포털에 표시 되는 텍스트
- 전자 메일 메시지와 OME 포털에 표시 되는 로고
- 전자 메일 메시지와 OME 포털에 배경색

언제든지 기본 모양과 느낌으로 되돌릴 수 있습니다.

더 많은 제어를 원하는 경우에 조직에서 시작 되는 암호화 된 전자 메일에 대 한 여러 서식 파일을 만들 수 있습니다. 이러한 서식 파일을 사용 하 여, 전자 메일 메시지의 모양 및 느낌 이상의 것을 제어할 수 있지만 최종 사용자 경험의 부분을 제어할 수도 있습니다. 등의 받는 사람 메일 서식이 파일이 적용 된이 고 Google, yahoo 및 Microsoft 계정을 사용 하는 사용자 Office 365 메시지 암호화 포털에 로그인 하려면 이러한 계정을 사용할 수 있는지 여부를 지정할 수 있습니다. 여러 사용 사례는 다음과 같이 데 서식 파일을 사용할 수 있습니다.

- 예: 재무, 판매 등의 각 부서에 대 한 서식 파일입니다.
- 서로 다른 제품에 대 한 서식 파일
- 서로 다른 각 지역 또는 국가 대 한 서식 파일

서식 파일을 만든 후 Exchange 메일 흐름 규칙을 사용 하 여 암호화 된 전자 메일 적용할 수 있습니다. 이러한 서식 파일을 사용 하 여 브랜드 되는 모든 메일을 해지할 수 있습니다.
  
||
|:-----|
|이 문서는 Office 365 메시지 암호화에 대 한 문서를 더 큰 시리즈의 일부입니다. 이 문서는 관리자 및 ITPros 위한 것입니다. 방금 경우 보내거나 암호화 된 메시지를 받는 방법에 대 한 정보에 대 한 자세한 내용은 [Office 365 메시지 암호화 OME ()](ome.md) 의 문서 목록을 참조 하 고 요구 사항에 가장 적합 한 문서를 찾습니다. |
||

## <a name="create-branding-templates"></a>브랜딩 서식 파일 만들기

새로 만들기 OMEConfiguration cmdlet과 함께 Windows PowerShell에서 조직에 대 한 브랜딩 서식 파일을 만듭니다. 다음은 서식 파일을 만든 후 Set-omeconfiguration cmdlet을 사용 하 여 서식 파일의 부분을 정의 합니다. 여러 서식 파일을 만들 수 있습니다.

![사용자 지정할 수 있는 전자 메일 부분](media/ome-template-breakout.png)
  
1. Office 365 조직에 대 한 전역 관리자 권한이 있는 작업이 나 교육용 계정을 사용 하는 Windows PowerShell 세션을 시작 하 고 Exchange Online에 연결 합니다. 자세한 내용은 [Connect to Exchange Online PowerShell를](https://aka.ms/exopowershell)참조 하십시오.

2. 새 서식 파일을 만들려면 새로 만들기 OMEConfiguration cmdlet을 사용 합니다.
     ```powershell
     New-OMEConfiguration -Identity <OMEConfigurationIdParameter>
     ```
     예:
     ```powershell
     New-OMEConfiguration -Identity <Branding template 1>
     ```
3. [Set-omeconfiguration](https://docs.microsoft.com/powershell/module/exchange/encryption-and-certificates/Set-OMEConfiguration) 의 설명에 따라 Set-omeconfiguration cmdlet을 사용 하 여 정의 된 서식 파일에 대 한 사용자 지정을 정의 하거나 지침에 대 한 다음 표를 사용 합니다.

|**암호화 환경에서 사용자 지정하려는 기능**|**이러한 명령을 사용 하 여**|
|:-----|:-----|
|배경색  <br/> | `Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> -BackgroundColor "<Hexadecimal color code>"` <br/> **예제:** <br/>  `Set-OMEConfiguration -Identity "Branding Template 1" -BackgroundColor "#ffffff"` <br/> |
|로고  <br/> | `Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> -Image <Byte[]>` <br/> **예제:** <br/>  `Set-OMEConfiguration -Identity "Branding Template 1" -Image (Get-Content "C:\Temp\contosologo.png" -Encoding byte)` <br/> 지원되는 파일 형식: .png, .jpg, .bmp 또는 .tiff  <br/> 로고 파일의 최적 크기: 40KB 미만  <br/> 최적 로그 이미지 크기: 170x70 픽셀  <br/> |
|보낸 사람의 이름과 전자 메일 주소 옆에 있는 텍스트| `Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> -IntroductionText "<String up to 1024 characters>"` <br/> **예제:** <br/>  `Set-OMEConfiguration -Identity "Branding Template 1" -IntroductionText "has sent you a secure message."`|
|"읽기 메시지" 단추에 표시 되는 텍스트| `Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> -ReadButtonText "<String up to 1024 characters>"` <br/> **예제:** <br/>  `Set-OMEConfiguration -Identity "OME Configuration" -ReadButtonText "Read Secure Message."`|
|아래 "메시지 읽기" 단추 위에 표시 되는 텍스트| `Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> -EmailText "<String up to 1024 characters>"` <br/> **예제:** <br/>  `Set-OMEConfiguration -Identity "OME Configuration" -EmailText "Encrypted message from ContosoPharma secure messaging system."`|
|암호화된 메시지를 포함하는 전자 메일의 고지 사항 설명문  <br/> | `Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> -DisclaimerText "<Disclaimer statement. String of up to 1024 characters.>"` <br/> **예제:** <br/>  `Set-OMEConfiguration -Identity "Branding Template 1" -DisclaimerText "This message is confidential for the use of the addressee only."`|
|암호화된 메일 보기 포털 위쪽에 표시되는 텍스트<br/> | `Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> -PortalText "<Text for your portal. String of up to 128 characters.>"` <br/> **예제:** <br/>  `Set-OMEConfiguration -Identity "OME Configuration" -PortalText "ContosoPharma secure email portal."` <br/> |
|사용 하도록 설정 하거나이 사용자 지정 서식 파일에 대 한 일회용 암호를 사용 하 여 인증을 사용 하지 않도록 설정 하려면| `Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> -OTPEnabled <$true|$false>` <br/> **예제:** <br/>이 사용자 지정 서식 파일에 대 한 일회용 암호 코드를 사용 하도록 설정 하려면 <br/>  `Set-OMEConfiguration -Identity "Branding Template 1" -OTPEnabled $true` <br/> 이 사용자 지정 서식 파일에 대 한 일회용 암호 코드를 사용 하지 않도록 설정 하려면 <br/>  `Set-OMEConfiguration -Identity "Branding Template 1" -OTPEnabled $false`|
|사용 하도록 설정 하거나이 사용자 지정 서식 파일에 대 한 Microsoft, Google, 또는 yahoo id 가진 인증을 사용 하지 않도록 설정 하려면| `Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> -SocialIdSignIn <$true|$false>` <br/> **예제:** <br/>이 사용자 지정 서식 파일에 대 한 공유 Id를 사용 하도록 설정 하려면 <br/>  `Set-OMEConfiguration -Identity "Branding Template 1" -SocialIdSignIn $true` <br/> 이 사용자 지정 서식 파일에 대 한 공유 Id를 사용 하지 않도록 설정 하려면 <br/>  `Set-OMEConfiguration -Identity "Branding Template 1" -SocialIdSignIn $false`|

## <a name="to-remove-brand-customizations-from-the-ome-portal-and-email-messages-encrypted-by-ome"></a>OME 하 여 암호화 된 OME 포털 및 전자 메일 메시지에서 브랜드 사용자 지정 항목을 제거 하려면
  
1. [Exchange Online PowerShell에 연결합니다](https://aka.ms/exopowershell).

2. [Set-omeconfiguration](https://docs.microsoft.com/powershell/module/exchange/encryption-and-certificates/Set-OMEConfiguration)의 설명에 따라 Set-omeconfiguration cmdlet을 사용 합니다. PortalText 값을 빈 문자열 값을 설정 하 고 조직을 제거 하려면 DisclaimerText, EmailText에서 사용자 지정 브랜드의 `""`합니다. 모든 이미지 로고, 등의 값에 대 한 값을 설정 `"$null"`합니다.

**암호화 사용자 지정 옵션**

**암호화 환경의 이 기능을 기본 텍스트 및 이미지로 되돌리려면**|**이러한 명령을 사용 하 여**|
|:-----|:-----|
|암호화된 전자 메일 메시지에 포함되는 기본 텍스트  <br/> 암호화된 메시지를 보기 위한 지침 위에 표시되는 기본 텍스트| `Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> -EmailText "<empty string>"` <br/> **예제:** <br/>  `Set-OMEConfiguration -Identity "OME Configuration" -EmailText ""`|
|암호화된 메시지를 포함하는 전자 메일의 고지 사항 설명문| `Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> DisclaimerText "<empty string>"` <br/> **예제:** <br/>  `Set-OMEConfiguration -Identity "OME Configuration" -DisclaimerText ""`|
|암호화된 메일 보기 포털 위쪽에 표시되는 텍스트| `Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> -PortalText "<empty string>"` <br/> **예제 되돌리기에 대 한 저장 기본값:** <br/>  `Set-OMEConfiguration -Identity "OME Configuration" -PortalText ""` <br/> |
|로고| `Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> -Image <"$null">` <br/> **예제 되돌리기에 대 한 저장 기본값:** <br/>  `Set-OMEConfiguration -Identity "OME configuration" -Image $null`|
|배경색| `Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> -BackgroundColor <"$null">` <br/> **예제 되돌리기에 대 한 저장 기본값:** <br/>  `Set-OMEConfiguration -Identity "OME configuration" -BackgroundColor $null`|

## <a name="create-an-exchange-mail-flow-rule-that-applies-custom-branding-to-encrypted-emails"></a>사용자 지정 브랜딩 암호화 된 전자 메일에 적용 되는 Exchange 메일 흐름 규칙을 만들기

브랜딩 서식 파일을 만든 후 특정 조건에 따라 해당 사용자 지정 브랜딩 적용할 Exchange 메일 흐름 규칙 만들 수 있습니다. 이러한 규칙은 다음과 같은 시나리오에서 사용자 지정 브랜딩 적용 됩니다.

- 전자 메일 수동으로 Outlook 또는 OWA 클라이언트에서 최종 사용자가 암호화 된 경우
- 전자 메일 자동으로 Exchange 메일 흐름 규칙 또는 Office 365 데이터 손실 방지 정책에서 암호화 된 경우

암호화 적용 되는 Exchange 메일 흐름 규칙을 만드는 방법에 대 한 자세한 내용은 [Office 365에서 전자 메일 메시지를 암호화 메일 흐름 규칙 정의](define-mail-flow-rules-to-encrypt-email.md)참조 하십시오.

1. 웹 브라우저에서 [Office 365에 로그인](https://support.office.com/article/b9582171-fd1f-4284-9846-bdd72bb28426#ID0EAABAAA=Web_browser)전역 관리자 권한을 부여 하는 작업이 나 교육용 계정을 사용 하 여 합니다.

2. **Admin** 타일을 선택 합니다.

3. Office 365 관리 센터에서 **관리 센터** \> **Exchange**를 선택합니다.

4. EAC에서 **메일 흐름** 으로 이동 \> **규칙** 및 선택 **새로** ![새 아이콘](media/457cd93f-22c2-4571-9f83-1b129bcfb58e.gif) \> **새 규칙 만들기**. EAC를 사용 하는 방법에 대 한 자세한 내용은 [Exchange Online의 Exchange 관리 센터](https://docs.microsoft.com/exchange/exchange-admin-center)를 참조 하십시오.

5. **이름**영업 부서에 대 한 브랜딩 등 규칙에 대 한 이름을 입력 합니다.

6. **하는 경우이 규칙 적용** 에서 조건을 선택, 사용 가능한 조건 목록에서 원하는 다른 조건 뿐아니라 **보낸 사람이 조직 내부에 있는** 조건을 선택 합니다. 등 특정 브랜드 서식 파일을 적용 하려는 될 수 있습니다.

     - 재무 부서의 구성원에서 보낸 모든 암호화 된 전자 메일
     - "외부" 또는 "파트너" 등의 특정 키워드를 사용 하 여 보낸 암호화 된 전자 메일
     - 특정 도메인으로 전송 하는 암호화 된 전자 메일

7. **다음을 수행**하십시오에서 **메시지 보안 수정**을 선택 > **OME 메시지에 브랜딩 사용자 지정 적용**합니다. 다음으로, 드롭다운 메뉴에서 만든 것에서 브랜딩 서식 파일을 선택 합니다.
8. (선택 사항) 메일 흐름 규칙을도 사용자 지정 외에도 암호화를 적용 하려는 경우 **메시지 보안 수정** 을 선택 하 고 **Office 365 메시지 암호화 적용 및 권한 보호를**선택 브랜딩에서 **다음을 수행**합니다. 목록에서 RMS 템플릿을 선택, **저장**을 선택 하 고 **확인**을 선택 합니다.
  
     모든 기본 서식 파일을 포함 하는 서식 파일 목록이 및 Office 365에서으로 옵션에 대해 만든 모든 사용자 지정 서식 파일을 사용 합니다. 목록이 비어 있으면 설정 되었는지 확인 하면가 Office 365 메시지 암호화 새 기능을 함께 [새로운 Office 365 메시지 암호화 기능 설정](set-up-new-message-encryption-capabilities.md)의 설명에 따라 합니다. 기본 서식 파일에 대 한 정보를 [구성 하 고 Azure 정보 보호에 대 한 서식 파일 관리](https://docs.microsoft.com/information-protection/deploy-use/configure-policy-templates)를 참조 하십시오. **전달 하지 않음** 옵션에 대 한 정보를 [전자 메일 전달 하지 않음 옵션](https://docs.microsoft.com/information-protection/deploy-use/configure-usage-rights#do-not-forward-option-for-emails)을 참조 하십시오. **만 암호화** 옵션에 대 한 정보를 [전자 메일만 암호화 옵션](https://docs.microsoft.com/information-protection/deploy-use/configure-usage-rights#encrypt-only-option-for-emails)을 참조 하십시오.

     다른 작업을 지정 하려면 **작업 추가** 선택할 수 있습니다.
