---
title: Microsoft 365 보안에서 앱 상태 모니터링 및 보고
description: 조직에서 클라우드 앱 사용에 대 한 자세한 정보를 얻을 수 있는 방법에 대해 설명 합니다.
keywords: 보안, 맬웨어, Microsoft 365, M365, 보안 센터, 모니터, 보고서, 앱
ms.prod: w10
ms.mktglfcycl: deploy
ms.localizationpriority: medium
ms.author: ellevin
author: levinec
manager: dansimp
audience: ITPro
ms.collection: M365-security-compliance
ms.topic: article
ms.openlocfilehash: 02cc511532f65172aba2c0f98cdf594776f586a5
ms.sourcegitcommit: ef27da3ea5340d6e7a2eaa1288e2e005ef8e4788
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/23/2019
ms.locfileid: "30791840"
---
# <a name="monitor-and-report-app-status-in-microsoft-365-security"></a>Microsoft 365 보안에서 앱 상태 모니터링 및 보고

[!include[Prerelease�information](prerelease.md)]

이러한 보고서는 앱의 종류, 위험 수준 및 알림을 포함 하 여 조직에서 클라우드 앱을 사용 하는 방법에 대 한 자세한 정보를 제공 합니다.

## <a name="monitor-email-accounts-at-risk"></a>위험에 대 한 전자 메일 계정 모니터링

**전자 메일 보호** 는 위험의 전자 메일 계정을 보여 줍니다. Windows Defender 보안 센터에서 계정을 클릭 하 여 더 자세히 조사할 수 있습니다.

![전자 메일 보호 카드](./media/security-docs/email-protection.png)

## <a name="monitor-app-permissions-granted-by-users"></a>사용자가 허용한 앱 사용 권한 모니터링

**cloud app security-OAuth 앱** 은 사용자가 사용 권한을 부여 받은 Cloud app Security에서 검색 된 앱을 나열 합니다. Cloud App Security의 위험 카탈로그에는 70 위험 요소를 사용 하 여 평가 되는 16000 개 이상의 앱이 포함 됩니다.

위험 요인은 앱 게시자와 같은 일반 정보에서 응용 프로그램이 rest 암호화에 대해 지원 되는지 여부, 사용자 작업의 감사 로그를 제공 하는지 등의 보안 조치 및 제어에서 시작 됩니다.

![Cloud App Security OAuth 앱 카드](./media/security-docs/cloud-app-security-oauth-apps.png)

## <a name="monitor-cloud-app-user-accounts"></a>cloud app 사용자 계정 모니터링

**검토를 위한 Cloud app accounts에** 는 주의가 필요한 계정이 나열 되어 있습니다.

![검토 카드용 클라우드 앱 계정](./media/security-docs/cloud-app-accounts-for-review.png)

## <a name="understand-which-cloud-apps-are-used"></a>사용 되는 클라우드 앱 이해

**검색 된 클라우드 앱 (범주)** 은 조직에서 사용 중인 앱의 종류와 cloud App Security의 클라우드 검색 대시보드에 연결 되는 링크를 표시 합니다. 자세한 내용은 [퀵 스타트: 검색 된 앱에](https://docs.microsoft.com/cloud-app-security/discovered-apps)대 한 작업을 참조 하세요.  

![검색 된 클라우드 앱 범주 카드](./media/security-docs/discovered-cloud-apps-categories.png)

## <a name="monitor-where-users-access-cloud-apps"></a>사용자가 클라우드 앱에 액세스 하는 위치 모니터링

**클라우드 앱 활동 위치** 에는 사용자가 클라우드 앱에 액세스 하는 위치가 표시 됩니다.

![Cloud App activity 위치 카드](./media/security-docs/cloud-app-activity-locations.png)

## <a name="monitor-health-for-infrastructure-workloads"></a>인프라 작업의 상태 모니터링

**인프라 상태** 는 Azure 보안 센터에서 인프라 작업에 대 한 상태 알림을 표시 합니다.

Azure 보안 센터는 온-프레미스 및 클라우드 워크 로드에서 통합 된 보안 관리 및 advanced threat protection을 제공 합니다. 방화벽 및 기타 파트너 솔루션을 비롯 한 다양 한 원본의 보안 데이터를 수집, 검색 및 분석할 수 있습니다.

자세한 내용은 [Azure 보안 센터 설명서](https://docs.microsoft.com/azure/security-center/)를 참조 하세요.

![인프라 상태 카드](./media/security-docs/infrastructure-health.png)
