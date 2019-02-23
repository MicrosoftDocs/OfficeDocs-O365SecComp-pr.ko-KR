---
title: 데이터 거버넌스 권장 사항을 표시하기 위해 콘텐츠가 식별되는 방법
ms.author: brendonb
author: stephow-MSFT
manager: laurawi
ms.date: 1/15/2019
ms.audience: Admin
ms.topic: overview
ms.service: O365-seccomp
localization_priority: Priority
search.appverid:
- MOE150
- MET150
ROBOTS: NOINDEX, NOFOLLOW
description: 'Office 365 보안 및 준수 센터는 조직의 현재 설정을 기반으로 데이터 거버넌스 권장 사항을 제공하며 몇 번의 클릭만으로 설정을 완료할 수 있는 기능을 서비스합니다. 이 권장 사항의 일부는 조직 내의 특정 콘텐츠를 검색한 후 해당 콘텐츠를 관리하는 단계별 방법을 권장합니다. 예를 들어, 권장 사항이 비즈니스 측면에서 중요한 콘텐츠(예: 비공개 유지 권한 또는 NDA 정보)가 포함된 항목을 검색할 수 있으며, 사용자는 해당 항목에 보존 레이블을 자동으로 적용하여 필요에 따라 해당 항목을 분류하고 보존할 수 있습니다. 이 항목에는 사용자가 확인할 수 있는 데이터 거버넌스 권장 사항이 나열되어 있으며 각 권장 사항을 표시하기 위해 어떤 콘텐츠가 검색되는지 설명합니다.'
ms.openlocfilehash: 24e41501ed11d54e60f8b3d9f27a2e96f3cde112
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30220438"
---
# <a name="how-content-is-identified-for-data-governance-recommendations"></a><span data-ttu-id="c32a7-106">데이터 거버넌스 권장 사항을 표시하기 위해 콘텐츠가 식별되는 방법</span><span class="sxs-lookup"><span data-stu-id="c32a7-106">How content is identified for data-governance recommendations</span></span>

<span data-ttu-id="c32a7-p102">Office 365 보안 및 준수 센터는 조직의 현재 설정을 기반으로 데이터 거버넌스 권장 사항을 제공하며 몇 번의 클릭만으로 설정을 완료할 수 있는 기능을 서비스합니다. 이 권장 사항의 일부는 조직 내의 특정 콘텐츠를 검색한 후 해당 콘텐츠를 관리하는 단계별 방법을 권장합니다. 예를 들어, 권장 사항이 비즈니스 측면에서 중요한 콘텐츠(예: 비공개 유지 권한 또는 NDA 정보)가 포함된 항목을 검색할 수 있으며, 사용자는 해당 항목에 보존 레이블을 자동으로 적용하여 필요에 따라 해당 항목을 분류하고 보존할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c32a7-p102">The Office 365 Security & Compliance Center provides recommendations for data governance based on your org's current setup and lets you set things up in a couple clicks. Some of these recommendations detect specific content in your organization and then provide recommended steps for managing that content. For example, a recommendation might detect items that contain business-critical content (such as attorney-client privilege or NDA info), and then let you automatically apply a retention label to those items to ensure that they’re classified and retained as needed.</span></span>

<span data-ttu-id="c32a7-110">이 항목에는 사용자가 확인할 수 있는 데이터 거버넌스 권장 사항이 나열되어 있으며 각 권장 사항을 표시하기 위해 어떤 콘텐츠가 검색되는지 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="c32a7-110">This topic lists the data-governance recommendations you might see and describes what content is detected to trigger each one.</span></span>

## <a name="clean-up-voicemail"></a><span data-ttu-id="c32a7-111">음성 사서함 정리</span><span class="sxs-lookup"><span data-stu-id="c32a7-111">Clean up voicemail</span></span>

<span data-ttu-id="c32a7-p103">‘음성 메일’ 메시지 유형으로 식별된 전자 메일 메시지가 사용자의 사서함에서 감지되었을 때 이 권장 사항이 표시됩니다. [Exchange에서의 메시지 속성](https://docs.microsoft.com/en-us/exchange/policy-and-compliance/ediscovery/message-properties-and-search-operators?view=exchserver-2019#searchable-properties-in-exchange)에 대해 자세히 알아보세요.</span><span class="sxs-lookup"><span data-stu-id="c32a7-p103">This recommendation appears when email messages identified as the message type ‘voicemail’ are detected in users’ mailboxes. Learn more about [message properties in Exchange](https://docs.microsoft.com/en-us/exchange/policy-and-compliance/ediscovery/message-properties-and-search-operators?view=exchserver-2019#searchable-properties-in-exchange).</span></span>

## <a name="label-attorney-client-privilege-content"></a><span data-ttu-id="c32a7-114">비공개 유지 권한 콘텐츠 레이블 지정</span><span class="sxs-lookup"><span data-stu-id="c32a7-114">Label attorney-client privilege content</span></span> 

<span data-ttu-id="c32a7-115">다음 중 한 가지 조건이 충족되면 이 권장 사항이 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="c32a7-115">This recommendation appears when either of the following criteria are met.</span></span>

- <span data-ttu-id="c32a7-116">전자 메일 메시지의 본문에서 다음 키워드 조합이 검색되는 경우:</span><span class="sxs-lookup"><span data-stu-id="c32a7-116">Any of combination of these keywords is detected in the body of an email message:</span></span>
    - <span data-ttu-id="c32a7-117">ACP</span><span class="sxs-lookup"><span data-stu-id="c32a7-117">ACP</span></span>
    - <span data-ttu-id="c32a7-118">비공개 유지 권한</span><span class="sxs-lookup"><span data-stu-id="c32a7-118">Attorney Client Privilege</span></span>
    - <span data-ttu-id="c32a7-119">비공개 유지 권한</span><span class="sxs-lookup"><span data-stu-id="c32a7-119">Attorney-Client Privilege</span></span>
    - <span data-ttu-id="c32a7-120">비공개 유지 권한</span><span class="sxs-lookup"><span data-stu-id="c32a7-120">Attorney-Client Privileged</span></span>

- <span data-ttu-id="c32a7-121">SharePoint 또는 OneDrive 파일에서 다음 키워드 조합이 검색되는 경우:</span><span class="sxs-lookup"><span data-stu-id="c32a7-121">Any combination of these keywords are detected in SharePoint or OneDrive files:</span></span>
    - <span data-ttu-id="c32a7-122">ACP</span><span class="sxs-lookup"><span data-stu-id="c32a7-122">ACP</span></span>
    - <span data-ttu-id="c32a7-123">비공개 유지 권한\*</span><span class="sxs-lookup"><span data-stu-id="c32a7-123">Attorney Client Privilege\*</span></span>
    - <span data-ttu-id="c32a7-124">AC 권한</span><span class="sxs-lookup"><span data-stu-id="c32a7-124">AC Privilege</span></span>

## <a name="retain-audio-files"></a><span data-ttu-id="c32a7-125">오디오 파일 보존</span><span class="sxs-lookup"><span data-stu-id="c32a7-125">Retain audio files</span></span>

<span data-ttu-id="c32a7-126">SharePoint 또는 OneDrive에서 다음 파일 형식이 검색되면 이 권장 사항이 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="c32a7-126">This recommendation appears when any of the following file types are detected in SharePoint or OneDrive.</span></span>

- <span data-ttu-id="c32a7-127">.MP3</span><span class="sxs-lookup"><span data-stu-id="c32a7-127">.MP3</span></span>
- <span data-ttu-id="c32a7-128">.WMA</span><span class="sxs-lookup"><span data-stu-id="c32a7-128">.WMA</span></span>
- <span data-ttu-id="c32a7-129">.WAV</span><span class="sxs-lookup"><span data-stu-id="c32a7-129">.WAV</span></span>
- <span data-ttu-id="c32a7-130">.RA</span><span class="sxs-lookup"><span data-stu-id="c32a7-130">.RA</span></span>
- <span data-ttu-id="c32a7-131">.RAM</span><span class="sxs-lookup"><span data-stu-id="c32a7-131">.RAM</span></span>
- <span data-ttu-id="c32a7-132">.RM</span><span class="sxs-lookup"><span data-stu-id="c32a7-132">.RM</span></span>
- <span data-ttu-id="c32a7-133">.MID</span><span class="sxs-lookup"><span data-stu-id="c32a7-133">.MID</span></span>
- <span data-ttu-id="c32a7-134">.OGG</span><span class="sxs-lookup"><span data-stu-id="c32a7-134">.OGG</span></span>
- <span data-ttu-id="c32a7-135">.AIFF</span><span class="sxs-lookup"><span data-stu-id="c32a7-135">.AIFF</span></span>
- <span data-ttu-id="c32a7-136">.PCM</span><span class="sxs-lookup"><span data-stu-id="c32a7-136">.PCM</span></span>
- <span data-ttu-id="c32a7-137">.AAC</span><span class="sxs-lookup"><span data-stu-id="c32a7-137">.AAC</span></span>
- <span data-ttu-id="c32a7-138">.FLAC</span><span class="sxs-lookup"><span data-stu-id="c32a7-138">.FLAC</span></span>
- <span data-ttu-id="c32a7-139">.ALAC</span><span class="sxs-lookup"><span data-stu-id="c32a7-139">.ALAC</span></span>

## <a name="retain-cad-files"></a><span data-ttu-id="c32a7-140">CAD 파일 보존</span><span class="sxs-lookup"><span data-stu-id="c32a7-140">Retain CAD files</span></span>

<span data-ttu-id="c32a7-141">SharePoint 또는 OneDrive에서 다음 파일 형식이 검색되면 이 권장 사항이 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="c32a7-141">This recommendation appears when any of the following file types are detected in SharePoint or OneDrive.</span></span>

- <span data-ttu-id="c32a7-142">.3DXML</span><span class="sxs-lookup"><span data-stu-id="c32a7-142">.3DXML</span></span>
- <span data-ttu-id="c32a7-143">.ACIS</span><span class="sxs-lookup"><span data-stu-id="c32a7-143">.ACIS</span></span>
- <span data-ttu-id="c32a7-144">.ARC</span><span class="sxs-lookup"><span data-stu-id="c32a7-144">.ARC</span></span>
- <span data-ttu-id="c32a7-145">.ASM</span><span class="sxs-lookup"><span data-stu-id="c32a7-145">.ASM</span></span>
- <span data-ttu-id="c32a7-146">.CAT\*</span><span class="sxs-lookup"><span data-stu-id="c32a7-146">.CAT\*</span></span>
- <span data-ttu-id="c32a7-147">.CGR</span><span class="sxs-lookup"><span data-stu-id="c32a7-147">.CGR</span></span>
- <span data-ttu-id="c32a7-148">.DW\*</span><span class="sxs-lookup"><span data-stu-id="c32a7-148">.DW\*</span></span>
- <span data-ttu-id="c32a7-149">.DX\*</span><span class="sxs-lookup"><span data-stu-id="c32a7-149">.DX\*</span></span>
- <span data-ttu-id="c32a7-150">.EDRW</span><span class="sxs-lookup"><span data-stu-id="c32a7-150">.EDRW</span></span>
- <span data-ttu-id="c32a7-151">.IAM</span><span class="sxs-lookup"><span data-stu-id="c32a7-151">.IAM</span></span>
- <span data-ttu-id="c32a7-152">.IGES</span><span class="sxs-lookup"><span data-stu-id="c32a7-152">.IGES</span></span>
- <span data-ttu-id="c32a7-153">.IGS</span><span class="sxs-lookup"><span data-stu-id="c32a7-153">.IGS</span></span>
- <span data-ttu-id="c32a7-154">.IPT</span><span class="sxs-lookup"><span data-stu-id="c32a7-154">.IPT</span></span>
- <span data-ttu-id="c32a7-155">.JT</span><span class="sxs-lookup"><span data-stu-id="c32a7-155">.JT</span></span>
- <span data-ttu-id="c32a7-156">.MF1</span><span class="sxs-lookup"><span data-stu-id="c32a7-156">.MF1</span></span>
- <span data-ttu-id="c32a7-157">.NEU</span><span class="sxs-lookup"><span data-stu-id="c32a7-157">.NEU</span></span>
- <span data-ttu-id="c32a7-158">.PAR</span><span class="sxs-lookup"><span data-stu-id="c32a7-158">.PAR</span></span>
- <span data-ttu-id="c32a7-159">.PKG</span><span class="sxs-lookup"><span data-stu-id="c32a7-159">.PKG</span></span>
- <span data-ttu-id="c32a7-160">.PRC</span><span class="sxs-lookup"><span data-stu-id="c32a7-160">.PRC</span></span>
- <span data-ttu-id="c32a7-161">.PRT</span><span class="sxs-lookup"><span data-stu-id="c32a7-161">.PRT</span></span>
- <span data-ttu-id="c32a7-162">.PSM</span><span class="sxs-lookup"><span data-stu-id="c32a7-162">.PSM</span></span>
- <span data-ttu-id="c32a7-163">.PWD</span><span class="sxs-lookup"><span data-stu-id="c32a7-163">.PWD</span></span>
- <span data-ttu-id="c32a7-164">.SLD\*</span><span class="sxs-lookup"><span data-stu-id="c32a7-164">.SLD\*</span></span>
- <span data-ttu-id="c32a7-165">.STEP</span><span class="sxs-lookup"><span data-stu-id="c32a7-165">.STEP</span></span>
- <span data-ttu-id="c32a7-166">.STL</span><span class="sxs-lookup"><span data-stu-id="c32a7-166">.STL</span></span>
- <span data-ttu-id="c32a7-167">.STP</span><span class="sxs-lookup"><span data-stu-id="c32a7-167">.STP</span></span>
- <span data-ttu-id="c32a7-168">.U3D</span><span class="sxs-lookup"><span data-stu-id="c32a7-168">.U3D</span></span>
- <span data-ttu-id="c32a7-169">.UNV</span><span class="sxs-lookup"><span data-stu-id="c32a7-169">.UNV</span></span>
- <span data-ttu-id="c32a7-170">.VRML</span><span class="sxs-lookup"><span data-stu-id="c32a7-170">.VRML</span></span>
- <span data-ttu-id="c32a7-171">.WRL</span><span class="sxs-lookup"><span data-stu-id="c32a7-171">.WRL</span></span>
- <span data-ttu-id="c32a7-172">.X_\*</span><span class="sxs-lookup"><span data-stu-id="c32a7-172">.X_\*</span></span>
- <span data-ttu-id="c32a7-173">.XAS</span><span class="sxs-lookup"><span data-stu-id="c32a7-173">.XAS</span></span>
- <span data-ttu-id="c32a7-174">.XMT\*</span><span class="sxs-lookup"><span data-stu-id="c32a7-174">.XMT\*</span></span>
- <span data-ttu-id="c32a7-175">.XPR</span><span class="sxs-lookup"><span data-stu-id="c32a7-175">.XPR</span></span>

## <a name="retain-image-files"></a><span data-ttu-id="c32a7-176">이미지 파일 보존</span><span class="sxs-lookup"><span data-stu-id="c32a7-176">Retain image files</span></span>

<span data-ttu-id="c32a7-177">SharePoint 또는 OneDrive에서 다음 파일 형식이 검색되면 이 권장 사항이 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="c32a7-177">This recommendation appears when any of the following file types are detected in SharePoint or OneDrive.</span></span>

- <span data-ttu-id="c32a7-178">.JPEG</span><span class="sxs-lookup"><span data-stu-id="c32a7-178">.JPEG</span></span>
- <span data-ttu-id="c32a7-179">.GIF</span><span class="sxs-lookup"><span data-stu-id="c32a7-179">.GIF</span></span>
- <span data-ttu-id="c32a7-180">.TIF\*</span><span class="sxs-lookup"><span data-stu-id="c32a7-180">.TIF\*</span></span>
- <span data-ttu-id="c32a7-181">.BMP</span><span class="sxs-lookup"><span data-stu-id="c32a7-181">.BMP</span></span>
- <span data-ttu-id="c32a7-182">.PNG</span><span class="sxs-lookup"><span data-stu-id="c32a7-182">.PNG</span></span>
- <span data-ttu-id="c32a7-183">.RAW</span><span class="sxs-lookup"><span data-stu-id="c32a7-183">.RAW</span></span>
- <span data-ttu-id="c32a7-184">.PSD</span><span class="sxs-lookup"><span data-stu-id="c32a7-184">.PSD</span></span>
- <span data-ttu-id="c32a7-185">.PSP</span><span class="sxs-lookup"><span data-stu-id="c32a7-185">.PSP</span></span>
- <span data-ttu-id="c32a7-186">.JPG</span><span class="sxs-lookup"><span data-stu-id="c32a7-186">.JPG</span></span>
- <span data-ttu-id="c32a7-187">.EXIF</span><span class="sxs-lookup"><span data-stu-id="c32a7-187">.EXIF</span></span>
- <span data-ttu-id="c32a7-188">.PPM</span><span class="sxs-lookup"><span data-stu-id="c32a7-188">.PPM</span></span>
- <span data-ttu-id="c32a7-189">.PGM</span><span class="sxs-lookup"><span data-stu-id="c32a7-189">.PGM</span></span>
- <span data-ttu-id="c32a7-190">.PBM</span><span class="sxs-lookup"><span data-stu-id="c32a7-190">.PBM</span></span>
- <span data-ttu-id="c32a7-191">.PNM</span><span class="sxs-lookup"><span data-stu-id="c32a7-191">.PNM</span></span>
- <span data-ttu-id="c32a7-192">.WEBP</span><span class="sxs-lookup"><span data-stu-id="c32a7-192">.WEBP</span></span>

## <a name="retain-nda-content"></a><span data-ttu-id="c32a7-193">NDA 콘텐츠 보존</span><span class="sxs-lookup"><span data-stu-id="c32a7-193">Retain NDA content</span></span> 

<span data-ttu-id="c32a7-194">다음 중 한 가지 조건이 충족되면 이 권장 사항이 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="c32a7-194">This recommendation appears when either of the following criteria are met.</span></span>

- <span data-ttu-id="c32a7-195">전자 메일 메시지의 본문에서 다음 키워드 조합이 검색되는 경우:</span><span class="sxs-lookup"><span data-stu-id="c32a7-195">Any of combination of these keywords is detected in the body of an email message:</span></span>
    - <span data-ttu-id="c32a7-196">NDA</span><span class="sxs-lookup"><span data-stu-id="c32a7-196">NDA</span></span>
    - <span data-ttu-id="c32a7-197">“비밀 유지 계약”</span><span class="sxs-lookup"><span data-stu-id="c32a7-197">“Non-Disclosure Agreement”</span></span>
    - <span data-ttu-id="c32a7-198">“비밀 유지 계약”</span><span class="sxs-lookup"><span data-stu-id="c32a7-198">“Non Disclosure Agreement”</span></span>

- <span data-ttu-id="c32a7-199">SharePoint 또는 OneDrive의 .PDF 또는 .DOC 파일에서 다음 키워드 조합이 검색되는 경우:</span><span class="sxs-lookup"><span data-stu-id="c32a7-199">Any combination of these keywords are detected in .PDF or .DOC files in SharePoint or OneDrive:</span></span>
    - <span data-ttu-id="c32a7-200">NDA</span><span class="sxs-lookup"><span data-stu-id="c32a7-200">NDA</span></span>
    - <span data-ttu-id="c32a7-201">비밀 유지 계약</span><span class="sxs-lookup"><span data-stu-id="c32a7-201">Non Disclosure Agreement</span></span>

## <a name="retain-software-development-files"></a><span data-ttu-id="c32a7-202">소프트웨어 개발 파일 보존</span><span class="sxs-lookup"><span data-stu-id="c32a7-202">Retain software development files</span></span>

<span data-ttu-id="c32a7-203">SharePoint 또는 OneDrive에서 다음 파일 형식이 검색되면 이 권장 사항이 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="c32a7-203">This recommendation appears when any of the following file types are detected in SharePoint or OneDrive.</span></span>

- <span data-ttu-id="c32a7-204">.ASAX</span><span class="sxs-lookup"><span data-stu-id="c32a7-204">.ASAX</span></span>
- <span data-ttu-id="c32a7-205">.ASM</span><span class="sxs-lookup"><span data-stu-id="c32a7-205">.ASM</span></span>
- <span data-ttu-id="c32a7-206">.ASP\*</span><span class="sxs-lookup"><span data-stu-id="c32a7-206">.ASP\*</span></span>
- <span data-ttu-id="c32a7-207">.BAT</span><span class="sxs-lookup"><span data-stu-id="c32a7-207">.BAT</span></span>
- <span data-ttu-id="c32a7-208">.CONFIG</span><span class="sxs-lookup"><span data-stu-id="c32a7-208">.CONFIG</span></span>
- <span data-ttu-id="c32a7-209">.CS</span><span class="sxs-lookup"><span data-stu-id="c32a7-209">.CS</span></span>
- <span data-ttu-id="c32a7-210">.CSS</span><span class="sxs-lookup"><span data-stu-id="c32a7-210">.CSS</span></span>
- <span data-ttu-id="c32a7-211">.DISCO</span><span class="sxs-lookup"><span data-stu-id="c32a7-211">.DISCO</span></span>
- <span data-ttu-id="c32a7-212">.HTM\*</span><span class="sxs-lookup"><span data-stu-id="c32a7-212">.HTM\*</span></span>
- <span data-ttu-id="c32a7-213">.INC</span><span class="sxs-lookup"><span data-stu-id="c32a7-213">.INC</span></span>
- <span data-ttu-id="c32a7-214">.JAD</span><span class="sxs-lookup"><span data-stu-id="c32a7-214">.JAD</span></span>
- <span data-ttu-id="c32a7-215">.JAVA</span><span class="sxs-lookup"><span data-stu-id="c32a7-215">.JAVA</span></span>
- <span data-ttu-id="c32a7-216">.JS\*</span><span class="sxs-lookup"><span data-stu-id="c32a7-216">.JS\*</span></span>
- <span data-ttu-id="c32a7-217">.LIB</span><span class="sxs-lookup"><span data-stu-id="c32a7-217">.LIB</span></span>
- <span data-ttu-id="c32a7-218">.O</span><span class="sxs-lookup"><span data-stu-id="c32a7-218">.O</span></span>
- <span data-ttu-id="c32a7-219">.PHP</span><span class="sxs-lookup"><span data-stu-id="c32a7-219">.PHP</span></span>
- <span data-ttu-id="c32a7-220">.RC</span><span class="sxs-lookup"><span data-stu-id="c32a7-220">.RC</span></span>
- <span data-ttu-id="c32a7-221">.RESX</span><span class="sxs-lookup"><span data-stu-id="c32a7-221">.RESX</span></span>
- <span data-ttu-id="c32a7-222">.RPT</span><span class="sxs-lookup"><span data-stu-id="c32a7-222">.RPT</span></span>
- <span data-ttu-id="c32a7-223">.RSS</span><span class="sxs-lookup"><span data-stu-id="c32a7-223">.RSS</span></span>
- <span data-ttu-id="c32a7-224">.SCPT</span><span class="sxs-lookup"><span data-stu-id="c32a7-224">.SCPT</span></span>
- <span data-ttu-id="c32a7-225">.SRC</span><span class="sxs-lookup"><span data-stu-id="c32a7-225">.SRC</span></span>
- <span data-ttu-id="c32a7-226">.VB\*</span><span class="sxs-lookup"><span data-stu-id="c32a7-226">.VB\*</span></span>
- <span data-ttu-id="c32a7-227">.WSF</span><span class="sxs-lookup"><span data-stu-id="c32a7-227">.WSF</span></span>
- <span data-ttu-id="c32a7-228">.XCODEPROJ</span><span class="sxs-lookup"><span data-stu-id="c32a7-228">.XCODEPROJ</span></span>
- <span data-ttu-id="c32a7-229">.XML</span><span class="sxs-lookup"><span data-stu-id="c32a7-229">.XML</span></span>
- <span data-ttu-id="c32a7-230">.XSD</span><span class="sxs-lookup"><span data-stu-id="c32a7-230">.XSD</span></span>
- <span data-ttu-id="c32a7-231">.XSL\*</span><span class="sxs-lookup"><span data-stu-id="c32a7-231">.XSL\*</span></span>

## <a name="retain-video-files"></a><span data-ttu-id="c32a7-232">비디오 파일 보존</span><span class="sxs-lookup"><span data-stu-id="c32a7-232">Retain video files</span></span>

<span data-ttu-id="c32a7-233">SharePoint 또는 OneDrive에서 다음 파일 형식이 검색되면 이 권장 사항이 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="c32a7-233">This recommendation appears when any of the following file types are detected in SharePoint or OneDrive.</span></span>

- <span data-ttu-id="c32a7-234">.AVCHD</span><span class="sxs-lookup"><span data-stu-id="c32a7-234">.AVCHD</span></span>
- <span data-ttu-id="c32a7-235">.AVI</span><span class="sxs-lookup"><span data-stu-id="c32a7-235">.AVI</span></span>
- <span data-ttu-id="c32a7-236">.FLV</span><span class="sxs-lookup"><span data-stu-id="c32a7-236">.FLV</span></span>
- <span data-ttu-id="c32a7-237">.MOV</span><span class="sxs-lookup"><span data-stu-id="c32a7-237">.MOV</span></span>
- <span data-ttu-id="c32a7-238">.MP2V</span><span class="sxs-lookup"><span data-stu-id="c32a7-238">.MP2V</span></span>
- <span data-ttu-id="c32a7-239">.MP4</span><span class="sxs-lookup"><span data-stu-id="c32a7-239">.MP4</span></span>
- <span data-ttu-id="c32a7-240">.MP4V</span><span class="sxs-lookup"><span data-stu-id="c32a7-240">.MP4V</span></span>
- <span data-ttu-id="c32a7-241">.MPE</span><span class="sxs-lookup"><span data-stu-id="c32a7-241">.MPE</span></span>
- <span data-ttu-id="c32a7-242">.MPEG</span><span class="sxs-lookup"><span data-stu-id="c32a7-242">.MPEG</span></span>
- <span data-ttu-id="c32a7-243">.MPEG1</span><span class="sxs-lookup"><span data-stu-id="c32a7-243">.MPEG1</span></span>
- <span data-ttu-id="c32a7-244">.MPEG2</span><span class="sxs-lookup"><span data-stu-id="c32a7-244">.MPEG2</span></span>
- <span data-ttu-id="c32a7-245">.MPEG4</span><span class="sxs-lookup"><span data-stu-id="c32a7-245">.MPEG4</span></span>
- <span data-ttu-id="c32a7-246">.MPG</span><span class="sxs-lookup"><span data-stu-id="c32a7-246">.MPG</span></span>
- <span data-ttu-id="c32a7-247">.MPG2</span><span class="sxs-lookup"><span data-stu-id="c32a7-247">.MPG2</span></span>
- <span data-ttu-id="c32a7-248">.MPG4</span><span class="sxs-lookup"><span data-stu-id="c32a7-248">.MPG4</span></span>
- <span data-ttu-id="c32a7-249">.WMV</span><span class="sxs-lookup"><span data-stu-id="c32a7-249">.WMV</span></span>
- <span data-ttu-id="c32a7-250">.XMV</span><span class="sxs-lookup"><span data-stu-id="c32a7-250">.XMV</span></span>
