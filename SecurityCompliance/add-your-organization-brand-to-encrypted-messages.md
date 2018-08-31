---
title: 조직 브랜드를 암호화 된 메시지에 추가
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 11/2/2017
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 7a29260d-2959-42aa-8916-feceff6ee51d
description: 'Exchange 관리자 권한으로 조직의 브랜딩 조직의 암호화 된 전자 메일 메시지와 암호화 포털의 내용에 적용할 수 있습니다. '
ms.openlocfilehash: 2f34b5cea3155f587fd7787f1f69270d1373400b
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22533516"
---
# <a name="add-your-organizations-brand-to-your-encrypted-messages"></a>암호화된 메시지에 조직 브랜드 추가

관리자는 Exchange Online 또는 Exchange Online 보호 조직의 Office 365 메시지 암호화 전자 메일 메시지의 모양 및 암호화 포털의 내용을 사용자 지정 브랜딩 회사를 적용할 수 있습니다. Get-omeconfiguration 및 Set-omeconfiguration Windows PowerShell cmdlet을 사용 하 여 암호화 된 전자 메일 메시지의 받는 사람에 대 한 보기 환경에서 다음과 같은 측면을 사용자 지정할 수 있습니다.
  
- 암호화된 메시지를 포함하는 전자 메일의 소개 텍스트
    
- 암호화된 메시지를 포함하는 전자 메일의 고지 사항 텍스트
    
- OME 포털에 표시 되는 텍스트
    
- 전자 메일 메시지와 OME 포털에 표시 되는 로고
    
- 전자 메일 메시지와 OME 포털에 배경색
    
언제든지 기본 모양과 느낌으로 되돌릴 수 있습니다.
  
||
|:-----|
|이 문서는 Office 365 메시지 암호화에 대 한 문서를 더 큰 시리즈의 일부입니다. 이 문서는 관리자 및 ITPros 위한 것입니다. 방금 경우 보내거나 암호화 된 메시지를 받는 방법에 대 한 정보에 대 한 자세한 내용은 [Office 365 메시지 암호화 OME ()](ome.md) 의 문서 목록을 참조 하 고 요구 사항에 가장 적합 한 문서를 찾습니다. |
||
   
**조직의 브랜드로 OME 하 여 암호화 된 OME 포털 및 전자 메일 메시지의 모양을 사용자 지정 하려면**
  
1. [Exchange Online를 사용 하 여 원격 PowerShell 연결](http://technet.microsoft.com/en-us/library/jj984289%28v=exchg.150%29.aspx)의 설명에 따라 원격 PowerShell을 사용 하는 Exchange Online에 연결 합니다.
    
2. [Set-omeconfiguration](http://technet.microsoft.com/en-us/3ef0aec0-ce28-411d-abe8-7236f082af1b) 의 설명에 따라 Set-omeconfiguration cmdlet을 사용 하거나 지침에 대 한 다음 표를 사용 합니다. 
    
**암호화 사용자 지정 옵션**

|**암호화 환경에서 사용자 지정하려는 기능**|**이러한 명령을 사용 하 여**|
|:-----|:-----|
|암호화 된 전자 메일 메시지와 함께 제공 되는 기본 텍스트입니다. 암호화 된 메시지를 보기 위한 지침 위에 표시 되는 기본 텍스트  <br/> | `Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> -EmailText "<String up to 1024 characters>"` <br/> **예제:** <br/>  `Set-OMEConfiguration -Identity "OME Configuration" -EmailText "Encrypted message from ContosoPharma secure messaging system."`|
|암호화된 메시지를 포함하는 전자 메일의 고지 사항 설명문  <br/> | `Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> -DisclaimerText "<Disclaimer statement. String of up to 1024 characters.>"` <br/> **예제:** <br/>  `Set-OMEConfiguration -Identity "OME Configuration" -DisclaimerText "This message is confidential for the use of the addressee only."` <br/> |
|암호화된 메일 보기 포털 위쪽에 표시되는 텍스트<br/> | `Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> -PortalText "<Text for your portal. String of up to 128 characters.>"` <br/> **예제:** <br/>  `Set-OMEConfiguration -Identity "OME Configuration" -PortalText "ContosoPharma secure email portal."` <br/> |
|로고  <br/> | `Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> -Image <Byte[]>` <br/> **예제:** <br/>  `Set-OMEConfiguration -Identity "OME configuration" -Image (Get-Content "C:\Temp\contosologo.png" -Encoding byte)` <br/> 지원되는 파일 형식: .png, .jpg, .bmp 또는 .tiff  <br/> 로고 파일의 최적 크기: 40KB 미만  <br/> 최적 로그 이미지 크기: 170x70 픽셀  <br/> |
|배경색  <br/> | `Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> -BackgroundColor "<Hexadecimal color code>"` <br/> **예제:** <br/>  `Set-OMEConfiguration -Identity "OME Configuration" -BackgroundColor "#ffffff"` <br/> |
   
**OME 하 여 암호화 된 OME 포털 및 전자 메일 메시지에서 브랜드 사용자 지정 항목을 제거 하려면**
  
1. [Exchange Online를 사용 하 여 원격 PowerShell 연결](http://technet.microsoft.com/library/jj984289%28v=exchg.150%29.aspx)의 설명에 따라 원격 PowerShell을 사용 하는 Exchange Online에 연결 합니다.
    
2. [Set-omeconfiguration](http://technet.microsoft.com/3ef0aec0-ce28-411d-abe8-7236f082af1b)의 설명에 따라 Set-omeconfiguration cmdlet을 사용 합니다. PortalText 값을 빈 문자열 값을 설정 하 고 조직을 제거 하려면 DisclaimerText, EmailText에서 사용자 지정 브랜드의 `""`합니다. 모든 이미지 로고, 등의 값에 대 한 값을 설정 `"$null"`합니다.
    
**암호화 사용자 지정 옵션**

**암호화 환경의 이 기능을 기본 텍스트 및 이미지로 되돌리려면**|**이러한 명령을 사용 하 여**|
|:-----|:-----|
|암호화된 전자 메일 메시지에 포함되는 기본 텍스트  <br/> 암호화된 메시지를 보기 위한 지침 위에 표시되는 기본 텍스트  <br/> | `Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> -EmailText "<empty string>"` <br/> **예제:** <br/>  `Set-OMEConfiguration -Identity "OME Configuration" -EmailText ""` <br/> |
|암호화된 메시지를 포함하는 전자 메일의 고지 사항 설명문  <br/> | `Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> DisclaimerText "<empty string>"` <br/> **예제:** <br/>  `Set-OMEConfiguration -Identity "OME Configuration" -DisclaimerText ""` <br/> |
|암호화된 메일 보기 포털 위쪽에 표시되는 텍스트  <br/> | `Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> -PortalText "<empty string>"` <br/> **예제 되돌리기에 대 한 저장 기본값:** <br/>  `Set-OMEConfiguration -Identity "OME Configuration" -PortalText ""` <br/> |
|로고  <br/> | `Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> -Image <"$null">` <br/> **예제 되돌리기에 대 한 저장 기본값:** <br/>  `Set-OMEConfiguration -Identity "OME configuration" -Image $null` <br/> |
|배경색  <br/> | `Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> -BackgroundColor <"$null">` <br/> **예제 되돌리기에 대 한 저장 기본값:** <br/>  `Set-OMEConfiguration -Identity "OME configuration" -BackgroundColor $null` <br/> |
   

