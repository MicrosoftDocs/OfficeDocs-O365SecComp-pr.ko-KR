---
title: 정보 장벽 개요
ms.author: chrfox
author: chrfox
manager: laurawi
ms.date: 07/08/2019
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.collection:
- M365-security-compliance
localization_priority: None
description: 정보 장애물을 사용 하 여 조직 내에서 Microsoft 팀을 사용 하 여 통신을 준수 하는지 확인 합니다.
ms.openlocfilehash: b23e0f4285b2bee08dd19793f8461f39328e85f5
ms.sourcegitcommit: 7a0cb7e1da39fc485fc29e7325b843d16b9808af
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/07/2019
ms.locfileid: "36230402"
---
# <a name="information-barriers"></a>정보 장벽

## <a name="overview"></a>개요

Microsoft 클라우드 서비스에는 강력한 통신 및 공동 작업 기능이 포함 되어 있습니다. 하지만 조직에서 발생할 수 있는 충돌을 방지 하기 위해 두 그룹 간의 통신을 제한 하려는 경우를 가정해 보겠습니다. 아니면 내부 정보를 보호 하기 위해 조직 내부의 특정 사용자 간의 통신을 제한 하려는 경우도 있습니다. Microsoft 365을 사용 하면 그룹 및 조직에서 통신 및 공동 작업을 수행할 수 있으므로 필요한 경우 특정 사용자 그룹 간에 통신을 제한할 수 있는 방법이 있나요? 정보 장벽에서는 다음을 수행할 수 있습니다. 

Microsoft 팀부터 정보 장애물을 즉시 롤아웃할 수 있습니다. [구독](#required-licenses-and-permissions) 에 정보 장애가 포함 된 경우 규정 준수 관리자 또는 정보 장벽 관리자는 Microsoft 팀의 사용자 그룹 간 통신을 허용 하거나 차단 하는 정책을 정의할 수 있습니다. 정보 장벽 정책은 다음과 같은 경우에 사용할 수 있습니다.

- 하루 상인은 마케팅 팀에서 다른 사람에 게 전화를 걸 수 없습니다.
- 기밀 회사 정보에 대 한 작업을 수행 하는 금융 직원은 조직 내의 특정 그룹에서 전화를 받을 수 없습니다.
- 영업 비밀 자료가 있는 내부 팀이 조직 내의 특정 그룹에 있는 사용자와 통화 하거나 온라인으로 대화할 수 없습니다.
- 연구 팀은 제품 개발 팀과 온라인 으로만 전화를 걸어 대화할 수 있습니다.

이러한 모든 시나리오 (및 이상)에서 정보 장벽 정책은 Microsoft 팀의 통신을 방지 하거나 허용 하도록 정의할 수 있습니다. 이러한 정책을 사용 하면 사용자가 전화를 걸 수도 있고 채팅을 할 수 없거나, 사용자가 Microsoft 팀의 특정 그룹과 통신 하는 것을 허용 합니다. 정보 장벽 정책을 적용 하면 해당 정책에 포함 된 사용자가 Microsoft 팀의 다른 사람들과 통신을 시도할 때마다 정보 장벽 정책에 정의 된 대로 통신을 방지 하거나 허용 하기 위해 검사가 수행 됩니다. 정보 장벽에 대 한 사용자 환경에 대 한 자세한 내용은 [Microsoft 팀의 정보 장벽](https://docs.microsoft.com/MicrosoftTeams/information-barriers-in-teams)를 참조 하세요.

> [!IMPORTANT]
> 현재 정보 장애물은 SharePoint Online 또는 OneDrive를 통한 전자 메일 통신 또는 파일 공유에는 적용 되지 않습니다. 또한 정보 장애물은 [준수 경계](set-up-compliance-boundaries.md)와는 별개입니다.<p>정보 장벽 정책을 정의 하 고 적용 하기 전에 조직에 [Exchange 주소록 정책이](https://docs.microsoft.com/en-us/exchange/address-books/address-book-policies/address-book-policies) 적용 되지 않았는지 확인 합니다. 정보 장애물은 주소록 정책에 따라 달라 집니다. 

## <a name="what-happens-with-information-barriers"></a>정보 장벽에 따라 수행 되는 작업

정보 장벽 정책이 적용 되 면 다른 특정 사용자와 통신 하지 않아야 하는 사용자는 해당 사용자를 찾거나, 선택 하거나, 채팅 하거나, 전화를 걸 수 없습니다. 정보 장벽에서는 확인이 수행 되어 무단 통신을 방지 합니다.

초기 정보 장애물은 Microsoft 팀 채팅 및 채널만 해당 됩니다. Microsoft 팀에서 정보 장벽 정책은 다음과 같은 종류의 무단 통신을 결정 하 고 방지 합니다.
- 사용자 검색
- 팀에 구성원 추가
- 다른 사용자와의 채팅 세션 시작
- 그룹 채팅 시작
- 다른 사용자에 게 모임 참가 초대
- 화면 공유
- 전화 걸기 

활동을 방지 하기 위해 관련 된 사용자가 정보 장벽 정책에 포함 된 경우에는 작업을 계속할 수 없게 됩니다. 또한 정보 장벽 정책에 포함 된 모든 사용자는 Microsoft 팀에서 다른 사람들과의 통신을 차단할 수 있습니다. 정보 장벽 정책의 영향을 받는 사용자가 같은 팀 또는 그룹 채팅에 속해 있으면 해당 채팅 세션에서 제거 될 수 있으며, 그룹에 대 한 추가 통신을 허용 하지 못할 수 있습니다.

정보 장벽에 대 한 사용자 환경에 대 한 자세한 내용은 [Microsoft 팀의 정보 장벽](https://docs.microsoft.com/MicrosoftTeams/information-barriers-in-teams)를 참조 하세요.

## <a name="required-licenses-and-permissions"></a>필요한 라이선스 및 사용 권한

정보 장애물은 지금 롤아웃 되며 다음과 같은 구독에 포함 됩니다.

- Microsoft 365 E5
- Office 365 E5
- Office 365 Advanced Compliance
- Microsoft 365 E5 정보 보호 및 규정 준수

자세한 내용은 [준수 솔루션](https://products.office.com/business/security-and-compliance/compliance-solutions)을 참조 하십시오.

[정보 장벽 정책을 정의 하거나 편집](information-barriers-policies.md)하려면 다음 역할 중 하나를 할당 받아야 합니다.

- Microsoft 365 전역 관리자
- Office 365 전역 관리자
- 준수 관리자
- IB 준수 관리 (새 역할입니다.)

역할 및 사용 권한에 대 한 자세한 내용은 [Office 365 보안 & 준수 센터의 사용 권한을](permissions-in-the-security-and-compliance-center.md)참조 하세요.

정보 장벽 정책을 정의, 유효성 검사 또는 편집 하려면 PowerShell cmdlet을 잘 알고 있어야 합니다. [방법 문서에는](information-barriers-policies.md)여러 PowerShell cmdlet 예제가 제공 되지만, 조직에 대 한 매개 변수 등의 추가 정보를 알고 있어야 합니다.

## <a name="next-steps"></a>다음 단계

- [Microsoft 팀의 정보 장벽에 대해 자세히 알아보기](https://docs.microsoft.com/MicrosoftTeams/information-barriers-in-teams)

- [정보 장벽 정책에 사용할 수 있는 특성 확인](information-barriers-attributes.md)

- [정보 장벽에 대 한 정책 정의](information-barriers-policies.md)

- [정보 장벽 정책 편집 또는 제거](information-barriers-edit-segments-policies.md.md) 

