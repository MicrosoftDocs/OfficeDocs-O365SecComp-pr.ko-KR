---
title: 상위 도메인 메일 흐름 상태 파악
ms.author: chrisda
author: chrisda
manager: serdars
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.assetid: ''
description: 관리자는 Office 365 Security & 준수 센터의 메일 흐름 대시보드에 있는 최상위 도메인 메일 흐름 상태에 대해 알아볼 수 있습니다.
ROBOTS: NOINDEX, NOFOLLOW
ms.openlocfilehash: 04aa986982465a4c66fbf99f517fb34622d65e19
ms.sourcegitcommit: fec1010e405f14e792d650aee0312b78fced3343
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/21/2019
ms.locfileid: "30722996"
---
# <a name="top-domain-mail-flow-status-insight"></a>상위 도메인 메일 흐름 상태 파악

> [!NOTE]
> 이 항목에서 설명 하는 기능은 모든 Office 365 조직에 배포 되지 않으며 변경 될 수 있습니다.

**최상위 도메인 메일 흐름 상태** 정보를 통해 메일 흐름 측면에서 조직의 도메인에 대 한 현재 상태를 알 수 있습니다. 이러한 통찰력은 ***메일 흐름에 영향*** 을 주는 (예: 외부 전자 메일을 받을 수 없음), 특히 도메인 만료 또는 잘못 된 MX 레코드가 있는 도메인의 문제를 파악 하 고 문제를 해결 하는 데 도움이 됩니다.

![Office 365 보안 & 준수 센터의 메일 흐름 대시보드에서 가장 중요 한 도메인 흐름 상태를 파악 합니다.](media/domain-mail-flow-status-selected.png)

**자세한 내용은 자세히 보기** 를 클릭 하면 각 도메인의 상태에 대 한 세부 정보를 보여 주는 플라이 아웃이 나타납니다.

도메인에 대 한 녹색 확인 표시는 현재 MX 레코드 (메일 흐름 insights 대시보드를 탐색할 때)가 레코드에 포함 된 값과 일치 하 고, 지난 2 시간 동안 도메인에서 전자 메일을 받은 것을 나타냅니다.

도메인에 대 한 빨간색 x는 MX 레코드가 변경 되었으며 도메인에서 지난 6 시간 동안 전자 메일을 받지 못했음을 나타냅니다. 이는 사용자의 도메인이 만료 되었거나 MX 레코드가 잘못 업데이트 되었음을 나타내는 것일 수 있습니다. 도메인 등록 기관 또는 DNS 호스팅 서비스에 문의 하 여 도메인의 사용 기간이 만료 되었는지 여부 또는 도메인의 MX 레코드가 올바르지 않은 지 확인 합니다.

![최상위 도메인 흐름 상태 이해의 세부 정보 플라이 아웃](media/domain-mail-flow-status-flyout.png)

## <a name="see-also"></a>참고 항목

메일 흐름 대시보드의 다른 메일 흐름 정보에 대 한 자세한 내용은 [Security & 준수 센터의 메일 흐름 정보](mail-flow-insights-v2.md)를 참조 하십시오.
