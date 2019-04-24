---
title: 검색 및 분석 설정 구성
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
ms.openlocfilehash: b17492b11603ff27b91da8def4db6cba519801ee
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32258756"
---
# <a name="configure-search-and-analytics-settings"></a>검색 및 분석 설정 구성

## <a name="near-duplicates-and-email-threading"></a>유사 중복 및 전자 메일 스레딩

이 섹션에서는 중복 검색, 중복 검색 및 전자 메일 스레딩에 대 한 매개 변수를 설정할 수 있습니다.

- 사용/사용 안 함: 사용 하도록 설정 된 경우 중복 검색, 근접 중복 검색 및 전자 메일 스레딩을 분석 흐름의 일부로 포함 합니다. 두 사용자는 서로의 상위에 구축 되므로 모든 기능을 사용 하거나 사용 하지 않도록 설정 해야 합니다.

- 임계값: 두 문서의 유사성 수준이 임계값을 초과 하는 경우 동일한 비슷한 중복 집합에 배치 됩니다.

- 기본적으로 중복 항목 숨기기:이 설정이 설정 되어 있으면 중복 문서를 숨기는 필터가 기본적으로 작업 집합에 적용 됩니다. 필요한 경우 작업 집합에서 필터를 수동으로 제거할 수 있습니다.

- 최소/최대 단어 수: 중복 및 전자 메일 스레딩은 최소 단어 수와 최대 단어 수를 포함 하는 문서에 대해서만 실행 됩니다.
자세한 내용은 [Near 중복 검색](near-duplicates.md) 및 [전자 메일 스레딩](email-threading.md)를 참조 하세요.

## <a name="themes"></a>테마

이 섹션에서는 테마에 대 한 매개 변수를 설정할 수 있습니다.

- Enable/disable: 사용 하도록 설정 된 경우 분석 흐름의 일부로 테마 클러스터링을 포함 합니다.
- 동적으로 동적으로 테마 수 조정: 필요한 수의 테마를 만들 수 있는 문서가 충분 하지 않은 경우도 있습니다. 이 설정을 사용 하도록 설정 하는 경우 원하는 최대 테마 수를 강제 실행 하는 것이 아니라 시스템에서 최대 테마 수를 동적으로 조정 합니다.
- 최대 테마 수: 원하는 테마 수
- 테마에 번호 포함: 사용 하도록 설정 하는 경우 테마를 생성할 때 숫자가 포함 됩니다.  

## <a name="optical-character-recognition-ocr"></a>OCR (광학 문자 인식)

이 설정을 사용 하도록 설정 하면 작업 집합으로 ingested는 이미지에서 OCR이 실행 되어 검색이 가능 하 게 할 수 있습니다.

## <a name="ignore-text"></a>텍스트 무시

특정 텍스트에는 전자 메일 내용에 관계 없이 특정 전자 메일에 추가 되는 긴 고 지 사항 등의 분석 품질이 감소 하는 경우가 있습니다. 이러한 경우를 알고 있는 경우 텍스트 (RegEx가 지원 됨)와 텍스트를 제외 해야 하는 모듈을 지정 하 여 분석에서이 텍스트를 제외할 수 있습니다.