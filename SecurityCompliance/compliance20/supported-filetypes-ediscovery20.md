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
ms.openlocfilehash: d8e9689cb04929137787225579dcda17005c8bfe
ms.sourcegitcommit: 7be8617ce75909f0fa1a2f6e72749e2ef4bb2d3e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/16/2019
ms.locfileid: "34088811"
---
# <a name="supported-file-types-in-advanced-ediscovery"></a>고급 eDiscovery에서 지원 되는 파일 형식

고급 eDiscovery에서는 다음 표에 설명 된 여러 다른 수준의 다양 한 파일 형식을 지원 합니다. 이 목록은 마무리 되지 않으며 유효성 검사 테스트를 계속할 때 새 파일 형식을 추가 합니다. 이 표에서는 파일 형식이 텍스트 추출 (이미지의 경우 OCR)에서 지원 되며, 기본 뷰어에 표시 되며, 고급 eDiscovery의 주석 달기 뷰어에도 지원 되는지 여부를 나타냅니다.

## <a name="archive--container"></a>보관/컨테이너

| Mime 형식 | 파일 id | 메타 데이터 추출 | 컨테이너 추출 | 가능한 내선 번호 |
| :- |  :- |  :- |  :- |  :- |
| application/x-y-7z-압축 | 예 | 예 | 예 | .7z |
| 응용 프로그램/x-rar-압축 | 예 | 예 | 예 | rar |
| application/x.x-tar | 예 | 예 | 예 | tar |
| 응용 프로그램/우편 번호 | 예 | 예 | 예 | .zip |
||||||||

## <a name="database"></a>데이터베이스

| Mime 형식 | 파일 id | 메타 데이터 추출 | 텍스트 추출 | 네이티브 뷰어 | 주석 달기 보기 | 가능한 내선 번호 |
| :- |  :- |  :- |  :- |  :- |  :- |  :- |
| 응용 프로그램/x-msaccess.exe | 예 | 예 | 예 | 아니요 | 아니요 | .mdb |
||||||||

## <a name="email"></a>메일

| Mime 형식 | 파일 id | 메타 데이터 추출 | 텍스트 추출 | 네이티브 뷰어 | 주석 달기 보기 | 가능한 내선 번호 |
| :- |  :- |  :- |  :- |  :- |  :- |  :- |
| application/vnd | 예 | 예 | 예 | 예 | 예 | .msg |
| message/rfc822-headers | 예 | 예 | 예 | 예 | 예 | .eml |
| 텍스트/vcard-연락처 | 예 | 예 | 예 | 예 | 예 | .vcf |
||||||||

## <a name="email-container"></a>전자 메일 컨테이너

| Mime 형식 | 파일 id | 메타 데이터 추출 | 컨테이너 추출 | 가능한 내선 번호 |
| :- |  :- |  :- |  :- |  :- |
| application/mbox | 예 | 예 | 예 | mbox |
| application/vnd | 예 | 예 | 예 | .pst |
||||||||

## <a name="html"></a>HTML

| Mime 형식 | 파일 id | 메타 데이터 추출 | 텍스트 추출 | 네이티브 뷰어 | 주석 달기 보기 | 가능한 내선 번호 |
| :- |  :- |  :- |  :- |  :- |  :- |  :- |
| 응용 프로그램/xhtml + xml | 예 | 예 | 예 | 예 | 예 | . xhtml |
| application/xml | 예 | 예 | 예 | 예 | 예 | .xml |
| 텍스트/html | 예 | 예 | 예 | 예 | 예 | .htm, .html, shtml.dll |
||||||||

## <a name="image"></a>이미지나

| Mime 형식 | 파일 id | 메타 데이터 추출 | OCR 텍스트 추출 | 네이티브 뷰어 | 주석 달기 보기 | 가능한 내선 번호 |
| :- |  :- |  :- |  :- |  :- |  :- |  :- |
| image/bmp | 예 | 예 | 예 | 예 | 예 | .bmp |
| image/emf | 예 | 예 | 예 | 예 | 예 | .emf |
| 이미지/gif | 예 | 예 | 예 | 예 | 예 | .gif |
| image/jpeg | 예 | 예 | 예 | 예 | 예 | .jpeg; .jpg |
| 이미지/png | 예 | 예 | 예 | 예 | 예 | .png |
| image/svg + xml | 예 | 예 | 예 | 예 | 아니요 | . svg |
| 이미지/tiff | 예 | 예 | 예 | 예 | 예 | .tif |
| image/vnd | 예 | 예 | 예 | 예 | 예 | dwg; dxf |
| image/wmf | 예 | 예 | 예 | 예 | 예 | .wmf |
||||||||

## <a name="microsoft-excel"></a>Microsoft Excel

| Mime 형식 | 파일 id | 메타 데이터 추출 | 텍스트 추출 | 네이티브 뷰어 | 주석 달기 보기 | 가능한 내선 번호 |
| :- |  :- |  :- |  :- |  :- |  :- |  :- |
| application/vnd | 예 | 예 | 예 | 예 | 예 | .dat; .xls |
| application/vnd macroenabled. 12 | 예 | 예 | 예 | 예 | 아니요 | .xlsb |
| application/vnd macroenabled. 12 | 예 | 예 | 예 | 예 | 예 | .xlsm |
| application/vnd macroenabled. 12 | 예 | 예 | 예 | 아니요 | 아니요 | . .xltm |
| 응용 프로그램/vnd. spreadsheetml | 예 | 예 | 예 | 예 | 예 | .xlsx |
| application/vnd. spreadsheetml | 예 | 예 | 예 | 예 | 예 | . .xltx |
||||||||

## <a name="microsoft-powerpoint"></a>Microsoft PowerPoint

| Mime 형식 | 파일 id | 메타 데이터 추출 | 텍스트 추출 | 네이티브 뷰어 | 주석 달기 보기 | 가능한 내선 번호 |
| :- |  :- |  :- |  :- |  :- |  :- |  :- |
| application/vnd | 예 | 예 | 예 | 예 | 예 | .pot; .pps; .ppt |
| 응용 프로그램/vnd presentationml presentation | 예 | 예 | 예 | 예 | 예 | .pptx |
| 응용 프로그램/vnd. presentationml | 예 | 예 | 예 | 예 | 예 | . ppsx |
| application/vnd. presentationml | 예 | 예 | 예 | 예 | 예 | . potx |
||||||||

## <a name="microsoft-publisher"></a>Microsoft Publisher

| Mime 형식 | 파일 id | 메타 데이터 추출 | 텍스트 추출 | 네이티브 뷰어 | 주석 달기 보기 | 가능한 내선 번호 |
| :- |  :- |  :- |  :- |  :- |  :- |  :- |
| 응용 프로그램/x-mspublisher | 예 | 예 | 예 | 예 | 예 | .pub |
||||||||

## <a name="microsoft-visio"></a>Microsoft Visio

| Mime 형식 | 파일 id | 메타 데이터 추출 | 텍스트 추출 | 네이티브 뷰어 | 주석 달기 보기 | 가능한 내선 번호 |
| :- |  :- |  :- |  :- |  :- |  :- |  :- |
| 응용 프로그램/vnd. 드로잉 | 예 | 예 | 예 | 예 | 아니요 |  |
| 응용 프로그램/vnd. visio | 예 | 예 | 예 | 예 | 예 | .vsd |
||||||||

## <a name="microsoft-word"></a>Microsoft Word

| Mime 형식 | 파일 id | 메타 데이터 추출 | 텍스트 추출 | 네이티브 뷰어 | 주석 달기 보기 | 가능한 내선 번호 |
| :- |  :- |  :- |  :- |  :- |  :- |  :- |
| application/msword | 예 | 예 | 예 | 예 | 예 | .dat; .doc |
| application/rtf | 예 | 예 | 예 | 예 | 예 | .doc; .rtf |
| application/vnd macroenabled. 12 | 예 | 예 | 예 | 예 | 예 | .docm |
| application/vnd macroenabled. 12 | 예 | 예 | 예 | 예 | 예 | normal.dotm |
| 응용 프로그램/vnd. wordprocessingml 문서 | 예 | 예 | 예 | 예 | 예 | .docx |
| application/vnd. wordprocessingml | 예 | 예 | 예 | 예 | 예 | . dotx |
||||||||

## <a name="microsoft-works"></a>Microsoft Works

| Mime 형식 | 파일 id | 메타 데이터 추출 | 텍스트 추출 | 네이티브 뷰어 | 주석 달기 보기 | 가능한 내선 번호 |
| :- |  :- |  :- |  :- |  :- |  :- |  :- |
| application/vnd-ss | 예 | 예 | 아니요 | 아니요 | 아니요 | wps |
| application/vnd-wp | 예 | 예 | 아니요 | 아니요 | 아니요 | wps |
||||||||

## <a name="open-document-format"></a>열린 문서 형식

| Mime 형식 | 파일 id | 메타 데이터 추출 | 텍스트 추출 | 네이티브 뷰어 | 주석 달기 보기 | 가능한 내선 번호 |
| :- |  :- |  :- |  :- |  :- |  :- |  :- |
| 응용 프로그램/vnd. 텍스트 | 예 | 예 | 예 | 예 | 예 | odt |
||||||||

## <a name="other"></a>기타

| Mime 형식 | 파일 id | 메타 데이터 추출 | 텍스트 추출 | 네이티브 뷰어 | 주석 달기 보기 | 가능한 내선 번호 |
| :- |  :- |  :- |  :- |  :- |  :- |  :- |
| application/json | 예 | 예 | 예 | 예 | 예 | 해당 없음 |
| application/vnd | 예 | 예 | 아니요 | 아니요 | 아니요 |  |
| 응용 프로그램/winhlp | 예 | 예 | 아니요 | 아니요 | 아니요 | .hlp |
| application/x-tnef | 예 | 예 | 아니요 | 아니요 | 아니요 |  |
||||||||

## <a name="plain-text"></a>일반 텍스트

| Mime 형식 | 파일 id | 메타 데이터 추출 | 텍스트 추출 | 네이티브 뷰어 | 주석 달기 보기 | 가능한 내선 번호 |
| :- |  :- |  :- |  :- |  :- |  :- |  :- |
| text/csv | 예 | 예 | 예 | 예 | 예 | .csv |
| 텍스트/일반 | 예 | 예 | 예 | 예 | 예 | con; .css; .csv; .dat; .txt |
||||||||

## <a name="portable-document-format"></a>PDF(Portable Document Format)

| Mime 형식 | 파일 id | 메타 데이터 추출 | 텍스트 추출 | 네이티브 뷰어 | 주석 달기 보기 | 가능한 내선 번호 |
| :- |  :- |  :- |  :- |  :- |  :- |  :- |
| application/pdf | 예 | 예 | 예 | 예 | 예 | .pdf |
||||||||

## <a name="word-perfect"></a>Word 완벽

| Mime 형식 | 파일 id | 메타 데이터 추출 | 텍스트 추출 | 네이티브 뷰어 | 주석 달기 보기 | 가능한 내선 번호 |
| :- |  :- |  :- |  :- |  :- |  :- |  :- |
| application/vnd; 버전 = 5.0 | 예 | 예 | 예 | 아니요 | 아니요 | .wpd |
| application/vnd; 버전 = 5.1 | 예 | 예 | 예 | 아니요 | 아니요 | .wpd |
| application/vnd; 버전 = 6.x | 예 | 예 | 예 | 아니요 | 아니요 | .wpd |
||||||||

## <a name="word-pro"></a>Word Pro

| Mime 형식 | 파일 id | 메타 데이터 추출 | 텍스트 추출 | 네이티브 뷰어 | 주석 달기 보기 | 가능한 내선 번호 |
| :- |  :- |  :- |  :- |  :- |  :- |  :- |
| application/vnd | 예 | 예 | 아니요 | 아니요 | 아니요 | lwp |
||||||||
