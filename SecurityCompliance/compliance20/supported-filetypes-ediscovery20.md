---
title: 고급 eDiscovery에서 지원 되는 파일 형식
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
ms.openlocfilehash: 378bd9ae88269d6a6d15a672473550e50179f772
ms.sourcegitcommit: 865b3dc071150b20bf3967e1263fc54e75898284
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/09/2019
ms.locfileid: "33834937"
---
# <a name="supported-file-types-in-advanced-ediscovery"></a>고급 eDiscovery에서 지원 되는 파일 형식

고급 eDiscovery는 다양 한 파일 형식을 지원 하며, 각 수준에서 지원 되며, 다음 표에 설명 되어 있습니다. 이 목록은 아직 마무리 되지 않으며 유효성 검사 테스트를 계속할 때 새 파일 형식을 추가 합니다. 이 표에서는 고급 eDiscovery의 사용 가능한 뷰어에서 파일 형식을 볼 수 있는지 여부도 나타냅니다.

| Mime 형식 | 설명 | 네이티브 뷰어 | 텍스트 뷰어 | 주석 달기 보기 | 컨테이너 추출 | 간격 |
| :- | :- | :- | :- | :- | :- | :- |
| application/mbox | 보관/컨테이너 |  |  |  | 예 | mbox |
| application/msword | 생산성 | 예 | 예 | 예 |  | .doc; .dat |
| application/pdf | 생산성 | 예 | 예 | 예 |  | .pdf |
| application/rtf | 오피스 | 예 | 예 | 예 |  | .rtf;. .doc |
| application/vnd | 생산성 | 예 | 예 | 예 |  | .xls; .dat |
| application/vnd macroenabled. 12 | 생산성 | 예 | 예 | 아니요 |  | .xlsb |
| application/vnd macroenabled. 12 | 생산성 | 예 | 예 | 예 |  | .xlsm |
| application/vnd macroenabled. 12 | 생산성 | 아니요 | 예 | 아니요 |  | . .xltm |
| application/vnd | 공동 작업 | 예 | 예 | 예 |  | .msg |
| application/vnd | 보관/컨테이너 |  |  |  | 예 | .pst |
| application/vnd | 생산성 | 예 | 예 | 예 |  | .ppt; .pps;. p |
| application/vnd macroenabled. 12 | 생산성 | 예 | 예 | 예 |  | .docm |
| application/vnd macroenabled. 12 | 생산성 | 예 | 예 | 예 |  | normal.dotm |
| 응용 프로그램/vnd. 텍스트 | 생산성 | 예 | 예 | 예 |  | odt  |
| 응용 프로그램/vnd presentationml presentation | 생산성 | 예 | 예 | 예 |  | .pptx |
| 응용 프로그램/vnd. presentationml | 생산성 | 예 | 예 | 예 |  | . ppsx |
| application/vnd. presentationml | 생산성 | 예 | 예 | 예 |  | . potx |
| 응용 프로그램/vnd. spreadsheetml | 생산성 | 예 | 예 | 예 |  | .xlsx |
| application/vnd. spreadsheetml | 생산성 | 예 | 예 | 예 |  | . .xltx |
| 응용 프로그램/vnd. wordprocessingml 문서 | 생산성 | 예 | 예 | 예 |  | .docx |
| application/vnd. wordprocessingml | 생산성 | 예 | 예 | 예 |  | . dotx |
| 응용 프로그램/vnd. visio | 생산성 | 예 | 예 | 예 |  | .vsd |
| application/x-y-7z-압축 | 보관/컨테이너 |  |  |  | 예 | .7z |
| 응용 프로그램/xhtml + xml | 오피스 | 예 | 예 | 예 |  | . xhtml |
| application/xml | 오피스 | 예 | 예 | 예 |  | .xml |
| 응용 프로그램/x-msaccess.exe | 생산성 | 예 | 예 | 예 |  | .mdb |
| 응용 프로그램/x-mspublisher | 생산성 | 예 | 예 | 예 |  | .pub |
| 응용 프로그램/x-rar-압축 | 보관/컨테이너 |  |  |  | 예 | rar |
| application/x.x-tar | 보관/컨테이너 |  |  |  | 예 | tar |
| 응용 프로그램/우편 번호 | 보관/컨테이너 |  |  |  | 예 | .zip |
| image/bmp | 이미지나 | 예 | 예 | 예 |  | .bmp |
| image/emf | 이미지나 | 예 | 예 | 예 |  | .emf |
| 이미지/gif | 이미지나 | 예 | 예 | 예 |  | .gif |
| image/jpeg | 이미지나 | 예 | 예 | 예 |  | .jpg; .jpeg; .dat;. jpgt |
| 이미지/png | 이미지나 | 예 | 예 | 예 |  | .png |
| 이미지/tiff | 이미지나 | 예 | 예 | 예 |  | .tif |
| image/vnd | 그림 | 예 | 예 | 예 |  | dwg; .dxf |
| image/wmf | 오피스 | 예 | 예 | 예 |  | .wmf |
| message/rfc822-headers | 공동 작업 | 예 | 예 | 예 |  | .eml |
| text/csv | 오피스 | 예 | 예 | 예 |  | .csv |
| 텍스트/html | 오피스 | 예 | 예 | 예 |  | .html; shtml.dll; .htm |
| 텍스트/일반 | 오피스 | 예 | 예 | 예 |  | .txt; .css; con, pl; .csv; .dat |
| 텍스트/vcard-연락처 | 공동 작업 | 예 | 예 | 예 |  | .vcf |
||||||||
