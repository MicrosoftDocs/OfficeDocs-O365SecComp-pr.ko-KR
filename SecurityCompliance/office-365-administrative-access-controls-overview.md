---
title: Office 365 관리 액세스 권한 컨트롤
ms.author: robmazz
author: robmazz
manager: laurawi
ms.date: 8/21/2018
audience: ITPro
ms.topic: article
ms.service: Office 365 Administration
localization_priority: None
search.appverid:
- MET150
ms.collection:
- Strat_O365_IP
- M365-security-compliance
description: '요약: Office 365의 관리 액세스 제어 및 데이터 분류에 대 한 개요입니다.'
ms.openlocfilehash: f5cac8b6161ea7eab6ea390e32caec1c5ddb9bac
ms.sourcegitcommit: c94cb88a9ce5bcc2d3c558f0fcc648519cc264a2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/20/2019
ms.locfileid: "30091030"
---
# <a name="administrative-access-controls-in-office-365"></a>Office 365 관리 액세스 권한 컨트롤 

## <a name="introduction"></a>소개
microsoft는 대부분의 Office 365 작업을 자동화 하는 시스템과 컨트롤에 대해 매우 많이 투자 되 고 적절 하 게 microsoft의 고객 콘텐츠에 대 한 액세스를 제한 합니다. 서비스를 관리 하 고 소프트웨어가 서비스를 운영 하는 사람입니다. 이를 통해 microsoft는 확장 시에 Office 365을 관리할 수 있을 뿐만 아니라, microsoft 엔지니어의 스피어 피싱 및 악의적인 행위자와 같은 고객 콘텐츠에 대 한 내부 위협의 위험을 관리할 수도 있습니다.

기본적으로 Microsoft 엔지니어가 관리 권한을 보유 하 고 있으며 Office 365의 고객 콘텐츠에 대 한 액세스 권한이 제로입니다. microsoft 엔지니어는 제한 된 시간 동안 고객 콘텐츠에 대 한 액세스를 제한 하 고 감사 하 고 보호할 수 있으며, 서비스 작업에 필요한 경우에만 가능 하며, microsoft의 선임 관리 (및 고객을 위해 고객 Lockbox 기능, 즉 고객에 게 라이선스가 부여 됩니다.

Microsoft는 여러 형태의 클라우드 전달을 사용 하 여 Office 365 등의 온라인 서비스를 제공 합니다.

- **공용 클라우드** -북미, 남미, 유럽, 아시아, 호주 등에서 호스팅되는 Office 365, Azure 및 기타 서비스의 다중 테 넌 트 버전을 포함 합니다.
- **국가별 클라우드** -중국의 office 365 (21vianet에서 운영 하는) 및 독일의 office 365 (예: Microsoft에서 운영 하는 sovereign 클라우드에) 외부에서 운영 하는 모든 회사 및 타사 클라우드를 포함 합니다. 독일어 데이터를 트러스티, 즉 Deutsche Telekom를 사용 하 여 Microsoft의 고객 데이터 및 고객 데이터에 대 한 액세스를 제어 하 고 모니터링 합니다.
- **정부 클라우드** -미국 정부 고객에 게 제공 되는 Office 365 및 Azure 서비스를 포함 합니다.

이 문서에서 설명 하는 것 처럼 Office 365 서비스에는 추가 정보를 포함 하 여 [exchange online](https://docs.microsoft.com/Exchange/exchange-online), [exchange online Protection](https://docs.microsoft.com/Office365/SecurityCompliance/eop/exchange-online-protection-overview), [SharePoint online](https://docs.microsoft.com/sharepoint/sharepoint-online) (비즈니스용 [OneDrive](https://docs.microsoft.com/OneDrive/onedrive)포함) 및 [비즈니스용 Skype](https://docs.microsoft.com/SkypeForBusiness/skype-for-business-online)가 포함 됩니다. 일부 [Yammer Enterprise](https://support.office.com/article/yammer-–-admin-help-e1464355-1f97-49ac-b2aa-dd320b179dbe?ui=en-US&rs=en-US&ad=US) 액세스 제어 다른 Office 365 서비스는이 문서의 범위를 벗어납니다.

## <a name="office-365-access-controls"></a>Office 365 액세스 제어
액세스 제어를 위해 Office 365 데이터는 고객 데이터 또는 다른 유형의 데이터로 분류 됩니다. 고객 데이터는 고객 콘텐츠 (전자 메일, SharePoint Online 콘텐츠, 인스턴트 메시지를 포함 하 여 office 365 사용자가 직접 만들거나 업로드 한 콘텐츠)와 같은 고객의 office 365 서비스 사용을 통해 고객을 대신해 서 제공 하는 모든 데이터입니다. 일정 항목, 문서 및 Office 365에 저장 된 연락처 및 EUII (최종 사용자 식별 정보) (사용자에 게 고유 하거나 개별 사용자에 게 linkable 하지만 고객 콘텐츠를 포함 하지 않는 데이터) 

기타 데이터 유형에는 계정 데이터 (관리자가 등록 하거나 구매할 때 제공 하는 정보, 신용 카드 세부 정보 등의 결제 데이터)가 포함 됩니다. 조직 차원 식별이 가능한 정보 (테 넌 트를 식별 하는 데 사용할 수 있는 데이터 또는 사용 현황 데이터, 개별 사용자에 게는 linkable 않으며 고객 콘텐츠는 포함 하지 않음) 및 시스템 메타 데이터 (구성 설정이 포함 된 서비스 로그 포함) 시스템 상태, Microsoft IP 주소 및 구독 및 테 넌 트에 대 한 기술 정보

Microsoft는 고객의 데이터 또는 액세스 제어 데이터에 대 한 승인 되지 않은 액세스 (예를 들어, 사용자의 콘텐츠 또는 EUII에 대 한 액세스를 포함 하 여 환경 내의 다른 데이터 또는 기능에 대 한 액세스를 관리 하는 데 사용 됨)에 액세스 제어 메커니즘을 설정 했습니다 Microsoft 암호, 보안 인증서 및 기타 인증 관련 데이터를 포함 하거나, Office 365 프로덕션 환경에 대 한 승인 되지 않은 물리적, 논리적 또는 원격 액세스를 제공 합니다.

Microsoft Office 365 for 운영에 사용 되는 액세스 제어는 다음과 같은 세 가지 범주로 분류할 수 있습니다.
- 격리 컨트롤
- 인적 컨트롤
- 기술 컨트롤

이러한 컨트롤을 결합 하면 Office 365에서 악의적인 작업을 방지 하 고 검색할 수 있습니다. Microsoft에서 사용 하는 격리, 인력 및 기술 제어 외에도 customer에서 구현 하는 컨트롤의 네 번째 범주를 사용할 수 있습니다.

Office 365에서는 온-프레미스 환경에서 데이터를 관리 하는 것과 같은 방법으로 데이터를 훨씬 더 관리할 수 있습니다. Office 365 조직에 등록 하는 사람은 자동으로 전역 관리자 (관리자)가 됩니다. 전역 관리자는 관리 포털의 모든 기능 (예: 관리 센터 및 원격 PowerShell)에 액세스할 수 있고, 사용자를 만들거나 편집 하 고, 관리자 역할을 다른 사용자에 게 할당 하 고, 사용자의 암호를 다시 설정 하 고, 도메인을 관리 하 고, 고객의 Lockbox를 승인 합니다. 기타 사항을 비롯 한 요청이 있습니다. 각 조직에는 최소 두 개의 관리자 계정을 지정 하 고 조직의 규모에 따라 다른 기능을 수행 하는 관리자를 여러 개 지정 하는 것이 좋습니다. 관리자 역할 및 사용 권한을 할당 하는 방법에 대 한 자세한 내용은 [office 365의 관리자 역할 할당](https://support.office.com/article/Assigning-admin-roles-in-Office-365-eac4d046-1afd-4f1a-85fc-8219c79e1504) 및 [office 365 관리자 역할 정보](https://support.office.com/article/Permissions-in-Office-365-DA585EEA-F576-4F55-A1E0-87090B6AAA9D)를 참조 하세요.


## <a name="related-links"></a>관련 링크

- [격리 컨트롤](office-365-isolation-controls.md)
- [인적 컨트롤](office-365-personnel-controls.md)
- [기술 컨트롤](office-365-technology-controls.md)
- [액세스 제어 모니터링 및 감사](office-365-monitoring-and-auditing-access-controls.md)
- [Yammer Enterprise 액세스 제어](office-365-yammer-enterprise-access-controls.md)