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
# <a name="add-your-organizations-brand-to-your-encrypted-messages"></a><span data-ttu-id="b921a-103">암호화된 메시지에 조직 브랜드 추가</span><span class="sxs-lookup"><span data-stu-id="b921a-103">Add your organization's brand to your encrypted messages</span></span>

<span data-ttu-id="b921a-p101">관리자는 Exchange Online 또는 Exchange Online 보호 조직의 Office 365 메시지 암호화 전자 메일 메시지의 모양 및 암호화 포털의 내용을 사용자 지정 브랜딩 회사를 적용할 수 있습니다. Get-omeconfiguration 및 Set-omeconfiguration Windows PowerShell cmdlet을 사용 하 여 암호화 된 전자 메일 메시지의 받는 사람에 대 한 보기 환경에서 다음과 같은 측면을 사용자 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b921a-p101">As an Exchange Online or Exchange Online Protection administrator, you can apply your company branding to customize the look of your organization's Office 365 Message Encryption email messages and the contents of the encryption portal. Using the Get-OMEConfiguration and Set-OMEConfiguration Windows PowerShell cmdlets, you can customize the following aspects of the viewing experience for recipients of encrypted email messages:</span></span>
  
- <span data-ttu-id="b921a-106">암호화된 메시지를 포함하는 전자 메일의 소개 텍스트</span><span class="sxs-lookup"><span data-stu-id="b921a-106">Introductory text of the email that contains the encrypted message</span></span>
    
- <span data-ttu-id="b921a-107">암호화된 메시지를 포함하는 전자 메일의 고지 사항 텍스트</span><span class="sxs-lookup"><span data-stu-id="b921a-107">Disclaimer text of the email that contains the encrypted message</span></span>
    
- <span data-ttu-id="b921a-108">OME 포털에 표시 되는 텍스트</span><span class="sxs-lookup"><span data-stu-id="b921a-108">Text that appears in the OME portal</span></span>
    
- <span data-ttu-id="b921a-109">전자 메일 메시지와 OME 포털에 표시 되는 로고</span><span class="sxs-lookup"><span data-stu-id="b921a-109">Logo that appears in the email message and OME portal</span></span>
    
- <span data-ttu-id="b921a-110">전자 메일 메시지와 OME 포털에 배경색</span><span class="sxs-lookup"><span data-stu-id="b921a-110">Background color in the email message and OME portal</span></span>
    
<span data-ttu-id="b921a-111">언제든지 기본 모양과 느낌으로 되돌릴 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b921a-111">You can also revert back to the default look and feel at any time.</span></span>
  
||
|:-----|
|<span data-ttu-id="b921a-p102">이 문서는 Office 365 메시지 암호화에 대 한 문서를 더 큰 시리즈의 일부입니다. 이 문서는 관리자 및 ITPros 위한 것입니다. 방금 경우 보내거나 암호화 된 메시지를 받는 방법에 대 한 정보에 대 한 자세한 내용은 [Office 365 메시지 암호화 OME ()](ome.md) 의 문서 목록을 참조 하 고 요구 사항에 가장 적합 한 문서를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="b921a-p102">This article is part of a larger series of articles about Office 365 Message Encryption. This article is intended for administrators and ITPros. If you're just looking for information on sending or receiving an encrypted message, see the list of articles in [Office 365 Message Encryption (OME)](ome.md) and locate the article that best fits your needs.</span></span> |
||
   
<span data-ttu-id="b921a-115">**조직의 브랜드로 OME 하 여 암호화 된 OME 포털 및 전자 메일 메시지의 모양을 사용자 지정 하려면**</span><span class="sxs-lookup"><span data-stu-id="b921a-115">**To customize the look of the OME portal and email messages encrypted by OME with your organization's brand**</span></span>
  
1. <span data-ttu-id="b921a-116">[Exchange Online를 사용 하 여 원격 PowerShell 연결](http://technet.microsoft.com/en-us/library/jj984289%28v=exchg.150%29.aspx)의 설명에 따라 원격 PowerShell을 사용 하는 Exchange Online에 연결 합니다.</span><span class="sxs-lookup"><span data-stu-id="b921a-116">Connect to Exchange Online using Remote PowerShell, as described in [Connect to Exchange Online Using Remote PowerShell](http://technet.microsoft.com/en-us/library/jj984289%28v=exchg.150%29.aspx).</span></span>
    
2. <span data-ttu-id="b921a-117">[Set-omeconfiguration](http://technet.microsoft.com/en-us/3ef0aec0-ce28-411d-abe8-7236f082af1b) 의 설명에 따라 Set-omeconfiguration cmdlet을 사용 하거나 지침에 대 한 다음 표를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="b921a-117">Use the Set-OMEConfiguration cmdlet as described in [Set-OMEConfiguration](http://technet.microsoft.com/en-us/3ef0aec0-ce28-411d-abe8-7236f082af1b) or use the following table for guidance.</span></span> 
    
<span data-ttu-id="b921a-118">**암호화 사용자 지정 옵션**</span><span class="sxs-lookup"><span data-stu-id="b921a-118">**Encryption customization options**</span></span>

|<span data-ttu-id="b921a-119">**암호화 환경에서 사용자 지정하려는 기능**</span><span class="sxs-lookup"><span data-stu-id="b921a-119">**To customize this feature of the encryption experience**</span></span>|<span data-ttu-id="b921a-120">**이러한 명령을 사용 하 여**</span><span class="sxs-lookup"><span data-stu-id="b921a-120">**Use these commands**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b921a-p103">암호화 된 전자 메일 메시지와 함께 제공 되는 기본 텍스트입니다. 암호화 된 메시지를 보기 위한 지침 위에 표시 되는 기본 텍스트</span><span class="sxs-lookup"><span data-stu-id="b921a-p103">Default text that accompanies encrypted email messages. The default text appears above the instructions for viewing encrypted messages</span></span>  <br/> | `Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> -EmailText "<String up to 1024 characters>"` <br/> <span data-ttu-id="b921a-123">**예제:**</span><span class="sxs-lookup"><span data-stu-id="b921a-123">**Example:**</span></span> <br/>  `Set-OMEConfiguration -Identity "OME Configuration" -EmailText "Encrypted message from ContosoPharma secure messaging system."`|
|<span data-ttu-id="b921a-124">암호화된 메시지를 포함하는 전자 메일의 고지 사항 설명문</span><span class="sxs-lookup"><span data-stu-id="b921a-124">Disclaimer statement in the email that contains the encrypted message</span></span>  <br/> | `Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> -DisclaimerText "<Disclaimer statement. String of up to 1024 characters.>"` <br/> <span data-ttu-id="b921a-125">**예제:**</span><span class="sxs-lookup"><span data-stu-id="b921a-125">**Example:**</span></span> <br/>  `Set-OMEConfiguration -Identity "OME Configuration" -DisclaimerText "This message is confidential for the use of the addressee only."` <br/> |
|<span data-ttu-id="b921a-126">암호화된 메일 보기 포털 위쪽에 표시되는 텍스트</span><span class="sxs-lookup"><span data-stu-id="b921a-126">Text that appears at the top of the encrypted mail viewing portal</span></span><br/> | `Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> -PortalText "<Text for your portal. String of up to 128 characters.>"` <br/> <span data-ttu-id="b921a-127">**예제:**</span><span class="sxs-lookup"><span data-stu-id="b921a-127">**Example:**</span></span> <br/>  `Set-OMEConfiguration -Identity "OME Configuration" -PortalText "ContosoPharma secure email portal."` <br/> |
|<span data-ttu-id="b921a-128">로고</span><span class="sxs-lookup"><span data-stu-id="b921a-128">Logo</span></span>  <br/> | `Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> -Image <Byte[]>` <br/> <span data-ttu-id="b921a-129">**예제:**</span><span class="sxs-lookup"><span data-stu-id="b921a-129">**Example:**</span></span> <br/>  `Set-OMEConfiguration -Identity "OME configuration" -Image (Get-Content "C:\Temp\contosologo.png" -Encoding byte)` <br/> <span data-ttu-id="b921a-130">지원되는 파일 형식: .png, .jpg, .bmp 또는 .tiff</span><span class="sxs-lookup"><span data-stu-id="b921a-130">Supported file formats: .png, .jpg, .bmp, or .tiff</span></span>  <br/> <span data-ttu-id="b921a-131">로고 파일의 최적 크기: 40KB 미만</span><span class="sxs-lookup"><span data-stu-id="b921a-131">Optimal size of logo file: less than 40 KB</span></span>  <br/> <span data-ttu-id="b921a-132">최적 로그 이미지 크기: 170x70 픽셀</span><span class="sxs-lookup"><span data-stu-id="b921a-132">Optimal size of logo image: 170x70 pixels</span></span>  <br/> |
|<span data-ttu-id="b921a-133">배경색</span><span class="sxs-lookup"><span data-stu-id="b921a-133">Background color</span></span>  <br/> | `Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> -BackgroundColor "<Hexadecimal color code>"` <br/> <span data-ttu-id="b921a-134">**예제:**</span><span class="sxs-lookup"><span data-stu-id="b921a-134">**Example:**</span></span> <br/>  `Set-OMEConfiguration -Identity "OME Configuration" -BackgroundColor "#ffffff"` <br/> |
   
<span data-ttu-id="b921a-135">**OME 하 여 암호화 된 OME 포털 및 전자 메일 메시지에서 브랜드 사용자 지정 항목을 제거 하려면**</span><span class="sxs-lookup"><span data-stu-id="b921a-135">**To remove brand customizations from the OME portal and email messages encrypted by OME**</span></span>
  
1. <span data-ttu-id="b921a-136">[Exchange Online를 사용 하 여 원격 PowerShell 연결](http://technet.microsoft.com/library/jj984289%28v=exchg.150%29.aspx)의 설명에 따라 원격 PowerShell을 사용 하는 Exchange Online에 연결 합니다.</span><span class="sxs-lookup"><span data-stu-id="b921a-136">Connect to Exchange Online using Remote PowerShell, as described in [Connect to Exchange Online Using Remote PowerShell](http://technet.microsoft.com/library/jj984289%28v=exchg.150%29.aspx).</span></span>
    
2. <span data-ttu-id="b921a-p104">[Set-omeconfiguration](http://technet.microsoft.com/3ef0aec0-ce28-411d-abe8-7236f082af1b)의 설명에 따라 Set-omeconfiguration cmdlet을 사용 합니다. PortalText 값을 빈 문자열 값을 설정 하 고 조직을 제거 하려면 DisclaimerText, EmailText에서 사용자 지정 브랜드의 `""`합니다. 모든 이미지 로고, 등의 값에 대 한 값을 설정 `"$null"`합니다.</span><span class="sxs-lookup"><span data-stu-id="b921a-p104">Use the Set-OMEConfiguration cmdlet as described in [Set-OMEConfiguration](http://technet.microsoft.com/3ef0aec0-ce28-411d-abe8-7236f082af1b). To remove your organization's branded customizations from the DisclaimerText, EmailText, and PortalText values, set the value to an empty string,  `""`. For all image values, such as Logo, set the value to  `"$null"`.</span></span>
    
<span data-ttu-id="b921a-140">**암호화 사용자 지정 옵션**</span><span class="sxs-lookup"><span data-stu-id="b921a-140">**Encryption customization options**</span></span>

<span data-ttu-id="b921a-141">**암호화 환경의 이 기능을 기본 텍스트 및 이미지로 되돌리려면**</span><span class="sxs-lookup"><span data-stu-id="b921a-141">**To revert this feature of the encryption experience back to the default text and image**</span></span>|<span data-ttu-id="b921a-142">**이러한 명령을 사용 하 여**</span><span class="sxs-lookup"><span data-stu-id="b921a-142">**Use these commands**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b921a-143">암호화된 전자 메일 메시지에 포함되는 기본 텍스트</span><span class="sxs-lookup"><span data-stu-id="b921a-143">Default text that accompanies encrypted email messages</span></span>  <br/> <span data-ttu-id="b921a-144">암호화된 메시지를 보기 위한 지침 위에 표시되는 기본 텍스트</span><span class="sxs-lookup"><span data-stu-id="b921a-144">The default text appears above the instructions for viewing encrypted messages</span></span>  <br/> | `Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> -EmailText "<empty string>"` <br/> <span data-ttu-id="b921a-145">**예제:**</span><span class="sxs-lookup"><span data-stu-id="b921a-145">**Example:**</span></span> <br/>  `Set-OMEConfiguration -Identity "OME Configuration" -EmailText ""` <br/> |
|<span data-ttu-id="b921a-146">암호화된 메시지를 포함하는 전자 메일의 고지 사항 설명문</span><span class="sxs-lookup"><span data-stu-id="b921a-146">Disclaimer statement in the email that contains the encrypted message</span></span>  <br/> | `Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> DisclaimerText "<empty string>"` <br/> <span data-ttu-id="b921a-147">**예제:**</span><span class="sxs-lookup"><span data-stu-id="b921a-147">**Example:**</span></span> <br/>  `Set-OMEConfiguration -Identity "OME Configuration" -DisclaimerText ""` <br/> |
|<span data-ttu-id="b921a-148">암호화된 메일 보기 포털 위쪽에 표시되는 텍스트</span><span class="sxs-lookup"><span data-stu-id="b921a-148">Text that appears at the top of the encrypted mail viewing portal</span></span>  <br/> | `Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> -PortalText "<empty string>"` <br/> <span data-ttu-id="b921a-149">**예제 되돌리기에 대 한 저장 기본값:**</span><span class="sxs-lookup"><span data-stu-id="b921a-149">**Example reverting back to default:**</span></span> <br/>  `Set-OMEConfiguration -Identity "OME Configuration" -PortalText ""` <br/> |
|<span data-ttu-id="b921a-150">로고</span><span class="sxs-lookup"><span data-stu-id="b921a-150">Logo</span></span>  <br/> | `Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> -Image <"$null">` <br/> <span data-ttu-id="b921a-151">**예제 되돌리기에 대 한 저장 기본값:**</span><span class="sxs-lookup"><span data-stu-id="b921a-151">**Example reverting back to default:**</span></span> <br/>  `Set-OMEConfiguration -Identity "OME configuration" -Image $null` <br/> |
|<span data-ttu-id="b921a-152">배경색</span><span class="sxs-lookup"><span data-stu-id="b921a-152">Background color</span></span>  <br/> | `Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> -BackgroundColor <"$null">` <br/> <span data-ttu-id="b921a-153">**예제 되돌리기에 대 한 저장 기본값:**</span><span class="sxs-lookup"><span data-stu-id="b921a-153">**Example reverting back to default:**</span></span> <br/>  `Set-OMEConfiguration -Identity "OME configuration" -BackgroundColor $null` <br/> |
   

