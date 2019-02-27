---
title: Advanced eDiscovery (미리 보기)에서 지원 되는 파일 형식
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
ms.openlocfilehash: 8b5651e7e1f1e15aae34a3100b25564f0b84abb7
ms.sourcegitcommit: baf23be44f1ed5abbf84f140b5ffa64fce605478
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/26/2019
ms.locfileid: "30296161"
---
# <a name="supported-file-types-in-advanced-ediscovery-preview"></a>Advanced eDiscovery (미리 보기)에서 지원 되는 파일 형식


| Mime 형식 | File 클래스 (예: Image, Archive, Email, Office Doc 등) | 네이티브 뷰어 | 텍스트 | 주석 달기 보기 | 컨테이너 추출 | 가능한 내선 번호 |
| :- | :- | :- | :- | :- | :- | :- |
| application/msword | 문서 | 예 | 예  | O | 아니요 | .doc; .dat |
| application/pdf | 문서 | 예 | 예  | O | 아니요 | .pdf |
| application/rtf | 문서 | 예 | 예  | O | 아니요 | .rtf;. .doc |
| application/vnd | 문서 | 예 | 예  | O | 아니요 | .xls; .dat |
| application/vnd macroenabled. 12 | 생산성/열린 문서 형식 | 예 | O | 아니요 | 아니요 | .xlsb |
| application/vnd macroenabled. 12 | 문서 | 예 | 예  | O | 아니요 | .xlsm |
| application/vnd macroenabled. 12 | 생산성/열린 문서 형식 | 아니요 | 예 | 아니요 | 아니요 | .xltm |
| application/vnd | 생산성 | 아니요 | 아니요 | 아니요 | 아니요 | .msg |
| application/vnd | 생산성/공동 작업 | 아니요 | 아니요 | 아니요 | 예 | .pst |
| application/vnd | 문서 | 예 | 예  | O | 아니요 | .ppt; .pps;. p |
| application/vnd macroenabled. 12 | 문서 | 예 | 예  | O | 아니요 | .docm |
| application/vnd macroenabled. 12 | 문서 | 예 | 예  | O | 아니요 | .dotm |
| 응용 프로그램/vnd. 텍스트 | 문서 | 예 | 예  | O | 아니요 | odt  |
| 응용 프로그램/vnd presentationml presentation | 문서 | 예 | 예  | O | 아니요 | .pptx |
| 응용 프로그램/vnd. presentationml | 생산성/열린 문서 형식 | 예 | 예  | O | 아니요 | . ppsx |
| application/vnd. presentationml | 문서 | 예 | 예  | O | 아니요 | .potx |
| 응용 프로그램/vnd. spreadsheetml | 문서 | 예 | 예  | O | 아니요 | .xlsx |
| application/vnd. spreadsheetml | 문서 | 예 | 예  | O | 아니요 | .xltx |
| 응용 프로그램/vnd. wordprocessingml 문서 | 문서 | 예 | 예  | O | 아니요 | .docx |
| application/vnd. wordprocessingml | 문서 | 예 | 예  | O | 아니요 | .dotx |
| 응용 프로그램/vnd. visio | 문서 | 예 | 예  | O | 아니요 | .vsd |
| application/x-y-7z-압축 | 보관/컨테이너 | 아니요 | 아니요 | 아니요 | 예 | .7z |
| 응용 프로그램/xhtml + xml | 문서 | 예 | 예  | O | 아니요 | . xhtml |
| application/xml | 문서 | 예 | 예  | O | 아니요 | .xml |
| 응용 프로그램/x-msaccess.exe | 문서 | 예 | 예  | O | 아니요 | .mdb |
| 응용 프로그램/x-mspublisher | 문서 | 예 | 예  | O | 아니요 | .pub |
| 응용 프로그램/x-rar-압축 | 보관/컨테이너 | 아니요 | 아니요 | 아니요 | 예 | rar |
| 응용 프로그램/우편 번호 | 보관/컨테이너 | 아니요 | 아니요 | 아니요 | 예 | .zip |
| image/bmp | 이미지 | 예 | 예  | O | 아니요 | .bmp |
| image/emf | 이미지 | 예 | 예  | O | 아니요 | .emf |
| 이미지/gif | 문서 | 예 | 예  | O | 아니요 | .gif |
| image/jpeg | 이미지 | 예 | 예  | O | 아니요 | .jpg; .jpeg; .dat;. jpgt |
| 이미지/png | 이미지 | 예 | 예  | O | 아니요 | .png |
| 이미지/tiff | 이미지 | 예 | 예  | O | 아니요 | .tif |
| image/vnd | 문서 | 예 | 예  | O | 아니요 | dwg; .dxf |
| image/wmf | 문서 | 예 | 예  | O | 아니요 | .wmf |
| message/rfc822-headers | 생산성/공동 작업 | 아니요 | 아니요 | 아니요 | 아니요 | .eml |
| text/csv | 문서 | 예 | 예  | O | 아니요 | .csv |
| 텍스트/html | 문서 | 예 | 예  | O | 아니요 | .html; shtml.dll; .htm |
| text/plain | 문서 | 예 | 예  | O | 아니요 | .txt; .css; con, pl; .csv; .dat |
| 텍스트/vcard-연락처 | 문서 | 예 | 예  | O | 아니요 | .vcf |