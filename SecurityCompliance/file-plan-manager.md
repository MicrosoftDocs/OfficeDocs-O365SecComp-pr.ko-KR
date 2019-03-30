---
title: 파일 계획 관리자 개요
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: conceptual
ms.service: O365-seccomp
localization_priority: Priority
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: af398293-c69d-465e-a249-d74561552d30
description: 파일 계획 관리자는 보존 레이블 및 정책에 대한 고급 관리 기능을 제공하고, 생성부터 공동 작업, 레코드 선언, 보존 및 최종 처리에 이르는 전체 콘텐츠 수명 주기 동안 레이블 및 레이블-콘텐츠 간 활동을 트래버스하는 통합 방법을 제공합니다.
ms.openlocfilehash: a6086ce73f898d261af46a1f1493b624db10931d
ms.sourcegitcommit: 799a958fcac643f62dfac6fa04020f2f4758635c
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/29/2019
ms.locfileid: "30997274"
---
# <a name="overview-of-file-plan-manager"></a>파일 계획 관리자 개요

파일 계획 관리자는 보존 레이블 및 정책에 대한 고급 관리 기능을 제공하고, 생성부터 공동 작업, 레코드 선언, 보존 및 최종 처리에 이르는 전체 콘텐츠 수명 주기 동안 레이블 및 레이블-콘텐츠 간 활동을 트래버스하는 통합 방법을 제공합니다.

![파일 계획 페이지](media/file-plan-page.png)

## <a name="accessing-file-plan-manager"></a>파일 계획 관리자 액세스

파일 계획 관리자에 액세스하려면 다음 두 가지 요구 사항이 충족되어야 합니다.
- Office 365 Enterprise E5 구독
- 사용자에게 보안 및 준수 센터의 다음 역할 중 하나가 할당되어야 합니다. 
    - 보존 관리자
    - 보기 전용 보존 관리자

## <a name="navigating-your-file-plan"></a>파일 계획 탐색

파일 계획 관리자를 사용하면 하나의 보기에서 모든 보존 레이블 및 정책의 설정을 보다 쉽게 검토할 수 있습니다.

파일 계획 외부에서 만들어진 보존 레이블도 파일 계획에서 사용할 수 있고 그 반대의 경우도 가능합니다.

**파일 계획 레이블** 탭에서 다음과 같은 추가 정보 및 기능을 사용할 수 있습니다.

### <a name="label-settings-columns"></a>레이블 설정 열
 
- **기준**은 보존 기간을 시작할 트리거 유형을 식별합니다. 유효한 값은 다음과 같습니다. 
    - 이벤트
    - 만든 날짜
    - 마지막으로 수정한 날짜
    - 레이블을 지정한 날짜
- **레코드**는 레이블이 적용될 때 항목이 선언된 레코드가 될지를 식별합니다. 유효한 값은 다음과 같습니다.
    - 아니요
    - 예
    - 예(규정)
- **보존**은 보존 유형을 식별합니다. 유효한 값은 다음과 같습니다.
    - 유지
    - 유지 및 삭제
    - 삭제
- **처리**는 보존 기간이 끝날 때 콘텐츠에 대해 수행할 작업을 식별합니다. 유효한 값은 다음과 같습니다. 
    - null
    - 작업 없음
    - 자동 삭제
    - 검토 필요(즉, 처리 검토)

![파일 계획의 레이블 설정](media/file-plan-label-columns.png)

### <a name="label-file-plan-descriptors-columns"></a>레이블 파일 계획 설명자 열

이제 보존 레이블 구성에 더 많은 정보를 포함할 수 있습니다. 레이블에 파일 계획 설명자를 삽입하면 파일 계획의 관리 효율성과 구성이 개선됩니다.

시작하기 위해 파일 계획 관리자에서는 직무/부서, 범주, 권한 유형 및 프로비저닝/인용에 대한 기본 제공 값을 제공합니다. 보존 레이블을 만들거나 편집할 때 새 파일 계획 설명자 값을 추가할 수 있습니다.

보존 레이블을 만들거나 편집할 때의 파일 계획 설명자 단계 보기는 다음과 같습니다.

![파일 계획 설명자](media/file-plan-descriptors.png)

파일 계획 관리자의 레이블 탭에 표시되는 파일 계획 설명자 열 보기는 다음과 같습니다.

![file-plan-descriptors-on-labels-tab.png](media/file-plan-descriptors-on-labels-tab.png)

## <a name="export-labels-out-of-your-file-plan"></a>파일 계획에서 레이블 내보내기

파일 계획 관리자에서 모든 보존 레이블의 세부 정보를 .csv 파일로 내보내 조직의 데이터 거버넌스 이해 관계자와 함께 정기적인 검토를 편리하게 수행할 수 있습니다.

모든 보존 레이블의 내보내려면 **파일 계획 관리자** \> **파일 계획 작업** \> **레이블 내보내기**로 이동합니다.

![파일 계획 내보내기 옵션](media/file-plan-export-labels-option.png)

모든 기존 보존 레이블을 포함하는 *.csv 파일이 열립니다.

![모든 보존 레이블이 표시되는 CSV 파일](media/file-plan-csv-file.png)

## <a name="import-labels-into-your-file-plan"></a>파일 계획으로 레이블 가져오기

파일 계획 관리자에서 기존 보존 레이블을 수정할 수 있을 뿐만 아니라 새 레이블을 대량으로 가져올 수 있습니다.

새 보존 레이블이 가져오고 기존 보존 레이블을 업데이트하려면 **파일 계획 관리자** \> **파일 계획 작업** \> **레이블 가져오기**로 이동합니다.

![파일 계획 가져오기 옵션](media/file-plan-import-labels-option.png)

![빈 파일 계획 서식 파일 다운로드 옵션](media/file-plan-blank-template-option.png)

빈 서식 파일을 다운로드합니다(또는 현재 파일 계획의 내보내기 기능을 통해 시작).

![Excel에서 빈 파일 계획 서식 파일 열기](media/file-plan-blank-template.png)

서식 파일을 채웁니다(항목에 대한 유효한 값에 대한 참조 정보가 곧 제공될 예정임).

![정보가 채워진 파일 계획 서식 파일](media/file-plan-filled-out-template.png)

채운 서식 파일을 업로드하면 파일 계획 관리자에서 항목의 유효성을 검사하고 가져오기 통계를 표시합니다.

![파일 계획 가져오기 통계](media/file-plan-import-statistics.png)

가져오기가 완료되면 파일 계획 관리자로 돌아가 새 정책 또는 기존 정책에 새 레이블을 할당합니다.

![레이블 게시 옵션](media/file-plan-publish-labels-option.png)

