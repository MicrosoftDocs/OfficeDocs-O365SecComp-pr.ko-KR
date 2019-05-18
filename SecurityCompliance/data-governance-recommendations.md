---
title: 데이터 거버넌스 권장 사항을 표시하기 위해 콘텐츠가 식별되는 방법
ms.author: brendonb
author: stephow-MSFT
manager: laurawi
ms.date: 1/15/2019
audience: Admin
ms.topic: overview
ms.service: O365-seccomp
localization_priority: Priority
search.appverid:
- MOE150
- MET150
ROBOTS: NOINDEX, NOFOLLOW
description: 'Office 365 보안 및 준수 센터는 조직의 현재 설정을 기반으로 데이터 거버넌스 권장 사항을 제공하며 몇 번의 클릭만으로 설정을 완료할 수 있는 기능을 서비스합니다. 이 권장 사항의 일부는 조직 내의 특정 콘텐츠를 검색한 후 해당 콘텐츠를 관리하는 단계별 방법을 권장합니다. 예를 들어, 권장 사항이 비즈니스 측면에서 중요한 콘텐츠(예: 비공개 유지 권한 또는 NDA 정보)가 포함된 항목을 검색할 수 있으며, 사용자는 해당 항목에 보존 레이블을 자동으로 적용하여 필요에 따라 해당 항목을 분류하고 보존할 수 있습니다. 이 항목에는 사용자가 확인할 수 있는 데이터 거버넌스 권장 사항이 나열되어 있으며 각 권장 사항을 표시하기 위해 어떤 콘텐츠가 검색되는지 설명합니다.'
ms.openlocfilehash: 3d96b7c15d5b6a0f6ec3bbf467bd8a1099af559a
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/17/2019
ms.locfileid: "34153710"
---
# <a name="how-content-is-identified-for-data-governance-recommendations"></a>데이터 거버넌스 권장 사항을 표시하기 위해 콘텐츠가 식별되는 방법

Office 365 보안 및 준수 센터는 조직의 현재 설정을 기반으로 데이터 거버넌스 권장 사항을 제공하며 몇 번의 클릭만으로 설정을 완료할 수 있는 기능을 서비스합니다. 이 권장 사항의 일부는 조직 내의 특정 콘텐츠를 검색한 후 해당 콘텐츠를 관리하는 단계별 방법을 권장합니다. 예를 들어, 권장 사항이 비즈니스 측면에서 중요한 콘텐츠(예: 비공개 유지 권한 또는 NDA 정보)가 포함된 항목을 검색할 수 있으며, 사용자는 해당 항목에 보존 레이블을 자동으로 적용하여 필요에 따라 해당 항목을 분류하고 보존할 수 있습니다.

이 항목에는 사용자가 확인할 수 있는 데이터 거버넌스 권장 사항이 나열되어 있으며 각 권장 사항을 표시하기 위해 어떤 콘텐츠가 검색되는지 설명합니다.

## <a name="clean-up-voicemail"></a>음성 사서함 정리

‘음성 메일’ 메시지 유형으로 식별된 전자 메일 메시지가 사용자의 사서함에서 감지되었을 때 이 권장 사항이 표시됩니다. [Exchange에서의 메시지 속성](https://docs.microsoft.com/ko-KR/exchange/policy-and-compliance/ediscovery/message-properties-and-search-operators?view=exchserver-2019#searchable-properties-in-exchange)에 대해 자세히 알아보세요.

## <a name="label-attorney-client-privilege-content"></a>비공개 유지 권한 콘텐츠 레이블 지정 

다음 중 한 가지 조건이 충족되면 이 권장 사항이 표시됩니다.

- 전자 메일 메시지의 본문에서 다음 키워드 조합이 검색되는 경우:
    - ACP
    - 비공개 유지 권한
    - 비공개 유지 권한
    - 비공개 유지 권한

- SharePoint 또는 OneDrive 파일에서 다음 키워드 조합이 검색되는 경우:
    - ACP
    - 비공개 유지 권한*
    - AC 권한

## <a name="retain-audio-files"></a>오디오 파일 보존

SharePoint 또는 OneDrive에서 다음 파일 형식이 검색되면 이 권장 사항이 표시됩니다.

- .MP3
- .WMA
- .WAV
- .RA
- .RAM
- .RM
- .MID
- .OGG
- .AIFF
- .PCM
- .AAC
- .FLAC
- .ALAC

## <a name="retain-cad-files"></a>CAD 파일 보존

SharePoint 또는 OneDrive에서 다음 파일 형식이 검색되면 이 권장 사항이 표시됩니다.

- .3DXML
- .ACIS
- .ARC
- .ASM
- .CAT*
- .CGR
- .DW*
- .DX*
- .EDRW
- .IAM
- .IGES
- .IGS
- .IPT
- .JT
- .MF1
- .NEU
- .PAR
- .PKG
- .PRC
- .PRT
- .PSM
- .PWD
- .SLD*
- .STEP
- .STL
- .STP
- .U3D
- .UNV
- .VRML
- .WRL
- .X_*
- .XAS
- .XMT*
- .XPR

## <a name="retain-image-files"></a>이미지 파일 보존

SharePoint 또는 OneDrive에서 다음 파일 형식이 검색되면 이 권장 사항이 표시됩니다.

- .JPEG
- .GIF
- .TIF*
- .BMP
- .PNG
- .RAW
- .PSD
- .PSP
- .JPG
- .EXIF
- .PPM
- .PGM
- .PBM
- .PNM
- .WEBP

## <a name="retain-nda-content"></a>NDA 콘텐츠 보존 

다음 중 한 가지 조건이 충족되면 이 권장 사항이 표시됩니다.

- 전자 메일 메시지의 본문에서 다음 키워드 조합이 검색되는 경우:
    - NDA
    - “비밀 유지 계약”
    - “비밀 유지 계약”

- SharePoint 또는 OneDrive의 .PDF 또는 .DOC 파일에서 다음 키워드 조합이 검색되는 경우:
    - NDA
    - 비밀 유지 계약

## <a name="retain-software-development-files"></a>소프트웨어 개발 파일 보존

SharePoint 또는 OneDrive에서 다음 파일 형식이 검색되면 이 권장 사항이 표시됩니다.

- .ASAX
- .ASM
- .ASP*
- .BAT
- .CONFIG
- .CS
- .CSS
- .DISCO
- .HTM*
- .INC
- .JAD
- .JAVA
- .JS*
- .LIB
- .O
- .PHP
- .RC
- .RESX
- .RPT
- .RSS
- .SCPT
- .SRC
- .VB*
- .WSF
- .XCODEPROJ
- .XML
- .XSD
- .XSL*

## <a name="retain-video-files"></a>비디오 파일 보존

SharePoint 또는 OneDrive에서 다음 파일 형식이 검색되면 이 권장 사항이 표시됩니다.

- .AVCHD
- .AVI
- .FLV
- .MOV
- .MP2V
- .MP4
- .MP4V
- .MPE
- .MPEG
- .MPEG1
- .MPEG2
- .MPEG4
- .MPG
- .MPG2
- .MPG4
- .WMV
- .XMV
