---
title: Microsoft 365에서 데이터 조사 (미리 보기)에 대 한 릴리스 정보
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection: ''
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: 이 문서에서는 Microsoft 365의 고급 eDiscovery (미리 보기)의 새 버전에 설명 합니다.
ms.openlocfilehash: 90bcbd4cae1e410e1544352a776ba4cbbedfa429
ms.sourcegitcommit: 7e2a0185cadea7f3a6afc5ddc445eac2e1ce22eb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/11/2019
ms.locfileid: "29695064"
---
# <a name="release-notes-for-data-investigations-preview-in-microsoft-365"></a>Microsoft 365에서 데이터 조사 (미리 보기)에 대 한 릴리스 정보

새 데이터 조사 (미리 보기) 도구를 사용할 수에서 분류할 조사 및 데이터를 수정 하려면 Microsoft 365에서 관련 사고, 예: 데이터 액체 엎질렀는지 여부 문제를 또는 내부 조사 합니다. 공용 데이터 미리 보기 조사 예정 된 기능 및 업데이트에 대 한 초기 액세스를 제공 합니다. 최신 기능에 대 한 초기 액세스 하려면 Office 365 보안 & 준수 센터의에서 데이터 조사 (미리 보기)에서 새 조사를 만듭니다. 자세한 방법, [관리 Microsoft 365에서 데이터 액체 엎질렀는지 여부 문제를](manage-data-spillage-incidents.md)참조 하십시오.

## <a name="whats-new"></a>새로운 기능 

- **조사** -조사를 만들어 검색 및 사고 그룹화 수 있습니다. 구성원 추가 또는 제거 하 여 조사를 액세스할 수 있는 사용자를 관리 합니다.  선택 하 고 좋아하는 조사 표시 수도 있습니다. 새 대시보드를 사용 하 여 조사 및 내에서 추적 및 모니터링 작업 합니다. 검사를 완료 한 후 닫습니다 하거나 삭제할 수 있습니다.

- **관심 있는 사람** – 관심 있는 사람으로 조사에 사용자를 추가 하는 경우, OneDrive 비즈니스 계정 하 고 Microsoft 팀 사이트에 대 한 사서함을 볼 수 있습니다. 조사 콘텐츠 검색 범위를 지정 하 고 사용할 수 있습니다. 관심 사용자를 더 자세히 조사를 볼 수도 있습니다 Office 365와 다른 Microsoft 서비스에서 팔 로우와 관련 된 레코드를 감사 합니다.

- **검색** – 만들기 다양 한를 사용 하 여 조직 전체의 검색 검색 조건입니다. 사용자 또는 사이트를 검색 하려면를 알고 있는 경우 해당 사용자가 관심 또는 검색 만들기 마법사에서 사이트 위치를 지정 하는 사람으로 추가 하 여 이렇게 수 있습니다. 

- **문제** -새 인시던트를 만들고 검토 하려는 검색 결과 추가 합니다. 개별 문서를 검토 하 고, 조사 정보를 유지 하도록 주석을 달 하 고, 서로 다른 환경으로 이동 하는 결과 내보낼 수 있습니다. 

- **검토** – 네이티브를 사용 하 여, 텍스트 및 네이티브 근처 보기 인시던트에 추가 하 고 문서를 검토 하 합니다. 중복 되는 값, 전자 메일 스레드 및 사고 검토를 지원 하는 데 도움이 되는 테마에서 항목을 그룹화 하는 문서를 분석을 적용할 수 있습니다. 

- **Redact, 태그와 주석을 달** -텍스트 교정 태그를 적용 하 고 문서를 검토할 때 주석을 합니다.
  
- **상세 인덱싱** – 부분적으로 인덱싱된 항목이 있을 경우, 될 필요에 따라 다시 인덱싱 모든 데이터를 검색에 사용할 수 있도록 합니다.

- **오류 수정** -Remediate 또는 오류를 처리 하는 다운로드 합니다. 파일 및 인덱싱 오류와 관련 된 다른 문제 암호로 보호 된, 대용량 파일 형식에 대 한 업데이트 관리 지원을 포함이 됩니다. 

- **작업** -장기 실행 프로세스의 상태를 추적 합니다.

- **사서함 항목 하드 삭제** -긴급 상황에서 해야 위치가 잘못 된 항목을 영구적으로 삭제 합니다. 이 위해 실행할 수 있습니다는 **새로 ComplianceSearchAction--PurgeType HardDelete 항목 지우기** 보안 & 사서함에서 항목을 영구적으로 제거 하려면 준수 센터 PowerShell에에서 명령 합니다. 자세한 내용은 [ComplianceSearchAction 새로 만들기를](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-content-search/new-compliancesearchaction)참조 하십시오.
