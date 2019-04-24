---
title: 보안 및 준수 센터의 메일 흐름 파악
ms.author: chrisda
author: chrisda
manager: serdars
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.assetid: beb6acaa-6016-4d54-ba7e-3d6d035e2b46
description: 관리자는 Security & 준수 센터의 메일 흐름 대시보드에 대해 알아볼 수 있습니다.
ROBOTS: NOINDEX, NOFOLLOW
ms.openlocfilehash: 4af35fea640c1f4c43464d1adf2e4a9f3b4f780d
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32252114"
---
# <a name="mail-flow-insights-in-the-security--compliance-center"></a>보안 및 준수 센터의 메일 흐름 파악

> [!NOTE]
> 이 항목에서 설명 하는 기능은 모든 Office 365 조직에 배포 되지 않으며 변경 될 수 있습니다.

관리자는 Security & 준수 센터의 메일 흐름 대시보드를 사용 하 여 경향 및 통찰력을 검색 하 고, Office 365 조직의 메일 흐름과 관련 된 문제를 해결 하는 조치를 취할 수 있습니다.

메일 흐름 대시보드에서 사용할 수 있는 다음과 같은 정보를 제공 합니다.

- [메일 흐름 맵 보고서](mfi-mail-flow-map-report.md) (이 보고서는 새로운 것 이며 현재 Office 365에서 배포 되 고 있습니다.)

- [도메인 메일 흐름 상태 파악](mfi-domain-mail-flow-status-insight.md) (이 정보는 신규 이며, 현재 Office 365에서 배포 되 고 있습니다.)

- [SMTP 인증 클라이언트 보고서](mfi-smtp-auth-clients-report.md) (이 보고서는 새로운 것 이며 현재 Office 365에서 배포 되 고 있습니다.)

- [보낸 사람 도메인 통찰력](mfi-sender-domain-insight.md) (이 정보는 신규 이며, 현재 Office 365에서 배포 되 고 있습니다.)

- [배달 못 함 보고서](mfi-non-delivery-report.md) (이 보고서는 새로운 것 이며 현재 Office 365에서 배포 되 고 있습니다.)

- [허용 되지 않는 도메인 보고서](mfi-non-accepted-domain-report.md) (이 보고서는 새로운 것 이며 현재 Office 365에서 배포 되 고 있습니다.)

- [아웃바운드 및 인바운드 메일 흐름](mfi-outbound-and-inbound-mail-flow.md)

- [큐 알림 및 큐](mfi-queue-alerts-and-queues.md)

- [자동 전달 메시지 보고서](mfi-auto-forwarded-messages-report.md)

- [메일 루프 파악](mfi-mail-loop-insight.md)

- [느린 메일 흐름 규칙 파악](mfi-slow-mail-flow-rules-insight.md)

## <a name="permissions-required-to-view-the-mail-flow-dashboard"></a>메일 흐름 대시보드를 보는 데 필요한 사용 권한

메일 흐름 대시보드는 다음 위치에서 사용할 수 있습니다.

- **Office 365 전역 관리자** 역할의 구성원

- **Office 365 Exchange 관리자** 역할의 구성원

- Security & 준수 센터에서 **메일 흐름 관리자 역할** 의 구성원 이 역할이 전역 관리자 또는 Exchange 관리자 역할의 구성원이 아닌 사용자에 게 명시적으로 할당 된 경우 다음을 수행 합니다.

  - 사용자는에서 [https://protection.office.com](https://protection.office.com)직접 보안 & 준수 센터에 로그인 해야 합니다.

  - 사용자에 게는 메일 흐름 대시보드에 대 한 읽기 전용 권한만 있습니다.

  - 사용자에 게 Office 365 관리 포털에 대 한 액세스 권한이 없습니다.

office 365 전역 관리자 역할에 대 한 자세한 내용은 [office 365 관리자 역할 정보](https://docs.microsoft.com/office365/admin/add-users/about-admin-roles)를 참조 하세요.

사용자에 게 보안 & 준수 센터 역할을 할당 하는 방법에 대 한 자세한 내용은 사용자에 게 [보안 & 준수 센터에 대 한 액세스 권한을 부여](https://docs.microsoft.com/office365/securitycompliance/grant-access-to-the-security-and-compliance-center)합니다.

## <a name="where-to-find-the-mail-flow-dashboard"></a>메일 흐름 대시보드를 찾는 위치

1. 의 Security & 준수 센터로 이동 [https://protection.office.com](https://protection.office.com)합니다.

2. **메일 흐름** 을 확장 한 다음 **대시보드**를 선택 합니다.

   ![Office 365 보안 & 준수 센터의 메일 흐름 대시보드](media/mail-flow-dashboard-v2.png)
