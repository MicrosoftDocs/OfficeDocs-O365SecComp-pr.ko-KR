---
title: Advanced eDiscovery에서 작업 관리 (미리 보기)
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
ms.openlocfilehash: 84e2a8dc389d738b8bda1ab21101b2e5e40eee03
ms.sourcegitcommit: cf9d9b545a7c153d314aa9c08c7fb16fcd785b3e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/21/2019
ms.locfileid: "30737648"
---
# <a name="manage-jobs-in-advanced-ediscovery-preview"></a>Advanced eDiscovery에서 작업 관리 (미리 보기)

다음은 Advanced eDiscovery (Preview)에서 사례의 **작업** 탭에 대해 추적 되는 작업 목록입니다.

| 작업 유형 | 설명 | 이 작업을 적용할 작업 |
| :- | :- | :- |
| custodian 데이터 다시 인덱싱 | custodian가 사례에 추가 되 면 모든 부분적으로 인덱싱된 항목이 고급 eDiscovery 인덱싱을 사용 하 여 다시 인덱싱되 며 자세한 내용은 [custodian 데이터의 고급 인덱싱을](indexing-custodian-data.md)참조 하십시오. | Office 365 고급 eDiscovery |
| 검색 결과 예측 | 검색 결과 예측은 Exchange, SharePoint 및 비즈니스용 OneDrive와 같은 작업에 대해 검색을 만들고 실행 했을 때의 결과입니다.  예측에는 검색 및 크기에 의해 반환 된 항목 수와 같은 통계가 포함 됩니다.  검색에 대 한 자세한 내용은 [Advanced eDiscovery에서 사례 데이터 수집](collecting-data-for-ediscovery.md)을 참조 하십시오. | Office 365 고급 eDiscovery |
| 검색 미리 보기 준비 | 검색 미리 보기 작업을 준비 하는 것은 Exchange, SharePoint 및 비즈니스용 OneDrive와 같은 작업을 만들고 검색을 실행 하는 결과입니다.  검색 결과의 미리 보기를 통해 검색의 efficacy를 확인할 수 있습니다.  검색에 대 한 자세한 내용은 [Advanced eDiscovery에서 사례 데이터 수집](collecting-data-for-ediscovery.md)을 참조 하십시오. | Office 365 고급 eDiscovery |
| 작업 집합에 데이터 추가 | 작업 집합에 검색 결과가 추가 될 때 실행 집합 작업에 데이터를 추가할 수 있습니다.  작업 집합을 관리 하는 방법에 대 한 자세한 내용은 [Advanced eDiscovery에서 작업 집합 관리](managing-working-sets.md)를 참조 하십시오. | Office 365 고급 eDiscovery |
| 다른 작업 집합에 데이터 추가 | 다른 작업 집합에 데이터 추가 사용자가 작업 집합 간에 데이터를 추가 하도록 선택할 때 만들어집니다. | Office 365 고급 eDiscovery |
| 작업 집합에 Office가 아닌 365 데이터 추가 | 작업 집합 작업에 office가 아닌 365 데이터를 추가 하려면 서비스 케이스와 관련이 있을 수 있는 클라이언트 컴퓨터에서 업로드 한 작업 집합에 데이터를 처리 하 고 추가 하는 작업이 포함 됩니다. 비 office 365 데이터를 추가 하는 방법에 대 한 자세한 내용은 다음을 참조 하십시오. [ 작업 집합](load-non-office365-data.md) | Office 365 고급 eDiscovery |
| 오류 해결 준비 |  | Office 365 고급 eDiscovery |
| 작업 집합에 재구성 된 데이터 추가 | 재구성 된 데이터를 작업 집합에 추가 하면 오류가 발생 한 파일을 재구성 하 여 Office 365 Advanced eDiscovery 작업 집합으로 다시 로드할 때 만들어지는 작업을 참조 합니다.  오류 수정에 대 한 자세한 내용은 [데이터를 처리할 때 오류 수정을](error-remediation.md)참조 하십시오. | Office 365 고급 eDiscovery |
| 부하 집합 비교 | 부하 집합을 비교 하 여 사용자가 작업 집합에 대 한 부하의 차이점을 조사할 수 있으며, 부하 집합에 대 한 자세한 내용은 [부하 집합 관리](manage-load-sets.md)를 참조 하세요. | Office 365 고급 eDiscovery |
| 문서 태그 지정 | 문서 태그 지정 작업 집합의 여러 문서가 태그 처리 될 때 발생 합니다.  자세한 내용은 [작업 집합의 태그 문서](tagging-documents.md)를 참조 하세요. | Office 365 고급 eDiscovery |
| 분석 실행 | 분석 작업 실행은 거의 중복 식별, 전자 메일 스레드 분석 및 테마 분석과 같은 처리 작업을 참조 하며, 분석에 대 한 자세한 내용은 [Advanced eDiscovery의 작업 집합에서 데이터 분석](analyzing-data-in-working-set.md)을 참조 하세요. | Office 365 고급 eDiscovery |
| 내보내기를 위해 데이터 준비 | 내보내기 작업에 대 한 데이터 준비 작업 집합에서 데이터를 내보내면 내보내기에 대 한 자세한 내용은 [Advanced eDiscovery에서 케이스 데이터 내보내기](exporting-data-ediscover20.md)를 참조 하십시오. | Office 365 고급 eDiscovery |
