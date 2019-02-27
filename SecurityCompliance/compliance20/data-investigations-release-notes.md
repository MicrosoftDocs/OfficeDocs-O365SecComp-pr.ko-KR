---
title: Microsoft 365의 데이터 조사 (미리 보기)에 대 한 릴리스 정보
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: 이 문서에서는 Microsoft 365의 새로운 고급 eDiscovery (미리 보기) 버전에 대해 설명 합니다.
ms.openlocfilehash: 900031815ef1a2bbbd770c22db958659d8a0ef99
ms.sourcegitcommit: baf23be44f1ed5abbf84f140b5ffa64fce605478
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/26/2019
ms.locfileid: "30297031"
---
# <a name="release-notes-for-data-investigations-preview-in-microsoft-365"></a>Microsoft 365의 데이터 조사 (미리 보기)에 대 한 릴리스 정보

Microsoft 365의 새 데이터 조사 (미리 보기) 도구를 사용 하 여 데이터 유출 사고나 내부 조사와 같은 데이터 관련 인시던트를 심사, 조사 및 수정할 수 있습니다. 데이터 조사의 공개 미리 보기를 통해 예정 된 기능 및 업데이트에 빠르게 액세스할 수 있습니다. 최신 기능에 빨리 액세스 하려면 Office 365 보안 & 준수 센터에서 데이터 조사 (미리 보기)에 새로운 조사를 작성 합니다. 자세한 내용은 [Microsoft 365에서 data 유출 인시던트 관리](manage-data-spillage-incidents.md)를 참조 하세요.

## <a name="whats-new"></a>새로운 기능 

- **조사** -조사를 만들어 검색 및 인시던트를 그룹화 할 수 있습니다. 구성원을 추가 하거나 제거 하 여 조사에 액세스할 수 있는 사용자를 관리 합니다.  또한 즐겨찾기 조사를 선택 하 고 표시할 수 있습니다. 새 대시보드를 사용 하 여 조사 내의 및 간 활동을 추적 하 고 모니터링 합니다. 조사를 완료 한 후에는 닫거나 삭제할 수 있습니다.

- **관심** 사용자-사용자를 조사에 추가할 때 관심 있는 사서함, 비즈니스용 OneDrive 계정 및 Microsoft 팀 사이트를 볼 수 있습니다. 이를 사용 하 여 조사 콘텐츠 검색의 범위를 지정할 수 있습니다. 관심 있는 사람을 추가로 조사 하기 위해 Office 365 및 기타 Microsoft 서비스의 활동과 관련 된 감사 레코드도 볼 수 있습니다.

- **검색** -다양 한 검색 조건을 사용 하 여 조직 전체 검색을 만듭니다. 검색 하려는 사용자 또는 사이트를 알고 있는 경우 해당 사용자를 관심 있는 사람으로 추가 하거나 검색 만들기 마법사에서 사이트 위치를 지정 하 여이 작업을 수행할 수 있습니다. 

- **인시던트** -새 인시던트를 만들고 검토 하려는 검색 결과를 추가 합니다. 개별 문서를 검토 하 고 조사 메모를 남기기 위해 주석을 달고 다른 환경으로 이동 하 여 결과를 내보낼 수 있습니다. 

- **검토** -인시던트에 추가 된 문서를 검토 하려면 native, text 및 near 기본 보기를 사용 합니다. 중복, 전자 메일 스레드 및 테마를 기준으로 항목을 그룹화 하 여 문서에 분석을 적용할 수도 있으며,이를 통해 인시던트 검토에 도움이 될 수 있습니다. 

- 문서를 검토할 때 텍스트 교정 **, 태그 지정 및 주석 달기** /태그 적용 및 주석 만들기
  
- **깊이 인덱싱** -부분적으로 인덱싱된 항목이 있는 경우 모든 데이터를 검색할 수 있도록 요청 시 해당 항목을 다시 인덱싱합니다.

- **오류** 해결 방법-처리 오류를 수정 하거나 다운로드 합니다. 여기에는 큰 파일 형식, 암호로 보호 된 파일 및 인덱싱 오류와 관련 된 기타 문제에 대 한 재구성 지원이 포함 됩니다. 

- **작업** -장기 실행 프로세스의 상태를 추적 합니다.

- **사서함 항목 영구 삭제** -긴급 상황에서는 잘못 된 항목을 영구적으로 삭제 해야 할 수 있습니다. 이렇게 하려면 Security & 준수 센터 PowerShell에서 **new-compliancesearchaction-PurgeType 하드 삭제** 명령을 실행 하 여 사서함에서 항목을 영구적으로 제거 하면 됩니다. 자세한 내용은 [new-compliancesearchaction](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-content-search/new-compliancesearchaction)를 참조 하십시오.
