---
title: 정보 장벽 개요
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 06/26/2019
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.collection:
- M365-security-compliance
localization_priority: None
description: 정보 장애물을 사용 하 여 조직 내에서 Microsoft 팀을 사용 하 여 통신을 준수 하는지 확인 합니다.
ms.openlocfilehash: 6565fc28d70ac6ff9a6f4df6edc75b89d19ae29a
ms.sourcegitcommit: 1c254108c522d0cb44023565268b5041d07748aa
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/27/2019
ms.locfileid: "35279476"
---
# <a name="information-barriers-preview"></a>정보 장벽 (미리 보기)

## <a name="overview"></a>개요

Microsoft 클라우드 서비스에는 강력한 통신 및 공동 작업 기능이 포함 되어 있습니다. 하지만 조직에서 발생할 수 있는 충돌을 방지 하기 위해 두 그룹 간의 통신을 제한 하려는 경우를 가정해 보겠습니다. 아니면 내부 정보를 보호 하기 위해 조직 내부의 특정 사용자 간의 통신을 제한 하려는 경우도 있습니다. Microsoft 365을 사용 하면 그룹 및 조직에서 통신 및 공동 작업을 수행할 수 있으므로 필요한 경우 특정 사용자 그룹 간에 통신을 제한할 수 있는 방법이 있나요? 정보 장벽에서는 다음을 수행할 수 있습니다. 

정보 장애물은 지금 미리 볼 수 있습니다 (Microsoft 팀부터 시작). 조직에서 이러한 기능을 사용할 수 있는 경우 준수 관리자 또는 정보 장벽 관리자는 Microsoft 팀의 사용자 그룹 간 통신을 허용 하거나 차단 하는 정책을 정의할 수 있습니다. 정보 장벽 정책은 다음과 같은 경우에 사용할 수 있습니다.

- 하루 상인은 마케팅 팀에서 다른 사람에 게 전화를 걸 수 없습니다.
- 기밀 회사 정보에 대 한 작업을 수행 하는 금융 직원은 조직 내의 특정 그룹에서 전화를 받을 수 없습니다.
- 영업 비밀 자료가 있는 내부 팀이 조직 내의 특정 그룹에 있는 사용자와 통화 하거나 온라인으로 대화할 수 없습니다.
- 연구 팀은 제품 개발 팀과 온라인 으로만 전화를 걸어 대화할 수 있습니다.

이러한 모든 시나리오 (및 이상)에서 정보 장벽 정책은 Microsoft 팀의 통신을 방지 하거나 허용 하도록 정의할 수 있습니다. 이러한 정책을 사용 하면 사용자가 전화를 걸 수도 있고 채팅을 할 수 없거나, 사용자가 Microsoft 팀의 특정 그룹과 통신 하는 것을 허용 합니다. 정보 장벽 정책을 적용 하면 해당 정책에 포함 된 사용자가 Microsoft 팀의 다른 사람들과 통신을 시도할 때마다 정보 장벽 정책에 정의 된 대로 통신을 방지 하거나 허용 하기 위해 검사가 수행 됩니다. 정보 장벽에 대 한 사용자 환경에 대 한 자세한 내용은 [Microsoft 팀의 정보 장벽](https://docs.microsoft.com/MicrosoftTeams/information-barriers-in-teams)를 참조 하세요.

> [!NOTE]
> 정보 장애물은 SharePoint Online 또는 OneDrive를 통한 전자 메일 통신 또는 파일 공유에는 적용 되지 않습니다. 또한 정보 장애물은 [준수 경계](set-up-compliance-boundaries.md)와는 별개입니다.

## <a name="required-licenses-and-permissions"></a>필요한 라이선스 및 사용 권한

**현재 정보 장벽 기능은 개인 미리 보기에**있습니다. 일반적으로 이러한 기능을 사용할 수 있는 경우 다음과 같은 구독에 포함 됩니다.

- Microsoft 365 E5
- Office 365 E5
- Office 365 Advanced Compliance
- Microsoft 365 E5 정보 보호 및 규정 준수

자세한 내용은 [준수 솔루션](https://products.office.com/business/security-and-compliance/compliance-solutions)을 참조 하십시오.

[정보 장벽 정책을 정의 하거나 편집](information-barriers-policies.md)하려면 다음 역할 중 하나를 할당 받아야 합니다.

- Microsoft 365 전역 관리자
- Office 365 전역 관리자
- 준수 관리자
- 정보 장벽 관리자

정보 장벽 정책을 정의, 유효성 검사 또는 편집 하려면 PowerShell cmdlet을 잘 알고 있어야 합니다. [방법 정보](information-barriers-policies.md)에 PowerShell cmdlet의 몇 가지 예를 제공 하지만, 조직에 대 한 매개 변수 등의 추가 정보를 파악 해야 합니다.

## <a name="concepts-of-information-barrier-policies"></a>정보 장벽 정책의 개념

정보 장벽 정책의 기본 개념을 이해 하는 데 도움이 됩니다.

- **사용자 계정 특성** 은 Azure Active Directory (또는 Exchange Online)에서 정의 됩니다. 이러한 특성에는 부서, 직함, 위치, 팀 이름 및 기타 작업 프로필 정보가 포함 될 수 있습니다. 

- **세그먼트** 는 선택한 **사용자 계정 특성**을 사용 하 여 Office 365 보안 & 준수 센터에 정의 된 사용자 집합입니다. ( [지원 되는 특성 목록](information-barriers-attributes.md)참조) 

- **정보 장벽 정책** 에 따라 통신 제한 또는 제한이 결정 됩니다. 정보 장벽 정책을 정의할 때는 두 가지 정책 유형 중에서 선택 합니다.
    - "차단" 정책은 한 세그먼트가 다른 세그먼트와 통신 하지 못하도록 합니다.
    - "허용" 정책은 한 세그먼트가 다른 특정 세그먼트와도 통신할 수 있도록 허용 합니다.

- **정책 응용 프로그램** 은 모든 정보 장벽 정책이 정의 된 후에 수행 되며, 조직에 적용할 준비가 된 것입니다.

## <a name="next-steps"></a>다음 단계

- [Microsoft 팀의 정보 장벽에 대해 자세히 알아보기](https://docs.microsoft.com/MicrosoftTeams/information-barriers-in-teams)
- [정보 장벽 정책에 사용할 수 있는 특성 확인](information-barriers-attributes.md)
- [정보 장벽에 대 한 정책 정의](information-barriers-policies.md) 

