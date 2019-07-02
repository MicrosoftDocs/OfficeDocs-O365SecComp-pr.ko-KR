---
title: 검토 집합에서 문서 내보내기
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: ''
ms.openlocfilehash: 7c1daccab799b3967c6b8c1d577060d062c05a70
ms.sourcegitcommit: e323610df2df71c84f536e8a38650d33d8069e41
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/04/2019
ms.locfileid: "34703791"
---
# <a name="export-documents-from-a-review-set"></a>검토 집합에서 문서 내보내기

다음 방법 중 하나를 통해 검토 집합에서 프레젠테이션이나 외부 리뷰에 대 한 콘텐츠를 내보낼 수 있습니다.

- [문서 다운로드](#download-documents-from-a-review-set)
 
- [문서 내보내기](#export-documents-from-a-review-set)

## <a name="download-documents-from-a-review-set"></a>검토 집합에서 문서 다운로드

다운로드에서는 기본 형식의 검토 집합에서 콘텐츠를 간단 하 게 다운로드 하는 간단한 방법을 제공 합니다. 다운로드 준비가 완료 되 면 브라우저 음성 안내가 표시 되도록 브라우저의 데이터 전송 기능을 활용 합니다. 이 방법을 사용 하 여 다운로드 한 파일은 컨테이너 파일로 압축 되 고 항목 수준 파일이 됩니다. 즉, 첨부 파일을 선택 하면 첨부 파일이 포함 된 전자 메일이 자동으로 수신 됩니다. 마찬가지로 word 문서에 포함 된 excel 스프레드시트를 선택 하면 excel 스프레드시트가 포함 된 word 문서를 받게 됩니다. 다운로드 한 항목은 파일 속성으로 표시 될 수 있는 마지막으로 수정한 날짜를 보존 합니다.

검토 집합에서 콘텐츠를 다운로드 하려면 먼저 다운로드 하려는 파일을 선택 하 고 작업 메뉴에서 "다운로드"를 선택 합니다.

![자동으로 생성 되는 컴퓨터 설명 스크린샷](../media/eDiscoDownload.png)

## <a name="export-documents-from-a-review-set"></a>검토 집합에서 문서 내보내기

내보내기를 사용 하면 다운로드 패키지에 포함 된 콘텐츠를 사용자 지정할 수 있습니다. 다음 설정을 사용 하 여 구성 페이지를 제공 합니다.

### <a name="metadata-file"></a>메타 데이터 파일

내보낸 파일에 연결 된 메타 데이터를 포함 하는 "로드 파일"으로 간주 될 수 있습니다. 메타 데이터 파일에서 사용할 수 있는 필드 목록은 link \[\]를 참조 하십시오. 이 파일은 일반적으로 3 개<sup>rd</sup> 파티 도구 ingested 될 수 있습니다.

### <a name="tag-data"></a>태그 데이터

이 콘텐츠는 메타 데이터 파일에서 필드로 추가 됩니다. 여기에는 검토 집합에 적용 된 태그 정보가 모두 포함 됩니다.

### <a name="text-files"></a>텍스트 파일

검토 집합에서 내보낸 각 파일에 대해 텍스트 파일을 생성할 수 있습니다. Ingesting 데이터의 일부로 서비스 파트너가 이러한 파일을 3 개의<sup>rd</sup> 파티 도구 다운스트림으로 필요로 하는 경우가 종종 있습니다.

### <a name="redacted-files"></a>Redacted 파일

검토 중에 redacted Pdf가 생성 되 면 내보내는 동안 이러한 파일을 사용할 수 있습니다. 사용자는 기본 파일만 내보낼지 아니면 redactions가 포함 된 natives를 Pdf에서 구운 것으로 바꿀지를 결정할 수 있습니다.

### <a name="export-location"></a>내보내기 위치

내보낸 콘텐츠가 Microsoft에서 제공한 Azure blob로 배달 되거나, 내보내기에서 세부 정보를 제공 하는 경우 고객의 blob를 사용할 수 있습니다.

### <a name="export-structure"></a>내보내기 구조

검토 집합에서 콘텐츠를 내보내면 콘텐츠가 다음 구조로 구성 됩니다.

  - 루트 폴더-다운로드 ID
    
      - 로드\_\_파일 .csv = 메타 데이터 파일 내보내기
    
      - 요약 .txt = 내보내기 통계가 포함 된 요약 파일
    
      - 입력\_또는 네이티브\_파일 = 모든 네이티브 파일 포함
    
      - 오류\_파일 = 내보내기에 포함 된 오류 파일을 포함 합니다.
        
          - ExtractionError-상위 파일에서 제대로 추출 되지 않은 파일의 사용 가능한 메타 데이터가 포함 된 csv입니다.
        
          - ProcessingError – 처리 오류가 발생 한 콘텐츠입니다. 이 콘텐츠는 항목 수준 이므로 첨부 파일에 처리 오류가 발생 한 경우 첨부 파일이 포함 된 전자 메일이이 폴더에 포함 됩니다.
    
      - 추출\_된\_텍스트 파일 = 처리 시 생성 되는 모든 추출한 텍스트 파일을 포함 합니다.