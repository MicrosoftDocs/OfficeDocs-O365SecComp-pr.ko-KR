---
title: 데이터 조사에서 지원 되는 파일 형식
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: ''
ms.openlocfilehash: bec8c01b75d68249a335c4de48909ce50ab3bf97
ms.sourcegitcommit: 2c5834235c32b2616e1813ce24eeb3419a09629f
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/02/2019
ms.locfileid: "31030357"
---
# <a name="supported-file-types-in-data-investigations"></a>데이터 조사에서 지원 되는 파일 형식


| Mime 형식 | File 클래스 (예: Image, Archive, Email, Office Doc 등) | 네이티브 뷰어 | 텍스트 | 주석 달기 보기 | 컨테이너 추출 | 가능한 내선 번호 |
| :- | :- | :- | :- | :- | :- | :- |
| application/msword | 오피스 | 예 | 예 | 예 | 아니요 | .doc; .dat |
| application/pdf | 오피스 | 예 | 예 | 예 | 아니요 | .pdf |
| application/rtf | 오피스 | 예 | 예 | 예 | 아니요 | .rtf;. .doc |
| application/vnd | 오피스 | 예 | 예 | 예 | 아니요 | .xls; .dat |
| application/vnd macroenabled. 12 | 생산성/열린 문서 형식 | 예 | 예 | 아니요 | 아니요 | .xlsb |
| application/vnd macroenabled. 12 | 오피스 | 예 | 예 | 예 | 아니요 | .xlsm |
| application/vnd macroenabled. 12 | 생산성/열린 문서 형식 | 아니요 | 예 | 아니요 | 아니요 | . .xltm |
| application/vnd | 생산성 | 아니요 | 아니요 | 아니요 | 아니요 | .msg |
| application/vnd | 생산성/공동 작업 | 아니요 | 아니요 | 아니요 | 예 | .pst |
| application/vnd | 오피스 | 예 | 예 | 예 | 아니요 | .ppt; .pps;. p |
| application/vnd macroenabled. 12 | 오피스 | 예 | 예 | 예 | 아니요 | .docm |
| application/vnd macroenabled. 12 | 오피스 | 예 | 예 | 예 | 아니요 | normal.dotm |
| 응용 프로그램/vnd. 텍스트 | 오피스 | 예 | 예 | 예 | 아니요 | odt  |
| 응용 프로그램/vnd presentationml presentation | 오피스 | 예 | 예 | 예 | 아니요 | .pptx |
| 응용 프로그램/vnd. presentationml | 생산성/열린 문서 형식 | 예 | 예 | 예 | 아니요 | . ppsx |
| application/vnd. presentationml | 오피스 | 예 | 예 | 예 | 아니요 | . potx |
| 응용 프로그램/vnd. spreadsheetml | 오피스 | 예 | 예 | 예 | 아니요 | .xlsx |
| application/vnd. spreadsheetml | 오피스 | 예 | 예 | 예 | 아니요 | . .xltx |
| 응용 프로그램/vnd. wordprocessingml 문서 | 오피스 | 예 | 예 | 예 | 아니요 | .docx |
| application/vnd. wordprocessingml | 오피스 | 예 | 예 | 예 | 아니요 | . dotx |
| 응용 프로그램/vnd. visio | 오피스 | 예 | 예 | 예 | 아니요 | .vsd |
| application/x-y-7z-압축 | 보관/컨테이너 | 아니요 | 아니요 | 아니요 | 예 | .7z |
| 응용 프로그램/xhtml + xml | 오피스 | 예 | 예 | 예 | 아니요 | . xhtml |
| application/xml | 오피스 | 예 | 예 | 예 | 아니요 | .xml |
| 응용 프로그램/x-msaccess.exe | 오피스 | 예 | 예 | 예 | 아니요 | .mdb |
| 응용 프로그램/x-mspublisher | 오피스 | 예 | 예 | 예 | 아니요 | .pub |
| 응용 프로그램/x-rar-압축 | 보관/컨테이너 | 아니요 | 아니요 | 아니요 | 예 | rar |
| 응용 프로그램/우편 번호 | 보관/컨테이너 | 아니요 | 아니요 | 아니요 | 예 | .zip |
| image/bmp | 이미지나 | 예 | 예 | 예 | 아니요 | .bmp |
| image/emf | 이미지나 | 예 | 예 | 예 | 아니요 | .emf |
| 이미지/gif | 오피스 | 예 | 예 | 예 | 아니요 | .gif |
| image/jpeg | 이미지나 | 예 | 예 | 예 | 아니요 | .jpg; .jpeg; .dat;. jpgt |
| 이미지/png | 이미지나 | 예 | 예 | 예 | 아니요 | .png |
| 이미지/tiff | 이미지나 | 예 | 예 | 예 | 아니요 | .tif |
| image/vnd | 오피스 | 예 | 예 | 예 | 아니요 | dwg; .dxf |
| image/wmf | 오피스 | 예 | 예 | 예 | 아니요 | .wmf |
| message/rfc822-headers | 생산성/공동 작업 | 아니요 | 아니요 | 아니요 | 아니요 | .eml |
| text/csv | 오피스 | 예 | 예 | 예 | 아니요 | .csv |
| 텍스트/html | 오피스 | 예 | 예 | 예 | 아니요 | .html; shtml.dll; .htm |
| 텍스트/일반 | 오피스 | 예 | 예 | 예 | 아니요 | .txt; .css; con, pl; .csv; .dat |
| 텍스트/vcard-연락처 | 오피스 | 예 | 예 | 예 | 아니요 | .vcf |